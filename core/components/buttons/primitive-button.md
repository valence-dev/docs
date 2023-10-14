# Primitive button
The `PrimitiveButton` component is the most basic fully-functional button component. It is used by all other button components, and can be used to make your own buttons.

## Props
Extends [`GenericClickableProps`](./generic-clickable.md) and [`GenericLayoutProps`](../../core/generic-props.md).

| Property    | Type                           | Description                                                                                                                            |
|-------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| variant     | `FillVariant`                | Sets the styling variant. Defaults to theme default.                                                                                   |
| size        | `ComponentSize`                | Sets the size class. Defaults to theme default size.                                                                                   |
| radius      | `ComponentSize`                | Sets the radius size class. Defaults to theme default radius.                                                                          |
| aspectRatio | `CSSProperties["aspectRatio"]` | Sets the `aspect-ratio` css property.                                                                                                  |
| square      | `boolean`                      | Shorthand for `aspect-ratio = 1`.                                                                                                      |
| shadow      | `boolean`                      | Specifies if a shadow will be shown under the button. The shadow is as defined in the `ValenceProvider`.                               |
| grow        | `boolean`                      | Shorthand for `flex-grow = 1`.                                                                                                         |
| disabled    | `boolean`                      | Specifies if this button is disabled.                                                                                                  |
| loading     | `boolean`                      | Specifies if this button is loading. If set, it will be disabled and its contents replaced with a `Loader`.                            |
| motion      | `MotionBehaviourProps`         | Defines motion behavior for this button. This will automatically be overridden if the user has reduced motion enabled on their device. |