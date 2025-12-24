# Transformations of Functions
<p class="article-date">July 2, 2024</p>

## Prerequisites
Before diving in, make sure you're comfortable with:
- [Domain and Range](/calculus/0101-domain-and-range)
- Basic function notation
- Graphing common parent functions

## Learning Objectives
By the end of this section, you will be able to:
- Identify the six basic transformations (shifts, stretches, reflections)
- Apply transformations in the correct order
- Write equations from transformed graphs
- Sketch transformed functions without a calculator
- Combine multiple transformations

## The Big Picture: Building Functions from Simple Pieces

Instead of memorizing countless function shapes, we can start with simple **parent functions** and transform them:

| Parent Function | Basic Shape |
|-----------------|-------------|
| $f(x) = x$ | Line through origin |
| $f(x) = x^2$ | U-shaped parabola |
| $f(x) = x^3$ | S-shaped cubic |
| $f(x) = \|x\|$ | V-shape |
| $f(x) = \sqrt{x}$ | Half parabola on side |
| $f(x) = \frac{1}{x}$ | Hyperbola |
| $f(x) = e^x$ | Exponential growth |
| $f(x) = \ln(x)$ | Logarithmic curve |
| $f(x) = \sin(x)$ | Wave |

**Every other function** in these families is just a transformation of the parent!

## The Six Basic Transformations

### Overview Table

| Transformation | Equation Form | Effect |
|----------------|---------------|--------|
| Vertical shift up $k$ | $f(x) + k$ | Moves graph UP $k$ units |
| Vertical shift down $k$ | $f(x) - k$ | Moves graph DOWN $k$ units |
| Horizontal shift right $h$ | $f(x - h)$ | Moves graph RIGHT $h$ units |
| Horizontal shift left $h$ | $f(x + h)$ | Moves graph LEFT $h$ units |
| Vertical stretch by $a$ | $a \cdot f(x)$ | Stretches vertically (if $a > 1$) |
| Vertical compression by $a$ | $a \cdot f(x)$ | Compresses vertically (if $0 < a < 1$) |
| Horizontal stretch by $b$ | $f(bx)$ | Compresses horizontally (if $b > 1$) |
| Horizontal compression | $f(bx)$ | Stretches horizontally (if $0 < b < 1$) |
| Reflection over x-axis | $-f(x)$ | Flips upside down |
| Reflection over y-axis | $f(-x)$ | Flips left-right |

> **Key Insight**: Horizontal transformations work "backwards" from what you might expect!

## Vertical Shifts: Adding/Subtracting Outside

$$y = f(x) + k$$

- **$k > 0$**: Shift UP by $k$ units
- **$k < 0$**: Shift DOWN by $|k|$ units

### Why It Works
Adding $k$ to every output value raises every point by $k$.

### Example
$y = x^2 + 3$ shifts the parabola UP 3 units.
- Original vertex: $(0, 0)$
- New vertex: $(0, 3)$

## Horizontal Shifts: Adding/Subtracting Inside

$$y = f(x - h)$$

- **$h > 0$**: Shift RIGHT by $h$ units
- **$h < 0$**: Shift LEFT by $|h|$ units

### Why It Works "Backwards"
To get the same $y$-value that $f$ originally gave at $x = 0$, you now need to input $x = h$. So the point moves from $x = 0$ to $x = h$ (rightward if $h > 0$).

### Example
$y = (x - 4)^2$ shifts the parabola RIGHT 4 units.
- Original vertex: $(0, 0)$
- New vertex: $(4, 0)$

> **Memory Trick**: "Minus means right, plus means left" (opposite of vertical!)

## Vertical Stretch/Compression: Multiplying Outside

$$y = a \cdot f(x)$$

- **$|a| > 1$**: Vertical STRETCH (taller)
- **$0 < |a| < 1$**: Vertical COMPRESSION (shorter)
- **$a < 0$**: Also reflects over x-axis

