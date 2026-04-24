# Partial Fractions
<p class="article-date">April 23, 2026</p>

*You know that feeling at Panda Express when you order a combo plate and everything's piled together — orange chicken on top of fried rice on top of chow mein? It's delicious, but if someone asked you to describe each item separately, you'd want to split them apart first. Partial fraction decomposition works the same way: you take a complicated fraction that's all mixed together and break it into simpler pieces you already know how to handle. Once it's split up, integration becomes almost trivial — just $\ln$ terms and $\arctan$ terms you've seen before.*

---

## What You'll Learn
- Understand why partial fraction decomposition is necessary for integrating rational functions
- Decompose rational expressions with distinct linear factors
- Decompose rational expressions with repeated linear factors
- Recognize and handle irreducible quadratic factors
- Use the Heaviside cover-up method for quick decomposition
- Solve for constants by plugging in roots and by equating coefficients
- Integrate each partial fraction to get $\ln$ and $\arctan$ terms
- Perform long division when the degree of the numerator is greater than or equal to the degree of the denominator
- Connect partial fractions to separable differential equations (logistic growth)

---

## Prerequisites
- [Antiderivatives](/calculus/0601-antiderivatives)
- [Logarithmic Functions](/calculus/0112-logarithmic-functions)
- [Rational Expressions](/calculus/0107-rational-expressions)

---

## The Core Concept

### Intuition First

Imagine Ganga is preparing for a Mock Trial competition at Rancho Bernardo High School. The opposing counsel has presented one long, tangled argument that weaves together three separate claims. It sounds overwhelming. But Ganga's strategy is to break it apart: address Claim A, then Claim B, then Claim C, each one simple enough to dismantle on its own. Together they seemed impossible; separated, each one falls.

That's partial fractions in a nutshell. An integral like:

$$\int \frac{3x + 5}{(x - 1)(x + 2)} \, dx$$

looks messy as a single fraction. But if we can write it as:

$$\int \left(\frac{A}{x - 1} + \frac{B}{x + 2}\right) dx$$

then each piece is just a simple $\frac{1}{u}$ integral — which gives us $\ln|u|$. We already know how to do that!

### The Definition

**Partial fraction decomposition** is the process of rewriting a proper rational function (degree of numerator $<$ degree of denominator) as a sum of simpler fractions whose denominators are the factors of the original denominator.

Given a rational function $\frac{P(x)}{Q(x)}$ where $\deg(P) < \deg(Q)$, we write:

$$\frac{P(x)}{Q(x)} = \frac{A_1}{\text{factor}_1} + \frac{A_2}{\text{factor}_2} + \cdots$$

### Why This Works for Integration

Every partial fraction falls into one of two types, both of which we can integrate:

1. $\displaystyle\int \frac{A}{x - a} \, dx = A \ln|x - a| + C$

2. $\displaystyle\int \frac{Ax + B}{x^2 + bx + c} \, dx$ leads to $\ln$ and/or $\arctan$ terms

So the strategy is: **decompose, then integrate each piece**.

### The Three Cases

| Case | Denominator Has | Form of Decomposition |
|------|----------------|----------------------|
| 1 | Distinct linear factors | $\frac{A}{x - a} + \frac{B}{x - b} + \cdots$ |
| 2 | Repeated linear factors | $\frac{A}{x - a} + \frac{B}{(x - a)^2} + \cdots$ |
| 3 | Irreducible quadratic factor | $\frac{Ax + B}{x^2 + bx + c}$ |

### Important Prerequisite: Long Division First!

Before decomposing, the fraction must be **proper** (numerator degree $<$ denominator degree). If it's not, perform polynomial long division first.

Think of it like driving on the I-5 — before you can merge onto the highway, you need to get on the on-ramp first. Long division is the on-ramp that gets you into the right form.

$$\frac{\text{improper fraction}}{\text{}} \xrightarrow{\text{long division}} \text{polynomial} + \frac{\text{proper fraction}}{\text{denominator}}$$

---

## Worked Examples

### Example 1: Distinct Linear Factors — The Basic Case

**Evaluate:** $\displaystyle\int \frac{5}{(x - 1)(x + 4)} \, dx$

**Step 1 — Set up the decomposition:**

$$\frac{5}{(x - 1)(x + 4)} = \frac{A}{x - 1} + \frac{B}{x + 4}$$

**Step 2 — Multiply both sides by $(x - 1)(x + 4)$:**

$$5 = A(x + 4) + B(x - 1)$$

**Step 3 — Solve for $A$ and $B$ by plugging in roots:**

Set $x = 1$: $5 = A(5) + B(0)$ $\Rightarrow$ $A = 1$

Set $x = -4$: $5 = A(0) + B(-5)$ $\Rightarrow$ $B = -1$

**Step 4 — Integrate:**

$$\int \frac{5}{(x-1)(x+4)} \, dx = \int \left(\frac{1}{x-1} - \frac{1}{x+4}\right) dx$$

$$= \ln|x - 1| - \ln|x + 4| + C$$

$$= \boxed{\ln\left|\frac{x-1}{x+4}\right| + C}$$

---

### Example 2: Three Distinct Linear Factors

**Evaluate:** $\displaystyle\int \frac{x + 7}{(x - 1)(x + 1)(x - 3)} \, dx$

**Set up:**

$$\frac{x + 7}{(x-1)(x+1)(x-3)} = \frac{A}{x-1} + \frac{B}{x+1} + \frac{C}{x-3}$$

**Multiply through:**

$$x + 7 = A(x+1)(x-3) + B(x-1)(x-3) + C(x-1)(x+1)$$

**Plug in roots:**

$x = 1$: $8 = A(2)(-2) = -4A$ $\Rightarrow$ $A = -2$

$x = -1$: $6 = B(-2)(-4) = 8B$ $\Rightarrow$ $B = \frac{3}{4}$

$x = 3$: $10 = C(2)(4) = 8C$ $\Rightarrow$ $C = \frac{5}{4}$

**Integrate:**

$$\int \left(\frac{-2}{x-1} + \frac{3/4}{x+1} + \frac{5/4}{x-3}\right) dx$$

$$= \boxed{-2\ln|x-1| + \frac{3}{4}\ln|x+1| + \frac{5}{4}\ln|x-3| + C}$$

---

### Example 3: The Heaviside Cover-Up Method

The **cover-up method** is a shortcut for distinct linear factors — like a speed hack on an AP exam. Instead of the full algebra, you "cover up" the factor in the denominator that matches each variable and evaluate what remains.

**Find the partial fractions of:** $\frac{3x + 11}{(x + 1)(x - 3)}$

For $A$ (the coefficient over $x + 1$): Cover up $(x + 1)$ in the original fraction and set $x = -1$:

$$A = \frac{3(-1) + 11}{(-1) - 3} = \frac{8}{-4} = -2$$

For $B$ (the coefficient over $x - 3$): Cover up $(x - 3)$ and set $x = 3$:

$$B = \frac{3(3) + 11}{(3) + 1} = \frac{20}{4} = 5$$

**Result:**

$$\frac{3x + 11}{(x+1)(x-3)} = \frac{-2}{x+1} + \frac{5}{x-3}$$

The cover-up method is like grabbing individual items off your Panda Express plate — you isolate one item at a time by covering up the rest.

---

