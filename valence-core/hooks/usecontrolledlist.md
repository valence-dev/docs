---
description: 'Last Updated: 2.0.0 (22/01/2024)'
---

# UseControlledList

`useControlledList` allows lists of a particular type to be controlled through a unified API.&#x20;

The type modifier passed in with the hook determines what type of items the hook will control. By default, this is `string`.

## Usage

```tsx
import { useControlledList, Button, Text } from "@valence-ui/core";

function MyComponent() { 
    const controlledList = useControlledList<string>(["hello", "world"]);
    
    return ( 
        <>
            {controlledList.items.map((item, index) => (
                <Text
                    key={index}
                >
                    {item}
                </Text>
            ))}
            
            <Button
                onClick={() => controlledList.add("there")}
            >
                Add "there"
            </Button>
            
            <Button
                onClick={() => controlledList.remove("world")}
            >
                Remove "world"
            </Button>
            
            <Button
                onClick={() => controlledList.clear()}
            >
                Clear
            </Button>
        </>
    )
}
```

## Return type

<table data-full-width="true"><thead><tr><th width="132">Attribute</th><th width="237">Type</th><th>Description</th></tr></thead><tbody><tr><td>items</td><td><code>T[]</code></td><td>The list of items.</td></tr><tr><td>add</td><td><code>(item: T) => void</code></td><td>Add an item to the list.</td></tr><tr><td>remove</td><td><code>(item: T) => void</code></td><td>Remove an item from the list.</td></tr><tr><td>update</td><td><code>(items: T[]) => void</code></td><td>Override all items in the list.</td></tr><tr><td>clear</td><td><code>() => void</code></td><td>Clear the list.</td></tr><tr><td>includes</td><td><code>(item: T) => boolean</code></td><td>Whether the list includes an item.</td></tr></tbody></table>
