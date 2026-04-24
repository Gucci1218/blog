# Series
<p class="article-date">April 23, 2026</p>

*You're at Panda Express, loading up a plate. First scoop: orange chicken. Second scoop: Beijing beef. Third: fried rice. Each scoop adds to the total weight on the plate. Now imagine a plate that never ends -- scoop after scoop after scoop, forever. Does the plate eventually weigh a million pounds? Or does it somehow settle at a finite weight because each scoop is lighter than the last? That question -- "what happens when you add infinitely many things together?" -- is the heart of infinite series. It's one of the most powerful ideas in all of mathematics, and it's the gateway to Taylor series, power series, and everything that makes BC Calculus special. Some infinite sums explode to infinity. Others converge to a beautiful, exact number. Learning to tell which is which? That's what this article is all about.*

---

## What You'll Learn
- Understand the definition of an infinite series as the sum of a sequence's terms
- Compute partial sums and connect them to convergence
- Identify and evaluate geometric series using the formula $S = \frac{a}{1 - r}$
- Recognize when a geometric series converges ($|r| < 1$) and diverges ($|r| \geq 1$)
- Evaluate telescoping series by cancellation of partial sums
- Prove the harmonic series diverges despite its terms approaching zero
- Apply the nth Term Test for Divergence
- Work with p-series and know the convergence criterion $p > 1$
- Use properties of convergent series (scalar multiples, sums, differences)
- Convert repeating decimals to fractions using geometric series

---

## Prerequisites
- [Sequences](/calculus/sequences)
- [Limits at Infinity](/calculus/0207-limits-at-infinity)
- [Antiderivatives](/calculus/0601-antiderivatives)

---

## The Core Concept

### Intuition First

Think about your Starbucks Rewards stars. Suppose on your first visit you earn 100 stars. On your second visit, 50. Then 25, then 12.5, and so on -- each visit gives you exactly half of what the previous one did. You're earning stars *forever*, visit after visit, for all eternity.

Will your total balance hit a million stars? Ten thousand? Or does it actually cap out at some specific number?

Here's the surprise: your total approaches exactly **200 stars** and never goes higher. $100 + 50 + 25 + 12.5 + \cdots = 200$. Adding infinitely many positive numbers gave you a *finite* total. That's a **convergent series**.

Now imagine a different scenario. You're visiting Ding Tea, and on visit $n$ you earn $\frac{1}{n}$ loyalty points: 1 point, then $\frac{1}{2}$, then $\frac{1}{3}$, then $\frac{1}{4}$, and so on. Each amount is shrinking toward zero -- surely the total stays finite, right?

Wrong. That sum -- $1 + \frac{1}{2} + \frac{1}{3} + \frac{1}{4} + \cdots$ -- grows without bound. It's the **harmonic series**, and it **diverges**. The terms go to zero, but they don't shrink *fast enough* for the total to stay finite.

This is the central tension of series: *just because the terms shrink to zero doesn't mean the sum is finite*. The rate at which they shrink is everything.

### Formal Definitions

**Definition:** Given a sequence $\{a_n\}$, the **infinite series** $\displaystyle\sum_{n=1}^{\infty} a_n$ is the "sum"

$$a_1 + a_2 + a_3 + a_4 + \cdots$$

But what does it *mean* to add infinitely many numbers? We can't literally do it. Instead, we define the sum through **partial sums**.

**Definition:** The **$N$th partial sum** of the series is:

$$S_N = \sum_{n=1}^{N} a_n = a_1 + a_2 + a_3 + \cdots + a_N$$

This is a finite sum -- no infinity involved. We *can* compute $S_1, S_2, S_3, \ldots$ and get a *sequence* of partial sums $\{S_N\}$.

**Definition:** The series $\displaystyle\sum_{n=1}^{\infty} a_n$ **converges** if the sequence of partial sums $\{S_N\}$ has a finite limit:

$$\sum_{n=1}^{\infty} a_n = \lim_{N \to \infty} S_N = S$$

If the limit doesn't exist or is infinite, the series **diverges**.

Think of it like building a tower of Lego bricks in your Robotics lab. Each brick $a_n$ adds height to the tower. The partial sum $S_N$ is the total height after $N$ bricks. If the tower approaches a fixed height as you keep adding bricks (because each brick is thinner and thinner), the series converges. If the tower grows forever, it diverges.

---

## Geometric Series

The **geometric series** is the single most important series in all of calculus. You *must* know it cold.

### The Setup

A geometric series has the form:

$$\sum_{n=0}^{\infty} ar^n = a + ar + ar^2 + ar^3 + \cdots$$

where $a$ is the **first term** and $r$ is the **common ratio** (each term is $r$ times the previous one).

### The Partial Sum Formula

The $N$th partial sum of a geometric series is:

$$S_N = a + ar + ar^2 + \cdots + ar^{N-1} = a \cdot \frac{1 - r^N}{1 - r} \quad (r \neq 1)$$

**Derivation** (this is clever -- watch closely):

$$S_N = a + ar + ar^2 + \cdots + ar^{N-1}$$

Multiply both sides by $r$:

$$rS_N = ar + ar^2 + ar^3 + \cdots + ar^{N}$$

Subtract the second equation from the first -- almost everything cancels:

$$S_N - rS_N = a - ar^N$$

$$S_N(1 - r) = a(1 - r^N)$$

$$\boxed{S_N = a \cdot \frac{1 - r^N}{1 - r}} \quad (r \neq 1)$$

### Convergence: The $|r| < 1$ Rule

Now take $N \to \infty$:

- If $|r| < 1$: then $r^N \to 0$, so $S_N \to \frac{a(1 - 0)}{1 - r} = \frac{a}{1 - r}$
- If $|r| \geq 1$: then $r^N$ doesn't approach $0$ (it either grows, oscillates, or stays at 1), so $S_N$ diverges

$$\boxed{\sum_{n=0}^{\infty} ar^n = \frac{a}{1 - r} \quad \text{if } |r| < 1}$$

$$\text{The series diverges if } |r| \geq 1$$

Your Starbucks example: $100 + 50 + 25 + 12.5 + \cdots = \sum_{n=0}^{\infty} 100\left(\frac{1}{2}\right)^n = \frac{100}{1 - \frac{1}{2}} = \frac{100}{\frac{1}{2}} = 200$ stars. Exactly as promised.

> **Be careful with the starting index.** The formula $\frac{a}{1-r}$ gives the sum starting from $n = 0$ with first term $a$. If a series starts at $n = 1$ (like $\sum_{n=1}^{\infty} ar^n = ar + ar^2 + \cdots$), the first term is $ar$ and the sum is $\frac{ar}{1-r}$. Always identify the **actual first term** of the series.

---

## Telescoping Series

A **telescoping series** is one where most terms in the partial sum cancel, leaving only a few surviving terms at the beginning and end -- like a collapsing telescope.

### How They Work

Consider $\displaystyle\sum_{n=1}^{\infty}\left(\frac{1}{n} - \frac{1}{n+1}\right)$.

Write out the partial sum:

$$S_N = \left(\frac{1}{1} - \frac{1}{2}\right) + \left(\frac{1}{2} - \frac{1}{3}\right) + \left(\frac{1}{3} - \frac{1}{4}\right) + \cdots + \left(\frac{1}{N} - \frac{1}{N+1}\right)$$

