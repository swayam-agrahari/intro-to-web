# Linking CSS to HTML

## Three main ways to add CSS:

1. **Inline CSS**

   - Written directly inside an element's `style` attribute.
   - Example: `<h1 style="color: blue;">Hello World</h1>`

2. **Internal CSS**

   - Written inside a `<style>` tag in the `<head>` section of the HTML file.
   - Example:
     ```html
     <style>
       h1 {
         color: red;
       }
     </style>
     ```

3. **External CSS**
   - Written in a separate `.css` file and linked with `<link>` tag in HTML.
   - Example:
     ```html
     <link rel="stylesheet" href="styles.css" />
     ```

Best practice: Use **external CSS** for cleaner code and reusability.

---

# 📦 The CSS Box Model

Every single HTML element on a webpage is treated as a **box** by CSS.  
Understanding this is **crucial** for layout, alignment, and spacing.

---

## 🧩 The 4 Parts of the Box Model

1. **Content** – The actual text, image, or element inside the box.
2. **Padding** – Space between the content and the border _(inside the box)_.
3. **Border** – The line wrapping around the padding and content.
4. **Margin** – Space outside the border, separating the box from other elements.

---

## 📊 Visual Representation

```
+---------------------------+
|        Margin             |
|  +---------------------+  |
|  |       Border        |  |
|  |  +---------------+  |  |
|  |  |   Padding     |  |  |
|  |  | +-----------+ |  |  |
|  |  | |  Content  | |  |  |
|  |  | +-----------+ |  |  |
|  |  +---------------+  |  |
|  +---------------------+  |
+---------------------------+
```

---

## 📝 Example Code

```css
.box {
  width: 200px; /* width of content */
  padding: 20px; /* inside spacing */
  border: 5px solid blue; /* border thickness + color */
  margin: 30px; /* outside spacing */
  background-color: lightyellow;
}
```

```html
<div class="box">Hello, I am a box model example!</div>
```

---

# 📌 The `position` Property

The `position` property in CSS specifies **how an element is positioned** in the document.

There are **five different position values**:

| Value      | Description                                                                               |
| ---------- | ----------------------------------------------------------------------------------------- |
| `static`   | Default positioning. Element follows the **normal document flow**.                        |
| `relative` | Positioned **relative to its original position**. Can be nudged using `top`, `left`, etc. |
| `fixed`    | Positioned **relative to the viewport**. It stays in place when scrolling.                |
| `absolute` | Positioned **relative to the nearest positioned ancestor** (not static).                  |
| `sticky`   | Acts like `relative` until it reaches a **scroll threshold**, then sticks.                |

---

## 📝 Example Code

```css
/* Parent container */
.container {
  width: 500px;
  height: 300px;
  background-color: lightgray;
  margin: 20px auto;
  position: relative; /*  Important: child absolute positions are relative to this */
  padding: 10px;
}

/* Child boxes */
.box1 {
  width: 100px;
  height: 50px;
  background-color: lightcoral;
  position: static; /* Default, normal flow */
}

.box2 {
  width: 100px;
  height: 50px;
  background-color: lightblue;
  position: relative; /* Moves relative to original position */
  top: 0px;
  left: 0px;
}

.box3 {
  width: 100px;
  height: 50px;
  background-color: lightgreen;
  position: absolute; /* Moves relative to nearest positioned parent (.container) */
  bottom: 0px;
  right: 0px;
}

.box4 {
  width: 100px;
  height: 50px;
  background-color: orange;
  position: fixed; /* Stays on screen when scrolling */
  top: 0px;
  left: 0px;
}

.box5 {
  width: 100px;
  height: 50px;
  background-color: violet;
  position: sticky; /* Sticks to top within parent container ie becomes fixed with hit with top */
  top: 0px;
}
```

```html
<div class="container">
  <div class="box1">Static</div>
  <div class="box2">Relative</div>
  <div class="box3">Absolute</div>
  <div class="box5">Sticky</div>
</div>

<div class="box4">Fixed</div>

<p>Scroll down to see fixed and sticky behavior...</p>
<p style="height: 1000px"></p>
<!-- Just to allow scrolling -->
```

# 📝 CSS Typography

We’ll style a paragraph and heading and explain the commonly used typography attributes.

---

## 📝 Example Code

```css
.card {
  width: 300px;
  padding: 20px;
  margin: 50px auto;
  color: white; /* Text color */
  background: linear-gradient(to right, #ff7e5f, #feb47b); /* Gradient */
  text-align: center;
  border: 1px solid rgb(102, 102, 102);
  border-radius: 15px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* Optional shadow for style */
}

.card h2 {
  margin-bottom: 15px;
}

.card p {
  font-size: 16px;
}
```

```html
<div class="card">
  <h2>Welcome!</h2>
  <p>This card demonstrates text color, background color, and gradient.</p>
</div>
```
