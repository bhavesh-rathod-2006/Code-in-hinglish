# CSS Flexbox Guide

## Introduction

CSS Flexbox (Flexible Box Layout) ek one-dimensional layout model hai jo ek container ke andar items ke beech space distribute karne aur unhe align karne ke liye design kiya gaya hai, chahe unki size unknown ho ya dynamic. Yeh responsive aur predictable layouts banane mein bahut acche se kaam karta hai, jo modern web design ke liye perfect hai.

### Key Concepts: Main Axis and Cross Axis

- **Main Axis**: Yeh primary axis hota hai jiske along flex items lay out aur distribute hote hain. Jab `flex-direction` `row` hota hai, toh by default yeh horizontally (left to right) chalta hai. Direction `flex-direction` ke hisab se change hoti hai (jaise `column` ke liye vertical). `justify-content` aur `flex-grow` jaisi properties is axis ke along kaam karti hain.
  
- **Cross Axis**: Yeh main axis ke perpendicular (90 degree) axis hota hai. Default horizontal main axis ke liye, cross axis vertical (top to bottom) hota hai. `align-items` aur `align-self` jaisi properties is axis ke along alignment ko control karti hain.

Flexbox mein shaamil hain:
- **Flex Container**: Parent element jisme `display: flex` ya `display: inline-flex` laga hota hai.
- **Flex Items**: Flex container ke direct children elements.

Yeh guide Flexbox ki sabhi major properties ko **do-do examples** ke sath detail mein samjhati hai aur aakhir mein **teen practical use cases** bhi deti hai.

---

## Flex Container Properties

Yeh properties flex container (parent element) par apply ki jaati hain.

### 1. `display`
Container aur uske children ke liye ek flex context establish karta hai.
- **Values**: `flex` (block-level), `inline-flex` (inline-level).
- **Default**: None (block ya inline).

**Example 1: Block-level flex container**
```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
</div>
```
```css
.container {
  display: flex;
  height: 100px;
  background: lightblue;
}
.item { padding: 20px; }
```
*Items ek block-level container mein horizontally lay out hote hain.*

**Example 2: Inline-level flex container**
```html
<p>Inline <span class="inline-flex">flex example</span> text.</p>
```
```css
.inline-flex {
  display: inline-flex;
  background: yellow;
  padding: 5px;
}
```
*Flex container aas-paas ke text ke sath inline flow karta hai.*

### 2. `flex-direction`
Main axis ki direction ko define karta hai.
- **Values**: `row` (default), `row-reverse`, `column`, `column-reverse`.
- Writing mode se affect hota hai (jaise RTL languages).

**Example 1: Column layout**
```html
<div class="container">
  <div class="item">Top</div>
  <div class="item">Bottom</div>
</div>
```
```css
.container {
  display: flex;
  flex-direction: column;
  height: 200px;
  background: lightgreen;
}
.item { flex: 1; padding: 10px; }
```
*Items vertically stack hote hain aur container ki height fill karte hain.*

**Example 2: Row-reverse layout**
```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
  <div class="item">Item 3</div>
</div>
```
```css
.container {
  display: flex;
  flex-direction: row-reverse;
  width: 300px;
  background: lightcoral;
}
.item { padding: 10px; background: white; }
```
*Items right se left ki taraf lay out hote hain.*

### 3. `flex-wrap`
 Yeh control karta hai ki items nayi lines mein wrap honge ya nahi.
- **Values**: `nowrap` (default), `wrap`, `wrap-reverse`.

**Example 1: Wrapping items**
```html
<div class="container">
  <div class="item">1</div><div class="item">2</div><div class="item">3</div><div class="item">4</div>
</div>
```
```css
.container {
  display: flex;
  flex-wrap: wrap;
  width: 200px;
  height: 100px;
  background: lightyellow;
}
.item { width: 80px; height: 40px; background: pink; }
```
*Jagah kam hone par items nayi row mein wrap ho jaate hain.*

**Example 2: No wrapping**
```html
<div class="container">
  <div class="item">Long content that overflows</div><div class="item">Short</div>
</div>
```
```css
.container {
  display: flex;
  flex-wrap: nowrap;
  width: 150px;
  background: lightgray;
  overflow: hidden;
}
.item { padding: 10px; }
```
*Items ek hi row mein rehte hain, aur zarurat padne par overflow ho sakte hain.*

### 4. `flex-flow`
`flex-direction` aur `flex-wrap` ka shorthand property hai.
- **Values**: jaise `row wrap`, `column nowrap`.

