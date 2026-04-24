# Sequences
<p class="article-date">April 23, 2026</p>

*Think about your morning Starbucks cold frappe order. Monday: grande. Tuesday: grande. Wednesday: you switch to venti because finals week hit different. Thursday: back to grande. Friday: treat yourself, trenta. Each day produces a single drink size — one value per day, lined up in order. That's a sequence. It's one of the simplest objects in all of mathematics: a list of numbers, one after another, following some pattern. But here's the question that launches an entire unit of BC Calculus: if you keep going forever, does your list settle down to some final value, or does it spiral off into oblivion? That question — what happens at infinity — is the gateway to everything in Unit 10. Series, convergence tests, Taylor polynomials, power series — all of it starts right here, with sequences. So grab your boba from Ding Tea, settle in, and let's build the foundation.*

---

## What You'll Learn
- Define a sequence and use proper notation ($\{a_n\}$, $a_n$)
- Write explicit and recursive formulas for sequences
- Determine whether a sequence converges or diverges
- Compute limits of sequences using limit laws, L'Hopital's Rule, and the Squeeze Theorem
- Classify sequences as bounded, unbounded, monotonic (increasing/decreasing)
- Apply the Monotone Convergence Theorem
- Rank growth rates: logarithmic < polynomial < exponential < factorial
- Analyze recursive sequences and find fixed points
- Recognize arithmetic, geometric, factorial, and alternating sequences
- Connect the limit of a sequence to the limit of a continuous function

---

## Prerequisites
- [Limits at Infinity](/calculus/0207-limits-at-infinity)
- [Exponential Functions](/calculus/0111-exponential-functions)
- [Logarithmic Functions](/calculus/0112-logarithmic-functions)

---

## The Core Concept

### Intuition First

You already understand sequences — you just might not realize it.

Every playlist on your phone is a sequence. Song 1, Song 2, Song 3, ... Each song has a position number (its index) and a value (the song itself). A sequence in math works the same way: it assigns a value to each positive integer.

Here's another way to think about it. Imagine you're learning to drive with Dad on the streets near Rancho Bernardo. Each day, Dad measures how close you park to the curb (in inches):

$$12, \, 8, \, 5, \, 3, \, 2, \, 1.5, \, 1.2, \, 1.1, \, 1.05, \, \ldots$$

Day after day, your parking gets better. The numbers are getting closer and closer to... what? To some small number near 1. We'd say this sequence **converges** — it settles toward a definite target. If instead your distances were $12, 15, 20, 28, 40, \ldots$, you'd be getting *worse* every day (yikes), and the sequence would **diverge** — it blows up to infinity with no target in sight.

That's the entire heart of this topic: **does the list of numbers approach a specific value as you go further and further out, or doesn't it?**

### The Formal Definition

A **sequence** is a function whose domain is the set of positive integers (or sometimes non-negative integers). We write it as:

$$\{a_n\} = \{a_1, a_2, a_3, \ldots\} \quad \text{or} \quad \{a_n\}_{n=1}^{\infty}$$

Each $a_n$ is called a **term** of the sequence, and $n$ is the **index**.

**Examples:**
- $a_n = \frac{1}{n}$: the sequence is $\left\{1, \frac{1}{2}, \frac{1}{3}, \frac{1}{4}, \ldots\right\}$
- $a_n = (-1)^n$: the sequence is $\{-1, 1, -1, 1, \ldots\}$
- $a_n = 2^n$: the sequence is $\{2, 4, 8, 16, \ldots\}$

### Explicit vs. Recursive Formulas

An **explicit formula** gives $a_n$ directly in terms of $n$:

$$a_n = 3n + 1 \quad \Rightarrow \quad a_1 = 4, \; a_2 = 7, \; a_3 = 10, \ldots$$

A **recursive formula** defines each term using previous terms, plus an initial condition:

$$a_1 = 2, \quad a_{n+1} = 3a_n - 1 \quad \Rightarrow \quad a_1 = 2, \; a_2 = 5, \; a_3 = 14, \ldots$$

Recursive formulas are like cooking with leftovers — today's meal is built from yesterday's. Explicit formulas let you jump straight to any term without computing all the ones before it.

### Convergence and Divergence

This is the big question.

> **Definition:** A sequence $\{a_n\}$ **converges** to a limit $L$ if the terms $a_n$ get arbitrarily close to $L$ as $n \to \infty$. We write:
>
> $$\lim_{n \to \infty} a_n = L$$
>
> If no such $L$ exists, the sequence **diverges**.

Formally (the $\varepsilon$-definition you'll see in textbooks): for every $\varepsilon > 0$, there exists an integer $N$ such that $|a_n - L| < \varepsilon$ whenever $n > N$. Translation: no matter how tiny a "target zone" you draw around $L$, eventually *all* the terms land inside it and stay there forever.

**Examples:**
- $a_n = \frac{1}{n} \to 0$ (converges)
- $a_n = (-1)^n$ diverges (bounces between $-1$ and $1$ forever, never settling)
- $a_n = 5 - \frac{3}{n^2} \to 5$ (converges)
- $a_n = n^2$ diverges (grows without bound)

### The Bridge: Sequences and Continuous Functions

Here's a powerful tool. If $f(x)$ is a continuous function and $a_n = f(n)$, then:

$$\boxed{\text{If } \lim_{x \to \infty} f(x) = L, \text{ then } \lim_{n \to \infty} a_n = L}$$

This lets you use everything you already know about limits of functions — including [L'Hopital's Rule](/calculus/0207-limits-at-infinity) — to evaluate limits of sequences. Just replace $n$ with $x$, find the limit of the continuous function, and that's your sequence limit.

**Warning:** The converse is not always true. A sequence can converge even if the corresponding continuous function doesn't have a limit (e.g., $a_n = \sin(2\pi n) = 0$ for all integers $n$, but $\lim_{x\to\infty}\sin(2\pi x)$ doesn't exist). However, for the AP exam, the forward direction is what you'll use.

### Bounded and Monotonic Sequences

These concepts help you prove convergence even when you can't find the exact limit.

**Bounded:**
- A sequence is **bounded above** if there exists $M$ such that $a_n \leq M$ for all $n$.
- A sequence is **bounded below** if there exists $m$ such that $a_n \geq m$ for all $n$.
- A sequence is **bounded** if it's both bounded above and bounded below.

**Monotonic:**
- A sequence is **increasing** (or non-decreasing) if $a_{n+1} \geq a_n$ for all $n$.
- A sequence is **decreasing** (or non-increasing) if $a_{n+1} \leq a_n$ for all $n$.
- A sequence is **monotonic** if it's either increasing or decreasing.

### The Monotone Convergence Theorem

$$\boxed{\text{If a sequence is both bounded and monotonic, then it converges.}}$$

This is one of the most important theorems in analysis. Think about it intuitively: if a sequence keeps going up (monotonic increasing) but has a ceiling it can never break through (bounded above), it *must* settle down to some value — it has nowhere else to go. It's like filling your Ding Tea cup drop by drop. The liquid level keeps rising (monotonic increasing) but can't exceed the rim of the cup (bounded above). Eventually the level approaches the top and stabilizes.

The theorem guarantees a limit *exists* but doesn't tell you what it is. You still need other techniques to find the actual value.

### The Squeeze Theorem for Sequences

If $b_n \leq a_n \leq c_n$ for all $n$ (at least beyond some index), and $\lim_{n\to\infty} b_n = \lim_{n\to\infty} c_n = L$, then:

$$\boxed{\lim_{n \to \infty} a_n = L}$$

Same idea as the Squeeze Theorem for functions — trap the sequence between two others that converge to the same limit, and the middle one has no choice but to converge there too. Like being squeezed between two friends walking toward Panda Express — you're going to Panda Express whether you planned to or not.

### Growth Rate Hierarchy

When sequences involve combinations of logarithms, polynomials, exponentials, and factorials, this hierarchy tells you which one "wins" as $n \to \infty$:

$$\boxed{\ln n \ll n^p \ll b^n \ll n! \ll n^n}$$

where $p > 0$ and $b > 1$. The symbol $\ll$ means "grows much slower than."

In practical terms:
- $\frac{\ln n}{n} \to 0$ (polynomial beats logarithm)
- $\frac{n^{100}}{2^n} \to 0$ (exponential beats any polynomial, even $n^{100}$)
- $\frac{3^n}{n!} \to 0$ (factorial beats any exponential)
- $\frac{n!}{n^n} \to 0$ ($n^n$ beats factorial)

Think of it like a speed race on the I-5: $\ln n$ is the bicycle, $n^p$ is the sedan, $b^n$ is the sports car, and $n!$ is the jet. No matter how big a head start the bicycle gets, the jet eventually leaves it in the dust.

---

## Worked Examples

### Example 1: Basic Limit of a Rational Sequence

**Problem:** Find $\displaystyle\lim_{n \to \infty} \frac{3n^2 + 5}{7n^2 - 2n}$.

**Solution:**

This is a rational expression in $n$. Just like with limits at infinity for functions, divide numerator and denominator by the highest power of $n$ (which is $n^2$):

$$\lim_{n \to \infty} \frac{3n^2 + 5}{7n^2 - 2n} = \lim_{n \to \infty} \frac{3 + \frac{5}{n^2}}{7 - \frac{2}{n}}$$

As $n \to \infty$, $\frac{5}{n^2} \to 0$ and $\frac{2}{n} \to 0$:

$$= \frac{3 + 0}{7 - 0} = \boxed{\frac{3}{7}}$$

**Rule of thumb:** For a ratio of two polynomials of the same degree, the limit is the ratio of the leading coefficients. Same degree = divide the top coefficients.

---

### Example 2: Limit Using L'Hopital's Rule

**Problem:** Find $\displaystyle\lim_{n \to \infty} \frac{\ln n}{n}$.

**Solution:**

Direct substitution gives $\frac{\infty}{\infty}$, which is indeterminate. Replace $n$ with the continuous variable $x$ and apply L'Hopital's Rule:

$$\lim_{x \to \infty} \frac{\ln x}{x} = \lim_{x \to \infty} \frac{\frac{1}{x}}{1} = \lim_{x \to \infty} \frac{1}{x} = 0$$

Since the continuous function limit is $0$, the sequence limit is also:

$$\boxed{\lim_{n \to \infty} \frac{\ln n}{n} = 0}$$

This confirms the growth rate hierarchy: logarithms grow slower than polynomials. No matter how slowly $n$ grows compared to, say, $n^2$, the plain old $n$ still crushes $\ln n$ in the long run.

---

### Example 3: Geometric Sequences

**Problem:** Determine convergence of $a_n = \left(\frac{2}{3}\right)^n$.

**Solution:**

This is a geometric sequence with ratio $r = \frac{2}{3}$. For a geometric sequence $a_n = r^n$:

- If $|r| < 1$: the sequence converges to $0$
- If $|r| = 1$: the sequence is $1, 1, 1, \ldots$ (if $r=1$) or $-1, 1, -1, \ldots$ (if $r = -1$, diverges)
- If $|r| > 1$: the sequence diverges

Since $|r| = \frac{2}{3} < 1$:

$$\lim_{n \to \infty} \left(\frac{2}{3}\right)^n = \boxed{0}$$

Each term is $\frac{2}{3}$ of the previous one. The terms shrink like your mint chocolate chip ice cream scoop on a hot day at Coronado beach — each moment, it's a fraction of what it was before, heading steadily toward zero.

---

### Example 4: The Squeeze Theorem in Action

**Problem:** Find $\displaystyle\lim_{n \to \infty} \frac{\sin n}{n}$.

**Solution:**

We can't use L'Hopital's Rule here because $\sin n$ doesn't approach infinity — it just oscillates. But we know:

$$-1 \leq \sin n \leq 1 \quad \text{for all } n$$

Divide everything by $n$ (which is positive):

$$-\frac{1}{n} \leq \frac{\sin n}{n} \leq \frac{1}{n}$$

Since $\lim_{n\to\infty} \left(-\frac{1}{n}\right) = 0$ and $\lim_{n\to\infty} \frac{1}{n} = 0$, the Squeeze Theorem gives:

$$\boxed{\lim_{n \to \infty} \frac{\sin n}{n} = 0}$$

The oscillation of $\sin n$ is irrelevant — the $\frac{1}{n}$ factor crushes it to zero.

---

### Example 5: Alternating Sequence with Decay

**Problem:** Determine whether $a_n = \frac{(-1)^n}{n^2}$ converges or diverges. If it converges, find the limit.

**Solution:**

The $(-1)^n$ factor makes the terms alternate in sign:

$$a_1 = -1, \quad a_2 = \frac{1}{4}, \quad a_3 = -\frac{1}{9}, \quad a_4 = \frac{1}{16}, \quad \ldots$$

Even though the terms flip between positive and negative, their *magnitude* is $\frac{1}{n^2}$, which shrinks to zero. We can use the Squeeze Theorem:

$$-\frac{1}{n^2} \leq \frac{(-1)^n}{n^2} \leq \frac{1}{n^2}$$

Both bounds go to $0$, so:

$$\boxed{\lim_{n \to \infty} \frac{(-1)^n}{n^2} = 0}$$

**Key insight:** An alternating sequence can still converge — as long as the magnitude of the terms approaches zero. Compare this with $(-1)^n$ (no decay factor), which diverges because the terms bounce between $-1$ and $1$ forever.

---

### Example 6: Exponential vs. Polynomial — L'Hopital's Rule (Repeated)

**Problem:** Find $\displaystyle\lim_{n \to \infty} \frac{n^3}{e^n}$.

**Solution:**

Direct substitution: $\frac{\infty}{\infty}$, indeterminate. Replace $n$ with $x$ and apply L'Hopital's Rule repeatedly:

$$\lim_{x \to \infty} \frac{x^3}{e^x} \stackrel{\text{L'H}}{=} \lim_{x \to \infty} \frac{3x^2}{e^x} \stackrel{\text{L'H}}{=} \lim_{x \to \infty} \frac{6x}{e^x} \stackrel{\text{L'H}}{=} \lim_{x \to \infty} \frac{6}{e^x} = 0$$

Each application of L'Hopital's reduces the polynomial degree by 1, while $e^x$ remains $e^x$. Eventually the numerator becomes a constant and the denominator is still $e^x \to \infty$.

$$\boxed{\lim_{n \to \infty} \frac{n^3}{e^n} = 0}$$

This is the growth rate hierarchy in action: exponential crushes polynomial, always. Even $n^{1000}$ would lose to $e^n$ — you'd just need 1000 applications of L'Hopital's Rule.

---

### Example 7: A Sequence Defined by $n$-th Roots

**Problem:** Find $\displaystyle\lim_{n \to \infty} n^{1/n}$.

**Solution:**

Let $a_n = n^{1/n}$. Take the natural log:

$$\ln a_n = \frac{\ln n}{n}$$

We showed in Example 2 that $\frac{\ln n}{n} \to 0$. Therefore:

$$\lim_{n \to \infty} \ln a_n = 0$$

Since the exponential function is continuous:

$$\lim_{n \to \infty} a_n = e^0 = \boxed{1}$$

This is a classic and surprising result. Even though $n$ grows without bound, the $n$-th root "tames" it so effectively that $n^{1/n} \to 1$. Similarly, $(2n)^{1/n} \to 1$, and in general $c^{1/n} \to 1$ for any constant $c > 0$. The $n$-th root is an incredibly powerful compressor.

---

### Example 8: Recursive Sequence and Fixed Points

**Problem:** The sequence $\{a_n\}$ is defined by $a_1 = 2$ and $a_{n+1} = \frac{1}{2}\left(a_n + \frac{6}{a_n}\right)$. Assuming the sequence converges, find its limit.

**Solution:**

This is the Babylonian method (also called Newton's method) for computing $\sqrt{6}$. Let's see why.

**Step 1: Assume the limit exists.** Let $\lim_{n\to\infty} a_n = L$.

**Step 2: Take the limit of both sides** of the recursion:

$$\lim_{n\to\infty} a_{n+1} = \lim_{n\to\infty} \frac{1}{2}\left(a_n + \frac{6}{a_n}\right)$$

Since $a_{n+1} \to L$ and $a_n \to L$:

$$L = \frac{1}{2}\left(L + \frac{6}{L}\right)$$

**Step 3: Solve for $L$.**

$$2L = L + \frac{6}{L}$$

$$L = \frac{6}{L}$$

$$L^2 = 6$$

$$L = \sqrt{6} \quad (\text{taking the positive root since all terms are positive})$$

$$\boxed{L = \sqrt{6} \approx 2.449}$$

**What's a fixed point?** A fixed point of the recursion $a_{n+1} = f(a_n)$ is a value $L$ where $f(L) = L$. At a fixed point, the sequence "stays put" — if it ever reaches $L$, it stays there forever. We just found that the fixed point of $f(x) = \frac{1}{2}\left(x + \frac{6}{x}\right)$ is $x = \sqrt{6}$.

Let's verify with a few terms: $a_1 = 2$, $a_2 = \frac{1}{2}(2 + 3) = 2.5$, $a_3 = \frac{1}{2}(2.5 + 2.4) = 2.45$, $a_4 \approx 2.44949$. That's converging to $\sqrt{6} \approx 2.44949$ incredibly fast.

---

### Example 9: Factorial vs. Exponential

**Problem:** Show that $\displaystyle\lim_{n \to \infty} \frac{2^n}{n!} = 0$.

**Solution:**

We can't directly use L'Hopital's Rule (factorials aren't differentiable in the usual sense). Instead, let's use a bounding argument.

Write out the terms of $\frac{2^n}{n!}$:

$$\frac{2^n}{n!} = \frac{2 \cdot 2 \cdot 2 \cdots 2}{1 \cdot 2 \cdot 3 \cdots n}$$

For $n \geq 3$, each factor $\frac{2}{k}$ (where $k \geq 3$) is at most $\frac{2}{3}$:

$$\frac{2^n}{n!} = \frac{2}{1} \cdot \frac{2}{2} \cdot \frac{2}{3} \cdot \frac{2}{4} \cdots \frac{2}{n} \leq 2 \cdot 1 \cdot \underbrace{\frac{2}{3} \cdot \frac{2}{3} \cdots \frac{2}{3}}_{n - 2 \text{ factors}} = 2 \left(\frac{2}{3}\right)^{n-2}$$

Since $\left(\frac{2}{3}\right)^{n-2} \to 0$ (geometric decay), the bound squeezes $\frac{2^n}{n!}$ to zero:

$$0 \leq \frac{2^n}{n!} \leq 2\left(\frac{2}{3}\right)^{n-2} \to 0$$

$$\boxed{\lim_{n \to \infty} \frac{2^n}{n!} = 0}$$

Factorial growth demolishes exponential growth. Think of it this way: $2^n$ multiplies by $2$ each step, but $n!$ multiplies by $n$ each step — and $n$ keeps getting bigger. By $n = 10$, you're multiplying by $10$ in the denominator but only $2$ in the numerator. The factorial runs away.

---

### Example 10: Bounded and Monotonic — Proving Convergence

**Problem:** Show that $a_n = \frac{n}{n+1}$ is bounded and monotonic, and find its limit.

**Solution:**

**Bounded:** For all $n \geq 1$:

$$a_n = \frac{n}{n+1} = 1 - \frac{1}{n+1}$$

Since $\frac{1}{n+1} > 0$, we have $a_n < 1$ (bounded above by 1). Since $n \geq 1$ and $n+1 > 0$, we have $a_n > 0$ (bounded below by 0). So $0 < a_n < 1$ — the sequence is bounded.

**Monotonic:** Check if $a_{n+1} > a_n$:

$$a_{n+1} - a_n = \frac{n+1}{n+2} - \frac{n}{n+1} = \frac{(n+1)^2 - n(n+2)}{(n+2)(n+1)}$$

$$= \frac{n^2 + 2n + 1 - n^2 - 2n}{(n+2)(n+1)} = \frac{1}{(n+2)(n+1)} > 0$$

Since $a_{n+1} - a_n > 0$ for all $n$, the sequence is **strictly increasing**.

**By the Monotone Convergence Theorem**, the sequence converges.

**Finding the limit:**

$$\lim_{n \to \infty} \frac{n}{n+1} = \lim_{n \to \infty} \frac{1}{1 + \frac{1}{n}} = \frac{1}{1+0} = \boxed{1}$$

The sequence approaches 1 from below but never reaches it — like endlessly walking halfway to the Panda Express counter. You get closer and closer, but (in this mathematical idealization) never quite arrive. Of course, in real life you'd just walk over and order your orange chicken.

---

## Key Formulas & Rules

| Concept | Formula / Rule |
|---------|---------------|
| Sequence notation | $\{a_n\}_{n=1}^{\infty}$, individual term is $a_n$ |
| Convergence | $\lim_{n\to\infty} a_n = L$ (finite number) |
| Divergence | $\lim_{n\to\infty} a_n$ does not exist or is $\pm\infty$ |
| Arithmetic sequence | $a_n = a_1 + (n-1)d$ (always diverges unless $d = 0$) |
| Geometric sequence | $a_n = a_1 \cdot r^{n-1}$; converges iff $\|r\| < 1$ (limit $= 0$) or $r = 1$ (limit $= a_1$) |
| Continuous function bridge | If $\lim_{x\to\infty} f(x) = L$ and $a_n = f(n)$, then $\lim_{n\to\infty} a_n = L$ |
| L'Hopital's for sequences | Replace $n$ with $x$, apply L'Hopital's to $\frac{f(x)}{g(x)}$ |
| Squeeze Theorem | If $b_n \leq a_n \leq c_n$ and $b_n, c_n \to L$, then $a_n \to L$ |
| Monotone Convergence Theorem | Bounded + Monotonic $\Rightarrow$ Convergent |
| Growth rate hierarchy | $\ln n \ll n^p \ll b^n \ll n! \ll n^n$ (for $p > 0$, $b > 1$) |
| $n$-th root limit | $\lim_{n\to\infty} n^{1/n} = 1$ |
| Important limit | $\lim_{n\to\infty}\left(1 + \frac{1}{n}\right)^n = e$ |
| Fixed point of recursion | If $a_{n+1} = f(a_n)$ and $a_n \to L$, then $L = f(L)$ |

---

## Common Mistakes to Avoid

### 1. Confusing sequences with series

**Wrong:** "The sequence $\frac{1}{n}$ converges to $0$, so $\sum \frac{1}{n}$ converges."

**Right:** A sequence is a **list** of numbers; a series is a **sum** of numbers. The sequence $\{1/n\}$ does converge to $0$, but the series $\sum 1/n$ (the harmonic series) diverges to infinity. Convergence of the sequence $a_n \to 0$ is *necessary* for the series to converge, but it's not *sufficient*. You'll explore this deeply in the next article on [Series](/calculus/series).

---

### 2. Applying L'Hopital's Rule directly to $n$ instead of $x$

**Wrong:** $\lim_{n\to\infty} \frac{n}{e^n}$, then differentiate with respect to $n$: "$\frac{d}{dn}(n) = 1$."

**Right:** Replace $n$ with the continuous variable $x$ first, then apply L'Hopital's Rule to $\lim_{x\to\infty} \frac{x}{e^x}$. L'Hopital's Rule requires functions that are differentiable on an interval — sequences are defined only at integer inputs. The bridge theorem lets you move from $n$ to $x$ safely.

---

### 3. Forgetting that $(-1)^n$ diverges

**Wrong:** "$(-1)^n$ is bounded between $-1$ and $1$, so it converges."

**Right:** Bounded does *not* imply convergent by itself. The sequence $(-1)^n = -1, 1, -1, 1, \ldots$ is bounded but **not monotonic** — it oscillates forever and never settles on a single value. You need bounded AND monotonic for the Monotone Convergence Theorem.

---

### 4. Assuming convergence of a recursive sequence without verification

**Wrong:** Defining $a_{n+1} = 2a_n$ with $a_1 = 1$ and assuming it converges. "Let $L$ be the limit, then $L = 2L$, so $L = 0$."

**Right:** The sequence $1, 2, 4, 8, 16, \ldots$ obviously diverges to infinity. The "fixed point" technique only works *after* you've established that the sequence actually converges. Always check boundedness and monotonicity (or use another argument) before using the fixed-point method.

---

### 5. Misranking growth rates

**Wrong:** "Since $100^n > n^{100}$ for small $n$, we have $100^n > n^{100}$ for all $n$."

**Right:** For large $n$, $n^{100}$ is polynomial and $100^n$ is exponential. The exponential *eventually* wins, so $\frac{n^{100}}{100^n} \to 0$, meaning $100^n$ does dominate. But be careful with the direction of the comparison — the issue is knowing *which* function is in the numerator and which is in the denominator. Also, $n^n$ beats $n!$, which beats $b^n$, which beats $n^p$, which beats $\ln n$. Don't mix up the order.

---

### 6. Using the Monotone Convergence Theorem when the sequence isn't monotonic

**Wrong:** "$a_n = \frac{(-1)^n}{n}$ is bounded, so by the Monotone Convergence Theorem it converges."

**Right:** The sequence $\frac{(-1)^n}{n}$ is bounded but **not monotonic** (it alternates). The Monotone Convergence Theorem does not apply. (This sequence does converge to $0$, but you need the Squeeze Theorem to prove it, not the MCT.)

---

## AP Exam Tips

### For BC Students:

1. **Sequences are the gateway to series.** While the AP exam rarely asks a standalone "find the limit of this sequence" problem, understanding convergence of sequences is *essential* for every convergence test you'll learn. The nth-Term Test, Ratio Test, and Root Test all rely on sequence limits. Master this topic, and series become dramatically easier.

2. **L'Hopital's Rule on sequences is a favorite.** When you see $\frac{n^2}{\ln n}$, $\frac{e^n}{n^5}$, or $\frac{\ln n}{\sqrt{n}}$, immediately think: replace $n$ with $x$ and apply L'Hopital's. This technique appears frequently in MC questions testing whether you can evaluate limits needed for convergence tests.

3. **Know the growth rate hierarchy cold.** The AP exam loves to test $\lim_{n\to\infty} \frac{n^k}{r^n}$ (always $0$ for $r > 1$) and $\lim_{n\to\infty} \frac{r^n}{n!}$ (always $0$). These show up as answer justifications for the Ratio Test. Memorize: $\ln n \ll n^p \ll b^n \ll n! \ll n^n$.

4. **Geometric sequences are the most tested type.** If you see $r^n$ with $|r| < 1$, it converges to $0$. If $|r| > 1$, it diverges. If $|r| = 1$, it depends (converges for $r = 1$, diverges for $r = -1$). This comes back repeatedly in geometric series and the Ratio Test.

5. **The Squeeze Theorem for sequences is a free response favorite.** When a sequence has an oscillating factor (like $\sin n$ or $\cos n$ or $(-1)^n$) multiplied by a decaying factor (like $\frac{1}{n}$), bound the oscillating part between $-1$ and $1$, then squeeze.

6. **Recursive sequences appear in free response.** The exam might give a recursive definition and ask you to show convergence and find the limit. Remember: (1) assume the limit exists, (2) set $L = f(L)$, (3) solve. But first make sure the sequence actually converges (check bounded + monotonic if needed).

7. **Don't confuse sequence convergence with series convergence.** If the exam asks "does the sequence $\{a_n\}$ converge?" that's about whether $a_n$ approaches a limit. If it asks "does $\sum a_n$ converge?" that's a totally different question. Read carefully.

8. **The limit $\left(1 + \frac{1}{n}\right)^n \to e$ is worth knowing.** This specific sequence appears in compound interest problems and occasionally in MC questions. More generally, $\left(1 + \frac{k}{n}\right)^n \to e^k$.

---

## Practice Problems

### Basic (Problems 1-5)

**1.** Find $\displaystyle\lim_{n \to \infty} \frac{5n + 3}{2n - 1}$.

---

**2.** Determine whether the sequence $a_n = \frac{(-1)^n \cdot n}{n + 1}$ converges or diverges.

---

**3.** Find $\displaystyle\lim_{n \to \infty} \frac{n^2 + 1}{3n^2 + 7n}$.

---

**4.** Find the first five terms of the sequence defined by $a_1 = 1$, $a_{n+1} = a_n + 2n$. Is the sequence increasing, decreasing, or neither?

---

**5.** Find $\displaystyle\lim_{n \to \infty} \left(\frac{3}{4}\right)^n$.

---

### Intermediate (Problems 6-10)

**6.** Find $\displaystyle\lim_{n \to \infty} \frac{\ln(n^2)}{n}$.

---

**7.** Use the Squeeze Theorem to find $\displaystyle\lim_{n \to \infty} \frac{\cos(n^2)}{n}$.

---

**8.** Find $\displaystyle\lim_{n \to \infty} \frac{n^2}{e^{n/3}}$.

---

**9.** Determine whether the sequence $a_n = \frac{2^n}{n!}$ converges or diverges. If it converges, find its limit.

---

**10.** Show that $a_n = \frac{n!}{n^n}$ converges to $0$.

---

### Advanced (Problems 11-15)

**11.** The sequence $\{a_n\}$ is defined by $a_1 = 1$ and $a_{n+1} = \sqrt{2 + a_n}$. Show that the sequence is bounded above by $2$ and increasing, then find its limit.

---

**12.** Find $\displaystyle\lim_{n \to \infty} \left(1 + \frac{3}{n}\right)^n$.

---

**13.** Find $\displaystyle\lim_{n \to \infty} \left(\sqrt{n+1} - \sqrt{n}\right)$.

---

**14.** Find $\displaystyle\lim_{n \to \infty} \frac{(-3)^n}{n!}$.

---

**15.** Find $\displaystyle\lim_{n \to \infty} \left(\frac{n+2}{n}\right)^n$.

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

$\displaystyle\lim_{n \to \infty} \frac{n^3 + 2n}{4n^3 - n^2 + 1} =$

| Choice | Answer |
|--------|--------|
| **(A)** | $0$ |
| **(B)** | $\frac{1}{4}$ |
| **(C)** | $\frac{1}{2}$ |
| **(D)** | $\infty$ |

---

#### Problem 17 (Multiple Choice)

Which of the following sequences diverges?

| Choice | Answer |
|--------|--------|
| **(A)** | $a_n = \frac{5^n}{n!}$ |
| **(B)** | $a_n = \frac{(-1)^n}{n^3}$ |
| **(C)** | $a_n = \frac{n + (-1)^n}{n}$ |
| **(D)** | $a_n = (-1)^n \left(\frac{n}{n+1}\right)$ |

---

#### Problem 18 (Multiple Choice)

The sequence $\{a_n\}$ is defined by $a_1 = 10$ and $a_{n+1} = \frac{1}{2}a_n + 3$. Assuming the sequence converges, its limit is:

| Choice | Answer |
|--------|--------|
| **(A)** | $3$ |
| **(B)** | $5$ |
| **(C)** | $6$ |
| **(D)** | $10$ |

---

#### Problem 19 (Free Response)

> Consider the sequence defined by $a_n = \frac{n^2}{2^n}$ for $n \geq 1$.
>
> **(a)** Write the first five terms of the sequence. Based on the terms, conjecture whether the sequence converges or diverges.
>
> **(b)** Find $\displaystyle\lim_{n \to \infty} \frac{n^2}{2^n}$ using L'Hopital's Rule. Show all work.
>
> **(c)** Is the sequence monotonically decreasing for all $n \geq 1$? Justify your answer.
>
> **(d)** Using the growth rate hierarchy, explain why $\frac{n^k}{2^n} \to 0$ for any positive integer $k$.

---

#### Problem 20 (Free Response)

> Ganga is saving up for a Ding Tea boba drink fund. She opens a savings jar with $\$5$ and each week adds $\$2$ plus $10\%$ of whatever is currently in the jar. The amount in the jar after week $n$ is modeled by:
>
> $$a_1 = 5, \quad a_{n+1} = 1.1 \, a_n + 2$$
>
> **(a)** Find $a_2$, $a_3$, and $a_4$. Round to two decimal places.
>
> **(b)** Assuming the sequence $\{a_n\}$ converges, find its limit. (Is this limit realistic? Briefly explain.)
>
> **(c)** In reality, the sequence diverges. Explain why by showing that $a_{n+1} > a_n$ for all $n \geq 1$ and that the sequence is unbounded.
>
> **(d)** Suppose instead that Ganga earns $5\%$ weekly interest (not $10\%$): $a_{n+1} = 1.05\, a_n + 2$. Does this sequence also diverge? Use the same reasoning from part (c).

---

## Answer Key

<details>
<summary><strong>Problem 1 Solution</strong></summary>

**Find $\displaystyle\lim_{n \to \infty} \frac{5n + 3}{2n - 1}$.**

Divide numerator and denominator by $n$:

$$\lim_{n \to \infty} \frac{5n + 3}{2n - 1} = \lim_{n \to \infty} \frac{5 + \frac{3}{n}}{2 - \frac{1}{n}} = \frac{5 + 0}{2 - 0} = \boxed{\frac{5}{2}}$$

Both numerator and denominator are degree 1 polynomials, so the limit is the ratio of leading coefficients: $\frac{5}{2}$.

</details>

---

<details>
<summary><strong>Problem 2 Solution</strong></summary>

**Determine whether $a_n = \frac{(-1)^n \cdot n}{n + 1}$ converges or diverges.**

Let's look at what happens as $n \to \infty$. The magnitude is:

$$\left|\frac{(-1)^n \cdot n}{n+1}\right| = \frac{n}{n+1} \to 1$$

So the terms alternate between values close to $+1$ and $-1$:

- $a_1 = \frac{-1}{2} = -0.5$
- $a_2 = \frac{2}{3} \approx 0.667$
- $a_3 = \frac{-3}{4} = -0.75$
- $a_4 = \frac{4}{5} = 0.8$
- $a_{100} = \frac{100}{101} \approx 0.990$
- $a_{101} = \frac{-101}{102} \approx -0.990$

The terms oscillate between values approaching $+1$ and $-1$ and never settle on a single value.

$$\boxed{\text{The sequence diverges.}}$$

Even though the magnitude converges to $1$, the sign keeps flipping, so there is no single limit.

</details>

---

<details>
<summary><strong>Problem 3 Solution</strong></summary>

**Find $\displaystyle\lim_{n \to \infty} \frac{n^2 + 1}{3n^2 + 7n}$.**

Divide numerator and denominator by $n^2$:

$$\lim_{n \to \infty} \frac{n^2 + 1}{3n^2 + 7n} = \lim_{n \to \infty} \frac{1 + \frac{1}{n^2}}{3 + \frac{7}{n}} = \frac{1 + 0}{3 + 0} = \boxed{\frac{1}{3}}$$

</details>

---

<details>
<summary><strong>Problem 4 Solution</strong></summary>

**Find the first five terms of the sequence defined by $a_1 = 1$, $a_{n+1} = a_n + 2n$.**

Compute recursively:

- $a_1 = 1$
- $a_2 = a_1 + 2(1) = 1 + 2 = 3$
- $a_3 = a_2 + 2(2) = 3 + 4 = 7$
- $a_4 = a_3 + 2(3) = 7 + 6 = 13$
- $a_5 = a_4 + 2(4) = 13 + 8 = 21$

The first five terms are: $\boxed{1, 3, 7, 13, 21}$.

Since each term increases (we're adding a positive number $2n > 0$ at each step), the sequence is **increasing**.

**Bonus:** The explicit formula is $a_n = n^2 - n + 1$ (verify: $a_1 = 1 - 1 + 1 = 1$, $a_2 = 4 - 2 + 1 = 3$, etc.).

</details>

---

<details>
<summary><strong>Problem 5 Solution</strong></summary>

**Find $\displaystyle\lim_{n \to \infty} \left(\frac{3}{4}\right)^n$.**

This is a geometric sequence with ratio $r = \frac{3}{4}$. Since $|r| = \frac{3}{4} < 1$:

$$\lim_{n \to \infty} \left(\frac{3}{4}\right)^n = \boxed{0}$$

Each term is $\frac{3}{4}$ of the previous one. The terms decay exponentially: $0.75, 0.5625, 0.4219, \ldots \to 0$.

</details>

---

<details>
<summary><strong>Problem 6 Solution</strong></summary>

**Find $\displaystyle\lim_{n \to \infty} \frac{\ln(n^2)}{n}$.**

First, simplify using log properties:

$$\frac{\ln(n^2)}{n} = \frac{2\ln n}{n}$$

Now replace $n$ with $x$ and apply L'Hopital's Rule (since $\frac{2\ln x}{x} \to \frac{\infty}{\infty}$):

$$\lim_{x \to \infty} \frac{2\ln x}{x} \stackrel{\text{L'H}}{=} \lim_{x \to \infty} \frac{2/x}{1} = \lim_{x \to \infty} \frac{2}{x} = 0$$

$$\boxed{\lim_{n \to \infty} \frac{\ln(n^2)}{n} = 0}$$

This confirms the growth hierarchy: $\ln(n^2) = 2\ln n$ is still logarithmic, which is dominated by the polynomial $n$.

</details>

---

<details>
<summary><strong>Problem 7 Solution</strong></summary>

**Use the Squeeze Theorem to find $\displaystyle\lim_{n \to \infty} \frac{\cos(n^2)}{n}$.**

Since $-1 \leq \cos(n^2) \leq 1$ for all $n$, divide by $n$ (positive for $n \geq 1$):

$$-\frac{1}{n} \leq \frac{\cos(n^2)}{n} \leq \frac{1}{n}$$

Both bounds approach $0$:

$$\lim_{n \to \infty}\left(-\frac{1}{n}\right) = 0 \quad \text{and} \quad \lim_{n \to \infty}\frac{1}{n} = 0$$

By the Squeeze Theorem:

$$\boxed{\lim_{n \to \infty} \frac{\cos(n^2)}{n} = 0}$$

</details>

---

<details>
<summary><strong>Problem 8 Solution</strong></summary>

**Find $\displaystyle\lim_{n \to \infty} \frac{n^2}{e^{n/3}}$.**

Replace $n$ with $x$. This gives $\frac{\infty}{\infty}$, so apply L'Hopital's Rule:

$$\lim_{x \to \infty} \frac{x^2}{e^{x/3}} \stackrel{\text{L'H}}{=} \lim_{x \to \infty} \frac{2x}{\frac{1}{3}e^{x/3}} = \lim_{x \to \infty} \frac{6x}{e^{x/3}}$$

Still $\frac{\infty}{\infty}$, apply L'Hopital's again:

$$\stackrel{\text{L'H}}{=} \lim_{x \to \infty} \frac{6}{\frac{1}{3}e^{x/3}} = \lim_{x \to \infty} \frac{18}{e^{x/3}} = 0$$

$$\boxed{\lim_{n \to \infty} \frac{n^2}{e^{n/3}} = 0}$$

Exponential growth (even $e^{n/3}$, which grows more slowly than $e^n$) always beats polynomial growth.

</details>

---

<details>
<summary><strong>Problem 9 Solution</strong></summary>

**Determine whether $a_n = \frac{2^n}{n!}$ converges or diverges. If it converges, find its limit.**

The sequence converges to $0$. This was shown in detail in Example 9 using the bounding argument:

For $n \geq 3$:

$$0 \leq \frac{2^n}{n!} = \frac{2}{1} \cdot \frac{2}{2} \cdot \frac{2}{3} \cdot \frac{2}{4} \cdots \frac{2}{n} \leq 2 \cdot 1 \cdot \left(\frac{2}{3}\right)^{n-2}$$

Since $\left(\frac{2}{3}\right)^{n-2} \to 0$ (geometric decay with $|r| < 1$), the Squeeze Theorem gives:

$$\boxed{\lim_{n \to \infty} \frac{2^n}{n!} = 0}$$

Let's verify with a few terms: $a_1 = 2$, $a_2 = 2$, $a_3 = \frac{8}{6} \approx 1.33$, $a_4 = \frac{16}{24} \approx 0.67$, $a_5 = \frac{32}{120} \approx 0.27$, $a_{10} = \frac{1024}{3628800} \approx 0.000282$. Clearly heading to zero.

</details>

---

<details>
<summary><strong>Problem 10 Solution</strong></summary>

**Show that $a_n = \frac{n!}{n^n}$ converges to $0$.**

Write out the fraction:

$$\frac{n!}{n^n} = \frac{1 \cdot 2 \cdot 3 \cdots n}{n \cdot n \cdot n \cdots n} = \frac{1}{n} \cdot \frac{2}{n} \cdot \frac{3}{n} \cdots \frac{n}{n}$$

Each factor $\frac{k}{n} \leq 1$ for $k \leq n$, and the first factor is $\frac{1}{n}$. So:

$$0 \leq \frac{n!}{n^n} = \frac{1}{n} \cdot \underbrace{\frac{2}{n} \cdot \frac{3}{n} \cdots \frac{n}{n}}_{\leq 1 \text{ (each factor} \leq 1\text{)}} \leq \frac{1}{n}$$

Since $\frac{1}{n} \to 0$, the Squeeze Theorem gives:

$$\boxed{\lim_{n \to \infty} \frac{n!}{n^n} = 0}$$

This confirms $n^n$ dominates $n!$ in the growth hierarchy.

</details>

---

<details>
<summary><strong>Problem 11 Solution</strong></summary>

**The sequence $a_1 = 1$, $a_{n+1} = \sqrt{2 + a_n}$. Show bounded above by 2 and increasing, then find the limit.**

**Bounded above by 2 (by induction):**

*Base case:* $a_1 = 1 < 2$. True.

*Inductive step:* Assume $a_n < 2$. Then:

$$a_{n+1} = \sqrt{2 + a_n} < \sqrt{2 + 2} = \sqrt{4} = 2$$

So $a_{n+1} < 2$. By induction, $a_n < 2$ for all $n$.

**Increasing (show $a_{n+1} > a_n$):**

We need $\sqrt{2 + a_n} > a_n$, which is equivalent to $2 + a_n > a_n^2$ (since both sides are positive), i.e., $a_n^2 - a_n - 2 < 0$, i.e., $(a_n - 2)(a_n + 1) < 0$.

Since $a_n < 2$ (bounded above) and $a_n > 0$ (all terms are positive — easy to verify since $a_1 = 1 > 0$ and $a_{n+1} = \sqrt{2 + a_n} > 0$), we have $a_n - 2 < 0$ and $a_n + 1 > 0$, so the product is negative. Therefore $a_{n+1} > a_n$ for all $n$.

**By the Monotone Convergence Theorem**, the sequence converges.

**Finding the limit:** Let $L = \lim_{n\to\infty} a_n$. Then:

$$L = \sqrt{2 + L}$$

$$L^2 = 2 + L$$

$$L^2 - L - 2 = 0$$

$$(L - 2)(L + 1) = 0$$

$$L = 2 \quad \text{or} \quad L = -1$$

Since all terms are positive, $L > 0$, so:

$$\boxed{L = 2}$$

Let's verify: $a_1 = 1$, $a_2 = \sqrt{3} \approx 1.732$, $a_3 = \sqrt{2 + 1.732} \approx 1.932$, $a_4 \approx 1.983$, $a_5 \approx 1.996$. Clearly approaching $2$.

</details>

---

<details>
<summary><strong>Problem 12 Solution</strong></summary>

**Find $\displaystyle\lim_{n \to \infty} \left(1 + \frac{3}{n}\right)^n$.**

This is a variation of the fundamental limit $\lim_{n\to\infty}\left(1 + \frac{1}{n}\right)^n = e$.

Let $m = \frac{n}{3}$, so $n = 3m$ and as $n \to \infty$, $m \to \infty$:

$$\left(1 + \frac{3}{n}\right)^n = \left(1 + \frac{1}{m}\right)^{3m} = \left[\left(1 + \frac{1}{m}\right)^m\right]^3$$

Since $\left(1 + \frac{1}{m}\right)^m \to e$:

$$\lim_{n \to \infty} \left(1 + \frac{3}{n}\right)^n = e^3$$

**Alternative method using logarithms:** Let $a_n = \left(1 + \frac{3}{n}\right)^n$. Then:

$$\ln a_n = n \ln\left(1 + \frac{3}{n}\right)$$

Replace $n$ with $x$:

$$\lim_{x \to \infty} x \ln\left(1 + \frac{3}{x}\right) = \lim_{x \to \infty} \frac{\ln\left(1 + \frac{3}{x}\right)}{1/x}$$

This is $\frac{0}{0}$. Apply L'Hopital's:

$$= \lim_{x \to \infty} \frac{\frac{-3/x^2}{1 + 3/x}}{-1/x^2} = \lim_{x \to \infty} \frac{3}{1 + 3/x} = \frac{3}{1} = 3$$

So $\ln a_n \to 3$, giving $a_n \to e^3$.

$$\boxed{\lim_{n \to \infty} \left(1 + \frac{3}{n}\right)^n = e^3 \approx 20.086}$$

</details>

---

<details>
<summary><strong>Problem 13 Solution</strong></summary>

**Find $\displaystyle\lim_{n \to \infty} \left(\sqrt{n+1} - \sqrt{n}\right)$.**

Direct approach gives $\infty - \infty$, which is indeterminate. Rationalize by multiplying by the conjugate:

$$\sqrt{n+1} - \sqrt{n} = \frac{(\sqrt{n+1} - \sqrt{n})(\sqrt{n+1} + \sqrt{n})}{\sqrt{n+1} + \sqrt{n}}$$

$$= \frac{(n+1) - n}{\sqrt{n+1} + \sqrt{n}} = \frac{1}{\sqrt{n+1} + \sqrt{n}}$$

As $n \to \infty$, the denominator $\to \infty$:

$$\lim_{n \to \infty} \frac{1}{\sqrt{n+1} + \sqrt{n}} = \boxed{0}$$

Even though both $\sqrt{n+1}$ and $\sqrt{n}$ go to infinity, they get closer and closer together. The gap between consecutive square roots shrinks to zero.

</details>

---

<details>
<summary><strong>Problem 14 Solution</strong></summary>

**Find $\displaystyle\lim_{n \to \infty} \frac{(-3)^n}{n!}$.**

First, note that $\left|\frac{(-3)^n}{n!}\right| = \frac{3^n}{n!}$.

Using the same bounding technique as Example 9. For $n \geq 4$:

$$\frac{3^n}{n!} = \frac{3}{1} \cdot \frac{3}{2} \cdot \frac{3}{3} \cdot \frac{3}{4} \cdot \frac{3}{5} \cdots \frac{3}{n}$$

For $k \geq 4$, each factor $\frac{3}{k} \leq \frac{3}{4}$:

$$\frac{3^n}{n!} \leq \frac{3}{1} \cdot \frac{3}{2} \cdot \frac{3}{3} \cdot \left(\frac{3}{4}\right)^{n-3} = \frac{27}{6} \cdot \left(\frac{3}{4}\right)^{n-3} = \frac{9}{2}\left(\frac{3}{4}\right)^{n-3}$$

Since $\left(\frac{3}{4}\right)^{n-3} \to 0$, we get $\frac{3^n}{n!} \to 0$. Therefore $\left|\frac{(-3)^n}{n!}\right| \to 0$.

By the Squeeze Theorem (since $-\frac{3^n}{n!} \leq \frac{(-3)^n}{n!} \leq \frac{3^n}{n!}$):

$$\boxed{\lim_{n \to \infty} \frac{(-3)^n}{n!} = 0}$$

Factorial beats exponential, regardless of sign.

</details>

---

<details>
<summary><strong>Problem 15 Solution</strong></summary>

**Find $\displaystyle\lim_{n \to \infty} \left(\frac{n+2}{n}\right)^n$.**

Rewrite:

$$\left(\frac{n+2}{n}\right)^n = \left(1 + \frac{2}{n}\right)^n$$

This has the same form as Problem 12. Using the substitution $m = n/2$ (so $n = 2m$):

$$\left(1 + \frac{2}{n}\right)^n = \left(1 + \frac{1}{m}\right)^{2m} = \left[\left(1 + \frac{1}{m}\right)^m\right]^2 \to e^2$$

$$\boxed{\lim_{n \to \infty} \left(\frac{n+2}{n}\right)^n = e^2 \approx 7.389}$$

</details>

---

<details>
<summary><strong>Problem 16 Solution</strong></summary>

**Answer: (B)** $\frac{1}{4}$

$$\lim_{n \to \infty} \frac{n^3 + 2n}{4n^3 - n^2 + 1}$$

Both numerator and denominator are degree 3 polynomials. Divide by $n^3$:

$$= \lim_{n \to \infty} \frac{1 + \frac{2}{n^2}}{4 - \frac{1}{n} + \frac{1}{n^3}} = \frac{1 + 0}{4 - 0 + 0} = \frac{1}{4}$$

This matches **(B)**.

- (A) $0$ would be the answer if the numerator had lower degree than the denominator.
- (C) $\frac{1}{2}$ is incorrect — the leading coefficient ratio is $\frac{1}{4}$, not $\frac{1}{2}$.
- (D) $\infty$ would be the answer if the numerator had higher degree.

</details>

---

<details>
<summary><strong>Problem 17 Solution</strong></summary>

**Answer: (D)** $a_n = (-1)^n \left(\frac{n}{n+1}\right)$

Let's check each option:

**(A)** $a_n = \frac{5^n}{n!}$: By the growth hierarchy, $n!$ dominates $5^n$, so $\frac{5^n}{n!} \to 0$. **Converges.**

**(B)** $a_n = \frac{(-1)^n}{n^3}$: The magnitude is $\frac{1}{n^3} \to 0$. By the Squeeze Theorem, this converges to $0$. **Converges.**

**(C)** $a_n = \frac{n + (-1)^n}{n} = 1 + \frac{(-1)^n}{n}$: Since $\frac{(-1)^n}{n} \to 0$, the sequence converges to $1$. **Converges.**

**(D)** $a_n = (-1)^n \cdot \frac{n}{n+1}$: The magnitude is $\frac{n}{n+1} \to 1$, so the terms alternate between values approaching $+1$ and $-1$. The sequence oscillates and never settles. **Diverges.**

$$\boxed{\text{(D)}}$$

</details>

---

<details>
<summary><strong>Problem 18 Solution</strong></summary>

**Answer: (C)** $6$

Assuming the sequence converges to $L$, take the limit of both sides of $a_{n+1} = \frac{1}{2}a_n + 3$:

$$L = \frac{1}{2}L + 3$$

$$L - \frac{1}{2}L = 3$$

$$\frac{1}{2}L = 3$$

$$L = 6$$

**Verification:** Let's check convergence. Compute a few terms:

- $a_1 = 10$
- $a_2 = \frac{1}{2}(10) + 3 = 8$
- $a_3 = \frac{1}{2}(8) + 3 = 7$
- $a_4 = \frac{1}{2}(7) + 3 = 6.5$
- $a_5 = \frac{1}{2}(6.5) + 3 = 6.25$
- $a_6 = 6.125$

The sequence is decreasing and bounded below by $6$ (you can prove this by induction), so by the Monotone Convergence Theorem it converges.

$$\boxed{\text{(C)}\ L = 6}$$

</details>

---

<details>
<summary><strong>Problem 19 Solution</strong></summary>

**(a)** First five terms of $a_n = \frac{n^2}{2^n}$:

- $a_1 = \frac{1}{2} = 0.5$
- $a_2 = \frac{4}{4} = 1$
- $a_3 = \frac{9}{8} = 1.125$
- $a_4 = \frac{16}{16} = 1$
- $a_5 = \frac{25}{32} = 0.78125$

The sequence increases initially, then decreases. **Conjecture:** the sequence converges to $0$ because exponential growth in the denominator eventually dominates polynomial growth in the numerator.

**(b)** Replace $n$ with $x$. Since $\frac{x^2}{2^x} = \frac{x^2}{e^{x\ln 2}}$, this gives $\frac{\infty}{\infty}$. Apply L'Hopital's Rule:

$$\lim_{x \to \infty} \frac{x^2}{2^x} \stackrel{\text{L'H}}{=} \lim_{x \to \infty} \frac{2x}{(\ln 2) \cdot 2^x} \stackrel{\text{L'H}}{=} \lim_{x \to \infty} \frac{2}{(\ln 2)^2 \cdot 2^x} = \frac{2}{\infty} = 0$$

$$\boxed{\lim_{n \to \infty} \frac{n^2}{2^n} = 0}$$

**(c)** The sequence is **not** monotonically decreasing for all $n \geq 1$.

From part (a): $a_1 = 0.5 < a_2 = 1 < a_3 = 1.125$, so the sequence is *increasing* for the first few terms. It begins to decrease after $n = 3$.

To find where the sequence starts decreasing, check when $a_{n+1} < a_n$:

$$\frac{(n+1)^2}{2^{n+1}} < \frac{n^2}{2^n} \implies \frac{(n+1)^2}{2} < n^2 \implies (n+1)^2 < 2n^2$$

$$n^2 + 2n + 1 < 2n^2 \implies n^2 - 2n - 1 > 0 \implies n > 1 + \sqrt{2} \approx 2.414$$

So for $n \geq 3$, the sequence is decreasing. But it is **not** monotonically decreasing for all $n \geq 1$.

**(d)** For any positive integer $k$, the growth rate hierarchy tells us:

$$\text{exponential growth} \gg \text{polynomial growth}$$

Specifically, $2^n$ is exponential (base $b = 2 > 1$) and $n^k$ is polynomial (degree $k$). Since exponentials always eventually dominate polynomials:

$$\lim_{n \to \infty} \frac{n^k}{2^n} = 0$$

This can be proven by applying L'Hopital's Rule $k$ times. Each application reduces the polynomial degree by $1$ while the denominator remains $(\ln 2)^j \cdot 2^x$ (still exponential). After $k$ applications, the numerator is a constant and the denominator is $(\ln 2)^k \cdot 2^x \to \infty$, giving a limit of $0$.

</details>

---

<details>
<summary><strong>Problem 20 Solution</strong></summary>

**Ganga's Ding Tea boba fund:** $a_1 = 5$, $a_{n+1} = 1.1\,a_n + 2$.

**(a)** Compute $a_2$, $a_3$, $a_4$:

- $a_2 = 1.1(5) + 2 = 5.5 + 2 = 7.50$
- $a_3 = 1.1(7.5) + 2 = 8.25 + 2 = 10.25$
- $a_4 = 1.1(10.25) + 2 = 11.275 + 2 = 13.28$ (rounded to two decimal places)

$$\boxed{a_2 = 7.50, \quad a_3 = 10.25, \quad a_4 = 13.28}$$

**(b)** Assuming convergence, let $L = \lim_{n\to\infty} a_n$. Then:

$$L = 1.1L + 2$$

$$L - 1.1L = 2$$

$$-0.1L = 2$$

$$L = -20$$

The "limit" would be $L = -20$, which is **not realistic** — you can't have a negative amount of money in a savings jar. This negative value is a red flag telling us our assumption of convergence was wrong. The sequence does not actually converge.

$$\boxed{L = -20 \text{ (not realistic; the assumption of convergence is invalid)}}$$

**(c)** Show $a_{n+1} > a_n$ for all $n \geq 1$:

$$a_{n+1} - a_n = 1.1a_n + 2 - a_n = 0.1a_n + 2$$

Since $a_1 = 5 > 0$ and each subsequent term is $a_{n+1} = 1.1a_n + 2 > 0$ (because $a_n > 0$ implies $a_{n+1} > 0$), all terms are positive. Therefore:

$$a_{n+1} - a_n = 0.1a_n + 2 > 0 + 2 > 0$$

So the sequence is **strictly increasing** for all $n$.

**Unbounded:** Since the sequence is increasing and $a_{n+1} = 1.1a_n + 2 > 1.1a_n$, we have:

$$a_n > a_1 \cdot (1.1)^{n-1} = 5 \cdot (1.1)^{n-1}$$

Since $(1.1)^{n-1} \to \infty$ (geometric growth with $r = 1.1 > 1$), the sequence $a_n \to \infty$.

The sequence is increasing and unbounded, so it **diverges to infinity**.

**(d)** With $5\%$ interest: $a_{n+1} = 1.05\,a_n + 2$, $a_1 = 5$.

The same analysis applies:

$$a_{n+1} - a_n = 1.05a_n + 2 - a_n = 0.05a_n + 2 > 0$$

So the sequence is still strictly increasing. And:

$$a_{n+1} = 1.05a_n + 2 > 1.05a_n$$

$$\implies a_n > 5 \cdot (1.05)^{n-1} \to \infty$$

**Yes, this sequence also diverges.** Any recursion of the form $a_{n+1} = ra_n + c$ with $r > 1$ and $c > 0$ will diverge to infinity, regardless of the initial value. The multiplier $r > 1$ causes exponential growth that the constant addition $c$ only accelerates. The fixed point $L = \frac{c}{1 - r}$ is negative (since $1 - r < 0$), which is physically unreachable, confirming divergence.

$$\boxed{\text{The sequence diverges to infinity for both } r = 1.1 \text{ and } r = 1.05.}$$

</details>

---

## What's Next

You've just built the entire foundation for Unit 10. Sequences are the atoms that everything else is made of — series are sums of sequences, convergence tests check whether sequences of partial sums settle down, and Taylor polynomials are built term by term as sequences of increasingly accurate approximations. The key ideas you'll carry forward are: how to evaluate limits (L'Hopital's, Squeeze Theorem, growth hierarchies), the Monotone Convergence Theorem for proving convergence exists, and the fixed-point technique for recursive sequences. Next up: [Series](/calculus/series), where we ask the wild question — what happens when you *add up* infinitely many terms of a sequence? Can an infinite sum ever equal a finite number? Spoiler: yes, and it's one of the most beautiful ideas in all of mathematics. Like ordering an infinite number of increasingly tiny boba pearls from Ding Tea — at some point, the total volume converges and you've got yourself a finite cup of deliciousness.

---

<div align="center">

[← Vector-Valued Functions](/calculus/vector-valued-functions) | [Series →](/calculus/series)

</div>
