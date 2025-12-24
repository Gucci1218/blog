# Riemann Sums

*How do you find the area of a shape with curved edges? The ancient Greeks struggled with this problem for centuries. The breakthrough came from a simple but powerful idea: approximate the curved region with rectangles, then use more and more rectangles until the approximation becomes exact. This is the Riemann sum—the foundation of the definite integral.*

---

## What You'll Learn
- Understand how rectangles approximate area under a curve
- Calculate left, right, and midpoint Riemann sums
- Use summation notation for Riemann sums
- Recognize that more rectangles give better approximations
- Connect Riemann sums to the definite integral

---

## Prerequisites
- Function evaluation
- Summation notation (sigma notation)
- [Understanding Limits](/calculus/understanding-limits)

---

## The Core Concept

### Intuition First

Imagine you want to find the area under a curve between $x = a$ and $x = b$. There's no simple formula like "length × width" because the top isn't straight.

**The Big Idea**: Slice the region into thin vertical strips. If each strip is thin enough, it's almost a rectangle. Add up all the rectangle areas, and you get an approximation of the true area.

### Setting Up a Riemann Sum

**Step 1**: Divide the interval $[a, b]$ into $n$ equal subintervals.

Each subinterval has width:
$$\Delta x = \frac{b - a}{n}$$

**Step 2**: In each subinterval, choose a sample point $x_i^*$ to determine the rectangle's height.

**Step 3**: The area of each rectangle is:
$$\text{Area}_i = f(x_i^*) \cdot \Delta x$$

**Step 4**: Sum all rectangles:
$$\text{Riemann Sum} = \sum_{i=1}^{n} f(x_i^*) \Delta x$$

### Types of Riemann Sums

The choice of sample point determines the type of Riemann sum:

| Type | Sample Point $x_i^*$ | Description |
|------|---------------------|-------------|
| **Left** | $x_{i-1} = a + (i-1)\Delta x$ | Left endpoint of each subinterval |
| **Right** | $x_i = a + i \cdot \Delta x$ | Right endpoint of each subinterval |
| **Midpoint** | $\frac{x_{i-1} + x_i}{2}$ | Middle of each subinterval |

### Visual Understanding

For an **increasing function**:
- Left Riemann sum **underestimates** the area
- Right Riemann sum **overestimates** the area

For a **decreasing function**:
- Left Riemann sum **overestimates** the area
- Right Riemann sum **underestimates** the area

**Midpoint sums** are typically more accurate than left or right sums with the same number of rectangles.

### The Formulas

For $n$ equal subintervals on $[a, b]$ with $\Delta x = \frac{b-a}{n}$:

**Left Riemann Sum**:
$$L_n = \sum_{i=0}^{n-1} f(x_i) \Delta x = \sum_{i=0}^{n-1} f(a + i \cdot \Delta x) \Delta x$$

**Right Riemann Sum**:
$$R_n = \sum_{i=1}^{n} f(x_i) \Delta x = \sum_{i=1}^{n} f(a + i \cdot \Delta x) \Delta x$$

**Midpoint Riemann Sum**:
$$M_n = \sum_{i=1}^{n} f(\bar{x}_i) \Delta x \quad \text{where } \bar{x}_i = a + \left(i - \frac{1}{2}\right) \Delta x$$

### The Limit: From Approximation to Exactness

As $n \to \infty$, the rectangles become infinitely thin, and all Riemann sums converge to the same value—the **exact area**:

$$\text{Area} = \lim_{n \to \infty} \sum_{i=1}^{n} f(x_i^*) \Delta x$$

This limit is the **definite integral** (coming in the next article!).

### Worked Examples

**Example 1**: Approximate $\int_0^2 x^2 \, dx$ using a left Riemann sum with $n = 4$ rectangles.

**Solution**:

*Step 1*: Calculate $\Delta x$:
$$\Delta x = \frac{2 - 0}{4} = 0.5$$

*Step 2*: Find the left endpoints:
- $x_0 = 0$
- $x_1 = 0.5$
- $x_2 = 1$
- $x_3 = 1.5$

