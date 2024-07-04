---
description: 'Last updated: 3.0.0 (04/07/2024)'
---

# Grid

The Grid is a component system used to interface directly with the CSS `grid` properties. This system includes the `Grid` itself, and the `Grid.Item` sub-component.

## Usage

```tsx
import { Grid } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Grid
            columns={3}
            rows={2}
            gap={10}
        >
            <Grid.Item
                column="auto"
            >
                // Grid item children...
            </Grid.Item>
            
            // More Grid items...
        </Grid>
    )
}
```

## Props

_Extends `GenericGridProps` and `PolymorphicLayoutProps`._

No unique props.

### GridItemProps

_Extends `GenericGridItemProps` and `PolymorphicLayoutProps`._

***

## Changelog

* **3.0.0:** now uses `rows` and `columns` props instead of `templateRows` and `templateColumns` props; these props can now accept `number` types and will create that many `1fr` columns.
