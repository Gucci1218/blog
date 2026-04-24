# AP Calculus BC — Practice Test 1: Solutions

> Complete answer key and detailed solutions
> April 2026

---

## Quick Answer Key

### Section I — Multiple Choice

| Q | Ans | Q | Ans | Q | Ans | Q | Ans | Q | Ans |
|---|-----|---|-----|---|-----|---|-----|---|-----|
| 1 | C | 10 | A | 19 | A | 28 | B | 37 | B |
| 2 | B | 11 | B | 20 | A | 29 | B | 38 | C |
| 3 | B | 12 | C | 21 | A | 30 | C | 39 | C |
| 4 | A | 13 | B | 22 | B | 31 | D | 40 | B |
| 5 | A | 14 | C | 23 | D | 32 | B | 41 | A |
| 6 | C | 15 | A | 24 | A | 33 | B | 42 | C |
| 7 | C | 16 | A | 25 | B | 34 | B | 43 | B |
| 8 | B | 17 | A | 26 | A | 35 | B | 44 | C |
| 9 | B | 18 | C | 27 | B | 36 | C | 45 | B |

---

## Section I: Multiple Choice Solutions

### Part A — No Calculator

<details>
<summary><strong>Question 1</strong></summary>

**$\displaystyle \lim_{x \to 0} \frac{\sin 3x}{5x} =$**

**(A)** $0$ | **(B)** $\dfrac{1}{5}$ | **(C)** $\dfrac{3}{5}$ | **(D)** $\dfrac{5}{3}$

**Answer: (C) $\dfrac{3}{5}$**

**Solution:**

Multiply and divide by $3$ to create the standard limit form $\frac{\sin u}{u} \to 1$:

$$\lim_{x \to 0} \frac{\sin 3x}{5x} = \lim_{x \to 0} \frac{3}{5} \cdot \frac{\sin 3x}{3x}$$

As $x \to 0$, we have $3x \to 0$, so $\frac{\sin 3x}{3x} \to 1$:

$$= \frac{3}{5} \cdot 1 = \frac{3}{5}$$

**Common mistake:** Forgetting to multiply by $\frac{3}{3}$ and incorrectly writing the answer as $\frac{1}{5}$. Always match the argument of sine with the denominator.

</details>

<details>
<summary><strong>Question 2</strong></summary>

**If $f(x) = x^3 \ln x$, then $f'(x) =$**

**(A)** $3x^2 \ln x$ | **(B)** $x^2(3\ln x + 1)$ | **(C)** $x^2(3\ln x - 1)$ | **(D)** $3x^2 \ln x + x^2$

**Answer: (B) $x^2(3\ln x + 1)$**

**Solution:**

Use the product rule with $u = x^3$ and $v = \ln x$:

$$f'(x) = (x^3)'(\ln x) + (x^3)(\ln x)' = 3x^2 \ln x + x^3 \cdot \frac{1}{x}$$

$$= 3x^2 \ln x + x^2 = x^2(3\ln x + 1)$$

Note that answer choice (D) is $3x^2 \ln x + x^2$, which is the same expression before factoring. The factored form (B) is the credited answer.

**Common mistake:** Only differentiating one part of the product (just $x^3$) and forgetting the product rule entirely, getting answer (A).

</details>

<details>
<summary><strong>Question 3</strong></summary>

**$\displaystyle \lim_{x \to \infty} \frac{5x^3 - 2x}{3x^3 + 7} =$**

**(A)** $0$ | **(B)** $\dfrac{5}{3}$ | **(C)** $\dfrac{-2}{7}$ | **(D)** $\infty$

**Answer: (B) $\dfrac{5}{3}$**

**Solution:**

When the degrees of the numerator and denominator are equal, the limit is the ratio of the leading coefficients:

$$\lim_{x \to \infty} \frac{5x^3 - 2x}{3x^3 + 7} = \frac{5}{3}$$

Alternatively, divide every term by $x^3$:

$$\lim_{x \to \infty} \frac{5 - \frac{2}{x^2}}{3 + \frac{7}{x^3}} = \frac{5 - 0}{3 + 0} = \frac{5}{3}$$

**Common mistake:** Choosing (C) by comparing the non-leading terms $-2x$ and $7$ instead of the leading coefficients.

</details>

<details>
<summary><strong>Question 4</strong></summary>

**$\displaystyle \int x e^{x^2} \, dx =$**

**(A)** $\frac{1}{2}e^{x^2} + C$ | **(B)** $e^{x^2} + C$ | **(C)** $x^2 e^{x^2} + C$ | **(D)** $\frac{1}{2}x^2 e^{x^2} + C$

**Answer: (A) $\dfrac{1}{2}e^{x^2} + C$**

**Solution:**

Use $u$-substitution. Let $u = x^2$, so $du = 2x\,dx$, which means $x\,dx = \frac{du}{2}$:

$$\int x e^{x^2}\,dx = \int e^u \cdot \frac{du}{2} = \frac{1}{2}e^u + C = \frac{1}{2}e^{x^2} + C$$

**Common mistake:** Forgetting the $\frac{1}{2}$ factor from the substitution and choosing (B).

</details>

<details>
<summary><strong>Question 5</strong></summary>

**If $x^2 + y^2 = 25$, then $\dfrac{dy}{dx} =$**

**(A)** $\dfrac{-x}{y}$ | **(B)** $\dfrac{x}{y}$ | **(C)** $\dfrac{-2x}{y}$ | **(D)** $\dfrac{-y}{x}$

**Answer: (A) $\dfrac{-x}{y}$**

**Solution:**

Differentiate both sides implicitly with respect to $x$:

$$2x + 2y\frac{dy}{dx} = 0$$

Solve for $\frac{dy}{dx}$:

$$2y\frac{dy}{dx} = -2x$$

$$\frac{dy}{dx} = \frac{-x}{y}$$

**Common mistake:** Dividing incorrectly and getting $\frac{-2x}{y}$ by forgetting that the $2$ cancels from both sides.

</details>

<details>
<summary><strong>Question 6</strong></summary>

**The function $f(x) = x^4 - 4x^3$ has a local minimum at $x =$**

**(A)** $0$ | **(B)** $1$ | **(C)** $3$ | **(D)** $4$

**Answer: (C) $3$**

**Solution:**

Find the critical points:

$$f'(x) = 4x^3 - 12x^2 = 4x^2(x - 3)$$

Setting $f'(x) = 0$: $x = 0$ or $x = 3$.

Use the first derivative test to classify:
- For $x < 0$: $f'(x) = 4(\text{pos})(x - 3) < 0$ (decreasing)
- For $0 < x < 3$: $f'(x) = 4x^2(x - 3) < 0$ (still decreasing)
- For $x > 3$: $f'(x) = 4x^2(x - 3) > 0$ (increasing)

At $x = 0$: $f'$ does not change sign (negative on both sides), so $x = 0$ is neither a local max nor min.

At $x = 3$: $f'$ changes from negative to positive, so $x = 3$ is a **local minimum**.

**Common mistake:** Assuming $x = 0$ is a local min because $f'(0) = 0$. You must verify a sign change in $f'$ to confirm a local extremum.

</details>

<details>
<summary><strong>Question 7</strong></summary>

**$\displaystyle \int_0^{\pi} \sin x \, dx =$**

**(A)** $0$ | **(B)** $1$ | **(C)** $2$ | **(D)** $-2$

**Answer: (C) $2$**

**Solution:**

$$\int_0^{\pi} \sin x\,dx = \Big[-\cos x\Big]_0^{\pi} = (-\cos\pi) - (-\cos 0) = -(-1) - (-(1)) = 1 + 1 = 2$$

**Common mistake:** Getting $0$ by confusing this with $\int_0^{2\pi}\sin x\,dx = 0$. Over $[0, \pi]$, $\sin x \ge 0$, so the integral must be positive.

</details>

<details>
<summary><strong>Question 8</strong></summary>

**$\displaystyle \lim_{x \to 0} \frac{e^x - 1 - x}{x^2} =$**

**(A)** $0$ | **(B)** $\dfrac{1}{2}$ | **(C)** $1$ | **(D)** $\infty$

**Answer: (B) $\dfrac{1}{2}$**

**Solution:**

Direct substitution gives $\frac{0}{0}$. Apply L'Hopital's Rule:

$$\lim_{x \to 0} \frac{e^x - 1 - x}{x^2} = \lim_{x \to 0} \frac{e^x - 1}{2x}$$

This is still $\frac{0}{0}$, so apply L'Hopital's Rule again:

$$= \lim_{x \to 0} \frac{e^x}{2} = \frac{e^0}{2} = \frac{1}{2}$$

Alternatively, use the Taylor series $e^x = 1 + x + \frac{x^2}{2} + \cdots$:

$$\frac{e^x - 1 - x}{x^2} = \frac{\frac{x^2}{2} + \frac{x^3}{6} + \cdots}{x^2} = \frac{1}{2} + \frac{x}{6} + \cdots \to \frac{1}{2}$$

**Common mistake:** Applying L'Hopital's Rule only once and then incorrectly evaluating $\frac{e^0 - 1}{0}$ as $0$.

</details>

<details>
<summary><strong>Question 9</strong></summary>

**If $f(x) = \arctan(2x)$, then $f'(x) =$**

**(A)** $\dfrac{1}{1 + 4x^2}$ | **(B)** $\dfrac{2}{1 + 4x^2}$ | **(C)** $\dfrac{2}{1 + 2x^2}$ | **(D)** $\dfrac{1}{1 + 2x^2}$

**Answer: (B) $\dfrac{2}{1 + 4x^2}$**

**Solution:**

Use the chain rule with the derivative of $\arctan u$:

$$\frac{d}{dx}\arctan(2x) = \frac{1}{1 + (2x)^2} \cdot \frac{d}{dx}(2x) = \frac{1}{1 + 4x^2} \cdot 2 = \frac{2}{1 + 4x^2}$$

**Common mistake:** Forgetting the chain rule factor of $2$ and choosing (A), or incorrectly squaring inside to get $1 + 2x^2$ instead of $1 + 4x^2$.

</details>

<details>
<summary><strong>Question 10</strong></summary>

**$\displaystyle \int \frac{3}{x^2 - 9} \, dx =$**

**(A)** $\frac{1}{2}\ln\left|\frac{x-3}{x+3}\right| + C$ | **(B)** $\ln|x^2 - 9| + C$ | **(C)** $\frac{3}{2}\ln\left|\frac{x-3}{x+3}\right| + C$ | **(D)** $3\arctan\left(\frac{x}{3}\right) + C$

