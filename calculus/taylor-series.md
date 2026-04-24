# Taylor and Maclaurin Series
<p class="article-date">April 23, 2026</p>

*You know how when you're at Starbucks and the barista asks what frappe you want, you don't describe the entire molecular composition of the drink? You just say "java chip" and they know exactly what you mean. Taylor series work the same way — they let you describe complicated functions like $e^x$, $\sin x$, and $\ln(1+x)$ using nothing but polynomials. And polynomials are the "java chip frappe" of math: simple, familiar, and easy to work with. The idea is beautiful: at any point $a$, you can build a polynomial that matches the function's value, its slope, its concavity, its rate of change of concavity, and so on — stacking one derivative at a time until the polynomial becomes an increasingly perfect copy of the original function. It's like building a Robotics prototype: start with the chassis (the constant term), add the motor (the first derivative), add the steering (the second derivative), and keep refining until the robot does exactly what the real machine does. This is the crown jewel of BC Calculus — the topic that ties everything together.*

---

## What You'll Learn
- Understand how Taylor polynomials approximate functions by matching derivatives at a center point
- Write the general formula for a Taylor series centered at $x = a$
- Recognize a Maclaurin series as the special case where $a = 0$
- Memorize the six must-know Maclaurin series: $e^x$, $\sin x$, $\cos x$, $\frac{1}{1-x}$, $\ln(1+x)$, $\arctan x$
- Build Taylor polynomials degree by degree ($T_1$, $T_2$, $T_3$, ...)
- Derive Taylor series by computing derivatives at the center
- Create new Taylor series from known series using substitution, differentiation, integration, and multiplication
- Determine the interval of convergence for a Taylor series
- Use Taylor polynomials to approximate function values and definite integrals

---

## Prerequisites
- [Power Series](/calculus/power-series)
- [Higher-Order Derivatives](/calculus/0405-higher-order-derivatives)
- [Tangent Lines](/calculus/0303-tangent-lines)

---

## The Core Concept

### Intuition First

Let's start with something you already know. Back in [Tangent Lines](/calculus/0303-tangent-lines), you learned that a tangent line at a point $x = a$ gives you the best *linear* approximation of a function near that point. The tangent line matches the function's **value** and its **slope** at $a$. Two pieces of information, one straight line.

But a straight line can only do so much. Think about driving with Dad on the winding roads near Lake Hodges. If you're at a particular point on the road and you know your current position and the direction you're heading, you can predict where you'll be in the next instant — that's the tangent line. But roads curve. If you also know *how fast you're turning the wheel* (the second derivative — concavity), you can predict your path even better. Add the rate at which your turning is changing (third derivative), and your prediction improves even more.

That's exactly what Taylor polynomials do. Instead of matching just the value and slope (2 pieces of info), we match the value, the first derivative, the second derivative, the third derivative, and so on — as many derivatives as we want. Each additional derivative adds another term to the polynomial, and each term makes the approximation better.

It's like building a playlist for a road trip to LA. One song gives you the vibe. Five songs give you a solid preview. Twenty songs and you basically *are* the playlist. A Taylor polynomial with more terms is a better "playlist" for the function.

### Building Taylor Polynomials Step by Step

Let's say we want to approximate a function $f(x)$ near $x = a$. We want a polynomial $T_n(x)$ of degree $n$ that matches $f$ and all its derivatives up to the $n$-th at $x = a$.

**Degree 0 (constant approximation):**

$$T_0(x) = f(a)$$

This just matches the function's value. It's flat — a horizontal line.

**Degree 1 (linear approximation — the tangent line):**

$$T_1(x) = f(a) + f'(a)(x - a)$$

Matches the value *and* the slope.

**Degree 2 (quadratic approximation):**

$$T_2(x) = f(a) + f'(a)(x - a) + \frac{f''(a)}{2!}(x - a)^2$$

Matches the value, slope, *and* concavity.

**Degree 3 (cubic approximation):**

$$T_3(x) = f(a) + f'(a)(x - a) + \frac{f''(a)}{2!}(x - a)^2 + \frac{f'''(a)}{3!}(x - a)^3$$

See the pattern? Each new term uses the next derivative, divided by the corresponding factorial, multiplied by $(x - a)$ raised to the matching power.

### The Taylor Series Formula

If we keep going forever — adding infinitely many terms — we get the **Taylor series**:

$$\boxed{f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(x - a)^n = f(a) + f'(a)(x-a) + \frac{f''(a)}{2!}(x-a)^2 + \frac{f'''(a)}{3!}(x-a)^3 + \cdots}$$

Where:
- $f^{(n)}(a)$ is the $n$-th derivative of $f$ evaluated at $x = a$
- $n!$ is $n$ factorial ($0! = 1$, $1! = 1$, $2! = 2$, $3! = 6$, $4! = 24$, etc.)
- $(x - a)^n$ centers the polynomial at $x = a$
- The series equals $f(x)$ wherever it converges

### Maclaurin Series — The Special Case

A **Maclaurin series** is simply a Taylor series centered at $a = 0$:

$$\boxed{f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(0)}{n!}x^n = f(0) + f'(0)x + \frac{f''(0)}{2!}x^2 + \frac{f'''(0)}{3!}x^3 + \cdots}$$

Most of the "famous" series you need to memorize for the AP exam are Maclaurin series (centered at 0), because most common functions have clean derivatives at the origin.

### Why the Factorial?

You might wonder why we divide by $n!$. Here's the key: when you take the $n$-th derivative of $(x - a)^n$, you get $n!$ (by the power rule applied repeatedly). Dividing by $n!$ cancels this out, ensuring that the $n$-th derivative of $T_n(x)$ at $x = a$ exactly equals $f^{(n)}(a)$. The factorial is the "balancing weight" that keeps everything matched.

---

## The Six Must-Memorize Maclaurin Series

These six series appear on virtually every AP BC exam. Memorize them like you memorize your Panda Express order — they need to roll off your tongue automatically.

### 1. $e^x$

$$\boxed{e^x = \sum_{n=0}^{\infty} \frac{x^n}{n!} = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \frac{x^4}{4!} + \cdots}$$

**Converges for:** all real $x$ (interval of convergence: $(-\infty, \infty)$)

**Why it works:** Every derivative of $e^x$ is $e^x$, and $e^0 = 1$. So $f^{(n)}(0) = 1$ for all $n$, giving $\frac{1}{n!}x^n$ for each term.

### 2. $\sin x$

$$\boxed{\sin x = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+1}}{(2n+1)!} = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!} + \cdots}$$

**Converges for:** all real $x$ (interval of convergence: $(-\infty, \infty)$)

**Pattern:** Only odd powers, alternating signs, starting positive.

### 3. $\cos x$

$$\boxed{\cos x = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n}}{(2n)!} = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!} + \cdots}$$

**Converges for:** all real $x$ (interval of convergence: $(-\infty, \infty)$)

**Pattern:** Only even powers, alternating signs, starting positive. Notice this is the derivative of the $\sin x$ series (term by term), as it should be.

### 4. $\frac{1}{1 - x}$ (Geometric Series)

$$\boxed{\frac{1}{1-x} = \sum_{n=0}^{\infty} x^n = 1 + x + x^2 + x^3 + x^4 + \cdots}$$

**Converges for:** $|x| < 1$ (interval of convergence: $(-1, 1)$)

