# CSS Units

CSS units ka use `width`, `height`, `font-size`, `margin`, `padding` aur doosri properties ki measurements define karne ke liye hota hai. Ye absolute (fixed) ya relative (context par depend karne wale) ho sakte hain. Neeche CSS units ke alag-alag types define kiye gaye hain, aur har type ke baad 3 se 4 practical examples diye gaye hain.

## 1. Absolute Units

### Definition

Absolute units fixed measurements hoti hain, jo doosre elements ya viewport ke size ke saath change nahi hoti hain. Ye print layouts ya un situations mein useful hoti hain jahan precise sizes ki zaroorat hoti hai. Common absolute units mein `px` (pixels), `cm` (centimeters), `mm` (millimeters), aur `in` (inches) shamil hain.

### Examples

#### Example 1: Font Size ke liye Pixels (px) ka Use

**HTML**

```html
<p class="pixel-font">This text is in pixels.</p>
```

**CSS**

```css
.pixel-font {
  font-size: 16px;
}
```

**Result**: Text fixed 16 pixels ke size mein display hota hai.

#### Example 2: Width ke liye Centimeters (cm) ka Use

**HTML**

```html
<div class="cm-box">Box</div>
```

**CSS**

```css
.cm-box {
  width: 5cm;
  height: 2cm;
  background-color: #007BFF;
}
```

**Result**: Box ki width fixed 5 centimeters aur height 2 centimeters hoti hai.

#### Example 3: Margin ke liye Millimeters (mm) ka Use

**HTML**

```html
<div class="mm-margin">Content</div>
```

**CSS**

```css
.mm-margin {
  margin: 10mm;
  border: 1px solid #000;
}
```

**Result**: Div ke chaaron taraf fixed 10-millimeter margin hota hai.

#### Example 4: Padding ke liye Inches (in) ka Use

**HTML**

```html
<div class="inch-padding">Padded Content</div>
```

**CSS**

```css
.inch-padding {
  padding: 0.5in;
  background-color: #28a745;
}
```

**Result**: Div ke chaaron taraf fixed 0.5-inch padding hoti hai.

## 2. Relative Units: Viewport-Based

### Definition

Viewport-based relative units browser window ke size ke according scale hoti hain. Common units mein `vw` (viewport width), `vh` (viewport height), `vmin` (viewport width aur height mein se chhoti value), aur `vmax` (viewport width aur height mein se badi value) shamil hain.

### Examples

#### Example 1: Font Size ke liye Viewport Width (vw) ka Use

**HTML**

```html
<h1 class="vw-font">Responsive Heading</h1>
```

**CSS**

```css
.vw-font {
  font-size: 5vw;
}
```

**Result**: Heading ka font size viewport ki width ka 5% hota hai aur browser window ke size ke saath change hota hai.

#### Example 2: Div ki Height ke liye Viewport Height (vh) ka Use

**HTML**

```html
<div class="vh-box">Full Height Box</div>
```

**CSS**

```css
.vh-box {
  height: 50vh;
  background-color: #dc3545;
}
```

**Result**: Div ki height viewport ki height ka 50% hoti hai.

#### Example 3: Square Box ke liye Viewport Minimum (vmin) ka Use

**HTML**

```html
<div class="vmin-box">Square Box</div>
```

**CSS**

```css
.vmin-box {
  width: 20vmin;
  height: 20vmin;
  background-color: #ffc107;
}
```

**Result**: Box ki width aur height viewport ki chhoti dimension (width ya height) ka 20% hoti hain, jiski wajah se box square shape mein rehta hai.

#### Example 4: Border Width ke liye Viewport Maximum (vmax) ka Use

**HTML**

```html
<div class="vmax-border">Bordered Content</div>
```

**CSS**

```css
.vmax-border {
  border: 1vmax solid #17a2b8;
  padding: 10px;
}
```

**Result**: Border ki thickness viewport ki badi dimension ka 1% hoti hai.

## 3. Relative Units: Font-Based

### Definition

Font-based relative units font size ke according scale hoti hain. Ye element ke apne font size ya uske parent ke font size par depend kar sakti hain. Common units mein `rem` (root element ka font size), `em` (element ke context mein font size), aur `ex` (font mein letter 'x' ki height) shamil hain.

### Examples

