# Limits: The Foundation
<p class="article-date">August 17, 2024</p>

*You've heard that calculus is about "instantaneous change." But how do you calculate something at a single instant? The answer is limits - the most important idea in all of calculus.*

---

## What You'll Learn

- What a limit actually means (intuitively and formally)
- How to read and write limit notation
- How to evaluate limits graphically, numerically, and algebraically
- When limits don't exist and why
- Why limits are the foundation of everything in calculus

---

## Prerequisites

Before diving in, make sure you're comfortable with:
- [Functions Refresher](/calculus/0201-functions-refresher) - function notation, evaluating f(x)
- [The Concept of Change](/calculus/0202-the-concept-of-change) - average rate of change, the idea of "approaching"

---

## The Core Concept

### The Problem We're Trying to Solve

Remember from [The Concept of Change](/calculus/0202-the-concept-of-change) when we tried to find instantaneous speed? We kept making our time interval smaller and smaller:

| Interval | Average Speed |
|----------|---------------|
| 1 minute | 30 mph |
| 10 seconds | 27.5 mph |
| 1 second | 27.1 mph |
| 0.1 seconds | 27.01 mph |
| 0.01 seconds | 27.001 mph |

The values are *approaching* 27 mph. But we can never actually use an interval of 0 seconds (that would be division by zero).

**This is exactly what limits solve.**

A limit lets us say: "As the interval approaches zero, the speed approaches 27 mph" - without ever actually dividing by zero.

---

### Intuition First: The Approaching Game

Imagine you're walking toward a wall. You take a step that covers half the remaining distance. Then another step covering half of what's left. Then another.

```
You:    |------>|---->|-->|->|>|
Wall:                          |
```

**Question**: Do you ever reach the wall?

**Mathematically**: No. You always have some distance left.

**In limit terms**: As the number of steps approaches infinity, your distance from the wall approaches zero.

You never *get* to zero. But you get *arbitrarily close*. Close enough that the remaining distance is smaller than any number you can name.

**That's what a limit is.**

---

### The Notation

$$\lim_{x \to a} f(x) = L$$

This reads: "The limit of f(x) as x approaches a equals L"

It means: As x gets closer and closer to a (but never equals a), f(x) gets closer and closer to L.

**Key insight**: We never care what happens *at* x = a. We only care what happens as we *approach* a.

---

### Why "At" Doesn't Matter

Consider this function:

$$f(x) = \frac{x^2 - 1}{x - 1}$$

What's f(1)?

$$f(1) = \frac{1 - 1}{1 - 1} = \frac{0}{0} = \text{undefined}$$

The function literally doesn't exist at x = 1. There's a hole in the graph.

But what's the *limit* as x approaches 1?

Let's make a table:

| x | f(x) |
|---|------|
| 0.9 | 1.9 |
| 0.99 | 1.99 |
| 0.999 | 1.999 |
| 1.001 | 2.001 |
| 1.01 | 2.01 |
| 1.1 | 2.1 |

The values approach **2** from both sides!

So: $\lim_{x \to 1} \frac{x^2 - 1}{x - 1} = 2$

Even though f(1) doesn't exist, the limit exists and equals 2.

---

### The Algebra Behind This

Why did the limit equal 2? Let's factor:

$$\frac{x^2 - 1}{x - 1} = \frac{(x+1)(x-1)}{x-1}$$

For $x \neq 1$, we can cancel:

$$= x + 1$$

So as x approaches 1:
$$\lim_{x \to 1} (x + 1) = 1 + 1 = 2$$

> **Key technique**: When you get $\frac{0}{0}$, try to factor and cancel. This is called an **indeterminate form**.

---

## Three Ways to Find Limits

### Method 1: Direct Substitution

The easiest method. Just plug in the value.

**Example**: $\lim_{x \to 3} (x^2 + 2x)$

$$= 3^2 + 2(3) = 9 + 6 = 15$$

**When it works**: When the function is continuous at that point (no holes, jumps, or asymptotes).

**When it fails**: When you get $\frac{0}{0}$ or $\frac{\text{number}}{0}$

---

### Method 2: Algebraic Manipulation

When direct substitution gives $\frac{0}{0}$, try:
- **Factoring** (most common)
- **Rationalizing** (for square roots)
- **Common denominators** (for complex fractions)

**Example with factoring**:

$$\lim_{x \to 2} \frac{x^2 - 4}{x - 2}$$

Direct substitution: $\frac{4-4}{2-2} = \frac{0}{0}$ ❌

