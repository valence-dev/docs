---
description: 'Last updated: 2.0.0 (22/01/2024)'
---

# Polymorphism

Polymorphism is a complex subject, and is currently a weak point of Valence's type-checking systems. Dive into this subject at your own risk.

Polymorphism allows select Valence components to take different element form on the DOM, affording the components unique attributes and functionality that are usually disallowed by React or HTML.

Valence has three primary polymorphic components:

<table data-view="cards"><thead><tr><th></th><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><h4>Polymorphic Button</h4></td><td>Default: <code>button</code></td><td></td><td><a href="../valence-utils/polymorphism/polymorphic-button.md">polymorphic-button.md</a></td></tr><tr><td></td><td><h4>Polymorphic Layout</h4></td><td>Default: <code>div</code></td><td><a href="../valence-utils/polymorphism/polymorphic-layout.md">polymorphic-layout.md</a></td></tr><tr><td></td><td><h4>Polymorphic Text</h4></td><td>Default: <code>p</code></td><td><a href="../valence-utils/polymorphism/polymorphic-text.md">polymorphic-text.md</a></td></tr></tbody></table>

## Usage

To use polymorphism on compatible components, simply use the `component` prop to change the underlying DOM component.

```tsx
import { Button } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Button 
            component="a"
            href="https://isaacshea.com"
        >
            Go to Isaac's website!
        </Button>
    )
}
```

{% hint style="info" %}
You may encounter TypeScript errors if you are using unusual props on polymorphic components. If you are _sure_ everything works, simply add a `//@ts-ignore` to the line above to get TypeScript to calm down.
{% endhint %}

## When can I use this?

Every component that at some point extends the `PolymorphicTextProps`, `PolymorphicButtonProps` or `PolymorphicLayoutProps` will support polymorphism, which generally includes:

* All buttons
* [Flex](../valence-core/components/layout/flex/), [Grid ](../valence-core/components/layout/grid.md)& all derivative components
* [Modal](../valence-core/components/overlays/modal.md) & [Sheets](../valence-app/components/overlays/dynamic-sheet.md)

## What is the `link` component?

The `component="link"` prop sets the underlying element to a [react-router-dom](https://reactrouter.com/en/main/components/link)-compatible `Link` component, allowing it to interact with the React Router API.
