# CSS 3D Transform Properties 

Yeh guide CSS 3D transform properties (`perspective`, `translate3d()`, `scale3d()`, `rotateX()`, `rotateY()`, `rotateZ()`, `rotate3d()`, aur `matrix3d()`) ko cover karti hai. Isme har value ki detailed description, har property ke do examples, aur external CSS file (`styles.css`) mein defined styles shamil hain. Har example mein class ke sath HTML aur external stylesheet se corresponding CSS di gayi hai. `perspective` property ko 3D effects enable karne ke liye include kiya gaya hai, kyunki yeh 3D rendering space ki depth ko define karti hai.

In examples ko use karne ke liye, ek HTML file banayein aur external CSS file ko is tarah link karein:

```html
<link rel="stylesheet" href="styles.css">
```

**Note**: 3D transforms sahi se dikhne ke liye, parent element ko aksar ek `perspective` value ki zaroorat hoti hai, aur element ko 3D positioning maintain rakhne ke liye `transform-style: preserve-3d` ki zaroorat ho sakti hai.

## 1. `perspective`
`perspective` property viewer se 3D element ki distance define karti hai, jo 3D effect ki intensity ko control karti hai. Yeh aksar parent element par apply ki jaati hai.

### Description of Values
- **Length**: Viewer se z=0 plane ki distance specify karti hai. Chhoti values (jaise `500px`) stronger 3D effects create karti hain, jabki badi values (jaise `2000px`) subtler effects create karti hain. Pixels ya dusre length units mein measure kiya jata hai. Value `0` ya `none` hone par 3D effect disable ho jata hai.
- **Syntax**: `perspective: length | none;` (jaise `perspective: 500px`).
- **Applied To**: Usually parent element par apply hoti hai taaki child elements ke liye ek 3D space create ho sake. Individual elements ke liye `transform` property ke andar `perspective()` function mein bhi use ki ja sakti hai.
- **Inheritance**: Inherit nahi hota; parent ke perspective ko adopt karne ke liye `inherit` ka use karein.

### Example 1: Parent with Perspective
**HTML:**
```html
<div class="perspective-example1">
  <div class="inner">Box with perspective 500px</div>
</div>
```

**CSS (styles.css):**
```css
.perspective-example1 {
  perspective: 500px; /* Strong 3D effect */
}
.perspective-example1 .inner {
  transform: rotateY(45deg);
  width: 100px;
  height: 100px;
  background-color: #3498db;
  color: white;
  padding: 10px;
}
```

### Example 2: Parent with Larger Perspective
**HTML:**
```html
<div class="perspective-example2">
  <div class="inner">Box with perspective 1000px</div>
</div>
```

**CSS (styles.css):**
```css
.perspective-example2 {
  perspective: 1000px; /* Subtler 3D effect */
}
.perspective-example2 .inner {
  transform: rotateY(45deg);
  width: 100px;
  height: 100px;
  background-color: #e74c3c;
  color: white;
  padding: 10px;
}
```

## 2. `translate3d()`
`translate3d()` function kisi element ko 3D space mein x, y, aur z axes ke along move karta hai.

### Description of Values
- **X-axis**: Horizontal displacement. Positive values (jaise `50px`) right move karti hain, negative values left move karti hain. Length units accept karta hai (jaise `px`, `%`, `rem`).
- **Y-axis**: Vertical displacement. Positive values (jaise `50px`) down move karti hain, negative values up move karti hain.
- **Z-axis**: Depth displacement. Positive values (jaise `50px`) viewer ki taraf move karti hain, negative values door move karti hain. Visible hone ke liye `perspective` ki zaroorat hoti hai.
- **Syntax**: `translate3d(x, y, z)` (jaise `translate3d(50px, 20px, 30px)`).
- **Inheritance**: Inherit nahi hota; parent ke transform ko adopt karne ke liye `inherit` ka use karein.

