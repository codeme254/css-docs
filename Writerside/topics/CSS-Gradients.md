# CSS Gradients

Gradients are a type of background feature in CSS that allows for smooth transitions between colors.

Gradients can be used to apply background effects on an element without the need for an external image.

Gradients are declared using the `background` or `background-image` property

There are three major types of gradients in CSS:
- Linear gradient
- Radial gradient
- Conic gradient

## `linear-gradient`
Linear gradients transition colors along a straight line.

You can optionally define the direction (e.g., `to right`, to `bottom-left`) and specify multiple color stops.

Here is the syntax
```CSS
background: linear-gradient(direction, color-stop1, color-stop2, ...;
```

Examples:
```HTML
<div>
    <h1>Hello world</h1>
</div>
```

```CSS
div {  
  height: 550px;
  background: linear-gradient(red, green, blue, orange);  
}
```
![basic linear gradient](basic-linear-gradient.png)

We can use the keywords `top`, `bottom`, `right` and `left` to define the direction of a linear gradient.

The gradient below goes to the right
```CSS
div {  
  height: 550px;
  background: linear-gradient(to right,red, green, blue, orange);  
}
```
![linear gradient to right](linear-gradient-to-right.png)

We can also combine these keywords, the gradient below goes to the bottom right for example:

```CSS
div {  
  height: 550px;
  background: linear-gradient(to bottom right,red, green, blue, orange);  
}
```

![linear gradient to bottom right](gradient-to-bottom-right.png)

### `repeating-linear-gradient`
We can also create repetition patterns for `linear-gradient` using `repeating-linear-gradient`:
```CSS
div {
  height: 550px;
  background: repeating-linear-gradient(red, green 40px);
}
```
![repeating linear gradient](repeating-linear-gradient.png)

The `40px` value at the end defines the distance at which the gradient starts repeating.

Here, the browser will render a gradient that transitions from red to green and after `40px` the pattern will repeat 
itself.

## `radial-gradient`
Radial gradients transition colors outward in a circular or elliptical pattern from a central point.

```HTML
<div>
    <h1>Hello, world</h1>
</div>
```
```CSS
div {
   height: 550px;
   background-image: radial-gradient(red, yellow, green);
}
```

![radial gradient](radial-gradient.png)

You can also specify a shape for the radial gradient as either `ellipse` or `circle`, the default is `ellipse`.

```CSS
div {
  height: 550px;
  background-image: radial-gradient(circle, red, yellow, green);
}
```

![circular radial gradient](circle-radial-gradient.png)

### `repeating-radial-gradient`
We can also create repetition patterns for `radial-gradient` using `repeating-radial-gradient`:

```CSS
div {
  height: 550px;
  background: repeating-radial-gradient(circle,red, green 40px);
}
```
![repeating radial gradient](repeating-radial-gradient.png)

## `conic-gradient`
Conic gradients transition colors around a center point, similar to a pie chart.

```HTML
<div>
    <h1>Hello, world</h1>
</div>
```
```CSS
div {
  height: 550px;
  background-image: conic-gradient(red, yellow, green, orange, blue);
}
```
![conic gradient](conic-gradient.png)

You can optionally specify an angle.
```CSS
div {
  height: 550px;
  background-image: conic-gradient(from 80deg,red, yellow, green, orange, blue);
}
```
![conic gradient with angle specified](angled-conic-gradient.png)

### `repeating-conic-gradient`
We can also create repetition patterns for `conic-gradient` using `repeating-conic-gradient`.

In `repeating-conic-gradient`, we don't specify the repetition distance in px as in `repeating-linear-gradient` and
`repeating-radial-gradient`, we use `deg` (degrees) instead.

```CSS
div {
  height: 550px;
  background: repeating-conic-gradient(red, green 40deg);
}
```

![repeating conic gradient](repeating-conic-gradient.png)