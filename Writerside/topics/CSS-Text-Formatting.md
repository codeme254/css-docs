# CSS Text Formatting

## `color` property
The color property in CSS is used to set the color of the text.

It’s one of the most fundamental and widely used properties for styling web pages.

```HTML
<p>
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Omnis nulla,
      dolorem aspernatur ex nemo voluptatibus, maxime voluptatum blanditiis sed
      magni in ullam unde mollitia quas fuga quisquam laborum harum rerum
      temporibus architecto! Nostrum nesciunt porro velit ea, itaque autem ab
      earum nihil vero, qui consectetur esse ad voluptas placeat laboriosam?
</p>
```

```CSS
p {
  color: crimson;
}
```
![color](color.png)

## `text-align` property
The css `text-align` property is used to control horizontal alignment of text.

The values for `text-align` property are:
- **left**: aligns text to the left.
- **right**: aligns text to the right.
- **center**: centers the text horizontally.
- **justify**: spreads text evenly, aligning both left and right edges.

The default value is left.

```HTML
<p>
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Omnis nulla,
      dolorem aspernatur ex nemo voluptatibus, maxime voluptatum blanditiis sed
      magni in ullam unde mollitia quas fuga quisquam laborum harum rerum
      temporibus architecto! Nostrum nesciunt porro velit ea, itaque autem ab
      earum nihil vero, qui consectetur esse ad voluptas placeat laboriosam?
</p>
```

**right align**
```CSS
p {
  text-align: right;
}
```
![right align](align-text-right.png)

**center align**
```CSS
p {
  text-align: center;
}
```
![center align](align-text-center.png)

**justify align**
```CSS
p {
  text-align: justify;
}
```
![justify align](align-text-justify.png)

## `text-align-last`
The `text-align-last` property specifies the alignment of the last line of text.

It also takes `left`, `right`, `center` and `justify` as its values.

**Example 1: aligning the last line to the right**
```CSS
p {
  text-align: justify;
  text-align-last: right;
}
```
![text-align-last: right;](text-align-last-right.png)

**Example 2: aligning the last line to the left**
```CSS
p {
  text-align: justify;
  text-align-last: center;
}
```
![text-align-last: center;](text-align-last-center.png)

## `text-transform`
The `text-tranform` property is used to control the capitalization of text.

The values are:
- **none**: No transformation, the text appears as written.
- **capitalize**: transforms the first letter of each word to uppercase.
- **uppercase**: transforms all text to uppercase.
- **lowercase**: transforms all text to lowercase.

**capitalize**
```CSS
p {
  text-transform: capitalize;
}
```
![capitalize](capitalize.png)

**uppercase**
```CSS
p {
  text-transform: uppercase;
}
```
![uppercase](uppercase.png)

**lowercase**
```CSS
p {
  text-transform: lowercase;
}
```
![lowercase](lowercase.png)

## `text-decoration`
The `text-decoration` property is used to set the appearance of decorative lines on a text.

It is shorthand for the following properties:
- **text-decoration-line**
- **text-decoration-color**
- **text-decoration-style**
- **text-decoration-thickness**

### `text-decoration-line`
Specify the type of line applied to text.

Values:
- **none**: no decoration (default).
- **underline**: adds a line below the text.
- **overline**: adds a line above the text.
- **line-through**: adds a strikethrough.

```HTML
<h2 class="none">Hello world</h2>
<h2 class="overline">Hello world</h2>
<h2 class="underline">Hello world</h2>
<h2 class="line-through">Hello world</h2>
```

```CSS
.none {
  text-decoration: none;
}

.overline {
  text-decoration: overline;
}

.underline {
  text-decoration: underline;
}

.line-through {
  text-decoration: line-through;
}
```

![text decoration line](text-decoration-line.png)

### `text-decoration-color`
Specifies the color of the line applied to text.

```CSS
.none {
  text-decoration: none;
}

.overline {
  text-decoration: overline;
  text-decoration-color: crimson;
}

.underline {
  text-decoration: underline;
  text-decoration-color: blue;
}

.line-through {
  text-decoration: line-through;
  text-decoration-color: rgb(15, 246, 19);
}
```
![text decoration color](text-decoration-color.png)

### `text-decoration-thickness`
Sets the thickness of the decoration line.

```CSS
.none {
  text-decoration: none;
}

.overline {
  text-decoration: overline;
  text-decoration-color: crimson;
  text-decoration-thickness: 15px;
}

.underline {
  text-decoration: underline;
  text-decoration-color: blue;
  text-decoration-thickness: 5px;
}

.line-through {
  text-decoration: line-through;
  text-decoration-color: rgb(15, 246, 19);
  text-decoration-thickness: 10px;
}
```
![text decoration thickness](text-decoration-thickness.png)

### `text-decoration-style`
Defines the style of the text decoration line.

Values:
- **solid**: (default) a single solid line.
- **double**: two parallel lines.
- **dotted**: a dotted line.
- **dashed**: a dashed line.
- **wavy**: a wavy line.

```CSS
.none {
  text-decoration: none;
}

.overline {
  text-decoration: overline;
  text-decoration-color: crimson;
  text-decoration-thickness: 5px;
  text-decoration-style: dashed;
}

.underline {
  text-decoration: underline;
  text-decoration-color: blue;
  text-decoration-thickness: 5px;
  text-decoration-style: wavy;
}

.line-through {
  text-decoration: line-through;
  text-decoration-color: rgb(15, 246, 19);
  text-decoration-thickness: 3px;
  text-decoration-style: double;
}
```
![text decoration style](text-decoration-style.png)

### `text-decoration` shorthand
The shorthand combines the above properties for compact declarations.

There is no specific order for the declarations, however; for the declaration to take effect, you must specify
the `text-decoration-style` somewhere in the declaration.

```CSS
.underline {
    text-decoration: red wavy 5px underline;
}
```

## `text-indent`
Defines the indentation of the first line of text in a block.

```HTML
<p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempora omnis
      maiores repudiandae expedita numquam ullam, assumenda quisquam eius
      dolores dolorem distinctio! Facilis asperiores sed ab, corporis illo unde
      dolorum mollitia perferendis optio, atque rem aliquid earum corrupti, odio
      porro quibusdam. Fugiat odio culpa, dignissimos eaque explicabo libero
      dolorum repellat mollitia. Lorem ipsum dolor sit amet consectetur
      adipisicing elit. Provident, adipisci iste sint illum architecto quam
      consequuntur. Corporis libero quas nobis dignissimos deserunt assumenda
      aspernatur earum sint, dolorem ipsam nesciunt neque, quam, fugit culpa.
      Laboriosam velit dicta minus, in, aliquam, eaque sed consequuntur
      consequatur vel sunt perspiciatis corporis ea qui? Eligendi?
</p>
```
```CSS
p {
  text-indent: 150px;
}
```
![text-indent](text-indent.png)

## `letter-spacing`
Controls the spacing between characters in a text.

```CSS
p {
  letter-spacing: 5px;
}
```
![letter spacing](letter-spacing.png)

## `line-height`
This property controls the distance between lines of text.

For the value, a good practice is to use a unit-less number, which will be multiplied by the element's font-size to
get the line-height value.

```CSS
p {
  line-height: 2;
}
```

![line height](line-height.png)

## `word-spacing`
Specifies the spacing between words in a text.

```CSS
p {
  word-spacing: 20px;
}
```
![word spacing](word-spacing.png)