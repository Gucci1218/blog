# Continuous Functions

## Learning Objectives

By the end of this article, you will be able to:

- Identify which common functions are continuous and where
- State the domains of continuity for polynomial, rational, radical, trigonometric, exponential, and logarithmic functions
- Apply continuity properties to combinations of functions
- Determine continuity of composite functions
- Use continuity to evaluate limits by direct substitution
- Recognize the power of continuity for simplifying calculus problems
- Complete Unit 1 with a comprehensive understanding of limits and continuity

---

## The Core Concept: A Catalog of Continuous Functions

### The Big Picture

One of the most powerful results in calculus is this:

> **Most functions you encounter are continuous on their natural domains.**

This means that once you know a function's domain, you automatically know where it's continuous. No need to check the three conditions at every single point—the function is "well-behaved" throughout its domain.

### Why This Matters

If $f$ is continuous at $x = a$, then:

$$\lim_{x \to a} f(x) = f(a)$$

This is the **direct substitution property**. Instead of doing limit algebra, you can simply plug in the value!

---

## Polynomial Functions

### The Rule

**Polynomials are continuous everywhere.**

$$P(x) = a_nx^n + a_{n-1}x^{n-1} + \cdots + a_1x + a_0$$

is continuous for all real numbers $x$.

### Why?

Polynomials are built from:
- Constants (continuous everywhere)
- The identity function $f(x) = x$ (continuous everywhere)
- Addition, subtraction, multiplication (preserve continuity)

### Examples

| Function | Domain | Continuous on |
|----------|--------|---------------|
| $f(x) = 5$ | $\mathbb{R}$ | $\mathbb{R}$ |
| $f(x) = 3x - 7$ | $\mathbb{R}$ | $\mathbb{R}$ |
| $f(x) = x^2 - 4x + 1$ | $\mathbb{R}$ | $\mathbb{R}$ |
| $f(x) = x^{100} - x^{50} + 1$ | $\mathbb{R}$ | $\mathbb{R}$ |

### Implication for Limits

For any polynomial $P(x)$ and any real number $a$:

$$\lim_{x \to a} P(x) = P(a)$$

Just substitute!

---

## Rational Functions

### The Rule

**Rational functions are continuous wherever they are defined.**

$$R(x) = \frac{P(x)}{Q(x)}$$

is continuous for all $x$ where $Q(x) \neq 0$.

### The Domain

The domain of a rational function is all real numbers except where the denominator equals zero.

### Examples

| Function | Denominator = 0 | Domain | Continuous on |
|----------|-----------------|--------|---------------|
| $\frac{x+1}{x-2}$ | $x = 2$ | $\mathbb{R} \setminus \{2\}$ | $(-\infty, 2) \cup (2, \infty)$ |
| $\frac{x^2}{x^2-4}$ | $x = \pm 2$ | $\mathbb{R} \setminus \{-2, 2\}$ | $(-\infty, -2) \cup (-2, 2) \cup (2, \infty)$ |
| $\frac{1}{x^2+1}$ | Never (always $\geq 1$) | $\mathbb{R}$ | $\mathbb{R}$ |

### Implication for Limits

For a rational function $R(x) = \frac{P(x)}{Q(x)}$:

$$\lim_{x \to a} R(x) = R(a) = \frac{P(a)}{Q(a)} \quad \text{provided } Q(a) \neq 0$$

If $Q(a) = 0$, you need other techniques (factoring, etc.).

---

## Root Functions

### The Rule

**Root functions are continuous on their domains.**

- $f(x) = \sqrt[n]{x}$ where $n$ is odd: continuous on $\mathbb{R}$
- $f(x) = \sqrt[n]{x}$ where $n$ is even: continuous on $[0, \infty)$

More generally, $f(x) = \sqrt[n]{g(x)}$ is continuous wherever $g(x)$ is in the domain of the root function.

### Examples

