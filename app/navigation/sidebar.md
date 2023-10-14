# `Sidebar`
The `Sidebar` component is a vertical stack of buttons designed to handle page-level actions or navigation, such as jumping to page section anchors. It is designed to be used with the [`AppContainer` component](../layout/app-container.md). On desktop devices it will appear as a stack of [`ButtonWithIcons`](../../core/components/buttons/button-with-icon.md), and will be transformed to a horizontal row of [`IconButtons`](../../core/components/buttons/icon-button.md) on mobile devices.

## Props
Extends `GenericReactiveLayoutProps`.
| Property      | Type                                 | Description                                                                    |
|---------------|--------------------------------------|--------------------------------------------------------------------------------|
| buttons       | `SidebarButtonProps[]`               | Buttons to display on the sidebar (required).                                  |
| jumpToSection | `(section: string) => void`          | An optional function to facilitate scrolling to a desired section of the page. |
| gap           | `ReactiveProp<CSSProperties["gap"]>` | Sets `gap` css property.                                                       |


### `SidebarButtonProps`
Extends [`ButtonWithIconProps`](../../core/components/buttons/button-with-icon.md).
| Property    | Type      | Description                                                                                                                                              |
|-------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| highlighted | `boolean` | Specifies if this button is highlighted.                                                                                                                 |
| jumpTo      | `string`  | The ID of a page anchor this button should scroll to when clicked. Requires the `jumpToSection` function to be provided to the parent `Sidebar` element. |