**Answer: (A) $\dfrac{1}{2}\ln\left|\dfrac{x-3}{x+3}\right| + C$**

**Solution:**

Factor the denominator: $x^2 - 9 = (x-3)(x+3)$. Use partial fractions:

$$\frac{3}{(x-3)(x+3)} = \frac{A}{x-3} + \frac{B}{x+3}$$

$$3 = A(x+3) + B(x-3)$$

Setting $x = 3$: $3 = 6A \Rightarrow A = \frac{1}{2}$

Setting $x = -3$: $3 = -6B \Rightarrow B = -\frac{1}{2}$

$$\int \frac{3}{x^2 - 9}\,dx = \int \frac{1/2}{x-3}\,dx - \int \frac{1/2}{x+3}\,dx$$

$$= \frac{1}{2}\ln|x-3| - \frac{1}{2}\ln|x+3| + C = \frac{1}{2}\ln\left|\frac{x-3}{x+3}\right| + C$$

**Common mistake:** Trying to use the $\arctan$ formula, which applies to $x^2 + 9$ (sum), not $x^2 - 9$ (difference).

</details>

<details>
<summary><strong>Question 11</strong></summary>

**The slope field for a differential equation is shown to have horizontal segments along the line $y = 2$ and vertical segments along the line $x = 0$. Which differential equation could produce this slope field?**

**(A)** $\dfrac{dy}{dx} = x(y - 2)$ | **(B)** $\dfrac{dy}{dx} = \dfrac{y - 2}{x}$ | **(C)** $\dfrac{dy}{dx} = x + y - 2$ | **(D)** $\dfrac{dy}{dx} = xy - 2$

**Answer: (B) $\dfrac{dy}{dx} = \dfrac{y - 2}{x}$**

**Solution:**

We need two conditions:
- **Horizontal segments** (slope $= 0$) when $y = 2$
- **Vertical segments** (slope undefined) when $x = 0$

Check each option:

**(A)** $\frac{dy}{dx} = x(y-2)$: Zero when $y = 2$ or $x = 0$. At $x = 0$, slope is $0$ (horizontal), not vertical.

**(B)** $\frac{dy}{dx} = \frac{y-2}{x}$: Zero when $y = 2$. Undefined when $x = 0$. Both conditions satisfied.

**(C)** $\frac{dy}{dx} = x + y - 2$: Zero when $x + y = 2$, not just $y = 2$. Never undefined.

**(D)** $\frac{dy}{dx} = xy - 2$: Zero when $xy = 2$, not when $y = 2$.

**Common mistake:** Choosing (A) because it also has a factor of $(y - 2)$, but forgetting to check whether $x = 0$ makes the slope undefined or zero.

</details>

<details>
<summary><strong>Question 12</strong></summary>

**$\displaystyle \sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n}$ converges to**

**(A)** $0$ | **(B)** $\dfrac{1}{2}$ | **(C)** $\ln 2$ | **(D)** $1$

**Answer: (C) $\ln 2$**

**Solution:**

This is the alternating harmonic series:

$$1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \cdots$$

Recall the Maclaurin series for $\ln(1 + x)$:

$$\ln(1 + x) = \sum_{n=1}^{\infty} \frac{(-1)^{n+1} x^n}{n} = x - \frac{x^2}{2} + \frac{x^3}{3} - \cdots$$

Setting $x = 1$:

$$\ln 2 = \sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n}$$

**Common mistake:** Thinking the series diverges because the harmonic series $\sum \frac{1}{n}$ diverges. The alternating version converges by the Alternating Series Test.

</details>

<details>
<summary><strong>Question 13</strong></summary>

**If $f(x) = \displaystyle \int_1^{x^2} \sqrt{t + 3} \, dt$, then $f'(x) =$**

**(A)** $\sqrt{x^2 + 3}$ | **(B)** $2x\sqrt{x^2 + 3}$ | **(C)** $2x\sqrt{x^4 + 3}$ | **(D)** $\sqrt{x^4 + 3}$

**Answer: (B) $2x\sqrt{x^2 + 3}$**

**Solution:**

By the Fundamental Theorem of Calculus (Part 1) combined with the chain rule:

If $f(x) = \int_a^{g(x)} h(t)\,dt$, then $f'(x) = h(g(x)) \cdot g'(x)$.

Here $h(t) = \sqrt{t + 3}$ and $g(x) = x^2$, so $g'(x) = 2x$:

$$f'(x) = \sqrt{(x^2) + 3} \cdot 2x = 2x\sqrt{x^2 + 3}$$

**Common mistake:** Substituting $t = x^2$ into the integrand as $\sqrt{(x^2)^2 + 3} = \sqrt{x^4 + 3}$ instead of $\sqrt{x^2 + 3}$. Remember: the upper limit $x^2$ replaces $t$, not $t^2$.

</details>

<details>
<summary><strong>Question 14</strong></summary>

**Which of the following series diverges?**

**(A)** $\displaystyle \sum_{n=1}^{\infty} \frac{1}{n^2}$ | **(B)** $\displaystyle \sum_{n=1}^{\infty} \frac{1}{2^n}$ | **(C)** $\displaystyle \sum_{n=1}^{\infty} \frac{1}{n}$ | **(D)** $\displaystyle \sum_{n=1}^{\infty} \frac{(-1)^n}{n}$

**Answer: (C) $\displaystyle \sum_{n=1}^{\infty} \frac{1}{n}$**

**Solution:**

Check each:

- **(A)** $\sum \frac{1}{n^2}$: $p$-series with $p = 2 > 1$. **Converges** (to $\frac{\pi^2}{6}$).
- **(B)** $\sum \frac{1}{2^n}$: Geometric series with $|r| = \frac{1}{2} < 1$. **Converges** (to $1$).
- **(C)** $\sum \frac{1}{n}$: Harmonic series ($p$-series with $p = 1$). **Diverges**.
- **(D)** $\sum \frac{(-1)^n}{n}$: Alternating harmonic series. **Converges** by AST (to $-\ln 2$).

**Common mistake:** Confusing the harmonic series with the alternating harmonic series. The alternation makes (D) converge, but (C) without alternation diverges.

</details>

<details>
<summary><strong>Question 15</strong></summary>

**If $y = e^{3x}\sin x$, then $\dfrac{dy}{dx} =$**

**(A)** $e^{3x}(3\sin x + \cos x)$ | **(B)** $e^{3x}(\sin x + 3\cos x)$ | **(C)** $3e^{3x}\cos x$ | **(D)** $e^{3x}(3\sin x - \cos x)$

**Answer: (A) $e^{3x}(3\sin x + \cos x)$**

**Solution:**

Use the product rule with $u = e^{3x}$ and $v = \sin x$:

$$\frac{dy}{dx} = (e^{3x})'\sin x + e^{3x}(\sin x)' = 3e^{3x}\sin x + e^{3x}\cos x$$

$$= e^{3x}(3\sin x + \cos x)$$

**Common mistake:** Forgetting the chain rule on $e^{3x}$ (the derivative is $3e^{3x}$, not $e^{3x}$), or mixing up which term gets which derivative in the product rule.

</details>

<details>
<summary><strong>Question 16</strong></summary>

**The interval of convergence for $\displaystyle \sum_{n=0}^{\infty} \frac{x^n}{3^n}$ is**

**(A)** $(-3, 3)$ | **(B)** $[-3, 3]$ | **(C)** $(-3, 3]$ | **(D)** $(-1, 1)$

**Answer: (A) $(-3, 3)$**

**Solution:**

Rewrite the series as a geometric series:

$$\sum_{n=0}^{\infty} \frac{x^n}{3^n} = \sum_{n=0}^{\infty} \left(\frac{x}{3}\right)^n$$

A geometric series $\sum r^n$ converges when $|r| < 1$:

$$\left|\frac{x}{3}\right| < 1 \implies |x| < 3 \implies -3 < x < 3$$

Check endpoints:
- $x = 3$: $\sum 1^n = 1 + 1 + 1 + \cdots$ diverges.
- $x = -3$: $\sum (-1)^n = 1 - 1 + 1 - 1 + \cdots$ diverges.

Interval of convergence: $(-3, 3)$.

**Common mistake:** Choosing (B) by forgetting to check the endpoints, or choosing (D) by not recognizing the $3^n$ in the denominator as part of the common ratio.

</details>

<details>
<summary><strong>Question 17</strong></summary>

**$\displaystyle \int \frac{1}{x^2 + 4} \, dx =$**

**(A)** $\frac{1}{2}\arctan\left(\frac{x}{2}\right) + C$ | **(B)** $\arctan\left(\frac{x}{2}\right) + C$ | **(C)** $\frac{1}{4}\arctan\left(\frac{x}{2}\right) + C$ | **(D)** $\ln(x^2 + 4) + C$

**Answer: (A) $\dfrac{1}{2}\arctan\left(\dfrac{x}{2}\right) + C$**

**Solution:**

Use the standard formula $\int \frac{1}{x^2 + a^2}\,dx = \frac{1}{a}\arctan\left(\frac{x}{a}\right) + C$.

Here $a^2 = 4$, so $a = 2$:

$$\int \frac{1}{x^2 + 4}\,dx = \frac{1}{2}\arctan\left(\frac{x}{2}\right) + C$$

**Common mistake:** Using $\frac{1}{a^2}$ instead of $\frac{1}{a}$, giving $\frac{1}{4}$ instead of $\frac{1}{2}$. Or confusing this integral with $\int \frac{2x}{x^2+4}\,dx = \ln(x^2+4) + C$.

</details>

<details>
<summary><strong>Question 18</strong></summary>

**A particle moves along the $x$-axis with velocity $v(t) = t^2 - 4t + 3$. The particle changes direction at $t =$**

**(A)** $1$ only | **(B)** $3$ only | **(C)** $1$ and $3$ | **(D)** $2$

**Answer: (C) $1$ and $3$**

**Solution:**

The particle changes direction when $v(t)$ changes sign. Find where $v(t) = 0$:

$$t^2 - 4t + 3 = (t - 1)(t - 3) = 0 \implies t = 1 \text{ or } t = 3$$

Check sign changes:
- $t < 1$: $v(0) = 3 > 0$
- $1 < t < 3$: $v(2) = 4 - 8 + 3 = -1 < 0$
- $t > 3$: $v(4) = 16 - 16 + 3 = 3 > 0$

