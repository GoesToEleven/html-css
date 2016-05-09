## Media
### Images, Audio, Video, IFrames
Summary: 

### Images

### Audio

### Video

### Iframe

### Code Example: Media

Place this code into a .html file and open it in your browser.

```html
<!DOCTYPE html><html><head><title>Media</title><!-- Ignore the block behind me. It's not important. --><script type="text/javascript">function clickswap(e){a=document.querySelector("#"+e);b=document.querySelector("#"+e+" + div");if(b.getAttribute("hide")=="yes"){b.setAttribute("hide","no");a.setAttribute("selected","yes");}else{b.setAttribute("hide","yes");a.setAttribute("selected","no");}}</script><style type="text/css"> *{box-sizing:border-box;}body{background-color:rgb(20,20,20);color:white;padding-left:0px;}div{border:1px solid white;width:90vw;margin:10px auto;padding-left:5px;}a{color:gray;font-size:0.7em;}div[hide="yes"]{display:none;}button{border-radius:4px;font-size:20px;width:20%;position:relative;border:none;text-align:center;display:inline-block;margin-top:10px;margin-bottom:0px;clear:right;}button[selected="no"]{background-color:rgba(255,50,50,0.7);color:white;}button[selected="yes"]{background-color:rgba(50,255,50,0.7);color:white;}</style>
  <!-- This is the important css -->
  <style type="text/css">
    img {
        max-width: 100%;
    }
    audio {
        position: relative;
        width: 100%;
    }
    video {
        position: relative;
        width: 100%;
    }
    iframe {
        position: relative;
        width: 500px;
        height: 375px;
    }
  </style>
</head><body>
<p>Click on the buttons to show the indicated media</p>

<button selected="no" id="ImagesTab" onclick="clickswap('ImagesTab')">Images</button>
<div hide="yes">
  <p>A lovely gradient for your eyes to enjoy.
  <a href="http://pcwallart.com/">Source</a></p>
  <img src="http://cdn.pcwallart.com/images/color-gradient-background-wallpaper-2.jpg">
</div>

<button selected="no" id="AudioTab" onclick="clickswap('AudioTab')">Audio</button>
<div hide="yes">
  <p> A test sound of the ocean.
  <a href="http://www.sample-videos.com">Source</a></p> 
  <audio controls> 
    <source src="http://www.sample-videos.com/audio/mp3/wave.mp3" type="audio/mp3"> 
    Audio Not Supported! 
  </audio>
</div>

<button selected="no" id="VideoTab" onclick="clickswap('VideoTab')">Video</button>
<div hide="yes">
  <p> A common test video.
  <a href="http://www.sample-videos.com">Source</a></p> 
  <video controls> 
    <source src="http://www.sample-videos.com/video/mp4/720/big_buck_bunny_720p_2mb.mp4" type="video/mp4"> 
    Video Not Supported! 
  </video>
</div>

<button selected="no" id="IFrameTab" onclick="clickswap('IFrameTab')">IFrame</button>
<div hide="yes">
  <p>This is an iframe of a youtube video!</p> 
  <iframe src="https://www.youtube.com/embed/C0DPdy98e4c" frameborder="0" allowfullscreen></iframe>
</div>
</body></html>
```

* sources: 
 * http://learn.shayhowe.com/html-css/adding-media/
 * http://www.w3schools.com/css/css3_images.asp
 * http://www.w3schools.com/tags/tag_audio.asp
 * http://www.w3schools.com/html/html5_video.asp
 * http://www.w3schools.com/tags/tag_iframe.asp
* <small>Created by Allen J. Mills,[(Github)](https://github.com/FelixVicis) (DATE)<small>



