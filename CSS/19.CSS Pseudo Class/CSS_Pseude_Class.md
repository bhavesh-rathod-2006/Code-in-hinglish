# CSS Pseudo-Classes Guide

## Introduction
CSS pseudo-classes aise keywords hote hain jo selectors ke saath add kiye jate hain, taaki elements ko unki state, position ya user interaction ke basis par style kiya ja sake. Iske liye additional classes ya IDs ki zaroorat nahi hoti. Yeh dynamic aur context-based styling provide karte hain, jisse interactivity aur design flexibility improve hoti hai. Is guide mein important pseudo-classes, unka syntax aur har definition ke turant baad three examples explain kiye gaye hain, followed by use cases.

## CSS Pseudo-Classes

### 1. **:hover**
**Description**: Jab user apne pointer (jaise mouse) ko kisi element ke upar le jata hai, tab yeh us element par specified styles apply karta hai.

**Syntax**:
```css
selector:hover {
  /* Jab selector par hover hoga, tab styles apply hongi */
}
```

**Example 1: Button Hover Effect**:
```html
<button class="btn">Click Me</button>
```
```css
.btn:hover {
  background-color: #007bff;
  color: white;
}
```
**Result**: Button par hover karne par uska background blue aur text white ho jayega.

**Example 2: Link Underline on Hover**:
```html
<a href="#" class="link">Learn More</a>
```
```css
.link:hover {
  text-decoration: underline;
  color: navy;
}
```
**Result**: Link par hover karne par uske neeche underline aa jayegi aur uska color navy ho jayega.

**Example 3: Image Zoom on Hover**:
```html
<img src="photo.jpg" alt="Photo" class="thumbnail">
```
```css
.thumbnail:hover {
  transform: scale(1.1);
}
```
**Result**: Image par hover karne par woh thodi zoom hokar badi dikhai degi.

### 2. **:focus**
**Description**: Jab kisi element ko focus milta hai, tab yeh us par specified styles apply karta hai. Aam taur par form inputs par click karne ya keyboard navigation ke through focus milta hai.

**Syntax**:
```css
selector:focus {
  /* Jab selector focused hoga, tab styles apply hongi */
}
```

**Example 1: Input Field Outline**:
```html
<input type="text" class="input" placeholder="Enter text">
```
```css
.input:focus {
  outline: 2px solid blue;
}
```
**Result**: Input field par focus aane par uske around blue outline dikhai degi.

**Example 2: Textarea Highlight**:
```html
<textarea class="message"></textarea>
```
```css
.message:focus {
  border-color: green;
  background-color: #f0fff0;
}
```
**Result**: Textarea par focus aane par uska border green aur background light green ho jayega.

**Example 3: Button Focus Style**:
```html
<button class="submit">Submit</button>
```
```css
.submit:focus {
  box-shadow: 0 0 5px rgba(0, 0, 255, 0.5);
}
```
**Result**: Button par focus aane par uske around blue shadow dikhai degi.

### 3. **:first-child**
**Description**: Yeh kisi parent ke child elements mein se pehle child ko select karta hai, agar woh specified selector se match karta ho.

**Syntax**:
```css
selector:first-child {
  /* Siblings mein pehle child se match hone wale selector par styles apply hongi */
}
```

**Example 1: First List Item**:
```html
<ul class="list">
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
```
```css
.list li:first-child {
  font-weight: bold;
}
```
**Result**: Sirf pehla `<li>` (Item 1) bold hoga.

**Example 2: First Paragraph in Article**:
```html
<article class="post">
  <p>Intro paragraph.</p>
  <p>Second paragraph.</p>
</article>
```
```css
.post p:first-child {
  color: blue;
}
```
**Result**: Sirf pehle child ke roop mein maujood `<p>` (Intro paragraph) blue hoga.

**Example 3: First Div in Container**:
```html
<div class="container">
  <div>Section 1</div>
  <div>Section 2</div>
</div>
```
```css
.container div:first-child {
  background-color: #f0f0f0;
}
```
**Result**: Sirf pehle `<div>` (Section 1) ka background light gray hoga.

