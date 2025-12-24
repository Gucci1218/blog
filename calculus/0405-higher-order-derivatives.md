# Higher-Order Derivatives
<p class="article-date">April 26, 2025</p>

The first derivative tells us about rate of change and slope. But what if we want to know how the rate of change itself is changing? That's where **higher-order derivatives** come in. The second derivative reveals concavity and acceleration, the third derivative (jerk) describes how acceleration changes, and the pattern continues. These tools are essential for curve sketching, optimization, and physics applications.

---

## What You'll Learn

- Compute second, third, and higher-order derivatives
- Understand the physical meaning of higher derivatives
- Use second derivative to determine concavity
- Find inflection points where concavity changes
- Apply the Second Derivative Test for local extrema
- Connect derivatives to position, velocity, acceleration, and jerk
- Master AP Calculus problems involving higher derivatives

---

## Prerequisites

- All differentiation rules: [Power](/calculus/0304-basic-derivative-rules), [Product](/calculus/0305-product-rule), [Quotient](/calculus/0306-quotient-rule), [Chain](/calculus/0307-chain-rule)
- [Trig Derivatives](/calculus/0402-derivatives-trig)
- [Exponential](/calculus/0403-derivatives-exp) and [Log Derivatives](/calculus/0404-derivatives-log)

---

## The Core Concept

### What Is a Higher-Order Derivative?

The **first derivative** $f'(x)$ is the derivative of $f(x)$.

The **second derivative** $f''(x)$ is the derivative of $f'(x)$.

The **third derivative** $f'''(x)$ is the derivative of $f''(x)$.

And so on!

### Notation

| Order | Prime Notation | Leibniz Notation |
|-------|---------------|------------------|
| First | $f'(x)$ | $\frac{dy}{dx}$ or $\frac{df}{dx}$ |
| Second | $f''(x)$ | $\frac{d^2y}{dx^2}$ |
| Third | $f'''(x)$ | $\frac{d^3y}{dx^3}$ |
| Fourth | $f^{(4)}(x)$ | $\frac{d^4y}{dx^4}$ |
| $n$th | $f^{(n)}(x)$ | $\frac{d^ny}{dx^n}$ |

*Note: After the third derivative, we switch to $f^{(n)}$ notation to avoid too many primes.*

### Physical Interpretation

For a position function $s(t)$:

| Derivative | Name | Meaning |
|------------|------|---------|
| $s(t)$ | Position | Where the object is |
| $s'(t) = v(t)$ | Velocity | How fast position changes |
| $s''(t) = a(t)$ | Acceleration | How fast velocity changes |
| $s'''(t) = j(t)$ | Jerk | How fast acceleration changes |

---

## Computing Higher-Order Derivatives

### Example 1: Polynomial

**Find $f'(x)$, $f''(x)$, and $f'''(x)$ for $f(x) = x^4 - 3x^3 + 2x^2 - x + 5$**

**Solution:**

$$f'(x) = 4x^3 - 9x^2 + 4x - 1$$

$$f''(x) = 12x^2 - 18x + 4$$

$$f'''(x) = 24x - 18$$

$$f^{(4)}(x) = 24$$

$$f^{(5)}(x) = 0$$

**Note:** For a polynomial of degree $n$, the $(n+1)$th derivative and beyond are all zero.

---

### Example 2: Sine Function

**Find the first four derivatives of $f(x) = \sin(x)$**

**Solution:**

$$f(x) = \sin(x)$$
$$f'(x) = \cos(x)$$
$$f''(x) = -\sin(x)$$
$$f'''(x) = -\cos(x)$$
$$f^{(4)}(x) = \sin(x)$$

**Pattern:** The derivatives of $\sin(x)$ cycle with period 4!

| $n \mod 4$ | $f^{(n)}(x)$ |
|------------|-------------|
| 0 | $\sin(x)$ |
| 1 | $\cos(x)$ |
| 2 | $-\sin(x)$ |
| 3 | $-\cos(x)$ |

---

### Example 3: Cosine Function

**Find the first four derivatives of $g(x) = \cos(x)$**

**Solution:**

$$g(x) = \cos(x)$$
$$g'(x) = -\sin(x)$$
$$g''(x) = -\cos(x)$$
$$g'''(x) = \sin(x)$$
$$g^{(4)}(x) = \cos(x)$$

**Same cycle, different starting point!**

---

### Example 4: Exponential

**Find $f^{(n)}(x)$ for $f(x) = e^x$**

**Solution:**

$$f(x) = e^x$$
$$f'(x) = e^x$$
$$f''(x) = e^x$$
$$f'''(x) = e^x$$

