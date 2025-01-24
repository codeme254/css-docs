# CSS Overflow

The overflow property in CSS controls how content is displayed when it overflows the boundaries of its container.

It is commonly used to manage scrollbars or hide excess content.

The overflow property takes the following values:
- **visible (default)**
- **hidden**
- **scroll**
- **auto**

## `visible` (default)
Behavior: Content that overflows the container is not clipped and remains visible outside the container's boundaries.

Rarely used deliberately; suitable when overflow content should be fully displayed without restrictions.

```HTML
<div>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Possimus nostrum,
      accusantium similique voluptas natus tempora unde mollitia doloribus,
      explicabo perferendis nisi atque dicta! Enim explicabo nesciunt incidunt
      iure, facilis inventore.
</div>
```
```CSS
div {
  width: 200px;
  height: 100px;
  border: 2px solid red;
  overflow: visible; /* default */
}
```
![overflow: visible;](overflow-visible.png)

## `hidden`
Content that overflows the container is clipped and hidden from view.

```CSS
div {
  width: 200px;
  height: 100px;
  border: 2px solid red;
  overflow: hidden;
}
```
![overflow: hidden;](overflow-hidden.png)

## `scroll`
Content that overflows is clipped, but scrollbars are always added to scroll to see the content
(even if not necessary).

```CSS
div {
  width: 200px;
  height: 100px;
  border: 2px solid red;
  overflow: scroll;
}
```
![overflow: scroll;](overflow-scroll.png)

![overflow:scroll;](overflow-scroll-2.png)

In the example above, the scroll bars appear even when not necessary (when content is not overflowing), the `auto`
value fixes this.

## `auto`
Content that overflows is clipped, and scrollbars appear only when necessary.

```CSS
div {
  width: 200px;
  height: 100px;
  border: 2px solid red;
  overflow: auto;
}
```
![overflow: auto;](overflow-auto.png)

![overflow: auto;](overflow-auto-2.png)

## `overflow-x` and `overflow-y`
The overflow-x and overflow-y properties control the overflow behavior for the horizontal (x) and vertical 
(y) axes independently.

The values are similar to the overflow property and behave similar.