# Inverse Functions
<p class="article-date">June 28, 2024</p>

## Prerequisites
Before diving in, make sure you're comfortable with:
- [Domain and Range](/calculus/0101-domain-and-range)
- [Composite Functions](/calculus/0102-composite-functions)
- Solving equations for a variable

## Learning Objectives
By the end of this section, you will be able to:
- Understand inverse functions as "undo" operations
- Determine if a function has an inverse (one-to-one test)
- Find inverse functions algebraically
- Graph inverse functions using reflection over $y = x$
- Verify inverses using composition
- Work with restricted domains to create inverses

## The Big Picture: Undoing Functions

An **inverse function** reverses what the original function does.

If $f$ takes input $a$ and produces output $b$:
$$f(a) = b$$

Then $f^{-1}$ (read "f inverse") takes $b$ and returns $a$:
$$f^{-1}(b) = a$$

> **Intuition**: If $f$ is "double and add 3," then $f^{-1}$ is "subtract 3 and halve."

### Example
- $f(x) = 2x + 3$ converts $4 \to 11$
- $f^{-1}(x) = \frac{x - 3}{2}$ converts $11 \to 4$

## The Defining Property

Two functions are inverses if and only if:

$$f(f^{-1}(x)) = x \quad \text{AND} \quad f^{-1}(f(x)) = x$$

In other words, composing a function with its inverse (in either order) gives you back the original input.

## When Does an Inverse Exist?

**Not every function has an inverse.** A function has an inverse only if it is **one-to-one** (also called injective).

### One-to-One Definition
A function is one-to-one if different inputs always produce different outputs:
$$\text{If } f(a) = f(b), \text{ then } a = b$$

### The Horizontal Line Test

**Graphically**: A function has an inverse if and only if every horizontal line crosses the graph at most once.

| Function | One-to-One? | Has Inverse? |
|----------|-------------|--------------|
| $f(x) = x^2$ (all $x$) | No (e.g., $f(-2) = f(2) = 4$) | No |
| $f(x) = x^3$ | Yes | Yes |
| $f(x) = \|x\|$ | No | No |
| $f(x) = 2x + 5$ | Yes (linear, non-zero slope) | Yes |
| $f(x) = e^x$ | Yes | Yes |

## Finding Inverse Functions Algebraically

### The Three-Step Method

1. Replace $f(x)$ with $y$
2. Swap $x$ and $y$
3. Solve for $y$, then write as $f^{-1}(x)$

### Worked Example 1: Linear Function

**Problem**: Find the inverse of $f(x) = 3x - 7$.

**Solution**:

**Step 1**: Write as $y = 3x - 7$

**Step 2**: Swap $x$ and $y$: $x = 3y - 7$

**Step 3**: Solve for $y$:
$$x + 7 = 3y$$
$$y = \frac{x + 7}{3}$$

**Answer**: $f^{-1}(x) = \dfrac{x + 7}{3}$

**Verify**:
- $f(f^{-1}(x)) = f\left(\frac{x+7}{3}\right) = 3 \cdot \frac{x+7}{3} - 7 = x + 7 - 7 = x$ ✓
- $f^{-1}(f(x)) = f^{-1}(3x - 7) = \frac{(3x-7)+7}{3} = \frac{3x}{3} = x$ ✓

### Worked Example 2: Rational Function

**Problem**: Find the inverse of $f(x) = \dfrac{2x + 1}{x - 3}$.

**Solution**:

**Step 1**: $y = \dfrac{2x + 1}{x - 3}$

**Step 2**: Swap: $x = \dfrac{2y + 1}{y - 3}$

**Step 3**: Solve for $y$:
$$x(y - 3) = 2y + 1$$
$$xy - 3x = 2y + 1$$
$$xy - 2y = 3x + 1$$
$$y(x - 2) = 3x + 1$$
$$y = \frac{3x + 1}{x - 2}$$

**Answer**: $f^{-1}(x) = \dfrac{3x + 1}{x - 2}$

### Worked Example 3: Radical Function

**Problem**: Find the inverse of $f(x) = \sqrt{x - 4}$ for $x \ge 4$.

**Solution**:

**Step 1**: $y = \sqrt{x - 4}$

