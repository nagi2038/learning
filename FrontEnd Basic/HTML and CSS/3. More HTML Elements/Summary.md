# MORE HTML ELEMENTS

- [MORE HTML ELEMENTS](#more-html-elements)
  - [Audio Element](#audio-element)
  - [VIDEO ELEMENT](#video-element)
  - [Image Map](#image-map)
  - [Tables](#tables)
  - [Iframe embed object Eelemnt](#iframe-embed-object-eelemnt)
  - [Global Attributes](#global-attributes)
  - [SVG( Scalable Vector Graphics )](#svg-scalable-vector-graphics-)
  - [Popover \& Details](#popover--details)
  - [Progress \& Meter](#progress--meter)

**_Section Intro_**

- Audio & Video
- Image Map
- Tables
- Iframe
- Global Attributes
- SVG Elements
- Proover & Details
- Progress & Meter

## Audio Element

```html
<audio src="./song1.mp3" type="audio/mp3" controls></audio>
```

**_FallBack_**

```html
<audio controls>
  <source src="./song1.mp3" type="audio/mp3" />
  <!-- Fallback if audio do not support -->
  <p>Your Browser does not support the audio element</p>
</audio>
```

**_AUTOPLAY_**

```html
<audio controls autoplay>
  <source src="./song1.mp3" type="audio/mp3" />
  <!-- Fallback if audio do not support -->
  <p>Your Browser does not support the audio element</p>
</audio>
```

```html
<audio src="./song1.mp3" type="audio/mp3" controls autoplay></audio>
```

**_LOOP THE SONG_**

```html
<audio controls autoplay loop>
  <source src="./song1.mp3" type="audio/mp3" />
  <!-- Fallback if audio do not support -->
  <p>Your Browser does not support the audio element</p>
</audio>
```

| Attribute | Description                              |
| :-------- | :--------------------------------------- |
| controls  | show the control to the screen           |
| autopaly  | paly the audio once site is opened       |
| loop      | loop the audio                           |
| muted     | audio will be muted we can unmute        |
| type      | type value changes based on video format |

- we can have `fallback` text when audio is not supported.

## VIDEO ELEMENT

```html
<video
  src="./video1.mov"
  type="video/quicktime"
  controls
  muted
  autoplay
  loop
></video>
```

| Attribute | Description                              |
| :-------- | :--------------------------------------- |
| controls  | show the control to the screen           |
| autopaly  | paly the audio once site is opened       |
| loop      | loop the audio                           |
| muted     | audio will be muted we can't unmute      |
| type      | type value changes based on video format |

## Image Map

- click able part of image to navigate or do some action.

```html
<img src="./computer.jpg" alt="computer" usemap="#computermap" />
<map name="computermap">
  <area
    shape="rect"
    coords="34,44,270,350"
    href="computer.html"
    alt="Computer"
  />
  <area shape="rect" coords="290,172,333,250" href="phone.html" alt="Phone" />
  <area shape="circle" coords="337,300,45" href="coffe.html" alt="Coffe" />
  <area shape="default" coords="" href="other.html" alt="Other" />
</map>
```

| Attribute | Description                    |
| :-------- | :----------------------------- |
| shape     | rect, circle, polygon, default |
| coords    | Coords change based on shape   |

- if `shape` attribute value is `default` what ever area which not mapped will be mapped under default.

## Tables

Used for tabluar data

| Tags       | Description                                                                        |
| :--------- | :--------------------------------------------------------------------------------- |
| `table`    | main tag to create a table                                                         |
| `thead`    | where heading of the table is stored                                               |
| `tbody`    | where more data is stored                                                          |
| `tr`       | to create table row                                                                |
| `td`       | to store cell value/table data                                                     |
| `th`       | table head cell value/ table head value                                            |
| `colgroup` | to change the properties of the column                                             |
| `col`      | to apply the properties if it is child of `colgroup` and **grandchild** of `table` |

| Attribute | Description                                                  |
| :-------- | :----------------------------------------------------------- |
| colspan   | default colspan is 1 we can change to other positive numbers |
| rowspan   | default rowspan is 1 we can change to other positive numbers |

```html
<colgroup>
  <col />
  <col span="2" style="background-color: lightgreen" />
  <col style="background-color: lightgrey" />
</colgroup>
```

## Iframe embed object Eelemnt

- Used to embad another html document with in current html.

Below are the examples

**_WEB PAGE_**

```html
<iframe src="https://developer.mozilla.org/en-US/" frameborder="0"></iframe>
```

**_LOCAL WEBPAGE_**

```html
<iframe src="./test.html" frameborder="3"></iframe>
```

**_EMBED YOUTUBE_**

```html
<iframe
  src="https://www.youtube.com/embed/xjMP0hspNLE"
  frameborder="0"
  width="450"
  height="250"
></iframe>
```

**_EMBED PDF_**

```html
<iframe
  src="./invoicesample.pdf"
  frameborder="0"
  height="350"
  width="300"
></iframe>
```

**_EMBED GOOGLE MAPS_**

```html
<iframe
  src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d7654.155170758068!2d80.21320689489394!3d16.420885578487795!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3a35843923d6f96f%3A0xdafe3fe58432f617!2sGudipudi%2C%20Andhra%20Pradesh%20522402!5e0!3m2!1sen!2sin!4v1755158041079!5m2!1sen!2sin"
  width="250"
  height="250"
  style="border: 0"
  allowfullscreen=""
  loading="lazy"
  referrerpolicy="no-referrer-when-downgrade"
></iframe>
```

**_EMBED TAG_**

```html
<embed
  src="https://www.youtube.com/embed/xjMP0hspNLE"
  width="350"
  height="200"
/>
```

**_OBJECT TAG_**

```html
<object
  data="https://www.youtube.com/embed/xjMP0hspNLE"
  width="350"
  height="200"
></object>
```

## Global Attributes

- `class`

```html
<h2 class="class">Class is an global value</h2>
```

- `id`

```html
<h2 id="id">Id is a global value</h2>
```

- `style` - to style the elements

```html
<h2 style="background-color: red">Style is a global value</h2>
```

- `accesskey` - keyboard control keys

```html
<button
  accesskey="h"
  onclick="alert('you have clicked')"
  title="alt+h key board shortcut"
></button>
```

- `title` - general used a tooltip

```html
<button
  accesskey="h"
  onclick="alert('you have clicked')"
  title="alt+h key board shortcut"
>
  SUBMIT
</button>
```

- `hidden` - to hide the element

```html
<div hidden>This is a hidden element</div>
```

- `tabindex` - on clicking tab key foucs changes based on the index

```html
<button tabindex="1">Button 1</button>
<button tabindex="4">Button 4</button>
<button tabindex="3">Button 3</button>
<button tabindex="2">Button 2</button>
```

- `contenteditable` - make element content editable

```html
<div contenteditable="true">This is an editable div element</div>
```

- `dragable` - make element dragable
-

```html
<div draggable="true">This is dragable element</div>
```

- `autofocus` - after page old cursor will focus on to the element

```html
<input type="number" name="number" id="number" autofocus />
```

## SVG( Scalable Vector Graphics )

[blobmaker](https://www.blobmaker.app/)

- even after resize the quality doesn't change unlike images.

```html
<svg width="300" height="300">
  <circle cx="70" cy="70" r="80" fill="blue" stroke="black" stroke-width="5" />
  <text x="35" y="80" font-size="40" font-family="Verdana" fill="white">
    SVG
  </text>
</svg>
```

## Popover & Details

- popover is like a toogle button for popup

```html
<button popovertarget="popover-1">Open PopOver1</button>
<div popover id="popover-1">This is popover -1</div>
```

- Details tag can be used for FAQs

```html
<details>
  <summary>Details</summary>
  Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, ad quis!
  Esse fugit molestias perferendis eius veniam asperiores nihil eligendi
  quibusdam reprehenderit voluptates voluptatem numquam qui, repudiandae,
  repellat id eum!
</details>
```

## Progress & Meter

```html
<label for="file">File Progress : </label>
<progress id="file" max="100" value="90">50%</progress>
```

- Emtpy progress tag acts like a loading bar

```html
<progress></progress>
```

- METER

```html
<label for="fuel">Fuel:</label>
<meter
  value="80"
  id="fuel"
  min="0"
  max="100"
  low="30"
  high="90"
  optimal="80"
></meter>
```
