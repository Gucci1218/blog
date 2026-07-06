# Solubility Equilibria and Ksp
<p class="article-date">July 5, 2026</p>

*Last weekend my little cousin wanted to make rock candy, so we stirred sugar into a jar of iced tea to build the syrup. The first spoonful vanished instantly. So did the second, and the fifth. It felt like the tea could swallow sugar forever — until, somewhere around the tenth spoon, it stopped. Suddenly the extra sugar just drifted to the bottom and sat there in a little white dune, no matter how hard I stirred. The tea was "full." That full point has a real name: the solution is **saturated**, and it's not that dissolving stopped — it's that sugar is now dissolving and re-crystallizing at exactly the same rate, a solid-and-dissolved standoff. That's a **solubility equilibrium**. A few days later, as the jar slowly cooled and evaporated, that same sugar came marching back out of solution and grew into crystals on the string we'd hung inside — dissolving run in reverse, which is **precipitation**. This article is about pinning that saturation point down with a single number, $K_{sp}$, for the slightly-soluble ionic salts AP loves. It's the capstone of Unit 7 — equilibrium applied to the simple, physical act of something dissolving.*

---

## What You'll Learn
- Write the **solubility-product expression** $K_{sp}$ for any slightly-soluble salt, and explain why the solid is left out
- Set up an **ICE table** for a dissolving salt and convert between $K_{sp}$ and **molar solubility** in *both* directions
- Handle the coefficient-power trap correctly (why $\ce{CaF2}$ gives $K_{sp} = 4s^3$, not $s^2$)
- Convert molar solubility to grams per liter using molar mass
- Explain why you **cannot** rank solubility by comparing $K_{sp}$ values across salts with different formulas — and compute $s$ to do it right
- Use the **ion product $Q$** versus $K_{sp}$ to predict whether a precipitate forms when two solutions are mixed (including the dilution step)
- Apply the **common-ion effect**: predict and calculate how a shared ion decreases solubility (Le Chatelier)
- Reason about **pH and solubility** — why salts of basic anions dissolve more in acid, and why $\ce{AgCl}$ doesn't care about pH
- Connect dissolving to **free energy** ($\Delta G^\circ = -RT\ln K$) as a preview of Unit 9

---

