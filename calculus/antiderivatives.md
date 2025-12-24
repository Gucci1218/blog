# Antiderivatives

*You've spent weeks learning how to take derivatives. Now it's time to run the movie backwards. Given a derivative, can you figure out what the original function was? This reverse process—finding **antiderivatives**—is the gateway to integration, one of the two pillars of calculus.*

---

## What You'll Learn
- Understand what an antiderivative is and why there are infinitely many
- Apply basic antiderivative rules (power, exponential, trigonometric)
- Use the notation for indefinite integrals
- Solve initial value problems
- Recognize when a function has no elementary antiderivative

---

## Prerequisites
- [Basic Derivative Rules](/calculus/basic-derivative-rules)
- [Derivatives of Trigonometric Functions](/calculus/derivatives-trig)
- [Derivatives of Exponential Functions](/calculus/derivatives-exp)

---

## The Core Concept

### Intuition First

Imagine you're a detective. Someone hands you a velocity function and asks: "What was the position function?" You know that velocity is the derivative of position, so you need to work backwards—find a function whose derivative gives you the velocity.

This "reverse derivative" is called an **antiderivative**.

### The Definition

A function $F(x)$ is an **antiderivative** of $f(x)$ if:

$$F'(x) = f(x)$$

**Example**: $F(x) = x^3$ is an antiderivative of $f(x) = 3x^2$ because $\frac{d}{dx}[x^3] = 3x^2$.

### The "+C" Mystery

Here's a crucial insight: if $F(x)$ is an antiderivative of $f(x)$, then so is $F(x) + C$ for any constant $C$.

Why? Because the derivative of a constant is zero:
$$\frac{d}{dx}[F(x) + C] = F'(x) + 0 = f(x)$$

This means **every function has infinitely many antiderivatives**, all differing by a constant.

**Example**: All of these are antiderivatives of $2x$:
- $x^2$
- $x^2 + 1$
- $x^2 - 7$
- $x^2 + \pi$

### The Indefinite Integral

We use a special notation for the general antiderivative:

$$\int f(x) \, dx = F(x) + C$$

This is called the **indefinite integral** of $f(x)$.

| Symbol | Meaning |
|--------|---------|
| $\int$ | Integral sign (elongated S) |
| $f(x)$ | Integrand (function to integrate) |
| $dx$ | Indicates variable of integration |
| $F(x)$ | Any antiderivative of $f(x)$ |
| $C$ | Constant of integration |

### Basic Antiderivative Rules

Since antidifferentiation reverses differentiation, we can reverse our derivative rules:

**Power Rule for Integrals** (for $n \neq -1$):

$$\int x^n \, dx = \frac{x^{n+1}}{n+1} + C$$

*"Add one to the exponent, divide by the new exponent"*

**Constant Multiple Rule**:

$$\int k \cdot f(x) \, dx = k \int f(x) \, dx$$

**Sum/Difference Rule**:

$$\int [f(x) \pm g(x)] \, dx = \int f(x) \, dx \pm \int g(x) \, dx$$

### Important Antiderivatives to Memorize

| Function $f(x)$ | Antiderivative $\int f(x) \, dx$ |
|-----------------|----------------------------------|
| $k$ (constant) | $kx + C$ |
| $x^n$ $(n \neq -1)$ | $\frac{x^{n+1}}{n+1} + C$ |
| $\frac{1}{x}$ | $\ln|x| + C$ |
| $e^x$ | $e^x + C$ |
| $a^x$ | $\frac{a^x}{\ln a} + C$ |
| $\sin x$ | $-\cos x + C$ |
| $\cos x$ | $\sin x + C$ |
| $\sec^2 x$ | $\tan x + C$ |
| $\csc^2 x$ | $-\cot x + C$ |
| $\sec x \tan x$ | $\sec x + C$ |
| $\csc x \cot x$ | $-\csc x + C$ |
| $\frac{1}{\sqrt{1-x^2}}$ | $\arcsin x + C$ |
| $\frac{1}{1+x^2}$ | $\arctan x + C$ |

