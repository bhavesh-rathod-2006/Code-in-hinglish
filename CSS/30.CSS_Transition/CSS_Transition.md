# CSS Transition Properties

Yeh guide CSS transition properties (`transition`, `transition-delay`, `transition-duration`, `transition-property`, aur `transition-timing-function`) ko cover karti hai. Isme har value ki detailed description, har property ke do examples, aur external CSS file (`styles.css`) mein defined styles shamil hain. Har example mein class ke sath HTML aur external stylesheet se corresponding CSS di gayi hai. Transitions ka use CSS properties mein hone wale changes ko ek specified duration mein smoothly animate karne ke liye kiya jata hai.

In examples ko use karne ke liye, ek HTML file banayein aur external CSS file ko is tarah link karein:

```html
<link rel="stylesheet" href="styles.css">
```

**Note**: Animation ko trigger karne ke liye transitions ko state change (jaise `:hover`, `:focus`) ki zaroorat hoti hai. Niche diye gaye examples effects dikhane ke liye `:hover` ka use karte hain.

## 1. `transition`
`transition` shorthand property `transition-property`, `transition-duration`, `transition-timing-function`, aur `transition-delay` ko ek hi declaration mein combine karti hai.

### Description of Values
- **Property**: Transition hone wali CSS property ko specify karti hai (jaise `background-color`, `width`, ya sabhi animatable properties ke liye `all`).
- **Duration**: Transition mein lagne wale time ko set karti hai (jaise 0.5 seconds ke liye `0.5s`, milliseconds ke liye `500ms`).
- **Timing Function**: Transition ki speed curve ko define karti hai (jaise `ease`, `linear`, `ease-in`, `ease-out`, `ease-in-out`, ya `cubic-bezier(n,n,n,n)`).
- **Delay** (optional): Transition start hone se pehle ka delay set karti hai (jaise `0.2s`). Agar omit kiya jaye, toh default `0s` hota hai.
- **Multiple Transitions**: Multiple transitions ko comma se separate karein (jaise `width 0.5s ease, opacity 0.3s linear`).
- **Syntax**: `transition: property duration timing-function delay;` (jaise `transition: width 0.5s ease 0.2s;`).
- **Inheritance**: Inherit nahi hota; parent ke transition ko adopt karne ke liye `inherit` ka use karein.

### Example 1: Transition Background Color
**HTML:**
```html
<div class="transition-example1">Hover to change background color</div>
```

**CSS (styles.css):**
```css
.transition-example1 {
  width: 100px;
  height: 100px;
  background-color: #3498db;
  color: white;
  padding: 10px;
  transition: background-color 0.5s ease; /* Transition background-color over 0.5s */
}
.transition-example1:hover {
  background-color: #e74c3c;
}
```

### Example 2: Multiple Transitions
**HTML:**
```html
<div class="transition-example2">Hover to change width and opacity</div>
```

**CSS (styles.css):**
```css
.transition-example2 {
  width: 100px;
  height: 100px;
  background-color: #2ecc71;
  color: white;
  padding: 10px;
  opacity: 1;
  transition: width 0.5s ease-in, opacity 0.3s linear; /* Transition width and opacity */
}
.transition-example2:hover {
  width: 150px;
  opacity: 0.5;
}
```

## 2. `transition-delay`
`transition-delay` property transition start hone se pehle wait karne ka time specify karti hai.

### Description of Values
- **Time**: Delay ko seconds (jaise `0.2s`) ya milliseconds (jaise `200ms`) mein specify karti hai. Negative values transition ko turant start kar deti hain par uske kuch part ko skip kar deti hain.
- **Multiple Delays**: Multiple transitions ke liye delays ko comma se separate karein (jaise `0.2s, 0.5s`).
- **Syntax**: `transition-delay: time;` (jaise `transition-delay: 0.2s;`).
- **Inheritance**: Inherit nahi hota; parent ke transition-delay ko adopt karne ke liye `inherit` ka use karein.

### Example 1: Delayed Width Transition
**HTML:**
```html
<div class="transition-delay-example1">Hover to change width after delay</div>
```

