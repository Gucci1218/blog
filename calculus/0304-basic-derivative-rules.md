# Basic Derivative Rules
<p class="article-date">December 18, 2024</p>

## Learning Objectives

By the end of this article, you will be able to:

- Apply the constant rule, power rule, and constant multiple rule
- Differentiate sums and differences of functions
- Use the derivatives of exponential and logarithmic functions
- Apply the derivatives of sine and cosine
- Combine multiple rules to differentiate complex expressions
- Rewrite functions to make differentiation easier
- Recognize when to use which rule
- Solve AP Calculus problems efficiently using derivative rules

---

## The Core Concept: Shortcuts That Save Time

### Why We Need Rules

In previous articles, we computed derivatives using the limit definition:

$$f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$$

This works, but it's slow. Imagine using this definition to differentiate $f(x) = x^{10} + 3x^7 - 5x^4 + 2x - 1$. That would take forever!

Fortunately, mathematicians have discovered **shortcut rules** that let us differentiate instantly—without computing any limits.

### The Philosophy Behind the Rules

Each rule is **proven** using the limit definition (once), and then we can **use** the rule forever after. It's like having pre-computed answers:

- Limit definition = calculating from scratch every time
- Derivative rules = using a lookup table of results

Let's build your toolkit of derivative rules.

---

## Rule 1: The Constant Rule

### Statement

$$\boxed{\frac{d}{dx}[c] = 0}$$

The derivative of any constant is zero.

### Intuition

A constant function $f(x) = c$ is a horizontal line. Horizontal lines have slope zero everywhere.

```
y = 5
     |
   5 |_______________
     |
   0 |_________________ x

Slope = 0 everywhere
```

### Proof (Using the Definition)

$$\frac{d}{dx}[c] = \lim_{h \to 0} \frac{c - c}{h} = \lim_{h \to 0} \frac{0}{h} = \lim_{h \to 0} 0 = 0$$

### Examples

| Function | Derivative |
|----------|------------|
| $f(x) = 7$ | $f'(x) = 0$ |
| $f(x) = -3$ | $f'(x) = 0$ |
| $f(x) = \pi$ | $f'(x) = 0$ |
| $f(x) = \sqrt{2}$ | $f'(x) = 0$ |

---

## Rule 2: The Power Rule

### Statement

$$\boxed{\frac{d}{dx}[x^n] = nx^{n-1}}$$

"Bring down the exponent, then reduce the exponent by 1."

### This Works for ALL Real Exponents

The power rule works for:
- Positive integers: $x^5$
- Negative integers: $x^{-3}$
- Fractions: $x^{1/2}$
- Irrational numbers: $x^{\pi}$
- Zero: $x^0 = 1$ (constant, so derivative is 0)

### Memory Device

$$x^n \xrightarrow{\text{derivative}} nx^{n-1}$$

"The exponent comes down in front, and the new exponent is one less."

### Proof (For Positive Integer $n$)

Using the binomial theorem:

$$(x+h)^n = x^n + nx^{n-1}h + \binom{n}{2}x^{n-2}h^2 + \cdots + h^n$$

$$\frac{d}{dx}[x^n] = \lim_{h \to 0} \frac{(x+h)^n - x^n}{h}$$

$$= \lim_{h \to 0} \frac{nx^{n-1}h + \binom{n}{2}x^{n-2}h^2 + \cdots + h^n}{h}$$

$$= \lim_{h \to 0} \left[nx^{n-1} + \binom{n}{2}x^{n-2}h + \cdots + h^{n-1}\right] = nx^{n-1}$$

### Examples

| Function | Derivative | Work |
|----------|------------|------|
| $x^5$ | $5x^4$ | Bring down 5, reduce exponent |
| $x^{100}$ | $100x^{99}$ | |
| $x^1 = x$ | $1 \cdot x^0 = 1$ | |
| $x^0 = 1$ | $0 \cdot x^{-1} = 0$ | Constant! |

---

### Power Rule with Negative Exponents

**Example 1:** Find $\frac{d}{dx}\left[\frac{1}{x^3}\right]$

**Solution:**

