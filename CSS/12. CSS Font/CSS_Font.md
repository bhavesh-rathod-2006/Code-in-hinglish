# CSS Fonts

CSS `font` properties text ki appearance ko control karti hain. Yeh text ka typeface (font), size, style aur doosri characteristics define karti hain. Is guide mein `font-family`, web-safe fonts, font fallbacks, `font-style`, `font-size`, Google Fonts, font pairing, aur `font` shorthand ko detail mein explain kiya gaya hai. Har property ke **2 practical examples** diye gaye hain, jo W3Schools se inspire hain. Har example ka purpose aur usage bhi explain kiya gaya hai.

## Font Properties

### 1. Font Family

- **Explanation**: `font-family` property text ka typeface set karti hai. Aap specific font ya generic family (jaise `serif`, `sans-serif`, `monospace`) use kar sakte ho. Multiple fonts comma se likhe jaate hain taaki agar pehla font available na ho to browser next font use kare. Last mein hamesha ek generic family deni chahiye reliability ke liye. Jinke naam mein space ho unhe quotes mein likhna padta hai (jaise `"Times New Roman"`).
- **Purpose**: Text ka visual style define karti hai, jo readability aur design ko affect karta hai.
- **Values**: Font names (jaise `Arial`, `"Times New Roman"`), generic families (jaise `serif`, `sans-serif`).

### 2. Web-Safe Fonts

- **Explanation**: Web-safe fonts woh fonts hote hain jo almost har operating system aur browser mein available hote hain. Isse text sab devices par same tarah render hota hai bina external font download kiye.
- **Purpose**: Cross-device compatibility aur consistent design maintain karna.
- **Common Web-Safe Fonts**: `Arial`, `Helvetica`, `Times New Roman`, `Courier New`, `Verdana`, `Georgia`.

### 3. Font Fallbacks

- **Explanation**: Font fallbacks alternative fonts hote hain jo `font-family` mein list kiye jaate hain. Browser pehle font ko try karta hai, agar available nahi ho to next font use karta hai. Agar koi bhi available na ho to generic family use hoti hai.
- **Purpose**: Font rendering ko reliable banana aur backup fonts provide karna.
- **Syntax**: `font-family: primary-font, fallback-font, generic-family;`

### 4. Font Style

- **Explanation**: `font-style` property text ko normal, italic ya oblique banati hai. `italic` font ka asli italic version use karta hai, jabki `oblique` normal font ko thoda slant karta hai.
- **Purpose**: Text ko emphasis ya stylish appearance dena.
- **Values**: `normal`, `italic`, `oblique`.

### 5. Font Size

- **Explanation**: `font-size` property text ka size set karti hai. `px` fixed size deta hai, `rem` aur `em` relative size dete hain, aur keywords jaise `small`, `large` predefined sizes provide karte hain.
- **Purpose**: Readability aur visual hierarchy control karna.
- **Values**: `px`, `%`, `em`, `rem`, `vw`, `vh`, keywords (jaise `medium`, `large`).

### 6. Google Fonts

- **Explanation**: Google Fonts free web fonts hote hain jo `<link>` tag ya `@import` ke through website mein add kiye ja sakte hain. Font include karne ke baad use `font-family` mein fallback ke saath use karte hain.
- **Purpose**: Modern aur high-quality fonts use karna.
- **Usage**: `<link href="https://fonts.googleapis.com/css2?family=FontName&display=swap" rel="stylesheet">` add karo, phir `font-family: 'FontName', fallback;` use karo.

### 7. Font Pairing

- **Explanation**: Font pairing ka matlab do ya zyada fonts ko combine karke attractive aur balanced design banana hai. Usually serif font ko sans-serif font ke saath pair kiya jata hai ya same font family ke different weights use kiye jaate hain.
- **Purpose**: Design ko visually appealing banana aur content hierarchy improve karna.
- **Tips**: Serif + Sans-serif ka combination use karo aur ek design mein maximum 2–3 fonts hi use karo.