**Why this matters:** This is the geometric series you learned earlier. It's the parent of many other series — substitution, differentiation, and integration of this series generate tons of other useful series.

### 5. $\ln(1 + x)$

$$\boxed{\ln(1+x) = \sum_{n=1}^{\infty} \frac{(-1)^{n+1} x^n}{n} = x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \cdots}$$

**Converges for:** $-1 < x \leq 1$ (interval of convergence: $(-1, 1]$)

**Where it comes from:** Integrate $\frac{1}{1+x} = \frac{1}{1-(-x)} = \sum (-x)^n = \sum (-1)^n x^n$ term by term.

### 6. $\arctan x$

$$\boxed{\arctan x = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+1}}{2n+1} = x - \frac{x^3}{3} + \frac{x^5}{5} - \frac{x^7}{7} + \cdots}$$

**Converges for:** $-1 \leq x \leq 1$ (interval of convergence: $[-1, 1]$)

**Where it comes from:** Integrate $\frac{1}{1+x^2} = \frac{1}{1-(-x^2)} = \sum (-x^2)^n = \sum (-1)^n x^{2n}$ term by term.

### Quick Reference Table

| Function | Maclaurin Series | Interval of Convergence |
|----------|-----------------|------------------------|
| $e^x$ | $\displaystyle\sum_{n=0}^{\infty} \frac{x^n}{n!}$ | $(-\infty, \infty)$ |
| $\sin x$ | $\displaystyle\sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+1}}{(2n+1)!}$ | $(-\infty, \infty)$ |
| $\cos x$ | $\displaystyle\sum_{n=0}^{\infty} \frac{(-1)^n x^{2n}}{(2n)!}$ | $(-\infty, \infty)$ |
| $\frac{1}{1-x}$ | $\displaystyle\sum_{n=0}^{\infty} x^n$ | $(-1, 1)$ |
| $\ln(1+x)$ | $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1} x^n}{n}$ | $(-1, 1]$ |
| $\arctan x$ | $\displaystyle\sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+1}}{2n+1}$ | $[-1, 1]$ |

---

## Worked Examples

### Example 1: Deriving the Maclaurin Series for $e^x$ from Scratch

Let's verify the $e^x$ series by computing derivatives at $a = 0$.

Let $f(x) = e^x$. Find $f^{(n)}(0)$ for each $n$:

| $n$ | $f^{(n)}(x)$ | $f^{(n)}(0)$ |
|-----|-------------|--------------|
| 0 | $e^x$ | $1$ |
| 1 | $e^x$ | $1$ |
| 2 | $e^x$ | $1$ |
| 3 | $e^x$ | $1$ |
| $n$ | $e^x$ | $1$ |

Every derivative of $e^x$ is $e^x$, and $e^0 = 1$. So:

$$e^x = \sum_{n=0}^{\infty} \frac{1}{n!} x^n = 1 + x + \frac{x^2}{2} + \frac{x^3}{6} + \frac{x^4}{24} + \cdots$$

$$\boxed{e^x = \sum_{n=0}^{\infty} \frac{x^n}{n!}}$$

This converges for all $x$ (the ratio test gives $\lim_{n \to \infty} \frac{|x|}{n+1} = 0 < 1$ for any finite $x$).

---

### Example 2: Deriving the Maclaurin Series for $\sin x$

Let $f(x) = \sin x$. Compute successive derivatives at $x = 0$:

| $n$ | $f^{(n)}(x)$ | $f^{(n)}(0)$ |
|-----|-------------|--------------|
| 0 | $\sin x$ | $0$ |
| 1 | $\cos x$ | $1$ |
| 2 | $-\sin x$ | $0$ |
| 3 | $-\cos x$ | $-1$ |
| 4 | $\sin x$ | $0$ |
| 5 | $\cos x$ | $1$ |

The pattern cycles with period 4: $0, 1, 0, -1, 0, 1, 0, -1, \ldots$

Only the **odd** terms survive (the even ones are zero):

$$\sin x = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!} + \cdots$$

$$\boxed{\sin x = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+1}}{(2n+1)!}}$$

**Mnemonic:** "Sine is odd" — it's an odd function, and its series has only odd powers. Similarly, "cosine is even" — only even powers appear in its series.

---

### Example 3: Taylor Series for $\ln x$ Centered at $a = 1$

Not every Taylor series is centered at 0. Let's find the Taylor series for $f(x) = \ln x$ centered at $a = 1$.

Compute derivatives of $\ln x$ and evaluate at $x = 1$:

| $n$ | $f^{(n)}(x)$ | $f^{(n)}(1)$ |
|-----|-------------|--------------|
| 0 | $\ln x$ | $0$ |
| 1 | $\frac{1}{x} = x^{-1}$ | $1$ |
| 2 | $-x^{-2}$ | $-1$ |
| 3 | $2x^{-3}$ | $2$ |
| 4 | $-6x^{-4}$ | $-6$ |
| $n$ ($n \geq 1$) | $\frac{(-1)^{n+1}(n-1)!}{x^n}$ | $(-1)^{n+1}(n-1)!$ |

Plug into the Taylor formula:

$$\ln x = \sum_{n=1}^{\infty} \frac{(-1)^{n+1}(n-1)!}{n!}(x-1)^n = \sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n}(x-1)^n$$

$$\boxed{\ln x = (x-1) - \frac{(x-1)^2}{2} + \frac{(x-1)^3}{3} - \frac{(x-1)^4}{4} + \cdots}$$

**Note:** If you substitute $u = x - 1$ (so $x = 1 + u$), this becomes $\ln(1 + u) = u - \frac{u^2}{2} + \frac{u^3}{3} - \cdots$, which is exactly the Maclaurin series for $\ln(1+u)$. The two forms are the same series, just viewed differently.

**Convergence:** $0 < x \leq 2$ (or equivalently $|x - 1| \leq 1$ with the left endpoint excluded).

---

### Example 4: Taylor Series from Known Series — $e^{-x^2}$ by Substitution

This is the technique you'll use most often on the AP exam: instead of computing derivatives from scratch, **substitute** into a known series.

We know:

$$e^u = 1 + u + \frac{u^2}{2!} + \frac{u^3}{3!} + \cdots$$

Substitute $u = -x^2$:

$$e^{-x^2} = 1 + (-x^2) + \frac{(-x^2)^2}{2!} + \frac{(-x^2)^3}{3!} + \frac{(-x^2)^4}{4!} + \cdots$$

$$= 1 - x^2 + \frac{x^4}{2!} - \frac{x^6}{3!} + \frac{x^8}{4!} - \cdots$$

$$\boxed{e^{-x^2} = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n}}{n!}}$$

**Converges for:** all real $x$ (since $e^u$ converges everywhere, and $u = -x^2$ is defined for all $x$).

**Why this matters:** The function $e^{-x^2}$ has no elementary antiderivative — you literally cannot write $\int e^{-x^2}\,dx$ using any combination of basic functions. But you *can* integrate the Taylor series term by term. This is one of the most powerful applications of Taylor series, and the AP exam loves it.

---

### Example 5: Finding a Maclaurin Series by Differentiation of a Known Series

Find the Maclaurin series for $\frac{1}{(1-x)^2}$.

Start with the known geometric series:

$$\frac{1}{1-x} = \sum_{n=0}^{\infty} x^n = 1 + x + x^2 + x^3 + \cdots$$

