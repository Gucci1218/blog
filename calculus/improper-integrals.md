# Improper Integrals
<p class="article-date">April 23, 2026</p>

*Imagine standing at Coronado Beach, staring south along the coastline stretching toward Mexico. The sand seems to go on forever. Now picture this: you start laying down a strip of sand one foot wide along that infinite shoreline, but the strip gets thinner and thinner the further you go. Could the total area of sand in that strip actually be finite — even though the beach never ends? That's the wild idea behind improper integrals. Sometimes, adding up infinitely many things gives you a perfectly finite answer. Sometimes it doesn't. Learning to tell the difference is one of the most elegant skills in all of calculus.*

---

## What You'll Learn
- Recognize when an integral is "improper" (infinite limits or discontinuous integrands)
- Evaluate Type 1 improper integrals (infinite limits of integration)
- Evaluate Type 2 improper integrals (discontinuous integrands)
- Determine whether an improper integral converges or diverges
- Apply the p-integral test: $\int_1^\infty \frac{1}{x^p}\,dx$ converges if and only if $p > 1$
- Use the Direct Comparison Test for improper integrals
- Use the Limit Comparison Test for improper integrals
- Understand Gabriel's Horn (finite volume, infinite surface area)
- Connect improper integrals to series (preview of the Integral Test)

---

## Prerequisites
- [Definite Integrals](/calculus/0603-definite-integrals)
- [Fundamental Theorem of Calculus](/calculus/0604-fundamental-theorem)
- [Limits at Infinity](/calculus/0207-limits-at-infinity)

---

## The Core Concept

### Intuition First

Think about your Starbucks Rewards balance. Every week you earn some stars, but suppose each week you earn *fewer* stars than the week before — maybe half as many. Week 1: 100 stars. Week 2: 50. Week 3: 25. Week 4: 12.5. And so on, forever.

Even though you're earning stars for all eternity, your total balance approaches a limit: 200 stars. It never reaches 201. Adding infinitely many shrinking quantities can produce a finite total. That's **convergence**.

Now imagine a different rewards program where you earn 1 star the first week, $\frac{1}{2}$ the second, $\frac{1}{3}$ the third, $\frac{1}{4}$ the fourth... This also shrinks toward zero, but the total grows without bound — it's the harmonic series, and it **diverges**.

Improper integrals are the continuous version of this idea. Instead of adding up discrete terms, we're computing area under a curve that either:

1. **Stretches to infinity** (the interval is unbounded), or
2. **Shoots to infinity** (the function has a vertical asymptote inside the interval)

In both cases, the standard definite integral $\int_a^b f(x)\,dx$ breaks down because something is infinite. We fix it with limits.

### The Formal Definition

**Type 1: Infinite Limits of Integration**

If $f$ is continuous on $[a, \infty)$:

$$\int_a^\infty f(x)\,dx = \lim_{b \to \infty} \int_a^b f(x)\,dx$$

If this limit exists and is finite, the integral **converges**. Otherwise, it **diverges**.

Similarly:

$$\int_{-\infty}^b f(x)\,dx = \lim_{a \to -\infty} \int_a^b f(x)\,dx$$

For a doubly-infinite integral, split at any point $c$:

$$\int_{-\infty}^{\infty} f(x)\,dx = \int_{-\infty}^{c} f(x)\,dx + \int_{c}^{\infty} f(x)\,dx$$

Both pieces must converge independently. If either one diverges, the whole integral diverges.

**Type 2: Discontinuous Integrand**

If $f$ is continuous on $[a, b)$ but has a vertical asymptote at $x = b$:

$$\int_a^b f(x)\,dx = \lim_{t \to b^-} \int_a^t f(x)\,dx$$

If $f$ has a vertical asymptote at $x = a$:

$$\int_a^b f(x)\,dx = \lim_{t \to a^+} \int_t^b f(x)\,dx$$

If $f$ has a vertical asymptote at some interior point $x = c$ where $a < c < b$, split:

$$\int_a^b f(x)\,dx = \int_a^c f(x)\,dx + \int_c^b f(x)\,dx$$

Again, both pieces must converge.

### Why "Improper"?

The word "improper" just means the integral doesn't fit the standard definition — either the interval is infinite or the function blows up somewhere. It doesn't mean the integral is wrong or bad. It means we need to be more careful, using limits to handle the infinity.

---

## The p-Integral: Your Most Important Tool

Before diving into examples, let's establish the single most important result for improper integrals.

**The p-Integral Test:**

$$\int_1^\infty \frac{1}{x^p}\,dx \quad \begin{cases} \text{converges to } \frac{1}{p-1} & \text{if } p > 1 \\[6pt] \text{diverges} & \text{if } p \leq 1 \end{cases}$$

**Proof for $p > 1$:**

$$\int_1^\infty \frac{1}{x^p}\,dx = \lim_{b \to \infty} \int_1^b x^{-p}\,dx = \lim_{b \to \infty} \left[\frac{x^{-p+1}}{-p+1}\right]_1^b = \lim_{b \to \infty} \frac{1}{1-p}\left(b^{1-p} - 1\right)$$

Since $p > 1$, we have $1 - p < 0$, so $b^{1-p} \to 0$ as $b \to \infty$:

$$= \frac{1}{1-p}(0 - 1) = \frac{1}{p-1}$$

$$\boxed{\int_1^\infty \frac{1}{x^p}\,dx = \frac{1}{p-1} \quad \text{for } p > 1}$$

**For $p = 1$:** $\int_1^\infty \frac{1}{x}\,dx = \lim_{b \to \infty} \ln b = \infty$ — **diverges**.

**For $p < 1$:** $b^{1-p} \to \infty$ — **diverges**.

Think of it this way: $\frac{1}{x}$ decays "just barely" too slowly for the area to be finite. Anything that decays faster (like $\frac{1}{x^2}$, $\frac{1}{x^{1.001}}$) converges. Anything that decays as slowly or slower diverges.

It's like ordering boba at Ding Tea — a medium cup is *just* the right size. Any bigger and the drink overflows (diverges). Any smaller and it fits perfectly (converges). The p-integral at $p = 1$ is the exact tipping point.

---

## Worked Examples

### Example 1: A Basic Type 1 Integral (Convergent)

**Evaluate** $\displaystyle\int_1^\infty \frac{1}{x^2}\,dx$

**Step 1 — Replace $\infty$ with $b$:**

$$\int_1^\infty \frac{1}{x^2}\,dx = \lim_{b \to \infty} \int_1^b x^{-2}\,dx$$

**Step 2 — Evaluate the definite integral:**

$$= \lim_{b \to \infty} \left[-\frac{1}{x}\right]_1^b = \lim_{b \to \infty} \left(-\frac{1}{b} + \frac{1}{1}\right)$$

**Step 3 — Take the limit:**

$$= \lim_{b \to \infty} \left(1 - \frac{1}{b}\right) = 1 - 0 = \boxed{1}$$

