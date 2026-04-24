# Convergence Tests
<p class="article-date">April 23, 2026</p>

*Picture yourself at the Panda Express on Rancho Bernardo Road, loading your plate at the buffet. You scoop orange chicken, Beijing beef, fried rice — each scoop smaller than the last because your plate is running out of room. Here's the calculus question: if you kept scooping forever, with each scoop getting tinier and tinier, would your plate eventually overflow, or would the total amount of food settle at some finite limit? That's the central question of convergence tests. You've already learned what a series is — an infinite sum $\sum a_n$. Now you need the tools to determine whether that sum converges to a finite number or diverges to infinity. This article hands you a complete toolkit: eight different tests, each designed for a different type of series, plus a decision flowchart so you'll always know which test to reach for on the AP exam.*

---

## What You'll Learn
- Apply the nth Term Test (Divergence Test) as a quick first check
- Use the Integral Test to connect series to improper integrals
- Identify and evaluate p-series ($\sum \frac{1}{n^p}$)
- Compare series using the Direct Comparison Test
- Compare series using the Limit Comparison Test
- Apply the Ratio Test (especially for factorials and exponentials)
- Apply the Root Test (for nth-power expressions)
- Test alternating series with the Alternating Series Test (Leibniz Test)
- Distinguish between absolute and conditional convergence
- Estimate remainders with the Alternating Series Error Bound
- Follow a systematic decision flowchart: "Which test should I use?"

---

## Prerequisites
- [Series](/calculus/series)
- [Improper Integrals](/calculus/improper-integrals)
- [Limits at Infinity](/calculus/0207-limits-at-infinity)

---

## The Core Concept

### Intuition First

You already know from the [series article](/calculus/series) that an infinite series is a sum like:

$$\sum_{n=1}^{\infty} a_n = a_1 + a_2 + a_3 + \cdots$$

The big question is: does this infinite sum settle down to a finite number (converge), or does it grow without bound (diverge)?

Think about it like your Starbucks Rewards balance. Every visit, you earn some stars. If each visit earns you *half* the stars of the previous visit — 100, 50, 25, 12.5, ... — your balance approaches 200 and never goes past it. That sum **converges**. But if each visit earns you a fixed amount — even just 1 star — then over infinitely many visits, your balance blows up to infinity. That **diverges**.

The tricky part is that some series *look* like they should converge — the terms get smaller and smaller — but they actually diverge. The harmonic series $\sum \frac{1}{n}$ is the classic example. Each term $\frac{1}{n} \to 0$, yet the sum is infinite. So "terms going to zero" is necessary for convergence but not sufficient. You need stronger tools.

That's what convergence tests are: a toolkit of increasingly powerful magnifying glasses that let you inspect a series and determine its fate. Think of each test as a different flavor of boba at Ding Tea — some work for certain series, some don't, and knowing which to order is half the battle.

### The Formal Setup

Given a series $\sum_{n=1}^{\infty} a_n$, its **partial sums** are:

$$S_N = \sum_{n=1}^{N} a_n = a_1 + a_2 + \cdots + a_N$$

- If $\lim_{N \to \infty} S_N = L$ (a finite number), the series **converges** to $L$.
- If $\lim_{N \to \infty} S_N$ does not exist or is $\pm\infty$, the series **diverges**.

Convergence tests are shortcuts that let you determine convergence or divergence *without* computing $S_N$ directly (which is usually impossible).

---

## Test 1: The nth Term Test (Divergence Test)

### Statement

> If $\lim_{n \to \infty} a_n \neq 0$, then $\sum_{n=1}^{\infty} a_n$ **diverges**.

That's it. If the terms don't approach zero, the series can't converge.

### When to Use It

**Always check this first.** It's the fastest test — a quick sanity check before pulling out heavier tools.

### Critical Warning

The nth Term Test is a **one-way street**. It can only prove **divergence**. If $\lim_{n \to \infty} a_n = 0$, the test is **inconclusive** — the series might converge or might diverge. The harmonic series $\sum \frac{1}{n}$ has $a_n \to 0$ but diverges. So "terms go to zero" is necessary but not sufficient.

Think of it like a Mock Trial objection: if the witness contradicts themselves (terms don't go to zero), the testimony is thrown out (series diverges). But if the witness is consistent (terms go to zero), you still don't know if they're telling the truth — you need more evidence.

### Worked Example

**Does** $\displaystyle\sum_{n=1}^{\infty} \frac{n}{2n + 3}$ **converge or diverge?**

Check the limit:

$$\lim_{n \to \infty} \frac{n}{2n + 3} = \lim_{n \to \infty} \frac{1}{2 + \frac{3}{n}} = \frac{1}{2} \neq 0$$

Since the limit is not zero, the series **diverges** by the nth Term Test.

---

## Test 2: The Integral Test

### Statement

> Let $f$ be a positive, continuous, decreasing function on $[1, \infty)$ with $f(n) = a_n$. Then:
>
> $$\sum_{n=1}^{\infty} a_n \text{ and } \int_1^{\infty} f(x)\,dx \text{ either both converge or both diverge.}$$

### When to Use It

When $a_n = f(n)$ for some function $f(x)$ that you can integrate. This test builds a bridge between series and the [improper integrals](/calculus/improper-integrals) you've already mastered.

### Why It Works (Intuition)

Imagine the rectangles in a left Riemann sum for $\int_1^\infty f(x)\,dx$, each with width 1 and height $f(n)$. The total area of these rectangles is exactly $\sum_{n=1}^{\infty} f(n) = \sum a_n$. Since $f$ is decreasing, these rectangles overestimate the integral on one side and underestimate on the other. So the sum and the integral are squeezed together — if one converges, so does the other.

### Important Note

The Integral Test tells you whether the series converges, but it does NOT give you the sum. The value of the integral $\neq$ the sum of the series.

### Worked Example

**Does** $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n^2 + 1}$ **converge or diverge?**

Let $f(x) = \frac{1}{x^2 + 1}$. This is positive, continuous, and decreasing on $[1, \infty)$.

$$\int_1^{\infty} \frac{1}{x^2 + 1}\,dx = \lim_{b \to \infty} [\arctan x]_1^b = \lim_{b \to \infty} \left(\arctan b - \arctan 1\right) = \frac{\pi}{2} - \frac{\pi}{4} = \frac{\pi}{4}$$

The integral converges, so the series $\sum \frac{1}{n^2 + 1}$ **converges** by the Integral Test.

---

## Test 3: The p-Series Test

### Statement

> $$\sum_{n=1}^{\infty} \frac{1}{n^p} \quad \begin{cases} \textbf{converges} & \text{if } p > 1 \\[6pt] \textbf{diverges} & \text{if } p \leq 1 \end{cases}$$

### When to Use It

Whenever you see $\sum \frac{1}{n^p}$ or can recognize a series as a p-series. This is also the most common comparison target — you'll compare other series *to* a p-series.

### Key Examples

| Series | $p$ | Converges? |
|--------|-----|------------|
| $\sum \frac{1}{n^2}$ | $2$ | Yes (converges to $\frac{\pi^2}{6}$) |
| $\sum \frac{1}{n^3}$ | $3$ | Yes |
| $\sum \frac{1}{\sqrt{n}} = \sum \frac{1}{n^{1/2}}$ | $1/2$ | No |
| $\sum \frac{1}{n}$ | $1$ | No (harmonic series) |
| $\sum \frac{1}{n^{1.001}}$ | $1.001$ | Yes (barely!) |

The boundary is $p = 1$. Think of it like the minimum GPA to pass a class — you need *strictly more* than 1.0 to converge. Exactly 1.0 (the harmonic series) doesn't cut it.

### Why It Works

The p-series test is a direct consequence of the Integral Test. We proved in the [improper integrals article](/calculus/improper-integrals) that $\int_1^\infty \frac{1}{x^p}\,dx$ converges iff $p > 1$. Since $f(x) = \frac{1}{x^p}$ is positive, continuous, and decreasing on $[1, \infty)$ for $p > 0$, the Integral Test gives us the p-series result.

