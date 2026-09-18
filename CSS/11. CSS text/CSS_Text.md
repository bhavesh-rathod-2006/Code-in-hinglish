# CSS Text

CSS `text` properties HTML elements ke andar text ki appearance aur formatting ko control karti hain. Is guide mein `color`, `text-align`, `text-decoration`, `text-transform`, `text-spacing` (`letter-spacing` aur `word-spacing`), aur `text-shadow` ko detail mein samjhaya gaya hai. Har property ke **2 examples** diye gaye hain taaki uska use clearly samajh aaye.

## Text Properties

1. **Text Color**: Text ka color set karta hai.
   - Property: `color`
   - Values: Named colors (jaise `red`), Hex (jaise `#FF0000`), RGB (jaise `rgb(255, 0, 0)`), HSL, etc.

2. **Text Alignment**: Text ki horizontal alignment control karta hai.
   - Property: `text-align`
   - Values: `left`, `right`, `center`, `justify`.

3. **Text Decoration**: Text par decorative lines add ya modify karta hai.
   - Property: `text-decoration`
   - Values: `none`, `underline`, `overline`, `line-through`.
   - Shorthand: `text-decoration: style color thickness;` (Example: `underline red 2px`).

4. **Text Transform**: Text ke letters ka case change karta hai.
   - Property: `text-transform`
   - Values: `uppercase`, `lowercase`, `capitalize`.

5. **Text Spacing**:
   - **Letter Spacing**: Characters ke beech ki space adjust karta hai.
     - Property: `letter-spacing`
     - Values: `px`, `em`, etc. (Negative value bhi use kar sakte hain.)
   - **Word Spacing**: Words ke beech ki space adjust karta hai.
     - Property: `word-spacing`
     - Values: `px`, `em`, etc. (Negative value bhi use kar sakte hain.)

6. **Text Shadow**: Text ke peeche shadow effect add karta hai.
   - Property: `text-shadow`
   - Values: `h-shadow v-shadow blur-radius color`
     (Example: `2px 2px 4px rgba(0, 0, 0, 0.5)`).

### Key Notes

- Text properties sirf **content area** ko style karti hain, element ke layout ko nahi (Border ya Outline ki tarah nahi).
- Zyada tar text properties **inherit** hoti hain, yani parent element se child elements tak apply ho jati hain jab tak override na kiya jaye.
- `text-shadow` visual effect ko enhance karta hai bina layout ko affect kiye.
- `border` Box Model ka part hota hai aur size affect karta hai, `outline` Box Model ke bahar hoti hai aur space nahi leti, jabki text properties sirf content ko style karti hain.

## Examples

### Text Color Examples

#### 1. Hex Color

```html
<p style="color: #FF4500; border: 1px solid black; padding: 10px;">
  This text is orange-red using a hex code (#FF4500).
</p>
```

**Output Samjho:**
- Text ka color **Orange-Red** hoga.
- Hex code `#FF4500` use kiya gaya hai.
- Border aur padding sirf paragraph ko highlight karne ke liye diye gaye hain.

#### 2. RGB Color

```html
<p style="color: rgb(0, 128, 0); border: 1px solid gray; padding: 10px;">
  This text is green using RGB (0, 128, 0).
</p>
```

**Output Samjho:**
- Text ka color **Green** hoga.
- RGB format `rgb(0, 128, 0)` use hua hai.
- Border gray color ka hai.

---

### Text Alignment Examples

#### 1. Center Alignment

```html
<div style="border: 2px solid blue; padding: 10px;">
  <p style="text-align: center;">
    This text is centered within its container.
  </p>
</div>
```

**Output Samjho:**
- Text container ke center mein align hoga.
- `text-align: center` horizontal center alignment deta hai.

#### 2. Justify Alignment

```html
<div style="border: 2px solid green; padding: 10px; width: 300px;">
  <p style="text-align: justify;">
    This text is justified, spreading evenly across the container’s width for a neat appearance.
  </p>
</div>
```

**Output Samjho:**
- Text left aur right dono sides se evenly spread hoga.
- `justify` se paragraph newspaper style alignment mein dikhega.

---

### Text Decoration Examples

#### 1. Underline with Custom Color

```html
<p style="text-decoration: underline blue 2px; color: navy;">
  This text has a 2px blue underline.
</p>
```

**Output Samjho:**
- Text ke niche **Blue underline** hogi.
- Underline ki thickness **2px** hai.
- Text ka color **Navy** hai.

#### 2. Line-Through

```html
<p style="text-decoration: line-through red; color: black; border: 1px solid red; padding: 5px;">
  This text has a red line-through, as if struck out.
</p>
```

**Output Samjho:**
- Text ke beech mein **Red line** dikhegi.
- Yeh strike-out effect jaisa lagega.

---

### Text Transform Examples

#### 1. Uppercase

```html
<h3 style="text-transform: uppercase; color: purple; border: 1px solid purple; padding: 10px;">
  this heading is transformed to uppercase.
</h3>
```

**Output Samjho:**
- Saare letters **UPPERCASE** mein convert ho jayenge.
- Original lowercase text uppercase mein display hoga.

#### 2. Capitalize

```html
<p style="text-transform: capitalize; color: teal;">
  this text capitalizes the first letter of each word.
</p>
```

**Output Samjho:**
- Har word ka first letter capital ho jayega.
- Baaki letters same rahenge.

---

### Letter Spacing Examples

#### 1. Positive Letter Spacing

```html
<p style="letter-spacing: 3px; color: darkblue; border: 1px solid darkblue; padding: 10px;">
  This text has 3px spacing between letters.
</p>
```

**Output Samjho:**
- Har letter ke beech **3px** extra space hogi.
- Text zyada spread out dikhega.

#### 2. Negative Letter Spacing

```html
<p style="letter-spacing: -1px; color: maroon;">
  This text has reduced letter spacing by 1px.
</p>
```

**Output Samjho:**
- Letters ek dusre ke aur paas aa jayenge.
- Spacing **1px** reduce ho jayegi.

---

### Word Spacing Examples

#### 1. Increased Word Spacing

```html
<p style="word-spacing: 5px; color: green; border: 1px solid green; padding: 10px;">
  This text has 5px spacing between words.
</p>
```

**Output Samjho:**
- Har word ke beech **5px** extra gap hoga.
- Sentence zyada spaced dikhega.

#### 2. Negative Word Spacing

```html
<p style="word-spacing: -2px; color: brown; width: 200px;">
  This text has words squeezed closer by 2px.
</p>
```

**Output Samjho:**
- Words ek dusre ke aur paas aa jayenge.
- Gap **2px** kam ho jayega.

---

### Text Shadow Examples

#### 1. Single Shadow

```html
<h2 style="text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5); color: coral;">
  This heading has a black shadow with 2px offset and 4px blur.
</h2>
```

**Output Samjho:**
- Text ke peeche **Black shadow** dikhegi.
- Horizontal offset: **2px**
- Vertical offset: **2px**
- Blur radius: **4px**
- Text ka color **Coral** hai.

#### 2. Multiple Shadows

```html
<h2 style="text-shadow: 1px 1px 2px blue, -1px -1px 2px red; color: white; background: black; padding: 10px;">
  This heading has a blue and red shadow in opposite directions.
</h2>
```

**Output Samjho:**
- Text par **2 shadows** apply hongi.
- Ek shadow **Blue** direction mein hogi.
- Dusri shadow **Red** opposite direction mein hogi.
- White text black background par glowing effect dega.