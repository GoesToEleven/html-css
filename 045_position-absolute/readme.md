## Position Layout
### Static and Absolute
Summary: Using the `position:<kind>;` property, you may specify the type of positioning/method used on an element.

In this lesson, we will focus on the position properties of *static* and *absolute* specifically. There will be a code demo at the bottom.

1. **Static**
    ```css
    .static-me {
        position: static;
        border: 3px solid black;
    }
    ```
  An object positioned as static will explicitly follow the flow of the webpage, top down. It will not be affected by any top/down/left/right properties. You can use this to specifically isolate an object from the behavior of other objects.

2. **Absolute**
    ```css
    absolute-me {
        position: absolute;
        bottom: 0;
        right: 0;
        border: 3px solid black;    
    }
    ```
  An absolutely positioned object acts much like the fixed object. The difference between the two is that the absolute object's viewport is its parent object.

  With this in mind, an absolutely positioned object that is a child of main will look *exactly* as a fixed object except for one point, *it will scroll with the page.*

  A point to note: An absolute object within a static object will position itself to the closest grandparent that is a non-static object. *eg: An absolute child within a static child of a relative object will position itself to the relative object--not its static parent.*

### Code Example: Absolute & Static

Place this code into a .html file and open it in your browser.

Look carefully at both examples, in the second, why does the absolutely positioned div choose it's grandparent to anchor with instead?

```html
<!DOCTYPE html>
<html>
<head>
    <title>Lesson: Absolute</title>
<style type="text/css">
    body {
        background-color: rgb(20,20,20);
        color: white;
        padding-left: 50px;
    }
    div {
         background-color: rgb(30,30,30);
     }
    .boxed {
         position: relative;
         width:70%;
         height:200px;
         border: 1px dashed white;    
     }
     .absolute-me {
         position: absolute;
         right: 0px;
         left: 10%;
         bottom: 30px;

         border: 1px dotted red;
         padding-top: 10px;
         padding-bottom: 10px;
     }
</style>
</head>
<body>
<!-- Simple Example -->
<div class="boxed">
    <div class="absolute-me">This has been anchored inside of another div.</div>
</div>
<br>
<!-- Example of skipped parent. -->
<div class="boxed">
    <div class="boxed" style="position: static;border-color: green;">
        <p>The absolute div below me will choose our grandparent to align to.</p>
        <div class="absolute-me">This has been anchored inside of another div.</div>
    </div>
</div>
</body>
</html>
```

* sources: 
 * http://www.w3schools.com/css/css_positioning.asp