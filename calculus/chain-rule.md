# The Chain Rule

## Learning Objectives

By the end of this article, you will be able to:

- Recognize composite functions that require the chain rule
- Apply the chain rule using the "outside-inside" method
- Use Leibniz notation to understand why the chain rule works
- Differentiate functions with nested compositions
- Combine the chain rule with product and quotient rules
- Apply the generalized power rule
- Avoid common chain rule errors
- Solve AP Calculus problems involving composite functions

---

## The Core Concept: Functions Inside Functions

### What Is a Composite Function?

A **composite function** is a function inside another function. We write $f(g(x))$ or $(f \circ g)(x)$.

**Examples:**
- $\sin(x^2)$ — sine of $x^2$ (not $\sin x$ times $x$)
- $(3x + 1)^5$ — a linear function raised to the 5th power
- $e^{\cos x}$ — $e$ to the power of $\cos x$
- $\ln(\sin x)$ — natural log of $\sin x$

In each case, there's an **outer function** and an **inner function**:

| Expression | Outer Function | Inner Function |
|------------|----------------|----------------|
| $\sin(x^2)$ | $\sin(\square)$ | $x^2$ |
| $(3x + 1)^5$ | $(\square)^5$ | $3x + 1$ |
| $e^{\cos x}$ | $e^{\square}$ | $\cos x$ |
| $\ln(\sin x)$ | $\ln(\square)$ | $\sin x$ |

### Why Previous Rules Fail

None of our previous rules handle these:

- **Power rule:** Works for $x^5$, but not $(3x + 1)^5$
- **Exponential rule:** Works for $e^x$, but not $e^{\cos x}$
- **Trig rules:** Work for $\sin x$, but not $\sin(x^2)$

We need a new rule: the **chain rule**.

---

## The Chain Rule

### Statement

If $y = f(g(x))$, then:

$$\boxed{\frac{dy}{dx} = f'(g(x)) \cdot g'(x)}$$

**In words:** "Derivative of the outer (evaluated at the inner) times derivative of the inner."

### Alternative Notations

**Leibniz notation:** If $y = f(u)$ where $u = g(x)$:

$$\boxed{\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx}}$$

This looks like fractions canceling! (They're not really fractions, but this memory trick works.)

**Prime notation:**

$$[f(g(x))]' = f'(g(x)) \cdot g'(x)$$

### The "Outside-Inside" Method

1. **Identify** the outer and inner functions
2. **Differentiate** the outer function (leave the inner alone)
3. **Multiply** by the derivative of the inner function

---

## Intuition: Why Rates Multiply

### The Chain of Effects

Imagine a chain of cause and effect:

- $x$ changes → $u = g(x)$ changes → $y = f(u)$ changes

If $u$ changes 3 times as fast as $x$, and $y$ changes 2 times as fast as $u$, then $y$ changes $3 \times 2 = 6$ times as fast as $x$.

**Rates multiply through a chain!**

### Real-World Example

Suppose:
- Your car burns fuel at 0.05 gallons per mile ($\frac{du}{dx}$)
- Fuel costs \$4 per gallon ($\frac{dy}{du}$)

Then your cost changes at:
$$\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx} = 4 \times 0.05 = 0.20 \text{ dollars per mile}$$

---

## Applying the Chain Rule

### Step-by-Step Process

1. **Identify** the outer function $f$ and inner function $g$
2. **Find** $f'$ (the derivative of the outer)
3. **Evaluate** $f'$ at $g(x)$ (plug the inner function back in)
4. **Multiply** by $g'(x)$ (the derivative of the inner)

### Example 1: Power of a Linear Function

**Differentiate $y = (3x + 1)^5$**

**Solution:**

**Step 1:** Identify functions
- Outer: $f(u) = u^5$
- Inner: $g(x) = 3x + 1$

**Step 2:** Find derivatives
- $f'(u) = 5u^4$
- $g'(x) = 3$

**Step 3:** Apply chain rule
$$\frac{dy}{dx} = f'(g(x)) \cdot g'(x) = 5(3x + 1)^4 \cdot 3 = 15(3x + 1)^4$$

