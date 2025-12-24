# How This Blog Was Created
<p class="article-date">December 24, 2024</p>

*Ever wondered how this calculus blog works? This guide walks you through everything from scratch - Markdown basics, math equations with KaTeX, the Docsify framework, and deploying to GitHub Pages. By the end, you'll be able to create your own articles!*

---

## What You'll Learn

- Write content using Markdown syntax
- Create beautiful math equations with KaTeX
- Understand how Docsify turns files into a website
- Set up and test the blog locally
- Create a new article from scratch
- Deploy to GitHub Pages

---

## Part 1: Markdown Basics

### What is Markdown?

**Markdown** is a lightweight text formatting language. Instead of clicking buttons like in Word, you use simple symbols to format text. It's:
- Easy to read even without rendering
- Used everywhere: GitHub, Reddit, Discord, Notion
- Perfect for technical writing

### Essential Markdown Syntax

#### Headings

```markdown
# Heading 1 (Title)
## Heading 2 (Section)
### Heading 3 (Subsection)
#### Heading 4 (Sub-subsection)
```

#### Text Formatting

```markdown
**bold text**
*italic text*
***bold and italic***
~~strikethrough~~
`inline code`
```

Renders as: **bold text**, *italic text*, ***bold and italic***, ~~strikethrough~~, `inline code`

#### Lists

**Unordered list:**
```markdown
- Item one
- Item two
  - Nested item
  - Another nested
- Item three
```

**Ordered list:**
```markdown
1. First step
2. Second step
3. Third step
```

#### Links and Images

```markdown
[Link text](https://example.com)
![Alt text for image](path/to/image.png)
```

#### Blockquotes

```markdown
> This is a quote.
> It can span multiple lines.
```

Renders as:
> This is a quote.
> It can span multiple lines.

#### Code Blocks

For multi-line code, use triple backticks with the language name:

````markdown
```python
def hello():
    print("Hello, World!")
```
````

Renders as:
```python
def hello():
    print("Hello, World!")
```

#### Tables

```markdown
| Column 1 | Column 2 | Column 3 |
|----------|----------|----------|
| Row 1    | Data     | Data     |
| Row 2    | Data     | Data     |
```

Renders as:

| Column 1 | Column 2 | Column 3 |
|----------|----------|----------|
| Row 1    | Data     | Data     |
| Row 2    | Data     | Data     |

#### Horizontal Rule

```markdown
---
```

Creates a dividing line like the ones separating sections in this article.

#### HTML in Markdown

You can use HTML directly in Markdown:

```html
<details>
<summary>Click to expand</summary>

Hidden content goes here!

</details>
```

Renders as:

<details>
<summary>Click to expand</summary>

Hidden content goes here!

</details>

---

## Part 2: KaTeX for Math Equations

### What is KaTeX?

**KaTeX** (pronounced "kay-tech") is a fast math rendering library. It takes LaTeX-style syntax and displays beautiful mathematical equations in web browsers.

### Inline vs Display Math

**Inline math** appears within text using single dollar signs:
```markdown
The derivative is $f'(x) = 2x$.
```
Renders as: The derivative is $f'(x) = 2x$.

**Display math** appears centered on its own line using double dollar signs:
```markdown
$$f(x) = \int_a^b g(t) \, dt$$
```
Renders as:
$$f(x) = \int_a^b g(t) \, dt$$

### Essential KaTeX Syntax

#### Basic Operations

| What you want | KaTeX code | Result |
|---------------|------------|--------|
| Fraction | `\frac{a}{b}` | $\frac{a}{b}$ |
| Square root | `\sqrt{x}` | $\sqrt{x}$ |
| nth root | `\sqrt[n]{x}` | $\sqrt[n]{x}$ |
| Exponent | `x^2` or `x^{10}` | $x^2$, $x^{10}$ |
| Subscript | `x_1` or `x_{max}` | $x_1$, $x_{max}$ |
| Both | `x_1^2` | $x_1^2$ |

#### Greek Letters

| Letter | Code | Letter | Code |
|--------|------|--------|------|
| $\alpha$ | `\alpha` | $\beta$ | `\beta` |
| $\gamma$ | `\gamma` | $\delta$ | `\delta` |
| $\theta$ | `\theta` | $\pi$ | `\pi` |
| $\sigma$ | `\sigma` | $\omega$ | `\omega` |

