# Power Series
<p class="article-date">April 23, 2026</p>

*You know how a recipe can be broken down into individual ingredients — a little sugar here, a dash of cinnamon there, each one measured precisely? A power series does the same thing with functions. It takes something complicated like $e^x$ or $\ln(1 + x)$ and expresses it as an infinite sum of simple polynomial ingredients: $c_0 + c_1 x + c_2 x^2 + c_3 x^3 + \cdots$. Each term is just a coefficient times a power of $x$ — the mathematical equivalent of adding one ingredient at a time to a Panda Express orange chicken recipe until it tastes exactly right. The more terms you add, the closer you get to the real thing. And the beautiful part? Unlike a recipe with a fixed number of steps, a power series can be infinitely precise — as long as you stay within its radius of convergence.*

---

## What You'll Learn
- Define a power series centered at $x = a$ and identify its coefficients
- Understand the three possible cases for the radius of convergence ($R = 0$, $R = \infty$, $0 < R < \infty$)
- Use the Ratio Test to find the radius of convergence $R$
- Determine the full interval of convergence (IOC) by checking endpoints separately
- Differentiate and integrate power series term by term
- Build new power series from known ones using substitution and multiplication
- Represent $\frac{1}{1 - x}$ as the geometric power series $\sum_{n=0}^{\infty} x^n$
- Derive power series representations for functions like $\frac{1}{1 + x^2}$, $\ln(1 + x)$, and $\arctan x$
- Recognize when and how to manipulate known series to create new ones

---

## Prerequisites
- [Convergence Tests](/calculus/convergence-tests)
- [Geometric Series](/calculus/series)
- [Derivatives](/calculus/0304-basic-derivative-rules)

---

## The Core Concept

### Intuition First

Think about ordering a custom drink at Ding Tea. You start with a base (tea), then add boba, then adjust the sweetness level, then add toppings. Each addition refines the drink, getting it closer to your perfect order. The more customization you add, the more precisely the drink matches your taste.

A power series works the same way. Instead of building a drink, you're building a *function* — one polynomial term at a time. Start with a constant ($c_0$). Then add a linear term ($c_1 x$). Then a quadratic term ($c_2 x^2$). Each new term you add refines the approximation, getting it closer and closer to the actual function you're trying to represent.

The key question is: **for which values of $x$ does this infinite sum actually converge to a finite value?** That's where the radius of convergence comes in. Near the center, the series works perfectly. Far from the center, the terms might blow up and the series diverges. There's a boundary — the radius of convergence — that separates the "safe zone" from the "danger zone."

It's like how your favorite Starbucks frappe tastes perfect when the proportions are right, but if someone keeps adding espresso shots without limit, eventually it becomes undrinkable. The radius of convergence is the boundary where the balance tips.

### The Formal Definition

A **power series centered at $a$** is an infinite series of the form:

$$\boxed{\sum_{n=0}^{\infty} c_n(x - a)^n = c_0 + c_1(x - a) + c_2(x - a)^2 + c_3(x - a)^3 + \cdots}$$

