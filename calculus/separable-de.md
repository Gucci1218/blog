# Separable Differential Equations
<p class="article-date">April 23, 2026</p>

*So far, we've visualized DEs with slope fields and approximated solutions with Euler's Method. But what if we could solve them exactly — get an actual formula? For a special class of differential equations called **separable equations**, we can. The trick is beautifully simple: get all the $y$ stuff on one side, all the $x$ stuff on the other, and integrate both sides. It's like sorting your Starbucks order — cold drinks on one tray, hot drinks on the other — then dealing with each group on its own terms.*

---

## What You'll Learn
- Identify whether a DE is separable
- Solve separable DEs using separation of variables
- Handle initial value problems (IVPs) with separable DEs
- Work with implicit vs. explicit solutions
- Recognize common separable equations and their solution families
- Avoid the most frequent mistakes on the AP exam

---

## Prerequisites
- [Slope Fields](/calculus/slope-fields)
- [Antiderivatives](/calculus/0601-antiderivatives)
- [Logarithmic Functions](/calculus/0112-logarithmic-functions)
- [Exponential Functions](/calculus/0111-exponential-functions)

---

## The Core Concept

### Intuition First

Imagine you're at Ding Tea near school, and you've ordered a drink with boba. Right now, everything's mixed together — tea, ice, boba, syrup. But what if you could magically separate the boba to one side of the cup and the tea to the other? Then you could analyze each part independently.

That's exactly what we do with separable DEs. When $\frac{dy}{dx}$ can be written as a product of a function of $x$ and a function of $y$, we split them apart and integrate each side separately.

### The Definition

A differential equation is **separable** if it can be written as:

$$\frac{dy}{dx} = g(x) \cdot h(y)$$

That is, the right side is a product of a function of $x$ alone and a function of $y$ alone.

### The Method

**Step 1:** Rewrite to separate variables:

$$\frac{1}{h(y)} \, dy = g(x) \, dx$$

**Step 2:** Integrate both sides:

$$\int \frac{1}{h(y)} \, dy = \int g(x) \, dx$$

**Step 3:** Solve for $y$ (if possible) and apply initial conditions.

### Why This Works

We're treating $\frac{dy}{dx}$ as a fraction and "multiplying both sides by $dx$." Technically, this is a shortcut — the rigorous justification uses the chain rule — but it works perfectly and is how you'll use it on the AP exam.

---

## Is It Separable?

Before solving, you need to recognize when a DE is separable.

| DE | Separable? | Why? |
|----|-----------|------|
| $\frac{dy}{dx} = xy$ | Yes | $g(x) = x$, $h(y) = y$ |
| $\frac{dy}{dx} = x + y$ | No | Can't factor as $g(x) \cdot h(y)$ |
| $\frac{dy}{dx} = \frac{x^2}{y}$ | Yes | $g(x) = x^2$, $h(y) = \frac{1}{y}$ |
| $\frac{dy}{dx} = e^{x+y}$ | Yes | $= e^x \cdot e^y$ |
| $\frac{dy}{dx} = x^2 + y^2$ | No | Sum of functions, not a product |
| $\frac{dy}{dx} = (1 + x)(1 + y)$ | Yes | Already factored |
| $\frac{dy}{dx} = \frac{6x^2}{2y + \cos y}$ | Yes | $g(x) = 6x^2$, $\frac{1}{h(y)} = 2y + \cos y$ |

**Tip:** Look for products, quotients, or sums in exponents (which become products via $e^{a+b} = e^a \cdot e^b$).

---

## Worked Examples

### Example 1: The Classic First Separable DE

**Solve:** $\frac{dy}{dx} = 2xy$, $y(0) = 3$

**Step 1 — Separate:**

$$\frac{dy}{y} = 2x \, dx$$

**Step 2 — Integrate:**

$$\int \frac{dy}{y} = \int 2x \, dx$$

$$\ln|y| = x^2 + C$$

**Step 3 — Solve for $y$:**

$$|y| = e^{x^2 + C} = e^C \cdot e^{x^2}$$

$$y = Ae^{x^2} \quad \text{where } A = \pm e^C$$

**Step 4 — Apply initial condition** $y(0) = 3$:

$$3 = Ae^0 = A$$

$$\boxed{y = 3e^{x^2}}$$

---

### Example 2: Separating a Quotient

**Solve:** $\frac{dy}{dx} = \frac{x^2}{y}$, $y(0) = 4$

**Separate:**

$$y \, dy = x^2 \, dx$$

**Integrate:**

$$\int y \, dy = \int x^2 \, dx$$

$$\frac{y^2}{2} = \frac{x^3}{3} + C$$

**Apply IC** $y(0) = 4$:

$$\frac{16}{2} = 0 + C \Rightarrow C = 8$$

