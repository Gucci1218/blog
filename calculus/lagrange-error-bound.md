# Lagrange Error Bound
<p class="article-date">April 23, 2026</p>

*You're at Starbucks, ordering your usual caramel frappe, and the barista says, "We're out of caramel syrup, but I can make something that's pretty close." You'd probably ask: "How close?" That's the Lagrange Error Bound in a nutshell. Throughout this entire series, you've learned to build Taylor polynomials -- beautiful approximations that mimic functions like $e^x$, $\sin x$, and $\ln(1 + x)$ near a center point. But approximations are only useful if you know how good they are. The Lagrange Error Bound is the mathematical guarantee that answers the question: "If I use $n$ terms of the Taylor series, how far off could I possibly be from the real value?" It's the receipt that proves your approximation is worth what you paid for it.*

---

## What You'll Learn
- Understand the Taylor polynomial remainder $R_n(x) = f(x) - P_n(x)$ and what it represents
- State and apply the Lagrange Error Bound formula
- Find $M$, the bound on the $(n+1)$-th derivative, on the relevant interval
- Use the error bound to determine how many terms are needed for a desired accuracy
- Connect the Lagrange Error Bound to the Alternating Series Error Bound
- Know when to use Lagrange vs. Alternating Series estimation
- Develop a step-by-step strategy for error bound problems on the AP exam
- Approximate common functions ($e$, $\sin$, $\cos$, $\ln$) to a specified number of decimal places
- Understand why factorials grow so fast, making Taylor approximations incredibly powerful

---

## Prerequisites
- [Taylor and Maclaurin Series](/calculus/taylor-series)
- [Higher-Order Derivatives](/calculus/0405-higher-order-derivatives)
- [Convergence Tests](/calculus/convergence-tests)

---

## The Core Concept

### Intuition First

Imagine you're learning a new K-pop choreography. You watch the video once and get the general vibe -- that's like using the first term of a Taylor polynomial. You watch it again and nail the first eight counts -- that's adding more terms. Each time you rewatch, your performance gets closer to the original. But your dance teacher asks: "How far off are you from the actual choreography right now?"

That's the error question. The **remainder** $R_n(x)$ is the gap between your current approximation (the Taylor polynomial $P_n(x)$) and the real function $f(x)$:

$$R_n(x) = f(x) - P_n(x)$$

The Lagrange Error Bound gives you a **worst-case guarantee** on how big that gap can be. It's like your dance teacher saying, "You're off by at most two beats in the whole routine." You might actually be closer than that, but you're guaranteed to be no worse.

### Why Do We Need a Bound?

The Taylor polynomial of degree $n$ centered at $x = a$ is:

$$P_n(x) = \sum_{k=0}^{n} \frac{f^{(k)}(a)}{k!}(x - a)^k$$

This polynomial agrees with $f$ at $x = a$ in value, first derivative, second derivative, ..., all the way up to the $n$-th derivative. But away from $a$, the polynomial and $f$ start to drift apart. The remainder $R_n(x)$ measures that drift:

$$f(x) = P_n(x) + R_n(x)$$

We want to know: *how big can $R_n(x)$ be?*

### The Formal Definition

**Lagrange Error Bound (Taylor's Theorem with Remainder):**

If $f$ has continuous derivatives through order $n + 1$ on an interval containing $a$ and $x$, then:

$$\boxed{|R_n(x)| \leq \frac{M \cdot |x - a|^{n+1}}{(n+1)!}}$$

where $M = \max_{z} |f^{(n+1)}(z)|$ for all $z$ between $a$ and $x$.

**In words:** The absolute error when using the $n$-th degree Taylor polynomial is at most:

$$\frac{(\text{max of the next derivative}) \times |x - a|^{n+1}}{(n+1)!}$$

### Breaking Down Each Piece

| Symbol | What It Means | How to Find It |
|--------|--------------|----------------|
| $R_n(x)$ | The error (remainder) when using $P_n(x)$ | This is what we're bounding |
| $n$ | Degree of the Taylor polynomial | Given in the problem |
| $a$ | Center of the Taylor series | Given in the problem |
| $x$ | The point where you're approximating | Given in the problem |
| $M$ | Maximum of $\|f^{(n+1)}(z)\|$ on the interval between $a$ and $x$ | **This is the hard part** -- you need to find or bound the $(n+1)$-th derivative |
| $(n+1)!$ | Factorial of $(n+1)$ | Just compute it -- factorials grow insanely fast |

### Finding $M$ -- The Key Skill

Finding $M$ is where most of the work (and most of the mistakes) happen. Here's the strategy:

**Step 1:** Compute $f^{(n+1)}(x)$ -- the $(n+1)$-th derivative.

**Step 2:** Determine the interval between $a$ and $x$.

**Step 3:** Find the maximum of $|f^{(n+1)}(z)|$ on that interval.

For many common functions, this step has nice shortcuts:

| Function | All derivatives are... | So $M$ is... |
|----------|----------------------|--------------|
| $e^x$ | $e^x$ (always) | $e^x$ evaluated at the right endpoint |
| $\sin x$ | $\pm \sin x$ or $\pm \cos x$ | At most $1$ (always!) |
| $\cos x$ | $\pm \sin x$ or $\pm \cos x$ | At most $1$ (always!) |
| $\ln(1+x)$ centered at $0$ | $\frac{(-1)^n \cdot n!}{(1+x)^{n+1}}$ | Depends on the interval |

For $\sin x$ and $\cos x$, you can **always** use $M = 1$. This makes error bound problems with trig functions especially clean.

### Why Factorials Make Everything Work

Here's the beautiful secret behind Taylor series: **factorials grow faster than any exponential**.

Consider $\frac{x^{n+1}}{(n+1)!}$ for a fixed $x$, say $x = 10$:

| $n$ | $\frac{10^{n+1}}{(n+1)!}$ | Decimal |
|-----|---------------------------|---------|
| 1 | $\frac{100}{2}$ | $50$ |
| 3 | $\frac{10{,}000}{24}$ | $416.7$ |
| 5 | $\frac{1{,}000{,}000}{720}$ | $1388.9$ |
| 10 | $\frac{10^{11}}{39916800}$ | $2505.2$ |
| 15 | $\frac{10^{16}}{2.09 \times 10^{13}}$ | $478.8$ |
| 20 | $\frac{10^{21}}{5.11 \times 10^{19}}$ | $19.6$ |
| 25 | $\frac{10^{26}}{4.03 \times 10^{26}}$ | $0.248$ |
| 30 | $\frac{10^{31}}{8.22 \times 10^{33}}$ | $0.000012$ |

Even for $x = 10$ (which is far from the center), by the time you reach $n = 30$, the error bound is tiny. For values close to the center (like $x = 0.1$), convergence is blazingly fast -- just a few terms gives you 10+ decimal places of accuracy.

It's like ordering at Panda Express -- each additional side dish ($n$-th term) adds less and less to your plate. The factorial in the denominator is the portion control that makes sure each additional term contributes less than the one before, eventually becoming negligibly small.

### Alternating Series Error Bound -- The Other Tool

Before we dive into examples, let's talk about the **other** error estimation tool you should know: the Alternating Series Error Bound.

**Alternating Series Estimation Theorem:** If a series $\sum (-1)^n a_n$ satisfies:
1. $a_n > 0$ (terms alternate in sign)
2. $a_{n+1} \leq a_n$ (terms decrease in absolute value)
3. $\lim_{n \to \infty} a_n = 0$

Then the error from using the partial sum $S_n$ is at most $|a_{n+1}|$ -- the absolute value of the **first omitted term**.

$$|S - S_n| \leq a_{n+1}$$

### When to Use Which?

| Situation | Use... | Why |
|-----------|--------|-----|
| The Taylor series **alternates** in sign | Alternating Series Error Bound | It's simpler and often gives a tighter bound |
| The Taylor series does **not** alternate | Lagrange Error Bound | It's the only option |
| The problem says "use the Lagrange Error Bound" | Lagrange | They told you to |
| You need to bound the error for a **specific** $n$ | Either one (if applicable) | Lagrange always works; alternating is easier when valid |
| You need to find the **minimum** $n$ for a given accuracy | Either one | Use whichever gives fewer required terms |

**Key insight:** For functions like $\sin x$, $\cos x$, and $\ln(1+x)$ (whose Maclaurin series alternate), the Alternating Series Error Bound is usually easier to apply. But the Lagrange Error Bound works for **every** Taylor series, alternating or not.

---

## Worked Examples

### Example 1: Error Bound for $e^x$ -- The Classic Setup

**Use the 3rd-degree Maclaurin polynomial to approximate $e^{0.5}$, and find an upper bound on the error.**

The Maclaurin series for $e^x$ is:

$$e^x = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \cdots$$

So $P_3(x) = 1 + x + \frac{x^2}{2} + \frac{x^3}{6}$.

At $x = 0.5$:

$$P_3(0.5) = 1 + 0.5 + \frac{0.25}{2} + \frac{0.125}{6} = 1 + 0.5 + 0.125 + 0.02083\overline{3} = 1.6458\overline{3}$$

**Error bound:** We need $|R_3(0.5)|$. Here $n = 3$, $a = 0$, $x = 0.5$.

$$|R_3(0.5)| \leq \frac{M \cdot |0.5 - 0|^4}{4!}$$

We need $M = \max_{z \in [0, 0.5]} |f^{(4)}(z)|$. Since $f^{(4)}(x) = e^x$ and $e^x$ is increasing:

$$M = e^{0.5}$$

But wait -- we don't know $e^{0.5}$ exactly (that's what we're trying to approximate!). So we use an **overestimate**: $e^{0.5} < e^1 = e < 3$.

$$|R_3(0.5)| \leq \frac{3 \cdot (0.5)^4}{4!} = \frac{3 \cdot 0.0625}{24} = \frac{0.1875}{24} = 0.0078125$$

$$\boxed{|R_3(0.5)| \leq 0.0079}$$

So our approximation $P_3(0.5) \approx 1.6458$ is within $0.008$ of the true value. (The actual value is $e^{0.5} \approx 1.6487$, and the actual error is about $0.003$ -- well within our bound.)

**AP tip:** On the exam, using $M = e < 3$ (or even $M = 3$) is perfectly acceptable and much cleaner than trying to pin down a tighter bound.

---

### Example 2: Error Bound for $\sin x$ -- The Easy $M$

**Approximate $\sin(0.1)$ using $P_3(x)$ centered at $0$. Bound the error.**

The Maclaurin series for $\sin x$ is:

$$\sin x = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \cdots$$

So $P_3(x) = x - \frac{x^3}{6}$.

At $x = 0.1$:

$$P_3(0.1) = 0.1 - \frac{0.001}{6} = 0.1 - 0.000166\overline{6} = 0.099833\overline{3}$$

**Error bound:** $n = 3$, $a = 0$, $x = 0.1$.

$$|R_3(0.1)| \leq \frac{M \cdot |0.1|^4}{4!}$$

$f^{(4)}(x) = \sin x$ (since the derivatives of $\sin$ cycle: $\sin, \cos, -\sin, -\cos, \sin, \ldots$). So:

$$M = \max_{z \in [0, 0.1]} |\sin z| \leq 1$$

Using $M = 1$:

$$|R_3(0.1)| \leq \frac{1 \cdot (0.1)^4}{24} = \frac{0.0001}{24} \approx 4.17 \times 10^{-6}$$

$$\boxed{|R_3(0.1)| \leq 4.17 \times 10^{-6}}$$

That's accurate to 5 decimal places with just two non-zero terms. Factorials are incredibly powerful.

---

### Example 3: How Many Terms Do You Need?

**How many terms of the Maclaurin series for $\cos x$ are needed to approximate $\cos(1)$ with error less than $0.001$?**

The Maclaurin series for $\cos x$ is:

$$\cos x = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!} + \cdots$$