The integral **converges** to $1$. This confirms the p-integral formula: $p = 2 > 1$, so $\frac{1}{p-1} = \frac{1}{1} = 1$.

---

### Example 2: A Basic Type 1 Integral (Divergent)

**Evaluate** $\displaystyle\int_1^\infty \frac{1}{x}\,dx$

$$\int_1^\infty \frac{1}{x}\,dx = \lim_{b \to \infty} \int_1^b \frac{1}{x}\,dx = \lim_{b \to \infty} [\ln|x|]_1^b = \lim_{b \to \infty} (\ln b - \ln 1) = \lim_{b \to \infty} \ln b = \infty$$

The integral **diverges**. This is $p = 1$, the exact boundary case.

Think of it like driving up the I-5 to LA. Even though the scenery gets less interesting per mile (you've already seen the coast, now it's just flat freeway), the total "scenery points" keep piling up without bound. The rate of decrease ($\frac{1}{x}$) isn't fast enough.

---

### Example 3: Exponential Decay

**Evaluate** $\displaystyle\int_0^\infty e^{-3x}\,dx$

$$= \lim_{b \to \infty} \int_0^b e^{-3x}\,dx = \lim_{b \to \infty} \left[-\frac{1}{3}e^{-3x}\right]_0^b$$

$$= \lim_{b \to \infty} \left(-\frac{1}{3}e^{-3b} + \frac{1}{3}e^{0}\right) = 0 + \frac{1}{3} = \boxed{\frac{1}{3}}$$

**Converges** to $\frac{1}{3}$. Exponential decay always beats any polynomial — $e^{-3x}$ shrinks so fast that the total area is finite.

---

### Example 4: Integral from $-\infty$ to a Finite Bound

**Evaluate** $\displaystyle\int_{-\infty}^0 e^{2x}\,dx$

$$= \lim_{a \to -\infty} \int_a^0 e^{2x}\,dx = \lim_{a \to -\infty} \left[\frac{1}{2}e^{2x}\right]_a^0$$

$$= \lim_{a \to -\infty} \left(\frac{1}{2}e^{0} - \frac{1}{2}e^{2a}\right) = \frac{1}{2} - 0 = \boxed{\frac{1}{2}}$$

**Converges** to $\frac{1}{2}$.

---

### Example 5: Doubly-Infinite Integral

**Evaluate** $\displaystyle\int_{-\infty}^{\infty} \frac{1}{1 + x^2}\,dx$

Split at $x = 0$:

$$\int_{-\infty}^{\infty} \frac{1}{1 + x^2}\,dx = \int_{-\infty}^{0} \frac{1}{1 + x^2}\,dx + \int_{0}^{\infty} \frac{1}{1 + x^2}\,dx$$

**Right half:**

$$\int_0^\infty \frac{1}{1+x^2}\,dx = \lim_{b \to \infty} [\arctan x]_0^b = \lim_{b \to \infty} (\arctan b - \arctan 0) = \frac{\pi}{2} - 0 = \frac{\pi}{2}$$

**Left half:**

$$\int_{-\infty}^0 \frac{1}{1+x^2}\,dx = \lim_{a \to -\infty} [\arctan x]_a^0 = 0 - \left(-\frac{\pi}{2}\right) = \frac{\pi}{2}$$

**Total:**

$$\frac{\pi}{2} + \frac{\pi}{2} = \boxed{\pi}$$

This is a famous result: the total area under the curve $y = \frac{1}{1+x^2}$ across the entire real line is exactly $\pi$. Beautiful.

---

### Example 6: Type 2 — Vertical Asymptote at an Endpoint

**Evaluate** $\displaystyle\int_0^1 \frac{1}{\sqrt{x}}\,dx$

The integrand $\frac{1}{\sqrt{x}} \to \infty$ as $x \to 0^+$, so this is a Type 2 improper integral.

$$= \lim_{t \to 0^+} \int_t^1 x^{-1/2}\,dx = \lim_{t \to 0^+} \left[2\sqrt{x}\right]_t^1 = \lim_{t \to 0^+} \left(2\sqrt{1} - 2\sqrt{t}\right) = 2 - 0 = \boxed{2}$$

**Converges** to $2$. Even though the function shoots to infinity near $x = 0$, the area underneath remains finite because $\frac{1}{\sqrt{x}}$ grows "slowly enough."

---

### Example 7: Type 2 — Vertical Asymptote in the Interior

**Evaluate** $\displaystyle\int_0^3 \frac{1}{(x - 1)^2}\,dx$

The integrand has a vertical asymptote at $x = 1$, which is *inside* the interval $[0, 3]$. We must split:

$$\int_0^3 \frac{1}{(x-1)^2}\,dx = \int_0^1 \frac{1}{(x-1)^2}\,dx + \int_1^3 \frac{1}{(x-1)^2}\,dx$$

**Left piece:**

$$\int_0^1 \frac{1}{(x-1)^2}\,dx = \lim_{t \to 1^-} \left[-\frac{1}{x-1}\right]_0^t = \lim_{t \to 1^-} \left(-\frac{1}{t-1} + \frac{1}{0-1}\right) = \lim_{t \to 1^-} \left(-\frac{1}{t-1} - 1\right)$$

As $t \to 1^-$, $t - 1 \to 0^-$, so $-\frac{1}{t-1} \to +\infty$.

The left piece **diverges**, so the entire integral **diverges**.

We don't even need to check the right piece. Once one part diverges, the whole thing diverges.

**Critical warning:** If you blindly apply the FTC without checking for discontinuities:

$$\left[-\frac{1}{x-1}\right]_0^3 = -\frac{1}{2} - (-(-1)) = -\frac{1}{2} - 1 = -\frac{3}{2}$$

This is **wrong**! You'd get a negative answer for an integral of a positive function — a clear sign something went wrong. Always check for vertical asymptotes inside your interval.

---

### Example 8: A Tricky Convergence with Partial Fractions

**Evaluate** $\displaystyle\int_2^\infty \frac{1}{x^2 - 1}\,dx$

**Step 1 — Partial fractions:**

$$\frac{1}{x^2-1} = \frac{1}{(x-1)(x+1)} = \frac{1}{2}\cdot\frac{1}{x-1} - \frac{1}{2}\cdot\frac{1}{x+1}$$

**Step 2 — Integrate:**

$$\int_2^\infty \frac{1}{x^2-1}\,dx = \lim_{b \to \infty} \frac{1}{2}\int_2^b \left(\frac{1}{x-1} - \frac{1}{x+1}\right)dx$$

$$= \lim_{b \to \infty} \frac{1}{2}\left[\ln\left|\frac{x-1}{x+1}\right|\right]_2^b$$

$$= \lim_{b \to \infty} \frac{1}{2}\left(\ln\left|\frac{b-1}{b+1}\right| - \ln\left|\frac{1}{3}\right|\right)$$

