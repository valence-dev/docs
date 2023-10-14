# Multipart button
The `MultipartButton` is the most complex button included in Valence by default, and includes support for numerous props. 

## Props
Extends [`PrimitiveButtonProps`](./primitive-button.md).
| Property      | Type        | Description                                                                                                 |
|---------------|-------------|-------------------------------------------------------------------------------------------------------------|
| title         | `string`    | The title/main text content of this button (required).                                                      |
| subtitle      | `string`    | Descriptive secondary text of this button.                                                                  |
| leftIcon      | `ReactNode` | An icon to display to the left of the button's text content.                                                |
| rightIcon     | `ReactNode` | An icon to display to the right of the button's text content. Defaults to a Tabler `IconChevronRight` icon. |
| titleProps    | `TextProps` | Properties to pass to the title text component.                                                             |
| subtitleProps | `TextProps` | Properties to pass to the subtitle text component.                                                          |
> This button does not use the `children` prop.