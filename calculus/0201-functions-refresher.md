# Functions Refresher
<p class="article-date">August 3, 2024</p>

*Before we dive into calculus, let's make sure we're speaking the same language. Functions are EVERYTHING in calc - if you're shaky here, everything else will feel harder than it needs to be.*

---

## What Is a Function, Really?

Forget the formal definition for a sec. Here's how I think about it:

> **A function is a machine. You put something in, it does something to it, and you get something out.**

That's it. Input → Process → Output.

### The Vending Machine Analogy

- You input: **B4** (the code)
- The machine processes: finds row B, column 4
- You get output: **Snickers bar**

Same input always gives same output. That's a function.

### Not a Function?

Imagine a broken vending machine where pressing B4 sometimes gives you Snickers, sometimes gives you Doritos.

**That's NOT a function.** Functions must be consistent - same input = same output, every time.

---

## Function Notation

### The Basics

$$f(x) = x^2 + 3$$

Let's break this down:

| Symbol | Meaning |
|--------|---------|
| f | The name of the function (like naming your machine) |
| x | The input (what you put in) |
| f(x) | The output (what you get out) - read as "f of x" |
| x² + 3 | The rule (what the machine does) |

### Examples

If $f(x) = x^2 + 3$:

- $f(2) = 2^2 + 3 = 4 + 3 = 7$
- $f(-1) = (-1)^2 + 3 = 1 + 3 = 4$
- $f(0) = 0^2 + 3 = 0 + 3 = 3$
- $f(a) = a^2 + 3$
- $f(x+h) = (x+h)^2 + 3$

> **AP Alert**: That last one - $f(x+h)$ - shows up CONSTANTLY in calculus. Get comfortable substituting expressions, not just numbers.

---

## The Functions You MUST Know for AP Calc

### 1. Polynomial Functions

$$f(x) = x^3 - 2x^2 + 5x - 1$$