**Step 3 — Take the limit:**

$$\frac{b-1}{b+1} = \frac{1 - \frac{1}{b}}{1 + \frac{1}{b}} \to 1 \quad \text{as } b \to \infty$$

$$= \frac{1}{2}\left(\ln 1 - \ln\frac{1}{3}\right) = \frac{1}{2}\left(0 + \ln 3\right) = \boxed{\frac{\ln 3}{2}}$$

---

### Example 9: Comparison Test in Action

**Determine whether** $\displaystyle\int_1^\infty \frac{1}{x^2 + 5}\,dx$ **converges or diverges.**

We don't need to evaluate this exactly — we just need to determine convergence.

**Comparison:** For $x \geq 1$:

$$x^2 + 5 > x^2 \implies \frac{1}{x^2 + 5} < \frac{1}{x^2}$$

We know $\int_1^\infty \frac{1}{x^2}\,dx$ converges (p-integral with $p = 2 > 1$).

Since $0 \leq \frac{1}{x^2 + 5} \leq \frac{1}{x^2}$ and the bigger integral converges, the smaller one **converges** too by the **Direct Comparison Test**.

Think of it like this: if Ganga can finish her entire Science Olympiad study packet in one weekend (the bigger task is finite), then she can definitely finish just the biology section (a smaller portion of the same task) in that time too.

---

### Example 10: Comparison Test — Divergence Direction

**Determine whether** $\displaystyle\int_1^\infty \frac{1}{\sqrt{x} + 1}\,dx$ **converges or diverges.**

**Comparison:** For $x \geq 1$:

$$\sqrt{x} + 1 \leq \sqrt{x} + \sqrt{x} = 2\sqrt{x} \implies \frac{1}{\sqrt{x} + 1} \geq \frac{1}{2\sqrt{x}}$$

We know $\int_1^\infty \frac{1}{2\sqrt{x}}\,dx = \frac{1}{2}\int_1^\infty x^{-1/2}\,dx$ diverges (p-integral with $p = \frac{1}{2} \leq 1$).

Since $\frac{1}{\sqrt{x}+1} \geq \frac{1}{2\sqrt{x}} \geq 0$ and the smaller integral diverges, the larger one **diverges** too.

---

### Gabriel's Horn: The Mind-Bending Paradox

Here's a concept that will truly bend your brain. Take the curve $y = \frac{1}{x}$ for $x \geq 1$ and revolve it around the x-axis. You get a shape called **Gabriel's Horn** — an infinitely long trumpet.

**Volume** (using the disk method):

$$V = \pi\int_1^\infty \left(\frac{1}{x}\right)^2 dx = \pi\int_1^\infty \frac{1}{x^2}\,dx = \pi \cdot 1 = \boxed{\pi}$$

The volume is finite! You could fill Gabriel's Horn with exactly $\pi$ cubic units of paint.

**Surface Area:**

$$S = 2\pi\int_1^\infty \frac{1}{x}\sqrt{1 + \frac{1}{x^4}}\,dx$$

Since $\sqrt{1 + \frac{1}{x^4}} > 1$, we have:

$$S > 2\pi\int_1^\infty \frac{1}{x}\,dx = \infty$$

The surface area is infinite!

**The paradox:** You can fill the horn with a finite amount of paint, but you can never paint its inner surface. You'd need infinite paint to coat the walls, yet finite paint to fill the entire inside. This is the kind of thing that makes your brain feel like it just did a backflip during a dance rehearsal.

The resolution? The horn gets infinitely narrow — so the paint filling the inside *does* coat the walls, just in an infinitely thin layer. The mathematical "paradox" comes from confusing physical paint (which has thickness) with mathematical area (which has none).

---

## Key Formulas & Rules

| Concept | Formula / Rule |
|---------|---------------|
| Type 1 (upper $\infty$) | $\int_a^\infty f(x)\,dx = \lim_{b \to \infty} \int_a^b f(x)\,dx$ |
| Type 1 (lower $-\infty$) | $\int_{-\infty}^b f(x)\,dx = \lim_{a \to -\infty} \int_a^b f(x)\,dx$ |
| Type 1 (both $\pm\infty$) | Split: $\int_{-\infty}^c f\,dx + \int_c^\infty f\,dx$ (both must converge) |
| Type 2 (asymptote at $b$) | $\int_a^b f(x)\,dx = \lim_{t \to b^-} \int_a^t f(x)\,dx$ |
| Type 2 (asymptote at $a$) | $\int_a^b f(x)\,dx = \lim_{t \to a^+} \int_t^b f(x)\,dx$ |
| Type 2 (interior asymptote) | Split at the asymptote; both pieces must converge |
| p-integral ($p > 1$) | $\int_1^\infty \frac{1}{x^p}\,dx = \frac{1}{p-1}$ — **converges** |
| p-integral ($p \leq 1$) | $\int_1^\infty \frac{1}{x^p}\,dx$ — **diverges** |
| $\int_a^\infty e^{-kx}\,dx$ ($k > 0$) | $= \frac{e^{-ka}}{k}$ — **converges** |
| Direct Comparison | If $0 \leq f(x) \leq g(x)$ and $\int g$ converges, then $\int f$ converges |
| Direct Comparison | If $f(x) \geq g(x) \geq 0$ and $\int g$ diverges, then $\int f$ diverges |
| Limit Comparison | If $\lim_{x\to\infty}\frac{f(x)}{g(x)} = L$ with $0 < L < \infty$, then $\int f$ and $\int g$ both converge or both diverge |

---

## Common Mistakes to Avoid

### 1. Forgetting to check for discontinuities inside the interval

**Wrong:** Evaluate $\int_0^2 \frac{1}{x-1}\,dx$ directly:

$$[\ln|x-1|]_0^2 = \ln 1 - \ln 1 = 0$$

**Right:** Recognize the vertical asymptote at $x = 1$. Split into $\int_0^1$ and $\int_1^2$, each evaluated with limits. Both pieces diverge, so the integral **diverges** (the answer is *not* zero).

---

### 2. Treating $\int_{-\infty}^{\infty}$ as a single limit

**Wrong:**

$$\int_{-\infty}^{\infty} x\,dx = \lim_{b \to \infty} \int_{-b}^{b} x\,dx = \lim_{b \to \infty} 0 = 0$$

**Right:** Split into two independent limits:

$$\int_{-\infty}^{0} x\,dx = \lim_{a \to -\infty}\frac{a^2}{2} \cdot (-1) = -\infty \quad \text{(diverges)}$$

Since one piece diverges, the integral **diverges**. The "symmetric" cancellation is not valid — that would be the Cauchy Principal Value, which is a different concept not tested on the AP exam.

---

### 3. Confusing $p > 1$ vs. $p < 1$ for convergence

**Wrong:** "The bigger the power, the bigger the function, so it diverges more."