Since this is an alternating series (for $x = 1$), we can use the **Alternating Series Error Bound**: the error is at most the absolute value of the first omitted term.

We need: $\frac{|x|^{2k}}{(2k)!} < 0.001$ where we evaluate at $x = 1$.

| Terms used | First omitted term | Value |
|------------|-------------------|-------|
| $1 - \frac{1}{2}$ (2 terms) | $\frac{1}{4!} = \frac{1}{24}$ | $0.0417$ |
| $1 - \frac{1}{2} + \frac{1}{24}$ (3 terms) | $\frac{1}{6!} = \frac{1}{720}$ | $0.00139$ |
| $1 - \frac{1}{2} + \frac{1}{24} - \frac{1}{720}$ (4 terms) | $\frac{1}{8!} = \frac{1}{40320}$ | $0.0000248$ |

With **4 terms**, the first omitted term is $\frac{1}{40320} \approx 0.0000248 < 0.001$. $\checkmark$

$$\boxed{\text{4 terms are needed (through the } x^6 \text{ term)}}$$

**Note:** We could also use the Lagrange Error Bound here (with $M = 1$ since all derivatives of $\cos$ are bounded by 1), and we'd get a similar answer.

---

### Example 4: Lagrange Error Bound for $\ln(1 + x)$

**Use the 4th-degree Maclaurin polynomial for $\ln(1 + x)$ to approximate $\ln(1.5)$. Bound the error using the Lagrange Error Bound.**

The Maclaurin series for $\ln(1 + x)$ is:

$$\ln(1 + x) = x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \cdots$$

So $P_4(x) = x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4}$.

At $x = 0.5$ (since $\ln(1.5) = \ln(1 + 0.5)$):

$$P_4(0.5) = 0.5 - \frac{0.25}{2} + \frac{0.125}{3} - \frac{0.0625}{4} = 0.5 - 0.125 + 0.04167 - 0.015625 = 0.40104$$

**Error bound:** $n = 4$, $a = 0$, $x = 0.5$.

We need $f^{(5)}(x)$ for $f(x) = \ln(1 + x)$.

The derivatives of $\ln(1 + x)$:
- $f'(x) = \frac{1}{1+x} = (1+x)^{-1}$
- $f''(x) = -(1+x)^{-2}$
- $f'''(x) = 2(1+x)^{-3}$
- $f^{(4)}(x) = -6(1+x)^{-4}$
- $f^{(5)}(x) = 24(1+x)^{-5} = \frac{24}{(1+x)^5}$

So $|f^{(5)}(z)| = \frac{24}{(1+z)^5}$ for $z \in [0, 0.5]$.

This is a decreasing function, so it's maximized at $z = 0$:

$$M = \frac{24}{(1+0)^5} = 24$$

$$|R_4(0.5)| \leq \frac{24 \cdot (0.5)^5}{5!} = \frac{24 \cdot 0.03125}{120} = \frac{0.75}{120} = 0.00625$$

$$\boxed{|R_4(0.5)| \leq 0.00625}$$

The actual value is $\ln(1.5) \approx 0.40546$, and our approximation is $0.40104$, giving an actual error of about $0.0044$ -- within our bound. $\checkmark$

---

### Example 5: Taylor Polynomial Not Centered at Zero

**The function $f(x) = \sqrt{x}$ is approximated by a 2nd-degree Taylor polynomial centered at $a = 4$. Find an upper bound on the error for $|R_2(x)|$ on the interval $[3.5, 4.5]$.**

**Step 1:** Compute derivatives of $f(x) = x^{1/2}$:
- $f'(x) = \frac{1}{2}x^{-1/2}$
- $f''(x) = -\frac{1}{4}x^{-3/2}$
- $f'''(x) = \frac{3}{8}x^{-5/2}$

**Step 2:** For the Lagrange Error Bound with $n = 2$, we need $M = \max |f'''(z)|$ on $[3.5, 4.5]$.

$$|f'''(z)| = \frac{3}{8}z^{-5/2} = \frac{3}{8z^{5/2}}$$

This is a decreasing function, so it's maximized at the left endpoint $z = 3.5$:

$$M = \frac{3}{8(3.5)^{5/2}} = \frac{3}{8 \cdot 22.918} = \frac{3}{183.34} \approx 0.01636$$

**Step 3:** The maximum value of $|x - 4|$ on $[3.5, 4.5]$ is $0.5$.

$$|R_2(x)| \leq \frac{0.01636 \cdot (0.5)^3}{3!} = \frac{0.01636 \cdot 0.125}{6} = \frac{0.002045}{6} \approx 0.000341$$

