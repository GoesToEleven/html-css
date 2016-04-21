## Flexbox
### Containers, Properties, and Items
Summary: With the addition of `display:flex;` introduced with CSS3 layout behavior has become much easier to accomplish. 

In this lesson we will cover much of the basics involving flexbox and their interior items. There is a code demo at the bottom. For more precise information involving this topic, I recommend reading through the sources.

1. **Flex Container**
    ```css
    .flex-container {
        display: flex;
    }
    ```
  We begin with the root of flexbox's functionality, the flex container. Before any other options can be defined, we need to let our container know that it should act as a flexbox; thus, `display:flex;`.

  The container that has this property, and all children, are now flex objects.

1. **Flex Wrap**
    ```css
    .wrap {
        display: flex;
        flex-wrap: wrap | nowrap | wrap-reverse;
    }
    ```
  Of the most useful flexbox properties is the one it achieved it's name for: flex.

  `flex-wrap: wrap;` informs the container with this property that it should now arrange it's children according to an axis(more details in the next section) and now, in the case of overlap, elements will _wrap_ around the screen.

  `flex-wrap: wrap-reverse;` will do as the label claims and organizes the children in reverse order.

  `flex-wrap: nowrap;` will explicitly disable wrap properties. *This is the default behavior of a container*

1. **Flex Axis**
    ```css
    .flex-container {
        display: flex;
        flex-direction: row | column | row-reversed | column-reversed;
    }
    ```
  We mentioned the concept of axis to align children of a flex container. There are several different ways of doing this and each have their own specific meaning.
  * `flex-direction`

    This specifies the 'main' axis. Specifically, this property defines the direction objects will flex into.
  * `justify-content`

    This is the next axis modifier. With this property we defile alignment _along_ the main axis. From here, we can distribute extra space evenly.
  * `align-items`

    Another layer down. This property will modify how objects are aligned across the main axis cross axis.

    Example: if you have your objects arranged in row format (left to right) this property defines where along an object's top to bottom it is positioned.
  * `align-content`

    This serves the same as `justify-content` for the cross axis. It will determine how extra space on the cross axis is distributed.

1. **Flex Items**

  There are a number of properties to target children of flex objects as well. These are just a few of them.

  * `order`

    This property will accept an integer to determine what order this element will appear at.
  * `flex-grow`/`flex-shrink`

    These defines how much a single element will resize in relation to other siblings.
  * `align-self`

    This will override the parent's alignment.

### Code Example: Flexbox

Place this code into a .html file and open it in your browser.

Look for these things when editing the div of "Edit_My_Class":
* When the class is only "container":

    Notice how the elements flow down the page. This is the default behavior of HTML
* Class is "container flex"
    
    Here we can see that row is the default flex layout. Notice that the objects attempt to squish into a singular row?
* Class is "container flex row"
    
    Was there a difference? Why?
* .. "container flex col"
    
    Look at the css for class of col, why do you think it requires a different height?
* .. "container flex row-" and "container flex col-"

    These are reversed row and reversed column.
* add "wrap" to the classes previously used(reversed and not)
* change wrap to "wrap-"
    
    This is reversed wrap, what kind of changes do you see with row, col, row-, and col-?

```html
<!DOCTYPE html>
<html>
<head>
  <title>Lesson Title</title>
  <style type="text/css">
    /*Helpers*/
    * {
      box-sizing: border-box;
    }
    .item {
      width: 100px;
      height: 100px;
      margin: 2px;
      border: 1px solid rgb(165, 162, 52);
      background-color: rgb(81, 79, 0);: 
    }
    .container {
      position: relative;
      width: 100%;
      height: 100%;
      background-color: rgb(16, 7, 56);
      border: 1px solid rgb(58, 45, 114);
      padding: 10px;
    }
    body {
      background-color: rgb(20,20,20);
      color: white;
      padding-left: 50px;
    }
    /*Container Properties*/
    .flex{
      display: flex;
    }
    .row {
      flex-direction: row;
    }
    .row- {
      flex-direction: row-reverse;
    }
    .col {
      /* Q: Why must I limit the height when applying a column layout, but not a row layout?*/
      flex-direction: column;
      height: 500px;
    }
    .col- {
      flex-direction: column-reverse;
      height: 500px;
    }
    .wrap {
      flex-wrap: wrap;
    }
    .wrap- {
      flex-wrap: wrap-reverse;
    }
    /*Item Properties*/
    .important {
      border-color: red;
      background-color: darkred;
      flex-grow: 2;
    }
  </style>
</head>
<body>
<!-- Change this container div's class to a few of the properties above. -->
<div id="Edit_My_Class" class="container">
  <!-- Give a few of us the class of "item important" -->
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
  <div class="item">4</div>
  <div class="item">5</div>
  <div class="item">6</div>
  <div class="item">7</div>
  <div class="item">8</div>
  <div class="item">9</div>
  <div class="item">10</div>
  <div class="item">11</div>
  <div class="item">12</div>
</div>
</body>
</html>
```

* sources: 
 * https://css-tricks.com/snippets/css/a-guide-to-flexbox/
 * http://www.w3schools.com/css/css3_flexbox.asp
* <small>Created by Allen J. Mills,[(Github)](https://github.com/FelixVicis) (4/14/16)<small>