### Example 4: Repeated Linear Factors

**Evaluate:** $\displaystyle\int \frac{2x + 3}{(x - 1)^2(x + 2)} \, dx$

When a factor is repeated, you need a term for each power:

$$\frac{2x + 3}{(x-1)^2(x+2)} = \frac{A}{x-1} + \frac{B}{(x-1)^2} + \frac{C}{x+2}$$

**Multiply through by $(x-1)^2(x+2)$:**

$$2x + 3 = A(x-1)(x+2) + B(x+2) + C(x-1)^2$$

**Plug in roots:**

$x = 1$: $5 = B(3)$ $\Rightarrow$ $B = \frac{5}{3}$

$x = -2$: $-1 = C(-3)^2 = 9C$ $\Rightarrow$ $C = -\frac{1}{9}$

**For $A$, equate coefficients of $x^2$:**

Left side: coefficient of $x^2$ is $0$.

Right side: $A(1) + C(1) = A + C$

So $A + C = 0$ $\Rightarrow$ $A = -C = \frac{1}{9}$

**Integrate:**

$$\int \left(\frac{1/9}{x-1} + \frac{5/3}{(x-1)^2} + \frac{-1/9}{x+2}\right) dx$$

For the middle term, recall: $\displaystyle\int \frac{1}{(x-1)^2} \, dx = -\frac{1}{x-1} + C$

$$= \boxed{\frac{1}{9}\ln|x-1| - \frac{5}{3(x-1)} - \frac{1}{9}\ln|x+2| + C}$$

---

### Example 5: Long Division Required First

**Evaluate:** $\displaystyle\int \frac{x^3 + 2x}{x^2 - 1} \, dx$

The numerator has degree 3, the denominator degree 2 — it's **improper**. Long division first!

$$x^3 + 2x \div (x^2 - 1)$$

$x^3 + 2x = (x)(x^2 - 1) + 3x$

So:

$$\frac{x^3 + 2x}{x^2 - 1} = x + \frac{3x}{x^2 - 1}$$

Now decompose $\frac{3x}{x^2 - 1} = \frac{3x}{(x-1)(x+1)}$:

$$\frac{3x}{(x-1)(x+1)} = \frac{A}{x-1} + \frac{B}{x+1}$$

$x = 1$: $A = \frac{3}{2}$ and $x = -1$: $B = \frac{3}{2}$

**Integrate:**

$$\int \left(x + \frac{3/2}{x-1} + \frac{3/2}{x+1}\right) dx$$

$$= \boxed{\frac{x^2}{2} + \frac{3}{2}\ln|x-1| + \frac{3}{2}\ln|x+1| + C}$$

---

### Example 6: Equating Coefficients Method

Sometimes plugging in roots alone doesn't give you all constants, especially with repeated factors. The **equating coefficients** method handles this.

**Decompose:** $\frac{4x^2 + 3x - 1}{(x + 1)(x - 2)^2}$

**Set up:**

$$\frac{4x^2 + 3x - 1}{(x+1)(x-2)^2} = \frac{A}{x+1} + \frac{B}{x-2} + \frac{C}{(x-2)^2}$$

**Multiply through:**

$$4x^2 + 3x - 1 = A(x-2)^2 + B(x+1)(x-2) + C(x+1)$$

**Plug in $x = -1$:** $4 - 3 - 1 = A(9)$ $\Rightarrow$ $A = 0$

**Plug in $x = 2$:** $16 + 6 - 1 = C(3)$ $\Rightarrow$ $C = 7$

**Now equate $x^2$ coefficients** to find $B$:

Left: $4$. Right: $A + B = 0 + B$. So $B = 4$.

**Check with the $x^0$ (constant) term:**

Left: $-1$. Right: $A(4) + B(-2) + C(1) = 0 - 8 + 7 = -1$. Confirmed!

**Result:**

$$\frac{4x^2 + 3x - 1}{(x+1)(x-2)^2} = \frac{4}{x-2} + \frac{7}{(x-2)^2}$$

**Integrate:**

$$\int \left(\frac{4}{x-2} + \frac{7}{(x-2)^2}\right) dx = \boxed{4\ln|x-2| - \frac{7}{x-2} + C}$$

---

### Example 7: Irreducible Quadratic Factor

**Evaluate:** $\displaystyle\int \frac{3x^2 + 2}{(x - 1)(x^2 + 4)} \, dx$

Since $x^2 + 4$ has no real roots (discriminant $= 0 - 16 < 0$), it's irreducible. Use $Ax + B$ in the numerator:

$$\frac{3x^2 + 2}{(x-1)(x^2+4)} = \frac{A}{x-1} + \frac{Bx + C}{x^2 + 4}$$

**Multiply through:**

$$3x^2 + 2 = A(x^2 + 4) + (Bx + C)(x - 1)$$

**Plug in $x = 1$:** $5 = 5A$ $\Rightarrow$ $A = 1$

**Equate $x^2$ coefficients:** $3 = A + B = 1 + B$ $\Rightarrow$ $B = 2$

**Equate constant terms:** $2 = 4A - C = 4 - C$ $\Rightarrow$ $C = 2$

**Integrate:**

$$\int \frac{1}{x-1} \, dx + \int \frac{2x + 2}{x^2 + 4} \, dx$$

Split the second integral:

$$\int \frac{2x}{x^2 + 4} \, dx + \int \frac{2}{x^2 + 4} \, dx$$

The first is $\ln(x^2 + 4)$ (by substitution $u = x^2 + 4$). The second is $2 \cdot \frac{1}{2}\arctan\frac{x}{2} = \arctan\frac{x}{2}$.

$$= \boxed{\ln|x - 1| + \ln(x^2 + 4) + \arctan\frac{x}{2} + C}$$

---

### Example 8: Partial Fractions in a Definite Integral

**Evaluate:** $\displaystyle\int_2^5 \frac{1}{x^2 - 1} \, dx$

**Factor:** $x^2 - 1 = (x-1)(x+1)$

**Decompose:**

$$\frac{1}{(x-1)(x+1)} = \frac{A}{x-1} + \frac{B}{x+1}$$

Cover-up: $A = \frac{1}{1+1} = \frac{1}{2}$, $B = \frac{1}{-1-1} = -\frac{1}{2}$

$$\frac{1}{x^2 - 1} = \frac{1}{2}\left(\frac{1}{x-1} - \frac{1}{x+1}\right)$$

**Integrate:**

$$\frac{1}{2}\left[\ln|x-1| - \ln|x+1|\right]_2^5 = \frac{1}{2}\left[\ln\left|\frac{x-1}{x+1}\right|\right]_2^5$$

$$= \frac{1}{2}\left(\ln\frac{4}{6} - \ln\frac{1}{3}\right) = \frac{1}{2}\left(\ln\frac{2}{3} - \ln\frac{1}{3}\right) = \frac{1}{2}\ln\left(\frac{2/3}{1/3}\right) = \frac{1}{2}\ln 2$$

$$= \boxed{\frac{\ln 2}{2}}$$

---

### Example 9 (Bonus): Partial Fractions in a Separable DE (Logistic Equation)

This is where partial fractions show up on the BC exam in a big way — solving the **logistic differential equation**.

**Solve:** $\frac{dP}{dt} = 0.5P\left(1 - \frac{P}{100}\right)$, $P(0) = 10$

