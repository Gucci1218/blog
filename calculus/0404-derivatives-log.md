# Derivatives of Logarithmic Functions
<p class="article-date">March 22, 2025</p>

Logarithms are the inverse of exponentials, so it's no surprise their derivatives are closely related. The derivative of $\ln(x)$ is beautifully simple: $\frac{1}{x}$. Even better, **logarithmic differentiation** gives us a powerful technique for differentiating complex products, quotients, and functions like $x^x$ that don't fit our usual rules.

---

## What You'll Learn

- Derive and apply $\frac{d}{dx}[\ln(x)] = \frac{1}{x}$
- Differentiate $\ln(u)$ using the chain rule
- Apply the derivative of $\log_a(x)$ for any base
- Master logarithmic differentiation for complex functions
- Differentiate functions of the form $f(x)^{g(x)}$
- Solve AP Calculus problems involving logarithms

---

## Prerequisites

- [Exponential Derivatives](/calculus/0403-derivatives-exp) — logarithms are inverses of exponentials
- [Chain Rule](/calculus/0307-chain-rule) — essential for $\ln(g(x))$
- [Implicit Differentiation](/calculus/0401-implicit-differentiation) — used to derive log rules
- Properties of logarithms: $\ln(ab) = \ln(a) + \ln(b)$, $\ln(a^n) = n\ln(a)$

---

## The Core Concept

### Deriving $\frac{d}{dx}[\ln(x)]$

Let $y = \ln(x)$. Then $e^y = x$.

**Differentiate both sides implicitly:**

$$e^y \cdot \frac{dy}{dx} = 1$$

$$\frac{dy}{dx} = \frac{1}{e^y}$$

Since $e^y = x$:

$$\frac{dy}{dx} = \frac{1}{x}$$

$$\boxed{\frac{d}{dx}[\ln(x)] = \frac{1}{x}, \quad x > 0}$$

### Why This Is Beautiful

- $e^x$ is its own derivative
- $\ln(x)$ has the simplest possible derivative: $\frac{1}{x}$

These two functions are perfect inverses in every way!

---

## The Logarithm Derivative Rules

### Rule 1: Natural Logarithm

$$\boxed{\frac{d}{dx}[\ln(x)] = \frac{1}{x}}$$

### Rule 2: Natural Logarithm with Chain Rule

