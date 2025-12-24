# Motion Along a Line

When an object moves along a straight line, calculus gives us the perfect tools to analyze its motion. The position function tells us where, its derivative (velocity) tells us how fast and in what direction, and the second derivative (acceleration) tells us how the motion is changing. These concepts connect abstract derivatives to the real, physical world.

---

## What You'll Learn

- Relate position, velocity, and acceleration through derivatives
- Interpret the sign of velocity (direction) and acceleration (speeding up/slowing down)
- Find when a particle is at rest, moving left/right
- Calculate total distance traveled vs. displacement
- Analyze motion using graphs of position, velocity, or acceleration
- Solve AP Calculus motion problems with confidence

---

## Prerequisites

- [Basic Derivative Rules](/calculus/basic-derivative-rules)
- [Higher-Order Derivatives](/calculus/higher-order-derivatives)
- Integration basics (for some problems)

---

## The Core Concept

### The Motion Hierarchy

For a particle moving along a line with position $s(t)$ at time $t$:

$$\boxed{s(t) \xrightarrow{\text{derivative}} v(t) \xrightarrow{\text{derivative}} a(t)}$$

| Function | Name | Meaning |
|----------|------|---------|
| $s(t)$ | Position | Where the particle is |
| $v(t) = s'(t)$ | Velocity | Rate of change of position |
| $a(t) = v'(t) = s''(t)$ | Acceleration | Rate of change of velocity |

### Going Backwards (Integration)

$$\boxed{s(t) \xleftarrow{\text{integral}} v(t) \xleftarrow{\text{integral}} a(t)}$$

---

## Interpreting Signs

### Velocity Sign

| $v(t)$ | Meaning |
|--------|---------|
| $v(t) > 0$ | Moving right (or up) |
| $v(t) < 0$ | Moving left (or down) |
| $v(t) = 0$ | At rest (momentarily stopped) |

### Acceleration Sign

| $a(t)$ | Meaning |
|--------|---------|
| $a(t) > 0$ | Velocity increasing |
| $a(t) < 0$ | Velocity decreasing |

### Speed vs. Velocity

- **Velocity** = signed quantity (includes direction)
- **Speed** = $|v(t)|$ = magnitude only (always ≥ 0)

### Speeding Up vs. Slowing Down

This is the key insight that confuses many students:

$$\boxed{\text{Speeding up: } v(t) \text{ and } a(t) \text{ have the SAME sign}}$$

$$\boxed{\text{Slowing down: } v(t) \text{ and } a(t) \text{ have OPPOSITE signs}}$$

**Why?**
- If you're moving right ($v > 0$) and accelerating right ($a > 0$), you speed up.
- If you're moving right ($v > 0$) but accelerating left ($a < 0$), you slow down.
- If you're moving left ($v < 0$) and accelerating left ($a < 0$), you speed up (going faster to the left).

---

## Worked Examples

### Example 1: Basic Motion Analysis

**A particle moves along a line with position $s(t) = t^3 - 6t^2 + 9t + 2$ for $t \geq 0$.**

**Find:**
- (a) Velocity and acceleration functions
- (b) When is the particle at rest?
- (c) When is the particle moving right? Left?
- (d) When is the particle speeding up? Slowing down?

**Solution:**

**(a) Velocity and acceleration:**

$$v(t) = s'(t) = 3t^2 - 12t + 9 = 3(t^2 - 4t + 3) = 3(t-1)(t-3)$$

$$a(t) = v'(t) = 6t - 12 = 6(t - 2)$$

**(b) At rest when $v(t) = 0$:**

$3(t-1)(t-3) = 0$

$t = 1$ or $t = 3$ seconds

**(c) Direction of motion:**

| Interval | $v(t)$ | Direction |
|----------|--------|-----------|
| $0 < t < 1$ | $+$ | Right |
| $1 < t < 3$ | $-$ | Left |
| $t > 3$ | $+$ | Right |

**(d) Speeding up/slowing down:**

$a(t) = 0$ when $t = 2$

| Interval | $v(t)$ | $a(t)$ | Motion |
|----------|--------|--------|--------|
| $0 < t < 1$ | $+$ | $-$ | Slowing down |
| $1 < t < 2$ | $-$ | $-$ | Speeding up |
| $2 < t < 3$ | $-$ | $+$ | Slowing down |
| $t > 3$ | $+$ | $+$ | Speeding up |

---

