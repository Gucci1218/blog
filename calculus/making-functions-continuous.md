# Making Functions Continuous

## Learning Objectives

By the end of this article, you will be able to:

- Identify removable discontinuities that can be "fixed"
- Find the value needed to make a function continuous at a point
- Extend functions continuously by defining missing values
- Solve for constants in piecewise functions to ensure continuity
- Handle multiple constants with systems of equations
- Recognize when a discontinuity cannot be removed
- Master AP Calculus problems on continuous extensions

---

## The Core Concept: Filling in the Holes

### The Intuition

Imagine a bridge with a small gap in it. If the gap is small enough and the two sides line up perfectly, you could place a single board across to complete the bridge. But if the two sides are at different heights or the gap is infinitely wide, no single board would work.

**Removable discontinuities** are like small gaps where the sides line up—we can fill them with a single point. **Jump and infinite discontinuities** are like misaligned sides or infinite gaps—they can't be fixed with a simple patch.

### What Does "Making Continuous" Mean?

When we "make a function continuous" at a point $x = a$, we:

1. Find the limit $L = \lim_{x \to a} f(x)$
2. Define (or redefine) $f(a) = L$

This works **only if the limit exists**. If the limit doesn't exist (jump or infinite discontinuity), we cannot make the function continuous by changing just one value.

### The Key Formula

To make $f$ continuous at $x = a$:

$$\boxed{f(a) = \lim_{x \to a} f(x)}$$

This is both the **condition** for continuity and the **solution** for how to achieve it.

---

## Type 1: Removing Holes in Rational Functions

### The Classic Setup

Many rational functions have "holes" where both numerator and denominator equal zero. These create removable discontinuities.

### Example 1: Basic Hole Removal

**Problem:** Define $f(2)$ to make $f(x) = \frac{x^2 - 4}{x - 2}$ continuous at $x = 2$.

**Solution:**

**Step 1: Find the limit**

Factor and simplify:
$$\lim_{x \to 2} \frac{x^2 - 4}{x - 2} = \lim_{x \to 2} \frac{(x-2)(x+2)}{x-2} = \lim_{x \to 2} (x + 2) = 4$$

**Step 2: Define the value**

For continuity, we need $f(2) = \lim_{x \to 2} f(x) = 4$.

**Answer:** Define $f(2) = 4$.

**The continuous version:**
$$f(x) = \begin{cases} \frac{x^2 - 4}{x - 2} & \text{if } x \neq 2 \\ 4 & \text{if } x = 2 \end{cases}$$

Or simply: $f(x) = x + 2$ for all $x$.

---

### Example 2: Cubic Over Linear

**Problem:** Find the value of $f(3)$ that makes $f(x) = \frac{x^3 - 27}{x - 3}$ continuous at $x = 3$.

**Solution:**

Recall the factoring formula: $a^3 - b^3 = (a-b)(a^2 + ab + b^2)$

$$x^3 - 27 = (x - 3)(x^2 + 3x + 9)$$

$$\lim_{x \to 3} \frac{(x-3)(x^2 + 3x + 9)}{x - 3} = \lim_{x \to 3} (x^2 + 3x + 9) = 9 + 9 + 9 = 27$$

**Answer:** $f(3) = 27$

---

### Example 3: Higher Multiplicity

**Problem:** Make $g(x) = \frac{x^2 - 6x + 9}{x - 3}$ continuous at $x = 3$.

**Solution:**

Factor the numerator:
$$x^2 - 6x + 9 = (x - 3)^2$$

$$\lim_{x \to 3} \frac{(x-3)^2}{x - 3} = \lim_{x \to 3} (x - 3) = 0$$

**Answer:** $g(3) = 0$

---

## Type 2: Trigonometric Functions with Indeterminate Forms

### Key Limits to Remember

$$\lim_{x \to 0} \frac{\sin x}{x} = 1 \qquad \lim_{x \to 0} \frac{1 - \cos x}{x} = 0 \qquad \lim_{x \to 0} \frac{1 - \cos x}{x^2} = \frac{1}{2}$$

### Example 4: The Sinc Function

**Problem:** Find $f(0)$ to make $f(x) = \frac{\sin x}{x}$ continuous at $x = 0$.

**Solution:**

$$\lim_{x \to 0} \frac{\sin x}{x} = 1$$

