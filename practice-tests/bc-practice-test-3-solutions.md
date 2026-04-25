# AP Calculus BC — Practice Test 3: Solutions

> Complete answer key and detailed solutions — Project Leviathan
> April 2026

---

## Quick Answer Key

### Section I — Multiple Choice

| Q | Ans | Q | Ans | Q | Ans | Q | Ans | Q | Ans |
|---|-----|---|-----|---|-----|---|-----|---|-----|
| 1 | B | 10 | A | 19 | D | 28 | C | 37 | D |
| 2 | C | 11 | C | 20 | C | 29 | A | 38 | A |
| 3 | A | 12 | B | 21 | A | 30 | B | 39 | C |
| 4 | D | 13 | A | 22 | D | 31 | D | 40 | B |
| 5 | B | 14 | D | 23 | B | 32 | C | 41 | D |
| 6 | A | 15 | B | 24 | C | 33 | B | 42 | B |
| 7 | C | 16 | C | 25 | A | 34 | A | 43 | A |
| 8 | B | 17 | A | 26 | D | 35 | C | 44 | C |
| 9 | D | 18 | B | 27 | B | 36 | B | 45 | D |

---

## Section I: Multiple Choice Solutions

### Part A — No Calculator

<details>
<summary><strong>Question 1</strong></summary>

**The salinity of seawater sampled at depth $d$ meters is modeled by $S(d) = \dfrac{5d^2 + 8d}{d^2 + 4}$ parts per thousand. As Leviathan descends indefinitely, the steady-state salinity $\displaystyle \lim_{d \to \infty} S(d) =$**

**(A)** $0$ | **(B)** $5$ | **(C)** $2$ | **(D)** $8$

**Answer: (B) $5$**

**Solution:**

The numerator and denominator are both degree-2 polynomials. When the degrees match, the limit at infinity is the ratio of the leading coefficients:

$$\lim_{d \to \infty} \frac{5d^2 + 8d}{d^2 + 4} = \frac{5}{1} = 5$$

To verify, divide every term by $d^2$:

$$\lim_{d \to \infty} \frac{5 + \dfrac{8}{d}}{1 + \dfrac{4}{d^2}} = \frac{5 + 0}{1 + 0} = 5$$

**Common mistake:** Using the ratio of the non-leading terms $\dfrac{8}{4} = 2$ and choosing (C), or using the ratio of the $d^1$-coefficient to the $d^0$-coefficient instead of comparing leading terms.

</details>

<details>
<summary><strong>Question 2</strong></summary>

**The power output of Leviathan's thruster during a lab test is modeled by $P(t) = t^3 \ln t$ kilowatts for $t > 0$. The derivative $P'(t)$ is**

**(A)** $3t^2 \ln t$ | **(B)** $t^2$ | **(C)** $t^2(3\ln t + 1)$ | **(D)** $t^2(3\ln t - 1)$

**Answer: (C) $t^2(3\ln t + 1)$**

**Solution:**

Apply the product rule with $u = t^3$ and $v = \ln t$:

$$P'(t) = (t^3)' \cdot \ln t + t^3 \cdot (\ln t)'$$

$$= 3t^2 \ln t + t^3 \cdot \frac{1}{t}$$

$$= 3t^2 \ln t + t^2$$

$$= t^2(3\ln t + 1)$$

**Common mistake:** Forgetting the second term of the product rule and choosing (A), which only accounts for differentiating $t^3$ while treating $\ln t$ as a constant.

</details>

<details>
<summary><strong>Question 3</strong></summary>

**The temperature gradient in a water column above a hydrothermal vent is $T(z) = \dfrac{e^{2z}}{z^2 + 1}$ degrees Celsius. The derivative $T'(z)$ is**

**(A)** $\dfrac{2e^{2z}(z^2 + 1) - 2ze^{2z}}{(z^2 + 1)^2}$ | **(B)** $\dfrac{2e^{2z}}{2z}$ | **(C)** $\dfrac{e^{2z}(2z^2 + 2z + 2)}{(z^2 + 1)^2}$ | **(D)** $\dfrac{2e^{2z}(z^2 + 1) + 2ze^{2z}}{(z^2 + 1)^2}$

**Answer: (A) $\dfrac{2e^{2z}(z^2 + 1) - 2ze^{2z}}{(z^2 + 1)^2}$**

**Solution:**

Apply the quotient rule with $u = e^{2z}$ and $v = z^2 + 1$:

$$T'(z) = \frac{u'v - uv'}{v^2}$$

Compute each derivative:
- $u' = 2e^{2z}$ (chain rule)
- $v' = 2z$

Substitute:

$$T'(z) = \frac{2e^{2z}(z^2 + 1) - e^{2z}(2z)}{(z^2 + 1)^2} = \frac{2e^{2z}(z^2 + 1) - 2ze^{2z}}{(z^2 + 1)^2}$$

This can also be factored as $\dfrac{e^{2z}(2z^2 + 2 - 2z)}{(z^2 + 1)^2}$, which confirms the numerator structure.

**Common mistake:** Getting a plus sign instead of a minus sign in the quotient rule (choosing D), or oversimplifying by canceling incorrectly (choosing B).

</details>

<details>
<summary><strong>Question 4</strong></summary>

**The hull pressure $P$ and internal volume $V$ of Leviathan's pressure chamber satisfy $P^3 + V^3 = 9$. At the test point where $P = 1$ and $V = 2$, $\dfrac{dP}{dV} =$**

**(A)** $-\dfrac{1}{4}$ | **(B)** $\dfrac{4}{1}$ | **(C)** $-8$ | **(D)** $-4$

**Answer: (D) $-4$**

**Solution:**

First verify the point: $1^3 + 2^3 = 1 + 8 = 9$. Checks out.

Differentiate both sides implicitly with respect to $V$:

$$3P^2 \frac{dP}{dV} + 3V^2 = 0$$

Solve for $\dfrac{dP}{dV}$:

$$\frac{dP}{dV} = -\frac{3V^2}{3P^2} = -\frac{V^2}{P^2}$$

Substitute $P = 1$, $V = 2$:

$$\frac{dP}{dV} = -\frac{2^2}{1^2} = -\frac{4}{1} = -4$$

**Common mistake:** Inverting the fraction and computing $-\dfrac{P^2}{V^2} = -\dfrac{1}{4}$, which gives $\dfrac{dV}{dP}$ instead of $\dfrac{dP}{dV}$.

</details>

<details>
<summary><strong>Question 5</strong></summary>

**Ocean current speed at a calibration station is modeled by $v(t) = t^3 - 6t^2 + 9t$ knots for $0 \le t \le 5$ hours. The current speed reaches a local maximum at $t =$**

**(A)** $0$ | **(B)** $1$ | **(C)** $3$ | **(D)** $5$

**Answer: (B) $1$**

**Solution:**

Find critical points by setting $v'(t) = 0$:

$$v'(t) = 3t^2 - 12t + 9 = 3(t^2 - 4t + 3) = 3(t - 1)(t - 3) = 0$$

Critical points: $t = 1$ and $t = 3$.

Use the second derivative test: $v''(t) = 6t - 12$.

- At $t = 1$: $v''(1) = 6 - 12 = -6 < 0 \implies$ **local maximum**
- At $t = 3$: $v''(3) = 18 - 12 = 6 > 0 \implies$ local minimum

Therefore the local maximum occurs at $t = 1$, where $v(1) = 1 - 6 + 9 = 4$ knots.

**Common mistake:** Confusing the local maximum and minimum, or evaluating $v(t)$ at the endpoints $t = 0$ and $t = 5$ without testing the interior critical points.

</details>

<details>
<summary><strong>Question 6</strong></summary>

**During instrument calibration, an engineer evaluates $\displaystyle \int 4x^3 e^{x^4}\,dx =$**

**(A)** $e^{x^4} + C$ | **(B)** $4x^3 e^{x^4} + C$ | **(C)** $x^4 e^{x^4} + C$ | **(D)** $\dfrac{e^{x^4}}{x^4} + C$

**Answer: (A) $e^{x^4} + C$**

**Solution:**

Use $u$-substitution. Let $u = x^4$, so $du = 4x^3\,dx$.

The integral transforms directly:

$$\int 4x^3 e^{x^4}\,dx = \int e^u\,du = e^u + C = e^{x^4} + C$$

Verify by differentiating: $\dfrac{d}{dx}\left[e^{x^4}\right] = e^{x^4} \cdot 4x^3$. Correct.

**Common mistake:** Choosing (B) by thinking the integrand itself is the antiderivative, or choosing (C) by incorrectly applying a power-times-exponential pattern.

</details>

<details>
<summary><strong>Question 7</strong></summary>

**The amplitude of a sonar ping reflected off the seafloor decays as $A(\theta) = \dfrac{\sin 3\theta}{\theta}$ for small angles $\theta$. $\displaystyle \lim_{\theta \to 0} \frac{\sin 3\theta}{\theta} =$**

**(A)** $0$ | **(B)** $1$ | **(C)** $3$ | **(D)** $\dfrac{1}{3}$

**Answer: (C) $3$**

**Solution:**

Multiply and divide by $3$ to create the standard limit form:

$$\lim_{\theta \to 0} \frac{\sin 3\theta}{\theta} = \lim_{\theta \to 0} 3 \cdot \frac{\sin 3\theta}{3\theta}$$

Let $u = 3\theta$. As $\theta \to 0$, $u \to 0$:

$$= 3 \cdot \lim_{u \to 0} \frac{\sin u}{u} = 3 \cdot 1 = 3$$

**Common mistake:** Forgetting the factor of $3$ and applying $\lim \dfrac{\sin u}{u} = 1$ directly without adjusting the argument, giving the incorrect answer (B).

</details>

<details>
<summary><strong>Question 8</strong></summary>

**Leviathan's buoyancy control system requires the limit $\displaystyle \lim_{x \to 0} \frac{e^{3x} - 3x - 1}{x^2}$. Using L'Hôpital's Rule, this limit equals**

**(A)** $1$ | **(B)** $\dfrac{9}{2}$ | **(C)** $3$ | **(D)** $0$

**Answer: (B) $\dfrac{9}{2}$**

**Solution:**

Check the form: at $x = 0$, the numerator is $1 - 0 - 1 = 0$ and the denominator is $0$. This is $\dfrac{0}{0}$, so apply L'Hôpital's Rule:

$$\lim_{x \to 0} \frac{3e^{3x} - 3}{2x}$$

At $x = 0$: numerator $= 3 - 3 = 0$, denominator $= 0$. Still $\dfrac{0}{0}$, so apply L'Hôpital's Rule again:

$$\lim_{x \to 0} \frac{9e^{3x}}{2} = \frac{9 \cdot 1}{2} = \frac{9}{2}$$

Alternatively, use the Maclaurin series: $e^{3x} = 1 + 3x + \dfrac{9x^2}{2} + \cdots$

$$\frac{e^{3x} - 3x - 1}{x^2} = \frac{\frac{9x^2}{2} + \text{higher order}}{x^2} \to \frac{9}{2}$$

**Common mistake:** Applying L'Hôpital's Rule only once, getting $\dfrac{3e^{3x}-3}{2x}$, and evaluating at $x = 0$ as $\dfrac{0}{0}$ but then stopping or making an arithmetic error instead of applying the rule a second time.

</details>

<details>
<summary><strong>Question 9</strong></summary>

**The angle of Leviathan's robotic arm is given by $\phi(t) = \arcsin(2t)$. The angular velocity $\phi'(t)$ is**

**(A)** $\dfrac{1}{\sqrt{1 - 4t^2}}$ | **(B)** $\dfrac{2}{\sqrt{1 - 2t^2}}$ | **(C)** $\dfrac{1}{\sqrt{1 - 2t^2}}$ | **(D)** $\dfrac{2}{\sqrt{1 - 4t^2}}$

**Answer: (D) $\dfrac{2}{\sqrt{1 - 4t^2}}$**

**Solution:**

Use the chain rule with $\dfrac{d}{dt}[\arcsin(u)] = \dfrac{u'}{\sqrt{1 - u^2}}$ where $u = 2t$:

$$\phi'(t) = \frac{(2t)'}{\sqrt{1 - (2t)^2}} = \frac{2}{\sqrt{1 - 4t^2}}$$

**Common mistake:** Forgetting the chain rule factor of $2$ (choosing A), or incorrectly squaring only the coefficient to get $1 - 2t^2$ in the denominator instead of $1 - 4t^2$ (choosing B).

</details>

<details>
<summary><strong>Question 10</strong></summary>

**The work done by Leviathan's ballast pump over one full cycle is $\displaystyle \int_0^{2\pi} 4\cos^2 t \, dt =$**

**(A)** $4\pi$ | **(B)** $2\pi$ | **(C)** $\pi$ | **(D)** $8\pi$

**Answer: (A) $4\pi$**

**Solution:**

Use the power-reduction identity $\cos^2 t = \dfrac{1 + \cos 2t}{2}$:

$$\int_0^{2\pi} 4\cos^2 t\,dt = \int_0^{2\pi} 4 \cdot \frac{1 + \cos 2t}{2}\,dt = \int_0^{2\pi} (2 + 2\cos 2t)\,dt$$

$$= \left[2t + \sin 2t\right]_0^{2\pi} = (4\pi + \sin 4\pi) - (0 + \sin 0) = 4\pi + 0 - 0 = 4\pi$$

Note: The $\sin 2t$ term vanishes because $\sin$ is zero at both endpoints.

**Common mistake:** Forgetting to apply the power-reduction formula and incorrectly integrating $4\cos^2 t$ as $4 \cdot \dfrac{\sin 2t}{2}$, or dropping the factor of $4$ and getting $\pi$ or $2\pi$.

</details>

<details>
<summary><strong>Question 11</strong></summary>

**The depth of Leviathan during a test dive is $d(t) = 3t^4 - 16t^3 + 24t^2$ meters. The depth function changes concavity at $t =$**

**(A)** $\dfrac{2}{3}$ only | **(B)** $1$ only | **(C)** $\dfrac{2}{3}$ and $2$ | **(D)** $2$ only

**Answer: (C) $\dfrac{2}{3}$ and $2$**

**Solution:**

Find the second derivative and set it equal to zero:

$$d'(t) = 12t^3 - 48t^2 + 48t$$

$$d''(t) = 36t^2 - 96t + 48 = 12(3t^2 - 8t + 4)$$

Factor the quadratic:

$$3t^2 - 8t + 4 = (3t - 2)(t - 2) = 0$$

$$t = \frac{2}{3} \quad \text{or} \quad t = 2$$

Verify sign changes in $d''(t)$:

- For $t < \dfrac{2}{3}$: $d''(0) = 48 > 0$ (concave up)
- For $\dfrac{2}{3} < t < 2$: $d''(1) = 36 - 96 + 48 = -12 < 0$ (concave down)
- For $t > 2$: $d''(3) = 324 - 288 + 48 = 84 > 0$ (concave up)

The sign of $d''(t)$ changes at both $t = \dfrac{2}{3}$ and $t = 2$, confirming both are inflection points.

**Common mistake:** Only finding one root of the quadratic, or not verifying that $d''(t)$ actually changes sign (a zero of $d''$ is only an inflection point if the sign changes).

</details>

<details>
<summary><strong>Question 12</strong></summary>

**Leviathan's onboard processor computes accumulated pressure data using $G(x) = \displaystyle \int_1^{\sin x} \frac{dt}{\sqrt{t^2 + 1}}$. Then $G'(x) =$**

**(A)** $\dfrac{1}{\sqrt{\sin^2 x + 1}}$ | **(B)** $\dfrac{\cos x}{\sqrt{\sin^2 x + 1}}$ | **(C)** $\dfrac{\cos x}{\sin^2 x + 1}$ | **(D)** $\dfrac{\sin x}{\sqrt{\sin^2 x + 1}}$

**Answer: (B) $\dfrac{\cos x}{\sqrt{\sin^2 x + 1}}$**

**Solution:**

Apply the Fundamental Theorem of Calculus (Part 1) combined with the chain rule. If $G(x) = \displaystyle \int_a^{u(x)} f(t)\,dt$, then $G'(x) = f(u(x)) \cdot u'(x)$.

Here $f(t) = \dfrac{1}{\sqrt{t^2 + 1}}$ and $u(x) = \sin x$, so $u'(x) = \cos x$.

$$G'(x) = \frac{1}{\sqrt{(\sin x)^2 + 1}} \cdot \cos x = \frac{\cos x}{\sqrt{\sin^2 x + 1}}$$

**Common mistake:** Forgetting to multiply by the chain rule factor $\cos x$ (choosing A), or forgetting the square root in the denominator (choosing C).

</details>

<details>
<summary><strong>Question 13</strong></summary>

**A marine biologist models the growth rate of tube worms near a vent with the differential equation $\dfrac{dL}{dt} = t - L$. In the slope field for this equation, the slopes are zero along the line**

**(A)** $L = t$ | **(B)** $L = 0$ | **(C)** $t = 0$ | **(D)** $L = -t$

**Answer: (A) $L = t$**

**Solution:**

The slopes in the slope field are zero when $\dfrac{dL}{dt} = 0$:

$$t - L = 0 \implies L = t$$

This means that at every point along the line $L = t$ (a diagonal line through the origin with slope $1$), the slope field has horizontal line segments.

**Common mistake:** Setting $L = 0$ instead of $\dfrac{dL}{dt} = 0$. Answer (B) gives the line where $L$ is zero, not where the slope is zero. Always set the right-hand side of the DE equal to zero to find the nullcline.

</details>

<details>
<summary><strong>Question 14</strong></summary>

**The Maclaurin series for the pressure correction function $\dfrac{1}{1 + x^2}$ is**

**(A)** $\displaystyle \sum_{n=0}^{\infty} x^{2n}$ | **(B)** $\displaystyle \sum_{n=0}^{\infty} (-1)^n x^n$ | **(C)** $\displaystyle \sum_{n=0}^{\infty} \dfrac{(-1)^n x^{2n}}{(2n)!}$ | **(D)** $\displaystyle \sum_{n=0}^{\infty} (-1)^n x^{2n}$

**Answer: (D) $\displaystyle \sum_{n=0}^{\infty} (-1)^n x^{2n}$**

**Solution:**

Start with the geometric series $\dfrac{1}{1 - r} = \displaystyle \sum_{n=0}^{\infty} r^n$ for $|r| < 1$.

Substitute $r = -x^2$:

$$\frac{1}{1 + x^2} = \frac{1}{1 - (-x^2)} = \sum_{n=0}^{\infty} (-x^2)^n = \sum_{n=0}^{\infty} (-1)^n x^{2n}$$

This is valid for $|x^2| < 1$, i.e., $|x| < 1$.

Expanded: $1 - x^2 + x^4 - x^6 + \cdots$

**Common mistake:** Choosing (A), which omits the alternating sign, giving $\dfrac{1}{1-x^2}$ instead. Or choosing (C), which is the Maclaurin series for $\cos x$, not $\dfrac{1}{1+x^2}$.

</details>

<details>
<summary><strong>Question 15</strong></summary>

**The flow rate through a filtration valve is $Q(x) = \dfrac{5x - 1}{x^2 - x}$. Using partial fractions, $\displaystyle \int \frac{5x - 1}{x^2 - x}\,dx =$**

**(A)** $5\ln|x^2 - x| + C$ | **(B)** $\ln|x| + 4\ln|x - 1| + C$ | **(C)** $4\ln|x| + \ln|x - 1| + C$ | **(D)** $\ln|x| - 4\ln|x - 1| + C$

**Answer: (B) $\ln|x| + 4\ln|x - 1| + C$**

**Solution:**

Factor the denominator: $x^2 - x = x(x - 1)$.

Set up the partial fraction decomposition:

$$\frac{5x - 1}{x(x - 1)} = \frac{A}{x} + \frac{B}{x - 1}$$

Multiply both sides by $x(x - 1)$:

$$5x - 1 = A(x - 1) + Bx$$

**Find $A$:** Set $x = 0$:

$$-1 = A(-1) \implies A = 1$$

**Find $B$:** Set $x = 1$:

$$4 = B(1) \implies B = 4$$

Therefore:

$$\int \frac{5x - 1}{x(x - 1)}\,dx = \int \left(\frac{1}{x} + \frac{4}{x - 1}\right)dx = \ln|x| + 4\ln|x - 1| + C$$

**Common mistake:** Swapping the values of $A$ and $B$ (choosing C), or using $\dfrac{d}{dx}[x^2 - x] = 2x - 1$ to attempt a direct $u$-substitution (choosing A), which is invalid since $5x - 1 \ne k(2x - 1)$.

</details>

<details>
<summary><strong>Question 16</strong></summary>

**The series $\displaystyle \sum_{n=1}^{\infty} \frac{(-1)^n \sqrt{n}}{n + 1}$ converges. The convergence can be established by**

**(A)** the geometric series test | **(B)** the $p$-series test with $p > 1$ | **(C)** the alternating series test | **(D)** the ratio test

**Answer: (C) the alternating series test**

**Solution:**

This is an alternating series of the form $\displaystyle \sum_{n=1}^{\infty} (-1)^n b_n$ where $b_n = \dfrac{\sqrt{n}}{n + 1}$.

The alternating series test requires two conditions:

**Condition 1:** $b_n > 0$ for all $n \ge 1$. Since $\sqrt{n} > 0$ and $n + 1 > 0$, we have $b_n > 0$. $\checkmark$

**Condition 2:** $b_n$ is eventually decreasing. For large $n$:

$$b_n = \frac{\sqrt{n}}{n + 1} = \frac{n^{1/2}}{n + 1} \approx \frac{1}{n^{1/2}}$$

To confirm $b_n$ is decreasing, consider $f(x) = \dfrac{\sqrt{x}}{x + 1}$. Then:

$$f'(x) = \frac{\dfrac{1}{2\sqrt{x}}(x + 1) - \sqrt{x}}{(x + 1)^2} = \frac{\dfrac{x + 1 - 2x}{2\sqrt{x}}}{(x + 1)^2} = \frac{1 - x}{2\sqrt{x}(x + 1)^2}$$

For $x > 1$, $f'(x) < 0$, so $b_n$ is decreasing for $n \ge 2$. $\checkmark$

**Condition 3:** $\displaystyle \lim_{n \to \infty} b_n = \lim_{n \to \infty} \frac{\sqrt{n}}{n + 1} = \lim_{n \to \infty} \frac{1/\sqrt{n}}{1 + 1/n} = \frac{0}{1} = 0$. $\checkmark$

All conditions of the alternating series test are met, so the series converges.

**Why not the other tests?**
- **(A)** Not geometric — there is no common ratio between successive terms.
- **(B)** The $p$-series test applies to $\sum \dfrac{1}{n^p}$, not to alternating series with this structure. Also, the absolute series $\sum \dfrac{\sqrt{n}}{n+1} \approx \sum \dfrac{1}{\sqrt{n}}$ diverges ($p = \dfrac{1}{2} < 1$).
- **(D)** The ratio test gives $L = 1$ (inconclusive) for this series.

**Common mistake:** Choosing (B) by reasoning that $\dfrac{\sqrt{n}}{n+1} \approx \dfrac{1}{\sqrt{n}}$ behaves like a $p$-series. While that comparison is useful, it actually shows the absolute series *diverges* ($p = \dfrac{1}{2} < 1$), so the $p$-series test cannot establish convergence here.

</details>

<details>
<summary><strong>Question 17</strong></summary>

**A navigation engineer verifies the sonar calibration integral $\displaystyle \int \frac{dx}{x^2 + 16} =$**

**(A)** $\dfrac{1}{4}\arctan\!\left(\dfrac{x}{4}\right) + C$ | **(B)** $\arctan\!\left(\dfrac{x}{4}\right) + C$ | **(C)** $\dfrac{1}{4}\arcsin\!\left(\dfrac{x}{4}\right) + C$ | **(D)** $\arcsin\!\left(\dfrac{x}{4}\right) + C$

**Answer: (A) $\dfrac{1}{4}\arctan\!\left(\dfrac{x}{4}\right) + C$**

**Solution:**

Use the standard integral formula $\displaystyle \int \frac{dx}{x^2 + a^2} = \frac{1}{a}\arctan\!\left(\frac{x}{a}\right) + C$.

Here $a^2 = 16$, so $a = 4$:

$$\int \frac{dx}{x^2 + 16} = \frac{1}{4}\arctan\!\left(\frac{x}{4}\right) + C$$

**Verification:** Differentiate $\dfrac{1}{4}\arctan\!\left(\dfrac{x}{4}\right)$:

$$\frac{d}{dx}\left[\frac{1}{4}\arctan\!\left(\frac{x}{4}\right)\right] = \frac{1}{4} \cdot \frac{1}{1 + (x/4)^2} \cdot \frac{1}{4} = \frac{1}{16} \cdot \frac{1}{1 + x^2/16} = \frac{1}{16 + x^2} \checkmark$$

**Common mistake:** Forgetting the $\dfrac{1}{a}$ factor out front and choosing (B), which is missing the $\dfrac{1}{4}$ multiplier. Or confusing $\arctan$ with $\arcsin$ (choices C and D), which arises from the integral $\displaystyle \int \dfrac{dx}{\sqrt{a^2 - x^2}}$ — a different form entirely.

</details>

<details>
<summary><strong>Question 18</strong></summary>

**During a calibration run, Leviathan moves along a linear track with velocity $v(t) = t^2 - 4t + 3$ m/s. The total distance traveled from $t = 0$ to $t = 4$ is**

**(A)** $\displaystyle \int_0^4 (t^2 - 4t + 3)\,dt$ | **(B)** $\displaystyle \int_0^4 |t^2 - 4t + 3|\,dt$ | **(C)** $\left|\displaystyle \int_0^4 (t^2 - 4t + 3)\,dt\right|$ | **(D)** $\displaystyle \int_0^4 (t^2 - 4t + 3)^2\,dt$

**Answer: (B) $\displaystyle \int_0^4 |t^2 - 4t + 3|\,dt$**

**Solution:**

The key distinction is between **displacement** and **total distance traveled**.

- **Displacement** $= \displaystyle \int_0^4 v(t)\,dt$ (the signed integral — this is choice A).
- **Total distance** $= \displaystyle \int_0^4 |v(t)|\,dt$ (the integral of the absolute value of velocity).

Total distance requires the absolute value because when $v(t) < 0$, the object moves backward, but that backward motion still contributes positive distance.

Note that $v(t) = t^2 - 4t + 3 = (t-1)(t-3)$, which is negative on the interval $(1, 3)$. Since the velocity changes sign, the displacement and total distance are different, and we must use the absolute value.

**Common mistake:** Choosing (A), which gives displacement (net change in position), not total distance. Or choosing (C), which takes the absolute value of the entire integral — this just gives $|\text{displacement}|$, which still doesn't account for the back-and-forth motion.

</details>

<details>
<summary><strong>Question 19</strong></summary>

**The interval of convergence of the power series $\displaystyle \sum_{n=1}^{\infty} \frac{(-1)^n (x + 2)^n}{n^2 \cdot 3^n}$ is**

**(A)** $(-5, 1)$ | **(B)** $[-5, 1)$ | **(C)** $(-5, 1]$ | **(D)** $[-5, 1]$

**Answer: (D) $[-5, 1]$**

**Solution:**

**Step 1: Find the radius of convergence** using the ratio test.

Let $a_n = \dfrac{(-1)^n (x+2)^n}{n^2 \cdot 3^n}$. Compute:

$$\left|\frac{a_{n+1}}{a_n}\right| = \left|\frac{(x+2)^{n+1}}{(n+1)^2 \cdot 3^{n+1}} \cdot \frac{n^2 \cdot 3^n}{(x+2)^n}\right| = \frac{|x+2|}{3} \cdot \frac{n^2}{(n+1)^2}$$

$$\lim_{n \to \infty} \left|\frac{a_{n+1}}{a_n}\right| = \frac{|x+2|}{3} \cdot 1 = \frac{|x+2|}{3}$$

The series converges when $\dfrac{|x+2|}{3} < 1$, i.e., $|x + 2| < 3$, giving $-5 < x < 1$. The radius of convergence is $R = 3$, centered at $x = -2$.

**Step 2: Test the endpoints.**

**At $x = -5$:** $\displaystyle \sum_{n=1}^{\infty} \frac{(-1)^n(-3)^n}{n^2 \cdot 3^n} = \sum_{n=1}^{\infty} \frac{(-1)^n \cdot (-1)^n \cdot 3^n}{n^2 \cdot 3^n} = \sum_{n=1}^{\infty} \frac{(-1)^{2n}}{n^2} = \sum_{n=1}^{\infty} \frac{1}{n^2}$

This is a $p$-series with $p = 2 > 1$, which **converges**.

**At $x = 1$:** $\displaystyle \sum_{n=1}^{\infty} \frac{(-1)^n \cdot 3^n}{n^2 \cdot 3^n} = \sum_{n=1}^{\infty} \frac{(-1)^n}{n^2}$

This is an alternating series with $b_n = \dfrac{1}{n^2} \to 0$ and $b_n$ decreasing, so it **converges** by the alternating series test. (In fact, it converges absolutely since $\sum \dfrac{1}{n^2}$ converges.)