where:
- $c_n$ are the **coefficients** (constants that don't depend on $x$)
- $a$ is the **center** of the power series
- $x$ is the variable

When $a = 0$, we get the simpler form:

$$\sum_{n=0}^{\infty} c_n x^n = c_0 + c_1 x + c_2 x^2 + c_3 x^3 + \cdots$$

**Think of a power series as an "infinite polynomial."** A regular polynomial has finitely many terms and works for all $x$. A power series has infinitely many terms but might only work for certain values of $x$.

### Radius and Interval of Convergence

For any power series $\sum c_n(x - a)^n$, there are exactly **three possible cases**:

| Case | Radius of Convergence | Interval of Convergence | Meaning |
|------|----------------------|------------------------|---------|
| 1 | $R = 0$ | Only $x = a$ | The series only converges at its center — useless for representing functions |
| 2 | $R = \infty$ | $(-\infty, \infty)$ | The series converges for all real $x$ — the dream scenario |
| 3 | $0 < R < \infty$ | Centered at $a$, width $2R$ | The series converges on some interval around $a$, and we must check endpoints separately |

For Case 3, the series definitely converges when $|x - a| < R$ and definitely diverges when $|x - a| > R$. At the endpoints $x = a \pm R$, **anything can happen** — the series might converge at both, one, or neither endpoint. That's why we always check them separately.

Think of it like the range of your car radio as Dad drives you through San Diego. The station broadcasts from a central tower (center $a$). Within a certain radius, you get perfect reception (convergence). Beyond that radius, you get static (divergence). Right at the boundary, the signal might cut in and out — you have to test it to find out.

---

## Finding the Radius of Convergence: The Ratio Test

The **Ratio Test** is the go-to tool for finding $R$. Given $\sum c_n(x - a)^n$:

$$L = \lim_{n \to \infty} \left|\frac{c_{n+1}}{c_n}\right|$$

Then:

$$R = \frac{1}{L}$$

(If $L = 0$, then $R = \infty$. If $L = \infty$, then $R = 0$.)

**Why does this work?** The Ratio Test says $\sum a_n$ converges when $\lim \left|\frac{a_{n+1}}{a_n}\right| < 1$. For a power series, this limit involves $|x - a|$, and setting it less than $1$ gives you the radius.

**Full procedure for the Ratio Test on $\sum c_n(x - a)^n$:**

1. Compute $\lim_{n \to \infty} \left|\frac{c_{n+1}(x - a)^{n+1}}{c_n(x - a)^n}\right| = |x - a| \cdot \lim_{n \to \infty}\left|\frac{c_{n+1}}{c_n}\right| = |x - a| \cdot L$

2. Set $|x - a| \cdot L < 1$, giving $|x - a| < \frac{1}{L} = R$

3. The series converges for $a - R < x < a + R$

4. **Check each endpoint separately** using other convergence tests (p-series, AST, etc.)

---

## Worked Examples

### Example 1: Finding Radius and IOC — $\sum_{n=0}^{\infty} \frac{x^n}{3^n}$

This is our "hello world" of power series. Let's find where it converges.

**Identify:** $c_n = \frac{1}{3^n}$, center $a = 0$.

**Apply the Ratio Test:**

$$\lim_{n \to \infty} \left|\frac{a_{n+1}}{a_n}\right| = \lim_{n \to \infty} \left|\frac{x^{n+1}/3^{n+1}}{x^n/3^n}\right| = \lim_{n \to \infty} \left|\frac{x}{3}\right| = \frac{|x|}{3}$$

Set $\frac{|x|}{3} < 1$: $|x| < 3$, so $R = 3$.

**Check endpoints:**

At $x = 3$: $\sum \frac{3^n}{3^n} = \sum 1 = 1 + 1 + 1 + \cdots$ **diverges**.

At $x = -3$: $\sum \frac{(-3)^n}{3^n} = \sum (-1)^n = 1 - 1 + 1 - 1 + \cdots$ **diverges**.

$$\boxed{R = 3, \quad \text{IOC: } (-3, 3)}$$

**Bonus insight:** This is actually a geometric series! $\sum \left(\frac{x}{3}\right)^n = \frac{1}{1 - x/3} = \frac{3}{3 - x}$ for $|x| < 3$.

---

### Example 2: A Series with $R = \infty$ — $\sum_{n=0}^{\infty} \frac{x^n}{n!}$

**Identify:** $c_n = \frac{1}{n!}$, center $a = 0$.

**Ratio Test:**

$$\lim_{n \to \infty} \left|\frac{x^{n+1}/(n+1)!}{x^n/n!}\right| = \lim_{n \to \infty} \left|\frac{x}{n+1}\right| = |x| \cdot \lim_{n \to \infty} \frac{1}{n + 1} = |x| \cdot 0 = 0$$

Since the limit is $0 < 1$ for **all** $x$, the series converges everywhere.

$$\boxed{R = \infty, \quad \text{IOC: } (-\infty, \infty)}$$

This is actually the series for $e^x$! We'll see more of this when we get to Taylor series.

---

### Example 3: Endpoint Drama — $\sum_{n=1}^{\infty} \frac{x^n}{n}$

**Identify:** $c_n = \frac{1}{n}$ (starting at $n = 1$), center $a = 0$.

**Ratio Test:**

$$\lim_{n \to \infty} \left|\frac{x^{n+1}/(n+1)}{x^n/n}\right| = \lim_{n \to \infty} |x| \cdot \frac{n}{n+1} = |x| \cdot 1 = |x|$$

Set $|x| < 1$: $R = 1$.

**Check endpoints — this is where it gets interesting:**

At $x = 1$: $\sum_{n=1}^{\infty} \frac{1}{n} = 1 + \frac{1}{2} + \frac{1}{3} + \cdots$ — this is the **harmonic series**, which **diverges**.

At $x = -1$: $\sum_{n=1}^{\infty} \frac{(-1)^n}{n} = -1 + \frac{1}{2} - \frac{1}{3} + \cdots$ — this is the **alternating harmonic series**, which **converges** by the AST.

$$\boxed{R = 1, \quad \text{IOC: } [-1, 1)}$$

Notice the asymmetry: one endpoint is included, the other isn't. This happens frequently on the AP exam. Always check both endpoints — never assume they behave the same way.

This series actually equals $-\ln(1 - x)$ on $[-1, 1)$. We'll derive this in Example 7.

---

### Example 4: A Series Centered at $a \neq 0$ — $\sum_{n=0}^{\infty} \frac{(-1)^n (x - 2)^n}{5^n}$

**Identify:** $c_n = \frac{(-1)^n}{5^n}$, center $a = 2$.

**Ratio Test:**

$$\lim_{n \to \infty} \left|\frac{(-1)^{n+1}(x-2)^{n+1}/5^{n+1}}{(-1)^n(x-2)^n/5^n}\right| = \lim_{n \to \infty} \frac{|x - 2|}{5} = \frac{|x - 2|}{5}$$

Set $\frac{|x-2|}{5} < 1$: $|x - 2| < 5$, so $R = 5$.

The open interval is $(2 - 5, 2 + 5) = (-3, 7)$.

**Check endpoints:**

At $x = 7$: $\sum \frac{(-1)^n \cdot 5^n}{5^n} = \sum (-1)^n$ **diverges**.

At $x = -3$: $\sum \frac{(-1)^n(-5)^n}{5^n} = \sum \frac{(-1)^n \cdot (-1)^n \cdot 5^n}{5^n} = \sum 1$ **diverges**.

$$\boxed{R = 5, \quad \text{IOC: } (-3, 7)}$$

This is a geometric series $\sum \left(\frac{-(x-2)}{5}\right)^n = \frac{1}{1 + (x-2)/5} = \frac{5}{x + 3}$.

---

### Example 5: Finding $R$ with Factorials — $\sum_{n=0}^{\infty} \frac{n! \cdot x^n}{10^n}$

**Ratio Test:**

$$\lim_{n \to \infty} \left|\frac{(n+1)! \cdot x^{n+1}/10^{n+1}}{n! \cdot x^n/10^n}\right| = \lim_{n \to \infty} \frac{(n+1)|x|}{10} = \infty$$

for any $x \neq 0$.

The limit is infinite for every nonzero $x$, so the series only converges at $x = 0$.

$$\boxed{R = 0, \quad \text{IOC: } \{0\} \text{ (only the center)}}$$

This is the $R = 0$ case. The factorial in the coefficients grows so fast that the terms blow up for any nonzero $x$, no matter how small. It's like trying to add Starbucks espresso shots where each shot is $n!$ times stronger — even the tiniest amount of $x$ makes it explode.

---

### Example 6: Geometric Series as a Power Series

This is the **most important power series in all of AP Calculus BC.** Everything else builds from it.

The geometric series formula says:

$$\frac{1}{1 - x} = \sum_{n=0}^{\infty} x^n = 1 + x + x^2 + x^3 + \cdots \quad \text{for } |x| < 1$$

This is a power series centered at $0$ with $c_n = 1$ for all $n$, and $R = 1$.

**Why is this so powerful?** Because we can use substitution, differentiation, and integration to create power series for *many* other functions from this one starting point. It's like how the base tea at Ding Tea can become dozens of different drinks depending on what you add to it.

**Quick substitution examples:**

**Replace $x$ with $-x$:**

$$\frac{1}{1 + x} = \sum_{n=0}^{\infty} (-x)^n = \sum_{n=0}^{\infty} (-1)^n x^n = 1 - x + x^2 - x^3 + \cdots \quad \text{for } |x| < 1$$

**Replace $x$ with $x^2$:**

$$\frac{1}{1 - x^2} = \sum_{n=0}^{\infty} (x^2)^n = \sum_{n=0}^{\infty} x^{2n} = 1 + x^2 + x^4 + x^6 + \cdots \quad \text{for } |x| < 1$$

**Replace $x$ with $-x^2$:**

$$\frac{1}{1 + x^2} = \sum_{n=0}^{\infty} (-x^2)^n = \sum_{n=0}^{\infty} (-1)^n x^{2n} = 1 - x^2 + x^4 - x^6 + \cdots \quad \text{for } |x| < 1$$

This last one is especially important — we'll integrate it to get $\arctan x$ in Example 7.

---

### Example 7: Building New Series — Integration for $\ln(1 + x)$ and $\arctan x$

This is where the magic happens. We take known power series and integrate them term by term to create series for functions that would be extremely difficult to find otherwise.

**Series for $\ln(1 + x)$:**

Start with the series we derived above:

$$\frac{1}{1 + x} = \sum_{n=0}^{\infty} (-1)^n x^n \quad \text{for } |x| < 1$$

Integrate both sides from $0$ to $x$:

$$\int_0^x \frac{1}{1 + t} \, dt = \sum_{n=0}^{\infty} (-1)^n \int_0^x t^n \, dt$$

$$\ln(1 + x) = \sum_{n=0}^{\infty} (-1)^n \frac{x^{n+1}}{n+1} = x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \cdots$$

Re-indexing (let $m = n + 1$):

$$\boxed{\ln(1 + x) = \sum_{n=1}^{\infty} \frac{(-1)^{n+1} x^n}{n} = x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \cdots}$$

**IOC:** The original series had $|x| < 1$. After integration, the IOC becomes $(-1, 1]$ — the right endpoint $x = 1$ is now included (it gives the convergent alternating harmonic series), while $x = -1$ still diverges. In fact, $\ln(2) = 1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \cdots$, which is a beautiful result.

**Series for $\arctan x$:**

Start with:

$$\frac{1}{1 + x^2} = \sum_{n=0}^{\infty} (-1)^n x^{2n} \quad \text{for } |x| < 1$$

Integrate both sides from $0$ to $x$:

$$\int_0^x \frac{1}{1 + t^2} \, dt = \sum_{n=0}^{\infty} (-1)^n \int_0^x t^{2n} \, dt$$

$$\arctan x = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{2n+1} = x - \frac{x^3}{3} + \frac{x^5}{5} - \frac{x^7}{7} + \cdots$$

$$\boxed{\arctan x = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+1}}{2n+1} \quad \text{for } -1 \leq x \leq 1}$$

**IOC:** $[-1, 1]$ — both endpoints converge (alternating series at each).

Plugging in $x = 1$ gives the stunning formula:

$$\frac{\pi}{4} = 1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + \cdots$$

