# Derivatives of Exponential Functions

The exponential function $e^x$ holds a special place in calculus — it's the only function that equals its own derivative. This remarkable property makes $e$ the natural base for exponential growth and decay problems. In this article, you'll master differentiating $e^x$, general exponentials $a^x$, and complex combinations.

---

## What You'll Learn

- Understand why $e^x$ is its own derivative
- Differentiate $e^x$ and $e^{u(x)}$ using the chain rule
- Derive and apply the formula for $\frac{d}{dx}[a^x]$
- Solve problems involving exponential growth and decay
- Handle complex combinations of exponential functions
- Tackle AP Calculus problems with confidence

---

## Prerequisites

- [Chain Rule](/calculus/chain-rule) — essential for $e^{3x}$, $e^{x^2}$, etc.
- [Product Rule](/calculus/product-rule) and [Quotient Rule](/calculus/quotient-rule)
- Basic properties of exponents: $e^{a+b} = e^a \cdot e^b$, $(e^a)^b = e^{ab}$

---

## The Core Concept

### What Makes $e$ Special?

The number $e \approx 2.71828...$ is defined so that:

$$\lim_{h \to 0} \frac{e^h - 1}{h} = 1$$

This limit is the key! It means when we differentiate $e^x$, something magical happens.

### Deriving $\frac{d}{dx}[e^x]$

Using the limit definition of the derivative:

$$\frac{d}{dx}[e^x] = \lim_{h \to 0} \frac{e^{x+h} - e^x}{h}$$

Factor out $e^x$:

$$= \lim_{h \to 0} \frac{e^x \cdot e^h - e^x}{h} = \lim_{h \to 0} e^x \cdot \frac{e^h - 1}{h}$$

Since $e^x$ doesn't depend on $h$:

$$= e^x \cdot \lim_{h \to 0} \frac{e^h - 1}{h} = e^x \cdot 1 = e^x$$

$$\boxed{\frac{d}{dx}[e^x] = e^x}$$

**The derivative of $e^x$ is itself!** No other function has this property.

---

## The Exponential Derivative Rules

### Rule 1: Natural Exponential

$$\boxed{\frac{d}{dx}[e^x] = e^x}$$

### Rule 2: Natural Exponential with Chain Rule

$$\boxed{\frac{d}{dx}[e^{u}] = e^{u} \cdot \frac{du}{dx}}$$

### Rule 3: General Exponential

$$\boxed{\frac{d}{dx}[a^x] = a^x \ln(a)}$$

### Rule 4: General Exponential with Chain Rule

$$\boxed{\frac{d}{dx}[a^{u}] = a^{u} \ln(a) \cdot \frac{du}{dx}}$$

---

## Deriving $\frac{d}{dx}[a^x]$

For any positive base $a \neq 1$, we can write:

$$a^x = e^{\ln(a^x)} = e^{x \ln(a)}$$

Now differentiate using the chain rule:

$$\frac{d}{dx}[a^x] = \frac{d}{dx}[e^{x \ln(a)}] = e^{x \ln(a)} \cdot \ln(a)$$

Since $e^{x \ln(a)} = a^x$:

$$\frac{d}{dx}[a^x] = a^x \ln(a)$$

**Special case:** When $a = e$, $\ln(e) = 1$, so we get $\frac{d}{dx}[e^x] = e^x \cdot 1 = e^x$.

---

## Worked Examples: Basic Exponentials

### Example 1: Simple $e^x$

**Differentiate $f(x) = 5e^x$**

**Solution:**

$$f'(x) = 5 \cdot e^x = 5e^x$$

**Answer:** $f'(x) = 5e^x$

---

### Example 2: $e^x$ with Linear Argument

**Differentiate $f(x) = e^{3x}$**

**Solution:**

- Outer: $e^u$, derivative: $e^u$
- Inner: $u = 3x$, derivative: $3$

$$f'(x) = e^{3x} \cdot 3 = 3e^{3x}$$

