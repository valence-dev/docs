# Grid button
The `GridButton` is a unique button that shares many attributes with the `ButtonWithIcon`, but instead arranges its contents vertically within a square button. As the name suggests, this button is ideal for grids of buttons with similar priority and a close relevance. The prominence of the icon in this button type should be considered when designing for it.

## Props
Extends `TextButtonProps`.
| Property     | Type                | Description                                    |
|--------------|---------------------|------------------------------------------------|
| icon        | `ReactNode`         | The icon of this button (required).                        |
| iconPosition | `"top" \| "bottom"` | The position of this icon relative to the text. Defaults to `"top"`. |