**Right:** The bigger the power in the *denominator*, the *faster* the function decays, and the *more likely* it converges. $\frac{1}{x^3}$ decays faster than $\frac{1}{x^2}$, which decays faster than $\frac{1}{x}$.

Remember: **p bigger than 1 = converges**. Think of it like grades — you need *more* than a 1.0 GPA to pass (converge). Exactly 1.0 or below? You don't make it (diverge).

---

### 4. Getting the comparison direction wrong

**Wrong:** "$\frac{1}{x^2+1} < \frac{1}{x^2}$ and $\int \frac{1}{x^2}$ converges, therefore $\int \frac{1}{x^2+1}$ diverges."

**Right:** If the *bigger* function converges, the *smaller* one converges too. If the *smaller* function diverges, the *bigger* one diverges too.

Think of it like this: if Ganga can carry all the Panda Express bags to the car (bigger task = finite), she can definitely carry just the orange chicken (smaller task = also finite).

---

### 5. Evaluating the antiderivative at $\infty$ without a limit

**Wrong:** $\int_1^\infty \frac{1}{x^2}\,dx = \left[-\frac{1}{x}\right]_1^\infty = -\frac{1}{\infty} + 1 = 1$

**Right:** Always write the limit explicitly:

$$\lim_{b \to \infty}\left[-\frac{1}{x}\right]_1^b = \lim_{b \to \infty}\left(-\frac{1}{b} + 1\right) = 1$$

The answer happens to be the same, but on the AP free response, you *must* show the limit notation to earn full credit.

---

## AP Exam Tips

**1. Always write the limit.** On free response, the AP graders specifically look for $\lim_{b \to \infty}$ notation. Jumping straight to "plug in $\infty$" will cost you points even if your final answer is correct.

**2. The p-integral is your best friend.** Memorize: $\int_1^\infty \frac{1}{x^p}\,dx$ converges iff $p > 1$. This fact appears constantly — both directly and as the comparison target.

**3. Comparison tests save time on MC.** Many multiple-choice questions ask "does this converge or diverge?" without asking for the exact value. Use comparison with a known p-integral to answer quickly.

**4. Check for hidden discontinuities.** Before evaluating any definite integral, scan the integrand for division by zero or other discontinuities inside $[a, b]$. This is a classic trap on both MC and FR.

**5. Connect to series (BC).** The Integral Test for series says: $\sum_{n=1}^{\infty} f(n)$ and $\int_1^\infty f(x)\,dx$ either both converge or both diverge (when $f$ is positive, continuous, and decreasing). This bridge between Unit 8 and Unit 10 is heavily tested.

**6. Gabriel's Horn is fair game.** While they won't ask you to compute the full surface area integral, they might ask about the volume or use the horn as a conceptual question about the relationship between convergence and divergence.

**7. Know the common convergent integrals.** These appear repeatedly:
- $\int_1^\infty \frac{1}{x^2}\,dx = 1$
- $\int_0^\infty e^{-x}\,dx = 1$
- $\int_{-\infty}^{\infty}\frac{1}{1+x^2}\,dx = \pi$

**8. Time management.** Improper integral evaluations on FR are typically worth 3-4 points. Don't spend 10 minutes on one — set up the limit, evaluate the antiderivative, take the limit, state convergence or divergence.

---

## Practice Problems

### Basic (Problems 1-5)

**1.** Evaluate $\displaystyle\int_1^\infty \frac{1}{x^3}\,dx$.

---

**2.** Determine whether $\displaystyle\int_1^\infty \frac{1}{\sqrt{x}}\,dx$ converges or diverges. If it converges, find its value.

---

**3.** Evaluate $\displaystyle\int_0^\infty e^{-5x}\,dx$.

---

**4.** Evaluate $\displaystyle\int_{-\infty}^{0} e^{4x}\,dx$.

---

**5.** Determine whether $\displaystyle\int_0^1 \frac{1}{x^{2/3}}\,dx$ converges or diverges. If it converges, find its value.

---

### Intermediate (Problems 6-10)

**6.** Evaluate $\displaystyle\int_2^\infty \frac{1}{x(\ln x)^2}\,dx$.

---

**7.** Evaluate $\displaystyle\int_0^4 \frac{1}{\sqrt{4 - x}}\,dx$.

---

**8.** Determine whether $\displaystyle\int_1^\infty \frac{x}{x^3 + 1}\,dx$ converges or diverges.

---

**9.** Evaluate $\displaystyle\int_{-\infty}^{\infty} \frac{1}{4 + x^2}\,dx$.

---

**10.** Evaluate $\displaystyle\int_0^{\pi/2} \tan x\,dx$.

---

### Advanced (Problems 11-15)

**11.** Evaluate $\displaystyle\int_0^\infty xe^{-x}\,dx$.

---

**12.** Determine whether $\displaystyle\int_1^\infty \frac{\sin^2 x}{x^2}\,dx$ converges or diverges.

---

**13.** Evaluate $\displaystyle\int_0^1 \ln x\,dx$.

---

**14.** Determine whether $\displaystyle\int_1^\infty \frac{1}{x + e^x}\,dx$ converges or diverges.

---

**15.** Evaluate $\displaystyle\int_0^\infty \frac{x}{(1 + x^2)^2}\,dx$.

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

Which of the following improper integrals converges?

| Choice | Integral |
|--------|----------|
| **(A)** | $\displaystyle\int_1^\infty \frac{1}{x^{0.99}}\,dx$ |
| **(B)** | $\displaystyle\int_1^\infty \frac{1}{x}\,dx$ |
| **(C)** | $\displaystyle\int_1^\infty \frac{1}{x\ln x}\,dx$ |
| **(D)** | $\displaystyle\int_1^\infty \frac{1}{x^{1.01}}\,dx$ |

---

#### Problem 17 (Multiple Choice)

If $\displaystyle\int_1^\infty f(x)\,dx$ converges and $0 \leq g(x) \leq f(x)$ for all $x \geq 1$, which of the following must be true?

| Choice | Statement |
|--------|-----------|
| **(A)** | $\displaystyle\int_1^\infty g(x)\,dx$ converges |
| **(B)** | $\displaystyle\int_1^\infty g(x)\,dx$ diverges |
| **(C)** | $\displaystyle\int_1^\infty [f(x) - g(x)]\,dx$ diverges |
| **(D)** | $\displaystyle\int_1^\infty g(x)\,dx = \int_1^\infty f(x)\,dx$ |

---

#### Problem 18 (Multiple Choice)

The integral $\displaystyle\int_0^3 \frac{1}{(x-1)^{2/3}}\,dx$ is:

| Choice | Answer |
|--------|--------|
| **(A)** | Divergent because of the asymptote at $x = 1$ |
| **(B)** | Convergent and equal to $3\left(\sqrt[3]{2} + 1\right)$ |
| **(C)** | Convergent and equal to $3\left(\sqrt[3]{4} + 1\right)$ |
| **(D)** | Convergent and equal to $3\sqrt[3]{2}$ |

