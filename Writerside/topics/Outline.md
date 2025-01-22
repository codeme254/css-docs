# Outline

The CSS `outline` property is used to draw a line around an element, outside its border edge, for emphasis or visual
distinction.

Unlike border, the outline does not affect the layout of the element, meaning it doesn't take up space.

## Individual Outline Properties
### `outline-style`
Sets the style of the outline.

Options include: `solid`, `dotted`, `dashed`, `double`, `groove` e.t.c.

```HTML
<div class="solid">
    <h2>solid</h2>
</div>

<div class="dotted">
    <h2>dotted</h2>
</div>

<div class="double">
    <h2>double</h2>
</div>

<div class="dashed">
    <h2>dashed</h2>
</div>
```

```CSS
.solid {
  outline-style: solid;
}

.dotted {
  outline-style: dotted;
}

.double {
  outline-style: double;
}

.dashed {
  outline-style: dashed;
}
```
![outline style](outline-style.png)

### `outline-width`
Specifies the thickness of the outline.

```HTML
<div>
    <h2>Hello, World</h2>
</div>
```
```CSS
div {
  outline-style: solid;
  outline-width: 8px;
}
```
![outline width](outline-width.png)

### `outline-color`
Specifies the color of the outline.

```CSS
div {
  outline-style: solid;
  outline-width: 8px;
  outline-color: crimson;
}
```
![outline-color](outline-color.png)

### `outline-offset`
Specifies the space between the border and the outline.

```CSS
div {
  border: 5px solid green;
  outline-style: solid;
  outline-width: 5px;
  outline-color: crimson;
  outline-offset: 30px;
}
```

![outline-offset](outline-offset.png)

## `outline` shorthand
You can specify the `outline-style`, `outline-width` and `outline-color` in one declaration using the `outline`
shorthand as shown.

```CSS
div {
  outline: solid 3px green;
}
```

![outline shorthand](outline-shorthand.png)