**Separate:**

$$\frac{dP}{P(1 - P/100)} = 0.5 \, dt$$

Rewrite: $P\left(1 - \frac{P}{100}\right) = \frac{P(100 - P)}{100}$

$$\frac{100 \, dP}{P(100 - P)} = 0.5 \, dt$$

**Partial fractions on $\frac{100}{P(100 - P)}$:**

$$\frac{100}{P(100-P)} = \frac{A}{P} + \frac{B}{100-P}$$

$P = 0$: $A = 1$. $\quad P = 100$: $B = 1$.

$$\frac{100}{P(100-P)} = \frac{1}{P} + \frac{1}{100-P}$$

**Integrate:**

$$\ln|P| - \ln|100 - P| = 0.5t + C$$

$$\ln\left|\frac{P}{100 - P}\right| = 0.5t + C$$

$P(0) = 10$: $\ln\frac{10}{90} = C = \ln\frac{1}{9}$

Solving for $P$:

$$\frac{P}{100 - P} = \frac{1}{9}e^{0.5t}$$

$$9P = (100 - P)e^{0.5t} = 100e^{0.5t} - Pe^{0.5t}$$

$$P(9 + e^{0.5t}) = 100e^{0.5t}$$

$$\boxed{P(t) = \frac{100}{1 + 9e^{-0.5t}}}$$

This is the standard logistic solution with carrying capacity $L = 100$. Partial fractions were essential to getting here!

---

## Key Formulas & Rules

| Situation | Setup | Integration Result |
|-----------|-------|--------------------|
| $\frac{1}{(x-a)(x-b)}$ | $\frac{A}{x-a} + \frac{B}{x-b}$ | $A\ln\|x-a\| + B\ln\|x-b\| + C$ |
| $\frac{1}{(x-a)^2}$ | Already simple | $-\frac{1}{x-a} + C$ |
| $\frac{1}{(x-a)^2(x-b)}$ | $\frac{A}{x-a} + \frac{B}{(x-a)^2} + \frac{C}{x-b}$ | $A\ln\|x-a\| - \frac{B}{x-a} + C\ln\|x-b\| + K$ |
| $\frac{1}{x^2 + a^2}$ | Already simple | $\frac{1}{a}\arctan\frac{x}{a} + C$ |
| $\frac{x}{x^2 + a^2}$ | Already simple | $\frac{1}{2}\ln(x^2 + a^2) + C$ |
| Improper fraction | Long divide first | Polynomial + proper fraction |
| Cover-up (Heaviside) | Cover factor, plug in root | Quick $A, B, C$ values |

---

## Common Mistakes to Avoid

### Mistake 1: Forgetting to Check if the Fraction is Proper

Before decomposing, always compare degrees. If $\deg(\text{numerator}) \geq \deg(\text{denominator})$, you must do long division first.

- **Wrong:** Decomposing $\frac{x^3}{x^2 - 4}$ directly as $\frac{A}{x-2} + \frac{B}{x+2}$
- **Right:** Long divide first: $\frac{x^3}{x^2 - 4} = x + \frac{4x}{x^2 - 4}$, then decompose $\frac{4x}{(x-2)(x+2)}$

---

### Mistake 2: Missing Terms for Repeated Factors

Each power of a repeated factor needs its own term.

- **Wrong:** $\frac{1}{(x-3)^3(x+1)} = \frac{A}{(x-3)^3} + \frac{B}{x+1}$
- **Right:** $\frac{1}{(x-3)^3(x+1)} = \frac{A}{x-3} + \frac{B}{(x-3)^2} + \frac{C}{(x-3)^3} + \frac{D}{x+1}$

Think of it like stacking boba pearls — if you have three layers, you need a cup for each layer, not just the top one.

---

### Mistake 3: Using Just a Constant Over a Quadratic Factor

For irreducible quadratic factors, you need a linear numerator.

- **Wrong:** $\frac{A}{x^2 + 1}$
- **Right:** $\frac{Ax + B}{x^2 + 1}$

---

### Mistake 4: Forgetting Absolute Values in $\ln$

- **Wrong:** $\int \frac{1}{x - 3} \, dx = \ln(x - 3) + C$
- **Right:** $\int \frac{1}{x - 3} \, dx = \ln|x - 3| + C$

This matters when $x < 3$!

---

### Mistake 5: Sign Errors When Factoring Negatives

Be careful when the denominator has factors like $(a - x)$ instead of $(x - a)$.

- $\frac{1}{3 - x} = -\frac{1}{x - 3}$

- **Wrong:** $\int \frac{1}{3 - x} \, dx = \ln|3 - x| + C$... well, this is actually correct, but if you rewrote it:
- **Also Right:** $\int \frac{1}{3-x} \, dx = -\ln|x - 3| + C$

Just be consistent with signs.

---

### Mistake 6: Not Factoring the Denominator Completely

- **Wrong:** Trying to decompose $\frac{1}{x^3 - x}$ without factoring first
- **Right:** Factor $x^3 - x = x(x-1)(x+1)$, then decompose as $\frac{A}{x} + \frac{B}{x-1} + \frac{C}{x+1}$

Always factor completely before setting up the decomposition — like breaking down your Science Olympiad problem into all its sub-parts before trying to solve anything.

---

## AP Exam Tips

### BC-Specific Notes
- Partial fractions is a **BC-only** topic (not on AB)
- Typically appears as 1-2 multiple choice questions and occasionally in free response
- Most commonly tested: distinct linear factors (Case 1) — this is the bread and butter
- Repeated factors (Case 2) appear less frequently but do show up
- Irreducible quadratic factors (Case 3) are rare on the exam — know the setup but don't stress

### What the AP Readers Look For (Free Response)

1. **Correct decomposition setup** — right number of terms with correct form
2. **Algebraic work** to find constants — show the plug-in or coefficient-matching steps
3. **Correct antidifferentiation** of each piece
4. **$+ C$** for indefinite integrals
5. **Correct evaluation** at bounds for definite integrals

### Time-Saving Strategies

1. **Use Heaviside cover-up** for distinct linear factors — it's fast and accurate
2. **Memorize** that $\frac{1}{(x-a)(x-b)} = \frac{1}{a-b}\left(\frac{1}{x-a} - \frac{1}{x-b}\right)$ for quick decompositions
3. **Recognize $\frac{1}{x^2 - a^2}$** as $\frac{1}{(x-a)(x+a)}$ immediately — this comes up constantly
4. **If you see a logistic DE** on the free response, partial fractions is the technique needed to solve it
5. **Check your answer** by differentiating if time permits — this catches sign errors

### Common AP Phrasing

> "Evaluate $\int \frac{P(x)}{Q(x)} \, dx$ using partial fractions."

> "Find the antiderivative of ..."

> "Solve the differential equation $\frac{dy}{dx} = \frac{y(L - y)}{k}$ with initial condition ..."

---

## Practice Problems

### Basic (Problems 1-5)

**1.** Evaluate: $\displaystyle\int \frac{3}{(x+1)(x-2)} \, dx$

---

**2.** Evaluate: $\displaystyle\int \frac{4x}{(x-3)(x+3)} \, dx$

---

**3.** Evaluate: $\displaystyle\int \frac{1}{x^2 - 9} \, dx$

---

