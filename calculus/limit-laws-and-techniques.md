# Limit Laws & Techniques

*You've learned what limits are and when they exist. Now it's time to build your toolkit - the rules and techniques that let you evaluate almost any limit quickly and confidently.*

---

## What You'll Learn

- The fundamental limit laws and how to apply them
- When and why each technique works
- A systematic approach to evaluating any limit
- Special limits you should memorize
- How to recognize which technique to use

---

## Prerequisites

Before diving in, make sure you're comfortable with:
- [Limits: The Foundation](/calculus/limits-the-foundation) - basic limit concepts
- [Understanding Limits](/calculus/understanding-limits) - epsilon-delta intuition, when limits exist
- [Functions Refresher](/calculus/functions-refresher) - factoring, rationalizing, function composition

---

## The Core Concept

### Why Do We Need Limit Laws?

Imagine you need to find:

$$\lim_{x \to 2} (x^2 + 3x - 1)$$

You *could* make a table of values approaching 2 from both sides... but that's tedious.

Instead, limit laws let us break complex limits into simple pieces, evaluate each piece, and combine them. It's like having a set of power tools instead of doing everything by hand.

---

## The Fundamental Limit Laws

If $\lim_{x \to a} f(x) = L$ and $\lim_{x \to a} g(x) = M$, then:

### Law 1: Constant Law

$$\lim_{x \to a} c = c$$

*The limit of a constant is just that constant.*

**Example:** $\lim_{x \to 5} 7 = 7$

---

### Law 2: Identity Law

$$\lim_{x \to a} x = a$$

*As x approaches a, x approaches a. (Obvious, but important!)*

**Example:** $\lim_{x \to 3} x = 3$

---

### Law 3: Sum/Difference Law

$$\lim_{x \to a} [f(x) \pm g(x)] = L \pm M$$

*The limit of a sum is the sum of the limits.*

**Example:** $\lim_{x \to 2} (x^2 + 3x) = \lim_{x \to 2} x^2 + \lim_{x \to 2} 3x = 4 + 6 = 10$

---

### Law 4: Constant Multiple Law

$$\lim_{x \to a} [c \cdot f(x)] = c \cdot L$$

*Constants can be pulled out of limits.*

**Example:** $\lim_{x \to 4} 5x = 5 \cdot \lim_{x \to 4} x = 5 \cdot 4 = 20$

---

### Law 5: Product Law

$$\lim_{x \to a} [f(x) \cdot g(x)] = L \cdot M$$

*The limit of a product is the product of the limits.*

**Example:** $\lim_{x \to 3} (x \cdot x^2) = 3 \cdot 9 = 27$

---

### Law 6: Quotient Law

$$\lim_{x \to a} \frac{f(x)}{g(x)} = \frac{L}{M}, \quad \text{provided } M \neq 0$$

*The limit of a quotient is the quotient of the limits (if the denominator's limit isn't zero).*

**Example:** $\lim_{x \to 2} \frac{x + 1}{x - 1} = \frac{3}{1} = 3$

---

### Law 7: Power Law

$$\lim_{x \to a} [f(x)]^n = L^n$$

*The limit of a power is the power of the limit.*

**Example:** $\lim_{x \to 2} x^3 = (\lim_{x \to 2} x)^3 = 2^3 = 8$

---

### Law 8: Root Law

$$\lim_{x \to a} \sqrt[n]{f(x)} = \sqrt[n]{L}$$

*Provided L > 0 when n is even.*

**Example:** $\lim_{x \to 9} \sqrt{x} = \sqrt{9} = 3$

---

## The Master Theorem: Direct Substitution

Here's the powerful consequence of all these laws:

> **Direct Substitution Property:** If f(x) is a polynomial, rational function, or any combination of continuous functions, and f is defined at x = a, then:
> $$\lim_{x \to a} f(x) = f(a)$$

In other words: **just plug in the value!**

### When Direct Substitution Works

| Function Type | Direct Sub Works? |
|---------------|-------------------|
| Polynomials | Always ✓ |
| Rational functions (denom ≠ 0) | Yes ✓ |
| Trig functions (at defined points) | Yes ✓ |
| Exponential functions | Always ✓ |
| Root functions (positive radicand) | Yes ✓ |

### When Direct Substitution Fails

Direct substitution fails when you get:
- $\frac{0}{0}$ — **Indeterminate form** (need more work)
- $\frac{\text{number}}{0}$ — **Undefined** (may be infinite or DNE)

---

## Techniques for Indeterminate Forms

When direct substitution gives $\frac{0}{0}$, use one of these techniques:

### Technique 1: Factoring

**When to use:** The numerator and/or denominator are polynomials.

**Strategy:** Factor, cancel the common factor, then substitute.

**Example:**

$$\lim_{x \to 3} \frac{x^2 - 9}{x - 3}$$

