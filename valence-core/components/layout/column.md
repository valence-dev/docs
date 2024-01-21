---
description: 'Last updated: 2.0.0 (21/01/2024)'
---

# Column

Built on the back of the Grid component system, the Column system is a light wrapper that is useful to create a simpler grid.

## Usage

```tsx
import { Column } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Column.Container
            columns={3}
            rows={2}
            gap={10}
        >
            <Column>
                // Column children...
            </Column>
            
            // More Columns...
        </Column.Container>
    )
}
```

## Props

### ColumnProps

_Extends_ [_`FlexProps`_](flex/#props)_._&#x20;

No unique props.

### ColumnContainerProps

_Extends_ [_`GridProps`_](grid.md#props) _and `GenericLayoutProps`._

<table data-full-width="true"><thead><tr><th width="114">Property</th><th width="115">Type</th><th>Description</th></tr></thead><tbody><tr><td>columns</td><td><code>number</code></td><td>Sets the number of columns in the grid. <code>2</code> by default.</td></tr><tr><td>rows</td><td><code>number</code></td><td>Sets the number of rows in the grid. <code>1</code> by default.</td></tr></tbody></table>