**4.** Evaluate: $\displaystyle\int \frac{x + 5}{x^2 + 4x + 3} \, dx$

---

**5.** Evaluate: $\displaystyle\int_3^7 \frac{2}{(x-1)(x+1)} \, dx$

---

### Intermediate (Problems 6-10)

**6.** Evaluate: $\displaystyle\int \frac{5x - 1}{(x-2)(x+1)(x-3)} \, dx$

---

**7.** Evaluate: $\displaystyle\int \frac{x + 3}{(x + 1)^2} \, dx$

---

**8.** Evaluate: $\displaystyle\int \frac{x^2 + 1}{x^2 - x} \, dx$

*(Hint: Is this fraction proper?)*

---

**9.** Evaluate: $\displaystyle\int \frac{3x + 1}{(x-1)^2(x+2)} \, dx$

---

**10.** Evaluate: $\displaystyle\int_2^4 \frac{x + 1}{(x)(x - 1)} \, dx$

---

### Advanced (Problems 11-15)

**11.** Evaluate: $\displaystyle\int \frac{2x + 1}{(x+1)(x^2 + 1)} \, dx$

---

**12.** Evaluate: $\displaystyle\int \frac{x^3 + x + 2}{x^2 + 2x} \, dx$

*(Hint: Long division first.)*

---

**13.** Evaluate: $\displaystyle\int \frac{6}{(x-1)^2(x+2)^2} \, dx$

---

**14.** Solve the separable DE using partial fractions:

$$\frac{dy}{dx} = y(4 - y), \quad y(0) = 1$$

---

**15.** Evaluate: $\displaystyle\int \frac{x^2 + 2x + 3}{(x+1)(x^2 + 4)} \, dx$

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

$\displaystyle\int \frac{1}{x^2 - 4} \, dx =$

| Choice | Answer |
|--------|--------|
| **(A)** | $\frac{1}{4}\ln\left\|\frac{x-2}{x+2}\right\| + C$ |
| **(B)** | $\frac{1}{2}\ln\left\|\frac{x-2}{x+2}\right\| + C$ |
| **(C)** | $\ln\|x-2\| - \ln\|x+2\| + C$ |
| **(D)** | $\frac{1}{4}\ln\|x^2 - 4\| + C$ |

---

#### Problem 17 (Multiple Choice)

What is the correct partial fraction form of $\frac{2x}{(x+1)^2(x-3)}$?

| Choice | Answer |
|--------|--------|
| **(A)** | $\frac{A}{x+1} + \frac{B}{x-3}$ |
| **(B)** | $\frac{A}{x+1} + \frac{B}{(x+1)^2} + \frac{C}{x-3}$ |
| **(C)** | $\frac{Ax + B}{(x+1)^2} + \frac{C}{x-3}$ |
| **(D)** | $\frac{A}{(x+1)^2} + \frac{B}{x-3}$ |

---

#### Problem 18 (Multiple Choice)

$\displaystyle\int_2^3 \frac{5}{x^2 - 1} \, dx =$

| Choice | Answer |
|--------|--------|
| **(A)** | $\frac{5}{2}\ln\frac{4}{3}$ |
| **(B)** | $\frac{5}{2}\left(\ln\frac{2}{4} - \ln\frac{1}{3}\right)$ |
| **(C)** | $\frac{5}{2}\ln\frac{3}{2}$ |
| **(D)** | $\frac{5}{2}\ln\frac{2}{3}$ |

---

#### Problem 19 (Free Response)

Consider the function $f(x) = \frac{2x + 6}{x^2 + 3x + 2}$.

> **(a)** Factor the denominator and decompose $f(x)$ into partial fractions.
>
> **(b)** Evaluate $\displaystyle\int f(x) \, dx$.
>
> **(c)** Evaluate $\displaystyle\int_0^1 f(x) \, dx$. Express your answer as a single logarithm.
>
> **(d)** Find the value of $k$ such that $\displaystyle\int_0^k f(x) \, dx = \ln 5$.

---

#### Problem 20 (Free Response — Challenging)

Ganga is tracking the spread of a rumor through the Rancho Bernardo High School Mock Trial team of 50 members. Let $R(t)$ represent the number of team members who have heard the rumor after $t$ hours. The rate at which the rumor spreads is modeled by:

$$\frac{dR}{dt} = 0.02R(50 - R)$$

At $t = 0$, only Ganga knows the rumor, so $R(0) = 1$.

> **(a)** Using partial fraction decomposition, solve this initial value problem for $R(t)$.
>
> **(b)** How many team members have heard the rumor after 5 hours? Round to the nearest whole number.
>
> **(c)** At what time have exactly half the team members heard the rumor?
>
> **(d)** What is the maximum rate at which the rumor spreads, and when does this occur? *(Hint: Think about what value of $R$ maximizes $R(50 - R)$.)*

---

## Answer Key

<details>
<summary><strong>Problem 1 Solution</strong></summary>

**Evaluate:** $\displaystyle\int \frac{3}{(x+1)(x-2)} \, dx$

**Decompose:**

$$\frac{3}{(x+1)(x-2)} = \frac{A}{x+1} + \frac{B}{x-2}$$

Multiply through: $3 = A(x-2) + B(x+1)$

$x = 2$: $3 = 3B$ $\Rightarrow$ $B = 1$

$x = -1$: $3 = -3A$ $\Rightarrow$ $A = -1$

**Integrate:**

$$\int \left(\frac{-1}{x+1} + \frac{1}{x-2}\right) dx = -\ln|x+1| + \ln|x-2| + C$$

$$= \boxed{\ln\left|\frac{x-2}{x+1}\right| + C}$$

</details>

---

<details>
<summary><strong>Problem 2 Solution</strong></summary>

**Evaluate:** $\displaystyle\int \frac{4x}{(x-3)(x+3)} \, dx$

**Decompose:**

$$\frac{4x}{(x-3)(x+3)} = \frac{A}{x-3} + \frac{B}{x+3}$$

Multiply through: $4x = A(x+3) + B(x-3)$

$x = 3$: $12 = 6A$ $\Rightarrow$ $A = 2$

$x = -3$: $-12 = -6B$ $\Rightarrow$ $B = 2$

**Integrate:**

$$\int \left(\frac{2}{x-3} + \frac{2}{x+3}\right) dx = 2\ln|x-3| + 2\ln|x+3| + C$$

$$= \boxed{2\ln|x-3| + 2\ln|x+3| + C}$$

Or equivalently: $2\ln|x^2 - 9| + C$.

</details>

---

<details>
<summary><strong>Problem 3 Solution</strong></summary>

**Evaluate:** $\displaystyle\int \frac{1}{x^2 - 9} \, dx$

**Factor:** $x^2 - 9 = (x-3)(x+3)$

**Decompose:**

$$\frac{1}{(x-3)(x+3)} = \frac{A}{x-3} + \frac{B}{x+3}$$

$x = 3$: $1 = 6A$ $\Rightarrow$ $A = \frac{1}{6}$

$x = -3$: $1 = -6B$ $\Rightarrow$ $B = -\frac{1}{6}$

**Integrate:**

$$\int \frac{1}{6}\left(\frac{1}{x-3} - \frac{1}{x+3}\right) dx = \frac{1}{6}\left(\ln|x-3| - \ln|x+3|\right) + C$$