### Example 2: Finding Position at Key Times

**For the particle in Example 1, find its position at $t = 0, 1, 3$.**

**Solution:**

$$s(0) = 0 - 0 + 0 + 2 = 2$$
$$s(1) = 1 - 6 + 9 + 2 = 6$$
$$s(3) = 27 - 54 + 27 + 2 = 2$$

The particle starts at position 2, moves right to position 6, then moves back left to position 2.

---

### Example 3: Displacement vs. Total Distance

**For the particle in Example 1, find:**
- (a) Displacement from $t = 0$ to $t = 4$
- (b) Total distance traveled from $t = 0$ to $t = 4$

**Solution:**

**(a) Displacement = final position − initial position:**

$$s(4) = 64 - 96 + 36 + 2 = 6$$
$$s(0) = 2$$

$$\text{Displacement} = s(4) - s(0) = 6 - 2 = 4 \text{ units right}$$

**(b) Total distance (account for direction changes):**

The particle changes direction at $t = 1$ and $t = 3$.

$$s(0) = 2, \quad s(1) = 6, \quad s(3) = 2, \quad s(4) = 6$$

| Interval | Distance |
|----------|----------|
| $t: 0 \to 1$ | $|6 - 2| = 4$ |
| $t: 1 \to 3$ | $|2 - 6| = 4$ |
| $t: 3 \to 4$ | $|6 - 2| = 4$ |

$$\text{Total distance} = 4 + 4 + 4 = 12 \text{ units}$$

---

### Example 4: Velocity Given, Find Position

**A particle has velocity $v(t) = 3t^2 - 6t$ and initial position $s(0) = 4$. Find $s(t)$.**

**Solution:**

$$s(t) = \int v(t) \, dt = \int (3t^2 - 6t) \, dt = t^3 - 3t^2 + C$$

Using $s(0) = 4$:
$$4 = 0 - 0 + C \Rightarrow C = 4$$

$$s(t) = t^3 - 3t^2 + 4$$

---

### Example 5: Acceleration Given

**A particle has acceleration $a(t) = 6t - 4$, initial velocity $v(0) = 2$, and initial position $s(0) = 1$. Find $s(t)$.**

**Solution:**

**Find velocity:**
$$v(t) = \int a(t) \, dt = \int (6t - 4) \, dt = 3t^2 - 4t + C_1$$

Using $v(0) = 2$: $C_1 = 2$

$$v(t) = 3t^2 - 4t + 2$$

**Find position:**
$$s(t) = \int v(t) \, dt = \int (3t^2 - 4t + 2) \, dt = t^3 - 2t^2 + 2t + C_2$$

Using $s(0) = 1$: $C_2 = 1$

$$s(t) = t^3 - 2t^2 + 2t + 1$$

---

### Example 6: Trig Motion (Simple Harmonic)

**A particle moves with position $s(t) = 3\sin(2t)$ for $t \geq 0$.**

**Find velocity, acceleration, and when the particle is at rest.**

**Solution:**

$$v(t) = s'(t) = 6\cos(2t)$$
$$a(t) = v'(t) = -12\sin(2t)$$

**At rest when $v(t) = 0$:**

$\cos(2t) = 0$

$2t = \frac{\pi}{2}, \frac{3\pi}{2}, \frac{5\pi}{2}, ...$

$t = \frac{\pi}{4}, \frac{3\pi}{4}, \frac{5\pi}{4}, ...$

**Note:** $a(t) = -12\sin(2t) = -4 \cdot 3\sin(2t) = -4s(t)$

This is simple harmonic motion! Acceleration is proportional to displacement and directed toward equilibrium.

---

### Example 7: Exponential Motion

**A particle moves with position $s(t) = e^{-t}(t + 1)$ for $t \geq 0$.**

**Find when the particle is moving right and when it's at rest.**

**Solution:**

$$v(t) = -e^{-t}(t + 1) + e^{-t}(1) = e^{-t}(-t - 1 + 1) = -te^{-t}$$

**At rest:** $v(t) = 0$ when $t = 0$ (since $e^{-t} \neq 0$)

**Direction:**
- For $t > 0$: $v(t) = -te^{-t} < 0$ (moving left)

The particle starts at rest, then moves left for all $t > 0$.

---

### Example 8: Maximum Distance from Origin

**A particle moves with $s(t) = t^3 - 12t$ for $t \geq 0$. Find the maximum distance from the origin for $0 \leq t \leq 4$.**

