# CSS Pseudo-Elements Guide

## Introduction

CSS pseudo-elements aise keywords hote hain jo selectors ke saath add kiye jaate hain, taaki kisi element ke specific parts ko style kiya ja sake ya element ke content se pehle ya baad mein content insert kiya ja sake. Ye HTML ko modify kiye bina content ke specific parts ko style karne ya decorative elements add karne ki facility dete hain. Is guide mein important pseudo-elements, unka syntax aur har definition ke turant baad teen examples diye gaye hain, jiske baad unke use cases explain kiye gaye hain.

## CSS Pseudo-Elements

### 1. **::before**
**Description**: Ye kisi element ke existing content se pehle content insert karta hai. Kya insert karna hai, ye specify karne ke liye `content` property ki zaroorat hoti hai (jaise text, image ya empty string).

**Syntax**:
```css
selector::before {
  content: "value";
  /* Other styles */
}
```

**Example 1: Adding a Decorative Icon**:
```html
<p class="note">Important message</p>
```
```css
.note::before {
  content: "★ ";
  color: gold;
}
```
**Result**: Text "Important message" se pehle ek golden star dikhai dega.

**Example 2: Inserting a Quote Symbol**:
```html
<blockquote class="quote">Wisdom is power.</blockquote>
```
```css
.quote::before {
  content: "“";
  font-size: 1.5em;
  color: #333;
}
```
**Result**: Blockquote ke text se pehle ek opening quotation mark dikhai dega.

**Example 3: Adding a Bullet Point**:
```html
<li class="item">Task 1</li>
```
```css
.item::before {
  content: "• ";
  color: blue;
}
```
**Result**: List item ke text se pehle ek blue bullet point dikhai dega.

### 2. **::after**
**Description**: Ye kisi element ke existing content ke baad content insert karta hai. Kya insert karna hai, ye specify karne ke liye `content` property ki zaroorat hoti hai.

**Syntax**:
```css
selector::after {
  content: "value";
  /* Other styles */
}
```

**Example 1: Adding a Link Arrow**:
```html
<a href="#" class="link">Read More</a>
```
```css
.link::after {
  content: " →";
  color: blue;
}
```
**Result**: Link ke text ke baad ek blue right arrow dikhai dega.

**Example 2: Decorative Line After Heading**:
```html
<h2 class="section-title">About Us</h2>
```
```css
.section-title::after {
  content: "";
  display: block;
  width: 50px;
  height: 2px;
  background: black;
  margin-top: 5px;
}
```
**Result**: Heading ke neeche ek black horizontal line dikhai degi.

**Example 3: Adding a Suffix to Prices**:
```html
<span class="price">19.99</span>
```
```css
.price::after {
  content: " USD";
  font-size: 0.8em;
}
```
**Result**: Price ki value ke baad "USD" dikhai dega.

### 3. **::first-line**
**Description**: Ye kisi block-level element ki text ki pehli line ko style karta hai. Text wrap hone ya viewport ka size change hone par ye automatically adjust hota hai.

**Syntax**:
```css
selector::first-line {
  /* Styles applied to the first line */
}
```

**Example 1: Highlighting First Line of Paragraph**:
```html
<p class="intro">This is an introductory paragraph with multiple lines of text. It explains the topic in detail.</p>
```
```css
.intro::first-line {
  font-weight: bold;
  color: navy;
}
```
**Result**: Paragraph ki pehli line bold aur navy color mein dikhai degi.

**Example 2: Uppercase First Line in Article**:
```html
<article class="post">Welcome to our blog. This is a sample article with several lines of content.</article>
```
```css
.post::first-line {
  text-transform: uppercase;
}
```
**Result**: Article ki pehli line uppercase mein dikhai degi.

**Example 3: Styling First Line in Blockquote**:
```html
<blockquote class="quote">Life is a journey, not a destination. Enjoy the ride.</blockquote>
```
```css
.quote::first-line {
  color: green;
  font-style: italic;
}
```
**Result**: Blockquote ki pehli line green aur italic style mein dikhai degi.

### 4. **::first-letter**
**Description**: Ye kisi block-level element ki pehli line ke pehle letter ko style karta hai. Iska use aksar drop caps ya decorative initial letters banane ke liye hota hai.

**Syntax**:
```css
selector::first-letter {
  /* Styles applied to the first letter */
}
```

