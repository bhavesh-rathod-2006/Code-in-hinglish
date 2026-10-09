# CSS Animation Properties 

Yeh guide CSS animation properties (`@keyframes`, `animation-name`, `animation-duration`, `animation-delay`, `animation-iteration-count`, `animation-direction`, `animation-timing-function`, `animation-fill-mode`, aur `animation`) ko cover karti hai. Isme har value ki detailed description, har property ke do examples, aur external CSS file (`styles.css`) mein defined styles shamil hain. Har example mein class ke sath HTML aur external stylesheet se corresponding CSS di gayi hai. Aakhir mein, kuch additional animation examples practical applications ko demonstrate karte hain.

In examples ko use karne ke liye, ek HTML file banayein aur external CSS file ko is tarah link karein:

```html
<link rel="stylesheet" href="styles.css">
```

## 1. `@keyframes`
`@keyframes` rule animation ke keyframes ko define karta hai, jo animation ke alag-alag points par styles specify karta hai.

### Description of Values
- **Animation Name**: Ek custom identifier (jaise `fadeIn`) jo `animation-name` ke zariye keyframes ko kisi element se link karta hai.
- **Keyframes**: Percentages (jaise `0%`, `50%`, `100%`) ya keywords (`from`, `to`) ke roop mein define kiye jaate hain jo animation stages ko indicate karte hain. Har keyframe mein us point par apply hone wali CSS properties hoti hain.
- **Syntax**: 
  ```css
  @keyframes animation-name {
    from { /* styles */ }
    to { /* styles */ }
  }
  ```
  ya
  ```css
  @keyframes animation-name {
    0% { /* styles */ }
    50% { /* styles */ }
    100% { /* styles */ }
  }
  ```
- **Scope**: CSS mein define hota hai (global ya kisi selector ke andar scoped) aur `animation-name` dwara reference kiya jata hai.

### Example 1: Fade-In Keyframes
**HTML:**
```html
<div class="keyframes-example1">Fade in animation</div>
```

**CSS (styles.css):**
```css
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}
.keyframes-example1 {
  width: 100px;
  height: 100px;
  background-color: #3498db;
  color: white;
  padding: 10px;
  animation: fadeIn 1s ease;
}
```

### Example 2: Slide Keyframes
**HTML:**
```html
<div class="keyframes-example2">Slide in from left</div>
```

**CSS (styles.css):**
```css
@keyframes slideIn {
  0% { transform: translateX(-100px); }
  100% { transform: translateX(0); }
}
.keyframes-example2 {
  width: 100px;
  height: 100px;
  background-color: #e74c3c;
  color: white;
  padding: 10px;
  animation: slideIn 0.5s ease;
}
```

## 2. `animation-name`
`animation-name` property specify karti hai ki kisi element par kaun sa `@keyframes` rule apply karna hai.

### Description of Values
- **Name**: `@keyframes` rule ka identifier (jaise `fadeIn`, `slideIn`). Yeh `@keyframes` name se exact match hona chahiye.
- **None**: Animation ko disable kar deta hai (`none`).
- **Multiple Animations**: Multiple names ko comma se separate karein (jaise `fadeIn, slideIn`).
- **Syntax**: `animation-name: name | none;` (jaise `animation-name: fadeIn;`).
- **Inheritance**: Inherit nahi hota; parent ke animation-name ko adopt karne ke liye `inherit` ka use karein.

### Example 1: Single Animation Name
**HTML:**
```html
<div class="animation-name-example1">Fade in effect</div>
```

**CSS (styles.css):**
```css
@keyframes fadeEffect {
  from { opacity: 0; }
  to { opacity: 1; }
}
.animation-name-example1 {
  width: 100px;
  height: 100px;
  background-color: #2ecc71;
  color: white;
  padding: 10px;
  animation-name: fadeEffect;
  animation-duration: 1s;
}
```

### Example 2: Multiple Animation Names
**HTML:**
```html
<div class="animation-name-example2">Fade and scale effect</div>
```

**CSS (styles.css):**
```css
@keyframes fade {
  from { opacity: 0; }
  to { opacity: 1; }
}
@keyframes scale {
  from { transform: scale(0.5); }
  to { transform: scale(1); }
}
.animation-name-example2 {
  width: 100px;
  height: 100px;
  background-color: #f1c40f;
  color: black;
  padding: 10px;
  animation-name: fade, scale;
  animation-duration: 0.5s, 0.5s;
}
```

## 3. `animation-duration`
`animation-duration` property specify karti hai ki animation ko ek cycle complete karne mein kitna time lagta hai.

