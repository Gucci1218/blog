# Volume: Disk and Washer Methods

*Take a two-dimensional region and spin it around an axis—you get a three-dimensional solid. But how do you calculate the volume of these curvy shapes? The disk and washer methods slice these solids into thin circular pieces, then integrate to find the exact volume. It's like stacking infinitely many coins to build a sculpture.*

---

## What You'll Learn
- Visualize solids of revolution
- Apply the disk method for solid rotations
- Apply the washer method when there's a hole
- Choose the correct method based on the axis of rotation
- Set up volume integrals from graphs and equations

---

## Prerequisites
- [Definite Integrals](/calculus/definite-integrals)
- [Area Between Curves](/calculus/area-between-curves)

---

## The Core Concept

### What Is a Solid of Revolution?

When you rotate a region around an axis, the resulting 3D shape is called a **solid of revolution**.

**Examples**:
- Rotate a rectangle around one edge → cylinder
- Rotate a right triangle around one leg → cone
- Rotate a semicircle around its diameter → sphere

### The Disk Method

When rotating around an axis with no gap between the region and the axis:

**For rotation around the x-axis**:

$$V = \int_a^b \pi [f(x)]^2 \, dx$$

**For rotation around the y-axis** (when given $x = g(y)$):

$$V = \int_c^d \pi [g(y)]^2 \, dy$$

**Why $\pi r^2$?**

Each thin slice perpendicular to the axis of rotation is a **disk** (a filled circle):
- Radius = $f(x)$ (distance from axis to curve)
- Area of disk = $\pi r^2 = \pi [f(x)]^2$
- Thickness = $dx$
- Volume of thin disk = $\pi [f(x)]^2 \, dx$

Stack all disks → integrate!

### The Washer Method

When there's a **gap** between the region and the axis (creating a hole in the solid):

$$V = \int_a^b \pi \left([R(x)]^2 - [r(x)]^2\right) dx$$

where:
- $R(x)$ = **outer radius** (distance from axis to outer curve)
- $r(x)$ = **inner radius** (distance from axis to inner curve)

**Why "washer"?** Each slice looks like a washer (a disk with a hole)—the area is $\pi R^2 - \pi r^2$.

### Setting Up the Integral: Key Steps

1. **Sketch the region** and the axis of rotation
2. **Identify the slice direction**: perpendicular to the axis of rotation
3. **Find the radius/radii**: distance from axis to curve(s)
4. **Determine limits**: where does the region begin and end?
5. **Write and evaluate** the integral

### Rotating Around Different Axes

**Around x-axis**: Slice vertically, integrate with respect to x
- Radius = y-value = $f(x)$

**Around y-axis**: Slice horizontally, integrate with respect to y
- Radius = x-value = $g(y)$

**Around $y = k$ (horizontal line)**:
- Radius = |distance from curve to line| = $|f(x) - k|$

**Around $x = k$ (vertical line)**:
- Radius = |distance from curve to line| = $|x - k|$ or $|g(y) - k|$

### Worked Examples

**Example 1**: Find the volume when $y = \sqrt{x}$ from $x = 0$ to $x = 4$ is rotated around the x-axis.

**Solution**:

Using the disk method:
- Radius = $f(x) = \sqrt{x}$
- Limits: $x = 0$ to $x = 4$

$$V = \int_0^4 \pi (\sqrt{x})^2 \, dx = \pi \int_0^4 x \, dx$$

$$= \pi \left[\frac{x^2}{2}\right]_0^4 = \pi \cdot \frac{16}{2} = 8\pi$$

---

**Example 2**: Find the volume when the region bounded by $y = x^2$ and $y = 4$ is rotated around the x-axis.

**Solution**:

This creates a washer (the parabola is below the line $y = 4$).

- Outer radius: $R = 4$ (the line)
- Inner radius: $r = x^2$ (the parabola)
- Limits: $x^2 = 4 \Rightarrow x = \pm 2$

$$V = \int_{-2}^{2} \pi [4^2 - (x^2)^2] \, dx = \pi \int_{-2}^{2} (16 - x^4) \, dx$$

$$= \pi \left[16x - \frac{x^5}{5}\right]_{-2}^{2}$$

