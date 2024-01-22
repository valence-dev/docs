---
description: 'Last updated: 2.0.0 (21/01/2024)'
---

# Grid

The Grid is a component system used to interface directly with the CSS `grid` properties. This system includes the `Grid` itself, and the `Grid.Item` sub-component.

## Usage

```tsx
import { Grid } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Grid
            templateColumns="1fr 1fr 1fr"
            templateRows="1fr 1fr"
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
