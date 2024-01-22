---
description: 'Last updated: 2.0.0 (21/01/2024)'
---

# Styled Flex

The Styled Flex is a basic wrapper around the [Flex](./) component that provides basic theme-controlled styling props, such as the `variant`, `size` and `radius` props.

## Usage

```tsx
import { StyledFlex } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <StyledFlex
            variant="filled"
            size="xs"
            radius="xl"
            shadow
        >
            // Flex children...
        </StyledFlex>
    )
}
```

## Props

_Extends_ [_`FlexProps`_](./#props)_._

<table data-full-width="true"><thead><tr><th width="115">Property</th><th width="171">Type</th><th>Description</th></tr></thead><tbody><tr><td>variant</td><td><code>FillVariant</code></td><td>Sets the styling variant. Defaults to the theme default variant.</td></tr><tr><td>size</td><td><code>ComponentSize</code></td><td>Sets the size of this component. Defaults to the theme default size.</td></tr><tr><td>radius</td><td><code>ComponentSize</code></td><td>Sets the radius of this component. Defaults to the theme default border size.</td></tr><tr><td>shadow</td><td><code>boolean</code></td><td>Whether to include a shadow underneath this component. Will display the theme default shadow.</td></tr></tbody></table>