Differentiate both sides with respect to $x$:

$$\frac{d}{dx}\left[\frac{1}{1-x}\right] = \frac{1}{(1-x)^2}$$

$$\frac{d}{dx}\left[\sum_{n=0}^{\infty} x^n\right] = \sum_{n=1}^{\infty} nx^{n-1} = 1 + 2x + 3x^2 + 4x^3 + \cdots$$

Therefore:

$$\boxed{\frac{1}{(1-x)^2} = \sum_{n=1}^{\infty} nx^{n-1} = \sum_{n=0}^{\infty} (n+1)x^n, \quad |x| < 1}$$

The interval of convergence stays the same: $|x| < 1$. (Differentiating a power series doesn't change the radius of convergence, though you may need to re-check endpoints.)

---

### Example 6: Finding a Maclaurin Series by Integration of a Known Series

Find the Maclaurin series for $\arctan x$ using the geometric series.

Start with:

$$\frac{1}{1-u} = \sum_{n=0}^{\infty} u^n$$

Substitute $u = -x^2$:

$$\frac{1}{1+x^2} = \sum_{n=0}^{\infty} (-x^2)^n = \sum_{n=0}^{\infty} (-1)^n x^{2n} = 1 - x^2 + x^4 - x^6 + \cdots$$

Now integrate both sides from $0$ to $x$:

$$\int_0^x \frac{1}{1+t^2}\,dt = \arctan x$$

$$\int_0^x \sum_{n=0}^{\infty} (-1)^n t^{2n}\,dt = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{2n+1}$$

Therefore:

$$\boxed{\arctan x = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+1}}{2n+1} = x - \frac{x^3}{3} + \frac{x^5}{5} - \frac{x^7}{7} + \cdots}$$

**Converges for:** $|x| \leq 1$ (including both endpoints).

**Fun fact:** Plugging in $x = 1$ gives $\arctan(1) = \frac{\pi}{4}$, so:

$$\frac{\pi}{4} = 1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + \cdots$$

This is the **Leibniz formula for $\pi$** — you can compute $\pi$ using nothing but fractions. (It converges very slowly though, so don't try to get 10 decimal places this way.)

---

### Example 7: Taylor Series by Multiplication — $x^2 \sin x$

Find the Maclaurin series for $x^2 \sin x$.

This one's simple — just multiply the known $\sin x$ series by $x^2$:

$$\sin x = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!} + \cdots$$

$$x^2 \sin x = x^2 \left(x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!} + \cdots\right)$$

$$= x^3 - \frac{x^5}{3!} + \frac{x^7}{5!} - \frac{x^9}{7!} + \cdots$$

$$\boxed{x^2 \sin x = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+3}}{(2n+1)!}}$$

**Converges for:** all real $x$ (same as $\sin x$).

Multiplication by a polynomial never changes the radius of convergence — it just shifts the powers.

---

### Example 8: Using Taylor Series to Approximate an Integral

Approximate $\displaystyle\int_0^{1} e^{-x^2}\,dx$ using the first four non-zero terms of the Maclaurin series.

From Example 4:

$$e^{-x^2} = 1 - x^2 + \frac{x^4}{2!} - \frac{x^6}{3!} + \cdots$$

Integrate term by term from 0 to 1:

$$\int_0^1 e^{-x^2}\,dx \approx \int_0^1 \left(1 - x^2 + \frac{x^4}{2} - \frac{x^6}{6}\right)\,dx$$

$$= \left[x - \frac{x^3}{3} + \frac{x^5}{10} - \frac{x^7}{42}\right]_0^1$$

$$= 1 - \frac{1}{3} + \frac{1}{10} - \frac{1}{42}$$

$$= \frac{210 - 70 + 21 - 5}{210} = \frac{156}{210} = \frac{26}{35}$$

$$\boxed{\int_0^1 e^{-x^2}\,dx \approx \frac{26}{35} \approx 0.7429}$$

(The actual value is approximately $0.7468$, so four terms already gives us two decimal places of accuracy.)

This is a *huge* deal. The function $e^{-x^2}$ has no antiderivative you can write with elementary functions — it's related to the "error function" in statistics, which shows up everywhere in science and engineering. Taylor series let you compute its integral to any desired accuracy.

---

### Example 9: Finding the Taylor Series for $\cos(x^2)$ by Substitution

Find the Maclaurin series for $\cos(x^2)$.

We know:

$$\cos u = 1 - \frac{u^2}{2!} + \frac{u^4}{4!} - \frac{u^6}{6!} + \cdots$$

Substitute $u = x^2$:

$$\cos(x^2) = 1 - \frac{(x^2)^2}{2!} + \frac{(x^2)^4}{4!} - \frac{(x^2)^6}{6!} + \cdots$$

$$= 1 - \frac{x^4}{2!} + \frac{x^8}{4!} - \frac{x^{12}}{6!} + \cdots$$

$$\boxed{\cos(x^2) = \sum_{n=0}^{\infty} \frac{(-1)^n x^{4n}}{(2n)!}}$$

**Converges for:** all real $x$.

---

### Example 10: Taylor Series Centered at $a = \pi/2$ for $\cos x$

Find the Taylor series for $f(x) = \cos x$ centered at $a = \frac{\pi}{2}$.

Compute derivatives at $x = \frac{\pi}{2}$:

| $n$ | $f^{(n)}(x)$ | $f^{(n)}\!\left(\frac{\pi}{2}\right)$ |
|-----|-------------|--------------------------------------|
| 0 | $\cos x$ | $0$ |
| 1 | $-\sin x$ | $-1$ |
| 2 | $-\cos x$ | $0$ |
| 3 | $\sin x$ | $1$ |
| 4 | $\cos x$ | $0$ |
| 5 | $-\sin x$ | $-1$ |

The pattern cycles: $0, -1, 0, 1, 0, -1, 0, 1, \ldots$

Only odd-indexed terms are non-zero:

$$\cos x = -\left(x - \frac{\pi}{2}\right) + \frac{1}{3!}\left(x - \frac{\pi}{2}\right)^3 - \frac{1}{5!}\left(x - \frac{\pi}{2}\right)^5 + \cdots$$

$$\boxed{\cos x = \sum_{n=0}^{\infty} \frac{(-1)^{n+1}}{(2n+1)!}\left(x - \frac{\pi}{2}\right)^{2n+1}}$$

Notice something cool: this is exactly $-\sin\!\left(x - \frac{\pi}{2}\right)$, which makes sense because $\cos x = -\sin\!\left(x - \frac{\pi}{2}\right)$ is a trig identity. The Taylor series "knows" the identity.

---

## Key Formulas & Rules

| Formula / Concept | Description |
|-------------------|-------------|
| $\displaystyle f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(x-a)^n$ | Taylor series centered at $x = a$ |
| $\displaystyle f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(0)}{n!}x^n$ | Maclaurin series (Taylor with $a = 0$) |
| $T_n(x) = \displaystyle\sum_{k=0}^{n} \frac{f^{(k)}(a)}{k!}(x-a)^k$ | Taylor polynomial of degree $n$ (partial sum) |
| $c_n = \frac{f^{(n)}(a)}{n!}$ | The $n$-th coefficient of a Taylor series |
| $f^{(n)}(a) = n! \cdot c_n$ | Recovering the $n$-th derivative from the coefficient |
| Substitution | Replace $x$ with $g(x)$ in a known series |
| Term-by-term differentiation | $\frac{d}{dx}\left[\sum c_n x^n\right] = \sum n \cdot c_n x^{n-1}$ |
| Term-by-term integration | $\int \sum c_n x^n\,dx = C + \sum \frac{c_n x^{n+1}}{n+1}$ |
| Radius stays the same | Differentiation and integration preserve the radius of convergence |

