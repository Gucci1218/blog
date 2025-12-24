# Derivatives of Trigonometric Functions

Trigonometric functions appear everywhere in calculus — from modeling waves and oscillations to describing circular motion. Knowing how to differentiate $\sin$, $\cos$, $\tan$, and their inverses is essential for AP Calculus. The good news? Once you learn the patterns, these derivatives become second nature.

---

## What You'll Learn

- Derive the derivatives of $\sin(x)$ and $\cos(x)$ from first principles
- Memorize and apply derivatives of all six trig functions
- Differentiate inverse trig functions ($\arcsin$, $\arccos$, $\arctan$)
- Combine trig derivatives with chain rule, product rule, and quotient rule
- Solve AP Calculus problems involving trigonometric derivatives

---

## Prerequisites

- [Understanding Limits](/calculus/understanding-limits) — needed for the limit definition
- [Chain Rule](/calculus/chain-rule) — essential for $\sin(3x)$, $\cos(x^2)$, etc.
- [Product Rule](/calculus/product-rule) and [Quotient Rule](/calculus/quotient-rule)
- Basic trig identities: $\sin^2(x) + \cos^2(x) = 1$, $\tan(x) = \frac{\sin(x)}{\cos(x)}$

---

## The Core Concept

### Two Fundamental Limits

Before diving into derivatives, we need two special limits that make everything work:

$$\boxed{\lim_{x \to 0} \frac{\sin(x)}{x} = 1}$$

$$\boxed{\lim_{x \to 0} \frac{1 - \cos(x)}{x} = 0}$$

These limits (where $x$ is in **radians**) are the foundation of all trig derivatives.

### Why Radians Matter

These limits **only work in radians**. If you use degrees, the derivatives change by a factor of $\frac{\pi}{180}$. This is why calculus always uses radians!

---

## Deriving $\frac{d}{dx}[\sin(x)]$

Using the limit definition of the derivative:

$$\frac{d}{dx}[\sin(x)] = \lim_{h \to 0} \frac{\sin(x + h) - \sin(x)}{h}$$

**Apply the angle addition formula:** $\sin(x + h) = \sin(x)\cos(h) + \cos(x)\sin(h)$

$$= \lim_{h \to 0} \frac{\sin(x)\cos(h) + \cos(x)\sin(h) - \sin(x)}{h}$$

**Rearrange:**

$$= \lim_{h \to 0} \frac{\sin(x)[\cos(h) - 1] + \cos(x)\sin(h)}{h}$$

$$= \lim_{h \to 0} \sin(x) \cdot \frac{\cos(h) - 1}{h} + \lim_{h \to 0} \cos(x) \cdot \frac{\sin(h)}{h}$$

**Apply our fundamental limits:**

$$= \sin(x) \cdot 0 + \cos(x) \cdot 1 = \cos(x)$$

$$\boxed{\frac{d}{dx}[\sin(x)] = \cos(x)}$$

---

## Deriving $\frac{d}{dx}[\cos(x)]$

Similarly, using the limit definition and $\cos(x + h) = \cos(x)\cos(h) - \sin(x)\sin(h)$:

$$\frac{d}{dx}[\cos(x)] = \lim_{h \to 0} \frac{\cos(x)\cos(h) - \sin(x)\sin(h) - \cos(x)}{h}$$

$$= \lim_{h \to 0} \cos(x) \cdot \frac{\cos(h) - 1}{h} - \lim_{h \to 0} \sin(x) \cdot \frac{\sin(h)}{h}$$

$$= \cos(x) \cdot 0 - \sin(x) \cdot 1 = -\sin(x)$$

$$\boxed{\frac{d}{dx}[\cos(x)] = -\sin(x)}$$

**Note the negative sign!** This is where many students make errors.

---

## The Six Trig Derivatives

### Basic Trig Functions

| Function | Derivative |
|----------|------------|
| $\sin(x)$ | $\cos(x)$ |
| $\cos(x)$ | $-\sin(x)$ |
| $\tan(x)$ | $\sec^2(x)$ |
| $\cot(x)$ | $-\csc^2(x)$ |
| $\sec(x)$ | $\sec(x)\tan(x)$ |
| $\csc(x)$ | $-\csc(x)\cot(x)$ |

### Memory Tricks

1. **"Co" functions have negatives:** $\cos$, $\cot$, $\csc$ all have negative derivatives
2. **Sine and cosine cycle:** $\sin \to \cos \to -\sin \to -\cos \to \sin$
3. **Tan and sec are partners:** Both involve $\sec$
4. **Cot and csc are partners:** Both involve $\csc$

---

## Deriving the Other Four

