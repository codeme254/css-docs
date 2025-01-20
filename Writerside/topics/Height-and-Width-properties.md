# Height and Width properties

## `height`

The `height` property sets the height of an element to a specific value.

It can use any units like `px`, `em`, `rem`, `%`, `vh`, `vw`, e.t.c.

```HTML
<div>
    <h2>Hello, world</h2>
</div>
```

```CSS
div {
  border: 1px solid red;
  height: 300px;
}
```

![height](height.png)

### `max-height`

The `max-height` properties specifies the maximum height an element can grow to.

If the content height exceeds this value, it will be clipped.

```HTML
<div>
    <h2>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime ex
        quidem deserunt sed ipsum perspiciatis eum quibusdam dignissimos modi
        beatae.
    </h2>
</div>
```
```CSS
div {
  border: 3px solid red;
  height: 90px;
}
```
![max-height](max-height.png)

### `min-height`
The `min-height` property specifies the minimum height an element can shrink to.

Even if the content is smaller, the element cannot go below this height.
```HTML
<div>
    <h2>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime ex
        quidem deserunt sed ipsum perspiciatis eum quibusdam dignissimos modi
        beatae.
    </h2>
</div>
```

```CSS
div {
  border: 3px solid red;
  min-height: 250px;
}
```
![min-height](min-height.png)

## `width`
The `width` property sets the width of an element to a specified value.

It can use any units like `px`, `em`, `rem`, `%`, `vh`, `vw`, e.t.c.

```HTML
<h2>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ex, ut.</h2>
```
```CSS
h2 {
  border: 2px solid;
  width: 250px;
}
```
![width](width.png)

### `max-width`
The `max-width` property specifies the maximum width an element can grow to.

If the content width exceeds this value, it will wrap or be clipped.

```CSS
h2 {
  border: 2px solid;
  max-width: 50px;
}
```
![max-width](max-width.png)

### `min-width`
The `min-width` property specifies the minimum width an element can shrink to.

Even if the content is smaller, the element will not go below this width.

```HTML
<h2>Hello, world</h2>
```
```CSS
h2 {
  border: 2px solid;
  min-width: 150px;
}
```
![min-width](min-width.png)