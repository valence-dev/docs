# Generic props

## `GenericProps`
Every Valence component has these properties. Individual components may implement these props differently, and some may choose to entirely ignore the `children` prop.

| Property | Type            | Description                               |
|----------|-----------------|-------------------------------------------|
| children | `ReactNode`     | Children components.                      |
| style    | `CSSProperties` | Optional additional styles.               |
| id       | `string`        | Optional ID to provide to each component. |

## `GenericLayoutProps`
Extends `GenericProps`. Most layout-conscious properties will make use of these properties. The exact implementation and default values for these properties will vary on a case-by-case basis.
| Property        | Type                               | Description                               |
|-----------------|------------------------------------|-------------------------------------------|
| backgroundColor | `CSSProperties["backgroundColor"]` | Sets the `background-color` css property. |
| color          | `CSSProperties["color"]`           | Sets the `color` css property.            |
| padding         | `CSSProperties["padding"]`         | Sets the `padding` css property.          |
| margin          | `CSSProperties["margin"]`          | Sets the `margin` css property.           |
| width           | `CSSProperties["width"]`           | Sets the `width` css property.            |
| height          | `CSSProperties["height"]`          | Sets the `height` css property.           |

## `GenericReactiveProps`
Extends `GenericProps`. These props are used as a base for all [reactive components](./breakpoints.md), and simply replace the `style` prop with a `style?: ReactiveProp<CSSProperties>` prop.

## `GenericReactiveLayoutProps`
Extends `GenericReactiveProps`. These props are used by all reactive layout-conscious components, and simply replace the types of `GenericLayoutProps` with their `ReactiveProp` equivalents.