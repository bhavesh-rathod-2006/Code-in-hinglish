# HTML Semantic Elements

HTML Semantic Elements webpage ke structure ko **meaning (semantic meaning)** dete hain. Inse browser, search engines aur developers ko samajhna easy ho jata hai ki page ka kaunsa part header hai, footer hai, article hai ya navigation hai.

HTML5 me introduce hue semantic elements **Accessibility**, **SEO** aur **Code Readability** improve karte hain.

---

## 1. The `<article>` Element

`<article>` element ka use **independent aur self-contained content** ke liye hota hai. Aisa content jo apne aap me complete ho aur alag se bhi use ya share kiya ja sake.

Examples: Blog post, News article, Product review, Forum post.

### Example 1: Blog Post

```html
<article>
  <h2>The Benefits of Semantic HTML</h2>
  <p>Semantic HTML improves accessibility and SEO by providing structure to content.</p>
</article>
```

**Explanation (Hinglish):**

Ye ek standalone blog post create karta hai jisme heading aur paragraph dono article ke andar hain.

---

### Example 2: Product Review

```html
<article>
  <h3>Review: Wireless Headphones</h3>
  <p>These headphones offer excellent sound quality and long battery life.</p>
  <p>Rating: 4.5/5</p>
</article>
```

**Explanation (Hinglish):**

Ye ek independent product review hai jo alag se bhi publish ki ja sakti hai.

---

### Example 3: Forum Comment

```html
<article>
  <h4>User Comment on Topic</h4>
  <p>I agree with the points made in the original post.</p>
  <footer>Posted by User123</footer>
</article>
```

**Explanation (Hinglish):**

Ye forum comment ko ek independent content ki tarah show karta hai.

---

## 2. The `<aside>` Element

`<aside>` element ka use **main content se indirectly related content** ke liye hota hai.

Examples: Sidebar, Related Links, Advertisements, Quotes.

### Example 1: Sidebar Information

```html
<aside>
  <h4>About the Author</h4>
  <p>John Doe is a web developer with 10 years of experience.</p>
</aside>
```

**Explanation (Hinglish):**

Ye author ki information sidebar me display karta hai.

---

### Example 2: Related Links

```html
<aside>
  <h4>Related Articles</h4>
  <ul>
    <li><a href="#">HTML Basics</a></li>
    <li><a href="#">CSS Tips</a></li>
  </ul>
</aside>
```

**Explanation (Hinglish):**

Ye main article se related links sidebar me show karta hai.

---

### Example 3: Pull Quote

```html
<aside>
  <blockquote>"Semantic elements make code more meaningful."</blockquote>
</aside>
```

**Explanation (Hinglish):**

Ye main article ki important quote ko alag highlight karta hai.

---

## 3. The `<details>` Element

`<details>` element ka use **expand/collapse content** ke liye hota hai.

User click karke content ko show ya hide kar sakta hai.

### Example 1: FAQ Entry

```html
<details>
  <summary>What is HTML?</summary>
  <p>HTML is the standard markup language for creating web pages.</p>
</details>
```

**Explanation (Hinglish):**

Ye FAQ question create karta hai jo click karne par answer show karta hai.

---

### Example 2: Technical Specs

```html
<details>
  <summary>View Specifications</summary>
  <ul>
    <li>Processor: Intel i7</li>
    <li>RAM: 16GB</li>
  </ul>
</details>
```

**Explanation (Hinglish):**

Click karne par product specifications open ya close hongi.

---

### Example 3: Spoiler Alert

```html
<details>
  <summary>Spoiler for Movie</summary>
  <p>The hero saves the day in the end.</p>
</details>
```

**Explanation (Hinglish):**

Movie spoiler tab tak hidden rahega jab tak user click nahi karega.

---

## 4. The `<figcaption>` Element

`<figcaption>` element ka use `<figure>` ke andar caption ya description dene ke liye hota hai.

### Example 1: Image Caption

```html
<figure>
  <img src="image.jpg" alt="Mountain">
  <figcaption>Mountain Landscape</figcaption>
</figure>
```

**Explanation (Hinglish):**

Ye image ke niche caption display karta hai.

---

### Example 2: Diagram Label

```html
<figure>
  <img src="diagram.png" alt="Flowchart">
  <figcaption>Fig. 1: Process Flowchart</figcaption>
</figure>
```

**Explanation (Hinglish):**

Ye diagram ko figure number aur title deta hai.

---

### Example 3: Code Snippet Description

```html
<figure>
  <code>console.log("Hello");</code>
  <figcaption>Example JavaScript Output</figcaption>
</figure>
```

**Explanation (Hinglish):**

Ye code snippet ke niche uska description show karta hai.

---

## 5. The `<figure>` Element

`<figure>` element ka use **self-contained content** ke liye hota hai.

Examples: Images, Diagrams, Charts, Videos, Code.

### Example 1: Illustration

```html
<figure>
  <img src="illustration.svg" alt="Drawing">
</figure>
```

