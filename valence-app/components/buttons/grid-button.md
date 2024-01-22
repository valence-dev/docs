---
description: 'Last updated: 2.0.0 (22/01/2024)'
---

# Grid Button

The Grid Button is a large square button with a central icon and room for short descriptive text underneath. It is, as the name suggests, best used within a [Grid](../../../valence-core/components/layout/grid.md) system.

## Usage

```tsx
import { GridButton } from "@valence-ui/app";
import { Icon123 } from "@tabler/icons-react";

function MyComponent() { 
    return ( 
        <GridButton
            icon={<Icon123 />}
        >
            Grid button
        </GridButton>
    )
}
```

### Change icon position

```tsx
import { GridButton } from "@valence-ui/app";
import { Icon123 } from "@tabler/icons-react";

function MyComponent() { 
    return ( 
        <GridButton
            icon={<Icon123 />}
            iconPosition="bottom"
        >
            Grid button
        </GridButton>
    )
}
```

***

## Props

_Extends_ [_`TextButtonProps`_](../../../valence-core/components/buttons/text-button.md#props)_._

<table data-full-width="true"><thead><tr><th width="159">Property</th><th width="197">Type</th><th>Description</th></tr></thead><tbody><tr><td>icon (required)</td><td><code>ReactNode</code></td><td>The icon to include with this button.</td></tr><tr><td>iconPosition</td><td><code>"top" | "bottom"</code></td><td>The position of the icon relative to the text. Defaults to <code>"top"</code>.</td></tr></tbody></table>
