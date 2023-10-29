# Sidebar
The `Sidebar` component is an adaptive component used to display actions relating to the page it is within. On desktop devices, this will appear down the left-hand side of the screen, and on mobile devices it will appear as a [`SlideUp`](../overlays/slide-up.md) that can be opened with a [`FAB`](../buttons/fab.md).


## Props
Extends `GenericReactiveLayoutProps`.
| Property       | Type                                 | Description                           |
|----------------|--------------------------------------|---------------------------------------|
| gap            | `ReactiveProp<CSSProperties["gap"]>` | Sets `gap` css property.              |
| mobileFabIcon  | `ReactNode`                          | An icon to display on the mobile FAB. |
| mobileFabProps | `FABProps`                           | Props to pass to the mobile FAB.      |