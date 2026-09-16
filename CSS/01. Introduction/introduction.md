# Introduction to CSS

CSS (Cascading Style Sheets) ek stylesheet language hai jo HTML ya XML me likhe hue document ki presentation (design aur appearance) ko describe karti hai. CSS batata hai ki HTML elements screen par, paper par, speech me, ya kisi aur media par kaise display honge. Iski help se web developers webpage ka layout, colors, fonts, spacing, aur overall visual appearance control kar sakte hain, jisse website zyada attractive aur user-friendly ban jaati hai. CSS World Wide Web ki ek core technology hai, HTML aur JavaScript ke saath. Yeh content aur design ko alag rakhta hai, jisse website ko maintain karna, reuse karna, aur accessibility improve karna easy ho jaata hai.

---

# CSS Syntax

CSS syntax rules ka collection hota hai jo define karta hai ki HTML elements ko kaise style kiya jayega. Har CSS rule do main parts se milkar banta hai: **Selector** aur **Declaration Block**.

- **Selector** decide karta hai ki kaunse HTML element ko style karna hai.
- **Declaration Block** ke andar ek ya usse zyada declarations hoti hain.
- Har declaration me ek **Property** aur uski **Value** hoti hai.
- Property aur Value ke beech colon (`:`) use hota hai.
- Har declaration semicolon (`;`) se end hoti hai.
- Pura declaration block curly braces (`{}`) ke andar likha jata hai.

## Basic Syntax Structure

```css
selector {
  property: value;
  property: value;
}
```

- **Selector**: HTML element(s) ko identify karta hai jinko style karna hai. Examples: `h1`, `p`, `.class`, `#id`.
- **Property**: Style ka attribute hota hai jo change karna hai. Examples: `color`, `font-size`, `margin`.
- **Value**: Property ko assign ki gayi value hoti hai. Examples: `blue`, `16px`, `10px`.

## Example of CSS Syntax

```css
h1 {
  color: blue;
  font-size: 24px;
  text-align: center;
}
```

Is example me:

- Selector `h1` sabhi `<h1>` elements ko target karta hai.
- `color: blue;` heading ka text color blue kar deta hai.
- `font-size: 24px;` heading ka font size 24 pixels set karta hai.
- `text-align: center;` heading ko center align karta hai.

## Applying CSS Syntax in Practice

Neeche example diya gaya hai jisme HTML document ke andar CSS ke **Inline**, **Internal**, aur **External** tino types use kiye gaye hain.

### HTML File (`index.html`)

```html
<!DOCTYPE html>
<html>
<head>
  <title>CSS Syntax Example</title>
  <link rel="stylesheet" href="styles.css">
  <style>
    /* Internal CSS */
    p {
      color: green;
      font-size: 18px;
    }
  </style>
</head>
<body>
  <h1 style="color: purple; font-size: 28px;">This is an Inline CSS Heading</h1>
  <p>This paragraph uses Internal CSS.</p>
  <div class="external">This div uses External CSS.</div>
</body>
</html>
```

### CSS File (`styles.css`)

```css
/* External CSS */
.external {
  background-color: lightgray;
  padding: 10px;
  text-align: center;
}
```

**Explanation:**

- **Inline CSS:** `<h1>` element ke andar `style` attribute use karke CSS directly apply ki gayi hai (`color: purple; font-size: 28px;`).
- **Internal CSS:** `<head>` section ke andar `<style>` tag me sabhi `<p>` elements ke liye CSS rules likhe gaye hain (`color: green; font-size: 18px;`).
- **External CSS:** `styles.css` file me `.external` class define ki gayi hai jo `<div>` element ko light gray background, padding, aur center alignment deti hai.

---

# Types of CSS

CSS ko HTML document me apply karne ke **3 primary ways** hote hain:

1. **Inline CSS**
2. **Internal CSS**
3. **External CSS**

Har method ka apna use case, advantage, aur limitation hota hai.

---

## 1. Inline CSS

Inline CSS directly HTML element ke andar `style` attribute ki help se apply ki jaati hai. Yeh quick aur one-time styling ke liye useful hoti hai, lekin bade projects me use karna recommend nahi kiya jata kyunki isse HTML aur CSS mix ho jate hain aur code maintain karna difficult ho jata hai.

**Example:**

```html
<h1 style="color: blue; font-family: Arial;">This is an Inline CSS Heading</h1>

<p style="font-size: 16px; color: green;">
  This paragraph uses inline CSS for styling.
</p>
```

---

## 2. Internal CSS

Internal CSS `<style>` tag ke andar likhi jaati hai jo HTML document ke `<head>` section me hota hai. Yeh single-page website ya ek hi HTML page ke multiple elements ko style karne ke liye suitable hoti hai. Is method me HTML aur CSS ek hi file me rehte hain.

**Example:**

```html
<!DOCTYPE html>
<html>
<head>
  <title>Internal CSS Example</title>
  <style>
    h1 {
      color: purple;
      font-family: Verdana;
    }

    p {
      font-size: 18px;
      color: darkblue;
    }
  </style>
</head>
<body>
  <h1>This is an Internal CSS Heading</h1>
  <p>This paragraph uses internal CSS for styling.</p>
</body>
</html>
```

---

## 3. External CSS

External CSS me CSS rules ek alag `.css` file me likhe jate hain. HTML document us CSS file ko `<link>` tag ki help se connect karta hai. Yeh large websites ke liye sabse efficient aur recommended method hai kyunki ek hi CSS file ko multiple HTML pages me reuse kiya ja sakta hai. Isse code maintain karna aur update karna easy ho jata hai.

**Example:**

### HTML File (`index.html`)

```html
<!DOCTYPE html>
<html>
<head>
  <title>External CSS Example</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <h1>This is an External CSS Heading</h1>
  <p>This paragraph uses external CSS for styling.</p>
</body>
</html>
```

### CSS File (`styles.css`)

```css
h1 {
  color: red;
  font-family: Georgia;
}

p {
  font-size: 20px;
  color: black;
}
```