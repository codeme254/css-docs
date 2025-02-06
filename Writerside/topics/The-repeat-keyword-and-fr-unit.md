# The repeat keyword and fr unit

So far, we have been defining our rows and columns one by one:

```CSS
grid-template-rows: 200px 200px;
grid-template-columns: 200px 200px 200px;
```

Imagine we had 10 rows, for example, each one 150px in height; it wouldn't make sense to have to define all of them
one by one as we have been doing.

In CSS Grid, we have the `repeat` keyword which can help us to simplify this.

Syntax:
```CSS
grid-template-rows: repeat(NUMBER_OF_TIMES, SIZE);
```

```CSS
.container {
  display: grid;
  grid-template-rows: repeat(2, 150px);
  grid-template-columns: repeat(3, 150px);

  row-gap: 30px;
  column-gap: 30px;
}
```

Assuming we wanted the third column track to occupy more space, we can easily define that as shown:

```CSS
.container {
  display: grid;
  grid-template-rows: repeat(2, 150px);
  grid-template-columns: repeat(2, 150px) 300px;

  row-gap: 30px;
  column-gap: 30px;
}
```
![bigger third column track](grid-bigger-third-column-track.png)

What if we want the third column track to occupy the rest of the grid container.

In grid, we can use the `fr` unit; this will make the track expand to occupy all the remaining space.

The fr unit in CSS Grid stands for fractional unit.

It is used to define a flexible portion of available space within a grid container.

The fr unit distributes space proportionally among grid tracks (rows or columns).

- `1fr` means one fraction of the available space.
- `2fr` means twice as much space as `1fr`.
- e.t.c..

```CSS
.container {
  display: grid;
  grid-template-rows: repeat(2, 150px);
  grid-template-columns: repeat(2, 150px) 1fr;

  row-gap: 30px;
  column-gap: 30px;
}
```

![](fr-unit-1.png)

We can use the fr unit to make our column tracks have the same width:

```CSS
.container {
  display: grid;
  grid-template-rows: repeat(2, 150px);
  grid-template-columns: repeat(3, 1fr);

  row-gap: 30px;
  column-gap: 30px;
}
```

![equal column tracks](equal-column-tracks.png)