### Derivative of $\tan(x)$

Using $\tan(x) = \frac{\sin(x)}{\cos(x)}$ and the quotient rule:

$$\frac{d}{dx}[\tan(x)] = \frac{\cos(x) \cdot \cos(x) - \sin(x) \cdot (-\sin(x))}{\cos^2(x)}$$

$$= \frac{\cos^2(x) + \sin^2(x)}{\cos^2(x)} = \frac{1}{\cos^2(x)} = \sec^2(x)$$

$$\boxed{\frac{d}{dx}[\tan(x)] = \sec^2(x)}$$

---

### Derivative of $\cot(x)$

Using $\cot(x) = \frac{\cos(x)}{\sin(x)}$:

$$\frac{d}{dx}[\cot(x)] = \frac{-\sin(x) \cdot \sin(x) - \cos(x) \cdot \cos(x)}{\sin^2(x)}$$

$$= \frac{-\sin^2(x) - \cos^2(x)}{\sin^2(x)} = \frac{-1}{\sin^2(x)} = -\csc^2(x)$$

$$\boxed{\frac{d}{dx}[\cot(x)] = -\csc^2(x)}$$

---

### Derivative of $\sec(x)$

Using $\sec(x) = \frac{1}{\cos(x)}$:

$$\frac{d}{dx}[\sec(x)] = \frac{0 \cdot \cos(x) - 1 \cdot (-\sin(x))}{\cos^2(x)} = \frac{\sin(x)}{\cos^2(x)}$$

$$= \frac{1}{\cos(x)} \cdot \frac{\sin(x)}{\cos(x)} = \sec(x)\tan(x)$$

$$\boxed{\frac{d}{dx}[\sec(x)] = \sec(x)\tan(x)}$$

---

### Derivative of $\csc(x)$

Using $\csc(x) = \frac{1}{\sin(x)}$:

$$\frac{d}{dx}[\csc(x)] = \frac{0 \cdot \sin(x) - 1 \cdot \cos(x)}{\sin^2(x)} = \frac{-\cos(x)}{\sin^2(x)}$$

$$= -\frac{1}{\sin(x)} \cdot \frac{\cos(x)}{\sin(x)} = -\csc(x)\cot(x)$$

$$\boxed{\frac{d}{dx}[\csc(x)] = -\csc(x)\cot(x)}$$

---

## Worked Examples: Basic Trig Derivatives

### Example 1: Simple Sine

**Differentiate $f(x) = 3\sin(x)$**

**Solution:**

$$f'(x) = 3\cos(x)$$

**Answer:** $f'(x) = 3\cos(x)$

---

### Example 2: Cosine with Constant

**Differentiate $g(x) = -2\cos(x) + 5$**

**Solution:**

$$g'(x) = -2(-\sin(x)) + 0 = 2\sin(x)$$

**Answer:** $g'(x) = 2\sin(x)$

---

### Example 3: Tangent

**Differentiate $h(x) = \tan(x) + x$**

**Solution:**

$$h'(x) = \sec^2(x) + 1$$

**Answer:** $h'(x) = \sec^2(x) + 1$

---

## Trig Derivatives with Chain Rule

When the argument of a trig function is more than just $x$, apply the chain rule!

### General Formulas

$$\frac{d}{dx}[\sin(u)] = \cos(u) \cdot \frac{du}{dx}$$

$$\frac{d}{dx}[\cos(u)] = -\sin(u) \cdot \frac{du}{dx}$$

$$\frac{d}{dx}[\tan(u)] = \sec^2(u) \cdot \frac{du}{dx}$$

---

### Example 4: Sine with Linear Argument

**Differentiate $f(x) = \sin(3x)$**

**Solution:**

- Outer: $\sin(u)$, derivative: $\cos(u)$
- Inner: $u = 3x$, derivative: $3$

$$f'(x) = \cos(3x) \cdot 3 = 3\cos(3x)$$

**Answer:** $f'(x) = 3\cos(3x)$

---

### Example 5: Cosine with Quadratic Argument

**Differentiate $g(x) = \cos(x^2)$**

**Solution:**

$$g'(x) = -\sin(x^2) \cdot 2x = -2x\sin(x^2)$$

**Answer:** $g'(x) = -2x\sin(x^2)$

---

### Example 6: Tangent with Complex Argument

**Differentiate $h(x) = \tan(5x - 1)$**

**Solution:**

$$h'(x) = \sec^2(5x - 1) \cdot 5 = 5\sec^2(5x - 1)$$

**Answer:** $h'(x) = 5\sec^2(5x - 1)$

---

### Example 7: Secant with Chain Rule

