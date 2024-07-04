---
description: 'Last updated: 3.0.0 (04/07/2024) | Added: 2.0.0'
---

# UseDisclosure

`useDisclosure` is a hook that allows the manipulation of a `boolean` state. It is widely used internally to hide or show components such as the [Tooltip](../components/overlays/tooltip.md) and [Modal](../components/overlays/modal.md).

## Usage

```tsx
import { useDisclosure, Tooltip, Button } from "@valence-ui/core";

function MyComponent() { 
    const disclosure = useDisclosure(false);

    return ( 
        <Tooltip
            disclosure={disclosure}
        >
            <Tooltip.Trigger>
                <Button
                    onClick={() => disclosure.open()}
                >
                    I'm a button!
                </Button>
            </Tooltip.Trigger>
            <Tooltip.Content>
                I'm a tooltip!
            </Tooltip.Content>
        </Tooltip>
    )
}
```

{% hint style="info" %}
Many Valence components (such as the Tooltip) will accept the entire Disclosure as a prop, but this may be overkill or incompatible with many external components. If you instead need the raw `boolean` value, use the `disclosure.opened` attribute.
{% endhint %}

## Return type

<table data-full-width="false"><thead><tr><th width="130.11726384364823">Attribute</th><th width="276">Type</th><th>Description</th></tr></thead><tbody><tr><td>opened</td><td><code>boolean</code></td><td>Whether the disclosure is open.</td></tr><tr><td>open</td><td><code>() => void</code></td><td>Open the disclosure.</td></tr><tr><td>close</td><td><code>() => void</code></td><td>Close the disclosure.</td></tr><tr><td>toggle</td><td><code>() => void</code></td><td>Toggle the disclosure.</td></tr><tr><td>update</td><td><code>(value: boolean) => void</code></td><td>Manually update the disclosure.</td></tr></tbody></table>

***

## Changelog

* **3.0.0:** added the `.toggle()` method to the return type.
* **2.0.0:** added hook.
