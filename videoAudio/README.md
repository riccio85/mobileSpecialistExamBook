### Specify multpile viedo formats

```html
<video controls>
  <source src="https://storageurl/videos/chrome.webm" type="video/webm">
  <source src="https://storageurl/videos/chrome.mp4" type="video/mp4">
  <p>This browser does not support the video element.</p>
</video>
```

### With image poster
```html
<video controls>
  <source src="https://storageurl/videos/chrome.webm" type="video/webm">
  <source src="https://storageurl/videos/chrome.mp4" type="video/mp4">
  <p>This browser does not support the video element.</p>
</video>
```
### Addtrack element (add captions) useful for accessibility
```html
<video controls>
  <source src="https://storage..s/videos/chrome.webm" type="video/webm" />
  <source src="https://storage.go./videos/chrome.mp4" type="video/mp4" />
  <track src="chrome-subtitles-en.vtt" label="English captions"
         kind="captions" srclang="en" default>
  <p>This browser does not support the video element.</p>
</video>
```

### Specify start and end time #t=[start_time][,end_time]
```html
<source src="video/chrome.webm#t=5,10" type="video/webm">
```

### Fullscreening content
```javascript
document.body.requestFullScreen();
```

### Listening fullscreen change
```javascript
video.addEventListener("fullscreenchange", handler);
```

### Checking if is fullscreen
```javascript
console.log("In full screen mode: ", video.displayingFullscreen);
```


## Video media events
https://developer.mozilla.org/en-US/docs/Web/Guide/Events/Media_events
### onended
```javascript
var v = document.getElementById("myVideo");
   v.onended = function() {
       document.getElementsByClassName("end-notice")[0].style.display = "";
};
```
