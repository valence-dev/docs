---
description: 'Last updated: 3.0.0 (04/07/2024)'
---

# Bottom Sheet

{% hint style="warning" %}
In Valence 3, this component now imports from `@valence-ui/core`.
{% endhint %}

{% hint style="info" %}
The Bottom Sheet is best used on touchscreen-only devices, thus it is suggested to use the Dynamic Sheet component instead.
{% endhint %}

The Bottom Sheet is an overlay that aims to replicate the common "slide up sheet" UI pattern on mobile devices. The sheet will respond to pointer or touch drag.

## Usage

```tsx
import { BottomSheet, useDisclosure, Button } from "@valence-ui/core";

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

_Extends_ [_`GenericSheetProps`_](../../../generics/generic-sheet-props.md#genericsheetprops)_._

<table data-full-width="false"><thead><tr><th width="192.5351812366738">Property</th><th width="136">Type</th><th>Description</th></tr></thead><tbody><tr><td>releaseOffset</td><td><code>number</code></td><td>The offset the sheet must be from its original position before it will close. Defaults to 50% of the viewport height.</td></tr><tr><td>releaseVelocity</td><td><code>number</code></td><td>The velocity the sheet must be moving at before it will close. Defaults to <code>500</code>.</td></tr><tr><td>allowInnerScrolling</td><td><code>boolean</code></td><td>Whether to allow the sheet to scroll its inner content. Defaults to <code>false</code>.</td></tr><tr><td>innerFlexProps</td><td><code>FlexProps</code></td><td>Optional props to apply to the inner flex component.</td></tr></tbody></table>

***

## Changelog

* **3.3.0:** now imports from `@valence-ui/core`.
* **2.2.0:** fixed bugs with scrollable content; added `innerFlexProps` and `allowInnerScrolling` props.
