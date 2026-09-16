# CSS Background Guide

Yeh guide CSS ki background properties ko detail me explain karti hai. Isme `background-color`, `background-repeat`, `background-attachment`, `background-image`, `background-position`, `background-size`, `background-origin`, `background-clip`, aur `background` shorthand cover kiye gaye hain.

---

## 1. Background Color (`background-color`)

`background-color` property kisi HTML element ka background color set karti hai. Isme color names, hexadecimal values, RGB, RGBA, HSL, aur HSLA formats use kiye ja sakte hain.

**Examples:**

```css
/* Example 1: Using a color name */
div {
  background-color: lightblue;
  padding: 20px;
}

/* Example 2: Using hexadecimal */
section {
  background-color: #ff6347; /* Tomato */
  padding: 20px;
}

/* Example 3: Using RGB */
article {
  background-color: rgb(255, 192, 203); /* Pink */
  padding: 20px;
}

/* Example 4: Using RGBA for transparency */
aside {
  background-color: rgba(0, 128, 0, 0.3); /* Semi-transparent green */
  padding: 20px;
}
```

**Explanation:**

- **Color Name:** Direct color name use kiya gaya hai (`lightblue`).
- **Hexadecimal:** `#ff6347` Tomato color ko represent karta hai.
- **RGB:** `rgb(255, 192, 203)` Pink color ko represent karta hai.
- **RGBA:** `rgba(0, 128, 0, 0.3)` semi-transparent green background create karta hai.

---

## 2. Background Repeat (`background-repeat`)

`background-repeat` property control karti hai ki background image repeat hogi ya nahi. Iske possible values hain `repeat` (default), `repeat-x`, `repeat-y`, `no-repeat`, `space`, aur `round`.

**Examples:**

```css
/* Example 1: No repeat */
div {
  background-image: url('flower.png');
  background-repeat: no-repeat;
  height: 200px;
}

/* Example 2: Repeat horizontally */
section {
  background-image: url('pattern.png');
  background-repeat: repeat-x;
  height: 100px;
}

/* Example 3: Repeat vertically */
article {
  background-image: url('stripe.png');
  background-repeat: repeat-y;
  height: 200px;
}

/* Example 4: Space repetition */
aside {
  background-image: url('dot.png');
  background-repeat: space;
  height: 200px;
}
```

**Explanation:**

- **repeat:** Image horizontal aur vertical dono direction me repeat hoti hai (default).
- **no-repeat:** Image sirf ek baar show hoti hai.
- **repeat-x:** Image sirf horizontal direction me repeat hoti hai.
- **repeat-y:** Image sirf vertical direction me repeat hoti hai.
- **space:** Images ke beech equal spacing create hoti hai.
- **round:** Image repeat hote waqt automatically resize ho jaati hai taaki poori space fill ho.

---

## 3. Background Attachment (`background-attachment`)

`background-attachment` property decide karti hai ki background image content ke saath scroll karegi ya fixed rahegi. Iski values hain `scroll` (default), `fixed`, aur `local`.

**Examples:**

```css
/* Example 1: Fixed attachment */
body {
  background-image: url('landscape.jpg');
  background-attachment: fixed;
  height: 500px;
}

/* Example 2: Scroll attachment */
div {
  background-image: url('bg-image.jpg');
  background-attachment: scroll;
  height: 300px;
  overflow: scroll;
}

/* Example 3: Local attachment */
section {
  background-image: url('texture.png');
  background-attachment: local;
  height: 200px;
  overflow: scroll;
}
```

**Explanation:**

- **scroll:** Background image content ke saath scroll karti hai (default).
- **fixed:** Background image screen par fixed rehti hai, scroll karne par move nahi hoti.
- **local:** Background image sirf element ke andar scroll hone par move karti hai.

---

## 4. Background Image (`background-image`)

`background-image` property ek ya multiple background images set karti hai. Image URL ya CSS gradients dono use kiye ja sakte hain. Multiple images ko commas se separate kiya jata hai.

**Examples:**