---

## Common Mistakes to Avoid

### Mistake 1: Confusing the General Term Index

**Wrong:** Writing $\sin x = \sum_{n=0}^{\infty} \frac{(-1)^n x^n}{n!}$ (that's $e^{-x}$, not $\sin x$).

**Right:** $\sin x$ has only **odd powers**: $\sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+1}}{(2n+1)!}$. The exponent on $x$ and the factorial in the denominator must match, and for sine they're both $2n+1$.

**Tip:** When in doubt, write out the first three or four terms and compare to the series you memorized. If they match, your general term is correct.

---

### Mistake 2: Forgetting to Adjust the Interval of Convergence After Substitution

When you substitute $u = -x^2$ into the geometric series $\frac{1}{1-u} = \sum u^n$ (which converges for $|u| < 1$), the new convergence condition is:

$$|-x^2| < 1 \implies x^2 < 1 \implies |x| < 1$$

**Wrong:** Saying $e^{-x^2} = \sum \frac{(-1)^n x^{2n}}{n!}$ converges for $|x| < 1$. (It actually converges for all $x$, because $e^u$ converges everywhere.)

**Right:** The interval of convergence depends on the *original* series, not just the substitution mechanically. For $e^u$, the original converges for all $u$, so $e^{-x^2}$ converges for all $x$. For $\frac{1}{1-u}$, the original converges for $|u| < 1$, so $\frac{1}{1+x^2}$ converges for $|x| < 1$.

---

### Mistake 3: Wrong Factorial in the Denominator

**Wrong:** For $\cos x$, writing $\frac{(-1)^n x^{2n}}{n!}$ instead of $\frac{(-1)^n x^{2n}}{(2n)!}$.

The factorial must match the power of $x$. If the power is $2n$, the factorial is $(2n)!$, not $n!$.

**Tip:** The series for $e^x$ is the only one where the power is $n$ and the factorial is $n!$. For $\sin$ and $\cos$, the factorial always matches the power exactly.

---

### Mistake 4: Forgetting That Taylor Coefficients Give You Derivatives

A common AP free-response question gives you a Taylor series and asks for a specific derivative. Remember:

$$\text{If } f(x) = \sum c_n(x - a)^n, \text{ then } f^{(n)}(a) = n! \cdot c_n$$

**Example:** If the coefficient of $(x-3)^4$ in the Taylor series for $f$ centered at $a = 3$ is $\frac{7}{2}$, then:

$$f^{(4)}(3) = 4! \cdot \frac{7}{2} = 24 \cdot \frac{7}{2} = 84$$

Students frequently forget to multiply by $n!$.

---

### Mistake 5: Not Centering at the Right Point

When building a Taylor series centered at $a = 2$, every factor must be $(x - 2)^n$, and every derivative must be evaluated at $x = 2$.

**Wrong:** Computing $f'(0)$ for a Taylor series centered at $a = 2$.

**Right:** Compute $f'(2)$, $f''(2)$, $f'''(2)$, etc.

---

## AP Exam Tips

### For BC Students:

1. **Taylor and Maclaurin series appear on every BC exam.** Expect at least one free-response question and 3-5 multiple-choice questions on this topic. It is the most heavily tested BC-only topic.

2. **Memorize the six Maclaurin series cold.** You should be able to write $e^x$, $\sin x$, $\cos x$, $\frac{1}{1-x}$, $\ln(1+x)$, and $\arctan x$ from memory in under 30 seconds total. Practice writing them on flashcards until they're automatic — like knowing your Ding Tea order without looking at the menu.

3. **Substitution is your fastest tool.** Most AP problems don't require computing derivatives from scratch. Instead, they ask for the Maclaurin series of something like $e^{-3x}$, $\sin(2x)$, or $\frac{1}{1+x^3}$ — all of which are quick substitutions into known series. Learn to recognize these instantly.

4. **"Find the first four non-zero terms" is the most common phrasing.** When a problem says this, write out terms until you have exactly four that aren't zero. For $\sin x$, the first four non-zero terms are $x - \frac{x^3}{6} + \frac{x^5}{120} - \frac{x^7}{5040}$.

5. **Know how to extract derivatives from series.** If a problem gives you a Taylor series and asks for $f^{(5)}(0)$, find the coefficient of $x^5$ and multiply by $5!$. This is worth easy points.

6. **Integrating series is a key skill.** Problems like "approximate $\int_0^{0.5} \sin(x^2)\,dx$" require you to: (a) write the series for $\sin(x^2)$, (b) integrate term by term, (c) evaluate the definite integral. Practice this workflow.

7. **Taylor polynomials vs. Taylor series.** A Taylor polynomial $T_n(x)$ has finitely many terms (degree $n$). A Taylor series has infinitely many. The AP exam may ask for either. Read carefully.

8. **The coefficient pattern reveals the function.** If a free-response gives you $f(0) = 3$, $f'(0) = -1$, $f''(0) = 4$, $f'''(0) = -12$, they're basically asking you to build the Taylor polynomial $T_3(x) = 3 - x + 2x^2 - 2x^3$. Don't overthink it — just plug into the formula.

---

## Practice Problems

### Basic (Problems 1-5)

**1.** Write the first four non-zero terms of the Maclaurin series for $e^{-x}$.

---

**2.** Write the first four non-zero terms of the Maclaurin series for $\sin(2x)$.

---

**3.** Write the Maclaurin series for $\frac{1}{1+x}$ in sigma notation and state the interval of convergence.

---

**4.** Find the Maclaurin polynomial of degree 3 (i.e., $T_3(x)$) for $f(x) = \cos x$.

---

**5.** The Maclaurin series for a function $f$ is $f(x) = 2 + 3x + \frac{5}{2}x^2 + \frac{7}{6}x^3 + \cdots$. Find $f(0)$, $f'(0)$, $f''(0)$, and $f'''(0)$.

---

### Intermediate (Problems 6-10)

**6.** Find the Maclaurin series for $e^{3x}$ in sigma notation. State the interval of convergence.

---

**7.** Find the first four non-zero terms of the Maclaurin series for $\ln(1 + x^2)$.

---

**8.** Find the first four non-zero terms of the Maclaurin series for $x \cos(x^2)$.

---

**9.** Find the Taylor series for $e^x$ centered at $a = 1$. Write the first four terms and the general term.

---

**10.** Use the Maclaurin series for $\cos x$ to find the Maclaurin series for $\frac{1 - \cos x}{x^2}$. State the first three non-zero terms.

---

### Advanced (Problems 11-15)

**11.** Find the Maclaurin series for $\frac{x}{1 + x^3}$ in sigma notation and state the interval of convergence.

---

**12.** Use the Taylor series to approximate $\displaystyle\int_0^{0.5} \frac{\sin x}{x}\,dx$ using the first three non-zero terms.

---

**13.** Find the first four non-zero terms of the Taylor series for $\sqrt{x}$ centered at $a = 4$.

---

