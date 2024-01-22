---
description: 'Last updated: 2.0.0 (22/01/2024)'
---

# UseColors

{% hint style="info" %}
This hook forms part of the [Color utility system](../../core-concepts/color/). For more information about how this system works, see [Color](../../core-concepts/color/).
{% endhint %}

`useColors` is a hook that allows the usage of Valence colors in any component. All components must be a child of the `ValenceProvider` to function correctly.

## Usage

```tsx
import { useColors, Button } from "@valence-ui/core";
import { CSSProperties } from "react";

function MyComponent() { 
    const { getHex } = useColors();

    const buttonStyle: CSSProperties = { 
        color: getHex("blue", "weak"),
    }
    
    return ( 
        <Button
            style={buttonStyle}
        >
            I'm a button!
        </Button>
    )
}
```

## Return type

<table data-full-width="true"><thead><tr><th width="135">Attribute</th><th width="405">Type</th><th>Description</th></tr></thead><tbody><tr><td>getSwatch</td><td><code>(key: string | undefined):</code> <a href="../../core-concepts/color/color-types.md#swatchopacity"><code>Swatch</code></a> <code>| undefined</code></td><td>Gets the swatch for the given color key. If the color does not exist, this will return <code>undefined</code>.</td></tr><tr><td>getHex</td><td><code>(key: string | undefined, opacity?:</code> <a href="../../core-concepts/color/color-types.md#swatchopacity"><code>SwatchOpacity</code></a><code>): string | undefined</code></td><td>Gets the hex code for the given color key. If the color does not exist, this will return the key as-is.</td></tr><tr><td>getBgHex</td><td><code>(key: string, variant?: FillVariant, hovered?: boolean): string | undefined</code></td><td>Gets the most suitable background color, based upon the supplied parameters.</td></tr><tr><td>getFgHex</td><td><code>(key: string, variant?: FillVariant): string | undefined</code></td><td>Gets the most suitable foreground color, based upon the supplied parameters.</td></tr></tbody></table>
