---
description: 'Last updated: 2.0.0 (21/01/2024)'
---

# Image

## Usage

```tsx
import { Image } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Image
            src="https://images.unsplash.com/photo-1419242902214-272b3f66ee7a?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=720&q=80"
            alt="A random image"
        />
    )
}
```

### Override width & height

```tsx
import { Image } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Image
            src="https://images.unsplash.com/photo-1419242902214-272b3f66ee7a?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=720&q=80"
            alt="A random image"
            
            width={200}
            height={300}
        />
    )
}
```

### Override fit & position

```tsx
import { Image } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Image
            src="https://images.unsplash.com/photo-1419242902214-272b3f66ee7a?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=720&q=80"
            alt="A random image"
            
            fit="fill"
            position="center"
        />
    )
}
```

### Custom placeholder

```tsx
import { Image, Flex, Text } from "@valence-ui/core";

function MyComponent() { 
    return ( 
        <Image
            src="https://images.unsplash.com/photo-1419242902214-272b3f66ee7a?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=720&q=80"
            alt="A random image"
            
            placeholder={
                <Flex
                    align="center"
                    justify="center"
                    height="100%"
                    width="100%"
                >
                    <Text>
                        Image not found
                    </Text>
                </Flex>
            }
        />
    )
}
```

***

## Props

_Extends_ [_`GenericImageProps`_](image.md#genericimageprops) _and `GenericProps`._

<table data-full-width="true"><thead><tr><th width="147">Property</th><th width="263">Type</th><th>Description</th></tr></thead><tbody><tr><td>placeholder</td><td><code>ReactNode</code></td><td>Placeholder content for this image.</td></tr><tr><td>radius</td><td><code>ComponentSize</code></td><td>Defines the border radius size class of this image. Defaults to the theme default radius size class.</td></tr><tr><td>width</td><td><code>CSSProperties["width"]</code></td><td>Sets <code>width</code> css property.</td></tr><tr><td>height</td><td><code>CSSProperties["height"]</code></td><td>Sets <code>height</code> css property.</td></tr><tr><td>square</td><td><code>boolean</code></td><td>Shorthand for <code>aspect-ratio = "1/1".</code></td></tr><tr><td>color</td><td><code>CSSProperties["color"]</code></td><td>Sets <code>color</code> css property.</td></tr><tr><td>shadow</td><td><code>boolean</code></td><td>Specifies if a shadow will be shown.</td></tr></tbody></table>

### GenericImageProps

<table data-full-width="true"><thead><tr><th width="150">Property</th><th width="353">Type</th><th>Description</th></tr></thead><tbody><tr><td>src (required)</td><td><code>string | ArrayBuffer | undefined</code></td><td>Source URI of this image.</td></tr><tr><td>alt (required</td><td><code>string</code></td><td>Alt text for this image.</td></tr><tr><td>fit</td><td><code>CSSProperties["objectFit"]</code></td><td>Sets <code>object-fit</code> css property.</td></tr><tr><td>position</td><td><code>CSSProperties["objectPosition"]</code></td><td>Sets <code>object-position</code> css property.</td></tr></tbody></table>