### Example 1: Translate in 3D Space
**HTML:**
```html
<div class="perspective-parent">
  <div class="translate3d-example1">Translated 50px right, 20px down, 30px forward</div>
</div>
```

**CSS (styles.css):**
```css
.perspective-parent {
  perspective: 500px;
}
.translate3d-example1 {
  transform: translate3d(50px, 20px, 30px);
  width: 100px;
  height: 100px;
  background-color: #2ecc71;
  color: white;
  padding: 10px;
}
```

### Example 2: Translate Away in 3D
**HTML:**
```html
<div class="perspective-parent">
  <div class="translate3d-example2">Translated 0px, 0px, -50px</div>
</div>
```

**CSS (styles.css):**
```css
.perspective-parent {
  perspective: 500px;
}
.translate3d-example2 {
  transform: translate3d(0, 0, -50px);
  width: 100px;
  height: 100px;
  background-color: #f1c40f;
  color: black;
  padding: 10px;
}
```

## 3. `scale3d()`
`scale3d()` function kisi element ko 3D space mein x, y, aur z axes ke along scale karta hai.

### Description of Values
- **X-axis Scale**: Horizontal scaling ke liye unitless number. Values > 1 (jaise `2`) stretch karti hain, < 1 (jaise `0.5`) shrink karti hain, `1` se koi change nahi hota, negative values flip karti hain (jaise `-1`).
- **Y-axis Scale**: Vertical scaling ke liye unitless number.
- **Z-axis Scale**: Depth scaling ke liye unitless number. Z-axis ke along element size ko affect karta hai; visible hone ke liye `perspective` ki zaroorat hoti hai.
- **Syntax**: `scale3d(x, y, z)` (jaise `scale3d(1.5, 1, 2)`).
- **Inheritance**: Inherit nahi hota; parent ke transform ko adopt karne ke liye `inherit` ka use karein.

### Example 1: Scale in 3D
**HTML:**
```html
<div class="perspective-parent">
  <div class="scale3d-example1">Scaled 1.5x x-axis, 1x y-axis, 2x z-axis</div>
</div>
```

**CSS (styles.css):**
```css
.perspective-parent {
  perspective: 500px;
}
.scale3d-example1 {
  transform: scale3d(1.5, 1, 2);
  width: 100px;
  height: 100px;
  background-color: #9b59b6;
  color: white;
  padding: 10px;
}
```

### Example 2: Scale with Z-Axis Shrink
**HTML:**
```html
<div class="perspective-parent">
  <div class="scale3d-example2">Scaled 1x x-axis, 0.8x y-axis, 0.5x z-axis</div>
</div>
```

**CSS (styles.css):**
```css
.perspective-parent {
  perspective: 500px;
}
.scale3d-example2 {
  transform: scale3d(1, 0.8, 0.5);
  width: 100px;
  height: 100px;
  background-color: #1abc9c;
  color: white;
  padding: 10px;
}
```

## 4. `rotateX()`
`rotateX()` function kisi element ko x-axis (horizontal axis) ke charon taraf rotate karta hai, jisse ek flipping effect milta hai.

### Description of Values
- **Angle**: Rotation angle specify karta hai. Positive values (jaise `45deg`) top edge ko door rotate karti hain, negative values (jaise `-45deg`) top edge ko viewer ki taraf rotate karti hain. `deg`, `rad`, `turn` accept karta hai.
- **Syntax**: `rotateX(angle)` (jaise `rotateX(45deg)`).
- **Inheritance**: Inherit nahi hota; parent ke transform ko adopt karne ke liye `inherit` ka use karein.

### Example 1: RotateX Forward
**HTML:**
```html
<div class="perspective-parent">
  <div class="rotatex-example1">Rotated 45 degrees around x-axis</div>
</div>
```

**CSS (styles.css):**
```css
.perspective-parent {
  perspective: 500px;
}
.rotatex-example1 {
  transform: rotateX(45deg);
  width: 100px;
  height: 100px;
  background-color: #e67e22;
  color: white;
  padding: 10px;
}
```