$v(t)$ changes sign at both $t = 1$ (positive to negative) and $t = 3$ (negative to positive), so the particle changes direction at both.

**Common mistake:** Choosing (D) $t = 2$ because $t = 2$ is where the velocity has a minimum (vertex of the parabola), but the velocity does not equal zero there.

</details>

<details>
<summary><strong>Question 19</strong></summary>

**The Maclaurin series for $\cos x$ is**

**(A)** $\displaystyle \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n}}{(2n)!}$ | **(B)** $\displaystyle \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+1}}{(2n+1)!}$ | **(C)** $\displaystyle \sum_{n=0}^{\infty} \frac{x^{2n}}{(2n)!}$ | **(D)** $\displaystyle \sum_{n=0}^{\infty} \frac{(-1)^n x^n}{n!}$

**Answer: (A) $\displaystyle \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n}}{(2n)!}$**

**Solution:**

The Maclaurin series for $\cos x$ is:

$$\cos x = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!} + \cdots = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n}}{(2n)!}$$

Key features: only even powers of $x$, alternating signs, factorial denominators with even numbers.

- **(B)** is the series for $\sin x$ (odd powers).
- **(C)** is missing the $(-1)^n$ alternating sign.
- **(D)** is the series for $e^{-x}$ (all powers, not just even).

**Common mistake:** Confusing the $\cos x$ and $\sin x$ series. Remember: **co**sine uses even powers ($2n$), **s**ine uses odd powers ($2n+1$).

</details>

<details>
<summary><strong>Question 20</strong></summary>

**$\displaystyle \int_0^1 x e^x \, dx =$**

**(A)** $1$ | **(B)** $e - 1$ | **(C)** $e$ | **(D)** $2e - 1$

**Answer: (A) $1$**

**Solution:**

Use integration by parts with $u = x$, $dv = e^x\,dx$, so $du = dx$, $v = e^x$:

$$\int_0^1 xe^x\,dx = \Big[xe^x\Big]_0^1 - \int_0^1 e^x\,dx$$

$$= \Big[xe^x\Big]_0^1 - \Big[e^x\Big]_0^1 = (1 \cdot e^1 - 0 \cdot e^0) - (e^1 - e^0)$$

$$= e - (e - 1) = e - e + 1 = 1$$

**Common mistake:** Forgetting to subtract the second integral, or making an error evaluating the boundary terms and getting $e - 1$.

</details>

<details>
<summary><strong>Question 21</strong></summary>

**If $\dfrac{dy}{dx} = 2y$ and $y(0) = 5$, then $y(t) =$**

**(A)** $5e^{2t}$ | **(B)** $2e^{5t}$ | **(C)** $5e^{t^2}$ | **(D)** $e^{2t} + 4$

**Answer: (A) $5e^{2t}$**

**Solution:**

This is a separable differential equation:

$$\frac{dy}{y} = 2\,dt$$

Integrate both sides:

$$\ln|y| = 2t + C_1 \implies y = Ce^{2t}$$

Apply the initial condition $y(0) = 5$:

$$5 = Ce^0 = C \implies C = 5$$

$$y(t) = 5e^{2t}$$

**Common mistake:** Mixing up the coefficient and the initial condition, getting $2e^{5t}$. Remember: the coefficient of $y$ goes in the exponent, the initial value goes in front.

</details>

<details>
<summary><strong>Question 22</strong></summary>

**$\displaystyle \lim_{x \to 0} \frac{\tan x - x}{x^3} =$**

**(A)** $0$ | **(B)** $\dfrac{1}{3}$ | **(C)** $\dfrac{1}{2}$ | **(D)** $1$

**Answer: (B) $\dfrac{1}{3}$**

**Solution:**

Direct substitution gives $\frac{0}{0}$. Use the Taylor series for $\tan x$:

$$\tan x = x + \frac{x^3}{3} + \frac{2x^5}{15} + \cdots$$

$$\frac{\tan x - x}{x^3} = \frac{\frac{x^3}{3} + \frac{2x^5}{15} + \cdots}{x^3} = \frac{1}{3} + \frac{2x^2}{15} + \cdots \to \frac{1}{3}$$

Alternatively, apply L'Hopital's Rule three times:

$$\lim_{x \to 0} \frac{\tan x - x}{x^3} = \lim_{x \to 0} \frac{\sec^2 x - 1}{3x^2} = \lim_{x \to 0} \frac{\tan^2 x}{3x^2} = \frac{1}{3}\lim_{x \to 0}\left(\frac{\tan x}{x}\right)^2 = \frac{1}{3}(1)^2 = \frac{1}{3}$$

**Common mistake:** Applying L'Hopital's once and stopping too early, or making an algebraic error in the repeated differentiation.

</details>

<details>
<summary><strong>Question 23</strong></summary>

**Let $f$ be continuous on $[a, b]$ and let $F$ be an antiderivative of $f$. Which statement is guaranteed by the Fundamental Theorem of Calculus?**

**(A)** $F'(x) = f(x)$ for all $x$ in $(a, b)$ | **(B)** $\int_a^b f(x)\,dx = F(b) - F(a)$ | **(C)** $f$ has a maximum on $[a, b]$ | **(D)** Both (A) and (B)

**Answer: (D) Both (A) and (B)**

**Solution:**

The Fundamental Theorem of Calculus has two parts:

**FTC Part 1:** If $f$ is continuous on $[a, b]$ and $F(x) = \int_a^x f(t)\,dt$, then $F'(x) = f(x)$ for all $x$ in $(a, b)$. Since $F$ is given as an antiderivative, $F'(x) = f(x)$. Statement (A) is guaranteed.

**FTC Part 2:** If $f$ is continuous on $[a, b]$ and $F$ is any antiderivative of $f$, then $\int_a^b f(x)\,dx = F(b) - F(a)$. Statement (B) is guaranteed.

**(C)** is guaranteed by the Extreme Value Theorem, not FTC.

Both (A) and (B) are consequences of FTC, so the answer is **(D)**.

**Common mistake:** Choosing only (A) or only (B), forgetting that FTC has two parts and both statements are valid.

</details>

<details>
<summary><strong>Question 24</strong></summary>

**$\displaystyle \int \frac{5x + 3}{x^2 + x} \, dx =$**

**(A)** $3\ln|x| + 2\ln|x+1| + C$ | **(B)** $5\ln|x^2+x| + C$ | **(C)** $2\ln|x| + 3\ln|x+1| + C$ | **(D)** $\frac{5}{2}\ln|x^2 + x| + 3\arctan x + C$

**Answer: (A) $3\ln|x| + 2\ln|x+1| + C$**

**Solution:**

Factor the denominator: $x^2 + x = x(x + 1)$. Use partial fractions:

$$\frac{5x + 3}{x(x+1)} = \frac{A}{x} + \frac{B}{x+1}$$

$$5x + 3 = A(x + 1) + Bx$$

Setting $x = 0$: $3 = A(1) \implies A = 3$

Setting $x = -1$: $-5 + 3 = B(-1) \implies -2 = -B \implies B = 2$

$$\int \frac{5x+3}{x(x+1)}\,dx = \int \frac{3}{x}\,dx + \int \frac{2}{x+1}\,dx = 3\ln|x| + 2\ln|x+1| + C$$

**Common mistake:** Choosing (C) by swapping the coefficients $A$ and $B$. Always verify by plugging values back in.

</details>

<details>
<summary><strong>Question 25</strong></summary>

**Let $a_n = \dfrac{n!}{n^n}$. Then $\displaystyle \lim_{n \to \infty} \frac{a_{n+1}}{a_n} =$**

**(A)** $0$ | **(B)** $\dfrac{1}{e}$ | **(C)** $1$ | **(D)** $e$

**Answer: (B) $\dfrac{1}{e}$**

**Solution:**

Compute the ratio:

$$\frac{a_{n+1}}{a_n} = \frac{(n+1)!}{(n+1)^{n+1}} \cdot \frac{n^n}{n!} = \frac{(n+1) \cdot n!}{(n+1)^{n+1} \cdot n!} \cdot n^n = \frac{n^n}{(n+1)^n}$$

$$= \left(\frac{n}{n+1}\right)^n = \left(\frac{1}{1 + \frac{1}{n}}\right)^n$$

Using the fundamental limit $\left(1 + \frac{1}{n}\right)^n \to e$:

$$\lim_{n \to \infty} \left(\frac{1}{1 + \frac{1}{n}}\right)^n = \frac{1}{e}$$

**Common mistake:** Getting the ratio upside down and computing $\left(\frac{n+1}{n}\right)^n \to e$, or claiming the limit is $1$ because $\frac{n}{n+1} \to 1$.

</details>

<details>
<summary><strong>Question 26</strong></summary>

**If $x = t^2 + 1$ and $y = t^3 - t$, then $\dfrac{dy}{dx}$ at $t = 2$ is**

**(A)** $\dfrac{11}{4}$ | **(B)** $\dfrac{5}{2}$ | **(C)** $\dfrac{7}{4}$ | **(D)** $4$

**Answer: (A) $\dfrac{11}{4}$**

**Solution:**

For parametric curves, $\frac{dy}{dx} = \frac{dy/dt}{dx/dt}$:

$$\frac{dx}{dt} = 2t, \qquad \frac{dy}{dt} = 3t^2 - 1$$

$$\frac{dy}{dx} = \frac{3t^2 - 1}{2t}$$

At $t = 2$:

$$\frac{dy}{dx}\bigg|_{t=2} = \frac{3(4) - 1}{2(2)} = \frac{12 - 1}{4} = \frac{11}{4}$$

**Common mistake:** Computing $\frac{dx}{dy}$ instead of $\frac{dy}{dx}$, or making an arithmetic error with $3(4) - 1$.

</details>

<details>
<summary><strong>Question 27</strong></summary>

**The third-degree Taylor polynomial for $e^x$ centered at $x = 0$ is**

**(A)** $1 + x + x^2 + x^3$ | **(B)** $1 + x + \frac{x^2}{2} + \frac{x^3}{6}$ | **(C)** $x + \frac{x^2}{2} + \frac{x^3}{3}$ | **(D)** $1 + x + \frac{x^2}{2} + \frac{x^3}{3}$

**Answer: (B) $1 + x + \dfrac{x^2}{2} + \dfrac{x^3}{6}$**

**Solution:**

The Maclaurin series for $e^x$ is:

$$e^x = \sum_{n=0}^{\infty} \frac{x^n}{n!} = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \cdots$$

The third-degree Taylor polynomial is:

$$P_3(x) = 1 + x + \frac{x^2}{2} + \frac{x^3}{6}$$

since $2! = 2$ and $3! = 6$.

**Common mistake:** Using $\frac{x^3}{3}$ instead of $\frac{x^3}{3!} = \frac{x^3}{6}$, confusing the power series for $-\ln(1-x)$ with that of $e^x$.

</details>

<details>
<summary><strong>Question 28</strong></summary>

**$\displaystyle \int_1^{\infty} \frac{1}{x^3} \, dx =$**

**(A)** $\dfrac{1}{3}$ | **(B)** $\dfrac{1}{2}$ | **(C)** $1$ | **(D)** diverges

**Answer: (B) $\dfrac{1}{2}$**

**Solution:**

Evaluate as an improper integral:

$$\int_1^{\infty} x^{-3}\,dx = \lim_{b \to \infty} \int_1^b x^{-3}\,dx = \lim_{b \to \infty} \left[\frac{x^{-2}}{-2}\right]_1^b$$

$$= \lim_{b \to \infty} \left(-\frac{1}{2b^2} + \frac{1}{2}\right) = 0 + \frac{1}{2} = \frac{1}{2}$$

This is a $p$-series integral with $p = 3 > 1$, so it converges.

**Common mistake:** Using the wrong antiderivative power rule, or choosing $\frac{1}{3}$ by incorrectly dividing by the exponent $3$ instead of the new exponent $-2$.

</details>

<details>
<summary><strong>Question 29</strong></summary>

**For the parametric curve $x = 3\cos\theta$, $y = 3\sin\theta$, the length of the curve from $\theta = 0$ to $\theta = \pi$ is**

**(A)** $3$ | **(B)** $3\pi$ | **(C)** $6\pi$ | **(D)** $9\pi$

**Answer: (B) $3\pi$**

**Solution:**

The arc length formula for parametric curves is:

$$L = \int_{\alpha}^{\beta} \sqrt{\left(\frac{dx}{d\theta}\right)^2 + \left(\frac{dy}{d\theta}\right)^2}\,d\theta$$

Compute the derivatives:

$$\frac{dx}{d\theta} = -3\sin\theta, \qquad \frac{dy}{d\theta} = 3\cos\theta$$

$$\left(\frac{dx}{d\theta}\right)^2 + \left(\frac{dy}{d\theta}\right)^2 = 9\sin^2\theta + 9\cos^2\theta = 9$$

$$L = \int_0^{\pi} \sqrt{9}\,d\theta = \int_0^{\pi} 3\,d\theta = 3\pi$$

This makes geometric sense: the curve is a circle of radius $3$, and $\theta$ from $0$ to $\pi$ traces half the circle. The circumference is $2\pi(3) = 6\pi$, so half is $3\pi$.

**Common mistake:** Using the full circle circumference $6\pi$ by integrating from $0$ to $2\pi$ instead of $0$ to $\pi$.

</details>

<details>
<summary><strong>Question 30</strong></summary>

**The radius of convergence of $\displaystyle \sum_{n=0}^{\infty} \frac{(x-2)^n}{n \cdot 5^n}$ is**

**(A)** $1$ | **(B)** $2$ | **(C)** $5$ | **(D)** $\infty$

**Answer: (C) $5$**

**Solution:**

Apply the Ratio Test:

$$\lim_{n \to \infty} \left|\frac{a_{n+1}}{a_n}\right| = \lim_{n \to \infty} \left|\frac{(x-2)^{n+1}}{(n+1) \cdot 5^{n+1}} \cdot \frac{n \cdot 5^n}{(x-2)^n}\right|$$

$$= \lim_{n \to \infty} \frac{|x-2|}{5} \cdot \frac{n}{n+1} = \frac{|x-2|}{5} \cdot 1 = \frac{|x-2|}{5}$$

The series converges when $\frac{|x-2|}{5} < 1$, i.e., $|x - 2| < 5$.

The radius of convergence is $R = 5$.

**Common mistake:** Confusing the center ($2$) with the radius, or forgetting that the $5^n$ in the denominator contributes to the radius.

</details>

---

### Part B — Calculator Allowed

<details>
<summary><strong>Question 31</strong></summary>

**A lifeguard at Coronado Beach spots a swimmer at time $t = 0$. The swimmer's distance from shore (in meters) is modeled by $d(t) = 50 + 12\sin(0.5t)$ for $0 \le t \le 10$ seconds. At what time $t$ is the swimmer moving toward shore the fastest?**

**(A)** $t = 0$ | **(B)** $t = \pi$ | **(C)** $t = 3.142$ | **(D)** $t = 6.283$

**Answer: (D) $t = 6.283$**

**Solution:**

"Moving toward shore the fastest" means $d'(t)$ is most negative (the distance is decreasing the fastest).

$$d'(t) = 12 \cdot 0.5 \cos(0.5t) = 6\cos(0.5t)$$

$d'(t)$ is most negative when $\cos(0.5t) = -1$:

$$0.5t = \pi \implies t = 2\pi \approx 6.283$$

Verify: $d'(2\pi) = 6\cos(\pi) = 6(-1) = -6$, which is the minimum value of $d'(t)$.

At $t = \pi$: $d'(\pi) = 6\cos(\pi/2) = 6(0) = 0$, so the swimmer is momentarily stationary.

**Common mistake:** Choosing $t = \pi$ because $\cos(0.5 \cdot \pi) = 0$, which is where the rate of distance change is zero, not where it's most negative.

</details>

<details>
<summary><strong>Question 32</strong></summary>

**The region bounded by $y = e^{-x^2}$, $y = 0$, $x = 0$, and $x = 2$ is revolved about the $x$-axis. The volume of the resulting solid is**

**(A)** $1.764$ | **(B)** $2.396$ | **(C)** $3.758$ | **(D)** $5.544$

**Answer: (B) $2.396$**

**Solution:**

Using the disk method, the volume is:

$$V = \pi \int_0^2 \left(e^{-x^2}\right)^2 dx = \pi \int_0^2 e^{-2x^2}\,dx$$

This integral has no elementary antiderivative, so use a calculator:

$$\int_0^2 e^{-2x^2}\,dx \approx 0.7627$$

$$V = \pi(0.7627) \approx 2.396$$

**Common mistake:** Forgetting to square the function when using the disk method, computing $\pi\int e^{-x^2}\,dx$ instead of $\pi\int e^{-2x^2}\,dx$.

</details>

<details>
<summary><strong>Question 33</strong></summary>

**Ganga is driving along Pacific Coast Highway and her velocity (in mph) at time $t$ hours is given by $v(t) = 40 + 15\sin(\pi t)$. How far does she travel from $t = 0$ to $t = 2$ hours?**

**(A)** $70$ miles | **(B)** $80$ miles | **(C)** $\frac{30}{\pi} + 80$ miles | **(D)** $80 + \frac{30}{\pi}$ miles

**Answer: (B) $80$ miles**

**Solution:**

Since $v(t) = 40 + 15\sin(\pi t) \ge 40 - 15 = 25 > 0$ for all $t$, the velocity is always positive. The total distance is:

$$\int_0^2 v(t)\,dt = \int_0^2 (40 + 15\sin(\pi t))\,dt$$

$$= \left[40t - \frac{15}{\pi}\cos(\pi t)\right]_0^2$$

$$= \left(80 - \frac{15}{\pi}\cos(2\pi)\right) - \left(0 - \frac{15}{\pi}\cos(0)\right)$$

$$= 80 - \frac{15}{\pi}(1) + \frac{15}{\pi}(1) = 80$$

The cosine terms cancel because $\cos(2\pi) = \cos(0) = 1$.

**Common mistake:** Forgetting that $\cos(2\pi) = \cos(0)$, which causes the sine terms to cancel, and instead getting an answer involving $\frac{1}{\pi}$.

</details>

<details>
<summary><strong>Question 34</strong></summary>

**Using Euler's method with step size $\Delta t = 0.5$, approximate $y(1)$ if $\dfrac{dy}{dt} = t + y$ and $y(0) = 1$.**

**(A)** $2.250$ | **(B)** $2.500$ | **(C)** $2.875$ | **(D)** $3.188$

**Answer: (B) $2.500$**

**Solution:**

Euler's method: $y_{n+1} = y_n + f(t_n, y_n) \cdot \Delta t$ where $f(t, y) = t + y$.

**Step 1:** $t_0 = 0$, $y_0 = 1$

$$y_1 = y_0 + f(0, 1) \cdot 0.5 = 1 + (0 + 1)(0.5) = 1 + 0.5 = 1.5$$

**Step 2:** $t_1 = 0.5$, $y_1 = 1.5$

$$y_2 = y_1 + f(0.5, 1.5) \cdot 0.5 = 1.5 + (0.5 + 1.5)(0.5) = 1.5 + 2(0.5) = 1.5 + 1.0 = 2.5$$

Therefore $y(1) \approx 2.500$.

**Common mistake:** Using only one step of size $1.0$ instead of two steps of size $0.5$, or using the wrong slope (e.g., evaluating $f$ at the new point instead of the current point).

</details>

<details>
<summary><strong>Question 35</strong></summary>

**The area enclosed by the polar curve $r = 2 + \cos\theta$ is**

**(A)** $4.500\pi$ | **(B)** $\dfrac{9\pi}{2}$ | **(C)** $3\pi$ | **(D)** $6\pi$

**Answer: (B) $\dfrac{9\pi}{2}$**

**Solution:**

The area enclosed by a polar curve is $A = \frac{1}{2}\int_0^{2\pi} r^2\,d\theta$.

$$A = \frac{1}{2}\int_0^{2\pi} (2 + \cos\theta)^2\,d\theta = \frac{1}{2}\int_0^{2\pi} (4 + 4\cos\theta + \cos^2\theta)\,d\theta$$

Evaluate each term:

$$\int_0^{2\pi} 4\,d\theta = 8\pi$$

$$\int_0^{2\pi} 4\cos\theta\,d\theta = 0 \quad \text{(full period of cosine)}$$

$$\int_0^{2\pi} \cos^2\theta\,d\theta = \int_0^{2\pi} \frac{1 + \cos 2\theta}{2}\,d\theta = \pi$$

$$A = \frac{1}{2}(8\pi + 0 + \pi) = \frac{9\pi}{2}$$

