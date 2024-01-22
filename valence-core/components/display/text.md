---
description: 'Last updated: 2.0.0 (21/01/2024)'
layout:
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Text

The Text component is a markdown-compatible paragraph wrapper that is particularly handy when dealing with formatting for internationalization.

This component forms the back-bone of all components that render text, including the [Button](../buttons/text-button.md), [Alert](alert.md), [Pill](pill.md), etc.

## Usage

```tsx
import { Text } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Text>
            I'm a **markdown-compatible** text component!
        </Text>
    )
}
```

### Font family

```tsx
import { Text } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Text
            family="Plus Jakarta Sans"
        >
            I'm a **markdown-compatible** text component!
        </Text>
    )
}
```

{% hint style="info" %}
The font family will need to be correctly installed before use. [See more](../../fundamentals/using-custom-fonts.md).
{% endhint %}

### Styles

```tsx
import { Text } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Text
            bold
            italic
            monospace
            size="md"
            transform="uppercase"
            align="right"
        >
            I'm a **markdown-compatible** text component!
        </Text>
    )
}
```

{% hint style="info" %}
**After more specificity?** The `weight` prop allows any CSS `font-weight` attribute, and the `fontSize` prop allows any `font-size` attribute.
{% endhint %}

***

## Supported markdown attributes

* `\n` - line break/newline
* `***{...}***` - bold & italicized text
* `**{...}**` - bold text
* `*{...}*` - italicized text
* `` `{...}` `` - monospace text

***

## Props

Extends `GenericProps`, `GenericClickableProps` and `PolymorphicTextProps`.

<table data-full-width="true"><thead><tr><th width="145">Property</th><th width="332">Type</th><th>Description</th></tr></thead><tbody><tr><td>family</td><td><code>CSSProperties["fontFamily"]</code></td><td>Sets <code>font-family</code> css property.</td></tr><tr><td>weight</td><td><code>CSSProperties["fontWeight"]</code></td><td>Sets <code>font-weight</code> css property.</td></tr><tr><td>fontSize</td><td><code>CSSProperties["fontSize"]</code></td><td>Sets <code>font-size</code> css property.</td></tr><tr><td>align</td><td><code>CSSProperties["textAlign"]</code></td><td>Sets <code>text-align</code> css property.</td></tr><tr><td>transform</td><td><code>CSSProperties["textTransform"]</code></td><td>Sets <code>text-transform</code> css property.</td></tr><tr><td>size</td><td><code>ComponentSize</code></td><td>Sets the size of the text.</td></tr><tr><td>color</td><td><code>CSSProperties["color"]</code></td><td>Sets <code>color</code> css property.</td></tr><tr><td>italic</td><td><code>boolean</code></td><td>Shorthand for <code>font-style: italic</code>.</td></tr><tr><td>bold</td><td><code>boolean</code></td><td>Shorthand for <code>font-weight: 800</code>.</td></tr><tr><td>monospace</td><td><code>boolean</code></td><td>Shorthand for <code>font-family: monospace</code>.</td></tr></tbody></table>