### Worked Examples

**Example 1**: Find $\int (3x^2 + 2x - 5) \, dx$

**Solution**:

Apply the sum rule and power rule term by term:

$$\int 3x^2 \, dx + \int 2x \, dx - \int 5 \, dx$$

$$= 3 \cdot \frac{x^3}{3} + 2 \cdot \frac{x^2}{2} - 5x + C$$

$$= x^3 + x^2 - 5x + C$$

**Verify**: $\frac{d}{dx}[x^3 + x^2 - 5x + C] = 3x^2 + 2x - 5$ ✓

---

**Example 2**: Find $\int \frac{4}{x^3} \, dx$

**Solution**:

First, rewrite using negative exponents:

$$\int 4x^{-3} \, dx = 4 \cdot \frac{x^{-2}}{-2} + C = -2x^{-2} + C = -\frac{2}{x^2} + C$$

---

**Example 3**: Find $\int (\sqrt{x} + \frac{1}{\sqrt{x}}) \, dx$

**Solution**:

Rewrite using fractional exponents:

$$\int (x^{1/2} + x^{-1/2}) \, dx$$

$$= \frac{x^{3/2}}{3/2} + \frac{x^{1/2}}{1/2} + C$$

$$= \frac{2}{3}x^{3/2} + 2x^{1/2} + C$$

$$= \frac{2}{3}x\sqrt{x} + 2\sqrt{x} + C$$

---

**Example 4**: Find $\int (e^x + \sin x) \, dx$

**Solution**:

$$= e^x + (-\cos x) + C = e^x - \cos x + C$$

---

**Example 5**: Find $\int \frac{x^3 + 2x - 1}{x^2} \, dx$

**Solution**:

Divide each term by $x^2$:

$$\int \left(\frac{x^3}{x^2} + \frac{2x}{x^2} - \frac{1}{x^2}\right) dx = \int (x + 2x^{-1} - x^{-2}) \, dx$$

$$= \frac{x^2}{2} + 2\ln|x| - \frac{x^{-1}}{-1} + C$$

$$= \frac{x^2}{2} + 2\ln|x| + \frac{1}{x} + C$$

---

### Initial Value Problems

An **initial value problem (IVP)** asks you to find a specific antiderivative that passes through a given point.

**Example 6**: Find $f(x)$ if $f'(x) = 6x^2 - 4x + 1$ and $f(0) = 3$.

**Solution**:

*Step 1*: Find the general antiderivative:

$$f(x) = \int (6x^2 - 4x + 1) \, dx = 2x^3 - 2x^2 + x + C$$

*Step 2*: Use the initial condition to find $C$:

$$f(0) = 2(0)^3 - 2(0)^2 + 0 + C = 3$$
$$C = 3$$

*Step 3*: Write the particular solution:

$$f(x) = 2x^3 - 2x^2 + x + 3$$

---

## Key Formulas & Rules

| Rule | Formula |
|------|---------|
| Power Rule | $\int x^n \, dx = \frac{x^{n+1}}{n+1} + C$ $(n \neq -1)$ |
| Constant Multiple | $\int k \cdot f(x) \, dx = k \int f(x) \, dx$ |
| Sum/Difference | $\int [f \pm g] \, dx = \int f \, dx \pm \int g \, dx$ |
| Special: $n = -1$ | $\int \frac{1}{x} \, dx = \ln|x| + C$ |

**Memory Trick for Trig**:
- Derivatives of "co-" functions have a negative sign
- Therefore, antiderivatives that produce "co-" functions need negative signs

---

## Common Mistakes to Avoid

1. **Forgetting +C**: Every indefinite integral needs a constant of integration.

