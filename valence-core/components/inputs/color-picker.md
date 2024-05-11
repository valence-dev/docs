---
description: 'Added: 2.5.0 | Last updated: 2.5.0 (11/05/2024)'
---

# Color Picker

## Usage

```tsx
import { ColorPicker } from "@valence-ui/core";

function MyComponent() { 
    const [value, setValue] = React.useState("red");

    return ( 
        <ColorPicker
            value={value}
            setValue={setValue}
        />
    )
}
```

***

## Props

_Extends `GenericInputProps<string>` and `ColorPickerEventProps`._

<table data-full-width="true"><thead><tr><th width="162"></th><th width="299"></th><th></th></tr></thead><tbody><tr><td>colors</td><td><code>Color[]</code></td><td>A list of colors to choose from. If left unset, will use the theme default color list (excluding <code>permaWhite</code> and <code>permaBlack</code>).</td></tr><tr><td>gap</td><td><code>number</code></td><td>Sets the gap between colors. <code>5</code> by default.</td></tr><tr><td>wrap</td><td><code>CSSProperties["flexWrap"]</code></td><td>How the colors will wrap within the container. Defaults to <code>"nowrap"</code>.</td></tr><tr><td>swatchMotion</td><td><code>MotionBehaviourProps</code></td><td>Motion props to apply to the swatch buttons.</td></tr></tbody></table>
