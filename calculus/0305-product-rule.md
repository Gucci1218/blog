# The Product Rule
<p class="article-date">December 24, 2024</p>

## Learning Objectives

By the end of this article, you will be able to:

- Understand why the derivative of a product requires a special rule
- Apply the product rule to differentiate products of functions
- Choose when to use the product rule versus simplifying first
- Extend the product rule to products of three or more functions
- Combine the product rule with other derivative rules
- Avoid common product rule mistakes
- Solve AP Calculus problems involving the product rule

---

## The Core Concept: Why Products Are Tricky

### A Tempting (But Wrong) Guess

You might think:

$$\frac{d}{dx}[f(x) \cdot g(x)] \stackrel{?}{=} f'(x) \cdot g'(x)$$

**This is FALSE!**

Let's test it with a simple example.

**Example:** Let $f(x) = x$ and $g(x) = x$, so $f(x) \cdot g(x) = x^2$.

**Wrong method:** $f'(x) \cdot g'(x) = 1 \cdot 1 = 1$

**Correct answer:** $\frac{d}{dx}[x^2] = 2x$

Clearly $1 \neq 2x$, so the naive guess is wrong!

### The Real Rule: Product Rule

$$\boxed{\frac{d}{dx}[f(x) \cdot g(x)] = f'(x) \cdot g(x) + f(x) \cdot g'(x)}$$

In words: "The derivative of the first times the second, plus the first times the derivative of the second."

### Alternative Notations

Using different notation:

$$\frac{d}{dx}[uv] = u'v + uv'$$

Or using Leibniz notation:

$$\frac{d(uv)}{dx} = \frac{du}{dx} \cdot v + u \cdot \frac{dv}{dx}$$

---

## Intuition: Why This Formula Makes Sense

### The Rectangle Analogy

Imagine a rectangle with width $f(x)$ and height $g(x)$. The area is $A = f(x) \cdot g(x)$.

```
         g(x)
    ┌──────────────┐
    │              │
f(x)│      A       │
    │              │
    └──────────────┘
```

Now suppose both dimensions are changing. How fast does the area change?

When $x$ changes by a tiny amount $\Delta x$:
- Width changes by $\Delta f \approx f'(x) \Delta x$
- Height changes by $\Delta g \approx g'(x) \Delta x$

The new area is approximately:

```
             g + Δg
    ┌────────────────────┐
    │          │    B    │
    │    A     │─────────│
f+Δf│          │         │
    │──────────│    C    │
    │          │         │
    └────────────────────┘
```

- Original area: $A = fg$
- New horizontal strip: $B = f \cdot \Delta g$
- New vertical strip: $C = \Delta f \cdot g$
- Corner (negligible): $\Delta f \cdot \Delta g \approx 0$

**Change in area:** $\Delta A \approx f \cdot \Delta g + g \cdot \Delta f$

**Rate of change:** $\frac{dA}{dx} = f \cdot g' + g \cdot f' = f'g + fg'$

---

## Proof of the Product Rule

### Using the Limit Definition

$$\frac{d}{dx}[f(x)g(x)] = \lim_{h \to 0} \frac{f(x+h)g(x+h) - f(x)g(x)}{h}$$

**The trick:** Add and subtract $f(x+h)g(x)$ in the numerator.

$$= \lim_{h \to 0} \frac{f(x+h)g(x+h) - f(x+h)g(x) + f(x+h)g(x) - f(x)g(x)}{h}$$

$$= \lim_{h \to 0} \frac{f(x+h)[g(x+h) - g(x)] + g(x)[f(x+h) - f(x)]}{h}$$

$$= \lim_{h \to 0} f(x+h) \cdot \frac{g(x+h) - g(x)}{h} + \lim_{h \to 0} g(x) \cdot \frac{f(x+h) - f(x)}{h}$$

$$= f(x) \cdot g'(x) + g(x) \cdot f'(x)$$

$$= f(x)g'(x) + f'(x)g(x) \quad \checkmark$$

---

## How to Apply the Product Rule

### Step-by-Step Process

1. **Identify** the two factors: $f(x)$ and $g(x)$
2. **Find** $f'(x)$ and $g'(x)$ separately
3. **Apply** the formula: $f'g + fg'$
4. **Simplify** if needed

### Memory Tricks

**"First d-second plus second d-first"**
- (First)(derivative of second) + (second)(derivative of first)
- $f \cdot g' + g \cdot f'$

**"Left d-right plus right d-left"**

