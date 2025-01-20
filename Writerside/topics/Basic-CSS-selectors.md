# Basic CSS selectors

To style elements on a webpage, CSS relies on selectors to target specific HTML elements.

A CSS selector is a pattern used to identify the HTML elements you want to style.

Think of selectors as a way to tell CSS: "Apply these styles to this element or group of elements.

Some basic selectors are:

- Class selectors
- ID selector
- Type/Element selector
- Grouping selector
- Universal selector

## Class Selector

The class selector is used to target elements that have a specific `class` attribute.

Classes are reusable, meaning you can apply the same class to multiple elements.

Classes are ideal for applying styles to multiple elements that share the same design.

```HTML
<p class="text">The sky is blue.</p>
<p class="text">The grass is green.</p>
```

```CSS
.text {
  font-size: 18px;
  color: crimson;
}
```

## ID Selector

The ID selector targets a single element with a specific `id` attribute.

IDs are unique, meaning each element can have only one ID, and no two elements should share the same ID.

```HTML
<h1 id="title">A good day</h1>
```

```CSS
#title {
  font-size: 24px;
  color: crimson;
}
```

## Type/Element Selector

The type selector (also called the element selector) targets all elements of a specific HTML tag.

For example, you can style all `<p>` tags or all `<h1>` tags.

Element selector is useful for applying general styles across a webpage.

```HTML
<p>The sky is blue.</p>
<p>The grass is green.</p>
<p>It's a beautiful day.</p>
```

```CSS
p {
  font-size: 18px;
  color: crimson;
}
```

## Grouping Selector

The grouping selector is used to apply the same styles to multiple elements by separating their selectors with a comma.

This reduces repetition and makes the code more clean and efficient.

The grouping selector is ideal for applying common styles to multiple elements.

```HTML
<h1>This is a heading</h1>
<p>This is a paragraph</p>
<h3>This is a subheading</h3>
<p class="text">This is more text</p>
<h4 id="subtitle">This is a subtitle</h4>
```

```CSS
h1, p, h3, .text, #subtitle {
  color: crimson;
  font-size: 18px;
}
```

## Universal Selector

The universal selector targets all elements in a webpage.

It is represented by an asterisk (\*).

The universal selector is often used for resetting styles to ensure consistent behavior across browsers.

```HTML
<h1>This is a heading</h1>
<p>This is a paragraph</p>
<h3>This is a subheading</h3>
<p class="text">This is more text</p>
<h4 id="subtitle">This is a subtitle</h4>
```

```CSS
* {
  font-size: 18px;
  color: crimson;
}
```
