---
description: 'Last updated: 2.0.0 (22/01/2024)'
---

# Overlay

## BackdropFilter

```tsx
type BackdropFilter = "blur" | "dot-blur" | "none";
```

## GenericOverlayBackgroundProps

Extends [`GenericProps`](global.md#genericprops) and `PolymorphicLayoutProps`.

<table data-full-width="true"><thead><tr><th width="177">Property</th><th width="349">Type</th><th>Description</th></tr></thead><tbody><tr><td>closeOnClick</td><td><code>boolean</code></td><td>Whether to close this overlay when it is clicked.</td></tr><tr><td>backdropFilter</td><td><code>BackdropFilter</code></td><td>A filter to apply to the page contents behind the overlay.</td></tr><tr><td>backgroundColor</td><td><code>CSSProperties["backgroundColor"]</code></td><td>Sets <code>background-color</code> css property.</td></tr><tr><td>padding</td><td><code>CSSProperties["padding"]</code></td><td>Sets <code>padding</code> css property.</td></tr><tr><td>zIndex</td><td><code>CSSProperties["zIndex"]</code></td><td>Sets <code>z-index</code> css property.</td></tr></tbody></table>

## GenericOverlayHeaderProps

<table data-full-width="true"><thead><tr><th width="153">Property</th><th width="101">Type</th><th>Description</th></tr></thead><tbody><tr><td>title (required)</td><td><code>string</code></td><td>The title of this overlay.</td></tr></tbody></table>

## GenericOverlayProps

Extends [`GenericLayoutProps`](layout.md) and `PolymorphicLayoutProps`.

<table data-full-width="true"><thead><tr><th width="239">Property</th><th width="336">Type</th><th>Description</th></tr></thead><tbody><tr><td>title (required)</td><td><code>string</code></td><td>The title of this overlay.</td></tr><tr><td>header</td><td><code>(props:</code> <a href="overlay.md#genericoverlayheaderprops"><code>GenericOverlayHeaderProps</code></a><code>) => ReactNode</code></td><td>Optionally replace the default header with a custom component.</td></tr><tr><td>closeOnOverlayClick</td><td><code>boolean</code></td><td>Whether to close this overlay when the overlay is clicked.</td></tr><tr><td>closeOnEscape</td><td><code>boolean</code></td><td>Whether to close this overlay when the escape key is pressed.</td></tr><tr><td>lockScroll</td><td><code>boolean</code></td><td>Whether to lock scrolling when this overlay is open.</td></tr><tr><td>withShadow</td><td><code>boolean</code></td><td>Whether to include a shadow underneath the overlay.</td></tr><tr><td>radius</td><td><a href="global.md#componentsize"><code>ComponentSize</code></a></td><td>Sets the <code>border-radius</code> css property.</td></tr><tr><td>overlayBackgroundProps</td><td><a href="overlay.md#genericoverlaybackgroundprops"><code>GenericOverlayBackgroundProps</code></a></td><td>Optional props to pass to the overlay background component.</td></tr></tbody></table>
