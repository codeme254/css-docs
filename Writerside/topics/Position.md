# Position

The position property in CSS determines how an element is positioned in the document flow and how it interacts 
with other elements.

The values for position property are:
- **static**
- **relative**
- **fixed**
- **absolute**
- **sticky**

These properties work hand in hand with the **top**, **bottom**, **right**, and **left** properties to adjust the 
position of the element.


## **static** (default)
The element is positioned according to the normal document flow (its default position in the layout).

Does not respond to top, right, bottom or left.


## **relative**
The element is positioned relative to its normal position in the document flow.

The element remains in the flow but you can adjust its position using top, right, bottom, left.

```HTML
<div></div>
```

```CSS
div {
  width: 50px;
  height: 50px;
  background-color: red;

  position: relative;
  top: 50px;
  left: 100px;
}
```
![position: relative;](position-relative.png)

## **fixed**
The element is positioned relative to the viewport (the browser window).

It stays in the same position even when the page is scrolled.

The element is removed from the normal document flow.

Can be used in sticky headers, footers, or elements like back-to-top button.

```CSS
div {
  position: fixed;
  top: 20px;
  right: 20px;
}
```

## **absolute**

The element is positioned relative to its nearest positioned ancestor (an ancestor with relative, absolute, or 
fixed position).

If no positioned ancestor exists, it positions itself relative to the initial containing block (the html element).

The element is removed from the normal document flow.

Used in precise placement of elements, overlays or tooltips.

```HTML
<div class="parent">
    <div class="child"></div>
</div>
```

```CSS
.parent {
  width: 300px;
  height: 300px;
  background-color: green;
  position: relative;
}

.child {
  width: 100px;
  height: 100px;
  background-color: red;

  position: absolute;
  bottom: 10px;
  right: 20px;
}
```

![position: absolute;](position-absolute.png)

## **sticky**
Behavior: The element toggles between relative and fixed depending on the scroll position.

The element acts as relative until it reaches a defined offset (top, bottom, left, right), then it becomes fixed.

```CSS
.parent {
  width: 100%;
  height: 20px;
  background-color: green;
  margin-top: 100px;

  position: sticky;
  top: 0px;
  left: 0;
}
```

## The `z-index` property
Sometimes when working with the position property, elements end up stacking on top each other, in such cases, we might
want a certain element to appear in front of the other, this is where the z-index property comes in.

The z-index property in CSS controls the stacking order of elements on the z-axis (visual depth).

It determines which elements appear in front of or behind others.

z-index works only on elements with a positioning context (position set to relative, absolute, fixed, or sticky). 
It does not apply to static elements.

The default value is auto, which means the element follows the natural stacking order.

Elements with a higher z-index value appear in front of those with a lower value.

```HTML
<div class="element1"></div>
<div class="element2"></div>
```

```CSS
.element1 {
  width: 150px;
  height: 150px;
  background-color: green;

  position: absolute;
  top: 10px;
  left: 10px;
}

.element2 {
  width: 130px;
  height: 130px;
  background-color: red;

  position: absolute;
  top: 20px;
  left: 20px;
}
```
![example](z-index-1.png)

In the example above, the red and green boxes are stacked on top of each other, we can make the green element appear
on top of the red element by giving the green element a higher z-index than the red element.

```CSS
.element1 {
  width: 150px;
  height: 150px;
  background-color: green;

  position: absolute;
  top: 10px;
  left: 10px;
  z-index: 1000;
}

.element2 {
  width: 130px;
  height: 130px;
  background-color: red;

  position: absolute;
  top: 20px;
  left: 20px;
  z-index: 200;
}
```
![example](z-index-2.png)