### Example
$y = 3x^2$ stretches the parabola vertically by factor of 3.
- Point $(1, 1)$ becomes $(1, 3)$
- Point $(2, 4)$ becomes $(2, 12)$

## Horizontal Stretch/Compression: Multiplying Inside

$$y = f(bx)$$

- **$|b| > 1$**: Horizontal COMPRESSION (narrower)
- **$0 < |b| < 1$**: Horizontal STRETCH (wider)
- **$b < 0$**: Also reflects over y-axis

### Why It Works "Backwards"
If $b = 2$, then to reach the same $y$-value, you only need half the $x$-value. The graph is compressed horizontally.

### Example
$y = (2x)^2$ compresses the parabola horizontally by factor of 2.
- Point $(2, 4)$ becomes $(1, 4)$
- The graph is "squeezed" toward the y-axis

## Reflections

### Reflection over x-axis: $y = -f(x)$
- Multiply the OUTPUT by $-1$
- Every point $(x, y)$ becomes $(x, -y)$
- Flips the graph upside down

### Reflection over y-axis: $y = f(-x)$
- Multiply the INPUT by $-1$
- Every point $(x, y)$ becomes $(-x, y)$
- Flips the graph left-to-right

### Example
For $f(x) = \sqrt{x}$:
- $-\sqrt{x}$ reflects over x-axis (opens downward)
- $\sqrt{-x}$ reflects over y-axis (defined for $x \le 0$)

## Combining Transformations: Order Matters!

When multiple transformations are present, apply them in this order:

### Standard Order (for graphing)
1. Horizontal shifts (inside the function)
2. Horizontal stretch/compression (inside)
3. Reflections
4. Vertical stretch/compression (outside)
5. Vertical shifts (outside)

### The General Form
$$y = a \cdot f(b(x - h)) + k$$

| Parameter | Effect |
|-----------|--------|
| $a$ | Vertical stretch/compression and reflection over x-axis |
| $b$ | Horizontal stretch/compression and reflection over y-axis |
| $h$ | Horizontal shift (right if positive) |
| $k$ | Vertical shift (up if positive) |

## Worked Example 1: Identifying Transformations

**Problem**: Describe the transformations to obtain $y = -2(x + 3)^2 - 5$ from $y = x^2$.

**Solution**:
Starting from $y = x^2$:

1. **$(x + 3)^2$**: Shift LEFT 3 units
2. **$-2(x + 3)^2$**:
   - The $2$ stretches vertically by factor of 2
   - The $-$ reflects over the x-axis
3. **$-2(x + 3)^2 - 5$**: Shift DOWN 5 units

**Summary**: Left 3, vertical stretch by 2, reflect over x-axis, down 5.

**New vertex**: $(-3, -5)$ (parabola opens downward)

## Worked Example 2: Writing the Equation

**Problem**: The graph of $y = |x|$ is shifted right 2 units, reflected over the x-axis, and shifted up 4 units. Write the equation.

**Solution**:
Apply transformations in order:

1. Shift right 2: $y = |x - 2|$
2. Reflect over x-axis: $y = -|x - 2|$
3. Shift up 4: $y = -|x - 2| + 4$

**Answer**: $y = -|x - 2| + 4$

## Worked Example 3: Graphing Step by Step

**Problem**: Graph $y = \sqrt{x - 1} + 2$

**Solution**:
Start with parent function $y = \sqrt{x}$ with key points $(0, 0)$, $(1, 1)$, $(4, 2)$.

1. Shift right 1: $(0,0) \to (1, 0)$, $(1, 1) \to (2, 1)$, $(4, 2) \to (5, 2)$
2. Shift up 2: $(1, 0) \to (1, 2)$, $(2, 1) \to (2, 3)$, $(5, 2) \to (5, 4)$

**Key points of transformed function**: $(1, 2)$, $(2, 3)$, $(5, 4)$

Starting point (replaces the origin): $(1, 2)$

## Worked Example 4: Complete Analysis

**Problem**: For $g(x) = 3\sin(2x - \pi) + 1$, identify all transformations.