1. Direct substitution: $\frac{9 - 9}{3 - 3} = \frac{0}{0}$ ✗
2. Factor: $\frac{(x-3)(x+3)}{x-3}$
3. Cancel: $x + 3$ (valid since $x \neq 3$ in a limit)
4. Substitute: $3 + 3 = 6$

**Common factoring patterns:**
- Difference of squares: $a^2 - b^2 = (a-b)(a+b)$
- Sum of cubes: $a^3 + b^3 = (a+b)(a^2 - ab + b^2)$
- Difference of cubes: $a^3 - b^3 = (a-b)(a^2 + ab + b^2)$

---

### Technique 2: Rationalizing

**When to use:** Square roots (or other roots) in numerator or denominator.

**Strategy:** Multiply by the conjugate over itself.

**Example:**

$$\lim_{x \to 0} \frac{\sqrt{x + 4} - 2}{x}$$

1. Direct substitution: $\frac{0}{0}$ ✗
2. Multiply by conjugate:
$$= \lim_{x \to 0} \frac{\sqrt{x+4} - 2}{x} \cdot \frac{\sqrt{x+4} + 2}{\sqrt{x+4} + 2}$$
3. Simplify numerator: $(x + 4) - 4 = x$
$$= \lim_{x \to 0} \frac{x}{x(\sqrt{x+4} + 2)}$$
4. Cancel: $\frac{1}{\sqrt{x+4} + 2}$
5. Substitute: $\frac{1}{\sqrt{4} + 2} = \frac{1}{4}$

**Remember:** The conjugate of $\sqrt{a} - b$ is $\sqrt{a} + b$

---

### Technique 3: Common Denominators

**When to use:** Complex fractions (fractions within fractions).

**Strategy:** Combine fractions in numerator/denominator, then simplify.

**Example:**

$$\lim_{x \to 0} \frac{\frac{1}{x+3} - \frac{1}{3}}{x}$$

1. Direct substitution: $\frac{0}{0}$ ✗
2. Combine fractions in numerator:
$$\frac{1}{x+3} - \frac{1}{3} = \frac{3 - (x+3)}{3(x+3)} = \frac{-x}{3(x+3)}$$
3. Rewrite:
$$= \lim_{x \to 0} \frac{\frac{-x}{3(x+3)}}{x} = \lim_{x \to 0} \frac{-x}{3x(x+3)}$$
4. Cancel x:
$$= \lim_{x \to 0} \frac{-1}{3(x+3)} = \frac{-1}{9}$$

---

### Technique 4: Expanding

**When to use:** Expressions like $(a + h)^n$ where substitution creates $\frac{0}{0}$.

**Strategy:** Expand the polynomial, simplify, then substitute.

**Example:**

$$\lim_{h \to 0} \frac{(x + h)^2 - x^2}{h}$$

1. Expand: $(x+h)^2 = x^2 + 2xh + h^2$
2. Simplify:
$$= \lim_{h \to 0} \frac{x^2 + 2xh + h^2 - x^2}{h} = \lim_{h \to 0} \frac{2xh + h^2}{h}$$
3. Factor: $= \lim_{h \to 0} \frac{h(2x + h)}{h} = \lim_{h \to 0} (2x + h)$
4. Substitute: $= 2x$

*(This is the derivative of $x^2$!)*

---

### Technique 5: Using Special Limits

**When to use:** Limits involving trig functions or exponentials.

**The Big Three (Memorize These!):**

$$\lim_{x \to 0} \frac{\sin x}{x} = 1$$

$$\lim_{x \to 0} \frac{1 - \cos x}{x} = 0$$

$$\lim_{x \to 0} \frac{1 - \cos x}{x^2} = \frac{1}{2}$$

**Example:**

$$\lim_{x \to 0} \frac{\sin(5x)}{3x}$$

Rewrite to match the special form:
$$= \lim_{x \to 0} \frac{\sin(5x)}{5x} \cdot \frac{5x}{3x} = 1 \cdot \frac{5}{3} = \frac{5}{3}$$

---

### Technique 6: Substitution (Change of Variable)

**When to use:** Complex expressions that can be simplified with a substitution.

**Strategy:** Let $u = $ some expression, rewrite the limit in terms of u.

**Example:**

$$\lim_{x \to 1} \frac{\sin(x - 1)}{x - 1}$$

Let $u = x - 1$. As $x \to 1$, $u \to 0$.

$$= \lim_{u \to 0} \frac{\sin u}{u} = 1$$

---

## The Decision Flowchart

When evaluating $\lim_{x \to a} f(x)$:

```
Step 1: Try Direct Substitution
         |
         v
    Does it give a number?
    /                    \
  YES                    NO
   |                      |
   v                      v
 Done!              What form?
                   /          \
                0/0          k/0 (k≠0)
                 |              |
                 v              v
          Try techniques:   Infinite limit
          1. Factor         or DNE
          2. Rationalize    (check both sides)
          3. Common denom
          4. Expand
          5. Special limits
          6. Substitution
```