**Solution:**

$$v(t) = 3t^2 - 12 = 3(t^2 - 4) = 3(t-2)(t+2)$$

Critical point in $[0, 4]$: $t = 2$

Evaluate $|s(t)|$ at critical points and endpoints:

$$|s(0)| = |0| = 0$$
$$|s(2)| = |8 - 24| = |-16| = 16$$
$$|s(4)| = |64 - 48| = |16| = 16$$

**Maximum distance from origin: 16 units** (at both $t = 2$ and $t = 4$)

---

## Graphical Analysis

### Reading Motion from Graphs

**From a position graph $s(t)$:**
- Slope = velocity
- Positive slope → moving right
- Negative slope → moving left
- Zero slope → at rest
- Increasing slope → speeding up (if moving right)

**From a velocity graph $v(t)$:**
- Value above x-axis → moving right
- Value below x-axis → moving left
- Crosses x-axis → changes direction
- Slope = acceleration
- Area under curve = displacement

**From an acceleration graph $a(t)$:**
- Value above x-axis → velocity increasing
- Value below x-axis → velocity decreasing
- Area under curve = change in velocity

---

### Example 9: Interpreting a Velocity Graph

**The velocity of a particle is shown below. At $t = 0$, the particle is at position $s = 2$.**

```
v(t)
  4 |    /\
  2 |   /  \
  0 |--/----\--/----> t
 -2 |        \/
    0  1  2  3  4
```

**Find:**
- (a) When is the particle moving right?
- (b) When is the particle at rest?
- (c) Displacement from $t = 0$ to $t = 4$
- (d) Position at $t = 2$

**Solution:**

**(a)** Moving right when $v(t) > 0$: $0 < t < 3$

**(b)** At rest when $v(t) = 0$: $t = 0$ and $t = 3$

**(c)** Displacement = area under velocity curve (signed)

Area from 0 to 2: triangle with base 2, height 4 → $\frac{1}{2}(2)(4) = 4$

Area from 2 to 3: triangle with base 1, height 4 to 0 → $\frac{1}{2}(1)(4) = 2$

Area from 3 to 4: triangle below axis, base 1, height 2 → $-\frac{1}{2}(1)(2) = -1$

Total displacement: $4 + 2 - 1 = 5$ units

**(d)** Position at $t = 2$: $s(2) = s(0) + \text{displacement from 0 to 2} = 2 + 4 = 6$

---

## Key Formulas & Relationships

### Derivative Relationships

$$v(t) = \frac{ds}{dt} = s'(t)$$

$$a(t) = \frac{dv}{dt} = v'(t) = s''(t)$$

### Integral Relationships

$$s(t) = s(t_0) + \int_{t_0}^{t} v(\tau) \, d\tau$$

$$v(t) = v(t_0) + \int_{t_0}^{t} a(\tau) \, d\tau$$

### Distance vs. Displacement

$$\text{Displacement} = s(b) - s(a) = \int_a^b v(t) \, dt$$

$$\text{Total Distance} = \int_a^b |v(t)| \, dt$$

### Speed

$$\text{Speed} = |v(t)|$$

---

## Common Mistakes to Avoid

### Mistake 1: Confusing Velocity and Speed

**Wrong:** "The particle's speed is $-5$ m/s"

Speed is always non-negative! Speed = $|v(t)|$

**Right:** "The velocity is $-5$ m/s" or "The speed is $5$ m/s"

---

### Mistake 2: Speeding Up = Positive Acceleration

**Wrong:** "The particle is speeding up because $a(t) > 0$"

**Right:** Check if $v(t)$ and $a(t)$ have the same sign.

If $v = -3$ and $a = 2$, the particle is slowing down (opposite signs), even though $a > 0$.

---

### Mistake 3: Displacement = Total Distance

**Wrong:** Using displacement formula for "how far did the particle travel?"

**Right:** Total distance requires finding where direction changes, then summing $|s(t_i) - s(t_{i-1})|$ for each interval.

---

### Mistake 4: Forgetting Initial Conditions

When integrating to find $v(t)$ or $s(t)$, don't forget the constant of integration! Use initial conditions to find it.

---

## AP Exam Tips

### Common Question Types

