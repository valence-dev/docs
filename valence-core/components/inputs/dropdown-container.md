---
description: 'Last updated: 2.0.0 (18/01/2024)'
---

# Dropdown container

{% hint style="danger" %}
This is a foundational component and is not designed to be used by itself. Only use this if you intend to make your own inputs.
{% endhint %}

The Dropdown container is used to create dropdowns, and handles most of the styling and dropdown logic for the [Select input](select-input.md).&#x20;

Under the hood, this component is a wrapper around the [Input container](input-container.md), with additional components provided by [Floating UI](https://floating-ui.com/) to create the dropdown itself.

## Usage

```tsx
import { DropdownContainer } from "@valence-ui/core";

function MyComponent() { 

    return ( 
        <DropdownContainer 
            options={["hello", "world"]}        
            // For brevity, most suggested props
            // are not included.
        >
            // Your sub-component here.
            // It should have little to no styling,
            // as this is passed to the InputContainer.
        </DropdownContainer>
    )
}
```

If no `children` are supplied, a Text component rendering the selected option or a placeholder will be shown instead.

## Props

_Extends_ [_`InputContainerProps`_](input-container.md) _and_ [_`DropdownContainerEventProps`_](dropdown-container.md#dropdowncontainereventprops)_._

<table data-full-width="true"><thead><tr><th width="183">Property</th><th width="339">Type</th><th>Description</th></tr></thead><tbody><tr><td>options (required)</td><td><code>Option[]</code></td><td>A list of options to display.</td></tr><tr><td>placeholder</td><td><code>string</code></td><td>The placeholder text to display when no option is selected.</td></tr><tr><td>selected</td><td><code>number | null</code></td><td>The currently selected option.</td></tr><tr><td>setSelected</td><td><code>(option: number | null) => void</code></td><td>A callback to set the selected option.</td></tr><tr><td>highlighted</td><td><code>number | null</code></td><td>The currently highlighted option.</td></tr><tr><td>setHighlighted</td><td><code>(option: number | null) => void</code></td><td>A callback to set the highlighted option.</td></tr><tr><td>icon</td><td><code>ReactNode</code></td><td>An icon to display in the input container.</td></tr><tr><td>secondaryIcon</td><td><code>ReactNode</code></td><td>A secondary icon to display in the input container.</td></tr><tr><td>dropdownStyle</td><td><code>CSSProperties</code></td><td>Optional styles to pass to the dropdown.</td></tr></tbody></table>

### DropdownContainerEventProps

<table data-full-width="true"><thead><tr><th width="121">Property</th><th width="275">Type</th><th>Description</th></tr></thead><tbody><tr><td>onSelect</td><td><code>(option: Option) => void</code></td><td>A callback fired when an item is selected.</td></tr></tbody></table>
