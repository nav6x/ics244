# Assignment 02 Solutions: JavaScript Fundamentals and CSS3 Layouts

[← Back to Course README](../README.md)

- [1. Question 1: JavaScript `alert()` vs `prompt()` Dialogs](#1-question-1-javascript-alert-vs-prompt-dialogs)
- [2. Question 2: Greatest Among Three Numbers Using Ternary Operator](#2-question-2-greatest-among-three-numbers-using-ternary-operator)
- [3. Question 3: Registration Form with JavaScript Validation](#3-question-3-registration-form-with-javascript-validation)
- [4. Question 4: External Style Sheet Syntax](#4-question-4-external-style-sheet-syntax)
- [5. Question 5: Benefits and Demerits of External Style Sheets](#5-question-5-benefits-and-demerits-of-external-style-sheets)
- [6. Question 6: Advantages and Disadvantages of Inline Styles](#6-question-6-advantages-and-disadvantages-of-inline-styles)
- [7. Question 7: 5 Text Formatting CSS Properties](#7-question-7-5-text-formatting-css-properties)
- [8. Question 8: Element, Class, and ID Selectors Demo](#8-question-8-element-class-and-id-selectors-demo)
- [9. Question 9: CSS Hover Effect on Links (Color and Scaling)](#9-question-9-css-hover-effect-on-links-color-and-scaling)
- [10. Question 10: CSS Pseudo-Class Hover Effect](#10-question-10-css-pseudo-class-hover-effect)
- [11. Question 11: Event Handling in JavaScript](#11-question-11-event-handling-in-javascript)
- [12. Question 12: Variable Declarations in JS (`var`, `let`, `const`)](#12-question-12-variable-declarations-in-js-var-let-const)
- [13. Question 13: Document Object Model (DOM) and Selection Methods](#13-question-13-document-object-model-dom-and-selection-methods)
- [14. Question 14: Style Sheets and Components of a CSS Rule](#14-question-14-style-sheets-and-components-of-a-css-rule)
- [15. Question 15: Advantages of CSS](#15-question-15-advantages-of-css)
- [16. Question 16: Custom Font Implementation using `@font-face`](#16-question-16-custom-font-implementation-using-font-face)
- [17. Question 17: Five CSS Text Formatting Styles Demo](#17-question-17-five-css-text-formatting-styles-demo)

---

## 1. Question 1: JavaScript `alert()` vs `prompt()` Dialogs

### Differences Summary
- **`alert()`**: Displays an informational modal dialog box with a message and an **OK** button. It returns `undefined`.
- **`prompt()`**: Displays an interactive modal dialog box with an input text box, **OK**, and **Cancel** buttons. It returns the entered string (or `null` if cancelled).

```javascript
// alert() Example - Notification
alert("Welcome to the Web Programming Portal!");

// prompt() Example - User Input Collection
let userName = prompt("Please enter your name:", "Guest");
if (userName !== null) {
    console.log("Hello, " + userName);
}
```

---

## 2. Question 2: Greatest Among Three Numbers Using Ternary Operator

```javascript
// Collect inputs from user
let num1 = parseFloat(prompt("Enter first number:"));
let num2 = parseFloat(prompt("Enter second number:"));
let num3 = parseFloat(prompt("Enter third number:"));

// Evaluate greatest using nested ternary operator
let greatest = (num1 >= num2 && num1 >= num3) ? num1 : 
               (num2 >= num1 && num2 >= num3) ? num2 : num3;

console.log("The greatest number is: " + greatest);
```

---

## 3. Question 3: Registration Form with JavaScript Validation

```html
<!DOCTYPE html>
<html>
<head>
  <title>Registration Form</title>
  <script>
    function validateForm(event) {
      event.preventDefault(); // Prevent default page submission refresh
      let name = document.getElementById("name").value;
      let email = document.getElementById("email").value;

      if (name.trim() === "") {
        alert("Name cannot be empty.");
        return false;
      }
      if (!email.includes("@")) {
        alert("Please enter a valid email address.");
        return false;
      }

      alert("Registration Successful!");
      return true;
    }
  </script>
</head>
<body>

  <h2>Registration</h2>
  <form onsubmit="validateForm(event)">
    <label>Name: <input type="text" id="name"></label><br><br>
    <label>Email: <input type="text" id="email"></label><br><br>
    <button type="submit">Register</button>
  </form>

</body>
</html>
```

---

## 4. Question 4: External Style Sheet Syntax

To link an external CSS stylesheet, place the `<link>` tag within the `<head>` section of the HTML document:

```html
<head>
  <link rel="stylesheet" type="type/css" href="styles.css">
</head>
```

---

## 5. Question 5: Benefits and Demerits of External Style Sheets

### Benefits:
1. **Reusability**: One CSS file can style multiple web pages across an entire domain.
2. **Maintainability**: Site-wide global design updates require modifying only a single file.
3. **Cleaner HTML**: Keeps HTML markup separated from visual presentation logic.
4. **Fast Loading**: External stylesheets are cached by browsers after initial download.

### Demerits:
1. **Extra HTTP Request**: Requires an additional HTTP request to fetch the CSS file.
2. **Page Dependency**: If the CSS file fails to load, the webpage loses all visual formatting.

---

## 6. Question 6: Advantages and Disadvantages of Inline Styles

### Advantages:
1. **High Specificity**: Overrides external and internal CSS rules due to higher specificity weighting.
2. **Quick Fixes**: Ideal for rapid debugging or applying single-element one-off styles.
3. **No Extra Files**: Does not require fetching external CSS files.

### Disadvantages:
1. **Hard to Maintain**: Styles scattered throughout HTML make global site updates difficult.
2. **Zero Reusability**: Cannot reuse styles across multiple elements.
3. **Cluttered HTML**: Bloats document file size and mixes presentation with content.

---

## 7. Question 7: 5 Text Formatting CSS Properties

1. **`color`**: Sets textual foreground color (e.g., `color: blue;`).
2. **`font-family`**: Specifies font typeface stack (e.g., `font-family: Arial, sans-serif;`).
3. **`font-size`**: Sets text dimension (e.g., `font-size: 16px;`).
4. **`text-align`**: Sets horizontal alignment (e.g., `text-align: center;`).
5. **`text-decoration`**: Adds visual decorations like underlines (e.g., `text-decoration: underline;`).

---

## 8. Question 8: Element, Class, and ID Selectors Demo

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    /* Element Selector */
    p {
      color: blue;
    }
    /* Class Selector */
    .highlight {
      background-color: yellow;
    }
    /* ID Selector */
    #main-heading {
      text-align: center;
      font-size: 24px;
    }
  </style>
</head>
<body>

  <h1 id="main-heading">Selectors Demo</h1>
  <p>This is a paragraph styled by an element selector.</p>
  <p class="highlight">This paragraph uses a class selector.</p>

</body>
</html>
```

---

## 9. Question 9: CSS Hover Effect on Links (Color and Scaling)

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    a {
      color: blue;
      text-decoration: none;
      display: inline-block;
      transition: transform 0.3s, color 0.3s;
    }
    a:hover {
      color: red;
      transform: scale(1.2);
    }
  </style>
</head>
<body>

  <a href="#">Hover over me!</a>

</body>
</html>
```

---

## 10. Question 10: CSS Pseudo-Class Hover Effect

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    .box {
      width: 100px;
      height: 100px;
      background-color: green;
      transition: background-color 0.4s;
    }
    /* Pseudo-class hover selector */
    .box:hover {
      background-color: orange;
    }
  </style>
</head>
<body>

  <div class="box"></div>

</body>
</html>
```

---

## 11. Question 11: Event Handling in JavaScript

**Event Handling** is the process of responding to user interactions (clicks, keypresses, mouse movements) or browser lifecycle events in JavaScript. When an event fires, an associated callback function (event listener) executes automatically to update the page dynamically.

---

## 12. Question 12: Variable Declarations in JS (`var`, `let`, `const`)

| Keyword | Scope Level | Re-declaration | Re-assignment | Hoisting Context |
| :--- | :--- | :--- | :--- | :--- |
| **`var`** | Function / Global | Allowed | Allowed | Hoisted (Initialized as `undefined`) |
| **`let`** | Block Scope `{}` | Disallowed | Allowed | Hoisted (Temporal Dead Zone - TDZ) |
| **`const`** | Block Scope `{}` | Disallowed | Disallowed | Hoisted (Temporal Dead Zone - TDZ) |

```javascript
function testScopes() {
  var globalLike = "I am var";
  let blockScoped = "I am let";
  const constantVal = "I am const";

  if (true) {
    var globalLike = "var is updated";    // Updates outer var variable
    let blockScoped = "new let block";    // Creates separate block-scoped let variable
    // constantVal = "change";            // Uncaught TypeError
  }

  console.log(globalLike);   // Outputs: "var is updated"
  console.log(blockScoped);  // Outputs: "I am let"
}
```

---

## 13. Question 13: Document Object Model (DOM) and Selection Methods

The **Document Object Model (DOM)** is a programming interface for HTML web pages. It represents the document as a logical tree of node objects.

```html
<!DOCTYPE html>
<html>
<body>

  <h1 id="title">DOM Example</h1>
  <input type="text" name="username" value="JohnDoe">
  <p class="text-cls">First paragraph</p>
  <p class="text-cls">Second paragraph</p>

  <script>
    // 1. getElementById: Selects single element by ID
    let titleEl = document.getElementById("title");

    // 2. getElementsByName: Selects NodeList by name attribute
    let userInputs = document.getElementsByName("username");

    // 3. getElementsByTagName: Selects HTMLCollection by tag name
    let paragraphs = document.getElementsByTagName("p");

    // 4. getElementsByClassName: Selects HTMLCollection by class name
    let textElements = document.getElementsByClassName("text-cls");
  </script>

</body>
</html>
```

---

## 14. Question 14: Style Sheets and Components of a CSS Rule

A **Style Sheet** describes the layout and formatting of HTML documents. A CSS rule-set consists of:
1. **Selector**: Points to the target HTML element (e.g., `p`).
2. **Declaration Block**: Enclosed in `{}`.
3. **Property**: Style attribute being modified (e.g., `color`).
4. **Value**: Setting assigned to property (e.g., `red`).

```css
/* Selector { Property: Value; } */
p {
  color: red;
  font-size: 16px;
}
```

---

## 15. Question 15: Advantages of CSS

1. **Separation of Concerns**: Decouples HTML structure from presentation logic.
2. **Site-Wide Consistency**: Maintains uniform styling across multiple pages.
3. **Rapid Redesign**: Updating one external CSS file alters design site-wide.
4. **Improved Page Speed**: Browsers cache external `.css` files, speeding up loads.
5. **Multiple Device Support**: Adapts layouts to mobile, tablet, and desktop viewports using `@media` queries.

---

## 16. Question 16: Custom Font Implementation using `@font-face`

```css
@font-face {
  font-family: 'MyCustomFont';
  src: url('fonts/my-custom-font.woff2') format('woff2'),
       url('fonts/my-custom-font.woff') format('woff');
}

body {
  font-family: 'MyCustomFont', sans-serif;
}
```

---

## 17. Question 17: Five CSS Text Formatting Styles Demo

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    .text-demo {
      color: #336699;              /* 1. Text Color */
      text-align: justify;          /* 2. Text Alignment */
      text-decoration: underline;   /* 3. Text Decoration */
      text-transform: uppercase;    /* 4. Text Transform */
      line-height: 1.6;             /* 5. Line Height (Spacing) */
    }
  </style>
</head>
<body>

  <p class="text-demo">
    This paragraph demonstrates five different css text formatting properties.
  </p>

</body>
</html>
```