**CSS (styles.css):**
```css
.transition-delay-example1 {
  width: 100px;
  height: 100px;
  background-color: #9b59b6;
  color: white;
  padding: 10px;
  transition-property: width;
  transition-duration: 0.5s;
  transition-delay: 0.2s; /* 0.2s delay before width transition */
}
.transition-delay-example1:hover {
  width: 150px;
}
```

### Example 2: Delayed Opacity Transition
**HTML:**
```html
<div class="transition-delay-example2">Hover to fade after delay</div>
```

**CSS (styles.css):**
```css
.transition-delay-example2 {
  width: 100px;
  height: 100px;
  background-color: #1abc9c;
  color: white;
  padding: 10px;
  opacity: 1;
  transition-property: opacity;
  transition-duration: 0.3s;
  transition-delay: 0.4s; /* 0.4s delay before opacity transition */
}
.transition-delay-example2:hover {
  opacity: 0.3;
}
```

## 3. `transition-duration`
`transition-duration` property specify karti hai ki transition complete hone mein kitna time lagega.

### Description of Values
- **Time**: Duration ko seconds (jaise `0.5s`) ya milliseconds (jaise `500ms`) mein specify karti hai. `0s` transition ko disable kar deta hai.
- **Multiple Durations**: Multiple transitions ke liye durations ko comma se separate karein (jaise `0.5s, 0.3s`).
- **Syntax**: `transition-duration: time;` (jaise `transition-duration: 0.5s;`).
- **Inheritance**: Inherit nahi hota; parent ke transition-duration ko adopt karne ke liye `inherit` ka use karein.

### Example 1: Slow Width Transition
**HTML:**
```html
<div class="transition-duration-example1">Hover for slow width change</div>
```

**CSS (styles.css):**
```css
.transition-duration-example1 {
  width: 100px;
  height: 100px;
  background-color: #e67e22;
  color: white;
  padding: 10px;
  transition-property: width;
  transition-duration: 1s; /* 1s duration for width transition */
}
.transition-duration-example1:hover {
  width: 150px;
}
```

### Example 2: Fast Background Transition
**HTML:**
```html
<div class="transition-duration-example2">Hover for fast background change</div>
```

**CSS (styles.css):**
```css
.transition-duration-example2 {
  width: 100px;
  height: 100px;
  background-color: #34495e;
  color: white;
  padding: 10px;
  transition-property: background-color;
  transition-duration: 0.2s; /* 0.2s duration for background-color transition */
}
.transition-duration-example2:hover {
  background-color: #f39c12;
}
```

## 4. `transition-property`
`transition-property` property specify karti hai ki transition ke dauran kin CSS properties ko animate karna hai.

### Description of Values
- **Property Name**: Ek single CSS property specify karti hai (jaise `width`, `background-color`, `opacity`) ya sabhi animatable properties ke liye `all`.
- **Multiple Properties**: Properties ko comma se separate karein (jaise `width, opacity`).
- **None**: Transitions ko disable kar deta hai (`none`).
- **Syntax**: `transition-property: property | all | none;` (jaise `transition-property: width;`).
- **Inheritance**: Inherit nahi hota; parent ke transition-property ko adopt karne ke liye `inherit` ka use karein.

### Example 1: Transition Specific Property (Opacity)
**HTML:**
```html
<div class="transition-property-example1">Hover to fade opacity</div>
```

**CSS (styles.css):**
```css
.transition-property-example1 {
  width: 100px;
  height: 100px;
  background-color: #c0392b;
  color: white;
  padding: 10px;
  opacity: 1;
  transition-property: opacity; /* Only opacity transitions */
  transition-duration: 0.5s;
}
.transition-property-example1:hover {
  opacity: 0.4;
}
```

### Example 2: Transition Multiple Properties
**HTML:**
```html
<div class="transition-property-example2">Hover to change width and color</div>
```

**CSS (styles.css):**
```css
.transition-property-example2 {
  width: 100px;
  height: 100px;
  background-color: #8e44ad;
  color: white;
  padding: 10px;
  transition-property: width, background-color; /* Transition width and background-color */
  transition-duration: 0.5s;
}
.transition-property-example2:hover {
  width: 150px;
  background-color: #27ae60;
}
```