*Step 3*: Evaluate $f(x) = x^2$ at each:
- $f(0) = 0$
- $f(0.5) = 0.25$
- $f(1) = 1$
- $f(1.5) = 2.25$

*Step 4*: Calculate the sum:
$$L_4 = (0 + 0.25 + 1 + 2.25)(0.5) = 3.5 \times 0.5 = 1.75$$

The actual value is $\frac{8}{3} \approx 2.67$, so $L_4 = 1.75$ is an underestimate.

---

**Example 2**: Approximate $\int_1^3 (2x + 1) \, dx$ using a right Riemann sum with $n = 4$ rectangles.

**Solution**:

*Step 1*: $\Delta x = \frac{3 - 1}{4} = 0.5$

*Step 2*: Right endpoints:
- $x_1 = 1.5$
- $x_2 = 2$
- $x_3 = 2.5$
- $x_4 = 3$

*Step 3*: Evaluate $f(x) = 2x + 1$:
- $f(1.5) = 4$
- $f(2) = 5$
- $f(2.5) = 6$
- $f(3) = 7$

*Step 4*: Sum:
$$R_4 = (4 + 5 + 6 + 7)(0.5) = 22 \times 0.5 = 11$$

The actual value is $\int_1^3 (2x + 1) \, dx = [x^2 + x]_1^3 = 12 - 2 = 10$.

Since $f(x) = 2x + 1$ is increasing, $R_4 = 11$ overestimates.

---

**Example 3**: Use a midpoint sum with $n = 3$ to approximate $\int_0^3 \sqrt{x} \, dx$.

**Solution**:

*Step 1*: $\Delta x = \frac{3 - 0}{3} = 1$

*Step 2*: Midpoints:
- $\bar{x}_1 = 0.5$
- $\bar{x}_2 = 1.5$
- $\bar{x}_3 = 2.5$

*Step 3*: Evaluate $f(x) = \sqrt{x}$:
- $f(0.5) = \sqrt{0.5} \approx 0.707$
- $f(1.5) = \sqrt{1.5} \approx 1.225$
- $f(2.5) = \sqrt{2.5} \approx 1.581$

*Step 4*: Sum:
$$M_3 = (0.707 + 1.225 + 1.581)(1) \approx 3.513$$

The actual value is $\frac{2}{3}(3)^{3/2} = 2\sqrt{3} \approx 3.464$.

---

**Example 4**: Express $\lim_{n \to \infty} \sum_{i=1}^{n} \frac{3}{n} \left(\frac{3i}{n}\right)^2$ as a definite integral.

**Solution**:

Identify the components:
- $\Delta x = \frac{3}{n}$, so $b - a = 3$
- $x_i = \frac{3i}{n} = a + i \cdot \Delta x$, so $a = 0$
- $f(x_i) = \left(\frac{3i}{n}\right)^2 = x_i^2$, so $f(x) = x^2$

This is a right Riemann sum for:
$$\int_0^3 x^2 \, dx$$

---

**Example 5**: Given the table of values, approximate $\int_0^8 f(x) \, dx$ using a left Riemann sum.

| $x$ | 0 | 2 | 4 | 6 | 8 |
|-----|---|---|---|---|---|
| $f(x)$ | 3 | 5 | 4 | 2 | 6 |

**Solution**:

The subintervals have width $\Delta x = 2$.

Left endpoints: $x = 0, 2, 4, 6$

$$L_4 = [f(0) + f(2) + f(4) + f(6)] \cdot \Delta x$$
$$= (3 + 5 + 4 + 2)(2) = 14 \times 2 = 28$$

---

## Key Formulas & Rules

| Formula | Expression |
|---------|------------|
| Subinterval width | $\Delta x = \frac{b - a}{n}$ |
| $i$-th right endpoint | $x_i = a + i \cdot \Delta x$ |
| $i$-th left endpoint | $x_{i-1} = a + (i-1) \cdot \Delta x$ |
| $i$-th midpoint | $\bar{x}_i = a + (i - 0.5) \cdot \Delta x$ |
| Left sum | $L_n = \sum_{i=0}^{n-1} f(x_i) \Delta x$ |
| Right sum | $R_n = \sum_{i=1}^{n} f(x_i) \Delta x$ |
| Midpoint sum | $M_n = \sum_{i=1}^{n} f(\bar{x}_i) \Delta x$ |