1. **Given $s(t)$:** Find $v(t)$, $a(t)$, when at rest, direction of motion
2. **Given $v(t)$:** Find when speeding up/slowing down, total distance
3. **Given $a(t)$ and initial conditions:** Find $v(t)$ and $s(t)$
4. **Graph interpretation:** Read motion information from graphs
5. **Displacement vs. distance:** Know the difference!

### Key Phrases to Watch For

- "At rest" → $v(t) = 0$
- "Moving right/up" → $v(t) > 0$
- "Speeding up" → $v$ and $a$ same sign
- "Distance traveled" → Use $|v(t)|$ or break into intervals
- "Displacement" → $s(b) - s(a)$

### Speed Tips

1. Factor $v(t)$ to find when it equals zero
2. Make a sign chart for $v(t)$ and $a(t)$
3. For distance, identify direction changes first
4. Check units in your answer

---

## Practice Problems

### Basic (Problems 1-5)

**1.** A particle moves with position $s(t) = t^2 - 4t + 3$. Find:

$$\text{(a) } v(t) \quad \text{(b) } a(t) \quad \text{(c) When is the particle at rest?}$$

---

**2.** A particle has velocity $v(t) = 3t - 6$. Find:

$$\text{(a) When is the particle moving right?} \quad \text{(b) } a(t)$$

---

**3.** For $s(t) = \sin(t)$, find the velocity and acceleration at $t = \frac{\pi}{2}$.

---

**4.** A particle has $v(t) = t^2 - 4$ and $s(0) = 5$. Find $s(t)$.

---

**5.** Find the displacement from $t = 0$ to $t = 3$ if $v(t) = 2t - 1$.

---

### Intermediate (Problems 6-10)

**6.** A particle moves with $s(t) = t^3 - 9t^2 + 24t$ for $t \geq 0$. Find:

$$\text{(a) When at rest} \quad \text{(b) When moving left} \quad \text{(c) When speeding up}$$

---

**7.** Find the total distance traveled from $t = 0$ to $t = 4$ if $s(t) = t^3 - 6t^2 + 9t$.

---

**8.** A particle has $a(t) = -10$ (constant), $v(0) = 20$, and $s(0) = 0$. Find when the particle returns to its starting position.

---

**9.** For $s(t) = e^{-t}\cos(t)$, find $v(0)$ and $a(0)$.

---

**10.** A particle moves with $v(t) = (t-1)(t-3)^2$. Find all times when the particle changes direction.

---

### Advanced (Problems 11-15)

**11.** A ball is thrown upward with $s(t) = -16t^2 + 64t + 80$ feet. Find:

$$\text{(a) Maximum height} \quad \text{(b) When it hits the ground} \quad \text{(c) Speed at impact}$$

---

**12.** A particle moves so that $a(t) = \sin(t)$, $v(0) = 1$, $s(0) = 0$. Find $s(t)$.

---

**13.** For what values of $t > 0$ is the particle with $s(t) = t\ln(t)$ speeding up?

---

**14.** Two particles have positions $s_1(t) = t^2$ and $s_2(t) = 2t + 3$. When do they have the same velocity?

---

**15.** Find the total distance traveled from $t = 0$ to $t = 2\pi$ for $s(t) = \sin(t)$.

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

A particle moves along the x-axis with velocity $v(t) = t^2 - 5t + 4$. The particle is moving to the left for:

| Choice | Answer |
|--------|--------|
| **(A)** | $0 < t < 1$ |
| **(B)** | $1 < t < 4$ |
| **(C)** | $t > 4$ |
| **(D)** | $0 < t < 4$ |

---

#### Problem 17 (Multiple Choice)

A particle has position $s(t) = t^3 - 3t^2$ for $t \geq 0$. The total distance traveled from $t = 0$ to $t = 3$ is:

| Choice | Answer |
|--------|--------|
| **(A)** | $0$ |
| **(B)** | $4$ |
| **(C)** | $8$ |
| **(D)** | $12$ |

---

#### Problem 18 (Free Response)

A particle moves along the x-axis with velocity $v(t) = \cos(\pi t)$ for $0 \leq t \leq 3$. At $t = 0$, the particle is at position $x = 1$.

> **(a)** Find the acceleration of the particle at $t = 1$.
>
> **(b)** Find all times in $[0, 3]$ when the particle is at rest.
>
> **(c)** Find the position of the particle at $t = 1$.
>
> **(d)** Find the total distance traveled by the particle from $t = 0$ to $t = 3$.

---

#### Problem 19 (Multiple Choice)

