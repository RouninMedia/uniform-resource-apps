# Uniform Resource Apps (URAs)
On the web, we are long-familiar with the _UR-_ acronyms:

 - **URLs** _(Uniform Resource Locators)_
 - **URIs** _(Uniform Resource Indicators)_
 - **URNs** _(Uniform Resource Names)_

But we don't tend to talk about **Uniform Resource Apps** or **URAs**.

There's every reason why we should.

Who doesn't want a copy-pastable URI which delivers an offline, interactive app into the browser?

_____

## Before we start... a quick note on Single Document Apps
A Single Document App is an app, where all the

 - metadata
 - markup
 - styles
 - scripts
 - data
 - images
 - vectors etc.
 
are contained within a single file.

______

## Uniform Resource Apps (URAs) - Single Document Apps as Data URLs

Once we have a **Single Document App (SDA)**, we can go further.

We can share the **SDA** as a single **Data URL** (optionally encoded using Base-64) which represents the entire app.

We can call this a *Uniform Resource App* or **URA**.

______

**Working Example:**

A **Uniform Resource App** (`HTML` + `CSS` + `JS`) which you can copy-paste into your browser address bar:

### Base-64 Encoded Version:

*data:text/html;base64,PCFET0NUWVBFIGh0bWw+PGh0bWw+PGhlYWQ+PHN0eWxlPmJvZHl7ZGlzcGxheTpmbGV4O2p1c3RpZnktY29udGVudDpjZW50ZXI7YWxpZ24taXRlbXM6Y2VudGVyO2ZsZXgtZGlyZWN0aW9uOmNvbHVtbjtoZWlnaHQ6OTZ2aDtiYWNrZ3JvdW5kLWNvbG9yOnJnYigwLDAsNjMpO31oMSxwe2ZvbnQtc2l6ZTo3MnB4O3RleHQtc2hhZG93OjFweCAxcHggMXB4IHJnYigyNTUsMjU1LDI1NSksMXB4IC0xcHggMXB4IHJnYigyNTUsMjU1LDI1NSksLTFweCAtMXB4IDFweCByZ2IoMjU1LDI1NSwyNTUpLC0xcHggMXB4IDFweCByZ2IoMjU1LDI1NSwyNTUpO2FuaW1hdGlvbjpyb3RhdGVDb2xvcnMgMjFzIGxpbmVhciBpbmZpbml0ZTt9QGtleWZyYW1lcyByb3RhdGVDb2xvcnN7MTQuMjkle2NvbG9yOnllbGxvdzt9MjguNTcle2NvbG9yOm9yYW5nZTt9NDIuODYle2NvbG9yOmdyZWVuO301Ny4xNCV7Y29sb3I6Ymx1ZTt9NzEuNDMle2NvbG9yOmluZGlnbzt9ODUuNzIle2NvbG9yOnZpb2xldDt9fTwvc3R5bGU+PC9oZWFkPjxib2R5PjxoMT5Nb3VzZSBQb3NpdGlvbjo8L2gxPjxwIGNsYXNzPSJtb3VzZS1jb29yZGluYXRlcyI+eDogMDxicj55OiAwPC9wPjxzY3JpcHQ+Y29uc3QgbW91c2VDb29yZGluYXRlcz1kb2N1bWVudC5xdWVyeVNlbGVjdG9yKCcubW91c2UtY29vcmRpbmF0ZXMnKTtkb2N1bWVudC5ib2R5LmFkZEV2ZW50TGlzdGVuZXIoJ21vdXNlbW92ZScsKGUpPT57bW91c2VDb29yZGluYXRlcy5pbm5lckhUTUw9YHg6ICR7ZS5zY3JlZW5YfTxicj55OiAke2Uuc2NyZWVuWX1gfSk7ZG9jdW1lbnQuYm9keS5hZGRFdmVudExpc3RlbmVyKCdjbGljaycsKGUpPT57bW91c2VDb29yZGluYXRlcy5pbm5lckhUTUw9YHg6ICR7ZS5zY3JlZW5YfTxicj55OiAke2Uuc2NyZWVuWX1gfSk8L3NjcmlwdD48L2JvZHk+PC9odG1sPg==*

### Plaintext Version:

```
data:text/html,<!DOCTYPE html><html><head><style>body{display:flex;justify-content:center;align-items:center;flex-direction:column;height:96vh;background-color:rgb(0,0,63);}h1,p{font-size:72px;text-shadow:1px 1px 1px rgb(255,255,255),1px -1px 1px rgb(255,255,255),-1px -1px 1px rgb(255,255,255),-1px 1px 1px rgb(255,255,255);animation:rotateColors 21s linear infinite;}@keyframes rotateColors{14.29%{color:yellow;}28.57%{color:orange;}42.86%{color:green;}57.14%{color:blue;}71.43%{color:indigo;}85.72%{color:violet;}}</style></head><body><h1>Mouse Position:</h1><p class="mouse-coordinates">x: 0<br>y: 0</p><script>const mouseCoordinates=document.querySelector('.mouse-coordinates');document.body.addEventListener('mousemove',(e)=>{mouseCoordinates.innerHTML=`x: ${e.screenX}<br>y: ${e.screenY}`});document.body.addEventListener('click',(e)=>{mouseCoordinates.innerHTML=`x: ${e.screenX}<br>y: ${e.screenY}`})</script></body></html>
```
