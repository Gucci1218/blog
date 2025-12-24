# Piecewise Continuity
<p class="article-date">October 27, 2024</p>

## Learning Objectives

By the end of this article, you will be able to:

- Analyze piecewise functions for continuity at boundary points
- Determine which piece to use for function values vs. limits
- Find values of constants that make piecewise functions continuous
- Solve systems of equations arising from multiple boundary conditions
- Handle piecewise functions with three or more pieces
- Identify all points of discontinuity in piecewise functions
- Master AP Calculus problems involving piecewise continuity

---

## The Core Concept: Where the Pieces Meet

### The Intuition

A piecewise function is like a road built by different construction crews. Each crew builds their section perfectly smoothly. The question is: **do the sections connect seamlessly, or are there bumps, gaps, or cliffs where they meet?**

```
Smooth connection:              Gap at junction:

    ╱╲                              ╱╲
   ╱  ╲                            ╱  ╲
  ╱    ╲____                      ╱    ○
                                        ●____

Continuous at boundary          Discontinuous at boundary
```

### The Key Insight

**Within each piece**, a piecewise function is typically continuous (assuming each piece is a nice function like a polynomial, exponential, etc.).

**The only places discontinuities can occur** are at the **boundary points**—where the function switches from one formula to another.

### The Strategy

For a piecewise function with boundary at $x = a$:

1. **Find $f(a)$** — use whichever piece's domain includes $a$
2. **Find $\lim_{x \to a^-} f(x)$** — use the piece for $x < a$
3. **Find $\lim_{x \to a^+} f(x)$** — use the piece for $x > a$ (or $x \geq a$)
4. **Check all three conditions:**
   - Does $f(a)$ exist?
   - Does $\lim_{x \to a} f(x)$ exist? (i.e., do one-sided limits match?)
   - Does $\lim_{x \to a} f(x) = f(a)$?

---

## Understanding Domain Boundaries

### Reading Piecewise Notation

The inequalities in piecewise definitions tell you exactly which formula applies where.

$$f(x) = \begin{cases} x^2 & \text{if } x < 2 \\ 3x - 1 & \text{if } x \geq 2 \end{cases}$$

| To find... | Use this piece | Because... |
|------------|---------------|------------|
| $f(1)$ | $x^2$ | $1 < 2$ |
| $f(2)$ | $3x - 1$ | $2 \geq 2$ |
| $f(3)$ | $3x - 1$ | $3 \geq 2$ |
| $\lim_{x \to 2^-} f(x)$ | $x^2$ | approaching from $x < 2$ |
| $\lim_{x \to 2^+} f(x)$ | $3x - 1$ | approaching from $x > 2$ |

### Common Boundary Patterns

**Pattern 1: $<$ and $\geq$**
$$f(x) = \begin{cases} g(x) & \text{if } x < a \\ h(x) & \text{if } x \geq a \end{cases}$$

- $f(a) = h(a)$ (the second piece includes the boundary)
- Left limit uses $g(x)$
- Right limit uses $h(x)$

**Pattern 2: $\leq$ and $>$**
$$f(x) = \begin{cases} g(x) & \text{if } x \leq a \\ h(x) & \text{if } x > a \end{cases}$$

- $f(a) = g(a)$ (the first piece includes the boundary)
- Left limit uses $g(x)$
- Right limit uses $h(x)$

**Pattern 3: Three pieces**
$$f(x) = \begin{cases} g(x) & \text{if } x < a \\ c & \text{if } x = a \\ h(x) & \text{if } x > a \end{cases}$$

- $f(a) = c$ (explicitly defined)
- Left limit uses $g(x)$
- Right limit uses $h(x)$

---

## Worked Examples: Checking Continuity

### Example 1: Basic Two-Piece Function

**Problem:** Determine if $f(x) = \begin{cases} x^2 - 1 & \text{if } x < 2 \\ 2x + 1 & \text{if } x \geq 2 \end{cases}$ is continuous at $x = 2$.

**Solution:**

**Step 1: Find $f(2)$**

Since $2 \geq 2$, use the second piece:
$$f(2) = 2(2) + 1 = 5$$

**Step 2: Find the left-hand limit**

For $x < 2$, use $x^2 - 1$:
$$\lim_{x \to 2^-} (x^2 - 1) = 4 - 1 = 3$$

**Step 3: Find the right-hand limit**