$$= \pi \left[\left(32 - \frac{32}{5}\right) - \left(-32 + \frac{32}{5}\right)\right]$$

$$= \pi \left[64 - \frac{64}{5}\right] = \pi \cdot \frac{256}{5} = \frac{256\pi}{5}$$

---

**Example 3**: Find the volume when $y = x^2$ from $x = 0$ to $x = 2$ is rotated around the y-axis.

**Solution**:

For rotation around the y-axis, slice horizontally and integrate with respect to y.

Solve for x: $x = \sqrt{y}$
Limits: When $x = 0$, $y = 0$. When $x = 2$, $y = 4$.

$$V = \int_0^4 \pi (\sqrt{y})^2 \, dy = \pi \int_0^4 y \, dy$$

$$= \pi \left[\frac{y^2}{2}\right]_0^4 = \pi \cdot 8 = 8\pi$$

---

**Example 4**: Find the volume when the region bounded by $y = x$ and $y = x^2$ is rotated around the x-axis.

**Solution**:

Intersection: $x = x^2 \Rightarrow x = 0, 1$

On $[0, 1]$: $y = x$ is the outer curve, $y = x^2$ is the inner curve.

$$V = \int_0^1 \pi [(x)^2 - (x^2)^2] \, dx = \pi \int_0^1 (x^2 - x^4) \, dx$$

$$= \pi \left[\frac{x^3}{3} - \frac{x^5}{5}\right]_0^1 = \pi \left(\frac{1}{3} - \frac{1}{5}\right) = \pi \cdot \frac{2}{15} = \frac{2\pi}{15}$$

---

**Example 5**: Find the volume when $y = \sqrt{x}$ from $x = 1$ to $x = 4$ is rotated around the line $y = -1$.

**Solution**:

The axis is below the curve. Radius = distance from curve to axis.

$$R(x) = \sqrt{x} - (-1) = \sqrt{x} + 1$$

$$V = \int_1^4 \pi (\sqrt{x} + 1)^2 \, dx = \pi \int_1^4 (x + 2\sqrt{x} + 1) \, dx$$

$$= \pi \left[\frac{x^2}{2} + \frac{4x^{3/2}}{3} + x\right]_1^4$$

$$= \pi \left[\left(8 + \frac{32}{3} + 4\right) - \left(\frac{1}{2} + \frac{4}{3} + 1\right)\right]$$

$$= \pi \left[12 + \frac{32}{3} - \frac{3}{2} - \frac{4}{3}\right] = \pi \left[12 + \frac{28}{3} - \frac{3}{2}\right]$$

$$= \pi \left[\frac{72 + 56 - 9}{6}\right] = \frac{119\pi}{6}$$

---

**Example 6**: Find the volume of a sphere of radius $r$.

**Solution**:

A sphere is generated by rotating the semicircle $y = \sqrt{r^2 - x^2}$ around the x-axis.

$$V = \int_{-r}^{r} \pi (\sqrt{r^2 - x^2})^2 \, dx = \pi \int_{-r}^{r} (r^2 - x^2) \, dx$$

$$= \pi \left[r^2 x - \frac{x^3}{3}\right]_{-r}^{r}$$

$$= \pi \left[\left(r^3 - \frac{r^3}{3}\right) - \left(-r^3 + \frac{r^3}{3}\right)\right]$$

$$= \pi \left[2r^3 - \frac{2r^3}{3}\right] = \pi \cdot \frac{4r^3}{3} = \frac{4\pi r^3}{3}$$

This confirms the sphere volume formula!

---

## Key Formulas & Rules

| Method | Formula |
|--------|---------|
| Disk (around x-axis) | $V = \int_a^b \pi [f(x)]^2 \, dx$ |
| Disk (around y-axis) | $V = \int_c^d \pi [g(y)]^2 \, dy$ |
| Washer (around x-axis) | $V = \int_a^b \pi [R(x)^2 - r(x)^2] \, dx$ |
| Washer (around y-axis) | $V = \int_c^d \pi [R(y)^2 - r(y)^2] \, dy$ |

**Radius formulas for shifted axes**:

| Axis | Radius |
|------|--------|
| $y = k$ (below curve) | $R = f(x) - k$ |
| $y = k$ (above curve) | $R = k - f(x)$ |
| $x = k$ (right of curve) | $R = k - g(y)$ |
| $x = k$ (left of curve) | $R = g(y) - k$ |

