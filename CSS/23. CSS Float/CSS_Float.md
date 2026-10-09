# CSS Float Property Guide

## Introduction
CSS mein `float` property ka use kisi element ko uske parent container ke andar left ya right side mein position karne ke liye kiya jata hai. Isse doosra content, jaise text ya inline elements, floated element ke around wrap ho sakta hai. Originally, `float` ko images ke around text wrap karne ke liye design kiya gaya tha. Lekin iska use layouts banane ke liye bhi hota hai, halanki complex layouts ke liye aajkal Flexbox ya Grid jaise modern alternatives ko zyada prefer kiya jata hai. `clear` property, `float` ko complement karti hai aur control karti hai ki elements floated elements ke relative kaise behave karenge.

## Syntax
### Float
```css
float: none | left | right | initial | inherit;
```

### Clear
```css
clear: none | left | right | both | initial | inherit;
```

## Property Values

### Float
- `none`: Default value hai; element float nahi hota.
- `left`: Element ko left side mein position karta hai, jisse content uske right side ke around wrap hota hai.
- `right`: Element ko right side mein position karta hai, jisse content uske left side ke around wrap hota hai.
- `initial`: Property ko uski default value (`none`) par reset karta hai.
- `inherit`: Parent element se `float` ki value inherit karta hai.

### Clear
- `none`: Default value hai; element ke dono sides par floating elements allowed hote hain.
- `left`: Element ke left side par floating elements ko prevent karta hai.
- `right`: Element ke right side par floating elements ko prevent karta hai.
- `both`: Element ke dono sides par floating elements ko prevent karta hai, jisse element sabhi floats ke neeche aa jata hai.
- `initial`: Property ko uski default value (`none`) par reset karta hai.
- `inherit`: Parent element se `clear` ki value inherit karta hai.

## How Float and Clear Work
- **Float**: Element ko normal document flow se remove karke uske parent ke andar jitna possible ho, left ya right side mein position karta hai. Non-floated content, jaise text, floated element ke around wrap hota hai. Floated elements, clear na kiye jaane par, baad mein aane wale elements ke layout ko affect kar sakte hain.
- **Clear**: Iska use floated elements ke relative doosre elements ki placement control karne ke liye hota hai. Ye ensure karta hai ki element specified side ya sides par floated elements ke neeche appear ho, jisse unwanted text wrapping ya overlap prevent hota hai.

## Use Cases
1. **Image and Text Wrapping**: Articles ya blog posts mein images ke around text wrap karne ke liye `float` ka use karo. Uske baad aane wale content ko floated image ke neeche start karne ke liye `clear` ka use karo.
2. **Basic Multi-Column Layouts**: Side-by-side columns banane ke liye `float` apply karo, jaise sidebar aur main content. Content ko incorrectly wrap hone se bachane ke liye `clear` ka use karo.
3. **Navigation Menus**: Navigation items ko horizontally align karne ke liye `float` ka use karo. Menu ke neeche aane wale elements ki positioning manage karne ke liye `clear` ka use karo.

## Examples

### Example 1: Image with Text Wrapping
Is example mein image ko left side par float kiya gaya hai, jisse text uske around wrap hota hai. Saath hi, neeche aane wale element par `clear` apply kiya gaya hai.

**HTML**:
```html
<div class="container">
  <img src="example.jpg" alt="Sample Image" class="float-img">
  <p>This is a paragraph of text that wraps around the floated image. It demonstrates how text flows naturally around a floated element.</p>
  <p class="clear">This paragraph appears below the floated image due to the clear property.</p>
</div>
```

**CSS**:
```css
.float-img {
  float: left;
  width: 150px;
  margin-right: 10px;
}

.clear {
  clear: left;
}

.container {
  width: 500px;
  border: 1px solid #ccc;
  padding: 10px;
}
```

**Result**: Image left side par float hoti hai aur text uske right side ke around wrap hota hai. `clear: left` ki wajah se second paragraph floated image ke neeche start hota hai.

### Example 2: Two-Column Layout
Is example mein `float` ka use karke sidebar aur main content ka layout banaya gaya hai. `clear` ensure karta hai ki footer dono columns ke neeche rahe.

**HTML**:
```html
<div class="layout">
  <div class="sidebar">Sidebar Content</div>
  <div class="main">Main Content</div>
  <footer class="clear">Footer</footer>
</div>
```

**CSS**:
```css
.sidebar {
  float: left;
  width: 30%;
  background: #f0f0f0;
  padding: 10px;
}

.main {
  float: right;
  width: 65%;
  background: #e0e0e0;
  padding: 10px;
}

.clear {
  clear: both;
}

.layout {
  width: 600px;
  border: 1px solid #ccc;
}
```

**Result**: Sidebar aur main content ek-doosre ke side mein display hote hain. `clear: both` ki wajah se footer dono floated elements ke neeche appear hota hai.

### Example 3: Horizontal Navigation Menu
Is example mein `float` ka use navigation items ko horizontally align karne ke liye kiya gaya hai. `clear` content ko navigation menu ke neeche position karta hai.

**HTML**:
```html
<div class="nav-container">
  <ul class="nav">
    <li><a href="#">Home</a></li>
    <li><a href="#">About</a></li>
    <li><a href="#">Services</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
  <div class="clear content">Main content starts here.</div>
</div>
```

**CSS**:
```css
.nav {
  list-style: none;
  padding: 0;
  margin: 0;
}

.nav li {
  float: left;
  margin-right: 10px;
}

.nav a {
  display: block;
  padding: 10px;
  background: #ddd;
  text-decoration: none;
}

.clear {
  clear: both;
}

.nav-container {
  width: 500px;
  border: 1px solid #ccc;
  padding: 10px;
}
```

**Result**: Navigation items horizontally align hote hain, aur `clear: both` ki wajah se neeche ka content ek nayi line se start hota hai.

## Additional Notes
- **Parent Collapse**: Jab saare child elements floated hote hain, to parent container collapse ho sakta hai, yaani uski height lose ho sakti hai. Is problem ko fix karne ke liye `overflow: auto` ya clearfix hack ka use karo, jaise `.clearfix::after { content: ""; display: block; clear: both; }`.
- **Accessibility**: Ensure karo ki floated layouts screen reader ke flow ya responsive designs ko disturb na karein.
- **Modern Alternatives**: Complex layouts ke liye Flexbox ya CSS Grid consider karo, kyunki `float` primarily text wrapping ke liye design kiya gaya tha.
- **Browser Support**: `float` aur `clear` dono sabhi modern browsers mein supported hain.