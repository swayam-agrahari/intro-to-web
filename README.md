# ✅ Module 1: Basic HTML Structure

Every HTML page starts with a basic structure:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My First HTML Page</title>
  </head>
  <body>
    <h1>Hello, World!</h1>
    <p>Welcome to my first HTML page.</p>
  </body>
</html>
```

## 💡 Explanation

- `<!DOCTYPE html>` → Tells the browser that this is an **HTML5** document.
- `<html>` → The **root element** of the HTML page.
- `<head>` → Contains **metadata** about the document (not visible to the user).
- `<body>` → Contains all the **visible content** on the web page.

---

# ✅ Module 2: Text & Headings

```html
<h1>This is Heading 1</h1>
<h2>This is Heading 2</h2>
<h3>This is Heading 3</h3>
<p>This is a normal paragraph.</p>

<p><b>Bold text</b>, <i>Italic text</i>, <u>Underlined text</u></p>

<p>
  Here’s a <strong>very important</strong> note and <em>emphasized text</em>.
</p>
```

## 💡 Note

- `<b>` and `<i>` → Change **style only** (bold/italic).
- `<strong>` and `<em>` → Add **meaning or importance**, which is useful for **accessibility tools** like screen readers.

---

# ✅ Module 3: Lists

```html
<h2>Unordered List</h2>
<ul>
  <li>Apples</li>
  <li>Bananas</li>
  <li>Oranges</li>
</ul>

<h2>Ordered List</h2>
<ol>
  <li>Wake up</li>
  <li>Brush teeth</li>
  <li>Eat breakfast</li>
</ol>

<h2>Nested List</h2>
<ul>
  <li>
    Frontend
    <ul>
      <li>HTML</li>
      <li>CSS</li>
      <li>JavaScript</li>
    </ul>
  </li>
  <li>Backend</li>
</ul>
```

---

# ✅ Module 4: Links & Images

```html
<p>Visit <a href="https://www.google.com" target="_blank">Google</a></p>

<img src="https://via.placeholder.com/150" alt="Sample Image" />
```

### 💡 Comments:

- `target="_blank"` → Opens the link in a **new tab**.
- `alt` → Provides **alternative text** if the image can’t load; also helps **screen readers**.

---

# ✅ Module 5: Containers (`div` & `span`)

```html
<div style="border: 1px solid black; padding: 10px; margin: 10px;">
  <h2>This is inside a div</h2>
  <p>A <span style="color: red;">span</span> is for styling inline text.</p>
</div>
```

### 💡 Difference:

- `<div>` → A **block-level container** (used for larger sections).
- `<span>` → An **inline container** (used to style small chunks of text).

---

# ✅ Module 6: Tables

```html
<table border="1" cellpadding="5" cellspacing="0">
  <tr>
    <th>Name</th>
    <th>Age</th>
    <th>Country</th>
  </tr>
  <tr>
    <td>Alice</td>
    <td>24</td>
    <td>USA</td>
  </tr>
  <tr>
    <td>Bob</td>
    <td>30</td>
    <td>India</td>
  </tr>
</table>
```

---

# ✅ Module 7: Forms (Super Important!)

```html
<form action="#" method="post">
  <!-- Text input -->
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" required />
  <br /><br />

  <!-- Email input -->
  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required />
  <br /><br />

  <!-- Password input -->
  <label for="password">Password:</label>
  <input type="password" id="password" name="password" />
  <br /><br />

  <!-- Radio buttons -->
  <p>Gender:</p>
  <input type="radio" id="male" name="gender" value="male" />
  <label for="male">Male</label>
  <input type="radio" id="female" name="gender" value="female" />
  <label for="female">Female</label>
  <br /><br />

  <!-- Checkbox -->
  <input type="checkbox" id="subscribe" name="subscribe" />
  <label for="subscribe">Subscribe to newsletter</label>
  <br /><br />

  <!-- Dropdown -->
  <label for="country">Country:</label>
  <select id="country" name="country">
    <option value="us">USA</option>
    <option value="in">India</option>
    <option value="uk">UK</option>
  </select>
  <br /><br />

  <!-- Textarea -->
  <label for="message">Message:</label><br />
  <textarea id="message" name="message" rows="4" cols="30"></textarea>
  <br /><br />

  <!-- Submit button -->
  <button type="submit">Submit</button>
  <!-- Reset button -->
  <button type="reset">Reset</button>
</form>
```

---

# ✅ Module 8: Multimedia

```html
<h2>Video Example</h2>
<video width="320" height="240" controls>
  <source src="sample.mp4" type="video/mp4" />
  Your browser does not support video tag.
</video>

<h2>Audio Example</h2>
<audio controls>
  <source src="sample.mp3" type="audio/mpeg" />
  Your browser does not support audio tag.
</audio>
```

---

# ✅ Module 9: Semantic HTML (Best Practice!)

```html
<header>
  <h1>My Website</h1>
  <nav>
    <a href="#">Home</a> | <a href="#">About</a> |
    <a href="#">Contact</a>
  </nav>
</header>

<main>
  <article>
    <h2>Blog Post</h2>
    <p>This is a blog post inside an article.</p>
  </article>
</main>

<footer>
  <p>&copy; 2025 My Website</p>
</footer>
```

---
