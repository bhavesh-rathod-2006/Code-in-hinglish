# HTML Computer Code Elements: Focused Examples

HTML me kuch special elements diye gaye hain jo **computer code, keyboard input, program output aur variables** ko represent karne ke liye use hote hain.

Ye elements hain:

- `<code>`
- `<pre>`
- `<kbd>`
- `<samp>`
- `<var>`

Ye sab normally **monospace font** me display hote hain, jisse technical content aur code easily readable dikhta hai.

---

## 1. The `<code>` Element

`<code>` element ka use **inline computer code** dikhane ke liye hota hai. Jaise function names, variables, commands ya chhote code snippets jo sentence ke andar likhe jaate hain.

Ye text ko monospace font me display karta hai taaki wo normal text se alag dikhe.

### Example 1: Inline Function Name

```html
<p>In Python, the <code>len()</code> function returns the length of a string or list.</p>
```

**Explanation (Hinglish):**

Ye example Python ke `len()` function ko monospace font me highlight karta hai.

---

### Example 2: Inline Code Snippet

```html
<p>To check if a file exists in Bash, use the <code>test -f filename</code> condition.</p>
```

**Explanation (Hinglish):**

Ye Bash command ko inline code ki tarah display karta hai.

---

### Example 3: Inline CSS Property

```html
<p>To center an element in CSS, set the <code>margin: auto;</code> property.</p>
```

**Explanation (Hinglish):**

Ye CSS property `margin: auto;` ko inline monospace font me highlight karta hai.

---

## 2. The `<pre>` Element

`<pre>` element ka use **preformatted text** display karne ke liye hota hai.

Ye spaces, tabs aur line breaks ko exactly preserve karta hai. Isliye ye multi-line code aur formatted text ke liye best hai.

### Example 1: Python Code Block

```html
<pre>
def factorial(n):
    if n == 0:
        return 1
    return n * factorial(n - 1)
</pre>
```

**Explanation (Hinglish):**

Ye Python function ko uski original indentation aur formatting ke saath display karta hai.

---

### Example 2: ASCII Art

```html
<pre>
   _____
  /     \
 /_______\
</pre>
```

**Explanation (Hinglish):**

Ye ASCII art ko same spacing aur line breaks ke saath show karta hai.

---

### Example 3: Terminal Command Sequence

```html
<pre>
git init
git add .
git commit -m "Initial commit"
</pre>
```

**Explanation (Hinglish):**

Ye Git commands ko terminal ki tarah line-by-line display karta hai.

---

## 3. The `<kbd>` Element

`<kbd>` element ka use **user keyboard input** ya kisi button press ko represent karne ke liye hota hai.

Ye keyboard shortcuts, terminal commands aur game controller buttons dikhane ke liye use hota hai.

### Example 1: Keyboard Shortcut

```html
<p>To copy text, press <kbd>Ctrl + C</kbd>.</p>
```

**Explanation (Hinglish):**

Ye `Ctrl + C` keyboard shortcut ko highlight karta hai.

---

### Example 2: Terminal Command

```html
<p>To list directory contents, type <kbd>dir</kbd> in the Windows Command Prompt.</p>
```

**Explanation (Hinglish):**

Ye `dir` command ko user input ki tarah display karta hai.

---

### Example 3: Game Controller Input

```html
<p>In the game, press <kbd>X</kbd> to jump.</p>
```

**Explanation (Hinglish):**

Ye game ke `X` button ko keyboard/game input ki tarah show karta hai.

---

## 4. The `<samp>` Element

`<samp>` element ka use **sample output** ya **program output** dikhane ke liye hota hai.

Ye console messages, outputs aur error logs ko monospace font me display karta hai.

### Example 1: Python Output

```html
<p>The output of the command is <samp>Hello, World!</samp>.</p>
```

**Explanation (Hinglish):**

Ye program ka output `Hello, World!` sample output ki tarah dikhata hai.