**Answer:** $f'(x) = 3e^{3x}$

---

### Example 3: $e^x$ with Quadratic Argument

**Differentiate $g(x) = e^{x^2}$**

**Solution:**

$$g'(x) = e^{x^2} \cdot 2x = 2xe^{x^2}$$

**Answer:** $g'(x) = 2xe^{x^2}$

---

### Example 4: Negative Exponent

**Differentiate $h(x) = e^{-x}$**

**Solution:**

$$h'(x) = e^{-x} \cdot (-1) = -e^{-x}$$

**Answer:** $h'(x) = -e^{-x}$

---

### Example 5: General Exponential Base 2

**Differentiate $f(x) = 2^x$**

**Solution:**

$$f'(x) = 2^x \ln(2)$$

**Answer:** $f'(x) = 2^x \ln(2)$

---

### Example 6: General Exponential Base 10

**Differentiate $g(x) = 10^x$**

**Solution:**

$$g'(x) = 10^x \ln(10)$$

**Answer:** $g'(x) = 10^x \ln(10)$

---

## Worked Examples: Chain Rule Combinations

### Example 7: Exponential of Polynomial

**Differentiate $f(x) = e^{x^3 - 2x}$**

**Solution:**

$$f'(x) = e^{x^3 - 2x} \cdot (3x^2 - 2)$$

**Answer:** $f'(x) = (3x^2 - 2)e^{x^3 - 2x}$

---

### Example 8: Exponential of Trig Function

**Differentiate $g(x) = e^{\sin(x)}$**

**Solution:**

$$g'(x) = e^{\sin(x)} \cdot \cos(x)$$

**Answer:** $g'(x) = \cos(x) \cdot e^{\sin(x)}$

---

### Example 9: Exponential of Square Root

**Differentiate $h(x) = e^{\sqrt{x}}$**

**Solution:**

$$h'(x) = e^{\sqrt{x}} \cdot \frac{1}{2\sqrt{x}} = \frac{e^{\sqrt{x}}}{2\sqrt{x}}$$

**Answer:** $h'(x) = \frac{e^{\sqrt{x}}}{2\sqrt{x}}$

---

### Example 10: General Exponential with Chain Rule

**Differentiate $f(x) = 3^{2x+1}$**

**Solution:**

$$f'(x) = 3^{2x+1} \cdot \ln(3) \cdot 2 = 2\ln(3) \cdot 3^{2x+1}$$

**Answer:** $f'(x) = 2\ln(3) \cdot 3^{2x+1}$

---

## Product Rule with Exponentials

### Example 11: $x$ times $e^x$

**Differentiate $f(x) = xe^x$**

**Solution:**

$$f'(x) = 1 \cdot e^x + x \cdot e^x = e^x + xe^x = e^x(1 + x)$$

**Answer:** $f'(x) = e^x(1 + x)$ or $(x + 1)e^x$

---

### Example 12: $x^2$ times $e^x$

**Differentiate $g(x) = x^2 e^x$**

**Solution:**

$$g'(x) = 2x \cdot e^x + x^2 \cdot e^x = e^x(2x + x^2) = xe^x(2 + x)$$

**Answer:** $g'(x) = e^x(x^2 + 2x)$ or $xe^x(x + 2)$

---

### Example 13: Exponential times Trig

**Differentiate $h(x) = e^x \sin(x)$**

**Solution:**

$$h'(x) = e^x \sin(x) + e^x \cos(x) = e^x(\sin(x) + \cos(x))$$

**Answer:** $h'(x) = e^x(\sin(x) + \cos(x))$

---

### Example 14: Exponential times Polynomial

**Differentiate $f(x) = (x^2 + 3x)e^{2x}$**

**Solution:**

$$f'(x) = (2x + 3)e^{2x} + (x^2 + 3x) \cdot 2e^{2x}$$

$$= e^{2x}[(2x + 3) + 2(x^2 + 3x)]$$

