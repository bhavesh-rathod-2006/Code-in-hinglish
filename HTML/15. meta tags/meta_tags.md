# Comprehensive Guide to HTML Meta Tags

Ye guide HTML ke **Meta Tags** ko detail me explain karti hai. Meta tags webpage ke **`<head>` section** me likhe jaate hain aur browser, search engine aur social media platforms ko webpage ke baare me information dete hain.

Is guide me common meta tags, Open Graph (OG) tags aur Twitter Card tags ko Hinglish me explain kiya gaya hai.

---

# What are Meta Tags?

Meta tags HTML document ke **`<head>`** section me hote hain. Ye webpage par visible nahi hote, lekin webpage ke baare me important metadata provide karte hain.

Meta tags ki help se:

- Search engines webpage ko better understand karte hain.
- Browser webpage ko properly render karta hai.
- Social media platforms attractive preview generate karte hain.
- SEO aur Accessibility improve hoti hai.

---

# Common Meta Tags with Examples

## 1. Charset Meta Tag

Ye HTML document ki **character encoding** define karta hai.

```html
<meta charset="UTF-8">
```

**Explanation (Hinglish):**

`UTF-8` almost sabhi languages aur special characters support karta hai.

---

## 2. Viewport Meta Tag

Ye mobile devices par webpage ka size aur zoom control karta hai.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

**Explanation (Hinglish):**

Responsive website banane ke liye ye meta tag bahut important hai.

---

## 3. Description Meta Tag

Ye webpage ka short description provide karta hai.

```html
<meta name="description" content="Learn about HTML meta tags, including Open Graph and Twitter Card tags, with examples and detailed explanations.">
```

**Explanation (Hinglish):**

Search engines isi description ko search results me snippet ki tarah dikha sakte hain.

---

## 4. Keywords Meta Tag

Ye webpage se related keywords define karta hai.

```html
<meta name="keywords" content="meta tags, HTML, SEO, Open Graph, Twitter Card">
```

**Explanation (Hinglish):**

Aaj ke modern SEO me iska impact kam hai, lekin educational purpose ke liye use hota hai.

---

## 5. Author Meta Tag

Ye webpage ke author ka naam define karta hai.

```html
<meta name="author" content="John Doe">
```

**Explanation (Hinglish):**

Ye batata hai ki webpage kisne create kiya hai.

---

## 6. Robots Meta Tag

Ye search engine crawlers ko instructions deta hai.

```html
<meta name="robots" content="index, follow">

<!-- Ya indexing rokne ke liye -->
<meta name="robots" content="noindex, nofollow">
```

**Explanation (Hinglish):**

- `index` → Page search results me show ho sakta hai.
- `follow` → Links crawl kiye ja sakte hain.
- `noindex` → Page search results me show nahi hoga.
- `nofollow` → Links follow nahi kiye jayenge.

---

## 7. Refresh Meta Tag

Ye page ko refresh ya redirect karta hai.

```html
<meta http-equiv="refresh" content="5;url=https://example.com">
```

**Explanation (Hinglish):**

5 seconds baad webpage automatically redirect ho jayega.

---

## 8. Application Name Meta Tag

Ye web application ka naam define karta hai.

```html
<meta name="application-name" content="My Web App">
```

**Explanation (Hinglish):**

Browser aur operating system ko application ka naam batata hai.

---

# Open Graph (OG) Meta Tags

## Overview

Open Graph (OG) tags Facebook ne introduce kiye the taaki webpage social media par attractive preview ke saath share ho.

Ye Facebook, LinkedIn, Pinterest aur kai dusre platforms support karte hain.

---

## Why Use OG Tags?

- Social media preview improve hota hai.
- Image, title aur description customize kar sakte ho.
- Click-through rate improve hoti hai.
- Multiple platforms par same preview maintain hota hai.

---

## Common OG Tags with Examples

### 1. `og:title`

Social media par dikhne wala title.

```html
<meta property="og:title" content="Comprehensive Guide to HTML Meta Tags">
```

**Explanation (Hinglish):**

Share karne par ye title preview me dikhega.

---

### 2. `og:description`

Content ka short description.

```html
<meta property="og:description" content="A detailed guide on HTML meta tags, including Open Graph and Twitter Card tags, with examples.">
```

**Explanation (Hinglish):**

Preview ke niche description show hoti hai.

---

### 3. `og:image`

Preview image ka URL.

```html
<meta property="og:image" content="https://example.com/images/meta-tags-guide.jpg">
```

**Explanation (Hinglish):**

Social media preview me ye image display hogi.

---

### 4. `og:url`

Webpage ka original URL.

```html
<meta property="og:url" content="https://example.com/meta-tags-guide">
```

**Explanation (Hinglish):**

Canonical URL define karta hai.

---

### 5. `og:type`

Content kis type ka hai.

```html
<meta property="og:type" content="article">
```

**Explanation (Hinglish):**

Examples:

- `article`
- `website`
- `video`
- `product`

---

### 6. `og:site_name`

