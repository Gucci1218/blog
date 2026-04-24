# Slope Fields
<p class="article-date">April 23, 2026</p>

*Imagine you're standing on the cliffs at Torrey Pines, watching the ocean currents below. At every point in the water, the current has a direction — some spots pull north, others swirl east, and near the rocks the water barely moves. If you dropped a leaf into the water, it would trace a path determined by those local currents. Slope fields work the same way: they show you the "current" of a differential equation at every point, and solution curves are the paths a leaf would follow.*

---

## What You'll Learn
- Understand what a slope field is and why it's useful
- Draw slope fields from a given differential equation
- Read a slope field to identify key features of solutions
- Match differential equations to their slope fields
- Sketch solution curves through a given initial condition
- Recognize equilibrium solutions from a slope field

---

## Prerequisites
- [Derivative Definition](/calculus/0301-derivative-definition)
- [Basic Derivative Rules](/calculus/0304-basic-derivative-rules)
- [Curve Sketching](/calculus/0505-curve-sketching)

---

## The Core Concept

### Intuition First

Think about driving down the I-5 from San Diego to LA. At every point along the freeway, your GPS shows you a tiny arrow — your current direction and steepness (are you climbing a hill? descending toward the coast?). Now imagine painting those tiny arrows at *every* point on a map, not just along the freeway. You'd have a picture that shows, from *any* starting point, which direction you'd naturally head.

That's a **slope field** (also called a **direction field**). A differential equation like $\frac{dy}{dx} = x + y$ tells you the slope at every point $(x, y)$. A slope field is the visual map of all those slopes.

### The Definition

Given a differential equation of the form:

$$\frac{dy}{dx} = f(x, y)$$

A **slope field** is a grid of short line segments where, at each point $(x, y)$, the segment has slope $f(x, y)$.

Each tiny segment answers the question: *"If a solution curve passed through this exact point, what direction would it be heading?"*

### Why Slope Fields Matter

Most differential equations **can't be solved with a formula**. Unlike the neat equations you've been solving all year, real-world DEs often have no closed-form solution. Slope fields let you:

1. **Visualize** the behavior of solutions without solving
2. **Sketch** approximate solution curves
3. **Identify** long-term behavior (does the solution grow? stabilize? oscillate?)
4. **Verify** if a proposed solution makes sense

---

## How to Draw a Slope Field

### Step-by-Step Process

**Given:** $\frac{dy}{dx} = f(x, y)$

1. Choose a grid of points $(x, y)$
2. At each point, compute the slope $m = f(x, y)$
3. Draw a short line segment with that slope at that point

### Example 1: Drawing a Slope Field

**Draw the slope field for** $\frac{dy}{dx} = x - y$

**Step 1:** Build a slope table for selected points:

| $(x, y)$ | $\frac{dy}{dx} = x - y$ | Slope |
|-----------|--------------------------|-------|
| $(0, 0)$ | $0 - 0$ | $0$ (horizontal) |
| $(1, 0)$ | $1 - 0$ | $1$ (diagonal up-right) |
| $(0, 1)$ | $0 - 1$ | $-1$ (diagonal down-right) |
| $(1, 1)$ | $1 - 1$ | $0$ (horizontal) |
| $(2, 1)$ | $2 - 1$ | $1$ |
| $(1, 2)$ | $1 - 2$ | $-1$ |
| $(2, 2)$ | $2 - 2$ | $0$ (horizontal) |
| $(-1, 0)$ | $-1 - 0$ | $-1$ |
| $(0, -1)$ | $0 - (-1)$ | $1$ |

**Step 2:** Notice the pattern — the slope is zero whenever $x = y$ (along the line $y = x$). Above that line, slopes are negative; below, slopes are positive.

```
     y
     |  \  \  —  /  /
     |  \  \  —  /  /
     |  \  \  —  /  /
     |  \  —  /  /  /
     |  —  /  /  /  /
     +—————————————————→ x
        (slopes = 0 along y = x)
```

**Key insight:** Solutions are "attracted" toward the line $y = x$. No matter where you start, the solution curves approach this line.

---

### Example 2: Slope Depends Only on $y$

**Draw the slope field for** $\frac{dy}{dx} = y$

| $y$ value | Slope |
|-----------|-------|
| $y = 2$ | $2$ (steep upward) |
| $y = 1$ | $1$ |
| $y = 0$ | $0$ (horizontal) |
| $y = -1$ | $-1$ |
| $y = -2$ | $-2$ (steep downward) |

**Notice:** The slope depends *only* on $y$, not $x$. This means every point in the same horizontal row has the same slope. The segments form horizontal bands.

This is like the temperature of the ocean at different depths near La Jolla Cove — it doesn't matter whether you're 100 meters north or south along the shore; at the same depth, the temperature (and the rate it changes) is the same.

**Solution:** We know $\frac{dy}{dx} = y$ has the solution $y = Ce^x$. The slope field confirms this — the curves are exponential, growing above the x-axis and decaying below it.

---

### Example 3: Slope Depends Only on $x$

**Draw the slope field for** $\frac{dy}{dx} = \cos(x)$

| $x$ value | Slope |
|-----------|-------|
| $x = 0$ | $1$ |
| $x = \frac{\pi}{2}$ | $0$ |
| $x = \pi$ | $-1$ |
| $x = \frac{3\pi}{2}$ | $0$ |
| $x = 2\pi$ | $1$ |

