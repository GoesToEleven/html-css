## Units of Measurement
### 
Summary: Size, width, shape, length; these values are all incredibly important to everything we've used thus far. Hopefully with this lesson, any questions with regards to units will be resolved.

There are two categories to the units used in CSS, relative and absolute.

1. **Relative**

  Just to list off a few there are:
  * em: size relative to font-size
  * ch: relative to the width of 0 character.
  * rem: .. to the font-size of the root element
  * vw: .. to 1% of the width of the viewport.
  * vh: .. to 1% of the height of the viewport
  * vmin: .. to 1% of the viewports smallest dimension
  * vmax: .. to 1% of the viewports largest dimension
  * %: percentage of viewport. Quick version of most relevant vh/vw distance.

  Keep in mind, relative will always move with the device/screen of whatever is viewing it.

1. **Absolute**

  Same as before.
  * cm: centimeters
  * mm: millimeters
  * in: inches as 1 inch = 96px = 2.54 cm
  * px: pixels, **_Big Important note at bottom of this section_**
  * pt: point, 1/72 * 1 in
  * pc: picas, 12pt

  **Note about pixels**
  It is extremely misleading to consider pixels as an absolute form of measurement. The pixels width of a screen is dependant on the quality and manufacturer of the device/screen in question and changes wildly.

### Code Example: Title

Place this code into a .html file and open it in your browser.

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
    body {
      background-color: rgb(20,20,20);
      color: white;
      padding-left: 0px;
    }
    div {
      position: absolute;
      width: 10px;
      height: 10px;
      border: 1px dotted white;
    }
    .override {
      position: relative;
      width: 100%;
      height: 20px;
    }
  </style>
</head>
<body>

<p>Centimeters</p>
<div class="override">
  <div style="top: 5px;left: 0cm;"></div>
  <div style="top: 5px;left: 1cm;"></div>
  <div style="top: 5px;left: 2cm;"></div>
  <div style="top: 5px;left: 3cm;"></div>
  <div style="top: 5px;left: 4cm;"></div>
</div>

<p>Millimeters</p>
<div class="override">
  <div style="top: 5px;left: 0mm;"></div>
  <div style="top: 5px;left: 5mm;"></div>
  <div style="top: 5px;left: 10mm;"></div>
  <div style="top: 5px;left: 15mm;"></div>
  <div style="top: 5px;left: 20mm;"></div>
  <div style="top: 5px;left: 30mm;"></div>
  <div style="top: 5px;left: 40mm;"></div>
</div>

<p>Inches</p>
<div class="override">
  <div style="top: 5px;left: 0in;"></div>
  <div style="top: 5px;left: 1in;"></div>
  <div style="top: 5px;left: 2in;"></div>
  <div style="top: 5px;left: 3in;"></div>
  <div style="top: 5px;left: 4in;"></div>
</div>

<p>Percents</p>
<div class="override">
  <div style="top: 5px;left: 0%;"></div>
  <div style="top: 5px;left: 10%;"></div>
  <div style="top: 5px;left: 20%;"></div>
  <div style="top: 5px;left: 30%;"></div>
  <div style="top: 5px;left: 40%;"></div>
</div>

<p>Pixels</p>
<div class="override">
  <div style="top: 5px;left: 0px;"></div>
  <div style="top: 5px;left: 10px;"></div>
  <div style="top: 5px;left: 20px;"></div>
  <div style="top: 5px;left: 30px;"></div>
  <div style="top: 5px;left: 40px;"></div>
</div>

<p>Em</p>
<div class="override">
  <div style="top: 5px;left: 0em;"></div>
  <div style="top: 5px;left: 10em;"></div>
  <div style="top: 5px;left: 20em;"></div>
  <div style="top: 5px;left: 30em;"></div>
  <div style="top: 5px;left: 40em;"></div>
</div>

<p>Em Larger font size</p>
<div class="override" style="font-size: 50px;">
  <div style="top: 5px;left: 0em;"></div>
  <div style="top: 5px;left: 10em;"></div>
  <div style="top: 5px;left: 20em;"></div>
  <div style="top: 5px;left: 30em;"></div>
  <div style="top: 5px;left: 40em;"></div>
</div>

<p>Em smaller font size</p>
<div class="override" style="font-size: 10px;">
  <div style="top: 5px;left: 0em;"></div>
  <div style="top: 5px;left: 10em;"></div>
  <div style="top: 5px;left: 20em;"></div>
  <div style="top: 5px;left: 30em;"></div>
  <div style="top: 5px;left: 40em;"></div>
</div>

<p>VW</p>
<div class="override">
  <div style="top: 5px;left: 0vw;"></div>
  <div style="top: 5px;left: 10vw;"></div>
  <div style="top: 5px;left: 20vw;"></div>
  <div style="top: 5px;left: 30vw;"></div>
  <div style="top: 5px;left: 40vw;"></div>
</div>

<p>VMin</p>
<div class="override">
  <div style="top: 5px;left: 0vmin;"></div>
  <div style="top: 5px;left: 10vmin;"></div>
  <div style="top: 5px;left: 20vmin;"></div>
  <div style="top: 5px;left: 30vmin;"></div>
  <div style="top: 5px;left: 40vmin;"></div>
</div>

<p>VMax</p>
<div class="override">
  <div style="top: 5px;left: 0vmax;"></div>
  <div style="top: 5px;left: 10vmax;"></div>
  <div style="top: 5px;left: 20vmax;"></div>
  <div style="top: 5px;left: 30vmax;"></div>
  <div style="top: 5px;left: 40vmax;"></div>
</div>

</body>
</html>
```

* sources: 
 * http://www.w3schools.com/cssref/css_units.asp
* <small>Created by Allen J. Mills,[(Github)](https://github.com/FelixVicis) (4/14/16)<small>