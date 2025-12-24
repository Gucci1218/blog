# Exponential Functions
<p class="article-date">July 29, 2024</p>

## Prerequisites
Before diving in, make sure you're comfortable with:
- Properties of exponents
- [Transformations](/calculus/0104-transformations)
- Basic function concepts

## Learning Objectives
By the end of this section, you will be able to:
- Identify exponential functions and their key properties
- Graph exponential functions with transformations
- Understand the number $e$ and its significance
- Solve basic exponential equations
- Apply exponential functions to growth and decay problems

## The Big Picture: Multiplicative Growth

Exponential functions model situations where quantities multiply by a constant factor:

- Population doubling every year
- Radioactive decay (halving every period)
- Compound interest
- Viral spread

> **Key Insight**: In exponential functions, the variable is in the exponent, not the base.

## Definition of Exponential Functions

An **exponential function** has the form:
$$f(x) = a \cdot b^x$$

where:
- $a$ is the initial value (y-intercept when $x = 0$)
- $b$ is the base (growth/decay factor)
- $b > 0$ and $b \ne 1$

### Growth vs. Decay

| Condition | Behavior | Example |
|-----------|----------|---------|
| $b > 1$ | Exponential growth | $f(x) = 2^x$ |
| $0 < b < 1$ | Exponential decay | $f(x) = \left(\frac{1}{2}\right)^x$ |

## Properties of Exponential Functions

### Basic Properties

For $f(x) = b^x$ where $b > 0$, $b \ne 1$:

| Property | Value/Description |
|----------|-------------------|
| Domain | $(-\infty, \infty)$ |
| Range | $(0, \infty)$ |
| y-intercept | $(0, 1)$ |
| x-intercept | None |
| Horizontal asymptote | $y = 0$ |
| Behavior | One-to-one (passes horizontal line test) |

### Key Points

For $f(x) = b^x$:
- $f(0) = 1$ (always)
- $f(1) = b$
- $f(-1) = \frac{1}{b}$

## The Natural Base $e$

### Definition

The number $e$ is defined as:
$$e = \lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n \approx 2.71828...$$

### Why $e$ is Special

The function $f(x) = e^x$ has a remarkable property:

$$\frac{d}{dx}[e^x] = e^x$$

It's the only function that equals its own derivative!

### The Natural Exponential Function

$$f(x) = e^x$$

| Property | Value |
|----------|-------|
| Domain | $(-\infty, \infty)$ |
| Range | $(0, \infty)$ |
| y-intercept | $(0, 1)$ |
| Key point | $(1, e) \approx (1, 2.718)$ |
| Growth rate | Fastest at any point equals the function value |

## Graphs of Exponential Functions

### Basic Graph: $f(x) = b^x$

For $b > 1$ (growth):
- Increases from left to right
- Steeper as $x$ increases
- Approaches 0 as $x \to -\infty$

For $0 < b < 1$ (decay):
- Decreases from left to right
- Steeper as $x$ decreases
- Approaches 0 as $x \to \infty$

### Transformations

$$f(x) = a \cdot b^{x-h} + k$$

| Parameter | Effect |
|-----------|--------|
| $a$ | Vertical stretch/compression, reflection if negative |
| $h$ | Horizontal shift |
| $k$ | Vertical shift (moves asymptote to $y = k$) |

## Laws of Exponents

These rules are essential for working with exponentials:

| Rule | Formula |
|------|---------|
| Product Rule | $b^m \cdot b^n = b^{m+n}$ |
| Quotient Rule | $\frac{b^m}{b^n} = b^{m-n}$ |
| Power Rule | $(b^m)^n = b^{mn}$ |
| Zero Exponent | $b^0 = 1$ |
| Negative Exponent | $b^{-n} = \frac{1}{b^n}$ |
| Fractional Exponent | $b^{m/n} = \sqrt[n]{b^m}$ |

## Solving Exponential Equations

### Method 1: Same Base

If you can write both sides with the same base:
$$b^{f(x)} = b^{g(x)} \implies f(x) = g(x)$$

**Example**: Solve $2^{3x} = 8$

$8 = 2^3$, so $2^{3x} = 2^3$

$3x = 3 \implies x = 1$

### Method 2: Using Logarithms

When bases can't be matched, take the log of both sides:

**Example**: Solve $3^x = 20$

$\ln(3^x) = \ln(20)$

$x \ln 3 = \ln 20$

$x = \frac{\ln 20}{\ln 3} \approx 2.727$

## Applications

### Compound Interest

$$A = P\left(1 + \frac{r}{n}\right)^{nt}$$

where:
- $A$ = final amount
- $P$ = principal (initial investment)
- $r$ = annual interest rate (as decimal)
- $n$ = number of times compounded per year
- $t$ = time in years

### Continuous Compounding

$$A = Pe^{rt}$$

