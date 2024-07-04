---
description: 'Last updated: 3.0.0 (04/07/2024)'
---

# Flex Center

The Flex Center component is designed to create a [Flex](./) that is centered within its parent component. Under the hood, it uses two Flex components, an "inner" and "outer", to achieve this style.

## Usage

```tsx
import { FlexCenter } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <FlexCenter>
            // Flex children...
        </FlexCenter>
    )
}
```

## Props

_Extends_ [_`FlexProps`_](./#props)_._

<table data-full-width="true"><thead><tr><th width="129">Property</th><th width="303">Type</th><th>Description</th></tr></thead><tbody><tr><td>innerWidth</td><td><code>FlexProps["width"]</code></td><td>Width of the inner Flex component. Defaults to <code>50%</code>.</td></tr><tr><td>innerProps</td><td><code>Omit&#x3C;FlexProps, "children"></code></td><td>Optional props to pass to the inner Flex component.</td></tr></tbody></table>
