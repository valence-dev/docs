# Switch input
The `SwitchInput` is a controlled switch component designed to replace the `input=checkbox` component in some situations.

## Props
Extends `GenericLayoutProps`.
| Property    | Type                                                   | Description                                                 |
|-------------|--------------------------------------------------------|-------------------------------------------------------------|
| checked     | `boolean`                                              | The value of the input (required).                          |
| setChecked  | `Dispatch<SetStateAction<boolean>>`                    | Sets the value of the input (required).                     |
| label       | `string`                                               | The label associated with this input.                       |
| size        | `ComponentSize`                                        | Sets the size class. Defaults to theme default.             |
| radius      | `ComponentSize`                                        | Sets the radius size class. Defaults to `"xl"`.             |
| grow        | `boolean`                                              | Shorthand for `flex-grow = 1`.                              |
| autoFocus   | `boolean`                                              | Specifies if this input will be focused on mount.           |
| disabled    | `boolean`                                              | Specifies if this input is disabled.                        |
| readOnly    | `boolean`                                              | Specifies if this input is read only.                       |
| required    | `boolean`                                              | Specifies if this input is required.                        |
| loading     | `boolean`                                              | If set, this input will be replaced with a loader.          |
| onFocus     | `(e: SyntheticEvent<HTMLInputElement, Event>) => void` | Called when this input is focused.                          |
| onBlur      | `(e: SyntheticEvent<HTMLInputElement, Event>) => void` | Called when this input is blurred.                          |
| buttonProps | `PrimitiveButtonProps`                                 | Optional props to pass to the `Button` container component. |
| labelProps  | `TextProps`                                            | Optional props to pass to the `Text` label component.       |