**Pattern:** Every derivative of $e^x$ is $e^x$!

$$f^{(n)}(x) = e^x \text{ for all } n$$

---

### Example 5: Exponential with Chain Rule

**Find the first three derivatives of $f(x) = e^{3x}$**

**Solution:**

$$f(x) = e^{3x}$$
$$f'(x) = 3e^{3x}$$
$$f''(x) = 9e^{3x}$$
$$f'''(x) = 27e^{3x}$$

**Pattern:** $f^{(n)}(x) = 3^n e^{3x}$

---

### Example 6: Natural Log

**Find $f''(x)$ for $f(x) = \ln(x)$**

**Solution:**

$$f(x) = \ln(x)$$
$$f'(x) = \frac{1}{x} = x^{-1}$$
$$f''(x) = -x^{-2} = -\frac{1}{x^2}$$
$$f'''(x) = 2x^{-3} = \frac{2}{x^3}$$

**Pattern:** $f^{(n)}(x) = \frac{(-1)^{n-1}(n-1)!}{x^n}$ for $n \geq 1$

---

### Example 7: Product Rule Needed

**Find $f''(x)$ for $f(x) = x^2 e^x$**

**Solution:**

**First derivative (product rule):**
$$f'(x) = 2xe^x + x^2e^x = e^x(2x + x^2)$$

**Second derivative (product rule again):**
$$f''(x) = e^x(2x + x^2) + e^x(2 + 2x)$$
$$= e^x(2x + x^2 + 2 + 2x)$$
$$= e^x(x^2 + 4x + 2)$$

**Answer:** $f''(x) = e^x(x^2 + 4x + 2)$

---

### Example 8: Trig with Chain Rule

**Find $f''(x)$ for $f(x) = \sin(2x)$**

**Solution:**

$$f(x) = \sin(2x)$$
$$f'(x) = 2\cos(2x)$$
$$f''(x) = 2 \cdot (-\sin(2x)) \cdot 2 = -4\sin(2x)$$

**Answer:** $f''(x) = -4\sin(2x)$

**Note:** $f''(x) = -4f(x)$. This is characteristic of simple harmonic motion!

---

## The Second Derivative and Concavity

### What Concavity Means

- **Concave up** ($f'' > 0$): The graph curves upward like a smile 😊. Slopes are increasing.
- **Concave down** ($f'' < 0$): The graph curves downward like a frown 😞. Slopes are decreasing.

### The Second Derivative Test for Concavity

$$\boxed{f''(x) > 0 \implies \text{concave up at } x}$$

$$\boxed{f''(x) < 0 \implies \text{concave down at } x}$$

---

### Example 9: Finding Concavity Intervals

**Find where $f(x) = x^3 - 6x^2 + 9x + 1$ is concave up and concave down.**

**Solution:**

$$f'(x) = 3x^2 - 12x + 9$$
$$f''(x) = 6x - 12$$

Set $f''(x) = 0$: $6x - 12 = 0 \Rightarrow x = 2$

**Test intervals:**

| Interval | Test point | $f''$ | Concavity |
|----------|-----------|-------|-----------|
| $(-\infty, 2)$ | $x = 0$ | $-12 < 0$ | Down |
| $(2, \infty)$ | $x = 3$ | $6 > 0$ | Up |

**Answer:** Concave down on $(-\infty, 2)$, concave up on $(2, \infty)$

---

## Inflection Points

### Definition

An **inflection point** is where the concavity changes (from up to down or down to up).

### How to Find Inflection Points

1. Find where $f''(x) = 0$ or $f''(x)$ is undefined
2. Check that concavity actually changes at these points

---

### Example 10: Finding Inflection Points

**Find the inflection point(s) of $f(x) = x^3 - 6x^2 + 9x + 1$**

**Solution:**

From Example 9: $f''(x) = 6x - 12 = 0$ at $x = 2$

Concavity changes from down to up at $x = 2$. ✓

$f(2) = 8 - 24 + 18 + 1 = 3$

**Answer:** Inflection point at $(2, 3)$

---

### Example 11: Multiple Inflection Points

**Find all inflection points of $f(x) = x^4 - 4x^3$**

**Solution:**

$$f'(x) = 4x^3 - 12x^2$$
$$f''(x) = 12x^2 - 24x = 12x(x - 2)$$

$f''(x) = 0$ when $x = 0$ or $x = 2$

**Check sign changes:**

| Interval | Sign of $f''$ |
|----------|---------------|
| $x < 0$ | $12(-)(-)= +$ |
| $0 < x < 2$ | $12(+)(-)= -$ |
| $x > 2$ | $12(+)(+)= +$ |

