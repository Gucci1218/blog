# Continuity Basics

## Learning Objectives

By the end of this article, you will be able to:

- Explain what continuity means intuitively and formally
- Apply the three-part definition of continuity at a point
- Determine whether a function is continuous at a specific point
- Identify points of discontinuity from graphs and equations
- Understand continuity on an interval (open and closed)
- Recognize functions that are continuous on their domains
- Solve AP Calculus problems involving continuity

---

## The Core Concept: What Does "Continuous" Really Mean?

### The Intuition

Imagine drawing a curve on paper without lifting your pencil. If you can trace the entire curve in one smooth motion—no jumps, no gaps, no holes—that curve is **continuous**.

**Real-world examples:**

1. **Temperature throughout the day:** The temperature at noon doesn't suddenly "jump" from 70°F to 85°F in an instant. It changes smoothly and gradually. Temperature is continuous.

2. **Your height as you grow:** You don't go from 5'0" to 5'1" instantaneously. Growth happens continuously over time.

3. **Water flowing from a faucet:** The amount of water varies smoothly as you turn the handle—no sudden jumps.

**Contrast with discontinuous examples:**

1. **Postage rates:** The cost jumps at certain weight thresholds (0-1 oz: $0.68, 1-2 oz: $0.92, etc.)

2. **Your age:** You're 17 years old... then suddenly you're 18. Age (in whole years) jumps.

3. **Light switch:** On or off—no smooth transition between states.

### The Pencil Test (Informal Definition)

A function $f$ is **continuous on an interval** if you can draw its graph over that interval without lifting your pencil.

But this informal definition isn't precise enough for calculus. We need something we can actually verify mathematically.

### The Three Conditions for Continuity at a Point

A function $f$ is **continuous at $x = a$** if and only if ALL THREE conditions hold:

$$\boxed{
\begin{aligned}
&\textbf{1. } f(a) \text{ exists (the function is defined at } a\text{)} \\
&\textbf{2. } \lim_{x \to a} f(x) \text{ exists (the limit exists)} \\
&\textbf{3. } \lim_{x \to a} f(x) = f(a) \text{ (the limit equals the function value)}
\end{aligned}
}$$

Think of it as a three-part checklist. If ANY condition fails, the function is **discontinuous** at that point.

### Understanding Each Condition

**Condition 1: $f(a)$ exists**

The function must be defined at the point. There must be a "y-value" when you plug in $x = a$.

*Fails when:* The point is not in the domain (like $x = 0$ for $f(x) = \frac{1}{x}$)

**Condition 2: $\lim_{x \to a} f(x)$ exists**

The limit must exist, meaning both one-sided limits exist and are equal:
$$\lim_{x \to a^-} f(x) = \lim_{x \to a^+} f(x)$$

*Fails when:* There's a jump, or the function goes to infinity from either side

**Condition 3: $\lim_{x \to a} f(x) = f(a)$**

Even if both the function value and the limit exist, they must be equal. The function must actually "arrive" at the point it's approaching.

*Fails when:* The limit exists but doesn't match the function value (a hole with a point defined elsewhere)

### Visual Guide to the Three Conditions

```
Condition 1 fails:          Condition 2 fails:          Condition 3 fails:
(hole, no point)            (jump discontinuity)        (misplaced point)

     |                           |                           |
     |    ○                      |    ●                      |         ●
     |   / \                     |    |                      |
     |  /   \                    |    |                      |    ○
     |_/     \_____              | ---○                      |   / \
                                 |                           |__/   \____
  f(a) undefined              Left ≠ Right               Limit ≠ f(a)
```

---

## Checking Continuity: A Systematic Approach

### The Continuity Checklist

When asked "Is $f$ continuous at $x = a$?", follow these steps:

**Step 1:** Find $f(a)$. Is it defined? (If not, stop—discontinuous)

**Step 2:** Find $\lim_{x \to a} f(x)$. Does it exist? (If not, stop—discontinuous)

**Step 3:** Does $\lim_{x \to a} f(x) = f(a)$? (If not, discontinuous. If yes, continuous!)

### Example: Polynomial Function