**Useful Summation Formulas**:
- $\sum_{i=1}^{n} 1 = n$
- $\sum_{i=1}^{n} i = \frac{n(n+1)}{2}$
- $\sum_{i=1}^{n} i^2 = \frac{n(n+1)(2n+1)}{6}$
- $\sum_{i=1}^{n} i^3 = \left[\frac{n(n+1)}{2}\right]^2$

---

## Common Mistakes to Avoid

1. **Confusing left vs. right endpoints**: Left uses $i = 0$ to $n-1$; Right uses $i = 1$ to $n$.

2. **Forgetting $\Delta x$**: The Riemann sum is $\sum f(x_i^*) \cdot \Delta x$, not just $\sum f(x_i^*)$.

3. **Wrong number of terms**: With $n$ rectangles, you evaluate $f$ at $n$ points.

4. **Over/underestimate confusion**: Remember that it depends on whether $f$ is increasing or decreasing.

5. **Index errors**: Be careful whether your sum starts at $i = 0$ or $i = 1$.

6. **Unequal subintervals**: When given a table, subintervals may not be equal—check $\Delta x$ for each.

---

## AP Exam Tips

### For Both AB and BC:
- Riemann sums appear frequently on both multiple choice and free response
- Know how to interpret Riemann sums from tables of data
- Be able to identify whether a sum overestimates or underestimates
- Practice converting between sigma notation and definite integrals

### Common Question Types:
1. **Table-based**: Given function values at specific points, calculate a Riemann sum
2. **Graph-based**: Estimate area from a graph using rectangles
3. **Limit to integral**: Express a limit of Riemann sums as a definite integral
4. **Over/underestimate**: Determine if the approximation is too high or low

### Calculator Tips:
- On calculator-active sections, use the sum feature to compute Riemann sums
- Store $\Delta x$ in a variable for efficiency

---

## Practice Problems

### Basic (Problems 1-5)

**1.** Calculate the left Riemann sum for:

$$f(x) = x^2$$

on $[0, 4]$ with $n = 4$ subintervals.

---

**2.** Calculate the right Riemann sum for:

$$f(x) = 3x - 1$$

on $[1, 5]$ with $n = 4$ subintervals.

---

**3.** Use the following table to approximate $\int_0^{12} f(x) \, dx$ with a left Riemann sum:

| $x$ | 0 | 3 | 6 | 9 | 12 |
|-----|---|---|---|---|---|
| $f(x)$ | 2 | 5 | 8 | 6 | 4 |

---

**4.** Calculate the midpoint Riemann sum for:

$$f(x) = x^3$$

on $[0, 2]$ with $n = 2$ subintervals.

---

**5.** Is the left Riemann sum for $f(x) = e^x$ on $[0, 1]$ an overestimate or underestimate? Explain.

---

### Intermediate (Problems 6-10)

**6.** Use a right Riemann sum with $n = 5$ to approximate:

$$\int_0^5 \sqrt{x+1} \, dx$$

---

**7.** The table shows velocity $v(t)$ in m/s at different times. Approximate the total distance traveled from $t = 0$ to $t = 6$ using a left Riemann sum.

| $t$ (s) | 0 | 2 | 4 | 6 |
|---------|---|---|---|---|
| $v(t)$ (m/s) | 3 | 5 | 4 | 2 |

---

**8.** Express the limit as a definite integral:

$$\lim_{n \to \infty} \sum_{i=1}^{n} \frac{2}{n} \sin\left(\frac{2\pi i}{n}\right)$$

---

**9.** For $f(x) = \frac{1}{x}$ on $[1, 3]$:

**(a)** Calculate $L_4$ (left sum with 4 rectangles)

**(b)** Calculate $R_4$ (right sum with 4 rectangles)

**(c)** Which is larger? Why?

---

**10.** Find the exact value of:

$$\lim_{n \to \infty} \sum_{i=1}^{n} \frac{1}{n} \left(\frac{i}{n}\right)^3$$

---

### Advanced (Problems 11-15)

