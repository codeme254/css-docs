# Adding CSS to HTML

There are three main ways to include CSS in HTML:

- Inline CSS
- Internal CSS
- External CSS

## Inline CSS

Inline CSS applies styles directly to an HTML element using the `style` attribute within the opening tag of the element.

```HTML
<h1 style="font-size: 24px; color: crimson;">Hello, world</h1>
```

## Internal CSS

Internal CSS is defined within a `<style>` block inside the `<head>` section of the HTML document.

It applies styles to elements within the same page.

```HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <title>CSS</title>
    <style>
        h1 {
            font-size: 24px;
            color: crimson;
        }
    </style>
</head>
<body>
    <h1>Hello, world</h1>
</body>
</html>
```

## External CSS

External CSS involves writing styles in a separate `.css` file and linking it to the HTML document using the `<link>`
tag in the `<head>` section.

index.html:

```HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <title>CSS</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Hello, world</h1>
</body>
</html>
```

style.css

```CSS
h1 {
    color: crimson;
    font-size: 24px;
}
```

## Best practices when including CSS in HTML

1. Use external CSS for most projects to keep your HTML clean and styles reusable.
2. Avoid inline CSS unless absolutely necessary for one-off changes.
3. Use internal CSS sparingly, mainly for prototyping or one-page designs.