**Is $f(x) = x^2 - 3x + 2$ continuous at $x = 1$?**

**Step 1:** $f(1) = 1^2 - 3(1) + 2 = 1 - 3 + 2 = 0$ ✓ (defined)

**Step 2:** $\lim_{x \to 1} (x^2 - 3x + 2) = 0$ ✓ (exists)

**Step 3:** $\lim_{x \to 1} f(x) = 0 = f(1)$ ✓ (equal)

**Conclusion:** Yes, $f$ is continuous at $x = 1$.

In fact, **all polynomials are continuous everywhere**—this is a theorem you should know!

### Example: Rational Function

**Is $g(x) = \frac{x^2 - 4}{x - 2}$ continuous at $x = 2$?**

**Step 1:** $g(2) = \frac{4 - 4}{2 - 2} = \frac{0}{0}$ ✗ (undefined!)

**Conclusion:** $g$ is discontinuous at $x = 2$ because condition 1 fails.

Note: Even though $\lim_{x \to 2} g(x) = \lim_{x \to 2} \frac{(x-2)(x+2)}{x-2} = \lim_{x \to 2} (x+2) = 4$ exists, the function is still discontinuous because $g(2)$ itself is undefined.

---

## Continuity on Intervals

### Open Interval Continuity

A function $f$ is **continuous on an open interval $(a, b)$** if $f$ is continuous at every point $c$ in the interval.

Example: $f(x) = \frac{1}{x}$ is continuous on $(0, \infty)$ and on $(-\infty, 0)$, but not on any interval containing 0.

### Closed Interval Continuity

A function $f$ is **continuous on a closed interval $[a, b]$** if:

1. $f$ is continuous on the open interval $(a, b)$
2. $\lim_{x \to a^+} f(x) = f(a)$ (continuous from the right at $a$)
3. $\lim_{x \to b^-} f(x) = f(b)$ (continuous from the left at $b$)

**Why the one-sided limits at endpoints?**

At the endpoints, we can only approach from one direction (we can't approach $a$ from the left if we're only considering $[a, b]$).

### Example: Square Root Function

$f(x) = \sqrt{x}$ is continuous on $[0, \infty)$.

At $x = 0$:
- $f(0) = 0$ ✓
- $\lim_{x \to 0^+} \sqrt{x} = 0$ ✓
- We only need the right-hand limit since 0 is a left endpoint

---

## Functions Continuous on Their Domains

### The "Automatic" Continuity Theorem

Many common functions are continuous at every point in their domain. If a function is in this list and the point is in its domain, you can immediately conclude continuity.

**Always continuous on their domains:**

| Function Type | Examples | Domain |
|--------------|----------|--------|
| Polynomials | $x^3 - 2x + 5$ | All real numbers |
| Rational functions | $\frac{x+1}{x^2-4}$ | All $x$ where denominator ≠ 0 |
| Root functions | $\sqrt{x}$, $\sqrt[3]{x}$ | Where radicand ≥ 0 (even roots) |
| Trigonometric | $\sin x$, $\cos x$ | All real numbers |
| | $\tan x$, $\sec x$ | Where $\cos x \neq 0$ |
| Exponential | $e^x$, $2^x$ | All real numbers |
| Logarithmic | $\ln x$, $\log x$ | $x > 0$ |
| Inverse trig | $\arcsin x$, $\arctan x$ | Appropriate domains |

### What This Means in Practice

If someone asks:

"Is $f(x) = e^{\sin x}$ continuous at $x = \pi$?"

You can reason:
- $\sin x$ is continuous everywhere, including at $x = \pi$
- $e^u$ is continuous for all $u$
- The composition of continuous functions is continuous
- Therefore, $f$ is continuous at $x = \pi$

---

## Worked Examples

### Example 1: Checking All Three Conditions

**Problem:** Is $f(x) = \begin{cases} x^2 & \text{if } x \neq 2 \\ 5 & \text{if } x = 2 \end{cases}$ continuous at $x = 2$?

**Solution:**

**Step 1:** Find $f(2)$.
$$f(2) = 5 \quad \checkmark \text{ (defined)}$$