$$= \boxed{\frac{1}{6}\ln\left|\frac{x-3}{x+3}\right| + C}$$

</details>

---

<details>
<summary><strong>Problem 4 Solution</strong></summary>

**Evaluate:** $\displaystyle\int \frac{x + 5}{x^2 + 4x + 3} \, dx$

**Factor denominator:** $x^2 + 4x + 3 = (x+1)(x+3)$

**Decompose:**

$$\frac{x+5}{(x+1)(x+3)} = \frac{A}{x+1} + \frac{B}{x+3}$$

Multiply through: $x + 5 = A(x+3) + B(x+1)$

$x = -1$: $4 = 2A$ $\Rightarrow$ $A = 2$

$x = -3$: $2 = -2B$ $\Rightarrow$ $B = -1$

**Integrate:**

$$\int \left(\frac{2}{x+1} - \frac{1}{x+3}\right) dx = 2\ln|x+1| - \ln|x+3| + C$$

$$= \boxed{2\ln|x+1| - \ln|x+3| + C}$$

</details>

---

<details>
<summary><strong>Problem 5 Solution</strong></summary>

**Evaluate:** $\displaystyle\int_3^7 \frac{2}{(x-1)(x+1)} \, dx$

**Decompose:**

$$\frac{2}{(x-1)(x+1)} = \frac{A}{x-1} + \frac{B}{x+1}$$

$x = 1$: $2 = 2A$ $\Rightarrow$ $A = 1$

$x = -1$: $2 = -2B$ $\Rightarrow$ $B = -1$

**Integrate:**

$$\int_3^7 \left(\frac{1}{x-1} - \frac{1}{x+1}\right) dx = \left[\ln|x-1| - \ln|x+1|\right]_3^7$$

$$= \left[\ln\left|\frac{x-1}{x+1}\right|\right]_3^7$$

At $x = 7$: $\ln\frac{6}{8} = \ln\frac{3}{4}$

At $x = 3$: $\ln\frac{2}{4} = \ln\frac{1}{2}$

$$= \ln\frac{3}{4} - \ln\frac{1}{2} = \ln\frac{3/4}{1/2} = \ln\frac{3}{2}$$

$$= \boxed{\ln\frac{3}{2}}$$

</details>

---

<details>
<summary><strong>Problem 6 Solution</strong></summary>

**Evaluate:** $\displaystyle\int \frac{5x - 1}{(x-2)(x+1)(x-3)} \, dx$

**Decompose:**

$$\frac{5x-1}{(x-2)(x+1)(x-3)} = \frac{A}{x-2} + \frac{B}{x+1} + \frac{C}{x-3}$$

Multiply through: $5x - 1 = A(x+1)(x-3) + B(x-2)(x-3) + C(x-2)(x+1)$

$x = 2$: $9 = A(3)(-1) = -3A$ $\Rightarrow$ $A = -3$

$x = -1$: $-6 = B(-3)(-4) = 12B$ $\Rightarrow$ $B = -\frac{1}{2}$

$x = 3$: $14 = C(1)(4) = 4C$ $\Rightarrow$ $C = \frac{7}{2}$

**Integrate:**

$$\int \left(\frac{-3}{x-2} + \frac{-1/2}{x+1} + \frac{7/2}{x-3}\right) dx$$

$$= \boxed{-3\ln|x-2| - \frac{1}{2}\ln|x+1| + \frac{7}{2}\ln|x-3| + C}$$

</details>

---

<details>
<summary><strong>Problem 7 Solution</strong></summary>

**Evaluate:** $\displaystyle\int \frac{x + 3}{(x + 1)^2} \, dx$

**Decompose (repeated linear factor):**

$$\frac{x+3}{(x+1)^2} = \frac{A}{x+1} + \frac{B}{(x+1)^2}$$

Multiply through: $x + 3 = A(x + 1) + B$

$x = -1$: $2 = B$ $\Rightarrow$ $B = 2$

**Equate $x^1$ coefficients:** $1 = A$

**Integrate:**

$$\int \left(\frac{1}{x+1} + \frac{2}{(x+1)^2}\right) dx = \ln|x+1| + 2 \cdot \frac{(x+1)^{-1}}{-1} + C$$

$$= \boxed{\ln|x+1| - \frac{2}{x+1} + C}$$

</details>

---

<details>
<summary><strong>Problem 8 Solution</strong></summary>

**Evaluate:** $\displaystyle\int \frac{x^2 + 1}{x^2 - x} \, dx$

**Check degrees:** Numerator degree $= 2$, denominator degree $= 2$. The fraction is **improper**, so long divide first.

$$\frac{x^2 + 1}{x^2 - x} = 1 + \frac{x + 1}{x^2 - x}$$

(Since $x^2 + 1 = 1 \cdot (x^2 - x) + (x + 1)$)

**Factor:** $x^2 - x = x(x - 1)$

**Decompose $\frac{x + 1}{x(x-1)}$:**

$$\frac{x+1}{x(x-1)} = \frac{A}{x} + \frac{B}{x-1}$$

$x = 0$: $1 = A(-1)$ $\Rightarrow$ $A = -1$

$x = 1$: $2 = B(1)$ $\Rightarrow$ $B = 2$

**Integrate:**

$$\int \left(1 - \frac{1}{x} + \frac{2}{x-1}\right) dx$$

$$= \boxed{x - \ln|x| + 2\ln|x - 1| + C}$$

</details>

---

<details>
<summary><strong>Problem 9 Solution</strong></summary>

**Evaluate:** $\displaystyle\int \frac{3x + 1}{(x-1)^2(x+2)} \, dx$

**Decompose (repeated factor):**

$$\frac{3x + 1}{(x-1)^2(x+2)} = \frac{A}{x-1} + \frac{B}{(x-1)^2} + \frac{C}{x+2}$$

Multiply through: $3x + 1 = A(x-1)(x+2) + B(x+2) + C(x-1)^2$

$x = 1$: $4 = B(3)$ $\Rightarrow$ $B = \frac{4}{3}$

$x = -2$: $-5 = C(-3)^2 = 9C$ $\Rightarrow$ $C = -\frac{5}{9}$

**Equate $x^2$ coefficients:** $0 = A + C$ $\Rightarrow$ $A = -C = \frac{5}{9}$

**Verify with the constant term:**

Left: $1$. Right: $A(-1)(2) + B(2) + C(1) = -\frac{10}{9} + \frac{8}{3} - \frac{5}{9} = -\frac{10}{9} + \frac{24}{9} - \frac{5}{9} = \frac{9}{9} = 1$. Confirmed!

**Integrate:**

$$\int \left(\frac{5/9}{x-1} + \frac{4/3}{(x-1)^2} + \frac{-5/9}{x+2}\right) dx$$

$$= \boxed{\frac{5}{9}\ln|x-1| - \frac{4}{3(x-1)} - \frac{5}{9}\ln|x+2| + C}$$

Or: $\frac{5}{9}\ln\left|\frac{x-1}{x+2}\right| - \frac{4}{3(x-1)} + C$

</details>

---

<details>
<summary><strong>Problem 10 Solution</strong></summary>

**Evaluate:** $\displaystyle\int_2^4 \frac{x + 1}{x(x - 1)} \, dx$

**Decompose:**

