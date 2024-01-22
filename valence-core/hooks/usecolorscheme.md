---
description: 'Last updated: 2.0.0 (22/01/2024)'
---

# UseColorScheme

`useColorScheme` is a hook that provides the current preferred color scheme of the user's operating system. It also allows the app to toggle between light and dark color schemes.

Internally, this hook is used by the [Color utility system](../../core-concepts/color/) to provide the correct colors for the user's preferred color scheme.

## Usage

```tsx
import { useColorScheme, Button } from "@valence-ui/core";

function MyComponent() { 
    const { colorScheme } = useColorScheme();
    
    return ( 
        <Button
            color={colorScheme === "dark" ? "blue" : "red"}
        >
            I'm a button!
        </Button>
    )
}
```

## Return type

<table data-full-width="true"><thead><tr><th width="157">Attribute</th><th width="159">Type</th><th>Description</th></tr></thead><tbody><tr><td>colorScheme</td><td><code>ColorScheme</code></td><td>The color scheme.</td></tr><tr><td>isDarkMode</td><td><code>boolean</code></td><td>Is the color scheme <code>"dark"</code>?</td></tr><tr><td>isLightMode</td><td><code>boolean</code></td><td>Is thecolor scheme <code>"light"</code>?</td></tr><tr><td>toggle</td><td><code>() => void</code></td><td>Toggle the color scheme.</td></tr><tr><td>setDark</td><td><code>() => void</code></td><td>Set the color scheme to <code>"dark"</code>.</td></tr><tr><td>setLight</td><td><code>() => void</code></td><td>Set the color scheme to <code>"light"</code>.</td></tr></tbody></table>

### ColorScheme

```typescript
type ColorScheme = "light" | "dark";
```