$$= e^{2x}[2x + 3 + 2x^2 + 6x]$$

$$= e^{2x}[2x^2 + 8x + 3]$$

**Answer:** $f'(x) = e^{2x}(2x^2 + 8x + 3)$

---

## Quotient Rule with Exponentials

### Example 15: Exponential over $x$

**Differentiate $f(x) = \frac{e^x}{x}$**

**Solution:**

$$f'(x) = \frac{e^x \cdot x - e^x \cdot 1}{x^2} = \frac{e^x(x - 1)}{x^2}$$

**Answer:** $f'(x) = \frac{e^x(x - 1)}{x^2}$

---

### Example 16: Polynomial over Exponential

**Differentiate $g(x) = \frac{x^2}{e^x}$**

**Solution:**

$$g'(x) = \frac{2x \cdot e^x - x^2 \cdot e^x}{e^{2x}} = \frac{e^x(2x - x^2)}{e^{2x}} = \frac{2x - x^2}{e^x}$$

$$= \frac{x(2 - x)}{e^x}$$

**Answer:** $g'(x) = \frac{x(2 - x)}{e^x}$

*Alternative:* Write as $x^2 e^{-x}$ and use product rule.

---

## Nested Exponentials

### Example 17: $e$ to the $e^x$

**Differentiate $f(x) = e^{e^x}$**

**Solution:**

$$f'(x) = e^{e^x} \cdot e^x$$

**Answer:** $f'(x) = e^x \cdot e^{e^x}$ or $e^{x + e^x}$

---

### Example 18: Double Exponential

**Differentiate $g(x) = e^{e^{2x}}$**

**Solution:**

$$g'(x) = e^{e^{2x}} \cdot e^{2x} \cdot 2 = 2e^{2x} \cdot e^{e^{2x}}$$

**Answer:** $g'(x) = 2e^{2x + e^{2x}}$

---

## Finding Tangent Lines

### Example 19: Tangent to $e^x$

**Find the equation of the tangent line to $y = e^x$ at $x = 0$.**

**Solution:**

**Point:** $(0, e^0) = (0, 1)$

**Slope:** $\frac{dy}{dx} = e^x$, so at $x = 0$: $m = e^0 = 1$

**Tangent line:**

$$y - 1 = 1(x - 0)$$

$$y = x + 1$$

**Answer:** $y = x + 1$

---

### Example 20: Horizontal Tangent

**Find all points where $f(x) = xe^{-x}$ has a horizontal tangent.**

**Solution:**

$$f'(x) = 1 \cdot e^{-x} + x \cdot (-e^{-x}) = e^{-x}(1 - x)$$

Set $f'(x) = 0$:

$$e^{-x}(1 - x) = 0$$

Since $e^{-x} > 0$ always, we need $1 - x = 0$, so $x = 1$.

At $x = 1$: $f(1) = 1 \cdot e^{-1} = \frac{1}{e}$

**Answer:** Horizontal tangent at $\left(1, \frac{1}{e}\right)$

---

## Key Formulas & Rules

### Essential Formulas

$$\frac{d}{dx}[e^x] = e^x$$

$$\frac{d}{dx}[e^{u}] = e^{u} \cdot u'$$

$$\frac{d}{dx}[a^x] = a^x \ln(a)$$

$$\frac{d}{dx}[a^{u}] = a^{u} \ln(a) \cdot u'$$

### Quick Reference

| Function | Derivative |
|----------|------------|
| $e^x$ | $e^x$ |
| $e^{3x}$ | $3e^{3x}$ |
| $e^{-x}$ | $-e^{-x}$ |
| $e^{x^2}$ | $2xe^{x^2}$ |
| $2^x$ | $2^x \ln(2)$ |
| $10^x$ | $10^x \ln(10)$ |

---

## Common Mistakes to Avoid

### Mistake 1: Adding $\ln$ to $e^x$ Derivative

**Wrong:**