**Answer:** $f(0) = 1$

This is the famous **sinc function**, used extensively in signal processing:
$$\text{sinc}(x) = \begin{cases} \frac{\sin x}{x} & \text{if } x \neq 0 \\ 1 & \text{if } x = 0 \end{cases}$$

---

### Example 5: Tangent Over x

**Problem:** Make $g(x) = \frac{\tan x}{x}$ continuous at $x = 0$.

**Solution:**

$$\lim_{x \to 0} \frac{\tan x}{x} = \lim_{x \to 0} \frac{\sin x}{x \cos x} = \lim_{x \to 0} \frac{\sin x}{x} \cdot \frac{1}{\cos x} = 1 \cdot 1 = 1$$

**Answer:** $g(0) = 1$

---

### Example 6: Modified Sine Limit

**Problem:** Find $f(0)$ to make $f(x) = \frac{\sin 3x}{x}$ continuous at $x = 0$.

**Solution:**

Multiply and divide by 3:
$$\lim_{x \to 0} \frac{\sin 3x}{x} = \lim_{x \to 0} \frac{\sin 3x}{3x} \cdot 3 = 1 \cdot 3 = 3$$

**Answer:** $f(0) = 3$

**General pattern:** $\lim_{x \to 0} \frac{\sin(ax)}{x} = a$

---

### Example 7: Cosine Variation

**Problem:** Make $h(x) = \frac{1 - \cos x}{x^2}$ continuous at $x = 0$.

**Solution:**

Using the known limit:
$$\lim_{x \to 0} \frac{1 - \cos x}{x^2} = \frac{1}{2}$$

**Answer:** $h(0) = \frac{1}{2}$

---

## Type 3: Exponential and Logarithmic Functions

### Key Limit

$$\lim_{x \to 0} \frac{e^x - 1}{x} = 1$$

### Example 8: Exponential Hole

**Problem:** Find $f(0)$ to make $f(x) = \frac{e^x - 1}{x}$ continuous at $x = 0$.

**Solution:**

$$\lim_{x \to 0} \frac{e^x - 1}{x} = 1$$

**Answer:** $f(0) = 1$

---

### Example 9: Modified Exponential

**Problem:** Make $g(x) = \frac{e^{2x} - 1}{x}$ continuous at $x = 0$.

**Solution:**

Let $u = 2x$, so as $x \to 0$, $u \to 0$:
$$\lim_{x \to 0} \frac{e^{2x} - 1}{x} = \lim_{x \to 0} \frac{e^{2x} - 1}{2x} \cdot 2 = 1 \cdot 2 = 2$$

**Answer:** $g(0) = 2$

**General pattern:** $\lim_{x \to 0} \frac{e^{ax} - 1}{x} = a$

---

### Example 10: Logarithmic Function

**Problem:** Make $f(x) = \frac{\ln(1 + x)}{x}$ continuous at $x = 0$.

**Solution:**

This is a standard limit:
$$\lim_{x \to 0} \frac{\ln(1 + x)}{x} = 1$$

**Answer:** $f(0) = 1$

---

## Type 4: Radical Functions (Rationalization)

### Example 11: Square Root Difference

**Problem:** Find $f(4)$ to make $f(x) = \frac{\sqrt{x} - 2}{x - 4}$ continuous at $x = 4$.

**Solution:**

Rationalize the numerator:
$$\frac{\sqrt{x} - 2}{x - 4} \cdot \frac{\sqrt{x} + 2}{\sqrt{x} + 2} = \frac{x - 4}{(x - 4)(\sqrt{x} + 2)} = \frac{1}{\sqrt{x} + 2}$$

$$\lim_{x \to 4} \frac{1}{\sqrt{x} + 2} = \frac{1}{2 + 2} = \frac{1}{4}$$

**Answer:** $f(4) = \frac{1}{4}$

---

### Example 12: Difference of Square Roots

**Problem:** Make $g(x) = \frac{\sqrt{x + 5} - 3}{x - 4}$ continuous at $x = 4$.

**Solution:**

Rationalize:
$$\frac{\sqrt{x + 5} - 3}{x - 4} \cdot \frac{\sqrt{x + 5} + 3}{\sqrt{x + 5} + 3} = \frac{(x + 5) - 9}{(x - 4)(\sqrt{x + 5} + 3)} = \frac{x - 4}{(x - 4)(\sqrt{x + 5} + 3)}$$

