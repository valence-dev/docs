# Image
The Valence `Image` component is a light wrapper around the `<img>` element, and is designed to allow easy interaction with the `ValenceContext`. This component is also reactive.

## Props
Extends `GenericImageProps`.

| Property    | Type                                    | Description                                                                                          |
|-------------|-----------------------------------------|------------------------------------------------------------------------------------------------------|
| placeholder | `ReactNode`                             | Placeholder content for this image.                                                                  |
| radius      | `ReactiveProp<ComponentSize>`           | Defines the border radius size class of this image. Defaults to the theme default radius size class. |
| width       | `ReactiveProp<CSSProperties["width"]>`  | Sets `width` css property.                                                                           |
| height      | `ReactiveProp<CSSProperties["height"]>` | Sets `height` css property.                                                                          |
| square      | `ReactiveProp<boolean>`                 | Shorthand for `aspect-ratio = "1/1"`.                                                                |
| shadow      | `ReactiveProp<boolean>`                 | Specifies if a shadow will be shown.                                                                 |

### `GenericImageProps`
| Property | Type                                            | Description                          |
|----------|-------------------------------------------------|--------------------------------------|
| src      | `string \| ArrayBuffer \| undefined`            | Source URI of this image (required). |
| alt      | `string`                                        | Alt text for this image (required).  |
| fit      | `ReactiveProp<CSSProperties["objectFit"]>`      | Sets `object-fit` css property.      |
| position | `ReactiveProp<CSSProperties["objectPosition"]>` | Sets `object-position` css property. |