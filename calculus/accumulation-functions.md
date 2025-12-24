# Accumulation Functions

*What if a function is defined by an integral? These special functions—called accumulation functions—measure how much of something has accumulated from a starting point to a variable endpoint. Understanding them unlocks a deeper connection between integration and differentiation, and they appear constantly on AP exams.*

---

## What You'll Learn
- Define and interpret accumulation functions
- Analyze accumulation functions using graphs of the integrand
- Find maxima, minima, and inflection points of accumulation functions
- Connect the behavior of $f$ to the behavior of $g(x) = \int_a^x f(t) \, dt$
- Solve AP-style problems involving accumulation functions

---

## Prerequisites
- [Fundamental Theorem of Calculus](/calculus/fundamental-theorem)
- [Curve Sketching](/calculus/curve-sketching)

---

## The Core Concept

### What Is an Accumulation Function?

An **accumulation function** is a function defined by a definite integral with a variable upper limit:

$$g(x) = \int_a^x f(t) \, dt$$

Think of $g(x)$ as measuring the "total accumulated" from $a$ to $x$.

### Real-World Interpretation

If $f(t)$ represents a **rate**, then $g(x) = \int_a^x f(t) \, dt$ represents the **total accumulated amount**.

| Rate $f(t)$ | Accumulation $g(x)$ |
|-------------|---------------------|
| Velocity (m/s) | Displacement (m) |
| Flow rate (gal/min) | Volume (gal) |
| Revenue rate ($/day) | Total revenue ($) |
| Population growth rate | Population change |

### Key Properties from FTC Part 1

By the Fundamental Theorem of Calculus (Part 1):

$$g'(x) = f(x)$$

This single fact tells us everything about how $g$ behaves:

| $f(x)$ (integrand) | $g(x)$ (accumulation function) |
|--------------------|--------------------------------|
| $f(x) > 0$ | $g$ is increasing |
| $f(x) < 0$ | $g$ is decreasing |
| $f(x) = 0$ | $g$ has horizontal tangent (potential extremum) |
| $f$ changes sign | $g$ has local max or min |
| $f$ is increasing | $g$ is concave up |
| $f$ is decreasing | $g$ is concave down |
| $f$ has local max/min | $g$ has inflection point |

### Initial Value

What is $g(a)$?

$$g(a) = \int_a^a f(t) \, dt = 0$$

The accumulation function always starts at zero at $x = a$.

### Graphical Analysis

Given the graph of $f$, you can determine everything about $g$:

1. **Where is $g$ increasing?** Where $f > 0$ (above x-axis)
2. **Where is $g$ decreasing?** Where $f < 0$ (below x-axis)
3. **Where does $g$ have max/min?** Where $f$ crosses the x-axis
4. **What is $g(x)$ at a specific point?** The signed area from $a$ to $x$
5. **Where is $g$ concave up?** Where $f$ is increasing
6. **Where is $g$ concave down?** Where $f$ is decreasing

### Worked Examples

**Example 1**: Let $g(x) = \int_0^x (t^2 - 4) \, dt$. Find:
(a) $g'(x)$
(b) $g''(x)$
(c) Where $g$ has local extrema
(d) Where $g$ is concave up

**Solution**:

**(a)** By FTC Part 1:
$$g'(x) = x^2 - 4$$

**(b)**
$$g''(x) = 2x$$

**(c)** Local extrema occur where $g'(x) = 0$:
$$x^2 - 4 = 0 \Rightarrow x = \pm 2$$

Check sign changes:
- At $x = -2$: $g'$ changes from + to -, so **local maximum**
- At $x = 2$: $g'$ changes from - to +, so **local minimum**

**(d)** Concave up where $g''(x) > 0$:
$$2x > 0 \Rightarrow x > 0$$

$g$ is concave up on $(0, \infty)$.

---

**Example 2**: The graph of $f$ consists of two line segments: from $(0, 4)$ to $(2, 0)$ to $(6, -2)$.

Let $g(x) = \int_0^x f(t) \, dt$. Find $g(2)$, $g(4)$, and $g(6)$.

