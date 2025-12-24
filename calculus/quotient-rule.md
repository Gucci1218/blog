# The Quotient Rule

## Learning Objectives

By the end of this article, you will be able to:

- Apply the quotient rule to differentiate ratios of functions
- Use the "low d-high minus high d-low" mnemonic
- Derive the quotient rule from the product rule
- Choose between the quotient rule and rewriting with negative exponents
- Differentiate all six trigonometric functions
- Avoid common sign errors in the quotient rule
- Solve AP Calculus problems involving quotients

---

## The Core Concept: Dividing Functions

### Another Wrong Guess

Just as with products, you might hope:

$$\frac{d}{dx}\left[\frac{f(x)}{g(x)}\right] \stackrel{?}{=} \frac{f'(x)}{g'(x)}$$

**This is FALSE!**

**Example:** Let $f(x) = x^2$ and $g(x) = x$, so $\frac{f(x)}{g(x)} = x$.

**Wrong method:** $\frac{f'(x)}{g'(x)} = \frac{2x}{1} = 2x$

**Correct answer:** $\frac{d}{dx}[x] = 1$

Since $2x \neq 1$, the naive guess fails!

### The Quotient Rule

$$\boxed{\frac{d}{dx}\left[\frac{f(x)}{g(x)}\right] = \frac{f'(x) \cdot g(x) - f(x) \cdot g'(x)}{[g(x)]^2}}$$

### Alternative Notation

Using $u$ and $v$:

$$\frac{d}{dx}\left[\frac{u}{v}\right] = \frac{u'v - uv'}{v^2}$$

Or with Leibniz notation:

$$\frac{d}{dx}\left[\frac{u}{v}\right] = \frac{\frac{du}{dx} \cdot v - u \cdot \frac{dv}{dx}}{v^2}$$

---

## The Memory Device

### "Low D-High Minus High D-Low"

The most popular mnemonic:

$$\frac{d}{dx}\left[\frac{\text{high}}{\text{low}}\right] = \frac{\text{low} \cdot d(\text{high}) - \text{high} \cdot d(\text{low})}{(\text{low})^2}$$

**Full rhyme:** "Low d-high minus high d-low, draw the line and square below!"

### Breaking It Down

For $\frac{f}{g}$:
- **Low** = $g$ (the denominator)
- **High** = $f$ (the numerator)
- **d-high** = $f'$ (derivative of numerator)
- **d-low** = $g'$ (derivative of denominator)

$$\frac{g \cdot f' - f \cdot g'}{g^2}$$

### Visual Layout

```
        f
Given: ───
        g

           g · f'  −  f · g'
Answer: ─────────────────────
               g²
```

---

## Why the Minus Sign?

### Product Rule vs. Quotient Rule

| Rule | Formula | Sign |
|------|---------|------|
| Product | $f'g + fg'$ | **Plus** |
| Quotient | $\frac{f'g - fg'}{g^2}$ | **Minus** |

**Memory tip:** In the quotient rule, the numerator's derivative comes first (with the plus), and the denominator's derivative comes second (with the minus).

Think: "Numerator is Number 1" → its derivative term is positive.

---

## Deriving the Quotient Rule

### From the Product Rule

Write $\frac{f}{g} = f \cdot g^{-1}$ and use the product rule:

$$\frac{d}{dx}\left[f \cdot g^{-1}\right] = f' \cdot g^{-1} + f \cdot \frac{d}{dx}[g^{-1}]$$

For $\frac{d}{dx}[g^{-1}]$, use the power rule with chain rule (preview):
$$\frac{d}{dx}[g^{-1}] = -g^{-2} \cdot g' = -\frac{g'}{g^2}$$

So:
$$\frac{d}{dx}\left[\frac{f}{g}\right] = \frac{f'}{g} + f \cdot \left(-\frac{g'}{g^2}\right) = \frac{f'}{g} - \frac{fg'}{g^2}$$

$$= \frac{f'g - fg'}{g^2}$$

This confirms the quotient rule!

---

## Applying the Quotient Rule

