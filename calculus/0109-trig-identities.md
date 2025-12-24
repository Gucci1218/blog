# Trigonometric Identities
<p class="article-date">July 23, 2024</p>

## Prerequisites
Before diving in, make sure you're comfortable with:
- [Unit Circle](/calculus/0108-unit-circle)
- Basic algebraic manipulation
- Factoring techniques

## Learning Objectives
By the end of this section, you will be able to:
- Apply the Pythagorean identities
- Use reciprocal and quotient identities
- Simplify expressions using sum and difference formulas
- Apply double-angle and half-angle formulas
- Verify trigonometric identities
- Solve trigonometric equations

## The Big Picture: Why Identities?

Trig identities are equations that are true for ALL valid values of the variable. They allow us to:
- Simplify complex expressions
- Solve trig equations
- Evaluate integrals in calculus
- Transform expressions into more useful forms

> **Calculus Connection**: You'll use identities to simplify derivatives, evaluate integrals, and solve differential equations.

## The Fundamental Identities

### Pythagorean Identities

From the unit circle equation $x^2 + y^2 = 1$:

$$\sin^2\theta + \cos^2\theta = 1$$

Divide by $\cos^2\theta$:
$$\tan^2\theta + 1 = \sec^2\theta$$

Divide by $\sin^2\theta$:
$$1 + \cot^2\theta = \csc^2\theta$$

### Reciprocal Identities

$$\csc\theta = \frac{1}{\sin\theta}, \quad \sec\theta = \frac{1}{\cos\theta}, \quad \cot\theta = \frac{1}{\tan\theta}$$

### Quotient Identities

$$\tan\theta = \frac{\sin\theta}{\cos\theta}, \quad \cot\theta = \frac{\cos\theta}{\sin\theta}$$

### Even-Odd Identities

$$\cos(-\theta) = \cos\theta \quad \text{(even)}$$
$$\sin(-\theta) = -\sin\theta \quad \text{(odd)}$$
$$\tan(-\theta) = -\tan\theta \quad \text{(odd)}$$

### Cofunction Identities

$$\sin\left(\frac{\pi}{2} - \theta\right) = \cos\theta, \quad \cos\left(\frac{\pi}{2} - \theta\right) = \sin\theta$$
$$\tan\left(\frac{\pi}{2} - \theta\right) = \cot\theta, \quad \cot\left(\frac{\pi}{2} - \theta\right) = \tan\theta$$

## Sum and Difference Formulas

$$\sin(A + B) = \sin A \cos B + \cos A \sin B$$
$$\sin(A - B) = \sin A \cos B - \cos A \sin B$$

$$\cos(A + B) = \cos A \cos B - \sin A \sin B$$
$$\cos(A - B) = \cos A \cos B + \sin A \sin B$$

$$\tan(A + B) = \frac{\tan A + \tan B}{1 - \tan A \tan B}$$
$$\tan(A - B) = \frac{\tan A - \tan B}{1 + \tan A \tan B}$$

> **Memory Tip**: For sine, the sign in the middle matches the original. For cosine, it's opposite.

## Double-Angle Formulas

$$\sin(2\theta) = 2\sin\theta\cos\theta$$

$$\cos(2\theta) = \cos^2\theta - \sin^2\theta = 2\cos^2\theta - 1 = 1 - 2\sin^2\theta$$

$$\tan(2\theta) = \frac{2\tan\theta}{1 - \tan^2\theta}$$

### Derivation
Set $A = B = \theta$ in the sum formulas:
- $\sin(2\theta) = \sin\theta\cos\theta + \cos\theta\sin\theta = 2\sin\theta\cos\theta$
- $\cos(2\theta) = \cos\theta\cos\theta - \sin\theta\sin\theta = \cos^2\theta - \sin^2\theta$

## Half-Angle Formulas

$$\sin\frac{\theta}{2} = \pm\sqrt{\frac{1 - \cos\theta}{2}}$$

$$\cos\frac{\theta}{2} = \pm\sqrt{\frac{1 + \cos\theta}{2}}$$

$$\tan\frac{\theta}{2} = \frac{1 - \cos\theta}{\sin\theta} = \frac{\sin\theta}{1 + \cos\theta}$$

The sign depends on the quadrant of $\frac{\theta}{2}$.

## Power-Reducing Formulas

$$\sin^2\theta = \frac{1 - \cos(2\theta)}{2}$$

$$\cos^2\theta = \frac{1 + \cos(2\theta)}{2}$$

$$\tan^2\theta = \frac{1 - \cos(2\theta)}{1 + \cos(2\theta)}$$

