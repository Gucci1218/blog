# Definite Integrals
<p class="article-date">July 5, 2025</p>

*The definite integral takes us from approximation to exactness. By taking the limit of Riemann sums as the number of rectangles approaches infinity, we get the precise area under a curve. This seemingly simple concept unlocks solutions to problems in physics, engineering, economics, and beyond.*

---

## What You'll Learn
- Understand the definite integral as a limit of Riemann sums
- Use proper integral notation and interpret its meaning
- Apply properties of definite integrals
- Evaluate integrals using geometry
- Understand signed area and its implications

---

## Prerequisites
- [Riemann Sums](/calculus/0602-riemann-sums)
- [Understanding Limits](/calculus/0204-understanding-limits)

---

## The Core Concept

### From Riemann Sums to Definite Integrals

Recall that a Riemann sum approximates the area under a curve using rectangles:

$$\sum_{i=1}^{n} f(x_i^*) \Delta x$$

As $n \to \infty$ and $\Delta x \to 0$, this approximation becomes exact:

$$\lim_{n \to \infty} \sum_{i=1}^{n} f(x_i^*) \Delta x$$

This limit is the **definite integral**.

### The Definition

If $f$ is continuous on $[a, b]$, the **definite integral of $f$ from $a$ to $b$** is:

$$\int_a^b f(x) \, dx = \lim_{n \to \infty} \sum_{i=1}^{n} f(x_i^*) \Delta x$$

where $\Delta x = \frac{b-a}{n}$ and $x_i^*$ is any point in the $i$-th subinterval.

### Notation and Terminology

$$\int_a^b f(x) \, dx$$

| Component | Name | Meaning |
|-----------|------|---------|
| $\int$ | Integral sign | Indicates integration |
| $a$ | Lower limit | Starting point |
| $b$ | Upper limit | Ending point |
| $f(x)$ | Integrand | Function being integrated |
| $dx$ | Differential | Variable of integration |

The definite integral is a **number**, not a function (unlike the indefinite integral).

### Geometric Interpretation: Signed Area

The definite integral $\int_a^b f(x) \, dx$ represents the **signed area** between the curve $y = f(x)$ and the x-axis from $x = a$ to $x = b$:

- Area **above** the x-axis counts as **positive**
- Area **below** the x-axis counts as **negative**

**Example**: If the region above the axis has area 5 and the region below has area 3:
$$\int_a^b f(x) \, dx = 5 - 3 = 2$$

### When Does the Integral Exist?

**Theorem**: If $f$ is continuous on $[a, b]$, then $\int_a^b f(x) \, dx$ exists.

The integral also exists for many discontinuous functions, but continuity guarantees existence.

### Properties of Definite Integrals

**1. Constant Multiple**:
$$\int_a^b c \cdot f(x) \, dx = c \int_a^b f(x) \, dx$$

**2. Sum/Difference**:
$$\int_a^b [f(x) \pm g(x)] \, dx = \int_a^b f(x) \, dx \pm \int_a^b g(x) \, dx$$

**3. Additivity (Splitting)**:
$$\int_a^b f(x) \, dx + \int_b^c f(x) \, dx = \int_a^c f(x) \, dx$$

**4. Reversing Limits**:
$$\int_a^b f(x) \, dx = -\int_b^a f(x) \, dx$$

**5. Zero Width**:
$$\int_a^a f(x) \, dx = 0$$

**6. Comparison**: If $f(x) \geq g(x)$ on $[a, b]$, then:
$$\int_a^b f(x) \, dx \geq \int_a^b g(x) \, dx$$

**7. Bounds**: If $m \leq f(x) \leq M$ on $[a, b]$, then:
$$m(b-a) \leq \int_a^b f(x) \, dx \leq M(b-a)$$

### Evaluating Integrals Using Geometry

Some integrals can be computed without calculus by recognizing geometric shapes:

| Shape | Area Formula |
|-------|--------------|
| Rectangle | $\text{base} \times \text{height}$ |
| Triangle | $\frac{1}{2} \times \text{base} \times \text{height}$ |
| Trapezoid | $\frac{1}{2}(b_1 + b_2) \times h$ |
| Semicircle | $\frac{1}{2}\pi r^2$ |

### Worked Examples

**Example 1**: Evaluate $\int_0^4 3 \, dx$ using geometry.

**Solution**:

The integrand $f(x) = 3$ is a horizontal line at height 3.

The region is a rectangle with:
- Base = $4 - 0 = 4$
- Height = $3$