Factor: $\frac{(x+2)(x-2)}{x-2} = x + 2$ (for $x \neq 2$)

Therefore: $\lim_{x \to 2} (x + 2) = 4$

**Example with rationalizing**:

$$\lim_{x \to 0} \frac{\sqrt{x+1} - 1}{x}$$

Direct substitution: $\frac{0}{0}$ ❌

Multiply by conjugate:
$$= \lim_{x \to 0} \frac{\sqrt{x+1} - 1}{x} \cdot \frac{\sqrt{x+1} + 1}{\sqrt{x+1} + 1}$$

$$= \lim_{x \to 0} \frac{(x+1) - 1}{x(\sqrt{x+1} + 1)}$$

$$= \lim_{x \to 0} \frac{x}{x(\sqrt{x+1} + 1)}$$

$$= \lim_{x \to 0} \frac{1}{\sqrt{x+1} + 1}$$

$$= \frac{1}{\sqrt{1} + 1} = \frac{1}{2}$$

---

### Method 3: Graphical/Numerical Analysis

Sometimes you need to look at the graph or create a table of values.

**When to use**:
- Piecewise functions
- To verify your algebraic answer
- When algebra gets too messy

---

## Worked Examples

### Example 1: Direct Substitution

$$\lim_{x \to -2} (3x^3 - x + 5)$$

**Solution**:
$$= 3(-2)^3 - (-2) + 5$$
$$= 3(-8) + 2 + 5$$
$$= -24 + 7 = -17$$

---

### Example 2: Factoring

$$\lim_{x \to 3} \frac{x^2 - 9}{x - 3}$$

**Solution**:

Direct substitution: $\frac{9-9}{3-3} = \frac{0}{0}$ ❌

Factor numerator:
$$= \lim_{x \to 3} \frac{(x+3)(x-3)}{x-3}$$

Cancel (valid since $x \neq 3$):
$$= \lim_{x \to 3} (x + 3) = 6$$

---

### Example 3: Rationalizing

$$\lim_{x \to 4} \frac{x - 4}{\sqrt{x} - 2}$$

**Solution**:

Direct substitution: $\frac{0}{0}$ ❌

Multiply by conjugate of denominator:
$$= \lim_{x \to 4} \frac{x - 4}{\sqrt{x} - 2} \cdot \frac{\sqrt{x} + 2}{\sqrt{x} + 2}$$

$$= \lim_{x \to 4} \frac{(x-4)(\sqrt{x} + 2)}{x - 4}$$

$$= \lim_{x \to 4} (\sqrt{x} + 2) = \sqrt{4} + 2 = 4$$

---

### Example 4: Complex Fraction

$$\lim_{x \to 0} \frac{\frac{1}{x+2} - \frac{1}{2}}{x}$$

**Solution**:

Direct substitution: $\frac{0}{0}$ ❌

Combine fractions in numerator:
$$\frac{1}{x+2} - \frac{1}{2} = \frac{2 - (x+2)}{2(x+2)} = \frac{-x}{2(x+2)}$$

So:
$$= \lim_{x \to 0} \frac{\frac{-x}{2(x+2)}}{x} = \lim_{x \to 0} \frac{-x}{2(x+2)} \cdot \frac{1}{x}$$

$$= \lim_{x \to 0} \frac{-1}{2(x+2)} = \frac{-1}{2(2)} = -\frac{1}{4}$$

---

### Example 5: Piecewise Function

$$f(x) = \begin{cases} x^2 & \text{if } x < 1 \\ 2x - 1 & \text{if } x \geq 1 \end{cases}$$

Find $\lim_{x \to 1} f(x)$

**Solution**:

Check from the left ($x < 1$): $\lim_{x \to 1^-} x^2 = 1$

Check from the right ($x \geq 1$): $\lim_{x \to 1^+} (2x-1) = 2(1) - 1 = 1$

Both sides approach 1, so: $\lim_{x \to 1} f(x) = 1$

---

## When Limits Don't Exist

A limit **does not exist (DNE)** when:

### 1. Left and Right Limits Don't Match

$$f(x) = \begin{cases} 1 & \text{if } x < 0 \\ -1 & \text{if } x \geq 0 \end{cases}$$

$\lim_{x \to 0^-} f(x) = 1$ but $\lim_{x \to 0^+} f(x) = -1$

Since they don't match: $\lim_{x \to 0} f(x)$ **DNE**

### 2. Unbounded Behavior (Vertical Asymptote)