### 8. Font Shorthand

- **Explanation**: `font` shorthand ek hi line mein multiple font properties set karta hai. Isme `font-style`, `font-weight`, `font-size`, `line-height`, aur `font-family` include ho sakte hain. `font-size` aur `font-family` mandatory hote hain.
- **Purpose**: Multiple font properties ko short aur clean code mein likhna.
- **Syntax**: `font: style weight size/line-height family;`

### Key Notes

- Font properties sirf text content ko affect karti hain, element ke layout ko nahi (Border aur Outline ki tarah nahi).
- Zyada tar font properties inherited hoti hain, yani child elements tak apply ho jati hain jab tak override na kiya jaye.
- Web-safe fonts aur fallbacks compatibility ensure karte hain, jabki Google Fonts modern design provide karte hain.
- Font pairing carefully choose karni chahiye taaki readability aur visual balance bana rahe.
- `font` shorthand code ko short banata hai, lekin `font-size` aur `font-family` dena zaroori hota hai.

## Examples

### Font Family

**Explanation:** Typeface specify karta hai aur compatibility ke liye fallback fonts use karta hai.

#### 1. Arial with Sans-Serif Fallback

```html
<p style="font-family: Arial, sans-serif; color: blue; border: 1px solid blue; padding: 10px;">
  This text uses Arial, falling back to sans-serif if Arial is unavailable.
</p>
```

**Effect:** Agar Arial available hai to wahi use hoga, warna browser ka default sans-serif font use hoga.

#### 2. Times New Roman with Serif Fallback

```html
<p style="font-family: 'Times New Roman', Georgia, serif; color: darkred; border: 1px solid gray; padding: 10px;">
  This text tries Times New Roman, then Georgia, then a serif font.
</p>
```

**Effect:** Browser pehle Times New Roman try karega, phir Georgia, aur last mein koi generic serif font use karega.

---

### Web-Safe Fonts

**Explanation:** Aise fonts jo almost sab devices mein available hote hain.

#### 1. Verdana

```html
<div style="border: 2px solid green; padding: 10px;">
  <p style="font-family: Verdana, sans-serif; font-size: 16px;">
    This text uses web-safe Verdana, ensuring consistent display across devices.
  </p>
</div>
```

**Effect:** Verdana clean aur readable sans-serif look deta hai jo har device par consistent hota hai.

#### 2. Courier New

```html
<p style="font-family: 'Courier New', monospace; font-size: 14px; border: 1px solid navy; padding: 10px;">
  This text uses web-safe Courier New for a monospaced, typewriter-like style.
</p>
```

**Effect:** Courier New fixed-width aur typewriter jaisa style deta hai, jo coding text ke liye useful hota hai.

---

### Font Fallbacks

**Explanation:** Primary font unavailable hone par backup fonts use hote hain.

#### 1. Helvetica to Arial Fallback

```html
<p style="font-family: Helvetica, Arial, sans-serif; color: teal; padding: 5px;">
  This text tries Helvetica, then Arial, then sans-serif.
</p>
```

**Effect:** Browser pehle Helvetica use karega, phir Arial, aur last mein sans-serif font.

#### 2. Palatino to Serif Fallback

```html
<p style="font-family: 'Palatino Linotype', 'Book Antiqua', serif; color: purple; border: 1px solid purple; padding: 10px;">
  This text tries Palatino Linotype, then Book Antiqua, then serif.
</p>
```

**Effect:** Palatino Linotype priority hogi, warna Book Antiqua ya generic serif font use hoga.

---

### Font Style

**Explanation:** Text ko normal, italic ya oblique appearance deta hai.

#### 1. Italic Style

```html
<p style="font-style: italic; font-family: Georgia, serif; color: maroon; border: 1px solid maroon; padding: 10px;">
  This text is italicized in Georgia for a slanted, elegant look.
</p>
```

**Effect:** Georgia ka italic version text ko elegant slanted look deta hai.

#### 2. Oblique Style

