# CSS Flexbox

Flexbox is a module in CSS that makes it easy to align items to one another, in different directions and orders.

The main idea behind flexbox is to allow the container to expand and to shrink elements to best use all the available
space.

Flexbox is used to build one-dimensional layouts.

## Important terms in CSS Flexbox
The element on which we use flexbox is known as a **flex container**.

To change an element to a flex container, we set its display property to flex or inline-flex. (inline-flex will
create a flex container that behaves like an inline element).

```CSS
div {
    display: flex;
}
```
or 
```CSS
div {
    display: inline-flex;
}
```

All the direct children of a flex container are called **flex items**.

The direction in which these **flex items** are laid out is known as the **main axis**.

The other perpendicular axis is called the **cross axis**.

There are properties used on the flex container and other properties used of flex items themselves.

![flex](flex.png)

## Flex container properties
- **flex-direction**: Specifies in which direction the main axis goes. The default value is **row**.
The other values are: **row-reverse**, **column**, **column-reverse**.
- **flex-wrap**: defines if the flex items should wrap into a new line if there's not enough space in the flex container
or not. The default value is **nowrap**, other values are **wrap** and **wrap-reverse**.
- **justify-content**: defines how the flex items will be aligned along the main axis. The default value is
**flex-start**, other values are **flex-end**, **center**, **space-between**, **space-around**, **space-evenly**.
- **align-items**: defines how the flex items will be aligned along the cross-axis. The default value is **stretch**,
other values are **flex-start**, **flex-end**, **center** and **baseline**.
- **align-content**: only applies when there's more than one row of flex items. In that case, align-content controls
how the rows are aligned along the cross-axis. The default value is **stretch**, other values are **flex-start**,
**flex-end**, **center**, **space-between**, **space-around**.

## Flex items properties
- **align-self**: very similar to **align-items**, but for one individual flex item. The default value is **auto**,
other values are **stretch**, **flex-start**, **flex-end**, **center**, **baseline**.
- **order**: defines the order in which one specific flex-item should appear in the container. The default value is
**0**, but you can pass an integer value.,
- **flex-grow**: defines how much an element can grow, the default value is **0**, but you can pass an integer value.
- **flex-shrink**: defines how much an element can shrink, the default value is **1**, but you can pass an integer
value.
- **flex-basis**: defines the base width of an element, the default value is **auto**, but you can pass a length e.g.
300px.
- **flex**: shorthand for **flex-grow**, **flex-shrink** and **flex-basis**

## Code Setup
```HTML
<div class="container">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
    <div class="item">4</div>
    <div class="item">5</div>
</div>
```

```CSS
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.container {
  background-color: #ccc;
  padding: 10px;
}

.item {
  background-color: #f1425d;
  padding: 40px;
  margin: 10px;
  color: #fff;
  font-size: 20px;
}
```

![flexbox setup](flexbox-setup.png)