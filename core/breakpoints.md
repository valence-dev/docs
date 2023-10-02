# Breakpoints
Building a unified application or website can be unweildy when working with devices of multiple size classes. Valence helps to alleviate some of this pain by integrating breakpoint-sensitive props into many components, and providing an intuitive API to create and manage breakpoint-sensitive props for your own components.

Valence currently checks for two breakpoints, `mobile` and `mobileTall`. These values can be set in the `ValenceProvider`:
```ts
import { ValenceProvider } from "valence-ui";

function Demo() { 
  return ( 
    <ValenceProvider
      breakpoints={{
        mobileWidth: 800,
        mobileTallHeight: 750
      }}
    >
      <App />
    </ValenceProvider>
  )
}
```
> Both are measured in pixels and are based upon the viewport width; the shown values are default.

As the names suggest, the `mobileWidth` parameter is the width at which the device is considered "mobile", and the `mobileTallHeight` parameter is the height at which a mobile device is considered to be "tall".


## Breakpoint-sensitive props
Valence exposes the `ReactiveProp<T>` type, which is used under the hood to turn an existing type into a breakpoint-sensitive one. It has the following structure:
```ts
export type ReactiveProp<T> = T | {
  default: T;
  mobile?: T;
  mobileTall?: T;
};

// Elsewhere...
export type ReactivePadding = ReactiveProp<React.CSSProperties["padding"]>;

// In practice
const padding: ReactivePadding = "10px";
// OR
const otherPadding: ReactivePadding = {
  default: "10px",
  mobile: "5px",
  mobileTall: "8px",
}
```
> Supplying the `10px` directly to the padding variable is functionally the same as setting it as the `default` property.

In practice, this allows for a succinct yet highly extensible way for components to recieve props based upon the viewport's size. The `Flex` component makes use of this:
```ts
import { Flex } from "valence-ui";

function Demo() { 
  return ( 
    <Flex
      width={100}
      height={{ default: 100, mobile: 50 }}
    >
      Hello there
    </Flex>
  )
}
```
Most "reactive" props are labelled with the **[REACTIVE]** tag in their JSDom comments.


## Fallback priority
Because the `mobile` and `mobileTall` properties are not required, the following behaviour applies for how falling back occurs:

| Property     | Criteria                               | Fallback                              |
|--------------|----------------------------------------|---------------------------------------|
| `mobileTall` | If the device is mobile **and** tall     | `mobileTall` -> `mobile` -> `default` |
| `mobile`     | If the device is mobile and **not** tall | `mobile` -> `default`                 |
| `default`    | All other circumstances                | N/A                                   |


## Using this system
When creating your own components, you may want to utilise Valence's breakpoint system. Valence exposes the `getReactiveProp()` method and the `useBreakpoint` hook for this purpose. 

The `getReactiveProp()` method requires two parameters, `prop: ReactiveProp`, and `breakpoint: Breakpoint`. It will calculate the fallback based upon the properties available on the `prop` parameter and the criteria met by the `breakpoint` parameter, returning the correct prop for the scenario. To help generate the `breakpoint`, the `useBreakpoint` hook is exposed and can be called in the component and passed directly into this function, like so:

```ts
import { useBreakpoint, ReactiveProp, getReactiveProp } from "valence-ui";

type DemoProps = { 
  fontSize: ReactiveProp<number>;
}

function Demo(props: DemoProps) { 
  const breakpoint = useBreakpoint();

  const styles: CSSProperties = { 
    fontSize: getReactiveProp(props.fontSize, breakpoint),
  }

  //...
}
```

This can also be used in more complex circumstances, such as with setting with the `getTextColor()` method:

```ts
import { useBreakpoint, ReactiveProp, getReactiveProp, getTextColor, ButtonVariant, ValenceContext } from "valence-ui";
import { useContext } from "react";

type DemoProps = { 
  color: ReactiveProp<string>;
  variant: ReactiveProp<ButtonVariant>;
}

function Demo(props: DemoProps) { 
  const theme = useContext(ValenceContext);
  const breakpoint = useBreakpoint();

  const styles: CSSProperties = { 
    color: getTextColor(
      getReactiveProp(props.color, breakpoint),
      getReactiveProp(props.variant, breakpoint),
      theme
    )
  }

  //...
}
```