This is the **Leibniz formula for $\pi$** — an infinite series of simple fractions that adds up to $\frac{\pi}{4}$. It converges very slowly (you'd need thousands of terms for a few decimal places), but the fact that such a simple pattern gives you $\pi$ is one of the most beautiful results in all of mathematics.

---

### Example 8: Differentiation of Power Series — Series for $\frac{1}{(1 - x)^2}$

We can also differentiate power series term by term.

Start with:

$$\frac{1}{1 - x} = \sum_{n=0}^{\infty} x^n = 1 + x + x^2 + x^3 + \cdots \quad \text{for } |x| < 1$$

Differentiate both sides:

$$\frac{d}{dx}\left[\frac{1}{1-x}\right] = \frac{d}{dx}\left[\sum_{n=0}^{\infty} x^n\right]$$

$$\frac{1}{(1-x)^2} = \sum_{n=1}^{\infty} nx^{n-1} = 1 + 2x + 3x^2 + 4x^3 + \cdots$$

$$\boxed{\frac{1}{(1-x)^2} = \sum_{n=1}^{\infty} nx^{n-1} = \sum_{n=0}^{\infty} (n+1)x^n \quad \text{for } |x| < 1}$$

**Key fact:** When you differentiate or integrate a power series, the **radius of convergence stays the same** ($R$ doesn't change), but the behavior at the endpoints might change.

Think of it like the range of that radio station as you drive through San Diego. Differentiation and integration don't move the broadcast tower or change its power — the signal reaches the same distance ($R$). But the quality at the very edge of range (the endpoints) might improve or degrade.

---

### Example 9: Multiplication and Substitution — Series for $\frac{x^2}{1 + x^3}$

**Goal:** Find the power series for $\frac{x^2}{1 + x^3}$ centered at $0$.

**Strategy:** Rewrite as $x^2 \cdot \frac{1}{1 - (-x^3)}$ and use the geometric series with $u = -x^3$:

$$\frac{1}{1 + x^3} = \frac{1}{1 - (-x^3)} = \sum_{n=0}^{\infty} (-x^3)^n = \sum_{n=0}^{\infty} (-1)^n x^{3n} \quad \text{for } |x^3| < 1, \text{ i.e., } |x| < 1$$

Now multiply by $x^2$:

$$\frac{x^2}{1 + x^3} = x^2 \cdot \sum_{n=0}^{\infty} (-1)^n x^{3n} = \sum_{n=0}^{\infty} (-1)^n x^{3n+2}$$

$$\boxed{\frac{x^2}{1 + x^3} = x^2 - x^5 + x^8 - x^{11} + \cdots = \sum_{n=0}^{\infty} (-1)^n x^{3n+2} \quad \text{for } |x| < 1}$$

The radius of convergence is still $R = 1$, since the substitution $u = -x^3$ requires $|x^3| < 1$, which means $|x| < 1$.

---

### Example 10: Finding a Power Series by Integration — $\int \frac{1}{1 + x^4} \, dx$

Here's a case where power series make an "impossible" integral easy.

Try integrating $\frac{1}{1 + x^4}$ using standard techniques — it requires partial fractions with irreducible quadratics and gets extremely messy. But with power series, it's almost trivial.

**Step 1 — Write $\frac{1}{1 + x^4}$ as a power series:**

$$\frac{1}{1 + x^4} = \frac{1}{1 - (-x^4)} = \sum_{n=0}^{\infty} (-1)^n x^{4n} \quad \text{for } |x| < 1$$

**Step 2 — Integrate term by term:**

$$\int \frac{1}{1 + x^4} \, dx = \sum_{n=0}^{\infty} (-1)^n \frac{x^{4n+1}}{4n+1} + C$$

$$= x - \frac{x^5}{5} + \frac{x^9}{9} - \frac{x^{13}}{13} + \cdots + C$$

$$\boxed{\int \frac{1}{1+x^4}\,dx = \sum_{n=0}^{\infty} \frac{(-1)^n x^{4n+1}}{4n+1} + C \quad \text{for } |x| < 1}$$

This is a clean, elegant answer that would take pages to compute by hand using traditional methods. Power series turn hard integrals into easy ones — like using the express checkout at Sesame Donuts instead of waiting in the regular line.

---

## Key Formulas & Rules

| Concept | Formula / Rule |
|---------|---------------|
| Power series definition | $\sum_{n=0}^{\infty} c_n(x - a)^n$, center $a$, coefficients $c_n$ |
| Radius of convergence | $R = \frac{1}{\lim_{n \to \infty} \left\|c_{n+1}/c_n\right\|}$ (via Ratio Test) |
| IOC procedure | Find $R$, then check $x = a - R$ and $x = a + R$ separately |
| Geometric series | $\frac{1}{1-x} = \sum_{n=0}^{\infty} x^n$ for $\|x\| < 1$ |
| Substitution | Replace $x$ with $g(x)$ in a known series; IOC adjusts via $\|g(x)\| < R$ |
| Term-by-term differentiation | $f'(x) = \sum_{n=1}^{\infty} n c_n (x-a)^{n-1}$; same $R$ |
| Term-by-term integration | $\int f(x)\,dx = C + \sum_{n=0}^{\infty} \frac{c_n(x-a)^{n+1}}{n+1}$; same $R$ |
| $\frac{1}{1+x}$ | $\sum_{n=0}^{\infty} (-1)^n x^n$ for $\|x\| < 1$ |
| $\frac{1}{(1-x)^2}$ | $\sum_{n=0}^{\infty} (n+1)x^n$ for $\|x\| < 1$ |
| $\ln(1+x)$ | $\sum_{n=1}^{\infty} \frac{(-1)^{n+1}x^n}{n}$ for $-1 < x \leq 1$ |
| $\arctan x$ | $\sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+1}}{2n+1}$ for $-1 \leq x \leq 1$ |

---

## Common Mistakes to Avoid

### Mistake 1: Forgetting to Check Endpoints

**Wrong:** "The Ratio Test gives $|x| < 3$, so the IOC is $(-3, 3)$."

**Right:** The Ratio Test only tells you the *open* interval. You must test $x = -3$ and $x = 3$ separately using other tests (p-series, AST, Divergence Test, etc.) to determine if the endpoints are included.

The Ratio Test is **inconclusive** when the limit equals exactly $1$ — which is precisely what happens at the endpoints. It's like the Ratio Test bringing you to the front door and saying, "I got you here, but you need to knock and see for yourself."

---

### Mistake 2: Confusing Radius with Interval

**Wrong:** "$R = 5$, so the IOC is $(-5, 5)$."

**Right:** $R$ is the *distance* from the center to each edge. If the center is $a = 2$ and $R = 5$, the open interval is $(2 - 5, 2 + 5) = (-3, 7)$, not $(-5, 5)$.

The IOC is always centered at $a$, not at $0$.

---

### Mistake 3: Changing $R$ After Differentiation or Integration

**Wrong:** "I integrated a series with $R = 1$, so now $R = 2$."