Both endpoints converge, so the interval of convergence is $[-5, 1]$.

**Common mistake:** Forgetting to test the endpoints and choosing (A), or making a sign error when substituting $x = -5$ and concluding that endpoint diverges.

</details>

<details>
<summary><strong>Question 20</strong></summary>

**Integration by parts gives $\displaystyle \int x^2 \cos x\,dx =$**

**(A)** $x^2 \sin x + 2x\cos x + 2\sin x + C$ | **(B)** $x^2 \sin x - 2x\cos x + 2\sin x + C$ | **(C)** $x^2 \sin x + 2x\cos x - 2\sin x + C$ | **(D)** $x^2 \sin x + 2\cos x + C$

**Answer: (C) $x^2 \sin x + 2x\cos x - 2\sin x + C$**

**Solution:**

Apply integration by parts twice using the tabular method.

**First application:** Let $u = x^2$, $dv = \cos x\,dx$:

$$\int x^2 \cos x\,dx = x^2 \sin x - \int 2x \sin x\,dx$$

**Second application:** Let $u = 2x$, $dv = \sin x\,dx$:

$$\int 2x \sin x\,dx = 2x(-\cos x) - \int 2(-\cos x)\,dx = -2x\cos x + 2\int \cos x\,dx = -2x\cos x + 2\sin x$$

**Combine:**

$$\int x^2 \cos x\,dx = x^2 \sin x - (-2x\cos x + 2\sin x) + C$$

$$= x^2 \sin x + 2x\cos x - 2\sin x + C$$

**Verification by differentiation:**

$$\frac{d}{dx}\left[x^2 \sin x + 2x\cos x - 2\sin x\right]$$
$$= 2x\sin x + x^2\cos x + 2\cos x - 2x\sin x - 2\cos x$$
$$= x^2 \cos x \checkmark$$

**Common mistake:** Making a sign error in the second integration by parts. When integrating $\int 2x \sin x\,dx$, the antiderivative of $\sin x$ is $-\cos x$, and the subtraction of the next integral creates a double negative that is easy to mishandle (leading to choice A or B).

</details>

<details>
<summary><strong>Question 21</strong></summary>

**The concentration of dissolved minerals near a vent satisfies $\dfrac{dC}{dt} = 3C$ with $C(0) = 20$ mg/L. The concentration at time $t$ is**

**(A)** $20e^{3t}$ | **(B)** $20 + 3t$ | **(C)** $60t$ | **(D)** $\dfrac{20}{1 - 3t}$

**Answer: (A) $20e^{3t}$**

**Solution:**

This is a first-order linear ODE with constant coefficients. Separate variables:

$$\frac{dC}{C} = 3\,dt$$

Integrate both sides:

$$\int \frac{dC}{C} = \int 3\,dt$$

$$\ln|C| = 3t + K$$

$$C = e^{3t + K} = e^K \cdot e^{3t} = A e^{3t}$$

Apply the initial condition $C(0) = 20$:

$$20 = A \cdot e^0 = A$$

Therefore:

$$C(t) = 20e^{3t}$$

This is the standard exponential growth model: when $\dfrac{dC}{dt} = kC$, the solution is $C(t) = C(0)e^{kt}$.

**Common mistake:** Choosing (B) by treating $\dfrac{dC}{dt} = 3C$ as if it were $\dfrac{dC}{dt} = 3$, which would give a linear function. Or choosing (D), which solves a different DE: $\dfrac{dC}{dt} = 3C^2$.

</details>

<details>
<summary><strong>Question 22</strong></summary>

**To calibrate Leviathan's depth sensor, an engineer computes $\displaystyle \lim_{x \to 0} \frac{1 - \cos 2x}{x \sin x}$ using Taylor series. This limit equals**

**(A)** $0$ | **(B)** $1$ | **(C)** $4$ | **(D)** $2$

**Answer: (D) $2$**

**Solution:**

Expand each function using Maclaurin series, keeping the lowest-order terms:

$$\cos 2x = 1 - \frac{(2x)^2}{2!} + \frac{(2x)^4}{4!} - \cdots = 1 - 2x^2 + \frac{2x^4}{3} - \cdots$$

$$1 - \cos 2x = 2x^2 - \frac{2x^4}{3} + \cdots$$

$$\sin x = x - \frac{x^3}{6} + \cdots$$

$$x \sin x = x\!\left(x - \frac{x^3}{6} + \cdots\right) = x^2 - \frac{x^4}{6} + \cdots$$

Now compute the limit:

$$\lim_{x \to 0} \frac{1 - \cos 2x}{x \sin x} = \lim_{x \to 0} \frac{2x^2 - \frac{2x^4}{3} + \cdots}{x^2 - \frac{x^4}{6} + \cdots} = \lim_{x \to 0} \frac{2x^2(1 - \cdots)}{x^2(1 - \cdots)} = \frac{2}{1} = 2$$

**Alternative (L'Hôpital's Rule):** The form is $\dfrac{0}{0}$. Applying L'Hôpital's:

$$\lim_{x \to 0} \frac{2\sin 2x}{\sin x + x\cos x}$$

Still $\dfrac{0}{0}$. Apply again:

$$\lim_{x \to 0} \frac{4\cos 2x}{2\cos x - x\sin x} = \frac{4 \cdot 1}{2 \cdot 1 - 0} = \frac{4}{2} = 2$$

**Common mistake:** Using the identity $1 - \cos 2x = 2\sin^2 x$ but then misapplying $\lim \dfrac{\sin x}{x} = 1$ without properly accounting for the $x \sin x$ denominator, leading to an incorrect answer of $1$ or $4$.

</details>

<details>
<summary><strong>Question 23</strong></summary>

**Leviathan hovers at a fixed depth of $60$ meters. A research vessel on the surface drifts horizontally at a constant $2$ m/s, moving directly away from the point above Leviathan. When the horizontal distance between the vessel and Leviathan is $80$ meters, the rate at which the cable length between them is increasing is**

**(A)** $\dfrac{6}{5}$ | **(B)** $\dfrac{8}{5}$ | **(C)** $2$ | **(D)** $\dfrac{12}{5}$

**Answer: (B) $\dfrac{8}{5}$**

**Solution:**

Set up the geometry. Leviathan is at a fixed depth of $60$ m directly below the starting position. The vessel moves horizontally on the surface. Let:
- $x$ = horizontal distance from the point above Leviathan to the vessel
- $L$ = cable length (the hypotenuse)

By the Pythagorean theorem:

$$L^2 = x^2 + 60^2 = x^2 + 3600$$

Differentiate both sides with respect to time $t$:

$$2L\frac{dL}{dt} = 2x\frac{dx}{dt}$$

$$\frac{dL}{dt} = \frac{x}{L} \cdot \frac{dx}{dt}$$

When $x = 80$:

$$L = \sqrt{80^2 + 60^2} = \sqrt{6400 + 3600} = \sqrt{10000} = 100$$

Given $\dfrac{dx}{dt} = 2$ m/s:

$$\frac{dL}{dt} = \frac{80}{100} \cdot 2 = \frac{4}{5} \cdot 2 = \frac{8}{5} \text{ m/s}$$

**Common mistake:** Using $L = \sqrt{80^2 - 60^2}$ (subtracting instead of adding), or forgetting to find $L$ and dividing by $x$ instead, or confusing the vertical depth with the horizontal distance in the setup.

</details>

<details>
<summary><strong>Question 24</strong></summary>

**Leviathan's cylindrical sample collection tank has a radius that varies with height as $r(h) = \sqrt{h}$ meters. The tank fills with water at a rate of $2$ m$^3$/min. When the water height is $h = 4$ meters, the rate at which the water level is rising is $\dfrac{dh}{dt} =$**

**(A)** $\dfrac{1}{\pi}$ | **(B)** $\dfrac{1}{4\pi}$ | **(C)** $\dfrac{1}{2\pi}$ | **(D)** $\dfrac{2}{\pi}$

**Answer: (C) $\dfrac{1}{2\pi}$**

**Solution:**

Since the radius varies with height as $r(h) = \sqrt{h}$, this is a solid of revolution. The volume of water at height $h$ is found by integrating the cross-sectional area:

$$V = \int_0^h \pi [r(s)]^2\,ds = \int_0^h \pi s\,ds = \pi \cdot \frac{s^2}{2}\bigg|_0^h = \frac{\pi h^2}{2}$$

Differentiate with respect to $t$:

$$\frac{dV}{dt} = \pi h \cdot \frac{dh}{dt}$$

Given $\dfrac{dV}{dt} = 2$ and $h = 4$:

$$2 = \pi(4) \cdot \frac{dh}{dt}$$

$$\frac{dh}{dt} = \frac{2}{4\pi} = \frac{1}{2\pi}$$

**Common mistake:** Using the formula $V = \pi r^2 h$ for a standard cylinder (constant radius) and substituting $r = \sqrt{4} = 2$ to get $V = 4\pi h$, which gives $\dfrac{dh}{dt} = \dfrac{1}{2\pi}$ by coincidence — but for the wrong reasons. More dangerously, some students use $V = \pi r^2 h = \pi h \cdot h = \pi h^2$ (missing the $\dfrac{1}{2}$) and get an incorrect answer.

</details>

<details>
<summary><strong>Question 25</strong></summary>

**$\displaystyle \int_1^{e^2} \frac{\ln x}{x}\,dx =$**

**(A)** $2$ | **(B)** $\dfrac{1}{2}$ | **(C)** $4$ | **(D)** $1$

**Answer: (A) $2$**

**Solution:**

Use $u$-substitution. Let $u = \ln x$, so $du = \dfrac{1}{x}\,dx$.

Change the limits:
- When $x = 1$: $u = \ln 1 = 0$
- When $x = e^2$: $u = \ln(e^2) = 2$

The integral becomes:

$$\int_0^2 u\,du = \frac{u^2}{2}\bigg|_0^2 = \frac{4}{2} - 0 = 2$$

**Common mistake:** Forgetting to change the limits of integration and leaving them as $1$ to $e^2$, or miscalculating $\ln(e^2) = 2e$ instead of $2$.

</details>

<details>
<summary><strong>Question 26</strong></summary>

**Leviathan's path through a narrow canyon is described parametrically by $x(t) = t^2 + 1$ and $y(t) = t^3 - 3t$. The slope $\dfrac{dy}{dx}$ at $t = 1$ is**

**(A)** $3$ | **(B)** $1$ | **(C)** $-1$ | **(D)** $0$

**Answer: (D) $0$**

**Solution:**

For parametric equations, the slope is:

$$\frac{dy}{dx} = \frac{dy/dt}{dx/dt}$$

Compute each derivative:

$$\frac{dx}{dt} = 2t$$

$$\frac{dy}{dt} = 3t^2 - 3$$

At $t = 1$:

$$\frac{dx}{dt}\bigg|_{t=1} = 2(1) = 2$$

$$\frac{dy}{dt}\bigg|_{t=1} = 3(1)^2 - 3 = 3 - 3 = 0$$

Therefore:

$$\frac{dy}{dx}\bigg|_{t=1} = \frac{0}{2} = 0$$

The tangent line is horizontal at $t = 1$.

**Common mistake:** Computing $\dfrac{dx}{dy}$ instead of $\dfrac{dy}{dx}$ (getting $\dfrac{2}{0}$, which is undefined), or evaluating the derivatives at the point $(x, y) = (2, -2)$ rather than at $t = 1$.

</details>

<details>
<summary><strong>Question 27</strong></summary>

**The second-degree Taylor polynomial for $\sqrt{1 + x}$ centered at $x = 0$, used to approximate pressure corrections, is**

**(A)** $1 + x - \dfrac{x^2}{2}$ | **(B)** $1 + \dfrac{x}{2} - \dfrac{x^2}{8}$ | **(C)** $1 + \dfrac{x}{2} + \dfrac{x^2}{4}$ | **(D)** $1 - \dfrac{x}{2} + \dfrac{x^2}{8}$

**Answer: (B) $1 + \dfrac{x}{2} - \dfrac{x^2}{8}$**

**Solution:**

Let $f(x) = (1 + x)^{1/2}$. Compute the derivatives at $x = 0$:

$$f(x) = (1 + x)^{1/2} \implies f(0) = 1$$

$$f'(x) = \frac{1}{2}(1 + x)^{-1/2} \implies f'(0) = \frac{1}{2}$$

$$f''(x) = \frac{1}{2} \cdot \left(-\frac{1}{2}\right)(1 + x)^{-3/2} = -\frac{1}{4}(1 + x)^{-3/2} \implies f''(0) = -\frac{1}{4}$$

The second-degree Taylor polynomial is:

$$P_2(x) = f(0) + f'(0)x + \frac{f''(0)}{2!}x^2 = 1 + \frac{1}{2}x + \frac{-1/4}{2}x^2 = 1 + \frac{x}{2} - \frac{x^2}{8}$$

This can also be obtained from the binomial series $(1 + x)^{1/2} = 1 + \dfrac{1}{2}x + \dfrac{\frac{1}{2}\left(\frac{1}{2} - 1\right)}{2!}x^2 + \cdots = 1 + \dfrac{x}{2} - \dfrac{x^2}{8} + \cdots$

**Common mistake:** Forgetting to divide $f''(0)$ by $2!$ in the Taylor formula, giving $-\dfrac{1}{4}x^2$ instead of $-\dfrac{1}{8}x^2$ (choosing A). Or getting the sign of the second derivative wrong and choosing (C) or (D).

</details>

<details>
<summary><strong>Question 28</strong></summary>

**An engineer evaluates the convergence of $\displaystyle \int_0^{1} \frac{dx}{\sqrt{x}}$. This integral**

**(A)** diverges | **(B)** converges to $\dfrac{1}{2}$ | **(C)** converges to $2$ | **(D)** converges to $1$

**Answer: (C) converges to $2$**

**Solution:**

This is an improper integral because $\dfrac{1}{\sqrt{x}}$ is undefined at $x = 0$. Write it as a limit:

$$\int_0^1 \frac{dx}{\sqrt{x}} = \lim_{a \to 0^+} \int_a^1 x^{-1/2}\,dx$$

Find the antiderivative:

$$\int x^{-1/2}\,dx = \frac{x^{1/2}}{1/2} = 2\sqrt{x}$$

Evaluate:

$$\lim_{a \to 0^+} \left[2\sqrt{x}\right]_a^1 = \lim_{a \to 0^+} \left(2\sqrt{1} - 2\sqrt{a}\right) = 2 - 0 = 2$$

The integral converges to $2$.

**Common mistake:** Assuming that any integral with a discontinuity at the endpoint must diverge (choosing A), or applying the power rule incorrectly by writing $\int x^{-1/2}\,dx = \dfrac{x^{1/2}}{-1/2}$ with the wrong sign in the denominator.

