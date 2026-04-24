# Integration by Parts
<p class="article-date">April 23, 2026</p>

*You know how the product rule lets you differentiate two functions multiplied together? Well, integration by parts is the product rule running in reverse. It's the technique you reach for when you see an integral like $\int x \cos x \, dx$ and think, "These two functions don't belong together — I wish I could peel them apart." That's exactly what integration by parts does. It peels a product apart, piece by piece, trading one integral for a (hopefully) simpler one. Think of it like splitting a Ding Tea order between you and a friend — one of you handles the boba, the other handles the tea, and together you've conquered the whole drink.*

---

## What You'll Learn
- Derive the integration by parts formula from the product rule
- Apply the LIATE rule to choose $u$ and $dv$ strategically
- Evaluate integrals like $\int x e^x \, dx$, $\int \ln x \, dx$, $\int x^2 \sin x \, dx$
- Use the tabular method for repeated integration by parts
- Handle "boomerang" integrals where the original integral cycles back (e.g., $\int e^x \sin x \, dx$)
- Apply integration by parts to definite integrals
- Recognize when integration by parts is the right technique on the AP exam

---

## Prerequisites
- [Antiderivatives](/calculus/0601-antiderivatives)
- [Product Rule](/calculus/0305-product-rule)
- [Definite Integrals](/calculus/0603-definite-integrals)

---

## The Core Concept

### Intuition First

Remember the [product rule](/calculus/0305-product-rule)? It says:

$$\frac{d}{dx}[u \cdot v] = u'v + uv'$$

This tells us how to *differentiate* a product. But what if we flip the question around — what if we want to *integrate* a product?

Let's rearrange the product rule. Start with:

$$\frac{d}{dx}[uv] = u'v + uv'$$

Isolate $uv'$:

$$uv' = \frac{d}{dx}[uv] - u'v$$

Now integrate both sides with respect to $x$:

$$\int u \, v' \, dx = uv - \int v \, u' \, dx$$

Writing $v' \, dx = dv$ and $u' \, dx = du$, we get the classic formula.

### The Formula

$$\boxed{\int u \, dv = uv - \int v \, du}$$

In plain English: the integral of $u \, dv$ equals $u$ times $v$, minus the integral of $v \, du$.

The whole strategy is to choose $u$ and $dv$ so that the new integral $\int v \, du$ is **easier** than the original one. If you pick wisely, the problem simplifies. If you pick poorly, it gets worse. The art of integration by parts is all in the choosing.

### A Quick Analogy

Think of integration by parts like delegating tasks on the Robotics team. You have a complicated build (the original integral). You assign one part to a specialist ($u$, which gets differentiated and hopefully gets simpler) and the other part to the rest of the team ($dv$, which gets integrated). If you delegate well, the remaining work is manageable. If you hand the wrong task to the wrong person, you've created more chaos than you started with.

---

## The LIATE Rule — How to Choose $u$

The hardest part of integration by parts is deciding what to call $u$ and what to call $dv$. The **LIATE rule** gives you a priority order for choosing $u$:

| Priority | Type | Examples |
|----------|------|----------|
| 1st | **L** — Logarithmic | $\ln x$, $\log x$ |
| 2nd | **I** — Inverse trigonometric | $\arctan x$, $\arcsin x$ |
| 3rd | **A** — Algebraic (polynomials) | $x$, $x^2$, $3x + 1$ |
| 4th | **T** — Trigonometric | $\sin x$, $\cos x$ |
| 5th | **E** — Exponential | $e^x$, $2^x$ |

**Pick $u$ from whatever comes first in LIATE.** The function earlier in the list becomes $u$ (it gets differentiated), and everything else becomes $dv$ (it gets integrated).

**Why does LIATE work?**
- Logarithmic and inverse trig functions are hard to integrate but easy to differentiate — so make them $u$.
- Exponential functions are easy to integrate and don't simplify when differentiated — so they should be in $dv$.
- Polynomials get simpler when differentiated (lower degree each time) — so they usually become $u$ when paired with trig or exponential functions.

**Important:** LIATE is a guideline, not an absolute law. It works for the vast majority of AP-level problems, but occasionally you'll need to override it. When in doubt, ask yourself: "Does my choice of $u$ make $du$ simpler? Can I actually integrate $dv$?"

---

## Worked Examples

### Example 1: The Classic — $\int x e^x \, dx$

This is the "hello world" of integration by parts. We see a product of an algebraic function ($x$) and an exponential ($e^x$).

**LIATE check:** Algebraic (A) comes before Exponential (E), so $u = x$.

| | Choose | Compute |
|---|--------|---------|
| $u$ | $x$ | $du = dx$ |
| $dv$ | $e^x \, dx$ | $v = e^x$ |

**Apply the formula:**

$$\int x e^x \, dx = uv - \int v \, du = x e^x - \int e^x \, dx$$

$$= x e^x - e^x + C$$

$$\boxed{\int x e^x \, dx = e^x(x - 1) + C}$$

**Check:** Differentiate $e^x(x - 1)$: using the product rule, $e^x(x-1) + e^x(1) = e^x \cdot x - e^x + e^x = xe^x$. Correct!

---

### Example 2: Logarithms Love Being $u$ — $\int \ln x \, dx$

At first glance, this doesn't look like a product. But we can write it as $\int 1 \cdot \ln x \, dx$, treating the "1" as the other factor.

**LIATE check:** Logarithmic (L) comes first, so $u = \ln x$.

| | Choose | Compute |
|---|--------|---------|
| $u$ | $\ln x$ | $du = \frac{1}{x} \, dx$ |
| $dv$ | $dx$ | $v = x$ |

**Apply the formula:**

$$\int \ln x \, dx = x \ln x - \int x \cdot \frac{1}{x} \, dx$$

$$= x \ln x - \int 1 \, dx$$

$$= x \ln x - x + C$$

$$\boxed{\int \ln x \, dx = x \ln x - x + C}$$

This is one of those results worth memorizing. You'll see it pop up on the AP exam, and deriving it on the spot eats valuable time.

---

### Example 3: Trig and Algebra — $\int x \sin x \, dx$

Imagine Ganga is analyzing the displacement of an oscillating robot arm on the Robotics team. The velocity is $v(t) = t \sin t$, and she needs the position function — that means integrating $\int t \sin t \, dt$.

**LIATE check:** Algebraic (A) before Trigonometric (T), so $u = x$.

| | Choose | Compute |
|---|--------|---------|
| $u$ | $x$ | $du = dx$ |
| $dv$ | $\sin x \, dx$ | $v = -\cos x$ |

**Apply the formula:**

