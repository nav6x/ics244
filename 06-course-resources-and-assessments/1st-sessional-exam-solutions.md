# 1st Sessional Exam & Question Bank Solutions - Web Programming (ICS 244)

[← Back to Course README](../README.md)

- [1. Question 1: HTML Element Identification and HTML5 Tags](#1-question-1-html-element-identification-and-html5-tags)
- [2. Question 2: Family Lineage Nested Ordered Lists](#2-question-2-family-lineage-nested-ordered-lists)
- [3. Question 3: URL Referencing Techniques (Absolute vs Relative)](#3-question-3-url-referencing-techniques-absolute-vs-relative)
- [4. Question 4: Link Destinations and HTML List Types](#4-question-4-link-destinations-and-html-list-types)
- [5. Question 5: Importance of Semantic Structure in HTML](#5-question-5-importance-of-semantic-structure-in-html)
- [6. Question 6: Taxonomy of HTML Tag Types](#6-question-6-taxonomy-of-html-tag-types)
- [7. Question 7: JavaScript Prime Number Checker (`IsPrime()`)](#7-question-7-javascript-prime-number-checker-isprime)
- [8. Question 8: JavaScript Palindrome Checker with Exception Handling](#8-question-8-javascript-palindrome-checker-with-exception-handling)
- [9. Question 9: Complete HTML and CSS Sign-Up Form](#9-question-9-complete-html-and-css-sign-up-form)

---

## 1. Question 1: HTML Element Identification and HTML5 Tags

### A. HTML Element Identification
An **HTML element** is identified by tags: an opening tag (element name in angle brackets), the content, and a closing tag (the element name preceded by a slash `/`). Empty elements such as images or line breaks are self-closing and have no separate closing tag.

$$\text{HTML Element} = \text{Opening Tag } (\langle\text{tag}\rangle) + \text{Content} + \text{Closing Tag } (\langle/\text{tag}\rangle)$$

### B. Tag Examples

#### i) `<header>` and `<footer>`
The `<header>` and `<footer>` are semantic elements that describe the introductory and closing sections of a document or section respectively. The `<header>` typically contains the site title and navigation; the `<footer>` contains copyright or related metadata.

```html
<header>
  <h1>Fundamentals of Web Development</h1>
  <nav role="navigation">
    <ul>
      <li><a href="index.html">Home</a></li>
    </ul>
  </nav>
</header>

<!-- Main content here -->

<footer>
  <p>Copyright &copy; 2015 Share Your Travels</p>
</footer>
```

#### ii) `<figure>` and `<figcaption>`
`<figure>` groups self-contained content like images, diagrams, or illustrations; `<figcaption>` provides a caption for that figure.

```html
<figure>
  <img src="images/central-park.jpg" alt="Conservatory Pond">
  <figcaption>Conservatory Pond in Central Park</figcaption>
</figure>
```

---

## 2. Question 2: Family Lineage Nested Ordered Lists

**Problem**: Create an HTML document to describe an ordered list with the following contents:
- **Highest Level (Parents)**: Mother first. List style: Uppercase Roman numerals (`type="I"`), Background color: **pink**.
- **Middle Lists (Siblings)**: Brothers and sisters of each parent, eldest first. List style: Uppercase letters (`type="A"`). At least 3 items under each parent.
- **Inner Lists (Cousins)**: Children of uncles and aunts under proper parents. List style: Arabic numerals (`type="1"`), Background color: **green**. At least 3 items under each aunt/uncle.

```html
<!DOCTYPE html>
<html>
<body style="background-color: white;">

<ol type="I" style="background-color: pink;">
  <li>Mother's Name
    <ol type="A">
      <li>Eldest Sibling
        <ol style="background-color: green;" type="1">
          <li>Cousin 1</li>
          <li>Cousin 2</li>
          <li>Cousin 3</li>
        </ol>
      </li>
      <li>Middle Sibling
        <ol style="background-color: green;" type="1">
          <li>Cousin 1</li>
          <li>Cousin 2</li>
          <li>Cousin 3</li>
        </ol>
      </li>
      <li>Youngest Sibling
        <ol style="background-color: green;" type="1">
          <li>Cousin 1</li>
          <li>Cousin 2</li>
          <li>Cousin 3</li>
        </ol>
      </li>
    </ol>
  </li>

  <li>Father's Name
    <ol type="A">
      <li>Eldest Sibling
        <ol style="background-color: green;" type="1">
          <li>Cousin 1</li>
          <li>Cousin 2</li>
          <li>Cousin 3</li>
        </ol>
      </li>
      <li>Middle Sibling
        <ol style="background-color: green;" type="1">
          <li>Cousin 1</li>
          <li>Cousin 2</li>
          <li>Cousin 3</li>
        </ol>
      </li>
      <li>Youngest Sibling
        <ol style="background-color: green;" type="1">
          <li>Cousin 1</li>
          <li>Cousin 2</li>
          <li>Cousin 3</li>
        </ol>
      </li>
    </ol>
  </li>
</ol>

</body>
</html>
```

---

## 3. Question 3: URL Referencing Techniques (Absolute vs Relative)

URL referencing specifies how web documents locate internal and external resources. Two common types are **Absolute** and **Relative** referencing.

1. **Absolute Referencing**: Fully qualified URL specifying protocol, domain name, and path.
   - Example: `<a href="http://www.centralpark.com">Central Park</a>`
2. **Relative Referencing**: Path specified relative to the current document location.
   - Child Directory Example: `<a href="css/images/background.gif">Background Image</a>`
   - Root Reference Example: `<a href="/about.html">About Us Page</a>`

---

## 4. Question 4: Link Destinations and HTML List Types

### A. Link Destinations
1. **Email Link**: `<a href="mailto:person@somewhere.com">Someone</a>`
2. **Page Section Fragment**: `<a href="productX.html#reviews">Reviews</a>`
3. **JavaScript Trigger**: `<a href="javascript:OpenAnnoyingPopup();">See This</a>`
4. **Telephone Call**: `<a href="tel:+18009220579">Call Support</a>`

### B. Types of Lists in HTML
1. **Ordered List (`<ol>`)**: Numbered sequential items.
   ```html
   <ol>
     <li>Introduction</li>
     <li>Background</li>
   </ol>
   ```
2. **Unordered List (`<ul>`)**: Bulleted non-sequential items.
   ```html
   <ul>
     <li>Apples</li>
     <li>Oranges</li>
   </ul>
   ```
3. **Description List (`<dl>`)**: Terms (`<dt>`) and descriptions (`<dd>`).
   ```html
   <dl>
     <dt>Coffee</dt>
     <dd>Black hot drink</dd>
   </dl>
   ```

---

## 5. Question 5: Importance of Semantic Structure in HTML

Semantic HTML communicates structural meaning and hierarchy rather than just visual appearance.

Key benefits include:
- **Accessibility**: Screen readers for visually impaired users rely on semantic landmarks (`<header>`, `<nav>`, `<main>`, `<footer>`) to navigate documents.
- **Search Engine Optimization (SEO)**: Search engine web crawlers index content hierarchy accurately.
- **Code Maintainability**: Enhances code readability and organization for development teams.

---

## 6. Question 6: Taxonomy of HTML Tag Types

1. **Container Tags**: Consist of opening and closing tags that enclose content (e.g., `<html>...</html>`, `<body>...</body>`).
2. **Empty (Void) Tags**: No closing tag, self-contained elements (e.g., `<br />`, `<hr>`, `<img>`).
3. **Block-Level Elements**: Start on a new line and stretch to fill full container width (e.g., `<h1>`, `<p>`, `<div>`).
4. **Inline Elements**: Flow within surrounding text, consuming only as much width as required (e.g., `<a>`, `<em>`, `<span>`).

---

## 7. Question 7: JavaScript Prime Number Checker (`IsPrime()`)

```html
<!DOCTYPE html>
<html>
<head>
  <title>Prime Checker</title>
  <script>
    function IsPrime() {
      var num = parseInt(document.getElementById('userInput').value, 10);
      if (isNaN(num)) { alert('Please enter a valid integer'); return; }
      if (num <= 1) { alert(num + ' is NOT a Prime Number'); return; }
      for (var i = 2; i <= Math.sqrt(num); i++) {
        if (num % i === 0) { alert(num + ' is NOT a Prime Number'); return; }
      }
      alert(num + ' is a Prime Number');
    }
  </script>
</head>
<body>
  <h2>Prime Number Checker</h2>
  <p>Enter a number:</p>
  <input type="text" id="userInput">
  <button onclick="IsPrime()">Check</button>
</body>
</html>
```

---

## 8. Question 8: JavaScript Palindrome Checker with Exception Handling

```html
<!DOCTYPE html>
<html>
<body>
  <h2>Palindrome Checker</h2>
  <input type="text" id="strInput" placeholder="Enter string">
  <button onclick="checkPalindrome()">Check</button>
  <p id="result"></p>

  <script>
    function checkPalindrome() {
      var str = document.getElementById('strInput').value;
      var display = document.getElementById('result');
      try {
        if (str === '') throw 'Error: Input cannot be blank.';
        if (!isNaN(str)) throw 'Error: Input cannot be a number.';
        var reversed = str.split('').reverse().join('');
        display.textContent = (str === reversed) ? (str + ' IS a palindrome.') : (str + ' is NOT a palindrome.');
      } catch (e) {
        alert(e);
        display.textContent = '';
      }
    }
  </script>
</body>
</html>
```

---

## 9. Question 9: Complete HTML and CSS Sign-Up Form

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    body { font-family: sans-serif; }
    .form-container { background-color: #333; color: white; width: 400px; padding: 20px; }
    .header { background-color: orange; padding: 10px; color: white; margin-bottom: 15px; }
    label { display: inline-block; width: 120px; margin-bottom: 10px; }
    input[type=text], input[type=password], select { width: 200px; }
    .buttons { text-align: center; margin-top: 10px; }
    .submit-btn { background-color: green; color: white; padding: 5px 15px; border: none; }
    .cancel-btn { background-color: red; color: white; padding: 5px 15px; border: none; }
  </style>
</head>
<body>

<div class="form-container">
  <div class="header">Sign Up</div>
  <form>
    <label>First Name</label>
    <input type="text" placeholder="Enter First Name"><br>
    
    <label>Last Name</label>
    <input type="text" placeholder="Enter Last Name"><br>
    
    <label>Date of Birth</label>
    <select style="width:60px;"><option>Date</option></select>
    <select style="width:70px;"><option>Month</option></select>
    <select style="width:60px;"><option>Year</option></select><br>
    
    <label>Gender</label>
    <input type="radio" name="gender"> Male
    <input type="radio" name="gender"> Female<br>
    
    <label>Country</label>
    <select><option>Country</option></select><br>
    
    <label>E-mail</label>
    <input type="text" placeholder="Enter E-mail"><br>
    
    <label>Phone</label>
    <input type="text" placeholder="Enter Phone"><br>
    
    <label>Password</label>
    <input type="password"><br>
    
    <label>Confirm Password</label>
    <input type="password"><br>
    
    <div style="text-align:center; margin: 10px;">
      <input type="checkbox"> I Agree to the Terms of use
    </div>
    
    <div class="buttons">
      <input type="submit" value="Submit" class="submit-btn">
      <input type="button" value="Cancel" class="cancel-btn">
    </div>
  </form>
</div>

</body>
</html>
```