Look at the cancellation: $-\frac{1}{2}$ cancels with $+\frac{1}{2}$, $-\frac{1}{3}$ cancels with $+\frac{1}{3}$, and so on. Everything in the middle vanishes, leaving:

$$S_N = 1 - \frac{1}{N+1}$$

Take the limit:

$$\sum_{n=1}^{\infty}\left(\frac{1}{n} - \frac{1}{n+1}\right) = \lim_{N \to \infty}\left(1 - \frac{1}{N+1}\right) = 1$$

The key to telescoping series is **partial fractions**. When you see a term like $\frac{1}{n(n+1)}$, decompose it:

$$\frac{1}{n(n+1)} = \frac{1}{n} - \frac{1}{n+1}$$

Now you can telescope.

---

## The Harmonic Series: A Famous Divergence

The **harmonic series** is:

$$\sum_{n=1}^{\infty} \frac{1}{n} = 1 + \frac{1}{2} + \frac{1}{3} + \frac{1}{4} + \frac{1}{5} + \cdots$$

This series **diverges**, even though the terms $\frac{1}{n} \to 0$.

### Why It Diverges (Grouping Argument)

Group the terms cleverly:

$$1 + \frac{1}{2} + \underbrace{\frac{1}{3} + \frac{1}{4}}_{\geq \frac{1}{4} + \frac{1}{4} = \frac{1}{2}} + \underbrace{\frac{1}{5} + \frac{1}{6} + \frac{1}{7} + \frac{1}{8}}_{\geq 4 \cdot \frac{1}{8} = \frac{1}{2}} + \underbrace{\frac{1}{9} + \cdots + \frac{1}{16}}_{\geq 8 \cdot \frac{1}{16} = \frac{1}{2}} + \cdots$$

Each group sums to at least $\frac{1}{2}$. There are infinitely many groups, so:

$$S = 1 + \frac{1}{2} + \frac{1}{2} + \frac{1}{2} + \frac{1}{2} + \cdots = \infty$$

This is one of the most important results in all of series -- **terms going to zero is necessary but NOT sufficient for convergence.** It's like studying for Mock Trial: reviewing your case binder every day is *necessary* to be prepared, but it's not *sufficient* -- you also need to practice your opening statement, work on objections, and rehearse direct examinations.

---

## The nth Term Test for Divergence

This is the simplest and often the first test you should apply.

**Theorem (nth Term Test / Divergence Test):**

$$\text{If } \lim_{n \to \infty} a_n \neq 0, \text{ then } \sum_{n=1}^{\infty} a_n \text{ diverges.}$$

**Contrapositive (the useful direction):** If the series converges, then $\lim_{n \to \infty} a_n = 0$.

**The critical warning:** The converse is FALSE. If $\lim_{n \to \infty} a_n = 0$, the series *might* converge or *might* diverge. The harmonic series is the classic counterexample: $\lim_{n \to \infty}\frac{1}{n} = 0$, but $\sum \frac{1}{n}$ diverges.

Think of it as a bouncer at a concert venue. The nth Term Test can only **kick you out** (diverges). It can never **let you in** (prove convergence). If the terms don't go to zero, you're definitely out. But even if the terms do go to zero, you might still be denied entry.

**Example:** Does $\displaystyle\sum_{n=1}^{\infty} \frac{n}{2n + 3}$ converge or diverge?

$$\lim_{n \to \infty} \frac{n}{2n+3} = \lim_{n \to \infty} \frac{1}{2 + \frac{3}{n}} = \frac{1}{2} \neq 0$$

By the nth Term Test, the series **diverges**.

---

## p-Series

A **p-series** has the form:

$$\sum_{n=1}^{\infty} \frac{1}{n^p}$$

**Convergence rule:**

$$\boxed{\sum_{n=1}^{\infty} \frac{1}{n^p} \text{ converges if and only if } p > 1}$$

This mirrors the p-integral result you learned in [Improper Integrals](/calculus/improper-integrals): $\int_1^\infty \frac{1}{x^p}\,dx$ converges iff $p > 1$. That connection is no coincidence -- the **Integral Test** (coming in the next article) makes it rigorous.

**Key examples:**

| Series | p-value | Converges? |
|--------|---------|------------|
| $\sum \frac{1}{n^3}$ | $p = 3$ | Yes |
| $\sum \frac{1}{n^2}$ | $p = 2$ | Yes (equals $\frac{\pi^2}{6}$, amazingly) |
| $\sum \frac{1}{n}$ | $p = 1$ | No (harmonic series) |
| $\sum \frac{1}{\sqrt{n}}$ | $p = \frac{1}{2}$ | No |
| $\sum \frac{1}{n^{1.001}}$ | $p = 1.001$ | Yes (barely!) |

The boundary at $p = 1$ is razor-thin. Just like driving on the I-15 -- one lane to the left takes you north to Temecula, one lane to the right takes you south to Miramar. The harmonic series sits right on the dividing line, and it falls on the divergence side.

---

## Properties of Convergent Series

If $\sum a_n = A$ and $\sum b_n = B$ (both convergent), then:

| Property | Formula |
|----------|---------|
| Scalar multiple | $\displaystyle\sum_{n=1}^{\infty} ca_n = c \cdot A$ |
| Sum | $\displaystyle\sum_{n=1}^{\infty} (a_n + b_n) = A + B$ |
| Difference | $\displaystyle\sum_{n=1}^{\infty} (a_n - b_n) = A - B$ |

These work exactly like limit laws -- because the series sum *is* a limit (of partial sums).

**Important caveat:** You CANNOT combine a convergent and a divergent series and hope for convergence. If $\sum a_n$ converges and $\sum b_n$ diverges, then $\sum (a_n + b_n)$ **diverges**. (If it converged, then $\sum b_n = \sum (a_n + b_n) - \sum a_n$ would converge -- contradiction.)

Also, these properties say nothing about *products* of series. $\sum a_n b_n$ is NOT generally equal to $(\sum a_n)(\sum b_n)$.

---

## Repeating Decimals as Geometric Series

One of the coolest applications of geometric series: converting repeating decimals to fractions.

**Example:** What fraction equals $0.333\ldots$?

$$0.333\ldots = \frac{3}{10} + \frac{3}{100} + \frac{3}{1000} + \cdots = \sum_{n=1}^{\infty} \frac{3}{10^n} = \sum_{n=1}^{\infty} 3\left(\frac{1}{10}\right)^n$$

This is a geometric series with first term $a_1 = \frac{3}{10}$ and ratio $r = \frac{1}{10}$:

$$= \frac{\frac{3}{10}}{1 - \frac{1}{10}} = \frac{\frac{3}{10}}{\frac{9}{10}} = \frac{3}{9} = \frac{1}{3}$$

No surprise -- $0.333\ldots = \frac{1}{3}$ -- but now you can prove it with series!

---

## Worked Examples

### Example 1: Evaluating a Geometric Series

**Find the sum: $\displaystyle\sum_{n=0}^{\infty} \frac{3}{5^n}$**

Identify: $a = 3$, $r = \frac{1}{5}$. Since $|r| = \frac{1}{5} < 1$, the series converges.

