# `Text` & `Title`
Valence's `Text` and `Title` components support a number of basic inline [Markdown](https://www.markdownguide.org/) modifiers:
- `\n` line break/newline
- `***{...}***` for bolded, italicized text
- `**{...}**` for bolded text
- `*{...}*` for italicized text
- `{...}` for monospace text

## `Title`
Fundamentally, the `Title` component is a light wrapper around the `Text` component that exposes the optional `order` prop. It defaults to `1`, and specifies the `h1-h5` semantic header order, as well as some styles. The styles of each title level can be modified in the `ValenceProvider` `theme.titles` attribute, but defaults to the following values:

```ts
titles: {
  1: { fontSize: 28, bold: true },
  2: { fontSize: 22, bold: true },
  3: { fontSize: 18, bold: true },
  4: { fontSize: 16, bold: true },
  5: { fontSize: 14, bold: true },
  6: { fontSize: 12, bold: true },
},
```
> Each level accepts any of the Valence `TextProps` attributes.

## Props
| Property  | Type                             | Description                                                                                        |
|-----------|----------------------------------|----------------------------------------------------------------------------------------------------|
| family    | `CSSProperties["fontFamily"]`    | Sets `font-family` css property                                                                    |
| weight    | `CSSProperties["fontWeight"]`    | Sets `font-weight` css property                                                                    |
| fontSize  | `CSSProperties["fontSize"]`      | Sets `font-size` css property                                                                      |
| align     | `CSSProperties["textAlign"]`     | Sets `text-align` css property                                                                     |
| transform | `CSSProperties["textTransform"]` | Sets `text-transform` css property                                                                 |
| size      | `ComponentSize`                  | Sets the size of the text according to theme default sizing. Is overridden by the `fontSize` prop. |
| color     | `CSSProperties["color"]`         | Sets `color` css property                                                                          |
| italic    | `boolean`                        | Shorthand for `font-style: italic`                                                                 |
| bold      | `boolean`                        | Shorthand for `font-weight: 800`                                                                   |
| monospace | `boolean`                        | Shorthand for `font-family: monospace`                                                             |
> All formatting properties are overridden by any markdown styles applied to text sections.

## Polymorphism
Valence `Text` and `Title` components are [Polymorphic](../../core/polymorphism.md), thus accept the `component` prop. They additionally accept the `link` prop, which is used when `component=link` to redirect to another page. See the [Link documentation](https://reactrouter.com/en/main/components/link) for more information.