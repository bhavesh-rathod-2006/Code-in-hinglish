# CSS Height, Width, and Max-Width

CSS `height`, `width`, aur `max-width` properties HTML elements ki dimensions (size) control karne ke liye use hoti hain. Yeh guide in properties ka use, shorthand aur non-shorthand methods, aur examples ke saath detail me explain karti hai.

---

## Width

`width` property kisi element ke **content area ki width** set karti hai. Yeh padding, border, aur margin ko include nahi karti (jab tak `box-sizing: border-box` use na ho).

- **Purpose:** Element ki horizontal size define karna.
- **Values:**
  - Length units: `px`, `%`, `vw`, `rem`, `em`, etc.
  - `auto`: Browser automatically width calculate karta hai (block elements ke liye default).
  - `inherit`: Parent element se width inherit karta hai.
- **Key Notes:**
  - `width` block aur inline-block elements par apply hoti hai.
  - Normal inline elements `width` property ko ignore karte hain.
  - Percentage (`%`) value parent element ki width ke according calculate hoti hai.

### Width: Shorthand

`width` property ka koi alag shorthand normally use nahi hota. Lekin kuch rare cases me `size` property ke context me `width` aur `height` ko combine kiya ja sakta hai (yeh common practice nahi hai).

- **Syntax:** `width: value;`

**Example:**

```css
div {
  width: 250px;
}
```

---

## Height

`height` property kisi element ke **content area ki height** set karti hai. Yeh padding, border, aur margin ko include nahi karti.

- **Purpose:** Element ki vertical size define karna.
- **Values:**
  - Length units: `px`, `%`, `vh`, `rem`, `em`, etc.
  - `auto`: Browser content ke hisaab se height calculate karta hai (default).
  - `inherit`: Parent element se height inherit karta hai.
- **Key Notes:**
  - Percentage height tabhi work karti hai jab parent element ki height explicitly set ho.
  - Inline elements `height` ko ignore karte hain jab tak unka `display` `inline-block` ya `block` na ho.

### Height: Shorthand

`height` property ka bhi normally koi shorthand use nahi hota. Rare cases me `size` property ke saath pair ki ja sakti hai.

- **Syntax:** `height: value;`

**Example:**

```css
div {
  height: 150px;
}
```

---

## Max-Width

`max-width` property kisi element ki **maximum width** set karti hai. Isse element specified value se zyada wide nahi ho sakta, chahe `width` ya content usse bada ho.

- **Purpose:** Responsive design me element ki maximum width limit karna.
- **Values:**
  - Length units: `px`, `%`, `vw`, `rem`, `em`, etc.
  - `none`: Koi maximum width nahi hoti (default).
  - `inherit`: Parent se value inherit hoti hai.
- **Key Notes:**
  - Agar computed width `max-width` se zyada ho, to `max-width` apply hogi.
  - Responsive layouts me bahut useful hai taaki large screens par element bahut zyada wide na ho.
  - `max-width` negative values support nahi karti.

### Max-Width: Shorthand

`max-width` ek single property hai aur iska koi shorthand version nahi hota.

- **Syntax:** `max-width: value;`

**Example:**

```css
div {
  max-width: 500px;
}
```

---

## Examples

### Example 1: Basic Width and Height

Ek div ki fixed width aur height set ki gayi hai.

```html
<div style="width: 200px; height: 100px; background-color: lightblue;">
  This div has a fixed width of 200px and height of 100px.
</div>
```

**Explanation:**

- `width: 200px;` div ki width **200 pixels** set karta hai.
- `height: 100px;` div ki height **100 pixels** set karta hai.
- `background-color: lightblue;` div ka background light blue bana deta hai.

---

### Example 2: Percentage Width with Max-Width

Responsive design ke liye percentage width aur `max-width` use ki gayi hai.

```html
<div style="width: 80%; max-width: 500px; height: 150px; background-color: lightgreen;">
  This div takes 80% of parent width but won’t exceed 500px.
</div>
```

**Explanation:**

- `width: 80%;` div parent ki width ka **80%** lega.
- `max-width: 500px;` div kabhi bhi **500px se zyada wide** nahi hoga.
- `height: 150px;` fixed height set karta hai.

---

### Example 3: Auto Height with Fixed Width

`height: auto` use karke height content ke according adjust hoti hai.

```html
<div style="width: 300px; height: auto; background-color: lightcoral; padding: 10px;">
  This div has a fixed width of 300px and height adjusts to content.
</div>
```

**Explanation:**

- `width: 300px;` fixed width set karta hai.
- `height: auto;` content jitna hoga, height utni automatically adjust ho jayegi.
- `padding: 10px;` content ke andar spacing add karta hai.

---

### Example 4: Viewport Units and Max-Width

Viewport units (`vw` aur `vh`) ke saath `max-width` use ki gayi hai.

```html
<div style="width: 50vw; height: 20vh; max-width: 400px; background-color: lightyellow;">
  This div uses 50% viewport width, 20% viewport height, capped at 400px wide.
</div>
```

**Explanation:**

- `width: 50vw;` viewport (browser window) ki width ka **50%** use karta hai.
- `height: 20vh;` viewport ki height ka **20%** use karta hai.
- `max-width: 400px;` width ko maximum **400px** tak limit karta hai.

---

### Example 5: Combining Width, Height, and Max-Width

Fixed aur relative units ko `max-width` ke saath combine kiya gaya hai.

```html
<div style="width: 100%; height: 200px; max-width: 600px; background-color: lightgray; margin: 0 auto;">
  This div spans 100% of parent width, up to 600px, with a fixed 200px height.
</div>
```

**Explanation:**

- `width: 100%;` div parent ki poori width occupy karega.
- `max-width: 600px;` lekin width **600px se zyada** nahi hogi.
- `height: 200px;` fixed height set karta hai.
- `margin: 0 auto;` div ko page ke center me horizontally align karta hai.