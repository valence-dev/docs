---
description: 'Last updated: 2.0.0 (18/01/2024)'
---

# Primitive button

This is a foundational button component used by most other buttons, but should not be used directly unless you intend to make your own buttons.

## Usage

```tsx
import { PrimitiveButton } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <PrimitiveButton
            size="md"
            radius="sm"
            variant="light"
        >
            My first button!
        </PrimitiveButton>
    )
}
```

## Props

_Extends_ [_`GenericButtonProps`_](../../generics/generic-button-props.md)_._&#x20;

<table data-full-width="true"><thead><tr><th width="174">Property</th><th width="237">Type</th><th>Description</th></tr></thead><tbody><tr><td>motion</td><td><code>MotionBehaviourProps</code></td><td>Defines motion behavior for this button. This will automatically be overridden if the user has reduced motion enabled on their device.</td></tr></tbody></table>
