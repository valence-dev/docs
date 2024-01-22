---
description: 'Last updated: 2.0.0 (16/01/2024)'
---

# Sidebar

The `Sidebar` is a basic wrapper component used to display page-specific actions or navigation. It will usually appear to the left of the page content, but to the right of the [`Nav`](nav.md), and is an optional component in the [`AppContainer`](../../the-appcontainer.md).&#x20;

On the `mobile` breakpoint, the `Sidebar` will disappear and become a `SideSheet` that will appear from the left when opened.&#x20;

## Usage

```tsx
import { Sidebar } from "@valence-ui/app";

function MyComponent() { 
    return ( 
         <Sidebar>
             // Sidebar content...
         </Sidebar>   
    )
}
```

If you want to use the `Sidebar` outside of the `AppContainer`, you will need to pass a Disclosure into the `sideSheetProps` to allow it to open on `mobile` breakpoints, like so:

```tsx
import { Sidebar } from "@valence-ui/app";
import { useDisclosure } from "@valence-ui/core";

function MyComponent() { 
    const disclosure = useDisclosure();

    return ( 
         <Sidebar
              sideSheetProps={{
                   disclosure: disclosure,
              }}
         >
             // Sidebar content...
         </Sidebar>   
    )
}
```

## Changing width

Like many components, the `Sidebar` accepts a `width` prop that allows you to override it's default width. By default, `width = 250px`.

## Display options

The `display` prop can be used to change the breakpoints at which the `Sidebar` becomes a `SideSheet` overlay.

```tsx
import { Sidebar } from "@valence-ui/app";

function MyComponent() { 
    return ( 
         <Sidebar
              display={{
                   // Shown to the left of the page content
                   default: "inline",
                   // Becomes a SideSheet
                   mobile: "overlay",
                   // Entirely hidden; cannot be opened
                   tablet: "hidden",
              }}
         >
             // Sidebar content...
         </Sidebar>   
    )
}
```