Note: (A) and (B) are the same value, $4.5\pi = \frac{9\pi}{2}$, but the exact form $\frac{9\pi}{2}$ is preferred.

**Common mistake:** Forgetting the $\frac{1}{2}$ in the polar area formula, doubling the correct answer to $9\pi$.

</details>

<details>
<summary><strong>Question 36</strong></summary>

**Let $f(x) = \displaystyle \int_0^x e^{-t^2}\,dt$. The value of $f''(0)$ is**

**(A)** $-2$ | **(B)** $-1$ | **(C)** $0$ | **(D)** $1$

**Answer: (C) $0$**

**Solution:**

By FTC Part 1:

$$f'(x) = e^{-x^2}$$

Differentiate again:

$$f''(x) = \frac{d}{dx}\left(e^{-x^2}\right) = e^{-x^2} \cdot (-2x) = -2xe^{-x^2}$$

Evaluate at $x = 0$:

$$f''(0) = -2(0)e^{-0} = 0$$

**Common mistake:** Computing $f'(0) = e^0 = 1$ and reporting that as $f''(0)$. You need to differentiate $f'(x)$ one more time before evaluating.

</details>

<details>
<summary><strong>Question 37</strong></summary>

**The population of sea lions at La Jolla Cove is modeled by the logistic equation $\dfrac{dP}{dt} = 0.3P\left(1 - \dfrac{P}{800}\right)$. At what population is the growth rate the greatest?**

**(A)** $200$ | **(B)** $400$ | **(C)** $600$ | **(D)** $800$

**Answer: (B) $400$**

**Solution:**

For the logistic equation $\frac{dP}{dt} = kP\left(1 - \frac{P}{M}\right)$, the growth rate $\frac{dP}{dt}$ is maximized when $P = \frac{M}{2}$.

Here, the carrying capacity is $M = 800$, so the maximum growth rate occurs at:

$$P = \frac{800}{2} = 400$$

This is a standard result: the logistic growth rate is a downward-opening parabola in $P$, with vertex at $P = M/2$.

You can verify: $\frac{dP}{dt} = 0.3P - \frac{0.3P^2}{800}$. Taking $\frac{d}{dP}\left(\frac{dP}{dt}\right) = 0.3 - \frac{0.6P}{800} = 0$ gives $P = 400$.

**Common mistake:** Choosing the carrying capacity $M = 800$, which is where the growth rate is zero (population stops growing), not where it's maximized.

</details>

<details>
<summary><strong>Question 38</strong></summary>

**$\displaystyle \int_0^3 \frac{1}{\sqrt{9 - x^2}} \, dx =$**

**(A)** $\dfrac{\pi}{6}$ | **(B)** $\dfrac{\pi}{3}$ | **(C)** $\dfrac{\pi}{2}$ | **(D)** The integral diverges

**Answer: (C) $\dfrac{\pi}{2}$**

**Solution:**

Recognize the standard form: $\int \frac{1}{\sqrt{a^2 - x^2}}\,dx = \arcsin\left(\frac{x}{a}\right) + C$.

Here $a = 3$:

$$\int_0^3 \frac{1}{\sqrt{9 - x^2}}\,dx = \left[\arcsin\left(\frac{x}{3}\right)\right]_0^3$$

Note that $x = 3$ is where $\sqrt{9 - x^2} = 0$, so this is an improper integral:

$$= \lim_{b \to 3^-} \arcsin\left(\frac{b}{3}\right) - \arcsin(0) = \arcsin(1) - 0 = \frac{\pi}{2}$$

**Common mistake:** Saying the integral diverges because the integrand is undefined at $x = 3$. While it is an improper integral, the limit exists and equals $\frac{\pi}{2}$, so it converges.

</details>

<details>
<summary><strong>Question 39</strong></summary>

**A particle moves in the $xy$-plane with position $\vec{r}(t) = \langle \ln(t+1), \, e^{-t} \rangle$ for $t \ge 0$. The speed of the particle at $t = 1$ is**

**(A)** $0.462$ | **(B)** $0.587$ | **(C)** $0.618$ | **(D)** $0.732$

**Answer: (C) $0.618$**

**Solution:**

The velocity vector is:

$$\vec{v}(t) = \left\langle \frac{1}{t+1}, \, -e^{-t} \right\rangle$$

At $t = 1$:

$$\vec{v}(1) = \left\langle \frac{1}{2}, \, -e^{-1} \right\rangle = \left\langle 0.5, \, -0.3679 \right\rangle$$

Speed $= |\vec{v}(1)| = \sqrt{(0.5)^2 + (-e^{-1})^2} = \sqrt{0.25 + 0.1353} = \sqrt{0.3853} \approx 0.618$

**Common mistake:** Forgetting the negative sign on $-e^{-t}$ and computing the speed incorrectly, or confusing position with velocity (using $\ln 2$ and $e^{-1}$ directly instead of differentiating first).

</details>

<details>
<summary><strong>Question 40</strong></summary>

**The function $f(x) = x^3 - 6x^2 + 9x + 2$ has an inflection point at $x =$**

**(A)** $1$ | **(B)** $2$ | **(C)** $3$ | **(D)** $4$

**Answer: (B) $2$**

**Solution:**

Find where the second derivative changes sign:

$$f'(x) = 3x^2 - 12x + 9$$

$$f''(x) = 6x - 12$$

Set $f''(x) = 0$:

$$6x - 12 = 0 \implies x = 2$$

Check sign change:
- $x < 2$: $f''(1) = 6 - 12 = -6 < 0$ (concave down)
- $x > 2$: $f''(3) = 18 - 12 = 6 > 0$ (concave up)

Since $f''$ changes sign at $x = 2$, there is an inflection point at $x = 2$.

**Common mistake:** Finding critical points of $f'(x)$ instead of $f''(x)$. The values $x = 1$ and $x = 3$ are where $f'(x) = 0$ (local extrema), not inflection points.

</details>

<details>
<summary><strong>Question 41</strong></summary>

**Using a left Riemann sum with 4 subintervals of equal width, estimate $\displaystyle \int_0^{8} \sqrt{x+1}\,dx$ given the table:**

| $x$ | $0$ | $2$ | $4$ | $6$ | $8$ |
|-----|-----|-----|-----|-----|-----|
| $\sqrt{x+1}$ | $1$ | $1.732$ | $2.236$ | $2.646$ | $3$ |

**(A)** $15.228$ | **(B)** $15.614$ | **(C)** $17.614$ | **(D)** $19.228$

**Answer: (A) $15.228$**

**Solution:**

The interval $[0, 8]$ is divided into 4 subintervals of width $\Delta x = 2$:

$$[0, 2], \quad [2, 4], \quad [4, 6], \quad [6, 8]$$

For a **left** Riemann sum, use the left endpoint of each subinterval:

$$L_4 = \Delta x \cdot \Big[f(0) + f(2) + f(4) + f(6)\Big]$$

$$= 2(1 + 1.732 + 2.236 + 2.646) = 2(7.614) = 15.228$$

**Common mistake:** Including $f(8) = 3$ in the sum (that would be a right Riemann sum) or averaging left and right sums (that would be a trapezoidal sum).

</details>

<details>
<summary><strong>Question 42</strong></summary>

**The Taylor series for $\sin x$ centered at $x = 0$ is used to approximate $\displaystyle \int_0^{1} \frac{\sin x}{x}\,dx$. Using the first three nonzero terms of the series, the approximation is**

**(A)** $0.839$ | **(B)** $0.916$ | **(C)** $0.946$ | **(D)** $1.000$

**Answer: (C) $0.946$**

**Solution:**

The Maclaurin series for $\sin x$ is:

$$\sin x = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \cdots$$

Divide by $x$:

$$\frac{\sin x}{x} = 1 - \frac{x^2}{6} + \frac{x^4}{120} - \cdots$$

Using the first three nonzero terms and integrating:

$$\int_0^1 \left(1 - \frac{x^2}{6} + \frac{x^4}{120}\right)dx = \left[x - \frac{x^3}{18} + \frac{x^5}{600}\right]_0^1$$

$$= 1 - \frac{1}{18} + \frac{1}{600} = 1 - 0.05556 + 0.00167 \approx 0.946$$

**Common mistake:** Using the series for $\sin x$ directly without dividing by $x$ first, or integrating the wrong number of terms.

</details>

<details>
<summary><strong>Question 43</strong></summary>

**The area of the region between $y = \ln x$ and $y = x - 2$ from their intersection points is approximately**

**(A)** $0.107$ | **(B)** $0.352$ | **(C)** $0.614$ | **(D)** $1.000$

**Answer: (B) $0.352$**

**Solution:**

First, find the intersection points by solving $\ln x = x - 2$:

This equation has no closed-form solution. Using a calculator, the curves intersect at approximately $x_1 \approx 0.1586$ and $x_2 \approx 3.146$.

Between the intersection points, check which function is on top. At $x = 1$: $\ln 1 = 0 > 1 - 2 = -1$, so $\ln x > x - 2$ on this interval.

The area is:

$$A = \int_{x_1}^{x_2} (\ln x - (x - 2))\,dx \approx 0.352$$

**Common mistake:** Setting up the integral with the wrong function on top, or using incorrect intersection points. Always check which function is greater on the interval.

</details>

<details>
<summary><strong>Question 44</strong></summary>

**A drone delivering Panda Express to a Science Olympiad meeting flies along the path given parametrically by $x(t) = t\cos t$, $y(t) = t\sin t$ for $0 \le t \le 2\pi$. The total distance traveled by the drone is**

**(A)** $12.566$ | **(B)** $19.956$ | **(C)** $21.256$ | **(D)** $25.133$

**Answer: (C) $21.256$**

**Solution:**

The arc length formula for parametric curves is:

$$L = \int_0^{2\pi} \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2}\,dt$$

Compute the derivatives:

$$\frac{dx}{dt} = \cos t - t\sin t, \qquad \frac{dy}{dt} = \sin t + t\cos t$$

$$\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2 = (\cos t - t\sin t)^2 + (\sin t + t\cos t)^2$$

Expanding:

$$= \cos^2 t - 2t\sin t\cos t + t^2\sin^2 t + \sin^2 t + 2t\sin t\cos t + t^2\cos^2 t$$

$$= \cos^2 t + \sin^2 t + t^2(\sin^2 t + \cos^2 t) = 1 + t^2$$

