# CSS Custom properties (variables)

Custom properties (sometimes referred to as CSS variables or cascading variables) are entities defined by CSS 
authors that represent specific values to be reused throughout a document.

Complex websites have very large amounts of CSS, and this often results in a lot of repeated CSS values.

For example, it's common to see the same color used in hundreds of different places in stylesheets. Changing a color 
that's been duplicated in many places requires a search and replace across all rules and CSS files.

Custom properties allow a value to be defined in one place, then referenced in multiple other places so that 
it's easier to work with.

## Defining CSS Custom Properties
CSS variables are defined within a CSS rule, typically inside the :root pseudo-class for global scope.

A custom property is prefixed with `--`, followed by the property name (e.g., --my-property), 
and a property value that can be any valid CSS value.

syntax
```CSS
--variable-name: value;
```

example

```CSS
:root {
  --primary-color: #3498db;
  --font-medium-size: 16px;
}
```

## Using CSS custom properties
To use a css variable/custom properties, reference them with the `var()` function.

```CSS
:root {
  --primary-color: #3498db;
  --font-medium-size: 16px;
}

h2 {
  color: var(--primary-color);
  font-size: var(--font-medium-size);
}
```

## fallback values
CSS variables can have fallback values if the variable is not defined.

```CSS
:root {
  --primary-color: #3498db;
  --font-medium-size: 16px;
}

h2 {
  color: var(--primary-color, red);
  font-size: var(--font-medium-size, 18px);
}
```