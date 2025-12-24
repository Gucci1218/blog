# Types of Discontinuities

## Learning Objectives

By the end of this article, you will be able to:

- Identify and classify the three main types of discontinuities
- Distinguish between removable, jump, and infinite discontinuities
- Determine the type of discontinuity from a graph or equation
- "Remove" a removable discontinuity by redefining the function
- Connect discontinuity types to one-sided limits
- Analyze piecewise functions for discontinuity classification
- Solve AP Calculus problems involving discontinuity identification

---

## The Core Concept: Not All Discontinuities Are Created Equal

### The Intuition

When a function fails to be continuous at a point, something goes wrong with our "pencil test"—we have to lift the pencil. But *how* we have to lift it differs:

1. **Removable Discontinuity:** A tiny hole in the graph. You lift your pencil just for an instant to skip over a single missing point.

2. **Jump Discontinuity:** The graph suddenly jumps to a different height. You lift your pencil and move it up or down to continue drawing.

3. **Infinite Discontinuity:** The graph shoots off toward infinity. You'd have to lift your pencil and move it infinitely far away.

**Real-world analogies:**

| Type | Analogy |
|------|---------|
| Removable | A pothole in an otherwise smooth road—fixable |
| Jump | A staircase—discrete jumps between levels |
| Infinite | A cliff edge—the ground drops away infinitely |

### The Classification System

Every discontinuity falls into one of three categories based on what happens to the limit:

```
                    Does lim f(x) exist?
                     x→a
                    /              \
                  Yes               No
                   |                 |
            Is lim = f(a)?    Why doesn't it exist?
               /      \           /            \
             Yes       No    One-sided      At least one
              |        |     limits         one-sided limit
         CONTINUOUS  REMOVABLE  differ         is ±∞
                                  |              |
                               JUMP          INFINITE
```

---

## Type 1: Removable Discontinuities

### Definition

A function $f$ has a **removable discontinuity** at $x = a$ if:

$$\lim_{x \to a} f(x) \text{ exists, but either } f(a) \text{ is undefined or } f(a) \neq \lim_{x \to a} f(x)$$

### Why "Removable"?

We call it removable because we can "fix" the function by defining (or redefining) $f(a)$ to equal the limit. This fills in the hole and makes the function continuous.

### Visual Representation

```
     |                          |
   3 |      ○                 3 |      ●
     |     / \                  |     / \
   2 |    /   \               2 |    /   \
     |   /     \                |   /     \
   1 |  /       \             1 |  /       \
     |_/____●____\____          |_/         \____
          2                          2

   Hole at (2, 3)              Point at (2, 1)
   f(2) undefined              f(2) = 1 ≠ lim = 3
```

Both are removable discontinuities—the limit exists in both cases.

### Classic Example: The Cancelable Factor

$$f(x) = \frac{x^2 - 4}{x - 2}$$

**Analysis:**

Factor the numerator:
$$f(x) = \frac{(x-2)(x+2)}{x-2} = x + 2 \quad \text{for } x \neq 2$$

- $f(2)$ is undefined (division by zero)
- $\lim_{x \to 2} f(x) = \lim_{x \to 2} (x + 2) = 4$ (exists!)
- The limit exists but the function is undefined

**Conclusion:** Removable discontinuity at $x = 2$

**How to remove it:** Define $g(x) = \begin{cases} \frac{x^2-4}{x-2} & x \neq 2 \\ 4 & x = 2 \end{cases}$

Now $g$ is continuous at $x = 2$!

### Recognizing Removable Discontinuities

**From an equation:**
- Look for factors that cancel in numerator and denominator
- The $\frac{0}{0}$ indeterminate form often indicates removable discontinuity
- If $\lim_{x \to a} f(x)$ exists but $f(a)$ is undefined or different

**From a graph:**
- A single hole (open circle) with or without a point elsewhere
- The graph approaches the same height from both sides

---

## Type 2: Jump Discontinuities

### Definition

A function $f$ has a **jump discontinuity** at $x = a$ if:

$$\lim_{x \to a^-} f(x) \text{ and } \lim_{x \to a^+} f(x) \text{ both exist, but } \lim_{x \to a^-} f(x) \neq \lim_{x \to a^+} f(x)$$