**Step 2:** Find $\lim_{x \to 2} f(x)$.
For $x \neq 2$, we use $f(x) = x^2$:
$$\lim_{x \to 2} f(x) = \lim_{x \to 2} x^2 = 4 \quad \checkmark \text{ (exists)}$$

**Step 3:** Does the limit equal the function value?
$$\lim_{x \to 2} f(x) = 4 \neq 5 = f(2) \quad \text{✗}$$

**Conclusion:** $f$ is **discontinuous** at $x = 2$ because condition 3 fails.

---

### Example 2: Piecewise Function Analysis

**Problem:** Determine if $g(x) = \begin{cases} 2x + 1 & \text{if } x < 1 \\ 4 - x & \text{if } x \geq 1 \end{cases}$ is continuous at $x = 1$.

**Solution:**

**Step 1:** Find $g(1)$.
Since $1 \geq 1$, use the second piece:
$$g(1) = 4 - 1 = 3 \quad \checkmark$$

**Step 2:** Find $\lim_{x \to 1} g(x)$.

Left-hand limit (using $2x + 1$):
$$\lim_{x \to 1^-} g(x) = 2(1) + 1 = 3$$

Right-hand limit (using $4 - x$):
$$\lim_{x \to 1^+} g(x) = 4 - 1 = 3$$

Since both one-sided limits equal 3:
$$\lim_{x \to 1} g(x) = 3 \quad \checkmark$$

**Step 3:** Does the limit equal the function value?
$$\lim_{x \to 1} g(x) = 3 = g(1) \quad \checkmark$$

**Conclusion:** $g$ is **continuous** at $x = 1$.

---

### Example 3: Finding Where Discontinuities Occur

**Problem:** Find all points of discontinuity for $h(x) = \frac{x + 3}{x^2 - 9}$.

**Solution:**

First, factor the denominator:
$$h(x) = \frac{x + 3}{(x - 3)(x + 3)}$$

The function is undefined where the denominator equals zero:
$$x^2 - 9 = 0 \implies x = 3 \text{ or } x = -3$$

**At $x = 3$:**
- $h(3)$ is undefined (denominator = 0)
- Discontinuous at $x = 3$

**At $x = -3$:**
- $h(-3)$ is undefined (denominator = 0)
- Discontinuous at $x = -3$

Note: Even though the $(x + 3)$ factors "cancel," the function is still undefined at $x = -3$. The original function has a hole there.

**Points of discontinuity:** $x = -3$ and $x = 3$

---

### Example 4: Making a Function Continuous

**Problem:** Find the value of $k$ that makes $f(x) = \begin{cases} x^2 + k & \text{if } x \leq 2 \\ 3x & \text{if } x > 2 \end{cases}$ continuous at $x = 2$.

**Solution:**

For continuity at $x = 2$, we need:
$$\lim_{x \to 2^-} f(x) = \lim_{x \to 2^+} f(x) = f(2)$$

**Left-hand limit:**
$$\lim_{x \to 2^-} (x^2 + k) = 4 + k$$

**Right-hand limit:**
$$\lim_{x \to 2^+} 3x = 6$$

**Function value:**
$$f(2) = 2^2 + k = 4 + k$$

For continuity, set left limit = right limit:
$$4 + k = 6$$
$$k = 2$$

**Verification:** With $k = 2$:
- $f(2) = 4 + 2 = 6$
- $\lim_{x \to 2^-} f(x) = 4 + 2 = 6$
- $\lim_{x \to 2^+} f(x) = 6$

All three conditions satisfied! ✓

---

### Example 5: Continuity from a Graph

**Problem:** Using the graph below, determine where $f$ is discontinuous.

```
     y
     |
   4 |          ●
   3 |    ●----○
   2 |   /      \
   1 |  /        \
   0 |_/____●_____\______ x
        -2  0  2  4
```

**Solution:**

**At $x = -2$:**
The graph shows a filled dot at $(-2, 3)$ and the curve approaching 3 from both sides.
- $f(-2) = 3$ ✓
- $\lim_{x \to -2} f(x) = 3$ ✓
- Limit equals function value ✓
- **Continuous at $x = -2$**