**Explanation (Hinglish):**

Ye illustration ko standalone content ki tarah show karta hai.

---

### Example 2: Photo with Effects

```html
<figure>
  <img src="photo.jpg" alt="Cityscape" style="filter: grayscale(100%);">
</figure>
```

**Explanation (Hinglish):**

Ye photo par grayscale effect apply karta hai.

---

### Example 3: Embedded Video

```html
<figure>
  <video src="video.mp4" controls></video>
</figure>
```

**Explanation (Hinglish):**

Ye video ko standalone media content ki tarah display karta hai.

---

## 6. The `<footer>` Element

`<footer>` element webpage ya section ka footer define karta hai.

Examples: Copyright, Contact Info, Social Links.

### Example 1: Page Footer

```html
<footer>
  <p>Copyright © 2023 Example.com</p>
</footer>
```

**Explanation (Hinglish):**

Ye page ke bottom me copyright information show karta hai.

---

### Example 2: Article Footer

```html
<article>
  <p>Article content...</p>

  <footer>
    <p>Author: Jane Smith</p>
  </footer>
</article>
```

**Explanation (Hinglish):**

Ye article ke footer me author information show karta hai.

---

### Example 3: Contact Links

```html
<footer>
  <p>Contact us:
    <a href="mailto:info@example.com">info@example.com</a>
  </p>

  <p>Follow us on social media.</p>
</footer>
```

**Explanation (Hinglish):**

Ye contact email aur social media information footer me show karta hai.

---

## 7. The `<header>` Element

`<header>` element webpage ya section ka introductory part define karta hai.

Examples: Logo, Heading, Navigation, Intro.

### Example 1: Page Header

```html
<header>
  <h1>Website Title</h1>
  <p>Welcome to our site.</p>
</header>
```

**Explanation (Hinglish):**

Ye website ka main header create karta hai.

---

### Example 2: Section Header

```html
<section>

  <header>
    <h2>Chapter 1</h2>
  </header>

  <p>Chapter content...</p>

</section>
```

**Explanation (Hinglish):**

Ye section ke andar chapter heading define karta hai.

---

### Example 3: Logo Inclusion

```html
<header>
  <img src="logo.png" alt="Company Logo">

  <nav>
    Navigation links...
  </nav>

</header>
```

**Explanation (Hinglish):**

Ye company logo aur navigation links ko header me display karta hai.

---

## 8. The `<main>` Element

`<main>` element webpage ka **main content area** define karta hai.

> Ek webpage me sirf **ek `<main>` element** hona chahiye.

### Example 1: Basic Main Content

```html
<main>
  <h1>Main Heading</h1>
  <p>This is the primary content area.</p>
</main>
```

**Explanation (Hinglish):**

Ye page ka primary content area define karta hai.

---

### Example 2: Article Collection

```html
<main>

  <article>Article 1...</article>

  <article>Article 2...</article>

</main>
```

**Explanation (Hinglish):**

Ye multiple articles ko main content ke andar group karta hai.

---

### Example 3: Form Content

```html
<main>

  <form>
    <label>Name:
      <input type="text">
    </label>
  </form>

</main>
```

**Explanation (Hinglish):**

Ye form ko webpage ka main content banata hai.

---

## 9. The `<mark>` Element

`<mark>` element text ko **highlight** karne ke liye use hota hai.

### Example 1: Highlighted Search Term

```html
<p>Search results for <mark>HTML</mark>: Learn about semantic elements.</p>
```

**Explanation (Hinglish):**

Ye search keyword HTML ko highlight karta hai.

---

### Example 2: Important Phrase

```html
<p>The key point is <mark>accessibility matters</mark> in web design.</p>
```

**Explanation (Hinglish):**

Ye important phrase ko yellow highlight deta hai.

---

### Example 3: Code Highlight

```html
<p>In the code, <mark>return true;</mark> indicates success.</p>
```

**Explanation (Hinglish):**

Ye code ke important part ko highlight karta hai.

---

## 10. The `<nav>` Element

`<nav>` element navigation links ka group define karta hai.

### Example 1: Main Menu

```html
<nav>

  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">About</a></li>
  </ul>

</nav>
```

**Explanation (Hinglish):**

Ye website ka main navigation menu create karta hai.

---

### Example 2: Footer Navigation

```html
<footer>

  <nav>
    <a href="#">Privacy Policy</a> |
    <a href="#">Terms</a>
  </nav>

</footer>
```

**Explanation (Hinglish):**

Ye footer ke andar navigation links add karta hai.

---

### Example 3: Sidebar Navigation

```html
<aside>

  <nav>
    <ul>
      <li><a href="#">Category 1</a></li>
      <li><a href="#">Category 2</a></li>
    </ul>
  </nav>

</aside>
```

**Explanation (Hinglish):**

Ye sidebar me categories ki navigation create karta hai.

---

## 11. The `<section>` Element

`<section>` element webpage ke **related content ko group** karta hai.

