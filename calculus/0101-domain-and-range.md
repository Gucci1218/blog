# Domain and Range
<p class="article-date">June 20, 2024</p>

## Prerequisites
Before diving in, make sure you're comfortable with:
- Basic algebra (solving equations and inequalities)
- Familiarity with common function types (linear, quadratic, rational, radical)

## Learning Objectives
By the end of this section, you will be able to:
- Define domain and range in your own words
- Find the domain of polynomial, rational, radical, and composite functions
- Determine the range from a graph or equation
- Express domain and range using interval notation
- Identify restrictions that limit domain or range

## The Big Picture: What Are Domain and Range?

Think of a function as a machine: you feed it an input, it processes it, and spits out an output.

- **Domain**: All the possible inputs (x-values) the function can accept
- **Range**: All the possible outputs (y-values) the function can produce

> **Intuition**: Domain asks "What can I put in?" and Range asks "What can come out?"

### Why Does This Matter for Calculus?

In calculus, you'll need to:
- Find limits only where the function is defined (domain)
- Integrate only over valid intervals (domain)
- Determine where derivatives exist (domain)
- Analyze function behavior (range helps understand bounds)

## Interval Notation: The Language of Domain and Range

Before finding domains, let's master how to write them:

| Notation | Meaning | Example |
|----------|---------|---------|
| $(a, b)$ | All numbers between $a$ and $b$, excluding endpoints | $(2, 5)$ means $2 < x < 5$ |
| $[a, b]$ | All numbers between $a$ and $b$, including endpoints | $[2, 5]$ means $2 \le x \le 5$ |
| $[a, b)$ | Include $a$, exclude $b$ | $[2, 5)$ means $2 \le x < 5$ |
| $(a, b]$ | Exclude $a$, include $b$ | $(2, 5]$ means $2 < x \le 5$ |
| $(-\infty, a)$ | All numbers less than $a$ | $(-\infty, 3)$ means $x < 3$ |
| $(a, \infty)$ | All numbers greater than $a$ | $(3, \infty)$ means $x > 3$ |
| $(-\infty, \infty)$ | All real numbers | The entire number line |

**Key Rule**: Always use parentheses ( ) with infinity symbols, never brackets [ ].

**Union Symbol**: Use $\cup$ to combine separate intervals.
- Example: $(-\infty, 2) \cup (2, \infty)$ means all real numbers except 2

## Finding Domain: The Three Main Restrictions

Most functions accept all real numbers as inputs. We only restrict the domain when something "breaks" mathematically. There are three common restrictions:

### Restriction 1: Division by Zero

**Rule**: The denominator of a fraction cannot equal zero.

**Example**: Find the domain of $f(x) = \dfrac{1}{x - 3}$

Set the denominator $\ne 0$:
$$x - 3 \ne 0 \implies x \ne 3$$

**Domain**: $(-\infty, 3) \cup (3, \infty)$ or "all real numbers except 3"

### Restriction 2: Even Roots of Negative Numbers

**Rule**: You cannot take the square root (or any even root) of a negative number (in real numbers).

**Example**: Find the domain of $g(x) = \sqrt{x - 4}$

Set the radicand $\ge 0$:
$$x - 4 \ge 0 \implies x \ge 4$$

**Domain**: $[4, \infty)$

### Restriction 3: Logarithms of Non-Positive Numbers

**Rule**: You can only take the logarithm of positive numbers.

**Example**: Find the domain of $h(x) = \ln(2x + 6)$

Set the argument $> 0$:
$$2x + 6 > 0 \implies x > -3$$

**Domain**: $(-3, \infty)$

## Worked Example 1: Rational Function

**Problem**: Find the domain of $f(x) = \dfrac{x + 2}{x^2 - 9}$

**Solution**:

**Step 1**: Identify the restriction. This is a fraction, so we need denominator $\ne 0$.

**Step 2**: Factor and solve.
$$x^2 - 9 = 0$$
$$(x-3)(x+3) = 0$$
$$x = 3 \text{ or } x = -3$$

**Step 3**: Exclude these values.

**Domain**: $(-\infty, -3) \cup (-3, 3) \cup (3, \infty)$

