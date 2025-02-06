# Spanning Grid Items

We can span grid items across multiple grid cells in order to occupy an area.

We can do this using the `grid-row-start`, `grid-row-end` and `grid-column-start`, `grid-column-end` properties.

We have been using these properties to place items in single cells, this way, the end is just the beginning plus 1, for
example grid-row-start at 2 and grid-row-end at 3, if we put a higher number for the end, then the item will occupy
more cells.

```CSS
.item--1 {
  background-color: orange;
  grid-row: 2 / 3;
  grid-column: 2 / 4;
}
```

![spanning grid item](spanning-grid-items-1.png)

## The `span` keyword
We can use the span keyword to declare across how many grid cells a grid item should extend

```CSS
.item--1 {
  background-color: orange;
  grid-row: 2 / 3;
  grid-column: 2 / span 2;
}
```

The very end of a grid container is represented by -1.

```CSS
.item--1 {
  background-color: orange;
  grid-row: 2 / 3;
  grid-column: 1 / -1;
}
```
![span all the way to the end of a grid](span-to-the-end-of-a-grid.png)