---

## Common Mistakes to Avoid

1. **Forgetting to square**: Volume = $\pi r^2$, not $\pi r$.

2. **Wrong radius for shifted axis**: The radius is the distance from the curve to the axis, not the y-value.

3. **Subtracting in wrong order**: Always outer² - inner² (not inner² - outer²).

4. **Using wrong variable**: Match dx with x-limits, dy with y-limits.

5. **Forgetting $\pi$**: Every disk/washer integral has $\pi$ in front.

6. **Not visualizing the solid**: Always sketch to identify inner and outer radii.

---

## AP Exam Tips

### For Both AB and BC:
- Disk/washer problems appear on nearly every AP exam
- Practice setting up integrals from graphs (no equations given)
- Know how to handle non-standard axes of rotation
- Show your setup clearly—partial credit is available

### Common Question Types:
1. **Standard rotation**: Around x-axis or y-axis
2. **Shifted axis**: Around $y = k$ or $x = k$
3. **Calculator active**: Set up integral, use calculator to evaluate
4. **Conceptual**: Identify which method to use

### Time-Saving Tips:
- Memorize the formulas
- Draw the axis of rotation and label radii
- Check your answer's units and reasonableness

---

## Practice Problems

### Basic (Problems 1-5)

**1.** Find the volume when:

$$y = x^2$$

from $x = 0$ to $x = 3$ is rotated around the x-axis.

---

**2.** Find the volume when:

$$y = 2x$$

from $x = 0$ to $x = 4$ is rotated around the x-axis.

---

**3.** Find the volume when:

$$x = y^2$$

from $y = 0$ to $y = 2$ is rotated around the y-axis.

---

**4.** Find the volume when:

$$y = \sqrt{x}$$

from $x = 0$ to $x = 9$ is rotated around the x-axis.

---

**5.** Find the volume of a cone with radius 3 and height 6 using integration.

---

### Intermediate (Problems 6-10)

**6.** Find the volume when the region bounded by:

$$y = x^2 \quad \text{and} \quad y = x$$

is rotated around the x-axis.

---

**7.** Find the volume when the region bounded by:

$$y = \sqrt{x}, \quad y = 0, \quad x = 4$$

is rotated around the y-axis.

---

**8.** Find the volume when:

$$y = e^x$$

from $x = 0$ to $x = 1$ is rotated around the x-axis.

---

**9.** Find the volume when the region bounded by:

$$y = 4 - x^2 \quad \text{and} \quad y = 0$$

is rotated around the x-axis.

---

**10.** Find the volume when:

$$y = \frac{1}{x}$$

from $x = 1$ to $x = 3$ is rotated around the x-axis.

---

### Advanced (Problems 11-15)

**11.** Find the volume when the region bounded by:

$$y = x^2 \quad \text{and} \quad y = 4$$

is rotated around the line $y = 4$.

---

**12.** Find the volume when:

$$y = \sin x$$

from $x = 0$ to $x = \pi$ is rotated around the x-axis.

---

**13.** Find the volume when the region bounded by:

$$y = x, \quad y = 0, \quad x = 2$$

is rotated around the line $x = 3$.

---

**14.** Find the volume when the region bounded by:

$$y = \sqrt{x} \quad \text{and} \quad y = x$$

is rotated around the line $y = 1$.

---

**15.** A region is bounded by $y = x^3$, $y = 0$, and $x = 2$. Set up integrals for the volume when rotated around:
**(a)** the x-axis
**(b)** the y-axis
**(c)** the line $y = 8$

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

The region bounded by $y = x^2$ and $y = 2x$ is rotated around the x-axis. The volume is:

| Choice | Answer |
|--------|--------|
| **(A)** | $\frac{64\pi}{15}$ |
| **(B)** | $\frac{32\pi}{15}$ |
| **(C)** | $\frac{8\pi}{3}$ |
| **(D)** | $\frac{16\pi}{3}$ |

---

#### Problem 17 (Multiple Choice)

The volume of the solid generated by rotating the region bounded by $y = \sqrt{x}$, $y = 0$, and $x = 4$ around the line $y = 2$ is given by:

| Choice | Answer |
|--------|--------|
| **(A)** | $\int_0^4 \pi(2 - \sqrt{x})^2 \, dx$ |
| **(B)** | $\int_0^4 \pi[(2)^2 - (\sqrt{x})^2] \, dx$ |
| **(C)** | $\int_0^4 \pi[(2)^2 - (2 - \sqrt{x})^2] \, dx$ |
| **(D)** | $\int_0^2 \pi(4 - y^2)^2 \, dy$ |

---

#### Problem 18 (Free Response)

Let R be the region bounded by $y = x^2 + 1$ and $y = 5$.

> **(a)** Find the area of R.
>
> **(b)** Find the volume when R is rotated around the x-axis.
>
> **(c)** Find the volume when R is rotated around the line $y = 5$.

---

#### Problem 19 (Multiple Choice)

The region in the first quadrant bounded by $y = x^3$, $x = 0$, and $y = 8$ is rotated around the y-axis. The volume is:

| Choice | Answer |
|--------|--------|
| **(A)** | $\frac{96\pi}{5}$ |
| **(B)** | $\frac{48\pi}{5}$ |
| **(C)** | $32\pi$ |
| **(D)** | $\frac{64\pi}{5}$ |

---

#### Problem 20 (Free Response - Challenging)

Let R be the region enclosed by $y = 4 - x^2$ and $y = x + 2$.

> **(a)** Sketch R and find the points of intersection.
>
> **(b)** Set up, but do not evaluate, an integral for the volume when R is rotated around the x-axis.
>
> **(c)** Set up, but do not evaluate, an integral for the volume when R is rotated around the line $y = -2$.
>
> **(d)** Which volume is larger—part (b) or part (c)? Explain without evaluating.

---

## Answer Key

<details>
<summary><strong>Problem 1 Solution</strong></summary>

**Answer**: $\frac{243\pi}{5}$

**Step-by-step solution**:

$$V = \int_0^3 \pi (x^2)^2 \, dx = \pi \int_0^3 x^4 \, dx = \pi \left[\frac{x^5}{5}\right]_0^3 = \pi \cdot \frac{243}{5} = \frac{243\pi}{5}$$

</details>

---

<details>
<summary><strong>Problem 2 Solution</strong></summary>

**Answer**: $\frac{256\pi}{3}$

**Step-by-step solution**:

$$V = \int_0^4 \pi (2x)^2 \, dx = \pi \int_0^4 4x^2 \, dx = 4\pi \left[\frac{x^3}{3}\right]_0^4 = 4\pi \cdot \frac{64}{3} = \frac{256\pi}{3}$$

</details>

---

<details>
<summary><strong>Problem 3 Solution</strong></summary>

**Answer**: $\frac{32\pi}{5}$

**Step-by-step solution**:

$$V = \int_0^2 \pi (y^2)^2 \, dy = \pi \int_0^2 y^4 \, dy = \pi \left[\frac{y^5}{5}\right]_0^2 = \pi \cdot \frac{32}{5} = \frac{32\pi}{5}$$

</details>

---

<details>
<summary><strong>Problem 4 Solution</strong></summary>

**Answer**: $\frac{81\pi}{2}$

**Step-by-step solution**:

$$V = \int_0^9 \pi (\sqrt{x})^2 \, dx = \pi \int_0^9 x \, dx = \pi \left[\frac{x^2}{2}\right]_0^9 = \pi \cdot \frac{81}{2} = \frac{81\pi}{2}$$

</details>

---

<details>
<summary><strong>Problem 5 Solution</strong></summary>

**Answer**: $18\pi$

**Step-by-step solution**:

A cone with height 6 and radius 3 can be formed by rotating the line $y = \frac{3}{6}x = \frac{x}{2}$ from $x = 0$ to $x = 6$ around the x-axis.

$$V = \int_0^6 \pi \left(\frac{x}{2}\right)^2 dx = \pi \int_0^6 \frac{x^2}{4} \, dx = \frac{\pi}{4} \left[\frac{x^3}{3}\right]_0^6$$

$$= \frac{\pi}{4} \cdot \frac{216}{3} = \frac{\pi}{4} \cdot 72 = 18\pi$$