#### Calculus Symbols

| What you want | KaTeX code | Result |
|---------------|------------|--------|
| Derivative | `\frac{dy}{dx}` | $\frac{dy}{dx}$ |
| Partial | `\frac{\partial f}{\partial x}` | $\frac{\partial f}{\partial x}$ |
| Integral | `\int f(x) \, dx` | $\int f(x) \, dx$ |
| Definite integral | `\int_a^b f(x) \, dx` | $\int_a^b f(x) \, dx$ |
| Limit | `\lim_{x \to a} f(x)` | $\lim_{x \to a} f(x)$ |
| Sum | `\sum_{i=1}^{n} i` | $\sum_{i=1}^{n} i$ |
| Infinity | `\infty` | $\infty$ |

#### Comparison and Logic

| Symbol | Code | Symbol | Code |
|--------|------|--------|------|
| $\leq$ | `\leq` | $\geq$ | `\geq` |
| $\neq$ | `\neq` | $\approx$ | `\approx` |
| $\pm$ | `\pm` | $\times$ | `\times$ |
| $\cdot$ | `\cdot` | $\div$ | `\div` |

#### Functions and Formatting

```latex
\sin(x), \cos(x), \tan(x), \ln(x), \log(x)
```
Renders as: $\sin(x), \cos(x), \tan(x), \ln(x), \log(x)$

**Spacing in equations:**
- `\,` small space
- `\:` medium space
- `\;` large space
- `\quad` even larger space

#### Complex Examples

**Power Rule:**
```latex
$$\frac{d}{dx}[x^n] = nx^{n-1}$$
```
$$\frac{d}{dx}[x^n] = nx^{n-1}$$

**Quadratic Formula:**
```latex
$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$
```
$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

**Chain Rule:**
```latex
$$\frac{d}{dx}[f(g(x))] = f'(g(x)) \cdot g'(x)$$
```
$$\frac{d}{dx}[f(g(x))] = f'(g(x)) \cdot g'(x)$$

**Fundamental Theorem of Calculus:**
```latex
$$\int_a^b f(x) \, dx = F(b) - F(a)$$
```
$$\int_a^b f(x) \, dx = F(b) - F(a)$$

---

## Part 3: Practice Assignments

### Assignment 1: Markdown Basics

Create a markdown file with:
1. A main title and two section headings
2. A paragraph with **bold** and *italic* text
3. An unordered list of 3 items
4. An ordered list of 3 steps
5. A table with 3 columns and 2 rows
6. A blockquote
7. A code block in any language

### Assignment 2: KaTeX Equations

Write the KaTeX code for these equations:

1. $y = mx + b$

2. $\frac{x^2 + 1}{x - 3}$

3. $\lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$

4. $\int_0^{\pi} \sin(x) \, dx$

5. $\sum_{n=1}^{\infty} \frac{1}{n^2}$

<details>
<summary><strong>Check Your Answers</strong></summary>

1. `$y = mx + b$`
2. `$\frac{x^2 + 1}{x - 3}$`
3. `$\lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$`
4. `$\int_0^{\pi} \sin(x) \, dx$`
5. `$\sum_{n=1}^{\infty} \frac{1}{n^2}$`

</details>

### Assignment 3: Collapsible Solutions

Create a practice problem with a hidden solution using this pattern:

```markdown
**Problem:** Find $\frac{d}{dx}[x^3 + 2x]$

<details>
<summary><strong>Solution</strong></summary>

Using the power rule:
$$\frac{d}{dx}[x^3 + 2x] = 3x^2 + 2$$

