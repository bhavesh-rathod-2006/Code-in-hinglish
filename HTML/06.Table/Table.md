# HTML Table

HTML me **tables** `<table>` tag ki help se banayi jaati hain. Table ka use data ko **rows** aur **columns** ke format me organize karne ke liye hota hai. Tables ka use schedules, marksheets, comparison tables, timetables, reports aur results dikhane ke liye bahut common hai.

---

## Table Elements

- **`<table>`** → Complete table define karta hai.
- **`<tr>`** → Table ki ek row define karta hai.
- **`<th>`** → Table header cell define karta hai (default me bold aur center aligned hota hai).
- **`<td>`** → Table data cell define karta hai.
- **`<caption>`** → Table ka title/caption define karta hai (normally table ke upar show hota hai).
- **`<thead>`** → Table ke header section ko group karta hai (semantic element).
- **`<tbody>`** → Table ke body/content section ko group karta hai (semantic element).
- **`<tfoot>`** → Table ke footer section ko group karta hai (semantic element).

---

## Table Attributes

- **`border`** (on `<table>`) → Table ki border width pixels me set karta hai. Yeh old attribute hai, lekin browsers me abhi bhi work karta hai.
- **`colspan`** → Ek cell kitne columns tak span (merge) karega.
- **`rowspan`** → Ek cell kitni rows tak span (merge) karega.
- **`scope`** (on `<th>`) → Batata hai ki header kis row ya column ke liye hai (`row`, `col`, `rowgroup`, `colgroup`).
- **`headers`** → `<td>` ko ek ya multiple `<th>` se unke `id` ke through connect karta hai (accessibility ke liye useful).
- **`align` / `valign` / `width`** → Old attributes hain (Modern HTML me CSS use karna better hai).

---

### Basic Table (border attribute)

```html
<table border="1">
  <tr>
    <th>Course</th>
    <th>Duration</th>
  </tr>
  <tr>
    <td>Python at Coding Gita</td>
    <td>3 months</td>
  </tr>
  <tr>
    <td>Data Science at SwamiNarayan University</td>
    <td>6 months</td>
  </tr>
</table>
```

**Explanation:** Yeh ek simple table hai jisme `border="1"` use karke border dikhayi gayi hai.

---

### Table with Caption

```html
<table border="1">
  <caption>Coding Gita Workshop Schedule</caption>

  <tr>
    <th>Workshop</th>
    <th>Date</th>
  </tr>

  <tr>
    <td>JavaScript Basics</td>
    <td>October 2025</td>
  </tr>
</table>
```

**Explanation:** `caption` table ka heading/title hota hai jo table ke upar show hota hai.

---

### Table with Colspan and Rowspan

```html
<table border="1">
  <tr>
    <th colspan="2">SwamiNarayan University Programs</th>
  </tr>

  <tr>
    <td rowspan="2">AI Research</td>
    <td>Semester 1</td>
  </tr>

  <tr>
    <td>Semester 2</td>
  </tr>
</table>
```

**Explanation**

- `colspan="2"` → Header do columns ko merge karta hai.
- `rowspan="2"` → AI Research wali cell do rows tak merge hoti hai.

---

### Table with Scope and Headers (Accessibility)

```html
<table border="1">
  <tr>
    <th id="course" scope="col">Course</th>
    <th id="instructor" scope="col">Instructor</th>
  </tr>

  <tr>
    <td headers="course">Python at Coding Gita</td>
    <td headers="instructor">Dr. Patel</td>
  </tr>
</table>
```

**Explanation**

- `scope="col"` batata hai ki yeh column header hai.
- `headers` attribute data cell ko correct header se connect karta hai.

---

### Table using `<thead>`, `<tbody>`, `<tfoot>`

```html
<table border="1">
  <caption>SwamiNarayan University Results</caption>

  <thead>
    <tr>
      <th scope="col">Student</th>
      <th scope="col">Grade</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>Amit Sharma</td>
      <td>A</td>
    </tr>

    <tr>
      <td>Priya Desai</td>
      <td>B+</td>
    </tr>
  </tbody>

  <tfoot>
    <tr>
      <td colspan="2">Average Grade: B</td>
    </tr>
  </tfoot>
</table>
```

**Explanation**