**Differentiate $f(x) = \sec(2x)$**

**Solution:**

$$f'(x) = \sec(2x)\tan(2x) \cdot 2 = 2\sec(2x)\tan(2x)$$

**Answer:** $f'(x) = 2\sec(2x)\tan(2x)$

---

### Example 8: Nested Trig Functions

**Differentiate $f(x) = \sin(\cos(x))$**

**Solution:**

- Outer: $\sin(u)$
- Inner: $u = \cos(x)$

$$f'(x) = \cos(\cos(x)) \cdot (-\sin(x)) = -\sin(x)\cos(\cos(x))$$

**Answer:** $f'(x) = -\sin(x)\cos(\cos(x))$

---

## Powers of Trig Functions

### Example 9: Sine Squared

**Differentiate $f(x) = \sin^2(x)$**

Note: $\sin^2(x) = [\sin(x)]^2$

**Solution:**

$$f'(x) = 2\sin(x) \cdot \cos(x) = 2\sin(x)\cos(x)$$

Using the double angle identity: $2\sin(x)\cos(x) = \sin(2x)$

**Answer:** $f'(x) = 2\sin(x)\cos(x) = \sin(2x)$

---

### Example 10: Cosine Cubed

**Differentiate $g(x) = \cos^3(x)$**

**Solution:**

$$g'(x) = 3\cos^2(x) \cdot (-\sin(x)) = -3\cos^2(x)\sin(x)$$

**Answer:** $g'(x) = -3\cos^2(x)\sin(x)$

---

### Example 11: Tangent to the Fourth

**Differentiate $h(x) = \tan^4(x)$**

**Solution:**

$$h'(x) = 4\tan^3(x) \cdot \sec^2(x) = 4\tan^3(x)\sec^2(x)$$

**Answer:** $h'(x) = 4\tan^3(x)\sec^2(x)$

---

## Combining with Product and Quotient Rules

### Example 12: Product of $x$ and Sine

**Differentiate $f(x) = x\sin(x)$**

**Solution (Product Rule):**

$$f'(x) = 1 \cdot \sin(x) + x \cdot \cos(x) = \sin(x) + x\cos(x)$$

**Answer:** $f'(x) = \sin(x) + x\cos(x)$

---

### Example 13: Product of Sine and Cosine

**Differentiate $g(x) = \sin(x)\cos(x)$**

**Solution:**

$$g'(x) = \cos(x) \cdot \cos(x) + \sin(x) \cdot (-\sin(x))$$

$$= \cos^2(x) - \sin^2(x) = \cos(2x)$$

**Answer:** $g'(x) = \cos^2(x) - \sin^2(x) = \cos(2x)$

---

### Example 14: Quotient with Trig

**Differentiate $h(x) = \frac{\sin(x)}{x}$**

**Solution (Quotient Rule):**

$$h'(x) = \frac{x\cos(x) - \sin(x) \cdot 1}{x^2} = \frac{x\cos(x) - \sin(x)}{x^2}$$

**Answer:** $h'(x) = \frac{x\cos(x) - \sin(x)}{x^2}$

---

### Example 15: Exponential Times Trig

**Differentiate $f(x) = e^x\sin(x)$**

**Solution:**

$$f'(x) = e^x\sin(x) + e^x\cos(x) = e^x(\sin(x) + \cos(x))$$

**Answer:** $f'(x) = e^x(\sin(x) + \cos(x))$

---

## Inverse Trig Derivatives

### The Three Main Inverse Trig Derivatives

$$\boxed{\frac{d}{dx}[\arcsin(x)] = \frac{1}{\sqrt{1 - x^2}}}$$

$$\boxed{\frac{d}{dx}[\arccos(x)] = -\frac{1}{\sqrt{1 - x^2}}}$$

$$\boxed{\frac{d}{dx}[\arctan(x)] = \frac{1}{1 + x^2}}$$

### Complete Table

| Function | Derivative | Domain |
|----------|------------|--------|
| $\arcsin(x)$ | $\frac{1}{\sqrt{1-x^2}}$ | $-1 < x < 1$ |
| $\arccos(x)$ | $-\frac{1}{\sqrt{1-x^2}}$ | $-1 < x < 1$ |
| $\arctan(x)$ | $\frac{1}{1+x^2}$ | All real $x$ |
| $\text{arccot}(x)$ | $-\frac{1}{1+x^2}$ | All real $x$ |
| $\text{arcsec}(x)$ | $\frac{1}{|x|\sqrt{x^2-1}}$ | $|x| > 1$ |
| $\text{arccsc}(x)$ | $-\frac{1}{|x|\sqrt{x^2-1}}$ | $|x| > 1$ |

