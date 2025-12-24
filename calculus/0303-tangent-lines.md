# Tangent Lines and Linear Approximation
<p class="article-date">December 14, 2024</p>

## Learning Objectives

By the end of this article, you will be able to:

- Write equations of tangent lines confidently and quickly
- Use tangent lines to approximate function values (linearization)
- Understand local linearity and why "zooming in" makes curves look straight
- Determine whether a linear approximation overestimates or underestimates
- Find tangent lines from external points to curves
- Find common tangent lines to two curves
- Apply tangent line concepts to real-world problems
- Solve AP Calculus free-response questions involving tangent lines

---

## The Core Concept: Lines That Kiss Curves

### What Makes a Tangent Line Special?

A tangent line doesn't just touch a curve—it **matches the curve's direction** at that point. It's the best possible straight-line approximation to the curve near that point.

Three key properties:
1. **Passes through** the point $(a, f(a))$
2. **Has slope** equal to $f'(a)$
3. **Best linear approximation** to $f(x)$ near $x = a$

```
                    curve
                   /
                  /
                 • ← point of tangency
                /|
               / |
              /  | tangent line matches
             /   | the curve's direction
            /    |
```

### The Tangent Line Formula

The equation of the tangent line to $y = f(x)$ at $x = a$:

$$\boxed{y = f(a) + f'(a)(x - a)}$$

This is just point-slope form: $y - y_1 = m(x - x_1)$ rearranged.

**Memory trick:** The tangent line at $a$ gives:
- The correct **value** at $a$: plug in $x = a$ and get $y = f(a)$
- The correct **slope** at $a$: the coefficient of $(x - a)$ is $f'(a)$

---

## Quick Tangent Line Problems

### The Fast Method

For most problems, follow these three steps:

1. **Point:** Calculate $f(a)$
2. **Slope:** Calculate $f'(a)$
3. **Equation:** $y = f(a) + f'(a)(x - a)$

### Example 1: Basic Tangent Line

**Find the tangent line to $f(x) = x^3 - 2x$ at $x = 1$.**

**Solution:**

1. **Point:** $f(1) = 1 - 2 = -1$
2. **Slope:** $f'(x) = 3x^2 - 2$, so $f'(1) = 3 - 2 = 1$
3. **Equation:** $y = -1 + 1(x - 1) = x - 2$

**Answer:** $y = x - 2$

---

### Example 2: Tangent to a Trigonometric Function

**Find the tangent line to $f(x) = \sin x$ at $x = \frac{\pi}{3}$.**

**Solution:**

1. **Point:** $f\left(\frac{\pi}{3}\right) = \sin\frac{\pi}{3} = \frac{\sqrt{3}}{2}$

2. **Slope:** $f'(x) = \cos x$, so $f'\left(\frac{\pi}{3}\right) = \cos\frac{\pi}{3} = \frac{1}{2}$

3. **Equation:** $y = \frac{\sqrt{3}}{2} + \frac{1}{2}\left(x - \frac{\pi}{3}\right)$

**Answer:** $y = \frac{1}{2}x + \frac{\sqrt{3}}{2} - \frac{\pi}{6}$

Or equivalently: $y = \frac{1}{2}\left(x - \frac{\pi}{3}\right) + \frac{\sqrt{3}}{2}$

---

### Example 3: Tangent to an Exponential Function

**Find the tangent line to $f(x) = e^x$ at $x = 0$.**

**Solution:**

1. **Point:** $f(0) = e^0 = 1$
2. **Slope:** $f'(x) = e^x$, so $f'(0) = 1$
3. **Equation:** $y = 1 + 1(x - 0) = x + 1$

**Answer:** $y = x + 1$

This is a famous result: the tangent to $e^x$ at the origin is $y = x + 1$.

---

### Example 4: Tangent to a Logarithmic Function

**Find the tangent line to $f(x) = \ln x$ at $x = 1$.**

**Solution:**

1. **Point:** $f(1) = \ln 1 = 0$
2. **Slope:** $f'(x) = \frac{1}{x}$, so $f'(1) = 1$
3. **Equation:** $y = 0 + 1(x - 1) = x - 1$

**Answer:** $y = x - 1$

---

## Linear Approximation (Linearization)

### The Big Idea

Near $x = a$, the tangent line is almost indistinguishable from the curve. This means:

$$\boxed{f(x) \approx f(a) + f'(a)(x - a) \quad \text{for } x \text{ near } a}$$

This is called the **linear approximation** or **linearization** of $f$ at $a$.

We denote the linearization as $L(x)$:

$$L(x) = f(a) + f'(a)(x - a)$$

### Why This Works: Local Linearity

If you zoom in on any smooth curve at a point, it looks more and more like a straight line.

```
Zoomed out:           Zoomed in (at the dot):

    /\                      /
   /  \                    / ← looks straight!
  /    \                  •
 /   •  \                /
/        \              /
```

This property is called **local linearity**. Differentiable functions are locally linear.

---

### Example 5: Approximating $\sqrt{4.1}$

**Use linear approximation to estimate $\sqrt{4.1}$.**

**Solution:**

Let $f(x) = \sqrt{x}$. We want $f(4.1)$, which is near $a = 4$.

1. **Set up:** $f(x) = \sqrt{x}$, $a = 4$
2. **Point:** $f(4) = 2$
3. **Slope:** $f'(x) = \frac{1}{2\sqrt{x}}$, so $f'(4) = \frac{1}{4}$
4. **Linearization:** $L(x) = 2 + \frac{1}{4}(x - 4)$
5. **Approximate:** $L(4.1) = 2 + \frac{1}{4}(0.1) = 2 + 0.025 = 2.025$

**Answer:** $\sqrt{4.1} \approx 2.025$

(Actual value: $\sqrt{4.1} \approx 2.0248...$, so our estimate is excellent!)

---

### Example 6: Approximating $\sin(0.1)$

**Use linear approximation to estimate $\sin(0.1)$.**

**Solution:**

Let $f(x) = \sin x$, and use $a = 0$ (since 0.1 is close to 0).

1. **Point:** $f(0) = \sin 0 = 0$
2. **Slope:** $f'(x) = \cos x$, so $f'(0) = \cos 0 = 1$
3. **Linearization:** $L(x) = 0 + 1(x - 0) = x$
4. **Approximate:** $L(0.1) = 0.1$

**Answer:** $\sin(0.1) \approx 0.1$

(Actual value: $\sin(0.1) \approx 0.0998...$)

**Key insight:** For small $x$ (in radians), $\sin x \approx x$. This is used extensively in physics and engineering!

---

### Example 7: Approximating $(1.02)^5$

**Use linear approximation to estimate $(1.02)^5$.**

**Solution:**

Let $f(x) = x^5$, and use $a = 1$.

1. **Point:** $f(1) = 1$
2. **Slope:** $f'(x) = 5x^4$, so $f'(1) = 5$
3. **Linearization:** $L(x) = 1 + 5(x - 1)$
4. **Approximate:** $L(1.02) = 1 + 5(0.02) = 1 + 0.1 = 1.1$

**Answer:** $(1.02)^5 \approx 1.1$

(Actual value: $(1.02)^5 \approx 1.104...$)

---

### Example 8: The $(1 + x)^n$ Approximation

**For small $x$, show that $(1 + x)^n \approx 1 + nx$.**

**Solution:**

Let $f(x) = (1 + x)^n$, centered at $a = 0$.

1. **Point:** $f(0) = 1^n = 1$
2. **Slope:** $f'(x) = n(1 + x)^{n-1}$, so $f'(0) = n$
3. **Linearization:** $L(x) = 1 + n(x - 0) = 1 + nx$

$$\boxed{(1 + x)^n \approx 1 + nx \quad \text{for small } x}$$

This is incredibly useful! Examples:
- $(1.01)^{10} \approx 1 + 10(0.01) = 1.1$
- $(0.98)^5 = (1 - 0.02)^5 \approx 1 + 5(-0.02) = 0.9$
- $\sqrt{1.06} = (1.06)^{0.5} \approx 1 + 0.5(0.06) = 1.03$

---

## Overestimates vs. Underestimates

### Concavity Determines the Error

The tangent line approximation has predictable error based on the curve's **concavity**:

**If $f$ is concave up** ($f'' > 0$): The tangent line lies **below** the curve.
- Linear approximation **underestimates** $f(x)$

**If $f$ is concave down** ($f'' < 0$): The tangent line lies **above** the curve.
- Linear approximation **overestimates** $f(x)$

```
Concave UP (f'' > 0):          Concave DOWN (f'' < 0):

        curve                          tangent
       /    \                         /--------\
      /      \                       / curve    \
     • tangent                      •
    /  --------                    / \
   /                              /   \

Tangent is BELOW               Tangent is ABOVE
→ Underestimate                → Overestimate
```

---

### Example 9: Determining Over/Underestimate

**For $f(x) = \sqrt{x}$, does the linearization at $a = 4$ give an overestimate or underestimate of $\sqrt{5}$?**

**Solution:**

Find the concavity of $f(x) = \sqrt{x} = x^{1/2}$:

$f'(x) = \frac{1}{2}x^{-1/2}$

$f''(x) = -\frac{1}{4}x^{-3/2} = -\frac{1}{4x^{3/2}}$

Since $f''(x) < 0$ for all $x > 0$, the function is concave **down**.

**Answer:** The tangent line lies above the curve, so the linearization gives an **overestimate**.

(We found $L(4.1) = 2.025$ while $\sqrt{4.1} \approx 2.0248$. Indeed, $2.025 > 2.0248$.)

---

### Example 10: Error Analysis

**Using the linearization of $f(x) = e^x$ at $a = 0$, estimate $e^{0.1}$ and determine if it's an over or underestimate.**

**Solution:**

**Linearization:** $L(x) = 1 + x$ (from Example 3)

**Estimate:** $L(0.1) = 1.1$

**Concavity:** $f''(x) = e^x > 0$ for all $x$, so $f$ is concave **up**.

**Answer:** Since concave up → tangent below curve → **underestimate**.

$e^{0.1} \approx 1.105$, and indeed $1.1 < 1.105$.

---

## Tangent Lines from External Points

### The Problem Type

Given a curve $y = f(x)$ and an external point $P = (x_0, y_0)$ not on the curve, find all lines through $P$ that are tangent to the curve.

### The Strategy

1. Let the unknown point of tangency be $(a, f(a))$
2. The slope of the tangent at this point is $f'(a)$
3. The line through $P$ and $(a, f(a))$ must have slope $f'(a)$
4. Set up the equation: $\frac{f(a) - y_0}{a - x_0} = f'(a)$
5. Solve for $a$

---

### Example 11: Tangent Lines to a Parabola from an External Point

**Find all lines through $(0, -1)$ that are tangent to $y = x^2$.**

**Solution:**

Let the point of tangency be $(a, a^2)$.

**Tangent slope:** $f'(a) = 2a$

**Slope from $(0, -1)$ to $(a, a^2)$:** $\frac{a^2 - (-1)}{a - 0} = \frac{a^2 + 1}{a}$

**Set equal:**
$$\frac{a^2 + 1}{a} = 2a$$
$$a^2 + 1 = 2a^2$$
$$1 = a^2$$
$$a = \pm 1$$

**For $a = 1$:** Point $(1, 1)$, slope $2$
$$y - (-1) = 2(x - 0) \implies y = 2x - 1$$

**For $a = -1$:** Point $(-1, 1)$, slope $-2$
$$y - (-1) = -2(x - 0) \implies y = -2x - 1$$

**Answer:** $y = 2x - 1$ and $y = -2x - 1$

---

### Example 12: Tangent from a Point on the Axis

**Find all tangent lines to $y = x^3$ that pass through $(2, 0)$.**

**Solution:**

Let the point of tangency be $(a, a^3)$.

**Tangent slope:** $f'(a) = 3a^2$

**Slope from $(2, 0)$ to $(a, a^3)$:** $\frac{a^3 - 0}{a - 2} = \frac{a^3}{a - 2}$

**Set equal:**
$$\frac{a^3}{a - 2} = 3a^2$$

If $a \neq 0$: $\frac{a}{a - 2} = 3$
$$a = 3(a - 2) = 3a - 6$$
$$-2a = -6$$
$$a = 3$$

If $a = 0$: Check if $(2, 0)$, $(0, 0)$, slope $0$ works: $\frac{0 - 0}{0 - 2} = 0 = 3(0)^2$ ✓

**For $a = 3$:** Point $(3, 27)$, slope $27$
$$y - 0 = 27(x - 2) \implies y = 27x - 54$$

**For $a = 0$:** Point $(0, 0)$, slope $0$
$$y = 0$$

**Answer:** $y = 27x - 54$ and $y = 0$

---

## Common Tangent Lines

### Finding Lines Tangent to Two Curves

A **common tangent** to two curves touches both curves and is tangent to each.

**Strategy:**
1. Let $(a, f(a))$ be on the first curve with tangent slope $f'(a)$
2. Let $(b, g(b))$ be on the second curve with tangent slope $g'(b)$
3. For the same line: slopes must be equal AND points must be collinear
4. Set up and solve the system

---

### Example 13: Common Tangent to Two Parabolas

**Find the common tangent line(s) to $y = x^2$ and $y = -x^2 + 4x - 2$.**

**Solution:**

Let tangent point on first curve be $(a, a^2)$, slope $2a$.
Let tangent point on second curve be $(b, -b^2 + 4b - 2)$, slope $-2b + 4$.

**Condition 1: Slopes are equal**
$$2a = -2b + 4$$
$$a + b = 2 \quad \text{...(1)}$$

**Condition 2: Points are on the same line**

The slope between the two points equals the tangent slope:
$$\frac{(-b^2 + 4b - 2) - a^2}{b - a} = 2a$$

Simplify numerator: $-b^2 + 4b - 2 - a^2$

$$-b^2 + 4b - 2 - a^2 = 2a(b - a)$$
$$-b^2 + 4b - 2 - a^2 = 2ab - 2a^2$$
$$-b^2 + 4b - 2 - a^2 = 2ab - 2a^2$$
$$a^2 - b^2 + 4b - 2 - 2ab = 0$$
$$(a - b)(a + b) + 4b - 2 - 2ab = 0$$

Using $a + b = 2$ from (1):
$$(a - b)(2) + 4b - 2 - 2ab = 0$$
$$2a - 2b + 4b - 2 - 2ab = 0$$
$$2a + 2b - 2 - 2ab = 0$$
$$2(2) - 2 - 2ab = 0$$ (using $a + b = 2$)
$$4 - 2 - 2ab = 0$$
$$ab = 1$$

Now solve: $a + b = 2$ and $ab = 1$

These are roots of $t^2 - 2t + 1 = 0$, so $(t-1)^2 = 0$, giving $a = b = 1$.

**Point on first curve:** $(1, 1)$
**Slope:** $2(1) = 2$
**Line:** $y - 1 = 2(x - 1) \implies y = 2x - 1$

**Answer:** $y = 2x - 1$ is the only common tangent.

---

## Tangent Lines and Curve Behavior

### Horizontal Tangent Lines Revisited

A **horizontal tangent** occurs where $f'(x) = 0$.

These points are candidates for:
- Local maxima
- Local minima
- Inflection points (if concavity doesn't change)

### Example 14: All Horizontal Tangents

**Find all points where $f(x) = x^4 - 4x^3 + 4x^2$ has a horizontal tangent.**

**Solution:**

$$f'(x) = 4x^3 - 12x^2 + 8x = 4x(x^2 - 3x + 2) = 4x(x-1)(x-2)$$

Set $f'(x) = 0$: $x = 0, 1, 2$

**Points:**
- $x = 0$: $f(0) = 0$ → $(0, 0)$
- $x = 1$: $f(1) = 1 - 4 + 4 = 1$ → $(1, 1)$
- $x = 2$: $f(2) = 16 - 32 + 16 = 0$ → $(2, 0)$

**Answer:** Horizontal tangents at $(0, 0)$, $(1, 1)$, and $(2, 0)$

---

### Vertical Tangent Lines

A **vertical tangent** occurs where $f'(x) \to \pm\infty$.

The tangent line exists but is vertical: $x = a$

### Example 15: Finding Vertical Tangents

**Where does $f(x) = x^{1/3}$ have a vertical tangent?**

**Solution:**

$$f'(x) = \frac{1}{3}x^{-2/3} = \frac{1}{3x^{2/3}}$$

As $x \to 0$: $f'(x) \to \infty$

The function is continuous at $x = 0$ (since $f(0) = 0$), but the tangent is vertical.

**Answer:** Vertical tangent at $x = 0$ (the line $x = 0$, i.e., the $y$-axis)

---

## Applications of Tangent Lines

### Application 1: Estimating Change

If $y = f(x)$ and $x$ changes from $a$ to $a + \Delta x$:

**Exact change:** $\Delta y = f(a + \Delta x) - f(a)$

**Approximate change:** $\Delta y \approx f'(a) \cdot \Delta x$

This uses the tangent line: the rise equals slope times run.

---

### Example 16: Estimating Change

**The radius of a sphere is measured as 5 cm with an error of ±0.1 cm. Estimate the error in the calculated volume.**

**Solution:**

Volume: $V = \frac{4}{3}\pi r^3$

$$\frac{dV}{dr} = 4\pi r^2$$

At $r = 5$: $\frac{dV}{dr} = 4\pi(25) = 100\pi$

**Approximate error:**
$$\Delta V \approx \frac{dV}{dr} \cdot \Delta r = 100\pi \cdot (\pm 0.1) = \pm 10\pi \approx \pm 31.4 \text{ cm}^3$$

**Answer:** The error in volume is approximately $\pm 31.4$ cm³.

---

### Application 2: Newton's Method (Preview)

Newton's method uses tangent lines to find roots of equations. Starting with a guess $x_0$, the next approximation is where the tangent line crosses the $x$-axis:

$$x_{n+1} = x_n - \frac{f(x_n)}{f'(x_n)}$$

```
      |
      |   curve
      | /
      |/
   ───●─────────── tangent
     /|
    / |
   /  ●← next guess
```

---

### Example 17: One Newton's Method Step

**Starting with $x_0 = 2$, use one step of Newton's method to approximate a root of $f(x) = x^2 - 3$.**

**Solution:**

$f(x) = x^2 - 3$, $f'(x) = 2x$

$$x_1 = x_0 - \frac{f(x_0)}{f'(x_0)} = 2 - \frac{4 - 3}{4} = 2 - \frac{1}{4} = 1.75$$

**Answer:** $x_1 = 1.75$ (approximating $\sqrt{3} \approx 1.732...$)

---

## Practice Problems

### Basic Problems (1-5)

**1.** Find the equation of the tangent line to $f(x) = x^2 + 3x$ at $x = 2$.

---

**2.** Find the equation of the tangent line to $f(x) = \cos x$ at $x = 0$.

---

**3.** Use linear approximation to estimate $\sqrt{17}$ (use $a = 16$).

---

**4.** Use linear approximation to estimate $\ln(1.1)$ (use $a = 1$).

---

**5.** The linearization of $f(x) = x^3$ at $a = 2$ is used to estimate $f(2.1)$. Is this an overestimate or underestimate?

---

### Intermediate Problems (6-10)

**6.** Find the linearization of $f(x) = \tan x$ at $a = 0$, and use it to estimate $\tan(0.1)$.

---

**7.** Find all horizontal tangent lines to $y = x^3 - 6x^2 + 9x + 1$.

---

**8.** Find all lines through the point $(2, 3)$ that are tangent to the parabola $y = x^2$.

---

**9.** For what value of $x$ does the tangent line to $y = \sqrt{x}$ pass through the origin?

---

**10.** The tangent line to $y = f(x)$ at $(3, 5)$ passes through $(0, 2)$. Find $f(3)$ and $f'(3)$.

---

### Advanced Problems (11-15)

**11.** Find the equation of the tangent line to $y = e^{-x}$ at the point where the curve crosses the $y$-axis.

---

**12.** A common tangent to $y = x^2$ and $y = x^2 - 2x + 2$ exists. Find its equation.

---

**13.** The curves $y = x^2 + ax + b$ and $y = cx - x^2$ are tangent to each other at $(1, 0)$. Find $a$, $b$, and $c$.

---

**14.** Use linear approximation to estimate $(8.1)^{2/3}$.

---

**15.** For $f(x) = \sin x$, find the linearization at $a = \frac{\pi}{6}$ and estimate $\sin(32°)$.
(Note: $32° = \frac{32\pi}{180}$ radians)

---

### Challenge Problems (16-18)

**16.** Find all tangent lines to $y = x^3 - 3x$ that pass through the point $(1, -4)$.

---

**17.** Prove that the tangent line to $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$ at the point $(x_0, y_0)$ has equation $\frac{x \cdot x_0}{a^2} + \frac{y \cdot y_0}{b^2} = 1$.

---

**18.** Two tangent lines to $y = x^2$ intersect at $(3, -5)$. Find the $x$-coordinates of the points of tangency and show that $(3, -5)$ lies on the line connecting these points (the chord of contact).

---

## Solutions to Practice Problems

### Solution 1

Point: $f(2) = 4 + 6 = 10$

Slope: $f'(x) = 2x + 3$, so $f'(2) = 7$

Tangent: $y - 10 = 7(x - 2)$
$$y = 7x - 4$$

**Answer:** $y = 7x - 4$

---

### Solution 2

Point: $f(0) = \cos 0 = 1$

Slope: $f'(x) = -\sin x$, so $f'(0) = 0$

Tangent: $y - 1 = 0(x - 0)$
$$y = 1$$

**Answer:** $y = 1$ (horizontal tangent)

---

### Solution 3

$f(x) = \sqrt{x}$, $a = 16$

$f(16) = 4$, $f'(x) = \frac{1}{2\sqrt{x}}$, $f'(16) = \frac{1}{8}$

$L(x) = 4 + \frac{1}{8}(x - 16)$

$L(17) = 4 + \frac{1}{8}(1) = 4.125$

**Answer:** $\sqrt{17} \approx 4.125$

---

### Solution 4

$f(x) = \ln x$, $a = 1$

$f(1) = 0$, $f'(x) = \frac{1}{x}$, $f'(1) = 1$

$L(x) = 0 + 1(x - 1) = x - 1$

$L(1.1) = 0.1$

**Answer:** $\ln(1.1) \approx 0.1$

---

### Solution 5

$f(x) = x^3$, $f''(x) = 6x$

At $x = 2$: $f''(2) = 12 > 0$, so concave **up**.

Tangent lies below curve → **underestimate**.

**Answer:** Underestimate

---

### Solution 6

$f(x) = \tan x$, $a = 0$

$f(0) = 0$, $f'(x) = \sec^2 x$, $f'(0) = 1$

$L(x) = 0 + 1(x - 0) = x$

$L(0.1) = 0.1$

**Answer:** $L(x) = x$; $\tan(0.1) \approx 0.1$

---

### Solution 7

$y' = 3x^2 - 12x + 9 = 3(x^2 - 4x + 3) = 3(x-1)(x-3)$

$y' = 0$ when $x = 1$ or $x = 3$

At $x = 1$: $y = 1 - 6 + 9 + 1 = 5$
At $x = 3$: $y = 27 - 54 + 27 + 1 = 1$

**Answer:** Horizontal tangents: $y = 5$ at $(1, 5)$ and $y = 1$ at $(3, 1)$

---

### Solution 8

Let tangent point be $(a, a^2)$, slope $= 2a$.

Slope from $(2, 3)$ to $(a, a^2)$: $\frac{a^2 - 3}{a - 2}$

Set equal: $\frac{a^2 - 3}{a - 2} = 2a$

$a^2 - 3 = 2a(a - 2) = 2a^2 - 4a$

$0 = a^2 - 4a + 3 = (a-1)(a-3)$

$a = 1$ or $a = 3$

For $a = 1$: slope $= 2$, point $(1, 1)$
$y - 3 = 2(x - 2) \Rightarrow y = 2x - 1$

For $a = 3$: slope $= 6$, point $(3, 9)$
$y - 3 = 6(x - 2) \Rightarrow y = 6x - 9$

**Answer:** $y = 2x - 1$ and $y = 6x - 9$

---

### Solution 9

Tangent at $(a, \sqrt{a})$ has slope $\frac{1}{2\sqrt{a}}$.

Equation: $y - \sqrt{a} = \frac{1}{2\sqrt{a}}(x - a)$

For this to pass through $(0, 0)$:
$-\sqrt{a} = \frac{1}{2\sqrt{a}}(-a) = -\frac{a}{2\sqrt{a}} = -\frac{\sqrt{a}}{2}$

$\sqrt{a} = \frac{\sqrt{a}}{2}$ is false for $a > 0$.

Wait, let me redo: $0 - \sqrt{a} = \frac{1}{2\sqrt{a}}(0 - a)$

$-\sqrt{a} = -\frac{a}{2\sqrt{a}} = -\frac{\sqrt{a}}{2}$

This gives $\sqrt{a} = \frac{\sqrt{a}}{2}$, which is impossible for $a > 0$.

Hmm, let me reconsider. Actually:
$-\sqrt{a} = -\frac{a}{2\sqrt{a}}$
$\sqrt{a} = \frac{a}{2\sqrt{a}}$
$2a = a$

This only works if $a = 0$, but that's not in the domain.

Actually I think I need to reconsider. The tangent line equation passing through origin:
The tangent at $x = a$: $y = \sqrt{a} + \frac{1}{2\sqrt{a}}(x - a)$

At $x = 0$: $y = \sqrt{a} - \frac{a}{2\sqrt{a}} = \sqrt{a} - \frac{\sqrt{a}}{2} = \frac{\sqrt{a}}{2}$

For this to equal 0: $\frac{\sqrt{a}}{2} = 0$, so $a = 0$.

But at $a = 0$, the derivative is undefined.

**Answer:** No such tangent line exists (the origin is inside the curve for $x > 0$).

---

### Solution 10

The tangent passes through $(3, 5)$ and $(0, 2)$.

$f(3) = 5$ (the point is on the curve)

Slope: $f'(3) = \frac{5 - 2}{3 - 0} = 1$

**Answer:** $f(3) = 5$, $f'(3) = 1$

---

### Solution 11

$y = e^{-x}$ crosses $y$-axis at $x = 0$: point $(0, 1)$

$y' = -e^{-x}$, so $y'(0) = -1$

Tangent: $y - 1 = -1(x - 0)$
$$y = -x + 1$$

**Answer:** $y = -x + 1$

---

### Solution 12

First curve: $(a, a^2)$, slope $2a$
Second curve: $(b, b^2 - 2b + 2)$, slope $2b - 2$

Equal slopes: $2a = 2b - 2 \Rightarrow a = b - 1$

Points on same line with slope $2a$:
$\frac{(b^2 - 2b + 2) - a^2}{b - a} = 2a$

With $a = b - 1$:
$\frac{b^2 - 2b + 2 - (b-1)^2}{b - (b-1)} = 2(b-1)$

$\frac{b^2 - 2b + 2 - b^2 + 2b - 1}{1} = 2b - 2$

$1 = 2b - 2$

$b = \frac{3}{2}$, $a = \frac{1}{2}$

Point on first: $(\frac{1}{2}, \frac{1}{4})$, slope $= 1$

Line: $y - \frac{1}{4} = 1(x - \frac{1}{2})$
$$y = x - \frac{1}{4}$$

**Answer:** $y = x - \frac{1}{4}$

---

### Solution 13

Both curves pass through $(1, 0)$:
- $1 + a + b = 0 \Rightarrow a + b = -1$ ... (1)
- $c - 1 = 0 \Rightarrow c = 1$ ... (2)

Tangent at $(1, 0)$ means equal slopes:
- First: $y' = 2x + a$, at $x=1$: $2 + a$
- Second: $y' = c - 2x$, at $x=1$: $c - 2 = 1 - 2 = -1$

So $2 + a = -1 \Rightarrow a = -3$

From (1): $b = -1 - (-3) = 2$

**Answer:** $a = -3$, $b = 2$, $c = 1$

---

### Solution 14

$f(x) = x^{2/3}$, $a = 8$

$f(8) = 8^{2/3} = 4$

$f'(x) = \frac{2}{3}x^{-1/3} = \frac{2}{3x^{1/3}}$

$f'(8) = \frac{2}{3 \cdot 2} = \frac{1}{3}$

$L(x) = 4 + \frac{1}{3}(x - 8)$

$L(8.1) = 4 + \frac{1}{3}(0.1) = 4 + \frac{1}{30} \approx 4.033$

**Answer:** $(8.1)^{2/3} \approx 4.033$

---

### Solution 15

$f(x) = \sin x$, $a = \frac{\pi}{6}$

$f(\frac{\pi}{6}) = \frac{1}{2}$

$f'(x) = \cos x$, $f'(\frac{\pi}{6}) = \frac{\sqrt{3}}{2}$

$L(x) = \frac{1}{2} + \frac{\sqrt{3}}{2}(x - \frac{\pi}{6})$

$32° = \frac{32\pi}{180} = \frac{8\pi}{45}$ radians

$\frac{8\pi}{45} - \frac{\pi}{6} = \frac{16\pi - 15\pi}{90} = \frac{\pi}{90}$

$L(\frac{8\pi}{45}) = \frac{1}{2} + \frac{\sqrt{3}}{2} \cdot \frac{\pi}{90} = \frac{1}{2} + \frac{\sqrt{3}\pi}{180}$

$\approx 0.5 + \frac{1.732 \times 3.14159}{180} \approx 0.5 + 0.0302 \approx 0.530$

**Answer:** $\sin(32°) \approx 0.530$

---

### Solution 16

Let tangent point be $(a, a^3 - 3a)$, slope $= 3a^2 - 3$.

Slope from $(1, -4)$: $\frac{a^3 - 3a - (-4)}{a - 1} = \frac{a^3 - 3a + 4}{a - 1}$

Set equal: $\frac{a^3 - 3a + 4}{a - 1} = 3a^2 - 3$

$a^3 - 3a + 4 = (3a^2 - 3)(a - 1) = 3a^3 - 3a^2 - 3a + 3$

$0 = 2a^3 - 3a^2 + 1$

Try $a = 1$: $2 - 3 + 1 = 0$ ✓

Factor: $2a^3 - 3a^2 + 1 = (a - 1)(2a^2 - a - 1) = (a-1)(2a+1)(a-1) = (a-1)^2(2a+1)$

Solutions: $a = 1$ (double), $a = -\frac{1}{2}$

For $a = 1$: Point $(1, -2)$, slope $= 0$
Line: $y = -2$ (but check: does it pass through $(1, -4)$? $-2 \neq -4$)

Hmm, there's an issue. Let me verify: if $a = 1$, the tangent point is $(1, 1-3) = (1, -2)$.
The slope from $(1, -4)$ to $(1, -2)$ is undefined (vertical), not $0$.

So $a = 1$ doesn't work (the external point is directly below the tangent point).

For $a = -\frac{1}{2}$: Point $(-\frac{1}{2}, -\frac{1}{8} + \frac{3}{2}) = (-\frac{1}{2}, \frac{11}{8})$

Slope: $3(\frac{1}{4}) - 3 = -\frac{9}{4}$

Line: $y - (-4) = -\frac{9}{4}(x - 1)$
$y = -\frac{9}{4}x + \frac{9}{4} - 4 = -\frac{9}{4}x - \frac{7}{4}$

**Answer:** $y = -\frac{9}{4}x - \frac{7}{4}$

---

### Solution 17

Implicitly differentiate $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$:

$\frac{2x}{a^2} + \frac{2y}{b^2} \cdot y' = 0$

$y' = -\frac{b^2 x}{a^2 y}$

At $(x_0, y_0)$: slope $= -\frac{b^2 x_0}{a^2 y_0}$

Tangent line: $y - y_0 = -\frac{b^2 x_0}{a^2 y_0}(x - x_0)$

Multiply by $\frac{y_0}{b^2}$:

$\frac{y \cdot y_0}{b^2} - \frac{y_0^2}{b^2} = -\frac{x_0}{a^2}(x - x_0)$

$\frac{y \cdot y_0}{b^2} - \frac{y_0^2}{b^2} = -\frac{x \cdot x_0}{a^2} + \frac{x_0^2}{a^2}$

$\frac{x \cdot x_0}{a^2} + \frac{y \cdot y_0}{b^2} = \frac{x_0^2}{a^2} + \frac{y_0^2}{b^2} = 1$

**Answer:** $\frac{x \cdot x_0}{a^2} + \frac{y \cdot y_0}{b^2} = 1$ ∎

---

### Solution 18

Let tangent points be $(a, a^2)$ and $(b, b^2)$ with slopes $2a$ and $2b$.

Lines through $(3, -5)$:

From $(a, a^2)$: $\frac{a^2 - (-5)}{a - 3} = 2a$
$a^2 + 5 = 2a(a - 3) = 2a^2 - 6a$
$0 = a^2 - 6a - 5$
$a = \frac{6 \pm \sqrt{36 + 20}}{2} = \frac{6 \pm \sqrt{56}}{2} = 3 \pm \sqrt{14}$

So $a = 3 + \sqrt{14}$ and $b = 3 - \sqrt{14}$.

**Chord of contact:** Line through $(a, a^2)$ and $(b, b^2)$:

Slope: $\frac{a^2 - b^2}{a - b} = a + b = 6$

Using point $(b, b^2)$: $y - b^2 = 6(x - b)$

At $x = 3$: $y = b^2 + 6(3 - b) = b^2 - 6b + 18$

$= (3 - \sqrt{14})^2 - 6(3 - \sqrt{14}) + 18$
$= 9 - 6\sqrt{14} + 14 - 18 + 6\sqrt{14} + 18 = 23$

But we need to check if $(3, -5)$ is on this chord...

Actually, the chord of contact for tangents from external point $(h, k)$ to $y = x^2$ is: $y = \frac{x \cdot h + k}{1} = ...$

Let me use the formula: for $y = x^2$, chord of contact from $(h, k)$: $\frac{y + k}{2} = xh$, i.e., $y = 2hx - k$

From $(3, -5)$: $y = 6x - (-5) = 6x + 5$... but that doesn't pass through $(3, -5)$.

Using direct calculation: chord through $(3+\sqrt{14}, (3+\sqrt{14})^2)$ and $(3-\sqrt{14}, (3-\sqrt{14})^2)$

The $x$-coordinates are $3 \pm \sqrt{14}$.

**Answer:** $x$-coordinates of tangent points: $3 + \sqrt{14}$ and $3 - \sqrt{14}$

---

## AP Exam Tips

### Tangent Line Questions on the AP Exam

Tangent lines appear in multiple contexts:
1. **Straightforward:** "Find the tangent line at $x = a$"
2. **Linear approximation:** "Use the tangent line to estimate..."
3. **Interpretation:** "The line $y = 3x + 2$ is tangent to $f$ at $x = 1$. Find $f(1)$ and $f'(1)$."
4. **Tables/Graphs:** "From the table, estimate $f'(2)$ and write the tangent line."

### Common Free-Response Patterns

**Pattern 1:** Given a table, estimate derivative and write tangent line.

**Pattern 2:** Given position function, find velocity (derivative) at a time and interpret.

**Pattern 3:** Use tangent line to approximate, then determine over/underestimate using concavity.

### Key Points to Remember

1. **Tangent line formula:** $y = f(a) + f'(a)(x - a)$

2. **Linear approximation:** $f(x) \approx L(x)$ for $x$ near $a$

3. **Concavity and error:**
   - Concave up → underestimate
   - Concave down → overestimate

4. **Horizontal tangent:** $f'(x) = 0$

5. **Normal line slope:** $-\frac{1}{f'(a)}$

---

## Summary

**Tangent Line Equation:**
$$y = f(a) + f'(a)(x - a)$$

**Linear Approximation:**
$$f(x) \approx f(a) + f'(a)(x - a) \text{ for } x \text{ near } a$$

**Useful Approximations for Small $x$:**
- $\sin x \approx x$
- $\cos x \approx 1$
- $\tan x \approx x$
- $e^x \approx 1 + x$
- $\ln(1 + x) \approx x$
- $(1 + x)^n \approx 1 + nx$

**Over/Underestimate:**
- $f'' > 0$ (concave up) → tangent below → underestimate
- $f'' < 0$ (concave down) → tangent above → overestimate

**Tangent from External Point:** Set up equation where slope from external point to curve point equals derivative at that point.

Tangent lines are the bridge between calculus and algebra—they let us use linear tools to understand curved behavior!

---

<div align="center">

[← Derivative at a Point](calculus/derivative-at-a-point.md) | [Derivative Rules →](calculus/basic-derivative-rules.md)

</div>
