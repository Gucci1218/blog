# Optimization
<p class="article-date">May 17, 2025</p>

What's the largest box you can make from a piece of cardboard? What dimensions minimize the cost of a can? What path takes the least time? **Optimization** uses calculus to find the absolute best: the maximum profit, minimum cost, largest area, or shortest distance. These are among the most practical applications of derivatives.

---

## What You'll Learn

- Set up optimization problems from word descriptions
- Find absolute maximum and minimum values on closed intervals
- Use the First and Second Derivative Tests for extrema
- Solve classic optimization problems (box, fence, can, distance)
- Handle constrained optimization with substitution
- Master AP Calculus optimization questions

---

## Prerequisites

- [Basic Derivative Rules](/calculus/0304-basic-derivative-rules)
- [Higher-Order Derivatives](/calculus/0405-higher-order-derivatives) — Second Derivative Test
- Algebra skills for solving equations

---

## The Core Concept

### Finding Extrema

**Absolute (global) maximum:** The largest value of $f$ on its domain
**Absolute (global) minimum:** The smallest value of $f$ on its domain

### The Closed Interval Method

For a continuous function on a closed interval $[a, b]$:

1. Find all critical points (where $f'(x) = 0$ or undefined)
2. Evaluate $f$ at critical points AND endpoints
3. Compare all values — largest is absolute max, smallest is absolute min

### The General Optimization Process

1. **Read and understand** the problem
2. **Draw a diagram** and label variables
3. **Write the objective function** (what you're maximizing/minimizing)
4. **Write constraint equation(s)** (given conditions)
5. **Use constraints to eliminate variables** (get objective in one variable)
6. **Find the domain** of the objective function
7. **Take the derivative and find critical points**
8. **Determine if critical point is max or min** (use endpoints, First/Second Derivative Test)
9. **Answer the question asked** (may need to find other quantities)

---

## Worked Examples

### Example 1: Maximizing Area with Fixed Perimeter

**You have 100 feet of fencing to enclose a rectangular garden. What dimensions maximize the area?**

**Solution:**

**Step 1:** Draw and label.
- Let $x$ = length, $y$ = width
- Perimeter: $2x + 2y = 100$
- Area: $A = xy$ (objective function)

**Step 2:** Use constraint to eliminate a variable.
$$2x + 2y = 100 \Rightarrow y = 50 - x$$

**Step 3:** Substitute into objective.
$$A(x) = x(50 - x) = 50x - x^2$$

**Step 4:** Find domain.
$x > 0$ and $y = 50 - x > 0$, so $0 < x < 50$

**Step 5:** Find critical points.
$$A'(x) = 50 - 2x = 0$$
$$x = 25$$

**Step 6:** Verify maximum.
$$A''(x) = -2 < 0$$

Since $A'' < 0$, this is a maximum. (Or check endpoints: $A(0) = A(50) = 0$)

**Step 7:** Find dimensions.
$x = 25$ ft, $y = 50 - 25 = 25$ ft

**Answer:** A 25 ft × 25 ft square maximizes area at 625 ft².

---

### Example 2: Box with Maximum Volume

**From a 12-inch × 12-inch piece of cardboard, cut equal squares from each corner and fold up to make an open-top box. What size squares maximize volume?**

**Solution:**

**Step 1:** Let $x$ = side length of cut squares.

After folding:
- Base: $(12 - 2x) \times (12 - 2x)$
- Height: $x$

**Step 2:** Objective function.
$$V(x) = x(12 - 2x)^2$$

**Step 3:** Domain.
$x > 0$ and $12 - 2x > 0 \Rightarrow x < 6$

Domain: $0 < x < 6$

**Step 4:** Find critical points.

Expand: $V(x) = x(144 - 48x + 4x^2) = 4x^3 - 48x^2 + 144x$

$$V'(x) = 12x^2 - 96x + 144 = 12(x^2 - 8x + 12) = 12(x - 2)(x - 6)$$

Critical points: $x = 2$ and $x = 6$

Only $x = 2$ is in the domain $(0, 6)$.

**Step 5:** Verify maximum.
- $V(0) = 0$, $V(6) = 0$, $V(2) = 2(8)^2 = 128$

Maximum at $x = 2$.

**Answer:** Cut 2-inch squares from each corner. Maximum volume = 128 cubic inches.

---

### Example 3: Minimizing Distance

**Find the point on the line $y = 2x + 1$ closest to the point $(4, 0)$.**

**Solution:**

**Step 1:** A point on the line is $(x, 2x + 1)$.

**Step 2:** Distance from $(x, 2x + 1)$ to $(4, 0)$:
$$D = \sqrt{(x - 4)^2 + (2x + 1)^2}$$

**Step 3:** Minimize $D^2$ instead (easier, same result):
$$D^2 = (x - 4)^2 + (2x + 1)^2$$
$$= x^2 - 8x + 16 + 4x^2 + 4x + 1$$
$$= 5x^2 - 4x + 17$$

**Step 4:** Find critical point.
$$\frac{d(D^2)}{dx} = 10x - 4 = 0$$
$$x = \frac{2}{5}$$

**Step 5:** Verify minimum.
$$\frac{d^2(D^2)}{dx^2} = 10 > 0$$ ✓

**Step 6:** Find the point.
$$y = 2\left(\frac{2}{5}\right) + 1 = \frac{4}{5} + 1 = \frac{9}{5}$$

**Answer:** The closest point is $\left(\frac{2}{5}, \frac{9}{5}\right)$.

---

### Example 4: Fence Against a Wall

**A farmer has 200 feet of fencing to make a rectangular pen against a barn (no fencing needed on the barn side). What dimensions maximize area?**

**Solution:**

**Step 1:** Let $x$ = side perpendicular to barn (need 2 of these), $y$ = side parallel to barn.

Constraint: $2x + y = 200$

Objective: $A = xy$

**Step 2:** Substitute.
$$y = 200 - 2x$$
$$A(x) = x(200 - 2x) = 200x - 2x^2$$

**Step 3:** Domain: $x > 0$ and $y > 0 \Rightarrow 0 < x < 100$

**Step 4:** Critical point.
$$A'(x) = 200 - 4x = 0$$
$$x = 50$$

**Step 5:** Verify.
$$A''(x) = -4 < 0$$ ✓ Maximum

$y = 200 - 2(50) = 100$

**Answer:** Dimensions: 50 ft × 100 ft. Maximum area = 5000 ft².

---

### Example 5: Minimum Surface Area of a Can

**A cylindrical can must hold 1000 cm³. What dimensions minimize the surface area (and thus material cost)?**

**Solution:**

**Step 1:** Variables: radius $r$, height $h$

Constraint: $V = \pi r^2 h = 1000$

Objective: Surface area $S = 2\pi r^2 + 2\pi rh$ (two circles + side)

**Step 2:** Solve constraint for $h$.
$$h = \frac{1000}{\pi r^2}$$

**Step 3:** Substitute into objective.
$$S(r) = 2\pi r^2 + 2\pi r \cdot \frac{1000}{\pi r^2} = 2\pi r^2 + \frac{2000}{r}$$

**Step 4:** Domain: $r > 0$

**Step 5:** Find critical point.
$$S'(r) = 4\pi r - \frac{2000}{r^2} = 0$$
$$4\pi r = \frac{2000}{r^2}$$
$$4\pi r^3 = 2000$$
$$r^3 = \frac{500}{\pi}$$
$$r = \left(\frac{500}{\pi}\right)^{1/3} \approx 5.42 \text{ cm}$$

**Step 6:** Verify minimum.
$$S''(r) = 4\pi + \frac{4000}{r^3}$$

At $r = \left(\frac{500}{\pi}\right)^{1/3}$: $S'' > 0$ ✓ Minimum

**Step 7:** Find $h$.
$$h = \frac{1000}{\pi r^2} = \frac{1000}{\pi \cdot (500/\pi)^{2/3}} = \frac{1000 \cdot \pi^{2/3}}{\pi \cdot 500^{2/3}}$$

After simplification: $h = 2r$ (the height equals the diameter!)

**Answer:** $r \approx 5.42$ cm, $h \approx 10.84$ cm (or exactly: $h = 2r$)

---

### Example 6: Maximum Product

**Find two positive numbers whose sum is 100 and whose product is maximum.**

**Solution:**

Let the numbers be $x$ and $y$.

Constraint: $x + y = 100$

Objective: $P = xy$

Substitute: $P(x) = x(100 - x) = 100x - x^2$

$P'(x) = 100 - 2x = 0 \Rightarrow x = 50$

$y = 100 - 50 = 50$

**Answer:** Both numbers are 50. Maximum product = 2500.

---

### Example 7: Inscribed Rectangle in Semicircle

**A rectangle is inscribed in a semicircle of radius $R$. Find the dimensions that maximize the area.**

**Solution:**

**Step 1:** Place the semicircle on the x-axis with equation $y = \sqrt{R^2 - x^2}$.

Let the rectangle have width $2x$ and height $y$.

**Step 2:** The top corners touch the semicircle, so $y = \sqrt{R^2 - x^2}$

**Step 3:** Objective.
$$A = 2xy = 2x\sqrt{R^2 - x^2}$$

**Step 4:** Find critical point.
$$A'(x) = 2\sqrt{R^2 - x^2} + 2x \cdot \frac{-x}{\sqrt{R^2 - x^2}}$$
$$= 2\sqrt{R^2 - x^2} - \frac{2x^2}{\sqrt{R^2 - x^2}}$$
$$= \frac{2(R^2 - x^2) - 2x^2}{\sqrt{R^2 - x^2}}$$
$$= \frac{2R^2 - 4x^2}{\sqrt{R^2 - x^2}}$$

Set $A'(x) = 0$:
$$2R^2 - 4x^2 = 0$$
$$x^2 = \frac{R^2}{2}$$
$$x = \frac{R}{\sqrt{2}}$$

**Step 5:** Find dimensions.
$$y = \sqrt{R^2 - \frac{R^2}{2}} = \sqrt{\frac{R^2}{2}} = \frac{R}{\sqrt{2}}$$

Width $= 2x = \sqrt{2}R$

Height $= y = \frac{R}{\sqrt{2}} = \frac{\sqrt{2}R}{2}$

**Answer:** Width $= R\sqrt{2}$, Height $= \frac{R\sqrt{2}}{2}$. Maximum area $= R^2$.

---

### Example 8: Minimum Travel Time

**A person in a boat 3 km offshore wants to reach a point 5 km down the coast. They can row at 4 km/h and walk at 5 km/h. Where should they land to minimize total travel time?**

**Solution:**

**Step 1:** Let $x$ = distance down the coast to landing point.

- Rowing distance: $\sqrt{9 + x^2}$ (Pythagorean theorem)
- Walking distance: $5 - x$

**Step 2:** Time = Distance ÷ Speed

$$T(x) = \frac{\sqrt{9 + x^2}}{4} + \frac{5 - x}{5}$$

**Step 3:** Domain: $0 \leq x \leq 5$

**Step 4:** Find critical point.
$$T'(x) = \frac{x}{4\sqrt{9 + x^2}} - \frac{1}{5} = 0$$

$$\frac{x}{4\sqrt{9 + x^2}} = \frac{1}{5}$$

$$5x = 4\sqrt{9 + x^2}$$

$$25x^2 = 16(9 + x^2)$$

$$25x^2 = 144 + 16x^2$$

$$9x^2 = 144$$

$$x = 4$$ km

**Step 5:** Compare values.
- $T(0) = \frac{3}{4} + 1 = 1.75$ hours
- $T(4) = \frac{5}{4} + \frac{1}{5} = 1.45$ hours
- $T(5) = \frac{\sqrt{34}}{4} \approx 1.46$ hours

Minimum at $x = 4$.

**Answer:** Land 4 km down the coast. Minimum time ≈ 1.45 hours.

---

## Common Problem Types

### Type 1: Perimeter/Fencing Problems
- Fixed perimeter, maximize area
- Key insight: Square is optimal for rectangles

### Type 2: Box Problems
- Cut corners from cardboard, fold to make box
- Volume = length × width × height

### Type 3: Surface Area/Volume Problems
- Fixed volume, minimize surface area (or vice versa)
- Often involves cylinders, cans, boxes

### Type 4: Distance Problems
- Minimize distance from point to curve
- Easier to minimize $D^2$ instead of $D$

### Type 5: Cost/Revenue/Profit Problems
- Profit = Revenue − Cost
- Maximize profit: set marginal profit = 0

### Type 6: Inscribed Shapes
- Rectangle in circle/semicircle
- Use the equation of the curve as constraint

---

## Key Strategies

### Strategy 1: Minimize $D^2$ Instead of $D$

When minimizing distance $D = \sqrt{...}$, minimize $D^2$ instead. Same location, easier derivative!

### Strategy 2: Use Symmetry

For symmetric problems (like rectangle with fixed perimeter), the optimal solution is often symmetric (a square).

### Strategy 3: Check Endpoints

On a closed interval, extrema can occur at:
- Critical points (where $f' = 0$ or undefined)
- Endpoints

### Strategy 4: Use Second Derivative Test

If $f'(c) = 0$:
- $f''(c) > 0$ → local minimum
- $f''(c) < 0$ → local maximum

### Strategy 5: Physical Reasoning

If the problem has only one critical point and the quantity must have a max/min by physical reasoning, that critical point is the answer.

---

## Common Mistakes to Avoid

### Mistake 1: Forgetting Constraints

Don't just differentiate the objective — use constraints to reduce to one variable first.

### Mistake 2: Wrong Domain

Make sure all variables stay positive (for physical quantities) and constraints are satisfied.

### Mistake 3: Finding Critical Point but Not Verifying

Always verify your critical point is actually a max or min (Second Derivative Test, endpoint comparison, or physical reasoning).

### Mistake 4: Not Answering the Question

If asked for dimensions, give both. If asked for maximum value, plug critical point back into original function.

### Mistake 5: Algebra Errors

These problems involve lots of algebra. Check your work, especially when substituting constraints.

---

## AP Exam Tips

### Setup Is Crucial

- Draw a clear diagram
- Define all variables
- Write the objective function AND constraint
- Show the substitution step

### Show All Work

On free response:
1. State the objective function
2. Show constraint and substitution
3. Take derivative and set = 0
4. Verify max/min
5. State final answer with units

### Common Question Types

1. **Closed interval:** Use Closed Interval Method
2. **Open interval with one critical point:** Use Second Derivative Test
3. **Word problems:** Follow the 9-step process

### Time-Saving Tips

1. Recognize common setups (fence, box, can)
2. Remember: square often optimal for rectangles
3. For distance problems, minimize $D^2$

---

## Practice Problems

### Basic (Problems 1-5)

**1.** Find two positive numbers with sum 50 and maximum product.

---

**2.** A rectangle has perimeter 40. Find dimensions that maximize area.

---

**3.** Find the minimum value of $f(x) = x^2 + \frac{4}{x}$ for $x > 0$.

---

**4.** A farmer has 120 ft of fencing to make a rectangular pen against a barn. Find dimensions for maximum area.

---

**5.** Find the point on $y = x^2$ closest to $(0, 3)$.

---

### Intermediate (Problems 6-10)

**6.** An open-top box is made from a 20 × 30 inch cardboard by cutting equal squares from corners. Find the maximum volume.

---

**7.** A rectangular field is divided into two pens by a fence parallel to one side. Total fencing is 300 m. Maximize total area.

---

**8.** A can with no top must hold 500 cm³. Minimize surface area.

---

**9.** Find the dimensions of the largest rectangle inscribed in a circle of radius 5.

---

**10.** Find the minimum distance from the point $(3, 0)$ to the parabola $y = x^2$.

---

### Advanced (Problems 11-15)

**11.** A window has a rectangle topped by a semicircle. The perimeter is 12 ft. Find dimensions for maximum light (area).

---

**12.** A box with square base and open top must have volume 32,000 cm³. Minimize surface area.

---

**13.** A poster has 50 cm² of printed area. Margins are 4 cm on sides and 6 cm on top/bottom. Find dimensions minimizing total poster area.

---

**14.** A wire 100 cm long is cut into two pieces. One forms a square, the other a circle. How should it be cut to maximize total area?

---

**15.** An isosceles triangle is inscribed in a circle of radius $R$ with one vertex at the top. Find the dimensions of the triangle with maximum area.

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

A rectangle has perimeter 100. The maximum area is:

| Choice | Answer |
|--------|--------|
| **(A)** | 400 |
| **(B)** | 500 |
| **(C)** | 625 |
| **(D)** | 2500 |

---

#### Problem 17 (Multiple Choice)

An open box with square base and volume 4000 cm³ has minimum surface area when the side of the base is:

| Choice | Answer |
|--------|--------|
| **(A)** | 10 cm |
| **(B)** | 20 cm |
| **(C)** | $\sqrt[3]{8000}$ cm |
| **(D)** | $\sqrt{4000}$ cm |

---

#### Problem 18 (Free Response)

A farmer wants to fence a rectangular area of 1800 square meters. One side borders a river (no fence needed). Fencing costs \$10 per meter for the sides perpendicular to the river and \$5 per meter for the side parallel to the river.

> **(a)** Express the total cost $C$ as a function of $x$, the length of a side perpendicular to the river.
>
> **(b)** Find the dimensions that minimize cost.
>
> **(c)** What is the minimum cost?

---

#### Problem 19 (Multiple Choice)

The point on the curve $y = \sqrt{x}$ closest to $(4, 0)$ is:

| Choice | Answer |
|--------|--------|
| **(A)** | $(0, 0)$ |
| **(B)** | $(1, 1)$ |
| **(C)** | $\left(\frac{7}{2}, \sqrt{\frac{7}{2}}\right)$ |
| **(D)** | $(4, 2)$ |

---

#### Problem 20 (Free Response - Challenging)

A rectangular page contains 96 cm² of print. The margins are 2 cm on each side and 3 cm on top and bottom.

> **(a)** Express the total area $A$ of the page as a function of the width $x$ of the printed area.
>
> **(b)** Find the dimensions of the printed area that minimize the total page area.
>
> **(c)** Find the dimensions of the entire page.

---

## Solutions

<details>
<summary><strong>Solution 1</strong></summary>

Let numbers be $x$ and $50 - x$.

$P = x(50 - x) = 50x - x^2$

$P' = 50 - 2x = 0 \Rightarrow x = 25$

**Answer:** Both numbers are 25. Maximum product = 625.

</details>

---

<details>
<summary><strong>Solution 2</strong></summary>

$2x + 2y = 40 \Rightarrow y = 20 - x$

$A = x(20 - x) = 20x - x^2$

$A' = 20 - 2x = 0 \Rightarrow x = 10$

**Answer:** 10 × 10 square. Maximum area = 100.

</details>

---

<details>
<summary><strong>Solution 3</strong></summary>

$f(x) = x^2 + 4x^{-1}$

$f'(x) = 2x - 4x^{-2} = 2x - \frac{4}{x^2} = 0$

$2x = \frac{4}{x^2}$

$x^3 = 2$

$x = \sqrt[3]{2}$

$f(\sqrt[3]{2}) = (\sqrt[3]{2})^2 + \frac{4}{\sqrt[3]{2}} = 2^{2/3} + 4 \cdot 2^{-1/3} = 2^{2/3} + 2^2 \cdot 2^{-1/3} = 2^{2/3} + 2^{5/3} = 3 \cdot 2^{2/3}$

**Answer:** Minimum value is $3\sqrt[3]{4} \approx 4.76$

</details>

---

<details>
<summary><strong>Solution 4</strong></summary>

$2x + y = 120 \Rightarrow y = 120 - 2x$

$A = xy = x(120 - 2x) = 120x - 2x^2$

$A' = 120 - 4x = 0 \Rightarrow x = 30$

$y = 60$

**Answer:** 30 ft × 60 ft. Maximum area = 1800 ft².

</details>

---

<details>
<summary><strong>Solution 5</strong></summary>

Point on parabola: $(x, x^2)$

$D^2 = x^2 + (x^2 - 3)^2 = x^2 + x^4 - 6x^2 + 9 = x^4 - 5x^2 + 9$

$\frac{d(D^2)}{dx} = 4x^3 - 10x = 2x(2x^2 - 5) = 0$

$x = 0$ or $x = \pm\sqrt{5/2}$

Compare: At $x = 0$: $D^2 = 9$. At $x = \sqrt{5/2}$: $D^2 = 6.25 - 12.5 + 9 = 2.75$

Minimum at $x = \pm\sqrt{5/2}$

**Answer:** $\left(\sqrt{\frac{5}{2}}, \frac{5}{2}\right)$ or $\left(-\sqrt{\frac{5}{2}}, \frac{5}{2}\right)$

</details>

---

<details>
<summary><strong>Solution 6</strong></summary>

Cut squares of side $x$.

$V = x(20 - 2x)(30 - 2x) = x(4x^2 - 100x + 600) = 4x^3 - 100x^2 + 600x$

$V' = 12x^2 - 200x + 600 = 4(3x^2 - 50x + 150) = 0$

$x = \frac{50 \pm \sqrt{2500 - 1800}}{6} = \frac{50 \\pm \sqrt{700}}{6}$

$x \approx \frac{50 - 26.46}{6} \approx 3.92$ (in domain)

$V(3.92) \approx 1056$ in³

**Answer:** Cut ≈ 3.92 inch squares. Maximum volume ≈ 1056 in³.

</details>

---

<details>
<summary><strong>Solution 7</strong></summary>

Let $x$ = length of divided sides (need 3), $y$ = width.

$3x + 2y = 300$

$A = xy = x \cdot \frac{300 - 3x}{2} = \frac{300x - 3x^2}{2}$

$A' = \frac{300 - 6x}{2} = 0 \Rightarrow x = 50$

$y = \frac{300 - 150}{2} = 75$

**Answer:** 50 m × 75 m. Maximum area = 3750 m².

</details>

---

<details>
<summary><strong>Solution 8</strong></summary>

$V = \pi r^2 h = 500$

$S = \pi r^2 + 2\pi rh = \pi r^2 + 2\pi r \cdot \frac{500}{\pi r^2} = \pi r^2 + \frac{1000}{r}$

$S' = 2\pi r - \frac{1000}{r^2} = 0$

$r^3 = \frac{500}{\pi}$

$r = \left(\frac{500}{\pi}\right)^{1/3} \approx 5.42$ cm

$h = \frac{500}{\pi r^2} = r$ (height equals radius)

**Answer:** $r \approx 5.42$ cm, $h \approx 5.42$ cm.

</details>

---

<details>
<summary><strong>Solution 9</strong></summary>

Rectangle with corners at $(\pm x, \pm y)$ inscribed in $x^2 + y^2 = 25$

$A = 4xy$ where $y = \sqrt{25 - x^2}$

$A = 4x\sqrt{25 - x^2}$

$A' = 4\sqrt{25 - x^2} + 4x \cdot \frac{-x}{\sqrt{25 - x^2}} = \frac{4(25 - 2x^2)}{\sqrt{25 - x^2}} = 0$

$x = \frac{5}{\sqrt{2}}$, $y = \frac{5}{\sqrt{2}}$

Dimensions: $2x = 5\sqrt{2}$, $2y = 5\sqrt{2}$

**Answer:** $5\sqrt{2} \times 5\sqrt{2}$ (a square). Area = 50.

</details>

---

<details>
<summary><strong>Solution 10</strong></summary>

$D^2 = (x - 3)^2 + x^4$

$\frac{d(D^2)}{dx} = 2(x - 3) + 4x^3 = 0$

$2x^3 + x - 3 = 0$

By inspection or numerical methods: $x = 1$

$D = \sqrt{(1-3)^2 + 1} = \sqrt{5}$

**Answer:** Minimum distance = $\sqrt{5}$

</details>

---

<details>
<summary><strong>Solution 11</strong></summary>

Let $x$ = width (diameter of semicircle), $y$ = height of rectangle.

Perimeter: $2y + x + \frac{\pi x}{2} = 12$

$y = \frac{12 - x - \frac{\pi x}{2}}{2} = 6 - \frac{x}{2} - \frac{\pi x}{4}$

Area: $A = xy + \frac{\pi(x/2)^2}{2} = xy + \frac{\pi x^2}{8}$

Substitute and differentiate... Maximum at $x = \frac{24}{4 + \pi}$

**Answer:** Width $= \frac{24}{4 + \pi}$ ft, Height $= \frac{12}{4 + \pi}$ ft

</details>

---

<details>
<summary><strong>Solution 12</strong></summary>

$V = x^2 h = 32000$

$S = x^2 + 4xh = x^2 + \frac{128000}{x}$

$S' = 2x - \frac{128000}{x^2} = 0$

$x^3 = 64000 \Rightarrow x = 40$ cm

$h = \frac{32000}{1600} = 20$ cm

**Answer:** Base 40 cm × 40 cm, height 20 cm.

</details>

---

<details>
<summary><strong>Solution 13</strong></summary>

Let printed area be $x \times y = 50$

Total: $(x + 8)(y + 12) = (x + 8)\left(\frac{50}{x} + 12\right)$

$A = 50 + 12x + \frac{400}{x} + 96$

$A' = 12 - \frac{400}{x^2} = 0 \Rightarrow x = \frac{20}{\sqrt{3}}$

$y = \frac{50\sqrt{3}}{20} = \frac{5\sqrt{3}}{2}$

**Answer:** Printed area: $\frac{20}{\sqrt{3}} \times \frac{5\sqrt{3}}{2}$ cm

</details>

---

<details>
<summary><strong>Solution 14</strong></summary>

Let $x$ = perimeter of square.

Square: side $= x/4$, area $= x^2/16$

Circle: circumference $= 100 - x$, radius $= \frac{100-x}{2\pi}$, area $= \frac{(100-x)^2}{4\pi}$

Total area: $A = \frac{x^2}{16} + \frac{(100-x)^2}{4\pi}$

For maximum, check critical point and endpoints.

$A' = \frac{x}{8} - \frac{100-x}{2\pi} = 0$

$x = \frac{400}{4 + \pi}$

Compare with endpoints $x = 0$ (all circle) and $x = 100$ (all square).

**Answer:** Maximum when all in circle (no square): $x = 0$, all 100 cm for circle.

</details>

---

<details>
<summary><strong>Solution 15</strong></summary>

Place circle center at origin. Top vertex at $(0, R)$.

Base vertices at $(\pm x, y)$ where $x^2 + y^2 = R^2$.

Base $= 2x$, height $= R - y$

$A = \frac{1}{2}(2x)(R - y) = x(R - y)$

Using $x = \sqrt{R^2 - y^2}$:

$A = (R - y)\sqrt{R^2 - y^2}$

Take derivative, set to 0... Maximum when $y = -R/2$

Base $= 2\sqrt{R^2 - R^2/4} = R\sqrt{3}$

Height $= R - (-R/2) = 3R/2$

**Answer:** Base $= R\sqrt{3}$, height $= \frac{3R}{2}$. Area $= \frac{3\sqrt{3}R^2}{4}$

</details>

---

<details>
<summary><strong>Solution 16</strong></summary>

$2x + 2y = 100$, $y = 50 - x$

$A = x(50 - x)$, max at $x = 25$

$A = 25 \times 25 = 625$

**Answer:** **(C)** 625

</details>

---

<details>
<summary><strong>Solution 17</strong></summary>

$V = x^2 h = 4000$

$S = x^2 + 4xh = x^2 + \frac{16000}{x}$

$S' = 2x - \frac{16000}{x^2} = 0$

$x^3 = 8000$

$x = 20$ cm

**Answer:** **(B)** 20 cm

</details>

---

<details>
<summary><strong>Solution 18</strong></summary>

**(a)** Let $x$ = perpendicular side, $y$ = parallel side

Constraint: $xy = 1800 \Rightarrow y = \frac{1800}{x}$

Cost: $C = 10(2x) + 5y = 20x + \frac{9000}{x}$

**(b)** $C' = 20 - \frac{9000}{x^2} = 0$

$x^2 = 450$, $x = \sqrt{450} = 15\sqrt{2}$ m

$y = \frac{1800}{15\sqrt{2}} = 60\sqrt{2}$ m

**(c)** $C = 20(15\sqrt{2}) + 5(60\sqrt{2}) = 300\sqrt{2} + 300\sqrt{2} = 600\sqrt{2} \approx \$848.53$

</details>

---

<details>
<summary><strong>Solution 19</strong></summary>

Point on curve: $(x, \sqrt{x})$

$D^2 = (x - 4)^2 + x$

$\frac{d(D^2)}{dx} = 2(x - 4) + 1 = 2x - 7 = 0$

$x = 3.5$

**Answer:** **(C)** $\left(\frac{7}{2}, \sqrt{\frac{7}{2}}\right)$

</details>

---

<details>
<summary><strong>Solution 20</strong></summary>

**(a)** Print area: $xy = 96$

Total page: $(x + 4)(y + 6) = (x + 4)\left(\frac{96}{x} + 6\right)$

$A = 96 + 6x + \frac{384}{x} + 24 = 120 + 6x + \frac{384}{x}$

**(b)** $A' = 6 - \frac{384}{x^2} = 0$

$x^2 = 64$, $x = 8$ cm

$y = 12$ cm

**(c)** Page: $(8 + 4) \times (12 + 6) = 12 \times 18$ cm

</details>

---

## What's Next

With optimization mastered, you're ready for [Mean Value Theorem](/calculus/0504-mean-value-theorem), one of the most important theoretical results in calculus that connects average rate of change to instantaneous rate of change.

---

<div align="center">

[← Related Rates](/calculus/0502-related-rates) | [Mean Value Theorem →](/calculus/0504-mean-value-theorem)

</div>
