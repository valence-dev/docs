---
description: 'Last updated: 2.0.0 (18/01/2024)'
---

# Multi-part button

A button used to display complex actions. Does not directly accept the `children` prop, instead taking the `title` and `subtitle` props to display text content.

## Usage

```tsx
import { MultipartButton } from "@valence-ui/core";
import { IconPlus } from "@tabler/icons-react";

function MyComponent() { 
    return ( 
        <MultipartButton
             title="This is a multi-part button!"
             subtitle="Isn't that cool?"
             leftIcon={<IconPlus />}
        />
    )
}
```

## Adding a right icon

```tsx
import { MultipartButton } from "@valence-ui/core";
import { IconPlus, IconChevronRight } from "@tabler/icons-react";

function MyComponent() { 
    return ( 
        <MultipartButton
             title="This is a multi-part button!"
             subtitle="Isn't that cool?"
             leftIcon={<IconPlus />}
             rightIcon={<IconChevronRight />}
        />
    )
}
```

## Modifying the title or subtitle

`titleProps` and `subtitleProps` can be passed into the button to modify the appearance of the title and subtitle. Both under the hood use the `Text` component with some pre-configured styling.

```tsx
import { MultipartButton } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <MultipartButton
             title="This is a multi-part button!"
             subtitle="Isn't that cool?"
             titleProps={{
                  size: "xl"
                  color: "blue"
             }}
             subtitleProps={{
                  size: "xs"
                  color: "black"
             }}
        />
    )
}
```

## Props

_Extends_ [_`PrimitiveButtonProps`_](primitive-button.md#props)_._

<table data-full-width="true"><thead><tr><th width="171">Property</th><th width="132">Type</th><th>Description</th></tr></thead><tbody><tr><td>title (required)</td><td><code>string</code></td><td>Title/main text content of this button.</td></tr><tr><td>subtitle</td><td><code>string</code></td><td>Descriptive secondary text of this button.</td></tr><tr><td>leftIcon</td><td><code>ReactNode</code></td><td>Icon to display on the left of the button.</td></tr><tr><td>rightIcon</td><td><code>ReactNode</code></td><td>Icon to display on the right of the button.</td></tr><tr><td>titleProps</td><td><code>TextProps</code></td><td>Props to pass to the title text component.</td></tr><tr><td>subtitleProps</td><td><code>TextProps</code></td><td>Props to pass to the subtitle text component.</td></tr></tbody></table>