**Step 2**: Swap: $x = \sqrt{y - 4}$

**Step 3**: Solve for $y$:
$$x^2 = y - 4$$
$$y = x^2 + 4$$

**Answer**: $f^{-1}(x) = x^2 + 4$ for $x \ge 0$

Note: The domain of $f^{-1}$ is the range of $f$, which is $[0, \infty)$.

## Domain and Range of Inverses

**Key Relationship**:
- Domain of $f^{-1}$ = Range of $f$
- Range of $f^{-1}$ = Domain of $f$

The domain and range swap when you find the inverse!

### Worked Example 4: Finding Domain/Range

**Problem**: If $f(x) = \sqrt{x + 2}$ has domain $[-2, \infty)$, find the domain and range of $f^{-1}$.

**Solution**:

First, find the range of $f$:
- As $x$ goes from $-2$ to $\infty$, $\sqrt{x+2}$ goes from $0$ to $\infty$
- Range of $f$: $[0, \infty)$

Now apply the swap:
- Domain of $f^{-1}$ = Range of $f$ = $[0, \infty)$
- Range of $f^{-1}$ = Domain of $f$ = $[-2, \infty)$

## Graphing Inverse Functions

**The Reflection Principle**: The graph of $f^{-1}$ is the reflection of the graph of $f$ over the line $y = x$.

Why? Because if $(a, b)$ is on the graph of $f$ (meaning $f(a) = b$), then $(b, a)$ is on the graph of $f^{-1}$ (meaning $f^{-1}(b) = a$).

### Visual Checklist
- The graphs of $f$ and $f^{-1}$ are mirror images across $y = x$
- Points where $f$ crosses $y = x$ are **fixed points** (same on both graphs)
- If $f$ passes the horizontal line test, so does $f^{-1}$ for the vertical line test

## Restricting Domains

Functions that fail the horizontal line test can have inverses if we **restrict the domain**.

### Worked Example 5: Restricting $x^2$

**Problem**: Find an inverse for $f(x) = x^2$.

**Solution**:

$f(x) = x^2$ is not one-to-one on $(-\infty, \infty)$ because $f(-2) = f(2) = 4$.

**Restriction 1**: Define $f(x) = x^2$ for $x \ge 0$ only.
- Now $f$ is one-to-one
- $f^{-1}(x) = \sqrt{x}$ for $x \ge 0$

**Restriction 2**: Define $f(x) = x^2$ for $x \le 0$ only.
- Now $f$ is one-to-one
- $f^{-1}(x) = -\sqrt{x}$ for $x \ge 0$

This is exactly how inverse trig functions are defined—by restricting domains!

## Important Inverse Pairs

| Function | Inverse | Domain Restriction |
|----------|---------|-------------------|
| $f(x) = x^2$ | $f^{-1}(x) = \sqrt{x}$ | $x \ge 0$ for $f$ |
| $f(x) = x^3$ | $f^{-1}(x) = \sqrt[3]{x}$ | None needed |
| $f(x) = e^x$ | $f^{-1}(x) = \ln(x)$ | None needed |
| $f(x) = 10^x$ | $f^{-1}(x) = \log_{10}(x)$ | None needed |
| $f(x) = a^x$ | $f^{-1}(x) = \log_a(x)$ | None needed |

## Common Mistakes to Avoid

1. **Confusing $f^{-1}(x)$ with $\frac{1}{f(x)}$**
   - $f^{-1}(x)$ is the inverse function
   - $\frac{1}{f(x)} = [f(x)]^{-1}$ is the reciprocal
   - Example: If $f(x) = 2x$, then $f^{-1}(x) = \frac{x}{2}$, but $\frac{1}{f(x)} = \frac{1}{2x}$

2. **Forgetting to swap $x$ and $y$**
   - After swapping, $x$ becomes the independent variable

3. **Ignoring domain restrictions**
   - When taking square roots, remember $\sqrt{x^2} = |x|$, not $x$
   - The inverse exists only where the original function is one-to-one

4. **Not verifying the inverse**
   - Always check: $f(f^{-1}(x)) = x$ and $f^{-1}(f(x)) = x$