$$\lim_{x \to 0} \frac{1}{x^2} = \infty$$

Technically, we say the limit "does not exist" (though sometimes we write = ∞ to describe the behavior).

### 3. Oscillating Behavior

$$\lim_{x \to 0} \sin\left(\frac{1}{x}\right)$$

This oscillates infinitely fast between -1 and 1 as x → 0. It never settles on a value.

---

## Key Formulas & Rules

| Rule | Formula |
|------|---------|
| Constant | $\lim_{x \to a} c = c$ |
| Identity | $\lim_{x \to a} x = a$ |
| Sum | $\lim_{x \to a} [f(x) + g(x)] = \lim_{x \to a} f(x) + \lim_{x \to a} g(x)$ |
| Product | $\lim_{x \to a} [f(x) \cdot g(x)] = \lim_{x \to a} f(x) \cdot \lim_{x \to a} g(x)$ |
| Quotient | $\lim_{x \to a} \frac{f(x)}{g(x)} = \frac{\lim_{x \to a} f(x)}{\lim_{x \to a} g(x)}$ (if denominator ≠ 0) |
| Power | $\lim_{x \to a} [f(x)]^n = \left[\lim_{x \to a} f(x)\right]^n$ |

### Special Limits (Memorize These!)

$$\lim_{x \to 0} \frac{\sin x}{x} = 1$$

$$\lim_{x \to 0} \frac{1 - \cos x}{x} = 0$$

$$\lim_{x \to 0} \frac{e^x - 1}{x} = 1$$

---

## Common Mistakes to Avoid

### Mistake 1: Confusing f(a) with the limit

❌ "The limit is whatever f(a) equals"

✅ The limit is what f(x) *approaches* as x → a. These can be different!

### Mistake 2: Stopping at 0/0

❌ "I got 0/0, so the limit doesn't exist"

✅ 0/0 is *indeterminate* - it means you need to do more work (factor, rationalize, etc.)

### Mistake 3: Canceling without restrictions

❌ $\frac{(x-2)(x+3)}{x-2} = x + 3$ always

✅ $\frac{(x-2)(x+3)}{x-2} = x + 3$ for $x \neq 2$ (but this is fine for limits!)

### Mistake 4: Forgetting to check both sides

❌ Only checking the limit from one direction for piecewise functions

✅ Always check $\lim_{x \to a^-}$ AND $\lim_{x \to a^+}$ when the function changes at a

---

## AP Exam Tips

### For AP Calculus AB:
- Limits appear in Units 1-2 and are foundational for derivatives
- Know how to find limits graphically, numerically, AND algebraically
- The special limit $\frac{\sin x}{x} \to 1$ appears frequently

### For AP Calculus BC:
- Same as AB, plus L'Hôpital's Rule (covered later)
- Limits are crucial for series convergence tests

### Time-Saving Strategies:
1. **Try direct substitution first** - it works more often than you think
2. **Recognize $\frac{0}{0}$ immediately** - don't waste time; factor or rationalize
3. **For multiple choice**, estimate using a table if algebra looks messy

---

## Practice Problems

### Basic (Problems 1-5)

**Problem 1**: Evaluate $\lim_{x \to 4} (x^2 - 3x + 2)$

**Problem 2**: Evaluate $\lim_{x \to -1} \frac{x^2 - 1}{x + 1}$

**Problem 3**: Evaluate $\lim_{x \to 0} \frac{5x}{x}$

**Problem 4**: Evaluate $\lim_{x \to 2} \frac{x^2 - 4}{x - 2}$

**Problem 5**: Evaluate $\lim_{x \to 3} \sqrt{x^2 + 7}$

---

### Intermediate (Problems 6-10)

**Problem 6**: Evaluate $\lim_{x \to 1} \frac{x^3 - 1}{x - 1}$

**Problem 7**: Evaluate $\lim_{x \to 0} \frac{\sqrt{x+9} - 3}{x}$

**Problem 8**: Evaluate $\lim_{h \to 0} \frac{(2+h)^2 - 4}{h}$

**Problem 9**: Given $f(x) = \begin{cases} x^2 + 1 & \text{if } x \leq 2 \\ 4x - 3 & \text{if } x > 2 \end{cases}$, find $\lim_{x \to 2} f(x)$

**Problem 10**: Evaluate $\lim_{x \to 0} \frac{\frac{1}{3+x} - \frac{1}{3}}{x}$

---

### Advanced (Problems 11-15)