### Memory Tips

1. **Arcsin and arccos are opposites** (differ by a negative)
2. **Arctan has the simplest form:** $\frac{1}{1+x^2}$ — no square root!
3. **"Co" functions have negatives** (same pattern as regular trig)

---

## Deriving $\frac{d}{dx}[\arcsin(x)]$

Let $y = \arcsin(x)$, so $\sin(y) = x$.

**Differentiate implicitly:**

$$\cos(y) \cdot \frac{dy}{dx} = 1$$

$$\frac{dy}{dx} = \frac{1}{\cos(y)}$$

Since $\sin(y) = x$, we have $\cos(y) = \sqrt{1 - \sin^2(y)} = \sqrt{1 - x^2}$

$$\frac{d}{dx}[\arcsin(x)] = \frac{1}{\sqrt{1 - x^2}}$$

---

## Deriving $\frac{d}{dx}[\arctan(x)]$

Let $y = \arctan(x)$, so $\tan(y) = x$.

**Differentiate implicitly:**

$$\sec^2(y) \cdot \frac{dy}{dx} = 1$$

$$\frac{dy}{dx} = \frac{1}{\sec^2(y)} = \cos^2(y)$$

Since $\tan(y) = x$, using the identity $\sec^2(y) = 1 + \tan^2(y)$:

$$\frac{dy}{dx} = \frac{1}{1 + \tan^2(y)} = \frac{1}{1 + x^2}$$

---

## Worked Examples: Inverse Trig

### Example 16: Arcsin with Chain Rule

**Differentiate $f(x) = \arcsin(2x)$**

**Solution:**

$$f'(x) = \frac{1}{\sqrt{1 - (2x)^2}} \cdot 2 = \frac{2}{\sqrt{1 - 4x^2}}$$

**Answer:** $f'(x) = \frac{2}{\sqrt{1 - 4x^2}}$

---

### Example 17: Arctan with Chain Rule

**Differentiate $g(x) = \arctan(x^2)$**

**Solution:**

$$g'(x) = \frac{1}{1 + (x^2)^2} \cdot 2x = \frac{2x}{1 + x^4}$$

**Answer:** $g'(x) = \frac{2x}{1 + x^4}$

---

### Example 18: Arccos

**Differentiate $h(x) = \arccos(3x)$**

**Solution:**

$$h'(x) = -\frac{1}{\sqrt{1 - 9x^2}} \cdot 3 = -\frac{3}{\sqrt{1 - 9x^2}}$$

**Answer:** $h'(x) = -\frac{3}{\sqrt{1 - 9x^2}}$

---

### Example 19: Product with Arctan

**Differentiate $f(x) = x \cdot \arctan(x)$**

**Solution:**

$$f'(x) = 1 \cdot \arctan(x) + x \cdot \frac{1}{1 + x^2}$$

$$= \arctan(x) + \frac{x}{1 + x^2}$$

**Answer:** $f'(x) = \arctan(x) + \frac{x}{1 + x^2}$

---

### Example 20: Finding Tangent Lines

**Find the slope of the tangent to $y = \arctan(x)$ at $x = 1$.**

**Solution:**

$$\frac{dy}{dx} = \frac{1}{1 + x^2}$$

At $x = 1$:

$$m = \frac{1}{1 + 1} = \frac{1}{2}$$

**Answer:** Slope $= \frac{1}{2}$

---

## Key Formulas & Rules

### Basic Trig Derivatives

$$\frac{d}{dx}[\sin(x)] = \cos(x) \qquad \frac{d}{dx}[\cos(x)] = -\sin(x)$$

$$\frac{d}{dx}[\tan(x)] = \sec^2(x) \qquad \frac{d}{dx}[\cot(x)] = -\csc^2(x)$$

$$\frac{d}{dx}[\sec(x)] = \sec(x)\tan(x) \qquad \frac{d}{dx}[\csc(x)] = -\csc(x)\cot(x)$$

### With Chain Rule

$$\frac{d}{dx}[\sin(u)] = \cos(u) \cdot u' \qquad \frac{d}{dx}[\cos(u)] = -\sin(u) \cdot u'$$

### Inverse Trig Derivatives

$$\frac{d}{dx}[\arcsin(x)] = \frac{1}{\sqrt{1-x^2}} \qquad \frac{d}{dx}[\arccos(x)] = -\frac{1}{\sqrt{1-x^2}}$$

$$\frac{d}{dx}[\arctan(x)] = \frac{1}{1+x^2}$$

---

## Common Mistakes to Avoid

### Mistake 1: Forgetting the Negative for Cosine

**Wrong:**

