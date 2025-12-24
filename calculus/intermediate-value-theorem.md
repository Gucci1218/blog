# The Intermediate Value Theorem

## Learning Objectives

By the end of this article, you will be able to:

- State the Intermediate Value Theorem precisely
- Explain why continuity is essential for the theorem
- Use IVT to prove the existence of roots and solutions
- Apply IVT to guarantee values in real-world contexts
- Identify when IVT can and cannot be applied
- Solve AP Calculus multiple choice and free response problems using IVT

---

## The Core Concept: No Skipping Allowed

### The Intuition

Imagine you're hiking up a mountain. You start at 1,000 feet elevation and end at 5,000 feet. At some point during your hike, you **must** have been at exactly 3,000 feet. You can't teleport from below 3,000 feet to above 3,000 feet—you have to pass through every elevation in between.

This is the essence of the Intermediate Value Theorem: **a continuous function can't skip values**.

### Real-World Examples

**Temperature:** If the temperature was 60°F at 8 AM and 80°F at noon, then at some time between 8 AM and noon, the temperature was exactly 70°F (assuming temperature changes continuously).

**Growth:** If a child was 3 feet tall at age 5 and 5 feet tall at age 10, then at some age between 5 and 10, the child was exactly 4 feet tall.

**Speed:** If a car is stopped (0 mph) and later traveling at 60 mph, it must have been going exactly 35 mph at some moment in between.

### The Formal Statement

**Intermediate Value Theorem (IVT):**

If $f$ is continuous on the closed interval $[a, b]$ and $N$ is any number between $f(a)$ and $f(b)$, then there exists at least one number $c$ in $(a, b)$ such that $f(c) = N$.

$$\boxed{
\text{If } f \text{ is continuous on } [a,b] \text{ and } f(a) < N < f(b) \text{ (or } f(b) < N < f(a) \text{)},
}$$
$$\boxed{
\text{then } \exists \, c \in (a, b) \text{ such that } f(c) = N.
}$$

### Visual Representation

```
    y
    |
f(b)|_ _ _ _ _ _ _ _ _ ●
    |                 /
  N |_ _ _ _ _ _ _ _ ● c is here!
    |              /
    |            /
f(a)|_ _ _ _ _ ●
    |
    |_________|___|_____|_______ x
              a   c     b
```

The horizontal line $y = N$ must intersect the curve at least once between $a$ and $b$.

---

## The Three Requirements

For IVT to apply, you need **all three** conditions:

### 1. Continuity on $[a, b]$

The function must be continuous on the entire closed interval. No holes, jumps, or asymptotes allowed.

**Why it matters:** A discontinuous function can "jump over" values.

```
Continuous:                 Discontinuous:
    |    /                      |    ●
    |   /                       |    |
  N |--●-- (must cross)       N |-------- (can skip!)
    | /                         |  ○
    |/                          | /
```

### 2. $N$ is Between $f(a)$ and $f(b)$

The target value $N$ must be strictly between the endpoint values. It doesn't matter which endpoint is larger—$N$ just needs to be in the middle.

- If $f(a) < f(b)$, then $f(a) < N < f(b)$
- If $f(a) > f(b)$, then $f(b) < N < f(a)$

### 3. Looking for $c$ in the Open Interval $(a, b)$

The theorem guarantees $c$ exists somewhere strictly between $a$ and $b$ (not at the endpoints).

### Common Mistake Alert

IVT does **not** tell you:
- How many values of $c$ exist (there could be 1, 2, 100, or infinitely many)
- Where exactly $c$ is located
- How to find $c$

It only guarantees **existence**—at least one such $c$ must exist.

---

## The Most Important Application: Finding Roots

### The Root-Finding Version

If $f$ is continuous on $[a, b]$ and $f(a)$ and $f(b)$ have **opposite signs**, then there exists at least one $c$ in $(a, b)$ such that $f(c) = 0$.

$$\boxed{
f(a) \cdot f(b) < 0 \implies \exists \, c \in (a, b) \text{ with } f(c) = 0
}$$

**Why?** If $f(a) > 0$ and $f(b) < 0$ (or vice versa), then $0$ is between $f(a)$ and $f(b)$. By IVT, the function must equal $0$ somewhere in between.

