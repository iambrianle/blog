---
Title: Here is the Best Beginner-Friendly HTML Cheatsheet 
Description: In this post, I'll show you everything you need to know to code in Python and score high on basic Python tests.
Date: 2022-09-29T14:50:50+08:00
Draft: false
Tags: ["guide", "python"]
Categories: ["coding"]
Showtoc: true
Author: "Brian Le"

---
# Basic HTML

Welcome to the world of HTML! In this cheat sheet, I'll show you everything you need to know to get started with HTML and create your own web pages.

## HTML Structure

Every HTML document follows a basic structure:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Page Title</title>
</head>
<body>
  <!-- Your content goes here -->
</body>
</html>
```

Let's break down the structure:

- `<!DOCTYPE html>` declares the document type and must be placed at the very beginning of the HTML file.

- The `<html>` element is the root element of the HTML document and contains all other elements.

- Inside the `<html>` element, we have the `<head>` element, which contains metadata about the document, such as the page title.

- The `<title>` element is placed inside the `<head>` element and sets the title of the web page, which appears in the browser's title bar or tab.

- The `<body>` element contains the visible content of the web page. This is where you can add text, images, links, and other elements.

## Heading and Paragraph

To create headings and paragraphs in HTML, you can use the following tags:

- `<h1>` to `<h6>`: These tags represent different levels of headings, with `<h1>` being the highest and `<h6>` being the lowest.
Example:
```html
<h1>This is a Heading Level 1</h1>
<h2>This is a Heading Level 2</h2>
```
- `<p>`: This tag is used to create paragraphs of text.
Example:
```html
<p>This is a paragraph.</p>
```

## Links

To create links in HTML, you can use the `<a>` tag with the `href` attribute. The `href` attribute specifies the destination of the link (the URL of the web page).
Example:
```html
<a href="https://www.example.com">Click here</a> to visit our website.
```

## Images

To add images to your web page, use the `<img>` tag with the `src` attribute. The `src` attribute specifies the path to the image file.
Example:
```html
<img src="image.jpg" alt="Description of the image">
```
The `alt` attribute provides alternative text for the image, which is displayed if the image cannot be loaded.

## Lists

There are two types of lists in HTML: ordered lists and unordered lists.

- Ordered lists (`<ol>`) are used for numbered lists.
Example:
```html
<ol>
  <li>Item 1</li>
  <li>Item 2</li>
</ol>
```

- Unordered lists (`<ul>`) are used for bullet point lists.
Example:
```html
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
</ul>
```

## Tables

To create tables in HTML, you can use the `<table>` tag along with other table-related tags such as `<tr>` (table row), `<th>` (table header), and `<td>` (table data).
Example:
```html
<table>
  <tr>
    <th>Name</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>John</td>
    <td>25</td>
  </tr>
  <tr>
    <td>Jane</td>
    <td>30</td>
  </tr>
</table>
```

## CSS

CSS (Cascading Style Sheets) is used to style your HTML elements. You can apply CSS styles to HTML elements using the `style` attribute or by linking an external CSS file.

- Inline CSS (using the `style` attribute):
Example:
```html
<p style="color: blue;">This paragraph is blue.</p>
```

- External CSS (using a separate CSS file):
Create a separate CSS file with a .css extension and link it to your HTML file using the `<link>` tag. Example:
```html
<head>
  <link rel="stylesheet" href="styles.css">
</head>
```

## Conclusion

By now, you should have a good understanding of the basic HTML tags and structure. Remember to practice and experiment with HTML to further enhance your skills. Happy coding!

## Next Steps
Ready to learn more about HTML? Check out [W3Schools](https://www.w3schools.com/html/) for detailed tutorials and examples.

## Sources
Adapted from various HTML resources and personal knowledge.