**Right:** Differentiation and integration of a power series **do not change the radius of convergence.** The value of $R$ stays the same. Only the endpoint behavior (whether they're included or excluded) might change.

---

### Mistake 4: Substituting Without Adjusting the IOC

**Wrong:** Starting from $\frac{1}{1-x} = \sum x^n$ for $|x| < 1$ and substituting $x \to 3x$ to get $\frac{1}{1-3x} = \sum (3x)^n$ for $|x| < 1$.

**Right:** After substituting $x \to 3x$, the convergence condition becomes $|3x| < 1$, so $|x| < \frac{1}{3}$. The IOC shrinks.

Always substitute into the convergence condition too, not just the formula.

---

### Mistake 5: Forgetting the Constant of Integration

When integrating a power series, don't forget to determine the constant $C$. Usually you plug in a convenient value (often $x = 0$) to find it.

**Example:** Integrating $\frac{1}{1+x} = \sum (-1)^n x^n$ gives $\ln(1+x) = C + \sum \frac{(-1)^n x^{n+1}}{n+1}$. Setting $x = 0$: $\ln 1 = C + 0$, so $C = 0$.

---

### Mistake 6: Using the Wrong Test at Endpoints

At the endpoints, the Ratio Test gives a limit of exactly $1$ (inconclusive). You need a **different** test:
- **Alternating Series Test** if the endpoint produces an alternating series
- **p-Series Test** if it looks like $\sum \frac{1}{n^p}$
- **Divergence Test** if the terms don't approach zero
- **Comparison Tests** for anything else

---

## AP Exam Tips

### For BC Students:

1. **Power series is heavily tested on BC.** Expect 3-5 multiple choice questions and frequently one full free response (or part of a free response) on series topics. Power series is the heart of Unit 10.

2. **Memorize the geometric series and its variants.** The series $\frac{1}{1-x} = \sum x^n$ for $|x| < 1$ is the foundation. If you know this one series, you can derive everything else through substitution, differentiation, and integration.

3. **Always show your endpoint analysis.** On free response, the AP readers want to see: (a) you found $R$ using the Ratio Test, (b) you identified the two endpoint values, (c) you plugged each in and applied a convergence test. Full credit requires all three steps.

4. **Know the three key derived series cold:**
   - $\ln(1+x) = x - \frac{x^2}{2} + \frac{x^3}{3} - \cdots$ for $(-1, 1]$
   - $\arctan x = x - \frac{x^3}{3} + \frac{x^5}{5} - \cdots$ for $[-1, 1]$
   - $\frac{1}{(1-x)^2} = 1 + 2x + 3x^2 + \cdots$ for $(-1, 1)$

5. **"Find the power series representation"** means: write the function as $\sum c_n x^n$ (or $\sum c_n(x-a)^n$) and state the IOC. Both parts are needed for full credit.

6. **Integration of power series is a common FR technique.** If they ask you to find $\int f(x)\,dx$ where $f$ is given as a power series, just integrate each term. Don't forget $+C$ and use a known value (often $f(0)$) to determine it.

7. **The Ratio Test on the AP exam is quick.** Most BC power series problems give you a clean ratio that simplifies easily. If your Ratio Test algebra is getting messy, double-check that you set it up correctly.

8. **On MC, learn to quickly identify series type.** If you see $\sum \frac{x^n}{n!}$, that's $e^x$. If you see $\sum \frac{(-1)^n x^{2n+1}}{(2n+1)!}$, that's $\sin x$. Pattern recognition saves time.

---

## Practice Problems

### Basic (Problems 1-5)

**1.** Find the radius of convergence and interval of convergence for:

$$\sum_{n=0}^{\infty} \frac{x^n}{2^n}$$

---

**2.** Find the radius of convergence and interval of convergence for:

$$\sum_{n=1}^{\infty} \frac{x^n}{n \cdot 4^n}$$

---

**3.** Find the radius of convergence and interval of convergence for:

$$\sum_{n=0}^{\infty} \frac{(-1)^n x^n}{n+1}$$

---

**4.** Write the power series representation (centered at $0$) for $f(x) = \frac{1}{1 - 2x}$ and state the IOC.

---

**5.** Write the power series representation for $f(x) = \frac{1}{1 + 5x}$ and state the IOC.

---

### Intermediate (Problems 6-10)

**6.** Find the power series representation for $f(x) = \frac{x}{1 - x^2}$ and state the IOC.

---

**7.** Use the power series for $\frac{1}{1+x}$ to find the power series for $\ln(1 + x)$. Then evaluate $\ln(1 + x)$ at $x = 1$ to express $\ln 2$ as an infinite series.

---

**8.** Find the power series for $f(x) = \frac{1}{(1 + x)^2}$ by differentiating a known series. State the IOC.

---

**9.** Find the radius of convergence and interval of convergence for:

$$\sum_{n=1}^{\infty} \frac{(-1)^n (x - 3)^n}{n \cdot 2^n}$$

---

**10.** Find the power series representation for $\int \frac{1}{1 + x^3} \, dx$, centered at $0$. State the IOC.

---

### Advanced (Problems 11-15)

**11.** Find the power series for $f(x) = \frac{x^2}{(1 - x)^2}$ using differentiation and multiplication of known series. State the IOC.

---

**12.** Use a power series to evaluate $\int_0^{1/2} \frac{\arctan x}{x} \, dx$ as an infinite series (write the first four nonzero terms plus a pattern).

---

**13.** Find the radius and interval of convergence for:

$$\sum_{n=0}^{\infty} \frac{n^2 \cdot x^n}{3^n}$$

---

**14.** Find the power series for $f(x) = \ln\left(\frac{1+x}{1-x}\right)$ centered at $0$. State the IOC.

---

**15.** The function $f$ is defined by the power series $f(x) = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n}}{(2n)!}$. Find $f'(x)$ as a power series and identify both $f(x)$ and $f'(x)$ as known functions.

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

The interval of convergence for $\displaystyle\sum_{n=1}^{\infty} \frac{(x - 1)^n}{n \cdot 3^n}$ is:

| Choice | Answer |
|--------|--------|
| **(A)** | $(-2, 4)$ |
| **(B)** | $[-2, 4)$ |
| **(C)** | $(-2, 4]$ |
| **(D)** | $[-2, 4]$ |

---

#### Problem 17 (Multiple Choice)

The power series $\displaystyle\sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{2n+1}$ represents which function on its interval of convergence?

| Choice | Answer |
|--------|--------|
| **(A)** | $\sin x$ |
| **(B)** | $\arcsin x$ |
| **(C)** | $\arctan x$ |
| **(D)** | $\ln(1 + x)$ |

---

#### Problem 18 (Multiple Choice)

If $f(x) = \displaystyle\sum_{n=0}^{\infty} \frac{x^n}{2^n}$ for $|x| < 2$, then $f'(x) =$

| Choice | Answer |
|--------|--------|
| **(A)** | $\displaystyle\sum_{n=1}^{\infty} \frac{x^{n-1}}{2^n}$ |
| **(B)** | $\displaystyle\sum_{n=0}^{\infty} \frac{n x^{n-1}}{2^n}$ |
| **(C)** | $\displaystyle\sum_{n=1}^{\infty} \frac{n x^{n-1}}{2^n}$ |
| **(D)** | $\displaystyle\sum_{n=0}^{\infty} \frac{x^{n+1}}{(n+1) \cdot 2^n}$ |

---

#### Problem 19 (Free Response)

Consider the power series $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1} x^n}{n \cdot 2^n}$.

> **(a)** Find the radius of convergence $R$.
>
> **(b)** Determine the full interval of convergence, showing your endpoint analysis.
>
> **(c)** Find the function $f(x)$ that this power series represents. *(Hint: relate it to a known series for $\ln$.)*
>
> **(d)** Use the result from part (c) to find the exact value of the series when $x = 2$.

---

#### Problem 20 (Free Response — Challenging)

Ganga is on the Rancho Bernardo High School Science Olympiad team, studying the behavior of power series for a math-related event. She considers the function:

$$g(x) = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+2}}{(2n+1)(2n+2)}$$

> **(a)** Find the radius of convergence of this power series.
>
> **(b)** Show that $g''(x) = \frac{1}{1+x^2}$ by differentiating the series twice.
>
> **(c)** Using part (b) and the fact that $g(0) = 0$ and $g'(0) = 0$, find a closed-form expression for $g(x)$.
>
> **(d)** Evaluate $g(1)$ both as an infinite series and in closed form, verifying they are equal. Express your answer in terms of $\pi$.

