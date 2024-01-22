---
description: 'Last updated: 2.0.0 (21/01/2024)'
---

# Card

## Usage

```tsx
import { Card, Text, IconButton } from "@valence-ui/core";
import { Icon123 } from "@tabler/icons-react";

function MyComponent() { 
    return ( 
        <Card>
            <Card.Image
                src="https://image.src"
                alt="A random image"
            />
            <Card.Section>
                <Text>
                    Card text content!
                </Text>
            </Card.Section>
            <Card.Buttons>
                <IconButton>
                    <Icon123 />
                </IconButton>
            </Card.Buttons>
        </Card>
    )
}
```

## Props

_Extends `GenericLayoutProps` and `PolymorphicButtonProps`._

<table data-full-width="true"><thead><tr><th width="145">Property</th><th width="255">Type</th><th>Description</th></tr></thead><tbody><tr><td>size</td><td><code>ComponentSize</code></td><td>Defines the size class for this card.</td></tr><tr><td>radius</td><td><code>ComponentSize</code></td><td>Defines the radius size class for this card.</td></tr><tr><td>gap</td><td><code>CSSProperties["gap"]</code></td><td>Defines the gap size between this card's contents.</td></tr><tr><td>buttonProps</td><td><a href="../buttons/primitive-button.md#props"><code>PrimitiveButtonProps</code></a></td><td>Optional props to pass to the button component of this card.</td></tr><tr><td>flexProps</td><td><a href="flex/#props"><code>FlexProps</code></a></td><td>Optional props to pass to the <code>Flex</code> component of this card.</td></tr></tbody></table>

### CardImageProps

_Extends `GenericProps` and_ [_`GenericImageProps`_](../display/image.md#genericimageprops)_._

<table data-full-width="true"><thead><tr><th width="126">Property</th><th width="264">Type</th><th>Description</th></tr></thead><tbody><tr><td>radius</td><td><code>ComponentSize</code></td><td>Defines the radius size class of this image. Defaults to the theme default radius size class.</td></tr><tr><td>width</td><td><code>CSSProperties["width"]</code></td><td>Sets <code>width</code> css property.</td></tr><tr><td>height</td><td><code>CSSProperties["height"]</code></td><td>Sets <code>height</code> css property.</td></tr></tbody></table>

### CardSectionProps

_Extends_ [_`FlexProps`_](flex/#props)_._

No unique props.

### CardButtonsProps

_Extends_ [_`FlexProps`_](flex/#props)_._

No unique props.