Concavity changes at both $x = 0$ and $x = 2$. ✓

$f(0) = 0$ and $f(2) = 16 - 32 = -16$

**Answer:** Inflection points at $(0, 0)$ and $(2, -16)$

---

## The Second Derivative Test for Extrema

### The Test

If $f'(c) = 0$:

- If $f''(c) > 0$: **Local minimum** at $x = c$ (concave up)
- If $f''(c) < 0$: **Local maximum** at $x = c$ (concave down)
- If $f''(c) = 0$: **Test inconclusive** (use First Derivative Test)

---

### Example 12: Using Second Derivative Test

**Find and classify all local extrema of $f(x) = x^3 - 3x^2 - 9x + 5$**

**Solution:**

$$f'(x) = 3x^2 - 6x - 9 = 3(x^2 - 2x - 3) = 3(x-3)(x+1)$$

Critical points: $x = 3$ and $x = -1$

$$f''(x) = 6x - 6$$

**Test each critical point:**

- At $x = 3$: $f''(3) = 18 - 6 = 12 > 0$ → **Local minimum**
- At $x = -1$: $f''(-1) = -6 - 6 = -12 < 0$ → **Local maximum**

$f(3) = 27 - 27 - 27 + 5 = -22$
$f(-1) = -1 - 3 + 9 + 5 = 10$

**Answer:** Local max at $(-1, 10)$, local min at $(3, -22)$

---

### Example 13: When Second Derivative Test Fails

**Classify the critical point of $f(x) = x^4$**

**Solution:**

$$f'(x) = 4x^3 = 0 \Rightarrow x = 0$$
$$f''(x) = 12x^2$$
$$f''(0) = 0$$ — **Inconclusive!**

Use First Derivative Test:
- For $x < 0$: $f'(x) < 0$ (decreasing)
- For $x > 0$: $f'(x) > 0$ (increasing)

**Answer:** Local minimum at $x = 0$ (even though $f''(0) = 0$)

---

## Motion Problems

### Example 14: Position, Velocity, Acceleration

**A particle moves along a line with position $s(t) = t^3 - 6t^2 + 9t$ meters at time $t$ seconds.**

**Find:**
**(a)** Velocity and acceleration functions
**(b)** When is the particle at rest?
**(c)** When is the particle moving right/left?
**(d)** When is the particle speeding up/slowing down?

**Solution:**

**(a)**
$$v(t) = s'(t) = 3t^2 - 12t + 9 = 3(t-1)(t-3)$$
$$a(t) = v'(t) = 6t - 12 = 6(t - 2)$$

**(b)** At rest when $v(t) = 0$: $t = 1$ and $t = 3$ seconds

**(c)**
| Interval | $v(t)$ | Direction |
|----------|--------|-----------|
| $0 < t < 1$ | $+$ | Right |
| $1 < t < 3$ | $-$ | Left |
| $t > 3$ | $+$ | Right |

**(d)** Speeding up when $v$ and $a$ have the same sign:

| Interval | $v$ | $a$ | Speed |
|----------|-----|-----|-------|
| $0 < t < 1$ | $+$ | $-$ | Slowing |
| $1 < t < 2$ | $-$ | $-$ | Speeding up |
| $2 < t < 3$ | $-$ | $+$ | Slowing |
| $t > 3$ | $+$ | $+$ | Speeding up |

---

### Example 15: Simple Harmonic Motion

**Show that $x(t) = A\cos(\omega t)$ satisfies $x''(t) = -\omega^2 x(t)$**

**Solution:**

$$x(t) = A\cos(\omega t)$$
$$x'(t) = -A\omega\sin(\omega t)$$
$$x''(t) = -A\omega^2\cos(\omega t) = -\omega^2 \cdot A\cos(\omega t) = -\omega^2 x(t)$$

**This is the defining equation of simple harmonic motion!** The acceleration is proportional to displacement and always directed toward equilibrium.

---

## Special Patterns

### Example 16: $n$th Derivative of $x^n$

**Find $f^{(n)}(x)$ for $f(x) = x^n$**