### Description of Values
- **Time**: Seconds (jaise `1s`) ya milliseconds (jaise `1000ms`) mein duration. `0s` animation ko disable kar deta hai.
- **Multiple Durations**: Multiple animations ke liye durations ko comma se separate karein (jaise `0.5s, 1s`).
- **Syntax**: `animation-duration: time;` (jaise `animation-duration: 0.5s;`).
- **Inheritance**: Inherit nahi hota; parent ke animation-duration ko adopt karne ke liye `inherit` ka use karein.

### Example 1: Short Duration Animation
**HTML:**
```html
<div class="animation-duration-example1">Fast fade animation</div>
```

**CSS (styles.css):**
```css
@keyframes quickFade {
  from { opacity: 0; }
  to { opacity: 1; }
}
.animation-duration-example1 {
  width: 100px;
  height: 100px;
  background-color: #9b59b6;
  color: white;
  padding: 10px;
  animation-name: quickFade;
  animation-duration: 0.3s; /* Fast 0.3s animation */
}
```

### Example 2: Long Duration Animation
**HTML:**
```html
<div class="animation-duration-example2">Slow slide animation</div>
```

**CSS (styles.css):**
```css
@keyframes slowSlide {
  from { transform: translateX(-50px); }
  to { transform: translateX(0); }
}
.animation-duration-example2 {
  width: 100px;
  height: 100px;
  background-color: #1abc9c;
  color: white;
  padding: 10px;
  animation-name: slowSlide;
  animation-duration: 2s; /* Slow 2s animation */
}
```

## 4. `animation-delay`
`animation-delay` property animation start hone se pehle ka delay specify karti hai.

### Description of Values
- **Time**: Seconds (jaise `0.2s`) ya milliseconds (jaise `200ms`) mein delay. Negative values animation ko cycle ke beech se start karti hain.
- **Multiple Delays**: Multiple animations ke liye delays ko comma se separate karein (jaise `0.2s, 0.5s`).
- **Syntax**: `animation-delay: time;` (jaise `animation-delay: 0.2s;`).
- **Inheritance**: Inherit nahi hota; parent ke animation-delay ko adopt karne ke liye `inherit` ka use karein.

### Example 1: Delayed Fade Animation
**HTML:**
```html
<div class="animation-delay-example1">Delayed fade in</div>
```

**CSS (styles.css):**
```css
@keyframes delayedFade {
  from { opacity: 0; }
  to { opacity: 1; }
}
.animation-delay-example1 {
  width: 100px;
  height: 100px;
  background-color: #e67e22;
  color: white;
  padding: 10px;
  animation-name: delayedFade;
  animation-duration: 0.5s;
  animation-delay: 0.5s; /* 0.5s delay */
}
```

### Example 2: Negative Delay Animation
**HTML:**
```html
<div class="animation-delay-example2">Negative delay slide</div>
```

**CSS (styles.css):**
```css
@keyframes slideEffect {
  from { transform: translateX(-50px); }
  to { transform: translateX(0); }
}
.animation-delay-example2 {
  width: 100px;
  height: 100px;
  background-color: #34495e;
  color: white;
  padding: 10px;
  animation-name: slideEffect;
  animation-duration: 1s;
  animation-delay: -0.3s; /* Starts 0.3s into animation */
}
```

## 5. `animation-iteration-count`
`animation-iteration-count` property specify karti hai ki koi animation kitni baar repeat hoga.

### Description of Values
- **Number**: Ek positive integer (jaise `3`) ya partial cycles ke liye decimal (jaise `2.5`).
- **Infinite**: Bina ruke lagataar repeat hota rehta hai (`infinite`).
- **Syntax**: `animation-iteration-count: number | infinite;` (jaise `animation-iteration-count: 3;`).
- **Inheritance**: Inherit nahi hota; parent ke animation-iteration-count ko adopt karne ke liye `inherit` ka use karein.

### Example 1: Finite Iteration Count
**HTML:**
```html
<div class="animation-iteration-example1">Pulse 3 times</div>
```

**CSS (styles.css):**
```css
@keyframes pulse {
  0% { transform: scale(1); }
  50% { transform: scale(1.2); }
  100% { transform: scale(1); }
}
.animation-iteration-example1 {
  width: 100px;
  height: 100px;
  background-color: #c0392b;
  color: white;
  padding: 10px;
  animation-name: pulse;
  animation-duration: 0.5s;
  animation-iteration-count: 3; /* Repeats 3 times */
}
```