#### Example 1: Consistent Spacing ke liye rem ka Use

**HTML**

```html
<div class="rem-spacing">
  <p>Paragraph 1</p>
  <p>Paragraph 2</p>
</div>
```

**CSS**

```css
html {
  font-size: 16px;
}
.rem-spacing p {
  margin-bottom: 1.5rem;
}
```

**Result**: Paragraphs ke beech neeche ki taraf margin root font size ka 1.5 guna (24px) hota hai.

#### Example 2: Element-Specific Scaling ke liye em ka Use

**HTML**

```html
<div class="em-font">
  <p>Text with padding</p>
</div>
```

**CSS**

```css
.em-font {
  font-size: 20px;
}
.em-font p {
  padding: 1em;
}
```

**Result**: Paragraph ki padding 20px hoti hai, kyunki `1em` parent ke font size ke according calculate hota hai.

#### Example 3: Line Height ke liye ex ka Use

**HTML**

```html
<p class="ex-line">This is a test line.</p>
```

**CSS**

```css
.ex-line {
  line-height: 2ex;
}
```

**Result**: Line height font mein letter 'x' ki height ka do guna hoti hai.

#### Example 4: rem aur em ko Combine karna

**HTML**

```html
<div class="combo-font">
  <p>Scaled text</p>
</div>
```

**CSS**

```css
html {
  font-size: 16px;
}
.combo-font {
  font-size: 1.5rem; /* 24px */
}
.combo-font p {
  margin-left: 2em; /* 48px, based on parent's font-size */
}
```

**Result**: Paragraph ka left margin 48px hota hai, jo uske parent ke font size ke according scale hota hai.

## 4. Relative Units: Percentage-Based

### Definition

Percentage-based units (`%`) parent element ke dimensions ya properties, jaise `width`, `height`, ya `font-size`, ke according calculate hoti hain. Ye responsive designs ke liye useful hain, kyunki ye parent ke context ke according adjust hoti hain. `width` ya `height` jaisi properties ke liye percentage parent ki corresponding dimension par depend karti hai. `font-size` jaisi properties ke liye percentage parent ke font size par depend karti hai.

### Examples

#### Example 1: Responsive Width ke liye Percentage ka Use

**HTML**

```html
<div class="parent">
  <div class="percent-width">Child Div</div>
</div>
```

**CSS**

```css
.parent {
  width: 600px;
  background-color: #e9ecef;
}
.percent-width {
  width: 80%;
  background-color: #6f42c1;
  padding: 10px;
}
```

**Result**: Child div ki width 480px hoti hai, jo parent ki 600px width ka 80% hai. Iska background purple hota hai.

#### Example 2: Container mein Height ke liye Percentage ka Use

**HTML**

```html
<div class="parent-height">
  <div class="percent-height">Child Content</div>
</div>
```

**CSS**

```css
.parent-height {
  height: 200px;
  background-color: #dee2e6;
}
.percent-height {
  height: 50%;
  background-color: #fd7e14;
}
```

**Result**: Child div ki height 100px hoti hai, jo parent ki 200px height ka 50% hai. Iska background orange hota hai.

#### Example 3: Font Size Scaling ke liye Percentage ka Use

**HTML**

```html
<div class="percent-font">
  <p>Larger Text</p>
</div>
```

**CSS**

```css
.percent-font {
  font-size: 24px;
}
.percent-font p {
  font-size: 125%;
}
```

**Result**: Paragraph ka font size 30px hota hai, jo parent ke 24px font size ka 125% hai.

#### Example 4: Parent Width ke According Padding ke liye Percentage ka Use

**HTML**

```html
<div class="percent-padding">
  <p>Padded Content</p>
</div>
```

**CSS**

```css
.percent-padding {
  width: 400px;
  background-color: #f8f9fa;
}
.percent-padding p {
  padding: 5%;
}
```

**Result**: Paragraph ki padding chaaron taraf 20px hoti hai, jo parent ki 400px width ka 5% hai.

## Browser Support

Upar bataye gaye sabhi CSS units modern browsers, jaise Chrome, Firefox, Safari aur Edge, mein supported hain. Kuch purane browsers mein `vmin`, `vmax`, ya `ex` ka support limited ho sakta hai, isliye testing karna recommended hai.
