# The Unit Circle
<p class="article-date">July 18, 2024</p>

## Prerequisites
Before diving in, make sure you're comfortable with:
- Coordinate plane basics
- Pythagorean theorem
- Basic angle measurement

## Learning Objectives
By the end of this section, you will be able to:
- Convert between degrees and radians
- Locate angles on the unit circle
- Find exact values of sine, cosine, and tangent for special angles
- Understand the relationship between coordinates and trig functions
- Use reference angles to find trig values in any quadrant

## The Big Picture: Why the Unit Circle?

The **unit circle** is a circle with radius 1, centered at the origin. It's the foundation of trigonometry because:

- Every point on the circle has coordinates $(\cos\theta, \sin\theta)$
- It gives us exact values without a calculator
- It reveals patterns that extend to all angles

> **Key Insight**: On the unit circle, the $x$-coordinate is cosine and the $y$-coordinate is sine.

## Radians: The Natural Angle Measure

### Definition
One **radian** is the angle created when the arc length equals the radius.

Since the circumference of a unit circle is $2\pi$, a full rotation is $2\pi$ radians.

### Conversion Formulas

$$\text{Radians} = \text{Degrees} \times \frac{\pi}{180}$$

$$\text{Degrees} = \text{Radians} \times \frac{180}{\pi}$$

### Common Conversions

| Degrees | Radians |
|---------|---------|
| $0°$ | $0$ |
| $30°$ | $\frac{\pi}{6}$ |
| $45°$ | $\frac{\pi}{4}$ |
| $60°$ | $\frac{\pi}{3}$ |
| $90°$ | $\frac{\pi}{2}$ |
| $180°$ | $\pi$ |
| $270°$ | $\frac{3\pi}{2}$ |
| $360°$ | $2\pi$ |

> **Calculus Note**: Radians are required for calculus! Derivative formulas like $\frac{d}{dx}[\sin x] = \cos x$ only work in radians.

## The Unit Circle Diagram

Imagine the coordinate plane with a circle of radius 1:

```
                (0, 1)
                 90°
                 π/2
                  |
    120°  135°    |    45°   60°
   2π/3  3π/4    |   π/4   π/3
         \       |       /
          \      |      /
           \     |     /
  180° -----+----+----+----- 0°, 360°
    π      /     |     \     2π
          /      |      \
         /       |       \
   4π/3  5π/4    |   7π/4  5π/3
   240°  225°    |   315°  300°
                 |
               270°
               3π/2
               (0, -1)
```

## Coordinates on the Unit Circle

For any angle $\theta$, the point on the unit circle is:
$$(\cos\theta, \sin\theta)$$

This comes from the right triangle formed:
- Hypotenuse = radius = 1
- Adjacent side = $x$-coordinate = $\cos\theta$
- Opposite side = $y$-coordinate = $\sin\theta$

## The Special Angles

There are three "families" of special angles based on the reference angle:

### Family 1: 30° ($\frac{\pi}{6}$) Reference

$$\cos 30° = \frac{\sqrt{3}}{2}, \quad \sin 30° = \frac{1}{2}$$

### Family 2: 45° ($\frac{\pi}{4}$) Reference

$$\cos 45° = \frac{\sqrt{2}}{2}, \quad \sin 45° = \frac{\sqrt{2}}{2}$$

### Family 3: 60° ($\frac{\pi}{3}$) Reference

$$\cos 60° = \frac{1}{2}, \quad \sin 60° = \frac{\sqrt{3}}{2}$$

### Quadrantal Angles (0°, 90°, 180°, 270°)

| Angle | Coordinates | $\cos\theta$ | $\sin\theta$ |
|-------|-------------|--------------|--------------|
| $0$ | $(1, 0)$ | $1$ | $0$ |
| $\frac{\pi}{2}$ | $(0, 1)$ | $0$ | $1$ |
| $\pi$ | $(-1, 0)$ | $-1$ | $0$ |
| $\frac{3\pi}{2}$ | $(0, -1)$ | $0$ | $-1$ |

## Complete Unit Circle Values

