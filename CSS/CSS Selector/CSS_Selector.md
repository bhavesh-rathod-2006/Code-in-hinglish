## CSS Selectors

CSS selectors ka use specific HTML elements ko target karke unhe style dene ke liye kiya jata hai. Neeche CSS ke sabse common selectors diye gaye hain: **Element**, **ID**, **Class**, **Grouping**, aur **Universal**. Har selector ke saath multiple examples diye gaye hain taaki unka use clearly samajh aaye.

---

### 1. Element Selector

Element selector kisi specific HTML element type ke **saare instances** ko target karta hai, jaise `<p>`, `<h1>`, `<div>`, `<a>`, ya `<ul>`.

**Example 1**:

```css
h2 {
  color: teal;
  font-weight: bold;
}
```

```html
<h2>This is a styled heading</h2>
```

Yeh sabhi `<h2>` elements ko **teal text color** aur **bold font weight** deta hai.

---

**Example 2**:

```css
div {
  border: 1px solid black;
  padding: 10px;
}
```

```html
<div>This is a styled div</div>
<div>Another styled div</div>
```

Yeh sabhi `<div>` elements me **black border** aur **10 pixels padding** add karta hai.

---

**Example 3**:

```css
a {
  text-decoration: none;
  color: orange;
}
```

```html
<a href="#">This is a link</a>
```

Yeh sabhi `<a>` elements ki **underline remove** karta hai aur text ka color **orange** set karta hai.

---

**Example 4**:

```css
ul {
  list-style-type: square;
  margin-left: 20px;
}
```

```html
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
</ul>
```

Yeh sabhi `<ul>` elements ko **square bullets** aur **20 pixels left margin** deta hai.

---

### 2. ID Selector

ID selector kisi ek HTML element ko target karta hai jiske paas specific `id` attribute hota hai. Isme `#` symbol ke baad ID ka naam likha jata hai. Kyunki ek page me ID unique honi chahiye, isliye yeh selector sirf ek hi element par apply hota hai.

**Example 1**:

```css
#banner {
  background-color: yellow;
  text-align: center;
}
```

```html
<div id="banner">Welcome to our website!</div>
```

Yeh `id="banner"` wale element ko **yellow background** aur **center aligned text** deta hai.

---

**Example 2**:

```css
#footer {
  font-size: 14px;
  color: gray;
}
```

```html
<footer id="footer">Copyright 2025</footer>
```

Yeh `id="footer"` wale element ka **font size 14px** aur **text color gray** set karta hai.

---

**Example 3**:

```css
#hero-image {
  width: 100%;
  height: 300px;
}
```

```html
<img id="hero-image" src="image.jpg" alt="Hero Image">
```

Yeh `id="hero-image"` wale image ki **width 100%** aur **height 300 pixels** set karta hai.

---

**Example 4**:

```css
#sidebar {
  background-color: lightgray;
  width: 200px;
}
```

```html
<aside id="sidebar">Sidebar content</aside>
```

Yeh `id="sidebar"` wale element ko **light gray background** aur **200 pixels fixed width** deta hai.

---

### 3. Class Selector

Class selector un sabhi HTML elements ko target karta hai jinke paas same `class` attribute hota hai. Isme `.` (dot) symbol ke baad class ka naam likha jata hai. Ek hi class multiple elements me use ki ja sakti hai.

**Example 1**:

```css
.alert {
  background-color: red;
  color: white;
  padding: 10px;
}
```

```html
<div class="alert">This is an alert!</div>
<p class="alert">Another alert message</p>
```

Yeh `class="alert"` wale sabhi elements ko **red background**, **white text**, aur **10 pixels padding** deta hai.

---

**Example 2**:

```css
.card {
  border: 2px solid blue;
  border-radius: 5px;
}
```

```html
<div class="card">Card 1</div>
<div class="card">Card 2</div>
```

Yeh `class="card"` wale sabhi elements ko **blue border** aur **rounded corners** deta hai.

---

**Example 3**:

```css
.button {
  background-color: green;
  color: white;
  padding: 8px 16px;
}
```

```html
<button class="button">Click Me</button>
<a href="#" class="button">Link Button</a>
```

Yeh `class="button"` wale sabhi elements ko **green background**, **white text**, aur **button jaisa look** deta hai.

---

**Example 4**:

```css
.featured {
  font-style: italic;
  color: purple;
}
```

```html
<span class="featured">Featured Item</span>
<p class="featured">Featured Description</p>
```

Yeh `class="featured"` wale sabhi elements ko **italic font style** aur **purple text color** deta hai.

---

### 4. Grouping Selector

Grouping selector ki help se ek hi CSS rule ko multiple elements ya selectors par apply kiya ja sakta hai. Selectors ko comma (`,`) se separate kiya jata hai.

**Example 1**:

```css
h1, h3, .header {
  font-family: Helvetica;
  color: darkblue;
}
```