### Step-by-Step Process

1. **Identify** numerator $f$ and denominator $g$
2. **Find** $f'$ and $g'$ separately
3. **Apply:** $\frac{f'g - fg'}{g^2}$
4. **Simplify** (factor if possible)

### Example 1: Basic Quotient

**Differentiate $h(x) = \frac{x^2}{x + 1}$**

**Solution:**

- $f = x^2$, so $f' = 2x$
- $g = x + 1$, so $g' = 1$

$$h'(x) = \frac{(2x)(x + 1) - (x^2)(1)}{(x + 1)^2}$$

$$= \frac{2x^2 + 2x - x^2}{(x + 1)^2} = \frac{x^2 + 2x}{(x + 1)^2}$$

$$= \frac{x(x + 2)}{(x + 1)^2}$$

**Answer:** $h'(x) = \frac{x(x + 2)}{(x + 1)^2}$

---

### Example 2: Polynomial Over Polynomial

**Differentiate $f(x) = \frac{x^3 - 1}{x^2 + 1}$**

**Solution:**

- $u = x^3 - 1$, so $u' = 3x^2$
- $v = x^2 + 1$, so $v' = 2x$

$$f'(x) = \frac{(3x^2)(x^2 + 1) - (x^3 - 1)(2x)}{(x^2 + 1)^2}$$

Expand the numerator:
$$= \frac{3x^4 + 3x^2 - 2x^4 + 2x}{(x^2 + 1)^2}$$

$$= \frac{x^4 + 3x^2 + 2x}{(x^2 + 1)^2}$$

$$= \frac{x(x^3 + 3x + 2)}{(x^2 + 1)^2}$$

**Answer:** $f'(x) = \frac{x^4 + 3x^2 + 2x}{(x^2 + 1)^2}$

---

### Example 3: With Exponentials

**Differentiate $g(x) = \frac{e^x}{x}$**

**Solution:**

- $f = e^x$, so $f' = e^x$
- $g = x$, so $g' = 1$

$$g'(x) = \frac{e^x \cdot x - e^x \cdot 1}{x^2} = \frac{e^x(x - 1)}{x^2}$$

**Answer:** $g'(x) = \frac{e^x(x - 1)}{x^2}$

---

### Example 4: With Trigonometric Functions

**Differentiate $h(x) = \frac{\sin x}{x}$**

**Solution:**

- $f = \sin x$, so $f' = \cos x$
- $g = x$, so $g' = 1$

$$h'(x) = \frac{\cos x \cdot x - \sin x \cdot 1}{x^2} = \frac{x \cos x - \sin x}{x^2}$$

**Answer:** $h'(x) = \frac{x \cos x - \sin x}{x^2}$

---

### Example 5: With Logarithms

**Differentiate $f(x) = \frac{\ln x}{x^2}$**

**Solution:**

- $u = \ln x$, so $u' = \frac{1}{x}$
- $v = x^2$, so $v' = 2x$

$$f'(x) = \frac{\frac{1}{x} \cdot x^2 - \ln x \cdot 2x}{(x^2)^2}$$

$$= \frac{x - 2x \ln x}{x^4} = \frac{x(1 - 2\ln x)}{x^4} = \frac{1 - 2\ln x}{x^3}$$

**Answer:** $f'(x) = \frac{1 - 2\ln x}{x^3}$

---

## Derivatives of All Six Trig Functions

The quotient rule lets us derive the remaining four trig derivatives.

### Tangent

$$\tan x = \frac{\sin x}{\cos x}$$

$$\frac{d}{dx}[\tan x] = \frac{\cos x \cdot \cos x - \sin x \cdot (-\sin x)}{\cos^2 x}$$

$$= \frac{\cos^2 x + \sin^2 x}{\cos^2 x} = \frac{1}{\cos^2 x} = \sec^2 x$$

$$\boxed{\frac{d}{dx}[\tan x] = \sec^2 x}$$

---

### Cotangent

$$\cot x = \frac{\cos x}{\sin x}$$