$$= \frac{1}{\sqrt{x + 5} + 3}$$

$$\lim_{x \to 4} \frac{1}{\sqrt{x + 5} + 3} = \frac{1}{\sqrt{9} + 3} = \frac{1}{6}$$

**Answer:** $g(4) = \frac{1}{6}$

---

## Type 5: Piecewise Functions with One Unknown

### Example 13: Linear-Quadratic Junction

**Problem:** Find $k$ so that $f(x) = \begin{cases} x^2 + k & \text{if } x \leq 2 \\ 3x + 1 & \text{if } x > 2 \end{cases}$ is continuous at $x = 2$.

**Solution:**

For continuity, we need:
$$\lim_{x \to 2^-} f(x) = \lim_{x \to 2^+} f(x) = f(2)$$

**Left-hand limit (and function value):**
$$\lim_{x \to 2^-} (x^2 + k) = 4 + k = f(2)$$

**Right-hand limit:**
$$\lim_{x \to 2^+} (3x + 1) = 7$$

**Set equal:**
$$4 + k = 7 \implies k = 3$$

**Answer:** $k = 3$

---

### Example 14: Trigonometric Piecewise

**Problem:** Find $c$ so that $g(x) = \begin{cases} c \sin x & \text{if } x < \frac{\pi}{2} \\ \cos x + c & \text{if } x \geq \frac{\pi}{2} \end{cases}$ is continuous at $x = \frac{\pi}{2}$.

**Solution:**

**Left-hand limit:**
$$\lim_{x \to \frac{\pi}{2}^-} c \sin x = c \cdot 1 = c$$

**Right-hand limit (and function value):**
$$\lim_{x \to \frac{\pi}{2}^+} (\cos x + c) = 0 + c = c$$

Both limits equal $c$, and $g\left(\frac{\pi}{2}\right) = 0 + c = c$.

**The function is continuous for all values of $c$!**

---

### Example 15: Quadratic Coefficient

**Problem:** Find $a$ so that $h(x) = \begin{cases} ax^2 - 3 & \text{if } x < 1 \\ 2x + a & \text{if } x \geq 1 \end{cases}$ is continuous at $x = 1$.

**Solution:**

**Left-hand limit:**
$$\lim_{x \to 1^-} (ax^2 - 3) = a - 3$$

**Right-hand limit (and function value):**
$$\lim_{x \to 1^+} (2x + a) = 2 + a$$

**Set equal:**
$$a - 3 = 2 + a$$
$$-3 = 2$$

**This is impossible!** There is no value of $a$ that makes this function continuous at $x = 1$.

**Answer:** No such value exists.

---

## Type 6: Two or More Unknown Constants

### Example 16: Two Constants, One Boundary

**Problem:** Find $a$ and $b$ so that $f(x) = \begin{cases} ax + b & \text{if } x < 2 \\ x^2 & \text{if } x \geq 2 \end{cases}$ is continuous at $x = 2$ and $f(0) = 3$.

**Solution:**

**Continuity at $x = 2$:**
$$\lim_{x \to 2^-} (ax + b) = 2a + b$$
$$f(2) = 4$$

Equation 1: $2a + b = 4$

**Using $f(0) = 3$:**
$$f(0) = a(0) + b = b = 3$$

Equation 2: $b = 3$

**Solve:**
From Equation 2: $b = 3$
Substitute into Equation 1: $2a + 3 = 4 \implies a = \frac{1}{2}$

**Answer:** $a = \frac{1}{2}$, $b = 3$

---

### Example 17: Two Constants, Two Boundaries

**Problem:** Find $a$ and $b$ so that $g(x) = \begin{cases} 2x + a & \text{if } x < -1 \\ bx^2 + 1 & \text{if } -1 \leq x \leq 2 \\ 3x + b & \text{if } x > 2 \end{cases}$ is continuous everywhere.

**Solution:**

**Continuity at $x = -1$:**

Left: $\lim_{x \to -1^-} (2x + a) = -2 + a$

Right (and value): $g(-1) = b(-1)^2 + 1 = b + 1$

Equation 1: $-2 + a = b + 1 \implies a - b = 3$

**Continuity at $x = 2$:**

Left (and value): $g(2) = b(4) + 1 = 4b + 1$