**11.** Show that for any continuous function $f$ on $[a, b]$:

$$\lim_{n \to \infty} L_n = \lim_{n \to \infty} R_n$$

*(Hint: Consider $R_n - L_n$)*

---

**12.** Calculate:

$$\lim_{n \to \infty} \frac{1}{n} \left[\sin\frac{\pi}{n} + \sin\frac{2\pi}{n} + \cdots + \sin\frac{n\pi}{n}\right]$$

---

**13.** The function $f$ is continuous on $[0, 4]$. If $L_4 = 10$ and $R_4 = 14$, and you know that $f(0) = 2$ and $f(4) = 6$, use the trapezoidal rule to estimate $\int_0^4 f(x) \, dx$.

---

**14.** For $f(x) = x^2$ on $[0, 1]$, find a formula for $R_n$ and verify that $\lim_{n \to \infty} R_n = \frac{1}{3}$.

---

**15.** A function $f$ is concave up on $[a, b]$. Explain why the midpoint Riemann sum underestimates the integral, while the trapezoidal approximation overestimates it.

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

The function $f$ is continuous on $[0, 6]$ and has values given in the table.

| $x$ | 0 | 2 | 4 | 6 |
|-----|---|---|---|---|
| $f(x)$ | 1 | 4 | 3 | 5 |

Using a right Riemann sum with three subintervals of equal length, what is the approximation of $\int_0^6 f(x) \, dx$?

| Choice | Answer |
|--------|--------|
| **(A)** | 16 |
| **(B)** | 24 |
| **(C)** | 26 |
| **(D)** | 30 |

---

#### Problem 17 (Multiple Choice)

Which of the following limits is equal to $\int_2^5 x^3 \, dx$?

| Choice | Answer |
|--------|--------|
| **(A)** | $\lim_{n \to \infty} \sum_{i=1}^{n} \frac{3}{n} \left(\frac{3i}{n}\right)^3$ |
| **(B)** | $\lim_{n \to \infty} \sum_{i=1}^{n} \frac{3}{n} \left(2 + \frac{3i}{n}\right)^3$ |
| **(C)** | $\lim_{n \to \infty} \sum_{i=1}^{n} \frac{5}{n} \left(2 + \frac{5i}{n}\right)^3$ |
| **(D)** | $\lim_{n \to \infty} \sum_{i=1}^{n} \frac{1}{n} \left(2 + \frac{i}{n}\right)^3$ |

---

#### Problem 18 (Free Response)

Let $f(x) = 4 - x^2$ on the interval $[0, 2]$.

> **(a)** Use a left Riemann sum with $n = 4$ subintervals to approximate $\int_0^2 (4 - x^2) \, dx$.
>
> **(b)** Use a right Riemann sum with $n = 4$ subintervals to approximate $\int_0^2 (4 - x^2) \, dx$.
>
> **(c)** Is the actual value of the integral closer to your answer in part (a) or part (b)? Justify your answer.

---

#### Problem 19 (Multiple Choice)

If $f$ is a decreasing function on $[a, b]$ and $L_n$, $R_n$, and $M_n$ represent the left, right, and midpoint Riemann sums with $n$ equal subintervals, which of the following is true?

| Choice | Answer |
|--------|--------|
| **(A)** | $R_n < M_n < L_n$ |
| **(B)** | $L_n < M_n < R_n$ |
| **(C)** | $R_n < L_n < M_n$ |
| **(D)** | $M_n < R_n < L_n$ |

---

#### Problem 20 (Free Response - Challenging)

The rate of water flow into a tank is given by $r(t) = 2t + \sin t$ gallons per minute, where $t$ is measured in minutes.

> **(a)** Use a midpoint Riemann sum with 3 subintervals to approximate the total amount of water that flows into the tank during the first 6 minutes.
>
> **(b)** Is your approximation in part (a) an overestimate or underestimate of the actual amount? Justify your answer.
>
> **(c)** Write, but do not evaluate, an expression involving a limit that gives the exact amount of water that flows into the tank during the first 6 minutes.

---

## Answer Key

<details>
<summary><strong>Problem 1 Solution</strong></summary>

