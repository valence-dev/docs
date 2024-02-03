---
description: 'Last updated: 2.0.0 (22/01/2024)'
---

# Tooltip

## Usage

```tsx
import { Tooltip, Button } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Tooltip>
            <Tooltip.Trigger>
                <Button>
                    I'm a button!
                </Button>
            </Tooltip.Trigger>
            <Tooltip.Content>
                I'm a tooltip!
            </Tooltip.Content>
        </Tooltip>
    )
}
```

{% hint style="info" %}
Uncontrolled Tooltips will not show on [mobile breakpoints](../../../core-concepts/responsiveness.md).&#x20;
{% endhint %}

### Controlled

The Tooltip be used in a controlled fashion using the `useDisclosure` hook. The Tooltip will automatically hide when clicked away from (i.e. another element is focused), regardless of whether or not it is controlled.

```tsx
import { Tooltip, Button, useDisclosure } from "@valence-ui/core";

function MyComponent() { 
    const disclosure = useDisclosure(false);

    return ( 
        <Tooltip
            disclosure={disclosure}
        >
            <Tooltip.Trigger>
                <Button
                    onClick={() => disclosure.open()}
                >
                    I'm a button!
                </Button>
            </Tooltip.Trigger>
            <Tooltip.Content>
                I'm a tooltip!
            </Tooltip.Content>
        </Tooltip>
    )
}
```

### Custom content

The `Tooltip.Content` component accepts any valid JSX, or a raw string. This can be used to pass in icons or more complex content.

```tsx
import { Tooltip, Button, Icon } from "@valence-ui/core";
import { Icon123 } from "@tabler/icons-react";

function MyComponent() { 
    return ( 
        <Tooltip>
            <Tooltip.Trigger>
                <Button>
                    I'm a button!
                </Button>
            </Tooltip.Trigger>
            <Tooltip.Content>
                <Icon>
                    <Icon123 />
                </Icon>
            </Tooltip.Content>
        </Tooltip>
    )
}
```

***

## Props

### TooltipProps

_Extends_ [_`TooltipOptions`_](../../hooks/usetooltip.md)_._

<table data-full-width="true"><thead><tr><th width="185">Property</th><th width="132">Type</th><th>Description</th></tr></thead><tbody><tr><td>children (required)</td><td><code>ReactNode</code></td><td></td></tr></tbody></table>

### TooltipTriggerProps

<table data-full-width="true"><thead><tr><th width="183">Property</th><th width="204">Type</th><th>Description</th></tr></thead><tbody><tr><td>children (required)</td><td><code>ReactElement&#x3C;any></code></td><td></td></tr></tbody></table>

### TooltipContentProps

_Extends_ [_`StyledFlexProps`_](../layout/flex/styled-flex.md#props)_._

<table data-full-width="true"><thead><tr><th width="185">Property</th><th width="263">Type</th><th>Description</th></tr></thead><tbody><tr><td>children (required)</td><td><code>string | ReactNode</code></td><td></td></tr><tr><td>withShadow</td><td><code>boolean</code></td><td>Whether to display a shadow underneath the tooltip.</td></tr><tr><td>zIndex</td><td><code>CSSProperties["zIndex"]</code></td><td>The z-index of the tooltip.</td></tr></tbody></table>

***

## Changelog

* **2.2.0:** Uncontrolled tooltips will no longer show on [mobile breakpoints](../../hooks/usebreakpoint.md). Controlled tooltips (i.e. those that accept the `disclosure` prop) are unaffected.
