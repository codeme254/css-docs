# CSS Borders

In CSS, a border is a property that defines the edge of an element, separating its content from the surrounding elements.

CSS provides us with a variety of properties to help us work with borders.

## `border-style`

The border-style property in CSS defines the appearance of an element's border.

It determines how the border line will be displayed.

The key values are:

- **none**: No border is displayed (default for most elements).
- **solid**: A single, continuous line.
- **dotted**: A series of dots forming the border.
- **dashed**: A series of short dashes.
- **double**: Two solid lines with a small gap between them.
- **groove**: A carved effect, giving the appearance of the border being grooved into the page.
- **ridge**: The opposite of groove, appearing as though the border is coming out of the page.
- **inset**: Gives the impression that the border is embedded into the element.
- **outset**: Makes the border appear as though it is coming out from the element.

```HTML
<h2 class="none">None</h2>
<h2 class="solid">solid</h2>
<h2 class="dotted">dotted</h2>
<h2 class="dashed">dashed</h2>
<h2 class="double">double</h2>
<h2 class="groove">groove</h2>
<h2 class="ridge">ridge</h2>
<h2 class="inset">inset</h2>
<h2 class="outset">outset</h2>
```

```CSS
.none {
  border-style: none;
}

.solid {
  border-style: solid;
}

.dotted {
  border-style: dotted;
}

.dashed {
  border-style: dashed;
}

.double {
  border-style: double;
}

.groove {
  border-style: groove;
}

.ridge {
  border-style: ridge;
}

.inset {
  border-style: inset;
}

.outset {
  border-style: outset;
}
```

![border-style](border-style.png)

### Applying `border-style` to individual sides

You can also apply `border-style` to each side individually:

- **border-top-style**: applies `border-style` to the top side.
- **border-bottom-style**: applies `border-style` to the bottom side.
- **border-left-style**: applies `border-style` to the left side.
- **border-right-style**: applies `border-style` to the right side.

```HTML
<h2>Hello world</h2>
```

```CSS
h2 {
  border-top-style: solid;
  border-right-style: dotted;
  border-bottom-style: dashed;
  border-left-style: double;
}
```

![applying border-style to individual sides](border-style-to-individual-sides.png)

## `border-width`

The border-width property in CSS specifies the thickness of an element's border.

It determines how wide the border lines will be.

As for the values, you can use any length unit e.g 5px, 3em, 10rem, e.t.c., or use keywords; `thin`,
`medium` and `thick`.

Note that the `border-style` must have been defined for this to work.

```HTML
<h2>Hello world</h2>
<h2 class="thin">thin</h2>
<h2 class="medium">medium</h2>
<h3 class="thick">thick</h3>
```

```CSS
h2 {
  border-style: solid;
  border-width: 5px;
}

.thin {
  border-style: solid;
  border-width: thin;
}

.medium {
  border-style: solid;
  border-width: medium;
}

.thick {
  border-style: solid;
  border-width: thick;
}
```

![border-width](border-width.png)

### Applying border `border-width` to individual sides

You can specify different widths for each side.

- **border-top-width**: for the top side.
- **border-bottom-width**: for the bottom side.
- **border-right-width**: for the right side.
- **border-left-width**: for the left side.

```CSS
h2 {
  border-style: solid;
  border-top-width: 5px;
  border-right-width: 15px;
  border-bottom-width: 20px;
  border-left-width: 3px;
}
```

![individual sides border-width](individual-sides-border-width.png)

### `border-width` shorthands

- **one value**: applies to all sides e.g., `border-width: 5px;`.
- **two values**: first value is for top and bottom, second is for left and right, example, `border-width: 10px 20px;`.
- **three values**: first is for top, second is for left and right and third is for bottom,
  example, `border-width: 35px 15px 90px;`.
- **four values**: specifies top, right, bottom and left in that order, example, `border-width: 5px 10px 15px 20px;`.

## `border-color`

The border-color property in CSS specifies the color of an element's border. It determines how the
border lines will appear visually.

```CSS
h2 {
  border-style: solid;
  border-width: 10px;
  border-color: crimson;
}
```

![border-color](border-color.png)

### Applying `border-color` to individual sides

You can also apply `border-color` to individual sides:

- **border-top-color**: applies color to the top border.
- **border-bottom-color**: applies color to the bottom border.
- **border-left-color**: applies color to the left border.
- **border-right-color**: applies color to the right border.

```CSS
h2 {
  border-style: solid;
  border-width: 10px;
  border-top-color: crimson;
  border-left-color: blue;
  border-bottom-color: green;
  border-right-color: orange;
}
```

![border color on individual sides](border-color-to-individual-sides.png)

## The `border` shorthand

The border shorthand property in CSS allows you to set the border's width, style, and color in a single declaration.

Syntax:

```CSS
border: [border-width] [border-style] [border-color];
```

Note that the order doesn't matter but you must pass the border style.

```CSS
h2 {
  border: red 5px solid;
}
```

![border shorthand](border-shorthand.png)

### Using `border` shorthand on individual sides

You can apply the border shorthand for individual sides:

- **border-top**
- **border-bottom**
- **border-left**
- **border-right**

```CSS
h2 {
  border-top: 2px dashed red;
  border-right: pink dotted 5px;
  border-bottom: double black 10px;
  border-left: green 8px inset;
}
```

![border shorthand on individual sides](border-shorthand-on-individual-sides.png)
