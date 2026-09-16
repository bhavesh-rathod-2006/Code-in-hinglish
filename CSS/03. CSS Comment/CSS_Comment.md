# CSS Comments

CSS comments ka use CSS file ke andar explanatory notes ya annotations add karne ke liye kiya jata hai. Yeh developers ko code document karne me help karte hain, jisse code ko samajhna aur maintain karna easy ho jata hai. Browsers comments ko ignore kar dete hain, isliye comments webpage ke rendering ya design par koi effect nahi daalte.

---

## Syntax

CSS comments `/*` aur `*/` ke beech likhe jaate hain. Yeh single-line bhi ho sakte hain aur multi-line bhi.

```css
/* This is a single-line comment */

/* This is a
   multi-line comment */
```

**Explanation:**

- `/*` comment ki beginning ko show karta hai.
- `*/` comment ka ending point hota hai.
- Inke beech jo bhi text likha hota hai, browser usse ignore kar deta hai.

---

## Usage

CSS comments alag-alag purposes ke liye use kiye jaate hain.

- **Documentation:** Kisi specific style ya code section ka purpose explain karne ke liye.
- **Debugging:** Testing ke liye temporarily code ko disable karne ke liye, bina usse delete kiye.
- **Organization:** Stylesheet ke different sections ko separate aur organized rakhne ke liye.
- **Collaboration:** Ek hi project par kaam karne wale dusre developers ko code samajhne me help dene ke liye.

---

## Best Practices

CSS comments likhte waqt in best practices ko follow karna chahiye.

- Clear aur concise language use karo.
- Zyada comments mat likho; sirf complex ya non-obvious code ko explain karo.
- Comments ko us code ke upar ya side me likho jise woh describe kar rahe hain.
- Readability ke liye consistent formatting use karo.

---

## Examples

### Example 1: Documenting a Section

```css
/* Header Styles */
header {
  background-color: #333;
  color: white;
  padding: 20px;
}
```

**Explanation:**

Yeh comment batata hai ki neeche diya gaya CSS code **Header Styles** ke liye hai. Isse stylesheet ko padhna aur samajhna easy ho jata hai.

---

### Example 2: Explaining a Specific Rule

```css
/* Set font size to 16px for better readability */
body {
  font-size: 16px;
  line-height: 1.5;
}
```

**Explanation:**

Yeh comment explain karta hai ki `body` ka font size **16px** isliye set kiya gaya hai taaki text ki readability better ho.

---

### Example 3: Debugging with Comments

```css
/* Temporarily disable background image for testing */
/*
.hero {
  background-image: url('hero.jpg');
}
*/

.hero {
  background-color: #f0f0f0;
}
```

**Explanation:**

Is example me background image wala code comment ke andar daal diya gaya hai, isliye woh temporarily disable ho gaya hai. Testing ke liye `.hero` element par sirf background color apply ho raha hai.

---

### Example 4: Organizing Complex Styles

```css
/* Navigation Bar */
nav {
  display: flex;
  justify-content: space-between;
}

/* Navigation Links */
nav a {
  color: #007bff;
  text-decoration: none;
}

/* Hover Effect for Links */
nav a:hover {
  text-decoration: underline;
}
```

**Explanation:**

Is example me comments ki help se stylesheet ko alag-alag sections me organize kiya gaya hai.

- **Navigation Bar:** Navigation container ki styling.
- **Navigation Links:** Navigation ke links ki styling.
- **Hover Effect for Links:** Mouse hover hone par links ka effect.

---

## Notes

- Comments ko **nested** nahi kiya ja sakta. Example: `/* /* Nested */ */` invalid syntax hai.
- Codebase ko unnecessary clutter se bachane ke liye comments ka use limited aur meaningful rakho.
- Hamesha ensure karo ki comments code ke latest changes ke according relevant aur up-to-date hon.