**Pattern:**
$$f(x) = x^n$$
$$f'(x) = nx^{n-1}$$
$$f''(x) = n(n-1)x^{n-2}$$
$$f'''(x) = n(n-1)(n-2)x^{n-3}$$
$$\vdots$$
$$f^{(n)}(x) = n! \cdot x^0 = n!$$
$$f^{(n+1)}(x) = 0$$

---

### Example 17: General Pattern for $e^{ax}$

**Find $f^{(n)}(x)$ for $f(x) = e^{ax}$**

$$f^{(n)}(x) = a^n e^{ax}$$

**Proof by pattern:**
$$f(x) = e^{ax}$$
$$f'(x) = ae^{ax}$$
$$f''(x) = a^2e^{ax}$$
$$f^{(n)}(x) = a^n e^{ax}$$

---

## Implicit Second Derivatives

### Example 18: Second Derivative Implicitly

**Find $\frac{d^2y}{dx^2}$ for $x^2 + y^2 = 25$**

**Solution:**

**First derivative:**

$$2x + 2y\frac{dy}{dx} = 0$$
$$\frac{dy}{dx} = -\frac{x}{y}$$

**Second derivative (differentiate $\frac{dy}{dx}$ using quotient rule):**

$$\frac{d^2y}{dx^2} = -\frac{y \cdot 1 - x \cdot \frac{dy}{dx}}{y^2}$$

**Substitute $\frac{dy}{dx} = -\frac{x}{y}$:**

$$= -\frac{y - x \cdot \left(-\frac{x}{y}\right)}{y^2} = -\frac{y + \frac{x^2}{y}}{y^2}$$

$$= -\frac{\frac{y^2 + x^2}{y}}{y^2} = -\frac{y^2 + x^2}{y^3}$$

Since $x^2 + y^2 = 25$:

$$\frac{d^2y}{dx^2} = -\frac{25}{y^3}$$

**Answer:** $\frac{d^2y}{dx^2} = -\frac{25}{y^3}$

---

## Key Formulas & Rules

### Essential Facts

| Function | Second Derivative |
|----------|-------------------|
| $x^n$ | $n(n-1)x^{n-2}$ |
| $e^x$ | $e^x$ |
| $e^{ax}$ | $a^2 e^{ax}$ |
| $\ln(x)$ | $-\frac{1}{x^2}$ |
| $\sin(x)$ | $-\sin(x)$ |
| $\cos(x)$ | $-\cos(x)$ |
| $\sin(ax)$ | $-a^2\sin(ax)$ |
| $\cos(ax)$ | $-a^2\cos(ax)$ |

### Second Derivative Test Summary

| $f'(c)$ | $f''(c)$ | Conclusion |
|---------|----------|------------|
| $0$ | $> 0$ | Local minimum |
| $0$ | $< 0$ | Local maximum |
| $0$ | $= 0$ | Inconclusive |

### Concavity Summary

| $f''(x)$ | Concavity | Graph Shape |
|----------|-----------|-------------|
| $> 0$ | Up | ∪ (smile) |
| $< 0$ | Down | ∩ (frown) |
| Changes sign | Inflection point | |

---

## Common Mistakes to Avoid

### Mistake 1: Forgetting Chain Rule on Second Derivative

**Wrong:**

$$f(x) = \sin(3x), \quad f''(x) = -\sin(3x) \quad \text{✗}$$

**Right:**

$$f'(x) = 3\cos(3x), \quad f''(x) = -9\sin(3x) \quad \text{✓}$$

---

### Mistake 2: Second Derivative ≠ First Derivative Squared

**Wrong:**

$$f''(x) = [f'(x)]^2 \quad \text{✗}$$

$f''(x)$ is the derivative OF $f'(x)$, not the square!

---

### Mistake 3: Assuming $f''(c) = 0$ Means Inflection Point

$f''(c) = 0$ is **necessary** but not **sufficient** for an inflection point. You must verify that concavity actually changes.

**Counterexample:** $f(x) = x^4$ has $f''(0) = 0$ but no inflection at $x = 0$.

---

### Mistake 4: Confusing Speed and Velocity

- **Velocity** can be negative (direction matters)
- **Speed** = $|v(t)|$ is always non-negative

"Speeding up" means speed is increasing, not velocity!

---

## AP Exam Tips

### Must-Know Skills

1. Computing second derivatives accurately
2. Finding concavity intervals
3. Locating inflection points
4. Applying the Second Derivative Test
5. Motion problems: position → velocity → acceleration

### Common Question Types

1. **Find $f''(x)$** — direct computation
2. **Concavity intervals** — where is $f'' > 0$ or $f'' < 0$?
3. **Inflection points** — where does concavity change?
4. **Classify extrema** — Second Derivative Test
5. **Motion analysis** — when speeding up/slowing down?
6. **Implicit second derivatives** — for curves like circles

### Speed Tips

1. **For trig:** Second derivative of $\sin(ax)$ is $-a^2\sin(ax)$
2. **For exponentials:** Second derivative of $e^{ax}$ is $a^2 e^{ax}$
3. **For inflection points:** Find where $f'' = 0$, verify sign change

---

## Practice Problems

### Basic (Problems 1-5)

**1.** Find $f''(x)$ for:

$$f(x) = x^5 - 3x^3 + 2x$$

---

**2.** Find $g''(x)$ for:

$$g(x) = \cos(x)$$

---

**3.** Find $h''(x)$ for:

$$h(x) = e^{2x}$$

---

**4.** Find $f''(x)$ for:

$$f(x) = \ln(x)$$

---

**5.** Find the third derivative of:

$$g(x) = x^4 - 2x^2 + 1$$

---

### Intermediate (Problems 6-10)

**6.** Find all inflection points of:

$$f(x) = x^3 - 3x^2 + 2$$

---

**7.** Use the Second Derivative Test to classify the critical points of:

$$g(x) = x^3 - 12x$$

---

**8.** Find $f''(x)$ for:

$$f(x) = x^2\sin(x)$$

---

**9.** A particle has position $s(t) = t^3 - 9t^2 + 24t$. Find when the particle is speeding up.

---

**10.** Find the intervals where $f(x) = xe^x$ is concave up and concave down.

---

### Advanced (Problems 11-15)

**11.** Find $\frac{d^2y}{dx^2}$ for:

$$x^3 + y^3 = 6xy$$

at the point $(3, 3)$.

---

**12.** Find the $n$th derivative of:

$$f(x) = \sin(2x)$$

---

**13.** For $f(x) = x^4 - 4x^3 + 6x^2$, find all inflection points and determine where the graph is concave up/down.

---

**14.** Show that $y = e^{-x}\cos(x)$ satisfies $y'' + 2y' + 2y = 0$.

---

**15.** Find $f''(1)$ for:

$$f(x) = x^x$$

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

If $f(x) = x^4 - 6x^2$, then the graph of $f$ has inflection points at $x =$

| Choice | Answer |
|--------|--------|
| **(A)** | $-1$ only |
| **(B)** | $1$ only |
| **(C)** | $-1$ and $1$ |
| **(D)** | $0$ only |

---

#### Problem 17 (Multiple Choice)

The function $f(x) = xe^{-x}$ has a local maximum at:

| Choice | Answer |
|--------|--------|
| **(A)** | $x = 0$ |
| **(B)** | $x = 1$ |
| **(C)** | $x = -1$ |
| **(D)** | $f$ has no local maximum |

---

#### Problem 18 (Free Response)

Let $f(x) = x^3 - 6x^2 + 9x + 2$.

> **(a)** Find all critical points and classify each as a local max, local min, or neither.
>
> **(b)** Find all inflection points.
>
> **(c)** On what intervals is the graph of $f$ concave up? Concave down?

---

#### Problem 19 (Multiple Choice)

A particle moves along the x-axis with velocity $v(t) = t^2 - 4t + 3$. The particle is speeding up for:

| Choice | Answer |
|--------|--------|
| **(A)** | $0 < t < 1$ |
| **(B)** | $1 < t < 2$ |
| **(C)** | $2 < t < 3$ |
| **(D)** | $t > 3$ |

---

#### Problem 20 (Free Response - Challenging)

Let $f(x) = \frac{x^2}{x^2 + 3}$.

> **(a)** Find $f'(x)$ and $f''(x)$.
>
> **(b)** Find all critical points and use the Second Derivative Test to classify them.
>
> **(c)** Find all inflection points and determine the intervals of concavity.
>
> **(d)** Find $\lim_{x \to \infty} f(x)$ and $\lim_{x \to -\infty} f(x)$. Sketch the graph.

---

## Solutions

<details>
<summary><strong>Solution 1</strong></summary>

**Problem:** $f(x) = x^5 - 3x^3 + 2x$

$$f'(x) = 5x^4 - 9x^2 + 2$$
$$f''(x) = 20x^3 - 18x$$

**Answer:** $f''(x) = 20x^3 - 18x$

</details>

---

<details>
<summary><strong>Solution 2</strong></summary>

**Problem:** $g(x) = \cos(x)$

$$g'(x) = -\sin(x)$$
$$g''(x) = -\cos(x)$$

**Answer:** $g''(x) = -\cos(x)$

</details>

---

<details>
<summary><strong>Solution 3</strong></summary>

**Problem:** $h(x) = e^{2x}$

$$h'(x) = 2e^{2x}$$
$$h''(x) = 4e^{2x}$$

**Answer:** $h''(x) = 4e^{2x}$

</details>

---

<details>
<summary><strong>Solution 4</strong></summary>

**Problem:** $f(x) = \ln(x)$

$$f'(x) = \frac{1}{x} = x^{-1}$$
$$f''(x) = -x^{-2} = -\frac{1}{x^2}$$

**Answer:** $f''(x) = -\frac{1}{x^2}$

</details>

---

<details>
<summary><strong>Solution 5</strong></summary>

**Problem:** Third derivative of $g(x) = x^4 - 2x^2 + 1$

$$g'(x) = 4x^3 - 4x$$
$$g''(x) = 12x^2 - 4$$
$$g'''(x) = 24x$$

