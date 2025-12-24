# Solving Equations and Inequalities
<p class="article-date">July 11, 2024</p>

## Prerequisites
Before diving in, make sure you're comfortable with:
- [Factoring Techniques](/calculus/0105-factoring-techniques)
- Basic algebraic manipulation
- Properties of equality and inequality

## Learning Objectives
By the end of this section, you will be able to:
- Solve linear, quadratic, polynomial, rational, and radical equations
- Solve linear and polynomial inequalities
- Use sign charts for rational inequalities
- Handle absolute value equations and inequalities
- Verify solutions and identify extraneous solutions

## The Big Picture: Finding Where Equations Balance

Solving an equation means finding all values of the variable that make the equation true. In calculus, you'll solve equations constantly:
- Setting derivatives equal to zero to find critical points
- Finding where a function crosses the x-axis
- Solving differential equations

## Linear Equations

### Standard Form
$$ax + b = c$$

### Solution Method
Isolate $x$ by performing inverse operations:
$$x = \frac{c - b}{a}$$

### Example
Solve $3x - 7 = 14$

$$3x = 21$$
$$x = 7$$

## Quadratic Equations

### Three Methods

| Method | When to Use |
|--------|-------------|
| Factoring | When factors are obvious |
| Quadratic Formula | Always works |
| Completing the Square | For vertex form or derivations |

### Method 1: Factoring

**Example**: Solve $x^2 - 5x + 6 = 0$

Factor: $(x - 2)(x - 3) = 0$

Zero Product Property: $x = 2$ or $x = 3$

### Method 2: Quadratic Formula

For $ax^2 + bx + c = 0$:
$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

**Example**: Solve $2x^2 + 3x - 5 = 0$

$$x = \frac{-3 \pm \sqrt{9 + 40}}{4} = \frac{-3 \pm 7}{4}$$

$$x = 1 \text{ or } x = -\frac{5}{2}$$

### The Discriminant

The expression $b^2 - 4ac$ tells us about the solutions:

| Discriminant | Number of Real Solutions |
|--------------|--------------------------|
| $> 0$ | Two distinct real solutions |
| $= 0$ | One repeated real solution |
| $< 0$ | No real solutions (two complex) |

### Method 3: Completing the Square

**Example**: Solve $x^2 + 6x + 2 = 0$

$$x^2 + 6x = -2$$
$$x^2 + 6x + 9 = -2 + 9$$
$$(x + 3)^2 = 7$$
$$x + 3 = \pm\sqrt{7}$$
$$x = -3 \pm \sqrt{7}$$

## Polynomial Equations (Higher Degree)

### Strategy
1. Set equal to zero
2. Factor completely
3. Apply Zero Product Property

### Example
Solve $x^3 - 4x^2 - 7x + 10 = 0$

From factoring (previous section):
$$x^3 - 4x^2 - 7x + 10 = (x - 1)(x - 5)(x + 2) = 0$$

Solutions: $x = 1$, $x = 5$, $x = -2$

### The Rational Root Theorem

For $a_nx^n + ... + a_1x + a_0 = 0$, possible rational roots are:
$$\pm \frac{\text{factors of } a_0}{\text{factors of } a_n}$$

**Example**: Find possible rational roots of $2x^3 - 5x^2 + x + 2 = 0$

- Factors of 2 (constant): $\pm 1, \pm 2$
- Factors of 2 (leading): $\pm 1, \pm 2$
- Possible roots: $\pm 1, \pm 2, \pm \frac{1}{2}$

Test each to find actual roots.

## Rational Equations

### Strategy
1. Find the LCD of all fractions
2. Multiply both sides by the LCD
3. Solve the resulting equation
4. **Check for extraneous solutions** (values that make original denominators zero)

### Example
Solve $\dfrac{2}{x} + \dfrac{3}{x+1} = 1$

**Step 1**: LCD = $x(x + 1)$

**Step 2**: Multiply both sides:
$$2(x + 1) + 3x = x(x + 1)$$
$$2x + 2 + 3x = x^2 + x$$
$$5x + 2 = x^2 + x$$
$$0 = x^2 - 4x - 2$$

