---
description: 'Last updated: 2.0.0 (22/01/2024)'
---

# UseResponsiveProps

{% hint style="info" %}
This hook forms part of the [Responsiveness utility system](../../core-concepts/responsiveness.md). For more information about how this system works, see [Responsiveness](../../core-concepts/responsiveness.md).
{% endhint %}

`useResponsiveProps` is a hook that returns the current props based on the current device breakpoint. This should be used before de-structuring responsive props in a component, and will automatically convert them to their mother type.

This hook is used internally in nearly every component, and forms the backbone of the [Responsiveness](../../core-concepts/responsiveness.md) system introduced in Valence 2.

## Usage

```tsx
import { useResponsiveProps, ComponentSize, MakeResponsive, Button } from "@valence-ui/core";

type MyProps = { 
    size: ComponentSize,
}

function MyComponent(props: MakeResponsive<MyProps>) { 
    const { 
        size = "md",
    } = useResponsiveProps<MyProps>(props);
    
    return ( 
        <Button
            size={size}
        >
            I'm a button!
        </Button>
    )
}
```

### Setting responsive defaults

While de-structuring, it may be advantageous to provide responsive defaults for a prop. To achieve this, use nested `useResponsiveProps` hooks, like so:

```tsx
import { useResponsiveProps, ComponentSize, MakeResponsive, Button } from "@valence-ui/core";

type MyProps = { 
    size: ComponentSize,
}

function MyComponent(props: MakeResponsive<MyProps>) { 
    const { 
        size = useResponsiveProps({
            default: "md",
            mobile: "lg",
            tv: "xs",
        }),
    } = useResponsiveProps<MyProps>(props);
    
    return ( 
        <Button
            size={size}
        >
            I'm a button!
        </Button>
    )
}
```