---

## Answer Key

<details>
<summary><strong>Problem 1 Solution</strong></summary>

**Find the radius and interval of convergence for** $\sum_{n=0}^{\infty} \frac{x^n}{2^n}$.

This is a geometric series $\sum \left(\frac{x}{2}\right)^n$.

**Ratio Test:**

$$\lim_{n \to \infty} \left|\frac{x^{n+1}/2^{n+1}}{x^n/2^n}\right| = \left|\frac{x}{2}\right|$$

Set $\left|\frac{x}{2}\right| < 1$: $|x| < 2$, so $R = 2$.

**Endpoints:**

At $x = 2$: $\sum 1^n = 1 + 1 + 1 + \cdots$ **diverges** (Divergence Test).

At $x = -2$: $\sum (-1)^n = 1 - 1 + 1 - 1 + \cdots$ **diverges** (Divergence Test).

$$\boxed{R = 2, \quad \text{IOC: } (-2, 2)}$$

The series equals $\frac{1}{1 - x/2} = \frac{2}{2 - x}$ on this interval.

</details>

---

<details>
<summary><strong>Problem 2 Solution</strong></summary>

**Find the radius and interval of convergence for** $\sum_{n=1}^{\infty} \frac{x^n}{n \cdot 4^n}$.

**Ratio Test:**

$$\lim_{n \to \infty} \left|\frac{x^{n+1}/((n+1) \cdot 4^{n+1})}{x^n/(n \cdot 4^n)}\right| = \lim_{n \to \infty} \left|\frac{x}{4}\right| \cdot \frac{n}{n+1} = \frac{|x|}{4}$$

Set $\frac{|x|}{4} < 1$: $|x| < 4$, so $R = 4$.

**Endpoints:**

At $x = 4$: $\sum_{n=1}^{\infty} \frac{4^n}{n \cdot 4^n} = \sum_{n=1}^{\infty} \frac{1}{n}$ — harmonic series, **diverges**.

At $x = -4$: $\sum_{n=1}^{\infty} \frac{(-4)^n}{n \cdot 4^n} = \sum_{n=1}^{\infty} \frac{(-1)^n}{n}$ — alternating harmonic series, **converges** by AST.

$$\boxed{R = 4, \quad \text{IOC: } [-4, 4)}$$

</details>

---

<details>
<summary><strong>Problem 3 Solution</strong></summary>

**Find the radius and interval of convergence for** $\sum_{n=0}^{\infty} \frac{(-1)^n x^n}{n+1}$.

**Ratio Test:**

$$\lim_{n \to \infty} \left|\frac{(-1)^{n+1} x^{n+1}/(n+2)}{(-1)^n x^n/(n+1)}\right| = |x| \cdot \lim_{n \to \infty} \frac{n+1}{n+2} = |x|$$

Set $|x| < 1$: $R = 1$.

**Endpoints:**

At $x = 1$: $\sum_{n=0}^{\infty} \frac{(-1)^n}{n+1} = 1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \cdots$ — alternating harmonic series, **converges** by AST.

At $x = -1$: $\sum_{n=0}^{\infty} \frac{(-1)^n(-1)^n}{n+1} = \sum_{n=0}^{\infty} \frac{1}{n+1} = 1 + \frac{1}{2} + \frac{1}{3} + \cdots$ — harmonic series, **diverges**.

$$\boxed{R = 1, \quad \text{IOC: } (-1, 1]}$$

</details>

---

<details>
<summary><strong>Problem 4 Solution</strong></summary>

**Write the power series for** $f(x) = \frac{1}{1 - 2x}$.

Use the geometric series $\frac{1}{1-u} = \sum u^n$ with $u = 2x$:

$$\frac{1}{1 - 2x} = \sum_{n=0}^{\infty} (2x)^n = \sum_{n=0}^{\infty} 2^n x^n = 1 + 2x + 4x^2 + 8x^3 + \cdots$$

**Convergence:** $|2x| < 1 \Rightarrow |x| < \frac{1}{2}$

$$\boxed{\frac{1}{1-2x} = \sum_{n=0}^{\infty} 2^n x^n, \quad \text{IOC: } \left(-\frac{1}{2}, \frac{1}{2}\right)}$$

</details>

---

<details>
<summary><strong>Problem 5 Solution</strong></summary>

**Write the power series for** $f(x) = \frac{1}{1 + 5x}$.

Use the geometric series with $u = -5x$:

$$\frac{1}{1 + 5x} = \frac{1}{1 - (-5x)} = \sum_{n=0}^{\infty} (-5x)^n = \sum_{n=0}^{\infty} (-1)^n 5^n x^n$$

$$= 1 - 5x + 25x^2 - 125x^3 + \cdots$$

**Convergence:** $|-5x| < 1 \Rightarrow |x| < \frac{1}{5}$

$$\boxed{\frac{1}{1+5x} = \sum_{n=0}^{\infty} (-1)^n 5^n x^n, \quad \text{IOC: } \left(-\frac{1}{5}, \frac{1}{5}\right)}$$

</details>

---

<details>
<summary><strong>Problem 6 Solution</strong></summary>

**Find the power series for** $f(x) = \frac{x}{1 - x^2}$.

**Strategy:** Write $\frac{x}{1 - x^2} = x \cdot \frac{1}{1 - x^2}$.

Use the geometric series with $u = x^2$:

$$\frac{1}{1 - x^2} = \sum_{n=0}^{\infty} (x^2)^n = \sum_{n=0}^{\infty} x^{2n}$$

Multiply by $x$:

$$\frac{x}{1 - x^2} = x \cdot \sum_{n=0}^{\infty} x^{2n} = \sum_{n=0}^{\infty} x^{2n+1} = x + x^3 + x^5 + x^7 + \cdots$$

**Convergence:** $|x^2| < 1 \Rightarrow |x| < 1$

$$\boxed{\frac{x}{1-x^2} = \sum_{n=0}^{\infty} x^{2n+1}, \quad \text{IOC: } (-1, 1)}$$

</details>

---

<details>
<summary><strong>Problem 7 Solution</strong></summary>

**Derive the power series for $\ln(1+x)$, then express $\ln 2$ as an infinite series.**

Start with:

$$\frac{1}{1+x} = \sum_{n=0}^{\infty} (-1)^n x^n = 1 - x + x^2 - x^3 + \cdots \quad \text{for } |x| < 1$$

Integrate both sides from $0$ to $x$:

$$\int_0^x \frac{dt}{1+t} = \sum_{n=0}^{\infty} (-1)^n \int_0^x t^n \, dt$$

$$\ln(1+x) = \sum_{n=0}^{\infty} (-1)^n \frac{x^{n+1}}{n+1} = x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \cdots$$

Re-indexing:

$$\boxed{\ln(1+x) = \sum_{n=1}^{\infty} \frac{(-1)^{n+1} x^n}{n} \quad \text{for } -1 < x \leq 1}$$

Now evaluate at $x = 1$:

$$\ln 2 = \ln(1 + 1) = \sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n} = 1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \frac{1}{5} - \cdots$$

$$\boxed{\ln 2 = 1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \cdots = \sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n}}$$

The alternating harmonic series converges to $\ln 2$!

</details>

---

<details>
<summary><strong>Problem 8 Solution</strong></summary>

**Find the power series for** $f(x) = \frac{1}{(1+x)^2}$ **by differentiation.**

Start with:

$$\frac{1}{1+x} = \sum_{n=0}^{\infty} (-1)^n x^n \quad \text{for } |x| < 1$$

