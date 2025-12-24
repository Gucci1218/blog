# Logarithmic Functions
<p class="article-date">August 1, 2024</p>

## Prerequisites
Before diving in, make sure you're comfortable with:
- [Exponential Functions](/calculus/0111-exponential-functions)
- [Inverse Functions](/calculus/0103-inverse-functions)
- Properties of exponents

## Learning Objectives
By the end of this section, you will be able to:
- Understand logarithms as inverses of exponential functions
- Convert between exponential and logarithmic form
- Apply properties of logarithms to simplify expressions
- Solve logarithmic equations
- Graph logarithmic functions with transformations
- Use logarithms in real-world applications

## The Big Picture: Undoing Exponents

A **logarithm** answers the question: "What exponent gives me this result?"

$$\log_b(x) = y \quad \text{means} \quad b^y = x$$

> **Key Insight**: Logarithms are the inverse of exponential functions. If $f(x) = b^x$, then $f^{-1}(x) = \log_b(x)$.

### Example
$\log_2(8) = 3$ because $2^3 = 8$

"The power you raise 2 to in order to get 8 is 3."

## Converting Between Forms

| Exponential Form | Logarithmic Form |
|------------------|------------------|
| $b^y = x$ | $\log_b(x) = y$ |
| $2^3 = 8$ | $\log_2(8) = 3$ |
| $10^2 = 100$ | $\log_{10}(100) = 2$ |
| $e^1 = e$ | $\ln(e) = 1$ |
| $5^0 = 1$ | $\log_5(1) = 0$ |

## Common and Natural Logarithms

### Common Logarithm (Base 10)
$$\log(x) = \log_{10}(x)$$

Used for: pH scale, decibels, Richter scale

### Natural Logarithm (Base $e$)
$$\ln(x) = \log_e(x)$$

Used for: Calculus, continuous growth/decay, most scientific applications

## Properties of Logarithms

### Basic Properties

| Property | Formula | Example |
|----------|---------|---------|
| Log of 1 | $\log_b(1) = 0$ | $\log_5(1) = 0$ |
| Log of base | $\log_b(b) = 1$ | $\ln(e) = 1$ |
| Inverse property | $b^{\log_b(x)} = x$ | $10^{\log(5)} = 5$ |
| Inverse property | $\log_b(b^x) = x$ | $\ln(e^3) = 3$ |

### Logarithm Laws

| Law | Formula |
|-----|---------|
| Product Rule | $\log_b(xy) = \log_b(x) + \log_b(y)$ |
| Quotient Rule | $\log_b\left(\frac{x}{y}\right) = \log_b(x) - \log_b(y)$ |
| Power Rule | $\log_b(x^n) = n\log_b(x)$ |
| Change of Base | $\log_b(x) = \frac{\log_a(x)}{\log_a(b)} = \frac{\ln(x)}{\ln(b)}$ |

### Memory Aid
- Multiplication inside → Addition outside
- Division inside → Subtraction outside
- Power inside → Multiplication outside

## Worked Example 1: Expanding Logarithms

**Problem**: Expand $\log\left(\frac{x^3y^2}{z}\right)$

**Solution**:
$$= \log(x^3y^2) - \log(z)$$
$$= \log(x^3) + \log(y^2) - \log(z)$$
$$= 3\log(x) + 2\log(y) - \log(z)$$

## Worked Example 2: Condensing Logarithms

**Problem**: Write as a single logarithm: $2\ln(x) - \ln(y) + \frac{1}{2}\ln(z)$

**Solution**:
$$= \ln(x^2) - \ln(y) + \ln(z^{1/2})$$
$$= \ln(x^2) + \ln(\sqrt{z}) - \ln(y)$$
$$= \ln\left(\frac{x^2\sqrt{z}}{y}\right)$$

## Worked Example 3: Using Change of Base

**Problem**: Evaluate $\log_3(20)$ using natural logarithms.

**Solution**:
$$\log_3(20) = \frac{\ln(20)}{\ln(3)} = \frac{2.996}{1.099} \approx 2.727$$

## Graphs of Logarithmic Functions

### Basic Graph: $f(x) = \log_b(x)$

| Property | Value |
|----------|-------|
| Domain | $(0, \infty)$ |
| Range | $(-\infty, \infty)$ |
| x-intercept | $(1, 0)$ |
| Vertical asymptote | $x = 0$ |
| Key point | $(b, 1)$ |

### Behavior
- For $b > 1$: Increasing function
- For $0 < b < 1$: Decreasing function
- Passes through $(1, 0)$ always

### Transformations

$$f(x) = a\log_b(x - h) + k$$