$$\frac{d}{dx}[\cot x] = \frac{-\sin x \cdot \sin x - \cos x \cdot \cos x}{\sin^2 x}$$

$$= \frac{-\sin^2 x - \cos^2 x}{\sin^2 x} = \frac{-1}{\sin^2 x} = -\csc^2 x$$

$$\boxed{\frac{d}{dx}[\cot x] = -\csc^2 x}$$

---

### Secant

$$\sec x = \frac{1}{\cos x}$$

$$\frac{d}{dx}[\sec x] = \frac{0 \cdot \cos x - 1 \cdot (-\sin x)}{\cos^2 x}$$

$$= \frac{\sin x}{\cos^2 x} = \frac{1}{\cos x} \cdot \frac{\sin x}{\cos x} = \sec x \tan x$$

$$\boxed{\frac{d}{dx}[\sec x] = \sec x \tan x}$$

---

### Cosecant

$$\csc x = \frac{1}{\sin x}$$

$$\frac{d}{dx}[\csc x] = \frac{0 \cdot \sin x - 1 \cdot \cos x}{\sin^2 x}$$

$$= \frac{-\cos x}{\sin^2 x} = -\frac{1}{\sin x} \cdot \frac{\cos x}{\sin x} = -\csc x \cot x$$

$$\boxed{\frac{d}{dx}[\csc x] = -\csc x \cot x}$$

---

### Summary: All Six Trig Derivatives

| Function | Derivative |
|----------|------------|
| $\sin x$ | $\cos x$ |
| $\cos x$ | $-\sin x$ |
| $\tan x$ | $\sec^2 x$ |
| $\cot x$ | $-\csc^2 x$ |
| $\sec x$ | $\sec x \tan x$ |
| $\csc x$ | $-\csc x \cot x$ |

**Pattern:** The "co-" functions (cosine, cotangent, cosecant) all have negative derivatives.

---

## Quotient Rule vs. Rewriting

### When to Avoid the Quotient Rule

Sometimes rewriting with negative exponents is simpler.

**Example 6:** Differentiate $f(x) = \frac{5}{x^3}$

**Method 1: Quotient Rule** (more work)
$$f'(x) = \frac{0 \cdot x^3 - 5 \cdot 3x^2}{x^6} = \frac{-15x^2}{x^6} = -\frac{15}{x^4}$$

**Method 2: Rewrite** (easier)
$$f(x) = 5x^{-3}$$
$$f'(x) = 5(-3)x^{-4} = -15x^{-4} = -\frac{15}{x^4}$$

**Rule of thumb:** If the numerator is a constant, rewriting is usually easier.

---

### Example 7: Deciding Which Method

**Differentiate $g(x) = \frac{1}{x^2 + 1}$**

The denominator is NOT just a power of $x$, so we can't easily rewrite.

**Use quotient rule:**
$$g'(x) = \frac{0 \cdot (x^2 + 1) - 1 \cdot 2x}{(x^2 + 1)^2} = \frac{-2x}{(x^2 + 1)^2}$$

**Answer:** $g'(x) = \frac{-2x}{(x^2 + 1)^2}$

---

### Guidelines

| Situation | Best Approach |
|-----------|---------------|
| $\frac{\text{constant}}{x^n}$ | Rewrite as constant $\cdot x^{-n}$ |
| $\frac{\text{polynomial}}{x^n}$ | Often split: $\frac{ax^m + bx^k}{x^n} = ax^{m-n} + bx^{k-n}$ |
| $\frac{f(x)}{g(x)}$ where $g$ is not a simple power | Quotient rule |
| $\frac{f(x)}{g(x)}$ where both are complex | Quotient rule |

---

### Example 8: Splitting a Fraction

**Differentiate $h(x) = \frac{x^4 - 3x^2 + 2}{x^2}$**

**Method: Split first**
$$h(x) = \frac{x^4}{x^2} - \frac{3x^2}{x^2} + \frac{2}{x^2} = x^2 - 3 + 2x^{-2}$$