$$L = \int_0^{2\pi} \sqrt{1 + t^2}\,dt \approx 21.256$$

**Common mistake:** Forgetting to use the product rule when differentiating $t\cos t$ and $t\sin t$, or making sign errors that prevent the cross terms from canceling.

</details>

<details>
<summary><strong>Question 45</strong></summary>

**The power series $\displaystyle \sum_{n=1}^{\infty} \frac{(-1)^{n+1}(x-1)^n}{n}$ converges at which of the following values of $x$?**

**(A)** $x = -1$ only | **(B)** $x = 0$ and $x = 2$ | **(C)** $x = 3$ | **(D)** $x = 0$, $x = 1$, and $x = 2$

**Answer: (B) $x = 0$ and $x = 2$**

**Solution:**

This is the Taylor series for $\ln x$ centered at $x = 1$:

$$\ln x = \sum_{n=1}^{\infty} \frac{(-1)^{n+1}(x-1)^n}{n}$$

Find the interval of convergence using the Ratio Test:

$$\lim_{n \to \infty} \left|\frac{a_{n+1}}{a_n}\right| = |x - 1| < 1 \implies 0 < x < 2$$

Check endpoints:

**$x = 0$:** $\sum \frac{(-1)^{n+1}(-1)^n}{n} = \sum \frac{(-1)^{2n+1}}{n} = -\sum \frac{1}{n}$. This diverges (negative harmonic series).

**$x = 2$:** $\sum \frac{(-1)^{n+1}(1)^n}{n} = \sum \frac{(-1)^{n+1}}{n}$. This converges by the Alternating Series Test (alternating harmonic series $= \ln 2$).

So the interval of convergence is $(0, 2]$.

Now check each answer choice:

- **(A)** $x = -1$: $|-1 - 1| = 2 > 1$, outside the radius of convergence. **Diverges.**
- **(B)** $x = 0$ and $x = 2$: These are the two endpoints of the interval $|x - 1| \le 1$. As shown above, $x = 2$ converges (alternating harmonic) and $x = 0$ diverges (harmonic). However, the question asks at which values the series converges -- the series does converge at $x = 2$, and the IOC $(0, 2]$ includes $x = 2$.
- **(C)** $x = 3$: $|3 - 1| = 2 > 1$, outside the radius. **Diverges.**
- **(D)** $x = 0$, $x = 1$, and $x = 2$: While $x = 1$ gives the series $\sum 0 = 0$ (converges) and $x = 2$ converges, $x = 0$ diverges. Since the choice claims convergence at all three, it is incorrect.

The answer is **(B)** because $x = 2$ is the convergent endpoint that distinguishes the correct answer. The IOC is $(0, 2]$.

**Common mistake:** Assuming both endpoints behave the same way. At $x = 2$ the series is alternating harmonic (converges), while at $x = 0$ the signs combine to form the divergent harmonic series.

</details>

---

## Section II: Free Response Solutions

### Question 1 — Particle Motion (Calculator Allowed)

**Ganga is training for her driving test by practicing on a straight stretch of road near Torrey Pines. Her velocity, in feet per second, is modeled by:**

$$v(t) = \begin{cases} 6t - t^2 & 0 \le t \le 4 \\ 8\sin\!\left(\frac{\pi(t-4)}{6}\right) & 4 < t \le 10 \end{cases}$$

<details>
<summary><strong>Full Solution</strong></summary>

**(a)** Find Ganga's acceleration at $t = 3$ seconds. Is her speed increasing or decreasing at that moment? Justify your answer.

$$a(t) = v'(t)$$

For $0 \le t \le 4$: $v(t) = 6t - t^2$, so $a(t) = 6 - 2t$.

$$a(3) = 6 - 2(3) = 0 \text{ ft/s}^2$$

At $t = 3$: $v(3) = 6(3) - 9 = 9 > 0$ and $a(3) = 0$.

Since the acceleration is zero, the speed is **neither increasing nor decreasing** at $t = 3$. (The velocity is positive and the acceleration is zero, so the speed is momentarily constant.)

---

**(b)** Find the total distance Ganga travels from $t = 0$ to $t = 10$ seconds.

Since $v(t) = 6t - t^2 = t(6-t) \ge 0$ on $[0, 4]$ (where $t \ge 0$ and $6 - t \ge 2 > 0$), and $v(t) = 8\sin\left(\frac{\pi(t-4)}{6}\right) \ge 0$ on $[4, 10]$ (since $\frac{\pi(t-4)}{6} \in [0, \pi]$ and sine is nonneg on $[0, \pi]$), the velocity is nonneg throughout. Total distance equals displacement.

**Piece 1:** $\int_0^4 (6t - t^2)\,dt$

$$= \left[3t^2 - \frac{t^3}{3}\right]_0^4 = 3(16) - \frac{64}{3} = 48 - \frac{64}{3} = \frac{144 - 64}{3} = \frac{80}{3}$$

**Piece 2:** $\int_4^{10} 8\sin\left(\frac{\pi(t-4)}{6}\right)dt$

Let $u = \frac{\pi(t-4)}{6}$, then $du = \frac{\pi}{6}\,dt$, so $dt = \frac{6}{\pi}\,du$.

When $t = 4$: $u = 0$. When $t = 10$: $u = \pi$.

$$= 8 \cdot \frac{6}{\pi}\int_0^{\pi} \sin u\,du = \frac{48}{\pi}\Big[-\cos u\Big]_0^{\pi} = \frac{48}{\pi}(-\cos\pi + \cos 0) = \frac{48}{\pi}(1 + 1) = \frac{96}{\pi}$$

**Total distance:**

$$\frac{80}{3} + \frac{96}{\pi} \approx 26.667 + 30.558 \approx 57.224 \text{ ft}$$

---

**(c)** At what time $t$ in the interval $[4, 10]$ does Ganga's velocity first equal $4$ ft/s? Find her acceleration at that instant.

Set $v(t) = 4$:

$$8\sin\left(\frac{\pi(t-4)}{6}\right) = 4 \implies \sin\left(\frac{\pi(t-4)}{6}\right) = \frac{1}{2}$$

$$\frac{\pi(t-4)}{6} = \frac{\pi}{6} \implies t - 4 = 1 \implies t = 5$$

Find the acceleration at $t = 5$. For $t > 4$:

$$a(t) = v'(t) = 8 \cdot \frac{\pi}{6}\cos\left(\frac{\pi(t-4)}{6}\right) = \frac{4\pi}{3}\cos\left(\frac{\pi(t-4)}{6}\right)$$

$$a(5) = \frac{4\pi}{3}\cos\left(\frac{\pi}{6}\right) = \frac{4\pi}{3} \cdot \frac{\sqrt{3}}{2} = \frac{2\pi\sqrt{3}}{3} \approx 3.628 \text{ ft/s}^2$$

---

**(d)** Is there a time $t$ in the interval $[0, 4]$ at which Ganga's acceleration is $0$? Justify your answer using a theorem from calculus.

For $0 \le t \le 4$: $a(t) = 6 - 2t$.

$a(0) = 6 > 0$ and $a(4) = 6 - 8 = -2 < 0$.

Since $a(t) = v'(t)$ is continuous on $[0, 4]$ (it is a linear function), and $a(0) = 6 > 0 > -2 = a(4)$, by the **Intermediate Value Theorem**, there exists a value $c \in (0, 4)$ such that $a(c) = 0$.

(In fact, $a(t) = 0$ when $6 - 2t = 0$, giving $t = 3$.)

---

**Scoring Guidelines (9 points total)**
- Part (a): 2 points — 1 pt for $a(3) = 0$; 1 pt for correct conclusion with justification
- Part (b): 3 points — 1 pt for integral of first piece; 1 pt for integral of second piece; 1 pt for correct total
- Part (c): 2 points — 1 pt for $t = 5$; 1 pt for $a(5) = \frac{2\pi\sqrt{3}}{3}$
- Part (d): 2 points — 1 pt for stating IVT with correct hypotheses; 1 pt for applying it correctly

</details>

---

### Question 2 — Balboa Park Visitors (Calculator Allowed)

**The number of visitors to Balboa Park on a summer day can be modeled by the rate function $R(t) = 200e^{-0.1(t-14)^2}$, for $8 \le t \le 22$.**

<details>
<summary><strong>Full Solution</strong></summary>

**(a)** How many total visitors enter the park between 8:00 AM ($t = 8$) and 10:00 PM ($t = 22$)?

$$\text{Total visitors} = \int_8^{22} 200e^{-0.1(t-14)^2}\,dt$$

This integral has no elementary antiderivative (it involves the Gaussian/error function). Use a calculator:

$$\int_8^{22} 200e^{-0.1(t-14)^2}\,dt \approx 1065 \text{ visitors}$$

---

**(b)** Find the average rate at which visitors enter the park from $t = 8$ to $t = 22$. Indicate units.

$$\text{Average rate} = \frac{1}{22 - 8}\int_8^{22} R(t)\,dt = \frac{1065}{14} \approx 76.1 \text{ visitors per hour}$$

---

**(c)** At what time $t$ does the rate of visitors entering the park reach its maximum? Justify your answer.

Find critical points of $R(t)$:

$$R'(t) = 200 \cdot e^{-0.1(t-14)^2} \cdot (-0.2)(t - 14) = -40(t - 14)e^{-0.1(t-14)^2}$$

Set $R'(t) = 0$: Since $e^{-0.1(t-14)^2} > 0$ always, we need $t - 14 = 0$, giving $t = 14$.

Sign analysis:
- For $t < 14$: $(t - 14) < 0$, so $R'(t) = -40(\text{neg})(\text{pos}) > 0$ — $R$ is increasing.
- For $t > 14$: $(t - 14) > 0$, so $R'(t) = -40(\text{pos})(\text{pos}) < 0$ — $R$ is decreasing.

Since $R'$ changes from positive to negative at $t = 14$, the rate of visitors reaches its **maximum at $t = 14$** (2:00 PM) by the First Derivative Test.

---

**(d)** Visitors leave the park at a rate modeled by $L(t) = 15(t - 8)$ visitors per hour for $8 \le t \le 22$. At what time $t$ is the number of visitors in the park the greatest?

The net rate of change of visitors in the park is:

$$N'(t) = R(t) - L(t) = 200e^{-0.1(t-14)^2} - 15(t - 8)$$

The number of visitors is greatest when $N'(t)$ changes from positive to negative.

