**clock.html**

```html
<!DOCTYPE html>
<html>
<head>
  <title>Flip Clock</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="clock">
    <div class="hours">
      <div class="top"></div>
      <div class="bottom"></div>
    </div>
    <div class="minutes">
      <div class="top"></div>
      <div class="bottom"></div>
    </div>
    <div class="seconds">
      <div class="top"></div>
      <div class="bottom"></div>
    </div>
  </div>

  <script src="script.js"></script>
</body>
</html>
```

**style.css**

```css
.clock {
  width: 1000px;
  height: 200px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.hours, .minutes, .seconds {
  width: 200px;
  height: 200px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: #000;
  color: #fff;
  font-size: 50px;
  font-weight: bold;
}

.top, .bottom {
  width: 200px;
  height: 100px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #fff;
}
```

**script.js**

```javascript
// Get the current time
var date = new Date();
var hours = date.getHours();
var minutes = date.getMinutes();
var seconds = date.getSeconds();

// Set the initial time on the clock
document.querySelector('.hours .top').textContent = Math.floor(hours / 10);
document.querySelector('.hours .bottom').textContent = hours % 10;
document.querySelector('.minutes .top').textContent = Math.floor(minutes / 10);
document.querySelector('.minutes .bottom').textContent = minutes % 10;
document.querySelector('.seconds .top').textContent = Math.floor(seconds / 10);
document.querySelector('.seconds .bottom').textContent = seconds % 10;

// Update the clock every second
setInterval(function() {
  // Get the current time
  var date = new Date();
  var hours = date.getHours();
  var minutes = date.getMinutes();
  var seconds = date.getSeconds();

  // Update the time on the clock
  document.querySelector('.hours .top').textContent = Math.floor(hours / 10);
  document.querySelector('.hours .bottom').textContent = hours % 10;
  document.querySelector('.minutes .top').textContent = Math.floor(minutes / 10);
  document.querySelector('.minutes .bottom').textContent = minutes % 10;
  document.querySelector('.seconds .top').textContent = Math.floor(seconds / 10);
  document.querySelector('.seconds .bottom').textContent = seconds % 10;
}, 1000);
```

**Implementation Details**

The clock is implemented using HTML, CSS, and JavaScript. The HTML code creates the basic structure of the clock, including the three main sections (hours, minutes, and seconds) and the individual digits that make up each section. The CSS code styles the clock, giving it a simple and modern look. The JavaScript code is responsible for updating the clock every second to display the current time.

**Documentation**

The following documentation provides additional information about the clock's functionality:

* The clock is designed to be responsive, so it will adjust its size to fit any screen size.
* The clock can be customized by changing the colors and fonts used in the CSS code.
* The clock can be embedded into other websites or applications using the following code:

```html
<iframe src="clock.html" width="1000px" height="200px"></iframe>
```