$$\frac{d}{dx}[e^x] = e^x \ln(e) \quad \text{✗}$$

**Right:**

$$\frac{d}{dx}[e^x] = e^x \quad \text{✓}$$

The $\ln(a)$ factor only appears for bases other than $e$.

---

### Mistake 2: Forgetting Chain Rule

**Wrong:**

$$\frac{d}{dx}[e^{3x}] = e^{3x} \quad \text{✗}$$

**Right:**

$$\frac{d}{dx}[e^{3x}] = 3e^{3x} \quad \text{✓}$$

---

### Mistake 3: Wrong Formula for $a^x$

**Wrong:**

$$\frac{d}{dx}[2^x] = x \cdot 2^{x-1} \quad \text{✗}$$

This is the power rule — wrong for exponentials!

**Right:**

$$\frac{d}{dx}[2^x] = 2^x \ln(2) \quad \text{✓}$$

---

### Mistake 4: Confusing $e^x$ and $x^e$

| Expression | Type | Derivative |
|------------|------|------------|
| $e^x$ | Exponential | $e^x$ |
| $x^e$ | Power function | $ex^{e-1}$ |

---

## AP Exam Tips

### Must-Know Facts

1. $\frac{d}{dx}[e^x] = e^x$ — memorize this!
2. $\frac{d}{dx}[e^{kx}] = ke^{kx}$ — very common
3. $\frac{d}{dx}[a^x] = a^x \ln(a)$ — know the formula

### Common Question Types

1. **Basic derivatives:** $\frac{d}{dx}[e^{2x}]$
2. **Chain rule:** $\frac{d}{dx}[e^{x^2 + 1}]$
3. **Product rule:** $\frac{d}{dx}[xe^x]$
4. **Tangent lines:** Find tangent to $y = e^x$ at a point
5. **Horizontal tangents:** Where is $f'(x) = 0$?
6. **Growth/decay:** $\frac{d}{dx}[Ce^{kt}]$

### Speed Tips

1. **$e^{kx}$ pattern:** Derivative is $ke^{kx}$ — instant recognition
2. **Factor out $e^x$:** In product rule problems, factor $e^x$ at the end
3. **Rewrite general bases:** $a^x = e^{x\ln(a)}$ if needed

---

## Practice Problems

### Basic (Problems 1-5)

**1.** Differentiate:

$$f(x) = 7e^x$$

---

**2.** Differentiate:

$$g(x) = e^{5x}$$

---

**3.** Differentiate:

$$h(x) = e^{-2x}$$

---

**4.** Differentiate:

$$f(x) = 3^x$$

---

**5.** Differentiate:

$$g(x) = e^{x^2 + 1}$$

---

### Intermediate (Problems 6-10)

**6.** Differentiate:

$$f(x) = x^3 e^x$$

---

**7.** Differentiate:

$$g(x) = e^{\cos(x)}$$

---

**8.** Differentiate:

$$h(x) = \frac{e^x}{x^2}$$

---

**9.** Differentiate:

$$f(x) = e^{2x}\sin(3x)$$

---

**10.** Differentiate:

$$g(x) = 5^{x^2}$$

---

### Advanced (Problems 11-15)

**11.** Find the equation of the tangent line to $y = e^{2x}$ at $x = 0$.

---

**12.** Find all values of $x$ where $f(x) = x^2 e^{-x}$ has a horizontal tangent.

---

**13.** Differentiate:

$$h(x) = \frac{e^x - e^{-x}}{2}$$

*(This is $\sinh(x)$, the hyperbolic sine)*

---

**14.** Differentiate:

$$f(x) = e^{x\ln(x)}$$

*(Hint: What does $e^{x\ln(x)}$ simplify to?)*

---

**15.** Find $\frac{d^2y}{dx^2}$ for $y = xe^{-x}$.

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

If $f(x) = e^{x^2}$, then $f'(2) =$

