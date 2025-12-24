# Factoring Techniques
<p class="article-date">July 5, 2024</p>

## Prerequisites
Before diving in, make sure you're comfortable with:
- Basic arithmetic with polynomials
- Distributive property
- Exponent rules

## Learning Objectives
By the end of this section, you will be able to:
- Factor out the Greatest Common Factor (GCF)
- Factor trinomials of the form $x^2 + bx + c$ and $ax^2 + bx + c$
- Recognize and factor special patterns (difference of squares, perfect square trinomials, sum/difference of cubes)
- Factor by grouping
- Factor higher-degree polynomials
- Choose the right factoring strategy

## The Big Picture: Why Factoring Matters

Factoring is the reverse of multiplication:
$$\text{Expand: } (x + 3)(x - 2) = x^2 + x - 6$$
$$\text{Factor: } x^2 + x - 6 = (x + 3)(x - 2)$$

> **Calculus Connection**: You'll need factoring to:
> - Simplify before differentiating
> - Find zeros of derivatives (critical points)
> - Use partial fractions for integration
> - Simplify limits

## Strategy Overview: Which Method to Use?

| Look For | Technique |
|----------|-----------|
| Common factor in all terms | GCF first (always check this!) |
| Two terms, subtraction | Difference of squares or cubes |
| Two terms, addition | Sum of cubes (rare) |
| Three terms, $a = 1$ | Simple trinomial factoring |
| Three terms, $a \ne 1$ | AC method or trial and error |
| Four terms | Factor by grouping |

**Golden Rule**: Always factor out the GCF first!

## Technique 1: Greatest Common Factor (GCF)

Find the largest factor common to ALL terms.

### Example 1
Factor $6x^3 + 9x^2 - 15x$

**Solution**:
- GCF of coefficients: $\gcd(6, 9, 15) = 3$
- GCF of variables: $x$ (lowest power)
- GCF = $3x$

$$6x^3 + 9x^2 - 15x = 3x(2x^2 + 3x - 5)$$

### Example 2
Factor $4x^2y^3 - 8xy^2 + 12x^3y^4$

**Solution**:
- GCF of coefficients: $4$
- GCF of $x$: $x$ (lowest power)
- GCF of $y$: $y^2$ (lowest power)

$$= 4xy^2(xy - 2 + 3x^2y^2)$$

## Technique 2: Difference of Squares

$$a^2 - b^2 = (a + b)(a - b)$$

### Recognition
- Exactly TWO terms
- Subtraction
- Both terms are perfect squares

### Example
Factor $x^2 - 49$

**Solution**:
$$x^2 - 49 = x^2 - 7^2 = (x + 7)(x - 7)$$

### Example: Hidden Pattern
Factor $x^4 - 16$

**Solution**:
$$x^4 - 16 = (x^2)^2 - 4^2 = (x^2 + 4)(x^2 - 4)$$

Continue factoring $x^2 - 4$:
$$= (x^2 + 4)(x + 2)(x - 2)$$

Note: $x^2 + 4$ cannot be factored over the reals.

## Technique 3: Perfect Square Trinomials

$$a^2 + 2ab + b^2 = (a + b)^2$$
$$a^2 - 2ab + b^2 = (a - b)^2$$

### Recognition
- First term is a perfect square
- Last term is a perfect square
- Middle term is $2 \times \sqrt{\text{first}} \times \sqrt{\text{last}}$

### Example
Factor $x^2 + 10x + 25$

**Solution**:
- First: $x^2 = (x)^2$ ✓
- Last: $25 = (5)^2$ ✓
- Middle: $10x = 2(x)(5)$ ✓

$$x^2 + 10x + 25 = (x + 5)^2$$

### Example
Factor $4x^2 - 12x + 9$

