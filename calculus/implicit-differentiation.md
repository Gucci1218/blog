# Implicit Differentiation

So far, every function we've differentiated has been in **explicit form** — $y$ isolated on one side, like $y = x^2 + 3x$. But what about equations like $x^2 + y^2 = 25$ (a circle)? You can't easily solve for $y$, yet the curve still has tangent lines with slopes. **Implicit differentiation** lets us find $\frac{dy}{dx}$ without solving for $y$ first.

---

## What You'll Learn

- Understand the difference between explicit and implicit functions
- Apply the chain rule to differentiate terms containing $y$
- Find $\frac{dy}{dx}$ for implicitly defined curves
- Calculate slopes of tangent lines to circles, ellipses, and other curves
- Use implicit differentiation to find second derivatives
- Solve AP Calculus problems involving implicit relationships

---

## Prerequisites

- [Chain Rule](/calculus/chain-rule) — essential for understanding why $\frac{d}{dx}[y^2] = 2y \cdot \frac{dy}{dx}$
- [Product Rule](/calculus/product-rule) — needed for terms like $xy$
- [Quotient Rule](/calculus/quotient-rule) — useful for simplifying results

---

## The Core Concept

### Explicit vs. Implicit Functions

**Explicit form:** $y$ is isolated
- $y = x^2 - 4$
- $y = \sin(x)$
- $y = \frac{1}{x+1}$

**Implicit form:** $x$ and $y$ are mixed together
- $x^2 + y^2 = 25$ (circle)
- $x^2 + 4y^2 = 16$ (ellipse)
- $x^3 + y^3 = 6xy$ (folium of Descartes)

### Why Can't We Just Solve for $y$?

Sometimes we can! For $x^2 + y^2 = 25$:

$$y = \pm\sqrt{25 - x^2}$$

But this gives us **two functions** (upper and lower semicircles), and more complex equations might not be solvable at all.

Implicit differentiation gives us $\frac{dy}{dx}$ directly, without isolating $y$.

### The Key Insight: $y$ Depends on $x$

Here's the crucial idea: even though $y$ isn't written as a function of $x$, **we're assuming it is one**. When we differentiate, we treat $y$ as a function $y(x)$.

This means: **every time we differentiate a $y$ term, we must use the chain rule!**

$$\frac{d}{dx}[y^2] = 2y \cdot \frac{dy}{dx}$$

The $\frac{dy}{dx}$ appears because $y$ is a function of $x$ (the "inner function" in the chain rule).

---

## The Process

### Step-by-Step Method

1. **Differentiate both sides** of the equation with respect to $x$
2. **Apply the chain rule** to any term containing $y$ — multiply by $\frac{dy}{dx}$
3. **Collect all $\frac{dy}{dx}$ terms** on one side
4. **Solve for $\frac{dy}{dx}$**

### Key Derivative Rules for Implicit Differentiation

| Expression | Derivative with respect to $x$ |
|------------|-------------------------------|
| $y$ | $\frac{dy}{dx}$ |
| $y^2$ | $2y \cdot \frac{dy}{dx}$ |
| $y^n$ | $ny^{n-1} \cdot \frac{dy}{dx}$ |
| $\sin(y)$ | $\cos(y) \cdot \frac{dy}{dx}$ |
| $e^y$ | $e^y \cdot \frac{dy}{dx}$ |
| $xy$ | $y + x\frac{dy}{dx}$ (product rule) |

---

## Worked Examples

### Example 1: Circle (The Classic)

**Find $\frac{dy}{dx}$ for $x^2 + y^2 = 25$**

**Solution:**

**Step 1:** Differentiate both sides with respect to $x$:

$$\frac{d}{dx}[x^2] + \frac{d}{dx}[y^2] = \frac{d}{dx}[25]$$

**Step 2:** Apply derivatives (chain rule on $y^2$):

$$2x + 2y \cdot \frac{dy}{dx} = 0$$

**Step 3:** Solve for $\frac{dy}{dx}$:

$$2y \cdot \frac{dy}{dx} = -2x$$

$$\frac{dy}{dx} = \frac{-2x}{2y} = -\frac{x}{y}$$