$$\int x \sin x \, dx = x(-\cos x) - \int (-\cos x) \, dx$$

$$= -x \cos x + \int \cos x \, dx$$

$$= -x \cos x + \sin x + C$$

$$\boxed{\int x \sin x \, dx = -x \cos x + \sin x + C}$$

---

### Example 4: Inverse Trig — $\int \arctan x \, dx$

Just like $\ln x$, the function $\arctan x$ doesn't look like a product — but we can pair it with $1$: $\int 1 \cdot \arctan x \, dx$.

**LIATE check:** Inverse trig (I) comes before everything else present, so $u = \arctan x$.

| | Choose | Compute |
|---|--------|---------|
| $u$ | $\arctan x$ | $du = \frac{1}{1 + x^2} \, dx$ |
| $dv$ | $dx$ | $v = x$ |

**Apply the formula:**

$$\int \arctan x \, dx = x \arctan x - \int \frac{x}{1 + x^2} \, dx$$

For the remaining integral, use the substitution $w = 1 + x^2$, $dw = 2x \, dx$:

$$\int \frac{x}{1 + x^2} \, dx = \frac{1}{2} \int \frac{dw}{w} = \frac{1}{2} \ln|1 + x^2| = \frac{1}{2} \ln(1 + x^2)$$

(We drop the absolute value because $1 + x^2 > 0$ always.)

$$\boxed{\int \arctan x \, dx = x \arctan x - \frac{1}{2}\ln(1 + x^2) + C}$$

---

### Example 5: Repeated IBP — $\int x^2 e^x \, dx$

Sometimes one round of integration by parts isn't enough. Here, $x^2$ needs to be differentiated twice before it vanishes.

**Round 1:**

| | Choose | Compute |
|---|--------|---------|
| $u$ | $x^2$ | $du = 2x \, dx$ |
| $dv$ | $e^x \, dx$ | $v = e^x$ |

$$\int x^2 e^x \, dx = x^2 e^x - \int 2x e^x \, dx$$

The remaining integral $\int 2x e^x \, dx$ is not yet trivial — it's $2 \int x e^x \, dx$, which we solved in Example 1.

**Round 2:**

$$\int 2x e^x \, dx = 2\left(xe^x - e^x\right) = 2xe^x - 2e^x$$

**Combine:**

$$\int x^2 e^x \, dx = x^2 e^x - (2xe^x - 2e^x) + C$$

$$= x^2 e^x - 2xe^x + 2e^x + C$$

$$\boxed{\int x^2 e^x \, dx = e^x(x^2 - 2x + 2) + C}$$

Notice the pattern: the coefficients are $1, -2, +2$. We'll see a much faster way to get this using the **tabular method** below.

---

### Example 6: The Boomerang — $\int e^x \sin x \, dx$

This is one of the coolest tricks in calculus. Neither $e^x$ nor $\sin x$ simplifies when you differentiate it — both just keep cycling. So integration by parts seems like it'll go on forever. But something magical happens.

**Round 1:** Let $u = \sin x$, $dv = e^x \, dx$:

$$\int e^x \sin x \, dx = e^x \sin x - \int e^x \cos x \, dx$$

**Round 2:** Apply IBP again to $\int e^x \cos x \, dx$. Let $u = \cos x$, $dv = e^x \, dx$:

$$\int e^x \cos x \, dx = e^x \cos x - \int e^x (-\sin x) \, dx = e^x \cos x + \int e^x \sin x \, dx$$

**Substitute back** into Round 1:

$$\int e^x \sin x \, dx = e^x \sin x - \left(e^x \cos x + \int e^x \sin x \, dx\right)$$

$$\int e^x \sin x \, dx = e^x \sin x - e^x \cos x - \int e^x \sin x \, dx$$

The original integral has **boomeranged** back! Call it $I$:

$$I = e^x \sin x - e^x \cos x - I$$

$$2I = e^x(\sin x - \cos x)$$

$$\boxed{\int e^x \sin x \, dx = \frac{e^x(\sin x - \cos x)}{2} + C}$$

**Why "boomerang"?** The integral comes back to you — like throwing a boomerang at Torrey Pines and having it circle right back into your hand. You didn't simplify it to zero; instead, you set up an equation and solved for it algebraically. This technique works whenever both functions cycle under differentiation (exponentials with trig).

---

### Example 7: The Boomerang's Twin — $\int e^x \cos x \, dx$

Let's do the companion integral. The process is identical.

**Round 1:** Let $u = \cos x$, $dv = e^x \, dx$:

$$\int e^x \cos x \, dx = e^x \cos x - \int e^x (-\sin x) \, dx = e^x \cos x + \int e^x \sin x \, dx$$

**Round 2:** Let $u = \sin x$, $dv = e^x \, dx$:

$$\int e^x \sin x \, dx = e^x \sin x - \int e^x \cos x \, dx$$

**Substitute back:**

$$\int e^x \cos x \, dx = e^x \cos x + e^x \sin x - \int e^x \cos x \, dx$$

Let $I = \int e^x \cos x \, dx$:

$$I = e^x \cos x + e^x \sin x - I$$

$$2I = e^x(\cos x + \sin x)$$

$$\boxed{\int e^x \cos x \, dx = \frac{e^x(\cos x + \sin x)}{2} + C}$$

---

### Example 8: IBP with Definite Integrals — $\int_1^e x \ln x \, dx$

When using integration by parts with definite integrals, the formula becomes:

$$\int_a^b u \, dv = \left[uv\right]_a^b - \int_a^b v \, du$$

**LIATE check:** Logarithmic (L) before Algebraic (A), so $u = \ln x$.

| | Choose | Compute |
|---|--------|---------|
| $u$ | $\ln x$ | $du = \frac{1}{x} \, dx$ |
| $dv$ | $x \, dx$ | $v = \frac{x^2}{2}$ |

**Apply the formula:**

$$\int_1^e x \ln x \, dx = \left[\frac{x^2}{2} \ln x\right]_1^e - \int_1^e \frac{x^2}{2} \cdot \frac{1}{x} \, dx$$

$$= \left[\frac{x^2}{2} \ln x\right]_1^e - \frac{1}{2}\int_1^e x \, dx$$

**Evaluate the boundary term:**

$$\left[\frac{x^2}{2} \ln x\right]_1^e = \frac{e^2}{2} \ln e - \frac{1}{2} \ln 1 = \frac{e^2}{2}(1) - \frac{1}{2}(0) = \frac{e^2}{2}$$

**Evaluate the remaining integral:**