**Song version:** "Low d-high minus high d-low" is for quotient rule—don't mix them up!

---

## Worked Examples

### Example 1: Basic Product

**Differentiate $f(x) = x^2 \cdot e^x$**

**Solution:**

Let $u = x^2$ and $v = e^x$

- $u' = 2x$
- $v' = e^x$

$$f'(x) = u'v + uv' = 2x \cdot e^x + x^2 \cdot e^x$$

Factor out $e^x$:
$$f'(x) = e^x(2x + x^2) = e^x \cdot x(2 + x)$$

**Answer:** $f'(x) = (x^2 + 2x)e^x$ or $xe^x(x + 2)$

---

### Example 2: Polynomial Times Trig

**Differentiate $g(x) = x^3 \sin x$**

**Solution:**

Let $u = x^3$ and $v = \sin x$

- $u' = 3x^2$
- $v' = \cos x$

$$g'(x) = 3x^2 \cdot \sin x + x^3 \cdot \cos x$$

**Answer:** $g'(x) = 3x^2 \sin x + x^3 \cos x$

---

### Example 3: Exponential Times Trig

**Differentiate $h(x) = e^x \cos x$**

**Solution:**

Let $u = e^x$ and $v = \cos x$

- $u' = e^x$
- $v' = -\sin x$

$$h'(x) = e^x \cdot \cos x + e^x \cdot (-\sin x)$$
$$= e^x \cos x - e^x \sin x$$
$$= e^x(\cos x - \sin x)$$

**Answer:** $h'(x) = e^x(\cos x - \sin x)$

---

### Example 4: Root Times Log

**Differentiate $f(x) = \sqrt{x} \cdot \ln x$**

**Solution:**

Let $u = \sqrt{x} = x^{1/2}$ and $v = \ln x$

- $u' = \frac{1}{2}x^{-1/2} = \frac{1}{2\sqrt{x}}$
- $v' = \frac{1}{x}$

$$f'(x) = \frac{1}{2\sqrt{x}} \cdot \ln x + \sqrt{x} \cdot \frac{1}{x}$$

$$= \frac{\ln x}{2\sqrt{x}} + \frac{\sqrt{x}}{x}$$

$$= \frac{\ln x}{2\sqrt{x}} + \frac{1}{\sqrt{x}}$$

$$= \frac{\ln x + 2}{2\sqrt{x}}$$

**Answer:** $f'(x) = \frac{\ln x + 2}{2\sqrt{x}}$

---

### Example 5: Two Polynomials

**Differentiate $f(x) = (x^2 + 1)(x^3 - 2x)$**

**Solution:**

**Method 1: Product Rule**

Let $u = x^2 + 1$ and $v = x^3 - 2x$

- $u' = 2x$
- $v' = 3x^2 - 2$

$$f'(x) = 2x(x^3 - 2x) + (x^2 + 1)(3x^2 - 2)$$
$$= 2x^4 - 4x^2 + 3x^4 - 2x^2 + 3x^2 - 2$$
$$= 5x^4 - 3x^2 - 2$$

**Method 2: Expand First (Alternative)**

$$f(x) = x^5 - 2x^3 + x^3 - 2x = x^5 - x^3 - 2x$$
$$f'(x) = 5x^4 - 3x^2 - 2$$

Both methods give the same answer! For polynomials, expanding first is often easier.

**Answer:** $f'(x) = 5x^4 - 3x^2 - 2$

---

### Example 6: Finding a Specific Value

**If $f(x) = x^2 e^x$, find $f'(0)$.**

**Solution:**

$$f'(x) = 2x \cdot e^x + x^2 \cdot e^x = e^x(2x + x^2)$$

$$f'(0) = e^0(0 + 0) = 1 \cdot 0 = 0$$

**Answer:** $f'(0) = 0$

---

### Example 7: Tangent Line Problem

**Find the equation of the tangent line to $y = x \sin x$ at $x = \pi$.**

**Solution:**

**Step 1: Find the point.**
$$y(\pi) = \pi \sin \pi = \pi \cdot 0 = 0$$
Point: $(\pi, 0)$

**Step 2: Find the slope.**
$$y' = 1 \cdot \sin x + x \cdot \cos x = \sin x + x \cos x$$
$$y'(\pi) = \sin \pi + \pi \cos \pi = 0 + \pi(-1) = -\pi$$

**Step 3: Write the tangent line.**
$$y - 0 = -\pi(x - \pi)$$
$$y = -\pi x + \pi^2$$

**Answer:** $y = -\pi x + \pi^2$

