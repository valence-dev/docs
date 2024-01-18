---
description: 'Last modified: 2.0.0 (16/01/2024)'
---

# Color

Valence makes use of a powerful yet unconventional color system that uses opacity to mix colors.  This unusual method allows Valence to mix colors more dynamically than other libraries, making it easier to build layered elements (such as a button on a card), without creating an expansive color palette.

## Terminology

* **Swatch:** part of a color, including a six-digit base hex code (#XXXXXX) and three opacity levels, each of which is a two-digit hex code to be appended to the base code.
* **Color:** a complete Valence color, which includes a key, a default Swatch and an optional dark Swatch.

## The `useColors` hook

The `useColors` hook allows easy access to Valence's color palette, and exposes four unique functions that can be utilized in your code:

1. `getSwatch()` - Retrieves a swatch of a color from the palette, based on the color scheme the user has elected to use.
2. `getHex()` - Retrieves a hex code for a color at the given key. This function will return a complete hex code (including opacity) for a given color.
3. `getBgHex()` - This is an utility function to retrieve the best background color given the supplied `FillVariant`. This is the function used in all button components to determine their background color.
4. `getFgHex()` - Similarly to `getBgHex()`, this method will return a suitable foreground color for a given `FillVariant`. This is the function used in all button components to determine their text/icon color.

Every function accepts a `key` parameter, which is the `key` value of a Valence `Color`. `key` will also accept the following:

* `"primary"`, in which case the current primary color will be used.
* Any six-digit hex code, in which case a default Swatch will be created that can have its opacity modified.
* Any [web-safe color key](https://www.w3schools.com/tags/ref\_colornames.asp), which (if not found on the Valence palette), will just return exactly as it is. This should be used as an absolute last resort, because these values cannot have their opacity modified.