---

### Example 2: Error Message

```html
<p>If the file is missing, you might see <samp>FileNotFoundError: [Errno 2] No such file or directory</samp>.</p>
```

**Explanation (Hinglish):**

Ye Python ka error message sample output ki tarah display karta hai.

---

### Example 3: Terminal Output

```html
<p>Running <samp>pwd</samp> in the terminal outputs <samp>/home/user/project</samp>.</p>
```

**Explanation (Hinglish):**

Ye terminal command ka output monospace font me dikhata hai.

---

## 5. The `<var>` Element

`<var>` element ka use **variables** ya placeholders ko represent karne ke liye hota hai.

Browser me ye usually italic style me display hota hai.

### Example 1: Mathematical Variable

```html
<p>In the formula <var>F = ma</var>, <var>m</var> represents mass.</p>
```

**Explanation (Hinglish):**

Ye physics formula me `m` variable ko highlight karta hai.

---

### Example 2: Programming Variable

```html
<p>In Python, assign a value to <var>count</var> using <var>count = 10</var>.</p>
```

**Explanation (Hinglish):**

Ye programming variable `count` aur uski assignment ko variable ki tarah show karta hai.

---

### Example 3: Placeholder in Command

```html
<p>Use <var>username</var> in the command <var>ssh username@host</var>.</p>
```

**Explanation (Hinglish):**

Ye SSH command me `username` ko placeholder variable ki tarah display karta hai.

---

# Styling Computer Code Elements

CSS ki help se in elements ko aur readable aur attractive banaya ja sakta hai.

## Example: Styled `<pre>` Block

```html
<style>
  pre {
    background-color: #1e1e1e;
    color: #ffffff;
    padding: 15px;
    border-radius: 5px;
    font-family: Consolas, monospace;
  }
</style>

<pre>
for i in range(5):
    print(i)
</pre>
```

**Explanation (Hinglish):**

Ye `<pre>` block ko dark background, white text aur monospace font ke saath style karta hai.

---

## Example: Styled `<kbd>` Input

```html
<style>
  kbd {
    background-color: #f4f4f4;
    padding: 2px 4px;
    border: 1px solid #ccc;
    border-radius: 3px;
    font-family: Consolas, monospace;
  }
</style>

<p>Press <kbd>Enter</kbd> to submit the form.</p>
```

**Explanation (Hinglish):**

Ye `<kbd>` element ko keyboard key jaisa look deta hai.

---

## Best Practices

- **Use Specific Elements:** Har purpose ke liye sahi element use karo (`<code>`, `<pre>`, `<kbd>`, `<samp>`, `<var>`).
- **Preserve Formatting:** Multi-line code aur formatted text ke liye `<pre>` use karo.
- **Escape HTML Characters:** HTML code dikhate waqt `<` aur `>` ki jagah `&lt;` aur `&gt;` use karo.
- **Styling:** Monospace fonts aur CSS background colors use karke readability improve karo.
- **Accessibility:** Keyboard shortcuts ya outputs ke saath proper context likho, jaise `Press <kbd>Ctrl + C</kbd> to copy`.
- **Avoid Overuse:** Ye tags sirf technical content aur code ke liye hi use karo.

---

## Summary

HTML ke computer code elements technical content ko proper format me display karte hain.

| **Element** | **Use (Hinglish)** |
|-------------|---------------------|
| `<code>` | Inline code snippets, functions aur commands dikhane ke liye. |
| `<pre>` | Multi-line code aur formatted text ko original spacing ke saath display karne ke liye. |
| `<kbd>` | Keyboard shortcuts, terminal commands aur user input dikhane ke liye. |
| `<samp>` | Program ya terminal ka sample output aur error messages dikhane ke liye. |
| `<var>` | Variables aur placeholders ko represent karne ke liye. |

In elements ka sahi use code ko readable, professional aur semantically correct banata hai.