**Notice:** The slope depends *only* on $x$. Every point in the same vertical column has the same slope.

**Solution:** $y = \sin(x) + C$ — a family of sine curves, each shifted vertically by a different constant.

---

## Reading Slope Fields

### What to Look For

When you see a slope field on the AP exam, train your eye to spot these features:

| Feature | What It Means |
|---------|---------------|
| Horizontal segments ($m = 0$) | Points where $\frac{dy}{dx} = 0$ — possible max/min of solutions |
| All segments in a row same | Slope depends only on $y$ |
| All segments in a column same | Slope depends only on $x$ |
| Segments get steeper | Solution curves are accelerating (concavity) |
| Segments point toward a line | That line is an equilibrium or attractor |
| Vertical segments ($m \to \infty$) | Solution curve is nearly vertical — possible undefined behavior |

### Isoclines

An **isocline** is a curve along which all slopes are equal. Setting $f(x, y) = c$ for a constant $c$ gives you the isocline for slope $c$.

**Example:** For $\frac{dy}{dx} = x + y$:
- Isocline for slope $0$: $x + y = 0$ → $y = -x$ (all segments along this line are horizontal)
- Isocline for slope $1$: $x + y = 1$ → $y = 1 - x$
- Isocline for slope $-2$: $x + y = -2$ → $y = -2 - x$

These are parallel lines — a nice pattern that makes the slope field easier to draw.

Think of it like contour lines on a hiking trail map at Torrey Pines. Each contour connects points at the same elevation. Isoclines connect points with the same slope.

---

## Equilibrium Solutions

An **equilibrium solution** (also called a **constant solution**) is a horizontal line $y = k$ where the slope field shows all horizontal segments.

For $\frac{dy}{dx} = f(x, y)$, if $f(x, k) = 0$ for all $x$, then $y = k$ is an equilibrium solution.

### Example 4: Finding Equilibrium Solutions

**Find the equilibrium solutions for** $\frac{dy}{dx} = y(y - 2)$

Set $\frac{dy}{dx} = 0$:

$$y(y - 2) = 0$$

$$y = 0 \quad \text{or} \quad y = 2$$

**These are the equilibrium solutions.** The slope field has horizontal segments along both $y = 0$ and $y = 2$.

**Stability analysis** (by checking slopes):

| Region | $y(y-2)$ | Slope | Behavior |
|--------|----------|-------|----------|
| $y > 2$ | $(+)(+)$ | Positive | Solutions rise away from $y = 2$ |
| $0 < y < 2$ | $(+)(-)$ | Negative | Solutions fall toward $y = 0$ |
| $y < 0$ | $(-)(-)$ | Positive | Solutions rise toward $y = 0$ |

- $y = 0$ is **stable** (nearby solutions are attracted to it)
- $y = 2$ is **unstable** (nearby solutions move away from it)

Think of it like dancing to your favorite K-pop track. A stable equilibrium is like the chorus — no matter how wild the verses get, the song always pulls you back to that same catchy hook. An unstable equilibrium is like trying to hold a freeze pose mid-dance — the slightest wobble sends you tumbling away from that perfect balance point.

---

## Matching DEs to Slope Fields

### Strategy for AP Exam

When asked to match a differential equation to a slope field:

1. **Check easy points** — plug in $(0, 0)$, $(1, 0)$, $(0, 1)$ and compare slopes
2. **Look for horizontal segments** — where does $\frac{dy}{dx} = 0$?
3. **Check dependence** — does slope depend on $x$ only? $y$ only? Both?
4. **Check sign patterns** — where are slopes positive vs. negative?

### Example 5: Matching Practice

**Which DE matches a slope field where all segments along the x-axis are horizontal, and slopes get steeper as you move away from the x-axis (positive above, negative below)?**

- (A) $\frac{dy}{dx} = x$
- (B) $\frac{dy}{dx} = y$
- (C) $\frac{dy}{dx} = x + y$
- (D) $\frac{dy}{dx} = xy$

**Solution:**

- Horizontal along x-axis means $\frac{dy}{dx} = 0$ when $y = 0$. This eliminates (A) since $\frac{dy}{dx} = x \neq 0$ for most points on the x-axis.
- Positive above x-axis, negative below → (B) $\frac{dy}{dx} = y$ works.
- But check: "steeper as you move away" in *all* directions?
- For (B): slope at $(0, 2)$ is $2$, slope at $(3, 2)$ is also $2$. Slope doesn't depend on $x$, so segments in each row are identical. ✓
- For (D): slope at $(0, 2)$ is $0$, slope at $(3, 2)$ is $6$. Slope varies along rows. ✗

**Answer: (B)**

---

## Sketching Solution Curves

### How to Sketch a Solution Curve

Given a slope field and an initial condition $(x_0, y_0)$:

1. Start at the point $(x_0, y_0)$
2. Follow the direction of the nearby line segments
3. Draw a smooth curve that is tangent to each segment it passes through
4. Extend in both directions (left and right)

**The golden rule:** Your curve should *never* cross a line segment at an angle. It should always flow *along* the direction of the segments, like a leaf floating on ocean currents.