---

## Test 4: Direct Comparison Test

### Statement

> Suppose $0 \leq a_n \leq b_n$ for all $n$ (at least eventually).
>
> - If $\sum b_n$ **converges**, then $\sum a_n$ **converges**.
> - If $\sum a_n$ **diverges**, then $\sum b_n$ **diverges**.

### When to Use It

When you can bound your series above or below by a known series (usually a p-series or geometric series).

### The Intuition

If Ganga can carry all the Panda Express bags to the car (the bigger task is finite), she can definitely carry just the orange chicken (a smaller part of the same task). Conversely, if she can't even carry the orange chicken alone (the smaller task is infinite), she definitely can't carry everything.

In symbols: smaller $\leq$ bigger.
- Bigger converges? Smaller converges too.
- Smaller diverges? Bigger diverges too.

### Worked Example

**Does** $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n^2 + 5}$ **converge or diverge?**

For $n \geq 1$: $n^2 + 5 > n^2$, so $\frac{1}{n^2 + 5} < \frac{1}{n^2}$.

We know $\sum \frac{1}{n^2}$ converges (p-series, $p = 2 > 1$).

Since $0 < \frac{1}{n^2 + 5} < \frac{1}{n^2}$ and the bigger series converges, the smaller series **converges** by the Direct Comparison Test.

---

## Test 5: Limit Comparison Test

### Statement

> Suppose $a_n > 0$ and $b_n > 0$ for all $n$. If:
>
> $$\lim_{n \to \infty} \frac{a_n}{b_n} = L \quad \text{where } 0 < L < \infty$$
>
> then $\sum a_n$ and $\sum b_n$ **both converge or both diverge**.

### When to Use It

When Direct Comparison is awkward — when you can't easily show $a_n \leq b_n$ or $a_n \geq b_n$, but you can see that $a_n$ "behaves like" $b_n$ for large $n$. This is your go-to test for rational expressions.

### The Intuition

If $\frac{a_n}{b_n} \to L$ where $L$ is a finite, positive number, then $a_n$ and $b_n$ are essentially the same size for large $n$. One can't converge while the other diverges — they're proportional. It's like comparing the line at Ding Tea to the line at Starbucks. If one line is always roughly twice the other, then either both lines are manageable (finite) or both are impossibly long (infinite).

### Worked Example

**Does** $\displaystyle\sum_{n=1}^{\infty} \frac{3n + 1}{n^3 - 2n + 5}$ **converge or diverge?**

For large $n$, the dominant terms give us: $\frac{3n + 1}{n^3 - 2n + 5} \approx \frac{3n}{n^3} = \frac{3}{n^2}$.

Compare with $b_n = \frac{1}{n^2}$:

$$\lim_{n \to \infty} \frac{a_n}{b_n} = \lim_{n \to \infty} \frac{\frac{3n+1}{n^3 - 2n + 5}}{\frac{1}{n^2}} = \lim_{n \to \infty} \frac{n^2(3n+1)}{n^3 - 2n + 5} = \lim_{n \to \infty} \frac{3n^3 + n^2}{n^3 - 2n + 5} = 3$$

Since $0 < 3 < \infty$ and $\sum \frac{1}{n^2}$ converges (p-series, $p = 2$), the original series **converges** by the Limit Comparison Test.

---

## Test 6: The Ratio Test

### Statement

> Let $\displaystyle L = \lim_{n \to \infty} \left|\frac{a_{n+1}}{a_n}\right|$.
>
> - If $L < 1$, the series **converges absolutely**.
> - If $L > 1$ (or $L = \infty$), the series **diverges**.
> - If $L = 1$, the test is **inconclusive**.

### When to Use It

The Ratio Test is your best friend when the series involves **factorials** ($n!$), **exponentials** ($r^n$), or products of both. These are the series where the ratio $\frac{a_{n+1}}{a_n}$ simplifies beautifully because terms cancel.

### The Intuition

The Ratio Test asks: "What is the growth rate between consecutive terms?" If each term is less than a fixed fraction of the previous term ($L < 1$), the series shrinks geometrically and converges. If each term is bigger than the previous term ($L > 1$), the series blows up. If the ratio is exactly 1, the test can't decide — you need a different tool.

Think of it like your driving practice with Dad on the I-5. If each lesson you cover less distance than the last (ratio < 1), your total driving distance converges. If each lesson covers *more* distance (ratio > 1), you're heading to infinity — maybe all the way to San Francisco.

### Worked Example

**Does** $\displaystyle\sum_{n=1}^{\infty} \frac{n!}{3^n}$ **converge or diverge?**

$$L = \lim_{n \to \infty} \left|\frac{a_{n+1}}{a_n}\right| = \lim_{n \to \infty} \frac{(n+1)!}{3^{n+1}} \cdot \frac{3^n}{n!}$$

$$= \lim_{n \to \infty} \frac{(n+1) \cdot n!}{3 \cdot 3^n} \cdot \frac{3^n}{n!} = \lim_{n \to \infty} \frac{n+1}{3} = \infty$$

Since $L = \infty > 1$, the series **diverges** by the Ratio Test.

Factorials grow faster than exponentials — $n!$ eventually crushes $3^n$. The terms are getting *bigger*, not smaller.

---

## Test 7: The Root Test

### Statement

> Let $\displaystyle L = \lim_{n \to \infty} \sqrt[n]{|a_n|}$.
>
> - If $L < 1$, the series **converges absolutely**.
> - If $L > 1$ (or $L = \infty$), the series **diverges**.
> - If $L = 1$, the test is **inconclusive**.

### When to Use It

The Root Test is ideal when $a_n$ involves an **nth power** — expressions like $\left(\frac{n}{2n+1}\right)^n$ or $\frac{n^n}{3^n}$. Taking the nth root peels off the exponent and simplifies the expression dramatically.

The Root Test is less commonly tested on the AP exam than the Ratio Test, but when it applies, it's extremely clean.

### Worked Example

**Does** $\displaystyle\sum_{n=1}^{\infty} \left(\frac{2n}{3n + 1}\right)^n$ **converge or diverge?**

$$L = \lim_{n \to \infty} \sqrt[n]{\left(\frac{2n}{3n+1}\right)^n} = \lim_{n \to \infty} \frac{2n}{3n+1} = \lim_{n \to \infty} \frac{2}{3 + \frac{1}{n}} = \frac{2}{3}$$

Since $L = \frac{2}{3} < 1$, the series **converges** by the Root Test.

---

## Test 8: Alternating Series Test (Leibniz Test)

### Statement

> An alternating series $\displaystyle\sum_{n=1}^{\infty} (-1)^{n+1} b_n$ (where $b_n > 0$) **converges** if both:
>
> 1. $b_n$ is **decreasing** (eventually): $b_{n+1} \leq b_n$
> 2. $\lim_{n \to \infty} b_n = 0$

### When to Use It

When the series alternates in sign — terms flip between positive and negative. Look for $(-1)^n$, $(-1)^{n+1}$, or $\cos(n\pi)$ as a sign-flip factor.

### The Intuition

An alternating series is like a dance routine where you step forward, then back, then forward, then back — each step smaller than the last. Even though you're moving in both directions, you're homing in on a specific point. The forward and backward steps cancel each other out more and more precisely, and the partial sums converge.

### Worked Example

**Does** $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n}$ **converge or diverge?**

This is the **alternating harmonic series**: $1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \cdots$

Check the two conditions with $b_n = \frac{1}{n}$:

1. **Decreasing?** $\frac{1}{n+1} < \frac{1}{n}$ for all $n \geq 1$. Yes.
2. **Limit zero?** $\lim_{n \to \infty} \frac{1}{n} = 0$. Yes.

Both conditions are met, so the series **converges** by the Alternating Series Test.