---

#### Problem 19 (Free Response)

> Consider the improper integral $\displaystyle\int_1^\infty \frac{3}{x^2 + 2x}\,dx$.
>
> **(a)** Show that $\frac{3}{x^2 + 2x}$ can be written as $\frac{3}{2}\left(\frac{1}{x} - \frac{1}{x+2}\right)$.
>
> **(b)** Evaluate the improper integral or show that it diverges. Show all limit notation.
>
> **(c)** Use the Comparison Test to provide an alternative argument for convergence. Clearly state what function you compare to and why.

---

#### Problem 20 (Free Response)

> Ganga is in Robotics club and her team is modeling the power output $P(t)$ (in watts) of a solar panel over an infinite time horizon. The power output is modeled by:
>
> $$P(t) = \frac{100}{(t + 1)^2} \quad \text{for } t \geq 0$$
>
> where $t$ is measured in hours after sunrise.
>
> **(a)** Set up and evaluate an improper integral to find the total energy (in watt-hours) produced by the solar panel from $t = 0$ to $t = \infty$.
>
> **(b)** How much energy is produced in the first 9 hours? What fraction of the total energy does this represent?
>
> **(c)** The team considers an alternative model $Q(t) = \frac{100}{(t+1)^p}$ for $t \geq 0$. For what values of $p$ does the total energy $\int_0^\infty Q(t)\,dt$ converge? Find the total energy as a function of $p$ for those values.
>
> **(d)** The team debates: if $p = 1$, the panel produces more power at each moment than when $p = 2$, yet the total energy is infinite. Explain in a sentence or two why a "more powerful" panel can have an infinite total output while a "less powerful" one has a finite total.

---

## Answer Key

<details>
<summary><strong>Problem 1 Solution</strong></summary>

**Evaluate** $\displaystyle\int_1^\infty \frac{1}{x^3}\,dx$

This is a p-integral with $p = 3 > 1$, so it converges.

$$\int_1^\infty \frac{1}{x^3}\,dx = \lim_{b \to \infty}\int_1^b x^{-3}\,dx = \lim_{b \to \infty}\left[\frac{x^{-2}}{-2}\right]_1^b = \lim_{b \to \infty}\left(-\frac{1}{2b^2} + \frac{1}{2}\right)$$

$$= 0 + \frac{1}{2} = \boxed{\frac{1}{2}}$$

This matches the p-integral formula: $\frac{1}{p-1} = \frac{1}{3-1} = \frac{1}{2}$.

</details>

---

<details>
<summary><strong>Problem 2 Solution</strong></summary>

**Determine whether** $\displaystyle\int_1^\infty \frac{1}{\sqrt{x}}\,dx$ **converges or diverges.**

This is $\int_1^\infty x^{-1/2}\,dx$, a p-integral with $p = \frac{1}{2} \leq 1$, so it **diverges**.

To verify:

$$\int_1^\infty \frac{1}{\sqrt{x}}\,dx = \lim_{b \to \infty}\int_1^b x^{-1/2}\,dx = \lim_{b \to \infty}\left[2\sqrt{x}\right]_1^b = \lim_{b \to \infty}\left(2\sqrt{b} - 2\right) = \infty$$

The integral **diverges**.

</details>

---

<details>
<summary><strong>Problem 3 Solution</strong></summary>

**Evaluate** $\displaystyle\int_0^\infty e^{-5x}\,dx$

$$= \lim_{b \to \infty}\int_0^b e^{-5x}\,dx = \lim_{b \to \infty}\left[-\frac{1}{5}e^{-5x}\right]_0^b$$

$$= \lim_{b \to \infty}\left(-\frac{1}{5}e^{-5b} + \frac{1}{5}e^{0}\right)$$

As $b \to \infty$, $e^{-5b} \to 0$:

$$= 0 + \frac{1}{5} = \boxed{\frac{1}{5}}$$

</details>

---

<details>
<summary><strong>Problem 4 Solution</strong></summary>

**Evaluate** $\displaystyle\int_{-\infty}^{0} e^{4x}\,dx$

$$= \lim_{a \to -\infty}\int_a^0 e^{4x}\,dx = \lim_{a \to -\infty}\left[\frac{1}{4}e^{4x}\right]_a^0$$

$$= \lim_{a \to -\infty}\left(\frac{1}{4}e^{0} - \frac{1}{4}e^{4a}\right)$$

As $a \to -\infty$, $e^{4a} \to 0$:

$$= \frac{1}{4} - 0 = \boxed{\frac{1}{4}}$$

</details>

---

<details>
<summary><strong>Problem 5 Solution</strong></summary>

**Determine whether** $\displaystyle\int_0^1 \frac{1}{x^{2/3}}\,dx$ **converges or diverges.**

This is a Type 2 improper integral because $\frac{1}{x^{2/3}} \to \infty$ as $x \to 0^+$.

$$\int_0^1 \frac{1}{x^{2/3}}\,dx = \lim_{t \to 0^+}\int_t^1 x^{-2/3}\,dx = \lim_{t \to 0^+}\left[\frac{x^{1/3}}{1/3}\right]_t^1 = \lim_{t \to 0^+}\left[3x^{1/3}\right]_t^1$$

$$= \lim_{t \to 0^+}\left(3(1)^{1/3} - 3t^{1/3}\right) = 3 - 0 = \boxed{3}$$

The integral **converges** to $3$.

Note: For Type 2 p-integrals of the form $\int_0^1 \frac{1}{x^p}\,dx$, the integral converges when $p < 1$ and diverges when $p \geq 1$. Here $p = \frac{2}{3} < 1$, so it converges.

</details>

---

<details>
<summary><strong>Problem 6 Solution</strong></summary>

**Evaluate** $\displaystyle\int_2^\infty \frac{1}{x(\ln x)^2}\,dx$

**Substitution:** Let $u = \ln x$, so $du = \frac{1}{x}\,dx$.

When $x = 2$, $u = \ln 2$. When $x \to \infty$, $u \to \infty$.

$$\int_2^\infty \frac{1}{x(\ln x)^2}\,dx = \int_{\ln 2}^\infty \frac{1}{u^2}\,du$$

This is a p-integral with $p = 2 > 1$:

$$= \lim_{b \to \infty}\int_{\ln 2}^b u^{-2}\,du = \lim_{b \to \infty}\left[-\frac{1}{u}\right]_{\ln 2}^b = \lim_{b \to \infty}\left(-\frac{1}{b} + \frac{1}{\ln 2}\right)$$

$$= 0 + \frac{1}{\ln 2} = \boxed{\frac{1}{\ln 2}}$$

</details>

---

<details>
<summary><strong>Problem 7 Solution</strong></summary>

**Evaluate** $\displaystyle\int_0^4 \frac{1}{\sqrt{4 - x}}\,dx$