$$\int_0^4 3 \, dx = 4 \times 3 = 12$$

---

**Example 2**: Evaluate $\int_0^3 x \, dx$ using geometry.

**Solution**:

The integrand $f(x) = x$ is a line through the origin.

The region is a right triangle with:
- Base = $3$
- Height = $3$

$$\int_0^3 x \, dx = \frac{1}{2} \times 3 \times 3 = \frac{9}{2}$$

---

**Example 3**: Evaluate $\int_{-2}^2 \sqrt{4 - x^2} \, dx$ using geometry.

**Solution**:

The equation $y = \sqrt{4 - x^2}$ represents the upper half of the circle $x^2 + y^2 = 4$.

This is a semicircle with radius $r = 2$.

$$\int_{-2}^2 \sqrt{4 - x^2} \, dx = \frac{1}{2} \pi (2)^2 = 2\pi$$

---

**Example 4**: Evaluate $\int_0^4 |x - 2| \, dx$ using geometry.

**Solution**:

The function $|x - 2|$ creates a V-shape with vertex at $(2, 0)$.

From $x = 0$ to $x = 2$: A triangle with base 2, height 2
From $x = 2$ to $x = 4$: A triangle with base 2, height 2

$$\int_0^4 |x - 2| \, dx = \frac{1}{2}(2)(2) + \frac{1}{2}(2)(2) = 2 + 2 = 4$$

---

**Example 5**: Given $\int_0^5 f(x) \, dx = 8$ and $\int_0^3 f(x) \, dx = 3$, find $\int_3^5 f(x) \, dx$.

**Solution**:

Using the additivity property:

$$\int_0^3 f(x) \, dx + \int_3^5 f(x) \, dx = \int_0^5 f(x) \, dx$$

$$3 + \int_3^5 f(x) \, dx = 8$$

$$\int_3^5 f(x) \, dx = 5$$

---

**Example 6**: The graph of $f$ consists of two line segments as shown. If the region above the x-axis has area 6 and the region below has area 2, find $\int_0^4 f(x) \, dx$.

**Solution**:

The definite integral equals the signed area:

$$\int_0^4 f(x) \, dx = (\text{area above}) - (\text{area below}) = 6 - 2 = 4$$

---

### Net Change Interpretation

The definite integral $\int_a^b f(x) \, dx$ can be interpreted as the **net change** when $f$ represents a rate of change:

$$\int_a^b f'(x) \, dx = f(b) - f(a)$$

**Examples**:
- If $v(t)$ = velocity, then $\int_a^b v(t) \, dt$ = net displacement
- If $r(t)$ = rate of water flow, then $\int_a^b r(t) \, dt$ = net change in water volume

---

## Key Formulas & Rules

| Property | Formula |
|----------|---------|
| Definition | $\int_a^b f(x) \, dx = \lim_{n \to \infty} \sum_{i=1}^{n} f(x_i^*) \Delta x$ |
| Zero width | $\int_a^a f(x) \, dx = 0$ |
| Reverse limits | $\int_a^b f(x) \, dx = -\int_b^a f(x) \, dx$ |
| Constant multiple | $\int_a^b cf(x) \, dx = c\int_a^b f(x) \, dx$ |
| Sum | $\int_a^b [f(x) + g(x)] \, dx = \int_a^b f(x) \, dx + \int_a^b g(x) \, dx$ |
| Additivity | $\int_a^c f(x) \, dx = \int_a^b f(x) \, dx + \int_b^c f(x) \, dx$ |

---

## Common Mistakes to Avoid

1. **Forgetting signed area**: The integral can be negative if the function is below the x-axis.

2. **Confusing definite and indefinite integrals**: Definite integrals give numbers; indefinite integrals give functions.

3. **Wrong direction with reversed limits**: Remember $\int_a^b = -\int_b^a$.

4. **Ignoring the "+C"**: Definite integrals don't need +C (it cancels out in evaluation).

5. **Total distance vs. displacement**: $\int v(t) \, dt$ gives displacement, not total distance. For total distance, use $\int |v(t)| \, dt$.

6. **Area vs. integral**: Area is always positive; integrals can be negative.

---

## AP Exam Tips

### For Both AB and BC:
- Know properties of definite integrals cold—they're tested constantly
- Practice using geometry to evaluate simple integrals
- Understand the difference between signed area and total area
- Be able to interpret integrals in context (physics, rates)

### Common Question Types:
1. **Property application**: Use properties to find unknown integrals
2. **Geometric evaluation**: Calculate integrals from graphs
3. **Signed area interpretation**: Determine when integral is positive/negative
4. **Net change problems**: Interpret integrals as accumulated change