**At $x = 2$:**
The graph shows an open circle at $(2, 3)$ and a filled dot at $(2, 4)$.
- $f(2) = 4$ ✓
- $\lim_{x \to 2} f(x) = 3$ ✓ (approaching the open circle)
- $3 \neq 4$ ✗
- **Discontinuous at $x = 2$** (removable discontinuity)

**At $x = 0$:**
There's a point at the origin $(0, 0)$ that appears isolated.
Without more information, we'd need to check if this matches the limit.

---

### Example 6: Absolute Value Function

**Problem:** Is $f(x) = |x - 3|$ continuous at $x = 3$?

**Solution:**

Rewrite without absolute value:
$$f(x) = |x - 3| = \begin{cases} x - 3 & \text{if } x \geq 3 \\ -(x - 3) = 3 - x & \text{if } x < 3 \end{cases}$$

**Step 1:** $f(3) = |3 - 3| = 0$ ✓

**Step 2:** Find the limit.

Left-hand limit:
$$\lim_{x \to 3^-} (3 - x) = 3 - 3 = 0$$

Right-hand limit:
$$\lim_{x \to 3^+} (x - 3) = 3 - 3 = 0$$

$$\lim_{x \to 3} f(x) = 0 \quad \checkmark$$

**Step 3:** $\lim_{x \to 3} f(x) = 0 = f(3)$ ✓

**Conclusion:** $f(x) = |x - 3|$ is **continuous** at $x = 3$.

In fact, **absolute value functions are continuous everywhere**—the "corner" at $x = 3$ doesn't create a discontinuity.

---

### Example 7: Trigonometric Function

**Problem:** Is $g(x) = \tan x$ continuous at $x = \frac{\pi}{2}$?

**Solution:**

**Step 1:** Find $g\left(\frac{\pi}{2}\right)$.

$$g\left(\frac{\pi}{2}\right) = \tan\left(\frac{\pi}{2}\right) = \frac{\sin(\frac{\pi}{2})}{\cos(\frac{\pi}{2})} = \frac{1}{0}$$

This is undefined! ✗

**Conclusion:** $\tan x$ is **discontinuous** at $x = \frac{\pi}{2}$ because condition 1 fails.

Note: $\tan x$ has vertical asymptotes at $x = \frac{\pi}{2} + n\pi$ for all integers $n$.

---

### Example 8: Composition of Functions

**Problem:** Is $h(x) = \ln(\cos x)$ continuous at $x = 0$?

**Solution:**

We'll use the fact that compositions of continuous functions are continuous.

**At $x = 0$:**
- $\cos(0) = 1$, and cosine is continuous at 0
- $\ln(1) = 0$, and $\ln$ is continuous at 1 (which is in its domain since $1 > 0$)

Since both functions are continuous at the relevant points, their composition is continuous.

**Verification:**
- $h(0) = \ln(\cos 0) = \ln(1) = 0$ ✓
- $\lim_{x \to 0} \ln(\cos x) = \ln(\cos 0) = 0$ ✓
- Limit equals function value ✓

**Conclusion:** $h(x) = \ln(\cos x)$ is **continuous** at $x = 0$.

---

## Properties of Continuous Functions

### Algebraic Operations Preserve Continuity

If $f$ and $g$ are both continuous at $x = a$, then:

| Operation | Result |
|-----------|--------|
| $f + g$ | Continuous at $a$ |
| $f - g$ | Continuous at $a$ |
| $f \cdot g$ | Continuous at $a$ |
| $\frac{f}{g}$ | Continuous at $a$ (if $g(a) \neq 0$) |
| $c \cdot f$ (constant multiple) | Continuous at $a$ |

### Composition Preserves Continuity

If $g$ is continuous at $a$ and $f$ is continuous at $g(a)$, then $f \circ g$ (meaning $f(g(x))$) is continuous at $a$.

**Example:** Since $\sin x$ is continuous everywhere and $x^2 + 1$ is continuous everywhere, $\sin(x^2 + 1)$ is continuous everywhere.

