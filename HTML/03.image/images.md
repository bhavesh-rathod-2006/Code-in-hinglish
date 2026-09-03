# HTML `<img>` Tag and Its Attributes

HTML ka `<img>` tag webpage me image ko embed (display) karne ke liye use hota hai. Yeh ek **self-closing tag** hai jo image ko control karne, uski accessibility improve karne aur performance optimize karne ke liye different attributes support karta hai. Neeche `<img>` tag ke important attributes aur `loading` attribute ke saare possible values detail me explain kiye gaye hain.

---

## 1. `src` Attribute

`src` attribute image file ka path ya URL specify karta hai jo webpage par display hogi.

- **Purpose**: Image ka source define karta hai.
- **Example**:

```html
<img src="flower.jpg" alt="A flower">
```

Is example me `flower.jpg` image HTML file ke same folder me present hai.

---

## 2. `alt` Attribute

`alt` attribute image ke liye alternative text provide karta hai. Agar image load nahi hoti ya screen reader use ho raha ho, to yeh text show/read kiya jata hai.

- **Purpose**: Accessibility improve karta hai aur image ka fallback description provide karta hai.
- **Example**:

```html
<img src="flower.jpg" alt="A red rose in bloom">
```

Agar image load nahi hoti, to **"A red rose in bloom"** text display hoga.

---

## 3. `width` Attribute

`width` attribute image ki width pixels me set karta hai (ya CSS ke through doosri units me bhi set ki ja sakti hai).

- **Purpose**: Image ki display width control karta hai.
- **Example**:

```html
<img src="flower.jpg" alt="Resized flower" width="200">
```

Image ki width **200 pixels** hogi.

---

## 4. `height` Attribute

`height` attribute image ki height pixels me set karta hai (ya CSS ke through bhi set ki ja sakti hai).

- **Purpose**: Image ki display height control karta hai.
- **Example**:

```html
<img src="flower.jpg" alt="Resized flower" width="200" height="150">
```

Image ki width **200 pixels** aur height **150 pixels** hogi.

---

## 5. `loading` Attribute

`loading` attribute browser ko batata hai ki image ko **kab load karna hai**. Isse webpage ki performance improve hoti hai, especially jab page par bahut saari images ho.

- **Purpose**: Image loading behavior control karke page load speed optimize karta hai.

### Possible Values

- **`lazy`**: Image tab load hoti hai jab user us image ke viewport ke paas scroll karta hai. Isse initial page load fast hota hai.
  - **Example**:

    ```html
    <img src="flower.jpg" alt="Lazy loaded flower" width="200" loading="lazy">
    ```

    Image tab load hogi jab viewport ke near aayegi.

- **`eager`**: Image immediately load hoti hai, chahe page me kahin bhi ho. Agar `loading` attribute na diya ho, to generally browser isi behavior ko follow karta hai.
  - **Example**:

    ```html
    <img src="flower.jpg" alt="Eager loaded flower" width="200" loading="eager">
    ```

    Image page parse hote hi load ho jayegi.

- **`auto`**: Browser khud decide karta hai ki image ko `lazy` load kare ya `eager`, apni optimization ke according.
  - **Example**:

    ```html
    <img src="flower.jpg" alt="Auto loaded flower" width="200" loading="auto">
    ```

    Browser automatically best loading behavior choose karega.

### Browser Support

`loading` attribute modern browsers (Chrome, Firefox, Safari, Edge) me support hota hai. Agar browser support nahi karta, to default behavior **eager loading** hota hai.

### Note

- `lazy` use karo un images ke liye jo page ke neeche hain (below the fold).
- `eager` use karo hero image ya important images ke liye jo page load hote hi dikhni chahiye.

---

## 6. `title` Attribute

`title` attribute image par hover karne par ek tooltip show karta hai.

- **Purpose**: Image ke baare me extra information hover par dikhata hai.
- **Example**:

```html
<img src="flower.jpg" alt="Flower with tooltip" width="200" title="This is a red rose">
```

Hover karne par **"This is a red rose"** tooltip show hogi.

---

## 7. `srcset` Attribute

`srcset` attribute ek hi image ke multiple versions provide karta hai, taaki browser device aur screen ke hisaab se best image choose kar sake.

- **Purpose**: Responsive images provide karta hai aur performance improve karta hai.
- **Example**:

```html
<img src="flower.jpg"
     srcset="flower-small.jpg 480w, flower-medium.jpg 800w, flower-large.jpg 1200w"
     alt="Responsive flower"
     width="300">
```