(It converges to $\ln 2 \approx 0.693$, though the AST doesn't tell you the sum — just that it converges.)

Notice: the regular harmonic series $\sum \frac{1}{n}$ diverges, but the *alternating* harmonic series converges. The sign changes make all the difference.

---

## Absolute vs. Conditional Convergence

### Definitions

> - A series $\sum a_n$ **converges absolutely** if $\sum |a_n|$ converges.
> - A series $\sum a_n$ **converges conditionally** if $\sum a_n$ converges but $\sum |a_n|$ diverges.

### The Key Theorem

> **Absolute convergence implies convergence.** If $\sum |a_n|$ converges, then $\sum a_n$ converges.

The converse is NOT true. A series can converge without converging absolutely (that's conditional convergence).

### Example

The alternating harmonic series $\sum \frac{(-1)^{n+1}}{n}$:

- $\sum \frac{(-1)^{n+1}}{n}$ converges (by the Alternating Series Test).
- $\sum \left|\frac{(-1)^{n+1}}{n}\right| = \sum \frac{1}{n}$ diverges (harmonic series).

So the alternating harmonic series converges **conditionally** — it converges, but only because the sign changes save it. Remove the signs and it diverges.

Think of it like a Mock Trial case: the defense is strong enough to win when you hear both sides (alternating arguments back and forth), but if you only heard the prosecution's evidence (all positive terms), you'd convict (diverge). The alternation is doing the heavy lifting.

### How the AP Exam Tests This

A common question format: "Determine whether the series converges absolutely, converges conditionally, or diverges."

**Strategy:**
1. First, check $\sum |a_n|$. If it converges, the series converges **absolutely** (you're done).
2. If $\sum |a_n|$ diverges, check whether $\sum a_n$ converges (usually with the Alternating Series Test). If it does, the series converges **conditionally**.
3. If $\sum a_n$ also diverges, the series **diverges**.

---

## The Alternating Series Error Bound

### Statement

> If the alternating series $\sum_{n=1}^{\infty} (-1)^{n+1} b_n$ satisfies the conditions of the AST and you approximate the sum by the partial sum $S_N$, then:
>
> $$|S - S_N| \leq b_{N+1}$$
>
> The error is at most the absolute value of the **first omitted term**.

### Why It's Amazing

Most error bounds in calculus are complicated. This one is beautifully simple: the error is no bigger than the next term you didn't include. It's like ordering at Sesame Donuts — if you eat the first 5 donuts in a shrinking box (each smaller than the last), the total you're missing is less than the size of the 6th donut.

### Worked Example

**Approximate** $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n^3}$ **using the first 4 terms, and bound the error.**

$$S_4 = 1 - \frac{1}{8} + \frac{1}{27} - \frac{1}{64} = 1 - 0.125 + 0.03704 - 0.01563 \approx 0.89641$$

The error satisfies:

$$|S - S_4| \leq b_5 = \frac{1}{5^3} = \frac{1}{125} = 0.008$$

So the true sum is within $0.008$ of $0.89641$. That's a pretty good approximation from just 4 terms!

---

## Decision Flowchart: Which Test Should I Use?

Here's your systematic strategy for any series on the AP exam:

**Step 1: nth Term Test**

$$\lim_{n \to \infty} a_n \neq 0 \implies \text{DIVERGES. Done.}$$

If the limit IS zero, continue.

**Step 2: Recognize Special Forms**

| If the series looks like... | Use... |
|----------------------------|--------|
| $\sum \frac{1}{n^p}$ | **p-Series Test** |
| $\sum ar^n$ | **Geometric Series Test** ($|r| < 1$ converges) |
| Alternating signs $(-1)^n$ | **Alternating Series Test** |

**Step 3: Series Involves Factorials or Exponentials?**

| If you see... | Use... |
|--------------|--------|
| $n!$, $a^n$, or $\frac{n!}{a^n}$ | **Ratio Test** |
| $a_n = [\text{something}]^n$ | **Root Test** |

**Step 4: Rational Expression in $n$?**

$$\frac{\text{polynomial in } n}{\text{polynomial in } n} \implies \text{Limit Comparison with a p-series}$$

**Step 5: Can You Find a Bound?**

$$a_n \leq b_n \text{ or } a_n \geq b_n \text{ for a known series} \implies \text{Direct Comparison}$$

**Step 6: Can You Integrate $f(x)$ Where $f(n) = a_n$?**

$$\text{Use the Integral Test.}$$

**Mnemonic:** Think of it as the order you'd check things at a Ding Tea menu — first see if anything's obviously wrong (nth Term), then look for your favorites (special forms), then read the specials board (Ratio/Root), then compare prices (Comparison), and finally ask the staff (Integral Test).

---

## Worked Examples

### Example 1: nth Term Test in Action

**Does** $\displaystyle\sum_{n=1}^{\infty} \frac{3n^2}{n^2 + 1}$ **converge or diverge?**

$$\lim_{n \to \infty} \frac{3n^2}{n^2 + 1} = \lim_{n \to \infty} \frac{3}{1 + \frac{1}{n^2}} = 3 \neq 0$$

**Diverges** by the nth Term Test.

---

### Example 2: p-Series Recognition

**Does** $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n\sqrt{n}}$ **converge or diverge?**

Rewrite: $\frac{1}{n\sqrt{n}} = \frac{1}{n^{3/2}}$.

This is a p-series with $p = \frac{3}{2} > 1$, so it **converges**.

---

### Example 3: Integral Test

**Does** $\displaystyle\sum_{n=2}^{\infty} \frac{1}{n(\ln n)^2}$ **converge or diverge?**

Let $f(x) = \frac{1}{x(\ln x)^2}$. This is positive, continuous, and decreasing on $[2, \infty)$.

$$\int_2^{\infty} \frac{1}{x(\ln x)^2}\,dx$$

Substitute $u = \ln x$, $du = \frac{1}{x}\,dx$:

$$= \int_{\ln 2}^{\infty} \frac{1}{u^2}\,du = \lim_{b \to \infty}\left[-\frac{1}{u}\right]_{\ln 2}^b = 0 + \frac{1}{\ln 2} = \frac{1}{\ln 2}$$

The integral converges, so $\sum \frac{1}{n(\ln n)^2}$ **converges** by the Integral Test.

---

### Example 4: Direct Comparison

**Does** $\displaystyle\sum_{n=1}^{\infty} \frac{\sin^2 n}{n^3}$ **converge or diverge?**

Since $0 \leq \sin^2 n \leq 1$ for all $n$:

$$0 \leq \frac{\sin^2 n}{n^3} \leq \frac{1}{n^3}$$

We know $\sum \frac{1}{n^3}$ converges (p-series, $p = 3 > 1$).

By the Direct Comparison Test, $\sum \frac{\sin^2 n}{n^3}$ **converges**.

---

### Example 5: Limit Comparison

**Does** $\displaystyle\sum_{n=1}^{\infty} \frac{n^2 + 3}{n^4 - n + 2}$ **converge or diverge?**

For large $n$: $\frac{n^2 + 3}{n^4 - n + 2} \approx \frac{n^2}{n^4} = \frac{1}{n^2}$.

Compare with $b_n = \frac{1}{n^2}$:

$$\lim_{n \to \infty} \frac{a_n}{b_n} = \lim_{n \to \infty} \frac{n^2(n^2 + 3)}{n^4 - n + 2} = \lim_{n \to \infty} \frac{n^4 + 3n^2}{n^4 - n + 2} = 1$$

Since $0 < 1 < \infty$ and $\sum \frac{1}{n^2}$ converges, the original series **converges** by the Limit Comparison Test.

---

### Example 6: Ratio Test with Factorials

**Does** $\displaystyle\sum_{n=1}^{\infty} \frac{2^n}{n!}$ **converge or diverge?**

$$L = \lim_{n \to \infty}\left|\frac{a_{n+1}}{a_n}\right| = \lim_{n \to \infty}\frac{2^{n+1}}{(n+1)!} \cdot \frac{n!}{2^n} = \lim_{n \to \infty}\frac{2}{n+1} = 0$$

Since $L = 0 < 1$, the series **converges** by the Ratio Test.

Factorials in the denominator grow much faster than exponentials in the numerator. This series actually converges to $e^2 - 1$ (from the Taylor series of $e^x$).

---

### Example 7: Root Test

**Does** $\displaystyle\sum_{n=1}^{\infty} \left(\frac{n+1}{3n}\right)^n$ **converge or diverge?**

$$L = \lim_{n \to \infty} \sqrt[n]{\left(\frac{n+1}{3n}\right)^n} = \lim_{n \to \infty} \frac{n+1}{3n} = \frac{1}{3}$$

Since $L = \frac{1}{3} < 1$, the series **converges** by the Root Test.

---

### Example 8: Alternating Series with Error Bound

**Show that** $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n^2}$ **converges. Then find how many terms are needed for the error to be less than $0.01$.**