---

## Practice Problems

### Basic Problems (1-5)

**1.** Is $f(x) = 3x^2 - 5x + 2$ continuous at $x = 4$? Justify your answer.

---

**2.** Determine if $g(x) = \frac{x - 5}{x + 2}$ is continuous at $x = -2$.

---

**3.** Given $h(x) = \begin{cases} x + 2 & \text{if } x < 1 \\ 3 & \text{if } x \geq 1 \end{cases}$, is $h$ continuous at $x = 1$?

---

**4.** Find all points where $f(x) = \frac{1}{x^2 - 4}$ is discontinuous.

---

**5.** Is $g(x) = \sqrt{x - 3}$ continuous at $x = 3$?

---

### Intermediate Problems (6-10)

**6.** Determine if $f(x) = \begin{cases} \frac{x^2 - 1}{x - 1} & \text{if } x \neq 1 \\ 3 & \text{if } x = 1 \end{cases}$ is continuous at $x = 1$.

---

**7.** Find the value of $c$ that makes $g(x) = \begin{cases} cx + 2 & \text{if } x \leq 3 \\ x^2 - 4 & \text{if } x > 3 \end{cases}$ continuous at $x = 3$.

---

**8.** Determine all values of $x$ where $h(x) = \frac{x^2 - 5x + 6}{x^2 - 4}$ is discontinuous.

---

**9.** Is $f(x) = \begin{cases} x^2 - 4 & \text{if } x < 2 \\ 0 & \text{if } x = 2 \\ 4 - x^2 & \text{if } x > 2 \end{cases}$ continuous at $x = 2$?

---

**10.** For what value of $k$ is $g(x) = \begin{cases} k\cos x & \text{if } x \leq 0 \\ e^x - 1 & \text{if } x > 0 \end{cases}$ continuous at $x = 0$?

---

### Advanced Problems (11-15)

**11.** Find values of $a$ and $b$ such that $f(x) = \begin{cases} ax + b & \text{if } x < 1 \\ x^2 & \text{if } 1 \leq x \leq 3 \\ 2ax - b & \text{if } x > 3 \end{cases}$ is continuous everywhere.

---

**12.** Determine all points of discontinuity for $h(x) = \frac{|x - 2|}{x - 2}$.

---

**13.** Is $f(x) = x \cdot \sin\left(\frac{1}{x}\right)$ for $x \neq 0$ and $f(0) = 0$ continuous at $x = 0$?

---

**14.** Find all values of $x$ in $[0, 2\pi]$ where $g(x) = \sec x + \csc x$ is discontinuous.

---

**15.** Let $f(x) = \begin{cases} \frac{\sin x}{x} & \text{if } x \neq 0 \\ k & \text{if } x = 0 \end{cases}$. Find $k$ so that $f$ is continuous at $x = 0$.

---

### Challenge Problems (16-18)

**16.** Prove that $f(x) = \sqrt{x^2 + 1} - |x|$ is continuous on all of $\mathbb{R}$.

---

**17.** Find values of $a$, $b$, and $c$ such that $f(x) = \begin{cases} ax^2 + bx + c & \text{if } x \leq 0 \\ \sin x & \text{if } 0 < x < \pi \\ ax + b & \text{if } x \geq \pi \end{cases}$ is continuous everywhere and $f(-1) = 2$.

---

**18.** Define $f(x) = \lfloor x \rfloor + \lfloor -x \rfloor$ where $\lfloor \cdot \rfloor$ is the floor function. Determine all points where $f$ is discontinuous.

---

## Solutions to Practice Problems

### Solution 1

$f(x) = 3x^2 - 5x + 2$ is a polynomial.

**All polynomials are continuous everywhere.**

Therefore, $f$ is continuous at $x = 4$ (and at every other point).

If you want to verify:
- $f(4) = 3(16) - 5(4) + 2 = 48 - 20 + 2 = 30$
- $\lim_{x \to 4} f(x) = 30$
- $\lim_{x \to 4} f(x) = f(4)$ ✓

---

### Solution 2