**Answer:** $g'''(x) = 24x$

</details>

---

<details>
<summary><strong>Solution 6</strong></summary>

**Problem:** Inflection points of $f(x) = x^3 - 3x^2 + 2$

$$f'(x) = 3x^2 - 6x$$
$$f''(x) = 6x - 6 = 6(x - 1)$$

$f''(x) = 0$ when $x = 1$

Check sign change:
- $x < 1$: $f'' < 0$ (concave down)
- $x > 1$: $f'' > 0$ (concave up)

Concavity changes ✓

$f(1) = 1 - 3 + 2 = 0$

**Answer:** Inflection point at $(1, 0)$

</details>

---

<details>
<summary><strong>Solution 7</strong></summary>

**Problem:** Classify critical points of $g(x) = x^3 - 12x$

$$g'(x) = 3x^2 - 12 = 3(x^2 - 4) = 3(x-2)(x+2)$$

Critical points: $x = 2$ and $x = -2$

$$g''(x) = 6x$$

- At $x = 2$: $g''(2) = 12 > 0$ → **Local minimum**
- At $x = -2$: $g''(-2) = -12 < 0$ → **Local maximum**

**Answer:** Local max at $x = -2$, local min at $x = 2$

</details>

---

<details>
<summary><strong>Solution 8</strong></summary>

**Problem:** $f(x) = x^2\sin(x)$

**First derivative (product rule):**

$$f'(x) = 2x\sin(x) + x^2\cos(x)$$

**Second derivative (product rule on each term):**

$$f''(x) = 2\sin(x) + 2x\cos(x) + 2x\cos(x) + x^2(-\sin(x))$$
$$= 2\sin(x) + 4x\cos(x) - x^2\sin(x)$$
$$= (2 - x^2)\sin(x) + 4x\cos(x)$$

**Answer:** $f''(x) = (2 - x^2)\sin(x) + 4x\cos(x)$

</details>

---

<details>
<summary><strong>Solution 9</strong></summary>

**Problem:** $s(t) = t^3 - 9t^2 + 24t$, when speeding up?

$$v(t) = 3t^2 - 18t + 24 = 3(t^2 - 6t + 8) = 3(t-2)(t-4)$$
$$a(t) = 6t - 18 = 6(t - 3)$$

| Interval | $v(t)$ | $a(t)$ | Same sign? |
|----------|--------|--------|------------|
| $0 < t < 2$ | $+$ | $-$ | No (slowing) |
| $2 < t < 3$ | $-$ | $-$ | Yes (speeding up) |
| $3 < t < 4$ | $-$ | $+$ | No (slowing) |
| $t > 4$ | $+$ | $+$ | Yes (speeding up) |

**Answer:** Speeding up on $(2, 3)$ and $(4, \infty)$

</details>

---

<details>
<summary><strong>Solution 10</strong></summary>

**Problem:** Concavity of $f(x) = xe^x$

$$f'(x) = e^x + xe^x = e^x(1 + x)$$
$$f''(x) = e^x(1 + x) + e^x = e^x(2 + x)$$

$f''(x) = 0$ when $x = -2$

Since $e^x > 0$ always:
- $x < -2$: $f'' < 0$ (concave down)
- $x > -2$: $f'' > 0$ (concave up)

**Answer:** Concave down on $(-\infty, -2)$, concave up on $(-2, \infty)$

</details>

---

<details>
<summary><strong>Solution 11</strong></summary>

**Problem:** $\frac{d^2y}{dx^2}$ for $x^3 + y^3 = 6xy$ at $(3, 3)$

**First derivative:**

$$3x^2 + 3y^2\frac{dy}{dx} = 6y + 6x\frac{dy}{dx}$$
$$(3y^2 - 6x)\frac{dy}{dx} = 6y - 3x^2$$
$$\frac{dy}{dx} = \frac{6y - 3x^2}{3y^2 - 6x} = \frac{2y - x^2}{y^2 - 2x}$$

At $(3, 3)$: $\frac{dy}{dx} = \frac{6 - 9}{9 - 6} = \frac{-3}{3} = -1$

**Second derivative (use quotient rule on $\frac{dy}{dx}$):**

Let $u = 2y - x^2$, $v = y^2 - 2x$

$$\frac{d^2y}{dx^2} = \frac{u'v - uv'}{v^2}$$

$u' = 2\frac{dy}{dx} - 2x$, $v' = 2y\frac{dy}{dx} - 2$

At $(3, 3)$ with $\frac{dy}{dx} = -1$:
- $u' = 2(-1) - 6 = -8$
- $v' = 6(-1) - 2 = -8$
- $u = -3$, $v = 3$

$$\frac{d^2y}{dx^2} = \frac{(-8)(3) - (-3)(-8)}{9} = \frac{-24 - 24}{9} = \frac{-48}{9} = -\frac{16}{3}$$

**Answer:** $\frac{d^2y}{dx^2} = -\frac{16}{3}$

</details>

---

<details>
<summary><strong>Solution 12</strong></summary>

**Problem:** $n$th derivative of $f(x) = \sin(2x)$

The pattern:
- $f(x) = \sin(2x)$
- $f'(x) = 2\cos(2x)$
- $f''(x) = -4\sin(2x)$
- $f'''(x) = -8\cos(2x)$
- $f^{(4)}(x) = 16\sin(2x)$