### Example 2: Infinite Iteration Count
**HTML:**
```html
<div class="animation-iteration-example2">Infinite bounce</div>
```

**CSS (styles.css):**
```css
@keyframes bounce {
  0% { transform: translateY(0); }
  50% { transform: translateY(-20px); }
  100% { transform: translateY(0); }
}
.animation-iteration-example2 {
  width: 100px;
  height: 100px;
  background-color: #8e44ad;
  color: white;
  padding: 10px;
  animation-name: bounce;
  animation-duration: 0.8s;
  animation-iteration-count: infinite; /* Repeats forever */
}
```

## 6. `animation-direction`
`animation-direction` property specify karti hai ki animation aage (forward) chalega, peeche (backward) chalega, ya alternate hoga.

### Description of Values
- **Normal**: 0% se 100% tak aage ki taraf chalta hai (default).
- **Reverse**: 100% se 0% tak peeche ki taraf chalta hai.
- **Alternate**: Har cycle mein direction badalta hai (pehle forward, phir backward).
- **Alternate-reverse**: Backward direction se shuru karke alternate hota hai (pehle backward, phir forward).
- **Syntax**: `animation-direction: normal | reverse | alternate | alternate-reverse;` (jaise `animation-direction: alternate;`).
- **Inheritance**: Inherit nahi hota; parent ke animation-direction ko adopt karne ke liye `inherit` ka use karein.

### Example 1: Alternate Direction
**HTML:**
```html
<div class="animation-direction-example1">Alternate slide animation</div>
```

**CSS (styles.css):**
```css
@keyframes slideBackForth {
  from { transform: translateX(0); }
  to { transform: translateX(50px); }
}
.animation-direction-example1 {
  width: 100px;
  height: 100px;
  background-color: #27ae60;
  color: white;
  padding: 10px;
  animation-name: slideBackForth;
  animation-duration: 0.5s;
  animation-iteration-count: 4;
  animation-direction: alternate; /* Forward, then backward */
}
```

### Example 2: Reverse Direction
**HTML:**
```html
<div class="animation-direction-example2">Reverse fade animation</div>
```

**CSS (styles.css):**
```css
@keyframes fadeReverse {
  from { opacity: 0; }
  to { opacity: 1; }
}
.animation-direction-example2 {
  width: 100px;
  height: 100px;
  background-color: #d35400;
  color: white;
  padding: 10px;
  animation-name: fadeReverse;
  animation-duration: 0.5s;
  animation-iteration-count: 2;
  animation-direction: reverse; /* Plays backward */
}
```

## 7. `animation-timing-function`
`animation-timing-function` property animation ki speed curve ko define karti hai.

### Description of Values
- **Predefined Functions**:
  - `ease`: Dhire shuru hota hai, speed pakadta hai, phir dhire ho jata hai (default).
  - `linear`: Continuous same speed rehti hai.
  - `ease-in`: Dhire shuru hota hai, phir speed pakadta hai.
  - `ease-out`: Tej shuru hota hai, phir dhire ho jata hai.
  - `ease-in-out`: Shuru aur end mein dhire rehta hai, beech mein tez hota hai.
- **Cubic Bezier**: `cubic-bezier(x1, y1, x2, y2)` ka use karke custom curve (jaise `cubic-bezier(0.25, 0.1, 0.25, 1)`).
- **Steps**: `steps(n, [start|end])` ka use karke discrete steps (jaise `steps(4, end)`).
- **Multiple Timing Functions**: Multiple animations ke liye functions ko comma se separate karein.
- **Syntax**: `animation-timing-function: ease | linear | ease-in | ease-out | ease-in-out | cubic-bezier(n,n,n,n) | steps(n, [start|end]);`.
- **Inheritance**: Inherit nahi hota; parent ke animation-timing-function ko adopt karne ke liye `inherit` ka use karein.

### Example 1: Ease-In Timing Function
**HTML:**
```html
<div class="animation-timing-example1">Ease-in slide animation</div>
```

**CSS (styles.css):**
```css
@keyframes slideEaseIn {
  from { transform: translateX(0); }
  to { transform: translateX(50px); }
}
.animation-timing-example1 {
  width: 100px;
  height: 100px;
  background-color: #16a085;
  color: white;
  padding: 10px;
  animation-name: slideEaseIn;
  animation-duration: 0.5s;
  animation-timing-function: ease-in; /* Slow start, fast finish */
}
```

### Example 2: Cubic Bezier Timing Function
**HTML:**
```html
<div class="animation-timing-example2">Bouncy scale animation</div>
```

