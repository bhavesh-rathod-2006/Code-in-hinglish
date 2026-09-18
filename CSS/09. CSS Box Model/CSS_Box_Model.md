# CSS Box Model Content

CSS **Box Model** HTML elements ki structure ko rectangular boxes ke form mein define karta hai. Har element ke 4 layers hote hain, jo innermost se outermost order mein hote hain:

1. **Content**: Yeh sabse andar ka area hota hai jahan text, images, ya doosra content display hota hai. Iska size `width` aur `height` properties se set kiya jata hai.
2. **Padding**: Content aur border ke beech ki space ko padding kehte hain. Isse `padding` (shorthand) ya `padding-top`, `padding-right`, `padding-bottom`, `padding-left` se set kiya jata hai.
3. **Border**: Padding ke bahar wali line ya outline ko border kehte hain. Isse `border` (shorthand) ya `border-width`, `border-style`, `border-color` se set kiya jata hai.
4. **Margin**: Border ke bahar ki space ko margin kehte hain. Isse `margin` (shorthand) ya `margin-top`, `margin-right`, `margin-bottom`, `margin-left` se set kiya jata hai.

### Visual Representation

**Box Model Diagram**

Image description: Ek rectangular box ka diagram dikhaya gaya hai jisme layers hain: content (center mein blue), padding (green), border (gray), aur margin (yellow). Content sabse andar hota hai, uske baad padding, phir border, aur sabse bahar margin hota hai.

## Examples

### Example 1: Basic Box Model

Ek `div` jisme content, padding, border, aur margin sab use kiye gaye hain.

```html
<div style="width: 200px; height: 100px; padding: 20px; border: 5px solid black; margin: 30px; background-color: lightblue;">
  This div has content (200x100px), 20px padding, 5px border, and 30px margin.
</div>
```

**Output Samjho:**
- Content size: **200px × 100px**
- Padding: **20px** har side
- Border: **5px solid black**
- Margin: **30px** bahar ki side

---

### Example 2: Box-Sizing: Border-Box

`box-sizing: border-box` use karne se padding aur border bhi width ke andar include ho jate hain.

```html
<div style="box-sizing: border-box; width: 200px; height: 100px; padding: 20px; border: 5px solid blue; margin: 30px; background-color: lightgreen;">
  Total width is 200px, including padding and border.
</div>
```

**Output Samjho:**
- Total width **200px hi rahegi**.
- Padding aur border alag se width increase nahi karenge.
- Yeh responsive layouts mein bahut useful hota hai.

---

### Example 3: Margin Collapse

Do `div` ke margins collapse hone ka example.

```html
<div style="margin-bottom: 20px; border: 1px solid red; padding: 10px;">
  First div (margin-bottom: 20px)
</div>

<div style="margin-top: 30px; border: 1px solid green; padding: 10px;">
  Second div (margin-top: 30px)
</div>

<!-- Space between divs is 30px (larger margin), not 50px -->
```

**Output Samjho:**
- Pehle div ka bottom margin **20px** hai.
- Dusre div ka top margin **30px** hai.
- Dono margins add nahi honge.
- Inke beech ki space **30px** hogi (jo bada margin hai), is process ko **Margin Collapse** kehte hain.

---

### Example 4: Responsive Box with Max-Width

Ek responsive box jo center mein align hota hai aur maximum width set karta hai.

```html
<div style="width: 100%; max-width: 400px; height: 150px; padding: 15px; border: 3px solid purple; margin: 20px auto; background-color: lightyellow;">
  Responsive width, max 400px, with padding, border, and centered margin.
</div>
```

**Output Samjho:**
- Width screen ke hisaab se **100%** hogi.
- Lekin maximum width **400px** se zyada nahi hogi.
- `margin: 20px auto;` box ko horizontally center mein align karta hai.
- Padding aur border bhi apply honge.