### Example: Proving a Root Exists

**Problem:** Show that $f(x) = x^3 - x - 1$ has a root in the interval $[1, 2]$.

**Solution:**

**Step 1: Verify continuity**
$f(x) = x^3 - x - 1$ is a polynomial, so it's continuous everywhere, including on $[1, 2]$. ✓

**Step 2: Evaluate at endpoints**
$$f(1) = 1 - 1 - 1 = -1 < 0$$
$$f(2) = 8 - 2 - 1 = 5 > 0$$

**Step 3: Apply IVT**
Since $f$ is continuous on $[1, 2]$ and $f(1) < 0 < f(2)$, by the Intermediate Value Theorem, there exists at least one $c$ in $(1, 2)$ such that $f(c) = 0$.

**Conclusion:** The equation $x^3 - x - 1 = 0$ has at least one solution in the interval $(1, 2)$.

---

## Worked Examples

### Example 1: Basic IVT Application

**Problem:** Given that $f$ is continuous on $[0, 4]$ with $f(0) = 2$ and $f(4) = 10$, prove that $f(c) = 7$ for some $c$ in $(0, 4)$.

**Solution:**

- $f$ is continuous on $[0, 4]$ ✓
- $f(0) = 2$ and $f(4) = 10$
- $7$ is between $2$ and $10$ ✓

By IVT, there exists $c \in (0, 4)$ such that $f(c) = 7$. ∎

---

### Example 2: Proving a Solution Exists

**Problem:** Show that the equation $\cos x = x$ has at least one solution.

**Solution:**

Let $f(x) = \cos x - x$. We need to find where $f(x) = 0$.

$f$ is continuous everywhere (difference of continuous functions).

**Try some values:**
$$f(0) = \cos 0 - 0 = 1 - 0 = 1 > 0$$
$$f(1) = \cos 1 - 1 \approx 0.54 - 1 = -0.46 < 0$$

Since $f(0) > 0$ and $f(1) < 0$, and $f$ is continuous on $[0, 1]$, by IVT there exists $c \in (0, 1)$ such that $f(c) = 0$.

Therefore, $\cos c = c$ for some $c \in (0, 1)$. ∎

---

### Example 3: Finding an Interval Containing a Root

**Problem:** Find an interval of length 1 that contains a root of $g(x) = x^3 + 2x - 5$.

**Solution:**

$g$ is a polynomial, so it's continuous everywhere.

**Test integer values:**
$$g(0) = 0 + 0 - 5 = -5 < 0$$
$$g(1) = 1 + 2 - 5 = -2 < 0$$
$$g(2) = 8 + 4 - 5 = 7 > 0$$

Since $g(1) < 0$ and $g(2) > 0$, by IVT there's a root in $(1, 2)$.

**Answer:** The interval $[1, 2]$ contains a root.

---

### Example 4: Narrowing Down the Root Location

**Problem:** The function $f(x) = x^4 - 3x - 2$ has a root between 1 and 2. Narrow down the location to an interval of length 0.5.

**Solution:**

Verify: $f(1) = 1 - 3 - 2 = -4 < 0$ and $f(2) = 16 - 6 - 2 = 8 > 0$ ✓

**Test the midpoint:**
$$f(1.5) = (1.5)^4 - 3(1.5) - 2 = 5.0625 - 4.5 - 2 = -1.4375 < 0$$

Since $f(1.5) < 0$ and $f(2) > 0$, the root is in $(1.5, 2)$.

**Answer:** The root is in the interval $[1.5, 2]$.

---

### Example 5: Multiple Roots

**Problem:** Show that $h(x) = x^3 - 3x$ has at least three roots.

**Solution:**

$h$ is a polynomial, continuous everywhere.

**Evaluate at several points:**
$$h(-2) = -8 + 6 = -2 < 0$$
$$h(-1) = -1 + 3 = 2 > 0$$
$$h(0) = 0$$
$$h(1) = 1 - 3 = -2 < 0$$
$$h(2) = 8 - 6 = 2 > 0$$

**Apply IVT:**
- $h(-2) < 0$ and $h(-1) > 0$ → root in $(-2, -1)$
- $h(0) = 0$ → root at $x = 0$
- $h(1) < 0$ and $h(2) > 0$ → root in $(1, 2)$

