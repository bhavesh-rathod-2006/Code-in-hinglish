# CSS Outline

CSS `outline` property kisi element ke **border ke bahar** ek line draw karti hai. Yeh element ke **size ya layout ko affect nahi karti**. Is guide mein outline properties, outline styles ke types, border aur outline ka difference, aur examples cover kiye gaye hain.

## Outline Components

Ek outline ek single layer hoti hai jisme ye properties hoti hain:

1. **Outline Width**: Outline ki thickness (motai) set karti hai.
   - Isse `outline-width` se set kiya jata hai (jaise `px`, `thin` (1px), `medium` (3px), `thick` (5px)).

2. **Outline Style**: Outline line ka style define karti hai.
   - Isse `outline-style` se set kiya jata hai (types niche diye gaye hain).

3. **Outline Color**: Outline ka color set karti hai.
   - Isse `outline-color` se set kiya jata hai (jaise named colors, hex, RGB, ya `invert`).

4. **Outline (Shorthand)**: Width, style, aur color ko ek hi property mein combine karta hai.
   - Syntax: `outline: width style color;`

### Types of Outline Styles

`outline-style` property outline ki appearance define karti hai. Supported values ye hain:

- `none`: Koi outline nahi hoti (default).
- `solid`: Ek single continuous line.
- `dashed`: Chhoti-chhoti dashes ki line.
- `dotted`: Dots ki line.
- `double`: Do parallel lines.
- `groove`: Outline page ke andar carved hui hui lagti hai (3D effect, color par depend karta hai).
- `ridge`: Outline page se raised hui hui lagti hai (`groove` ka opposite).
- `inset`: Element andar daba hua (sunken) lagta hai (3D effect).
- `outset`: Element bahar nikla hua (raised) lagta hai (`inset` ka opposite).
- **Note**: `groove`, `ridge`, `inset`, aur `outset` ka appearance alag-alag browsers mein thoda different ho sakta hai kyunki yeh 3D rendering par depend karta hai.

### Key Notes

- Outline hamesha **border ke bahar** draw hoti hai aur Box Model mein koi extra space nahi leti.
- Outline rectangular hona zaroori nahi hai; yeh dusre elements ke upar overlap bhi kar sakti hai.
- Outline ko accessibility ke liye bahut use kiya jata hai (jaise keyboard navigation ke focus indicators).
- Outline ke individual sides ko control nahi kiya ja sakta (border ki tarah nahi).

## Difference Between Border and Outline

| **Property** | **Border** | **Outline** |
|--------------|------------|-------------|
| **Space** | Space leti hai aur element ke size ko affect karti hai (`box-sizing: content-box` mein include hoti hai). | Space nahi leti aur layout ya dimensions ko affect nahi karti. |
| **Box Model** | Box Model ka part hoti hai (padding aur margin ke beech). | Box Model ke bahar draw hoti hai aur dusre content ke upar float karti hai. |
| **Sides** | Har side ko alag set kar sakte hain (jaise `border-top`, `border-right`). | Sirf sabhi sides par ek saath apply hoti hai, individual side control nahi hota. |
| **Shape** | Hamesha element ke border shape ko follow karti hai (jaise `border-radius`). | Browser rendering ke hisaab se kabhi non-rectangular bhi ho sakti hai. |
| **Use Case** | Decoration aur structure ke liye use hoti hai (jaise content separate karna). | Highlighting aur focus state ke liye use hoti hai (especially accessibility mein). |
| **Rounding** | `border-radius` ko support karti hai, rounded corners banati hai. | `border-radius` ko har browser mein fully respect nahi karti, appearance vary ho sakta hai. |

## Visual Representation

**Outline vs Border Diagram**

*Image description*: Ek rectangular box dikhaya gaya hai jisme content area, padding, aur ek solid border (jaise black) hai. Border ke bahar ek dashed outline (jaise red) draw ki gayi hai jo element ke size ko affect nahi karti. Border Box Model ka part hoti hai, jabki outline uske bahar float karti hai.

## Examples

### Example 1: Solid Outline

Ek div jisme shorthand se solid outline lagayi gayi hai aur border ke saath compare kiya gaya hai.

```html
<div style="width: 200px; height: 100px; padding: 10px; border: 5px solid black; outline: 3px solid blue; background-color: lightblue;">
  This div has a 5px black border and a 3px solid blue outline.
</div>
```

**Output Samjho:**
- Border: **5px solid black**
- Outline: **3px solid blue**
- Outline border ke bahar dikhegi aur element ka size nahi badhega.

---

### Example 2: Dashed Outline with Individual Properties

Dashed outline ko individual properties se set kiya gaya hai.

```html
<div style="width: 200px; height: 100px; padding: 10px; border: 1px solid green; outline-width: 4px; outline-style: dashed; outline-color: red; background-color: lightgreen;">
  This div has a 1px green border and a 4px dashed red outline.
</div>
```

**Output Samjho:**
- Border: **1px solid green**
- Outline Width: **4px**
- Outline Style: **dashed**
- Outline Color: **red**

---

### Example 3: Dotted Outline for Focus State

Button par focus hone par dotted outline apply ki gayi hai.

```html
<button style="padding: 10px; border: 2px solid purple; outline: none;" onfocus="this.style.outline='3px dotted orange';" onblur="this.style.outline='none';">
  Focus this button to see a 3px dotted orange outline outside the 2px purple border.
</button>
```

**Output Samjho:**
- Normal state mein outline nahi dikhegi (`outline: none`).
- Jab button par focus aayega (Tab key ya click se), to **3px dotted orange outline** border ke bahar dikhegi.
- Focus hatne par outline phir se remove ho jayegi.

---

### Example 4: Groove Outline

3D effect ke liye groove outline use ki gayi hai.

```html
<div style="width: 150px; height: 80px; padding: 15px; border: 3px solid navy; outline: 5px groove coral; margin: 20px; background-color: lightyellow;">
  This div has a 3px navy border and a 5px groove coral outline.
</div>
```

**Output Samjho:**
- Border: **3px solid navy**
- Outline: **5px groove coral**
- Groove style ki wajah se outline 3D carved effect jaisi dikhegi.
- Margin ki wajah se element ke bahar **20px** ki space hogi.