| Angle (rad) | Angle (deg) | $\cos\theta$ | $\sin\theta$ | Coordinates |
|-------------|-------------|--------------|--------------|-------------|
| $0$ | $0°$ | $1$ | $0$ | $(1, 0)$ |
| $\frac{\pi}{6}$ | $30°$ | $\frac{\sqrt{3}}{2}$ | $\frac{1}{2}$ | $(\frac{\sqrt{3}}{2}, \frac{1}{2})$ |
| $\frac{\pi}{4}$ | $45°$ | $\frac{\sqrt{2}}{2}$ | $\frac{\sqrt{2}}{2}$ | $(\frac{\sqrt{2}}{2}, \frac{\sqrt{2}}{2})$ |
| $\frac{\pi}{3}$ | $60°$ | $\frac{1}{2}$ | $\frac{\sqrt{3}}{2}$ | $(\frac{1}{2}, \frac{\sqrt{3}}{2})$ |
| $\frac{\pi}{2}$ | $90°$ | $0$ | $1$ | $(0, 1)$ |
| $\frac{2\pi}{3}$ | $120°$ | $-\frac{1}{2}$ | $\frac{\sqrt{3}}{2}$ | $(-\frac{1}{2}, \frac{\sqrt{3}}{2})$ |
| $\frac{3\pi}{4}$ | $135°$ | $-\frac{\sqrt{2}}{2}$ | $\frac{\sqrt{2}}{2}$ | $(-\frac{\sqrt{2}}{2}, \frac{\sqrt{2}}{2})$ |
| $\frac{5\pi}{6}$ | $150°$ | $-\frac{\sqrt{3}}{2}$ | $\frac{1}{2}$ | $(-\frac{\sqrt{3}}{2}, \frac{1}{2})$ |
| $\pi$ | $180°$ | $-1$ | $0$ | $(-1, 0)$ |
| $\frac{7\pi}{6}$ | $210°$ | $-\frac{\sqrt{3}}{2}$ | $-\frac{1}{2}$ | $(-\frac{\sqrt{3}}{2}, -\frac{1}{2})$ |
| $\frac{5\pi}{4}$ | $225°$ | $-\frac{\sqrt{2}}{2}$ | $-\frac{\sqrt{2}}{2}$ | $(-\frac{\sqrt{2}}{2}, -\frac{\sqrt{2}}{2})$ |
| $\frac{4\pi}{3}$ | $240°$ | $-\frac{1}{2}$ | $-\frac{\sqrt{3}}{2}$ | $(-\frac{1}{2}, -\frac{\sqrt{3}}{2})$ |
| $\frac{3\pi}{2}$ | $270°$ | $0$ | $-1$ | $(0, -1)$ |
| $\frac{5\pi}{3}$ | $300°$ | $\frac{1}{2}$ | $-\frac{\sqrt{3}}{2}$ | $(\frac{1}{2}, -\frac{\sqrt{3}}{2})$ |
| $\frac{7\pi}{4}$ | $315°$ | $\frac{\sqrt{2}}{2}$ | $-\frac{\sqrt{2}}{2}$ | $(\frac{\sqrt{2}}{2}, -\frac{\sqrt{2}}{2})$ |
| $\frac{11\pi}{6}$ | $330°$ | $\frac{\sqrt{3}}{2}$ | $-\frac{1}{2}$ | $(\frac{\sqrt{3}}{2}, -\frac{1}{2})$ |

## Memory Tricks

### The "1-2-3" Pattern
For first quadrant angles:
- Cosine values (left to right): $\frac{\sqrt{3}}{2}, \frac{\sqrt{2}}{2}, \frac{1}{2}$
- Sine values (bottom to top): $\frac{1}{2}, \frac{\sqrt{2}}{2}, \frac{\sqrt{3}}{2}$

Think: $\frac{\sqrt{1}}{2}, \frac{\sqrt{2}}{2}, \frac{\sqrt{3}}{2}$

### The Hand Trick
Using your left hand (palm facing you):
- Thumb = 0°: $\cos = \frac{\sqrt{4}}{2} = 1$
- Index = 30°: $\cos = \frac{\sqrt{3}}{2}$
- Middle = 45°: $\cos = \frac{\sqrt{2}}{2}$
- Ring = 60°: $\cos = \frac{\sqrt{1}}{2} = \frac{1}{2}$
- Pinky = 90°: $\cos = \frac{\sqrt{0}}{2} = 0$

For sine, reverse the order!

## Reference Angles

The **reference angle** is the acute angle formed with the x-axis.

### Finding Reference Angles

| Quadrant | Reference Angle |
|----------|-----------------|
| I | $\theta$ (itself) |
| II | $\pi - \theta$ or $180° - \theta$ |
| III | $\theta - \pi$ or $\theta - 180°$ |
| IV | $2\pi - \theta$ or $360° - \theta$ |