First rewrite: $\frac{1}{x^3} = x^{-3}$

Apply the power rule:
$$\frac{d}{dx}[x^{-3}] = -3x^{-4} = -\frac{3}{x^4}$$

---

**Example 2:** Find $\frac{d}{dx}\left[\frac{1}{x}\right]$

**Solution:**

$$\frac{d}{dx}[x^{-1}] = -1 \cdot x^{-2} = -\frac{1}{x^2}$$

---

### Power Rule with Fractional Exponents

**Example 3:** Find $\frac{d}{dx}[\sqrt{x}]$

**Solution:**

Rewrite: $\sqrt{x} = x^{1/2}$

$$\frac{d}{dx}[x^{1/2}] = \frac{1}{2}x^{-1/2} = \frac{1}{2\sqrt{x}}$$

---

**Example 4:** Find $\frac{d}{dx}[\sqrt[3]{x^2}]$

**Solution:**

Rewrite: $\sqrt[3]{x^2} = x^{2/3}$

$$\frac{d}{dx}[x^{2/3}] = \frac{2}{3}x^{-1/3} = \frac{2}{3\sqrt[3]{x}}$$

---

### Converting Between Forms

When differentiating, you often need to convert:

| Original Form | Exponent Form |
|---------------|---------------|
| $\sqrt{x}$ | $x^{1/2}$ |
| $\sqrt[3]{x}$ | $x^{1/3}$ |
| $\sqrt[n]{x}$ | $x^{1/n}$ |
| $\frac{1}{x}$ | $x^{-1}$ |
| $\frac{1}{x^n}$ | $x^{-n}$ |
| $\sqrt[n]{x^m}$ | $x^{m/n}$ |

---

## Rule 3: The Constant Multiple Rule

### Statement

