# Flex & styled flex
`Flex` and `StyledFlex` are powerful, [reactive](../../core/breakpoints.md) layout components that offer wide usage for layout.

## Props
Extends [`GenericReactiveLayoutProps`](../../core/generic-props.md).
| Property  | Type                                            | Description                                                                                |
|-----------|-------------------------------------------------|--------------------------------------------------------------------------------------------|
| direction | `ReactiveProp<CSSProperties["flexDirection"]>`  | Sets the `flex-direction` css property. Defaults to `row`.                                 |
| align     | `ReactiveProp<CSSProperties["alignItems"]>`     | Sets the `align-items` css property. Defaults to `flex-start`.                             |
| justify   | `ReactiveProp<CSSProperties["justifyContent"]>` | Sets the `justify-content` css property. Defaults to `flex-start`                          |
| alignSelf | `ReactProp<CSSProperties["alignSelf"]>`         | Sets the `align-self` css property. Defaults to `stretch`.                                 |
| gap       | `ReactiveProp<CSSProperties["gap"]>`            | Sets the `gap` css property. Defaults to the theme default `padding` for the default size. |
| grow      | `ReactiveProp<boolean>`                         | Shorthand for `flex-grow = 1`. Defaults to `false`.                                        |
| noWrap    | `ReactiveProp<boolean>`                         | Shorthand for `flex-wrap = "nowrap"`. Defaults to `false`.                                 |

## `StyledFlex`
The `StyledFlex` component is a light wrapper around the `Flex` component that offers some standardised styling properties, similar to those found in [button](../buttons/primitive-button.md) and and [input](../inputs/input-container.md) components.

### Props
Extends `FlexProps`.
| Property | Type                          | Description                                                                                   |
|----------|-------------------------------|-----------------------------------------------------------------------------------------------|
| variant  | `ReactiveProp<FillVariant>` | Sets the styling variant. Defaults to the theme default variant.                              |
| size     | `ReactiveProp<ComponentSize>` | Sets the size of this component. Defaults to the theme default size.                          |
| radius   | `ReactiveProp<ComponentSize>` | Sets the radius of this component. Defaults to the theme default border size.                 |
| shadow   | `ReactiveProp<boolean>`       | Whether to include a shadow underneath this component. Will display the theme default shadow. |