2. **Wrong power rule application**: Don't forget to divide by the new exponent!
   - Wrong: $\int x^3 \, dx = x^4 + C$
   - Right: $\int x^3 \, dx = \frac{x^4}{4} + C$

3. **Using power rule for $\int \frac{1}{x} \, dx$**: The power rule gives $\frac{x^0}{0}$, which is undefined. Use $\ln|x| + C$ instead.

4. **Forgetting absolute value**: $\int \frac{1}{x} \, dx = \ln|x| + C$, not $\ln x + C$.

5. **Sign errors with trig functions**: Remember $\int \sin x \, dx = -\cos x + C$ (negative!).

6. **Trying to use product/quotient rules**: There's no simple "product rule" or "quotient rule" for integration. You must often simplify first.

---

## AP Exam Tips

### For Both AB and BC:
- Memorize all basic antiderivative formulas—they're tested frequently
- Always include +C for indefinite integrals
- Initial value problems appear regularly on free response sections
- Practice rewriting expressions (negative exponents, fractional exponents) before integrating

### Common Question Types:
1. **Direct integration**: Straightforward antiderivative calculation
2. **Initial value problems**: Find the particular antiderivative
3. **Particle motion**: Given velocity, find position
4. **Verify by differentiation**: Check your answer by taking the derivative

### Time-Saving Strategy:
When checking multiple choice answers, differentiate the answer choices to see which one gives the original integrand.

---

## Practice Problems

### Basic (Problems 1-5)

**1.** Find:

$$\int (4x^3 - 2x + 7) \, dx$$

---

**2.** Find:

$$\int \frac{5}{x^2} \, dx$$

---

**3.** Find:

$$\int (3\cos x - 2\sin x) \, dx$$

---

**4.** Find:

$$\int (e^x + 3^x) \, dx$$

---

**5.** Find:

$$\int \sqrt[3]{x^2} \, dx$$

---

### Intermediate (Problems 6-10)

**6.** Find:

$$\int \frac{x^4 - 3x^2 + 2}{x^2} \, dx$$

---

**7.** Find:

$$\int (\sqrt{x} - \frac{1}{\sqrt{x}})^2 \, dx$$

---

**8.** Solve the initial value problem:

$$f'(x) = 4x^3 - 6x, \quad f(1) = 2$$

---

**9.** Find:

$$\int \left(\sec^2 x + \frac{1}{1+x^2}\right) dx$$

---

**10.** Find all functions $f$ such that $f''(x) = 12x - 6$ and $f'(0) = 1$, $f(0) = 3$.

---

### Advanced (Problems 11-15)

**11.** Find:

$$\int \frac{(x+1)^2}{\sqrt{x}} \, dx$$

---

**12.** A particle moves along a line with acceleration $a(t) = 6t - 4$ m/s². If $v(0) = 5$ m/s and $s(0) = 2$ m, find the position function $s(t)$.

---

**13.** Find:

$$\int \frac{\sin x}{\cos^2 x} \, dx$$

*(Hint: Rewrite as a product)*

---

**14.** Find:

$$\int (2^x + 3^x)^2 \, dx$$

*(Hint: Expand first)*

---

**15.** The slope of a curve at any point $(x, y)$ is given by $\frac{dy}{dx} = 3x^2 - 4x + 1$. If the curve passes through $(2, 3)$, find the equation of the curve.

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

Evaluate:

$$\int (6x^2 - 4x + 3) \, dx$$

| Choice | Answer |
|--------|--------|
| **(A)** | $2x^3 - 2x^2 + 3x + C$ |
| **(B)** | $12x - 4 + C$ |
| **(C)** | $2x^3 - 2x^2 + 3 + C$ |
| **(D)** | $6x^3 - 4x^2 + 3x + C$ |

---

#### Problem 17 (Multiple Choice)

If $f'(x) = \sqrt{x}$ and $f(4) = 10$, then $f(x) =$