Verification: $V = \frac{1}{3}\pi r^2 h = \frac{1}{3}\pi(9)(6) = 18\pi$ ✓

</details>

---

<details>
<summary><strong>Problem 6 Solution</strong></summary>

**Answer**: $\frac{2\pi}{15}$

**Step-by-step solution**:

Intersections: $x^2 = x \Rightarrow x = 0, 1$

On $[0, 1]$: $y = x$ is outer, $y = x^2$ is inner.

$$V = \int_0^1 \pi [x^2 - (x^2)^2] \, dx = \pi \int_0^1 (x^2 - x^4) \, dx$$

$$= \pi \left[\frac{x^3}{3} - \frac{x^5}{5}\right]_0^1 = \pi \left(\frac{1}{3} - \frac{1}{5}\right) = \frac{2\pi}{15}$$

</details>

---

<details>
<summary><strong>Problem 7 Solution</strong></summary>

**Answer**: $8\pi$

**Step-by-step solution**:

For rotation around y-axis, use horizontal slices.

$y = \sqrt{x} \Rightarrow x = y^2$

When $x = 4$, $y = 2$.

$$V = \int_0^2 \pi (y^2)^2 \, dy$$

Wait, that's not right. Let me reconsider.

Actually, for this region rotated around the y-axis, the outer radius is $x = 4$ and inner radius is $x = y^2$.

$$V = \int_0^2 \pi [4^2 - (y^2)^2] \, dy = \pi \int_0^2 (16 - y^4) \, dy$$

$$= \pi \left[16y - \frac{y^5}{5}\right]_0^2 = \pi \left(32 - \frac{32}{5}\right) = \pi \cdot \frac{128}{5} = \frac{128\pi}{5}$$

</details>

---

<details>
<summary><strong>Problem 8 Solution</strong></summary>

**Answer**: $\frac{\pi(e^2 - 1)}{2}$

**Step-by-step solution**:

$$V = \int_0^1 \pi (e^x)^2 \, dx = \pi \int_0^1 e^{2x} \, dx = \pi \left[\frac{e^{2x}}{2}\right]_0^1$$

$$= \frac{\pi}{2}(e^2 - 1)$$

</details>

---

<details>
<summary><strong>Problem 9 Solution</strong></summary>

**Answer**: $\frac{256\pi}{15}$

**Step-by-step solution**:

Intersections with x-axis: $4 - x^2 = 0 \Rightarrow x = \pm 2$

$$V = \int_{-2}^{2} \pi (4 - x^2)^2 \, dx = \pi \int_{-2}^{2} (16 - 8x^2 + x^4) \, dx$$

$$= \pi \left[16x - \frac{8x^3}{3} + \frac{x^5}{5}\right]_{-2}^{2}$$

$$= \pi \left[\left(32 - \frac{64}{3} + \frac{32}{5}\right) - \left(-32 + \frac{64}{3} - \frac{32}{5}\right)\right]$$

$$= \pi \left[64 - \frac{128}{3} + \frac{64}{5}\right] = \pi \cdot \frac{960 - 640 + 192}{15} = \frac{512\pi}{15}$$

</details>

---

<details>
<summary><strong>Problem 10 Solution</strong></summary>

**Answer**: $\frac{2\pi}{3}$

**Step-by-step solution**:

$$V = \int_1^3 \pi \left(\frac{1}{x}\right)^2 dx = \pi \int_1^3 x^{-2} \, dx = \pi \left[-x^{-1}\right]_1^3$$

$$= \pi \left(-\frac{1}{3} + 1\right) = \frac{2\pi}{3}$$

</details>

---

<details>
<summary><strong>Problem 11 Solution</strong></summary>

**Answer**: $\frac{512\pi}{15}$

**Step-by-step solution**:

Rotating around $y = 4$: The radius is distance from curve to axis.

$R(x) = 4 - x^2$ (distance from parabola to line $y = 4$)

Limits: $x^2 = 4 \Rightarrow x = \pm 2$

$$V = \int_{-2}^{2} \pi (4 - x^2)^2 \, dx$$

This is the same integral as Problem 9: $\frac{512\pi}{15}$

</details>

---

<details>
<summary><strong>Problem 12 Solution</strong></summary>

