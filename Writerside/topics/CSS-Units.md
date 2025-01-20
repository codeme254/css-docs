# CSS Units

As we have seen thus far, many CSS properties like `width`, `height`, `margin`, `padding`
`font-size`, e.t.c., take a length.

CSS has many different ways of expressing lengths.

In CSS, length is a number and a unit with no whitespace. For example, `5px`.

There are two general kinds of units used for length and size in CSS:
- absolute
- relative

## Absolute length units
These units represent fixed values and are not affected by the size of their parent or viewport. 
They are generally not responsive.

These units include:
- `px` (pixels): 1 pixel is formally defined ad 1/96 of an inch. All other absolute length units are based on 
this definition of a pixel.
- `cm` (centimeters): 1cm is roughly 37.8 pixels.
- `mm` (millimeters): 1mm is roughly 3.78 pixels.
- `in` (inches): In CSS, 1 inch is roughly 96 pixels.
- `pt` (points): in CSS, 1pt is roughly 1.3333 pixels.
- `pc` (picas): In CSS, 1pc is roughly 16 pixels.

```HTML
<h2 class="px">px</h2>
<h2 class="cm">cm</h2>
<h2 class="mm">mm</h2>
<h2 class="in">in</h2>
<h2 class="pt">pt</h2>
<h2 class="pc">pc</h2>
```

```CSS
h2 {
  border: 2px solid;
}

.px {
  width: 200px;
}

.cm {
  width: 5.3cm;
}

.mm {
  width: 52.9mm;
}

.in {
  width: 2.1in;
}

.pt {
  width: 150.4pt;
}

.pc {
  width: 12.5pc;
}
```
![absolute units](absolute-units.png)

In absolute units, all the other units are rarely used except `px`.
## Relative Units
Relative units depend on the size of other elements (like parent elements, the root element, or the viewport). 
These units are essential for creating responsive designs.

These units include:
### `%` percent
This size is relative to the parent element.

```HTML
<div>
    <h2>Hello world</h2>
</div>
<div>
    <h3>What a better place</h3>
</div>
```
```CSS
div {
  border: 2px solid;
  margin-bottom: 10px;
}

h2 {
  border: 2px solid;
  width: 40%;
}

h3 {
  border: 2px solid;
  width: 110%;
}
```
![percentage](percentage-width.png)

### `em`
`em` means relative to the font-size of the element.

2em for example means 2 multiplied by the current font-size.

```HTML
<div>
    <h2>Hello world</h2>
</div>
```
```CSS
h2 {
  font-size: 20px;
  border: 2px solid;
  width: 5em; /*100px (20px*5em)*/
}
```
![em](em.png)

### `rem`
Relative to the font size of the root element (usually `<html>`).
```CSS
html {
  font-size: 10px;
}

h2 {
  font-size: 2rem;/* 2 * 10px */
}
```

### `vw` (viewport width)
1vw = 1% of the viewport width.

```CSS
div {
  width: 50vw; /* 50% of the viewport width */
}
```

### `vh` (viewport height)
1vh = 1% of the height of the viewport.

```CSS
div {
  height: 100vh; /* 100% of the viewport height */
}
```

### `ch`
Relative to the width of the character "0" in the element's font.

Useful for setting widths in typography.

```CSS
div {
  width: 20ch; /* Width of 20 "0" characters */
}
```