$$\frac{y^2}{2} = \frac{x^3}{3} + 8$$

$$\boxed{y^2 = \frac{2x^3}{3} + 16}$$

We could solve for $y = \sqrt{\frac{2x^3}{3} + 16}$ (taking the positive root since $y(0) = 4 > 0$), but the implicit form is perfectly acceptable on the AP exam.

---

### Example 3: Exponential Trick

**Solve:** $\frac{dy}{dx} = e^{x+y}$

**Rewrite:** $e^{x+y} = e^x \cdot e^y$ — now it's clearly separable!

**Separate:**

$$e^{-y} \, dy = e^x \, dx$$

**Integrate:**

$$\int e^{-y} \, dy = \int e^x \, dx$$

$$-e^{-y} = e^x + C$$

$$e^{-y} = -e^x - C$$

$$-y = \ln(-e^x - C)$$

$$\boxed{y = -\ln(-e^x + K)} \quad \text{where } K = -C$$

(The domain requires $-e^x + K > 0$, i.e., $x < \ln K$.)

---

### Example 4: Trigonometric Separable DE

**Solve:** $\frac{dy}{dx} = \frac{\cos x}{\sin y}$, $y\left(\frac{\pi}{2}\right) = \frac{\pi}{2}$

**Separate:**

$$\sin y \, dy = \cos x \, dx$$

**Integrate:**

$$\int \sin y \, dy = \int \cos x \, dx$$

$$-\cos y = \sin x + C$$

**Apply IC:** $y\left(\frac{\pi}{2}\right) = \frac{\pi}{2}$:

$$-\cos\left(\frac{\pi}{2}\right) = \sin\left(\frac{\pi}{2}\right) + C$$

$$0 = 1 + C \Rightarrow C = -1$$

$$\boxed{-\cos y = \sin x - 1} \quad \text{or} \quad \cos y = 1 - \sin x$$

---

### Example 5: A Common AP Pattern

**Solve:** $\frac{dy}{dx} = ky$, $y(0) = y_0$

This is the most important separable DE in all of calculus.

**Separate:**

$$\frac{dy}{y} = k \, dx$$

**Integrate:**

$$\ln|y| = kx + C$$

$$y = Ae^{kx}$$

**Apply IC:**

$$y_0 = Ae^0 = A$$

$$\boxed{y = y_0 e^{kx}}$$

This is the **exponential growth/decay model** — the foundation of the next article. It describes everything from population growth to the cooling of your Starbucks frappe on a warm San Diego afternoon.

---

### Example 6: Factoring to Make It Separable

**Solve:** $\frac{dy}{dx} = x^2 y - 3x^2$, $y(0) = 5$

At first glance, this doesn't look separable. But factor out $x^2$:

$$\frac{dy}{dx} = x^2(y - 3)$$

Now it's separable with $g(x) = x^2$ and $h(y) = y - 3$.

**Separate:**

$$\frac{dy}{y - 3} = x^2 \, dx$$

**Integrate:**

$$\ln|y - 3| = \frac{x^3}{3} + C$$

$$y - 3 = Ae^{x^3/3}$$

**Apply IC** $y(0) = 5$:

$$5 - 3 = Ae^0 \Rightarrow A = 2$$

$$\boxed{y = 3 + 2e^{x^3/3}}$$

**Notice:** $y = 3$ is an equilibrium solution (set $\frac{dy}{dx} = 0$). Our solution approaches $3$ as $x \to -\infty$ and grows without bound as $x \to +\infty$.

---

### Example 7: An Implicit Solution

**Solve:** $\frac{dy}{dx} = \frac{2x + 1}{3y^2 + 4}$, $y(0) = 1$

**Separate:**

$$(3y^2 + 4) \, dy = (2x + 1) \, dx$$

**Integrate:**

$$y^3 + 4y = x^2 + x + C$$

**Apply IC** $y(0) = 1$:

$$1 + 4 = 0 + 0 + C \Rightarrow C = 5$$

$$\boxed{y^3 + 4y = x^2 + x + 5}$$

This can't be solved explicitly for $y$ — and that's fine. Implicit solutions are perfectly valid on the AP exam. Think of it like a Mock Trial verdict — sometimes you can state a clear conclusion (explicit), and sometimes you present the evidence and let the relationship speak for itself (implicit).

---

### Example 8: Watch Out for Division by Zero

**Solve:** $\frac{dy}{dx} = y^2$, $y(0) = 1$

**Separate:**

$$\frac{dy}{y^2} = dx \quad \text{(requires } y \neq 0 \text{)}$$

**Integrate:**

$$\int y^{-2} \, dy = \int dx$$

$$-\frac{1}{y} = x + C$$

$$y = \frac{-1}{x + C}$$

**Apply IC** $y(0) = 1$:

$$1 = \frac{-1}{0 + C} \Rightarrow C = -1$$