**Pattern:** $f^{(n)}(x) = 2^n \sin\left(2x + \frac{n\pi}{2}\right)$

Or equivalently:

| $n \mod 4$ | $f^{(n)}(x)$ |
|------------|-------------|
| 0 | $2^n\sin(2x)$ |
| 1 | $2^n\cos(2x)$ |
| 2 | $-2^n\sin(2x)$ |
| 3 | $-2^n\cos(2x)$ |

</details>

---

<details>
<summary><strong>Solution 13</strong></summary>

**Problem:** Inflection points of $f(x) = x^4 - 4x^3 + 6x^2$

$$f'(x) = 4x^3 - 12x^2 + 12x$$
$$f''(x) = 12x^2 - 24x + 12 = 12(x^2 - 2x + 1) = 12(x-1)^2$$

$f''(x) = 0$ when $x = 1$

But $(x-1)^2 \geq 0$ for all $x$, so $f''(x) \geq 0$ always.

Concavity never changes — always concave up!

**Answer:** No inflection points. Concave up on $(-\infty, \infty)$.

</details>

---

<details>
<summary><strong>Solution 14</strong></summary>

**Problem:** Show $y = e^{-x}\cos(x)$ satisfies $y'' + 2y' + 2y = 0$

**Find $y'$ (product rule):**

