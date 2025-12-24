# Understanding Limits
<p class="article-date">August 24, 2024</p>

*You've learned what limits are and how to compute basic ones. Now let's go deeper - what does it really mean for a limit to exist? And how do we tackle limits that seem impossible at first glance?*

---

## What You'll Learn

- The precise (epsilon-delta) definition of a limit and what it actually means
- How to handle limits with absolute values
- The Squeeze Theorem - a powerful tool for tricky limits
- Advanced algebraic techniques for evaluating limits
- How to determine if a limit exists without computing it

---

## Prerequisites

Before diving in, make sure you're comfortable with:
- [Limits: The Foundation](/calculus/0203-limits-the-foundation) - basic limit concepts and techniques
- [Functions Refresher](/calculus/0201-functions-refresher) - absolute value, piecewise functions

---

## The Core Concept

### From Intuition to Precision

In [Limits: The Foundation](/calculus/0203-limits-the-foundation), we said:

> "As x gets closer and closer to a, f(x) gets closer and closer to L"

But what does "closer and closer" actually mean? Mathematicians in the 1800s realized they needed a rock-solid definition. The result is the **epsilon-delta definition** - one of the most important ideas in all of mathematics.

---

### The Epsilon-Delta Definition

$$\lim_{x \to a} f(x) = L$$

means: **For every $\varepsilon > 0$, there exists a $\delta > 0$ such that if $0 < |x - a| < \delta$, then $|f(x) - L| < \varepsilon$.**

That's a mouthful. Let's break it down with an analogy.

---

### The "Challenge Game" Analogy

Imagine you're playing a game with a skeptical friend:

**The Setup:**
- You claim that $\lim_{x \to 2} (3x - 1) = 5$
- Your friend doesn't believe you

**The Game:**
1. Your friend picks a tiny "tolerance" $\varepsilon$ (epsilon) - say, 0.01
   - This means: "I challenge you to get f(x) within 0.01 of 5"

2. You must find a "range" $\delta$ (delta) around x = 2
   - You respond: "If x is within δ of 2, then f(x) will be within 0.01 of 5"

3. For $f(x) = 3x - 1$, if x is within 0.0033 of 2 (so $\delta = 0.0033$), then:
   - When $x = 2.003$: $f(x) = 3(2.003) - 1 = 5.009$ ✓ (within 0.01 of 5)
   - When $x = 1.997$: $f(x) = 3(1.997) - 1 = 4.991$ ✓ (within 0.01 of 5)

**The Key:** No matter how small your friend makes $\varepsilon$, you can always find a $\delta$ that works. THAT's what makes the limit equal to 5.

---

### Visualizing Epsilon-Delta

Think of it as a "target zone":

```
f(x)
  |
L+ε|. . . . . . . . . . . . . . . upper bound
  |         ___________
L |........|    •      |........ target value
  |        |___________|
L-ε|. . . . . . . . . . . . . . . lower bound
  |
  |--------[-----•-----]--------→ x
           a-δ   a    a+δ

If x is in the δ-zone around a,
then f(x) must land in the ε-zone around L.
```

---

### Why This Matters

You don't need to write epsilon-delta proofs on the AP exam. But understanding this definition helps you:

1. **Know when limits exist**: Both sides must approach the same value
2. **Understand continuity**: A function is continuous when the limit equals the function value
3. **Grasp derivatives**: The derivative is defined using limits
4. **Build mathematical maturity**: This precision is what makes calculus rigorous

---

## Limits with Absolute Values

Absolute value functions often require careful analysis because they behave differently on each side of zero.

### Review: What |x| Means

$$|x| = \begin{cases} x & \text{if } x \geq 0 \\ -x & \text{if } x < 0 \end{cases}$$

More generally: $|x - a|$ measures the distance from x to a.

---

### Strategy for Absolute Value Limits

**Step 1:** Identify where the expression inside the absolute value equals zero.

**Step 2:** Check the limit from the left and right separately, using the appropriate piece.

**Step 3:** If both one-sided limits are equal, the limit exists.

---

### Worked Example: Basic Absolute Value

$$\lim_{x \to 0} \frac{|x|}{x}$$

**From the right** ($x > 0$): $|x| = x$, so $\frac{|x|}{x} = \frac{x}{x} = 1$

$$\lim_{x \to 0^+} \frac{|x|}{x} = 1$$

**From the left** ($x < 0$): $|x| = -x$, so $\frac{|x|}{x} = \frac{-x}{x} = -1$

