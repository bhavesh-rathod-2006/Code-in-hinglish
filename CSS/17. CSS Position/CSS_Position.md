# CSS Positioning

CSS ki `position` property control karti hai ki document mein kisi element ko kaise position kiya jayega. Yeh determine karti hai ki element apni normal position, parent ya viewport ke relative kahan place hoga. Iski help se hum layouts, overlays aur interactive elements ko precisely position kar sakte hain.

## Syntax
```css
position: static | relative | absolute | fixed | sticky;
```

## Values
- **`static`**: Yeh default value hai. Elements normal document flow ko follow karte hain. In par `top`, `right`, `bottom` ya `left` properties ka koi effect nahi hota.
- **`relative`**: Element ko uski normal position ke relative position karta hai. Offset properties (`top`, `right`, `bottom`, `left`) ka use karke element ko shift kar sakte hain, bina doosre elements ki original positioning ko affect kiye.
- **`absolute`**: Element ko normal document flow se remove kar deta hai aur nearest positioned ancestor ke relative position karta hai, jiski `position` value `static` ke alawa kuch bhi ho. Agar aisa koi ancestor nahi hai, toh yeh initial containing block ke relative position hota hai.
- **`fixed`**: Element ko viewport ke relative position karta hai, jisse scrolling ke dauran bhi woh apni position par rehta hai. Offset properties uski position define karti hain.
- **`sticky`**: Yeh `relative` aur `fixed` ka combination hai. Element initially `relative` behave karta hai, lekin scroll karte waqt specified threshold par pahunchne ke baad `fixed` ki tarah stick ho jata hai.

## Key Offset Properties

Yeh properties `relative`, `absolute`, `fixed` aur `sticky` elements ki positioning adjust karti hain:
- `top`: Top edge se distance set karta hai.
- `right`: Right edge se distance set karta hai.
- `bottom`: Bottom edge se distance set karta hai.
- `left`: Left edge se distance set karta hai.

## Relative vs Absolute Positioning in CSS

### 1. `position: relative`
- Element ko document flow mein uski **normal position ke relative** position kiya jata hai.
- Yeh normal document flow mein hi rehta hai, yani iski original space reserved rehti hai.
- `top`, `right`, `bottom` aur `left` properties ka use karke element ko shift kar sakte hain. Yeh values element ko uski original position se move karti hain.
- Doosre elements aise behave karte hain jaise element abhi bhi apni original position par hai. Woh uski khaali jagah ko fill nahi karte.
- Iska use commonly **positioning context** banane ke liye hota hai, taaki iske andar absolutely positioned child elements ko place kiya ja sake.

**Example:**
```css
.box {
  position: relative;
  top: 20px;    /* Element apni normal position se 20px neeche move hoga */
  left: 30px;   /* Element apni normal position se 30px right move hoga */
}
```

---

### 2. `position: absolute`
- Element ko uske **nearest positioned ancestor** ke relative position kiya jata hai. Positioned ancestor woh hota hai jiski `position` value `static` nahi hoti.
- Agar koi positioned ancestor nahi hai, toh element initial containing block ke relative position hota hai.
- Element **normal document flow se remove** ho jata hai. Iske liye normal flow mein koi space reserved nahi rehti aur surrounding elements iski positioning ko ignore karte hain.
- `top`, `right`, `bottom` aur `left` properties element ko positioned parent ke relative exact jagah par place karti hain.

**Example:**
```css
.parent {
  position: relative;   /* Positioning context create karta hai */
}

.child {
  position: absolute;
  top: 10px;
  right: 20px;          /* .parent ke top se 10px aur right se 20px door */
}
```

---

### Key Differences

| Feature                      | `relative`                          | `absolute`                              |
|-----------------------------|-------------------------------------|-----------------------------------------|
| Document flow               | Flow mein rehta hai                 | Flow se remove ho jata hai              |
| Positioning reference       | Apni original position              | Nearest positioned ancestor             |
| Space reserved              | Haan                                | Nahi                                    |
| Affects other elements      | Original space reserved rehti hai   | Normal flow ke doosre elements ko affect nahi karta |
| Common use                  | Small offsets / containing block    | Precise placement / overlays            |
| Stacking context            | `z-index` ke saath create kar sakta hai | `z-index` ke saath create kar sakta hai |

---

### Quick Tips
- Jab kisi child element ko `absolute` position karna ho, toh parent ko `position: relative` dena ek common practice hai.
- Layout ko disturb kiye bina element ko thoda adjust karne ke liye `relative` use karein.
- Tooltips, dropdowns, badges ya floating elements ko position karne ke liye `absolute` use karein.
- Overlapping elements ka stacking order control karne ke liye `z-index` ka use karein.

CSS layouts banate waqt yeh positioning concepts bahut useful hote hain.

## Examples

