# One-Sided Limits
<p class="article-date">September 14, 2024</p>

## Learning Objectives

By the end of this article, you will be able to:

- Explain what one-sided limits are and why they're necessary
- Distinguish between left-hand and right-hand limits
- Evaluate one-sided limits graphically and algebraically
- Use one-sided limits to determine if a two-sided limit exists
- Analyze piecewise functions using one-sided limits
- Identify different types of discontinuities using one-sided limits
- Apply one-sided limit concepts to AP Calculus problems

---

## The Core Concept: Why One-Sided Limits Matter

### The Intuition

Imagine you're walking toward a door from two different directions—from the left side of the hallway and from the right side. Even though you're heading to the same door, what you see as you approach might be completely different depending on which direction you're coming from.

One-sided limits work the same way. Sometimes, as we approach a point on a function, the function behaves differently depending on whether we're coming from the left or from the right.

**Real-world example:** Think about a store that has a "buy one get one 50% off" deal. If you buy exactly one item, you pay full price. But the instant you add a second item, the price structure changes. The "cost per item" approaching 1 item from below (0.5, 0.8, 0.99 items) is different from approaching 1 item from above (2 items, 1.5 items, 1.01 items).

### Why Do We Need One-Sided Limits?

Regular (two-sided) limits only exist when a function approaches the same value from both directions. But many real-world functions have **discontinuities**—places where the function "jumps" or has a "break." One-sided limits let us:

1. Analyze what happens on each side of a discontinuity
2. Determine whether a two-sided limit exists
3. Classify different types of discontinuities
4. Work with piecewise functions that have different rules on different intervals

### Formal Definitions

**Left-Hand Limit:**
$$\lim_{x \to a^-} f(x) = L$$

This means: "As $x$ approaches $a$ from the left (from values less than $a$), $f(x)$ approaches $L$."

The little minus sign ($-$) indicates we're approaching from the left (negative direction).

**Right-Hand Limit:**
$$\lim_{x \to a^+} f(x) = L$$

This means: "As $x$ approaches $a$ from the right (from values greater than $a$), $f(x)$ approaches $L$."

The little plus sign ($+$) indicates we're approaching from the right (positive direction).

### The Critical Connection

**For a two-sided limit to exist:**
$$\lim_{x \to a} f(x) = L \text{ if and only if } \lim_{x \to a^-} f(x) = L \text{ and } \lim_{x \to a^+} f(x) = L$$

In plain English: The two-sided limit exists **only when both one-sided limits exist AND are equal**.

---

## Graphical Understanding

### Example 1: Jump Discontinuity

Consider this graph where the function "jumps" at $x = 2$:

```
     |
   4 |         ●---
   3 |         |
   2 |    ---○ |
   1 |         |
     |_________________
         1   2   3
```

At $x = 2$:
- **Left-hand limit:** $\lim_{x \to 2^-} f(x) = 2$ (approaching from left, $y$ approaches 2)
- **Right-hand limit:** $\lim_{x \to 2^+} f(x) = 4$ (approaching from right, $y$ approaches 4)
- **Two-sided limit:** Does NOT exist (left ≠ right)

The hollow circle (○) at $(2, 2)$ and filled circle (●) at $(2, 4)$ show the function has a jump discontinuity.

### Example 2: Removable Discontinuity

```
     |
   3 |      ●
   2 |     / \
   1 |    /   \
     |   /  ○  \
     |_________________
         1   2   3
```

At $x = 2$:
- **Left-hand limit:** $\lim_{x \to 2^-} f(x) = 0$
- **Right-hand limit:** $\lim_{x \to 2^+} f(x) = 0$
- **Two-sided limit:** $\lim_{x \to 2} f(x) = 0$ (exists! Both sides agree)

Even though $f(2) = 3$ (the filled dot), the limit exists because both one-sided limits equal 0.

---

## Algebraic Evaluation

### Strategy 1: Direct Substitution (for continuous pieces)

For piecewise functions, evaluate each piece separately on its domain.

**Example:** Find $\lim_{x \to 3^-} f(x)$ and $\lim_{x \to 3^+} f(x)$ where:

$$f(x) = \begin{cases}
x^2 & \text{if } x < 3 \\
2x + 1 & \text{if } x \geq 3
\end{cases}$$

**Solution:**

For the **left-hand limit** (approaching from $x < 3$), use the first piece:
$$\lim_{x \to 3^-} f(x) = \lim_{x \to 3^-} x^2 = 3^2 = 9$$

