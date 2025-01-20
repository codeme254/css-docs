# CSS Padding

Padding is the space between the content of an element and its border.

It creates an inner space around the content, ensuring the content does not touch the edges of the element.

## Applying padding

You can apply padding to the individual sides of an element using the following properties:

- **padding-top**: Specifies the padding space on the top side of the element.
- **padding-bottom**: Specifies the padding space on the bottom side of the element.
- **padding-right**: Specifies the padding space on the right side of the element.
- **padding-left**: Specifies the padding space on the left side of the element.

```HTML
<h2>Hello, world</h2>
```

```CSS
h2 {
  border: 2px solid crimson;
  padding-top: 15px;
  padding-bottom: 50px;
  padding-right: 10px;
  padding-left: 30px;
}
```

![padding](padding-4-sides.png)

## Padding shorthand

The padding shorthand property in CSS allows you to set the padding for all four sides of an element in a
single declaration.

The syntax can vary depending on how many values you specify:

- **One value**: applies the same padding to all sides.

```CSS
h2 {
  border: 2px solid crimson;
  padding: 30px;
}
```

![1 value padding](padding-1-value.png)

- **Two values** The first applies to the top and bottom, and the second applies to the left and right.

```CSS
h2 {
  border: 2px solid crimson;
  padding: 30px 100px;
}
```

![2 values padding](padding-2-values.png)

- **Three values**: The first one applies to the top, the second to the right and left, and the third to the bottom.

```CSS
h2 {
  border: 2px solid crimson;
  padding: 15px 40px 100px;
}
```

![3 values padding](padding-3-values.png)

- **Four values**: Each value applies to a specific side, starting from the top and moving clockwise.

```CSS
h2 {
  border: 2px solid crimson;
  padding: 10px 20px 30px 40px;
}
```

![4 values padding](padding-4-values.png)

## The `padding-block` property

The `padding-block` property applies padding to the top and bottom of an element.

```CSS
h2 {
  border: 2px solid crimson;
  padding-block: 50px;
}
```

![padding-block](padding-block.png)

To apply padding to the top only, you can use `padding-block-start` and to apply padding to the bottom only, you can use
`padding-block-end`.

```CSS
h2 {
  border: 2px solid crimson;
  padding-block-start: 20px;
  padding-block-end: 50px;
}
```

![padding-block-start and padding-block-end](padding-block-start-end.png)

## The `padding-inline` property

The `padding-inline` property applies padding to the left and right of an element.

```CSS
h2 {
  border: 2px solid crimson;
  padding-inline: 50px;
}
```

![padding-inline](padding-inline.png)

You can use `padding-inline-start` to apply padding to the left and `padding-inline-end` to apply padding to the right.