**Conclusion:** There are at least three roots: one in $(-2, -1)$, one at $x = 0$, and one in $(1, 2)$.

(In fact, we can factor: $h(x) = x(x^2 - 3) = x(x - \sqrt{3})(x + \sqrt{3})$, confirming exactly three roots.)

---

### Example 6: IVT with a Table

**Problem:** The continuous function $f$ has values given in the table below. What is the minimum number of times $f(x) = 3$ on $[0, 10]$?

| $x$ | 0 | 2 | 4 | 6 | 8 | 10 |
|-----|---|---|---|---|---|----|
| $f(x)$ | 1 | 5 | 2 | 4 | 1 | 6 |

**Solution:**

We look for intervals where $f$ crosses the value 3:

- $[0, 2]$: $f(0) = 1 < 3 < 5 = f(2)$ → IVT guarantees at least one crossing ✓
- $[2, 4]$: $f(2) = 5 > 3 > 2 = f(4)$ → at least one crossing ✓
- $[4, 6]$: $f(4) = 2 < 3 < 4 = f(6)$ → at least one crossing ✓
- $[6, 8]$: $f(6) = 4 > 3 > 1 = f(8)$ → at least one crossing ✓
- $[8, 10]$: $f(8) = 1 < 3 < 6 = f(10)$ → at least one crossing ✓

**Answer:** At least **5** times.

---

### Example 7: When IVT Doesn't Apply

**Problem:** Let $f(x) = \frac{1}{x}$. Does IVT guarantee that $f(c) = 0$ for some $c$ in $[-1, 1]$?

**Solution:**

$f(x) = \frac{1}{x}$ is **not continuous** on $[-1, 1]$ because it's undefined at $x = 0$.

Even though $f(-1) = -1 < 0$ and $f(1) = 1 > 0$, we cannot apply IVT.

In fact, $f(x) = \frac{1}{x}$ never equals 0 for any $x$, demonstrating why continuity is essential.

**Answer:** No, IVT does not apply because $f$ is not continuous on the interval.

---

### Example 8: Application to Temperature

**Problem:** At 6 AM, the temperature was 58°F. At 2 PM, it was 84°F. Assuming temperature is a continuous function of time, prove that at some moment the temperature was exactly 70°F.

**Solution:**

Let $T(t)$ represent temperature at time $t$, where $t$ is in hours after midnight.

- $T(6) = 58$
- $T(14) = 84$ (2 PM = 14:00)
- Temperature varies continuously, so $T$ is continuous on $[6, 14]$

Since $58 < 70 < 84$, by IVT there exists some time $c \in (6, 14)$ such that $T(c) = 70$.

**Conclusion:** At some moment between 6 AM and 2 PM, the temperature was exactly 70°F. ∎

---

### Example 9: Fixed Point Theorem

**Problem:** Let $f$ be continuous on $[0, 1]$ with $0 \leq f(x) \leq 1$ for all $x$ in $[0, 1]$. Prove that there exists $c \in [0, 1]$ such that $f(c) = c$ (a "fixed point").

**Solution:**

Define $g(x) = f(x) - x$.

$g$ is continuous on $[0, 1]$ (difference of continuous functions).

**Evaluate at endpoints:**
$$g(0) = f(0) - 0 = f(0) \geq 0 \quad \text{(since } f(x) \geq 0 \text{)}$$
$$g(1) = f(1) - 1 \leq 0 \quad \text{(since } f(x) \leq 1 \text{)}$$

**Cases:**
- If $g(0) = 0$, then $f(0) = 0$, so $c = 0$ is a fixed point.
- If $g(1) = 0$, then $f(1) = 1$, so $c = 1$ is a fixed point.
- If $g(0) > 0$ and $g(1) < 0$, by IVT there exists $c \in (0, 1)$ with $g(c) = 0$, meaning $f(c) = c$.

**Conclusion:** In all cases, there exists $c \in [0, 1]$ such that $f(c) = c$. ∎

---

### Example 10: Proving Existence of Solutions

**Problem:** Prove that the equation $e^x = 3 - x$ has a solution.

**Solution:**

Let $f(x) = e^x - (3 - x) = e^x + x - 3$.

$f$ is continuous everywhere.