**Example 1: Row wrap**
```html
<div class="container">
  <div class="item">A</div><div class="item">B</div><div class="item">C</div><div class="item">D</div>
</div>
```
```css
.container {
  display: flex;
  flex-flow: row wrap;
  width: 150px;
  height: 80px;
  background: lavender;
}
.item { width: 60px; background: blue; color: white; }
```
*Items horizontally flow karte hain aur zarurat padne par wrap ho jaate hain.*

**Example 2: Column-reverse wrap**
```html
<div class="container">
  <div class="item">1</div><div class="item">2</div><div class="item">3</div>
</div>
```
```css
.container {
  display: flex;
  flex-flow: column-reverse wrap;
  height: 150px;
  background: orange;
}
.item { height: 40px; background: green; }
```
*Items neeche se upar (bottom-up) stack hote hain aur wrap hote hain.*

### 5. `justify-content`
Main axis ke along items ko align karta hai.
- **Values**: `flex-start` (default), `flex-end`, `center`, `space-between`, `space-around`, `space-evenly`.

**Example 1: Space-between**
```html
<div class="container">
  <div class="item">Left</div>
  <div class="item">Right</div>
</div>
```
```css
.container {
  display: flex;
  justify-content: space-between;
  width: 300px;
  height: 50px;
  background: cyan;
}
.item { padding: 10px; }
```
*Items container ke edges par push ho jaate hain.*

**Example 2: Center alignment**
```html
<div class="container">
  <div class="item">Centered</div>
</div>
```
```css
.container {
  display: flex;
  justify-content: center;
  width: 200px;
  height: 50px;
  background: magenta;
}
.item { padding: 10px; }
```
*Item horizontally center ho jata hai.*

### 6. `align-items`
Cross axis ke along items ko align karta hai.
- **Values**: `stretch` (default), `flex-start`, `flex-end`, `center`, `baseline`.

**Example 1: Center cross-axis**
```html
<div class="container">
  <div class="item short">Short</div>
  <div class="item tall">Tall content here</div>
</div>
```
```css
.container {
  display: flex;
  align-items: center;
  height: 100px;
  background: lime;
}
.item { padding: 10px; }
.tall { height: 60px; }
```
*Alag-alag heights hone ke bawajood items vertically center ho jaate hain.*

**Example 2: Baseline alignment**
```html
<div class="container">
  <div class="item">Text baseline</div>
  <div class="item" style="font-size: 24px;">Larger text</div>
</div>
```
```css
.container {
  display: flex;
  align-items: baseline;
  height: 50px;
  background: teal;
}
.item { padding: 10px; }
```
*Items apne text ki baseline ke hisab se align hote hain.*

### 7. `align-content`
Multi-line containers mein cross axis ke along lines ko align karta hai.
- **Values**: `stretch` (default), `flex-start`, `flex-end`, `center`, `space-between`, `space-around`, `space-evenly`.

**Example 1: Space-around lines**
```html
<div class="container">
  <div class="item">Line 1 Item</div><div class="item">Line 1 Item</div>
  <div class="item">Line 2 Item</div><div class="item">Line 2 Item</div>
</div>
```
```css
.container {
  display: flex;
  flex-wrap: wrap;
  align-content: space-around;
  height: 200px;
  width: 200px;
  background: gold;
}
.item { width: 80px; height: 40px; background: red; }
```
*Wrapped lines cross axis ke along evenly space ho jaati hain.*

**Example 2: Center lines**
```html
<div class="container">
  <div class="item">A</div><div class="item">B</div><div class="item">C</div>
</div>
```
```css
.container {
  display: flex;
  flex-wrap: wrap;
  align-content: center;
  height: 150px;
  width: 150px;
  background: purple;
}
.item { width: 60px; height: 30px; background: white; }
```
*Lines container ke andar vertically center ho jaati hain.*

### 8. `gap`
Flex items ke beech spacing set karta hai.
- **Values**: `<length>` (jaise `10px`), `<percentage>`, ya `row-gap`/`column-gap`.

**Example 1: Uniform gap**
```html
<div class="container">
  <div class="item">1</div><div class="item">2</div><div class="item">3</div>
</div>
```
```css
.container {
  display: flex;
  gap: 20px;
  width: 300px;
  background: indigo;
}
.item { padding: 10px; background: cyan; }
```
*Sabhi directions mein items ke beech 20px ka gap aata hai.*