Right: $\lim_{x \to 2^+} (3x + b) = 6 + b$

Equation 2: $4b + 1 = 6 + b \implies 3b = 5 \implies b = \frac{5}{3}$

**Solve for $a$:**
From Equation 1: $a = b + 3 = \frac{5}{3} + 3 = \frac{14}{3}$

**Answer:** $a = \frac{14}{3}$, $b = \frac{5}{3}$

---

### Example 18: Three Constants

**Problem:** Find $a$, $b$, and $c$ so that $f(x) = \begin{cases} ax^2 + bx + c & \text{if } x \leq 0 \\ e^x & \text{if } 0 < x < 1 \\ ax + b & \text{if } x \geq 1 \end{cases}$ is continuous everywhere, given $f(-1) = 2$.

**Solution:**

**Continuity at $x = 0$:**

Left (and value): $f(0) = c$

Right: $\lim_{x \to 0^+} e^x = 1$

Equation 1: $c = 1$

**Continuity at $x = 1$:**

Left: $\lim_{x \to 1^-} e^x = e$

Right (and value): $f(1) = a + b$

Equation 2: $a + b = e$

**Using $f(-1) = 2$:**
$$a(-1)^2 + b(-1) + c = 2$$
$$a - b + c = 2$$

Equation 3: $a - b + 1 = 2 \implies a - b = 1$

**Solve Equations 2 and 3:**
- $a + b = e$
- $a - b = 1$

Add: $2a = e + 1 \implies a = \frac{e + 1}{2}$

Subtract: $2b = e - 1 \implies b = \frac{e - 1}{2}$

**Answer:** $a = \frac{e + 1}{2}$, $b = \frac{e - 1}{2}$, $c = 1$

---

## Type 7: When Continuity Is Impossible

Not every discontinuity can be removed. Here's how to recognize unfixable cases.

### Jump Discontinuities

If the one-sided limits exist but are different, no single value can make the function continuous.

**Example:** $f(x) = \frac{|x|}{x}$ at $x = 0$

- $\lim_{x \to 0^-} = -1$
- $\lim_{x \to 0^+} = 1$

No value of $f(0)$ can equal both $-1$ and $1$.

### Infinite Discontinuities

If the limit is infinite, we can't define a real number value.

**Example:** $f(x) = \frac{1}{x}$ at $x = 0$

- $\lim_{x \to 0^+} = +\infty$
- $\lim_{x \to 0^-} = -\infty$

No real number works.

### Oscillating Discontinuities

If the function oscillates infinitely near the point, no limit exists.

**Example:** $f(x) = \sin\left(\frac{1}{x}\right)$ at $x = 0$

The function oscillates between $-1$ and $1$ infinitely often near $x = 0$.

---

## Worked Examples: Mixed Practice

### Example 19: Compound Fraction

**Problem:** Make $f(x) = \frac{\frac{1}{x} - \frac{1}{3}}{x - 3}$ continuous at $x = 3$.

**Solution:**

Simplify the numerator:
$$\frac{1}{x} - \frac{1}{3} = \frac{3 - x}{3x}$$

So:
$$f(x) = \frac{\frac{3-x}{3x}}{x - 3} = \frac{3-x}{3x(x-3)} = \frac{-(x-3)}{3x(x-3)} = \frac{-1}{3x}$$

$$\lim_{x \to 3} \frac{-1}{3x} = \frac{-1}{9}$$

**Answer:** $f(3) = -\frac{1}{9}$

---

### Example 20: Difference Quotient Form

**Problem:** Make $g(x) = \frac{(2+x)^3 - 8}{x}$ continuous at $x = 0$.

**Solution:**

This looks like a derivative! Let $h(t) = t^3$, then:
$$\frac{(2+x)^3 - 8}{x} = \frac{h(2+x) - h(2)}{x}$$

This is the difference quotient for $h$ at $t = 2$.

$$\lim_{x \to 0} \frac{(2+x)^3 - 8}{x} = h'(2) = 3(2)^2 = 12$$

**Alternative:** Expand $(2+x)^3 = 8 + 12x + 6x^2 + x^3$

$$\frac{8 + 12x + 6x^2 + x^3 - 8}{x} = \frac{12x + 6x^2 + x^3}{x} = 12 + 6x + x^2$$

$$\lim_{x \to 0} (12 + 6x + x^2) = 12$$