> **Calculus Connection**: These are essential for integrating even powers of sine and cosine.

## Product-to-Sum Formulas

$$\sin A \cos B = \frac{1}{2}[\sin(A+B) + \sin(A-B)]$$

$$\cos A \cos B = \frac{1}{2}[\cos(A-B) + \cos(A+B)]$$

$$\sin A \sin B = \frac{1}{2}[\cos(A-B) - \cos(A+B)]$$

## Sum-to-Product Formulas

$$\sin A + \sin B = 2\sin\frac{A+B}{2}\cos\frac{A-B}{2}$$

$$\sin A - \sin B = 2\cos\frac{A+B}{2}\sin\frac{A-B}{2}$$

$$\cos A + \cos B = 2\cos\frac{A+B}{2}\cos\frac{A-B}{2}$$

$$\cos A - \cos B = -2\sin\frac{A+B}{2}\sin\frac{A-B}{2}$$

## Strategies for Verifying Identities

1. **Work on one side only** (usually the more complex side)
2. **Convert everything to sine and cosine** when stuck
3. **Factor when possible**
4. **Multiply by conjugates** for expressions like $1 + \sin\theta$
5. **Use Pythagorean identities** to eliminate squares
6. **Look for patterns** (double angles, sum/difference)

## Worked Example 1: Simplifying

**Problem**: Simplify $\dfrac{\sin^2\theta}{\cos^2\theta} + 1$

**Solution**:
$$= \tan^2\theta + 1 = \sec^2\theta$$

## Worked Example 2: Verifying an Identity

**Problem**: Verify $\dfrac{1 + \tan^2\theta}{\csc^2\theta} = \tan^2\theta$

**Solution** (work on left side):
$$\frac{1 + \tan^2\theta}{\csc^2\theta} = \frac{\sec^2\theta}{\csc^2\theta}$$

$$= \frac{1/\cos^2\theta}{1/\sin^2\theta} = \frac{\sin^2\theta}{\cos^2\theta} = \tan^2\theta$$ ✓

## Worked Example 3: Using Sum Formula

**Problem**: Find $\sin 75°$ exactly.

**Solution**:
$$\sin 75° = \sin(45° + 30°)$$
$$= \sin 45°\cos 30° + \cos 45°\sin 30°$$
$$= \frac{\sqrt{2}}{2} \cdot \frac{\sqrt{3}}{2} + \frac{\sqrt{2}}{2} \cdot \frac{1}{2}$$
$$= \frac{\sqrt{6}}{4} + \frac{\sqrt{2}}{4} = \frac{\sqrt{6} + \sqrt{2}}{4}$$

## Worked Example 4: Double Angle

**Problem**: If $\cos\theta = \frac{3}{5}$ and $\theta$ is in Quadrant I, find $\sin(2\theta)$.

**Solution**:
Find $\sin\theta$: $\sin\theta = \sqrt{1 - \frac{9}{25}} = \frac{4}{5}$

$$\sin(2\theta) = 2\sin\theta\cos\theta = 2 \cdot \frac{4}{5} \cdot \frac{3}{5} = \frac{24}{25}$$

## Worked Example 5: Solving Trig Equation

**Problem**: Solve $2\sin^2\theta - 1 = 0$ for $\theta \in [0, 2\pi)$.

**Solution**:
$$\sin^2\theta = \frac{1}{2}$$
$$\sin\theta = \pm\frac{1}{\sqrt{2}} = \pm\frac{\sqrt{2}}{2}$$

Solutions: $\theta = \frac{\pi}{4}, \frac{3\pi}{4}, \frac{5\pi}{4}, \frac{7\pi}{4}$

## Key Formulas Summary

| Identity Type | Formula |
|---------------|---------|
| Pythagorean | $\sin^2\theta + \cos^2\theta = 1$ |
| Pythagorean | $\tan^2\theta + 1 = \sec^2\theta$ |
| Pythagorean | $1 + \cot^2\theta = \csc^2\theta$ |
| Double Angle | $\sin 2\theta = 2\sin\theta\cos\theta$ |
| Double Angle | $\cos 2\theta = \cos^2\theta - \sin^2\theta$ |
| Power Reducing | $\sin^2\theta = \frac{1 - \cos 2\theta}{2}$ |
| Power Reducing | $\cos^2\theta = \frac{1 + \cos 2\theta}{2}$ |

## Common Mistakes to Avoid

1. **Wrong signs in sum/difference formulas**
   - $\sin(A+B)$: plus in middle
   - $\cos(A+B)$: minus in middle

2. **Forgetting the 2 in double-angle formulas**
   - $\sin 2\theta = 2\sin\theta\cos\theta$, not $\sin\theta\cos\theta$

