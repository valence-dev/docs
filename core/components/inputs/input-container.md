# Input container
The `InputContainer` prop is a structural component similar to the [`PrimitiveButton`](../buttons/primitive-button.md) that is used to create other input components. Unless you intend to make your own inputs, you should avoid using this component.

## Props
### `GenericInputEventHandlerProps`
These props are provided to most Valence input elements, and are used to expose event handlers to higher order components.
| Property     | Type                                                   | Description                                                          |
|--------------|--------------------------------------------------------|----------------------------------------------------------------------|
| onInvalid    | `(e: SyntheticEvent<HTMLInputElement, Event>) => void` | Called when this input fails validation on form submission.          |
| onSelect     | `(e: SyntheticEvent<HTMLInputElement, Event>) => void` | Called when this input is selected and edited.                       |
| onEnterPress | `(e: SyntheticEvent<HTMLInputElement, Event>) => void` | Called when the `Enter` key is pressed while focus is on this input. |
| onKeyPress   | `(e: SyntheticEvent<HTMLInputElement, Event>) => void` | Called when any key is pressed while focus is on this input.         |
| onFocus      | `(e: SyntheticEvent<HTMLInputElement, Event>) => void` | Called when this input is focused.                                   |
| onBlur       | `(e: SyntheticEvent<HTMLInputElement, Event>) => void` | Called when this input is blurred.                                   |

### `GenericInputProps`
Extends [`GenericLayoutProps`](../../core/generic-props.md). These props are provided to most Valence input components, and provide basic property inputs.

| Property    | Type            | Description                                                                                                    |
|-------------|-----------------|----------------------------------------------------------------------------------------------------------------|
| icon        | `ReactNode`     | An icon to display at the left side of this input.                                                             |
| placeholder | `string`        | Placeholder text for this input. Defaults to blank.                                                            |
| size        | `ComponentSize` | Sets the size class for this input. Defaults to the theme default size.                                        |
| radius      | `ComponentSize` | Sets the size class for the radius of this input. Defaults to the theme default radius size.                   |
| grow        | `boolean`       | Shorthand for `flex-grow = 1`.                                                                                 |
| autoFocus   | `boolean`       | Specifies if this input will be focused upon mount.                                                            |
| disabled    | `boolean`       | Specifies if this input is disabled.                                                                           |
| readOnly    | `boolean`       | Specifies if this input is read only.                                                                          |
| required    | `boolean`       | Specifies if this input is required for a form.                                                                |
| loading     | `boolean`       | Specifies if this input is loading. If set, this input will be set to `readOnly` and its icon replaced with a `Loader`. |
| form        | `string`        | The ID of the `<form>` element this input belongs to.                                                          |
| name        | `string`        | The name of this input when submitted within a form.                                                           |
| tabIndex    | `number`        | The `tabIndex` html property of this input. Useful for keyboard-only navigation and accessibility.             |

### `InputContainerProps`
Extends `GenericInputProps` and simply makes the `children` property required. In this case, `children` should always be a valid styled child input for this container.