### Example 1: Relative Positioning for a Subtle Shift

Is example mein button ko uski normal position se thoda shift kiya gaya hai, taaki hover effect create ho sake.

```css
.button {
  position: relative;
  top: 0;
  left: 0;
  transition: all 0.3s ease;
}
.button:hover {
  position: relative;
  top: -5px;
  left: 5px;
}
```
```html
<button class="button">Hover Me</button>
```

**Explanation**: Button normal document flow mein rehta hai, lekin hover karne par 5px upar aur 5px right move hota hai. Isse layout ko disturb kiye bina dynamic effect create hota hai.

### Example 2: Absolute Positioning for a Dropdown Menu

Is example mein dropdown menu create kiya gaya hai, jo button ke neeche display hota hai.

```css
.menu-container {
  position: relative;
  display: inline-block;
}
.dropdown {
  position: absolute;
  top: 100%;
  left: 0;
  background-color: white;
  box-shadow: 0 2px 5px rgba(0,0,0,0.2);
  display: none;
}
.menu-container:hover .dropdown {
  display: block;
}
```
```html
<div class="menu-container">
  <button>Menu</button>
  <div class="dropdown">
    <a href="#">Option 1</a>
    <a href="#">Option 2</a>
  </div>
</div>
```

**Explanation**: `.menu-container` par `position: relative` set hai, isliye `.dropdown` isi container ke relative position hota hai. Jab user mouse ko container par le jata hai, tab dropdown button ke bilkul neeche display hota hai.

### Example 3: Fixed Positioning for a Cookie Banner

Is example mein cookie consent banner ko viewport ke bottom par fixed rakha gaya hai.

```css
.cookie-banner {
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
  background-color: #333;
  color: white;
  padding: 15px;
  text-align: center;
}
```
```html
<div class="cookie-banner">
  We use cookies to improve your experience. <button>Accept</button>
</div>
```

**Explanation**: Banner viewport ke bottom par rehta hai aur page scroll karne par bhi visible hota hai. Isse users cookie consent prompt ko dekh sakte hain.

### Example 4: Sticky Positioning for a Table of Contents

Is example mein table of contents ko sidebar ke top par sticky banaya gaya hai, taaki scrolling ke dauran navigation accessible rahe.

```css
.sidebar {
  height: 400px;
  overflow: auto;
}
.toc {
  position: sticky;
  top: 10px;
  background-color: #f0f0f0;
  padding: 10px;
}
```
```html
<div class="sidebar">
  <div class="toc">
    <a href="#section1">Section 1</a>
    <a href="#section2">Section 2</a>
  </div>
  <p>Long content here...</p>
</div>
```

**Explanation**: Scrolling ke dauran `.toc` sidebar ke top se 10px ki position par stick ho sakta hai. Isse navigation links scroll karte waqt bhi accessible rehte hain.

## Real-Life Use Cases
- **Navigation Bars**: `fixed` positioning ka use top ya bottom navigation bars ke liye hota hai. Jaise news websites ya e-commerce websites par menus ko scrolling ke dauran accessible rakhna.
- **Tooltips/Popovers**: `absolute` positioning ka use tooltips ya popovers ko kisi element ke paas dikhane ke liye hota hai, bina normal layout ko affect kiye.
- **Sticky Sidebars**: Documentation websites par table of contents ya sidebar ko scrolling ke dauran visible rakhne ke liye `sticky` positioning use hoti hai.
- **Modal Dialogs**: Modal popups ko content ke upar display karne ke liye `fixed` ya `absolute` positioning use hoti hai. Inhe aksar viewport ke center mein backdrop ke saath dikhaya jata hai.

## Usage Notes
- **Positioned Ancestor**: `absolute` positioning ke liye parent par `position: relative`, `absolute` ya `fixed` set kiya ja sakta hai, taaki woh positioning context provide kare.
- **Z-Index**: Overlapping elements ka stacking order control karne ke liye `z-index` use karein. Yeh `relative`, `absolute`, `fixed` aur `sticky` jaise positioned elements ke saath kaam karta hai.
- **Document Flow**: `static` aur `relative` normal document flow ko preserve karte hain, jabki `absolute` aur `fixed` elements ko normal flow se remove kar dete hain. Isse layout par effect pad sakta hai.
- **Sticky Requirements**: `sticky` ke liye `top`, `bottom` jaise offset mein se suitable value set karna zaroori hota hai. Parent ki height aur `overflow: auto` ya `overflow: scroll` jaisi properties bhi sticky behavior ko affect kar sakti hain.

## Browser Support
CSS ki `position` property sabhi modern browsers mein supported hai, jaise Chrome, Firefox, Safari, Edge aur Opera. `sticky` ko bhi modern browsers mein achha support milta hai, lekin purane browsers mein compatibility test karna useful ho sakta hai.