$$\boxed{|R_2(x)| \leq 0.00035 \text{ on } [3.5, 4.5]}$$

So $P_2(x)$ approximates $\sqrt{x}$ to better than 4 decimal places near $x = 4$. That's like knowing the exact distance from Rancho Bernardo to Balboa Park down to the inch.

---

### Example 6: Determining Accuracy of $e$ Itself

**How many terms of the Maclaurin series are needed to compute $e = e^1$ with error less than $10^{-6}$?**

The Maclaurin series for $e^x$ at $x = 1$:

$$e = \sum_{k=0}^{n} \frac{1}{k!} + R_n(1)$$

Using the Lagrange Error Bound:

$$|R_n(1)| \leq \frac{M \cdot 1^{n+1}}{(n+1)!} = \frac{M}{(n+1)!}$$

where $M = \max_{z \in [0,1]} e^z = e^1 = e < 3$.

So we need:

$$\frac{3}{(n+1)!} < 10^{-6}$$

$$(n+1)! > 3{,}000{,}000$$

| $n$ | $(n+1)!$ | $\frac{3}{(n+1)!}$ |
|-----|----------|-------------------|
| 8 | $9! = 362{,}880$ | $8.27 \times 10^{-6}$ |
| 9 | $10! = 3{,}628{,}800$ | $8.27 \times 10^{-7}$ |

At $n = 9$ (using terms through $\frac{1}{9!}$), the error is less than $10^{-6}$.

$$\boxed{n = 9 \text{ (10 terms, through } \frac{x^9}{9!}\text{)}}$$

Just 10 terms to compute $e$ to 6 decimal places. Factorials are doing the heavy lifting here -- $10! = 3{,}628{,}800$ absolutely crushes the numerator.

---

### Example 7: Alternating Series vs. Lagrange -- A Side-by-Side Comparison

**Approximate $\sin(0.5)$ using $P_5(x)$. Bound the error using (a) the Lagrange Error Bound, and (b) the Alternating Series Error Bound.**

$P_5(x) = x - \frac{x^3}{3!} + \frac{x^5}{5!}$

At $x = 0.5$:

$$P_5(0.5) = 0.5 - \frac{0.125}{6} + \frac{0.03125}{120} = 0.5 - 0.020833 + 0.000260 = 0.479427$$

**(a) Lagrange Error Bound:**

$n = 5$, so we need $f^{(6)}(x)$. The 6th derivative of $\sin x$ is $-\sin x$.

$$M = \max_{z \in [0, 0.5]} |\sin z| \leq 1$$

$$|R_5(0.5)| \leq \frac{1 \cdot (0.5)^6}{6!} = \frac{0.015625}{720} \approx 2.17 \times 10^{-5}$$

**(b) Alternating Series Error Bound:**

The first omitted term is $-\frac{(0.5)^7}{7!}$:

$$\left|\frac{(0.5)^7}{7!}\right| = \frac{0.0078125}{5040} \approx 1.55 \times 10^{-6}$$

**Comparison:**

| Method | Error Bound |
|--------|------------|
| Lagrange | $\leq 2.17 \times 10^{-5}$ |
| Alternating Series | $\leq 1.55 \times 10^{-6}$ |

The Alternating Series bound is about **14 times tighter** here. That's because the Lagrange bound uses the 6th derivative (and $6!$), while the Alternating Series bound uses the 7th term (and $7!$). When both methods apply, the Alternating Series bound often wins.

$$\boxed{\text{Both bounds confirm high accuracy; alternating series gives the tighter bound.}}$$

---

### Example 8: AP-Style Problem -- Bounding Error from a Table

**The function $f$ has derivatives of all orders. The table below gives values of $f$ and its first four derivatives at $x = 2$.**

| | $f(2)$ | $f'(2)$ | $f''(2)$ | $f'''(2)$ | $f^{(4)}(2)$ |
|---|--------|---------|----------|-----------|--------------|
| Value | $3$ | $-1$ | $4$ | $-6$ | $10$ |

**It is known that $|f^{(5)}(z)| \leq 20$ for all $z$ in $[2, 2.5]$.**

**(a) Write the 4th-degree Taylor polynomial for $f$ centered at $x = 2$.**

$$P_4(x) = 3 + (-1)(x-2) + \frac{4}{2!}(x-2)^2 + \frac{-6}{3!}(x-2)^3 + \frac{10}{4!}(x-2)^4$$

$$P_4(x) = 3 - (x-2) + 2(x-2)^2 - (x-2)^3 + \frac{5}{12}(x-2)^4$$

**(b) Use $P_4$ to approximate $f(2.3)$ and find the maximum possible error.**

$$P_4(2.3) = 3 - (0.3) + 2(0.09) - (0.027) + \frac{5}{12}(0.0081)$$

$$= 3 - 0.3 + 0.18 - 0.027 + 0.003375 = 2.856375$$

**Error bound:**

$$|R_4(2.3)| \leq \frac{20 \cdot (0.3)^5}{5!} = \frac{20 \cdot 0.00243}{120} = \frac{0.0486}{120} = 0.000405$$

$$\boxed{f(2.3) \approx 2.856 \text{ with error} \leq 0.000405}$$

This is a classic AP free response setup. The College Board loves giving you a table and asking you to build the Taylor polynomial and bound the error.

---

## Step-by-Step Strategy for Error Bound Problems

Here's your battle plan for any Lagrange Error Bound problem on the AP exam:

**Step 1: Identify the setup.**
- What is $f(x)$? What is $n$ (degree of the polynomial)? What is $a$ (the center)? What is $x$ (the evaluation point)?

**Step 2: Compute the $(n+1)$-th derivative.**
- If $f$ is $\sin x$, $\cos x$, or $e^x$, you know the pattern. For other functions, differentiate.

**Step 3: Find $M$.**
- Determine the interval between $a$ and $x$.
- Find the maximum of $|f^{(n+1)}(z)|$ on that interval.
- For $\sin$ and $\cos$: $M = 1$ always works.
- For $e^x$: $M = e^{\text{right endpoint}}$; overestimate with $e < 3$ if helpful.
- If a bound is given in the problem, use it.

**Step 4: Plug into the formula.**

$$|R_n(x)| \leq \frac{M \cdot |x - a|^{n+1}}{(n+1)!}$$

**Step 5: Interpret.**
- If they ask "how many terms," increase $n$ until the bound is small enough.
- If they ask "is the approximation within $\epsilon$," check if the bound $\leq \epsilon$.

---

## Key Formulas & Rules

| Formula / Concept | Expression | When to Use |
|-------------------|-----------|-------------|
| Taylor remainder | $R_n(x) = f(x) - P_n(x)$ | Definition of error |
| Lagrange Error Bound | $\|R_n(x)\| \leq \dfrac{M\|x-a\|^{n+1}}{(n+1)!}$ | Bounding error for any Taylor polynomial |
| $M$ (the bound) | $M = \max_{z \text{ between } a \text{ and } x} \|f^{(n+1)}(z)\|$ | Finding the worst-case next derivative |
| Alternating Series Error | $\|S - S_n\| \leq a_{n+1}$ | When the series alternates and decreases |
| $\sin x$ and $\cos x$ bound | $M = 1$ (all derivatives $\leq 1$) | Any error bound involving sin or cos |
| $e^x$ bound | $M = e^{\max}$ (use $e < 3$ for clean computation) | Any error bound involving $e^x$ |
| Factorial growth | $(n+1)!$ grows faster than any $x^{n+1}$ | Why Taylor series converge so well |

---

## Common Mistakes to Avoid

**1. Using the wrong derivative for $M$**

> **Wrong:** Using $f^{(n)}(x)$ to find $M$.
>
> **Right:** Using $f^{(n+1)}(x)$ -- the *next* derivative after the degree of your polynomial.

If your Taylor polynomial is degree 4, you need the **5th** derivative to bound the error. The $(n+1)$ is easy to mess up under exam pressure.

**2. Forgetting the absolute value around $x - a$**

> **Wrong:** $|R_n(x)| \leq \frac{M(x - a)^{n+1}}{(n+1)!}$ when $x < a$
>
> **Right:** $|R_n(x)| \leq \frac{M|x - a|^{n+1}}{(n+1)!}$