**Solution**:
First, rewrite in standard form by factoring inside:
$$g(x) = 3\sin\left(2\left(x - \frac{\pi}{2}\right)\right) + 1$$

Now identify:
- $a = 3$: Vertical stretch by 3 (amplitude = 3)
- $b = 2$: Horizontal compression by factor of 2 (period = $\frac{2\pi}{2} = \pi$)
- $h = \frac{\pi}{2}$: Shift right by $\frac{\pi}{2}$
- $k = 1$: Shift up 1

## Effect on Domain and Range

Transformations affect domain and range predictably:

| Transformation | Effect on Domain | Effect on Range |
|----------------|------------------|-----------------|
| Vertical shift $+k$ | No change | Shift by $k$ |
| Horizontal shift $-h$ | Shift by $h$ | No change |
| Vertical stretch $a$ | No change | Multiply by $a$ |
| Horizontal stretch $1/b$ | Multiply by $1/b$ | No change |
| Reflect over x-axis | No change | Negate range |
| Reflect over y-axis | Negate domain | No change |

### Example
If $f(x) = \sqrt{x}$ has domain $[0, \infty)$ and range $[0, \infty)$:

For $g(x) = -2\sqrt{x - 3} + 5$:
- Domain: Shifted right 3 → $[3, \infty)$
- Range: Stretched by 2, reflected, shifted up 5 → $(-\infty, 5]$

## Key Formulas

**General Transformation Form**:
$$y = a \cdot f(b(x - h)) + k$$

**Transformation Summary**:
| In Equation | Action | Direction |
|-------------|--------|-----------|
| $+k$ outside | Vertical shift | Up |
| $-k$ outside | Vertical shift | Down |
| $-h$ inside | Horizontal shift | Right |
| $+h$ inside | Horizontal shift | Left |
| $a > 1$ outside | Vertical stretch | Away from x-axis |
| $0 < a < 1$ outside | Vertical compress | Toward x-axis |
| $-$ outside | Reflection | Over x-axis |
| $-$ inside | Reflection | Over y-axis |

## Common Mistakes to Avoid

1. **Wrong direction for horizontal shifts**
   - $f(x - 3)$ shifts RIGHT 3, not left
   - Remember: inside works "backwards"

2. **Confusing stretch and compression**
   - $f(2x)$ compresses horizontally (by factor of 2)
   - $f(x/2)$ stretches horizontally (by factor of 2)

3. **Wrong order of transformations**
   - Apply horizontal transformations before vertical
   - Handle inside-the-function operations first

4. **Forgetting to factor when identifying $h$**
   - $y = \sin(2x - \pi)$ is NOT a shift of $\pi$ right
   - Factor: $y = \sin(2(x - \frac{\pi}{2}))$ — shift is $\frac{\pi}{2}$ right

5. **Mixing up reflection axes**
   - $-f(x)$: flip over x-axis (change $y$-values)
   - $f(-x)$: flip over y-axis (change $x$-values)

## Calculus Connection

Understanding transformations helps in calculus:

1. **Derivatives of Transformed Functions**:
   - $\frac{d}{dx}[f(x - h)] = f'(x - h)$ (horizontal shift doesn't change derivative formula)
   - $\frac{d}{dx}[a \cdot f(x)] = a \cdot f'(x)$ (constants pull out)

2. **Chain Rule**: $\frac{d}{dx}[f(bx)] = b \cdot f'(bx)$

3. **Graphing Derivatives**: The derivative graph relates to the original through slopes, which transformations affect predictably.

---

## Practice Problems

### Basic (Computational)

**Problem 1**
Describe the transformation: $y = x^2 + 5$

<details>
<summary>Show Solution</summary>

**Solution**:
This is a vertical shift UP 5 units.

Parent function $y = x^2$ with vertex $(0, 0)$ becomes vertex $(0, 5)$.
</details>

---

**Problem 2**
Describe the transformation: $y = (x - 4)^3$