| Choice | Answer |
|--------|--------|
| **(A)** | $\frac{2}{3}x^{3/2} + \frac{14}{3}$ |
| **(B)** | $\frac{2}{3}x^{3/2} + C$ |
| **(C)** | $\frac{1}{2\sqrt{x}} + 10$ |
| **(D)** | $\frac{2}{3}x^{3/2} + 10$ |

---

#### Problem 18 (Free Response)

Let $f$ be a function such that $f''(x) = 6x + 2$.

> **(a)** Find the general form of $f'(x)$.
>
> **(b)** If $f'(1) = 4$, find the particular form of $f'(x)$.
>
> **(c)** Using your answer from part (b), and given that $f(0) = 1$, find $f(x)$.

---

#### Problem 19 (Multiple Choice)

Which of the following is an antiderivative of $f(x) = \frac{1}{x} + \frac{1}{x^2}$?

| Choice | Answer |
|--------|--------|
| **(A)** | $\ln x - \frac{1}{x}$ |
| **(B)** | $\ln|x| - \frac{1}{x}$ |
| **(C)** | $\ln|x| + \frac{1}{x}$ |
| **(D)** | $-\frac{1}{x^2} - \frac{2}{x^3}$ |

---

#### Problem 20 (Free Response - Challenging)

A particle moves along the x-axis with velocity given by $v(t) = t^2 - 4t + 3$ for $t \geq 0$.

> **(a)** Find the acceleration function $a(t)$.
>
> **(b)** Find the position function $s(t)$ if $s(0) = 2$.
>
> **(c)** At what time(s) does the particle change direction?
>
> **(d)** Find the total distance traveled by the particle from $t = 0$ to $t = 4$.

---

## Answer Key

<details>
<summary><strong>Problem 1 Solution</strong></summary>

**Answer**: $x^4 - x^2 + 7x + C$

**Step-by-step solution**:

Apply the power rule term by term:

$$\int 4x^3 \, dx - \int 2x \, dx + \int 7 \, dx$$

$$= 4 \cdot \frac{x^4}{4} - 2 \cdot \frac{x^2}{2} + 7x + C$$

$$= x^4 - x^2 + 7x + C$$

</details>

---

<details>
<summary><strong>Problem 2 Solution</strong></summary>

**Answer**: $-\frac{5}{x} + C$

**Step-by-step solution**:

Rewrite using negative exponent:

$$\int 5x^{-2} \, dx = 5 \cdot \frac{x^{-1}}{-1} + C = -5x^{-1} + C = -\frac{5}{x} + C$$

</details>

---

<details>
<summary><strong>Problem 3 Solution</strong></summary>

**Answer**: $3\sin x + 2\cos x + C$

**Step-by-step solution**:

$$\int 3\cos x \, dx - \int 2\sin x \, dx$$

$$= 3\sin x - 2(-\cos x) + C$$

$$= 3\sin x + 2\cos x + C$$

</details>

---

<details>
<summary><strong>Problem 4 Solution</strong></summary>

**Answer**: $e^x + \frac{3^x}{\ln 3} + C$

**Step-by-step solution**:

Using the formulas $\int e^x \, dx = e^x + C$ and $\int a^x \, dx = \frac{a^x}{\ln a} + C$:

$$\int e^x \, dx + \int 3^x \, dx = e^x + \frac{3^x}{\ln 3} + C$$

</details>

---

<details>
<summary><strong>Problem 5 Solution</strong></summary>

**Answer**: $\frac{3}{5}x^{5/3} + C$ or $\frac{3}{5}\sqrt[3]{x^5} + C$

**Step-by-step solution**:

Rewrite: $\sqrt[3]{x^2} = x^{2/3}$

$$\int x^{2/3} \, dx = \frac{x^{5/3}}{5/3} + C = \frac{3}{5}x^{5/3} + C$$

</details>

---

<details>
<summary><strong>Problem 6 Solution</strong></summary>

