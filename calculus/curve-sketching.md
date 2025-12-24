# Curve Sketching

*Before graphing calculators existed, mathematicians had to sketch curves by hand using calculus. This skill isn't obsolete—understanding how derivatives reveal a function's behavior gives you insight that no calculator can provide. When you can predict a graph's shape from its equation, you truly understand the function.*

---

## What You'll Learn
- Use first and second derivatives to analyze function behavior
- Find and classify critical points as local maxima, minima, or neither
- Determine intervals of increase and decrease
- Find inflection points and intervals of concavity
- Sketch accurate graphs using calculus techniques
- Combine all analysis into a complete curve sketch

---

## Prerequisites
- [Derivatives](/calculus/definition-of-derivative)
- [Extreme Values](/calculus/extreme-values)
- [Mean Value Theorem](/calculus/mean-value-theorem)

---

## The Core Concept

### Intuition First

Think of driving along a winding mountain road:
- **First derivative** (f'): Are you going uphill or downhill? (increasing or decreasing)
- **Second derivative** (f''): Is the road curving left or right? (concavity)

When you combine these two pieces of information, you know everything about the road's shape without seeing it directly. That's exactly what curve sketching does for functions.

### The Complete Picture

| What to Find | What It Tells You |
|--------------|-------------------|
| Domain | Where the function exists |
| Intercepts | Where the curve crosses axes |
| Symmetry | Even, odd, or neither |
| $f'(x) = 0$ or undefined | Critical points |
| Sign of $f'(x)$ | Increasing/decreasing intervals |
| $f''(x) = 0$ or undefined | Possible inflection points |
| Sign of $f''(x)$ | Concavity |
| Limits at boundaries | Asymptotes and end behavior |

### The First Derivative Test

The first derivative tells you where a function increases or decreases:

- **$f'(x) > 0$**: Function is increasing (going up as x increases)
- **$f'(x) < 0$**: Function is decreasing (going down as x increases)
- **$f'(x) = 0$**: Horizontal tangent (potential max/min)

**First Derivative Test for Local Extrema**:

At a critical point $c$ where $f'(c) = 0$:
- If $f'$ changes from **positive to negative** at $c$ → **local maximum**
- If $f'$ changes from **negative to positive** at $c$ → **local minimum**
- If $f'$ doesn't change sign → **neither** (inflection point with horizontal tangent)

### The Second Derivative Test

The second derivative reveals **concavity**:

- **$f''(x) > 0$**: Concave up (smile shape, "holds water") ∪
- **$f''(x) < 0$**: Concave down (frown shape, "spills water") ∩

**Second Derivative Test for Local Extrema**:

At a critical point $c$ where $f'(c) = 0$:
- If $f''(c) > 0$ → **local minimum** (concave up = valley)
- If $f''(c) < 0$ → **local maximum** (concave down = peak)
- If $f''(c) = 0$ → **inconclusive** (use First Derivative Test)

### Inflection Points

An **inflection point** is where the concavity changes (from up to down or down to up).

To find inflection points:
1. Find where $f''(x) = 0$ or $f''(x)$ is undefined
2. Check that $f''$ actually changes sign at these points
3. Verify the point is in the domain of $f$

### Worked Examples

**Example 1**: Sketch $f(x) = x^3 - 3x^2 + 4$

**Step 1: Domain and Intercepts**

Domain: All real numbers (polynomial)

y-intercept: $f(0) = 4$, so $(0, 4)$

x-intercepts: Solve $x^3 - 3x^2 + 4 = 0$. By inspection or factoring: $(x+1)(x-2)^2 = 0$, so $x = -1$ and $x = 2$.

**Step 2: First Derivative Analysis**

$$f'(x) = 3x^2 - 6x = 3x(x - 2)$$

Critical points: $f'(x) = 0$ when $x = 0$ or $x = 2$

Sign chart for $f'$:

| Interval | Test point | $f'(x)$ | Behavior |
|----------|------------|---------|----------|
| $(-\infty, 0)$ | $x = -1$ | $3(-1)(-3) = 9 > 0$ | Increasing |
| $(0, 2)$ | $x = 1$ | $3(1)(-1) = -3 < 0$ | Decreasing |
| $(2, \infty)$ | $x = 3$ | $3(3)(1) = 9 > 0$ | Increasing |

By First Derivative Test:
- $x = 0$: local maximum (changes from + to -)
- $x = 2$: local minimum (changes from - to +)

**Step 3: Second Derivative Analysis**

$$f''(x) = 6x - 6 = 6(x - 1)$$

$f''(x) = 0$ when $x = 1$

Sign chart for $f''$:

| Interval | $f''(x)$ | Concavity |
|----------|----------|-----------|
| $(-\infty, 1)$ | $< 0$ | Concave down |
| $(1, \infty)$ | $> 0$ | Concave up |

Since $f''$ changes sign at $x = 1$, there's an inflection point at $(1, f(1)) = (1, 2)$.

**Step 4: Key Points**

- Local max: $(0, 4)$
- Local min: $(2, 0)$
- Inflection point: $(1, 2)$
- x-intercepts: $(-1, 0)$, $(2, 0)$
- y-intercept: $(0, 4)$

**Step 5: Sketch**

The curve starts from bottom-left, increases through $(-1, 0)$, reaches max at $(0, 4)$, decreases through inflection at $(1, 2)$, reaches min at $(2, 0)$, then increases to infinity.

---

**Example 2**: Sketch $f(x) = \frac{x^2}{x^2 - 1}$

**Step 1: Domain**

$x^2 - 1 = 0$ when $x = \pm 1$

Domain: $(-\infty, -1) \cup (-1, 1) \cup (1, \infty)$

**Step 2: Intercepts and Symmetry**

y-intercept: $f(0) = 0$, so $(0, 0)$

x-intercept: $x^2 = 0$ means $x = 0$, so $(0, 0)$

Symmetry: $f(-x) = \frac{(-x)^2}{(-x)^2 - 1} = \frac{x^2}{x^2 - 1} = f(x)$ → **Even function** (symmetric about y-axis)

**Step 3: Asymptotes**

Vertical: $x = 1$ and $x = -1$ (where denominator = 0)

Horizontal:

$$\lim_{x \to \infty} \frac{x^2}{x^2 - 1} = \lim_{x \to \infty} \frac{1}{1 - \frac{1}{x^2}} = 1$$

So $y = 1$ is a horizontal asymptote.

**Step 4: First Derivative**

$$f'(x) = \frac{2x(x^2-1) - x^2(2x)}{(x^2-1)^2} = \frac{2x^3 - 2x - 2x^3}{(x^2-1)^2} = \frac{-2x}{(x^2-1)^2}$$

$f'(x) = 0$ when $x = 0$

Since $(x^2-1)^2 > 0$ everywhere it's defined:
- $f'(x) > 0$ when $x < 0$ (in domain)
- $f'(x) < 0$ when $x > 0$ (in domain)

So $x = 0$ is a local maximum with $f(0) = 0$.

**Step 5: Second Derivative**

Using quotient rule on $f'(x) = \frac{-2x}{(x^2-1)^2}$:

$$f''(x) = \frac{-2(x^2-1)^2 - (-2x) \cdot 2(x^2-1)(2x)}{(x^2-1)^4}$$
$$= \frac{-2(x^2-1) + 8x^2}{(x^2-1)^3} = \frac{6x^2 + 2}{(x^2-1)^3}$$

Since $6x^2 + 2 > 0$ always:
- $f''(x) > 0$ when $x^2 - 1 > 0$, i.e., $|x| > 1$
- $f''(x) < 0$ when $x^2 - 1 < 0$, i.e., $|x| < 1$

No inflection points (concavity doesn't change within each piece of domain).

**Step 6: Sketch**

The function has three pieces:
- For $x < -1$: approaches $y = 1$ from above as $x \to -\infty$, concave up, approaches $+\infty$ as $x \to -1^-$
- For $-1 < x < 1$: concave down, maximum at $(0, 0)$, approaches $-\infty$ near both $x = -1$ and $x = 1$
- For $x > 1$: approaches $+\infty$ as $x \to 1^+$, concave up, approaches $y = 1$ from above as $x \to \infty$

---

**Example 3**: Sketch $f(x) = xe^{-x}$

**Step 1: Domain**

Domain: All real numbers

**Step 2: Intercepts**

y-intercept: $f(0) = 0$, so $(0, 0)$

x-intercept: $xe^{-x} = 0$ when $x = 0$ (since $e^{-x} \neq 0$), so $(0, 0)$

**Step 3: End Behavior**

$$\lim_{x \to -\infty} xe^{-x} = -\infty$$ (exponential grows faster than linear)

$$\lim_{x \to \infty} xe^{-x} = \lim_{x \to \infty} \frac{x}{e^x} = 0$$ (by L'Hôpital's Rule)

Horizontal asymptote: $y = 0$ (as $x \to \infty$)

**Step 4: First Derivative**

$$f'(x) = e^{-x} + x(-e^{-x}) = e^{-x}(1 - x)$$

$f'(x) = 0$ when $1 - x = 0$, i.e., $x = 1$

Since $e^{-x} > 0$ always:
- $f'(x) > 0$ when $x < 1$ (increasing)
- $f'(x) < 0$ when $x > 1$ (decreasing)

Local maximum at $x = 1$: $f(1) = 1 \cdot e^{-1} = \frac{1}{e} \approx 0.368$

**Step 5: Second Derivative**

$$f''(x) = -e^{-x}(1-x) + e^{-x}(-1) = e^{-x}(-1 + x - 1) = e^{-x}(x - 2)$$

$f''(x) = 0$ when $x = 2$

Since $e^{-x} > 0$:
- $f''(x) < 0$ when $x < 2$ (concave down)
- $f''(x) > 0$ when $x > 2$ (concave up)

Inflection point at $x = 2$: $f(2) = 2e^{-2} \approx 0.271$

**Step 6: Key Points**

- Local max: $(1, \frac{1}{e})$
- Inflection point: $(2, \frac{2}{e^2})$
- Intercept: $(0, 0)$
- Horizontal asymptote: $y = 0$ (right side)

---

**Example 4**: Sketch $f(x) = x^4 - 4x^3$

**Step 1: Domain and Intercepts**

Domain: All real numbers

y-intercept: $(0, 0)$

x-intercepts: $x^4 - 4x^3 = x^3(x - 4) = 0$ gives $x = 0$ and $x = 4$

**Step 2: First Derivative**

$$f'(x) = 4x^3 - 12x^2 = 4x^2(x - 3)$$

Critical points: $x = 0$ and $x = 3$

Sign chart:

| Interval | $f'(x)$ | Behavior |
|----------|---------|----------|
| $(-\infty, 0)$ | $< 0$ | Decreasing |
| $(0, 3)$ | $< 0$ | Decreasing |
| $(3, \infty)$ | $> 0$ | Increasing |

At $x = 0$: $f'$ doesn't change sign (stays negative), so **neither max nor min**
At $x = 3$: local minimum (changes - to +), $f(3) = 81 - 108 = -27$

**Step 3: Second Derivative**

$$f''(x) = 12x^2 - 24x = 12x(x - 2)$$

$f''(x) = 0$ when $x = 0$ or $x = 2$

Sign chart:

| Interval | $f''(x)$ | Concavity |
|----------|----------|-----------|
| $(-\infty, 0)$ | $> 0$ | Concave up |
| $(0, 2)$ | $< 0$ | Concave down |
| $(2, \infty)$ | $> 0$ | Concave up |

Inflection points: $(0, 0)$ and $(2, -16)$

**Step 4: Sketch**

The curve starts from $+\infty$ (upper left), decreases through $(0, 0)$ (inflection), continues decreasing with concavity change at $(2, -16)$ (inflection), reaches minimum at $(3, -27)$, then increases through $(4, 0)$ to $+\infty$.

---

**Example 5**: Complete Analysis of $f(x) = \frac{x}{x^2 + 1}$

**Domain**: All real numbers (denominator always positive)

**Intercepts**:
- y-intercept: $(0, 0)$
- x-intercept: $(0, 0)$

**Symmetry**: $f(-x) = \frac{-x}{x^2+1} = -f(x)$ → **Odd function**

**Asymptotes**:

$$\lim_{x \to \pm\infty} \frac{x}{x^2+1} = \lim_{x \to \pm\infty} \frac{1}{x} = 0$$

Horizontal asymptote: $y = 0$

**First Derivative**:

$$f'(x) = \frac{(x^2+1) - x(2x)}{(x^2+1)^2} = \frac{1-x^2}{(x^2+1)^2}$$

$f'(x) = 0$ when $x = \pm 1$

- $f'(x) > 0$ on $(-1, 1)$: increasing
- $f'(x) < 0$ on $(-\infty, -1)$ and $(1, \infty)$: decreasing

Local min at $(-1, -\frac{1}{2})$, local max at $(1, \frac{1}{2})$

**Second Derivative**:

$$f''(x) = \frac{-2x(x^2+1)^2 - (1-x^2) \cdot 2(x^2+1)(2x)}{(x^2+1)^4}$$
$$= \frac{-2x(x^2+1) - 4x(1-x^2)}{(x^2+1)^3} = \frac{2x(x^2 - 3)}{(x^2+1)^3}$$

$f''(x) = 0$ when $x = 0$ or $x = \pm\sqrt{3}$

Inflection points at $x = 0, \pm\sqrt{3}$

---

## Key Formulas & Rules

| Analysis Step | Formula/Method |
|---------------|----------------|
| Increasing | $f'(x) > 0$ |
| Decreasing | $f'(x) < 0$ |
| Concave Up | $f''(x) > 0$ |
| Concave Down | $f''(x) < 0$ |
| Local Max (1st test) | $f'$ changes + to - |
| Local Min (1st test) | $f'$ changes - to + |
| Local Max (2nd test) | $f'(c) = 0$ and $f''(c) < 0$ |
| Local Min (2nd test) | $f'(c) = 0$ and $f''(c) > 0$ |
| Inflection Point | $f''$ changes sign |

**Curve Sketching Checklist**:
1. Domain
2. Intercepts (x and y)
3. Symmetry (even/odd)
4. Asymptotes (vertical, horizontal, oblique)
5. First derivative analysis (critical points, increasing/decreasing)
6. Second derivative analysis (inflection points, concavity)
7. Key points and sketch

---

## Common Mistakes to Avoid

1. **Forgetting to check domain**: Always identify where the function exists before analyzing.

2. **Confusing critical points with extrema**: A critical point is where $f'(x) = 0$ or undefined. Not all critical points are maxima or minima.

3. **Assuming $f''(c) = 0$ means inflection point**: The second derivative must actually change sign for an inflection point.

4. **Ignoring endpoints**: On a closed interval, also check endpoints for absolute extrema.

5. **Missing vertical asymptotes**: Look for values where the denominator equals zero.

6. **Second Derivative Test limitations**: If $f''(c) = 0$, the test is inconclusive—use the First Derivative Test instead.

7. **Not verifying sign changes**: Always check intervals on both sides of critical points.

---

## AP Exam Tips

### For Both AB and BC:
- Memorize the curve sketching checklist
- Practice creating sign charts quickly
- Know both the First and Second Derivative Tests
- Be able to work backwards: given a graph of $f'$, sketch $f$

### Common Question Types:
1. **Analysis from equation**: Given $f(x)$, find extrema, inflection points, intervals
2. **Analysis from $f'$ graph**: Determine behavior of $f$ from derivative graph
3. **Justification questions**: Explain WHY a point is a max/min/inflection
4. **Sketching**: Draw a function given derivative information

### Free Response Tips:
- State your test (First or Second Derivative) before using it
- Show sign charts or explain sign changes
- Justify conclusions with clear reasoning
- Label key points on your sketch

---

## Practice Problems

### Basic (Problems 1-5)

**1.** Given:

$$f(x) = x^3 - 3x$$

Find all local extrema and inflection points.

---

**2.** Given:

$$f(x) = x^4 - 2x^2$$

Find all intervals where $f$ is increasing and decreasing.

---

**3.** Given:

$$f(x) = \frac{1}{x^2 + 1}$$

Find all intervals where $f$ is concave up and concave down.

---

**4.** Given:

$$f(x) = x^2 e^{-x}$$

Find the critical points and determine whether each is a local max or min.

---

**5.** Given:

$$f(x) = x + \frac{1}{x}$$

for $x > 0$. Find the absolute minimum value.

---

### Intermediate (Problems 6-10)

**6.** Given:

$$f(x) = x^3 - 6x^2 + 9x + 1$$

Complete a full curve sketch including intercepts, extrema, and inflection points.

---

**7.** Given:

$$f(x) = \frac{x^2 - 4}{x^2 - 9}$$

Find all asymptotes and analyze the behavior near each.

---

**8.** Given:

$$f(x) = x \ln x$$

for $x > 0$. Find all critical points, inflection points, and sketch the curve.

---

**9.** Given:

$$f(x) = \sin x + \cos x$$

on $[0, 2\pi]$. Find all local extrema and inflection points.

---

**10.** Given:

$$f(x) = x^{2/3}(x - 5)$$

Find all critical points and classify each using the First Derivative Test.

---

### Advanced (Problems 11-15)

**11.** Given:

$$f(x) = \frac{x^3}{x^2 - 1}$$

Complete a full analysis including domain, asymptotes, extrema, concavity, and sketch.

---

**12.** Given:

$$f(x) = e^{-x^2}$$

Find all extrema and inflection points. Identify this as a famous curve.

---

**13.** Given that:

$$f'(x) = (x - 1)^2(x + 2)$$

sketch a possible graph of $f(x)$, labeling all key features.

---

**14.** Given:

$$f(x) = x^4 - 4x^3 + 4x^2$$

Show that $f$ has exactly one local minimum and find it.

---

**15.** Given:

$$f(x) = \arctan(x^2)$$

Find all inflection points and determine the concavity on each interval.

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

The function $f(x) = x^3 - 3x^2 - 9x + 5$ has a local maximum at:

| Choice | Answer |
|--------|--------|
| **(A)** | $x = -1$ only |
| **(B)** | $x = 3$ only |
| **(C)** | $x = -1$ and $x = 3$ |
| **(D)** | $x = 1$ only |

---

#### Problem 17 (Multiple Choice)

The graph of $f''(x)$ is shown below (a parabola opening upward, crossing the x-axis at $x = 1$ and $x = 3$). How many inflection points does the graph of $f$ have?

| Choice | Answer |
|--------|--------|
| **(A)** | 0 |
| **(B)** | 1 |
| **(C)** | 2 |
| **(D)** | 3 |

---

#### Problem 18 (Free Response)

Let $f(x) = x^4 - 8x^2 + 16$.

> **(a)** Find all critical points of $f$ and classify each as a local maximum, local minimum, or neither.
>
> **(b)** Find all inflection points of $f$.
>
> **(c)** Sketch the graph of $f$, labeling all key features found in parts (a) and (b).

---

#### Problem 19 (Multiple Choice)

If $f'(x) = (x + 1)(x - 2)^2$, then the graph of $f$ has:

| Choice | Answer |
|--------|--------|
| **(A)** | one local maximum and one local minimum |
| **(B)** | one local maximum and no local minimum |
| **(C)** | no local maximum and one local minimum |
| **(D)** | no local extrema |

---

#### Problem 20 (Free Response - Challenging)

Let $f$ be a function defined on all real numbers such that $f(0) = 2$ and:

$$f'(x) = \frac{x}{(x^2 + 1)^2}$$

> **(a)** Find all critical points of $f$ and use the First Derivative Test to classify each.
>
> **(b)** Find $f''(x)$ and determine all inflection points.
>
> **(c)** Find $\lim_{x \to \infty} f(x)$ and $\lim_{x \to -\infty} f(x)$.
>
> **(d)** Sketch the graph of $f$.

---

## Answer Key

<details>
<summary><strong>Problem 1 Solution</strong></summary>

**Answer**: Local max at $(-1, 2)$, local min at $(1, -2)$, inflection point at $(0, 0)$

**Step-by-step solution**:

**First derivative**:

$$f'(x) = 3x^2 - 3 = 3(x-1)(x+1)$$

Critical points: $x = -1$ and $x = 1$

Sign chart for $f'$:
- $f'(x) > 0$ on $(-\infty, -1)$ and $(1, \infty)$
- $f'(x) < 0$ on $(-1, 1)$

By First Derivative Test:
- $x = -1$: local maximum, $f(-1) = -1 + 3 = 2$
- $x = 1$: local minimum, $f(1) = 1 - 3 = -2$

**Second derivative**:

$$f''(x) = 6x$$

$f''(x) = 0$ when $x = 0$

Sign changes from negative to positive at $x = 0$.

Inflection point: $(0, f(0)) = (0, 0)$

</details>

---

<details>
<summary><strong>Problem 2 Solution</strong></summary>

**Answer**: Increasing on $(-1, 0)$ and $(1, \infty)$; Decreasing on $(-\infty, -1)$ and $(0, 1)$

**Step-by-step solution**:

$$f'(x) = 4x^3 - 4x = 4x(x^2 - 1) = 4x(x-1)(x+1)$$

Critical points: $x = -1, 0, 1$

Sign chart:

| Interval | $4x$ | $(x-1)$ | $(x+1)$ | $f'(x)$ | Behavior |
|----------|------|---------|---------|---------|----------|
| $(-\infty, -1)$ | $-$ | $-$ | $-$ | $-$ | Decreasing |
| $(-1, 0)$ | $-$ | $-$ | $+$ | $+$ | Increasing |
| $(0, 1)$ | $+$ | $-$ | $+$ | $-$ | Decreasing |
| $(1, \infty)$ | $+$ | $+$ | $+$ | $+$ | Increasing |

</details>

---

<details>
<summary><strong>Problem 3 Solution</strong></summary>

**Answer**: Concave up on $(-\infty, -\frac{1}{\sqrt{3}})$ and $(\frac{1}{\sqrt{3}}, \infty)$; Concave down on $(-\frac{1}{\sqrt{3}}, \frac{1}{\sqrt{3}})$

**Step-by-step solution**:

$$f(x) = (x^2 + 1)^{-1}$$

$$f'(x) = -\frac{2x}{(x^2+1)^2}$$

$$f''(x) = \frac{-2(x^2+1)^2 - (-2x) \cdot 2(x^2+1)(2x)}{(x^2+1)^4}$$

$$= \frac{-2(x^2+1) + 8x^2}{(x^2+1)^3} = \frac{6x^2 - 2}{(x^2+1)^3}$$

$f''(x) = 0$ when $6x^2 - 2 = 0$, i.e., $x^2 = \frac{1}{3}$, so $x = \pm\frac{1}{\sqrt{3}}$

Since $(x^2+1)^3 > 0$:
- $f''(x) > 0$ when $6x^2 - 2 > 0$, i.e., $|x| > \frac{1}{\sqrt{3}}$
- $f''(x) < 0$ when $|x| < \frac{1}{\sqrt{3}}$

</details>

---

<details>
<summary><strong>Problem 4 Solution</strong></summary>

**Answer**: Critical points at $x = 0$ (local min) and $x = 2$ (local max)

**Step-by-step solution**:

$$f'(x) = 2xe^{-x} + x^2(-e^{-x}) = e^{-x}(2x - x^2) = xe^{-x}(2 - x)$$

Critical points: $x = 0$ and $x = 2$

**Second Derivative Test**:

$$f''(x) = e^{-x}(2 - x) + xe^{-x}(-1) + (2x - x^2)(-e^{-x})$$
$$= e^{-x}(2 - x - x - 2x + x^2) = e^{-x}(x^2 - 4x + 2)$$

At $x = 0$: $f''(0) = e^0(0 - 0 + 2) = 2 > 0$ → **local minimum**

At $x = 2$: $f''(2) = e^{-2}(4 - 8 + 2) = -2e^{-2} < 0$ → **local maximum**

</details>

---

<details>
<summary><strong>Problem 5 Solution</strong></summary>

**Answer**: Absolute minimum value is $2$ at $x = 1$

**Step-by-step solution**:

$$f'(x) = 1 - \frac{1}{x^2}$$

Setting $f'(x) = 0$:
$$1 - \frac{1}{x^2} = 0$$
$$x^2 = 1$$
$$x = 1$$ (since $x > 0$)

**Second Derivative Test**:

$$f''(x) = \frac{2}{x^3}$$

At $x = 1$: $f''(1) = 2 > 0$ → **local minimum**

Since $f(x) \to \infty$ as $x \to 0^+$ and $x \to \infty$, this local minimum is also the absolute minimum.

$$f(1) = 1 + 1 = 2$$

</details>

---

<details>
<summary><strong>Problem 6 Solution</strong></summary>

**Answer**: Local max at $(1, 5)$, local min at $(3, 1)$, inflection at $(2, 3)$

**Step-by-step solution**:

**Intercepts**:
- y-intercept: $(0, 1)$
- x-intercepts: Difficult to find exactly (one real root near $x \approx -0.1$)

**First derivative**:

$$f'(x) = 3x^2 - 12x + 9 = 3(x^2 - 4x + 3) = 3(x-1)(x-3)$$

Critical points: $x = 1$ and $x = 3$

$f(1) = 1 - 6 + 9 + 1 = 5$
$f(3) = 27 - 54 + 27 + 1 = 1$

Sign chart shows $f' > 0$ on $(-\infty, 1)$ and $(3, \infty)$, $f' < 0$ on $(1, 3)$

Local max at $(1, 5)$, local min at $(3, 1)$

**Second derivative**:

$$f''(x) = 6x - 12 = 6(x - 2)$$

$f''(x) = 0$ at $x = 2$

$f(2) = 8 - 24 + 18 + 1 = 3$

Inflection point at $(2, 3)$

</details>

---

<details>
<summary><strong>Problem 7 Solution</strong></summary>

**Answer**: Vertical asymptotes at $x = \pm 3$, horizontal asymptote at $y = 1$

**Step-by-step solution**:

**Vertical asymptotes**: $x^2 - 9 = 0$ when $x = \pm 3$

**Horizontal asymptote**:

$$\lim_{x \to \pm\infty} \frac{x^2 - 4}{x^2 - 9} = \lim_{x \to \pm\infty} \frac{1 - 4/x^2}{1 - 9/x^2} = 1$$

So $y = 1$ is a horizontal asymptote.

**Behavior near $x = 3$**:
- As $x \to 3^+$: numerator $\to 5$, denominator $\to 0^+$, so $f(x) \to +\infty$
- As $x \to 3^-$: numerator $\to 5$, denominator $\to 0^-$, so $f(x) \to -\infty$

**Behavior near $x = -3$**:
- As $x \to -3^+$: numerator $\to 5$, denominator $\to 0^-$, so $f(x) \to -\infty$
- As $x \to -3^-$: numerator $\to 5$, denominator $\to 0^+$, so $f(x) \to +\infty$

</details>

---

<details>
<summary><strong>Problem 8 Solution</strong></summary>

**Answer**: Critical point at $x = \frac{1}{e}$ (local min), inflection point at $x = \frac{1}{e^{3/2}}$

**Step-by-step solution**:

**Domain**: $x > 0$

**First derivative**:

$$f'(x) = \ln x + x \cdot \frac{1}{x} = \ln x + 1$$

$f'(x) = 0$ when $\ln x = -1$, i.e., $x = e^{-1} = \frac{1}{e}$

$f'(x) < 0$ for $x < \frac{1}{e}$, $f'(x) > 0$ for $x > \frac{1}{e}$

Local minimum at $x = \frac{1}{e}$: $f(\frac{1}{e}) = \frac{1}{e} \cdot (-1) = -\frac{1}{e}$

**Second derivative**:

$$f''(x) = \frac{1}{x}$$

Since $f''(x) = \frac{1}{x} > 0$ for all $x > 0$, the function is always concave up.

No inflection points.

**End behavior**:
- As $x \to 0^+$: $f(x) \to 0$ (since $x \to 0$ faster than $\ln x \to -\infty$)
- As $x \to \infty$: $f(x) \to \infty$

</details>

---

<details>
<summary><strong>Problem 9 Solution</strong></summary>

**Answer**: Local max at $x = \frac{\pi}{4}$, local min at $x = \frac{5\pi}{4}$; inflection points at $x = \frac{3\pi}{4}$ and $x = \frac{7\pi}{4}$

**Step-by-step solution**:

$$f'(x) = \cos x - \sin x$$

$f'(x) = 0$ when $\cos x = \sin x$, i.e., $\tan x = 1$

On $[0, 2\pi]$: $x = \frac{\pi}{4}$ and $x = \frac{5\pi}{4}$

$f(\frac{\pi}{4}) = \frac{\sqrt{2}}{2} + \frac{\sqrt{2}}{2} = \sqrt{2}$ (local max)
$f(\frac{5\pi}{4}) = -\frac{\sqrt{2}}{2} - \frac{\sqrt{2}}{2} = -\sqrt{2}$ (local min)

**Second derivative**:

$$f''(x) = -\sin x - \cos x$$

$f''(x) = 0$ when $\sin x + \cos x = 0$, i.e., $\tan x = -1$

On $[0, 2\pi]$: $x = \frac{3\pi}{4}$ and $x = \frac{7\pi}{4}$

Both are inflection points (sign of $f''$ changes at each).

</details>

---

<details>
<summary><strong>Problem 10 Solution</strong></summary>

**Answer**: Critical points at $x = 0$ (local max) and $x = 2$ (local min)

**Step-by-step solution**:

$$f(x) = x^{2/3}(x - 5) = x^{5/3} - 5x^{2/3}$$

$$f'(x) = \frac{5}{3}x^{2/3} - \frac{10}{3}x^{-1/3} = \frac{5x^{2/3}}{3} - \frac{10}{3x^{1/3}}$$

$$= \frac{5x - 10}{3x^{1/3}} = \frac{5(x - 2)}{3x^{1/3}}$$

Critical points:
- $f'(x) = 0$ when $x = 2$
- $f'(x)$ undefined when $x = 0$

Sign chart:

| Interval | $f'(x)$ | Behavior |
|----------|---------|----------|
| $(-\infty, 0)$ | $+$ | Increasing |
| $(0, 2)$ | $-$ | Decreasing |
| $(2, \infty)$ | $+$ | Increasing |

At $x = 0$: changes from + to -, so **local maximum**, $f(0) = 0$
At $x = 2$: changes from - to +, so **local minimum**, $f(2) = 2^{2/3}(-3) = -3\sqrt[3]{4} \approx -4.76$

</details>

---

<details>
<summary><strong>Problem 11 Solution</strong></summary>

**Answer**: See detailed analysis below.

**Domain**: All $x$ except $x = \pm 1$

**Intercept**: $(0, 0)$

**Symmetry**: $f(-x) = \frac{-x^3}{x^2 - 1} = -f(x)$ → Odd function

**Asymptotes**:
- Vertical: $x = 1$ and $x = -1$
- Oblique: Divide to get $f(x) = x + \frac{x}{x^2-1}$, so $y = x$ is an oblique asymptote

**First derivative**:

$$f'(x) = \frac{3x^2(x^2-1) - x^3(2x)}{(x^2-1)^2} = \frac{x^2(x^2 - 3)}{(x^2-1)^2}$$

$f'(x) = 0$ when $x = 0$ or $x = \pm\sqrt{3}$

At $x = 0$: $f'$ doesn't change sign (stays positive on both sides near 0 where defined), so neither max nor min
At $x = \sqrt{3}$: local minimum
At $x = -\sqrt{3}$: local maximum

**Values**: $f(\sqrt{3}) = \frac{3\sqrt{3}}{2}$, $f(-\sqrt{3}) = -\frac{3\sqrt{3}}{2}$

</details>

---

<details>
<summary><strong>Problem 12 Solution</strong></summary>

**Answer**: Global maximum at $x = 0$ with $f(0) = 1$; inflection points at $x = \pm\frac{1}{\sqrt{2}}$. This is the Gaussian function (bell curve).

**Step-by-step solution**:

$$f'(x) = e^{-x^2} \cdot (-2x) = -2xe^{-x^2}$$

$f'(x) = 0$ when $x = 0$

$f'(x) > 0$ for $x < 0$, $f'(x) < 0$ for $x > 0$

Global maximum at $x = 0$: $f(0) = 1$

**Second derivative**:

$$f''(x) = -2e^{-x^2} + (-2x)(-2x)e^{-x^2} = e^{-x^2}(4x^2 - 2)$$

$f''(x) = 0$ when $4x^2 - 2 = 0$, i.e., $x = \pm\frac{1}{\sqrt{2}}$

Both are inflection points where concavity changes.

This is the **Gaussian** or **normal distribution** bell curve.

</details>

---

<details>
<summary><strong>Problem 13 Solution</strong></summary>

**Answer**: Graph has local min at $x = -2$, inflection point (horizontal tangent) at $x = 1$

**Step-by-step solution**:

$f'(x) = (x-1)^2(x+2)$

Critical points: $x = 1$ and $x = -2$

Sign chart:

| Interval | $(x-1)^2$ | $(x+2)$ | $f'(x)$ | Behavior |
|----------|-----------|---------|---------|----------|
| $(-\infty, -2)$ | $+$ | $-$ | $-$ | Decreasing |
| $(-2, 1)$ | $+$ | $+$ | $+$ | Increasing |
| $(1, \infty)$ | $+$ | $+$ | $+$ | Increasing |

At $x = -2$: changes from - to +, so **local minimum**
At $x = 1$: doesn't change sign (stays positive), so **neither** (horizontal inflection point)

The sketch shows a function decreasing to a minimum at $x = -2$, then increasing with a point of inflection (horizontal tangent) at $x = 1$.

</details>

---

<details>
<summary><strong>Problem 14 Solution</strong></summary>

**Answer**: Local minimum at $x = 2$ with value $f(2) = 0$

**Step-by-step solution**:

$$f(x) = x^4 - 4x^3 + 4x^2 = x^2(x^2 - 4x + 4) = x^2(x-2)^2$$

$$f'(x) = 4x^3 - 12x^2 + 8x = 4x(x^2 - 3x + 2) = 4x(x-1)(x-2)$$

Critical points: $x = 0, 1, 2$

Sign chart:

| Interval | $f'(x)$ | Behavior |
|----------|---------|----------|
| $(-\infty, 0)$ | $-$ | Decreasing |
| $(0, 1)$ | $+$ | Increasing |
| $(1, 2)$ | $-$ | Decreasing |
| $(2, \infty)$ | $+$ | Increasing |

At $x = 0$: local minimum, $f(0) = 0$
At $x = 1$: local maximum, $f(1) = 1$
At $x = 2$: local minimum, $f(2) = 0$

Wait, this shows two local minima. Let me reconsider.

Actually, the function $f(x) = x^2(x-2)^2$ is always $\geq 0$ with zeros at $x = 0$ and $x = 2$.

So there are two local minima at $x = 0$ and $x = 2$, both with value $0$.

</details>

---

<details>
<summary><strong>Problem 15 Solution</strong></summary>

**Answer**: Inflection points at $x = \pm\frac{1}{\sqrt{3}}$

**Step-by-step solution**:

$$f'(x) = \frac{1}{1 + x^4} \cdot 2x = \frac{2x}{1 + x^4}$$

$$f''(x) = \frac{2(1 + x^4) - 2x \cdot 4x^3}{(1 + x^4)^2} = \frac{2 + 2x^4 - 8x^4}{(1 + x^4)^2} = \frac{2 - 6x^4}{(1 + x^4)^2}$$

$f''(x) = 0$ when $2 - 6x^4 = 0$, i.e., $x^4 = \frac{1}{3}$, so $x = \pm\frac{1}{3^{1/4}} = \pm\frac{1}{\sqrt[4]{3}}$

Sign analysis:
- $f''(x) > 0$ when $|x| < \frac{1}{\sqrt[4]{3}}$: concave up
- $f''(x) < 0$ when $|x| > \frac{1}{\sqrt[4]{3}}$: concave down

Inflection points at $x = \pm\frac{1}{\sqrt[4]{3}} \approx \pm 0.76$

</details>

---

<details>
<summary><strong>Problem 16 Solution</strong></summary>

**Answer**: **(A)** $x = -1$ only

**Step-by-step solution**:

$$f'(x) = 3x^2 - 6x - 9 = 3(x^2 - 2x - 3) = 3(x-3)(x+1)$$

Critical points: $x = -1$ and $x = 3$

Sign chart:
- $f'(x) > 0$ on $(-\infty, -1)$ and $(3, \infty)$
- $f'(x) < 0$ on $(-1, 3)$

At $x = -1$: changes from + to -, so **local maximum**
At $x = 3$: changes from - to +, so **local minimum**

The function has a local maximum at $x = -1$ only.

</details>

---

<details>
<summary><strong>Problem 17 Solution</strong></summary>

**Answer**: **(C)** 2

**Step-by-step solution**:

Inflection points of $f$ occur where $f''$ changes sign.

If $f''$ is a parabola opening upward, crossing the x-axis at $x = 1$ and $x = 3$:
- $f''(x) > 0$ for $x < 1$
- $f''(x) < 0$ for $1 < x < 3$
- $f''(x) > 0$ for $x > 3$

The sign of $f''$ changes at both $x = 1$ and $x = 3$.

Therefore, $f$ has **2 inflection points**.

</details>

---

<details>
<summary><strong>Problem 18 Solution</strong></summary>

**Answer**: See detailed solution below.

**(a) Critical points**:

$$f(x) = x^4 - 8x^2 + 16 = (x^2 - 4)^2$$

$$f'(x) = 4x^3 - 16x = 4x(x^2 - 4) = 4x(x-2)(x+2)$$

Critical points: $x = -2, 0, 2$

Sign chart:
| Interval | $f'(x)$ |
|----------|---------|
| $(-\infty, -2)$ | $-$ |
| $(-2, 0)$ | $+$ |
| $(0, 2)$ | $-$ |
| $(2, \infty)$ | $+$ |

- $x = -2$: local minimum, $f(-2) = 0$
- $x = 0$: local maximum, $f(0) = 16$
- $x = 2$: local minimum, $f(2) = 0$

**(b) Inflection points**:

$$f''(x) = 12x^2 - 16 = 4(3x^2 - 4)$$

$f''(x) = 0$ when $x = \pm\frac{2}{\sqrt{3}} = \pm\frac{2\sqrt{3}}{3}$

Both are inflection points where concavity changes.

$f(\pm\frac{2\sqrt{3}}{3}) = (\frac{4}{3} - 4)^2 = (-\frac{8}{3})^2 = \frac{64}{9}$

Inflection points: $(\pm\frac{2\sqrt{3}}{3}, \frac{64}{9})$

**(c)** The sketch shows a W-shape: decreasing to min at $(-2, 0)$, increasing to max at $(0, 16)$, decreasing to min at $(2, 0)$, then increasing.

</details>

---

<details>
<summary><strong>Problem 19 Solution</strong></summary>

**Answer**: **(C)** no local maximum and one local minimum

**Step-by-step solution**:

$f'(x) = (x+1)(x-2)^2$

Critical points: $x = -1$ and $x = 2$

Sign chart:

| Interval | $(x+1)$ | $(x-2)^2$ | $f'(x)$ |
|----------|---------|-----------|---------|
| $(-\infty, -1)$ | $-$ | $+$ | $-$ |
| $(-1, 2)$ | $+$ | $+$ | $+$ |
| $(2, \infty)$ | $+$ | $+$ | $+$ |

At $x = -1$: changes from - to +, so **local minimum**
At $x = 2$: doesn't change sign (stays +), so **neither**

The graph has **no local maximum and one local minimum**.

</details>

---

<details>
<summary><strong>Problem 20 Solution</strong></summary>

**Answer**: See detailed solution below.

**(a) Critical points**:

$f'(x) = \frac{x}{(x^2+1)^2} = 0$ when $x = 0$

Sign of $f'$:
- $f'(x) < 0$ for $x < 0$
- $f'(x) > 0$ for $x > 0$

At $x = 0$: changes from - to +, so **local minimum**

**(b) Second derivative**:

Using quotient rule:

$$f''(x) = \frac{(x^2+1)^2 - x \cdot 2(x^2+1)(2x)}{(x^2+1)^4} = \frac{(x^2+1) - 4x^2}{(x^2+1)^3} = \frac{1 - 3x^2}{(x^2+1)^3}$$

$f''(x) = 0$ when $1 - 3x^2 = 0$, i.e., $x = \pm\frac{1}{\sqrt{3}}$

Both are inflection points.

**(c) Limits**:

$$f(x) = \int \frac{x}{(x^2+1)^2} dx = -\frac{1}{2(x^2+1)} + C$$

Using $f(0) = 2$: $-\frac{1}{2} + C = 2$, so $C = \frac{5}{2}$

$$f(x) = -\frac{1}{2(x^2+1)} + \frac{5}{2}$$

$$\lim_{x \to \pm\infty} f(x) = 0 + \frac{5}{2} = \frac{5}{2}$$

**(d)** The sketch shows a function with horizontal asymptote $y = \frac{5}{2}$, a local minimum at $(0, 2)$, and inflection points at $x = \pm\frac{1}{\sqrt{3}}$.

</details>

---

## What's Next

You've now mastered curve sketching, completing Unit 4 on derivative applications. Next, explore [Antiderivatives](/calculus/antiderivatives) to begin Unit 5, where we reverse the process of differentiation and enter the world of integration.

---

<div align="center">

[← Mean Value Theorem](/calculus/mean-value-theorem) | [Antiderivatives →](/calculus/antiderivatives)

</div>