<details>
<summary>Show Solution</summary>

**Solution**:
This is a horizontal shift RIGHT 4 units.

The inflection point moves from $(0, 0)$ to $(4, 0)$.
</details>

---

**Problem 3**
Describe the transformation: $y = -|x|$

<details>
<summary>Show Solution</summary>

**Solution**:
This is a reflection over the x-axis.

The V-shape opens downward instead of upward.
</details>

---

**Problem 4**
Write the equation if $y = \sqrt{x}$ is shifted left 6 units.

<details>
<summary>Show Solution</summary>

**Solution**:
Left shift means add inside:

$$y = \sqrt{x + 6}$$
</details>

---

**Problem 5**
Write the equation if $y = e^x$ is shifted down 3 units and reflected over the x-axis.

<details>
<summary>Show Solution</summary>

**Solution**:
Reflect: $y = -e^x$
Shift down: $y = -e^x - 3$

**Answer**: $y = -e^x - 3$
</details>

---

### Intermediate (Multi-step)

**Problem 6**
Describe all transformations for $y = 2(x - 1)^2 + 3$.

<details>
<summary>Show Solution</summary>

**Solution**:
Starting from $y = x^2$:

1. Horizontal shift RIGHT 1 unit (from $x - 1$)
2. Vertical stretch by factor of 2 (from the 2)
3. Vertical shift UP 3 units (from $+3$)

Vertex moves from $(0, 0)$ to $(1, 3)$.
</details>

---

**Problem 7**
The function $y = |x|$ is transformed to have vertex at $(-2, 4)$ and open downward. Write the equation.

<details>
<summary>Show Solution</summary>

**Solution**:
- Vertex at $(-2, 4)$: shift left 2 and up 4
- Opens downward: reflect over x-axis

$$y = -|x + 2| + 4$$
</details>

---

**Problem 8**
For $f(x) = \sqrt{x}$ with domain $[0, \infty)$ and range $[0, \infty)$, find the domain and range of $g(x) = \sqrt{x + 4} - 2$.

<details>
<summary>Show Solution</summary>

**Solution**:
Transformations: left 4, down 2

**Domain**: Shift left 4: $[-4, \infty)$

**Range**: Shift down 2: $[-2, \infty)$
</details>

---

**Problem 9**
Graph the key points of $y = -2|x - 3| + 6$.

<details>
<summary>Show Solution</summary>

**Solution**:
Parent: $y = |x|$ with vertex $(0, 0)$ and points $(-1, 1)$, $(1, 1)$

Transformations:
1. Right 3: vertex → $(3, 0)$, points $(2, 1)$, $(4, 1)$
2. Vertical stretch by 2: vertex $(3, 0)$, points $(2, 2)$, $(4, 2)$
3. Reflect over x-axis: vertex $(3, 0)$, points $(2, -2)$, $(4, -2)$
4. Up 6: vertex $(3, 6)$, points $(2, 4)$, $(4, 4)$

**Key points**: $(3, 6)$ (vertex), $(2, 4)$, $(4, 4)$, $(0, 0)$, $(6, 0)$
</details>

---

**Problem 10**
Rewrite $y = \cos(3x + \pi)$ by factoring, then identify the transformations.

<details>
<summary>Show Solution</summary>

**Solution**:
Factor out the 3:
$$y = \cos\left(3\left(x + \frac{\pi}{3}\right)\right)$$

Transformations from $y = \cos(x)$:
1. Horizontal compression by factor of 3 (period = $\frac{2\pi}{3}$)
2. Horizontal shift LEFT by $\frac{\pi}{3}$
</details>

---

### Advanced (Complex Applications)

**Problem 11**
If $f(x) = x^2$, express $g(x) = 2x^2 - 8x + 11$ in transformation form $a(x - h)^2 + k$.

<details>
<summary>Show Solution</summary>