A particle moves with velocity $v(t) = 3t^2 - 12t + 9$. The particle is speeding up for:

| Choice | Answer |
|--------|--------|
| **(A)** | $0 < t < 1$ |
| **(B)** | $1 < t < 2$ |
| **(C)** | $2 < t < 3$ |
| **(D)** | $t > 3$ |

---

#### Problem 20 (Free Response - Challenging)

A particle moves along the x-axis with position given by $x(t) = te^{-t}$ for $t \geq 0$.

> **(a)** Find the velocity and acceleration functions.
>
> **(b)** Find the maximum distance the particle reaches from the origin.
>
> **(c)** Show that the particle approaches the origin as $t \to \infty$.
>
> **(d)** Find the time when the particle is moving fastest to the left.

---

## Solutions

<details>
<summary><strong>Solution 1</strong></summary>

**Problem:** $s(t) = t^2 - 4t + 3$

**(a)** $v(t) = 2t - 4$

**(b)** $a(t) = 2$

**(c)** At rest when $v(t) = 0$: $2t - 4 = 0 \Rightarrow t = 2$

</details>

---

<details>
<summary><strong>Solution 2</strong></summary>

**Problem:** $v(t) = 3t - 6$

**(a)** Moving right when $v(t) > 0$: $3t - 6 > 0 \Rightarrow t > 2$

**(b)** $a(t) = 3$ (constant acceleration)

</details>

---

<details>
<summary><strong>Solution 3</strong></summary>

**Problem:** $s(t) = \sin(t)$, find $v$ and $a$ at $t = \frac{\pi}{2}$

$v(t) = \cos(t)$, so $v(\frac{\pi}{2}) = \cos(\frac{\pi}{2}) = 0$

$a(t) = -\sin(t)$, so $a(\frac{\pi}{2}) = -\sin(\frac{\pi}{2}) = -1$

**Answer:** $v = 0$, $a = -1$ (at rest, accelerating downward)

</details>

---

<details>
<summary><strong>Solution 4</strong></summary>

**Problem:** $v(t) = t^2 - 4$, $s(0) = 5$

$$s(t) = \int (t^2 - 4) \, dt = \frac{t^3}{3} - 4t + C$$

$s(0) = 5$: $0 - 0 + C = 5 \Rightarrow C = 5$

**Answer:** $s(t) = \frac{t^3}{3} - 4t + 5$

</details>

---

<details>
<summary><strong>Solution 5</strong></summary>

**Problem:** Displacement with $v(t) = 2t - 1$ from $t = 0$ to $t = 3$

$$\text{Displacement} = \int_0^3 (2t - 1) \, dt = [t^2 - t]_0^3 = (9 - 3) - 0 = 6$$

**Answer:** 6 units

</details>

---

<details>
<summary><strong>Solution 6</strong></summary>

**Problem:** $s(t) = t^3 - 9t^2 + 24t$

$v(t) = 3t^2 - 18t + 24 = 3(t^2 - 6t + 8) = 3(t-2)(t-4)$

$a(t) = 6t - 18 = 6(t - 3)$

**(a)** At rest: $t = 2$ and $t = 4$

**(b)** Moving left when $v(t) < 0$: $2 < t < 4$

**(c)** Speeding up when $v$ and $a$ have same sign:

| Interval | $v$ | $a$ | Speeding up? |
|----------|-----|-----|--------------|
| $0 < t < 2$ | $+$ | $-$ | No |
| $2 < t < 3$ | $-$ | $-$ | Yes |
| $3 < t < 4$ | $-$ | $+$ | No |
| $t > 4$ | $+$ | $+$ | Yes |

**Answer:** Speeding up on $(2, 3) \cup (4, \infty)$

</details>

---

<details>
<summary><strong>Solution 7</strong></summary>

**Problem:** Total distance for $s(t) = t^3 - 6t^2 + 9t$ from $t = 0$ to $t = 4$

$v(t) = 3t^2 - 12t + 9 = 3(t-1)(t-3)$

Direction changes at $t = 1$ and $t = 3$

$s(0) = 0$, $s(1) = 1 - 6 + 9 = 4$, $s(3) = 27 - 54 + 27 = 0$, $s(4) = 64 - 96 + 36 = 4$

Total distance $= |4 - 0| + |0 - 4| + |4 - 0| = 4 + 4 + 4 = 12$

**Answer:** 12 units

</details>

---

