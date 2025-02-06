# Positioning Grid Items

We can position items wherever we want on the grid.

So far, all our grid items are laid out in their source order.

We can place a grid item where we want, let's for example reposition the first item with the orange background to a
different grid cell.

We can do this using the `grid-row-start`, `grid-row-end` and `grid-column-start`, `grid-column-end` properties as shown

```CSS
.item--1 {
  background-color: orange;
  grid-row-start: 2;
  grid-row-end: 3;
  grid-column-start: 2;
  grid-column-end: 3;
}
```

![positioning a grid item](position-grid-item.png)

We can simplify the code above using `grid-row` and `grid-column`

```CSS
grid-row: START / END;
grid-column: START / END;
```

```CSS
.item--1 {
  background-color: orange;
  grid-row: 2/3;
  grid-column: 2/3;
}
```

We can simplify the above code even further using `grid-area` property:

```CSS
grid-area: ROW-START / COLUMN-START / ROW-END / COLUMN-END;
```

```CSS
.item--1 {
  background-color: orange;
  grid-area: 2 / 2 / 3 / 3;
}
```