# Derivative at a Point

## Learning Objectives

By the end of this article, you will be able to:

- Calculate the derivative at a specific point using the limit definition
- Write the equation of a tangent line at a given point
- Write the equation of a normal line at a given point
- Estimate derivatives from tables of values
- Estimate derivatives from graphs
- Interpret the meaning of $f'(a)$ in context
- Recognize limits that represent derivatives at a point
- Solve AP Calculus problems involving derivatives at specific points

---

## The Core Concept: Zooming In on One Point

### Why Focus on a Single Point?

In the previous article, we learned to find the derivative function $f'(x)$—a formula that gives the slope at any $x$. But many real-world problems ask about a specific moment:

- "What was the velocity at exactly $t = 3$ seconds?"
- "How fast was the population growing in the year 2020?"
- "What's the slope of the tangent line at the point $(2, 5)$?"

These questions require the **derivative at a point**: $f'(a)$ for a specific value $a$.

### The Two Approaches

**Approach 1: Find $f'(x)$ first, then plug in $a$**

1. Compute the general derivative $f'(x)$
2. Substitute $x = a$ to get $f'(a)$

**Approach 2: Use the definition directly at $x = a$**

$$f'(a) = \lim_{h \to 0} \frac{f(a+h) - f(a)}{h}$$

or equivalently:

$$f'(a) = \lim_{x \to a} \frac{f(x) - f(a)}{x - a}$$

Both approaches give the same answer. Use whichever is more convenient for the problem.

---

## Computing $f'(a)$ Using the Definition

### Method 1: The $h$-Form

$$f'(a) = \lim_{h \to 0} \frac{f(a+h) - f(a)}{h}$$

**Example 1:** Find $f'(3)$ for $f(x) = x^2 - 2x$.

**Solution:**

$$f'(3) = \lim_{h \to 0} \frac{f(3+h) - f(3)}{h}$$

**Step 1:** Calculate $f(3)$.
$$f(3) = 9 - 6 = 3$$

**Step 2:** Calculate $f(3+h)$.
$$f(3+h) = (3+h)^2 - 2(3+h) = 9 + 6h + h^2 - 6 - 2h = 3 + 4h + h^2$$

**Step 3:** Form the difference quotient.
$$\frac{f(3+h) - f(3)}{h} = \frac{(3 + 4h + h^2) - 3}{h} = \frac{4h + h^2}{h} = 4 + h$$

**Step 4:** Take the limit.
$$f'(3) = \lim_{h \to 0} (4 + h) = 4$$

**Answer:** $f'(3) = 4$

---

### Method 2: The $x$-Form (Alternative Definition)

$$f'(a) = \lim_{x \to a} \frac{f(x) - f(a)}{x - a}$$

This form is often easier when you can factor $(x - a)$ out of the numerator.

**Example 2:** Find $f'(2)$ for $f(x) = x^3$.

**Solution:**

$$f'(2) = \lim_{x \to 2} \frac{x^3 - 8}{x - 2}$$

**Step 1:** Factor the numerator using the difference of cubes: $a^3 - b^3 = (a-b)(a^2 + ab + b^2)$
$$x^3 - 8 = x^3 - 2^3 = (x - 2)(x^2 + 2x + 4)$$

**Step 2:** Simplify and take the limit.
$$f'(2) = \lim_{x \to 2} \frac{(x-2)(x^2 + 2x + 4)}{x - 2} = \lim_{x \to 2} (x^2 + 2x + 4)$$
$$= 4 + 4 + 4 = 12$$

**Answer:** $f'(2) = 12$

---

### When to Use Which Form?

| Situation | Preferred Form |
|-----------|----------------|
| General computation | $h$-form |
| Numerator factors nicely as $(x - a)(\cdots)$ | $x$-form |
| Given $f(a)$ and need to find $f'(a)$ | Either works |
| Recognizing a limit as a derivative | $x$-form often clearer |

---

## Tangent Lines

### The Equation of a Tangent Line

The **tangent line** to $y = f(x)$ at the point $(a, f(a))$ is the line that:
1. Passes through the point $(a, f(a))$
2. Has slope equal to $f'(a)$

Using point-slope form:

$$\boxed{y - f(a) = f'(a)(x - a)}$$

or in slope-intercept form:

$$y = f'(a)(x - a) + f(a)$$

### Geometric Interpretation

```
       y
       |
       |        tangent line
       |       /
       |      /
       |     / ← slope = f'(a)
       |    •←(a, f(a))
       |   /
       |  / curve y = f(x)
       |_/_________________________ x
            a
```

The tangent line is the best linear approximation to the curve at that point.

---

### Example 3: Finding a Tangent Line

**Find the equation of the tangent line to $f(x) = x^2 + 1$ at $x = 2$.**

**Solution:**

**Step 1:** Find the point of tangency.
$$f(2) = 4 + 1 = 5$$
Point: $(2, 5)$

**Step 2:** Find the slope (derivative at $x = 2$).
$$f'(x) = 2x \implies f'(2) = 4$$

**Step 3:** Write the equation using point-slope form.
$$y - 5 = 4(x - 2)$$
$$y = 4x - 8 + 5$$
$$y = 4x - 3$$

**Answer:** $y = 4x - 3$

---

### Example 4: Tangent Line Using the Definition

**Find the equation of the tangent line to $f(x) = \sqrt{x}$ at $x = 9$.**

**Solution:**

**Step 1:** Find the point.
$$f(9) = \sqrt{9} = 3$$
Point: $(9, 3)$

**Step 2:** Find $f'(9)$ using the definition.

$$f'(9) = \lim_{h \to 0} \frac{\sqrt{9+h} - 3}{h}$$

Rationalize:
$$= \lim_{h \to 0} \frac{\sqrt{9+h} - 3}{h} \cdot \frac{\sqrt{9+h} + 3}{\sqrt{9+h} + 3} = \lim_{h \to 0} \frac{(9+h) - 9}{h(\sqrt{9+h} + 3)}$$

$$= \lim_{h \to 0} \frac{h}{h(\sqrt{9+h} + 3)} = \lim_{h \to 0} \frac{1}{\sqrt{9+h} + 3} = \frac{1}{3 + 3} = \frac{1}{6}$$

**Step 3:** Write the equation.
$$y - 3 = \frac{1}{6}(x - 9)$$
$$y = \frac{1}{6}x - \frac{3}{2} + 3 = \frac{1}{6}x + \frac{3}{2}$$

**Answer:** $y = \frac{1}{6}x + \frac{3}{2}$

---

### Example 5: Horizontal Tangent Lines

**Find all points where $f(x) = x^3 - 3x$ has a horizontal tangent line.**

**Solution:**

A horizontal tangent has slope = 0, so we need $f'(x) = 0$.

**Step 1:** Find $f'(x)$.
$$f'(x) = 3x^2 - 3$$

**Step 2:** Set $f'(x) = 0$ and solve.
$$3x^2 - 3 = 0$$
$$x^2 = 1$$
$$x = \pm 1$$

**Step 3:** Find the corresponding $y$-values.
$$f(1) = 1 - 3 = -2 \implies (1, -2)$$
$$f(-1) = -1 + 3 = 2 \implies (-1, 2)$$

**Answer:** Horizontal tangents at $(1, -2)$ and $(-1, 2)$.

---

## Normal Lines

### What is a Normal Line?

The **normal line** to a curve at a point is the line that is **perpendicular** to the tangent line at that point.

If two lines are perpendicular, their slopes are **negative reciprocals**:
$$m_{\text{tangent}} \cdot m_{\text{normal}} = -1$$

So if the tangent slope is $f'(a)$, the normal slope is:
$$m_{\text{normal}} = -\frac{1}{f'(a)}$$

(provided $f'(a) \neq 0$)

### Special Cases

| Tangent Slope | Normal Slope |
|---------------|--------------|
| $f'(a) = m$ (nonzero) | $-\frac{1}{m}$ |
| $f'(a) = 0$ (horizontal tangent) | Undefined (vertical normal) |
| $f'(a)$ undefined (vertical tangent) | $0$ (horizontal normal) |

---

### Example 6: Finding a Normal Line

**Find the equation of the normal line to $f(x) = x^2$ at $x = 3$.**

**Solution:**

**Step 1:** Find the point.
$$f(3) = 9$$
Point: $(3, 9)$

**Step 2:** Find the tangent slope.
$$f'(x) = 2x \implies f'(3) = 6$$

**Step 3:** Find the normal slope.
$$m_{\text{normal}} = -\frac{1}{6}$$

**Step 4:** Write the equation.
$$y - 9 = -\frac{1}{6}(x - 3)$$
$$y = -\frac{1}{6}x + \frac{1}{2} + 9 = -\frac{1}{6}x + \frac{19}{2}$$

**Answer:** $y = -\frac{1}{6}x + \frac{19}{2}$

---

### Example 7: Both Tangent and Normal Lines

**For $f(x) = \frac{1}{x}$ at $x = 2$, find both the tangent and normal line equations.**

**Solution:**

**Point:** $f(2) = \frac{1}{2}$, so $(2, \frac{1}{2})$

**Tangent slope:** $f'(x) = -\frac{1}{x^2} \implies f'(2) = -\frac{1}{4}$

**Tangent line:**
$$y - \frac{1}{2} = -\frac{1}{4}(x - 2)$$
$$y = -\frac{1}{4}x + \frac{1}{2} + \frac{1}{2} = -\frac{1}{4}x + 1$$

**Normal slope:** $m = -\frac{1}{(-1/4)} = 4$

**Normal line:**
$$y - \frac{1}{2} = 4(x - 2)$$
$$y = 4x - 8 + \frac{1}{2} = 4x - \frac{15}{2}$$

**Answers:**
- Tangent: $y = -\frac{1}{4}x + 1$
- Normal: $y = 4x - \frac{15}{2}$

---

## Estimating Derivatives from Tables

### The Difference Quotient Approximation

When you don't have a formula for $f(x)$ but have data points, you can **estimate** the derivative using:

$$f'(a) \approx \frac{f(a + h) - f(a)}{h}$$

for small $h$.

### Better Estimates: The Symmetric Difference Quotient

A more accurate estimate uses points on both sides:

$$f'(a) \approx \frac{f(a + h) - f(a - h)}{2h}$$

This is called the **central difference** or **symmetric difference quotient**.

```
Using both sides:          Using one side:

    •───────────•           •───────────•
  f(a-h)       f(a+h)      f(a)       f(a+h)
        \     /                  \
         \   /                    \
          \ /                      \
           • f(a)                   (less accurate)

  Symmetric (better)        One-sided
```

---

### Example 8: Estimating from a Table

**The table shows values of a differentiable function $f$. Estimate $f'(3)$.**

| $x$ | 1 | 2 | 3 | 4 | 5 |
|-----|---|---|---|---|---|
| $f(x)$ | 2 | 5 | 9 | 14 | 20 |

**Solution:**

**Method 1: Forward difference** (using $x = 3$ and $x = 4$)
$$f'(3) \approx \frac{f(4) - f(3)}{4 - 3} = \frac{14 - 9}{1} = 5$$

**Method 2: Backward difference** (using $x = 2$ and $x = 3$)
$$f'(3) \approx \frac{f(3) - f(2)}{3 - 2} = \frac{9 - 5}{1} = 4$$

**Method 3: Symmetric difference** (using $x = 2$ and $x = 4$)
$$f'(3) \approx \frac{f(4) - f(2)}{4 - 2} = \frac{14 - 5}{2} = \frac{9}{2} = 4.5$$

**Best estimate:** $f'(3) \approx 4.5$ (symmetric difference is most accurate)

---

### Example 9: Real-World Table Data

**The table shows the temperature $T$ (in °F) of a cup of coffee at time $t$ (in minutes). Estimate how fast the coffee is cooling at $t = 5$ minutes.**

| $t$ | 0 | 2 | 5 | 8 | 12 |
|-----|---|---|---|---|---|
| $T(t)$ | 180 | 165 | 145 | 130 | 115 |

**Solution:**

Using symmetric difference with $t = 2$ and $t = 8$:
$$T'(5) \approx \frac{T(8) - T(2)}{8 - 2} = \frac{130 - 165}{6} = \frac{-35}{6} \approx -5.83$$

**Answer:** The coffee is cooling at approximately $5.83$ °F per minute at $t = 5$.

(The negative sign indicates the temperature is decreasing.)

---

## Estimating Derivatives from Graphs

### Reading the Slope Visually

To estimate $f'(a)$ from a graph:

1. Draw (or imagine) the tangent line at $x = a$
2. Pick two clear points on that tangent line
3. Calculate the slope: $\frac{\text{rise}}{\text{run}}$

### Tips for Accuracy

- Use points that are far apart for better precision
- Choose points that land on grid intersections
- Remember: slope = $\frac{\Delta y}{\Delta x}$

---

### Example 10: Estimating from a Graph

```
     y
   6 |           •
   5 |         /
   4 |       •/
   3 |      /
   2 |    •/
   1 |   /
   0 |__•_________________ x
       0  1  2  3  4  5
```

**Estimate $f'(2)$.**

**Solution:**

The tangent line at $x = 2$ appears to pass through approximately:
- $(1, 2)$ and $(3, 4)$

Slope: $\frac{4 - 2}{3 - 1} = \frac{2}{2} = 1$

**Answer:** $f'(2) \approx 1$

---

### Example 11: Identifying Where $f'(x) = 0$

**From the graph below, identify all $x$-values where $f'(x) = 0$.**

```
     y
     |     •
     |    / \
     |   /   \      •
     |  /     \    / \
     | •       \  /   \
     |          \/     \
     |          •       •
     |_________________________ x
        1  2  3  4  5  6  7
```

**Solution:**

$f'(x) = 0$ where the tangent line is horizontal—at local maxima and minima.

From the graph:
- Local maximum near $x = 2$
- Local minimum near $x = 4$
- Local maximum near $x = 6$

**Answer:** $f'(x) = 0$ at approximately $x = 2$, $x = 4$, and $x = 6$.

---

### Example 12: Sign of the Derivative from a Graph

**Based on the graph, determine where $f'(x) > 0$, $f'(x) < 0$, and $f'(x) = 0$.**

```
     y
     |
   4 |      /\
   3 |     /  \
   2 |    /    \
   1 |   /      \____
   0 |__/____________\____ x
      -1  0  1  2  3  4  5
```

**Solution:**

- **$f'(x) > 0$** (function increasing): $x < 2$ approximately
- **$f'(x) = 0$** (horizontal tangent): $x = 2$ and $x \in [3, 4]$ (flat section)
- **$f'(x) < 0$** (function decreasing): $2 < x < 3$ and $x > 4$

---

## Recognizing Limits as Derivatives

### A Key AP Skill

Many AP problems present a limit and ask you to recognize it as a derivative. This tests your understanding of the definition.

**Pattern 1:** $\lim_{h \to 0} \frac{f(a+h) - f(a)}{h}$ represents $f'(a)$

**Pattern 2:** $\lim_{x \to a} \frac{f(x) - f(a)}{x - a}$ represents $f'(a)$

---

### Example 13: Identifying the Function and Point

**The limit $\lim_{h \to 0} \frac{(3+h)^4 - 81}{h}$ represents $f'(a)$ for some function $f$ and value $a$. Find $f$ and $a$.**

**Solution:**

Compare to $\lim_{h \to 0} \frac{f(a+h) - f(a)}{h}$:

- The expression $(3+h)^4$ suggests $f(x) = x^4$ and $a = 3$
- Note that $f(3) = 3^4 = 81$ ✓

**Answer:** $f(x) = x^4$, $a = 3$

To evaluate: $f'(x) = 4x^3$, so $f'(3) = 4(27) = 108$.

---

### Example 14: The $x$-Form Recognition

**Evaluate $\lim_{x \to 4} \frac{2^x - 16}{x - 4}$.**

**Solution:**

This has the form $\lim_{x \to a} \frac{f(x) - f(a)}{x - a}$ where:
- $f(x) = 2^x$
- $a = 4$
- $f(4) = 2^4 = 16$ ✓

So this limit equals $f'(4)$ where $f(x) = 2^x$.

The derivative of $2^x$ is $2^x \ln 2$ (we'll derive this later).

**Answer:** $\lim_{x \to 4} \frac{2^x - 16}{x - 4} = 2^4 \ln 2 = 16 \ln 2$

---

### Example 15: Trickier Recognition

**What does $\lim_{h \to 0} \frac{\sin\left(\frac{\pi}{6} + h\right) - \frac{1}{2}}{h}$ represent?**

**Solution:**

Compare to $\lim_{h \to 0} \frac{f(a+h) - f(a)}{h}$:

- $f(x) = \sin x$
- $a = \frac{\pi}{6}$
- $f\left(\frac{\pi}{6}\right) = \sin\left(\frac{\pi}{6}\right) = \frac{1}{2}$ ✓

This is $f'(\frac{\pi}{6})$ where $f(x) = \sin x$.

Since $(\sin x)' = \cos x$:
$$f'\left(\frac{\pi}{6}\right) = \cos\left(\frac{\pi}{6}\right) = \frac{\sqrt{3}}{2}$$

**Answer:** The limit represents $\frac{d}{dx}[\sin x]$ at $x = \frac{\pi}{6}$, which equals $\frac{\sqrt{3}}{2}$.

---

## Worked Examples: Comprehensive Practice

### Example 16: Complete Tangent Line Problem

**A particle moves along a curve given by $y = \frac{x^2}{x+1}$. Find the equation of the tangent line at the point where $x = 1$.**

**Solution:**

**Step 1:** Find the point.
$$y = \frac{1^2}{1+1} = \frac{1}{2}$$
Point: $\left(1, \frac{1}{2}\right)$

**Step 2:** Find $f'(1)$ using the definition.

$$f'(1) = \lim_{h \to 0} \frac{f(1+h) - f(1)}{h}$$

$$f(1+h) = \frac{(1+h)^2}{(1+h)+1} = \frac{1 + 2h + h^2}{2 + h}$$

$$f(1+h) - f(1) = \frac{1 + 2h + h^2}{2 + h} - \frac{1}{2}$$

Find common denominator:
$$= \frac{2(1 + 2h + h^2) - (2 + h)}{2(2 + h)} = \frac{2 + 4h + 2h^2 - 2 - h}{2(2+h)} = \frac{3h + 2h^2}{2(2+h)}$$

$$\frac{f(1+h) - f(1)}{h} = \frac{3h + 2h^2}{2h(2+h)} = \frac{h(3 + 2h)}{2h(2+h)} = \frac{3 + 2h}{2(2+h)}$$

$$f'(1) = \lim_{h \to 0} \frac{3 + 2h}{2(2+h)} = \frac{3}{4}$$

**Step 3:** Write the tangent line.
$$y - \frac{1}{2} = \frac{3}{4}(x - 1)$$
$$y = \frac{3}{4}x - \frac{3}{4} + \frac{1}{2} = \frac{3}{4}x - \frac{1}{4}$$

**Answer:** $y = \frac{3}{4}x - \frac{1}{4}$

---

### Example 17: Finding Points with Given Tangent Slope

**Find all points on the curve $y = x^3 - 3x^2$ where the tangent line has slope 9.**

**Solution:**

**Step 1:** Find $y'$.
$$y' = 3x^2 - 6x$$

**Step 2:** Set $y' = 9$ and solve.
$$3x^2 - 6x = 9$$
$$x^2 - 2x - 3 = 0$$
$$(x - 3)(x + 1) = 0$$
$$x = 3 \text{ or } x = -1$$

**Step 3:** Find the $y$-coordinates.
- $x = 3$: $y = 27 - 27 = 0$
- $x = -1$: $y = -1 - 3 = -4$

**Answer:** The tangent has slope 9 at points $(3, 0)$ and $(-1, -4)$.

---

### Example 18: Tangent Line Through an External Point

**Find the equations of all lines through the point $(0, -4)$ that are tangent to the parabola $y = x^2$.**

**Solution:**

Let the point of tangency be $(a, a^2)$ on the parabola.

**Step 1:** The tangent slope at $x = a$ is $f'(a) = 2a$.

**Step 2:** The tangent line at $(a, a^2)$ with slope $2a$ is:
$$y - a^2 = 2a(x - a)$$
$$y = 2ax - a^2$$

**Step 3:** This line must pass through $(0, -4)$:
$$-4 = 2a(0) - a^2$$
$$-4 = -a^2$$
$$a^2 = 4$$
$$a = \pm 2$$

**Step 4:** Find the tangent lines.
- $a = 2$: $y = 4x - 4$
- $a = -2$: $y = -4x - 4$

**Answer:** $y = 4x - 4$ and $y = -4x - 4$

---

## Practice Problems

### Basic Problems (1-5)

**1.** Use the definition to find $f'(4)$ for $f(x) = 3x - 7$.

---

**2.** Use the definition to find $f'(-1)$ for $f(x) = x^2 + 5x$.

---

**3.** Find the equation of the tangent line to $f(x) = x^2 - 4x$ at $x = 3$.

---

**4.** Find the equation of the normal line to $f(x) = \sqrt{x}$ at $x = 4$.

---

**5.** The table shows values of $g(x)$. Estimate $g'(2)$.

| $x$ | 0 | 1 | 2 | 3 | 4 |
|-----|---|---|---|---|---|
| $g(x)$ | 3 | 5 | 8 | 12 | 17 |

---

### Intermediate Problems (6-10)

**6.** Use the definition to find $f'(1)$ for $f(x) = \frac{2}{x}$.

---

**7.** Find all points on $y = x^3 - 12x$ where the tangent line is horizontal.

---

**8.** Find the equation of the tangent line to $f(x) = \frac{1}{x+1}$ at $x = 0$.

---

**9.** The limit $\lim_{h \to 0} \frac{\sqrt{9+h} - 3}{h}$ represents $f'(a)$ for some function and point. Identify $f(x)$ and $a$, then evaluate the limit.

---

**10.** From the graph, estimate $f'(1)$, $f'(3)$, and identify where $f'(x) = 0$.

```
     y
   4 |    /\
   3 |   /  \
   2 |  /    \___
   1 | /         \
   0 |/___________\____ x
     0  1  2  3  4  5
```

---

### Advanced Problems (11-15)

**11.** Find the equations of both the tangent and normal lines to $y = x^3$ at $x = -1$.

---

**12.** Find all points on $y = x^2 - 2x + 3$ where the tangent line passes through the origin.

---

**13.** The position of a particle is $s(t) = t^3 - 6t^2 + 9t$. Find:
(a) The velocity at $t = 2$
(b) The times when the particle is at rest

---

**14.** Find the value of $c$ such that the line $y = 2x + c$ is tangent to the parabola $y = x^2$.

---

**15.** Evaluate $\lim_{x \to \pi/4} \frac{\tan x - 1}{x - \pi/4}$ by recognizing it as a derivative.

---

### Challenge Problems (16-18)

**16.** Find all lines through $(1, 3)$ that are tangent to $y = x^2 + 1$.

---

**17.** The curves $y = x^2$ and $y = -x^2 + 4x - 2$ intersect at a point. Find the acute angle between their tangent lines at this intersection.

---

**18.** Let $f(x) = x^2 \sin\left(\frac{1}{x}\right)$ for $x \neq 0$ and $f(0) = 0$. Use the definition to find $f'(0)$, then determine if $f'(x)$ is continuous at $x = 0$.

---

## Solutions to Practice Problems

### Solution 1

$$f'(4) = \lim_{h \to 0} \frac{[3(4+h) - 7] - [3(4) - 7]}{h} = \lim_{h \to 0} \frac{12 + 3h - 7 - 12 + 7}{h}$$

$$= \lim_{h \to 0} \frac{3h}{h} = 3$$

**Answer:** $f'(4) = 3$

---

### Solution 2

$$f'(-1) = \lim_{h \to 0} \frac{[(-1+h)^2 + 5(-1+h)] - [1 - 5]}{h}$$

$$= \lim_{h \to 0} \frac{1 - 2h + h^2 - 5 + 5h - (-4)}{h} = \lim_{h \to 0} \frac{1 - 2h + h^2 - 5 + 5h + 4}{h}$$

$$= \lim_{h \to 0} \frac{3h + h^2}{h} = \lim_{h \to 0} (3 + h) = 3$$

**Answer:** $f'(-1) = 3$

---

### Solution 3

Point: $f(3) = 9 - 12 = -3$, so $(3, -3)$

Slope: $f'(x) = 2x - 4$, so $f'(3) = 2$

Tangent line: $y - (-3) = 2(x - 3)$
$$y = 2x - 9$$

**Answer:** $y = 2x - 9$

---

### Solution 4

Point: $(4, 2)$

Tangent slope: $f'(x) = \frac{1}{2\sqrt{x}}$, so $f'(4) = \frac{1}{4}$

Normal slope: $-\frac{1}{1/4} = -4$

Normal line: $y - 2 = -4(x - 4)$
$$y = -4x + 18$$

**Answer:** $y = -4x + 18$

---

### Solution 5

Using symmetric difference:
$$g'(2) \approx \frac{g(3) - g(1)}{3 - 1} = \frac{12 - 5}{2} = \frac{7}{2} = 3.5$$

**Answer:** $g'(2) \approx 3.5$

---

### Solution 6

$$f'(1) = \lim_{h \to 0} \frac{\frac{2}{1+h} - 2}{h} = \lim_{h \to 0} \frac{\frac{2 - 2(1+h)}{1+h}}{h}$$

$$= \lim_{h \to 0} \frac{2 - 2 - 2h}{h(1+h)} = \lim_{h \to 0} \frac{-2h}{h(1+h)} = \lim_{h \to 0} \frac{-2}{1+h} = -2$$

**Answer:** $f'(1) = -2$

---

### Solution 7

$y' = 3x^2 - 12$

Set $y' = 0$: $3x^2 - 12 = 0 \Rightarrow x^2 = 4 \Rightarrow x = \pm 2$

Points:
- $x = 2$: $y = 8 - 24 = -16$
- $x = -2$: $y = -8 + 24 = 16$

**Answer:** $(2, -16)$ and $(-2, 16)$

---

### Solution 8

Point: $f(0) = 1$, so $(0, 1)$

Using the definition:
$$f'(0) = \lim_{h \to 0} \frac{\frac{1}{h+1} - 1}{h} = \lim_{h \to 0} \frac{1 - (h+1)}{h(h+1)} = \lim_{h \to 0} \frac{-h}{h(h+1)} = \lim_{h \to 0} \frac{-1}{h+1} = -1$$

Tangent: $y - 1 = -1(x - 0)$
$$y = -x + 1$$

**Answer:** $y = -x + 1$

---

### Solution 9

This is $f'(a)$ where $f(x) = \sqrt{x}$ and $a = 9$ (since $\sqrt{9} = 3$).

$$f'(x) = \frac{1}{2\sqrt{x}} \implies f'(9) = \frac{1}{2\sqrt{9}} = \frac{1}{6}$$

**Answer:** $f(x) = \sqrt{x}$, $a = 9$, limit $= \frac{1}{6}$

---

### Solution 10

From the graph:
- At $x = 1$: The curve is rising steeply. Estimate $f'(1) \approx 2$
- At $x = 3$: The curve is flat. $f'(3) \approx 0$
- $f'(x) = 0$ at approximately $x = 2$ (peak) and $x = 3$ to $x = 4$ (flat section)

**Answer:** $f'(1) \approx 2$, $f'(3) \approx 0$, $f'(x) = 0$ at $x \approx 2$ and on $[3, 4]$

---

### Solution 11

Point: $(-1, -1)$

$y' = 3x^2$, so $y'(-1) = 3$

Tangent: $y - (-1) = 3(x - (-1))$
$$y = 3x + 2$$

Normal slope: $-\frac{1}{3}$

Normal: $y + 1 = -\frac{1}{3}(x + 1)$
$$y = -\frac{1}{3}x - \frac{4}{3}$$

**Answer:** Tangent: $y = 3x + 2$; Normal: $y = -\frac{1}{3}x - \frac{4}{3}$

---

### Solution 12

Let the point of tangency be $(a, a^2 - 2a + 3)$.

Slope at $x = a$: $f'(a) = 2a - 2$

The tangent line through $(a, a^2 - 2a + 3)$ with slope $2a - 2$:
$$y - (a^2 - 2a + 3) = (2a - 2)(x - a)$$

For this to pass through $(0, 0)$:
$$0 - (a^2 - 2a + 3) = (2a - 2)(0 - a)$$
$$-(a^2 - 2a + 3) = -a(2a - 2)$$
$$-a^2 + 2a - 3 = -2a^2 + 2a$$
$$a^2 = 3$$
$$a = \pm\sqrt{3}$$

Points:
- $a = \sqrt{3}$: $y = 3 - 2\sqrt{3} + 3 = 6 - 2\sqrt{3}$
- $a = -\sqrt{3}$: $y = 3 + 2\sqrt{3} + 3 = 6 + 2\sqrt{3}$

**Answer:** $(\sqrt{3}, 6 - 2\sqrt{3})$ and $(-\sqrt{3}, 6 + 2\sqrt{3})$

---

### Solution 13

$s(t) = t^3 - 6t^2 + 9t$

$v(t) = s'(t) = 3t^2 - 12t + 9$

**(a)** $v(2) = 12 - 24 + 9 = -3$

**(b)** Particle at rest when $v(t) = 0$:
$$3t^2 - 12t + 9 = 0$$
$$t^2 - 4t + 3 = 0$$
$$(t - 1)(t - 3) = 0$$
$$t = 1 \text{ or } t = 3$$

**Answer:** (a) $v(2) = -3$ units/time; (b) At rest at $t = 1$ and $t = 3$

---

### Solution 14

For $y = 2x + c$ to be tangent to $y = x^2$:

At the point of tangency, $x^2 = 2x + c$ AND the slopes match.

Slope of parabola: $y' = 2x$. Slope of line: $2$.

So $2x = 2 \Rightarrow x = 1$.

At $x = 1$: $y = 1$ on parabola.

For the line to pass through $(1, 1)$: $1 = 2(1) + c \Rightarrow c = -1$

**Answer:** $c = -1$

---

### Solution 15

This has form $\lim_{x \to a} \frac{f(x) - f(a)}{x - a}$ where $f(x) = \tan x$ and $a = \frac{\pi}{4}$.

Note: $\tan\left(\frac{\pi}{4}\right) = 1$ ✓

$f'(x) = \sec^2 x$

$$f'\left(\frac{\pi}{4}\right) = \sec^2\left(\frac{\pi}{4}\right) = \left(\frac{1}{\cos(\pi/4)}\right)^2 = \left(\frac{1}{1/\sqrt{2}}\right)^2 = (\sqrt{2})^2 = 2$$

**Answer:** $2$

---

### Solution 16

Let point of tangency be $(a, a^2 + 1)$.

Slope: $f'(a) = 2a$

Tangent line: $y - (a^2 + 1) = 2a(x - a)$

Must pass through $(1, 3)$:
$$3 - (a^2 + 1) = 2a(1 - a)$$
$$2 - a^2 = 2a - 2a^2$$
$$2 - a^2 = 2a - 2a^2$$
$$a^2 - 2a + 2 = 0$$

Discriminant: $4 - 8 = -4 < 0$. No real solutions.

**Answer:** There are no lines through $(1, 3)$ tangent to $y = x^2 + 1$.

(The point $(1, 3)$ is inside the parabola, so no tangent lines from it exist.)

---

### Solution 17

Find intersection: $x^2 = -x^2 + 4x - 2$
$$2x^2 - 4x + 2 = 0$$
$$x^2 - 2x + 1 = 0$$
$$(x - 1)^2 = 0$$
$$x = 1$$

At $x = 1$: $y = 1$. Point: $(1, 1)$

Slopes at $(1, 1)$:
- Curve 1: $y' = 2x \Rightarrow m_1 = 2$
- Curve 2: $y' = -2x + 4 \Rightarrow m_2 = 2$

Both slopes equal 2, so the curves are tangent (touch but don't cross).

**Answer:** The angle is $0°$ (the curves are tangent to each other).

---

### Solution 18

**Finding $f'(0)$:**
$$f'(0) = \lim_{h \to 0} \frac{h^2 \sin(1/h) - 0}{h} = \lim_{h \to 0} h \sin\left(\frac{1}{h}\right)$$

Since $|h \sin(1/h)| \leq |h| \to 0$, by squeeze theorem: $f'(0) = 0$

**Is $f'(x)$ continuous at 0?**

For $x \neq 0$, using product rule:
$$f'(x) = 2x \sin\left(\frac{1}{x}\right) + x^2 \cdot \cos\left(\frac{1}{x}\right) \cdot \left(-\frac{1}{x^2}\right)$$
$$= 2x \sin\left(\frac{1}{x}\right) - \cos\left(\frac{1}{x}\right)$$

As $x \to 0$:
- $2x \sin(1/x) \to 0$ (squeeze theorem)
- $\cos(1/x)$ oscillates between $-1$ and $1$, so $-\cos(1/x)$ oscillates

Thus $\lim_{x \to 0} f'(x)$ does not exist.

**Answer:** $f'(0) = 0$, but $f'(x)$ is NOT continuous at $x = 0$.

---

## AP Exam Tips

### Quick Recognition Patterns

When you see a limit like:
$$\lim_{h \to 0} \frac{f(a+h) - f(a)}{h} \text{ or } \lim_{x \to a} \frac{f(x) - f(a)}{x - a}$$

Immediately recognize it as $f'(a)$.

**Common disguises:**
- $\lim_{h \to 0} \frac{(2+h)^5 - 32}{h} = f'(2)$ where $f(x) = x^5$
- $\lim_{x \to 1} \frac{\ln x}{x - 1} = f'(1)$ where $f(x) = \ln x$

### Tangent Line Checklist

1. Find the point: $(a, f(a))$
2. Find the slope: $m = f'(a)$
3. Use point-slope form: $y - f(a) = f'(a)(x - a)$

### Common Mistakes

**Mistake 1:** Forgetting the point when writing the tangent line.

Wrong: "The tangent has slope 4" (incomplete)
Right: "The tangent at $(2, 3)$ is $y - 3 = 4(x - 2)$"

**Mistake 2:** Confusing tangent and normal slopes.

Remember: Normal slope = $-\frac{1}{\text{tangent slope}}$ (negative reciprocal)

**Mistake 3:** Not checking that estimated derivatives make sense.

If the function is increasing, $f'$ should be positive. If decreasing, negative.

---

## Summary

**Derivative at a Point:**
$$f'(a) = \lim_{h \to 0} \frac{f(a+h) - f(a)}{h} = \lim_{x \to a} \frac{f(x) - f(a)}{x - a}$$

**Tangent Line** at $(a, f(a))$:
$$y - f(a) = f'(a)(x - a)$$

**Normal Line** at $(a, f(a))$:
$$y - f(a) = -\frac{1}{f'(a)}(x - a) \quad \text{(when } f'(a) \neq 0\text{)}$$

**Estimating from Tables:**
- Forward/backward difference: $\frac{f(a+h) - f(a)}{h}$ or $\frac{f(a) - f(a-h)}{h}$
- Symmetric difference (better): $\frac{f(a+h) - f(a-h)}{2h}$

**Estimating from Graphs:**
- Draw the tangent line mentally
- Pick two points and calculate slope

**Key Skills:**
- Recognize limits that represent derivatives
- Find tangent/normal lines efficiently
- Estimate derivatives from data
- Interpret derivatives in context

---

<div align="center">

[← Derivative Definition](calculus/derivative-definition.md) | [Tangent Lines →](calculus/tangent-lines.md)

</div>