- `<thead>` → Header section.
- `<tbody>` → Main data section.
- `<tfoot>` → Footer section.

---

## More Examples of `<thead>`, `<tbody>`, `<tfoot>`

### Example 1 – Student Marks with Totals

```html
<table border="1">
  <caption>Coding Gita – Midterm Marks</caption>

  <thead>
    <tr>
      <th>Student</th>
      <th>Python</th>
      <th>HTML</th>
      <th>Total</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>Rahul</td>
      <td>85</td>
      <td>90</td>
      <td>175</td>
    </tr>

    <tr>
      <td>Sneha</td>
      <td>78</td>
      <td>88</td>
      <td>166</td>
    </tr>
  </tbody>

  <tfoot>
    <tr>
      <td colspan="3">Class Average</td>
      <td>170.5</td>
    </tr>
  </tfoot>
</table>
```

**Explanation:** `tfoot` me class ka average total show kiya gaya hai.

---

### Example 2 – Department-wise Summary

```html
<table border="1">
  <thead>
    <tr>
      <th>Department</th>
      <th>Students</th>
      <th>Pass %</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>Computer Science</td>
      <td>120</td>
      <td>92%</td>
    </tr>

    <tr>
      <td>Data Science</td>
      <td>80</td>
      <td>88%</td>
    </tr>
  </tbody>

  <tfoot>
    <tr>
      <td>Overall</td>
      <td>200</td>
      <td>90%</td>
    </tr>
  </tfoot>
</table>
```

**Explanation:** Footer me overall department summary di gayi hai.

---

## Using `<th>` for Row Headers (`scope="row"`)

Jab kisi row ka first cell poori row ka heading ho, tab `<th scope="row">` use karna chahiye.

```html
<table border="1">
  <caption>Course Details – Coding Gita & SwamiNarayan University</caption>

  <thead>
    <tr>
      <th scope="col">Detail</th>
      <th scope="col">Coding Gita</th>
      <th scope="col">SwamiNarayan University</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <th scope="row">Duration</th>
      <td>3 months</td>
      <td>6 months</td>
    </tr>

    <tr>
      <th scope="row">Mode</th>
      <td>Online + Offline</td>
      <td>Full-time Campus</td>
    </tr>

    <tr>
      <th scope="row">Focus</th>
      <td>Practical Coding</td>
      <td>Research + Industry</td>
    </tr>
  </tbody>
</table>
```

**Explanation:** `Duration`, `Mode`, aur `Focus` poori row ke headers hain.

---

### Another Simple Row Header Example

```html
<table border="1">
  <tr>
    <th scope="row">Course Name</th>
    <td>Full Stack Development</td>
  </tr>

  <tr>
    <th scope="row">Institute</th>
    <td>Coding Gita</td>
  </tr>

  <tr>
    <th scope="row">Fees</th>
    <td>₹25,000</td>
  </tr>
</table>
```

**Explanation:** Har row ka first cell us row ka heading hai.

---

# Notes: `scope` and `headers` Attributes in HTML Tables

## 1. What is the `scope` Attribute?

`scope` attribute sirf **header cells (`<th>`)** par use hota hai.

Yeh browser ko batata hai ki header kis row ya column ko represent karta hai.

### Common Values

| Value | Meaning |
|-------|---------|
| `scope="col"` | Header poore column ke liye hai. |
| `scope="row"` | Header poori row ke liye hai. |

---

### Simple Example of `scope`

```html
<table border="1">
  <tr>
    <th scope="col">Name</th>
    <th scope="col">Age</th>
    <th scope="col">City</th>
  </tr>

  <tr>
    <th scope="row">Rahul</th>
    <td>25</td>
    <td>Delhi</td>
  </tr>

  <tr>
    <th scope="row">Priya</th>
    <td>22</td>
    <td>Mumbai</td>
  </tr>
</table>
```

**Explanation**

- Name, Age aur City → Column headers.
- Rahul aur Priya → Row headers.

---

## 2. What is the `headers` Attribute?

`headers` attribute sirf **data cells (`<td>`)** me use hota hai.

Yeh data cell ko ek ya multiple headers ke `id` ke saath connect karta hai.

### Syntax

```html
<td headers="id1 id2">value</td>
```