**Step 3**: Quadratic formula:
$$x = \frac{4 \pm \sqrt{16 + 8}}{2} = \frac{4 \pm \sqrt{24}}{2} = 2 \pm \sqrt{6}$$

**Step 4**: Check: Neither value makes a denominator zero ✓

Solutions: $x = 2 + \sqrt{6}$ and $x = 2 - \sqrt{6}$

## Radical Equations

### Strategy
1. Isolate the radical
2. Raise both sides to the appropriate power
3. Solve the resulting equation
4. **Check all solutions** (squaring can introduce extraneous solutions)

### Example
Solve $\sqrt{x + 3} = x - 1$

**Step 1**: Square both sides:
$$x + 3 = (x - 1)^2 = x^2 - 2x + 1$$

**Step 2**: Rearrange:
$$x + 3 = x^2 - 2x + 1$$
$$0 = x^2 - 3x - 2$$

**Step 3**: Quadratic formula:
$$x = \frac{3 \pm \sqrt{9 + 8}}{2} = \frac{3 \pm \sqrt{17}}{2}$$

**Step 4**: Check both solutions in original:

For $x = \frac{3 + \sqrt{17}}{2} \approx 3.56$:
- LHS: $\sqrt{3.56 + 3} \approx 2.56$
- RHS: $3.56 - 1 = 2.56$ ✓

For $x = \frac{3 - \sqrt{17}}{2} \approx -0.56$:
- LHS: $\sqrt{-0.56 + 3} \approx 1.56$
- RHS: $-0.56 - 1 = -1.56$ ✗ (not equal!)

**Only solution**: $x = \frac{3 + \sqrt{17}}{2}$

## Absolute Value Equations

### Definition
$$|a| = \begin{cases} a & \text{if } a \ge 0 \\ -a & \text{if } a < 0 \end{cases}$$

### Solving $|f(x)| = k$ (where $k > 0$)

$$f(x) = k \quad \text{OR} \quad f(x) = -k$$

### Example
Solve $|2x - 5| = 7$

Case 1: $2x - 5 = 7 \implies x = 6$

Case 2: $2x - 5 = -7 \implies x = -1$

Solutions: $x = 6$ and $x = -1$

### Special Cases
- $|f(x)| = 0$: Only solution is $f(x) = 0$
- $|f(x)| = k$ where $k < 0$: No solution

## Linear Inequalities

### Rules
- Add/subtract: inequality direction unchanged
- Multiply/divide by positive: direction unchanged
- **Multiply/divide by negative: REVERSE the inequality**

### Example
Solve $3x - 7 > 2x + 5$

$$x > 12$$

Solution: $(12, \infty)$

### Example with Reversal
Solve $-2x + 4 \le 10$

$$-2x \le 6$$
$$x \ge -3$$ (reversed!)

Solution: $[-3, \infty)$

## Polynomial Inequalities

### Strategy (Sign Chart Method)
1. Get zero on one side
2. Factor completely
3. Find zeros (critical values)
4. Create a sign chart
5. Determine intervals that satisfy the inequality

### Example
Solve $x^2 - 4x - 5 > 0$

**Step 1**: Factor: $(x - 5)(x + 1) > 0$

**Step 2**: Critical values: $x = 5$ and $x = -1$

**Step 3**: Sign chart:

| Interval | $(x - 5)$ | $(x + 1)$ | Product |
|----------|-----------|-----------|---------|
| $x < -1$ | $-$ | $-$ | $+$ |
| $-1 < x < 5$ | $-$ | $+$ | $-$ |
| $x > 5$ | $+$ | $+$ | $+$ |

**Step 4**: We want $> 0$ (positive), so:

Solution: $(-\infty, -1) \cup (5, \infty)$

## Rational Inequalities

### Strategy
1. Get zero on one side
2. Combine into a single fraction
3. Factor numerator and denominator
4. Find all zeros (numerator) and undefined points (denominator)
5. Create sign chart
6. Determine solution intervals

