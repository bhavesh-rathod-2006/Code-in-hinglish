# CSS 2D Transform Properties 

Yeh guide CSS 2D transform properties (`translate()`, `rotate()`, `scaleX()`, `scaleY()`, `scale()`, `skewX()`, `skewY()`, `skew()`, aur `matrix()`) ko cover karti hai. Isme har value ki detailed description, har property ke do examples, aur external CSS file (`styles.css`) mein defined styles shamil hain. Har example mein class ke sath HTML aur external stylesheet se corresponding CSS di gayi hai.

In examples ko use karne ke liye, ek HTML file banayein aur external CSS file ko is tarah link karein:

```html
<link rel="stylesheet" href="styles.css">
```

## 1. `translate()`
`translate()` function kisi element ko x-axis aur/ya y-axis ke along move karta hai.

### Description of Values
- **X-axis**: Horizontal displacement ko specify karta hai. Positive values (jaise `50px`) element ko right move karti hain, negative values (jaise `-50px`) left move karti hain. Length units accept karta hai (jaise `px`, `%`, `rem`).
- **Y-axis** (optional): Vertical displacement ko specify karta hai. Positive values (jaise `50px`) element ko down move karti hain, negative values up move karti hain. Agar omit kiya jaye, toh default `0` hota hai.
- **Syntax**: `translate(x, y)` (jaise `translate(50px, 20px)`). Agar sirf ek value di jaye, toh woh x-axis par apply hoti hai, aur y-axis `0` hota hai.
- **Inheritance**: Inherit nahi hota; parent ke transform ko adopt karne ke liye `inherit` ka use karein.

### Example 1: Translate Right and Down
**HTML:**
```html
<div class="translate-example1">Translated 50px right, 20px down</div>
```

**CSS (styles.css):**
```css
.translate-example1 {
  transform: translate(50px, 20px);
  width: 100px;
  height: 100px;
  background-color: #3498db;
  color: white;
  padding: 10px;
}
```

### Example 2: Translate Left
**HTML:**
```html
<div class="translate-example2">Translated 30px left</div>
```

**CSS (styles.css):**
```css
.translate-example2 {
  transform: translate(-30px, 0);
  width: 100px;
  height: 100px;
  background-color: #e74c3c;
  color: white;
  padding: 10px;
}
```

## 2. `rotate()`
`rotate()` function kisi element ko uske origin (default: center) ke charon taraf rotate karta hai.

### Description of Values
- **Angle**: Rotation angle ko specify karta hai. Positive values (jaise `45deg`) clockwise rotate karti hain, negative values (jaise `-45deg`) counterclockwise rotate karti hain. `deg`, `rad`, `turn` jaise units accept karta hai.
- **Origin**: `transform-origin` dwara control hota hai (jaise `top left`). Default `center` hota hai.
- **Syntax**: `rotate(angle)` (jaise `rotate(45deg)`).
- **Inheritance**: Inherit nahi hota; parent ke transform ko adopt karne ke liye `inherit` ka use karein.

### Example 1: Rotate Clockwise
**HTML:**
```html
<div class="rotate-example1">Rotated 45 degrees clockwise</div>
```

**CSS (styles.css):**
```css
.rotate-example1 {
  transform: rotate(45deg);
  width: 100px;
  height: 100px;
  background-color: #2ecc71;
  color: white;
  padding: 10px;
}
```

### Example 2: Rotate Counterclockwise
**HTML:**
```html
<div class="rotate-example2">Rotated 30 degrees counterclockwise</div>
```

**CSS (styles.css):**
```css
.rotate-example2 {
  transform: rotate(-30deg);
  width: 100px;
  height: 100px;
  background-color: #f1c40f;
  color: black;
  padding: 10px;
}
```

## 3. `scaleX()`
`scaleX()` function kisi element ko horizontally scale karta hai.