| Function | Domain | Continuous on |
|----------|--------|---------------|
| $\sqrt{x}$ | $[0, \infty)$ | $[0, \infty)$ |
| $\sqrt[3]{x}$ | $\mathbb{R}$ | $\mathbb{R}$ |
| $\sqrt{x - 3}$ | $[3, \infty)$ | $[3, \infty)$ |
| $\sqrt{9 - x^2}$ | $[-3, 3]$ | $[-3, 3]$ |
| $\sqrt[4]{x + 1}$ | $[-1, \infty)$ | $[-1, \infty)$ |

### Key Insight

For even roots: the radicand (expression under the root) must be non-negative.

$$\sqrt{g(x)} \text{ is continuous where } g(x) \geq 0 \text{ and } g \text{ is continuous}$$

---

## Trigonometric Functions

### Sine and Cosine

**$\sin x$ and $\cos x$ are continuous everywhere.**

Domain: $\mathbb{R}$
Continuous on: $\mathbb{R}$

These are the "nicest" trig functions—no restrictions!

### Tangent and Secant

$$\tan x = \frac{\sin x}{\cos x} \qquad \sec x = \frac{1}{\cos x}$$

Undefined where $\cos x = 0$, which occurs at $x = \frac{\pi}{2} + n\pi$ for integer $n$.

**Continuous on:** $\mathbb{R} \setminus \left\{\frac{\pi}{2} + n\pi : n \in \mathbb{Z}\right\}$

Or equivalently: $\left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$, $\left(\frac{\pi}{2}, \frac{3\pi}{2}\right)$, etc.

### Cotangent and Cosecant

$$\cot x = \frac{\cos x}{\sin x} \qquad \csc x = \frac{1}{\sin x}$$

Undefined where $\sin x = 0$, which occurs at $x = n\pi$ for integer $n$.

**Continuous on:** $\mathbb{R} \setminus \{n\pi : n \in \mathbb{Z}\}$

Or equivalently: $(0, \pi)$, $(\pi, 2\pi)$, etc.

### Summary Table

| Function | Undefined at | Period | Continuous on each interval |
|----------|-------------|--------|----------------------------|
| $\sin x$ | Nowhere | $2\pi$ | $\mathbb{R}$ |
| $\cos x$ | Nowhere | $2\pi$ | $\mathbb{R}$ |
| $\tan x$ | $\frac{\pi}{2} + n\pi$ | $\pi$ | $\left(-\frac{\pi}{2} + n\pi, \frac{\pi}{2} + n\pi\right)$ |
| $\cot x$ | $n\pi$ | $\pi$ | $(n\pi, (n+1)\pi)$ |
| $\sec x$ | $\frac{\pi}{2} + n\pi$ | $2\pi$ | Same as $\tan x$ |
| $\csc x$ | $n\pi$ | $2\pi$ | Same as $\cot x$ |

---

## Exponential Functions

### The Rule

**Exponential functions are continuous everywhere.**

$$f(x) = a^x \quad (a > 0, a \neq 1)$$

is continuous for all real numbers $x$.

### Special Cases

| Function | Domain | Continuous on |
|----------|--------|---------------|
| $e^x$ | $\mathbb{R}$ | $\mathbb{R}$ |
| $2^x$ | $\mathbb{R}$ | $\mathbb{R}$ |
| $10^x$ | $\mathbb{R}$ | $\mathbb{R}$ |
| $e^{-x}$ | $\mathbb{R}$ | $\mathbb{R}$ |
| $e^{x^2}$ | $\mathbb{R}$ | $\mathbb{R}$ |

### Key Properties

- $\lim_{x \to a} e^x = e^a$ (direct substitution works)
- $e^x > 0$ for all $x$ (never zero, never negative)
- $e^x$ is strictly increasing

---

## Logarithmic Functions

### The Rule

**Logarithmic functions are continuous on $(0, \infty)$.**

$$f(x) = \log_a x \quad (a > 0, a \neq 1)$$

is continuous for all $x > 0$.

### The Domain Restriction

Logarithms are only defined for **positive** arguments:
- $\ln x$ requires $x > 0$
- $\ln(g(x))$ requires $g(x) > 0$

### Examples

