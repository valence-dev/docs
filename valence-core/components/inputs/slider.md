---
description: 'Last updated: 2.0.0 (18/01/2024)'
---

# Slider

Sliders are a more visually-focused alternative to the [Number input](number-input.md). By default, the slider will include a number input without controls positioned directly to its right.

## Usage

```tsx
import { Slider } from "@valence-ui/core";

function MyComponent() { 
    const [value, setValue] = React.useState(25);

    return ( 
        <Slider
            value={value}
            setValue={setValue}
        />
    )
}
```

## Min, max & step

Sliders will default to a minimum of `0`, maximum of `100` and step of `1`. This can be modified using the `min`, `max` and `step` props, respectively:

```tsx
import { Slider } from "@valence-ui/core";

function MyComponent() { 
    const [value, setValue] = React.useState(0);

    return ( 
        <Slider
            value={value}
            setValue={setValue}
            
            min={-50}
            max={200}
            step={10}
        />
    )
}
```

## Moving or hiding the manual input

By default, a "manual" number input will be positioned directly to the right of the slider. This can be moved or hidden entirely using the `manualInputPosition` and `includeManualInput` props:

```tsx
import { Slider } from "@valence-ui/core";

function MyComponent() { 
    const [value, setValue] = React.useState(25);

    return ( 
        <Slider
            value={value}
            setValue={setValue}
            
            manualInputPosition="left"    // Move the number input
            includeManualInput={false}    // Hide the number input
        />
    )
}
```

## Complex handle

By passing `true` into the `showValue` prop, the value of the slider will be displayed on the slider handle itself. This is especially recommended if you have hidden the manual input.

```tsx
import { Slider } from "@valence-ui/core";

function MyComponent() { 
    const [value, setValue] = React.useState(25);

    return ( 
        <Slider
            value={value}
            setValue={setValue}
            
            showValue={true}
        />
    )
}
```

***

## Props

_Extends_ [_`GenericInputProps<number>`_](../../generics/generic-input-props.md) _and_ [_`SliderEventProps`_](slider.md#slidereventprops)_._

<table data-full-width="true"><thead><tr><th width="202">Property</th><th width="343">Type</th><th>Description</th></tr></thead><tbody><tr><td>min</td><td><code>number</code></td><td>The minimum value of this input. <code>0</code> by default.</td></tr><tr><td>max</td><td><code>number</code></td><td>The maximum value of this input. <code>100</code> by default.</td></tr><tr><td>step</td><td><code>number</code></td><td>The step value of this input. <code>1</code> by default.</td></tr><tr><td>showValue</td><td><code>boolean</code></td><td>Whether to show this slider's value on the thumb. <code>false</code> by default.</td></tr><tr><td>invert</td><td><code>invert</code></td><td>Whether to invert the direction of the slider. <code>false</code> by default.</td></tr><tr><td>includeManualInput</td><td><code>boolean</code></td><td>Whether to include a manual input with this slider. <code>true</code> by default.</td></tr><tr><td>manualInputPosition</td><td><code>"left" | "right"</code></td><td>The position of this manual input, if shown. <code>"right"</code> by default.</td></tr><tr><td>trackProps</td><td><code>Omit&#x3C;</code><a href="slider.md#slidertrackprops"><code>SliderTrackProps</code></a><code>, "state"></code></td><td>Optional props to pass to the track component.</td></tr><tr><td>thumbProps</td><td><code>Omit&#x3C;</code><a href="slider.md#sliderthumbprops"><code>SliderThumbProps</code></a><code>, "state"></code></td><td>Optional props to pass to the thumb component.</td></tr></tbody></table>

### SliderEventProps

_Accepts `T = number` as an optional type identifier._

<table data-full-width="true"><thead><tr><th width="174">Property</th><th width="410">Type</th><th>Description</th></tr></thead><tbody><tr><td>onAfterChange</td><td><code>(value: T, thumbIndex: number) => void</code></td><td>Callback fired after a thumb has been moved.</td></tr><tr><td>onBeforeChange</td><td><code>(value: T, thumbIndex: number) => void</code></td><td>Callback fired before a thumb is starting to move.</td></tr><tr><td>onChange</td><td><code>(value: T, thumbIndex: number) => void</code></td><td>Callback fired when the value of this input changes.</td></tr><tr><td>onSliderClick</td><td><code>(value: number) => void</code></td><td>Callback fired when any part of the slider is clicked.</td></tr></tbody></table>

### SliderTrackProps

_Extends `StyledFlexProps`._

<table data-full-width="true"><thead><tr><th width="167">Property</th><th width="354">Type</th><th>Description</th></tr></thead><tbody><tr><td>state (required)</td><td><code>{ index: number, value: number }</code></td><td><em>(internal use)</em></td></tr><tr><td>highlight</td><td><code>boolean</code></td><td>Whether to highlight this track. <code>false</code> by default.</td></tr></tbody></table>

### SliderThumbProps

_Extends `StyledFlexProps`._

<table data-full-width="true"><thead><tr><th width="164">Property</th><th width="527">Type</th><th>Description</th></tr></thead><tbody><tr><td>state (required)</td><td><code>{ index: number, valueNow: number, value: number }</code></td><td><em>(internal use)</em></td></tr><tr><td>showValue</td><td><code>boolean</code></td><td>Whether to show the value of this slider. <code>false</code> by default.</td></tr></tbody></table>