$$\frac{d}{dx}[\cos(x)] = \sin(x) \quad \text{✗}$$

**Right:**

$$\frac{d}{dx}[\cos(x)] = -\sin(x) \quad \text{✓}$$

---

### Mistake 2: Forgetting Chain Rule

**Wrong:**

$$\frac{d}{dx}[\sin(2x)] = \cos(2x) \quad \text{✗}$$

**Right:**

$$\frac{d}{dx}[\sin(2x)] = 2\cos(2x) \quad \text{✓}$$

---

### Mistake 3: Confusing $\sin^2(x)$ with $\sin(x^2)$

| Expression | Meaning | Derivative |
|------------|---------|------------|
| $\sin^2(x)$ | $[\sin(x)]^2$ | $2\sin(x)\cos(x)$ |
| $\sin(x^2)$ | sine of $x^2$ | $2x\cos(x^2)$ |

---

### Mistake 4: Wrong Derivative for Inverse Trig

**Arcsin vs Arctan:**

- $\frac{d}{dx}[\arcsin(x)] = \frac{1}{\sqrt{1-x^2}}$ (square root in denominator)
- $\frac{d}{dx}[\arctan(x)] = \frac{1}{1+x^2}$ (no square root!)

---

### Mistake 5: Using Degrees

All trig derivatives assume **radians**. If you see degrees in a problem, convert first!

---

## AP Exam Tips

### What to Memorize

**Must know perfectly:**
- Derivatives of $\sin$, $\cos$, $\tan$
- Derivatives of $\arcsin$, $\arctan$

**Good to know:**
- Derivatives of $\sec$, $\csc$, $\cot$
- Derivative of $\arccos$

### Common Question Types

1. **Basic derivatives:** $\frac{d}{dx}[\sin(3x)]$
2. **Chain rule combinations:** $\frac{d}{dx}[\tan(x^2 + 1)]$
3. **Product/quotient with trig:** $\frac{d}{dx}[x^2\cos(x)]$
4. **Inverse trig:** $\frac{d}{dx}[\arctan(2x)]$
5. **Tangent line problems:** Find tangent to $y = \sin(x)$ at $x = \frac{\pi}{4}$

### Speed Tips

1. **Know the patterns cold** — these come up constantly
2. **Watch for double angles:** $2\sin(x)\cos(x) = \sin(2x)$
3. **Simplify using identities** when possible
4. **Don't forget the chain rule** — it's needed more often than not

---

## Practice Problems

### Basic (Problems 1-5)

**1.** Differentiate:

$$f(x) = 4\sin(x) - 3\cos(x)$$

---

**2.** Differentiate:

$$g(x) = \tan(x) + \sec(x)$$

---

**3.** Differentiate:

$$h(x) = \sin(5x)$$

---

**4.** Differentiate:

$$f(x) = \cos(x^2)$$

---

**5.** Differentiate:

$$g(x) = \sin^2(x)$$

---

### Intermediate (Problems 6-10)

**6.** Differentiate:

$$f(x) = x^2\sin(x)$$

---

**7.** Differentiate:

$$g(x) = \frac{\cos(x)}{x}$$

---

**8.** Differentiate:

$$h(x) = \tan^3(2x)$$

---

**9.** Differentiate:

$$f(x) = e^x\cos(3x)$$

---

**10.** Differentiate:

$$g(x) = \sin(x)\cos(2x)$$

---

### Advanced (Problems 11-15)

**11.** Differentiate:

$$f(x) = \arcsin(4x)$$

---

**12.** Differentiate:

$$g(x) = \arctan(\sqrt{x})$$

---

**13.** Find the equation of the tangent line to $y = \tan(x)$ at $x = \frac{\pi}{4}$.

---

**14.** Differentiate:

$$h(x) = x\arctan(x) - \frac{1}{2}\ln(1 + x^2)$$

---

**15.** Find $\frac{d^2y}{dx^2}$ for $y = \sin(2x)$.

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

What is $\frac{d}{dx}[\sin(x)\cos(x)]$?

| Choice | Answer |
|--------|--------|
| **(A)** | $\cos^2(x) - \sin^2(x)$ |
| **(B)** | $\cos^2(x) + \sin^2(x)$ |
| **(C)** | $-\cos^2(x) + \sin^2(x)$ |
| **(D)** | $2\sin(x)\cos(x)$ |

---

#### Problem 17 (Multiple Choice)

If $f(x) = \tan(3x)$, then $f'\left(\frac{\pi}{12}\right) =$

| Choice | Answer |
|--------|--------|
| **(A)** | $3$ |
| **(B)** | $6$ |
| **(C)** | $\frac{3}{2}$ |
| **(D)** | $4$ |