### Using Reference Angles

1. Find the reference angle
2. Determine the trig value for the reference angle
3. Apply the correct sign based on quadrant

## Signs in Each Quadrant: "All Students Take Calculus"

| Quadrant | Positive Trig Functions | Memory |
|----------|------------------------|--------|
| I | All | **A**ll |
| II | Sine (and cosecant) | **S**tudents |
| III | Tangent (and cotangent) | **T**ake |
| IV | Cosine (and secant) | **C**alculus |

## Tangent on the Unit Circle

$$\tan\theta = \frac{\sin\theta}{\cos\theta} = \frac{y}{x}$$

| Angle | $\tan\theta$ |
|-------|--------------|
| $0$ | $0$ |
| $\frac{\pi}{6}$ | $\frac{1}{\sqrt{3}} = \frac{\sqrt{3}}{3}$ |
| $\frac{\pi}{4}$ | $1$ |
| $\frac{\pi}{3}$ | $\sqrt{3}$ |
| $\frac{\pi}{2}$ | undefined |

## Worked Example 1: Finding Trig Values

**Problem**: Find $\sin\frac{5\pi}{4}$ and $\cos\frac{5\pi}{4}$.

**Solution**:

**Step 1**: Identify the quadrant.
$\frac{5\pi}{4} = \frac{5 \cdot 180°}{4} = 225°$, which is in Quadrant III.

**Step 2**: Find the reference angle.
$\frac{5\pi}{4} - \pi = \frac{5\pi}{4} - \frac{4\pi}{4} = \frac{\pi}{4}$

**Step 3**: Get the values for $\frac{\pi}{4}$.
$\cos\frac{\pi}{4} = \frac{\sqrt{2}}{2}$, $\sin\frac{\pi}{4} = \frac{\sqrt{2}}{2}$

**Step 4**: Apply signs (Quadrant III: both negative).
$$\cos\frac{5\pi}{4} = -\frac{\sqrt{2}}{2}, \quad \sin\frac{5\pi}{4} = -\frac{\sqrt{2}}{2}$$

## Worked Example 2: Converting and Evaluating

**Problem**: Convert $-150°$ to radians and find $\cos(-150°)$.

**Solution**:

**Radians**: $-150° \times \frac{\pi}{180°} = -\frac{5\pi}{6}$

**Reference angle**: $180° - 150° = 30° = \frac{\pi}{6}$

**Quadrant**: $-150°$ is the same as $210°$ (Quadrant III)

**Value**: $\cos 30° = \frac{\sqrt{3}}{2}$, but in Q3 cosine is negative.

$$\cos(-150°) = -\frac{\sqrt{3}}{2}$$

## Key Formulas

| Formula | Description |
|---------|-------------|
| $\sin^2\theta + \cos^2\theta = 1$ | Pythagorean identity |
| $\tan\theta = \frac{\sin\theta}{\cos\theta}$ | Definition of tangent |
| Point: $(\cos\theta, \sin\theta)$ | Coordinates on unit circle |

## Common Mistakes to Avoid

1. **Using degrees in calculus**
   - Always convert to radians for derivatives/integrals

2. **Wrong quadrant signs**
   - Remember: cosine = x (positive right), sine = y (positive up)

3. **Confusing reference angle with the angle**
   - Reference angle is always acute (between 0 and 90°)

4. **Mixing up sine and cosine**
   - Cosine is the x-coordinate (horizontal)
   - Sine is the y-coordinate (vertical)

5. **Forgetting that tangent can be undefined**
   - $\tan\theta$ is undefined when $\cos\theta = 0$

## Calculus Connection

The unit circle is essential for:

1. **Derivatives**: $\frac{d}{dx}[\sin x] = \cos x$ (must use radians!)

2. **Limits**: $\lim_{x \to 0} \frac{\sin x}{x} = 1$ (radians only)

3. **Trig Substitution**: Using $x = \sin\theta$ in integrals

4. **Periodic Functions**: Understanding oscillation and waves

---

## Practice Problems

### Basic (Computational)

**Problem 1**
Convert $120°$ to radians.

<details>
<summary>Show Solution</summary>

**Solution**:
$$120° \times \frac{\pi}{180°} = \frac{120\pi}{180} = \frac{2\pi}{3}$$
</details>

---

**Problem 2**
Convert $\frac{5\pi}{4}$ to degrees.

