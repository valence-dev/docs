---
description: 'Last updated: 2.0.0 (21/01/2024)'
---

# Title

Built on the [Text](text.md) component, the Title is a markdown-compatible and semantically accurate header/title component.

## Usage

```tsx
import { Title } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Title>
            I'm a **markdown-compatible** title!
        </Title>
    )
}
```

### Header order

The `order` prop controls which header element the title becomes (`h1`-`h6`). This defaults to `1`, thus making it a `h1` by default.

```tsx
import { Title } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Title
            order={2}
        >
            I'm a **markdown-compatible** title!
        </Title>
    )
}
```

***

## Props

_Extends_ [_`TextProps`_](text.md#props)_._

<table data-full-width="true"><thead><tr><th width="117">Property</th><th width="243">Type</th><th>Description</th></tr></thead><tbody><tr><td>order</td><td><code>1 | 2 | 3 | 4 | 5 | 6</code></td><td>Sets the order of the title.</td></tr></tbody></table>
