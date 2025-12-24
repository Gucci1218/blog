# Rational Expressions
<p class="article-date">July 14, 2024</p>

## Prerequisites
Before diving in, make sure you're comfortable with:
- [Factoring Techniques](/calculus/0105-factoring-techniques)
- [Solving Equations](/calculus/0106-solving-equations)
- Working with fractions (arithmetic)

## Learning Objectives
By the end of this section, you will be able to:
- Simplify rational expressions by factoring
- Multiply and divide rational expressions
- Add and subtract rational expressions using LCD
- Simplify complex fractions
- Identify domain restrictions

## The Big Picture: Fractions with Polynomials

A **rational expression** is a fraction where the numerator and/or denominator are polynomials:

$$\frac{x^2 - 4}{x + 3}, \quad \frac{2x + 1}{x^2 - 5x + 6}, \quad \frac{1}{x}$$

> **Calculus Connection**: Rational expressions appear constantly in calculus:
> - Quotient rule derivatives
> - Partial fractions for integration
> - Limits involving fractions
> - Related rates and optimization

## Domain Restrictions

**Critical Rule**: The denominator can NEVER equal zero.

Before simplifying, always identify values that make the denominator zero—these are **excluded from the domain**.

### Example
Find the domain of $\dfrac{x + 2}{x^2 - 9}$

Factor denominator: $x^2 - 9 = (x+3)(x-3)$

Set $\ne 0$: $x \ne 3$ and $x \ne -3$

**Domain**: All real numbers except $x = 3$ and $x = -3$

## Simplifying Rational Expressions

### Strategy
1. Factor numerator and denominator completely
2. Cancel common factors
3. State restrictions (values excluded from domain)

### Example 1: Basic Simplification
Simplify $\dfrac{x^2 - 4}{x^2 + 4x + 4}$

**Solution**:
$$= \frac{(x+2)(x-2)}{(x+2)^2} = \frac{x-2}{x+2}, \quad x \ne -2$$

### Example 2: Factoring Required
Simplify $\dfrac{x^2 - 5x + 6}{x^2 - 4}$

**Solution**:
$$= \frac{(x-2)(x-3)}{(x-2)(x+2)} = \frac{x-3}{x+2}, \quad x \ne 2, -2$$

> **Important**: Even though $(x-2)$ cancels, $x = 2$ is still excluded from the domain!

## Multiplying Rational Expressions

### Rule
$$\frac{A}{B} \cdot \frac{C}{D} = \frac{AC}{BD}$$

### Strategy
1. Factor all numerators and denominators
2. Cancel common factors
3. Multiply remaining factors

### Example
Multiply $\dfrac{x^2 - 9}{x^2 + 6x + 9} \cdot \dfrac{x + 3}{x - 3}$

**Solution**:
$$= \frac{(x+3)(x-3)}{(x+3)^2} \cdot \frac{x+3}{x-3}$$

$$= \frac{(x+3)(x-3)(x+3)}{(x+3)^2(x-3)}$$

$$= \frac{(x+3)^2(x-3)}{(x+3)^2(x-3)} = 1, \quad x \ne -3, 3$$

## Dividing Rational Expressions

### Rule
$$\frac{A}{B} \div \frac{C}{D} = \frac{A}{B} \cdot \frac{D}{C}$$

**Multiply by the reciprocal** of the second fraction.

### Example
Divide $\dfrac{x^2 - 1}{x + 2} \div \dfrac{x + 1}{x^2 - 4}$

**Solution**:
$$= \frac{x^2 - 1}{x + 2} \cdot \frac{x^2 - 4}{x + 1}$$

$$= \frac{(x+1)(x-1)}{x+2} \cdot \frac{(x+2)(x-2)}{x+1}$$

$$= \frac{(x+1)(x-1)(x+2)(x-2)}{(x+2)(x+1)}$$

$$= (x-1)(x-2) = x^2 - 3x + 2, \quad x \ne -2, -1, 2$$

## Adding and Subtracting Rational Expressions

### Same Denominator
$$\frac{A}{C} + \frac{B}{C} = \frac{A + B}{C}$$

### Different Denominators
1. Find the Least Common Denominator (LCD)
2. Rewrite each fraction with the LCD
3. Add or subtract numerators
4. Simplify if possible

### Finding the LCD
1. Factor each denominator
2. LCD = product of each factor raised to its highest power

