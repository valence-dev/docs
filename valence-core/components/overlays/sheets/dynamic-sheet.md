---
description: 'Last updated: 3.0.0 (04/07/2024)'
---

# Dynamic Sheet

{% hint style="warning" %}
In Valence 3, this component now imports from `@valence-ui/core`.
{% endhint %}

The Dynamic Sheet is a powerful responsive component that can be used to choose the best sheet for the [breakpoint](../../../../core-concepts/responsiveness.md) context. It can be used to switch between the [Side Sheet](side-sheet.md) and [Bottom Sheet](bottom-sheet.md) as required, utilizing ideal UI patterns for the breakpoint on which your app is running.

## Usage

```tsx
import { DynamicSheet, useDisclosure, Button } from "@valence-ui/app";

function MyComponent() { 
    const disclosure = useDisclosure();

    return ( 
        <>
            <Button
                onClick={() => disclosure.open()}
            > 
                Open sheet!
            </Button>
            
            <DynamicSheet
                disclosure={disclosure}
                title="I'm a dynamic sheet!"
            >
                // Sheet content...
            </DynamicSheet>
        </>
    )
}
```

### Changing the sheet type

By default, the Dynamic Sheet will be an inline Side Sheet, then change to an overlay Side Sheet on `"tablet"` breakpoints and a Bottom Sheet on `"mobile"` breakpoints. This behavior can be overridden with the `type` prop.

```tsx
import { DynamicSheet, useDisclosure, Button } from "@valence-ui/app";

function MyComponent() { 
    const disclosure = useDisclosure();

    return ( 
        <>
            <Button
                onClick={() => disclosure.open()}
            > 
                Open sheet!
            </Button>
            
            <DynamicSheet
                disclosure={disclosure}
                title="I'm a dynamic sheet!"
                type={{
                    desktopLarge: "inline",
                    default: "overlay",
                    mobile: "bottom",
                }}
            >
                // Sheet content...
            </DynamicSheet>
        </>
    )
}
```

***

## Props

<table data-full-width="false"><thead><tr><th width="206.7142857142857">Property</th><th width="201">Type</th><th>Description</th></tr></thead><tbody><tr><td>children (required)</td><td><code>ReactNode</code></td><td></td></tr><tr><td>disclosure (required)</td><td><a href="../../../hooks/usedisclosure.md#return-type"><code>Disclosure</code></a></td><td>A disclosure to handle the sheet's state.</td></tr><tr><td>title (required)</td><td><code>string</code></td><td>The title of the sheet.</td></tr><tr><td>type</td><td><code>DynamicSheetType</code></td><td>The type of the sheet.</td></tr><tr><td>sideSheetProps</td><td><a href="side-sheet.md#props"><code>SideSheetProps</code></a></td><td>Optional props to apply to the Side Sheet component, when displayed.</td></tr><tr><td>bottomSheetProps</td><td><a href="bottom-sheet.md#props"><code>BottomSheetProps</code></a></td><td>Optional props to apply to the Bottom Sheet component, when displayed.</td></tr></tbody></table>

### DynamicSheetType

```tsx
export type DynamicSheetType = SideSheetDisplay | "bottom";
```

***

## Changelog

* **3.3.0:** now imports from `@valence-ui/core`.