### Exponential Growth/Decay

$$A(t) = A_0 \cdot e^{kt}$$

- $k > 0$: growth
- $k < 0$: decay
- $A_0$: initial amount

### Half-Life Formula

$$A(t) = A_0 \cdot \left(\frac{1}{2}\right)^{t/h}$$

where $h$ is the half-life.

## Worked Example 1: Graphing

**Problem**: Graph $f(x) = 2^{x-1} - 3$

**Solution**:

Start with $y = 2^x$:
- Point: $(0, 1)$, $(1, 2)$, $(-1, \frac{1}{2})$
- Asymptote: $y = 0$

Apply transformations:
1. Shift right 1: $(1, 1)$, $(2, 2)$, $(0, \frac{1}{2})$
2. Shift down 3: $(1, -2)$, $(2, -1)$, $(0, -2.5)$

New asymptote: $y = -3$

## Worked Example 2: Solving Equations

**Problem**: Solve $5^{2x-1} = 125$

**Solution**:

Write 125 as a power of 5: $125 = 5^3$

$5^{2x-1} = 5^3$

$2x - 1 = 3$

$2x = 4$

$x = 2$

## Worked Example 3: Application

**Problem**: A bacteria population doubles every 3 hours. Starting with 500 bacteria, how many are there after 12 hours?

**Solution**:

Use $A(t) = A_0 \cdot 2^{t/d}$ where $d$ is doubling time.

$A(12) = 500 \cdot 2^{12/3} = 500 \cdot 2^4 = 500 \cdot 16 = 8000$

## Key Formulas Summary

| Formula | Description |
|---------|-------------|
| $f(x) = b^x$ | Basic exponential function |
| $f(x) = e^x$ | Natural exponential |
| $e \approx 2.71828$ | The natural base |
| $A = Pe^{rt}$ | Continuous compound interest |
| $A(t) = A_0 e^{kt}$ | Exponential growth/decay |

## Common Mistakes to Avoid

1. **Confusing $e^x$ with $x^e$**
   - $e^x$: exponential function (variable in exponent)
   - $x^e$: power function (variable in base)

2. **Wrong exponent rules**
   - $(2^3)^2 = 2^6$, not $2^9$
   - $2^3 \cdot 2^2 = 2^5$, not $2^6$

3. **Forgetting that $b^0 = 1$**
   - This gives the y-intercept

4. **Thinking exponential functions can equal zero**
   - $b^x > 0$ for all $x$ (never crosses x-axis)

5. **Confusing growth rate with growth factor**
   - If something grows 5% per year: factor = 1.05, rate = 0.05

## Calculus Connection

Exponential functions are central to calculus:

1. **Derivatives**: $\frac{d}{dx}[e^x] = e^x$ and $\frac{d}{dx}[b^x] = b^x \ln b$

2. **Integrals**: $\int e^x \, dx = e^x + C$ and $\int b^x \, dx = \frac{b^x}{\ln b} + C$

3. **Differential Equations**: $\frac{dy}{dx} = ky$ has solution $y = Ce^{kx}$

4. **Limits**: $\lim_{x \to \infty} e^x = \infty$ and $\lim_{x \to -\infty} e^x = 0$

---

## Practice Problems

### Basic (Computational)

**Problem 1**
Evaluate $3^{-2}$.

<details>
<summary>Show Solution</summary>

**Solution**:
$$3^{-2} = \frac{1}{3^2} = \frac{1}{9}$$
</details>

---

**Problem 2**
Simplify $2^5 \cdot 2^3$.

<details>
<summary>Show Solution</summary>

**Solution**:
$$2^5 \cdot 2^3 = 2^{5+3} = 2^8 = 256$$
</details>

---

**Problem 3**
Find the y-intercept of $f(x) = 5 \cdot 3^x$.

<details>
<summary>Show Solution</summary>

**Solution**:
$$f(0) = 5 \cdot 3^0 = 5 \cdot 1 = 5$$

y-intercept: $(0, 5)$
</details>

---

**Problem 4**
Solve: $4^x = 64$

<details>
<summary>Show Solution</summary>

**Solution**:
$$4^x = 4^3$$
$$x = 3$$
</details>

---

**Problem 5**
Is $f(x) = 0.5^x$ an example of growth or decay?

<details>
<summary>Show Solution</summary>

**Solution**:
Since the base $0.5 < 1$, this is **exponential decay**.

As $x$ increases, $0.5^x$ decreases toward 0.
</details>

---

### Intermediate (Multi-step)

**Problem 6**
Solve: $9^x = 27$

<details>
<summary>Show Solution</summary>

**Solution**:
Write both sides as powers of 3:
$$9 = 3^2 \text{ and } 27 = 3^3$$
$$(3^2)^x = 3^3$$
$$3^{2x} = 3^3$$
$$2x = 3$$
$$x = \frac{3}{2}$$
</details>

