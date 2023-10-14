# Polymorphism
Valence allows some of its components to become polymorphic, allowing different component types depending on the broad category of the component:

## `PolymorphicButton`
The `PolymorphicButton` component is a unique component of the bunch because it is wrapped in a [Framer motion component](https://www.framer.com/motion/), thus allowing it to take motion props from that library. `PolymorphicButton` allows for the following component types:

```ts
// Defaults to "button"
type PolymorphicButtonComponents = "a" | "button" | "link" | "span" | "div" | "input";
```
> The `link` type will transform the component into a [`Link` component from react-router-dom](https://reactrouter.com/en/main/components/link).


## `PolymorphicLayout`
The `PolymorphicLayout` component allows for the following component types:

```ts
// Defaults to "div"
export type PolymorphicLayoutComponents = "div" | "span" | "section" | "aside" | "form";
```

## `PolymorphicText`
The `PolymorphicText` component allows for the following component types:

```ts
// Defaults to "p"
export type PolymorphicTextComponents = "p" | "link" | "a" | "h1" | "h2" | "h3" | "h4" | "h5" | "h6" | "span" | "div";
```
> The `link` type will transform the component into a [`Link` component from react-router-dom](https://reactrouter.com/en/main/components/link).