**Step 1:** $g(-2) = \frac{-2 - 5}{-2 + 2} = \frac{-7}{0}$ is undefined.

**Conclusion:** $g$ is **discontinuous** at $x = -2$ because condition 1 fails.

---

### Solution 3

**Step 1:** $h(1) = 3$ (using the second piece since $1 \geq 1$) ✓

**Step 2:**
- Left: $\lim_{x \to 1^-} (x + 2) = 3$
- Right: $\lim_{x \to 1^+} 3 = 3$
- $\lim_{x \to 1} h(x) = 3$ ✓

**Step 3:** $\lim_{x \to 1} h(x) = 3 = h(1)$ ✓

**Conclusion:** $h$ is **continuous** at $x = 1$.

---

### Solution 4

$f(x) = \frac{1}{x^2 - 4} = \frac{1}{(x-2)(x+2)}$

The function is undefined where the denominator equals zero:
$$x^2 - 4 = 0 \implies x = 2 \text{ or } x = -2$$

**Points of discontinuity:** $x = -2$ and $x = 2$

---

### Solution 5

**Step 1:** $g(3) = \sqrt{3 - 3} = \sqrt{0} = 0$ ✓

**Step 2:** Since $x = 3$ is the left endpoint of the domain $[3, \infty)$, we only check the right-hand limit:
$$\lim_{x \to 3^+} \sqrt{x - 3} = 0$$ ✓

**Step 3:** $\lim_{x \to 3^+} g(x) = 0 = g(3)$ ✓

**Conclusion:** $g$ is **continuous** at $x = 3$ (from the right).

---

### Solution 6

**Step 1:** $f(1) = 3$ (by definition) ✓

**Step 2:** For $x \neq 1$:
$$\lim_{x \to 1} \frac{x^2 - 1}{x - 1} = \lim_{x \to 1} \frac{(x-1)(x+1)}{x-1} = \lim_{x \to 1} (x + 1) = 2$$

The limit exists and equals 2. ✓

**Step 3:** $\lim_{x \to 1} f(x) = 2 \neq 3 = f(1)$ ✗

**Conclusion:** $f$ is **discontinuous** at $x = 1$ because condition 3 fails.

---

### Solution 7

For continuity at $x = 3$:

**Left-hand limit:** $\lim_{x \to 3^-} (cx + 2) = 3c + 2$

**Right-hand limit:** $\lim_{x \to 3^+} (x^2 - 4) = 9 - 4 = 5$

**Function value:** $g(3) = c(3) + 2 = 3c + 2$

Set left = right:
$$3c + 2 = 5$$
$$3c = 3$$
$$c = 1$$

---

### Solution 8

$$h(x) = \frac{x^2 - 5x + 6}{x^2 - 4} = \frac{(x-2)(x-3)}{(x-2)(x+2)}$$

The function is undefined when $x^2 - 4 = 0$, i.e., at $x = 2$ and $x = -2$.

**Points of discontinuity:** $x = -2$ and $x = 2$

Note: At $x = 2$, the discontinuity is removable (the limit exists). At $x = -2$, there's a vertical asymptote.

---

### Solution 9

**Step 1:** $f(2) = 0$ ✓

**Step 2:**
- Left: $\lim_{x \to 2^-} (x^2 - 4) = 4 - 4 = 0$
- Right: $\lim_{x \to 2^+} (4 - x^2) = 4 - 4 = 0$
- $\lim_{x \to 2} f(x) = 0$ ✓

**Step 3:** $\lim_{x \to 2} f(x) = 0 = f(2)$ ✓

**Conclusion:** $f$ is **continuous** at $x = 2$.

---

### Solution 10

For continuity at $x = 0$:

**Left-hand limit:** $\lim_{x \to 0^-} k\cos x = k \cdot \cos(0) = k$

**Right-hand limit:** $\lim_{x \to 0^+} (e^x - 1) = e^0 - 1 = 0$

**Function value:** $g(0) = k\cos(0) = k$

Set left = right:
$$k = 0$$

---

### Solution 11