---

#### Problem 18 (Free Response)

Let $f(x) = \sin^2(x) + \cos^2(x)$.

> **(a)** Find $f'(x)$.
>
> **(b)** Explain why this result makes sense geometrically.
>
> **(c)** Use this result to find $\frac{d}{dx}[\sin^2(x)]$ without the product rule.

---

#### Problem 19 (Multiple Choice)

$\frac{d}{dx}[\arctan(e^x)] =$

| Choice | Answer |
|--------|--------|
| **(A)** | $\frac{e^x}{1 + e^x}$ |
| **(B)** | $\frac{e^x}{1 + e^{2x}}$ |
| **(C)** | $\frac{1}{1 + e^{2x}}$ |
| **(D)** | $\frac{e^x}{(1 + e^x)^2}$ |

---

#### Problem 20 (Free Response - Challenging)

The position of a particle moving along the x-axis is given by $x(t) = 3\sin(2t) + 4\cos(2t)$ for $t \geq 0$.

> **(a)** Find the velocity $v(t)$ and acceleration $a(t)$.
>
> **(b)** Find all times $t$ in $[0, \pi]$ when the particle is at rest.
>
> **(c)** Show that $a(t) = -4x(t)$. What does this tell you about the motion?

---

## Solutions

<details>
<summary><strong>Solution 1</strong></summary>

**Problem:** $f(x) = 4\sin(x) - 3\cos(x)$

$$f'(x) = 4\cos(x) - 3(-\sin(x)) = 4\cos(x) + 3\sin(x)$$

**Answer:** $f'(x) = 4\cos(x) + 3\sin(x)$

</details>

---

<details>
<summary><strong>Solution 2</strong></summary>

**Problem:** $g(x) = \tan(x) + \sec(x)$

$$g'(x) = \sec^2(x) + \sec(x)\tan(x)$$

**Answer:** $g'(x) = \sec^2(x) + \sec(x)\tan(x)$

</details>

---

<details>
<summary><strong>Solution 3</strong></summary>

**Problem:** $h(x) = \sin(5x)$

$$h'(x) = \cos(5x) \cdot 5 = 5\cos(5x)$$

**Answer:** $h'(x) = 5\cos(5x)$

</details>

---

<details>
<summary><strong>Solution 4</strong></summary>

**Problem:** $f(x) = \cos(x^2)$

$$f'(x) = -\sin(x^2) \cdot 2x = -2x\sin(x^2)$$

**Answer:** $f'(x) = -2x\sin(x^2)$

</details>

---

<details>
<summary><strong>Solution 5</strong></summary>

**Problem:** $g(x) = \sin^2(x) = [\sin(x)]^2$

$$g'(x) = 2\sin(x) \cdot \cos(x) = 2\sin(x)\cos(x)$$

Or equivalently: $g'(x) = \sin(2x)$

**Answer:** $g'(x) = 2\sin(x)\cos(x) = \sin(2x)$

</details>

---

<details>
<summary><strong>Solution 6</strong></summary>

**Problem:** $f(x) = x^2\sin(x)$

**Product rule:**

$$f'(x) = 2x \cdot \sin(x) + x^2 \cdot \cos(x) = 2x\sin(x) + x^2\cos(x)$$

**Answer:** $f'(x) = 2x\sin(x) + x^2\cos(x)$

</details>

---

<details>
<summary><strong>Solution 7</strong></summary>

**Problem:** $g(x) = \frac{\cos(x)}{x}$

**Quotient rule:**

$$g'(x) = \frac{-\sin(x) \cdot x - \cos(x) \cdot 1}{x^2} = \frac{-x\sin(x) - \cos(x)}{x^2}$$

**Answer:** $g'(x) = \frac{-x\sin(x) - \cos(x)}{x^2}$

</details>

---

<details>
<summary><strong>Solution 8</strong></summary>

**Problem:** $h(x) = \tan^3(2x) = [\tan(2x)]^3$

**Chain rule (two layers):**

$$h'(x) = 3[\tan(2x)]^2 \cdot \sec^2(2x) \cdot 2$$

$$= 6\tan^2(2x)\sec^2(2x)$$

**Answer:** $h'(x) = 6\tan^2(2x)\sec^2(2x)$

</details>

---

<details>
<summary><strong>Solution 9</strong></summary>

**Problem:** $f(x) = e^x\cos(3x)$

**Product rule:**

$$f'(x) = e^x \cdot \cos(3x) + e^x \cdot (-\sin(3x)) \cdot 3$$

$$= e^x\cos(3x) - 3e^x\sin(3x)$$