$$h'(x) = 2x - 0 + 2(-2)x^{-3} = 2x - \frac{4}{x^3}$$

**Answer:** $h'(x) = 2x - \frac{4}{x^3}$

Much easier than using the quotient rule directly!

---

## Worked Examples

### Example 9: Finding a Specific Value

**If $f(x) = \frac{x^2 + 1}{x - 1}$, find $f'(2)$.**

**Solution:**

$$f'(x) = \frac{2x(x - 1) - (x^2 + 1)(1)}{(x - 1)^2}$$

$$= \frac{2x^2 - 2x - x^2 - 1}{(x - 1)^2} = \frac{x^2 - 2x - 1}{(x - 1)^2}$$

$$f'(2) = \frac{4 - 4 - 1}{(2 - 1)^2} = \frac{-1}{1} = -1$$

**Answer:** $f'(2) = -1$

---

### Example 10: Tangent Line

**Find the equation of the tangent line to $y = \frac{x}{x + 2}$ at $x = 2$.**

**Solution:**

**Point:** $y(2) = \frac{2}{4} = \frac{1}{2}$, so $\left(2, \frac{1}{2}\right)$

**Slope:**
$$y' = \frac{1 \cdot (x + 2) - x \cdot 1}{(x + 2)^2} = \frac{x + 2 - x}{(x + 2)^2} = \frac{2}{(x + 2)^2}$$

$$y'(2) = \frac{2}{16} = \frac{1}{8}$$

**Tangent line:**
$$y - \frac{1}{2} = \frac{1}{8}(x - 2)$$
$$y = \frac{1}{8}x - \frac{1}{4} + \frac{1}{2} = \frac{1}{8}x + \frac{1}{4}$$

**Answer:** $y = \frac{1}{8}x + \frac{1}{4}$

---

### Example 11: Horizontal Tangent

**Find all $x$ where $f(x) = \frac{x^2}{x + 1}$ has a horizontal tangent.**

**Solution:**

From Example 1: $f'(x) = \frac{x(x + 2)}{(x + 1)^2}$

For horizontal tangent, $f'(x) = 0$.

The numerator must be zero: $x(x + 2) = 0$
$$x = 0 \text{ or } x = -2$$

Check: Both values give defined $f(x)$ (denominator $\neq 0$).

**Answer:** $x = 0$ and $x = -2$

---

### Example 12: Second Derivative

**Find $f''(x)$ for $f(x) = \frac{1}{x}$.**

**Solution:**

**First derivative:**
$$f'(x) = \frac{0 \cdot x - 1 \cdot 1}{x^2} = -\frac{1}{x^2} = -x^{-2}$$

**Second derivative:** (easier to use power rule now)
$$f''(x) = -(-2)x^{-3} = \frac{2}{x^3}$$

**Answer:** $f''(x) = \frac{2}{x^3}$

---

### Example 13: Combined with Other Functions

**Differentiate $g(x) = \frac{e^x + 1}{e^x - 1}$**

**Solution:**

- $f = e^x + 1$, so $f' = e^x$
- $g = e^x - 1$, so $g' = e^x$

$$g'(x) = \frac{e^x(e^x - 1) - (e^x + 1)e^x}{(e^x - 1)^2}$$

$$= \frac{e^x[(e^x - 1) - (e^x + 1)]}{(e^x - 1)^2}$$

$$= \frac{e^x[e^x - 1 - e^x - 1]}{(e^x - 1)^2}$$

$$= \frac{e^x(-2)}{(e^x - 1)^2} = \frac{-2e^x}{(e^x - 1)^2}$$

**Answer:** $g'(x) = \frac{-2e^x}{(e^x - 1)^2}$

---

### Example 14: With Trig Functions

**Differentiate $h(x) = \frac{1 + \sin x}{\cos x}$**

**Solution:**

- $f = 1 + \sin x$, so $f' = \cos x$
- $g = \cos x$, so $g' = -\sin x$

$$h'(x) = \frac{\cos x \cdot \cos x - (1 + \sin x)(-\sin x)}{\cos^2 x}$$