**CSS (styles.css):**
```css
@keyframes scaleBouncy {
  from { transform: scale(1); }
  to { transform: scale(1.5); }
}
.animation-timing-example2 {
  width: 100px;
  height: 100px;
  background-color: #8d5524;
  color: white;
  padding: 10px;
  animation-name: scaleBouncy;
  animation-duration: 0.5s;
  animation-timing-function: cubic-bezier(0.68, -0.55, 0.265, 1.55); /* Bouncy effect */
}
```

## 8. `animation-fill-mode`
`animation-fill-mode` property specify karti hai ki animation se pehle aur baad mein element ke styles kaise apply honge.

### Description of Values
- **None**: Animation se pehle ya baad mein koi extra style apply nahi hota (default).
- **Forwards**: Animation khatam hone ke baad last keyframe (100% ya `to`) ke styles ko retain karke rakhta hai.
- **Backwards**: Animation start hone se pehle delay period ke dauran pehle keyframe (0% ya `from`) ke styles apply kar deta hai.
- **Both**: `forwards` aur `backwards` dono ko combine karta hai.
- **Syntax**: `animation-fill-mode: none | forwards | backwards | both;` (jaise `animation-fill-mode: forwards;`).
- **Inheritance**: Inherit nahi hota; parent ke animation-fill-mode ko adopt karne ke liye `inherit` ka use karein.

### Example 1: Forwards Fill Mode
**HTML:**
```html
<div class="animation-fill-example1">Fade and stay opaque</div>
```

**CSS (styles.css):**
```css
@keyframes fadeStay {
  from { opacity: 0; }
  to { opacity: 1; }
}
.animation-fill-example1 {
  width: 100px;
  height: 100px;
  background-color: #2c3e50;
  color: white;
  padding: 10px;
  animation-name: fadeStay;
  animation-duration: 0.5s;
  animation-fill-mode: forwards; /* Retains final opacity */
}
```

### Example 2: Both Fill Mode
**HTML:**
```html
<div class="animation-fill-example2">Slide with both fill mode</div>
```

**CSS (styles.css):**
```css
@keyframes slideFill {
  from { transform: translateX(-50px); }
  to { transform: translateX(0); }
}
.animation-fill-example2 {
  width: 100px;
  height: 100px;
  background-color: #7f8c8d;
  color: white;
  padding: 10px;
  animation-name: slideFill;
  animation-duration: 0.5s;
  animation-delay: 0.2s;
  animation-fill-mode: both; /* Applies initial and final styles */
}
```

## 9. `animation`
`animation` shorthand property `animation-name`, `animation-duration`, `animation-timing-function`, `animation-delay`, `animation-iteration-count`, `animation-direction`, `animation-fill-mode`, aur `animation-play-state` ko combine karti hai.

### Description of Values
- **Name**: `@keyframes` ka naam (jaise `fadeIn`).
- **Duration**: Ek cycle ka time (jaise `0.5s`).
- **Timing Function**: Speed curve (jaise `ease`, `cubic-bezier(n,n,n,n)`).
- **Delay**: Start hone se pehle ka time (jaise `0.2s`).
- **Iteration Count**: Cycles ki sankhya (jaise `3`, `infinite`).
- **Direction**: Playback direction (jaise `normal`, `alternate`).
- **Fill Mode**: Animation se pehle/baad ke styles (jaise `forwards`, `both`).
- **Play State**: Animation state control karta hai (`running` ya `paused`, examples mein use nahi hua hai).
- **Multiple Animations**: Multiple animations ko comma se separate karein.
- **Syntax**: `animation: name duration timing-function delay iteration-count direction fill-mode [play-state];` (jaise `animation: fadeIn 0.5s ease 0.2s 1 normal forwards;`).
- **Inheritance**: Inherit nahi hota; parent ke animation ko adopt karne ke liye `inherit` ka use karein.

### Example 1: Single Animation Shorthand
**HTML:**
```html
<div class="animation-example1">Fade in with shorthand</div>
```

**CSS (styles.css):**
```css
@keyframes fadeShort {
  from { opacity: 0; }
  to { opacity: 1; }
}
.animation-example1 {
  width: 100px;
  height: 100px;
  background-color: #3498db;
  color: white;
  padding: 10px;
  animation: fadeShort 0.5s ease 0.2s 1 normal forwards; /* Name, duration, timing, delay, iterations, direction, fill */
}
```

### Example 2: Multiple Animations Shorthand
**HTML:**
```html
<div class="animation-example2">Slide and scale with shorthand</div>
```