<details>
<summary>Show Solution</summary>

**Solution**:
$$\frac{5\pi}{4} \times \frac{180°}{\pi} = \frac{5 \times 180°}{4} = 225°$$
</details>

---

**Problem 3**
Find $\cos\frac{\pi}{3}$ and $\sin\frac{\pi}{3}$.

<details>
<summary>Show Solution</summary>

**Solution**:
From the unit circle (60°):
$$\cos\frac{\pi}{3} = \frac{1}{2}, \quad \sin\frac{\pi}{3} = \frac{\sqrt{3}}{2}$$
</details>

---

**Problem 4**
Find $\tan\frac{\pi}{4}$.

<details>
<summary>Show Solution</summary>

**Solution**:
$$\tan\frac{\pi}{4} = \frac{\sin\frac{\pi}{4}}{\cos\frac{\pi}{4}} = \frac{\frac{\sqrt{2}}{2}}{\frac{\sqrt{2}}{2}} = 1$$
</details>

---

**Problem 5**
What are the coordinates of the point on the unit circle at $\theta = \pi$?

<details>
<summary>Show Solution</summary>

**Solution**:
At $\theta = \pi$ (180°), the point is $(-1, 0)$.

So $\cos\pi = -1$ and $\sin\pi = 0$.
</details>

---

### Intermediate (Multi-step)

**Problem 6**
Find $\sin\frac{7\pi}{6}$.

<details>
<summary>Show Solution</summary>

**Solution**:
$\frac{7\pi}{6} = 210°$ is in Quadrant III.

Reference angle: $\frac{7\pi}{6} - \pi = \frac{\pi}{6}$

$\sin\frac{\pi}{6} = \frac{1}{2}$

In Q3, sine is negative:
$$\sin\frac{7\pi}{6} = -\frac{1}{2}$$
</details>

---

**Problem 7**
Find $\cos\frac{11\pi}{6}$.

<details>
<summary>Show Solution</summary>

**Solution**:
$\frac{11\pi}{6} = 330°$ is in Quadrant IV.

Reference angle: $2\pi - \frac{11\pi}{6} = \frac{\pi}{6}$

$\cos\frac{\pi}{6} = \frac{\sqrt{3}}{2}$

In Q4, cosine is positive:
$$\cos\frac{11\pi}{6} = \frac{\sqrt{3}}{2}$$
</details>

---

**Problem 8**
Find all values of $\theta$ in $[0, 2\pi)$ where $\sin\theta = \frac{1}{2}$.

<details>
<summary>Show Solution</summary>

**Solution**:
$\sin\theta = \frac{1}{2}$ corresponds to reference angle $\frac{\pi}{6}$.

Sine is positive in Quadrants I and II:
- Q1: $\theta = \frac{\pi}{6}$
- Q2: $\theta = \pi - \frac{\pi}{6} = \frac{5\pi}{6}$

**Solutions**: $\theta = \frac{\pi}{6}, \frac{5\pi}{6}$
</details>

---

**Problem 9**
Find $\tan\frac{2\pi}{3}$.

<details>
<summary>Show Solution</summary>

**Solution**:
$\frac{2\pi}{3} = 120°$ is in Quadrant II.

Reference angle: $\pi - \frac{2\pi}{3} = \frac{\pi}{3}$

$\tan\frac{\pi}{3} = \sqrt{3}$

In Q2, tangent is negative (sine +, cosine -):
$$\tan\frac{2\pi}{3} = -\sqrt{3}$$
</details>

---

**Problem 10**
If $\cos\theta = -\frac{1}{2}$ and $\theta$ is in Quadrant II, find $\sin\theta$.

<details>
<summary>Show Solution</summary>

**Solution**:
Use $\sin^2\theta + \cos^2\theta = 1$:
$$\sin^2\theta + \frac{1}{4} = 1$$
$$\sin^2\theta = \frac{3}{4}$$
$$\sin\theta = \pm\frac{\sqrt{3}}{2}$$

In Q2, sine is positive:
$$\sin\theta = \frac{\sqrt{3}}{2}$$
</details>

---

### Advanced (Complex Applications)

**Problem 11**
Find all six trig function values for $\theta = \frac{5\pi}{3}$.

<details>
<summary>Show Solution</summary>

**Solution**:
$\frac{5\pi}{3} = 300°$ is in Quadrant IV.

Reference angle: $2\pi - \frac{5\pi}{3} = \frac{\pi}{3}$