For continuity at $x = 1$:
- Left: $\lim_{x \to 1^-} (ax + b) = a + b$
- Right: $\lim_{x \to 1^+} x^2 = 1$
- Need: $a + b = 1$ ... (equation 1)

For continuity at $x = 3$:
- Left: $\lim_{x \to 3^-} x^2 = 9$
- Right: $\lim_{x \to 3^+} (2ax - b) = 6a - b$
- Need: $6a - b = 9$ ... (equation 2)

Solve the system:
- From (1): $b = 1 - a$
- Substitute into (2): $6a - (1 - a) = 9$
- $7a - 1 = 9$
- $a = \frac{10}{7}$
- $b = 1 - \frac{10}{7} = -\frac{3}{7}$

**Answer:** $a = \frac{10}{7}$, $b = -\frac{3}{7}$

---

### Solution 12

$$h(x) = \frac{|x - 2|}{x - 2} = \begin{cases} 1 & \text{if } x > 2 \\ -1 & \text{if } x < 2 \end{cases}$$

**At $x = 2$:**
- $h(2) = \frac{0}{0}$ is undefined
- The function is discontinuous at $x = 2$

Even if we could define $h(2)$:
- $\lim_{x \to 2^-} h(x) = -1$
- $\lim_{x \to 2^+} h(x) = 1$
- The limit doesn't exist

**Point of discontinuity:** $x = 2$

---

### Solution 13

We need to find $\lim_{x \to 0} x \sin\left(\frac{1}{x}\right)$.

Since $-1 \leq \sin\left(\frac{1}{x}\right) \leq 1$ for all $x \neq 0$:

$$-|x| \leq x \sin\left(\frac{1}{x}\right) \leq |x|$$

As $x \to 0$: $-|x| \to 0$ and $|x| \to 0$

By the Squeeze Theorem:
$$\lim_{x \to 0} x \sin\left(\frac{1}{x}\right) = 0$$

Since $\lim_{x \to 0} f(x) = 0 = f(0)$, the function is **continuous** at $x = 0$.

---

### Solution 14

$g(x) = \sec x + \csc x = \frac{1}{\cos x} + \frac{1}{\sin x}$

Discontinuous where $\cos x = 0$ or $\sin x = 0$:

- $\cos x = 0$ at $x = \frac{\pi}{2}, \frac{3\pi}{2}$
- $\sin x = 0$ at $x = 0, \pi, 2\pi$

**Points of discontinuity in $[0, 2\pi]$:** $x = 0, \frac{\pi}{2}, \pi, \frac{3\pi}{2}, 2\pi$

---

### Solution 15

We know $\lim_{x \to 0} \frac{\sin x}{x} = 1$.

For continuity at $x = 0$:
$$\lim_{x \to 0} f(x) = f(0)$$
$$1 = k$$

**Answer:** $k = 1$

---

### Solution 16

We need to show $f(x) = \sqrt{x^2 + 1} - |x|$ is continuous on $\mathbb{R}$.

**Approach:** Show $f$ is a combination of continuous functions.

1. $x^2 + 1$ is continuous everywhere (polynomial)
2. $\sqrt{u}$ is continuous for $u > 0$
3. Since $x^2 + 1 > 0$ for all $x$, $\sqrt{x^2 + 1}$ is continuous everywhere
4. $|x|$ is continuous everywhere
5. The difference of continuous functions is continuous

Therefore, $f(x) = \sqrt{x^2 + 1} - |x|$ is continuous on all of $\mathbb{R}$.

---

### Solution 17

**At $x = 0$:**
- Left: $\lim_{x \to 0^-} (ax^2 + bx + c) = c$
- Right: $\lim_{x \to 0^+} \sin x = 0$
- Need: $c = 0$

**At $x = \pi$:**
- Left: $\lim_{x \to \pi^-} \sin x = 0$
- Right: $\lim_{x \to \pi^+} (ax + b) = a\pi + b$
- Need: $a\pi + b = 0$, so $b = -a\pi$

**Using $f(-1) = 2$:**
$$a(-1)^2 + b(-1) + c = 2$$
$$a - b + 0 = 2$$
$$a - (-a\pi) = 2$$
$$a(1 + \pi) = 2$$
$$a = \frac{2}{1 + \pi}$$

