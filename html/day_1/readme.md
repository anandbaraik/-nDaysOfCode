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