**Answer:** $g(0) = 12$

---

### Example 21: Nested Radicals

**Problem:** Make $f(x) = \frac{\sqrt{1 + x} - 1}{x}$ continuous at $x = 0$.

**Solution:**

Rationalize:
$$\frac{\sqrt{1+x} - 1}{x} \cdot \frac{\sqrt{1+x} + 1}{\sqrt{1+x} + 1} = \frac{(1+x) - 1}{x(\sqrt{1+x} + 1)} = \frac{x}{x(\sqrt{1+x} + 1)} = \frac{1}{\sqrt{1+x} + 1}$$

$$\lim_{x \to 0} \frac{1}{\sqrt{1+x} + 1} = \frac{1}{1 + 1} = \frac{1}{2}$$

**Answer:** $f(0) = \frac{1}{2}$

---

### Example 22: Product of Two Problematic Terms

**Problem:** Make $h(x) = x^2 \cdot \frac{\sin x}{x}$ continuous at $x = 0$.

**Solution:**

$$\lim_{x \to 0} x^2 \cdot \frac{\sin x}{x} = \lim_{x \to 0} x^2 \cdot \lim_{x \to 0} \frac{\sin x}{x} = 0 \cdot 1 = 0$$

Wait, let's be more careful. As $x \to 0$:

$$x^2 \cdot \frac{\sin x}{x} = x \cdot \sin x$$

$$\lim_{x \to 0} x \sin x = 0 \cdot 0 = 0$$

**Answer:** $h(0) = 0$

---

## Practice Problems

### Basic Problems (1-5)

**1.** Find $f(1)$ to make $f(x) = \frac{x^2 - 1}{x - 1}$ continuous at $x = 1$.

---

**2.** Find $g(0)$ to make $g(x) = \frac{\sin 5x}{x}$ continuous at $x = 0$.

---

**3.** Find $h(-2)$ to make $h(x) = \frac{x^2 + 5x + 6}{x + 2}$ continuous at $x = -2$.

---

**4.** Find $k$ so that $f(x) = \begin{cases} 2x + k & \text{if } x < 1 \\ x^2 + 3 & \text{if } x \geq 1 \end{cases}$ is continuous at $x = 1$.

---

**5.** Find $f(0)$ to make $f(x) = \frac{e^{3x} - 1}{x}$ continuous at $x = 0$.

---

### Intermediate Problems (6-10)

**6.** Find $f(9)$ to make $f(x) = \frac{x - 9}{\sqrt{x} - 3}$ continuous at $x = 9$.

---

**7.** Find $a$ and $b$ so that $g(x) = \begin{cases} ax + b & \text{if } x < 3 \\ 2x^2 - 9 & \text{if } x \geq 3 \end{cases}$ is continuous at $x = 3$ and $g(1) = 5$.

---

**8.** Find $g(0)$ to make $g(x) = \frac{1 - \cos 2x}{x}$ continuous at $x = 0$.

---

**9.** Find $c$ so that $h(x) = \begin{cases} \frac{x^2 - 4}{x - 2} & \text{if } x \neq 2 \\ c & \text{if } x = 2 \end{cases}$ is continuous at $x = 2$.

---

**10.** Find $a$ and $b$ so that $f(x) = \begin{cases} x + a & \text{if } x < -1 \\ bx^2 & \text{if } -1 \leq x \leq 1 \\ x + a & \text{if } x > 1 \end{cases}$ is continuous everywhere.

---

### Advanced Problems (11-15)

**11.** Find $f(0)$ to make $f(x) = \frac{\tan 2x}{\sin 3x}$ continuous at $x = 0$.

---

**12.** Find $a$, $b$, and $c$ so that $g(x) = \begin{cases} ax + b & \text{if } x \leq -1 \\ x^2 + c & \text{if } -1 < x < 2 \\ bx + a & \text{if } x \geq 2 \end{cases}$ is continuous everywhere and $g(0) = 1$.

---

**13.** Find $f(2)$ to make $f(x) = \frac{x^4 - 16}{x^3 - 8}$ continuous at $x = 2$.

---

**14.** Find all values of $k$ for which $h(x) = \begin{cases} kx + 1 & \text{if } x \leq k \\ x^2 & \text{if } x > k \end{cases}$ is continuous at $x = k$.

---

