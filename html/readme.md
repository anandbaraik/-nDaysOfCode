# why do we need html?

Html is the building block of web. there is no website without html so to develop a website it requires html.

- Html stands for `hypertext markup language`.
- useful to build the skeleton/outline of websites. these outline can be styled by using css. javascript can be used to add interactivity to these outlines.

## Parts of website

A website can have several features & sections like -

    - Logo
    - Hero section
    - Navbar/Sidebar
    - Forms
    - Footer
    - Sections
    - Buttons
    - Links
    - Medias (Image/Video/Audio)

### first ever created website - [world wide web](http://info.cern.ch/hypertext/WWW/TheProject.html)

## How the web works? [visit for detailed explanation](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/How_the_Web_works)

- When we type web address(like example.com) in the browser. browser goes to DNS server and finds the real address of server where website(like example.com) lives. then the browser sends an HTTP request to the server asking to send copy of this website(like example.com) to client in smaller chunks. this communication and all other data sent between client & server happens in internet connection using internet protocol `TCP/OP`.
- If the server accepts client's request, the server sends back "200 OK" message and starts sending website's files to the browser in smaller chunks called data-packet.
- Browser assembles these smaller chunks into a complete web page & displayed to us.

## Order in which component files are parsed

- Html files
- Css/JS files (as the browser parses html, if it finds any css/js file. it sends request back to server & then parses the css & js)
- Then browser generate the [Document object model](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) from the parsed html. generate the [Css object model](https://developer.mozilla.org/en-US/docs/Web/API/CSS_Object_Model) structure from the parsed css & [compiles & executes](https://developer.mozilla.org/en-US/docs/Web/Performance/How_browsers_work#javascript_compilation) the parsed javascript.

## HTML Element

Html element consists of an opening tag(<>), contents & closing tag (</>)

> ex: `<h1> Welcome to #40DaysOfCodes.</h1>`
> here `h1` is a html tag & `Welcome to #40DaysOfCodes.` is a content.

## Html Attribute

Attributes provides an additional informations about an element & contents. an attribute can only be added in the opening tag.

> ex: `<img src="image src" alt="image description">`
> here `alt` is an attribute in `img` tag which specifies the description about image and displayed to user when image is unavailable.

some of the most used attributes are :-

- alt
- autocomplete
- autofocus
- autoplay
- class
- id
- data-attribute (used to add custom info like: `data-name="anand"`)
- download
- for
- href
- type
- style

there are some event listeners attribute as well like `onclick`, `onsubmit`, `onkeydown` etc. useful to catch the events triggered by javascript for a specific element.

- there are few html tags which are self clossing. like:

  - `<br/>`
  - `<hr/>`
  - `<img/>`
  - `<link/>`
  - `<input/>`
  - `<meta/>`

* here `/` is optional for self closing tag but recommended to use it.

# HTML Comment

Comments are helpful to make codes more readable.

> `<!-- this is a paragraph which tells about lorem ipsum -->`
>
> <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries</p>

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

# Inline and Inline-block element

- Inline element : it respects only left & right spacing. it does not allow to set width & height. it does not force a line break.

- Inline-block element : it respects all top, bottom, left & right spacing. it allows setting width & height and starts on a new line if there is a line break.

# Formatting Elements

- `<b>`
- `<strong>` : make an important text
- `<i>`
- `<em>` : Make emphases to text
- ` <mark>`
- `<small>`
- `<del>`
- `<ins>` : inserted text
- `<sub>`
- `<sup>`
- `<pre>` : Preserve text space
- `<u>`

# Semantic Elements

Semantic elements are basically elements with a meaning. it tells us the purpose of any peice of code. using semantic elements will help search engine to better rank website and also screen readers to help visually impaired users.

list of semantic elements :

```
 <article>
 <aside>
 <details>
 <figcaption>
 <figure>
 <footer>
 <header>
 <main>
 <mark>
 <nav>

 <section>
 <summary>
 <time>
```

# Non Semantic Elements

Elements dont have any meaning and do not tell us anything about its content.

Ex: `<div>, <span>`

# MetaTags

Defines metadata about html document. metadata is basically an information about data. meta tag always goes in the `head` tag. it is mostly used for seo purpose. the metadata is not rendered on the website but is used by search engine to rank & display some data about website when you search it on the internet.

```
- <base> : specifies the base URL to use for all relative URLs in a document.
- <head> : contains metadata about the document
- <link>
- <meta> : represents about meta data which can't be represented by other meta tag
- <style> : contains style information about document
- <title> : defines the document title
```

# Grouping elements

```
- <div>
- <main>
- <p>
- <hr>
- <ul>
- <ol>
- <li>
- <dl>
- <dt>
- <pre>
```

# Multimedia tags & attributes

```
<!-- multimedia  tags -->
- <audio>
- <video>
- <source>
- <embed>
- <track>

<!-- attributes -->
- id
- class
- style
- src
- alt
- width & height
- forms attribute (action, method)
- event attributes (onclick, onsubmit)
```

# HTTP Methods

- GET : used for requesting data from specified resources. it can be cached & bookmarked. it remains in the browser history. can't be used to modify data and it should not be used when dealing with sensitive data. restriction on data length.
- POST : used to send data to server to create a resource. cant be cached & bookmarked and it does not remain in browser history. no restriction on data length
- PUT : used to send data to server to update a resource.
- PATCH : used to send data to a server to apply partial modification to a resource.
- DELETE : deletes the specified resource.
- HEAD : useful for checking what a GET request will return before actually making a GET request - like before downloading a large file or response body.
- OPTIONS : describes the communication options for the target resource.
- CONNECT : sed to start a two-way communications (a tunnel) with the requested resource.
- TRACE : used to perform a message loop-back test that tests the path for the target resource (useful for debugging purposes).

# web accessibility

Accessibility is all about making the web accessible for the disable people.So, that they can also navigate and access the web as the non-disable person.

> Accessibility is also known as a11y. The reason, there are 11 characters between a and y.

# Types of disability

- Vision
- Hear
- Speech
- Motor : People who have a problem with the movement of the hands, legs, fingers, slow response time, limited fine motor control
- Cogntive : Learning disabilities, distractibility, inability to remember or focus on large amounts of information. If there is caption asking to click images with 'trees' or what is 9 + 4 then it is going to be issue for the users

# Tools to test the accessibility?

- Chrome Lighthouse
- Wave
- Axe
- Screen readers - nvda, voiceover, jaws

# Basics of accessibility

- Correct structure of the HTML page
- alt tags of the images
- Keyboard focus
- Captions and subtitles of the video and audio
- Alternatives of captions such as what is 1+1
- Not color based messages and UI
- Responsive
- proper labels
- Avoid read more links and add descriptive content
- Proper color contrast
- ARIA tags
- Dynamic Content alert for screen readers
- Accessible forms: accessible by keyboard, clear criteria for the password, username etc., descriptive error messages, proper labels of input fields.
- Language support as per the geography

### Resources

- [Accessibility-MDN](https://developer.mozilla.org/en-US/docs/Web/Accessibility)
- [A11YTIPS](https://www.a11ytips.dev)