**14.** Find the Maclaurin series for $\frac{\arctan x}{x}$ and use it to evaluate $\displaystyle\sum_{n=0}^{\infty} \frac{(-1)^n}{(2n+1) \cdot 3^{2n+1}}$.

---

**15.** Find the first three non-zero terms of the Maclaurin series for $e^x \sin x$.

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

The coefficient of $x^5$ in the Maclaurin series for $f(x) = x^2 e^{-x}$ is

| Choice | Answer |
|--------|--------|
| **(A)** | $-\frac{1}{6}$ |
| **(B)** | $\frac{1}{6}$ |
| **(C)** | $-\frac{1}{3}$ |
| **(D)** | $\frac{1}{120}$ |

---

#### Problem 17 (Multiple Choice)

The Maclaurin series for $\ln(1 + x)$ is $x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \cdots$. What is $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n \cdot 2^n}$?

| Choice | Answer |
|--------|--------|
| **(A)** | $\ln 2$ |
| **(B)** | $\ln\!\left(\frac{3}{2}\right)$ |
| **(C)** | $\ln\!\left(\frac{1}{2}\right)$ |
| **(D)** | $\ln 3$ |

---

#### Problem 18 (Free Response)

Let $f$ be the function defined by $f(x) = e^{-x^2/2}$.

> **(a)** Write the first four non-zero terms and the general term of the Maclaurin series for $f(x)$.
>
> **(b)** Use the series from part (a) to write the first four non-zero terms and the general term of the Maclaurin series for $f'(x)$.
>
> **(c)** Use the series from part (a) to approximate $\displaystyle\int_0^1 e^{-x^2/2}\,dx$ using the first three non-zero terms. Express your answer as a fraction.
>
> **(d)** The Maclaurin series for $f$ converges for all $x$. Does the approximation in part (c) overestimate or underestimate the actual value of the integral? Justify your answer.

---

#### Problem 19 (Multiple Choice)

If $f(x) = \displaystyle\sum_{n=0}^{\infty} \frac{(x - 2)^n}{3^n}$, then $f(x) =$

| Choice | Answer |
|--------|--------|
| **(A)** | $\frac{3}{5 - x}$ |
| **(B)** | $\frac{1}{3 - x}$ |
| **(C)** | $\frac{1}{1 - x}$ |
| **(D)** | $\frac{3}{1 - x}$ |

---

#### Problem 20 (Free Response — Challenging)

Ganga is on the Robotics team and is programming a motor controller. The controller uses the function $\sin x$ internally, but the microprocessor can only perform addition, subtraction, and multiplication (no trig functions available). She decides to program a Taylor polynomial approximation instead.

> **(a)** Write the 5th-degree Maclaurin polynomial $T_5(x)$ for $\sin x$.
>
> **(b)** Use $T_5(x)$ to approximate $\sin(0.3)$. Show your work and express the answer to 6 decimal places.
>
> **(c)** The actual value of $\sin(0.3)$ is $0.295520...$. What is the absolute error of the approximation in part (b)? Is the approximation an overestimate or underestimate? Use the alternating series estimation theorem to justify your answer.
>
> **(d)** Ganga's mentor says the controller needs the approximation to be accurate to within $10^{-7}$ for inputs in $[-\pi, \pi]$. What is the minimum degree of the Maclaurin polynomial she should use? Justify your answer using the first omitted term of the alternating series.

---

## Answer Key

<details>
<summary><strong>Problem 1 Solution</strong></summary>

**Write the first four non-zero terms of the Maclaurin series for $e^{-x}$.**

Start with $e^u = 1 + u + \frac{u^2}{2!} + \frac{u^3}{3!} + \cdots$ and substitute $u = -x$:

$$e^{-x} = 1 + (-x) + \frac{(-x)^2}{2!} + \frac{(-x)^3}{3!} + \cdots$$

$$\boxed{e^{-x} = 1 - x + \frac{x^2}{2} - \frac{x^3}{6} + \cdots}$$

</details>

---

<details>
<summary><strong>Problem 2 Solution</strong></summary>

**Write the first four non-zero terms of the Maclaurin series for $\sin(2x)$.**

Start with $\sin u = u - \frac{u^3}{3!} + \frac{u^5}{5!} - \frac{u^7}{7!} + \cdots$ and substitute $u = 2x$:

$$\sin(2x) = 2x - \frac{(2x)^3}{3!} + \frac{(2x)^5}{5!} - \frac{(2x)^7}{7!} + \cdots$$

$$= 2x - \frac{8x^3}{6} + \frac{32x^5}{120} - \frac{128x^7}{5040} + \cdots$$

$$\boxed{\sin(2x) = 2x - \frac{4x^3}{3} + \frac{4x^5}{15} - \frac{8x^7}{315} + \cdots}$$

</details>

---

<details>
<summary><strong>Problem 3 Solution</strong></summary>

**Write the Maclaurin series for $\frac{1}{1+x}$ and state the interval of convergence.**

Start with $\frac{1}{1-u} = \sum_{n=0}^{\infty} u^n$ and substitute $u = -x$:

$$\frac{1}{1+x} = \frac{1}{1-(-x)} = \sum_{n=0}^{\infty} (-x)^n = \sum_{n=0}^{\infty} (-1)^n x^n$$

$$= 1 - x + x^2 - x^3 + x^4 - \cdots$$

**Interval of convergence:** The geometric series converges when $|-x| < 1$, i.e., $|x| < 1$.

$$\boxed{\frac{1}{1+x} = \sum_{n=0}^{\infty} (-1)^n x^n, \quad |x| < 1}$$

</details>

---

<details>
<summary><strong>Problem 4 Solution</strong></summary>

**Find $T_3(x)$ for $f(x) = \cos x$.**

From the Maclaurin series $\cos x = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \cdots$, the degree 3 polynomial uses all terms with power $\leq 3$:

$$T_3(x) = 1 - \frac{x^2}{2}$$

Note: There is no $x^3$ term (the coefficient of $x^3$ in the cosine series is 0), so $T_3(x) = T_2(x)$.

$$\boxed{T_3(x) = 1 - \frac{x^2}{2}}$$

</details>

---

<details>
<summary><strong>Problem 5 Solution</strong></summary>

**Given $f(x) = 2 + 3x + \frac{5}{2}x^2 + \frac{7}{6}x^3 + \cdots$, find $f(0)$, $f'(0)$, $f''(0)$, and $f'''(0)$.**

The Maclaurin series has the form $f(x) = \sum \frac{f^{(n)}(0)}{n!} x^n$, so:

- The constant term is $f(0) = 2$, so $\boxed{f(0) = 2}$.

- The coefficient of $x$ is $\frac{f'(0)}{1!} = 3$, so $\boxed{f'(0) = 3}$.

- The coefficient of $x^2$ is $\frac{f''(0)}{2!} = \frac{5}{2}$, so $f''(0) = 2! \cdot \frac{5}{2} = 2 \cdot \frac{5}{2} = \boxed{f''(0) = 5}$.