5. **Wrong domain for the inverse**
   - Domain of $f^{-1}$ equals Range of $f$, not Domain of $f$

## Calculus Connection

Inverse functions are essential in calculus:

1. **Derivative of Inverse Functions**:
   $$\frac{d}{dx}[f^{-1}(x)] = \frac{1}{f'(f^{-1}(x))}$$

2. **Inverse Trig Derivatives**: Finding derivatives of $\arcsin(x)$, $\arctan(x)$, etc.

3. **Logarithmic Differentiation**: Using $\ln(x)$ as the inverse of $e^x$

4. **Integration**: Many integrals result in inverse trig functions

---

## Practice Problems

### Basic (Computational)

**Problem 1**
Find the inverse of $f(x) = 4x + 5$.

<details>
<summary>Show Solution</summary>

**Solution**:
1. $y = 4x + 5$
2. Swap: $x = 4y + 5$
3. Solve: $x - 5 = 4y \implies y = \frac{x - 5}{4}$

**Answer**: $f^{-1}(x) = \dfrac{x - 5}{4}$
</details>

---

**Problem 2**
Find the inverse of $g(x) = \dfrac{x}{3} - 2$.

<details>
<summary>Show Solution</summary>

**Solution**:
1. $y = \frac{x}{3} - 2$
2. Swap: $x = \frac{y}{3} - 2$
3. Solve: $x + 2 = \frac{y}{3} \implies y = 3(x + 2) = 3x + 6$

**Answer**: $g^{-1}(x) = 3x + 6$
</details>

---

**Problem 3**
If $f(x) = x^3 - 1$, find $f^{-1}(x)$.

<details>
<summary>Show Solution</summary>

**Solution**:
1. $y = x^3 - 1$
2. Swap: $x = y^3 - 1$
3. Solve: $x + 1 = y^3 \implies y = \sqrt[3]{x + 1}$

**Answer**: $f^{-1}(x) = \sqrt[3]{x + 1}$
</details>

---

**Problem 4**
Verify that $f(x) = 2x - 6$ and $g(x) = \dfrac{x + 6}{2}$ are inverses.

<details>
<summary>Show Solution</summary>

**Solution**:
Check $f(g(x))$:
$$f\left(\frac{x + 6}{2}\right) = 2 \cdot \frac{x + 6}{2} - 6 = x + 6 - 6 = x \checkmark$$

Check $g(f(x))$:
$$g(2x - 6) = \frac{(2x - 6) + 6}{2} = \frac{2x}{2} = x \checkmark$$

**Verified**: They are inverses.
</details>

---

**Problem 5**
Does $f(x) = x^2 - 4$ have an inverse over all real numbers? Explain.

<details>
<summary>Show Solution</summary>

**Solution**:
No. The function $f(x) = x^2 - 4$ is not one-to-one because:
- $f(-3) = 9 - 4 = 5$
- $f(3) = 9 - 4 = 5$

Different inputs give the same output, so no inverse exists over all real numbers.

To have an inverse, we must restrict the domain to $x \ge 0$ or $x \le 0$.
</details>

---

### Intermediate (Multi-step)

**Problem 6**
Find the inverse of $f(x) = \sqrt{2x + 6}$.

<details>
<summary>Show Solution</summary>

**Solution**:
1. $y = \sqrt{2x + 6}$
2. Swap: $x = \sqrt{2y + 6}$
3. Solve:
   - $x^2 = 2y + 6$
   - $x^2 - 6 = 2y$
   - $y = \frac{x^2 - 6}{2}$

Domain of $f^{-1}$: Since $f$ has range $[0, \infty)$, we need $x \ge 0$.

**Answer**: $f^{-1}(x) = \dfrac{x^2 - 6}{2}$ for $x \ge 0$
</details>

---

**Problem 7**
Find the inverse of $g(x) = \dfrac{3}{x + 2}$.

<details>
<summary>Show Solution</summary>

**Solution**:
1. $y = \frac{3}{x + 2}$
2. Swap: $x = \frac{3}{y + 2}$
3. Solve:
   - $x(y + 2) = 3$
   - $xy + 2x = 3$
   - $xy = 3 - 2x$
   - $y = \frac{3 - 2x}{x}$

**Answer**: $g^{-1}(x) = \dfrac{3 - 2x}{x} = \dfrac{3}{x} - 2$
</details>

---

**Problem 8**
If $f(x) = x^2 + 3$ for $x \ge 0$, find $f^{-1}(x)$ and state its domain.

<details>
<summary>Show Solution</summary>

**Solution**:
1. $y = x^2 + 3$
2. Swap: $x = y^2 + 3$
3. Solve: $y^2 = x - 3 \implies y = \sqrt{x - 3}$

(We take positive root since original domain was $x \ge 0$)

Range of $f$: When $x \ge 0$, $x^2 + 3 \ge 3$, so range is $[3, \infty)$.

**Answer**: $f^{-1}(x) = \sqrt{x - 3}$ with domain $[3, \infty)$
</details>

---

**Problem 9**
The point $(4, 7)$ is on the graph of a one-to-one function $f$. What point must be on the graph of $f^{-1}$?

<details>
<summary>Show Solution</summary>

**Solution**:
If $(4, 7)$ is on $f$, then $f(4) = 7$.

Therefore, $f^{-1}(7) = 4$, meaning $(7, 4)$ is on $f^{-1}$.

**Answer**: $(7, 4)$
</details>

---

**Problem 10**
Find the inverse of $h(x) = \dfrac{x + 4}{x - 1}$.

<details>
<summary>Show Solution</summary>

**Solution**:
1. $y = \frac{x + 4}{x - 1}$
2. Swap: $x = \frac{y + 4}{y - 1}$
3. Solve:
   - $x(y - 1) = y + 4$
   - $xy - x = y + 4$
   - $xy - y = x + 4$
   - $y(x - 1) = x + 4$
   - $y = \frac{x + 4}{x - 1}$

**Answer**: $h^{-1}(x) = \dfrac{x + 4}{x - 1}$

Note: This function is its own inverse! (Called an involution)
</details>

---

### Advanced (Complex Applications)

**Problem 11**
Find the inverse of $f(x) = \dfrac{2x - 3}{4x + 1}$.

<details>
<summary>Show Solution</summary>

**Solution**:
1. $y = \frac{2x - 3}{4x + 1}$
2. Swap: $x = \frac{2y - 3}{4y + 1}$
3. Solve:
   - $x(4y + 1) = 2y - 3$
   - $4xy + x = 2y - 3$
   - $4xy - 2y = -x - 3$
   - $y(4x - 2) = -x - 3$
   - $y = \frac{-x - 3}{4x - 2} = \frac{-(x + 3)}{2(2x - 1)} = \frac{-x - 3}{4x - 2}$

**Answer**: $f^{-1}(x) = \dfrac{-x - 3}{4x - 2}$ or equivalently $\dfrac{x + 3}{2 - 4x}$
</details>

---

**Problem 12**
If $f(x) = x^2 - 6x$ for $x \ge 3$, find $f^{-1}(x)$.

<details>
<summary>Show Solution</summary>

**Solution**:
1. $y = x^2 - 6x$

Complete the square: $y = (x - 3)^2 - 9$

2. Swap: $x = (y - 3)^2 - 9$

3. Solve:
   - $x + 9 = (y - 3)^2$
   - $y - 3 = \pm\sqrt{x + 9}$
   - $y = 3 \pm \sqrt{x + 9}$

Since original domain is $x \ge 3$, range of $f^{-1}$ must be $\ge 3$, so take $+$:

**Answer**: $f^{-1}(x) = 3 + \sqrt{x + 9}$

Domain: Range of $f$ = $[-9, \infty)$ (minimum at $x = 3$ gives $f(3) = 9 - 18 = -9$)
</details>

---

**Problem 13**
Let $f(x) = e^{2x} + 1$. Find $f^{-1}(x)$ and its domain.

<details>
<summary>Show Solution</summary>

**Solution**:
1. $y = e^{2x} + 1$
2. Swap: $x = e^{2y} + 1$
3. Solve:
   - $x - 1 = e^{2y}$
   - $\ln(x - 1) = 2y$
   - $y = \frac{\ln(x - 1)}{2}$

Range of $f$: Since $e^{2x} > 0$ for all $x$, we have $e^{2x} + 1 > 1$, so range is $(1, \infty)$.

**Answer**: $f^{-1}(x) = \dfrac{\ln(x - 1)}{2}$ with domain $(1, \infty)$
</details>

---

**Problem 14**
If $f(x) = \dfrac{1}{x - 2} + 3$ for $x > 2$, find the domain and range of $f^{-1}$.

<details>
<summary>Show Solution</summary>

**Solution**:

First find range of $f$:
- As $x \to 2^+$: $\frac{1}{x-2} \to +\infty$, so $f(x) \to +\infty$
- As $x \to +\infty$: $\frac{1}{x-2} \to 0$, so $f(x) \to 3$

Range of $f$: $(3, \infty)$

Apply the swap:
- **Domain of $f^{-1}$** = Range of $f$ = $(3, \infty)$
- **Range of $f^{-1}$** = Domain of $f$ = $(2, \infty)$
</details>

---

**Problem 15**
Show that $f(x) = \dfrac{ax + b}{cx + d}$ is its own inverse when $a = -d$.

<details>
<summary>Show Solution</summary>

**Solution**:
Find $f(f(x))$ and show it equals $x$ when $a = -d$.

Let $y = f(x) = \frac{ax + b}{cx + d}$

$$f(f(x)) = f\left(\frac{ax + b}{cx + d}\right) = \frac{a \cdot \frac{ax + b}{cx + d} + b}{c \cdot \frac{ax + b}{cx + d} + d}$$

Multiply numerator and denominator by $(cx + d)$:

$$= \frac{a(ax + b) + b(cx + d)}{c(ax + b) + d(cx + d)}$$

$$= \frac{a^2x + ab + bcx + bd}{acx + bc + cdx + d^2}$$

$$= \frac{(a^2 + bc)x + b(a + d)}{(ac + cd)x + (bc + d^2)}$$

$$= \frac{(a^2 + bc)x + b(a + d)}{c(a + d)x + (bc + d^2)}$$

If $a = -d$, then $a + d = 0$:

$$= \frac{(a^2 + bc)x + 0}{0 + (bc + d^2)} = \frac{(a^2 + bc)x}{bc + d^2}$$

Since $a = -d$, we have $a^2 = d^2$, so $a^2 + bc = d^2 + bc = bc + d^2$:

$$= \frac{(bc + d^2)x}{bc + d^2} = x$$

**Verified**: When $a = -d$, $f(f(x)) = x$, so $f$ is its own inverse.
</details>

---

### AP Exam Style

**Problem 16**
If $f(x) = 5 - 2x$, then $f^{-1}(3) = $

(A) $-1$
(B) $1$
(C) $\frac{5}{2}$
(D) $11$

<details>
<summary>Show Solution</summary>

**Solution**:
Find $f^{-1}(x)$:
- $y = 5 - 2x$
- $x = 5 - 2y$
- $2y = 5 - x$
- $y = \frac{5 - x}{2}$

So $f^{-1}(3) = \frac{5 - 3}{2} = \frac{2}{2} = 1$

**Answer: (B)**
</details>

---

**Problem 17**
The function $f(x) = x^3 + 2$ has an inverse. Find $(f^{-1})'(10)$.

<details>
<summary>Show Solution</summary>

**Solution**:
First, find $f^{-1}(x)$:
- $y = x^3 + 2$
- $x = y^3 + 2$
- $y = \sqrt[3]{x - 2}$

So $f^{-1}(x) = (x - 2)^{1/3}$

$$(f^{-1})'(x) = \frac{1}{3}(x - 2)^{-2/3} = \frac{1}{3(x-2)^{2/3}}$$

$$(f^{-1})'(10) = \frac{1}{3(8)^{2/3}} = \frac{1}{3 \cdot 4} = \frac{1}{12}$$

**Answer**: $\dfrac{1}{12}$
</details>

---

**Problem 18**
If $f$ is a one-to-one function with $f(2) = 7$ and $f'(2) = 3$, find $(f^{-1})'(7)$.

<details>
<summary>Show Solution</summary>

**Solution**:
Use the inverse function derivative formula:
$$(f^{-1})'(b) = \frac{1}{f'(f^{-1}(b))}$$