For $x \geq 2$, use $2x + 1$:
$$\lim_{x \to 2^+} (2x + 1) = 4 + 1 = 5$$

**Step 4: Check the conditions**

- $f(2) = 5$ ✓ (exists)
- $\lim_{x \to 2^-} f(x) = 3 \neq 5 = \lim_{x \to 2^+} f(x)$ ✗

The one-sided limits are not equal, so $\lim_{x \to 2} f(x)$ does not exist.

**Conclusion:** $f$ is **discontinuous** at $x = 2$ (jump discontinuity).

---

### Example 2: Continuous Piecewise Function

**Problem:** Determine if $g(x) = \begin{cases} x + 3 & \text{if } x \leq 1 \\ x^2 + 2 & \text{if } x > 1 \end{cases}$ is continuous at $x = 1$.

**Solution:**

**Step 1: Find $g(1)$**

Since $1 \leq 1$, use the first piece:
$$g(1) = 1 + 3 = 4$$

**Step 2: Find the left-hand limit**

$$\lim_{x \to 1^-} (x + 3) = 1 + 3 = 4$$

**Step 3: Find the right-hand limit**

$$\lim_{x \to 1^+} (x^2 + 2) = 1 + 2 = 3$$

**Step 4: Check the conditions**

- $g(1) = 4$ ✓
- $\lim_{x \to 1^-} g(x) = 4 \neq 3 = \lim_{x \to 1^+} g(x)$ ✗

**Conclusion:** $g$ is **discontinuous** at $x = 1$ (jump discontinuity).

---

### Example 3: Function with Explicit Point Definition

**Problem:** Determine if $h(x) = \begin{cases} \frac{x^2 - 4}{x - 2} & \text{if } x \neq 2 \\ 5 & \text{if } x = 2 \end{cases}$ is continuous at $x = 2$.

**Solution:**

**Step 1: Find $h(2)$**

By definition: $h(2) = 5$

**Step 2: Find the limit**

For $x \neq 2$:
$$\lim_{x \to 2} \frac{x^2 - 4}{x - 2} = \lim_{x \to 2} \frac{(x-2)(x+2)}{x-2} = \lim_{x \to 2} (x + 2) = 4$$

**Step 3: Check the conditions**

- $h(2) = 5$ ✓
- $\lim_{x \to 2} h(x) = 4$ ✓
- $4 \neq 5$ ✗