---

## More Special Limits

### Limits Involving e

$$\lim_{x \to 0} \frac{e^x - 1}{x} = 1$$

$$\lim_{x \to \infty} \left(1 + \frac{1}{x}\right)^x = e$$

$$\lim_{x \to 0} (1 + x)^{1/x} = e$$

### Limits Involving ln

$$\lim_{x \to 0} \frac{\ln(1 + x)}{x} = 1$$

### General Trig Limits

For any constant $k$:

$$\lim_{x \to 0} \frac{\sin(kx)}{x} = k$$

$$\lim_{x \to 0} \frac{\sin(kx)}{kx} = 1$$

$$\lim_{x \to 0} \frac{\tan x}{x} = 1$$

---

## Worked Examples

### Example 1: Direct Substitution with Polynomial

$$\lim_{x \to -2} (x^3 + 4x^2 - 3x + 7)$$

**Solution:**

Polynomials are continuous everywhere, so use direct substitution:

$$= (-2)^3 + 4(-2)^2 - 3(-2) + 7$$
$$= -8 + 16 + 6 + 7 = 21$$

---

### Example 2: Factoring with Difference of Cubes

$$\lim_{x \to 2} \frac{x^3 - 8}{x - 2}$$

**Solution:**

1. Direct sub: $\frac{0}{0}$ ✗
2. Factor using $a^3 - b^3 = (a-b)(a^2 + ab + b^2)$:
$$x^3 - 8 = (x-2)(x^2 + 2x + 4)$$
3. Cancel:
$$= \lim_{x \to 2} \frac{(x-2)(x^2 + 2x + 4)}{x-2} = \lim_{x \to 2} (x^2 + 2x + 4)$$
4. Substitute: $= 4 + 4 + 4 = 12$

---

### Example 3: Rationalizing the Numerator

$$\lim_{x \to 7} \frac{\sqrt{x + 2} - 3}{x - 7}$$

**Solution:**

1. Direct sub: $\frac{0}{0}$ ✗
2. Multiply by conjugate:
$$= \lim_{x \to 7} \frac{\sqrt{x+2} - 3}{x - 7} \cdot \frac{\sqrt{x+2} + 3}{\sqrt{x+2} + 3}$$
3. Simplify numerator: $(x + 2) - 9 = x - 7$
$$= \lim_{x \to 7} \frac{x - 7}{(x-7)(\sqrt{x+2} + 3)}$$
4. Cancel:
$$= \lim_{x \to 7} \frac{1}{\sqrt{x+2} + 3} = \frac{1}{3 + 3} = \frac{1}{6}$$

---

### Example 4: Complex Fraction

$$\lim_{h \to 0} \frac{\frac{1}{(x+h)^2} - \frac{1}{x^2}}{h}$$

**Solution:**

1. Combine fractions in numerator:
$$\frac{1}{(x+h)^2} - \frac{1}{x^2} = \frac{x^2 - (x+h)^2}{x^2(x+h)^2}$$

2. Expand $(x+h)^2 = x^2 + 2xh + h^2$:
$$= \frac{x^2 - x^2 - 2xh - h^2}{x^2(x+h)^2} = \frac{-2xh - h^2}{x^2(x+h)^2}$$

3. Rewrite the full limit:
$$= \lim_{h \to 0} \frac{-2xh - h^2}{h \cdot x^2(x+h)^2}$$

4. Factor and cancel h:
$$= \lim_{h \to 0} \frac{h(-2x - h)}{h \cdot x^2(x+h)^2} = \lim_{h \to 0} \frac{-2x - h}{x^2(x+h)^2}$$

5. Substitute:
$$= \frac{-2x}{x^2 \cdot x^2} = \frac{-2x}{x^4} = \frac{-2}{x^3}$$

---

### Example 5: Special Trig Limit

$$\lim_{x \to 0} \frac{\sin(3x)}{\sin(5x)}$$

**Solution:**

Rewrite to use $\frac{\sin u}{u} \to 1$:

$$= \lim_{x \to 0} \frac{\sin(3x)}{3x} \cdot \frac{3x}{5x} \cdot \frac{5x}{\sin(5x)}$$

$$= \lim_{x \to 0} \frac{\sin(3x)}{3x} \cdot \frac{3}{5} \cdot \frac{5x}{\sin(5x)}$$

$$= 1 \cdot \frac{3}{5} \cdot 1 = \frac{3}{5}$$

---

## Key Formulas & Rules

### The Eight Limit Laws

