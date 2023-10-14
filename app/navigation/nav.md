# `Nav`
The `Nav` component is an implementation of a root-level navigator for webapps. It appears as a vertical stack of icon buttons down the left side of the screen, and is designed to be used in conjunction with the [`AppContainer` component](../layout/app-container.md).

## Props
Extends `GenericNavProps`.
| Property     | Type                   | Description                                                                          |
|--------------|------------------------|--------------------------------------------------------------------------------------|
| favicon      | `string`               | An optional favicon or app logo to include at the top of the nav on desktop devices. |
| faviconProps | `PrimitiveButtonProps` | Properties to pass to the favicon button.                                            |

### `GenericNavProps`
Extends `GenericReactiveLayoutProps`.
| Property      | Type                                 | Description                                                                                                                                           |
|---------------|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| buttons       | `NavButtonProps[]`                   | Buttons to display on the top of the nav.                                                                                                             |
| bottomButtons | `NavButtonProps[]`                   | Buttons to display on the bottom of the nav. On mobile devices, these will be grouped with the `buttons` horizontally along the bottom of the screen. |
| gap           | `ReactiveProp<CSSProperties["gap"]>` | Sets `gap` css property.                                                                                                                              |

### `NavButtonProps`
Extends [`IconButtonProps`](../../core/components/buttons/icon-button.md).
| Property      | Type                                 | Description                                                                                                                                           |
|---------------|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| buttons       | `NavButtonProps[]`                   | Buttons to display on the top of the nav.                                                                                                             |
| bottomButtons | `NavButtonProps[]`                   | Buttons to display on the bottom of the nav. On mobile devices, these will be grouped with the `buttons` horizontally along the bottom of the screen. |
| gap           | `ReactiveProp<CSSProperties["gap"]>` | Sets `gap` css property.                                                                                                                              |