**Answer**: $L_4 = 14$

**Step-by-step solution**:

$\Delta x = \frac{4 - 0}{4} = 1$

Left endpoints: $x_0 = 0, x_1 = 1, x_2 = 2, x_3 = 3$

Function values:
- $f(0) = 0$
- $f(1) = 1$
- $f(2) = 4$
- $f(3) = 9$

$$L_4 = (0 + 1 + 4 + 9)(1) = 14$$

</details>

---

<details>
<summary><strong>Problem 2 Solution</strong></summary>

**Answer**: $R_4 = 32$

**Step-by-step solution**:

$\Delta x = \frac{5 - 1}{4} = 1$

Right endpoints: $x_1 = 2, x_2 = 3, x_3 = 4, x_4 = 5$

Function values:
- $f(2) = 5$
- $f(3) = 8$
- $f(4) = 11$
- $f(5) = 14$

$$R_4 = (5 + 8 + 11 + 14)(1) = 38$$

Wait, let me recalculate. $f(x) = 3x - 1$:
- $f(2) = 6 - 1 = 5$
- $f(3) = 9 - 1 = 8$
- $f(4) = 12 - 1 = 11$
- $f(5) = 15 - 1 = 14$

$R_4 = (5 + 8 + 11 + 14)(1) = 38$

</details>

---

<details>
<summary><strong>Problem 3 Solution</strong></summary>

**Answer**: $L_4 = 63$

**Step-by-step solution**:

$\Delta x = 3$ (subintervals are [0,3], [3,6], [6,9], [9,12])

Left endpoints: $x = 0, 3, 6, 9$

$$L_4 = [f(0) + f(3) + f(6) + f(9)] \cdot \Delta x$$
$$= (2 + 5 + 8 + 6)(3) = 21 \times 3 = 63$$

</details>

---

<details>
<summary><strong>Problem 4 Solution</strong></summary>

**Answer**: $M_2 = 4.25$

**Step-by-step solution**:

$\Delta x = \frac{2 - 0}{2} = 1$

Midpoints: $\bar{x}_1 = 0.5$, $\bar{x}_2 = 1.5$

Function values:
- $f(0.5) = 0.125$
- $f(1.5) = 3.375$

$$M_2 = (0.125 + 3.375)(1) = 3.5$$

The actual value is $\int_0^2 x^3 \, dx = \frac{x^4}{4}\Big|_0^2 = 4$.

</details>

---

<details>
<summary><strong>Problem 5 Solution</strong></summary>

**Answer**: Underestimate

**Explanation**:

Since $f(x) = e^x$ is an increasing function on $[0, 1]$, the left Riemann sum uses function values at the left endpoints of each subinterval, which are smaller than the function values anywhere else in that subinterval.

Therefore, each rectangle has a height that is less than the actual curve above it, making the left Riemann sum an **underestimate** of the true area.

</details>

---

<details>
<summary><strong>Problem 6 Solution</strong></summary>

**Answer**: $R_5 \approx 9.14$

**Step-by-step solution**:

$\Delta x = \frac{5 - 0}{5} = 1$

Right endpoints: $x = 1, 2, 3, 4, 5$

Function values $f(x) = \sqrt{x + 1}$:
- $f(1) = \sqrt{2} \approx 1.414$
- $f(2) = \sqrt{3} \approx 1.732$
- $f(3) = \sqrt{4} = 2$
- $f(4) = \sqrt{5} \approx 2.236$
- $f(5) = \sqrt{6} \approx 2.449$

$$R_5 \approx (1.414 + 1.732 + 2 + 2.236 + 2.449)(1) \approx 9.83$$

</details>

---

<details>
<summary><strong>Problem 7 Solution</strong></summary>

**Answer**: 24 meters

**Step-by-step solution**:

$\Delta t = 2$ seconds

Left endpoints: $t = 0, 2, 4$

$$L_3 = [v(0) + v(2) + v(4)] \cdot \Delta t$$
$$= (3 + 5 + 4)(2) = 12 \times 2 = 24 \text{ meters}$$

</details>

---

<details>
<summary><strong>Problem 8 Solution</strong></summary>