If $x < a$, then $(x - a)$ is negative. Raising a negative number to an odd power gives a negative result. Always use $|x - a|$.

**3. Finding $M$ at the center instead of the maximum on the interval**

> **Wrong:** "$f^{(n+1)}(a) = 5$, so $M = 5$."
>
> **Right:** $M$ is the **maximum** of $|f^{(n+1)}(z)|$ over the *entire interval* from $a$ to $x$, not just at the center.

For $e^x$, the max is at the right endpoint (because $e^x$ is increasing). For $\frac{1}{(1+x)^5}$, the max might be at the left endpoint.

**4. Confusing when to use Alternating Series Error Bound vs. Lagrange**

> **Wrong:** Using the Alternating Series Error Bound on a series that doesn't alternate.
>
> **Right:** The Alternating Series Error Bound only works when the series alternates in sign, terms decrease in absolute value, and terms approach 0.

$e^x = 1 + x + \frac{x^2}{2} + \cdots$ does **not** alternate (for $x > 0$), so you must use Lagrange.

**5. Over-complicating $M$ when a simple bound exists**

> **Wrong:** Trying to find the exact maximum of $|\cos z|$ on $[0, 0.3]$ by computing $\cos(0) = 1$ and $\cos(0.3) = 0.955\ldots$ and determining the max.
>
> **Right:** All derivatives of $\sin$ and $\cos$ are at most 1 in absolute value. Use $M = 1$.

The AP exam rewards efficiency. A bound doesn't have to be tight -- it just has to be correct. Using $M = 1$ for trig functions is always valid and saves time.

**6. Forgetting that error bound gives an UPPER bound, not the exact error**

> **Wrong:** "The error is exactly $\frac{M|x-a|^{n+1}}{(n+1)!}$."
>
> **Right:** "The error is **at most** $\frac{M|x-a|^{n+1}}{(n+1)!}$."

The Lagrange Error Bound is a worst-case guarantee. The actual error is usually smaller.

---

## AP Exam Tips

1. **This topic appears almost every year on the BC exam.** It's typically part of the Series free response question (usually Question 6). Expect to write a Taylor polynomial, then bound the error -- often for 2-3 points of the question.

2. **Show the formula before plugging in.** Write $|R_n(x)| \leq \frac{M|x-a|^{n+1}}{(n+1)!}$ before substituting values. This earns method points even if your arithmetic is wrong.

3. **State your value of $M$ and justify it.** Don't just write $M = 1$. Write: "Since all derivatives of $\sin x$ are at most 1 in absolute value, $M = 1$." The justification is where the points are.

4. **When finding how many terms are needed,** set up the inequality and solve. Show: "We need $\frac{1 \cdot (0.5)^{n+1}}{(n+1)!} < 0.001$," then test values of $n$ until the inequality is satisfied.

5. **Know the connection to convergence.** If the Lagrange Error Bound $\to 0$ as $n \to \infty$, then the Taylor series converges to $f(x)$ at that point. This is how you *prove* that $e^x = \sum \frac{x^n}{n!}$ (not just that the series converges, but that it converges to $e^x$).

6. **Table problems are common.** The problem gives you $f(a), f'(a), f''(a), \ldots$ in a table and tells you $|f^{(n+1)}(z)| \leq M$ for all $z$ in some interval. All you need to do is build $P_n$, evaluate it, and apply the formula.

7. **Calculator section:** You may be asked to verify an approximation numerically. Know how to compute partial sums of Taylor series on your calculator.

8. **Don't confuse the degree of the polynomial with the number of non-zero terms.** For $\sin x$, the 5th-degree Maclaurin polynomial $P_5(x) = x - \frac{x^3}{6} + \frac{x^5}{120}$ has only 3 non-zero terms but is degree 5. The Lagrange Error Bound uses $n = 5$, not $n = 3$.

---

## Practice Problems

### Basic (1-5)

**Problem 1.** The Maclaurin polynomial $P_2(x) = 1 + x + \frac{x^2}{2}$ approximates $e^x$. Use the Lagrange Error Bound to find the maximum error when approximating $e^{0.1}$.

**Problem 2.** The Maclaurin polynomial $P_3(x) = x - \frac{x^3}{6}$ approximates $\sin x$. Find an upper bound on $|R_3(0.5)|$.

**Problem 3.** How many terms of the Maclaurin series $e^x = \sum \frac{x^n}{n!}$ are needed to approximate $e^{0.1}$ with error less than $10^{-8}$?

**Problem 4.** The Maclaurin series for $\cos x$ is $1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \cdots$. Use the Alternating Series Error Bound to determine how many terms are needed to approximate $\cos(0.2)$ with error less than $10^{-5}$.

**Problem 5.** For $f(x) = \ln(1 + x)$, compute $P_3(0.1)$ and use the Lagrange Error Bound to find the maximum error.

### Intermediate (6-10)

**Problem 6.** Use the Lagrange Error Bound to show that $|R_4(0.5)| < 0.003$ for the Maclaurin series of $e^x$.

**Problem 7.** The 5th-degree Maclaurin polynomial for $\sin x$ is $P_5(x) = x - \frac{x^3}{6} + \frac{x^5}{120}$. Bound the error when using $P_5$ to approximate $\sin(1)$ using both the Lagrange Error Bound and the Alternating Series Error Bound. Which gives the tighter bound?

**Problem 8.** How many terms of the Maclaurin series for $\ln(1 + x)$ are needed to approximate $\ln(1.2)$ with error less than $0.0001$?

**Problem 9.** The function $f(x) = \cos x$ is approximated by $P_4(x) = 1 - \frac{x^2}{2} + \frac{x^4}{24}$ centered at $a = 0$. For what values of $x$ is the error guaranteed to be less than $0.001$?

**Problem 10.** For $f(x) = e^{-x}$, write the 3rd-degree Maclaurin polynomial and use the Lagrange Error Bound to determine the maximum error when approximating $e^{-0.5}$.

### Advanced (11-15)

**Problem 11.** The function $f$ has derivatives of all orders. You are given that $f(1) = 2$, $f'(1) = -3$, $f''(1) = 5$, $f'''(1) = -8$, and $|f^{(4)}(z)| \leq 15$ for all $z$ in $[1, 1.5]$. Approximate $f(1.2)$ using $P_3(x)$ centered at $a = 1$ and bound the error.

**Problem 12.** The Taylor series for $e^x$ centered at $a = 1$ is $e + e(x-1) + \frac{e}{2}(x-1)^2 + \cdots$. Use the Lagrange Error Bound with $n = 2$ to bound the error when approximating $e^{1.5}$ with the 2nd-degree Taylor polynomial centered at $a = 1$.

**Problem 13.** Prove that the Maclaurin series for $\cos x$ converges to $\cos x$ for all real numbers $x$. (Hint: Show that the Lagrange Error Bound approaches 0 as $n \to \infty$.)

**Problem 14.** Find the smallest value of $n$ such that the $n$-th degree Maclaurin polynomial for $\sin x$ approximates $\sin(2)$ with error less than $10^{-4}$.

**Problem 15.** The Maclaurin series for $\arctan x$ is $x - \frac{x^3}{3} + \frac{x^5}{5} - \cdots$ (valid for $|x| \leq 1$). Use the Alternating Series Error Bound to determine how many terms are needed to approximate $\arctan(0.5)$ with error less than $0.001$.

### AP Exam Practice (16-20)

**Problem 16.** (Multiple Choice) The third-degree Maclaurin polynomial for $f(x) = e^{2x}$ is $P_3(x) = 1 + 2x + 2x^2 + \frac{4x^3}{3}$. According to the Lagrange Error Bound, $|R_3(0.1)|$ is at most:

| Choice | Answer |
|--------|--------|
| (A) | $\frac{16 \cdot e^{0.2} \cdot (0.1)^4}{4!}$ |
| (B) | $\frac{16(0.1)^4}{4!}$ |
| (C) | $\frac{8 \cdot e^{0.2} \cdot (0.1)^3}{3!}$ |
| (D) | $\frac{e^{0.2}(0.1)^4}{4!}$ |

