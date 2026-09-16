# CSS Borders Guide

Yeh guide CSS ki border properties ko detail me explain karti hai. Isme `border-style`, `border-width`, `border-color`, `border` shorthand, aur different types of borders cover kiye gaye hain.

---

## 1. Border Style (`border-style`)

`border-style` property kisi HTML element ki border ka style define karti hai. CSS me available border styles hain: `solid`, `dashed`, `dotted`, `double`, `groove`, `ridge`, `inset`, `outset`, `none`, aur `hidden`. Har border style alag visual effect create karta hai.

**Examples:**

```css
/* Example 1: Solid border */
div {
  border-style: solid;
  border-width: 2px;
  border-color: black;
  padding: 10px;
}

/* Example 2: Dashed border */
section {
  border-style: dashed;
  border-width: 3px;
  border-color: #ff0000; /* Red */
  padding: 10px;
}

/* Example 3: Dotted border */
article {
  border-style: dotted;
  border-width: 2px;
  border-color: blue;
  padding: 10px;
}

/* Example 4: Double border */
aside {
  border-style: double;
  border-width: 4px;
  border-color: #008000; /* Green */
  padding: 10px;
}
```

**Explanation:**

- **Solid:** Ek single continuous line wali border.
- **Dashed:** Chhoti-chhoti dashes wali border.
- **Dotted:** Chhote dots wali border.
- **Double:** Do parallel lines wali border jinke beech gap hota hai.

---

## 2. Border Width (`border-width`)

`border-width` property border ki thickness ya width set karti hai. Iski value pixels (`px`), percentage (`%`), ya keywords `thin`, `medium`, aur `thick` me di ja sakti hai. `border-width` tabhi work karegi jab `border-style` define kiya gaya ho.

**Examples:**

```css
/* Example 1: Pixel width */
div {
  border-style: solid;
  border-width: 5px;
  border-color: #333333;
  padding: 10px;
}

/* Example 2: Thin keyword */
section {
  border-style: dashed;
  border-width: thin;
  border-color: #ff6347; /* Tomato */
  padding: 10px;
}

/* Example 3: Medium keyword */
article {
  border-style: dotted;
  border-width: medium;
  border-color: rgb(0, 128, 128); /* Teal */
  padding: 10px;
}

/* Example 4: Mixed widths */
aside {
  border-style: solid;
  border-width: 2px 4px 6px 8px; /* Top, right, bottom, left */
  border-color: black;
  padding: 10px;
}
```

**Explanation:**

- **5px:** Border ki thickness 5 pixels hogi.
- **thin:** Thin border (lagbhag 1px).
- **medium:** Medium border (lagbhag 3px).
- **2px 4px 6px 8px:** Border ki width alag-alag sides ke liye set hoti hai.
  - Top = 2px
  - Right = 4px
  - Bottom = 6px
  - Left = 8px

---

## 3. Border Color (`border-color`)

`border-color` property border ka color set karti hai. Color names, hexadecimal values, RGB, RGBA, HSL, ya HSLA formats use kiye ja sakte hain. Yeh property tabhi work karti hai jab `border-style` define ho.

**Examples:**

```css
/* Example 1: Color name */
div {
  border-style: solid;
  border-width: 2px;
  border-color: blue;
  padding: 10px;
}

/* Example 2: Hexadecimal */
section {
  border-style: dashed;
  border-width: 3px;
  border-color: #ffa500; /* Orange */
  padding: 10px;
}

/* Example 3: RGB */
article {
  border-style: double;
  border-width: 4px;
  border-color: rgb(128, 0, 128); /* Purple */
  padding: 10px;
}

/* Example 4: RGBA for transparency */
aside {
  border-style: solid;
  border-width: 2px;
  border-color: rgba(0, 255, 0, 0.5); /* Semi-transparent green */
  padding: 10px;
}
```

**Explanation:**

- **Color Name:** Direct color name use kiya gaya hai (`blue`).
- **Hexadecimal:** `#ffa500` orange color ko represent karta hai.
- **RGB:** `rgb(128, 0, 128)` purple color ko represent karta hai.
- **RGBA:** `rgba(0, 255, 0, 0.5)` semi-transparent green color create karta hai.

---

## 4. Border Shorthand (`border`)

`border` shorthand property ek hi declaration me `border-width`, `border-style`, aur `border-color` ko combine karti hai. Order flexible hota hai, lekin teeno components specify karna zaroori hota hai.

**Examples:**

```css
/* Example 1: Basic shorthand */
div {
  border: 2px solid black;
  padding: 10px;
}

/* Example 2: Shorthand with color name */
section {
  border: 3px dashed red;
  padding: 10px;
}

/* Example 3: Shorthand with RGB */
article {
  border: medium dotted rgb(0, 0, 255);
  padding: 10px;
}

/* Example 4: Shorthand with hexadecimal */
aside {
  border: 4px double #008080; /* Teal */
  padding: 10px;
}
```

**Explanation:**

- `2px solid black` me width, style, aur color ek line me define kiye gaye hain.
- `3px dashed red` dashed red border create karta hai.
- `medium dotted rgb(0, 0, 255)` blue dotted border create karta hai.
- `4px double #008080` teal color ki double border create karta hai.

---

## 5. Types of Borders

`border-style` property different border types support karti hai. Har border type ka apna alag visual effect hota hai.

- **Solid:** Ek single continuous line.
- **Dashed:** Chhoti-chhoti dashes ki series.
- **Dotted:** Chhote dots ki series.
- **Double:** Do parallel lines jinke beech gap hota hai.
- **Groove:** Border carved ya andar dabi hui (3D effect) dikhti hai. Yeh `border-color` par depend karta hai.
- **Ridge:** Groove ka opposite effect, border raised dikhti hai.
- **Inset:** Element andar daba hua ya embedded dikhta hai.
- **Outset:** Inset ka opposite effect, element bahar utha hua dikhta hai.
- **None:** Koi border nahi hoti (default).
- **Hidden:** `none` jaisa hi hota hai, lekin table cell spacing ko affect karta hai.

**Examples:**

```css
/* Example 1: Groove border */
div {
  border: 4px groove #666666;
  padding: 10px;
}

/* Example 2: Ridge border */
section {
  border: 4px ridge #4682b4; /* Steel blue */
  padding: 10px;
}

/* Example 3: Inset border */
article {
  border: 3px inset #800080; /* Purple */
  padding: 10px;
}

/* Example 4: Outset border */
aside {
  border: 3px outset #008000; /* Green */
  padding: 10px;
}
```

**Explanation:**

- **Groove:** Border 3D carved effect deti hai.
- **Ridge:** Border raised ya ubhri hui dikhti hai.
- **Inset:** Element andar press hua hua dikhta hai.
- **Outset:** Element bahar ki taraf raised dikhta hai.

---

## Additional Notes

- **Shorthand Order:** `border` shorthand kisi bhi order me likhi ja sakti hai. Example:
  ```css
  border: solid 2px black;
  ```
  ya
  ```css
  border: 2px black solid;
  ```
  Dono valid hain.

- **Individual Sides:** Agar sirf kisi ek side ki border set karni ho, to `border-top`, `border-right`, `border-bottom`, ya `border-left` use kar sakte ho.

  **Example:**
  ```css
  border-top: 1px solid blue;
  ```

- **Requirement:** `border-width` aur `border-color` tabhi kaam karenge jab `border-style` property define ki gayi ho.