Yeh attribute especially **complex tables** me useful hota hai.

---

### Simple Example of `headers` Attribute

```html
<table border="1">
  <tr>
    <th id="name">Name</th>
    <th id="age">Age</th>
    <th id="city">City</th>
  </tr>

  <tr>
    <td headers="name">Rahul</td>
    <td headers="age">25</td>
    <td headers="city">Delhi</td>
  </tr>

  <tr>
    <td headers="name">Priya</td>
    <td headers="age">22</td>
    <td headers="city">Mumbai</td>
  </tr>
</table>
```

**Explanation**

- Har `<th>` ka ek unique `id` hai.
- Har `<td>` apne related header ko `headers` attribute se refer karta hai.

---

## 3. Example Using Both `scope` and `headers`

```html
<table border="1">
  <tr>
    <th id="name" scope="col">Name</th>
    <th id="age" scope="col">Age</th>
    <th id="city" scope="col">City</th>
  </tr>

  <tr>
    <th id="rahul" scope="row">Rahul</th>
    <td headers="age rahul">25</td>
    <td headers="city rahul">Delhi</td>
  </tr>

  <tr>
    <th id="priya" scope="row">Priya</th>
    <td headers="age priya">22</td>
    <td headers="city priya">Mumbai</td>
  </tr>
</table>
```

**Explanation**

- `scope` row aur column headers define karta hai.
- `headers` data cell ko multiple headers se connect karta hai.

---

## 4. Why Do We Use `scope` and `headers`?

| Reason | Simple Explanation |
|--------|--------------------|
| **Accessibility** | Screen readers data ko uske correct heading ke saath read karte hain (Example: "Age: 25"). |
| **Clarity** | Header aur data ke beech relationship clear hota hai. |
| **Complex Tables** | Ek data cell multiple headers se connect ho sakta hai. |
| **Better Understanding** | Humans aur assistive technologies dono ko table samajhne me help milti hai. |

---

## 5. What Happens If We Don’t Use Them?

| Situation | Result |
|-----------|--------|
| No `scope` aur no `headers` | Screen readers cells ko sirf sequence me read karte hain, context clear nahi hota. |
| Sirf `<th>` without `scope` | Simple tables me kaam karta hai, complex tables me confusion ho sakta hai. |
| Complex table me `headers` missing | Data aur headers ka relation properly identify nahi hota. |

### Example of Bad Practice

```html
<table border="1">
  <tr>
    <td>Name</td>
    <td>Age</td>
  </tr>

  <tr>
    <td>Rahul</td>
    <td>25</td>
  </tr>
</table>
```

**Screen Reader Output**

> "Name, Age, Rahul, 25"

Yeh clearly nahi batata ki Rahul ki age **25** hai.

---

## 6. Quick Summary

| Attribute | Used On | Purpose |
|-----------|---------|---------|
| `scope` | `<th>` | Batata hai header kis row ya column ka hai. |
| `headers` | `<td>` | Data cell ko ek ya multiple headers se `id` ke through connect karta hai. |
| Why Use? | Accessibility + Clarity | Screen readers aur users dono ke liye table samajhna easy hota hai. |
| If Not Used | Accessibility Issue | Table ka semantic meaning kam ho jata hai. |

---

## Best Practice

- Simple tables me **`scope="col"`** aur **`scope="row"`** zaroor use karo.
- Complex tables me `headers` attribute use karo jab ek cell multiple headers se related ho.
- Large tables ke liye `<thead>`, `<tbody>`, aur `<tfoot>` use karna best practice hai.

---

## Summary

- Tables **`<table>`**, **`<tr>`**, **`<th>`**, **`<td>`**, **`<caption>`**, **`<thead>`**, **`<tbody>`**, aur **`<tfoot>`** se banayi jaati hain.
- **`border`** attribute border dikhane ke liye use hota hai (old method, CSS preferred hai).
- **`colspan`** aur **`rowspan`** cells ko merge karne ke liye use hote hain.
- **`scope="col"`** column headers ke liye aur **`scope="row"`** row headers ke liye use karo.
- Accessibility aur semantic HTML ke liye **`scope`**, **`headers`**, aur **`thead` / `tbody` / `tfoot`** use karna best practice hai.

---