**Problem 11**: Evaluate $\lim_{x \to 4} \frac{x - 4}{\sqrt{x} - 2}$

**Problem 12**: Evaluate $\lim_{x \to 1} \frac{\sqrt{x} - 1}{x - 1}$

**Problem 13**: Evaluate $\lim_{x \to 0} \frac{\sqrt{1+x} - \sqrt{1-x}}{x}$

**Problem 14**: For what value of $k$ does $\lim_{x \to 2} \frac{x^2 + kx - 6}{x - 2}$ exist? Find the limit.

**Problem 15**: Evaluate $\lim_{x \to 0} \frac{x}{\sqrt{x+1} - 1}$

---

### AP Exam Practice (Problems 16-18)

**Problem 16** (AP Style - Multiple Choice):

$\lim_{x \to 3} \frac{x^2 - 9}{x^2 - 5x + 6}$ equals:

(A) 0  (B) 1  (C) 6  (D) Does not exist

**Problem 17** (AP Style - Free Response):

Let $g(x) = \frac{x^2 - 4x}{x^2 - 16}$

(a) Find $\lim_{x \to 0} g(x)$

(b) Find $\lim_{x \to 4} g(x)$

(c) Identify any vertical asymptotes and explain.

**Problem 18** (AP 2019 Style):

The function f is defined by $f(x) = \frac{2x^2 - 5x - 3}{x - 3}$ for $x \neq 3$.

(a) Find $\lim_{x \to 3} f(x)$

(b) Is f continuous at x = 3? Explain.

(c) If $f(3)$ were defined to make f continuous at x = 3, what would $f(3)$ equal?

---

## Answer Key

<details>
<summary><strong>Problem 1 Solution</strong></summary>

**Answer**: 6

**Step-by-step**:

This is direct substitution since the function is a polynomial (continuous everywhere).

$$\lim_{x \to 4} (x^2 - 3x + 2) = 4^2 - 3(4) + 2 = 16 - 12 + 2 = 6$$

</details>

<details>
<summary><strong>Problem 2 Solution</strong></summary>

**Answer**: -2

**Step-by-step**:

1. Try direct substitution: $\frac{(-1)^2 - 1}{-1 + 1} = \frac{0}{0}$ (indeterminate)

2. Factor the numerator: $x^2 - 1 = (x+1)(x-1)$

3. Simplify: $\frac{(x+1)(x-1)}{x+1} = x - 1$ for $x \neq -1$

4. Now substitute: $\lim_{x \to -1} (x-1) = -1 - 1 = -2$

</details>

<details>
<summary><strong>Problem 3 Solution</strong></summary>

**Answer**: 5

**Step-by-step**:

1. Simplify first: $\frac{5x}{x} = 5$ for all $x \neq 0$

2. Since we're taking the limit as x → 0 (not at 0), we use the simplified form

3. $\lim_{x \to 0} 5 = 5$

**Note**: Even though f(0) is undefined, the limit exists!

</details>

<details>
<summary><strong>Problem 4 Solution</strong></summary>

**Answer**: 4

**Step-by-step**:

1. Direct substitution gives $\frac{0}{0}$ (indeterminate)

2. Factor: $x^2 - 4 = (x+2)(x-2)$

3. Cancel: $\frac{(x+2)(x-2)}{x-2} = x + 2$ for $x \neq 2$

4. Substitute: $\lim_{x \to 2} (x+2) = 4$

</details>

<details>
<summary><strong>Problem 5 Solution</strong></summary>

**Answer**: 4

**Step-by-step**:

1. Direct substitution works (square root of a polynomial is continuous when the inside is positive)

2. $\lim_{x \to 3} \sqrt{x^2 + 7} = \sqrt{3^2 + 7} = \sqrt{9 + 7} = \sqrt{16} = 4$

</details>

<details>
<summary><strong>Problem 6 Solution</strong></summary>

**Answer**: 3

**Step-by-step**:

1. Direct substitution: $\frac{1-1}{1-1} = \frac{0}{0}$ (indeterminate)

2. Factor using difference of cubes: $x^3 - 1 = (x-1)(x^2 + x + 1)$

3. Cancel: $\frac{(x-1)(x^2+x+1)}{x-1} = x^2 + x + 1$

4. Substitute: $\lim_{x \to 1} (x^2 + x + 1) = 1 + 1 + 1 = 3$

</details>

<details>
<summary><strong>Problem 7 Solution</strong></summary>

**Answer**: $\frac{1}{6}$

**Step-by-step**:

1. Direct substitution: $\frac{\sqrt{9} - 3}{0} = \frac{0}{0}$ (indeterminate)

2. Rationalize by multiplying by $\frac{\sqrt{x+9} + 3}{\sqrt{x+9} + 3}$

3. Numerator becomes: $(\sqrt{x+9} - 3)(\sqrt{x+9} + 3) = (x+9) - 9 = x$

4. Full expression: $\frac{x}{x(\sqrt{x+9} + 3)} = \frac{1}{\sqrt{x+9} + 3}$

5. Substitute: $\frac{1}{\sqrt{0+9} + 3} = \frac{1}{3 + 3} = \frac{1}{6}$

</details>

<details>
<summary><strong>Problem 8 Solution</strong></summary>

**Answer**: 4

**Step-by-step**:

1. Expand $(2+h)^2 = 4 + 4h + h^2$

2. Substitute: $\frac{4 + 4h + h^2 - 4}{h} = \frac{4h + h^2}{h}$

3. Factor: $\frac{h(4 + h)}{h} = 4 + h$

4. Take limit: $\lim_{h \to 0} (4 + h) = 4$

**Note**: This is actually finding the derivative of $x^2$ at $x = 2$!

</details>

<details>
<summary><strong>Problem 9 Solution</strong></summary>

**Answer**: 5

**Step-by-step**:

1. Check left-hand limit (use $x^2 + 1$ since $x \leq 2$):
   $$\lim_{x \to 2^-} (x^2 + 1) = 4 + 1 = 5$$

2. Check right-hand limit (use $4x - 3$ since $x > 2$):
   $$\lim_{x \to 2^+} (4x - 3) = 8 - 3 = 5$$

3. Since both one-sided limits equal 5, the limit exists:
   $$\lim_{x \to 2} f(x) = 5$$

</details>

<details>
<summary><strong>Problem 10 Solution</strong></summary>

**Answer**: $-\frac{1}{9}$

**Step-by-step**:

1. Combine fractions in numerator:
   $$\frac{1}{3+x} - \frac{1}{3} = \frac{3 - (3+x)}{3(3+x)} = \frac{-x}{3(3+x)}$$

2. Divide by x:
   $$\frac{\frac{-x}{3(3+x)}}{x} = \frac{-x}{3(3+x)} \cdot \frac{1}{x} = \frac{-1}{3(3+x)}$$

3. Take limit:
   $$\lim_{x \to 0} \frac{-1}{3(3+x)} = \frac{-1}{3(3)} = -\frac{1}{9}$$

</details>

<details>
<summary><strong>Problem 11 Solution</strong></summary>

**Answer**: 4

**Step-by-step**:

1. Direct substitution: $\frac{0}{0}$ (indeterminate)

2. Rationalize denominator by multiplying by $\frac{\sqrt{x} + 2}{\sqrt{x} + 2}$

3. Denominator becomes: $(\sqrt{x} - 2)(\sqrt{x} + 2) = x - 4$

4. Full expression: $\frac{(x-4)(\sqrt{x} + 2)}{x - 4} = \sqrt{x} + 2$

5. Take limit: $\lim_{x \to 4} (\sqrt{x} + 2) = 2 + 2 = 4$

</details>

<details>
<summary><strong>Problem 12 Solution</strong></summary>

**Answer**: $\frac{1}{2}$

**Step-by-step**:

1. Direct substitution: $\frac{0}{0}$ (indeterminate)

2. Rationalize numerator by multiplying by $\frac{\sqrt{x} + 1}{\sqrt{x} + 1}$

3. Numerator becomes: $(\sqrt{x} - 1)(\sqrt{x} + 1) = x - 1$

4. Full expression: $\frac{x - 1}{(x-1)(\sqrt{x} + 1)} = \frac{1}{\sqrt{x} + 1}$

5. Take limit: $\frac{1}{\sqrt{1} + 1} = \frac{1}{2}$

</details>

<details>
<summary><strong>Problem 13 Solution</strong></summary>

**Answer**: 1

**Step-by-step**:

1. Direct substitution: $\frac{0}{0}$ (indeterminate)

2. Rationalize by multiplying by $\frac{\sqrt{1+x} + \sqrt{1-x}}{\sqrt{1+x} + \sqrt{1-x}}$

3. Numerator: $(1+x) - (1-x) = 2x$

4. Full expression: $\frac{2x}{x(\sqrt{1+x} + \sqrt{1-x})} = \frac{2}{\sqrt{1+x} + \sqrt{1-x}}$