3. **Squaring both sides incorrectly**
   - $(\sin\theta + \cos\theta)^2 \ne \sin^2\theta + \cos^2\theta$

4. **Confusing $\sin^2\theta$ with $\sin(\theta^2)$**
   - $\sin^2\theta = (\sin\theta)^2$

5. **Losing solutions when dividing by trig functions**
   - Check if the function could be zero first

## Calculus Connection

Trig identities are essential for:

1. **Integration**: $\int \sin^2 x \, dx$ requires power-reducing formula
2. **Derivatives**: Simplifying before differentiating
3. **Limits**: Rewriting to eliminate indeterminate forms
4. **Differential Equations**: Solving trig-based DEs

---

## Practice Problems

### Basic (Computational)

**Problem 1**
Simplify: $\sin^2\theta + \cos^2\theta + \tan^2\theta$

<details>
<summary>Show Solution</summary>

**Solution**:
$$= 1 + \tan^2\theta = \sec^2\theta$$
</details>

---

**Problem 2**
Simplify: $\dfrac{\sin\theta}{\csc\theta}$

<details>
<summary>Show Solution</summary>

**Solution**:
$$= \sin\theta \cdot \sin\theta = \sin^2\theta$$
</details>

---

**Problem 3**
Find $\cos 15°$ using a difference formula.

<details>
<summary>Show Solution</summary>

**Solution**:
$$\cos 15° = \cos(45° - 30°)$$
$$= \cos 45°\cos 30° + \sin 45°\sin 30°$$
$$= \frac{\sqrt{2}}{2} \cdot \frac{\sqrt{3}}{2} + \frac{\sqrt{2}}{2} \cdot \frac{1}{2}$$
$$= \frac{\sqrt{6} + \sqrt{2}}{4}$$
</details>

---

**Problem 4**
Use a double-angle formula to find $\cos 120°$.

<details>
<summary>Show Solution</summary>

**Solution**:
$$\cos 120° = \cos(2 \cdot 60°) = 2\cos^2 60° - 1$$
$$= 2 \cdot \frac{1}{4} - 1 = \frac{1}{2} - 1 = -\frac{1}{2}$$
</details>

---

**Problem 5**
Express $\sin^2 x$ without powers using a power-reducing formula.

<details>
<summary>Show Solution</summary>

**Solution**:
$$\sin^2 x = \frac{1 - \cos 2x}{2}$$
</details>

---

### Intermediate (Multi-step)

**Problem 6**
Verify: $\dfrac{\sin\theta}{1 + \cos\theta} = \dfrac{1 - \cos\theta}{\sin\theta}$

<details>
<summary>Show Solution</summary>

**Solution**:
Cross multiply and verify:
$$\sin\theta \cdot \sin\theta = (1 + \cos\theta)(1 - \cos\theta)$$
$$\sin^2\theta = 1 - \cos^2\theta$$
$$\sin^2\theta = \sin^2\theta$$ ✓
</details>

---

**Problem 7**
If $\tan\theta = \frac{3}{4}$ and $\theta$ is in Quadrant III, find $\sin 2\theta$.

<details>
<summary>Show Solution</summary>

**Solution**:
In Q3: $\sin\theta = -\frac{3}{5}$, $\cos\theta = -\frac{4}{5}$ (from 3-4-5 triangle)

$$\sin 2\theta = 2\sin\theta\cos\theta = 2 \cdot \left(-\frac{3}{5}\right) \cdot \left(-\frac{4}{5}\right) = \frac{24}{25}$$
</details>

---

**Problem 8**
Simplify: $\cos^4\theta - \sin^4\theta$

<details>
<summary>Show Solution</summary>

**Solution**:
Factor as difference of squares:
$$= (\cos^2\theta + \sin^2\theta)(\cos^2\theta - \sin^2\theta)$$
$$= 1 \cdot \cos 2\theta = \cos 2\theta$$
</details>

---

**Problem 9**
Solve: $\cos 2\theta = \cos\theta$ for $\theta \in [0, 2\pi)$.

<details>
<summary>Show Solution</summary>

**Solution**:
$$2\cos^2\theta - 1 = \cos\theta$$
$$2\cos^2\theta - \cos\theta - 1 = 0$$
$$(2\cos\theta + 1)(\cos\theta - 1) = 0$$

$\cos\theta = -\frac{1}{2}$: $\theta = \frac{2\pi}{3}, \frac{4\pi}{3}$

$\cos\theta = 1$: $\theta = 0$

**Solutions**: $\theta = 0, \frac{2\pi}{3}, \frac{4\pi}{3}$
</details>