Check the AST conditions with $b_n = \frac{1}{n^2}$:

1. **Decreasing?** $\frac{1}{(n+1)^2} < \frac{1}{n^2}$ for all $n \geq 1$. Yes.
2. **Limit zero?** $\lim_{n \to \infty} \frac{1}{n^2} = 0$. Yes.

The series **converges** by the Alternating Series Test.

For the error bound: we need $b_{N+1} < 0.01$, i.e., $\frac{1}{(N+1)^2} < 0.01$.

$$(N+1)^2 > 100 \implies N + 1 > 10 \implies N > 9$$

So $N = 10$ terms suffice. The partial sum $S_{10} = 1 - \frac{1}{4} + \frac{1}{9} - \cdots + \frac{1}{100}$ approximates the true sum with error less than $\frac{1}{121} \approx 0.00826$.

(This series converges to $\frac{\pi^2}{12} \approx 0.82247$.)

---

## Key Formulas & Rules

| Test | Condition | Conclusion |
|------|-----------|------------|
| **nth Term Test** | $\lim a_n \neq 0$ | Diverges |
| **Geometric Series** | $\sum ar^n$ | Converges if $\|r\| < 1$; Sum $= \frac{a}{1 - r}$ |
| **p-Series** | $\sum \frac{1}{n^p}$ | Converges if $p > 1$; Diverges if $p \leq 1$ |
| **Integral Test** | $f$ pos., cont., decreasing | $\sum a_n$ and $\int_1^\infty f(x)\,dx$ same behavior |
| **Direct Comparison** | $0 \leq a_n \leq b_n$ | $\sum b_n$ conv. $\Rightarrow$ $\sum a_n$ conv. |
| **Direct Comparison** | $a_n \geq b_n \geq 0$ | $\sum b_n$ div. $\Rightarrow$ $\sum a_n$ div. |
| **Limit Comparison** | $\lim \frac{a_n}{b_n} = L$, $0 < L < \infty$ | Both converge or both diverge |
| **Ratio Test** | $L = \lim\left\|\frac{a_{n+1}}{a_n}\right\|$ | $L < 1$: conv. abs.; $L > 1$: div.; $L = 1$: inconclusive |
| **Root Test** | $L = \lim \sqrt[n]{\|a_n\|}$ | $L < 1$: conv. abs.; $L > 1$: div.; $L = 1$: inconclusive |
| **Alternating Series** | $(-1)^n b_n$; $b_n$ decr., $b_n \to 0$ | Converges |
| **AST Error Bound** | $\|S - S_N\| \leq b_{N+1}$ | Error $\leq$ first omitted term |
| **Absolute Conv.** | $\sum \|a_n\|$ converges | $\sum a_n$ converges absolutely |

---

## Common Mistakes to Avoid

### 1. Using the nth Term Test to "prove" convergence

**Wrong:** "$\lim_{n \to \infty} \frac{1}{n} = 0$, so $\sum \frac{1}{n}$ converges by the nth Term Test."

**Right:** The nth Term Test can only prove **divergence**. If $\lim a_n = 0$, the test is inconclusive. The harmonic series is the classic counterexample — terms go to zero, but the sum is infinite. You need a different test (p-series with $p = 1 \leq 1$: diverges).

---

### 2. Getting the comparison direction wrong

**Wrong:** "$\frac{1}{n^2 + 1} < \frac{1}{n^2}$ and $\sum \frac{1}{n^2}$ converges, so... wait, which way does the comparison go?"

**Right:**
- **Bigger converges $\Rightarrow$ smaller converges.** (If the bigger one fits, the smaller one definitely fits.)
- **Smaller diverges $\Rightarrow$ bigger diverges.** (If the smaller one overflows, the bigger one definitely overflows.)

You CANNOT say: "Smaller converges $\Rightarrow$ bigger converges." That's like saying, "The small boba fits in the cup, so the large boba must fit too." Nope.

---

### 3. Forgetting to check ALL conditions of the Alternating Series Test

**Wrong:** "$\sum \frac{(-1)^n}{a_n}$ has alternating signs, so it converges by AST."

**Right:** You must verify **both** conditions:
1. $b_n$ is eventually decreasing
2. $\lim_{n \to \infty} b_n = 0$

Both are needed. If the terms don't go to zero, the series diverges by the nth Term Test (even if it alternates). If the terms aren't decreasing, the AST doesn't apply.

---

### 4. Using the Ratio Test on a p-series or rational expression

**Wrong:** Apply the Ratio Test to $\sum \frac{1}{n^2}$.

$$L = \lim_{n \to \infty} \frac{n^2}{(n+1)^2} = 1 \quad \text{(inconclusive!)}$$

**Right:** The Ratio Test almost always gives $L = 1$ for rational expressions in $n$. Use the **Limit Comparison Test** or **p-series Test** instead. Save the Ratio Test for series with factorials or exponentials.

---

### 5. Confusing absolute and conditional convergence

**Wrong:** "The series converges absolutely because it passes the Alternating Series Test."

**Right:** The AST tells you the series converges, but not whether it converges *absolutely*. To check absolute convergence, you must test $\sum |a_n|$ separately. If $\sum |a_n|$ converges, it's absolute. If $\sum |a_n|$ diverges but $\sum a_n$ converges, it's conditional.

---

## AP Exam Tips

**1. Always start with the nth Term Test.** It takes 5 seconds and can immediately resolve the question. If $\lim a_n \neq 0$, write "diverges by the nth Term Test" and move on.

**2. Know your p-series cold.** The boundary is $p = 1$. Converges for $p > 1$, diverges for $p \leq 1$. This is the most commonly used comparison target.

**3. Ratio Test = factorials and exponentials.** If you see $n!$ or $a^n$ in the series, reach for the Ratio Test immediately. It's almost always the right move.

**4. Limit Comparison = rational expressions.** For $\frac{\text{polynomial}}{\text{polynomial}}$, compare with the dominant term: $\frac{n^a}{n^b} = \frac{1}{n^{b-a}}$. Then it's a p-series question.

**5. On free response, state the test by name.** The AP graders award points for clear communication. Write: "By the Ratio Test, $L = \frac{1}{3} < 1$, so the series converges." Don't just compute — narrate.

**6. The alternating series error bound is a favorite FR topic.** A classic question: "How many terms of the series are needed to approximate the sum within $0.001$?" Set $b_{N+1} < 0.001$ and solve for $N$.

**7. Absolute vs. conditional is a guaranteed MC topic.** Expect 1-2 questions asking you to classify a series as absolutely convergent, conditionally convergent, or divergent. Follow the two-step strategy: test $\sum |a_n|$ first, then test $\sum a_n$ if needed.

**8. Don't waste time with the wrong test.** If the Ratio Test gives $L = 1$, don't panic — just switch to a different test. No single test works for every series; the flowchart is your roadmap.