| Function | Requirement | Domain | Continuous on |
|----------|-------------|--------|---------------|
| $\ln x$ | $x > 0$ | $(0, \infty)$ | $(0, \infty)$ |
| $\ln(x - 2)$ | $x - 2 > 0$ | $(2, \infty)$ | $(2, \infty)$ |
| $\ln(x^2)$ | $x^2 > 0$ | $\mathbb{R} \setminus \{0\}$ | $(-\infty, 0) \cup (0, \infty)$ |
| $\ln(\cos x)$ | $\cos x > 0$ | $\left(-\frac{\pi}{2} + 2n\pi, \frac{\pi}{2} + 2n\pi\right)$ | Same |
| $\log_{10}(x + 5)$ | $x + 5 > 0$ | $(-5, \infty)$ | $(-5, \infty)$ |

---

## Inverse Trigonometric Functions

### The Rule

**Inverse trig functions are continuous on their domains.**

| Function | Domain | Range | Continuous on |
|----------|--------|-------|---------------|
| $\arcsin x$ (or $\sin^{-1} x$) | $[-1, 1]$ | $\left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$ | $[-1, 1]$ |
| $\arccos x$ (or $\cos^{-1} x$) | $[-1, 1]$ | $[0, \pi]$ | $[-1, 1]$ |
| $\arctan x$ (or $\tan^{-1} x$) | $\mathbb{R}$ | $\left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$ | $\mathbb{R}$ |

### Key Facts

- $\arctan x$ is continuous everywhere—very useful!
- $\arcsin x$ and $\arccos x$ have restricted domains due to the range of sine and cosine

---

## Absolute Value Function

### The Rule

**The absolute value function is continuous everywhere.**

$$f(x) = |x|$$

is continuous for all real numbers $x$.

### Even at $x = 0$!

Despite the "corner" in the graph at $x = 0$, the function is still continuous there:

- $|0| = 0$
- $\lim_{x \to 0} |x| = 0$
- They're equal ✓

Note: Continuous ≠ Differentiable. The absolute value is continuous at 0 but not differentiable there.

### Compositions

$|g(x)|$ is continuous wherever $g(x)$ is continuous.

| Function | Continuous on |
|----------|---------------|
| $|x - 3|$ | $\mathbb{R}$ |
| $|x^2 - 4|$ | $\mathbb{R}$ |
| $|\sin x|$ | $\mathbb{R}$ |
| $|\ln x|$ | $(0, \infty)$ |

---

## Combining Continuous Functions

### Algebraic Operations

If $f$ and $g$ are both continuous at $x = a$, then:

| Operation | Result | Condition |
|-----------|--------|-----------|
| $f + g$ | Continuous at $a$ | — |
| $f - g$ | Continuous at $a$ | — |
| $f \cdot g$ | Continuous at $a$ | — |
| $\frac{f}{g}$ | Continuous at $a$ | $g(a) \neq 0$ |
| $c \cdot f$ | Continuous at $a$ | — |
| $[f]^n$ | Continuous at $a$ | — |

### Examples

If $f(x) = x^2$ and $g(x) = \sin x$, both continuous everywhere, then:

- $x^2 + \sin x$ is continuous everywhere
- $x^2 \cdot \sin x$ is continuous everywhere
- $\frac{\sin x}{x^2}$ is continuous everywhere except $x = 0$

---

## Composition of Functions

### The Rule

**If $g$ is continuous at $a$ and $f$ is continuous at $g(a)$, then $f \circ g$ is continuous at $a$.**

$$\lim_{x \to a} f(g(x)) = f\left(\lim_{x \to a} g(x)\right) = f(g(a))$$

### In Plain English

You can "pass the limit inside" a continuous function.

### Examples

**Example 1:** Is $h(x) = \sin(x^2)$ continuous at $x = 2$?

- Inner function: $g(x) = x^2$ is continuous at $x = 2$
- Outer function: $f(u) = \sin u$ is continuous at $u = g(2) = 4$
- Therefore: $h(x) = \sin(x^2)$ is continuous at $x = 2$ ✓

**Example 2:** Is $h(x) = \ln(\cos x)$ continuous at $x = 0$?