### Calculator Tips:
- Use `fnInt` or numerical integration to verify answers
- Graph the function to visualize signed areas

---

## Practice Problems

### Basic (Problems 1-5)

**1.** Evaluate using geometry:

$$\int_0^5 4 \, dx$$

---

**2.** Evaluate using geometry:

$$\int_0^6 \frac{x}{2} \, dx$$

---

**3.** Given:

$$\int_1^4 f(x) \, dx = 7$$

Find $\int_4^1 f(x) \, dx$.

---

**4.** Given:

$$\int_0^3 f(x) \, dx = 5 \quad \text{and} \quad \int_0^3 g(x) \, dx = 2$$

Find $\int_0^3 [2f(x) - 3g(x)] \, dx$.

---

**5.** Evaluate using geometry:

$$\int_{-3}^3 \sqrt{9 - x^2} \, dx$$

---

### Intermediate (Problems 6-10)

**6.** Given:

$$\int_0^6 f(x) \, dx = 10, \quad \int_0^4 f(x) \, dx = 3$$

Find $\int_4^6 f(x) \, dx$.

---

**7.** The graph of $f$ on $[0, 8]$ consists of two triangular regions. Triangle A (above x-axis) has vertices at $(0,0)$, $(4,0)$, $(2,3)$. Triangle B (below x-axis) has vertices at $(4,0)$, $(8,0)$, $(6,-2)$.

Find $\int_0^8 f(x) \, dx$.

---

**8.** Evaluate using geometry:

$$\int_{-2}^4 (2 - |x|) \, dx$$

---

**9.** If $\int_0^{10} f(x) \, dx = 12$ and $\int_5^{10} f(x) \, dx = 4$, find $\int_0^5 f(x) \, dx$.

---

**10.** A particle moves along a line with velocity $v(t)$ m/s. If $\int_0^5 v(t) \, dt = 8$:

**(a)** What is the displacement from $t = 0$ to $t = 5$?

**(b)** If the particle starts at position $s = 3$, what is its position at $t = 5$?

---

### Advanced (Problems 11-15)

**11.** Given:

$$\int_a^b f(x) \, dx = 5, \quad \int_a^b g(x) \, dx = -2, \quad \int_a^b h(x) \, dx = 3$$

Evaluate $\int_a^b [4f(x) - 2g(x) + h(x)] \, dx$.

---

**12.** If $f$ is an even function and $\int_{-3}^3 f(x) \, dx = 12$, find $\int_0^3 f(x) \, dx$.

---

**13.** If $f$ is an odd function and $\int_0^4 f(x) \, dx = 7$, find $\int_{-4}^4 f(x) \, dx$.

---

**14.** The graph of $f'$ is shown consisting of semicircular arcs. If $f(0) = 2$:

**(a)** Find $\int_0^2 f'(x) \, dx$ if the semicircle above the x-axis from $x = 0$ to $x = 2$ has radius 1.

**(b)** Find $f(2)$.

---

**15.** Prove that if $f$ is continuous and $f(x) \geq 0$ on $[a, b]$, then $\int_a^b f(x) \, dx \geq 0$.

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

If $\int_1^5 f(x) \, dx = 6$ and $\int_3^5 f(x) \, dx = 2$, then $\int_1^3 f(x) \, dx =$

| Choice | Answer |
|--------|--------|
| **(A)** | $-4$ |
| **(B)** | $3$ |
| **(C)** | $4$ |
| **(D)** | $8$ |

---

#### Problem 17 (Multiple Choice)

The graph of $f$ consists of a semicircle and two line segments as shown. The semicircle has radius 2, centered at the origin, below the x-axis. If the total area of the triangular regions above the x-axis is 6, what is $\int_{-4}^4 f(x) \, dx$?

| Choice | Answer |
|--------|--------|
| **(A)** | $6 - 2\pi$ |
| **(B)** | $6 + 2\pi$ |
| **(C)** | $2\pi - 6$ |
| **(D)** | $-6 - 2\pi$ |

---

#### Problem 18 (Free Response)

Let $f$ and $g$ be continuous functions with the following properties:
- $\int_0^4 f(x) \, dx = 8$
- $\int_0^4 g(x) \, dx = 5$
- $\int_2^4 f(x) \, dx = 3$