### Example 6: Sketching Through Initial Conditions

**For** $\frac{dy}{dx} = y - x$**, sketch the solution through $(0, 1)$.**

At $(0, 1)$: slope $= 1 - 0 = 1$ → start heading up-right at 45°

At $(0.5, 1.5)$: slope $= 1.5 - 0.5 = 1$ → still heading up at 45°

At $(1, 2)$: slope $= 2 - 1 = 1$ → still 45° (we're on the isocline $y - x = 1$!)

**Wait** — along $y = x + 1$, the slope is always $1$, and the line $y = x + 1$ itself has slope $1$. So $y = x + 1$ is actually a solution! We happened to start on it.

This is a beautiful result: the isocline for slope $1$ is itself a solution curve with slope $1$.

---

## Worked Examples

### Example 7: Complete Analysis

**For the DE** $\frac{dy}{dx} = 2 - y$:

**(a)** Find the equilibrium solution.

$\frac{dy}{dx} = 0$ when $2 - y = 0$, so $y = 2$.

**(b)** Describe the slope field.

| Region | Slope | Direction |
|--------|-------|-----------|
| $y < 2$ | Positive | Solutions rise toward $y = 2$ |
| $y = 2$ | Zero | Horizontal — equilibrium |
| $y > 2$ | Negative | Solutions fall toward $y = 2$ |

**(c)** Is the equilibrium stable or unstable?

**Stable** — solutions above and below are both attracted to $y = 2$.

**(d)** This models cooling! Think of stepping out of the ocean at Coronado Beach on a day when the air is 72°F. If you're colder than 72°, you warm up; if you're warmer, you cool down. Your temperature approaches 72° over time. The equilibrium $y = 2$ represents the ambient temperature.

---

### Example 8: Slope Field with Multiple Equilibria

**For** $\frac{dy}{dx} = y(1 - y)(y - 3)$**, analyze the slope field.**

**Equilibrium solutions:** $y = 0$, $y = 1$, $y = 3$

**Sign analysis:**

| Region | Sign of $y$ | Sign of $(1-y)$ | Sign of $(y-3)$ | Slope | Behavior |
|--------|-------------|------------------|-----------------|-------|----------|
| $y > 3$ | $+$ | $-$ | $+$ | $-$ | Falls toward $y = 3$ |
| $1 < y < 3$ | $+$ | $-$ | $-$ | $+$ | Rises toward $y = 3$ |
| $0 < y < 1$ | $+$ | $+$ | $-$ | $-$ | Falls toward $y = 0$ |
| $y < 0$ | $-$ | $+$ | $-$ | $+$ | Rises toward $y = 0$ |

**Stability:**
- $y = 0$: **Stable** (solutions above and below approach it)
- $y = 1$: **Unstable** (solutions move away)
- $y = 3$: **Stable** (solutions above and below approach it)

---

## Key Formulas & Rules

| Concept | Key Point |
|---------|-----------|
| Slope field | Grid of segments with slope $f(x, y)$ at each point $(x, y)$ |
| Isocline | Curve where $f(x, y) = c$ (constant slope) |
| Null isocline | Where $f(x, y) = 0$ (horizontal segments) |
| Equilibrium | Constant solution $y = k$ where $f(x, k) = 0$ for all $x$ |
| Stable equilibrium | Nearby solutions approach it |
| Unstable equilibrium | Nearby solutions move away |
| Solution curve | Smooth curve tangent to slope field at every point |

**Quick matching checklist:**
1. Where are the horizontal segments? → Set $\frac{dy}{dx} = 0$
2. Does slope depend on $x$, $y$, or both?
3. Where are slopes positive? Negative?
4. Do solutions appear to converge or diverge?

---

## Common Mistakes to Avoid

### Mistake 1: Drawing Segments Too Long

Slope field segments should be short and uniform in length. Long segments make it look like you're drawing solution curves, not a field.

---

### Mistake 2: Crossing Equilibrium Solutions

Solution curves **cannot cross** equilibrium solutions (or any other solution curve, by the uniqueness theorem). If $y = 2$ is an equilibrium, a solution starting at $y = 1$ will approach $y = 2$ but never reach or cross it.

Think of it like the lanes of the I-5 — two cars in different lanes might get closer, but they can't occupy the same lane at the same time without a collision.

---

### Mistake 3: Confusing the Isocline with the Solution

The isocline for slope $m$ is where $f(x, y) = m$. This is *not* necessarily a solution curve. The only time an isocline is also a solution is when the slope of the isocline itself equals $m$ (like we saw in Example 6).

---

### Mistake 4: Ignoring the Direction of Flow

When sketching solution curves, make sure you draw them flowing in the direction of increasing $x$ (left to right). The slopes tell you the *direction* of the curve, not just its shape.

---

### Mistake 5: Drawing Solution Curves That Cross Each Other

By the **Existence and Uniqueness Theorem**, two different solution curves to the same DE cannot intersect (as long as $f(x, y)$ is continuous and "well-behaved"). If your sketch has crossing curves, something is wrong.

---

## AP Exam Tips

### For AB:
- Slope fields appear regularly on both multiple choice and free response
- You should be able to **draw** a slope field from a DE (usually at 12–16 points)
- You should be able to **sketch a solution curve** through a given point on a slope field
- You should be able to **match** a DE to its slope field

### For BC:
- Same as AB, plus connection to Euler's method (next article)
- May need to identify stability of equilibrium solutions

### Common Free Response Format

The AP exam loves this structure:
1. "Draw the slope field at the 12 indicated points"
2. "Sketch the solution through the point $(0, 1)$"
3. "Find the equilibrium solution(s)"
4. "Is the equilibrium stable or unstable? Justify."

### Time-Saving Strategy

When matching DEs to slope fields on multiple choice:
- **First**, check $(0, 0)$ — it eliminates wrong answers fast
- **Second**, check where $\frac{dy}{dx} = 0$ — compare with horizontal segments
- **Third**, check if slopes depend on $x$ only, $y$ only, or both

---

## Practice Problems

### Basic (Problems 1-5)

**1.** For $\frac{dy}{dx} = x + 1$, compute the slope at the following points: $(0, 0)$, $(1, 2)$, $(-1, 3)$, $(2, -1)$.

---

**2.** For $\frac{dy}{dx} = y - 1$, describe the slope field. Where are the horizontal segments? Does the slope depend on $x$?

---

**3.** Find all equilibrium solutions for $\frac{dy}{dx} = (y - 1)(y + 3)$.

---

**4.** For $\frac{dy}{dx} = -\frac{x}{y}$, compute slopes at $(1, 1)$, $(1, -1)$, $(2, 1)$, and $(0, 3)$. What shape do the solution curves appear to be?

---

**5.** True or False:
- (a) Two different solution curves of the same DE can intersect.
- (b) A solution curve must be tangent to every slope segment it passes through.
- (c) If $\frac{dy}{dx} = f(y)$ (depends only on $y$), then all segments in the same row are identical.

---

### Intermediate (Problems 6-10)

**6.** For $\frac{dy}{dx} = y(2 - y)$:
- (a) Find all equilibrium solutions.
- (b) Determine the stability of each equilibrium.
- (c) Sketch the solution curve through $(0, 1)$.

---

**7.** Find the isoclines for $\frac{dy}{dx} = 2x - y$ corresponding to slopes $m = 0$, $m = 1$, and $m = -1$. What shape are they?

---

**8.** A slope field shows horizontal segments along the curve $y = x^2$. Which DE could produce this field?

| Choice | DE |
|--------|----|
| **(A)** | $\frac{dy}{dx} = y - x^2$ |
| **(B)** | $\frac{dy}{dx} = x^2 - y$ |
| **(C)** | $\frac{dy}{dx} = y + x^2$ |
| **(D)** | $\frac{dy}{dx} = x - y^2$ |

---

**9.** For $\frac{dy}{dx} = \sin(y)$, find:
- (a) All equilibrium solutions
- (b) Which equilibria are stable and which are unstable

---

**10.** A slope field has the following properties:
- All segments along the y-axis have slope $0$
- Slopes are positive to the right of the y-axis
- Slopes are negative to the left of the y-axis
- Slope magnitude increases with distance from the y-axis

Which DE matches?

| Choice | DE |
|--------|----|
| **(A)** | $\frac{dy}{dx} = x$ |
| **(B)** | $\frac{dy}{dx} = y$ |
| **(C)** | $\frac{dy}{dx} = x^2$ |
| **(D)** | $\frac{dy}{dx} = xy$ |

---

### Advanced (Problems 11-15)

**11.** For $\frac{dy}{dx} = y^2 - 4$:
- (a) Find all equilibrium solutions.
- (b) Classify each as stable or unstable.
- (c) If $y(0) = 1$, describe the long-term behavior of the solution.
- (d) If $y(0) = 3$, describe the long-term behavior.

---

**12.** Consider $\frac{dy}{dx} = e^{-y} - 1$.
- (a) Find the equilibrium solution.
- (b) Determine its stability.
- (c) What happens to solutions as $y \to -\infty$? As $y \to +\infty$?

---

**13.** A slope field for $\frac{dy}{dx} = f(x, y)$ shows that:
- Slopes are $0$ along both axes
- In quadrant I, slopes are positive
- In quadrant III, slopes are positive
- In quadrants II and IV, slopes are negative

Show that $f(x, y) = xy$ is consistent with these observations, and find the isoclines.

---

**14.** For the DE $\frac{dy}{dx} = \frac{x + y}{x - y}$:
- (a) Where is the slope undefined?
- (b) Where is the slope zero?
- (c) Where is the slope equal to $1$?
- (d) What type of curves are the solutions? *(Hint: convert to polar)*

---

**15.** Suppose a slope field has the property that rotating it 90° clockwise produces the same field. What can you conclude about the DE?

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

The slope field for a DE is shown to have horizontal segments along the line $y = 3$ and vertical symmetry about the y-axis. Which could be the DE?

| Choice | DE |
|--------|----|
| **(A)** | $\frac{dy}{dx} = y - 3$ |
| **(B)** | $\frac{dy}{dx} = x(y - 3)$ |
| **(C)** | $\frac{dy}{dx} = 3 - y + x$ |
| **(D)** | $\frac{dy}{dx} = x + y$ |

---

#### Problem 17 (Multiple Choice)

For $\frac{dy}{dx} = y(1 - y)$, which statement is true?

| Choice | Statement |
|--------|-----------|
| **(A)** | $y = 0$ is stable and $y = 1$ is unstable |
| **(B)** | $y = 0$ is unstable and $y = 1$ is stable |
| **(C)** | Both $y = 0$ and $y = 1$ are stable |
| **(D)** | Both $y = 0$ and $y = 1$ are unstable |

---

#### Problem 18 (Free Response)

Consider the differential equation $\frac{dy}{dx} = y - y^2$.

> **(a)** Sketch the slope field at the twelve points indicated: $x = -1, 0, 1$ and $y = -1, 0, 1, 2$.
>
> **(b)** Sketch the solution curve through the initial condition $y(0) = 0.5$.
>
> **(c)** Find all equilibrium solutions and classify their stability.
>
> **(d)** If $y(0) = 0.5$, what is $\lim_{x \to \infty} y(x)$? Justify your answer.

---

#### Problem 19 (Multiple Choice)

A slope field is drawn for $\frac{dy}{dx} = f(x, y)$. The segments at all points of the form $(x, 2)$ are horizontal, and the segments at all points of the form $(x, 0)$ are also horizontal. For points between $y = 0$ and $y = 2$, all slopes are positive. Which could be $f(x, y)$?

| Choice | $f(x, y)$ |
|--------|-----------|
| **(A)** | $y^2 - 2y$ |
| **(B)** | $2y - y^2$ |
| **(C)** | $(y - 2)^2$ |
| **(D)** | $y^2 + 2y$ |

---

#### Problem 20 (Free Response — Challenging)

The temperature $T$ (in °F) of a cup of chai changes according to the differential equation:

$$\frac{dT}{dt} = -0.05(T - 72)$$

where $t$ is time in minutes and $72°F$ is the ambient room temperature.

> **(a)** Draw the slope field for this DE on the axes with $0 \leq t \leq 20$ and $50 \leq T \leq 150$ at the points $t = 0, 5, 10, 15, 20$ and $T = 50, 72, 90, 110, 130, 150$.
>
> **(b)** If the chai starts at $150°F$, sketch the solution curve. Describe what happens physically.
>
> **(c)** If the chai starts at $50°F$ (say you grabbed an iced chai from a Balboa Park cafe and brought it indoors), sketch the solution curve. Describe what happens.
>
> **(d)** Find the equilibrium solution and classify its stability. Explain why this makes physical sense.
>
> **(e)** Without solving the DE, explain why no cup of chai at $150°F$ will ever cool below $72°F$.

---

## Answer Key

<details>
<summary><strong>Problem 1 Solution</strong></summary>

**For** $\frac{dy}{dx} = x + 1$:

| Point | Slope |
|-------|-------|
| $(0, 0)$ | $0 + 1 = 1$ |
| $(1, 2)$ | $1 + 1 = 2$ |
| $(-1, 3)$ | $-1 + 1 = 0$ |
| $(2, -1)$ | $2 + 1 = 3$ |

**Note:** The slope depends only on $x$, so all points in the same column have the same slope. The $y$-coordinate doesn't matter.

</details>

---

<details>
<summary><strong>Problem 2 Solution</strong></summary>

**For** $\frac{dy}{dx} = y - 1$:

- **Horizontal segments** where $y - 1 = 0$, i.e., along $y = 1$
- **No dependence on $x$** — all segments in the same row are identical
- **Above $y = 1$**: slopes are positive (solutions rise)
- **Below $y = 1$**: slopes are negative (solutions fall)
- $y = 1$ is a **stable** equilibrium — solutions approach it from both sides

</details>

---

<details>
<summary><strong>Problem 3 Solution</strong></summary>

**For** $\frac{dy}{dx} = (y - 1)(y + 3)$:

Set $(y - 1)(y + 3) = 0$:

$$y = 1 \quad \text{or} \quad y = -3$$

**Equilibrium solutions:** $y = 1$ and $y = -3$

</details>

---

<details>
<summary><strong>Problem 4 Solution</strong></summary>

**For** $\frac{dy}{dx} = -\frac{x}{y}$:

| Point | Slope |
|-------|-------|
| $(1, 1)$ | $-1$ |
| $(1, -1)$ | $1$ |
| $(2, 1)$ | $-2$ |
| $(0, 3)$ | $0$ |

The slopes are perpendicular to the radial direction from the origin. The solution curves are **circles** centered at the origin: $x^2 + y^2 = C$.

**Verification:** If $x^2 + y^2 = C$, then $2x + 2y\frac{dy}{dx} = 0$, giving $\frac{dy}{dx} = -\frac{x}{y}$. ✓

</details>

---

<details>
<summary><strong>Problem 5 Solution</strong></summary>

**(a) False.** By the Existence and Uniqueness Theorem, two different solution curves cannot intersect (assuming $f$ is continuous and satisfies the Lipschitz condition).

**(b) True.** This is the definition of a solution curve — it must be tangent to the slope field at every point.

**(c) True.** If $\frac{dy}{dx} = f(y)$, the slope at $(x, y)$ depends only on the $y$-coordinate. All points with the same $y$ have the same slope, so all segments in a horizontal row are identical.

</details>

---

<details>
<summary><strong>Problem 6 Solution</strong></summary>

**For** $\frac{dy}{dx} = y(2 - y)$:

**(a)** Equilibrium solutions: $y = 0$ and $y = 2$

**(b)** Sign analysis:

| Region | $y$ | $2 - y$ | Slope | Direction |
|--------|-----|---------|-------|-----------|
| $y > 2$ | $+$ | $-$ | $-$ | Falls toward $y = 2$ |
| $0 < y < 2$ | $+$ | $+$ | $+$ | Rises toward $y = 2$ |
| $y < 0$ | $-$ | $+$ | $-$ | Falls away from $y = 0$ |

- $y = 2$ is **stable** (solutions approach from both sides)
- $y = 0$ is **unstable** (solutions above rise away; solutions below fall away)

**(c)** Starting at $(0, 1)$: $y$ is between $0$ and $2$, so slopes are positive. The solution rises and approaches $y = 2$ as $x \to \infty$.

</details>

---

<details>
<summary><strong>Problem 7 Solution</strong></summary>

**For** $\frac{dy}{dx} = 2x - y$, isoclines where $2x - y = m$, i.e., $y = 2x - m$:

- $m = 0$: $y = 2x$ (all segments are horizontal along this line)
- $m = 1$: $y = 2x - 1$
- $m = -1$: $y = 2x + 1$

These are **parallel lines**, all with slope $2$.

</details>

---

<details>
<summary><strong>Problem 8 Solution</strong></summary>

**Answer: (A)** $\frac{dy}{dx} = y - x^2$

Horizontal segments occur where $\frac{dy}{dx} = 0$.

- **(A)** $y - x^2 = 0$ → $y = x^2$ ✓
- **(B)** $x^2 - y = 0$ → $y = x^2$ ✓ (also works!)

Wait — both (A) and (B) have horizontal segments along $y = x^2$. We need more info to distinguish them. Check slopes above and below:

For a point above $y = x^2$, say $(0, 1)$:
- **(A)**: $1 - 0 = 1 > 0$ (slopes positive above)
- **(B)**: $0 - 1 = -1 < 0$ (slopes negative above)

Without the actual slope field image, both are valid candidates. However, **(A)** gives positive slopes above the parabola (solutions diverge away), while **(B)** gives negative slopes above (solutions fall back toward the parabola).

**Answer: Both (A) and (B)** have horizontal segments along $y = x^2$, but they produce different slope fields. On the AP exam, you'd use the actual picture to decide.

</details>

---

<details>
<summary><strong>Problem 9 Solution</strong></summary>

**For** $\frac{dy}{dx} = \sin(y)$:

**(a)** Equilibrium solutions where $\sin(y) = 0$:

$$y = n\pi \quad \text{for } n = 0, \pm 1, \pm 2, \ldots$$

So $y = 0, \pm\pi, \pm 2\pi, \ldots$

**(b)** Between consecutive equilibria, check the sign of $\sin(y)$:

| Region | $\sin(y)$ | Slope |
|--------|-----------|-------|
| $0 < y < \pi$ | $+$ | Positive (rising) |
| $\pi < y < 2\pi$ | $-$ | Negative (falling) |
| $-\pi < y < 0$ | $-$ | Negative (falling) |

- **Stable:** $y = 0, \pm 2\pi, \pm 4\pi, \ldots$ (even multiples of $\pi$)
- **Unstable:** $y = \pm\pi, \pm 3\pi, \ldots$ (odd multiples of $\pi$)

</details>

---

<details>
<summary><strong>Problem 10 Solution</strong></summary>

**Answer: (A)** $\frac{dy}{dx} = x$

Check the properties:
- Along y-axis ($x = 0$): slope $= 0$ ✓
- Right of y-axis ($x > 0$): positive slopes ✓
- Left of y-axis ($x < 0$): negative slopes ✓
- Magnitude increases with $|x|$ ✓

**Why not (C)?** $\frac{dy}{dx} = x^2$ gives positive slopes on *both* sides of the y-axis, violating the condition that slopes are negative to the left. ✗

**Why not (D)?** $\frac{dy}{dx} = xy$ gives slope $0$ along the y-axis ✓, but also along the x-axis, and the sign depends on both $x$ and $y$. ✗

</details>

---

<details>
<summary><strong>Problem 11 Solution</strong></summary>

**For** $\frac{dy}{dx} = y^2 - 4 = (y-2)(y+2)$:

**(a)** Equilibria: $y = 2$ and $y = -2$

**(b)** Sign analysis:

| Region | $(y-2)$ | $(y+2)$ | Slope | Direction |
|--------|---------|---------|-------|-----------|
| $y > 2$ | $+$ | $+$ | $+$ | Rises away from $y = 2$ |
| $-2 < y < 2$ | $-$ | $+$ | $-$ | Falls toward $y = -2$ |
| $y < -2$ | $-$ | $-$ | $+$ | Rises toward $y = -2$ |

- $y = 2$: **Unstable** (solutions move away)
- $y = -2$: **Stable** (solutions approach from both sides)

**(c)** $y(0) = 1$: We're in $-2 < y < 2$, so slopes are negative. The solution decreases and approaches $y = -2$ as $x \to \infty$.

**(d)** $y(0) = 3$: We're in $y > 2$, so slopes are positive. The solution increases without bound — it blows up to infinity in finite time.

</details>

---

<details>
<summary><strong>Problem 12 Solution</strong></summary>

**For** $\frac{dy}{dx} = e^{-y} - 1$:

**(a)** Equilibrium: $e^{-y} - 1 = 0$ → $e^{-y} = 1$ → $y = 0$

**(b)** Stability:
- For $y > 0$: $e^{-y} < 1$, so $\frac{dy}{dx} < 0$ (falls toward $y = 0$)
- For $y < 0$: $e^{-y} > 1$, so $\frac{dy}{dx} > 0$ (rises toward $y = 0$)

$y = 0$ is **stable**.

**(c)**
- As $y \to -\infty$: $e^{-y} \to \infty$, so slopes become very large and positive
- As $y \to +\infty$: $e^{-y} \to 0$, so $\frac{dy}{dx} \to -1$ (slopes approach $-1$)

</details>

---

<details>
<summary><strong>Problem 13 Solution</strong></summary>

**Verify** $f(x, y) = xy$:

- Along x-axis ($y = 0$): $xy = 0$ ✓ (horizontal)
- Along y-axis ($x = 0$): $xy = 0$ ✓ (horizontal)
- Quadrant I ($x > 0, y > 0$): $xy > 0$ ✓ (positive slopes)
- Quadrant III ($x < 0, y < 0$): $xy > 0$ ✓ (positive slopes)
- Quadrant II ($x < 0, y > 0$): $xy < 0$ ✓ (negative slopes)
- Quadrant IV ($x > 0, y < 0$): $xy < 0$ ✓ (negative slopes)

All observations are consistent. ✓

**Isoclines:** $xy = m$, or $y = \frac{m}{x}$ — these are **hyperbolas** (for $m \neq 0$) and the **coordinate axes** (for $m = 0$).

</details>

---

<details>
<summary><strong>Problem 14 Solution</strong></summary>

**For** $\frac{dy}{dx} = \frac{x + y}{x - y}$:

**(a)** Undefined when $x - y = 0$, i.e., along $y = x$.

**(b)** Slope is zero when $x + y = 0$, i.e., along $y = -x$.

**(c)** Slope $= 1$ when $\frac{x + y}{x - y} = 1$:

$x + y = x - y$ → $2y = 0$ → $y = 0$ (the x-axis, excluding the origin)

**(d)** Converting to polar ($x = r\cos\theta$, $y = r\sin\theta$):

The DE becomes $\frac{dr}{d\theta} = r$ (after computation), which gives $r = Ce^{\theta}$.

The solutions are **logarithmic spirals** — like the spiral patterns you see in seashells at Windansea Beach!

</details>

---

<details>
<summary><strong>Problem 15 Solution</strong></summary>

If rotating the slope field 90° clockwise maps it to itself, then the slope at point $(y, -x)$ (the image of $(x, y)$ under 90° clockwise rotation) must be the original slope rotated by 90° as well.

A 90° clockwise rotation maps a segment with slope $m$ to one with slope $-\frac{1}{m}$ (the negative reciprocal).

So: $f(y, -x) = -\frac{1}{f(x, y)}$

One example: $\frac{dy}{dx} = \frac{x}{y}$ (which has circular solution curves — and circles are rotationally symmetric).

Another: $\frac{dy}{dx} = -\frac{x}{y}$ also works, since its solutions (circles) have the required symmetry.

</details>

---

<details>
<summary><strong>Problem 16 Solution</strong></summary>

**Answer: (B)** $\frac{dy}{dx} = x(y - 3)$

- Horizontal segments along $y = 3$: Need $\frac{dy}{dx} = 0$ when $y = 3$ for all $x$.
  - **(A)** $y - 3 = 0$ ✓ but no vertical symmetry
  - **(B)** $x(y - 3) = 0$ along $y = 3$ ✓
  - **(C)** $3 - y + x = 0$ along $y = 3$ only when $x = 0$ ✗
  - **(D)** $x + y = 0$ along $y = 3$ only when $x = -3$ ✗

- Vertical symmetry (symmetric about y-axis): Need $f(-x, y) = -f(x, y)$ (antisymmetric in $x$, which makes the slope field look symmetric visually — slopes on the left are mirror reflections of slopes on the right).
  - **(A)** $f(-x, y) = y - 3 = f(x, y)$ — same slope, not a mirror ✗
  - **(B)** $f(-x, y) = -x(y - 3) = -f(x, y)$ ✓ — slopes are negated, creating visual symmetry

**Answer: (B)**

</details>

---

<details>
<summary><strong>Problem 17 Solution</strong></summary>

**Answer: (B)** $y = 0$ is unstable and $y = 1$ is stable.

**For** $\frac{dy}{dx} = y(1 - y)$:

| Region | $y$ | $1 - y$ | Slope |
|--------|-----|---------|-------|
| $y > 1$ | $+$ | $-$ | $-$ (falls toward $y = 1$) |
| $0 < y < 1$ | $+$ | $+$ | $+$ (rises toward $y = 1$) |
| $y < 0$ | $-$ | $+$ | $-$ (falls away from $y = 0$) |

- $y = 1$: Stable (solutions approach from both sides)
- $y = 0$: Unstable (solutions above rise away; solutions below fall away)

</details>

---

<details>
<summary><strong>Problem 18 Solution</strong></summary>

**For** $\frac{dy}{dx} = y - y^2 = y(1 - y)$:

**(a)** Slope table:

| $(x, y)$ | $y(1 - y)$ | Slope |
|-----------|-----------|-------|
| $(-1, -1)$ | $(-1)(2)$ | $-2$ |
| $(0, -1)$ | $(-1)(2)$ | $-2$ |
| $(1, -1)$ | $(-1)(2)$ | $-2$ |
| $(-1, 0)$ | $(0)(1)$ | $0$ |
| $(0, 0)$ | $(0)(1)$ | $0$ |
| $(1, 0)$ | $(0)(1)$ | $0$ |
| $(-1, 1)$ | $(1)(0)$ | $0$ |
| $(0, 1)$ | $(1)(0)$ | $0$ |
| $(1, 1)$ | $(1)(0)$ | $0$ |
| $(-1, 2)$ | $(2)(-1)$ | $-2$ |
| $(0, 2)$ | $(2)(-1)$ | $-2$ |
| $(1, 2)$ | $(2)(-1)$ | $-2$ |

Notice: slopes depend only on $y$, so each row is identical.

**(b)** At $(0, 0.5)$: slope $= 0.5(0.5) = 0.25$ (positive). The solution rises, approaching $y = 1$ from below. It's a sigmoid-like curve leveling off at $y = 1$.

**(c)** Equilibria: $y = 0$ (unstable) and $y = 1$ (stable).

**(d)** Since $y(0) = 0.5$ is between $0$ and $1$, the solution rises toward the stable equilibrium:

$$\lim_{x \to \infty} y(x) = 1$$

**Justification:** In the region $0 < y < 1$, $\frac{dy}{dx} > 0$, so $y$ is increasing. The solution cannot cross $y = 1$ (equilibrium), so $y$ increases toward $1$.

</details>

---

<details>
<summary><strong>Problem 19 Solution</strong></summary>

**Answer: (B)** $2y - y^2$

We need:
- $f(x, y) = 0$ when $y = 0$ and $y = 2$
- $f(x, y) > 0$ for $0 < y < 2$

Check each:

- **(A)** $y^2 - 2y = y(y - 2)$: At $y = 1$: $1(1 - 2) = -1 < 0$ ✗
- **(B)** $2y - y^2 = y(2 - y)$: At $y = 1$: $1(2 - 1) = 1 > 0$ ✓, zeros at $y = 0, 2$ ✓
- **(C)** $(y - 2)^2$: At $y = 0$: $(0 - 2)^2 = 4 \neq 0$ ✗
- **(D)** $y^2 + 2y$: At $y = 2$: $4 + 4 = 8 \neq 0$ ✗

**Answer: (B)**

</details>

---

<details>
<summary><strong>Problem 20 Solution</strong></summary>

**For** $\frac{dT}{dt} = -0.05(T - 72)$:

**(a)** Slope table:

| $(t, T)$ | $-0.05(T - 72)$ |
|-----------|-----------------|
| Any $t$, $T = 150$ | $-0.05(78) = -3.9$ |
| Any $t$, $T = 130$ | $-0.05(58) = -2.9$ |
| Any $t$, $T = 110$ | $-0.05(38) = -1.9$ |
| Any $t$, $T = 90$ | $-0.05(18) = -0.9$ |
| Any $t$, $T = 72$ | $0$ (horizontal) |
| Any $t$, $T = 50$ | $-0.05(-22) = 1.1$ |

Slopes depend only on $T$, so each horizontal row has identical segments.

**(b)** Starting at $T = 150°F$: slopes are negative (chai is cooling). The curve decreases, approaching $T = 72°F$ asymptotically. Physically, the hot chai cools toward room temperature — like when Dad makes chai at home and it slowly cools on the kitchen counter while you're picking a K-pop playlist.

**(c)** Starting at $T = 50°F$: slopes are positive (cold chai is warming up). The curve increases, approaching $T = 72°F$ asymptotically. Physically, the cold iced chai warms up to room temperature.

**(d)** Equilibrium: $T = 72$ (where $\frac{dT}{dt} = 0$). It is **stable** because:
- Above $72°F$: $\frac{dT}{dt} < 0$ → temperature decreases toward 72
- Below $72°F$: $\frac{dT}{dt} > 0$ → temperature increases toward 72

This makes physical sense — Newton's Law of Cooling says objects approach the ambient temperature.

**(e)** The solution starting at $T = 150°F$ satisfies $T > 72$ for all $t$, because:
- $T = 72$ is an equilibrium solution
- By the Uniqueness Theorem, the solution starting at $150°F$ cannot cross the equilibrium at $72°F$
- Since $\frac{dT}{dt} < 0$ for $T > 72$, the temperature decreases but is bounded below by $72°F$

Therefore $T(t) > 72$ for all $t$ — the chai will never cool below room temperature.

</details>

---

## What's Next

Now that you can visualize differential equations through slope fields, you're ready for [Euler's Method](/calculus/eulers-method), where we'll use the slopes to *numerically approximate* solution values step by step — like navigating the Pacific Coast Highway with only a compass and short line-of-sight.

---

<div align="center">

[← Particle Motion with Integrals](/calculus/0705-particle-motion-integrals) | [Euler's Method →](/calculus/eulers-method)

</div>