The one-sided limits exist but aren't equal, so the two-sided limit doesn't exist.

### Why "Jump"?

The function literally "jumps" from one value to another at the discontinuity. There's a gap between where the left side ends and the right side begins.

### Visual Representation

```
     |
   4 |         ●----
   3 |         |
   2 |    ----○
   1 |
     |________________
          2

   Jump from 2 to 4 at x = 2
```

### The Size of the Jump

The **jump** is the difference between the one-sided limits:

$$\text{Jump} = \left| \lim_{x \to a^+} f(x) - \lim_{x \to a^-} f(x) \right|$$

### Classic Examples

**Example 1: Piecewise Function**

$$f(x) = \begin{cases} x + 1 & \text{if } x < 2 \\ x^2 & \text{if } x \geq 2 \end{cases}$$

At $x = 2$:
- Left limit: $\lim_{x \to 2^-} (x + 1) = 3$
- Right limit: $\lim_{x \to 2^+} x^2 = 4$
- $3 \neq 4$, so **jump discontinuity**
- Jump size: $|4 - 3| = 1$

**Example 2: The Sign Function**

$$\text{sgn}(x) = \begin{cases} -1 & \text{if } x < 0 \\ 0 & \text{if } x = 0 \\ 1 & \text{if } x > 0 \end{cases}$$

At $x = 0$:
- Left limit: $-1$
- Right limit: $1$
- Jump discontinuity with jump size 2

**Example 3: Floor Function**

$$f(x) = \lfloor x \rfloor$$

At every integer $n$:
- Left limit: $n - 1$
- Right limit: $n$
- Jump discontinuity at every integer

### Recognizing Jump Discontinuities

**From an equation:**
- Piecewise functions where pieces don't connect
- Step functions (floor, ceiling)
- Functions involving $|x|/x$ or similar sign-changing expressions

**From a graph:**
- A visible "jump" or gap between two pieces
- Open circle on one side, closed circle at a different height
- The two parts of the graph don't meet

---

## Type 3: Infinite Discontinuities

### Definition

A function $f$ has an **infinite discontinuity** at $x = a$ if:

$$\lim_{x \to a^-} f(x) = \pm\infty \quad \text{or} \quad \lim_{x \to a^+} f(x) = \pm\infty$$

At least one of the one-sided limits is infinite.

### Connection to Vertical Asymptotes

Infinite discontinuities occur at **vertical asymptotes**. The graph approaches a vertical line but never crosses it.

### Visual Representation

```
     |       |                    |       |
     |   \   |   /                |   \   |
     |    \  |  /                 |    \  |
     |     \ | /                  |     \ |   /
     |      \|/                   |      \|  /
     |_______↓________            |_______↓_/______
            a                            a

   Both sides → -∞             Left → -∞, Right → +∞
```

### Classic Examples

**Example 1: Simple Reciprocal**

$$f(x) = \frac{1}{x}$$

At $x = 0$:
- $\lim_{x \to 0^-} \frac{1}{x} = -\infty$
- $\lim_{x \to 0^+} \frac{1}{x} = +\infty$
- **Infinite discontinuity** at $x = 0$

**Example 2: Squared Reciprocal**

$$g(x) = \frac{1}{x^2}$$

At $x = 0$:
- $\lim_{x \to 0^-} \frac{1}{x^2} = +\infty$
- $\lim_{x \to 0^+} \frac{1}{x^2} = +\infty$
- **Infinite discontinuity** (both sides go to $+\infty$)

**Example 3: Rational Function**

$$h(x) = \frac{x + 1}{x^2 - 4} = \frac{x + 1}{(x-2)(x+2)}$$

At $x = 2$:
- Numerator: $2 + 1 = 3 \neq 0$
- Denominator: $0$
- This is $\frac{3}{0}$, not $\frac{0}{0}$
- **Infinite discontinuity** at $x = 2$

At $x = -2$:
- Numerator: $-2 + 1 = -1 \neq 0$
- Denominator: $0$
- **Infinite discontinuity** at $x = -2$

### The Key Distinction: $\frac{0}{0}$ vs. $\frac{c}{0}$

