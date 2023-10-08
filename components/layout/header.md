# Header
The `Header` component is a layout component that helps the positioning of a `Title` and other components. It is, by itself, mostly uninteresting, but when paired with the [`AppContainer`](./app-container.md) component, the two work to become a powerful page layout system.


## Breakpoint behaviour
On desktop devices, the `Header` will act as a static container that can be placed anywhere and will scroll with the content. On mobile devices, however, the `Header` will become fixed tot he top of the screen and can shrink as the user scrolls.

The `Header` will interpolate between the `regularHeight`/`tallHeight` (depending on the [viewport breakpoint](../../core/breakpoints.md)) and `compactHeight` on mobile devices, in accordance with the scroll position of the root html element.


## Props
Extends [`FlexProps`](./flex.md).
| Property        | Type      | Description                                                                                 |
|-----------------|-----------|---------------------------------------------------------------------------------------------|
| regularHeight   | `number`  | The height of this header for regular devices. Defaults to `100`.                           |
| tallHeight      | `number`  | The height of this header for tall mobile devices. Defaults to `150`.                       |
| compactHeight   | `number`  | The height of this header when it has been compacted. Defaults to `75`.                     |
| compactOnScroll | `boolean` | Whether this header should compact when the user scrolls down (mobile). Defaults to `true`. |