### Example 1: Same Denominator
Simplify $\dfrac{3x + 1}{x - 2} - \dfrac{x - 5}{x - 2}$

**Solution**:
$$= \frac{(3x + 1) - (x - 5)}{x - 2} = \frac{3x + 1 - x + 5}{x - 2} = \frac{2x + 6}{x - 2} = \frac{2(x + 3)}{x - 2}$$

### Example 2: Different Denominators
Simplify $\dfrac{2}{x + 3} + \dfrac{5}{x - 1}$

**Solution**:
LCD = $(x + 3)(x - 1)$

$$= \frac{2(x - 1)}{(x+3)(x-1)} + \frac{5(x + 3)}{(x+3)(x-1)}$$

$$= \frac{2(x-1) + 5(x+3)}{(x+3)(x-1)}$$

$$= \frac{2x - 2 + 5x + 15}{(x+3)(x-1)}$$

$$= \frac{7x + 13}{(x+3)(x-1)}, \quad x \ne -3, 1$$

### Example 3: Factored Denominators
Simplify $\dfrac{3}{x^2 - 4} - \dfrac{2}{x + 2}$

**Solution**:
Factor: $x^2 - 4 = (x+2)(x-2)$

LCD = $(x + 2)(x - 2)$

$$= \frac{3}{(x+2)(x-2)} - \frac{2(x-2)}{(x+2)(x-2)}$$

$$= \frac{3 - 2(x - 2)}{(x+2)(x-2)}$$

$$= \frac{3 - 2x + 4}{(x+2)(x-2)}$$

$$= \frac{7 - 2x}{(x+2)(x-2)}, \quad x \ne -2, 2$$

## Complex Fractions

A **complex fraction** has fractions in the numerator, denominator, or both.

### Method 1: Simplify Top and Bottom, Then Divide

### Method 2: Multiply by LCD of All Small Fractions

### Example 1
Simplify $\dfrac{\frac{1}{x} + \frac{1}{y}}{\frac{1}{x} - \frac{1}{y}}$

**Method 1**:
$$= \frac{\frac{y + x}{xy}}{\frac{y - x}{xy}} = \frac{y + x}{xy} \cdot \frac{xy}{y - x} = \frac{x + y}{y - x}$$

**Method 2**: Multiply top and bottom by $xy$:
$$= \frac{xy \cdot \left(\frac{1}{x} + \frac{1}{y}\right)}{xy \cdot \left(\frac{1}{x} - \frac{1}{y}\right)} = \frac{y + x}{y - x}$$

### Example 2
Simplify $\dfrac{1 - \frac{1}{x}}{1 + \frac{1}{x}}$

**Solution**: Multiply top and bottom by $x$:
$$= \frac{x - 1}{x + 1}$$

## Polynomial Long Division

When the numerator has degree $\ge$ denominator, divide to get a polynomial plus a remainder.

### Example
Simplify $\dfrac{x^2 + 3x + 5}{x + 1}$

**Solution** (using long division or synthetic division):

$$x^2 + 3x + 5 = (x + 1)(x + 2) + 3$$

So:
$$\frac{x^2 + 3x + 5}{x + 1} = x + 2 + \frac{3}{x + 1}$$

## Key Operations Summary

| Operation | Method |
|-----------|--------|
| Simplify | Factor and cancel |
| Multiply | Factor, cancel, multiply |
| Divide | Multiply by reciprocal |
| Add/Subtract (same denom) | Combine numerators |
| Add/Subtract (different denom) | Find LCD, convert, combine |
| Complex fractions | Multiply by LCD or simplify separately |

## Common Mistakes to Avoid

1. **Canceling terms instead of factors**
   - Wrong: $\frac{x + 3}{x + 5} = \frac{3}{5}$ (NO! Can't cancel the $x$'s)
   - Right: $\frac{x(x + 3)}{x(x + 5)} = \frac{x + 3}{x + 5}$ (cancel the factor $x$)

2. **Forgetting domain restrictions after canceling**
   - $\frac{(x-2)(x+1)}{x-2} = x + 1$, but $x \ne 2$ still!

3. **Sign errors when subtracting**
   - $\frac{A}{C} - \frac{B}{C} = \frac{A - B}{C}$, not $\frac{A - B}{C - C}$
   - Distribute the negative: $(3x - 5) - (2x + 1) = 3x - 5 - 2x - 1$