| Form at $x = a$ | Meaning | Type of Discontinuity |
|-----------------|---------|----------------------|
| $\frac{0}{0}$ | Indeterminate—need more analysis | Usually removable |
| $\frac{c}{0}$ where $c \neq 0$ | Infinite | Always infinite |

### Recognizing Infinite Discontinuities

**From an equation:**
- Denominator equals zero AND numerator doesn't equal zero
- Functions like $\tan x$, $\sec x$, $\csc x$, $\cot x$ at their undefined points
- Logarithms approaching zero: $\ln x$ as $x \to 0^+$

**From a graph:**
- The graph shoots up or down toward infinity
- A vertical asymptote is present
- The curve gets arbitrarily close to a vertical line

---

## Comparison Table

| Feature | Removable | Jump | Infinite |
|---------|-----------|------|----------|
| $\lim_{x \to a} f(x)$ | Exists | DNE | DNE |
| $\lim_{x \to a^-} f(x)$ | Equals $\lim_{x \to a^+}$ | Exists, finite | May be $\pm\infty$ |
| $\lim_{x \to a^+} f(x)$ | Equals $\lim_{x \to a^-}$ | Exists, finite | May be $\pm\infty$ |
| Graph appearance | Hole | Jump/gap | Vertical asymptote |
| Can be "fixed"? | Yes | No | No |
| Typical cause | $\frac{0}{0}$ form | Piecewise mismatch | $\frac{c}{0}$ form |

---

## Worked Examples

### Example 1: Classifying from a Rational Function

**Problem:** Classify all discontinuities of $f(x) = \frac{x^2 - x - 6}{x^2 - 9}$.

**Solution:**

Factor both numerator and denominator:
$$f(x) = \frac{(x-3)(x+2)}{(x-3)(x+3)}$$

Discontinuities occur where the denominator is zero: $x = 3$ and $x = -3$.

**At $x = 3$:**

The factor $(x - 3)$ cancels:
$$\lim_{x \to 3} f(x) = \lim_{x \to 3} \frac{x + 2}{x + 3} = \frac{5}{6}$$

The limit exists, but $f(3)$ is undefined.

**Classification:** Removable discontinuity at $x = 3$

**At $x = -3$:**

After canceling, we have $f(x) = \frac{x + 2}{x + 3}$ for $x \neq 3$.

$$\lim_{x \to -3} \frac{x + 2}{x + 3} = \frac{-1}{0}$$

This gives $\frac{-1}{0^+} = -\infty$ from the right and $\frac{-1}{0^-} = +\infty$ from the left.

**Classification:** Infinite discontinuity at $x = -3$

---

### Example 2: Piecewise Function Analysis

**Problem:** Classify the discontinuity of $g(x) = \begin{cases} x^2 & \text{if } x < 1 \\ 2x - 1 & \text{if } x \geq 1 \end{cases}$ at $x = 1$.

**Solution:**

**Function value:** $g(1) = 2(1) - 1 = 1$

**Left-hand limit:** $\lim_{x \to 1^-} x^2 = 1$

**Right-hand limit:** $\lim_{x \to 1^+} (2x - 1) = 1$

Both one-sided limits equal 1, so $\lim_{x \to 1} g(x) = 1$.

Also, $g(1) = 1$, so $\lim_{x \to 1} g(x) = g(1)$.

**Classification:** No discontinuity—the function is **continuous** at $x = 1$!

---

### Example 3: Another Piecewise Function

**Problem:** Classify all discontinuities of $h(x) = \begin{cases} x + 3 & \text{if } x < -1 \\ x^2 & \text{if } -1 \leq x < 2 \\ 5 & \text{if } x \geq 2 \end{cases}$

**Solution:**

Check the boundary points: $x = -1$ and $x = 2$.

**At $x = -1$:**
- $h(-1) = (-1)^2 = 1$
- Left: $\lim_{x \to -1^-} (x + 3) = 2$
- Right: $\lim_{x \to -1^+} x^2 = 1$
- $2 \neq 1$, so the two-sided limit doesn't exist

**Classification:** Jump discontinuity at $x = -1$ (jump size = 1)

