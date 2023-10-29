# Slide Up
The `SlideUp` is effectively a [`Modal`](../../core/components/overlays/modal.md) for mobile devices. It exposes many of the same props, however differs in that it slides up from the bottom of the screen, instead of appearing in the middle of it.

The `SlideUp` is best used in situations where the effects of its actions are best viewed in real-time. For example, when inserting additions into the page's content. The `SlideUp` *should not* be used in situations where a user's complete attention is required - instead, use the `Modal`.


## Props
Extends `GenericReactiveLayoutProps`.
| Property            | Type                          | Description                                                                               |
|---------------------|-------------------------------|-------------------------------------------------------------------------------------------|
| opened              | `boolean`                     | Specifies if this SlideUp is opened (required).                                           |
| close               | `() => void`                  | A function to call when this SlideUp is closed (required).                                |
| closeOnOverlayClick | `boolean`                     | Whether to close this SlideUp when the background overlay is clicked. Defaults to `true`. |
| closeOnEscape       | `boolean`                     | Whether to close this SlideUp when the escape key is pressed. Defaults to `true`.         |
| lockScroll          | `boolean`                     | Whether to lock scrolling when this SlideUp is open. Defaults to `false`.                 |
| radius              | `ReactiveProp<ComponentSize>` | [REACTIVE] Sets the size class of the border radius for the top two corners.              |
| shadow              | `ReactiveProp<boolean>`       | [REACTIVE] Specifies if a shadow will be shown. Defaults to `true`.                       |
| overlayProps        | `ModalOverlayProps`           | Props to pass to the background overlay component.                                        |
| flexProps           | `FlexProps`                   | Props to pass to the internal `Flex` component.                                           |