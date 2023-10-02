# Theming & the `ValenceProvider`
The `ValenceProvider` component provides a context value to all Valence components, and is essential for the functionality of the library as a whole. It must be rendered at the root of your application, and should only be used once.

```ts
import { ValenceContext } from "valence-ui";

function App() { 
  return (
    <ValenceProvider>
      <App />
    </ValenceProvider>
  )
}
```

The provider is then used as a context by all Valence components:

```ts
import { ValenceContext } from "../../../core";
import { useContext } from "react";

export function PrimitiveButton(props: PrimitiveButtonProps) { 
  const theme = useContext(ValenceContext);

  //...
}
```

The `ValenceContext` values can also be used by other components as well, so long as they are wrapped within the `ValenceProvider`!


## Props
`ValenceProvider` can have its default values overridden by supplying props to the provider:

| Prop                           | Type                                                    | Default                                      |
| ------------------------------ | ------------------------------------------------------- | -------------------------------------------- |
| `colors`                       | `ColorReactive[]`                                       | `DEFAULT_COLORS` ([see more](colors.md))     |
| `primaryColor`                 | `string`                                                | `"violet"`                                   |
| `defaultSize`                  | `ComponentSize`                                         | `"sm"`                                       |
| `defaultRadius`                | `ComponentSize`                                         | `"sm"`                                       |
| `defaultTransitionDuration`    | `React.CSSProperties["transitionDuration"]`             | `"0.1s"`                                     |
| `defaultShadow`                | `React.CSSProperties["boxShadow"]`                      | `"0px 10px 30px rgba(0, 0, 0, 0.2)"`         |
| `defaultVariant`               | `ButtonVariant`                                         | `"light"`                                    |
| `fontFamily`                   | N/A                                                     | N/A                                          |
| `fontFamily.default`           | `string`                                                | `"Inter, sans-serif"`                        |
| `fontFamily.heading`           | `string` (optional; falls back to `fontFamily.default`) | `undefined`                                  |
| `fontFamily.monospace`         | `string` (optional; falls back to `fontFamily.default`) | `"monospace"`                                |
| `sizeClasses`                  | N/A                                                     | N/A                                          |
| `sizeClasses.padding`          | `SizeClasses<React.CSSProperties["padding"]>`           | `{ xs: 10, sm: 15, md: 20, lg: 25, xl: 30 }` |
| `sizeClasses.height`           | `SizeClasses<React.CSSProperties["height"]>`            | `{ xs: 30, sm: 35, md: 40, lg: 50, xl: 60 }` |
| `sizeClasses.radius`           | `SizeClasses<React.CSSProperties["borderRadius"]>`      | `{ xs: 2, sm: 5, md: 10, lg: 15, xl: 25 }`   |
| `sizeClasses.fontSize`         | `SizeClasses<React.CSSProperties["fontSize"]>`          | `{ xs: 12, sm: 14, md: 16, lg: 18, xl: 20 }` |
| `titles`                       | N/A                                                     | N/A                                          |
| `titles.1`                     | `TextProps`                                             | `{ fontSize: 28, bold: true }`               |
| `titles.2`                     | `TextProps`                                             | `{ fontSize: 22, bold: true }`               |
| `titles.3`                     | `TextProps`                                             | `{ fontSize: 18, bold: true }`               |
| `titles.4`                     | `TextProps`                                             | `{ fontSize: 16, bold: true }`               |
| `titles.5`                     | `TextProps`                                             | `{ fontSize: 14, bold: true }`               |
| `titles.6`                     | `TextProps`                                             | `{ fontSize: 12, bold: true }`               |
| `breakpoints`                  | N/A                                                     | N/A                                          |
| `breakpoints.mobileWidth`      | `number`                                                | `800`                                        |
| `breakpoints.mobileTallHeight` | `number`                                                | `750`                                        |

> The `IValenceContext` type stores more information about these parameters.

## `getColor()` and `getFont()`
The `ValenceProvider` component exposes the `getColor()` and `getFont()` methods that can be used to retrieve the best colors and fonts for each situation. Using these is generally preferred over otherwise manually accessing these values via the `color` and `fontFamily` properties because they provide fallbacks for when the requested color or font is not available.

```ts
import { ValenceContext } from "valence-ui";

function Demo() { 
  const theme = useContext(ValenceContext);

  return (
    <div style={{ fontFamily: theme.getFont("heading") }}>
      What a strange conundrum
    </div>
  )
}
```
> In this situation, if no `heading` font is available, the `default` font will be used instead.

```ts
import { ValenceContext } from "valence-ui";

function Demo() { 
  const theme = useContext(ValenceContext);

  return (
    <>
      <div style={{ color: theme.getColor("red") }}>
        Theme colors are preferred and will be returned
        if they exist.
      </div>

      <div style={{ color: theme.getColor("#FF00FF") }}>
        Hex codes are also accepted!
      </div>

      <div style={{ color: theme.getColor("aubergine") }}>
        Aubergine is not a color included in the theme, 
        so the default color will be used instead.
      </div>
    </>
  )
}
```
> [See more about colors.](colors.md)