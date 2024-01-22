---
description: 'Last updated: 2.0.0 (22/01/2024)'
---

# Bottom Sheet

{% hint style="info" %}
The Bottom Sheet is best used on touchscreen-only devices, thus it is suggested to use the Dynamic Sheet component instead.
{% endhint %}

The Bottom Sheet is an overlay that aims to replicate the common "slide up sheet" UI pattern on mobile devices. The sheet will respond to pointer or touch drag.

## Usage

```tsx
import { BottomSheet, useDisclosure, Button } from "@valence-ui/app";

function MyComponent() { 
    const disclosure = useDisclosure();

    return ( 
        <>
            <Button
                onClick={() => disclosure.open()}
            > 
                Open sheet!
            </Button>
            
            <BottomSheet
                disclosure={disclosure}
                title="I'm a bottom sheet!"
            >
                // Sheet content...
            </BottomSheet>
        </>
    )
}
```

## Props

_Extends_ [_`GenericSheetProps`_](../../generics/generic-sheet-props.md#genericsheetprops)_._

<table data-full-width="true"><thead><tr><th width="169">Property</th><th width="100">Type</th><th>Description</th></tr></thead><tbody><tr><td>releaseOffset</td><td><code>number</code></td><td>The offset the sheet must be from its original position before it will close. Defaults to 50% of the viewport height.</td></tr><tr><td>releaseVelocity</td><td><code>number</code></td><td>The velocity the sheet must be moving at before it will close. Defaults to <code>500</code>.</td></tr></tbody></table>
