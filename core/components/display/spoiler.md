# Spoiler
The `Spoiler` component is a simple wrapper used to show or hide content at will. It accepts a single prop, `show`, and will animate between height `0` and `auto` based upon whether `show` is true or false.

## Props
Extends [`GenericProps`](../../core/generic-props.md).
| Property | Type      | Description                                                     |
|----------|-----------|-----------------------------------------------------------------|
| show     | `boolean` | Whether to show or hide the spoiler's content. Defaults to `true`. |