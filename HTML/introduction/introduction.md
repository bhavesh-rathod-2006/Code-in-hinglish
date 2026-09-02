## Introduction to HTML and CSS

### What is HTML?
HTML ek standard markup language hai jo web pages ka content create aur structure karne ke liye use hoti hai. Yeh webpage ki structure define karti hai by using different elements (tags) jaise headings, paragraphs, images, links, lists, tables, aur forms. Browsers HTML code ko read karte hain aur uske according content display karte hain. HTML ek programming language nahi hai; yeh ek markup language hai jo browser ko batati hai *kya* content show karna hai aur woh kaise organize kiya gaya hai.

**Full Form of HTML:**  
**HyperText Markup Language**

- **HyperText**: Aise text ko refer karta hai jisme links (hyperlinks) hoti hain jo dusre documents ya resources se connect karti hain.
- **Markup**: Iska matlab hai ki language special tags (markup) ka use karke content ka structure aur meaning define karti hai.
- **Language**: Yeh code likhne ka ek standardized tareeka hai jise browsers samajhta hain.

### What is CSS?
CSS woh language hai jo web pages ko style aur design karne ke liye use hoti hai. Jahan HTML structure aur content provide karta hai, wahin CSS presentation control karta hai — yani content dikhega kaise. CSS ki help se colors, fonts, sizes, spacing, layout, backgrounds, borders change kiye ja sakte hain aur responsive designs banaye ja sakte hain jo alag-alag screen sizes par sahi kaam karein. CSS design ko content se alag rakhti hai, jiski wajah se websites ko maintain aur update karna easy ho jata hai.

**Full Form of CSS:**  
**Cascading Style Sheets**

- **Cascading**: Iska matlab hai styles ek hierarchy ke according apply hoti hain (general rules se specific rules tak, aur multiple style sheets ek dusre ko override kar sakti hain).
- **Style Sheets**: Rules ka collection jo define karta hai ki HTML elements kaise display honge.

### Relationship Between HTML and CSS
- **HTML** → Webpage ka structure build karta hai (webpage ka skeleton{kankaal}).
- **CSS** → Style aur layout add karta hai (design aur appearance).

HTML aur CSS milkar internet par lagbhag har website ki foundation banate hain.

**Notes on the Structure of HTML**

Har HTML document ek standard basic structure follow karta hai. Yeh structure browser ko batata hai ki file ek HTML document hai aur important information aur visible content kahan likhna hai.

Yeh HTML page ka basic skeleton hai:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Page Title</title>
</head>
<body>
    <!-- All visible content goes here -->
</body>
</html>
```

### Explanation of Each Part

### 1. `<!DOCTYPE html>`
- Isse **Document Type Declaration** kaha jata hai.
- Yeh browser ko batata hai ki yeh document **HTML5** me likha gaya hai.
- Yeh HTML file ki bilkul first line honi chahiye.
- Yeh HTML tag nahi hai; yeh browser ke liye ek instruction hai.

**Example:**
```html
<!DOCTYPE html>
```

---

### 2. `<html>` ... `</html>`
- Yeh pure HTML document ka **root element** hai.
- Baaki sab kuch (head aur body) isi tag ke andar likha jata hai.
- `lang` attribute commonly page ki language specify karne ke liye use hota hai (jaise `lang="en"` English ke liye).

**Example:**
```html
<html lang="en">
    ...
</html>
```

---

### 3. `<head>` ... `</head>`
- **Head** section webpage ke baare me information contain karta hai.
- Yeh information webpage par visible nahi hoti.
- Isme metadata, title, CSS files ke links, scripts, etc. include hote hain.

**Common things written inside `<head>`:**

#### a) `<meta charset="UTF-8">`
- Page ki character encoding define karta hai.
- `UTF-8` almost sabhi languages aur special characters ko support karta hai.

#### b) `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
- Webpage ko responsive banata hai (mobile devices par bhi sahi dikhta hai).
- Browser ko batata hai ki width device screen ke according set kare.

#### c) `<title>` ... `</title>`
- Webpage ka **title** set karta hai.
- Yeh title browser tab me dikhai deta hai aur search engines bhi use karte hain.

**Example of head section:**
```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My First Webpage</title>
</head>
```

---

### 4. `<body>` ... `</body>`
- **Body** section webpage ka sara **visible content** contain karta hai.
- User jo bhi dekhta hai (text, images, links, headings, paragraphs, buttons, etc.) woh sab `<body>` tag ke andar likha jata hai.

**Example:**
```html
<body>
    <h1>Welcome to My Website</h1>
    <p>This is a paragraph of text.</p>
    <img src="photo.jpg" alt="A photo">
</body>
```

---

