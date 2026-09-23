# CSS Tables Guide

Yeh guide CSS ki un properties ko cover karti hai jo tables ko style karne ke liye use hoti hain. Isme table borders, size, alignments, styling aur responsive design ke baare mein detail mein bataya gaya hai. Jahan possible ho, wahan teen se zyada examples diye gaye hain, aur core properties se related variations bhi include ki gayi hain.

---

# Table Borders

`border` property ka use table, table headers aur table cells par border lagane ke liye hota hai. `border-collapse` property decide karti hai ki borders merge honge ya alag-alag rahenge, aur `border-spacing` separate borders ke beech ka gap set karti hai.

## CSS Properties

- **`border`**: Border ki width, style aur color specify karta hai (jaise `1px solid black`).
- **`border-collapse`**: Iski values `collapse` (borders merge ho jate hain) ya `separate` (default, borders alag rehte hain) hoti hain.
- **`border-spacing`**: Jab `border-collapse: separate` ho tab adjacent cell borders ke beech ka distance set karta hai.

## Examples

### 1. **Basic Border**

```css
table, th, td {
  border: 1px solid;
}
```

Table, headers aur cells par 1px ki solid border add karta hai.

### 2. **Border with Color**

```css
table, th, td {
  border: 1px solid green;
}
```

Border ka color green set karta hai.

### 3. **Collapsed Borders**

```css
table {
  border-collapse: collapse;
}
table, th, td {
  border: 1px solid black;
}
```

Adjacent borders ko merge karke ek single border bana deta hai.

### 4. **Border Spacing**

```css
table {
  border-collapse: separate;
  border-spacing: 15px;
}
table, th, td {
  border: 1px solid black;
}
```

Cells ke borders ke beech 15px ka gap add karta hai.

### 5. **Outside Table Border Only**

```css
table {
  border: 1px solid black;
}
```

Sirf poori table ke bahar border lagata hai, cells ke andar nahi.

### 6. **Variation: Dotted Border**

```css
table, th, td {
  border: 2px dotted red;
}
```

Red color ki dotted border use karta hai.

### HTML for examples (adapt as needed):

```html
<table>
  <tr>
    <th>Firstname</th>
    <th>Lastname</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>Peter</td>
    <td>Griffin</td>
    <td>$100</td>
  </tr>
</table>
```

---

# Table Size

`width` aur `height` properties ka use table aur cells ki dimensions control karne ke liye hota hai.

## CSS Properties

- **`width`**: Table ya cell ki width set karta hai (`%`, `px` ya `auto`).
- **`height`**: Table ya cell ki height set karta hai (`%`, `px` ya `auto`).

## Examples

### 1. **Full Width (100%)**

```css
table {
  width: 100%;
}
```

Table screen ya parent container ki poori width le lega.

### 2. **Half Width (50%)**

```css
table {
  width: 50%;
}
```

Table parent container ki sirf aadhi width le lega.

### 3. **Fixed Width (500px)**

```css
table {
  width: 500px;
}
```

Table ki width fixed 500 pixels hogi.

### 4. **Auto Width**

```css
table {
  width: auto;
}
```

Browser content ke hisaab se table ki width automatically decide karega.

### 5. **Header Height**

```css
th {
  height: 70px;
}
```

Table headers ki height 70px set karta hai.

### 6. **Variation: Cell Width and Height**

```css
td {
  width: 200px;
  height: 50px;
}
```

Data cells ki width 200px aur height 50px fix karta hai.

### HTML for examples:

```html
<table>
  <tr>
    <th>Firstname</th>
    <th>Lastname</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>Peter</td>
    <td>Griffin</td>
    <td>$100</td>
  </tr>
</table>
```

---

# Table Alignments

`text-align` horizontal alignment ke liye aur `vertical-align` vertical alignment ke liye use hota hai.

## CSS Properties

- **`text-align`**: Horizontal alignment set karta hai (`left`, `center`, `right`).
- **`vertical-align`**: Vertical alignment set karta hai (`top`, `middle`, `bottom`).

## Examples

### 1. **Center Horizontal (for td)**

```css
td {
  text-align: center;
}
```

Table data cell ke text ko center mein align karta hai.

### 2. **Left Horizontal (for th)**

```css
th {
  text-align: left;
}
```

Table header ka text left side align karta hai.

### 3. **Bottom Vertical**

```css
td {
  vertical-align: bottom;
  height: 100px;
}
```

Text ko cell ke bottom mein align karta hai.

### 4. **Right Horizontal Variation**

```css
td {
  text-align: right;
}
```

Table data cell ke text ko right side align karta hai.

### 5. **Top Vertical Variation**

```css
td {
  vertical-align: top;
  height: 100px;
}
```

Text ko cell ke top mein align karta hai.

