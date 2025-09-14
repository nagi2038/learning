# BOX MODELING AND POSITIONING

- [BOX MODELING AND POSITIONING](#box-modeling-and-positioning)
  - [Section Intro](#section-intro)
  - [Box Model](#box-model)
    - [Box Model Properties](#box-model-properties)
  - [Sizing and Overflow](#sizing-and-overflow)
  - [Padding](#padding)
  - [Margin](#margin)
  - [Universal Selector \& Reset](#universal-selector--reset)
  - [Border](#border)
  - [Display property](#display-property)
  - [Position Property](#position-property)
  - [Box Shadow](#box-shadow)

## Section Intro

- What is the Box Model?
- Height, Width & overflow
- Margin, Padding & Border
- Resetting Styles
- Positioning
- Box Shadows
- Border Radius
- Mini Projects

## Box Model

- Content - Text, images, etc
- Padding - Space between content and border
- Border - Separates the padding & margin
- Margin - Space outside of border

### Box Model Properties

- Width & height, max-width, max-height, min-width, min-height
- padding, padding-top, padding-right, padding-bottom, padding-left
- border, border-style, border-color, border-width
- margin, margin-top, margin-right, margin-bottom, margin-left.
- box-sizing

## Sizing and Overflow

When content over flow we can add codition to the text.

```css
.overflow-text{
  overflow: scroll;
  overflow-y: scroll;
  overflow-x: hidden;
}
```

## Padding

`padding: 20px 40px 12px 45px;`

padding : top right bottom left

`padding : 20px 30px 40px`

padding : top right & left bottom

`padding: 20px 40px;`

padding : top & bottom  , right  & left

`padding : 20px`

padding : top & bottom & right & left

## Margin

- space outside the border
- we can do negetive margin too.

What is auto margin?

- set the margin equally on both side make the element to center.

```css
.box-1 {
  margin: 100px auto;
    /* T-R-B-L */
  margin: 20px 30px 40px 50px;
}
```

## Universal Selector & Reset

- `*` is an universal selector.
- box-sizing :  `content-box` have no effect on max-width, and`border-box` make sure does not coross max-width ;

```css
*{
  margin : 0;
}
```

## Border

border is  element outter bound part

```css
.box{
  /* short hand */
  border: 2px solid black;

  border-width: 2px;
  border-style: solid;
  border-color: red;
}
```

- with out `border-width` `border-color` `border-style` makes no sence

```css

.box-1 {
  border: none;
  border-top: 4px solid blue;
  border-bottom: 2px solid green;
}

.box-2 {
  border-radius: 10px;
}

.box-3 {
  border-top-left-radius: 50px;
  border-bottom-right-radius: 50px;
}
```

## Display property

- none
- block
- inline
- inline-block
- flex
- grid
- table
- table-row
- table-cell
- list-item
- inherit
- initial

```css
.none-el {
  display: none;
}

.hidden-el {
  visibility: hidden;
}

p {
  background-color: lightblue;
  display: block;
}

a {
  background-color: lightcoral;
  display: inline-block;
  width: 60px;
  height: 60px;
  text-align: center;
  vertical-align: middle;
}
```

## Position Property

- static - Default value
- relative
- absolute - can be a child of relative
- fixed - fixed on the page
- sticky - fixed + relative

**_STATIC_**

if `postion` is **_static_** we can't use `top` `left` `right` `bottom` attributes.

**_RELATIVE_**

if `postion` is **_relative_** we can use `top` `left` `right` `bottom` attributes.

**_FIXED_**

if `postion` is **_fixed_** we can use `top` `left` `right` `bottom` attributes.

**_sticky_**

if `postion` is **_sticky_** we can use `top` `left` `right` `bottom` attributes.

```css
.box1 {
  position: static; /* by default it is static */
  left: 10px;
}

.box2 {
  position: relative;
  left: 30px;
  top: 20px;
}

.box3 {
  position: fixed;
  right: 5px;
  z-index : 2;
}

.box4 {
  position: sticky;
  top: 5px;
}

.box5 {
  position: relative;
  width: 400px;
  height: 400px;
  background-color: lightcoral;
}

.box6 {
  position: absolute;
  bottom: 20px;
  right: 20px;
}
```

- fixed element by defaults goes to behind of relative element
- `z-index`  can be used to move the element in z direction.
- `z-index` do not work on `static` element
- `z-index` can be negative also.

## Box Shadow

```css
.shadow{
  box-shadow : 5px 6px 8px 6px #000
  /* Horizontal offset, vertical offset, blur radius, spread radius, Color */
}
```

- Horizontal & Vertical Offset - How far from the element each way
- Blur Radius ( Optional ) - How Blury the shadow is
- Spread Radius ( optional ) - How much the shadow should grow or shrink

```css

.box-1 {
  box-shadow: -10px -10px 10px 2px rgb(230, 191, 36);
}

.box-2 {
  box-shadow: 5px 5px 10px 2px black;
}

.box-3 {
  box-shadow:
    5px 5px 10px 2px black,
    -5px -5px 10px 2px red;
}
```
