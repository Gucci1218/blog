# The Definition of the Derivative
<p class="article-date">December 3, 2024</p>

## Learning Objectives

By the end of this article, you will be able to:

- Understand the derivative as the limit of average rates of change
- Apply the limit definition of the derivative at a point
- Use the limit definition to find the derivative function
- Interpret the derivative as the slope of a tangent line
- Distinguish between average and instantaneous rates of change
- Determine when a function is differentiable at a point
- Understand the relationship between differentiability and continuity
- Solve AP Calculus problems using the definition of the derivative

---

## The Core Concept: From Average to Instantaneous

### The Speedometer Problem

Imagine you're driving a car and glance at your speedometer. It reads 60 mph. But what does "60 miles per hour" actually mean at that exact instant?

**Here's the puzzle:** Speed is distance divided by time. But at a single instant:
- You travel zero distance (no time passes)
- Zero time elapses

So speed = $\frac{0}{0}$... which is undefined!

Yet your speedometer shows a real number. How?

**The answer:** The speedometer doesn't measure speed at an instant directly. It measures your position over a tiny time interval and computes the average speed. As that interval gets smaller and smaller, the average speed approaches what we call the **instantaneous speed**.

This is exactly what a derivative does—it captures the instantaneous rate of change by taking a limit of average rates of change.

### From Secant Lines to Tangent Lines

Let's visualize this geometrically.

**Average Rate of Change = Slope of a Secant Line**

Given a function $f(x)$, pick two points on the curve:
- Point 1: $(a, f(a))$
- Point 2: $(a + h, f(a + h))$

The **secant line** connects these two points. Its slope is:

$$\text{Average Rate of Change} = \frac{f(a + h) - f(a)}{(a + h) - a} = \frac{f(a + h) - f(a)}{h}$$

This ratio is called the **difference quotient**.

```
      y
      |
      |           • (a+h, f(a+h))
      |          /|
      |         / |
      |        /  | rise = f(a+h) - f(a)
      |       /   |
      |      • (a, f(a))
      |      |____|
      |       run = h
      |_________________________ x
            a   a+h
```

**Instantaneous Rate of Change = Slope of the Tangent Line**

Now, what happens as we slide the second point closer to the first? As $h \to 0$:
- The two points get closer together
- The secant line rotates toward a limiting position
- That limiting position is the **tangent line**

```
        Secant lines approaching tangent:

               /
              /• (approaching point)
             /
            / ← secant rotates
           /
          •← fixed point
         /
        / ← tangent line (limit position)
```

The slope of the tangent line is the **derivative**.

---

## The Limit Definition of the Derivative

### Definition at a Point

The **derivative of $f$ at $x = a$**, denoted $f'(a)$, is defined as:

$$\boxed{f'(a) = \lim_{h \to 0} \frac{f(a + h) - f(a)}{h}}$$

provided this limit exists.

**In words:** The derivative at a point is the limit of the difference quotient as the interval shrinks to zero.

### Alternative Form (Using $x$ Instead of $h$)

Sometimes it's convenient to use a different form. If we let $x$ be the variable point approaching $a$:

$$\boxed{f'(a) = \lim_{x \to a} \frac{f(x) - f(a)}{x - a}}$$

This is equivalent to the first form (substitute $x = a + h$, so $h = x - a$).

### The Derivative as a Function

Instead of finding the derivative at one specific point, we can find a formula that works for any $x$:

$$\boxed{f'(x) = \lim_{h \to 0} \frac{f(x + h) - f(x)}{h}}$$

This gives us the **derivative function** $f'(x)$, which tells us the instantaneous rate of change at any point in the domain.

### Notation for Derivatives

There are several equivalent notations:

| Notation | Read as | When to use |
|----------|---------|-------------|
| $f'(x)$ | "f prime of x" | General use |
| $\frac{dy}{dx}$ | "dy dx" or "the derivative of y with respect to x" | Emphasizing variables |
| $\frac{df}{dx}$ | "df dx" | Same as above |
| $\frac{d}{dx}[f(x)]$ | "d dx of f of x" | Operator notation |
| $y'$ | "y prime" | Quick notation |
| $Df(x)$ | "D of f of x" | Operator notation |

At a specific point $x = a$:
- $f'(a)$
- $\frac{dy}{dx}\bigg|_{x=a}$
- $\frac{df}{dx}(a)$

---

## Understanding the Difference Quotient

### Breaking It Down

The difference quotient $\frac{f(x+h) - f(x)}{h}$ has three parts:

1. **$f(x+h)$**: The function value at a point slightly to the right
2. **$f(x)$**: The function value at the original point
3. **$h$**: The horizontal distance between the points (can be positive or negative)

**The numerator** $f(x+h) - f(x)$ = "rise" = change in $y$

**The denominator** $h$ = "run" = change in $x$

**The ratio** = slope of the secant line

### Visualizing $h$ Approaching Zero

```
h = 1:                  h = 0.5:                h → 0:
      •                       •                      • ← tangent
     /                       /                      /
    /  secant               / secant               /
   /                       /                      /
  •                       •                      •
  |_____|                 |__|                   |
  h = 1                   h = 0.5               tangent
```

As $h$ gets smaller, the secant line gets closer to the tangent line.

---

## Worked Examples: Finding Derivatives Using the Definition

### Example 1: A Linear Function

**Find $f'(x)$ for $f(x) = 3x + 2$ using the definition.**

**Solution:**

$$f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$$

**Step 1:** Find $f(x + h)$.
$$f(x + h) = 3(x + h) + 2 = 3x + 3h + 2$$

**Step 2:** Compute the difference quotient.
$$\frac{f(x+h) - f(x)}{h} = \frac{(3x + 3h + 2) - (3x + 2)}{h} = \frac{3h}{h} = 3$$

**Step 3:** Take the limit.
$$f'(x) = \lim_{h \to 0} 3 = 3$$

**Answer:** $f'(x) = 3$

**Interpretation:** The slope of $y = 3x + 2$ is 3 everywhere. This makes sense—linear functions have constant slope!

---

### Example 2: A Quadratic Function

**Find $f'(x)$ for $f(x) = x^2$ using the definition.**

**Solution:**

$$f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$$

**Step 1:** Find $f(x + h)$.
$$f(x + h) = (x + h)^2 = x^2 + 2xh + h^2$$

**Step 2:** Compute the difference quotient.
$$\frac{f(x+h) - f(x)}{h} = \frac{(x^2 + 2xh + h^2) - x^2}{h} = \frac{2xh + h^2}{h}$$

**Step 3:** Simplify (factor out $h$).
$$\frac{2xh + h^2}{h} = \frac{h(2x + h)}{h} = 2x + h$$

**Step 4:** Take the limit.
$$f'(x) = \lim_{h \to 0} (2x + h) = 2x$$

**Answer:** $f'(x) = 2x$

**Interpretation:**
- At $x = 0$: slope = $2(0) = 0$ (horizontal tangent at vertex)
- At $x = 1$: slope = $2(1) = 2$
- At $x = -2$: slope = $2(-2) = -4$

The slope of $x^2$ increases as you move right and decreases as you move left.

---

### Example 3: A Cubic Function

**Find $f'(2)$ for $f(x) = x^3$ using the definition.**

**Solution:**

$$f'(2) = \lim_{h \to 0} \frac{f(2+h) - f(2)}{h}$$

**Step 1:** Find $f(2 + h)$ and $f(2)$.
$$f(2 + h) = (2 + h)^3 = 8 + 12h + 6h^2 + h^3$$
$$f(2) = 2^3 = 8$$

**Step 2:** Compute the difference quotient.
$$\frac{f(2+h) - f(2)}{h} = \frac{(8 + 12h + 6h^2 + h^3) - 8}{h} = \frac{12h + 6h^2 + h^3}{h}$$

**Step 3:** Simplify.
$$\frac{12h + 6h^2 + h^3}{h} = \frac{h(12 + 6h + h^2)}{h} = 12 + 6h + h^2$$

**Step 4:** Take the limit.
$$f'(2) = \lim_{h \to 0} (12 + 6h + h^2) = 12$$

**Answer:** $f'(2) = 12$

---

### Example 4: A Square Root Function

**Find $f'(x)$ for $f(x) = \sqrt{x}$ using the definition.**

**Solution:**

$$f'(x) = \lim_{h \to 0} \frac{\sqrt{x+h} - \sqrt{x}}{h}$$

**Step 1:** This gives $\frac{0}{0}$ directly. Rationalize the numerator by multiplying by the conjugate.

$$\frac{\sqrt{x+h} - \sqrt{x}}{h} \cdot \frac{\sqrt{x+h} + \sqrt{x}}{\sqrt{x+h} + \sqrt{x}}$$

**Step 2:** Simplify the numerator using $(a-b)(a+b) = a^2 - b^2$.
$$= \frac{(x+h) - x}{h(\sqrt{x+h} + \sqrt{x})} = \frac{h}{h(\sqrt{x+h} + \sqrt{x})} = \frac{1}{\sqrt{x+h} + \sqrt{x}}$$

**Step 3:** Take the limit.
$$f'(x) = \lim_{h \to 0} \frac{1}{\sqrt{x+h} + \sqrt{x}} = \frac{1}{\sqrt{x} + \sqrt{x}} = \frac{1}{2\sqrt{x}}$$

**Answer:** $f'(x) = \frac{1}{2\sqrt{x}}$

**Note:** The domain of $f'$ is $x > 0$ (not $x \geq 0$) because the derivative doesn't exist at $x = 0$.

---

### Example 5: A Rational Function

**Find $f'(x)$ for $f(x) = \frac{1}{x}$ using the definition.**

**Solution:**

$$f'(x) = \lim_{h \to 0} \frac{\frac{1}{x+h} - \frac{1}{x}}{h}$$

**Step 1:** Combine the fractions in the numerator.
$$\frac{1}{x+h} - \frac{1}{x} = \frac{x - (x+h)}{x(x+h)} = \frac{-h}{x(x+h)}$$

**Step 2:** Divide by $h$.
$$\frac{\frac{-h}{x(x+h)}}{h} = \frac{-h}{x(x+h)} \cdot \frac{1}{h} = \frac{-1}{x(x+h)}$$

**Step 3:** Take the limit.
$$f'(x) = \lim_{h \to 0} \frac{-1}{x(x+h)} = \frac{-1}{x \cdot x} = -\frac{1}{x^2}$$

**Answer:** $f'(x) = -\frac{1}{x^2}$

---

### Example 6: Using the Alternative Form

**Find $f'(3)$ for $f(x) = x^2 + x$ using the alternative definition.**

**Solution:**

$$f'(3) = \lim_{x \to 3} \frac{f(x) - f(3)}{x - 3}$$

**Step 1:** Find $f(3)$.
$$f(3) = 9 + 3 = 12$$

**Step 2:** Set up the difference quotient.
$$\frac{f(x) - f(3)}{x - 3} = \frac{(x^2 + x) - 12}{x - 3} = \frac{x^2 + x - 12}{x - 3}$$

**Step 3:** Factor the numerator.
$$x^2 + x - 12 = (x + 4)(x - 3)$$

**Step 4:** Simplify and take the limit.
$$\frac{(x+4)(x-3)}{x-3} = x + 4$$
$$f'(3) = \lim_{x \to 3} (x + 4) = 7$$

**Answer:** $f'(3) = 7$

---

## Differentiability

### When Does the Derivative Exist?

A function $f$ is **differentiable at $x = a$** if $f'(a)$ exists—that is, if

$$\lim_{h \to 0} \frac{f(a+h) - f(a)}{h}$$

exists as a finite number.

### When is a Function NOT Differentiable?

The derivative fails to exist in these cases:

**1. Corner or Cusp (Sharp Turn)**

At a corner, the left and right tangent lines have different slopes.

```
       /\            Example: f(x) = |x| at x = 0
      /  \
     /    \          Left slope = -1
    /      \         Right slope = +1
```

$$f'(0) = \lim_{h \to 0^+} \frac{|h| - 0}{h} = 1$$
$$f'(0) = \lim_{h \to 0^-} \frac{|h| - 0}{h} = -1$$

Since left ≠ right, the derivative doesn't exist.

**2. Vertical Tangent**

If the tangent line is vertical, the slope is undefined (infinite).

```
       |             Example: f(x) = ∛x at x = 0
       |
    ___|___          The curve has a vertical tangent
       |             Slope → ∞
       |
```

$$f'(0) = \lim_{h \to 0} \frac{\sqrt[3]{h} - 0}{h} = \lim_{h \to 0} \frac{1}{h^{2/3}} = \infty$$

**3. Discontinuity**

If $f$ is not continuous at $a$, then $f$ is not differentiable at $a$.

```
       •             Example: jump discontinuity
       |
    ---|---○         Can't draw a tangent line
                     across a jump
```

### The Differentiability-Continuity Relationship

$$\boxed{\text{Differentiable at } a \implies \text{Continuous at } a}$$

**In words:** If a function is differentiable at a point, it must be continuous there.

**The converse is FALSE:** Continuous does NOT imply differentiable.

**Counterexample:** $f(x) = |x|$ is continuous at $x = 0$ but not differentiable there.

**Proof that differentiability implies continuity:**

If $f$ is differentiable at $a$, then $f'(a)$ exists. We need to show $\lim_{x \to a} f(x) = f(a)$.

$$\lim_{x \to a} [f(x) - f(a)] = \lim_{x \to a} \frac{f(x) - f(a)}{x - a} \cdot (x - a)$$
$$= f'(a) \cdot 0 = 0$$

So $\lim_{x \to a} f(x) = f(a)$, which means $f$ is continuous at $a$.

### Summary of Differentiability

| Condition | Continuous? | Differentiable? |
|-----------|-------------|-----------------|
| Smooth curve | Yes | Yes |
| Corner/cusp | Yes | No |
| Vertical tangent | Yes | No |
| Jump discontinuity | No | No |
| Removable discontinuity | No | No |

---

## Worked Examples: Differentiability

### Example 7: Checking Differentiability at a Corner

**Is $f(x) = |x - 2|$ differentiable at $x = 2$?**

**Solution:**

Check if $\lim_{h \to 0} \frac{f(2+h) - f(2)}{h}$ exists.

$$f(2) = |2 - 2| = 0$$

**Right-hand limit ($h > 0$):**
$$\lim_{h \to 0^+} \frac{|2 + h - 2| - 0}{h} = \lim_{h \to 0^+} \frac{|h|}{h} = \lim_{h \to 0^+} \frac{h}{h} = 1$$

**Left-hand limit ($h < 0$):**
$$\lim_{h \to 0^-} \frac{|2 + h - 2| - 0}{h} = \lim_{h \to 0^-} \frac{|h|}{h} = \lim_{h \to 0^-} \frac{-h}{h} = -1$$

Since $1 \neq -1$, the limit doesn't exist.

**Answer:** $f$ is **not differentiable** at $x = 2$.

---

### Example 8: Piecewise Function Differentiability

**For $f(x) = \begin{cases} x^2 & \text{if } x \leq 1 \\ 2x - 1 & \text{if } x > 1 \end{cases}$, is $f$ differentiable at $x = 1$?**

**Solution:**

**Step 1:** Check continuity first.
- $f(1) = 1^2 = 1$
- $\lim_{x \to 1^-} x^2 = 1$
- $\lim_{x \to 1^+} (2x - 1) = 1$

Yes, $f$ is continuous at $x = 1$.

**Step 2:** Check if the derivative exists.

**From the left:** $\frac{d}{dx}(x^2) = 2x$, so the left derivative at $x = 1$ is $2(1) = 2$.

**From the right:** $\frac{d}{dx}(2x - 1) = 2$, so the right derivative at $x = 1$ is $2$.

Since both one-sided derivatives equal 2, the derivative exists.

**Answer:** $f$ is **differentiable** at $x = 1$, with $f'(1) = 2$.

---

### Example 9: Where is a Function Not Differentiable?

**Find all points where $g(x) = |x^2 - 4|$ is not differentiable.**

**Solution:**

The expression inside the absolute value equals zero when:
$$x^2 - 4 = 0 \implies x = \pm 2$$

At these points, the function potentially has corners.

Rewrite without absolute value:
$$g(x) = \begin{cases} x^2 - 4 & \text{if } x \leq -2 \text{ or } x \geq 2 \\ -(x^2 - 4) = 4 - x^2 & \text{if } -2 < x < 2 \end{cases}$$

**At $x = 2$:**
- Left derivative: $\frac{d}{dx}(4 - x^2) = -2x \to -4$ at $x = 2$
- Right derivative: $\frac{d}{dx}(x^2 - 4) = 2x \to 4$ at $x = 2$
- $-4 \neq 4$, so not differentiable at $x = 2$

**At $x = -2$:**
- Left derivative: $\frac{d}{dx}(x^2 - 4) = 2x \to -4$ at $x = -2$
- Right derivative: $\frac{d}{dx}(4 - x^2) = -2x \to 4$ at $x = -2$
- $-4 \neq 4$, so not differentiable at $x = -2$

**Answer:** $g$ is not differentiable at $x = -2$ and $x = 2$.

---

## Interpreting the Derivative

### Physical Interpretation: Velocity

If $s(t)$ is the position of an object at time $t$, then:

- **Average velocity** over $[t, t+h]$: $\frac{s(t+h) - s(t)}{h}$
- **Instantaneous velocity** at time $t$: $v(t) = s'(t) = \lim_{h \to 0} \frac{s(t+h) - s(t)}{h}$

### Graphical Interpretation: Tangent Line Slope

$f'(a)$ = slope of the tangent line to $y = f(x)$ at the point $(a, f(a))$

### General Interpretation: Rate of Change

For any quantity $y = f(x)$:
- $f'(x)$ is the **instantaneous rate of change** of $y$ with respect to $x$
- Units of $f'(x)$ = (units of $y$) / (units of $x$)

---

## Practice Problems

### Basic Problems (1-5)

**1.** Use the definition of the derivative to find $f'(x)$ for $f(x) = 5x - 3$.

---

**2.** Use the definition to find $f'(x)$ for $f(x) = x^2 + 4x$.

---

**3.** Use the definition to find $f'(2)$ for $f(x) = x^2 - 3x + 1$.

---

**4.** Use the alternative form $\lim_{x \to a} \frac{f(x) - f(a)}{x - a}$ to find $f'(4)$ for $f(x) = \sqrt{x}$.

---

**5.** Is $f(x) = |x + 1|$ differentiable at $x = -1$? Explain.

---

### Intermediate Problems (6-10)

**6.** Use the definition to find $f'(x)$ for $f(x) = x^3 - 2x$.

---

**7.** Use the definition to find $f'(x)$ for $f(x) = \frac{1}{x + 1}$.

---

**8.** Use the definition to find $f'(x)$ for $f(x) = \sqrt{2x + 1}$.

---

**9.** For $g(x) = \begin{cases} x^2 + 1 & \text{if } x \leq 2 \\ 4x - 3 & \text{if } x > 2 \end{cases}$, determine if $g$ is differentiable at $x = 2$.

---

**10.** Find all points where $h(x) = |x^2 - 1|$ is not differentiable.

---

### Advanced Problems (11-15)

**11.** Use the definition to find $f'(x)$ for $f(x) = \frac{x}{x + 2}$.

---

**12.** Find the value of $k$ such that $f(x) = \begin{cases} kx^2 & \text{if } x \leq 1 \\ x + 2 & \text{if } x > 1 \end{cases}$ is differentiable at $x = 1$.

---

**13.** The position of a particle is given by $s(t) = t^2 - 4t + 3$. Use the definition to find the velocity at $t = 3$.

---

**14.** Use the definition to show that $f(x) = x^{2/3}$ is not differentiable at $x = 0$.

---

**15.** Find $f'(0)$ for $f(x) = x^2 \sin\left(\frac{1}{x}\right)$ for $x \neq 0$ and $f(0) = 0$ using the definition.

---

### Challenge Problems (16-18)

**16.** Prove that if $f(x) = x^n$ for positive integer $n$, then $f'(x) = nx^{n-1}$ using the definition and the binomial theorem.

---

**17.** Find values of $a$ and $b$ such that $f(x) = \begin{cases} ax^2 + bx & \text{if } x < 1 \\ x^3 & \text{if } x \geq 1 \end{cases}$ is differentiable everywhere.

---

**18.** Let $f(x) = \begin{cases} x^2 & \text{if } x \in \mathbb{Q} \\ 0 & \text{if } x \notin \mathbb{Q} \end{cases}$. Is $f$ differentiable at $x = 0$? Prove your answer.

---

## Solutions to Practice Problems

### Solution 1

$$f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h} = \lim_{h \to 0} \frac{[5(x+h) - 3] - [5x - 3]}{h}$$

$$= \lim_{h \to 0} \frac{5x + 5h - 3 - 5x + 3}{h} = \lim_{h \to 0} \frac{5h}{h} = \lim_{h \to 0} 5 = 5$$

**Answer:** $f'(x) = 5$

---

### Solution 2

$$f'(x) = \lim_{h \to 0} \frac{[(x+h)^2 + 4(x+h)] - [x^2 + 4x]}{h}$$

$$= \lim_{h \to 0} \frac{x^2 + 2xh + h^2 + 4x + 4h - x^2 - 4x}{h}$$

$$= \lim_{h \to 0} \frac{2xh + h^2 + 4h}{h} = \lim_{h \to 0} \frac{h(2x + h + 4)}{h}$$

$$= \lim_{h \to 0} (2x + h + 4) = 2x + 4$$

**Answer:** $f'(x) = 2x + 4$

---

### Solution 3

$$f'(2) = \lim_{h \to 0} \frac{f(2+h) - f(2)}{h}$$

First, find $f(2) = 4 - 6 + 1 = -1$.

$$f(2+h) = (2+h)^2 - 3(2+h) + 1 = 4 + 4h + h^2 - 6 - 3h + 1 = -1 + h + h^2$$

$$f'(2) = \lim_{h \to 0} \frac{(-1 + h + h^2) - (-1)}{h} = \lim_{h \to 0} \frac{h + h^2}{h} = \lim_{h \to 0} (1 + h) = 1$$

**Answer:** $f'(2) = 1$

---

### Solution 4

$$f'(4) = \lim_{x \to 4} \frac{\sqrt{x} - \sqrt{4}}{x - 4} = \lim_{x \to 4} \frac{\sqrt{x} - 2}{x - 4}$$

Rationalize:
$$= \lim_{x \to 4} \frac{\sqrt{x} - 2}{x - 4} \cdot \frac{\sqrt{x} + 2}{\sqrt{x} + 2} = \lim_{x \to 4} \frac{x - 4}{(x - 4)(\sqrt{x} + 2)}$$

$$= \lim_{x \to 4} \frac{1}{\sqrt{x} + 2} = \frac{1}{\sqrt{4} + 2} = \frac{1}{4}$$

**Answer:** $f'(4) = \frac{1}{4}$

---

### Solution 5

Check the one-sided limits:

**Right-hand:** $\lim_{h \to 0^+} \frac{|(-1+h) + 1|}{h} = \lim_{h \to 0^+} \frac{h}{h} = 1$

**Left-hand:** $\lim_{h \to 0^-} \frac{|(-1+h) + 1|}{h} = \lim_{h \to 0^-} \frac{|h|}{h} = \lim_{h \to 0^-} \frac{-h}{h} = -1$

Since $1 \neq -1$, the limit doesn't exist.

**Answer:** No, $f$ is not differentiable at $x = -1$.

---

### Solution 6

$$f'(x) = \lim_{h \to 0} \frac{[(x+h)^3 - 2(x+h)] - [x^3 - 2x]}{h}$$

Expand $(x+h)^3 = x^3 + 3x^2h + 3xh^2 + h^3$:

$$= \lim_{h \to 0} \frac{x^3 + 3x^2h + 3xh^2 + h^3 - 2x - 2h - x^3 + 2x}{h}$$

$$= \lim_{h \to 0} \frac{3x^2h + 3xh^2 + h^3 - 2h}{h} = \lim_{h \to 0} (3x^2 + 3xh + h^2 - 2) = 3x^2 - 2$$

**Answer:** $f'(x) = 3x^2 - 2$

---

### Solution 7

$$f'(x) = \lim_{h \to 0} \frac{\frac{1}{x+h+1} - \frac{1}{x+1}}{h}$$

Combine fractions:
$$\frac{1}{x+h+1} - \frac{1}{x+1} = \frac{(x+1) - (x+h+1)}{(x+h+1)(x+1)} = \frac{-h}{(x+h+1)(x+1)}$$

Divide by $h$:
$$\frac{-h}{h(x+h+1)(x+1)} = \frac{-1}{(x+h+1)(x+1)}$$

Take the limit:
$$f'(x) = \lim_{h \to 0} \frac{-1}{(x+h+1)(x+1)} = \frac{-1}{(x+1)^2}$$

**Answer:** $f'(x) = -\frac{1}{(x+1)^2}$

---

### Solution 8

$$f'(x) = \lim_{h \to 0} \frac{\sqrt{2(x+h)+1} - \sqrt{2x+1}}{h}$$

Rationalize:
$$= \lim_{h \to 0} \frac{[2(x+h)+1] - [2x+1]}{h(\sqrt{2x+2h+1} + \sqrt{2x+1})}$$

$$= \lim_{h \to 0} \frac{2h}{h(\sqrt{2x+2h+1} + \sqrt{2x+1})} = \lim_{h \to 0} \frac{2}{\sqrt{2x+2h+1} + \sqrt{2x+1}}$$

$$= \frac{2}{2\sqrt{2x+1}} = \frac{1}{\sqrt{2x+1}}$$

**Answer:** $f'(x) = \frac{1}{\sqrt{2x+1}}$

---

### Solution 9

**Check continuity:**
- $g(2) = 4 + 1 = 5$
- $\lim_{x \to 2^-} (x^2 + 1) = 5$
- $\lim_{x \to 2^+} (4x - 3) = 5$

Continuous at $x = 2$. ✓

**Check derivatives:**
- Left: $\frac{d}{dx}(x^2 + 1) = 2x \to 4$ at $x = 2$
- Right: $\frac{d}{dx}(4x - 3) = 4$ at $x = 2$

Both equal 4. ✓

**Answer:** Yes, $g$ is differentiable at $x = 2$ with $g'(2) = 4$.

---

### Solution 10

$h(x) = |x^2 - 1| = |(x-1)(x+1)|$

Corners occur where $x^2 - 1 = 0$, i.e., at $x = 1$ and $x = -1$.

**At $x = 1$:**
- Left of 1: $h(x) = 1 - x^2$, derivative = $-2x \to -2$
- Right of 1: $h(x) = x^2 - 1$, derivative = $2x \to 2$
- $-2 \neq 2$: not differentiable

**At $x = -1$:**
- Left of -1: $h(x) = x^2 - 1$, derivative = $2x \to -2$
- Right of -1: $h(x) = 1 - x^2$, derivative = $-2x \to 2$
- $-2 \neq 2$: not differentiable

**Answer:** $h$ is not differentiable at $x = -1$ and $x = 1$.

---

### Solution 11

$$f'(x) = \lim_{h \to 0} \frac{\frac{x+h}{x+h+2} - \frac{x}{x+2}}{h}$$

Combine fractions:
$$\frac{x+h}{x+h+2} - \frac{x}{x+2} = \frac{(x+h)(x+2) - x(x+h+2)}{(x+h+2)(x+2)}$$

Numerator: $(x+h)(x+2) - x(x+h+2) = x^2 + 2x + hx + 2h - x^2 - hx - 2x = 2h$

$$= \frac{2h}{(x+h+2)(x+2)}$$

Divide by $h$ and take limit:
$$f'(x) = \lim_{h \to 0} \frac{2}{(x+h+2)(x+2)} = \frac{2}{(x+2)^2}$$

**Answer:** $f'(x) = \frac{2}{(x+2)^2}$

---

### Solution 12

For differentiability at $x = 1$, we need:
1. Continuity: $k(1)^2 = 1 + 2 \Rightarrow k = 3$
2. Equal derivatives: $(kx^2)' = 2kx \to 2k$ at $x=1$; $(x+2)' = 1$

Need $2k = 1$, so $k = \frac{1}{2}$.

But this contradicts continuity requiring $k = 3$.

**Answer:** No value of $k$ makes $f$ differentiable at $x = 1$.

Wait, let me reconsider. For continuity: $k \cdot 1^2 = 1 + 2$ gives $k = 3$.

For differentiability: Left derivative = $2k(1) = 2k$. Right derivative = $1$.

We need $2k = 1$, so $k = 0.5$.

Since $k = 3$ for continuity but $k = 0.5$ for differentiability, there's no solution.

**Answer:** No such $k$ exists. The function cannot be made differentiable at $x = 1$.

---

### Solution 13

$$v(3) = s'(3) = \lim_{h \to 0} \frac{s(3+h) - s(3)}{h}$$

$s(3) = 9 - 12 + 3 = 0$

$s(3+h) = (3+h)^2 - 4(3+h) + 3 = 9 + 6h + h^2 - 12 - 4h + 3 = 6h + h^2 - 4h = 2h + h^2$

Wait, let me recalculate:
$s(3+h) = (3+h)^2 - 4(3+h) + 3 = 9 + 6h + h^2 - 12 - 4h + 3 = h^2 + 2h$

$$v(3) = \lim_{h \to 0} \frac{h^2 + 2h - 0}{h} = \lim_{h \to 0} (h + 2) = 2$$

**Answer:** $v(3) = 2$ (velocity is 2 units per time unit)

---

### Solution 14

$$f'(0) = \lim_{h \to 0} \frac{h^{2/3} - 0}{h} = \lim_{h \to 0} \frac{1}{h^{1/3}}$$

As $h \to 0^+$: $\frac{1}{h^{1/3}} \to +\infty$

As $h \to 0^-$: $\frac{1}{h^{1/3}} \to -\infty$

The limit doesn't exist (infinite).

**Answer:** The derivative doesn't exist at $x = 0$ because the limit is infinite (vertical tangent).

---

### Solution 15

$$f'(0) = \lim_{h \to 0} \frac{f(h) - f(0)}{h} = \lim_{h \to 0} \frac{h^2 \sin(1/h) - 0}{h} = \lim_{h \to 0} h \sin\left(\frac{1}{h}\right)$$

Since $-1 \leq \sin(1/h) \leq 1$:
$$-|h| \leq h \sin\left(\frac{1}{h}\right) \leq |h|$$

By the Squeeze Theorem: $\lim_{h \to 0} h \sin(1/h) = 0$

**Answer:** $f'(0) = 0$

---

### Solution 16

By the binomial theorem:
$$(x+h)^n = \sum_{k=0}^{n} \binom{n}{k} x^{n-k} h^k = x^n + nx^{n-1}h + \binom{n}{2}x^{n-2}h^2 + \cdots + h^n$$

$$f'(x) = \lim_{h \to 0} \frac{(x+h)^n - x^n}{h}$$

$$= \lim_{h \to 0} \frac{nx^{n-1}h + \binom{n}{2}x^{n-2}h^2 + \cdots + h^n}{h}$$

$$= \lim_{h \to 0} \left[nx^{n-1} + \binom{n}{2}x^{n-2}h + \cdots + h^{n-1}\right] = nx^{n-1}$$

**Answer:** $f'(x) = nx^{n-1}$ (the power rule!)

---

### Solution 17

**At $x = 1$:**

Continuity: $a(1)^2 + b(1) = 1^3 \Rightarrow a + b = 1$ ... (1)

Differentiability: $(ax^2 + bx)' = 2ax + b \to 2a + b$ at $x = 1$

$(x^3)' = 3x^2 \to 3$ at $x = 1$

Need: $2a + b = 3$ ... (2)

From (1): $b = 1 - a$. Substitute into (2):
$2a + (1 - a) = 3 \Rightarrow a = 2$, $b = -1$

**Answer:** $a = 2$, $b = -1$

---

### Solution 18

$$f'(0) = \lim_{h \to 0} \frac{f(h) - f(0)}{h} = \lim_{h \to 0} \frac{f(h) - 0}{h} = \lim_{h \to 0} \frac{f(h)}{h}$$

If $h \in \mathbb{Q}$: $\frac{f(h)}{h} = \frac{h^2}{h} = h \to 0$

If $h \notin \mathbb{Q}$: $\frac{f(h)}{h} = \frac{0}{h} = 0 \to 0$

In both cases, the limit is 0.

**Answer:** Yes, $f$ is differentiable at $x = 0$ with $f'(0) = 0$.

---

## AP Exam Tips

### Definition Recognition

The AP exam often presents limits that ARE derivatives in disguise:

$$\lim_{h \to 0} \frac{(2+h)^3 - 8}{h}$$

Recognize this as $f'(2)$ where $f(x) = x^3$. Answer: $3(2)^2 = 12$

$$\lim_{x \to 5} \frac{x^2 - 25}{x - 5}$$

Recognize this as $f'(5)$ where $f(x) = x^2$. Answer: $2(5) = 10$

### Common Mistakes to Avoid

**Mistake 1: Forgetting that $h$ can be negative**

When checking differentiability, always check both $h \to 0^+$ and $h \to 0^-$.

**Mistake 2: Assuming continuous = differentiable**

Remember: $|x|$ is continuous everywhere but not differentiable at $x = 0$.

**Mistake 3: Not simplifying before taking the limit**

Always algebraically simplify the difference quotient to cancel the $h$ in the denominator before taking the limit.

**Mistake 4: Confusing $f'(a)$ with $f(a)$**

$f(a)$ is the function value; $f'(a)$ is the derivative (slope) at that point.

### Key Formulas to Memorize

| Function | Derivative |
|----------|------------|
| $c$ (constant) | $0$ |
| $x$ | $1$ |
| $x^n$ | $nx^{n-1}$ |
| $\sqrt{x} = x^{1/2}$ | $\frac{1}{2\sqrt{x}}$ |
| $\frac{1}{x} = x^{-1}$ | $-\frac{1}{x^2}$ |

---

## Summary

**The derivative of $f$ at $x = a$:**

$$f'(a) = \lim_{h \to 0} \frac{f(a+h) - f(a)}{h} = \lim_{x \to a} \frac{f(x) - f(a)}{x - a}$$

**Interpretations:**
- Slope of the tangent line at $(a, f(a))$
- Instantaneous rate of change at $x = a$
- Limit of average rates of change

**Differentiability:**
- $f$ is differentiable at $a$ if $f'(a)$ exists
- Differentiable implies continuous (but not vice versa)
- Not differentiable at: corners, cusps, vertical tangents, discontinuities

**Process for finding derivatives using the definition:**
1. Write $\frac{f(x+h) - f(x)}{h}$
2. Expand and simplify
3. Cancel the $h$ in the denominator
4. Take the limit as $h \to 0$

The definition of the derivative is the foundation of differential calculus. While we'll soon learn shortcut rules, understanding this definition helps you know what a derivative really means!

---

<div align="center">

[← Continuous Functions](calculus/continuity-common-functions.md) | [Derivative at a Point →](calculus/derivative-at-a-point.md)

</div>
