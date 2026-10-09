# CSS Specificity

CSS specificity yeh tay karti hai ki jab multiple CSS rules ek hi element ko target karte hain, tab kaun sa rule apply hoga. Specificity calculation selector ke type par depend karti hai—jitna zyada specific selector hoga, uski precedence utni hi zyada hogi. Agar do selectors ki specificity same hoti hai, toh CSS file mein last wala rule jeet jata hai.

Niche alag-alag tarah ke CSS specificity rules define kiye gaye hain, aur har ek ke baad 3 se 4 practical examples diye gaye hain.

## 1. Element Selectors
### Definition
Element selectors HTML elements (jaise `p`, `div`, `h1`) ko target karte hain aur inka specificity score sabse kam (0,0,0,1) hota hai. Yeh sabse kam specific hote hain aur inhe dusre selector types se aasan se override kiya ja sakta hai.

### Examples
#### Example 1: Styling All Paragraphs
**HTML**
```html
<p>Text</p>
```
**CSS**
```css
p {
  color: blue;
}
```
**Result**: Saare `<p>` elements blue ho jate hain. Specificity: (0,0,0,1).

#### Example 2: Styling Divs
**HTML**
```html
<div>Content</div>
```
**CSS**
```css
div {
  background-color: #f0f0f0;
}
```
**Result**: Saare `<div>` elements ka background light gray ho jata hai. Specificity: (0,0,0,1).

#### Example 3: Styling Headings
**HTML**
```html
<h1>Title</h1>
```
**CSS**
```css
h1 {
  font-size: 24px;
}
```
**Result**: Saare `<h1>` elements ka font size 24px ho jata hai. Specificity: (0,0,0,1).

#### Example 4: Styling List Items
**HTML**
```html
<li>Item</li>
```
**CSS**
```css
li {
  margin-left: 20px;
}
```
**Result**: Saare `<li>` elements par 20px ka left margin lag jata hai. Specificity: (0,0,0,1).

## 2. Class, Attribute, and Pseudo-Class Selectors
### Definition
Class selectors (`.class`), attribute selectors (`[attribute]`), aur pseudo-classes (jaise `:hover`, `:first-child`) ki specificity element selectors se zyada (0,0,1,0) hoti hai. Yeh specific classes, attributes, ya states wale elements ko target karte hain.

### Examples
#### Example 1: Styling a Specific Class
**HTML**
```html
<p class="highlight">Highlighted text</p>
<p>Regular text</p>
```
**CSS**
```css
.highlight {
  background-color: yellow;
}
p {
  background-color: gray;
}
```
**Result**: Jis `<p>` par class `highlight` hai woh yellow ho jata hai, jo element selector ke gray background ko override kar deta hai. Specificity: (0,0,1,0) vs (0,0,0,1).

#### Example 2: Styling with Attribute Selector
**HTML**
```html
<input type="text" placeholder="Enter text">
<input type="password">
```
**CSS**
```css
input[type="text"] {
  border: 2px solid #007BFF;
}
input {
  border: 1px solid black;
}
```
**Result**: Text inputs par blue border lag jata hai, jo generic input ke black border ko override kar deta hai. Specificity: (0,0,1,0) vs (0,0,0,1).

#### Example 3: Styling with Pseudo-Class
**HTML**
```html
<a href="#">Link</a>
```
**CSS**
```css
a:hover {
  color: red;
}
a {
  color: blue;
}
```
**Result**: Hover karne par link red ho jata hai, jo default blue color ko override karta hai. Specificity: (0,0,1,0) vs (0,0,0,1).

#### Example 4: Styling with Multiple Classes
**HTML**
```html
<div class="box primary">Box</div>
<div class="box">Regular Box</div>
```
**CSS**
```css
.box.primary {
  background-color: #28a745;
}
.box {
  background-color: #dee2e6;
}
```
**Result**: Jis div mein `box` aur `primary` dono classes hain woh green ho jata hai, jo gray background ko override karta hai. Specificity: (0,0,2,0) vs (0,0,1,0).

## 3. ID Selectors
### Definition
ID selectors (`#id`) un elements ko target karte hain jinme specific `id` attribute hota hai. Inki specificity class ya element selectors se zyada (0,1,0,0) hoti hai. Yeh zyada specific hote hain par code flexibility banaye rakhne ke liye inka kam use karna chahiye.