- Inner: $g(x) = \cos x$ is continuous at $x = 0$, and $g(0) = 1 > 0$
- Outer: $f(u) = \ln u$ is continuous at $u = 1$
- Therefore: $h(x) = \ln(\cos x)$ is continuous at $x = 0$ ✓

**Example 3:** Is $h(x) = \sqrt{\sin x}$ continuous at $x = \frac{\pi}{2}$?

- Inner: $g(x) = \sin x$ is continuous, and $g\left(\frac{\pi}{2}\right) = 1 \geq 0$
- Outer: $f(u) = \sqrt{u}$ is continuous at $u = 1$
- Therefore: continuous at $x = \frac{\pi}{2}$ ✓

**Example 4:** Where is $h(x) = \sqrt{\sin x}$ continuous?

We need $\sin x \geq 0$, which occurs on $[0, \pi] \cup [2\pi, 3\pi] \cup \ldots$

Or: $[2n\pi, (2n+1)\pi]$ for integer $n$.

---

## The Direct Substitution Property

### The Power of Continuity

For any function $f$ that is continuous at $x = a$:

$$\boxed{\lim_{x \to a} f(x) = f(a)}$$

This transforms limit problems into simple evaluation problems!

### When to Use Direct Substitution

1. Check if the function is continuous at the point
2. If yes, just plug in the value
3. If no (or if you get an indeterminate form), use other techniques

### Examples

**Example 1:** $\lim_{x \to 3} (x^2 + 2x - 1)$

Polynomials are continuous everywhere. Direct substitution:
$$= 9 + 6 - 1 = 14$$

**Example 2:** $\lim_{x \to 0} \cos(e^x)$

Both $e^x$ and $\cos u$ are continuous. Direct substitution:
$$= \cos(e^0) = \cos(1) \approx 0.540$$

**Example 3:** $\lim_{x \to 1} \ln(x^2 + x)$

At $x = 1$: $x^2 + x = 2 > 0$, so $\ln$ is defined. Direct substitution:
$$= \ln(1 + 1) = \ln 2$$

**Example 4:** $\lim_{x \to \pi} \frac{\sin x}{x}$

Continuous at $x = \pi$ (denominator ≠ 0). Direct substitution:
$$= \frac{\sin \pi}{\pi} = \frac{0}{\pi} = 0$$

---

## Worked Examples: Determining Continuity

### Example 1: Complex Rational Function

**Problem:** Find all points where $f(x) = \frac{x^2 - 1}{x^3 - x}$ is discontinuous.

**Solution:**

Factor the denominator:
$$x^3 - x = x(x^2 - 1) = x(x-1)(x+1)$$

The function is undefined at $x = 0, 1, -1$.

**At $x = 0$:** Denominator = 0, numerator = $-1 \neq 0$. Infinite discontinuity.

**At $x = 1$:** Both = 0. Factor:
$$f(x) = \frac{(x-1)(x+1)}{x(x-1)(x+1)} = \frac{1}{x} \quad (x \neq 0, \pm 1)$$
The $(x-1)$ and $(x+1)$ cancel, but the discontinuity at $x = 1$ is removable.

**At $x = -1$:** Same analysis—removable discontinuity.

**Answer:**
- Infinite discontinuity at $x = 0$
- Removable discontinuities at $x = \pm 1$

---

### Example 2: Composite Function Domain

**Problem:** Find the domain and intervals of continuity for $g(x) = \ln(4 - x^2)$.

**Solution:**

We need $4 - x^2 > 0$:
$$x^2 < 4$$
$$-2 < x < 2$$

**Domain:** $(-2, 2)$

Since $\ln u$ is continuous for $u > 0$ and $4 - x^2$ is continuous (polynomial), the composition is continuous on its entire domain.

**Continuous on:** $(-2, 2)$

---

### Example 3: Combining Multiple Functions

**Problem:** Where is $h(x) = \frac{\sqrt{x}}{x - 4}$ continuous?

**Solution:**

**Numerator:** $\sqrt{x}$ requires $x \geq 0$

**Denominator:** $x - 4 \neq 0$, so $x \neq 4$

**Combined:** $x \geq 0$ and $x \neq 4$

**Domain:** $[0, 4) \cup (4, \infty)$

