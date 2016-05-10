# Plugins
<link rel="stylesheet" type="text/css" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.6.2/css/font-awesome.min.css">
## <i style="font-size: 3em;" class="fa fa-fort-awesome" aria-hidden="true"></i> [Font Awesome](http://fortawesome.github.io/Font-Awesome/)
Summary: We've discussed many ways in which CSS is extremely versitile and can be used to enhance otherwise stale html. This section is to discuss the plugins and import that help further this ablility.

Description

## <i style="font-size: 0.9em;" class="fa fa-wifi fa-rotate-270" aria-hidden="true" /> **[CDN](#cdn "Content Delivery Network")**

Get Bootstraps Font Awesome CDN
 >  https://maxcdn.bootstrapcdn.com/font-awesome/4.6.2/css/font-awesome.min.css

Get Cloudflares Font Awesome CDN
 > https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.6.2/css/font-awesome.min.css

Get your own configurable CND link from the source
 > https://fortawesome.github.io/Font-Awesome/get-started/

To add a CDN to your website use the following:
```html
<head>
  <link rel="stylesheet" type="text/css" href="your-CDN-Link-Here.css">
</head>
```

## Icons!

Font awesome has an enormous list(632 currently) of icons that can be used.

<i title="I'm only one of many!" style="font-size: 5em; position: relative; display: block; text-align: center;" class="fa fa-camera" aria-hidden="true" />
The simplist way to use them is to place them on a page with the i tag. 

Example: `<i class="fa fa-camera" aria-hidden="true" />`

Options can be applied within the classes, such as a size grow. 

Example: `<i class="fa fa-camera fa-2x" aria-hidden="true" />`


## <i title="Loading?" class="fa fa-cog fa-spin fa-lg" /> Advanced Features

###For those who seek more advanced features out of their icons:

- <div><i class="fa fa-check-circle-o"/> These Icons can be used as list icons.</div>

To listify your icons:
```html
<ul class="fa-ul">
<li><i class="fa-li fa-your-icon" /> This an unordered list with icons.</li>
</ul>

<ol class="fa-ol">
<li><i class="fa-li fa-your-icon" /> This is an ordered list with icons</li>
</ol>
```


- They can also be used as article icons.

<div><i class="fa fa-magic fa-4x fa-pull-left" />
Meditation is all about the pursuit of nothingness. It's like the ultimate rest. It's better than the best sleep you've ever had. It's a quieting of the mind. It sharpens everything, especially your appreciation of your surroundings. It keeps life fresh. -Hugh Jackman
Read more at: [source](http://www.brainyquote.com/quotes/keywords/meditation.html)</div>

  For article icons use fa class options `fa-pull-left` and `fa-pull-right`

- As you may have noticed in the title, you can have animated <i class="fa fa-power-off fa-spin fa-lg" /> icons!. Animation is done with fa class option `fa-spin`

- Next, there are options to rotate and flip icons. These are `fa-rotate-*` and `fa-flip-*`

  Hover over each cube below to see what option has been applied.

  <i class="fa fa-cube fa-2x" title="no-options" />
  <i class="fa fa-cube fa-2x fa-rotate-90" title="fa-rotate-90" />
  <i class="fa fa-cube fa-2x fa-rotate-180" title="fa-rotate-180" />
  <i class="fa fa-cube fa-2x fa-rotate-270" title="fa-rotate-270" />
  <i class="fa fa-cube fa-2x fa-flip-horizontal" title="fa-flip-horizontal" />
  <i class="fa fa-cube fa-2x fa-flip-vertical" title="fa-flip-vertical" />


- Finally, icons can be stacked. With option `fa-stack`.

  Example:
  ```
<span class="fa-stack fa-2x">
  <i class="fa fa-bomb fa-stack-1x" />
  <i class="fa fa-ban fa-flip-horizontal fa-stack-2x" style="color: rgba(255,0,0,0.5);" />
</span>
  ```

  <span class="fa-stack fa-2x">
  <i class="fa fa-bomb fa-stack-1x" />
  <i class="fa fa-ban fa-flip-horizontal fa-stack-2x" style="color: rgba(255,0,0,0.5);" />
  </span>

* sources: 
 * http://fortawesome.github.io/Font-Awesome/
* <small>Created by Allen J. Mills,[(Github)](https://github.com/FelixVicis) (DATE)<small>