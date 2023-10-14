# `useBreakpoint`
Designed to complement Valence's [breakpoint architecture](../core/breakpoints.md), this hooks generates a `Breakpoint` object, calculated with the current viewport width and height.

## Usage
```ts
import { useBreakpoint } from "valence-ui";

function Demo() {
  const breakpoint = useBreakpoint();

  console.log(breakpoint);
  // { isMobile: false, isMobileTall: false }
}
```