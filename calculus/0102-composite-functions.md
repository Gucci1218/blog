# Composite Functions
<p class="article-date">June 23, 2024</p>

## Prerequisites
Before diving in, make sure you're comfortable with:
- [Domain and Range](/calculus/0101-domain-and-range)
- Function notation and evaluation

## Learning Objectives
By the end of this section, you will be able to:
- Understand function composition as "functions within functions"
- Evaluate composite functions at specific values
- Find formulas for composite functions
- Determine the domain of composite functions
- Decompose complex functions into simpler components
- Recognize composition as preparation for the Chain Rule

## The Big Picture: Functions Within Functions

Imagine you have two machines:
- Machine $f$: Takes a number and doubles it
- Machine $g$: Takes a number and adds 3

**Composition** means connecting these machines: the output of one becomes the input of the other.

$$f(g(x)) = f(x + 3) = 2(x + 3) = 2x + 6$$

> **Notation**: $(f \circ g)(x)$ means $f(g(x))$ — read as "f of g of x" or "f composed with g"

**Key Insight**: Work from the **inside out**. First apply the inner function, then the outer function.

## Why This Matters for Calculus

Composite functions are everywhere in calculus:
- $\sin(x^2)$ is a composition: $\sin(\text{something})$ where something $= x^2$
- $e^{3x}$ is a composition: $e^{\text{something}}$ where something $= 3x$
- $\sqrt{1 + x^2}$ is a composition: $\sqrt{\text{something}}$ where something $= 1 + x^2$

The **Chain Rule** for derivatives is specifically designed for composite functions:
$$\frac{d}{dx}[f(g(x))] = f'(g(x)) \cdot g'(x)$$

## Core Concept: Evaluating Compositions

### Method 1: Substitute and Simplify

**Example**: If $f(x) = x^2$ and $g(x) = x + 3$, find $(f \circ g)(x)$.

**Solution**:
$$(f \circ g)(x) = f(g(x)) = f(x + 3) = (x + 3)^2 = x^2 + 6x + 9$$

### Method 2: Evaluate Step by Step

**Example**: If $f(x) = x^2$ and $g(x) = x + 3$, find $(f \circ g)(2)$.

**Solution**:
Step 1: Find the inner value: $g(2) = 2 + 3 = 5$
Step 2: Apply the outer function: $f(5) = 5^2 = 25$

So $(f \circ g)(2) = 25$

## Order Matters!

**Critical Point**: $f(g(x))$ is generally NOT equal to $g(f(x))$.

**Example**: Let $f(x) = x^2$ and $g(x) = x + 3$

$$f(g(x)) = f(x+3) = (x+3)^2 = x^2 + 6x + 9$$

$$g(f(x)) = g(x^2) = x^2 + 3$$

These are completely different functions!

## Worked Example 1: Finding Composite Functions

**Problem**: Let $f(x) = 2x - 1$ and $g(x) = x^2 + 4$. Find:
a) $(f \circ g)(x)$
b) $(g \circ f)(x)$
c) $(f \circ f)(x)$

**Solution**:

**a)** $(f \circ g)(x) = f(g(x)) = f(x^2 + 4) = 2(x^2 + 4) - 1 = 2x^2 + 8 - 1 = 2x^2 + 7$

**b)** $(g \circ f)(x) = g(f(x)) = g(2x - 1) = (2x-1)^2 + 4 = 4x^2 - 4x + 1 + 4 = 4x^2 - 4x + 5$

**c)** $(f \circ f)(x) = f(f(x)) = f(2x - 1) = 2(2x - 1) - 1 = 4x - 2 - 1 = 4x - 3$

## Worked Example 2: Evaluating at Specific Values

**Problem**: Let $f(x) = \sqrt{x}$ and $g(x) = x + 9$. Evaluate $(f \circ g)(7)$ and $(g \circ f)(16)$.

**Solution**:

**$(f \circ g)(7)$**:
- First: $g(7) = 7 + 9 = 16$
- Then: $f(16) = \sqrt{16} = 4$

**$(g \circ f)(16)$**:
- First: $f(16) = \sqrt{16} = 4$
- Then: $g(4) = 4 + 9 = 13$

## Worked Example 3: Using Tables

**Problem**: Use the tables to find $(f \circ g)(3)$ and $(g \circ f)(1)$.

| $x$ | $f(x)$ |
|-----|--------|
| 1 | 4 |
| 2 | 7 |
| 3 | 2 |
| 4 | 5 |

| $x$ | $g(x)$ |
|-----|--------|
| 1 | 3 |
| 2 | 1 |
| 3 | 4 |
| 4 | 2 |

**Solution**:

**$(f \circ g)(3)$**:
- First: $g(3) = 4$ (from g table)
- Then: $f(4) = 5$ (from f table)
- Answer: $(f \circ g)(3) = 5$

**$(g \circ f)(1)$**:
- First: $f(1) = 4$ (from f table)
- Then: $g(4) = 2$ (from g table)
- Answer: $(g \circ f)(1) = 2$

## Domain of Composite Functions

The domain of $f(g(x))$ must satisfy TWO conditions:
1. $x$ must be in the domain of $g$ (so $g(x)$ exists)
2. $g(x)$ must be in the domain of $f$ (so $f(g(x))$ exists)

### Worked Example 4: Finding Domain of Composition

**Problem**: Let $f(x) = \sqrt{x}$ and $g(x) = x - 4$. Find the domain of $(f \circ g)(x)$.

**Solution**:

**Step 1**: Find $(f \circ g)(x)$:
$$(f \circ g)(x) = f(g(x)) = f(x - 4) = \sqrt{x - 4}$$

**Step 2**: Apply domain restrictions.
- Domain of $g$: all real numbers (no restriction)
- For $f$: need input $\ge 0$, so $g(x) \ge 0 \implies x - 4 \ge 0 \implies x \ge 4$

**Domain**: $[4, \infty)$

### Worked Example 5: More Complex Domain

**Problem**: Let $f(x) = \dfrac{1}{x}$ and $g(x) = x^2 - 9$. Find the domain of $(f \circ g)(x)$.

**Solution**:

**Step 1**: Find $(f \circ g)(x)$:
$$(f \circ g)(x) = f(g(x)) = f(x^2 - 9) = \frac{1}{x^2 - 9}$$

**Step 2**: Apply domain restrictions.
- Domain of $g$: all real numbers
- For $f$: need input $\ne 0$, so $g(x) \ne 0 \implies x^2 - 9 \ne 0 \implies x \ne \pm 3$

**Domain**: $(-\infty, -3) \cup (-3, 3) \cup (3, \infty)$

## Decomposing Functions

Sometimes we need to work backwards: break a complex function into simpler parts.

### Worked Example 6: Decomposition

**Problem**: Write $h(x) = (3x + 1)^5$ as a composition $h(x) = f(g(x))$.

**Solution**:

Identify the "inner" and "outer" operations:
- Inner function (what's inside): $g(x) = 3x + 1$
- Outer function (what's applied to it): $f(x) = x^5$

Check: $f(g(x)) = f(3x + 1) = (3x + 1)^5$ ✓

### Common Decomposition Patterns

| Function $h(x)$ | Inner $g(x)$ | Outer $f(x)$ |
|-----------------|--------------|--------------|
| $\sqrt{x^2 + 1}$ | $x^2 + 1$ | $\sqrt{x}$ |
| $\sin(2x)$ | $2x$ | $\sin(x)$ |
| $e^{x^3}$ | $x^3$ | $e^x$ |
| $(x + 5)^{10}$ | $x + 5$ | $x^{10}$ |
| $\ln(x^2 - 4)$ | $x^2 - 4$ | $\ln(x)$ |
| $\dfrac{1}{x - 3}$ | $x - 3$ | $\dfrac{1}{x}$ |

## Key Formulas

| Notation | Meaning |
|----------|---------|
| $(f \circ g)(x)$ | $f(g(x))$ — apply $g$ first, then $f$ |
| $(g \circ f)(x)$ | $g(f(x))$ — apply $f$ first, then $g$ |
| $(f \circ f)(x)$ | $f(f(x))$ — apply $f$ twice |

**Domain Rule**:
$$\text{Domain of } f \circ g = \{x : x \in \text{dom}(g) \text{ and } g(x) \in \text{dom}(f)\}$$

## Common Mistakes to Avoid

1. **Wrong order of operations**
   - $(f \circ g)(x) = f(g(x))$, NOT $g(f(x))$
   - Work inside out!

2. **Assuming composition is commutative**
   - $f(g(x)) \ne g(f(x))$ in general
   - Always check both orders if asked

3. **Forgetting domain restrictions from the inner function**
   - Even if $f(g(x))$ simplifies nicely, check what $g(x)$ requires

4. **Incorrect substitution**
   - Replace EVERY $x$ in the outer function with the entire inner function
   - $f(x) = x^2 - 3x$ and $g(x) = 2x + 1$
   - $f(g(x)) = (2x+1)^2 - 3(2x+1)$, not $(2x+1)^2 - 3x$

5. **Confusing composition with multiplication**
   - $(f \circ g)(x) = f(g(x))$, NOT $f(x) \cdot g(x)$

## Calculus Connection

Understanding composition is essential for:

1. **Chain Rule**: $\frac{d}{dx}[f(g(x))] = f'(g(x)) \cdot g'(x)$

2. **u-Substitution**: Let $u = g(x)$, then $\int f(g(x)) \cdot g'(x) \, dx = \int f(u) \, du$

3. **Recognizing structure**: Seeing $(2x+1)^5$ as a composition helps you differentiate it correctly

---

## Practice Problems

### Basic (Computational)

**Problem 1**
If $f(x) = 3x + 2$ and $g(x) = x^2$, find $(f \circ g)(x)$.

<details>
<summary>Show Solution</summary>

**Solution**:
$$(f \circ g)(x) = f(g(x)) = f(x^2) = 3(x^2) + 2 = 3x^2 + 2$$
</details>

---

**Problem 2**
If $f(x) = 3x + 2$ and $g(x) = x^2$, find $(g \circ f)(x)$.

<details>
<summary>Show Solution</summary>

**Solution**:
$$(g \circ f)(x) = g(f(x)) = g(3x + 2) = (3x + 2)^2 = 9x^2 + 12x + 4$$
</details>

---

**Problem 3**
If $f(x) = x - 5$ and $g(x) = 2x + 1$, evaluate $(f \circ g)(4)$.

<details>
<summary>Show Solution</summary>

**Solution**:
- First: $g(4) = 2(4) + 1 = 9$
- Then: $f(9) = 9 - 5 = 4$

$(f \circ g)(4) = 4$
</details>

---

**Problem 4**
If $h(x) = \sqrt{x}$ and $k(x) = x + 16$, find $(h \circ k)(x)$.

<details>
<summary>Show Solution</summary>

**Solution**:
$$(h \circ k)(x) = h(k(x)) = h(x + 16) = \sqrt{x + 16}$$
</details>

---

**Problem 5**
If $f(x) = x^2 - 1$, find $(f \circ f)(x)$.

<details>
<summary>Show Solution</summary>

**Solution**:
$$(f \circ f)(x) = f(f(x)) = f(x^2 - 1) = (x^2 - 1)^2 - 1$$
$$= x^4 - 2x^2 + 1 - 1 = x^4 - 2x^2$$
</details>

---

### Intermediate (Multi-step)

**Problem 6**
If $f(x) = \dfrac{1}{x}$ and $g(x) = x + 2$, find $(f \circ g)(x)$ and its domain.

<details>
<summary>Show Solution</summary>

**Solution**:
$$(f \circ g)(x) = f(g(x)) = f(x + 2) = \frac{1}{x + 2}$$

Domain restrictions:
- $g(x)$: all real numbers
- $f$: needs input $\ne 0$, so $x + 2 \ne 0 \implies x \ne -2$

**Domain**: $(-\infty, -2) \cup (-2, \infty)$
</details>

---

**Problem 7**
If $f(x) = \sqrt{x}$ and $g(x) = 4 - x^2$, find the domain of $(f \circ g)(x)$.

<details>
<summary>Show Solution</summary>

**Solution**:
$(f \circ g)(x) = f(g(x)) = \sqrt{4 - x^2}$

For the square root: $4 - x^2 \ge 0$
$$x^2 \le 4$$
$$-2 \le x \le 2$$

**Domain**: $[-2, 2]$
</details>

---

**Problem 8**
Write $h(x) = \sin(x^2 + 1)$ as a composition of two functions.

<details>
<summary>Show Solution</summary>

**Solution**:
- Inner function: $g(x) = x^2 + 1$
- Outer function: $f(x) = \sin(x)$

Check: $f(g(x)) = \sin(x^2 + 1) = h(x)$ ✓

**Answer**: $f(x) = \sin(x)$ and $g(x) = x^2 + 1$
</details>

---

**Problem 9**
Use the tables to find $(f \circ g)(2)$ and $(g \circ g)(1)$.

| $x$ | 1 | 2 | 3 | 4 |
|-----|---|---|---|---|
| $f(x)$ | 2 | 4 | 1 | 3 |
| $g(x)$ | 3 | 1 | 4 | 2 |

<details>
<summary>Show Solution</summary>

**Solution**:

**$(f \circ g)(2)$**:
- $g(2) = 1$
- $f(1) = 2$
- Answer: $(f \circ g)(2) = 2$

**$(g \circ g)(1)$**:
- $g(1) = 3$
- $g(3) = 4$
- Answer: $(g \circ g)(1) = 4$
</details>

---

**Problem 10**
If $f(x) = x^2 + 3x$ and $g(x) = x - 1$, find $(f \circ g)(x)$ and simplify.

<details>
<summary>Show Solution</summary>

**Solution**:
$$(f \circ g)(x) = f(g(x)) = f(x - 1)$$
$$= (x-1)^2 + 3(x-1)$$
$$= x^2 - 2x + 1 + 3x - 3$$
$$= x^2 + x - 2$$
</details>

---

### Advanced (Complex Applications)

**Problem 11**
If $f(x) = \dfrac{x}{x - 1}$ and $g(x) = \dfrac{1}{x}$, find $(f \circ g)(x)$ and its domain.

<details>
<summary>Show Solution</summary>

**Solution**:
$$(f \circ g)(x) = f\left(\frac{1}{x}\right) = \frac{\frac{1}{x}}{\frac{1}{x} - 1} = \frac{\frac{1}{x}}{\frac{1-x}{x}} = \frac{1}{x} \cdot \frac{x}{1-x} = \frac{1}{1-x}$$

Domain restrictions:
- $g(x)$: $x \ne 0$
- $f$: input $\ne 1$, so $\frac{1}{x} \ne 1 \implies x \ne 1$

**Domain**: $(-\infty, 0) \cup (0, 1) \cup (1, \infty)$
</details>

---

**Problem 12**
Find functions $f$ and $g$ such that $(f \circ g)(x) = \dfrac{1}{(x + 3)^2}$.

<details>
<summary>Show Solution</summary>

**Solution**:
Several answers are possible. One decomposition:

- Inner: $g(x) = x + 3$
- Outer: $f(x) = \dfrac{1}{x^2}$

Check: $f(g(x)) = f(x + 3) = \dfrac{1}{(x+3)^2}$ ✓

Alternative:
- Inner: $g(x) = (x + 3)^2$
- Outer: $f(x) = \dfrac{1}{x}$
</details>

---

**Problem 13**
If $f(x) = 2x + 3$, find a function $g(x)$ such that $(f \circ g)(x) = x$ (i.e., $g$ is the inverse of $f$).

<details>
<summary>Show Solution</summary>

**Solution**:
We need $f(g(x)) = x$:
$$2 \cdot g(x) + 3 = x$$
$$2 \cdot g(x) = x - 3$$
$$g(x) = \frac{x - 3}{2}$$

Verify: $f(g(x)) = f\left(\frac{x-3}{2}\right) = 2 \cdot \frac{x-3}{2} + 3 = x - 3 + 3 = x$ ✓
</details>

---

**Problem 14**
If $f(x) = \sqrt{x - 1}$ and $g(x) = x^2 + 1$, find the domain of $(f \circ g)(x)$ and $(g \circ f)(x)$.

<details>
<summary>Show Solution</summary>

**Solution**:

**Domain of $(f \circ g)(x)$**:
$(f \circ g)(x) = f(x^2 + 1) = \sqrt{x^2 + 1 - 1} = \sqrt{x^2} = |x|$

Need: $x^2 + 1 - 1 \ge 0 \implies x^2 \ge 0$ (always true)

Domain: $(-\infty, \infty)$

**Domain of $(g \circ f)(x)$**:
$(g \circ f)(x) = g(\sqrt{x-1}) = (\sqrt{x-1})^2 + 1 = x - 1 + 1 = x$

Need: $x - 1 \ge 0$ (for the square root in $f$)

Domain: $[1, \infty)$
</details>

---

**Problem 15**
Let $f(x) = x^2$ and $g(x) = \sqrt{x}$. Show that $(f \circ g)(x) = x$ for $x \ge 0$, but $(g \circ f)(x) = |x|$ for all $x$.

<details>
<summary>Show Solution</summary>

**Solution**:

**$(f \circ g)(x)$** for $x \ge 0$:
$$f(g(x)) = f(\sqrt{x}) = (\sqrt{x})^2 = x$$

**$(g \circ f)(x)$** for all $x$:
$$g(f(x)) = g(x^2) = \sqrt{x^2} = |x|$$

The difference arises because:
- In $f \circ g$: we first take $\sqrt{x}$ (requires $x \ge 0$), then square it back
- In $g \circ f$: we first square (any $x$), then take square root (which gives the positive root)

For negative $x$: $(g \circ f)(-3) = \sqrt{9} = 3 = |-3|$
</details>

---

### AP Exam Style

**Problem 16**
If $f(x) = x^3$ and $g(x) = x - 2$, then $(f \circ g)(x) - (g \circ f)(x) = $

(A) $-6x^2 + 12x - 6$
(B) $6x^2 - 12x + 6$
(C) $-2$
(D) $6$

<details>
<summary>Show Solution</summary>

**Solution**:
$(f \circ g)(x) = f(x - 2) = (x - 2)^3 = x^3 - 6x^2 + 12x - 8$

$(g \circ f)(x) = g(x^3) = x^3 - 2$

Difference:
$$(x^3 - 6x^2 + 12x - 8) - (x^3 - 2) = -6x^2 + 12x - 8 + 2 = -6x^2 + 12x - 6$$

**Answer: (A)**
</details>

---

**Problem 17**
The function $h(x) = e^{2x+1}$ can be expressed as $f(g(x))$ where:

(A) $f(x) = e^x$ and $g(x) = 2x + 1$
(B) $f(x) = 2x + 1$ and $g(x) = e^x$
(C) $f(x) = e^{2x}$ and $g(x) = e$
(D) $f(x) = x + 1$ and $g(x) = e^{2x}$

<details>
<summary>Show Solution</summary>

**Solution**:
Test option (A): $f(g(x)) = e^{2x+1}$ ✓

**Answer: (A)**
</details>

---

**Problem 18**
If $f(x) = \sqrt{x + 4}$ and $g(x) = x^2 - 5$, what is the domain of $f \circ g$?

<details>
<summary>Show Solution</summary>

**Solution**:
$(f \circ g)(x) = f(x^2 - 5) = \sqrt{x^2 - 5 + 4} = \sqrt{x^2 - 1}$

Need: $x^2 - 1 \ge 0$
$(x-1)(x+1) \ge 0$

This is satisfied when $x \le -1$ or $x \ge 1$.

**Domain**: $(-\infty, -1] \cup [1, \infty)$
</details>

---

**Problem 19** *(Free Response Style)*
Let $f$ and $g$ be functions defined by $f(x) = \dfrac{2}{x+1}$ and $g(x) = 3x - 5$.

(a) Find $(g \circ f)(x)$ and simplify.
(b) Find the domain of $(g \circ f)(x)$.
(c) Find $(f \circ g)(x)$ and simplify.
(d) Solve $(f \circ g)(x) = 1$.

<details>
<summary>Show Solution</summary>

**Solution**:

**(a)**
$$(g \circ f)(x) = g\left(\frac{2}{x+1}\right) = 3 \cdot \frac{2}{x+1} - 5 = \frac{6}{x+1} - 5 = \frac{6 - 5(x+1)}{x+1} = \frac{6 - 5x - 5}{x+1} = \frac{1 - 5x}{x+1}$$

**(b)**
Domain restriction from $f$: $x + 1 \ne 0 \implies x \ne -1$

**Domain**: $(-\infty, -1) \cup (-1, \infty)$

**(c)**
$$(f \circ g)(x) = f(3x - 5) = \frac{2}{(3x-5)+1} = \frac{2}{3x - 4}$$

**(d)**
$$\frac{2}{3x - 4} = 1$$
$$2 = 3x - 4$$
$$6 = 3x$$
$$x = 2$$
</details>

---

**Problem 20** *(Free Response Style)*
The graph of $y = g(x)$ passes through the points $(1, 4)$, $(2, 3)$, $(3, 5)$, and $(4, 1)$.

(a) If $f(x) = x^2 - 2x$, find $(f \circ g)(3)$.
(b) If $h(x) = 2x - 1$, find $(g \circ h)(2)$ if it exists.
(c) Find all values of $x$ in the domain of $g$ such that $(g \circ g)(x)$ can be evaluated.

<details>
<summary>Show Solution</summary>

**Solution**:

**(a)**
- $g(3) = 5$ (from the given point)
- $f(5) = 5^2 - 2(5) = 25 - 10 = 15$

$(f \circ g)(3) = 15$

**(b)**
- $h(2) = 2(2) - 1 = 3$
- $g(3) = 5$ (from the given point)

$(g \circ h)(2) = 5$

**(c)**
For $(g \circ g)(x)$, we need:
1. $x$ in domain of $g$: $x \in \{1, 2, 3, 4\}$
2. $g(x)$ in domain of $g$: $g(x) \in \{1, 2, 3, 4\}$

Check each:
- $g(1) = 4$ ✓ (4 is in domain)
- $g(2) = 3$ ✓ (3 is in domain)
- $g(3) = 5$ ✗ (5 is not in domain)
- $g(4) = 1$ ✓ (1 is in domain)

**Answer**: $x \in \{1, 2, 4\}$
</details>

---

## What's Next

Now that you understand composite functions, you're ready to explore [Inverse Functions](/calculus/0103-inverse-functions), where we'll learn how to "undo" a function—a concept closely related to composition since $f(f^{-1}(x)) = x$.

---

<div align="center">

[← Domain and Range](/calculus/0101-domain-and-range) | [Inverse Functions →](/calculus/0103-inverse-functions)

</div>