| Choice | Answer |
|--------|--------|
| **(A)** | $2e^4$ |
| **(B)** | $4e^4$ |
| **(C)** | $e^4$ |
| **(D)** | $4e^2$ |

---

#### Problem 17 (Multiple Choice)

$\frac{d}{dx}\left[x^2 \cdot 2^x\right] =$

| Choice | Answer |
|--------|--------|
| **(A)** | $2x \cdot 2^x + x^2 \cdot 2^x$ |
| **(B)** | $2x \cdot 2^x + x^2 \cdot 2^x \ln(2)$ |
| **(C)** | $2x \cdot 2^{x-1}$ |
| **(D)** | $x^2 \cdot 2^x \ln(2)$ |

---

#### Problem 18 (Free Response)

Let $f(x) = xe^{-x}$ for $x \geq 0$.

> **(a)** Find $f'(x)$ and $f''(x)$.
>
> **(b)** Find the absolute maximum value of $f$ on $[0, \infty)$.
>
> **(c)** Find the x-coordinate of the inflection point.

---

#### Problem 19 (Multiple Choice)

The function $f(x) = e^{-x^2}$ has a local maximum at:

| Choice | Answer |
|--------|--------|
| **(A)** | $x = -1$ |
| **(B)** | $x = 0$ |
| **(C)** | $x = 1$ |
| **(D)** | $f$ has no local maximum |

---

#### Problem 20 (Free Response - Challenging)

A population grows according to $P(t) = 1000e^{0.05t}$, where $t$ is in years.

> **(a)** Find the rate of population growth $P'(t)$.
>
> **(b)** Show that $P'(t) = 0.05 \cdot P(t)$. What does this mean?
>
> **(c)** How long until the population is growing at a rate of 100 individuals per year?

---

## Solutions

<details>
<summary><strong>Solution 1</strong></summary>

**Problem:** $f(x) = 7e^x$

$$f'(x) = 7e^x$$

**Answer:** $f'(x) = 7e^x$

</details>

---

<details>
<summary><strong>Solution 2</strong></summary>

**Problem:** $g(x) = e^{5x}$

$$g'(x) = e^{5x} \cdot 5 = 5e^{5x}$$

**Answer:** $g'(x) = 5e^{5x}$

</details>

---

<details>
<summary><strong>Solution 3</strong></summary>

**Problem:** $h(x) = e^{-2x}$

$$h'(x) = e^{-2x} \cdot (-2) = -2e^{-2x}$$

**Answer:** $h'(x) = -2e^{-2x}$

</details>

---

<details>
<summary><strong>Solution 4</strong></summary>

**Problem:** $f(x) = 3^x$

$$f'(x) = 3^x \ln(3)$$

**Answer:** $f'(x) = 3^x \ln(3)$

</details>

---

<details>
<summary><strong>Solution 5</strong></summary>

**Problem:** $g(x) = e^{x^2 + 1}$

$$g'(x) = e^{x^2 + 1} \cdot 2x = 2xe^{x^2 + 1}$$

**Answer:** $g'(x) = 2xe^{x^2 + 1}$

</details>

---

<details>
<summary><strong>Solution 6</strong></summary>

**Problem:** $f(x) = x^3 e^x$

**Product rule:**

$$f'(x) = 3x^2 \cdot e^x + x^3 \cdot e^x = e^x(3x^2 + x^3) = x^2 e^x(3 + x)$$

**Answer:** $f'(x) = e^x(x^3 + 3x^2)$ or $x^2 e^x(x + 3)$

</details>

---

<details>
<summary><strong>Solution 7</strong></summary>

**Problem:** $g(x) = e^{\cos(x)}$

$$g'(x) = e^{\cos(x)} \cdot (-\sin(x)) = -\sin(x) \cdot e^{\cos(x)}$$

**Answer:** $g'(x) = -\sin(x) \cdot e^{\cos(x)}$

</details>

---

<details>
<summary><strong>Solution 8</strong></summary>

**Problem:** $h(x) = \frac{e^x}{x^2}$

