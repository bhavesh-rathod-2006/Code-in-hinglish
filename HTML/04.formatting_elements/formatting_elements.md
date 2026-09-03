# HTML Formatting Elements

HTML me different **formatting elements** hote hain jo webpage ke text ko style aur structure dene ke liye use kiye jaate hain. Yeh elements text ko zyada readable, attractive aur semantic (meaningful) banate hain. Neeche common HTML formatting elements ki explanation di gayi hai.

---

## 1. `<b>` - Bold Text

`<b>` element text ko **bold** banata hai. Yeh sirf text ka visual appearance change karta hai, semantic importance nahi batata.

- **Purpose**: Text ko visually highlight karna.
- **Example**:

```html
<p>Learn programming at <b>Coding Gita</b> to master web development.</p>
```

Is example me **"Coding Gita"** bold dikhai dega.

---

## 2. `<i>` - Italic Text

`<i>` element text ko **italic** banata hai. Yeh aksar special words, foreign terms ya visual emphasis ke liye use hota hai.

- **Purpose**: Text ko visual emphasis dena ya alternate style dikhana.
- **Example**:

```html
<p>SwamiNarayan University offers courses in <i>Computer Science</i>.</p>
```

Is example me **"Computer Science"** italic dikhai dega.

---

## 3. `<strong>` - Important Text

`<strong>` element important text ko indicate karta hai. Browser ise bold dikhata hai, lekin iski semantic importance bhi hoti hai.

- **Purpose**: Important content ko emphasize karna (Accessibility aur SEO ke liye useful).
- **Example**:

```html
<p><strong>Coding Gita</strong> provides hands-on coding workshops for beginners.</p>
```

Is example me **"Coding Gita"** bold hoga aur important maana jayega.

---

## 4. `<em>` - Emphasized Text

`<em>` element text ko emphasize karta hai. Browser ise generally italic dikhata hai aur semantic emphasis bhi add hota hai.

- **Purpose**: Stress ya importance show karna.
- **Example**:

```html
<p>At SwamiNarayan University, students are <em>encouraged</em> to innovate.</p>
```

Is example me **"encouraged"** italic aur emphasized hoga.

---

## 5. `<mark>` - Highlighted Text

`<mark>` element text ko highlight karta hai, usually yellow background ke saath.

- **Purpose**: Important ya noteworthy text ko highlight karna.
- **Example**:

```html
<p>Join <mark>Coding Gita</mark> for the latest AI programming course!</p>
```

Is example me **"Coding Gita"** highlighted dikhai dega.

---

## 6. `<small>` - Smaller Text

`<small>` element text ka font size chhota kar deta hai.

- **Purpose**: Secondary information ya side notes dikhane ke liye.
- **Example**:

```html
<p>SwamiNarayan University offers degrees. <small>Apply by December!</small></p>
```

Is example me **"Apply by December!"** chhote font me dikhai dega.

---

## 7. `<del>` - Deleted Text

`<del>` element deleted text ko show karta hai, generally strikethrough ke saath.

- **Purpose**: Batana ki yeh text remove ya outdated ho chuka hai.
- **Example**:

```html
<p>Coding Gita's old course fee: <del>$100</del>. New fee: $80.</p>
```

Is example me **"$100"** par line (strikethrough) hogi.

---

## 8. `<ins>` - Inserted Text

`<ins>` element newly added text ko underline karke show karta hai.

- **Purpose**: Naya add kiya hua content highlight karna.
- **Example**:

```html
<p>SwamiNarayan University now offers <ins>Data Science</ins> programs.</p>
```

Is example me **"Data Science"** underline hoga.

---

## 9. `<sub>` - Subscript Text

`<sub>` element text ko baseline ke neeche show karta hai.

- **Purpose**: Chemical formulas, mathematical notation ya footnotes ke liye.
- **Example**:

```html
<p>Coding Gita teaches algorithms like A<sub>n</sub> for sorting.</p>
```

Is example me **"n"** subscript me dikhai dega.

---

## 10. `<sup>` - Superscript Text

`<sup>` element text ko baseline ke upar show karta hai.

- **Purpose**: Exponents, ordinal numbers ya mathematical powers ke liye.
- **Example**:

```html
<p>SwamiNarayan University's 2<sup>nd</sup> annual tech fest is coming!</p>
```

