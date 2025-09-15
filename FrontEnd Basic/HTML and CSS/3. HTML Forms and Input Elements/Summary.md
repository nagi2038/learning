# HTML Forms and Input Elements

- [HTML Forms and Input Elements](#html-forms-and-input-elements)
  - [Section Intro](#section-intro)
  - [`<Form>` Elemet](#form-elemet)
    - [`<input>` Eelement Types](#input-eelement-types)
  - [Text-Based Input Tags](#text-based-input-tags)
  - [Input filed Atrributes](#input-filed-atrributes)
  - [Select Boxes \& Textarea](#select-boxes--textarea)
    - [Select Boxes](#select-boxes)
    - [Text area](#text-area)
  - [Check Boxes \& Radio Buttons](#check-boxes--radio-buttons)
    - [Check Boxes](#check-boxes)
    - [Radio buttons](#radio-buttons)
  - [Other Input Types](#other-input-types)
  - [Data List](#data-list)

## Section Intro

- Form Tag
- Input Tag
- Text-Based Inputs
- Input Field Attributes
- Select & Textarea
- Checkboxes & Radio
- Other Types
- DataList

## `<Form>` Elemet

```html
<form action="/api/process" method="POST">
  <input type="text" name="company" id="company" />
</form>
```

- HTML can only display forms, not process them
- They `<form>` tag needs to have `<input>` tags
- The action is the server-side endpoint and the methodis the **HTTP** method to use

### `<input>` Eelement Types

| element  | Description                                 |
| :------- | :------------------------------------------ |
| text     | single-line text field                      |
| email    | single line email                           |
| password | single line password with hidden characters |
| number   | single line numbers                         |
| textarea | Multi-line text field                       |
| select   | Dropdown list of options                    |
| date     | Date picker                                 |
| checkbox | Checkbox field with multiple options        |
| radio    | Radio boxes with single option              |
| file     | File Upload field                           |
| submit   | submit button                               |
| range    | slider input to select from a range         |
| color    | Color Picker                                |

## Text-Based Input Tags

- every form will have `input` tags along with their `label` tags
- In `label` tag we have `for` attribute that need to linked to `id` attribute in `input` tag
- such that when we click on **lable name** it will automatically point to **input field**
- submit button can be either `input` or `button` tag

## Input filed Atrributes

| Attribute   | Description                                         |
| :---------- | :-------------------------------------------------- |
| placeholder | shows text in input fields                          |
| value       | predefined value can set                            |
| name        | this is used for getting data on server side        |
| required    | make sure data is not empty                         |
| minlength   | make sure minimum char are entered                  |
| maxlength   | make sure not more than max char are entered        |
| disabled    | It will gray out and does allow to enter the value. |

- `placeholder` attribute can be used for password tho this mask the password
- `name` attribute set all key value as params in URL by default if don't mention `method` in `form`
- when you submitting sensitive data use `POST` method so value will not be shown in URL
- use `GET` for serach, filter such thing.

## Select Boxes & Textarea

### Select Boxes

```html
<label for="product">product</label><br />
<select name="product" id="product" multiple size="2">
  <option value="iphone">iPhone</option>
  <option value="imac" selected>iMac</option>
  <option value="ipad">iPad</option>
  <option value="macbook">Macbook</option>
  <option value="mackbook-pro">Mackbook Pro</option>
</select>
```

| Attribute | Description                                                                                             |
| :-------- | :------------------------------------------------------------------------------------------------------ |
| multiple  | we can select multiple value by holding `ctrl` key `<select name="product" id="product" multiple>`      |
| size      | when `multitple` attribute is set we can set window size/ no.of elements are visible with out scrolling |
| selected  | we can have predefined selected values `<option value="iphone" selected>iPhone</option>`                |

### Text area

Used to enter large text

| Attribute   | Description                          |
| :---------- | :----------------------------------- |
| placeholder | hint/shows text in input fields      |
| rows        | controll the height of the text area |
| cols        | controll the width of the text area  |

## Check Boxes & Radio Buttons

### Check Boxes

Used for selected multiple items.

```html
<form action="">
  <label for="item1">
    <input
      type="checkbox"
      name="language"
      id="item1"
      value="item1"
      checked
    />Item1
  </label>
  <label for="item2">
    <input type="checkbox" name="language" id="item2" value="item2" />Item2
  </label>
  <label for="item3">
    <input type="checkbox" name="language" id="item3" value="item3" />Item3
  </label>
  <label for="item4">
    <input type="checkbox" name="language" id="item4" value="item4" />Item4
  </label>
  <input type="submit" value="submit" />
</form>
```

| Attribute | Description                   |
| :-------- | :---------------------------- |
| checked   | by defautl it will be checked |
| disabled  | we can't edit the checkbox    |

### Radio buttons

At max only one can be selected

```html
<form>
  <label for="small">
    <input type="radio" name="size" id="small" value="small" /> SMALL
  </label>
  <label for="medium">
    <input type="radio" name="size" id="medium" value="medium" /> MEDIUM
  </label>
  <label for="large">
    <input type="radio" name="size" id="large" value="large" /> LARGE
  </label>
  <input type="submit" value="submit" />
</form>
```

| Attribute | Description                                                                                     |
| :-------- | :---------------------------------------------------------------------------------------------- |
| checked   | by defautl it will be checked                                                                   |
| disabled  | we can't edit the raido button ( be care full disable all the radio button if required not one) |

## Other Input Types

**_COLOR_**

```html
<div>
  <label for="color">color</label>
  <input type="color" name="color" id="color" />
</div>
```

**_DATE_**

```html
<div>
  <label for="date">Date</label>
  <input type="date" name="date" id="date" value="2025-08-12" />
</div>
```

**_TIME_**

```html
<div>
  <label for="time">Time</label>
  <input type="time" name="time" id="time" />
</div>
```

**_WEEK_**

```html
<div>
  <label for="week">Week</label>
  <input type="week" name="week" id="week" />
</div>
```

**_MONTH_**

```html
<div>
  <label for="month">Month</label>
  <input type="month" name="month" id="month" />
</div>
```

**_RANGE_**

```html
<div>
  <label for="range">Range</label>
  <input type="range" name="range" id="range" min="0" max="100" step="10" />
</div>
```

**_URL_**

```html
<div>
  <label for="url">URL</label>
  <input type="url" name="url" id="url" />
</div>
```

## Data List

It contains option + text Input

```html
<input list="language" id="fav-language" name="favLanguage" />
<datalist id="language">
  <option value="item1"></option>
  <option value="item2"></option>
  <option value="item3"></option>
  <option value="item4"></option>
  <option value="item5"></option>
</datalist>
```