**At $x = 2$:**
- $h(2) = 5$
- Left: $\lim_{x \to 2^-} x^2 = 4$
- Right: $\lim_{x \to 2^+} 5 = 5$
- $4 \neq 5$, so the two-sided limit doesn't exist

**Classification:** Jump discontinuity at $x = 2$ (jump size = 1)

---

### Example 4: Tangent Function

**Problem:** Classify the discontinuity of $f(x) = \tan x$ at $x = \frac{\pi}{2}$.

**Solution:**

$$\tan x = \frac{\sin x}{\cos x}$$

At $x = \frac{\pi}{2}$:
- $\sin\frac{\pi}{2} = 1 \neq 0$
- $\cos\frac{\pi}{2} = 0$

This is the $\frac{1}{0}$ form, indicating an infinite discontinuity.

Checking the one-sided limits:
- As $x \to \frac{\pi}{2}^-$: $\cos x \to 0^+$, so $\tan x \to +\infty$
- As $x \to \frac{\pi}{2}^+$: $\cos x \to 0^-$, so $\tan x \to -\infty$

**Classification:** Infinite discontinuity at $x = \frac{\pi}{2}$

---

### Example 5: Absolute Value in Denominator

**Problem:** Classify all discontinuities of $f(x) = \frac{x}{|x|}$.

**Solution:**

Rewrite without absolute value:
$$f(x) = \begin{cases} \frac{x}{x} = 1 & \text{if } x > 0 \\ \frac{x}{-x} = -1 & \text{if } x < 0 \end{cases}$$

The function is undefined at $x = 0$.

**At $x = 0$:**
- $f(0)$ is undefined
- Left: $\lim_{x \to 0^-} (-1) = -1$
- Right: $\lim_{x \to 0^+} (1) = 1$
- $-1 \neq 1$

**Classification:** Jump discontinuity at $x = 0$ (jump size = 2)

Note: Even though $f(0)$ is undefined, we classify based on the behavior of the limits. Since both one-sided limits are finite but unequal, it's a jump discontinuity.

---

### Example 6: Determining the Type from $\frac{0}{0}$

**Problem:** Classify the discontinuity of $f(x) = \frac{x^2 - 4x + 3}{x - 1}$ at $x = 1$.

**Solution:**

Check the form at $x = 1$:
- Numerator: $1 - 4 + 3 = 0$
- Denominator: $0$

This is $\frac{0}{0}$, so we need to factor.

$$f(x) = \frac{(x-1)(x-3)}{x-1} = x - 3 \quad \text{for } x \neq 1$$

$$\lim_{x \to 1} f(x) = \lim_{x \to 1} (x - 3) = -2$$

The limit exists.

**Classification:** Removable discontinuity at $x = 1$

---

### Example 7: Mixed Types in One Function

**Problem:** Find and classify all discontinuities of $g(x) = \frac{x^2 - 1}{x^2 - 3x + 2}$.

**Solution:**

Factor:
$$g(x) = \frac{(x-1)(x+1)}{(x-1)(x-2)}$$

Discontinuities at $x = 1$ and $x = 2$.

**At $x = 1$:**

The $(x-1)$ cancels:
$$\lim_{x \to 1} g(x) = \lim_{x \to 1} \frac{x+1}{x-2} = \frac{2}{-1} = -2$$

The limit exists.

**Classification:** Removable discontinuity at $x = 1$

**At $x = 2$:**

After simplifying, $g(x) = \frac{x+1}{x-2}$ for $x \neq 1$.

$$\lim_{x \to 2} \frac{x+1}{x-2} = \frac{3}{0}$$

- From left: $\frac{3}{0^-} = -\infty$
- From right: $\frac{3}{0^+} = +\infty$

**Classification:** Infinite discontinuity at $x = 2$

---

### Example 8: A Tricky Piecewise

**Problem:** Classify the discontinuity at $x = 0$ for:
$$f(x) = \begin{cases} e^{1/x} & \text{if } x > 0 \\ 0 & \text{if } x \leq 0 \end{cases}$$

**Solution:**

**Function value:** $f(0) = 0$

**Left-hand limit:** $\lim_{x \to 0^-} 0 = 0$