> **(a)** Find $\int_0^4 [3f(x) - 2g(x)] \, dx$.
>
> **(b)** Find $\int_0^2 f(x) \, dx$.
>
> **(c)** If $\int_2^4 g(x) \, dx = 1$, find $\int_0^2 [f(x) + g(x)] \, dx$.

---

#### Problem 19 (Multiple Choice)

Water flows into a tank at a rate of $r(t)$ gallons per minute. Which of the following expressions represents the total amount of water that flows into the tank during the first 10 minutes?

| Choice | Answer |
|--------|--------|
| **(A)** | $r(10) - r(0)$ |
| **(B)** | $r'(10)$ |
| **(C)** | $\int_0^{10} r(t) \, dt$ |
| **(D)** | $\int_0^{10} r'(t) \, dt$ |

---

#### Problem 20 (Free Response - Challenging)

The velocity of a particle moving along the x-axis is given by $v(t) = t^2 - 4t + 3$ for $0 \leq t \leq 5$.

> **(a)** Find the total displacement of the particle from $t = 0$ to $t = 5$.
>
> **(b)** Find the times when the particle changes direction.
>
> **(c)** Set up, but do not evaluate, an integral expression for the total distance traveled from $t = 0$ to $t = 5$.
>
> **(d)** Is the total distance greater than, less than, or equal to the displacement? Explain.

---

## Answer Key

<details>
<summary><strong>Problem 1 Solution</strong></summary>

**Answer**: $20$

**Step-by-step solution**:

The function $f(x) = 4$ is a horizontal line.

The region is a rectangle:
- Base = $5 - 0 = 5$
- Height = $4$

$$\int_0^5 4 \, dx = 5 \times 4 = 20$$

</details>

---

<details>
<summary><strong>Problem 2 Solution</strong></summary>

**Answer**: $9$

**Step-by-step solution**:

The function $f(x) = \frac{x}{2}$ is a line through the origin with slope $\frac{1}{2}$.

At $x = 6$: $f(6) = 3$

The region is a right triangle:
- Base = $6$
- Height = $3$

$$\int_0^6 \frac{x}{2} \, dx = \frac{1}{2} \times 6 \times 3 = 9$$

</details>

---

<details>
<summary><strong>Problem 3 Solution</strong></summary>

**Answer**: $-7$

**Step-by-step solution**:

Using the property $\int_a^b f(x) \, dx = -\int_b^a f(x) \, dx$:

$$\int_4^1 f(x) \, dx = -\int_1^4 f(x) \, dx = -7$$

</details>

---

<details>
<summary><strong>Problem 4 Solution</strong></summary>

**Answer**: $4$

**Step-by-step solution**:

Using linearity properties:

$$\int_0^3 [2f(x) - 3g(x)] \, dx = 2\int_0^3 f(x) \, dx - 3\int_0^3 g(x) \, dx$$

$$= 2(5) - 3(2) = 10 - 6 = 4$$

</details>

---

<details>
<summary><strong>Problem 5 Solution</strong></summary>

**Answer**: $\frac{9\pi}{2}$

**Step-by-step solution**:

The function $y = \sqrt{9 - x^2}$ represents the upper half of the circle $x^2 + y^2 = 9$.

This is a semicircle with radius $r = 3$.

$$\int_{-3}^3 \sqrt{9 - x^2} \, dx = \frac{1}{2}\pi(3)^2 = \frac{9\pi}{2}$$

</details>

---

<details>
<summary><strong>Problem 6 Solution</strong></summary>

**Answer**: $7$

**Step-by-step solution**:

Using the additivity property:

$$\int_0^4 f(x) \, dx + \int_4^6 f(x) \, dx = \int_0^6 f(x) \, dx$$

$$3 + \int_4^6 f(x) \, dx = 10$$

$$\int_4^6 f(x) \, dx = 7$$

</details>

---

<details>
<summary><strong>Problem 7 Solution</strong></summary>

**Answer**: $2$

**Step-by-step solution**:

**Triangle A** (above x-axis):
- Base = $4$ (from $x = 0$ to $x = 4$)
- Height = $3$
- Area = $\frac{1}{2}(4)(3) = 6$

**Triangle B** (below x-axis):
- Base = $4$ (from $x = 4$ to $x = 8$)
- Height = $2$
- Area = $\frac{1}{2}(4)(2) = 4$

Signed area:
$$\int_0^8 f(x) \, dx = 6 - 4 = 2$$

</details>

---

<details>
<summary><strong>Problem 8 Solution</strong></summary>

**Answer**: $2$

**Step-by-step solution**:

The function $f(x) = 2 - |x|$ creates an inverted V-shape with vertex at $(0, 2)$.

x-intercepts: $2 - |x| = 0 \Rightarrow x = \pm 2$

From $x = -2$ to $x = 2$: Triangle above x-axis
- Base = $4$, Height = $2$
- Area = $\frac{1}{2}(4)(2) = 4$

From $x = -2$ to $x = -2$: Nothing extra on left side (already covered)

From $x = 2$ to $x = 4$: Triangle below x-axis
- At $x = 4$: $f(4) = 2 - 4 = -2$
- Base = $2$, Height = $2$
- Area below = $\frac{1}{2}(2)(2) = 2$

$$\int_{-2}^4 (2 - |x|) \, dx = 4 - 2 = 2$$

</details>

---

<details>
<summary><strong>Problem 9 Solution</strong></summary>

**Answer**: $8$

**Step-by-step solution**:

Using additivity:

$$\int_0^5 f(x) \, dx + \int_5^{10} f(x) \, dx = \int_0^{10} f(x) \, dx$$

$$\int_0^5 f(x) \, dx + 4 = 12$$

$$\int_0^5 f(x) \, dx = 8$$

</details>

---

<details>
<summary><strong>Problem 10 Solution</strong></summary>

**Answer**: (a) 8 meters, (b) 11 meters

**Step-by-step solution**:

**(a)** Displacement = $\int_0^5 v(t) \, dt = 8$ meters

**(b)** Position at $t = 5$:
$$s(5) = s(0) + \text{displacement} = 3 + 8 = 11 \text{ meters}$$

</details>

---

<details>
<summary><strong>Problem 11 Solution</strong></summary>

**Answer**: $27$

**Step-by-step solution**:

$$\int_a^b [4f(x) - 2g(x) + h(x)] \, dx$$

$$= 4\int_a^b f(x) \, dx - 2\int_a^b g(x) \, dx + \int_a^b h(x) \, dx$$

$$= 4(5) - 2(-2) + 3 = 20 + 4 + 3 = 27$$

</details>

---

<details>
<summary><strong>Problem 12 Solution</strong></summary>

**Answer**: $6$

**Step-by-step solution**:

For an even function, $f(-x) = f(x)$, so the graph is symmetric about the y-axis.

$$\int_{-3}^3 f(x) \, dx = 2\int_0^3 f(x) \, dx$$

$$12 = 2\int_0^3 f(x) \, dx$$

$$\int_0^3 f(x) \, dx = 6$$

</details>

---

<details>
<summary><strong>Problem 13 Solution</strong></summary>

**Answer**: $0$

**Step-by-step solution**:

For an odd function, $f(-x) = -f(x)$.

The integral over a symmetric interval equals zero:

$$\int_{-4}^4 f(x) \, dx = 0$$

This is because the positive area on one side exactly cancels the negative area on the other side.

</details>

---

<details>
<summary><strong>Problem 14 Solution</strong></summary>

**Answer**: (a) $\frac{\pi}{2}$, (b) $2 + \frac{\pi}{2}$

**Step-by-step solution**:

**(a)** The semicircle above the x-axis from $x = 0$ to $x = 2$ has radius 1 (diameter 2).

Area of semicircle = $\frac{1}{2}\pi(1)^2 = \frac{\pi}{2}$

$$\int_0^2 f'(x) \, dx = \frac{\pi}{2}$$

**(b)** By the Fundamental Theorem:

$$\int_0^2 f'(x) \, dx = f(2) - f(0)$$

$$\frac{\pi}{2} = f(2) - 2$$

$$f(2) = 2 + \frac{\pi}{2}$$

</details>

---

<details>
<summary><strong>Problem 15 Solution</strong></summary>

**Answer**: Proof shown below.

**Step-by-step solution**:

The definite integral is defined as:
$$\int_a^b f(x) \, dx = \lim_{n \to \infty} \sum_{i=1}^{n} f(x_i^*) \Delta x$$

Since $f(x) \geq 0$ for all $x$ in $[a, b]$:
- Each $f(x_i^*) \geq 0$
- $\Delta x = \frac{b-a}{n} > 0$ (assuming $b > a$)

Therefore each term $f(x_i^*) \Delta x \geq 0$.

The sum of non-negative terms is non-negative:
$$\sum_{i=1}^{n} f(x_i^*) \Delta x \geq 0$$

The limit of non-negative values is non-negative:
$$\int_a^b f(x) \, dx = \lim_{n \to \infty} \sum_{i=1}^{n} f(x_i^*) \Delta x \geq 0$$