**Test values:**
$$f(0) = 1 + 0 - 3 = -2 < 0$$
$$f(1) = e + 1 - 3 = e - 2 \approx 0.718 > 0$$

Since $f(0) < 0$ and $f(1) > 0$, by IVT there exists $c \in (0, 1)$ such that $f(c) = 0$.

Therefore, $e^c = 3 - c$ for some $c \in (0, 1)$. ∎

---

## What IVT Does NOT Tell You

### IVT Guarantees Existence, Not Uniqueness

The theorem says "there exists **at least one**" value of $c$. There could be multiple values.

```
Example: f(x) = sin(x) on [0, 4π]

If we want f(c) = 0.5, IVT guarantees a solution exists.
But there are actually MANY solutions!
```

### IVT Doesn't Help You Find $c$

To actually find the value of $c$, you'd need other methods:
- Algebraic solving
- Graphing
- Numerical methods (bisection, Newton's method)

IVT just proves the solution exists—finding it is a separate problem.

### IVT Is One-Directional

**IVT says:** Continuous + endpoints straddle $N$ → solution exists

**IVT does NOT say:** Solution exists → endpoints straddle $N$

A function could equal $N$ even if $N$ isn't between $f(a)$ and $f(b)$!

---

## The Converse Is False!

### What Might Seem True

"If $f(c) = N$ for some $c$ in $(a, b)$, then $N$ must be between $f(a)$ and $f(b)$."

**This is FALSE!**

### Counterexample

Let $f(x) = x^2$ on $[-1, 2]$.

- $f(-1) = 1$
- $f(2) = 4$
- $f(0) = 0$

Here, $f(0) = 0$ even though $0$ is not between $f(-1) = 1$ and $f(2) = 4$.

---

## Practice Problems

### Basic Problems (1-5)

**1.** Use IVT to show that $f(x) = x^2 - 2$ has a root in $[1, 2]$.

---

**2.** Given that $g$ is continuous on $[2, 6]$ with $g(2) = -3$ and $g(6) = 5$, prove there exists $c \in (2, 6)$ with $g(c) = 0$.

---

**3.** Show that the equation $x^3 = x + 1$ has a solution in the interval $[1, 2]$.

---

**4.** The function $f$ is continuous on $[0, 5]$ with $f(0) = 4$ and $f(5) = -2$. Must there be a value $c$ where $f(c) = 1$? Explain.

---

**5.** Explain why IVT cannot be used to show that $f(x) = \tan x$ equals 0 somewhere in $\left(\frac{\pi}{4}, \frac{3\pi}{4}\right)$.

---

### Intermediate Problems (6-10)

**6.** Show that $\ln x = 4 - x$ has at least one solution.

---

**7.** The continuous function $f$ has the following values:

| $x$ | 1 | 3 | 5 | 7 | 9 |
|-----|---|---|---|---|---|
| $f(x)$ | 2 | 6 | 4 | 8 | 3 |

What is the minimum number of solutions to $f(x) = 5$ on $[1, 9]$?

---

**8.** Find an interval of length 0.5 containing a root of $f(x) = x^3 + x - 1$.

---

**9.** Prove that $2^x = 3x$ has a solution in $(1, 2)$.

---

**10.** Let $f$ be continuous on $[0, 2]$ with $f(0) = f(2) = 0$ and $f(1) = 1$. Prove that $f(c) = \frac{1}{2}$ for at least two values of $c$ in $[0, 2]$.

---

### Advanced Problems (11-15)

**11.** Show that every polynomial of odd degree has at least one real root.

---

**12.** Let $f$ and $g$ be continuous on $[a, b]$ with $f(a) > g(a)$ and $f(b) < g(b)$. Prove there exists $c \in (a, b)$ with $f(c) = g(c)$.

---

**13.** Prove that $x \cdot 2^x = 1$ has exactly one positive solution.

---

**14.** A car travels continuously along a straight road. At time $t = 0$, the car is at position $s = 0$. At time $t = 2$ hours, the car is at position $s = 120$ miles. Prove that at some instant, the car's speedometer read exactly 60 mph.

*(Hint: Consider the average velocity and what IVT implies about instantaneous velocity.)*

---

**15.** Let $f$ be continuous on $[0, 1]$ with $f(0) = 0$ and $f(1) = 1$. Prove that for any $n \geq 1$, there exist $n$ distinct points $c_1 < c_2 < \cdots < c_n$ in $(0, 1)$ such that $f(c_k) = \frac{k}{n+1}$ for $k = 1, 2, \ldots, n$.

---

### Challenge Problems (16-18)

**16.** Let $f$ be continuous on $[0, 2]$ with $f(0) = f(2)$. Prove that there exist points $c_1$ and $c_2$ with $c_2 - c_1 = 1$ such that $f(c_1) = f(c_2)$.

*(Hint: Consider $g(x) = f(x + 1) - f(x)$ on $[0, 1]$.)*

---

**17.** Suppose $f$ is continuous on $\mathbb{R}$ and $\lim_{x \to \infty} f(x) = \lim_{x \to -\infty} f(x) = 0$. If $f(0) = 1$, prove that $f$ achieves every value in $(0, 1]$.

---

**18.** Let $p(x)$ be a polynomial with $p(0) = -1$ and $p(1) = 1$. Prove that there is a root of $p$ in $(0, 1)$. Furthermore, if $p$ has exactly one root in $(0, 1)$, what can you conclude about the degree of $p$?

---

## Solutions to Practice Problems

### Solution 1

$f(x) = x^2 - 2$ is a polynomial, so it's continuous everywhere.

$$f(1) = 1 - 2 = -1 < 0$$
$$f(2) = 4 - 2 = 2 > 0$$

Since $f(1) < 0 < f(2)$ and $f$ is continuous on $[1, 2]$, by IVT there exists $c \in (1, 2)$ such that $f(c) = 0$.

Therefore, $x^2 - 2 = 0$ has a root in $(1, 2)$.

(Note: This root is $\sqrt{2} \approx 1.414$.)

---

### Solution 2

$g$ is continuous on $[2, 6]$. (Given)

$g(2) = -3 < 0$ and $g(6) = 5 > 0$.

Since $0$ is between $-3$ and $5$, by IVT there exists $c \in (2, 6)$ such that $g(c) = 0$. ∎

---

### Solution 3

Rewrite as $x^3 - x - 1 = 0$ and let $f(x) = x^3 - x - 1$.

$f$ is a polynomial, continuous everywhere.

$$f(1) = 1 - 1 - 1 = -1 < 0$$
$$f(2) = 8 - 2 - 1 = 5 > 0$$

By IVT, there exists $c \in (1, 2)$ such that $f(c) = 0$, meaning $c^3 = c + 1$. ∎

---

### Solution 4

Yes. Since $f$ is continuous on $[0, 5]$, $f(0) = 4$, $f(5) = -2$, and $1$ is between $-2$ and $4$, by IVT there must exist $c \in (0, 5)$ such that $f(c) = 1$. ∎

---

### Solution 5

$\tan x$ is **not continuous** on $\left(\frac{\pi}{4}, \frac{3\pi}{4}\right)$ because it has a vertical asymptote at $x = \frac{\pi}{2}$.

Since continuity on the interval is a requirement for IVT, we cannot apply the theorem.

---

### Solution 6

Let $f(x) = \ln x - (4 - x) = \ln x + x - 4$.

$f$ is continuous on $(0, \infty)$.

$$f(1) = 0 + 1 - 4 = -3 < 0$$
$$f(4) = \ln 4 + 4 - 4 = \ln 4 \approx 1.39 > 0$$

By IVT, there exists $c \in (1, 4)$ such that $f(c) = 0$, meaning $\ln c = 4 - c$. ∎

---

### Solution 7

Check where $f$ crosses 5:

- $[1, 3]$: $f(1) = 2 < 5 < 6 = f(3)$ → at least 1 crossing ✓
- $[3, 5]$: $f(3) = 6 > 5 > 4 = f(5)$ → at least 1 crossing ✓
- $[5, 7]$: $f(5) = 4 < 5 < 8 = f(7)$ → at least 1 crossing ✓
- $[7, 9]$: $f(7) = 8 > 5 > 3 = f(9)$ → at least 1 crossing ✓

**Answer:** At least **4** solutions.

---

### Solution 8

$f(x) = x^3 + x - 1$ is continuous everywhere.

$$f(0) = 0 + 0 - 1 = -1 < 0$$
$$f(1) = 1 + 1 - 1 = 1 > 0$$

Root is in $(0, 1)$. Now test the midpoint:

$$f(0.5) = 0.125 + 0.5 - 1 = -0.375 < 0$$

Since $f(0.5) < 0$ and $f(1) > 0$, the root is in $(0.5, 1)$.

**Answer:** The interval $[0.5, 1]$ (length 0.5) contains a root.

---

### Solution 9

Let $f(x) = 2^x - 3x$.

$f$ is continuous everywhere.

$$f(1) = 2 - 3 = -1 < 0$$
$$f(2) = 4 - 6 = -2 < 0$$

Hmm, both are negative. Let's try other values:

$$f(0) = 1 - 0 = 1 > 0$$

So $f(0) > 0$ and $f(1) < 0$. By IVT, there's a root in $(0, 1)$.

Wait, the problem asks for $(1, 2)$. Let me check $f(2)$ again and try $f(4)$:

$$f(4) = 16 - 12 = 4 > 0$$

So $f(2) = -2 < 0$ and $f(4) = 4 > 0$. Root in $(2, 4)$.

Hmm, let me try values more carefully between 1 and 2:

Actually, $f(1) = 2 - 3 = -1 < 0$ and we need to check where it becomes positive.

$f(1.5) = 2^{1.5} - 4.5 = 2\sqrt{2} - 4.5 \approx 2.83 - 4.5 = -1.67 < 0$

Let me try the other direction:
$f(0.5) = \sqrt{2} - 1.5 \approx 1.41 - 1.5 = -0.09 < 0$
$f(0.1) = 2^{0.1} - 0.3 \approx 1.07 - 0.3 = 0.77 > 0$

So there's a root in $(0.1, 0.5)$, not in $(1, 2)$.

Let me reconsider: maybe the problem wants us to find a different crossing. Actually, $2^x$ grows faster than $3x$ eventually:

$f(4) = 16 - 12 = 4 > 0$

So there's a root in $(2, 4)$.

The problem says $(1, 2)$, but there's no root there since $f(1) = -1$ and $f(2) = -2$, both negative.

**Correction:** The equation $2^x = 3x$ has solutions in $(0, 1)$ and $(2, 4)$, but not in $(1, 2)$. Perhaps the problem should read $(0, 1)$ or the equation is different.

---

### Solution 10

$f$ is continuous on $[0, 2]$ with $f(0) = 0$, $f(1) = 1$, $f(2) = 0$.

Since $\frac{1}{2}$ is between $0$ and $1$:

**On $[0, 1]$:** $f(0) = 0 < \frac{1}{2} < 1 = f(1)$

By IVT, there exists $c_1 \in (0, 1)$ with $f(c_1) = \frac{1}{2}$.

**On $[1, 2]$:** $f(1) = 1 > \frac{1}{2} > 0 = f(2)$

By IVT, there exists $c_2 \in (1, 2)$ with $f(c_2) = \frac{1}{2}$.

Since $c_1 \in (0, 1)$ and $c_2 \in (1, 2)$, we have $c_1 \neq c_2$.

Therefore, $f(c) = \frac{1}{2}$ for at least two values of $c$ in $[0, 2]$. ∎

---

### Solution 11

Let $p(x) = a_n x^n + a_{n-1}x^{n-1} + \cdots + a_1 x + a_0$ where $n$ is odd and $a_n \neq 0$.

**Behavior at infinity:**

As $x \to \infty$: The leading term dominates, so $p(x) \to +\infty$ if $a_n > 0$, or $p(x) \to -\infty$ if $a_n < 0$.

As $x \to -\infty$: Since $n$ is odd, $(-x)^n = -x^n$, so $p(x) \to -\infty$ if $a_n > 0$, or $p(x) \to +\infty$ if $a_n < 0$.

**In either case**, $p$ takes on both large positive and large negative values.

Since $p$ is continuous (polynomials are continuous everywhere), and $p$ takes values on both sides of 0, by IVT there must be some $c$ where $p(c) = 0$. ∎

---

### Solution 12

Let $h(x) = f(x) - g(x)$.

$h$ is continuous on $[a, b]$ (difference of continuous functions).

$$h(a) = f(a) - g(a) > 0 \quad \text{(given } f(a) > g(a) \text{)}$$
$$h(b) = f(b) - g(b) < 0 \quad \text{(given } f(b) < g(b) \text{)}$$

By IVT, there exists $c \in (a, b)$ such that $h(c) = 0$.

Therefore, $f(c) - g(c) = 0$, which means $f(c) = g(c)$. ∎

---

### Solution 13

Let $f(x) = x \cdot 2^x - 1$.

**Existence:**
$$f(0) = 0 - 1 = -1 < 0$$
$$f(1) = 2 - 1 = 1 > 0$$

By IVT, there exists at least one root in $(0, 1)$.

**Uniqueness:**

$f'(x) = 2^x + x \cdot 2^x \ln 2 = 2^x(1 + x \ln 2)$

For $x > 0$: $2^x > 0$ and $1 + x \ln 2 > 1 > 0$.

So $f'(x) > 0$ for all $x > 0$, meaning $f$ is strictly increasing on $(0, \infty)$.

A strictly increasing function can cross any horizontal line at most once.

**Conclusion:** There is exactly one positive solution. ∎

---

### Solution 14

Let $s(t)$ be the position at time $t$. We're given $s(0) = 0$ and $s(2) = 120$.

The average velocity is $\frac{120 - 0}{2 - 0} = 60$ mph.

By the Mean Value Theorem (which we'll cover later), if $s$ is differentiable on $(0, 2)$, then there exists $c \in (0, 2)$ such that $s'(c) = 60$ mph.

**Using IVT approach:** Assume velocity $v(t) = s'(t)$ is continuous.

If the car's velocity is always less than 60 mph or always greater than 60 mph, then:
- If $v(t) < 60$ for all $t$, then $s(2) - s(0) = \int_0^2 v(t) \, dt < 60 \cdot 2 = 120$. Contradiction.
- Similarly for $v(t) > 60$.

So velocity must be both above and below 60 at different times, and by IVT (applied to $v$), it must equal exactly 60 at some moment. ∎

---

### Solution 15

$f$ is continuous on $[0, 1]$ with $f(0) = 0$ and $f(1) = 1$.

For each $k$ from $1$ to $n$, we need to show $f(c_k) = \frac{k}{n+1}$.

Note that $0 < \frac{1}{n+1} < \frac{2}{n+1} < \cdots < \frac{n}{n+1} < 1$.

Since $f(0) = 0 < \frac{k}{n+1} < 1 = f(1)$ for each $k$, by IVT there exists $c_k \in (0, 1)$ such that $f(c_k) = \frac{k}{n+1}$.

We need to verify these are distinct. If $f$ is strictly increasing, they would automatically be distinct. In general, IVT guarantees existence, and by careful selection of the $c_k$ values (choosing the smallest such value for each $k$), we can ensure $c_1 < c_2 < \cdots < c_n$. ∎

---

### Solution 16

Define $g(x) = f(x + 1) - f(x)$ on $[0, 1]$.

$g$ is continuous on $[0, 1]$ (composition and difference of continuous functions).

$$g(0) = f(1) - f(0)$$
$$g(1) = f(2) - f(1)$$

Now, $g(0) + g(1) = f(1) - f(0) + f(2) - f(1) = f(2) - f(0) = 0$ (since $f(0) = f(2)$).

So $g(0) = -g(1)$.

**Case 1:** If $g(0) = 0$, then $f(1) = f(0)$, so let $c_1 = 0$, $c_2 = 1$.

**Case 2:** If $g(0) \neq 0$, then $g(0)$ and $g(1)$ have opposite signs.

By IVT, there exists $c \in (0, 1)$ such that $g(c) = 0$.

This means $f(c + 1) - f(c) = 0$, so $f(c) = f(c + 1)$.

Let $c_1 = c$ and $c_2 = c + 1$. Then $c_2 - c_1 = 1$ and $f(c_1) = f(c_2)$. ∎

---

### Solution 17

$f$ is continuous on $\mathbb{R}$, $\lim_{x \to \pm\infty} f(x) = 0$, and $f(0) = 1$.

Let $y$ be any value in $(0, 1]$.

**For $y = 1$:** We have $f(0) = 1$, so $y = 1$ is achieved.

**For $0 < y < 1$:**

Since $\lim_{x \to \infty} f(x) = 0$ and $f(0) = 1 > y$, there exists some large $M > 0$ such that $f(M) < y$.

We have $f(0) = 1 > y$ and $f(M) < y$.

By IVT applied to $[0, M]$, there exists $c \in (0, M)$ such that $f(c) = y$.

Similarly for negative $x$ using $\lim_{x \to -\infty} f(x) = 0$.

Therefore, $f$ achieves every value in $(0, 1]$. ∎

---

### Solution 18

$p$ is a polynomial, so it's continuous everywhere.

$p(0) = -1 < 0$ and $p(1) = 1 > 0$.

By IVT, there exists $c \in (0, 1)$ such that $p(c) = 0$.

**For the second part:**

If $p$ has exactly one root in $(0, 1)$, we can't immediately determine the degree. However:

- A polynomial of degree 1 (linear) has exactly one root total.
- A polynomial of degree 2 could have 0, 1, or 2 roots.
- Higher degrees could have more roots.

The condition of exactly one root in $(0, 1)$ combined with $p(0) < 0$ and $p(1) > 0$ suggests the polynomial crosses the $x$-axis exactly once in that interval. This is consistent with any odd-degree polynomial, or an even-degree polynomial that just touches or crosses once. Without more constraints, we cannot uniquely determine the degree. ∎

---

## AP Exam Tips

### The Standard IVT Template

When writing a solution using IVT:

1. **State continuity:** "$f$ is continuous on $[a, b]$ because..."
2. **Evaluate endpoints:** "$f(a) = ...$" and "$f(b) = ...$"
3. **Note the target value:** "$N = ...$ is between $f(a)$ and $f(b)$"
4. **Conclude:** "By the Intermediate Value Theorem, there exists $c \in (a, b)$ such that $f(c) = N$."

### Free Response Example

**Question:** Show that $x^5 + x = 7$ has a solution.

**Model Answer:**

"Let $f(x) = x^5 + x - 7$. Since $f$ is a polynomial, it is continuous on $[1, 2]$.

$f(1) = 1 + 1 - 7 = -5 < 0$

$f(2) = 32 + 2 - 7 = 27 > 0$

Since $f(1) < 0 < f(2)$ and $f$ is continuous on $[1, 2]$, by the Intermediate Value Theorem, there exists $c \in (1, 2)$ such that $f(c) = 0$.

Therefore, $c^5 + c = 7$ for some $c \in (1, 2)$."

### Common Mistakes

**Mistake 1: Forgetting to verify continuity**
Always explicitly state why the function is continuous.

**Mistake 2: Wrong interval notation**
IVT guarantees $c$ in the **open** interval $(a, b)$, not $[a, b]$.

**Mistake 3: Claiming more than IVT guarantees**
IVT only guarantees existence, not uniqueness or location.

**Mistake 4: Applying IVT when not applicable**
Check for discontinuities in the interval!

### Quick Check Questions

On multiple choice, IVT questions often ask:
- "Must there exist a value where $f(x) = k$?"
- "What is the minimum number of solutions?"
- "Which statement must be true?"

---

## Summary

**The Intermediate Value Theorem:**

If $f$ is continuous on $[a, b]$ and $N$ is between $f(a)$ and $f(b)$, then there exists at least one $c \in (a, b)$ such that $f(c) = N$.

**Key Requirements:**
1. Continuity on the closed interval $[a, b]$
2. $N$ strictly between $f(a)$ and $f(b)$
3. Conclusion: $c$ exists in the open interval $(a, b)$

**Main Applications:**
- Proving roots exist (when $f(a)$ and $f(b)$ have opposite signs)
- Guaranteeing a function takes on specific values
- Finding intervals containing solutions
- Fixed point theorems

**Remember:**
- IVT guarantees existence, not uniqueness
- IVT doesn't tell you where $c$ is or how to find it
- Continuity is essential—discontinuous functions can skip values

The Intermediate Value Theorem is a powerful existence theorem that connects the intuition of "continuous functions don't skip values" with rigorous mathematical proof!

---

**Next Topics to Explore:**
- Making Functions Continuous
- Properties of Continuous Functions
- Introduction to Derivatives