**Continuous on:** $[0, 4) \cup (4, \infty)$

---

### Example 4: Inverse Trig Composition

**Problem:** Find the domain and continuity intervals for $f(x) = \arcsin(2x - 1)$.

**Solution:**

For $\arcsin$, we need $-1 \leq 2x - 1 \leq 1$:
$$0 \leq 2x \leq 2$$
$$0 \leq x \leq 1$$

**Domain:** $[0, 1]$

**Continuous on:** $[0, 1]$

---

### Example 5: Exponential-Trig Combination

**Problem:** Evaluate $\lim_{x \to 0} e^{\sin x}$.

**Solution:**

$e^u$ is continuous everywhere, and $\sin x$ is continuous at $x = 0$.

By continuity of composition:
$$\lim_{x \to 0} e^{\sin x} = e^{\sin 0} = e^0 = 1$$

---

### Example 6: Multiple Compositions

**Problem:** Where is $f(x) = \sqrt{\ln(x)}$ continuous?

**Solution:**

**Step 1:** $\ln(x)$ requires $x > 0$

**Step 2:** $\sqrt{u}$ requires $u \geq 0$, so $\ln(x) \geq 0$

$\ln(x) \geq 0$ means $x \geq 1$

**Combined:** $x \geq 1$

**Continuous on:** $[1, \infty)$

---

### Example 7: Piecewise with Standard Functions

**Problem:** Where is $g(x) = \begin{cases} \frac{\sin x}{x} & \text{if } x \neq 0 \\ 1 & \text{if } x = 0 \end{cases}$ continuous?

**Solution:**

**For $x \neq 0$:** $\frac{\sin x}{x}$ is continuous (ratio of continuous functions, denominator ≠ 0)

**At $x = 0$:**
- $g(0) = 1$
- $\lim_{x \to 0} \frac{\sin x}{x} = 1$
- Limit = function value ✓

**Continuous on:** $\mathbb{R}$ (everywhere!)

This is the continuous extension of $\frac{\sin x}{x}$.

---

## Practice Problems

### Basic Problems (1-5)

**1.** State the domain and intervals of continuity for $f(x) = \frac{x + 3}{x^2 - 9}$.

---

**2.** Evaluate $\lim_{x \to 2} (x^3 - 3x + e^x)$ using continuity.

---

**3.** Find where $g(x) = \sqrt{x^2 - 4}$ is continuous.

---

**4.** Is $h(x) = \tan(x^2)$ continuous at $x = 0$? Justify.

---

**5.** Evaluate $\lim_{x \to \pi/4} \sin(\cos x)$ using continuity.

---

### Intermediate Problems (6-10)

**6.** Find all discontinuities of $f(x) = \frac{x^2 - 4}{x^3 - 8}$ and classify each.

---

**7.** Determine the domain and intervals of continuity for $g(x) = \ln(x^2 - 1)$.

---

**8.** Where is $h(x) = \arcsin\left(\frac{x}{2}\right)$ continuous?

---

**9.** Evaluate $\lim_{x \to 1} \sqrt{x + \ln x}$ using continuity.

---

**10.** Find all points where $f(x) = \frac{|x - 2|}{x - 2}$ is discontinuous and classify.

---

### Advanced Problems (11-15)

**11.** Determine where $g(x) = \sqrt{\cos x}$ is continuous.

---

**12.** Find the domain and continuity intervals for $h(x) = \ln(\sin x)$ on $[0, 2\pi]$.

---

**13.** Where is $f(x) = e^{1/x}$ continuous? What happens at $x = 0$?

---

**14.** Evaluate $\lim_{x \to 0^+} x^{\sin x}$ using continuity properties.

*(Hint: Write as $e^{\sin x \cdot \ln x}$)*

---

**15.** Find all values of $x$ where $g(x) = \lfloor \sin x \rfloor$ is discontinuous on $[0, 2\pi]$.

---

### Challenge Problems (16-18)

**16.** Prove that $f(x) = x \sin\left(\frac{1}{x}\right)$ for $x \neq 0$ and $f(0) = 0$ is continuous everywhere.

