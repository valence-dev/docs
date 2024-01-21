---
description: 'Last updated: 2.0.0 (21/01/2024)'
---

# Header

## Usage

```tsx
import { Header, Title } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Header>
            <Title>
                Page title!
            </Title>
        </Header>
    )
}
```

### Changing the height

By default, the Header will start at `100px` tall (`150px` on [`mobile`](../../../core-concepts/responsiveness.md)), and will compact to `75px` when the user scrolls from the top of the screen. This behavior can be overridden with the `height` and `compactHeight` props, respectively.

```tsx
import { Header, Title } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Header
            height={200}
            compactHeight={50}
        >
            <Title>
                Page title!
            </Title>
        </Header>
    )
}
```

Compacting on scroll can be entirely disabled with the `compact` prop being set to `false`. By default, the Header will only compact in `mobile` breakpoints

***

## Props

_Extends_ [_`FlexProps`_](flex/#props)_._

<table data-full-width="true"><thead><tr><th width="169">Property</th><th width="287">Type</th><th>Description</th></tr></thead><tbody><tr><td>height</td><td><code>number</code></td><td>Defines the height of this header. Defaults to <code>100</code> for regular devices, and <code>150</code> for <code>mobile</code> devices.</td></tr><tr><td>compactHeight</td><td><code>number</code></td><td>The height of this header when it has been compacted. Defaults to <code>75</code>.</td></tr><tr><td>position</td><td><code>CSSProperties["position"]</code></td><td>Defines the position of this header.</td></tr><tr><td>compact</td><td><code>boolean</code></td><td>Defines the breakpoints in which the header is allowed to compact. By default this is <code>true</code> for mobile devices, and <code>false</code> for all other devices.</td></tr></tbody></table>