$$\lim_{x \to 0^-} \frac{|x|}{x} = -1$$

**Conclusion:** Since $1 \neq -1$, the limit **does not exist**.

---

### Worked Example: Absolute Value That Works

$$\lim_{x \to 3} \frac{|x - 3|}{x^2 - 9}$$

First, note that $x^2 - 9 = (x-3)(x+3)$

**From the right** ($x > 3$): $|x - 3| = x - 3$

$$\frac{x - 3}{(x-3)(x+3)} = \frac{1}{x+3}$$

$$\lim_{x \to 3^+} \frac{1}{x+3} = \frac{1}{6}$$

**From the left** ($x < 3$): $|x - 3| = -(x - 3) = 3 - x$

$$\frac{-(x-3)}{(x-3)(x+3)} = \frac{-1}{x+3}$$

$$\lim_{x \to 3^-} \frac{-1}{x+3} = \frac{-1}{6}$$

**Conclusion:** Since $\frac{1}{6} \neq \frac{-1}{6}$, the limit **does not exist**.

---

## The Squeeze Theorem

Sometimes you can't evaluate a limit directly, but you can "trap" it between two functions whose limits you know.

### The Squeeze Theorem Statement

If $g(x) \leq f(x) \leq h(x)$ for all x near a (except possibly at a), and:

$$\lim_{x \to a} g(x) = \lim_{x \to a} h(x) = L$$

Then:

$$\lim_{x \to a} f(x) = L$$

---

### Visual Intuition

```
        h(x) - upper bound
       /    \
      /  f(x) - squeezed function
     / /    \ \
----•---------•---- L (the limit)
     \ \    / /
      \  f(x)
       \    /
        g(x) - lower bound

        ↑
       x = a
```

As x → a, f(x) is squeezed between g(x) and h(x), both approaching L. f(x) has nowhere to go but L!

---

### The Classic Example

$$\lim_{x \to 0} x^2 \sin\left(\frac{1}{x}\right)$$

**The problem:** $\sin(1/x)$ oscillates wildly as $x \to 0$ (between -1 and 1, infinitely fast).

**The solution:** Squeeze it!

We know: $-1 \leq \sin\left(\frac{1}{x}\right) \leq 1$

Multiply by $x^2$ (positive, so inequalities preserve):

$$-x^2 \leq x^2 \sin\left(\frac{1}{x}\right) \leq x^2$$

Now take limits:
- $\lim_{x \to 0} (-x^2) = 0$
- $\lim_{x \to 0} x^2 = 0$

By the Squeeze Theorem:

$$\lim_{x \to 0} x^2 \sin\left(\frac{1}{x}\right) = 0$$

---

### When to Use the Squeeze Theorem

Look for these signals:
- Bounded oscillating functions: $\sin(\cdot)$, $\cos(\cdot)$
- The bounded part is multiplied by something going to 0
- Direct evaluation seems impossible

---

## More Algebraic Techniques

### Technique 1: Factoring Higher Degree Polynomials

**Sum of Cubes:** $a^3 + b^3 = (a + b)(a^2 - ab + b^2)$

**Difference of Cubes:** $a^3 - b^3 = (a - b)(a^2 + ab + b^2)$

**Example:**

$$\lim_{x \to -2} \frac{x^3 + 8}{x + 2}$$

Factor using sum of cubes ($x^3 + 8 = x^3 + 2^3$):

$$= \lim_{x \to -2} \frac{(x + 2)(x^2 - 2x + 4)}{x + 2}$$

$$= \lim_{x \to -2} (x^2 - 2x + 4)$$

$$= 4 + 4 + 4 = 12$$

---

### Technique 2: Rationalizing with Higher Roots

For cube roots, use the identity: $a - b = \frac{a^3 - b^3}{a^2 + ab + b^2}$

**Example:**

$$\lim_{x \to 0} \frac{\sqrt[3]{1+x} - 1}{x}$$

Let $a = \sqrt[3]{1+x}$ and $b = 1$, so $a^3 - b^3 = (1+x) - 1 = x$

Multiply by $\frac{a^2 + ab + b^2}{a^2 + ab + b^2}$:

$$= \lim_{x \to 0} \frac{x}{x \cdot \left[(\sqrt[3]{1+x})^2 + \sqrt[3]{1+x} + 1\right]}$$

$$= \lim_{x \to 0} \frac{1}{(\sqrt[3]{1+x})^2 + \sqrt[3]{1+x} + 1}$$

$$= \frac{1}{1 + 1 + 1} = \frac{1}{3}$$

---