---

**17.** Let $f(x) = \begin{cases} x^2 \sin\left(\frac{1}{x}\right) & \text{if } x \neq 0 \\ 0 & \text{if } x = 0 \end{cases}$. Prove $f$ is continuous at $x = 0$.

---

**18.** Find all functions $f$ that are continuous on $\mathbb{R}$ and satisfy $f(x + y) = f(x) + f(y)$ for all $x, y$.

---

## Solutions to Practice Problems

### Solution 1

Factor the denominator: $x^2 - 9 = (x-3)(x+3)$

$$f(x) = \frac{x + 3}{(x-3)(x+3)} = \frac{1}{x - 3} \quad (x \neq -3)$$

**Domain:** $\mathbb{R} \setminus \{-3, 3\}$

**Discontinuities:**
- At $x = -3$: removable (factor cancels)
- At $x = 3$: infinite (vertical asymptote)

**Continuous on:** $(-\infty, -3) \cup (-3, 3) \cup (3, \infty)$

---

### Solution 2

$x^3 - 3x + e^x$ is a sum of continuous functions (polynomial + exponential).

Direct substitution:
$$\lim_{x \to 2} (x^3 - 3x + e^x) = 8 - 6 + e^2 = 2 + e^2$$

---

### Solution 3

Need $x^2 - 4 \geq 0$:
$$x^2 \geq 4$$
$$|x| \geq 2$$
$$x \leq -2 \text{ or } x \geq 2$$

**Continuous on:** $(-\infty, -2] \cup [2, \infty)$

---

### Solution 4

At $x = 0$:
- $x^2 = 0$
- $\tan(0) = 0$ is defined

Since $\tan u$ is continuous at $u = 0$ and $x^2$ is continuous everywhere:

**Yes, $h(x) = \tan(x^2)$ is continuous at $x = 0$.**

---

### Solution 5

Both $\cos x$ and $\sin u$ are continuous everywhere.

Direct substitution:
$$\lim_{x \to \pi/4} \sin(\cos x) = \sin\left(\cos\frac{\pi}{4}\right) = \sin\left(\frac{\sqrt{2}}{2}\right)$$

---

### Solution 6

Factor:
- Numerator: $x^2 - 4 = (x-2)(x+2)$
- Denominator: $x^3 - 8 = (x-2)(x^2 + 2x + 4)$

$$f(x) = \frac{(x-2)(x+2)}{(x-2)(x^2+2x+4)} = \frac{x+2}{x^2+2x+4} \quad (x \neq 2)$$

At $x = 2$:
$$\lim_{x \to 2} \frac{x+2}{x^2+2x+4} = \frac{4}{12} = \frac{1}{3}$$

**Discontinuity:** Removable at $x = 2$

---

### Solution 7

Need $x^2 - 1 > 0$:
$$x^2 > 1$$
$$|x| > 1$$
$$x < -1 \text{ or } x > 1$$

**Domain:** $(-\infty, -1) \cup (1, \infty)$

**Continuous on:** $(-\infty, -1) \cup (1, \infty)$

---

### Solution 8

For $\arcsin$, need $-1 \leq \frac{x}{2} \leq 1$:
$$-2 \leq x \leq 2$$

**Continuous on:** $[-2, 2]$

---

### Solution 9

At $x = 1$:
- $x + \ln x = 1 + 0 = 1 \geq 0$ ✓
- All functions involved are continuous

Direct substitution:
$$\lim_{x \to 1} \sqrt{x + \ln x} = \sqrt{1 + \ln 1} = \sqrt{1 + 0} = 1$$

---

### Solution 10

$$f(x) = \frac{|x-2|}{x-2} = \begin{cases} 1 & \text{if } x > 2 \\ -1 & \text{if } x < 2 \end{cases}$$

At $x = 2$:
- $f(2)$ is undefined
- $\lim_{x \to 2^-} f(x) = -1$
- $\lim_{x \to 2^+} f(x) = 1$

**Jump discontinuity at $x = 2$**

---

### Solution 11

Need $\cos x \geq 0$.

