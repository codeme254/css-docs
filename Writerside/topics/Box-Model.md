# Box Model

The CSS Box Model is a fundamental concept in web design that defines how elements are displayed and how their 
dimensions (width, height, padding, borders, and margins) are calculated.

Understanding the box model is crucial for layout and spacing in CSS.

## Components of the box model
Each HTML element is treated as a rectangular box comprising four areas:
- **Content**: The area where text, images, or other content is displayed.
- **Padding**: Space between the content and the border.
- **Border**: A line surrounding the padding and content.
- **Margin**: Space between the border of an element and adjacent elements. Adds space outside the element, 
pushing it away from other elements.

![box model](box-model.png)

## Box Model Dimensions
The size of an element is calculated as:

**Total Width** = `width + padding-left + padding-right + border-left + border-right + margin-left + margin-right`

**Total Height** = `height + padding-top + padding-bottom + border-top + border-bottom + margin-top + margin-bottom`

## Box Model Types
### Standard Box Model(default)
The width and height properties apply to the content only. Padding, borders, and margins are added on top.

This is the default behavior and is the equivalent of `box-sizing: content-box;`

```HTML
<div class="standard">
    <h2>Hello world</h2>
</div>
```
```CSS
.standard {
  width: 200px;
  padding: 10px;
  border: 5px solid black;
  margin: 15px;
}
```
![standard box sizing](standard-box-sizing.png)

### Alternative (`box-sizing: border-box;`)
The width and height properties include content, padding, and border.

```HTML
<div class="standard">
    <p>box-sizing: content-box;</p>
</div>
<div class="border-box">
    <p>box-sizing: border-box;</p>
</div>
```
```CSS
.standard {
  width: 200px;
  padding: 10px;
  border: 5px solid black;
  margin: 15px;
}

.border-box {
  width: 200px;
  padding: 10px;
  border: 5px solid black;
  margin: 15px;
  box-sizing: border-box;
}
```
![border-box vs content-box](border-box.png)


The border box behavior is the behavior that is commonly used as it makes creating layouts easier, the convention is 
to target all elements and change their box-sizing property to border-box when starting out css styling.

```CSS
* {
  box-sizing: border-box;
}
```