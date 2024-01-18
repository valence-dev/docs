---
description: 'Last updated: 2.0.0 (18/01/2024)'
---

# Text area

## Usage

```tsx
import { Textarea } from "@valence-ui/core";

function MyComponent() { 
    const [value, setValue] = React.useState("");

    return ( 
        <Textarea
            value={value}
            setValue={setValue}
        />
    )
}
```

### Allow resize

```tsx
import { Textarea } from "@valence-ui/core";

function MyComponent() { 
    const [value, setValue] = React.useState("");

    return ( 
        <Textarea
            value={value}
            setValue={setValue}
            
            minHeight={100}
            maxHeight={250}
            minWidth={300}
            maxWidth={500}
        />
    )
}
```

## Props

_Extends_ [_`GenericTextInputProps`_](../../generics/generic-input-props.md) _and_ [_`GenericTextInputEventProps`_](../../generics/generic-input-props.md)_._

<table data-full-width="true"><thead><tr><th width="153">Property</th><th width="292">Type</th><th>Description</th></tr></thead><tbody><tr><td>autoComplete</td><td><code>boolean</code></td><td>Whether the value of the input can be automatically completed by the browser/OS. Defaults to <code>false</code>.</td></tr><tr><td>spellCheck</td><td><code>boolean</code></td><td>Whether the input is subject to spell checking by the browser/OS. Defaults to <code>true</code>.</td></tr><tr><td>cols</td><td><code>number</code></td><td>Specifies the visible width of the input.</td></tr><tr><td>rows</td><td><code>number</code></td><td>Specifies the visible number of lines in the input.</td></tr><tr><td>wrap</td><td><code>LineWrapBehaviour</code></td><td>Specifies how the text in the input is to be wrapped.</td></tr><tr><td>resize</td><td><code>ResizeBehaviour</code></td><td>Specifies how the input can be resized. Defaults to <code>"none"</code>.</td></tr><tr><td>minHeight</td><td><code>CSSProperties["minHeight"]</code></td><td>The minimum height of the input.</td></tr><tr><td>maxHeight</td><td><code>CSSProperties["maxHeight"]</code></td><td>The maximum height of the input.</td></tr><tr><td>minWidth</td><td><code>CSSProperties["minWidth"]</code></td><td>The minimum width of the input.</td></tr><tr><td>maxWidth</td><td><code>CSSProperties["maxWidth"]</code></td><td>The maximum width of the input.</td></tr><tr><td>grow</td><td><code>boolean</code></td><td>Shorthand for <code>flex-grow = 1</code>.</td></tr></tbody></table>

### `LineWrapBehaviour`

```json
"soft" | "hard" | "off"
```

### `ResizeBehaviour`

```json
"none" | "both" | "horizontal" | "vertical"
```
