---
description: 'Last updated: 2.0.0 (22/01/2024)'
---

# Modal background

{% hint style="danger" %}
This is a foundational component and is not designed to be used by itself. Only use this if you intend to make your own modals or overlays.
{% endhint %}

## Usage

```tsx
import { ModalBackground, Button, useDisclosure } from "@valence-ui/core";

function MyComponent() { 
    const disclosure = useDisclosure(false);

    return ( 
        <>
            <Button
                onClick={() => disclosure.open()}
            >
                Open modal
            </Button>
            
            <ModalBackground
                disclosure={disclosure}
            >
                // Modal content...
            </ModalBackground>
        </>
    )
}
```

### Changing blur style

The `backdropFilter` prop can be used to change if and how the background is blurred.

```tsx
import { ModalBackground, Button, useDisclosure } from "@valence-ui/core";

function MyComponent() { 
    const disclosure = useDisclosure(false);

    return ( 
        <>
            <Button
                onClick={() => disclosure.open()}
            >
                Open modal
            </Button>
            
            <ModalBackground
                disclosure={disclosure}
                backdropFilter="blur"     // Default
            >
                // Modal content...
            </ModalBackground>
        </>
    )
}
```

***

## Props

_Extends `GenericOverlayBackgroundProps`._

<table data-full-width="true"><thead><tr><th width="128">Property</th><th width="141">Type</th><th>Description</th></tr></thead><tbody><tr><td>disclosure</td><td><code>Disclosure</code></td><td>A disclosure to specify state information about the modal.</td></tr></tbody></table>