| Law | Formula |
|-----|---------|
| Constant | $\lim_{x \to a} c = c$ |
| Identity | $\lim_{x \to a} x = a$ |
| Sum/Diff | $\lim [f \pm g] = \lim f \pm \lim g$ |
| Constant Multiple | $\lim [cf] = c \cdot \lim f$ |
| Product | $\lim [f \cdot g] = \lim f \cdot \lim g$ |
| Quotient | $\lim [f/g] = \lim f / \lim g$ (if $\lim g \neq 0$) |
| Power | $\lim [f^n] = (\lim f)^n$ |
| Root | $\lim \sqrt[n]{f} = \sqrt[n]{\lim f}$ |

### Special Limits to Memorize

| Limit | Value |
|-------|-------|
| $\lim_{x \to 0} \frac{\sin x}{x}$ | 1 |
| $\lim_{x \to 0} \frac{\tan x}{x}$ | 1 |
| $\lim_{x \to 0} \frac{1 - \cos x}{x}$ | 0 |
| $\lim_{x \to 0} \frac{1 - \cos x}{x^2}$ | $\frac{1}{2}$ |
| $\lim_{x \to 0} \frac{e^x - 1}{x}$ | 1 |
| $\lim_{x \to 0} \frac{\ln(1+x)}{x}$ | 1 |

---

## Common Mistakes to Avoid

### Mistake 1: Stopping at 0/0

❌ "I got 0/0, so the answer is 0" or "the limit doesn't exist"

✅ 0/0 is *indeterminate* - it means you need to use a technique to simplify further

### Mistake 2: Applying Quotient Law When Denominator → 0

❌ Using $\lim \frac{f}{g} = \frac{\lim f}{\lim g}$ when $\lim g = 0$

✅ The quotient law requires $\lim g \neq 0$. When $\lim g = 0$, you need a different approach.

### Mistake 3: Forgetting the Conjugate for Both Terms

❌ Conjugate of $\sqrt{x+1} - \sqrt{x}$ is $\sqrt{x+1} + \sqrt{x+1}$

✅ Conjugate of $\sqrt{x+1} - \sqrt{x}$ is $\sqrt{x+1} + \sqrt{x}$

### Mistake 4: Misusing Special Limits

❌ $\lim_{x \to 0} \frac{\sin(3x)}{x} = 1$

✅ $\lim_{x \to 0} \frac{\sin(3x)}{x} = 3$ (the argument must match the denominator)

### Mistake 5: Canceling Before Factoring

❌ $\frac{x^2 - 4}{x - 2} = \frac{x^2}{x} - \frac{4}{2}$ (WRONG!)

✅ Factor first: $\frac{(x-2)(x+2)}{x-2} = x + 2$

---

## AP Exam Tips

### For AP Calculus AB:
- Limit laws and techniques appear throughout the exam
- Most limits can be done with factoring or rationalizing
- Know your special trig limits cold
- Practice recognizing which technique to use quickly

### For AP Calculus BC:
- Same as AB, plus limits in series contexts
- L'Hôpital's Rule (coming later) is another powerful tool

### Time-Saving Strategies:

1. **Always try direct substitution first** - takes 5 seconds
2. **See a difference of squares?** Factor immediately
3. **See a square root?** Think conjugate
4. **See $\sin$ or $\cos$ over $x$?** Think special limits
5. **On multiple choice:** If factoring looks messy, estimate with a calculator

### Common AP Question Types:

1. "Evaluate the limit" (straightforward computation)
2. "For what value of k does the limit exist?" (find k so numerator has the right factor)
3. "Which limit equals the derivative?" (recognize limit definition)
4. Piecewise functions (check one-sided limits)

---

## Practice Problems

### Basic (Problems 1-5)

**1.** Evaluate:

$$\lim_{x \to 3} (2x^2 - 5x + 1)$$

---

**2.** Evaluate:

$$\lim_{x \to -1} \frac{x^2 - 1}{x + 1}$$

---

**3.** Evaluate:

$$\lim_{x \to 4} \frac{x - 4}{\sqrt{x} - 2}$$

---

**4.** Evaluate:

$$\lim_{x \to 0} \frac{\sin(4x)}{x}$$

---

**5.** Evaluate:

$$\lim_{x \to 2} \frac{x^2 - 4}{x^2 - 5x + 6}$$

### Intermediate (Problems 6-10)

**6.** Evaluate:

$$\lim_{x \to 1} \frac{x^3 - 1}{x^2 - 1}$$

---

**7.** Evaluate:

$$\lim_{x \to 0} \frac{\sqrt{1 + x} - 1}{x}$$

---

**8.** Evaluate:

$$\lim_{h \to 0} \frac{(3 + h)^2 - 9}{h}$$

---

**9.** Evaluate:

$$\lim_{x \to 0} \frac{\tan(2x)}{3x}$$

---

**10.** Evaluate:

$$\lim_{x \to 0} \frac{\frac{1}{2+x} - \frac{1}{2}}{x}$$

### Advanced (Problems 11-15)

**11.** Evaluate:

$$\lim_{x \to 0} \frac{1 - \cos(3x)}{x^2}$$

---

**12.** Evaluate:

$$\lim_{x \to 8} \frac{\sqrt[3]{x} - 2}{x - 8}$$

---

**13.** Evaluate:

$$\lim_{x \to 0} \frac{\sqrt{1+x} - \sqrt{1-x}}{x}$$

---

**14.** Evaluate:

$$\lim_{x \to 0} x \cot(3x)$$

*(Hint: $\cot \theta = \frac{\cos \theta}{\sin \theta}$)*

---

**15.** Evaluate:

$$\lim_{x \to 4} \frac{x^2 - 3x - 4}{x^2 - 8x + 16}$$

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

Evaluate the following limit:

$$\lim_{x \to 2} \frac{x^3 - 8}{x^2 - 4}$$

| Choice | Answer |
|--------|--------|
| **(A)** | 0 |
| **(B)** | 2 |
| **(C)** | 3 |
| **(D)** | Does not exist |

---

#### Problem 17 (Multiple Choice)

Given that $\lim_{x \to 0} \frac{\sin(kx)}{2x} = 3$, find the value of $k$.

| Choice | Answer |
|--------|--------|
| **(A)** | $\frac{3}{2}$ |
| **(B)** | 3 |
| **(C)** | 6 |
| **(D)** | $\frac{2}{3}$ |

---

#### Problem 18 (Free Response)

Let $f(x) = \frac{x^2 - 2x - 8}{x^2 - 16}$

Answer the following:

> **(a)** Find $\lim_{x \to 4} f(x)$
>
> **(b)** Find $\lim_{x \to -4} f(x)$, or explain why it does not exist.
>
> **(c)** At which x-value does $f$ have a hole? At which does it have a vertical asymptote?

---

#### Problem 19 (Free Response - Derivative Definition)

The limit below represents the derivative of some function $f$ at some value $x = a$:

$$\lim_{h \to 0} \frac{(2+h)^3 - 8}{h}$$

Answer the following:

> **(a)** Evaluate this limit.
>
> **(b)** What is $f(x)$?
>
> **(c)** What is $a$?

---

#### Problem 20 (Challenging - Find k)

For what value of $k$ does the following limit exist?

$$\lim_{x \to 3} \frac{x^2 + kx - 12}{x - 3}$$

Once you find $k$, evaluate the limit.

---

## Answer Key

<details>
<summary><strong>Solution 1</strong></summary>

**Answer**: 4

**Direct substitution:**

Polynomials are continuous everywhere, so:

$$\lim_{x \to 3} (2x^2 - 5x + 1) = 2(3)^2 - 5(3) + 1$$

$$= 18 - 15 + 1 = 4$$

</details>

---

<details>
<summary><strong>Solution 2</strong></summary>

**Answer**: -2

**Step 1 - Check direct substitution:**

Direct substitution: $\frac{0}{0}$ (indeterminate)

**Step 2 - Factor numerator:**

$$x^2 - 1 = (x+1)(x-1)$$

**Step 3 - Cancel:**

$$\frac{(x+1)(x-1)}{x+1} = x - 1$$

**Step 4 - Substitute:**

$$\lim_{x \to -1} (x - 1) = -1 - 1 = -2$$

</details>

---

<details>
<summary><strong>Solution 3</strong></summary>

**Answer**: 4

**Step 1 - Check direct substitution:**

Direct substitution: $\frac{0}{0}$ (indeterminate)

**Step 2 - Rationalize:**

Multiply by $\frac{\sqrt{x} + 2}{\sqrt{x} + 2}$:

$$= \lim_{x \to 4} \frac{(x-4)(\sqrt{x} + 2)}{(\sqrt{x} - 2)(\sqrt{x} + 2)}$$

**Step 3 - Simplify denominator:**

$$= \lim_{x \to 4} \frac{(x-4)(\sqrt{x} + 2)}{x - 4}$$

**Step 4 - Cancel and substitute:**

$$= \lim_{x \to 4} (\sqrt{x} + 2) = 2 + 2 = 4$$

</details>

---

<details>
<summary><strong>Solution 4</strong></summary>

**Answer**: 4

**Using the special limit:**

We use $\lim_{u \to 0} \frac{\sin u}{u} = 1$

**Rewrite:**

$$\lim_{x \to 0} \frac{\sin(4x)}{x} = \lim_{x \to 0} \frac{\sin(4x)}{4x} \cdot 4$$

$$= 1 \cdot 4 = 4$$

</details>

---

<details>
<summary><strong>Solution 5</strong></summary>

**Answer**: -4

**Step 1 - Check direct substitution:**

Direct substitution: $\frac{0}{0}$ (indeterminate)

**Step 2 - Factor:**

- Numerator: $x^2 - 4 = (x-2)(x+2)$
- Denominator: $x^2 - 5x + 6 = (x-2)(x-3)$