## Worked Example 2: Radical Function

**Problem**: Find the domain of $g(x) = \sqrt{6 - 2x}$

**Solution**:

**Step 1**: Set the radicand $\ge 0$.
$$6 - 2x \ge 0$$

**Step 2**: Solve the inequality.
$$6 \ge 2x$$
$$3 \ge x$$
$$x \le 3$$

**Domain**: $(-\infty, 3]$

## Worked Example 3: Combined Restrictions

**Problem**: Find the domain of $h(x) = \dfrac{\sqrt{x + 1}}{x - 4}$

**Solution**:

This function has TWO restrictions:
1. Square root: $x + 1 \ge 0 \implies x \ge -1$
2. Denominator: $x - 4 \ne 0 \implies x \ne 4$

**Step 1**: Apply the square root restriction: $x \ge -1$, so we start at $[-1, \infty)$

**Step 2**: Remove where denominator = 0: exclude $x = 4$

**Domain**: $[-1, 4) \cup (4, \infty)$

## Worked Example 4: Polynomial Functions

**Problem**: Find the domain of $p(x) = 3x^4 - 2x^2 + 7x - 1$

**Solution**:

Polynomials have NO restrictions. You can plug in any real number.

**Domain**: $(-\infty, \infty)$ or "all real numbers"

## Finding Range

Range is trickier than domain. Here are the main strategies:

### Strategy 1: Graph Analysis

Look at the graph and identify the lowest and highest y-values the function reaches.

**Example**: $f(x) = x^2$
- The parabola opens upward with vertex at $(0, 0)$
- Lowest point: $y = 0$
- Goes up forever
- **Range**: $[0, \infty)$

### Strategy 2: Inverse Function Approach

If you can find the inverse, the domain of the inverse equals the range of the original.

### Strategy 3: Analyze Function Behavior

For common functions, use what you know about their behavior.

| Function Type | Range |
|---------------|-------|
| $f(x) = x^2$ | $[0, \infty)$ |
| $f(x) = x^3$ | $(-\infty, \infty)$ |
| $f(x) = \|x\|$ | $[0, \infty)$ |
| $f(x) = \sqrt{x}$ | $[0, \infty)$ |
| $f(x) = e^x$ | $(0, \infty)$ |
| $f(x) = \ln(x)$ | $(-\infty, \infty)$ |
| $f(x) = \sin(x)$ | $[-1, 1]$ |
| $f(x) = \cos(x)$ | $[-1, 1]$ |

## Worked Example 5: Finding Range

**Problem**: Find the range of $f(x) = \sqrt{x - 2} + 3$

**Solution**:

**Step 1**: Start with the basic function $\sqrt{x}$ which has range $[0, \infty)$

