---
description: 'Added: 2.5.0 | Last updated: 2.5.0 (11/05/2024)'
---

# Color Swatch

A `ColorSwatch` is a simple component that allows the display of a single color. It uses the [`getHex`](../../../core-concepts/color/) method under the hood, so will accept a color stored on the [Valence palette](../../fundamentals/the-valenceprovider.md), a hex value (denoted with `#------`), or any valid web color as a fallback.

## Usage

```tsx
import { ColorSwatch } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <ColorSwatch
            color="red"
        />
    )
}
```

***

## Props

<table data-full-width="true"><thead><tr><th width="162"></th><th width="259"></th><th></th></tr></thead><tbody><tr><td>color (required)</td><td><code>CSSProperties["color"]</code></td><td>The color to display. Will default to the theme default color.</td></tr><tr><td>opacity</td><td><code>SwatchOpacity</code></td><td>The opacity of the color to display. Will default to completely filled.</td></tr><tr><td>size</td><td><code>ComponentSize</code></td><td>The size of the swatch. Defaults to theme default.</td></tr><tr><td>radius</td><td><code>ComponentSize</code></td><td>The size of the swatch. Defaults to <code>"xl"</code>.</td></tr><tr><td>withOutline</td><td><code>boolean</code></td><td>Whether to display the swatch with an outline. Defaults to <code>true</code>.</td></tr></tbody></table>