**Example 2: Row-specific gap**
```html
<div class="container">
  <div class="item">Row Gap</div><div class="item">Test</div>
</div>
```
```css
.container {
  display: flex;
  flex-direction: column;
  row-gap: 15px;
  height: 100px;
  background: brown;
}
.item { padding: 10px; }
```
*Column layout mein 15px ka vertical gap aata hai.*

---

## Flex Item Properties

Yeh properties individual flex items (child elements) par apply ki jaati hain.

### 1. `order`
Flex items ke display order ko control karta hai.
- **Values**: Integer (default: 0); kam value wale items pehle dikhte hain.

**Example 1: Reordering items**
```html
<div class="container">
  <div class="item" style="order: 2;">Second</div>
  <div class="item" style="order: 1;">First</div>
  <div class="item">Third</div>
</div>
```
```css
.container {
  display: flex;
  width: 300px;
  background: olive;
}
.item { padding: 10px; background: yellow; }
```
*Items is order mein dikhte hain: First, Second, Third.*

**Example 2: Negative order**
```html
<div class="container">
  <div class="item" style="order: -1;">Priority</div>
  <div class="item">Normal 1</div>
  <div class="item">Normal 2</div>
</div>
```
```css
.container {
  display: flex;
  background: navy;
}
.item { color: white; padding: 10px; }
```
*Priority wala item sabse pehle dikhta hai.*

### 2. `flex-grow`
Yeh decide karta hai ki baaki items ke mukable koi item kitna grow karega.
- **Values**: Number (default: 0).

**Example 1: Equal growth**
```html
<div class="container">
  <div class="item">Grow 1</div>
  <div class="item">Grow 2</div>
</div>
```
```css
.container {
  display: flex;
  width: 300px;
  height: 50px;
  background: pink;
}
.item { flex-grow: 1; padding: 10px; }
```
*Container ko fill karne ke liye dono items barabar grow karte hain.*

**Example 2: Unequal growth**
```html
<div class="container">
  <div class="item" style="flex-grow: 2;">Bigger</div>
  <div class="item" style="flex-grow: 1;">Smaller</div>
</div>
```
```css
.container {
  display: flex;
  width: 300px;
  background: gray;
}
.item { padding: 10px; }
```
*Pehla item dusre item se dugna (2x) grow karta hai.*

### 3. `flex-shrink`
Yeh decide karta hai ki space kam hone par koi item kitna shrink (chhota) hoga.
- **Values**: Number (default: 1).

**Example 1: Prevent shrinking**
```html
<div class="container">
  <div class="item fixed">Fixed width</div>
  <div class="item shrink">Shrinkable</div>
</div>
```
```css
.container {
  display: flex;
  width: 200px;
  background: maroon;
}
.item { padding: 10px; }
.fixed { flex-shrink: 0; width: 150px; }
.shrink { flex-shrink: 1; }
```
*Pehla item apni width maintain rakhta hai; dusra shrink ho jata hai.*

**Example 2: Unequal shrinking**
```html
<div class="container">
  <div class="item" style="flex-shrink: 2;">Shrinks more</div>
  <div class="item" style="flex-shrink: 1;">Shrinks less</div>
</div>
```
```css
.container {
  display: flex;
  width: 150px;
  background: silver;
}
.item { width: 100px; padding: 5px; }
```
*Pehla item dusre se dugna (2x) shrink hota hai.*

### 4. `flex-basis`
Grow/shrink hone se pehle item ki initial size set karta hai.
- **Values**: `<length>`, `auto` (default), `<percentage>`.

**Example 1: Fixed basis**
```html
<div class="container">
  <div class="item">Basis 100px</div>
  <div class="item">Auto</div>
</div>
```
```css
.container {
  display: flex;
  width: 300px;
  background: teal;
}
.item { padding: 10px; }
.item:first-child { flex-basis: 100px; }
```
*Pehla item 100px width se shuru hota hai.*

**Example 2: Percentage basis**
```html
<div class="container">
  <div class="item" style="flex-basis: 50%;">50%</div>
  <div class="item" style="flex-basis: 25%;">25%</div>
</div>
```
```css
.container {
  display: flex;
  background: fuchsia;
}
.item { padding: 10px; }
```
*Items container ke size ke percentage ke hisab se size hote hain.*

### 5. `flex`
`flex-grow`, `flex-shrink`, aur `flex-basis` ka shorthand property hai.
- **Values**: jaise `1` (1 1 0%), `0 1 auto`, `none` (0 0 auto).