**Example 1: Drop Cap in Paragraph**:
```html
<p class="story">Once upon a time, there was a great adventure.</p>
```
```css
.story::first-letter {
  font-size: 2em;
  float: left;
  margin-right: 5px;
  color: red;
}
```
**Result**: Pehla letter ("O") bada, left side par aur red color mein dikhai dega, jisse drop cap effect create hoga.

**Example 2: Decorative First Letter in Heading**:
```html
<h2 class="title">Introduction</h2>
```
```css
.title::first-letter {
  color: gold;
  font-weight: bold;
}
```
**Result**: Pehla letter ("I") golden color aur bold style mein dikhai dega.

**Example 3: Styling First Letter in Article**:
```html
<article class="content">Welcome to our site. This is a sample text.</article>
```
```css
.content::first-letter {
  font-size: 1.5em;
  color: blue;
}
```
**Result**: Pehla letter ("W") bada aur blue color mein dikhai dega.

### 5. **::selection**
**Description**: Ye kisi element ke content ke us part ko style karta hai jise user select karta hai (jaise highlighted text).

**Syntax**:
```css
selector::selection {
  /* Styles applied to selected content */
}
```

**Example 1: Custom Text Selection**:
```html
<p class="text">Select this text to see the effect.</p>
```
```css
.text::selection {
  background: yellow;
  color: black;
}
```
**Result**: Select kiye gaye text ka background yellow aur text color black hoga.

**Example 2: Selection in Article**:
```html
<article class="article">This is an article with selectable content.</article>
```
```css
.article::selection {
  background: blue;
  color: white;
}
```
**Result**: Article mein select kiye gaye text ka background blue aur text color white hoga.

**Example 3: Selection in Input Field**:
```html
<input type="text" class="input" value="Type here">
```
```css
.input::selection {
  background: green;
  color: white;
}
```
**Result**: Input field mein select kiye gaye text ka background green aur text color white hoga.

## 1. What is a pseudo-element?

Simple words mein:

> **Pseudo-element humein kisi HTML element ke specific part ko style ya create karne deta hai, bina ek aur HTML element add kiye.**

**Pseudo** word ka matlab hota hai "real nahi" ya "nakli".

Example ke liye, maan lo hamare paas ye HTML hai:

```html
<p>Hello World</p>
```

Normally, agar humein text se pehle ek chhota `★` chahiye, toh hum aise likh sakte hain:

```html
<p>★ Hello World</p>
```

Lekin CSS humein ek aur tareeka deta hai:

```css
p::before {
  content: "★";
}
```

Ab browser screen par aise dikhayega:

```text
★ Hello World
```

Lekin humne HTML mein actual mein `★` add nahi kiya.

---

### `::before`

> **Element ke existing content se pehle kuch generated content add karo.**

```css
p::before {
  content: "👉 ";
}
```

```html
<p>Hello</p>
```

Visual result:

```text
👉 Hello
```

### `::after`

> **Element ke existing content ke baad kuch generated content add karo.**

```css
p::after {
  content: " ✔";
}
```

Visual result:

```text
Hello ✔
```

Isse kuch is tarah samjho:

```text
          <p>Hello</p>
             ↓
       ┌─────────────┐
       │   before    │
       │    Hello    │
       │    after    │
       └─────────────┘
```

Aur simple tarike se:

```text
::before → [ CONTENT ] ← ::after

           Hello
```

---

# 3. Very important: `content`

**`::before` aur `::after` ko normally dikhne ke liye `content` property ki zaroorat hoti hai.**

Example:

```css
p::before {
  content: "★";
}
```

Agar tum ye likhte ho:

```css
p::before {
  color: red;
}
```

Toh generally tumhe kuch bhi dikhai nahi dega, kyunki tumne koi content generate hi nahi kiya hai.

Tum empty content bhi generate kar sakte ho:

```css
p::before {
  content: "";
}
```

Ye **decorative shapes** create karte waqt bahut useful hota hai.

---

# 4. Why do we even need pseudo-elements?

Maan lo tumhare paas ye HTML hai:

```html
<h1>Welcome</h1>
```

Tum iske neeche ek line banana chahte ho.

### Without pseudo-element

Tum aise likh sakte ho:

```html
<h1>Welcome</h1>
<div class="line"></div>
```

Ab tumne sirf decoration ke liye ek extra HTML element add kar diya.

### With pseudo-element

```css
h1::after {
  content: "";
  display: block;
  width: 100px;
  height: 3px;
  background: black;
}
```

HTML same rahega:

```html
<h1>Welcome</h1>
```