$$= e^x[\cos(3x) - 3\sin(3x)]$$

**Answer:** $f'(x) = e^x[\cos(3x) - 3\sin(3x)]$

</details>

---

<details>
<summary><strong>Solution 10</strong></summary>

**Problem:** $g(x) = \sin(x)\cos(2x)$

**Product rule:**

$$g'(x) = \cos(x) \cdot \cos(2x) + \sin(x) \cdot (-\sin(2x)) \cdot 2$$

$$= \cos(x)\cos(2x) - 2\sin(x)\sin(2x)$$

**Answer:** $g'(x) = \cos(x)\cos(2x) - 2\sin(x)\sin(2x)$

</details>

---

<details>
<summary><strong>Solution 11</strong></summary>

**Problem:** $f(x) = \arcsin(4x)$

$$f'(x) = \frac{1}{\sqrt{1 - (4x)^2}} \cdot 4 = \frac{4}{\sqrt{1 - 16x^2}}$$

**Answer:** $f'(x) = \frac{4}{\sqrt{1 - 16x^2}}$

</details>

---

<details>
<summary><strong>Solution 12</strong></summary>

**Problem:** $g(x) = \arctan(\sqrt{x})$

$$g'(x) = \frac{1}{1 + (\sqrt{x})^2} \cdot \frac{1}{2\sqrt{x}}$$

$$= \frac{1}{1 + x} \cdot \frac{1}{2\sqrt{x}} = \frac{1}{2\sqrt{x}(1 + x)}$$

**Answer:** $g'(x) = \frac{1}{2\sqrt{x}(1 + x)}$

</details>

---

<details>
<summary><strong>Solution 13</strong></summary>

**Problem:** Tangent to $y = \tan(x)$ at $x = \frac{\pi}{4}$

**Point:** At $x = \frac{\pi}{4}$, $y = \tan(\frac{\pi}{4}) = 1$

**Slope:** $\frac{dy}{dx} = \sec^2(x)$

At $x = \frac{\pi}{4}$: $m = \sec^2(\frac{\pi}{4}) = (\sqrt{2})^2 = 2$

**Tangent line:**

$$y - 1 = 2\left(x - \frac{\pi}{4}\right)$$

$$y = 2x - \frac{\pi}{2} + 1$$

**Answer:** $y = 2x - \frac{\pi}{2} + 1$

</details>

---

<details>
<summary><strong>Solution 14</strong></summary>

**Problem:** $h(x) = x\arctan(x) - \frac{1}{2}\ln(1 + x^2)$

**First term (product rule):**

$$\frac{d}{dx}[x\arctan(x)] = \arctan(x) + x \cdot \frac{1}{1 + x^2}$$

$$= \arctan(x) + \frac{x}{1 + x^2}$$

**Second term:**

$$\frac{d}{dx}\left[-\frac{1}{2}\ln(1 + x^2)\right] = -\frac{1}{2} \cdot \frac{2x}{1 + x^2} = -\frac{x}{1 + x^2}$$

**Combine:**

$$h'(x) = \arctan(x) + \frac{x}{1 + x^2} - \frac{x}{1 + x^2} = \arctan(x)$$

**Answer:** $h'(x) = \arctan(x)$

</details>

---

<details>
<summary><strong>Solution 15</strong></summary>

**Problem:** Find $\frac{d^2y}{dx^2}$ for $y = \sin(2x)$

**First derivative:**

$$\frac{dy}{dx} = 2\cos(2x)$$

**Second derivative:**

$$\frac{d^2y}{dx^2} = 2 \cdot (-\sin(2x)) \cdot 2 = -4\sin(2x)$$

**Answer:** $\frac{d^2y}{dx^2} = -4\sin(2x)$

</details>

---

<details>
<summary><strong>Solution 16</strong></summary>

**Problem:** $\frac{d}{dx}[\sin(x)\cos(x)]$

**Product rule:**

$$= \cos(x) \cdot \cos(x) + \sin(x) \cdot (-\sin(x))$$

$$= \cos^2(x) - \sin^2(x)$$

**Answer:** **(A)** $\cos^2(x) - \sin^2(x)$

*Note: This also equals $\cos(2x)$*

</details>

---

<details>
<summary><strong>Solution 17</strong></summary>

**Problem:** $f(x) = \tan(3x)$, find $f'\left(\frac{\pi}{12}\right)$

$$f'(x) = 3\sec^2(3x)$$

At $x = \frac{\pi}{12}$:

$$f'\left(\frac{\pi}{12}\right) = 3\sec^2\left(\frac{\pi}{4}\right) = 3 \cdot (\sqrt{2})^2 = 3 \cdot 2 = 6$$