**Right-hand limit:**

As $x \to 0^+$, $\frac{1}{x} \to +\infty$, so $e^{1/x} \to +\infty$.

$$\lim_{x \to 0^+} e^{1/x} = +\infty$$

One of the one-sided limits is infinite.

**Classification:** Infinite discontinuity at $x = 0$

---

## Removing Removable Discontinuities

### The Process

To "remove" a removable discontinuity at $x = a$:

1. Find $L = \lim_{x \to a} f(x)$
2. Define a new function: $g(x) = \begin{cases} f(x) & \text{if } x \neq a \\ L & \text{if } x = a \end{cases}$
3. Now $g$ is continuous at $x = a$

### Example

**Original:** $f(x) = \frac{\sin x}{x}$ (undefined at $x = 0$)

**The limit:** $\lim_{x \to 0} \frac{\sin x}{x} = 1$

**Fixed version:** $g(x) = \begin{cases} \frac{\sin x}{x} & \text{if } x \neq 0 \\ 1 & \text{if } x = 0 \end{cases}$

This is called the **sinc function** and is continuous everywhere!

---

## Practice Problems

### Basic Problems (1-5)

**1.** Classify the discontinuity of $f(x) = \frac{x - 3}{x^2 - 9}$ at $x = 3$.

---

**2.** Classify the discontinuity of $g(x) = \frac{1}{(x - 2)^2}$ at $x = 2$.

---

**3.** For $h(x) = \begin{cases} 2x + 1 & \text{if } x < 1 \\ x^2 + 2 & \text{if } x \geq 1 \end{cases}$, classify any discontinuity at $x = 1$.

---

**4.** Classify the discontinuity of $f(x) = \frac{x^2 - 4}{x + 2}$ at $x = -2$.

---

**5.** Classify the discontinuity of $g(x) = \lfloor x \rfloor$ at $x = 3$.

---

### Intermediate Problems (6-10)

**6.** Find and classify all discontinuities of $f(x) = \frac{x^2 - 5x + 6}{x^2 - 4}$.

---

**7.** Classify the discontinuity of $g(x) = \frac{|x - 1|}{x - 1}$ at $x = 1$.

---

**8.** For $h(x) = \begin{cases} \frac{x^2 - 1}{x - 1} & \text{if } x \neq 1 \\ 3 & \text{if } x = 1 \end{cases}$, classify any discontinuity at $x = 1$.

---

**9.** Classify the discontinuity of $f(x) = \csc x$ at $x = \pi$.

---

**10.** Find and classify all discontinuities of $g(x) = \frac{x^3 - 8}{x^2 - 4}$.

---

### Advanced Problems (11-15)

**11.** For $f(x) = \begin{cases} x + 2 & \text{if } x < -1 \\ x^2 & \text{if } -1 \leq x < 1 \\ 2 - x & \text{if } x \geq 1 \end{cases}$, find and classify all discontinuities.

---

**12.** Classify the discontinuity of $g(x) = x \cdot \lfloor \frac{1}{x} \rfloor$ at $x = 0$.

---

**13.** Find all discontinuities of $h(x) = \frac{\tan x}{x}$ on $(-\pi, \pi)$ and classify each.

---

**14.** For what value of $a$ does $f(x) = \begin{cases} \frac{x^2 - 9}{x - 3} & \text{if } x \neq 3 \\ a & \text{if } x = 3 \end{cases}$ have a removable discontinuity that has been removed?

---

**15.** Classify all discontinuities of $g(x) = \frac{1}{1 + e^{1/x}}$ on $\mathbb{R}$.

---

### Challenge Problems (16-18)

**16.** Let $f(x) = \frac{x^3 - x^2 - x + 1}{x^3 - 3x + 2}$. Find and classify all discontinuities.

---

**17.** Define $g(x) = \begin{cases} \sin\left(\frac{1}{x}\right) & \text{if } x \neq 0 \\ 0 & \text{if } x = 0 \end{cases}$. What type of discontinuity (if any) exists at $x = 0$?

---

**18.** Find and classify all discontinuities of $h(x) = \frac{|x^2 - 4|}{x^2 - 4}$ on $\mathbb{R}$.

