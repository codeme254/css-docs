# CSS Backgrounds

CSS background properties allow you to control the appearance of an element's background.

These properties add/control background effects for an element.

These properties are:
- background-color
- background-image
- background-repeat
- background-attachment
- background-position
- background (shorthand property)

## `background-color`
The `background-color` adds a solid color behind an element.

It can take color values like named colors, hex, RGB, HSL, and others.

```HTML
<h1>This is the title</h1>
```
```CSS
h1 {
  background-color: crimson;
}
```
![background color](background-color.png)

## `background-image`
The `background-image` property sets an image as the background of an element.

It takes `url()` function as a value where you pass the path to the image you want to use as a background.

```HTML
<div>
    <h1>Hello world</h1>
</div>
```
```CSS
div {
  height: 400px;
  background-image: url(pets.jpg);
}
```
![background image](background-image.png)

## `background-repeat`
When we use an image as a background, by default, the image is repeated so that it covers the entire element as shown
below:

![background image](background-image.png)

The background-repeat property controls if and how the background image repeats.

We can use this property to turn off this behavior or control this behavior.

By default, the image repeats both horizontally and vertically.

The `background-repeat` property takes the following values:
- _**repeat**_: (default value) repeats both horizontally and vertically.
- _**repeat-x**_: repeats only horizontally.
- _**repeat-y**_: repeats only vertically.
- _**no-repeat**_: prevents an image from repeating.

The image below is repeated both vertically and horizontally
```HTML
<div>
    <h1>Hello world</h1>
</div>
```

```CSS
div {
  height:550px;
  background-image: url(pets-small.jpg);
}
```
![default repeat behavior](default-repeat.png)


We can make it repeat horizontally by passing `repeat-x` as the value to `background-repeat`.

```CSS
div {
  height:550px;
  background-image: url(pets-small.jpg);
  background-repeat: repeat-x;
}
```
![repeat-x](repeat-x.png)

We can also make it repeat vertically only by passing `repeat-y` as the value to `background-repeat`.

```CSS
div {
  height:550px;
  background-image: url(pets-small.jpg);
  background-repeat: repeat-y;
}
```
![repeat-y](repeat-y.png)

If we don't want the background to be repeated, we can pass `no-repeat` as the value to `background-repeat`

```CSS
div {
  height:550px;
  background-image: url(pets-small.jpg);
  background-repeat: no-repeat;
}
```
![no-repeat](no-repeat.png)

## `bakcground-attachment`
The `background-attachment` property determines whether the background scrolls with the page or stays fixed in place.

The options are:
- _**scroll**_: (default); background scrolls with the page.
- _**fixed**_: background stays in place while the page content scrolls.

```HTML
<div>
    <h1>Hello world</h1>
</div>
```

```CSS
div {
  height:550px;
  background-image: url(pets-small.jpg);
  background-attachment: fixed;
}
```

## `background-position`
The background-position property specifies the starting position of the background image.

You can define it using the following keywords; `top`, `center`, `bottom`, `left` and `right`.

Examples:

```HTML
<div>
    <h1>Hello world</h1>
</div>
```

we can position the background image at the center:
```CSS
div {
  height:550px;
  background-image: url(pets-small.jpg);
  background-repeat: no-repeat;
  background-position: center;
}
```
![position center](pos-center.png)

we can position the background image to the right:

```CSS
div {
  height:550px;
  background-image: url(pets-small.jpg);
  background-repeat: no-repeat;
  background-position: right;
}
```
![position right](pos-right.png)

We can also combine these keywords, for example, we can position the image to the top right.

```CSS
div {
  height:550px;
  background-image: url(pets-small.jpg);
  background-repeat: no-repeat;
  background-position: right top;
}
```

![position top right](pos-top-right.png)

## `background-size`
The `background-size` property defines the size of the background image.

The options are:
- _**auto**_ (default): keeps the original size of the image.
- _**cover**_: scales the image to cover the entire element.
- _**contain**_: fits the image within the element maintaining its aspect ratio.
- You can also use custom dimensions, e.g., 100 px.

```HTML
<div>
    <h1>Hello world</h1>
</div>
```

```CSS
div {
  height:550px;
  background-image: url(pets.jpg);
  background-repeat: no-repeat;
  background-size: cover;
}
```
![background-size: cover;](back-size-cover.png)


Background size set to `contain`;
```CSS
div {
  height:550px;
  background-image: url(pets.jpg);
  background-repeat: no-repeat;
  background-size: contain;
}
```
![background-size: contain;](back-size-contain.png)

## `background` shorthand
The `background` shorthand property combines all the individual background properties into one declaration.

Here is the syntax:
```CSS
background: [COLOR] [IMAGE] [REPEAT] [ATTACHMENT] [POSITION] / [SIZE];
```

Consider the CSS code below:

```CSS
div {
  height:550px;
  background-color: crimson;
  background-image: url(pets-small.jpg);
  background-repeat: no-repeat;
  background-attachment: scroll;
  background-position: left;
  background-size: contain;
}
```
It ends up producing this output:
![background](bg-all.png)

We can use the `background` shorthand to summarize the code above to a single line as shown:

```CSS
div {
  height:550px;
  background: crimson url(pets-small.jpg) no-repeat scroll left / contain;
}
```