## CSS Basics
### Selectors
Summary: CSS is a language used to enrich standard HTML by adding _style!_

Selectors are the backbone of everything you will do with CSS. With this lesson, you will be able to select exactly what you want within an html page and nothing else.

## Basic Selectors

1. **All**
  ```css
    * {}
  ```
  The above selector(*) will select for every element on the screen. Use this for global effects.

1. **Elements**
  ```css
    element {}
    element, anotherElement {}
  ```

  This is the most basic of selectors, the element selector.

  This will select all elements of a specific kind; eg: `div {}` will select all div elements on the screen.

  The second tag is a collection of elements to select. If you wish to select on both div _and_ p elements you would use `div, p {}`.

1. **Children Elements**
  ```css
    element childElement {}
    element > childElement {}
  ```
  We begin to complicate matters slightly. These are the children/parent selectors. For example, if we wish to get all divs directly within body we would select on: `body div {}`. This would give us only those elements and no others any farther within the page.

  To reverse this and select an input who has a parent of form you would select on `form>input {}`

1. **Sibling Elements**
  ```css
    element + siblingElement {}
    siblingElement ~ element {}
  ```
  Sibling elements are those that exist at the same level. For example:
  ```html
  <div>First</div>
  <p>Second</p>
  ```
  The div and p here are siblings of each other.

  If we wished to give style to the text of the p We would do either:
  ```css
  div + p {color: red;} /* Select the p after the div */
  ```
  or,
  ```css
  p ~ div {color: red;} /* Select the p who has a div as previous sibling */
  ```

### Code Example: Simple Selectors

Place this code into a .html file and open it in your browser.

Key Takeaways

```html
<!DOCTYPE html>
<html>
<head>
  <title>Lesson Title</title>
  <style type="text/css">
    /*Helpers*/
    * {
      /* For all elements, I wish to add a border. This includes html and body.*/
      box-sizing: border-box;
      border: 1px dotted white;
    }
    body {
      /* On body and below. */
      background-color: rgb(20,20,20);
      color: white;
      border-color: orange;
      height: 70vh;
    }
    div {
      /* Selecting all divs and below*/
      position: relative;
      width: 80%;
      margin: 10px;

      border-color: lightblue;
      font-size: 1.3em;
    }
    div p {
      /* Selecting only a p that is a child of div */
      border-color: red;
      color: green;
      background-color: rgba(255,0,0,0.2);
      font-size: initial;
    }

    p + div {
      /* Selecting only a div that is a sibling of p.

         Note: This does not select the parent div as it has no sibling of p;
      */
      background-color: rgba(0,255,0,0.2);
    }
  </style>
</head>
<body>
  Body Text
  <div>
    Parent Div Text
    <p>Child P Text</p>
    <div>Child Div Text</div>
  </div>

  
  <ol style="font-size: 1.1em;">
    <h3 style="border-bottom: 1px solid white;">
      Things to watch for:
    </h3>
    <li>CSS attached to an element above is also applied to children. This is why a text color set at body applies to everything except when it has been explicitly set.</li>
    <li>Using the examples above, can you change the text color of this ordered list?</li>
    <li>Sibling selectors are very interesting when applied to a list of items. Can you change the color of every list item here except the first? How about the last instead?</li>
  </ol>
</body>
</html>
```

------------------------------

## Specific Selectors

1. **ID**
  ```css
    #elementID {}
  ```
  ID's are given to html elements with with the form `<element id="elementID" />`. Using this as an identifying id for _one_ element, you can target a specific element for style.

1. **Class**
  ```css
    .className {}
  ```
  Classes, on the other hand, are added to an element with `<element class="className" />`
  These identifiers are designed for _groups_ of elements and are often added in bulk where separate class names are separated by space.

  Depending on your specific style, classes are often used to create optional styles for elements. An example of this could be:
  ```css
  table {}
  table.Dark {}
  table.Light {}
  ```
  Where the styling on a table of class Dark would be different than the same having class Light or even no class.