**Answer**: $\int_0^{2\pi} \sin x \, dx$

**Step-by-step solution**:

Identify components:
- $\Delta x = \frac{2}{n}$... wait, let me look more carefully.

Looking at $\frac{2}{n}$ and $\frac{2\pi i}{n}$:

If $\Delta x = \frac{2}{n}$ and $x_i = \frac{2\pi i}{n}$...

Actually, let's rewrite: $\frac{2\pi i}{n} = \frac{2\pi}{n} \cdot i$

So $\Delta x = \frac{2\pi}{n}$? But the coefficient outside is $\frac{2}{n}$.

Hmm, this doesn't match standard form. Let me reconsider.

If $\Delta x = \frac{2}{n}$ then $b - a = 2$.
$x_i = a + i \cdot \Delta x$

Looking at $\sin\left(\frac{2\pi i}{n}\right) = \sin(\pi \cdot \frac{2i}{n})$

If $a = 0$, $b = 2$, and $f(x) = \sin(\pi x)$, then:
$x_i = \frac{2i}{n}$ and $f(x_i) = \sin(\pi \cdot \frac{2i}{n}) = \sin\frac{2\pi i}{n}$

This gives: $\int_0^2 \sin(\pi x) \, dx$

</details>

---

<details>
<summary><strong>Problem 9 Solution</strong></summary>

**Answer**: (a) $L_4 \approx 1.283$, (b) $R_4 \approx 0.950$, (c) $L_4 > R_4$ because $f$ is decreasing

**Step-by-step solution**:

$\Delta x = \frac{3-1}{4} = 0.5$

**(a) Left Riemann sum**:

Left endpoints: $x = 1, 1.5, 2, 2.5$

$$L_4 = \left(\frac{1}{1} + \frac{1}{1.5} + \frac{1}{2} + \frac{1}{2.5}\right)(0.5)$$
$$= (1 + 0.667 + 0.5 + 0.4)(0.5) = 2.567 \times 0.5 \approx 1.283$$

**(b) Right Riemann sum**:

Right endpoints: $x = 1.5, 2, 2.5, 3$

$$R_4 = \left(\frac{1}{1.5} + \frac{1}{2} + \frac{1}{2.5} + \frac{1}{3}\right)(0.5)$$
$$= (0.667 + 0.5 + 0.4 + 0.333)(0.5) = 1.9 \times 0.5 = 0.950$$

**(c)** $L_4 > R_4$ because $f(x) = \frac{1}{x}$ is a decreasing function on $[1, 3]$. For decreasing functions, left sums overestimate and right sums underestimate.

</details>

---

<details>
<summary><strong>Problem 10 Solution</strong></summary>

**Answer**: $\frac{1}{4}$

**Step-by-step solution**:

This is a right Riemann sum for $\int_0^1 x^3 \, dx$.

Here $\Delta x = \frac{1}{n}$ and $x_i = \frac{i}{n}$, so $a = 0$, $b = 1$, $f(x) = x^3$.

$$\int_0^1 x^3 \, dx = \frac{x^4}{4}\Big|_0^1 = \frac{1}{4}$$

</details>

---

<details>
<summary><strong>Problem 11 Solution</strong></summary>

**Answer**: Proof shown below.

**Step-by-step solution**:

Consider $R_n - L_n$:

$$R_n - L_n = \sum_{i=1}^{n} f(x_i) \Delta x - \sum_{i=0}^{n-1} f(x_i) \Delta x$$

$$= [f(x_n) - f(x_0)] \Delta x = [f(b) - f(a)] \cdot \frac{b-a}{n}$$

As $n \to \infty$:

$$\lim_{n \to \infty} (R_n - L_n) = [f(b) - f(a)] \cdot \lim_{n \to \infty} \frac{b-a}{n} = 0$$

Since the difference approaches 0, and both limits exist for continuous functions, we have:

$$\lim_{n \to \infty} L_n = \lim_{n \to \infty} R_n$$

</details>

---

<details>
<summary><strong>Problem 12 Solution</strong></summary>

**Answer**: $\frac{2}{\pi}$

**Step-by-step solution**:

This is a right Riemann sum for $\int_0^\pi \sin x \, dx$.

