---
description: 'Last updated: 2.0.0 (18/01/2024)'
---

# Range slider

The Range slider is an expansion of the single-handle [Slider](slider.md) component. This component can simultaneously support a virtually limitless number of handles.

## Usage

```tsx
import { RangeSlider } from "@valence-ui/core";

function MyComponent() { 
    const [value, setValue] = React.useState([25, 50, 75]);

    return ( 
        <RangeSlider 
            value={value}
            setValue={setValue}
        />
    )
}
```

> The number of values handled (and therefore handles displayed) is determined by the number of initial values passed to the `useState`.

### Minimum distance & pearling

You can stop one thumb from pushing its peers when they collide by using the `pearling` prop. Additionally, the `minDistance` prop controls the minimum distance that two thumbs can become. If `pearling=true`, the thumbs will begin pushing one another around once they reach the `minDistance` from one another.

```tsx
import { RangeSlider } from "@valence-ui/core";

function MyComponent() { 
    const [value, setValue] = React.useState([25, 50, 75]);

    return ( 
        <RangeSlider 
            value={value}
            setValue={setValue}
            
            pearling={false}
            minDistance={10}
        />
    )
}
```

### Other modifications

Other modifications can be made to the Range slider using the same props as the regular Slider.

[See the Slider reference.](slider.md)

***

## Props

_Extends_ [_`GenericInputProps<number[]>`_](../../generics/generic-input-props.md) _and_ [_`SliderEventProps<number[]>`_](slider.md#slidereventprops)_._

<table data-full-width="true"><thead><tr><th width="203">Property</th><th width="358">Type</th><th>Description</th></tr></thead><tbody><tr><td>min</td><td><code>number</code></td><td>The minimum value of this input. <code>0</code> by default.</td></tr><tr><td>max</td><td><code>number</code></td><td>The maximum value of this input. <code>100</code> by default.</td></tr><tr><td>step</td><td><code>number</code></td><td>The step value of this input. <code>1</code> by default.</td></tr><tr><td>minDistance</td><td><code>number</code></td><td>The minimum distance between the two thumbs. <code>0</code> by default.</td></tr><tr><td>pearling</td><td><code>boolean</code></td><td>Whether the active thumb will push other thumbs. <code>true</code> by default.</td></tr><tr><td>showValue</td><td><code>boolean</code></td><td>Whether to show this slider's value on the thumb. <code>false</code> by default.</td></tr><tr><td>invert</td><td><code>boolean</code></td><td>Whether to invert the direction of the slider. <code>false</code> by default.</td></tr><tr><td>includeManualInput</td><td><code>boolean</code></td><td>Whether to include a manual input with this slider. <code>true</code> by default.</td></tr><tr><td>manualInputPosition</td><td><code>"left" | "right"</code></td><td>The position of this manual input, if shown. <code>"right"</code> by default.</td></tr><tr><td>trackProps</td><td><code>Omit&#x3C;</code><a href="slider.md#slidertrackprops"><code>SliderTrackProps</code></a><code>, "state"></code></td><td>Optional props to pass to track components.</td></tr><tr><td>thumbProps</td><td><code>Omit&#x3C;</code><a href="slider.md#sliderthumbprops"><code>SliderThumbProps</code></a><code>, "state"></code></td><td>Optional props to pass to thumb components.</td></tr></tbody></table>
