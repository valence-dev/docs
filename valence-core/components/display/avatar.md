---
description: 'Last update: 2.0.0 (21/01/2024)'
---

# Avatar

The Avatar component builds upon the [Image](image.md) component, appearing as a round image with a custom icon placeholder.

## Usage

```tsx
import { Avatar } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Avatar
            src="https://images.unsplash.com/photo-1419242902214-272b3f66ee7a?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=720&q=80"
            alt="A nice avatar!"
        />
    )
}
```

### Overriding default props

```tsx
import { Avatar } from "@valence-ui/core";
import { IconUserCircle } from "@tabler/icons-react";

function MyComponent() { 
    return ( 
        <Avatar
            src="https://images.unsplash.com/photo-1419242902214-272b3f66ee7a?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=720&q=80"
            alt="A nice avatar!"
            
            square={false}
            radius="sm"
            placeholder={<IconUserCircle />}
        />
    )
}
```

### Setting a fill variant

```tsx
import { Avatar } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Avatar
            src="https://images.unsplash.com/photo-1419242902214-272b3f66ee7a?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=720&q=80"
            alt="A nice avatar!"
            
            variant="filled"     // Defaults to theme default
        />
    )
}
```

### Customising the placeholder

```tsx
import { Avatar } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Avatar
            src="https://images.unsplash.com/photo-1419242902214-272b3f66ee7a?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=720&q=80"
            alt="A nice avatar!"
            
            placeholderColor="blue"
        />
    )
}
```

***

## Props

_Extends_ [_`ImageProps`_](image.md#props)_._

<table data-full-width="true"><thead><tr><th width="182">Property</th><th width="255">Type</th><th>Description</th></tr></thead><tbody><tr><td>placeholderColor</td><td><code>CSSProperties["color"]</code></td><td>Placeholder color for this avatar.</td></tr><tr><td>variant</td><td><code>FillVariant</code></td><td>Defines the fill variant for this avatar. Defaults to theme default fill variant.</td></tr></tbody></table>