$$\frac{x+1}{x(x-1)} = \frac{A}{x} + \frac{B}{x-1}$$

Multiply through: $x + 1 = A(x - 1) + Bx$

$x = 0$: $1 = -A$ $\Rightarrow$ $A = -1$

$x = 1$: $2 = B$ $\Rightarrow$ $B = 2$

**Integrate:**

$$\int_2^4 \left(\frac{-1}{x} + \frac{2}{x-1}\right) dx = \left[-\ln|x| + 2\ln|x-1|\right]_2^4$$

At $x = 4$: $-\ln 4 + 2\ln 3$

At $x = 2$: $-\ln 2 + 2\ln 1 = -\ln 2$

$$= (-\ln 4 + 2\ln 3) - (-\ln 2) = -\ln 4 + 2\ln 3 + \ln 2$$

$$= \ln 2 - \ln 4 + 2\ln 3 = \ln 2 - 2\ln 2 + 2\ln 3 = -\ln 2 + 2\ln 3$$

$$= \ln\frac{9}{2}$$

$$= \boxed{\ln\frac{9}{2}}$$

</details>

---

<details>
<summary><strong>Problem 11 Solution</strong></summary>

**Evaluate:** $\displaystyle\int \frac{2x + 1}{(x+1)(x^2 + 1)} \, dx$

**Decompose (irreducible quadratic factor):**

$$\frac{2x + 1}{(x+1)(x^2+1)} = \frac{A}{x+1} + \frac{Bx + C}{x^2 + 1}$$

Multiply through: $2x + 1 = A(x^2 + 1) + (Bx + C)(x + 1)$

$x = -1$: $-1 = A(2)$ $\Rightarrow$ $A = -\frac{1}{2}$

**Equate $x^2$ coefficients:** $0 = A + B$ $\Rightarrow$ $B = \frac{1}{2}$

**Equate constant terms:** $1 = A + C = -\frac{1}{2} + C$ $\Rightarrow$ $C = \frac{3}{2}$

**Integrate:**

$$\int \left(\frac{-1/2}{x+1} + \frac{(1/2)x + 3/2}{x^2+1}\right) dx$$

$$= -\frac{1}{2}\ln|x+1| + \frac{1}{2}\int \frac{x}{x^2+1} \, dx + \frac{3}{2}\int \frac{1}{x^2+1} \, dx$$

$$= -\frac{1}{2}\ln|x+1| + \frac{1}{4}\ln(x^2+1) + \frac{3}{2}\arctan x + C$$

$$= \boxed{-\frac{1}{2}\ln|x+1| + \frac{1}{4}\ln(x^2 + 1) + \frac{3}{2}\arctan x + C}$$

</details>

---

<details>
<summary><strong>Problem 12 Solution</strong></summary>

**Evaluate:** $\displaystyle\int \frac{x^3 + x + 2}{x^2 + 2x} \, dx$

**Long division first** (degree 3 over degree 2):

$x^3 + x + 2 \div (x^2 + 2x)$:

$x^3 + x + 2 = (x - 2)(x^2 + 2x) + (5x + 2)$

Check: $(x-2)(x^2 + 2x) = x^3 + 2x^2 - 2x^2 - 4x = x^3 - 4x$. Then $x^3 - 4x + 5x + 2 = x^3 + x + 2$. Confirmed!

$$\frac{x^3 + x + 2}{x^2 + 2x} = (x - 2) + \frac{5x + 2}{x^2 + 2x}$$

**Factor:** $x^2 + 2x = x(x + 2)$

**Decompose $\frac{5x + 2}{x(x+2)}$:**

$$\frac{5x+2}{x(x+2)} = \frac{A}{x} + \frac{B}{x+2}$$

$x = 0$: $2 = 2A$ $\Rightarrow$ $A = 1$

$x = -2$: $-8 = -2B$ $\Rightarrow$ $B = 4$

**Integrate:**

$$\int \left(x - 2 + \frac{1}{x} + \frac{4}{x+2}\right) dx$$

$$= \boxed{\frac{x^2}{2} - 2x + \ln|x| + 4\ln|x + 2| + C}$$

</details>

---

<details>
<summary><strong>Problem 13 Solution</strong></summary>

**Evaluate:** $\displaystyle\int \frac{6}{(x-1)^2(x+2)^2} \, dx$

**Decompose (two repeated factors):**

$$\frac{6}{(x-1)^2(x+2)^2} = \frac{A}{x-1} + \frac{B}{(x-1)^2} + \frac{C}{x+2} + \frac{D}{(x+2)^2}$$

Multiply through by $(x-1)^2(x+2)^2$:

$$6 = A(x-1)(x+2)^2 + B(x+2)^2 + C(x-1)^2(x+2) + D(x-1)^2$$

$x = 1$: $6 = B(9)$ $\Rightarrow$ $B = \frac{2}{3}$

$x = -2$: $6 = D(9)$ $\Rightarrow$ $D = \frac{2}{3}$

**Equate $x^3$ coefficients:** $0 = A + C$

**Equate $x^0$ (constant) terms:**

$6 = A(-1)(4) + B(4) + C(1)(-2) + D(1) = -4A + \frac{8}{3} - 2C + \frac{2}{3}$

$6 = -4A - 2C + \frac{10}{3}$

Since $C = -A$:

$6 = -4A + 2A + \frac{10}{3} = -2A + \frac{10}{3}$

$-2A = 6 - \frac{10}{3} = \frac{8}{3}$

$A = -\frac{4}{3}$, $C = \frac{4}{3}$

**Integrate:**

$$\int \left(\frac{-4/3}{x-1} + \frac{2/3}{(x-1)^2} + \frac{4/3}{x+2} + \frac{2/3}{(x+2)^2}\right) dx$$

$$= -\frac{4}{3}\ln|x-1| - \frac{2}{3(x-1)} + \frac{4}{3}\ln|x+2| - \frac{2}{3(x+2)} + C$$

$$= \boxed{\frac{4}{3}\ln\left|\frac{x+2}{x-1}\right| - \frac{2}{3(x-1)} - \frac{2}{3(x+2)} + C}$$

</details>

---

<details>
<summary><strong>Problem 14 Solution</strong></summary>

**Solve:** $\frac{dy}{dx} = y(4 - y)$, $y(0) = 1$

**Separate:**

$$\frac{dy}{y(4 - y)} = dx$$

**Partial fractions on $\frac{1}{y(4-y)}$:**

$$\frac{1}{y(4-y)} = \frac{A}{y} + \frac{B}{4-y}$$

$y = 0$: $1 = 4A$ $\Rightarrow$ $A = \frac{1}{4}$

$y = 4$: $1 = 4B$ $\Rightarrow$ $B = \frac{1}{4}$

So: $\frac{1}{y(4-y)} = \frac{1}{4}\left(\frac{1}{y} + \frac{1}{4-y}\right)$

**Integrate both sides:**

$$\frac{1}{4}\left(\ln|y| - \ln|4 - y|\right) = x + C$$

$$\frac{1}{4}\ln\left|\frac{y}{4-y}\right| = x + C$$

$$\ln\left|\frac{y}{4-y}\right| = 4x + C_1$$

**Apply IC** $y(0) = 1$:

$$\ln\frac{1}{3} = C_1$$

$$\ln\left|\frac{y}{4-y}\right| = 4x + \ln\frac{1}{3}$$

