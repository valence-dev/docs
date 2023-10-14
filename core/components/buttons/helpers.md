# Button helpers
Valence's button ecosystem requires a few helper types and functions, as described here.

## Color getters
### `getBackgroundColor()`
This function retrieves the most suitable background color for a button, given the context provided in the function paramters. This function does not return a [`Color`](../../core/colors.md), but instead returns a singular hex string with opacity and coloring calculated.

```ts
function getBackgroundColor(
  color: CSSProperties["backgroundColor"],
  variant: FillVariant | undefined,
  hovered: boolean,
  theme: IValenceContext        // Passed in from useContext(ValenceContext)
): string
```

### `getTextColor()`
Similar to `getBackgroundColor()`, this method will return the most suitable text color, given the context provided in the function parameters. This function does not return a [`Color`](../../core/colors.md), but instead returns a singular hex string with opacity and coloring calculated.

```ts
function getTextColor(
  color: CSSProperties["color"],
  variant: FillVariant | undefined,
  theme: IValenceContext        // Passed in from useContext(ValenceContext)
): string
```


## Motion behaviour
All buttons can have motion behaviour, powered by [Framer Motion](https://www.framer.com/motion/). To help assist with the creation and management of the `motionBehaviour` prop, the following types and functions were created. Motion behaviour is automatically overridden if the browser detects that [reduced motion](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-reduced-motion) is preferred.

## `MotionBehaviourProps`
This type defines the expected value for a component with motion behaviour. This is the type used in the `motionBehaviour` prop for all Valence buttons.

```ts
type MotionBehaviourProps = {
  /** Behaviour for while the component is hovered 
   * `grow` = `scale: 1.1`
   * `raise` = `y: -2` (up)
   * `none` = nothing (default)
   */
  onHover?: "grow" | "raise" | "none";
  /** Behaviour for while the component is being tapped
   * `shrink` = `scale: 0.75`
   * `bounce` = `y: 2` (down; default)
   */
  onTap?: "shrink" | "bounce";
}
```

## `MotionBehaviour` & `MotionBehaviourValue`
These define the output of the `getMotionBehaviour()` method, and are used internally when communicating with Framer Motion.

```ts
/** Defines the values for motion behaviour */
type MotionBehaviourValue = {
  scale?: number | string;
  x?: number | string;
  y?: number | string;
  z?: number | string;
}

/** Defines the return type for the `getMotionBehaviour` function */
export type MotionBehaviour = {
  whileHover?: MotionBehaviourValue;
  whileTap?: MotionBehaviourValue
}
```

## `getMotionBehaviour()`
This function retrieves which `MotionBehaviour` this component should use, given the provided parameters.

```ts
export function getMotionBehaviour(
  props: MotionBehaviourProps | undefined, 
  reducedMotion: boolean | null,
): MotionBehaviour
```