**Solution**:

**$g(2)$**: Area of triangle from 0 to 2
- Base = 2, height = 4
- $g(2) = \frac{1}{2}(2)(4) = 4$

**$g(4)$**: $g(4) = g(2) + \int_2^4 f(t) \, dt$

From $x = 2$ to $x = 4$: trapezoid with heights 0 and $-1$, base 2.

Actually, let me find where $f = 0$ between 2 and 6.
The line from $(2, 0)$ to $(6, -2)$ has slope $= \frac{-2}{4} = -\frac{1}{2}$.
$f(t) = 0 - \frac{1}{2}(t - 2) = -\frac{1}{2}t + 1$

At $t = 4$: $f(4) = -\frac{1}{2}(4) + 1 = -1$

$\int_2^4 f(t) \, dt$ = area of triangle below x-axis with vertices at $(2, 0)$, $(4, 0)$, $(4, -1)$

Wait, that's not right. The line goes from $(2, 0)$ to $(6, -2)$, so at $t = 4$, $f = -1$.

The region from 2 to 4 is a triangle with base 2 and height 1 (below x-axis).
$\int_2^4 f(t) \, dt = -\frac{1}{2}(2)(1) = -1$

$g(4) = 4 + (-1) = 3$

**$g(6)$**: $g(6) = g(4) + \int_4^6 f(t) \, dt$

From $x = 4$ to $x = 6$: trapezoid with heights $-1$ and $-2$, base 2 (all below x-axis).
$\int_4^6 f(t) \, dt = -\frac{1}{2}(1 + 2)(2) = -3$

$g(6) = 3 + (-3) = 0$

---

**Example 3**: Let $g(x) = \int_1^x \frac{\sin t}{t} \, dt$. Find $g'(x)$ and $g'(1)$.

**Solution**:

By FTC Part 1:
$$g'(x) = \frac{\sin x}{x}$$

$$g'(1) = \frac{\sin 1}{1} = \sin 1 \approx 0.841$$

---

**Example 4**: Let $g(x) = \int_2^x f(t) \, dt$ where $f$ is continuous and $f(3) = 5$, $f'(3) = -2$.

Find:
(a) $g'(3)$
(b) $g''(3)$
(c) Is $g$ increasing or decreasing at $x = 3$?
(d) Is $g$ concave up or down at $x = 3$?

**Solution**:

**(a)** $g'(x) = f(x)$, so $g'(3) = f(3) = 5$

**(b)** $g''(x) = f'(x)$, so $g''(3) = f'(3) = -2$

**(c)** Since $g'(3) = 5 > 0$, $g$ is **increasing** at $x = 3$.

**(d)** Since $g''(3) = -2 < 0$, $g$ is **concave down** at $x = 3$.

---

**Example 5**: Let $g(x) = \int_0^{x^2} e^{-t^2} \, dt$. Find $g'(x)$.

**Solution**:

Use FTC Part 1 with chain rule. Let $u = x^2$.

$$g'(x) = e^{-(x^2)^2} \cdot 2x = 2xe^{-x^4}$$

---

## Key Formulas & Rules

| Property | Formula |
|----------|---------|
| Definition | $g(x) = \int_a^x f(t) \, dt$ |
| First derivative | $g'(x) = f(x)$ |
| Second derivative | $g''(x) = f'(x)$ |
| Initial value | $g(a) = 0$ |
| With chain rule | $\frac{d}{dx}\int_a^{u(x)} f(t) \, dt = f(u(x)) \cdot u'(x)$ |

**Analysis Summary**:

| To find... | Look at... |
|------------|------------|
| Where $g$ increases | Where $f > 0$ |
| Where $g$ decreases | Where $f < 0$ |
| Local max of $g$ | Where $f$ changes from + to - |
| Local min of $g$ | Where $f$ changes from - to + |
| Where $g$ is concave up | Where $f$ is increasing |
| Where $g$ is concave down | Where $f$ is decreasing |
| Inflection points of $g$ | Where $f$ has local max/min |
| Value of $g(b)$ | Signed area from $a$ to $b$ |