**Solution**:
Complete the square:
$$g(x) = 2x^2 - 8x + 11$$
$$= 2(x^2 - 4x) + 11$$
$$= 2(x^2 - 4x + 4 - 4) + 11$$
$$= 2((x - 2)^2 - 4) + 11$$
$$= 2(x - 2)^2 - 8 + 11$$
$$= 2(x - 2)^2 + 3$$

**Transformations**: Right 2, vertical stretch by 2, up 3.

**Vertex**: $(2, 3)$
</details>

---

**Problem 12**
Given $f(x)$ with domain $[-3, 5]$ and range $[-2, 4]$, find the domain and range of $g(x) = -3f(x - 2) + 1$.

<details>
<summary>Show Solution</summary>

**Solution**:
Transformations: right 2, vertical stretch by 3, reflect over x-axis, up 1

**Domain**: Shift right 2
$$[-3 + 2, 5 + 2] = [-1, 7]$$

**Range**:
- Original range: $[-2, 4]$
- Multiply by $-3$: $[-12, 6]$ (note order flips: $-3(4) = -12$, $-3(-2) = 6$)
- Add 1: $[-11, 7]$

**Domain**: $[-1, 7]$, **Range**: $[-11, 7]$
</details>

---

**Problem 13**
Write an equation for a function that is a horizontally stretched version of $y = \ln(x)$ by factor of 2, reflected over the y-axis, and shifted right 3 units.

<details>
<summary>Show Solution</summary>

**Solution**:
Apply in order:

1. Horizontal stretch by 2: $y = \ln(x/2)$ or $y = \ln\left(\frac{x}{2}\right)$
2. Reflect over y-axis: $y = \ln\left(\frac{-x}{2}\right)$
3. Shift right 3: $y = \ln\left(\frac{-(x-3)}{2}\right) = \ln\left(\frac{3-x}{2}\right)$

**Answer**: $y = \ln\left(\dfrac{3-x}{2}\right)$
</details>

---

**Problem 14**
The graph of $y = f(x)$ passes through $(1, 3)$, $(2, 5)$, and $(4, -1)$. Find three points on the graph of $y = 2f(x - 3) - 4$.

<details>
<summary>Show Solution</summary>

**Solution**:
For each point $(x, y)$:
- New $x$: $x + 3$ (shift right)
- New $y$: $2y - 4$ (stretch by 2, then down 4)

$(1, 3) \to (1+3, 2(3)-4) = (4, 2)$

$(2, 5) \to (2+3, 2(5)-4) = (5, 6)$

$(4, -1) \to (4+3, 2(-1)-4) = (7, -6)$

**Points**: $(4, 2)$, $(5, 6)$, $(7, -6)$
</details>

---

**Problem 15**
Find the equation of a parabola with vertex at $(3, -2)$, passing through $(5, 6)$, opening upward.

<details>
<summary>Show Solution</summary>

**Solution**:
Vertex form: $y = a(x - 3)^2 - 2$

Use point $(5, 6)$ to find $a$:
$$6 = a(5 - 3)^2 - 2$$
$$6 = 4a - 2$$
$$8 = 4a$$
$$a = 2$$

**Answer**: $y = 2(x - 3)^2 - 2$
</details>

---

### AP Exam Style

**Problem 16**
If $f(x) = x^2$, which of the following represents a shift of 3 units right and 2 units down?

(A) $y = (x + 3)^2 - 2$
(B) $y = (x - 3)^2 - 2$
(C) $y = (x + 3)^2 + 2$
(D) $y = (x - 2)^2 - 3$

<details>
<summary>Show Solution</summary>

**Solution**:
- Right 3: use $(x - 3)$
- Down 2: subtract 2

**Answer: (B)** $y = (x - 3)^2 - 2$
</details>

---

**Problem 17**
The graph of $y = f(x)$ has a maximum at $(2, 5)$. What is the maximum point of $y = -f(x - 1) + 3$?

<details>
<summary>Show Solution</summary>

**Solution**:
Original maximum: $(2, 5)$

