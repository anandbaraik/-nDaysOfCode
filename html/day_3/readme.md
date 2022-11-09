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