</details>
```

---

## Part 4: Understanding Docsify

### What is Docsify?

**Docsify** is a documentation site generator that:
- Converts Markdown files into a beautiful website
- Requires no build step - it works directly in the browser
- Supports plugins for search, themes, and math rendering
- Is perfect for documentation and educational content

### How It Works

```
Your Files                    What Users See
-----------                   --------------
_sidebar.md     ──────►      Navigation menu
index.html      ──────►      Site configuration
*.md files      ──────►      Page content
```

When someone visits your site:
1. Browser loads `index.html`
2. Docsify JavaScript reads the URL
3. It fetches the corresponding `.md` file
4. It converts Markdown to HTML
5. KaTeX renders the math equations
6. User sees a beautiful page!

### Key Files Explained

#### `_sidebar.md` - Navigation

This file defines your table of contents:

```markdown
- AP Calculus (AB + BC)

  - Getting Started
    - [Why Calculus Matters](calculus/0001-why-calculus-matters.md)
    - [History of Calculus](calculus/0002-history-of-calculus.md)

  - Unit 1: Limits and Continuity
    - [Functions Refresher](calculus/0201-functions-refresher.md)
    - [Limits Overview](calculus/0203-limits-the-foundation.md)
```

**Key points:**
- Indentation creates hierarchy
- `[Display Name](path/to/file.md)` creates links
- The sidebar updates automatically when you edit this file

#### `index.html` - Site Configuration

This is the brain of your Docsify site. It contains:

**1. Site metadata:**
```html
<title>AP Calculus Blog</title>
<meta name="description" content="Learn calculus...">
```

**2. CSS styling:**
```html
<style>
  body { font-family: 'Inter', sans-serif; }
  .katex { color: #3730a3; }
  /* ... more styles ... */
</style>
```

**3. Docsify configuration:**
```html
<script>
  window.$docsify = {
    name: 'AP Calculus',
    loadSidebar: true,
    subMaxLevel: 2,
    search: 'auto',
    // ... more options ...
  }
</script>
```

**4. Plugin scripts:**
```html
<script src="//cdn.jsdelivr.net/npm/docsify/lib/docsify.min.js"></script>
<script src="//cdn.jsdelivr.net/npm/docsify-katex@latest/dist/docsify-katex.js"></script>
```

#### Article Files (`*.md`)

Each article is a Markdown file with:
- A title (# Heading)
- Optional date tag
- Content sections
- Math equations
- Practice problems
- Navigation footer

---

## Part 5: Testing Locally

### Prerequisites

1. **Node.js** - Download from [nodejs.org](https://nodejs.org)
2. **docsify-cli** - Install globally:
   ```bash
   npm install -g docsify-cli
   ```

### Running the Local Server

1. Open your terminal/command prompt
2. Navigate to your blog folder:
   ```bash
   cd C:/dev/ganga/blog
   ```
3. Start the server:
   ```bash
   docsify serve
   ```
4. Open your browser to `http://localhost:3000`

You'll see your blog running locally! Any changes you save will appear after refreshing the browser.

### Troubleshooting

| Problem | Solution |
|---------|----------|
| "docsify not found" | Run `npm install -g docsify-cli` again |
| Page not loading | Check file path in `_sidebar.md` |
| Math not rendering | Verify KaTeX script is in `index.html` |
| Styles broken | Clear browser cache (Ctrl+Shift+R) |

---

## Part 6: Creating a New Article (Step-by-Step)

Let's create a simple Unit 7 article on **Slope Fields**.

### Step 1: Create the File

Create a new file: `calculus/0801-slope-fields.md`

The naming convention is:
- `08` = Unit 7 (unit number + 1, because 00 is Getting Started)
- `01` = First article in the unit
- `slope-fields` = Descriptive name

### Step 2: Add the Basic Structure

```markdown
# Slope Fields
<p class="article-date">December 24, 2024</p>

*Introduction paragraph explaining what slope fields are and why they matter.*

---

## What You'll Learn

- Objective 1
- Objective 2
- Objective 3

---

## The Core Concept

Explanation goes here...

### Key Formula

$$\frac{dy}{dx} = f(x, y)$$

### Example 1

**Problem:** Draw the slope field for $\frac{dy}{dx} = x + y$

**Solution:**
Step-by-step solution...

---

## Practice Problems

### Problem 1

Question here...

<details>
<summary><strong>Answer</strong></summary>

Solution here...

</details>

---

<div align="center">

[← Previous Article](/calculus/0705-particle-motion-integrals) | [Next Article →](/calculus/0802-eulers-method)

</div>
```

### Step 3: Update the Sidebar

Edit `_sidebar.md` and add your new article:

```markdown
  - Unit 7: Differential Equations
    - [Slope Fields](calculus/0801-slope-fields.md)
    - [Euler Method](calculus/0802-eulers-method.md)
```

### Step 4: Test Locally

```bash
cd C:/dev/ganga/blog
docsify serve
```

Visit `http://localhost:3000/#/calculus/0801-slope-fields` to see your article!

### Step 5: Verify

Check that:
- [ ] Title appears correctly
- [ ] Date shows below the title
- [ ] Math equations render properly
- [ ] Navigation links work
- [ ] Article appears in sidebar

---

## Part 7: Git, GitHub, and GitHub Pages

### What is Git?

**Git** is a version control system that:
- Tracks changes to your files over time
- Lets you undo mistakes by going back to previous versions
- Allows multiple people to work on the same project
- Creates a complete history of your project

Think of it like "Track Changes" in Word, but for your entire project.

### Essential Git Commands

```bash
# Check what files have changed
git status

# Add files to be committed
git add .                    # Add all files
git add filename.md          # Add specific file

# Save changes with a message
git commit -m "Add slope fields article"

# Upload to GitHub
git push
```

### What is GitHub?

**GitHub** is a website that:
- Stores your Git repositories online
- Provides a backup of your code
- Enables collaboration with others
- Offers free hosting via GitHub Pages

### What is GitHub Pages?

**GitHub Pages** turns your repository into a live website:

```
Your Repository              Live Website
---------------              ------------
github.com/you/blog    ►    you.github.io/blog
```

It's completely free and automatically updates when you push changes!

### How It All Works Together

```
1. You edit files locally
        ↓
2. git add . (stage changes)
        ↓
3. git commit -m "message" (save snapshot)
        ↓
4. git push (upload to GitHub)
        ↓
5. GitHub Pages rebuilds your site
        ↓
6. Changes appear live in ~1 minute!
```

### Complete Workflow Example

Let's say you just created the slope fields article:

```bash
# 1. Check what changed
git status
# Shows: new file: calculus/0801-slope-fields.md
#        modified: _sidebar.md

# 2. Stage all changes
git add .

# 3. Commit with a descriptive message
git commit -m "Add slope fields article to Unit 7"

# 4. Push to GitHub
git push

# 5. Wait ~1 minute, then visit your live site!
```

### Setting Up GitHub Pages (One-Time)

1. Go to your repository on GitHub
2. Click **Settings** → **Pages**
3. Under "Source", select **main** branch
4. Select **/ (root)** folder
5. Click **Save**
6. Your site will be live at `https://username.github.io/repository-name`

---

## Quick Reference Card

### Markdown Cheatsheet

| Element | Syntax |
|---------|--------|
| Heading | `# H1` `## H2` `### H3` |
| Bold | `**text**` |
| Italic | `*text*` |
| Link | `[text](url)` |
| Image | `![alt](path)` |
| Code | `` `code` `` |
| List | `- item` or `1. item` |
| Quote | `> quote` |
| Table | `| col | col |` |

### KaTeX Cheatsheet

| Element | Syntax |
|---------|--------|
| Fraction | `\frac{a}{b}` |
| Exponent | `x^2` or `x^{n+1}` |
| Subscript | `x_1` or `x_{max}` |
| Square root | `\sqrt{x}` |
| Integral | `\int_a^b f \, dx` |
| Limit | `\lim_{x \to a}` |
| Sum | `\sum_{i=1}^{n}` |
| Greek | `\alpha \beta \pi` |

### Git Cheatsheet

| Command | Purpose |
|---------|---------|
| `git status` | See what changed |
| `git add .` | Stage all changes |
| `git commit -m "msg"` | Save snapshot |
| `git push` | Upload to GitHub |
| `git pull` | Download latest |
| `git log` | View history |

---

## Conclusion

You now have all the knowledge needed to:

1. **Write content** using Markdown formatting
2. **Create equations** using KaTeX math syntax
3. **Understand the structure** of this Docsify blog
4. **Test changes locally** before publishing
5. **Create new articles** following the established pattern
6. **Deploy to GitHub Pages** for the world to see

The best way to learn is by doing. Start by making small edits to existing articles, then try creating your own. Don't worry about mistakes - Git keeps a history of everything, so you can always go back!

Happy blogging!

---

<div align="center">

[← History of Calculus](/calculus/0002-history-of-calculus) | [Domain and Range →](/calculus/0101-domain-and-range)

</div>