**Answer**: $\frac{x^3}{3} - 3x - \frac{2}{x} + C$

**Step-by-step solution**:

Divide each term by $x^2$:

$$\int \left(x^2 - 3 + 2x^{-2}\right) dx$$

$$= \frac{x^3}{3} - 3x + 2 \cdot \frac{x^{-1}}{-1} + C$$

$$= \frac{x^3}{3} - 3x - \frac{2}{x} + C$$

</details>

---

<details>
<summary><strong>Problem 7 Solution</strong></summary>

**Answer**: $\frac{x^2}{2} - 2x + \ln|x| + C$

**Step-by-step solution**:

First expand the square:

$$\left(\sqrt{x} - \frac{1}{\sqrt{x}}\right)^2 = x - 2\sqrt{x} \cdot \frac{1}{\sqrt{x}} + \frac{1}{x} = x - 2 + \frac{1}{x}$$

Now integrate:

$$\int \left(x - 2 + \frac{1}{x}\right) dx = \frac{x^2}{2} - 2x + \ln|x| + C$$

</details>

---

<details>
<summary><strong>Problem 8 Solution</strong></summary>

**Answer**: $f(x) = x^4 - 3x^2 + 4$

**Step-by-step solution**:

**Step 1**: Find the general antiderivative:

$$f(x) = \int (4x^3 - 6x) \, dx = x^4 - 3x^2 + C$$

**Step 2**: Use initial condition $f(1) = 2$:

$$f(1) = 1 - 3 + C = 2$$
$$C = 4$$

**Step 3**: The particular solution is:

$$f(x) = x^4 - 3x^2 + 4$$

</details>

---

<details>
<summary><strong>Problem 9 Solution</strong></summary>

**Answer**: $\tan x + \arctan x + C$

**Step-by-step solution**:

$$\int \sec^2 x \, dx + \int \frac{1}{1+x^2} \, dx$$

$$= \tan x + \arctan x + C$$

</details>

---

<details>
<summary><strong>Problem 10 Solution</strong></summary>

**Answer**: $f(x) = 2x^3 - 3x^2 + x + 3$

**Step-by-step solution**:

**Step 1**: Find $f'(x)$ by integrating $f''(x)$:

$$f'(x) = \int (12x - 6) \, dx = 6x^2 - 6x + C_1$$

**Step 2**: Use $f'(0) = 1$:

$$f'(0) = 0 - 0 + C_1 = 1 \Rightarrow C_1 = 1$$

So $f'(x) = 6x^2 - 6x + 1$

**Step 3**: Find $f(x)$ by integrating $f'(x)$:

$$f(x) = \int (6x^2 - 6x + 1) \, dx = 2x^3 - 3x^2 + x + C_2$$

**Step 4**: Use $f(0) = 3$:

$$f(0) = 0 + C_2 = 3 \Rightarrow C_2 = 3$$

**Final answer**: $f(x) = 2x^3 - 3x^2 + x + 3$

</details>

---

<details>
<summary><strong>Problem 11 Solution</strong></summary>

**Answer**: $\frac{2}{5}x^{5/2} + \frac{4}{3}x^{3/2} + 2x^{1/2} + C$

**Step-by-step solution**:

Expand $(x+1)^2 = x^2 + 2x + 1$, then divide by $\sqrt{x} = x^{1/2}$:

$$\frac{x^2 + 2x + 1}{x^{1/2}} = x^{3/2} + 2x^{1/2} + x^{-1/2}$$

Integrate:

$$\int (x^{3/2} + 2x^{1/2} + x^{-1/2}) \, dx$$

$$= \frac{x^{5/2}}{5/2} + 2 \cdot \frac{x^{3/2}}{3/2} + \frac{x^{1/2}}{1/2} + C$$

$$= \frac{2}{5}x^{5/2} + \frac{4}{3}x^{3/2} + 2\sqrt{x} + C$$

</details>

---

<details>
<summary><strong>Problem 12 Solution</strong></summary>

