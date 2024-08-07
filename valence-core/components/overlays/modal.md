---
description: 'Last updated: 3.0.0 (04/07/2024)'
---

# Modal

## Usage

```tsx
import { Modal, Button, useDisclosure } from "@valence-ui/core";

function MyComponent() { 
    const disclosure = useDisclosure(false);

    return ( 
        <>
            <Button
                onClick={() => disclosure.open()}
            >
                Open modal
            </Button>
            
            <Modal
                disclosure={disclosure}
                title="My modal"
            >
                Hello there!
            </Modal>
        </>
    )
}
```

### Advanced props

```tsx
import { Modal, Button, useDisclosure } from "@valence-ui/core";

function MyComponent() { 
    const disclosure = useDisclosure(false);

    return ( 
        <>
            <Button
                onClick={() => disclosure.open()}
            >
                Open modal
            </Button>
            
            <Modal
                disclosure={disclosure}
                title="My modal"
                
                closeOnOverlayClick={false}    // true by default
                closeOnEscape={false}          // true by default 
                lockScroll={false}             // true by default
            >
                Hello there!
            </Modal>
        </>
    )
}
```

### Background props

```tsx
import { Modal, Button, useDisclosure } from "@valence-ui/core";

function MyComponent() { 
    const disclosure = useDisclosure(false);

    return ( 
        <>
            <Button
                onClick={() => disclosure.open()}
            >
                Open modal
            </Button>
            
            <Modal
                disclosure={disclosure}
                title="My modal"
                
                overlayBackgroundProps={{
                    backgroundColor: "white",
                    backdropFilter: "dot-blur",
                }}
            >
                Hello there!
            </Modal>
        </>
    )
}
```

{% hint style="info" %}
For more information about the accepted props, see Modal Background.
{% endhint %}

***

## Props

_Extends `GenericOverlayProps`._

<table data-full-width="true"><thead><tr><th width="203">Property</th><th width="145">Type</th><th>Description</th></tr></thead><tbody><tr><td>disclosure (required)</td><td><code>Disclosure</code></td><td>A disclosure to handle state information about this modal.</td></tr><tr><td>flexProps</td><td><a href="../layout/flex/#props"><code>FlexProps</code></a></td><td>Optional props to pass to the flex component.</td></tr><tr><td>innerFlexProps</td><td><code>FlexProps</code></td><td>Optional props to pass to the inner flex component.</td></tr></tbody></table>

***

## Changelog

* **3.0.0:** Added a `1px` border to unify with sheets and help distinguish foreground from background.
* **2.2.0:** Changed how internal scrolling works; added `innerFlexProps`.