The integrand has a vertical asymptote at $x = 4$ (the upper endpoint), so this is Type 2.

$$= \lim_{t \to 4^-}\int_0^t (4 - x)^{-1/2}\,dx$$

**Substitution:** Let $u = 4 - x$, $du = -dx$.

$$= \lim_{t \to 4^-}\int_{4}^{4-t} u^{-1/2}(-du) = \lim_{t \to 4^-}\int_{4-t}^{4} u^{-1/2}\,du$$

Or more directly, using the antiderivative:

$$\int (4-x)^{-1/2}\,dx = -2(4-x)^{1/2} + C$$

So:

$$= \lim_{t \to 4^-}\left[-2\sqrt{4-x}\right]_0^t = \lim_{t \to 4^-}\left(-2\sqrt{4-t} + 2\sqrt{4}\right)$$

$$= -2(0) + 2(2) = \boxed{4}$$

</details>

---

<details>
<summary><strong>Problem 8 Solution</strong></summary>

**Determine whether** $\displaystyle\int_1^\infty \frac{x}{x^3 + 1}\,dx$ **converges or diverges.**

**Limit Comparison** with $\frac{1}{x^2}$:

For large $x$:

$$\frac{x}{x^3 + 1} \approx \frac{x}{x^3} = \frac{1}{x^2}$$

Formally:

$$\lim_{x \to \infty}\frac{\frac{x}{x^3+1}}{\frac{1}{x^2}} = \lim_{x \to \infty}\frac{x \cdot x^2}{x^3 + 1} = \lim_{x \to \infty}\frac{x^3}{x^3 + 1} = \lim_{x \to \infty}\frac{1}{1 + \frac{1}{x^3}} = 1$$

Since $0 < 1 < \infty$ and $\int_1^\infty \frac{1}{x^2}\,dx$ converges ($p = 2 > 1$), by the Limit Comparison Test, $\int_1^\infty \frac{x}{x^3+1}\,dx$ also **converges**.

Alternatively, by **Direct Comparison**: for $x \geq 1$, $x^3 + 1 > x^3$, so $\frac{x}{x^3+1} < \frac{x}{x^3} = \frac{1}{x^2}$. Since $\int_1^\infty \frac{1}{x^2}\,dx$ converges and $\frac{x}{x^3+1} < \frac{1}{x^2}$, the integral converges by Direct Comparison.

</details>

---

<details>
<summary><strong>Problem 9 Solution</strong></summary>

**Evaluate** $\displaystyle\int_{-\infty}^{\infty} \frac{1}{4 + x^2}\,dx$

Split at $x = 0$:

$$\int_{-\infty}^{\infty}\frac{1}{4+x^2}\,dx = \int_{-\infty}^{0}\frac{1}{4+x^2}\,dx + \int_{0}^{\infty}\frac{1}{4+x^2}\,dx$$

**Right half:**

Note that $\frac{1}{4+x^2} = \frac{1}{4}\cdot\frac{1}{1+(x/2)^2}$, and $\int \frac{1}{4+x^2}\,dx = \frac{1}{2}\arctan\frac{x}{2} + C$.

$$\int_0^\infty \frac{1}{4+x^2}\,dx = \lim_{b \to \infty}\left[\frac{1}{2}\arctan\frac{x}{2}\right]_0^b = \lim_{b \to \infty}\frac{1}{2}\arctan\frac{b}{2} - \frac{1}{2}\arctan 0$$

$$= \frac{1}{2}\cdot\frac{\pi}{2} - 0 = \frac{\pi}{4}$$

**Left half:** By symmetry of the integrand (even function):

$$\int_{-\infty}^0 \frac{1}{4+x^2}\,dx = \frac{\pi}{4}$$

**Total:**

$$\frac{\pi}{4} + \frac{\pi}{4} = \boxed{\frac{\pi}{2}}$$

</details>

---

<details>
<summary><strong>Problem 10 Solution</strong></summary>

**Evaluate** $\displaystyle\int_0^{\pi/2} \tan x\,dx$

The integrand $\tan x = \frac{\sin x}{\cos x} \to \infty$ as $x \to \frac{\pi}{2}^-$. This is a Type 2 improper integral.

$$\int_0^{\pi/2}\tan x\,dx = \lim_{t \to (\pi/2)^-}\int_0^t \tan x\,dx = \lim_{t \to (\pi/2)^-}[-\ln|\cos x|]_0^t$$

$$= \lim_{t \to (\pi/2)^-}\left(-\ln|\cos t| + \ln|\cos 0|\right) = \lim_{t \to (\pi/2)^-}\left(-\ln|\cos t| + \ln 1\right)$$

$$= \lim_{t \to (\pi/2)^-}\left(-\ln|\cos t|\right)$$

As $t \to \frac{\pi}{2}^-$, $\cos t \to 0^+$, so $\ln|\cos t| \to -\infty$, and $-\ln|\cos t| \to +\infty$.

The integral **diverges**.

Think of driving along Torrey Pines cliffs — as you approach the edge, the slope gets steeper and steeper without bound. The total "steepness" you accumulate is infinite.

</details>

---

<details>
<summary><strong>Problem 11 Solution</strong></summary>

**Evaluate** $\displaystyle\int_0^\infty xe^{-x}\,dx$

Use **integration by parts**: $u = x$, $dv = e^{-x}\,dx$, so $du = dx$, $v = -e^{-x}$.

$$\int_0^\infty xe^{-x}\,dx = \lim_{b \to \infty}\int_0^b xe^{-x}\,dx$$

$$= \lim_{b \to \infty}\left(\left[-xe^{-x}\right]_0^b + \int_0^b e^{-x}\,dx\right)$$

$$= \lim_{b \to \infty}\left(-be^{-b} + 0 + \left[-e^{-x}\right]_0^b\right)$$

$$= \lim_{b \to \infty}\left(-be^{-b} - e^{-b} + e^{0}\right)$$

$$= \lim_{b \to \infty}\left(-be^{-b} - e^{-b} + 1\right)$$

Now, $\lim_{b \to \infty} be^{-b} = \lim_{b \to \infty}\frac{b}{e^b} = 0$ (by L'Hopital's Rule or because exponentials dominate polynomials).

Also, $\lim_{b \to \infty} e^{-b} = 0$.

$$= 0 - 0 + 1 = \boxed{1}$$

This is actually $\Gamma(2) = 1! = 1$ — a preview of the Gamma function you'll see in more advanced math.

</details>

---

<details>
<summary><strong>Problem 12 Solution</strong></summary>

**Determine whether** $\displaystyle\int_1^\infty \frac{\sin^2 x}{x^2}\,dx$ **converges or diverges.**

Use the **Direct Comparison Test**.

Since $0 \leq \sin^2 x \leq 1$ for all $x$:

$$0 \leq \frac{\sin^2 x}{x^2} \leq \frac{1}{x^2}$$

