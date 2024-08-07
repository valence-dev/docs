---
description: 'Last updated: 3.0.0 (04/07/2024)'
---

# Grid

## GenericGridProps

_Extends_ [_`GenericLayoutProps`_](layout.md#genericlayoutprops)_._

<table data-full-width="true"><thead><tr><th width="165.00260078023405">Property</th><th width="388">Type</th><th>Description</th></tr></thead><tbody><tr><td>grid</td><td><code>CSSProperties["grid"]</code></td><td>Sets <code>grid</code> css property.</td></tr><tr><td>gap</td><td><code>CSSProperties["gap"]</code></td><td>Sets <code>gap</code> css property.</td></tr><tr><td>rowGap</td><td><code>CSSProperties["rowGap"]</code></td><td>Sets <code>row-gap</code> css property.</td></tr><tr><td>columnGap</td><td><code>CSSProperties["columnGap"]</code></td><td>Sets <code>column-gap</code> css property.</td></tr><tr><td>template</td><td><code>CSSProperties["gridTemplate"]</code></td><td>Sets <code>grid-template</code> css property.</td></tr><tr><td>rows</td><td><code>number | CSSProperties["gridTemplateRows"]</code></td><td>Sets <code>grid-template-rows</code> css property.</td></tr><tr><td>columns</td><td><code>number | CSSProperties["gridTemplateColumns"]</code></td><td>Sets <code>grid-template-columns</code> css property.</td></tr><tr><td>templateAreas</td><td><code>CSSProperties["gridTemplateAreas"]</code></td><td>Sets <code>grid-template-areas</code> css property.</td></tr><tr><td>autoRows</td><td><code>CSSProperties["gridAutoRows"]</code></td><td>Sets <code>grid-auto-rows</code> css property.</td></tr><tr><td>autoColumns</td><td><code>CSSProperties["gridAutoColumns"]</code></td><td>Sets <code>grid-auto-columns</code> css property.</td></tr><tr><td>autoFlow</td><td><code>CSSProperties["gridAutoFlow"]</code></td><td>Sets <code>grid-auto-flow</code> css property.</td></tr><tr><td>justifyItems</td><td><code>CSSProperties["justifyItems"]</code></td><td>Sets <code>justify-items</code> css property.</td></tr><tr><td>justifyContent</td><td><code>CSSProperties["justifyContent"]</code></td><td>Sets <code>justify-content</code> css property.</td></tr><tr><td>alignItems</td><td><code>CSSProperties["alignItems"]</code></td><td>Sets <code>align-items</code> css property.</td></tr><tr><td>alignContent</td><td><code>CSSProperties["alignContent"]</code></td><td>Sets <code>align-content</code> css property.</td></tr></tbody></table>

## GenericGridItemProps

Extends [`GenericLayoutProps`](layout.md#genericlayoutprops).

<table data-full-width="true"><thead><tr><th width="140">Property</th><th width="344">Type</th><th>Description</th></tr></thead><tbody><tr><td>area</td><td><code>CSSProperties["gridArea"]</code></td><td>Sets <code>grid-area</code> css property.</td></tr><tr><td>column</td><td><code>CSSProperties["gridColumn"]</code></td><td>Sets <code>grid-column</code> css property.</td></tr><tr><td>columnStart</td><td><code>CSSProperties["gridColumnStart"]</code></td><td>Sets <code>grid-column-start</code> css property.</td></tr><tr><td>columnEnd</td><td><code>CSSProperties["gridColumnEnd"]</code></td><td>Sets <code>grid-column-end</code> css property.</td></tr><tr><td>row</td><td><code>CSSProperties["gridRow"]</code></td><td>Sets <code>grid-row</code>css property.</td></tr><tr><td>rowStart</td><td><code>CSSProperties["gridRowStart"]</code></td><td>Sets <code>grid-row-start</code> css property.</td></tr><tr><td>rowEnd</td><td><code>CSSProperties["gridRowEnd"]</code></td><td>Sets <code>grid-row-end</code> css property.</td></tr><tr><td>justify</td><td><code>CSSProperties["justifySelf"]</code></td><td>Sets <code>justify-self</code> css property.</td></tr><tr><td>align</td><td><code>CSSProperties["alignSelf"]</code></td><td>Sets <code>align-self</code> css property.</td></tr><tr><td>place</td><td><code>CSSProperties["placeSelf"]</code></td><td>Sets <code>place-self</code> css property.</td></tr><tr><td>order</td><td><code>CSSProperties["order"]</code></td><td>Sets <code>order</code> css property.</td></tr></tbody></table>

***

## Changelog

* **3.0.0:** Replaced `templateRows` and `templateColumns` props with `rows` and `columns` props, respectively; allowed them to accept `number` types as well.
