# CSS Display Guide

Yeh guide CSS ki `display` property ko cover karti hai, jo elements ke layout behavior ko control karti hai, including `contents` value. Isme display ki important values ki explanation di gayi hai aur har major category ke liye 3 se zyada examples diye gaye hain.

## Display Property Overview

`display` property yeh specify karti hai ki koi element layout mein kaise render hoga. Yeh element ke box type aur dusre elements ke saath uske interaction ko affect karti hai.

### CSS Property

- **`display`**: Element ka display type define karti hai (jaise `block`, `inline`, `inline-block`, `none`, `flex`, `grid`).

---

## Common Display Values

### 1. Block

Block-level elements hamesha ek **new line** se start hote hain aur available width ki poori space le lete hain.

#### Examples

**1. Basic Block Display**

```css
div {
  display: block;
}
```

`div` ko block element ki tarah behave karne par force karta hai, jo poori width occupy karta hai.

**2. Block with Background**

```css
div {
  display: block;
  background-color: #f0f0f0;
  padding: 10px;
}
```

Block behavior ko highlight karne ke liye background aur padding add karta hai.

**3. Block on Span**

```css
span {
  display: block;
  border: 1px solid black;
}
```

Inline `span` ko block element mein convert karta hai, jisse woh new line se start hota hai.

**4. Block with Fixed Width**

```css
div {
  display: block;
  width: 200px;
  background-color: lightblue;
}
```

Block element ki width ko 200px tak limit karta hai.

### HTML for examples:

```html
<div>Block Element 1</div>
<div>Block Element 2</div>
<span>Span as Block</span>
```

---

### 2. Inline

Inline elements **new line se start nahi hote** aur sirf jitni width zarurat hoti hai utni hi space lete hain.

#### Examples

**1. Basic Inline Display**

```css
span {
  display: inline;
}
```

`span` elements ko inline hi rakhta hai taaki woh side by side dikhein.

**2. Inline with Padding**

```css
span {
  display: inline;
  padding: 5px;
  background-color: yellow;
}
```

Inline elements mein padding aur background add karta hai.

**3. Inline on Div**

```css
div {
  display: inline;
  margin-right: 10px;
}
```

`div` ko inline behave karata hai, jisse multiple divs same line mein aa jate hain.

**4. Inline with Border**

```css
span {
  display: inline;
  border: 1px solid red;
}
```

Inline elements par border add karta hai taaki woh clearly visible ho.

### HTML for examples:

```html
<span>Inline 1</span>
<span>Inline 2</span>
<div>Inline Div</div>
```

---

### 3. Inline-Block

Inline-block elements inline hote hain, lekin `width` aur `height` ko bhi respect karte hain. Matlab yeh inline aur block dono ki properties ka combination hote hain.

#### Examples

**1. Basic Inline-Block**

```css
div {
  display: inline-block;
  width: 100px;
  height: 100px;
}
```

`div` elements ko inline dikhata hai aur specified width aur height bhi apply karta hai.

**2. Inline-Block with Background**

```css
div {
  display: inline-block;
  width: 120px;
  height: 50px;
  background-color: lightgreen;
}
```

Inline-block elements par background color add karta hai.

**3. Inline-Block with Margin**

```css
span {
  display: inline-block;
  width: 80px;
  margin: 5px;
  border: 1px solid black;
}
```

Inline-block `span` elements par margin aur border apply karta hai.

**4. Inline-Block with Padding**

```css
div {
  display: inline-block;
  width: 150px;
  padding: 10px;
  background-color: pink;
}
```

Inline-block elements ke andar spacing ke liye padding add karta hai.

### HTML for examples:

```html
<div>Box 1</div>
<div>Box 2</div>
<span>Inline-Block Span</span>
```

---

### 4. None

`display: none` kisi bhi element ko completely hide kar deta hai aur usse layout se bhi remove kar deta hai.

#### Examples

**1. Basic None Display**

```css
div {
  display: none;
}
```

`div` ko poori tarah hide kar deta hai.

**2. None on Hover**

```css
div:hover {
  display: none;
}
```

Mouse hover karte hi `div` hide ho jata hai.

**3. None with Class**

```css
.hidden {
  display: none;
}
```

`hidden` class wale elements ko hide karta hai.

**4. None on Specific Element**

```css
#special {
  display: none;
}
```

`id="special"` wale element ko hide karta hai.

### HTML for examples:

```html
<div>Hidden Div</div>
<div class="hidden">Class Hidden</div>
<div id="special">Special Hidden</div>
```

---

### 5. Flex

`display: flex` flexible box layout ko enable karta hai. Isse child elements rows ya columns mein arrange hote hain aur flexible sizing milti hai.

#### Examples

**1. Basic Flex Container**

```css
.container {
  display: flex;
}
```

Container ko flexbox banata hai aur children ko row mein align karta hai.

**2. Flex with Direction**

```css
.container {
  display: flex;
  flex-direction: column;
}
```

Flex items ko column mein arrange karta hai.

**3. Flex with Justify Content**

```css
.container {
  display: flex;
  justify-content: space-between;
}
```

Flex items ko container mein equal space ke saath spread karta hai.

**4. Flex with Item Styling**

```css
.container {
  display: flex;
}

.item {
  flex: 1;
  background-color: lightcoral;
  margin: 5px;
}
```

Sabhi flex items ko equal grow karata hai aur unke beech margin add karta hai.

### HTML for examples:

```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
  <div class="item">Item 3</div>
</div>
```

---

### 6. Grid

`display: grid` grid layout ko enable karta hai. Isse rows aur columns par precise control milta hai.

#### Examples

**1. Basic Grid Container**

```css
.container {
  display: grid;
  grid-template-columns: auto auto;
}
```

Do columns wala grid create karta hai.

**2. Grid with Gap**

```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 10px;
}
```

Grid cells ke beech 10px ka gap add karta hai.

**3. Grid with Fixed Columns**

```css
.container {
  display: grid;
  grid-template-columns: 100px 200px;
}
```

Columns ki width fixed 100px aur 200px set karta hai.

**4. Grid with Styling**

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}

.item {
  background-color: lightblue;
  padding: 10px;
}
```

Teen columns wala grid create karta hai aur items ko style bhi karta hai.

### HTML for examples:

```html
<div class="container">
  <div class="item">Grid Item 1</div>
  <div class="item">Grid Item 2</div>
  <div class="item">Grid Item 3</div>
</div>
```

---

## Notes

- `display` property layout control ke liye bahut important hai. Isse `margin`, `padding`, `width` jaise CSS properties ke saath combine karne se aur powerful layouts ban sakte hain.
- `block` ka use full-width elements ke liye karo.
- `inline` ka use text ki tarah flow hone wale elements ke liye karo.
- `inline-block` ka use un inline elements ke liye karo jinko width aur height bhi deni ho.
- `none` ka use kisi element ko hide karne ke liye karo.
- `flex` flexible layouts banane ke liye use hota hai.
- `grid` structured rows aur columns wale layouts ke liye use hota hai.
- `contents` element ka box remove karta hai, lekin uske child elements ka layout preserve rakhta hai.
- **Note:** `display: contents` purane browsers ya kuch specific elements (jaise `img` jaise replaced elements) ke saath expected tarike se kaam nahi kar sakta.