4. **Wrong LCD**
   - For $\frac{1}{x}$ and $\frac{1}{x^2}$: LCD = $x^2$, not $x$
   - Use highest power of each factor

5. **Canceling across addition**
   - Wrong: $\frac{x + 2}{x} = 2$ (NO!)
   - You can only cancel factors that multiply the entire expression

## Calculus Connection

Rational expressions are essential for:

1. **Quotient Rule**: $\left(\frac{f}{g}\right)' = \frac{f'g - fg'}{g^2}$

2. **Partial Fractions**: Breaking $\frac{1}{x^2-1}$ into $\frac{1}{2(x-1)} - \frac{1}{2(x+1)}$ for integration

3. **Limits**: Simplifying $\lim_{x \to 2} \frac{x^2 - 4}{x - 2}$ by factoring

4. **Asymptotes**: Finding horizontal and vertical asymptotes of rational functions

---

## Practice Problems

### Basic (Computational)

**Problem 1**
Simplify: $\dfrac{x^2 - 16}{x + 4}$

<details>
<summary>Show Solution</summary>

**Solution**:
$$= \frac{(x+4)(x-4)}{x+4} = x - 4, \quad x \ne -4$$
</details>

---

**Problem 2**
Simplify: $\dfrac{x^2 + 5x + 6}{x^2 + 2x}$

<details>
<summary>Show Solution</summary>

**Solution**:
$$= \frac{(x+2)(x+3)}{x(x+2)} = \frac{x+3}{x}, \quad x \ne 0, -2$$
</details>

---

**Problem 3**
Multiply: $\dfrac{x}{x + 1} \cdot \dfrac{x + 1}{x^2}$

<details>
<summary>Show Solution</summary>

**Solution**:
$$= \frac{x(x+1)}{(x+1)x^2} = \frac{1}{x}, \quad x \ne 0, -1$$
</details>

---

**Problem 4**
Divide: $\dfrac{x^2}{x - 3} \div \dfrac{x}{x - 3}$

<details>
<summary>Show Solution</summary>

**Solution**:
$$= \frac{x^2}{x-3} \cdot \frac{x-3}{x} = \frac{x^2(x-3)}{(x-3)x} = x, \quad x \ne 0, 3$$
</details>

---

**Problem 5**
Add: $\dfrac{2}{x} + \dfrac{3}{x}$

<details>
<summary>Show Solution</summary>

**Solution**:
$$= \frac{2 + 3}{x} = \frac{5}{x}, \quad x \ne 0$$
</details>

---

### Intermediate (Multi-step)

**Problem 6**
Simplify: $\dfrac{x^2 - x - 6}{x^2 - 9}$

<details>
<summary>Show Solution</summary>

**Solution**:
$$= \frac{(x-3)(x+2)}{(x-3)(x+3)} = \frac{x+2}{x+3}, \quad x \ne 3, -3$$
</details>

---

**Problem 7**
Multiply: $\dfrac{x^2 - 4}{x^2 + 3x} \cdot \dfrac{x^2 + x}{x - 2}$

<details>
<summary>Show Solution</summary>

**Solution**:
$$= \frac{(x+2)(x-2)}{x(x+3)} \cdot \frac{x(x+1)}{x-2}$$

$$= \frac{(x+2)(x-2) \cdot x(x+1)}{x(x+3)(x-2)}$$

$$= \frac{(x+2)(x+1)}{x+3}, \quad x \ne 0, 2, -3$$
</details>

---

**Problem 8**
Subtract: $\dfrac{x}{x - 2} - \dfrac{2}{x + 2}$

<details>
<summary>Show Solution</summary>

**Solution**:
LCD = $(x-2)(x+2)$

$$= \frac{x(x+2)}{(x-2)(x+2)} - \frac{2(x-2)}{(x-2)(x+2)}$$

$$= \frac{x(x+2) - 2(x-2)}{(x-2)(x+2)}$$

$$= \frac{x^2 + 2x - 2x + 4}{(x-2)(x+2)}$$

$$= \frac{x^2 + 4}{x^2 - 4}, \quad x \ne 2, -2$$
</details>

---

**Problem 9**
Simplify the complex fraction: $\dfrac{\frac{1}{x} - 1}{1 - \frac{1}{x}}$

<details>
<summary>Show Solution</summary>

**Solution**:
Multiply top and bottom by $x$:

$$= \frac{1 - x}{x - 1} = \frac{-(x-1)}{x-1} = -1, \quad x \ne 0, 1$$
</details>