### Technique 3: Combining Fractions Strategically

**Example:**

$$\lim_{x \to 0} \left(\frac{1}{x} - \frac{1}{x^2 + x}\right)$$

Find common denominator:

$$= \lim_{x \to 0} \frac{x^2 + x - x}{x(x^2 + x)}$$

$$= \lim_{x \to 0} \frac{x^2}{x \cdot x(x + 1)}$$

$$= \lim_{x \to 0} \frac{1}{x + 1} = 1$$

---

### Technique 4: Using Special Limits

Remember these from [Limits: The Foundation](/calculus/0203-limits-the-foundation):

$$\lim_{x \to 0} \frac{\sin x}{x} = 1$$

$$\lim_{x \to 0} \frac{1 - \cos x}{x} = 0$$

$$\lim_{x \to 0} \frac{1 - \cos x}{x^2} = \frac{1}{2}$$

**Example using special limits:**

$$\lim_{x \to 0} \frac{\sin(3x)}{x}$$

Rewrite to match the special form:

$$= \lim_{x \to 0} \frac{\sin(3x)}{3x} \cdot 3$$

Let $u = 3x$. As $x \to 0$, $u \to 0$:

$$= 3 \cdot \lim_{u \to 0} \frac{\sin u}{u} = 3 \cdot 1 = 3$$

---

## Determining Limit Existence

### The Existence Theorem

$$\lim_{x \to a} f(x) = L \text{ exists if and only if } \lim_{x \to a^-} f(x) = \lim_{x \to a^+} f(x) = L$$

Both one-sided limits must:
1. Exist
2. Be equal

---

### Types of Non-Existence

**Type 1: Jump Discontinuity**

Left and right limits exist but aren't equal.

$$f(x) = \begin{cases} 1 & x < 0 \\ 2 & x \geq 0 \end{cases}$$

$\lim_{x \to 0^-} f(x) = 1$ but $\lim_{x \to 0^+} f(x) = 2$

---

**Type 2: Infinite Discontinuity (Vertical Asymptote)**

One or both sides approach $\pm\infty$.

$$\lim_{x \to 0} \frac{1}{x}$$

From right: $+\infty$. From left: $-\infty$. Limit DNE.

---

**Type 3: Oscillating Behavior**

Function doesn't settle to any value.

$$\lim_{x \to 0} \sin\left(\frac{1}{x}\right)$$

Oscillates between -1 and 1 forever. Limit DNE.

---

## Key Formulas & Rules

### Epsilon-Delta Definition
For every $\varepsilon > 0$, there exists $\delta > 0$ such that:
$$0 < |x - a| < \delta \implies |f(x) - L| < \varepsilon$$

### Squeeze Theorem
If $g(x) \leq f(x) \leq h(x)$ near $a$ and $\lim_{x \to a} g(x) = \lim_{x \to a} h(x) = L$, then $\lim_{x \to a} f(x) = L$

### Absolute Value Definition
$$|x - a| < \delta \iff a - \delta < x < a + \delta$$

### Limit Existence Criterion
$$\lim_{x \to a} f(x) \text{ exists } \iff \lim_{x \to a^-} f(x) = \lim_{x \to a^+} f(x)$$

---

## Common Mistakes to Avoid

### Mistake 1: Forgetting to Check Both Sides for Absolute Values

❌ Computing limit without considering sign changes

✅ Always split into cases: What happens when the inside is positive vs negative?

### Mistake 2: Misapplying the Squeeze Theorem

❌ Using bounds that don't converge to the same limit

✅ Both bounding functions must approach the SAME value

### Mistake 3: Confusing "Limit DNE" with "Limit = ∞"

❌ Saying $\lim_{x \to 0} \frac{1}{x^2} $ doesn't exist