**15.** Find $f(0)$ to make $f(x) = \frac{\sqrt{1 + \sin x} - \sqrt{1 - \sin x}}{x}$ continuous at $x = 0$.

---

### Challenge Problems (16-18)

**16.** Find $f(0)$ to make $f(x) = \left(\frac{\sin x}{x}\right)^{\frac{1}{x^2}}$ continuous at $x = 0$.

*(Hint: Take the natural log and use L'Hôpital's Rule or known limits.)*

---

**17.** Find values of $a$ and $b$ such that $g(x) = \begin{cases} \frac{\sin ax}{x} & \text{if } x < 0 \\ b & \text{if } x = 0 \\ \frac{e^{bx} - 1}{x} & \text{if } x > 0 \end{cases}$ is continuous at $x = 0$ and the common limit equals 2.

---

**18.** Define $h(x) = \frac{x^n - a^n}{x - a}$ where $n$ is a positive integer. Find $h(a)$ to make $h$ continuous at $x = a$, and express your answer in terms of $n$ and $a$.

---

## Solutions to Practice Problems

### Solution 1

$$\lim_{x \to 1} \frac{x^2 - 1}{x - 1} = \lim_{x \to 1} \frac{(x-1)(x+1)}{x-1} = \lim_{x \to 1} (x + 1) = 2$$

**Answer:** $f(1) = 2$

---

### Solution 2

$$\lim_{x \to 0} \frac{\sin 5x}{x} = \lim_{x \to 0} \frac{\sin 5x}{5x} \cdot 5 = 1 \cdot 5 = 5$$

**Answer:** $g(0) = 5$

---

### Solution 3

$$h(x) = \frac{x^2 + 5x + 6}{x + 2} = \frac{(x+2)(x+3)}{x+2} = x + 3 \quad (x \neq -2)$$

$$\lim_{x \to -2} (x + 3) = 1$$

**Answer:** $h(-2) = 1$

---

### Solution 4

Left limit: $\lim_{x \to 1^-} (2x + k) = 2 + k$

Right limit (and value): $f(1) = 1 + 3 = 4$

Set equal: $2 + k = 4 \implies k = 2$

**Answer:** $k = 2$

---

### Solution 5

$$\lim_{x \to 0} \frac{e^{3x} - 1}{x} = \lim_{x \to 0} \frac{e^{3x} - 1}{3x} \cdot 3 = 1 \cdot 3 = 3$$

**Answer:** $f(0) = 3$

---

### Solution 6

Rationalize the denominator:
$$\frac{x - 9}{\sqrt{x} - 3} \cdot \frac{\sqrt{x} + 3}{\sqrt{x} + 3} = \frac{(x-9)(\sqrt{x} + 3)}{x - 9} = \sqrt{x} + 3$$

$$\lim_{x \to 9} (\sqrt{x} + 3) = 3 + 3 = 6$$

**Answer:** $f(9) = 6$

---

### Solution 7

**Continuity at $x = 3$:**

Left: $3a + b$

Right (and value): $g(3) = 18 - 9 = 9$

Equation 1: $3a + b = 9$

**Using $g(1) = 5$:**

$g(1) = a(1) + b = a + b = 5$

Equation 2: $a + b = 5$

**Solve:**

Subtract: $2a = 4 \implies a = 2$

Then: $b = 5 - 2 = 3$

**Answer:** $a = 2$, $b = 3$

---

### Solution 8

$$\lim_{x \to 0} \frac{1 - \cos 2x}{x}$$

Using the identity $1 - \cos 2x = 2\sin^2 x$:

$$= \lim_{x \to 0} \frac{2\sin^2 x}{x} = \lim_{x \to 0} 2 \sin x \cdot \frac{\sin x}{x} = 2 \cdot 0 \cdot 1 = 0$$

**Answer:** $g(0) = 0$

---

### Solution 9

$$\lim_{x \to 2} \frac{x^2 - 4}{x - 2} = \lim_{x \to 2} (x + 2) = 4$$

**Answer:** $c = 4$

---

### Solution 10

**At $x = -1$:**

Left: $-1 + a$

Right (and value): $b(-1)^2 = b$

Equation 1: $a - 1 = b$

**At $x = 1$:**

Left (and value): $b(1)^2 = b$

Right: $1 + a$

Equation 2: $b = 1 + a$

From both equations: $a - 1 = b$ and $b = 1 + a$