---

**Problem 10**
Add: $\dfrac{3}{x^2 - 1} + \dfrac{2}{x + 1}$

<details>
<summary>Show Solution</summary>

**Solution**:
Factor: $x^2 - 1 = (x+1)(x-1)$

LCD = $(x+1)(x-1)$

$$= \frac{3}{(x+1)(x-1)} + \frac{2(x-1)}{(x+1)(x-1)}$$

$$= \frac{3 + 2(x-1)}{(x+1)(x-1)}$$

$$= \frac{3 + 2x - 2}{(x+1)(x-1)}$$

$$= \frac{2x + 1}{x^2 - 1}, \quad x \ne 1, -1$$
</details>

---

### Advanced (Complex Applications)

**Problem 11**
Simplify: $\dfrac{x^3 - 8}{x^2 - 4}$

<details>
<summary>Show Solution</summary>

**Solution**:
Factor numerator (difference of cubes): $x^3 - 8 = (x-2)(x^2 + 2x + 4)$

Factor denominator: $x^2 - 4 = (x-2)(x+2)$

$$= \frac{(x-2)(x^2 + 2x + 4)}{(x-2)(x+2)} = \frac{x^2 + 2x + 4}{x + 2}, \quad x \ne 2, -2$$
</details>

---

**Problem 12**
Simplify: $\dfrac{x^2 - y^2}{x^3 + y^3} \cdot \dfrac{x^2 - xy + y^2}{x - y}$

<details>
<summary>Show Solution</summary>

**Solution**:
Factor:
- $x^2 - y^2 = (x+y)(x-y)$
- $x^3 + y^3 = (x+y)(x^2 - xy + y^2)$

$$= \frac{(x+y)(x-y)}{(x+y)(x^2-xy+y^2)} \cdot \frac{x^2-xy+y^2}{x-y}$$

$$= \frac{(x+y)(x-y)(x^2-xy+y^2)}{(x+y)(x^2-xy+y^2)(x-y)} = 1$$

with restrictions $x \ne y, -y$
</details>

---

**Problem 13**
Simplify: $\dfrac{1}{x-1} - \dfrac{1}{x} - \dfrac{1}{x(x-1)}$

<details>
<summary>Show Solution</summary>

**Solution**:
LCD = $x(x-1)$

$$= \frac{x}{x(x-1)} - \frac{x-1}{x(x-1)} - \frac{1}{x(x-1)}$$

$$= \frac{x - (x-1) - 1}{x(x-1)}$$

$$= \frac{x - x + 1 - 1}{x(x-1)}$$

$$= \frac{0}{x(x-1)} = 0, \quad x \ne 0, 1$$
</details>

---

**Problem 14**
Simplify the complex fraction: $\dfrac{\frac{1}{x+h} - \frac{1}{x}}{h}$

<details>
<summary>Show Solution</summary>

**Solution**:
First simplify the numerator:
$$\frac{1}{x+h} - \frac{1}{x} = \frac{x - (x+h)}{x(x+h)} = \frac{-h}{x(x+h)}$$

Then divide by $h$:
$$= \frac{-h}{x(x+h)} \cdot \frac{1}{h} = \frac{-1}{x(x+h)}, \quad h \ne 0$$

Note: This is the difference quotient for $f(x) = \frac{1}{x}$!
</details>

---

**Problem 15**
Express as a single fraction: $\dfrac{x}{x^2 - 4} + \dfrac{1}{x + 2} - \dfrac{1}{x - 2}$

<details>
<summary>Show Solution</summary>

**Solution**:
LCD = $(x+2)(x-2) = x^2 - 4$

$$= \frac{x}{(x+2)(x-2)} + \frac{x-2}{(x+2)(x-2)} - \frac{x+2}{(x+2)(x-2)}$$

$$= \frac{x + (x-2) - (x+2)}{x^2-4}$$

$$= \frac{x + x - 2 - x - 2}{x^2-4}$$

$$= \frac{x - 4}{x^2 - 4}, \quad x \ne 2, -2$$
</details>

---

### AP Exam Style

**Problem 16**
Simplify $\dfrac{x^2 - 9}{x^2 + 6x + 9}$ and use it to evaluate $\displaystyle\lim_{x \to -3} \dfrac{x^2 - 9}{x^2 + 6x + 9}$

<details>
<summary>Show Solution</summary>