---

## Solutions to Practice Problems

### Solution 1

$$f(x) = \frac{x - 3}{x^2 - 9} = \frac{x - 3}{(x-3)(x+3)} = \frac{1}{x + 3} \quad \text{for } x \neq 3$$

$$\lim_{x \to 3} f(x) = \lim_{x \to 3} \frac{1}{x + 3} = \frac{1}{6}$$

The limit exists.

**Classification:** Removable discontinuity at $x = 3$

---

### Solution 2

At $x = 2$:
- Numerator: $1 \neq 0$
- Denominator: $0$

This is $\frac{1}{0}$, and since $(x-2)^2 > 0$ for $x \neq 2$:

$$\lim_{x \to 2} \frac{1}{(x-2)^2} = +\infty$$

**Classification:** Infinite discontinuity at $x = 2$

---

### Solution 3

**Function value:** $h(1) = 1^2 + 2 = 3$

**Left-hand limit:** $\lim_{x \to 1^-} (2x + 1) = 3$

**Right-hand limit:** $\lim_{x \to 1^+} (x^2 + 2) = 3$

Since $\lim_{x \to 1} h(x) = 3 = h(1)$:

**Classification:** No discontinuity—$h$ is continuous at $x = 1$

---

### Solution 4

$$f(x) = \frac{x^2 - 4}{x + 2} = \frac{(x-2)(x+2)}{x+2} = x - 2 \quad \text{for } x \neq -2$$

$$\lim_{x \to -2} f(x) = -2 - 2 = -4$$

The limit exists.

**Classification:** Removable discontinuity at $x = -2$

---

### Solution 5

At $x = 3$:
- $\lim_{x \to 3^-} \lfloor x \rfloor = 2$
- $\lim_{x \to 3^+} \lfloor x \rfloor = 3$
- $2 \neq 3$

**Classification:** Jump discontinuity at $x = 3$ (jump size = 1)

---

### Solution 6

$$f(x) = \frac{x^2 - 5x + 6}{x^2 - 4} = \frac{(x-2)(x-3)}{(x-2)(x+2)}$$

Discontinuities at $x = 2$ and $x = -2$.

**At $x = 2$:**
$$\lim_{x \to 2} \frac{x - 3}{x + 2} = \frac{-1}{4}$$
Removable discontinuity

**At $x = -2$:**
$$\lim_{x \to -2} \frac{x - 3}{x + 2} = \frac{-5}{0}$$
Infinite discontinuity

---

### Solution 7

$$g(x) = \frac{|x - 1|}{x - 1} = \begin{cases} 1 & \text{if } x > 1 \\ -1 & \text{if } x < 1 \end{cases}$$

- $\lim_{x \to 1^-} g(x) = -1$
- $\lim_{x \to 1^+} g(x) = 1$
- $-1 \neq 1$

**Classification:** Jump discontinuity at $x = 1$ (jump size = 2)

---

### Solution 8

For $x \neq 1$:
$$h(x) = \frac{(x-1)(x+1)}{x-1} = x + 1$$

$$\lim_{x \to 1} h(x) = 2$$

But $h(1) = 3 \neq 2$.

**Classification:** Removable discontinuity at $x = 1$

---

### Solution 9

$$\csc x = \frac{1}{\sin x}$$

At $x = \pi$:
- $\sin \pi = 0$
- $\frac{1}{0}$ form

As $x \to \pi^-$: $\sin x \to 0^+$, so $\csc x \to +\infty$
As $x \to \pi^+$: $\sin x \to 0^-$, so $\csc x \to -\infty$

**Classification:** Infinite discontinuity at $x = \pi$

---

### Solution 10

$$g(x) = \frac{x^3 - 8}{x^2 - 4} = \frac{(x-2)(x^2 + 2x + 4)}{(x-2)(x+2)}$$

Discontinuities at $x = 2$ and $x = -2$.

**At $x = 2$:**
$$\lim_{x \to 2} \frac{x^2 + 2x + 4}{x + 2} = \frac{12}{4} = 3$$
Removable discontinuity

**At $x = -2$:**
$$\lim_{x \to -2} \frac{x^2 + 2x + 4}{x + 2} = \frac{4}{0}$$
Infinite discontinuity

