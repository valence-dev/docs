---
description: 'Last updated: 2.1.0 (30/01/2024) | Added: 2.1.0'
---

# Avatar Group

The Avatar Group is a wrapper component designed specifically for creating a group of [Avatar](avatar.md) components.&#x20;

The Avatar Group accepts most props that the Avatar does (except `src` and `alt`), and will set those props as the props for the children Avatars.

## Usage

```tsx
import { AvatarGroup, Avatar } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <AvatarGroup>
            <Avatar
                src="Avatar url..."
                alt="A nice avatar!"
            />
            <Avatar
                src="Avatar url..."
                alt="A nice avatar!"
            />
        </AvatarGroup>
    )
}
```

The spacing between Avatars in the group can be adjusted with the `gap` property. By default, the Avatar Group will bunch its children together.

***

## Props

_Extends_ [_`AvatarProps`_](avatar.md#props)_._

<table data-full-width="true"><thead><tr><th width="184">Property</th><th width="131">Type</th><th>Description</th></tr></thead><tbody><tr><td>gap</td><td><code>number</code></td><td>The space between avatars.</td></tr><tr><td>children (required)</td><td><code>ReactNode</code></td><td></td></tr></tbody></table>