## Prerequisites
- [The Equilibrium Constant](/chemistry/0902-equilibrium-constant) — $K_{sp}$ is just an equilibrium constant for a dissolving reaction, and the "pure solids are left out" rule comes straight from here
- [ICE Tables](/chemistry/0903-ice-tables) — every $K_{sp}$ ↔ solubility calculation is an ICE table, just with a solid on the left instead of a gas
- [Le Chatelier's Principle](/chemistry/0904-le-chatelier) — the common-ion effect and the pH-and-solubility rules are pure Le Chatelier shifts on a dissolving equilibrium

---

## The Core Concept

### Intuition First

Go back to that jar of iced tea. When I dropped in the first spoon of sugar, every grain dissolved because the tea was nowhere near full — there was tons of room. But dissolving isn't a one-way street. The instant sugar molecules are floating around dissolved, some of them randomly bump back into the undissolved pile and stick again. Early on, dissolving *wins* by a landslide, so the pile shrinks. But as the tea fills up with dissolved sugar, the re-sticking speeds up. Eventually the two rates match:

$$\text{sugar}(s) \; \ce{<=>} \; \text{sugar}(aq)$$

Now the pile at the bottom stops changing. Not because nothing's happening — sugar is *still* dissolving and *still* re-crystallizing every second — but because those two happen at the **same rate**. That balanced standoff is the **saturation point**, and it is a genuine dynamic equilibrium, exactly like every equilibrium from the last four articles.

For slightly-soluble **ionic salts** — think $\ce{AgCl}$, $\ce{CaF2}$, $\ce{Mg(OH)2}$ — the exact same thing happens, with one twist: the salt splits into *ions* when it dissolves. Silver chloride sitting at the bottom of a beaker is doing this:

$$\ce{AgCl(s) <=> Ag+(aq) + Cl-(aq)}$$

Here's the structural map I want you to carry through the whole article:

| The rock-candy jar | The chemistry |
|---|---|
| Sugar dissolving until no more will go in | $\ce{solid <=> dissolved ions}$ at equilibrium |
| The "full" point where extra sugar won't dissolve | the **solubility limit** (saturation) |
| The undissolved dune at the bottom | the **pure solid** — left out of $K_{sp}$ |
| Crystals growing back on the string | **precipitation** — the reverse of dissolving |
| "How much sugar fits before it's full?" | **molar solubility**, $s$ |

The number that pins down *how full* a salt's solution gets is the **solubility product**, $K_{sp}$. That's the whole topic.

### The Solubility Product $K_{sp}$

For a general salt dissolving into ions:

$$\ce{M_xX_y(s) <=> \mathnormal{x}\, M^+(aq) + \mathnormal{y}\, X^-(aq)}$$

the equilibrium constant is written using only the dissolved ions:

$$\boxed{\,K_{sp} = [\ce{M+}]^x\,[\ce{X-}]^y\,}$$

Two things to notice, both familiar from [The Equilibrium Constant](/chemistry/0902-equilibrium-constant):

1. **The solid is not in the expression.** A pure solid has no meaningful "concentration" — its activity is 1 — so $\ce{M_xX_y(s)}$ never appears. That undissolved dune at the bottom of the jar? It doesn't get a term. (This is also *why* adding more solid to a saturated solution changes nothing: you can't push on a term that isn't there.)
2. **The ion coefficients become exponents**, just like any $K$ expression.

A small $K_{sp}$ means the salt barely dissolves (equilibrium sits far left, mostly solid). A larger $K_{sp}$ means more dissolves before the solution fills up. Every salt on the AP $K_{sp}$ table is "slightly soluble" — the ones that dissolve freely (like $\ce{NaCl}$) don't get a $K_{sp}$ because they never reach this kind of equilibrium at normal concentrations.

**Writing $K_{sp}$ expressions — a few salts:**

| Salt | Dissolution equation | $K_{sp}$ expression |
|---|---|---|
| $\ce{AgCl}$ | $\ce{AgCl(s) <=> Ag+ + Cl-}$ | $[\ce{Ag+}][\ce{Cl-}]$ |
| $\ce{CaF2}$ | $\ce{CaF2(s) <=> Ca^2+ + 2F-}$ | $[\ce{Ca^2+}][\ce{F-}]^2$ |
| $\ce{Ag2CrO4}$ | $\ce{Ag2CrO4(s) <=> 2Ag+ + CrO4^2-}$ | $[\ce{Ag+}]^2[\ce{CrO4^2-}]$ |
| $\ce{Mg(OH)2}$ | $\ce{Mg(OH)2(s) <=> Mg^2+ + 2OH-}$ | $[\ce{Mg^2+}][\ce{OH-}]^2$ |
| $\ce{Ca3(PO4)2}$ | $\ce{Ca3(PO4)2(s) <=> 3Ca^2+ + 2PO4^3-}$ | $[\ce{Ca^2+}]^3[\ce{PO4^3-}]^2$ |

### Molar Solubility vs. $K_{sp}$ — Two Different Numbers

This is the distinction students blur, so nail it now:

- **Molar solubility** ($s$) = how many **moles of the salt** dissolve per liter to make a saturated solution. Units: $\text{mol/L}$. It's the "how much fits" number.
- $K_{sp}$ = the equilibrium constant, a pure number built from the *ion* concentrations.

They're related but not equal, and the bridge between them is an ICE table. When $s$ moles of $\ce{CaF2}$ dissolve, they release $s$ moles of $\ce{Ca^2+}$ **and $2s$ moles of $\ce{F-}$** — the coefficients ride along. That's the whole reason $K_{sp}$ and $s$ aren't the same, and it's where the exponents bite.

Here's the general shape of every one of these calculations, using an ICE table (the solid gets no column):

| | $\ce{CaF2(s)}$ | $\ce{Ca^2+}$ | $\ce{2F-}$ |
|---|---|---|---|
| **I**nitial | — | $0$ | $0$ |
| **C**hange | — | $+s$ | $+2s$ |
| **E**quilibrium | — | $s$ | $2s$ |

Then plug into $K_{sp}$:

$$K_{sp} = [\ce{Ca^2+}][\ce{F-}]^2 = (s)(2s)^2 = 4s^3$$

That $(2s)^2 = 4s^2$ is the single most-missed step in the whole topic. **The 2 gets squared too.** Here's the shortcut table for the common formula types:

| Salt type | Example | $K_{sp}$ in terms of $s$ | Solve for $s$ |
|---|---|---|---|
| 1:1 ($\ce{MX}$) | $\ce{AgCl}$ | $s^2$ | $s=\sqrt{K_{sp}}$ |
| 1:2 or 2:1 ($\ce{MX2},\,\ce{M2X}$) | $\ce{CaF2},\,\ce{Ag2CrO4}$ | $4s^3$ | $s=\sqrt[3]{K_{sp}/4}$ |
| 1:3 or 3:1 | $\ce{AlF3}$ (approx.) | $27s^4$ | $s=\sqrt[4]{K_{sp}/27}$ |
| 3:2 | $\ce{Ca3(PO4)2}$ | $108s^5$ | $s=\sqrt[5]{K_{sp}/108}$ |

### The Ion Product $Q$: Will It Precipitate?

The rock candy grew back on the string when the cooling syrup got *too* full — more sugar dissolved than the tea could hold, so the excess crashed out. For ionic salts we predict that crash with the **ion product $Q_{sp}$**: the exact same formula as $K_{sp}$, but using the concentrations you *actually have right now* (not necessarily equilibrium ones). Then compare:

| Comparison | Meaning | What happens |
|---|---|---|
| $Q < K_{sp}$ | fewer ions than saturation allows | **unsaturated** — no precipitate; more could dissolve |
| $Q = K_{sp}$ | exactly at saturation | **saturated** — at equilibrium, no change |
| $Q > K_{sp}$ | more ions than can stay dissolved | **supersaturated** — a **precipitate forms** until $Q$ drops back to $K_{sp}$ |

This is just $Q$ vs $K$ from equilibrium, wearing a solubility costume. The one extra wrinkle: when you **mix two solutions**, each one dilutes the other, so you must recompute the concentrations for the new combined volume *before* plugging into $Q$.

### Free Energy Preview

We'll fully unpack this in Unit 9, but here's the one-line connection: dissolving is a favorability question, and $K_{sp}$ *is* that favorability written as a number. The bridge is

$$\Delta G^\circ_{\text{dissolution}} = -RT\ln K_{sp}$$

Since every $K_{sp}$ on the table is much less than 1, $\ln K_{sp}$ is negative, which makes $\Delta G^\circ$ **positive** — dissolving these salts is nonspontaneous under standard conditions, which is exactly why they're "slightly soluble." Hold that thought; we cash it out in [Free Energy and Equilibrium](/chemistry/1103-free-energy-equilibrium).

---

## Worked Examples

### Example 1: Writing $K_{sp}$ Expressions

**Problem:** Write the balanced dissolution equation and $K_{sp}$ expression for (a) $\ce{BaSO4}$, (b) $\ce{Mg(OH)2}$, and (c) $\ce{Ca3(PO4)2}$.

**Solution:**

**(a)** $\ce{BaSO4}$ splits into one $\ce{Ba^2+}$ and one $\ce{SO4^2-}$:
$$\ce{BaSO4(s) <=> Ba^2+ + SO4^2-} \qquad K_{sp} = [\ce{Ba^2+}][\ce{SO4^2-}]$$

**(b)** $\ce{Mg(OH)2}$ gives one $\ce{Mg^2+}$ and **two** $\ce{OH-}$:
$$\ce{Mg(OH)2(s) <=> Mg^2+ + 2OH-} \qquad K_{sp} = [\ce{Mg^2+}][\ce{OH-}]^2$$

**(c)** $\ce{Ca3(PO4)2}$ gives three $\ce{Ca^2+}$ and two $\ce{PO4^3-}$:
$$\ce{Ca3(PO4)2(s) <=> 3Ca^2+ + 2PO4^3-} \qquad K_{sp} = [\ce{Ca^2+}]^3[\ce{PO4^3-}]^2$$

**Answer:** Expressions above; note the solid never appears and each coefficient becomes an exponent.

---

### Example 2: $K_{sp}$ → Molar Solubility (1:1 salt)

**Problem:** $\ce{AgCl}$ has $K_{sp} = 1.8 \times 10^{-10}$. Find its molar solubility in pure water.

**Solution:**

**Step 1 — ICE.** $\ce{AgCl(s) <=> Ag+ + Cl-}$. If $s$ mol/L dissolves, then $[\ce{Ag+}] = s$ and $[\ce{Cl-}] = s$.

**Step 2 — Plug in.**
$$K_{sp} = [\ce{Ag+}][\ce{Cl-}] = (s)(s) = s^2 = 1.8 \times 10^{-10}$$

**Step 3 — Solve.**
$$s = \sqrt{1.8 \times 10^{-10}} = 1.3 \times 10^{-5}\ \text{mol/L}$$

**Answer:** $s = 1.3 \times 10^{-5}\ \text{M}$. Only about 13 millionths of a mole dissolves per liter — genuinely "slightly soluble."

---

### Example 3: $K_{sp}$ → Molar Solubility (the $4s^3$ type)

**Problem:** $\ce{CaF2}$ has $K_{sp} = 3.9 \times 10^{-11}$. Find its molar solubility.

**Solution:**

**Step 1 — ICE.** $\ce{CaF2(s) <=> Ca^2+ + 2F-}$, so $[\ce{Ca^2+}] = s$ and $[\ce{F-}] = 2s$.

**Step 2 — Plug in, and square the whole $2s$.**
$$K_{sp} = [\ce{Ca^2+}][\ce{F-}]^2 = (s)(2s)^2 = (s)(4s^2) = 4s^3$$

**Step 3 — Solve.**
$$4s^3 = 3.9 \times 10^{-11} \;\Rightarrow\; s^3 = 9.75 \times 10^{-12} \;\Rightarrow\; s = \sqrt[3]{9.75 \times 10^{-12}} = 2.1 \times 10^{-4}\ \text{M}$$

**Answer:** $s = 2.1 \times 10^{-4}\ \text{M}$. Watch the trap: if you'd forgotten to square the 2 you'd get $s^3 = K_{sp}$ and a wrong answer.

---

### Example 4: Molar Solubility → $K_{sp}$ (backward direction)

**Problem:** The molar solubility of $\ce{PbI2}$ is measured as $1.3 \times 10^{-3}\ \text{M}$. Calculate $K_{sp}$.

**Solution:**

**Step 1 — ICE.** $\ce{PbI2(s) <=> Pb^2+ + 2I-}$, so $[\ce{Pb^2+}] = s = 1.3 \times 10^{-3}$ and $[\ce{I-}] = 2s = 2.6 \times 10^{-3}$.

**Step 2 — Plug the actual numbers into $K_{sp}$.**
$$K_{sp} = [\ce{Pb^2+}][\ce{I-}]^2 = (1.3 \times 10^{-3})(2.6 \times 10^{-3})^2$$

**Step 3 — Compute.**
$$= (1.3 \times 10^{-3})(6.76 \times 10^{-6}) = 8.8 \times 10^{-9}$$

**Answer:** $K_{sp} = 8.8 \times 10^{-9}$. (Same $4s^3$ structure, run in reverse: $4(1.3\times10^{-3})^3$ gives the same value.)

---

### Example 5: Solubility in Grams per Liter

**Problem:** Using $s = 1.3 \times 10^{-5}\ \text{M}$ for $\ce{AgCl}$ (Example 2), express its solubility in grams per liter. ($M_{\ce{AgCl}} = 143.32\ \text{g/mol}$.)

**Solution:**

**Step 1 — Molar solubility is moles of *salt* per liter.** One mole of dissolved $\ce{AgCl}$ = one mole of formula units, so multiply by molar mass:
$$\left(1.3 \times 10^{-5}\ \frac{\text{mol}}{\text{L}}\right)\left(143.32\ \frac{\text{g}}{\text{mol}}\right)$$

**Step 2 — Compute.**
$$= 1.9 \times 10^{-3}\ \text{g/L}$$

**Answer:** About $1.9 \times 10^{-3}\ \text{g/L}$ — under 2 milligrams of $\ce{AgCl}$ per liter of water.

---

### Example 6: You Cannot Rank by $K_{sp}$ Alone

**Problem:** $\ce{AgCl}$ has $K_{sp} = 1.8 \times 10^{-10}$ and $\ce{Ag2CrO4}$ has $K_{sp} = 1.1 \times 10^{-12}$. Which is *more soluble*?

**Solution:**

**Step 1 — Resist the trap.** $\ce{Ag2CrO4}$ has the smaller $K_{sp}$, so it "should" be less soluble... but the two salts have **different formulas**, so their $K_{sp}$ expressions have different shapes. You must compute $s$ for each.

**Step 2 — $\ce{AgCl}$** (1:1): $s = \sqrt{1.8 \times 10^{-10}} = 1.3 \times 10^{-5}\ \text{M}$.

**Step 3 — $\ce{Ag2CrO4}$** (2:1): $\ce{Ag2CrO4(s) <=> 2Ag+ + CrO4^2-}$, so $K_{sp} = (2s)^2(s) = 4s^3$.
$$4s^3 = 1.1 \times 10^{-12} \;\Rightarrow\; s^3 = 2.75 \times 10^{-13} \;\Rightarrow\; s = 6.5 \times 10^{-5}\ \text{M}$$

**Step 4 — Compare the $s$ values.** $6.5 \times 10^{-5} > 1.3 \times 10^{-5}$.

**Answer:** $\ce{Ag2CrO4}$ is **more** soluble, even though it has the *smaller* $K_{sp}$. Comparing $K_{sp}$ directly is only valid for salts with identical formula types.

---

### Example 7: Predicting Precipitation with $Q$

**Problem:** $50.0\ \text{mL}$ of $1.0 \times 10^{-3}\ \text{M}\ \ce{AgNO3}$ is mixed with $50.0\ \text{mL}$ of $1.0 \times 10^{-3}\ \text{M}\ \ce{NaCl}$. Will $\ce{AgCl}$ (\,$K_{sp} = 1.8 \times 10^{-10}$\,) precipitate?

**Solution:**

**Step 1 — Account for dilution.** Total volume is now $100.0\ \text{mL}$, so each solution is diluted by half:
$$[\ce{Ag+}] = (1.0 \times 10^{-3})\cdot\frac{50.0}{100.0} = 5.0 \times 10^{-4}\ \text{M}$$
$$[\ce{Cl-}] = (1.0 \times 10^{-3})\cdot\frac{50.0}{100.0} = 5.0 \times 10^{-4}\ \text{M}$$

**Step 2 — Compute the ion product $Q$** with the actual mixed concentrations:
$$Q = [\ce{Ag+}][\ce{Cl-}] = (5.0 \times 10^{-4})(5.0 \times 10^{-4}) = 2.5 \times 10^{-7}$$

**Step 3 — Compare to $K_{sp}$.** $Q = 2.5 \times 10^{-7}$ is far larger than $K_{sp} = 1.8 \times 10^{-10}$, so $Q > K_{sp}$.

**Answer:** **Yes, $\ce{AgCl}$ precipitates.** There are more ions in solution than saturation allows, so silver chloride crashes out until $Q$ falls back to $K_{sp}$. (Forgetting the dilution — using $1.0\times10^{-3}$ directly — is the classic error here.)

---

### Example 8: A Mixing Case That Does *Not* Precipitate

**Problem:** $100.0\ \text{mL}$ of $2.0 \times 10^{-4}\ \text{M}\ \ce{Pb(NO3)2}$ is mixed with $100.0\ \text{mL}$ of $2.0 \times 10^{-4}\ \text{M}\ \ce{NaCl}$. Does $\ce{PbCl2}$ (\,$K_{sp} = 1.7 \times 10^{-5}$\,) form?

**Solution:**

**Step 1 — Dilute (each halved, total $200.0\ \text{mL}$).**
$$[\ce{Pb^2+}] = 1.0 \times 10^{-4}\ \text{M}, \qquad [\ce{Cl-}] = 1.0 \times 10^{-4}\ \text{M}$$

**Step 2 — Build $Q$ with the right exponent** ($\ce{PbCl2 <=> Pb^2+ + 2Cl-}$):
$$Q = [\ce{Pb^2+}][\ce{Cl-}]^2 = (1.0 \times 10^{-4})(1.0 \times 10^{-4})^2 = 1.0 \times 10^{-12}$$

**Step 3 — Compare.** $Q = 1.0 \times 10^{-12}$ is far *smaller* than $K_{sp} = 1.7 \times 10^{-5}$, so $Q < K_{sp}$.

**Answer:** **No precipitate.** The solution is unsaturated — it could hold much more $\ce{PbCl2}$ before crashing out.

---

### Example 9: Common-Ion Effect (calculation)

**Problem:** Compare the molar solubility of $\ce{AgCl}$ ($K_{sp} = 1.8 \times 10^{-10}$) in pure water versus in $0.10\ \text{M}\ \ce{NaCl}$.

**Solution:**

**Step 1 — Pure water** (from Example 2): $s = 1.3 \times 10^{-5}\ \text{M}$.

**Step 2 — In $0.10\ \text{M}\ \ce{NaCl}$, set up the ICE with a head start of $\ce{Cl-}$.** The $\ce{NaCl}$ already supplies $0.10\ \text{M}\ \ce{Cl-}$ before any $\ce{AgCl}$ dissolves:

| | $\ce{AgCl(s)}$ | $\ce{Ag+}$ | $\ce{Cl-}$ |
|---|---|---|---|
| I | — | $0$ | $0.10$ |
| C | — | $+s$ | $+s$ |
| E | — | $s$ | $0.10 + s$ |

**Step 3 — Plug in and approximate.** Because $\ce{AgCl}$ barely dissolves, $s \ll 0.10$, so $0.10 + s \approx 0.10$:
$$K_{sp} = (s)(0.10 + s) \approx (s)(0.10) = 1.8 \times 10^{-10}$$
$$s = \frac{1.8 \times 10^{-10}}{0.10} = 1.8 \times 10^{-9}\ \text{M}$$

**Answer:** Solubility drops from $1.3 \times 10^{-5}\ \text{M}$ to $1.8 \times 10^{-9}\ \text{M}$ — about **7,000 times less soluble**. The added $\ce{Cl-}$ (a common ion) is a product; by [Le Chatelier](/chemistry/0904-le-chatelier), extra product shifts $\ce{AgCl(s) <=> Ag+ + Cl-}$ left, suppressing dissolving. (And $s < 0.10$ by a factor of $10^8$, so the approximation was excellent.)

---

### Example 10: Common-Ion Effect on a $4s^3$ salt

**Problem:** Find the molar solubility of $\ce{CaF2}$ ($K_{sp} = 3.9 \times 10^{-11}$) in $0.10\ \text{M}\ \ce{NaF}$, and compare to pure water.

**Solution:**

**Step 1 — ICE with the common ion.** $\ce{NaF}$ supplies $0.10\ \text{M}\ \ce{F-}$ up front. Dissolving $s$ mol/L of $\ce{CaF2}$ adds $s$ of $\ce{Ca^2+}$ and $2s$ of $\ce{F-}$:
$$[\ce{Ca^2+}] = s, \qquad [\ce{F-}] = 0.10 + 2s \approx 0.10$$

**Step 2 — Plug in.**
$$K_{sp} = (s)(0.10)^2 = 0.010\,s = 3.9 \times 10^{-11}$$
$$s = \frac{3.9 \times 10^{-11}}{0.010} = 3.9 \times 10^{-9}\ \text{M}$$

**Step 3 — Compare** to pure-water $s = 2.1 \times 10^{-4}\ \text{M}$ (Example 3).

**Answer:** Solubility collapses from $2.1 \times 10^{-4}$ to $3.9 \times 10^{-9}\ \text{M}$. The common ion crushes solubility, just like adding sugar to already-sweet tea makes it even harder to dissolve more.

---

### Example 11: pH and Solubility — Reasoning

**Problem:** Explain, using Le Chatelier, why $\ce{Mg(OH)2}$ dissolves much more in acidic solution than in pure water, but $\ce{AgCl}$'s solubility is essentially unaffected by pH.

**Solution:**

**Step 1 — Write the $\ce{Mg(OH)2}$ equilibrium.**
$$\ce{Mg(OH)2(s) <=> Mg^2+ + 2OH-}$$
The $\ce{OH-}$ is a **basic anion**. Add acid, and the $\ce{H+}$ reacts away that hydroxide:
$$\ce{OH- + H+ -> H2O}$$

**Step 2 — Apply Le Chatelier.** Removing $\ce{OH-}$ (a product) pulls the dissolution equilibrium to the **right**, so more $\ce{Mg(OH)2}$ dissolves. This is exactly how antacids like milk of magnesia neutralize stomach acid — the acid *consumes* the anion and keeps the solid dissolving.

**Step 3 — Now $\ce{AgCl}$.**
$$\ce{AgCl(s) <=> Ag+ + Cl-}$$
$\ce{Cl-}$ is the conjugate base of the **strong** acid $\ce{HCl}$, so it is **not basic** — it does not react with $\ce{H+}$. Adding acid removes nothing, so there is no shift.

**Answer:** Salts of **basic anions** ($\ce{OH-}, \ce{CO3^2-}, \ce{F-}, \ce{PO4^3-}$) dissolve more in acid because $\ce{H+}$ eats the anion and drags dissolution forward. $\ce{AgCl}$ is pH-independent because $\ce{Cl-}$ isn't basic.

---

### Example 12: pH and Solubility — Limestone Caves

**Problem:** Cave systems form as slightly-acidic groundwater dissolves limestone, $\ce{CaCO3}$. Write the reactions and explain the driving force.

**Solution:**

**Step 1 — The solubility equilibrium.**
$$\ce{CaCO3(s) <=> Ca^2+ + CO3^2-}$$
Carbonate, $\ce{CO3^2-}$, is a **basic anion** (the conjugate base of the weak acid $\ce{HCO3-}$).

**Step 2 — Rainwater carries dissolved $\ce{CO2}$**, making carbonic acid, so the water is mildly acidic. The $\ce{H+}$ reacts with carbonate:
$$\ce{CO3^2- + H+ -> HCO3-} \quad(\text{and further } \ce{HCO3- + H+ -> H2CO3 -> H2O + CO2})$$

**Step 3 — Le Chatelier.** Consuming $\ce{CO3^2-}$ removes a product, shifting $\ce{CaCO3}$ dissolution right — so the limestone slowly dissolves, hollowing out the cave. When that mineral-rich water later drips and releases $\ce{CO2}$, the equilibrium reverses and $\ce{CaCO3}$ re-precipitates, building stalactites — precipitation, just like rock candy on a string.

**Answer:** Acidic water dissolves $\ce{CaCO3}$ because $\ce{H+}$ consumes the basic carbonate ion, pulling dissolution forward; reversing the process re-deposits the solid.

---

### Example 13: Free Energy of Dissolution

**Problem:** Estimate $\Delta G^\circ_{\text{dissolution}}$ for $\ce{AgCl}$ ($K_{sp} = 1.8 \times 10^{-10}$) at $298\ \text{K}$, and interpret the sign. ($R = 8.314\ \text{J/mol·K}$.)

**Solution:**

**Step 1 — Use the bridge equation.**
$$\Delta G^\circ = -RT\ln K_{sp} = -(8.314)(298)\ln(1.8 \times 10^{-10})$$

**Step 2 — Compute.** $\ln(1.8 \times 10^{-10}) = -22.4$, so
$$\Delta G^\circ = -(2478)(-22.4) \approx +5.6 \times 10^{4}\ \text{J/mol} = +56\ \text{kJ/mol}$$

**Step 3 — Interpret.** $\Delta G^\circ > 0$: dissolving $\ce{AgCl}$ is **nonspontaneous** under standard conditions (1 M ions) — consistent with it being only slightly soluble. A salt with $K_{sp} > 1$ would give a negative $\Delta G^\circ$ and dissolve readily.

**Answer:** $\Delta G^\circ \approx +56\ \text{kJ/mol}$; positive, because $K_{sp} \ll 1$. We develop $\Delta G^\circ = -RT\ln K$ fully in [Free Energy and Equilibrium](/chemistry/1103-free-energy-equilibrium).

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Putting the solid in the $K_{sp}$ expression | Habit of including every species | Pure solids (and liquids) are **never** in $K_{sp}$ — only dissolved ions |
| Writing $K_{sp} = s^3$ for $\ce{CaF2}$ instead of $4s^3$ | Forgetting to square the coefficient in $(2s)^2$ | The whole ion concentration, coefficient and all, gets raised to the power: $(2s)^2 = 4s^2$ |
| Ranking solubility straight from $K_{sp}$ | Assuming smaller $K_{sp}$ = less soluble | Only valid for **same-formula-type** salts; otherwise compute $s$ for each |
| Forgetting dilution when mixing two solutions | Using the original concentrations for $Q$ | Recompute each ion for the **combined volume** first ($c_1V_1 = c_2V_2$) |
| Confusing $s$ (molar solubility) with an ion concentration | Coefficients aren't 1 | For $\ce{CaF2}$, $[\ce{Ca^2+}] = s$ but $[\ce{F-}] = 2s$ — track each separately |
| Thinking common ions or acid change $K_{sp}$ | Solubility went down/up, so "$K$ must have changed" | $K_{sp}$ is fixed at a given temperature; what changes is the *position* of equilibrium (and thus $s$) |
| Expecting acid to boost $\ce{AgCl}$ solubility | Over-applying the pH rule | Only **basic anions** react with $\ce{H+}$; $\ce{Cl-}, \ce{NO3-}, \ce{Br-}$ (conjugates of strong acids) don't |

---

## AP Exam Tips

- **Leave the solid out.** A $K_{sp}$ expression that contains the solid earns zero on that part. Only aqueous ions, each raised to its coefficient.
- **The molar-solubility ICE is worth setting up explicitly.** Show $[\ce{Ca^2+}] = s$ and $[\ce{F-}] = 2s$, then $K_{sp} = 4s^3$. Graders reward the coefficient-power step even in "explain" questions.
- **Never rank solubility by $K_{sp}$ across different formulas.** If a free-response asks you to compare, compute $s$ for each and compare *those*. State this reasoning — it's a common conceptual point.
- **Common ion → less soluble, always.** If asked "does solubility increase or decrease in $\ce{NaCl}$ solution?", the answer is decrease, and the justification is Le Chatelier (added product shifts left). $K_{sp}$ itself does not change.
- **Basic anions dissolve more in acid.** Hydroxides, carbonates, fluorides, phosphates, sulfides — their solubility rises in acid because $\ce{H+}$ consumes the anion. Salts of strong-acid anions ($\ce{Cl-}, \ce{NO3-}$) are pH-independent. This is a frequent multiple-choice and short-answer item.
- **$Q$ vs $K_{sp}$ for precipitation.** $Q > K_{sp}$ → precipitate; $Q < K_{sp}$ → no precipitate. On mixing problems, dilution to the new total volume is a graded step — don't skip it.
- **Sign of $\Delta G^\circ$.** $K_{sp} < 1$ means $\Delta G^\circ_{\text{dissolution}} > 0$. Expect this connection to show up as a bridge into Unit 9.
- **Calculator:** cube roots via $x^{1/3}$ (or $\text{ans}\,\wedge\,(1/3)$) — practice so you don't fumble the $4s^3$ solve under time pressure.

---

## Practice Problems

### Problem 1
Write the dissolution equation and $K_{sp}$ expression for $\ce{PbBr2}$.

<details>
<summary><strong>Solution</strong></summary>

$$\ce{PbBr2(s) <=> Pb^2+ + 2Br-} \qquad K_{sp} = [\ce{Pb^2+}][\ce{Br-}]^2$$

**Answer:** $K_{sp} = [\ce{Pb^2+}][\ce{Br-}]^2$ (solid omitted; the 2 on $\ce{Br-}$ becomes the exponent).

</details>

---

### Problem 2
Write the $K_{sp}$ expression for $\ce{Al(OH)3}$.

<details>
<summary><strong>Solution</strong></summary>

$$\ce{Al(OH)3(s) <=> Al^3+ + 3OH-} \qquad K_{sp} = [\ce{Al^3+}][\ce{OH-}]^3$$

**Answer:** $K_{sp} = [\ce{Al^3+}][\ce{OH-}]^3$.

</details>

---

### Problem 3
$\ce{BaSO4}$ has $K_{sp} = 1.1 \times 10^{-10}$. Find its molar solubility in pure water.

<details>
<summary><strong>Solution</strong></summary>

1:1 salt, so $K_{sp} = s^2$.
$$s = \sqrt{1.1 \times 10^{-10}} = 1.05 \times 10^{-5}\ \text{M}$$

**Answer:** $s \approx 1.0 \times 10^{-5}\ \text{M}$.

</details>

---

### Problem 4
$\ce{Mg(OH)2}$ has $K_{sp} = 5.6 \times 10^{-12}$. Find its molar solubility.

<details>
<summary><strong>Solution</strong></summary>

$\ce{Mg(OH)2(s) <=> Mg^2+ + 2OH-}$, so $[\ce{Mg^2+}] = s$, $[\ce{OH-}] = 2s$:
$$K_{sp} = (s)(2s)^2 = 4s^3 = 5.6 \times 10^{-12}$$
$$s^3 = 1.4 \times 10^{-12} \;\Rightarrow\; s = 1.1 \times 10^{-4}\ \text{M}$$

**Answer:** $s \approx 1.1 \times 10^{-4}\ \text{M}$.

</details>

---

### Problem 5
The molar solubility of $\ce{Ag2CrO4}$ is $6.5 \times 10^{-5}\ \text{M}$. Calculate $K_{sp}$.

<details>
<summary><strong>Solution</strong></summary>

$\ce{Ag2CrO4(s) <=> 2Ag+ + CrO4^2-}$, so $[\ce{Ag+}] = 2s$, $[\ce{CrO4^2-}] = s$:
$$K_{sp} = (2s)^2(s) = 4s^3 = 4(6.5 \times 10^{-5})^3 = 4(2.75 \times 10^{-13})$$
$$= 1.1 \times 10^{-12}$$

**Answer:** $K_{sp} = 1.1 \times 10^{-12}$.

</details>

---

### Problem 6
$\ce{CaCO3}$ has molar solubility $5.8 \times 10^{-5}\ \text{M}$. Express it in g/L. ($M_{\ce{CaCO3}} = 100.09\ \text{g/mol}$.)

<details>
<summary><strong>Solution</strong></summary>

$$\left(5.8 \times 10^{-5}\ \tfrac{\text{mol}}{\text{L}}\right)(100.09\ \tfrac{\text{g}}{\text{mol}}) = 5.8 \times 10^{-3}\ \text{g/L}$$

**Answer:** $\approx 5.8 \times 10^{-3}\ \text{g/L}$ (about 5.8 mg per liter).

</details>

---

### Problem 7
$\ce{CaF2}$ has $K_{sp} = 3.9 \times 10^{-11}$ and $\ce{PbCl2}$ has $K_{sp} = 1.7 \times 10^{-5}$. Which has the larger molar solubility?

<details>
<summary><strong>Solution</strong></summary>

Both are $4s^3$-type salts, but compute $s$ to be safe.
$\ce{CaF2}$: $s = \sqrt[3]{3.9\times10^{-11}/4} = 2.1 \times 10^{-4}\ \text{M}$.
$\ce{PbCl2}$: $s = \sqrt[3]{1.7\times10^{-5}/4} = \sqrt[3]{4.25\times10^{-6}} = 1.6 \times 10^{-2}\ \text{M}$.

**Answer:** $\ce{PbCl2}$ is far more soluble ($1.6 \times 10^{-2}$ vs $2.1 \times 10^{-4}\ \text{M}$). Here the larger $K_{sp}$ *does* mean larger $s$ because the formula types match — but you should still show $s$.

</details>

---

### Problem 8
$\ce{Mg(OH)2}$ has $K_{sp} = 5.6 \times 10^{-12}$ and $\ce{Ni(OH)2}$ has $K_{sp} = 5.5 \times 10^{-16}$. Without computing $s$, can you say which is more soluble? Explain.

<details>
<summary><strong>Solution</strong></summary>

Both are $\ce{M(OH)2}$ salts — identical formula type — so both give $K_{sp} = 4s^3$. Because $s = \sqrt[3]{K_{sp}/4}$ is a monotonic function of $K_{sp}$, the larger $K_{sp}$ wins. $\ce{Mg(OH)2}$ has the larger $K_{sp}$.

**Answer:** $\ce{Mg(OH)2}$ is more soluble. (Direct $K_{sp}$ comparison is legitimate *here* only because the formulas match.)

</details>

---

### Problem 9
Is a solution that is $2.0 \times 10^{-3}\ \text{M}$ in $\ce{Ca^2+}$ and $2.0 \times 10^{-3}\ \text{M}$ in $\ce{F-}$ saturated, unsaturated, or will it precipitate? ($K_{sp,\,\ce{CaF2}} = 3.9 \times 10^{-11}$.)

<details>
<summary><strong>Solution</strong></summary>

$$Q = [\ce{Ca^2+}][\ce{F-}]^2 = (2.0 \times 10^{-3})(2.0 \times 10^{-3})^2 = (2.0 \times 10^{-3})(4.0 \times 10^{-6}) = 8.0 \times 10^{-9}$$
$Q = 8.0 \times 10^{-9} > K_{sp} = 3.9 \times 10^{-11}$.

**Answer:** $Q > K_{sp}$, so $\ce{CaF2}$ **precipitates**.

</details>

---

### Problem 10
$100.0\ \text{mL}$ of $0.020\ \text{M}\ \ce{Pb(NO3)2}$ is mixed with $100.0\ \text{mL}$ of $0.020\ \text{M}\ \ce{NaI}$. Will $\ce{PbI2}$ (\,$K_{sp} = 7.1 \times 10^{-9}$\,) precipitate?

<details>
<summary><strong>Solution</strong></summary>

Dilute to $200.0\ \text{mL}$ (each halved): $[\ce{Pb^2+}] = 0.010\ \text{M}$, $[\ce{I-}] = 0.010\ \text{M}$.
$$Q = [\ce{Pb^2+}][\ce{I-}]^2 = (0.010)(0.010)^2 = 1.0 \times 10^{-6}$$
$Q = 1.0 \times 10^{-6} > 7.1 \times 10^{-9} = K_{sp}$.

**Answer:** $Q > K_{sp}$ → **yes, $\ce{PbI2}$ precipitates.** (Miss the dilution and you'd use $0.020$ and still get precipitation here — but the halved values are the graded step.)

</details>

---

### Problem 11
Calculate the molar solubility of $\ce{BaSO4}$ ($K_{sp} = 1.1 \times 10^{-10}$) in $0.050\ \text{M}\ \ce{Na2SO4}$, and compare to pure water.

<details>
<summary><strong>Solution</strong></summary>

Common ion $\ce{SO4^2-}$ starts at $0.050\ \text{M}$. ICE: $[\ce{Ba^2+}] = s$, $[\ce{SO4^2-}] = 0.050 + s \approx 0.050$.
$$K_{sp} = (s)(0.050) = 1.1 \times 10^{-10} \;\Rightarrow\; s = \frac{1.1 \times 10^{-10}}{0.050} = 2.2 \times 10^{-9}\ \text{M}$$
Pure water (Problem 3): $s = 1.0 \times 10^{-5}\ \text{M}$.

**Answer:** $s = 2.2 \times 10^{-9}\ \text{M}$, roughly 5,000× less soluble than in pure water — the common-ion effect.

</details>

---

### Problem 12
Rank these in order of *increasing* solubility in **acidic** solution and explain: $\ce{AgCl}$, $\ce{CaCO3}$, $\ce{Mg(OH)2}$.

<details>
<summary><strong>Solution</strong></summary>

The question is about which anions are basic (react with $\ce{H+}$).
- $\ce{AgCl}$: $\ce{Cl-}$ is the conjugate base of a strong acid → not basic → **pH-independent**, no boost from acid.
- $\ce{CaCO3}$: $\ce{CO3^2-}$ is basic → dissolves much more in acid.
- $\ce{Mg(OH)2}$: $\ce{OH-}$ is strongly basic → dissolves much more in acid.

Both carbonate and hydroxide get large boosts; $\ce{AgCl}$ gets none.

**Answer:** In acid, $\ce{AgCl}$ stays least affected while $\ce{CaCO3}$ and $\ce{Mg(OH)2}$ dissolve far more because their anions are basic and consume $\ce{H+}$, pulling dissolution forward (Le Chatelier).

</details>

---

### Problem 13
Explain why adding a few drops of concentrated $\ce{HNO3}$ to a saturated solution of $\ce{Mg(OH)2}$ (with solid at the bottom) causes more solid to dissolve, but adding $\ce{HNO3}$ to saturated $\ce{AgCl}$ does essentially nothing.

<details>
<summary><strong>Solution</strong></summary>

$\ce{Mg(OH)2(s) <=> Mg^2+ + 2OH-}$: the strong acid supplies $\ce{H+}$, which neutralizes $\ce{OH-}$ ($\ce{H+ + OH- -> H2O}$). Removing the product $\ce{OH-}$ shifts the equilibrium right, so more solid dissolves.

$\ce{AgCl(s) <=> Ag+ + Cl-}$: $\ce{Cl-}$ is not basic, so $\ce{H+}$ has nothing to react with; no product is removed, no shift. (The $\ce{NO3-}$ is a spectator either way.)

**Answer:** Acid dissolves $\ce{Mg(OH)2}$ because $\ce{H+}$ consumes the basic $\ce{OH-}$; $\ce{AgCl}$ is unaffected because $\ce{Cl-}$ isn't basic.

</details>

---

### Problem 14
A salt $\ce{MX}$ has $K_{sp} = 4.0 \times 10^{-8}$. (a) Find $s$ in pure water. (b) Find $s$ in $0.20\ \text{M}\ \ce{NaX}$. (c) By what factor did the common ion reduce solubility?

<details>
<summary><strong>Solution</strong></summary>

**(a)** $s = \sqrt{4.0 \times 10^{-8}} = 2.0 \times 10^{-4}\ \text{M}$.

**(b)** $[\ce{X-}] = 0.20 + s \approx 0.20$: $K_{sp} = (s)(0.20) = 4.0 \times 10^{-8}$, so $s = 2.0 \times 10^{-7}\ \text{M}$.

**(c)** Factor $= \dfrac{2.0 \times 10^{-4}}{2.0 \times 10^{-7}} = 1.0 \times 10^{3}$.

**Answer:** (a) $2.0 \times 10^{-4}\ \text{M}$; (b) $2.0 \times 10^{-7}\ \text{M}$; (c) about **1,000× less soluble**.

</details>

---

### Problem 15
For $\ce{BaSO4}$, $\Delta G^\circ_{\text{dissolution}}$ at $298\ \text{K}$ is positive. Without a calculator, is $K_{sp}$ greater than or less than 1? Explain using $\Delta G^\circ = -RT\ln K_{sp}$.

<details>
<summary><strong>Solution</strong></summary>

If $\Delta G^\circ > 0$, then from $\Delta G^\circ = -RT\ln K_{sp}$ we need $-RT\ln K_{sp} > 0$. Since $R$ and $T$ are positive, $\ln K_{sp} < 0$, which means $K_{sp} < 1$.

**Answer:** $K_{sp} < 1$ — consistent with $\ce{BaSO4}$ being only slightly soluble. (Its actual $K_{sp}$ is $1.1 \times 10^{-10}$.)

</details>

---

## Quick Reference

| Concept | Rule / Formula |
|---|---|
| $K_{sp}$ expression | For $\ce{M_xX_y(s) <=> \mathnormal{x}M^+ + \mathnormal{y}X^-}$: $K_{sp} = [\ce{M+}]^x[\ce{X-}]^y$ (solid omitted) |
| 1:1 salt ($\ce{AgCl}$) | $K_{sp} = s^2$, so $s = \sqrt{K_{sp}}$ |
| 1:2 / 2:1 salt ($\ce{CaF2}, \ce{Ag2CrO4}$) | $K_{sp} = 4s^3$, so $s = \sqrt[3]{K_{sp}/4}$ |
| 3:2 salt ($\ce{Ca3(PO4)2}$) | $K_{sp} = 108s^5$ |
| Molar → g/L | multiply $s\,(\text{mol/L})$ by molar mass |
| Comparing salts | compute $s$ for each — **don't** compare $K_{sp}$ across different formula types |
| Ion product | $Q > K_{sp}$ → precipitate; $Q = K_{sp}$ → saturated; $Q < K_{sp}$ → unsaturated |
| Mixing solutions | dilute each ion to the combined volume *before* finding $Q$ |
| Common-ion effect | shared ion → equilibrium shifts left → **solubility decreases** ($K_{sp}$ unchanged) |
| pH and solubility | basic anions ($\ce{OH-}, \ce{CO3^2-}, \ce{F-}, \ce{PO4^3-}$) → **more soluble in acid**; strong-acid anions ($\ce{Cl-}, \ce{NO3-}$) → pH-independent |
| Free energy | $\Delta G^\circ_{\text{dissolution}} = -RT\ln K_{sp}$; $K_{sp} < 1 \Rightarrow \Delta G^\circ > 0$ |

---

<div align="center">

[← Le Chatelier's Principle](/chemistry/0904-le-chatelier) | [pH, pOH, and Strong Acids →](/chemistry/1001-ph-poh-strong-acids-bases)

</div>
