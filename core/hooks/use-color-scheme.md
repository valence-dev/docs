# `useColorScheme`
To dynamically support numerous color schemes, the `useColorScheme` hook is utilised by the [`ValenceProvider`](../core/valence-provider.md) to automatically adapt to the user's system theme.

This hook also exposes a number of useful secondary functions, as defined in the `UseColorSchemeOutput` type:

```ts
type UseColorSchemeOutput = {
  colorScheme: ColorScheme;
  isDarkMode: boolean;
  isLightMode: boolean;
  toggle: () => void;
  setDark: () => void;
  setLight: () => void;
}
```

## Usage
```ts
import { useColorScheme } from "valence-ui";

function Demo() { 
  const { colorScheme } = useColorScheme();

  console.log(colorScheme === "dark");
  // Results will vary, of course.
}
```