**Quotient rule:**

$$h'(x) = \frac{e^x \cdot x^2 - e^x \cdot 2x}{x^4} = \frac{e^x(x^2 - 2x)}{x^4} = \frac{e^x \cdot x(x - 2)}{x^4}$$

$$= \frac{e^x(x - 2)}{x^3}$$

**Answer:** $h'(x) = \frac{e^x(x - 2)}{x^3}$

</details>

---

<details>
<summary><strong>Solution 9</strong></summary>

**Problem:** $f(x) = e^{2x}\sin(3x)$

**Product rule:**

$$f'(x) = 2e^{2x} \cdot \sin(3x) + e^{2x} \cdot 3\cos(3x)$$

$$= e^{2x}[2\sin(3x) + 3\cos(3x)]$$

**Answer:** $f'(x) = e^{2x}[2\sin(3x) + 3\cos(3x)]$

</details>

---

<details>
<summary><strong>Solution 10</strong></summary>

**Problem:** $g(x) = 5^{x^2}$

$$g'(x) = 5^{x^2} \cdot \ln(5) \cdot 2x = 2x\ln(5) \cdot 5^{x^2}$$

**Answer:** $g'(x) = 2x\ln(5) \cdot 5^{x^2}$

</details>

---

<details>
<summary><strong>Solution 11</strong></summary>

**Problem:** Tangent to $y = e^{2x}$ at $x = 0$

**Point:** $(0, e^0) = (0, 1)$

**Slope:** $\frac{dy}{dx} = 2e^{2x}$, at $x = 0$: $m = 2e^0 = 2$

**Tangent:**

$$y - 1 = 2(x - 0)$$

$$y = 2x + 1$$

**Answer:** $y = 2x + 1$

</details>

---

<details>
<summary><strong>Solution 12</strong></summary>

**Problem:** Horizontal tangents of $f(x) = x^2 e^{-x}$

$$f'(x) = 2x \cdot e^{-x} + x^2 \cdot (-e^{-x}) = e^{-x}(2x - x^2) = xe^{-x}(2 - x)$$

Set $f'(x) = 0$:

$$xe^{-x}(2 - x) = 0$$

Since $e^{-x} \neq 0$: $x = 0$ or $x = 2$

**Answer:** $x = 0$ and $x = 2$

</details>

---

<details>
<summary><strong>Solution 13</strong></summary>

**Problem:** $h(x) = \frac{e^x - e^{-x}}{2}$

$$h'(x) = \frac{e^x - (-e^{-x})}{2} = \frac{e^x + e^{-x}}{2}$$

**Answer:** $h'(x) = \frac{e^x + e^{-x}}{2}$

*Note: This is $\cosh(x)$, the hyperbolic cosine.*

</details>

---

<details>
<summary><strong>Solution 14</strong></summary>

**Problem:** $f(x) = e^{x\ln(x)}$

First, simplify: $e^{x\ln(x)} = e^{\ln(x^x)} = x^x$

Now differentiate $f(x) = x^x$ using logarithmic differentiation:

Let $y = x^x$, so $\ln(y) = x\ln(x)$

$$\frac{1}{y} \cdot y' = \ln(x) + x \cdot \frac{1}{x} = \ln(x) + 1$$

$$y' = y(\ln(x) + 1) = x^x(\ln(x) + 1)$$

**Answer:** $f'(x) = x^x(\ln(x) + 1)$

</details>

---

<details>
<summary><strong>Solution 15</strong></summary>

**Problem:** $\frac{d^2y}{dx^2}$ for $y = xe^{-x}$

**First derivative:**

$$y' = e^{-x} + x(-e^{-x}) = e^{-x}(1 - x)$$

**Second derivative:**

$$y'' = -e^{-x}(1 - x) + e^{-x}(-1) = e^{-x}[-(1 - x) - 1]$$

$$= e^{-x}[-1 + x - 1] = e^{-x}(x - 2)$$