</details>

---

<details>
<summary><strong>Problem 16 Solution</strong></summary>

**Answer**: **(C)** $4$

**Step-by-step solution**:

Using additivity:

$$\int_1^3 f(x) \, dx + \int_3^5 f(x) \, dx = \int_1^5 f(x) \, dx$$

$$\int_1^3 f(x) \, dx + 2 = 6$$

$$\int_1^3 f(x) \, dx = 4$$

</details>

---

<details>
<summary><strong>Problem 17 Solution</strong></summary>

**Answer**: **(A)** $6 - 2\pi$

**Step-by-step solution**:

Semicircle (below x-axis):
- Radius = 2
- Area = $\frac{1}{2}\pi(2)^2 = 2\pi$
- Contributes $-2\pi$ to the signed area

Triangular regions (above x-axis):
- Total area = 6
- Contributes $+6$ to the signed area

$$\int_{-4}^4 f(x) \, dx = 6 + (-2\pi) = 6 - 2\pi$$

</details>

---

<details>
<summary><strong>Problem 18 Solution</strong></summary>

**Answer**: (a) $14$, (b) $5$, (c) $9$

**(a)**:
$$\int_0^4 [3f(x) - 2g(x)] \, dx = 3(8) - 2(5) = 24 - 10 = 14$$

**(b)**:
$$\int_0^2 f(x) \, dx + \int_2^4 f(x) \, dx = \int_0^4 f(x) \, dx$$
$$\int_0^2 f(x) \, dx + 3 = 8$$
$$\int_0^2 f(x) \, dx = 5$$

**(c)**:
First find $\int_0^2 g(x) \, dx$:
$$\int_0^2 g(x) \, dx + \int_2^4 g(x) \, dx = \int_0^4 g(x) \, dx$$
$$\int_0^2 g(x) \, dx + 1 = 5$$
$$\int_0^2 g(x) \, dx = 4$$

Then:
$$\int_0^2 [f(x) + g(x)] \, dx = \int_0^2 f(x) \, dx + \int_0^2 g(x) \, dx = 5 + 4 = 9$$

</details>

---

<details>
<summary><strong>Problem 19 Solution</strong></summary>

**Answer**: **(C)** $\int_0^{10} r(t) \, dt$

**Step-by-step solution**:

If $r(t)$ represents the rate of water flow (gallons per minute), then the total amount of water that flows into the tank is the integral of the rate over the time interval:

$$\text{Total water} = \int_0^{10} r(t) \, dt$$

(A) is wrong because it gives the change in the rate, not the accumulated amount.
(B) gives the instantaneous rate of change of the rate.
(D) gives the change in the rate function.

</details>

---

<details>
<summary><strong>Problem 20 Solution</strong></summary>

**Answer**: See detailed solution below.

**(a) Displacement**:

$$\int_0^5 (t^2 - 4t + 3) \, dt = \left[\frac{t^3}{3} - 2t^2 + 3t\right]_0^5$$

$$= \frac{125}{3} - 50 + 15 - 0 = \frac{125}{3} - 35 = \frac{125 - 105}{3} = \frac{20}{3}$$

**(b) Direction changes**:

$v(t) = 0$ when $t^2 - 4t + 3 = (t-1)(t-3) = 0$

$t = 1$ and $t = 3$

Check sign changes:
- $v(0) = 3 > 0$
- $v(2) = -1 < 0$
- $v(4) = 3 > 0$

Particle changes direction at $t = 1$ and $t = 3$.

**(c) Total distance**:

$$\int_0^1 |v(t)| \, dt + \int_1^3 |v(t)| \, dt + \int_3^5 |v(t)| \, dt$$

$$= \int_0^1 (t^2 - 4t + 3) \, dt + \int_1^3 -(t^2 - 4t + 3) \, dt + \int_3^5 (t^2 - 4t + 3) \, dt$$

**(d)** Total distance is **greater than** displacement.

The particle moves right, then left, then right again. The back-and-forth motion means the total path length exceeds the net displacement. Displacement only measures "how far from start" while distance measures "how far traveled."

</details>

---

## What's Next

Now that you understand definite integrals, you're ready for the [Fundamental Theorem of Calculus](/calculus/0604-fundamental-theorem)—the crown jewel that connects differentiation and integration in one beautiful statement.

---

<div align="center">

[← Riemann Sums](/calculus/0602-riemann-sums) | [Fundamental Theorem →](/calculus/0604-fundamental-theorem)

</div>