### Example
Solve $\dfrac{x - 2}{x + 3} \le 0$

**Critical values**:
- Numerator = 0: $x = 2$
- Denominator = 0: $x = -3$ (undefined, not included)

**Sign chart**:

| Interval | $(x - 2)$ | $(x + 3)$ | Quotient |
|----------|-----------|-----------|----------|
| $x < -3$ | $-$ | $-$ | $+$ |
| $-3 < x < 2$ | $-$ | $+$ | $-$ |
| $x > 2$ | $+$ | $+$ | $+$ |

We want $\le 0$ (negative or zero):
- Include $x = 2$ (makes expression = 0) ✓
- Exclude $x = -3$ (undefined) ✗

Solution: $(-3, 2]$

## Absolute Value Inequalities

### Two Types

**Type 1: $|f(x)| < k$** (less than)
$$-k < f(x) < k$$

**Type 2: $|f(x)| > k$** (greater than)
$$f(x) < -k \quad \text{OR} \quad f(x) > k$$

> **Memory Aid**:
> - Less than = "AND" (between)
> - Greater than = "OR" (outside)

### Example
Solve $|3x - 2| < 7$

$$-7 < 3x - 2 < 7$$
$$-5 < 3x < 9$$
$$-\frac{5}{3} < x < 3$$

Solution: $\left(-\frac{5}{3}, 3\right)$

### Example
Solve $|2x + 1| \ge 5$

$$2x + 1 \le -5 \quad \text{OR} \quad 2x + 1 \ge 5$$
$$x \le -3 \quad \text{OR} \quad x \ge 2$$

Solution: $(-\infty, -3] \cup [2, \infty)$

## Key Formulas Summary

| Equation Type | Method |
|---------------|--------|
| Linear | Isolate variable |
| Quadratic | Factor, formula, or complete the square |
| Polynomial | Factor, use Zero Product Property |
| Rational | Multiply by LCD, check for extraneous solutions |
| Radical | Isolate, raise to power, CHECK solutions |
| Absolute Value | Split into cases |

| Inequality Type | Method |
|-----------------|--------|
| Linear | Solve normally, reverse if multiply/divide by negative |
| Polynomial | Sign chart |
| Rational | Sign chart (exclude zeros of denominator) |
| Absolute Value | Split into compound inequality or union |

## Common Mistakes to Avoid

1. **Forgetting to check for extraneous solutions**
   - Always verify rational and radical equation solutions

2. **Not reversing inequality when multiplying by negative**
   - $-x > 3$ becomes $x < -3$

3. **Including undefined values in rational inequalities**
   - If denominator = 0, that point is NEVER in the solution

4. **Wrong inequality symbol with absolute value**
   - $|x| < 3$ means between: $-3 < x < 3$
   - $|x| > 3$ means outside: $x < -3$ or $x > 3$

5. **Distributing incorrectly when squaring**
   - $(x + 1)^2 = x^2 + 2x + 1$, NOT $x^2 + 1$

## Calculus Connection

Solving equations is fundamental to calculus:

1. **Critical Points**: Solve $f'(x) = 0$
2. **Inflection Points**: Solve $f''(x) = 0$
3. **Zeros of Functions**: Solve $f(x) = 0$
4. **Optimization**: Solve derivative equations
5. **Initial Value Problems**: Solve for constants

---

## Practice Problems

### Basic (Computational)

**Problem 1**
Solve: $5x - 3 = 2x + 9$

<details>
<summary>Show Solution</summary>

**Solution**:
$$3x = 12$$
$$x = 4$$
</details>

---

**Problem 2**
Solve: $x^2 - 9 = 0$

<details>
<summary>Show Solution</summary>

**Solution**:
$$(x + 3)(x - 3) = 0$$
$$x = -3 \text{ or } x = 3$$
</details>

---

**Problem 3**
Solve: $x^2 + 4x - 12 = 0$

<details>
<summary>Show Solution</summary>

