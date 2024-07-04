---
description: 'Last updated: 3.0.0 (04/07/2024)'
---

# Primitive button

{% hint style="danger" %}
This is a foundational component and should not be used by itself. Only use this component if you intend to make your own buttons.
{% endhint %}

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

_Extends_ [_`GenericButtonProps`_](../../generics/generic-button-props.md)_._

<table data-full-width="false"><thead><tr><th width="131.01472995090015">Property</th><th width="238">Type</th><th>Description</th></tr></thead><tbody><tr><td>motion</td><td><code>MotionBehaviourProps</code></td><td>Defines motion behavior for this button. This will automatically be overridden if the user has reduced motion enabled on their device.</td></tr><tr><td>float</td><td><a href="../../hooks/usefloating.md#props"><code>UseFloatingProps</code></a></td><td>Defines floating behavior for this button.</td></tr></tbody></table>

## Changelog

* **3.0.0:** Added the `float` property, allowing all buttons to float like a FAB.