---

**Problem 7**
Graph $f(x) = -2^x + 4$ and identify the asymptote.

<details>
<summary>Show Solution</summary>

**Solution**:
Starting from $y = 2^x$:
1. Reflect over x-axis: $y = -2^x$
2. Shift up 4: $y = -2^x + 4$

Key points:
- Original $(0, 1)$ → $(0, -1)$ → $(0, 3)$
- Original $(1, 2)$ → $(1, -2)$ → $(1, 2)$

**Asymptote**: $y = 4$
</details>

---

**Problem 8**
Solve: $e^{2x} = 7$

<details>
<summary>Show Solution</summary>

**Solution**:
$$\ln(e^{2x}) = \ln 7$$
$$2x = \ln 7$$
$$x = \frac{\ln 7}{2} \approx 0.973$$
</details>

---

**Problem 9**
If $\$1000$ is invested at 6% annual interest compounded monthly, find the amount after 5 years.

<details>
<summary>Show Solution</summary>

**Solution**:
$$A = P\left(1 + \frac{r}{n}\right)^{nt}$$
$$A = 1000\left(1 + \frac{0.06}{12}\right)^{12 \cdot 5}$$
$$A = 1000(1.005)^{60}$$
$$A \approx 1000(1.3489) = \$1348.85$$
</details>

---

**Problem 10**
A radioactive substance has a half-life of 10 years. What fraction remains after 30 years?

<details>
<summary>Show Solution</summary>

**Solution**:
$$A(t) = A_0 \cdot \left(\frac{1}{2}\right)^{t/h}$$
$$A(30) = A_0 \cdot \left(\frac{1}{2}\right)^{30/10}$$
$$= A_0 \cdot \left(\frac{1}{2}\right)^3 = A_0 \cdot \frac{1}{8}$$

**Answer**: $\frac{1}{8}$ of the original remains.
</details>

---

### Advanced (Complex Applications)

**Problem 11**
Solve: $2^{x+1} = 3^{x-1}$

<details>
<summary>Show Solution</summary>

**Solution**:
Take natural log of both sides:
$$\ln(2^{x+1}) = \ln(3^{x-1})$$
$$(x+1)\ln 2 = (x-1)\ln 3$$
$$x\ln 2 + \ln 2 = x\ln 3 - \ln 3$$
$$x\ln 2 - x\ln 3 = -\ln 3 - \ln 2$$
$$x(\ln 2 - \ln 3) = -(\ln 3 + \ln 2)$$
$$x = \frac{-\ln 6}{\ln 2 - \ln 3} = \frac{\ln 6}{\ln 3 - \ln 2} = \frac{\ln 6}{\ln(3/2)}$$
$$x \approx \frac{1.792}{0.405} \approx 4.42$$
</details>

---

**Problem 12**
The population of a city grows according to $P(t) = 50000e^{0.03t}$ where $t$ is years after 2020. In what year will the population reach 75,000?

<details>
<summary>Show Solution</summary>

**Solution**:
$$75000 = 50000e^{0.03t}$$
$$1.5 = e^{0.03t}$$
$$\ln 1.5 = 0.03t$$
$$t = \frac{\ln 1.5}{0.03} \approx \frac{0.405}{0.03} \approx 13.5$$

The population reaches 75,000 approximately **13.5 years after 2020**, so around mid-2033.
</details>

---

**Problem 13**
Find the value of $x$ if $e^x + e^{-x} = 4$.

<details>
<summary>Show Solution</summary>

**Solution**:
Let $u = e^x$, so $e^{-x} = \frac{1}{u}$:
$$u + \frac{1}{u} = 4$$
$$u^2 + 1 = 4u$$
$$u^2 - 4u + 1 = 0$$
$$u = \frac{4 \pm \sqrt{16-4}}{2} = \frac{4 \pm \sqrt{12}}{2} = 2 \pm \sqrt{3}$$

Since $u = e^x > 0$, both solutions are valid:
$$e^x = 2 + \sqrt{3} \implies x = \ln(2 + \sqrt{3})$$
$$e^x = 2 - \sqrt{3} \implies x = \ln(2 - \sqrt{3}) = -\ln(2 + \sqrt{3})$$

**Solutions**: $x = \pm\ln(2 + \sqrt{3}) \approx \pm 1.317$
</details>

---

**Problem 14**
Compare the growth of $f(x) = 2^x$ and $g(x) = x^2$ for large $x$.

<details>
<summary>Show Solution</summary>

**Solution**:
For small $x$, $x^2$ may be larger. But as $x$ increases:

| $x$ | $2^x$ | $x^2$ |
|-----|-------|-------|
| 2 | 4 | 4 |
| 5 | 32 | 25 |
| 10 | 1024 | 100 |
| 20 | $\approx 10^6$ | 400 |