**Solution**:
$$(x + 6)(x - 2) = 0$$
$$x = -6 \text{ or } x = 2$$
</details>

---

**Problem 4**
Solve: $|x - 4| = 7$

<details>
<summary>Show Solution</summary>

**Solution**:
Case 1: $x - 4 = 7 \implies x = 11$

Case 2: $x - 4 = -7 \implies x = -3$

Solutions: $x = 11$ and $x = -3$
</details>

---

**Problem 5**
Solve: $2x - 5 > 9$

<details>
<summary>Show Solution</summary>

**Solution**:
$$2x > 14$$
$$x > 7$$

Solution: $(7, \infty)$
</details>

---

### Intermediate (Multi-step)

**Problem 6**
Solve: $x^2 - 6x + 7 = 0$

<details>
<summary>Show Solution</summary>

**Solution**:
Using the quadratic formula:
$$x = \frac{6 \pm \sqrt{36 - 28}}{2} = \frac{6 \pm \sqrt{8}}{2} = \frac{6 \pm 2\sqrt{2}}{2} = 3 \pm \sqrt{2}$$

Solutions: $x = 3 + \sqrt{2}$ and $x = 3 - \sqrt{2}$
</details>

---

**Problem 7**
Solve: $\dfrac{x}{x-2} = \dfrac{4}{x-2} + 2$

<details>
<summary>Show Solution</summary>

**Solution**:
Multiply by $(x - 2)$:
$$x = 4 + 2(x - 2)$$
$$x = 4 + 2x - 4$$
$$x = 2x$$
$$0 = x$$

Check: $x = 0$ doesn't make denominator zero ✓

Solution: $x = 0$
</details>

---

**Problem 8**
Solve: $\sqrt{2x + 1} = x - 1$

<details>
<summary>Show Solution</summary>

**Solution**:
Square both sides:
$$2x + 1 = (x - 1)^2 = x^2 - 2x + 1$$
$$2x + 1 = x^2 - 2x + 1$$
$$4x = x^2$$
$$x^2 - 4x = 0$$
$$x(x - 4) = 0$$
$$x = 0 \text{ or } x = 4$$

Check $x = 0$: $\sqrt{1} = 1 \ne -1$ ✗

Check $x = 4$: $\sqrt{9} = 3 = 4 - 1$ ✓

Solution: $x = 4$
</details>

---

**Problem 9**
Solve: $x^2 - 2x - 8 < 0$

<details>
<summary>Show Solution</summary>

**Solution**:
Factor: $(x - 4)(x + 2) < 0$

Critical values: $x = -2$ and $x = 4$

Sign chart shows negative when $-2 < x < 4$

Solution: $(-2, 4)$
</details>

---

**Problem 10**
Solve: $|2x - 3| \le 5$

<details>
<summary>Show Solution</summary>

**Solution**:
$$-5 \le 2x - 3 \le 5$$
$$-2 \le 2x \le 8$$
$$-1 \le x \le 4$$

Solution: $[-1, 4]$
</details>

---

### Advanced (Complex Applications)

**Problem 11**
Solve: $x^3 - 2x^2 - 5x + 6 = 0$

<details>
<summary>Show Solution</summary>

**Solution**:
Try possible rational roots: $\pm 1, \pm 2, \pm 3, \pm 6$

$f(1) = 1 - 2 - 5 + 6 = 0$ ✓

So $(x - 1)$ is a factor. Divide:
$$x^3 - 2x^2 - 5x + 6 = (x - 1)(x^2 - x - 6) = (x - 1)(x - 3)(x + 2)$$

Solutions: $x = 1$, $x = 3$, $x = -2$
</details>

---

**Problem 12**
Solve: $\dfrac{x + 1}{x - 3} > 2$

<details>
<summary>Show Solution</summary>

**Solution**:
$$\frac{x + 1}{x - 3} - 2 > 0$$
$$\frac{x + 1 - 2(x - 3)}{x - 3} > 0$$
$$\frac{x + 1 - 2x + 6}{x - 3} > 0$$
$$\frac{-x + 7}{x - 3} > 0$$
$$\frac{7 - x}{x - 3} > 0$$