### Description of Values
- **Scale Factor**: Ek unitless number jo horizontal scaling specify karta hai. 1 se badi values (jaise `2`) element ko stretch karti hain, 1 se chhoti values (jaise `0.5`) shrink karti hain, `1` se koi change nahi hota, aur negative values isse flip kar deti hain (jaise `-1`).
- **Syntax**: `scaleX(factor)` (jaise `scaleX(1.5)`).
- **Inheritance**: Inherit nahi hota; parent ke transform ko adopt karne ke liye `inherit` ka use karein.

### Example 1: ScaleX Stretch
**HTML:**
```html
<div class="scalex-example1">Scaled 1.5x horizontally</div>
```

**CSS (styles.css):**
```css
.scalex-example1 {
  transform: scaleX(1.5);
  width: 100px;
  height: 100px;
  background-color: #9b59b6;
  color: white;
  padding: 10px;
}
```

### Example 2: ScaleX Flip
**HTML:**
```html
<div class="scalex-example2">Flipped horizontally</div>
```

**CSS (styles.css):**
```css
.scalex-example2 {
  transform: scaleX(-1);
  width: 100px;
  height: 100px;
  background-color: #1abc9c;
  color: white;
  padding: 10px;
}
```

## 4. `scaleY()`
`scaleY()` function kisi element ko vertically scale karta hai.

### Description of Values
- **Scale Factor**: Ek unitless number jo vertical scaling specify karta hai. 1 se badi values (jaise `2`) element ko stretch karti hain, 1 se chhoti values (jaise `0.5`) shrink karti hain, `1` se koi change nahi hota, aur negative values isse flip kar deti hain (jaise `-1`).
- **Syntax**: `scaleY(factor)` (jaise `scaleY(0.8)`).
- **Inheritance**: Inherit nahi hota; parent ke transform ko adopt karne ke liye `inherit` ka use karein.

### Example 1: ScaleY Shrink
**HTML:**
```html
<div class="scaley-example1">Scaled 0.8x vertically</div>
```

**CSS (styles.css):**
```css
.scaley-example1 {
  transform: scaleY(0.8);
  width: 100px;
  height: 100px;
  background-color: #e67e22;
  color: white;
  padding: 10px;
}
```

### Example 2: ScaleY Stretch
**HTML:**
```html
<div class="scaley-example2">Scaled 1.5x vertically</div>
```

**CSS (styles.css):**
```css
.scaley-example2 {
  transform: scaleY(1.5);
  width: 100px;
  height: 100px;
  background-color: #34495e;
  color: white;
  padding: 10px;
}
```

## 5. `scale()`
`scale()` function kisi element ko horizontally aur/ya vertically scale karta hai.

### Description of Values
- **X-axis Scale**: Horizontal scaling ke liye ek unitless number. 1 se badi values stretch karti hain, 1 se chhoti shrink karti hain, `1` se koi change nahi hota, aur negative values flip karti hain.
- **Y-axis Scale** (optional): Vertical scaling ke liye ek unitless number. Agar omit kiya jaye, toh x-axis value ke barabar hota hai.
- **Syntax**: `scale(x, y)` (jaise `scale(2, 0.5)`). Agar ek value di jaye, toh woh dono axes par apply hoti hai (jaise `scale(2)`).
- **Inheritance**: Inherit nahi hota; parent ke transform ko adopt karne ke liye `inherit` ka use karein.

### Example 1: Uniform Scale
**HTML:**
```html
<div class="scale-example1">Scaled 1.2x both axes</div>
```

**CSS (styles.css):**
```css
.scale-example1 {
  transform: scale(1.2);
  width: 100px;
  height: 100px;
  background-color: #c0392b;
  color: white;
  padding: 10px;
}
```

### Example 2: Non-Uniform Scale
**HTML:**
```html
<div class="scale-example2">Scaled 1.5x horizontally, 0.7x vertically</div>
```

**CSS (styles.css):**
```css
.scale-example2 {
  transform: scale(1.5, 0.7);
  width: 100px;
  height: 100px;
  background-color: #8e44ad;
  color: white;
  padding: 10px;
}
```

## 6. `skewX()`
`skewX()` function kisi element ko x-axis ke along skew karta hai, jisse woh horizontally tilt hota hai.