### Examples
#### Example 1: Styling a Specific ID
**HTML**
```html
<div id="header">Header</div>
<div>Content</div>
```
**CSS**
```css
#header {
  background-color: #dc3545;
}
div {
  background-color: #f8f9fa;
}
```
**Result**: Jis div mein `id="header"` hai woh red ho jata hai, jo generic div ke background ko override karta hai. Specificity: (0,1,0,0) vs (0,0,0,1).

#### Example 2: Styling an ID with Pseudo-Class
**HTML**
```html
<button id="submit-btn">Submit</button>
```
**CSS**
```css
#submit-btn:hover {
  background-color: #007BFF;
}
button {
  background-color: #6c757d;
}
```
**Result**: `id="submit-btn"` wala button hover karne par blue ho jata hai, jo default gray ko override karta hai. Specificity: (0,1,1,0) vs (0,0,0,1).

#### Example 3: Combining ID and Class
**HTML**
```html
<div id="content" class="main">Main Content</div>
```
**CSS**
```css
#content.main {
  border: 3px solid #ffc107;
}
div {
  border: 1px solid black;
}
```
**Result**: `id="content"` aur class `main` wale div par yellow border aa jata hai, jo black border ko override karta hai. Specificity: (0,1,1,0) vs (0,0,0,1).

#### Example 4: ID Overriding Class
**HTML**
```html
<p id="special" class="text">Special Text</p>
```
**CSS**
```css
#special {
  color: purple;
}
.text {
  color: green;
}
```
**Result**: `id="special"` wala paragraph purple ho jata hai, jo class ke green color ko override karta hai. Specificity: (0,1,0,0) vs (0,0,1,0).

## 4. Inline Styles and !important
### Definition
Inline styles (jo HTML element ke `style` attribute mein likhe jaate hain) ki specificity sabse zyada (1,0,0,0) hoti hai, bas tab nahi jab unhe `!important` se override kiya jaye. `!important` sabhi dusre rules par bhari padta hai, par iska use dhyan se karna chahiye kyunki yeh debugging ko mushkil bana deta hai.

### Examples
#### Example 1: Inline Style
**HTML**
```html
<p style="color: red;">Inline styled text</p>
```
**CSS**
```css
p {
  color: blue;
}
```
**Result**: Paragraph inline style ki wajah se red rehta hai, jo CSS rule ko override karta hai. Specificity: (1,0,0,0) vs (0,0,0,1).

#### Example 2: Using !important
**HTML**
```html
<p class="highlight">Important text</p>
```
**CSS**
```css
.highlight {
  color: green !important;
}
p {
  color: blue;
}
```
**Result**: Paragraph `!important` ki wajah se green ho jata hai, jo element selector ko override kar deta hai. Specificity: `!important` beats (0,0,0,1).

#### Example 3: Inline Style vs Class
**HTML**
```html
<div class="box" style="background-color: yellow;">Inline Box</div>
```
**CSS**
```css
.box {
  background-color: gray;
}
```
**Result**: Div ka background inline style ki wajah se yellow rehta hai, jo class ko override karta hai. Specificity: (1,0,0,0) vs (0,0,1,0).

#### Example 4: !important vs Inline Style
**HTML**
```html
<p style="color: red;" class="urgent">Urgent Text</p>
```
**CSS**
```css
.urgent {
  color: purple !important;
}
```
**Result**: Paragraph `!important` ki wajah se purple ho jata hai, jo inline style ko bhi override kar deta hai. Specificity: `!important` beats (1,0,0,0).

## Specificity Calculation
Specificity ko chaar hissron ke value (a,b,c,d) se calculate kiya jata hai:
- **a**: Inline styles (inline hai toh 1, nahi toh 0).
- **b**: ID selectors ki sankhya (number).
- **c**: Class, attribute, ya pseudo-class selectors ki sankhya.
- **d**: Element ya pseudo-element selectors ki sankhya.

Jaise ki:
- `p`: (0,0,0,1)
- `.class`: (0,0,1,0)
- `#id`: (0,1,0,0)
- `#id .class p`: (0,1,1,1)
- Inline style: (1,0,0,0)
- `!important`: Sabhi rules ko override kar deta hai jab tak ki dusra `!important` zyada specificity wala na ho.

## Browser Support
CSS specificity ke rules sabhi modern browsers mein support hote hain, jaise Chrome, Firefox, Safari, aur Edge.