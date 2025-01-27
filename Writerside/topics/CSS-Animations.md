# CSS Animations

CSS animations enable elements to transition between different states or keyframes.

They provide more control than transitions, allowing multiple steps in the animation process.

Animations are defined using the `@keyframes` rule and applied to elements with the `animation` property.

## `@keyframes`
Defines the animation's keyframes (states or steps).

Syntax:

```CSS
@keyframes animation-name {
  0% { property: value; }
  30% { property: value; }
  50% { property: value; }
  ...
  100% { property: value; }
}

```

For example:

```CSS
@keyframes slideIn {
  0% {
    transform: translateX(-100%);
  }
  100% {
    transform: translateX(0);
  }
}
```

## `animation-name`
Specifies the name of the animation (matches the name in @keyframes).

```CSS
div {
  animation-name: slideIn;
}

@keyframes slideIn {
  0% {
    transform: translateX(-100%);
  }
  100% {
    transform: translateX(0);
  }
}
```

## `animation-duration`
Defines how long the animation takes to complete.

```CSS
div {
  animation-name: slideIn;
  animation-duration: 2s;
}

@keyframes slideIn {
  0% {
    transform: translateX(-100%);
  }
  100% {
    transform: translateX(0);
  }
}
```

## `animation-iteration-count`
Specifies how many times the animation repeats.

The default value is 1, meaning the animation runs once, you can supply a custom value or use the `infinite` keyword
which makes the animation run indefinitely.

```CSS
div {
  animation-name: slideIn;
  animation-duration: 2s;
  animation-iteration-count: 5;
}

@keyframes slideIn {
  0% {
    transform: translateX(-100%);
  }
  100% {
    transform: translateX(0);
  }
}
```

## `animation-direction`
Specifies the direction of the animation playback.

The values are:
- **normal**: Default, plays forward.
- **reverse**: Plays backward.
- **alternate**: Alternates between forward and backward.
- **alternate-reverse**: Alternates between backward and forward.

```CSS
div {
  animation-name: slideIn;
  animation-duration: 2s;
  animation-iteration-count: 5;
  animation-direction: alternate;
}

@keyframes slideIn {
  0% {
    transform: translateX(-100%);
  }
  100% {
    transform: translateX(0);
  }
}
```

## `animation-timing-function`
Controls the pacing of the animation.

The common values are:
- **ease** (default): Starts slow, accelerates, then slows down.
- **linear**: Constant speed.
- **ease-in**: Starts slow.
- **ease-out**: Ends slow.
- **ease-in-out**: Slow at both ends.
- **cubic-bezier(n, n, n, n)**: Custom timing function.

```CSS
div {
  animation-name: slideIn;
  animation-duration: 2s;
  animation-iteration-count: 5;
  animation-direction: alternate;
  animation-timing-function: ease-out;
}

@keyframes slideIn {
  0% {
    transform: translateX(-100%);
  }
  100% {
    transform: translateX(0);
  }
}
```

## `animation-delay`
Specifies a delay before the animation starts.

```CSS
div {
  animation-name: slideIn;
  animation-duration: 2s;
  animation-iteration-count: 5;
  animation-direction: alternate;
  animation-timing-function: ease-out;
  animation-delay: 3s;
}

@keyframes slideIn {
  0% {
    transform: translateX(-100%);
  }
  100% {
    transform: translateX(0);
  }
}
```