$$= \frac{\cos^2 x + \sin x + \sin^2 x}{\cos^2 x}$$

$$= \frac{1 + \sin x}{\cos^2 x}$$

**Answer:** $h'(x) = \frac{1 + \sin x}{\cos^2 x}$ or $\sec^2 x + \sec x \tan x$

---

### Example 15: Product and Quotient Together

**Differentiate $f(x) = x^2 \cdot \frac{\sin x}{x + 1}$**

**Solution:**

First, let $u = x^2$ and $v = \frac{\sin x}{x + 1}$.

We need $v'$ (quotient rule):
$$v' = \frac{\cos x (x + 1) - \sin x (1)}{(x + 1)^2} = \frac{(x + 1)\cos x - \sin x}{(x + 1)^2}$$

Now apply product rule:
$$f'(x) = 2x \cdot \frac{\sin x}{x + 1} + x^2 \cdot \frac{(x + 1)\cos x - \sin x}{(x + 1)^2}$$

$$= \frac{2x \sin x}{x + 1} + \frac{x^2[(x + 1)\cos x - \sin x]}{(x + 1)^2}$$

This can be combined over a common denominator if needed.

**Answer:** $f'(x) = \frac{2x \sin x}{x + 1} + \frac{x^2[(x + 1)\cos x - \sin x]}{(x + 1)^2}$

---

## Common Mistakes

### Mistake 1: Wrong Sign (The Biggest Error!)

**Wrong:** $\frac{f'g + fg'}{g^2}$ (used plus instead of minus) ✗

**Right:** $\frac{f'g - fg'}{g^2}$ ✓

### Mistake 2: Wrong Order

**Wrong:** $\frac{fg' - f'g}{g^2}$ (subtracted in wrong order) ✗

**Right:** $\frac{f'g - fg'}{g^2}$ ✓

**Remember:** "Low d-high MINUS high d-low" — the derivative of the TOP comes first!

### Mistake 3: Forgetting to Square the Denominator

**Wrong:** $\frac{f'g - fg'}{g}$ ✗

**Right:** $\frac{f'g - fg'}{g^2}$ ✓

### Mistake 4: Using Quotient Rule When Unnecessary

For $\frac{5}{x^2}$, don't use the quotient rule. Just write $5x^{-2}$ and differentiate: $-10x^{-3}$.

### Mistake 5: Simplification Errors

After applying the quotient rule, simplify carefully:
- Expand products in the numerator
- Combine like terms
- Factor if possible

---

## Practice Problems

### Basic Problems (1-5)

**1.** Differentiate $f(x) = \frac{x^2}{x + 3}$.

---

**2.** Differentiate $g(x) = \frac{x + 1}{x - 1}$.

---

**3.** Differentiate $h(x) = \frac{e^x}{x^2}$.

---

**4.** Differentiate $f(x) = \frac{\cos x}{x}$.

---

**5.** Find $f'(1)$ for $f(x) = \frac{x^3}{x^2 + 1}$.

---

### Intermediate Problems (6-10)

**6.** Differentiate $g(x) = \frac{x^2 - 4}{x^2 + 4}$.

---

**7.** Differentiate $h(x) = \frac{\ln x}{x}$.

---

**8.** Find the equation of the tangent line to $y = \frac{e^x}{1 + e^x}$ at $x = 0$.

---

**9.** Find all values of $x$ where $f(x) = \frac{x}{x^2 + 1}$ has a horizontal tangent.

---

**10.** Differentiate $f(x) = \frac{x^2 + 3x - 1}{x}$ by first simplifying.

---

### Advanced Problems (11-15)

**11.** Differentiate $g(x) = \frac{\sin x}{1 + \cos x}$.

---

**12.** Find $f''(x)$ for $f(x) = \frac{x}{x + 1}$.

---

**13.** Differentiate $h(x) = \frac{x e^x}{x + 1}$.

---

**14.** Find the equation of the normal line to $y = \frac{x^2}{x - 1}$ at $x = 2$.

