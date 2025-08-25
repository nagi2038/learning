# ESSENTIAL HTML

- Editor : VS Code
- VS code Extension : **Live Server**, **Prettier**

---

- [ESSENTIAL HTML](#essential-html)
  - [Short cuts in VS CODE](#short-cuts-in-vs-code)
  - [CREATE \& OPEN HTML File](#create--open-html-file)
  - [HTML Tags \& Attributes](#html-tags--attributes)
    - [COMMON TAGS](#common-tags)
    - [Tag Attributes](#tag-attributes)
  - [Document Structure](#document-structure)
    - [Comments in HTML](#comments-in-html)
  - [SandBox Files Setup](#sandbox-files-setup)
  - [Meta Tags \& Search](#meta-tags--search)
    - [Charset](#charset)
    - [View Port](#view-port)
    - [Description and Keywords](#description-and-keywords)
    - [Author](#author)
    - [Robots](#robots)
  - [Headings,Paragraphs \& Emphasis](#headingsparagraphs--emphasis)
  - [Browser Devtools Intro](#browser-devtools-intro)
  - [Lists](#lists)
  - [Anchor Tags](#anchor-tags)
  - [Images](#images)
    - [Image Attributes](#image-attributes)
    - [Fig and fig caption](#fig-and-fig-caption)
  - [Block vs Inline Elements](#block-vs-inline-elements)
  - [Line Breaks, Horizontal Rules \& Entities](#line-breaks-horizontal-rules--entities)
    - [HTML Entities](#html-entities)
  - [div and span](#div-and-span)
  - [Classes \& IDs](#classes--ids)
  - [Sematic Elements](#sematic-elements)
  - [Emmet Crash Course](#emmet-crash-course)
  - [Keyboard Shortcuts](#keyboard-shortcuts)

## Short cuts in VS CODE

- `Ctrl + Enter` it create a new line and move the cursor to next line
- `! + Enter` it will create a boiler plate HTML code
- `Ctrl + s` it save the file with adding **prettier** it format the docs.
- `Ctrl + /` to mark line as comment.
- `Ctrl + D` to copy previous line to next or selected text.
- Run command `Create Table of Contents` (in the VS Code Command Palette) to insert a new table of contents.

## CREATE & OPEN HTML File

- File name extension : `.html`
- Why `index.html` ? => By default returned file from server is `index.html`
- Why not file extension can be `.txt`? Browser does not understand file and do not phrase the `HTML` text rather render it is a normal file.

## HTML Tags & Attributes

- Tags are the building blocks of a web page.
- Used to structure content
- Most have an open and closing tags

**TAG**  
tags are used to structure our content.
`<tagname>My Content</tagname>`

Some **tags** offer styling like `<h1>` , `<p>`  
`<h1>` - make font size larger and default color black  
`<p>` - make font size small default color black

\*\*NOTE - Styling should be done by CSS only.

### COMMON TAGS

- `<html>` : Root element of a webpage wrap every thing except `<DOCTYPE>` tag.
- `<head></head>` : Contains document information such as the title (content not gonna show in browser window)
- `<title></title>` : Title of document
- `<body></body>` : Body/Content of document (display the content on browser)
- `<h1>-<h6>` : Headings
- `<p>` : Paragraphs
- `<a>` : Link to other pages or resources.
- `<img>` : Images
- `<ul><ol>` : Unordered and Ordered Lists
- `<table>` : Tables
- `<div><span>` : Generic Containers
- `<form><input>` : Forms & inputs.

### Tag Attributes

```HTML
<tagname attributeName="value">Content</tagname>
<tagname attributeName="value" /> ( SELF CLOSING TAGS )
```

- Attributes provide additional information
- Some tags do not include content and only include attributes
- Slash is Optional on self-closing tags

## Document Structure

```html
<!DOCTYPE html>
<!--Tells browser it's an HTML5 document-->
<html lang="en">
  <!-- Root element-->
  <head>
    <!--Contains meta info, title, links to other resources, etc-->
    <title>My First Web Page</title>
    <!--title of the page-->
  </head>
  <body>
    <!--page content-->
    <h1>hello World!</h1>
  </body>
</html>
```

### Comments in HTML

```html
<!--This is comment line in HTML-->
```

- All these comments are also show on webpage
- Avoid providing sensitive data in comments.

## SandBox Files Setup

- Maintain two folder
  - Start folder
  - Finished folder

It will be easy for the bigener to solve and practice.

## Meta Tags & Search

- Snippets of text that describe the content of a web page.
- They are not visible on the web page & are placed in head.
- Search engines can use these tags to understand the content.
- Some tags can impact SEO( Search Engine Optimization )

### Charset

```html
<meta charset="UTF-8" />
```

- Specifies character encoding
- HTML5 spec encourages UTF-8 standard, since it covers all symbols in the world.
- Should be the first child element in the `<head>`

### View Port

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

- Controls layout on different device/screen size.
- Width is set to the width of the device.
- Initial scale is set to 1.0 to ensure no unwanted zoom, etc.

### Description and Keywords

```html
<meta
  name="description"
  content="Learn HTML, CSS and JS with our beginner-friendly tutorials."
/>

<meta
  name="keywords"
  content="HTML, CSS, JS,  Web development
  />
```

- Description is displayed in search results
- Description should be no more than 160 characters( It will be shown on browser)
- Keywords should relate to the page content

### Author

```html
<meta name="author" content="John Doe" />
```

- Provides information about the content author
- Good to use on blog Posts

### Robots

```html
<meta name="robots" content="index, follow" />
```

- Controls how search engines index the page
- index/noindex tells whether to index the page or not.
- follow/nofollow tells whether to index and follow links.

## Headings,Paragraphs & Emphasis

- Good to have only single `<h1>` tag per page.
- Other `<h>` you can have multiple tags in same page.
- `<h>` and `<p>` are **block** level tags ( Block means It will take whole horizontal space )
- `<strong>`, `<emp>`, `<ins>`, `<mark>`, `<del>`, `<sub>`, `<sup>` are **inline** tag. ( It do not push the text next to it to next other line)

## Browser Devtools Intro

- `Right Click + Inspect`, `F12` to navigate to dev tools
- Element menu
- Console menu
- Styles menu ( check what default or customized style applied )
- .hov option
- .cls option
- Editing text in elements tag
- Changing screen resolution
- checking with different mobile versions
- docking of dev tools tab

## Lists

- Unordered list `<ul>` tag
  - By default they are built points
  - We can remove the bullet point by changing the property `list-style-type: none;`
  - you can add other shapes `circle`, `square`, `disc`, `auto`, `decimal`, `disclosure-open`, `disclosure-close` ..
- Ordered list `<ol>` tag
- Nested Order list
- Definition list `<dl>` tag
  - It has `<dt>` definition term
  - It has `<dd>` definition description

## Anchor Tags

- `<a>` is an anchor tag
- self closing tag
- it will have an attribute `href` where navigation address is provided.
  - navigate `target` attribute
  - `_blank` it opens new web page
  - by default it is `_self` it open in web page
  - Explore `_parent` and `_top`
- you can link internal tag `#service` which is id tag of other element.
- you can link mail `mailto:yourmail@gmail.com`
- you can link telephone number `tel:+9194324325`
- you can link you local file like PDFs
- you can add attribute `title` on hover it show the title message.

## Images

```html
<img src="/image.jpg" alt="Image" />
```

- `src` is the location of the image.
- `alt` is alternate text if image is not displayed.
- Image can be added as background image using CSS
- Self closing tag

### Image Attributes

- `width` define the width of the image
- `height` defines the height of the image
- `title` defines the title of the image(on hover it will show the text)

### Fig and fig caption

```html
<figure>
  <img src="images/landscape.jpg" alt="Landscape" />
  <!-- it will caption the figure -->
  <figcaption>Fig.1 - Beautiful landscape</figcaption>
</figure>
```

## Block vs Inline Elements

| Inline Elements                                           | Block Elements                                                         |
| :-------------------------------------------------------- | :--------------------------------------------------------------------- |
| Inline elements occupy only sufficient width required     | Block elements occupy the full width irrespective of their sufficiency |
| Inline elements don't start in a new line                 | Block elements always start in a line                                  |
| Inline elements allow other inline elements to sit behind | Block elements doesn't allow other elements to sit behind              |
| Inline elements don't have top and bottom margin          | Block elements have top and bottom margin.                             |

|                                                                                           Block                                                                                           |                                                                      Inline                                                                       |
| :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------: |
| `<div>`, `<p>`, `<h1>-<h6>`, `<ul>`, `<ol>`, `<li>`, `<table>`, `<form>`, `<header>`, `<footer>`, `<section>`, `<nav>`, `<article>`, `<aside>`, `<main>`, `<blockquote>`, `<hr>`, `<pre>` | `<span>`, `<a>`, `<img>`, `<button>`, `<input>`, `<label>`, `<small>`, `<strong>`, `<em>`, `<mark>`, `<line>`, `<ins>`, `<del>`, `<sub>`, `<sup>` |

---

## Line Breaks, Horizontal Rules & Entities

- `<br />` line break ( don't use this use CSS )
- `<hr />` give horizontal line ( don't use this use border property to set this)
- `<pre>` this will preserve the content format
- `<code>` to write the code

### HTML Entities

- `&gt;` for >
- `&lt;` for <
- `&quot;` for "
- `&apos;` for '
- `&nbsp;` for Non-breaking space
- `&copy;` for &copy;
- `&reg;` for &reg;
- `&trade;` for &trade;
- `&deg;` for > &deg;

## div and span

```html
<div>
  <h3>Content Title</h3>
  <p>This is my content</p>
  <a href="#">Link</a>
</div>
```

- Generic containers for content
- **divs** are `block-level` & **span** are `inline`
- Used with **classes** and **ids**

## Classes & IDs

- `class` is an attribute `can` be **repeated**
- `id` is an attribute `can't` be **repeated** in same page
- `id` can be used for links

## Sematic Elements

- `<header>` Header of the layout
- `<footer>` Footer of the layout
- `<nav>` Navigation area
- `<main>` The main content area
- `<article>` Publication area
- `<section>` Grouped area
- `<aside>` sidebar/secondary content

Why these are called **semantic** tags?  
Ans : Because they describe the content that they contain `<h1>` `<p>` is also semantic tag.

[Check out html semantic tags](/FrontEnd%20Basic/HTML%20and%20CSS/sandbox-starter/html-sandbox-starter/01-essential-html/10-semantic-elements/index.html)

## Emmet Crash Course

[Cheat Sheet](https://docs.emmet.io/cheat-sheet/)

## Keyboard Shortcuts

- `ctrl` + `shift` + `p` command pallet
- `ctrl` + `` ` ``