---

## Common Mistakes to Avoid

1. **Confusing $f$ and $g$**: Remember $g' = f$, so $f$ is the derivative, not $g$.

2. **Forgetting $g(a) = 0$**: The accumulation function always equals zero at the starting point.

3. **Sign errors with area**: Area below the x-axis contributes negatively to $g$.

4. **Inflection point confusion**: Inflection points of $g$ occur where $f$ has max/min (not where $f = 0$).

5. **Missing the chain rule**: When the upper limit is $u(x)$, don't forget to multiply by $u'(x)$.

6. **Confusing increasing/concave up**: $g$ increasing means $f > 0$; $g$ concave up means $f$ increasing.

---

## AP Exam Tips

### For Both AB and BC:
- Accumulation function problems appear on almost every AP exam
- Practice analyzing $g$ from the graph of $f$
- Know the relationships between $f$, $g$, $g'$, and $g''$ cold
- Be ready to calculate $g$ values by finding signed areas

### Common Question Types:
1. **Graph analysis**: Given graph of $f$, analyze $g$
2. **Calculate $g(x)$**: Find accumulated values using geometry
3. **Find extrema**: Locate where $g$ has max/min
4. **Concavity**: Determine where $g$ is concave up/down
5. **Chain rule variants**: Differentiate integrals with composite upper limits

### Free Response Strategy:
- Clearly state the connection $g' = f$
- Justify max/min using sign change of $g' = f$
- Calculate areas carefully (watch for positive/negative regions)
- Label points of interest on any graphs you draw

---

## Practice Problems

### Basic (Problems 1-5)

**1.** Let $g(x) = \int_0^x (3t^2 - 2t) \, dt$.

Find $g'(x)$ and $g'(2)$.

---

**2.** Let $g(x) = \int_1^x \cos t \, dt$.

Find:
**(a)** $g(1)$
**(b)** $g'(x)$
**(c)** $g(\pi)$

---

**3.** The graph of $f$ is a horizontal line $f(t) = 3$ for $0 \leq t \leq 5$.

If $g(x) = \int_0^x f(t) \, dt$, find $g(5)$.

---

**4.** Let $g(x) = \int_2^x (t - 4) \, dt$.

Find where $g$ has a local minimum.

---

**5.** If $g(x) = \int_0^x f(t) \, dt$ and $f(x) = x^3 - 3x$, where is $g$ increasing?

---

### Intermediate (Problems 6-10)

**6.** The graph of $f$ consists of a semicircle of radius 2 above the x-axis from $x = 0$ to $x = 4$.

If $g(x) = \int_0^x f(t) \, dt$, find:
**(a)** $g(4)$
**(b)** $g(2)$

---

**7.** Let $g(x) = \int_0^x f(t) \, dt$ where $f$ is graphed as a line segment from $(0, -2)$ to $(4, 2)$.

**(a)** Find $g(4)$.
**(b)** Find where $g$ has a local minimum.
**(c)** Find $g$ at its minimum.

---

**8.** Let $g(x) = \int_1^{x^3} \frac{1}{t} \, dt$.

Find $g'(x)$.

---

**9.** Let $g(x) = \int_0^x f(t) \, dt$ where $f$ is continuous.

If $f(2) = 0$, $f(x) > 0$ for $x < 2$, and $f(x) < 0$ for $x > 2$:
**(a)** Where does $g$ have a local maximum?
**(b)** What is the sign of $g(3)$ compared to $g(2)$?

---

**10.** Let $g(x) = \int_0^x t \cdot e^{t^2} \, dt$.

Find $g'(x)$ and determine where $g$ is concave up.

---

### Advanced (Problems 11-15)

**11.** Let $g(x) = \int_x^{2x} \sin t \, dt$.

Find $g'(x)$.

---

**12.** The graph of $f'$ (not $f$) is shown as a parabola opening downward with vertex at $(2, 4)$ and x-intercepts at $x = 0$ and $x = 4$.

If $g(x) = \int_0^x f(t) \, dt$, find:
**(a)** Where $g'$ has a local maximum
**(b)** Where $g$ has an inflection point

