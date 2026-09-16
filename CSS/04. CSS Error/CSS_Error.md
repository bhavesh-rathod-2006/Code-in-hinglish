# Common CSS Errors and How to Fix Them

Yeh guide CSS me hone wali common errors, unke causes (kyun error aati hai), aur unke solutions explain karti hai. Examples W3Schools CSS Tutorial ki guidelines se inspired hain.

---

## 1. Syntax Errors

**Description:** CSS me agar syntax galat ho, jaise semicolon (`;`) miss ho, curly braces (`{}`) properly close na ho, ya property ka naam galat likha ho, to CSS rules kaam nahi karte.

**Example:**

```css
/* Incorrect: Missing semicolon */
p {
  color: blue
}

/* Correct */
p {
  color: blue;
}
```

**Explanation:**

- Pehle example me `color: blue` ke baad semicolon missing hai.
- Dusre example me semicolon add kiya gaya hai, isliye CSS rule sahi tarah apply hoga.

**Solution:**

- Har property-value pair ke baad semicolon (`;`) zaroor lagao.
- Curly braces (`{}`) ko properly open aur close karo.
- Syntax highlighting wale code editor (jaise VS Code) ka use karo taaki errors jaldi identify ho sake.

---

## 2. Incorrect Selector Usage

**Description:** Agar galat selector type use kiya jaye (jaise class ki jagah ID ya ID ki jagah class) ya selector ka spelling galat ho, to style HTML element par apply nahi hota.

**Example:**

```css
/* Incorrect: Using class selector when targeting an ID */
.header {
  background-color: #f0f0f0;
}

/* Correct: Targeting the ID */
#header {
  background-color: #f0f0f0;
}
```

**Explanation:**

- `.header` class selector hai.
- `#header` ID selector hai.
- Agar HTML element me `id="header"` diya hai, to CSS me `#header` hi use karna hoga.

**Solution:**

- Selector type ko dhyan se check karo.
- **Class selector** ke liye `.` use hota hai.
- **ID selector** ke liye `#` use hota hai.
- CSS selector ka naam HTML ke selector se exactly match hona chahiye.

---

## 3. Specificity Issues

**Description:** CSS me jis rule ki specificity zyada hoti hai, woh lower specificity wale rule ko override kar deta hai. Is wajah se kabhi-kabhi unexpected styling dekhne ko milti hai.

**Example:**

```css
/* Lower specificity */
div {
  color: green;
}

/* Higher specificity overrides the above */
#container p {
  color: red;
}
```

**Explanation:**

- `div` selector ki specificity kam hai.
- `#container p` selector me ID use hui hai, isliye iski specificity zyada hai.
- Is case me paragraph ka color **red** ho jayega, green nahi.

**Solution:**

- CSS specificity ka order samjho:
  - Inline CSS
  - ID Selector
  - Class Selector
  - Element Selector
- Browser Developer Tools ka use karke inspect karo ki kaunsa CSS rule apply ho raha hai.
- Zarurat pade to specificity ko sahi tarah adjust karo.

---

## 4. Invalid Property Values

**Description:** Agar CSS property ke liye invalid ya unsupported value use kar di jaye, to browser us property ko ignore kar deta hai.

**Example:**

```css
/* Incorrect: Invalid value for font-size */
p {
  font-size: largepx;
}

/* Correct */
p {
  font-size: 16px;
}
```

**Explanation:**

- `largepx` valid CSS value nahi hai.
- `16px` valid value hai, isliye browser isse apply karega.

**Solution:**

- CSS property ki valid values verify karo.
- Hamesha correct units use karo, jaise:
  - `px`
  - `%`
  - `rem`
  - `em`
- Property aur value dono ko CSS Reference ya documentation se check karo.

---

## Additional Tips

- CSS issues debug karne ke liye browser ke **Developer Tools** ka use karo.
- CSS code ko validate karne ke liye **W3C CSS Validator** jaisi tools use karo.
- CSS properties aur selectors ki detailed documentation ke liye **W3Schools CSS Tutorial** aur **CSS Reference** dekh sakte ho.