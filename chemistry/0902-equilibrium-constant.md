# The Equilibrium Constant
<p class="article-date">July 5, 2026</p>

*My little cousin has this wooden toy bowl — a smooth, curved salad bowl, really — and a single glass marble. His whole game is dropping the marble into the bowl from different heights and different spots along the rim and watching it swirl around. And here's the thing that made me stop and stare: no matter WHERE he drops it, the marble always ends up in the exact same place. Dead center, bottom of the bowl. Drop it high on the left, it rolls to the bottom. Flick it hard around the rim, it spirals down and settles at the bottom. The starting point never matters — the SHAPE of the bowl decides where "rest" is. That resting spot is the whole idea behind the **equilibrium constant, $K$**: at a given temperature, a reaction always settles into the same ratio of products to reactants, no matter what amounts you started with. And if you catch the marble mid-roll and ask "which way is it about to move?" — that's the **reaction quotient, $Q$**. Compare where the marble is now ($Q$) to where it wants to rest ($K$), and you instantly know which way the reaction will roll. This is the number that runs all of AP Unit 7, and once the bowl clicks, it never un-clicks.*

---

## What You'll Learn

- Write the **equilibrium constant expression** $K_c$ for any balanced reaction — products over reactants, each raised to its coefficient
- Know exactly **what to include and exclude**: leave out pure solids and pure liquids; keep aqueous and gas species (and *why*)
- Write $K$ expressions for **heterogeneous equilibria** (mixed phases) without tripping on the omitted solids/liquids
- Convert between $K_c$ (concentrations) and $K_p$ (partial pressures) using $K_p = K_c(RT)^{\Delta n}$
- **Calculate the numerical value of $K$** by plugging equilibrium concentrations or pressures into the expression
- Read the **magnitude of $K$**: $K \gg 1$ favors products, $K \ll 1$ favors reactants, $K \approx 1$ means both matter
- Know what $K$ does **not** tell you — it says nothing about reaction **rate**
- Apply the three **manipulation rules**: reverse a reaction → $1/K$; scale by $n$ → $K^n$; add reactions → multiply their $K$'s
- Compute the **reaction quotient $Q$** and compare it to $K$ to **predict the direction** a reaction will shift

---

## Prerequisites

- [Introduction to Equilibrium](/chemistry/0901-introduction-to-equilibrium) — you must already know that equilibrium is **dynamic** (forward and reverse reactions never stop, they just run at equal rates), and that concentrations go *constant*, not *zero*. This article turns that idea into a single number you can calculate. Everything here assumes you're comfortable with the double arrow $\ce{<=>}$ and the idea of a reaction "settling."

---

## The Core Concept

### Intuition First

Let's stay with my cousin's marble and bowl, because every single piece of this topic is sitting inside that bowl.

**The resting spot is $K$.** Drop the marble in, let it swirl, and it settles at the bottom. That bottom point is fixed — it's baked into the *shape of the bowl*, not into how you dropped the marble. In chemistry, the "resting spot" is a specific **ratio of products to reactants**. Start the Haber reaction with pure $\ce{N2}$ and $\ce{H2}$, or start it with pure $\ce{NH3}$, or start with a random mix — at the same temperature, they all settle to the *same* ratio. That fixed ratio is the equilibrium constant $K$.