**Step 3 - Cancel:**

$$= \lim_{x \to 2} \frac{(x-2)(x+2)}{(x-2)(x-3)} = \lim_{x \to 2} \frac{x+2}{x-3}$$

**Step 4 - Substitute:**

$$= \frac{2+2}{2-3} = \frac{4}{-1} = -4$$

</details>

<details>
<summary><strong>Solution 6</strong></summary>

**Answer**: $\frac{3}{2}$

**Step 1 - Check direct substitution:**

Direct substitution: $\frac{0}{0}$ (indeterminate)

**Step 2 - Factor:**

- Numerator: $x^3 - 1 = (x-1)(x^2 + x + 1)$
- Denominator: $x^2 - 1 = (x-1)(x+1)$

**Step 3 - Cancel:**

$$= \lim_{x \to 1} \frac{(x-1)(x^2 + x + 1)}{(x-1)(x+1)}$$

$$= \lim_{x \to 1} \frac{x^2 + x + 1}{x + 1}$$

**Step 4 - Substitute:**

$$= \frac{1 + 1 + 1}{1 + 1} = \frac{3}{2}$$

</details>

---

<details>
<summary><strong>Solution 7</strong></summary>

**Answer**: $\frac{1}{2}$

**Step 1 - Check direct substitution:**

Direct substitution: $\frac{0}{0}$ (indeterminate)

**Step 2 - Rationalize:**

Multiply by $\frac{\sqrt{1+x} + 1}{\sqrt{1+x} + 1}$:

$$= \lim_{x \to 0} \frac{(\sqrt{1+x} - 1)(\sqrt{1+x} + 1)}{x(\sqrt{1+x} + 1)}$$

**Step 3 - Simplify numerator:**

$(1 + x) - 1 = x$

$$= \lim_{x \to 0} \frac{x}{x(\sqrt{1+x} + 1)}$$

**Step 4 - Cancel:**

$$= \lim_{x \to 0} \frac{1}{\sqrt{1+x} + 1}$$

**Step 5 - Substitute:**

$$= \frac{1}{\sqrt{1} + 1} = \frac{1}{2}$$

</details>

---

<details>
<summary><strong>Solution 8</strong></summary>

**Answer**: 6

**Step 1 - Expand:**

$$(3+h)^2 = 9 + 6h + h^2$$

**Step 2 - Substitute:**

$$= \lim_{h \to 0} \frac{9 + 6h + h^2 - 9}{h} = \lim_{h \to 0} \frac{6h + h^2}{h}$$

**Step 3 - Factor:**

$$= \lim_{h \to 0} \frac{h(6 + h)}{h} = \lim_{h \to 0} (6 + h)$$

**Step 4 - Substitute:**

$$= 6$$

**Note:** This is the derivative of $x^2$ at $x = 3$.

</details>

---

<details>
<summary><strong>Solution 9</strong></summary>

**Answer**: $\frac{2}{3}$

**Rewrite using trig identity:**

$$\tan x = \frac{\sin x}{\cos x}$$

So:

$$\lim_{x \to 0} \frac{\tan(2x)}{3x} = \lim_{x \to 0} \frac{\sin(2x)}{3x \cos(2x)}$$

**Apply special limit:**

$$= \lim_{x \to 0} \frac{\sin(2x)}{2x} \cdot \frac{2}{3} \cdot \frac{1}{\cos(2x)}$$

$$= 1 \cdot \frac{2}{3} \cdot 1 = \frac{2}{3}$$

</details>

---

<details>
<summary><strong>Solution 10</strong></summary>

**Answer**: $-\frac{1}{4}$

**Step 1 - Combine fractions in numerator:**

$$\frac{1}{2+x} - \frac{1}{2} = \frac{2 - (2+x)}{2(2+x)} = \frac{-x}{2(2+x)}$$

**Step 2 - Rewrite:**

$$= \lim_{x \to 0} \frac{\frac{-x}{2(2+x)}}{x} = \lim_{x \to 0} \frac{-x}{2x(2+x)}$$

**Step 3 - Cancel x:**

$$= \lim_{x \to 0} \frac{-1}{2(2+x)}$$

**Step 4 - Substitute:**

$$= \frac{-1}{2(2)} = -\frac{1}{4}$$

</details>

<details>
<summary><strong>Solution 11</strong></summary>

**Answer**: $\frac{9}{2}$

**Method 1 - Using special limit:**

Use $\lim_{u \to 0} \frac{1 - \cos u}{u^2} = \frac{1}{2}$

Let $u = 3x$, so as $x \to 0$, $u \to 0$:

$$\lim_{x \to 0} \frac{1 - \cos(3x)}{x^2} = \lim_{x \to 0} \frac{1 - \cos(3x)}{(3x)^2} \cdot 9$$

