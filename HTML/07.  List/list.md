# HTML List

HTML Lists ka use items ko **organize** aur **structured format** me display karne ke liye hota hai. Lists do main types ki hoti hain: **Ordered (Numbered)** aur **Unordered (Bulleted)**. HTML me nested lists aur description lists bhi available hain jo special use cases ke liye use hoti hain.

## List Elements

- `<ul>`: **Unordered List** define karta hai. Isme items bullet points ke saath display hote hain.
- `<ol>`: **Ordered List** define karta hai. Isme items numbers ya letters ke saath display hote hain.
- `<li>`: List ke andar ek **list item** define karta hai. Ye `<ul>` aur `<ol>` dono ke andar use hota hai.
- `<dl>`: **Description List** define karta hai jisme terms aur unki descriptions hoti hain.
- `<dt>`: Description list ke andar **term (title)** define karta hai.
- `<dd>`: Term ki **description** define karta hai.

## List Attributes

Neeche list elements ke important attributes diye gaye hain. Kuch attributes (jaise `type` aur `start`) aaj bhi support hote hain.

### `<ul>` Attributes

- `type` *(Deprecated)*: Bullet style specify karta hai.
  - `disc` → Filled circle bullet.
  - `circle` → Hollow circle bullet.
  - `square` → Square bullet.

### `<ol>` Attributes

- `type`: Numbering style decide karta hai.
  - `1` → Numbers (1, 2, 3...)
  - `A` → Uppercase letters (A, B, C...)
  - `a` → Lowercase letters (a, b, c...)
  - `I` → Uppercase Roman numerals (I, II, III...)
  - `i` → Lowercase Roman numerals (i, ii, iii...)

- `start`: Ordered list kis number ya letter se start hogi.
- `reversed`: List ko reverse order me display karta hai (counting neeche ki taraf hoti hai).

### `<li>` Attributes

- `value` *(Sirf `<ol>` ke liye)*: Kisi specific list item ka number manually set karta hai.

---

## Examples

### Unordered List (`<ul>`)

Ek unordered list jisme bullet points use hue hain.

```html
<ul type="disc">
  <!-- ul: unordered list; type="disc": bullet style set karta hai -->
  <li>Python Workshop at Coding Gita</li>
  <li>Data Science Program at SwamiNarayan University</li>
  <li>JavaScript Bootcamp</li>
</ul>
```

Ye courses ki ek bulleted list display karega.

---

### Ordered List (`<ol>`)

Ek ordered list jisme numbers aur attributes use hue hain.

```html
<ol type="1" start="2">
  <!-- ol: ordered list; type="1": numeric numbering; start="2": numbering 2 se start hogi -->
  <li>Introduction to Programming</li>
  <li>Advanced Python at Coding Gita</li>
  <li>AI Research at SwamiNarayan University</li>
</ol>
```

Ye numbered list **2, 3, 4** se start hogi.

---

### Ordered List with `reversed`

Reverse order me ordered list.

```html
<ol reversed type="A">
  <!-- reversed: reverse counting; type="A": uppercase letters -->
  <li>Final Project Submission</li>
  <li>Midterm Exam at SwamiNarayan University</li>
  <li>Course Orientation</li>
</ol>
```

Ye list uppercase letters me reverse order (**C, B, A**) me display hogi.

---

### Ordered List with `value`

`value` attribute numbering ko manually set karta hai.

```html
<ol type="1">
  <li>Python Basics</li>
  <li value="5">Advanced Python</li>
  <!-- value="5": is item ki numbering manually 5 set hogi -->
  <li>Web Development at Coding Gita</li>
</ol>
```

Ye list me second item **5** hoga aur next item **6** continue karega.

---

### Description List (`<dl>`)

Terms aur unki descriptions dikhane ke liye description list use hoti hai.

```html
<dl>
  <!-- dl: description list -->
  <dt>Coding Gita</dt>
  <!-- dt: term -->
  <dd>Offers practical coding workshops in Python and JavaScript.</dd>
  <!-- dd: description -->

  <dt>SwamiNarayan University</dt>
  <dd>Provides degrees in Computer Science and AI.</dd>
</dl>
```

Ye terms aur unki indented descriptions display karega.

---

### Nested Lists

List ke andar ek aur list banane ko nested list kehte hain.

```html
<ul type="circle">
  <!-- Main unordered list -->

  <li>Coding Gita Courses
    <ol type="a">
      <!-- Nested ordered list -->
      <li>Python Basics</li>
      <li>Advanced JavaScript</li>
    </ol>
  </li>

  <li>SwamiNarayan University Programs
    <ul type="square">
      <!-- Nested unordered list -->
      <li>Data Science</li>
      <li>AI Research</li>
    </ul>
  </li>

</ul>
```

Ye main bullet list ke andar ordered aur unordered sublists display karega.

---

## Summary

HTML Lists ke 3 main types hote hain:

- **`<ul>`** → Unordered list (bullet points).
- **`<ol>`** → Ordered list (numbers, letters, Roman numerals).
- **`<dl>`** → Description list (terms aur descriptions).

### Important Attributes Recap

- `type` → Bullet ya numbering style change karta hai.
- `start` → Ordered list ko kisi specific number se start karta hai.
- `reversed` → Ordered list ko reverse order me display karta hai.
- `value` → Kisi specific list item ki numbering manually set karta hai.

Nested lists ka use hierarchical structure (main topic aur subtopics) dikhane ke liye hota hai.