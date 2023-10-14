# Alert
The `Alert` component is used to provide inline error and other alert handling. 

## Props
Extends [`GenericClickableProps`](../buttons/generic-clickable.md), [`PolymorphicButtonProps`](../../core/polymorphism.md) and [`GenericLayoutProps`](../../core/generic-props.md).
| Property | Type            | Description                                                               |
|----------|-----------------|---------------------------------------------------------------------------|
| alert    | `AlertContent`  | The content of this alert (required).                                     |
| show     | `boolean`       | Whether to mount and show this alert.                                     |
| variant  | `FillVariant` | The styling variant of this alert. Defaults to `filled`.                  |
| size     | `ComponentSize` | The size of this alert. Defaults to the theme default size.               |
| radius   | `ComponentSize` | The border size of this alert. Defaults to the theme default border size. |
| shadow   | `boolean`       | Specifies if a shadow will be shown.                                      |

### `Alert`
| Property | Type        | Description                         |
|----------|-------------|-------------------------------------|
| title    | `string`    | The title of this alert (required). |
| message  | `string`    | The message of this alert.          |
| icon     | `ReactNode` | The icon of this alert.             |