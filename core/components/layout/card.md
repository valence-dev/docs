# Card
The `Card` component ecosystem is an extensible way to design cards. The `Card` component is a layout wrapper around the [`PrimitiveButton`](../buttons/primitive-button.md), and then accepts `Card.Image`, `Card.Section` or `Card.Buttons` as children.

## `Card` props
Extends `GenericReactiveLayoutProps`.
| Property    | Type                                 | Description                                                                    |
|-------------|--------------------------------------|--------------------------------------------------------------------------------|
| size        | `ReactiveProp<ComponentSize>`        | [REACTIVE] Defines the size class for this card.                               |
| radius      | `ReactiveProp<ComponentSize>`        | [REACTIVE] Defines the radius size class for this card.                        |
| gap         | `ReactiveProp<CSSProperties["gap"]>` | [REACTIVE] Defines the gap size between this card's contents. Defaults to `0`. |
| buttonProps | `PrimitiveButtonProps`               | Optional props to pass to the button component of this card.                   |
| flexProps   | `FlexProps`                          | Optional props to pass to the `Flex` component of this card.                   |

## Card image
The `Card.Image` provides a simple wrapper around the [`Image`](../display/images/image.md) component that gives it some default values especially for a usage within the card.

### Props
Extends `GenericReactiveProps` & `GenericImageProps`.
| Property | Type                                    | Description                                                         |
|----------|-----------------------------------------|---------------------------------------------------------------------|
| radius   | `ReactiveProp<ComponentSize>`           | [REACTIVE] Defines the radius size class of this image.             |
| width    | `ReactiveProp<CSSProperties["width"]>`  | [REACTIVE] Sets `width` css property. Defaults to `"100%"`.         |
| height   | `ReactiveProp<CSSProperties["height"]>` | [REACTIVE] Sets `height` css property. Defaults to `"fit-content"`. |


## Card section
The `Card.Section` component is a basic wrapper around the [`Flex`](../layout/flex.md) component that gives it some default values for use within the `Card`.

### Props
Extends `FlexProps`.


## Card buttons
The `Card.Button` component is a basic `Flex` row component that stops any event propagation to the card below it, allowing it to safely store small buttons or input elements. This component should be used with reservation. 

### Props
Extends `FlexProps`.