Note that $\frac{d}{dx}\left[\frac{1}{1+x}\right] = -\frac{1}{(1+x)^2}$.

Differentiating both sides:

$$-\frac{1}{(1+x)^2} = \sum_{n=1}^{\infty} (-1)^n n x^{n-1}$$

Multiply by $-1$:

$$\frac{1}{(1+x)^2} = \sum_{n=1}^{\infty} (-1)^{n+1} n x^{n-1} = -\sum_{n=1}^{\infty} (-1)^n n x^{n-1}$$

Let's write this out to see the pattern:

$$\frac{1}{(1+x)^2} = 1 - 2x + 3x^2 - 4x^3 + \cdots = \sum_{n=0}^{\infty} (-1)^n (n+1) x^n$$

$$\boxed{\frac{1}{(1+x)^2} = \sum_{n=0}^{\infty} (-1)^n (n+1) x^n \quad \text{for } |x| < 1}$$

The radius of convergence remains $R = 1$, unchanged by differentiation.

</details>

---

<details>
<summary><strong>Problem 9 Solution</strong></summary>

**Find the radius and interval of convergence for** $\sum_{n=1}^{\infty} \frac{(-1)^n (x-3)^n}{n \cdot 2^n}$.

**Ratio Test:**

$$\lim_{n \to \infty} \left|\frac{(-1)^{n+1}(x-3)^{n+1}/((n+1) \cdot 2^{n+1})}{(-1)^n(x-3)^n/(n \cdot 2^n)}\right| = |x-3| \cdot \frac{1}{2} \cdot \lim_{n \to \infty}\frac{n}{n+1} = \frac{|x-3|}{2}$$

Set $\frac{|x-3|}{2} < 1$: $|x-3| < 2$, so $R = 2$. The center is $a = 3$.

Open interval: $(3 - 2, 3 + 2) = (1, 5)$.

**Endpoints:**

At $x = 5$: $(x-3) = 2$, so $\sum_{n=1}^{\infty} \frac{(-1)^n \cdot 2^n}{n \cdot 2^n} = \sum_{n=1}^{\infty} \frac{(-1)^n}{n}$ — alternating harmonic series, **converges** by AST.

At $x = 1$: $(x-3) = -2$, so $\sum_{n=1}^{\infty} \frac{(-1)^n(-2)^n}{n \cdot 2^n} = \sum_{n=1}^{\infty} \frac{(-1)^n \cdot (-1)^n \cdot 2^n}{n \cdot 2^n} = \sum_{n=1}^{\infty} \frac{1}{n}$ — harmonic series, **diverges**.

$$\boxed{R = 2, \quad \text{IOC: } (1, 5]}$$

</details>

---

<details>
<summary><strong>Problem 10 Solution</strong></summary>

**Find the power series for** $\int \frac{1}{1+x^3}\,dx$.

Start with the geometric series, substituting $u = -x^3$:

$$\frac{1}{1+x^3} = \frac{1}{1-(-x^3)} = \sum_{n=0}^{\infty} (-x^3)^n = \sum_{n=0}^{\infty} (-1)^n x^{3n}$$

for $|x^3| < 1$, i.e., $|x| < 1$.

Integrate term by term:

$$\int \frac{dx}{1+x^3} = C + \sum_{n=0}^{\infty} (-1)^n \frac{x^{3n+1}}{3n+1}$$

$$= C + x - \frac{x^4}{4} + \frac{x^7}{7} - \frac{x^{10}}{10} + \cdots$$

$$\boxed{\int \frac{dx}{1+x^3} = C + \sum_{n=0}^{\infty} \frac{(-1)^n x^{3n+1}}{3n+1} \quad \text{for } |x| < 1}$$

(The radius of convergence stays $R = 1$; endpoint behavior may change with integration.)

</details>

---

<details>
<summary><strong>Problem 11 Solution</strong></summary>

**Find the power series for** $f(x) = \frac{x^2}{(1-x)^2}$.

**Strategy:** We know from Example 8 that:

$$\frac{1}{(1-x)^2} = \sum_{n=0}^{\infty} (n+1) x^n = 1 + 2x + 3x^2 + 4x^3 + \cdots \quad \text{for } |x| < 1$$

Multiply by $x^2$:

$$\frac{x^2}{(1-x)^2} = x^2 \cdot \sum_{n=0}^{\infty} (n+1) x^n = \sum_{n=0}^{\infty} (n+1) x^{n+2}$$

Re-index by letting $m = n + 2$, so $n = m - 2$ and $n + 1 = m - 1$:

$$= \sum_{m=2}^{\infty} (m-1) x^m = x^2 + 2x^3 + 3x^4 + 4x^5 + \cdots$$

Or equivalently:

$$\boxed{\frac{x^2}{(1-x)^2} = \sum_{n=2}^{\infty} (n-1)x^n = \sum_{n=0}^{\infty} (n+1) x^{n+2} \quad \text{for } |x| < 1}$$

**Verification:** $\frac{x^2}{(1-x)^2} = \left(\frac{x}{1-x}\right)^2$. At $x = \frac{1}{2}$: $\left(\frac{1/2}{1/2}\right)^2 = 1$. From the series: $\frac{1}{4} + \frac{2}{8} + \frac{3}{16} + \cdots$. Using the closed form gives us confidence the answer is correct.

</details>

---

<details>
<summary><strong>Problem 12 Solution</strong></summary>

**Evaluate** $\int_0^{1/2} \frac{\arctan x}{x}\,dx$ **as an infinite series.**

From Example 7:

$$\arctan x = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+1}}{2n+1} = x - \frac{x^3}{3} + \frac{x^5}{5} - \frac{x^7}{7} + \cdots$$

Divide by $x$:

$$\frac{\arctan x}{x} = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n}}{2n+1} = 1 - \frac{x^2}{3} + \frac{x^4}{5} - \frac{x^6}{7} + \cdots$$

Integrate from $0$ to $\frac{1}{2}$:

$$\int_0^{1/2} \frac{\arctan x}{x}\,dx = \sum_{n=0}^{\infty} \frac{(-1)^n}{2n+1} \int_0^{1/2} x^{2n}\,dx$$

$$= \sum_{n=0}^{\infty} \frac{(-1)^n}{2n+1} \cdot \frac{(1/2)^{2n+1}}{2n+1} = \sum_{n=0}^{\infty} \frac{(-1)^n}{(2n+1)^2 \cdot 2^{2n+1}}$$

Writing out the first four nonzero terms:

$$= \frac{1}{1^2 \cdot 2} - \frac{1}{3^2 \cdot 2^3} + \frac{1}{5^2 \cdot 2^5} - \frac{1}{7^2 \cdot 2^7} + \cdots$$

$$= \frac{1}{2} - \frac{1}{72} + \frac{1}{800} - \frac{1}{6272} + \cdots$$

$$\boxed{\int_0^{1/2} \frac{\arctan x}{x}\,dx = \sum_{n=0}^{\infty} \frac{(-1)^n}{(2n+1)^2 \cdot 2^{2n+1}} \approx 0.4872}$$

</details>

---

<details>
<summary><strong>Problem 13 Solution</strong></summary>

**Find the radius and interval of convergence for** $\sum_{n=0}^{\infty} \frac{n^2 x^n}{3^n}$.

**Ratio Test:**

$$\lim_{n \to \infty} \left|\frac{(n+1)^2 x^{n+1} / 3^{n+1}}{n^2 x^n / 3^n}\right| = \frac{|x|}{3} \cdot \lim_{n \to \infty} \frac{(n+1)^2}{n^2} = \frac{|x|}{3} \cdot 1 = \frac{|x|}{3}$$

Set $\frac{|x|}{3} < 1$: $|x| < 3$, so $R = 3$.