$$\boxed{\frac{d}{dx}[c \cdot f(x)] = c \cdot f'(x)}$$

Constants can be "pulled out" of derivatives.

### Intuition

If you double a function, you double its rate of change. If you halve a function, you halve its rate of change.

### Proof

$$\frac{d}{dx}[cf(x)] = \lim_{h \to 0} \frac{cf(x+h) - cf(x)}{h} = c \cdot \lim_{h \to 0} \frac{f(x+h) - f(x)}{h} = c \cdot f'(x)$$

### Examples

| Function | Derivative |
|----------|------------|
| $5x^3$ | $5 \cdot 3x^2 = 15x^2$ |
| $-2x^4$ | $-2 \cdot 4x^3 = -8x^3$ |
| $\frac{x^5}{3}$ | $\frac{1}{3} \cdot 5x^4 = \frac{5x^4}{3}$ |
| $\pi x^2$ | $\pi \cdot 2x = 2\pi x$ |

---

## Rule 4: The Sum and Difference Rules

### Statement

$$\boxed{\frac{d}{dx}[f(x) + g(x)] = f'(x) + g'(x)}$$

$$\boxed{\frac{d}{dx}[f(x) - g(x)] = f'(x) - g'(x)}$$

The derivative of a sum is the sum of the derivatives.

### Intuition

Rates of change add up. If your salary grows at \$1000/year and your expenses grow at \$300/year, your savings rate changes at \$700/year.

### Examples

**Example 5:** Differentiate $f(x) = x^3 + x^2$

$$f'(x) = 3x^2 + 2x$$

---

**Example 6:** Differentiate $g(x) = 4x^5 - 7x^3 + 2x - 9$

$$g'(x) = 20x^4 - 21x^2 + 2 - 0 = 20x^4 - 21x^2 + 2$$

---

**Example 7:** Differentiate $h(x) = x^4 - \frac{3}{x^2} + 5\sqrt{x}$

First rewrite:
$$h(x) = x^4 - 3x^{-2} + 5x^{1/2}$$

Then differentiate:
$$h'(x) = 4x^3 - 3(-2)x^{-3} + 5 \cdot \frac{1}{2}x^{-1/2}$$
$$= 4x^3 + 6x^{-3} + \frac{5}{2}x^{-1/2}$$
$$= 4x^3 + \frac{6}{x^3} + \frac{5}{2\sqrt{x}}$$

---

## Combining Rules: A Systematic Approach

### The Process

For any polynomial or power function combination:

1. **Rewrite** roots as fractional exponents
2. **Rewrite** fractions with $x$ in denominator as negative exponents
3. **Apply** power rule term by term
4. **Simplify** if needed

### Example 8: Full Walkthrough

**Differentiate $f(x) = \frac{4}{x^3} - \frac{2}{\sqrt{x}} + 3x^2 - 7$**

**Step 1: Rewrite**
$$f(x) = 4x^{-3} - 2x^{-1/2} + 3x^2 - 7$$

**Step 2: Differentiate each term**
$$f'(x) = 4(-3)x^{-4} - 2\left(-\frac{1}{2}\right)x^{-3/2} + 3(2)x^1 - 0$$

**Step 3: Simplify**
$$f'(x) = -12x^{-4} + x^{-3/2} + 6x$$
$$= -\frac{12}{x^4} + \frac{1}{x^{3/2}} + 6x$$
$$= -\frac{12}{x^4} + \frac{1}{\sqrt{x^3}} + 6x$$

---

## Rule 5: Derivatives of Exponential Functions

### The Natural Exponential Function

$$\boxed{\frac{d}{dx}[e^x] = e^x}$$

The function $e^x$ is its own derivative! This is one of the most remarkable facts in calculus.

### Why $e$?

The number $e \approx 2.71828...$ is the unique base for which $\frac{d}{dx}[a^x] = a^x$. For any other base, a constant factor appears.

### General Exponential Functions

$$\boxed{\frac{d}{dx}[a^x] = a^x \ln a}$$

where $a > 0$, $a \neq 1$.

**Special cases:**
- $\frac{d}{dx}[2^x] = 2^x \ln 2$
- $\frac{d}{dx}[10^x] = 10^x \ln 10$
- $\frac{d}{dx}[e^x] = e^x \ln e = e^x \cdot 1 = e^x$ ✓

### Examples

**Example 9:** Differentiate $f(x) = 5e^x$

$$f'(x) = 5e^x$$

---

**Example 10:** Differentiate $g(x) = 3 \cdot 2^x$

$$g'(x) = 3 \cdot 2^x \ln 2$$

---

**Example 11:** Differentiate $h(x) = e^x + x^e$

$$h'(x) = e^x + ex^{e-1}$$

Note: $x^e$ uses the power rule (constant exponent), while $e^x$ uses the exponential rule (constant base).

---

## Rule 6: Derivatives of Logarithmic Functions

### Natural Logarithm

$$\boxed{\frac{d}{dx}[\ln x] = \frac{1}{x}}$$

### General Logarithm

$$\boxed{\frac{d}{dx}[\log_a x] = \frac{1}{x \ln a}}$$

### Examples

**Example 12:** Differentiate $f(x) = 4\ln x$

$$f'(x) = \frac{4}{x}$$

---

**Example 13:** Differentiate $g(x) = \log_{10} x$

$$g'(x) = \frac{1}{x \ln 10}$$

---

**Example 14:** Differentiate $h(x) = x^2 + 3\ln x - e^x$

$$h'(x) = 2x + \frac{3}{x} - e^x$$

---

## Rule 7: Derivatives of Sine and Cosine

### The Basic Trig Derivatives

$$\boxed{\frac{d}{dx}[\sin x] = \cos x}$$

$$\boxed{\frac{d}{dx}[\cos x] = -\sin x}$$

### Memory Device

Think of a cycle: $\sin \to \cos \to -\sin \to -\cos \to \sin \to \cdots$

```
     sin x
      ↓ differentiate
     cos x
      ↓ differentiate
    -sin x
      ↓ differentiate
    -cos x
      ↓ differentiate
     sin x (back to start)
```

### Why the Negative Sign?

Looking at the graphs:
- When $\sin x$ is at its maximum, it's momentarily flat (slope 0). At that point, $\cos x = 0$. ✓
- When $\cos x$ is at its maximum, $\sin x$ is about to decrease, so the derivative should be negative.

### Examples

**Example 15:** Differentiate $f(x) = 3\sin x + 2\cos x$

$$f'(x) = 3\cos x - 2\sin x$$

---

**Example 16:** Differentiate $g(x) = x^2 - 5\sin x$

$$g'(x) = 2x - 5\cos x$$

---

**Example 17:** Differentiate $h(x) = \sin x + e^x - \ln x$

$$h'(x) = \cos x + e^x - \frac{1}{x}$$

---

## Summary of Basic Derivative Rules

| Function $f(x)$ | Derivative $f'(x)$ |
|-----------------|-------------------|
| $c$ (constant) | $0$ |
| $x^n$ | $nx^{n-1}$ |
| $e^x$ | $e^x$ |
| $a^x$ | $a^x \ln a$ |
| $\ln x$ | $\frac{1}{x}$ |
| $\log_a x$ | $\frac{1}{x \ln a}$ |
| $\sin x$ | $\cos x$ |
| $\cos x$ | $-\sin x$ |

**Combination rules:**
- $(cf)' = cf'$ (constant multiple)
- $(f + g)' = f' + g'$ (sum)
- $(f - g)' = f' - g'$ (difference)

---

## Common Mistakes to Avoid

### Mistake 1: Forgetting to Rewrite Before Differentiating

**Wrong:** $\frac{d}{dx}\left[\frac{1}{x^2}\right] = \frac{0}{2x} = 0$ ✗

**Right:** $\frac{d}{dx}[x^{-2}] = -2x^{-3} = -\frac{2}{x^3}$ ✓

### Mistake 2: Confusing Power Rule and Exponential Rule

**$x^5$** → Power rule: $5x^4$ (variable base, constant exponent)

**$5^x$** → Exponential rule: $5^x \ln 5$ (constant base, variable exponent)

### Mistake 3: Wrong Sign for Cosine

**Wrong:** $\frac{d}{dx}[\cos x] = \sin x$ ✗

**Right:** $\frac{d}{dx}[\cos x] = -\sin x$ ✓

### Mistake 4: Treating $e$ as a Variable

**Wrong:** $\frac{d}{dx}[e^3] = 3e^2$ ✗

**Right:** $\frac{d}{dx}[e^3] = 0$ (it's a constant!) ✓

### Mistake 5: Misapplying the Power Rule to Exponentials

**Wrong:** $\frac{d}{dx}[e^x] = xe^{x-1}$ ✗

**Right:** $\frac{d}{dx}[e^x] = e^x$ ✓

---

## Worked Examples

### Example 18: Polynomial

**Differentiate $f(x) = 3x^5 - 2x^3 + 7x - 4$**

$$f'(x) = 15x^4 - 6x^2 + 7$$

---

### Example 19: Mixed Radicals and Powers

**Differentiate $g(x) = \sqrt{x} - \frac{1}{\sqrt{x}} + x^3$**

Rewrite: $g(x) = x^{1/2} - x^{-1/2} + x^3$

$$g'(x) = \frac{1}{2}x^{-1/2} - \left(-\frac{1}{2}\right)x^{-3/2} + 3x^2$$
$$= \frac{1}{2\sqrt{x}} + \frac{1}{2x^{3/2}} + 3x^2$$

---

### Example 20: Exponential and Polynomial

**Differentiate $h(x) = e^x - x^e + e$**

- $\frac{d}{dx}[e^x] = e^x$
- $\frac{d}{dx}[x^e] = ex^{e-1}$ (power rule, $e$ is constant)
- $\frac{d}{dx}[e] = 0$ (constant)

$$h'(x) = e^x - ex^{e-1}$$

---

### Example 21: Logarithmic and Trigonometric

**Differentiate $f(x) = 2\ln x + 3\cos x$**

$$f'(x) = \frac{2}{x} - 3\sin x$$

---

### Example 22: Finding a Specific Derivative Value

**If $f(x) = x^4 - 2x^2 + \sin x$, find $f'(\pi)$.**

$$f'(x) = 4x^3 - 4x + \cos x$$
$$f'(\pi) = 4\pi^3 - 4\pi + \cos\pi = 4\pi^3 - 4\pi - 1$$

---

### Example 23: Writing a Tangent Line

**Find the tangent line to $y = e^x + x^2$ at $x = 0$.**

**Point:** $y(0) = e^0 + 0 = 1$, so $(0, 1)$

**Slope:** $y' = e^x + 2x$, so $y'(0) = 1 + 0 = 1$

**Tangent:** $y - 1 = 1(x - 0) \Rightarrow y = x + 1$

---

### Example 24: Horizontal Tangent

**Find all $x$ where $f(x) = x^3 - 6x^2 + 9x + 1$ has a horizontal tangent.**

$$f'(x) = 3x^2 - 12x + 9 = 3(x^2 - 4x + 3) = 3(x-1)(x-3)$$

$f'(x) = 0$ when $x = 1$ or $x = 3$

---

### Example 25: Second Derivative

**Find $f''(x)$ for $f(x) = x^5 - 3x^3 + 2x$**

$$f'(x) = 5x^4 - 9x^2 + 2$$
$$f''(x) = 20x^3 - 18x$$

---

### Example 26: Equation of Normal Line

**Find the normal line to $y = \ln x$ at $x = e$.**

**Point:** $(e, \ln e) = (e, 1)$

**Tangent slope:** $y' = \frac{1}{x}$, so $y'(e) = \frac{1}{e}$

**Normal slope:** $-e$ (negative reciprocal)

**Normal line:** $y - 1 = -e(x - e)$
$$y = -ex + e^2 + 1$$

---

## Practice Problems

### Basic Problems (1-5)

**1.** Differentiate $f(x) = 7x^4 - 3x^2 + 5$.

---

**2.** Differentiate $g(x) = \frac{4}{x^2} + \frac{3}{x}$.

---

**3.** Differentiate $h(x) = \sqrt[3]{x} + \sqrt{x^5}$.

---

**4.** Differentiate $f(x) = 5e^x - 2\sin x$.

---

**5.** Differentiate $g(x) = 3\ln x + 4\cos x - 7$.

---

### Intermediate Problems (6-10)

**6.** Differentiate $f(x) = x^{2.5} - x^{-0.5} + \pi^2$.

---

**7.** Differentiate $g(x) = \frac{x^4 - 3x^2 + 1}{x^2}$.

---

**8.** Find $f'(1)$ for $f(x) = x^3 + 2\ln x - e^x$.

---

**9.** Find the equation of the tangent line to $y = \sin x + \cos x$ at $x = 0$.

---

**10.** Find all points where $y = x^4 - 8x^2$ has a horizontal tangent.

---

### Advanced Problems (11-15)

**11.** Differentiate $f(x) = \frac{\sqrt{x} + 1}{\sqrt{x}}$.

---

**12.** Find $f''(4)$ for $f(x) = x^{3/2} + \frac{6}{\sqrt{x}}$.

---

**13.** Find the equation of the normal line to $y = e^x$ at $x = 1$.

---

**14.** For what values of $x$ is the tangent to $y = x^3 - 3x^2$ parallel to the line $y = 9x + 5$?

---

**15.** Find constants $a$ and $b$ so that the tangent to $y = ax^2 + bx$ at $(1, 5)$ has slope 8.

---

### Challenge Problems (16-18)

**16.** If $f(x) = x^n$ and $f'(2) = 12$, find $n$.

---

**17.** Find all functions of the form $f(x) = ax^2 + bx + c$ such that $f(0) = 1$, $f'(0) = 2$, and $f''(0) = 6$.

---

**18.** The line $y = ax + b$ is tangent to both $y = x^2$ and $y = x^2 - 2x + 2$. Find $a$ and $b$.

---

## Solutions to Practice Problems

### Solution 1

$$f'(x) = 28x^3 - 6x$$

---

### Solution 2

Rewrite: $g(x) = 4x^{-2} + 3x^{-1}$

$$g'(x) = -8x^{-3} - 3x^{-2} = -\frac{8}{x^3} - \frac{3}{x^2}$$

---

### Solution 3

Rewrite: $h(x) = x^{1/3} + x^{5/2}$

$$h'(x) = \frac{1}{3}x^{-2/3} + \frac{5}{2}x^{3/2}$$
$$= \frac{1}{3x^{2/3}} + \frac{5x^{3/2}}{2} = \frac{1}{3\sqrt[3]{x^2}} + \frac{5\sqrt{x^3}}{2}$$

---

### Solution 4

$$f'(x) = 5e^x - 2\cos x$$

---

### Solution 5

$$g'(x) = \frac{3}{x} - 4\sin x$$

---

### Solution 6

$$f'(x) = 2.5x^{1.5} + 0.5x^{-1.5}$$
$$= \frac{5}{2}x^{3/2} + \frac{1}{2x^{3/2}}$$

Note: $\pi^2$ is a constant, so its derivative is 0.

---

### Solution 7

First simplify:
$$g(x) = \frac{x^4}{x^2} - \frac{3x^2}{x^2} + \frac{1}{x^2} = x^2 - 3 + x^{-2}$$

$$g'(x) = 2x - 2x^{-3} = 2x - \frac{2}{x^3}$$

---

### Solution 8

$$f'(x) = 3x^2 + \frac{2}{x} - e^x$$
$$f'(1) = 3(1) + 2 - e = 5 - e$$

---

### Solution 9

Point: $y(0) = \sin 0 + \cos 0 = 0 + 1 = 1$, so $(0, 1)$

Slope: $y' = \cos x - \sin x$, so $y'(0) = 1 - 0 = 1$

Tangent: $y - 1 = 1(x - 0) \Rightarrow y = x + 1$

---

### Solution 10

$$y' = 4x^3 - 16x = 4x(x^2 - 4) = 4x(x-2)(x+2)$$

$y' = 0$ when $x = 0, 2, -2$

Points:
- $(0, 0)$
- $(2, 16 - 32) = (2, -16)$
- $(-2, -16)$

**Horizontal tangents at $(0, 0)$, $(2, -16)$, $(-2, -16)$**

---

### Solution 11

Simplify first:
$$f(x) = \frac{\sqrt{x}}{\sqrt{x}} + \frac{1}{\sqrt{x}} = 1 + x^{-1/2}$$

$$f'(x) = 0 - \frac{1}{2}x^{-3/2} = -\frac{1}{2x^{3/2}}$$

---

### Solution 12

$$f(x) = x^{3/2} + 6x^{-1/2}$$
$$f'(x) = \frac{3}{2}x^{1/2} - 3x^{-3/2}$$
$$f''(x) = \frac{3}{4}x^{-1/2} + \frac{9}{2}x^{-5/2}$$

$$f''(4) = \frac{3}{4}(4)^{-1/2} + \frac{9}{2}(4)^{-5/2}$$
$$= \frac{3}{4} \cdot \frac{1}{2} + \frac{9}{2} \cdot \frac{1}{32}$$
$$= \frac{3}{8} + \frac{9}{64} = \frac{24 + 9}{64} = \frac{33}{64}$$

---

### Solution 13

Point: $(1, e)$

Tangent slope: $y' = e^x$, so $y'(1) = e$

Normal slope: $-\frac{1}{e}$

Normal: $y - e = -\frac{1}{e}(x - 1)$
$$y = -\frac{x}{e} + \frac{1}{e} + e = -\frac{x}{e} + \frac{1 + e^2}{e}$$

---

### Solution 14

The line $y = 9x + 5$ has slope 9.

$$y' = 3x^2 - 6x$$

Set $3x^2 - 6x = 9$:
$$x^2 - 2x - 3 = 0$$
$$(x-3)(x+1) = 0$$
$$x = 3 \text{ or } x = -1$$

---

### Solution 15

The point $(1, 5)$ is on the curve:
$$5 = a(1)^2 + b(1) = a + b \quad \text{...(1)}$$

The slope at $x = 1$ is 8:
$$y' = 2ax + b$$
$$8 = 2a(1) + b = 2a + b \quad \text{...(2)}$$

Subtract (1) from (2): $3 = a$

From (1): $b = 5 - 3 = 2$

**Answer:** $a = 3$, $b = 2$

---

### Solution 16

$$f(x) = x^n, \quad f'(x) = nx^{n-1}$$
$$f'(2) = n \cdot 2^{n-1} = 12$$

Try $n = 3$: $3 \cdot 2^2 = 12$ ✓

**Answer:** $n = 3$

---

### Solution 17

$$f(x) = ax^2 + bx + c$$
$$f'(x) = 2ax + b$$
$$f''(x) = 2a$$

Given:
- $f(0) = c = 1$
- $f'(0) = b = 2$
- $f''(0) = 2a = 6 \Rightarrow a = 3$

**Answer:** $f(x) = 3x^2 + 2x + 1$

---

### Solution 18

For tangency to $y = x^2$ at $(t, t^2)$:
- Slope: $2t$
- Line: $y = 2t(x - t) + t^2 = 2tx - t^2$

So $a = 2t$ and $b = -t^2$.

For tangency to $y = x^2 - 2x + 2$ at $(s, s^2 - 2s + 2)$:
- Slope: $2s - 2$
- Line: $y = (2s-2)(x - s) + s^2 - 2s + 2$
- $= (2s-2)x - 2s^2 + 2s + s^2 - 2s + 2 = (2s-2)x - s^2 + 2$

So $a = 2s - 2$ and $b = -s^2 + 2$.

Equating:
$2t = 2s - 2 \Rightarrow t = s - 1$
$-t^2 = -s^2 + 2$
$t^2 = s^2 - 2$
$(s-1)^2 = s^2 - 2$
$s^2 - 2s + 1 = s^2 - 2$
$-2s = -3$
$s = \frac{3}{2}$, $t = \frac{1}{2}$

$a = 2(\frac{1}{2}) = 1$
$b = -(\frac{1}{2})^2 = -\frac{1}{4}$

**Answer:** $a = 1$, $b = -\frac{1}{4}$

---

## AP Exam Tips

### Speed Matters

On the AP exam, you need to differentiate quickly and accurately. Practice until these rules are automatic:

- See $x^5$ → immediately think $5x^4$
- See $\sin x$ → immediately think $\cos x$
- See $e^x$ → immediately think $e^x$

### Common AP Question Types

1. **Find $f'(c)$:** Differentiate, then substitute
2. **Find tangent line:** Need both $f(a)$ and $f'(a)$
3. **Find where tangent is horizontal:** Solve $f'(x) = 0$
4. **Match function to derivative graph:** Know that $f' > 0$ means $f$ increasing

### Watch For These Traps

- $\frac{d}{dx}[e^5] = 0$ (not $5e^4$!) — it's a constant
- $\frac{d}{dx}[\ln 3] = 0$ — also a constant
- $\frac{d}{dx}[x^{\pi}] = \pi x^{\pi - 1}$ — power rule, not exponential

---

## Summary

**The Essential Rules:**

| Rule | Formula |
|------|---------|
| Constant | $\frac{d}{dx}[c] = 0$ |
| Power | $\frac{d}{dx}[x^n] = nx^{n-1}$ |
| Constant Multiple | $\frac{d}{dx}[cf] = cf'$ |
| Sum | $\frac{d}{dx}[f+g] = f' + g'$ |
| Exponential | $\frac{d}{dx}[e^x] = e^x$ |
| General Exponential | $\frac{d}{dx}[a^x] = a^x \ln a$ |
| Natural Log | $\frac{d}{dx}[\ln x] = \frac{1}{x}$ |
| Sine | $\frac{d}{dx}[\sin x] = \cos x$ |
| Cosine | $\frac{d}{dx}[\cos x] = -\sin x$ |

**Key Techniques:**
1. Rewrite roots as fractional powers: $\sqrt{x} = x^{1/2}$
2. Rewrite fractions as negative powers: $\frac{1}{x^3} = x^{-3}$
3. Simplify before differentiating when possible
4. Differentiate term by term

These rules are the foundation for all derivative calculations. Master them, and you'll be ready for the product rule, quotient rule, and chain rule!

---

<div align="center">

[← Tangent Lines](calculus/tangent-lines.md) | [Product Rule →](calculus/product-rule.md)

</div>
