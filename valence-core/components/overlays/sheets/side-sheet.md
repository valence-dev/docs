---
description: 'Last updated: 3.0.0 (04/07/2024)'
---

# Side Sheet

{% hint style="warning" %}
In Valence 3, this component now imports from `@valence-ui/core`.
{% endhint %}

{% hint style="info" %}
The Side Sheet is best used on desktop devices, thus it is suggested to use the Dynamic Sheet component instead.
{% endhint %}

The Side Sheet is an aside that can be used to place optional content to the right of the main page's content. It is best used for complex or specific actions that are unsuitable for the primary content on the page.

## Usage

```tsx
import { SideSheet, useDisclosure, Button } from "@valence-ui/app";

function MyComponent() { 
    const disclosure = useDisclosure();

    return ( 
        <>
            <Button
                onClick={() => disclosure.open()}
            > 
                Open sheet!
            </Button>
            
            <SideSheet
                disclosure={disclosure}
                title="I'm a side sheet!"
            >
                // Sheet content...
            </SideSheet>
        </>
    )
}
```

### Position & display type

By default, the Side Sheet will appear to the right of the page on `"desktop"` [breakpoints](../../../../core-concepts/responsiveness.md) and larger, pushing the content left if there isn't enough room. On `"tablet"` breakpoints and smaller, the Side Sheet will become an overlay.

This behavior can be modified using the `display` prop, where behavior for each breakpoint may be defined.

While in `"overlay"` display mode, the `direction` prop can be used to change which side the sheet will appear from, defaulting to `"right"` if not supplied.

```tsx
import { SideSheet, useDisclosure, Button } from "@valence-ui/app";

function MyComponent() { 
    const disclosure = useDisclosure();

    return ( 
        <>
            <Button
                onClick={() => disclosure.open()}
            > 
                Open sheet!
            </Button>
            
            <SideSheet
                disclosure={disclosure}
                title="I'm a side sheet!"
                display={{
                    desktop: "overlay", 
                    tablet: "overlay",
                    desktopLarge: "inline",
                }}
                direction="left"
            >
                // Sheet content...
            </SideSheet>
        </>
    )
}
```

***

## Props

Extends [`GenericSheetProps`](../../../generics/generic-sheet-props.md#genericsheetprops).

<table data-full-width="true"><thead><tr><th width="158.7981308411215">Property</th><th width="216">Type</th><th>Description</th></tr></thead><tbody><tr><td>display</td><td><a href="side-sheet.md#sidesheetdisplay"><code>SideSheetDisplay</code></a></td><td>The display option for the sidebar. Defaults to <code>"inline"</code> on desktop and bigger, and <code>"overlay"</code> on mobile and smaller.</td></tr><tr><td>direction</td><td><code>"left" | "right"</code></td><td>The direction that this sidebar will appear from. Direction will only be adhered to if the display type is <code>"overlay"</code>. Otherwise, it will be <code>"right"</code> by default.</td></tr><tr><td>innerFlexProps</td><td><code>FlexProps</code></td><td>Optional props to pass to the inner flex component.</td></tr></tbody></table>

### SideSheetDisplay

```tsx
type SideSheetDisplay = "inline" | "overlay";
```

***

## Changelog

* **3.3.0:** now imports from `@valence-ui/core`.
* **2.2.0:** Reworked internal scrolling; added `innerFlexProps` prop.