**Answer:** **(B)** $6$

</details>

---

<details>
<summary><strong>Solution 18</strong></summary>

**Problem:** $f(x) = \sin^2(x) + \cos^2(x)$

**(a) Find $f'(x)$:**

$$f'(x) = 2\sin(x)\cos(x) + 2\cos(x)(-\sin(x))$$

$$= 2\sin(x)\cos(x) - 2\sin(x)\cos(x) = 0$$

**Answer (a):** $f'(x) = 0$

**(b) Geometric explanation:**

Since $\sin^2(x) + \cos^2(x) = 1$ (the Pythagorean identity), we have $f(x) = 1$ for all $x$.

The derivative of a constant is zero, which matches our answer.

**Answer (b):** $f(x) = 1$ is constant, so its derivative is zero.

**(c) Find $\frac{d}{dx}[\sin^2(x)]$:**

From $\sin^2(x) + \cos^2(x) = 1$:

$$\frac{d}{dx}[\sin^2(x)] + \frac{d}{dx}[\cos^2(x)] = 0$$

Let $u = \frac{d}{dx}[\sin^2(x)]$. Then:

$$\frac{d}{dx}[\cos^2(x)] = 2\cos(x)(-\sin(x)) = -2\sin(x)\cos(x)$$

So: $u + (-2\sin(x)\cos(x)) = 0$

$$u = 2\sin(x)\cos(x)$$

**Answer (c):** $\frac{d}{dx}[\sin^2(x)] = 2\sin(x)\cos(x)$

</details>

---

<details>
<summary><strong>Solution 19</strong></summary>

**Problem:** $\frac{d}{dx}[\arctan(e^x)]$

$$= \frac{1}{1 + (e^x)^2} \cdot e^x = \frac{e^x}{1 + e^{2x}}$$

**Answer:** **(B)** $\frac{e^x}{1 + e^{2x}}$

</details>

---

<details>
<summary><strong>Solution 20</strong></summary>

**Problem:** $x(t) = 3\sin(2t) + 4\cos(2t)$

**(a) Velocity and acceleration:**

$$v(t) = x'(t) = 6\cos(2t) - 8\sin(2t)$$

$$a(t) = v'(t) = -12\sin(2t) - 16\cos(2t)$$

**Answer (a):** $v(t) = 6\cos(2t) - 8\sin(2t)$, $a(t) = -12\sin(2t) - 16\cos(2t)$

**(b) When is particle at rest?**

Set $v(t) = 0$:

$$6\cos(2t) - 8\sin(2t) = 0$$

$$6\cos(2t) = 8\sin(2t)$$

$$\tan(2t) = \frac{6}{8} = \frac{3}{4}$$

$$2t = \arctan\left(\frac{3}{4}\right) + n\pi$$

$$t = \frac{1}{2}\arctan\left(\frac{3}{4}\right) + \frac{n\pi}{2}$$

For $t \in [0, \pi]$:

- $t_1 = \frac{1}{2}\arctan\left(\frac{3}{4}\right) \approx 0.322$
- $t_2 = \frac{1}{2}\arctan\left(\frac{3}{4}\right) + \frac{\pi}{2} \approx 1.893$
- $t_3 = \frac{1}{2}\arctan\left(\frac{3}{4}\right) + \pi \approx 3.464$ (outside range)

**Answer (b):** $t = \frac{1}{2}\arctan\left(\frac{3}{4}\right)$ and $t = \frac{1}{2}\arctan\left(\frac{3}{4}\right) + \frac{\pi}{2}$

**(c) Show $a(t) = -4x(t)$:**

$$a(t) = -12\sin(2t) - 16\cos(2t)$$

$$-4x(t) = -4[3\sin(2t) + 4\cos(2t)] = -12\sin(2t) - 16\cos(2t)$$

Yes, $a(t) = -4x(t)$ ✓

**Interpretation:** This is **simple harmonic motion**. The acceleration is proportional to displacement and always directed toward equilibrium (the origin). The particle oscillates back and forth like a spring or pendulum.

**Answer (c):** The relation $a = -4x$ indicates simple harmonic motion with angular frequency $\omega = 2$.

</details>

---

## What's Next

Now that you've mastered trig derivatives, you're ready for [Derivatives of Exponential Functions](/calculus/derivatives-exp), where you'll learn why $e^x$ is its own derivative and how to differentiate $a^x$ for any base $a$.

---

<div align="center">

[← Implicit Differentiation](/calculus/implicit-differentiation) | [Exponential Derivatives →](/calculus/derivatives-exp)

</div>