**Endpoints:**

At $x = 3$: $\sum n^2 \cdot \frac{3^n}{3^n} = \sum n^2$. Since $n^2 \to \infty$, this **diverges** by the Divergence Test.

At $x = -3$: $\sum n^2 \cdot \frac{(-3)^n}{3^n} = \sum n^2 (-1)^n$. Since $|n^2(-1)^n| = n^2 \to \infty$, this **diverges** by the Divergence Test.

$$\boxed{R = 3, \quad \text{IOC: } (-3, 3)}$$

</details>

---

<details>
<summary><strong>Problem 14 Solution</strong></summary>

**Find the power series for** $f(x) = \ln\left(\frac{1+x}{1-x}\right)$.

Use log properties:

$$\ln\left(\frac{1+x}{1-x}\right) = \ln(1+x) - \ln(1-x)$$

We know:

$$\ln(1+x) = \sum_{n=1}^{\infty} \frac{(-1)^{n+1} x^n}{n} = x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \cdots$$

For $\ln(1-x)$, replace $x$ with $-x$ in $\ln(1+x)$:

$$\ln(1-x) = \sum_{n=1}^{\infty} \frac{(-1)^{n+1}(-x)^n}{n} = \sum_{n=1}^{\infty} \frac{(-1)^{n+1}(-1)^n x^n}{n} = -\sum_{n=1}^{\infty} \frac{x^n}{n}$$

$$= -x - \frac{x^2}{2} - \frac{x^3}{3} - \frac{x^4}{4} - \cdots$$

Subtract:

$$\ln(1+x) - \ln(1-x) = \left(x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \cdots\right) - \left(-x - \frac{x^2}{2} - \frac{x^3}{3} - \frac{x^4}{4} - \cdots\right)$$

$$= 2x + \frac{2x^3}{3} + \frac{2x^5}{5} + \cdots = 2\sum_{n=0}^{\infty} \frac{x^{2n+1}}{2n+1}$$

(All the even-powered terms cancel; the odd-powered terms double.)

$$\boxed{\ln\left(\frac{1+x}{1-x}\right) = 2\sum_{n=0}^{\infty} \frac{x^{2n+1}}{2n+1} = 2x + \frac{2x^3}{3} + \frac{2x^5}{5} + \cdots \quad \text{for } |x| < 1}$$

The IOC is $(-1, 1)$ since both $\ln(1+x)$ and $\ln(1-x)$ require $|x| < 1$ (and $x = 1$ makes $\ln(1-x) = \ln 0$, which is undefined).

</details>

---

<details>
<summary><strong>Problem 15 Solution</strong></summary>

**The function** $f(x) = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n}}{(2n)!}$. **Find $f'(x)$ and identify both functions.**

Write out the first few terms of $f(x)$:

$$f(x) = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!} + \cdots$$

This is the **Maclaurin series for $\cos x$**, so $f(x) = \cos x$.

**Differentiate term by term:**

$$f'(x) = \sum_{n=1}^{\infty} \frac{(-1)^n \cdot 2n \cdot x^{2n-1}}{(2n)!} = \sum_{n=1}^{\infty} \frac{(-1)^n x^{2n-1}}{(2n-1)!}$$

Write out:

$$f'(x) = -x + \frac{x^3}{3!} - \frac{x^5}{5!} + \cdots = -\left(x - \frac{x^3}{3!} + \frac{x^5}{5!} - \cdots\right)$$

The expression in parentheses is the series for $\sin x$.

$$\boxed{f(x) = \cos x, \quad f'(x) = -\sin x}$$

This confirms the familiar derivative: $\frac{d}{dx}[\cos x] = -\sin x$. Both series converge for all $x$ ($R = \infty$).

</details>

---

<details>
<summary><strong>Problem 16 Solution</strong></summary>

**Answer: (B)** $[-2, 4)$

**Work:**

The series is $\sum_{n=1}^{\infty} \frac{(x-1)^n}{n \cdot 3^n}$ with center $a = 1$.

**Ratio Test:**

$$\lim_{n \to \infty} \left|\frac{(x-1)^{n+1}/((n+1) \cdot 3^{n+1})}{(x-1)^n/(n \cdot 3^n)}\right| = \frac{|x-1|}{3} \cdot \lim_{n \to \infty} \frac{n}{n+1} = \frac{|x-1|}{3}$$

Set $\frac{|x-1|}{3} < 1$: $|x-1| < 3$, so $R = 3$.

Open interval: $(1-3, 1+3) = (-2, 4)$.

**Endpoint $x = 4$:** $(x-1)^n = 3^n$, so $\sum \frac{3^n}{n \cdot 3^n} = \sum \frac{1}{n}$ — harmonic series, **diverges**.

**Endpoint $x = -2$:** $(x-1)^n = (-3)^n$, so $\sum \frac{(-3)^n}{n \cdot 3^n} = \sum \frac{(-1)^n}{n}$ — alternating harmonic series, **converges** by AST.

IOC: $[-2, 4)$. **Answer: (B).**

</details>

---

<details>
<summary><strong>Problem 17 Solution</strong></summary>

**Answer: (C)** $\arctan x$

The series $\sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{2n+1} = x - \frac{x^3}{3} + \frac{x^5}{5} - \frac{x^7}{7} + \cdots$

This is the well-known power series for $\arctan x$, derived by integrating the geometric series $\frac{1}{1+x^2} = \sum (-1)^n x^{2n}$ term by term.

- **(A)** $\sin x$ has factorials in the denominator: $\sum \frac{(-1)^n x^{2n+1}}{(2n+1)!}$
- **(B)** $\arcsin x$ has a different form involving double factorials
- **(D)** $\ln(1+x)$ has $x^n/n$, not $x^{2n+1}/(2n+1)$

**Answer: (C).**

</details>

---

<details>
<summary><strong>Problem 18 Solution</strong></summary>

**Answer: (C)** $\sum_{n=1}^{\infty} \frac{n x^{n-1}}{2^n}$

Given $f(x) = \sum_{n=0}^{\infty} \frac{x^n}{2^n}$.

Differentiate term by term:

$$f'(x) = \sum_{n=0}^{\infty} \frac{d}{dx}\left[\frac{x^n}{2^n}\right] = \sum_{n=0}^{\infty} \frac{n x^{n-1}}{2^n}$$

When $n = 0$, the term is $\frac{0 \cdot x^{-1}}{1} = 0$, so the $n = 0$ term contributes nothing. We can start the sum at $n = 1$:

$$f'(x) = \sum_{n=1}^{\infty} \frac{n x^{n-1}}{2^n}$$

Why not the other choices?

- **(A)** is missing the factor of $n$ from the power rule
- **(B)** includes the $n = 0$ term, which is $0$ and normally we start at $n = 1$; however the issue is more subtle — while (B) and (C) are technically equal since the $n=0$ term vanishes, the standard convention is to start at $n = 1$ to avoid the $0 \cdot x^{-1}$ term
- **(D)** is the integral, not the derivative

**Answer: (C).**

</details>

---

<details>
<summary><strong>Problem 19 Solution</strong></summary>

**(a)** Find the radius of convergence.

**Ratio Test:**

$$\lim_{n \to \infty} \left|\frac{(-1)^{n+2} x^{n+1} / ((n+1) \cdot 2^{n+1})}{(-1)^{n+1} x^n / (n \cdot 2^n)}\right| = \frac{|x|}{2} \cdot \lim_{n \to \infty} \frac{n}{n+1} = \frac{|x|}{2}$$

Set $\frac{|x|}{2} < 1$: $|x| < 2$.

$$\boxed{R = 2}$$

**(b)** Determine the full IOC.

Open interval: $(-2, 2)$.

**Endpoint $x = 2$:**

$$\sum_{n=1}^{\infty} \frac{(-1)^{n+1} \cdot 2^n}{n \cdot 2^n} = \sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n} = 1 - \frac{1}{2} + \frac{1}{3} - \cdots$$

