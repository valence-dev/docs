# Modal
The `Modal` is a controlled overlay component that allows a title and body content.

## Props
| Property            | Type                | Description                                                   |
|---------------------|---------------------|---------------------------------------------------------------|
| title               | `string`            | The title of this modal (required).                           |
| opened              | `boolean`           | Specifies if this modal is opened (required).                 |
| close               | `() => void`        | A function to call when this modal is closed (required).      |
| closeOnOverlayClick | `boolean`           | Whether to close this modal when the overlay is clicked.      |
| closeOnEscape       | `boolean`           | Whether to close this modal when the `Escape` key is pressed. |
| lockScroll          | `boolean`           | Whether to lock page scrolling while this modal is opened.    |
| withShadow          | `boolean`           | Whether to show a shadow underneath this modal.               |
| radius              | `ComponentSize`     | Sets the `border-radius` css property.                        |
| overlayProps        | `ModalOverlayProps` | Properties to pass to the overlay component.                  |
| flexProps           | `FlexProps`         | Properties to pass to the `Flex` component.                   |

## `ModalOverlay`
Used as an assistant component to the `Modal`.

### Props
| Property        | Type                               | Description                                                                            |
|-----------------|------------------------------------|----------------------------------------------------------------------------------------|
| opened          | `boolean`                          | Whether this overlay is open (required).                                               |
| close           | `() => void`                       | A function to call when this overlay is closed (required).                             |
| closeOnClick    | `boolean`                          | Whether to close this overlay when it is clicked.                                      |
| blurBackground  | `boolean`                          | Whether the contents of the page behind the overlay should be blurred.                 |
| backgroundColor | `CSSProperties["backgroundColor"]` | Sets the `background-color` css property. Defaults to the theme's `permaBlack` color.  |
| padding         | `CSSProperties["padding"]`         | Sets the `padding` css property. Defaults to the theme's padding for the default size. |
| zIndex          | `CSSProperties["zIndex"]`          | Sets the `zIndex` css property. Defaults to `200`.                                     |