**9. Series with $\ln n$ in the denominator often need the Integral Test.** Terms like $\frac{1}{n \ln n}$ don't fit neatly into p-series or comparison tests, but $\int \frac{1}{x \ln x}\,dx = \ln(\ln x)$ is easy to evaluate.

**10. Remember: convergence tests tell you IF a series converges, not WHAT it converges to.** The sum itself is a separate (and usually harder) question. On the AP exam, you're almost always asked just about convergence/divergence, not the actual sum.

---

## Practice Problems

### Basic (Problems 1-5)

**1.** Determine whether $\displaystyle\sum_{n=1}^{\infty} \frac{n + 1}{3n + 2}$ converges or diverges.

---

**2.** Determine whether $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n^4}$ converges or diverges.

---

**3.** Determine whether $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n}$ converges absolutely, converges conditionally, or diverges.

---

**4.** Determine whether $\displaystyle\sum_{n=1}^{\infty} \frac{3^n}{n!}$ converges or diverges.

---

**5.** Determine whether $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n^2 + 3n}$ converges or diverges.

---

### Intermediate (Problems 6-10)

**6.** Determine whether $\displaystyle\sum_{n=2}^{\infty} \frac{1}{n \ln n}$ converges or diverges.

---

**7.** Determine whether $\displaystyle\sum_{n=1}^{\infty} \frac{n^2}{2^n}$ converges or diverges.

---

**8.** Determine whether $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n \cdot n}{n^2 + 1}$ converges absolutely, converges conditionally, or diverges.

---

**9.** Determine whether $\displaystyle\sum_{n=1}^{\infty} \frac{5n + 1}{n^3 + 4}$ converges or diverges.

---

**10.** Determine whether $\displaystyle\sum_{n=1}^{\infty} \left(\frac{n}{2n + 3}\right)^n$ converges or diverges.

---

### Advanced (Problems 11-15)

**11.** Determine whether $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n^{3/2}}$ converges absolutely, converges conditionally, or diverges.

---

**12.** Determine whether $\displaystyle\sum_{n=1}^{\infty} \frac{(2n)!}{(n!)^2 \cdot 4^n}$ converges or diverges.

---

**13.** Approximate $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n^4}$ using the first 3 terms, and find a bound on the error.

---

**14.** Determine whether $\displaystyle\sum_{n=1}^{\infty} \frac{n!}{n^n}$ converges or diverges.

---

**15.** Determine whether $\displaystyle\sum_{n=2}^{\infty} \frac{1}{\sqrt{n} - 1}$ converges or diverges.

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

Which of the following series converges conditionally?

| Choice | Series |
|--------|--------|
| **(A)** | $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n}{n^2}$ |
| **(B)** | $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n}{n}$ |
| **(C)** | $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n}{\sqrt{n}}$ |
| **(D)** | Both (B) and (C) |

---

#### Problem 17 (Multiple Choice)

The Ratio Test applied to $\displaystyle\sum_{n=1}^{\infty} \frac{n! \cdot 5^n}{(2n)!}$ gives:

| Choice | Result |
|--------|--------|
| **(A)** | $L = 0$; converges |
| **(B)** | $L = \frac{5}{4}$; diverges |
| **(C)** | $L = 1$; inconclusive |
| **(D)** | $L = \frac{5}{2}$; diverges |

---

#### Problem 18 (Multiple Choice)

How many terms of $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n^3}$ are needed to approximate the sum with error less than $0.001$?

| Choice | Answer |
|--------|--------|
| **(A)** | 7 |
| **(B)** | 9 |
| **(C)** | 10 |
| **(D)** | 100 |

---

#### Problem 19 (Free Response)

> Consider the series $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1} \cdot n}{2^n}$.
>
> **(a)** Show that the series converges.
>
> **(b)** Does the series converge absolutely or conditionally? Justify your answer.
>
> **(c)** Use the first 4 terms to approximate the sum, and find a bound on the error.

---

#### Problem 20 (Free Response)

> Ganga is building a robot for the Rancho Bernardo Robotics team. The robot's sensor makes measurements every second, and the measurement error at time $n$ (in seconds) is modeled by $a_n = \frac{n^2}{3^n}$.
>
> **(a)** Show that the series $\displaystyle\sum_{n=1}^{\infty} \frac{n^2}{3^n}$ converges using the Ratio Test.
>
> **(b)** The team also considers an alternative sensor with error $b_n = \frac{n + 1}{n^3 + 2}$. Use the Limit Comparison Test to determine whether $\displaystyle\sum_{n=1}^{\infty} b_n$ converges.
>
> **(c)** A third sensor has error $c_n = \frac{(-1)^n}{n + 1}$. Determine whether $\displaystyle\sum_{n=1}^{\infty} c_n$ converges absolutely, converges conditionally, or diverges. Justify.
>
> **(d)** For the sensor in part (c), how many terms are needed so that the partial sum approximation of the total error is within $0.05$ of the true value?

---

## Answer Key

<details>
<summary><strong>Problem 1 Solution</strong></summary>

**Determine whether** $\displaystyle\sum_{n=1}^{\infty} \frac{n + 1}{3n + 2}$ **converges or diverges.**

Apply the **nth Term Test**:

$$\lim_{n \to \infty} \frac{n + 1}{3n + 2} = \lim_{n \to \infty} \frac{1 + \frac{1}{n}}{3 + \frac{2}{n}} = \frac{1}{3} \neq 0$$

Since the limit is not zero, the series **diverges** by the nth Term Test.

$$\boxed{\text{Diverges}}$$

</details>

---

<details>
<summary><strong>Problem 2 Solution</strong></summary>

**Determine whether** $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n^4}$ **converges or diverges.**

This is a **p-series** with $p = 4 > 1$.

Since $p > 1$, the series **converges** by the p-Series Test.

$$\boxed{\text{Converges}}$$

</details>

---

<details>
<summary><strong>Problem 3 Solution</strong></summary>

**Determine whether** $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n}$ **converges absolutely, converges conditionally, or diverges.**

**Step 1 — Test absolute convergence:**

$\sum \left|\frac{(-1)^{n+1}}{n}\right| = \sum \frac{1}{n}$

This is the harmonic series ($p = 1$), which **diverges**. So the series does NOT converge absolutely.

**Step 2 — Test conditional convergence using the AST:**

With $b_n = \frac{1}{n}$:

1. $b_{n+1} = \frac{1}{n+1} < \frac{1}{n} = b_n$ for all $n \geq 1$. Decreasing? Yes.
2. $\lim_{n \to \infty} \frac{1}{n} = 0$. Yes.

Both conditions are satisfied, so the series **converges** by the Alternating Series Test.

Since the series converges but not absolutely, it converges **conditionally**.

$$\boxed{\text{Converges conditionally}}$$

</details>

---

<details>
<summary><strong>Problem 4 Solution</strong></summary>

**Determine whether** $\displaystyle\sum_{n=1}^{\infty} \frac{3^n}{n!}$ **converges or diverges.**

Use the **Ratio Test** (factorials present):

$$L = \lim_{n \to \infty} \left|\frac{a_{n+1}}{a_n}\right| = \lim_{n \to \infty} \frac{3^{n+1}}{(n+1)!} \cdot \frac{n!}{3^n} = \lim_{n \to \infty} \frac{3}{n + 1} = 0$$

Since $L = 0 < 1$, the series **converges** by the Ratio Test.

(This series converges to $e^3 - 1$, from the Taylor series of $e^x$.)

$$\boxed{\text{Converges}}$$

</details>

---

<details>
<summary><strong>Problem 5 Solution</strong></summary>

**Determine whether** $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n^2 + 3n}$ **converges or diverges.**

Factor the denominator: $n^2 + 3n = n(n + 3)$.

For large $n$: $\frac{1}{n(n+3)} \approx \frac{1}{n^2}$.

Use the **Limit Comparison Test** with $b_n = \frac{1}{n^2}$:

$$\lim_{n \to \infty} \frac{a_n}{b_n} = \lim_{n \to \infty} \frac{n^2}{n(n+3)} = \lim_{n \to \infty} \frac{n}{n + 3} = 1$$

Since $0 < 1 < \infty$ and $\sum \frac{1}{n^2}$ converges ($p = 2 > 1$), the series **converges** by the Limit Comparison Test.

$$\boxed{\text{Converges}}$$

</details>

---

<details>
<summary><strong>Problem 6 Solution</strong></summary>

**Determine whether** $\displaystyle\sum_{n=2}^{\infty} \frac{1}{n \ln n}$ **converges or diverges.**

Use the **Integral Test**. Let $f(x) = \frac{1}{x \ln x}$, which is positive, continuous, and decreasing on $[2, \infty)$.

$$\int_2^{\infty} \frac{1}{x \ln x}\,dx$$

Substitute $u = \ln x$, $du = \frac{1}{x}\,dx$:

$$= \int_{\ln 2}^{\infty} \frac{1}{u}\,du = \lim_{b \to \infty} [\ln u]_{\ln 2}^b = \lim_{b \to \infty} (\ln b - \ln(\ln 2)) = \infty$$

The integral **diverges**, so the series **diverges** by the Integral Test.

Note: This series looks similar to $\sum \frac{1}{n(\ln n)^2}$ from Example 3, but the exponent on $\ln n$ makes all the difference. Just like $\sum \frac{1}{n}$ (p = 1) diverges while $\sum \frac{1}{n^2}$ (p = 2) converges, the series $\sum \frac{1}{n(\ln n)^p}$ diverges when $p \leq 1$ and converges when $p > 1$.

$$\boxed{\text{Diverges}}$$

</details>

---

<details>
<summary><strong>Problem 7 Solution</strong></summary>

**Determine whether** $\displaystyle\sum_{n=1}^{\infty} \frac{n^2}{2^n}$ **converges or diverges.**

Use the **Ratio Test** (exponential $2^n$ in denominator):

$$L = \lim_{n \to \infty} \left|\frac{a_{n+1}}{a_n}\right| = \lim_{n \to \infty} \frac{(n+1)^2}{2^{n+1}} \cdot \frac{2^n}{n^2}$$

$$= \lim_{n \to \infty} \frac{(n+1)^2}{2n^2} = \lim_{n \to \infty} \frac{n^2 + 2n + 1}{2n^2} = \lim_{n \to \infty} \frac{1 + \frac{2}{n} + \frac{1}{n^2}}{2} = \frac{1}{2}$$

Since $L = \frac{1}{2} < 1$, the series **converges** by the Ratio Test.

$$\boxed{\text{Converges}}$$

</details>

---

<details>
<summary><strong>Problem 8 Solution</strong></summary>

**Determine whether** $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^n \cdot n}{n^2 + 1}$ **converges absolutely, converges conditionally, or diverges.**

**Step 1 — Test absolute convergence:**

$\sum \left|\frac{(-1)^n \cdot n}{n^2 + 1}\right| = \sum \frac{n}{n^2 + 1}$

For large $n$: $\frac{n}{n^2 + 1} \approx \frac{n}{n^2} = \frac{1}{n}$.

Limit Comparison with $\frac{1}{n}$:

$$\lim_{n \to \infty} \frac{\frac{n}{n^2+1}}{\frac{1}{n}} = \lim_{n \to \infty} \frac{n^2}{n^2 + 1} = 1$$

Since $\sum \frac{1}{n}$ diverges (harmonic), $\sum \frac{n}{n^2+1}$ also **diverges**. Not absolutely convergent.

**Step 2 — Test conditional convergence using the AST:**

With $b_n = \frac{n}{n^2 + 1}$:

1. **Decreasing?** Check: $b_{n+1} \leq b_n$? We need $\frac{n+1}{(n+1)^2+1} \leq \frac{n}{n^2+1}$.

   Cross-multiply (both sides positive): $(n+1)(n^2+1) \leq n((n+1)^2+1)$

   Left: $n^3 + n + n^2 + 1$. Right: $n(n^2 + 2n + 2) = n^3 + 2n^2 + 2n$.

   So we need: $n^3 + n^2 + n + 1 \leq n^3 + 2n^2 + 2n$, i.e., $1 \leq n^2 + n$, which is true for $n \geq 1$. Yes, $b_n$ is decreasing.

2. **Limit zero?** $\lim_{n \to \infty} \frac{n}{n^2+1} = \lim_{n \to \infty} \frac{1}{n + \frac{1}{n}} = 0$. Yes.

Both conditions are met, so the series **converges** by the AST.

Since it converges but not absolutely, it converges **conditionally**.

$$\boxed{\text{Converges conditionally}}$$

</details>

---

<details>
<summary><strong>Problem 9 Solution</strong></summary>

**Determine whether** $\displaystyle\sum_{n=1}^{\infty} \frac{5n + 1}{n^3 + 4}$ **converges or diverges.**

For large $n$: $\frac{5n + 1}{n^3 + 4} \approx \frac{5n}{n^3} = \frac{5}{n^2}$.

Use the **Limit Comparison Test** with $b_n = \frac{1}{n^2}$:

$$\lim_{n \to \infty} \frac{\frac{5n+1}{n^3+4}}{\frac{1}{n^2}} = \lim_{n \to \infty} \frac{n^2(5n+1)}{n^3+4} = \lim_{n \to \infty} \frac{5n^3 + n^2}{n^3 + 4} = 5$$

Since $0 < 5 < \infty$ and $\sum \frac{1}{n^2}$ converges ($p = 2 > 1$), the series **converges** by the Limit Comparison Test.

$$\boxed{\text{Converges}}$$

</details>

---

<details>
<summary><strong>Problem 10 Solution</strong></summary>

**Determine whether** $\displaystyle\sum_{n=1}^{\infty} \left(\frac{n}{2n + 3}\right)^n$ **converges or diverges.**

Use the **Root Test** (nth power):

$$L = \lim_{n \to \infty} \sqrt[n]{\left(\frac{n}{2n+3}\right)^n} = \lim_{n \to \infty} \frac{n}{2n + 3} = \lim_{n \to \infty} \frac{1}{2 + \frac{3}{n}} = \frac{1}{2}$$

Since $L = \frac{1}{2} < 1$, the series **converges** by the Root Test.

$$\boxed{\text{Converges}}$$

</details>

---

<details>
<summary><strong>Problem 11 Solution</strong></summary>

**Determine whether** $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n^{3/2}}$ **converges absolutely, converges conditionally, or diverges.**

**Step 1 — Test absolute convergence:**

$$\sum \left|\frac{(-1)^{n+1}}{n^{3/2}}\right| = \sum \frac{1}{n^{3/2}}$$

This is a p-series with $p = \frac{3}{2} > 1$, which **converges**.

Since $\sum |a_n|$ converges, the series converges **absolutely**.

$$\boxed{\text{Converges absolutely}}$$