<details>
<summary><strong>Solution 8</strong></summary>

**Problem:** $a = -10$, $v(0) = 20$, $s(0) = 0$

$v(t) = -10t + 20$

$s(t) = -5t^2 + 20t$

Returns to start when $s(t) = 0$:

$-5t^2 + 20t = 0$
$-5t(t - 4) = 0$
$t = 0$ or $t = 4$

**Answer:** $t = 4$ seconds

</details>

---

<details>
<summary><strong>Solution 9</strong></summary>

**Problem:** $s(t) = e^{-t}\cos(t)$

$v(t) = -e^{-t}\cos(t) + e^{-t}(-\sin(t)) = -e^{-t}(\cos(t) + \sin(t))$

$v(0) = -e^0(1 + 0) = -1$

$a(t) = e^{-t}(\cos(t) + \sin(t)) + (-e^{-t})(-\sin(t) + \cos(t))$
$= e^{-t}(\cos(t) + \sin(t) + \sin(t) - \cos(t)) = 2e^{-t}\sin(t)$

$a(0) = 2e^0(0) = 0$

**Answer:** $v(0) = -1$, $a(0) = 0$

</details>

---

<details>
<summary><strong>Solution 10</strong></summary>

**Problem:** $v(t) = (t-1)(t-3)^2$

$v(t) = 0$ at $t = 1$ and $t = 3$

Check sign changes:
- At $t = 1$: $(t-1)$ changes sign, $(t-3)^2$ doesn't → $v$ changes sign
- At $t = 3$: $(t-3)^2$ doesn't change sign → $v$ doesn't change sign

**Answer:** Direction changes only at $t = 1$

</details>

---

<details>
<summary><strong>Solution 11</strong></summary>

**Problem:** $s(t) = -16t^2 + 64t + 80$

$v(t) = -32t + 64$

**(a)** Maximum height when $v = 0$: $t = 2$

$s(2) = -64 + 128 + 80 = 144$ feet

**(b)** Hits ground when $s(t) = 0$:

$-16t^2 + 64t + 80 = 0$
$t^2 - 4t - 5 = 0$
$(t-5)(t+1) = 0$
$t = 5$ (positive)

**(c)** Speed at impact: $|v(5)| = |-32(5) + 64| = |-96| = 96$ ft/s

</details>

---

<details>
<summary><strong>Solution 12</strong></summary>

**Problem:** $a(t) = \sin(t)$, $v(0) = 1$, $s(0) = 0$

$v(t) = \int \sin(t) \, dt = -\cos(t) + C_1$

$v(0) = 1$: $-1 + C_1 = 1 \Rightarrow C_1 = 2$

$v(t) = -\cos(t) + 2$

$s(t) = \int (-\cos(t) + 2) \, dt = -\sin(t) + 2t + C_2$

$s(0) = 0$: $0 + 0 + C_2 = 0 \Rightarrow C_2 = 0$

**Answer:** $s(t) = -\sin(t) + 2t$

</details>

---

<details>
<summary><strong>Solution 13</strong></summary>

**Problem:** When is $s(t) = t\ln(t)$ speeding up for $t > 0$?

$v(t) = \ln(t) + 1$

$a(t) = \frac{1}{t}$

Since $t > 0$, $a(t) > 0$ always.

Speeding up when $v(t) > 0$ (same sign as $a$):

$\ln(t) + 1 > 0$
$\ln(t) > -1$
$t > e^{-1} = \frac{1}{e}$

**Answer:** $t > \frac{1}{e}$

</details>

---

<details>
<summary><strong>Solution 14</strong></summary>

**Problem:** $s_1(t) = t^2$, $s_2(t) = 2t + 3$

$v_1(t) = 2t$, $v_2(t) = 2$

Same velocity when $2t = 2 \Rightarrow t = 1$

**Answer:** $t = 1$

</details>

---

<details>
<summary><strong>Solution 15</strong></summary>

**Problem:** Total distance for $s(t) = \sin(t)$ from $t = 0$ to $t = 2\pi$

$v(t) = \cos(t) = 0$ at $t = \frac{\pi}{2}, \frac{3\pi}{2}$

$s(0) = 0$, $s(\frac{\pi}{2}) = 1$, $s(\frac{3\pi}{2}) = -1$, $s(2\pi) = 0$

Distance $= |1 - 0| + |-1 - 1| + |0 - (-1)| = 1 + 2 + 1 = 4$

