---
description: 'Last updated: 2.0.0 (22/01/2024)'
---

# UseBreakpoint

{% hint style="info" %}
This hook forms part of the [Responsiveness utility system](../../core-concepts/responsiveness.md). For more information about how this system works, see [Responsiveness](../../core-concepts/responsiveness.md).
{% endhint %}

`useBreakpoint` is a hook that returns the current responsive breakpoint. The hook will use breakpoint attributes defined in the `ValenceProvider` to determine the current device breakpoint.

## Usage

```tsx
import { useBreakpoint, Button } from "@valence-ui/core";

function MyComponent() { 
    const { isMobile } = useBreakpoint();
    
    return ( 
        <Button
            color={isMobile ? "blue" : "red"}
        >
            I'm a button!
        </Button>
    )
}
```

## Return type

<table data-full-width="true"><thead><tr><th width="172">Attribute</th><th width="117">Type</th><th>Description</th></tr></thead><tbody><tr><td>isMobile</td><td><code>boolean</code></td><td>Is the current breakpoint <code>"mobile"</code>?</td></tr><tr><td>isTablet</td><td><code>boolean</code></td><td>Is the current breakpoint <code>"tablet"</code>?</td></tr><tr><td>isDefault</td><td><code>boolean</code></td><td>Is the current breakpoint <code>"default"</code>?</td></tr><tr><td>isDesktopLarge</td><td><code>boolean</code></td><td>Is the current breakpoint <code>"desktopLarge"</code>?</td></tr><tr><td>isTV</td><td><code>boolean</code></td><td>Is the current breakpoint <code>"tv"</code>?</td></tr></tbody></table>
