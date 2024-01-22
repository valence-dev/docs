---
description: 'Last updated: 2.0.0 (22/01/2024)'
---

# Color types

## SwatchOpacity

```tsx
type SwatchOpacity = "weak" | "medium" | "strong";
```

## Swatch

<table data-full-width="true"><thead><tr><th width="122">Attribute</th><th width="353">Type</th><th>Description</th></tr></thead><tbody><tr><td>base</td><td><code>string</code></td><td>The base color of the swatch. This should be a six-digit hex code starting with a <code>#</code>.</td></tr><tr><td>opacity</td><td><code>[key in</code> <a href="color-types.md#swatchopacity"><code>SwatchOpacity</code></a><code>]: string</code></td><td>The opacity levels for the swatch. Each of these should be two-digit hex codes, and will be appended to the base color to create the various shades of the color.</td></tr></tbody></table>

## Color

<table data-full-width="true"><thead><tr><th width="177">Attribute</th><th width="115">Type</th><th>Description</th></tr></thead><tbody><tr><td>key (required)</td><td><code>string</code></td><td>The key of the color. This should be a unique string that identifies the color.</td></tr><tr><td>default (required)</td><td><a href="color-types.md#swatch"><code>Swatch</code></a></td><td>The default swatch for the color. This is used when the current color scheme is light, or when the color does not have a dark swatch.</td></tr><tr><td>dark</td><td><code>Swatch</code></td><td>The dark swatch for the color. This is used when the current color scheme is dark. If this is not provided, the default swatch will be used.</td></tr></tbody></table>