---

### Example 8: Second Derivative

**Find $f''(x)$ for $f(x) = x e^x$.**

**Solution:**

**First derivative:**
$$f'(x) = 1 \cdot e^x + x \cdot e^x = e^x + xe^x = e^x(1 + x)$$

**Second derivative:** (Apply product rule again to $e^x(1+x)$)
$$f''(x) = e^x \cdot (1 + x) + e^x \cdot 1 = e^x(1 + x) + e^x$$
$$= e^x(1 + x + 1) = e^x(2 + x)$$

**Answer:** $f''(x) = e^x(x + 2)$

---

## Product of Three or More Functions

### The Extended Product Rule

For three functions:

$$\frac{d}{dx}[fgh] = f'gh + fg'h + fgh'$$

**Pattern:** Each function gets differentiated once while the others stay the same, then add.

### Derivation

Think of $fgh$ as $(fg) \cdot h$:

$$\frac{d}{dx}[(fg)h] = (fg)'h + (fg)h'$$
$$= (f'g + fg')h + fgh'$$
$$= f'gh + fg'h + fgh'$$

### Example 9: Three Factors

**Differentiate $f(x) = x^2 e^x \sin x$**

**Solution:**

$$f'(x) = (x^2)' \cdot e^x \cdot \sin x + x^2 \cdot (e^x)' \cdot \sin x + x^2 \cdot e^x \cdot (\sin x)'$$

$$= 2x \cdot e^x \sin x + x^2 \cdot e^x \cdot \sin x + x^2 \cdot e^x \cdot \cos x$$

$$= e^x(2x \sin x + x^2 \sin x + x^2 \cos x)$$

$$= x e^x(2\sin x + x\sin x + x\cos x)$$

**Answer:** $f'(x) = xe^x(2\sin x + x\sin x + x\cos x)$

Or factored differently: $f'(x) = xe^x[(2+x)\sin x + x\cos x]$

---

## When NOT to Use the Product Rule

### Simplify First When Possible

Sometimes a "product" can be simplified before differentiating.

**Example 10:** Differentiate $f(x) = x^3 \cdot x^5$

**Bad approach:** Use product rule with $u = x^3$, $v = x^5$

**Good approach:** Simplify first: $f(x) = x^8$, so $f'(x) = 8x^7$

### When It's Really Just One Term

**Example 11:** Differentiate $f(x) = 5x^4$

This is NOT a product rule problem! It's just $5 \cdot x^4$ where 5 is a constant.

$$f'(x) = 5 \cdot 4x^3 = 20x^3$$

### When Expansion Is Easier

If both factors are polynomials, expanding might be faster than the product rule.

**Example 12:** Differentiate $(2x + 1)(x - 3)$

**Product rule:** $(2)(x-3) + (2x+1)(1) = 2x - 6 + 2x + 1 = 4x - 5$

**Expand first:** $2x^2 - 6x + x - 3 = 2x^2 - 5x - 3$, then differentiate: $4x - 5$

Both work, but with more complex products, the product rule is essential.

---

## Combining Product Rule with Other Rules

### Example 13: Product with Power Rule Preparation

**Differentiate $f(x) = (x^2 + 3x)\sqrt{x}$**

**Solution:**

Let $u = x^2 + 3x$ and $v = \sqrt{x} = x^{1/2}$

- $u' = 2x + 3$
- $v' = \frac{1}{2}x^{-1/2}$

$$f'(x) = (2x + 3) \cdot x^{1/2} + (x^2 + 3x) \cdot \frac{1}{2}x^{-1/2}$$

$$= (2x + 3)\sqrt{x} + \frac{x^2 + 3x}{2\sqrt{x}}$$

To combine, use common denominator $2\sqrt{x}$:

$$= \frac{2(2x + 3)\sqrt{x} \cdot \sqrt{x}}{2\sqrt{x}} + \frac{x^2 + 3x}{2\sqrt{x}}$$

$$= \frac{2(2x + 3)x + x^2 + 3x}{2\sqrt{x}} = \frac{4x^2 + 6x + x^2 + 3x}{2\sqrt{x}} = \frac{5x^2 + 9x}{2\sqrt{x}}$$

**Answer:** $f'(x) = \frac{5x^2 + 9x}{2\sqrt{x}} = \frac{x(5x + 9)}{2\sqrt{x}} = \frac{\sqrt{x}(5x + 9)}{2}$

---

### Example 14: With Trigonometric Functions