For the **right-hand limit** (approaching from $x \geq 3$), use the second piece:
$$\lim_{x \to 3^+} f(x) = \lim_{x \to 3^+} (2x + 1) = 2(3) + 1 = 7$$

Since $9 \neq 7$, the two-sided limit $\lim_{x \to 3} f(x)$ does NOT exist.

### Strategy 2: Factoring and Simplifying

**Example:** Find $\lim_{x \to 2^+} \frac{x^2 - 4}{x - 2}$

**Solution:**

Factor the numerator:
$$\lim_{x \to 2^+} \frac{(x-2)(x+2)}{x-2}$$

Cancel the common factor (valid because we're approaching 2, not at 2):
$$\lim_{x \to 2^+} (x + 2) = 2 + 2 = 4$$

Note: For this function, $\lim_{x \to 2^-} f(x) = 4$ as well, so $\lim_{x \to 2} f(x) = 4$.

### Strategy 3: Analyzing Sign Changes

**Example:** Find $\lim_{x \to 0^-} \frac{x}{|x|}$ and $\lim_{x \to 0^+} \frac{x}{|x|}$

**Solution:**

Recall that $|x| = \begin{cases} x & \text{if } x \geq 0 \\ -x & \text{if } x < 0 \end{cases}$

**Left-hand limit** (when $x < 0$, so $|x| = -x$):
$$\lim_{x \to 0^-} \frac{x}{|x|} = \lim_{x \to 0^-} \frac{x}{-x} = \lim_{x \to 0^-} (-1) = -1$$

**Right-hand limit** (when $x > 0$, so $|x| = x$):
$$\lim_{x \to 0^+} \frac{x}{|x|} = \lim_{x \to 0^+} \frac{x}{x} = \lim_{x \to 0^+} (1) = 1$$

Since $-1 \neq 1$, the two-sided limit does NOT exist.

---

## Worked Examples

### Example 1: Piecewise Function Analysis

**Problem:** Given $f(x) = \begin{cases}
3x - 1 & \text{if } x < 1 \\
x^2 + 1 & \text{if } x \geq 1
\end{cases}$

Find: (a) $\lim_{x \to 1^-} f(x)$ (b) $\lim_{x \to 1^+} f(x)$ (c) $\lim_{x \to 1} f(x)$ (d) $f(1)$

**Solution:**

**(a) Left-hand limit:**
When approaching from the left, use $f(x) = 3x - 1$:
$$\lim_{x \to 1^-} f(x) = \lim_{x \to 1^-} (3x - 1) = 3(1) - 1 = 2$$

**(b) Right-hand limit:**
When approaching from the right, use $f(x) = x^2 + 1$:
$$\lim_{x \to 1^+} f(x) = \lim_{x \to 1^+} (x^2 + 1) = 1^2 + 1 = 2$$

**(c) Two-sided limit:**
Since both one-sided limits exist and equal 2:
$$\lim_{x \to 1} f(x) = 2$$

**(d) Function value:**
Since $x = 1$ satisfies $x \geq 1$, use the second piece:
$$f(1) = 1^2 + 1 = 2$$

**Conclusion:** This function is continuous at $x = 1$ because $\lim_{x \to 1} f(x) = f(1) = 2$.

---

### Example 2: Square Root Function

**Problem:** Evaluate $\lim_{x \to 4^-} \frac{\sqrt{x} - 2}{x - 4}$ and $\lim_{x \to 4^+} \frac{\sqrt{x} - 2}{x - 4}$

**Solution:**

Both limits give the indeterminate form $\frac{0}{0}$, so we'll rationalize the numerator.

Multiply by the conjugate:
$$\frac{\sqrt{x} - 2}{x - 4} \cdot \frac{\sqrt{x} + 2}{\sqrt{x} + 2} = \frac{(\sqrt{x})^2 - 4}{(x - 4)(\sqrt{x} + 2)} = \frac{x - 4}{(x - 4)(\sqrt{x} + 2)}$$

Cancel $(x - 4)$:
$$= \frac{1}{\sqrt{x} + 2}$$

**Left-hand limit:**
$$\lim_{x \to 4^-} \frac{1}{\sqrt{x} + 2} = \frac{1}{\sqrt{4} + 2} = \frac{1}{4}$$

**Right-hand limit:**
$$\lim_{x \to 4^+} \frac{1}{\sqrt{x} + 2} = \frac{1}{\sqrt{4} + 2} = \frac{1}{4}$$

Both one-sided limits equal $\frac{1}{4}$, so $\lim_{x \to 4} \frac{\sqrt{x} - 2}{x - 4} = \frac{1}{4}$.

---

### Example 3: Absolute Value with Variable

**Problem:** Find $\lim_{x \to 3^-} \frac{|x - 3|}{x - 3}$ and $\lim_{x \to 3^+} \frac{|x - 3|}{x - 3}$

**Solution:**

Recall: $|x - 3| = \begin{cases} x - 3 & \text{if } x \geq 3 \\ -(x - 3) & \text{if } x < 3 \end{cases}$

**Left-hand limit** (when $x < 3$):
$$\lim_{x \to 3^-} \frac{|x - 3|}{x - 3} = \lim_{x \to 3^-} \frac{-(x - 3)}{x - 3} = \lim_{x \to 3^-} (-1) = -1$$

**Right-hand limit** (when $x > 3$):
$$\lim_{x \to 3^+} \frac{|x - 3|}{x - 3} = \lim_{x \to 3^+} \frac{x - 3}{x - 3} = \lim_{x \to 3^+} (1) = 1$$

Since $-1 \neq 1$, the two-sided limit does NOT exist.

---

### Example 4: Rational Function with Restriction

**Problem:** Given $g(x) = \frac{x^2 - 9}{x + 3}$, find $\lim_{x \to -3^-} g(x)$ and $\lim_{x \to -3^+} g(x)$

**Solution:**

Factor the numerator:
$$g(x) = \frac{(x - 3)(x + 3)}{x + 3}$$

For $x \neq -3$, this simplifies to:
$$g(x) = x - 3$$

**Left-hand limit:**
$$\lim_{x \to -3^-} (x - 3) = -3 - 3 = -6$$

**Right-hand limit:**
$$\lim_{x \to -3^+} (x - 3) = -3 - 3 = -6$$

Both one-sided limits equal $-6$, so $\lim_{x \to -3} g(x) = -6$.

Note: Even though $g(-3)$ is undefined, the limit exists because the function approaches the same value from both sides.

---

### Example 5: Floor Function

**Problem:** The floor function $f(x) = \lfloor x \rfloor$ gives the greatest integer less than or equal to $x$. Find $\lim_{x \to 2^-} \lfloor x \rfloor$ and $\lim_{x \to 2^+} \lfloor x \rfloor$.

**Solution:**

**Left-hand limit:**
As $x$ approaches 2 from the left (e.g., 1.9, 1.99, 1.999...), $\lfloor x \rfloor = 1$:
$$\lim_{x \to 2^-} \lfloor x \rfloor = 1$$

**Right-hand limit:**
As $x$ approaches 2 from the right (e.g., 2.1, 2.01, 2.001...), or at $x = 2$ itself, $\lfloor x \rfloor = 2$:
$$\lim_{x \to 2^+} \lfloor x \rfloor = 2$$

Since $1 \neq 2$, the two-sided limit $\lim_{x \to 2} \lfloor x \rfloor$ does NOT exist.

**Note:** The floor function has a jump discontinuity at every integer.

---

## Practice Problems

### Basic Problems (1-5)

**1.** Given:

$$f(x) = \begin{cases} 2x + 1 & \text{if } x < 0 \\ x^2 & \text{if } x \geq 0 \end{cases}$$

Find $\lim_{x \to 0^-} f(x)$ and $\lim_{x \to 0^+} f(x)$.

---

**2.** Evaluate:

$$\lim_{x \to 5^-} \frac{|x - 5|}{x - 5} \quad \text{and} \quad \lim_{x \to 5^+} \frac{|x - 5|}{x - 5}$$

---

**3.** For:

$$g(x) = \begin{cases} x + 3 & \text{if } x \leq 2 \\ 5 & \text{if } x > 2 \end{cases}$$

Find $\lim_{x \to 2^-} g(x)$, $\lim_{x \to 2^+} g(x)$, and $\lim_{x \to 2} g(x)$.

---

**4.** Find:

$$\lim_{x \to 1^-} \frac{x^2 - 1}{x - 1} \quad \text{and} \quad \lim_{x \to 1^+} \frac{x^2 - 1}{x - 1}$$

---

**5.** Given:

$$h(x) = \begin{cases} -x & \text{if } x < -1 \\ x^2 + 2 & \text{if } x \geq -1 \end{cases}$$

Determine if $\lim_{x \to -1} h(x)$ exists.

### Intermediate Problems (6-10)

**6.** Evaluate:

$$\lim_{x \to 0^-} \frac{x}{|x|} \quad \text{and} \quad \lim_{x \to 0^+} \frac{x}{|x|}$$

Does $\lim_{x \to 0} \frac{x}{|x|}$ exist?

---

**7.** For:

$$f(x) = \begin{cases} x^2 - 4 & \text{if } x < 2 \\ 2x & \text{if } x = 2 \\ 3x - 6 & \text{if } x > 2 \end{cases}$$

Find all one-sided limits at $x = 2$ and determine if the two-sided limit exists.

---

**8.** Find:

$$\lim_{x \to 3^-} \frac{\sqrt{9 - x^2}}{3 - x}$$

*(Hint: rationalize)*

---

**9.** Given:

$$f(x) = \frac{x^2 + x - 6}{x - 2}$$

Find $\lim_{x \to 2^-} f(x)$ and $\lim_{x \to 2^+} f(x)$.

---

**10.** Evaluate:

$$\lim_{x \to -2^-} \frac{|x + 2|}{x^2 - 4} \quad \text{and} \quad \lim_{x \to -2^+} \frac{|x + 2|}{x^2 - 4}$$

### Advanced Problems (11-15)

**11.** For:

$$g(x) = \begin{cases} \frac{x^2 - 16}{x - 4} & \text{if } x \neq 4 \\ 7 & \text{if } x = 4 \end{cases}$$

Find $\lim_{x \to 4^-} g(x)$, $\lim_{x \to 4^+} g(x)$, and determine if $g$ is continuous at $x = 4$.

---

**12.** Find:

$$\lim_{x \to 1^+} \frac{\sqrt{x - 1}}{x - 1}$$

Explain why the left-hand limit doesn't exist.

---

**13.** Given:

$$f(x) = \begin{cases} ax + b & \text{if } x < 1 \\ 3x^2 - 1 & \text{if } x \geq 1 \end{cases}$$

Find values of $a$ and $b$ that make $\lim_{x \to 1} f(x)$ exist and equal 2.

---

**14.** Evaluate:

$$\lim_{x \to 0^-} \frac{1}{x} \quad \text{and} \quad \lim_{x \to 0^+} \frac{1}{x}$$

Describe the behavior in both cases.

---

**15.** For the ceiling function $f(x) = \lceil x \rceil$ (smallest integer greater than or equal to $x$), find:

$$\lim_{x \to 3^-} \lceil x \rceil \quad \text{and} \quad \lim_{x \to 3^+} \lceil x \rceil$$

### Challenge Problems (16-18)

**16.** Given:

$$h(x) = \begin{cases} \frac{\sin x}{x} & \text{if } x < 0 \\ \frac{1 - \cos x}{x} & \text{if } x > 0 \end{cases}$$

Find $\lim_{x \to 0^-} h(x)$ and $\lim_{x \to 0^+} h(x)$.

*(You may use the fact that $\lim_{x \to 0} \frac{\sin x}{x} = 1$)*

---

**17.** Find all values of $c$ for which $\lim_{x \to 2} f(x)$ exists, where:

$$f(x) = \begin{cases} x^2 + c & \text{if } x < 2 \\ cx + 1 & \text{if } x \geq 2 \end{cases}$$

---

**18.** Analyze:

$$\lim_{x \to 0^-} x \cdot \lfloor \frac{1}{x} \rfloor \quad \text{and} \quad \lim_{x \to 0^+} x \cdot \lfloor \frac{1}{x} \rfloor$$

*(This is challenging!)*

---

## Solutions to Practice Problems

### Solution 1
**Left-hand limit:** Use $f(x) = 2x + 1$ for $x < 0$:
$$\lim_{x \to 0^-} f(x) = 2(0) + 1 = 1$$

**Right-hand limit:** Use $f(x) = x^2$ for $x \geq 0$:
$$\lim_{x \to 0^+} f(x) = 0^2 = 0$$

Since $1 \neq 0$, the two-sided limit does not exist.

---

### Solution 2

**Left-hand limit:**

When $x < 5$, we have $x - 5 < 0$, so $|x - 5| = -(x - 5)$:

$$\lim_{x \to 5^-} \frac{|x - 5|}{x - 5} = \lim_{x \to 5^-} \frac{-(x - 5)}{x - 5} = -1$$

**Right-hand limit:**

When $x > 5$, we have $x - 5 > 0$, so $|x - 5| = x - 5$:

$$\lim_{x \to 5^+} \frac{|x - 5|}{x - 5} = \lim_{x \to 5^+} \frac{x - 5}{x - 5} = 1$$

---

### Solution 3
**Left-hand limit:** Use $g(x) = x + 3$ for $x \leq 2$:
$$\lim_{x \to 2^-} g(x) = 2 + 3 = 5$$

**Right-hand limit:** Use $g(x) = 5$ for $x > 2$:
$$\lim_{x \to 2^+} g(x) = 5$$

**Two-sided limit:** Since both one-sided limits equal 5:
$$\lim_{x \to 2} g(x) = 5$$

This function is continuous at $x = 2$.

---

### Solution 4
Factor the numerator:
$$\frac{x^2 - 1}{x - 1} = \frac{(x - 1)(x + 1)}{x - 1} = x + 1 \quad (x \neq 1)$$

**Left-hand limit:**
$$\lim_{x \to 1^-} (x + 1) = 1 + 1 = 2$$

**Right-hand limit:**
$$\lim_{x \to 1^+} (x + 1) = 1 + 1 = 2$$

Both limits equal 2, so $\lim_{x \to 1} \frac{x^2 - 1}{x - 1} = 2$.

---

### Solution 5
**Left-hand limit:** Use $h(x) = -x$ for $x < -1$:
$$\lim_{x \to -1^-} h(x) = -(-1) = 1$$

**Right-hand limit:** Use $h(x) = x^2 + 2$ for $x \geq -1$:
$$\lim_{x \to -1^+} h(x) = (-1)^2 + 2 = 3$$

Since $1 \neq 3$, the limit $\lim_{x \to -1} h(x)$ does NOT exist.

---

### Solution 6

**Left-hand limit:**

When $x < 0$, we have $|x| = -x$:

$$\lim_{x \to 0^-} \frac{x}{|x|} = \lim_{x \to 0^-} \frac{x}{-x} = -1$$

**Right-hand limit:**

When $x > 0$, we have $|x| = x$:

$$\lim_{x \to 0^+} \frac{x}{|x|} = \lim_{x \to 0^+} \frac{x}{x} = 1$$

**Conclusion:**

Since $-1 \neq 1$, the limit $\lim_{x \to 0} \frac{x}{|x|}$ does NOT exist.

---

### Solution 7
**Left-hand limit:** Use $f(x) = x^2 - 4$ for $x < 2$:
$$\lim_{x \to 2^-} f(x) = 2^2 - 4 = 0$$

**Right-hand limit:** Use $f(x) = 3x - 6$ for $x > 2$:
$$\lim_{x \to 2^+} f(x) = 3(2) - 6 = 0$$

Both one-sided limits equal 0, so $\lim_{x \to 2} f(x) = 0$.

Note: $f(2) = 2(2) = 4$, so the function is NOT continuous at $x = 2$ (removable discontinuity).

---

### Solution 8

As $x \to 3^-$, we approach from values less than 3, so $x < 3$ and thus $3 - x > 0$.

Direct substitution gives $\frac{0}{0}$, so rationalize the numerator:

$$\frac{\sqrt{9 - x^2}}{3 - x} \cdot \frac{\sqrt{9 - x^2}}{\sqrt{9 - x^2}} = \frac{9 - x^2}{(3 - x)\sqrt{9 - x^2}}$$

Factor the numerator:

$$= \frac{(3 - x)(3 + x)}{(3 - x)\sqrt{9 - x^2}}$$

$$= \frac{3 + x}{\sqrt{9 - x^2}}$$

Now substitute:

$$\lim_{x \to 3^-} \frac{3 + x}{\sqrt{9 - x^2}} = \frac{3 + 3}{\sqrt{9 - 9}} = \frac{6}{0^+}$$

This approaches $+\infty$ (the denominator approaches 0 from the positive side).

---

### Solution 9
Factor the numerator:
$$f(x) = \frac{(x + 3)(x - 2)}{x - 2} = x + 3 \quad (x \neq 2)$$

**Left-hand limit:**
$$\lim_{x \to 2^-} (x + 3) = 2 + 3 = 5$$

**Right-hand limit:**
$$\lim_{x \to 2^+} (x + 3) = 2 + 3 = 5$$

Both limits equal 5, so $\lim_{x \to 2} f(x) = 5$.

---

### Solution 10

Factor the denominator: $x^2 - 4 = (x + 2)(x - 2)$

**Left-hand limit:**

When $x < -2$, we have $x + 2 < 0$, so $|x + 2| = -(x + 2)$:

$$\lim_{x \to -2^-} \frac{|x + 2|}{x^2 - 4} = \lim_{x \to -2^-} \frac{-(x + 2)}{(x + 2)(x - 2)}$$

$$= \lim_{x \to -2^-} \frac{-1}{x - 2} = \frac{-1}{-2 - 2} = \frac{1}{4}$$

**Right-hand limit:**

When $x > -2$, we have $x + 2 > 0$, so $|x + 2| = x + 2$:

$$\lim_{x \to -2^+} \frac{|x + 2|}{x^2 - 4} = \lim_{x \to -2^+} \frac{x + 2}{(x + 2)(x - 2)}$$

$$= \lim_{x \to -2^+} \frac{1}{x - 2} = \frac{1}{-2 - 2} = -\frac{1}{4}$$

**Conclusion:**

Since $\frac{1}{4} \neq -\frac{1}{4}$, the two-sided limit does not exist.

---

### Solution 11
For $x \neq 4$, factor and simplify:
$$g(x) = \frac{(x - 4)(x + 4)}{x - 4} = x + 4$$

**Left-hand limit:**
$$\lim_{x \to 4^-} g(x) = \lim_{x \to 4^-} (x + 4) = 8$$

**Right-hand limit:**
$$\lim_{x \to 4^+} g(x) = \lim_{x \to 4^+} (x + 4) = 8$$

The two-sided limit exists: $\lim_{x \to 4} g(x) = 8$

However, $g(4) = 7 \neq 8$, so $g$ is NOT continuous at $x = 4$ (removable discontinuity).

---

### Solution 12

**Right-hand limit:**

$$\lim_{x \to 1^+} \frac{\sqrt{x - 1}}{x - 1}$$

Let $u = x - 1$, so as $x \to 1^+$, we have $u \to 0^+$:

$$= \lim_{u \to 0^+} \frac{\sqrt{u}}{u}$$

$$= \lim_{u \to 0^+} \frac{1}{\sqrt{u}} = +\infty$$

**Left-hand limit:**

Does not exist because $\sqrt{x - 1}$ is not defined for $x < 1$ (can't take the square root of a negative number in the real numbers).

---

### Solution 13
For the limit to exist and equal 2, we need:
$$\lim_{x \to 1^-} f(x) = \lim_{x \to 1^+} f(x) = 2$$

**Left-hand limit:**
$$\lim_{x \to 1^-} (ax + b) = a(1) + b = a + b$$

**Right-hand limit:**
$$\lim_{x \to 1^+} (3x^2 - 1) = 3(1)^2 - 1 = 2$$

For both to equal 2:
$$a + b = 2$$

There are infinitely many solutions. For example:
- $a = 1, b = 1$
- $a = 2, b = 0$
- $a = 0, b = 2$
- $a = 3, b = -1$

Any pair $(a, b)$ satisfying $a + b = 2$ works.

---

### Solution 14
**Left-hand limit:**
As $x \to 0^-$ (approaching from negative values), $\frac{1}{x}$ becomes a large negative number:
$$\lim_{x \to 0^-} \frac{1}{x} = -\infty$$

**Right-hand limit:**
As $x \to 0^+$ (approaching from positive values), $\frac{1}{x}$ becomes a large positive number:
$$\lim_{x \to 0^+} \frac{1}{x} = +\infty$$

Neither one-sided limit exists as a finite number, and they approach different infinities, so the two-sided limit does not exist.

---

### Solution 15
The ceiling function $\lceil x \rceil$ gives the smallest integer $\geq x$.

**Left-hand limit:**
As $x \to 3^-$ (e.g., 2.9, 2.99, 2.999...), $\lceil x \rceil = 3$:
$$\lim_{x \to 3^-} \lceil x \rceil = 3$$

**Right-hand limit:**
As $x \to 3^+$ (e.g., 3.1, 3.01, 3.001...), or at $x = 3$, $\lceil x \rceil = 3$:
$$\lim_{x \to 3^+} \lceil x \rceil = 3$$

Both limits equal 3, so $\lim_{x \to 3} \lceil x \rceil = 3$.

Note: The ceiling function is right-continuous at integers (unlike the floor function, which is left-continuous).

---

### Solution 16

**Left-hand limit:**

Use $h(x) = \frac{\sin x}{x}$ for $x < 0$:

$$\lim_{x \to 0^-} h(x) = \lim_{x \to 0^-} \frac{\sin x}{x} = 1$$

*(Using the standard limit $\lim_{x \to 0} \frac{\sin x}{x} = 1$)*

**Right-hand limit:**

Use $h(x) = \frac{1 - \cos x}{x}$ for $x > 0$:

$$\lim_{x \to 0^+} h(x) = \lim_{x \to 0^+} \frac{1 - \cos x}{x}$$

Use L'Hôpital's rule or the identity $1 - \cos x = 2\sin^2(\frac{x}{2})$:

$$= \lim_{x \to 0^+} \frac{2\sin^2(\frac{x}{2})}{x}$$

$$= \lim_{x \to 0^+} \frac{2\sin^2(\frac{x}{2})}{2 \cdot \frac{x}{2}}$$

$$= \lim_{x \to 0^+} \sin\left(\frac{x}{2}\right) \cdot \frac{\sin(\frac{x}{2})}{\frac{x}{2}}$$

$$= 0 \cdot 1 = 0$$

**Conclusion:**

Since $1 \neq 0$, the two-sided limit $\lim_{x \to 0} h(x)$ does not exist.

---

### Solution 17
For the limit to exist at $x = 2$, the one-sided limits must be equal:
$$\lim_{x \to 2^-} f(x) = \lim_{x \to 2^+} f(x)$$

**Left-hand limit:**
$$\lim_{x \to 2^-} (x^2 + c) = 4 + c$$

**Right-hand limit:**
$$\lim_{x \to 2^+} (cx + 1) = 2c + 1$$

Set them equal:
$$4 + c = 2c + 1$$
$$4 - 1 = 2c - c$$
$$3 = c$$

Therefore, $c = 3$ is the only value for which the limit exists.

Verification: With $c = 3$:
- Left: $4 + 3 = 7$
- Right: $2(3) + 1 = 7$ ✓

---

### Solution 18

This is a very challenging problem!

**Right-hand limit:**

When $x > 0$ is very small, $\frac{1}{x}$ is a large positive number.

For example:
- If $x = 0.01$, then $\frac{1}{x} = 100$, so $\lfloor \frac{1}{x} \rfloor = 100$
- If $x = 0.001$, then $\frac{1}{x} = 1000$, so $\lfloor \frac{1}{x} \rfloor = 1000$

In general, for small positive $x$:

$$\lfloor \frac{1}{x} \rfloor \approx \frac{1}{x}$$

(They differ by less than 1.)

So:

$$x \cdot \lfloor \frac{1}{x} \rfloor \approx x \cdot \frac{1}{x} = 1$$

More precisely:

$$\frac{1}{x} - 1 < \lfloor \frac{1}{x} \rfloor \leq \frac{1}{x}$$

Multiplying by $x > 0$:

$$1 - x < x \cdot \lfloor \frac{1}{x} \rfloor \leq 1$$

By the squeeze theorem, as $x \to 0^+$:

$$\lim_{x \to 0^+} x \cdot \lfloor \frac{1}{x} \rfloor = 1$$

**Left-hand limit:**

When $x < 0$ is very small (close to zero from the left), $\frac{1}{x}$ is a large negative number.

For example:
- If $x = -0.01$, then $\frac{1}{x} = -100$, so $\lfloor \frac{1}{x} \rfloor = -100$
- If $x = -0.001$, then $\frac{1}{x} = -1000$, so $\lfloor \frac{1}{x} \rfloor = -1000$

For negative $x$, we have:

$$\frac{1}{x} \leq \lfloor \frac{1}{x} \rfloor < \frac{1}{x} + 1$$

Multiplying by $x < 0$ (inequality reverses):

$$1 > x \cdot \lfloor \frac{1}{x} \rfloor \geq 1 + x$$

By the squeeze theorem, as $x \to 0^-$:

$$\lim_{x \to 0^-} x \cdot \lfloor \frac{1}{x} \rfloor = 1$$

**Conclusion:**

Surprisingly, both one-sided limits equal 1!

---

## AP Exam Tips

### Strategy for One-Sided Limits

1. **Identify the point of discontinuity** - Look for breaks, jumps, or different function rules
2. **Determine which piece applies** - For piecewise functions, check which formula to use from each side
3. **Evaluate separately** - Calculate left and right limits independently
4. **Compare results** - The two-sided limit exists only if both one-sided limits are equal

### Common Mistakes to Avoid

**Mistake 1: Using the wrong piece of a piecewise function**
- Always check whether the boundary point is included (≤ vs <)
- Left-hand limits use the piece for $x < a$
- Right-hand limits use the piece for $x \geq a$ (or $x > a$)

**Mistake 2: Confusing limits with function values**
- $\lim_{x \to a} f(x)$ can exist even when $f(a)$ is undefined
- $\lim_{x \to a} f(x)$ can differ from $f(a)$

**Mistake 3: Assuming both one-sided limits exist**
- Sometimes only one one-sided limit exists (e.g., $\sqrt{x}$ at $x = 0$)
- Infinite limits are NOT the same as limits that exist

**Mistake 4: Forgetting to simplify before substituting**
- Indeterminate forms ($\frac{0}{0}$) require algebraic manipulation first
- Factor, rationalize, or use other techniques before evaluating

**Mistake 5: Incorrect absolute value handling**
- Remember: $|x - a| = \begin{cases} x - a & \text{if } x \geq a \\ -(x - a) & \text{if } x < a \end{cases}$
- The sign changes at the boundary

### Quick Recognition Guide

| Function Type | One-Sided Limits Behavior |
|--------------|---------------------------|
| Piecewise with different rules | May have different values from left/right |
| Absolute value expressions | Often have different values due to sign change |
| Rational functions | Same from both sides unless there's a restriction |
| Floor/Ceiling functions | Jump discontinuities at integers |
| Square roots | May only have right-hand limit at boundary |

### Graphical Analysis Tips

When given a graph:
- Trace your finger from the left approaching the point
- Note what $y$-value you're approaching (left-hand limit)
- Trace from the right approaching the point
- Note what $y$-value you're approaching (right-hand limit)
- Open circles indicate the function value is undefined there
- Filled circles indicate the actual function value

### Limit Existence Checklist

For $\lim_{x \to a} f(x)$ to exist:
- [ ] $\lim_{x \to a^-} f(x)$ exists (finite value)
- [ ] $\lim_{x \to a^+} f(x)$ exists (finite value)
- [ ] Both one-sided limits are equal

If any box is unchecked, the two-sided limit does NOT exist.

---

## Connection to Continuity

A function $f$ is **continuous at $x = a$** if:
1. $f(a)$ exists (the function is defined at $a$)
2. $\lim_{x \to a} f(x)$ exists (both one-sided limits exist and are equal)
3. $\lim_{x \to a} f(x) = f(a)$ (the limit equals the function value)

One-sided limits help us identify three types of discontinuities:

**1. Jump Discontinuity:** Both one-sided limits exist but are not equal
$$\lim_{x \to a^-} f(x) \neq \lim_{x \to a^+} f(x)$$

**2. Removable Discontinuity:** Both one-sided limits exist and are equal, but either $f(a)$ is undefined or $\lim_{x \to a} f(x) \neq f(a)$
$$\lim_{x \to a^-} f(x) = \lim_{x \to a^+} f(x) \neq f(a)$$

**3. Infinite Discontinuity:** At least one one-sided limit is infinite
$$\lim_{x \to a^-} f(x) = \pm\infty \text{ or } \lim_{x \to a^+} f(x) = \pm\infty$$

---

## Summary

One-sided limits are essential for understanding function behavior at points of discontinuity:

- **Left-hand limits** ($\lim_{x \to a^-}$) approach from values less than $a$
- **Right-hand limits** ($\lim_{x \to a^+}$) approach from values greater than $a$
- **Two-sided limits exist** only when both one-sided limits exist and are equal
- **Piecewise functions** require careful attention to which piece applies from each direction
- **Absolute value expressions** often produce different one-sided limits due to sign changes
- **Graphical analysis** helps visualize one-sided limit behavior

Mastering one-sided limits prepares you for understanding continuity, the Intermediate Value Theorem, and derivatives—all crucial topics in AP Calculus!

---

**Next Topics to Explore:**
- Continuity and the Intermediate Value Theorem
- Infinite Limits and Vertical Asymptotes
- Limits at Infinity and Horizontal Asymptotes
- Introduction to Derivatives

---

<div align="center">

[← Limit Laws & Techniques](calculus/limit-laws-and-techniques.md) | [Limits at Infinity →](calculus/limits-at-infinity.md)

</div>