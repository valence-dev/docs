---
description: 'Last updated: 2.0.0 (16/01/2024)'
---

# Nav

The `Nav` component is a container component designed to handle movement between high-level pages of the application. It can also be used for application-level actions, such as signing out, changing the color scheme, etc.

The `Nav` is displayed as a vertical strip containing `IconButton` buttons down the left-hand side of the screen, and will transform to a horizontal strip on the `mobile` [breakpoint](../../../core-concepts/responsiveness.md). This component is designed to be used within the [`AppContainer`](../../the-appcontainer.md), but can be used elsewhere.

## Usage

```tsx
import { Nav } from "@valence-ui/app";
import { IconCategory } from "@tabler/icons-react";

function MyComponent() { 
    return ( 
        <Nav
            buttons={[
                {
                    id: "page1",
                    children: <IconCategory />,
                    highlighted: true,
                    to: "/page-1"
                },
                // More buttons...
            ]}
        />
    )
}
```

## Displaying buttons on the bottom

By default, all items in the `buttons` prop will be stacked vertically from the top down. In some circumstances, you may want to display buttons at the bottom of the `Nav`, for which the `bottomButtons` prop becomes useful:

```tsx
import { Nav } from "@valence-ui/app";
import { IconCategory, IconLogout } from "@tabler/icons-react";

function MyComponent() { 
    return ( 
        <Nav
            buttons={[
                {
                    id: "page1",
                    children: <IconCategory />,
                    highlighted: true,
                    to: "/page-1"
                },
                // More buttons...
            ]},
            bottomButtons={[
                {
                    id: "signOut",
                    children: <IconLogout />,
                    onClick: () => alert("Signed out")
                },
                // More buttons...
            ]},
        />
    )
}
```

The `bottomButtons` prop acts effectively the same as the `buttons` prop, but will stack on the bottom instead of top.

On the `mobile` breakpoint, both regular and bottom buttons will be stacked next to one another horizontally from left-to-right, with `bottomButtons` towards the right.

## Hiding specific buttons

Every child of the `buttons` and `bottomButtons` prop accepts a `show` prop, which allows you to control the breakpoints at which this button is visible. This can be useful to hide specific buttons on the `mobile` breakpoint, especially if you have many buttons stacking across the smaller `Nav`.

```tsx
import { Nav } from "@valence-ui/app";
import { IconCategory } from "@tabler/icons-react";

function MyComponent() { 
    return ( 
        <Nav
            buttons={[
                {
                    id: "page1",
                    children: <IconCategory />,
                    highlighted: true,
                    to: "/page-1",
                    // Show on everything except mobile
                    show: { 
                        default: true,
                        mobile: false,
                    }
                },
                // More buttons...
            ]}
        />
    )
}
```

## Adding a favicon

The `Nav` component also accepts a `favicon` and `faviconProps`, which can be used to add a custom graphic, logo or icon at the top of the `Nav`. Note that the favicon will not show on `mobile` breakpoints.

```tsx
import { Nav } from "@valence-ui/app";
import { IconCategory } from "@tabler/icons-react";
import FaviconImg from "./assets/images/favicon.png";

function MyComponent() { 
    return ( 
        <Nav
            favicon={FaviconImg}
            faviconProps={{
                // Custom props to turn the favicon 
                // into a link button
                component: "link",
                to: "/home",
            }}
            buttons={[
                {
                    id: "page1",
                    children: <IconCategory />,
                    highlighted: true,
                    to: "/page-1",
                    // Show on everything except mobile
                    show: { 
                        default: true,
                        mobile: false,
                    }
                },
                // More buttons...
            ]}
        />
    )
}
```