Substitute: $a - 1 = 1 + a \implies -1 = 1$ (Contradiction!)

**Wait**, let me recheck. The function uses $x + a$ for both $x < -1$ and $x > 1$.

At $x = 1$: Left is $b(1)^2 = b$, Right is $1 + a$.

So: $b = 1 + a$ ... (Equation 2)

At $x = -1$: Left is $-1 + a$, Right (value) is $b$.

So: $-1 + a = b$ ... (Equation 1)

From (1): $a - 1 = b$
From (2): $a + 1 = b$

These give $a - 1 = a + 1$, which is impossible.

**Answer:** No values of $a$ and $b$ make this function continuous everywhere.

---

### Solution 11

$$\lim_{x \to 0} \frac{\tan 2x}{\sin 3x} = \lim_{x \to 0} \frac{\frac{\sin 2x}{\cos 2x}}{\sin 3x}$$

$$= \lim_{x \to 0} \frac{\sin 2x}{\sin 3x \cdot \cos 2x}$$

$$= \lim_{x \to 0} \frac{\sin 2x}{2x} \cdot \frac{3x}{\sin 3x} \cdot \frac{2x}{3x} \cdot \frac{1}{\cos 2x}$$

$$= 1 \cdot 1 \cdot \frac{2}{3} \cdot 1 = \frac{2}{3}$$

**Answer:** $f(0) = \frac{2}{3}$

---

### Solution 12

**At $x = -1$:**

Left (and value): $a(-1) + b = -a + b$

Right: $(-1)^2 + c = 1 + c$

Equation 1: $-a + b = 1 + c$

**At $x = 2$:**

Left: $4 + c$

Right (and value): $2b + a$

Equation 2: $4 + c = 2b + a$

**Using $g(0) = 1$:**

$g(0) = 0 + c = c = 1$

Equation 3: $c = 1$

**Solve:**

From (3): $c = 1$

Substitute into (1): $-a + b = 2$

Substitute into (2): $5 = 2b + a$

Add these: $b + b = 7 \implies$ wait, let me redo:

From (1): $b - a = 2$
From (2): $a + 2b = 5$

Add: $3b = 7 \implies b = \frac{7}{3}$

Then: $a = b - 2 = \frac{7}{3} - 2 = \frac{1}{3}$

**Answer:** $a = \frac{1}{3}$, $b = \frac{7}{3}$, $c = 1$

---

### Solution 13

Factor:
- $x^4 - 16 = (x^2 - 4)(x^2 + 4) = (x-2)(x+2)(x^2+4)$
- $x^3 - 8 = (x-2)(x^2 + 2x + 4)$

$$\frac{x^4 - 16}{x^3 - 8} = \frac{(x-2)(x+2)(x^2+4)}{(x-2)(x^2+2x+4)} = \frac{(x+2)(x^2+4)}{x^2+2x+4}$$

$$\lim_{x \to 2} \frac{(x+2)(x^2+4)}{x^2+2x+4} = \frac{(4)(8)}{4+4+4} = \frac{32}{12} = \frac{8}{3}$$

**Answer:** $f(2) = \frac{8}{3}$

---

### Solution 14

For continuity at $x = k$:

Left (and value): $k \cdot k + 1 = k^2 + 1$

Right: $k^2$

Set equal: $k^2 + 1 = k^2$, which gives $1 = 0$.

**This is impossible for any $k$.**

**Answer:** No value of $k$ works.

---

### Solution 15

Rationalize:
$$\frac{\sqrt{1+\sin x} - \sqrt{1-\sin x}}{x} \cdot \frac{\sqrt{1+\sin x} + \sqrt{1-\sin x}}{\sqrt{1+\sin x} + \sqrt{1-\sin x}}$$

$$= \frac{(1+\sin x) - (1-\sin x)}{x(\sqrt{1+\sin x} + \sqrt{1-\sin x})} = \frac{2\sin x}{x(\sqrt{1+\sin x} + \sqrt{1-\sin x})}$$

$$\lim_{x \to 0} \frac{2\sin x}{x} \cdot \frac{1}{\sqrt{1+\sin x} + \sqrt{1-\sin x}}$$

$$= 2 \cdot 1 \cdot \frac{1}{\sqrt{1} + \sqrt{1}} = 2 \cdot \frac{1}{2} = 1$$