5. Take limit: $\frac{2}{\sqrt{1} + \sqrt{1}} = \frac{2}{2} = 1$

</details>

<details>
<summary><strong>Problem 14 Solution</strong></summary>

**Answer**: $k = 1$, limit = 5

**Step-by-step**:

1. For the limit to exist when direct substitution gives $\frac{0}{0}$, we need $(x-2)$ to be a factor of the numerator.

2. If $x = 2$ is a root of $x^2 + kx - 6$:
   $$4 + 2k - 6 = 0$$
   $$2k = 2$$
   $$k = 1$$

3. With $k = 1$: $x^2 + x - 6 = (x+3)(x-2)$

4. Simplify: $\frac{(x+3)(x-2)}{x-2} = x + 3$

5. Take limit: $\lim_{x \to 2} (x + 3) = 5$

</details>

<details>
<summary><strong>Problem 15 Solution</strong></summary>

**Answer**: 2

**Step-by-step**:

1. Direct substitution: $\frac{0}{0}$ (indeterminate)

2. Rationalize denominator: multiply by $\frac{\sqrt{x+1} + 1}{\sqrt{x+1} + 1}$

3. Denominator becomes: $(x + 1) - 1 = x$

4. Full expression: $\frac{x(\sqrt{x+1} + 1)}{x} = \sqrt{x+1} + 1$

5. Take limit: $\sqrt{1} + 1 = 2$

</details>

<details>
<summary><strong>Problem 16 Solution</strong></summary>

**Answer**: (C) 6

**Step-by-step**:

1. Factor numerator: $x^2 - 9 = (x-3)(x+3)$

2. Factor denominator: $x^2 - 5x + 6 = (x-3)(x-2)$

3. Simplify: $\frac{(x-3)(x+3)}{(x-3)(x-2)} = \frac{x+3}{x-2}$

4. Take limit: $\frac{3+3}{3-2} = \frac{6}{1} = 6$

</details>

<details>
<summary><strong>Problem 17 Solution</strong></summary>

**(a) Answer**: 0

Factor: $g(x) = \frac{x(x-4)}{(x-4)(x+4)} = \frac{x}{x+4}$ for $x \neq 4$

$\lim_{x \to 0} \frac{x}{x+4} = \frac{0}{4} = 0$

**(b) Answer**: $\frac{1}{2}$

Using simplified form: $\lim_{x \to 4} \frac{x}{x+4} = \frac{4}{8} = \frac{1}{2}$

**(c) Answer**: Vertical asymptote at $x = -4$

The factor $(x + 4)$ remains in the denominator after simplification. As $x \to -4$, the denominator approaches 0 while the numerator approaches -4, creating unbounded behavior.

Note: There is NO vertical asymptote at $x = 4$ because the factor cancels (it's a removable discontinuity/hole instead).

</details>

<details>
<summary><strong>Problem 18 Solution</strong></summary>

**(a) Answer**: 7

Factor: $2x^2 - 5x - 3 = (2x + 1)(x - 3)$

Simplify: $\frac{(2x+1)(x-3)}{x-3} = 2x + 1$

$\lim_{x \to 3} (2x + 1) = 7$

**(b) Answer**: No, f is not continuous at x = 3

For continuity at x = 3, we need:
1. f(3) to be defined ❌ (given that f is defined for $x \neq 3$)
2. $\lim_{x \to 3} f(x)$ to exist ✓ (equals 7)
3. $\lim_{x \to 3} f(x) = f(3)$ ❌ (can't check since f(3) undefined)

Since f(3) is not defined, f is not continuous at x = 3.

**(c) Answer**: $f(3) = 7$

To make f continuous, we need $f(3) = \lim_{x \to 3} f(x) = 7$

This would "fill in the hole" in the graph.

</details>

---

## What's Next

Now that you understand limits, we're ready to explore them more deeply:

- **Understanding Limits** - Formal definition (epsilon-delta) and more intuition
- **Limit Laws & Techniques** - More tools for evaluating limits
- **One-Sided Limits** - Left and right limits in detail

Limits are the foundation of everything in calculus. Master them, and derivatives and integrals will make so much more sense!

---

*"The limit concept is the cornerstone of calculus - without it, we couldn't make sense of instantaneous rates of change or accumulation."*

---

<div align="center">

[← Concept of Change](calculus/the-concept-of-change.md) | [Understanding Limits →](calculus/understanding-limits.md)

</div>