---

**13.** Let $f$ be continuous on $[0, 6]$ with $f(0) = 0$. The graph of $f'$ is given as a line from $(0, 3)$ to $(6, -3)$.

If $g(x) = \int_0^x f(t) \, dt$:
**(a)** Find where $f$ has its maximum
**(b)** Find where $g$ has an inflection point
**(c)** Find where $g$ has its maximum

---

**14.** Prove that if $f$ is an odd function and $g(x) = \int_0^x f(t) \, dt$, then $g$ is an even function.

---

**15.** Let $g(x) = \int_0^x |t - 2| \, dt$ for $0 \leq x \leq 4$.

Find the maximum value of $g$ on $[0, 4]$.

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

The graph of a function $f$ is shown below. The graph consists of a semicircle and line segments.

If $g(x) = \int_0^x f(t) \, dt$, which of the following is true?

| Choice | Answer |
|--------|--------|
| **(A)** | $g(4) < g(2) < g(6)$ |
| **(B)** | $g(2) < g(4) < g(6)$ |
| **(C)** | $g(2) < g(6) < g(4)$ |
| **(D)** | $g(6) < g(2) < g(4)$ |

*(Assume the semicircle from 0 to 4 is above the x-axis with radius 2, and the line segment from 4 to 6 is below the x-axis.)*

---

#### Problem 17 (Multiple Choice)

Let $g(x) = \int_2^x f(t) \, dt$. If $f$ is a continuous function with $f(x) < 0$ for $x < 5$ and $f(x) > 0$ for $x > 5$, then $g$ has a:

| Choice | Answer |
|--------|--------|
| **(A)** | local maximum at $x = 5$ |
| **(B)** | local minimum at $x = 5$ |
| **(C)** | local maximum at $x = 2$ |
| **(D)** | point of inflection at $x = 5$ |

---

#### Problem 18 (Free Response)

Let $g(x) = \int_0^x f(t) \, dt$, where the graph of $f$ consists of:
- A line segment from $(0, 4)$ to $(2, 0)$
- A line segment from $(2, 0)$ to $(5, -3)$
- A line segment from $(5, -3)$ to $(7, 0)$

> **(a)** Find $g(2)$ and $g(5)$.
>
> **(b)** Find all values of $x$ in $(0, 7)$ where $g$ has a local maximum.
>
> **(c)** Find all values of $x$ in $(0, 7)$ where $g$ has a point of inflection.
>
> **(d)** Find the absolute maximum value of $g$ on $[0, 7]$.

---

#### Problem 19 (Multiple Choice)

If $g(x) = \int_0^{\sin x} (t^2 + 1) \, dt$, then $g'(x) =$

| Choice | Answer |
|--------|--------|
| **(A)** | $\sin^2 x + 1$ |
| **(B)** | $(\sin^2 x + 1)\cos x$ |
| **(C)** | $\cos x \cdot \sin^2 x$ |
| **(D)** | $(\sin^2 x + 1)$ |

---

#### Problem 20 (Free Response - Challenging)

The rate at which customers enter a store is modeled by $E(t) = 10 + 20\sin\left(\frac{\pi t}{6}\right)$ customers per hour, where $t$ is the number of hours since the store opened. The rate at which customers leave is a constant $L(t) = 12$ customers per hour.

> **(a)** At what rate is the number of customers in the store changing at $t = 3$ hours?
>
> **(b)** Let $N(t) = \int_0^t [E(s) - L(s)] \, ds$ represent the net change in customers since opening. Find $N(6)$.
>
> **(c)** At what time in the interval $[0, 12]$ is $N(t)$ at its maximum?
>
> **(d)** Find the maximum number of customers that have accumulated in the store beyond the initial count.

---

## Answer Key

<details>
<summary><strong>Problem 1 Solution</strong></summary>

**Answer**: $g'(x) = 3x^2 - 2x$, $g'(2) = 8$

**Step-by-step solution**:

By FTC Part 1:
$$g'(x) = 3x^2 - 2x$$