**Answer:** $\frac{dy}{dx} = -\frac{x}{y}$

**Interpretation:** At the point $(3, 4)$ on the circle, the slope is $-\frac{3}{4}$. At $(3, -4)$, the slope is $\frac{3}{4}$.

---

### Example 2: Ellipse

**Find $\frac{dy}{dx}$ for $\frac{x^2}{9} + \frac{y^2}{4} = 1$**

**Solution:**

Rewrite as: $\frac{x^2}{9} + \frac{y^2}{4} = 1$

**Differentiate:**

$$\frac{2x}{9} + \frac{2y}{4} \cdot \frac{dy}{dx} = 0$$

$$\frac{2x}{9} + \frac{y}{2} \cdot \frac{dy}{dx} = 0$$

**Solve for $\frac{dy}{dx}$:**

$$\frac{y}{2} \cdot \frac{dy}{dx} = -\frac{2x}{9}$$

$$\frac{dy}{dx} = -\frac{2x}{9} \cdot \frac{2}{y} = -\frac{4x}{9y}$$

**Answer:** $\frac{dy}{dx} = -\frac{4x}{9y}$

---

### Example 3: Product of $x$ and $y$

**Find $\frac{dy}{dx}$ for $xy = 6$**

**Solution:**

Use the **product rule** on $xy$:

$$\frac{d}{dx}[xy] = \frac{d}{dx}[6]$$

$$x \cdot \frac{dy}{dx} + y \cdot 1 = 0$$

$$x \cdot \frac{dy}{dx} + y = 0$$

**Solve for $\frac{dy}{dx}$:**

$$\frac{dy}{dx} = -\frac{y}{x}$$

**Answer:** $\frac{dy}{dx} = -\frac{y}{x}$

---

### Example 4: Cubic Terms

**Find $\frac{dy}{dx}$ for $x^3 + y^3 = 9$**

**Solution:**

**Differentiate:**

$$3x^2 + 3y^2 \cdot \frac{dy}{dx} = 0$$

**Solve:**

$$3y^2 \cdot \frac{dy}{dx} = -3x^2$$

$$\frac{dy}{dx} = -\frac{x^2}{y^2}$$

**Answer:** $\frac{dy}{dx} = -\frac{x^2}{y^2}$

---

### Example 5: Mixed Terms with Product Rule

**Find $\frac{dy}{dx}$ for $x^2y + xy^2 = 6$**

**Solution:**

Differentiate each term using product rule:

For $x^2y$: $\frac{d}{dx}[x^2y] = 2xy + x^2\frac{dy}{dx}$

For $xy^2$: $\frac{d}{dx}[xy^2] = y^2 + x \cdot 2y\frac{dy}{dx} = y^2 + 2xy\frac{dy}{dx}$

**Full equation:**

$$2xy + x^2\frac{dy}{dx} + y^2 + 2xy\frac{dy}{dx} = 0$$

**Collect $\frac{dy}{dx}$ terms:**

$$x^2\frac{dy}{dx} + 2xy\frac{dy}{dx} = -2xy - y^2$$

$$\frac{dy}{dx}(x^2 + 2xy) = -2xy - y^2$$

$$\frac{dy}{dx} = \frac{-2xy - y^2}{x^2 + 2xy} = \frac{-y(2x + y)}{x(x + 2y)}$$

**Answer:** $\frac{dy}{dx} = -\frac{y(2x + y)}{x(x + 2y)}$

---

### Example 6: Trigonometric Functions

**Find $\frac{dy}{dx}$ for $\sin(y) = x$**

**Solution:**

**Differentiate:**

$$\cos(y) \cdot \frac{dy}{dx} = 1$$

**Solve:**

$$\frac{dy}{dx} = \frac{1}{\cos(y)}$$

Using $\sin(y) = x$, we know $\cos(y) = \sqrt{1 - x^2}$ (for appropriate range):

$$\frac{dy}{dx} = \frac{1}{\sqrt{1 - x^2}}$$

**Answer:** $\frac{dy}{dx} = \frac{1}{\cos(y)} = \frac{1}{\sqrt{1-x^2}}$

