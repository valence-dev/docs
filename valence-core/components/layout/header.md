---
description: 'Last updated: 2.0.0 (21/01/2024)'
---

# Header

## Usage

```tsx
import { Header, Title } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Header>
            <Title>
                Page title!
            </Title>
        </Header>
    )
}
```

***

## Props

_Extends_ [_`FlexProps`_](flex/#props)_._

<table data-full-width="true"><thead><tr><th width="133.48323170731706">Property</th><th width="282">Type</th><th>Description</th></tr></thead><tbody><tr><td>position</td><td><code>CSSProperties["position"]</code></td><td>Defines the position of this header.</td></tr><tr><td>innerProps</td><td><code>FlexProps</code></td><td>Properties to pass to the inner flex component.</td></tr></tbody></table>

### Changelog

* **2.4.0:** rebuilt the Header component, removing compacting logic and replacing it with native CSS alternatives.