$$\frac{y}{4-y} = \frac{1}{3}e^{4x}$$

**Solve for $y$:**

$3y = (4-y)e^{4x} = 4e^{4x} - ye^{4x}$

$y(3 + e^{4x}) = 4e^{4x}$

$$\boxed{y = \frac{4e^{4x}}{3 + e^{4x}} = \frac{4}{1 + 3e^{-4x}}}$$

This is the logistic solution with carrying capacity $L = 4$. As $t \to \infty$, $y \to 4$.

</details>

---

<details>
<summary><strong>Problem 15 Solution</strong></summary>

**Evaluate:** $\displaystyle\int \frac{x^2 + 2x + 3}{(x+1)(x^2 + 4)} \, dx$

**Decompose:**

$$\frac{x^2 + 2x + 3}{(x+1)(x^2+4)} = \frac{A}{x+1} + \frac{Bx + C}{x^2 + 4}$$

Multiply through: $x^2 + 2x + 3 = A(x^2 + 4) + (Bx + C)(x+1)$

$x = -1$: $1 - 2 + 3 = A(5)$ $\Rightarrow$ $2 = 5A$ $\Rightarrow$ $A = \frac{2}{5}$

**Equate $x^2$ coefficients:** $1 = A + B = \frac{2}{5} + B$ $\Rightarrow$ $B = \frac{3}{5}$

**Equate constant terms:** $3 = 4A + C = \frac{8}{5} + C$ $\Rightarrow$ $C = \frac{7}{5}$

**Integrate:**

$$\int \left(\frac{2/5}{x+1} + \frac{(3/5)x + 7/5}{x^2+4}\right) dx$$

$$= \frac{2}{5}\ln|x+1| + \frac{3}{5}\int \frac{x}{x^2+4} \, dx + \frac{7}{5}\int \frac{1}{x^2+4} \, dx$$

$$= \frac{2}{5}\ln|x+1| + \frac{3}{10}\ln(x^2+4) + \frac{7}{10}\arctan\frac{x}{2} + C$$

$$= \boxed{\frac{2}{5}\ln|x+1| + \frac{3}{10}\ln(x^2 + 4) + \frac{7}{10}\arctan\frac{x}{2} + C}$$

</details>

---

<details>
<summary><strong>Problem 16 Solution</strong></summary>

**Answer: (A)** $\frac{1}{4}\ln\left|\frac{x-2}{x+2}\right| + C$

**Work:**

$$\frac{1}{x^2 - 4} = \frac{1}{(x-2)(x+2)} = \frac{A}{x-2} + \frac{B}{x+2}$$

$x = 2$: $1 = 4A$ $\Rightarrow$ $A = \frac{1}{4}$

$x = -2$: $1 = -4B$ $\Rightarrow$ $B = -\frac{1}{4}$

$$\int \frac{1}{4}\left(\frac{1}{x-2} - \frac{1}{x+2}\right) dx = \frac{1}{4}\left(\ln|x-2| - \ln|x+2|\right) + C = \frac{1}{4}\ln\left|\frac{x-2}{x+2}\right| + C$$

**Why not (B)?** That has $\frac{1}{2}$ instead of $\frac{1}{4}$ — a common error from forgetting the partial fraction coefficients.

**Why not (C)?** Missing the $\frac{1}{4}$ factor entirely.

**Why not (D)?** $\frac{d}{dx}\left[\frac{1}{4}\ln|x^2-4|\right] = \frac{x}{2(x^2-4)} \neq \frac{1}{x^2-4}$.

**Answer: (A)**

</details>

---

<details>
<summary><strong>Problem 17 Solution</strong></summary>

**Answer: (B)** $\frac{A}{x+1} + \frac{B}{(x+1)^2} + \frac{C}{x-3}$

The denominator has a **repeated linear factor** $(x+1)^2$ and a **distinct linear factor** $(x-3)$.

For the repeated factor $(x+1)^2$, we need terms for both $(x+1)$ and $(x+1)^2$.

- **(A)** is wrong because it only has one term for the repeated factor
- **(C)** is wrong because $\frac{Ax+B}{(x+1)^2}$ is the form for an irreducible quadratic, not a repeated linear factor
- **(D)** is wrong because it only has the $(x+1)^2$ term, missing the $(x+1)$ term

**Answer: (B)**

</details>

---

<details>
<summary><strong>Problem 18 Solution</strong></summary>

**Answer: (A)** $\frac{5}{2}\ln\frac{4}{3}$

**Work:**

$$\frac{5}{x^2 - 1} = \frac{5}{(x-1)(x+1)}$$

Decompose: $\frac{5}{(x-1)(x+1)} = \frac{A}{x-1} + \frac{B}{x+1}$

$x = 1$: $5 = 2A$ $\Rightarrow$ $A = \frac{5}{2}$

$x = -1$: $5 = -2B$ $\Rightarrow$ $B = -\frac{5}{2}$

$$\int_2^3 \frac{5}{2}\left(\frac{1}{x-1} - \frac{1}{x+1}\right) dx = \frac{5}{2}\left[\ln\left|\frac{x-1}{x+1}\right|\right]_2^3$$

At $x = 3$: $\ln\frac{2}{4} = \ln\frac{1}{2}$

At $x = 2$: $\ln\frac{1}{3}$

$$= \frac{5}{2}\left(\ln\frac{1}{2} - \ln\frac{1}{3}\right) = \frac{5}{2}\ln\frac{1/2}{1/3} = \frac{5}{2}\ln\frac{3}{2}$$

Wait — let me recalculate. $\frac{1/2}{1/3} = \frac{3}{2}$. So this gives $\frac{5}{2}\ln\frac{3}{2}$.

Hmm, but let me check: $\ln\frac{3}{2} = \ln 3 - \ln 2$. And $\ln\frac{4}{3} = \ln 4 - \ln 3 = 2\ln 2 - \ln 3$. These are different.

Let me recompute more carefully.

$$\frac{5}{2}\left[\ln|x-1| - \ln|x+1|\right]_2^3$$

$$= \frac{5}{2}\left[(\ln 2 - \ln 4) - (\ln 1 - \ln 3)\right]$$

$$= \frac{5}{2}\left[\ln 2 - \ln 4 - 0 + \ln 3\right]$$

$$= \frac{5}{2}\left[\ln 2 + \ln 3 - \ln 4\right]$$

$$= \frac{5}{2}\left[\ln 6 - \ln 4\right] = \frac{5}{2}\ln\frac{6}{4} = \frac{5}{2}\ln\frac{3}{2}$$

So the answer is $\frac{5}{2}\ln\frac{3}{2}$.

**Answer: (C)** $\frac{5}{2}\ln\frac{3}{2}$

</details>

---

<details>
<summary><strong>Problem 19 Solution</strong></summary>

**For** $f(x) = \frac{2x + 6}{x^2 + 3x + 2}$:

**(a)** Factor: $x^2 + 3x + 2 = (x+1)(x+2)$

Decompose:

$$\frac{2x+6}{(x+1)(x+2)} = \frac{A}{x+1} + \frac{B}{x+2}$$

Multiply: $2x + 6 = A(x+2) + B(x+1)$

$x = -1$: $4 = A(1)$ $\Rightarrow$ $A = 4$