| Parameter | Effect |
|-----------|--------|
| $h$ | Horizontal shift (asymptote at $x = h$) |
| $k$ | Vertical shift |
| $a > 0$ | Vertical stretch |
| $a < 0$ | Vertical stretch + reflection |

## Solving Logarithmic Equations

### Method 1: Convert to Exponential Form

**Example**: Solve $\log_2(x) = 5$

Convert: $2^5 = x$

$x = 32$

### Method 2: Use Properties to Combine

**Example**: Solve $\log(x) + \log(x - 3) = 1$

$$\log(x(x-3)) = 1$$
$$x(x - 3) = 10^1 = 10$$
$$x^2 - 3x - 10 = 0$$
$$(x - 5)(x + 2) = 0$$
$$x = 5 \text{ or } x = -2$$

Check: $x = -2$ is invalid (can't take log of negative)

**Solution**: $x = 5$

### Method 3: Take Logarithm of Both Sides

**Example**: Solve $3^x = 15$

$$\log(3^x) = \log(15)$$
$$x\log(3) = \log(15)$$
$$x = \frac{\log(15)}{\log(3)} \approx 2.465$$

## Domain Restrictions

**Critical Rule**: The argument of a logarithm must be positive.

$\log_b(f(x))$ requires $f(x) > 0$

### Example
Find the domain of $f(x) = \ln(2x - 6)$

Require: $2x - 6 > 0$
$$x > 3$$

**Domain**: $(3, \infty)$

## Applications

### pH Scale
$$\text{pH} = -\log[H^+]$$

### Decibels
$$dB = 10\log\left(\frac{I}{I_0}\right)$$

### Earthquake Magnitude (Richter)
$$M = \log\left(\frac{A}{A_0}\right)$$

### Time to Double/Triple
If $A = A_0 e^{rt}$, time to double:
$$t = \frac{\ln 2}{r}$$

## Key Formulas Summary

| Formula | Description |
|---------|-------------|
| $\log_b(x) = y \Leftrightarrow b^y = x$ | Definition |
| $\log_b(xy) = \log_b x + \log_b y$ | Product rule |
| $\log_b(x/y) = \log_b x - \log_b y$ | Quotient rule |
| $\log_b(x^n) = n\log_b x$ | Power rule |
| $\log_b x = \frac{\ln x}{\ln b}$ | Change of base |
| $\ln(e^x) = x$ and $e^{\ln x} = x$ | Inverse properties |

## Common Mistakes to Avoid

1. **Wrong domain**
   - $\log(-4)$ is undefined
   - Always check that arguments are positive

2. **Incorrect log rules**
   - $\log(x + y) \ne \log(x) + \log(y)$
   - $\log(x - y) \ne \log(x) - \log(y)$

3. **Forgetting to check solutions**
   - Extraneous solutions can arise when squaring or combining logs

4. **Confusing $\ln(x)$ and $\log(x)$**
   - $\ln$ is base $e$
   - $\log$ (no base shown) typically means base 10

5. **Wrong change of base direction**
   - $\log_b(x) = \frac{\ln x}{\ln b}$, not $\frac{\ln b}{\ln x}$

## Calculus Connection

Logarithms are essential in calculus:

1. **Derivatives**:
   $$\frac{d}{dx}[\ln x] = \frac{1}{x}$$
   $$\frac{d}{dx}[\log_b x] = \frac{1}{x \ln b}$$

2. **Integrals**:
   $$\int \frac{1}{x} dx = \ln|x| + C$$

3. **Logarithmic Differentiation**: For $y = x^x$, take $\ln$ of both sides first

4. **Growth/Decay**: Solving for time in $A = A_0 e^{kt}$

---

## Practice Problems

### Basic (Computational)

**Problem 1**
Convert to logarithmic form: $5^3 = 125$

<details>
<summary>Show Solution</summary>

**Solution**:
$$\log_5(125) = 3$$
</details>

---

**Problem 2**
Evaluate: $\log_4(16)$

<details>
<summary>Show Solution</summary>

**Solution**:
$4^? = 16$

$4^2 = 16$

$$\log_4(16) = 2$$
</details>

---

**Problem 3**
Evaluate: $\ln(e^5)$

<details>
<summary>Show Solution</summary>

**Solution**:
Using the inverse property:
$$\ln(e^5) = 5$$
</details>

---

**Problem 4**
Evaluate: $10^{\log(7)}$

<details>
<summary>Show Solution</summary>

**Solution**:
Using the inverse property:
$$10^{\log(7)} = 7$$
</details>

---

**Problem 5**
Find the domain of $f(x) = \log(x - 5)$.

<details>
<summary>Show Solution</summary>

**Solution**:
Require $x - 5 > 0$:
$$x > 5$$

**Domain**: $(5, \infty)$
</details>

---

### Intermediate (Multi-step)

**Problem 6**
Expand: $\ln\left(\dfrac{x^4}{y^2z}\right)$

<details>
<summary>Show Solution</summary>

**Solution**:
$$= \ln(x^4) - \ln(y^2z)$$
$$= \ln(x^4) - [\ln(y^2) + \ln(z)]$$
$$= 4\ln(x) - 2\ln(y) - \ln(z)$$
</details>

---

**Problem 7**
Condense: $3\log(x) - \log(y) + \frac{1}{2}\log(z)$

<details>
<summary>Show Solution</summary>

**Solution**:
$$= \log(x^3) - \log(y) + \log(z^{1/2})$$
$$= \log\left(\frac{x^3 \cdot \sqrt{z}}{y}\right)$$
</details>

---

**Problem 8**
Solve: $\log_3(x) = 4$

<details>
<summary>Show Solution</summary>

**Solution**:
Convert to exponential form:
$$3^4 = x$$
$$x = 81$$
</details>

---

**Problem 9**
Solve: $2^{x+1} = 7$

<details>
<summary>Show Solution</summary>

**Solution**:
$$\ln(2^{x+1}) = \ln(7)$$
$$(x+1)\ln(2) = \ln(7)$$
$$x + 1 = \frac{\ln 7}{\ln 2}$$
$$x = \frac{\ln 7}{\ln 2} - 1 \approx 2.807 - 1 = 1.807$$
</details>

---

**Problem 10**
Solve: $\log(x) + \log(x + 9) = 1$

<details>
<summary>Show Solution</summary>

**Solution**:
$$\log(x(x + 9)) = 1$$
$$x(x + 9) = 10$$
$$x^2 + 9x - 10 = 0$$
$$(x + 10)(x - 1) = 0$$
$$x = -10 \text{ or } x = 1$$

Check: $x = -10$ invalid (negative argument)

**Solution**: $x = 1$
</details>

---

### Advanced (Complex Applications)

**Problem 11**
Solve: $\ln(x - 2) + \ln(x + 2) = \ln(x + 10)$

<details>
<summary>Show Solution</summary>

**Solution**:
$$\ln((x-2)(x+2)) = \ln(x + 10)$$
$$(x-2)(x+2) = x + 10$$
$$x^2 - 4 = x + 10$$
$$x^2 - x - 14 = 0$$
$$x = \frac{1 \pm \sqrt{1 + 56}}{2} = \frac{1 \pm \sqrt{57}}{2}$$

$x = \frac{1 + \sqrt{57}}{2} \approx 4.27$ or $x = \frac{1 - \sqrt{57}}{2} \approx -3.27$

Check domains: need $x - 2 > 0$, so $x > 2$

Only $x = \frac{1 + \sqrt{57}}{2}$ is valid.
</details>

---

**Problem 12**
If $\log_2(x) = a$ and $\log_2(y) = b$, express $\log_2\left(\dfrac{8x^2}{y^3}\right)$ in terms of $a$ and $b$.

<details>
<summary>Show Solution</summary>

**Solution**:
$$\log_2\left(\frac{8x^2}{y^3}\right) = \log_2(8) + \log_2(x^2) - \log_2(y^3)$$
$$= 3 + 2\log_2(x) - 3\log_2(y)$$
$$= 3 + 2a - 3b$$
</details>

---

**Problem 13**
Solve: $e^{2x} - 5e^x + 6 = 0$

<details>
<summary>Show Solution</summary>

**Solution**:
Let $u = e^x$:
$$u^2 - 5u + 6 = 0$$
$$(u - 2)(u - 3) = 0$$
$$u = 2 \text{ or } u = 3$$

$$e^x = 2 \implies x = \ln 2$$
$$e^x = 3 \implies x = \ln 3$$

**Solutions**: $x = \ln 2$ and $x = \ln 3$
</details>

---

**Problem 14**
Find the inverse of $f(x) = 3 + 2\ln(x - 1)$.

<details>
<summary>Show Solution</summary>

**Solution**:
Let $y = 3 + 2\ln(x - 1)$

Swap and solve:
$$x = 3 + 2\ln(y - 1)$$
$$x - 3 = 2\ln(y - 1)$$
$$\frac{x - 3}{2} = \ln(y - 1)$$
$$e^{(x-3)/2} = y - 1$$
$$y = e^{(x-3)/2} + 1$$

**Inverse**: $f^{-1}(x) = e^{(x-3)/2} + 1$
</details>

---

**Problem 15**
Show that $\log_a(b) \cdot \log_b(a) = 1$.

<details>
<summary>Show Solution</summary>

**Solution**:
Using change of base:
$$\log_a(b) = \frac{\ln b}{\ln a}$$
$$\log_b(a) = \frac{\ln a}{\ln b}$$

Product:
$$\log_a(b) \cdot \log_b(a) = \frac{\ln b}{\ln a} \cdot \frac{\ln a}{\ln b} = 1$$
</details>

---

### AP Exam Style

**Problem 16**
If $\ln(x) = 3$ and $\ln(y) = 4$, find $\ln(xy^2)$.

<details>
<summary>Show Solution</summary>

**Solution**:
$$\ln(xy^2) = \ln(x) + \ln(y^2) = \ln(x) + 2\ln(y)$$
$$= 3 + 2(4) = 11$$
</details>

---

**Problem 17**
The derivative of $\ln(x^2 + 1)$ is:

(A) $\dfrac{1}{x^2 + 1}$

(B) $\dfrac{2x}{x^2 + 1}$

(C) $\dfrac{2}{x^2 + 1}$

(D) $\dfrac{x}{x^2 + 1}$

<details>
<summary>Show Solution</summary>

**Solution**:
Using chain rule:
$$\frac{d}{dx}[\ln(x^2 + 1)] = \frac{1}{x^2 + 1} \cdot 2x = \frac{2x}{x^2 + 1}$$

**Answer: (B)**
</details>

---

**Problem 18**
Solve $\log_2(x - 1) + \log_2(x + 1) = 3$.

<details>
<summary>Show Solution</summary>

**Solution**:
$$\log_2((x-1)(x+1)) = 3$$
$$\log_2(x^2 - 1) = 3$$
$$x^2 - 1 = 2^3 = 8$$
$$x^2 = 9$$
$$x = \pm 3$$

Check: $x = -3$ gives $\log_2(-4)$, undefined.

**Solution**: $x = 3$
</details>

---

**Problem 19** *(Free Response Style)*
A population grows according to $P(t) = 1000e^{0.05t}$.

(a) Find the initial population.
(b) After how many years will the population reach 3000?
(c) Find $\frac{dP}{dt}$ when $t = 10$.
(d) What is the relative growth rate (as a percentage)?

<details>
<summary>Show Solution</summary>

**Solution**:

**(a)** $P(0) = 1000e^0 = 1000$

**(b)** Solve $3000 = 1000e^{0.05t}$:
$$3 = e^{0.05t}$$
$$\ln 3 = 0.05t$$
$$t = \frac{\ln 3}{0.05} = 20\ln 3 \approx 21.97 \text{ years}$$

**(c)** $\frac{dP}{dt} = 1000 \cdot 0.05 \cdot e^{0.05t} = 50e^{0.05t}$

At $t = 10$: $\frac{dP}{dt} = 50e^{0.5} \approx 50(1.649) \approx 82.4$ per year

**(d)** Relative growth rate = $\frac{P'(t)}{P(t)} = \frac{50e^{0.05t}}{1000e^{0.05t}} = 0.05 = 5\%$
</details>

---

**Problem 20** *(Free Response Style)*
Consider $f(x) = \ln(x^2 - 4)$.

(a) Find the domain of $f$.
(b) Find all vertical asymptotes.
(c) Find $f'(x)$.
(d) Determine where $f$ is increasing and decreasing.

<details>
<summary>Show Solution</summary>

**Solution**:

**(a)** Require $x^2 - 4 > 0$:
$$(x-2)(x+2) > 0$$

Positive when $x < -2$ or $x > 2$

**Domain**: $(-\infty, -2) \cup (2, \infty)$

**(b)** Vertical asymptotes where argument approaches 0:

At $x = -2$ and $x = 2$

**(c)**
$$f'(x) = \frac{1}{x^2 - 4} \cdot 2x = \frac{2x}{x^2 - 4}$$

**(d)** Analyze sign of $f'(x) = \frac{2x}{x^2 - 4}$:

On $(-\infty, -2)$: numerator $< 0$, denominator $> 0$, so $f' < 0$. **Decreasing**.

On $(2, \infty)$: numerator $> 0$, denominator $> 0$, so $f' > 0$. **Increasing**.
</details>

---

## What's Next

Congratulations! You've completed Unit 0: Pre-Calculus Foundations. With these essential skills mastered, you're fully prepared to begin your calculus journey. Head to [Unit 1: Limits and Continuity](/calculus/0203-limits-the-foundation) to start exploring the core concepts of calculus!

---

<div align="center">

[← Exponential Functions](/calculus/0111-exponential-functions) | [Limits Overview →](/calculus/0203-limits-the-foundation)

</div>