We have $f(2) = 7$, so $f^{-1}(7) = 2$.

$$(f^{-1})'(7) = \frac{1}{f'(f^{-1}(7))} = \frac{1}{f'(2)} = \frac{1}{3}$$

**Answer**: $\dfrac{1}{3}$
</details>

---

**Problem 19** *(Free Response Style)*
Let $f(x) = \dfrac{3x + 1}{x - 2}$ for $x \ne 2$.

(a) Find $f^{-1}(x)$.
(b) Find the domain and range of $f^{-1}$.
(c) Find any fixed points (values where $f(x) = x$).
(d) Verify that any fixed points of $f$ are also fixed points of $f^{-1}$.

<details>
<summary>Show Solution</summary>

**Solution**:

**(a)**
1. $y = \frac{3x + 1}{x - 2}$
2. Swap: $x = \frac{3y + 1}{y - 2}$
3. Solve:
   - $x(y - 2) = 3y + 1$
   - $xy - 2x = 3y + 1$
   - $xy - 3y = 2x + 1$
   - $y(x - 3) = 2x + 1$
   - $y = \frac{2x + 1}{x - 3}$

**$f^{-1}(x) = \dfrac{2x + 1}{x - 3}$**

**(b)**
- Domain of $f^{-1}$ = Range of $f$
- The horizontal asymptote of $f$ is $y = 3$, so range of $f$ is $(-\infty, 3) \cup (3, \infty)$
- **Domain of $f^{-1}$**: $x \ne 3$
- **Range of $f^{-1}$**: $y \ne 2$ (domain of $f$)

**(c)**
Solve $f(x) = x$:
$$\frac{3x + 1}{x - 2} = x$$
$$3x + 1 = x(x - 2) = x^2 - 2x$$
$$x^2 - 5x - 1 = 0$$
$$x = \frac{5 \pm \sqrt{25 + 4}}{2} = \frac{5 \pm \sqrt{29}}{2}$$

**(d)**
Check $f^{-1}(x) = x$ for $x = \frac{5 + \sqrt{29}}{2}$:
$$\frac{2x + 1}{x - 3} = x$$
$$2x + 1 = x(x - 3) = x^2 - 3x$$
$$x^2 - 5x - 1 = 0$$

Same equation! So fixed points of $f$ are also fixed points of $f^{-1}$. ✓
</details>

---

**Problem 20** *(Free Response Style)*
A function $g$ is defined on the interval $[0, 4]$ by the graph shown:
- $(0, 1)$, $(1, 3)$, $(2, 4)$, $(3, 2)$, $(4, 0)$ (piecewise linear connecting these points)

(a) Explain why $g$ has an inverse.
(b) Find $g^{-1}(3)$.
(c) Find the domain and range of $g^{-1}$.
(d) If $g$ is extended so that $g(5) = 1$, does $g$ still have an inverse? Explain.

<details>
<summary>Show Solution</summary>

**Solution**:

**(a)**
The function $g$ passes the horizontal line test (each $y$-value corresponds to exactly one $x$-value in the given points). Looking at the $y$-values: $1, 3, 4, 2, 0$ — all are distinct.

Therefore, $g$ is one-to-one and has an inverse.

**(b)**
$g^{-1}(3)$ asks: for what $x$ does $g(x) = 3$?

From the points, $g(1) = 3$, so $g^{-1}(3) = 1$.

**(c)**
- Domain of $g^{-1}$ = Range of $g$ = $[0, 4]$ (looking at all $y$-values)
- Range of $g^{-1}$ = Domain of $g$ = $[0, 4]$

**(d)**
If $g(5) = 1$, then $g$ would not have an inverse because:
- $g(0) = 1$ and $g(5) = 1$

Two different inputs give the same output, violating the one-to-one property.

**No**, $g$ would no longer have an inverse.
</details>

---

## What's Next

Now that you understand inverse functions, you're ready to explore [Transformations](/calculus/0104-transformations), where we'll learn how shifting, stretching, and reflecting change function graphs—building intuition for how equations relate to visual representations.

---

<div align="center">

[← Composite Functions](/calculus/0102-composite-functions) | [Transformations →](/calculus/0104-transformations)

</div>
