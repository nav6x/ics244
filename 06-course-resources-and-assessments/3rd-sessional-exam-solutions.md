# 3rd Sessional Exam & Question Bank Solutions - Web Programming (ICS 244)

[← Back to Course README](../README.md)

- [1. Question 1: JavaScript Libraries, Purpose of jQuery and Advantages](#1-question-1-javascript-libraries-purpose-of-jquery-and-advantages)
- [2. Question 2: Document Object Model (DOM) and jQuery Selection](#2-question-2-document-object-model-dom-and-jquery-selection)
- [3. Question 3: Events in jQuery and Event Handling](#3-question-3-events-in-jquery-and-event-handling)
- [4. Question 4: jQuery Hide and Show Paragraph Buttons](#4-question-4-jquery-hide-and-show-paragraph-buttons)
- [5. Question 5: jQuery Change Heading Text on Click](#5-question-5-jquery-change-heading-text-on-click)
- [6. Question 6: jQuery Mouseover Background Color Change](#6-question-6-jquery-mouseover-background-color-change)
- [7. Question 7: jQuery Operations (Selecting, Adding Content, Changing Attributes)](#7-question-7-jquery-operations-selecting-adding-content-changing-attributes)
- [8. Question 8: jQuery Image Rollover Effect](#8-question-8-jquery-image-rollover-effect)
- [9. Question 9: jQuery Animated Photo Gallery](#9-question-9-jquery-animated-photo-gallery)
- [10. Question 10: jQuery Form Validation](#10-question-10-jquery-form-validation)
- [11. Question 11: jQuery Sliding Login Panel](#11-question-11-jquery-sliding-login-panel)

---

## 1. Question 1: JavaScript Libraries, Purpose of jQuery and Advantages

### A. JavaScript Libraries & Purpose of jQuery
A **JavaScript library** is a collection of pre-written JavaScript code snippets and functions that abstract complex, repetitive tasks to streamline web application development.

The primary **purpose of jQuery** is to simplify client-side scripting. It wraps verbose, multi-line vanilla JavaScript operations into concise, chainable single-line method calls (e.g., `$(selector)`).

### B. Four Advantages of jQuery
1. **Simplified DOM Manipulation**: Employs intuitive CSS3 selector syntax (`$('#id')`, `.class`) to query and modify HTML elements effortlessly.
2. **Cross-Browser Compatibility**: Normalizes browser inconsistencies, ensuring identical script behavior across Chrome, Firefox, Safari, and Edge.
3. **Streamlined AJAX Support**: Simplifies asynchronous HTTP requests (`$.ajax()`, `$.get()`, `$.post()`) without page reloads.
4. **Built-in Animations & Effects**: Provides out-of-the-box methods for visual transitions (`.fadeIn()`, `.slideToggle()`, `.animate()`).

---

## 2. Question 2: Document Object Model (DOM) and jQuery Selection

### Document Object Model (DOM)
The **DOM** is a standard programming interface for web documents. It represents the HTML page as a hierarchical tree of node objects, enabling programming languages (like JavaScript) to dynamically manipulate the document structure, styles, and content.

### How jQuery Helps in Selecting and Modifying Elements
Vanilla JavaScript requires verbose DOM queries (e.g., `document.getElementsByClassName('item')`). jQuery uses CSS-style selectors to query elements concisely:
```javascript
// Vanilla JS
let elements = document.getElementsByClassName('highlight');
for (let el of elements) { el.style.color = 'red'; }

// Equivalent jQuery Single-Line Call
$('.highlight').css('color', 'red').hide();
```

---

## 3. Question 3: Events in jQuery and Event Handling

**Events** are user interactions or browser state changes (e.g., clicking a button, hovering a mouse, pressing a key, submitting a form). **Event handling** binds listener functions to specific events so that code executes automatically when the event fires.

```html
<!DOCTYPE html>
<html>
<head>
  <title>jQuery Event Demo</title>
  <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
  <script>
    $(document).ready(function(){
      $("#myBtn").click(function(){
        alert("Button was clicked!");
      });
    });
  </script>
</head>
<body>

  <button id="myBtn">Click Me</button>

</body>
</html>
```

---

## 4. Question 4: jQuery Hide and Show Paragraph Buttons

```html
<!DOCTYPE html>
<html>
<head>
  <title>Hide and Show</title>
  <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
  <script>
    $(document).ready(function(){
      $("#hideBtn").click(function(){
        $("p").hide();
      });
      $("#showBtn").click(function(){
        $("p").show();
      });
    });
  </script>
</head>
<body>

  <p>This is a paragraph that will disappear and reappear.</p>
  <button id="hideBtn">Hide</button>
  <button id="showBtn">Show</button>

</body>
</html>
```

---

## 5. Question 5: jQuery Change Heading Text on Click

```html
<!DOCTYPE html>
<html>
<head>
  <title>Change Text</title>
  <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
  <script>
    $(document).ready(function(){
      $("button").click(function(){
        $("h1").text("The Heading Has Been Changed!");
      });
    });
  </script>
</head>
<body>

  <h1>Original Heading</h1>
  <button>Change Text</button>

</body>
</html>
```

---

## 6. Question 6: jQuery Mouseover Background Color Change

```html
<!DOCTYPE html>
<html>
<head>
  <title>Mouseover Event</title>
  <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
  <script>
    $(document).ready(function(){
      $("p").mouseover(function(){
        $(this).css("background-color", "yellow");
      });
    });
  </script>
</head>
<body>

  <p>Hover over this paragraph to change its background color.</p>
  <p>Hover over this one too!</p>

</body>
</html>
```

---

## 7. Question 7: jQuery Operations (Selecting, Adding Content, Changing Attributes)

```html
<!DOCTYPE html>
<html>
<head>
  <title>jQuery Operations</title>
  <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
  <script>
    $(document).ready(function(){
      $("#actionBtn").click(function(){
        // 1. Selecting elements using jQuery selectors
        var $box = $(".content-box");

        // 2. Adding new content to a page
        $box.append("<p>New content added dynamically!</p>");

        // 3. Changing HTML attributes of an image
        $("#myImage").attr("src", "https://via.placeholder.com/150/0000FF/808080");
      });
    });
  </script>
</head>
<body>

  <div class="content-box">
    <h2>Demo Box</h2>
  </div>
  <img id="myImage" src="https://via.placeholder.com/150/FF0000/FFFFFF" alt="Placeholder">
  <br><br>
  <button id="actionBtn">Run Operations</button>

</body>
</html>
```

---

## 8. Question 8: jQuery Image Rollover Effect

```html
<!DOCTYPE html>
<html>
<head>
  <title>Image Rollover</title>
  <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
  <script>
    $(document).ready(function(){
      $("#rolloverImg").hover(
        function() {
          // Mouse enters
          $(this).attr("src", "https://via.placeholder.com/200/0000FF");
        }, 
        function() {
          // Mouse leaves
          $(this).attr("src", "https://via.placeholder.com/200/FF0000");
        }
      );
    });
  </script>
</head>
<body>

  <h3>Hover over the image</h3>
  <img id="rolloverImg" src="https://via.placeholder.com/200/FF0000" alt="Rollover Image">

</body>
</html>
```

---

## 9. Question 9: jQuery Animated Photo Gallery

```html
<!DOCTYPE html>
<html>
<head>
  <title>Photo Gallery</title>
  <style>
    .thumb { width: 100px; cursor: pointer; margin: 5px; }
    #mainImage { width: 400px; display: none; margin-top: 20px; }
  </style>
  <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
  <script>
    $(document).ready(function(){
      $(".thumb").click(function(){
        var newSrc = $(this).attr("src");
        $("#mainImage").fadeOut(300, function() {
          $(this).attr("src", newSrc).fadeIn(500);
        });
      });
    });
  </script>
</head>
<body>

  <div>
    <img class="thumb" src="https://via.placeholder.com/400?text=Image+1" alt="Thumb 1">
    <img class="thumb" src="https://via.placeholder.com/400?text=Image+2" alt="Thumb 2">
    <img class="thumb" src="https://via.placeholder.com/400?text=Image+3" alt="Thumb 3">
  </div>

  <div>
    <img id="mainImage" src="https://via.placeholder.com/400?text=Image+1" alt="Main View">
  </div>

</body>
</html>
```

---

## 10. Question 10: jQuery Form Validation

```html
<!DOCTYPE html>
<html>
<head>
  <title>Form Validation</title>
  <style>
    .error { color: red; display: none; font-size: 12px; }
  </style>
  <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
  <script>
    $(document).ready(function(){
      $("#myForm").submit(function(e){
        e.preventDefault();
        var isValid = true;

        // 1. Validate Name
        if ($("#name").val().trim() === "") {
          $("#nameError").show();
          isValid = false;
        } else {
          $("#nameError").hide();
        }

        // 2. Validate Email using Regex
        var emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
        if (!emailPattern.test($("#email").val())) {
          $("#emailError").show();
          isValid = false;
        } else {
          $("#emailError").hide();
        }

        // 3. Validate Password Length (>= 6)
        if ($("#password").val().length < 6) {
          $("#pwdError").show();
          isValid = false;
        } else {
          $("#pwdError").hide();
        }

        if (isValid) {
          alert("Form submitted successfully!");
        }
      });
    });
  </script>
</head>
<body>

  <form id="myForm">
    <label>Name:</label><br>
    <input type="text" id="name">
    <span class="error" id="nameError">Name cannot be empty</span><br><br>

    <label>Email:</label><br>
    <input type="text" id="email">
    <span class="error" id="emailError">Valid email required</span><br><br>

    <label>Password:</label><br>
    <input type="password" id="password">
    <span class="error" id="pwdError">Password must be at least 6 chars</span><br><br>

    <button type="submit">Submit</button>
  </form>

</body>
</html>
```

---

## 11. Question 11: jQuery Sliding Login Panel

```html
<!DOCTYPE html>
<html>
<head>
  <title>Sliding Login Panel</title>
  <style>
    #loginPanel {
      background-color: #f1f1f1;
      padding: 20px;
      width: 250px;
      display: none; /* Hidden initially */
      border: 1px solid #ccc;
      margin-top: 10px;
    }
  </style>
  <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
  <script>
    $(document).ready(function(){
      $("#toggleLogin").click(function(){
        $("#loginPanel").slideToggle("fast");
      });
    });
  </script>
</head>
<body>

  <button id="toggleLogin">Login / Close</button>

  <div id="loginPanel">
    <h3>Login</h3>
    <label>Username:</label><br>
    <input type="text"><br><br>

    <label>Password:</label><br>
    <input type="password"><br><br>

    <button>Submit</button>
  </div>

</body>
</html>
```
