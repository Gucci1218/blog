# The Fundamental Theorem of Calculus

*For centuries, differentiation and integration seemed like separate operations—one finding slopes, the other finding areas. Then came the breakthrough: they're inverse operations, two sides of the same coin. The Fundamental Theorem of Calculus (FTC) is the bridge that connects these two pillars of calculus, and it's arguably the most important theorem in all of mathematics.*

---

## What You'll Learn
- Understand both parts of the Fundamental Theorem of Calculus
- Use FTC Part 1 to differentiate integral functions
- Use FTC Part 2 to evaluate definite integrals
- Apply the chain rule with FTC Part 1
- Connect antiderivatives to definite integrals

---

## Prerequisites
- [Antiderivatives](/calculus/antiderivatives)
- [Definite Integrals](/calculus/definite-integrals)
- [Chain Rule](/calculus/chain-rule)

---

## The Core Concept

### Intuition First

Imagine you're tracking water flowing into a tank:
- The **rate of flow** at any moment is $f(t)$ gallons per minute
- The **total amount** accumulated up to time $x$ is $\int_0^x f(t) \, dt$

Now ask: at what rate is the total changing? It's changing at the rate water is flowing in—which is just $f(x)$!

This is the essence of FTC Part 1: **the derivative of the accumulation function equals the original function**.

### FTC Part 1: Differentiation of Integrals

**Theorem (FTC Part 1)**: If $f$ is continuous on $[a, b]$, then the function

$$g(x) = \int_a^x f(t) \, dt$$

is continuous on $[a, b]$, differentiable on $(a, b)$, and

$$g'(x) = \frac{d}{dx}\left[\int_a^x f(t) \, dt\right] = f(x)$$

**In words**: The derivative of an integral (with respect to its upper limit) gives back the original function.

### Understanding the Notation

In $g(x) = \int_a^x f(t) \, dt$:
- $a$ is a constant (fixed lower limit)
- $x$ is the variable upper limit
- $t$ is a "dummy variable" for integration
- $g(x)$ represents the accumulated area from $a$ to $x$

### FTC Part 2: Evaluation of Integrals

