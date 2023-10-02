# Colors
Valence has a color system that it uses to style components. Colors are exposed to the [`ValenceProvider`](valence-provider.md) as an array of `ColorReactive` objects. Each `ColorReactive` has the following structure:
```ts
type ColorReactive = {
  /** The key to use when referencing this color in code */
  key: string;
  /** Information about this color in light/default mode */
  default: Color;
  /** Information about this color in dark mode */
  dark?: Color;
}
```

This enables the theme to provide the correct `Color` based on the current color scheme (light or dark). The `Color` type the has the following structure:

```ts
type Color = {
  /** The base, opaque version of this color */
  base: string;

  /** Two-digit HEX values to append to the base color to provide transparency effects */
  opacity: {
    /** Defines a very "diluted" value for this colour */
    weak: string;
    /** Mid-range color opacity */
    medium: string;
    /** Strong color opacity */
    strong: string;
  }
}
```
As can be seen here, Valence departs from similar libraries (such as [Mantine](https://mantine.dev/theming/colors/)) in that it uses opacity effects as opposed to different shades of the same color. The rationale behind this is that it is a more concise yet more "layerable" and therefore extensible solution. This means that multiple layered components can all have their background colors visible.


## Retrieving colors
`ValenceProvider` exposes the `getColor()` method that can be used to retrieve the best color for this situation. This method serves a number of functions:
- Adapting to the current color scheme
- Providing fallbacks in the case of unknown colors
The method has one parameter, `key: string`, which is used to find the closest color it can. If the provided color exists on the `ValenceProvider`, then it will be returned. If it does not, but a valid hex code (ie. starting with `#`) is supplied, a `Color` created with that hex code is created. Failing both those criteria, the method will return the provider's `primaryColor`.


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


## Color schemes
Because Valence natively (and somewhat forcibly) supports color schemes, the `white` and `black` colors invert when converting between light and dark schemes. In the vast majority of circumstances, this is a handy feature, however the `permaWhite` and `permaBlack` colors have also been exposed, and as the name suggests they will not change based on the current scheme.

In some circumstances it is useful to desaturate or change perferred opacity values for darker environments, thus `ColorReactive` exposes two separate `Colors` (`default` and `dark`), which will be chosen based on the current scheme. The `dark` color property is notably not required, and the `ValenceProvider` will automatically fall back to the `default` property in this case.


## Default color reference
The following colors are provided by default as part of the `ValenceProvided`:
```ts
const
  BASE_WHITE: Color = { base: "#EFEEEE", opacity: { weak: "19", medium: "2A", strong: "A0" } },
  BASE_BLACK: Color = { base: "#11181C", opacity: { weak: "19", medium: "30", strong: "5A" } };
const DEFAULT_COLORS: ColorReactive[] = [
  {
    key: "white",
    default: BASE_WHITE,
    dark: BASE_BLACK,
  },
  {
    key: "black",
    default: BASE_BLACK,
    dark: BASE_WHITE,
  },
  {
    key: "permaWhite",
    default: BASE_WHITE,
  },
  {
    key: "permaBlack",
    default: BASE_BLACK,
  },
  {
    key: "violet",
    default: { base: "#7C5DDE", opacity: { weak: "20", medium: "4A", strong: "A0" } },
    dark: { base: "#8F76DE", opacity: { weak: "20", medium: "4A", strong: "A0" } }
  },
  {
    key: "red",
    default: { base: "#E5524F", opacity: { weak: "20", medium: "4A", strong: "A0" } },
    dark: { base: "#E26765", opacity: { weak: "20", medium: "4A", strong: "A0" } }
  },
]
```
> Adding your own colors will append to this list, unless you wish to override a particular key.


## Fine-tuned control
### `getReactiveColor()`
This method is used under the hood by the `ValenceProvider`. It accepts two parameters, `colorReactive: ColorReactive` and `isDarkMode: boolean = false`, and will return the best `Color` from the provided `ColorReactive` to suit the current scheme. This method also provides a fallback to the `light` color in cases where the `dark` color was not provided.

### `getUnidentifiedHexColor()`
This method is used under the hood to generate a `Color` from a provided hex code. It accepts a `hex: string` parameter, and will return a `Color` in the following form:
```ts
{
  base: hex,
  {
    weak: "20",
    medium: "4A",
    strong: "A0"
  }
}
```
> These opacity values are standard across most default colors.