$$\boxed{\frac{d}{dx}[\ln(u)] = \frac{1}{u} \cdot \frac{du}{dx} = \frac{u'}{u}}$$

This form $\frac{u'}{u}$ is incredibly useful — the derivative of $\ln(\text{something})$ is $\frac{\text{derivative of something}}{\text{something}}$.

### Rule 3: General Logarithm (Any Base)

$$\boxed{\frac{d}{dx}[\log_a(x)] = \frac{1}{x \ln(a)}}$$

### Rule 4: General Logarithm with Chain Rule

$$\boxed{\frac{d}{dx}[\log_a(u)] = \frac{u'}{u \ln(a)}}$$

---

## Deriving $\frac{d}{dx}[\log_a(x)]$

Using the change of base formula:

$$\log_a(x) = \frac{\ln(x)}{\ln(a)}$$

Since $\ln(a)$ is a constant:

$$\frac{d}{dx}[\log_a(x)] = \frac{1}{\ln(a)} \cdot \frac{d}{dx}[\ln(x)] = \frac{1}{\ln(a)} \cdot \frac{1}{x} = \frac{1}{x\ln(a)}$$

**Special case:** When $a = e$, $\ln(e) = 1$, so $\frac{d}{dx}[\ln(x)] = \frac{1}{x}$.

---

## Worked Examples: Basic Logarithms

### Example 1: Simple $\ln(x)$

**Differentiate $f(x) = 3\ln(x)$**

**Solution:**

$$f'(x) = 3 \cdot \frac{1}{x} = \frac{3}{x}$$

**Answer:** $f'(x) = \frac{3}{x}$

---

### Example 2: $\ln$ of Linear Function

**Differentiate $f(x) = \ln(2x)$**

**Solution:**

$$f'(x) = \frac{1}{2x} \cdot 2 = \frac{2}{2x} = \frac{1}{x}$$

**Answer:** $f'(x) = \frac{1}{x}$

*Note: This makes sense since $\ln(2x) = \ln(2) + \ln(x)$, and $\ln(2)$ is constant!*

---

### Example 3: $\ln$ of Polynomial

**Differentiate $g(x) = \ln(x^2 + 1)$**

**Solution:**

$$g'(x) = \frac{2x}{x^2 + 1}$$

**Answer:** $g'(x) = \frac{2x}{x^2 + 1}$

---

### Example 4: $\ln$ of Power

**Differentiate $h(x) = \ln(x^3)$**

**Solution Method 1 (Chain Rule):**

$$h'(x) = \frac{3x^2}{x^3} = \frac{3}{x}$$

**Solution Method 2 (Simplify First):**

$\ln(x^3) = 3\ln(x)$, so $h'(x) = 3 \cdot \frac{1}{x} = \frac{3}{x}$

**Answer:** $h'(x) = \frac{3}{x}$

---

### Example 5: Log Base 10

**Differentiate $f(x) = \log_{10}(x)$**

**Solution:**

$$f'(x) = \frac{1}{x\ln(10)}$$

**Answer:** $f'(x) = \frac{1}{x\ln(10)}$

---

## Chain Rule with Logarithms

### Example 6: $\ln$ of Trig Function

**Differentiate $f(x) = \ln(\sin(x))$**

**Solution:**

$$f'(x) = \frac{\cos(x)}{\sin(x)} = \cot(x)$$

**Answer:** $f'(x) = \cot(x)$

---

### Example 7: $\ln$ of $\cos(x)$

**Differentiate $g(x) = \ln(\cos(x))$**

**Solution:**

$$g'(x) = \frac{-\sin(x)}{\cos(x)} = -\tan(x)$$

**Answer:** $g'(x) = -\tan(x)$

---

### Example 8: $\ln$ of Exponential

**Differentiate $h(x) = \ln(e^x)$**

**Solution Method 1:**

$$h'(x) = \frac{e^x}{e^x} = 1$$

**Solution Method 2 (Simplify First):**

$\ln(e^x) = x$, so $h'(x) = 1$

**Answer:** $h'(x) = 1$

---

### Example 9: Nested Logarithm

**Differentiate $f(x) = \ln(\ln(x))$**

**Solution:**

$$f'(x) = \frac{1}{\ln(x)} \cdot \frac{1}{x} = \frac{1}{x\ln(x)}$$

**Answer:** $f'(x) = \frac{1}{x\ln(x)}$

---

### Example 10: $\ln$ of Absolute Value

**Differentiate $g(x) = \ln|x|$**

**Solution:**

For $x > 0$: $\ln|x| = \ln(x)$, so $g'(x) = \frac{1}{x}$

For $x < 0$: $\ln|x| = \ln(-x)$, so $g'(x) = \frac{-1}{-x} = \frac{1}{x}$

**Answer:** $g'(x) = \frac{1}{x}$ for all $x \neq 0$

*This is why we often write $\int \frac{1}{x}dx = \ln|x| + C$*

---

## Product and Quotient Rule with Logarithms

### Example 11: Product with $x$

**Differentiate $f(x) = x\ln(x)$**

**Solution:**

$$f'(x) = 1 \cdot \ln(x) + x \cdot \frac{1}{x} = \ln(x) + 1$$

**Answer:** $f'(x) = \ln(x) + 1$

---

### Example 12: Product with $x^2$

**Differentiate $g(x) = x^2\ln(x)$**

**Solution:**

$$g'(x) = 2x\ln(x) + x^2 \cdot \frac{1}{x} = 2x\ln(x) + x = x(2\ln(x) + 1)$$

**Answer:** $g'(x) = x(2\ln(x) + 1)$

---

### Example 13: Quotient

**Differentiate $h(x) = \frac{\ln(x)}{x}$**

**Solution:**

$$h'(x) = \frac{\frac{1}{x} \cdot x - \ln(x) \cdot 1}{x^2} = \frac{1 - \ln(x)}{x^2}$$

**Answer:** $h'(x) = \frac{1 - \ln(x)}{x^2}$

---

## Logarithmic Differentiation

### When to Use It

Logarithmic differentiation is powerful for:

1. **Products of many functions:** $f(x) = x^2(x+1)^3(x-2)^4$
2. **Complex quotients:** $f(x) = \frac{x^2\sqrt{x+1}}{(x-1)^3}$
3. **Variable base AND exponent:** $f(x) = x^x$, $f(x) = (\sin x)^x$

### The Technique

1. Take $\ln$ of both sides: $\ln(y) = \ln(f(x))$
2. Simplify using log properties
3. Differentiate implicitly
4. Solve for $\frac{dy}{dx}$
5. Substitute back $y = f(x)$

---

### Example 14: $x^x$

**Differentiate $f(x) = x^x$ for $x > 0$**

**Solution:**

Let $y = x^x$

**Take ln of both sides:**

$$\ln(y) = \ln(x^x) = x\ln(x)$$

**Differentiate implicitly:**

$$\frac{1}{y} \cdot \frac{dy}{dx} = 1 \cdot \ln(x) + x \cdot \frac{1}{x} = \ln(x) + 1$$

**Solve for $\frac{dy}{dx}$:**

$$\frac{dy}{dx} = y(\ln(x) + 1) = x^x(\ln(x) + 1)$$

**Answer:** $f'(x) = x^x(\ln(x) + 1)$

---

### Example 15: $x^{\sin(x)}$

**Differentiate $f(x) = x^{\sin(x)}$ for $x > 0$**

**Solution:**

Let $y = x^{\sin(x)}$

$$\ln(y) = \sin(x) \cdot \ln(x)$$

**Differentiate (product rule on right side):**

$$\frac{1}{y} \cdot \frac{dy}{dx} = \cos(x)\ln(x) + \sin(x) \cdot \frac{1}{x}$$

$$\frac{dy}{dx} = y\left[\cos(x)\ln(x) + \frac{\sin(x)}{x}\right]$$

$$= x^{\sin(x)}\left[\cos(x)\ln(x) + \frac{\sin(x)}{x}\right]$$

**Answer:** $f'(x) = x^{\sin(x)}\left[\cos(x)\ln(x) + \frac{\sin(x)}{x}\right]$

---

### Example 16: Complex Product

**Differentiate $f(x) = x^2(x+1)^3(x+2)^4$**

**Solution:**

Let $y = x^2(x+1)^3(x+2)^4$

$$\ln(y) = 2\ln(x) + 3\ln(x+1) + 4\ln(x+2)$$

**Differentiate:**

$$\frac{1}{y} \cdot \frac{dy}{dx} = \frac{2}{x} + \frac{3}{x+1} + \frac{4}{x+2}$$

$$\frac{dy}{dx} = y\left[\frac{2}{x} + \frac{3}{x+1} + \frac{4}{x+2}\right]$$

$$= x^2(x+1)^3(x+2)^4\left[\frac{2}{x} + \frac{3}{x+1} + \frac{4}{x+2}\right]$$

**Answer:** $f'(x) = x^2(x+1)^3(x+2)^4\left[\frac{2}{x} + \frac{3}{x+1} + \frac{4}{x+2}\right]$

---

### Example 17: Complex Quotient

**Differentiate $f(x) = \frac{\sqrt{x}(x-1)^2}{(x+1)^3}$**

**Solution:**

$$\ln(y) = \frac{1}{2}\ln(x) + 2\ln(x-1) - 3\ln(x+1)$$

**Differentiate:**

$$\frac{1}{y} \cdot \frac{dy}{dx} = \frac{1}{2x} + \frac{2}{x-1} - \frac{3}{x+1}$$

$$\frac{dy}{dx} = \frac{\sqrt{x}(x-1)^2}{(x+1)^3}\left[\frac{1}{2x} + \frac{2}{x-1} - \frac{3}{x+1}\right]$$

**Answer:** $f'(x) = \frac{\sqrt{x}(x-1)^2}{(x+1)^3}\left[\frac{1}{2x} + \frac{2}{x-1} - \frac{3}{x+1}\right]$

---

## Finding Tangent Lines

### Example 18: Tangent to $\ln(x)$

**Find the equation of the tangent line to $y = \ln(x)$ at $x = e$.**

**Solution:**

**Point:** $(e, \ln(e)) = (e, 1)$

**Slope:** $\frac{dy}{dx} = \frac{1}{x}$, at $x = e$: $m = \frac{1}{e}$

**Tangent line:**

$$y - 1 = \frac{1}{e}(x - e)$$

$$y = \frac{x}{e} - 1 + 1 = \frac{x}{e}$$

**Answer:** $y = \frac{x}{e}$

---

### Example 19: Tangent to $x\ln(x)$

**Find the slope of the tangent to $y = x\ln(x)$ at $x = 1$.**

**Solution:**

From Example 11: $\frac{dy}{dx} = \ln(x) + 1$

At $x = 1$:

$$m = \ln(1) + 1 = 0 + 1 = 1$$

**Answer:** Slope $= 1$

---

### Example 20: Horizontal Tangent

**Find where $f(x) = x^2 - 4\ln(x)$ has a horizontal tangent.**

**Solution:**

$$f'(x) = 2x - \frac{4}{x}$$

Set $f'(x) = 0$:

$$2x - \frac{4}{x} = 0$$

$$2x = \frac{4}{x}$$

$$2x^2 = 4$$

$$x^2 = 2$$

$$x = \sqrt{2}$$ (only positive value since domain requires $x > 0$)

**Answer:** $x = \sqrt{2}$

---

## Key Formulas & Rules

### Essential Formulas

$$\frac{d}{dx}[\ln(x)] = \frac{1}{x}$$

$$\frac{d}{dx}[\ln(u)] = \frac{u'}{u}$$

$$\frac{d}{dx}[\log_a(x)] = \frac{1}{x\ln(a)}$$

$$\frac{d}{dx}[\ln|x|] = \frac{1}{x}$$

### Quick Reference

| Function | Derivative |
|----------|------------|
| $\ln(x)$ | $\frac{1}{x}$ |
| $\ln(3x)$ | $\frac{1}{x}$ |
| $\ln(x^2)$ | $\frac{2}{x}$ |
| $\ln(x^2+1)$ | $\frac{2x}{x^2+1}$ |
| $\log_{10}(x)$ | $\frac{1}{x\ln(10)}$ |
| $x\ln(x)$ | $\ln(x) + 1$ |

### Logarithmic Differentiation Pattern

For $y = f(x)^{g(x)}$:

$$\frac{dy}{dx} = f(x)^{g(x)}\left[g'(x)\ln(f(x)) + g(x)\frac{f'(x)}{f(x)}\right]$$

---

## Common Mistakes to Avoid

### Mistake 1: Wrong Derivative for $\ln(x)$

**Wrong:**

$$\frac{d}{dx}[\ln(x)] = \frac{1}{\ln(x)} \quad \text{✗}$$

**Right:**

$$\frac{d}{dx}[\ln(x)] = \frac{1}{x} \quad \text{✓}$$

---

### Mistake 2: Forgetting Chain Rule

**Wrong:**

$$\frac{d}{dx}[\ln(x^2 + 1)] = \frac{1}{x^2 + 1} \quad \text{✗}$$

**Right:**

$$\frac{d}{dx}[\ln(x^2 + 1)] = \frac{2x}{x^2 + 1} \quad \text{✓}$$

---

### Mistake 3: Confusing $\ln(x^n)$ and $(\ln x)^n$

| Expression | Meaning | Derivative |
|------------|---------|------------|
| $\ln(x^n)$ | $n\ln(x)$ | $\frac{n}{x}$ |
| $(\ln x)^n$ | $[\ln(x)]^n$ | $n(\ln x)^{n-1} \cdot \frac{1}{x}$ |

---

### Mistake 4: Power Rule on $x^x$

**Wrong:**

$$\frac{d}{dx}[x^x] = x \cdot x^{x-1} = x^x \quad \text{✗}$$

Power rule doesn't work when the exponent contains $x$!

**Right:** Use logarithmic differentiation to get $x^x(\ln(x) + 1)$

---

## AP Exam Tips

### Must-Know Facts

1. $\frac{d}{dx}[\ln(x)] = \frac{1}{x}$
2. $\frac{d}{dx}[\ln(u)] = \frac{u'}{u}$ — the "u-prime over u" pattern
3. When to use logarithmic differentiation

### Common Question Types

1. **Basic log derivatives:** $\frac{d}{dx}[\ln(x^2 + 1)]$
2. **Products with $\ln$:** $\frac{d}{dx}[x\ln(x)]$
3. **Tangent lines:** To $y = \ln(x)$ at various points
4. **Logarithmic differentiation:** For $x^x$ or complex products
5. **Implicit with logs:** Equations like $\ln(xy) = x + y$

### Speed Tips

1. **Simplify first:** $\ln(x^3) = 3\ln(x)$ makes differentiation easier
2. **Recognize $\frac{u'}{u}$:** Derivative of $\ln(u)$ pattern appears often
3. **Log properties save time:** Use them before differentiating

---

## Practice Problems

### Basic (Problems 1-5)

**1.** Differentiate:

$$f(x) = 5\ln(x)$$

---

**2.** Differentiate:

$$g(x) = \ln(3x + 1)$$

---

**3.** Differentiate:

$$h(x) = \ln(x^4)$$

---

**4.** Differentiate:

$$f(x) = \log_2(x)$$

---

**5.** Differentiate:

$$g(x) = \ln(\sqrt{x})$$

---

### Intermediate (Problems 6-10)

**6.** Differentiate:

$$f(x) = \ln(x^2 + 4x)$$

---

**7.** Differentiate:

$$g(x) = x^3\ln(x)$$

---

**8.** Differentiate:

$$h(x) = \frac{\ln(x)}{x^2}$$

---

**9.** Differentiate:

$$f(x) = \ln(\tan(x))$$

---

**10.** Differentiate:

$$g(x) = e^x\ln(x)$$

---

### Advanced (Problems 11-15)

**11.** Use logarithmic differentiation:

$$f(x) = x^{2x}$$

---

**12.** Use logarithmic differentiation:

$$g(x) = (\cos x)^x$$

---

**13.** Find the equation of the tangent line to $y = \ln(x^2)$ at $x = e$.

---

**14.** Find all values of $x$ where $f(x) = \ln(x) - x$ has a horizontal tangent.

---

**15.** Differentiate:

$$h(x) = \ln\left(\frac{x+1}{x-1}\right)$$

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

$\frac{d}{dx}[\ln(x^2 + e^x)] =$

| Choice | Answer |
|--------|--------|
| **(A)** | $\frac{2x + e^x}{x^2 + e^x}$ |
| **(B)** | $\frac{1}{x^2 + e^x}$ |
| **(C)** | $\frac{2x + e^x}{x^2 + e^{2x}}$ |
| **(D)** | $\frac{2x}{x^2} + \frac{e^x}{e^x}$ |

---

#### Problem 17 (Multiple Choice)

If $f(x) = x\ln(x) - x$, then $f'(e) =$

| Choice | Answer |
|--------|--------|
| **(A)** | $0$ |
| **(B)** | $1$ |
| **(C)** | $e$ |
| **(D)** | $\frac{1}{e}$ |

---

#### Problem 18 (Free Response)

Let $f(x) = \ln(x) - \frac{x}{e}$ for $x > 0$.

> **(a)** Find $f'(x)$ and $f''(x)$.
>
> **(b)** Find the absolute maximum value of $f$ and the value of $x$ at which it occurs.
>
> **(c)** Show that $\ln(x) < \frac{x}{e}$ for all $x > 0$, $x \neq e$.

---

#### Problem 19 (Multiple Choice)

Using logarithmic differentiation, $\frac{d}{dx}[x^{\sqrt{x}}]$ for $x > 0$ equals:

| Choice | Answer |
|--------|--------|
| **(A)** | $x^{\sqrt{x}}\left(\frac{\ln(x)}{2\sqrt{x}} + \frac{1}{\sqrt{x}}\right)$ |
| **(B)** | $x^{\sqrt{x}}\left(\frac{\ln(x) + 2}{2\sqrt{x}}\right)$ |
| **(C)** | $\sqrt{x} \cdot x^{\sqrt{x}-1}$ |
| **(D)** | $x^{\sqrt{x}} \cdot \ln(x)$ |

---

#### Problem 20 (Free Response - Challenging)

Consider the function $f(x) = x^{1/x}$ for $x > 0$.

> **(a)** Use logarithmic differentiation to find $f'(x)$.
>
> **(b)** Find the maximum value of $f$ and show that $e^{1/e}$ is the largest value of $x^{1/x}$.
>
> **(c)** Determine whether $e^\pi$ or $\pi^e$ is larger. *(Hint: Consider $f(e)$ vs $f(\pi)$)*

---

## Solutions

<details>
<summary><strong>Solution 1</strong></summary>

**Problem:** $f(x) = 5\ln(x)$

$$f'(x) = 5 \cdot \frac{1}{x} = \frac{5}{x}$$

**Answer:** $f'(x) = \frac{5}{x}$

</details>

---

<details>
<summary><strong>Solution 2</strong></summary>

**Problem:** $g(x) = \ln(3x + 1)$

$$g'(x) = \frac{3}{3x + 1}$$

**Answer:** $g'(x) = \frac{3}{3x + 1}$

</details>

---

<details>
<summary><strong>Solution 3</strong></summary>

**Problem:** $h(x) = \ln(x^4)$

**Method 1:** $h(x) = 4\ln(x)$, so $h'(x) = \frac{4}{x}$

**Method 2:** $h'(x) = \frac{4x^3}{x^4} = \frac{4}{x}$

**Answer:** $h'(x) = \frac{4}{x}$

</details>

---

<details>
<summary><strong>Solution 4</strong></summary>

**Problem:** $f(x) = \log_2(x)$

$$f'(x) = \frac{1}{x\ln(2)}$$

**Answer:** $f'(x) = \frac{1}{x\ln(2)}$

</details>

---

<details>
<summary><strong>Solution 5</strong></summary>

**Problem:** $g(x) = \ln(\sqrt{x}) = \ln(x^{1/2}) = \frac{1}{2}\ln(x)$

$$g'(x) = \frac{1}{2} \cdot \frac{1}{x} = \frac{1}{2x}$$

**Answer:** $g'(x) = \frac{1}{2x}$

</details>

---

<details>
<summary><strong>Solution 6</strong></summary>

**Problem:** $f(x) = \ln(x^2 + 4x)$

$$f'(x) = \frac{2x + 4}{x^2 + 4x} = \frac{2(x + 2)}{x(x + 4)}$$

**Answer:** $f'(x) = \frac{2x + 4}{x^2 + 4x}$

</details>

---

<details>
<summary><strong>Solution 7</strong></summary>

**Problem:** $g(x) = x^3\ln(x)$

**Product rule:**

$$g'(x) = 3x^2\ln(x) + x^3 \cdot \frac{1}{x} = 3x^2\ln(x) + x^2 = x^2(3\ln(x) + 1)$$

**Answer:** $g'(x) = x^2(3\ln(x) + 1)$

</details>

---

<details>
<summary><strong>Solution 8</strong></summary>

**Problem:** $h(x) = \frac{\ln(x)}{x^2}$

**Quotient rule:**

$$h'(x) = \frac{\frac{1}{x} \cdot x^2 - \ln(x) \cdot 2x}{x^4} = \frac{x - 2x\ln(x)}{x^4} = \frac{1 - 2\ln(x)}{x^3}$$

**Answer:** $h'(x) = \frac{1 - 2\ln(x)}{x^3}$

</details>

---

<details>
<summary><strong>Solution 9</strong></summary>

**Problem:** $f(x) = \ln(\tan(x))$

$$f'(x) = \frac{\sec^2(x)}{\tan(x)} = \frac{1/\cos^2(x)}{\sin(x)/\cos(x)} = \frac{1}{\sin(x)\cos(x)}$$

Using $2\sin(x)\cos(x) = \sin(2x)$:

$$f'(x) = \frac{2}{\sin(2x)} = 2\csc(2x)$$

**Answer:** $f'(x) = \frac{\sec^2(x)}{\tan(x)} = 2\csc(2x)$

</details>

---

<details>
<summary><strong>Solution 10</strong></summary>

**Problem:** $g(x) = e^x\ln(x)$

**Product rule:**

$$g'(x) = e^x\ln(x) + e^x \cdot \frac{1}{x} = e^x\left(\ln(x) + \frac{1}{x}\right)$$

**Answer:** $g'(x) = e^x\left(\ln(x) + \frac{1}{x}\right)$

</details>

---

<details>
<summary><strong>Solution 11</strong></summary>

**Problem:** $f(x) = x^{2x}$ (logarithmic differentiation)

Let $y = x^{2x}$

$$\ln(y) = 2x\ln(x)$$

**Differentiate:**

$$\frac{1}{y} \cdot y' = 2\ln(x) + 2x \cdot \frac{1}{x} = 2\ln(x) + 2$$

$$y' = y \cdot 2(\ln(x) + 1) = x^{2x} \cdot 2(\ln(x) + 1)$$

**Answer:** $f'(x) = 2x^{2x}(\ln(x) + 1)$

</details>

---

<details>
<summary><strong>Solution 12</strong></summary>

**Problem:** $g(x) = (\cos x)^x$

Let $y = (\cos x)^x$

$$\ln(y) = x\ln(\cos x)$$

**Differentiate:**

$$\frac{y'}{y} = \ln(\cos x) + x \cdot \frac{-\sin x}{\cos x} = \ln(\cos x) - x\tan x$$

$$y' = (\cos x)^x[\ln(\cos x) - x\tan x]$$

**Answer:** $g'(x) = (\cos x)^x[\ln(\cos x) - x\tan x]$

</details>

---

<details>
<summary><strong>Solution 13</strong></summary>

**Problem:** Tangent to $y = \ln(x^2) = 2\ln(x)$ at $x = e$

**Point:** $(e, 2\ln(e)) = (e, 2)$

**Slope:** $y' = \frac{2}{x}$, at $x = e$: $m = \frac{2}{e}$

**Tangent:**

$$y - 2 = \frac{2}{e}(x - e)$$

$$y = \frac{2x}{e} - 2 + 2 = \frac{2x}{e}$$

**Answer:** $y = \frac{2x}{e}$

</details>

---

<details>
<summary><strong>Solution 14</strong></summary>

**Problem:** Horizontal tangent of $f(x) = \ln(x) - x$

$$f'(x) = \frac{1}{x} - 1$$

Set $f'(x) = 0$:

$$\frac{1}{x} - 1 = 0$$

$$\frac{1}{x} = 1$$

$$x = 1$$

**Answer:** $x = 1$

</details>

---

<details>
<summary><strong>Solution 15</strong></summary>

**Problem:** $h(x) = \ln\left(\frac{x+1}{x-1}\right)$

**Simplify first:**

$$h(x) = \ln(x+1) - \ln(x-1)$$

**Differentiate:**

$$h'(x) = \frac{1}{x+1} - \frac{1}{x-1} = \frac{(x-1) - (x+1)}{(x+1)(x-1)} = \frac{-2}{x^2-1}$$

**Answer:** $h'(x) = \frac{-2}{x^2-1}$

</details>

---

<details>
<summary><strong>Solution 16</strong></summary>

**Problem:** $\frac{d}{dx}[\ln(x^2 + e^x)]$

$$= \frac{2x + e^x}{x^2 + e^x}$$

**Answer:** **(A)** $\frac{2x + e^x}{x^2 + e^x}$

</details>

---

<details>
<summary><strong>Solution 17</strong></summary>

**Problem:** $f(x) = x\ln(x) - x$, find $f'(e)$

$$f'(x) = \ln(x) + x \cdot \frac{1}{x} - 1 = \ln(x) + 1 - 1 = \ln(x)$$

$$f'(e) = \ln(e) = 1$$

**Answer:** **(B)** $1$

</details>

---

<details>
<summary><strong>Solution 18</strong></summary>

**Problem:** $f(x) = \ln(x) - \frac{x}{e}$

**(a) Derivatives:**

$$f'(x) = \frac{1}{x} - \frac{1}{e}$$

$$f''(x) = -\frac{1}{x^2}$$

**(b) Maximum:**

Set $f'(x) = 0$: $\frac{1}{x} = \frac{1}{e}$, so $x = e$

Since $f''(e) = -\frac{1}{e^2} < 0$, this is a maximum.

$$f(e) = \ln(e) - \frac{e}{e} = 1 - 1 = 0$$

**Answer (b):** Maximum value is $0$ at $x = e$

**(c) Show $\ln(x) < \frac{x}{e}$ for $x \neq e$:**

Since $f(x) = \ln(x) - \frac{x}{e}$ has its maximum at $x = e$ with $f(e) = 0$, we have $f(x) \leq 0$ for all $x > 0$, with equality only at $x = e$.

Therefore $\ln(x) - \frac{x}{e} < 0$ for $x \neq e$, which means $\ln(x) < \frac{x}{e}$.

</details>

---

<details>
<summary><strong>Solution 19</strong></summary>

**Problem:** $\frac{d}{dx}[x^{\sqrt{x}}]$

Let $y = x^{\sqrt{x}}$

$$\ln(y) = \sqrt{x}\ln(x)$$

**Differentiate:**

$$\frac{y'}{y} = \frac{1}{2\sqrt{x}}\ln(x) + \sqrt{x} \cdot \frac{1}{x}$$

$$= \frac{\ln(x)}{2\sqrt{x}} + \frac{1}{\sqrt{x}} = \frac{\ln(x) + 2}{2\sqrt{x}}$$

$$y' = x^{\sqrt{x}} \cdot \frac{\ln(x) + 2}{2\sqrt{x}}$$

**Answer:** **(B)** $x^{\sqrt{x}}\left(\frac{\ln(x) + 2}{2\sqrt{x}}\right)$

</details>

---

<details>
<summary><strong>Solution 20</strong></summary>

**Problem:** $f(x) = x^{1/x}$ for $x > 0$

**(a) Find $f'(x)$:**

Let $y = x^{1/x}$

$$\ln(y) = \frac{1}{x}\ln(x) = \frac{\ln(x)}{x}$$

**Differentiate (quotient rule on right):**

$$\frac{y'}{y} = \frac{\frac{1}{x} \cdot x - \ln(x) \cdot 1}{x^2} = \frac{1 - \ln(x)}{x^2}$$

$$y' = x^{1/x} \cdot \frac{1 - \ln(x)}{x^2}$$

**Answer (a):** $f'(x) = x^{1/x} \cdot \frac{1 - \ln(x)}{x^2}$

**(b) Maximum value:**

$f'(x) = 0$ when $1 - \ln(x) = 0$, so $\ln(x) = 1$, giving $x = e$

For $x < e$: $\ln(x) < 1$, so $f'(x) > 0$ (increasing)
For $x > e$: $\ln(x) > 1$, so $f'(x) < 0$ (decreasing)

Maximum at $x = e$: $f(e) = e^{1/e}$

**Answer (b):** Maximum is $e^{1/e} \approx 1.4447$

**(c) Compare $e^\pi$ and $\pi^e$:**

Consider $f(e) = e^{1/e}$ and $f(\pi) = \pi^{1/\pi}$

Since $\pi > e$ and $f$ is decreasing for $x > e$:

$$f(\pi) < f(e)$$

$$\pi^{1/\pi} < e^{1/e}$$

Raise both sides to the power $e\pi$:

$$(\pi^{1/\pi})^{e\pi} < (e^{1/e})^{e\pi}$$

$$\pi^e < e^\pi$$

**Answer (c):** $e^\pi > \pi^e$

</details>

---

## What's Next

You've now mastered the derivatives of logarithmic functions! Next up is [Higher-Order Derivatives](/calculus/0405-higher-order-derivatives), where you'll learn about second derivatives, concavity, and how derivatives beyond the first give us deeper insight into function behavior.

---

<div align="center">

[← Exponential Derivatives](/calculus/0403-derivatives-exp) | [Higher-Order Derivatives →](/calculus/0405-higher-order-derivatives)

</div>
