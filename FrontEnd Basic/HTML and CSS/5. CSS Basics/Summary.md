# CSS Basic

- [CSS Basic](#css-basic)
  - [Implementing CSS](#implementing-css)
    - [Inline CSS](#inline-css)
    - [Internal CSS](#internal-css)
    - [External CSS](#external-css)
  - [CSS Selector Syntax](#css-selector-syntax)
    - [Type selector](#type-selector)
    - [Class Selector](#class-selector)
    - [ID Selector](#id-selector)
    - [Descendants](#descendants)
    - [Inheritance](#inheritance)
  - [Fonts in CSS](#fonts-in-css)
    - [System/Web Safe Fonts](#systemweb-safe-fonts)
    - [Web Fonts](#web-fonts)
  - [Font \&  Text Properties](#font---text-properties)
    - [font-size](#font-size)
    - [font weight](#font-weight)
    - [font style](#font-style)
    - [font variant](#font-variant)
    - [All fonts can be used in one property](#all-fonts-can-be-used-in-one-property)
    - [text-decoration](#text-decoration)
    - [text-transform](#text-transform)
    - [letter-spacing](#letter-spacing)
    - [text-indent](#text-indent)
    - [word-spacing](#word-spacing)
    - [text-align](#text-align)
    - [line-height](#line-height)
  - [Colors ( Color Name, HEX, RGB, HSL )](#colors--color-name-hex-rgb-hsl-)
    - [color Names](#color-names)
    - [Hexidecimal Values](#hexidecimal-values)
    - [RGB Values](#rgb-values)
    - [HSL Values](#hsl-values)
  - [Specificity](#specificity)
  - [Backgrounds](#backgrounds)
    - [Linear gradient](#linear-gradient)
  - [Styling links](#styling-links)

**_SECTION INTRO_**

- Implementing CSS
- Basic Selectors
- Fonts, Text Properties
- Colors
- CSS Specificity
- Backgrounds
- Styling Link States
- Font Awesome

## Implementing CSS

- ❌ Inline CSS - Add CSS to the HTML tag
- ❌ Internal CSS - Add CSS within `style` tags
- ✅ External CSS - CSS in it's own file

```css
.selector {
  property1: value1;
  property2: value2;
}
```

### Inline CSS

- Affects only single tag element
- Generally Not recommended, since it is limited to particular tag only.

```html
<h1 style="color: blue; font-size: 50px">
  HTML & CSS Sandbox - Implementing CSS
</h1>
<p style="color:red; text-decoration: underline;">This is a paragraph</p>
<p>This paragraph is not affect because above line</p>
```

### Internal CSS

- Affects all the elements of the DOM(Document Object Model)
- This is also not recommended type of style since it is limited to html file only

```html
<head>
  <style>
    h1 {
      color: blue;
      font-size: 50px;
    }
    p {
      color: rgb(255, 85, 0);
    }
  </style>
</head>
```

### External CSS

- Create a file with extension `.css`
- It is a best practice since we can link same style sheet to multiple elements using `link` tag.

```html
<link rel="stylesheet" href="./style.css" />
```

## CSS Selector Syntax

- Type Selectors
- Class Selectors ( best practice to use for styling )
- ID Selectors
- Descendants
- html, body & Selector
- Multiple Selectors

### Type selector

- using actual element (`h1`..`h5`, `p`....) as selector

```html
<style>
  h1 {
    color: red;
  }
</style>
```

### Class Selector

```html
<!-- index.html -->
<div>
  <h2 class="formal">Keep It Formal</h2>
  <p>Clothing to keep you looking sharp</p>
  <a href="#">View collections</a>
</div>
```

```css
/* style.css */
.formal {
  color: brown;
}
```

### ID Selector

- Generally IDs are not used for styling
- IDs are used for input and label tags, referencing the element

```html
<!-- index.html -->
<div id="container">
  <div>This is new line</div>
</div>
```

```css
/* style.css */
#container {
  color: red;
}
```

```css
/* style.css - Multiple elements style*/
#container, div {
  color: red;
}
```

### Descendants

- There is specificity while handling with descendent
- [Learn more about specificity](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_cascade/Specificity)
- Id : 1-0-0
- Class : 0-1-0
- Type : 0-0-1
- No value : 0-0-0 `(*)` and `pseudo-class`
- Cominators :
  - `+` : [next sibling](https://developer.mozilla.org/en-US/docs/Web/CSS/Next-sibling_combinator)
  - `>` : [Child Combinator](https://developer.mozilla.org/en-US/docs/Web/CSS/Child_combinator)
  - `~` : [Subsequent-sibling combinator](https://developer.mozilla.org/en-US/docs/Web/CSS/Subsequent-sibling_combinator)
  - `<space>` : [Descendant combinator](https://developer.mozilla.org/en-US/docs/Web/CSS/Descendant_combinator)
  - `||` : [Column combinator](https://developer.mozilla.org/en-US/docs/Web/CSS/Column_combinator)
- Not every thing is inheritable

### Inheritance

```css
body {
    font-family: Arial, Helvetica, sans-serif; /* Inheritable */
    border: 1px solid black; /* can't be inherited */
}
```

## Fonts in CSS

### System/Web Safe Fonts

- Arial (sans-serif)
- Verdana (sans-serif)
- Tahoma (sans-serif)
- Terbuchet (sans-serif)
- Time New Roman (serif)
- Georgia (serif)
- Garamond (serif)
- Courier New (monospace)
- Brush Script (cursive)

What is the difference between sans-serif and serif

| Serif                   | Sans-serif                     |
| :---------------------- | :----------------------------- |
| They have edge extended | They don't have extended edges |

### Web Fonts

Need to be imported into a project using a **_@font-face_** rule or a service like a **_Google Fonts_**

can be imported to the HTML file using `<link>` or the CSS file using `@import`

## Font &  Text Properties

- font-family
- font-size
- font-weight
- font-style
- font-variant
- line-height
- letter-spacing
- word-spacing
- text-align
- text-decoration
- text-transform
- text-indent

### font-size

[font size](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size)

```css
/* <absolute-size> values */
font-size: xx-small;
font-size: x-small;
font-size: small;
font-size: medium;
font-size: large;
font-size: x-large;
font-size: xx-large;
font-size: xxx-large;

/* <relative-size> values */
font-size: smaller;
font-size: larger;

/* <length> values */
font-size: 12px;
font-size: 0.8em;

/* <percentage> values */
font-size: 80%;

/* math value */
font-size: math;

/* Global values */
font-size: inherit;
font-size: initial;
font-size: revert;
font-size: revert-layer;
font-size: unset;
```

### font weight

[font weight](https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight)

```css
/* <font-weight-absolute> keyword values */
font-weight: normal;
font-weight: bold;

/* <font-weight-absolute> numeric values [1,1000] */
font-weight: 100;
font-weight: 200;
font-weight: 300;
font-weight: 400; /* normal */
font-weight: 500;
font-weight: 600;
font-weight: 700; /* bold */
font-weight: 800;
font-weight: 900;

/* Keyword values relative to the parent */
font-weight: lighter;
font-weight: bolder;

/* Global values */
font-weight: inherit;
font-weight: initial;
font-weight: revert;
font-weight: revert-layer;
font-weight: unset;
```

### font style

[font sytle](https://developer.mozilla.org/en-US/docs/Web/CSS/font-style)

```css
font-style: normal;
font-style: italic;
font-style: oblique;
font-style: oblique 10deg;

/* Global values */
font-style: inherit;
font-style: initial;
font-style: revert;
font-style: revert-layer;
font-style: unset;
```

### font variant

[font variant](https://developer.mozilla.org/en-US/docs/Web/CSS/font-variant)

```css
font-variant: small-caps;
font-variant: common-ligatures small-caps;

/* Global values */
font-variant: inherit;
font-variant: initial;
font-variant: revert;
font-variant: revert-layer;
font-variant: unset;
```

### All fonts can be used in one property

```css
/* font-size font-family */
font: 1.2em "Fira Sans", sans-serif;

/* font-size/line height font-family */
font: 1.2em/2 "Fira Sans", sans-serif;

/* font-style font-weight font-size font-family */
font: italic bold 1.2em "Fira Sans", sans-serif;

/* font-stretch font-variant font-size font-family */
font: ultra-condensed small-caps 1.2em "Fira Sans", sans-serif;

/* system font */
font: caption;
```

- While using `font` => `font-size` and `font-family` are mandotery fields.
- `font-style`, `font-variant` and `font-weight` must precede `font-size`.
- `font-variant` may only specify the values defined in CSS 2.1, that is normal and small-caps.
- `font-stretch` may only be a single keyword value.
- `line-height` must immediately follow `font-size`, preceded by "/", like this: `16px/3`.
- `font-family` must be the last value specified.

### text-decoration

[text-decoration](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration) is short hand of :

- [text-decoration-line](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration-line)
- [text-decoration-color](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration-color)
- [text-decoration-style](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration-style)
- [text-decoration-thickness](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration-thickness)

```css
text-decoration: underline;
text-decoration: overline red;
text-decoration: none;

/* Global values */
text-decoration: inherit;
text-decoration: initial;
text-decoration: revert;
text-decoration: revert-layer;
text-decoration: unset;
```

### text-transform

[text-tranfrom](https://developer.mozilla.org/en-US/docs/Web/CSS/text-transform) property specifies how to capitalize an element's text. It can be used to make text appear in all-uppercase or all-lowercase, or with each word capitalized. It also can help improve legibility for ruby.

```css
/* Keyword values */
text-transform: none;
text-transform: capitalize;
text-transform: uppercase;
text-transform: lowercase;
text-transform: full-width;
text-transform: full-size-kana;
text-transform: math-auto;

/* Global values */
text-transform: inherit;
text-transform: initial;
text-transform: revert;
text-transform: revert-layer;
text-transform: unset;
```

### letter-spacing

[letter-spacing](https://developer.mozilla.org/en-US/docs/Web/CSS/letter-spacing) property sets the horizontal spacing behavior between text characters. This value is added to the natural spacing between characters while rendering the text. Positive values of letter-spacing causes characters to spread farther apart, while negative values of letter-spacing bring characters closer together.

```css
/* Keyword value */
letter-spacing: normal;

/* <length> values */
letter-spacing: 0.3em;
letter-spacing: 3px;
letter-spacing: -1px;

/* Global values */
letter-spacing: inherit;
letter-spacing: initial;
letter-spacing: revert;
letter-spacing: revert-layer;
letter-spacing: unset;
```

### text-indent

[text-indent](https://developer.mozilla.org/en-US/docs/Web/CSS/text-indent) property sets the length of empty space (indentation) that is put before lines of text in a block.

```css
/* <length> values */
text-indent: 3mm;
text-indent: 40px;

/* <percentage> value
   relative to the containing block width */
text-indent: 15%;

/* Keyword values */
text-indent: 5em each-line;
text-indent: 5em hanging;
text-indent: 5em hanging each-line;

/* Global values */
text-indent: inherit;
text-indent: initial;
text-indent: revert;
text-indent: revert-layer;
text-indent: unset;
```

### word-spacing

[word-spacing](https://developer.mozilla.org/en-US/docs/Web/CSS/word-spacing) property sets the length of space between words and between tags.

```css
/* Keyword value */
word-spacing: normal;

/* <length> values */
word-spacing: 3px;
word-spacing: -1px;

/* Global values */
word-spacing: inherit;
word-spacing: initial;
word-spacing: revert;
word-spacing: revert-layer;
word-spacing: unset;
```

### text-align

[text-align](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)

```css
/* Keyword values */
text-align: start;
text-align: end;
text-align: left;
text-align: right;
text-align: center;
text-align: justify;
text-align: match-parent;

/* Block alignment values (Non-standard syntax) */
text-align: -moz-center;
text-align: -webkit-center;

/* Global values */
text-align: inherit;
text-align: initial;
text-align: revert;
text-align: revert-layer;
text-align: unset;
```

### line-height

[line-heigh](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height)

```css
/* Keyword value */
line-height: normal;

/* Unitless values: use this number multiplied
by the element's font size */
line-height: 3.5;

/* <length> values */
line-height: 3em;

/* <percentage> values */
line-height: 34%;

/* Global values */
line-height: inherit;
line-height: initial;
line-height: revert;
line-height: revert-layer;
line-height: unset;
```

## Colors ( Color Name, HEX, RGB, HSL )

| colors           | small desc        |
| :--------------- | :---------------- |
| color            | Text Colors       |
| background-color | Background colors |
| border           | Border Colors     |
| outline          | Outline Colors    |
| box-shadow       | Box drop Shadows  |
| text-shadow      | Text Drop Shadows |
| fill             | SVG fill colors   |

### color Names

- red, blue, green, yellow, etc
- darkred, darkblue, darkgreen, etc
- lightred, lightblue,lightgreen, etc
- mediumred, mediumblue, mediumgreen, etc
- coral, chocolate, crimsom, khaki, etc

[color-names](https://htmlcolorcodes.com/color-names/)

### Hexidecimal Values

`#AA 39 39`
`#RED GREEN BLUE`

- Made up of 6 digits organizedin paris for RGB
- Range from `00` to `FF` where `00`  means no intensity and `FF` means max intenisty.
- Letters represent the intensity greater than 9. A represents 10, B->11 and so on.

### RGB Values

- Made up of 3 paris of digits from `0-255` -> `(0,0,0)=> black` `(255,255,255) => white`
- `0` means no intensity and `255` means max intensity.
- We can also use `rgba(0,0,0,0.5)` which include alpha (transparency)
- Transprency is useful for image overlays

### HSL Values

- Specify by hue, staturation, lightness
- Measured by degrees on a color wheel from `0` to `360`
- The lightness and staturation value range form `0%` to `100%`

`opcaity : 1;` this will effect entire class or element.

## Specificity

Specificity is an algorithm that **_calculate the weight_** that is applied to a given CSS declaration.

1. Inline CSS (Style attribute) - high specificity
2. ID #
3. Class .
4. Element

> Important > Inline > ID > Class > Element

- if the specifity is same most recent will be applied.
- `!important` will have high specificity than any other.
- Don't use `!important` very often unless it is required.

```css
h1 {
  color : red !important;
}
```

## Backgrounds

- `background-color`
- `background-image` repeats image by default.
- `background-repeat` set value to `no-repeat` image don't repeat
- `background-size` set value to `cover` will cover entire div/tag
- `background-postion` set value to `center` I'm will always reamins at center.

short hand for every thing : `background`

```css
background : url("./hero.jpg") no-repeat center/cover;
background-attachment: fixed;
```

### Linear gradient

```css
 /* Linear gradient */
background: linear-gradient(to bottom, lightblue, darkblue);
background: linear-gradient(to left, lightgreen, darkblue);
background: linear-gradient(to bottom left, lightgreen, darkblue);
```

## Styling links

| states     | description               |
| :--------- | :------------------------ |
| `a:link`   | Normal unvisted link      |
| `a:hover`  | Link when hovered         |
| `a:active` | Moment link is clicked    |
| `a:focus`  | Moment link recives focus |
| `a:visted` | Link user has visted      |

## Font awesome

[font awesome](https://fontawesome.com/)