Transformations:
- Shift right 1: $(2 + 1, 5) = (3, 5)$
- Reflect over x-axis: $(3, -5)$ — this becomes a MINIMUM
- Shift up 3: $(3, -5 + 3) = (3, -2)$

Wait — after reflection, the maximum becomes a minimum!

The new function has a **minimum** at $(3, -2)$, not a maximum.

If the question asks for the maximum, there isn't one (the function now opens upward to infinity).

**Answer**: The function has a minimum at $(3, -2)$, not a maximum.
</details>

---

**Problem 18**
If $g(x) = 2\sqrt{x + 4} - 3$, which transformations were applied to $f(x) = \sqrt{x}$?

(A) Left 4, stretch by 2, down 3
(B) Right 4, stretch by 2, up 3
(C) Left 4, compress by 2, down 3
(D) Right 4, compress by 1/2, up 3

<details>
<summary>Show Solution</summary>

**Solution**:
$g(x) = 2\sqrt{x + 4} - 3$

- $x + 4$ inside: shift LEFT 4
- Multiply by 2 outside: vertical STRETCH by 2
- Subtract 3: shift DOWN 3

**Answer: (A)**
</details>

---

**Problem 19** *(Free Response Style)*
Let $f(x) = |x|$.

(a) Write the equation of $g(x)$, which is $f(x)$ shifted right 2 units and up 1 unit.
(b) Write the equation of $h(x)$, which is $g(x)$ reflected over the x-axis.
(c) Find the x-intercepts of $h(x)$.
(d) Find the domain and range of $h(x)$.

<details>
<summary>Show Solution</summary>

**Solution**:

**(a)** $g(x) = |x - 2| + 1$

**(b)** $h(x) = -(|x - 2| + 1) = -|x - 2| - 1$

**(c)** Find where $h(x) = 0$:
$$-|x - 2| - 1 = 0$$
$$-|x - 2| = 1$$
$$|x - 2| = -1$$

This has no solution since absolute value cannot be negative.

**No x-intercepts.**

**(d)**
- Domain: all real numbers, $(-\infty, \infty)$
- Range: $h(x) = -|x-2| - 1 \le -1$ for all $x$, so Range = $(-\infty, -1]$
</details>

---

**Problem 20** *(Free Response Style)*
A scientist models population growth with $P(t) = 100 \cdot 2^{t}$ where $t$ is in years.

(a) Describe the transformation from the parent function $y = 2^x$ to $P(t)$.
(b) A new model $Q(t) = 100 \cdot 2^{t-3} + 50$ is proposed. Describe all transformations from $P(t)$ to $Q(t)$.
(c) Interpret the transformation $t - 3$ in context.
(d) If $P(0) = 100$, find $Q(0)$ and interpret.

<details>
<summary>Show Solution</summary>

**Solution**:

**(a)** From $y = 2^x$ to $P(t) = 100 \cdot 2^t$:
- Vertical stretch by factor of 100

**(b)** From $P(t) = 100 \cdot 2^t$ to $Q(t) = 100 \cdot 2^{t-3} + 50$:
- Horizontal shift RIGHT 3 units
- Vertical shift UP 50 units

**(c)** The shift right by 3 means the population reaches each level 3 years later than the original model. It represents a 3-year delay in growth.

**(d)**
$$Q(0) = 100 \cdot 2^{0-3} + 50 = 100 \cdot 2^{-3} + 50 = 100 \cdot \frac{1}{8} + 50 = 12.5 + 50 = 62.5$$

Interpretation: At time $t = 0$, the delayed model with baseline shows a population of 62.5 (compared to 100 in the original). The 50 represents a baseline population that exists independent of the exponential growth.
</details>

---

## What's Next

Now that you understand transformations, you're ready to explore [Factoring Techniques](/calculus/0105-factoring-techniques), where we'll master the essential algebra skills needed to simplify expressions before applying calculus operations.

---

<div align="center">

[← Inverse Functions](/calculus/0103-inverse-functions) | [Factoring Techniques →](/calculus/0105-factoring-techniques)

</div>