This is the alternating harmonic series, which **converges** by the AST ($\frac{1}{n} \to 0$ and is decreasing).

**Endpoint $x = -2$:**

$$\sum_{n=1}^{\infty} \frac{(-1)^{n+1}(-2)^n}{n \cdot 2^n} = \sum_{n=1}^{\infty} \frac{(-1)^{n+1}(-1)^n}{n} = \sum_{n=1}^{\infty} \frac{-1}{n} = -\sum_{n=1}^{\infty} \frac{1}{n}$$

This is the negative harmonic series, which **diverges**.

$$\boxed{\text{IOC: } (-2, 2]}$$

**(c)** Identify the function.

Compare with the known series:

$$\ln(1+u) = \sum_{n=1}^{\infty} \frac{(-1)^{n+1} u^n}{n} \quad \text{for } -1 < u \leq 1$$

Our series is:

$$\sum_{n=1}^{\infty} \frac{(-1)^{n+1} x^n}{n \cdot 2^n} = \sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n} \left(\frac{x}{2}\right)^n$$

This matches the $\ln(1+u)$ series with $u = \frac{x}{2}$:

$$f(x) = \ln\left(1 + \frac{x}{2}\right) = \ln\left(\frac{x + 2}{2}\right)$$

$$\boxed{f(x) = \ln\left(1 + \frac{x}{2}\right)}$$

**(d)** Evaluate the series at $x = 2$.

$$f(2) = \ln\left(1 + \frac{2}{2}\right) = \ln(1 + 1) = \ln 2$$

The series at $x = 2$:

$$\sum_{n=1}^{\infty} \frac{(-1)^{n+1} \cdot 2^n}{n \cdot 2^n} = \sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n} = 1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \cdots$$

$$\boxed{\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n} = \ln 2}$$

This confirms that the alternating harmonic series converges to $\ln 2$.

</details>

---

<details>
<summary><strong>Problem 20 Solution</strong></summary>

**(a)** Find the radius of convergence of $g(x) = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+2}}{(2n+1)(2n+2)}$.

**Ratio Test:** Let $a_n = \frac{(-1)^n x^{2n+2}}{(2n+1)(2n+2)}$.

$$\left|\frac{a_{n+1}}{a_n}\right| = \left|\frac{(-1)^{n+1} x^{2n+4}}{(2n+3)(2n+4)} \cdot \frac{(2n+1)(2n+2)}{(-1)^n x^{2n+2}}\right|$$

$$= |x|^2 \cdot \frac{(2n+1)(2n+2)}{(2n+3)(2n+4)}$$

$$\lim_{n \to \infty} \left|\frac{a_{n+1}}{a_n}\right| = |x|^2 \cdot \lim_{n \to \infty}\frac{(2n+1)(2n+2)}{(2n+3)(2n+4)} = |x|^2 \cdot 1 = x^2$$

Set $x^2 < 1$: $|x| < 1$.

$$\boxed{R = 1}$$

**(b)** Show that $g''(x) = \frac{1}{1+x^2}$.

Differentiate $g(x)$ once:

$$g'(x) = \sum_{n=0}^{\infty} \frac{(-1)^n (2n+2) x^{2n+1}}{(2n+1)(2n+2)} = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+1}}{2n+1}$$

Differentiate again:

$$g''(x) = \sum_{n=0}^{\infty} \frac{(-1)^n (2n+1) x^{2n}}{2n+1} = \sum_{n=0}^{\infty} (-1)^n x^{2n}$$

We recognize this as the geometric series:

$$\sum_{n=0}^{\infty} (-1)^n x^{2n} = \sum_{n=0}^{\infty} (-x^2)^n = \frac{1}{1 - (-x^2)} = \frac{1}{1 + x^2}$$

$$\boxed{g''(x) = \frac{1}{1+x^2}}$$

**(c)** Find a closed form for $g(x)$.

From part (b): $g''(x) = \frac{1}{1+x^2}$

Integrate once:

$$g'(x) = \int \frac{1}{1+x^2}\,dx = \arctan x + C_1$$

Using $g'(0) = 0$ (from the series, $g'(0) = \frac{(-1)^0 \cdot 0^1}{1} = 0$):

$$0 = \arctan 0 + C_1 = 0 + C_1$$

So $C_1 = 0$ and $g'(x) = \arctan x$.

Integrate again:

$$g(x) = \int \arctan x \, dx$$

Using integration by parts (from the [Integration by Parts](/calculus/integration-by-parts) article, Example 4):

$$\int \arctan x \, dx = x \arctan x - \frac{1}{2}\ln(1 + x^2) + C_2$$

Using $g(0) = 0$:

$$0 = 0 \cdot \arctan 0 - \frac{1}{2}\ln 1 + C_2 = 0 - 0 + C_2$$

So $C_2 = 0$.

$$\boxed{g(x) = x\arctan x - \frac{1}{2}\ln(1 + x^2)}$$

**(d)** Evaluate $g(1)$ both ways.

**From the series:**

$$g(1) = \sum_{n=0}^{\infty} \frac{(-1)^n \cdot 1^{2n+2}}{(2n+1)(2n+2)} = \sum_{n=0}^{\infty} \frac{(-1)^n}{(2n+1)(2n+2)}$$

$$= \frac{1}{1 \cdot 2} - \frac{1}{3 \cdot 4} + \frac{1}{5 \cdot 6} - \frac{1}{7 \cdot 8} + \cdots$$

$$= \frac{1}{2} - \frac{1}{12} + \frac{1}{30} - \frac{1}{56} + \cdots$$

**From the closed form:**

$$g(1) = 1 \cdot \arctan 1 - \frac{1}{2}\ln(1 + 1) = \frac{\pi}{4} - \frac{1}{2}\ln 2$$

Both expressions must be equal:

$$\boxed{g(1) = \frac{\pi}{4} - \frac{\ln 2}{2} = \sum_{n=0}^{\infty} \frac{(-1)^n}{(2n+1)(2n+2)}}$$

Numerically: $g(1) = \frac{\pi}{4} - \frac{\ln 2}{2} \approx 0.7854 - 0.3466 \approx 0.4388$.

From the series: $\frac{1}{2} - \frac{1}{12} + \frac{1}{30} - \frac{1}{56} + \cdots \approx 0.5 - 0.0833 + 0.0333 - 0.0179 + \cdots \approx 0.4388$. They match!

This is the kind of beautiful connection between power series and closed-form expressions that makes Ganga's Science Olympiad teammates stop and appreciate the elegance of calculus.

</details>

---

## What's Next

You've just unlocked one of the most powerful ideas in all of calculus: expressing functions as infinite polynomials. Power series let you represent, differentiate, and integrate functions in ways that standard techniques can't touch. You've seen how a single geometric series $\frac{1}{1-x} = \sum x^n$ can be transformed through substitution, differentiation, and integration into series for $\ln(1+x)$, $\arctan x$, and many more.

Next up: [Taylor Series](/calculus/taylor-series), where you'll learn the systematic recipe for building the power series of *any* function around any point. Instead of deriving each series from the geometric series (which is clever but limited), Taylor's formula gives you a direct method — involving the function's derivatives — to generate the coefficients $c_n$ for any differentiable function. It's the difference between improvising a recipe from scratch and having the official Panda Express cookbook that tells you the exact amount of every ingredient.

---

<div align="center">

[← Convergence Tests](/calculus/convergence-tests) | [Taylor Series →](/calculus/taylor-series)

</div>