---

**Problem 10**
Verify: $\tan\theta + \cot\theta = \dfrac{2}{\sin 2\theta}$

<details>
<summary>Show Solution</summary>

**Solution**:
$$\tan\theta + \cot\theta = \frac{\sin\theta}{\cos\theta} + \frac{\cos\theta}{\sin\theta}$$
$$= \frac{\sin^2\theta + \cos^2\theta}{\sin\theta\cos\theta} = \frac{1}{\sin\theta\cos\theta}$$

Since $\sin 2\theta = 2\sin\theta\cos\theta$:
$$= \frac{1}{\frac{\sin 2\theta}{2}} = \frac{2}{\sin 2\theta}$$ ✓
</details>

---

### Advanced (Complex Applications)

**Problem 11**
Verify: $\dfrac{1 - \cos 2\theta}{\sin 2\theta} = \tan\theta$

<details>
<summary>Show Solution</summary>

**Solution**:
$$\frac{1 - \cos 2\theta}{\sin 2\theta} = \frac{1 - (1 - 2\sin^2\theta)}{2\sin\theta\cos\theta}$$
$$= \frac{2\sin^2\theta}{2\sin\theta\cos\theta} = \frac{\sin\theta}{\cos\theta} = \tan\theta$$ ✓
</details>

---

**Problem 12**
Find $\sin 3\theta$ in terms of $\sin\theta$.

<details>
<summary>Show Solution</summary>

**Solution**:
$$\sin 3\theta = \sin(2\theta + \theta)$$
$$= \sin 2\theta \cos\theta + \cos 2\theta \sin\theta$$
$$= 2\sin\theta\cos\theta \cdot \cos\theta + (1 - 2\sin^2\theta)\sin\theta$$
$$= 2\sin\theta\cos^2\theta + \sin\theta - 2\sin^3\theta$$
$$= 2\sin\theta(1 - \sin^2\theta) + \sin\theta - 2\sin^3\theta$$
$$= 2\sin\theta - 2\sin^3\theta + \sin\theta - 2\sin^3\theta$$
$$= 3\sin\theta - 4\sin^3\theta$$
</details>

---

**Problem 13**
Solve: $\sin\theta + \cos\theta = 1$ for $\theta \in [0, 2\pi)$.

<details>
<summary>Show Solution</summary>

**Solution**:
Square both sides:
$$\sin^2\theta + 2\sin\theta\cos\theta + \cos^2\theta = 1$$
$$1 + \sin 2\theta = 1$$
$$\sin 2\theta = 0$$
$$2\theta = 0, \pi, 2\pi, 3\pi$$
$$\theta = 0, \frac{\pi}{2}, \pi, \frac{3\pi}{2}$$

Check each in original:
- $\theta = 0$: $0 + 1 = 1$ ✓
- $\theta = \frac{\pi}{2}$: $1 + 0 = 1$ ✓
- $\theta = \pi$: $0 + (-1) = -1$ ✗
- $\theta = \frac{3\pi}{2}$: $-1 + 0 = -1$ ✗

**Solutions**: $\theta = 0, \frac{\pi}{2}$
</details>

---

**Problem 14**
Express $\cos^4 x$ without powers.

<details>
<summary>Show Solution</summary>

**Solution**:
$$\cos^4 x = (\cos^2 x)^2 = \left(\frac{1 + \cos 2x}{2}\right)^2$$
$$= \frac{1 + 2\cos 2x + \cos^2 2x}{4}$$
$$= \frac{1 + 2\cos 2x + \frac{1 + \cos 4x}{2}}{4}$$
$$= \frac{2 + 4\cos 2x + 1 + \cos 4x}{8}$$
$$= \frac{3 + 4\cos 2x + \cos 4x}{8}$$
</details>

---

**Problem 15**
If $\sin\alpha = \frac{4}{5}$ (Q1) and $\cos\beta = \frac{5}{13}$ (Q1), find $\sin(\alpha + \beta)$.

<details>
<summary>Show Solution</summary>

**Solution**:
Find missing values:
- $\cos\alpha = \frac{3}{5}$ (from 3-4-5)
- $\sin\beta = \frac{12}{13}$ (from 5-12-13)

$$\sin(\alpha + \beta) = \sin\alpha\cos\beta + \cos\alpha\sin\beta$$
$$= \frac{4}{5} \cdot \frac{5}{13} + \frac{3}{5} \cdot \frac{12}{13}$$
$$= \frac{20}{65} + \frac{36}{65} = \frac{56}{65}$$
</details>

---

### AP Exam Style