*This is the derivative of $\arcsin(x)$!*

---

### Example 7: Finding a Tangent Line

**Find the equation of the tangent line to $x^2 + y^2 = 25$ at the point $(3, 4)$.**

**Solution:**

From Example 1: $\frac{dy}{dx} = -\frac{x}{y}$

**Slope at $(3, 4)$:**

$$m = -\frac{3}{4}$$

**Tangent line (point-slope form):**

$$y - 4 = -\frac{3}{4}(x - 3)$$

$$y = -\frac{3}{4}x + \frac{9}{4} + 4$$

$$y = -\frac{3}{4}x + \frac{25}{4}$$

**Answer:** $y = -\frac{3}{4}x + \frac{25}{4}$

---

### Example 8: Second Derivative

**Find $\frac{d^2y}{dx^2}$ for $x^2 + y^2 = 25$**

**Solution:**

From Example 1: $\frac{dy}{dx} = -\frac{x}{y}$

**Differentiate $\frac{dy}{dx}$ again** using the quotient rule:

$$\frac{d^2y}{dx^2} = \frac{d}{dx}\left[-\frac{x}{y}\right] = -\frac{y \cdot 1 - x \cdot \frac{dy}{dx}}{y^2}$$

**Substitute $\frac{dy}{dx} = -\frac{x}{y}$:**

$$\frac{d^2y}{dx^2} = -\frac{y - x\left(-\frac{x}{y}\right)}{y^2} = -\frac{y + \frac{x^2}{y}}{y^2}$$

$$= -\frac{\frac{y^2 + x^2}{y}}{y^2} = -\frac{y^2 + x^2}{y^3}$$

Since $x^2 + y^2 = 25$:

$$\frac{d^2y}{dx^2} = -\frac{25}{y^3}$$

**Answer:** $\frac{d^2y}{dx^2} = -\frac{25}{y^3}$

---

## Key Formulas & Rules