Har section ka apna heading hona recommended hai.

### Example 1: Chapter Division

```html
<section>
  <h2>Introduction</h2>
  <p>This is the intro section.</p>
</section>
```

**Explanation (Hinglish):**

Ye introduction section ko define karta hai.

---

### Example 2: News Items

```html
<section>
  <h3>News Item 1</h3>
  <p>Details...</p>
</section>
```

**Explanation (Hinglish):**

Ye ek news item ko alag thematic section me rakhta hai.

---

### Example 3: Product Features

```html
<section>
  <h2>Features</h2>

  <ul>
    <li>Feature 1</li>
    <li>Feature 2</li>
  </ul>

</section>
```

**Explanation (Hinglish):**

Ye product features ko ek section ke andar organize karta hai.

---

## 12. The `<summary>` Element

`<summary>` element `<details>` ka visible heading hota hai.

User isi heading par click karke details open ya close karta hai.

### Example 1: Accordion Heading

```html
<details>
  <summary>Click for More Info</summary>
  <p>Additional information here.</p>
</details>
```

**Explanation (Hinglish):**

Ye accordion style expandable heading create karta hai.

---

### Example 2: Glossary Term

```html
<details>
  <summary>HTML</summary>
  <p>HyperText Markup Language</p>
</details>
```

**Explanation (Hinglish):**

Ye HTML term ka expandable meaning show karta hai.

---

### Example 3: Warning Toggle

```html
<details>

  <summary>View Warnings</summary>

  <ul>
    <li>Warning 1</li>
    <li>Warning 2</li>
  </ul>

</details>
```

**Explanation (Hinglish):**

Warnings click karne par hi visible hongi.

---

## 13. The `<time>` Element

`<time>` element kisi **date, time ya duration** ko define karta hai.

Machine-readable format ke liye `datetime` attribute use hota hai.

### Example 1: Event Date

```html
<p>
  The event is on
  <time datetime="2023-10-01">October 1, 2023</time>.
</p>
```

**Explanation (Hinglish):**

Ye event ki date semantic format me define karta hai.

---

### Example 2: Timestamp

```html
<p>
  Published:
  <time datetime="2023-09-15T14:30">
    September 15, 2023 at 2:30 PM
  </time>
</p>
```

**Explanation (Hinglish):**

Ye publish date aur time dono show karta hai.

---

### Example 3: Duration

```html
<p>
  The meeting lasts
  <time datetime="PT1H30M">
    1 hour and 30 minutes
  </time>.
</p>
```

**Explanation (Hinglish):**

Ye meeting ki duration semantic format me define karta hai.

---

# Styling Semantic Elements

Semantic elements ko CSS ki help se attractive aur readable banaya ja sakta hai.

## Example: Styled `<article>`

```html
<style>
  article {
    border: 1px solid #ccc;
    padding: 10px;
    margin: 10px;
  }
</style>

<article>
  <h2>Styled Article</h2>
  <p>Content here.</p>
</article>
```

**Explanation (Hinglish):**

Ye article ke around border, padding aur margin add karta hai.

---

## Example: Styled `<aside>`

```html
<style>
  aside {
    float: right;
    width: 30%;
    background-color: #f4f4f4;
    padding: 10px;
  }
</style>

<aside>
  <h4>Sidebar</h4>
  <p>Related info.</p>
</aside>
```

**Explanation (Hinglish):**

Ye aside ko right side me sidebar ki tarah display karta hai.

---

## Best Practices

- Generic `<div>` aur `<span>` ki jagah semantic elements use karo jab possible ho.
- `<article>` ka content independent aur reusable hona chahiye.
- Har `<section>` ke andar heading use karna best practice hai.
- Ek webpage me sirf **ek `<main>`** use karo.
- `<time>` ke saath `datetime` attribute zarur use karo taaki machine-readable date mile.
- Semantic elements accessibility aur SEO dono improve karte hain.

---

## Summary

HTML Semantic Elements webpage ko meaningful structure dete hain.

| **Element** | **Use (Hinglish)** |
|-------------|---------------------|
| `<article>` | Independent content jaise blog, news, review ya forum post. |
| `<aside>` | Sidebar, related links, advertisements ya extra information. |
| `<details>` | Expand/Collapse content ya FAQ section. |
| `<summary>` | `<details>` ka clickable heading. |
| `<figure>` | Self-contained content jaise image, video, chart ya code. |
| `<figcaption>` | Figure ka caption ya description. |
| `<header>` | Page ya section ka introductory content. |
| `<footer>` | Footer content jaise copyright aur contact info. |
| `<main>` | Page ka primary content area. |
| `<mark>` | Important text ya search result highlight karna. |
| `<nav>` | Navigation menu ya important links ka group. |
| `<section>` | Related content ko thematic section me organize karna. |
| `<time>` | Date, time ya duration ko semantic format me define karna. |

Semantic HTML use karne se code zyada readable, SEO-friendly aur accessibility-friendly ban jata hai.