```css
/* Example 1: Single image */
header {
  background-image: url('header-bg.jpg');
  background-color: #cccccc; /* Fallback */
  height: 150px;
}

/* Example 2: Linear gradient */
div {
  background-image: linear-gradient(to right, red, yellow);
  height: 100px;
}

/* Example 3: Multiple images */
section {
  background-image: url('star.png'), url('cloud.png');
  background-position: top left, bottom right;
  background-repeat: no-repeat, no-repeat;
  height: 200px;
}

/* Example 4: Radial gradient */
article {
  background-image: radial-gradient(circle, blue, white);
  height: 200px;
}
```

**Explanation:**

- **Single Image:** Background me ek image set hoti hai.
- **Linear Gradient:** Do ya zyada colors ke beech smooth transition create hota hai.
- **Multiple Images:** Ek hi element par multiple background images layer ki ja sakti hain.
- **Radial Gradient:** Colors center se bahar ki taraf circular gradient create karte hain.

---

## 5. Background Position (`background-position`)

`background-position` property background image ki starting position set karti hai. Position keywords (`top`, `center`, `bottom`, `left`, `right`), percentages, ya pixel values se define ki ja sakti hai.

**Examples:**

```css
/* Example 1: Using keywords */
div {
  background-image: url('icon.png');
  background-position: center center; /* Centered horizontally and vertically */
  background-repeat: no-repeat;
  height: 200px;
}

/* Example 2: Using percentages */
section {
  background-image: url('logo.png');
  background-position: 50% 75%; /* 50% from left, 75% from top */
  background-repeat: no-repeat;
  height: 200px;
}

/* Example 3: Using pixel values */
article {
  background-image: url('pattern.png');
  background-position: 10px 20px; /* 10px from left, 20px from top */
  background-repeat: no-repeat;
  height: 200px;
}

/* Example 4: Mixed units */
aside {
  background-image: url('image.png');
  background-position: left 10%; /* Left edge, 10% from top */
  background-repeat: no-repeat;
  height: 200px;
}
```

**Explanation:**

- **Keywords:** Image ko center, top, bottom, left, ya right par place karte hain.
- **Percentages:** Image ki position percentage ke basis par set hoti hai.
- **Pixel Values:** Exact pixel distance se image ki position set hoti hai.
- **Mixed Units:** Ek direction keyword aur dusri direction percentage ya pixel me di ja sakti hai.

---

## 6. Background Size (`background-size`)

`background-size` property background image ka size define karti hai. Values ho sakti hain `auto` (default), specific length (`px`, `%`), `cover`, aur `contain`.

**Examples:**

```css
/* Auto size */
div {
  background-image: url('image.png');
  background-size: auto; /* Original image size */
  background-repeat: no-repeat;
  height: 200px;
}

/* Specific size */
section {
  background-image: url('logo.png');
  background-size: 100px 50px; /* Width 100px, height 50px */
  background-repeat: no-repeat;
  height: 200px;
}

/* Cover */
article {
  background-image: url('bg.jpg');
  background-size: cover; /* Scales to cover, may crop */
  background-position: center;
  height: 200px;
}

/* Contain */
aside {
  background-image: url('pattern.png');
  background-size: contain; /* Scales to fit, no cropping */
  background-repeat: no-repeat;
  background-position: center;
  height: 200px;
}
```

**Explanation:**

- **auto:** Image apne original size me show hoti hai.
- **100px 50px:** Width aur height manually set ki jaati hai.
- **cover:** Image poore element ko cover karti hai, zarurat pade to crop bhi ho sakti hai.
- **contain:** Image poori element ke andar fit hoti hai bina crop hue.

---

## 7. Background Origin (`background-origin`)

`background-origin` property define karti hai ki background image kis area se position hona start karegi. Values hain `padding-box`, `border-box`, aur `content-box`.

**Examples:**

```css
/* Padding-box (default) */
div {
  background-image: url('flower.png');
  background-origin: padding-box;
  background-repeat: no-repeat;
  padding: 20px;
  border: 5px solid black;
  height: 200px;
}

/* Border-box */
section {
  background-image: url('pattern.png');
  background-origin: border-box;
  background-repeat: no-repeat;
  padding: 20px;
  border: 5px solid black;
  height: 200px;
}

/* Content-box */
article {
  background-image: url('icon.png');
  background-origin: content-box;
  background-repeat: no-repeat;
  padding: 20px;
  border: 5px solid black;
  height: 200px;
}
```