$$\boxed{\text{For } y \text{ terms: } \frac{d}{dx}[f(y)] = f'(y) \cdot \frac{dy}{dx}}$$

**Common patterns:**

| Original | Derivative |
|----------|------------|
| $y^n$ | $ny^{n-1} \cdot \frac{dy}{dx}$ |
| $\sin(y)$ | $\cos(y) \cdot \frac{dy}{dx}$ |
| $\cos(y)$ | $-\sin(y) \cdot \frac{dy}{dx}$ |
| $e^y$ | $e^y \cdot \frac{dy}{dx}$ |
| $\ln(y)$ | $\frac{1}{y} \cdot \frac{dy}{dx}$ |
| $xy$ | $y + x\frac{dy}{dx}$ |
| $x^2y$ | $2xy + x^2\frac{dy}{dx}$ |

---

## Common Mistakes to Avoid

### Mistake 1: Forgetting $\frac{dy}{dx}$ on $y$ terms

**Wrong:**

$$\frac{d}{dx}[y^2] = 2y \quad \text{✗}$$

**Right:**

$$\frac{d}{dx}[y^2] = 2y \cdot \frac{dy}{dx} \quad \text{✓}$$

This is THE most common error. Every time you differentiate a $y$ term, you must include $\frac{dy}{dx}$.

---

### Mistake 2: Forgetting the Product Rule

For $xy$:

**Wrong:**

$$\frac{d}{dx}[xy] = \frac{dy}{dx} \quad \text{✗}$$

**Right:**

$$\frac{d}{dx}[xy] = x\frac{dy}{dx} + y \quad \text{✓}$$

---

### Mistake 3: Applying $\frac{dy}{dx}$ to $x$ Terms

**Wrong:**

$$\frac{d}{dx}[x^2] = 2x \cdot \frac{dy}{dx} \quad \text{✗}$$

**Right:**

$$\frac{d}{dx}[x^2] = 2x \quad \text{✓}$$

Only $y$ terms get the chain rule treatment with $\frac{dy}{dx}$.

---

### Mistake 4: Not Substituting Back

When asked to evaluate $\frac{dy}{dx}$ at a specific point, don't forget to substitute the coordinates!

---

## AP Exam Tips

### Multiple Choice Strategy

1. **Identify implicit equations** — look for $x$ and $y$ terms mixed together
2. **Differentiate systematically** — term by term, applying chain rule to $y$
3. **Watch for product rule situations** — terms like $xy$, $x^2y$, $xy^2$
4. **Verify your answer** — substitute a point if given

### Free Response Expectations

- **Show every step** of implicit differentiation
- **Explicitly write** "$\frac{dy}{dx}$" when applying the chain rule
- **Box or clearly state** your final answer
- **Simplify** but don't over-simplify (factoring is usually enough)

### Common AP Question Types

1. **Find $\frac{dy}{dx}$** for an implicit equation
2. **Find the slope** at a given point
3. **Write the tangent line equation** at a point on the curve
4. **Find where the tangent is horizontal** (set $\frac{dy}{dx} = 0$)
5. **Find where the tangent is vertical** (set denominator of $\frac{dy}{dx} = 0$)

---

## Practice Problems

### Basic (Problems 1-5)

**1.** Find $\frac{dy}{dx}$:

$$x^2 + y^2 = 100$$

---

**2.** Find $\frac{dy}{dx}$:

$$x^2 - y^2 = 16$$

---

**3.** Find $\frac{dy}{dx}$:

$$3x + 4y = 12$$

---

**4.** Find $\frac{dy}{dx}$:

$$y^3 = x$$

---

**5.** Find $\frac{dy}{dx}$:

$$xy = 10$$

---

### Intermediate (Problems 6-10)

**6.** Find $\frac{dy}{dx}$:

$$x^2 + xy + y^2 = 7$$

---

**7.** Find $\frac{dy}{dx}$:

$$\sqrt{x} + \sqrt{y} = 4$$

---

**8.** Find $\frac{dy}{dx}$:

$$x^3 + y^3 = 6xy$$

*(This is the folium of Descartes)*

---

**9.** Find the slope of the tangent to $x^2 + y^2 = 25$ at the point $(4, 3)$.

---

**10.** Find $\frac{dy}{dx}$:

$$\cos(y) = x$$

---

### Advanced (Problems 11-15)

**11.** Find the equation of the tangent line to:

$$x^2 + 4y^2 = 8$$

at the point $(2, 1)$.

---

**12.** Find $\frac{dy}{dx}$:

$$e^{xy} = x + y$$

---

**13.** Find all points on:

$$x^2 + y^2 = 25$$

where the tangent line is horizontal.

---

**14.** Find $\frac{d^2y}{dx^2}$ for:

$$x^2 - y^2 = 16$$

---

**15.** Find $\frac{dy}{dx}$:

$$\sin(x + y) = y^2\cos(x)$$

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

Given $x^2y - y^3 = 8$, find $\frac{dy}{dx}$.

| Choice | Answer |
|--------|--------|
| **(A)** | $\frac{2xy}{3y^2 - x^2}$ |
| **(B)** | $\frac{2xy}{x^2 - 3y^2}$ |
| **(C)** | $\frac{-2xy}{3y^2 - x^2}$ |
| **(D)** | $\frac{-2xy}{x^2 + 3y^2}$ |

---

#### Problem 17 (Multiple Choice)

The curve $x^2 + xy + y^2 = 3$ passes through $(1, 1)$. Find the slope of the tangent at this point.

| Choice | Answer |
|--------|--------|
| **(A)** | $-1$ |
| **(B)** | $0$ |
| **(C)** | $1$ |
| **(D)** | $-\frac{1}{3}$ |

---

#### Problem 18 (Free Response)

Consider the curve defined by $x^3 + y^3 = 9xy$.

> **(a)** Find $\frac{dy}{dx}$ in terms of $x$ and $y$.
>
> **(b)** Find the equation of the tangent line at the point $(2, 4)$.
>
> **(c)** At what point(s) other than the origin does the curve have a horizontal tangent?

---

#### Problem 19 (Multiple Choice)

If $\sin(xy) = y$, what is $\frac{dy}{dx}$?

| Choice | Answer |
|--------|--------|
| **(A)** | $\frac{y\cos(xy)}{1 - x\cos(xy)}$ |
| **(B)** | $\frac{y\cos(xy)}{1 + x\cos(xy)}$ |
| **(C)** | $\frac{-y\cos(xy)}{1 - x\cos(xy)}$ |
| **(D)** | $\frac{\cos(xy)}{1 - x\cos(xy)}$ |

---

#### Problem 20 (Free Response - Challenging)

The curve $y^2 = x^3 - 4x$ is called a **cubic curve**.

> **(a)** Find $\frac{dy}{dx}$.
>
> **(b)** Find all points where the tangent line is vertical.
>
> **(c)** Show that the tangent line at $(2, 0)$ does not exist, and explain geometrically why.

---

## Solutions

<details>
<summary><strong>Solution 1</strong></summary>

**Problem:** $x^2 + y^2 = 100$

**Differentiate both sides:**

$$2x + 2y\frac{dy}{dx} = 0$$

**Solve:**

$$\frac{dy}{dx} = -\frac{x}{y}$$

**Answer:** $\frac{dy}{dx} = -\frac{x}{y}$

</details>

---

<details>
<summary><strong>Solution 2</strong></summary>

**Problem:** $x^2 - y^2 = 16$

**Differentiate:**

$$2x - 2y\frac{dy}{dx} = 0$$

**Solve:**

$$\frac{dy}{dx} = \frac{x}{y}$$

**Answer:** $\frac{dy}{dx} = \frac{x}{y}$

</details>

---

<details>
<summary><strong>Solution 3</strong></summary>

**Problem:** $3x + 4y = 12$

**Differentiate:**

$$3 + 4\frac{dy}{dx} = 0$$

**Solve:**

$$\frac{dy}{dx} = -\frac{3}{4}$$

**Answer:** $\frac{dy}{dx} = -\frac{3}{4}$

*Note: This is a line, so the slope is constant.*

</details>

---

<details>
<summary><strong>Solution 4</strong></summary>

**Problem:** $y^3 = x$

**Differentiate:**

$$3y^2\frac{dy}{dx} = 1$$

**Solve:**

$$\frac{dy}{dx} = \frac{1}{3y^2}$$

**Answer:** $\frac{dy}{dx} = \frac{1}{3y^2}$

</details>

---

<details>
<summary><strong>Solution 5</strong></summary>

**Problem:** $xy = 10$

**Use product rule:**

$$x\frac{dy}{dx} + y = 0$$

**Solve:**

$$\frac{dy}{dx} = -\frac{y}{x}$$

**Answer:** $\frac{dy}{dx} = -\frac{y}{x}$

</details>

---

<details>
<summary><strong>Solution 6</strong></summary>

**Problem:** $x^2 + xy + y^2 = 7$

**Differentiate term by term:**

$$2x + \left(x\frac{dy}{dx} + y\right) + 2y\frac{dy}{dx} = 0$$

**Collect $\frac{dy}{dx}$ terms:**

$$x\frac{dy}{dx} + 2y\frac{dy}{dx} = -2x - y$$

$$\frac{dy}{dx}(x + 2y) = -2x - y$$

**Solve:**

$$\frac{dy}{dx} = \frac{-2x - y}{x + 2y}$$

**Answer:** $\frac{dy}{dx} = -\frac{2x + y}{x + 2y}$

</details>

---

<details>
<summary><strong>Solution 7</strong></summary>

**Problem:** $\sqrt{x} + \sqrt{y} = 4$

Rewrite: $x^{1/2} + y^{1/2} = 4$

**Differentiate:**

$$\frac{1}{2}x^{-1/2} + \frac{1}{2}y^{-1/2}\frac{dy}{dx} = 0$$

$$\frac{1}{2\sqrt{x}} + \frac{1}{2\sqrt{y}}\frac{dy}{dx} = 0$$

**Solve:**

$$\frac{dy}{dx} = -\frac{\sqrt{y}}{\sqrt{x}} = -\sqrt{\frac{y}{x}}$$

**Answer:** $\frac{dy}{dx} = -\sqrt{\frac{y}{x}}$

</details>

---

<details>
<summary><strong>Solution 8</strong></summary>

**Problem:** $x^3 + y^3 = 6xy$ (Folium of Descartes)

**Differentiate:**

$$3x^2 + 3y^2\frac{dy}{dx} = 6\left(y + x\frac{dy}{dx}\right)$$

$$3x^2 + 3y^2\frac{dy}{dx} = 6y + 6x\frac{dy}{dx}$$

**Collect terms:**

$$3y^2\frac{dy}{dx} - 6x\frac{dy}{dx} = 6y - 3x^2$$

$$\frac{dy}{dx}(3y^2 - 6x) = 6y - 3x^2$$

**Solve:**

$$\frac{dy}{dx} = \frac{6y - 3x^2}{3y^2 - 6x} = \frac{2y - x^2}{y^2 - 2x}$$

**Answer:** $\frac{dy}{dx} = \frac{2y - x^2}{y^2 - 2x}$

</details>

---

<details>
<summary><strong>Solution 9</strong></summary>

**Problem:** Slope at $(4, 3)$ on $x^2 + y^2 = 25$

From earlier: $\frac{dy}{dx} = -\frac{x}{y}$

**Substitute $(4, 3)$:**

$$\frac{dy}{dx} = -\frac{4}{3}$$

**Answer:** Slope $= -\frac{4}{3}$

</details>

---

<details>
<summary><strong>Solution 10</strong></summary>

**Problem:** $\cos(y) = x$

**Differentiate:**

$$-\sin(y)\frac{dy}{dx} = 1$$

**Solve:**

$$\frac{dy}{dx} = -\frac{1}{\sin(y)}$$

Using $\cos(y) = x$, so $\sin(y) = \sqrt{1-x^2}$:

$$\frac{dy}{dx} = -\frac{1}{\sqrt{1-x^2}}$$

**Answer:** $\frac{dy}{dx} = -\frac{1}{\sin(y)} = -\frac{1}{\sqrt{1-x^2}}$

*This is the derivative of $\arccos(x)$!*

</details>

---

<details>
<summary><strong>Solution 11</strong></summary>

**Problem:** Tangent to $x^2 + 4y^2 = 8$ at $(2, 1)$

**Differentiate:**

$$2x + 8y\frac{dy}{dx} = 0$$

$$\frac{dy}{dx} = -\frac{x}{4y}$$

**At $(2, 1)$:**

$$m = -\frac{2}{4(1)} = -\frac{1}{2}$$

**Tangent line:**

$$y - 1 = -\frac{1}{2}(x - 2)$$

$$y = -\frac{1}{2}x + 2$$

**Answer:** $y = -\frac{1}{2}x + 2$

</details>

---

<details>
<summary><strong>Solution 12</strong></summary>

**Problem:** $e^{xy} = x + y$

**Differentiate (chain rule on left, sum on right):**

$$e^{xy}\left(y + x\frac{dy}{dx}\right) = 1 + \frac{dy}{dx}$$

**Expand:**

$$ye^{xy} + xe^{xy}\frac{dy}{dx} = 1 + \frac{dy}{dx}$$

**Collect $\frac{dy}{dx}$:**

$$xe^{xy}\frac{dy}{dx} - \frac{dy}{dx} = 1 - ye^{xy}$$

$$\frac{dy}{dx}(xe^{xy} - 1) = 1 - ye^{xy}$$

**Solve:**

$$\frac{dy}{dx} = \frac{1 - ye^{xy}}{xe^{xy} - 1}$$

**Answer:** $\frac{dy}{dx} = \frac{1 - ye^{xy}}{xe^{xy} - 1}$

</details>

---

<details>
<summary><strong>Solution 13</strong></summary>

**Problem:** Horizontal tangents on $x^2 + y^2 = 25$

**Horizontal tangent means $\frac{dy}{dx} = 0$:**

$$-\frac{x}{y} = 0$$

This requires $x = 0$.

**Substitute into original equation:**

$$0 + y^2 = 25$$

$$y = \pm 5$$

**Answer:** $(0, 5)$ and $(0, -5)$

</details>

---

<details>
<summary><strong>Solution 14</strong></summary>

**Problem:** $\frac{d^2y}{dx^2}$ for $x^2 - y^2 = 16$

**First derivative:**

$$2x - 2y\frac{dy}{dx} = 0 \Rightarrow \frac{dy}{dx} = \frac{x}{y}$$

**Second derivative (quotient rule):**

$$\frac{d^2y}{dx^2} = \frac{y \cdot 1 - x \cdot \frac{dy}{dx}}{y^2}$$

**Substitute $\frac{dy}{dx} = \frac{x}{y}$:**

$$= \frac{y - x \cdot \frac{x}{y}}{y^2} = \frac{y - \frac{x^2}{y}}{y^2} = \frac{\frac{y^2 - x^2}{y}}{y^2} = \frac{y^2 - x^2}{y^3}$$

Since $x^2 - y^2 = 16$, we have $y^2 - x^2 = -16$:

$$\frac{d^2y}{dx^2} = \frac{-16}{y^3}$$

**Answer:** $\frac{d^2y}{dx^2} = -\frac{16}{y^3}$

</details>

---

<details>
<summary><strong>Solution 15</strong></summary>

**Problem:** $\sin(x + y) = y^2\cos(x)$

**Differentiate (chain rule on left, product rule on right):**

$$\cos(x + y)\left(1 + \frac{dy}{dx}\right) = 2y\frac{dy}{dx}\cos(x) + y^2(-\sin(x))$$

**Expand left side:**

$$\cos(x + y) + \cos(x + y)\frac{dy}{dx} = 2y\cos(x)\frac{dy}{dx} - y^2\sin(x)$$

**Collect $\frac{dy}{dx}$:**

$$\cos(x + y)\frac{dy}{dx} - 2y\cos(x)\frac{dy}{dx} = -y^2\sin(x) - \cos(x + y)$$

$$\frac{dy}{dx}[\cos(x + y) - 2y\cos(x)] = -y^2\sin(x) - \cos(x + y)$$

**Solve:**

$$\frac{dy}{dx} = \frac{-y^2\sin(x) - \cos(x + y)}{\cos(x + y) - 2y\cos(x)}$$

**Answer:** $\frac{dy}{dx} = \frac{-y^2\sin(x) - \cos(x + y)}{\cos(x + y) - 2y\cos(x)}$

</details>

---

<details>
<summary><strong>Solution 16</strong></summary>

**Problem:** $x^2y - y^3 = 8$

**Differentiate:**

$$2xy + x^2\frac{dy}{dx} - 3y^2\frac{dy}{dx} = 0$$

**Collect terms:**

$$\frac{dy}{dx}(x^2 - 3y^2) = -2xy$$

$$\frac{dy}{dx} = \frac{-2xy}{x^2 - 3y^2} = \frac{2xy}{3y^2 - x^2}$$

**Answer:** **(A)** $\frac{2xy}{3y^2 - x^2}$

</details>

---

<details>
<summary><strong>Solution 17</strong></summary>

**Problem:** $x^2 + xy + y^2 = 3$ at $(1, 1)$

From Solution 6: $\frac{dy}{dx} = -\frac{2x + y}{x + 2y}$

**At $(1, 1)$:**

$$\frac{dy}{dx} = -\frac{2(1) + 1}{1 + 2(1)} = -\frac{3}{3} = -1$$

**Answer:** **(A)** $-1$

</details>

---

<details>
<summary><strong>Solution 18</strong></summary>

**Problem:** $x^3 + y^3 = 9xy$

**(a) Find $\frac{dy}{dx}$:**

**Differentiate:**

$$3x^2 + 3y^2\frac{dy}{dx} = 9y + 9x\frac{dy}{dx}$$

$$3y^2\frac{dy}{dx} - 9x\frac{dy}{dx} = 9y - 3x^2$$

$$\frac{dy}{dx} = \frac{9y - 3x^2}{3y^2 - 9x} = \frac{3y - x^2}{y^2 - 3x}$$

**Answer (a):** $\frac{dy}{dx} = \frac{3y - x^2}{y^2 - 3x}$

**(b) Tangent at $(2, 4)$:**

$$m = \frac{3(4) - 4}{16 - 6} = \frac{8}{10} = \frac{4}{5}$$

$$y - 4 = \frac{4}{5}(x - 2)$$

$$y = \frac{4}{5}x + \frac{12}{5}$$

**Answer (b):** $y = \frac{4}{5}x + \frac{12}{5}$

**(c) Horizontal tangent (other than origin):**

Set numerator $= 0$: $3y - x^2 = 0$, so $y = \frac{x^2}{3}$

Substitute into original: $x^3 + \frac{x^6}{27} = 9x \cdot \frac{x^2}{3} = 3x^3$

$$x^3 + \frac{x^6}{27} = 3x^3$$

$$\frac{x^6}{27} = 2x^3$$

$$x^6 = 54x^3$$

$$x^3(x^3 - 54) = 0$$

$x = 0$ or $x = \sqrt[3]{54} = 3\sqrt[3]{2}$

For $x = 3\sqrt[3]{2}$: $y = \frac{(3\sqrt[3]{2})^2}{3} = \frac{9\sqrt[3]{4}}{3} = 3\sqrt[3]{4}$

**Answer (c):** $(3\sqrt[3]{2}, 3\sqrt[3]{4})$

</details>

---

<details>
<summary><strong>Solution 19</strong></summary>

**Problem:** $\sin(xy) = y$

**Differentiate:**

$$\cos(xy)\left(y + x\frac{dy}{dx}\right) = \frac{dy}{dx}$$

$$y\cos(xy) + x\cos(xy)\frac{dy}{dx} = \frac{dy}{dx}$$

**Collect $\frac{dy}{dx}$:**

$$y\cos(xy) = \frac{dy}{dx} - x\cos(xy)\frac{dy}{dx}$$

$$y\cos(xy) = \frac{dy}{dx}(1 - x\cos(xy))$$

$$\frac{dy}{dx} = \frac{y\cos(xy)}{1 - x\cos(xy)}$$

**Answer:** **(A)** $\frac{y\cos(xy)}{1 - x\cos(xy)}$

</details>

---

<details>
<summary><strong>Solution 20</strong></summary>

**Problem:** $y^2 = x^3 - 4x$

**(a) Find $\frac{dy}{dx}$:**

$$2y\frac{dy}{dx} = 3x^2 - 4$$

$$\frac{dy}{dx} = \frac{3x^2 - 4}{2y}$$

**Answer (a):** $\frac{dy}{dx} = \frac{3x^2 - 4}{2y}$

**(b) Vertical tangent (denominator = 0):**

$2y = 0 \Rightarrow y = 0$

Substitute: $0 = x^3 - 4x = x(x^2 - 4) = x(x-2)(x+2)$

$x = 0, 2, -2$

Points: $(0, 0)$, $(2, 0)$, $(-2, 0)$

**Answer (b):** $(0, 0)$, $(2, 0)$, $(-2, 0)$

**(c) At $(2, 0)$:**

$\frac{dy}{dx} = \frac{3(4) - 4}{2(0)} = \frac{8}{0}$ — undefined!

**Geometric explanation:** At $(2, 0)$, the curve has a **vertical tangent**. The curve crosses the x-axis and the tangent line is vertical (undefined slope). Geometrically, the curve $y^2 = x^3 - 4x$ passes through $(2, 0)$ with a vertical tangent — the curve comes from above and below, meeting at this point.

**Answer (c):** The tangent doesn't exist because the slope is undefined ($\frac{8}{0}$). Geometrically, the tangent line is vertical at this point.

</details>

---

## What's Next

Now that you can differentiate implicit equations, you're ready to explore [Derivatives of Trigonometric Functions](/calculus/derivatives-trig), which will give you powerful tools for differentiating sine, cosine, tangent, and their inverses.

---

<div align="center">

[← Chain Rule](/calculus/chain-rule) | [Trig Derivatives →](/calculus/derivatives-trig)

</div>
