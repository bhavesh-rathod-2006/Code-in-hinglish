# CSS Attribute Selectors: Types and Examples

CSS attribute selectors ka use HTML elements ko unke attributes ki presence ya unki value ke basis par style karne ke liye hota hai. Neeche har type ke attribute selector ki definition di gayi hai, jiske baad uske use ko samjhane ke liye 3 se 4 practical examples diye gaye hain.

## 1. [attribute]

### Definition

Ye un sabhi elements ko select karta hai jinmein specified attribute present hota hai, chahe us attribute ki value kuch bhi ho.

### Examples

#### Example 1: Styling Elements with a `title` Attribute

**HTML**
```html
<p title="info">Paragraph with title</p>
<p>No title</p>
```

**CSS**
```css
[title] {
  color: blue;
}
```

**Result**: Jis paragraph mein `title` attribute hai, uska text blue ho jayega.

#### Example 2: Styling Elements with a `data-type` Attribute

**HTML**
```html
<div data-type="primary">Primary Content</div>
<div>Secondary Content</div>
```

**CSS**
```css
[data-type] {
  font-weight: bold;
}
```

**Result**: Jis `div` mein `data-type` attribute hai, uska text bold ho jayega.

#### Example 3: Styling Images with an `alt` Attribute

**HTML**
```html
<img src="image.jpg" alt="description">
<img src="image2.jpg">
```

**CSS**
```css
[alt] {
  border: 2px solid green;
}
```

**Result**: Jis image mein `alt` attribute hai, uske around green border aa jayega.

## 2. [attribute="value"]

### Definition

Ye un elements ko select karta hai jinke specified attribute ki value bilkul given value se match karti hai.

### Examples

#### Example 1: Styling Text Inputs

**HTML**
```html
<input type="text" placeholder="Text">
<input type="password" placeholder="Password">
```

**CSS**
```css
input[type="text"] {
  background-color: lightyellow;
}
```

**Result**: Sirf text input ka background light yellow ho jayega.

#### Example 2: Styling Links with a Specific `target` Value

**HTML**
```html
<a href="https://example.com" target="_blank">External Link</a>
<a href="page.html">Internal Link</a>
```

**CSS**
```css
a[target="_blank"] {
  color: red;
}
```

**Result**: Jis link ka `target` attribute `_blank` hai, uska text red ho jayega.

#### Example 3: Styling Elements with a Specific `data-category` Value

**HTML**
```html
<div data-category="news">News Item</div>
<div data-category="blog">Blog Post</div>
```

**CSS**
```css
[data-category="news"] {
  border-left: 4px solid blue;
}
```

**Result**: Jis `div` ki `data-category` value `"news"` hai, uske left side par blue border aa jayega.

#### Example 4: Styling Buttons with a Specific `type` Value

**HTML**
```html
<button type="submit">Submit</button>
<button type="button">Cancel</button>
```

**CSS**
```css
button[type="submit"] {
  background-color: green;
  color: white;
}
```

**Result**: Submit button ka background green aur text white ho jayega.

## 3. [attribute~="value"]

### Definition

Ye un elements ko select karta hai jinke attribute ki value mein specified word alag se present hota hai. Ye words space se separate hone chahiye.

### Examples

#### Example 1: Styling Elements with a Specific Class Word

**HTML**
```html
<div class="card highlight primary">Card 1</div>
<div class="card secondary">Card 2</div>
```

**CSS**
```css
[class~="highlight"] {
  background-color: yellow;
}
```

**Result**: Jis `div` ki class list mein `"highlight"` word hai, uska background yellow ho jayega.

#### Example 2: Styling Elements with a Specific `rel` Word

**HTML**
```html
<a href="site.html" rel="nofollow external">Link 1</a>
<a href="page.html" rel="bookmark">Link 2</a>
```

**CSS**
```css
[rel~="nofollow"] {
  text-decoration: underline;
}
```

**Result**: Jis link ke `rel` attribute mein `"nofollow"` word hai, uske text ke neeche underline aa jayegi.

#### Example 3: Styling Elements with a Custom Data Attribute

**HTML**
```html
<span data-tags="urgent important">Task 1</span>
<span data-tags="low">Task 2</span>
```

**CSS**
```css
[data-tags~="urgent"] {
  color: red;
}
```

**Result**: Jis `span` ke `data-tags` attribute mein `"urgent"` word hai, uska text red ho jayega.

## 4. [attribute*="value"]

### Definition

Ye un elements ko select karta hai jinke attribute ki value mein specified text ya substring kahin bhi present hota hai.

### Examples