**Key features:**
- Smooth, continuous curves
- No breaks, no holes
- Easy to differentiate (you'll love these in calc)

### 2. Rational Functions

$$f(x) = \frac{x^2 - 1}{x + 2}$$

**Key features:**
- Fractions with polynomials
- Watch out for values that make denominator = 0 (undefined!)
- Can have vertical asymptotes

### 3. Trigonometric Functions

$$f(x) = \sin(x), \cos(x), \tan(x)$$

**What you need to know:**
- Unit circle values (0°, 30°, 45°, 60°, 90° and their radian equivalents)
- Graphs and their shapes
- Periods: sin and cos repeat every $2\pi$, tan repeats every $\pi$

| Angle | sin | cos | tan |
|-------|-----|-----|-----|
| 0 | 0 | 1 | 0 |
| π/6 | 1/2 | √3/2 | √3/3 |
| π/4 | √2/2 | √2/2 | 1 |
| π/3 | √3/2 | 1/2 | √3 |
| π/2 | 1 | 0 | undefined |

### 4. Exponential Functions

$$f(x) = e^x, \quad f(x) = 2^x, \quad f(x) = a^x$$

**Key features:**
- Always positive (never crosses x-axis)
- $e ≈ 2.718$ (this number is SPECIAL in calculus)
- Grows super fast

> **Why e is special**: The derivative of $e^x$ is just $e^x$. It's the only function that equals its own derivative. Mind = blown.

### 5. Logarithmic Functions

$$f(x) = \ln(x), \quad f(x) = \log(x)$$

**Key features:**
- Inverse of exponential
- Only defined for x > 0
- $\ln$ means natural log (base e)
- Grows super slow

**Essential log rules:**
- $\ln(ab) = \ln(a) + \ln(b)$
- $\ln(a/b) = \ln(a) - \ln(b)$
- $\ln(a^n) = n \cdot \ln(a)$
- $\ln(e) = 1$
- $\ln(1) = 0$

### 6. Absolute Value Function

$$f(x) = |x|$$

**Key feature:**
- Has a sharp corner at x = 0
- This corner matters in calculus (derivative doesn't exist there!)

### 7. Square Root Function

$$f(x) = \sqrt{x}$$

**Key features:**
- Only defined for x ≥ 0
- Same as $x^{1/2}$ (this form is better for calculus)

---

## Domain and Range

### Domain = Valid Inputs

"What can I put into this machine?"

**Common restrictions:**
- Can't divide by zero → exclude values that make denominator 0
- Can't take square root of negative → restrict to non-negative inputs
- Can't take log of zero or negative → restrict to positive inputs

### Range = Possible Outputs

"What can this machine produce?"

### Example

$$f(x) = \sqrt{x-3}$$

**Domain**: Need $x - 3 \geq 0$, so $x \geq 3$. Domain: $[3, \infty)$

**Range**: Square root always gives non-negative outputs. Range: $[0, \infty)$

---

## Function Operations

### Adding/Subtracting

$(f + g)(x) = f(x) + g(x)$

$(f - g)(x) = f(x) - g(x)$

### Multiplying/Dividing

$(f \cdot g)(x) = f(x) \cdot g(x)$

$\left(\frac{f}{g}\right)(x) = \frac{f(x)}{g(x)}$ (where $g(x) \neq 0$)

### Composition (Super Important!)

$(f \circ g)(x) = f(g(x))$

This means: first apply g, then apply f to the result.

**Example:**

If $f(x) = x^2$ and $g(x) = x + 1$:

$(f \circ g)(x) = f(g(x)) = f(x+1) = (x+1)^2$

$(g \circ f)(x) = g(f(x)) = g(x^2) = x^2 + 1$

Notice: $f \circ g \neq g \circ f$ in general! Order matters!

> **AP Alert**: Function composition is the foundation of the Chain Rule - the most important derivative rule. Master this now.

---

## Graphing Essentials

### Key Features to Identify

1. **Intercepts**
   - x-intercepts: where $f(x) = 0$
   - y-intercept: $f(0)$

2. **Symmetry**
   - Even function: $f(-x) = f(x)$ (symmetric about y-axis)
   - Odd function: $f(-x) = -f(x)$ (symmetric about origin)

3. **Asymptotes**
   - Vertical: where function → ±∞
   - Horizontal: where function levels off as x → ±∞

4. **Increasing/Decreasing**
   - Where is the function going up? Down?
   - This is EXACTLY what derivatives tell us!

---

## Transformations (Quick Reference)

Starting with $y = f(x)$:

| Transformation | Effect |
|---------------|--------|
| $y = f(x) + c$ | Shift UP by c |
| $y = f(x) - c$ | Shift DOWN by c |
| $y = f(x + c)$ | Shift LEFT by c |
| $y = f(x - c)$ | Shift RIGHT by c |
| $y = -f(x)$ | Reflect over x-axis |
| $y = f(-x)$ | Reflect over y-axis |
| $y = cf(x)$ | Vertical stretch by c |
| $y = f(cx)$ | Horizontal compress by c |

> **Memory trick**: Changes INSIDE the parentheses (affecting x) work "backwards" from what you'd expect.

---

## The Difference Quotient Preview

Here's why all of this matters for calculus. The derivative is defined as:

$$f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$$

To use this, you MUST be able to:

1. Find $f(x+h)$ - substitute $(x+h)$ into your function
2. Subtract $f(x)$
3. Simplify the algebra

### Example: Let's Practice

$f(x) = x^2$

**Step 1**: Find $f(x+h)$
$$f(x+h) = (x+h)^2 = x^2 + 2xh + h^2$$

**Step 2**: Compute $f(x+h) - f(x)$
$$x^2 + 2xh + h^2 - x^2 = 2xh + h^2$$

**Step 3**: Divide by h
$$\frac{2xh + h^2}{h} = \frac{h(2x + h)}{h} = 2x + h$$

**Step 4**: Let h → 0
$$2x + 0 = 2x$$

So the derivative of $x^2$ is $2x$!

---

## Practice Problems

### Problem 1

If $f(x) = 3x^2 - 2x + 1$, find $f(x+h)$.

<details>
<summary>Click for Answer</summary>

$$f(x+h) = 3(x+h)^2 - 2(x+h) + 1$$
$$= 3(x^2 + 2xh + h^2) - 2x - 2h + 1$$
$$= 3x^2 + 6xh + 3h^2 - 2x - 2h + 1$$

</details>

### Problem 2

Find the domain of $f(x) = \frac{\sqrt{x+4}}{x-2}$

<details>
<summary>Click for Answer</summary>

Two restrictions:
1. Inside square root must be ≥ 0: $x + 4 \geq 0 → x \geq -4$
2. Denominator can't be 0: $x \neq 2$

Domain: $[-4, 2) \cup (2, \infty)$

</details>

### Problem 3

If $f(x) = e^x$ and $g(x) = \ln(x)$, find $(f \circ g)(x)$ and $(g \circ f)(x)$.

<details>
<summary>Click for Answer</summary>

$(f \circ g)(x) = f(g(x)) = f(\ln(x)) = e^{\ln(x)} = x$

$(g \circ f)(x) = g(f(x)) = g(e^x) = \ln(e^x) = x$

They're inverses! Composing a function with its inverse gives you back x.

</details>

---

## Key Takeaways

| Concept | Why It Matters for Calculus |
|---------|----------------------------|
| Function notation | You'll write $f'(x)$, $f''(x)$, etc. for derivatives |
| Substituting $f(x+h)$ | Foundation of derivative definition |
| Function composition | Needed for Chain Rule |
| Domain restrictions | Important for continuity and differentiability |
| Parent functions | You'll memorize their derivatives |

---

## Up Next

Now that we're solid on functions, let's explore **The Concept of Change** - where we start thinking about rates and slopes, the heart of calculus.

---

*If functions still feel fuzzy, that's okay. Bookmark this page. You'll come back to it when we hit derivatives and suddenly these examples will make even more sense.*

---

<div align="center">

[← History of Calculus](calculus/history-of-calculus.md) | [Concept of Change →](calculus/the-concept-of-change.md)

</div>