---

**15.** If $f(x) = \frac{g(x)}{h(x)}$, $g(2) = 3$, $g'(2) = -1$, $h(2) = 4$, $h'(2) = 2$, find $f'(2)$.

---

### Challenge Problems (16-18)

**16.** Prove that $\frac{d}{dx}\left[\frac{1 - \cos x}{\sin x}\right] = \frac{1}{1 + \cos x}$.

---

**17.** Find all functions of the form $f(x) = \frac{ax + b}{x + c}$ such that $f(0) = 1$ and $f'(0) = 2$.

---

**18.** The curves $y = \frac{1}{x}$ and $y = \frac{1}{x^2}$ intersect at $x = 1$. Find the acute angle between their tangent lines at this point.

---

## Solutions to Practice Problems

### Solution 1

$$f'(x) = \frac{2x(x + 3) - x^2(1)}{(x + 3)^2} = \frac{2x^2 + 6x - x^2}{(x + 3)^2} = \frac{x^2 + 6x}{(x + 3)^2}$$

$$= \frac{x(x + 6)}{(x + 3)^2}$$

**Answer:** $f'(x) = \frac{x(x + 6)}{(x + 3)^2}$

---

### Solution 2

$$g'(x) = \frac{1(x - 1) - (x + 1)(1)}{(x - 1)^2} = \frac{x - 1 - x - 1}{(x - 1)^2} = \frac{-2}{(x - 1)^2}$$

**Answer:** $g'(x) = \frac{-2}{(x - 1)^2}$

---

### Solution 3

$$h'(x) = \frac{e^x \cdot x^2 - e^x \cdot 2x}{x^4} = \frac{e^x(x^2 - 2x)}{x^4} = \frac{e^x \cdot x(x - 2)}{x^4} = \frac{e^x(x - 2)}{x^3}$$

**Answer:** $h'(x) = \frac{e^x(x - 2)}{x^3}$

---

### Solution 4

$$f'(x) = \frac{-\sin x \cdot x - \cos x \cdot 1}{x^2} = \frac{-x\sin x - \cos x}{x^2}$$

**Answer:** $f'(x) = \frac{-x\sin x - \cos x}{x^2}$

---

### Solution 5

$$f'(x) = \frac{3x^2(x^2 + 1) - x^3(2x)}{(x^2 + 1)^2} = \frac{3x^4 + 3x^2 - 2x^4}{(x^2 + 1)^2} = \frac{x^4 + 3x^2}{(x^2 + 1)^2}$$

$$f'(1) = \frac{1 + 3}{(1 + 1)^2} = \frac{4}{4} = 1$$

**Answer:** $f'(1) = 1$

---

### Solution 6

$$g'(x) = \frac{2x(x^2 + 4) - (x^2 - 4)(2x)}{(x^2 + 4)^2}$$

$$= \frac{2x[(x^2 + 4) - (x^2 - 4)]}{(x^2 + 4)^2} = \frac{2x(8)}{(x^2 + 4)^2} = \frac{16x}{(x^2 + 4)^2}$$

**Answer:** $g'(x) = \frac{16x}{(x^2 + 4)^2}$

---

### Solution 7

$$h'(x) = \frac{\frac{1}{x} \cdot x - \ln x \cdot 1}{x^2} = \frac{1 - \ln x}{x^2}$$

**Answer:** $h'(x) = \frac{1 - \ln x}{x^2}$

---

### Solution 8

Point: $y(0) = \frac{e^0}{1 + e^0} = \frac{1}{2}$, so $\left(0, \frac{1}{2}\right)$

Derivative:
$$y' = \frac{e^x(1 + e^x) - e^x \cdot e^x}{(1 + e^x)^2} = \frac{e^x + e^{2x} - e^{2x}}{(1 + e^x)^2} = \frac{e^x}{(1 + e^x)^2}$$

$$y'(0) = \frac{1}{(1 + 1)^2} = \frac{1}{4}$$

Tangent: $y - \frac{1}{2} = \frac{1}{4}(x - 0)$