</details>

<details>
<summary><strong>Question 29</strong></summary>

**Which of the following series diverges?**

**(A)** $\displaystyle \sum_{n=1}^{\infty} \frac{1}{n}$ | **(B)** $\displaystyle \sum_{n=1}^{\infty} \frac{1}{n^2}$ | **(C)** $\displaystyle \sum_{n=1}^{\infty} \frac{1}{2^n}$ | **(D)** $\displaystyle \sum_{n=1}^{\infty} \frac{(-1)^n}{n}$

**Answer: (A) $\displaystyle \sum_{n=1}^{\infty} \frac{1}{n}$**

**Solution:**

Analyze each series:

**(A)** $\displaystyle \sum_{n=1}^{\infty} \frac{1}{n}$ — This is the **harmonic series**, a $p$-series with $p = 1$. Since $p \le 1$, it **diverges**. This is a fundamental result in calculus.

**(B)** $\displaystyle \sum_{n=1}^{\infty} \frac{1}{n^2}$ — This is a $p$-series with $p = 2 > 1$, so it **converges** (to $\dfrac{\pi^2}{6}$).

**(C)** $\displaystyle \sum_{n=1}^{\infty} \frac{1}{2^n}$ — This is a geometric series with ratio $r = \dfrac{1}{2}$. Since $|r| < 1$, it **converges** (to $1$).

**(D)** $\displaystyle \sum_{n=1}^{\infty} \frac{(-1)^n}{n}$ — This is the **alternating harmonic series**. By the alternating series test ($b_n = \dfrac{1}{n} \to 0$ and $b_n$ is decreasing), it **converges** (to $-\ln 2$).

Only (A) diverges.

**Common mistake:** Confusing the harmonic series $\sum \dfrac{1}{n}$ with the alternating harmonic series $\sum \dfrac{(-1)^n}{n}$. The alternating version converges (D), but the non-alternating version diverges (A). Students sometimes think $\dfrac{1}{n} \to 0$ implies the series converges — but the divergence test only works one way (terms not going to zero $\implies$ divergence; terms going to zero does NOT guarantee convergence).

</details>

<details>
<summary><strong>Question 30</strong></summary>

**Leviathan's test vehicle moves along a path given by $\vec{r}(t) = \langle \sin 2t, \; \cos 3t \rangle$. The acceleration vector $\vec{a}(t)$ is**

**(A)** $\langle 2\cos 2t, \; -3\sin 3t \rangle$ | **(B)** $\langle -4\sin 2t, \; -9\cos 3t \rangle$ | **(C)** $\langle -2\sin 2t, \; -3\cos 3t \rangle$ | **(D)** $\langle 4\cos 2t, \; 9\sin 3t \rangle$

**Answer: (B) $\langle -4\sin 2t, \; -9\cos 3t \rangle$**

**Solution:**

The acceleration vector is the second derivative of the position vector.

**Step 1:** Find the velocity vector $\vec{v}(t) = \vec{r}\,'(t)$:

$$\vec{v}(t) = \left\langle \frac{d}{dt}[\sin 2t], \; \frac{d}{dt}[\cos 3t] \right\rangle = \langle 2\cos 2t, \; -3\sin 3t \rangle$$

**Step 2:** Find the acceleration vector $\vec{a}(t) = \vec{v}\,'(t)$:

$$\vec{a}(t) = \left\langle \frac{d}{dt}[2\cos 2t], \; \frac{d}{dt}[-3\sin 3t] \right\rangle$$

$$= \langle 2 \cdot (-\sin 2t) \cdot 2, \; -3 \cdot (\cos 3t) \cdot 3 \rangle$$

$$= \langle -4\sin 2t, \; -9\cos 3t \rangle$$

**Common mistake:** Stopping after one derivative and choosing (A), which is the velocity vector, not the acceleration vector. Or forgetting the chain rule on the second differentiation and choosing (C), where the coefficients $2$ and $3$ aren't squared.

</details>

### Part B — Calculator Allowed

<details>
<summary><strong>Question 31</strong></summary>

**The water temperature surrounding Leviathan during descent is modeled by $T(d) = 2 + 20e^{-0.001d}$ degrees Celsius, where $d$ is depth in meters. The average temperature from $d = 0$ to $d = 4000$ meters is closest to**

**(A)** $4.218$ | **(B)** $5.346$ | **(C)** $6.103$ | **(D)** $6.908$

**Answer: (D) $6.908$**

**Solution:**

The average value of a function on $[a, b]$ is $\dfrac{1}{b - a}\displaystyle\int_a^b f(x)\,dx$. Here:

$$T_{\text{avg}} = \frac{1}{4000}\int_0^{4000}\left(2 + 20e^{-0.001d}\right)d\!d$$

Find the antiderivative:

$$\int \left(2 + 20e^{-0.001d}\right)d\!d = 2d + 20 \cdot \frac{e^{-0.001d}}{-0.001} = 2d - 20000\,e^{-0.001d}$$

Evaluate from $0$ to $4000$:

$$\left[2d - 20000\,e^{-0.001d}\right]_0^{4000} = \left(8000 - 20000\,e^{-4}\right) - \left(0 - 20000\right)$$

$$= 8000 - 20000\,e^{-4} + 20000 = 28000 - 20000\,e^{-4}$$

Using a calculator: $e^{-4} \approx 0.01832$, so:

$$28000 - 20000(0.01832) = 28000 - 366.31 = 27633.69$$

Divide by $4000$:

$$T_{\text{avg}} = \frac{27633.69}{4000} \approx 6.908$$

**Common mistake:** Forgetting to divide by the interval length $(b - a) = 4000$, which gives the total integral ($\approx 27634$) instead of the average. Or using $+20000\,e^{-0.001d}$ instead of $-20000\,e^{-0.001d}$ as the antiderivative of the exponential term.

</details>

<details>
<summary><strong>Question 32</strong></summary>

**The hull of Leviathan is modeled by revolving the curve $y = 3e^{-x^2/8}$ about the $x$-axis for $-3 \le x \le 3$. The volume of the resulting solid is closest to**

**(A)** $78.54$ cubic units | **(B)** $88.37$ cubic units | **(C)** $96.83$ cubic units | **(D)** $113.10$ cubic units

**Answer: (C) $96.83$ cubic units**

**Solution:**

Using the disk method, the volume of a solid of revolution about the $x$-axis is:

$$V = \pi \int_{-3}^{3} [y(x)]^2\,dx = \pi \int_{-3}^{3} \left[3e^{-x^2/8}\right]^2 dx$$

$$= \pi \int_{-3}^{3} 9\,e^{-x^2/4}\,dx = 9\pi \int_{-3}^{3} e^{-x^2/4}\,dx$$

Since $e^{-x^2/4}$ is an even function, we can write:

$$V = 9\pi \cdot 2\int_0^3 e^{-x^2/4}\,dx = 18\pi \int_0^3 e^{-x^2/4}\,dx$$

This integral involves the Gaussian function and cannot be evaluated with elementary antiderivatives. Using a calculator:

$$\int_0^3 e^{-x^2/4}\,dx \approx 1.7136$$

Therefore:

$$V = 18\pi(1.7136) \approx 18(3.14159)(1.7136) \approx 96.83 \text{ cubic units}$$

**Common mistake:** Forgetting to square the function before integrating (computing $\pi \int 3e^{-x^2/8}\,dx$ instead of $\pi \int 9e^{-x^2/4}\,dx$), or using the shell method formula when the disk method is appropriate for revolution about the $x$-axis.

</details>

<details>
<summary><strong>Question 33</strong></summary>

**The rate of mineral deposition from a hydrothermal vent is modeled by $R(t) = 45 e^{-0.12t}$ grams per hour. The total mass deposited from $t = 0$ to $t = 24$ hours is closest to**

**(A)** $291.8$ g | **(B)** $354.0$ g | **(C)** $375.0$ g | **(D)** $412.5$ g

**Answer: (B) $354.0$ g**

**Solution:**

The total mass is the integral of the rate function:

$$M = \int_0^{24} 45\,e^{-0.12t}\,dt$$

Find the antiderivative:

$$\int 45\,e^{-0.12t}\,dt = 45 \cdot \frac{e^{-0.12t}}{-0.12} = -375\,e^{-0.12t}$$

Evaluate from $0$ to $24$:

$$M = \left[-375\,e^{-0.12t}\right]_0^{24} = -375\,e^{-2.88} - (-375\,e^{0})$$

$$= -375\,e^{-2.88} + 375 = 375\left(1 - e^{-2.88}\right)$$

Using a calculator: $e^{-2.88} \approx 0.05613$, so:

$$M = 375(1 - 0.05613) = 375(0.9439) \approx 354.0 \text{ g}$$

**Common mistake:** Computing $\dfrac{45}{-0.12}$ incorrectly (getting $-360$ instead of $-375$), or evaluating the antiderivative at only one endpoint instead of computing the definite integral as a difference.

</details>

<details>
<summary><strong>Question 34</strong></summary>

**The temperature of Leviathan's external hull sensor satisfies $\dfrac{dT}{dt} = -0.2T + 10$ with $T(0) = 80$ degrees Celsius, where $t$ is in minutes. Using Euler's method with step size $\Delta t = 2$ minutes, $T(8) \approx$**

**(A)** $53.89$ | **(B)** $56.48$ | **(C)** $60.80$ | **(D)** $68.00$

**Answer: (A) $53.89$**

**Solution:**

Euler's method: $T_{n+1} = T_n + \Delta t \cdot f(t_n, T_n)$ where $f(t, T) = -0.2T + 10$ and $\Delta t = 2$.

**Step 1:** $t_0 = 0$, $T_0 = 80$

$$f(0, 80) = -0.2(80) + 10 = -16 + 10 = -6$$

$$T_1 = 80 + 2(-6) = 80 - 12 = 68$$

**Step 2:** $t_1 = 2$, $T_1 = 68$

$$f(2, 68) = -0.2(68) + 10 = -13.6 + 10 = -3.6$$

$$T_2 = 68 + 2(-3.6) = 68 - 7.2 = 60.8$$

**Step 3:** $t_2 = 4$, $T_2 = 60.8$

$$f(4, 60.8) = -0.2(60.8) + 10 = -12.16 + 10 = -2.16$$

$$T_3 = 60.8 + 2(-2.16) = 60.8 - 4.32 = 56.48$$

**Step 4:** $t_3 = 6$, $T_3 = 56.48$

$$f(6, 56.48) = -0.2(56.48) + 10 = -11.296 + 10 = -1.296$$

$$T_4 = 56.48 + 2(-1.296) = 56.48 - 2.592 = 53.888$$

Therefore $T(8) \approx 53.89$.

**Common mistake:** Stopping one step early and reporting $T(6) = 56.48$ (choice B) or $T(4) = 60.80$ (choice C). With $\Delta t = 2$, reaching $t = 8$ requires $\dfrac{8 - 0}{2} = 4$ steps, not $3$. Another error is using $\Delta t = 1$ instead of $\Delta t = 2$.

</details>

<details>
<summary><strong>Question 35</strong></summary>

**Leviathan's spiral descent through an undersea canyon is given by $x(t) = e^t \cos t$ and $y(t) = e^t \sin t$ for $0 \le t \le \pi$. The arc length of this path is closest to**

**(A)** $24.85$ | **(B)** $28.14$ | **(C)** $31.31$ | **(D)** $36.47$

**Answer: (C) $31.31$**

**Solution:**

The arc length of a parametric curve is:

$$L = \int_0^{\pi} \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2}\,dt$$

Find the derivatives:

$$\frac{dx}{dt} = e^t \cos t - e^t \sin t = e^t(\cos t - \sin t)$$

$$\frac{dy}{dt} = e^t \sin t + e^t \cos t = e^t(\sin t + \cos t)$$

Compute the sum of squares:

$$\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2 = e^{2t}(\cos t - \sin t)^2 + e^{2t}(\sin t + \cos t)^2$$

$$= e^{2t}\left[(\cos^2 t - 2\sin t\cos t + \sin^2 t) + (\sin^2 t + 2\sin t\cos t + \cos^2 t)\right]$$

$$= e^{2t}\left[1 - 2\sin t\cos t + 1 + 2\sin t\cos t\right] = e^{2t} \cdot 2 = 2e^{2t}$$

Therefore the speed is $\sqrt{2e^{2t}} = \sqrt{2}\,e^t$, and:

$$L = \int_0^{\pi} \sqrt{2}\,e^t\,dt = \sqrt{2}\left[e^t\right]_0^{\pi} = \sqrt{2}(e^{\pi} - 1)$$

Using a calculator: $e^{\pi} \approx 23.1407$, so:

$$L = \sqrt{2}(23.1407 - 1) = 1.4142 \times 22.1407 \approx 31.31$$

**Common mistake:** Forgetting to apply the product rule when differentiating $e^t\cos t$ and $e^t\sin t$ — writing $\dfrac{dx}{dt} = -e^t\sin t$ instead of $e^t(\cos t - \sin t)$. Or not simplifying the expression under the radical and attempting to evaluate a more complicated integral numerically when the exact form $\sqrt{2}\,e^t$ is available.

</details>

<details>
<summary><strong>Question 36</strong></summary>

**The population of chemosynthetic bacteria near a hydrothermal vent follows the logistic model $\dfrac{dN}{dt} = 0.05N\!\left(1 - \dfrac{N}{8000}\right)$, where $N$ is measured in thousands. The population is growing fastest when $N =$**

**(A)** $2000$ | **(B)** $4000$ | **(C)** $6000$ | **(D)** $8000$

**Answer: (B) $4000$**

**Solution:**

This is the standard logistic growth equation $\dfrac{dN}{dt} = rN\!\left(1 - \dfrac{N}{K}\right)$ with growth rate $r = 0.05$ and carrying capacity $K = 8000$.

A fundamental property of the logistic model is that the growth rate $\dfrac{dN}{dt}$ is maximized when the population is at exactly half the carrying capacity:

$$N = \frac{K}{2} = \frac{8000}{2} = 4000$$

**Verification:** The growth rate function $g(N) = 0.05N\!\left(1 - \dfrac{N}{8000}\right) = 0.05N - \dfrac{0.05N^2}{8000}$ is a downward-opening parabola in $N$. Taking its derivative with respect to $N$:

$$g'(N) = 0.05 - \frac{0.05 \cdot 2N}{8000} = 0.05 - \frac{N}{80000}$$

Setting $g'(N) = 0$:

$$0.05 = \frac{N}{80000} \implies N = 4000$$

Since $g''(N) = -\dfrac{1}{80000} < 0$, this is indeed a maximum.