Isliye:

> **Pseudo-elements decorative content aur chhoti UI details ke liye bahut useful hote hain, jinhe alag HTML elements ke roop mein add karne ki zaroorat nahi hoti.**

---

# 5. Where do we actually use them?

Yahin par pseudo-elements kaafi useful ho jaate hain.

## Use case 1: Icons / symbols

```css
li::before {
  content: "✓";
  color: green;
}
```

HTML:

```html
<ul>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
</ul>
```

Result:

```text
✓ HTML
✓ CSS
✓ JavaScript
```

---

# 6. Use case 2: Underline / decorative line

Websites mein iska use bahut common hai.

```css
h2 {
  position: relative;
}

h2::after {
  content: "";
  display: block;
  width: 60px;
  height: 4px;
  background: blue;
}
```

Tumhe ye add karne ki zaroorat nahi hai:

```html
<div class="underline"></div>
```

---

# 7. Use case 3: Creating shapes

Ye khaas taur par un **CSS triangles** ko banane mein useful hai, jinke baare mein tum pehle pooch rahe the.

Example:

```css
.box::after {
  content: "";
  position: absolute;

  border-left: 30px solid transparent;
  border-right: 30px solid transparent;
  border-top: 30px solid red;
}
```

Yahan `::after` ek chhote generated element ki tarah kaam karta hai, jise hum position aur style kar sakte hain.

Ye un main reasons mein se ek hai jinki wajah se developers pseudo-elements use karte hain.

---

# 8. Use case 4: Overlay

Maan lo tumhare paas ek image hai:

```html
<div class="card">
  <img src="image.jpg">
</div>
```

Tum image ke upar ek dark transparent layer lagana chahte ho.

Is tarah ek extra element add karne ke bajaye:

```html
<div class="card">
    <img src="image.jpg">
    <div class="overlay"></div>
</div>
```

Tum ye kar sakte ho:

```css
.card {
  position: relative;
}

.card::after {
  content: "";
  position: absolute;
  inset: 0;
  background: rgba(0, 0, 0, 0.4);
}
```

Ab pseudo-element overlay ki tarah kaam karega.

---

# 9. Use case 5: Tooltip

HTML:

```html
<button class="btn">Hover me</button>
```

CSS:

```css
.btn {
  position: relative;
}

.btn::after {
  content: "Click this button";
  position: absolute;
  top: 100%;
  left: 0;
}
```

Ye text kisi doosre HTML element ko add karne ke bajaye CSS ke through generate hota hai.

---

# 10. Use case 6: Adding quotation marks

```html
<p class="quote">
  Learning CSS takes practice.
</p>
```

```css
.quote::before {
  content: "“";
}

.quote::after {
  content: "”";
}
```

Result:

```text
“Learning CSS takes practice.”
```

---

# 11. `::before` and `::after` are NOT actual HTML elements

Ye ek important concept hai.

Agar tum ye likhte ho:

```css
p::before {
  content: "Hello";
}
```

Toh tumne HTML ko is tarah change nahi kiya hai:

```html
<p>
    <span>Hello</span>
    ...
</p>
```

Iske bajaye, CSS rendering ke liye ek **generated pseudo-element** create karta hai.

Isliye students ko ye samjhao:

> **Pseudo-elements mainly styling aur rendering ke purpose se use hote hain. Ye normal HTML elements nahi hain jinhe tum HTML file mein likhte ho.**

---

# 12. Pseudo-class vs pseudo-element

### Pseudo-class

Ismein use hota hai:

```css
:
```

Examples:

```css
button:hover
input:focus
a:visited
li:first-child
```

Ye kisi existing element ki **state ya condition** ko describe karta hai.

Example:

```css
button:hover {
  background: red;
}
```

Meaning:

> Jab button par mouse hover ho raha ho, tab ye style apply karo.

---

### Pseudo-element

Ismein use hota hai:

```css
::
```

Examples:

```css
p::before
p::after
p::first-letter
p::first-line
```

Ye kisi **element ke specific part ya generated content** ko target karta hai.

Simple comparison:

| Pseudo-class              | Pseudo-element                  |
| ------------------------- | ------------------------------- |
| `:hover`                  | `::before`                      |
| `:focus`                  | `::after`                       |
| `:first-child`            | `::first-letter`                |
| State/condition ko describe karta hai | Element ke part/generated content ko style karta hai |
| `:`                       | `::`                            |