#### Example 1: Styling Links with a Substring in `href`

**HTML**
```html
<a href="https://example.com">Example Site</a>
<a href="https://test.com">Test Site</a>
```

**CSS**
```css
a[href*="example"] {
  font-weight: bold;
}
```

**Result**: Jis link ke `href` attribute mein `"example"` text hai, uska text bold ho jayega.

#### Example 2: Styling Elements with a Substring in `data-id`

**HTML**
```html
<div data-id="user123">User Profile</div>
<div data-id="admin456">Admin Profile</div>
```

**CSS**
```css
[data-id*="user"] {
  background-color: lightblue;
}
```

**Result**: Jis `div` ke `data-id` attribute mein `"user"` text hai, uska background light blue ho jayega.

#### Example 3: Styling Images with a Substring in `src`

**HTML**
```html
<img src="photos/cat.jpg" alt="Cat">
<img src="images/dog.jpg" alt="Dog">
```

**CSS**
```css
img[src*="photos"] {
  border-radius: 10px;
}
```

**Result**: Jis image ke `src` attribute mein `"photos"` text hai, uske corners rounded ho jayenge.

#### Example 4: Styling Inputs with a Substring in `placeholder`

**HTML**
```html
<input placeholder="Enter your name">
<input placeholder="Type password">
```

**CSS**
```css
input[placeholder*="name"] {
  border: 1px solid purple;
}
```

**Result**: Jis input ke `placeholder` mein `"name"` text hai, uske around purple border aa jayega.

## 5. [attribute^="value"]

### Definition

Ye un elements ko select karta hai jinke attribute ki value specified value se start hoti hai.

### Examples

#### Example 1: Styling Links Starting with "https"

**HTML**
```html
<a href="https://example.com">Secure Site</a>
<a href="http://test.com">Non-Secure Site</a>
```

**CSS**
```css
a[href^="https"] {
  color: green;
}
```

**Result**: Jis link ka `href` `"https"` se start hota hai, uska text green ho jayega.

#### Example 2: Styling Elements with a `data-id` Starting with "prod"

**HTML**
```html
<div data-id="prod123">Product 1</div>
<div data-id="cat456">Category 1</div>
```

**CSS**
```css
[data-id^="prod"] {
  font-style: italic;
}
```

**Result**: Jis `div` ka `data-id` `"prod"` se start hota hai, uska text italic ho jayega.

#### Example 3: Styling Images with `src` Starting with "images"

**HTML**
```html
<img src="images/photo1.jpg" alt="Photo 1">
<img src="media/photo2.jpg" alt="Photo 2">
```

**CSS**
```css
img[src^="images"] {
  border: 3px solid orange;
}
```

**Result**: Jis image ka `src` `"images"` se start hota hai, uske around orange border aa jayega.

## 6. [attribute$="value"]

### Definition

Ye un elements ko select karta hai jinke attribute ki value specified value par end hoti hai.

### Examples

#### Example 1: Styling Images with `src` Ending in ".jpg"

**HTML**
```html
<img src="photo.jpg" alt="Photo">
<img src="image.png" alt="Image">
```

**CSS**
```css
img[src$=".jpg"] {
  opacity: 0.8;
}
```

**Result**: Jis image ka `src` `".jpg"` par end hota hai, uski opacity kam hokar `0.8` ho jayegi.

#### Example 2: Styling Links with `href` Ending in ".pdf"

**HTML**
```html
<a href="document.pdf">Download PDF</a>
<a href="page.html">Go to Page</a>
```

**CSS**
```css
a[href$=".pdf"] {
  text-decoration: none;
  color: purple;
}
```

**Result**: Jis link ka `href` `".pdf"` par end hota hai, usmein underline nahi hogi aur text purple ho jayega.

#### Example 3: Styling Elements with `data-file` Ending in "txt"

**HTML**
```html
<div data-file="notes.txt">Notes</div>
<div data-file="data.csv">Data</div>
```

**CSS**
```css
[data-file$=".txt"] {
  background-color: lightgray;
}
```

**Result**: Jis `div` ka `data-file` `".txt"` par end hota hai, uska background light gray ho jayega.

#### Example 4: Styling Inputs with `name` Ending in "email"

**HTML**
```html
<input name="user_email" type="email">
<input name="username" type="text">
```

**CSS**
```css
input[name$="email"] {
  border-color: teal;
}
```

**Result**: Jis input ka `name` `"email"` par end hota hai, uske border ka color teal ho jayega.

## Browser Support

Sabhi attribute selectors modern browsers mein supported hain, jinmein Chrome, Firefox, Safari aur Edge shamil hain.