---

### Solution 11

Check $x = -1$ and $x = 1$.

**At $x = -1$:**
- $f(-1) = (-1)^2 = 1$
- Left: $\lim_{x \to -1^-} (x + 2) = 1$
- Right: $\lim_{x \to -1^+} x^2 = 1$
- $\lim_{x \to -1} f(x) = 1 = f(-1)$

**Continuous** at $x = -1$

**At $x = 1$:**
- $f(1) = 2 - 1 = 1$
- Left: $\lim_{x \to 1^-} x^2 = 1$
- Right: $\lim_{x \to 1^+} (2 - x) = 1$
- $\lim_{x \to 1} f(x) = 1 = f(1)$

**Continuous** at $x = 1$

**Conclusion:** No discontinuities—$f$ is continuous everywhere!

---

### Solution 12

As shown in the one-sided limits article:

$$\lim_{x \to 0^+} x \cdot \lfloor \frac{1}{x} \rfloor = 1$$
$$\lim_{x \to 0^-} x \cdot \lfloor \frac{1}{x} \rfloor = 1$$

Both one-sided limits exist and equal 1. The function is undefined at $x = 0$.

**Classification:** Removable discontinuity at $x = 0$

---

### Solution 13

On $(-\pi, \pi)$:

$\tan x$ is undefined at $x = \pm\frac{\pi}{2}$.

**At $x = 0$:**
$$\lim_{x \to 0} \frac{\tan x}{x} = \lim_{x \to 0} \frac{\sin x}{x \cos x} = 1 \cdot 1 = 1$$
Function undefined at $x = 0$, limit exists.
**Removable discontinuity** at $x = 0$

**At $x = \frac{\pi}{2}$ and $x = -\frac{\pi}{2}$:**
$\tan x \to \pm\infty$, so $\frac{\tan x}{x} \to \pm\infty$.
**Infinite discontinuities** at $x = \pm\frac{\pi}{2}$

---

### Solution 14

$$\lim_{x \to 3} \frac{x^2 - 9}{x - 3} = \lim_{x \to 3} \frac{(x-3)(x+3)}{x-3} = \lim_{x \to 3} (x + 3) = 6$$

For the discontinuity to be removed (i.e., for $f$ to be continuous), we need:
$$f(3) = a = 6$$

**Answer:** $a = 6$

---

### Solution 15

At $x = 0$:
- As $x \to 0^+$: $\frac{1}{x} \to +\infty$, so $e^{1/x} \to +\infty$, thus $g(x) = \frac{1}{1 + \infty} = 0$
- As $x \to 0^-$: $\frac{1}{x} \to -\infty$, so $e^{1/x} \to 0$, thus $g(x) = \frac{1}{1 + 0} = 1$

$$\lim_{x \to 0^-} g(x) = 1 \neq 0 = \lim_{x \to 0^+} g(x)$$

**Classification:** Jump discontinuity at $x = 0$ (jump size = 1)

---

### Solution 16

Factor both polynomials:
- Numerator: $x^3 - x^2 - x + 1 = (x-1)(x-1)(x+1) = (x-1)^2(x+1)$
- Denominator: $x^3 - 3x + 2 = (x-1)(x-1)(x+2) = (x-1)^2(x+2)$

$$f(x) = \frac{(x-1)^2(x+1)}{(x-1)^2(x+2)} = \frac{x+1}{x+2} \quad \text{for } x \neq 1$$

**At $x = 1$:**
$$\lim_{x \to 1} \frac{x+1}{x+2} = \frac{2}{3}$$
**Removable discontinuity**

**At $x = -2$:**
$$\lim_{x \to -2} \frac{x+1}{x+2} = \frac{-1}{0}$$
**Infinite discontinuity**

---

### Solution 17

As $x \to 0$, $\frac{1}{x} \to \pm\infty$, and $\sin\left(\frac{1}{x}\right)$ oscillates between $-1$ and $1$ infinitely often.

The limit $\lim_{x \to 0} \sin\left(\frac{1}{x}\right)$ does not exist—not because it's infinite, but because it oscillates.

