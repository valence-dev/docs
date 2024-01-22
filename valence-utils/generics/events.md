---
description: 'Last updated: 2.0.0 (22/01/2024)'
---

# Events

## MouseClickEvents

<table data-full-width="true"><thead><tr><th width="157">Property</th><th width="360">Type</th><th>Description</th></tr></thead><tbody><tr><td>onClick</td><td><code>(event: React.MouseEvent) => void</code></td><td>Fires on a mouse click event.</td></tr><tr><td>onDoubleClick</td><td><code>(event: React.MouseEvent) => void</code></td><td>Fires on a mouse double-click event.</td></tr></tbody></table>

## MouseEvents

<table data-full-width="true"><thead><tr><th width="165">Property</th><th width="365">Type</th><th>Description</th></tr></thead><tbody><tr><td>onMouseDown</td><td><code>(event: React.MouseEvent) => void</code></td><td>Fires when a mouse button is pressed down on this element.</td></tr><tr><td>onMouseUp</td><td><code>(event: React.MouseEvent) => void</code></td><td>Fires when a mouse button is released on this element.</td></tr><tr><td>onMouseOver</td><td><code>(event: React.MouseEvent) => void</code></td><td>Fires when a mouse enters this element and its children.</td></tr><tr><td>onMouseEnter</td><td><code>(event: React.MouseEvent) => void</code></td><td>Fires when a mouse enters this element.</td></tr><tr><td>onMouseLeave</td><td><code>(event: React.MouseEvent) => void</code></td><td>Fires when a mouse leaves this element.</td></tr><tr><td>onMouseMove</td><td><code>(event: React.MouseEvent) => void</code></td><td>Fires when a mouse moves while over this element.</td></tr></tbody></table>

## PointerEvents

<table data-full-width="true"><thead><tr><th width="172">Property</th><th width="378">Type</th><th>Description</th></tr></thead><tbody><tr><td>onPointerDown</td><td><code>(event: React.PointerEvent) => void</code></td><td>Fires when a pointer becomes active on this element. This is for triggering drag events as this event is only called once on touchscreen devices.</td></tr><tr><td>onPointerUp</td><td><code>(event: React.PointerEvent) => void</code></td><td>Fires when a pointer is no longer active on this element.</td></tr><tr><td>onPointerCancel</td><td><code>(event: React.PointerEvent) => void</code></td><td>Fires when the browser determines there are unlikely to be any more pointer events.</td></tr><tr><td>onPointerEnter</td><td><code>(event: React.PointerEvent) => void</code></td><td>Fires when a pointing device is moved onto this element and its children.</td></tr><tr><td>onPointerLeave</td><td><code>(event: React.PointerEvent) => void</code></td><td>Fires when a pointing device is moved off this element.</td></tr><tr><td>onPointerMove</td><td><code>(event: React.PointerEvent) => void</code></td><td>Fires when a pointer moves while over this element.</td></tr><tr><td>onPointerOver</td><td><code>(event: React.PointerEvent) => void</code></td><td>Fires when a pointer is moved onto this element.</td></tr></tbody></table>

## FocusEvents

<table data-full-width="true"><thead><tr><th width="115">Property</th><th width="359">Type</th><th>Description</th></tr></thead><tbody><tr><td>onFocus</td><td><code>(event: React.FocusEvent) => void</code></td><td>Fires when this element receives focus.</td></tr><tr><td>onBlur</td><td><code>(event: React.FocusEvent) => void</code></td><td>Fires when this element loses focus.</td></tr></tbody></table>

## KeyboardEvents

<table data-full-width="true"><thead><tr><th width="137">Property</th><th width="389">Type</th><th>Description</th></tr></thead><tbody><tr><td>onKeyDown</td><td><code>(event: React.KeyboardEvent) => void</code></td><td>Fires when a key is pressed down.</td></tr><tr><td>onKeyPress</td><td><code>(event: React.KeyboardEvent) => void</code></td><td>Fires after a key is pressed and released.</td></tr><tr><td>onKeyUp</td><td><code>(event: React.KeyboardEvent) => void</code></td><td>Fires when a key is released.</td></tr></tbody></table>