From $\frac{\pi}{3}$: $\cos = \frac{1}{2}$, $\sin = \frac{\sqrt{3}}{2}$

In Q4: cosine +, sine -

$$\cos\frac{5\pi}{3} = \frac{1}{2}, \quad \sin\frac{5\pi}{3} = -\frac{\sqrt{3}}{2}$$

$$\tan\frac{5\pi}{3} = \frac{-\sqrt{3}/2}{1/2} = -\sqrt{3}$$

$$\sec\frac{5\pi}{3} = 2, \quad \csc\frac{5\pi}{3} = -\frac{2\sqrt{3}}{3}, \quad \cot\frac{5\pi}{3} = -\frac{\sqrt{3}}{3}$$
</details>

---

**Problem 12**
Find all angles in $[0, 2\pi)$ where $\tan\theta = -1$.

<details>
<summary>Show Solution</summary>

**Solution**:
$\tan\theta = -1$ means reference angle is $\frac{\pi}{4}$.

Tangent is negative in Q2 and Q4:
- Q2: $\theta = \pi - \frac{\pi}{4} = \frac{3\pi}{4}$
- Q4: $\theta = 2\pi - \frac{\pi}{4} = \frac{7\pi}{4}$

**Solutions**: $\theta = \frac{3\pi}{4}, \frac{7\pi}{4}$
</details>

---

**Problem 13**
Simplify $\sin(-\theta)$ and $\cos(-\theta)$ using the unit circle.

<details>
<summary>Show Solution</summary>

**Solution**:
If $\theta$ corresponds to point $(x, y) = (\cos\theta, \sin\theta)$,

then $-\theta$ corresponds to $(x, -y)$ (reflection over x-axis).

Therefore:
$$\cos(-\theta) = \cos\theta$$ (same x-coordinate)
$$\sin(-\theta) = -\sin\theta$$ (opposite y-coordinate)

Cosine is even, sine is odd.
</details>

---

**Problem 14**
Find the exact value of $\cos 75°$ using $\cos(45° + 30°)$.

<details>
<summary>Show Solution</summary>

**Solution**:
Using the sum formula:
$$\cos(A + B) = \cos A \cos B - \sin A \sin B$$

$$\cos 75° = \cos 45° \cos 30° - \sin 45° \sin 30°$$

$$= \frac{\sqrt{2}}{2} \cdot \frac{\sqrt{3}}{2} - \frac{\sqrt{2}}{2} \cdot \frac{1}{2}$$

$$= \frac{\sqrt{6}}{4} - \frac{\sqrt{2}}{4}$$

$$= \frac{\sqrt{6} - \sqrt{2}}{4}$$
</details>

---

**Problem 15**
If $\sin\theta = \frac{3}{5}$ and $\theta$ is in Quadrant I, find $\cos\theta$ and $\tan\theta$.

<details>
<summary>Show Solution</summary>

**Solution**:
Using Pythagorean identity:
$$\cos^2\theta = 1 - \sin^2\theta = 1 - \frac{9}{25} = \frac{16}{25}$$

In Q1, cosine is positive:
$$\cos\theta = \frac{4}{5}$$

$$\tan\theta = \frac{\sin\theta}{\cos\theta} = \frac{3/5}{4/5} = \frac{3}{4}$$
</details>

---

### AP Exam Style

**Problem 16**
The terminal side of angle $\theta$ in standard position passes through $(-3, 4)$. Find $\cos\theta$.

<details>
<summary>Show Solution</summary>

**Solution**:
Find the radius: $r = \sqrt{(-3)^2 + 4^2} = \sqrt{25} = 5$

$$\cos\theta = \frac{x}{r} = \frac{-3}{5}$$
</details>

---

**Problem 17**
Which of the following equals $\sin\frac{7\pi}{6}$?

(A) $\sin\frac{\pi}{6}$
(B) $-\sin\frac{\pi}{6}$
(C) $\cos\frac{\pi}{6}$
(D) $-\cos\frac{\pi}{6}$

<details>
<summary>Show Solution</summary>

**Solution**:
$\frac{7\pi}{6}$ is in Q3 with reference angle $\frac{\pi}{6}$.

In Q3, sine is negative:
$$\sin\frac{7\pi}{6} = -\sin\frac{\pi}{6}$$

**Answer: (B)**
</details>

---

**Problem 18**
If $\cos\theta < 0$ and $\tan\theta > 0$, in which quadrant is $\theta$?