**Problem 17.** (Multiple Choice) The Maclaurin series for $\sin x$ is used to approximate $\sin(0.3)$. What is the least degree of the Maclaurin polynomial that guarantees the approximation is within $10^{-4}$ of the true value?

| Choice | Answer |
|--------|--------|
| (A) | 3 |
| (B) | 4 |
| (C) | 5 |
| (D) | 7 |

**Problem 18.** (Multiple Choice) If $P_5(x)$ is the 5th-degree Taylor polynomial for $\cos x$ centered at $x = 0$, then the Lagrange Error Bound for $|\cos(0.5) - P_5(0.5)|$ is:

| Choice | Answer |
|--------|--------|
| (A) | $\frac{(0.5)^5}{5!}$ |
| (B) | $\frac{(0.5)^6}{6!}$ |
| (C) | $\frac{(0.5)^7}{7!}$ |
| (D) | $\frac{(0.5)^6}{5!}$ |

**Problem 19.** (Free Response) Let $f$ be a function with derivatives of all orders, and let $P_3(x)$ be the third-degree Taylor polynomial for $f$ about $x = 0$. The Maclaurin series for $f$ is given by:

$$f(x) = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n}}{(2n)!}$$

> (a) Write $P_3(x)$.
>
> (b) Use $P_3$ to approximate $f(0.5)$.
>
> (c) Use the Lagrange Error Bound to show that this approximation differs from $f(0.5)$ by less than $\frac{1}{300}$.
>
> (d) Could you use the Alternating Series Error Bound instead? If so, find that bound and compare it to the Lagrange bound.

**Problem 20.** (Free Response) Ganga is approximating the value of $e^{-0.3}$ for a Science Olympiad problem. She uses the $n$-th degree Maclaurin polynomial for $e^x$.

> (a) Write the 4th-degree Maclaurin polynomial for $e^x$ and use it to approximate $e^{-0.3}$.
>
> (b) Use the Lagrange Error Bound to find the maximum error in this approximation. (Hint: what is $M$ for $f(x) = e^x$ on the interval $[-0.3, 0]$?)
>
> (c) How many terms of the Maclaurin series does Ganga need to guarantee her approximation of $e^{-0.3}$ is accurate to within $10^{-7}$?
>
> (d) An alternative approach: the Maclaurin series for $e^{-x}$ is an alternating series for $x > 0$. Use the Alternating Series Error Bound with the 4th-degree polynomial for $e^{-x}$ to bound the error. Is this bound tighter than the Lagrange bound from part (b)?

---

## Answer Key

<details>
<summary><strong>Problem 1 Solution</strong></summary>

**Lagrange Error Bound for $P_2(x) = 1 + x + \frac{x^2}{2}$ approximating $e^{0.1}$.**

Here $n = 2$, $a = 0$, $x = 0.1$.

We need $f^{(3)}(x) = e^x$. On $[0, 0.1]$:

$$M = \max_{z \in [0, 0.1]} e^z = e^{0.1} < e < 3$$

$$|R_2(0.1)| \leq \frac{3 \cdot (0.1)^3}{3!} = \frac{3 \cdot 0.001}{6} = \frac{0.003}{6} = \boxed{0.0005}$$

So $P_2(0.1) = 1 + 0.1 + 0.005 = 1.105$ approximates $e^{0.1}$ with error at most $0.0005$. (The actual value is $e^{0.1} \approx 1.10517$.)

</details>

---

<details>
<summary><strong>Problem 2 Solution</strong></summary>

**Upper bound on $|R_3(0.5)|$ for $\sin x$.**

$n = 3$, $a = 0$, $x = 0.5$.

$f^{(4)}(x) = \sin x$, so $M = 1$ (since $|\sin z| \leq 1$ for all $z$).

$$|R_3(0.5)| \leq \frac{1 \cdot (0.5)^4}{4!} = \frac{0.0625}{24} \approx \boxed{0.0026}$$

</details>

---

<details>
<summary><strong>Problem 3 Solution</strong></summary>

**How many terms to approximate $e^{0.1}$ with error less than $10^{-8}$?**

We need $\frac{M \cdot (0.1)^{n+1}}{(n+1)!} < 10^{-8}$, where $M = e^{0.1} < 3$.

$$\frac{3 \cdot (0.1)^{n+1}}{(n+1)!} < 10^{-8}$$

$$\frac{3 \cdot 10^{-(n+1)}}{(n+1)!} < 10^{-8}$$

$$\frac{3}{(n+1)! \cdot 10^{n+1}} < 10^{-8}$$

Test values:

| $n$ | $(n+1)!$ | $\frac{3}{(n+1)! \cdot 10^{n+1}}$ |
|-----|----------|-------------------------------|
| 3 | $24$ | $\frac{3}{24 \cdot 10{,}000} = 1.25 \times 10^{-5}$ |
| 4 | $120$ | $\frac{3}{120 \cdot 100{,}000} = 2.5 \times 10^{-7}$ |
| 5 | $720$ | $\frac{3}{720 \cdot 1{,}000{,}000} = 4.17 \times 10^{-9}$ |

At $n = 5$: $4.17 \times 10^{-9} < 10^{-8}$. $\checkmark$

$$\boxed{n = 5 \text{ (6 terms, through } \frac{x^5}{5!}\text{)}}$$

</details>

---

<details>
<summary><strong>Problem 4 Solution</strong></summary>

**How many terms of the $\cos x$ series for $\cos(0.2)$ with error less than $10^{-5}$?**

The Maclaurin series for $\cos x$ at $x = 0.2$:

$$\cos(0.2) = 1 - \frac{(0.2)^2}{2!} + \frac{(0.2)^4}{4!} - \frac{(0.2)^6}{6!} + \cdots$$

This is an alternating series. The error is at most the first omitted term:

| Terms used | First omitted term | Value |
|------------|-------------------|-------|
| $1$ (1 term) | $\frac{(0.2)^2}{2!} = 0.02$ | Too large |
| $1 - 0.02$ (2 terms) | $\frac{(0.2)^4}{4!} = \frac{0.0016}{24} \approx 6.67 \times 10^{-5}$ | Too large |
| 3 terms | $\frac{(0.2)^6}{6!} = \frac{6.4 \times 10^{-5}}{720} \approx 8.89 \times 10^{-8}$ | $< 10^{-5}$ $\checkmark$ |

$$\boxed{3 \text{ terms (through } \frac{x^4}{4!}\text{)}}$$

</details>

---

<details>
<summary><strong>Problem 5 Solution</strong></summary>

**$P_3(0.1)$ for $\ln(1 + x)$ and Lagrange Error Bound.**

$$P_3(x) = x - \frac{x^2}{2} + \frac{x^3}{3}$$

$$P_3(0.1) = 0.1 - \frac{0.01}{2} + \frac{0.001}{3} = 0.1 - 0.005 + 0.000333 = 0.095333$$

For the error bound: $n = 3$, $a = 0$, $x = 0.1$.

$f^{(4)}(x)$ for $f(x) = \ln(1+x)$:

$$f^{(4)}(x) = \frac{-6}{(1+x)^4}$$

$$|f^{(4)}(z)| = \frac{6}{(1+z)^4}$$

On $[0, 0.1]$, this is maximized at $z = 0$: $M = \frac{6}{1} = 6$.

$$|R_3(0.1)| \leq \frac{6 \cdot (0.1)^4}{4!} = \frac{6 \cdot 0.0001}{24} = \frac{0.0006}{24} = \boxed{0.000025}$$

The actual value is $\ln(1.1) \approx 0.095310$, and $|0.095333 - 0.095310| = 0.000023$, which is within our bound. $\checkmark$

</details>

---

<details>
<summary><strong>Problem 6 Solution</strong></summary>

**Show $|R_4(0.5)| < 0.003$ for the Maclaurin series of $e^x$.**

$n = 4$, $a = 0$, $x = 0.5$.

$f^{(5)}(x) = e^x$. On $[0, 0.5]$: $M = e^{0.5} < e < 3$.

$$|R_4(0.5)| \leq \frac{3 \cdot (0.5)^5}{5!} = \frac{3 \cdot 0.03125}{120} = \frac{0.09375}{120} = 0.00078125$$

Since $0.00078125 < 0.003$:

$$\boxed{|R_4(0.5)| \leq 0.00078 < 0.003 \quad \checkmark}$$

</details>

---

<details>
<summary><strong>Problem 7 Solution</strong></summary>

**Bound error of $P_5$ approximating $\sin(1)$ -- Lagrange vs. Alternating Series.**

**Lagrange Error Bound:**

$n = 5$, $a = 0$, $x = 1$. $f^{(6)}(x) = -\sin x$, so $M = 1$.

$$|R_5(1)| \leq \frac{1 \cdot 1^6}{6!} = \frac{1}{720} \approx 0.001389$$

**Alternating Series Error Bound:**

The first omitted term (after $P_5$) is $-\frac{x^7}{7!}$:

$$\left|\frac{1^7}{7!}\right| = \frac{1}{5040} \approx 0.000198$$

**Comparison:**

| Method | Bound |
|--------|-------|
| Lagrange | $0.001389$ |
| Alternating Series | $0.000198$ |

$$\boxed{\text{Alternating Series gives the tighter bound: } 0.000198 \text{ vs. } 0.001389}$$

The Alternating Series bound is about 7 times tighter because it effectively uses the 7th-degree information rather than the 6th.

</details>

---

<details>
<summary><strong>Problem 8 Solution</strong></summary>

**How many terms for $\ln(1.2)$ with error less than $0.0001$?**

$\ln(1.2) = \ln(1 + 0.2)$, and the Maclaurin series is:

$$\ln(1 + x) = x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \cdots = \sum_{k=1}^{n} \frac{(-1)^{k+1} x^k}{k}$$

This is an alternating series for $x = 0.2 > 0$. Using the Alternating Series Error Bound, the error after $n$ terms is at most:

$$\frac{(0.2)^{n+1}}{n+1}$$

| $n$ | First omitted term | Value |
|-----|-------------------|-------|
| 3 | $\frac{(0.2)^4}{4} = \frac{0.0016}{4}$ | $0.0004$ |
| 4 | $\frac{(0.2)^5}{5} = \frac{0.00032}{5}$ | $0.000064$ |

At $n = 4$: $0.000064 < 0.0001$. $\checkmark$

$$\boxed{4 \text{ terms (through } \frac{x^4}{4}\text{)}}$$

</details>

---

<details>
<summary><strong>Problem 9 Solution</strong></summary>

**For what values of $x$ is $|R_4(x)| < 0.001$ for $P_4(x)$ approximating $\cos x$?**

$n = 4$, $a = 0$. $f^{(5)}(x) = -\sin x$, so $M = 1$.

$$|R_4(x)| \leq \frac{1 \cdot |x|^5}{5!} = \frac{|x|^5}{120}$$

We need:

$$\frac{|x|^5}{120} < 0.001$$

$$|x|^5 < 0.12$$

$$|x| < (0.12)^{1/5}$$

Computing: $0.12^{1/5} = e^{\frac{1}{5}\ln(0.12)} = e^{\frac{1}{5}(-2.12)} = e^{-0.424} \approx 0.655$

$$\boxed{|x| < 0.655, \text{ i.e., } -0.655 < x < 0.655}$$

Within this interval, $P_4(x)$ approximates $\cos x$ with error less than $0.001$.

</details>

---

<details>
<summary><strong>Problem 10 Solution</strong></summary>

**3rd-degree Maclaurin polynomial for $e^{-x}$ and Lagrange Error Bound at $x = 0.5$.**

$f(x) = e^{-x}$, so:
- $f(0) = 1$
- $f'(x) = -e^{-x}$, $f'(0) = -1$
- $f''(x) = e^{-x}$, $f''(0) = 1$
- $f'''(x) = -e^{-x}$, $f'''(0) = -1$

$$P_3(x) = 1 - x + \frac{x^2}{2} - \frac{x^3}{6}$$

$$P_3(0.5) = 1 - 0.5 + 0.125 - 0.02083 = 0.60417$$

For the error bound: $n = 3$, $a = 0$, $x = 0.5$.

$f^{(4)}(x) = e^{-x}$. On $[0, 0.5]$: $|f^{(4)}(z)| = e^{-z}$.

Since $e^{-z}$ is decreasing, $M = e^{0} = 1$.

$$|R_3(0.5)| \leq \frac{1 \cdot (0.5)^4}{4!} = \frac{0.0625}{24} \approx \boxed{0.0026}$$

The actual value is $e^{-0.5} \approx 0.60653$, and the actual error is $|0.60653 - 0.60417| = 0.00236$, which is within our bound. $\checkmark$

</details>

---

<details>
<summary><strong>Problem 11 Solution</strong></summary>

**Approximate $f(1.2)$ using $P_3(x)$ centered at $a = 1$ and bound the error.**

$$P_3(x) = 2 + (-3)(x-1) + \frac{5}{2!}(x-1)^2 + \frac{-8}{3!}(x-1)^3$$

$$= 2 - 3(x-1) + \frac{5}{2}(x-1)^2 - \frac{4}{3}(x-1)^3$$

At $x = 1.2$ (so $x - 1 = 0.2$):

$$P_3(1.2) = 2 - 3(0.2) + \frac{5}{2}(0.04) - \frac{4}{3}(0.008)$$

$$= 2 - 0.6 + 0.1 - 0.01067 = 1.48933$$

**Error bound:** $n = 3$, $|x - a| = 0.2$, $M = 15$ (given that $|f^{(4)}(z)| \leq 15$ on $[1, 1.5]$).

$$|R_3(1.2)| \leq \frac{15 \cdot (0.2)^4}{4!} = \frac{15 \cdot 0.0016}{24} = \frac{0.024}{24} = \boxed{0.001}$$

$$f(1.2) \approx 1.489 \text{ with error} \leq 0.001$$

</details>

---

<details>
<summary><strong>Problem 12 Solution</strong></summary>

**Lagrange Error Bound for $e^{1.5}$ using the 2nd-degree Taylor polynomial centered at $a = 1$.**

$P_2(x) = e + e(x-1) + \frac{e}{2}(x-1)^2$

For $f(x) = e^x$: all derivatives are $e^x$, so $f^{(3)}(z) = e^z$.

$n = 2$, $a = 1$, $x = 1.5$. On $[1, 1.5]$:

$$M = \max_{z \in [1, 1.5]} e^z = e^{1.5}$$

Since we're trying to bound the error, we can overestimate: $e^{1.5} < e^2 < 3^2 = 9$. (Or more tightly, $e^{1.5} \approx 4.48$, so use $M = 5$ for a clean bound.)

Using $M = 5$:

$$|R_2(1.5)| \leq \frac{5 \cdot (0.5)^3}{3!} = \frac{5 \cdot 0.125}{6} = \frac{0.625}{6} \approx \boxed{0.1042}$$

This is a relatively large error because $x = 1.5$ is a half-unit away from the center and we only used a 2nd-degree polynomial. More terms would dramatically improve accuracy.

</details>

---

<details>
<summary><strong>Problem 13 Solution</strong></summary>

**Prove the Maclaurin series for $\cos x$ converges to $\cos x$ for all $x$.**

We need to show that $R_n(x) \to 0$ as $n \to \infty$ for every real number $x$.

All derivatives of $\cos x$ are $\pm \sin x$ or $\pm \cos x$, so $|f^{(n+1)}(z)| \leq 1$ for all $z$ and all $n$.

By the Lagrange Error Bound:

$$|R_n(x)| \leq \frac{1 \cdot |x|^{n+1}}{(n+1)!}$$

We need to show $\frac{|x|^{n+1}}{(n+1)!} \to 0$ as $n \to \infty$ for any fixed $x$.

**Proof:** For any fixed $x$, consider the ratio of consecutive terms:

$$\frac{|x|^{n+2}/(n+2)!}{|x|^{n+1}/(n+1)!} = \frac{|x|}{n+2}$$

For $n$ large enough, $\frac{|x|}{n+2} < \frac{1}{2}$, so the terms decrease geometrically. A sequence that eventually decreases by at least half at each step converges to 0.

Alternatively, we know $\sum_{n=0}^{\infty} \frac{|x|^n}{n!} = e^{|x|}$ converges, so the terms $\frac{|x|^n}{n!} \to 0$.

