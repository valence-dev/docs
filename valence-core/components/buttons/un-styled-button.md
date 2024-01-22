---
description: 'Last updated: 2.0.0 (18/01/2024)'
---

# Un-styled button

A very basic button component devoid of _all_ style, including the native browser-applied styles. Useful for building very unusual buttons.

## Usage

```tsx
import { UnstyledButton } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <UnstyledButton
            style={{
                // New styles here
            }}
        >
            // New children here
        </UnstyledButton>
    )
}
```

## Props

_Extends `GenericClickableProps`, `GenericClickableEventProps`, `PolymorphicButtonProps`, `GenericLayoutProps`._

_No unique props._
