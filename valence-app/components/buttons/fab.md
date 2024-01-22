---
description: 'Last updated: 2.0.0 (22/01/2024)'
---

# FAB

The Floating Action Button (or FAB) is a specialized button that floats relative to the user's viewport.

## Usage

```tsx
import { FAB } from "@valence-ui/app";
import { Icon123 } from "@tabler/icons-react";

function MyComponent() { 
    return ( 
        <FAB>
            <Icon123 />
        </FAB>
    )
}
```

### Float position & offset

The position and offset of the FAB can be modified using the `vPosition`, `hPosition` and `offset` props.

```tsx
import { FAB } from "@valence-ui/app";
import { Icon123 } from "@tabler/icons-react";

function MyComponent() { 
    return ( 
        <FAB
            vPosition="bottom"
            hPosition="right"
            offset={20}
        >
            <Icon123 />
        </FABon>
    )
}
```

***

## Props

_Extends_ [_`IconButtonProps`_](../../../valence-core/components/buttons/icon-button.md#props)_._

<table data-full-width="true"><thead><tr><th width="134">Property</th><th width="263">Type</th><th>Description</th></tr></thead><tbody><tr><td>vPosition</td><td><code>"top" | "bottom"</code></td><td>Vertical position of this button on the page. Defaults to <code>"bottom"</code>.</td></tr><tr><td>hPosition</td><td><code>"left" | "right"</code></td><td>Horizontal position of this button on the page. Defaults to <code>"right"</code>.</td></tr><tr><td>offset</td><td><code>number</code></td><td>The distance in <code>px</code> this button sits from the edge of the page. Defaults to <code>20</code>.</td></tr><tr><td>zIndex</td><td><code>CSSProperties["zIndex"]</code></td><td>Sets <code>z-index</code> css property. Defaults to <code>100</code>.</td></tr></tbody></table>
