# Generic clickable props
| Property     | Type                              | Description                                              |
|--------------|-----------------------------------|----------------------------------------------------------|
| to           | `string`                          | Sets the `to` property on `Link` polymorphic components. |
| href         | `string`                          | Sets the html `href` property on valid elements.         |
| target       | `string`                          | Sets the html `target` property on valid elements.       |
| type         | `"submit" \| "reset" \| "button"` | Sets the html `type` property on valid elements.         |
| onClick      | `() => void`                      | Sets the `onClick` event.                                |
| onMouseEnter | `() => void`                      | Sets the `onMouseEnter` event.                           |
| onMouseLeave | `() => void`                      | Sets the `onMouseLeave` event.                           |
| onMouseDown  | `(event: any) => void`            | Sets the `onMouseDown` event.                            |
| onMouseUp    | `(event: any) => void`            | Sets the `onMouseUp` event.                              |
| onFocus      | `() => void`                      | Sets the `onFocus` event.                                |
| onBlur       | `() => void`                      | Sets the `onBlur` event.                                 |