```html
<h1>Main Title</h1>
<h3>Subtitle</h3>
<div class="header">Header Text</div>
```

Yeh `<h1>`, `<h3>`, aur `class="header"` wale elements par **Helvetica font** aur **dark blue color** apply karta hai.

---

**Example 2**:

```css
p, span, .text {
  line-height: 1.5;
  color: black;
}
```

```html
<p>Paragraph text</p>
<span>Inline text</span>
<div class="text">Other text</div>
```

Yeh `<p>`, `<span>`, aur `class="text"` wale elements par **line height 1.5** aur **black color** apply karta hai.

---

**Example 3**:

```css
footer, nav, #menu {
  background-color: darkgray;
  padding: 10px;
}
```

```html
<nav>Navigation</nav>
<footer>Footer</footer>
<div id="menu">Menu</div>
```

Yeh `<nav>`, `<footer>`, aur `id="menu"` wale element ko **dark gray background** aur **10 pixels padding** deta hai.

---

**Example 4**:

```css
a, button, .link-style {
  text-decoration: none;
  color: teal;
}
```

```html
<a href="#">Link</a>
<button>Button</button>
<span class="link-style">Styled Span</span>
```

Yeh `<a>`, `<button>`, aur `class="link-style"` wale elements ki **underline remove** karta hai aur **teal color** apply karta hai.

---

### 5. Universal Selector

Universal selector (`*`) page ke **sabhi HTML elements** ko target karta hai. Iska use mostly global styling ya reset CSS ke liye kiya jata hai. Iska impact bahut broad hota hai, isliye ise carefully use karna chahiye.

**Example 1**:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

Yeh sabhi elements ki **margin aur padding reset** karta hai aur `box-sizing` ko `border-box` set karta hai.

---

**Example 2**:

```css
* {
  font-family: Arial, sans-serif;
}
```

Yeh page ke sabhi elements par **Arial font** (ya fallback sans-serif font) apply karta hai.

---

**Example 3**:

```css
* {
  color: darkslategray;
}
```

Yeh sabhi elements ke text ka color **dark slate gray** set karta hai.

---

**Example 4**:

```css
* {
  border: 1px solid lightgray;
}
```

Yeh sabhi elements par **light gray border** apply karta hai. Yeh layout debugging ke time kaafi useful hota hai.

---

### Example Combining Selectors

Neeche ek complete example diya gaya hai jisme **Universal, Element, ID, Class, aur Grouping** selectors ko ek external CSS file ke through HTML document me use kiya gaya hai.

#### HTML File (`index.html`)

```html
<!DOCTYPE html>
<html>
<head>
  <title>CSS Selectors Example</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <h1>Main Heading</h1>
  <h2 class="title">Subheading</h2>
  <h3 class="header">Another Heading</h3>
  <p>This is a paragraph.</p>
  <p class="text">Another paragraph.</p>
  <div id="intro">Introduction section</div>
  <div id="banner">Banner Content</div>
  <span class="highlight">Highlighted text</span>
  <p class="highlight title">Highlighted and titled paragraph</p>
  <div class="alert">Alert Message</div>
  <button class="button">Click Me</button>
  <footer id="footer">Footer Content</footer>
</body>
</html>
```

#### CSS File (`styles.css`)

```css
/* Universal Selector */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* Element Selector */
p {
  color: navy;
  font-size: 16px;
}

h3 {
  font-style: italic;
}

/* ID Selector */
#intro {
  background-color: lightblue;
  padding: 15px;
}

#banner {
  background-color: yellow;
  text-align: center;
}

#footer {
  font-size: 14px;
  color: gray;
}

/* Class Selector */
.highlight {
  color: white;
  background-color: darkgreen;
}

.alert {
  background-color: red;
  color: white;
  padding: 10px;
}

.button {
  background-color: green;
  color: white;
  padding: 8px 16px;
}

/* Grouping Selector */
h1, h2, .title, .header {
  font-family: Arial;
  color: darkred;
}

p, .text {
  line-height: 1.5;
}
```

**Explanation:**

- **Universal Selector:** Sabhi elements ki margin aur padding reset karta hai aur `box-sizing` ko `border-box` set karta hai.
- **Element Selector:** Sabhi `<p>` elements ko **navy color** aur **16px font size** deta hai, aur `<h3>` elements ko **italic style** deta hai.
- **ID Selector:** Unique elements jaise `#intro`, `#banner`, aur `#footer` ko alag-alag specific styles apply karta hai.
- **Class Selector:** `class="highlight"`, `class="alert"`, aur `class="button"` wale sabhi elements par same styles apply karta hai.
- **Grouping Selector:** Multiple elements aur classes jaise `<h1>`, `<h2>`, `.title`, `.header`, aur `<p>`, `.text` par common styles ek hi rule me apply karta hai.