# CSS Fonts

## Generic font families
Generic font families are a fallback mechanism.

Generic font families are broad categories of fonts that represent the overall style of a font 
rather than specifying a particular typeface.

These families are used in CSS to provide fallback options when a preferred font is unavailable on the user's system.

They ensure that text is displayed in a consistent and readable manner.

They can also be used to classify other fonts.

Generic font families are:
- serif
- sans-serif
- monospace
- cursive
- fantasy

### serif fonts
These are fonts with small lines or strokes called "serifs" attached to the end of characters.

Examples include: Lucida Bright, Lucida Fax, Palatino, Palatino Linotype, Palladio, URW Palladio, serif..

Often used for print media, formal documents, and long blocks of text because the serifs guide the eye along the lines.

![serif font](serif-font.png)


### sans-serif
Fonts without the small lines or embellishments at the ends of characters, resulting in a clean and modern appearance.

Examples include: Open Sans, Fira Sans, Lucida Sans, Lucida Sans Unicode, Trebuchet MS, Liberation Sans, 
Nimbus Sans L, sans-serif.

Commonly used for web content, digital interfaces, and informal designs due to their simplicity and 
readability on screens.

![sans serif](sans-serif.png)

### monospace
Fonts where each character takes up the same amount of horizontal space.

All glyphs have the same fixed width.

Used for coding, technical documents, and tabular data because the uniform spacing aligns characters and lines 
perfectly.

Examples include:  Fira Mono, DejaVu Sans Mono, Menlo, Consolas, Liberation Mono, Monaco, Lucida Console, monospace.

![monospace](monospace.png)

### cursive
Fonts designed to resemble handwritten or script styles, with flowing and sometimes connected characters.

Glyphs in cursive fonts generally have either joining strokes or other cursive characteristics beyond those of 
italic typefaces. The glyphs are partially or completely connected, and the result looks more like handwritten 
pen or brush writing than printed letter work.

Used for decorative or creative purposes, such as invitations, headings, or informal contexts.

Examples include: Brush Script MT, Brush Script Std, Lucida Calligraphy, Lucida Handwriting, Apple Chancery, cursive.

![cursive](cursive.png)

### fantasy
Decorative fonts with playful or artistic designs, often used to convey creativity or uniqueness.

Examples include: Papyrus, Herculanum, Party LET, Curlz MT, Harrington, fantasy.

![fantasy](fantasy.png)

## `font-family`
The font-family property in CSS is used to specify the typeface (or font) for text in a web page.

It allows you to set multiple fonts in a prioritized order, known as a **font stack**, to ensure text 
is displayed correctly even if a particular font is unavailable.

In the example below, the browser tries Verdana first, if it is unavailable, it falls back to Genevac, if neither is
available, it defaults to any sans-serif font.

```HTML
<h1>Hello, world</h1>
```

```CSS
h1 {
  font-family: Verdana, Geneva, sans-serif;
}
```

![font-family](font-family.png)

Always specify multiple fonts to account for compatibility issues.

Include at least one generic family at the end to ensure a reasonable default.

Font names with multiple words must be enclosed within double quotes.

```CSS
h1 {
  font-family: "Comic Sans MS", "Brush Script MT", cursive;
}
```

## `font-style`
The font-style property in CSS defines the style or slant of the text.

It is commonly used to apply italics or other stylistic variations to text.

The values here are:
- **normal**: The text is displayed in a standard, upright style (default value).
- **italic**: The text is displayed in an italicized style.
- **oblique**: regular form of the font but slanted a bit.
- **initial**: resets the value to its default (`normal`).
- **inherit**: inherits the `font-style` value from its parent element.

```HTML
<p class="normal">normal</p>
<p class="italic">italic</p>
<p class="oblique">oblique</p>
```

```CSS
.normal {
  font-style: normal;
}

.italic {
  font-style: italic;
}

.oblique {
  font-style: oblique;
}
```

![font-style](font-style.png)

## `font-weight`
The font-weight property controls the thickness (or boldness) of the font used for text.

Its values are:
- **normal**: default font weight (equal to numeric weight 400).
- **bold**: applies a bold weight to the text (equal to numeric weight 700).
- **bolder**: Makes the font weight heavier than its parent element (not well supported in most browsers).
- **lighter**: Makes the font weight lighter than its parent element. (not well supported in most browsers).
- You can also use numeric values 100 to 900, i.e., 100 (thin), 200 (extra light), 300 (light), 
400 (normal), 500 (medium), 600 (semi-bold), 700 (bold), 800 (extra bold), and 900 (black)

```HTML
<p class="text-1">text 1</p>
<p class="text-2">text 2</p>
<p class="text-3">text 3</p>
```

```CSS
.text-1 {
  font-weight: normal;
}

.text-2 {
  font-weight: bold;
}

.text-3 {
  font-weight: 900;
}
```
![font-weight](font-weight.png)

## `font-variant`
The font-variant property specifies whether or not a text should be displayed in a small-caps font.

In a small-caps font, all lowercase letters are converted to uppercase letters. However, the converted uppercase 
letters appears in a smaller font size than the original uppercase letters in the text.

The values are:
- **normal**: the default value, text appears as it is, with no special variation.
- **small-caps**: Displays lowercase letters as uppercase but in a smaller size. Uppercase letters remain unchanged.
- **inherit**: Inherits the font-variant value from its parent element.

```HTML
<p>Lorem Ipsum Dolor Sit Amet Consectetur Adipisicing.</p>
```
```CSS
p {
  font-variant: small-caps;
}
```
![font-variant](font-variant.png)

## `font-size`
The font-size property is used to control the size of the text on a webpage.

For the value, it can take a custom value such as `24px` or one of the following keywords

- **xx-small**: extremely small text.
- **x-small**: slightly smaller than small.
- **small**: standard small text.
- **medium**: default font-size (usually equivalent to 16px in most browsers)
- **large**: larger than normal text.
- **x-large**: larger than large.
- **xx-large**: larger than `x-large`.

```HTML
<p class="xx-small">xx small</p>
<p class="x-small">x-small</p>
<p class="small">small</p>
<p class="medium">medium</p>
<p class="large">large</p>
<p class="x-large">x-large</p>
<p class="xx-large">xx-large</p>
<p class="text">text</p>
```

```CSS
.xx-small {
  font-size: xx-small;
}

.x-small {
  font-size: x-small;
}

.small {
  font-size: small;
}

.medium {
  font-size: medium;
}

.large {
  font-size: large;
}

.x-large {
  font-size: x-large;
}

.xx-large {
  font-size: xx-large;
}

.text {
  font-size: 56px;
}
```

![font-size](font-size.png)