✅ We write $\lim_{x \to 0} \frac{1}{x^2} = \infty$ to describe the behavior (though technically the limit doesn't exist as a real number)

### Mistake 4: Rushing Through Absolute Value Problems

❌ $\lim_{x \to 0} \frac{|x|}{x} = 1$ (only checked positive side)

✅ Must check both sides: from right = 1, from left = -1, so DNE

---

## AP Exam Tips

### For AP Calculus AB:
- Epsilon-delta is NOT tested computationally, but understanding helps
- Squeeze theorem appears occasionally - know when to use it
- Absolute value limits are common in multiple choice
- Always check one-sided limits for piecewise functions

### For AP Calculus BC:
- Same as AB, but may appear in more complex series contexts
- Squeeze theorem is essential for some convergence arguments

### Time-Saving Strategies:
1. **For absolute values**: Immediately identify where the expression inside equals zero
2. **For oscillating functions multiplied by vanishing terms**: Think Squeeze Theorem
3. **Check answer choices**: If options include "DNE", verify both one-sided limits
4. **Factor aggressively**: Most 0/0 forms can be factored

---

## Practice Problems

### Basic (Problems 1-5)

**1.** Evaluate:

$$\lim_{x \to 2^+} \frac{|x - 2|}{x - 2}$$

---

**2.** Evaluate:

$$\lim_{x \to 0} x \cos\left(\frac{1}{x}\right)$$

---

**3.** Evaluate:

$$\lim_{x \to -1} \frac{x^3 + 1}{x + 1}$$

---

**4.** Evaluate:

$$\lim_{x \to 0} \frac{\sin(5x)}{x}$$

---

**5.** Does the following limit exist? Explain.

$$\lim_{x \to 0} \frac{|x|}{x}$$

### Intermediate (Problems 6-10)

**6.** Evaluate:

$$\lim_{x \to 4} \frac{|x - 4|}{x^2 - 16}$$

---

**7.** Evaluate:

$$\lim_{x \to 0} x^2 \cos\left(\frac{1}{x^2}\right)$$

---

**8.** Evaluate:

$$\lim_{x \to 0} \frac{\sin(2x)}{\sin(3x)}$$

---

**9.** Evaluate:

$$\lim_{x \to 0} \frac{\sqrt{1 + x} - \sqrt{1 - x}}{x}$$

---

**10.** Evaluate:

$$\lim_{x \to 1} \frac{x^3 - 1}{x^2 - 1}$$

### Advanced (Problems 11-15)

**11.** Evaluate:

$$\lim_{x \to 0} \frac{1 - \cos(2x)}{x^2}$$

---

**12.** Evaluate:

$$\lim_{x \to 0} \frac{\tan x - \sin x}{x^3}$$

---

**13.** Evaluate:

$$\lim_{x \to 0} \left(\frac{1}{\sin x} - \frac{1}{x}\right)$$

---

**14.** For what value of $k$ is the following function continuous at $x = 0$?

$$f(x) = \begin{cases} \frac{\sin(3x)}{x} & x \neq 0 \\ k & x = 0 \end{cases}$$

---

**15.** Evaluate:

$$\lim_{x \to 0} \frac{\sqrt[3]{1 + x} - 1}{x}$$

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

Evaluate the following limit:

$$\lim_{x \to 0} \frac{x^2 \sin(1/x)}{x}$$

| Choice | Answer |
|--------|--------|
| **(A)** | 0 |
| **(B)** | 1 |
| **(C)** | -1 |
| **(D)** | Does not exist |

---

#### Problem 17 (Multiple Choice)

Given that $\lim_{x \to 2^-} f(x) = 5$ and $\lim_{x \to 2^+} f(x) = 3$, which of the following **must** be true?

| Choice | Answer |
|--------|--------|
| **(A)** | $f(2) = 4$ |
| **(B)** | $\lim_{x \to 2} f(x) = 4$ |
| **(C)** | $\lim_{x \to 2} f(x)$ does not exist |
| **(D)** | $f$ has a vertical asymptote at $x = 2$ |

---

#### Problem 18 (Free Response)

Let $g(x)$ be defined as:

$$g(x) = \frac{|2x - 6|}{x - 3}$$

Answer the following:

> **(a)** Find $\lim_{x \to 3^+} g(x)$
>
> **(b)** Find $\lim_{x \to 3^-} g(x)$
>
> **(c)** Does $\lim_{x \to 3} g(x)$ exist? Justify your answer.
>
> **(d)** Sketch a graph of $g(x)$ near $x = 3$

---

#### Problem 19 (Free Response - Squeeze Theorem)

Use the Squeeze Theorem to evaluate the following limit. **Show your work and justify each step.**

$$\lim_{x \to 0^+} \sqrt{x} \sin\left(\frac{1}{x}\right)$$

---

#### Problem 20 (Challenging - Piecewise Continuity)

The function $h$ is defined by:

$$h(x) = \begin{cases} ax^2 + b & \text{if } x < 1 \\[8pt] \dfrac{x^2 - 1}{x - 1} & \text{if } x > 1 \end{cases}$$

Find values of $a$ and $b$ such that $\lim_{x \to 1} h(x)$ exists and equals 2.

---

## Answer Key

<details>
<summary><strong>Solution 1</strong></summary>

**Answer**: 1

**Right-hand limit analysis:**

From the right means $x > 2$, so $x - 2 > 0$.

When $x - 2 > 0$: $|x - 2| = x - 2$

$$\lim_{x \to 2^+} \frac{|x - 2|}{x - 2} = \lim_{x \to 2^+} \frac{x - 2}{x - 2}$$

$$= \lim_{x \to 2^+} 1 = 1$$

</details>

---

<details>
<summary><strong>Solution 2</strong></summary>

**Answer**: 0

**Using the Squeeze Theorem:**

We know: $-1 \leq \cos(1/x) \leq 1$ for all $x \neq 0$

**Case 1 - When $x > 0$:**

$$-x \leq x\cos(1/x) \leq x$$

**Case 2 - When $x < 0$:**

$$x \leq x\cos(1/x) \leq -x$$

(Inequalities flip when multiplying by negative)

**Combined:**

In both cases, $|x\cos(1/x)| \leq |x|$

So: $-|x| \leq x\cos(1/x) \leq |x|$

**Applying Squeeze Theorem:**

Since $\lim_{x \to 0} (-|x|) = 0$ and $\lim_{x \to 0} |x| = 0$:

$$\lim_{x \to 0} x\cos(1/x) = 0$$

</details>

---

<details>
<summary><strong>Solution 3</strong></summary>

**Answer**: 3

**Step 1 - Check direct substitution:**

Direct substitution gives $\frac{0}{0}$ (indeterminate).

**Step 2 - Factor using sum of cubes:**

$$x^3 + 1 = (x + 1)(x^2 - x + 1)$$

**Step 3 - Simplify and evaluate:**

$$\lim_{x \to -1} \frac{(x + 1)(x^2 - x + 1)}{x + 1} = \lim_{x \to -1} (x^2 - x + 1)$$

$$= (-1)^2 - (-1) + 1 = 1 + 1 + 1 = 3$$

</details>

---

<details>
<summary><strong>Solution 4</strong></summary>

**Answer**: 5

**Using the special limit:**

We use $\lim_{u \to 0} \frac{\sin u}{u} = 1$

**Rewrite to match special form:**

$$\frac{\sin(5x)}{x} = \frac{\sin(5x)}{5x} \cdot 5$$

**Substitute:**

Let $u = 5x$. As $x \to 0$, $u \to 0$:

$$\lim_{x \to 0} \frac{\sin(5x)}{x} = 5 \cdot \lim_{u \to 0} \frac{\sin u}{u} = 5 \cdot 1 = 5$$

</details>

---

<details>
<summary><strong>Solution 5</strong></summary>

**Answer**: No, the limit does not exist.

**Right-hand limit:**

When $x > 0$: $|x| = x$, so $\frac{|x|}{x} = 1$

$$\lim_{x \to 0^+} \frac{|x|}{x} = 1$$

**Left-hand limit:**

When $x < 0$: $|x| = -x$, so $\frac{|x|}{x} = \frac{-x}{x} = -1$

$$\lim_{x \to 0^-} \frac{|x|}{x} = -1$$

**Conclusion:**

Since $1 \neq -1$, the one-sided limits are not equal, so $\lim_{x \to 0} \frac{|x|}{x}$ does not exist.

</details>

<details>
<summary><strong>Solution 6</strong></summary>

**Answer**: Does not exist

**Setup:**

Note that $x^2 - 16 = (x-4)(x+4)$

**Right-hand limit** ($x > 4$):

When $x > 4$: $|x - 4| = x - 4$

$$\frac{x - 4}{(x-4)(x+4)} = \frac{1}{x + 4}$$

$$\lim_{x \to 4^+} \frac{1}{x+4} = \frac{1}{8}$$

**Left-hand limit** ($x < 4$):

When $x < 4$: $|x - 4| = -(x - 4)$

$$\frac{-(x-4)}{(x-4)(x+4)} = \frac{-1}{x + 4}$$

$$\lim_{x \to 4^-} \frac{-1}{x+4} = \frac{-1}{8}$$

**Conclusion:**

Since $\frac{1}{8} \neq \frac{-1}{8}$, the limit does not exist.

</details>

---

<details>
<summary><strong>Solution 7</strong></summary>

**Answer**: 0

**Using the Squeeze Theorem:**

Since $-1 \leq \cos(1/x^2) \leq 1$:

$$-x^2 \leq x^2 \cos(1/x^2) \leq x^2$$

**Applying Squeeze Theorem:**

Since $\lim_{x \to 0} (-x^2) = 0$ and $\lim_{x \to 0} x^2 = 0$:

$$\lim_{x \to 0} x^2 \cos(1/x^2) = 0$$

</details>

---

<details>
<summary><strong>Solution 8</strong></summary>

**Answer**: $\frac{2}{3}$

**Rewrite using the special limit:**

$$\frac{\sin(2x)}{\sin(3x)} = \frac{\sin(2x)}{2x} \cdot \frac{3x}{\sin(3x)} \cdot \frac{2x}{3x}$$

$$= \frac{\sin(2x)}{2x} \cdot \frac{3x}{\sin(3x)} \cdot \frac{2}{3}$$

**Evaluate each part as $x \to 0$:**

- $\frac{\sin(2x)}{2x} \to 1$
- $\frac{3x}{\sin(3x)} \to 1$ (reciprocal of special limit)

**Final answer:**

$$\lim_{x \to 0} \frac{\sin(2x)}{\sin(3x)} = 1 \cdot 1 \cdot \frac{2}{3} = \frac{2}{3}$$

</details>

---

<details>
<summary><strong>Solution 9</strong></summary>

**Answer**: 1

**Step 1 - Check direct substitution:**

Direct substitution: $\frac{0}{0}$ (indeterminate)

**Step 2 - Rationalize:**

Multiply by $\frac{\sqrt{1+x} + \sqrt{1-x}}{\sqrt{1+x} + \sqrt{1-x}}$

**Numerator becomes:**

$$(\sqrt{1+x} - \sqrt{1-x})(\sqrt{1+x} + \sqrt{1-x}) = (1+x) - (1-x) = 2x$$

**Step 3 - Simplify:**

$$= \lim_{x \to 0} \frac{2x}{x(\sqrt{1+x} + \sqrt{1-x})}$$

$$= \lim_{x \to 0} \frac{2}{\sqrt{1+x} + \sqrt{1-x}}$$

**Step 4 - Substitute:**

$$= \frac{2}{\sqrt{1} + \sqrt{1}} = \frac{2}{2} = 1$$

</details>

---

<details>
<summary><strong>Solution 10</strong></summary>

**Answer**: $\frac{3}{2}$

**Step 1 - Check direct substitution:**

Direct substitution: $\frac{0}{0}$ (indeterminate)

**Step 2 - Factor:**

- Numerator: $x^3 - 1 = (x-1)(x^2 + x + 1)$
- Denominator: $x^2 - 1 = (x-1)(x+1)$

**Step 3 - Cancel and simplify:**

$$= \lim_{x \to 1} \frac{(x-1)(x^2 + x + 1)}{(x-1)(x+1)}$$

$$= \lim_{x \to 1} \frac{x^2 + x + 1}{x + 1}$$

**Step 4 - Substitute:**

$$= \frac{1 + 1 + 1}{1 + 1} = \frac{3}{2}$$

</details>

<details>
<summary><strong>Solution 11</strong></summary>

**Answer**: 2

**Method 1 - Using trig identity:**

Use the identity: $1 - \cos(2x) = 2\sin^2(x)$

$$\lim_{x \to 0} \frac{1 - \cos(2x)}{x^2} = \lim_{x \to 0} \frac{2\sin^2(x)}{x^2}$$

$$= 2 \lim_{x \to 0} \left(\frac{\sin x}{x}\right)^2 = 2 \cdot 1^2 = 2$$

**Method 2 - Using special limit:**

Use $\lim_{u \to 0} \frac{1 - \cos u}{u^2} = \frac{1}{2}$

Let $u = 2x$:

$$\lim_{x \to 0} \frac{1 - \cos(2x)}{x^2} = \lim_{u \to 0} \frac{1 - \cos u}{(u/2)^2}$$

$$= \lim_{u \to 0} \frac{4(1 - \cos u)}{u^2} = 4 \cdot \frac{1}{2} = 2$$

</details>

---

<details>
<summary><strong>Solution 12</strong></summary>

**Answer**: $\frac{1}{2}$

**Step 1 - Rewrite the expression:**

$$\tan x - \sin x = \frac{\sin x}{\cos x} - \sin x = \sin x \left(\frac{1}{\cos x} - 1\right)$$

$$= \sin x \cdot \frac{1 - \cos x}{\cos x}$$

**Step 2 - Substitute into limit:**

$$\frac{\tan x - \sin x}{x^3} = \frac{\sin x (1 - \cos x)}{x^3 \cos x}$$

$$= \frac{\sin x}{x} \cdot \frac{1 - \cos x}{x^2} \cdot \frac{1}{\cos x}$$

**Step 3 - Evaluate each part as $x \to 0$:**

- $\frac{\sin x}{x} \to 1$
- $\frac{1 - \cos x}{x^2} \to \frac{1}{2}$
- $\frac{1}{\cos x} \to 1$

**Final answer:**

$$\lim_{x \to 0} \frac{\tan x - \sin x}{x^3} = 1 \cdot \frac{1}{2} \cdot 1 = \frac{1}{2}$$

</details>

---

<details>
<summary><strong>Solution 13</strong></summary>

**Answer**: 0

**Step 1 - Combine fractions:**

$$\frac{1}{\sin x} - \frac{1}{x} = \frac{x - \sin x}{x \sin x}$$

This is an indeterminate form $\frac{0}{0}$ as $x \to 0$.

**Step 2 - Using Taylor series:**

$$\sin x = x - \frac{x^3}{6} + ...$$

So:

$$x - \sin x = x - \left(x - \frac{x^3}{6} + ...\right) = \frac{x^3}{6} + ...$$

And:

$$x \sin x = x\left(x - \frac{x^3}{6} + ...\right) = x^2 - \frac{x^4}{6} + ...$$

**Step 3 - Evaluate:**

$$\lim_{x \to 0} \frac{x - \sin x}{x \sin x} = \lim_{x \to 0} \frac{\frac{x^3}{6}}{x^2} = \lim_{x \to 0} \frac{x}{6} = 0$$

</details>

---

<details>
<summary><strong>Solution 14</strong></summary>

**Answer**: $k = 3$

**Continuity condition:**

For continuity at $x = 0$, we need:

$$\lim_{x \to 0} f(x) = f(0) = k$$

**Find the limit:**

$$\lim_{x \to 0} \frac{\sin(3x)}{x} = \lim_{x \to 0} \frac{\sin(3x)}{3x} \cdot 3$$

$$= 1 \cdot 3 = 3$$

**Conclusion:**

So we need $k = 3$.

</details>

---

<details>
<summary><strong>Solution 15</strong></summary>

**Answer**: $\frac{1}{3}$

**Step 1 - Check direct substitution:**

Direct substitution: $\frac{0}{0}$ (indeterminate)

**Step 2 - Cube root rationalization:**

Let $a = \sqrt[3]{1+x}$, so $a^3 = 1+x$.

We use: $a - 1 = \frac{a^3 - 1}{a^2 + a + 1}$

**Step 3 - Apply the identity:**

$$\sqrt[3]{1+x} - 1 = \frac{(1+x) - 1}{(\sqrt[3]{1+x})^2 + \sqrt[3]{1+x} + 1}$$

$$= \frac{x}{(\sqrt[3]{1+x})^2 + \sqrt[3]{1+x} + 1}$$

**Step 4 - Simplify and evaluate:**

$$\frac{\sqrt[3]{1+x} - 1}{x} = \frac{1}{(\sqrt[3]{1+x})^2 + \sqrt[3]{1+x} + 1}$$

$$\lim_{x \to 0} \frac{1}{(\sqrt[3]{1+x})^2 + \sqrt[3]{1+x} + 1} = \frac{1}{1 + 1 + 1} = \frac{1}{3}$$

</details>

<details>
<summary><strong>Solution 16</strong></summary>

**Answer**: (A) 0

**Simplify the expression:**

$$\frac{x^2 \sin(1/x)}{x} = x \sin(1/x)$$

**Apply Squeeze Theorem:**

Since $-1 \leq \sin(1/x) \leq 1$:

$$-|x| \leq x\sin(1/x) \leq |x|$$

As $x \to 0$: both bounds approach 0.

**Conclusion:**

By Squeeze Theorem: $\lim_{x \to 0} x\sin(1/x) = 0$

</details>

---

<details>
<summary><strong>Solution 17</strong></summary>

**Answer**: (C)

**Analysis:**

Since $\lim_{x \to 2^-} f(x) = 5 \neq 3 = \lim_{x \to 2^+} f(x)$, the one-sided limits are not equal.

By the existence theorem, $\lim_{x \to 2} f(x)$ does not exist.

**Why other choices are wrong:**

- **(A)** is wrong: We know nothing about $f(2)$
- **(B)** is wrong: The limit doesn't exist, not equal to 4
- **(D)** is wrong: A jump discontinuity is not a vertical asymptote

</details>

---

<details>
<summary><strong>Solution 18</strong></summary>

**(a) Answer**: 2

**Right-hand limit:**

For $x > 3$: $2x - 6 > 0$, so $|2x - 6| = 2x - 6$

$$g(x) = \frac{2x - 6}{x - 3} = \frac{2(x - 3)}{x - 3} = 2$$

$$\lim_{x \to 3^+} g(x) = 2$$

---

**(b) Answer**: -2

**Left-hand limit:**

For $x < 3$: $2x - 6 < 0$, so $|2x - 6| = -(2x - 6) = 6 - 2x$

$$g(x) = \frac{6 - 2x}{x - 3} = \frac{-2(x - 3)}{x - 3} = -2$$

$$\lim_{x \to 3^-} g(x) = -2$$

---

**(c) Answer**: No

**Conclusion:**

The limit does not exist because:

$$\lim_{x \to 3^+} g(x) = 2 \neq -2 = \lim_{x \to 3^-} g(x)$$

For a limit to exist, the left-hand and right-hand limits must be equal.

---

**(d) Graph sketch**:

```
y
|
2 |. . . . . ●−−−−−−−−−−
  |          |
  |          |
  |----------|----------→ x
  |          3
  |          |
-2|−−−−−−−−−−○ . . . . .
  |
```

The function equals 2 for all $x > 3$ and equals -2 for all $x < 3$. There's a jump discontinuity at $x = 3$.

</details>

---

<details>
<summary><strong>Solution 19</strong></summary>

**Answer**: 0

**Step 1 - Identify bounds:**

For all $x > 0$: $-1 \leq \sin(1/x) \leq 1$

**Step 2 - Multiply by $\sqrt{x}$:**

Since $\sqrt{x} > 0$ for $x > 0$, inequalities preserve:

$$-\sqrt{x} \leq \sqrt{x}\sin(1/x) \leq \sqrt{x}$$

**Step 3 - Take limits of bounds:**

$$\lim_{x \to 0^+} (-\sqrt{x}) = 0$$

$$\lim_{x \to 0^+} \sqrt{x} = 0$$

**Step 4 - Apply Squeeze Theorem:**

Since both bounds approach 0:

$$\lim_{x \to 0^+} \sqrt{x}\sin(1/x) = 0$$

**Justification:**

The Squeeze Theorem applies because we have $g(x) \leq f(x) \leq h(x)$ where:
- $g(x) = -\sqrt{x}$
- $f(x) = \sqrt{x}\sin(1/x)$
- $h(x) = \sqrt{x}$

And both $g$ and $h$ approach 0 as $x \to 0^+$.

</details>

---

<details>
<summary><strong>Solution 20</strong></summary>

**Answer**: $a = 1$, $b = 1$

**Step 1 - Find the right-hand limit:**

For $x > 1$:

$$h(x) = \frac{x^2 - 1}{x - 1} = \frac{(x-1)(x+1)}{x-1} = x + 1$$

$$\lim_{x \to 1^+} h(x) = \lim_{x \to 1^+} (x + 1) = 2$$

**Step 2 - Find the left-hand limit:**

For $x < 1$:

$$\lim_{x \to 1^-} h(x) = \lim_{x \to 1^-} (ax^2 + b) = a(1)^2 + b = a + b$$

**Step 3 - Set up equation:**

For the limit to exist and equal 2, we need:

$$a + b = 2$$

**Step 4 - Choose values:**

This gives infinitely many solutions. The simplest choice: $a = 1$, $b = 1$

**Verification:**

- Left limit: $\lim_{x \to 1^-} (x^2 + 1) = 2$ ✓
- Right limit: $\lim_{x \to 1^+} (x + 1) = 2$ ✓
- Both equal 2, so $\lim_{x \to 1} h(x) = 2$ ✓

</details>

---

## What's Next

Now that you have a deeper understanding of limits, we'll explore:

- [Limit Laws & Techniques](/calculus/limit-laws-techniques) - Systematic rules for combining limits
- [One-Sided Limits](/calculus/0206-one-sided-limits) - Left and right limits in more detail
- [Limits at Infinity](/calculus/0207-limits-at-infinity) - What happens as x → ∞

The precision you've gained with epsilon-delta thinking will serve you well as we move toward derivatives - which are themselves defined as limits!

---

*"The limit is the fundamental idea behind calculus. Once you truly understand what 'approaching' means, everything else falls into place."*

---

<div align="center">

[← Limits: The Foundation](calculus/limits-the-foundation.md) | [Limit Laws & Techniques →](calculus/limit-laws-and-techniques.md)

</div>