**Differentiate $f(x) = x^2 \cos x + x \sin x$**

**Solution:**

Differentiate term by term, applying the product rule to each:

**First term:** $\frac{d}{dx}[x^2 \cos x] = 2x \cos x + x^2(-\sin x) = 2x \cos x - x^2 \sin x$

**Second term:** $\frac{d}{dx}[x \sin x] = 1 \cdot \sin x + x \cos x = \sin x + x \cos x$

**Combine:**
$$f'(x) = 2x \cos x - x^2 \sin x + \sin x + x \cos x$$
$$= 3x \cos x - x^2 \sin x + \sin x$$
$$= (3x)\cos x + (1 - x^2)\sin x$$

**Answer:** $f'(x) = 3x \cos x + (1 - x^2) \sin x$

---

## Common Mistakes

### Mistake 1: Forgetting a Term

**Wrong:** $(x^2)' \cdot (e^x) = 2x e^x$ ✗

**Right:** $(x^2)' \cdot e^x + x^2 \cdot (e^x)' = 2xe^x + x^2 e^x$ ✓

### Mistake 2: Multiplying Derivatives

**Wrong:** $(x^2 \sin x)' = (2x)(\cos x) = 2x \cos x$ ✗

**Right:** $(x^2 \sin x)' = 2x \sin x + x^2 \cos x$ ✓

### Mistake 3: Using Product Rule for Constants

**Wrong:** Applying product rule to $3x^2$ as if it's $(3)(x^2)$

The constant multiple rule handles this: $(3x^2)' = 3 \cdot 2x = 6x$

### Mistake 4: Sign Errors with Cosine

Remember: $(\cos x)' = -\sin x$ (negative!)

**Wrong:** $(x \cos x)' = \cos x + x \sin x$ ✗

**Right:** $(x \cos x)' = \cos x + x(-\sin x) = \cos x - x \sin x$ ✓

---

## Practice Problems

### Basic Problems (1-5)

**1.** Differentiate $f(x) = x^4 e^x$.

---

**2.** Differentiate $g(x) = x^2 \sin x$.

---

**3.** Differentiate $h(x) = e^x \ln x$.

---

**4.** Differentiate $f(x) = \sqrt{x} \cos x$.

---

**5.** Find $f'(1)$ for $f(x) = x^3 \ln x$.

---

### Intermediate Problems (6-10)

**6.** Differentiate $f(x) = (x^2 + 1)e^x$.

---

**7.** Differentiate $g(x) = x^2 \sin x \cos x$.

---

**8.** Find the equation of the tangent line to $y = xe^x$ at $x = 0$.

---

**9.** Differentiate $h(x) = (3x - 1)(2x + 5)$ using the product rule. Verify by expanding first.

---

**10.** Find all $x$ where $f(x) = x^2 e^x$ has a horizontal tangent.

---

### Advanced Problems (11-15)

**11.** Find $f''(x)$ for $f(x) = x^2 \sin x$.

---

**12.** Differentiate $g(x) = x \ln x - x$.

---

**13.** If $f(x) = x^2 g(x)$, $g(2) = 3$, and $g'(2) = -1$, find $f'(2)$.

---

**14.** Find the equation of the normal line to $y = x \cos x$ at $x = \frac{\pi}{2}$.

---

**15.** Differentiate $f(x) = (x^2 + 1)(x^3 - 1)(x - 2)$.

---

### Challenge Problems (16-18)

**16.** If $h(x) = f(x) \cdot g(x)$, $f(3) = 2$, $f'(3) = -1$, $g(3) = 5$, $g'(3) = 4$, find $h'(3)$.

---

**17.** Find all functions $f(x)$ such that $f(x) \cdot f'(x) = x$ and $f(0) = 1$.

---

**18.** Prove that $\frac{d}{dx}[x^n e^x] = e^x(x^n + nx^{n-1})$ for positive integer $n$.

---

## Solutions to Practice Problems

### Solution 1

Let $u = x^4$, $v = e^x$. Then $u' = 4x^3$, $v' = e^x$.

$$f'(x) = 4x^3 e^x + x^4 e^x = e^x(4x^3 + x^4) = x^3 e^x(4 + x)$$

**Answer:** $f'(x) = x^3 e^x(x + 4)$

---

### Solution 2

$$g'(x) = 2x \sin x + x^2 \cos x$$

**Answer:** $g'(x) = 2x \sin x + x^2 \cos x$

---

### Solution 3

Let $u = e^x$, $v = \ln x$. Then $u' = e^x$, $v' = \frac{1}{x}$.