Therefore $|R_n(x)| \to 0$, which means:

$$\cos x = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n}}{(2n)!} \quad \text{for all } x \in \mathbb{R}$$

$$\boxed{\text{The Maclaurin series for } \cos x \text{ converges to } \cos x \text{ for all } x.}$$

</details>

---

<details>
<summary><strong>Problem 14 Solution</strong></summary>

**Smallest $n$ so $P_n(x)$ approximates $\sin(2)$ with error less than $10^{-4}$.**

The Maclaurin series for $\sin x$ at $x = 2$:

$$\sin(2) = 2 - \frac{8}{6} + \frac{32}{120} - \frac{128}{5040} + \cdots$$

Using the Lagrange Error Bound with $M = 1$:

$$|R_n(2)| \leq \frac{2^{n+1}}{(n+1)!} < 10^{-4}$$

| $n$ | $\frac{2^{n+1}}{(n+1)!}$ |
|-----|--------------------------|
| 5 | $\frac{64}{720} = 0.0889$ |
| 7 | $\frac{256}{40320} = 0.00635$ |
| 9 | $\frac{1024}{3628800} = 0.000282$ |
| 11 | $\frac{4096}{479001600} = 8.55 \times 10^{-6}$ |

At $n = 11$: $8.55 \times 10^{-6} < 10^{-4}$. $\checkmark$

But we can also try the Alternating Series bound (since $\sin x$ alternates). Note that the Maclaurin series for $\sin(2)$ has non-zero terms at degrees $1, 3, 5, 7, \ldots$. Using the alternating series error (first omitted term):

After $P_9$: first omitted non-zero term is $\frac{2^{11}}{11!} = \frac{2048}{39916800} = 5.13 \times 10^{-5} < 10^{-4}$. $\checkmark$

So with the Alternating Series bound, $n = 9$ suffices.

$$\boxed{n = 9 \text{ (using Alternating Series bound) or } n = 11 \text{ (using Lagrange bound)}}$$

Since the problem asks for the smallest $n$ such that the approximation is within $10^{-4}$, and we can use either method, the answer is $n = 9$.

</details>

---

<details>
<summary><strong>Problem 15 Solution</strong></summary>

**How many terms for $\arctan(0.5)$ with error less than $0.001$?**

$$\arctan(0.5) = 0.5 - \frac{(0.5)^3}{3} + \frac{(0.5)^5}{5} - \frac{(0.5)^7}{7} + \cdots$$

This is an alternating series with decreasing terms (since $|x| = 0.5 < 1$). By the Alternating Series Error Bound, the error after $n$ terms is at most the absolute value of the $(n+1)$-th term.

| $n$ | First omitted term | Value |
|-----|-------------------|-------|
| 1 | $\frac{(0.5)^3}{3}$ | $0.04167$ |
| 2 | $\frac{(0.5)^5}{5}$ | $0.00625$ |
| 3 | $\frac{(0.5)^7}{7}$ | $0.001116$ |
| 4 | $\frac{(0.5)^9}{9}$ | $0.000217$ |

At $n = 4$: $0.000217 < 0.001$. $\checkmark$

$$\boxed{4 \text{ terms}}$$

$\arctan(0.5) \approx 0.5 - 0.04167 + 0.00625 - 0.001116 = 0.46347$

(Actual: $\arctan(0.5) \approx 0.46365$.)

</details>

---

<details>
<summary><strong>Problem 16 Solution</strong></summary>

**Answer: (A)** $\frac{16 \cdot e^{0.2} \cdot (0.1)^4}{4!}$

For $f(x) = e^{2x}$:

$f^{(4)}(x) = 2^4 e^{2x} = 16e^{2x}$

On $[0, 0.1]$: $M = 16e^{2(0.1)} = 16e^{0.2}$.

$$|R_3(0.1)| \leq \frac{16e^{0.2} \cdot (0.1)^4}{4!}$$

This matches **(A)**.

Why not (B)? Choice (B) omits the $e^{0.2}$ factor, which means it doesn't correctly account for $M$.

Why not (D)? Choice (D) uses $e^{0.2}$ but forgets the factor of $16$ from the chain rule ($f^{(4)}(x) = 16e^{2x}$, not $e^{2x}$).

$\boxed{\text{(A)}}$

</details>

---

<details>
<summary><strong>Problem 17 Solution</strong></summary>

**Answer: (A) 3**

Using the Lagrange Error Bound with $M = 1$ (all derivatives of $\sin x$ are bounded by 1):

$$|R_n(0.3)| \leq \frac{(0.3)^{n+1}}{(n+1)!}$$

| $n$ | $\frac{(0.3)^{n+1}}{(n+1)!}$ |
|-----|--------------------------|
| 2 | $\frac{0.027}{6} = 0.0045$ |
| 3 | $\frac{0.0081}{24} = 0.0003375$ |

At $n = 3$: $0.0003375 < 10^{-4} = 0.0001$?

Wait, $0.0003375 > 0.0001$. Let's check $n = 4$:

$$\frac{(0.3)^5}{5!} = \frac{0.00243}{120} = 0.00002025 < 10^{-4} \quad \checkmark$$

But actually, we should note that for $\sin x$, $P_3(x) = x - \frac{x^3}{6}$ and $P_4(x) = x - \frac{x^3}{6}$ (the $x^4$ term is zero). So $P_3 = P_4$, and the Lagrange bound for $n = 3$ asks about $f^{(4)}$, while the bound for $n = 4$ asks about $f^{(5)}$.

With $n = 3$: $|R_3(0.3)| \leq \frac{(0.3)^4}{4!} = \frac{0.0081}{24} = 0.0003375$. Not yet below $10^{-4}$.

With $n = 4$: $|R_4(0.3)| \leq \frac{(0.3)^5}{5!} = \frac{0.00243}{120} = 0.00002025 < 10^{-4}$. $\checkmark$

But the question asks for the least *degree*, and $P_3 = P_4$ for $\sin x$. So degree 3 uses the same polynomial as degree 4. The Lagrange bound with degree 3 gives $0.0003375$, which is NOT less than $10^{-4}$.

However, we need to think about this more carefully. The $n = 3$ error bound is $3.375 \times 10^{-4}$, which is greater than $10^{-4}$, so $n = 3$ does not guarantee the desired accuracy based on the Lagrange bound.

With $n = 4$ (or equivalently $n = 3$ paired with the Alternating Series bound where the next nonzero term is $\frac{(0.3)^5}{5!}$), we get error $< 10^{-4}$.

The question specifically asks about the Maclaurin polynomial degree. The degree-3 polynomial $P_3(x) = x - \frac{x^3}{6}$ is the same as $P_4(x)$. The Lagrange Error Bound at degree 3 gives $\frac{(0.3)^4}{4!} = 3.375 \times 10^{-4}$, which does not guarantee error $< 10^{-4}$.

But we note that $f^{(4)}(x) = \sin x$, so actually on $[0, 0.3]$, $M = \sin(0.3) < 0.3$. Using this tighter bound:

$$|R_3(0.3)| \leq \frac{0.3 \cdot (0.3)^4}{4!} = \frac{(0.3)^5}{24} = \frac{0.00243}{24} = 0.00010125$$

Still barely above $10^{-4}$. So $n = 3$ is borderline.

The safest answer the AP exam expects: using $M = 1$ (the standard bound), the least degree that guarantees error $< 10^{-4}$ via Lagrange is degree 3, since $\frac{1 \cdot (0.3)^4}{4!} = 3.375 \times 10^{-4}$ doesn't quite work, but we can observe that $P_3 = P_4$ and the degree-4 Lagrange bound gives $2.025 \times 10^{-5}$.

The answer is $\boxed{\text{(A)} \; n = 3}$, because a 3rd-degree Maclaurin polynomial for $\sin x$ is the same as the 4th-degree polynomial (the $x^4$ coefficient is 0), so using the Lagrange bound with $n = 4$ gives error $\frac{(0.3)^5}{5!} = 2.03 \times 10^{-5} < 10^{-4}$.

</details>

---

<details>
<summary><strong>Problem 18 Solution</strong></summary>

**Answer: (B)** $\frac{(0.5)^6}{6!}$

The 5th-degree Maclaurin polynomial for $\cos x$ is:

$$P_5(x) = 1 - \frac{x^2}{2!} + \frac{x^4}{4!}$$

(The $x^1, x^3, x^5$ coefficients are all zero for $\cos x$.)

Using the Lagrange Error Bound with $n = 5$:

$$|R_5(0.5)| \leq \frac{M \cdot (0.5)^6}{6!}$$

$f^{(6)}(x) = -\cos x$, so $M = \max|{-\cos z}| = 1$ on $[0, 0.5]$.

$$|R_5(0.5)| \leq \frac{1 \cdot (0.5)^6}{6!} = \frac{(0.5)^6}{6!}$$

$\boxed{\text{(B)}}$

Note: Some students incorrectly use $n = 4$ because $P_5 = P_4$ for $\cos x$ (the $x^5$ term is zero). But the problem says "$P_5(x)$ is the 5th-degree Taylor polynomial," so we use $n = 5$, giving $\frac{(0.5)^6}{6!}$.

</details>

---

<details>
<summary><strong>Problem 19 Solution</strong></summary>

The series $\sum_{n=0}^{\infty} \frac{(-1)^n x^{2n}}{(2n)!} = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \cdots$ is the Maclaurin series for $\cos x$. So $f(x) = \cos x$.

**(a)** $P_3(x)$ includes all terms up through degree 3:

$$P_3(x) = 1 - \frac{x^2}{2!} = 1 - \frac{x^2}{2}$$

(The $x^1$ and $x^3$ terms are zero.)

$$\boxed{P_3(x) = 1 - \frac{x^2}{2}}$$

**(b)** Approximate $f(0.5)$:

$$P_3(0.5) = 1 - \frac{(0.5)^2}{2} = 1 - \frac{0.25}{2} = 1 - 0.125 = \boxed{0.875}$$

**(c)** Lagrange Error Bound with $n = 3$, $a = 0$, $x = 0.5$:

$f^{(4)}(x) = \cos x$, so $M = \max_{z \in [0, 0.5]} |\cos z| \leq 1$.

$$|R_3(0.5)| \leq \frac{1 \cdot (0.5)^4}{4!} = \frac{0.0625}{24} = \frac{1}{384} \approx 0.00260$$

Is $\frac{1}{384} < \frac{1}{300}$?

$\frac{1}{384} < \frac{1}{300}$ since $384 > 300$. $\checkmark$

$$\boxed{|R_3(0.5)| \leq \frac{1}{384} < \frac{1}{300}}$$

**(d)** The series $1 - \frac{(0.5)^2}{2!} + \frac{(0.5)^4}{4!} - \cdots$ is alternating with decreasing terms. By the Alternating Series Error Bound, the error after $P_3$ (which uses terms through $n = 1$ in the series, i.e., $1 - \frac{x^2}{2}$) is at most the next term:

$$\left|\frac{(0.5)^4}{4!}\right| = \frac{0.0625}{24} = \frac{1}{384} \approx 0.00260$$

In this case, both bounds give the same value: $\frac{1}{384}$. This happens because $M = 1$ for $\cos x$ and the Lagrange bound with $n = 3$ reduces to $\frac{|x|^4}{4!}$, which is exactly the absolute value of the first omitted term.

$$\boxed{\text{Both bounds give } \frac{1}{384}; \text{ they are equal here.}}$$

</details>

---

<details>
<summary><strong>Problem 20 Solution</strong></summary>

**(a)** The 4th-degree Maclaurin polynomial for $e^x$:

$$P_4(x) = 1 + x + \frac{x^2}{2} + \frac{x^3}{6} + \frac{x^4}{24}$$

At $x = -0.3$:

$$P_4(-0.3) = 1 + (-0.3) + \frac{0.09}{2} + \frac{-0.027}{6} + \frac{0.0081}{24}$$

$$= 1 - 0.3 + 0.045 - 0.0045 + 0.0003375$$

$$= \boxed{0.7408375}$$

**(b)** Lagrange Error Bound: $n = 4$, $a = 0$, $x = -0.3$.

$f^{(5)}(x) = e^x$. On $[-0.3, 0]$: $|f^{(5)}(z)| = e^z$, which is maximized at $z = 0$.

$$M = e^0 = 1$$

$$|R_4(-0.3)| \leq \frac{1 \cdot |-0.3|^5}{5!} = \frac{(0.3)^5}{120} = \frac{0.00243}{120} = \boxed{0.00002025}$$

**(c)** We need $\frac{1 \cdot (0.3)^{n+1}}{(n+1)!} < 10^{-7}$ (using $M = 1$).

| $n$ | $\frac{(0.3)^{n+1}}{(n+1)!}$ |
|-----|--------------------------|
| 4 | $\frac{0.00243}{120} = 2.025 \times 10^{-5}$ |
| 5 | $\frac{0.000729}{720} = 1.0125 \times 10^{-6}$ |
| 6 | $\frac{0.0002187}{5040} = 4.34 \times 10^{-8}$ |

At $n = 6$: $4.34 \times 10^{-8} < 10^{-7}$. $\checkmark$

$$\boxed{n = 6 \text{ (7 terms)}}$$

**(d)** The Maclaurin series for $e^{-x}$ at $x = 0.3$:

$$e^{-0.3} = 1 - 0.3 + \frac{(0.3)^2}{2!} - \frac{(0.3)^3}{3!} + \frac{(0.3)^4}{4!} - \cdots$$

This IS an alternating series (for $x = 0.3 > 0$). The 4th-degree polynomial for $e^{-x}$ is:

$$P_4(-x \text{ series}) = 1 - 0.3 + 0.045 - 0.0045 + 0.0003375$$

By the Alternating Series Error Bound, the error is at most the first omitted term:

$$\left|\frac{(0.3)^5}{5!}\right| = \frac{0.00243}{120} = 0.00002025$$

Wait -- this gives the same value as the Lagrange bound! That's because for $e^{-x}$ (an alternating series), the first omitted term is $\frac{(0.3)^5}{5!}$, while the Lagrange bound for $e^x$ at $x = -0.3$ with $M = 1$ is also $\frac{(0.3)^5}{5!}$.

However, we can do better with the Alternating Series bound. The first omitted term of the $e^{-0.3}$ alternating series is:

$$\frac{-(0.3)^5}{5!} = -0.00002025$$

Its absolute value is $0.00002025$.

$$\boxed{\text{Both bounds give } 2.025 \times 10^{-5}; \text{ they are equal in this case.}}$$

In general, for the alternating series $e^{-x}$, the Alternating Series Error Bound is often comparable to the Lagrange bound because $M = e^0 = 1$ on $[-0.3, 0]$, making the Lagrange formula $\frac{(0.3)^5}{5!}$ match the alternating bound exactly.

</details>

---

## What's Next

You did it.

This is the **final article** in the entire AP Calculus BC curriculum. Every topic -- from the very first limits article back in Unit 1, through derivatives, integrals, differential equations, advanced integration, parametric and polar curves, sequences, series, and now Taylor series with error bounds -- you've covered it all. The Lagrange Error Bound is a fitting finale because it brings together so many ideas: derivatives, factorials, convergence, and the fundamental question of how well a polynomial can approximate any function.

Think about where you started. You were learning what a limit was, trying to figure out why $\frac{0}{0}$ doesn't always mean "undefined." Now you can take any smooth function, build a polynomial that mimics it to arbitrary precision, and *prove* exactly how good that approximation is. You can compute $e$, $\sin(17\degree)$, or $\ln(1.5)$ by hand, to as many decimal places as you want, and provide a mathematical guarantee on your accuracy. That's an incredible amount of power.

From Rancho Bernardo to Balboa Park, from Panda Express orange chicken to Ding Tea boba, from Mock Trial arguments to Robotics builds, from Science Olympiad tests to learning to drive with Dad on the San Diego freeways -- this journey through calculus has been about more than just math. It's been about building the confidence to take on hard problems, break them into pieces, and solve them one step at a time. The same skills that got you through $\epsilon$-$\delta$ proofs and integration by parts will carry you through college applications, AP exams, and whatever comes next.

You're ready for the AP exam. Go crush it.

---

<div align="center">

[← Taylor Series](/calculus/taylor-series)

</div>