Is example me **"nd"** superscript me dikhai dega.

---

# HTML Quotation and Citation Elements

HTML me kuch special elements hote hain jo quotations, abbreviations, contact information aur text direction ko semantic way me represent karte hain. Inme `<blockquote>`, `<q>`, `<abbr>`, `<address>`, `<cite>`, aur `<bdo>` include hote hain.

---

## 1. `<blockquote>` Element

`<blockquote>` element kisi doosre source se liye gaye **long quotation** ko define karta hai. Browser ise generally indentation ke saath display karta hai.

- **Attributes**
  - `cite`: Quote ka source URL specify karta hai (browser me visible nahi hota, lekin accessibility aur scripts ke liye useful hota hai).

- **Example**

```html
<p>From a recent Coding Gita workshop:</p>

<blockquote cite="https://codinggita.com/workshops">
  Our practical sessions focus on real-world coding projects to enhance student skills.
</blockquote>
```

Is example me quotation indent hokar show hogi aur `cite` attribute uska source define karega.

---

## 2. `<q>` Element

`<q>` element ek **short inline quotation** ke liye use hota hai. Browser automatically quotation marks add karta hai.

- **Attributes**
  - `cite`: Quote ka source URL specify karta hai.

- **Example**

```html
<p>
  SwamiNarayan University’s mission is:
  <q cite="https://swaminarayanuniversity.ac.in/about">
    To foster innovation through practical learning.
  </q>
</p>
```

Is example me quotation marks automatically show honge.

---

## 3. `<abbr>` Element

`<abbr>` element abbreviation ya acronym define karta hai. Hover karne par full form tooltip me dikhai deti hai.

- **Attributes**
  - `title`: Abbreviation ka full form ya description.

- **Example**

```html
<p>
  Coding Gita collaborates with
  <abbr title="SwamiNarayan University">SNU</abbr>
  for advanced tech programs.
</p>
```

Hover karne par **"SwamiNarayan University"** tooltip me show hoga.

---

## 4. `<address>` Element

`<address>` element document ya article ke author ya owner ki contact information show karta hai.

- **Attributes**
  - Global attributes support karta hai (`class`, `id`, etc.).

- **Example**

```html
<address>
  Coding Gita <br>
  Shree Swaminarayan Vishvamangal Gurukul <br>
  Ahmedabad-Mehsana Highway, Saij, Kalol <br>
  Gandhinagar, Gujarat 382725
</address>
```

Is example me address italics aur line breaks ke saath display hoga.

---

## 5. `<cite>` Element

`<cite>` element kisi creative work ka **title** define karta hai, jaise book, article, course, movie ya painting.

- **Attributes**
  - Global attributes support karta hai.

- **Example**

```html
<p><cite>Full Stack Development 2025</cite> is a flagship course by Coding Gita.</p>
```

Is example me **"Full Stack Development 2025"** italics me show hoga.

> **Note:** Kisi person ka naam `<cite>` me nahi likhna chahiye, kyunki `<cite>` sirf creative work ke title ke liye hota hai.

---

## 6. `<bdo>` Element

`<bdo>` (Bi-Directional Override) text ki direction ko override karta hai. Yeh RTL (Right-to-Left) languages ke liye useful hai.

- **Attributes**
  - `dir`: Text direction set karta hai (`ltr` ya `rtl`).

- **Example**

```html
<p>
  SwamiNarayan University supports multilingual coding sessions,
  e.g., <bdo dir="rtl">કોડિંગ</bdo> for Gujarati.
</p>
```

Is example me Gujarati text Right-to-Left direction me display hoga.

---

## `<blockquote>` vs `<cite>`

`<blockquote>` aur `<cite>` dono quotation se related hain, lekin dono ka purpose alag hai.

---

# 1. `<blockquote>` – Long Quotations Ke Liye

`<blockquote>` tab use hota hai jab aap kisi doosre source ka **lamba quotation** dikhana chahte ho.

### Real-life Use Cases

### Use Case 1: Famous Person Ka Quote

```html
<blockquote>
  The greatest glory in living lies not in never falling,
  but in rising every time we fall.
</blockquote>
```

---

### Use Case 2: Customer Testimonial