**Answer:** 4 units

</details>

---

<details>
<summary><strong>Solution 16</strong></summary>

**Problem:** $v(t) = t^2 - 5t + 4 = (t-1)(t-4)$

$v(t) < 0$ (moving left) when $1 < t < 4$

**Answer:** **(B)** $1 < t < 4$

</details>

---

<details>
<summary><strong>Solution 17</strong></summary>

**Problem:** $s(t) = t^3 - 3t^2$, total distance from $t = 0$ to $t = 3$

$v(t) = 3t^2 - 6t = 3t(t - 2)$

$v = 0$ at $t = 0, 2$

$s(0) = 0$, $s(2) = 8 - 12 = -4$, $s(3) = 27 - 27 = 0$

Distance $= |{-4} - 0| + |0 - ({-4})| = 4 + 4 = 8$

**Answer:** **(C)** $8$

</details>

---

<details>
<summary><strong>Solution 18</strong></summary>

**Problem:** $v(t) = \cos(\pi t)$, $x(0) = 1$

**(a)** $a(t) = -\pi\sin(\pi t)$

$a(1) = -\pi\sin(\pi) = 0$

**(b)** At rest when $\cos(\pi t) = 0$:

$\pi t = \frac{\pi}{2}, \frac{3\pi}{2}, \frac{5\pi}{2}$

$t = \frac{1}{2}, \frac{3}{2}, \frac{5}{2}$

**(c)** $x(t) = x(0) + \int_0^t \cos(\pi \tau) \, d\tau = 1 + \frac{\sin(\pi t)}{\pi}$

$x(1) = 1 + \frac{\sin(\pi)}{\pi} = 1 + 0 = 1$

**(d)** Direction changes at $t = \frac{1}{2}, \frac{3}{2}, \frac{5}{2}$

$x(0) = 1$, $x(\frac{1}{2}) = 1 + \frac{1}{\pi}$, $x(\frac{3}{2}) = 1 - \frac{1}{\pi}$, $x(\frac{5}{2}) = 1 + \frac{1}{\pi}$, $x(3) = 1$

Distance $= \frac{1}{\pi} + \frac{2}{\pi} + \frac{2}{\pi} + \frac{1}{\pi} = \frac{6}{\pi}$

</details>

---

<details>
<summary><strong>Solution 19</strong></summary>

**Problem:** $v(t) = 3t^2 - 12t + 9 = 3(t-1)(t-3)$

$a(t) = 6t - 12 = 6(t-2)$

| Interval | $v$ | $a$ | Same sign? |
|----------|-----|-----|------------|
| $0 < t < 1$ | $+$ | $-$ | No |
| $1 < t < 2$ | $-$ | $-$ | Yes |
| $2 < t < 3$ | $-$ | $+$ | No |
| $t > 3$ | $+$ | $+$ | Yes |

**Answer:** **(B)** $1 < t < 2$ (also $t > 3$, but not an option)

</details>

---

<details>
<summary><strong>Solution 20</strong></summary>

**Problem:** $x(t) = te^{-t}$

**(a)** $v(t) = e^{-t} - te^{-t} = e^{-t}(1 - t)$

$a(t) = -e^{-t}(1-t) + e^{-t}(-1) = e^{-t}(t - 2)$

**(b)** Maximum distance when $v = 0$: $t = 1$

$x(1) = e^{-1} = \frac{1}{e}$

**(c)** $\lim_{t \to \infty} te^{-t} = \lim_{t \to \infty} \frac{t}{e^t} = 0$ (by L'Hôpital's or exponential dominance)

**(d)** Moving left when $v < 0$, i.e., $t > 1$

Fastest left = minimum of $v(t)$ for $t > 1$

$v'(t) = a(t) = e^{-t}(t-2) = 0$ at $t = 2$

For $1 < t < 2$: $a < 0$ (velocity decreasing, so getting more negative)
For $t > 2$: $a > 0$ (velocity increasing toward 0)

Maximum leftward speed at $t = 2$: $|v(2)| = e^{-2}$

</details>

---

## What's Next

Now that you understand motion along a line, you're ready for [Related Rates](/calculus/related-rates), where you'll apply derivatives to find how quantities that are related to each other change over time.

---

<div align="center">

[← Higher-Order Derivatives](/calculus/higher-order-derivatives) | [Related Rates →](/calculus/related-rates)

</div>