### Example 2: RotateX Backward
**HTML:**
```html
<div class="perspective-parent">
  <div class="rotatex-example2">Rotated -45 degrees around x-axis</div>
</div>
```

**CSS (styles.css):**
```css
.perspective-parent {
  perspective: 500px;
}
.rotatex-example2 {
  transform: rotateX(-45deg);
  width: 100px;
  height: 100px;
  background-color: #34495e;
  color: white;
  padding: 10px;
}
```

## 5. `rotateY()`
`rotateY()` function kisi element ko y-axis (vertical axis) ke charon taraf rotate karta hai, jisse side-to-side flipping effect milta hai.

### Description of Values
- **Angle**: Rotation angle specify karta hai. Positive values (jaise `45deg`) right edge ko door rotate karti hain, negative values (jaise `-45deg`) right edge ko viewer ki taraf rotate karti hain. `deg`, `rad`, `turn` accept karta hai.
- **Syntax**: `rotateY(angle)` (jaise `rotateY(45deg)`).
- **Inheritance**: Inherit nahi hota; parent ke transform ko adopt karne ke liye `inherit` ka use karein.

### Example 1: RotateY Right
**HTML:**
```html
<div class="perspective-parent">
  <div class="rotatey-example1">Rotated 45 degrees around y-axis</div>
</div>
```

**CSS (styles.css):**
```css
.perspective-parent {
  perspective: 500px;
}
.rotatey-example1 {
  transform: rotateY(45deg);
  width: 100px;
  height: 100px;
  background-color: #c0392b;
  color: white;
  padding: 10px;
}
```

### Example 2: RotateY Left
**HTML:**
```html
<div class="perspective-parent">
  <div class="rotatey-example2">Rotated -45 degrees around y-axis</div>
</div>
```

**CSS (styles.css):**
```css
.perspective-parent {
  perspective: 500px;
}
.rotatey-example2 {
  transform: rotateY(-45deg);
  width: 100px;
  height: 100px;
  background-color: #8e44ad;
  color: white;
  padding: 10px;
}
```

## 6. `rotateZ()`
`rotateZ()` function kisi element ko z-axis (screen ke perpendicular) ke charon taraf rotate karta hai, jo 2D rotation ki tarah hi hota hai.

### Description of Values
- **Angle**: Rotation angle specify karta hai. Positive values (jaise `45deg`) clockwise rotate karti hain, negative values (jaise `-45deg`) counterclockwise rotate karti hain. `deg`, `rad`, `turn` accept karta hai.
- **Syntax**: `rotateZ(angle)` (jaise `rotateZ(45deg)`).
- **Inheritance**: Inherit nahi hota; parent ke transform ko adopt karne ke liye `inherit` ka use karein.

### Example 1: RotateZ Clockwise
**HTML:**
```html
<div class="perspective-parent">
  <div class="rotatez-example1">Rotated 45 degrees around z-axis</div>
</div>
```

**CSS (styles.css):**
```css
.perspective-parent {
  perspective: 500px;
}
.rotatez-example1 {
  transform: rotateZ(45deg);
  width: 100px;
  height: 100px;
  background-color: #27ae60;
  color: white;
  padding: 10px;
}
```

### Example 2: RotateZ Counterclockwise
**HTML:**
```html
<div class="perspective-parent">
  <div class="rotatez-example2">Rotated -45 degrees around z-axis</div>
</div>
```

**CSS (styles.css):**
```css
.perspective-parent {
  perspective: 500px;
}
.rotatez-example2 {
  transform: rotateZ(-45deg);
  width: 100px;
  height: 100px;
  background-color: #d35400;
  color: white;
  padding: 10px;
}
```

## 7. `rotate3d()`
`rotate3d()` function kisi element ko x, y, aur z components dwara defined ek custom 3D axis ke charon taraf rotate karta hai.