### Description of Values
- **Angle**: Horizontal skew angle specify karta hai. Positive values (jaise `20deg`) top ko right side tilt karti hain, negative values (jaise `-20deg`) top ko left side tilt karti hain. `deg`, `rad`, ya `turn` accept karta hai.
- **Syntax**: `skewX(angle)` (jaise `skewX(20deg)`).
- **Inheritance**: Inherit nahi hota; parent ke transform ko adopt karne ke liye `inherit` ka use karein.

### Example 1: SkewX Right Tilt
**HTML:**
```html
<div class="skewx-example1">Skewed 20 degrees on x-axis</div>
```

**CSS (styles.css):**
```css
.skewx-example1 {
  transform: skewX(20deg);
  width: 100px;
  height: 100px;
  background-color: #27ae60;
  color: white;
  padding: 10px;
}
```

### Example 2: SkewX Left Tilt
**HTML:**
```html
<div class="skewx-example2">Skewed -15 degrees on x-axis</div>
```

**CSS (styles.css):**
```css
.skewx-example2 {
  transform: skewX(-15deg);
  width: 100px;
  height: 100px;
  background-color: #d35400;
  color: white;
  padding: 10px;
}
```

## 7. `skewY()`
`skewY()` function kisi element ko y-axis ke along skew karta hai, jisse woh vertically tilt hota hai.

### Description of Values
- **Angle**: Vertical skew angle specify karta hai. Positive values (jaise `20deg`) right side ko neeche ki taraf tilt karti hain, negative values (jaise `-20deg`) right side ko upar ki taraf tilt karti hain. `deg`, `rad`, ya `turn` accept karta hai.
- **Syntax**: `skewY(angle)` (jaise `skewY(20deg)`).
- **Inheritance**: Inherit nahi hota; parent ke transform ko adopt karne ke liye `inherit` ka use karein.

### Example 1: SkewY Down Tilt
**HTML:**
```html
<div class="skewy-example1">Skewed 20 degrees on y-axis</div>
```

**CSS (styles.css):**
```css
.skewy-example1 {
  transform: skewY(20deg);
  width: 100px;
  height: 100px;
  background-color: #2980b9;
  color: white;
  padding: 10px;
}
```

### Example 2: SkewY Up Tilt
**HTML:**
```html
<div class="skewy-example2">Skewed -15 degrees on y-axis</div>
```

**CSS (styles.css):**
```css
.skewy-example2 {
  transform: skewY(-15deg);
  width: 100px;
  height: 100px;
  background-color: #f39c12;
  color: white;
  padding: 10px;
}
```

## 8. `skew()`
`skew()` function kisi element ko x-axis aur y-axis dono ke along skew karta hai.

### Description of Values
- **X-axis Angle**: Horizontal skew angle specify karta hai. Positive values top right tilt karti hain, negative values left tilt karti hain.
- **Y-axis Angle** (optional): Vertical skew angle specify karta hai. Positive values right side ko down tilt karti hain, negative values up tilt karti hain. Agar omit kiya jaye, toh default `0` hota hai.
- **Syntax**: `skew(x-angle, y-angle)` (jaise `skew(20deg, 10deg)`). Agar ek value di jaye, toh y-angle `0` hota hai.
- **Inheritance**: Inherit nahi hota; parent ke transform ko adopt karne ke liye `inherit` ka use karein.

### Example 1: Skew Both Axes
**HTML:**
```html
<div class="skew-example1">Skewed 20deg x, 10deg y</div>
```

**CSS (styles.css):**
```css
.skew-example1 {
  transform: skew(20deg, 10deg);
  width: 100px;
  height: 100px;
  background-color: #16a085;
  color: white;
  padding: 10px;
}
```

### Example 2: Skew X-Axis Only
**HTML:**
```html
<div class="skew-example2">Skewed 15deg on x-axis only</div>
```

**CSS (styles.css):**
```css
.skew-example2 {
  transform: skew(15deg);
  width: 100px;
  height: 100px;
  background-color: #8d5524;
  color: white;
  padding: 10px;
}
```

