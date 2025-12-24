# Limits at Infinity
<p class="article-date">September 21, 2024</p>

## Learning Objectives

By the end of this article, you will be able to:

- Explain what limits at infinity mean conceptually
- Distinguish between limits at infinity and infinite limits
- Evaluate limits as $x \to \infty$ and $x \to -\infty$
- Identify horizontal asymptotes using limits at infinity
- Apply the dominant term strategy for polynomial and rational functions
- Evaluate limits involving radicals, exponentials, and logarithms at infinity
- Solve AP Calculus problems involving end behavior of functions

---

## The Core Concept: What Happens "Way Out There"?

### The Intuition

Imagine you're driving on a perfectly straight highway that stretches to the horizon. As you travel farther and farther, what happens to your distance from your starting point? It keeps growing forever—there's no final destination you "reach."

But now imagine that same highway gradually approaches a river running parallel to it. No matter how far you drive, the highway gets closer and closer to the river but never quite touches it. This is exactly what limits at infinity describe: **the value a function approaches as the input grows without bound**.

**Real-world example:** Think about a cup of hot coffee cooling in a room. When you first pour it, it's 180°F. Over time, it cools down. After 1 hour, maybe it's 100°F. After 2 hours, 75°F. After a whole day, it might be 70.1°F. As time goes to infinity, the coffee temperature approaches room temperature (70°F) but never goes below it.

### Two Different Concepts: Don't Confuse Them!

**Limits at Infinity** (this article):
$$\lim_{x \to \infty} f(x) = L \quad \text{or} \quad \lim_{x \to -\infty} f(x) = L$$

We're asking: "As $x$ gets larger and larger (or more and more negative), what value does $f(x)$ approach?"

**Infinite Limits** (different concept):
$$\lim_{x \to a} f(x) = \infty \quad \text{or} \quad \lim_{x \to a} f(x) = -\infty$$

This asks: "As $x$ approaches a specific number $a$, does $f(x)$ grow without bound?"

| Type | What varies | What we're finding |
|------|-------------|-------------------|
| Limit at infinity | $x \to \pm\infty$ | The $y$-value approached |
| Infinite limit | $x \to a$ (specific number) | Whether $y \to \pm\infty$ |

### Formal Definitions

**Limit as $x \to \infty$:**
$$\lim_{x \to \infty} f(x) = L$$

This means: "For any desired closeness to $L$, we can find a point beyond which $f(x)$ stays within that closeness to $L$."

In plain English: Eventually, $f(x)$ gets as close to $L$ as we want and stays close.

**Limit as $x \to -\infty$:**
$$\lim_{x \to -\infty} f(x) = L$$

This means: "As $x$ becomes increasingly negative (going left on the number line), $f(x)$ approaches $L$."

### Horizontal Asymptotes

When $\lim_{x \to \infty} f(x) = L$ or $\lim_{x \to -\infty} f(x) = L$, the line $y = L$ is a **horizontal asymptote** of the graph.

A function can have:
- **No horizontal asymptotes** (like $f(x) = x^2$)
- **One horizontal asymptote** (like $f(x) = e^x$, which has $y = 0$ as $x \to -\infty$)
- **Two horizontal asymptotes** (like $f(x) = \arctan(x)$, which has $y = -\frac{\pi}{2}$ and $y = \frac{\pi}{2}$)

---

## The Dominant Term Strategy

### The Big Idea

When $x$ becomes very large (or very negative), the term with the **highest power** dominates the behavior of the expression. All other terms become negligible in comparison.

**Example:** Consider $f(x) = 3x^4 + 100x^3 - 5000x^2 + x - 1$

When $x = 1000$:
- $3x^4 = 3,000,000,000,000$ (3 trillion)
- $100x^3 = 100,000,000,000$ (100 billion)
- $-5000x^2 = -5,000,000,000$ (5 billion)
- $x - 1 = 999$

The $3x^4$ term is 30 times larger than all other terms combined! As $x$ grows, this dominance becomes even more extreme.

### Strategy for Polynomials

For any polynomial $P(x) = a_nx^n + a_{n-1}x^{n-1} + \cdots + a_1x + a_0$ where $a_n \neq 0$:

$$\lim_{x \to \infty} P(x) = \lim_{x \to \infty} a_nx^n$$

**The limit depends on:**
1. The **sign** of the leading coefficient $a_n$
2. The **degree** $n$ (whether it's even or odd)

| Leading Coefficient | Degree | $\lim_{x \to \infty}$ | $\lim_{x \to -\infty}$ |
|---------------------|--------|----------------------|----------------------|
| Positive ($a_n > 0$) | Even | $+\infty$ | $+\infty$ |
| Positive ($a_n > 0$) | Odd | $+\infty$ | $-\infty$ |
| Negative ($a_n < 0$) | Even | $-\infty$ | $-\infty$ |
| Negative ($a_n < 0$) | Odd | $-\infty$ | $+\infty$ |

**Memory trick:** For even degree, both ends go the same direction (like a parabola). For odd degree, the ends go opposite directions (like a cubic).

---

## Rational Functions: The Core Technique

Rational functions (polynomial divided by polynomial) are the most common type you'll see on the AP exam.

### The Divide-by-Highest-Power Method

For $\lim_{x \to \infty} \frac{P(x)}{Q(x)}$, divide every term by the highest power of $x$ in the **denominator**.

**Why this works:** Terms like $\frac{1}{x}$, $\frac{1}{x^2}$, etc. all approach 0 as $x \to \infty$.

### The Three Cases

Let $n$ = degree of numerator, $m$ = degree of denominator.

**Case 1: $n < m$ (denominator wins)**
$$\lim_{x \to \pm\infty} \frac{P(x)}{Q(x)} = 0$$

The denominator grows faster, pushing the fraction toward zero.

**Case 2: $n = m$ (tie game)**
$$\lim_{x \to \pm\infty} \frac{P(x)}{Q(x)} = \frac{\text{leading coefficient of } P}{\text{leading coefficient of } Q}$$

When the degrees match, the limit is the ratio of leading coefficients.

**Case 3: $n > m$ (numerator wins)**
$$\lim_{x \to \pm\infty} \frac{P(x)}{Q(x)} = \pm\infty$$

The numerator grows faster, so the fraction grows without bound.

### Quick Reference Table

| Numerator Degree | Denominator Degree | Limit at $\pm\infty$ | Horizontal Asymptote |
|------------------|-------------------|---------------------|---------------------|
| Lower | Higher | 0 | $y = 0$ |
| Equal | Equal | Leading coef. ratio | $y = \frac{a_n}{b_m}$ |
| Higher | Lower | $\pm\infty$ | None |

---

## Worked Examples

### Example 1: Basic Polynomial

**Problem:** Find $\lim_{x \to \infty} (5x^3 - 2x^2 + x - 7)$ and $\lim_{x \to -\infty} (5x^3 - 2x^2 + x - 7)$

**Solution:**

The leading term is $5x^3$.

**As $x \to \infty$:**
Since the coefficient is positive and the degree is odd:
$$\lim_{x \to \infty} (5x^3 - 2x^2 + x - 7) = +\infty$$

**As $x \to -\infty$:**
For odd degree with positive leading coefficient, the left end goes down:
$$\lim_{x \to -\infty} (5x^3 - 2x^2 + x - 7) = -\infty$$

---

### Example 2: Rational Function (Degrees Equal)

**Problem:** Find $\lim_{x \to \infty} \frac{4x^2 - 3x + 1}{2x^2 + 5x - 2}$

**Solution:**

Both polynomials have degree 2, so we divide every term by $x^2$:

$$\lim_{x \to \infty} \frac{4x^2 - 3x + 1}{2x^2 + 5x - 2} = \lim_{x \to \infty} \frac{\frac{4x^2}{x^2} - \frac{3x}{x^2} + \frac{1}{x^2}}{\frac{2x^2}{x^2} + \frac{5x}{x^2} - \frac{2}{x^2}}$$

$$= \lim_{x \to \infty} \frac{4 - \frac{3}{x} + \frac{1}{x^2}}{2 + \frac{5}{x} - \frac{2}{x^2}}$$

As $x \to \infty$: $\frac{3}{x} \to 0$, $\frac{1}{x^2} \to 0$, $\frac{5}{x} \to 0$, $\frac{2}{x^2} \to 0$

$$= \frac{4 - 0 + 0}{2 + 0 - 0} = \frac{4}{2} = 2$$

**Shortcut:** For equal degrees, just use the ratio of leading coefficients: $\frac{4}{2} = 2$.

---

### Example 3: Rational Function (Numerator Degree Lower)

**Problem:** Find $\lim_{x \to \infty} \frac{3x + 2}{x^3 - 4x + 1}$

**Solution:**

Numerator degree: 1
Denominator degree: 3

Since the denominator has higher degree, the limit is 0.

**Verification using division by $x^3$:**

$$\lim_{x \to \infty} \frac{\frac{3x}{x^3} + \frac{2}{x^3}}{\frac{x^3}{x^3} - \frac{4x}{x^3} + \frac{1}{x^3}} = \lim_{x \to \infty} \frac{\frac{3}{x^2} + \frac{2}{x^3}}{1 - \frac{4}{x^2} + \frac{1}{x^3}} = \frac{0 + 0}{1 - 0 + 0} = 0$$

---

### Example 4: Rational Function (Numerator Degree Higher)

**Problem:** Find $\lim_{x \to \infty} \frac{x^3 + 2x}{x^2 - 1}$

**Solution:**

Numerator degree: 3
Denominator degree: 2

Since the numerator has higher degree, the limit is $\pm\infty$.

Divide by $x^2$:

$$\lim_{x \to \infty} \frac{x^3 + 2x}{x^2 - 1} = \lim_{x \to \infty} \frac{x + \frac{2}{x}}{1 - \frac{1}{x^2}} = \frac{\infty + 0}{1 - 0} = +\infty$$

As $x \to \infty$, the numerator grows without bound while the denominator approaches 1.

---

### Example 5: Difference of Polynomials with Same Degree

**Problem:** Find $\lim_{x \to \infty} (\sqrt{x^2 + 3x} - x)$

**Solution:**

This appears to be $\infty - \infty$, which is indeterminate. We need algebraic manipulation.

**Rationalize by multiplying by the conjugate:**

$$\lim_{x \to \infty} (\sqrt{x^2 + 3x} - x) \cdot \frac{\sqrt{x^2 + 3x} + x}{\sqrt{x^2 + 3x} + x}$$

$$= \lim_{x \to \infty} \frac{(x^2 + 3x) - x^2}{\sqrt{x^2 + 3x} + x}$$

$$= \lim_{x \to \infty} \frac{3x}{\sqrt{x^2 + 3x} + x}$$

Now divide numerator and denominator by $x$ (note: for $x > 0$, $\sqrt{x^2} = x$):

$$= \lim_{x \to \infty} \frac{3}{\frac{\sqrt{x^2 + 3x}}{x} + 1}$$

$$= \lim_{x \to \infty} \frac{3}{\sqrt{\frac{x^2 + 3x}{x^2}} + 1}$$

$$= \lim_{x \to \infty} \frac{3}{\sqrt{1 + \frac{3}{x}} + 1}$$

$$= \frac{3}{\sqrt{1 + 0} + 1} = \frac{3}{1 + 1} = \frac{3}{2}$$

---

### Example 6: Exponential Functions

**Problem:** Find $\lim_{x \to \infty} e^{-x}$ and $\lim_{x \to -\infty} e^{-x}$

**Solution:**

Recall that $e^{-x} = \frac{1}{e^x}$.

**As $x \to \infty$:**
$e^x$ grows without bound, so $\frac{1}{e^x} \to 0$:
$$\lim_{x \to \infty} e^{-x} = 0$$

**As $x \to -\infty$:**
Let $x = -t$ where $t \to \infty$. Then $e^{-x} = e^{-(-t)} = e^t \to \infty$:
$$\lim_{x \to -\infty} e^{-x} = +\infty$$

---

### Example 7: Rational Function as $x \to -\infty$

**Problem:** Find $\lim_{x \to -\infty} \frac{2x^3 - x}{5x^3 + 3}$

**Solution:**

Both have degree 3, so the limit is the ratio of leading coefficients:

$$\lim_{x \to -\infty} \frac{2x^3 - x}{5x^3 + 3} = \frac{2}{5}$$

Note: For rational functions where degrees are equal, the limit is the same for $x \to \infty$ and $x \to -\infty$.

---

### Example 8: Radical in Denominator

**Problem:** Find $\lim_{x \to \infty} \frac{x}{\sqrt{x^2 + 4}}$

**Solution:**

Divide numerator and denominator by $x$ (for $x > 0$):

$$\lim_{x \to \infty} \frac{x}{\sqrt{x^2 + 4}} = \lim_{x \to \infty} \frac{\frac{x}{x}}{\frac{\sqrt{x^2 + 4}}{x}}$$

For $x > 0$: $\frac{\sqrt{x^2 + 4}}{x} = \frac{\sqrt{x^2 + 4}}{\sqrt{x^2}} = \sqrt{\frac{x^2 + 4}{x^2}} = \sqrt{1 + \frac{4}{x^2}}$

$$= \lim_{x \to \infty} \frac{1}{\sqrt{1 + \frac{4}{x^2}}} = \frac{1}{\sqrt{1 + 0}} = 1$$

---

### Example 9: What About $x \to -\infty$ with Radicals?

**Problem:** Find $\lim_{x \to -\infty} \frac{x}{\sqrt{x^2 + 4}}$

**Solution:**

**Critical point:** When $x < 0$, we have $\sqrt{x^2} = |x| = -x$ (not $x$).

Divide by $|x| = -x$ (since $x < 0$):

$$\lim_{x \to -\infty} \frac{x}{\sqrt{x^2 + 4}} = \lim_{x \to -\infty} \frac{\frac{x}{-x}}{\frac{\sqrt{x^2 + 4}}{-x}}$$

$$= \lim_{x \to -\infty} \frac{-1}{\sqrt{\frac{x^2 + 4}{x^2}}} = \lim_{x \to -\infty} \frac{-1}{\sqrt{1 + \frac{4}{x^2}}}$$

$$= \frac{-1}{\sqrt{1 + 0}} = -1$$

**Key insight:** The function $\frac{x}{\sqrt{x^2 + 4}}$ has two different horizontal asymptotes: $y = 1$ as $x \to \infty$ and $y = -1$ as $x \to -\infty$.

---

### Example 10: Exponential vs. Polynomial

**Problem:** Find $\lim_{x \to \infty} \frac{x^{100}}{e^x}$

**Solution:**

This is a competition between polynomial growth ($x^{100}$) and exponential growth ($e^x$).

**Exponential always wins.**

Even though $x^{100}$ seems enormous, $e^x$ eventually grows faster than any polynomial.

$$\lim_{x \to \infty} \frac{x^{100}}{e^x} = 0$$

**Hierarchy of growth rates (slowest to fastest):**
1. Logarithmic: $\ln x$
2. Polynomial: $x^n$ for any $n > 0$
3. Exponential: $e^x$

For large $x$: $\ln x \ll x^n \ll e^x$

---

## Special Limits to Know

### Fundamental Limits at Infinity

| Limit | Value | Notes |
|-------|-------|-------|
| $\lim_{x \to \infty} \frac{1}{x^n}$ | $0$ | For any $n > 0$ |
| $\lim_{x \to \infty} e^{-x}$ | $0$ | Exponential decay |
| $\lim_{x \to -\infty} e^{x}$ | $0$ | Same function, different direction |
| $\lim_{x \to \infty} e^x$ | $+\infty$ | Exponential growth |
| $\lim_{x \to \infty} \ln x$ | $+\infty$ | Grows, but slowly |
| $\lim_{x \to \infty} \frac{\ln x}{x}$ | $0$ | $x$ dominates $\ln x$ |
| $\lim_{x \to \infty} \arctan x$ | $\frac{\pi}{2}$ | Horizontal asymptote |
| $\lim_{x \to -\infty} \arctan x$ | $-\frac{\pi}{2}$ | Horizontal asymptote |

---

## Practice Problems

### Basic Problems (1-5)

**1.** Find:
$$\lim_{x \to \infty} (3x^4 - 2x^2 + 5)$$

---

**2.** Find:
$$\lim_{x \to -\infty} (-2x^5 + x^3 - 1)$$

---

**3.** Evaluate:
$$\lim_{x \to \infty} \frac{5x + 3}{2x - 1}$$

---

**4.** Find:
$$\lim_{x \to \infty} \frac{x^2}{x^3 + 1}$$

---

**5.** Evaluate:
$$\lim_{x \to \infty} \frac{3x^3 + x}{x^2 - 4}$$

---

### Intermediate Problems (6-10)

**6.** Find both:
$$\lim_{x \to \infty} \frac{2x^2 - 5x + 1}{3x^2 + x - 7} \quad \text{and} \quad \lim_{x \to -\infty} \frac{2x^2 - 5x + 1}{3x^2 + x - 7}$$

---

**7.** Evaluate:
$$\lim_{x \to \infty} \frac{x + 2}{\sqrt{x^2 + 1}}$$

---

**8.** Find:
$$\lim_{x \to -\infty} \frac{x + 2}{\sqrt{x^2 + 1}}$$

---

**9.** Evaluate:
$$\lim_{x \to \infty} (\sqrt{x^2 + x} - x)$$

---

**10.** Find:
$$\lim_{x \to \infty} \frac{e^x - e^{-x}}{e^x + e^{-x}}$$

---

### Advanced Problems (11-15)

**11.** Find:
$$\lim_{x \to \infty} \frac{\sqrt{9x^2 + 1}}{x + 1}$$

---

**12.** Evaluate:
$$\lim_{x \to -\infty} \frac{\sqrt{9x^2 + 1}}{x + 1}$$

---

**13.** Find:
$$\lim_{x \to \infty} \left( \sqrt{x^2 + 4x} - \sqrt{x^2 - 2x} \right)$$

---

**14.** Evaluate:
$$\lim_{x \to \infty} x \left( \sqrt{1 + \frac{1}{x}} - 1 \right)$$

---

**15.** Find:
$$\lim_{x \to \infty} \frac{x^2 \cdot 2^x}{3^x}$$

---

### Challenge Problems (16-18)

**16.** Find:
$$\lim_{x \to \infty} \frac{\sqrt{x + \sqrt{x + \sqrt{x}}}}{x}$$

---

**17.** Evaluate:
$$\lim_{x \to \infty} \left( \sqrt[3]{x^3 + x^2} - x \right)$$

---

**18.** Find both horizontal asymptotes of:
$$f(x) = \frac{2x + 3}{\sqrt{4x^2 + 1}}$$

---

## Solutions to Practice Problems

### Solution 1

The leading term is $3x^4$ (positive coefficient, even degree).

$$\lim_{x \to \infty} (3x^4 - 2x^2 + 5) = +\infty$$

---

### Solution 2

The leading term is $-2x^5$ (negative coefficient, odd degree).

For odd degree with negative leading coefficient:
- As $x \to \infty$: goes to $-\infty$
- As $x \to -\infty$: goes to $+\infty$

$$\lim_{x \to -\infty} (-2x^5 + x^3 - 1) = +\infty$$

---

### Solution 3

Both numerator and denominator have degree 1. Use ratio of leading coefficients:

$$\lim_{x \to \infty} \frac{5x + 3}{2x - 1} = \frac{5}{2}$$

**Verification:**
$$\lim_{x \to \infty} \frac{5 + \frac{3}{x}}{2 - \frac{1}{x}} = \frac{5 + 0}{2 - 0} = \frac{5}{2}$$

---

### Solution 4

Numerator degree: 2
Denominator degree: 3

Since denominator has higher degree:

$$\lim_{x \to \infty} \frac{x^2}{x^3 + 1} = 0$$

---

### Solution 5

Numerator degree: 3
Denominator degree: 2

Since numerator has higher degree:

$$\lim_{x \to \infty} \frac{3x^3 + x}{x^2 - 4} = +\infty$$

(Both leading coefficients are positive, so the limit is $+\infty$.)

---

### Solution 6

Both have degree 2, so use the ratio of leading coefficients:

$$\lim_{x \to \infty} \frac{2x^2 - 5x + 1}{3x^2 + x - 7} = \frac{2}{3}$$

$$\lim_{x \to -\infty} \frac{2x^2 - 5x + 1}{3x^2 + x - 7} = \frac{2}{3}$$

For rational functions with equal degrees, the limit is the same in both directions.

---

### Solution 7

Divide by $x$ (for $x > 0$, $\sqrt{x^2} = x$):

$$\lim_{x \to \infty} \frac{x + 2}{\sqrt{x^2 + 1}} = \lim_{x \to \infty} \frac{1 + \frac{2}{x}}{\sqrt{1 + \frac{1}{x^2}}}$$

$$= \frac{1 + 0}{\sqrt{1 + 0}} = \frac{1}{1} = 1$$

---

### Solution 8

For $x < 0$: $\sqrt{x^2} = |x| = -x$

Divide by $-x$:

$$\lim_{x \to -\infty} \frac{x + 2}{\sqrt{x^2 + 1}} = \lim_{x \to -\infty} \frac{\frac{x + 2}{-x}}{\frac{\sqrt{x^2 + 1}}{-x}}$$

$$= \lim_{x \to -\infty} \frac{-1 - \frac{2}{x}}{\sqrt{1 + \frac{1}{x^2}}}$$

$$= \frac{-1 - 0}{\sqrt{1 + 0}} = \frac{-1}{1} = -1$$

---

### Solution 9

Rationalize:

$$\lim_{x \to \infty} (\sqrt{x^2 + x} - x) \cdot \frac{\sqrt{x^2 + x} + x}{\sqrt{x^2 + x} + x}$$

$$= \lim_{x \to \infty} \frac{x^2 + x - x^2}{\sqrt{x^2 + x} + x} = \lim_{x \to \infty} \frac{x}{\sqrt{x^2 + x} + x}$$

Divide by $x$:

$$= \lim_{x \to \infty} \frac{1}{\sqrt{1 + \frac{1}{x}} + 1} = \frac{1}{\sqrt{1} + 1} = \frac{1}{2}$$

---

### Solution 10

Divide numerator and denominator by $e^x$:

$$\lim_{x \to \infty} \frac{e^x - e^{-x}}{e^x + e^{-x}} = \lim_{x \to \infty} \frac{1 - e^{-2x}}{1 + e^{-2x}}$$

As $x \to \infty$, $e^{-2x} \to 0$:

$$= \frac{1 - 0}{1 + 0} = 1$$

Note: This is actually $\tanh(x)$, and $\lim_{x \to \infty} \tanh x = 1$.

---

### Solution 11

For $x > 0$: $\sqrt{9x^2} = 3x$

$$\lim_{x \to \infty} \frac{\sqrt{9x^2 + 1}}{x + 1} = \lim_{x \to \infty} \frac{\sqrt{9 + \frac{1}{x^2}}}{1 + \frac{1}{x}}$$

$$= \frac{\sqrt{9 + 0}}{1 + 0} = \frac{3}{1} = 3$$

---

### Solution 12

For $x < 0$: $\sqrt{9x^2} = |3x| = -3x$

$$\lim_{x \to -\infty} \frac{\sqrt{9x^2 + 1}}{x + 1}$$

Divide by $-x$ (which is positive when $x < 0$):

$$= \lim_{x \to -\infty} \frac{\frac{\sqrt{9x^2 + 1}}{-x}}{\frac{x + 1}{-x}}$$

$$= \lim_{x \to -\infty} \frac{\sqrt{9 + \frac{1}{x^2}}}{-1 - \frac{1}{x}}$$

$$= \frac{\sqrt{9 + 0}}{-1 - 0} = \frac{3}{-1} = -3$$

---

### Solution 13

Rationalize:

$$\lim_{x \to \infty} \frac{(x^2 + 4x) - (x^2 - 2x)}{\sqrt{x^2 + 4x} + \sqrt{x^2 - 2x}}$$

$$= \lim_{x \to \infty} \frac{6x}{\sqrt{x^2 + 4x} + \sqrt{x^2 - 2x}}$$

Divide by $x$:

$$= \lim_{x \to \infty} \frac{6}{\sqrt{1 + \frac{4}{x}} + \sqrt{1 - \frac{2}{x}}}$$

$$= \frac{6}{\sqrt{1} + \sqrt{1}} = \frac{6}{2} = 3$$

---

### Solution 14

Rationalize by multiplying by $\frac{\sqrt{1 + \frac{1}{x}} + 1}{\sqrt{1 + \frac{1}{x}} + 1}$:

$$\lim_{x \to \infty} x \cdot \frac{\left(1 + \frac{1}{x}\right) - 1}{\sqrt{1 + \frac{1}{x}} + 1}$$

$$= \lim_{x \to \infty} x \cdot \frac{\frac{1}{x}}{\sqrt{1 + \frac{1}{x}} + 1}$$

$$= \lim_{x \to \infty} \frac{1}{\sqrt{1 + \frac{1}{x}} + 1}$$

$$= \frac{1}{\sqrt{1} + 1} = \frac{1}{2}$$

---

### Solution 15

Rewrite:

$$\lim_{x \to \infty} \frac{x^2 \cdot 2^x}{3^x} = \lim_{x \to \infty} x^2 \cdot \left(\frac{2}{3}\right)^x$$

Since $\frac{2}{3} < 1$, we have $\left(\frac{2}{3}\right)^x \to 0$ as $x \to \infty$.

Exponential decay beats polynomial growth:

$$= 0$$

---

### Solution 16

Factor out $x$ from under the outermost radical:

$$\lim_{x \to \infty} \frac{\sqrt{x + \sqrt{x + \sqrt{x}}}}{x}$$

For large $x$, $\sqrt{x + \sqrt{x}} \approx \sqrt{x}$ and $\sqrt{x + \sqrt{x + \sqrt{x}}} \approx \sqrt{x}$.

More rigorously, divide inside by $x$:

$$= \lim_{x \to \infty} \frac{\sqrt{x\left(1 + \frac{\sqrt{x + \sqrt{x}}}{x}\right)}}{x}$$

$$= \lim_{x \to \infty} \frac{\sqrt{x} \cdot \sqrt{1 + \frac{\sqrt{x + \sqrt{x}}}{x}}}{x}$$

$$= \lim_{x \to \infty} \frac{\sqrt{1 + \frac{\sqrt{x + \sqrt{x}}}{x}}}{\sqrt{x}}$$

As $x \to \infty$, $\frac{\sqrt{x + \sqrt{x}}}{x} \to 0$:

$$= \lim_{x \to \infty} \frac{\sqrt{1}}{\sqrt{x}} = 0$$

---

### Solution 17

Let $y = \sqrt[3]{x^3 + x^2} - x$. Multiply by the conjugate for cube roots:

Using $(a - b)(a^2 + ab + b^2) = a^3 - b^3$:

$$y = \frac{(x^3 + x^2) - x^3}{(\sqrt[3]{x^3 + x^2})^2 + x\sqrt[3]{x^3 + x^2} + x^2}$$

$$= \frac{x^2}{(\sqrt[3]{x^3 + x^2})^2 + x\sqrt[3]{x^3 + x^2} + x^2}$$

For large $x$: $\sqrt[3]{x^3 + x^2} \approx x$

$$\lim_{x \to \infty} \frac{x^2}{x^2 + x^2 + x^2} = \frac{x^2}{3x^2} = \frac{1}{3}$$

---

### Solution 18

**As $x \to \infty$:**

For $x > 0$: $\sqrt{4x^2} = 2x$

$$\lim_{x \to \infty} \frac{2x + 3}{\sqrt{4x^2 + 1}} = \lim_{x \to \infty} \frac{2 + \frac{3}{x}}{\sqrt{4 + \frac{1}{x^2}}} = \frac{2}{2} = 1$$

**As $x \to -\infty$:**

For $x < 0$: $\sqrt{4x^2} = |2x| = -2x$

$$\lim_{x \to -\infty} \frac{2x + 3}{\sqrt{4x^2 + 1}} = \lim_{x \to -\infty} \frac{2 + \frac{3}{x}}{-\sqrt{4 + \frac{1}{x^2}}} = \frac{2}{-2} = -1$$

**Horizontal asymptotes:** $y = 1$ and $y = -1$

---

## AP Exam Tips

### Quick Recognition Strategies

**For Rational Functions:**
1. Compare degrees immediately
2. If equal, write down the ratio of leading coefficients
3. If different, determine 0 or $\pm\infty$

**For Radicals:**
1. Remember $\sqrt{x^2} = |x|$, not $x$
2. For $x \to -\infty$, use $\sqrt{x^2} = -x$
3. The sign matters!

**For Indeterminate Forms:**
1. $\infty - \infty$: Rationalize or find common denominator
2. $\frac{\infty}{\infty}$: Divide by highest power in denominator
3. $0 \cdot \infty$: Rewrite as a fraction

### Common Mistakes to Avoid

**Mistake 1: Forgetting $\sqrt{x^2} = |x|$**

Wrong: $\lim_{x \to -\infty} \frac{x}{\sqrt{x^2}} = 1$

Right: $\lim_{x \to -\infty} \frac{x}{\sqrt{x^2}} = \lim_{x \to -\infty} \frac{x}{|x|} = \lim_{x \to -\infty} \frac{x}{-x} = -1$

**Mistake 2: Wrong application of degree comparison**

When degrees are equal, the limit is the ratio of leading coefficients, NOT 1.

**Mistake 3: Ignoring the sign of infinity**

For $\lim_{x \to \infty} \frac{-3x^3}{x^2}$, the answer is $-\infty$, not $\infty$.

**Mistake 4: Not rationalizing $\infty - \infty$ forms**

$\sqrt{x^2 + 1} - x$ as $x \to \infty$ is NOT zero. You must rationalize.

### Hierarchy of Growth Rates

From slowest to fastest:

$$(\ln x)^n \ll x^a \ll x^b \ll b^x \ll x! \ll x^x$$

where $0 < a < b$ and $b > 1$.

For the AP exam, remember:
- **Logarithms grow slowest**
- **Polynomials beat logarithms**
- **Exponentials beat polynomials**

### Horizontal Asymptote Summary

| Function Type | Horizontal Asymptote(s) |
|---------------|------------------------|
| Polynomial | None (unless constant) |
| Rational (num < denom) | $y = 0$ |
| Rational (num = denom) | $y = \frac{a_n}{b_n}$ |
| Rational (num > denom) | None |
| $e^{-x}$ | $y = 0$ (as $x \to \infty$) |
| $\arctan x$ | $y = \pm\frac{\pi}{2}$ |

---

## Connection to Other Topics

### Limits at Infinity and Continuity

A function can be continuous everywhere but still have limits at infinity. For example, $f(x) = \frac{1}{1 + x^2}$ is continuous on all of $\mathbb{R}$, but $\lim_{x \to \pm\infty} f(x) = 0$.

### Looking Ahead: L'Hôpital's Rule

In Unit 3, you'll learn L'Hôpital's Rule, which provides another method for evaluating limits at infinity when you have indeterminate forms like $\frac{\infty}{\infty}$.

### End Behavior and Curve Sketching

Understanding limits at infinity is essential for sketching curves. The horizontal asymptotes tell you what the "tails" of the graph look like as they extend infinitely far left or right.

---

## Summary

Limits at infinity describe the **end behavior** of functions:

- **$\lim_{x \to \infty} f(x) = L$** means $f(x)$ approaches $L$ as $x$ increases without bound
- **$\lim_{x \to -\infty} f(x) = L$** means $f(x)$ approaches $L$ as $x$ decreases without bound
- **Horizontal asymptotes** occur at $y = L$ when these limits exist

**Key techniques:**
- **Dominant term strategy:** For polynomials, only the leading term matters
- **Degree comparison:** For rational functions, compare numerator and denominator degrees
- **Divide by highest power:** Simplify fractions by dividing all terms by $x^n$
- **Rationalization:** Handle $\infty - \infty$ forms by multiplying by conjugates
- **Sign awareness:** Remember $\sqrt{x^2} = |x|$, which is $-x$ when $x < 0$

**Growth rate hierarchy:** Logarithms < Polynomials < Exponentials

Mastering limits at infinity prepares you for understanding horizontal asymptotes in curve sketching, improper integrals, and the behavior of sequences and series!

---

**Next Topics to Explore:**
- Continuity and the Formal Definition
- Types of Discontinuities
- Intermediate Value Theorem

---

<div align="center">

[← One-Sided Limits](calculus/one-sided-limits.md) | [Continuity Basics →](calculus/continuity-definition.md)

</div>