$\cos x \geq 0$ on $\left[-\frac{\pi}{2} + 2n\pi, \frac{\pi}{2} + 2n\pi\right]$ for integer $n$.

**Continuous on:** $\bigcup_{n \in \mathbb{Z}} \left[-\frac{\pi}{2} + 2n\pi, \frac{\pi}{2} + 2n\pi\right]$

Or: $\left[-\frac{\pi}{2}, \frac{\pi}{2}\right] \cup \left[\frac{3\pi}{2}, \frac{5\pi}{2}\right] \cup \ldots$

---

### Solution 12

Need $\sin x > 0$ on $[0, 2\pi]$.

$\sin x > 0$ on $(0, \pi)$.

**Domain on $[0, 2\pi]$:** $(0, \pi)$

**Continuous on:** $(0, \pi)$

---

### Solution 13

$e^{1/x}$ is continuous wherever $\frac{1}{x}$ is defined, i.e., $x \neq 0$.

**Continuous on:** $(-\infty, 0) \cup (0, \infty)$

**At $x = 0$:**
- $\lim_{x \to 0^+} e^{1/x} = e^{+\infty} = +\infty$
- $\lim_{x \to 0^-} e^{1/x} = e^{-\infty} = 0$

The one-sided limits are different (one is infinite), so there's a discontinuity at $x = 0$ (infinite from the right, with a one-sided limit of 0 from the left—neither matches, so it's a mix of infinite and jump behavior).

---

### Solution 14

Write $x^{\sin x} = e^{\sin x \cdot \ln x}$.

As $x \to 0^+$:
- $\sin x \to 0$
- $\ln x \to -\infty$

We need $\lim_{x \to 0^+} \sin x \cdot \ln x$.

$$\lim_{x \to 0^+} \sin x \cdot \ln x = \lim_{x \to 0^+} \frac{\ln x}{\csc x} = \lim_{x \to 0^+} \frac{1/x}{-\csc x \cot x}$$

This is getting complex. Use $\sin x \approx x$ for small $x$:

$$\lim_{x \to 0^+} x \ln x = 0$$ (standard result)

Therefore:
$$\lim_{x \to 0^+} x^{\sin x} = e^0 = 1$$

---

### Solution 15

$\lfloor \sin x \rfloor$ on $[0, 2\pi]$:

- $\sin x$ ranges from $-1$ to $1$
- $\lfloor \sin x \rfloor \in \{-1, 0, 1\}$

$\lfloor \sin x \rfloor = 1$ only when $\sin x = 1$ (at $x = \frac{\pi}{2}$)

$\lfloor \sin x \rfloor = 0$ when $0 \leq \sin x < 1$

$\lfloor \sin x \rfloor = -1$ when $-1 \leq \sin x < 0$

**Discontinuities occur when $\sin x$ crosses integers:**
- When $\sin x$ crosses 0 (going down): $x = \pi$
- When $\sin x$ crosses 0 (going up from below 0): $x = 2\pi$
- When $\sin x$ reaches 1: $x = \frac{\pi}{2}$ (jump from 0 to 1 and back)

**Discontinuous at:** $x = \frac{\pi}{2}, \pi, 2\pi$ (within $[0, 2\pi]$)

---

### Solution 16

We need to show $\lim_{x \to 0} x \sin\left(\frac{1}{x}\right) = 0 = f(0)$.

Since $-1 \leq \sin\left(\frac{1}{x}\right) \leq 1$:
$$-|x| \leq x \sin\left(\frac{1}{x}\right) \leq |x|$$

As $x \to 0$, both $-|x|$ and $|x|$ approach 0.

By the Squeeze Theorem:
$$\lim_{x \to 0} x \sin\left(\frac{1}{x}\right) = 0 = f(0)$$

Therefore $f$ is continuous at $x = 0$, and continuous everywhere else (product of continuous functions).

**$f$ is continuous on $\mathbb{R}$.**

---

### Solution 17

Similar to Solution 16, but with $x^2$:

$$-x^2 \leq x^2 \sin\left(\frac{1}{x}\right) \leq x^2$$

As $x \to 0$, both bounds approach 0.