## 9. `matrix()`
`matrix()` function ek 2x3 transformation matrix ka use karke 2D transformation apply karta hai, jo multiple effects (translate, rotate, scale, skew) ko combine karta hai.

### Description of Values
- **Matrix Values**: Chhah unitless numbers (`a, b, c, d, tx, ty`) jo ek 2x3 matrix define karte hain:
  - `a`: Horizontal scaling (`scaleX` ki tarah).
  - `b`: Horizontal skewing (`skewY` se related).
  - `c`: Vertical skewing (`skewX` se related).
  - `d`: Vertical scaling (`scaleY` ki tarah).
  - `tx`: Horizontal translation (`translateX` ki tarah).
  - `ty`: Vertical translation (`translateY` ki tarah).
- **Syntax**: `matrix(a, b, c, d, tx, ty)` (jaise translation ke liye `matrix(1, 0, 0, 1, 50, 50)`).
- **Use Case**: Multiple transforms ko ek hi function mein combine karta hai; complex transformations ke liye matrix math ki samajh honi zaroori hai.
- **Inheritance**: Inherit nahi hota; parent ke transform ko adopt karne ke liye `inherit` ka use karein.

### Example 1: Matrix for Translation and Scale
**HTML:**
```html
<div class="matrix-example1">Translated 50px right, scaled 1.2x</div>
```

**CSS (styles.css):**
```css
.matrix-example1 {
  transform: matrix(1.2, 0, 0, 1.2, 50, 0); /* Scale 1.2x both axes, translate 50px right */
  width: 100px;
  height: 100px;
  background-color: #2c3e50;
  color: white;
  padding: 10px;
}
```

### Example 2: Matrix for Skew and Translation
**HTML:**
```html
<div class="matrix-example2">Skewed 20deg x, translated 20px down</div>
```

**CSS (styles.css):**
```css
.matrix-example2 {
  transform: matrix(1, 0, 0.36397, 1, 0, 20); /* SkewX ~20deg (tan(20deg) ≈ 0.36397), translate 20px down */
  width: 100px;
  height: 100px;
  background-color: #7f8c8d;
  color: white;
  padding: 10px;
}
```

## Notes
- CSS code ko `styles.css` naam ki file mein save karein aur ise `<link rel="stylesheet" href="styles.css">` ka use karke apne HTML se link karein.
- **General Notes**:
  - `transform` property 2D space mein transformations apply karti hai, jo layout flow ko bigade bina position, rotation, scale, ya skew ko affect karti hai.
  - Multiple transforms ko combine kiya ja sakta hai (jaise `transform: translate(50px) rotate(45deg);`), aur yeh order mein apply hote hain.
  - Transformations ke reference point ko adjust karne ke liye `transform-origin` ka use karein (default: `center`).
  - Elements ke charon taraf kafi space rakhein taaki clipping se bacha ja sake, khas karke `rotate()` ya `skew()` ke liye.
- **For `translate()`**: Layout ko affect kiye bina simple repositioning ke liye use karein; element ke size ke relative percentage-based movement ko support karta hai.
- **For `rotate()`**: `deg` mein angles sabse common hain; custom pivot points ke liye `transform-origin` ka use karein.
- **For `scaleX()`, `scaleY()`, `scale()`**: 1 se kam values shrink karti hain, 1 se badi stretch karti hain, negative values flip karti hain. Ek value ke sath `scale()` uniformly apply hota hai.
- **For `skewX()`, `skewY()`, `skew()`**: Skewing shape ko distort karta hai; readability issues se bachne ke liye iska kam use karein.
- **For `matrix()`**: Advanced transformations ke liye 2x3 matrix ko represent karta hai; precise values ke liye tools ya calculations ka use karein (jaise `skewX(20deg)` ≈ `matrix(1, 0, 0.36397, 1, 0, 0)`).
- Browsers par transformations ko test karein, kyunki rendering alag ho sakti hai, khas karke `matrix()` ke liye.
- Readability aur accessibility ka dhyan rakhein; zyada transforms (jaise heavy skew ya negative scaling) text ko distort kar sakte hain.