Exponential functions eventually dominate polynomial functions:
$$\lim_{x \to \infty} \frac{2^x}{x^2} = \infty$$

**$2^x$ grows much faster than $x^2$ for large $x$.**
</details>

---

**Problem 15**
Simplify: $\dfrac{e^{3x} \cdot e^{-x}}{e^{x+1}}$

<details>
<summary>Show Solution</summary>

**Solution**:
$$\frac{e^{3x} \cdot e^{-x}}{e^{x+1}} = \frac{e^{3x-x}}{e^{x+1}} = \frac{e^{2x}}{e^{x+1}}$$
$$= e^{2x-(x+1)} = e^{2x-x-1} = e^{x-1}$$
</details>

---

### AP Exam Style

**Problem 16**
If $f(x) = 3e^{2x}$, find $f'(x)$.

<details>
<summary>Show Solution</summary>

**Solution**:
Using chain rule:
$$f'(x) = 3 \cdot e^{2x} \cdot 2 = 6e^{2x}$$
</details>

---

**Problem 17**
Which function has a horizontal asymptote at $y = 5$?

(A) $f(x) = 5e^x$
(B) $f(x) = e^x + 5$
(C) $f(x) = e^{x-5}$
(D) $f(x) = 5 - e^{-x}$

<details>
<summary>Show Solution</summary>

**Solution**:
As $x \to \infty$:
- (A) $\to \infty$
- (B) $\to \infty$
- (C) $\to \infty$
- (D) $5 - e^{-x} \to 5 - 0 = 5$ ✓

**Answer: (D)**
</details>

---

**Problem 18**
Solve $5 \cdot 2^x = 40$ for $x$.

<details>
<summary>Show Solution</summary>

**Solution**:
$$2^x = 8 = 2^3$$
$$x = 3$$
</details>

---

**Problem 19** *(Free Response Style)*
A cup of coffee cools according to Newton's Law of Cooling: $T(t) = 70 + 130e^{-0.05t}$, where $T$ is in °F and $t$ is in minutes.

(a) What is the initial temperature of the coffee?
(b) What is the temperature of the room?
(c) When will the coffee reach 100°F?
(d) Find the rate of cooling at $t = 10$ minutes.

<details>
<summary>Show Solution</summary>

**Solution**:

**(a)** $T(0) = 70 + 130e^0 = 70 + 130 = 200°F$

**(b)** As $t \to \infty$, $e^{-0.05t} \to 0$, so $T \to 70°F$. Room temperature is **70°F**.

**(c)** Solve $100 = 70 + 130e^{-0.05t}$:
$$30 = 130e^{-0.05t}$$
$$\frac{30}{130} = e^{-0.05t}$$
$$\ln\frac{3}{13} = -0.05t$$
$$t = \frac{-\ln(3/13)}{0.05} = \frac{\ln(13/3)}{0.05} \approx 29.5 \text{ minutes}$$

**(d)** $T'(t) = 130 \cdot (-0.05) \cdot e^{-0.05t} = -6.5e^{-0.05t}$

$T'(10) = -6.5e^{-0.5} \approx -6.5(0.607) \approx -3.94°F/min$

The coffee is cooling at about **3.94°F per minute** at $t = 10$.
</details>

---

**Problem 20** *(Free Response Style)*
The value of an investment is modeled by $V(t) = 1000e^{0.08t}$ where $t$ is in years.

(a) What is the initial investment?
(b) What is the annual growth rate (as a percentage)?
(c) How long until the investment doubles?
(d) What is the instantaneous rate of change of the investment at $t = 5$ years?

<details>
<summary>Show Solution</summary>

**Solution**:

**(a)** $V(0) = 1000e^0 = \$1000$

**(b)** The continuous growth rate is 8%. To find effective annual rate:
$$e^{0.08} \approx 1.0833$$
Effective annual rate: about **8.33%**

**(c)** Solve $2000 = 1000e^{0.08t}$:
$$2 = e^{0.08t}$$
$$\ln 2 = 0.08t$$
$$t = \frac{\ln 2}{0.08} \approx 8.66 \text{ years}$$

**(d)** $V'(t) = 1000 \cdot 0.08 \cdot e^{0.08t} = 80e^{0.08t}$

$V'(5) = 80e^{0.4} \approx 80(1.492) \approx \$119.35/year$

The investment is growing at about **\$119.35 per year** at $t = 5$.
</details>

---

## What's Next

Now that you've mastered exponential functions, you're ready to explore [Logarithmic Functions](/calculus/0112-logarithmic-functions), the inverses of exponential functions that are essential for solving exponential equations and for calculus integration.

---

<div align="center">

[← Inverse Trig Functions](/calculus/0110-inverse-trig-functions) | [Logarithmic Functions →](/calculus/0112-logarithmic-functions)

</div>