$$y' = -e^{-x}\cos(x) + e^{-x}(-\sin(x)) = -e^{-x}(\cos(x) + \sin(x))$$

**Find $y''$:**

$$y'' = e^{-x}(\cos(x) + \sin(x)) + (-e^{-x})(-\sin(x) + \cos(x))$$
$$= e^{-x}(\cos(x) + \sin(x) + \sin(x) - \cos(x))$$
$$= 2e^{-x}\sin(x)$$

**Check $y'' + 2y' + 2y$:**

$$= 2e^{-x}\sin(x) + 2(-e^{-x})(\cos(x) + \sin(x)) + 2e^{-x}\cos(x)$$
$$= 2e^{-x}\sin(x) - 2e^{-x}\cos(x) - 2e^{-x}\sin(x) + 2e^{-x}\cos(x)$$
$$= 0$$ ✓

</details>

---

<details>
<summary><strong>Solution 15</strong></summary>

**Problem:** $f''(1)$ for $f(x) = x^x$

From log differentiation: $f'(x) = x^x(\ln(x) + 1)$

**Find $f''(x)$:**

$$f''(x) = f'(x)(\ln(x) + 1) + x^x \cdot \frac{1}{x}$$
$$= x^x(\ln(x) + 1)^2 + x^{x-1}$$

At $x = 1$:

$$f''(1) = 1^1(\ln(1) + 1)^2 + 1^0 = 1 \cdot 1 + 1 = 2$$

**Answer:** $f''(1) = 2$

</details>

---

<details>
<summary><strong>Solution 16</strong></summary>

**Problem:** Inflection points of $f(x) = x^4 - 6x^2$

$$f'(x) = 4x^3 - 12x$$
$$f''(x) = 12x^2 - 12 = 12(x^2 - 1) = 12(x-1)(x+1)$$

$f''(x) = 0$ when $x = 1$ or $x = -1$

Sign changes at both points ✓

**Answer:** **(C)** $-1$ and $1$

