---
description: 'Last updated: 2.2.0 (02/02/2024) | Added: 2.2.0'
---

# Overflow Container

The Overflow Container allows its children content to scroll freely within a set parent's boundaries. By default, this container will only scroll vertically and will grow to 100% of its parent's width and height.

## Usage

```tsx
import { OverflowContainer } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <OverflowContainer
            direction="vertical"
            width="100%"
            height="100%"
        >
            // Container children...
        </OverflowContainer>
    )
}
```

***

## Props

_Extends `GenericProps`._

<table data-full-width="true"><thead><tr><th width="133">Property</th><th width="262">Type</th><th>Description</th></tr></thead><tbody><tr><td>direction</td><td><code>OverflowDirection</code></td><td>The direction the container allows its inner content to scroll. Defaults to <code>"vertical"</code>.</td></tr><tr><td>width</td><td><code>CSSProperties["width"]</code></td><td>The width of the container.</td></tr><tr><td>height</td><td><code>CSSProperties["height"]</code></td><td>The height of the container.</td></tr><tr><td>innerProps</td><td><a href="flex/#props"><code>FlexProps</code></a></td><td>Optional props to pass to the inner flex component.</td></tr></tbody></table>

### OverflowDirection

```tsx
type OverflowDirection = "horizontal" | "vertical" | "both" | "none";
```