**Common mistake:** Choosing $K = 8000$ (choice D), which is the carrying capacity — the population level where growth stops entirely ($\dfrac{dN}{dt} = 0$), not where growth is fastest. Or confusing the carrying capacity with the maximum growth rate.

</details>

<details>
<summary><strong>Question 37</strong></summary>

**The region bounded by $y = \dfrac{4}{1 + x^2}$, $y = 0$, $x = 0$, and $x = 2$ is revolved about the $y$-axis. The volume of the resulting solid is closest to**

**(A)** $14.47$ | **(B)** $17.63$ | **(C)** $18.85$ | **(D)** $20.23$

**Answer: (D) $20.23$**

**Solution:**

Since we revolve about the $y$-axis and the region is described in terms of $x$, the **shell method** is the most efficient approach:

$$V = 2\pi \int_0^2 x \cdot \frac{4}{1 + x^2}\,dx = 8\pi \int_0^2 \frac{x}{1 + x^2}\,dx$$

Use $u$-substitution: let $u = 1 + x^2$, so $du = 2x\,dx$, meaning $x\,dx = \dfrac{du}{2}$.

Change limits: when $x = 0$, $u = 1$; when $x = 2$, $u = 5$.

$$V = 8\pi \cdot \frac{1}{2}\int_1^5 \frac{du}{u} = 4\pi \left[\ln u\right]_1^5 = 4\pi(\ln 5 - \ln 1) = 4\pi \ln 5$$

Using a calculator:

$$V = 4\pi \ln 5 \approx 4(3.14159)(1.6094) \approx 20.22$$

**Common mistake:** Using the disk/washer method instead of shells. Since the axis of revolution is the $y$-axis and the bounds are given in $x$, the disk method would require solving for $x$ in terms of $y$ and splitting the integral — much more complicated. Another error is forgetting the factor of $x$ in the shell method formula (computing $2\pi \int \dfrac{4}{1+x^2}\,dx$ instead of $2\pi \int \dfrac{4x}{1+x^2}\,dx$).

</details>

<details>
<summary><strong>Question 38</strong></summary>

**Leviathan's sonar return signal strength is $S(r) = \dfrac{100}{r^{1.5}}$ watts, where $r$ is range in km. The total energy received from $r = 1$ to $r = \infty$ is $\displaystyle \int_1^{\infty} \frac{100}{r^{1.5}}\,dr$. This integral equals**

**(A)** $200$ | **(B)** $100$ | **(C)** $50$ | **(D)** The integral diverges

**Answer: (A) $200$**

**Solution:**

Rewrite the integrand using exponent notation:

$$\int_1^{\infty} 100\,r^{-3/2}\,dr = \lim_{b \to \infty} \int_1^{b} 100\,r^{-3/2}\,dr$$

Find the antiderivative using the power rule:

$$\int r^{-3/2}\,dr = \frac{r^{-1/2}}{-1/2} = -2r^{-1/2} = \frac{-2}{\sqrt{r}}$$

Evaluate:

$$\lim_{b \to \infty} \left[\frac{-200}{\sqrt{r}}\right]_1^{b} = \lim_{b \to \infty} \left(\frac{-200}{\sqrt{b}} - \frac{-200}{\sqrt{1}}\right)$$

$$= \lim_{b \to \infty} \left(\frac{-200}{\sqrt{b}} + 200\right) = 0 + 200 = 200$$

The integral converges to $200$.

**Key insight:** This is a $p$-integral $\int_1^{\infty} r^{-p}\,dr$ with $p = 1.5 > 1$, so it converges. If $p \le 1$, it would diverge.

**Common mistake:** Thinking all improper integrals to infinity must diverge (choosing D). Or making an error with the power rule: writing the antiderivative of $r^{-3/2}$ as $\dfrac{r^{-1/2}}{-3/2}$ instead of $\dfrac{r^{-1/2}}{-1/2}$, which would give $\dfrac{200}{3} \approx 66.7$ — not matching any choice.

</details>

<details>
<summary><strong>Question 39</strong></summary>

**Leviathan's position relative to the deployment ship is $\vec{r}(t) = \langle 50\cos(0.2t), \; 30\sin(0.3t), \; -5t \rangle$ meters. The speed of Leviathan at $t = 10$ seconds is closest to**

**(A)** $8.22$ m/s | **(B)** $10.45$ m/s | **(C)** $13.68$ m/s | **(D)** $16.91$ m/s

**Answer: (C) $13.68$ m/s**

**Solution:**

Speed is the magnitude of the velocity vector. First, find $\vec{v}(t) = \vec{r}\,'(t)$:

$$\vec{v}(t) = \left\langle -50(0.2)\sin(0.2t), \; 30(0.3)\cos(0.3t), \; -5 \right\rangle = \langle -10\sin(0.2t), \; 9\cos(0.3t), \; -5 \rangle$$

At $t = 10$:

$$\vec{v}(10) = \langle -10\sin(2), \; 9\cos(3), \; -5 \rangle$$

Using a calculator (radians):

$$\sin(2) \approx 0.9093, \quad \cos(3) \approx -0.9900$$

$$\vec{v}(10) \approx \langle -9.093, \; -8.910, \; -5 \rangle$$

The speed is:

$$|\vec{v}(10)| = \sqrt{(-9.093)^2 + (-8.910)^2 + (-5)^2}$$

$$= \sqrt{82.68 + 79.39 + 25} = \sqrt{187.07} \approx 13.68 \text{ m/s}$$

**Common mistake:** Forgetting the chain rule when differentiating — writing $\vec{v}(t) = \langle -50\sin(0.2t), \; 30\cos(0.3t), \; -5 \rangle$ instead of multiplying by the inner derivatives $0.2$ and $0.3$. This leads to component values that are $5\times$ and $\tfrac{10}{3}\times$ too large, giving an incorrect speed.

</details>

<details>
<summary><strong>Question 40</strong></summary>

**A sonar sweep pattern is described by the polar curve $r = 4\sin 2\theta$. The total area enclosed by one petal of this curve is**

**(A)** $\pi$ | **(B)** $2\pi$ | **(C)** $4\pi$ | **(D)** $8\pi$

**Answer: (B) $2\pi$**

**Solution:**

The curve $r = 4\sin 2\theta$ is a four-petaled rose. One petal is traced out when $\sin 2\theta \ge 0$, for example from $\theta = 0$ to $\theta = \dfrac{\pi}{2}$.

The area enclosed by a polar curve is:

$$A = \frac{1}{2}\int_{\alpha}^{\beta} r^2\,d\theta = \frac{1}{2}\int_0^{\pi/2} (4\sin 2\theta)^2\,d\theta$$

$$= \frac{1}{2}\int_0^{\pi/2} 16\sin^2 2\theta\,d\theta = 8\int_0^{\pi/2} \sin^2 2\theta\,d\theta$$

Use the half-angle identity $\sin^2 u = \dfrac{1 - \cos 2u}{2}$ with $u = 2\theta$:

$$= 8\int_0^{\pi/2} \frac{1 - \cos 4\theta}{2}\,d\theta = 4\int_0^{\pi/2} (1 - \cos 4\theta)\,d\theta$$

$$= 4\left[\theta - \frac{\sin 4\theta}{4}\right]_0^{\pi/2} = 4\left[\left(\frac{\pi}{2} - \frac{\sin 2\pi}{4}\right) - \left(0 - 0\right)\right]$$

$$= 4\left(\frac{\pi}{2} - 0\right) = 2\pi$$

**Common mistake:** Computing the total area of all four petals ($8\pi$, choice D) instead of just one petal. Or using the wrong limits of integration — for instance, integrating from $0$ to $\pi$ traces two petals, not one.

</details>

<details>
<summary><strong>Question 41</strong></summary>

**Leviathan's depth readings are recorded every 5 minutes during descent:**

| $t$ (min) | $0$ | $5$ | $10$ | $15$ | $20$ | $25$ | $30$ |
|-----------|-----|------|------|------|------|------|------|
| $d(t)$ (m) | $0$ | $180$ | $520$ | $1100$ | $1850$ | $2700$ | $3400$ |

**Using a trapezoidal sum with 6 subintervals, the approximate total depth-time (in m$\cdot$min) from $t = 0$ to $t = 30$ is**

**(A)** $36{,}500$ | **(B)** $38{,}125$ | **(C)** $39{,}500$ | **(D)** $40{,}250$

**Answer: (D) $40{,}250$**

**Solution:**

The trapezoidal rule with $n = 6$ subintervals of width $\Delta t = 5$ is:

$$\int_0^{30} d(t)\,dt \approx \frac{\Delta t}{2}\left[d(t_0) + 2d(t_1) + 2d(t_2) + 2d(t_3) + 2d(t_4) + 2d(t_5) + d(t_6)\right]$$

$$= \frac{5}{2}\left[0 + 2(180) + 2(520) + 2(1100) + 2(1850) + 2(2700) + 3400\right]$$

$$= \frac{5}{2}\left[0 + 360 + 1040 + 2200 + 3700 + 5400 + 3400\right]$$

$$= \frac{5}{2}\left[16100\right] = \frac{80500}{2} = 40250$$

**Alternatively**, compute each trapezoid individually:

$$T = \frac{5}{2}(0 + 180) + \frac{5}{2}(180 + 520) + \frac{5}{2}(520 + 1100) + \frac{5}{2}(1100 + 1850) + \frac{5}{2}(1850 + 2700) + \frac{5}{2}(2700 + 3400)$$

$$= \frac{5}{2}(180 + 700 + 1620 + 2950 + 4550 + 6100)$$

$$= \frac{5}{2}(16100) = 40250 \text{ m}\cdot\text{min}$$

**Common mistake:** Using the left or right Riemann sum instead of the trapezoidal sum. The left sum gives $5(0 + 180 + 520 + 1100 + 1850 + 2700) = 31750$, and the right sum gives $5(180 + 520 + 1100 + 1850 + 2700 + 3400) = 48750$. Also, forgetting the $\dfrac{1}{2}$ factor that makes the trapezoid formula different from a simple sum.

</details>

<details>
<summary><strong>Question 42</strong></summary>

**The Maclaurin series for $e^x$ is used to approximate $\displaystyle \int_0^{0.5} e^{-x^3}\,dx$. Using the first three nonzero terms of the resulting series, the approximation is closest to**

**(A)** $0.4744$ | **(B)** $0.4849$ | **(C)** $0.4938$ | **(D)** $0.5000$

**Answer: (B) $0.4849$**

**Solution:**

Start with the Maclaurin series for $e^u$:

$$e^u = 1 + u + \frac{u^2}{2!} + \frac{u^3}{3!} + \cdots$$

Substitute $u = -x^3$:

$$e^{-x^3} = 1 + (-x^3) + \frac{(-x^3)^2}{2!} + \cdots = 1 - x^3 + \frac{x^6}{2} - \cdots$$

The first three nonzero terms are $1 - x^3 + \dfrac{x^6}{2}$. Integrate term by term from $0$ to $0.5$:

$$\int_0^{0.5} \left(1 - x^3 + \frac{x^6}{2}\right)dx = \left[x - \frac{x^4}{4} + \frac{x^7}{14}\right]_0^{0.5}$$

Using a calculator with $x = 0.5$:

$$= 0.5 - \frac{(0.5)^4}{4} + \frac{(0.5)^7}{14}$$

$$= 0.5 - \frac{0.0625}{4} + \frac{0.0078125}{14}$$

$$= 0.5 - 0.015625 + 0.000558$$

$$\approx 0.4849$$

**Common mistake:** Using the series for $e^{x^3}$ (with positive terms) instead of $e^{-x^3}$ (alternating signs). Or integrating the series for $e^{-x^3}$ itself rather than substituting $-x^3$ into the $e^u$ series — i.e., writing $e^{-x^3} = 1 - x^3 + \dfrac{x^6}{2!}$ but then incorrectly computing $\int x^6/2\,dx = \dfrac{x^7}{12}$ instead of $\dfrac{x^7}{14}$.

</details>

<details>
<summary><strong>Question 43</strong></summary>

**The cross section of a sediment deposit is modeled by the region between $y = 5\sin\!\left(\dfrac{\pi x}{3}\right)$ and $y = x$ for $0 \le x \le 3$. The area of this region is closest to**

**(A)** $6.52$ | **(B)** $7.39$ | **(C)** $8.24$ | **(D)** $9.11$

**Answer: (A) $6.52$**

**Solution:**

First, find where the curves intersect on $[0, 3]$. Set $5\sin\!\left(\dfrac{\pi x}{3}\right) = x$.

At $x = 0$: both sides equal $0$ (intersection).

Using a calculator, the curves also intersect at $x = 2.5$: $5\sin\!\left(\dfrac{2.5\pi}{3}\right) = 5\sin\!\left(\dfrac{5\pi}{6}\right) = 5 \cdot 0.5 = 2.5$ ✓

Check which function is on top between $0$ and $2.5$. At $x = 1$: $5\sin\!\left(\dfrac{\pi}{3}\right) = 5 \cdot \dfrac{\sqrt{3}}{2} \approx 4.33 > 1$. So $5\sin\!\left(\dfrac{\pi x}{3}\right) > x$ on $(0, 2.5)$.

On $(2.5, 3)$: at $x = 3$, $5\sin(\pi) = 0 < 3$. So $x > 5\sin\!\left(\dfrac{\pi x}{3}\right)$ on $(2.5, 3)$.

The total area is:

$$A = \int_0^{2.5}\left[5\sin\!\left(\frac{\pi x}{3}\right) - x\right]dx + \int_{2.5}^{3}\left[x - 5\sin\!\left(\frac{\pi x}{3}\right)\right]dx$$

**First integral:** Using a calculator:

$$\int_0^{2.5}\left[5\sin\!\left(\frac{\pi x}{3}\right) - x\right]dx \approx 5.78$$

**Second integral:** Using a calculator:

$$\int_{2.5}^{3}\left[x - 5\sin\!\left(\frac{\pi x}{3}\right)\right]dx \approx 0.74$$

**Total area:**

$$A \approx 5.78 + 0.74 = 6.52$$

**Common mistake:** Not realizing the curves cross at $x = 2.5$ and integrating $\int_0^3\left[5\sin\!\left(\dfrac{\pi x}{3}\right) - x\right]dx$ without absolute values, which gives $\approx 5.05$ (the net signed area, not the total area). Always check for intersections within the interval when finding the area "between" two curves.

</details>

<details>
<summary><strong>Question 44</strong></summary>

**The power series $\displaystyle \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+1}}{2n+1}$ represents which function?**

**(A)** $\sin x$ | **(B)** $\ln(1 + x)$ | **(C)** $\arctan x$ | **(D)** $\tanh x$

**Answer: (C) $\arctan x$**

**Solution:**

Write out the first several terms of the series:

$$\sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+1}}{2n+1} = x - \frac{x^3}{3} + \frac{x^5}{5} - \frac{x^7}{7} + \cdots$$

Compare with the known Maclaurin series:

- $\sin x = x - \dfrac{x^3}{3!} + \dfrac{x^5}{5!} - \cdots = x - \dfrac{x^3}{6} + \dfrac{x^5}{120} - \cdots$ — denominators are factorials, not matching.

- $\ln(1 + x) = x - \dfrac{x^2}{2} + \dfrac{x^3}{3} - \cdots$ — has even powers, not matching.

- $\arctan x = x - \dfrac{x^3}{3} + \dfrac{x^5}{5} - \dfrac{x^7}{7} + \cdots$ — **matches exactly!** ✓

- $\tanh x = x - \dfrac{x^3}{3} + \dfrac{2x^5}{15} - \cdots$ — coefficient of $x^5$ is $\dfrac{2}{15}$, not $\dfrac{1}{5}$.

**Derivation:** Start with the geometric series $\dfrac{1}{1 + t^2} = \displaystyle\sum_{n=0}^{\infty} (-1)^n t^{2n}$ for $|t| < 1$. Integrate both sides from $0$ to $x$:

$$\arctan x = \int_0^x \frac{dt}{1 + t^2} = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{2n+1}$$

**Common mistake:** Confusing the series for $\arctan x$ with $\sin x$. Both have odd powers and alternating signs, but the denominators are different: $\arctan x$ has $2n + 1$ (odd integers), while $\sin x$ has $(2n + 1)!$ (factorials of odd integers).

</details>

<details>
<summary><strong>Question 45</strong></summary>

**Leviathan's onboard computer evaluates $\displaystyle \int_1^{5} \frac{\ln x}{x^2}\,dx$. The value is closest to**

**(A)** $0.2944$ | **(B)** $0.3617$ | **(C)** $0.4103$ | **(D)** $0.4781$

**Answer: (D) $0.4781$**

**Solution:**

Use integration by parts. Let $u = \ln x$ and $dv = x^{-2}\,dx$:

$$du = \frac{1}{x}\,dx, \qquad v = \frac{x^{-1}}{-1} = -\frac{1}{x}$$

Apply the formula $\int u\,dv = uv - \int v\,du$:

$$\int_1^5 \frac{\ln x}{x^2}\,dx = \left[-\frac{\ln x}{x}\right]_1^5 - \int_1^5 \left(-\frac{1}{x}\right)\cdot\frac{1}{x}\,dx$$

$$= \left[-\frac{\ln x}{x}\right]_1^5 + \int_1^5 \frac{1}{x^2}\,dx$$

Evaluate the boundary term:

$$\left[-\frac{\ln x}{x}\right]_1^5 = -\frac{\ln 5}{5} - \left(-\frac{\ln 1}{1}\right) = -\frac{\ln 5}{5} + 0 = -\frac{\ln 5}{5}$$

Evaluate the remaining integral:

$$\int_1^5 \frac{1}{x^2}\,dx = \left[-\frac{1}{x}\right]_1^5 = -\frac{1}{5} - (-1) = -\frac{1}{5} + 1 = \frac{4}{5}$$

Combine:

$$\int_1^5 \frac{\ln x}{x^2}\,dx = -\frac{\ln 5}{5} + \frac{4}{5}$$

Using a calculator: $\ln 5 \approx 1.6094$, so:

$$= -\frac{1.6094}{5} + \frac{4}{5} = -0.3219 + 0.8 = 0.4781$$

**Common mistake:** Choosing the wrong parts — setting $u = \dfrac{1}{x^2}$ and $dv = \ln x\,dx$ makes the integral harder, not easier. Also, sign errors are common when evaluating $v = -\dfrac{1}{x}$ and then computing $-\int v\,du$, where the double negative must be handled carefully.

</details>

---

## Section II: Free Response Solutions

### Part A — Calculator Allowed

### Question 1

<details>
<summary><strong>Full Solution</strong></summary>

**Leviathan's vertical velocity (in meters per minute, positive = descending) during an emergency ascent-and-redive maneuver is modeled by**

$$v(t) = \begin{cases} -60 + 4t^2 & 0 \le t \le 5 \\ 40 + 25\sin\!\left(\dfrac{\pi(t - 5)}{10}\right) & 5 < t \le 15 \end{cases}$$

**where $t$ is in minutes after the maneuver begins.**

**(a)** Find Leviathan's acceleration at $t = 3$ minutes. Is Leviathan's speed increasing or decreasing at that moment? Justify your answer.

**Solution:**

For $0 \le t \le 5$, we have $v(t) = -60 + 4t^2$, so:

$$a(t) = v'(t) = 8t$$

**[1 point]** At $t = 3$:

$$a(3) = 8(3) = 24 \text{ m/min}^2$$

**[1 point]** Now determine whether speed is increasing or decreasing. We need the velocity at $t = 3$:

$$v(3) = -60 + 4(9) = -60 + 36 = -24 \text{ m/min}$$

Since $v(3) = -24 < 0$ and $a(3) = 24 > 0$, the velocity and acceleration have **opposite signs**. When velocity and acceleration have opposite signs, the speed (absolute value of velocity) is **decreasing**.

$$\boxed{a(3) = 24 \text{ m/min}^2; \text{ speed is decreasing because } v(3) \text{ and } a(3) \text{ have opposite signs.}}$$

---

**(b)** Find the total distance Leviathan travels (vertically) from $t = 0$ to $t = 15$ minutes.

**Solution:**

**[1 point]** Total distance $= \displaystyle\int_0^{15} |v(t)|\,dt$. We must find where $v(t) = 0$ on each piece.

**Piece 1** ($0 \le t \le 5$): Set $-60 + 4t^2 = 0$:

$$4t^2 = 60 \implies t^2 = 15 \implies t = \sqrt{15} \approx 3.873$$

For $0 \le t < \sqrt{15}$: $v(t) < 0$ (ascending). For $\sqrt{15} < t \le 5$: $v(t) > 0$ (descending).

**Piece 2** ($5 < t \le 15$): $v(t) = 40 + 25\sin\!\left(\dfrac{\pi(t-5)}{10}\right)$. Since $|\sin(\cdot)| \le 1$, we have $v(t) \ge 40 - 25 = 15 > 0$ for all $t$ in $(5, 15]$. So $v(t) > 0$ throughout this piece.

**[1 point]** Compute each integral:

$$\int_0^{\sqrt{15}} |v(t)|\,dt = \int_0^{\sqrt{15}} (60 - 4t^2)\,dt = \left[60t - \frac{4t^3}{3}\right]_0^{\sqrt{15}}$$

$$= 60\sqrt{15} - \frac{4(\sqrt{15})^3}{3} = 60\sqrt{15} - \frac{4 \cdot 15\sqrt{15}}{3} = 60\sqrt{15} - 20\sqrt{15} = 40\sqrt{15}$$

$$\int_{\sqrt{15}}^{5} (- 60 + 4t^2)\,dt = \left[-60t + \frac{4t^3}{3}\right]_{\sqrt{15}}^{5}$$

$$= \left(-300 + \frac{500}{3}\right) - \left(-60\sqrt{15} + 20\sqrt{15}\right) = -\frac{400}{3} + 40\sqrt{15}$$

$$\int_5^{15} \left[40 + 25\sin\!\left(\frac{\pi(t-5)}{10}\right)\right]dt = \left[40t\right]_5^{15} + 25\left[-\frac{10}{\pi}\cos\!\left(\frac{\pi(t-5)}{10}\right)\right]_5^{15}$$

$$= 40(10) + 25\cdot\frac{-10}{\pi}\left[\cos(\pi) - \cos(0)\right] = 400 - \frac{250}{\pi}(-1 - 1) = 400 + \frac{500}{\pi}$$

**[1 point]** Combine all three pieces:

$$\text{Distance} = 40\sqrt{15} + \left(-\frac{400}{3} + 40\sqrt{15}\right) + 400 + \frac{500}{\pi}$$

$$= 80\sqrt{15} - \frac{400}{3} + 400 + \frac{500}{\pi}$$

Using a calculator: $\sqrt{15} \approx 3.87298$, so $80\sqrt{15} \approx 309.839$:

$$\approx 309.839 - 133.333 + 400 + 159.155 \approx 735.661$$

$$\boxed{\text{Distance} = 80\sqrt{15} - \frac{400}{3} + 400 + \frac{500}{\pi} \approx 735.66 \text{ meters}}$$

---

**(c)** Is there a time $t$ in the interval $[0, 5]$ where Leviathan's acceleration is exactly $20$ m/min$^2$? Justify your answer using a theorem from calculus.

**Solution:**

**[1 point]** From part (a), $a(t) = v'(t) = 8t$ on $[0, 5]$.

Evaluate: $a(0) = 0$ and $a(5) = 40$.

**[1 point]** Since $a(t) = 8t$ is continuous on $[0, 5]$ and $0 < 20 < 40$, by the **Intermediate Value Theorem**, there exists a value $c \in (0, 5)$ such that $a(c) = 20$.

In fact, $8c = 20 \implies c = 2.5$, and indeed $a(2.5) = 8(2.5) = 20$ m/min$^2$.

Alternatively, applying the **Mean Value Theorem** to $v(t)$: since $v$ is continuous on $[0, 5]$ and differentiable on $(0, 5)$:

$$\frac{v(5) - v(0)}{5 - 0} = \frac{(-60 + 100) - (-60)}{5} = \frac{40 - (-60)}{5} = \frac{100}{5} = 20$$

By the MVT, there exists $c \in (0, 5)$ with $v'(c) = a(c) = 20$ m/min$^2$.

$$\boxed{\text{Yes. By the IVT (or MVT), there exists } c \in (0, 5) \text{ with } a(c) = 20.}$$

---

**(d)** At what time $t$ in the interval $(5, 15)$ does Leviathan's velocity first equal $55$ m/min? Find the acceleration at that instant.

**Solution:**

**[1 point]** Set $v(t) = 55$ on the second piece:

$$40 + 25\sin\!\left(\frac{\pi(t - 5)}{10}\right) = 55$$

$$25\sin\!\left(\frac{\pi(t - 5)}{10}\right) = 15$$

$$\sin\!\left(\frac{\pi(t - 5)}{10}\right) = \frac{15}{25} = \frac{3}{5}$$

The **first** solution (smallest positive value):

$$\frac{\pi(t - 5)}{10} = \arcsin\!\left(\frac{3}{5}\right) \approx 0.6435$$

$$t - 5 = \frac{10(0.6435)}{\pi} \approx \frac{6.435}{3.14159} \approx 2.048$$

$$t \approx 7.048 \text{ minutes}$$

**[1 point]** Now find the acceleration. For $5 < t \le 15$:

$$a(t) = v'(t) = 25 \cdot \frac{\pi}{10}\cos\!\left(\frac{\pi(t - 5)}{10}\right) = \frac{5\pi}{2}\cos\!\left(\frac{\pi(t - 5)}{10}\right)$$

Since $\sin\!\left(\dfrac{\pi(t-5)}{10}\right) = \dfrac{3}{5}$, we use the Pythagorean identity:

$$\cos\!\left(\frac{\pi(t-5)}{10}\right) = \sqrt{1 - \left(\frac{3}{5}\right)^2} = \sqrt{1 - \frac{9}{25}} = \sqrt{\frac{16}{25}} = \frac{4}{5}$$

(Positive because $\dfrac{\pi(t-5)}{10} \approx 0.6435$ is in the first quadrant.)

$$a = \frac{5\pi}{2} \cdot \frac{4}{5} = 2\pi \approx 6.283 \text{ m/min}^2$$

$$\boxed{t \approx 7.048 \text{ min}, \quad a = 2\pi \approx 6.283 \text{ m/min}^2}$$

---

**Scoring Guidelines (9 points total)**
- Part (a): 2 points — 1 point for $a(3) = 24$; 1 point for correct justification that speed is decreasing (opposite signs of $v$ and $a$)
- Part (b): 3 points — 1 point for identifying $t = \sqrt{15}$ as the zero of $v$; 1 point for correct absolute-value integrals on each piece; 1 point for correct final numerical answer
- Part (c): 2 points — 1 point for invoking the IVT or MVT with correct hypotheses; 1 point for correct conclusion
- Part (d): 2 points — 1 point for correct time $t \approx 7.048$; 1 point for correct acceleration $a = 2\pi$

</details>

### Question 2

<details>
<summary><strong>Full Solution</strong></summary>

**A hydrothermal vent releases superheated water at a rate modeled by**

$$F(t) = 200\left(1 + 0.4\sin(0.5t)\right) e^{-0.05t}$$

**liters per minute, where $t$ is in minutes, for $0 \le t \le 30$.**

**(a)** Find the total volume of superheated water released from $t = 0$ to $t = 30$ minutes. Round to the nearest liter.

**Solution:**

**[1 point]** The total volume is:

$$V = \int_0^{30} F(t)\,dt = \int_0^{30} 200\left(1 + 0.4\sin(0.5t)\right)e^{-0.05t}\,dt$$

Split into two integrals:

$$V = \underbrace{\int_0^{30} 200\,e^{-0.05t}\,dt}_{I_1} + \underbrace{\int_0^{30} 80\sin(0.5t)\,e^{-0.05t}\,dt}_{I_2}$$

**Integral $I_1$:**

$$I_1 = 200\left[-\frac{1}{0.05}e^{-0.05t}\right]_0^{30} = 200(-20)\left[e^{-1.5} - 1\right] = -4000\left(e^{-1.5} - 1\right) = 4000\left(1 - e^{-1.5}\right)$$

$$= 4000(1 - 0.22313) = 4000(0.77687) \approx 3107.5$$

**Integral $I_2$:** Using the formula $\displaystyle\int e^{at}\sin(bt)\,dt = \frac{e^{at}(a\sin bt - b\cos bt)}{a^2 + b^2}$, with $a = -0.05$, $b = 0.5$:

$$a^2 + b^2 = 0.0025 + 0.25 = 0.2525$$

$$I_2 = 80\left[\frac{e^{-0.05t}(-0.05\sin(0.5t) - 0.5\cos(0.5t))}{0.2525}\right]_0^{30}$$

At $t = 30$: $\sin(15) \approx 0.6503$, $\cos(15) \approx -0.7597$, $e^{-1.5} \approx 0.22313$:

$$= \frac{0.22313(-0.05(0.6503) - 0.5(-0.7597))}{0.2525} = \frac{0.22313(-0.03252 + 0.37985)}{0.2525} = \frac{0.22313(0.34733)}{0.2525} \approx 0.30700$$

At $t = 0$: $\sin(0) = 0$, $\cos(0) = 1$, $e^{0} = 1$:

$$= \frac{1(-0 - 0.5)}{0.2525} = \frac{-0.5}{0.2525} \approx -1.98020$$

$$I_2 = 80\left(0.30700 - (-1.98020)\right) = 80(2.28720) \approx 182.98$$

**[1 point]** Total volume:

$$V \approx 3107.5 + 183.0 = 3290.5$$

$$\boxed{V \approx 3291 \text{ liters}}$$

---

**(b)** Find the average rate of flow from $t = 0$ to $t = 30$ minutes. Include units in your answer.

**Solution:**

**[1 point]** The average rate of flow is:

$$\text{Average rate} = \frac{1}{30 - 0}\int_0^{30} F(t)\,dt = \frac{V}{30}$$

**[1 point]** Using the result from part (a):

$$= \frac{3291}{30} \approx 109.7$$

$$\boxed{\text{Average rate} \approx 109.7 \text{ liters per minute}}$$

---

**(c)** At what time $t$ in the interval $(0, 30)$ is the flow rate at its maximum? Justify your answer.

**Solution:**

**[1 point]** Find $F'(t)$ using the product rule:

$$F(t) = 200\left(1 + 0.4\sin(0.5t)\right)e^{-0.05t}$$

$$F'(t) = 200\,e^{-0.05t}\left[0.2\cos(0.5t) - 0.05\left(1 + 0.4\sin(0.5t)\right)\right]$$

$$= 200\,e^{-0.05t}\left[0.2\cos(0.5t) - 0.05 - 0.02\sin(0.5t)\right]$$

Since $200\,e^{-0.05t} > 0$ for all $t$, set the bracket equal to zero:

$$0.2\cos(0.5t) - 0.02\sin(0.5t) = 0.05$$

**[1 point]** Using a calculator to solve numerically, evaluate the left side at several values:

| $t$ | $0.2\cos(0.5t) - 0.02\sin(0.5t)$ | vs. $0.05$ |
|---|---|---|
| $0$ | $0.200$ | $> 0.05$ |
| $2$ | $0.2\cos(1) - 0.02\sin(1) \approx 0.0912$ | $> 0.05$ |
| $2.5$ | $0.2\cos(1.25) - 0.02\sin(1.25) \approx 0.0441$ | $< 0.05$ |

Refining: the first zero occurs at $t \approx 2.439$.

Check the sign of $F'$: $F'(t) > 0$ for $t < 2.439$ and $F'(t) < 0$ for $t$ just after $2.439$. By the **First Derivative Test**, $F$ has a **local maximum** at $t \approx 2.439$.

Comparing values at the critical point and endpoints:
- $F(0) = 200(1)(1) = 200$
- $F(2.439) \approx 200(1 + 0.4(0.9396))(0.8852) \approx 200(1.3758)(0.8852) \approx 243.6$
- $F(30) \approx 200(1 + 0.4(0.6503))(0.22313) \approx 56.2$

The maximum flow rate occurs at $t \approx 2.439$ minutes.

$$\boxed{t \approx 2.439 \text{ minutes (max flow rate } \approx 243.6 \text{ L/min)}}$$

---

**(d)** Leviathan's collection system captures superheated water at a rate of $G(t) = 120\,e^{-0.03t}$ liters per minute. Find the total net volume of uncollected water released from $t = 0$ to $t = 30$ minutes.

**Solution:**

**[1 point]** The net uncollected volume is:

$$\text{Net} = \int_0^{30} \left[F(t) - G(t)\right]\,dt = \int_0^{30} F(t)\,dt - \int_0^{30} G(t)\,dt$$

From part (a), $\displaystyle\int_0^{30} F(t)\,dt \approx 3291$.

**[1 point]** Compute $\displaystyle\int_0^{30} G(t)\,dt$:

$$\int_0^{30} 120\,e^{-0.03t}\,dt = 120\left[-\frac{1}{0.03}\,e^{-0.03t}\right]_0^{30} = -4000\left[e^{-0.9} - 1\right] = 4000\left(1 - e^{-0.9}\right)$$

$$= 4000(1 - 0.40657) = 4000(0.59343) \approx 2373.7$$

**[1 point]** Therefore:

$$\text{Net uncollected} \approx 3291 - 2374 \approx 917$$

$$\boxed{\text{Net uncollected volume} \approx 917 \text{ liters}}$$

---

**Scoring Guidelines (9 points total)**
- Part (a): 2 points — 1 point for correct integral setup; 1 point for correct numerical answer (rounded)
- Part (b): 2 points — 1 point for average value formula $\frac{1}{30}\int_0^{30}F(t)\,dt$; 1 point for correct answer with units
- Part (c): 2 points — 1 point for finding $F'(t) = 0$; 1 point for justification via First Derivative Test and comparison with endpoints
- Part (d): 3 points — 1 point for correct setup $\int[F - G]\,dt$; 1 point for evaluating $\int G(t)\,dt$; 1 point for correct final answer

</details>

### Part B — No Calculator

### Question 3

<details>
<summary><strong>Full Solution</strong></summary>

**The concentration $y$ of dissolved hydrogen sulfide (in mmol/L) near a hydrothermal vent varies with distance $x$ (in meters from the vent) according to the differential equation**

$$\frac{dy}{dx} = -\frac{y^2}{x + 1}, \qquad y > 0, \; x > -1$$

**(a)** On your own axes, sketch a slope field for the given differential equation at the twelve points $(x, y)$ for $x \in \{0, 1, 2\}$ and $y \in \{1, 2, 3, 4\}$.

**Solution:**

**[1 point]** Compute the slope $\dfrac{dy}{dx} = -\dfrac{y^2}{x + 1}$ at each of the twelve points:

| | $x = 0$ | $x = 1$ | $x = 2$ |
|---|---|---|---|
| $y = 1$ | $-\dfrac{1}{1} = -1$ | $-\dfrac{1}{2}$ | $-\dfrac{1}{3}$ |
| $y = 2$ | $-\dfrac{4}{1} = -4$ | $-\dfrac{4}{2} = -2$ | $-\dfrac{4}{3}$ |
| $y = 3$ | $-\dfrac{9}{1} = -9$ | $-\dfrac{9}{2}$ | $-\dfrac{9}{3} = -3$ |
| $y = 4$ | $-\dfrac{16}{1} = -16$ | $-\dfrac{16}{2} = -8$ | $-\dfrac{16}{3}$ |

**[1 point]** Key features of the slope field:
- **All slopes are negative** since $y^2 > 0$ and $x + 1 > 0$ for the given points, so $y$ is always decreasing.
- Slopes are **steeper** (more negative) for larger $y$ values and for smaller $x$ values.
- As $x$ increases, slopes become less steep (closer to zero) — concentration decreases more slowly farther from the vent.
- Draw short line segments at each point with the computed slope. The segments at $y = 4$, $x = 0$ are extremely steep (slope $= -16$, nearly vertical).

---

**(b)** Find the particular solution $y = f(x)$ to the differential equation with the initial condition $f(0) = 2$. Write your answer in explicit form.

**Solution:**

**[1 point]** Separate variables. Since $y > 0$, we can divide both sides by $y^2$:

$$\frac{dy}{y^2} = -\frac{dx}{x + 1}$$

**[1 point]** Integrate both sides:

$$\int y^{-2}\,dy = -\int \frac{dx}{x + 1}$$

$$-\frac{1}{y} = -\ln|x + 1| + C$$

Since $x > -1$, we have $x + 1 > 0$, so $|x + 1| = x + 1$:

$$-\frac{1}{y} = -\ln(x + 1) + C$$

Multiply both sides by $-1$:

$$\frac{1}{y} = \ln(x + 1) - C$$

**[1 point]** Apply the initial condition $f(0) = 2$ (i.e., $y = 2$ when $x = 0$):

$$\frac{1}{2} = \ln(0 + 1) - C = \ln(1) - C = 0 - C = -C$$

$$C = -\frac{1}{2}$$

So $\dfrac{1}{y} = \ln(x + 1) + \dfrac{1}{2}$.

Solve for $y$:

$$y = \frac{1}{\ln(x + 1) + \dfrac{1}{2}} = \frac{2}{2\ln(x + 1) + 1}$$

$$\boxed{f(x) = \frac{2}{2\ln(x + 1) + 1}}$$

---

**(c)** For the particular solution found in part (b), find the domain of $f$ and describe the behavior of $f(x)$ as $x \to \infty$.

**Solution:**

**[1 point]** The domain requires two conditions:
1. $x > -1$ (given in the original DE)
2. The denominator $2\ln(x + 1) + 1 \neq 0$, and since $y > 0$, we need $2\ln(x + 1) + 1 > 0$

From condition 2:

$$2\ln(x + 1) + 1 > 0 \implies \ln(x + 1) > -\frac{1}{2} \implies x + 1 > e^{-1/2} \implies x > e^{-1/2} - 1$$

Since $e^{-1/2} - 1 \approx -0.3935 > -1$, condition 2 is the binding constraint.

$$\boxed{\text{Domain: } x > e^{-1/2} - 1, \quad\text{i.e., } x > \frac{1}{\sqrt{e}} - 1}$$

**[1 point]** Behavior as $x \to \infty$:

As $x \to \infty$, $\ln(x + 1) \to \infty$, so $2\ln(x + 1) + 1 \to \infty$, and therefore:

$$f(x) = \frac{2}{2\ln(x + 1) + 1} \to 0^+$$

The concentration of dissolved hydrogen sulfide **approaches $0$** as the distance from the vent increases without bound. This makes physical sense: the chemical becomes increasingly diluted farther from its source.

---

**(d)** Explain why the solution found in part (b) satisfies $f(x) > 0$ for all $x$ in its domain. Is $f$ concave up or concave down on its domain? Justify your answer.

**Solution:**

**[1 point]** **Why $f(x) > 0$:** On the domain $x > e^{-1/2} - 1$, we have $\ln(x + 1) > -\dfrac{1}{2}$, which means:

$$2\ln(x + 1) + 1 > 0$$

Since the numerator $2 > 0$ and the denominator is positive, $f(x) = \dfrac{2}{2\ln(x+1) + 1} > 0$ for all $x$ in the domain.

**[1 point]** **Concavity:** Find $\dfrac{d^2y}{dx^2}$ by differentiating the DE. Starting from $\dfrac{dy}{dx} = -\dfrac{y^2}{x+1}$, differentiate both sides with respect to $x$ using the quotient rule:

$$\frac{d^2y}{dx^2} = \frac{d}{dx}\!\left[-\frac{y^2}{x+1}\right] = -\frac{2y\,\dfrac{dy}{dx}\,(x+1) - y^2 \cdot 1}{(x+1)^2}$$

$$= \frac{-2y\,\dfrac{dy}{dx}\,(x+1) + y^2}{(x+1)^2}$$

Substitute $\dfrac{dy}{dx} = -\dfrac{y^2}{x+1}$:

$$= \frac{-2y\!\left(-\dfrac{y^2}{x+1}\right)(x+1) + y^2}{(x+1)^2} = \frac{2y^3 + y^2}{(x+1)^2} = \frac{y^2(2y + 1)}{(x+1)^2}$$

Since $y > 0$ on the domain:
- $y^2 > 0$
- $2y + 1 > 0$
- $(x + 1)^2 > 0$

Therefore $\dfrac{d^2y}{dx^2} > 0$ for all $x$ in the domain.

$$\boxed{f \text{ is concave up on its entire domain because } f''(x) = \frac{y^2(2y + 1)}{(x+1)^2} > 0.}$$

---

**Scoring Guidelines (9 points total)**
- Part (a): 2 points — 1 point for correct slopes at all twelve points; 1 point for correctly drawn line segments consistent with the computed slopes
- Part (b): 3 points — 1 point for separating variables correctly; 1 point for correct antiderivatives on both sides; 1 point for applying the initial condition and solving for explicit $y$
- Part (c): 2 points — 1 point for correct domain $x > e^{-1/2} - 1$; 1 point for correct limit behavior as $x \to \infty$
- Part (d): 2 points — 1 point for explaining $f(x) > 0$; 1 point for computing $f''(x)$ and concluding concave up with justification

</details>

<details>
<summary><strong>Free Response 4</strong></summary>

**Leviathan's sonar return amplitude as a function of range is modeled by $f(x) = \dfrac{x}{(1 + x)^3}$, where $x$ is a normalized range parameter.**

---

**(a)** Find the first four nonzero terms of the Maclaurin series for $\dfrac{1}{(1 + x)^3}$ by taking successive derivatives at $x = 0$. Then write the first four nonzero terms of the Maclaurin series for $f(x)$.

Let $g(x) = (1 + x)^{-3}$. We compute derivatives and evaluate at $x = 0$:

$$g(x) = (1 + x)^{-3} \implies g(0) = 1$$

$$g'(x) = -3(1 + x)^{-4} \implies g'(0) = -3$$

$$g''(x) = 12(1 + x)^{-5} \implies g''(0) = 12$$

$$g'''(x) = -60(1 + x)^{-6} \implies g'''(0) = -60$$

Building the Maclaurin series $g(x) = \displaystyle\sum_{n=0}^{\infty} \frac{g^{(n)}(0)}{n!} x^n$:

$$\frac{1}{(1 + x)^3} = 1 + \frac{-3}{1!}x + \frac{12}{2!}x^2 + \frac{-60}{3!}x^3 + \cdots$$

$$\boxed{\frac{1}{(1 + x)^3} = 1 - 3x + 6x^2 - 10x^3 + \cdots}$$

> *Note:* The general term is $(-1)^n \dfrac{(n+1)(n+2)}{2}\, x^n$. *(1 pt for series of $1/(1+x)^3$)*

Now multiply by $x$ to obtain $f(x)$:

$$f(x) = \frac{x}{(1 + x)^3} = x\!\left(1 - 3x + 6x^2 - 10x^3 + \cdots\right)$$

$$\boxed{f(x) = x - 3x^2 + 6x^3 - 10x^4 + \cdots}$$

> *(1 pt for series of $f(x)$)*

---

**(b)** Use the series from part (a) to write the first four nonzero terms of a power series for $H(x) = \displaystyle\int_0^x \frac{t}{(1 + t)^3}\,dt$. Express $H(x)$ in closed form.

**Series for $H(x)$:** Integrate the series for $f(x)$ term by term:

$$H(x) = \int_0^x \!\left(t - 3t^2 + 6t^3 - 10t^4 + \cdots\right) dt$$

$$\boxed{H(x) = \frac{x^2}{2} - x^3 + \frac{3}{2}x^4 - 2x^5 + \cdots}$$

> *(1 pt for series integration)*

**Closed form:** Evaluate $\displaystyle\int_0^x \frac{t}{(1 + t)^3}\,dt$ directly. Let $u = 1 + t$, so $t = u - 1$ and $dt = du$. When $t = 0$, $u = 1$; when $t = x$, $u = 1 + x$.