$$\boxed{y = \frac{1}{1 - x}}$$

**Critical observation:** This solution has a vertical asymptote at $x = 1$. The solution blows up! Even though we started with a perfectly innocent initial condition $y(0) = 1$, the solution only exists for $x < 1$.

Also: when we divided by $y^2$, we assumed $y \neq 0$. Notice that $y = 0$ is also a solution (the equilibrium solution). We "lost" this solution when dividing.

---

## The Lost Solution Problem

### Why You Need to Be Careful

When you separate variables and divide by $h(y)$, you're assuming $h(y) \neq 0$. But $h(y) = 0$ might give you an **equilibrium solution** that you've "lost."

**Rule:** After solving a separable DE, always check if $h(y) = 0$ gives additional constant solutions.

### Example 9: Lost Equilibrium

**Solve:** $\frac{dy}{dx} = y(1 - y)$

**Separate** (assuming $y \neq 0$ and $y \neq 1$):

$$\frac{dy}{y(1-y)} = dx$$

**Partial fractions:**

$$\frac{1}{y(1-y)} = \frac{1}{y} + \frac{1}{1-y}$$

**Integrate:**

$$\ln|y| - \ln|1-y| = x + C$$

$$\ln\left|\frac{y}{1-y}\right| = x + C$$

$$\frac{y}{1-y} = Ae^x$$

$$y = \frac{Ae^x}{1 + Ae^x}$$

**Don't forget the lost solutions:** $y = 0$ and $y = 1$ are also solutions (equilibria).

This DE models **logistic growth** — we'll see it extensively in the next article.

---

## Key Formulas & Rules

| Step | Action |
|------|--------|
| 1. Identify | Check if $\frac{dy}{dx} = g(x) \cdot h(y)$ |
| 2. Separate | Move $y$ terms left, $x$ terms right: $\frac{dy}{h(y)} = g(x) \, dx$ |
| 3. Integrate | $\int \frac{dy}{h(y)} = \int g(x) \, dx + C$ |
| 4. Solve | Solve for $y$ if possible (implicit is OK) |
| 5. Apply IC | Plug in initial condition to find $C$ |
| 6. Check | Did you lose any equilibrium solutions? |

### Important Separable DEs to Recognize

| DE | Solution |
|----|----------|
| $\frac{dy}{dx} = ky$ | $y = Ce^{kx}$ |
| $\frac{dy}{dx} = k(y - A)$ | $y = A + Ce^{kx}$ |
| $\frac{dy}{dx} = ky(M - y)$ | Logistic: $y = \frac{M}{1 + Be^{-kMx}}$ |
| $\frac{dy}{dx} = -\frac{x}{y}$ | $x^2 + y^2 = C$ (circles) |
| $\frac{dy}{dx} = \frac{y}{x}$ | $y = Cx$ (lines through origin) |

---

## Common Mistakes to Avoid

### Mistake 1: Forgetting the Constant of Integration

You need *one* constant $C$, placed on one side only. Don't write $C$ on both sides.

- **Wrong:** $\ln|y| + C_1 = x^2 + C_2$
- **Right:** $\ln|y| = x^2 + C$ (where $C = C_2 - C_1$)

---

### Mistake 2: Dropping Absolute Values Too Early

When integrating $\int \frac{dy}{y} = \ln|y|$, the absolute value matters.

To go from $\ln|y| = f(x) + C$ to $y = \pm e^{f(x) + C}$, we absorb the $\pm$ into the constant: $y = Ae^{f(x)}$ where $A$ can be positive or negative.

Use the initial condition to determine the sign of $A$.

---

### Mistake 3: Trying to Separate the Inseparable

$\frac{dy}{dx} = x + y$ is **not** separable. You cannot factor $x + y$ as $g(x) \cdot h(y)$. Don't force it. If the DE isn't separable, you need a different method (linear DEs, which are beyond the AP exam scope).

---

### Mistake 4: Losing Equilibrium Solutions

When you divide by $h(y)$, check: does $h(y) = 0$ give a constant solution?

Think of it like a Mock Trial case — you need to account for *all* possibilities, not just the obvious ones. Missing the equilibrium solution is like ignoring a key piece of evidence.

---

### Mistake 5: Plugging In the IC at the Wrong Step

**Best practice:** Apply the initial condition *right after integrating*, before solving for $y$. This often avoids messy algebra.

For example, if you get $\ln|y - 2| = x^2 + C$ with $y(0) = 5$:
- Plug in: $\ln|3| = 0 + C$, so $C = \ln 3$
- Then: $\ln|y - 2| = x^2 + \ln 3$

This is cleaner than solving for $y$ first and then plugging in.

---

### Mistake 6: Sign Errors with Negative Exponents

When integrating $\int y^{-2} \, dy$, remember:

$$\int y^{-2} \, dy = \frac{y^{-1}}{-1} + C = -\frac{1}{y} + C$$

Don't forget the negative sign!

---

## AP Exam Tips

### For Both AB and BC:
- Separable DEs appear on **every** AP exam — it's the most tested DE topic
- Free response often combines slope fields + separation of variables
- You must show the separation step clearly for full credit

### The AP Scoring Checklist

When grading free response, AP readers look for:

1. **Separation** — Did you correctly separate $y$ and $x$ to opposite sides?
2. **Antidifferentiation** — Did you integrate both sides correctly?
3. **Constant of integration** — Did you include $+C$?
4. **Initial condition** — Did you use it to find $C$?
5. **Solution** — Is your final answer correct?

Missing any of these typically costs 1 point each.

### Common Free Response Format

> "Given $\frac{dy}{dx} = f(x, y)$ with $y(a) = b$, find the particular solution."

Your response should clearly show all 5 steps above.

### Time-Saving Tips

1. **Apply IC early** — plug in right after integrating (before solving for $y$)
2. **Don't simplify unnecessarily** — $y = 3 + 2e^{x^2}$ is a fine answer; no need to expand
3. **Check by differentiating** — if time permits, verify your solution satisfies the original DE

---

## Practice Problems

### Basic (Problems 1-5)

**1.** Solve: $\frac{dy}{dx} = 3y$, $y(0) = 5$

---

**2.** Solve: $\frac{dy}{dx} = \frac{x}{y}$, $y(0) = 2$

---

**3.** Solve: $\frac{dy}{dx} = e^x e^{-y}$, $y(0) = 0$

---

**4.** Solve: $\frac{dy}{dx} = \frac{6x^2}{2y}$, $y(0) = 3$

---

**5.** Determine which of these are separable:

(a) $\frac{dy}{dx} = x^2 y + x^2$

(b) $\frac{dy}{dx} = x + y^2$

(c) $\frac{dy}{dx} = \frac{\sin x}{e^y}$

(d) $\frac{dy}{dx} = xy + x + y + 1$

---

### Intermediate (Problems 6-10)

**6.** Solve: $\frac{dy}{dx} = (1 + y^2)\tan x$, $y(0) = 1$

---

**7.** Solve: $\frac{dy}{dx} = \frac{2x}{y + 1}$, $y(0) = 3$

---

**8.** Solve: $\frac{dy}{dx} = xy^2 - 4x$, $y(0) = 3$ *(Hint: factor the right side)*

---

**9.** Solve: $\frac{dy}{dx} = e^{2x - y}$, $y(0) = 1$

---

**10.** Find the general solution of $\frac{dy}{dx} = \frac{1 + y}{1 + x}$ and describe the solution curves geometrically.

---

### Advanced (Problems 11-15)

**11.** Solve: $\frac{dy}{dx} = \frac{y \ln y}{x}$, $y(1) = e$

---

**12.** Solve: $\cos y \, \frac{dy}{dx} = \frac{\cos x}{\sin y}$, $y\left(\frac{\pi}{6}\right) = \frac{\pi}{6}$

*(Hint: Multiply both sides by $\sin y$)*

---

**13.** Solve: $\frac{dy}{dx} = y^2 - 1$, $y(0) = 0$. Identify all equilibrium solutions and determine the long-term behavior.

---

**14.** A separable DE has the general solution $y^2 + x^2 = C$.
(a) What are the solution curves?
(b) What is the DE?
(c) Are there any equilibrium solutions?

---

**15.** Solve the initial value problem:

$$x \, dy - y \, dx = x^2 \, dy$$

with $y(1) = 2$.

*(Hint: Rewrite in the form $\frac{dy}{dx} = \ldots$ first.)*

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

The solution to $\frac{dy}{dx} = 2y$ with $y(0) = 3$ is:

| Choice | Answer |
|--------|--------|
| **(A)** | $y = 3e^{2x}$ |
| **(B)** | $y = e^{2x} + 3$ |
| **(C)** | $y = 2e^{3x}$ |
| **(D)** | $y = 3e^{x^2}$ |

---

#### Problem 17 (Multiple Choice)

Which of the following DEs is NOT separable?

| Choice | DE |
|--------|----|
| **(A)** | $\frac{dy}{dx} = x^2 y^3$ |
| **(B)** | $\frac{dy}{dx} = e^{x+y}$ |
| **(C)** | $\frac{dy}{dx} = x \cos y$ |
| **(D)** | $\frac{dy}{dx} = x^2 + y^2$ |

---

#### Problem 18 (Free Response)

Consider the differential equation $\frac{dy}{dx} = \frac{2x}{y}$ with initial condition $y(1) = 2$.

