# HTML Entities and Symbols

HTML Entities special codes hote hain jo **reserved characters, symbols aur emojis** ko webpage par sahi tarike se display karne ke liye use kiye jaate hain.

Ye ensure karte hain ki HTML parser reserved characters jaise `<`, `>` aur `&` ko code na samjhe, balki normal character ki tarah display kare.

Is guide me HTML entities, symbols aur emojis ko Hinglish me explain kiya gaya hai.

---

## What are HTML Entities?

HTML Entities aise strings hote hain jo **ampersand (`&`) se start** aur **semicolon (`;`) par end** hote hain.

Ye reserved characters, currency symbols, mathematical symbols aur emojis ko represent karte hain.

Entities likhne ke 3 tarike hote hain:

- **Named Entity** → `&copy;`
- **Decimal Entity** → `&#169;`
- **Hexadecimal Entity** → `&#xA9;`

---

### Key Features

- **Reserved Characters:** `<`, `>`, `&` jaise characters ko safely display karte hain.
- **Symbol Support:** Currency, math symbols, arrows aur emojis show karte hain.
- **Formats:** Named, Decimal aur Hexadecimal entities available hoti hain.
- **Accessibility:** Different browsers aur devices par proper rendering ensure karte hain.

---

## Table of Emojis and Symbols with Hexadecimal Values

| **Symbol** | **Description** | **Named Entity** | **Hexadecimal Entity** | **Decimal Entity** |
|------------|-----------------|------------------|------------------------|--------------------|
| 😊 | Smiling Face | — | `&#x1F60A;` | `&#128522;` |
| ✅ | Check Mark Button | — | `&#x2705;` | `&#9989;` |
| ♥ | Heart | `&hearts;` | `&#x2665;` | `&#9829;` |
| → | Right Arrow | `&rarr;` | `&#x2192;` | `&#8594;` |
| ← | Left Arrow | `&larr;` | `&#x2190;` | `&#8592;` |
| ↑ | Up Arrow | `&uarr;` | `&#x2191;` | `&#8593;` |
| © | Copyright | `&copy;` | `&#xA9;` | `&#169;` |
| ® | Registered Trademark | `&reg;` | `&#xAE;` | `&#174;` |
| ™ | Trademark | `&trade;` | `&#x2122;` | `&#8482;` |
| € | Euro | `&euro;` | `&#x20AC;` | `&#8364;` |
| £ | Pound | `&pound;` | `&#xA3;` | `&#163;` |
| ≠ | Not Equal | `&ne;` | `&#x2260;` | `&#8800;` |
| ∑ | Summation | `&sum;` | `&#x2211;` | `&#8721;` |
| ∞ | Infinity | `&infin;` | `&#x221E;` | `&#8734;` |
| – | En Dash | `&ndash;` | `&#x2013;` | `&#8211;` |
| — | Em Dash | `&mdash;` | `&#x2014;` | `&#8212;` |

---

# Common HTML Entities and Examples

Neeche HTML entities ko categories ke according explain kiya gaya hai.

---

## 1. Reserved Characters

Reserved characters HTML me special meaning rakhte hain. Unhe display karne ke liye entities use karni padti hain.

### Example 1: Less Than (`<`)

```html
<p>Use &lt; for the less-than symbol.</p>

<p>Code: if (x &lt; 10) { ... }</p>

<p>Hex: if (x &#x3C; 10) { ... }</p>
```

**Explanation (Hinglish):**

Ye `<` symbol ko safely display karta hai.

---

### Example 2: Greater Than (`>`)

```html
<p>The greater-than symbol is &gt;.</p>

<p>Example: x &gt; y</p>

<p>Hex: x &#x3E; y</p>
```

**Explanation (Hinglish):**

Ye `>` comparison symbol ko display karta hai.

---

### Example 3: Ampersand (`&`)

```html
<p>Use &amp; for the ampersand.</p>

<p>Brand: Smith &amp; Co.</p>

<p>Hex: Smith &#x26; Co.</p>
```

**Explanation (Hinglish):**

Ye company name me `&` symbol show karta hai.