**Explanation:**

- **padding-box:** Background image padding area se start hoti hai (default).
- **border-box:** Background image border ke area ko bhi include karti hai.
- **content-box:** Background image sirf content area se start hoti hai.

---

## 8. Background Clip (`background-clip`)

`background-clip` property decide karti hai ki background color ya image kis area tak visible hogi. Values hain `border-box`, `padding-box`, aur `content-box`.

**Examples:**

```css
/* Border-box (default) */
div {
  background-image: url('bg.jpg');
  background-clip: border-box;
  padding: 20px;
  border: 5px dashed black;
  height: 200px;
}

/* Padding-box */
section {
  background-color: lightblue;
  background-clip: padding-box;
  padding: 20px;
  border: 5px dashed black;
  height: 200px;
}

/* Content-box */
article {
  background-image: url('pattern.png');
  background-clip: content-box;
  padding: 20px;
  border: 5px dashed black;
  height: 200px;
}
```

**Explanation:**

- **border-box:** Background border ke niche tak visible hoti hai (default).
- **padding-box:** Background sirf padding edge tak visible hoti hai.
- **content-box:** Background sirf content area ke andar visible hoti hai.

---

## 9. Background Shorthand (`background`)

`background` shorthand property ek hi declaration me `background-color`, `background-image`, `background-position`, `background-size`, `background-repeat`, `background-attachment`, `background-origin`, aur `background-clip` ko combine karti hai. `background-position` aur `background-size` ke beech slash (`/`) use hota hai.

**Examples:**

```css
/* Example 1: Center center cover */
main {
  background: #ffffff url('bg.jpg') center center/cover no-repeat fixed padding-box content-box;
  /* Color, image, position/size, repeat, attachment, origin, clip */
  height: 400px;
}

/* Example 2: Basic shorthand */
div {
  background: #f0f0f0 url('tile.png') center center no-repeat fixed;
  height: 300px;
}

/* Example 3: Shorthand with gradient and position */
section {
  background: linear-gradient(blue, green) top left no-repeat padding-box;
  height: 200px;
}

/* Example 4: Shorthand with position and size */
article {
  background: url('pattern.jpg') 20px 30px/50px 50px repeat scroll content-box;
  height: 200px;
}
```

**Explanation:**

- **Example 1:** White background color, image center me, `cover` size, no-repeat, fixed attachment, padding-box origin, aur content-box clip use kiya gaya hai.
- **Example 2:** Basic shorthand me color, image, position, repeat, aur attachment ek line me likhe gaye hain.
- **Example 3:** Gradient background top-left position se apply kiya gaya hai.
- **Example 4:** Background image ki position pixels me aur size `50px × 50px` set ki gayi hai.

---

## Additional Notes

- **Shorthand Order:** Normally order hota hai `background-color`, `background-image`, `background-position`, `background-size` (slash `/` ke baad), `background-repeat`, `background-attachment`, `background-origin`, aur `background-clip`. Order flexible hai, lekin `background-size` hamesha `background-position` ke baad `/` ke saath likhi jaati hai.

- **Center Center Cover:** `center center/cover` image ko horizontally aur vertically center karta hai aur image ko poore element ko cover karne ke liye scale karta hai. Zarurat pade to image crop bhi ho sakti hai.

- **Background Position:** Agar horizontal aur vertical position alag control karni ho, to `background-position-x` aur `background-position-y` properties use kar sakte ho.

- **Fallbacks:** `background-image` use karte waqt `background-color` bhi specify karna achha practice hai taaki image load na hone par background color dikh sake.

- **Multiple Backgrounds:** Multiple images ko `background-image` me commas se separate karke layer kiya ja sakta hai. Unki corresponding properties (`background-position`, `background-size`, `background-repeat`) bhi same order me commas se separate likhi jaati hain.

- **Browser Compatibility:** Zyada tar background properties modern browsers me support hoti hain, lekin `background-origin` aur `background-clip` ko older browsers me test karna achha practice hai.