# CSS Math functions

CSS math functions allow dynamic calculations for values in your styles, providing flexibility and responsiveness.

There's a wide variety of math functions, but in this guide we will focus on the four most commonly used math functions:
- calc()
- max()
- min()
- clamp()

[More CSS functions are here](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Functions#math_functions)

## `calc()`
The calc() function lets you specify CSS property values using addition, subtraction, multiplication, and division.\

It is often used to combine two CSS values that have different units, such as % and px.

```CSS
div {
  background-color: red;
  height: 30px;
  width: calc(100% - 150px);
}
```
![calc](calc.png)

## `max()`
The max() function selects the largest value from a comma-separated list.

```CSS
div {
  background-color: red;
  height: 30px;
  width: max(10vw, 400px, 50%);
}
```

## `min()`
The min() function selects the smallest value from a comma-separated list.

```CSS
div {
  background-color: red;
  height: 30px;
  width: min(10vw, 400px, 50%);
}
```

## `clamp()`
It sets a value that is constrained between a minimum, preferred, and maximum value.

We can combine the functions of min() and max() by using clamp(). The clamp() math function takes a minimum value, 
the value to be clamped, and the maximum value as arguments.

```CSS
property: clamp(min-value, clamp-value, max-value);
```

If the value to be clamped is less than the passed minimum value, the function will return the minimum value.

If the value to be clamped is greater than the passed maximum value, the function will return the maximum value.

If the value to be clamped is between the passed minimum and maximum values, the function will return the 
original value to be clamped.

In the code below, the width of the element will end up being 30rem the value is between the passed minimum and maximum
values.
```CSS
div {
  background-color: red;
  height: 30px;
  width: clamp(10rem, 30rem, 55rem);
}
```

In the code below, the width of the element will be 20rem because the clamp value is greater than the maximum value.
```CSS
div {
  background-color: red;
  height: 30px;
  width: clamp(10rem, 30rem, 20rem);
}
```

In the code below, the width of the element will be 10 rem because the clamp value is less than the minimum value.
```CSS
div {
  background-color: red;
  height: 30px;
  width: clamp(10rem, 3rem, 20rem);
}
```