**Temperature is the shape of the bowl.** This is the one thing that *can* move the resting spot. Warp the bowl (change the temperature) and the bottom shifts to a new location. So $K$ is constant *for a given temperature* — change the temperature and you get a different $K$. (We'll do exactly *how* temperature moves it in a later article; for now, just remember: same temperature, same resting spot.)

**$Q$ is where the marble is RIGHT NOW.** Freeze-frame the marble halfway down the left wall. It's not at rest yet — but it's *somewhere*, and that position is a number. The reaction quotient $Q$ uses the exact same formula as $K$, but with whatever concentrations you happen to have at this instant, equilibrium or not. $Q$ is a snapshot; $K$ is the destination.

**Comparing $Q$ to $K$ tells you which way it rolls.** This is the payoff. If the marble is up the left wall, it's going to roll *right* toward the bottom. If it's up the right wall, it rolls *left*. Look at where it is versus where it rests, and the direction is obvious. In chemistry:

| Marble | Chemistry | Meaning |
|---|---|---|
| $Q < K$ (not enough product yet) | reaction runs **forward** → makes more product | rolls **right** toward products |
| $Q > K$ (too much product) | reaction runs **reverse** → makes more reactant | rolls **left** toward reactants |
| $Q = K$ | already **at equilibrium** | marble is **at rest** |

**A tilted bowl is a lopsided $K$.** Imagine the bowl isn't symmetric — its resting point sits way over on the product side. That's a **large $K$**: at rest, the mixture is almost all products. A bowl whose low point sits way over on the reactant side is a **small $K$**: at rest, barely any reaction happened. The number $K$ literally encodes how lopsided the bowl is.

Carry this map through the whole article:

| The marble in the bowl | The chemistry |
|---|---|
| The fixed resting spot at the bottom | the **equilibrium constant** $K$ |
| The shape of the bowl | the **temperature** (the only thing that changes $K$) |
| Where the marble is right now | the **reaction quotient** $Q$ |
| Comparing "now" to "rest" | comparing $Q$ to $K$ → **direction of shift** |
| A bowl tilted toward one side | a **very large or very small** $K$ |

### The Equilibrium Constant Expression

For a general balanced reaction

$$\ce{aA + bB <=> cC + dD}$$

the equilibrium constant in terms of concentration is

$$K_c = \frac{[\ce{C}]^c\,[\ce{D}]^d}{[\ce{A}]^a\,[\ce{B}]^b}$$

In words: **products over reactants, each species raised to the power of its coefficient** in the balanced equation. Square brackets $[\ce{X}]$ mean "molar concentration of $\ce{X}$ at equilibrium," in mol/L. The little subscript $c$ reminds you these are concentrations.

That's it. Every $K_c$ expression in the course is built from that one template. The coefficients become exponents; products go on top; reactants go on the bottom.

### What Goes In — and What Gets Left Out

Here is the rule that AP loves to test, and it has exactly one exception to memorize:

> **Pure solids $(s)$ and pure liquids $(l)$ are left OUT of the $K$ expression.** Only **gases $(g)$** and **aqueous species $(aq)$** appear.

Why? The honest answer is that $K$ is really built from **activities**, not concentrations, and the activity of a pure solid or pure liquid is defined as **1**. A pure solid's "concentration" (its density-based amount per volume) doesn't change as the reaction proceeds — a chunk of solid is just as dense whether there's a lot or a little of it. Since it never changes, it contributes a constant factor of $1$ and simply drops out. Same for a pure liquid like water in a molten or pure state.

The classic gotcha: **water**. If water is a pure liquid solvent $\ce{H2O(l)}$, leave it out. If water is a **gas** $\ce{H2O(g)}$, it stays in. Phase label decides everything — always read the $(s)$, $(l)$, $(g)$, $(aq)$.

An equilibrium that mixes phases (some solid or liquid, some gas or aqueous) is called a **heterogeneous equilibrium**. You handle it the exact same way — write products over reactants — then cross out anything labeled $(s)$ or $(l)$.

### $K_c$ vs. $K_p$

For reactions involving gases, we can measure "amount" two ways: by **concentration** (mol/L, giving $K_c$) or by **partial pressure** (atm, giving $K_p$). $K_p$ uses the exact same products-over-reactants template, but with equilibrium partial pressures $P_{\ce{X}}$ instead of concentrations:

$$K_p = \frac{(P_{\ce{C}})^c\,(P_{\ce{D}})^d}{(P_{\ce{A}})^a\,(P_{\ce{B}})^b}$$

The two are linked through the ideal gas law. The relationship is:

$$\boxed{\,K_p = K_c\,(RT)^{\Delta n}\,}$$

where:

- $R = 0.08206\ \frac{\text{L·atm}}{\text{mol·K}}$ (use this value because pressures are in atm),
- $T$ is the temperature in **kelvin**,
- $\Delta n = (\text{moles of gas products}) - (\text{moles of gas reactants})$ — count **only gases**, using the balanced coefficients.

A few consequences worth internalizing:

- If $\Delta n = 0$ (same number of gas molecules on both sides), then $(RT)^0 = 1$ and $K_p = K_c$. They're equal.
- If $\Delta n > 0$ (more gas moles as products), $K_p > K_c$.
- If $\Delta n < 0$ (fewer gas moles as products), $K_p < K_c$.

### The Magnitude of $K$ — Reading the Bowl's Tilt

The *number* $K$ tells you how far the reaction goes before resting:

| Value of $K$ | Bowl picture | At equilibrium... |
|---|---|---|
| $K \gg 1$ (large, e.g. $10^{5}$) | bottom sits far toward the product side | mostly **products** — reaction "goes to completion" |
| $K \ll 1$ (small, e.g. $10^{-5}$) | bottom sits far toward the reactant side | mostly **reactants** — barely reacts |
| $K \approx 1$ | bottom near the middle | **significant amounts of both** |

**What $K$ does NOT tell you: how FAST.** This is a favorite AP trap and a genuine Unit 5 vs. Unit 7 distinction. A huge $K$ means the reaction *strongly favors products at equilibrium* — it says nothing about how long that takes. The rusting of iron and the combustion of diamond both have enormous $K$ values, yet one takes years and the other essentially never happens at room temperature. **Speed is kinetics (Unit 5); position of rest is equilibrium (Unit 7).** The marble always ends up at the bottom of the bowl — $K$ tells you *where* the bottom is, not how quickly the marble gets there.

### Properties of $K$ — Manipulating Reactions

Often you know $K$ for one reaction and need $K$ for a modified version. Three rules cover everything:

1. **Reverse the reaction → invert $K$.** $K_\text{reverse} = \dfrac{1}{K_\text{forward}}$. (Flip the bowl's product/reactant sides; the ratio flips too.)
2. **Multiply all coefficients by $n$ → raise $K$ to the $n$.** $K_\text{new} = (K_\text{old})^{n}$. This includes halving, where $n = \tfrac{1}{2}$ (take the square root).
3. **Add two reactions → multiply their $K$'s.** If reaction 3 = reaction 1 + reaction 2, then $K_3 = K_1 \times K_2$.

These stack. If a problem asks you to reverse *and* double a reaction, invert *and* then square. Rule 3 is the equilibrium cousin of Hess's Law: where Hess's Law **adds** the $\Delta H$'s of combined steps, equilibrium **multiplies** the $K$'s.

### The Reaction Quotient $Q$ and Predicting Direction

$Q$ is computed with the **identical** expression as $K$ — same species, same exponents, products over reactants — but you plug in the **current** concentrations (or pressures), which may or may not be at equilibrium.

$$Q_c = \frac{[\ce{C}]^c\,[\ce{D}]^d}{[\ce{A}]^a\,[\ce{B}]^b}\quad(\text{current values})$$

Then compare:

$$\boxed{\;Q < K \Rightarrow \text{shifts forward (→ products)}\quad Q > K \Rightarrow \text{shifts reverse (→ reactants)}\quad Q = K \Rightarrow \text{at equilibrium}\;}$$

The intuition is the marble: $Q$ is where it is, $K$ is where it rests. If $Q$ is "too small" (not enough product built up yet, $Q < K$), the reaction rolls **forward** to make more product and raise $Q$ up to $K$. If $Q$ is "too big" ($Q > K$), it rolls **reverse**. When $Q = K$, the marble is already at the bottom — no net motion.

---

## Worked Examples

### Example 1: Write $K_c$ for a Homogeneous Gas Reaction

**Problem:** Write the $K_c$ expression for the Haber process: $\ce{N2(g) + 3H2(g) <=> 2NH3(g)}$.

**Solution:**

- **Step 1** — Products on top, reactants on bottom: $\ce{NH3}$ up, $\ce{N2}$ and $\ce{H2}$ down.
- **Step 2** — Each coefficient becomes an exponent: $\ce{NH3}$ has coefficient 2, $\ce{N2}$ has 1, $\ce{H2}$ has 3.

$$K_c = \frac{[\ce{NH3}]^2}{[\ce{N2}]\,[\ce{H2}]^3}$$

**Answer:** $K_c = \dfrac{[\ce{NH3}]^2}{[\ce{N2}][\ce{H2}]^3}$

### Example 2: Heterogeneous Equilibrium — Omit the Solid

**Problem:** Write $K_c$ for the decomposition of limestone: $\ce{CaCO3(s) <=> CaO(s) + CO2(g)}$.

**Solution:**

- **Step 1** — Template: $K_c = \dfrac{[\ce{CaO}]\,[\ce{CO2}]}{[\ce{CaCO3}]}$.
- **Step 2** — Cross out pure solids. Both $\ce{CaCO3(s)}$ and $\ce{CaO(s)}$ are solids (activity $= 1$); they leave. Only the gas $\ce{CO2}$ survives.

$$K_c = [\ce{CO2}]$$

**Answer:** $K_c = [\ce{CO2}]$. The equilibrium depends *only* on the $\ce{CO2}$ concentration — a striking result that surprises everyone the first time.

### Example 3: The Water Trap

**Problem:** Write $K_c$ for each: (a) $\ce{H2O(l) <=> H+(aq) + OH-(aq)}$ and (b) $\ce{H2(g) + CO2(g) <=> H2O(g) + CO(g)}$.

**Solution:**

- **(a)** Water is a **pure liquid** here — omit it. $K_c = [\ce{H+}][\ce{OH-}]$.
- **(b)** Water is a **gas** here — keep it. All four species are gases.

$$K_c^{(b)} = \frac{[\ce{H2O}]\,[\ce{CO}]}{[\ce{H2}]\,[\ce{CO2}]}$$

**Answer:** (a) $K_c = [\ce{H+}][\ce{OH-}]$; (b) $K_c = \dfrac{[\ce{H2O}][\ce{CO}]}{[\ce{H2}][\ce{CO2}]}$. Same molecule, opposite treatment — the phase label is everything.

### Example 4: Compute $K_c$ from Equilibrium Concentrations

**Problem:** For $\ce{H2(g) + I2(g) <=> 2HI(g)}$, the equilibrium concentrations are $[\ce{H2}] = 0.020$ M, $[\ce{I2}] = 0.020$ M, and $[\ce{HI}] = 0.140$ M. Find $K_c$.

**Solution:**

- **Step 1** — Expression: $K_c = \dfrac{[\ce{HI}]^2}{[\ce{H2}][\ce{I2}]}$.
- **Step 2** — Plug in: $K_c = \dfrac{(0.140)^2}{(0.020)(0.020)} = \dfrac{0.0196}{0.00040}$.
- **Step 3** — Divide: $K_c = 49$.

**Answer:** $K_c = 49$ (unitless — we treat $K$ as dimensionless in AP Chem).

### Example 5: Compute $K_p$ from Equilibrium Pressures

**Problem:** For $\ce{2SO2(g) + O2(g) <=> 2SO3(g)}$, equilibrium partial pressures are $P_{\ce{SO2}} = 0.10$ atm, $P_{\ce{O2}} = 0.20$ atm, $P_{\ce{SO3}} = 2.0$ atm. Find $K_p$.

**Solution:**

- **Step 1** — $K_p = \dfrac{(P_{\ce{SO3}})^2}{(P_{\ce{SO2}})^2\,(P_{\ce{O2}})}$.
- **Step 2** — Plug in: $K_p = \dfrac{(2.0)^2}{(0.10)^2(0.20)} = \dfrac{4.0}{(0.010)(0.20)} = \dfrac{4.0}{0.0020}$.
- **Step 3** — Divide: $K_p = 2.0 \times 10^{3}$.

**Answer:** $K_p = 2.0 \times 10^{3}$ — large, so products ($\ce{SO3}$) are strongly favored.

### Example 6: Convert $K_c$ → $K_p$

**Problem:** For $\ce{N2(g) + 3H2(g) <=> 2NH3(g)}$ at $T = 500$ K, $K_c = 6.0 \times 10^{-2}$. Find $K_p$. ($R = 0.08206$.)

**Solution:**

- **Step 1** — Count $\Delta n$ (gas moles): products $= 2$, reactants $= 1 + 3 = 4$, so $\Delta n = 2 - 4 = -2$.
- **Step 2** — Apply $K_p = K_c(RT)^{\Delta n}$. Compute $RT = (0.08206)(500) = 41.03$.
- **Step 3** — $(RT)^{-2} = \dfrac{1}{(41.03)^2} = \dfrac{1}{1683} = 5.94 \times 10^{-4}$.
- **Step 4** — Multiply: $K_p = (6.0\times10^{-2})(5.94\times10^{-4}) = 3.6 \times 10^{-5}$.

**Answer:** $K_p = 3.6 \times 10^{-5}$. Since $\Delta n < 0$, $K_p < K_c$, as expected.

### Example 7: Convert $K_p$ → $K_c$

**Problem:** For $\ce{2NO2(g) <=> N2O4(g)}$ at $298$ K, $K_p = 6.7$. Find $K_c$.

**Solution:**

- **Step 1** — $\Delta n = 1 - 2 = -1$.
- **Step 2** — Rearrange $K_p = K_c(RT)^{\Delta n}$ for $K_c$: $K_c = \dfrac{K_p}{(RT)^{\Delta n}} = K_p\,(RT)^{-\Delta n} = K_p\,(RT)^{+1}$.
- **Step 3** — $RT = (0.08206)(298) = 24.5$.
- **Step 4** — $K_c = (6.7)(24.5) = 1.6 \times 10^{2}$.

**Answer:** $K_c = 1.6 \times 10^{2}$. (Flipping the sign in the exponent when solving for $K_c$ is the step people miss.)

### Example 8: Interpret the Magnitude of $K$

**Problem:** Three reactions have $K = 3 \times 10^{8}$, $K = 1.5$, and $K = 4 \times 10^{-12}$. For each, state whether products or reactants dominate at equilibrium.

**Solution:**

- $K = 3\times10^{8} \gg 1$ → **products strongly favored** (bowl tilted hard toward products).
- $K = 1.5 \approx 1$ → **significant amounts of both** reactants and products.
- $K = 4\times10^{-12} \ll 1$ → **reactants strongly favored**; the reaction barely proceeds.

**Answer:** Products; both; reactants — reading straight off the exponent's sign and size.

### Example 9: Reverse a Reaction

**Problem:** For $\ce{N2(g) + 3H2(g) <=> 2NH3(g)}$, $K = 6.0 \times 10^{-2}$. Find $K$ for the reverse reaction $\ce{2NH3(g) <=> N2(g) + 3H2(g)}$.

**Solution:**

- **Step 1** — Reversing inverts $K$: $K_\text{rev} = \dfrac{1}{K}$.
- **Step 2** — $K_\text{rev} = \dfrac{1}{6.0\times10^{-2}} = 16.7$.

**Answer:** $K_\text{rev} = 17$ (2 sig figs). Notice a small $K$ forward becomes a large $K$ reverse.

### Example 10: Scale the Coefficients

**Problem:** For $\ce{N2(g) + 3H2(g) <=> 2NH3(g)}$, $K = 6.0 \times 10^{-2}$. Find $K$ for the halved reaction $\ce{1/2 N2(g) + 3/2 H2(g) <=> NH3(g)}$.

**Solution:**

- **Step 1** — All coefficients are multiplied by $n = \tfrac{1}{2}$, so raise $K$ to the $\tfrac{1}{2}$ (take the square root).
- **Step 2** — $K_\text{new} = (6.0\times10^{-2})^{1/2} = \sqrt{0.060} = 0.245$.

**Answer:** $K_\text{new} = 0.24$.

### Example 11: Add Reactions (Multiply $K$'s)

**Problem:** Given
$$\ce{A <=> B}\quad K_1 = 2.0 \qquad \ce{B <=> C}\quad K_2 = 5.0$$
find $K$ for the overall reaction $\ce{A <=> C}$.

**Solution:**

- **Step 1** — Add the two reactions: $\ce{A <=> B}$ plus $\ce{B <=> C}$ gives $\ce{A <=> C}$ (the $\ce{B}$ cancels, appearing as product then reactant).
- **Step 2** — Adding reactions means multiplying $K$'s: $K_\text{overall} = K_1 \times K_2 = (2.0)(5.0)$.

$$K_\text{overall} = 10$$

**Answer:** $K_\text{overall} = 10$.

### Example 12: A Combined Manipulation

**Problem:** For $\ce{2SO2(g) + O2(g) <=> 2SO3(g)}$, $K = 100$. Find $K$ for $\ce{SO3(g) <=> SO2(g) + 1/2 O2(g)}$.

**Solution:**

- **Step 1** — The target is the **reverse** of the original *and* **halved**. Do it in two moves.
- **Step 2** — Reverse first: $K_\text{rev} = \dfrac{1}{100} = 0.010$.
- **Step 3** — Then halve (raise to $\tfrac{1}{2}$): $K_\text{final} = (0.010)^{1/2} = \sqrt{0.010} = 0.10$.

**Answer:** $K_\text{final} = 0.10$. (Order doesn't matter: squaring/rooting and inverting commute — you'd get the same number reversing the order.)

### Example 13: Predict the Direction with $Q$ vs. $K$

**Problem:** For $\ce{H2(g) + I2(g) <=> 2HI(g)}$, $K_c = 49$. A flask currently holds $[\ce{H2}] = 0.10$ M, $[\ce{I2}] = 0.10$ M, $[\ce{HI}] = 0.10$ M. Which way does the reaction shift?

**Solution:**

- **Step 1** — Compute $Q$ with current values: $Q = \dfrac{[\ce{HI}]^2}{[\ce{H2}][\ce{I2}]} = \dfrac{(0.10)^2}{(0.10)(0.10)} = \dfrac{0.010}{0.010} = 1.0$.
- **Step 2** — Compare: $Q = 1.0 < K = 49$, so $Q < K$.
- **Step 3** — $Q < K$ means "not enough product yet" → shifts **forward** to make more $\ce{HI}$.

**Answer:** $Q = 1.0 < K = 49$, so the reaction shifts **forward (toward products)**. The marble is up the reactant wall and rolls right.

### Example 14: $Q$ vs. $K$ the Other Direction

**Problem:** For $\ce{2NO2(g) <=> N2O4(g)}$, $K_p = 6.7$. Right now $P_{\ce{NO2}} = 0.20$ atm and $P_{\ce{N2O4}} = 2.0$ atm. Which way does it shift?

**Solution:**

- **Step 1** — $Q_p = \dfrac{P_{\ce{N2O4}}}{(P_{\ce{NO2}})^2} = \dfrac{2.0}{(0.20)^2} = \dfrac{2.0}{0.040} = 50$.
- **Step 2** — Compare: $Q_p = 50 > K_p = 6.7$, so $Q > K$.
- **Step 3** — $Q > K$ means "too much product" → shifts **reverse** to remake $\ce{NO2}$.

**Answer:** $Q > K$, so the reaction shifts **reverse (toward reactants)**.

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Including solids/liquids in $K$ | You write products-over-reactants mechanically and forget to check phases | Circle every $(s)$ and $(l)$ in the equation *first*, then cross them out of the expression |
| Dropping $\ce{H2O(g)}$ because "water is always omitted" | Overgeneralizing the water rule | Only pure **liquid** water is omitted; gaseous water $\ce{H2O(g)}$ stays in |
| Forgetting coefficients as exponents | Rushing the expression | Write the coefficient as a superscript *as you place each species* |
| Using $R = 8.314$ in $K_p = K_c(RT)^{\Delta n}$ | Confusing the two gas constants | Pressures are in atm, so use $R = 0.08206\ \frac{\text{L·atm}}{\text{mol·K}}$ |
| Counting $\Delta n$ over all species | Forgetting only gases matter | $\Delta n$ = moles of **gas** products − **gas** reactants; ignore $(s)$, $(l)$, $(aq)$ |
| Reversing gives $-K$ instead of $1/K$ | Confusing with Hess's Law's sign flip | $K$ is a *ratio* — reversing **inverts** it ($1/K$); it's never negative |
| Adding $K$'s when combining reactions | Copying the Hess's Law "add" habit | Adding reactions → **multiply** the $K$'s; only $\Delta H$ gets added |
| Thinking a big $K$ means a fast reaction | Confusing amount with speed | $K$ = position of rest (Unit 7); rate = kinetics (Unit 5). They're unrelated |
| Using non-equilibrium values in $K$ | Not noticing the numbers are "right now" | If the problem says *current* or *initial*, you're computing $Q$, not $K$ |

---

## AP Exam Tips

- **Omit pure solids and pure liquids from every $K$ (and $Q$) expression.** Their activity is 1. This is tested almost every year — losing it is losing free points. Aqueous and gas species only.
- **Memorize $K_p = K_c(RT)^{\Delta n}$**, with $\Delta n = $ (moles gas products) − (moles gas reactants) and $R = 0.08206$. If $\Delta n = 0$, then $K_p = K_c$.
- **Know the three manipulation rules cold:** reverse → $\tfrac{1}{K}$; scale by $n$ → $K^n$; add reactions → multiply $K$'s. These show up as multi-step MCQs and as parts of FRQs.
- **$Q$ vs. $K$ predicts direction:** $Q < K$ shifts **forward** (right, toward products); $Q > K$ shifts **reverse** (left); $Q = K$ is equilibrium. Always compute $Q$ and compare — don't guess.
- **$K$ says NOTHING about rate.** If a free-response asks "will products form quickly?", the magnitude of $K$ is *not* the answer — that's kinetics. Watch for this trap.
- **$K$ is unitless in AP Chem.** Don't attach units to your answer; report the bare number (often in scientific notation).
- **On the calculator:** for scaling with fractional $n$, remember halving = square root and doubling = squaring. Show the setup — FRQ points come from the correct expression even if arithmetic slips.

---

## Practice Problems

### Problem 1
Write the $K_c$ expression for $\ce{2NO(g) + O2(g) <=> 2NO2(g)}$.

<details>
<summary><strong>Solution</strong></summary>

Products over reactants, coefficients as exponents:

$$K_c = \frac{[\ce{NO2}]^2}{[\ce{NO}]^2\,[\ce{O2}]}$$

**Answer:** $K_c = \dfrac{[\ce{NO2}]^2}{[\ce{NO}]^2[\ce{O2}]}$

</details>

---

### Problem 2
Write the $K_c$ expression for $\ce{Fe3O4(s) + 4H2(g) <=> 3Fe(s) + 4H2O(g)}$.

<details>
<summary><strong>Solution</strong></summary>

Cross out both solids ($\ce{Fe3O4}$ and $\ce{Fe}$). Only the two gases remain:

$$K_c = \frac{[\ce{H2O}]^4}{[\ce{H2}]^4}$$

**Answer:** $K_c = \dfrac{[\ce{H2O}]^4}{[\ce{H2}]^4}$

</details>

---

### Problem 3
Write $K_c$ for the dissolving of silver chloride: $\ce{AgCl(s) <=> Ag+(aq) + Cl-(aq)}$.

<details>
<summary><strong>Solution</strong></summary>

$\ce{AgCl}$ is a pure solid — omit it. The products are aqueous ions, which stay:

$$K_c = [\ce{Ag+}][\ce{Cl-}]$$

**Answer:** $K_c = [\ce{Ag+}][\ce{Cl-}]$ (this special $K$ is called $K_{sp}$, coming in a later article).

</details>

---

### Problem 4
For $\ce{PCl5(g) <=> PCl3(g) + Cl2(g)}$, equilibrium concentrations are $[\ce{PCl5}] = 0.010$ M, $[\ce{PCl3}] = 0.15$ M, $[\ce{Cl2}] = 0.15$ M. Calculate $K_c$.

<details>
<summary><strong>Solution</strong></summary>

$$K_c = \frac{[\ce{PCl3}][\ce{Cl2}]}{[\ce{PCl5}]} = \frac{(0.15)(0.15)}{0.010} = \frac{0.0225}{0.010} = 2.25$$

**Answer:** $K_c = 2.3$

</details>

---

### Problem 5
For $\ce{N2O4(g) <=> 2NO2(g)}$, equilibrium partial pressures are $P_{\ce{N2O4}} = 0.75$ atm and $P_{\ce{NO2}} = 0.50$ atm. Find $K_p$.

<details>
<summary><strong>Solution</strong></summary>

$$K_p = \frac{(P_{\ce{NO2}})^2}{P_{\ce{N2O4}}} = \frac{(0.50)^2}{0.75} = \frac{0.25}{0.75} = 0.33$$

**Answer:** $K_p = 0.33$

</details>

---

### Problem 6
For $\ce{CO(g) + Cl2(g) <=> COCl2(g)}$ at $T = 600$ K, $K_c = 1.2 \times 10^{3}$. Find $K_p$. ($R = 0.08206$.)

<details>
<summary><strong>Solution</strong></summary>

$\Delta n = 1 - 2 = -1$. Then $RT = (0.08206)(600) = 49.2$.

$$K_p = K_c(RT)^{\Delta n} = (1.2\times10^{3})(49.2)^{-1} = \frac{1.2\times10^{3}}{49.2} = 24$$

**Answer:** $K_p = 24$. Since $\Delta n < 0$, $K_p < K_c$, as expected.

</details>

---

### Problem 7
For $\ce{2H2(g) + O2(g) <=> 2H2O(g)}$ at $500$ K, $K_p = 5.0 \times 10^{2}$. Find $K_c$. ($R = 0.08206$.)

<details>
<summary><strong>Solution</strong></summary>

$\Delta n = 2 - 3 = -1$. Solve for $K_c$: $K_c = K_p\,(RT)^{+1}$ (sign flips when isolating $K_c$).

$RT = (0.08206)(500) = 41.03$, so

$$K_c = (5.0\times10^{2})(41.03) = 2.1 \times 10^{4}$$

**Answer:** $K_c = 2.1 \times 10^{4}$

</details>

---

### Problem 8
A reaction has $K = 2 \times 10^{-9}$. Describe the equilibrium mixture, and state whether this tells you the reaction is slow.

<details>
<summary><strong>Solution</strong></summary>

$K = 2\times10^{-9} \ll 1$, so at equilibrium the mixture is **almost entirely reactants** — the reaction barely proceeds. It tells you **nothing** about speed: $K$ is about the position of equilibrium (Unit 7), not the rate (Unit 5). A reaction with a tiny $K$ could still reach that equilibrium quickly or slowly.

**Answer:** Reactant-dominated equilibrium; magnitude says nothing about rate.

</details>

---

### Problem 9
For $\ce{2SO3(g) <=> 2SO2(g) + O2(g)}$, $K = 4.0 \times 10^{-3}$. Find $K$ for the reverse reaction $\ce{2SO2(g) + O2(g) <=> 2SO3(g)}$.

<details>
<summary><strong>Solution</strong></summary>

Reversing inverts $K$:

$$K_\text{rev} = \frac{1}{4.0\times10^{-3}} = 2.5 \times 10^{2}$$

**Answer:** $K_\text{rev} = 2.5 \times 10^{2}$

</details>

---

### Problem 10
For $\ce{N2(g) + O2(g) <=> 2NO(g)}$, $K = 1.0 \times 10^{-5}$. Find $K$ for $\ce{2N2(g) + 2O2(g) <=> 4NO(g)}$.

<details>
<summary><strong>Solution</strong></summary>

All coefficients are doubled, so $n = 2$: raise $K$ to the 2nd power.

$$K_\text{new} = (1.0\times10^{-5})^2 = 1.0 \times 10^{-10}$$

**Answer:** $K_\text{new} = 1.0 \times 10^{-10}$

</details>

---

### Problem 11
Given $\ce{C(s) + O2(g) <=> CO2(g)}$ with $K_1 = 1 \times 10^{69}$ and $\ce{2CO(g) + O2(g) <=> 2CO2(g)}$ with $K_2 = 1 \times 10^{90}$, find $K$ for $\ce{2C(s) + O2(g) <=> 2CO(g)}$.

<details>
<summary><strong>Solution</strong></summary>

Target = (reaction 1 doubled) + (reaction 2 reversed).

- Double reaction 1: $\ce{2C(s) + 2O2(g) <=> 2CO2(g)}$, $K = (K_1)^2 = 1\times10^{138}$.
- Reverse reaction 2: $\ce{2CO2(g) <=> 2CO(g) + O2(g)}$, $K = 1/K_2 = 1\times10^{-90}$.
- Add them ($\ce{2CO2}$ and one $\ce{O2}$ cancel) → multiply the $K$'s:

$$K = (1\times10^{138})(1\times10^{-90}) = 1 \times 10^{48}$$

**Answer:** $K = 1 \times 10^{48}$

</details>

---

### Problem 12
For $\ce{H2(g) + I2(g) <=> 2HI(g)}$, $K_c = 50$. A flask contains $[\ce{H2}] = 0.20$ M, $[\ce{I2}] = 0.20$ M, $[\ce{HI}] = 2.0$ M. Compute $Q$ and predict the direction of shift.

<details>
<summary><strong>Solution</strong></summary>

$$Q = \frac{[\ce{HI}]^2}{[\ce{H2}][\ce{I2}]} = \frac{(2.0)^2}{(0.20)(0.20)} = \frac{4.0}{0.040} = 100$$

$Q = 100 > K = 50$, so $Q > K$ → shifts **reverse (toward reactants)** to lower $Q$.

**Answer:** $Q = 100 > K$; shifts reverse.

</details>

---

### Problem 13
For $\ce{PCl5(g) <=> PCl3(g) + Cl2(g)}$, $K_c = 1.8$. Currently $[\ce{PCl5}] = 0.50$ M, $[\ce{PCl3}] = 0.30$ M, $[\ce{Cl2}] = 0.30$ M. Which way does the reaction shift?

<details>
<summary><strong>Solution</strong></summary>

$$Q = \frac{[\ce{PCl3}][\ce{Cl2}]}{[\ce{PCl5}]} = \frac{(0.30)(0.30)}{0.50} = \frac{0.090}{0.50} = 0.18$$

$Q = 0.18 < K = 1.8$, so $Q < K$ → shifts **forward (toward products)**.

**Answer:** $Q = 0.18 < K$; shifts forward.

</details>

---

### Problem 14
At a certain moment for $\ce{2NO2(g) <=> N2O4(g)}$ ($K_p = 6.7$), $P_{\ce{NO2}} = 0.40$ atm and $P_{\ce{N2O4}} = 1.07$ atm. Is the system at equilibrium? If not, which way does it shift?

<details>
<summary><strong>Solution</strong></summary>

$$Q_p = \frac{P_{\ce{N2O4}}}{(P_{\ce{NO2}})^2} = \frac{1.07}{(0.40)^2} = \frac{1.07}{0.16} = 6.7$$

$Q_p = 6.7 = K_p$, so the system **is at equilibrium** — no net shift. The marble is already at rest.

**Answer:** At equilibrium ($Q = K$); no shift.

</details>

---

### Problem 15
Water gas shift: $\ce{CO(g) + H2O(g) <=> CO2(g) + H2(g)}$, $K_c = 5.0$. (a) Write $K_c$. (b) At $[\ce{CO}] = 0.20$, $[\ce{H2O}] = 0.20$, $[\ce{CO2}] = 0.40$, $[\ce{H2}] = 0.40$ M, find $Q$ and the direction. (c) Explain why $K_p = K_c$ for this reaction.

<details>
<summary><strong>Solution</strong></summary>

**(a)** All four are gases:
$$K_c = \frac{[\ce{CO2}][\ce{H2}]}{[\ce{CO}][\ce{H2O}]}$$

**(b)** $Q = \dfrac{(0.40)(0.40)}{(0.20)(0.20)} = \dfrac{0.16}{0.040} = 4.0$. Since $Q = 4.0 < K = 5.0$, shifts **forward (toward products)**.

**(c)** $\Delta n = 2 - 2 = 0$, so $K_p = K_c(RT)^0 = K_c$. Equal moles of gas on both sides means the two constants coincide.

**Answer:** (a) as above; (b) $Q = 4.0 < K$, forward; (c) $\Delta n = 0 \Rightarrow K_p = K_c$.

</details>

---

## Quick Reference

| Concept | Formula / Rule |
|---|---|
| $K_c$ expression | $K_c = \dfrac{[\ce{C}]^c[\ce{D}]^d}{[\ce{A}]^a[\ce{B}]^b}$ (products/reactants, coefficients as exponents) |
| Omit from $K$ | pure solids $(s)$ and pure liquids $(l)$ — activity $= 1$ |
| Include in $K$ | gases $(g)$ and aqueous species $(aq)$ |
| $K_p$ | same template with partial pressures $P_{\ce{X}}$ |
| $K_c \leftrightarrow K_p$ | $K_p = K_c(RT)^{\Delta n}$, $\ \Delta n = $ mol gas products − reactants, $R = 0.08206$ |
| $K \gg 1$ | products favored (bowl tilts toward products) |
| $K \ll 1$ | reactants favored (bowl tilts toward reactants) |
| $K \approx 1$ | significant amounts of both |
| $K$ tells you | position of equilibrium — **NOT** rate |
| Reverse reaction | $K \to \dfrac{1}{K}$ |
| Scale by $n$ | $K \to K^{n}$ (halve → $\sqrt{K}$; double → $K^2$) |
| Add reactions | $K_\text{overall} = K_1 \times K_2$ |
| Reaction quotient | $Q$: same expression, **current** values |
| $Q < K$ | shifts **forward** (→ products) |
| $Q > K$ | shifts **reverse** (→ reactants) |
| $Q = K$ | at equilibrium (no shift) |

---

<div align="center">

[← Introduction to Equilibrium](/chemistry/0901-introduction-to-equilibrium) | [ICE Tables →](/chemistry/0903-ice-tables)

</div>