Then: $b = -a\pi = -\frac{2\pi}{1 + \pi}$

**Answer:** $a = \frac{2}{1 + \pi}$, $b = -\frac{2\pi}{1 + \pi}$, $c = 0$

---

### Solution 18

Consider $f(x) = \lfloor x \rfloor + \lfloor -x \rfloor$.

**For integer $n$:**
$$f(n) = n + (-n) = 0$$

**For non-integer $x$ where $n < x < n + 1$:**
$$\lfloor x \rfloor = n$$
$$\lfloor -x \rfloor = \lfloor -(n + \text{fractional part}) \rfloor = -n - 1$$
$$f(x) = n + (-n - 1) = -1$$

So $f(x) = \begin{cases} 0 & \text{if } x \in \mathbb{Z} \\ -1 & \text{if } x \notin \mathbb{Z} \end{cases}$

At each integer $n$:
- $f(n) = 0$
- $\lim_{x \to n} f(x) = -1$ (approaching from either side, $f = -1$)

Since the limit doesn't equal the function value at integers, $f$ is discontinuous at every integer.

**Points of discontinuity:** All integers ($\mathbb{Z}$)

---

## AP Exam Tips

### Quick Continuity Check

1. **Polynomials:** Always continuous everywhere
2. **Rational functions:** Continuous except where denominator = 0
3. **Piecewise functions:** Check the boundary points
4. **Compositions:** If each piece is continuous where it matters, so is the composition

### Common Mistakes to Avoid

**Mistake 1: Confusing "undefined" with "limit doesn't exist"**

A function can have a limit even where it's undefined:
$$\lim_{x \to 2} \frac{x^2 - 4}{x - 2} = 4 \text{ exists, even though } f(2) \text{ is undefined}$$

**Mistake 2: Forgetting to check all three conditions**

Students often check only condition 3 without verifying conditions 1 and 2 first.

**Mistake 3: Assuming continuous = differentiable**

Continuity is necessary but not sufficient for differentiability. $f(x) = |x|$ is continuous at $x = 0$ but not differentiable there.

**Mistake 4: Wrong piece for piecewise functions**

At $x = a$, the function value $f(a)$ uses whichever piece includes $a$ in its domain (check ≤ vs <).

### Continuity Decision Tree

```
Is f continuous at x = a?
         |
    Is f(a) defined?
      /         \
    No           Yes
     |            |
   STOP       Does lim f(x) exist?
   Discontinuous    /         \
                  No           Yes
                   |            |
                 STOP       Does lim = f(a)?
                 Discontinuous    /         \
                                No           Yes
                                 |            |
                               STOP      CONTINUOUS!
                               Discontinuous
```

### What to Write on Free Response

When justifying continuity, write all three conditions:

"$f$ is continuous at $x = 2$ because:
1. $f(2) = 5$ (defined)
2. $\lim_{x \to 2} f(x) = 5$ (limit exists)
3. $\lim_{x \to 2} f(x) = f(2)$ (limit equals function value)"

---

## Summary

A function $f$ is **continuous at $x = a$** if three conditions hold:

1. **$f(a)$ is defined** — the function has a value at that point
2. **$\lim_{x \to a} f(x)$ exists** — both one-sided limits exist and are equal
3. **$\lim_{x \to a} f(x) = f(a)$** — the limit equals the function value

**Key facts:**
- Polynomials are continuous everywhere
- Rational functions are continuous except where the denominator is zero
- Compositions of continuous functions are continuous
- Sums, differences, products, and quotients (when defined) of continuous functions are continuous

**For piecewise functions:**
- Check the boundary points where the formula changes
- Evaluate both one-sided limits using the appropriate pieces
- Ensure the function value matches the limit

Understanding continuity is essential for the Intermediate Value Theorem, differentiability, and the Fundamental Theorem of Calculus!

---

**Next Topics to Explore:**
- Types of Discontinuities (Removable, Jump, Infinite)
- Continuity for Piecewise Functions
- The Intermediate Value Theorem