**Answer:** $\frac{dy}{dx} = 15(3x + 1)^4$

---

### Example 2: Sine of a Polynomial

**Differentiate $y = \sin(x^2)$**

**Solution:**

- Outer: $\sin(\square)$, derivative: $\cos(\square)$
- Inner: $x^2$, derivative: $2x$

$$\frac{dy}{dx} = \cos(x^2) \cdot 2x = 2x\cos(x^2)$$

**Answer:** $\frac{dy}{dx} = 2x\cos(x^2)$

---

### Example 3: Exponential of Trig

**Differentiate $y = e^{\sin x}$**

**Solution:**

- Outer: $e^{\square}$, derivative: $e^{\square}$
- Inner: $\sin x$, derivative: $\cos x$

$$\frac{dy}{dx} = e^{\sin x} \cdot \cos x$$

**Answer:** $\frac{dy}{dx} = e^{\sin x} \cos x$

---

### Example 4: Log of a Polynomial

**Differentiate $y = \ln(x^2 + 1)$**

**Solution:**

- Outer: $\ln(\square)$, derivative: $\frac{1}{\square}$
- Inner: $x^2 + 1$, derivative: $2x$

$$\frac{dy}{dx} = \frac{1}{x^2 + 1} \cdot 2x = \frac{2x}{x^2 + 1}$$

**Answer:** $\frac{dy}{dx} = \frac{2x}{x^2 + 1}$

---

### Example 5: Square Root (Fractional Power)

**Differentiate $y = \sqrt{4x - 3}$**

**Solution:**

Rewrite: $y = (4x - 3)^{1/2}$

- Outer: $(\square)^{1/2}$, derivative: $\frac{1}{2}(\square)^{-1/2}$
- Inner: $4x - 3$, derivative: $4$

$$\frac{dy}{dx} = \frac{1}{2}(4x - 3)^{-1/2} \cdot 4 = \frac{2}{\sqrt{4x - 3}}$$

**Answer:** $\frac{dy}{dx} = \frac{2}{\sqrt{4x - 3}}$

---

## The Generalized Power Rule

### A Special Case of the Chain Rule

For $y = [g(x)]^n$:

$$\boxed{\frac{d}{dx}[g(x)]^n = n[g(x)]^{n-1} \cdot g'(x)}$$

This is the chain rule applied to the power function.

### Examples

| Function | Derivative |
|----------|------------|
| $(x^2 + 1)^3$ | $3(x^2 + 1)^2 \cdot 2x = 6x(x^2 + 1)^2$ |
| $(5x - 2)^4$ | $4(5x - 2)^3 \cdot 5 = 20(5x - 2)^3$ |
| $\frac{1}{(x + 1)^2} = (x+1)^{-2}$ | $-2(x + 1)^{-3} \cdot 1 = \frac{-2}{(x+1)^3}$ |
| $\sqrt{x^3 + 5} = (x^3 + 5)^{1/2}$ | $\frac{1}{2}(x^3 + 5)^{-1/2} \cdot 3x^2 = \frac{3x^2}{2\sqrt{x^3 + 5}}$ |

---

## Common Chain Rule Patterns

### Pattern 1: Trig Functions with Inner Function

$$\frac{d}{dx}[\sin(g(x))] = \cos(g(x)) \cdot g'(x)$$

$$\frac{d}{dx}[\cos(g(x))] = -\sin(g(x)) \cdot g'(x)$$

$$\frac{d}{dx}[\tan(g(x))] = \sec^2(g(x)) \cdot g'(x)$$

**Example 6:** $\frac{d}{dx}[\cos(3x)] = -\sin(3x) \cdot 3 = -3\sin(3x)$

**Example 7:** $\frac{d}{dx}[\tan(x^2)] = \sec^2(x^2) \cdot 2x = 2x\sec^2(x^2)$

---

### Pattern 2: Exponential with Inner Function

$$\frac{d}{dx}[e^{g(x)}] = e^{g(x)} \cdot g'(x)$$

$$\frac{d}{dx}[a^{g(x)}] = a^{g(x)} \ln a \cdot g'(x)$$

**Example 8:** $\frac{d}{dx}[e^{5x}] = e^{5x} \cdot 5 = 5e^{5x}$

**Example 9:** $\frac{d}{dx}[e^{x^2}] = e^{x^2} \cdot 2x = 2xe^{x^2}$

**Example 10:** $\frac{d}{dx}[2^{3x}] = 2^{3x} \cdot \ln 2 \cdot 3 = 3(\ln 2)2^{3x}$

---

### Pattern 3: Logarithm with Inner Function

$$\frac{d}{dx}[\ln(g(x))] = \frac{g'(x)}{g(x)}$$

This is incredibly useful! The derivative of $\ln(\text{something})$ is $\frac{\text{derivative of something}}{\text{something}}$.

**Example 11:** $\frac{d}{dx}[\ln(x^3)] = \frac{3x^2}{x^3} = \frac{3}{x}$

**Example 12:** $\frac{d}{dx}[\ln(\sin x)] = \frac{\cos x}{\sin x} = \cot x$

**Example 13:** $\frac{d}{dx}[\ln(e^x + 1)] = \frac{e^x}{e^x + 1}$

---

## Multiple Chain Rules (Nested Functions)

### When Functions Are Deeply Nested

For $y = f(g(h(x)))$, apply the chain rule from outside to inside:

$$\frac{dy}{dx} = f'(g(h(x))) \cdot g'(h(x)) \cdot h'(x)$$

**Think of it as:** Derivative of the outermost, times derivative of the next layer, times derivative of the innermost.

### Example 14: Three Layers

**Differentiate $y = \sin(\cos(x^2))$**

**Solution:**

Layers from outside to inside:
1. Outer: $\sin(\square)$
2. Middle: $\cos(\square)$
3. Inner: $x^2$

$$\frac{dy}{dx} = \cos(\cos(x^2)) \cdot (-\sin(x^2)) \cdot 2x$$

$$= -2x\sin(x^2)\cos(\cos(x^2))$$

**Answer:** $\frac{dy}{dx} = -2x\sin(x^2)\cos(\cos(x^2))$

---

### Example 15: Exponential of Exponential

**Differentiate $y = e^{e^x}$**

**Solution:**

- Outer: $e^{\square}$, derivative: $e^{\square}$
- Inner: $e^x$, derivative: $e^x$

$$\frac{dy}{dx} = e^{e^x} \cdot e^x = e^x \cdot e^{e^x}$$

**Answer:** $\frac{dy}{dx} = e^x \cdot e^{e^x}$ or $e^{x + e^x}$

---

### Example 16: Power of Trig of Linear

**Differentiate $y = [\sin(2x)]^3$**

**Solution:**

This has three layers:
1. Outer: $(\square)^3$
2. Middle: $\sin(\square)$
3. Inner: $2x$

$$\frac{dy}{dx} = 3[\sin(2x)]^2 \cdot \cos(2x) \cdot 2$$

$$= 6\sin^2(2x)\cos(2x)$$

**Answer:** $\frac{dy}{dx} = 6\sin^2(2x)\cos(2x)$

---

## Combining Chain Rule with Product/Quotient Rules

### Example 17: Product with Chain Rule

**Differentiate $y = x^2 \sin(3x)$**

**Solution:**

Use product rule: $(fg)' = f'g + fg'$

- $f = x^2$, $f' = 2x$
- $g = \sin(3x)$, $g' = \cos(3x) \cdot 3 = 3\cos(3x)$ (chain rule!)

$$\frac{dy}{dx} = 2x \cdot \sin(3x) + x^2 \cdot 3\cos(3x)$$

$$= 2x\sin(3x) + 3x^2\cos(3x)$$

**Answer:** $\frac{dy}{dx} = 2x\sin(3x) + 3x^2\cos(3x)$

---

### Example 18: Product of Two Composite Functions

**Differentiate $y = e^{2x}\cos(5x)$**

**Solution:**

- $f = e^{2x}$, $f' = 2e^{2x}$
- $g = \cos(5x)$, $g' = -5\sin(5x)$

$$\frac{dy}{dx} = 2e^{2x}\cos(5x) + e^{2x}(-5\sin(5x))$$

$$= e^{2x}[2\cos(5x) - 5\sin(5x)]$$

**Answer:** $\frac{dy}{dx} = e^{2x}[2\cos(5x) - 5\sin(5x)]$

---

### Example 19: Quotient with Chain Rule

**Differentiate $y = \frac{e^x}{\sqrt{x + 1}}$**

**Solution:**

Rewrite denominator: $\sqrt{x + 1} = (x + 1)^{1/2}$

Use quotient rule:
- $f = e^x$, $f' = e^x$
- $g = (x + 1)^{1/2}$, $g' = \frac{1}{2}(x + 1)^{-1/2} = \frac{1}{2\sqrt{x + 1}}$

$$\frac{dy}{dx} = \frac{e^x \cdot (x + 1)^{1/2} - e^x \cdot \frac{1}{2}(x + 1)^{-1/2}}{(x + 1)}$$

$$= \frac{e^x \sqrt{x + 1} - \frac{e^x}{2\sqrt{x + 1}}}{x + 1}$$

Factor out $\frac{e^x}{2\sqrt{x+1}}$:

$$= \frac{e^x}{2\sqrt{x+1}} \cdot \frac{2(x + 1) - 1}{x + 1} = \frac{e^x(2x + 1)}{2(x + 1)^{3/2}}$$

**Answer:** $\frac{dy}{dx} = \frac{e^x(2x + 1)}{2(x + 1)^{3/2}}$

---

### Example 20: Chain Rule Inside Quotient

**Differentiate $y = \frac{\sin(2x)}{x^2 + 1}$**

**Solution:**

- $f = \sin(2x)$, $f' = 2\cos(2x)$
- $g = x^2 + 1$, $g' = 2x$

$$\frac{dy}{dx} = \frac{2\cos(2x)(x^2 + 1) - \sin(2x)(2x)}{(x^2 + 1)^2}$$

$$= \frac{2(x^2 + 1)\cos(2x) - 2x\sin(2x)}{(x^2 + 1)^2}$$

**Answer:** $\frac{dy}{dx} = \frac{2(x^2 + 1)\cos(2x) - 2x\sin(2x)}{(x^2 + 1)^2}$

---

## Special Applications

### Derivative of $a^x$ Revisited

Using chain rule with $a^x = e^{x \ln a}$:

$$\frac{d}{dx}[a^x] = \frac{d}{dx}[e^{x \ln a}] = e^{x \ln a} \cdot \ln a = a^x \ln a$$

---

### Example 21: Logarithmic Differentiation Preview

**Differentiate $y = x^x$ (for $x > 0$)**

**Solution:**

This is tricky: the base AND exponent contain $x$!

Take the natural log of both sides:
$$\ln y = \ln(x^x) = x \ln x$$

Differentiate implicitly:
$$\frac{1}{y} \cdot \frac{dy}{dx} = 1 \cdot \ln x + x \cdot \frac{1}{x} = \ln x + 1$$

Solve for $\frac{dy}{dx}$:
$$\frac{dy}{dx} = y(\ln x + 1) = x^x(\ln x + 1)$$

**Answer:** $\frac{dy}{dx} = x^x(\ln x + 1)$

---

### Example 22: Finding Tangent Lines

**Find the equation of the tangent line to $y = e^{-x^2}$ at $x = 1$.**

**Solution:**

**Point:** $y(1) = e^{-1} = \frac{1}{e}$

**Derivative:**
$$\frac{dy}{dx} = e^{-x^2} \cdot (-2x) = -2xe^{-x^2}$$

**Slope at $x = 1$:**
$$\frac{dy}{dx}\bigg|_{x=1} = -2(1)e^{-1} = -\frac{2}{e}$$

**Tangent line:**
$$y - \frac{1}{e} = -\frac{2}{e}(x - 1)$$

$$y = -\frac{2}{e}x + \frac{2}{e} + \frac{1}{e} = -\frac{2}{e}x + \frac{3}{e}$$

**Answer:** $y = -\frac{2}{e}x + \frac{3}{e}$ or $y = \frac{3 - 2x}{e}$

---

## Common Mistakes

### Mistake 1: Forgetting the Chain Rule Entirely

**Wrong:** $\frac{d}{dx}[\sin(3x)] = \cos(3x)$ ✗

**Right:** $\frac{d}{dx}[\sin(3x)] = \cos(3x) \cdot 3 = 3\cos(3x)$ ✓

### Mistake 2: Wrong Order of Operations

**Wrong:** $\frac{d}{dx}[(2x + 1)^4] = 4(2)^3 \cdot 2$ ✗

**Right:** $\frac{d}{dx}[(2x + 1)^4] = 4(2x + 1)^3 \cdot 2 = 8(2x + 1)^3$ ✓

Keep the inner function intact when applying the power rule!

### Mistake 3: Misidentifying the Inner Function

For $y = \sin^2 x = (\sin x)^2$:

**Wrong inner:** $x$ → Wrong answer

**Right inner:** $\sin x$

$$\frac{dy}{dx} = 2\sin x \cdot \cos x = 2\sin x \cos x = \sin(2x)$$

### Mistake 4: Stopping Too Early

For $y = \sqrt{\sin x}$:

**Wrong:** $\frac{dy}{dx} = \frac{1}{2\sqrt{\sin x}}$ (forgot inner derivative!) ✗

**Right:** $\frac{dy}{dx} = \frac{1}{2\sqrt{\sin x}} \cdot \cos x = \frac{\cos x}{2\sqrt{\sin x}}$ ✓

### Mistake 5: Confusing $\sin^2 x$ with $\sin(x^2)$

| Expression | Meaning | Derivative |
|------------|---------|------------|
| $\sin^2 x$ | $(\sin x)^2$ | $2\sin x \cos x$ |
| $\sin(x^2)$ | $\sin$ of $x^2$ | $2x\cos(x^2)$ |

These are completely different functions!

---

## Practice Problems

### Basic Problems (1-5)

**1.** Differentiate $f(x) = (2x - 5)^7$.

---

**2.** Differentiate $g(x) = \sin(4x)$.

---

**3.** Differentiate $h(x) = e^{3x}$.

---

**4.** Differentiate $f(x) = \ln(x^2 + 4)$.

---

**5.** Differentiate $g(x) = \sqrt{1 - x^2}$.

---

### Intermediate Problems (6-10)

**6.** Differentiate $f(x) = \cos^3(x)$.

---

**7.** Differentiate $g(x) = e^{\sin x}$.

---

**8.** Differentiate $h(x) = \ln(\cos x)$.

---

**9.** Differentiate $f(x) = \tan(x^2 + 1)$.

---

**10.** Differentiate $g(x) = (x^3 + 2x)^{-4}$.

---

### Advanced Problems (11-15)

**11.** Differentiate $f(x) = x^2 e^{-3x}$.

---

**12.** Differentiate $g(x) = \sin(e^x)$.

---

**13.** Differentiate $h(x) = \sqrt{\sin(2x)}$.

---

**14.** Find $f'(\pi)$ for $f(x) = \sin(\cos x)$.

---

**15.** Find the equation of the tangent line to $y = \ln(x^2)$ at $x = e$.

---

### Challenge Problems (16-18)

**16.** Differentiate $f(x) = e^{x\sin x}$.

---

**17.** If $f(x) = [g(x)]^3$ and $g(2) = 3$, $g'(2) = 4$, find $f'(2)$.

---

**18.** Find all values of $x$ in $[0, 2\pi]$ where $f(x) = e^{\sin x}$ has a horizontal tangent.

---

## Solutions to Practice Problems

### Solution 1

$$f'(x) = 7(2x - 5)^6 \cdot 2 = 14(2x - 5)^6$$

**Answer:** $f'(x) = 14(2x - 5)^6$

---

### Solution 2

$$g'(x) = \cos(4x) \cdot 4 = 4\cos(4x)$$

**Answer:** $g'(x) = 4\cos(4x)$

---

### Solution 3

$$h'(x) = e^{3x} \cdot 3 = 3e^{3x}$$

**Answer:** $h'(x) = 3e^{3x}$

---

### Solution 4

$$f'(x) = \frac{1}{x^2 + 4} \cdot 2x = \frac{2x}{x^2 + 4}$$

**Answer:** $f'(x) = \frac{2x}{x^2 + 4}$

---

### Solution 5

Rewrite: $g(x) = (1 - x^2)^{1/2}$

$$g'(x) = \frac{1}{2}(1 - x^2)^{-1/2} \cdot (-2x) = \frac{-x}{\sqrt{1 - x^2}}$$

**Answer:** $g'(x) = \frac{-x}{\sqrt{1 - x^2}}$

---

### Solution 6

$f(x) = (\cos x)^3$

$$f'(x) = 3(\cos x)^2 \cdot (-\sin x) = -3\cos^2 x \sin x$$

**Answer:** $f'(x) = -3\cos^2 x \sin x$

---

### Solution 7

$$g'(x) = e^{\sin x} \cdot \cos x$$

**Answer:** $g'(x) = e^{\sin x} \cos x$

---

### Solution 8

$$h'(x) = \frac{1}{\cos x} \cdot (-\sin x) = \frac{-\sin x}{\cos x} = -\tan x$$

**Answer:** $h'(x) = -\tan x$

---

### Solution 9

$$f'(x) = \sec^2(x^2 + 1) \cdot 2x = 2x\sec^2(x^2 + 1)$$

**Answer:** $f'(x) = 2x\sec^2(x^2 + 1)$

---

### Solution 10

$$g'(x) = -4(x^3 + 2x)^{-5} \cdot (3x^2 + 2) = \frac{-4(3x^2 + 2)}{(x^3 + 2x)^5}$$

**Answer:** $g'(x) = \frac{-4(3x^2 + 2)}{(x^3 + 2x)^5}$

---

### Solution 11

Use product rule:
- $f = x^2$, $f' = 2x$
- $g = e^{-3x}$, $g' = -3e^{-3x}$

$$f'(x) = 2x \cdot e^{-3x} + x^2 \cdot (-3e^{-3x})$$
$$= e^{-3x}(2x - 3x^2) = xe^{-3x}(2 - 3x)$$

**Answer:** $f'(x) = xe^{-3x}(2 - 3x)$

---

### Solution 12

Two chain rules:
- Outer: $\sin(\square)$
- Inner: $e^x$

$$g'(x) = \cos(e^x) \cdot e^x = e^x \cos(e^x)$$

**Answer:** $g'(x) = e^x \cos(e^x)$

---

### Solution 13

$h(x) = [\sin(2x)]^{1/2}$

Three layers: power, then sine, then $2x$

$$h'(x) = \frac{1}{2}[\sin(2x)]^{-1/2} \cdot \cos(2x) \cdot 2$$

$$= \frac{\cos(2x)}{\sqrt{\sin(2x)}}$$

**Answer:** $h'(x) = \frac{\cos(2x)}{\sqrt{\sin(2x)}}$

---

### Solution 14

$$f'(x) = \cos(\cos x) \cdot (-\sin x) = -\sin x \cos(\cos x)$$

$$f'(\pi) = -\sin\pi \cdot \cos(\cos\pi) = 0 \cdot \cos(-1) = 0$$

**Answer:** $f'(\pi) = 0$

---

### Solution 15

$y = \ln(x^2) = 2\ln x$

Point: At $x = e$, $y = 2\ln e = 2$, so $(e, 2)$

Derivative: $y' = \frac{2}{x}$, so $y'(e) = \frac{2}{e}$

Tangent: $y - 2 = \frac{2}{e}(x - e)$

$$y = \frac{2}{e}x - 2 + 2 = \frac{2x}{e}$$

**Answer:** $y = \frac{2x}{e}$

---

### Solution 16

The exponent $x\sin x$ requires product rule:

$$\frac{d}{dx}[x\sin x] = \sin x + x\cos x$$

So:
$$f'(x) = e^{x\sin x} \cdot (\sin x + x\cos x)$$

**Answer:** $f'(x) = e^{x\sin x}(\sin x + x\cos x)$

---

### Solution 17

$$f'(x) = 3[g(x)]^2 \cdot g'(x)$$

$$f'(2) = 3[g(2)]^2 \cdot g'(2) = 3(3)^2(4) = 3(9)(4) = 108$$

**Answer:** $f'(2) = 108$

---

### Solution 18

$$f'(x) = e^{\sin x} \cdot \cos x$$

$f'(x) = 0$ when $\cos x = 0$ (since $e^{\sin x} > 0$ always)

In $[0, 2\pi]$: $\cos x = 0$ at $x = \frac{\pi}{2}, \frac{3\pi}{2}$

**Answer:** $x = \frac{\pi}{2}$ and $x = \frac{3\pi}{2}$

---

## AP Exam Tips

### Recognizing Chain Rule Problems

Look for:
- Parentheses with something other than just $x$ inside
- Powers of expressions: $(...)^n$
- Trig functions of expressions: $\sin(...), \cos(...)$
- Exponentials with non-$x$ exponents: $e^{...}$
- Logarithms of expressions: $\ln(...)$

### Speed Tips

1. **Practice patterns:** Know that $\frac{d}{dx}[e^{3x}] = 3e^{3x}$ instantly
2. **Identify layers first:** Before computing, list outer → inner
3. **Don't simplify mid-computation:** Apply rules first, simplify at the end

### Common FRQ Patterns

1. **Composite functions from tables:** Given $f(1) = 2$, $f'(1) = 3$, $g(2) = 1$, $g'(2) = 4$, find $(f \circ g)'(2)$

   Solution: $(f \circ g)'(2) = f'(g(2)) \cdot g'(2) = f'(1) \cdot 4 = 3 \cdot 4 = 12$

2. **Related rates:** Often require chain rule for implicit relationships

3. **Tangent line to composite:** Find point, use chain rule for slope

### The "Onion" Visualization

Think of composite functions as layers of an onion:
- You peel from outside to inside
- Each layer contributes a factor to the derivative

$$f(g(h(x))) \rightarrow f'(\cdot) \cdot g'(\cdot) \cdot h'(x)$$

---

## Summary

**The Chain Rule:**
$$\frac{d}{dx}[f(g(x))] = f'(g(x)) \cdot g'(x)$$

**Leibniz Form:**
$$\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx}$$

**Generalized Power Rule:**
$$\frac{d}{dx}[g(x)]^n = n[g(x)]^{n-1} \cdot g'(x)$$

**Common Patterns:**

| Function | Derivative |
|----------|------------|
| $\sin(g(x))$ | $\cos(g(x)) \cdot g'(x)$ |
| $\cos(g(x))$ | $-\sin(g(x)) \cdot g'(x)$ |
| $e^{g(x)}$ | $e^{g(x)} \cdot g'(x)$ |
| $\ln(g(x))$ | $\frac{g'(x)}{g(x)}$ |
| $[g(x)]^n$ | $n[g(x)]^{n-1} \cdot g'(x)$ |

**Key Points:**
- Identify outer and inner functions first
- Differentiate outer, keep inner intact, then multiply by inner's derivative
- For nested functions, work from outside to inside
- Often combined with product/quotient rules
- Never forget the inner derivative!

The chain rule is essential for almost all derivative problems beyond basic functions. Master it, and you can differentiate nearly anything!

---

<div align="center">

[← Quotient Rule](calculus/quotient-rule.md) | [Implicit Differentiation →](calculus/implicit-differentiation.md)

</div>
