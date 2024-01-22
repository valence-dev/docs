---
description: 'Last updated: 2.0.0 (21/01/2024)'
---

# Loader

## Usage

```tsx
import { Loader } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Loader />
    )
}
```

### Custom size & color

By default, the size and color of the Loader will be inherited from the ValenceProvider.

```tsx
import { Loader } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Loader 
            size="lg"
            color="blue"
        />
    )
}
```

***

## Props

_Extends `GenericProps`._

<table data-full-width="true"><thead><tr><th width="120">Property</th><th width="256">Type</th><th>Description</th></tr></thead><tbody><tr><td>size</td><td><code>ComponentSize</code></td><td>Sets element size class. Defaults to theme default.</td></tr><tr><td>color</td><td><code>CSSProperties["color"]</code></td><td>Color of the loader. Defaults to theme default.</td></tr></tbody></table>