**Solution**:
- First: $4x^2 = (2x)^2$ ✓
- Last: $9 = (3)^2$ ✓
- Middle: $12x = 2(2x)(3)$ ✓ (and it's subtracted)

$$4x^2 - 12x + 9 = (2x - 3)^2$$

## Technique 4: Sum and Difference of Cubes

$$a^3 + b^3 = (a + b)(a^2 - ab + b^2)$$
$$a^3 - b^3 = (a - b)(a^2 + ab + b^2)$$

> **Memory Aid**: "SOAP" — Same sign, Opposite sign, Always Positive
> - First factor: same sign as original
> - Second factor: opposite, then always plus

### Example
Factor $x^3 - 27$

**Solution**:
$$x^3 - 27 = x^3 - 3^3 = (x - 3)(x^2 + 3x + 9)$$

### Example
Factor $8x^3 + 125$

**Solution**:
$$8x^3 + 125 = (2x)^3 + 5^3 = (2x + 5)(4x^2 - 10x + 25)$$

## Technique 5: Simple Trinomial Factoring ($a = 1$)

For $x^2 + bx + c$, find two numbers that:
- **Multiply** to give $c$
- **Add** to give $b$

### Example
Factor $x^2 + 7x + 12$

**Solution**:
Need numbers that multiply to $12$ and add to $7$:
- $3 \times 4 = 12$ ✓
- $3 + 4 = 7$ ✓

$$x^2 + 7x + 12 = (x + 3)(x + 4)$$

### Example with Negatives
Factor $x^2 - 5x - 14$

**Solution**:
Need numbers that multiply to $-14$ and add to $-5$:
- $(-7) \times 2 = -14$ ✓
- $(-7) + 2 = -5$ ✓

$$x^2 - 5x - 14 = (x - 7)(x + 2)$$

### Sign Patterns

| $b$ (middle) | $c$ (last) | Signs in factors |
|--------------|------------|------------------|
| $+$ | $+$ | $(x + \_)(x + \_)$ |
| $-$ | $+$ | $(x - \_)(x - \_)$ |
| $+$ | $-$ | $(x + \text{bigger})(x - \text{smaller})$ |
| $-$ | $-$ | $(x - \text{bigger})(x + \text{smaller})$ |

## Technique 6: AC Method ($a \ne 1$)

For $ax^2 + bx + c$:

1. Multiply $a \cdot c$
2. Find two numbers that multiply to $ac$ and add to $b$
3. Rewrite the middle term using these numbers
4. Factor by grouping

### Example
Factor $2x^2 + 7x + 3$

**Solution**:

**Step 1**: $a \cdot c = 2 \cdot 3 = 6$

**Step 2**: Find numbers that multiply to $6$ and add to $7$: $1$ and $6$

**Step 3**: Rewrite: $2x^2 + x + 6x + 3$

**Step 4**: Group and factor:
$$= x(2x + 1) + 3(2x + 1)$$
$$= (2x + 1)(x + 3)$$

### Example
Factor $6x^2 - 11x - 10$

**Solution**:

**Step 1**: $a \cdot c = 6 \cdot (-10) = -60$

**Step 2**: Find numbers that multiply to $-60$ and add to $-11$: $4$ and $-15$

**Step 3**: Rewrite: $6x^2 + 4x - 15x - 10$

**Step 4**: Group and factor:
$$= 2x(3x + 2) - 5(3x + 2)$$
$$= (3x + 2)(2x - 5)$$

## Technique 7: Factor by Grouping

For four terms: group into pairs and factor each pair.

### Example
Factor $x^3 + 2x^2 + 3x + 6$

**Solution**:
$$= (x^3 + 2x^2) + (3x + 6)$$
$$= x^2(x + 2) + 3(x + 2)$$
$$= (x + 2)(x^2 + 3)$$

### Example
Factor $xy - 2y + 4x - 8$

**Solution**:
$$= y(x - 2) + 4(x - 2)$$
$$= (x - 2)(y + 4)$$

## Technique 8: Substitution for Higher Degrees

Sometimes a substitution reveals a familiar pattern.

### Example
Factor $x^4 - 5x^2 + 4$

**Solution**:
Let $u = x^2$:
$$u^2 - 5u + 4 = (u - 1)(u - 4)$$

Substitute back:
$$= (x^2 - 1)(x^2 - 4)$$

Factor further:
$$= (x + 1)(x - 1)(x + 2)(x - 2)$$

## Complete Factoring Strategy

1. **Factor out the GCF** (always first!)
2. **Count the terms**:
   - 2 terms: difference of squares? Sum/difference of cubes?
   - 3 terms: perfect square trinomial? Regular trinomial?
   - 4 terms: factor by grouping
3. **Check if any factors can be factored further**
4. **Verify by multiplying back**

## Key Formulas Summary

| Pattern | Factored Form |
|---------|---------------|
| $a^2 - b^2$ | $(a + b)(a - b)$ |
| $a^2 + 2ab + b^2$ | $(a + b)^2$ |
| $a^2 - 2ab + b^2$ | $(a - b)^2$ |
| $a^3 + b^3$ | $(a + b)(a^2 - ab + b^2)$ |
| $a^3 - b^3$ | $(a - b)(a^2 + ab + b^2)$ |

## Common Mistakes to Avoid

1. **Forgetting to factor out the GCF first**
   - $2x^2 + 4x = 2x(x + 2)$, not just looking for trinomial factors

2. **Sign errors in AC method**
   - Keep careful track of positive and negative factors

3. **Stopping too early**
   - $x^4 - 16 = (x^2 + 4)(x^2 - 4)$, but $x^2 - 4$ factors further!

4. **Trying to factor $a^2 + b^2$**
   - The sum of squares does NOT factor over the reals
   - $x^2 + 9 \ne (x + 3)(x + 3)$

5. **Wrong signs in sum/difference of cubes**
   - Use SOAP: Same, Opposite, Always Positive

## Calculus Connection

Factoring is essential for:

1. **Finding Critical Points**: Set $f'(x) = 0$ and factor to solve

2. **Simplifying Before Differentiation**: Factor first to avoid messy quotient rule

3. **Partial Fractions**: Factor denominators to decompose fractions for integration

4. **Limits**: Factor to cancel common terms and evaluate indeterminate forms

---

## Practice Problems

### Basic (Computational)

**Problem 1**
Factor completely: $5x^3 - 15x^2$

<details>
<summary>Show Solution</summary>

**Solution**:
GCF = $5x^2$
$$5x^3 - 15x^2 = 5x^2(x - 3)$$
</details>

---

**Problem 2**
Factor: $x^2 - 81$

<details>
<summary>Show Solution</summary>

**Solution**:
Difference of squares: $x^2 - 9^2$
$$x^2 - 81 = (x + 9)(x - 9)$$
</details>

---

**Problem 3**
Factor: $x^2 + 8x + 15$

<details>
<summary>Show Solution</summary>

**Solution**:
Need numbers that multiply to 15 and add to 8: 3 and 5
$$x^2 + 8x + 15 = (x + 3)(x + 5)$$
</details>

---

**Problem 4**
Factor: $x^2 - 6x + 9$

<details>
<summary>Show Solution</summary>

**Solution**:
Perfect square trinomial: $x^2 - 2(x)(3) + 3^2$
$$x^2 - 6x + 9 = (x - 3)^2$$
</details>

---

**Problem 5**
Factor: $x^3 + 64$

<details>
<summary>Show Solution</summary>

**Solution**:
Sum of cubes: $x^3 + 4^3$
$$x^3 + 64 = (x + 4)(x^2 - 4x + 16)$$
</details>

---

### Intermediate (Multi-step)

**Problem 6**
Factor completely: $2x^3 - 18x$

<details>
<summary>Show Solution</summary>

**Solution**:
GCF first: $2x(x^2 - 9)$

Then difference of squares:
$$2x^3 - 18x = 2x(x + 3)(x - 3)$$
</details>

---

**Problem 7**
Factor: $3x^2 + 10x + 8$

<details>
<summary>Show Solution</summary>

**Solution**:
AC method: $a \cdot c = 24$, need factors that add to 10: 4 and 6

$$3x^2 + 4x + 6x + 8$$
$$= x(3x + 4) + 2(3x + 4)$$
$$= (3x + 4)(x + 2)$$
</details>

---

**Problem 8**
Factor: $x^2 - 2x - 35$

<details>
<summary>Show Solution</summary>

**Solution**:
Need numbers that multiply to $-35$ and add to $-2$: $-7$ and $5$
$$x^2 - 2x - 35 = (x - 7)(x + 5)$$
</details>

---

**Problem 9**
Factor: $x^3 - 3x^2 - 4x + 12$

<details>
<summary>Show Solution</summary>

**Solution**:
Group: $(x^3 - 3x^2) + (-4x + 12)$
$$= x^2(x - 3) - 4(x - 3)$$
$$= (x - 3)(x^2 - 4)$$
$$= (x - 3)(x + 2)(x - 2)$$
</details>

---

**Problem 10**
Factor: $4x^2 - 25y^2$

<details>
<summary>Show Solution</summary>

**Solution**:
Difference of squares: $(2x)^2 - (5y)^2$
$$4x^2 - 25y^2 = (2x + 5y)(2x - 5y)$$
</details>

---

### Advanced (Complex Applications)

**Problem 11**
Factor completely: $x^4 - 81$

<details>
<summary>Show Solution</summary>

**Solution**:
Difference of squares: $(x^2)^2 - 9^2$
$$= (x^2 + 9)(x^2 - 9)$$

Factor $x^2 - 9$ further:
$$= (x^2 + 9)(x + 3)(x - 3)$$

Note: $x^2 + 9$ cannot be factored over the reals.
</details>

---

**Problem 12**
Factor: $6x^2 - 7x - 20$

<details>
<summary>Show Solution</summary>

**Solution**:
AC method: $a \cdot c = -120$, need factors that add to $-7$: $8$ and $-15$

$$6x^2 + 8x - 15x - 20$$
$$= 2x(3x + 4) - 5(3x + 4)$$
$$= (3x + 4)(2x - 5)$$
</details>

---

**Problem 13**
Factor: $x^6 - 1$

<details>
<summary>Show Solution</summary>

**Solution**:
Difference of squares: $(x^3)^2 - 1^2$
$$= (x^3 + 1)(x^3 - 1)$$

Apply sum and difference of cubes:
$$= (x + 1)(x^2 - x + 1)(x - 1)(x^2 + x + 1)$$
</details>

---

**Problem 14**
Factor: $x^4 + 4x^2 - 21$

<details>
<summary>Show Solution</summary>

**Solution**:
Let $u = x^2$:
$$u^2 + 4u - 21 = (u + 7)(u - 3)$$

Substitute back:
$$= (x^2 + 7)(x^2 - 3)$$

Neither factor factors further over the reals.
</details>

---

**Problem 15**
Factor completely: $3x^4 - 24x^2 + 48$

<details>
<summary>Show Solution</summary>

**Solution**:
GCF = 3:
$$= 3(x^4 - 8x^2 + 16)$$

Let $u = x^2$:
$$= 3(u^2 - 8u + 16) = 3(u - 4)^2$$

Substitute back:
$$= 3(x^2 - 4)^2 = 3[(x + 2)(x - 2)]^2$$
$$= 3(x + 2)^2(x - 2)^2$$
</details>

---

### AP Exam Style

**Problem 16**
Factor $x^3 - 8$ and use it to evaluate $\displaystyle\lim_{x \to 2} \frac{x^3 - 8}{x - 2}$

<details>
<summary>Show Solution</summary>

**Solution**:
Factor: $x^3 - 8 = (x - 2)(x^2 + 2x + 4)$

$$\lim_{x \to 2} \frac{(x - 2)(x^2 + 2x + 4)}{x - 2} = \lim_{x \to 2} (x^2 + 2x + 4)$$

$$= 4 + 4 + 4 = 12$$
</details>

---

**Problem 17**
For what value of $k$ is $x^2 + kx + 36$ a perfect square trinomial?

<details>
<summary>Show Solution</summary>

**Solution**:
For perfect square: $x^2 + kx + 36 = (x + a)^2$ where $a^2 = 36$

So $a = 6$ (or $-6$), and $k = 2a = 12$ (or $-12$)

**Answer**: $k = 12$ or $k = -12$
</details>

---

**Problem 18**
If $f(x) = x^2 - 4x - 12$, find the zeros by factoring.

<details>
<summary>Show Solution</summary>

**Solution**:
Factor: Need numbers that multiply to $-12$ and add to $-4$: $-6$ and $2$

$$x^2 - 4x - 12 = (x - 6)(x + 2)$$

Set equal to zero:
$$x = 6 \text{ or } x = -2$$
</details>

---

**Problem 19** *(Free Response Style)*
Consider $f(x) = x^3 - 4x^2 - 7x + 10$.

(a) Show that $(x - 1)$ is a factor of $f(x)$.
(b) Factor $f(x)$ completely.
(c) Find all zeros of $f(x)$.
(d) Use the factored form to determine the end behavior and sketch the graph.

<details>
<summary>Show Solution</summary>

**Solution**:

**(a)** By the Factor Theorem, $(x - 1)$ is a factor if $f(1) = 0$:
$$f(1) = 1 - 4 - 7 + 10 = 0$$ ✓

**(b)** Divide by $(x - 1)$ using synthetic or long division:

| 1 | 1 | -4 | -7 | 10 |
|---|---|----|----|-----|
| | | 1 | -3 | -10 |
| | 1 | -3 | -10 | 0 |

So $f(x) = (x - 1)(x^2 - 3x - 10)$

Factor the quadratic:
$$x^2 - 3x - 10 = (x - 5)(x + 2)$$

$$f(x) = (x - 1)(x - 5)(x + 2)$$

**(c)** Zeros: $x = 1$, $x = 5$, $x = -2$

**(d)** Leading term is $x^3$ (positive):
- As $x \to -\infty$, $f(x) \to -\infty$
- As $x \to \infty$, $f(x) \to \infty$

Graph crosses x-axis at $x = -2, 1, 5$.
</details>

---

**Problem 20** *(Free Response Style)*
The polynomial $p(x) = 2x^3 + ax^2 + bx - 6$ has factors $(x - 1)$ and $(x + 2)$.

(a) Find the values of $a$ and $b$.
(b) Find the third factor.
(c) Find all values of $x$ where $p(x) = 0$.

<details>
<summary>Show Solution</summary>

**Solution**:

**(a)** Since $(x - 1)$ is a factor: $p(1) = 0$
$$2(1) + a(1) + b(1) - 6 = 0$$
$$2 + a + b - 6 = 0$$
$$a + b = 4 \quad \text{...(1)}$$

Since $(x + 2)$ is a factor: $p(-2) = 0$
$$2(-8) + a(4) + b(-2) - 6 = 0$$
$$-16 + 4a - 2b - 6 = 0$$
$$4a - 2b = 22$$
$$2a - b = 11 \quad \text{...(2)}$$

Add equations (1) and (2):
$$3a = 15 \implies a = 5$$

From (1): $b = 4 - 5 = -1$

**$a = 5$, $b = -1$**

**(b)** $p(x) = 2x^3 + 5x^2 - x - 6$

We know two factors: $(x - 1)(x + 2) = x^2 + x - 2$

Divide: $\frac{2x^3 + 5x^2 - x - 6}{x^2 + x - 2} = 2x + 3$

Third factor: $(2x + 3)$

**(c)** $p(x) = (x - 1)(x + 2)(2x + 3) = 0$

Solutions: $x = 1$, $x = -2$, $x = -\frac{3}{2}$
</details>

---

## What's Next

Now that you've mastered factoring, you're ready to explore [Solving Equations](/calculus/0106-solving-equations), where we'll apply these techniques to find solutions to polynomial, rational, and radical equations.

---

<div align="center">

[← Transformations](/calculus/0104-transformations) | [Solving Equations →](/calculus/0106-solving-equations)

</div>