$$h'(x) = e^x \ln x + e^x \cdot \frac{1}{x} = e^x\left(\ln x + \frac{1}{x}\right)$$

**Answer:** $h'(x) = e^x\left(\ln x + \frac{1}{x}\right)$

---

### Solution 4

Let $u = x^{1/2}$, $v = \cos x$. Then $u' = \frac{1}{2}x^{-1/2}$, $v' = -\sin x$.

$$f'(x) = \frac{1}{2\sqrt{x}} \cos x + \sqrt{x}(-\sin x) = \frac{\cos x}{2\sqrt{x}} - \sqrt{x} \sin x$$

**Answer:** $f'(x) = \frac{\cos x}{2\sqrt{x}} - \sqrt{x} \sin x$

---

### Solution 5

$$f'(x) = 3x^2 \ln x + x^3 \cdot \frac{1}{x} = 3x^2 \ln x + x^2$$

$$f'(1) = 3(1)^2 \ln 1 + 1^2 = 3(0) + 1 = 1$$

**Answer:** $f'(1) = 1$

---

### Solution 6

$$f'(x) = 2x \cdot e^x + (x^2 + 1) \cdot e^x = e^x(2x + x^2 + 1) = e^x(x^2 + 2x + 1)$$
$$= e^x(x + 1)^2$$

**Answer:** $f'(x) = e^x(x + 1)^2$

---

### Solution 7

Use the three-function product rule with $f = x^2$, $g = \sin x$, $h = \cos x$:

$$g'(x) = 2x \sin x \cos x + x^2 \cos x \cos x + x^2 \sin x (-\sin x)$$
$$= 2x \sin x \cos x + x^2 \cos^2 x - x^2 \sin^2 x$$
$$= 2x \sin x \cos x + x^2(\cos^2 x - \sin^2 x)$$
$$= x \sin 2x + x^2 \cos 2x$$

**Answer:** $g'(x) = x \sin 2x + x^2 \cos 2x$ (or $2x \sin x \cos x + x^2 \cos 2x$)

---

### Solution 8

Point: $(0, 0 \cdot e^0) = (0, 0)$

Slope: $y' = e^x + xe^x = e^x(1 + x)$
$y'(0) = e^0(1 + 0) = 1$

Tangent: $y - 0 = 1(x - 0) \Rightarrow y = x$

**Answer:** $y = x$

---

### Solution 9

**Product rule:**
$$h'(x) = 3(2x + 5) + (3x - 1)(2) = 6x + 15 + 6x - 2 = 12x + 13$$

**Expand first:**
$h(x) = 6x^2 + 15x - 2x - 5 = 6x^2 + 13x - 5$
$h'(x) = 12x + 13$ ✓

**Answer:** $h'(x) = 12x + 13$

---

### Solution 10

$$f'(x) = 2xe^x + x^2 e^x = xe^x(2 + x)$$

$f'(x) = 0$ when $x = 0$ or $x = -2$ (since $e^x \neq 0$)

**Answer:** $x = 0$ and $x = -2$

---

### Solution 11

First derivative:
$$f'(x) = 2x \sin x + x^2 \cos x$$

Second derivative (product rule on each term):
$$f''(x) = [2\sin x + 2x \cos x] + [2x \cos x + x^2(-\sin x)]$$
$$= 2\sin x + 2x \cos x + 2x \cos x - x^2 \sin x$$
$$= 2\sin x + 4x \cos x - x^2 \sin x$$
$$= (2 - x^2)\sin x + 4x \cos x$$

**Answer:** $f''(x) = (2 - x^2)\sin x + 4x \cos x$

---

### Solution 12

$$g'(x) = 1 \cdot \ln x + x \cdot \frac{1}{x} - 1 = \ln x + 1 - 1 = \ln x$$

**Answer:** $g'(x) = \ln x$

---

### Solution 13

$$f'(x) = 2x \cdot g(x) + x^2 \cdot g'(x)$$

$$f'(2) = 2(2) \cdot g(2) + (2)^2 \cdot g'(2) = 4(3) + 4(-1) = 12 - 4 = 8$$

**Answer:** $f'(2) = 8$

---

### Solution 14

Point: $\left(\frac{\pi}{2}, \frac{\pi}{2} \cos \frac{\pi}{2}\right) = \left(\frac{\pi}{2}, 0\right)$

