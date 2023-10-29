# Column
The `Column` and `Column.Container` component system is a flexible and reactive method to layout content on a page.

## `Column` props
Extends `GenericColumnProps`.

## `GenericColumnProps`
Extends `FlexProps`.

## Column container
The `Column.Container` is ideal for storing `Column` components, and is effectively a `Flex` row with some default values set.

### Props
Extends `FlexProps`.
| Property | Type                                      | Description                                 |
|----------|-------------------------------------------|---------------------------------------------|
| flow     | `ReactiveProp<CSSProperties["flexFlow"]>` | [REACTIVE] Defines `flex-flow` css property |