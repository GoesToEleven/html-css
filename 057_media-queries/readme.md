## Advanced Layout
### Media Query
Summary: These advanced methods of layout design will give absolute control over how your page is viewed.

Media Query is to, simply put, query the user's browser. This can allow an extreme amount of control.

These queries come in the form `@media not|only TYPE and (QUERY) {};`

### **Types**
  ```text
    all    : All media types.
    print  : Media types read/used by printers.
    screen : Media used by computer screens, tablets, phones, ect.
    speech : Used for programs that read a page aloud.
  ``` 

  As you can see, the number of media types can account for many situations.

### **Queries**
  Queries are the backbone of this functionality. There are numerous parameters that can be queried but the most common you will use are:
  ```text
  max-width   : Maximum size of the viewable width.
  min-width   : Minimum size of the viewable width.
  max-height  : Maximum size of the viewable height.
  min-height  : Minimum size of the viewable height.
  orientation : Orientation of the viewport. Landscape or Portrait.
  ```

### **Mobile or Desktop First?**

  History is fascinating in many forms. Here is one aspect you may not be aware of.

  In the eve of 2004, a website launches. This site's goal: a resolution dependant layout. [This demo is still alive today](http://www.themaninblue.com/experiment/ResolutionLayout/). CSS3 would not be ready for another four years, and yet, the war for platform begins.

  The terms mobile or desktop first are actually very simple; they simply mean what platform your website is designed to be seen on. In development, this can mean quite a lot. Time and money must go into design and at minimum one design must be excellent. In an ideal world, there would be enough time and money to ensure that all aspects of the layout would work perfectly regardless of platform but in business this is not so.

  As to the war between desktop and mobile, that war has ended. It is common practice to think of your mobile users just as, if not more, important as any others.

  That is, however, not to say that there is no discussion on what we now call Responsive Web Design. Here are a couple of pages that still have notes to chime in on where our designs should go.
  * [Code My Views: Mobile First Design](https://codemyviews.com/blog/mobilefirst)
  * [Codepen: Think Element-First](https://codepen.io/tomhodgins/post/forget-mobile-first-desktop-first-it-s-time-to-think-element-first)

### Code Example: Media Queries

Place this code into a .html file and open it in your browser.

```html
<!DOCTYPE html>
<html>
<head>
  <title>Media Queries</title>
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

    p {
        background-color: rgba(0,255,0,0.2);
    }

    *[hideMe] {
        display: none;
    }

    @media screen and (min-width: 800px) {
        *[ifBig] {
            display: block;
        }
        p {
            background-color: rgba(255,0,0,0.2);
        }
    }

    @media screen and (max-width: 600px) {
        *[ifSmall] {
            display: block;
        }
        p {
            background-color: rgba(0,0,255,0.2);
        }
    }

    @media print {
        body {
            background-color: white;
            color: black;
        }
        p {
            background-color: transparent;
        }
        *[hideMe] {
            display: block;
        }
    }
  </style>
</head>
<body>

<p hideMe ifBig>Hello World, You should only be able to see me if the screen is big!</p>

<p hideMe ifSmall>On the other hand, if the screen is small, I should be visible.</p>

<p hideME>Nothing, however, hides from the printer!</p>

<p>Resize the screen; make it big, small, try to print it. What do you see?</p>

</body>
</html>
```

* sources: 
 * http://www.w3schools.com/css/css3_mediaqueries_ex.asp
 * http://www.w3schools.com/cssref/css3_pr_mediaquery.asp
 * https://en.wikipedia.org/wiki/Responsive_web_design
* <small>Created by Allen J. Mills,[(Github)](https://github.com/FelixVicis) (5/3/2016)<small>
