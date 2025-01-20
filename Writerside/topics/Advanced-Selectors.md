# Advanced Selectors

Some advanced selectors in CSS are:

- Combinator selectors
- Pseudo-classes
- Attribute selectors
- Pseudo-elements
- Compound selectors

## Combinator selectors

Combinator selectors allow you to style elements based on their relationship with other elements.

There are four main types of combinator selectors:

- Descendant selector
- Direct child selector
- Adjacent sibling selector
- General sibling selector

### Descendant selector (` `)

The descendant selector selects elements that are descendants (children, grandchildren, e.t.c) of another selector.

The syntax is:

```CSS
ancestor descendant {
    /* styles */
}
```

```HTML
<div class="parent">
    <p>Roses are </p>
    <div>
        <p>violets are blue</p>
        <div>
            <p>CSS is fun</p>
        </div>
    </div>
</div>
```

```CSS
.parent p {
   background-color: crimson;
}
```

![direct child](direct-child.png)

### Direct child selector (`>`)

The direct child selector selects only the direct child of an element.

The syntax is:

```CSS
parent > child {
  /*styles*/
}
```

```HTML
<div class="parent">
    <p>Roses are </p>
    <div>
        <p>violets are blue</p>
        <div>
            <p>CSS is fun</p>
        </div>
    </div>
</div>
```

```CSS
.parent > p {
   background-color: crimson;
}
```

![direct child selector](direct-child-selector.png)

### Adjacent sibling selector (`+`)

The adjacent sibling selector selects an element immediately preceded by a specified sibling element.

The syntax is:

```CSS
element1 + element2 {
    /* styles */
}
```

```HTML
<h1>Hello world</h1>
<p>Learning CSS is pure fun</p>
<p>Another paragraph, but it won't be selected</p>

<h1>My title</h1>
<p>My paragraph</p>
<p>Another paragraph</p>
<p>Yet another paragraph</p>
```

```CSS
h1 + p {
  background-color: red;
}
```

![adjacent sibling selector](adjacent-sibling-selector.png)

### General sibling selector (`~`)

The general sibling combinator selects all siblings of an element that share the same parent and appear after the
specified element.

The syntax is:

```CSS
element1 ~ element2 {
    /* styles */
}
```

```HTML
<span>Text up above but won't be selected</span>
<h1>Hello world</h1>
<p>Learning CSS is pure fun</p>
<p>Another paragraph, but it won't be selected</p>

<h1>My title</h1>
<p>My paragraph</p>
<p>Another paragraph</p>
<p>Yet another paragraph</p>
```

```CSS
h1 ~ p {
  background-color: red;
}
```

In the example above, the span is a sibling to the first h1 element, but it will not be selected because it's not coming
after the h1.

![general sibling selector](general-sibling-selectr.png)

## Pseudo-classes

Pseudo-classes are special keywords in CSS that target elements based on their state, position, or relationship
to other elements.

### Structural pseudo-classes

These pseudo-classes are used to select elements based on their position in the DOM structure.

#### `:first-child`

Targets the first child of its parent.

```HTML
<ol>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
    <li>Item 4</li>
    <li>Item 5</li>
    <li>Item 6</li>
</ol>
```

```CSS
li:first-child {
   background-color: crimson;
}
```

![first child](first-child.png)

#### `:last-child`

Targets the last child of its parent.

```CSS
li:last-child {
   background-color: crimson;
}
```

![last child](last-child.png)

#### `:nth-child(n)`

Targets the nth child of its parent.

```CSS
li:nth-child(3) {
  background-color: crimson;
}
```

![nth child](n-th-child.png)

#### `:nth-last-child(n)`

Targets the nth child from the end.

```CSS
li:nth-last-child(2) {
  background-color: crimson;
}
```

![nth last child](nth-last-child.png)

#### `:only-child`

Targets an element that is the only child of its parent.

```HTML
<div>
    <p>Hello, world</p>
</div>
```

```CSS
p:only-child {
  background-color: crimson;
}
```

![only child](only-child.png)

### Interactive pseudo-classes

These pseudo-classes apply styles based on user interaction.

Examples:

#### `:hover`

Styles an element when the user hovers on it.

```HTML
<button>Click me</button>
```

```CSS
button:hover {
   background-color: crimson;
}
```

#### `:focus`

Styles an element when it is focused, e.g., a text input.

```HTML
<input type="text" placeholder="enter your name" class="name-input">
```

```CSS
.name-input:focus {
  background-color: #ccc;
}
```

#### `:active`

Styles an element when it is being clicked on.

```HTML
<button>Click me</button>
```

```CSS
button:active{
  background-color: crimson;
}
```

#### `:visited`

Styles a link that the user has already visited.

```HTML
<a href="https://google.com">Open link</a>
```

```CSS
a:visited {
  color: orange;
}
```

#### `:link`

Styles an unvisited link.

```HTML
<a href="https://google.com">Open link</a>
```

```CSS
a:link {
  color: orange;
}
```

### Form pseudo-classes

These pseudo-classes are used for styling form elements based on their state.

#### `:checked`

Targets checked checkboxes or radio buttons.

```HTML
<input type="checkbox" checked class="checkbox" />
<h1>Hello world</h1>
```

```CSS
.checkbox:checked + h1 {
  color: red;
}
```