Slope of tangent: $y' = \cos x + x(-\sin x) = \cos x - x \sin x$
$$y'\left(\frac{\pi}{2}\right) = 0 - \frac{\pi}{2}(1) = -\frac{\pi}{2}$$

Normal slope: $\frac{2}{\pi}$

Normal line: $y - 0 = \frac{2}{\pi}\left(x - \frac{\pi}{2}\right)$
$$y = \frac{2}{\pi}x - 1$$

**Answer:** $y = \frac{2}{\pi}x - 1$

---

### Solution 15

Let $u = x^2 + 1$, $v = x^3 - 1$, $w = x - 2$

$$f'(x) = u'vw + uv'w + uvw'$$
$$= 2x(x^3 - 1)(x - 2) + (x^2 + 1)(3x^2)(x - 2) + (x^2 + 1)(x^3 - 1)(1)$$

This is complex to expand fully. The answer in factored form uses the given expression.

**Answer:** $f'(x) = 2x(x^3-1)(x-2) + 3x^2(x^2+1)(x-2) + (x^2+1)(x^3-1)$

---

### Solution 16

$$h'(x) = f'(x)g(x) + f(x)g'(x)$$

$$h'(3) = f'(3) \cdot g(3) + f(3) \cdot g'(3)$$
$$= (-1)(5) + (2)(4) = -5 + 8 = 3$$

**Answer:** $h'(3) = 3$

---

### Solution 17

Given $f(x) \cdot f'(x) = x$, this is $\frac{1}{2}\frac{d}{dx}[f(x)^2] = x$.

Integrating: $\frac{1}{2}f(x)^2 = \frac{x^2}{2} + C$

So $f(x)^2 = x^2 + 2C$

Using $f(0) = 1$: $1 = 0 + 2C$, so $C = \frac{1}{2}$

$f(x)^2 = x^2 + 1$

$f(x) = \sqrt{x^2 + 1}$ (taking positive root since $f(0) = 1 > 0$)

**Answer:** $f(x) = \sqrt{x^2 + 1}$

---

### Solution 18

Let $f(x) = x^n e^x$.

$$f'(x) = nx^{n-1} \cdot e^x + x^n \cdot e^x = e^x(nx^{n-1} + x^n) = e^x \cdot x^{n-1}(n + x)$$

Or written as: $e^x(x^n + nx^{n-1})$ ✓

**Answer:** Proven. $\frac{d}{dx}[x^n e^x] = e^x(x^n + nx^{n-1})$

---

## AP Exam Tips

### Recognizing Product Rule Problems

Look for:
- Two different types of functions multiplied: $x^2 e^x$, $x \sin x$
- Products where neither factor is a constant
- Problems asking for $f'(a)$ where $f$ is given as a product

### Speed Tips

1. **Identify factors quickly:** Write $u = ...$, $v = ...$ if it helps
2. **Don't simplify mid-calculation:** Apply the rule, then simplify at the end
3. **Factor out common terms:** $e^x$ and powers of $x$ often factor out

### Common FRQ Patterns

1. **Given values:** "If $f(2) = 3$ and $g(2) = 5$, and $h(x) = f(x)g(x)$..."
2. **Tangent lines:** Find tangent to $y = f(x)g(x)$ at a point
3. **Analysis:** Where does $f(x) = x^2 e^x$ have horizontal tangents?

### Multiple Choice Tips

- If an answer has only one term, it's probably wrong for a product rule problem
- Check that both original functions appear in the answer
- Watch for sign errors, especially with $\cos x$ derivatives

---

## Summary

**The Product Rule:**
$$\frac{d}{dx}[f(x) \cdot g(x)] = f'(x) \cdot g(x) + f(x) \cdot g'(x)$$

**In shorthand:** $(uv)' = u'v + uv'$

**Key Points:**
- The derivative of a product is NOT the product of derivatives
- "First times derivative of second, plus second times derivative of first"
- For three functions: $(fgh)' = f'gh + fg'h + fgh'$
- Factor out common terms when simplifying
- Sometimes expanding first is easier (especially for polynomial products)

**Common with:**
- $x^n \cdot e^x$: Leads to $e^x$ times polynomial
- $x^n \cdot \sin x$ or $x^n \cdot \cos x$: Trig terms remain
- $x^n \cdot \ln x$: Watch for the $\frac{1}{x}$ term

The product rule is essential for differentiating combinations of functions. Next up: the quotient rule for handling divisions!

---

<div align="center">

[← Derivative Rules](calculus/basic-derivative-rules.md) | [Quotient Rule →](calculus/quotient-rule.md)

</div>