- The coefficient of $x^3$ is $\frac{f'''(0)}{3!} = \frac{7}{6}$, so $f'''(0) = 3! \cdot \frac{7}{6} = 6 \cdot \frac{7}{6} = \boxed{f'''(0) = 7}$.

</details>

---

<details>
<summary><strong>Problem 6 Solution</strong></summary>

**Find the Maclaurin series for $e^{3x}$ in sigma notation.**

Substitute $u = 3x$ into $e^u = \sum_{n=0}^{\infty} \frac{u^n}{n!}$:

$$e^{3x} = \sum_{n=0}^{\infty} \frac{(3x)^n}{n!} = \sum_{n=0}^{\infty} \frac{3^n x^n}{n!}$$

$$= 1 + 3x + \frac{9x^2}{2} + \frac{27x^3}{6} + \cdots$$

**Interval of convergence:** $(-\infty, \infty)$ (since $e^u$ converges for all $u$, and $u = 3x$ is defined for all $x$).

$$\boxed{e^{3x} = \sum_{n=0}^{\infty} \frac{3^n x^n}{n!}, \quad (-\infty, \infty)}$$

</details>

---

<details>
<summary><strong>Problem 7 Solution</strong></summary>

**Find the first four non-zero terms of the Maclaurin series for $\ln(1 + x^2)$.**

Start with $\ln(1 + u) = u - \frac{u^2}{2} + \frac{u^3}{3} - \frac{u^4}{4} + \cdots$ and substitute $u = x^2$:

$$\ln(1 + x^2) = x^2 - \frac{(x^2)^2}{2} + \frac{(x^2)^3}{3} - \frac{(x^2)^4}{4} + \cdots$$

$$\boxed{\ln(1 + x^2) = x^2 - \frac{x^4}{2} + \frac{x^6}{3} - \frac{x^8}{4} + \cdots}$$

**Interval of convergence:** $|x^2| \leq 1$, so $|x| \leq 1$.

</details>

---

<details>
<summary><strong>Problem 8 Solution</strong></summary>

**Find the first four non-zero terms of the Maclaurin series for $x\cos(x^2)$.**

First, find $\cos(x^2)$ by substituting $u = x^2$ into $\cos u$:

$$\cos(x^2) = 1 - \frac{x^4}{2!} + \frac{x^8}{4!} - \frac{x^{12}}{6!} + \cdots$$

Now multiply by $x$:

$$x\cos(x^2) = x - \frac{x^5}{2!} + \frac{x^9}{4!} - \frac{x^{13}}{6!} + \cdots$$

$$\boxed{x\cos(x^2) = x - \frac{x^5}{2} + \frac{x^9}{24} - \frac{x^{13}}{720} + \cdots}$$

</details>

---

<details>
<summary><strong>Problem 9 Solution</strong></summary>

**Find the Taylor series for $e^x$ centered at $a = 1$.**

Compute $f^{(n)}(1)$ for $f(x) = e^x$: every derivative of $e^x$ is $e^x$, so $f^{(n)}(1) = e$ for all $n$.

$$e^x = \sum_{n=0}^{\infty} \frac{e}{n!}(x-1)^n = e \sum_{n=0}^{\infty} \frac{(x-1)^n}{n!}$$

**First four terms:**

$$e^x = e + e(x-1) + \frac{e}{2}(x-1)^2 + \frac{e}{6}(x-1)^3 + \cdots$$

$$\boxed{e^x = \sum_{n=0}^{\infty} \frac{e}{n!}(x - 1)^n}$$

**Note:** This is just $e \cdot e^{(x-1)} = e^{1} \cdot e^{x-1} = e^x$. The factors of $e$ out front come from evaluating derivatives at $x = 1$ instead of $x = 0$.

</details>

---

<details>
<summary><strong>Problem 10 Solution</strong></summary>

**Find the Maclaurin series for $\frac{1 - \cos x}{x^2}$.**

Start with the Maclaurin series for $\cos x$:

$$\cos x = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!} + \cdots$$

So:

$$1 - \cos x = \frac{x^2}{2!} - \frac{x^4}{4!} + \frac{x^6}{6!} - \cdots$$

Divide by $x^2$:

$$\frac{1 - \cos x}{x^2} = \frac{1}{2!} - \frac{x^2}{4!} + \frac{x^4}{6!} - \cdots$$

$$\boxed{\frac{1 - \cos x}{x^2} = \frac{1}{2} - \frac{x^2}{24} + \frac{x^4}{720} - \cdots}$$

**Interesting:** $\lim_{x \to 0} \frac{1 - \cos x}{x^2} = \frac{1}{2}$, which you can read directly from the series (it's the constant term). This is way easier than applying L'Hopital's rule twice.

</details>

---

<details>
<summary><strong>Problem 11 Solution</strong></summary>

**Find the Maclaurin series for $\frac{x}{1 + x^3}$ in sigma notation.**

Start with $\frac{1}{1-u} = \sum_{n=0}^{\infty} u^n$ and substitute $u = -x^3$:

$$\frac{1}{1 + x^3} = \frac{1}{1 - (-x^3)} = \sum_{n=0}^{\infty} (-x^3)^n = \sum_{n=0}^{\infty} (-1)^n x^{3n}$$

Multiply by $x$:

$$\frac{x}{1 + x^3} = \sum_{n=0}^{\infty} (-1)^n x^{3n+1}$$

$$= x - x^4 + x^7 - x^{10} + \cdots$$

**Interval of convergence:** $|-x^3| < 1 \implies |x| < 1$.

$$\boxed{\frac{x}{1+x^3} = \sum_{n=0}^{\infty} (-1)^n x^{3n+1}, \quad |x| < 1}$$

</details>

---

<details>
<summary><strong>Problem 12 Solution</strong></summary>

**Approximate $\displaystyle\int_0^{0.5} \frac{\sin x}{x}\,dx$ using the first three non-zero terms.**

Start with the Maclaurin series for $\sin x$:

$$\sin x = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!} + \cdots$$

Divide by $x$:

$$\frac{\sin x}{x} = 1 - \frac{x^2}{3!} + \frac{x^4}{5!} - \frac{x^6}{7!} + \cdots = 1 - \frac{x^2}{6} + \frac{x^4}{120} - \cdots$$

Integrate term by term from 0 to 0.5:

$$\int_0^{0.5} \frac{\sin x}{x}\,dx \approx \int_0^{0.5}\left(1 - \frac{x^2}{6} + \frac{x^4}{120}\right)\,dx$$

$$= \left[x - \frac{x^3}{18} + \frac{x^5}{600}\right]_0^{0.5}$$

$$= 0.5 - \frac{(0.5)^3}{18} + \frac{(0.5)^5}{600}$$

$$= 0.5 - \frac{0.125}{18} + \frac{0.03125}{600}$$

$$= 0.5 - 0.006944\overline{4} + 0.0000520\overline{8}$$

$$\boxed{\int_0^{0.5} \frac{\sin x}{x}\,dx \approx 0.49311 \approx \frac{4441}{9009}}$$

(The exact answer using three terms is $\frac{1}{2} - \frac{1}{144} + \frac{1}{19200} = \frac{4441}{9009} \approx 0.493108$.)

</details>

---

<details>
<summary><strong>Problem 13 Solution</strong></summary>

**Find the first four non-zero terms of the Taylor series for $\sqrt{x}$ centered at $a = 4$.**

Let $f(x) = x^{1/2}$. Compute derivatives at $x = 4$:

| $n$ | $f^{(n)}(x)$ | $f^{(n)}(4)$ |
|-----|-------------|--------------|
| 0 | $x^{1/2}$ | $2$ |
| 1 | $\frac{1}{2}x^{-1/2}$ | $\frac{1}{4}$ |
| 2 | $-\frac{1}{4}x^{-3/2}$ | $-\frac{1}{32}$ |
| 3 | $\frac{3}{8}x^{-5/2}$ | $\frac{3}{256}$ |

Apply the Taylor formula:

$$\sqrt{x} = f(4) + f'(4)(x-4) + \frac{f''(4)}{2!}(x-4)^2 + \frac{f'''(4)}{3!}(x-4)^3 + \cdots$$

$$= 2 + \frac{1}{4}(x-4) + \frac{-1/32}{2}(x-4)^2 + \frac{3/256}{6}(x-4)^3 + \cdots$$

$$\boxed{\sqrt{x} = 2 + \frac{1}{4}(x-4) - \frac{1}{64}(x-4)^2 + \frac{1}{512}(x-4)^3 - \cdots}$$

**Quick check:** At $x = 4$: $\sqrt{4} = 2$. The series gives $2 + 0 + 0 + 0 = 2$. Correct.

</details>

---

<details>
<summary><strong>Problem 14 Solution</strong></summary>

**Find the Maclaurin series for $\frac{\arctan x}{x}$ and evaluate $\displaystyle\sum_{n=0}^{\infty} \frac{(-1)^n}{(2n+1) \cdot 3^{2n+1}}$.**

We know:

$$\arctan x = x - \frac{x^3}{3} + \frac{x^5}{5} - \frac{x^7}{7} + \cdots = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+1}}{2n+1}$$

