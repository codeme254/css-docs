# Flex Container

when we set the display property of the container to flex, the elements will be aligned side by side as shown:

```CSS
.container {
  background-color: #ccc;
  padding: 10px;

  display: flex;
}
```
![display: flex;](display-flex.png)

## `flex-direction`
The default value for the flex-direction is `row`, and that is why the elements are side by side.

![flex-direction: row;](display-flex.png)

`row-reverse`:
```CSS
.container {
  background-color: #ccc;
  padding: 10px;

  display: flex;
  flex-direction: row-reverse;
}
```
![row-reverse](row-reverse.png)

When we set the `flex-direction` property to be column, the main axis now goes from top to bottom, and the items end up
stacking on top of each other:

```CSS
.container {
  background-color: #ccc;
  padding: 10px;

  display: flex;
  flex-direction: column;
}
```
![flex-direction: column;](flex-direction-column.png)

Using `column-reverse` makes the main axis go from bottom to top, and the items end up as shown below:

![flex-direction: column-reverse;](column-reverse.png)

## `justify-content`
`center`: all the items are aligned to the center of the main axis.

```CSS
.container {
  display: flex;
  justify-content: center;
}
```

![justify-content: center;](justify-content-center.png)

`space-between`: the available space is evenly distributed between the flex items.

```CSS
.container {
  display: flex;
  justify-content: space-between;
}
```
![justify-content: space-between;](justify-content-space-between.png)

`space-around`: puts the same amount of space on both the left side and right side of each flex item.
```CSS
.container {
  display: flex;
  justify-content: space-around;
}
```
![justify-content: space-around;](justify-content-space-around.png)

_experiment with space-evenly, flex-end and flex-start which is the default_


## `align-items`
To better visualize the working of `align-items` property, let's change the height of one of the flex items.

```HTML
<div class="container">
    <div class="item">1</div>
    <div class="item i2">2</div>
    <div class="item">3</div>
    <div class="item">4</div>
    <div class="item">5</div>
</div>
```
```CSS
.i2 {
  height: 200px;
}
```
![align-items: stretch;](align-items-stretch.png)

Notice that all the elements end up getting the 200px height, this is because the initial value on align-items property
is stretch.

`center`: center flex-items relative to the item which is taller/bigger in the vertical direction.

```CSS
.container {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

![align-items: center;](align-items-center.png)

`flex-start`
```CSS
.container {
  display: flex;
  justify-content: center;
  align-items: flex-start;
}
```

![align-items: flex-start;](align-items-flex-start.png)

_experiment with the flex-end value and baseline as well_