**Answer**: $\frac{\pi^2}{2}$

**Step-by-step solution**:

$$V = \int_0^{\pi} \pi (\sin x)^2 \, dx = \pi \int_0^{\pi} \sin^2 x \, dx$$

Using $\sin^2 x = \frac{1 - \cos 2x}{2}$:

$$= \pi \int_0^{\pi} \frac{1 - \cos 2x}{2} \, dx = \frac{\pi}{2} \left[x - \frac{\sin 2x}{2}\right]_0^{\pi}$$

$$= \frac{\pi}{2} (\pi - 0) = \frac{\pi^2}{2}$$

</details>

---

<details>
<summary><strong>Problem 13 Solution</strong></summary>

**Answer**: $\frac{20\pi}{3}$

**Step-by-step solution**:

Rotating around $x = 3$. Use washers with horizontal slices.

$y$ goes from 0 to 2.

At height $y$: The region extends from $x = 0$ to $x = y$ (since $y = x$).

Outer radius: $R = 3 - 0 = 3$
Inner radius: $r = 3 - y$

$$V = \int_0^2 \pi [3^2 - (3-y)^2] \, dy = \pi \int_0^2 [9 - 9 + 6y - y^2] \, dy$$

$$= \pi \int_0^2 (6y - y^2) \, dy = \pi \left[3y^2 - \frac{y^3}{3}\right]_0^2$$

$$= \pi \left(12 - \frac{8}{3}\right) = \frac{28\pi}{3}$$

</details>

---

<details>
<summary><strong>Problem 14 Solution</strong></summary>

**Answer**: $\frac{\pi}{6}$

**Step-by-step solution**:

Intersections: $\sqrt{x} = x \Rightarrow x = 0, 1$

Rotating around $y = 1$. Both curves are below $y = 1$.

Outer radius: $R = 1 - x$ (from $y = 1$ to $y = x$)
Inner radius: $r = 1 - \sqrt{x}$ (from $y = 1$ to $y = \sqrt{x}$)

$$V = \int_0^1 \pi [(1-x)^2 - (1-\sqrt{x})^2] \, dx$$

$$= \pi \int_0^1 [(1 - 2x + x^2) - (1 - 2\sqrt{x} + x)] \, dx$$

$$= \pi \int_0^1 (x^2 - 3x + 2\sqrt{x}) \, dx$$

$$= \pi \left[\frac{x^3}{3} - \frac{3x^2}{2} + \frac{4x^{3/2}}{3}\right]_0^1$$

$$= \pi \left(\frac{1}{3} - \frac{3}{2} + \frac{4}{3}\right) = \pi \left(\frac{5}{3} - \frac{3}{2}\right) = \pi \cdot \frac{1}{6} = \frac{\pi}{6}$$

</details>

---

<details>
<summary><strong>Problem 15 Solution</strong></summary>

**Answer**: See solutions below.

**(a) Around x-axis**:
$$V = \int_0^2 \pi (x^3)^2 \, dx = \int_0^2 \pi x^6 \, dx$$

**(b) Around y-axis**:
$x = y^{1/3}$, $y$ from 0 to 8:
$$V = \int_0^8 \pi (y^{1/3})^2 \, dy = \int_0^8 \pi y^{2/3} \, dy$$

**(c) Around $y = 8$**:
$R = 8 - x^3$:
$$V = \int_0^2 \pi (8 - x^3)^2 \, dx$$

</details>

---

<details>
<summary><strong>Problem 16 Solution</strong></summary>

**Answer**: **(A)** $\frac{64\pi}{15}$

**Step-by-step solution**:

Intersections: $x^2 = 2x \Rightarrow x = 0, 2$

Outer: $y = 2x$, Inner: $y = x^2$

$$V = \int_0^2 \pi [(2x)^2 - (x^2)^2] \, dx = \pi \int_0^2 (4x^2 - x^4) \, dx$$

$$= \pi \left[\frac{4x^3}{3} - \frac{x^5}{5}\right]_0^2 = \pi \left(\frac{32}{3} - \frac{32}{5}\right) = \pi \cdot \frac{64}{15} = \frac{64\pi}{15}$$

</details>

---

<details>
<summary><strong>Problem 17 Solution</strong></summary>