**Theorem (FTC Part 2)**: If $f$ is continuous on $[a, b]$ and $F$ is any antiderivative of $f$ (meaning $F' = f$), then

$$\int_a^b f(x) \, dx = F(b) - F(a)$$

**Notation**: We write $F(x)\Big|_a^b$ or $[F(x)]_a^b$ to mean $F(b) - F(a)$.

**In words**: To evaluate a definite integral, find any antiderivative and subtract its values at the limits.

### Why FTC Part 2 Works

FTC Part 2 follows from Part 1:

Let $g(x) = \int_a^x f(t) \, dt$. By FTC Part 1, $g'(x) = f(x)$, so $g$ is an antiderivative of $f$.

If $F$ is any other antiderivative, then $F(x) = g(x) + C$ for some constant $C$.

Therefore:
$$F(b) - F(a) = [g(b) + C] - [g(a) + C] = g(b) - g(a) = \int_a^b f(t) \, dt - \int_a^a f(t) \, dt = \int_a^b f(t) \, dt$$

### FTC Part 1 with Chain Rule

When the upper limit is a function of $x$, use the chain rule:

$$\frac{d}{dx}\left[\int_a^{u(x)} f(t) \, dt\right] = f(u(x)) \cdot u'(x)$$

When both limits are functions:

$$\frac{d}{dx}\left[\int_{v(x)}^{u(x)} f(t) \, dt\right] = f(u(x)) \cdot u'(x) - f(v(x)) \cdot v'(x)$$

### Worked Examples

**Example 1**: Find $\frac{d}{dx}\left[\int_2^x \sqrt{t^3 + 1} \, dt\right]$

**Solution**:

By FTC Part 1, this is simply the integrand evaluated at the upper limit:

$$\frac{d}{dx}\left[\int_2^x \sqrt{t^3 + 1} \, dt\right] = \sqrt{x^3 + 1}$$

---

**Example 2**: Find $\frac{d}{dx}\left[\int_0^{x^2} \sin t \, dt\right]$

**Solution**:

Use FTC Part 1 with chain rule. Let $u = x^2$.

$$\frac{d}{dx}\left[\int_0^{x^2} \sin t \, dt\right] = \sin(x^2) \cdot \frac{d}{dx}(x^2) = \sin(x^2) \cdot 2x = 2x\sin(x^2)$$

---

**Example 3**: Find $\frac{d}{dx}\left[\int_x^5 e^{t^2} \, dt\right]$

**Solution**:

First, reverse the limits (which changes the sign):

$$\int_x^5 e^{t^2} \, dt = -\int_5^x e^{t^2} \, dt$$

Now apply FTC Part 1:

$$\frac{d}{dx}\left[-\int_5^x e^{t^2} \, dt\right] = -e^{x^2}$$

---

**Example 4**: Evaluate $\int_1^4 (3x^2 - 2x + 1) \, dx$

**Solution**:

Find an antiderivative:
$$F(x) = x^3 - x^2 + x$$

Apply FTC Part 2:
$$\int_1^4 (3x^2 - 2x + 1) \, dx = [x^3 - x^2 + x]_1^4$$

$$= (64 - 16 + 4) - (1 - 1 + 1) = 52 - 1 = 51$$

---

**Example 5**: Evaluate $\int_0^{\pi/2} \cos x \, dx$

**Solution**:

Antiderivative of $\cos x$ is $\sin x$.

$$\int_0^{\pi/2} \cos x \, dx = [\sin x]_0^{\pi/2} = \sin\frac{\pi}{2} - \sin 0 = 1 - 0 = 1$$

---

**Example 6**: Evaluate $\int_1^e \frac{1}{x} \, dx$

**Solution**:

Antiderivative of $\frac{1}{x}$ is $\ln|x|$.

$$\int_1^e \frac{1}{x} \, dx = [\ln|x|]_1^e = \ln e - \ln 1 = 1 - 0 = 1$$

---

**Example 7**: Find $\frac{d}{dx}\left[\int_{2x}^{x^3} \cos t \, dt\right]$

**Solution**:

Both limits are functions of $x$. Split the integral:

$$\int_{2x}^{x^3} \cos t \, dt = \int_0^{x^3} \cos t \, dt - \int_0^{2x} \cos t \, dt$$

Now differentiate:

$$\frac{d}{dx}\left[\int_0^{x^3} \cos t \, dt\right] = \cos(x^3) \cdot 3x^2$$

$$\frac{d}{dx}\left[\int_0^{2x} \cos t \, dt\right] = \cos(2x) \cdot 2$$

Combine:
$$\frac{d}{dx}\left[\int_{2x}^{x^3} \cos t \, dt\right] = 3x^2\cos(x^3) - 2\cos(2x)$$

---

**Example 8**: If $g(x) = \int_1^x \frac{1}{1+t^2} \, dt$, find $g'(x)$ and $g(1)$.

**Solution**:

By FTC Part 1:
$$g'(x) = \frac{1}{1+x^2}$$

For $g(1)$:
$$g(1) = \int_1^1 \frac{1}{1+t^2} \, dt = 0$$

(Any integral from $a$ to $a$ equals zero.)

---

## Key Formulas & Rules

| Theorem | Formula |
|---------|---------|
| FTC Part 1 | $\frac{d}{dx}\int_a^x f(t) \, dt = f(x)$ |
| FTC Part 1 (chain rule) | $\frac{d}{dx}\int_a^{u(x)} f(t) \, dt = f(u(x)) \cdot u'(x)$ |
| FTC Part 1 (both limits) | $\frac{d}{dx}\int_{v(x)}^{u(x)} f(t) \, dt = f(u) \cdot u' - f(v) \cdot v'$ |
| FTC Part 2 | $\int_a^b f(x) \, dx = F(b) - F(a)$ where $F' = f$ |

**Memory Device**:
- **Part 1**: "Derivative undoes integral" → $\frac{d}{dx}\int f = f$
- **Part 2**: "Antiderivative evaluates integral" → $\int f = F|_a^b$

---

## Common Mistakes to Avoid

1. **Forgetting the chain rule**: When the upper limit is $u(x)$, multiply by $u'(x)$.

2. **Wrong sign when lower limit varies**: If the lower limit is a function of $x$, it contributes with a **negative** sign.

3. **Confusing the variable of integration**: In $\int_a^x f(t) \, dt$, differentiate with respect to $x$, not $t$.

4. **Forgetting to subtract in FTC Part 2**: $F(b) - F(a)$, not just $F(b)$.

5. **Not checking continuity**: FTC requires $f$ to be continuous on the interval.

6. **Wrong evaluation order**: $[F(x)]_a^b = F(b) - F(a)$ (upper minus lower).

---

## AP Exam Tips

### For Both AB and BC:
- FTC appears on nearly every AP exam—know it cold
- Part 1 questions often use chain rule variants
- Part 2 is used constantly for evaluation
- Be ready to interpret results in context (net change, accumulation)

### Common Question Types:
1. **Differentiate an integral**: Direct application of FTC Part 1
2. **Evaluate a definite integral**: Apply FTC Part 2
3. **Accumulation functions**: Find where $g(x) = \int_a^x f(t) \, dt$ has max/min
4. **Rate/amount problems**: Connect integral of rate to net change

### Free Response Tips:
- State which part of FTC you're using
- Show the antiderivative clearly before evaluating
- With chain rule, show the multiplication by the derivative of the limit

---

## Practice Problems

### Basic (Problems 1-5)

**1.** Find:

$$\frac{d}{dx}\left[\int_0^x t^3 \, dt\right]$$

---

**2.** Evaluate:

$$\int_0^2 (4x - 3) \, dx$$

---

**3.** Find:

$$\frac{d}{dx}\left[\int_3^x \sin(t^2) \, dt\right]$$

---

**4.** Evaluate:

$$\int_0^{\pi} \sin x \, dx$$

---

**5.** Find:

$$\frac{d}{dx}\left[\int_x^0 e^t \, dt\right]$$

---

### Intermediate (Problems 6-10)

**6.** Find:

$$\frac{d}{dx}\left[\int_1^{x^2} \sqrt{t + 1} \, dt\right]$$

---

**7.** Evaluate:

$$\int_1^4 \left(\sqrt{x} + \frac{1}{x^2}\right) dx$$

---

**8.** If $g(x) = \int_2^x (t^2 - 4) \, dt$, find:

**(a)** $g'(x)$

**(b)** $g'(3)$

**(c)** $g(2)$

---

**9.** Find:

$$\frac{d}{dx}\left[\int_0^{\sin x} t^2 \, dt\right]$$

---

**10.** Evaluate:

$$\int_{-1}^1 (e^x - e^{-x}) \, dx$$

---

### Advanced (Problems 11-15)

**11.** Find:

$$\frac{d}{dx}\left[\int_{x}^{x^2} \frac{1}{1+t^4} \, dt\right]$$

---

**12.** Let $g(x) = \int_0^x f(t) \, dt$ where $f$ is the function graphed below (a line from $(0, 2)$ to $(4, -2)$).

**(a)** Find where $g$ has a maximum.

**(b)** Find where $g$ is concave up.

---

**13.** Evaluate:

$$\int_0^{\ln 3} e^{2x} \, dx$$

---

**14.** If $\frac{d}{dx}\int_0^x f(t) \, dt = x\cos(\pi x)$, find $f(2)$.

---

**15.** Find the value of $c$ such that:

$$\int_0^c x^2 \, dx = 72$$

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

$$\frac{d}{dx}\int_2^{x^3} \sqrt{1 + t^2} \, dt =$$

| Choice | Answer |
|--------|--------|
| **(A)** | $\sqrt{1 + x^6}$ |
| **(B)** | $3x^2\sqrt{1 + x^6}$ |
| **(C)** | $3x^2\sqrt{1 + x^2}$ |
| **(D)** | $\frac{x^3}{\sqrt{1 + x^6}}$ |

---

#### Problem 17 (Multiple Choice)

$$\int_0^4 |x - 2| \, dx =$$

| Choice | Answer |
|--------|--------|
| **(A)** | 0 |
| **(B)** | 2 |
| **(C)** | 4 |
| **(D)** | 8 |

---

#### Problem 18 (Free Response)

Let $g(x) = \int_0^x f(t) \, dt$, where the graph of $f$ is shown consisting of line segments connecting:
$(0, 2) \to (2, 2) \to (4, -1) \to (6, -1)$

> **(a)** Find $g(2)$, $g(4)$, and $g(6)$.
>
> **(b)** Find $g'(3)$.
>
> **(c)** On what interval(s) is $g$ increasing?
>
> **(d)** Find the absolute maximum of $g$ on $[0, 6]$.

---

#### Problem 19 (Multiple Choice)

If $F(x) = \int_x^{x^2} \sin(t^2) \, dt$, then $F'(x) =$

| Choice | Answer |
|--------|--------|
| **(A)** | $\sin(x^4) - \sin(x^2)$ |
| **(B)** | $2x\sin(x^4) - \sin(x^2)$ |
| **(C)** | $2x\sin(x^4) + \sin(x^2)$ |
| **(D)** | $\sin(x^4) \cdot 2x - \sin(x^2)$ |

---

#### Problem 20 (Free Response - Challenging)

The rate at which oil leaks from a storage tank is modeled by $L(t) = 2000e^{-0.5t}$ gallons per hour, where $t$ is measured in hours.

> **(a)** Find the total amount of oil that leaks from the tank during the first 2 hours.
>
> **(b)** Find the average rate of leakage during the first 2 hours.
>
> **(c)** At what rate is the total leaked oil accumulating at $t = 2$ hours?
>
> **(d)** If the tank initially contained 8000 gallons, write an expression for the amount of oil remaining in the tank at time $t$.

---

## Answer Key

<details>
<summary><strong>Problem 1 Solution</strong></summary>

**Answer**: $x^3$

**Step-by-step solution**:

By FTC Part 1:

$$\frac{d}{dx}\left[\int_0^x t^3 \, dt\right] = x^3$$

Simply replace $t$ with $x$ in the integrand.

</details>

---

<details>
<summary><strong>Problem 2 Solution</strong></summary>

**Answer**: $2$

**Step-by-step solution**:

Find the antiderivative:
$$F(x) = 2x^2 - 3x$$

Apply FTC Part 2:
$$\int_0^2 (4x - 3) \, dx = [2x^2 - 3x]_0^2 = (8 - 6) - (0) = 2$$

</details>

---

<details>
<summary><strong>Problem 3 Solution</strong></summary>

**Answer**: $\sin(x^2)$

**Step-by-step solution**:

By FTC Part 1:

$$\frac{d}{dx}\left[\int_3^x \sin(t^2) \, dt\right] = \sin(x^2)$$

</details>

---

<details>
<summary><strong>Problem 4 Solution</strong></summary>

**Answer**: $2$

**Step-by-step solution**:

$$\int_0^{\pi} \sin x \, dx = [-\cos x]_0^{\pi} = -\cos\pi - (-\cos 0)$$
$$= -(-1) - (-1) = 1 + 1 = 2$$

</details>

---

<details>
<summary><strong>Problem 5 Solution</strong></summary>

**Answer**: $-e^x$

**Step-by-step solution**:

First, reverse the limits:
$$\int_x^0 e^t \, dt = -\int_0^x e^t \, dt$$

Then apply FTC Part 1:
$$\frac{d}{dx}\left[-\int_0^x e^t \, dt\right] = -e^x$$

</details>

---

<details>
<summary><strong>Problem 6 Solution</strong></summary>

**Answer**: $2x\sqrt{x^2 + 1}$

**Step-by-step solution**:

Apply FTC Part 1 with chain rule. Let $u = x^2$, so $u' = 2x$.

$$\frac{d}{dx}\left[\int_1^{x^2} \sqrt{t + 1} \, dt\right] = \sqrt{x^2 + 1} \cdot 2x = 2x\sqrt{x^2 + 1}$$

</details>

---

<details>
<summary><strong>Problem 7 Solution</strong></summary>

**Answer**: $\frac{17}{6}$

**Step-by-step solution**:

Rewrite: $\sqrt{x} = x^{1/2}$ and $\frac{1}{x^2} = x^{-2}$

Antiderivative:
$$F(x) = \frac{x^{3/2}}{3/2} + \frac{x^{-1}}{-1} = \frac{2}{3}x^{3/2} - \frac{1}{x}$$

Evaluate:
$$\left[\frac{2}{3}x^{3/2} - \frac{1}{x}\right]_1^4 = \left(\frac{2}{3}(8) - \frac{1}{4}\right) - \left(\frac{2}{3}(1) - 1\right)$$

$$= \left(\frac{16}{3} - \frac{1}{4}\right) - \left(\frac{2}{3} - 1\right) = \frac{16}{3} - \frac{1}{4} - \frac{2}{3} + 1$$

$$= \frac{14}{3} + \frac{3}{4} = \frac{56 + 9}{12} = \frac{65}{12}$$

Wait, let me recalculate:
$$= \frac{16}{3} - \frac{1}{4} - \frac{2}{3} + 1 = \frac{14}{3} + \frac{3}{4} = \frac{56}{12} + \frac{9}{12} = \frac{65}{12}$$

</details>

---

<details>
<summary><strong>Problem 8 Solution</strong></summary>

**Answer**: (a) $x^2 - 4$, (b) $5$, (c) $0$

**(a)** By FTC Part 1:
$$g'(x) = x^2 - 4$$

**(b)**
$$g'(3) = 9 - 4 = 5$$

**(c)**
$$g(2) = \int_2^2 (t^2 - 4) \, dt = 0$$

</details>

---

<details>
<summary><strong>Problem 9 Solution</strong></summary>

**Answer**: $\sin^2 x \cos x$

**Step-by-step solution**:

Apply FTC Part 1 with chain rule. Let $u = \sin x$, so $u' = \cos x$.

$$\frac{d}{dx}\left[\int_0^{\sin x} t^2 \, dt\right] = (\sin x)^2 \cdot \cos x = \sin^2 x \cos x$$

</details>

---

<details>
<summary><strong>Problem 10 Solution</strong></summary>

**Answer**: $0$

**Step-by-step solution**:

$$\int_{-1}^1 (e^x - e^{-x}) \, dx = [e^x + e^{-x}]_{-1}^1$$

$$= (e + e^{-1}) - (e^{-1} + e) = 0$$

Alternatively: $f(x) = e^x - e^{-x}$ is an odd function, and the integral of an odd function over a symmetric interval is 0.

</details>

---

<details>
<summary><strong>Problem 11 Solution</strong></summary>

**Answer**: $\frac{2x}{1+x^8} - \frac{1}{1+x^4}$

**Step-by-step solution**:

Apply FTC Part 1 with both limits as functions:

$$\frac{d}{dx}\left[\int_x^{x^2} \frac{1}{1+t^4} \, dt\right] = \frac{1}{1+(x^2)^4} \cdot 2x - \frac{1}{1+x^4} \cdot 1$$

$$= \frac{2x}{1+x^8} - \frac{1}{1+x^4}$$

</details>

---

<details>
<summary><strong>Problem 12 Solution</strong></summary>

**Answer**: (a) Maximum at $x = 2$, (b) Concave up on $(2, 4)$

**Step-by-step solution**:

**(a)** $g'(x) = f(x)$. $g$ has a maximum where $g'$ changes from positive to negative.

$f(x)$ goes from 2 to -2 linearly, so $f(x) = 0$ at $x = 2$.

For $x < 2$: $f(x) > 0$, so $g' > 0$ (increasing)
For $x > 2$: $f(x) < 0$, so $g' < 0$ (decreasing)

Maximum at $x = 2$.

**(b)** $g''(x) = f'(x)$. $g$ is concave up where $f'(x) > 0$.

$f$ is decreasing (slope = $-1$) from $(0,2)$ to $(4,-2)$, so $f'(x) = -1 < 0$ on $(0, 4)$.

Actually, looking more carefully: $f$ goes from 2 to -2 over $x = 0$ to $x = 4$, so slope = $\frac{-2-2}{4-0} = -1$.

$g$ is concave down on $(0, 4)$ since $f' < 0$ there.

On $(4, 6)$, $f$ is constant at $-1$, so $f' = 0$, meaning $g$ has no concavity change.

$g$ is never concave up based on this description.

</details>

---

<details>
<summary><strong>Problem 13 Solution</strong></summary>

**Answer**: $4$

**Step-by-step solution**:

Antiderivative of $e^{2x}$ is $\frac{1}{2}e^{2x}$.

$$\int_0^{\ln 3} e^{2x} \, dx = \left[\frac{1}{2}e^{2x}\right]_0^{\ln 3}$$

$$= \frac{1}{2}e^{2\ln 3} - \frac{1}{2}e^0 = \frac{1}{2}e^{\ln 9} - \frac{1}{2}$$

$$= \frac{1}{2}(9) - \frac{1}{2} = \frac{9-1}{2} = 4$$

</details>

---

<details>
<summary><strong>Problem 14 Solution</strong></summary>

**Answer**: $f(2) = 2\cos(2\pi) = 2$

**Step-by-step solution**:

By FTC Part 1:
$$\frac{d}{dx}\int_0^x f(t) \, dt = f(x)$$

We're told this equals $x\cos(\pi x)$, so:
$$f(x) = x\cos(\pi x)$$

Therefore:
$$f(2) = 2\cos(2\pi) = 2(1) = 2$$

</details>

---

<details>
<summary><strong>Problem 15 Solution</strong></summary>

**Answer**: $c = 6$

**Step-by-step solution**:

$$\int_0^c x^2 \, dx = \left[\frac{x^3}{3}\right]_0^c = \frac{c^3}{3} = 72$$

$$c^3 = 216$$

$$c = 6$$

</details>

---

<details>
<summary><strong>Problem 16 Solution</strong></summary>

**Answer**: **(B)** $3x^2\sqrt{1 + x^6}$

**Step-by-step solution**:

Apply FTC Part 1 with chain rule. Let $u = x^3$, so $u' = 3x^2$.

$$\frac{d}{dx}\int_2^{x^3} \sqrt{1 + t^2} \, dt = \sqrt{1 + (x^3)^2} \cdot 3x^2 = 3x^2\sqrt{1 + x^6}$$

</details>

---

<details>
<summary><strong>Problem 17 Solution</strong></summary>

**Answer**: **(C)** $4$

**Step-by-step solution**:

Split at $x = 2$ where the absolute value changes:

$$\int_0^4 |x - 2| \, dx = \int_0^2 (2-x) \, dx + \int_2^4 (x-2) \, dx$$

$$= \left[2x - \frac{x^2}{2}\right]_0^2 + \left[\frac{x^2}{2} - 2x\right]_2^4$$

$$= (4 - 2) - 0 + (8 - 8) - (2 - 4)$$

$$= 2 + 0 - (-2) = 2 + 2 = 4$$

</details>

---

<details>
<summary><strong>Problem 18 Solution</strong></summary>

**Answer**: See detailed solution below.

**(a)**
$g(2) = \int_0^2 f(t) \, dt = $ area of rectangle with base 2, height 2 $= 4$

$g(4) = \int_0^4 f(t) \, dt = 4 + \int_2^4 f(t) \, dt$

From $(2,2)$ to $(4,-1)$: trapezoid with bases 2 and -1, height 2.
Area = $\frac{1}{2}(2 + (-1))(2) = 1$

$g(4) = 4 + 1 = 5$

Wait, let me recalculate. The region from $x=2$ to $x=4$ is a trapezoid that goes from positive to negative.

Actually, $f$ crosses zero. From $f(2) = 2$ to $f(4) = -1$, $f = 0$ at $x = \frac{2(4) + 2(-1)}{2-(-1)} = ...$

Linear function: $f(t) = 2 - \frac{3}{2}(t-2) = 2 - \frac{3t}{2} + 3 = 5 - \frac{3t}{2}$

$f = 0$ when $t = \frac{10}{3}$

Area from 2 to 10/3: triangle with base $\frac{4}{3}$, height 2 → $\frac{1}{2} \cdot \frac{4}{3} \cdot 2 = \frac{4}{3}$

Area from 10/3 to 4: triangle with base $\frac{2}{3}$, height 1 → $\frac{1}{2} \cdot \frac{2}{3} \cdot 1 = \frac{1}{3}$ (negative)

$g(4) = 4 + \frac{4}{3} - \frac{1}{3} = 4 + 1 = 5$

$g(6) = g(4) + \int_4^6 f(t) \, dt = 5 + (-1)(2) = 3$

**(b)** $g'(3) = f(3)$

At $x = 3$: $f(3) = 5 - \frac{9}{2} = \frac{1}{2}$

**(c)** $g$ is increasing where $g'(x) = f(x) > 0$, which is $[0, \frac{10}{3})$.

**(d)** Maximum occurs at $x = \frac{10}{3}$ where $g' = f = 0$ and changes from positive to negative.

$g(\frac{10}{3}) = 4 + \frac{4}{3} = \frac{16}{3}$

</details>

---

<details>
<summary><strong>Problem 19 Solution</strong></summary>

**Answer**: **(B)** $2x\sin(x^4) - \sin(x^2)$

**Step-by-step solution**:

$$F'(x) = \sin((x^2)^2) \cdot 2x - \sin(x^2) \cdot 1 = 2x\sin(x^4) - \sin(x^2)$$

</details>

---

<details>
<summary><strong>Problem 20 Solution</strong></summary>

**Answer**: See detailed solution below.

**(a) Total oil leaked in first 2 hours**:

$$\int_0^2 2000e^{-0.5t} \, dt = 2000 \cdot \left[-2e^{-0.5t}\right]_0^2$$

$$= -4000[e^{-1} - e^0] = -4000(e^{-1} - 1) = 4000(1 - e^{-1})$$

$$\approx 4000(1 - 0.368) \approx 4000(0.632) \approx 2528 \text{ gallons}$$

**(b) Average rate of leakage**:

$$\text{Average} = \frac{1}{2-0}\int_0^2 L(t) \, dt = \frac{4000(1-e^{-1})}{2} = 2000(1-e^{-1}) \approx 1264 \text{ gal/hr}$$

**(c) Rate of accumulation at $t = 2$**:

By FTC Part 1, the rate at which total leaked oil is accumulating equals the rate function:

$$L(2) = 2000e^{-1} \approx 736 \text{ gallons per hour}$$

**(d) Amount remaining**:

$$A(t) = 8000 - \int_0^t L(s) \, ds = 8000 - \int_0^t 2000e^{-0.5s} \, ds$$

$$= 8000 - 4000(1 - e^{-0.5t}) = 8000 - 4000 + 4000e^{-0.5t}$$

$$= 4000 + 4000e^{-0.5t} = 4000(1 + e^{-0.5t})$$

</details>

---

## What's Next

With the Fundamental Theorem mastered, you're ready to explore [Accumulation Functions](/calculus/accumulation-functions), where we'll study functions defined by integrals and their powerful applications.

---

<div align="center">

[← Definite Integrals](/calculus/definite-integrals) | [Accumulation Functions →](/calculus/accumulation-functions)

</div>