![:checked pseudo-class](checked.png)

#### `:disabled`

Targets disabled form elements.

```HTML
<input type="text" placeholder="username" class="username" disabled>
```

```CSS
.username:disabled {
  background-color: #999;
}
```

![:disabled pseudo class](disabled-pseudo-class.png)

#### `:required`

Targets form elements with the `required` attribute.

```HTML
<input type="text" placeholder="username" class="username" required />
```

```CSS
.username:required {
  background-color: green;
  color: white;
}
```

![:required pseudo class](required.png)

#### `:invalid`

Targets form elements with invalid input.

```HTML
<input type="number" max="1000" placeholder="amount" class="amount-input" />
```

```CSS
.amount-input:invalid {
  background-color: red;
}
```

![:invalid pseudo class](invalid.png)

## Attribute selectors

CSS attribute selectors allow you to target HTML elements based on their attributes and attribute values.

### Types of attribute selectors

#### `[attribute]`

Select elements with the specified attribute, regardless of its value.

Example: `[type]` selects all elements with a type attribute.

```HTML
<input type="text" placeholder="username" />
<input type="password" placeholder="password" />
```

```CSS
[type] {
  background-color: crimson;
}
```

![[type] attribute selector](type.png)

#### `[attribute="value"]`

Select elements where the attribute's value matches exactly.

Example: `[type="password"]` selects only `<input>` elements with `type="password"`.

```HTML
<input type="text" placeholder="username" />
<input type="password" placeholder="password" />
```

```CSS
[type="password"] {
    background-color: crimson;
}
```

![[type="value"]](type=value.png)

#### `[attribute~="value"]`

Select elements where the attribute's value is a space-separated list of words, and one of the words matches.

Example: `[class~="button"]` matches elements with `class="button primary"` or `class="secondary button"`,
but not `class="buttons"`.

```HTML
<button class="button">just a button</button>
<button class="primary button">primary button</button>
<button class="secondary text-white button">secondary button</button>
<button class="buttons">action button</button>
```

```CSS
[class~="button"] {
    background-color: red;
}
```

![[type~=value]](type~=value.png)

#### `[attribute^="value"]`

Select elements where the attribute's value starts with the specified value.

Example: `[href^="https"]` matches links starting with `https`.

```HTML
<a href="https://example.com">Secure Link</a>
<a href="https://google.com">visit google</a>
<a href="http://example.com">Non-Secure Link</a>
```

```CSS
[href^="https"] {
    color: green;
}
```

![type^=value](type^=value.png)

#### `[attribute$="value"]`

Select elements where the attribute's value ends with the specified value.

Example: `[src$=".jpg"]` matches images with `.jpg` extensions.

```HTML
<a href="https://example.com">Secure Link</a>
<a href="https://google.com">visit google</a>
<a href="https://example.net">Non-Secure Link</a>
```

```HTML
[href$=".com"] {
    color: green;
}
```

#### [attribute*="value"]

Select elements where the attribute's value contains the specified value anywhere.

Example: [title*="important"] matches elements with a title attribute containing the word "important" anywhere.

```HTML
<p title="important text">some important text</p>
<p title="this text is also important">another important text</p>
<p title="some text">some text</p>
```

```CSS
[title*="important"] {
    color: green;
}
```

![title*=important](titlestartequalimportant.png)

## Pseudo-elements

CSS pseudo-elements allow you to style specific parts of an element without requiring additional markup.

### Common Pseudo-elements

#### `::first-line`

Styles only the first line of text within a block-level element.

```HTML
<p>
      Lorem ipsum dolor sit, amet consectetur adipisicing elit. Totam,
      dignissimos reiciendis, veniam quibusdam facere, incidunt natus
      impedit nobis quia harum facilis sint aut iste maxime? Excepturi
      officia quos natus autem libero labore ullam, pariatur quo enim
      quasi doloribus velit reprehenderit aliquid amet ad nemo nulla
      nostrum! Ipsa dolorem ullam voluptatem.
</p>
```

```CSS
p::first-line {
  color: red;
}
```

![:first-line pseudo element](first-line-pseudo-element.png)

#### `::first-letter`

Styles the first letter of the first line of a block-level element.

```CSS
p::first-letter {
    font-size: 48px;
    color: crimson;
}
```

![:first-letter](first-letter.png)

#### `::selection`

Styles the portion of an element that the user has selected (highlighted with the mouse or keyboard).

```HTML
<h1>title</h1>
<p>
    Lorem ipsum dolor sit, amet consectetur adipisicing elit. Totam,
    dignissimos reiciendis, veniam quibusdam facere, incidunt natus
    impedit nobis quia harum facilis sint aut iste maxime? Excepturi
    officia quos natus autem libero labore ullam, pariatur quo enim
    quasi doloribus velit reprehenderit aliquid amet ad nemo nulla
    nostrum! Ipsa dolorem ullam voluptatem.
</p>
```

```CSS
h1::selection {
    background-color: green;
    color: white;
}

p::selection {
    background-color: crimson;
    color: white;
}
```

![::selection pseudo element](selection.png)

#### `::placeholder`

```HTML
<input type="text" placeholder="enter your name" class="name-input">
```

```CSS
.name-input::placeholder {
    color: crimson;
}
```

![::placeholder pseudo element](placeholder.png)
