# Flex Items

## `align-self`
Overrides the align-items property for an individual flex item.

```CSS
.i3 {
  align-self: flex-end;
}
```

![align-self: flex-end;](align-self.png)

_experiment with flex-start, stretch and center_

## `order`
Flexbox orders all the elements according to their order number, in ascending order. The default value for
all the elements is 0.

Elements with a lower order number are shown in the beginning.

```CSS
.i3 {
  order: -1;
}
```
![order](order.png)

## `flex-grow`
Gives an item the ability of an element to grow.

Specify an integer.

```CSS
.i3 {
  flex-grow: 1;
}
```

## `flex-basis`
Used to set the width of a flex item.

```CSS
.i3 {
  flex-basis: 400px;
}
```

![flex-basis](flex-basis.png)

## `flex-shrink`
Allows an element to shrink.

## `flex` shorthand.
```CSS
flex: <grow> <shrink> <basis>;
```