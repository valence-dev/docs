---
description: 'Last updated: 2.0.0 (21/01/2024)'
---

# Space

## Usage

```tsx
import { Space } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Space
            height={20}
        />
    )
}
```

### Horizontal context

The Space component can also be used within horizontal [Flex](flex/) components; simply use the `width` prop instead.

```tsx
import { Space } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Space
            width={20}
        />
    )
}
```

### Grow

The Space component can grow to fill any blank space within the parent container using the `grow` prop. This will automatically adjust to horizontal or vertical contexts.

```tsx
import { Space } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Space
            grow
        />
    )
}
```