### Description of Values
- **X-vector**: Rotation axis ke x-component ko define karne wala unitless number (jaise x-axis ke liye `1`).
- **Y-vector**: Rotation axis ke y-component ko define karne wala unitless number (jaise koi y-axis contribution na hone par `0`).
- **Z-vector**: Rotation axis ke z-component ko define karne wala unitless number (jaise koi z-axis contribution na hone par `0`).
- **Angle**: Defined axis ke charon taraf rotation angle specify karta hai. Positive values ek direction mein rotate karti hain, negative opposite direction mein. `deg`, `rad`, `turn` accept karta hai.
- **Syntax**: `rotate3d(x, y, z, angle)` (jaise diagonal x-y axis ke charon taraf rotation ke liye `rotate3d(1, 1, 0, 45deg)`).
- **Inheritance**: Inherit nahi hota; parent ke transform ko adopt karne ke liye `inherit` ka use karein.

### Example 1: Rotate3d Diagonal Axis
**HTML:**
```html
<div class="perspective-parent">
  <div class="rotate3d-example1">Rotated 45 degrees around x-y axis</div>
</div>
```

**CSS (styles.css):**
```css
.perspective-parent {
  perspective: 500px;
}
.rotate3d-example1 {
  transform: rotate3d(1, 1, 0, 45deg);
  width: 100px;
  height: 100px;
  background-color: #16a085;
  color: white;
  padding: 10px;
}
```

### Example 2: Rotate3d Custom Axis
**HTML:**
```html
<div class="perspective-parent">
  <div class="rotate3d-example2">Rotated -60 degrees around x-z axis</div>
</div>
```

**CSS (styles.css):**
```css
.perspective-parent {
  perspective: 500px;
}
.rotate3d-example2 {
  transform: rotate3d(1, 0, 1, -60deg);
  width: 100px;
  height: 100px;
  background-color: #8d5524;
  color: white;
  padding: 10px;
}
```

## Notes
- CSS code ko `styles.css` naam ki file mein save karein aur ise `<link rel="stylesheet" href="styles.css">` ka use karke apne HTML se link karein.
- **General Notes**:
  - Depth create karne ke liye 3D transforms ko ek `perspective` value ki zaroorat hoti hai (parent par ya `transform` ke andar `perspective()` ke zariye).
  - Agar child elements ko 3D positioning maintain rakhni hai, toh parent elements par `transform-style: preserve-3d` ka use karein.
  - `transform-origin` property (jaise `transform-origin: center`) rotations aur scaling ke liye pivot point ko adjust karti hai.
  - Elements ke charon taraf kafi space rakhein taaki clipping se bacha ja sake, khas karke `rotateX()`, `rotateY()`, ya `translate3d()` ke liye.
- **For `perspective`**:
  - Chhoti values (jaise `500px`) dramatic 3D effects create karti hain; badi values (jaise `2000px`) subtler hoti hain.
  - Saare children mein consistent 3D space ke liye ise parent element par apply karein.
- **For `translate3d()`**: Elements ko 3D mein move karta hai; z-axis effects sirf `perspective` ke sath hi dikhte hain.
- **For `scale3d()`**: 3D mein scale karta hai; z-axis scaling `perspective` ke sath depth perception ko affect karti hai.
- **For `rotateX()`, `rotateY()`, `rotateZ()`**: Specific axes ke charon taraf rotate karta hai; `rotateZ()` 2D `rotate()` ke barabar hota hai.
- **For `rotate3d()`**: Rotation ke liye ek custom axis define karta hai; axis-specific rotations ke liye x, y, z components ko `1` ya `0` par set karein.
- Browsers par 3D transforms ko test karein, kyunki rendering aur performance alag ho sakti hai (zaroorat padne par older browsers ke liye `-webkit-transform` ka use karein).
- Readability ka dhyan rakhein; zyada rotations ya scaling text ko distort kar sakte hain.
- Accessibility ke liye, critical content ke liye sirf 3D effects par depend hone se bachein, kyunki ho sakta hai ki yeh sabhi devices par render na ho.