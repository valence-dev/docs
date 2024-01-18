---
description: 'Last updated: 2.0.0 (18/01/2024)'
---

# Select input

## Usage

```tsx
import { SelectInput, Option } from "@valence-ui/core";

function MyComponent() { 
    const [value, setValue] = React.useState<Option | null>("option1");

    return ( 
        <SelectInput
            value={value}
            setValue={setValue}
            options={[
                "option1",
                "option2",
                "option3"
            ]}
        />
    )
}
```

## Custom options

The `Option` type is a composite type that will accept a `string` (as shown above), or an object that includes a `label`, `value` and `icon`, of which `value` is required:

```tsx
import { SelectInput, Option } from "@valence-ui/core";

function MyComponent() { 
    const [value, setValue] = React.useState<Option | null>("option1");

    return ( 
        <SelectInput
            value={value}
            setValue={setValue}
            options={[
                "option1",
                { value: "option2", label: "Option 2" },
                "option3"
            ]}
        />
    )
}
```

Here, `"Option 2"` will be displayed instead of `"option2"`, allowing you to map value to readable strings.

```tsx
import { SelectInput, Option } from "@valence-ui/core";
import { IconCloud } from "@tabler/react-icons";

function MyComponent() { 
    const [value, setValue] = React.useState<Option | null>("option1");

    return ( 
        <SelectInput
            value={value}
            setValue={setValue}
            options={[
                "option1",
                { value: "option2", icon: <IconCloud /> },
                "option3"
            ]}
        />
    )
}
```

Here, the `IconCloud` will be displayed to the left of the option in the dropdown, and the input will use that icon if `option2` is selected. If the option is selected, the icon will be replaced with a check icon in the dropdown.

***

## Props

_Extends_ [_`GenericInputProps<Option | null>`_](../../generics/generic-input-props.md) _and `SelectInputEventProps`._

<table data-full-width="true"><thead><tr><th width="181.33333333333331">Property</th><th width="172">Type</th><th>Description</th></tr></thead><tbody><tr><td>options (required)</td><td><code>Option[]</code></td><td>A list of options to supply for the content of this input.</td></tr><tr><td>icon</td><td><code>ReactNode</code></td><td>An icon to display at the left side of this input.</td></tr><tr><td>placeholder</td><td><code>string</code></td><td>The placeholder text to display when this input is empty.</td></tr><tr><td>actionicon</td><td><code>ReactNode</code></td><td>An icon to display at the right side of this input.</td></tr><tr><td>grow</td><td><code>boolean</code></td><td>Shorthand for <code>flex-grow = 1</code>.</td></tr><tr><td>dropdownStyle</td><td><code>CSSProperties</code></td><td>Optional styles to apply to the dropdown container.</td></tr></tbody></table>

### SelectInputEventProps

_Extends_ [_`GenericTextInputEventProps`_](../../generics/generic-input-props.md)_._

<table data-full-width="true"><thead><tr><th width="134">Property</th><th width="336">Type</th><th>Description</th></tr></thead><tbody><tr><td>onSelect</td><td><code>(value: Option | null) => void</code></td><td>Callback to be called when an option is selected.</td></tr></tbody></table>