### 6. **Middle Vertical Variation**

```css
td {
  vertical-align: middle;
  height: 100px;
}
```

Text ko cell ke beech (middle) mein align karta hai.

### HTML for examples:

```html
<table>
  <tr>
    <th>Firstname</th>
    <th>Lastname</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>Peter</td>
    <td>Griffin</td>
    <td>$100</td>
  </tr>
</table>
```

---

# Table Styling

Table ko aur attractive banane ke liye padding, dividers, hover effect aur zebra striping use ki jaati hai.

## CSS Properties

- **`padding`**: Cells ke andar space add karta hai.
- **`border-bottom`**: Horizontal divider line add karta hai.
- **`:hover`**: Mouse table row ke upar lane par highlight effect deta hai.
- **`nth-child()`**: Alternate rows par styling apply karne ke liye use hota hai.
- **`background-color`, `color`**: Background aur text ke colors set karte hain.

## Examples

### 1. **Padding**

```css
th, td {
  padding: 10px;
  text-align: left;
}
```

Cells ke andar 10px ka space add karta hai aur text left align karta hai.

### 2. **Horizontal Dividers**

```css
th, td {
  border-bottom: 1px solid #ddd;
}
```

Har row ke niche light gray horizontal divider line add karta hai.

### 3. **Hoverable Rows**

```css
tr:hover {
  background-color: coral;
}
```

Mouse row ke upar lane par uska background coral color ka ho jata hai.

### 4. **Zebra Striping**

```css
tr:nth-child(even) {
  background-color: #f2f2f2;
}
```

Even rows par light gray background apply karta hai.

### 5. **Header Styling Variation**

```css
th {
  background-color: #04AA6D;
  color: white;
}
```

Header ka background green aur text white ho jata hai.

### 6. **Odd Striping Variation**

```css
tr:nth-child(odd) {
  background-color: #e0e0e0;
}
```

Odd rows par light gray background apply karta hai.

### HTML for examples:

```html
<table>
  <tr>
    <th>Firstname</th>
    <th>Lastname</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>Peter</td>
    <td>Griffin</td>
    <td>$100</td>
  </tr>
</table>
```

---

# Responsive Tables

Responsive tables ke liye ek container `div` use kiya jata hai jisme `overflow-x: auto` property lagayi jaati hai. Isse chhoti screen par table horizontal scroll ho jata hai.

## CSS Properties

- **`overflow-x`**: Horizontal scrolling enable karta hai (`auto`).

## Examples

### 1. **Basic Responsive Scroll**

```css
.tablecontainer {
  overflow-x: auto;
}
```

Horizontal scroll enable karta hai jab table screen se bada ho.

**HTML:**

```html
<div class="tablecontainer">
  <table>
    <!-- Table content with many columns -->
  </table>
</div>
```

---

### 2. **With Table Width Variation**

```css
.tablecontainer {
  overflow-x: auto;
}
table {
  width: 100%;
}
```

Table full width lega aur zarurat padne par horizontal scroll bhi hoga.

---

### 3. **With Min-Width Variation**

```css
.tablecontainer {
  overflow-x: auto;
}
table {
  min-width: 800px;
}
```

Table ki minimum width 800px hogi aur chhoti screen par scroll aayega.

---

### 4. **Combined with Borders**

```css
.tablecontainer {
  overflow-x: auto;
}
table, th, td {
  border: 1px solid black;
  border-collapse: collapse;
}
```

Responsive scrolling ke saath collapsed borders bhi apply karta hai.

---

### 5. **With Padding Variation**

```css
.tablecontainer {
  overflow-x: auto;
}
th, td {
  padding: 10px;
}
```

Responsive table ke cells ke andar 10px padding add karta hai.

---

### 6. **Full Example with Wide Table**

```css
.tablecontainer {
  overflow-x: auto;
}
```

**HTML:**

```html
<div class="tablecontainer">
  <table>
    <tr>
      <th>First Name</th>
      <th>Last Name</th>
      <th>Points</th>
      <th>Points</th>
      <th>Points</th>
      <th>Points</th>
      <th>Points</th>
      <th>Points</th>
      <th>Points</th>
      <th>Points</th>
      <th>Points</th>
      <th>Points</th>
    </tr>
    <tr>
      <td>Jill</td>
      <td>Smith</td>
      <td>50</td>
      <td>50</td>
      <td>50</td>
      <td>50</td>
      <td>50</td>
      <td>50</td>
      <td>50</td>
      <td>50</td>
      <td>50</td>
      <td>50</td>
    </tr>
  </table>
</div>
```

Yeh example ek wide table dikhata hai jisme bahut saare columns hain. Agar screen chhoti ho to `tablecontainer` ki wajah se horizontal scrolling automatically enable ho jaati hai.