<details>
<summary>Show Solution</summary>

**Solution**:
$\cos\theta < 0$: Quadrants II or III

$\tan\theta > 0$: Quadrants I or III

Both conditions: **Quadrant III**
</details>

---

**Problem 19** *(Free Response Style)*
Consider the angle $\theta = -\frac{5\pi}{6}$.

(a) Find the reference angle.
(b) Determine the quadrant.
(c) Find the exact values of $\sin\theta$, $\cos\theta$, and $\tan\theta$.
(d) Find a positive coterminal angle.

<details>
<summary>Show Solution</summary>

**Solution**:

**(a)** First convert to positive: $-\frac{5\pi}{6} + 2\pi = \frac{7\pi}{6}$

Reference angle from $\frac{7\pi}{6}$: $\frac{7\pi}{6} - \pi = \frac{\pi}{6}$

**(b)** $\frac{7\pi}{6} = 210°$ is in **Quadrant III**

**(c)** From $\frac{\pi}{6}$: $\cos = \frac{\sqrt{3}}{2}$, $\sin = \frac{1}{2}$

In Q3, both are negative:
$$\sin\left(-\frac{5\pi}{6}\right) = -\frac{1}{2}$$
$$\cos\left(-\frac{5\pi}{6}\right) = -\frac{\sqrt{3}}{2}$$
$$\tan\left(-\frac{5\pi}{6}\right) = \frac{-1/2}{-\sqrt{3}/2} = \frac{1}{\sqrt{3}} = \frac{\sqrt{3}}{3}$$

**(d)** Add $2\pi$: $-\frac{5\pi}{6} + 2\pi = \frac{7\pi}{6}$
</details>

---

**Problem 20** *(Free Response Style)*
A point $P$ moves around the unit circle starting from $(1, 0)$.

(a) After rotating $\frac{3\pi}{4}$ radians counterclockwise, what are the coordinates of $P$?
(b) What is the shortest distance from $P$ to the point $(1, 0)$?
(c) For what angles $\theta \in [0, 2\pi)$ is the y-coordinate of $P$ equal to $\frac{\sqrt{2}}{2}$?
(d) For what angles is the x-coordinate greater than the y-coordinate?

<details>
<summary>Show Solution</summary>

**Solution**:

**(a)** At $\theta = \frac{3\pi}{4}$:
$$P = \left(\cos\frac{3\pi}{4}, \sin\frac{3\pi}{4}\right) = \left(-\frac{\sqrt{2}}{2}, \frac{\sqrt{2}}{2}\right)$$

**(b)** Distance from $\left(-\frac{\sqrt{2}}{2}, \frac{\sqrt{2}}{2}\right)$ to $(1, 0)$:
$$d = \sqrt{\left(-\frac{\sqrt{2}}{2} - 1\right)^2 + \left(\frac{\sqrt{2}}{2}\right)^2}$$
$$= \sqrt{\left(\frac{-\sqrt{2} - 2}{2}\right)^2 + \frac{1}{2}}$$
$$= \sqrt{\frac{2 + 4\sqrt{2} + 4}{4} + \frac{1}{2}}$$
$$= \sqrt{\frac{6 + 4\sqrt{2} + 2}{4}} = \sqrt{\frac{8 + 4\sqrt{2}}{4}} = \sqrt{2 + \sqrt{2}}$$

**(c)** $\sin\theta = \frac{\sqrt{2}}{2}$ at:
$$\theta = \frac{\pi}{4}, \frac{3\pi}{4}$$

**(d)** $\cos\theta > \sin\theta$

In Q1: this is true for $0 \le \theta < \frac{\pi}{4}$
In Q4: this is true for $\frac{5\pi}{4} < \theta < 2\pi$

Actually, more carefully: $\cos\theta = \sin\theta$ when $\theta = \frac{\pi}{4}$ and $\theta = \frac{5\pi}{4}$.

$\cos\theta > \sin\theta$ when $\theta \in \left[0, \frac{\pi}{4}\right) \cup \left(\frac{5\pi}{4}, 2\pi\right)$
</details>

---

## What's Next

Now that you've mastered the unit circle, you're ready to explore [Trig Identities](/calculus/0109-trig-identities), where we'll discover relationships between trig functions that simplify complex expressions.

---

<div align="center">

[← Rational Expressions](/calculus/0107-rational-expressions) | [Trig Identities →](/calculus/0109-trig-identities)

</div>
