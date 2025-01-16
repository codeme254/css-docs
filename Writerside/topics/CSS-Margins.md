# CSS Margins

In CSS, margins are the space outside an element's border, used to create separation between the element 
and surrounding elements.

## Applying margins
You can apply margins to individual sides of an element using the following properties:
- **margin-top**: specifies the margin above an element.
- **margin-bottom**: specifies the margin below an element.
- **margin-right**: specifies the margin to the right of an element.
- **margin-left**: specfies the margin to the left of an element.

```HTML
<h3>top element</h3>
<h2>the element</h2>
<h3>bottom element</h3>
```

```CSS
h2 {
  margin-top: 20px;
  margin-bottom: 50px;
  margin-left: 100px;
  margin-right: 50px;
}
```
![margin on individual sides of element](margin-on-individual-sides-of-an-element.png)

## Margin shorthand
The margin shorthand property in CSS allows you to define margins for multiple sides of an element in a 
single declaration.

The syntax is:
```CSS
margin: [top] [right] [bottom] [left];
```

### variants for the `margin` shorthand

#### four values
- `margin: top right bottom left;`
- set margins on all four sides explicitly.

```CSS
h2 {
  margin: 20px 50px 50px 100px;
}
```

#### three values
- `margin: top right-left bottom;`
- sets the top margin, a shared value for the left and right margin and the bottom margin.
```CSS
h2 {
  margin: 10px 20px 30px;
} 
```

#### two values
- `margin: top-bottom right-left`;
- sets a shared margin for the top and bottom, and another for the left and right.
```CSS
h2 {
  margin: 10px 20px;
} 
```

#### one value
- `margin: all;`
- Applies margin to all the four sides.
```CSS
h2 {
  margin: 20px;
} 
```

## `margin-block`
The `margin-block` property applies margins to the top and bottom and of an element.

```CSS
h2 {
  margin-block: 100px;
}
```
![margin-block](margin-block.png)

### `margin-block-start` vs `margin-block-end`
`margin-block-start` applies margin to the top of the element only while `margin-block-end` applies margin to the bottom
of the element only.

```CSS
h2 {
  margin-block-start: 30px;
  margin-block-end: 69px;
}
```
![margin-block-start and margin-block-end](margin-block-start-end.png)

## `margin-inline`
The `margin-inline` property applies margins to the left and right of an element.
```CSS
h2 {
  margin-inline: 100px;
}
```
![margin-inline](margin-inline.png)

### `margin-inline-start` vs `margin-inline-end`
`margin-inline-start` applies margin to the left of an element only while `margin-inline-right` applies margin to the
right of an element only.

```CSS
h2 {
  margin-inline-start: 40px;
  margin-inline-end: 30px;
}
```
![margin-inline-start and margin-inline-end](margin-inline-start-end.png)