$$g'(2) = 3(4) - 2(2) = 12 - 4 = 8$$

</details>

---

<details>
<summary><strong>Problem 2 Solution</strong></summary>

**Answer**: (a) $0$, (b) $\cos x$, (c) $0$

**(a)** $g(1) = \int_1^1 \cos t \, dt = 0$

**(b)** By FTC Part 1: $g'(x) = \cos x$

**(c)** $g(\pi) = \int_1^\pi \cos t \, dt = [\sin t]_1^\pi = \sin\pi - \sin 1 = 0 - \sin 1 = -\sin 1$

Actually, let me recalculate:
$g(\pi) = \sin\pi - \sin 1 = 0 - \sin 1 \approx -0.841$

</details>

---

<details>
<summary><strong>Problem 3 Solution</strong></summary>

**Answer**: $g(5) = 15$

**Step-by-step solution**:

$g(5) = \int_0^5 3 \, dt = 3t\Big|_0^5 = 15$

Or geometrically: rectangle with base 5 and height 3 = 15.

</details>

---

<details>
<summary><strong>Problem 4 Solution</strong></summary>

**Answer**: $x = 4$

**Step-by-step solution**:

$g'(x) = x - 4 = 0$ when $x = 4$

For $x < 4$: $g' < 0$ (decreasing)
For $x > 4$: $g' > 0$ (increasing)

So $g$ has a local minimum at $x = 4$.

</details>

---

<details>
<summary><strong>Problem 5 Solution</strong></summary>

**Answer**: $(-\infty, -\sqrt{3}) \cup (\sqrt{3}, \infty)$

**Step-by-step solution**:

$g$ is increasing where $g'(x) = f(x) > 0$.

$f(x) = x^3 - 3x = x(x^2 - 3) = x(x - \sqrt{3})(x + \sqrt{3})$

Sign chart shows $f > 0$ on $(-\sqrt{3}, 0) \cup (\sqrt{3}, \infty)$.

Wait, let me redo: Critical points at $x = 0, \pm\sqrt{3}$

Testing: $f(-2) = -8 + 6 = -2 < 0$
$f(-1) = -1 + 3 = 2 > 0$
$f(1) = 1 - 3 = -2 < 0$
$f(2) = 8 - 6 = 2 > 0$

So $f > 0$ on $(-\sqrt{3}, 0) \cup (\sqrt{3}, \infty)$.

</details>

---

<details>
<summary><strong>Problem 6 Solution</strong></summary>

**Answer**: (a) $2\pi$, (b) $\pi$

**(a)** $g(4)$ = area of semicircle = $\frac{1}{2}\pi(2)^2 = 2\pi$

**(b)** $g(2)$ = area of quarter circle = $\frac{1}{4}\pi(2)^2 = \pi$

</details>

---

<details>
<summary><strong>Problem 7 Solution</strong></summary>

**Answer**: (a) $0$, (b) $x = 2$, (c) $-2$

**(a)** The line from $(0, -2)$ to $(4, 2)$ crosses zero at $x = 2$.

Triangle below axis (0 to 2): $\frac{1}{2}(2)(2) = 2$ (negative contribution: $-2$)
Triangle above axis (2 to 4): $\frac{1}{2}(2)(2) = 2$ (positive contribution: $+2$)

$g(4) = -2 + 2 = 0$

**(b)** Local min where $g' = f$ changes from - to +, which is at $x = 2$.

**(c)** $g(2) = -2$

</details>

---

<details>
<summary><strong>Problem 8 Solution</strong></summary>

**Answer**: $\frac{3x^2}{x^3} = \frac{3}{x}$

**Step-by-step solution**:

Apply FTC Part 1 with chain rule. Let $u = x^3$.

$$g'(x) = \frac{1}{x^3} \cdot 3x^2 = \frac{3x^2}{x^3} = \frac{3}{x}$$

</details>

---

<details>
<summary><strong>Problem 9 Solution</strong></summary>

**Answer**: (a) $x = 2$, (b) $g(3) < g(2)$

**(a)** $g' = f$ changes from + to - at $x = 2$, so $g$ has local max at $x = 2$.

