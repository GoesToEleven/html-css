## Box Sizing
### Border-Box

Summary: `box-sizing: border-box;` makes sizing elements to take the same space much easier than alternatives.

In this lesson, we will focus on the CSS3 property *box-sizing*. There will be a code demo at the bottom.

* **Box Sizing**

    ```css
    .boxed {
        box-sizing: border-box;
        height: 100px;
        width: 50%;
    }
    ```
  As you may have learned before now, sizing objects using css is a bit more complicated than just a single size. For a single direction size includes: Margin, Border, Padding, and then content. Taking this into account, using something as woefully simple as height or width is too simple to properly take into account the real dimentions of an object.

  However, there is hope. Using box-sizing will, in essance, make sizing do exactly what you think it should.

  With `box-sizing: border-box;` width and height are now calculated with padding and border taken into account. Such behavior is so desired that it is not uncommon to see,
    ```css
    * {
        box-sizing: border-box;
    }
    ```
  as standard practice in many style sheets.

### Code Example: Boxes, more corners than expected!

Place this code into a .html file and open it in your browser.

look at this

```html
<!DOCTYPE html>
<html>
<head>
    <title>Lesson: Border Box</title>
<style type="text/css">
    body {
        background-color: rgb(20,20,20);
        color: white;
        padding-left: 50px;
    }
    div {
        border: 1px dashed white;
        position: static;
    }
    .boxed {
         box-sizing: border-box;
     }
     .px100 {
        width: 300px;
        height: 100px;
     }
     .largePadding {
        padding: 50px;
     }
     .smallPadding {
        padding: 10px;
     }
</style>
</head>
<body>
<div class="px100 smallPadding">Box 1: Even if we have the same width/height,</div>
<div class="px100 largePadding">Box 2: ..notice that we're different?</div>

<br><br>

<div class="px100 largePadding boxed">Box 3: We on the other hand,</div>
<div class="px100 smallPadding boxed">Box 4: ..are exactly the same--at least on the outside.</div>
</body>
</html>
```

* sources: 
 * http://www.w3schools.com/css/css3_box-sizing.asp
* <small>Created by Allen J. Mills,[(Github)](https://github.com/FelixVicis) (4/14/16)<small>