---
description: 'Last updated: 3.0.0 (04/07/2024)'
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

_Extends_ [_`FlexCenterProps`_](flex/flex-center.md#props)_._

<table data-full-width="true"><thead><tr><th width="133.48323170731706">Property</th><th width="282">Type</th><th>Description</th></tr></thead><tbody><tr><td>position</td><td><code>CSSProperties["position"]</code></td><td>Defines the position of this header.</td></tr></tbody></table>

### Changelog

* **3.0.0:** `HeaderProps` now extends `FlexCenterProps`. The `innerProps` prop still works, but is not documented here.
* **2.4.0:** rebuilt the Header component, removing compacting logic and replacing it with native CSS alternatives.
