---
description: 'Last updated: 2.0.0 (21/01/2024)'
---

# Outline Container

## Usage

```tsx
import { OutlineContainer } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <OutlineContainer
            label="Floating container"
        >
            // Container children...
        </OutlineContainer>
    )
}
```

### Overriding position

The Outline Container accepts the `GenericFloatingLayoutProps` type, allowing you to position it wherever you please on the screen. By default, it will be inline until it is `10px` from the top of the screen (`75px` on [`mobile`](../../../core-concepts/responsiveness.md)), from which point it will become sticky.

```tsx
import { OutlineContainer } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <OutlineContainer
            label="Floating container"
            top="unset"
            bottom={20}
            left={20}
            right={100}
        >
            // Container children...
        </OutlineContainer>
    )
}
```

### Inline use

The Outline Container will stick to the top of the screen by default, but can be used as an inline component by setting the `sticky` prop to `false`.

```tsx
import { OutlineContainer } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <OutlineContainer
            label="Floating container"
            sticky={false}
        >
            // Container children...
        </OutlineContainer>
    )
}
```

***

## Props

_Extends `GenericFloatingLayoutProps` and_ [_`FlexProps`_](flex/#props)_._

<table data-full-width="true"><thead><tr><th width="135">Property</th><th width="303">Type</th><th>Description</th></tr></thead><tbody><tr><td>sticky</td><td><code>boolean</code></td><td>Determines if this container will stick to the window, or simply be a part of it. <code>true</code> by default.</td></tr><tr><td>label</td><td><code>string</code></td><td>A label to display below the container.</td></tr><tr><td>labelProps</td><td><code>Omit&#x3C;TextProps, "children"></code></td><td>Optional props to pass to the label component.</td></tr><tr><td>spacing</td><td><code>number</code></td><td>Spacing around the container. <code>5px</code> by default.</td></tr><tr><td>radius</td><td><code>ComponentSize</code></td><td>Size class of the component's radius. Defaults to theme default.</td></tr></tbody></table>