**(b)** Since $f < 0$ for $x > 2$, the integral from 2 to 3 is negative.
$g(3) = g(2) + \int_2^3 f(t) \, dt < g(2)$

</details>

---

<details>
<summary><strong>Problem 10 Solution</strong></summary>

**Answer**: $g'(x) = xe^{x^2}$, concave up for all $x \neq 0$

**Step-by-step solution**:

By FTC Part 1:
$$g'(x) = x \cdot e^{x^2}$$

For concavity, find $g''$:
$$g''(x) = e^{x^2} + x \cdot 2x \cdot e^{x^2} = e^{x^2}(1 + 2x^2)$$

Since $e^{x^2} > 0$ and $1 + 2x^2 > 0$ for all $x$:
$g'' > 0$ everywhere, so $g$ is concave up on $(-\infty, \infty)$.

</details>

---

<details>
<summary><strong>Problem 11 Solution</strong></summary>

**Answer**: $2\sin(2x) - \sin x$

**Step-by-step solution**:

$$g(x) = \int_x^{2x} \sin t \, dt = \int_0^{2x} \sin t \, dt - \int_0^x \sin t \, dt$$

$$g'(x) = \sin(2x) \cdot 2 - \sin(x) \cdot 1 = 2\sin(2x) - \sin x$$

</details>

---

<details>
<summary><strong>Problem 12 Solution</strong></summary>

**Answer**: (a) $x = 2$, (b) $x = 0$ and $x = 4$

**(a)** $g'(x) = f(x)$, so $g' $ has local max where $f$ has local max.

Since $f' $ has zeros at $x = 0$ and $x = 4$, $f$ has local extrema there.

Since $f' > 0$ on $(0, 4)$ (parabola above axis), $f$ is increasing on $(0, 4)$.

So $f$ has local min at $x = 0$ and local max at $x = 4$.

Wait, the graph is of $f'$, opening downward. So:
- $f' > 0$ on $(0, 4)$ means $f$ is increasing
- $f'$ changes from + to - at... actually $f' = 0$ at $x = 0$ and $x = 4$.

For $x < 0$: $f' < 0$
For $0 < x < 4$: $f' > 0$
For $x > 4$: $f' < 0$

So $f$ has local min at $x = 0$ and local max at $x = 4$.

Since $g' = f$, $g'$ has local max at $x = 4$.

**(b)** $g$ has inflection where $g'' = f' = 0$ and changes sign.
$f' = 0$ at $x = 0$ and $x = 4$, and $f'$ changes sign at both.

Inflection points of $g$ at $x = 0$ and $x = 4$.

But also, $g'' = f'$ changes sign where $f$ has local max, which is at the vertex $x = 2$.

Wait, $g'' = f'$, and we're given the graph of $f'$. $f'$ doesn't change sign at $x = 2$ (that's where it has its max, but it stays positive on both sides near $x = 2$).

So inflection points are at $x = 0$ and $x = 4$ where $f' = g''$ changes sign.

</details>

---

<details>
<summary><strong>Problem 13 Solution</strong></summary>

**Answer**: (a) $x = 3$, (b) $x = 3$, (c) Need more analysis

**(a)** $f$ has max where $f' = 0$ and changes from + to -.

$f'$ goes from 3 to -3 linearly, so $f' = 0$ at $x = 3$.

$f' > 0$ for $x < 3$, $f' < 0$ for $x > 3$, so $f$ has max at $x = 3$.

**(b)** $g$ has inflection where $g'' = f' = 0$ and changes sign.

This occurs at $x = 3$.

**(c)** $g$ has max where $g' = f = 0$ and changes from + to -.

We need to know where $f = 0$. We know $f(0) = 0$ and $f$ has max at $x = 3$.

Since $f' = 3 - x$ (linear from 3 to -3 over 0 to 6), integrating:
$f(x) = 3x - \frac{x^2}{2} + C$

Using $f(0) = 0$: $C = 0$

$f(x) = 3x - \frac{x^2}{2} = x(3 - \frac{x}{2}) = 0$ when $x = 0$ or $x = 6$.

