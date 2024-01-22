---
description: 'Last updated: 2.0.0 (18/01/2024)'
---

# Text button

A simple button designed for rendering text. Uses the `Text` component to render text. This is the default button; it will be used as `Button`.

## Usage

```tsx
import { Button } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Button 
            size="md"
            radius="sm"
            variant="light"
        >
            A *markdown* compatible text button!
        </Button>
    )
}
```

## Props

_Extends_ [_`PrimitiveButtonProps`_](primitive-button.md#props)_._

<table data-full-width="true"><thead><tr><th width="175">Property</th><th width="134">Type</th><th>Description</th></tr></thead><tbody><tr><td>children</td><td><code>string</code></td><td>Children of this component.</td></tr><tr><td>textProps</td><td><code>TextProps</code></td><td>Properties to apply to the <code>Text</code> component.</td></tr></tbody></table>