> **(a)** Sketch the slope field at the nine points where $x = -1, 0, 1$ and $y = -1, 1, 2$. *(Note: slope is undefined at $y = 0$.)*
>
> **(b)** Find the particular solution to the IVP. Express $y$ as a function of $x$.
>
> **(c)** Describe the solution curve geometrically.
>
> **(d)** For what values of $x$ is the solution valid?

---

#### Problem 19 (Multiple Choice)

If $\frac{dy}{dx} = xy$ and $y(0) = -2$, then $y(1) =$

| Choice | Answer |
|--------|--------|
| **(A)** | $-2e$ |
| **(B)** | $-2\sqrt{e}$ |
| **(C)** | $2\sqrt{e}$ |
| **(D)** | $-2e^{1/2}$ |

---

#### Problem 20 (Free Response — Challenging)

The amount of boba $B$ (in ounces) remaining in your Ding Tea cup $t$ minutes after you start drinking satisfies:

$$\frac{dB}{dt} = -0.3\sqrt{B}$$

You start with $B(0) = 9$ ounces of boba.

> **(a)** Solve this IVP for $B(t)$.
>
> **(b)** According to your model, at what time will all the boba be gone?
>
> **(c)** Is $\frac{d^2B}{dt^2}$ positive or negative? What does this mean about the rate at which you consume boba?
>
> **(d)** Your friend starts with $16$ ounces of boba and drinks at the same rate. Set up and solve their IVP. How much longer does their boba last compared to yours?

---

## Answer Key

<details>
<summary><strong>Problem 1 Solution</strong></summary>

**Solve:** $\frac{dy}{dx} = 3y$, $y(0) = 5$

$$\frac{dy}{y} = 3 \, dx$$

$$\ln|y| = 3x + C$$

$$y = Ae^{3x}$$

$y(0) = 5$: $A = 5$

$$\boxed{y = 5e^{3x}}$$

</details>

---

<details>
<summary><strong>Problem 2 Solution</strong></summary>

**Solve:** $\frac{dy}{dx} = \frac{x}{y}$, $y(0) = 2$

$$y \, dy = x \, dx$$

$$\frac{y^2}{2} = \frac{x^2}{2} + C$$

$y(0) = 2$: $\frac{4}{2} = 0 + C$, so $C = 2$

$$\frac{y^2}{2} = \frac{x^2}{2} + 2$$

$$y^2 = x^2 + 4$$

$$\boxed{y = \sqrt{x^2 + 4}} \quad \text{(positive root since } y(0) = 2 > 0\text{)}$$

The solution curves are hyperbolas.

</details>

---

<details>
<summary><strong>Problem 3 Solution</strong></summary>

**Solve:** $\frac{dy}{dx} = e^x e^{-y}$, $y(0) = 0$

$$e^y \, dy = e^x \, dx$$

$$e^y = e^x + C$$

$y(0) = 0$: $e^0 = e^0 + C$ → $1 = 1 + C$ → $C = 0$

$$e^y = e^x$$

$$\boxed{y = x}$$

Satisfying! The solution is just the line $y = x$.

Verify: $\frac{dy}{dx} = 1$ and $e^x \cdot e^{-y} = e^x \cdot e^{-x} = e^0 = 1$. ✓

</details>

---

<details>
<summary><strong>Problem 4 Solution</strong></summary>

**Solve:** $\frac{dy}{dx} = \frac{6x^2}{2y}$, $y(0) = 3$

$$2y \, dy = 6x^2 \, dx$$

$$y^2 = 2x^3 + C$$

$y(0) = 3$: $9 = 0 + C$, so $C = 9$

$$y^2 = 2x^3 + 9$$

$$\boxed{y = \sqrt{2x^3 + 9}} \quad \text{(positive root)}$$

</details>

---

<details>
<summary><strong>Problem 5 Solution</strong></summary>

**(a)** $\frac{dy}{dx} = x^2 y + x^2 = x^2(y + 1)$ → **Yes**, separable. $g(x) = x^2$, $h(y) = y + 1$.

**(b)** $\frac{dy}{dx} = x + y^2$ → **No**. Cannot factor as $g(x) \cdot h(y)$.

**(c)** $\frac{dy}{dx} = \frac{\sin x}{e^y} = e^{-y} \sin x$ → **Yes**, separable. $g(x) = \sin x$, $h(y) = e^{-y}$.

**(d)** $\frac{dy}{dx} = xy + x + y + 1 = x(y + 1) + (y + 1) = (x + 1)(y + 1)$ → **Yes**, separable! (Factor by grouping.)

</details>

---

<details>
<summary><strong>Problem 6 Solution</strong></summary>

**Solve:** $\frac{dy}{dx} = (1 + y^2)\tan x$, $y(0) = 1$

$$\frac{dy}{1 + y^2} = \tan x \, dx$$

$$\arctan y = -\ln|\cos x| + C = \ln|\sec x| + C$$