### Complete Basic Structure (Ready to Use)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Webpage</title>
</head>
<body>
    <h1>Hello World!</h1>
    <p>This is my first HTML page.</p>
</body>
</html>
```

---

### Quick Summary

| Part                  | Purpose                                      | Visible on Page? |
|-----------------------|----------------------------------------------|------------------|
| `<!DOCTYPE html>`     | HTML5 document declare karta hai             | No               |
| `<html>`              | Puri webpage ka root container hai           | No               |
| `<head>`              | Metadata aur page information contain karta hai | No            |
| `<title>`             | Browser tab ka title set karta hai           | No (tab me dikhta hai) |
| `<meta>`              | Extra information provide karta hai (encoding, viewport, etc.) | No |
| `<body>`              | Sara visible content contain karta hai       | Yes              |

Yeh structure har webpage ki foundation hai. Jab bhi nayi HTML file banao, hamesha isi basic skeleton se start karo.

---

## HTML Basic Technical Terms

Yahan HTML me use hone wale basic technical terms ki clear definitions aur proper examples diye gaye hain.

### 1. Tag
**Tag** ek special keyword hota hai jo angle brackets (`< >`) ke andar likha jata hai aur browser ko batata hai ki content ko kaise structure ya display karna hai.

- Tags usually pair(jode) me aate hain: ek **opening tag** aur ek **closing tag**.
- Opening tag: `<` se start hota hai.
- Closing tag: `</` se start hota hai.

**Example:**
```html
<p>This is a paragraph.</p>
```

- `<p>` → Opening tag
- `</p>` → Closing tag

---

### 2. Element
**Element** ek complete structure hota hai jo opening tag, content (agar ho), aur closing tag se milkar banta hai.

**Formula:**  
**Element = Opening Tag + Content + Closing Tag**

**Example:**
```html
<h1>Welcome to HTML</h1>
```

- Pura `<h1>Welcome to HTML</h1>` ek **element** hai.
- `<h1>` aur `</h1>` tags hain.
- `Welcome to HTML` content hai.

---

### 3. Attribute
**Attribute** HTML element ke baare me extra information provide karta hai. Yeh opening tag ke andar name-value pair ke form me likha jata hai.

**Syntax:**  
`attribute_name="value"`

**Example:**
```html
<img src="photo.jpg" alt="A beautiful landscape" width="300">
```

- `src`, `alt`, aur `width` attributes hain.
- `"photo.jpg"`, `"A beautiful landscape"`, aur `"300"` unki values hain.

Common attributes: `id`, `class`, `src`, `href`, `alt`, `style`, `title`, etc.

---

### 4. Closing Tag
**Closing tag** HTML element ka end show karta hai. Yeh tag name se pehle forward slash (`/`) ke saath likha jata hai.

**Example:**
```html
<p>This is a paragraph of text.</p>
```

- `</p>` **closing tag** hai.

Agar closing tag (zyadatar cases me) nahi likhenge, to browser content ko sahi tarah display nahi kar sakta.

---

### 5. Self-Closing Tag (Void Element)
Kuch HTML tags ko closing tag ki zarurat nahi hoti kyunki unke andar koi content nahi hota. Inhe **self-closing tags** ya **void elements** kaha jata hai.

Modern HTML (HTML5) me inhe sirf `<tag>` ya `<tag />` dono tareeke se likh sakte ho (dono valid hain).

**Common Self-Closing Tags:**

| Tag | Purpose | Example |
|------|---------|---------|
| `<br>` | Line break dene ke liye | `Hello<br>World` |
| `<hr>` | Horizontal line dikhane ke liye | `<hr>` |
| `<img>` | Image display karne ke liye | `<img src="pic.jpg" alt="Photo">` |
| `<input>` | Form input field banane ke liye | `<input type="text">` |
| `<meta>` | Metadata define karne ke liye | `<meta charset="UTF-8">` |
| `<link>` | External resource connect karne ke liye | `<link rel="stylesheet" href="style.css">` |

**Example:**
```html
<img src="logo.png" alt="Website Logo">
<br>
<hr>
```

---

### Quick Summary Table

| Term | Definition | Example |
|------|------------|---------|
| **Tag** | Angle brackets `<>` ke andar likha keyword | `<p>`, `</p>` |
| **Element** | Opening tag + content + closing tag | `<p>Hello</p>` |
| **Attribute** | Opening tag ke andar extra information | `src="image.jpg"` |
| **Closing Tag** | Element ko end karta hai (`</tag>`) | `</h1>`, `</div>` |
| **Self-Closing** | Aisa tag jise closing tag ki zarurat nahi hoti | `<br>`, `<img>`, `<hr>` |

Yeh HTML document ke core building blocks hain. Inhe achhi tarah samajhne se tum clean aur correct HTML code likh paoge.