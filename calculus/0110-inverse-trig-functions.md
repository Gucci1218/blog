# Inverse Trigonometric Functions
<p class="article-date">July 26, 2024</p>

## Prerequisites
Before diving in, make sure you're comfortable with:
- [Unit Circle](/calculus/0108-unit-circle)
- [Inverse Functions](/calculus/0103-inverse-functions)
- [Trig Identities](/calculus/0109-trig-identities)

## Learning Objectives
By the end of this section, you will be able to:
- Understand the need for restricted domains in inverse trig functions
- Evaluate inverse trig functions exactly and with a calculator
- Know the domains and ranges of all six inverse trig functions
- Simplify compositions of trig and inverse trig functions
- Graph inverse trig functions

## The Big Picture: Finding Angles

Regular trig functions answer: "Given an angle, what's the ratio?"
$$\sin(30°) = \frac{1}{2}$$

Inverse trig functions answer: "Given a ratio, what's the angle?"
$$\arcsin\left(\frac{1}{2}\right) = 30°$$

> **Notation**: $\arcsin(x) = \sin^{-1}(x)$ (both mean the same thing)
>
> **Warning**: $\sin^{-1}(x) \ne \frac{1}{\sin(x)}$ (that's $\csc(x)$!)

## Why We Need Restricted Domains

The sine function is **not one-to-one** on its natural domain because it repeats every $2\pi$:
- $\sin(30°) = \frac{1}{2}$
- $\sin(150°) = \frac{1}{2}$
- $\sin(390°) = \frac{1}{2}$
- ... infinitely many angles!

To have an inverse, we **restrict the domain** to where the function is one-to-one.

## The Three Main Inverse Trig Functions

### Arcsine: $y = \arcsin(x)$

**Definition**: $y = \arcsin(x)$ means $\sin(y) = x$ where $-\frac{\pi}{2} \le y \le \frac{\pi}{2}$

| Property | Value |
|----------|-------|
| Domain | $[-1, 1]$ |
| Range | $\left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$ |
| Output quadrants | Q1 and Q4 |

**Example**: $\arcsin\left(\frac{\sqrt{2}}{2}\right) = \frac{\pi}{4}$ because $\sin\frac{\pi}{4} = \frac{\sqrt{2}}{2}$

### Arccosine: $y = \arccos(x)$

**Definition**: $y = \arccos(x)$ means $\cos(y) = x$ where $0 \le y \le \pi$

| Property | Value |
|----------|-------|
| Domain | $[-1, 1]$ |
| Range | $[0, \pi]$ |
| Output quadrants | Q1 and Q2 |

**Example**: $\arccos\left(-\frac{1}{2}\right) = \frac{2\pi}{3}$ because $\cos\frac{2\pi}{3} = -\frac{1}{2}$

### Arctangent: $y = \arctan(x)$

**Definition**: $y = \arctan(x)$ means $\tan(y) = x$ where $-\frac{\pi}{2} < y < \frac{\pi}{2}$

| Property | Value |
|----------|-------|
| Domain | $(-\infty, \infty)$ |
| Range | $\left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$ |
| Output quadrants | Q1 and Q4 |

**Example**: $\arctan(1) = \frac{\pi}{4}$ because $\tan\frac{\pi}{4} = 1$

## Summary Table

| Function | Domain | Range | Output Quadrants |
|----------|--------|-------|------------------|
| $\arcsin(x)$ | $[-1, 1]$ | $\left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$ | Q1, Q4 |
| $\arccos(x)$ | $[-1, 1]$ | $[0, \pi]$ | Q1, Q2 |
| $\arctan(x)$ | $\mathbb{R}$ | $\left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$ | Q1, Q4 |
| $\text{arccsc}(x)$ | $\|x\| \ge 1$ | $\left[-\frac{\pi}{2}, \frac{\pi}{2}\right] \setminus \{0\}$ | Q1, Q4 |
| $\text{arcsec}(x)$ | $\|x\| \ge 1$ | $[0, \pi] \setminus \{\frac{\pi}{2}\}$ | Q1, Q2 |
| $\text{arccot}(x)$ | $\mathbb{R}$ | $(0, \pi)$ | Q1, Q2 |

## Evaluating Inverse Trig Functions

### Step-by-Step Method

1. **Identify the trig ratio** given
2. **Find the reference angle** from the unit circle
3. **Determine the correct quadrant** based on the function's range
4. **Apply the appropriate sign** to get the final answer

### Worked Example 1

**Problem**: Find $\arcsin\left(-\frac{\sqrt{3}}{2}\right)$

**Solution**:

Step 1: We need an angle whose sine is $-\frac{\sqrt{3}}{2}$

Step 2: Reference angle: $\sin^{-1}\frac{\sqrt{3}}{2} = \frac{\pi}{3}$

Step 3: Arcsine range is $[-\frac{\pi}{2}, \frac{\pi}{2}]$, so output is in Q1 or Q4

Step 4: Since the value is negative, we need Q4: $-\frac{\pi}{3}$

**Answer**: $\arcsin\left(-\frac{\sqrt{3}}{2}\right) = -\frac{\pi}{3}$

### Worked Example 2

**Problem**: Find $\arccos\left(-\frac{\sqrt{2}}{2}\right)$

**Solution**:

Step 1: We need an angle whose cosine is $-\frac{\sqrt{2}}{2}$

Step 2: Reference angle: $\frac{\pi}{4}$

Step 3: Arccosine range is $[0, \pi]$, so output is in Q1 or Q2

Step 4: Since cosine is negative, we need Q2: $\pi - \frac{\pi}{4} = \frac{3\pi}{4}$

**Answer**: $\arccos\left(-\frac{\sqrt{2}}{2}\right) = \frac{3\pi}{4}$

### Worked Example 3

**Problem**: Find $\arctan(-1)$

**Solution**:

Step 1: We need an angle whose tangent is $-1$

Step 2: Reference angle: $\frac{\pi}{4}$

Step 3: Arctangent range is $(-\frac{\pi}{2}, \frac{\pi}{2})$

Step 4: Since tangent is negative, we need Q4: $-\frac{\pi}{4}$

**Answer**: $\arctan(-1) = -\frac{\pi}{4}$

## Compositions of Trig and Inverse Trig Functions

### Type 1: $\sin(\arcsin(x))$ and similar

When the inverse trig is inside:
$$\sin(\arcsin(x)) = x \quad \text{for } x \in [-1, 1]$$
$$\cos(\arccos(x)) = x \quad \text{for } x \in [-1, 1]$$
$$\tan(\arctan(x)) = x \quad \text{for } x \in \mathbb{R}$$

### Type 2: $\arcsin(\sin(x))$ and similar

When the trig function is inside, be careful with the range:
$$\arcsin(\sin(x)) = x \quad \text{only if } x \in \left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$$

**Example**: $\arcsin(\sin(\frac{5\pi}{6})) \ne \frac{5\pi}{6}$

Since $\sin\frac{5\pi}{6} = \frac{1}{2}$:
$$\arcsin\left(\frac{1}{2}\right) = \frac{\pi}{6}$$

### Type 3: Mixed functions like $\sin(\arccos(x))$

Use a right triangle or Pythagorean identity.

**Example**: Find $\sin(\arccos(\frac{3}{5}))$

Let $\theta = \arccos(\frac{3}{5})$, so $\cos\theta = \frac{3}{5}$ with $\theta \in [0, \pi]$

Using $\sin^2\theta + \cos^2\theta = 1$:
$$\sin\theta = \sqrt{1 - \frac{9}{25}} = \frac{4}{5}$$

(Positive because $\theta$ is in Q1 or Q2 where sine is positive)

## Graphs of Inverse Trig Functions

### Graph of $y = \arcsin(x)$
- Domain: $[-1, 1]$
- Range: $[-\frac{\pi}{2}, \frac{\pi}{2}]$
- Passes through: $(0, 0)$, $(1, \frac{\pi}{2})$, $(-1, -\frac{\pi}{2})$
- S-shaped curve

### Graph of $y = \arccos(x)$
- Domain: $[-1, 1]$
- Range: $[0, \pi]$
- Passes through: $(0, \frac{\pi}{2})$, $(1, 0)$, $(-1, \pi)$
- Decreasing function

### Graph of $y = \arctan(x)$
- Domain: $(-\infty, \infty)$
- Range: $(-\frac{\pi}{2}, \frac{\pi}{2})$
- Horizontal asymptotes at $y = \pm\frac{\pi}{2}$
- Passes through: $(0, 0)$, $(1, \frac{\pi}{4})$, $(-1, -\frac{\pi}{4})$

## Important Relationships

$$\arcsin(x) + \arccos(x) = \frac{\pi}{2}$$

$$\arctan(x) + \text{arccot}(x) = \frac{\pi}{2}$$

$$\arctan(x) + \arctan\left(\frac{1}{x}\right) = \begin{cases} \frac{\pi}{2} & x > 0 \\ -\frac{\pi}{2} & x < 0 \end{cases}$$

## Key Formulas

| Expression | Result | Condition |
|------------|--------|-----------|
| $\sin(\arcsin x)$ | $x$ | $\|x\| \le 1$ |
| $\cos(\arccos x)$ | $x$ | $\|x\| \le 1$ |
| $\tan(\arctan x)$ | $x$ | all $x$ |
| $\arcsin(\sin x)$ | $x$ | $x \in [-\frac{\pi}{2}, \frac{\pi}{2}]$ |
| $\arccos(\cos x)$ | $x$ | $x \in [0, \pi]$ |
| $\arctan(\tan x)$ | $x$ | $x \in (-\frac{\pi}{2}, \frac{\pi}{2})$ |

## Common Mistakes to Avoid

1. **Confusing $\sin^{-1}$ with $\frac{1}{\sin}$**
   - $\sin^{-1}(x) = \arcsin(x)$, NOT $\csc(x)$

2. **Forgetting range restrictions**
   - $\arcsin\left(\sin\frac{5\pi}{6}\right) = \frac{\pi}{6}$, not $\frac{5\pi}{6}$

3. **Using degrees when radians are expected**
   - Calculator must be in correct mode!

4. **Wrong quadrant for output**
   - Know the range of each inverse function

5. **Thinking $\arcsin(-x) = \pi + \arcsin(x)$**
   - Actually: $\arcsin(-x) = -\arcsin(x)$ (odd function)

## Calculus Connection

Inverse trig functions are essential in calculus:

1. **Derivatives**:
   $$\frac{d}{dx}[\arcsin x] = \frac{1}{\sqrt{1-x^2}}$$
   $$\frac{d}{dx}[\arccos x] = \frac{-1}{\sqrt{1-x^2}}$$
   $$\frac{d}{dx}[\arctan x] = \frac{1}{1+x^2}$$

2. **Integrals**:
   $$\int \frac{1}{\sqrt{1-x^2}} dx = \arcsin x + C$$
   $$\int \frac{1}{1+x^2} dx = \arctan x + C$$

---

## Practice Problems

### Basic (Computational)

**Problem 1**
Find $\arcsin(0)$.

<details>
<summary>Show Solution</summary>

**Solution**:
What angle in $[-\frac{\pi}{2}, \frac{\pi}{2}]$ has sine equal to 0?

$\sin(0) = 0$

**Answer**: $\arcsin(0) = 0$
</details>

---

**Problem 2**
Find $\arccos(1)$.

<details>
<summary>Show Solution</summary>

**Solution**:
What angle in $[0, \pi]$ has cosine equal to 1?

$\cos(0) = 1$

**Answer**: $\arccos(1) = 0$
</details>

---

**Problem 3**
Find $\arctan(\sqrt{3})$.

<details>
<summary>Show Solution</summary>

**Solution**:
What angle in $(-\frac{\pi}{2}, \frac{\pi}{2})$ has tangent equal to $\sqrt{3}$?

$\tan\frac{\pi}{3} = \sqrt{3}$

**Answer**: $\arctan(\sqrt{3}) = \frac{\pi}{3}$
</details>

---

**Problem 4**
Find $\arcsin\left(\frac{1}{2}\right)$.

<details>
<summary>Show Solution</summary>

**Solution**:
$\sin\frac{\pi}{6} = \frac{1}{2}$

**Answer**: $\arcsin\left(\frac{1}{2}\right) = \frac{\pi}{6}$
</details>

---

**Problem 5**
Find $\arccos\left(\frac{\sqrt{3}}{2}\right)$.

<details>
<summary>Show Solution</summary>

**Solution**:
$\cos\frac{\pi}{6} = \frac{\sqrt{3}}{2}$

**Answer**: $\arccos\left(\frac{\sqrt{3}}{2}\right) = \frac{\pi}{6}$
</details>

---

### Intermediate (Multi-step)

**Problem 6**
Find $\arccos\left(-\frac{1}{2}\right)$.

<details>
<summary>Show Solution</summary>

**Solution**:
Reference angle: $\frac{\pi}{3}$ (since $\cos\frac{\pi}{3} = \frac{1}{2}$)

Arccosine range is $[0, \pi]$, and cosine is negative in Q2.

$\pi - \frac{\pi}{3} = \frac{2\pi}{3}$

**Answer**: $\arccos\left(-\frac{1}{2}\right) = \frac{2\pi}{3}$
</details>

---

**Problem 7**
Find $\sin(\arccos(\frac{4}{5}))$.

<details>
<summary>Show Solution</summary>

**Solution**:
Let $\theta = \arccos(\frac{4}{5})$, so $\cos\theta = \frac{4}{5}$ with $\theta \in [0, \pi]$

$\sin\theta = \sqrt{1 - \frac{16}{25}} = \sqrt{\frac{9}{25}} = \frac{3}{5}$

(Positive since $\theta \in [0, \pi]$)

**Answer**: $\sin(\arccos(\frac{4}{5})) = \frac{3}{5}$
</details>

---

**Problem 8**
Simplify $\arcsin(\sin(\frac{5\pi}{4}))$.

<details>
<summary>Show Solution</summary>

**Solution**:
First find $\sin(\frac{5\pi}{4})$:

$\frac{5\pi}{4}$ is in Q3, reference angle $\frac{\pi}{4}$

$\sin(\frac{5\pi}{4}) = -\frac{\sqrt{2}}{2}$

Now find $\arcsin(-\frac{\sqrt{2}}{2})$:

Arcsine range is $[-\frac{\pi}{2}, \frac{\pi}{2}]$, so answer is $-\frac{\pi}{4}$

**Answer**: $\arcsin(\sin(\frac{5\pi}{4})) = -\frac{\pi}{4}$
</details>

---

**Problem 9**
Find $\tan(\arcsin(\frac{5}{13}))$.

<details>
<summary>Show Solution</summary>

**Solution**:
Let $\theta = \arcsin(\frac{5}{13})$, so $\sin\theta = \frac{5}{13}$ with $\theta \in [-\frac{\pi}{2}, \frac{\pi}{2}]$

Find $\cos\theta$: $\cos\theta = \sqrt{1 - \frac{25}{169}} = \frac{12}{13}$ (positive in this range)

$\tan\theta = \frac{\sin\theta}{\cos\theta} = \frac{5/13}{12/13} = \frac{5}{12}$

**Answer**: $\tan(\arcsin(\frac{5}{13})) = \frac{5}{12}$
</details>

---

**Problem 10**
Find $\cos(\arctan(2))$.

<details>
<summary>Show Solution</summary>

**Solution**:
Let $\theta = \arctan(2)$, so $\tan\theta = 2 = \frac{2}{1}$

Draw a right triangle: opposite = 2, adjacent = 1, hypotenuse = $\sqrt{5}$

$\cos\theta = \frac{1}{\sqrt{5}} = \frac{\sqrt{5}}{5}$

**Answer**: $\cos(\arctan(2)) = \frac{\sqrt{5}}{5}$
</details>

---

### Advanced (Complex Applications)

**Problem 11**
Simplify $\arctan(x) + \arctan(\frac{1}{x})$ for $x > 0$.

<details>
<summary>Show Solution</summary>

**Solution**:
Let $\alpha = \arctan(x)$ and $\beta = \arctan(\frac{1}{x})$

Then $\tan\alpha = x$ and $\tan\beta = \frac{1}{x}$

Note that $\tan\alpha \cdot \tan\beta = x \cdot \frac{1}{x} = 1$

This means $\alpha + \beta = \frac{\pi}{2}$ (since $\tan(\frac{\pi}{2} - \alpha) = \cot\alpha = \frac{1}{\tan\alpha}$)

**Answer**: $\arctan(x) + \arctan(\frac{1}{x}) = \frac{\pi}{2}$ for $x > 0$
</details>

---

**Problem 12**
Express $\sin(2\arcsin(x))$ in terms of $x$.

<details>
<summary>Show Solution</summary>

**Solution**:
Let $\theta = \arcsin(x)$, so $\sin\theta = x$

$\cos\theta = \sqrt{1 - x^2}$ (for $\theta \in [-\frac{\pi}{2}, \frac{\pi}{2}]$, cosine is non-negative)

$\sin(2\theta) = 2\sin\theta\cos\theta = 2x\sqrt{1 - x^2}$

**Answer**: $\sin(2\arcsin(x)) = 2x\sqrt{1 - x^2}$
</details>

---

**Problem 13**
Solve: $\arcsin(x) + \arccos(x) = \frac{\pi}{2}$

<details>
<summary>Show Solution</summary>

**Solution**:
This is actually an identity! It's true for all $x \in [-1, 1]$.

Let $\alpha = \arcsin(x)$, so $\sin\alpha = x$ with $\alpha \in [-\frac{\pi}{2}, \frac{\pi}{2}]$

Then $\cos(\frac{\pi}{2} - \alpha) = \sin\alpha = x$

So $\arccos(x) = \frac{\pi}{2} - \alpha = \frac{\pi}{2} - \arcsin(x)$

Therefore $\arcsin(x) + \arccos(x) = \frac{\pi}{2}$

**Answer**: All $x \in [-1, 1]$
</details>

---

**Problem 14**
Find all solutions: $\arctan(x) = \arctan(2) + \arctan(3)$

<details>
<summary>Show Solution</summary>

**Solution**:
Use the tangent addition formula:
$$\tan(\arctan 2 + \arctan 3) = \frac{2 + 3}{1 - 2 \cdot 3} = \frac{5}{-5} = -1$$

But $\arctan(2) + \arctan(3) > \frac{\pi}{2}$ (both are positive and their sum exceeds $\frac{\pi}{2}$)

So we're in Q2 relative to the tangent's period, giving us:
$\arctan(2) + \arctan(3) = \pi + \arctan(-1) = \pi - \frac{\pi}{4} = \frac{3\pi}{4}$

But arctan's range is $(-\frac{\pi}{2}, \frac{\pi}{2})$, so this has no solution in standard range.

Actually, if we're just looking at the equation, $x = -1$ would make $\arctan(x) = -\frac{\pi}{4}$, which doesn't equal $\frac{3\pi}{4}$.

**No solution in the principal range**
</details>

---

**Problem 15**
Express $\cos(\arcsin(x) + \arccos(x))$ as a single value.

<details>
<summary>Show Solution</summary>

**Solution**:
Since $\arcsin(x) + \arccos(x) = \frac{\pi}{2}$:

$\cos(\arcsin(x) + \arccos(x)) = \cos\frac{\pi}{2} = 0$

**Answer**: $0$
</details>

---

### AP Exam Style

**Problem 16**
What is the domain of $f(x) = \arcsin(2x - 1)$?

<details>
<summary>Show Solution</summary>

**Solution**:
Arcsine requires $-1 \le 2x - 1 \le 1$

$0 \le 2x \le 2$

$0 \le x \le 1$

**Domain**: $[0, 1]$
</details>

---

**Problem 17**
Evaluate $\cos(\arcsin(\frac{3}{5}) + \arccos(\frac{5}{13}))$.

<details>
<summary>Show Solution</summary>

**Solution**:
Let $\alpha = \arcsin(\frac{3}{5})$ and $\beta = \arccos(\frac{5}{13})$

From $\alpha$: $\sin\alpha = \frac{3}{5}$, $\cos\alpha = \frac{4}{5}$

From $\beta$: $\cos\beta = \frac{5}{13}$, $\sin\beta = \frac{12}{13}$

$\cos(\alpha + \beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta$
$= \frac{4}{5} \cdot \frac{5}{13} - \frac{3}{5} \cdot \frac{12}{13}$
$= \frac{20}{65} - \frac{36}{65} = -\frac{16}{65}$

**Answer**: $-\frac{16}{65}$
</details>

---

**Problem 18**
If $\theta = \arctan(-2)$, which quadrant contains the angle $\theta$?

<details>
<summary>Show Solution</summary>

**Solution**:
Arctangent range is $(-\frac{\pi}{2}, \frac{\pi}{2})$

Since $-2 < 0$, we need the angle where tangent is negative in this range.

That's Quadrant IV (where $-\frac{\pi}{2} < \theta < 0$).

**Answer**: Quadrant IV
</details>

---

**Problem 19** *(Free Response Style)*
Let $f(x) = \arcsin(x) + \arcsin(\sqrt{1-x^2})$ for $0 \le x \le 1$.

(a) Find $f(0)$ and $f(1)$.
(b) Show that $f(x) = \frac{\pi}{2}$ for all $x$ in the domain.
(c) Explain geometrically why this identity holds.

<details>
<summary>Show Solution</summary>

**Solution**:

**(a)**
$f(0) = \arcsin(0) + \arcsin(1) = 0 + \frac{\pi}{2} = \frac{\pi}{2}$

$f(1) = \arcsin(1) + \arcsin(0) = \frac{\pi}{2} + 0 = \frac{\pi}{2}$

**(b)** Let $\theta = \arcsin(x)$, so $\sin\theta = x$ and $\cos\theta = \sqrt{1-x^2}$ (for $\theta \in [0, \frac{\pi}{2}]$)

Then $\arcsin(\sqrt{1-x^2}) = \arcsin(\cos\theta) = \frac{\pi}{2} - \theta$

(Using the cofunction identity: $\sin(\frac{\pi}{2} - \theta) = \cos\theta$)

So $f(x) = \theta + (\frac{\pi}{2} - \theta) = \frac{\pi}{2}$

**(c)** If $\theta$ is an angle in a right triangle with hypotenuse 1, then:
- $\sin\theta = x$ (opposite/hypotenuse)
- $\cos\theta = \sqrt{1-x^2}$ (adjacent/hypotenuse)

The other acute angle is $\frac{\pi}{2} - \theta$, and its sine equals $\cos\theta = \sqrt{1-x^2}$.

So the sum of the two arcsines gives the sum of the two acute angles: $\theta + (\frac{\pi}{2} - \theta) = \frac{\pi}{2}$.
</details>

---

**Problem 20** *(Free Response Style)*
(a) State the domain and range of $y = 2\arctan(x - 1) + \pi$.

(b) Find any intercepts.

(c) Find any horizontal asymptotes.

(d) Sketch the graph.

<details>
<summary>Show Solution</summary>

**Solution**:

**(a)**
Base function $\arctan(x)$: domain $\mathbb{R}$, range $(-\frac{\pi}{2}, \frac{\pi}{2})$

$\arctan(x - 1)$: horizontal shift, same domain/range

$2\arctan(x - 1)$: range becomes $(-\pi, \pi)$

$2\arctan(x - 1) + \pi$: range becomes $(0, 2\pi)$

**Domain**: $(-\infty, \infty)$
**Range**: $(0, 2\pi)$

**(b)** y-intercept: Set $x = 0$:
$y = 2\arctan(-1) + \pi = 2(-\frac{\pi}{4}) + \pi = \frac{\pi}{2}$

y-intercept: $(0, \frac{\pi}{2})$

x-intercept: Set $y = 0$:
$2\arctan(x-1) + \pi = 0$
$\arctan(x-1) = -\frac{\pi}{2}$

This has no solution since $-\frac{\pi}{2}$ is outside the range of arctangent.

**No x-intercept**

**(c)** As $x \to \infty$: $\arctan(x-1) \to \frac{\pi}{2}$, so $y \to 2(\frac{\pi}{2}) + \pi = 2\pi$

As $x \to -\infty$: $\arctan(x-1) \to -\frac{\pi}{2}$, so $y \to 2(-\frac{\pi}{2}) + \pi = 0$

**Horizontal asymptotes**: $y = 0$ and $y = 2\pi$

**(d)** The graph is an S-curve:
- Centered at $(1, \pi)$
- Increases from asymptote $y = 0$ to asymptote $y = 2\pi$
- Passes through $(0, \frac{\pi}{2})$ and $(2, \frac{3\pi}{2})$
</details>

---

## What's Next

Now that you've mastered inverse trig functions, you're ready to explore [Exponential Functions](/calculus/0111-exponential-functions), where we'll study functions that model growth and decay—essential for calculus applications.

---

<div align="center">

[← Trig Identities](/calculus/0109-trig-identities) | [Exponential Functions →](/calculus/0111-exponential-functions)

</div>