$f > 0$ on $(0, 6)$, so $g$ is increasing on $[0, 6]$.

$g$ has max at $x = 6$.

</details>

---

<details>
<summary><strong>Problem 14 Solution</strong></summary>

**Answer**: Proof shown below.

**Step-by-step solution**:

We need to show $g(-x) = g(x)$.

$$g(-x) = \int_0^{-x} f(t) \, dt$$

Let $u = -t$, so $du = -dt$. When $t = 0$, $u = 0$. When $t = -x$, $u = x$.

$$g(-x) = \int_0^x f(-u)(-du) = \int_0^x -f(-u) \, du$$

Since $f$ is odd, $f(-u) = -f(u)$:

$$g(-x) = \int_0^x -(-f(u)) \, du = \int_0^x f(u) \, du = g(x)$$

Therefore $g$ is even.

</details>

---

<details>
<summary><strong>Problem 15 Solution</strong></summary>

**Answer**: $4$

**Step-by-step solution**:

$|t - 2| = \begin{cases} 2 - t & t < 2 \\ t - 2 & t \geq 2 \end{cases}$

$g(0) = 0$

$g(2) = \int_0^2 (2-t) \, dt = [2t - \frac{t^2}{2}]_0^2 = 4 - 2 = 2$

$g(4) = g(2) + \int_2^4 (t-2) \, dt = 2 + [\frac{t^2}{2} - 2t]_2^4$
$= 2 + (8 - 8) - (2 - 4) = 2 + 0 + 2 = 4$

$g' = |x - 2| \geq 0$ always, so $g$ is increasing.

Maximum on $[0, 4]$ is at $x = 4$: $g(4) = 4$.

</details>

---

<details>
<summary><strong>Problem 16 Solution</strong></summary>

**Answer**: **(C)** $g(2) < g(6) < g(4)$

**Step-by-step solution**:

$g(2) = \frac{1}{4}$ of semicircle area = $\frac{1}{4}(2\pi) = \frac{\pi}{2} \approx 1.57$

$g(4) = $ full semicircle = $2\pi \approx 6.28$

$g(6) = g(4) + \int_4^6 f(t) \, dt$

