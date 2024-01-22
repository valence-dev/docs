---
description: 'Last updated: 2.0.0 (21/01/2024)'
---

# Icon

## Usage

```tsx
import { Icon } from "@valence-ui/core";
import { Icon123 } from "@tabler/icons-react";

function MyComponent() { 
    return ( 
        <Icon>
            <Icon123 />
        </Icon>
    )
}
```

### Override default styles

```tsx
import { Icon } from "@valence-ui/core";
import { Icon123 } from "@tabler/icons-react";

function MyComponent() { 
    return ( 
        <Icon
            size={30}
            stroke={2}
            color="blue"
        >
            <Icon123 />
        </Icon>
    )
}
```

{% hint style="info" %}
Icon colors are pulled from theme colors by default. If the `color` prop is not supplied, the icon will inherit color from its parent component.
{% endhint %}

***

## Props

<table data-full-width="true"><thead><tr><th width="125">Property</th><th width="129">Type</th><th>Description</th></tr></thead><tbody><tr><td>size</td><td><code>number</code></td><td>Size of the icon. Defaults to theme default icon size.</td></tr><tr><td>stroke</td><td><code>number</code></td><td>Stroke width of the icon. <code>1.5</code> by default.</td></tr><tr><td>color</td><td><code>string</code></td><td>Color of the icon. Inherits by default.</td></tr><tr><td>children</td><td><code>ReactNode</code></td><td></td></tr></tbody></table>