**Step 2**: The transformation $\sqrt{x-2}$ shifts right (doesn't affect range): still $[0, \infty)$

**Step 3**: Adding 3 shifts everything up by 3:
$$[0, \infty) + 3 = [3, \infty)$$

**Range**: $[3, \infty)$

## Worked Example 6: Range of a Rational Function

**Problem**: Find the range of $g(x) = \dfrac{2}{x - 1} + 4$

**Solution**:

**Step 1**: The basic function $\dfrac{1}{x}$ has range $(-\infty, 0) \cup (0, \infty)$ (all reals except 0)

**Step 2**: $\dfrac{2}{x-1}$ stretches and shifts horizontally, but the range is still $(-\infty, 0) \cup (0, \infty)$

**Step 3**: Adding 4 shifts the range up by 4:
$$(-\infty, 0) \cup (0, \infty) + 4 = (-\infty, 4) \cup (4, \infty)$$

**Range**: $(-\infty, 4) \cup (4, \infty)$ or "all real numbers except 4"

## Key Formulas and Rules

| Function Type | Domain Restriction | How to Find Domain |
|---------------|-------------------|-------------------|
| Polynomial | None | $(-\infty, \infty)$ |
| Rational $\frac{p(x)}{q(x)}$ | $q(x) \ne 0$ | Solve $q(x) = 0$, exclude those values |
| Square root $\sqrt{f(x)}$ | $f(x) \ge 0$ | Solve $f(x) \ge 0$ |
| Logarithm $\log(f(x))$ | $f(x) > 0$ | Solve $f(x) > 0$ |
| Combination | Apply all restrictions | Find intersection of all conditions |

## Common Mistakes to Avoid

1. **Using brackets with infinity**
   - Wrong: $[3, \infty]$
   - Correct: $[3, \infty)$

2. **Forgetting to factor denominators completely**
   - $\frac{1}{x^2 - 4}$ has TWO excluded values: $x = 2$ and $x = -2$

3. **Using wrong inequality for square roots**
   - Square roots need $\ge 0$, not $> 0$
   - $\sqrt{0} = 0$ is perfectly valid!

4. **Confusing domain and range**
   - Domain = x-values (horizontal)
   - Range = y-values (vertical)

5. **Forgetting that odd roots accept all real numbers**
   - $\sqrt[3]{x}$ has domain $(-\infty, \infty)$
   - Only EVEN roots ($\sqrt{x}, \sqrt[4]{x}$, etc.) have restrictions

## Calculus Connection

Understanding domain is essential for calculus because:

1. **Limits**: $\lim_{x \to a} f(x)$ only makes sense if $a$ is in or near the domain
2. **Derivatives**: $f'(x)$ exists only where $f(x)$ is defined (and more)
3. **Integrals**: $\int_a^b f(x) \, dx$ requires $f$ to be defined on $[a, b]$
4. **Continuity**: A function can only be continuous on its domain

---

## Practice Problems

### Basic (Computational)

**Problem 1**
Find the domain of $f(x) = \dfrac{5}{x + 7}$

<details>
<summary>Show Solution</summary>

**Solution**:
Set denominator $\ne 0$:
$$x + 7 \ne 0 \implies x \ne -7$$

**Domain**: $(-\infty, -7) \cup (-7, \infty)$
</details>

---

**Problem 2**
Find the domain of $g(x) = \sqrt{x + 5}$

<details>
<summary>Show Solution</summary>

**Solution**:
Set radicand $\ge 0$:
$$x + 5 \ge 0 \implies x \ge -5$$

**Domain**: $[-5, \infty)$
</details>

---

**Problem 3**
Find the domain of $h(x) = x^3 - 4x^2 + 2x - 9$

<details>
<summary>Show Solution</summary>

**Solution**:
This is a polynomial. Polynomials have no restrictions.

**Domain**: $(-\infty, \infty)$
</details>

---

**Problem 4**
Find the domain of $f(x) = \ln(x - 2)$

<details>
<summary>Show Solution</summary>

**Solution**:
Set argument $> 0$:
$$x - 2 > 0 \implies x > 2$$

**Domain**: $(2, \infty)$
</details>

---

**Problem 5**
Find the range of $f(x) = x^2 + 4$

<details>
<summary>Show Solution</summary>

**Solution**:
The basic function $x^2$ has range $[0, \infty)$.

Adding 4 shifts the range up by 4:
$$[0, \infty) + 4 = [4, \infty)$$

**Range**: $[4, \infty)$
</details>

---

### Intermediate (Multi-step)

**Problem 6**
Find the domain of $f(x) = \dfrac{x - 1}{x^2 - 5x + 6}$

<details>
<summary>Show Solution</summary>

**Solution**:
Factor the denominator:
$$x^2 - 5x + 6 = (x - 2)(x - 3)$$

Set denominator $\ne 0$:
$$(x - 2)(x - 3) \ne 0$$
$$x \ne 2 \text{ and } x \ne 3$$

**Domain**: $(-\infty, 2) \cup (2, 3) \cup (3, \infty)$
</details>

---

**Problem 7**
Find the domain of $g(x) = \sqrt{9 - x^2}$

<details>
<summary>Show Solution</summary>

**Solution**:
Set radicand $\ge 0$:
$$9 - x^2 \ge 0$$
$$9 \ge x^2$$
$$-3 \le x \le 3$$

**Domain**: $[-3, 3]$
</details>

---

**Problem 8**
Find the domain of $h(x) = \dfrac{\sqrt{x}}{x - 4}$

<details>
<summary>Show Solution</summary>

**Solution**:
Two restrictions:
1. Square root: $x \ge 0$
2. Denominator: $x \ne 4$

Combining: $x \ge 0$ AND $x \ne 4$

**Domain**: $[0, 4) \cup (4, \infty)$
</details>

---

**Problem 9**
Find the domain of $f(x) = \ln(x^2 - 4)$

<details>
<summary>Show Solution</summary>

**Solution**:
Set argument $> 0$:
$$x^2 - 4 > 0$$
$$(x-2)(x+2) > 0$$

Sign analysis: positive when $x < -2$ or $x > 2$

**Domain**: $(-\infty, -2) \cup (2, \infty)$
</details>

---

**Problem 10**
Find the range of $f(x) = -2(x - 3)^2 + 5$

<details>
<summary>Show Solution</summary>

**Solution**:
This is a downward-opening parabola in vertex form.

Vertex: $(3, 5)$ — this is the maximum point.

Since the parabola opens downward, y-values go from $-\infty$ up to 5.

**Range**: $(-\infty, 5]$
</details>

---

### Advanced (Complex Applications)

**Problem 11**
Find the domain of $f(x) = \dfrac{\sqrt{x + 3}}{x^2 - x - 6}$

<details>
<summary>Show Solution</summary>

**Solution**:
Two restrictions:

1. Square root: $x + 3 \ge 0 \implies x \ge -3$

2. Denominator: $x^2 - x - 6 \ne 0$
   $$(x - 3)(x + 2) \ne 0$$
   $$x \ne 3 \text{ and } x \ne -2$$

Combining: Start with $[-3, \infty)$, then remove $x = -2$ and $x = 3$

**Domain**: $[-3, -2) \cup (-2, 3) \cup (3, \infty)$
</details>

---

**Problem 12**
Find the domain of $g(x) = \sqrt{x - 1} + \sqrt{5 - x}$

<details>
<summary>Show Solution</summary>

**Solution**:
Two square root restrictions (both must be satisfied):

1. $x - 1 \ge 0 \implies x \ge 1$
2. $5 - x \ge 0 \implies x \le 5$

Combining: $1 \le x \le 5$

**Domain**: $[1, 5]$
</details>

---

**Problem 13**
Find the domain of $h(x) = \log_2(x - 1) + \dfrac{1}{x - 3}$

<details>
<summary>Show Solution</summary>

**Solution**:
Two restrictions:

1. Logarithm: $x - 1 > 0 \implies x > 1$
2. Denominator: $x - 3 \ne 0 \implies x \ne 3$

Combining: $x > 1$ AND $x \ne 3$

**Domain**: $(1, 3) \cup (3, \infty)$
</details>

---

**Problem 14**
Find the domain and range of $f(x) = \sqrt{4 - x^2}$

<details>
<summary>Show Solution</summary>

**Solution**:

**Domain**:
$$4 - x^2 \ge 0 \implies x^2 \le 4 \implies -2 \le x \le 2$$
Domain: $[-2, 2]$

**Range**:
This is the top half of a circle with radius 2.
- Minimum value: $f(\pm 2) = \sqrt{0} = 0$
- Maximum value: $f(0) = \sqrt{4} = 2$

Range: $[0, 2]$
</details>

---

**Problem 15**
Find the domain of $f(x) = \dfrac{1}{\sqrt{x^2 - 9}}$

<details>
<summary>Show Solution</summary>

**Solution**:
Two restrictions:

1. Square root (radicand $\ge 0$): $x^2 - 9 \ge 0$
2. Denominator $\ne 0$: $\sqrt{x^2 - 9} \ne 0 \implies x^2 - 9 \ne 0$

Combined: $x^2 - 9 > 0$ (strict inequality)

$$(x-3)(x+3) > 0$$

This is positive when $x < -3$ or $x > 3$.

**Domain**: $(-\infty, -3) \cup (3, \infty)$
</details>

---

### AP Exam Style

**Problem 16**
The function $f$ is defined by $f(x) = \dfrac{\sqrt{2x - 4}}{x - 5}$. What is the domain of $f$?

(A) $x \ge 2$
(B) $x \ge 2, x \ne 5$
(C) $x > 2$
(D) $[2, 5) \cup (5, \infty)$

<details>
<summary>Show Solution</summary>

**Solution**:

Square root: $2x - 4 \ge 0 \implies x \ge 2$

Denominator: $x \ne 5$

Combined: $x \ge 2$ and $x \ne 5$

In interval notation: $[2, 5) \cup (5, \infty)$

**Answer: (D)**

Note: (B) is also correct as an inequality statement, but (D) is the proper interval notation form.
</details>

---

**Problem 17**
If $g(x) = \ln(9 - x^2)$, for which values of $x$ is $g(x)$ defined?

<details>
<summary>Show Solution</summary>

**Solution**:
Need $9 - x^2 > 0$:
$$x^2 < 9$$
$$-3 < x < 3$$

**Domain**: $(-3, 3)$
</details>

---

**Problem 18**
The range of the function $f(x) = 3 - \sqrt{x + 1}$ is:

(A) $(-\infty, 3]$
(B) $[3, \infty)$
(C) $(-\infty, 3)$
(D) $(3, \infty)$

<details>
<summary>Show Solution</summary>

**Solution**:
Start with $\sqrt{x+1}$ which has range $[0, \infty)$.

Then $-\sqrt{x+1}$ has range $(-\infty, 0]$.

Then $3 - \sqrt{x+1}$ shifts up by 3: $(-\infty, 3]$.

The maximum value is 3 (when $x = -1$), and values decrease from there.

**Answer: (A)**
</details>

---

**Problem 19** *(Free Response Style)*
Let $f(x) = \dfrac{x + 2}{x^2 - 4}$.

(a) Find the domain of $f$.
(b) Simplify $f(x)$ and state any restrictions.
(c) Explain why the domain of the simplified form differs from the original.

<details>
<summary>Show Solution</summary>

**Solution**:

**(a)** Factor denominator: $x^2 - 4 = (x-2)(x+2)$

Set $\ne 0$: $x \ne 2$ and $x \ne -2$

**Domain**: $(-\infty, -2) \cup (-2, 2) \cup (2, \infty)$

**(b)**
$$f(x) = \frac{x + 2}{(x-2)(x+2)} = \frac{1}{x - 2}$$

with restriction $x \ne -2$ (and $x \ne 2$ from simplified form)

**(c)** The simplified form $\frac{1}{x-2}$ appears to have domain $(-\infty, 2) \cup (2, \infty)$, which would include $x = -2$.

However, the original function is undefined at $x = -2$ (division by zero), so we must maintain this restriction. The two forms are equal only where both are defined.

This creates a "hole" in the graph at $x = -2$.
</details>

---

**Problem 20** *(Free Response Style)*
A function is defined as $h(x) = \sqrt{a - x}$ where $a$ is a constant.

(a) If the domain of $h$ is $(-\infty, 7]$, find the value of $a$.
(b) What is the range of $h$ with this value of $a$?
(c) Find a formula for $h^{-1}(x)$ and state its domain.

<details>
<summary>Show Solution</summary>

**Solution**:

**(a)** For $\sqrt{a - x}$, we need $a - x \ge 0$, so $x \le a$.

The domain is $(-\infty, a]$.

Given domain is $(-\infty, 7]$, so $a = 7$.

**(b)** With $h(x) = \sqrt{7 - x}$:

$\sqrt{7-x}$ takes on all values $\ge 0$ (as $x$ ranges over $(-\infty, 7]$)

**Range**: $[0, \infty)$

**(c)** To find inverse:
$$y = \sqrt{7 - x}$$
$$y^2 = 7 - x$$
$$x = 7 - y^2$$

So $h^{-1}(x) = 7 - x^2$

Domain of $h^{-1}$ = Range of $h$ = $[0, \infty)$

**Answer**: $h^{-1}(x) = 7 - x^2$ with domain $[0, \infty)$
</details>

---

## What's Next

Now that you understand domain and range, you're ready to explore [Composite Functions](/calculus/0102-composite-functions), where we'll combine functions by plugging one into another—a skill essential for the Chain Rule in calculus.

---

<div align="center">

[← History of Calculus](/calculus/0002-history-of-calculus) | [Composite Functions →](/calculus/0102-composite-functions)

</div>