Website ka naam.

```html
<meta property="og:site_name" content="Example Blog">
```

**Explanation (Hinglish):**

Preview me website name show hota hai.

---

### 7. `og:locale`

Language aur region define karta hai.

```html
<meta property="og:locale" content="en_US">
```

**Explanation (Hinglish):**

Example:

- `en_US`
- `en_GB`
- `hi_IN`

---

## Best Practices for OG Tags

- Minimum image size **1200×630 px** use karo.
- Har page ke liye unique title aur description rakho.
- `og:url` zarur add karo.
- Facebook Sharing Debugger se preview test karo.

---

# Twitter Card Meta Tags

## Overview

Twitter (X) Card tags webpage ko Twitter par rich preview ke saath display karte hain.

Ye image, video aur summary preview support karte hain.

---

## Why Use Twitter Card Tags?

- Rich preview show hota hai.
- Engagement aur clicks badhte hain.
- Analytics support milta hai.

---

## Common Twitter Card Tags with Examples

### 1. `twitter:card`

Twitter Card ka type define karta hai.

```html
<meta name="twitter:card" content="summary_large_image">
```

**Explanation (Hinglish):**

Ye large image preview create karta hai.

---

### 2. `twitter:title`

Twitter preview ka title.

```html
<meta name="twitter:title" content="Guide to HTML Meta Tags">
```

---

### 3. `twitter:description`

Twitter preview description.

```html
<meta name="twitter:description" content="Explore HTML meta tags with examples, including OG and Twitter Cards.">
```

---

### 4. `twitter:image`

Twitter preview image.

```html
<meta name="twitter:image" content="https://example.com/images/meta-tags-guide.jpg">
```

---

### 5. `twitter:site`

Website ka Twitter handle.

```html
<meta name="twitter:site" content="@ExampleSite">
```

---

### 6. `twitter:creator`

Content creator ka Twitter handle.

```html
<meta name="twitter:creator" content="@JohnDoe">
```

---

# Twitter Card Types

## 1. Summary Card

Small thumbnail ke saath preview.

```html
<meta name="twitter:card" content="summary">
```

---

## 2. Summary Large Image Card

Large image ke saath preview.

```html
<meta name="twitter:card" content="summary_large_image">
```

---

## 3. Player Card

Video ya audio preview embed karta hai.

```html
<meta name="twitter:card" content="player">

<meta name="twitter:player" content="https://example.com/video.mp4">
```

---

## 4. App Card

Mobile application promote karta hai.

```html
<meta name="twitter:card" content="app">

<meta name="twitter:app:name:iphone" content="My App">
```

---

## Best Practices for Twitter Card Tags

- Summary card image: **280×150 px**
- Large image card: **1200×628 px**
- Twitter Card Validator se test karo.
- OG aur Twitter title/description same rakhna better practice hai.

---

# Example of a Complete Meta Tag Setup

```html
<head>

  <!-- Standard Meta Tags -->

  <meta charset="UTF-8">

  <meta name="viewport"
        content="width=device-width, initial-scale=1.0">

  <meta name="description"
        content="A guide to HTML meta tags with examples.">

  <meta name="keywords"
        content="meta tags, HTML, SEO, Open Graph, Twitter Card">

  <meta name="author"
        content="John Doe">

  <meta name="robots"
        content="index, follow">

  <meta name="application-name"
        content="My Web App">

  <!-- Open Graph Tags -->

  <meta property="og:title"
        content="Comprehensive Guide to HTML Meta Tags">

  <meta property="og:description"
        content="A detailed guide on HTML meta tags.">

  <meta property="og:image"
        content="https://example.com/images/meta-tags-guide.jpg">

  <meta property="og:url"
        content="https://example.com/meta-tags-guide">

  <meta property="og:type"
        content="article">

  <meta property="og:site_name"
        content="Example Blog">

  <meta property="og:locale"
        content="en_US">

  <!-- Twitter Card Tags -->

  <meta name="twitter:card"
        content="summary_large_image">

  <meta name="twitter:title"
        content="Guide to HTML Meta Tags">

  <meta name="twitter:description"
        content="Explore HTML meta tags with examples.">

  <meta name="twitter:image"
        content="https://example.com/images/meta-tags-guide.jpg">

  <meta name="twitter:site"
        content="@ExampleSite">

  <meta name="twitter:creator"
        content="@JohnDoe">

</head>
```

**Explanation (Hinglish):**

Ye ek complete SEO + Social Sharing setup hai.

---

# Examples of HTML Meta Tags, Open Graph Tags, and Twitter Card Tags

## Common Meta Tags

### Example 1: Blog Post

```html
<meta charset="UTF-8">

<meta name="viewport"
      content="width=device-width, initial-scale=1.0">

<meta name="description"
      content="Explore the top technology trends shaping 2025.">

<meta name="keywords"
      content="technology, trends, 2025, innovation">

<meta name="author"
      content="Jane Smith">

<meta name="robots"
      content="index, follow">
```