This is called an **oscillating discontinuity** or sometimes an **essential discontinuity**. It doesn't fit neatly into the three main categories.

**Note:** Some textbooks classify this under "discontinuity where the limit doesn't exist," but it's neither jump (the one-sided limits don't exist as finite values) nor infinite (it doesn't go to $\pm\infty$).

---

### Solution 18

$$h(x) = \frac{|x^2 - 4|}{x^2 - 4}$$

Note that $x^2 - 4 = (x-2)(x+2)$.

- When $x^2 - 4 > 0$ (i.e., $x < -2$ or $x > 2$): $h(x) = 1$
- When $x^2 - 4 < 0$ (i.e., $-2 < x < 2$): $h(x) = -1$
- When $x = \pm 2$: undefined

**At $x = 2$:**
- $\lim_{x \to 2^-} h(x) = -1$
- $\lim_{x \to 2^+} h(x) = 1$
**Jump discontinuity** (jump size = 2)

**At $x = -2$:**
- $\lim_{x \to -2^-} h(x) = 1$
- $\lim_{x \to -2^+} h(x) = -1$
**Jump discontinuity** (jump size = 2)

---

## AP Exam Tips

### Quick Classification Guide

**Step 1:** Find where the function is undefined or where pieces meet.

**Step 2:** At each point, check:
- Does $\lim_{x \to a^-} f(x)$ exist and is it finite?
- Does $\lim_{x \to a^+} f(x)$ exist and is it finite?

**Step 3:** Classify:

| Left Limit | Right Limit | Classification |
|------------|-------------|----------------|
| Finite $L$ | Finite $L$ (same) | Removable (if $f(a) \neq L$ or undefined) |
| Finite $L_1$ | Finite $L_2$ (different) | Jump |
| $\pm\infty$ | Anything | Infinite |
| Anything | $\pm\infty$ | Infinite |

### Common Exam Patterns

**1. Rational functions:**
- Factor completely
- $\frac{0}{0}$ at a point → likely removable
- $\frac{c}{0}$ at a point → infinite

**2. Piecewise functions:**
- Check all boundary points
- Evaluate both one-sided limits
- Usually jump if limits differ, removable if limit ≠ function value

**3. Trigonometric functions:**
- $\tan x$, $\sec x$: infinite at $\cos x = 0$
- $\cot x$, $\csc x$: infinite at $\sin x = 0$

### What to Write on Free Response

When classifying a discontinuity:

"At $x = 2$, there is a **removable discontinuity** because:
- $\lim_{x \to 2} f(x) = 4$ exists
- But $f(2)$ is undefined (or $f(2) \neq 4$)"

"At $x = 3$, there is a **jump discontinuity** because:
- $\lim_{x \to 3^-} f(x) = 5$
- $\lim_{x \to 3^+} f(x) = 2$
- The one-sided limits are unequal"

"At $x = 0$, there is an **infinite discontinuity** because:
- $\lim_{x \to 0^+} f(x) = +\infty$"

---

## Summary

| Type | Key Feature | Limit Behavior | Fixable? |
|------|-------------|---------------|----------|
| **Removable** | Hole in graph | $\lim_{x \to a} f(x)$ exists | Yes |
| **Jump** | Graph jumps | Left limit ≠ Right limit (both finite) | No |
| **Infinite** | Vertical asymptote | At least one limit is $\pm\infty$ | No |

**Recognition tips:**
- **Removable:** Look for cancelable factors ($\frac{0}{0}$ form)
- **Jump:** Look for piecewise definitions with mismatched values
- **Infinite:** Look for non-cancelable zero in denominator ($\frac{c}{0}$ form)

**Removing a removable discontinuity:**
Define $f(a) = \lim_{x \to a} f(x)$ to "fill the hole"

Understanding discontinuity types is essential for the Intermediate Value Theorem (which requires continuity) and for analyzing where functions behave unexpectedly!

---

**Next Topics to Explore:**
- Continuity with Piecewise Functions
- The Intermediate Value Theorem
- Making Functions Continuous

---

<div align="center">

[← Continuity Basics](calculus/continuity-definition.md) | [Piecewise Continuity →](calculus/continuity-piecewise.md)

</div>