**Problem 16**
Simplify $\dfrac{1 - \cos^2\theta}{\sin\theta}$ to a single trig function.

<details>
<summary>Show Solution</summary>

**Solution**:
$$\frac{1 - \cos^2\theta}{\sin\theta} = \frac{\sin^2\theta}{\sin\theta} = \sin\theta$$
</details>

---

**Problem 17**
Which expression equals $\cos^2\theta - \sin^2\theta$?

(A) $1$
(B) $\cos 2\theta$
(C) $\sin 2\theta$
(D) $2\cos\theta$

<details>
<summary>Show Solution</summary>

**Solution**:
By the double-angle formula for cosine:
$$\cos 2\theta = \cos^2\theta - \sin^2\theta$$

**Answer: (B)**
</details>

---

**Problem 18**
Solve $2\sin\theta\cos\theta = \cos\theta$ for $\theta \in [0, 2\pi)$.

<details>
<summary>Show Solution</summary>

**Solution**:
$$\cos\theta(2\sin\theta - 1) = 0$$

$\cos\theta = 0$: $\theta = \frac{\pi}{2}, \frac{3\pi}{2}$

$\sin\theta = \frac{1}{2}$: $\theta = \frac{\pi}{6}, \frac{5\pi}{6}$

**Solutions**: $\theta = \frac{\pi}{6}, \frac{\pi}{2}, \frac{5\pi}{6}, \frac{3\pi}{2}$
</details>

---

**Problem 19** *(Free Response Style)*
(a) Verify the identity: $\dfrac{\sin 2\theta}{1 + \cos 2\theta} = \tan\theta$

(b) Use this identity to find $\tan 22.5°$.

<details>
<summary>Show Solution</summary>

**Solution**:

**(a)**
$$\frac{\sin 2\theta}{1 + \cos 2\theta} = \frac{2\sin\theta\cos\theta}{1 + (2\cos^2\theta - 1)}$$
$$= \frac{2\sin\theta\cos\theta}{2\cos^2\theta} = \frac{\sin\theta}{\cos\theta} = \tan\theta$$ ✓

**(b)** Use $\theta = 22.5°$, so $2\theta = 45°$:
$$\tan 22.5° = \frac{\sin 45°}{1 + \cos 45°} = \frac{\frac{\sqrt{2}}{2}}{1 + \frac{\sqrt{2}}{2}}$$
$$= \frac{\frac{\sqrt{2}}{2}}{\frac{2 + \sqrt{2}}{2}} = \frac{\sqrt{2}}{2 + \sqrt{2}}$$

Rationalize:
$$= \frac{\sqrt{2}(2 - \sqrt{2})}{(2 + \sqrt{2})(2 - \sqrt{2})} = \frac{2\sqrt{2} - 2}{4 - 2} = \frac{2(\sqrt{2} - 1)}{2} = \sqrt{2} - 1$$
</details>

---

**Problem 20** *(Free Response Style)*
Let $f(x) = \sin^2 x - \cos^2 x$.

(a) Express $f(x)$ as a single trig function.
(b) Find all zeros of $f$ in $[0, 2\pi)$.
(c) Find $f'(x)$.
(d) Verify $f'(x)$ matches the derivative of your answer in part (a).

<details>
<summary>Show Solution</summary>

**Solution**:

**(a)**
$$f(x) = \sin^2 x - \cos^2 x = -(\cos^2 x - \sin^2 x) = -\cos 2x$$

**(b)** $-\cos 2x = 0$ when $\cos 2x = 0$:
$$2x = \frac{\pi}{2}, \frac{3\pi}{2}, \frac{5\pi}{2}, \frac{7\pi}{2}$$
$$x = \frac{\pi}{4}, \frac{3\pi}{4}, \frac{5\pi}{4}, \frac{7\pi}{4}$$

**(c)** Using the original form:
$$f'(x) = 2\sin x \cos x - 2\cos x(-\sin x)$$
$$= 2\sin x \cos x + 2\sin x \cos x = 4\sin x \cos x = 2\sin 2x$$

**(d)** From part (a), $f(x) = -\cos 2x$:
$$f'(x) = -(-\sin 2x) \cdot 2 = 2\sin 2x$$ ✓
</details>

---

## What's Next

Now that you've mastered trig identities, you're ready to explore [Inverse Trig Functions](/calculus/0110-inverse-trig-functions), where we'll learn to find angles when given trig values—essential for solving equations and for calculus integration.

---

<div align="center">

[← Unit Circle](/calculus/0108-unit-circle) | [Inverse Trig Functions →](/calculus/0110-inverse-trig-functions)

</div>