**Solution**:
$$\frac{x^2 - 9}{x^2 + 6x + 9} = \frac{(x+3)(x-3)}{(x+3)^2} = \frac{x-3}{x+3}$$

$$\lim_{x \to -3} \frac{x-3}{x+3} = \frac{-6}{0}$$

The limit does not exist (approaches $\pm\infty$).

More precisely: as $x \to -3^+$, denominator $\to 0^+$, numerator $\to -6$, so limit $= -\infty$
</details>

---

**Problem 17**
If $f(x) = \dfrac{2x}{x - 1}$, find and simplify $f\left(\dfrac{1}{x}\right)$.

<details>
<summary>Show Solution</summary>

**Solution**:
$$f\left(\frac{1}{x}\right) = \frac{2 \cdot \frac{1}{x}}{\frac{1}{x} - 1} = \frac{\frac{2}{x}}{\frac{1-x}{x}} = \frac{2}{x} \cdot \frac{x}{1-x} = \frac{2}{1-x}$$
</details>

---

**Problem 18**
For what values of $x$ is $\dfrac{x - 3}{x^2 - 5x + 6}$ undefined?

<details>
<summary>Show Solution</summary>

**Solution**:
Factor denominator: $x^2 - 5x + 6 = (x-2)(x-3)$

Undefined when denominator = 0:
$$x = 2 \text{ or } x = 3$$
</details>

---

**Problem 19** *(Free Response Style)*
Consider $f(x) = \dfrac{x^2 - 4}{x^2 - x - 2}$.

(a) Find the domain of $f$.
(b) Simplify $f(x)$ and state any restrictions.
(c) Find the coordinates of any holes in the graph.
(d) Find any vertical asymptotes.

<details>
<summary>Show Solution</summary>

**Solution**:

**(a)** Factor denominator: $x^2 - x - 2 = (x-2)(x+1)$

Undefined when $x = 2$ or $x = -1$

**Domain**: $(-\infty, -1) \cup (-1, 2) \cup (2, \infty)$

**(b)**
$$f(x) = \frac{(x+2)(x-2)}{(x-2)(x+1)} = \frac{x+2}{x+1}, \quad x \ne 2, -1$$

**(c)** The factor $(x-2)$ canceled, creating a hole at $x = 2$.

Find y-coordinate: $\frac{2+2}{2+1} = \frac{4}{3}$

**Hole at $(2, \frac{4}{3})$**

**(d)** The factor $(x+1)$ in the denominator doesn't cancel.

**Vertical asymptote at $x = -1$**
</details>

---

**Problem 20** *(Free Response Style)*
The expression $\dfrac{x^2 + 5x + 6}{x^2 - 9} \div \dfrac{x + 2}{x^2 - 6x + 9}$ can be simplified.

(a) Perform the division and simplify completely.
(b) State all values excluded from the domain.
(c) Verify your answer by substituting $x = 4$ into both the original and simplified expressions.

<details>
<summary>Show Solution</summary>

**Solution**:

**(a)**
$$= \frac{x^2 + 5x + 6}{x^2 - 9} \cdot \frac{x^2 - 6x + 9}{x + 2}$$

Factor everything:
$$= \frac{(x+2)(x+3)}{(x+3)(x-3)} \cdot \frac{(x-3)^2}{x+2}$$

Cancel common factors:
$$= \frac{(x+2)(x+3)(x-3)^2}{(x+3)(x-3)(x+2)} = x - 3$$

**Simplified**: $x - 3$

**(b)** Excluded values (from original expression):
- $x^2 - 9 = 0$: $x = 3, -3$
- $x + 2 = 0$: $x = -2$
- $x^2 - 6x + 9 = 0$: $x = 3$ (already listed)

**Excluded**: $x = -3, -2, 3$

**(c)** Substitute $x = 4$:

Original:
$$\frac{16 + 20 + 6}{16 - 9} \div \frac{4 + 2}{16 - 24 + 9} = \frac{42}{7} \div \frac{6}{1} = 6 \div 6 = 1$$

Simplified: $4 - 3 = 1$ ✓
</details>

---

## What's Next

Now that you've mastered rational expressions, you're ready to explore [Unit Circle](/calculus/0108-unit-circle), where we'll build the foundation for all of trigonometry by understanding angles and their relationships to coordinates.

---

<div align="center">

[← Solving Equations](/calculus/0106-solving-equations) | [Unit Circle →](/calculus/0108-unit-circle)

</div>
