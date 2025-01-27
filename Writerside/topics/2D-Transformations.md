# 2D Transformations

CSS 2D transformations modify elements by translating, rotating, scaling, skewing, or combining these transformations.

They are applied using the transform property, allowing rich visual effects.

These transformations include:

- translate()
- rotate()
- scaleX()
- scaleY()
- scale()
- skewX()
- skewY()
- skew()
- matrix()

## `translate()`
Moves an element from it's current position.

```CSS
transform: translate(x, y);
```

- x: Horizontal movement.
- y: Vertical movement.

```HTML
<div>
    <h2>Hello, world</h2>
</div>
```

```CSS
div {
  transform: translate(400px, 300px);

  width: 200px;
  height: 200px;
  border: 3px solid red;
}
```

You can also use `translateX()` to move an element in the horizontal direction and `translateY()` to move an element
in the vertical direction.
```CSS
div {
  transform: translateX(300px) translateY(300px);

  width: 200px;
  height: 200px;
  border: 3px solid red;
}
```

## `rotate()`
Rotates an element clockwise or counterclockwise around its origin.

The value is supplied in degree units i.e. `deg`.

```CSS
div {
  transform: rotate(45deg);

  width: 200px;
  height: 200px;
  border: 3px solid red;
}
```
![rotate](rotate.png)

## `scaleX()`
Scales the width of an element along the horizontal axis.

The value passed does not take any units as it is a ratio value.

```CSS
div {
  transform: scaleX(2);

  width: 200px;
  height: 200px;
  border: 3px solid red;
}
```
![scaleX()](scale-x.png)

## `scaleY()`
Scales an element along the vertical axis.

The value passed does not take any units as it is a ratio value.

```CSS
div {
  transform: scaleY(2);

  width: 200px;
  height: 200px;
  border: 3px solid red;
  margin: 100px;
}
```

![scaleY()](scale-y.png)

## `skewX()`
Skews an element along the horizontal axis.

Value is passed in degree units.

```CSS
div {
  transform: skewX(30deg);

  width: 200px;
  height: 200px;
  border: 3px solid red;
  margin: 100px;
}
```

![skewX()](skew-x.png)

## `skewY()`
Skews an element along the vertical axis.

Value is passed in degree units.

```CSS
div {
  transform: skewY(30deg);

  width: 200px;
  height: 200px;
  border: 3px solid red;
  margin: 100px;
}
```
![skewY()](skew-y.png)