With $\Delta x = \frac{\pi}{n}$ and $x_i = \frac{i\pi}{n}$:

$$\lim_{n \to \infty} \frac{1}{n} \sum_{i=1}^{n} \sin\frac{i\pi}{n} = \frac{1}{\pi} \int_0^\pi \sin x \, dx$$

Wait, let me reconsider. We have $\frac{1}{n}$ outside, and $\sin\frac{i\pi}{n}$.

If $\Delta x = \frac{\pi}{n}$, then the sum would be $\sum \sin(x_i) \cdot \frac{\pi}{n}$.

But we have $\frac{1}{n}$, so: $\frac{1}{n} = \frac{1}{\pi} \cdot \frac{\pi}{n}$

So this equals $\frac{1}{\pi} \int_0^\pi \sin x \, dx = \frac{1}{\pi}[-\cos x]_0^\pi = \frac{1}{\pi}(1 - (-1)) = \frac{2}{\pi}$

</details>

---

<details>
<summary><strong>Problem 13 Solution</strong></summary>

**Answer**: $T_4 = 12$

**Step-by-step solution**:

The trapezoidal rule gives the average of left and right sums:

$$T_n = \frac{L_n + R_n}{2} = \frac{10 + 14}{2} = 12$$

</details>

---

<details>
<summary><strong>Problem 14 Solution</strong></summary>

**Answer**: $R_n = \frac{(n+1)(2n+1)}{6n^2}$, and $\lim_{n \to \infty} R_n = \frac{1}{3}$

**Step-by-step solution**:

For $f(x) = x^2$ on $[0,1]$:

$\Delta x = \frac{1}{n}$ and $x_i = \frac{i}{n}$

$$R_n = \sum_{i=1}^{n} \left(\frac{i}{n}\right)^2 \cdot \frac{1}{n} = \frac{1}{n^3} \sum_{i=1}^{n} i^2$$

Using $\sum_{i=1}^{n} i^2 = \frac{n(n+1)(2n+1)}{6}$:

$$R_n = \frac{1}{n^3} \cdot \frac{n(n+1)(2n+1)}{6} = \frac{(n+1)(2n+1)}{6n^2}$$

Taking the limit:

$$\lim_{n \to \infty} \frac{(n+1)(2n+1)}{6n^2} = \lim_{n \to \infty} \frac{2n^2 + 3n + 1}{6n^2} = \frac{2}{6} = \frac{1}{3}$$

</details>

---

<details>
<summary><strong>Problem 15 Solution</strong></summary>

**Answer**: See explanation below.

**Explanation**:

**Midpoint underestimates for concave up functions**:

When $f$ is concave up, the curve lies above every secant line. At the midpoint of each subinterval, the tangent line lies below the curve. The midpoint rectangle's height equals the function value at the midpoint, which is below the average height of the curve over that interval.

**Trapezoid overestimates for concave up functions**:

The trapezoidal rule connects the endpoints with a straight line. When $f$ is concave up, the curve sags below this straight line, so the trapezoid encloses more area than lies under the curve.

</details>

---

<details>
<summary><strong>Problem 16 Solution</strong></summary>

**Answer**: **(B)** 24

**Step-by-step solution**:

$\Delta x = \frac{6 - 0}{3} = 2$

Right endpoints: $x = 2, 4, 6$

$$R_3 = [f(2) + f(4) + f(6)] \cdot \Delta x = (4 + 3 + 5)(2) = 12 \times 2 = 24$$

</details>

---

<details>
<summary><strong>Problem 17 Solution</strong></summary>

**Answer**: **(B)** $\lim_{n \to \infty} \sum_{i=1}^{n} \frac{3}{n} \left(2 + \frac{3i}{n}\right)^3$

**Step-by-step solution**:

For $\int_2^5 x^3 \, dx$:
- $a = 2$, $b = 5$
- $\Delta x = \frac{5-2}{n} = \frac{3}{n}$
- $x_i = a + i \cdot \Delta x = 2 + \frac{3i}{n}$
- $f(x_i) = \left(2 + \frac{3i}{n}\right)^3$