We know $\int_1^\infty \frac{1}{x^2}\,dx$ converges (p-integral, $p = 2 > 1$).

By the Direct Comparison Test, $\displaystyle\int_1^\infty \frac{\sin^2 x}{x^2}\,dx$ **converges**.

Note: We cannot easily find the exact value — but the question only asks about convergence, and comparison gives us the answer cleanly.

</details>

---

<details>
<summary><strong>Problem 13 Solution</strong></summary>

**Evaluate** $\displaystyle\int_0^1 \ln x\,dx$

This is a Type 2 improper integral because $\ln x \to -\infty$ as $x \to 0^+$.

$$\int_0^1 \ln x\,dx = \lim_{t \to 0^+}\int_t^1 \ln x\,dx$$

**Integration by parts:** $u = \ln x$, $dv = dx$, so $du = \frac{1}{x}\,dx$, $v = x$.

$$\int \ln x\,dx = x\ln x - \int x \cdot \frac{1}{x}\,dx = x\ln x - x + C$$

So:

$$= \lim_{t \to 0^+}\left[x\ln x - x\right]_t^1 = \lim_{t \to 0^+}\left((1\cdot\ln 1 - 1) - (t\ln t - t)\right)$$

$$= \lim_{t \to 0^+}\left((0 - 1) - t\ln t + t\right)$$

$$= -1 - \lim_{t \to 0^+} t\ln t + 0$$

We need $\lim_{t \to 0^+} t\ln t$. This is a $0 \cdot (-\infty)$ form. Rewrite:

$$\lim_{t \to 0^+} t\ln t = \lim_{t \to 0^+}\frac{\ln t}{1/t}$$

This is $\frac{-\infty}{\infty}$, so apply L'Hopital's Rule:

$$= \lim_{t \to 0^+}\frac{1/t}{-1/t^2} = \lim_{t \to 0^+}\frac{t^2}{-t} = \lim_{t \to 0^+}(-t) = 0$$

Therefore:

$$\int_0^1 \ln x\,dx = -1 - 0 = \boxed{-1}$$

</details>

---

<details>
<summary><strong>Problem 14 Solution</strong></summary>

**Determine whether** $\displaystyle\int_1^\infty \frac{1}{x + e^x}\,dx$ **converges or diverges.**

Use the **Direct Comparison Test**.

For $x \geq 1$:

$$x + e^x > e^x \implies \frac{1}{x + e^x} < \frac{1}{e^x} = e^{-x}$$

We know $\int_1^\infty e^{-x}\,dx$ converges:

$$\int_1^\infty e^{-x}\,dx = \lim_{b \to \infty}\left[-e^{-x}\right]_1^b = 0 + e^{-1} = \frac{1}{e}$$

Since $0 < \frac{1}{x+e^x} < e^{-x}$ for $x \geq 1$ and $\int_1^\infty e^{-x}\,dx$ converges, by the Direct Comparison Test, $\displaystyle\int_1^\infty \frac{1}{x+e^x}\,dx$ **converges**.

</details>

---

<details>
<summary><strong>Problem 15 Solution</strong></summary>

**Evaluate** $\displaystyle\int_0^\infty \frac{x}{(1 + x^2)^2}\,dx$

**Substitution:** Let $u = 1 + x^2$, so $du = 2x\,dx$, which means $x\,dx = \frac{du}{2}$.

When $x = 0$, $u = 1$. When $x \to \infty$, $u \to \infty$.

$$\int_0^\infty \frac{x}{(1+x^2)^2}\,dx = \int_1^\infty \frac{1}{u^2}\cdot\frac{du}{2} = \frac{1}{2}\int_1^\infty u^{-2}\,du$$

$$= \frac{1}{2}\lim_{b \to \infty}\left[-\frac{1}{u}\right]_1^b = \frac{1}{2}\lim_{b \to \infty}\left(-\frac{1}{b} + 1\right) = \frac{1}{2}(0 + 1) = \boxed{\frac{1}{2}}$$

</details>

---

<details>
<summary><strong>Problem 16 Solution</strong></summary>

**Answer: (D)** $\displaystyle\int_1^\infty \frac{1}{x^{1.01}}\,dx$

Apply the p-integral test to each:

- **(A)** $p = 0.99 < 1$ — **diverges**
- **(B)** $p = 1$ — **diverges**
- **(C)** This is not a standard p-integral, but let's check: $\int_1^\infty \frac{1}{x\ln x}\,dx$. Substitute $u = \ln x$, $du = \frac{dx}{x}$:
  $$\int_{\ln 1}^{\infty}\frac{du}{u} = \int_0^\infty \frac{du}{u}$$
  This diverges (it's the p-integral in $u$ with $p = 1$). **Diverges.**
- **(D)** $p = 1.01 > 1$ — **converges** to $\frac{1}{0.01} = 100$.

$\boxed{\text{(D)}}$

</details>

---

<details>
<summary><strong>Problem 17 Solution</strong></summary>

**Answer: (A)** $\displaystyle\int_1^\infty g(x)\,dx$ converges.

This is a direct application of the **Direct Comparison Test**:

- We're given $0 \leq g(x) \leq f(x)$ for all $x \geq 1$
- We're given $\int_1^\infty f(x)\,dx$ converges

Since $g$ is bounded above by $f$ and both are non-negative, and the integral of the bigger function converges, the integral of the smaller function must also converge.

Why not the other choices?

- **(B)** is the opposite — it would converge, not diverge.
- **(C)** $f(x) - g(x) \geq 0$, and $f(x) - g(x) \leq f(x)$, so $\int [f - g]\,dx$ also converges (by Comparison again). So (C) is false.
- **(D)** We only know $g \leq f$; equality of the integrals is not guaranteed. For example, $f(x) = \frac{1}{x^2}$ and $g(x) = \frac{1}{x^3}$ both converge but to different values.

$\boxed{\text{(A)}}$

</details>

---

<details>
<summary><strong>Problem 18 Solution</strong></summary>

**Answer: (B)** Convergent and equal to $3\left(\sqrt[3]{2} + 1\right)$

The integrand $\frac{1}{(x-1)^{2/3}}$ has a vertical asymptote at $x = 1$ (inside the interval $[0, 3]$). This is a Type 2 improper integral. Split at the asymptote:

$$\int_0^3 \frac{1}{(x-1)^{2/3}}\,dx = \int_0^1 \frac{1}{(x-1)^{2/3}}\,dx + \int_1^3 \frac{1}{(x-1)^{2/3}}\,dx$$

**Left piece** (note: for $x < 1$, $(x-1)$ is negative, so we work with $|x-1|^{2/3} = (1-x)^{2/3}$):

$$\int_0^1 \frac{dx}{(1-x)^{2/3}} = \lim_{t \to 1^-}\int_0^t (1-x)^{-2/3}\,dx$$

Let $u = 1 - x$, $du = -dx$:

$$= \lim_{t \to 1^-}\left[-3(1-x)^{1/3}\right]_0^t = \lim_{t \to 1^-}\left(-3(1-t)^{1/3} + 3(1)^{1/3}\right) = 0 + 3 = 3$$

**Right piece:**

$$\int_1^3 \frac{dx}{(x-1)^{2/3}} = \lim_{t \to 1^+}\left[3(x-1)^{1/3}\right]_t^3 = 3(2)^{1/3} - \lim_{t \to 1^+}3(t-1)^{1/3} = 3\sqrt[3]{2} - 0 = 3\sqrt[3]{2}$$

**Total:**

$$3 + 3\sqrt[3]{2} = 3(1 + \sqrt[3]{2}) = \boxed{3\left(\sqrt[3]{2} + 1\right)}$$

The integral **converges**. Answer: **(B)**.

</details>

---

<details>
<summary><strong>Problem 19 Solution</strong></summary>

**(a)** Show the partial fraction decomposition:

$$\frac{3}{x^2 + 2x} = \frac{3}{x(x + 2)}$$

Set up: $\frac{3}{x(x+2)} = \frac{A}{x} + \frac{B}{x+2}$

Multiply both sides by $x(x+2)$:

$$3 = A(x+2) + Bx$$

Set $x = 0$: $3 = 2A$, so $A = \frac{3}{2}$.

Set $x = -2$: $3 = -2B$, so $B = -\frac{3}{2}$.

$$\frac{3}{x(x+2)} = \frac{3/2}{x} + \frac{-3/2}{x+2} = \frac{3}{2}\left(\frac{1}{x} - \frac{1}{x+2}\right) \quad \checkmark$$

**(b)** Evaluate the improper integral:

$$\int_1^\infty \frac{3}{x^2+2x}\,dx = \frac{3}{2}\int_1^\infty\left(\frac{1}{x} - \frac{1}{x+2}\right)dx$$

$$= \frac{3}{2}\lim_{b \to \infty}\int_1^b \left(\frac{1}{x} - \frac{1}{x+2}\right)dx$$

$$= \frac{3}{2}\lim_{b \to \infty}\left[\ln|x| - \ln|x+2|\right]_1^b$$

$$= \frac{3}{2}\lim_{b \to \infty}\left[\ln\left|\frac{x}{x+2}\right|\right]_1^b$$

$$= \frac{3}{2}\lim_{b \to \infty}\left(\ln\frac{b}{b+2} - \ln\frac{1}{3}\right)$$

$$= \frac{3}{2}\left(\ln 1 - \ln\frac{1}{3}\right) = \frac{3}{2}\left(0 + \ln 3\right)$$

$$= \boxed{\frac{3\ln 3}{2}}$$

The integral **converges** to $\frac{3\ln 3}{2}$.

**(c)** Alternative convergence argument via Comparison:

For $x \geq 1$: $x^2 + 2x > x^2$, so:

$$\frac{3}{x^2 + 2x} < \frac{3}{x^2}$$

We know $\int_1^\infty \frac{3}{x^2}\,dx = 3 \cdot 1 = 3$ converges (p-integral, $p = 2 > 1$).

Since $0 < \frac{3}{x^2 + 2x} < \frac{3}{x^2}$ and $\int_1^\infty \frac{3}{x^2}\,dx$ converges, by the Direct Comparison Test, $\int_1^\infty \frac{3}{x^2 + 2x}\,dx$ **converges**.

</details>

---

<details>
<summary><strong>Problem 20 Solution</strong></summary>

**(a)** Total energy = $\int_0^\infty P(t)\,dt$:

$$\int_0^\infty \frac{100}{(t+1)^2}\,dt = \lim_{b \to \infty}\int_0^b 100(t+1)^{-2}\,dt$$

$$= \lim_{b \to \infty}\left[-\frac{100}{t+1}\right]_0^b = \lim_{b \to \infty}\left(-\frac{100}{b+1} + \frac{100}{1}\right)$$

$$= 0 + 100 = \boxed{100 \text{ watt-hours}}$$

**(b)** Energy in the first 9 hours:

$$\int_0^9 \frac{100}{(t+1)^2}\,dt = \left[-\frac{100}{t+1}\right]_0^9 = -\frac{100}{10} + \frac{100}{1} = -10 + 100 = 90 \text{ watt-hours}$$

Fraction of total: $\frac{90}{100} = \boxed{90\%}$

The first 9 hours produce 90% of the panel's total (infinite-time) energy output. This makes sense — the power output decays so rapidly that most of the energy comes early.

**(c)** With $Q(t) = \frac{100}{(t+1)^p}$:

$$\int_0^\infty \frac{100}{(t+1)^p}\,dt$$

Substitute $u = t + 1$, $du = dt$. When $t = 0$, $u = 1$; when $t \to \infty$, $u \to \infty$.

$$= 100\int_1^\infty u^{-p}\,du$$

This is a p-integral. It converges when $p > 1$.

For $p > 1$:

$$= 100 \cdot \frac{1}{p - 1} = \boxed{\frac{100}{p - 1} \text{ watt-hours}}$$

Check: when $p = 2$, total = $\frac{100}{1} = 100$ watt-hours, matching part (a). $\checkmark$

**(d)** When $p = 1$, $Q(t) = \frac{100}{t+1}$. At every moment $t$, $Q(t) > P(t)$ (since $\frac{1}{t+1} > \frac{1}{(t+1)^2}$ for $t > 0$). So this panel is indeed "more powerful" at each instant.

However, $Q(t)$ decays like $\frac{1}{t}$, which doesn't decay fast enough for the total energy to converge. The function $P(t) = \frac{1}{(t+1)^2}$ decays much faster, so even though it produces less power at each moment, the total energy remains finite. It's the *rate of decay* that determines convergence, not the size at any given moment.

It's like comparing two boba rewards programs at Ding Tea: one gives you $\frac{1}{n}$ stars on visit $n$ (harmonic — never reaches a total limit, even though each visit adds less), while the other gives $\frac{1}{n^2}$ stars per visit (converges to a finite total). The first program is always more generous per visit, but the second program has a calculable lifetime total.

</details>

---

## What's Next

You've now mastered the art of taming infinity — determining when an infinite process yields a finite result and when it runs away to infinity. This convergence-vs-divergence thinking is the beating heart of the next major BC topic: **infinite series**. In Unit 9, we'll shift gears to [Parametric Derivatives](/calculus/parametric-derivatives), where curves are described by separate $x(t)$ and $y(t)$ equations — like tracking a drone's position over Balboa Park using separate east-west and north-south coordinates. And when we get to Unit 10 (Series), the **Integral Test** will bring us full circle, using the improper integrals you learned today to determine whether infinite sums converge.

---

<div align="center">

[← Partial Fractions](/calculus/partial-fractions) | [Parametric Derivatives →](/calculus/parametric-derivatives)

</div>