$y(0) = 1$: $\arctan(1) = \ln(1) + C$ → $\frac{\pi}{4} = 0 + C$ → $C = \frac{\pi}{4}$

$$\arctan y = \ln|\sec x| + \frac{\pi}{4}$$

$$\boxed{y = \tan\left(\ln|\sec x| + \frac{\pi}{4}\right)}$$

</details>

---

<details>
<summary><strong>Problem 7 Solution</strong></summary>

**Solve:** $\frac{dy}{dx} = \frac{2x}{y + 1}$, $y(0) = 3$

$$(y + 1) \, dy = 2x \, dx$$

$$\frac{y^2}{2} + y = x^2 + C$$

$y(0) = 3$: $\frac{9}{2} + 3 = 0 + C$ → $C = \frac{15}{2}$

$$\boxed{\frac{y^2}{2} + y = x^2 + \frac{15}{2}}$$

Or: $y^2 + 2y = 2x^2 + 15$

</details>

---

<details>
<summary><strong>Problem 8 Solution</strong></summary>

**Solve:** $\frac{dy}{dx} = xy^2 - 4x = x(y^2 - 4) = x(y - 2)(y + 2)$, $y(0) = 3$

**Separate** (since $y(0) = 3$, we're in the region $y > 2$):

$$\frac{dy}{(y-2)(y+2)} = x \, dx$$

**Partial fractions:**

$$\frac{1}{(y-2)(y+2)} = \frac{1}{4}\left(\frac{1}{y-2} - \frac{1}{y+2}\right)$$

$$\frac{1}{4}\left(\ln|y-2| - \ln|y+2|\right) = \frac{x^2}{2} + C$$

$$\ln\left|\frac{y-2}{y+2}\right| = 2x^2 + C_1$$

$y(0) = 3$: $\ln\left|\frac{1}{5}\right| = C_1$ → $C_1 = -\ln 5$

$$\ln\left|\frac{y-2}{y+2}\right| = 2x^2 - \ln 5$$

$$\frac{y-2}{y+2} = \frac{1}{5}e^{2x^2}$$

**Equilibrium solutions:** $y = 2$ and $y = -2$ (lost when dividing).

</details>

---

<details>
<summary><strong>Problem 9 Solution</strong></summary>

**Solve:** $\frac{dy}{dx} = e^{2x - y} = e^{2x} \cdot e^{-y}$, $y(0) = 1$

$$e^y \, dy = e^{2x} \, dx$$

$$e^y = \frac{e^{2x}}{2} + C$$

$y(0) = 1$: $e^1 = \frac{1}{2} + C$ → $C = e - \frac{1}{2}$

$$e^y = \frac{e^{2x}}{2} + e - \frac{1}{2}$$

$$\boxed{y = \ln\left(\frac{e^{2x}}{2} + e - \frac{1}{2}\right)}$$

</details>

---

<details>
<summary><strong>Problem 10 Solution</strong></summary>

**Solve:** $\frac{dy}{dx} = \frac{1 + y}{1 + x}$

$$\frac{dy}{1 + y} = \frac{dx}{1 + x}$$

$$\ln|1 + y| = \ln|1 + x| + C$$

$$|1 + y| = A|1 + x|$$

$$1 + y = K(1 + x) \quad \text{where } K = \pm A$$

$$\boxed{y = K(1 + x) - 1}$$

These are **lines through the point $(-1, -1)$**, each with a different slope $K$. The solution curves are a family of lines radiating from a single point — like rays of sunlight fanning out at sunset over the Pacific!

**Lost solution:** $y = -1$ (when $K = 0$) is also part of the family.

</details>

---

<details>
<summary><strong>Problem 11 Solution</strong></summary>

**Solve:** $\frac{dy}{dx} = \frac{y \ln y}{x}$, $y(1) = e$

$$\frac{dy}{y \ln y} = \frac{dx}{x}$$

Let $u = \ln y$, $du = \frac{dy}{y}$:

$$\int \frac{du}{u} = \int \frac{dx}{x}$$

$$\ln|\ln y| = \ln|x| + C$$

$$|\ln y| = A|x|$$

$$\ln y = Kx$$

$y(1) = e$: $\ln e = K(1)$ → $K = 1$

$$\ln y = x$$

$$\boxed{y = e^x}$$

</details>

---

<details>
<summary><strong>Problem 12 Solution</strong></summary>

**Solve:** $\cos y \cdot \frac{dy}{dx} = \frac{\cos x}{\sin y}$

Multiply both sides by $\sin y$:

$$\sin y \cos y \, \frac{dy}{dx} = \cos x$$

$$\sin y \cos y \, dy = \cos x \, dx$$

Note: $\sin y \cos y = \frac{1}{2}\sin(2y)$

$$\frac{1}{2}\sin(2y) \, dy = \cos x \, dx$$

$$-\frac{1}{4}\cos(2y) = \sin x + C$$

$y\left(\frac{\pi}{6}\right) = \frac{\pi}{6}$:

$$-\frac{1}{4}\cos\left(\frac{\pi}{3}\right) = \sin\left(\frac{\pi}{6}\right) + C$$

$$-\frac{1}{4} \cdot \frac{1}{2} = \frac{1}{2} + C$$

$$-\frac{1}{8} = \frac{1}{2} + C \Rightarrow C = -\frac{5}{8}$$

$$\boxed{-\frac{1}{4}\cos(2y) = \sin x - \frac{5}{8}}$$

</details>

---

<details>
<summary><strong>Problem 13 Solution</strong></summary>

**Solve:** $\frac{dy}{dx} = y^2 - 1 = (y - 1)(y + 1)$, $y(0) = 0$

**Equilibria:** $y = 1$ and $y = -1$

Since $y(0) = 0$ is between the equilibria, and the slope at $(0, 0)$ is $0 - 1 = -1 < 0$, the solution decreases.

**Separate:**

$$\frac{dy}{(y-1)(y+1)} = dx$$

**Partial fractions:** $\frac{1}{(y-1)(y+1)} = \frac{1}{2}\left(\frac{1}{y-1} - \frac{1}{y+1}\right)$

$$\frac{1}{2}\ln\left|\frac{y-1}{y+1}\right| = x + C$$

$y(0) = 0$: $\frac{1}{2}\ln\left|\frac{-1}{1}\right| = C$ → $\frac{1}{2}\ln 1 = C$ → $C = 0$

$$\ln\left|\frac{y-1}{y+1}\right| = 2x$$

$$\frac{y-1}{y+1} = \pm e^{2x}$$

Since $y(0) = 0$: $\frac{-1}{1} = -1$, so we use the negative sign:

$$\frac{y-1}{y+1} = -e^{2x}$$

Solving: $y - 1 = -e^{2x}(y + 1) = -ye^{2x} - e^{2x}$

$y + ye^{2x} = 1 - e^{2x}$

$$\boxed{y = \frac{1 - e^{2x}}{1 + e^{2x}}}$$

**Long-term behavior:** As $x \to \infty$: $y \to \frac{-e^{2x}}{e^{2x}} = -1$

The solution approaches the stable equilibrium $y = -1$.

</details>

---

<details>
<summary><strong>Problem 14 Solution</strong></summary>

**Given:** $y^2 + x^2 = C$

**(a)** The solution curves are **circles** centered at the origin with radius $\sqrt{C}$.

**(b)** Differentiate implicitly: $2y \frac{dy}{dx} + 2x = 0$

$$\boxed{\frac{dy}{dx} = -\frac{x}{y}}$$

**(c)** There are no equilibrium solutions (constant $y$), because $\frac{dy}{dx} = 0$ only when $x = 0$, and the solutions are circles, not horizontal lines.

However, the single point $y = 0$, $x = 0$ (the origin) is a degenerate solution ($C = 0$).

</details>

---

<details>
<summary><strong>Problem 15 Solution</strong></summary>

**Rewrite:** $x \, dy - y \, dx = x^2 \, dy$

$(x - x^2) \, dy = y \, dx$

$x(1 - x) \, dy = y \, dx$

$$\frac{dy}{y} = \frac{dx}{x(1-x)}$$

**Partial fractions:** $\frac{1}{x(1-x)} = \frac{1}{x} + \frac{1}{1-x}$

$$\ln|y| = \ln|x| - \ln|1 - x| + C = \ln\left|\frac{x}{1-x}\right| + C$$

$$y = A \cdot \frac{x}{1-x}$$

$y(1) = 2$: This gives $\frac{1}{1-1} = \frac{1}{0}$ — undefined!

The initial condition $y(1) = 2$ is problematic because $x = 1$ is a singularity of the DE. This IVP has no solution in the standard sense.

</details>

---

<details>
<summary><strong>Problem 16 Solution</strong></summary>

**Answer: (A)** $y = 3e^{2x}$

$\frac{dy}{y} = 2 \, dx$ → $\ln|y| = 2x + C$ → $y = Ae^{2x}$

$y(0) = 3$: $A = 3$

**Answer: (A)**

Why not (D)? $\frac{d}{dx}[3e^{x^2}] = 6xe^{x^2}$, not $2 \cdot 3e^{x^2}$.

</details>

---

<details>
<summary><strong>Problem 17 Solution</strong></summary>

**Answer: (D)** $\frac{dy}{dx} = x^2 + y^2$

- **(A)** $x^2 y^3$ → product ✓
- **(B)** $e^{x+y} = e^x \cdot e^y$ → product ✓
- **(C)** $x \cos y$ → product ✓
- **(D)** $x^2 + y^2$ → sum, cannot be factored ✗

**Answer: (D)**

</details>

---

<details>
<summary><strong>Problem 18 Solution</strong></summary>

**For** $\frac{dy}{dx} = \frac{2x}{y}$, $y(1) = 2$:

**(a)** Slope table (slopes undefined at $y = 0$):

| $(x, y)$ | $\frac{2x}{y}$ |
|-----------|----------------|
| $(-1, -1)$ | $2$ |
| $(-1, 1)$ | $-2$ |
| $(-1, 2)$ | $-1$ |
| $(0, -1)$ | $0$ |
| $(0, 1)$ | $0$ |
| $(0, 2)$ | $0$ |
| $(1, -1)$ | $-2$ |
| $(1, 1)$ | $2$ |
| $(1, 2)$ | $1$ |

**(b)** Separate: $y \, dy = 2x \, dx$

$\frac{y^2}{2} = x^2 + C$

$y(1) = 2$: $\frac{4}{2} = 1 + C$ → $C = 1$

$y^2 = 2x^2 + 2$

$$\boxed{y = \sqrt{2x^2 + 2}} \quad \text{(positive root)}$$

**(c)** $y^2 - 2x^2 = 2$, or $\frac{y^2}{2} - x^2 = 1$ — this is a **hyperbola** with the $y$-axis as the transverse axis.

**(d)** Since $2x^2 + 2 > 0$ for all $x$, the solution is valid for **all real $x$**.

</details>

---

<details>
<summary><strong>Problem 19 Solution</strong></summary>

**Answer: (B) and (D)** — they're the same! $-2\sqrt{e} = -2e^{1/2}$

$\frac{dy}{y} = x \, dx$ → $\ln|y| = \frac{x^2}{2} + C$

$y(0) = -2$: $\ln 2 = C$

$\ln|y| = \frac{x^2}{2} + \ln 2$

$|y| = 2e^{x^2/2}$

Since $y(0) = -2 < 0$: $y = -2e^{x^2/2}$

$y(1) = -2e^{1/2} = -2\sqrt{e}$

**Answer: (B) or (D)** (both are correct notations for the same value)

</details>

---

<details>
<summary><strong>Problem 20 Solution</strong></summary>

**For** $\frac{dB}{dt} = -0.3\sqrt{B}$, $B(0) = 9$:

**(a)** Separate:

$$\frac{dB}{\sqrt{B}} = -0.3 \, dt$$

$$B^{-1/2} \, dB = -0.3 \, dt$$

$$2B^{1/2} = -0.3t + C$$

$$2\sqrt{B} = -0.3t + C$$

$B(0) = 9$: $2(3) = C$ → $C = 6$

$$2\sqrt{B} = 6 - 0.3t$$

$$\sqrt{B} = 3 - 0.15t$$

$$\boxed{B(t) = (3 - 0.15t)^2} \quad \text{for } 0 \leq t \leq 20$$

**(b)** All boba gone when $B = 0$:

$(3 - 0.15t)^2 = 0$ → $t = \frac{3}{0.15} = 20$ minutes

**The boba runs out at $t = 20$ minutes.** About the length of a study break at Ding Tea between classes.

**(c)** $B'(t) = -0.3\sqrt{B} = -0.3(3 - 0.15t)$

$B''(t) = -0.3(-0.15) = 0.045 > 0$

$B'' > 0$ means the rate of boba consumption is **slowing down** — you drink fastest at the beginning (big sips through the straw when the cup is full) and slower toward the end (chasing the last few pearls at the bottom).

**(d)** Friend's IVP: $\frac{dB}{dt} = -0.3\sqrt{B}$, $B(0) = 16$

Same separation:

$2\sqrt{B} = -0.3t + C$

$B(0) = 16$: $2(4) = C$ → $C = 8$

$\sqrt{B} = 4 - 0.15t$

$B(t) = (4 - 0.15t)^2$

Boba gone when $t = \frac{4}{0.15} = \frac{80}{3} \approx 26.67$ minutes.

**Difference:** $26.67 - 20 = 6.67$ minutes longer.

Even though your friend started with almost twice the boba ($16$ vs $9$ oz), they only lasted about $\frac{1}{3}$ longer — because the square root in the model means more boba = faster drinking rate. Starting with more doesn't make it last proportionally longer!

</details>

---

## What's Next

Now that you can solve separable DEs exactly, you're ready for the crown jewel application: [Exponential Growth and Decay](/calculus/exponential-growth-decay). We'll model everything from population explosions to the cooling of your Sesame Donuts coffee on a Saturday morning.

---

<div align="center">

[← Euler's Method](/calculus/eulers-method) | [Exponential Growth & Decay →](/calculus/exponential-growth-decay)

</div>
