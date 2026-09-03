# HTML Links

HTML me links **`<a>` (anchor)** tag ki help se banaye jaate hain. Links users ko ek page se doosre page, website ya same page ke kisi specific section par navigate karne ki facility dete hain. `<a>` tag me kai important attributes hote hain, jisme **`href`**, **`target`**, **`title`**, aur **`download`** sabse zyada use hote hain.

Neeche HTML Links, unke attributes (especially `target`), link types aur bookmarks ki complete explanation di gayi hai.

---

## Basic HTML Links

`<a>` tag ek **hyperlink** create karta hai. Iska sabse important attribute **`href`** hota hai, jo batata hai ki link kis destination par jayega.

### Key Attributes

- **`href`** → Link kis URL ya page par jayega, yeh specify karta hai.
- **`target`** → Link ko kahan open karna hai (same tab, new tab, iframe, etc.).
- **`title`** → Hover karne par tooltip show karta hai.
- **`download`** → Link ko open karne ke bajay file download karwata hai.

### Example of a Basic Link

```html
<a href="https://codinggita.com">Visit Coding Gita</a>
```

Is example me **"Visit Coding Gita"** ek clickable link ban jayega jo Coding Gita website open karega.

---

### Example with `title` and `download`

```html
<a href="brochure.pdf" download title="Download Coding Gita Brochure">
  Download Brochure
</a>
```

Is example me:

- File **`brochure.pdf`** download hogi.
- Hover karne par tooltip **"Download Coding Gita Brochure"** show hoga.

---

## Types of Links: Internal and External

HTML me mainly **2 types ke links** hote hain.

### 1. External Links

External links kisi **doosri website ya domain** par le jaate hain. Yeh generally `http://` ya `https://` se start hote hain.

**Example**

```html
<a href="https://swaminarayanuniversity.ac.in" target="_blank">
  Explore SwamiNarayan University
</a>
```

Yeh user ko ek alag website par le jayega.

**Key Point**

- Doosri website open karta hai.
- Mostly `target="_blank"` use kiya jata hai taaki new tab me open ho.

---

### 2. Internal Links

Internal links **same website** ke kisi doosre page ya resource par le jaate hain.

**Example (Another Page)**

```html
<a href="courses.html" target="_self">
  View Our Courses
</a>
```

Ya

```html
<a href="/courses/python" target="_self">
  Python Course
</a>
```

Yeh same website ke page ko open karega.

---

### Internal Link (Bookmark) on the Same Page

```html
<a href="#workshops" target="_self">
  Go to Workshops Section
</a>
```

Yeh same page ke **Workshops** section tak scroll karega.

---

## The `target` Attribute

`target` attribute decide karta hai ki linked page ya document **kahan open hoga**.

### Possible Values

| Value | Description |
|-------|-------------|
| `_self` | Link same tab/window me open hota hai. (Default) |
| `_blank` | Link new tab ya new window me open hota hai. |
| `_parent` | Link parent frame me open hota hai. |
| `_top` | Link poori window me open hota hai aur frames se bahar aa jata hai. |
| `frame-name` | Link kisi specific iframe ya frame me open hota hai. |

---

## Examples of `target` Attribute

### 1. Using `_self` (Default)

```html
<a href="https://codinggita.com/courses" target="_self">
  View Coding Gita Courses
</a>
```

**Result:** Link current tab me hi open hoga aur current page replace ho jayega.

---

### 2. Using `_blank`

```html
<a href="https://swaminarayanuniversity.ac.in" target="_blank">
  Explore SwamiNarayan University
</a>
```

**Result:** Link new tab me open hoga aur current page open hi rahega.

---

### 3. Using `_parent` (Frameset Example)

```html
<frameset cols="50%,50%">
  <frame src="frame1.html">
  <frame src="frame2.html">

  <a href="https://codinggita.com" target="_parent">
    Go to Coding Gita
  </a>
</frameset>
```

**Result:** Link parent frame me open hoga.

> **Note:** Frameset HTML5 me deprecated hai, lekin exam aur theory ke liye jaana zaroori hai.

---

### 4. Using `_top`

```html
<frameset cols="50%,50%">
  <frame src="frame1.html">
  <frame src="frame2.html">

  <a href="https://swaminarayanuniversity.ac.in" target="_top">
    Go to SwamiNarayan University
  </a>
</frameset>
```

**Result:** Link poori browser window me open hoga aur frames remove ho jayenge.

---

### 5. Using a Custom Frame Name

```html
<iframe name="content-frame" src="about.html"></iframe>

<a href="https://codinggita.com" target="content-frame">
  Load Coding Gita in Frame
</a>
```

**Result:** Coding Gita website **iframe** ke andar load hogi.

---

# Bookmarks (Internal Links)

Bookmarks user ko **same webpage ke kisi specific section** par direct le jaate hain.

### Bookmarks Banane Ke Steps

### Step 1: Target Element Ko `id` Do

```html
<h2 id="workshops">Coding Gita Workshops</h2>
```

### Step 2: `href` Me `#id-name` Likho

```html
<a href="#workshops">Go to Workshops Section</a>
```

Browser automatically us section tak scroll karega.

---

## Example of Bookmarks

```html
<body id="top">

  <h1>Coding Gita and SwamiNarayan University</h1>

  <p>
    Jump to:
    <a href="#workshops" target="_self">Workshops</a> |
    <a href="#programs" target="_self">Programs</a>
  </p>

  <h2 id="workshops">Coding Gita Workshops</h2>
  <p>Practical sessions on Python, JavaScript, and more.</p>

  <h2 id="programs">SwamiNarayan University Programs</h2>
  <p>Degrees in Computer Science, AI, and Data Science.</p>

  <p>
    <a href="#top" target="_self">Back to Top</a>
  </p>

</body>
```

### Is Example Me Kya Hota Hai?

- **Workshops** par click karne se page `id="workshops"` wale section tak scroll karega.
- **Programs** par click karne se `id="programs"` wale section tak scroll karega.
- **Back to Top** par click karne se page `id="top"` wale top section par aa jayega.
- Sab links `target="_self"` use kar rahe hain, isliye same tab me hi navigation hoti hai.

---

## Quick Comparison

| Feature | Internal Link | External Link |
|---------|---------------|---------------|
| Destination | Same website ya same webpage | Doosri website |
| URL Format | `about.html`, `/courses/python`, `#section` | `https://example.com` |
| Internet Required | Nahi (local page bhi ho sakta hai) | Haan (website open karne ke liye) |
| Example | `<a href="about.html">About</a>` | `<a href="https://codinggita.com">Coding Gita</a>` |

---

## Quick Comparison of `target` Values

| `target` Value | Kahan Open Hota Hai? |
|----------------|----------------------|
| `_self` | Same tab me. |
| `_blank` | New tab/window me. |
| `_parent` | Parent frame me. |
| `_top` | Full browser window me. |
| `content-frame` | Specific iframe ya frame me. |

---

## Summary

HTML me links **`<a>` tag** ki help se banaye jaate hain. `href` destination batata hai, `target` decide karta hai ki link kahan open hoga, `title` tooltip show karta hai, aur `download` file download karwata hai.

Links mainly do types ke hote hain:

- **Internal Links** → Same website ya same page ke section par le jaate hain.
- **External Links** → Kisi doosri website par le jaate hain.

Bookmarks `id` attribute aur `href="#id-name"` ki help se same webpage ke specific section par navigation provide karte hain, jisse long webpages me navigation easy ho jata hai.

---