## Position Layout
### Static and Relative
Summary: Using the `position:<kind>;` property, you may specify the type of positioning/method used on an element.

In this lesson, we will focus on the position properties of *static* and *relative* specifically. There will be a code demo at the bottom.

1. **Static**
    ```css
    .static-me {
        position: static;
        border: 3px solid black;
    }
    ```
  An object positioned as static will explicitly follow the flow of the webpage, top down. It will not be affected by any top/down/left/right properties. You can use this to specifically isolate an object from the behavior of other objects.

2. **Relative**
    ```css
    .relative-me {
        position: relative;
        left: 10 px;
        border: 3px solid black;    
    }
    ```
  Relatively positioned objects will position themselves relative to their neighboring parents. As you can imagine; a div within body will position itself relative of the page, a picture within the div will do the same after the div's positioning ect. ect..

### Code Example: Relative & Static

Place this code into a .html file and open it in your browser.

Watch closely as to what happens when you change the div specially marked from relative-me to static-me. When static or relative what happens when you tell it to move left or right?

```html
<!DOCTYPE html>
<html>
<head>
    <title>Lesson: Static and Relative</title>
<style type="text/css">
    body {
        background-color: rgb(20,20,20);
        color: white;

        padding-left: 50px;
    }
    div {
        box-sizing: border-box;
        height: 200px;
        width: 80%;
        border: 2px dotted silver;
        background-color: rgb(30,30,30);
    }
    .static-me {
        position: static;
        border-color: red;
        border-style: dashed;
    }
    .relative-me {
        position: relative;
        border-color: lightblue;
        border-style: dashed;
    }
    .left {
        left: 20px;
    }
    .right {
        right: 20px;
    }
</style>
</head>
<body>
<div class="relative-me left"> 
    This object is relative of body to the left.  
    <div class="relative-me right">
        <strong>Change Me</strong>
        <p>
        Change me from relative to static, watch the difference.
        If you give tell me to move left or right, what happens?
        </p>
    </div>
</div>
<div class="relative-me right">
    Div, relative right, inside main
</div>
</body>
</html>
```

* sources: 
 * http://www.w3schools.com/css/css_positioning.asp
* <small>Created by Allen J. Mills,[(Github)](https://github.com/FelixVicis) (4/14/16)<small>