---
description: 'Last updated: 2.5.0 (11/05/2024)'
---

# Unstyled button

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

<table data-full-width="true"><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td>motion</td><td><code>MotionBehaviourProps</code></td><td>Defines motion behavior for this button. This will automatically be overridden if the user has reduced motion enabled on their device.</td></tr></tbody></table>
