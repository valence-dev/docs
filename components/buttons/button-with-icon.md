# Button with icon
The `ButtonWithIcon` component is a composite of the [`Button`](./text-button.md) and [`IconButton`](./icon-button.md) components.

## Props
Extends [`TextButtonProps`](./text-button.md).
| Property     | Type                | Description                                    |
|--------------|---------------------|------------------------------------------------|
| icon        | `ReactNode`         | The icon of this button (required).                        |
| iconPosition | `"left" \| "right"` | The position of this icon relative to the text. Defaults to `"left"`. |