**Answer:** $\frac{d^2y}{dx^2} = e^{-x}(x - 2)$

</details>

---

<details>
<summary><strong>Solution 16</strong></summary>

**Problem:** $f(x) = e^{x^2}$, find $f'(2)$

$$f'(x) = 2xe^{x^2}$$

$$f'(2) = 2(2)e^{4} = 4e^4$$

**Answer:** **(B)** $4e^4$

</details>

---

<details>
<summary><strong>Solution 17</strong></summary>

**Problem:** $\frac{d}{dx}[x^2 \cdot 2^x]$

**Product rule:**

$$= 2x \cdot 2^x + x^2 \cdot 2^x \ln(2)$$

**Answer:** **(B)** $2x \cdot 2^x + x^2 \cdot 2^x \ln(2)$

</details>

---

<details>
<summary><strong>Solution 18</strong></summary>

**Problem:** $f(x) = xe^{-x}$ for $x \geq 0$

**(a) Find $f'(x)$ and $f''(x)$:**

From Solutions 12 and 15:

$$f'(x) = e^{-x}(1 - x)$$

$$f''(x) = e^{-x}(x - 2)$$

**(b) Absolute maximum:**

Critical point: $f'(x) = 0$ when $x = 1$

$f(1) = 1 \cdot e^{-1} = \frac{1}{e}$

Check endpoints: $f(0) = 0$, $\lim_{x \to \infty} xe^{-x} = 0$

**Answer (b):** Maximum value is $\frac{1}{e}$ at $x = 1$

**(c) Inflection point:**

$f''(x) = 0$ when $x = 2$

Since $f''$ changes sign at $x = 2$, this is an inflection point.

**Answer (c):** $x = 2$

</details>

---

<details>
<summary><strong>Solution 19</strong></summary>

**Problem:** Local maximum of $f(x) = e^{-x^2}$

$$f'(x) = e^{-x^2} \cdot (-2x) = -2xe^{-x^2}$$

Set $f'(x) = 0$: $-2xe^{-x^2} = 0$

Since $e^{-x^2} \neq 0$: $x = 0$

Check: $f''(x) = -2e^{-x^2} + (-2x)(-2x)e^{-x^2} = e^{-x^2}(-2 + 4x^2)$

$f''(0) = e^0(-2) = -2 < 0$ ✓ (concave down, so local max)

**Answer:** **(B)** $x = 0$

</details>

---

<details>
<summary><strong>Solution 20</strong></summary>

**Problem:** $P(t) = 1000e^{0.05t}$

**(a) Rate of growth:**

$$P'(t) = 1000 \cdot 0.05 \cdot e^{0.05t} = 50e^{0.05t}$$

**Answer (a):** $P'(t) = 50e^{0.05t}$

**(b) Show $P'(t) = 0.05 \cdot P(t)$:**

$$0.05 \cdot P(t) = 0.05 \cdot 1000e^{0.05t} = 50e^{0.05t} = P'(t)$$ ✓

**Meaning:** The rate of change is proportional to the current population. This is the defining property of exponential growth — the bigger the population, the faster it grows.

**(c) When is $P'(t) = 100$?**

$$50e^{0.05t} = 100$$

$$e^{0.05t} = 2$$

$$0.05t = \ln(2)$$

$$t = \frac{\ln(2)}{0.05} = 20\ln(2) \approx 13.86 \text{ years}$$

**Answer (c):** $t = 20\ln(2) \approx 13.86$ years

</details>

---

## What's Next

With exponential derivatives mastered, you're ready for [Derivatives of Logarithmic Functions](/calculus/derivatives-log), where you'll learn that $\frac{d}{dx}[\ln(x)] = \frac{1}{x}$ and discover the powerful technique of logarithmic differentiation.

---

<div align="center">

[← Trig Derivatives](/calculus/derivatives-trig) | [Log Derivatives →](/calculus/derivatives-log)

</div>