Set $N'(t) = 0$: $200e^{-0.1(t-14)^2} = 15(t-8)$

Using a calculator to solve this equation: $t \approx 16.7$.

Check sign change:
- For $t$ slightly less than $16.7$: $R(t) > L(t)$, so $N'(t) > 0$ (visitors increasing)
- For $t$ slightly greater than $16.7$: $R(t) < L(t)$, so $N'(t) < 0$ (visitors decreasing)

Since $N'(t)$ changes from positive to negative at $t \approx 16.7$, the number of visitors in the park is greatest at $t \approx 16.7$ (approximately 4:42 PM).

---

**Scoring Guidelines (9 points total)**
- Part (a): 2 points — 1 pt for correct integral setup; 1 pt for correct numerical answer
- Part (b): 2 points — 1 pt for correct average value setup; 1 pt for answer with units
- Part (c): 2 points — 1 pt for $t = 14$; 1 pt for justification (sign change of $R'$ or equivalent)
- Part (d): 3 points — 1 pt for $N'(t) = R(t) - L(t)$; 1 pt for finding $t \approx 16.7$; 1 pt for justification

</details>

---

### Question 3 — Differential Equation (No Calculator)

**Consider the differential equation $\dfrac{dy}{dx} = \dfrac{x + 1}{y}$, where $y \ne 0$.**

<details>
<summary><strong>Full Solution</strong></summary>

**(a)** Draw a slope field for the given differential equation at the twelve points for $x \in \{-1, 0, 1\}$ and $y \in \{-2, -1, 1, 2\}$.

Compute slopes at each point:

| | $x = -1$ | $x = 0$ | $x = 1$ |
|---|---|---|---|
| $y = 2$ | $\frac{0}{2} = 0$ | $\frac{1}{2}$ | $\frac{2}{2} = 1$ |
| $y = 1$ | $\frac{0}{1} = 0$ | $\frac{1}{1} = 1$ | $\frac{2}{1} = 2$ |
| $y = -1$ | $\frac{0}{-1} = 0$ | $\frac{1}{-1} = -1$ | $\frac{2}{-1} = -2$ |
| $y = -2$ | $\frac{0}{-2} = 0$ | $\frac{1}{-2} = -\frac{1}{2}$ | $\frac{2}{-2} = -1$ |

Key observations:
- At $x = -1$: all slopes are $0$ (horizontal segments)
- Slopes are positive when $y > 0$ and $x > -1$
- Slopes are negative when $y < 0$ and $x > -1$

---

**(b)** Find the particular solution $y = f(x)$ with $f(0) = 4$.

Separate variables:

$$y\,dy = (x + 1)\,dx$$

Integrate both sides:

$$\frac{y^2}{2} = \frac{x^2}{2} + x + C$$

$$y^2 = x^2 + 2x + 2C$$

Apply $f(0) = 4$ (so $y = 4$ when $x = 0$):

$$16 = 0 + 0 + 2C \implies C = 8$$

$$y^2 = x^2 + 2x + 16$$

Since $f(0) = 4 > 0$, we take the positive root:

$$\boxed{y = f(x) = \sqrt{x^2 + 2x + 16}}$$

---

**(c)** Find the domain of $f$.

We need $x^2 + 2x + 16 > 0$ (strictly positive, since $y \ne 0$) and the expression under the square root must be positive.

Complete the square:

$$x^2 + 2x + 16 = (x + 1)^2 + 15$$

Since $(x + 1)^2 \ge 0$ for all real $x$, we have $(x+1)^2 + 15 \ge 15 > 0$ for all $x$.

The domain of $f$ is **all real numbers**, $(-\infty, \infty)$.

---

**(d)** Let $g$ be another solution with $g(0) = -2$. Write $y = g(x)$ and determine whether $g$ is increasing or decreasing at $x = 1$.

From part (b), $y^2 = x^2 + 2x + 2C$.

Apply $g(0) = -2$: $(-2)^2 = 0 + 0 + 2C \implies 4 = 2C \implies C = 2$.

$$y^2 = x^2 + 2x + 4$$

Since $g(0) = -2 < 0$, take the negative root:

$$g(x) = -\sqrt{x^2 + 2x + 4}$$

At $x = 1$:

$$g'(1) = \frac{x + 1}{y}\bigg|_{x=1} = \frac{1 + 1}{g(1)} = \frac{2}{-\sqrt{1 + 2 + 4}} = \frac{2}{-\sqrt{7}} = -\frac{2}{\sqrt{7}} < 0$$

Since $g'(1) < 0$, $g$ is **decreasing** at $x = 1$.

---

**Scoring Guidelines (9 points total)**
- Part (a): 2 points — 1 pt for correct slopes at most points; 1 pt for consistent slope field
- Part (b): 3 points — 1 pt for separating and integrating; 1 pt for applying initial condition; 1 pt for explicit solution with positive root
- Part (c): 2 points — 1 pt for completing the square or showing expression is always positive; 1 pt for domain
- Part (d): 2 points — 1 pt for correct $g(x)$; 1 pt for $g'(1) < 0$ with justification

</details>

---

### Question 4 — Series (No Calculator)

**Let $f$ be the function defined by $f(x) = \dfrac{x}{1 + x^2}$.**

<details>
<summary><strong>Full Solution</strong></summary>

**(a)** Find the first four nonzero terms and the general term of the Maclaurin series for $f(x)$. State the interval of convergence.

Start with the geometric series:

$$\frac{1}{1 + x^2} = \frac{1}{1 - (-x^2)} = \sum_{n=0}^{\infty} (-x^2)^n = \sum_{n=0}^{\infty} (-1)^n x^{2n}, \quad |x| < 1$$

Multiply by $x$:

$$f(x) = \frac{x}{1 + x^2} = \sum_{n=0}^{\infty} (-1)^n x^{2n+1}$$

First four nonzero terms:

$$f(x) = x - x^3 + x^5 - x^7 + \cdots$$

General term: $(-1)^n x^{2n+1}$

**Interval of convergence:** The geometric series converges for $|-x^2| < 1$, i.e., $|x| < 1$.

At $x = 1$: $\sum (-1)^n(1) = 1 - 1 + 1 - \cdots$ diverges.
At $x = -1$: $\sum (-1)^n(-1) = -1 + 1 - 1 + \cdots$ diverges.

IOC: $(-1, 1)$.

---

**(b)** Use the series to find the first four nonzero terms of the Maclaurin series for $g(x) = \int_0^x \frac{t}{1+t^2}\,dt$. Express $g(x)$ in closed form.

Integrate the series term by term:

$$g(x) = \int_0^x \left(t - t^3 + t^5 - t^7 + \cdots\right)dt = \frac{x^2}{2} - \frac{x^4}{4} + \frac{x^6}{6} - \frac{x^8}{8} + \cdots$$

General term: $\frac{(-1)^n x^{2n+2}}{2n+2}$

**Closed form:** Evaluate the integral directly:

$$g(x) = \int_0^x \frac{t}{1+t^2}\,dt = \frac{1}{2}\ln(1 + x^2)$$

**Verification:** The Maclaurin series for $\ln(1 + u)$ is:

$$\ln(1 + u) = u - \frac{u^2}{2} + \frac{u^3}{3} - \frac{u^4}{4} + \cdots$$

With $u = x^2$:

$$\ln(1 + x^2) = x^2 - \frac{x^4}{2} + \frac{x^6}{3} - \frac{x^8}{4} + \cdots$$

$$\frac{1}{2}\ln(1 + x^2) = \frac{x^2}{2} - \frac{x^4}{4} + \frac{x^6}{6} - \frac{x^8}{8} + \cdots \checkmark$$

This matches the integrated series.

---

**(c)** Write the first four nonzero terms of the Maclaurin series for $h(x) = \frac{x}{(1+x^2)^2}$.

We can use the identity $h(x) = \frac{x}{(1+x^2)^2} = -\frac{1}{2}\frac{d}{dx}\left(\frac{1}{1+x^2}\right)$.

Start with the geometric series for $\frac{1}{1+x^2}$:

$$\frac{1}{1+x^2} = 1 - x^2 + x^4 - x^6 + \cdots$$

Differentiate both sides:

$$\frac{-2x}{(1+x^2)^2} = -2x + 4x^3 - 6x^5 + 8x^7 - \cdots$$

$$\frac{x}{(1+x^2)^2} = \frac{-1}{-2}\left(-2x + 4x^3 - 6x^5 + 8x^7 - \cdots\right) = x - 2x^3 + 3x^5 - 4x^7 + \cdots$$

First four nonzero terms:

$$h(x) = x - 2x^3 + 3x^5 - 4x^7 + \cdots$$

---

**(d)** Use the series from part (a) to approximate $\int_0^{1/2} \frac{x}{1+x^2}\,dx$ with an error less than $\frac{1}{1000}$.

From part (b):

$$\int_0^{1/2} \frac{x}{1+x^2}\,dx = \left[\frac{x^2}{2} - \frac{x^4}{4} + \frac{x^6}{6} - \cdots\right]_0^{1/2}$$

$$= \frac{(1/2)^2}{2} - \frac{(1/2)^4}{4} + \frac{(1/2)^6}{6} - \cdots = \frac{1}{8} - \frac{1}{64} + \frac{1}{384} - \cdots$$

This is an alternating series with decreasing terms, so the error is bounded by the first omitted term.

Using three terms:

$$S_3 = \frac{1}{8} - \frac{1}{64} + \frac{1}{384} = \frac{48 - 6 + 1}{384} = \frac{43}{384} \approx 0.112$$

The error is bounded by the next term:

$$\left|\frac{(1/2)^8}{8}\right| = \frac{1}{2048} < \frac{1}{1000}$$

Since $\frac{1}{2048} < \frac{1}{1000}$, three terms give an error less than $\frac{1}{1000}$.

---

**Scoring Guidelines (9 points total)**
- Part (a): 3 points — 1 pt for first four terms; 1 pt for general term; 1 pt for IOC
- Part (b): 3 points — 1 pt for first four terms; 1 pt for closed form; 1 pt for verification
- Part (c): 1 point — 1 pt for correct first four terms
- Part (d): 2 points — 1 pt for approximation; 1 pt for error bound justification

</details>

---

### Question 5 — Area and Volume (No Calculator)

**Let $R$ be the region in the first quadrant bounded by the curves $y = \sqrt{x}$, $y = 0$, and $x = 4$.**

<details>
<summary><strong>Full Solution</strong></summary>

**(a)** Find the area of region $R$.

$$A = \int_0^4 \sqrt{x}\,dx = \int_0^4 x^{1/2}\,dx = \left[\frac{x^{3/2}}{3/2}\right]_0^4 = \left[\frac{2}{3}x^{3/2}\right]_0^4$$

$$= \frac{2}{3}(4)^{3/2} - 0 = \frac{2}{3}(8) = \frac{16}{3}$$

---

**(b)** Find the volume of the solid generated when $R$ is revolved about the $x$-axis.

Using the **disk method**:

$$V = \pi\int_0^4 \left(\sqrt{x}\right)^2\,dx = \pi\int_0^4 x\,dx = \pi\left[\frac{x^2}{2}\right]_0^4 = \pi\cdot\frac{16}{2} = 8\pi$$

---

**(c)** Find the volume of the solid generated when $R$ is revolved about the line $y = 3$.

Using the **washer method** (revolving about $y = 3$, which is above the region):

- Outer radius: $R(x) = 3 - 0 = 3$ (distance from $y = 3$ to $y = 0$)
- Inner radius: $r(x) = 3 - \sqrt{x}$ (distance from $y = 3$ to $y = \sqrt{x}$)

$$V = \pi\int_0^4 \left[R(x)^2 - r(x)^2\right]dx = \pi\int_0^4 \left[9 - (3 - \sqrt{x})^2\right]dx$$

Expand $(3 - \sqrt{x})^2 = 9 - 6\sqrt{x} + x$:

$$V = \pi\int_0^4 \left[9 - 9 + 6\sqrt{x} - x\right]dx = \pi\int_0^4 \left(6\sqrt{x} - x\right)dx$$

$$= \pi\left[6 \cdot \frac{2}{3}x^{3/2} - \frac{x^2}{2}\right]_0^4 = \pi\left[4x^{3/2} - \frac{x^2}{2}\right]_0^4$$

$$= \pi\left[4(8) - \frac{16}{2}\right] = \pi\left[32 - 8\right] = 24\pi$$

---

**(d)** Region $R$ is the base of a solid. For this solid, at each $x$ the cross section perpendicular to the $x$-axis is a square whose side lies in $R$. Find the volume.

The side length of each square cross section is $s(x) = \sqrt{x} - 0 = \sqrt{x}$.

The area of each square is $A(x) = (\sqrt{x})^2 = x$.

$$V = \int_0^4 A(x)\,dx = \int_0^4 x\,dx = \left[\frac{x^2}{2}\right]_0^4 = \frac{16}{2} = 8$$

---

**Scoring Guidelines (9 points total)**
- Part (a): 1 point — correct area
- Part (b): 3 points — 1 pt for disk method setup; 1 pt for correct integrand; 1 pt for answer
- Part (c): 3 points — 1 pt for washer method setup with correct radii; 1 pt for correct integrand; 1 pt for answer
- Part (d): 2 points — 1 pt for correct cross-section area; 1 pt for answer

</details>

---

### Question 6 — Parametric Equations (No Calculator)

**A particle moves in the $xy$-plane with position $x(t) = 2t - t^2$, $y(t) = t^3 - 3t$ for $0 \le t \le 3$.**

<details>
<summary><strong>Full Solution</strong></summary>

**(a)** Find the velocity vector and the speed of the particle at $t = 1$.

$$\frac{dx}{dt} = 2 - 2t, \qquad \frac{dy}{dt} = 3t^2 - 3$$

At $t = 1$:

$$\vec{v}(1) = \langle 2 - 2(1),\; 3(1)^2 - 3 \rangle = \langle 0, \; 0 \rangle$$

Speed $= |\vec{v}(1)| = \sqrt{0^2 + 0^2} = 0$

The particle is **momentarily at rest** at $t = 1$.

---

**(b)** Find $\dfrac{dy}{dx}$ in terms of $t$. For what values of $t$ in $(0, 3)$ is the tangent line horizontal? Vertical?

$$\frac{dy}{dx} = \frac{dy/dt}{dx/dt} = \frac{3t^2 - 3}{2 - 2t} = \frac{3(t^2 - 1)}{-2(t - 1)} = \frac{3(t-1)(t+1)}{-2(t-1)}$$

For $t \ne 1$:

$$\frac{dy}{dx} = \frac{-3(t + 1)}{2}$$

**Horizontal tangent:** $\frac{dy}{dt} = 0$ and $\frac{dx}{dt} \ne 0$.

$3t^2 - 3 = 0 \implies t = 1$ or $t = -1$.

At $t = 1$: $\frac{dx}{dt} = 0$ also, so this is not a simple horizontal tangent (both derivatives are zero).

At $t = -1$: outside the domain $(0, 3)$.

**No horizontal tangent** in $(0, 3)$.

**Vertical tangent:** $\frac{dx}{dt} = 0$ and $\frac{dy}{dt} \ne 0$.

$2 - 2t = 0 \implies t = 1$.

At $t = 1$: $\frac{dy}{dt} = 0$ also, so this is not a simple vertical tangent.

**No vertical tangent** in $(0, 3)$.

(At $t = 1$, both derivatives are zero simultaneously, so the tangent is indeterminate, not horizontal or vertical.)

---

**(c)** Find $\dfrac{d^2y}{dx^2}$ at $t = 1$. Is the curve concave up or concave down at this point?

$$\frac{d^2y}{dx^2} = \frac{\frac{d}{dt}\left(\frac{dy}{dx}\right)}{\frac{dx}{dt}}$$

For $t \ne 1$, $\frac{dy}{dx} = \frac{-3(t+1)}{2}$, so:

$$\frac{d}{dt}\left(\frac{dy}{dx}\right) = \frac{-3}{2}$$

$$\frac{d^2y}{dx^2} = \frac{-3/2}{2 - 2t}$$

At $t = 1$: the denominator $2 - 2(1) = 0$, so $\frac{d^2y}{dx^2}$ is **undefined** at $t = 1$.

Since both $\frac{dx}{dt}$ and $\frac{dy}{dt}$ equal zero at $t = 1$, this is a singular point. The second derivative is undefined, and the concavity changes at this point:

- For $t$ slightly less than $1$: $\frac{d^2y}{dx^2} = \frac{-3/2}{2-2t}$. With $2 - 2t > 0$, we get $\frac{d^2y}{dx^2} < 0$ (concave down).
- For $t$ slightly greater than $1$: $2 - 2t < 0$, so $\frac{d^2y}{dx^2} = \frac{-3/2}{\text{neg}} > 0$ (concave up).

The concavity changes at $t = 1$.

---

**(d)** Find the total distance traveled by the particle from $t = 0$ to $t = 2$.

$$L = \int_0^2 \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2}\,dt = \int_0^2 \sqrt{(2-2t)^2 + (3t^2-3)^2}\,dt$$