```html
<p style="font-style: oblique; font-family: Arial, sans-serif; color: navy; border: 1px solid navy; padding: 10px;">
  This text uses oblique style in Arial, slanting the normal font.
</p>
```

**Effect:** Arial ka normal font slant ho jata hai aur italic jaisa effect deta hai.

---

### Font Size

**Explanation:** Text ka size control karta hai.

#### 1. Fixed Pixel Size

```html
<h3 style="font-size: 20px; font-family: Verdana, sans-serif; color: blue;">
  This heading is 20px in size, ensuring a fixed scale.
</h3>
```

**Effect:** Heading ka size fixed 20px hoga.

#### 2. Relative Rem Size

```html
<p style="font-size: 1.2rem; font-family: Arial, sans-serif; color: green; border: 1px solid green;">
  This text is 1.2rem, scaling relative to the root font size.
</p>
```

**Effect:** Root font size ke according dynamically scale hoga (Example: 16px × 1.2 = 19.2px).

---

### Google Fonts

**Explanation:** Google ke free hosted fonts use karta hai.

#### 1. Roboto

```html
<link href="https://fonts.googleapis.com/css2?family=Roboto&display=swap" rel="stylesheet">

<p style="font-family: 'Roboto', sans-serif; font-size: 16px; color: orange; border: 1px solid orange; padding: 10px;">
  This text uses Google's Roboto font with a sans-serif fallback.
</p>
```

**Effect:** Roboto modern aur clean font look deta hai. Agar load na ho to sans-serif use hoga.

#### 2. Lora

```html
<link href="https://fonts.googleapis.com/css2?family=Lora&display=swap" rel="stylesheet">

<p style="font-family: 'Lora', serif; font-size: 18px; color: darkred; border: 1px solid darkred; padding: 10px;">
  This text uses Google's Lora font, a serif typeface.
</p>
```

**Effect:** Lora elegant serif style provide karta hai, fallback mein serif font use hoga.

---

### Font Pairing

**Explanation:** Do fonts combine karke balanced aur attractive design banana.

#### 1. Serif and Sans-Serif Pairing

```html
<div style="border: 2px solid teal; padding: 10px;">
  <h2 style="font-family: Georgia, serif; font-size: 24px; color: teal;">
    Georgia Heading (Serif)
  </h2>

  <p style="font-family: Helvetica, sans-serif; font-size: 16px;">
    Helvetica body text (Sans-Serif) for contrast and readability.
  </p>
</div>
```

**Effect:** Georgia heading aur Helvetica body text milkar clean contrast aur readability create karte hain.

#### 2. Same Font, Different Weights

```html
<link href="https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;700&display=swap" rel="stylesheet">

<div style="border: 2px solid purple; padding: 10px;">
  <h2 style="font-family: 'Open Sans', sans-serif; font-weight: 700; font-size: 20px;">
    Bold Open Sans Heading
  </h2>

  <p style="font-family: 'Open Sans', sans-serif; font-weight: 400; font-size: 14px;">
    Regular Open Sans body text for a cohesive look.
  </p>
</div>
```

**Effect:** Same font family ke bold aur regular weights se clear hierarchy create hoti hai.

---

### Font Shorthand

**Explanation:** Multiple font properties ko ek hi line mein set karta hai.

#### 1. Basic Shorthand

```html
<p style="font: italic 16px Arial, sans-serif; color: navy; border: 1px solid navy; padding: 10px;">
  This text uses italic 16px Arial via shorthand.
</p>
```

**Effect:** Ek hi line mein italic style, 16px size aur Arial font apply ho jata hai.

#### 2. Shorthand with Line-Height and Weight

```html
<p style="font: bold 18px/1.6 'Times New Roman', serif; color: darkgreen; border: 1px solid darkgreen; padding: 10px;">
  This text uses bold 18px Times New Roman with 1.6 line-height.
</p>
```

**Effect:** Bold weight, 18px font size, 1.6 line-height aur Times New Roman font ek hi shorthand property se apply ho jata hai.