---
description: 'Last updated: 2.0.0 (18/01/2024)'
---

# Number input

## Usage

```tsx
import { NumberInput } from "@valence-ui/core";

function MyComponent() { 
    const [value, setValue] = React.useState(0);

    return ( 
        <NumberInput
            value={value}
            setValue={setValue}
        />
    )
}
```

## Min, max & step

```tsx
import { NumberInput } from "@valence-ui/core";

function MyComponent() { 
    const [value, setValue] = React.useState(4);

    return ( 
        <NumberInput
            value={value}
            setValue={setValue}
            
            min={0}
            max={10}
            step={2}
        />
    )
}
```

## Hiding or modifying controls

The controls can be entirely hidden using the `showControls` prop:

```tsx
import { NumberInput } from "@valence-ui/core";

function MyComponent() { 
    const [value, setValue] = React.useState(0);

    return ( 
        <NumberInput
            value={value}
            setValue={setValue}
            
            showControls={false}
        />
    )
}
```

Additionally, the icons used can be overridden by the `controlIcons` prop:

```tsx
import { NumberInput } from "@valence-ui/core";
import { IconMinus, IconPlus } from "@tabler/icons-react";

function MyComponent() { 
    const [value, setValue] = React.useState(0);

    return ( 
        <NumberInput
            value={value}
            setValue={setValue}
            
            controlIcons={{
                up: <IconPlus />,
                down: <IconMinus />
            }}
        />
    )
}
```

## Props

Extends [`GenericInputProps<number>`](../../generics/generic-input-props.md) and [`GenericTextInputEventProps`](../../generics/generic-input-props.md).

<table data-full-width="true"><thead><tr><th width="155">Property</th><th width="401">Type</th><th>Description</th></tr></thead><tbody><tr><td>icon</td><td><code>ReactNode</code></td><td>An icon to display at the left side of this input.</td></tr><tr><td>placeholder</td><td><code>string</code></td><td>Text that appears in this input when it has no value.</td></tr><tr><td>min</td><td><code>number</code></td><td>The minimum value of this input.</td></tr><tr><td>max</td><td><code>number</code></td><td>The maximum value of this input.</td></tr><tr><td>step</td><td><code>number</code></td><td>The step value of this input. Defaults to <code>1</code>.</td></tr><tr><td>showControls</td><td><code>boolean</code></td><td>Whether the stepper controls are shown.</td></tr><tr><td>controlIcons</td><td><code>{ up?: ReactNode, down?: ReactNode }</code></td><td>Sets custom icons for the stepper control buttons.</td></tr><tr><td>grow</td><td><code>boolean</code></td><td>Shorthand for <code>flex-grow = 1</code>.</td></tr><tr><td>inputStyle</td><td><code>CSSProperties</code></td><td>Optional styles to apply to the input component.</td></tr></tbody></table>
