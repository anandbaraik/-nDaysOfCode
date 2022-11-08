# DOM

- The Document Object Model (DOM) is a programming interface for web documents. It represents the page so that programs can change the document structure, style, and content.
- It starts with a html root element followed by head and body. The head and the body are the immediate children of the root element `html`. Before the root element, there is a declaration.

## Declaration

Declaration tells the browser that the document is Html & browser renders it as a html.

> `<!DOCTYPE html>`
>
> Code to declare a html. this declaration is not the part of DOM Tree.

## Root Element

The `html` element is the root of the dom tree and parent of `head & body`. the dom tree is wrapped by `html` tag.

```html
<!DOCTYPE html>
<html></html>
```

## DOM Tree

```html
<!DOCTYPE html>

<html>
  <head>
    <title>#40DaysOfCode</title>
  </head>
  <body>
    <h1 id="header">I'm the header</h1>
  </body>
</html>
```

The dom tree of above code snippet

![DOM Tree](https://user-images.githubusercontent.com/31516195/200629942-875cb9fe-de4d-4793-8269-8f930da2d1b4.png)

- Different kind of html elememts are -
  - Heading elements (h1 to h6)
  - Paragraph element (p)
  - Section element (section or div: `section` is semantic element & `div` is non semantic)
  - Header section (header)
  - Main section (main)
  - Footer section

## Inline style

We can use `style` html attribute to apply css to an html element. for ex:-

```

<h1 style="color:red"> I am a red text</h1>
```

## Inline element & Block element

Some element takes whole width where as some element takes the width required to fit the content.

- Inline element : occupies the space that is enough for the content.
- Block element: occupies the whole width of viewport.

List of block element

- `<address></address>`
- `<article></article>`
- `<aside></aside>`
- `<blockquote></blockquote>`
- `<canvas></canvas> `
- `<dd></dd>` : describe the name in description list
- `<dl></dl>` : create a description list
- `<dt></dt>` : describe about the term in description list
- `<div></div>`
- `<footer></footer>`
- `<form></form>`
- `<h1></h1> to <h6></h6>`
- `<header></header>` : create header of document
- `<hr/>`
- `<li></li>`
- `<main></main>` : wraps the main content of the document
- `<nav><nav>`
- `<noscript></noscript>`
- `<ol></ol>`
- `<ul><ul>`
- `<p></p>`
- `<pre></pre>` : create a space preserved content, eg poetry
- `<section><section>`
- `<table></table>`
- `<video></video>`

List of inline elements :

- `<a>`
- `<abbr>`
- `<acronym>`
- `<audio>`
- `<b>`
- `<bdo>` : reverse a text
- `<big>` : make text bigger
- `<br>`
- `<button>`
- `<cite>` : to add citation
- `<code>`
- `<dfn>` : write definition using HTML
- `<em>`
- `<i>`
- `<img>`
- `<input>`
- `<kbd>` : defines create keyboard inputs
- `<label>`
- `<map>`
- `<object>`
- `<output>`
- `<samp>`
- `<script>`
- `<select>`
- `<small>`
- `<span>`
- `<strong> `
- `<sub>`
- `<sup> `
- `<textarea>`
- `<time>` : represents a specific period of time
- `<var>`
- `<tt> `