Critical values: $x = 7$ (numerator) and $x = 3$ (denominator)

Sign chart:

| Interval | $(7-x)$ | $(x-3)$ | Quotient |
|----------|---------|---------|----------|
| $x < 3$ | $+$ | $-$ | $-$ |
| $3 < x < 7$ | $+$ | $+$ | $+$ |
| $x > 7$ | $-$ | $+$ | $-$ |

Solution: $(3, 7)$
</details>

---

**Problem 13**
Solve: $\sqrt{x + 5} - \sqrt{x - 3} = 2$

<details>
<summary>Show Solution</summary>

**Solution**:
Isolate one radical:
$$\sqrt{x + 5} = 2 + \sqrt{x - 3}$$

Square:
$$x + 5 = 4 + 4\sqrt{x - 3} + (x - 3)$$
$$x + 5 = x + 1 + 4\sqrt{x - 3}$$
$$4 = 4\sqrt{x - 3}$$
$$1 = \sqrt{x - 3}$$
$$1 = x - 3$$
$$x = 4$$

Check: $\sqrt{9} - \sqrt{1} = 3 - 1 = 2$ ✓

Solution: $x = 4$
</details>

---

**Problem 14**
Solve: $\dfrac{x^2 - 4}{x^2 - 9} \le 0$

<details>
<summary>Show Solution</summary>

**Solution**:
Factor:
$$\frac{(x-2)(x+2)}{(x-3)(x+3)} \le 0$$

Critical values: $x = -3, -2, 2, 3$

Sign chart (all factors):

| Interval | Sign |
|----------|------|
| $x < -3$ | $+$ |
| $-3 < x < -2$ | $-$ |
| $-2 < x < 2$ | $+$ |
| $2 < x < 3$ | $-$ |
| $x > 3$ | $+$ |

Include zeros of numerator ($x = \pm 2$), exclude zeros of denominator ($x = \pm 3$)

Solution: $(-3, -2] \cup [2, 3)$
</details>

---

**Problem 15**
Solve: $|x^2 - 4| = 3x$

<details>
<summary>Show Solution</summary>

**Solution**:
Note: $3x$ must be $\ge 0$, so $x \ge 0$

Case 1: $x^2 - 4 = 3x$ (when $x^2 - 4 \ge 0$)
$$x^2 - 3x - 4 = 0$$
$$(x - 4)(x + 1) = 0$$
$$x = 4 \text{ or } x = -1$$

Check domain ($x \ge 0$): only $x = 4$
Check $x^2 - 4 \ge 0$: $16 - 4 = 12 \ge 0$ ✓

Case 2: $-(x^2 - 4) = 3x$ (when $x^2 - 4 < 0$)
$$-x^2 + 4 = 3x$$
$$x^2 + 3x - 4 = 0$$
$$(x + 4)(x - 1) = 0$$
$$x = -4 \text{ or } x = 1$$

Check domain ($x \ge 0$): only $x = 1$
Check $x^2 - 4 < 0$: $1 - 4 = -3 < 0$ ✓

Solutions: $x = 1$ and $x = 4$
</details>

---

### AP Exam Style

**Problem 16**
Find all values of $x$ for which $\dfrac{x - 1}{x + 2} \ge 1$.

<details>
<summary>Show Solution</summary>

**Solution**:
$$\frac{x - 1}{x + 2} - 1 \ge 0$$
$$\frac{x - 1 - (x + 2)}{x + 2} \ge 0$$
$$\frac{-3}{x + 2} \ge 0$$

Since $-3 < 0$, we need $x + 2 < 0$:
$$x < -2$$

Solution: $(-\infty, -2)$
</details>

---

**Problem 17**
If $f(x) = x^3 - 6x^2 + 9x$, find all values where $f(x) = 0$.

<details>
<summary>Show Solution</summary>

**Solution**:
Factor out $x$:
$$x(x^2 - 6x + 9) = x(x - 3)^2 = 0$$