$$\sum_{n=0}^{\infty} \frac{3}{5^n} = \sum_{n=0}^{\infty} 3\left(\frac{1}{5}\right)^n = \frac{3}{1 - \frac{1}{5}} = \frac{3}{\frac{4}{5}} = \boxed{\frac{15}{4}}$$

---

### Example 2: Geometric Series Starting at $n = 1$

**Find the sum: $\displaystyle\sum_{n=1}^{\infty} \left(\frac{2}{3}\right)^n$**

The first term (when $n = 1$) is $a_1 = \frac{2}{3}$. The ratio is $r = \frac{2}{3}$. Since $|r| < 1$:

$$\sum_{n=1}^{\infty}\left(\frac{2}{3}\right)^n = \frac{\frac{2}{3}}{1 - \frac{2}{3}} = \frac{\frac{2}{3}}{\frac{1}{3}} = \boxed{2}$$

Alternatively: $\sum_{n=1}^{\infty}\left(\frac{2}{3}\right)^n = \sum_{n=0}^{\infty}\left(\frac{2}{3}\right)^n - 1 = \frac{1}{1 - \frac{2}{3}} - 1 = 3 - 1 = 2$.

---

### Example 3: Geometric Series -- Divergence

**Does $\displaystyle\sum_{n=0}^{\infty} \frac{5^n}{4^n}$ converge or diverge?**

Rewrite: $\sum_{n=0}^{\infty}\left(\frac{5}{4}\right)^n$. Here $r = \frac{5}{4}$ and $|r| = \frac{5}{4} > 1$.

The series **diverges**. Each term is *larger* than the previous one -- the partial sums grow without bound.

---

### Example 4: Telescoping Series

**Evaluate: $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n(n+1)}$**

**Step 1 -- Partial fractions:**

$$\frac{1}{n(n+1)} = \frac{1}{n} - \frac{1}{n+1}$$

**Step 2 -- Write out the partial sum:**

$$S_N = \sum_{n=1}^{N}\left(\frac{1}{n} - \frac{1}{n+1}\right) = \left(1 - \frac{1}{2}\right) + \left(\frac{1}{2} - \frac{1}{3}\right) + \left(\frac{1}{3} - \frac{1}{4}\right) + \cdots + \left(\frac{1}{N} - \frac{1}{N+1}\right)$$

**Step 3 -- Cancel (telescope):**

$$S_N = 1 - \frac{1}{N+1}$$

**Step 4 -- Take the limit:**

$$\sum_{n=1}^{\infty} \frac{1}{n(n+1)} = \lim_{N \to \infty}\left(1 - \frac{1}{N+1}\right) = \boxed{1}$$

---

### Example 5: nth Term Test

**Does $\displaystyle\sum_{n=1}^{\infty} \frac{n^2}{3n^2 + 1}$ converge or diverge?**

Compute the limit of the terms:

$$\lim_{n \to \infty} \frac{n^2}{3n^2 + 1} = \lim_{n \to \infty} \frac{1}{3 + \frac{1}{n^2}} = \frac{1}{3} \neq 0$$

By the nth Term Test, the series **diverges**.

You don't need any other test. If the terms don't go to zero, it's over -- like forgetting your lines in Mock Trial opening statements. No matter how good the rest of your case is, you've already lost.

---

### Example 6: p-Series Identification

**Determine convergence or divergence:**

**(a)** $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n^4}$

This is a p-series with $p = 4 > 1$. It **converges**.

**(b)** $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n^{2/3}}$

This is a p-series with $p = \frac{2}{3} < 1$. It **diverges**.

**(c)** $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n\sqrt{n}}$

Rewrite: $\frac{1}{n\sqrt{n}} = \frac{1}{n^{3/2}}$. This is a p-series with $p = \frac{3}{2} > 1$. It **converges**.

---

### Example 7: Repeating Decimal to Fraction

**Express $0.2\overline{45} = 0.24545\ldots$ as a fraction.**

Separate the non-repeating and repeating parts:

$$0.2\overline{45} = 0.2 + 0.045 + 0.00045 + 0.0000045 + \cdots$$

$$= \frac{2}{10} + \frac{45}{1000} + \frac{45}{100{,}000} + \frac{45}{10{,}000{,}000} + \cdots$$

$$= \frac{1}{5} + \sum_{n=0}^{\infty} \frac{45}{1000}\left(\frac{1}{100}\right)^n$$

The geometric part has $a = \frac{45}{1000} = \frac{9}{200}$ and $r = \frac{1}{100}$:

$$= \frac{1}{5} + \frac{\frac{9}{200}}{1 - \frac{1}{100}} = \frac{1}{5} + \frac{\frac{9}{200}}{\frac{99}{100}} = \frac{1}{5} + \frac{9}{200} \cdot \frac{100}{99} = \frac{1}{5} + \frac{9}{198}$$

$$= \frac{1}{5} + \frac{1}{22} = \frac{22}{110} + \frac{5}{110} = \boxed{\frac{27}{110}}$$

---

### Example 8: Combining Series Properties

**Given $\displaystyle\sum_{n=1}^{\infty} a_n = 7$ and $\displaystyle\sum_{n=1}^{\infty} b_n = 3$, find $\displaystyle\sum_{n=1}^{\infty}(4a_n - 2b_n)$.**

By the properties of convergent series:

$$\sum_{n=1}^{\infty}(4a_n - 2b_n) = 4\sum_{n=1}^{\infty} a_n - 2\sum_{n=1}^{\infty} b_n = 4(7) - 2(3) = 28 - 6 = \boxed{22}$$

---

## Key Formulas & Rules

| Concept | Formula / Rule |
|---------|---------------|
| Series definition | $\displaystyle\sum_{n=1}^{\infty} a_n = \lim_{N \to \infty} S_N$ where $S_N = a_1 + a_2 + \cdots + a_N$ |
| Geometric series ($\|r\| < 1$) | $\displaystyle\sum_{n=0}^{\infty} ar^n = \frac{a}{1 - r}$ |
| Geometric series divergence | Diverges if $\|r\| \geq 1$ |
| Geometric partial sum | $S_N = a \cdot \frac{1 - r^N}{1 - r}$ |
| Telescoping series | Write partial sums, cancel interior terms, take the limit |
| Harmonic series | $\displaystyle\sum_{n=1}^{\infty}\frac{1}{n}$ diverges |
| p-series | $\displaystyle\sum_{n=1}^{\infty}\frac{1}{n^p}$ converges iff $p > 1$ |
| nth Term Test | If $\lim_{n\to\infty} a_n \neq 0$, then $\sum a_n$ diverges |
| nth Term Test (warning) | If $\lim_{n\to\infty} a_n = 0$, the test is **inconclusive** |
| Scalar multiple | $\sum ca_n = c\sum a_n$ |
| Sum/Difference | $\sum (a_n \pm b_n) = \sum a_n \pm \sum b_n$ (both must converge) |

---

## Common Mistakes to Avoid

**1. Thinking $\lim a_n = 0$ means the series converges.**