**Answer**: $s(t) = t^3 - 2t^2 + 5t + 2$

**Step-by-step solution**:

**Step 1**: Find velocity by integrating acceleration:

$$v(t) = \int (6t - 4) \, dt = 3t^2 - 4t + C_1$$

Using $v(0) = 5$: $C_1 = 5$

So $v(t) = 3t^2 - 4t + 5$

**Step 2**: Find position by integrating velocity:

$$s(t) = \int (3t^2 - 4t + 5) \, dt = t^3 - 2t^2 + 5t + C_2$$

Using $s(0) = 2$: $C_2 = 2$

**Final answer**: $s(t) = t^3 - 2t^2 + 5t + 2$

</details>

---

<details>
<summary><strong>Problem 13 Solution</strong></summary>

**Answer**: $\sec x + C$

**Step-by-step solution**:

Rewrite $\frac{\sin x}{\cos^2 x}$ as:

$$\frac{\sin x}{\cos^2 x} = \frac{1}{\cos x} \cdot \frac{\sin x}{\cos x} = \sec x \tan x$$

Therefore:

$$\int \sec x \tan x \, dx = \sec x + C$$

</details>

---

<details>
<summary><strong>Problem 14 Solution</strong></summary>

**Answer**: $\frac{4^x}{\ln 4} + \frac{2 \cdot 6^x}{\ln 6} + \frac{9^x}{\ln 9} + C$

**Step-by-step solution**:

Expand $(2^x + 3^x)^2$:

$$= (2^x)^2 + 2(2^x)(3^x) + (3^x)^2 = 4^x + 2 \cdot 6^x + 9^x$$

Integrate:

$$\int (4^x + 2 \cdot 6^x + 9^x) \, dx = \frac{4^x}{\ln 4} + \frac{2 \cdot 6^x}{\ln 6} + \frac{9^x}{\ln 9} + C$$

</details>

---

<details>
<summary><strong>Problem 15 Solution</strong></summary>

**Answer**: $y = x^3 - 2x^2 + x - 1$

**Step-by-step solution**:

**Step 1**: Integrate $\frac{dy}{dx}$ to find $y$:

$$y = \int (3x^2 - 4x + 1) \, dx = x^3 - 2x^2 + x + C$$

**Step 2**: Use the point $(2, 3)$:

$$3 = 8 - 8 + 2 + C = 2 + C$$
$$C = 1$$

Wait, let me recalculate:
$$3 = (2)^3 - 2(2)^2 + 2 + C = 8 - 8 + 2 + C = 2 + C$$
$$C = 1$$

**Final answer**: $y = x^3 - 2x^2 + x + 1$

Actually, let me verify: at $x = 2$: $8 - 8 + 2 + 1 = 3$ ✓

</details>

---

<details>
<summary><strong>Problem 16 Solution</strong></summary>

**Answer**: **(A)** $2x^3 - 2x^2 + 3x + C$

**Step-by-step solution**:

$$\int (6x^2 - 4x + 3) \, dx = 6 \cdot \frac{x^3}{3} - 4 \cdot \frac{x^2}{2} + 3x + C$$

$$= 2x^3 - 2x^2 + 3x + C$$

</details>

---

<details>
<summary><strong>Problem 17 Solution</strong></summary>

**Answer**: **(A)** $\frac{2}{3}x^{3/2} + \frac{14}{3}$

**Step-by-step solution**:

**Step 1**: Integrate $f'(x) = \sqrt{x} = x^{1/2}$:

$$f(x) = \frac{x^{3/2}}{3/2} + C = \frac{2}{3}x^{3/2} + C$$

**Step 2**: Use $f(4) = 10$:

$$f(4) = \frac{2}{3}(4)^{3/2} + C = \frac{2}{3}(8) + C = \frac{16}{3} + C = 10$$