### 4. **:last-child**
**Description**: Yeh kisi parent ke child elements mein se aakhri child ko select karta hai, agar woh specified selector se match karta ho.

**Syntax**:
```css
selector:last-child {
  /* Siblings mein aakhri child se match hone wale selector par styles apply hongi */
}
```

**Example 1: Last List Item**:
```html
<ul class="nav">
  <li>Home</li>
  <li>About</li>
  <li>Contact</li>
</ul>
```
```css
.nav li:last-child {
  border-bottom: 2px solid black;
}
```
**Result**: Sirf aakhri `<li>` (Contact) ke neeche black border hoga.

**Example 2: Last Paragraph in Section**:
```html
<section class="content">
  <p>Paragraph 1</p>
  <p>Paragraph 2</p>
  <p>Conclusion</p>
</section>
```
```css
.content p:last-child {
  font-style: italic;
}
```
**Result**: Sirf aakhri child ke roop mein maujood `<p>` (Conclusion) italic ho jayega.

**Example 3: Last Div in Wrapper**:
```html
<div class="wrapper">
  <div>Box 1</div>
  <div>Box 2</div>
  <div>Box 3</div>
</div>
```
```css
.wrapper div:last-child {
  background-color: #e0e0e0;
}
```
**Result**: Sirf aakhri `<div>` (Box 3) ka background gray ho jayega.

### 5. **:nth-child(n)**
**Description**: Yeh siblings ke beech elements ko unki position ke basis par select karta hai. Ismein kisi specific index ya pattern ka use kar sakte hain, jaise `2`, `odd`, `even` ya `2n+1`.

**Syntax**:
```css
selector:nth-child(n) {
  /* Siblings mein nth position par selector se match hone wale element par styles apply hongi */
}
```

**Example 1: Alternate List Items**:
```html
<ul class="items">
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
  <li>Item 4</li>
</ul>
```
```css
.items li:nth-child(even) {
  background-color: #f0f0f0;
}
```
**Result**: Even-numbered `<li>` elements (Item 2 aur Item 4) ka background light gray ho jayega.

**Example 2: Third Paragraph in Article**:
```html
<article class="blog">
  <p>Paragraph 1</p>
  <p>Paragraph 2</p>
  <p>Paragraph 3</p>
</article>
```
```css
.blog p:nth-child(3) {
  color: red;
}
```
**Result**: Sirf teesra `<p>` (Paragraph 3) red hoga, agar woh apne parent ka third child hai.

**Example 3: Every Third Div**:
```html
<div class="grid">
  <div>Box 1</div>
  <div>Box 2</div>
  <div>Box 3</div>
  <div>Box 4</div>
</div>
```
```css
.grid div:nth-child(3n) {
  border: 1px solid blue;
}
```
**Result**: Har teesre `<div>` (jaise Box 3) par blue border lagega.

## Use Cases
1. **Interactive UI Elements**: User interaction ko improve karne ke liye `:hover` aur `:focus` use karein, jaise buttons ya form fields ko highlight karna.
2. **List Styling**: Lists, navigation menus ya article sections mein pehle ya aakhri item ko alag dikhane ke liye `:first-child` aur `:last-child` use karein.
3. **Zebra-Striped Tables or Lists**: Tables ya lists mein alternate rows ke colors set karne ke liye `:nth-child` ke saath `odd` ya `even` use karein. Isse content padhna aasaan hota hai.
4. **Conditional Formatting**: Repeating layouts, jaise grid items ya gallery images mein specific elements ko style karne ke liye `:nth-child` ke saath patterns, jaise `2n+1`, use karein.

## Additional Notes
- **Specificity**: Pseudo-classes selector ki specificity badhati hain. CSS conflicts se bachne ke liye inhe carefully combine karein.
- **Performance**: Pseudo-classes additional HTML markup ki zaroorat nahi hone deti, lekin complex `:nth-child` patterns rendering ko affect kar sakte hain.
- **Browser Support**: Yahan listed sabhi pseudo-classes modern browsers mein supported hain.
- **Accessibility**: Keyboard navigation use karne wale users ke liye `:focus` styles clearly visible rakhein, taaki website accessible rahe.