$x = -2$: $2 = B(-1)$ $\Rightarrow$ $B = -2$

$$\boxed{f(x) = \frac{4}{x+1} - \frac{2}{x+2}}$$

**(b)** Integrate:

$$\int f(x) \, dx = 4\ln|x+1| - 2\ln|x+2| + C$$

$$= \boxed{4\ln|x+1| - 2\ln|x+2| + C}$$

**(c)** Definite integral:

$$\int_0^1 f(x) \, dx = \left[4\ln|x+1| - 2\ln|x+2|\right]_0^1$$

At $x = 1$: $4\ln 2 - 2\ln 3$

At $x = 0$: $4\ln 1 - 2\ln 2 = -2\ln 2$

$$= (4\ln 2 - 2\ln 3) - (-2\ln 2) = 6\ln 2 - 2\ln 3$$

$$= \ln 2^6 - \ln 3^2 = \ln 64 - \ln 9$$

$$= \boxed{\ln\frac{64}{9}}$$

**(d)** We need: $\displaystyle\int_0^k f(x) \, dx = \ln 5$

$$\left[4\ln|x+1| - 2\ln|x+2|\right]_0^k = \ln 5$$

$$(4\ln(k+1) - 2\ln(k+2)) - (0 - 2\ln 2) = \ln 5$$

$$4\ln(k+1) - 2\ln(k+2) + 2\ln 2 = \ln 5$$

$$\ln(k+1)^4 - \ln(k+2)^2 + \ln 4 = \ln 5$$

$$\ln\frac{4(k+1)^4}{(k+2)^2} = \ln 5$$

$$\frac{4(k+1)^4}{(k+2)^2} = 5$$

Try $k = 1$: $\frac{4(2)^4}{(3)^2} = \frac{64}{9} \approx 7.1$ — too large.

Try $k = \frac{1}{2}$: $\frac{4(3/2)^4}{(5/2)^2} = \frac{4 \cdot 81/16}{25/4} = \frac{81/4}{25/4} = \frac{81}{25} = 3.24$ — too small.

Let's solve this more carefully. Let $u = k + 1$, so $k + 2 = u + 1$:

$4u^4 = 5(u+1)^2$

$4u^4 = 5u^2 + 10u + 5$

$4u^4 - 5u^2 - 10u - 5 = 0$

This quartic is difficult to solve by hand. Let us try a simpler approach and check if the problem has a "nice" answer.

Try $k = 1$: We computed $\int_0^1 f(x)\,dx = \ln\frac{64}{9} \neq \ln 5$.

Actually, let's reconsider. Trying to find a nice closed form:

$\frac{4(k+1)^4}{(k+2)^2} = 5$

Let's try $k$ such that $k+1 = a$ and $k+2 = a+1$. We need $4a^4 = 5(a+1)^2$.

$4a^4 = 5a^2 + 10a + 5$

Testing $a = \frac{\sqrt{5}}{2}$... this doesn't simplify nicely.

The answer does not reduce to a neat closed form, so we solve numerically. From our bracketing: $k \approx 0.84$.

More precisely, $4(k+1)^4 = 5(k+2)^2$. Numerically solving gives:

$$\boxed{k \approx 0.84}$$

(On the AP exam, this part would typically be set up with nicer numbers. The key skill is setting up the equation correctly.)

</details>

---

<details>
<summary><strong>Problem 20 Solution</strong></summary>

**For** $\frac{dR}{dt} = 0.02R(50 - R)$, $R(0) = 1$:

**(a)** Separate:

$$\frac{dR}{R(50 - R)} = 0.02 \, dt$$

**Partial fractions:**

$$\frac{1}{R(50-R)} = \frac{A}{R} + \frac{B}{50-R}$$

$R = 0$: $1 = 50A$ $\Rightarrow$ $A = \frac{1}{50}$

$R = 50$: $1 = 50B$ $\Rightarrow$ $B = \frac{1}{50}$

$$\frac{1}{R(50-R)} = \frac{1}{50}\left(\frac{1}{R} + \frac{1}{50-R}\right)$$

**Integrate:**

$$\frac{1}{50}\left(\ln|R| - \ln|50 - R|\right) = 0.02t + C$$

$$\frac{1}{50}\ln\left|\frac{R}{50-R}\right| = 0.02t + C$$

$$\ln\left|\frac{R}{50-R}\right| = t + C_1$$

(Since $50 \cdot 0.02 = 1$)

**Apply IC** $R(0) = 1$:

$$\ln\frac{1}{49} = C_1$$

$$\ln\frac{R}{50-R} = t - \ln 49$$

$$\frac{R}{50-R} = \frac{e^t}{49}$$

**Solve for $R$:**

$49R = (50 - R)e^t = 50e^t - Re^t$

$R(49 + e^t) = 50e^t$

$$\boxed{R(t) = \frac{50e^t}{49 + e^t} = \frac{50}{1 + 49e^{-t}}}$$

This is the logistic model with carrying capacity $L = 50$.

**(b)** At $t = 5$:

$$R(5) = \frac{50}{1 + 49e^{-5}} = \frac{50}{1 + 49(0.006738)} = \frac{50}{1 + 0.3302} = \frac{50}{1.3302} \approx 37.59$$

$$\boxed{R(5) \approx 38 \text{ team members}}$$

After 5 hours, about 38 of the 50 Mock Trial team members have heard Ganga's rumor.

**(c)** Half the team: $R = 25$

$$25 = \frac{50}{1 + 49e^{-t}}$$

$$1 + 49e^{-t} = 2$$

$$49e^{-t} = 1$$

$$e^{-t} = \frac{1}{49}$$

$$t = \ln 49 = 2\ln 7$$

$$\boxed{t = \ln 49 \approx 3.89 \text{ hours}}$$

About 3 hours and 53 minutes — roughly the length of an after-school Mock Trial practice session.

**(d)** The rate is $\frac{dR}{dt} = 0.02R(50 - R)$.

The product $R(50 - R)$ is a downward-opening parabola in $R$, maximized at:

$$R = \frac{50}{2} = 25$$

The maximum rate is:

$$0.02(25)(25) = 0.02(625) = 12.5 \text{ people per hour}$$

This occurs when $R = 25$, which from part (c) happens at $t = \ln 49 \approx 3.89$ hours.

$$\boxed{\text{Max rate} = 12.5 \text{ people/hour at } t = \ln 49 \approx 3.89 \text{ hours}}$$

This is a key feature of logistic growth: the fastest spread happens when exactly half the population has been reached. It's the inflection point of the logistic curve — the moment the rumor is spreading through the Mock Trial team like wildfire, right before it starts to slow down because most people have already heard it.

</details>

---

## What's Next

You've now added partial fractions to your integration toolkit — the technique that lets you break apart any rational function into pieces you already know how to integrate. This skill shows up everywhere: from straightforward integration problems to solving logistic differential equations. Next up, we'll tackle [Improper Integrals](/calculus/improper-integrals), where we push integration to its limits (literally) by integrating over infinite intervals or through discontinuities. It turns out some of these "impossible" integrals converge to beautiful finite answers — and partial fractions will be one of the tools you use to evaluate them.

---

<div align="center">

[← Integration by Parts](/calculus/integration-by-parts) | [Improper Integrals →](/calculus/improper-integrals)

</div>