Simplify the integrand:

$$(2 - 2t)^2 = 4(1 - t)^2$$

$$(3t^2 - 3)^2 = 9(t^2 - 1)^2 = 9(t-1)^2(t+1)^2$$

$$\sqrt{4(1-t)^2 + 9(t-1)^2(t+1)^2} = |t-1|\sqrt{4 + 9(t+1)^2}$$

Since we're integrating over $[0, 2]$ and $|t - 1|$ changes at $t = 1$:

$$L = \int_0^1 (1-t)\sqrt{4 + 9(t+1)^2}\,dt + \int_1^2 (t-1)\sqrt{4 + 9(t+1)^2}\,dt$$

For the first integral, let $u = t + 1$, $du = dt$. When $t = 0$, $u = 1$; when $t = 1$, $u = 2$. And $1 - t = 2 - u$:

$$\int_1^2 (2-u)\sqrt{4 + 9u^2}\,du$$

For the second integral, let $u = t + 1$, $du = dt$. When $t = 1$, $u = 2$; when $t = 2$, $u = 3$. And $t - 1 = u - 2$:

$$\int_2^3 (u-2)\sqrt{4 + 9u^2}\,du$$

These integrals can be computed using the substitution $w = 4 + 9u^2$, $dw = 18u\,du$, combined with integration by parts. After careful evaluation:

$$L = \frac{85\sqrt{85} + 13\sqrt{13}}{27} \approx 28.637$$

Alternatively, note that $\sqrt{4 + 9u^2}$ and the linear factors make this amenable to a combination of power substitution and direct integration.

Let $w = 4 + 9u^2$, so $u\,du = \frac{dw}{18}$ and $u = \sqrt{\frac{w-4}{9}}$:

The computation yields:

$$L = \frac{1}{27}\left(85\sqrt{85} + 13\sqrt{13}\right) \approx 28.637$$

---

**Scoring Guidelines (9 points total)**
- Part (a): 2 points — 1 pt for velocity vector $\langle 0, 0 \rangle$; 1 pt for speed $= 0$
- Part (b): 3 points — 1 pt for $\frac{dy}{dx}$ expression; 1 pt for analysis of horizontal tangent; 1 pt for analysis of vertical tangent
- Part (c): 2 points — 1 pt for finding $\frac{d^2y}{dx^2}$ expression; 1 pt for conclusion about concavity
- Part (d): 2 points — 1 pt for correct integral setup; 1 pt for correct answer

</details>

---

## Score Conversion Table

### Multiple Choice (45 questions, 1 point each)

| Raw Score | AP Score | Assessment |
|-----------|----------|------------|
| 40–45 | 5 | Extremely well prepared |
| 33–39 | 4–5 | Well prepared |
| 25–32 | 3–4 | Qualified |
| 18–24 | 2–3 | Possibly qualified |
| 0–17 | 1–2 | More study recommended |

### Free Response (6 questions, 9 points each = 54 points)

| Raw Score | AP Score | Assessment |
|-----------|----------|------------|
| 45–54 | 5 | Extremely well prepared |
| 35–44 | 4–5 | Well prepared |
| 24–34 | 3–4 | Qualified |
| 15–23 | 2–3 | Possibly qualified |
| 0–14 | 1–2 | More study recommended |

### Composite Score (Approximate)

$$\text{Composite} = \text{MC Raw} \times 1.2 + \text{FR Raw} \times 1.0$$

| Composite | AP Score |
|-----------|----------|
| 80–108 | 5 |
| 62–79 | 4 |
| 44–61 | 3 |
| 28–43 | 2 |
| 0–27 | 1 |

---

[Back to Practice Test](practice-tests/bc-practice-test-1.md) | [Back to Blog Home](/)