$$C = 10 - \frac{16}{3} = \frac{30 - 16}{3} = \frac{14}{3}$$

**Final answer**: $f(x) = \frac{2}{3}x^{3/2} + \frac{14}{3}$

</details>

---

<details>
<summary><strong>Problem 18 Solution</strong></summary>

**Answer**: See detailed solution below.

**(a)** General form of $f'(x)$:

$$f'(x) = \int (6x + 2) \, dx = 3x^2 + 2x + C$$

**(b)** Using $f'(1) = 4$:

$$f'(1) = 3(1)^2 + 2(1) + C = 3 + 2 + C = 4$$
$$C = -1$$

So $f'(x) = 3x^2 + 2x - 1$

**(c)** Find $f(x)$:

$$f(x) = \int (3x^2 + 2x - 1) \, dx = x^3 + x^2 - x + K$$

Using $f(0) = 1$:

$$f(0) = 0 + 0 - 0 + K = 1$$
$$K = 1$$

**Final answer**: $f(x) = x^3 + x^2 - x + 1$

</details>

---

<details>
<summary><strong>Problem 19 Solution</strong></summary>

**Answer**: **(B)** $\ln|x| - \frac{1}{x}$

**Step-by-step solution**:

$$\int \left(\frac{1}{x} + \frac{1}{x^2}\right) dx = \int \frac{1}{x} \, dx + \int x^{-2} \, dx$$

$$= \ln|x| + \frac{x^{-1}}{-1} + C = \ln|x| - \frac{1}{x} + C$$

The question asks for "an antiderivative" (not the general antiderivative), so we can use $C = 0$.

Answer: $\ln|x| - \frac{1}{x}$

Note: Choice (A) is wrong because it's missing the absolute value in $\ln|x|$.

</details>

---

<details>
<summary><strong>Problem 20 Solution</strong></summary>

**Answer**: See detailed solution below.

**(a)** Acceleration function:

$$a(t) = v'(t) = 2t - 4$$

**(b)** Position function:

$$s(t) = \int (t^2 - 4t + 3) \, dt = \frac{t^3}{3} - 2t^2 + 3t + C$$

Using $s(0) = 2$:
$$s(0) = 0 + C = 2 \Rightarrow C = 2$$

$$s(t) = \frac{t^3}{3} - 2t^2 + 3t + 2$$

**(c)** Direction changes when velocity changes sign:

$$v(t) = t^2 - 4t + 3 = (t-1)(t-3) = 0$$

$t = 1$ and $t = 3$

Verify sign changes:
- $v(0) = 3 > 0$ (moving right)
- $v(2) = -1 < 0$ (moving left)
- $v(4) = 3 > 0$ (moving right)

Particle changes direction at $t = 1$ and $t = 3$.

**(d)** Total distance from $t = 0$ to $t = 4$:

Calculate positions:
- $s(0) = 2$
- $s(1) = \frac{1}{3} - 2 + 3 + 2 = \frac{10}{3}$
- $s(3) = 9 - 18 + 9 + 2 = 2$
- $s(4) = \frac{64}{3} - 32 + 12 + 2 = \frac{64}{3} - 18 = \frac{10}{3}$

Total distance:
$$= |s(1) - s(0)| + |s(3) - s(1)| + |s(4) - s(3)|$$
$$= \left|\frac{10}{3} - 2\right| + \left|2 - \frac{10}{3}\right| + \left|\frac{10}{3} - 2\right|$$
$$= \frac{4}{3} + \frac{4}{3} + \frac{4}{3} = 4$$

**Total distance = 4 units**

</details>

---

## What's Next

Now that you understand antiderivatives, you're ready for [Riemann Sums](/calculus/riemann-sums), where we'll discover how to use rectangles to approximate the area under a curve—setting the stage for the definite integral.

---

<div align="center">

[← Curve Sketching](/calculus/curve-sketching) | [Riemann Sums →](/calculus/riemann-sums)

</div>