Imagine karo ki tumhare paas ek student hai:

```text
Student = HTML element
```

Student pehle se hi wahan hai.

### `::before`

Tum student se **pehle kuch add karte ho**:

```text
⭐ Student
```

### `::after`

Tum student ke **baad kuch add karte ho**:

```text
Student ⭐
```

Tumne HTML mein koi doosra student create nahi kiya.

Tumne bas CSS ke through visually kuch add kiya hai.

---

# 14. One important thing about `::before` and `::after`

Ye kisi element ke **content ke saath associated** hote hain.

Example:

```html
<h1>Hello</h1>
```

Isse approximately is tarah samjho:

```text
┌─────────────────────────┐
│ before │ Hello │ after  │
└─────────────────────────┘
```

Isliye:

```css
h1::before
```

`"Hello"` se pehle aayega.

Aur:

```css
h1::after
```

`"Hello"` ke baad aayega.

---

# 15. Why do we use `position: relative`?

Tumhe aksar ye code dikhai dega:

```css
.box {
  position: relative;
}

.box::after {
  content: "";
  position: absolute;
  right: 0;
  top: 0;
}
```

Kyun?

Kyunki hum chahte hain ki pseudo-element ko `.box` ke relative position kiya jaaye.

Apna pehle padha hua positioning concept yaad karo:

```text
.box
  ↓
position: relative
  ↓
::after
position: absolute
  ↓
uses .box as containing block
```

Isliye pseudo-elements in properties ke saath bahut achhe se kaam karte hain:

```css
position: relative;
position: absolute;
```

Inka use in cheezon ke liye kiya ja sakta hai:

* overlays
* decorations
* badges
* lines
* triangles
* arrows
* tooltips
* icons

---

# 16. One practical example I'd use in class

Students ko ye example do:

### HTML

```html
<div class="card">
  <h2>CSS</h2>
  <p>Learn CSS step by step</p>
</div>
```

### CSS

```css
.card {
  width: 300px;
  padding: 20px;
  border: 1px solid #ddd;
  position: relative;
}

.card::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 5px;
  background: blue;
}
```

Result:

```text
━━━━━━━━━━━━━━━━━━━━  ← ::before
|                  |
|       CSS        |
|                  |
| Learn CSS step   |
| by step          |
|                  |
━━━━━━━━━━━━━━━━━━━━
```

Phir students ko batao:

> "Humne ek extra `<div>` add kiye bina ye blue line create ki."

**Yahi pseudo-elements ka asli fayda hai.**

---

> **Pseudo-element CSS ka ek feature hai jo humein kisi element ke specific part ko style karne ya extra HTML element likhe bina generated content add karne deta hai.**

Aur `before`/`after` ke liye:

> **`::before` element ke content se pehle generated content add karta hai, jabki `::after` element ke content ke baad generated content add karta hai.**

## Use Cases

1. **Decorative Content**: Extra HTML add kiye bina icons, lines ya text (jaise arrows aur quotes) add karne ke liye `::before` aur `::after` use karo, taaki design aur attractive bane.
2. **Typographic Effects**: Articles mein drop caps ya highlighted first lines jaise text effects create karne ke liye `::first-line` aur `::first-letter` apply karo.
3. **User Interaction Feedback**: Selected text ka appearance customize karne ke liye `::selection` use karo. Isse forms ya zyada content wale pages par user experience behtar ho sakta hai.
4. **Dynamic Styling**: Interactive effects create karne ke liye pseudo-elements ko pseudo-classes ke saath combine karo, jaise hover ke time decorative effects dikhana.

## Additional Notes

- **Syntax Note**: Modern CSS mein pseudo-elements ke liye double colons (`::`) use hote hain, lekin backward compatibility ke liye single colon (`:`) bhi supported hai (jaise `:before`).
- **Content Property**: `::before` aur `::after` ke liye `content` property zaroori hoti hai, chahe woh empty hi kyun na ho (`content: ""`).
- **Limitations**: `::first-line` aur `::first-letter` sirf block-level elements par apply hote hain. `::selection` sirf kuch limited properties support karta hai, jaise `color` aur `background`.
- **Browser Support**: Yahan diye gaye sabhi pseudo-elements modern browsers mein supported hain.
- **Accessibility**: Agar `::before` aur `::after` ka content meaningful information deta hai, toh screen readers ke liye ARIA ke through us information ko accessible banana ensure karo. Agar content sirf decoration ke liye hai, toh use decorative hi rakho.