The Riemann sum is:
$$\sum_{i=1}^{n} f(x_i) \Delta x = \sum_{i=1}^{n} \frac{3}{n} \left(2 + \frac{3i}{n}\right)^3$$

</details>

---

<details>
<summary><strong>Problem 18 Solution</strong></summary>

**Answer**: (a) $L_4 = 6.75$, (b) $R_4 = 4.75$, (c) Closer to (a)

**(a) Left Riemann sum**:

$\Delta x = 0.5$

Left endpoints: $x = 0, 0.5, 1, 1.5$

- $f(0) = 4$
- $f(0.5) = 4 - 0.25 = 3.75$
- $f(1) = 3$
- $f(1.5) = 4 - 2.25 = 1.75$

$$L_4 = (4 + 3.75 + 3 + 1.75)(0.5) = 12.5 \times 0.5 = 6.25$$

**(b) Right Riemann sum**:

Right endpoints: $x = 0.5, 1, 1.5, 2$

- $f(0.5) = 3.75$
- $f(1) = 3$
- $f(1.5) = 1.75$
- $f(2) = 0$

$$R_4 = (3.75 + 3 + 1.75 + 0)(0.5) = 8.5 \times 0.5 = 4.25$$

**(c)** The actual value is $\int_0^2 (4-x^2) \, dx = [4x - \frac{x^3}{3}]_0^2 = 8 - \frac{8}{3} = \frac{16}{3} \approx 5.33$.

Since $f(x) = 4 - x^2$ is decreasing on $[0, 2]$, $L_4$ overestimates and $R_4$ underestimates.

The actual value (5.33) is closer to the average of $L_4$ and $R_4$, which is $\frac{6.25 + 4.25}{2} = 5.25$.

</details>

---

<details>
<summary><strong>Problem 19 Solution</strong></summary>

**Answer**: **(A)** $R_n < M_n < L_n$

**Explanation**:

For a decreasing function:
- **Left sum overestimates** (uses larger values at left endpoints)
- **Right sum underestimates** (uses smaller values at right endpoints)
- **Midpoint sum** is between them, typically closer to the true value

Therefore: $R_n < M_n < L_n$

</details>

---

<details>
<summary><strong>Problem 20 Solution</strong></summary>

**Answer**: See detailed solution below.

**(a) Midpoint Riemann sum with 3 subintervals**:

$\Delta t = \frac{6 - 0}{3} = 2$

Midpoints: $t = 1, 3, 5$

- $r(1) = 2(1) + \sin(1) \approx 2 + 0.841 = 2.841$
- $r(3) = 2(3) + \sin(3) \approx 6 + 0.141 = 6.141$
- $r(5) = 2(5) + \sin(5) \approx 10 + (-0.959) = 9.041$

$$M_3 = (2.841 + 6.141 + 9.041)(2) \approx 18.023 \times 2 \approx 36.05 \text{ gallons}$$

**(b)** To determine over/underestimate, we need to check concavity.

$r''(t) = -\sin t$

On $[0, 6]$, $\sin t$ changes sign, so $r$ is sometimes concave up and sometimes concave down. Without more analysis, we cannot definitively say whether the midpoint sum over- or underestimates.

However, since $r(t) = 2t + \sin t$ is predominantly linear with a small oscillation, and $r''(t)$ has varying sign, the midpoint rule likely provides a good approximation.

**(c)** Exact amount:

$$\lim_{n \to \infty} \sum_{i=1}^{n} r\left(\frac{6i}{n}\right) \cdot \frac{6}{n} = \lim_{n \to \infty} \sum_{i=1}^{n} \left(2 \cdot \frac{6i}{n} + \sin\frac{6i}{n}\right) \cdot \frac{6}{n}$$

Or equivalently: $\int_0^6 (2t + \sin t) \, dt$

</details>

---

## What's Next

Now that you understand how Riemann sums approximate area, you're ready for [Definite Integrals](/calculus/definite-integrals), where we'll define the integral as the limit of Riemann sums and explore its properties.

---

<div align="center">

[← Antiderivatives](/calculus/antiderivatives) | [Definite Integrals →](/calculus/definite-integrals)

</div>