**CSS (styles.css):**
```css
@keyframes slideShort {
  from { transform: translateX(-50px); }
  to { transform: translateX(0); }
}
@keyframes scaleShort {
  from { transform: scale(0.8); }
  to { transform: scale(1); }
}
.animation-example2 {
  width: 100px;
  height: 100px;
  background-color: #e74c3c;
  color: white;
  padding: 10px;
  animation: slideShort 0.5s ease, scaleShort 0.5s linear 0.1s; /* Two animations with different timings */
}
```

## Additional Animation Examples
Niche common effects ke liye CSS animations ko demonstrate karne wale practical examples diye gaye hain.

### Example 1: Pulsing Button
**HTML:**
```html
<div class="pulse-button">Pulsing Button</div>
```

**CSS (styles.css):**
```css
@keyframes pulseButton {
  0% { transform: scale(1); box-shadow: 0 0 0 rgba(0, 0, 0, 0.2); }
  50% { transform: scale(1.1); box-shadow: 0 0 10px rgba(0, 0, 0, 0.4); }
  100% { transform: scale(1); box-shadow: 0 0 0 rgba(0, 0, 0, 0.2); }
}
.pulse-button {
  width: 100px;
  height: 40px;
  background-color: #2ecc71;
  color: white;
  text-align: center;
  padding: 10px;
  border-radius: 5px;
  animation: pulseButton 1.5s ease infinite;
}
```

### Example 2: Spinning Square
**HTML:**
```html
<div class="spin-square">Spinning Square</div>
```

**CSS (styles.css):**
```css
@keyframes spin {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}
.spin-square {
  width: 100px;
  height: 100px;
  background-color: #9b59b6;
  color: white;
  padding: 10px;
  animation: spin 2s linear infinite;
}
```

### Example 3: Color Change Background
**HTML:**
```html
<div class="color-change">Color Changing Background</div>
```

**CSS (styles.css):**
```css
@keyframes colorChange {
  0% { background-color: #1abc9c; }
  33% { background-color: #e67e22; }
  66% { background-color: #c0392b; }
  100% { background-color: #1abc9c; }
}
.color-change {
  width: 100px;
  height: 100px;
  color: white;
  padding: 10px;
  animation: colorChange 3s ease-in-out infinite;
}
```

## Notes
- CSS code ko `styles.css` naam ki file mein save karein aur ise `<link rel="stylesheet" href="styles.css">` ka use karke apne HTML se link karein.
- **General Notes**:
  - Animations automatically run hote hain (transitions ke opposite, jinhe `:hover` jaise state change ki zaroorat hoti hai).
  - Animation sequences ko define karne ke liye `@keyframes` ka use karein, jinhe `animation-name` dwara reference kiya jata hai.
  - Sirf animatable properties (jaise `opacity`, `transform`, `background-color`) ko hi animate kiya ja sakta hai.
  - `animation` shorthand mein values ko comma se separate karke multiple animations ko combine karein.
- **For `@keyframes`**: Smooth animations ke liye clear keyframes (`from`, `to`, ya percentages) define karein.
- **For `animation-name`**: Dhyan rakhein ki names `@keyframes` se exact match karein.
- **For `animation-duration`**: User-friendly animations ke liye reasonable durations (jaise `0.3s` se `2s`) ka use karein.
- **For `animation-delay`**: Negative delays animation ko cycle ke beech se start karte hain; staggered effects ke liye useful hain.
- **For `animation-iteration-count`**: Spinners jaise continuous animations ke liye `infinite` ka use karein.
- **For `animation-direction`**: `alternate` ek smooth aage-peeche ka effect create karta hai.
- **For `animation-timing-function`**: `ease` jaise predefined functions common hain; `cubic-bezier` ya `steps` custom control offer karte hain.
- **For `animation-fill-mode`**: Final styles ko retain karne ke liye `forwards`, aur initial/final styles ke liye `both` ka use karein.
- **For `animation` shorthand**: Order hota hai `name duration timing-function delay iteration-count direction fill-mode [play-state]`.
- Browsers par animations ko test karein; zaroorat padne par older browsers ke liye `-webkit-animation` ka use karein.
- Performance ko optimize karne ke liye `opacity` aur `transform` jaisi properties ko animate karein, jo GPU-accelerated hoti hain.
- Accessibility ka dhyan rakhein: aisi excessive animations se bachein jo distract kar sakti hain ya motion sensitivity ki problem create kar sakti hain.
- Readability ke liye, animated elements mein sufficient contrast maintain karein.