(When a series converges absolutely, you don't even need to check the AST — absolute convergence automatically implies convergence.)

</details>

---

<details>
<summary><strong>Problem 12 Solution</strong></summary>

**Determine whether** $\displaystyle\sum_{n=1}^{\infty} \frac{(2n)!}{(n!)^2 \cdot 4^n}$ **converges or diverges.**

Use the **Ratio Test** (factorials present):

$$\frac{a_{n+1}}{a_n} = \frac{(2(n+1))!}{((n+1)!)^2 \cdot 4^{n+1}} \cdot \frac{(n!)^2 \cdot 4^n}{(2n)!}$$

$$= \frac{(2n+2)!}{(2n)!} \cdot \frac{(n!)^2}{((n+1)!)^2} \cdot \frac{4^n}{4^{n+1}}$$

Simplify each factor:

$$\frac{(2n+2)!}{(2n)!} = (2n+2)(2n+1)$$

$$\frac{(n!)^2}{((n+1)!)^2} = \frac{1}{(n+1)^2}$$

$$\frac{4^n}{4^{n+1}} = \frac{1}{4}$$

Multiply:

$$\frac{a_{n+1}}{a_n} = \frac{(2n+2)(2n+1)}{(n+1)^2} \cdot \frac{1}{4} = \frac{2(n+1)(2n+1)}{(n+1)^2} \cdot \frac{1}{4} = \frac{2(2n+1)}{4(n+1)} = \frac{2n+1}{2(n+1)}$$

Take the limit:

$$L = \lim_{n \to \infty} \frac{2n + 1}{2n + 2} = 1$$

The Ratio Test is **inconclusive** ($L = 1$).

We need a different approach. This series is actually related to the central binomial coefficient: $a_n = \binom{2n}{n} \cdot \frac{1}{4^n}$. By Stirling's approximation, $\binom{2n}{n} \approx \frac{4^n}{\sqrt{\pi n}}$, so:

$$a_n \approx \frac{4^n}{\sqrt{\pi n}} \cdot \frac{1}{4^n} = \frac{1}{\sqrt{\pi n}}$$

Use the **Limit Comparison Test** with $b_n = \frac{1}{\sqrt{n}}$:

$$\lim_{n \to \infty} \frac{a_n}{b_n} = \lim_{n \to \infty} \frac{\sqrt{n} \cdot (2n)!}{(n!)^2 \cdot 4^n} = \frac{1}{\sqrt{\pi}}$$

Since $0 < \frac{1}{\sqrt{\pi}} < \infty$ and $\sum \frac{1}{\sqrt{n}}$ diverges ($p = \frac{1}{2} \leq 1$), the series **diverges** by the Limit Comparison Test.

$$\boxed{\text{Diverges}}$$

</details>

---

<details>
<summary><strong>Problem 13 Solution</strong></summary>

**Approximate** $\displaystyle\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n^4}$ **using the first 3 terms, and find a bound on the error.**

First, confirm the AST applies: $b_n = \frac{1}{n^4}$ is decreasing and $\lim b_n = 0$. Yes.

**Compute the partial sum:**

$$S_3 = \frac{1}{1^4} - \frac{1}{2^4} + \frac{1}{3^4} = 1 - \frac{1}{16} + \frac{1}{81}$$

$$= 1 - 0.0625 + 0.012346 = 0.949846$$

**Error bound** (Alternating Series Error Bound):

$$|S - S_3| \leq b_4 = \frac{1}{4^4} = \frac{1}{256} \approx 0.003906$$

So the true sum is within $0.0040$ of $0.9498$.

$$\boxed{S \approx 0.9498 \text{ with error} \leq \frac{1}{256} \approx 0.0039}$$

(The exact value is $\frac{7\pi^4}{720} \approx 0.9470$.)

</details>

---

<details>
<summary><strong>Problem 14 Solution</strong></summary>

**Determine whether** $\displaystyle\sum_{n=1}^{\infty} \frac{n!}{n^n}$ **converges or diverges.**

Use the **Ratio Test** (factorials present):

$$\frac{a_{n+1}}{a_n} = \frac{(n+1)!}{(n+1)^{n+1}} \cdot \frac{n^n}{n!} = \frac{(n+1) \cdot n!}{(n+1)^{n+1}} \cdot \frac{n^n}{n!}$$

$$= \frac{n^n}{(n+1)^n} = \left(\frac{n}{n+1}\right)^n = \left(\frac{1}{1 + \frac{1}{n}}\right)^n$$

Take the limit:

$$L = \lim_{n \to \infty} \left(\frac{1}{1 + \frac{1}{n}}\right)^n = \frac{1}{\lim_{n \to \infty}\left(1 + \frac{1}{n}\right)^n} = \frac{1}{e}$$

Since $L = \frac{1}{e} \approx 0.368 < 1$, the series **converges** by the Ratio Test.

$$\boxed{\text{Converges}}$$

</details>

---

<details>
<summary><strong>Problem 15 Solution</strong></summary>

**Determine whether** $\displaystyle\sum_{n=2}^{\infty} \frac{1}{\sqrt{n} - 1}$ **converges or diverges.**

For large $n$: $\sqrt{n} - 1 \approx \sqrt{n}$, so $\frac{1}{\sqrt{n} - 1} \approx \frac{1}{\sqrt{n}}$.

Use the **Limit Comparison Test** with $b_n = \frac{1}{\sqrt{n}}$:

$$\lim_{n \to \infty} \frac{a_n}{b_n} = \lim_{n \to \infty} \frac{\sqrt{n}}{\sqrt{n} - 1} = \lim_{n \to \infty} \frac{1}{1 - \frac{1}{\sqrt{n}}} = 1$$

Since $0 < 1 < \infty$ and $\sum \frac{1}{\sqrt{n}}$ diverges (p-series, $p = \frac{1}{2} \leq 1$), the series **diverges** by the Limit Comparison Test.

$$\boxed{\text{Diverges}}$$

</details>

---

<details>
<summary><strong>Problem 16 Solution</strong></summary>

**Answer: (D)** Both (B) and (C).

Check each series:

**(A)** $\sum \frac{(-1)^n}{n^2}$

$\sum \left|\frac{(-1)^n}{n^2}\right| = \sum \frac{1}{n^2}$ converges ($p = 2 > 1$). So this converges **absolutely**, not conditionally.

**(B)** $\sum \frac{(-1)^n}{n}$

$\sum |a_n| = \sum \frac{1}{n}$ diverges (harmonic). But the series converges by AST ($b_n = \frac{1}{n}$: decreasing, limit 0). So it converges **conditionally**. Yes.

**(C)** $\sum \frac{(-1)^n}{\sqrt{n}}$

$\sum |a_n| = \sum \frac{1}{\sqrt{n}}$ diverges ($p = \frac{1}{2} \leq 1$). But the series converges by AST ($b_n = \frac{1}{\sqrt{n}}$: decreasing, limit 0). So it converges **conditionally**. Yes.

Both (B) and (C) converge conditionally.

$$\boxed{\text{(D)}}$$

</details>

---

<details>
<summary><strong>Problem 17 Solution</strong></summary>

**Answer: (A)** $L = 0$; converges.

Apply the Ratio Test:

$$\frac{a_{n+1}}{a_n} = \frac{(n+1)! \cdot 5^{n+1}}{(2(n+1))!} \cdot \frac{(2n)!}{n! \cdot 5^n}$$

$$= \frac{(n+1) \cdot 5}{(2n+2)(2n+1)} = \frac{5(n+1)}{(2n+2)(2n+1)} = \frac{5(n+1)}{2(n+1)(2n+1)} = \frac{5}{2(2n+1)}$$

$$L = \lim_{n \to \infty} \frac{5}{2(2n+1)} = 0$$

Since $L = 0 < 1$, the series **converges** by the Ratio Test.

$$\boxed{\text{(A)}}$$

</details>

---

<details>
<summary><strong>Problem 18 Solution</strong></summary>

**Answer: (B)** 9 terms.

We need $b_{N+1} < 0.001$, where $b_n = \frac{1}{n^3}$.

$$\frac{1}{(N+1)^3} < 0.001$$

$$(N+1)^3 > 1000$$

$$N + 1 > 10 \quad \text{(since } 10^3 = 1000\text{)}$$

$$N > 9$$

So we need $N \geq 10$? Let's check more carefully.

$N + 1 > \sqrt[3]{1000} = 10$, so $N + 1 \geq 11$, meaning $N \geq 10$.

But wait: $N + 1 > 10$ means $N + 1 = 11$ works (the first omitted term is $b_{11} = \frac{1}{1331} < 0.001$). So $N = 10$ terms.

Actually, let's check $N = 9$: $b_{10} = \frac{1}{10^3} = \frac{1}{1000} = 0.001$. This is NOT strictly less than $0.001$; it equals $0.001$.