---

## 2. Currency Symbols

Currency symbols ko HTML entities se display kiya jata hai taaki har browser me sahi dikhein.

### Example 1: Euro (€)

```html
<p>Price: &euro;99.99</p>

<p>Cost: &#x20AC;99.99</p>

<p>Total: &#8364;99.99</p>
```

**Explanation (Hinglish):**

Ye Euro currency symbol show karta hai.

---

### Example 2: Pound (£)

```html
<p>Book: &pound;15.00</p>

<p>Fee: &#xA3;20.00</p>

<p>Decimal: &#163;25.00</p>
```

**Explanation (Hinglish):**

Ye British Pound symbol display karta hai.

---

### Example 3: Yen (¥)

```html
<p>Item: &yen;5000</p>

<p>Price: &#xA5;7500</p>

<p>Total: &#165;10000</p>
```

**Explanation (Hinglish):**

Ye Japanese Yen symbol show karta hai.

---

## 3. Mathematical Symbols

Math equations aur technical content ke liye ye entities use hoti hain.

### Example 1: Not Equal (≠)

```html
<p>Use &ne; for inequality.</p>

<p>Equation: x &ne; y</p>

<p>Hex: x &#x2260; y</p>
```

**Explanation (Hinglish):**

Ye `≠` symbol show karta hai.

---

### Example 2: Summation (∑)

```html
<p>Summation: &sum;</p>

<p>Formula: &#x2211; from i=1 to n</p>

<p>Decimal: &#8721; i</p>
```

**Explanation (Hinglish):**

Ye Summation symbol `∑` display karta hai.

---

### Example 3: Infinity (∞)

```html
<p>Infinity: &infin;</p>

<p>Range: x &infin;</p>

<p>Hex: x &#x221E;</p>
```

**Explanation (Hinglish):**

Ye Infinity symbol show karta hai.

---

## 4. Punctuation and Special Characters

Ye entities punctuation aur special characters ko display karti hain.

### Example 1: En Dash (–)

```html
<p>Range: 2023&ndash;2025</p>

<p>Days: Monday&ndash;Friday</p>

<p>Hex: 2020&#x2013;2023</p>
```

**Explanation (Hinglish):**

En Dash ranges dikhane ke liye use hota hai.

---

### Example 2: Em Dash (—)

```html
<p>Use &mdash; for emphasis.</p>

<p>She said &mdash; confidently &mdash; it works.</p>

<p>Hex: She said &#x2014; it works.</p>
```

**Explanation (Hinglish):**

Em Dash sentence ke andar strong pause ya emphasis ke liye use hota hai.

---

### Example 3: Non-Breaking Space (`&nbsp;`)

```html
<p>Keep together: 10&nbsp;km</p>

<p>Distance: 5&nbsp;miles</p>

<p>Hex: 100&nbsp;meters</p>
```

**Explanation (Hinglish):**

`&nbsp;` line break ko prevent karta hai.

---

## 5. Copyright and Trademark Symbols

Legal aur branding symbols ke liye HTML entities use hoti hain.

### Example 1: Copyright (©)

```html
<p>&copy; 2023 Example Inc.</p>

<p>All rights: &#xA9; 2023</p>

<p>Decimal: &#169; 2023</p>
```

**Explanation (Hinglish):**

Ye Copyright symbol display karta hai.

---

### Example 2: Registered Trademark (®)

```html
<p>Brand: Example&reg;</p>

<p>Product: Widget &#xAE;</p>

<p>Decimal: Gadget &#174;</p>
```

**Explanation (Hinglish):**

Ye Registered Trademark symbol show karta hai.

---

### Example 3: Trademark (™)

```html
<p>Product: Gadget&trade;</p>

<p>Brand: Tech &#x2122;</p>

<p>Decimal: Item &#8482;</p>
```

**Explanation (Hinglish):**

Ye Trademark symbol display karta hai.

---

## 6. Arrows and Directional Symbols

Navigation aur diagrams me arrows use kiye jaate hain.

### Example 1: Left Arrow (←)