Divide by $x$:

$$\frac{\arctan x}{x} = 1 - \frac{x^2}{3} + \frac{x^4}{5} - \frac{x^6}{7} + \cdots = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n}}{2n+1}$$

Now look at the given sum:

$$\sum_{n=0}^{\infty} \frac{(-1)^n}{(2n+1) \cdot 3^{2n+1}} = \frac{1}{3}\sum_{n=0}^{\infty} \frac{(-1)^n}{(2n+1) \cdot 3^{2n}} = \frac{1}{3}\sum_{n=0}^{\infty} \frac{(-1)^n \left(\frac{1}{3}\right)^{2n}}{2n+1}$$

This is $\frac{1}{3} \cdot \frac{\arctan(1/3)}{1/3} = \frac{\arctan(1/3)}{1} = \arctan\!\left(\frac{1}{3}\right)$.

Wait — let's be more careful. The original $\arctan$ series is:

$$\arctan x = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+1}}{2n+1}$$

Substitute $x = \frac{1}{3}$:

$$\arctan\!\left(\frac{1}{3}\right) = \sum_{n=0}^{\infty} \frac{(-1)^n}{(2n+1) \cdot 3^{2n+1}}$$

$$\boxed{\sum_{n=0}^{\infty} \frac{(-1)^n}{(2n+1) \cdot 3^{2n+1}} = \arctan\!\left(\frac{1}{3}\right)}$$

</details>

---

<details>
<summary><strong>Problem 15 Solution</strong></summary>

**Find the first three non-zero terms of the Maclaurin series for $e^x \sin x$.**

Multiply the two known series:

$$e^x = 1 + x + \frac{x^2}{2} + \frac{x^3}{6} + \frac{x^4}{24} + \cdots$$

$$\sin x = x + 0 \cdot x^2 - \frac{x^3}{6} + 0 \cdot x^4 + \frac{x^5}{120} + \cdots$$

We need to multiply and collect terms up to the smallest powers. Let's carefully compute:

**$x^1$ terms:** $1 \cdot x = x$

**$x^2$ terms:** $x \cdot x = x^2$

**$x^3$ terms:** $\frac{x^2}{2} \cdot x + 1 \cdot \left(-\frac{x^3}{6}\right) = \frac{x^3}{2} - \frac{x^3}{6} = \frac{x^3}{3}$

So the first three non-zero terms are:

$$\boxed{e^x \sin x = x + x^2 + \frac{x^3}{3} - \cdots}$$

**Verification:** We can also get this from the formula $e^x \sin x = \text{Im}(e^{(1+i)x})$, but the multiplication method is what the AP exam expects.

</details>

---

<details>
<summary><strong>Problem 16 Solution</strong></summary>

**Answer: (A)** $-\frac{1}{6}$

The Maclaurin series for $e^{-x}$ is:

$$e^{-x} = \sum_{n=0}^{\infty} \frac{(-1)^n x^n}{n!} = 1 - x + \frac{x^2}{2} - \frac{x^3}{6} + \frac{x^4}{24} - \cdots$$

Multiply by $x^2$:

$$x^2 e^{-x} = x^2 - x^3 + \frac{x^4}{2} - \frac{x^5}{6} + \frac{x^6}{24} - \cdots$$

The coefficient of $x^5$ comes from the $\frac{(-1)^3 x^3}{3!} = -\frac{x^3}{6}$ term of $e^{-x}$, multiplied by $x^2$:

$$\text{coefficient of } x^5 = \frac{(-1)^3}{3!} = -\frac{1}{6}$$

This matches **(A)**.

</details>

---

<details>
<summary><strong>Problem 17 Solution</strong></summary>

**Answer: (B)** $\ln\!\left(\frac{3}{2}\right)$

The Maclaurin series for $\ln(1+x)$ is:

$$\ln(1+x) = \sum_{n=1}^{\infty} \frac{(-1)^{n+1} x^n}{n} = x - \frac{x^2}{2} + \frac{x^3}{3} - \cdots$$

Substitute $x = \frac{1}{2}$:

$$\ln\!\left(1 + \frac{1}{2}\right) = \sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n \cdot 2^n}$$

$$\ln\!\left(\frac{3}{2}\right) = \sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n \cdot 2^n}$$

This matches **(B)**.

**Check:** $x = \frac{1}{2}$ is in the interval of convergence $(-1, 1]$, so this is valid.

</details>

---

<details>
<summary><strong>Problem 18 Solution</strong></summary>

**(a)** Find the Maclaurin series for $f(x) = e^{-x^2/2}$.

Substitute $u = -\frac{x^2}{2}$ into $e^u = \sum \frac{u^n}{n!}$:

$$e^{-x^2/2} = \sum_{n=0}^{\infty} \frac{1}{n!}\left(-\frac{x^2}{2}\right)^n = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n}}{n! \cdot 2^n}$$

**First four non-zero terms:**

$$e^{-x^2/2} = 1 - \frac{x^2}{2} + \frac{x^4}{8} - \frac{x^6}{48} + \cdots$$

**General term:** $\displaystyle\frac{(-1)^n x^{2n}}{n! \cdot 2^n}$

---

**(b)** Differentiate the series term by term:

$$f'(x) = \frac{d}{dx}\left[1 - \frac{x^2}{2} + \frac{x^4}{8} - \frac{x^6}{48} + \cdots\right]$$

$$= -x + \frac{x^3}{2} - \frac{x^5}{8} + \cdots$$

**General term:** Differentiate $\frac{(-1)^n x^{2n}}{n! \cdot 2^n}$:

$$f'(x) = \sum_{n=1}^{\infty} \frac{(-1)^n \cdot 2n \cdot x^{2n-1}}{n! \cdot 2^n} = \sum_{n=1}^{\infty} \frac{(-1)^n x^{2n-1}}{(n-1)! \cdot 2^{n-1}}$$

Or equivalently, shifting the index with $m = n - 1$:

$$f'(x) = \sum_{m=0}^{\infty} \frac{(-1)^{m+1} x^{2m+1}}{m! \cdot 2^m}$$

