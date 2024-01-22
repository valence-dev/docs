---
description: 'Last updated: 2.0.0 (22/01/2024)'
---

# UseDetectKeyDown

`useDetectKeyDown` detects when a key is pressed and fires the callback function. It attaches the event listener to the document body, thus making it handy for keyboard shortcuts, etc.

## Usage

```tsx
import { useDetectKeyDown, Text } from "@valence-ui/core";

function MyComponent() { 
    useDetectKeyDown(
        (e) => console.log("Key pressed!", e),
        "Escape",
        true,
    );
    
    return ( 
        <Text> 
            Press `Escape`!
        </Text>
    )
}
```

### Listen for multiple keys

Passing a list of keycodes into the `keys` parameter allows the hook to listen for any number of keys. A `switch` block in the callback function may be necessary to distinguish between the keys pressed.

```tsx
import { useDetectKeyDown, Text } from "@valence-ui/core";

function MyComponent() { 
    useDetectKeyDown(
        (e) => {
            switch(e.key) {
                case "Escape": return console.log("Escape pressed!");
                case "F": return console.log("F pressed!");
                default: return console.log("Unknown key pressed!");
            }
        },
        ["Escape", "F", "G"],
        true,
    );
    
    return ( 
        <Text> 
            Press `Escape`, "F" or "G"!
        </Text>
    )
}
```

### Controlled listening

Using a Disclosure or boolean state allows you to control when the hook is listening for keyboard events, without unmounting the component it is attached to.

```tsx
import { useDetectKeyDown, useDisclosure, Button } from "@valence-ui/core";

function MyComponent() {
    const disclosure = useDisclosure(); 
    
    useDetectKeyDown(
        (e) => {
            console.log("Escape pressed!");
            disclosure.close();
        },
        "Escape",
        disclosure.opened,
    );
    
    return ( 
        <Button
            onClick={() => disclosure.update(!disclosure.opened)}
        > 
            { disclosure.opened 
                ? "Press `Escape`"
                : "Don't press `Escape`"
            }
        </Button>
    )
}
```

***

## Parameters

<table data-full-width="true"><thead><tr><th width="193">Parameter</th><th width="292">Type</th><th>Description</th></tr></thead><tbody><tr><td>callback (required)</td><td><code>(e: KeyboardEvent) => void</code></td><td>The function to call when the key is pressed.</td></tr><tr><td>keys (required)</td><td><code>string | string[]</code></td><td>A key or array of keys to listen for.</td></tr><tr><td>runCheck</td><td><code>boolean</code></td><td>Whether to listen for keyboard events.</td></tr><tr><td>deps</td><td><code>any[]</code></td><td>Any dependencies to pass to the <code>useEffect</code> hook.</td></tr></tbody></table>