$$y = \frac{1}{4}x + \frac{1}{2}$$

**Answer:** $y = \frac{1}{4}x + \frac{1}{2}$

---

### Solution 9

$$f'(x) = \frac{1(x^2 + 1) - x(2x)}{(x^2 + 1)^2} = \frac{x^2 + 1 - 2x^2}{(x^2 + 1)^2} = \frac{1 - x^2}{(x^2 + 1)^2}$$

$f'(x) = 0$ when $1 - x^2 = 0$, so $x = \pm 1$.

**Answer:** $x = 1$ and $x = -1$

---

### Solution 10

Simplify first:
$$f(x) = \frac{x^2}{x} + \frac{3x}{x} - \frac{1}{x} = x + 3 - x^{-1}$$

$$f'(x) = 1 + 0 + x^{-2} = 1 + \frac{1}{x^2}$$

**Answer:** $f'(x) = 1 + \frac{1}{x^2}$

---

### Solution 11

$$g'(x) = \frac{\cos x(1 + \cos x) - \sin x(-\sin x)}{(1 + \cos x)^2}$$

$$= \frac{\cos x + \cos^2 x + \sin^2 x}{(1 + \cos x)^2} = \frac{\cos x + 1}{(1 + \cos x)^2} = \frac{1}{1 + \cos x}$$

**Answer:** $g'(x) = \frac{1}{1 + \cos x}$

---

### Solution 12

First derivative:
$$f'(x) = \frac{1(x + 1) - x(1)}{(x + 1)^2} = \frac{1}{(x + 1)^2} = (x + 1)^{-2}$$

Second derivative:
$$f''(x) = -2(x + 1)^{-3} \cdot 1 = \frac{-2}{(x + 1)^3}$$

**Answer:** $f''(x) = \frac{-2}{(x + 1)^3}$

---

### Solution 13

Use quotient rule with $f = xe^x$ and $g = x + 1$:

First, $f' = e^x + xe^x = e^x(1 + x)$ (product rule)

$$h'(x) = \frac{e^x(1 + x)(x + 1) - xe^x(1)}{(x + 1)^2}$$

$$= \frac{e^x[(1 + x)(x + 1) - x]}{(x + 1)^2} = \frac{e^x[(x + 1)^2 - x]}{(x + 1)^2}$$

$$= \frac{e^x[x^2 + 2x + 1 - x]}{(x + 1)^2} = \frac{e^x(x^2 + x + 1)}{(x + 1)^2}$$

**Answer:** $h'(x) = \frac{e^x(x^2 + x + 1)}{(x + 1)^2}$

---

### Solution 14

Point: $y(2) = \frac{4}{1} = 4$, so $(2, 4)$

Derivative:
$$y' = \frac{2x(x - 1) - x^2(1)}{(x - 1)^2} = \frac{2x^2 - 2x - x^2}{(x - 1)^2} = \frac{x^2 - 2x}{(x - 1)^2} = \frac{x(x - 2)}{(x - 1)^2}$$

$$y'(2) = \frac{2(0)}{1} = 0$$

Tangent slope is 0, so normal slope is undefined (vertical line).

**Answer:** Normal line: $x = 2$

---

### Solution 15

$$f'(x) = \frac{g'(x)h(x) - g(x)h'(x)}{[h(x)]^2}$$

$$f'(2) = \frac{(-1)(4) - (3)(2)}{4^2} = \frac{-4 - 6}{16} = \frac{-10}{16} = -\frac{5}{8}$$

**Answer:** $f'(2) = -\frac{5}{8}$

---

### Solution 16

Let $f(x) = \frac{1 - \cos x}{\sin x}$

$$f'(x) = \frac{\sin x \cdot \sin x - (1 - \cos x)\cos x}{\sin^2 x}$$

$$= \frac{\sin^2 x - \cos x + \cos^2 x}{\sin^2 x} = \frac{1 - \cos x}{\sin^2 x}$$

