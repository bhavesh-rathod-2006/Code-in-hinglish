## Paragraph (`<p>`) Tag & Heading Tags (`<h1>`–`<h6>`)

### 1. Paragraph Tag – `<p>`

**Purpose**  
`<p>` tag ka use **paragraph** ya text ka ek alag block define karne ke liye hota hai. Browser automatically paragraph ke upar aur neeche thodi spacing (margin) add kar deta hai.

**Basic Syntax**
```html
<p>This is a paragraph of text.</p>
```

**Key Points**
- Yeh ek **block-level** element hai (matlab yeh hamesha new line se start hota hai aur available width le leta hai).
- `<p>` tag ke andar **block-level elements** (jaise headings, lists ya doosra `<p>`) nahi rakhne chahiye.
- HTML5 me best practice ke liye closing tag (`</p>`) zaroor use karna chahiye, chahe kuch browsers ise automatically close kar dete hain.

**Common Attributes for `<p>`**

| Attribute | Description | Example |
|-----------|-------------|---------|
| `title` | Mouse hover karne par tooltip text show hota hai. | `<p title="Extra info">...</p>` |
| `lang` | Paragraph ki language specify karta hai. | `<p lang="en">...</p>` |
| `dir` | Text ki direction set karta hai (`ltr` ya `rtl`). | `<p dir="rtl">...</p>` |
| `align` | Text alignment set karta hai (**Deprecated** – CSS use karo). | `<p align="center">...</p>` |

> **Note**: `align` attribute ki jagah CSS properties (`text-align`, `margin`, `padding`, etc.) use karna better practice hai.

---

### 2. Heading Tags – `<h1>` to `<h6>`

**Purpose**  
Heading tags different importance level ke **headings** define karte hain. Yeh webpage ko proper structure dete hain aur SEO (Search Engine Optimization) me bhi help karte hain.

**Hierarchy**

| Tag | Level | Typical Use | Default Size (approx.) |
|------|-------|-------------|------------------------|
| `<h1>` | Sabse important | Main page title | Largest |
| `<h2>` | Second level | Major section heading | Large |
| `<h3>` | Third level | Sub-section heading | Medium-large |
| `<h4>` | Fourth level | Chhoti sub-heading | Medium |
| `<h5>` | Fifth level | Minor heading | Small-medium |
| `<h6>` | Sabse kam important | Least significant heading | Smallest |

**Basic Syntax**
```html
<h1>Main Heading</h1>
<h2>Sub Heading</h2>
<h3>Sub-sub Heading</h3>
<!-- ... up to h6 -->
```

**Key Points**
- Heading tags bhi **block-level** elements hote hain.
- Inhe **logical order** me use karna chahiye (jaise bina reason ke `<h1>` se direct `<h4>` par jump nahi karna chahiye).
- Normally ek webpage me **sirf ek `<h1>`** hona chahiye, jo page ka main title hota hai.
- Search engines higher-level headings (`<h1>`, `<h2>`) ko zyada importance dete hain.

**Common Attributes for Heading Tags (`<h1>`–`<h6>`)**

| Attribute | Description | Example |
|-----------|-------------|---------|
| `title` | Mouse hover karne par tooltip show hota hai. | `<h2 title="Click for more">...</h2>` |
| `lang` | Heading ki language define karta hai. | `<h1 lang="hi">...</h1>` |
| `dir` | Text ki direction set karta hai. | `<h1 dir="rtl">...</h1>` |
| `align` | Text alignment set karta hai (**Deprecated** – CSS use karo). | `<h1 align="center">...</h1>` |

---

### Quick Comparison

| Feature | `<p>` Tag | `<h1>`–`<h6>` Tags |
|---------|-----------|--------------------|
| Purpose | Paragraph ya body text likhne ke liye use hota hai. | Different importance level ke headings banane ke liye use hote hain. |
| SEO Importance | Kam importance hoti hai. | High importance hoti hai, especially `<h1>` aur `<h2>`. |
| Default Spacing | Upar aur neeche normal margin hoti hai. | Zyada margin aur text by default bold hota hai. |
| Can contain | Text aur inline elements rakh sakta hai. | Text aur inline elements rakh sakte hain. |
| Best Practice | Body text ke liye use karo. | Webpage ka proper structure banane ke liye use karo. |

---