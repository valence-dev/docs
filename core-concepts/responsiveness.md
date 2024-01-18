---
description: 'Last updated: 2.0.0 (16/01/2024)'
---

# Responsiveness

Valence has been designed from the ground up to support responsiveness as a design paradigm. This means that every component's are _responsive_, allowing every component to respond in real-time to the size of the window or device the user is viewing your page on.

In practice, this means you can write one codebase that will dynamically adapt to the device your users are using, allowing you to write concise code that works everywhere.

> **This system has changed dramatically in v2:** this was previously known as Reactiveness, and was far less powerful than it is now.

## Using responsive props

To tell if a prop is responsive, you can view the type-hint in your code editor. It will generally by in the following form:

```tsx
prop: Responsive<Type>
```

Responsive props can act "normally", in the sense that their regular types can be supplied to them, like so:

```tsx
export function MyApp() { 
    return ( 
        <MyComponent 
            size={20}
        />
    )
}
```

Responsive props have the unique property that they can be expanded, thus allowing you to supply up to five unique values for five breakpoints:

```tsx
export function MyApp() { 
    return ( 
        <MyComponent
            size={{
                // Shown here in ascending size
                mobile: 15,
                tablet: 17,
                default: 20,    // Effectively the same as not expanding
                desktopLarge: 25,
                tv: 30,
            }}
        />
    )
}
```

This is called "expanded form", and when like this the `default` parameter is required, and all other parameters are optional. If you choose not to supply values for a particular breakpoint, Valence will fallback until it reaches a defined value, or the `default` value.

## About fallbacks

"Falling back" occurs when a value for a particular breakpoint is not supplied in the prop, thus Valence must calculate the "nearest" valid prop to use instead. The following order of operations applies for each:

* **Mobile:** mobile -> tablet -> default
* **Tablet:** tablet -> default
* **Desktop Large:** desktopLarge -> default
* **TV:** tv -> desktopLarge -> default

## Making a component responsive

Valence exposes a critical type that allows for all of a component's props to become responsive; `MakeResponsive`. This type will transform any type into a `Responsive` type, allowing you to give it custom props based on common device breakpoints.

Valence also exposes the `useResponsiveProps()` hook, which can be used to de-structure a component's props such that the correct prop for the current breakpoint is returned.&#x20;

To fully understand what this means, let's take a look at an example:

```tsx
import { MakeResponsive, useResponsiveProps } from "@valence-ui/core";

export type MyComponentProps = {
    /* The size of this component, in pixels */
    size: number;
}  
      
export function MyComponent(props: MakeResponsive<MyComponentProps>) { 
    const { 
        size 
    } = useResponsiveProps<MyComponentProps>(props);
    
    console.log(size);
    
    return (</>)
}

// Elsewhere...

export function MyApp() { 
    return ( 
        <MyComponent
            size={{
                default: 20,
                mobile: 15,
                tablet: 17
            }}
        />
    )
}
```

Running the code above, you'll find that `MyComponent` will log one of the sizes, depending on the current screen breakpoint. You can see this in action by increasing or decreasing the width of your window.&#x20;

While the above example is mundane, it demonstrates a powerful feature of the `MakeResponsive` type and `useResponsiveProps` hook, and that is to take a mundane type and make it responsive.

## De-structuring responsive props

You may find that, during the de-structuring process, you need to define responsive behavior for a prop by default. To do so, another custom hook, `useResponsiveProp()` must be invoked:

```tsx
export function MyComponent(props: MakeResponsive<MyComponentProps>) { 
    const { 
        size = useResponsiveProp({
            default: 20,
            mobile: 15,
            tablet: 17
        })
    } = useResponsiveProps<MyComponentProps>(props);
```

The `useResponsiveProp` hook is nearly identical to the `useResponsiveProps` hook (note the extra `s`), except that the former will only calculate the correct value for an individual prop, not a complete object's worth.

## Modifying breakpoints

Modifying the breakpoints used to calculate responsive props can be done by overriding the `breakpoints` property on the `ValenceProvider`, like so:

```tsx
export function MyApp() { 
    return ( 
        <ValenceProvider
            breakpoints={{
                mobileWidth: 480,
                tabletWidth: 768,
                // Default is inferred between these two
                desktopLargeWidth: 1024,
                tvWidth: 1440,
            }}
        >
    )
}
```

Note that _all_ breakpoints must be supplied if you are to override at least one.