$$\frac{1}{2}\int_1^e x \, dx = \frac{1}{2} \left[\frac{x^2}{2}\right]_1^e = \frac{1}{2} \cdot \frac{e^2 - 1}{2} = \frac{e^2 - 1}{4}$$

**Combine:**

$$\int_1^e x \ln x \, dx = \frac{e^2}{2} - \frac{e^2 - 1}{4} = \frac{2e^2}{4} - \frac{e^2 - 1}{4} = \frac{2e^2 - e^2 + 1}{4}$$

$$\boxed{\int_1^e x \ln x \, dx = \frac{e^2 + 1}{4}}$$

---

## The Tabular Method (Rapid-Fire IBP)

When you need to apply integration by parts **multiple times** — like when a polynomial is multiplied by $e^x$, $\sin x$, or $\cos x$ — the tabular method saves enormous time. Instead of writing out the full formula over and over, you organize everything into a table.

### How It Works

1. Put $u$ (the function you're differentiating repeatedly) in the left column.
2. Put $dv$ (the function you're integrating repeatedly) in the right column.
3. Differentiate down the left column until you reach $0$.
4. Integrate down the right column the same number of rows.
5. Draw diagonal arrows from left to right, alternating signs: $+, -, +, -, \ldots$
6. Multiply along each diagonal and add everything up.

### Example: $\int x^2 e^x \, dx$ via Tabular Method

| Sign | Derivatives of $u = x^2$ | Integrals of $dv = e^x \, dx$ |
|------|--------------------------|-------------------------------|
| $+$ | $x^2$ | $e^x$ |
| $-$ | $2x$ | $e^x$ |
| $+$ | $2$ | $e^x$ |
| | $0$ | |

Read off the diagonals (left entry times the right entry one row down, with alternating signs):

$$\int x^2 e^x \, dx = (+)(x^2)(e^x) + (-)(2x)(e^x) + (+)(2)(e^x) + C$$

$$= x^2 e^x - 2xe^x + 2e^x + C$$

$$\boxed{\int x^2 e^x \, dx = e^x(x^2 - 2x + 2) + C}$$

Same answer as Example 5 — but in about 30 seconds instead of two full pages of work!

### Example: $\int x^3 \cos x \, dx$ via Tabular Method

| Sign | Derivatives of $u = x^3$ | Integrals of $dv = \cos x \, dx$ |
|------|--------------------------|----------------------------------|
| $+$ | $x^3$ | $\sin x$ |
| $-$ | $3x^2$ | $-\cos x$ |
| $+$ | $6x$ | $-\sin x$ |
| $-$ | $6$ | $\cos x$ |
| | $0$ | |

$$\int x^3 \cos x \, dx = x^3 \sin x - 3x^2(-\cos x) + 6x(-\sin x) - 6(\cos x) + C$$

$$= x^3 \sin x + 3x^2 \cos x - 6x \sin x - 6 \cos x + C$$

$$\boxed{\int x^3 \cos x \, dx = x^3 \sin x + 3x^2 \cos x - 6x \sin x - 6\cos x + C}$$

Try doing that with four rounds of standard IBP — you'd be writing until the bell rings. The tabular method is a lifesaver on the AP exam when time is tight.

---

## Key Formulas & Rules

| Formula | When to Use |
|---------|-------------|
| $\int u \, dv = uv - \int v \, du$ | The core IBP formula |
| $\int_a^b u \, dv = [uv]_a^b - \int_a^b v \, du$ | IBP with definite integrals |
| **LIATE** priority: L-I-A-T-E | Choosing $u$ (pick from highest priority) |
| $\int \ln x \, dx = x\ln x - x + C$ | Memorize this result |
| $\int x e^x \, dx = e^x(x - 1) + C$ | Common IBP result |
| $\int x \sin x \, dx = -x\cos x + \sin x + C$ | Common IBP result |
| $\int x \cos x \, dx = x \sin x + \cos x + C$ | Common IBP result |
| $\int e^x \sin x \, dx = \frac{e^x(\sin x - \cos x)}{2} + C$ | Boomerang technique |
| $\int e^x \cos x \, dx = \frac{e^x(\sin x + \cos x)}{2} + C$ | Boomerang technique |
| $\int \arctan x \, dx = x\arctan x - \frac{1}{2}\ln(1+x^2) + C$ | Inverse trig IBP |

---

## Common Mistakes to Avoid

### Mistake 1: Choosing $u$ and $dv$ Backwards

**Wrong:** For $\int x e^x \, dx$, letting $u = e^x$ and $dv = x \, dx$:

$du = e^x \, dx$, $v = \frac{x^2}{2}$

$$\int x e^x \, dx = \frac{x^2}{2}e^x - \int \frac{x^2}{2} e^x \, dx$$

The new integral is **harder** — we went from $x$ to $x^2$. That's going backwards.

**Right:** Let $u = x$ (algebraic), $dv = e^x \, dx$ (exponential). LIATE tells you A comes before E.

---

### Mistake 2: Forgetting the Minus Sign

The formula is $uv \mathbf{-} \int v \, du$, not $uv + \int v \, du$. That minus sign is easy to drop, especially when you're juggling negative trig derivatives.

**Tip:** After each IBP step, double-check the sign in front of the remaining integral.

---

### Mistake 3: Switching Which Function Is $u$ Midway Through a Boomerang

In the boomerang technique ($\int e^x \sin x \, dx$), you must be **consistent** with your choice.

**Wrong:** Round 1: $u = \sin x$, $dv = e^x \, dx$. Round 2: $u = e^x$, $dv = \cos x \, dx$. This will undo your first step and you'll go in circles forever.

**Right:** In both rounds, keep the same type of function as $u$. If you start with $u = \text{trig}$, keep $u = \text{trig}$ in round 2.

---

### Mistake 4: Forgetting $+C$ in Indefinite Integrals

When you finish integration by parts, the result is still an indefinite integral. Don't forget $+C$.

**Wrong:** $\int x e^x \, dx = e^x(x - 1)$

**Right:** $\int x e^x \, dx = e^x(x - 1) + C$

---

### Mistake 5: Not Verifying by Differentiation

Integration by parts can involve many steps, and sign errors are common. The fastest way to check your answer is to differentiate it using the product rule and confirm you get back the original integrand. If you have 30 seconds at the end of a free response, this is the best use of that time.

---

## AP Exam Tips

### For BC Students:

1. **Integration by parts is BC-only.** It will not appear on the AB exam. But on the BC exam, it shows up almost every year — typically in one free response and 2-3 multiple choice questions.

2. **Memorize the common results.** The integrals of $\ln x$, $x e^x$, and $x \sin x$ come up so frequently that having them memorized saves precious time. You may still need to show work on a free response, but knowing the answer lets you verify quickly.

3. **Recognize when IBP is needed.** If you see a product of two different types of functions (especially polynomial $\times$ exponential, polynomial $\times$ trig, or anything involving $\ln x$ or $\arctan x$), think integration by parts.

4. **The tabular method is your friend on the MC section.** When a problem involves $x^2 \sin x$ or $x^3 e^x$, the tabular method gets you the answer in under a minute — critical when you have about 2 minutes per MC question.

5. **Watch for "evaluate $\int_0^1 \arctan x \, dx$" style problems.** These look intimidating but are straightforward IBP problems once you identify $u = \arctan x$ and $dv = dx$.

6. **Boomerang problems are worth 3-4 points on a free response.** The AP graders look for: (a) correct setup of IBP, (b) correct second application, (c) recognizing the original integral reappears, and (d) solving algebraically for the integral. Don't skip steps.

7. **When IBP is combined with other techniques,** you might need to use $u$-substitution after an IBP step (like in $\int \arctan x \, dx$ where the remaining integral requires a sub). Be flexible.

8. **On the calculator section,** you can verify IBP results numerically. If you find $\int_0^1 x e^x \, dx = 1$, punch it into the calculator to confirm.

---

## Practice Problems

### Basic (Problems 1-5)

**1.** Evaluate $\int x e^{2x} \, dx$.

---

**2.** Evaluate $\int x \cos x \, dx$.

---

**3.** Evaluate $\int \ln(3x) \, dx$.

---

**4.** Evaluate $\int x \cdot 2^x \, dx$.

---

**5.** Evaluate the definite integral $\int_0^1 x e^x \, dx$.

---

### Intermediate (Problems 6-10)

**6.** Evaluate $\int x^2 \sin x \, dx$.

---

**7.** Evaluate $\int e^{2x} \cos x \, dx$.

---

**8.** Evaluate $\int \arcsin x \, dx$.

---

**9.** Evaluate $\int_1^e (\ln x)^2 \, dx$.

---

**10.** Evaluate $\int x^2 e^{-x} \, dx$.

---

### Advanced (Problems 11-15)

**11.** Evaluate $\int x^3 e^{x^2} \, dx$. *(Hint: this requires substitution before IBP.)*

---

**12.** Evaluate $\int e^x \sin(2x) \, dx$ using the boomerang technique.

---

**13.** Evaluate $\int_0^{\pi} x^2 \cos x \, dx$.

---

**14.** Evaluate $\int \ln(x^2 + 1) \, dx$.

---

**15.** Evaluate $\int x \arctan x \, dx$.

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

$\int x e^{3x} \, dx =$

| Choice | Answer |
|--------|--------|
| **(A)** | $\frac{1}{3}xe^{3x} - \frac{1}{9}e^{3x} + C$ |
| **(B)** | $\frac{1}{3}xe^{3x} + \frac{1}{9}e^{3x} + C$ |
| **(C)** | $3xe^{3x} - 9e^{3x} + C$ |
| **(D)** | $xe^{3x} - e^{3x} + C$ |

---

#### Problem 17 (Multiple Choice)

$\int_0^1 \arctan x \, dx =$

| Choice | Answer |
|--------|--------|
| **(A)** | $\frac{\pi}{4} - \frac{1}{2}\ln 2$ |
| **(B)** | $\frac{\pi}{4} + \frac{1}{2}\ln 2$ |
| **(C)** | $\frac{\pi}{4} - \ln 2$ |
| **(D)** | $1 - \frac{\pi}{4}$ |

---

#### Problem 18 (Free Response)

Ganga is studying the flow rate of boba tea from a dispenser at Ding Tea. She models the rate at which tea fills a cup as $R(t) = te^{-0.5t}$ ounces per second, where $t$ is the time in seconds after the dispenser is turned on.

> **(a)** Find $\int te^{-0.5t} \, dt$.
>
> **(b)** How many ounces of tea are dispensed in the first 4 seconds?
>
> **(c)** Find the time $t > 0$ at which the flow rate is maximized.
>
> **(d)** As $t \to \infty$, what is the total amount of tea that would be dispensed? Interpret this result in context.

---

#### Problem 19 (Multiple Choice)

Using the tabular method, $\int x^2 \cos(2x) \, dx =$

| Choice | Answer |
|--------|--------|
| **(A)** | $\frac{x^2}{2}\sin(2x) + \frac{x}{2}\cos(2x) - \frac{1}{4}\sin(2x) + C$ |
| **(B)** | $\frac{x^2}{2}\sin(2x) + \frac{x}{4}\cos(2x) + \frac{1}{4}\sin(2x) + C$ |
| **(C)** | $\frac{x^2}{2}\sin(2x) + \frac{x}{2}\cos(2x) - \frac{1}{8}\sin(2x) + C$ |
| **(D)** | $\frac{x^2}{4}\sin(2x) + \frac{x}{4}\cos(2x) - \frac{1}{8}\sin(2x) + C$ |

---

#### Problem 20 (Free Response — Challenging)

Ganga is on a road trip with Dad down the I-5 from San Diego to LA, practicing her freeway driving. She's tracking the car's velocity, which she models as $v(t) = t^2 e^{-t/3}$ miles per minute for the first few minutes after merging onto the freeway (where $t = 0$ is the moment she enters the on-ramp).

> **(a)** Find the position function $s(t)$, given that $s(0) = 0$ (the car starts at the on-ramp). Use integration by parts (tabular method recommended).
>
> **(b)** Find the total distance traveled in the first 6 minutes.
>
> **(c)** Find the acceleration $a(t)$ and determine the time at which the car reaches its maximum velocity.
>
> **(d)** Explain why the model $v(t) = t^2 e^{-t/3}$ is not realistic for the entire drive to LA. What physical behavior does the model predict as $t \to \infty$?

---

## Answer Key

<details>
<summary><strong>Problem 1 Solution</strong></summary>

**Evaluate $\int x e^{2x} \, dx$.**

**LIATE:** $u = x$ (A), $dv = e^{2x} \, dx$ (E).

| | Choose | Compute |
|---|--------|---------|
| $u$ | $x$ | $du = dx$ |
| $dv$ | $e^{2x}\,dx$ | $v = \frac{1}{2}e^{2x}$ |

$$\int x e^{2x}\, dx = \frac{x}{2}e^{2x} - \int \frac{1}{2}e^{2x}\, dx$$

$$= \frac{x}{2}e^{2x} - \frac{1}{4}e^{2x} + C$$

$$\boxed{\int x e^{2x}\, dx = \frac{e^{2x}}{4}(2x - 1) + C}$$

</details>

---

<details>
<summary><strong>Problem 2 Solution</strong></summary>

**Evaluate $\int x \cos x \, dx$.**

**LIATE:** $u = x$ (A), $dv = \cos x \, dx$ (T).

| | Choose | Compute |
|---|--------|---------|
| $u$ | $x$ | $du = dx$ |
| $dv$ | $\cos x\,dx$ | $v = \sin x$ |

$$\int x \cos x \, dx = x \sin x - \int \sin x \, dx$$

$$= x \sin x - (-\cos x) + C$$

$$\boxed{\int x \cos x \, dx = x \sin x + \cos x + C}$$

</details>

---

<details>
<summary><strong>Problem 3 Solution</strong></summary>

**Evaluate $\int \ln(3x) \, dx$.**

**Method 1 — Direct IBP:**

Let $u = \ln(3x)$, $dv = dx$.

$du = \frac{1}{x}\,dx$ (since $\frac{d}{dx}\ln(3x) = \frac{3}{3x} = \frac{1}{x}$), $v = x$.

$$\int \ln(3x)\,dx = x\ln(3x) - \int x \cdot \frac{1}{x}\,dx$$

$$= x\ln(3x) - \int 1\,dx$$

$$= x\ln(3x) - x + C$$

$$\boxed{\int \ln(3x)\,dx = x\ln(3x) - x + C}$$

**Method 2 — Using log properties:**

$\ln(3x) = \ln 3 + \ln x$, so:

$$\int \ln(3x)\,dx = \int \ln 3\,dx + \int \ln x\,dx = x\ln 3 + (x\ln x - x) + C = x\ln(3x) - x + C$$

Same answer.

</details>

---

<details>
<summary><strong>Problem 4 Solution</strong></summary>

**Evaluate $\int x \cdot 2^x \, dx$.**

**LIATE:** $u = x$ (A), $dv = 2^x \, dx$ (E).

Recall that $\int 2^x \, dx = \frac{2^x}{\ln 2} + C$.

| | Choose | Compute |
|---|--------|---------|
| $u$ | $x$ | $du = dx$ |
| $dv$ | $2^x\,dx$ | $v = \frac{2^x}{\ln 2}$ |

$$\int x \cdot 2^x \, dx = \frac{x \cdot 2^x}{\ln 2} - \int \frac{2^x}{\ln 2}\,dx$$

$$= \frac{x \cdot 2^x}{\ln 2} - \frac{1}{\ln 2} \cdot \frac{2^x}{\ln 2} + C$$

$$= \frac{x \cdot 2^x}{\ln 2} - \frac{2^x}{(\ln 2)^2} + C$$

$$\boxed{\int x \cdot 2^x \, dx = \frac{2^x}{\ln 2}\left(x - \frac{1}{\ln 2}\right) + C}$$

</details>

---

<details>
<summary><strong>Problem 5 Solution</strong></summary>

**Evaluate $\int_0^1 x e^x \, dx$.**

From Example 1, we know $\int x e^x \, dx = e^x(x - 1) + C$.

$$\int_0^1 x e^x \, dx = \left[e^x(x - 1)\right]_0^1$$

$$= e^1(1 - 1) - e^0(0 - 1)$$

$$= e(0) - 1(-1)$$

$$= 0 + 1$$

$$\boxed{\int_0^1 x e^x \, dx = 1}$$

</details>

---

<details>
<summary><strong>Problem 6 Solution</strong></summary>

**Evaluate $\int x^2 \sin x \, dx$.**

Use the **tabular method** with $u = x^2$, $dv = \sin x \, dx$:

| Sign | Derivatives of $x^2$ | Integrals of $\sin x$ |
|------|----------------------|----------------------|
| $+$ | $x^2$ | $-\cos x$ |
| $-$ | $2x$ | $-\sin x$ |
| $+$ | $2$ | $\cos x$ |
| | $0$ | |

Read diagonals (left entry times the right entry one row below, with alternating signs):

$$\int x^2 \sin x \, dx = (+)(x^2)(-\cos x) + (-)(2x)(-\sin x) + (+)(2)(\cos x) + C$$

$$= -x^2 \cos x + 2x \sin x + 2\cos x + C$$

$$\boxed{\int x^2 \sin x \, dx = -x^2 \cos x + 2x \sin x + 2\cos x + C}$$

**Verify:** Differentiate $-x^2 \cos x + 2x \sin x + 2\cos x$:

$= -2x\cos x + x^2 \sin x + 2\sin x + 2x\cos x - 2\sin x = x^2 \sin x$ ✓

</details>

---

<details>
<summary><strong>Problem 7 Solution</strong></summary>

**Evaluate $\int e^{2x} \cos x \, dx$.**

This is a **boomerang** integral. Let $I = \int e^{2x} \cos x \, dx$.

**Round 1:** $u = \cos x$, $dv = e^{2x}\,dx$:

$du = -\sin x\,dx$, $v = \frac{1}{2}e^{2x}$

$$I = \frac{1}{2}e^{2x}\cos x - \int \frac{1}{2}e^{2x}(-\sin x)\,dx = \frac{1}{2}e^{2x}\cos x + \frac{1}{2}\int e^{2x}\sin x\,dx$$

**Round 2:** Apply IBP to $\int e^{2x}\sin x\,dx$. Let $u = \sin x$, $dv = e^{2x}\,dx$:

$du = \cos x\,dx$, $v = \frac{1}{2}e^{2x}$

$$\int e^{2x}\sin x\,dx = \frac{1}{2}e^{2x}\sin x - \int \frac{1}{2}e^{2x}\cos x\,dx = \frac{1}{2}e^{2x}\sin x - \frac{1}{2}I$$

**Substitute back:**

$$I = \frac{1}{2}e^{2x}\cos x + \frac{1}{2}\left(\frac{1}{2}e^{2x}\sin x - \frac{1}{2}I\right)$$

$$I = \frac{1}{2}e^{2x}\cos x + \frac{1}{4}e^{2x}\sin x - \frac{1}{4}I$$

$$I + \frac{1}{4}I = \frac{1}{2}e^{2x}\cos x + \frac{1}{4}e^{2x}\sin x$$

$$\frac{5}{4}I = \frac{e^{2x}}{4}(2\cos x + \sin x)$$

$$I = \frac{e^{2x}(2\cos x + \sin x)}{5}$$

$$\boxed{\int e^{2x}\cos x\,dx = \frac{e^{2x}(2\cos x + \sin x)}{5} + C}$$

</details>

---

<details>
<summary><strong>Problem 8 Solution</strong></summary>

**Evaluate $\int \arcsin x \, dx$.**

Write as $\int 1 \cdot \arcsin x \, dx$.

**LIATE:** Inverse trig (I) first, so $u = \arcsin x$, $dv = dx$.

| | Choose | Compute |
|---|--------|---------|
| $u$ | $\arcsin x$ | $du = \frac{1}{\sqrt{1 - x^2}}\,dx$ |
| $dv$ | $dx$ | $v = x$ |

$$\int \arcsin x\,dx = x\arcsin x - \int \frac{x}{\sqrt{1 - x^2}}\,dx$$

For the remaining integral, use substitution: $w = 1 - x^2$, $dw = -2x\,dx$, so $x\,dx = -\frac{1}{2}\,dw$:

$$\int \frac{x}{\sqrt{1-x^2}}\,dx = -\frac{1}{2}\int \frac{dw}{\sqrt{w}} = -\frac{1}{2} \cdot 2\sqrt{w} = -\sqrt{1 - x^2}$$

Therefore:

$$\int \arcsin x\,dx = x\arcsin x - (-\sqrt{1 - x^2}) + C$$

$$\boxed{\int \arcsin x\,dx = x\arcsin x + \sqrt{1 - x^2} + C}$$

</details>

---

<details>
<summary><strong>Problem 9 Solution</strong></summary>

**Evaluate $\int_1^e (\ln x)^2 \, dx$.**

Let $u = (\ln x)^2$, $dv = dx$.

$du = 2\ln x \cdot \frac{1}{x}\,dx = \frac{2\ln x}{x}\,dx$, $v = x$

$$\int_1^e (\ln x)^2\,dx = \left[x(\ln x)^2\right]_1^e - \int_1^e x \cdot \frac{2\ln x}{x}\,dx$$

$$= \left[x(\ln x)^2\right]_1^e - 2\int_1^e \ln x\,dx$$

**Evaluate the boundary term:**

$\left[x(\ln x)^2\right]_1^e = e(\ln e)^2 - 1(\ln 1)^2 = e(1)^2 - 1(0)^2 = e$

**Evaluate $\int_1^e \ln x\,dx$:**

We know $\int \ln x\,dx = x\ln x - x + C$, so:

$$\int_1^e \ln x\,dx = \left[x\ln x - x\right]_1^e = (e \cdot 1 - e) - (1 \cdot 0 - 1) = 0 - (-1) = 1$$

**Combine:**

$$\int_1^e (\ln x)^2\,dx = e - 2(1) = e - 2$$

$$\boxed{\int_1^e (\ln x)^2\,dx = e - 2 \approx 0.718}$$

</details>

---

<details>
<summary><strong>Problem 10 Solution</strong></summary>

**Evaluate $\int x^2 e^{-x} \, dx$.**

Use the **tabular method** with $u = x^2$, $dv = e^{-x}\,dx$:

| Sign | Derivatives of $x^2$ | Integrals of $e^{-x}$ |
|------|----------------------|----------------------|
| $+$ | $x^2$ | $-e^{-x}$ |
| $-$ | $2x$ | $e^{-x}$ |
| $+$ | $2$ | $-e^{-x}$ |
| | $0$ | |

$$\int x^2 e^{-x}\,dx = (+)(x^2)(-e^{-x}) + (-)(2x)(e^{-x}) + (+)(2)(-e^{-x}) + C$$

$$= -x^2 e^{-x} - 2x e^{-x} - 2e^{-x} + C$$

$$\boxed{\int x^2 e^{-x}\,dx = -e^{-x}(x^2 + 2x + 2) + C}$$

</details>

---

<details>
<summary><strong>Problem 11 Solution</strong></summary>

**Evaluate $\int x^3 e^{x^2} \, dx$.**

**Key insight:** This doesn't fit standard IBP directly. We need **substitution first**.

Rewrite: $\int x^3 e^{x^2}\,dx = \int x^2 \cdot x e^{x^2}\,dx$

Let $w = x^2$, so $dw = 2x\,dx$, meaning $x\,dx = \frac{1}{2}\,dw$. Also $x^2 = w$.

$$\int x^2 \cdot xe^{x^2}\,dx = \int w \cdot e^w \cdot \frac{1}{2}\,dw = \frac{1}{2}\int we^w\,dw$$

Now apply IBP: $u = w$, $dv = e^w\,dw$:

$$\frac{1}{2}\int we^w\,dw = \frac{1}{2}\left(we^w - \int e^w\,dw\right) = \frac{1}{2}\left(we^w - e^w\right) + C$$

$$= \frac{1}{2}e^w(w - 1) + C$$

Substitute back $w = x^2$:

$$\boxed{\int x^3 e^{x^2}\,dx = \frac{1}{2}e^{x^2}(x^2 - 1) + C}$$

</details>

---

<details>
<summary><strong>Problem 12 Solution</strong></summary>

**Evaluate $\int e^x \sin(2x) \, dx$.**

Let $I = \int e^x \sin(2x)\,dx$.

**Round 1:** $u = \sin(2x)$, $dv = e^x\,dx$:

$du = 2\cos(2x)\,dx$, $v = e^x$

$$I = e^x\sin(2x) - \int 2e^x\cos(2x)\,dx = e^x\sin(2x) - 2\int e^x\cos(2x)\,dx$$

**Round 2:** Apply IBP to $\int e^x\cos(2x)\,dx$. Let $u = \cos(2x)$, $dv = e^x\,dx$:

$du = -2\sin(2x)\,dx$, $v = e^x$

$$\int e^x\cos(2x)\,dx = e^x\cos(2x) - \int e^x(-2\sin(2x))\,dx = e^x\cos(2x) + 2\int e^x\sin(2x)\,dx$$

$$= e^x\cos(2x) + 2I$$

**Substitute back into Round 1:**

$$I = e^x\sin(2x) - 2\left(e^x\cos(2x) + 2I\right)$$

$$I = e^x\sin(2x) - 2e^x\cos(2x) - 4I$$

$$5I = e^x\sin(2x) - 2e^x\cos(2x)$$

$$I = \frac{e^x(\sin(2x) - 2\cos(2x))}{5}$$

$$\boxed{\int e^x\sin(2x)\,dx = \frac{e^x(\sin(2x) - 2\cos(2x))}{5} + C}$$

</details>

---

<details>
<summary><strong>Problem 13 Solution</strong></summary>

**Evaluate $\int_0^{\pi} x^2 \cos x \, dx$.**

Use the **tabular method** with $u = x^2$, $dv = \cos x\,dx$:

| Sign | Derivatives of $x^2$ | Integrals of $\cos x$ |
|------|----------------------|----------------------|
| $+$ | $x^2$ | $\sin x$ |
| $-$ | $2x$ | $-\cos x$ |
| $+$ | $2$ | $-\sin x$ |
| | $0$ | |

$$\int x^2\cos x\,dx = x^2\sin x - 2x(-\cos x) + 2(-\sin x) + C$$

$$= x^2\sin x + 2x\cos x - 2\sin x + C$$

**Evaluate from $0$ to $\pi$:**

$$\int_0^{\pi} x^2\cos x\,dx = \left[x^2\sin x + 2x\cos x - 2\sin x\right]_0^{\pi}$$

At $x = \pi$:

$$\pi^2\sin\pi + 2\pi\cos\pi - 2\sin\pi = \pi^2(0) + 2\pi(-1) - 2(0) = -2\pi$$

At $x = 0$:

$$0 + 0 - 0 = 0$$

$$\boxed{\int_0^{\pi} x^2\cos x\,dx = -2\pi}$$

</details>

---

<details>
<summary><strong>Problem 14 Solution</strong></summary>

**Evaluate $\int \ln(x^2 + 1) \, dx$.**

Let $u = \ln(x^2 + 1)$, $dv = dx$.

$du = \frac{2x}{x^2 + 1}\,dx$, $v = x$

$$\int \ln(x^2+1)\,dx = x\ln(x^2+1) - \int \frac{2x^2}{x^2+1}\,dx$$

For the remaining integral, rewrite the fraction:

$$\frac{2x^2}{x^2+1} = \frac{2(x^2+1) - 2}{x^2+1} = 2 - \frac{2}{x^2+1}$$

So:

$$\int \frac{2x^2}{x^2+1}\,dx = \int \left(2 - \frac{2}{x^2+1}\right)\,dx = 2x - 2\arctan x$$

**Combine:**

$$\int \ln(x^2+1)\,dx = x\ln(x^2+1) - (2x - 2\arctan x) + C$$

$$\boxed{\int \ln(x^2+1)\,dx = x\ln(x^2+1) - 2x + 2\arctan x + C}$$

</details>

---

<details>
<summary><strong>Problem 15 Solution</strong></summary>

**Evaluate $\int x \arctan x \, dx$.**

**LIATE:** Inverse trig (I) before Algebraic (A), so $u = \arctan x$, $dv = x\,dx$.

| | Choose | Compute |
|---|--------|---------|
| $u$ | $\arctan x$ | $du = \frac{1}{1+x^2}\,dx$ |
| $dv$ | $x\,dx$ | $v = \frac{x^2}{2}$ |

$$\int x\arctan x\,dx = \frac{x^2}{2}\arctan x - \int \frac{x^2}{2} \cdot \frac{1}{1+x^2}\,dx$$

$$= \frac{x^2}{2}\arctan x - \frac{1}{2}\int \frac{x^2}{1+x^2}\,dx$$

Rewrite the fraction:

$$\frac{x^2}{1+x^2} = \frac{(1+x^2) - 1}{1+x^2} = 1 - \frac{1}{1+x^2}$$

$$\frac{1}{2}\int \frac{x^2}{1+x^2}\,dx = \frac{1}{2}\int\left(1 - \frac{1}{1+x^2}\right)\,dx = \frac{1}{2}\left(x - \arctan x\right)$$

**Combine:**

$$\int x\arctan x\,dx = \frac{x^2}{2}\arctan x - \frac{1}{2}x + \frac{1}{2}\arctan x + C$$

$$\boxed{\int x\arctan x\,dx = \frac{x^2 + 1}{2}\arctan x - \frac{x}{2} + C}$$

</details>

---

<details>
<summary><strong>Problem 16 Solution</strong></summary>

**Answer: (A)** $\frac{1}{3}xe^{3x} - \frac{1}{9}e^{3x} + C$

Let $u = x$, $dv = e^{3x}\,dx$. Then $du = dx$, $v = \frac{1}{3}e^{3x}$.

$$\int xe^{3x}\,dx = \frac{x}{3}e^{3x} - \int \frac{1}{3}e^{3x}\,dx = \frac{x}{3}e^{3x} - \frac{1}{9}e^{3x} + C$$

$$= \frac{e^{3x}}{9}(3x - 1) + C$$

This matches **(A)**.

</details>

---

<details>
<summary><strong>Problem 17 Solution</strong></summary>

**Answer: (A)** $\frac{\pi}{4} - \frac{1}{2}\ln 2$

From Example 4, we know $\int \arctan x\,dx = x\arctan x - \frac{1}{2}\ln(1+x^2) + C$.

$$\int_0^1 \arctan x\,dx = \left[x\arctan x - \frac{1}{2}\ln(1+x^2)\right]_0^1$$

At $x = 1$:

$$1 \cdot \arctan(1) - \frac{1}{2}\ln(1+1) = \frac{\pi}{4} - \frac{1}{2}\ln 2$$

At $x = 0$:

$$0 \cdot \arctan(0) - \frac{1}{2}\ln(1) = 0 - 0 = 0$$

$$\int_0^1 \arctan x\,dx = \frac{\pi}{4} - \frac{1}{2}\ln 2$$

This matches **(A)**.

</details>

---

<details>
<summary><strong>Problem 18 Solution</strong></summary>

**(a)** Find $\int te^{-0.5t}\,dt$.

Let $u = t$, $dv = e^{-0.5t}\,dt$.

$du = dt$, $v = \frac{e^{-0.5t}}{-0.5} = -2e^{-0.5t}$

$$\int te^{-0.5t}\,dt = t(-2e^{-0.5t}) - \int (-2e^{-0.5t})\,dt$$

$$= -2te^{-0.5t} + 2\int e^{-0.5t}\,dt$$

$$= -2te^{-0.5t} + 2(-2e^{-0.5t}) + C$$

$$\boxed{\int te^{-0.5t}\,dt = -2e^{-0.5t}(t + 2) + C}$$

**(b)** Total tea dispensed in the first 4 seconds:

$$\int_0^4 te^{-0.5t}\,dt = \left[-2e^{-0.5t}(t+2)\right]_0^4$$

At $t = 4$: $-2e^{-2}(4+2) = -12e^{-2} = -12(0.13534) \approx -1.624$

At $t = 0$: $-2e^{0}(0+2) = -4$

$$\int_0^4 te^{-0.5t}\,dt = -1.624 - (-4) = 2.376$$

$$\boxed{\approx 2.376 \text{ ounces}}$$

**(c)** The flow rate is $R(t) = te^{-0.5t}$.

$R'(t) = e^{-0.5t} + t(-0.5)e^{-0.5t} = e^{-0.5t}(1 - 0.5t)$

Set $R'(t) = 0$: since $e^{-0.5t} > 0$ always, we need $1 - 0.5t = 0$, so $t = 2$.

Check: $R'(t) > 0$ for $t < 2$ and $R'(t) < 0$ for $t > 2$, confirming a maximum.

$$\boxed{t = 2 \text{ seconds}}$$

The flow rate is maximized at $t = 2$ seconds, with $R(2) = 2e^{-1} \approx 0.736$ oz/sec.

**(d)** As $t \to \infty$:

$$\int_0^{\infty} te^{-0.5t}\,dt = \lim_{b \to \infty}\left[-2e^{-0.5t}(t+2)\right]_0^b$$

As $b \to \infty$: $-2e^{-0.5b}(b+2) \to 0$ (exponential decay dominates the linear growth).

$$= 0 - (-4) = 4$$

$$\boxed{\text{Total tea dispensed} = 4 \text{ ounces}}$$

**Interpretation:** If the dispenser ran forever, it would dispense a total of 4 ounces. This makes physical sense — the flow rate starts at 0, peaks at $t = 2$, then decays exponentially, so the dispenser slows to a trickle and the total converges.

</details>

---

<details>
<summary><strong>Problem 19 Solution</strong></summary>

**Answer: (A)** $\frac{x^2}{2}\sin(2x) + \frac{x}{2}\cos(2x) - \frac{1}{4}\sin(2x) + C$

Use the **tabular method** with $u = x^2$, $dv = \cos(2x)\,dx$:

| Sign | Derivatives of $x^2$ | Integrals of $\cos(2x)$ |
|------|----------------------|-------------------------|
| $+$ | $x^2$ | $\frac{1}{2}\sin(2x)$ |
| $-$ | $2x$ | $-\frac{1}{4}\cos(2x)$ |
| $+$ | $2$ | $-\frac{1}{8}\sin(2x)$ |
| | $0$ | |

$$\int x^2\cos(2x)\,dx = (+)(x^2)\left(\frac{1}{2}\sin(2x)\right) + (-)(2x)\left(-\frac{1}{4}\cos(2x)\right) + (+)(2)\left(-\frac{1}{8}\sin(2x)\right) + C$$

$$= \frac{x^2}{2}\sin(2x) + \frac{2x}{4}\cos(2x) - \frac{2}{8}\sin(2x) + C$$

$$= \frac{x^2}{2}\sin(2x) + \frac{x}{2}\cos(2x) - \frac{1}{4}\sin(2x) + C$$

This matches **(A)**.

</details>

---

<details>
<summary><strong>Problem 20 Solution</strong></summary>

**(a)** Find $s(t) = \int t^2 e^{-t/3}\,dt$ with $s(0) = 0$.

Use the **tabular method** with $u = t^2$, $dv = e^{-t/3}\,dt$:

| Sign | Derivatives of $t^2$ | Integrals of $e^{-t/3}$ |
|------|----------------------|------------------------|
| $+$ | $t^2$ | $-3e^{-t/3}$ |
| $-$ | $2t$ | $9e^{-t/3}$ |
| $+$ | $2$ | $-27e^{-t/3}$ |
| | $0$ | |

$$\int t^2 e^{-t/3}\,dt = (+)(t^2)(-3e^{-t/3}) + (-)(2t)(9e^{-t/3}) + (+)(2)(-27e^{-t/3}) + C$$

$$= -3t^2 e^{-t/3} - 18t e^{-t/3} - 54e^{-t/3} + C$$

$$= -3e^{-t/3}(t^2 + 6t + 18) + C$$

Apply $s(0) = 0$:

$$0 = -3e^{0}(0 + 0 + 18) + C = -54 + C$$

$$C = 54$$

$$\boxed{s(t) = -3e^{-t/3}(t^2 + 6t + 18) + 54}$$

**(b)** Total distance in first 6 minutes.

Since $v(t) = t^2 e^{-t/3} \geq 0$ for all $t \geq 0$, the total distance equals the displacement:

$$s(6) = -3e^{-2}(36 + 36 + 18) + 54 = -3e^{-2}(90) + 54$$

$$= -270e^{-2} + 54 = -270(0.13534) + 54$$

$$= -36.54 + 54$$

$$\boxed{s(6) \approx 17.46 \text{ miles}}$$

**(c)** Acceleration:

$$a(t) = v'(t) = \frac{d}{dt}\left[t^2 e^{-t/3}\right]$$

Using the product rule:

$$a(t) = 2te^{-t/3} + t^2\left(-\frac{1}{3}\right)e^{-t/3} = e^{-t/3}\left(2t - \frac{t^2}{3}\right) = \frac{te^{-t/3}}{3}(6 - t)$$

Set $a(t) = 0$: since $e^{-t/3} > 0$, we need $t(6-t) = 0$, giving $t = 0$ or $t = 6$.

For $0 < t < 6$: $a(t) > 0$ (velocity increasing). For $t > 6$: $a(t) < 0$ (velocity decreasing).

$$\boxed{v \text{ is maximized at } t = 6 \text{ minutes}}$$

At this time, $v(6) = 36e^{-2} \approx 4.87$ miles per minute $\approx 292$ mph. (Not realistic — see part (d)!)

**(d)** As $t \to \infty$:

$$v(t) = t^2 e^{-t/3} \to 0$$

The model predicts the car's velocity eventually approaches zero — the car slows to a stop. This is unrealistic for highway driving because:

- Real highway velocity stabilizes at a cruising speed (e.g., 65 mph), rather than decaying to zero.
- The model also predicts an unrealistically high peak velocity of about 292 mph at $t = 6$ minutes.
- The model only makes sense for the initial acceleration phase (first few minutes) where the car speeds up from the on-ramp and then adjusts to traffic flow. A constant velocity model would be more appropriate for the sustained freeway portion of the San Diego to LA drive.

</details>

---

## What's Next

You've just learned one of the most powerful integration techniques in the BC toolkit. Integration by parts lets you tackle products of functions that no substitution could handle — and the tabular method makes repeated applications nearly effortless. Combined with the boomerang trick, you're now equipped to handle exponential-trig integrals that once seemed impossible.

Next up: [Partial Fractions](/calculus/partial-fractions), where you'll learn how to break apart complicated rational functions into simpler pieces that are easy to integrate — like splitting a complicated Panda Express plate into individual entrees that you can enjoy one at a time.

---

<div align="center">

[← Exponential Growth & Decay](/calculus/exponential-growth-decay) | [Partial Fractions →](/calculus/partial-fractions)

</div>
