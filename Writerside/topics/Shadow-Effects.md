# Shadow Effects

CSS shadow effects add depth and dimension to your web design by creating shadows on elements.

These include:
- box-shadow
- text-shadow
- drop-shadow

## `box-shadow`
The box-shadow property applies shadows to the outer frame of a box-like element (e.g., div, button).

```CSS
box-shadow: offset-x offset-y blur-radius spread-radius color;
```
- **offset-x**: Horizontal shadow distance (positive for right, negative for left).
- **offset-y**: Vertical shadow distance (positive for bottom, negative for top).
- **blur-radius**: Blurring effect (higher values create softer shadows).
- **spread-radius**: Shadow size (positive to expand, negative to shrink).
- **color**: Shadow color.

```HTML
<div>
    <h2>Hello, world</h2>
</div>
```
```CSS
div {
  width: 300px;
  height: 300px;
  margin: 30px;

  /* box shadow */
  box-shadow: 5px 5px 20px 2px red;
}
```
![box shadow](box-shadow.png)

### Multiple box shadows
You can add multiple shadows to an element by separating them with commas:
```CSS
box-shadow: shadow1, shadow2, shadow3;
```

```CSS
div {
  width: 300px;
  height: 300px;
  margin: 30px;

  /* box shadow */
  box-shadow:
    5px 5px 20px 2px red,
    5px 5px 25px 9px green,
    5px 5px 25px 9px orange;
}
```
![multiple box shadows](multiple-box-shadows.png)

## `text-shadow`
The text-shadow property adds shadows to text, enhancing typography.

```CSS
text-shadow: offset-x offset-y blur-radius color;
```

The syntax is similar to box-shadow syntax but without the spread-radius

```CSS
h2 {
  text-shadow: 2px 2px 3px red;
}
```
![text shadow](text-shadow.png)


## `drop-shadow`
The `drop-shadow` function in the filter property applies a shadow to images or SVGs, similar to box-shadow 
but with better clipping behavior.

Unlike box-shadow, drop-shadow considers the shape of the image or SVG instead of just its bounding box.

```CSS
filter: drop-shadow(offset-x offset-y blur-radius color);
```

```HTML
<img src="img.png" alt="img" width="100px">
```
```CSS
img {
  filter: drop-shadow(10px 10px 10px red);
}
```
![drop shadow](drop-shadow.png)