**Conclusion:** $h$ is **discontinuous** at $x = 2$ (removable discontinuity—the limit exists but doesn't match the function value).

---

### Example 4: Three-Piece Function

**Problem:** Find all points of discontinuity for:
$$f(x) = \begin{cases} x + 4 & \text{if } x < -2 \\ x^2 & \text{if } -2 \leq x < 1 \\ 3 - x & \text{if } x \geq 1 \end{cases}$$

**Solution:**

Check boundary points: $x = -2$ and $x = 1$.

**At $x = -2$:**

- $f(-2) = (-2)^2 = 4$ (using middle piece since $-2 \leq -2$)
- $\lim_{x \to -2^-} (x + 4) = -2 + 4 = 2$
- $\lim_{x \to -2^+} x^2 = 4$
- Left limit $\neq$ right limit

**Discontinuous at $x = -2$** (jump discontinuity)

**At $x = 1$:**

- $f(1) = 3 - 1 = 2$ (using third piece since $1 \geq 1$)
- $\lim_{x \to 1^-} x^2 = 1$
- $\lim_{x \to 1^+} (3 - x) = 2$
- Left limit $\neq$ right limit

**Discontinuous at $x = 1$** (jump discontinuity)

**Answer:** Discontinuous at $x = -2$ and $x = 1$.

---

## Finding Constants for Continuity

### The Core Technique

When a piecewise function contains unknown constants, we can find values that make the function continuous by setting:

$$\lim_{x \to a^-} f(x) = \lim_{x \to a^+} f(x) = f(a)$$

### Example 5: One Unknown Constant

**Problem:** Find $k$ so that $f(x) = \begin{cases} 2x + k & \text{if } x \leq 3 \\ x^2 & \text{if } x > 3 \end{cases}$ is continuous at $x = 3$.

**Solution:**

For continuity at $x = 3$:
$$\lim_{x \to 3^-} f(x) = \lim_{x \to 3^+} f(x) = f(3)$$

**Left-hand limit (and function value, since $3 \leq 3$):**
$$\lim_{x \to 3^-} (2x + k) = 6 + k = f(3)$$

**Right-hand limit:**
$$\lim_{x \to 3^+} x^2 = 9$$

**Set them equal:**
$$6 + k = 9$$
$$k = 3$$

**Verification:** With $k = 3$:
- $f(3) = 2(3) + 3 = 9$
- $\lim_{x \to 3^-} f(x) = 9$
- $\lim_{x \to 3^+} f(x) = 9$ ✓

---

### Example 6: One Constant, Different Setup

**Problem:** Find $c$ so that $g(x) = \begin{cases} cx^2 + 1 & \text{if } x < 2 \\ x + c & \text{if } x \geq 2 \end{cases}$ is continuous at $x = 2$.

**Solution:**

**Left-hand limit:**
$$\lim_{x \to 2^-} (cx^2 + 1) = 4c + 1$$

**Right-hand limit (and function value):**
$$\lim_{x \to 2^+} (x + c) = 2 + c = g(2)$$

**Set left = right:**
$$4c + 1 = 2 + c$$
$$3c = 1$$
$$c = \frac{1}{3}$$

**Verification:** With $c = \frac{1}{3}$:
- $g(2) = 2 + \frac{1}{3} = \frac{7}{3}$
- $\lim_{x \to 2^-} g(x) = 4 \cdot \frac{1}{3} + 1 = \frac{7}{3}$
- $\lim_{x \to 2^+} g(x) = \frac{7}{3}$ ✓

---

### Example 7: Two Unknown Constants

**Problem:** Find $a$ and $b$ so that $f(x) = \begin{cases} ax + b & \text{if } x < 1 \\ x^2 & \text{if } 1 \leq x \leq 4 \\ bx + a & \text{if } x > 4 \end{cases}$ is continuous everywhere.

**Solution:**

We need continuity at both $x = 1$ and $x = 4$.

**At $x = 1$:**

- $f(1) = 1^2 = 1$
- $\lim_{x \to 1^-} (ax + b) = a + b$
- $\lim_{x \to 1^+} x^2 = 1$

For continuity: $a + b = 1$ ... (Equation 1)

**At $x = 4$:**

- $f(4) = 4^2 = 16$
- $\lim_{x \to 4^-} x^2 = 16$
- $\lim_{x \to 4^+} (bx + a) = 4b + a$

For continuity: $4b + a = 16$ ... (Equation 2)

**Solve the system:**

From Equation 1: $a = 1 - b$

Substitute into Equation 2:
$$4b + (1 - b) = 16$$
$$3b + 1 = 16$$
$$3b = 15$$
$$b = 5$$

Then: $a = 1 - 5 = -4$

**Answer:** $a = -4$, $b = 5$

**Verification:**
- At $x = 1$: Left limit $= -4 + 5 = 1$, $f(1) = 1$ ✓
- At $x = 4$: Right limit $= 5(4) + (-4) = 16$, $f(4) = 16$ ✓

---

### Example 8: Trigonometric Piecewise Function

**Problem:** Find $k$ so that $g(x) = \begin{cases} k \cos x & \text{if } x \leq 0 \\ e^x - 1 & \text{if } x > 0 \end{cases}$ is continuous at $x = 0$.

**Solution:**

**Left-hand limit (and function value):**
$$\lim_{x \to 0^-} k \cos x = k \cos 0 = k \cdot 1 = k = g(0)$$

**Right-hand limit:**
$$\lim_{x \to 0^+} (e^x - 1) = e^0 - 1 = 0$$

**Set them equal:**
$$k = 0$$

---

### Example 9: Square Root in Piecewise

**Problem:** Find $c$ so that $h(x) = \begin{cases} \sqrt{x + c} & \text{if } x \geq 0 \\ x^2 + c & \text{if } x < 0 \end{cases}$ is continuous at $x = 0$.

**Solution:**

**Right-hand limit (and function value):**
$$\lim_{x \to 0^+} \sqrt{x + c} = \sqrt{c} = h(0)$$

(Note: We need $c \geq 0$ for this to be defined.)

**Left-hand limit:**
$$\lim_{x \to 0^-} (x^2 + c) = 0 + c = c$$

**Set them equal:**
$$\sqrt{c} = c$$
$$c = c^2 \quad \text{(squaring both sides, valid since } c \geq 0\text{)}$$
$$c^2 - c = 0$$
$$c(c - 1) = 0$$
$$c = 0 \text{ or } c = 1$$

**Check both solutions:**

- $c = 0$: $\sqrt{0} = 0$ ✓
- $c = 1$: $\sqrt{1} = 1$ ✓

**Answer:** $c = 0$ or $c = 1$

---

### Example 10: Three Constants

**Problem:** Find $a$, $b$, and $c$ so that $f(x) = \begin{cases} ax^2 + bx + c & \text{if } x \leq 0 \\ \sin x & \text{if } 0 < x < \pi \\ ax + b & \text{if } x \geq \pi \end{cases}$ is continuous everywhere, given that $f(-1) = 2$.

**Solution:**

**Continuity at $x = 0$:**

- $f(0) = a(0)^2 + b(0) + c = c$
- $\lim_{x \to 0^-} (ax^2 + bx + c) = c$
- $\lim_{x \to 0^+} \sin x = 0$

For continuity: $c = 0$ ... (Equation 1)

**Continuity at $x = \pi$:**

- $f(\pi) = a\pi + b$
- $\lim_{x \to \pi^-} \sin x = 0$
- $\lim_{x \to \pi^+} (ax + b) = a\pi + b$

For continuity: $a\pi + b = 0$, so $b = -a\pi$ ... (Equation 2)

**Using $f(-1) = 2$:**

$$a(-1)^2 + b(-1) + c = 2$$
$$a - b + c = 2$$

Substitute $c = 0$ and $b = -a\pi$:
$$a - (-a\pi) + 0 = 2$$
$$a + a\pi = 2$$
$$a(1 + \pi) = 2$$
$$a = \frac{2}{1 + \pi}$$

Then: $b = -a\pi = -\frac{2\pi}{1 + \pi}$

**Answer:**
$$a = \frac{2}{1 + \pi}, \quad b = -\frac{2\pi}{1 + \pi}, \quad c = 0$$

---

## Special Cases and Tricky Situations

### Case 1: The Constant Appears in the Boundary

**Problem:** Find $k$ so that $f(x) = \begin{cases} x + 1 & \text{if } x < k \\ x^2 & \text{if } x \geq k \end{cases}$ is continuous at $x = k$.

**Solution:**

For continuity at $x = k$:
$$\lim_{x \to k^-} (x + 1) = \lim_{x \to k^+} x^2$$
$$k + 1 = k^2$$
$$k^2 - k - 1 = 0$$
$$k = \frac{1 \pm \sqrt{5}}{2}$$

**Answer:** $k = \frac{1 + \sqrt{5}}{2}$ or $k = \frac{1 - \sqrt{5}}{2}$

---

### Case 2: No Value Makes It Continuous

**Problem:** Is there a value of $c$ that makes $g(x) = \begin{cases} x^2 + c & \text{if } x < 1 \\ 2x + c & \text{if } x \geq 1 \end{cases}$ continuous at $x = 1$?

**Solution:**

**Left-hand limit:**
$$\lim_{x \to 1^-} (x^2 + c) = 1 + c$$

**Right-hand limit:**
$$\lim_{x \to 1^+} (2x + c) = 2 + c$$

For continuity: $1 + c = 2 + c$, which gives $1 = 2$.

**This is impossible!** No value of $c$ can make the function continuous at $x = 1$.

The pieces have the same constant $c$, but their "base" values differ by 1 at $x = 1$.

---

### Case 3: Already Continuous for All Values

**Problem:** For what values of $k$ is $h(x) = \begin{cases} x + k & \text{if } x \leq 2 \\ 3x + k - 4 & \text{if } x > 2 \end{cases}$ continuous at $x = 2$?

**Solution:**

**Left-hand limit (and function value):**
$$\lim_{x \to 2^-} (x + k) = 2 + k = h(2)$$

**Right-hand limit:**
$$\lim_{x \to 2^+} (3x + k - 4) = 6 + k - 4 = 2 + k$$

Both limits equal $2 + k$ for any value of $k$!

**Answer:** The function is continuous at $x = 2$ for **all values of $k$**.

---

## Practice Problems

### Basic Problems (1-5)

**1.** Determine if $f(x) = \begin{cases} 3x - 2 & \text{if } x < 1 \\ x^2 & \text{if } x \geq 1 \end{cases}$ is continuous at $x = 1$.

---

**2.** Find $k$ so that $g(x) = \begin{cases} kx + 3 & \text{if } x \leq 2 \\ x^2 - 1 & \text{if } x > 2 \end{cases}$ is continuous at $x = 2$.

---

**3.** Determine if $h(x) = \begin{cases} \frac{x^2 - 9}{x - 3} & \text{if } x \neq 3 \\ 6 & \text{if } x = 3 \end{cases}$ is continuous at $x = 3$.

---

**4.** Find all points of discontinuity for $f(x) = \begin{cases} x + 5 & \text{if } x < -1 \\ x^2 + 3 & \text{if } x \geq -1 \end{cases}$

---

**5.** Find $c$ so that $g(x) = \begin{cases} x^2 + c & \text{if } x < 3 \\ 4x - 2 & \text{if } x \geq 3 \end{cases}$ is continuous at $x = 3$.

---

### Intermediate Problems (6-10)

**6.** Find $a$ and $b$ so that $f(x) = \begin{cases} ax + b & \text{if } x < 2 \\ x^2 & \text{if } 2 \leq x \leq 5 \\ ax + b & \text{if } x > 5 \end{cases}$ is continuous everywhere.

---

**7.** For what value(s) of $k$ is $g(x) = \begin{cases} k^2x & \text{if } x \leq 1 \\ kx^2 & \text{if } x > 1 \end{cases}$ continuous at $x = 1$?

---

**8.** Find all points of discontinuity for:
$$h(x) = \begin{cases} |x + 2| & \text{if } x < 0 \\ x^2 - 2 & \text{if } 0 \leq x < 2 \\ 2x - 2 & \text{if } x \geq 2 \end{cases}$$

---

**9.** Find $c$ so that $f(x) = \begin{cases} \frac{\sin x}{x} & \text{if } x \neq 0 \\ c & \text{if } x = 0 \end{cases}$ is continuous at $x = 0$.

---

**10.** Find $a$ and $b$ so that $g(x) = \begin{cases} ae^x & \text{if } x \leq 0 \\ bx + 1 & \text{if } 0 < x < 1 \\ \ln x + b & \text{if } x \geq 1 \end{cases}$ is continuous everywhere.

---

### Advanced Problems (11-15)

**11.** Find all values of $k$ for which $f(x) = \begin{cases} \frac{x^2 - k^2}{x - k} & \text{if } x \neq k \\ 2k & \text{if } x = k \end{cases}$ is continuous at $x = k$.

---

**12.** Find $a$, $b$, and $c$ so that $g(x) = \begin{cases} ax^2 + bx + c & \text{if } x \leq 1 \\ 2x & \text{if } x > 1 \end{cases}$ is continuous at $x = 1$, has $g(0) = 3$, and has $g'(1^-) = g'(1^+)$ (the derivatives match).

---

**13.** Determine all points where $h(x) = \begin{cases} \lfloor x \rfloor & \text{if } x < 2 \\ x - 1 & \text{if } x \geq 2 \end{cases}$ is discontinuous.

---

**14.** Find all values of $a$ for which $f(x) = \begin{cases} ax^2 + 1 & \text{if } x \leq a \\ 2ax & \text{if } x > a \end{cases}$ is continuous at $x = a$.

---

**15.** The function $g(x) = \begin{cases} px + q & \text{if } x < -1 \\ x^2 + 1 & \text{if } -1 \leq x \leq 2 \\ rx + s & \text{if } x > 2 \end{cases}$ is continuous everywhere. Find $p$, $q$, $r$, and $s$ given that $g(-2) = 0$ and $g(3) = 8$.

---

### Challenge Problems (16-18)

**16.** Find all values of $k$ such that $f(x) = \begin{cases} \frac{1 - \cos(kx)}{x^2} & \text{if } x \neq 0 \\ 2 & \text{if } x = 0 \end{cases}$ is continuous at $x = 0$.

*(Hint: Use the limit $\lim_{u \to 0} \frac{1 - \cos u}{u^2} = \frac{1}{2}$)*

---

**17.** Define $g(x) = \begin{cases} x^n \sin\left(\frac{1}{x}\right) & \text{if } x \neq 0 \\ 0 & \text{if } x = 0 \end{cases}$. For what positive integer values of $n$ is $g$ continuous at $x = 0$?

---

**18.** Find constants $a$ and $b$ so that $h(x) = \begin{cases} \frac{\sqrt{1 + ax} - 1}{x} & \text{if } x > 0 \\ b & \text{if } x = 0 \\ \frac{e^{ax} - 1}{x} & \text{if } x < 0 \end{cases}$ is continuous at $x = 0$.

---

## Solutions to Practice Problems

### Solution 1

**Function value:** $f(1) = 1^2 = 1$

**Left-hand limit:** $\lim_{x \to 1^-} (3x - 2) = 1$

**Right-hand limit:** $\lim_{x \to 1^+} x^2 = 1$

Since $\lim_{x \to 1} f(x) = 1 = f(1)$:

**$f$ is continuous at $x = 1$.**

---

### Solution 2

**Left-hand limit (and function value):**
$$\lim_{x \to 2^-} (kx + 3) = 2k + 3 = g(2)$$

**Right-hand limit:**
$$\lim_{x \to 2^+} (x^2 - 1) = 3$$

Set equal: $2k + 3 = 3$, so $k = 0$.

---

### Solution 3

**Function value:** $h(3) = 6$

**Limit:**
$$\lim_{x \to 3} \frac{x^2 - 9}{x - 3} = \lim_{x \to 3} \frac{(x-3)(x+3)}{x-3} = \lim_{x \to 3} (x + 3) = 6$$

Since $\lim_{x \to 3} h(x) = 6 = h(3)$:

**$h$ is continuous at $x = 3$.**

---

### Solution 4

**At $x = -1$:**
- $f(-1) = (-1)^2 + 3 = 4$
- $\lim_{x \to -1^-} (x + 5) = 4$
- $\lim_{x \to -1^+} (x^2 + 3) = 4$

All three equal 4, so $f$ is continuous at $x = -1$.

**No points of discontinuity.**

---

### Solution 5

**Left-hand limit:**
$$\lim_{x \to 3^-} (x^2 + c) = 9 + c$$

**Right-hand limit (and function value):**
$$\lim_{x \to 3^+} (4x - 2) = 10 = g(3)$$

Set equal: $9 + c = 10$, so $c = 1$.

---

### Solution 6

**At $x = 2$:**
- $\lim_{x \to 2^-} (ax + b) = 2a + b$
- $f(2) = 4$

Equation 1: $2a + b = 4$

**At $x = 5$:**
- $f(5) = 25$
- $\lim_{x \to 5^+} (ax + b) = 5a + b$

Equation 2: $5a + b = 25$

**Solve:**
Subtract Equation 1 from Equation 2:
$$3a = 21 \implies a = 7$$
$$b = 4 - 2(7) = -10$$

**Answer:** $a = 7$, $b = -10$

---

### Solution 7

**Left-hand limit (and function value):**
$$\lim_{x \to 1^-} k^2x = k^2$$

**Right-hand limit:**
$$\lim_{x \to 1^+} kx^2 = k$$

Set equal: $k^2 = k$
$$k^2 - k = 0$$
$$k(k - 1) = 0$$
$$k = 0 \text{ or } k = 1$$

---

### Solution 8

**At $x = 0$:**
- $h(0) = 0^2 - 2 = -2$
- $\lim_{x \to 0^-} |x + 2| = |2| = 2$
- $\lim_{x \to 0^+} (x^2 - 2) = -2$
- $2 \neq -2$

**Discontinuous at $x = 0$** (jump)

**At $x = 2$:**
- $h(2) = 2(2) - 2 = 2$
- $\lim_{x \to 2^-} (x^2 - 2) = 2$
- $\lim_{x \to 2^+} (2x - 2) = 2$

**Continuous at $x = 2$**

**Answer:** Discontinuous only at $x = 0$

---

### Solution 9

$$\lim_{x \to 0} \frac{\sin x}{x} = 1$$

For continuity: $c = 1$

---

### Solution 10

**At $x = 0$:**
- $g(0) = ae^0 = a$
- $\lim_{x \to 0^-} ae^x = a$
- $\lim_{x \to 0^+} (bx + 1) = 1$

Equation 1: $a = 1$

**At $x = 1$:**
- $g(1) = \ln 1 + b = b$
- $\lim_{x \to 1^-} (bx + 1) = b + 1$
- $\lim_{x \to 1^+} (\ln x + b) = b$

Equation 2: $b + 1 = b$ is impossible!

Wait—we need $\lim_{x \to 1^-} = \lim_{x \to 1^+}$:
$$b + 1 = b$$

This has no solution. Let me re-read the problem...

Actually, looking at the boundary: $x \geq 1$ means $g(1) = \ln 1 + b = b$.

So we need: $\lim_{x \to 1^-}(bx + 1) = b + 1 = g(1) = b$

This gives $b + 1 = b$, which is impossible.

**There is no solution—the function cannot be made continuous everywhere.**

---

### Solution 11

$$\lim_{x \to k} \frac{x^2 - k^2}{x - k} = \lim_{x \to k} \frac{(x-k)(x+k)}{x-k} = \lim_{x \to k} (x + k) = 2k$$

For continuity: $f(k) = 2k$ must equal the limit $2k$.

This is always true! The function is continuous at $x = k$ for **all values of $k$**.

---

### Solution 12

**Continuity at $x = 1$:**
- $\lim_{x \to 1^-} (ax^2 + bx + c) = a + b + c$
- $\lim_{x \to 1^+} 2x = 2$

Equation 1: $a + b + c = 2$

**Given $g(0) = 3$:**
$$a(0)^2 + b(0) + c = c = 3$$

Equation 2: $c = 3$

**Derivative matching at $x = 1$:**
- $g'(x) = 2ax + b$ for $x < 1$, so $g'(1^-) = 2a + b$
- $g'(x) = 2$ for $x > 1$, so $g'(1^+) = 2$

Equation 3: $2a + b = 2$

**Solve:**
From Equation 2: $c = 3$
From Equation 1: $a + b + 3 = 2$, so $a + b = -1$
From Equation 3: $2a + b = 2$

Subtract: $a = 3$
Then: $b = -1 - 3 = -4$

**Answer:** $a = 3$, $b = -4$, $c = 3$

---

### Solution 13

The floor function $\lfloor x \rfloor$ has jump discontinuities at all integers.

For $x < 2$, discontinuities at integers: ..., $-1$, $0$, $1$.

**At $x = 2$:**
- $h(2) = 2 - 1 = 1$
- $\lim_{x \to 2^-} \lfloor x \rfloor = 1$
- $\lim_{x \to 2^+} (x - 1) = 1$

Continuous at $x = 2$!

**Discontinuities:** All integers less than 2 (i.e., ..., $-2$, $-1$, $0$, $1$)

---

### Solution 14

**Left-hand limit (and function value):**
$$\lim_{x \to a^-} (ax^2 + 1) = a \cdot a^2 + 1 = a^3 + 1 = f(a)$$

**Right-hand limit:**
$$\lim_{x \to a^+} 2ax = 2a^2$$

Set equal: $a^3 + 1 = 2a^2$
$$a^3 - 2a^2 + 1 = 0$$

Test $a = 1$: $1 - 2 + 1 = 0$ ✓

Factor: $(a - 1)(a^2 - a - 1) = 0$

$$a = 1 \text{ or } a = \frac{1 \pm \sqrt{5}}{2}$$

---

### Solution 15

**At $x = -1$:**
- $g(-1) = 1 + 1 = 2$
- $\lim_{x \to -1^-} (px + q) = -p + q$

Equation 1: $-p + q = 2$

**At $x = 2$:**
- $g(2) = 4 + 1 = 5$
- $\lim_{x \to 2^+} (rx + s) = 2r + s$

Equation 2: $2r + s = 5$

**Using $g(-2) = 0$:**
$$p(-2) + q = 0$$

Equation 3: $-2p + q = 0$

**Using $g(3) = 8$:**
$$r(3) + s = 8$$

Equation 4: $3r + s = 8$

**Solve for $p$ and $q$:**
Equation 3: $q = 2p$
Substitute into Equation 1: $-p + 2p = 2$, so $p = 2$, $q = 4$

**Solve for $r$ and $s$:**
Subtract Equation 2 from Equation 4: $r = 3$
Then: $s = 5 - 2(3) = -1$

**Answer:** $p = 2$, $q = 4$, $r = 3$, $s = -1$

---

### Solution 16

Using the substitution $u = kx$, as $x \to 0$, $u \to 0$:

$$\lim_{x \to 0} \frac{1 - \cos(kx)}{x^2} = \lim_{x \to 0} \frac{1 - \cos(kx)}{x^2} \cdot \frac{k^2}{k^2} = k^2 \cdot \lim_{u \to 0} \frac{1 - \cos u}{u^2} = k^2 \cdot \frac{1}{2} = \frac{k^2}{2}$$

For continuity: $\frac{k^2}{2} = 2$, so $k^2 = 4$, giving $k = \pm 2$.

---

### Solution 17

We need $\lim_{x \to 0} x^n \sin\left(\frac{1}{x}\right) = 0$.

Since $-1 \leq \sin\left(\frac{1}{x}\right) \leq 1$:
$$-|x|^n \leq x^n \sin\left(\frac{1}{x}\right) \leq |x|^n$$

As $x \to 0$, $|x|^n \to 0$ for any $n > 0$.

By the Squeeze Theorem, the limit is 0.

**Answer:** $g$ is continuous at $x = 0$ for **all positive integers $n$**.

---

### Solution 18

**Right-hand limit:**

Rationalize: $\frac{\sqrt{1 + ax} - 1}{x} \cdot \frac{\sqrt{1 + ax} + 1}{\sqrt{1 + ax} + 1} = \frac{ax}{x(\sqrt{1 + ax} + 1)} = \frac{a}{\sqrt{1 + ax} + 1}$

$$\lim_{x \to 0^+} \frac{a}{\sqrt{1 + ax} + 1} = \frac{a}{2}$$

**Left-hand limit:**

Using $\lim_{u \to 0} \frac{e^u - 1}{u} = 1$:

$$\lim_{x \to 0^-} \frac{e^{ax} - 1}{x} = a \cdot \lim_{x \to 0^-} \frac{e^{ax} - 1}{ax} = a \cdot 1 = a$$

**For continuity:**

We need: $\frac{a}{2} = b = a$

From $\frac{a}{2} = a$: $a = 0$

Then $b = 0$.

**Answer:** $a = 0$, $b = 0$

---

## AP Exam Tips

### Systematic Approach

When analyzing piecewise continuity:

1. **List all boundary points** where the formula changes
2. **For each boundary point:**
   - Calculate the function value (use the piece that includes that point)
   - Calculate both one-sided limits (use appropriate pieces)
   - Compare: Do all three match?

### Finding Constants Checklist

1. Write the continuity condition: left limit = right limit (= function value)
2. Substitute the boundary value into each piece
3. Set up the equation(s) and solve
4. **Always verify** your answer by plugging back in

### Common Errors to Avoid

**Error 1: Using the wrong piece for $f(a)$**

For $f(x) = \begin{cases} g(x) & \text{if } x < a \\ h(x) & \text{if } x \geq a \end{cases}$

$f(a) = h(a)$, NOT $g(a)$. The $\geq$ includes the boundary!

**Error 2: Confusing limits with function values**

The left-hand limit uses the piece for $x < a$, even if that piece doesn't include $a$ in its domain.

**Error 3: Forgetting to check all boundaries**

For a three-piece function with boundaries at $x = 1$ and $x = 3$, you need to check BOTH points.

**Error 4: Assuming continuity means the pieces are equal everywhere**

We only need the pieces to match AT the boundary point.

### Template for Free Response

"To find the value of $k$ that makes $f$ continuous at $x = 2$:

For continuity, we need $\lim_{x \to 2^-} f(x) = \lim_{x \to 2^+} f(x) = f(2)$.

Left-hand limit: $\lim_{x \to 2^-} (\text{left piece}) = ...$

Right-hand limit: $\lim_{x \to 2^+} (\text{right piece}) = ...$

Setting these equal: $... = ...$

Solving: $k = ...$

Verification: [plug back in and confirm]"

---

## Summary

**Analyzing piecewise continuity:**

1. Discontinuities can only occur at **boundary points** where the formula changes
2. At each boundary $x = a$:
   - Find $f(a)$ using the piece whose domain includes $a$
   - Find $\lim_{x \to a^-}$ using the piece for $x < a$
   - Find $\lim_{x \to a^+}$ using the piece for $x > a$
3. All three must be equal for continuity

**Finding constants:**

- Set up equations from the continuity condition
- Multiple boundaries → system of equations
- Always verify your solution

**Key insight:** The function value $f(a)$ is determined by which piece's domain includes the boundary point (check $<$ vs $\leq$, etc.).

Mastering piecewise continuity prepares you for the Intermediate Value Theorem and for analyzing piecewise-defined functions throughout calculus!

---

**Next Topics to Explore:**
- The Intermediate Value Theorem
- Making Functions Continuous
- Continuous Functions and Their Properties

---

<div align="center">

[← Types of Discontinuities](calculus/types-of-discontinuities.md) | [Intermediate Value Theorem →](calculus/intermediate-value-theorem.md)

</div>