**First four non-zero terms:** $f'(x) = -x + \frac{x^3}{2} - \frac{x^5}{8} + \frac{x^7}{48} - \cdots$

---

**(c)** Integrate using the first three non-zero terms:

$$\int_0^1 e^{-x^2/2}\,dx \approx \int_0^1 \left(1 - \frac{x^2}{2} + \frac{x^4}{8}\right)\,dx$$

$$= \left[x - \frac{x^3}{6} + \frac{x^5}{40}\right]_0^1$$

$$= 1 - \frac{1}{6} + \frac{1}{40}$$

$$= \frac{120 - 20 + 3}{120}$$

$$\boxed{= \frac{103}{120}}$$

---

**(d)** The series for $e^{-x^2/2}$ is alternating (for $x \in [0, 1]$, the terms alternate in sign and decrease in magnitude). By the alternating series estimation theorem, the error from truncating after the $\frac{x^4}{8}$ term is bounded by the absolute value of the first omitted term.

The first omitted term in the *integrand* is $-\frac{x^6}{48}$. Since this term is **negative**, the partial sum $1 - \frac{x^2}{2} + \frac{x^4}{8}$ is **greater than** $e^{-x^2/2}$ for $x \in (0, 1)$.

Therefore, the integral approximation **overestimates** the actual value.

$$\boxed{\text{The approximation is an overestimate.}}$$

</details>

---

<details>
<summary><strong>Problem 19 Solution</strong></summary>

**Answer: (A)** $\frac{3}{5 - x}$

The given series is:

$$f(x) = \sum_{n=0}^{\infty} \frac{(x-2)^n}{3^n} = \sum_{n=0}^{\infty} \left(\frac{x-2}{3}\right)^n$$

This is a geometric series with first term $1$ and common ratio $r = \frac{x-2}{3}$.

The sum of a geometric series is $\frac{1}{1 - r}$:

$$f(x) = \frac{1}{1 - \frac{x-2}{3}} = \frac{1}{\frac{3 - (x-2)}{3}} = \frac{3}{3 - x + 2} = \frac{3}{5 - x}$$

This matches **(A)**.

**Convergence condition:** $\left|\frac{x-2}{3}\right| < 1 \implies |x - 2| < 3 \implies -1 < x < 5$.

</details>

---

<details>
<summary><strong>Problem 20 Solution</strong></summary>

**(a)** The 5th-degree Maclaurin polynomial for $\sin x$:

$$T_5(x) = x - \frac{x^3}{3!} + \frac{x^5}{5!} = x - \frac{x^3}{6} + \frac{x^5}{120}$$

$$\boxed{T_5(x) = x - \frac{x^3}{6} + \frac{x^5}{120}}$$

---

**(b)** Approximate $\sin(0.3)$ using $T_5(0.3)$:

$$T_5(0.3) = 0.3 - \frac{(0.3)^3}{6} + \frac{(0.3)^5}{120}$$

$$= 0.3 - \frac{0.027}{6} + \frac{0.00243}{120}$$

$$= 0.3 - 0.0045 + 0.00002025$$

$$\boxed{T_5(0.3) = 0.295520}$$

(To 6 decimal places: $0.295520$.)

---

**(c)** The actual value is $\sin(0.3) = 0.295520...$

The absolute error is:

$$|T_5(0.3) - \sin(0.3)| = |0.295520... - 0.295520...| \approx 2.5 \times 10^{-8}$$

The Maclaurin series for $\sin x$ is an **alternating series** (for positive $x$). By the alternating series estimation theorem, the error is bounded by the absolute value of the first omitted term:

$$\left|\frac{(0.3)^7}{7!}\right| = \frac{0.0002187}{5040} \approx 4.34 \times 10^{-8}$$

Since the first omitted term is $-\frac{x^7}{5040}$ (negative), the partial sum $T_5(x)$ is an **overestimate** of $\sin x$ for $x > 0$.

$$\boxed{\text{Absolute error} \approx 2.5 \times 10^{-8}. \text{ The approximation is an overestimate.}}$$

---

**(d)** For inputs in $[-\pi, \pi]$, we need $|R_n(\pi)| < 10^{-7}$, where $R_n$ is the remainder.

The worst case is $x = \pi$ (largest magnitude). By the alternating series estimation theorem, the error is bounded by the first omitted term:

$$\left|\frac{\pi^{N+1}}{(N+1)!}\right| < 10^{-7}$$

where $N$ is the degree of the polynomial (using the next non-zero term after degree $N$).

Test successive odd terms (since only odd terms are non-zero in $\sin x$):

| Degree $N$ | First omitted term at $x = \pi$ | Value |
|-----------|--------------------------------|-------|
| 5 | $\frac{\pi^7}{7!} = \frac{3020.3}{5040}$ | $\approx 0.599$ |
| 7 | $\frac{\pi^9}{9!} = \frac{29809}{362880}$ | $\approx 0.0821$ |
| 9 | $\frac{\pi^{11}}{11!} = \frac{294204}{39916800}$ | $\approx 0.00737$ |
| 11 | $\frac{\pi^{13}}{13!}$ | $\approx 4.67 \times 10^{-4}$ |
| 13 | $\frac{\pi^{15}}{15!}$ | $\approx 2.21 \times 10^{-5}$ |
| 15 | $\frac{\pi^{17}}{17!}$ | $\approx 7.95 \times 10^{-7}$ |
| 17 | $\frac{\pi^{19}}{19!}$ | $\approx 2.21 \times 10^{-8}$ |

Since $\frac{\pi^{19}}{19!} \approx 2.21 \times 10^{-8} < 10^{-7}$ but $\frac{\pi^{17}}{17!} \approx 7.95 \times 10^{-7} > 10^{-7}$:

Ganga needs the polynomial of degree 17 so that the first omitted term (degree 19) satisfies the error bound.

$$\boxed{\text{Minimum degree: } 17}$$

This means Ganga's code would compute: $T_{17}(x) = x - \frac{x^3}{6} + \frac{x^5}{120} - \frac{x^7}{5040} + \frac{x^9}{362880} - \frac{x^{11}}{39916800} + \frac{x^{13}}{6227020800} - \frac{x^{15}}{1307674368000} + \frac{x^{17}}{355687428096000}$. That's nine terms — totally manageable for a microprocessor, and way cheaper than computing the actual sine function.

</details>

---

## What's Next

You just learned the most powerful idea in BC Calculus: any "nice" function can be represented as an infinite polynomial — a Taylor series — that matches the function's value and every derivative at a chosen center point. You can build new series from the six you memorized using substitution, differentiation, integration, and multiplication. And you can use these series to approximate integrals that would otherwise be impossible.

But there's a lingering question: *how good is the approximation?* If you use $T_5(x)$ instead of the full infinite series, how far off could you be? That's exactly what the **Lagrange Error Bound** answers — it gives you a precise upper bound on the error of a Taylor polynomial approximation, which is essential for guaranteeing accuracy on the AP exam and in real-world engineering (like Ganga's Robotics controller).

Next up: [Lagrange Error Bound](/calculus/lagrange-error-bound) — the mathematical safety net that tells you exactly how accurate your Taylor polynomial is.

---

<div align="center">

[← Power Series](/calculus/power-series) | [Lagrange Error Bound →](/calculus/lagrange-error-bound)

</div>