$$\int_1^{1+x} \frac{u - 1}{u^3}\,du = \int_1^{1+x} \left(u^{-2} - u^{-3}\right) du$$

$$= \left[-u^{-1} + \frac{1}{2}u^{-2}\right]_1^{1+x}$$

$$= \left(-\frac{1}{1+x} + \frac{1}{2(1+x)^2}\right) - \left(-1 + \frac{1}{2}\right)$$

$$= -\frac{1}{1+x} + \frac{1}{2(1+x)^2} + \frac{1}{2}$$

$$\boxed{H(x) = \frac{1}{2} - \frac{1}{1 + x} + \frac{1}{2(1 + x)^2}}$$

> *(1 pt for closed form)*

---

**(c)** Find the interval of convergence of the Maclaurin series for $f(x)$.

The Maclaurin series for $f(x)$ is:

$$f(x) = \sum_{n=1}^{\infty} (-1)^{n-1}\,\frac{n(n+1)}{2}\, x^n$$

**Radius of convergence via the Ratio Test:**

$$\left|\frac{a_{n+1}}{a_n}\right| = \frac{(n+1)(n+2)/2}{n(n+1)/2} \cdot |x| = \frac{n+2}{n} \cdot |x|$$

$$\lim_{n \to \infty} \frac{n+2}{n} \cdot |x| = |x|$$

The series converges when $|x| < 1$, so the radius of convergence is $R = 1$.

**Check $x = 1$:** The terms become $(-1)^{n-1}\,\dfrac{n(n+1)}{2}$, and $\dfrac{n(n+1)}{2} \to \infty$. The terms do not approach zero, so the series **diverges**.

**Check $x = -1$:** The terms become $(-1)^{n-1} \cdot (-1)^n \cdot \dfrac{n(n+1)}{2} = -\dfrac{n(n+1)}{2}$, and $\dfrac{n(n+1)}{2} \to \infty$. The terms do not approach zero, so the series **diverges**.

$$\boxed{\text{Interval of convergence: } (-1,\, 1)}$$

> *(2 pts: 1 for radius, 1 for endpoint analysis)*

---

**(d)** Show that the first three nonzero terms of the series for $H(x)$ approximate $H\!\left(\dfrac{1}{3}\right)$ with error less than $\dfrac{1}{100}$.

From part (b), the power series for $H(x)$ is:

$$H(x) = \frac{x^2}{2} - x^3 + \frac{3}{2}x^4 - 2x^5 + \cdots$$

At $x = \dfrac{1}{3}$ (which is inside the interval of convergence), we evaluate the first several terms:

| Term | Value | Sign |
|------|-------|------|
| $\dfrac{(1/3)^2}{2} = \dfrac{1}{18}$ | $\approx 0.0556$ | $+$ |
| $-(1/3)^3 = -\dfrac{1}{27}$ | $\approx -0.0370$ | $-$ |
| $\dfrac{3}{2}(1/3)^4 = \dfrac{1}{54}$ | $\approx 0.0185$ | $+$ |
| $-2(1/3)^5 = -\dfrac{2}{243}$ | $\approx -0.0082$ | $-$ |

**Verification of alternating series conditions at $x = \dfrac{1}{3}$:**

1. **Alternating signs:** The terms alternate in sign: $+, -, +, -, \ldots$ &check;
2. **Decreasing absolute values:** $\dfrac{1}{18} > \dfrac{1}{27} > \dfrac{1}{54} > \dfrac{2}{243} > \cdots$ &check;
3. **Terms approach zero:** $\lim_{n \to \infty} a_n = 0$ &check;

By the **Alternating Series Estimation Theorem**, the error from using the first three nonzero terms is bounded by the absolute value of the **first omitted term** (the fourth term):

$$|\text{error}| \le \left|-2\!\left(\frac{1}{3}\right)^5\right| = \frac{2}{243}$$

Since $\dfrac{2}{243} < \dfrac{1}{100}$ (because $2 \times 100 = 200 < 243$):

$$\boxed{|\text{error}| \le \frac{2}{243} \approx 0.00823 < \frac{1}{100} = 0.01}$$

> *(2 pts: 1 for identifying alternating series bound, 1 for completing the inequality)*

</details>

<details>
<summary><strong>Free Response 5</strong></summary>

**The cross section of Leviathan's observation dome is modeled by the region $R$ in the first quadrant bounded by $y = 4 - x^2$, $y = 0$, and $x = 0$.**

*The parabola $y = 4 - x^2$ intersects $y = 0$ when $x = 2$. So region $R$ is bounded by $x = 0$, $x = 2$, $y = 0$, and $y = 4 - x^2$.*

---

**(a)** Find the area of region $R$.

$$A = \int_0^2 (4 - x^2)\,dx$$

$$= \left[4x - \frac{x^3}{3}\right]_0^2$$

$$= \left(8 - \frac{8}{3}\right) - 0$$

$$= \frac{24}{3} - \frac{8}{3}$$

$$\boxed{A = \frac{16}{3}}$$

> *(2 pts: 1 for integral setup, 1 for evaluation)*

---

**(b)** The dome is formed by revolving $R$ about the $y$-axis. Find the volume of the resulting solid.

**Using the shell method** (integrating with respect to $x$):

$$V = 2\pi \int_0^2 x(4 - x^2)\,dx$$

$$= 2\pi \int_0^2 (4x - x^3)\,dx$$

$$= 2\pi \left[2x^2 - \frac{x^4}{4}\right]_0^2$$

$$= 2\pi \left(8 - \frac{16}{4}\right) = 2\pi\left(8 - 4\right)$$

$$\boxed{V = 8\pi}$$

> *Alternatively, using the disk method (integrating with respect to $y$): Since $y = 4 - x^2 \implies x = \sqrt{4 - y}$, we have $V = \pi\displaystyle\int_0^4 (\sqrt{4 - y})^2\,dy = \pi\int_0^4 (4 - y)\,dy = \pi\left[4y - \frac{y^2}{2}\right]_0^4 = \pi(16 - 8) = 8\pi$. Same result.* *(2 pts: 1 for setup, 1 for evaluation)*

---

**(c)** A reinforced outer shell is formed by revolving $R$ about the line $x = 3$. Set up and evaluate the integral using the shell method.

The shell radius is the distance from a vertical strip at position $x$ to the axis $x = 3$, which is $(3 - x)$. The shell height is $(4 - x^2)$.

$$V = 2\pi \int_0^2 (3 - x)(4 - x^2)\,dx$$

Expand the integrand:

$$(3 - x)(4 - x^2) = 12 - 3x^2 - 4x + x^3$$

Now integrate:

$$V = 2\pi \int_0^2 (12 - 4x - 3x^2 + x^3)\,dx$$

$$= 2\pi \left[12x - 2x^2 - x^3 + \frac{x^4}{4}\right]_0^2$$

$$= 2\pi \left(24 - 8 - 8 + \frac{16}{4}\right)$$

$$= 2\pi \left(24 - 8 - 8 + 4\right)$$

$$= 2\pi(12)$$

$$\boxed{V = 24\pi}$$

> *(3 pts: 1 for shell radius $(3-x)$, 1 for integral setup, 1 for evaluation)*

---

**(d)** Region $R$ is the base of a solid whose cross sections perpendicular to the $x$-axis are semicircles with diameter along $R$ in the $xy$-plane. Find the volume.

At each $x$, the diameter of the semicircle is the height of region $R$:

$$d = 4 - x^2$$

The radius of the semicircle is:

$$r = \frac{4 - x^2}{2}$$

The area of each semicircular cross section is:

$$A(x) = \frac{1}{2}\pi r^2 = \frac{\pi}{2} \cdot \frac{(4 - x^2)^2}{4} = \frac{\pi}{8}(4 - x^2)^2$$

The volume is:

$$V = \int_0^2 \frac{\pi}{8}(4 - x^2)^2\,dx$$

Expand $(4 - x^2)^2 = 16 - 8x^2 + x^4$:

$$V = \frac{\pi}{8}\int_0^2 (16 - 8x^2 + x^4)\,dx$$

$$= \frac{\pi}{8}\left[16x - \frac{8x^3}{3} + \frac{x^5}{5}\right]_0^2$$

$$= \frac{\pi}{8}\left(32 - \frac{64}{3} + \frac{32}{5}\right)$$

Find a common denominator of 15:

$$= \frac{\pi}{8}\left(\frac{480}{15} - \frac{320}{15} + \frac{96}{15}\right)$$

$$= \frac{\pi}{8} \cdot \frac{256}{15}$$

$$\boxed{V = \frac{32\pi}{15}}$$

> *(2 pts: 1 for semicircle area setup, 1 for evaluation)*

</details>

<details>
<summary><strong>Free Response 6</strong></summary>

**After recovery, engineers analyze Leviathan's trajectory through a hydrothermal vent field. The submersible's position at time $t$ minutes ($0 \le t \le 6$) is given by:**

$$x(t) = t^3 - 9t, \qquad y(t) = 2t^2 - 3t$$

---

**(a)** Find the velocity vector and the speed of Leviathan at $t = 1$.

Compute the derivatives:

$$x'(t) = 3t^2 - 9, \qquad y'(t) = 4t - 3$$

At $t = 1$:

$$x'(1) = 3(1)^2 - 9 = 3 - 9 = -6$$

$$y'(1) = 4(1) - 3 = 1$$

$$\boxed{\text{Velocity vector: } \vec{v}(1) = \langle -6,\, 1 \rangle}$$

The speed is the magnitude of the velocity vector:

$$\text{speed} = \|\vec{v}(1)\| = \sqrt{(-6)^2 + 1^2} = \sqrt{36 + 1}$$

$$\boxed{\text{Speed} = \sqrt{37} \text{ units per minute}}$$

> *(2 pts: 1 for velocity vector, 1 for speed)*

---

**(b)** Find $\dfrac{dy}{dx}$ in terms of $t$. For what values of $t$ in $(0, 6)$ is the tangent line horizontal? Vertical?

$$\frac{dy}{dx} = \frac{dy/dt}{dx/dt} = \frac{4t - 3}{3t^2 - 9}$$

$$\boxed{\frac{dy}{dx} = \frac{4t - 3}{3t^2 - 9}}$$

**Horizontal tangent** when $\dfrac{dy}{dt} = 0$ and $\dfrac{dx}{dt} \ne 0$:

$$4t - 3 = 0 \implies t = \frac{3}{4}$$

Check: $x'\!\left(\dfrac{3}{4}\right) = 3\!\left(\dfrac{9}{16}\right) - 9 = \dfrac{27}{16} - 9 = -\dfrac{117}{16} \ne 0$ &check;

$$\boxed{\text{Horizontal tangent at } t = \frac{3}{4}}$$

**Vertical tangent** when $\dfrac{dx}{dt} = 0$ and $\dfrac{dy}{dt} \ne 0$:

$$3t^2 - 9 = 0 \implies t^2 = 3 \implies t = \sqrt{3}$$

(We discard $t = -\sqrt{3}$ since it is not in $(0, 6)$.)

Check: $y'(\sqrt{3}) = 4\sqrt{3} - 3 \approx 3.93 \ne 0$ &check;

$$\boxed{\text{Vertical tangent at } t = \sqrt{3}}$$

> *(3 pts: 1 for dy/dx formula, 1 for horizontal, 1 for vertical)*

---

**(c)** Find $\dfrac{d^2y}{dx^2}$ at $t = 2$. Is the trajectory concave up or concave down?

Using the formula:

$$\frac{d^2y}{dx^2} = \frac{\dfrac{d}{dt}\!\left(\dfrac{dy}{dx}\right)}{\dfrac{dx}{dt}}$$

First, compute $\dfrac{d}{dt}\!\left(\dfrac{dy}{dx}\right)$ using the quotient rule on $\dfrac{4t - 3}{3t^2 - 9}$:

$$\frac{d}{dt}\!\left(\frac{4t - 3}{3t^2 - 9}\right) = \frac{(4)(3t^2 - 9) - (4t - 3)(6t)}{(3t^2 - 9)^2}$$

Expand the numerator:

$$= \frac{12t^2 - 36 - 24t^2 + 18t}{(3t^2 - 9)^2} = \frac{-12t^2 + 18t - 36}{(3t^2 - 9)^2}$$

Factor out $-6$:

$$= \frac{-6(2t^2 - 3t + 6)}{(3t^2 - 9)^2}$$

At $t = 2$:

**Numerator:** $-12(4) + 18(2) - 36 = -48 + 36 - 36 = -48$

**Denominator of the quotient rule:** $(3(4) - 9)^2 = (12 - 9)^2 = 3^2 = 9$

$$\frac{d}{dt}\!\left(\frac{dy}{dx}\right)\bigg|_{t=2} = \frac{-48}{9} = -\frac{16}{3}$$

Also, $x'(2) = 3(4) - 9 = 3$.

Therefore:

$$\frac{d^2y}{dx^2}\bigg|_{t=2} = \frac{-16/3}{3} = -\frac{16}{9}$$

$$\boxed{\frac{d^2y}{dx^2}\bigg|_{t=2} = -\frac{16}{9}}$$

Since $\dfrac{d^2y}{dx^2} < 0$, the trajectory is **concave down** at $t = 2$.

> *(2 pts: 1 for computation, 1 for concavity conclusion with justification)*

---

**(d)** Set up, but do not evaluate, an integral for the total distance traveled from $t = 0$ to $t = 4$.

The total distance traveled is:

$$L = \int_0^4 \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2}\,dt$$

Substituting $x'(t) = 3t^2 - 9$ and $y'(t) = 4t - 3$:

$$(3t^2 - 9)^2 = 9t^4 - 54t^2 + 81$$

$$(4t - 3)^2 = 16t^2 - 24t + 9$$

Adding:

$$(3t^2 - 9)^2 + (4t - 3)^2 = 9t^4 - 38t^2 - 24t + 90$$

$$\boxed{L = \int_0^4 \sqrt{9t^4 - 38t^2 - 24t + 90}\,\,dt}$$

> *(2 pts: 1 for correct integrand, 1 for correct bounds)*

</details>

---

**Score Interpretation**

| Score | Assessment |
|-------|-----------|
| 85–99 | Outstanding — you're ready to ace the AP exam |
| 70–84 | Strong — review a few weak spots |
| 55–69 | Solid — targeted practice on missed topics |
| 40–54 | Developing — revisit core concepts |
| Below 40 | Keep studying — focus on fundamentals first |

*Note: The actual AP exam is scored 1–5. This test has 99 total points (45 MC + 54 FR).*

---

[Back to Practice Test 3](practice-tests/bc-practice-test-3.md)

[Back to Blog Home](/)