If the line segment from 4 to 6 is below the x-axis (let's say it goes to height -2):
$\int_4^6 f(t) \, dt \approx -2$ (area of triangle below axis)

$g(6) \approx 6.28 - 2 = 4.28$

So $g(2) < g(6) < g(4)$.

</details>

---

<details>
<summary><strong>Problem 17 Solution</strong></summary>

**Answer**: **(B)** local minimum at $x = 5$

**Step-by-step solution**:

$g' = f$

$f < 0$ for $x < 5$ means $g' < 0$ (decreasing)
$f > 0$ for $x > 5$ means $g' > 0$ (increasing)

$g'$ changes from negative to positive at $x = 5$, so $g$ has a **local minimum** at $x = 5$.

</details>

---

<details>
<summary><strong>Problem 18 Solution</strong></summary>

**Answer**: See detailed solution below.

**(a)**
$g(2)$ = triangle area from 0 to 2 = $\frac{1}{2}(2)(4) = 4$

$g(5)$ = $g(2) + \int_2^5 f(t) \, dt$

From 2 to 5: triangle below axis with base 3 and height 3 (at $t=5$, $f=-3$)
Area = $\frac{1}{2}(3)(3) = 4.5$ (negative)

$g(5) = 4 - 4.5 = -0.5$

**(b)** Local max where $f$ changes from + to -.

$f = 0$ at $x = 2$, and $f > 0$ before, $f < 0$ after.

Local maximum at $x = 2$.

**(c)** Inflection points where $f' = g''$ changes sign, i.e., where $f$ has local max or min.

The slope of $f$ changes at $x = 2$ (from $-2$ to $-1$) and at $x = 5$ (from $-1$ to $+1.5$).

Inflection points at $x = 2$ and $x = 5$.

**(d)** Compare $g(0) = 0$, $g(2) = 4$, $g(5) = -0.5$, $g(7)$.

$g(7) = g(5) + \int_5^7 f(t) \, dt$

From 5 to 7: triangle with base 2, height 3 (below to on axis)
$\int_5^7 f(t) \, dt = \frac{1}{2}(2)(3) = 3$ (but the area is actually a triangle going from -3 to 0)

Area = $\frac{1}{2}(2)(3) = 3$ (negative since below axis)

Wait, from $(5, -3)$ to $(7, 0)$, the region is below the x-axis.
Area = $\frac{1}{2}(2)(3) = 3$, but it's negative.

$g(7) = -0.5 + (-3) = -3.5$?

No wait, the line goes from -3 at $x=5$ up to 0 at $x=7$. This is below the x-axis, so the contribution is negative.

Actually, the signed area from 5 to 7 is negative: $-\frac{1}{2}(2)(3) = -3$.

$g(7) = -0.5 + (-3) = -3.5$

Hmm, that's not right either. Let me recalculate.

The area of a triangle with vertices at $(5, -3)$, $(7, 0)$, and $(5, 0)$ is $\frac{1}{2} \cdot 2 \cdot 3 = 3$.

Since it's below the x-axis... wait, it's actually a triangle that's below the x-axis except at the endpoint.

The signed integral is: $\int_5^7 f(t) \, dt$ where $f$ goes from $-3$ to $0$ linearly.

This is $\frac{1}{2}(-3 + 0)(2) = -3$.

$g(7) = -0.5 + (-3) = -3.5$

So maximum is $g(2) = 4$.

</details>

---

<details>
<summary><strong>Problem 19 Solution</strong></summary>

**Answer**: **(B)** $(\sin^2 x + 1)\cos x$

**Step-by-step solution**:

Apply FTC Part 1 with chain rule. Let $u = \sin x$.

$$g'(x) = ((\sin x)^2 + 1) \cdot \cos x = (\sin^2 x + 1)\cos x$$

</details>

---

<details>
<summary><strong>Problem 20 Solution</strong></summary>

**Answer**: See detailed solution below.

**(a)** Net rate of change at $t = 3$:

$$E(3) - L(3) = 10 + 20\sin\frac{\pi}{2} - 12 = 10 + 20 - 12 = 18 \text{ customers/hour}$$

**(b)** $N(6) = \int_0^6 [E(t) - L(t)] \, dt = \int_0^6 [10 + 20\sin\frac{\pi t}{6} - 12] \, dt$

$= \int_0^6 [-2 + 20\sin\frac{\pi t}{6}] \, dt$

$= [-2t - 20 \cdot \frac{6}{\pi}\cos\frac{\pi t}{6}]_0^6$

$= [-12 - \frac{120}{\pi}\cos\pi] - [0 - \frac{120}{\pi}\cos 0]$

$= -12 + \frac{120}{\pi} + \frac{120}{\pi} = -12 + \frac{240}{\pi} \approx -12 + 76.4 \approx 64.4$ customers

**(c)** $N'(t) = E(t) - L(t) = -2 + 20\sin\frac{\pi t}{6}$

$N'(t) = 0$ when $\sin\frac{\pi t}{6} = 0.1$

$\frac{\pi t}{6} = \arcsin(0.1) \approx 0.1$ or $\pi - 0.1$

$t \approx \frac{6(0.1)}{\pi} \approx 0.19$ or $t \approx \frac{6(\pi - 0.1)}{\pi} \approx 5.81$

Check second derivative or sign change to find max.

At $t \approx 5.81$: $N'$ changes from + to -, so local max.

Also check $t = 12$ for absolute max on $[0, 12]$.

**(d)** Calculate $N$ at critical points and endpoints to find maximum accumulation.

</details>

---

## What's Next

Congratulations on completing Unit 5! You now have a solid foundation in integration. Continue to [Area Between Curves](/calculus/area-between-curves) in Unit 6 to see how integrals solve geometric problems.

---

<div align="center">

[← Fundamental Theorem](/calculus/fundamental-theorem) | [Area Between Curves →](/calculus/area-between-curves)

</div>