$$= \frac{1}{2} \cdot 9 = \frac{9}{2}$$

**Method 2 - Using trig identity:**

Use $1 - \cos(3x) = 2\sin^2(3x/2)$:

$$= \lim_{x \to 0} \frac{2\sin^2(3x/2)}{x^2}$$

$$= 2 \lim_{x \to 0} \left(\frac{\sin(3x/2)}{x}\right)^2$$

$$= 2 \lim_{x \to 0} \left(\frac{\sin(3x/2)}{3x/2} \cdot \frac{3}{2}\right)^2$$

$$= 2 \cdot \left(1 \cdot \frac{3}{2}\right)^2 = 2 \cdot \frac{9}{4} = \frac{9}{2}$$

</details>

---

<details>
<summary><strong>Solution 12</strong></summary>

**Answer**: $\frac{1}{12}$

**Step 1 - Check direct substitution:**

Direct substitution: $\frac{2-2}{8-8} = \frac{0}{0}$ (indeterminate)

**Step 2 - Substitution:**

Let $u = \sqrt[3]{x}$, so $x = u^3$ and as $x \to 8$, $u \to 2$:

$$= \lim_{u \to 2} \frac{u - 2}{u^3 - 8}$$

**Step 3 - Factor using difference of cubes:**

$$u^3 - 8 = (u - 2)(u^2 + 2u + 4)$$

**Step 4 - Cancel:**

$$= \lim_{u \to 2} \frac{u - 2}{(u-2)(u^2 + 2u + 4)}$$

$$= \lim_{u \to 2} \frac{1}{u^2 + 2u + 4}$$

**Step 5 - Substitute:**

$$= \frac{1}{4 + 4 + 4} = \frac{1}{12}$$

</details>

---

<details>
<summary><strong>Solution 13</strong></summary>

**Answer**: 1

**Step 1 - Check direct substitution:**

Direct substitution: $\frac{0}{0}$ (indeterminate)

**Step 2 - Rationalize:**

Multiply by $\frac{\sqrt{1+x} + \sqrt{1-x}}{\sqrt{1+x} + \sqrt{1-x}}$:

$$= \lim_{x \to 0} \frac{(1+x) - (1-x)}{x(\sqrt{1+x} + \sqrt{1-x})}$$

**Step 3 - Simplify numerator:**

$$1 + x - 1 + x = 2x$$

$$= \lim_{x \to 0} \frac{2x}{x(\sqrt{1+x} + \sqrt{1-x})}$$

**Step 4 - Cancel x:**

$$= \lim_{x \to 0} \frac{2}{\sqrt{1+x} + \sqrt{1-x}}$$

**Step 5 - Substitute:**

$$= \frac{2}{1 + 1} = 1$$

</details>

---

<details>
<summary><strong>Solution 14</strong></summary>

**Answer**: $\frac{1}{3}$

**Rewrite using trig identity:**

$$x \cot(3x) = x \cdot \frac{\cos(3x)}{\sin(3x)} = \frac{x \cos(3x)}{\sin(3x)}$$

**Rearrange:**

$$= \lim_{x \to 0} \frac{x}{\sin(3x)} \cdot \cos(3x)$$

$$= \lim_{x \to 0} \frac{1}{\frac{\sin(3x)}{x}} \cdot \cos(3x)$$

$$= \lim_{x \to 0} \frac{1}{\frac{\sin(3x)}{3x} \cdot 3} \cdot \cos(3x)$$

**Evaluate:**

$$= \frac{1}{1 \cdot 3} \cdot 1 = \frac{1}{3}$$

</details>

---

<details>
<summary><strong>Solution 15</strong></summary>

**Answer**: Does not exist (or $+\infty$)

**Step 1 - Factor:**

- Numerator: $x^2 - 3x - 4 = (x-4)(x+1)$
- Denominator: $x^2 - 8x + 16 = (x-4)^2$

**Step 2 - Simplify:**

$$= \lim_{x \to 4} \frac{(x-4)(x+1)}{(x-4)^2} = \lim_{x \to 4} \frac{x+1}{x-4}$$

**Step 3 - Analyze:**

As $x \to 4$: numerator $\to 5$ and denominator $\to 0$.

**Step 4 - Check signs:**

- From right ($x > 4$): denominator is positive, so limit $= +\infty$
- From left ($x < 4$): denominator is negative, so limit $= -\infty$

**Conclusion:**

Since the one-sided limits don't agree, the limit **does not exist**.

(We can say the limit is $+\infty$ from the right and $-\infty$ from the left.)

</details>

<details>
<summary><strong>Solution 16</strong></summary>

**Answer**: (C) 3

**Step 1 - Check direct substitution:**

Direct substitution: $\frac{0}{0}$ (indeterminate)

**Step 2 - Factor:**

- Numerator: $x^3 - 8 = (x-2)(x^2 + 2x + 4)$
- Denominator: $x^2 - 4 = (x-2)(x+2)$

