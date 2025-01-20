# Colors

CSS provides various ways to define colors for styling elements.

They include:

- Predefined color names.
- The `rgb()` function
- hex
- The `hsl()` function
- The `rgba()` function
- The `hsla()` function

## Predefined color names

CSS comes with a set of predefined color names that can be used directly in your styles.

These color names are the same as those we are used to in our day-to-day life, for example, red, green, blue, orange,
black, white e.t.c.

```HTML
<h1>This is the heading</h1>
```

```CSS
h1 {
  color: red;
}
```

![predefined color name](predefined-color-name-output.png)

## Opacity

Now that we are talking about colors, this is a great time to talk about the opacity property in CSS.

The opacity property determines the transparency of an element.

It takes any numeric value between 0 and 1 (0 and 1 inclusive) where 1 is fully opaque and 0 is completely transparent.

```HTML
<h1>This is the heading</h1>
```

```CSS
h1 {
  color: red;
  opacity: 0.2;
}
```

![opacity](opacity.png)

## The `rgb()` function

The `rgb()` function in CSS(`rgb(red, green, blue)`) specifies colors by combining the intensities of red, green, and blue.

Each of these color channels can have a value between 0 (no intensity) and 255 (full intensity).

This allows for the creation of a wide range of colors.

Syntax:

```CSS
element {
  color: rgb(red, green, blue);
}
```

here are some examples:

- `rgb(0, 0, 0)`: Black (absence of all colors)
- `rgb(255, 255, 255)`: White (full intensity of all colors)
- `rgb(255, 0, 0)`: Red (full intensity of red, no green or blue)
- `rgb(0, 255, 0)`: Green (full intensity of green, no red or blue)
- `rgb(0, 0, 255)`: Blue (full intensity of blue, no red or green)
- `rgb(255, 255, 0)`: Yellow (full intensity of red and green, no blue)

### Example 1 `rgb()`:

```HTML
<h1>This is a heading</h1>
```

```CSS
h1 {
  color: rgb(0, 255, 0);
}
```

![rgb](rgb.png)

### Example 2 `rgb()`

```HTML
<h1>This is a heading</h1>
```

```CSS
h1 {
  color: rgb(90, 255, 200);
}
```

![rgb](rgb-2.png)

### Example 3 `rgb()`

```HTML
<h1>This is a heading</h1>
```

```CSS
h1 {
  color: rgb(90, 25, 220);
}
```

![rgb](rgb-3.png)

## Hex (Hexadecimal)

Hexadecimal color codes represent colors in six digits, using combinations of `0–9` and `A-F`.

Each pair corresponds to red, green and blue.

Syntax:

```CSS
element {
  color: #rrggbb;
}
```

For example, #ff0000 would result in a red color because red is set to its highest value (ff) and the others are set to
their lowest value (00).

```HTML
<h1>This is a heading</h1>
```

```CSS
h1 {
  color: #ff0000;
}
```

![hex](hex-1.png)

#00ff00 would result in a green color because green is set to its highest value (ff) and the others are set to their
lowest value (00).

```HTML
<h1>This is a heading</h1>
```

```CSS
h1 {
  color: #00ff00;
}
```

![hex](hex-2.png)

You could also go for the shorthand in the form #rgb, for example, red would end up being #f00 and blue would end up
being #0f0

## The `hsl()` function

The `hsl()` function (`hsl(hue, saturation, lightness)`) represents colors using:

- **Hue**: The type of color (0-360 degrees on the color wheel).
- **Saturation**: Intensity of the color (0% to 100%).
- **Lightness**: Brightness of the color (0% to 100%)

```HTML
<h1>This is a heading</h1>
```

```CSS
h1 {
  color: hsl(0, 100%, 70%);
}
```

![hsl](hsl.png)

## The `rgba()` function

`rgba()` is an extension of `rgb()` with an added alpha parameter for transparency.

The alpha parameter takes a value between 0 and 1 (0 and 1 inclusive), and this will determine how transparent or how
opaque and element is with zero meaning completely transparent and one meaning completely opaque.

```HTML
<h1>This is a heading</h1>
```

```CSS
h1 {
  color: rgba(255, 0, 0, .2);
}
```

![rgba](rgba.png)

## The `hsla()` function

`hsla()` extends `hsl()` with an alpha channel for transparency.

The alpha parameter takes a value between 0 and 1 (0 and 1 inclusive), and this will determine how transparent or how
opaque and element is with zero meaning completely transparent and one meaning completely opaque.

```HTML
<h1>This is a heading</h1>
```

```CSS
h1 {
  color: hsla(0, 100%, 70%, .3);
}
```

![hsla](hsla.png)

## The `transparent` keyword

The `transparent` keyword sets and element color to fully transparent.

```HTML
<h1>This is a heading</h1>
```

```CSS
h1 {
  color: transparent;
}
```
