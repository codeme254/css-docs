# CSS Transitions

CSS transitions make property changes smooth and visually appealing by animating the transition between states.

## `transition-delay`
Defines the time to wait before the transition starts.

The value is supplied in seconds units i.e. `s`

```CSS
div {
  transition-delay: 0.5s;
}
```

## `transition-duration`
Specifies how long the transition takes to complete.

```CSS
div {
  transition-duration: 1s;
}
```

## `transition-property`
Specifies the CSS property to animate.

Use the `all` keyword to animate all animatable properties.

```CSS
div {
  transition-property: background-color;
}
```

## `transition-timing-function`
Defines the speed curve of the transition.

The common values are:

- **ease** (default): Starts slow, accelerates, then slows down.
- **linear**: Maintains a constant speed.
- **ease-in**: Starts slow, then accelerates.
- **ease-out**: Starts fast, then slows down.
- **ease-in-out**: Starts slow, accelerates in the middle, then slows down.

```CSS
div {
  transition-timing-function: ease-in-out;
}
```

You can supply a custom timing function using `cubic-bezier()` i.e. `cubic-bezier(n, n, n, n)`

```CSS
div {
  transition-timing-function: cubic-bezier(0.25, 0.1, 0.25, 1));
}
```

## The `transition` shorthand
Combines transition-property, transition-duration, transition-timing-function, and transition-delay into a single line.

```CSS
transition: property duration timing-function delay;
```

```CSS
div {
  transition: background-color 0.5s ease-in 0.2s;
}
```