- **Wrong:** "$\lim_{n \to \infty}\frac{1}{n} = 0$, so $\sum \frac{1}{n}$ converges."
- **Right:** The harmonic series diverges despite $\frac{1}{n} \to 0$. The nth Term Test can only prove *divergence* (when the limit isn't zero), never convergence. It's a one-way door.

**2. Using the geometric series formula when $|r| \geq 1$.**

- **Wrong:** $\sum_{n=0}^{\infty} 2^n = \frac{1}{1 - 2} = -1$.
- **Right:** $|r| = 2 \geq 1$, so the series diverges. The formula $\frac{a}{1-r}$ does NOT apply. Getting a negative answer for a sum of positive terms is a dead giveaway that something went wrong.

**3. Misidentifying $a$ and $r$ in a geometric series.**

- **Wrong:** For $\sum_{n=1}^{\infty}\frac{3}{4^n}$, using $a = 3$ and $r = \frac{1}{4}$ in the formula $\frac{a}{1-r}$ to get $\frac{3}{3/4} = 4$.
- **Right:** The first term is $a_1 = \frac{3}{4}$ (plug in $n = 1$), not $3$. The sum is $\frac{3/4}{1 - 1/4} = \frac{3/4}{3/4} = 1$. Always identify the **actual first term** by plugging in the starting index.

**4. Forgetting to check both pieces of a telescoping series.**

- **Wrong:** Assuming all telescoping series converge.
- **Right:** After the cancellation, you're left with a limit. If that limit is infinite, the series diverges. Always take the limit of $S_N$ to check.

**5. Confusing series with sequences.**

- **Wrong:** "The sequence $\frac{1}{n}$ diverges."
- **Right:** The *sequence* $\left\{\frac{1}{n}\right\}$ converges to $0$. The *series* $\sum \frac{1}{n}$ diverges. A sequence is a list; a series is a sum. Completely different questions.

**6. Applying p-series results to non-p-series.**

- **Wrong:** "$\sum \frac{1}{n^2 + 1}$ is a p-series with $p = 2$, so it converges."
- **Right:** $\frac{1}{n^2 + 1}$ is NOT $\frac{1}{n^p}$. It *behaves like* a p-series with $p = 2$ (and it does converge), but you need a comparison test to prove it -- not the p-series rule directly. The p-series rule only applies to $\sum \frac{1}{n^p}$ exactly.

**7. Adding/subtracting convergent and divergent series.**

- **Wrong:** "$\sum a_n$ converges and $\sum b_n$ diverges, so $\sum (a_n + b_n)$ might converge."
- **Right:** The sum of a convergent and divergent series ALWAYS diverges. No exceptions.

---

## AP Exam Tips

1. **The nth Term Test is your first move.** On any convergence/divergence question, always check: does $\lim_{n\to\infty} a_n = 0$? If not, write "diverges by the nth Term Test" and move on. This takes 10 seconds and earns full credit.

2. **Geometric series are free points.** If you can write a series in the form $\sum ar^n$, you immediately know whether it converges (check $|r|$) and what it converges to ($\frac{a}{1-r}$). Graders love seeing clean identification of $a$ and $r$.

3. **Memorize the harmonic series result.** "The harmonic series $\sum \frac{1}{n}$ diverges" appears as a comparison benchmark in nearly every convergence problem. Know it instantly.

4. **Partial fractions unlock telescoping.** When you see $\frac{1}{n(n+1)}$ or $\frac{1}{(2n-1)(2n+1)}$ or similar products in the denominator, decompose with partial fractions and telescope.

5. **p-series is your second benchmark.** After the harmonic series, the p-series family is the most common comparison target. Know the rule: $p > 1$ converges, $p \leq 1$ diverges.

6. **Watch the starting index on MC.** A series starting at $n = 0$ versus $n = 1$ versus $n = 3$ changes the first term. The formula $\frac{a}{1-r}$ uses $a$ = first term, not $a$ = some coefficient. Plug in the starting index to find the actual first term.

7. **Show the limit notation for partial sums.** On free-response, when evaluating a telescoping series, write $S_N = \ldots$, show the cancellation, then write $\lim_{N \to \infty} S_N = \ldots$. Graders award points for this structure.

8. **Repeating decimal problems are geometric.** If asked to express $0.\overline{36}$ as a fraction, recognize it as $\sum_{n=1}^{\infty}\frac{36}{100^n}$ with $r = \frac{1}{100}$. Quick and clean.

9. **Don't mix up "the sequence converges" and "the series converges."** The AP sometimes asks about the sequence $\{a_n\}$ separately from the series $\sum a_n$. Read carefully. For the series to converge, we need the *partial sums* to have a finite limit, not just the terms.

10. **The nth Term Test gives divergence only.** If you write "the series converges by the nth Term Test because $a_n \to 0$," you will lose points. This is the single most common incorrect justification on the AP exam.

---

## Practice Problems

### Basic (1--5)

**Problem 1.** Determine whether the geometric series $\displaystyle\sum_{n=0}^{\infty}\left(\frac{3}{7}\right)^n$ converges or diverges. If it converges, find the sum.

**Problem 2.** Evaluate $\displaystyle\sum_{n=1}^{\infty}\frac{4}{3^n}$.

**Problem 3.** Use the nth Term Test to determine whether $\displaystyle\sum_{n=1}^{\infty}\frac{3n + 1}{n + 2}$ converges or diverges.

**Problem 4.** Classify each as convergent or divergent:
- (a) $\displaystyle\sum_{n=1}^{\infty}\frac{1}{n^5}$
- (b) $\displaystyle\sum_{n=1}^{\infty}\frac{1}{n^{0.8}}$
- (c) $\displaystyle\sum_{n=1}^{\infty}\frac{1}{\sqrt[3]{n}}$

**Problem 5.** Express the repeating decimal $0.\overline{7} = 0.777\ldots$ as a fraction using a geometric series.

### Intermediate (6--10)

**Problem 6.** Evaluate the telescoping series $\displaystyle\sum_{n=1}^{\infty}\frac{1}{n(n+2)}$. *(Hint: partial fractions.)*

**Problem 7.** Find the sum: $\displaystyle\sum_{n=0}^{\infty}\frac{2^{n+1}}{5^n}$.

**Problem 8.** Given $\displaystyle\sum_{n=1}^{\infty} a_n = 10$ and $\displaystyle\sum_{n=1}^{\infty} b_n = 4$, find:
- (a) $\displaystyle\sum_{n=1}^{\infty}(3a_n + b_n)$
- (b) $\displaystyle\sum_{n=1}^{\infty}(a_n - 5b_n)$

**Problem 9.** Express $0.\overline{36} = 0.363636\ldots$ as a fraction using a geometric series.

**Problem 10.** Determine convergence or divergence: $\displaystyle\sum_{n=1}^{\infty}\frac{(-1)^n \cdot n}{n + 1}$. *(Careful -- which test should you try first?)*

### Advanced (11--15)

**Problem 11.** Evaluate: $\displaystyle\sum_{n=1}^{\infty}\frac{1}{(2n-1)(2n+1)}$. *(Hint: partial fractions and telescope.)*

**Problem 12.** Find the values of $x$ for which the geometric series $\displaystyle\sum_{n=0}^{\infty}(2x)^n$ converges, and express the sum as a function of $x$.

**Problem 13.** Evaluate: $\displaystyle\sum_{n=1}^{\infty}\left[\frac{3}{4^n} + \frac{2}{n(n+1)}\right]$.

**Problem 14.** A bouncing ball is dropped from a height of 10 meters. Each bounce reaches $\frac{3}{5}$ of the previous height. Find the total vertical distance traveled by the ball.

**Problem 15.** Evaluate: $\displaystyle\sum_{n=2}^{\infty}\frac{1}{n^2 - 1}$. *(Hint: factor the denominator, then use partial fractions.)*

### AP Exam Practice (16--20)

**Problem 16 (MC).** Which of the following series converges?

| Choice | Series |
|--------|--------|
| (A) | $\displaystyle\sum_{n=1}^{\infty}\frac{n}{n+1}$ |
| (B) | $\displaystyle\sum_{n=1}^{\infty}\frac{1}{\sqrt{n}}$ |
| (C) | $\displaystyle\sum_{n=1}^{\infty}\left(\frac{4}{5}\right)^n$ |
| (D) | $\displaystyle\sum_{n=1}^{\infty}\frac{1}{n}$ |

**Problem 17 (MC).** The sum of the series $\displaystyle\sum_{n=1}^{\infty}\frac{(-3)^{n-1}}{4^n}$ is:

| Choice | Answer |
|--------|--------|
| (A) | $\frac{1}{7}$ |
| (B) | $\frac{1}{4}$ |
| (C) | $\frac{3}{7}$ |
| (D) | $\frac{4}{7}$ |

**Problem 18 (MC).** If $\displaystyle\sum_{n=1}^{\infty} a_n$ diverges and $\displaystyle\sum_{n=1}^{\infty} b_n$ converges, which of the following must be true?

| Choice | Statement |
|--------|-----------|
| (A) | $\displaystyle\sum_{n=1}^{\infty}(a_n + b_n)$ converges |
| (B) | $\displaystyle\sum_{n=1}^{\infty}(a_n + b_n)$ diverges |
| (C) | $\displaystyle\sum_{n=1}^{\infty} a_n b_n$ diverges |
| (D) | $\lim_{n\to\infty} a_n \neq 0$ |

**Problem 19 (FR).** Consider the series $\displaystyle\sum_{n=1}^{\infty}\frac{3}{n(n+3)}$.

> (a) Use partial fractions to write $\frac{3}{n(n+3)}$ as a difference of two fractions.
>
> (b) Write out the first 8 terms of the partial sum $S_N$ and identify the terms that remain after cancellation.
>
> (c) Find an explicit formula for $S_N$ and evaluate $\displaystyle\sum_{n=1}^{\infty}\frac{3}{n(n+3)}$.

**Problem 20 (FR).** A local Sesame Donuts location runs a promotion. On day 1, they give away 120 donuts. Each subsequent day, they give away $\frac{2}{3}$ of the previous day's amount.

> (a) Write a series expression for the total number of donuts given away over all days.
>
> (b) Find the total number of donuts given away if the promotion runs forever.
>
> (c) After how many complete days will the shop have given away at least 350 donuts? (Use the partial sum formula.)
>
> (d) Suppose instead they give away $\frac{120}{n}$ donuts on day $n$. Does the total converge or diverge? Justify your answer.

---

## Answer Key

<details><summary><strong>Problem 1 Solution</strong></summary>

Determine whether $\displaystyle\sum_{n=0}^{\infty}\left(\frac{3}{7}\right)^n$ converges or diverges.

This is a geometric series with $a = 1$ (the first term when $n = 0$: $\left(\frac{3}{7}\right)^0 = 1$) and $r = \frac{3}{7}$.

Since $|r| = \frac{3}{7} < 1$, the series **converges**.

$$\sum_{n=0}^{\infty}\left(\frac{3}{7}\right)^n = \frac{1}{1 - \frac{3}{7}} = \frac{1}{\frac{4}{7}} = \boxed{\frac{7}{4}}$$

</details>

---

<details><summary><strong>Problem 2 Solution</strong></summary>

Evaluate $\displaystyle\sum_{n=1}^{\infty}\frac{4}{3^n}$.

Rewrite: $\sum_{n=1}^{\infty}4\left(\frac{1}{3}\right)^n$.

The first term (when $n = 1$) is $a_1 = 4 \cdot \frac{1}{3} = \frac{4}{3}$. The ratio is $r = \frac{1}{3}$. Since $|r| < 1$:

$$\sum_{n=1}^{\infty}\frac{4}{3^n} = \frac{\frac{4}{3}}{1 - \frac{1}{3}} = \frac{\frac{4}{3}}{\frac{2}{3}} = \boxed{2}$$

</details>

---

<details><summary><strong>Problem 3 Solution</strong></summary>

Use the nth Term Test on $\displaystyle\sum_{n=1}^{\infty}\frac{3n + 1}{n + 2}$.

$$\lim_{n \to \infty}\frac{3n + 1}{n + 2} = \lim_{n \to \infty}\frac{3 + \frac{1}{n}}{1 + \frac{2}{n}} = \frac{3}{1} = 3 \neq 0$$

Since $\lim_{n \to \infty} a_n = 3 \neq 0$, the series **diverges** by the nth Term Test.

$$\boxed{\text{Diverges}}$$

</details>

---

<details><summary><strong>Problem 4 Solution</strong></summary>

**(a)** $\displaystyle\sum_{n=1}^{\infty}\frac{1}{n^5}$: p-series with $p = 5 > 1$. **Converges.** $\checkmark$

**(b)** $\displaystyle\sum_{n=1}^{\infty}\frac{1}{n^{0.8}}$: p-series with $p = 0.8 < 1$. **Diverges.**

**(c)** $\displaystyle\sum_{n=1}^{\infty}\frac{1}{\sqrt[3]{n}} = \sum \frac{1}{n^{1/3}}$: p-series with $p = \frac{1}{3} < 1$. **Diverges.**

$$\boxed{\text{(a) Converges, (b) Diverges, (c) Diverges}}$$

</details>

---

<details><summary><strong>Problem 5 Solution</strong></summary>

Express $0.\overline{7} = 0.777\ldots$ as a fraction.

$$0.777\ldots = \frac{7}{10} + \frac{7}{100} + \frac{7}{1000} + \cdots = \sum_{n=1}^{\infty}\frac{7}{10^n} = \sum_{n=1}^{\infty}7\left(\frac{1}{10}\right)^n$$

This is a geometric series with first term $a_1 = \frac{7}{10}$ and $r = \frac{1}{10}$:

$$= \frac{\frac{7}{10}}{1 - \frac{1}{10}} = \frac{\frac{7}{10}}{\frac{9}{10}} = \boxed{\frac{7}{9}}$$

</details>

---

<details><summary><strong>Problem 6 Solution</strong></summary>

Evaluate $\displaystyle\sum_{n=1}^{\infty}\frac{1}{n(n+2)}$.

**Step 1 -- Partial fractions:**

$$\frac{1}{n(n+2)} = \frac{A}{n} + \frac{B}{n+2}$$

Multiply by $n(n+2)$: $1 = A(n+2) + Bn$.

Set $n = 0$: $1 = 2A \implies A = \frac{1}{2}$.

Set $n = -2$: $1 = -2B \implies B = -\frac{1}{2}$.

$$\frac{1}{n(n+2)} = \frac{1}{2}\left(\frac{1}{n} - \frac{1}{n+2}\right)$$

**Step 2 -- Write out the partial sum:**

$$S_N = \frac{1}{2}\sum_{n=1}^{N}\left(\frac{1}{n} - \frac{1}{n+2}\right)$$

$$= \frac{1}{2}\left[\left(1 - \frac{1}{3}\right) + \left(\frac{1}{2} - \frac{1}{4}\right) + \left(\frac{1}{3} - \frac{1}{5}\right) + \left(\frac{1}{4} - \frac{1}{6}\right) + \cdots + \left(\frac{1}{N} - \frac{1}{N+2}\right)\right]$$

This telescopes, but the "gap" is 2 (not 1), so the cancellation is slightly different. After cancellation, the surviving terms are from the beginning ($\frac{1}{1}$ and $\frac{1}{2}$) and the end ($-\frac{1}{N+1}$ and $-\frac{1}{N+2}$):

$$S_N = \frac{1}{2}\left(1 + \frac{1}{2} - \frac{1}{N+1} - \frac{1}{N+2}\right) = \frac{1}{2}\left(\frac{3}{2} - \frac{1}{N+1} - \frac{1}{N+2}\right)$$

**Step 3 -- Take the limit:**

$$\lim_{N \to \infty} S_N = \frac{1}{2}\left(\frac{3}{2} - 0 - 0\right) = \boxed{\frac{3}{4}}$$

</details>

---

<details><summary><strong>Problem 7 Solution</strong></summary>

Find the sum: $\displaystyle\sum_{n=0}^{\infty}\frac{2^{n+1}}{5^n}$.

Rewrite:

$$\sum_{n=0}^{\infty}\frac{2^{n+1}}{5^n} = \sum_{n=0}^{\infty}2 \cdot \frac{2^n}{5^n} = 2\sum_{n=0}^{\infty}\left(\frac{2}{5}\right)^n$$

This is a geometric series with $a = 2$ (first term when $n = 0$ is $\frac{2^1}{5^0} = 2$) and $r = \frac{2}{5}$. Since $|r| < 1$:

$$= 2 \cdot \frac{1}{1 - \frac{2}{5}} = 2 \cdot \frac{1}{\frac{3}{5}} = 2 \cdot \frac{5}{3} = \boxed{\frac{10}{3}}$$

</details>

---

<details><summary><strong>Problem 8 Solution</strong></summary>

Given $\sum a_n = 10$ and $\sum b_n = 4$:

**(a)** $\displaystyle\sum_{n=1}^{\infty}(3a_n + b_n) = 3\sum a_n + \sum b_n = 3(10) + 4 = \boxed{34}$

**(b)** $\displaystyle\sum_{n=1}^{\infty}(a_n - 5b_n) = \sum a_n - 5\sum b_n = 10 - 5(4) = 10 - 20 = \boxed{-10}$

</details>

---

<details><summary><strong>Problem 9 Solution</strong></summary>

Express $0.\overline{36} = 0.363636\ldots$ as a fraction.

$$0.\overline{36} = \frac{36}{100} + \frac{36}{10{,}000} + \frac{36}{1{,}000{,}000} + \cdots = \sum_{n=1}^{\infty}\frac{36}{100^n}$$

This is a geometric series with first term $a_1 = \frac{36}{100} = \frac{9}{25}$ and $r = \frac{1}{100}$:

$$= \frac{\frac{36}{100}}{1 - \frac{1}{100}} = \frac{\frac{36}{100}}{\frac{99}{100}} = \frac{36}{99} = \frac{4}{11}$$

$$\boxed{\frac{4}{11}}$$

</details>

---

<details><summary><strong>Problem 10 Solution</strong></summary>

Determine convergence or divergence: $\displaystyle\sum_{n=1}^{\infty}\frac{(-1)^n \cdot n}{n + 1}$.

**Try the nth Term Test first:**

$$\lim_{n \to \infty}\frac{(-1)^n \cdot n}{n + 1}$$

Compute the absolute value: $\left|\frac{(-1)^n \cdot n}{n+1}\right| = \frac{n}{n+1} \to 1$.

Since the terms alternate between values approaching $+1$ and $-1$, the limit $\lim_{n \to \infty} a_n$ does not exist (certainly $\neq 0$).

By the nth Term Test, the series **diverges**.

$$\boxed{\text{Diverges by the nth Term Test}}$$

</details>

---

<details><summary><strong>Problem 11 Solution</strong></summary>

Evaluate: $\displaystyle\sum_{n=1}^{\infty}\frac{1}{(2n-1)(2n+1)}$.

**Step 1 -- Partial fractions:**

$$\frac{1}{(2n-1)(2n+1)} = \frac{A}{2n-1} + \frac{B}{2n+1}$$

Multiply by $(2n-1)(2n+1)$: $1 = A(2n+1) + B(2n-1)$.

Set $n = \frac{1}{2}$: $1 = A(2) \implies A = \frac{1}{2}$.

Set $n = -\frac{1}{2}$: $1 = B(-2) \implies B = -\frac{1}{2}$.

$$\frac{1}{(2n-1)(2n+1)} = \frac{1}{2}\left(\frac{1}{2n-1} - \frac{1}{2n+1}\right)$$

**Step 2 -- Write the partial sum:**

$$S_N = \frac{1}{2}\sum_{n=1}^{N}\left(\frac{1}{2n-1} - \frac{1}{2n+1}\right)$$

$$= \frac{1}{2}\left[\left(\frac{1}{1} - \frac{1}{3}\right) + \left(\frac{1}{3} - \frac{1}{5}\right) + \left(\frac{1}{5} - \frac{1}{7}\right) + \cdots + \left(\frac{1}{2N-1} - \frac{1}{2N+1}\right)\right]$$

This telescopes cleanly (gap of 1 in the sequence of odd reciprocals):

$$S_N = \frac{1}{2}\left(1 - \frac{1}{2N+1}\right)$$

**Step 3 -- Take the limit:**

$$\sum_{n=1}^{\infty}\frac{1}{(2n-1)(2n+1)} = \lim_{N \to \infty}\frac{1}{2}\left(1 - \frac{1}{2N+1}\right) = \frac{1}{2}(1 - 0) = \boxed{\frac{1}{2}}$$

</details>

---

<details><summary><strong>Problem 12 Solution</strong></summary>

Find the values of $x$ for which $\displaystyle\sum_{n=0}^{\infty}(2x)^n$ converges, and express the sum.

This is a geometric series with $r = 2x$. It converges when $|r| < 1$:

$$|2x| < 1 \implies |x| < \frac{1}{2} \implies -\frac{1}{2} < x < \frac{1}{2}$$

When it converges, the sum is:

$$\sum_{n=0}^{\infty}(2x)^n = \frac{1}{1 - 2x}$$

$$\boxed{\text{Converges for } -\frac{1}{2} < x < \frac{1}{2}, \quad S = \frac{1}{1 - 2x}}$$

</details>

---

<details><summary><strong>Problem 13 Solution</strong></summary>

Evaluate: $\displaystyle\sum_{n=1}^{\infty}\left[\frac{3}{4^n} + \frac{2}{n(n+1)}\right]$.

By the sum property:

$$\sum_{n=1}^{\infty}\left[\frac{3}{4^n} + \frac{2}{n(n+1)}\right] = \sum_{n=1}^{\infty}\frac{3}{4^n} + 2\sum_{n=1}^{\infty}\frac{1}{n(n+1)}$$

**First series:** Geometric with $a_1 = \frac{3}{4}$ and $r = \frac{1}{4}$:

$$\sum_{n=1}^{\infty}\frac{3}{4^n} = \frac{3/4}{1 - 1/4} = \frac{3/4}{3/4} = 1$$

**Second series:** Telescoping (from Example 4):

$$\sum_{n=1}^{\infty}\frac{1}{n(n+1)} = 1$$

**Combined:**

$$1 + 2(1) = \boxed{3}$$

</details>

---

<details><summary><strong>Problem 14 Solution</strong></summary>

A ball is dropped from 10 meters and each bounce reaches $\frac{3}{5}$ of the previous height.

The ball falls 10 m down, then bounces up $10 \cdot \frac{3}{5} = 6$ m and falls 6 m, then bounces up $6 \cdot \frac{3}{5} = \frac{18}{5}$ m and falls $\frac{18}{5}$ m, and so on.

**Total distance** = initial drop + 2 $\times$ (all bounce heights):

$$D = 10 + 2\sum_{n=1}^{\infty}10\left(\frac{3}{5}\right)^n$$

The geometric series: first term $a_1 = 10 \cdot \frac{3}{5} = 6$, ratio $r = \frac{3}{5}$:

$$\sum_{n=1}^{\infty}10\left(\frac{3}{5}\right)^n = \frac{6}{1 - \frac{3}{5}} = \frac{6}{\frac{2}{5}} = 15$$

**Total distance:**

$$D = 10 + 2(15) = 10 + 30 = \boxed{40 \text{ meters}}$$

</details>

---

<details><summary><strong>Problem 15 Solution</strong></summary>

Evaluate: $\displaystyle\sum_{n=2}^{\infty}\frac{1}{n^2 - 1}$.

**Step 1 -- Factor and decompose:**

$$\frac{1}{n^2 - 1} = \frac{1}{(n-1)(n+1)} = \frac{1}{2}\left(\frac{1}{n-1} - \frac{1}{n+1}\right)$$

(Partial fractions: $\frac{1}{(n-1)(n+1)} = \frac{A}{n-1} + \frac{B}{n+1}$. Setting $n = 1$: $1 = 2A$, so $A = \frac{1}{2}$. Setting $n = -1$: $1 = -2B$, so $B = -\frac{1}{2}$.)

**Step 2 -- Partial sum:**

$$S_N = \frac{1}{2}\sum_{n=2}^{N}\left(\frac{1}{n-1} - \frac{1}{n+1}\right)$$

$$= \frac{1}{2}\left[\left(\frac{1}{1} - \frac{1}{3}\right) + \left(\frac{1}{2} - \frac{1}{4}\right) + \left(\frac{1}{3} - \frac{1}{5}\right) + \left(\frac{1}{4} - \frac{1}{6}\right) + \cdots + \left(\frac{1}{N-1} - \frac{1}{N+1}\right)\right]$$

The gap is 2, so the surviving terms are from the first two pairs ($\frac{1}{1}$ and $\frac{1}{2}$) and the last two negative terms ($-\frac{1}{N}$ and $-\frac{1}{N+1}$):

$$S_N = \frac{1}{2}\left(1 + \frac{1}{2} - \frac{1}{N} - \frac{1}{N+1}\right)$$

**Step 3 -- Take the limit:**

$$\lim_{N \to \infty} S_N = \frac{1}{2}\left(\frac{3}{2} - 0 - 0\right) = \boxed{\frac{3}{4}}$$

</details>

---

<details><summary><strong>Problem 16 Solution</strong></summary>

Which series converges?

**(A)** $\displaystyle\sum_{n=1}^{\infty}\frac{n}{n+1}$: $\lim_{n\to\infty}\frac{n}{n+1} = 1 \neq 0$. **Diverges** by the nth Term Test.

**(B)** $\displaystyle\sum_{n=1}^{\infty}\frac{1}{\sqrt{n}} = \sum \frac{1}{n^{1/2}}$: p-series with $p = \frac{1}{2} < 1$. **Diverges.**

**(C)** $\displaystyle\sum_{n=1}^{\infty}\left(\frac{4}{5}\right)^n$: geometric with $r = \frac{4}{5}$ and $|r| < 1$. **Converges.**

**(D)** $\displaystyle\sum_{n=1}^{\infty}\frac{1}{n}$: harmonic series. **Diverges.**

$$\boxed{\textbf{(C)}}$$

</details>

---

<details><summary><strong>Problem 17 Solution</strong></summary>

Find the sum of $\displaystyle\sum_{n=1}^{\infty}\frac{(-3)^{n-1}}{4^n}$.

Rewrite:

$$\sum_{n=1}^{\infty}\frac{(-3)^{n-1}}{4^n} = \sum_{n=1}^{\infty}\frac{1}{(-3)}\cdot\frac{(-3)^n}{4^n} \cdot \frac{1}{1}$$

Actually, let's be more careful. When $n = 1$: $\frac{(-3)^0}{4^1} = \frac{1}{4}$. When $n = 2$: $\frac{(-3)^1}{4^2} = \frac{-3}{16}$. The ratio between consecutive terms is:

$$r = \frac{-3/16}{1/4} = \frac{-3}{16} \cdot \frac{4}{1} = \frac{-3}{4}$$

So this is a geometric series with first term $a_1 = \frac{1}{4}$ and $r = -\frac{3}{4}$. Since $|r| = \frac{3}{4} < 1$:

$$\sum_{n=1}^{\infty}\frac{(-3)^{n-1}}{4^n} = \frac{\frac{1}{4}}{1 - \left(-\frac{3}{4}\right)} = \frac{\frac{1}{4}}{1 + \frac{3}{4}} = \frac{\frac{1}{4}}{\frac{7}{4}} = \frac{1}{7}$$

$$\boxed{\textbf{(A)}\ \frac{1}{7}}$$

</details>

---

<details><summary><strong>Problem 18 Solution</strong></summary>

If $\sum a_n$ diverges and $\sum b_n$ converges, which must be true?

**(A)** $\sum(a_n + b_n)$ converges -- **NO.** If this converged, then $\sum a_n = \sum(a_n + b_n) - \sum b_n$ would be the difference of two convergent series, hence convergent. But $\sum a_n$ diverges -- contradiction.

**(B)** $\sum(a_n + b_n)$ diverges -- **YES.** By the argument above, if $\sum(a_n + b_n)$ converged, we'd get a contradiction. So it must diverge.

**(C)** $\sum a_n b_n$ diverges -- **Not necessarily.** Consider $a_n = 1$ (diverges) and $b_n = \frac{1}{n^2}$ (converges). Then $a_n b_n = \frac{1}{n^2}$, which converges. So (C) can be false.

**(D)** $\lim a_n \neq 0$ -- **Not necessarily.** The harmonic series $\sum \frac{1}{n}$ diverges but $\lim \frac{1}{n} = 0$.

$$\boxed{\textbf{(B)}}$$

</details>

---

<details><summary><strong>Problem 19 Solution</strong></summary>

**(a) Partial fractions of $\frac{3}{n(n+3)}$:**

$$\frac{3}{n(n+3)} = \frac{A}{n} + \frac{B}{n+3}$$

Multiply by $n(n+3)$: $3 = A(n+3) + Bn$.

Set $n = 0$: $3 = 3A \implies A = 1$.

Set $n = -3$: $3 = -3B \implies B = -1$.

$$\boxed{\frac{3}{n(n+3)} = \frac{1}{n} - \frac{1}{n+3}}$$

---

**(b) First 8 terms of the partial sum:**

$$S_N = \sum_{n=1}^{N}\left(\frac{1}{n} - \frac{1}{n+3}\right)$$

Writing out terms:

$$n=1: \quad \frac{1}{1} - \frac{1}{4}$$

$$n=2: \quad \frac{1}{2} - \frac{1}{5}$$

$$n=3: \quad \frac{1}{3} - \frac{1}{6}$$

$$n=4: \quad \frac{1}{4} - \frac{1}{7}$$

$$n=5: \quad \frac{1}{5} - \frac{1}{8}$$

$$n=6: \quad \frac{1}{6} - \frac{1}{9}$$

$$n=7: \quad \frac{1}{7} - \frac{1}{10}$$

$$n=8: \quad \frac{1}{8} - \frac{1}{11}$$

The cancellation has a gap of 3. The $-\frac{1}{4}$ from $n=1$ cancels with the $+\frac{1}{4}$ from $n=4$. The $-\frac{1}{5}$ from $n=2$ cancels with $+\frac{1}{5}$ from $n=5$. And so on.

The surviving terms from the beginning: $\frac{1}{1}$, $\frac{1}{2}$, $\frac{1}{3}$ (the first three positive terms).

The surviving terms from the end: $-\frac{1}{N+1}$, $-\frac{1}{N+2}$, $-\frac{1}{N+3}$ (the last three negative terms).

---

**(c) Explicit formula and evaluation:**

$$S_N = 1 + \frac{1}{2} + \frac{1}{3} - \frac{1}{N+1} - \frac{1}{N+2} - \frac{1}{N+3}$$

$$= \frac{11}{6} - \frac{1}{N+1} - \frac{1}{N+2} - \frac{1}{N+3}$$

Taking the limit:

$$\sum_{n=1}^{\infty}\frac{3}{n(n+3)} = \lim_{N \to \infty} S_N = \frac{11}{6} - 0 - 0 - 0 = \boxed{\frac{11}{6}}$$

</details>

---

<details><summary><strong>Problem 20 Solution</strong></summary>

**(a) Series expression for total donuts:**

Day 1: 120 donuts. Day 2: $120 \cdot \frac{2}{3}$. Day 3: $120 \cdot \left(\frac{2}{3}\right)^2$. In general, day $n$: $120\left(\frac{2}{3}\right)^{n-1}$.

$$\boxed{D = \sum_{n=1}^{\infty}120\left(\frac{2}{3}\right)^{n-1} = \sum_{n=0}^{\infty}120\left(\frac{2}{3}\right)^{n}}$$

---

**(b) Total donuts if the promotion runs forever:**

Geometric series with $a = 120$ and $r = \frac{2}{3}$. Since $|r| < 1$:

$$D = \frac{120}{1 - \frac{2}{3}} = \frac{120}{\frac{1}{3}} = \boxed{360 \text{ donuts}}$$

---

**(c) After how many complete days will the shop have given away at least 350 donuts?**

The partial sum is:

$$S_N = 120 \cdot \frac{1 - \left(\frac{2}{3}\right)^N}{1 - \frac{2}{3}} = 120 \cdot \frac{1 - \left(\frac{2}{3}\right)^N}{\frac{1}{3}} = 360\left(1 - \left(\frac{2}{3}\right)^N\right)$$

We need $S_N \geq 350$:

$$360\left(1 - \left(\frac{2}{3}\right)^N\right) \geq 350$$

$$1 - \left(\frac{2}{3}\right)^N \geq \frac{350}{360} = \frac{35}{36}$$

$$\left(\frac{2}{3}\right)^N \leq \frac{1}{36}$$

Take the natural log (note: $\ln\frac{2}{3} < 0$, so the inequality flips):

$$N \ln\frac{2}{3} \leq \ln\frac{1}{36}$$

$$N \geq \frac{\ln\frac{1}{36}}{\ln\frac{2}{3}} = \frac{-\ln 36}{\ln 2 - \ln 3} = \frac{\ln 36}{\ln 3 - \ln 2}$$

Computing numerically:

$$N \geq \frac{\ln 36}{\ln 1.5} = \frac{3.5835}{0.4055} \approx 8.84$$

Since $N$ must be a whole number, $N = 9$.

**Verify:** $S_9 = 360\left(1 - \left(\frac{2}{3}\right)^9\right) = 360\left(1 - \frac{512}{19683}\right) = 360 \cdot \frac{19171}{19683} \approx 350.65 \geq 350$. $\checkmark$

$S_8 = 360\left(1 - \left(\frac{2}{3}\right)^8\right) = 360\left(1 - \frac{256}{6561}\right) \approx 345.97 < 350$. $\checkmark$

$$\boxed{N = 9 \text{ days}}$$

---

**(d) Does $\sum_{n=1}^{\infty}\frac{120}{n}$ converge or diverge?**

$$\sum_{n=1}^{\infty}\frac{120}{n} = 120\sum_{n=1}^{\infty}\frac{1}{n}$$

This is 120 times the harmonic series, which **diverges**.

By the scalar multiple property, since $\sum \frac{1}{n}$ diverges, $120\sum \frac{1}{n}$ also **diverges**.

In practical terms: giving away $\frac{120}{n}$ donuts on day $n$ means the daily amount shrinks to zero, but it doesn't shrink fast enough. The total number of donuts given away grows without bound. The shop would eventually need to give away infinitely many donuts -- time to order more flour from Sesame Donuts headquarters.

$$\boxed{\text{Diverges (scalar multiple of the harmonic series)}}$$

</details>

---

## What's Next

You've just taken your first steps into the world of infinite series -- learning to tell the difference between sums that settle down to a finite number and sums that spiral off to infinity. You can now evaluate geometric series, telescope your way through cleverly structured sums, spot instant divergence with the nth Term Test, and classify p-series by their exponent. But here's the thing: most series you'll encounter on the AP exam aren't geometric, telescoping, or p-series. They're messier. How do you determine convergence for something like $\sum \frac{n^2}{3^n}$ or $\sum \frac{\ln n}{n^2}$? That's where **[Convergence Tests](/calculus/convergence-tests)** come in -- a toolkit of powerful tests (Integral Test, Comparison Test, Ratio Test, Alternating Series Test, and more) that let you classify virtually any series. Think of this article as learning to recognize the basic boba flavors at Ding Tea; the next article teaches you how to identify every single item on the menu.

---

<div align="center">

[← Sequences](/calculus/sequences) | [Convergence Tests →](/calculus/convergence-tests)

</div>