```html
<blockquote>
  This course completely changed my career.
  I got my first developer job within three months.
</blockquote>
```

---

### Use Case 3: Book Excerpt

```html
<blockquote>
  It was the best of times,
  it was the worst of times...
</blockquote>
```

---

### Use Case 4: News Article

```html
<blockquote>
  The minister announced that new education policies
  will come into effect next year.
</blockquote>
```

---

### Use Case 5: Research Paper

```html
<blockquote>
  Artificial Intelligence has become one of the fastest
  growing technologies in recent years.
</blockquote>
```

---

# 2. `<cite>` – Source Ya Title Mention Karne Ke Liye

`<cite>` quote ko contain nahi karta. Yeh us quotation ke **source** ya kisi creative work ka **title** batata hai.

### Use Case 1: Book Name

```html
<p>I recently read <cite>Atomic Habits</cite>.</p>
```

---

### Use Case 2: Movie Title

```html
<p>My favorite movie is <cite>Interstellar</cite>.</p>
```

---

### Use Case 3: Website Name

```html
<p>According to <cite>MDN Web Docs</cite>, the picture element...</p>
```

---

### Use Case 4: Research Paper Title

```html
<p>
  The findings are discussed in
  <cite>Deep Learning for Image Recognition</cite>.
</p>
```

---

### Use Case 5: Painting

```html
<p><cite>Mona Lisa</cite> was painted by Leonardo da Vinci.</p>
```

---

# Using Both Together (Most Common)

```html
<blockquote>
  Stay hungry. Stay foolish.
</blockquote>

<cite>Steve Jobs – Stanford Commencement Speech (2005)</cite>
```

Yahan `<blockquote>` quote ko show karta hai aur `<cite>` us quote ka source batata hai.

---

# Kab `<blockquote>` Use Nahi Karna Chahiye

❌ Agar quote sentence ke andar chhota ho.

```html
<p>Steve Jobs said, "Stay hungry. Stay foolish."</p>
```

Is situation me `<q>` use karna chahiye.

```html
<p>Steve Jobs said, <q>Stay hungry. Stay foolish.</q></p>
```

---

## Quick Comparison

| Situation | Element |
|-----------|---------|
| Book, speech, article ya interview se long quotation | `<blockquote>` |
| Sentence ke andar short quotation | `<q>` |
| Book, movie, song, website, research paper ya painting ka title | `<cite>` |
| Quotation ka source ya creative work mention karna | `<cite>` (common usage) |

---

## Example Combining Multiple Elements

```html
<p>According to the <abbr title="SwamiNarayan University">SNU</abbr>:</p>

<blockquote cite="https://swaminarayanuniversity.ac.in/news">
  <p>Our practical sessions integrate real-world projects for hands-on learning.</p>

  <cite>— University Newsletter, 2025</cite>
</blockquote>

<p>Contact us at:</p>

<address>
  Coding Gita Campus <br>
  Ahmedabad-Mehsana Highway, Saij, Kalol <br>
  Gandhinagar, Gujarat 382725
</address>

<p>
  The workshop emphasized:
  <q cite="https://codinggita.com/mission">
    Coding is a skill for the future.
  </q>
</p>

<p>
  For multilingual support, see
  <bdo dir="rtl">ગુજરાતી</bdo>
  integration.
</p>
```

Is example me `<abbr>`, `<blockquote>`, `<cite>`, `<address>`, `<q>`, aur `<bdo>` ek saath use kiye gaye hain taaki semantic aur accessible HTML structure ban sake.

---

## Summary

`<blockquote>`, `<q>`, `<abbr>`, `<address>`, `<cite>`, aur `<bdo>` HTML ke semantic elements hain jo quotations, abbreviations, contact information aur text direction ko sahi tarike se represent karte hain.

- **`<blockquote>`** → Long quotation ke liye.
- **`<q>`** → Short inline quotation ke liye.
- **`<abbr>`** → Abbreviation ka full form hover par dikhane ke liye.
- **`<address>`** → Contact information ke liye.
- **`<cite>`** → Creative work ka title ya quotation ka source batane ke liye.
- **`<bdo>`** → Text direction (`ltr` ya `rtl`) override karne ke liye.

In elements ko use karne se webpage zyada semantic, accessible aur SEO-friendly banta hai.

---