### Code Example: Specific Selectors

Place this code into a .html file and open it in your browser.

Specific selectors are excellent when targeting singular objects.

* Did you notice that the first div had both boxify and px100 class. Add the missing class to both SecondDiv and ThirdDiv to make both square and a white border.
* Can you create a new class px500 using px100 as an example.
* Add this new class px500 to replace px100 on ThirdDiv
* Can you target SecondDiv using it's id to make the border color and font color green. <br><small>Hint: use FirstDiv as an example.</small>

```html
<!DOCTYPE html>
<html>
<head>
  <title>Specific Selectors</title>
  <style type="text/css">
    /*Helpers*/
    body {
      background-color: rgb(20,20,20);
      color: white;
      height: 70vh;
    }
    div {
      position: relative;
    }
    /* Classes  ---- */
    .boxify {
      box-sizing: border-box;
      border: 1px dotted white;
    }
    .px100 {
      width: 100px;
      height: 100px;
    }
    /* ID's  ---- */
    #FirstDiv {
      color: red;
      border-color: red;
    }
  </style>
</head>
<body>
  <div id="FirstDiv" class="boxify px100">First Div</div>
  <div id="SecondDiv" class="boxify px100">Second Div</div>
  <div id="ThirdDiv" class="boxify px100">Third Div</div>
</body>
</html>
```
------------------------------

## Special Selectors

This section will be among the most complicated selectors available to use. With these selectors CSS can have tremendous power over your webpage.

1. **Attribute**
  ```css
    *[attribute] {},
    *[attribute=valueExact] {},
    *[[attribute~=valueContaining] {},
    *[attribute^=valuePrefix] {},
    *[attribute$=valuePostfix] {},
    *[attribute*=valueInfix] {},
  ```

  Attribute selectors will allow you to select on all of the other options not previously discussed for an element. For example: 

  Links on a page often have several attributes tied to them such as href, target, and title among others. With these selectors, you could treat all links that have, for example, `target:_blank` with a special format.

1. **Pseudo**
  ```css
    :link {},
    :visited {},
    :focus {},
    :hover {},
    <!-- And Many More! -->
  ```

  Pseudo selectors are similar to javascript events. This allows for very specialised styles to apply to elements.

### Code Example: Special Selectors

Place this code into a .html file and open it in your browser.

* Notice, we're getting rather abstract at this level.
* Of the attributes, did you notice that you do not need to use _real_ attributes. You may make your own.
* Events, and especially selecting on then, can get difficult. Can you answer why the selector including hover ends with `*[show]`?

```html
<!DOCTYPE html>
<html>
<head>
  <title>Special Selectors</title>
  <style type="text/css">
    /*Helpers*/
    * {
      box-sizing: border-box;
    }
    body {
      background-color: rgb(20,20,20);
      color: white;
      height: 70vh;
    }
    /* Attributes */
    *[show="No"] {
      /* Objects with attribute of show equal to No */
      display: none;
    }
    *[extend] {
      /* Selecting on Objects with an attribute of extend. */
      position: relative;
      top: 0px;
      left: 0px;
      right: 0px;
      height: 10%;
      margin-bottom: 50px;
    }
    /* Events */
    *:focus {
      /* Any element that has access to the event Focus. */
      background-color: yellow;
    }
    *[extend]:hover *[show] {
      /* For an object with attribute extend, On event hover, change the child with attribute show. */
      display: block;
      color: red;
    }
  </style>
</head>
<body>
<div extend>
  <div show="Yes">Hover over me!</div>
  <div show="No">Hello World!</div>
</nav>
<br />
<content>
  <input value="Click On Me!" />
</content>
</body>
</html>
```

* sources: 
 * http://www.w3schools.com/cssref/css_selectors.asp
* <small>Created by Allen J. Mills,[(Github)](https://github.com/FelixVicis) (4/27/16)<small>