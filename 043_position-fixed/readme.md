## Position Layout
### Fixed
Summary: Using the `position:<kind>;` property, you may specify the type of positioning/method used on an element.

In this lesson, we will focus on the position property of *fixed* specifically. There will be a code demo at the bottom.

2. **Fixed**

    ```css
    .fix-me {
        position: fixed;
        top: 0;
        left: 0;
        border: 3px solid black;    
    }
    ```
  A fixed object will keep itself in an absolute position relative to the viewport. In this way, it has no inheritance of child/parent as before when speaking of a view into the webpage as it is now tied directly above all to the viewport.

### Code Example: Fixed

Place this code into a .html file and open it in your browser.

Look for these things while interacting with this demo:
* What happens to fixed objects when you scroll the page?
* When changing the number of directions(top/bottom/left/right) specified how does the object react.
* What other objects(if any) can interact with these fixed objects. What happens when all fixed objects are anchored to the same place?

```html
<!DOCTYPE html>
<html>
<head>
    <title>Lesson: Static and Fixed</title>
<style type="text/css">
    body {
        background-color: rgb(20,20,20);
        color: white;

        padding-left: 50px;
        height: 1000px;
    }
    div {
        border: 2px dotted silver;
        background-color: rgb(30,30,30);
    }
    .fix-me {
        position: fixed;
        border: 2px dotted white;
        border-radius: 10px;
        padding: 10px;
    }
</style>
</head>
<body>

<!-- Corner, Top/Left -->
<div class="fix-me" style="left: 20px;top: 20px; border-color: red;">1</div>

<!-- Opposite, left/right - from top -->
<div class="fix-me" style="left: 100px;top: 400px; right:50px; border-color: green;">2</div>

<!-- All Specified -->
<div class="fix-me" style="left: 20px;bottom: 20px; top:75%; right: 75%; border-color: yellow;">3</div>

<!-- Opposite, top/bottom - from right -->
<div class="fix-me" style="bottom: 20px;right: 100px; top:20px; border-color: lightblue;">4</div>

<!-- One direction specified -->
<div class="fix-me" style="right: 20px;border-color: orange;">5</div>

<div>
    <p>I'm static!</p>
    <p>For all the other div's, change the left right top bottom parameters.</p>
    <p>Notice, as you do so, that css does it's best to match where you've asked the div to move to.</p>
    <p>An object with two sides of a corner (left and top for example) will move relative to that corner.</p>
    <p>Something with two opposite sides (left and right) will stretch between them</p>
    <p>Finally, an object with all four directions specified will attempt to stretch to meet all requirements.</p>
</div>

</body>
</html>
```

* sources: 
 * http://www.w3schools.com/css/css_positioning.asp
* <small>Created by Allen J. Mills,[(Github)](https://github.com/FelixVicis) (4/14/16)<small>