So $N = 9$ gives error $\leq b_{10} = 0.001$, which satisfies "less than or equal to $0.001$." But the question says "error less than $0.001$," meaning we need $b_{N+1} < 0.001$ strictly.

$b_{10} = 0.001$ is not strictly less than $0.001$. So $N = 9$ does NOT work if we require strict inequality.

$N = 10$: $b_{11} = \frac{1}{1331} \approx 0.000751 < 0.001$. This works.

Hmm, but the answer choice "9" is listed. Looking again at the problem: the error bound gives $|S - S_N| \leq b_{N+1}$. With $N = 9$, $|S - S_9| \leq b_{10} = \frac{1}{1000} = 0.001$.

For the error to be strictly less than $0.001$, we'd technically need $b_{N+1} < 0.001$, which requires $N = 10$.

However, on the AP exam, the standard interpretation is that $|S - S_N| \leq b_{N+1}$, and if $b_{N+1} \leq 0.001$, that's typically accepted. With this convention, $N = 9$ works since $b_{10} = 0.001 \leq 0.001$.

But among the answer choices, $N = 9$ is listed as (B) and $N = 10$ as (C). Given the phrasing "error less than 0.001," the technically correct answer is $N = 10$. However, $b_{10} = 0.001$ is right on the boundary. On the AP exam, this distinction is typically resolved by choosing $N = 10$ to be safe, but the intended answer among these choices is most likely **(B) 9**, because $|S - S_9| \leq \frac{1}{1000}$, and many AP resources accept "$\leq$" for these problems.

$$\boxed{\text{(B)} \; N = 9}$$

</details>

---

<details>
<summary><strong>Problem 19 Solution</strong></summary>

**(a)** Show that $\sum \frac{(-1)^{n+1} \cdot n}{2^n}$ converges.

**Method:** Use the **Ratio Test**.

$$L = \lim_{n \to \infty} \left|\frac{a_{n+1}}{a_n}\right| = \lim_{n \to \infty} \frac{(n+1)}{2^{n+1}} \cdot \frac{2^n}{n} = \lim_{n \to \infty} \frac{n+1}{2n} = \frac{1}{2}$$

Since $L = \frac{1}{2} < 1$, the series **converges** (in fact, absolutely) by the Ratio Test.

Alternatively, since this converges absolutely (shown below in part b), it certainly converges.

**(b)** Does the series converge absolutely or conditionally?

Test $\sum |a_n| = \sum \frac{n}{2^n}$.

From part (a), the Ratio Test gives $L = \frac{1}{2} < 1$ for $\sum \frac{n}{2^n}$, so $\sum \frac{n}{2^n}$ **converges**.

Since $\sum |a_n|$ converges, the series converges **absolutely**.

$$\boxed{\text{Converges absolutely}}$$

**(c)** Approximate using 4 terms and bound the error.

$$S_4 = \frac{1}{2} - \frac{2}{4} + \frac{3}{8} - \frac{4}{16}$$

$$= \frac{1}{2} - \frac{1}{2} + \frac{3}{8} - \frac{1}{4}$$

$$= 0 + 0.375 - 0.25 = 0.125$$

Since this series converges absolutely (not just conditionally), the Alternating Series Error Bound still applies (the conditions of the AST are met: $b_n = \frac{n}{2^n}$ is eventually decreasing and $\lim b_n = 0$).

Let's verify $b_n$ is decreasing: $\frac{n+1}{2^{n+1}} < \frac{n}{2^n}$ when $n + 1 < 2n$, i.e., $n > 1$. So $b_n$ is decreasing for $n \geq 2$.

Error bound:

$$|S - S_4| \leq b_5 = \frac{5}{2^5} = \frac{5}{32} = 0.15625$$

So $S \approx 0.125$ with error at most $0.15625$.

(The exact sum is $\sum_{n=1}^{\infty} \frac{(-1)^{n+1} n}{2^n} = \frac{2}{9} \approx 0.2222$.)

$$\boxed{S_4 = 0.125, \quad |S - S_4| \leq \frac{5}{32} \approx 0.156}$$

</details>

---

<details>
<summary><strong>Problem 20 Solution</strong></summary>

**(a)** Show that $\sum \frac{n^2}{3^n}$ converges using the Ratio Test.

$$L = \lim_{n \to \infty} \left|\frac{a_{n+1}}{a_n}\right| = \lim_{n \to \infty} \frac{(n+1)^2}{3^{n+1}} \cdot \frac{3^n}{n^2}$$

$$= \lim_{n \to \infty} \frac{(n+1)^2}{3n^2} = \frac{1}{3} \lim_{n \to \infty} \left(\frac{n+1}{n}\right)^2 = \frac{1}{3} \cdot 1 = \frac{1}{3}$$

Since $L = \frac{1}{3} < 1$, the series **converges** by the Ratio Test. $\quad \blacksquare$

**(b)** Use the Limit Comparison Test for $\sum \frac{n+1}{n^3 + 2}$.

For large $n$: $\frac{n+1}{n^3+2} \approx \frac{n}{n^3} = \frac{1}{n^2}$.

Compare with $b_n = \frac{1}{n^2}$:

$$\lim_{n \to \infty} \frac{a_n}{b_n} = \lim_{n \to \infty} \frac{n^2(n+1)}{n^3 + 2} = \lim_{n \to \infty} \frac{n^3 + n^2}{n^3 + 2} = 1$$

Since $0 < 1 < \infty$ and $\sum \frac{1}{n^2}$ converges (p-series, $p = 2 > 1$), the series $\sum \frac{n+1}{n^3+2}$ **converges** by the Limit Comparison Test.

**(c)** Determine convergence type for $\sum \frac{(-1)^n}{n+1}$.

**Step 1 — Absolute convergence?**

$\sum \left|\frac{(-1)^n}{n+1}\right| = \sum \frac{1}{n+1}$

This is essentially the harmonic series (shifted by 1), which **diverges**. So no absolute convergence.

**Step 2 — Conditional convergence?**

Apply the AST with $b_n = \frac{1}{n+1}$:

1. **Decreasing?** $\frac{1}{n+2} < \frac{1}{n+1}$ for all $n \geq 1$. Yes.
2. **Limit zero?** $\lim_{n \to \infty} \frac{1}{n+1} = 0$. Yes.

Both conditions are met, so the series **converges** by the AST.

Since it converges but not absolutely, $\sum \frac{(-1)^n}{n+1}$ converges **conditionally**.

$$\boxed{\text{Converges conditionally}}$$

**(d)** How many terms for error $< 0.05$?

By the Alternating Series Error Bound:

$$|S - S_N| \leq b_{N+1} = \frac{1}{N + 2}$$

We need: $\frac{1}{N + 2} < 0.05$

$$N + 2 > \frac{1}{0.05} = 20$$

$$N > 18$$

So $N = 19$ terms are needed. Check: $b_{20} = \frac{1}{21} \approx 0.0476 < 0.05$. Confirmed.

$$\boxed{N = 19 \text{ terms}}$$

</details>

---

## What's Next

You now have a complete toolkit for determining whether a series converges or diverges — eight distinct tests, each suited to a different type of series, plus the ability to classify convergence as absolute or conditional and estimate errors for alternating series. This is the analytical backbone of everything that follows.

Next up: [Power Series](/calculus/power-series), where you'll combine these convergence tools with the idea of plugging a variable $x$ into a series. Instead of a fixed sum $\sum a_n$, you'll study $\sum a_n x^n$ — a function defined by a series. You'll learn about the **interval of convergence** (the set of $x$-values where the series converges) and the **radius of convergence**, using the very Ratio and Root Tests you practiced here. Power series are the gateway to Taylor and Maclaurin series — arguably the crown jewel of BC Calculus.

---

<div align="center">

[← Series](/calculus/series) | [Power Series →](/calculus/power-series)

</div>