**Answer:** $f(0) = 1$

---

### Solution 16

Let $y = \left(\frac{\sin x}{x}\right)^{1/x^2}$

Take the natural log:
$$\ln y = \frac{1}{x^2} \ln\left(\frac{\sin x}{x}\right)$$

As $x \to 0$, $\frac{\sin x}{x} \to 1$, so $\ln\left(\frac{\sin x}{x}\right) \to 0$.

We need $\lim_{x \to 0} \frac{\ln(\frac{\sin x}{x})}{x^2}$.

Using the expansion $\frac{\sin x}{x} = 1 - \frac{x^2}{6} + O(x^4)$:

$$\ln\left(1 - \frac{x^2}{6} + O(x^4)\right) \approx -\frac{x^2}{6}$$

$$\lim_{x \to 0} \frac{-x^2/6}{x^2} = -\frac{1}{6}$$

So $\ln y \to -\frac{1}{6}$, meaning $y \to e^{-1/6}$.

**Answer:** $f(0) = e^{-1/6}$

---

### Solution 17

Left limit: $\lim_{x \to 0^-} \frac{\sin ax}{x} = a$

Right limit: $\lim_{x \to 0^+} \frac{e^{bx} - 1}{x} = b$

For continuity: $a = b$ (both limits equal)

For the common limit to equal 2: $a = b = 2$

**Answer:** $a = 2$, $b = 2$

---

### Solution 18

$$\lim_{x \to a} \frac{x^n - a^n}{x - a}$$

This is the definition of the derivative of $f(x) = x^n$ at $x = a$!

$$\lim_{x \to a} \frac{x^n - a^n}{x - a} = f'(a) = n \cdot a^{n-1}$$

**Alternative:** Factor using $x^n - a^n = (x-a)(x^{n-1} + x^{n-2}a + \cdots + xa^{n-2} + a^{n-1})$

$$= \lim_{x \to a} (x^{n-1} + x^{n-2}a + \cdots + a^{n-1}) = na^{n-1}$$

**Answer:** $h(a) = na^{n-1}$

---

## AP Exam Tips

### Recognition Patterns

| Expression Type | Limit as $x \to 0$ |
|----------------|-------------------|
| $\frac{\sin ax}{x}$ | $a$ |
| $\frac{\sin ax}{\sin bx}$ | $\frac{a}{b}$ |
| $\frac{e^{ax} - 1}{x}$ | $a$ |
| $\frac{\ln(1 + ax)}{x}$ | $a$ |
| $\frac{1 - \cos x}{x^2}$ | $\frac{1}{2}$ |
| $\frac{\tan ax}{x}$ | $a$ |

### Common Mistakes

**Mistake 1: Forgetting the limit must exist**

You can only make a function continuous if the limit exists. Jump and infinite discontinuities cannot be fixed.

**Mistake 2: Algebra errors in factoring**

Double-check your factoring, especially with cubics and quartics.

**Mistake 3: Wrong formula for piecewise**

Use the correct piece for the function value vs. the limit.

**Mistake 4: Not verifying the answer**

Always plug your answer back in to check continuity.

### Free Response Template

"To make $f$ continuous at $x = a$:

Step 1: Find $\lim_{x \to a} f(x)$.
[Show work]
$\lim_{x \to a} f(x) = L$

Step 2: For continuity, we need $f(a) = \lim_{x \to a} f(x)$.

Therefore, $f(a) = L$."

---

## Summary

**Making a function continuous at $x = a$:**

1. **Find the limit:** Calculate $L = \lim_{x \to a} f(x)$
2. **Define the value:** Set $f(a) = L$

**This only works when:**
- The limit exists (not infinite, not oscillating)
- Both one-sided limits are equal (not a jump)

**Key techniques:**
- Factor and cancel for rational functions
- Rationalize for radical functions
- Use standard limits for trig and exponential functions
- Set up equations for piecewise functions

**When it's impossible:**
- Jump discontinuity (one-sided limits differ)
- Infinite discontinuity (limit is $\pm\infty$)
- Oscillating discontinuity (limit doesn't exist)

Knowing how to make functions continuous reinforces your understanding of limits and prepares you for defining derivatives!

---

**Next Topics to Explore:**
- Properties of Continuous Functions
- Introduction to Derivatives
- The Definition of the Derivative