```html
<p>Back: &larr;</p>

<p>Link: &#x2190; Home</p>

<p>Decimal: &#8592; Start</p>
```

**Explanation (Hinglish):**

Ye Left Arrow show karta hai.

---

### Example 2: Right Arrow (→)

```html
<p>Next: &rarr;</p>

<p>Continue: &#x2192; Page</p>

<p>Decimal: Go &#8594;</p>
```

**Explanation (Hinglish):**

Ye Right Arrow display karta hai.

---

### Example 3: Up Arrow (↑)

```html
<p>Scroll: &uarr;</p>

<p>Top: &#x2191;</p>

<p>Decimal: Up &#8593;</p>
```

**Explanation (Hinglish):**

Ye Up Arrow display karta hai.

---

## 7. Emojis

HTML me emojis numeric entities se display kiye jaate hain.

### Example 1: Smiling Face (😊)

```html
<p>Joy: &#x1F60A;</p>

<p>Reaction: Happy &#x1F60A;</p>

<p>Decimal: Smile &#128522;</p>
```

**Explanation (Hinglish):**

Ye Smiling Face emoji display karta hai.

---

### Example 2: Check Mark Button (✅)

```html
<p>Done: &#x2705;</p>

<p>Task: Complete &#x2705;</p>

<p>Decimal: Approved &#9989;</p>
```

**Explanation (Hinglish):**

Ye Check Mark emoji show karta hai.

---

### Example 3: Heart (♥)

```html
<p>Love: &hearts;</p>

<p>Favorite: &#x2665; Item</p>

<p>Decimal: Like &#9829;</p>
```

**Explanation (Hinglish):**

Ye Heart symbol display karta hai.

---

# Styling Entities with CSS

CSS ki help se entities aur emojis ko attractive banaya ja sakta hai.

## Example: Styled Emoji

```html
<style>
  .emoji {
    font-size: 1.5em;
    color: #e91e63;
  }
</style>

<p>Great work! <span class="emoji">&#x1F60A;</span></p>
```

**Explanation (Hinglish):**

Ye emoji ko bada aur pink color me display karta hai.

---

## Example: Styled Symbol

```html
<style>
  .symbol {
    font-weight: bold;
    color: #0066cc;
  }
</style>

<p>Sum: <span class="symbol">&#x2211;</span></p>
```

**Explanation (Hinglish):**

Ye Summation symbol ko blue aur bold style deta hai.

---

# Best Practices

- Reserved characters (`<`, `>`, `&`) ke liye hamesha entities (`&lt;`, `&gt;`, `&amp;`) use karo.
- Agar available ho to **Named Entities** use karo (`&copy;`, `&euro;`) kyunki ye readable hoti hain.
- Hexadecimal (`&#xA9;`) aur Decimal (`&#169;`) entities bhi browser compatible hoti hain.
- Emojis use karte waqt accessibility improve karne ke liye `aria-label` use kar sakte ho.

```html
<span aria-label="smiling face">&#x1F60A;</span>
```

- Pure project me ek hi entity format consistently use karo.
- Unicode emojis aur symbols ko different browsers me test zarur karo.
- Sirf special characters aur symbols ke liye entities use karo taaki code clean rahe.

---

# Summary

HTML Entities special characters, symbols aur emojis ko safely display karne ke liye use hoti hain.

| **Category** | **Examples** |
|--------------|--------------|
| Reserved Characters | `&lt;`, `&gt;`, `&amp;` |
| Currency Symbols | `&euro;`, `&pound;`, `&yen;` |
| Mathematical Symbols | `&sum;`, `&ne;`, `&infin;` |
| Punctuation | `&ndash;`, `&mdash;`, `&nbsp;` |
| Legal Symbols | `&copy;`, `&reg;`, `&trade;` |
| Arrows | `&larr;`, `&rarr;`, `&uarr;` |
| Emojis | `&#x1F60A;`, `&#x2705;`, `&hearts;` |

HTML Entities ki help se webpage par special characters har browser aur device me sahi tarike se render hote hain aur HTML code bhi error-free rehta hai.