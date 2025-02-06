# Our First CSS Grid

```HTML
<div class="container">
    <div class="item item--1">1: orange</div>
    <div class="item item--2">2: green</div>
    <div class="item item--3">3: violet</div>
    <div class="item item--4">4: pink</div>
    <div class="item item--5">5: blue</div>
    <div class="item item--6">6: brown</div>
</div>
```

```CSS
.container {
  background-color: #eee;
  width: 1000px;
  margin: 30px auto;
}
```

## Turning an element into a grid container
To turn an element into a grid container, we set its display property to grid.

```CSS
.container {
  display: grid;
}
```

## Defining rows and columns
We can use `grid-template-rows` to define the height and structure of rows within a CSS Grid layout.

Assume we want two rows in our grid, each 200px in height:

```CSS
.container {
  display: grid;
  grid-template-rows: 200px 200px;
}
```

![grid-template-rows: 200px 200px;](grid-template-rows.png)

This creates two tracks for the rows.

Similarly, we can use `grid-template-columns` to define the width and structure of columns within a CSS Grid layout.

Assume we want three columns in our grid, each 200px wide:

```CSS
.container {
  display: grid;
  grid-template-rows: 200px 200px;
  grid-template-columns: 200px 200px 200px;
}
```
![combining rows and columns](grid-template-rows-and-columns.png)

This creates three tracks for the columns.

Complete the set-up:
```CSS
.item {
  padding: 20px;
  font-size: 30px;
  font-family: sans-serif;
  color: white;
}

.item--1 {
  background-color: orange;
}

.item--2 {
  background-color: green;
}

.item--3 {
  background-color: violet;
}

.item--4 {
  background-color: pink;
}

.item--5 {
  background-color: blue;
}

.item--6 {
  background-color: brown;
}
```
![grid complete setup](grid-complete-setup.png)

## Adding gutters with `row-gap` and `column-gap`
We can have space between the grid items and this is called a gutter.

### `row-gap`
Adds vertical spacing (gutter) between adjacent rows in a grid layout.

```CSS
.container {
  display: grid;
  grid-template-rows: 200px 200px;
  grid-template-columns: 200px 200px 200px;

  row-gap: 30px;
}
```

![row-gap](row-gap.png)

### `column-gap`
Adds horizontal spacing (gutter) between adjacent columns in a grid layout.

```CSS
.container {
  display: grid;
  grid-template-rows: 200px 200px;
  grid-template-columns: 200px 200px 200px;

  row-gap: 30px;
  column-gap: 30px;
}
```

![column-gap](column-gap.png)

If you want to use same-sized gutter in the row and column, you can use the `gap` property.