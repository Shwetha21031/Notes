**HTML, or Hypertext Markup Language**, is the standard language used to create and design web pages. 
It provides the structure and content of a webpage, defining elements such as text, images, links, and multimedia.

```
Hypertext - Hypertext is text displayed on a computer or other digital device that contains links to other text

Markup Language - A markup language is a system for annotating text to indicate semantic meaning or structure. It uses tags or codes embedded within the text to define elements and their attributes, such as formatting, layout, and organization. These tags are interpreted by software applications to render or process the text according to the specified instructions.

Examples: Some common markup languages include:
   - HTML (Hypertext Markup Language): Used for creating web pages and defining their structure and content.
   - XML (Extensible Markup Language): Used for storing and exchanging structured data.
   - Markdown: A lightweight markup language used for formatting plain text documents, commonly used in README files, documentation, and forums.
   - LaTeX: A typesetting system used for creating professional-looking documents, particularly in academia and publishing.
```

Here's a brief overview of HTML:

### Structure:
- HTML documents are structured using elements enclosed in opening and closing tags (`<tag>`...`</tag>`).
- The basic structure of an HTML document includes `<html>`, `<head>`, and `<body>` tags.
  - `<html>`: Contains the entire HTML document.
  - `<head>`: Contains metadata about the document, such as title, character set, and links to external resources.
  - `<body>`: Contains the visible content of the document.
- [more on structure](/html/structure.md)
### Elements:
- HTML elements define the structure and content of a webpage.
- Examples of elements include headings (`<h1>`...`<h6>`), paragraphs (`<p>`), images (`<img>`), links (`<a>`), lists (`<ul>`, `<ol>`, `<li>`), and more.

### Attributes:
- HTML elements can have attributes that provide additional information about the element.
- Attributes are specified within the opening tag and are written as name-value pairs (e.g., `attribute="value"`).
- Examples of attributes include `src` for specifying the source of an image and `href` for specifying the destination of a link.

### Semantic HTML:
- Semantic HTML elements convey meaning to both the browser and developers, improving accessibility and SEO.
- Examples of semantic elements include `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`, `<aside>`, and more.

### HTML5:
- HTML5 is the latest version of HTML, introducing new elements, attributes, and APIs.
- It offers improved support for multimedia, graphics, and interactive features, making it suitable for modern web development.

### Basic Example:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My First Web Page</title>
</head>
<body>
    <header>
        <h1>Welcome to My Website</h1>
    </header>
    <nav>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
    <main>
        <section id="home">
            <h2>Home</h2>
            <p>This is the homepage of my website.</p>
        </section>
        <section id="about">
            <h2>About</h2>
            <p>Learn more about us.</p>
        </section>
        <section id="contact">
            <h2>Contact</h2>
            <p>Get in touch with us.</p>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 My Website. All rights reserved.</p>
    </footer>
</body>
</html>
```
