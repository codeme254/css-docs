# The Display Property

The CSS display property defines how an element is displayed on the page and determines the layout behavior 
of the element and its children.

The common values of display are: `block`, `inline`, `inline-block`, `none`, `flex`, `grid`, `inline-flex`, and
`inline-grid`.

## block
Makes an element a block level element, taking up the full width of its container.
```HTML
<div>
    <a href="#">Home</a>
    <a href="#">About</a>
    <a href="#">Services</a>
    <a href="#">Contact</a>
</div>
```
The anchor tags are inline elements, which means they take up only the space they need.
![before](displa-block-before.png)

We can make them occupy the entire parent width using `display: block;`
```CSS
a {
  display: block;
  border: 1px solid red;
}
```
![after](display-block-after.png)

## inline
Makes the element an inline-level element, only as wide as its content, without starting a new line.

```HTML
<div>
    <h2>service 1</h2>
    <h2>service 2</h2>
    <h2>service 3</h2>
</div>
```

Before:
![before](display-inline-before.png)

```CSS
h2 {
  display: inline;
}
```
After:
![after](display-inline-after.png)

## flex
Turns an element into a flex container, the element also becomes a block level element (more about this later).

`inline-flex` is similar to `flex` but the element is displayed inline.

## grid
Turns an element into a grid container, the element also becomes a block level element (more about this later).

`inline-grid` is similar to `grid` but the element is displayed inline.