**Example 1: Simple flex shorthand**
```html
<div class="container">
  <div class="item">Flex 1</div>
  <div class="item">Flex 1</div>
</div>
```
```css
.container {
  display: flex;
  width: 300px;
  background: pink;
}
.item { flex: 1; padding: 10px; }
```
*Items barabar tarike se grow aur shrink hote hain.*

**Example 2: Custom flex shorthand**
```html
<div class="container">
  <div class="item" style="flex: 2 1 100px;">Larger</div>
  <div class="item" style="flex: 1 1 50px;">Smaller</div>
</div>
```
```css
.container {
  display: flex;
  width: 400px;
  background: coral;
}
.item { padding: 10px; }
```
*Pehle item ka basis bada hota hai aur woh zyada grow karta hai.*

### 6. `align-self`
Kisi specific flex item ke liye `align-items` ko override karta hai.
- **Values**: `auto` (default, `align-items` ko inherit karta hai), `flex-start`, `flex-end`, `center`, `baseline`, `stretch`.

**Example 1: Center single item**
```html
<div class="container">
  <div class="item">Default</div>
  <div class="item" style="align-self: center;">Centered</div>
</div>
```
```css
.container {
  display: flex;
  height: 100px;
  background: violet;
}
.item { padding: 10px; }
```
*Dusra item vertically center ho jata hai.*

**Example 2: Flex-end override**
```html
<div class="container">
  <div class="item">Top</div>
  <div class="item" style="align-self: flex-end;">Bottom</div>
</div>
```
```css
.container {
  display: flex;
  align-items: flex-start;
  height: 100px;
  background: skyblue;
}
.item { padding: 10px; }
```
*Dusra item bottom mein align ho jata hai.*

---

## Practical Use Cases with Examples

Flexbox bohot saare layouts ke liye versatile hai. Niche **teen practical use cases** unke examples ke sath diye gaye hain.

### Use Case 1: Navigation Bar
Flexbox ka sabse common use-case evenly spaced links ke sath ek responsive navigation bar banana hai.

**Example: Responsive Navigation Bar**
```html
<nav class="nav">
  <a href="#" class="nav-item">Home</a>
  <a href="#" class="nav-item">About</a>
  <a href="#" class="nav-item">Services</a>
  <a href="#" class="nav-item">Contact</a>
</nav>
```
```css
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: navy;
  padding: 10px;
}
.nav-item {
  color: white;
  text-decoration: none;
  padding: 10px;
}
@media (max-width: 600px) {
  .nav {
    flex-direction: column;
    align-items: stretch;
  }
  .nav-item {
    text-align: center;
    margin: 5px 0;
  }
}
```
*Yeh ek aisa horizontal nav bar banata hai jo chhoti screens par vertically switch ho jata hai.*

### Use Case 2: Card Layout with Wrapping
Flexbox responsively wrap hone wale card layouts banane ke liye ideal hai, jaise ki product grid.

**Example: Product Card Grid**
```html
<div class="card-container">
  <div class="card">Product 1</div>
  <div class="card">Product 2</div>
  <div class="card">Product 3</div>
  <div class="card">Product 4</div>
</div>
```
```css
.card-container {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  justify-content: center;
  padding: 20px;
}
.card {
  flex: 1 1 200px; /* Grow, shrink, min 200px */
  background: lightblue;
  padding: 20px;
  text-align: center;
  border-radius: 5px;
}
```
*Cards rows mein wrap hote hain, aur spacing wa alignment consistent rehti hai.*

### Use Case 3: Centered Hero Section
Flexbox hero section mein content ko center (horizontally aur vertically dono) karna bohot aasan bana deta hai.

**Example: Hero Section**
```html
<section class="hero">
  <div class="hero-content">
    <h1>Welcome</h1>
    <p>Discover our amazing services!</p>
    <button>Learn More</button>
  </div>
</section>
```
```css
.hero {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background: linear-gradient(to right, #ff7e5f, #feb47b);
}
.hero-content {
  text-align: center;
  padding: 20px;
  background: rgba(255, 255, 255, 0.8);
  border-radius: 10px;
}
```
*Content viewport mein perfectly center ho jata hai, jo hero sections ke liye ideal hai.*

---

## Conclusion
Flexbox one-dimensional layouts ke liye ek powerful tool hai, jo navigation bars, card grids, aur centered content ke liye flexibility deta hai. Complex two-dimensional layouts ke liye ise CSS Grid ke sath combine karein. Sabhi browsers par test zaroor karein, kyunki older versions (jaise IE11) mein vendor prefixes ya fallbacks ki zaroorat ho sakti hai.