**Explanation (Hinglish):**

Technology blog ke liye meta tags.

---

### Example 2: E-commerce Product Page

```html
<meta charset="UTF-8">

<meta name="viewport"
      content="width=device-width, initial-scale=1.0">

<meta name="description"
      content="Buy the latest smartphone with 5G and 128GB storage.">

<meta name="keywords"
      content="smartphone, 5G, electronics, buy online">

<meta name="author"
      content="TechStore Inc.">

<meta name="robots"
      content="index, nofollow">
```

**Explanation (Hinglish):**

E-commerce product page ke liye.

---

### Example 3: Video Platform Landing Page

```html
<meta charset="UTF-8">

<meta name="viewport"
      content="width=device-width, initial-scale=1.0">

<meta name="description"
      content="Stream movies and TV shows in HD with a subscription.">

<meta name="keywords"
      content="streaming, movies, TV shows, subscription">

<meta name="author"
      content="StreamVibe Team">

<meta name="robots"
      content="index, follow">
```

**Explanation (Hinglish):**

Video streaming website homepage ke liye.

---

# Open Graph (OG) Tags

## Example 1: Blog Post

```html
<meta property="og:title"
      content="Top Technology Trends for 2025">

<meta property="og:description"
      content="Discover the innovations shaping the future of tech in 2025.">

<meta property="og:image"
      content="https://blog.example.com/images/tech-trends-2025.jpg">

<meta property="og:url"
      content="https://blog.example.com/tech-trends-2025">

<meta property="og:type"
      content="article">

<meta property="og:site_name"
      content="Tech Blog">
```

---

## Example 2: E-commerce Product Page

```html
<meta property="og:title"
      content="Latest 5G Smartphone - 128GB">

<meta property="og:description"
      content="Shop the new 5G smartphone with stunning features.">

<meta property="og:image"
      content="https://store.example.com/images/smartphone.jpg">

<meta property="og:url"
      content="https://store.example.com/smartphone-128gb">

<meta property="og:type"
      content="product">

<meta property="og:site_name"
      content="TechStore">
```

---

## Example 3: Video Platform Landing Page

```html
<meta property="og:title"
      content="StreamVibe: Unlimited Movies & TV Shows">

<meta property="og:description"
      content="Watch your favorite movies and shows in HD anytime, anywhere.">

<meta property="og:image"
      content="https://streamvibe.example.com/images/streaming-banner.jpg">

<meta property="og:url"
      content="https://streamvibe.example.com">

<meta property="og:type"
      content="website">

<meta property="og:site_name"
      content="StreamVibe">
```

---

# Twitter Card Tags

## Example 1: Blog Post

```html
<meta name="twitter:card"
      content="summary_large_image">

<meta name="twitter:title"
      content="Top Tech Trends for 2025">

<meta name="twitter:description"
      content="Discover the innovations shaping 2025.">

<meta name="twitter:image"
      content="https://blog.example.com/images/tech-trends-2025.jpg">

<meta name="twitter:site"
      content="@TechBlog">

<meta name="twitter:creator"
      content="@JaneSmith">
```

---

## Example 2: E-commerce Product Page

```html
<meta name="twitter:card"
      content="summary">

<meta name="twitter:title"
      content="New 5G Smartphone - 128GB">

<meta name="twitter:description"
      content="Get the latest smartphone with top features.">

<meta name="twitter:image"
      content="https://store.example.com/images/smartphone-thumb.jpg">

<meta name="twitter:site"
      content="@TechStore">

<meta name="twitter:creator"
      content="@TechStoreInc">
```

---

## Example 3: Video Platform Landing Page

```html
<meta name="twitter:card"
      content="player">

<meta name="twitter:title"
      content="StreamVibe: Watch Movies in HD">

<meta name="twitter:description"
      content="Stream unlimited movies and shows with StreamVibe.">

<meta name="twitter:image"
      content="https://streamvibe.example.com/images/video-thumb.jpg">

<meta name="twitter:site"
      content="@StreamVibe">

<meta name="twitter:player"
      content="https://streamvibe.example.com/video/trailer.mp4">
```

---

# Notes

- **OG Image Size:** Minimum **1200×630 px** use karo.
- **Twitter Summary Image:** **280×150 px** recommended hai.
- **Twitter Large Image:** **1200×628 px** recommended hai.
- Facebook Sharing Debugger aur Twitter Card Validator se tags test karo.
- OG aur Twitter tags me title aur description consistent rakhna better practice hai.

---

# Conclusion

Meta tags webpage ko **SEO friendly**, **mobile friendly** aur **social media friendly** banate hain.

- **Common Meta Tags** → Browser aur Search Engine ke liye metadata provide karte hain.
- **Open Graph Tags** → Facebook, LinkedIn, Pinterest jaise platforms par rich preview banate hain.
- **Twitter Card Tags** → Twitter (X) par attractive image, video aur summary preview show karte hain.

Sahi meta tags use karne se website ki visibility, engagement aur user experience improve hota hai.