**Step 3 - Cancel:**

$$= \lim_{x \to 2} \frac{(x-2)(x^2 + 2x + 4)}{(x-2)(x+2)}$$

$$= \lim_{x \to 2} \frac{x^2 + 2x + 4}{x + 2}$$

**Step 4 - Substitute:**

$$= \frac{4 + 4 + 4}{4} = \frac{12}{4} = 3$$

</details>

---

<details>
<summary><strong>Solution 17</strong></summary>

**Answer**: (C) 6

**Rewrite using special limit:**

$$\lim_{x \to 0} \frac{\sin(kx)}{2x} = \lim_{x \to 0} \frac{\sin(kx)}{kx} \cdot \frac{k}{2}$$

$$= 1 \cdot \frac{k}{2} = \frac{k}{2}$$

**Solve for k:**

We're told this equals 3:

$$\frac{k}{2} = 3$$

$$k = 6$$

</details>

---

<details>
<summary><strong>Solution 18</strong></summary>

**(a) Answer**: $\frac{3}{4}$

**Factor:**

- Numerator: $x^2 - 2x - 8 = (x-4)(x+2)$
- Denominator: $x^2 - 16 = (x-4)(x+4)$

**Simplify:**

$$f(x) = \frac{(x-4)(x+2)}{(x-4)(x+4)} = \frac{x+2}{x+4} \text{ for } x \neq 4$$

**Evaluate:**

$$\lim_{x \to 4} f(x) = \frac{4+2}{4+4} = \frac{6}{8} = \frac{3}{4}$$

---

**(b) Answer**: Does not exist (vertical asymptote)

**Analyze:**

$$\lim_{x \to -4} f(x) = \lim_{x \to -4} \frac{x+2}{x+4}$$

As $x \to -4$: numerator $\to -2$ (non-zero), denominator $\to 0$

**Check signs:**

- From right: $\frac{-2}{0^+} = -\infty$
- From left: $\frac{-2}{0^-} = +\infty$

The limit does not exist.

---

**(c) Answer**: Hole at $x = 4$; vertical asymptote at $x = -4$

- At $x = 4$: The factor $(x-4)$ cancels, leaving a **hole** (removable discontinuity)
- At $x = -4$: The factor $(x+4)$ remains in the denominator, creating a **vertical asymptote**

</details>

---

<details>
<summary><strong>Solution 19</strong></summary>

**(a) Answer**: 12

**Expand:**

$$(2+h)^3 = 8 + 12h + 6h^2 + h^3$$

**Substitute:**

$$\lim_{h \to 0} \frac{(2+h)^3 - 8}{h} = \lim_{h \to 0} \frac{8 + 12h + 6h^2 + h^3 - 8}{h}$$

$$= \lim_{h \to 0} \frac{12h + 6h^2 + h^3}{h}$$

$$= \lim_{h \to 0} (12 + 6h + h^2) = 12$$

---

**(b) Answer**: $f(x) = x^3$

The limit has the form $\lim_{h \to 0} \frac{f(a+h) - f(a)}{h}$

Comparing $(2+h)^3 - 8 = (2+h)^3 - 2^3$, we see $f(x) = x^3$

---

**(c) Answer**: $a = 2$

The limit is $f'(2)$, the derivative of $f(x) = x^3$ at $x = 2$.

Indeed, $f'(x) = 3x^2$, so $f'(2) = 12$ ✓

</details>

---

<details>
<summary><strong>Solution 20</strong></summary>

**Answer**: $k = 1$; limit = 7

**Step 1 - Find k:**

For the limit to exist when direct substitution gives $\frac{0}{0}$, the numerator must have $(x-3)$ as a factor.

For $(x-3)$ to be a factor, $x = 3$ must be a root of $x^2 + kx - 12$:

$$3^2 + 3k - 12 = 0$$

$$9 + 3k - 12 = 0$$

$$3k = 3$$

$$k = 1$$

**Step 2 - Factor with k = 1:**

$$x^2 + x - 12 = (x + 4)(x - 3)$$

**Step 3 - Evaluate the limit:**

$$\lim_{x \to 3} \frac{(x+4)(x-3)}{x-3} = \lim_{x \to 3} (x + 4) = 7$$

</details>

---

## What's Next

Now that you have a complete toolkit for evaluating limits, we'll explore:

- [One-Sided Limits](/calculus/one-sided-limits) - Left and right limits in detail
- [Limits at Infinity](/calculus/limits-at-infinity) - What happens as $x \to \pm\infty$
- [Continuity](/calculus/continuity) - When functions have no breaks or jumps

These limit skills are essential - you'll use them constantly when we get to derivatives!

---

*"The art of evaluating limits is knowing which tool to reach for. Master these techniques, and limits become routine."*

*Last updated: December 2024*