Browser viewport aur screen resolution ke hisaab se best image choose karega.

---

Think about `srcset` from the **browser's perspective**.

Browser ka kaam sirf itna hai:

> **"Developer ne jitni image versions di hain, unme se kaunsi image best quality degi bina unnecessary badi file download kiye?"**

Bas isi concept ko `srcset` kehte hain.

---

## Step 1: Aap Multiple Versions Provide Karte Ho

```html
<img
  src="image-800.jpg"
  srcset="
    image-400.jpg 400w,
    image-800.jpg 800w,
    image-1200.jpg 1200w
"
  sizes="50vw"
  alt="Example">
```

Developer browser ko bol raha hai:

> "Browser, mere paas same image ke 3 alag-alag sizes available hain."

- 400px wide
- 800px wide
- 1200px wide

---

## Step 2: Browser Do Questions Puchta Hai

### Question 1:

**Image page par kitni space occupy karegi?**

Iska answer browser ko `sizes` attribute se milta hai.

Example:

```html
sizes="50vw"
```

Matlab:

> "Image viewport ki width ka 50% occupy karegi."

Agar viewport **1000px** hai:

```text
Image display width = 500px
```

---

### Question 2:

**Image kitni sharp honi chahiye?**

Yeh depend karta hai **Device Pixel Ratio (DPR)** par.

Examples:

- Normal monitor → DPR = 1
- Retina display → DPR = 2
- Kuch smartphones → DPR = 3

Agar:

```text
Display width = 500px
DPR = 2
```

To browser ko actually chahiye:

```text
500 × 2 = 1000px image
```

---

## Step 3: Browser Closest Image Choose Karta Hai

Available images:

```text
400w
800w
1200w
```

Browser ko chahiye:

```text
1000px
```

To browser choose karega:

```text
1200w
```

Kyuki:

```text
800w → Too small
1200w → Sabse closest
```

---

### Another Example

Browser ko chahiye:

```text
380px
```

Browser choose karega:

```text
400w
```

---

Browser ko chahiye:

```text
760px
```

Browser choose karega:

```text
800w
```

---

## Hum Hamesha 1200px Image Download Kyun Nahi Karte?

Kyuki badi image ka file size bhi bada hota hai.

Example:

```text
1200px image = 250 KB
400px image = 40 KB
```

Agar image sirf **300px** width me display ho rahi hai, to 1200px image download karna bandwidth waste karega aur page ko slow bana dega.

---

## Developer's Point of View

Developer ka kaam browser ko force karna nahi hai ki kaunsi image use kare.

Developer ka kaam sirf multiple image sizes provide karna hai.

```html
<img
  src="image-800.jpg"
  srcset="
      image-400.jpg 400w,
      image-800.jpg 800w,
      image-1200.jpg 1200w
"
  sizes="100vw">
```

Uske baad browser khud decide karta hai based on:

1. Display size (`sizes`)
2. Screen width (Viewport)
3. Device Pixel Ratio (Retina ya normal screen)
4. Browser zoom level (kuch situations me)
5. Network conditions (browser optimization)

---

## Simple Analogy

Socho tum pizza order kar rahe ho.

Tum delivery wale ko bolte ho ki options available hain:

- Small
- Medium
- Large

Tum usse yeh nahi bolte ki kaunsa pizza lana hai.

Woh decide karta hai:

- Kitne log kha rahe hain.
- Kitni appetite hai.

Waise hi `srcset` me:

- Developer multiple image sizes provide karta hai.
- Browser user ke device aur page layout ko dekhkar best image choose karta hai.
- Isse quality bhi achhi rehti hai aur unnecessary data download bhi nahi hota.

---

### In One Sentence

**`srcset` attribute developer ko ek hi image ke multiple versions provide karne deta hai, aur browser automatically user ke device ki screen resolution aur image ke display size ke hisaab se best image choose karta hai, taaki quality aur performance dono balance rahein.**

---

## Summary

`<img>` tag HTML ka ek important tag hai jo webpage me images display karne ke liye use hota hai. Iske attributes jaise `src`, `alt`, `width`, `height`, `loading`, `title`, `usemap`, aur `srcset` image ki display, accessibility, responsiveness aur performance ko control karte hain. `loading` attribute ke `lazy`, `eager`, aur `auto` values image loading behavior optimize karte hain, jabki `srcset` browser ko multiple image versions me se best image choose karne ki flexibility deta hai.

---