**Answer**: **(C)** $\int_0^4 \pi[(2)^2 - (2 - \sqrt{x})^2] \, dx$

**Step-by-step solution**:

The axis $y = 2$ is above the curve $y = \sqrt{x}$.

Outer radius from $y = 0$ to axis: $R = 2 - 0 = 2$
Inner radius from $y = \sqrt{x}$ to axis: $r = 2 - \sqrt{x}$

$$V = \int_0^4 \pi [2^2 - (2 - \sqrt{x})^2] \, dx$$

</details>

---

<details>
<summary><strong>Problem 18 Solution</strong></summary>

**Answer**: See detailed solution below.

**(a) Area of R**:

Intersections: $x^2 + 1 = 5 \Rightarrow x = \pm 2$

$$\text{Area} = \int_{-2}^{2} [5 - (x^2 + 1)] \, dx = \int_{-2}^{2} (4 - x^2) \, dx = \left[4x - \frac{x^3}{3}\right]_{-2}^{2} = \frac{32}{3}$$

**(b) Volume around x-axis**:

Outer: $R = 5$, Inner: $r = x^2 + 1$

$$V = \int_{-2}^{2} \pi [25 - (x^2 + 1)^2] \, dx = \int_{-2}^{2} \pi [25 - x^4 - 2x^2 - 1] \, dx$$

$$= \pi \int_{-2}^{2} (24 - 2x^2 - x^4) \, dx = \pi \left[24x - \frac{2x^3}{3} - \frac{x^5}{5}\right]_{-2}^{2}$$

$$= \pi \left[\left(48 - \frac{16}{3} - \frac{32}{5}\right) - \left(-48 + \frac{16}{3} + \frac{32}{5}\right)\right] = \frac{1856\pi}{15}$$

**(c) Volume around $y = 5$**:

Radius: $R = 5 - (x^2 + 1) = 4 - x^2$

$$V = \int_{-2}^{2} \pi (4 - x^2)^2 \, dx = \frac{512\pi}{15}$$

</details>

---

<details>
<summary><strong>Problem 19 Solution</strong></summary>

**Answer**: **(A)** $\frac{96\pi}{5}$

**Step-by-step solution**:

For rotation around y-axis, use horizontal slices.

$y = x^3 \Rightarrow x = y^{1/3}$

$$V = \int_0^8 \pi (y^{1/3})^2 \, dy = \pi \int_0^8 y^{2/3} \, dy = \pi \left[\frac{y^{5/3}}{5/3}\right]_0^8$$

$$= \frac{3\pi}{5} \cdot 8^{5/3} = \frac{3\pi}{5} \cdot 32 = \frac{96\pi}{5}$$

</details>

---

<details>
<summary><strong>Problem 20 Solution</strong></summary>

**Answer**: See detailed solution below.

**(a)** Intersections:
$4 - x^2 = x + 2$
$x^2 + x - 2 = 0$
$(x + 2)(x - 1) = 0$
$x = -2, 1$

Points: $(-2, 0)$ and $(1, 3)$

**(b)** Around x-axis:

Outer: $y = 4 - x^2$, Inner: $y = x + 2$

$$V = \int_{-2}^{1} \pi [(4 - x^2)^2 - (x + 2)^2] \, dx$$

**(c)** Around $y = -2$:

Both curves are above $y = -2$.

Outer radius: $R = (4 - x^2) - (-2) = 6 - x^2$
Inner radius: $r = (x + 2) - (-2) = x + 4$

$$V = \int_{-2}^{1} \pi [(6 - x^2)^2 - (x + 4)^2] \, dx$$

**(d)** The volume in part (c) is larger because the axis is further from the region. When you move the axis of rotation away from a region, the resulting solid has a larger "hole" but an even larger outer radius, resulting in greater volume. The radii in (c) are larger than in (b), so the washer areas are larger.

</details>

---

## What's Next

You've mastered disk and washer methods. Now learn the [Shell Method](/calculus/volume-shell), an alternative technique that's sometimes easier—especially when rotating around the y-axis.

---

<div align="center">

[← Area Between Curves](/calculus/area-between-curves) | [Volume: Shell Method →](/calculus/volume-shell)

</div>