## 5. `transition-timing-function`
`transition-timing-function` property transition ki speed curve ko define karti hai, jo yeh control karti hai ki animation kaise aage badhega.

### Description of Values
- **Predefined Functions**:
  - `ease`: Dhire shuru hota hai, speed pakadta hai, phir dhire ho jata hai (default).
  - `linear`: Poore time same speed rehti hai.
  - `ease-in`: Dhire shuru hota hai, phir speed pakadta hai.
  - `ease-out`: Tej shuru hota hai, phir dhire ho jata hai.
  - `ease-in-out`: Shuru aur end mein dhire rehta hai, beech mein tez hota hai.
- **Cubic Bezier**: `cubic-bezier(x1, y1, x2, y2)` dwara defined custom curve (jaise `cubic-bezier(0.25, 0.1, 0.25, 1)`).
- **Steps**: `steps(n, [start|end])` ka use karke discrete steps (jaise char steps ke liye `steps(4, end)`).
- **Multiple Timing Functions**: Multiple transitions ke liye functions ko comma se separate karein (jaise `ease, linear`).
- **Syntax**: `transition-timing-function: ease | linear | ease-in | ease-out | ease-in-out | cubic-bezier(n,n,n,n) | steps(n, [start|end]);`.
- **Inheritance**: Inherit nahi hota; parent ke transition-timing-function ko adopt karne ke liye `inherit` ka use karein.

### Example 1: Ease-In Timing Function
**HTML:**
```html
<div class="transition-timing-example1">Hover for ease-in width change</div>
```

**CSS (styles.css):**
```css
.transition-timing-example1 {
  width: 100px;
  height: 100px;
  background-color: #16a085;
  color: white;
  padding: 10px;
  transition-property: width;
  transition-duration: 0.5s;
  transition-timing-function: ease-in; /* Slow start, fast finish */
}
.transition-timing-example1:hover {
  width: 150px;
}
```

### Example 2: Cubic Bezier Timing Function
**HTML:**
```html
<div class="transition-timing-example2">Hover for custom bezier opacity change</div>
```

**CSS (styles.css):**
```css
.transition-timing-example2 {
  width: 100px;
  height: 100px;
  background-color: #8d5524;
  color: white;
  padding: 10px;
  opacity: 1;
  transition-property: opacity;
  transition-duration: 0.5s;
  transition-timing-function: cubic-bezier(0.68, -0.55, 0.265, 1.55); /* Bouncy effect */
}
.transition-timing-example2:hover {
  opacity: 0.3;
}
```

## Notes
- CSS code ko `styles.css` naam ki file mein save karein aur ise `<link rel="stylesheet" href="styles.css">` ka use karke apne HTML se link karein.
- **General Notes**:
  - Transitions CSS properties mein hone wale changes ko trigger hone par (jaise `:hover`, `:focus`, ya JavaScript dwara) animate karte hain.
  - Sirf animatable properties (jaise `width`, `opacity`, `background-color`) hi transition ho sakti hain; `display` jaisi properties nahi.
  - Concise code ke liye `transition` shorthand ka use karein, aur correct order dhyan rakhein: `property duration timing-function delay`.
  - Values ko comma se separate karke multiple transitions define kiye ja sakte hain.
- **For `transition-delay`**: Animations ko stagger karne ke liye use karein; negative delays transition ko animation ke beech se shuru karte hain.
- **For `transition-duration`**: Smooth aur user-friendly animations ke liye duration ko reasonable rakhein (jaise `0.3s` se `1s`).
- **For `transition-property`**: Simplicity ke liye `all` specify karein, lekin better performance ke liye specific properties ki list dein.
- **For `transition-timing-function`**: `ease` jaise predefined functions common hain; custom curves ke liye `cubic-bezier` ya frame-like animations ke liye `steps` ka use karein.
- Browsers par transitions ko test karein, kyunki timing functions aur rendering alag ho sakti hai (zaroorat padne par older browsers ke liye `-webkit-transition` ka use karein).
- Dhyan rakhein ki transitions user experience ko behtar banayein bina kisi delay ya distraction ke.
- Accessibility ke liye, critical content ke liye sirf transitions par depend hone se bachein, aur readability ke liye kafi contrast rakhein.