# Floating Action Button (FAB)
As the name suggests, the `FAB` component is an `IconButton` that has fixed positioning relative to the page. Its position and offset can be modified, but by default it sits 20px from the bottom-right corner of the window.

Floating Action Buttons are useful for important actions, such as opening menus and moving to new screens. They are best utilised on mobile devices, however can be used everywhere in the correct circumstances.


## Props
Extends `IconButtonProps`.
| Property  | Type                      | Description                                                            |
|-----------|---------------------------|------------------------------------------------------------------------|
| vPosition | `"top" \| "bottom"`       | Vertical position of this button on the page. Defaults to `"bottom"`.  |
| hPosition | `"left" \| "right"`       | Horizontal position of this button on the page. Defaults to `"right"`. |
| offset    | `number`                  | The distance from the edge of the page. Defaults to `20`.              |
| zIndex    | `CSSProperties["zIndex"]` | Sets `z-index` css property. Defaults to `100`.                        |