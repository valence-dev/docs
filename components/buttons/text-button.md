# Text button
Known as the `Button` component, the text button is a light wrapper around the [`PrimitiveButton`](./primitive-button.md) component. This button accepts a `string` as its children, and uses the [`Text`](../display/text.md) component to style its content.

## Props
Extends [`PrimitiveButtonProps`](./primitive-button.md).
| Property  | Type        | Description                                  |
|-----------|-------------|----------------------------------------------|
| children  | `string`    | The children of this component.              |
| textProps | `TextProps` | Properties to apply to the `Text` component. |