Solutions: $x = 0$ and $x = 3$ (double root)
</details>

---

**Problem 18**
Solve $2^{x+1} = 8$ for $x$.

<details>
<summary>Show Solution</summary>

**Solution**:
$$2^{x+1} = 2^3$$
$$x + 1 = 3$$
$$x = 2$$
</details>

---

**Problem 19** *(Free Response Style)*
Consider the equation $\sqrt{x + 4} = x - 2$.

(a) Find all solutions algebraically.
(b) Verify your solutions.
(c) Explain why one solution might be extraneous.
(d) Graph both sides to confirm your answer.

<details>
<summary>Show Solution</summary>

**Solution**:

**(a)** Square both sides:
$$x + 4 = (x - 2)^2 = x^2 - 4x + 4$$
$$x + 4 = x^2 - 4x + 4$$
$$5x = x^2$$
$$x^2 - 5x = 0$$
$$x(x - 5) = 0$$
$$x = 0 \text{ or } x = 5$$

**(b)** Verify $x = 0$:
- LHS: $\sqrt{4} = 2$
- RHS: $0 - 2 = -2$
- $2 \ne -2$ ✗ EXTRANEOUS

Verify $x = 5$:
- LHS: $\sqrt{9} = 3$
- RHS: $5 - 2 = 3$
- $3 = 3$ ✓

**Only solution: $x = 5$**

**(c)** Squaring both sides can introduce extraneous solutions because $(-a)^2 = a^2$. The solution $x = 0$ satisfies the squared equation but not the original because the RHS is negative while the LHS (a square root) must be non-negative.

**(d)** The graph of $y = \sqrt{x + 4}$ starts at $(-4, 0)$ and increases.
The graph of $y = x - 2$ is a line.
They intersect only at $x = 5$.
</details>

---

**Problem 20** *(Free Response Style)*
Let $f(x) = \dfrac{x^2 - 1}{x^2 - 4}$.

(a) Find the domain of $f$.
(b) Solve $f(x) = 0$.
(c) Solve $f(x) < 0$.
(d) Find the horizontal asymptote and explain what it tells us about $f(x) = 1$.

<details>
<summary>Show Solution</summary>

**Solution**:

**(a)** Denominator $\ne 0$:
$$x^2 - 4 \ne 0 \implies x \ne \pm 2$$

Domain: $(-\infty, -2) \cup (-2, 2) \cup (2, \infty)$

**(b)** $f(x) = 0$ when numerator = 0:
$$x^2 - 1 = 0$$
$$x = \pm 1$$

**(c)** Factor: $f(x) = \frac{(x-1)(x+1)}{(x-2)(x+2)}$

Critical values: $x = -2, -1, 1, 2$

Sign chart:

| Interval | Sign |
|----------|------|
| $x < -2$ | $+$ |
| $-2 < x < -1$ | $-$ |
| $-1 < x < 1$ | $+$ |
| $1 < x < 2$ | $-$ |
| $x > 2$ | $+$ |

Solution (where $f(x) < 0$): $(-2, -1) \cup (1, 2)$

**(d)** Horizontal asymptote: As $x \to \pm\infty$:
$$f(x) = \frac{x^2 - 1}{x^2 - 4} \to \frac{x^2}{x^2} = 1$$

So $y = 1$ is the horizontal asymptote.

For $f(x) = 1$:
$$\frac{x^2 - 1}{x^2 - 4} = 1$$
$$x^2 - 1 = x^2 - 4$$
$$-1 = -4$$

This is never true! So $f(x) = 1$ has no solution, which matches the fact that the graph approaches but never reaches the asymptote $y = 1$.
</details>

---

## What's Next

Now that you've mastered solving equations and inequalities, you're ready to explore [Rational Expressions](/calculus/0107-rational-expressions), where we'll learn to simplify, add, subtract, multiply, and divide fractions containing polynomials.

---

<div align="center">

[← Factoring Techniques](/calculus/0105-factoring-techniques) | [Rational Expressions →](/calculus/0107-rational-expressions)

</div>
