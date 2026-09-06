# What is a Favicon?

**Favicon** ek chhota icon hota hai jo browser tab me website ke title ke side me dikhai deta hai.

**Example:**  
Jab aap Google open karte ho, tab browser tab me colorful **"G"** icon dikhai deta hai. Wahi Google ka favicon hai.

---

## Why Should You Add a Favicon?

Favicon add karne ke kuch important benefits:

- Website ko professional look deta hai.
- Users aapki website ko easily identify kar sakte hain.
- Browser bookmarks me bhi website achhi dikhai deti hai.

---

## How to Add a Favicon

### Step 1: Create or Get a Favicon Image

Sabse pehle ek **square image** chahiye.

**Recommended Size (Beginners):**

- `32 × 32 px`
- `16 × 16 px`

Aap favicon image:

- Canva ya Paint me bana sakte ho.
- `favicon.io` jaise websites se free download kar sakte ho.
- Kisi logo ko online favicon generator se convert kar sakte ho.

Image ko save karo:

- `favicon.ico` (Most Common)
- ya `favicon.png`

---

### Step 2: Put the File in Your Website Folder

Favicon file ko apni HTML file ke **same folder** (root/main folder) me rakho.

**Example Folder Structure**

```text
MyWebsite/
│── index.html
│── favicon.ico
│── favicon.png
│── style.css
```

**Explanation (Hinglish):**

`index.html` aur `favicon.ico` same folder me hone chahiye.

---

### Step 3: Add This Code in Your HTML

Ye line **`<head>`** section ke andar add karo.

```html
<link rel="icon" href="favicon.ico" type="image/x-icon">
```

**Explanation (Hinglish):**

Browser ko batata hai ki website ka favicon `favicon.ico` file hai.

---

## Full Example

```html
<!DOCTYPE html>
<html>
<head>

    <title>My First Website</title>

    <!-- Favicon -->
    <link rel="icon" href="favicon.ico" type="image/x-icon">

</head>

<body>

    <h1>Hello World!</h1>

</body>
</html>
```

**Explanation (Hinglish):**

Is HTML page me browser tab par `favicon.ico` icon show hoga.

---

## Other Common Ways

### Using PNG File

Agar favicon PNG format me ho.

```html
<link rel="icon" href="favicon.png" type="image/png">
```

**Explanation (Hinglish):**

PNG favicon ko browser load karega.

---

### Using SVG File (Modern & Sharp)

Agar favicon SVG format me ho.

```html
<link rel="icon" href="favicon.svg" type="image/svg+xml">
```

**Explanation (Hinglish):**

SVG favicon high quality aur sharp icon provide karta hai.

---

## Best Simple Setup

Agar `.ico` aur `.png` dono use karna ho.

```html
<head>

    <title>My Website</title>

    <link rel="icon" href="favicon.ico">

    <link rel="icon" href="favicon.png" type="image/png">

</head>
```

**Explanation (Hinglish):**

Browser supported format ko automatically choose karega.

---

# Quick Tips

| **Tip** | **Why (Hinglish)** |
|---------|---------------------|
| Keep the image simple. | Chhote icon me zyada details clear nahi dikhti. |
| Make it square. | Favicons hamesha square shape me hone chahiye. |
| Use `.ico` or `.png`. | Ye formats sabse zyada browser support dete hain. |
| Name it `favicon.ico`. | Kai browsers automatically is file ko detect kar lete hain. |
| Clear browser cache after changing favicon. | `Ctrl + Shift + R` dabakar naya favicon refresh karo. |

---

# Common Mistakes

- Favicon code ko `<head>` ke bahar likhna.
- File path ya file name galat likhna.
- Bahut large ya complicated image use karna.
- Browser cache clear ya refresh na karna.

---

# Summary

**Favicon add karne ke 3 simple steps:**

### 1. Ek small square image banao.

**Example File Name:**

```text
favicon.ico
```

### 2. File ko website folder me rakho.

```text
index.html
favicon.ico
```

### 3. `<head>` section me ye line add karo.

```html
<link rel="icon" href="favicon.ico">
```

**Bas itna hi! 🎉** Ab aapki website browser tab me apna favicon show karegi.