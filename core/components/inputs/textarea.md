# Textarea
The `Textarea` Valence component is a light wrapper around the `textarea` element that provides a similar API to the [`TextInput`](./text-input.md).

## Props
Extends `GenericInputProps` & `GenericInputEventHandlerProps`.
| Property     | Type                               | Description                                                                                            |
|--------------|------------------------------------|--------------------------------------------------------------------------------------------------------|
| value        | `string`                           | The value of this input (required).                                                                    |
| setValue     | `Dispatch<SetStateAction<string>>` | Sets the value of this input (required).                                                               |
| autoComplete | `boolean`                          | Whether the value of this input can be automatically completed by the browser/OS. Defaults to `false`. |
| spellCheck   | `boolean`                          | Whether this input is subject to spell checking by the browser/OS. Defaults to `true`.                 |
| minLength    | `number`                           | The minimum length of this input.                                                                      |
| maxLength    | `number`                           | The maximum length of this input.                                                                      |
| cols         | `number`                           | Specifies the visible width of this input.                                                             |
| rows         | `number`                           | Specifies the visible number of lines in this input.                                                   |
| wrap         | `LineWrapBehaviour`                | Specifies how the text in this input is to be wrapped.                                                 |
| resize       | `ResizeBehaviour`                  | Specifies how this input can be resized. Defaults to `"none"`.                                         |
| minHeight    | `CSSProperties["minHeight"]`       | The minimum height of this input.                                                                      |
| maxHeight    | `CSSProperties["maxHeight"]`       | The maximum height of this input.                                                                      |
| minWidth     | `CSSProperties["minWidth"]`        | The minimum width of this input.                                                                       |
| maxWidth     | `CSSProperties["maxWidth"]`        | The maximum width of this input.                                                                       |

## `LineWrapBehaviour`
[Read more](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea).
- `"soft"` - The browser ensures that all line breaks in the entered value area are a `CR+LF` pair, but no additional breaks are added to the value.
- `"hard"` - The browser automatically inserts line breaks so that each line is no longer than the width of the input; the `cols` prop must be specified for this to take effect.
- `"off"` - Like `soft`, but changes in appearance to `white-space: pre` so that line segments exceeding `cols` are not wrapped and the `Textarea` becomes horizontally scrollable.

## `ResizeBehaviour`
[Read more](https://developer.mozilla.org/en-US/docs/Web/CSS/resize)
- `"none"` - The input offers no user-controllable method to resize it.
- `"both"` - The input can be resized both horizontally and vertically.
- `"horizontal"` - The input can be resized in the horizontal direction.
- `"vertical"` - The input can be resized in the vertical direction.