</details>

---

<details>
<summary><strong>Solution 17</strong></summary>

**Problem:** Local max of $f(x) = xe^{-x}$

$$f'(x) = e^{-x} - xe^{-x} = e^{-x}(1 - x)$$

$f'(x) = 0$ when $x = 1$

$$f''(x) = -e^{-x}(1-x) + e^{-x}(-1) = e^{-x}(x - 2)$$

$f''(1) = e^{-1}(-1) < 0$ → Local maximum ✓

**Answer:** **(B)** $x = 1$

</details>

---

<details>
<summary><strong>Solution 18</strong></summary>

**Problem:** $f(x) = x^3 - 6x^2 + 9x + 2$

**(a) Critical points:**

$$f'(x) = 3x^2 - 12x + 9 = 3(x^2 - 4x + 3) = 3(x-1)(x-3)$$

Critical points: $x = 1$ and $x = 3$

$$f''(x) = 6x - 12$$

- $f''(1) = -6 < 0$ → Local max at $x = 1$, $f(1) = 1 - 6 + 9 + 2 = 6$
- $f''(3) = 6 > 0$ → Local min at $x = 3$, $f(3) = 27 - 54 + 27 + 2 = 2$

**(b) Inflection points:**

$f''(x) = 0$ when $x = 2$

$f(2) = 8 - 24 + 18 + 2 = 4$

**Inflection point at $(2, 4)$**

**(c) Concavity:**

- $x < 2$: $f'' < 0$, concave down
- $x > 2$: $f'' > 0$, concave up

</details>

---

<details>
<summary><strong>Solution 19</strong></summary>

**Problem:** $v(t) = t^2 - 4t + 3 = (t-1)(t-3)$

$v(t) = 0$ at $t = 1, 3$

$a(t) = 2t - 4 = 0$ at $t = 2$

| Interval | $v$ | $a$ | Speeding up? |
|----------|-----|-----|--------------|
| $0 < t < 1$ | $+$ | $-$ | No |
| $1 < t < 2$ | $-$ | $-$ | Yes |
| $2 < t < 3$ | $-$ | $+$ | No |
| $t > 3$ | $+$ | $+$ | Yes |

**Answer:** **(B)** $1 < t < 2$ (also $t > 3$ but not listed)

</details>

---

<details>
<summary><strong>Solution 20</strong></summary>

**Problem:** $f(x) = \frac{x^2}{x^2 + 3}$

**(a) Derivatives:**

$$f'(x) = \frac{2x(x^2+3) - x^2(2x)}{(x^2+3)^2} = \frac{2x^3 + 6x - 2x^3}{(x^2+3)^2} = \frac{6x}{(x^2+3)^2}$$

$$f''(x) = \frac{6(x^2+3)^2 - 6x \cdot 2(x^2+3)(2x)}{(x^2+3)^4}$$
$$= \frac{6(x^2+3) - 24x^2}{(x^2+3)^3} = \frac{6x^2 + 18 - 24x^2}{(x^2+3)^3} = \frac{18 - 18x^2}{(x^2+3)^3}$$
$$= \frac{18(1-x^2)}{(x^2+3)^3}$$

**(b) Critical points:**

$f'(x) = 0$ when $x = 0$

$f''(0) = \frac{18}{27} = \frac{2}{3} > 0$ → Local minimum at $x = 0$

**(c) Inflection points:**

$f''(x) = 0$ when $1 - x^2 = 0$, so $x = \pm 1$

- $|x| < 1$: $f'' > 0$, concave up
- $|x| > 1$: $f'' < 0$, concave down

Inflection points at $x = -1$ and $x = 1$

$f(\pm 1) = \frac{1}{4}$

**(d) Limits and sketch:**

$$\lim_{x \to \pm\infty} \frac{x^2}{x^2+3} = \lim_{x \to \pm\infty} \frac{1}{1 + 3/x^2} = 1$$

Horizontal asymptote at $y = 1$

The graph has a minimum at $(0, 0)$, inflection points at $(\pm 1, 1/4)$, and approaches $y = 1$ as $x \to \pm\infty$.

</details>

---

## What's Next

Congratulations! You've completed **Unit 3: Advanced Derivatives**. You now have all the differentiation tools needed for calculus. Next up is **Unit 4: Applications of Derivatives**, starting with [Motion](/calculus/0501-motion) where you'll apply derivatives to real-world problems involving position, velocity, and acceleration.

---

<div align="center">

[← Log Derivatives](/calculus/0404-derivatives-log) | [Unit 4: Motion →](/calculus/0501-motion)

</div>
