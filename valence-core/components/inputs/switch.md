---
description: 'Last updated: 2.0.0 (18/01/2024)'
---

# Switch

## Usage

```tsx
import { Switch } from "@valence-ui/core";

function MyComponent() { 
    const [value, setValue] = React.useState(false);

    return ( 
        <Switch
            value={value}
            setValue={setValue}
            label="My switch!"
        />
    )
}
```

## Props

_Extends_ [_`GenericInputProps<boolean>`_](../../generics/generic-input-props.md)_._

<table data-full-width="true"><thead><tr><th width="177">Property</th><th width="238">Type</th><th>Description</th></tr></thead><tbody><tr><td>label</td><td><code>string</code></td><td>The label associated with this input.</td></tr><tr><td>grow</td><td><code>boolean</code></td><td>Shorthand for <code>flex-grow = 1</code>.</td></tr><tr><td><code>buttonProps</code></td><td><code>PrimitiveButtonProps</code></td><td>Optional props to pass to the <code>Button</code> container component.</td></tr><tr><td><code>labelProps</code></td><td><code>TextProps</code></td><td>Optional props to pass to the <code>Text</code> label component.</td></tr></tbody></table>