By the Squeeze Theorem:
$$\lim_{x \to 0} x^2 \sin\left(\frac{1}{x}\right) = 0 = f(0)$$

**$f$ is continuous at $x = 0$.**

---

### Solution 18

This is a famous result! Functions satisfying $f(x + y) = f(x) + f(y)$ are called **additive functions**.

**If $f$ is continuous**, then $f(x) = cx$ for some constant $c$.

**Proof sketch:**

1. $f(0) = 0$ (set $x = y = 0$)
2. $f(nx) = nf(x)$ for positive integers $n$ (by induction)
3. $f\left(\frac{x}{n}\right) = \frac{f(x)}{n}$
4. $f(rx) = rf(x)$ for all rationals $r$
5. By continuity, this extends to all reals: $f(x) = f(1) \cdot x$

**Answer:** $f(x) = cx$ for some constant $c \in \mathbb{R}$

---

## AP Exam Tips

### Quick Reference: Common Functions

| Function Type | Continuous On |
|--------------|---------------|
| Polynomial | $\mathbb{R}$ |
| Rational $\frac{P}{Q}$ | Where $Q \neq 0$ |
| $\sqrt[n]{x}$ (n even) | $[0, \infty)$ |
| $\sqrt[n]{x}$ (n odd) | $\mathbb{R}$ |
| $\sin x$, $\cos x$ | $\mathbb{R}$ |
| $\tan x$, $\sec x$ | $x \neq \frac{\pi}{2} + n\pi$ |
| $\cot x$, $\csc x$ | $x \neq n\pi$ |
| $e^x$, $a^x$ | $\mathbb{R}$ |
| $\ln x$, $\log_a x$ | $(0, \infty)$ |
| $\arcsin x$, $\arccos x$ | $[-1, 1]$ |
| $\arctan x$ | $\mathbb{R}$ |
| $|x|$ | $\mathbb{R}$ |

### Direct Substitution Checklist

1. Is the function continuous at the point?
2. Is the point in the domain?
3. If yes to both → just plug in!
4. If no → use other limit techniques

### Common Mistakes

**Mistake 1:** Forgetting domain restrictions on logarithms and even roots

**Mistake 2:** Assuming all trig functions are continuous everywhere (tan, sec, csc, cot have asymptotes!)

**Mistake 3:** Not checking if the composition's intermediate value is in the outer function's domain

**Mistake 4:** Confusing continuity with differentiability ($|x|$ is continuous but not differentiable at 0)

---

## Summary

### The Continuous Function Catalog

Most standard functions are continuous on their natural domains:

- **Polynomials:** Continuous everywhere
- **Rational functions:** Continuous except where denominator = 0
- **Root functions:** Continuous on their domains (even roots need non-negative radicands)
- **Trigonometric:** $\sin$, $\cos$ everywhere; others except at asymptotes
- **Exponential:** Continuous everywhere
- **Logarithmic:** Continuous on $(0, \infty)$
- **Inverse trig:** Continuous on their restricted domains
- **Absolute value:** Continuous everywhere

### Operations Preserve Continuity

If $f$ and $g$ are continuous:
- $f \pm g$, $f \cdot g$, $f/g$ (where defined), $f \circ g$ are all continuous

### The Power of Continuity

For continuous functions:
$$\lim_{x \to a} f(x) = f(a)$$

This **direct substitution property** makes evaluating limits trivial when continuity applies!

---

## Unit 1 Complete!

Congratulations! You've completed **Unit 1: Limits and Continuity**. You now understand:

- What limits are and how to evaluate them
- One-sided limits and limits at infinity
- The formal definition of continuity
- Types of discontinuities
- The Intermediate Value Theorem
- How to make functions continuous
- Which common functions are continuous and where

These concepts form the foundation for everything that follows in calculus—derivatives, integrals, and beyond!

---

**Next Unit: Derivatives Basics**
- The Definition of the Derivative
- Derivatives at a Point
- Tangent Lines
- Basic Derivative Rules

---

<div align="center">

[← Making Functions Continuous](calculus/making-functions-continuous.md) | [Derivative Definition →](calculus/derivative-definition.md)

</div>