$$= \frac{1 - \cos x}{1 - \cos^2 x} = \frac{1 - \cos x}{(1 - \cos x)(1 + \cos x)} = \frac{1}{1 + \cos x}$$ ✓

---

### Solution 17

$f(x) = \frac{ax + b}{x + c}$

Condition 1: $f(0) = \frac{b}{c} = 1$, so $b = c$

Condition 2: $f'(x) = \frac{a(x + c) - (ax + b)(1)}{(x + c)^2} = \frac{ac - b}{(x + c)^2}$

$f'(0) = \frac{ac - b}{c^2} = 2$

Since $b = c$: $\frac{ac - c}{c^2} = \frac{c(a - 1)}{c^2} = \frac{a - 1}{c} = 2$

So $a = 2c + 1$

With $b = c$, the family of functions is $f(x) = \frac{(2c + 1)x + c}{x + c}$ for any $c \neq 0$.

**Answer:** $f(x) = \frac{(2c+1)x + c}{x + c}$ where $c \neq 0$ (one-parameter family)

---

### Solution 18

At $x = 1$, both curves pass through $(1, 1)$.

For $y = \frac{1}{x} = x^{-1}$: $y' = -x^{-2}$, so slope at $x = 1$ is $-1$.

For $y = \frac{1}{x^2} = x^{-2}$: $y' = -2x^{-3}$, so slope at $x = 1$ is $-2$.

Angle between lines with slopes $m_1 = -1$ and $m_2 = -2$:

$$\tan\theta = \left|\frac{m_1 - m_2}{1 + m_1 m_2}\right| = \left|\frac{-1 - (-2)}{1 + (-1)(-2)}\right| = \left|\frac{1}{3}\right| = \frac{1}{3}$$

$$\theta = \arctan\left(\frac{1}{3}\right) \approx 18.43°$$

**Answer:** $\theta = \arctan\left(\frac{1}{3}\right) \approx 18.4°$

---

## AP Exam Tips

### When to Expect Quotient Rule

- Rational functions: $\frac{p(x)}{q(x)}$
- Trig functions: $\tan x$, $\cot x$, $\sec x$, $\csc x$
- Problems involving rates of ratios

### Speed Tips

1. **Memorize trig derivatives:** Don't derive $\tan x$ every time
2. **Simplify first** when possible
3. **Factor after applying** the rule to check for cancellation

### Common FRQ Patterns

1. **Given table values:** "$f(2) = 3$, $g(2) = 5$, find $\frac{d}{dx}\left[\frac{f}{g}\right]$ at $x = 2$"
2. **Horizontal tangents:** Where does $\frac{f}{g}$ have $f'(x) = 0$? Set numerator = 0
3. **Asymptote behavior:** Connected to where denominator = 0

### The Sign Check

After computing, do a quick sign check:
- Is the original function increasing or decreasing at that point?
- Does your derivative's sign match?

---

## Summary

**The Quotient Rule:**
$$\frac{d}{dx}\left[\frac{f}{g}\right] = \frac{f'g - fg'}{g^2}$$

**Mnemonic:** "Low d-high minus high d-low, draw the line and square below"

**Six Trig Derivatives:**
| $\sin x \to \cos x$ | $\cos x \to -\sin x$ |
|---------------------|----------------------|
| $\tan x \to \sec^2 x$ | $\cot x \to -\csc^2 x$ |
| $\sec x \to \sec x \tan x$ | $\csc x \to -\csc x \cot x$ |

**When to Avoid Quotient Rule:**
- $\frac{\text{constant}}{x^n}$: Rewrite as constant $\cdot x^{-n}$
- $\frac{\text{polynomial}}{x^n}$: Split into separate terms

**Key Points:**
- The minus sign is crucial—double-check it!
- Numerator derivative term comes first (with +)
- Denominator gets squared
- Simplify and factor your answer when possible

The quotient rule completes your toolkit for rational functions. Next up: the chain rule, which handles compositions!

---

<div align="center">

[← Product Rule](calculus/product-rule.md) | [Chain Rule →](calculus/chain-rule.md)

</div>
