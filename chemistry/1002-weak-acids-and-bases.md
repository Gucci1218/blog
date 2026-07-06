# Weak Acids and Bases
<p class="article-date">July 5, 2026</p>

*Pour a splash of vinegar over your salad and you get that sharp, mouth-puckering tang — the taste of acid. But here's the thing that genuinely surprised me when I started AP Chem: that bottle of white vinegar is basically pure acetic acid diluted in water, and at any given moment only about **1 in 100** of its acid molecules has actually let go of a proton. The other 99 are just sitting there, whole, un-ionized, minding their own business. That's what chemists mean by a **weak** acid — not that it's watered down, but that it's **reluctant** to give up its proton. The tang you taste is only that tiny ionized fraction, held in a constant tug-of-war with the un-ionized majority. And there's a single number, $K_a$, that measures exactly how reluctant the acid is. This article is about that reluctance — how to measure it, how to calculate the pH it produces, and why "weak" is a statement about equilibrium, not about concentration.*

---

## What You'll Learn

- Explain why a **weak acid or base only partially ionizes**, so its dissolving is a reversible **equilibrium** (a double arrow), not a one-way reaction
- Draw the sharp line between **strong vs. weak** (extent of ionization) and **concentrated vs. dilute** (amount of acid) — they are completely different ideas
- Write the **acid-ionization** equilibrium and its constant $K_a = \frac{[\ce{H3O+}][\ce{A-}]}{[\ce{HA}]}$, and the **base-ionization** constant $K_b$
- Rank acids by **strength** using $K_a$ and $\text{p}K_a = -\log K_a$ (bigger $K_a$ / smaller $\text{p}K_a$ = stronger)
- Calculate the **pH of a weak acid** with an **ICE table**, the **small-$x$ approximation**, and the **5% validity check**
- Run the **reverse problem**: find $K_a$ from a measured pH and starting concentration
- Compute **percent ionization** and explain the classic twist — *why it rises as you dilute*
- Calculate the **pH of a weak base** through $K_b$, an ICE table, and $\text{pOH} \to \text{pH}$
- Use the conjugate relationship $K_a \times K_b = K_w = 1.0\times10^{-14}$ (and $\text{p}K_a + \text{p}K_b = 14$) to find one from the other
- **Classify a salt solution** as acidic, basic, or neutral from its ions, and compute its pH via the conjugate's $K_a$ or $K_b$

---

## Prerequisites

- [pH, pOH, and Strong Acids and Bases](/chemistry/1001-ph-poh-strong-acids-bases) — you must already be fluent with $\text{pH} = -\log[\ce{H+}]$, the $\text{pH} + \text{pOH} = 14$ relationship, and $K_w = 1.0\times10^{-14}$. Weak acids are the *contrast* to strong ones: a strong acid ionizes 100%, so $[\ce{H+}]$ equals the concentration outright; a weak acid does not, which is the entire reason we need everything below.
- [ICE Tables and Equilibrium Calculations](/chemistry/0903-ice-tables) — **a weak-acid pH problem is an ICE problem in disguise.** Every calculation in this article is: set up ICE, plug the Equilibrium row into $K_a$ (or $K_b$), solve for $x$. If the three-row ledger feels shaky, patch it here first.
- [The Equilibrium Constant](/chemistry/0902-equilibrium-constant) — $K_a$ and $K_b$ *are* equilibrium constants (products over reactants). Everything you know about what $K$ means — small $K$ sits far left, large $K$ sits far right — transfers directly.

---

## The Core Concept

### Intuition First

Let me stay in the kitchen with that bottle of vinegar, because the whole topic lives inside it.

Vinegar is **acetic acid**, $\ce{CH3COOH}$ (you'll also see it written $\ce{HC2H3O2}$ — same molecule, and the first $\ce{H}$ is the acidic one). Imagine you could shrink down and count the molecules floating in the bottle. You'd expect an acid to be busy dumping protons everywhere. Instead you'd find something almost lazy: out of every 100 acetic acid molecules, roughly **99 are still intact** and only **1 has actually split** into $\ce{H+}$ and acetate $\ce{CH3COO-}$. And it's not that the same one stays split forever — molecules are constantly letting go and grabbing back on, but at any snapshot the *count* holds steady at about 99 whole, 1 broken. That steady, two-directional standoff is an **equilibrium**, and we write it with a **double arrow**:

$$\ce{CH3COOH + H2O <=> H3O+ + CH3COO-}$$

Here's the map that made it click for me. Every part of the vinegar bottle corresponds to a part of the chemistry:

| In the vinegar bottle | In the chemistry |
|---|---|
| The whole bottle of acetic acid sitting at rest | The **weak acid at equilibrium** |
| The ~1% that has let go of its proton | The ionized fraction → **percent ionization** |
| The ~99% still holding on, un-ionized | The reactant $\ce{HA}$ that dominates |
| How *reluctant* the acid is to let go | A **small $K_a$** |
| The tang you actually taste | The small amount of free $\ce{H+}$ that made it out |

The single most important idea in this whole unit is hiding in that table: **"weak" means the equilibrium sits far to the LEFT — mostly un-ionized — NOT that the acid is dilute.** I can make a *concentrated* weak acid (a huge amount of acetic acid) and a *dilute* strong acid (a tiny drop of $\ce{HCl}$). The strong one still ionizes 100%; the weak one still only ~1%. Strong/weak is about **what fraction breaks apart**. Concentrated/dilute is about **how much acid you dumped in**. Do not let anyone blur those two — I'll hammer it again below because the AP exam loves this trap.

### Strong vs. Weak, Revisited

Back in [Acid–Base Reactions](/chemistry/0605-acid-base-reactions), a **strong acid** was defined as one that ionizes completely. Dissolve $\ce{HCl}$ and it's a one-way street — a single arrow:

$$\ce{HCl -> H+ + Cl-} \qquad (\text{100\% ionized, no equilibrium})$$

There's essentially no $\ce{HCl}$ molecule left, so for a strong acid $[\ce{H+}]$ just equals the acid's concentration and you're done (that's the whole [strong-acid](/chemistry/1001-ph-poh-strong-acids-bases) shortcut).

A **weak acid** refuses to finish the job. It reaches an equilibrium with reactants still present — a double arrow:

$$\ce{HA + H2O <=> H3O+ + A-} \qquad (\text{partly ionized, sits at equilibrium})$$

That single difference — one arrow vs. two — is the reason weak acids need an ICE table and strong acids don't.

> **Strong/weak ≠ concentrated/dilute.** Strong vs. weak = the *fraction* that ionizes (a property of the acid itself). Concentrated vs. dilute = *how much* you have (a property of the solution you mixed). A 12 M solution of acetic acid is a **concentrated weak** acid. A 0.0001 M solution of $\ce{HCl}$ is a **dilute strong** acid. Keep the two axes separate.

**The short lists worth memorizing.** There are only a handful of strong acids and bases; *everything else is weak.*

- **Strong acids:** $\ce{HCl}$, $\ce{HBr}$, $\ce{HI}$, $\ce{HNO3}$, $\ce{HClO4}$, $\ce{H2SO4}$ (first proton).
- **Strong bases:** the Group 1 hydroxides ($\ce{NaOH}$, $\ce{KOH}$, …) and heavy Group 2 hydroxides ($\ce{Ca(OH)2}$, $\ce{Ba(OH)2}$).
- **Weak acids** (need $K_a$): acetic $\ce{CH3COOH}$, formic $\ce{HCOOH}$, hydrofluoric $\ce{HF}$, hydrocyanic $\ce{HCN}$, carbonic $\ce{H2CO3}$, and so on.
- **Weak bases** (need $K_b$): ammonia $\ce{NH3}$, the amines like methylamine $\ce{CH3NH2}$, and the anions of weak acids.

### $K_a$: The Number for "How Reluctant"

Since a weak acid sits at equilibrium, it has an equilibrium constant — we just give it the special name **acid-ionization constant, $K_a$.** For the general acid $\ce{HA}$:

$$\ce{HA + H2O <=> H3O+ + A-} \qquad K_a = \frac{[\ce{H3O+}][\ce{A-}]}{[\ce{HA}]}$$

Water is the solvent (a pure liquid), so — exactly as in [The Equilibrium Constant](/chemistry/0902-equilibrium-constant) — it does **not** appear in the expression. Everything else is products-over-reactants, just like any $K$.

**Reading $K_a$ is reading reluctance:**

- **Big $K_a$** (say $10^{-2}$) → the top of the fraction is relatively large → lots of ionization → the equilibrium leans right → **stronger** weak acid.
- **Small $K_a$** (say $10^{-10}$) → barely anything on top → almost no ionization → equilibrium far left → **weaker** acid, more reluctant.

Some real values to anchor the scale (memorize the *order of magnitude*, not the digits):

| Weak acid | Formula | $K_a$ | $\text{p}K_a$ |
|---|---|---|---|
| Hydrofluoric | $\ce{HF}$ | $6.8\times10^{-4}$ | 3.17 |
| Formic | $\ce{HCOOH}$ | $1.8\times10^{-4}$ | 3.74 |
| Acetic (vinegar) | $\ce{CH3COOH}$ | $1.8\times10^{-5}$ | 4.74 |
| Hypochlorous | $\ce{HClO}$ | $3.0\times10^{-8}$ | 7.52 |
| Hydrocyanic | $\ce{HCN}$ | $6.2\times10^{-10}$ | 9.21 |

### $\text{p}K_a$: A Friendlier Scale

Those $K_a$ values are ugly powers of ten, so — just like pH tames $[\ce{H+}]$ — we define:

$$\boxed{\text{p}K_a = -\log K_a}$$

The "p" does the same job it always does: take the negative log to turn a tiny exponential number into a friendly small one. Because of the minus sign, the ranking **flips**:

$$\text{larger } K_a \iff \text{smaller } \text{p}K_a \iff \text{stronger acid}$$

So in the table above, $\ce{HF}$ ($\text{p}K_a = 3.17$) is the strongest of the group and $\ce{HCN}$ ($\text{p}K_a = 9.21$) the weakest. When the AP exam hands you $\text{p}K_a$ values and asks "which is the strongest acid?", the answer is always the **smallest** $\text{p}K_a$.

### $K_b$: The Same Story for Bases

A **weak base** does the mirror-image thing: instead of donating a proton, it *accepts* one from water, generating $\ce{OH-}$. The general weak base $\ce{B}$ (think ammonia):

$$\ce{B + H2O <=> BH+ + OH-} \qquad K_b = \frac{[\ce{BH+}][\ce{OH-}]}{[\ce{B}]}$$

For ammonia specifically:

$$\ce{NH3 + H2O <=> NH4+ + OH-} \qquad K_b = \frac{[\ce{NH4+}][\ce{OH-}]}{[\ce{NH3}]} = 1.8\times10^{-5}$$

Same rules: bigger $K_b$ = stronger base, and $\text{p}K_b = -\log K_b$ with smaller $\text{p}K_b$ = stronger base. The only difference from the acid case is that solving a $K_b$ problem hands you $[\ce{OH-}]$ first, so you get **pOH** and then convert to pH.

### The Recipe (memorize this rhythm)

Every weak-acid pH problem in this article follows the **exact same five beats**:

1. **Write** the ionization equation and its $K_a$ expression.
2. **Build an ICE table**, letting $x = [\ce{H+}]$ produced.
3. **Plug** the Equilibrium row into $K_a$.
4. **Approximate:** since $K_a$ is small, assume $x$ is tiny compared to the starting concentration, so $[\ce{HA}]_0 - x \approx [\ce{HA}]_0$. Solve the easy equation for $x$.
5. **Validate** with the 5% rule, then convert $x = [\ce{H+}]$ to pH.

That's it. Let's run it until it's automatic.

---

## Worked Examples

### Example 1: pH of a Weak Acid (the full ICE walkthrough)

**Problem:** Find the pH of $0.100\ \text{M}$ acetic acid, $\ce{CH3COOH}$, given $K_a = 1.8\times10^{-5}$.

**Solution:**

**Step 1 — Equation and expression.**
$$\ce{CH3COOH <=> H+ + CH3COO-} \qquad K_a = \frac{[\ce{H+}][\ce{CH3COO-}]}{[\ce{CH3COOH}]}$$
(I'll write $\ce{H+}$ as shorthand for $\ce{H3O+}$ — they mean the same thing.)

**Step 2 — ICE table**, with $x$ = moles/L of acid that ionize:

| | $\ce{CH3COOH}$ | $\ce{H+}$ | $\ce{CH3COO-}$ |
|---|---|---|---|
| **I** | 0.100 | 0 | 0 |
| **C** | $-x$ | $+x$ | $+x$ |
| **E** | $0.100 - x$ | $x$ | $x$ |

**Step 3 — Plug in:**
$$1.8\times10^{-5} = \frac{(x)(x)}{0.100 - x} = \frac{x^2}{0.100 - x}$$

**Step 4 — Small-$x$ approximation.** Because $K_a$ is tiny, $x$ will be far smaller than 0.100, so $0.100 - x \approx 0.100$:
$$1.8\times10^{-5} = \frac{x^2}{0.100} \implies x^2 = 1.8\times10^{-6} \implies x = 1.34\times10^{-3}\ \text{M}$$

**Step 5 — Validate (5% rule):**
$$\frac{x}{0.100}\times100 = \frac{1.34\times10^{-3}}{0.100}\times100 = 1.34\% < 5\% \checkmark$$
The approximation holds. Now $x = [\ce{H+}] = 1.34\times10^{-3}\ \text{M}$, so:
$$\text{pH} = -\log(1.34\times10^{-3}) = 2.87$$

**Answer:** $\text{pH} = 2.87$. (Sanity check: a *strong* 0.100 M acid would give pH exactly 1.00 — the weak acid's pH is much higher because so little ionized.)

### Example 2: A More Reluctant Acid — $\ce{HCN}$

**Problem:** Find the pH of $0.250\ \text{M}$ hydrocyanic acid, $\ce{HCN}$, $K_a = 6.2\times10^{-10}$.

**Solution:**

**Step 1–2.** $\ce{HCN <=> H+ + CN-}$; ICE gives Equilibrium row $[\ce{HCN}] = 0.250 - x$, $[\ce{H+}] = [\ce{CN-}] = x$.

**Step 3–4.** With such a small $K_a$, drop the $x$ immediately:
$$6.2\times10^{-10} = \frac{x^2}{0.250} \implies x^2 = 1.55\times10^{-10} \implies x = 1.24\times10^{-5}\ \text{M}$$

**Step 5 — Validate:** $\frac{1.24\times10^{-5}}{0.250}\times100 = 0.005\% \ll 5\% \checkmark$ (a huge $K_a$ would be needed to fail this).
$$\text{pH} = -\log(1.24\times10^{-5}) = 4.91$$

**Answer:** $\text{pH} = 4.91$. Notice: same ballpark concentration as Example 1, but a far weaker acid → far higher pH (closer to neutral).

### Example 3: When the Approximation FAILS (use the quadratic)

**Problem:** Find the pH of $0.0100\ \text{M}$ hydrofluoric acid, $\ce{HF}$, $K_a = 6.8\times10^{-4}$. (Here $K_a$ is relatively big *and* the concentration is small — a recipe for trouble.)

**Solution:**

**Try the shortcut first:**
$$6.8\times10^{-4} = \frac{x^2}{0.0100} \implies x = \sqrt{6.8\times10^{-6}} = 2.61\times10^{-3}$$
**Validate:** $\frac{2.61\times10^{-3}}{0.0100}\times100 = 26\% > 5\%$ ✗ — **fails badly.** So we must keep the $-x$.

**Solve the real quadratic:**
$$6.8\times10^{-4} = \frac{x^2}{0.0100 - x} \implies x^2 + 6.8\times10^{-4}x - 6.8\times10^{-6} = 0$$
$$x = \frac{-6.8\times10^{-4} + \sqrt{(6.8\times10^{-4})^2 + 4(6.8\times10^{-6})}}{2} = 2.28\times10^{-3}\ \text{M}$$
$$\text{pH} = -\log(2.28\times10^{-3}) = 2.64$$

**Answer:** $\text{pH} = 2.64$. The approximation would have given pH 2.58 — off enough to matter. **Moral: always run the 5% check; when it fails, use the quadratic.**

### Example 4: Formic Acid (another clean one)

**Problem:** Find the pH of $0.500\ \text{M}$ formic acid, $\ce{HCOOH}$, $K_a = 1.8\times10^{-4}$.

**Solution:**
$$1.8\times10^{-4} = \frac{x^2}{0.500} \implies x^2 = 9.0\times10^{-5} \implies x = 9.49\times10^{-3}\ \text{M}$$
**Validate:** $\frac{9.49\times10^{-3}}{0.500}\times100 = 1.9\% < 5\% \checkmark$
$$\text{pH} = -\log(9.49\times10^{-3}) = 2.02$$

**Answer:** $\text{pH} = 2.02$.

### Example 5: The Reverse Problem — Find $K_a$ from pH

**Problem:** A $0.200\ \text{M}$ solution of an unknown weak acid $\ce{HA}$ has a measured $\text{pH} = 2.75$. What is $K_a$?

**Solution:**

**Step 1 — pH back to $[\ce{H+}]$:**
$$[\ce{H+}] = 10^{-2.75} = 1.78\times10^{-3}\ \text{M}$$

**Step 2 — that's $x$.** From the ICE table, ionizing produces equal $\ce{H+}$ and $\ce{A-}$, so $[\ce{A-}] = x = 1.78\times10^{-3}$ too, and the leftover acid is $[\ce{HA}] = 0.200 - x = 0.198\ \text{M}$.

**Step 3 — plug into $K_a$:**
$$K_a = \frac{(1.78\times10^{-3})(1.78\times10^{-3})}{0.198} = \frac{3.17\times10^{-6}}{0.198} = 1.6\times10^{-5}$$

**Answer:** $K_a \approx 1.6\times10^{-5}$ (which, note, is right around acetic acid — the unknown could well be vinegar's acid).

### Example 6: Percent Ionization

**Problem:** What is the percent ionization of the $0.100\ \text{M}$ acetic acid from Example 1?

**Solution:** Percent ionization compares how much *actually* ionized to how much you *started* with:
$$\%\text{ ionization} = \frac{[\ce{H+}]_{\text{eq}}}{[\ce{HA}]_0}\times100$$
From Example 1, $[\ce{H+}]_{\text{eq}} = 1.34\times10^{-3}$ and $[\ce{HA}]_0 = 0.100$:
$$\%\text{ ionization} = \frac{1.34\times10^{-3}}{0.100}\times100 = 1.34\%$$

**Answer:** $1.34\%$ — literally the "about 1 in 100" from the vinegar story. (And notice this is the same fraction as the 5% check; the validity check *is* a percent-ionization check.)

### Example 7: The Dilution Twist — Percent Ionization RISES

**Problem:** Dilute that acetic acid tenfold to $0.0100\ \text{M}$. Does the percent ionization go up or down? Compute it. ($K_a = 1.8\times10^{-5}$.)

**Solution:**
$$1.8\times10^{-5} = \frac{x^2}{0.0100} \implies x^2 = 1.8\times10^{-7} \implies x = 4.24\times10^{-4}\ \text{M}$$
$$\%\text{ ionization} = \frac{4.24\times10^{-4}}{0.0100}\times100 = 4.24\%$$

**Answer:** It **rose** from 1.34% to 4.24%. This shocks people — you added water, so shouldn't it get *weaker*? But $K_a$ is fixed; look at $\% = \frac{x}{C_0}$ where $x \approx \sqrt{K_a\,C_0}$, so $\% \approx \sqrt{K_a/C_0}$. As $C_0$ shrinks, the fraction ionized **grows** (Le Châtelier: diluting shifts the equilibrium toward the side with more dissolved particles — the ionized side). Note the two facts don't conflict: percent ionization goes *up*, but the actual $[\ce{H+}]$ goes *down* (from $1.34\times10^{-3}$ to $4.24\times10^{-4}$), so the diluted solution is still less acidic overall.

### Example 8: pH of a Weak Base — Ammonia

**Problem:** Find the pH of $0.150\ \text{M}$ ammonia, $\ce{NH3}$, $K_b = 1.8\times10^{-5}$.

**Solution:**

**Step 1 — equation and $K_b$:**
$$\ce{NH3 + H2O <=> NH4+ + OH-} \qquad K_b = \frac{[\ce{NH4+}][\ce{OH-}]}{[\ce{NH3}]}$$

**Step 2 — ICE**, with $x = [\ce{OH-}]$ produced: Equilibrium row is $[\ce{NH3}] = 0.150 - x$, $[\ce{NH4+}] = [\ce{OH-}] = x$.

**Step 3–4 — approximate:**
$$1.8\times10^{-5} = \frac{x^2}{0.150} \implies x^2 = 2.7\times10^{-6} \implies x = 1.64\times10^{-3}\ \text{M} = [\ce{OH-}]$$
**Validate:** $\frac{1.64\times10^{-3}}{0.150}\times100 = 1.1\% < 5\% \checkmark$

**Step 5 — $[\ce{OH-}] \to$ pOH $\to$ pH** (this is the extra step that base problems need):
$$\text{pOH} = -\log(1.64\times10^{-3}) = 2.79 \qquad \text{pH} = 14.00 - 2.79 = 11.21$$

**Answer:** $\text{pH} = 11.21$ — basic, as expected. **Do not forget the pOH-to-pH conversion**; a $K_b$ problem gives you $[\ce{OH-}]$, never $[\ce{H+}]$ directly.

### Example 9: Weak Base — Methylamine

**Problem:** Find the pH of $0.0500\ \text{M}$ methylamine, $\ce{CH3NH2}$, $K_b = 4.4\times10^{-4}$.

**Solution:**
$$4.4\times10^{-4} = \frac{x^2}{0.0500} \implies x^2 = 2.2\times10^{-5} \implies x = 4.69\times10^{-3}$$
**Validate:** $\frac{4.69\times10^{-3}}{0.0500}\times100 = 9.4\% > 5\%$ ✗ — use the quadratic:
$$x^2 + 4.4\times10^{-4}x - 2.2\times10^{-5} = 0 \implies x = 4.48\times10^{-3}\ \text{M} = [\ce{OH-}]$$
$$\text{pOH} = -\log(4.48\times10^{-3}) = 2.35 \qquad \text{pH} = 14.00 - 2.35 = 11.65$$

**Answer:** $\text{pH} = 11.65$.

### Example 10: The Conjugate Relationship — $K_a \times K_b = K_w$

**Problem:** Acetic acid has $K_a = 1.8\times10^{-5}$. Find $K_b$ for its conjugate base, acetate $\ce{CH3COO-}$.

**Solution:** For **any conjugate acid–base pair**, the ionization constants are locked together by:
$$\boxed{K_a \times K_b = K_w = 1.0\times10^{-14}}$$
Why? Add the acid's ionization to the base's ionization and the two half-reactions sum to the autoionization of water, so their constants multiply to $K_w$. Therefore:
$$K_b = \frac{K_w}{K_a} = \frac{1.0\times10^{-14}}{1.8\times10^{-5}} = 5.6\times10^{-10}$$

**Answer:** $K_b(\ce{CH3COO-}) = 5.6\times10^{-10}$. It's tiny — acetate is an extremely weak base. That's the **"stronger acid → weaker conjugate base"** seesaw: a fairly decent acid like acetic acid ($K_a = 1.8\times10^{-5}$) must have a feeble conjugate base. In $\text{p}$ terms, $\text{p}K_a + \text{p}K_b = 14$, so $\text{p}K_b = 14 - 4.74 = 9.26$.

### Example 11: Classifying a Salt — Acidic, Basic, or Neutral?

**Problem:** Predict whether each dissolves to give an acidic, basic, or neutral solution: (a) $\ce{NaCl}$, (b) $\ce{NaC2H3O2}$ (sodium acetate), (c) $\ce{NH4Cl}$, (d) $\ce{NaHCO3}$ (baking soda).

**Solution:** A salt splits into a **cation** and an **anion**; each ion may or may not react with water ("hydrolyze"). The trick is to trace each ion back to its parent acid or base:

- An ion from a **strong** parent is a **spectator** — it does nothing to pH.
- An ion from a **weak** parent **does** react, tugging the pH.

| Salt | Cation (from…) | Anion (from…) | Result |
|---|---|---|---|
| (a) $\ce{NaCl}$ | $\ce{Na+}$ (strong base $\ce{NaOH}$) | $\ce{Cl-}$ (strong acid $\ce{HCl}$) | both spectators → **neutral** |
| (b) $\ce{NaC2H3O2}$ | $\ce{Na+}$ (spectator) | $\ce{C2H3O2-}$ (weak acid $\ce{HC2H3O2}$) | anion is a base → **basic** |
| (c) $\ce{NH4Cl}$ | $\ce{NH4+}$ (weak base $\ce{NH3}$) | $\ce{Cl-}$ (spectator) | cation is an acid → **acidic** |
| (d) $\ce{NaHCO3}$ | $\ce{Na+}$ (spectator) | $\ce{HCO3-}$ (from weak $\ce{H2CO3}$) | anion is a base → **basic** |

**Answer:** (a) neutral, (b) basic, (c) acidic, (d) basic. The rule of thumb: **the ion from the *weak* partner wins.** Anion of a weak acid → basic; cation of a weak base → acidic; two spectators → neutral.

### Example 12: pH of a Salt Solution (basic salt)

**Problem:** Find the pH of $0.200\ \text{M}$ sodium acetate, $\ce{NaC2H3O2}$. ($K_a$ of acetic acid $= 1.8\times10^{-5}$.)

**Solution:**

**Step 1 — identify the reacting ion.** $\ce{Na+}$ is a spectator. Acetate $\ce{C2H3O2-}$ is the conjugate base of a weak acid, so it hydrolyzes as a **base**:
$$\ce{C2H3O2- + H2O <=> HC2H3O2 + OH-}$$

**Step 2 — get its $K_b$** from the conjugate relationship (Example 10):
$$K_b = \frac{K_w}{K_a} = \frac{1.0\times10^{-14}}{1.8\times10^{-5}} = 5.6\times10^{-10}$$

**Step 3 — ICE + approximate** (this is now just a weak-base problem, $x = [\ce{OH-}]$):
$$5.6\times10^{-10} = \frac{x^2}{0.200} \implies x^2 = 1.11\times10^{-10} \implies x = 1.05\times10^{-5}\ \text{M} = [\ce{OH-}]$$
(5% check passes trivially: 0.005%.)

**Step 4 — pOH → pH:**
$$\text{pOH} = -\log(1.05\times10^{-5}) = 4.98 \qquad \text{pH} = 14.00 - 4.98 = 9.02$$

**Answer:** $\text{pH} = 9.02$ — basic, exactly as the classification predicted.

### Example 13: pH of an Acidic Salt

**Problem:** Find the pH of $0.100\ \text{M}$ ammonium chloride, $\ce{NH4Cl}$. ($K_b$ of ammonia $= 1.8\times10^{-5}$.)

**Solution:**

**Step 1.** $\ce{Cl-}$ is a spectator. $\ce{NH4+}$ is the conjugate **acid** of weak base ammonia, so it hydrolyzes as an acid:
$$\ce{NH4+ <=> NH3 + H+}$$

**Step 2 — get its $K_a$:**
$$K_a = \frac{K_w}{K_b} = \frac{1.0\times10^{-14}}{1.8\times10^{-5}} = 5.6\times10^{-10}$$

**Step 3 — ICE + approximate**, $x = [\ce{H+}]$:
$$5.6\times10^{-10} = \frac{x^2}{0.100} \implies x^2 = 5.6\times10^{-11} \implies x = 7.48\times10^{-6}\ \text{M} = [\ce{H+}]$$

**Step 4 — straight to pH** (an acid problem gives $[\ce{H+}]$ directly, no pOH detour):
$$\text{pH} = -\log(7.48\times10^{-6}) = 5.13$$

**Answer:** $\text{pH} = 5.13$ — acidic, as predicted.

### Example 14: The "Both Weak" Case (qualitative)

**Problem:** Is a solution of ammonium fluoride, $\ce{NH4F}$, acidic, basic, or neutral? ($K_a$ of $\ce{NH4+} = 5.6\times10^{-10}$; $K_b$ of $\ce{F-} = K_w/K_a(\ce{HF}) = 1.0\times10^{-14}/6.8\times10^{-4} = 1.5\times10^{-11}$.)

**Solution:** *Both* ions react — the cation $\ce{NH4+}$ pulls acidic, the anion $\ce{F-}$ pulls basic. Whichever has the **larger constant wins the tug-of-war.** Compare:
$$K_a(\ce{NH4+}) = 5.6\times10^{-10} \quad \text{vs.} \quad K_b(\ce{F-}) = 1.5\times10^{-11}$$
The acid constant is about 37× larger, so the acidic pull dominates.

**Answer:** **Slightly acidic.** (General rule for a "both weak" salt: compare the cation's $K_a$ to the anion's $K_b$ — bigger constant sets the direction.)

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Treating a weak acid like a strong one — setting $[\ce{H+}] = $ concentration | Habit from strong-acid problems | If it's **not** on the strong list, it's weak → you *must* use $K_a$ and an ICE table |
| Confusing "weak" with "dilute" | The words feel similar | Weak = *fraction* ionized (a property of the acid); dilute = *amount* (a property of the mix). Concentrated weak acids exist! |
| Skipping the 5% validity check | The approximation usually works, so people get lazy | *Always* check $\frac{x}{C_0}\times100$. If $> 5\%$, redo with the quadratic — big $K_a$ + small $C_0$ is the danger zone |
| Reporting $[\ce{OH-}]$ as the pH for a base | Forgetting bases give $\ce{OH-}$, not $\ce{H+}$ | Base problem → find pOH first, then $\text{pH} = 14 - \text{pOH}$ |
| Thinking bigger $\text{p}K_a$ = stronger acid | The minus sign in $\text{p}K_a = -\log K_a$ flips it | **Smaller** $\text{p}K_a$ = stronger. Small p, strong acid |
| Using $K_a$ directly for a salt of a weak acid | The *salt* contains the conjugate **base** | Convert first: $K_b = K_w / K_a$, then run a base ICE table |
| Assuming every salt is neutral | $\ce{NaCl}$ is neutral, so people generalize | Trace each ion to its parent — the ion from the **weak** partner controls the pH |
| Dropping $x$ when it's actually large | Blindly approximating | The approximation assumes $x \ll C_0$; when $K_a$ is big or $C_0$ small, it breaks — the 5% check catches it |

---

## AP Exam Tips

- **"Weak" is code for "equilibrium."** The instant you see a weak acid or base, your brain should fire: *double arrow, partial ionization, ICE table, $K_a$ or $K_b$* — never the strong-acid shortcut. Graders award points for *showing* the equilibrium setup.
- **The weak-acid pH ritual is guaranteed to appear:** ICE table → small-$x$ approximation → **5% validity check** → pH. Write out the ICE table even on multiple choice; it prevents silly errors. State the approximation explicitly on free-response — it's often worth a point.
- **Memorize $K_a \times K_b = K_w = 1.0\times10^{-14}$** (and $\text{p}K_a + \text{p}K_b = 14$). Nearly every salt-hydrolysis and conjugate-pair question hinges on this one conversion.
- **Percent ionization rises on dilution.** This is a favorite conceptual trap. Add water → higher % ionized (Le Châtelier shifts toward more particles) — even though $[\ce{H+}]$ itself drops. Be ready to explain it in words *and* justify with $\% \approx \sqrt{K_a/C_0}$.
- **Salt hydrolysis classification is a near-certain question.** Drill the reflex: cation of a strong base + anion of a strong acid = neutral; anion of a weak acid = basic; cation of a weak base = acidic. Trace each ion to its parent.
- **Bigger $K_a$ / smaller $\text{p}K_a$ = stronger acid**, and stronger acid → weaker conjugate base. The seesaw shows up in ranking questions constantly.
- **Calculator care:** $10^{-\text{pH}}$ and $-\log$ are your workhorses. Watch significant figures — pH's decimal places equal the sig figs of $[\ce{H+}]$ (a pH of 2.87 has *two* sig figs, from the mantissa).

---

## Practice Problems

### Problem 1
Explain, in one or two sentences, the difference between a *weak* acid and a *dilute* acid. Give an example of a concentrated weak acid.

<details>
<summary><strong>Solution</strong></summary>

*Weak* describes the **fraction** of molecules that ionize — a weak acid only partially ionizes and sits at equilibrium (double arrow), regardless of how much is present. *Dilute* describes the **amount** of acid dissolved (low concentration). They're independent. A bottle of 12 M glacial acetic acid is **concentrated but still weak** — there's a lot of it, but only ~1% ionizes at any moment.

</details>

### Problem 2
Write the ionization equation and the $K_a$ expression for hydrofluoric acid, $\ce{HF}$.

<details>
<summary><strong>Solution</strong></summary>

$$\ce{HF + H2O <=> H3O+ + F-} \qquad K_a = \frac{[\ce{H3O+}][\ce{F-}]}{[\ce{HF}]}$$

Water is the solvent and does not appear in the expression.

</details>

### Problem 3
Rank these acids from strongest to weakest: acid A ($K_a = 3\times10^{-4}$), acid B ($\text{p}K_a = 9.1$), acid C ($K_a = 1.8\times10^{-5}$).

<details>
<summary><strong>Solution</strong></summary>

Put everything on one scale. Acid B: $K_a = 10^{-9.1} = 7.9\times10^{-10}$. Now compare $K_a$ values (bigger = stronger):
$$\text{A } (3\times10^{-4}) > \text{C } (1.8\times10^{-5}) > \text{B } (7.9\times10^{-10})$$
**Strongest → weakest: A, C, B.**

</details>

### Problem 4
Find the pH of $0.250\ \text{M}$ acetic acid, $\ce{CH3COOH}$ ($K_a = 1.8\times10^{-5}$).

<details>
<summary><strong>Solution</strong></summary>

$$1.8\times10^{-5} = \frac{x^2}{0.250} \implies x^2 = 4.5\times10^{-6} \implies x = 2.12\times10^{-3}\ \text{M}$$
Validate: $\frac{2.12\times10^{-3}}{0.250}\times100 = 0.85\% < 5\% \checkmark$
$$\text{pH} = -\log(2.12\times10^{-3}) = \mathbf{2.67}$$

</details>

### Problem 5
Find the pH of $0.0200\ \text{M}$ nitrous acid, $\ce{HNO2}$ ($K_a = 4.5\times10^{-4}$). Watch the approximation.

<details>
<summary><strong>Solution</strong></summary>

Try the shortcut: $x = \sqrt{(4.5\times10^{-4})(0.0200)} = \sqrt{9.0\times10^{-6}} = 3.0\times10^{-3}$.
Check: $\frac{3.0\times10^{-3}}{0.0200}\times100 = 15\% > 5\%$ ✗ — use the quadratic:
$$x^2 + 4.5\times10^{-4}x - 9.0\times10^{-6} = 0 \implies x = 2.79\times10^{-3}\ \text{M}$$
$$\text{pH} = -\log(2.79\times10^{-3}) = \mathbf{2.55}$$

</details>

### Problem 6
A $0.150\ \text{M}$ solution of a weak acid $\ce{HA}$ has $\text{pH} = 3.20$. Find $K_a$.

<details>
<summary><strong>Solution</strong></summary>

$$[\ce{H+}] = 10^{-3.20} = 6.31\times10^{-4}\ \text{M} = x = [\ce{A-}]$$
$$[\ce{HA}] = 0.150 - 6.31\times10^{-4} \approx 0.149\ \text{M}$$
$$K_a = \frac{(6.31\times10^{-4})^2}{0.149} = \frac{3.98\times10^{-7}}{0.149} = \mathbf{2.7\times10^{-6}}$$

</details>

### Problem 7
Compute the percent ionization for the acid in Problem 4 (0.250 M acetic acid).

<details>
<summary><strong>Solution</strong></summary>

From Problem 4, $[\ce{H+}]_{\text{eq}} = 2.12\times10^{-3}$:
$$\%\text{ ionization} = \frac{2.12\times10^{-3}}{0.250}\times100 = \mathbf{0.85\%}$$

</details>

### Problem 8
Acetic acid is 1.34% ionized at 0.100 M. Without doing the full calculation, predict whether the percent ionization at 0.0010 M will be higher or lower, and explain why.

<details>
<summary><strong>Solution</strong></summary>

**Higher.** Since $\% \approx \sqrt{K_a/C_0}$ and $K_a$ is fixed, decreasing $C_0$ *increases* the percent ionized. Equivalently, diluting shifts the equilibrium toward the side with more dissolved particles (the ionized side), per Le Châtelier. (Numerically it works out to about 13%.) Note this does **not** mean the solution is more acidic — $[\ce{H+}]$ still falls on dilution.

</details>

### Problem 9
Find the pH of $0.300\ \text{M}$ ammonia, $\ce{NH3}$ ($K_b = 1.8\times10^{-5}$).

<details>
<summary><strong>Solution</strong></summary>

$$1.8\times10^{-5} = \frac{x^2}{0.300} \implies x^2 = 5.4\times10^{-6} \implies x = 2.32\times10^{-3}\ \text{M} = [\ce{OH-}]$$
Validate: $\frac{2.32\times10^{-3}}{0.300}\times100 = 0.77\% < 5\% \checkmark$
$$\text{pOH} = -\log(2.32\times10^{-3}) = 2.63 \implies \text{pH} = 14.00 - 2.63 = \mathbf{11.37}$$

</details>

### Problem 10
Pyridine, $\ce{C5H5N}$, is a weak base with $K_b = 1.7\times10^{-9}$. Find the pH of a $0.100\ \text{M}$ solution.

<details>
<summary><strong>Solution</strong></summary>

$$1.7\times10^{-9} = \frac{x^2}{0.100} \implies x^2 = 1.7\times10^{-10} \implies x = 1.30\times10^{-5}\ \text{M} = [\ce{OH-}]$$
(5% check trivially passes.)
$$\text{pOH} = -\log(1.30\times10^{-5}) = 4.89 \implies \text{pH} = 14.00 - 4.89 = \mathbf{9.11}$$

</details>

### Problem 11
Hypochlorous acid $\ce{HClO}$ has $K_a = 3.0\times10^{-8}$. Find $K_b$ and $\text{p}K_b$ for its conjugate base, $\ce{ClO-}$.

<details>
<summary><strong>Solution</strong></summary>

$$K_b = \frac{K_w}{K_a} = \frac{1.0\times10^{-14}}{3.0\times10^{-8}} = \mathbf{3.3\times10^{-7}}$$
$$\text{p}K_a = -\log(3.0\times10^{-8}) = 7.52, \quad \text{p}K_b = 14 - 7.52 = \mathbf{6.48}$$

</details>

### Problem 12
Classify each salt solution as acidic, basic, or neutral: (a) $\ce{KBr}$, (b) $\ce{KF}$, (c) $\ce{NH4NO3}$, (d) $\ce{NaCN}$.

<details>
<summary><strong>Solution</strong></summary>

- (a) $\ce{KBr}$: $\ce{K+}$ (from strong base $\ce{KOH}$) + $\ce{Br-}$ (from strong acid $\ce{HBr}$) → both spectators → **neutral**
- (b) $\ce{KF}$: $\ce{K+}$ spectator + $\ce{F-}$ (from weak $\ce{HF}$) → anion is a base → **basic**
- (c) $\ce{NH4NO3}$: $\ce{NH4+}$ (from weak base $\ce{NH3}$) + $\ce{NO3-}$ (from strong $\ce{HNO3}$) → cation is an acid → **acidic**
- (d) $\ce{NaCN}$: $\ce{Na+}$ spectator + $\ce{CN-}$ (from weak $\ce{HCN}$) → anion is a base → **basic**

</details>

### Problem 13
Find the pH of $0.250\ \text{M}$ sodium fluoride, $\ce{NaF}$. ($K_a$ of $\ce{HF} = 6.8\times10^{-4}$.)

<details>
<summary><strong>Solution</strong></summary>

$\ce{F-}$ is the conjugate base of weak $\ce{HF}$; $\ce{Na+}$ is a spectator. Get $K_b$:
$$K_b = \frac{1.0\times10^{-14}}{6.8\times10^{-4}} = 1.47\times10^{-11}$$
$$\ce{F- + H2O <=> HF + OH-}: \quad 1.47\times10^{-11} = \frac{x^2}{0.250} \implies x = 1.92\times10^{-6}\ \text{M} = [\ce{OH-}]$$
$$\text{pOH} = -\log(1.92\times10^{-6}) = 5.72 \implies \text{pH} = 14.00 - 5.72 = \mathbf{8.28}$$

Basic, as expected for the salt of a weak acid.

</details>

### Problem 14
Find the pH of $0.400\ \text{M}$ ammonium chloride, $\ce{NH4Cl}$. ($K_b$ of $\ce{NH3} = 1.8\times10^{-5}$.)

<details>
<summary><strong>Solution</strong></summary>

$\ce{NH4+}$ is the conjugate acid of weak $\ce{NH3}$; $\ce{Cl-}$ is a spectator. Get $K_a$:
$$K_a = \frac{1.0\times10^{-14}}{1.8\times10^{-5}} = 5.6\times10^{-10}$$
$$\ce{NH4+ <=> NH3 + H+}: \quad 5.6\times10^{-10} = \frac{x^2}{0.400} \implies x^2 = 2.24\times10^{-10} \implies x = 1.50\times10^{-5}\ \text{M} = [\ce{H+}]$$
$$\text{pH} = -\log(1.50\times10^{-5}) = \mathbf{4.82}$$

Acidic, as expected.

</details>

### Problem 15
Ammonium cyanide, $\ce{NH4CN}$, contains two weak ions. Given $K_a(\ce{NH4+}) = 5.6\times10^{-10}$ and $K_b(\ce{CN-}) = 1.6\times10^{-5}$, predict whether the solution is acidic, basic, or neutral.

<details>
<summary><strong>Solution</strong></summary>

Both ions react: $\ce{NH4+}$ pulls acidic, $\ce{CN-}$ pulls basic. Compare their constants:
$$K_b(\ce{CN-}) = 1.6\times10^{-5} \gg K_a(\ce{NH4+}) = 5.6\times10^{-10}$$
The base constant is far larger, so the basic pull dominates → **the solution is basic.**

</details>

---

## Quick Reference

| Concept | Formula / Rule |
|---|---|
| Acid ionization | $\ce{HA + H2O <=> H3O+ + A-}$, $\;K_a = \dfrac{[\ce{H3O+}][\ce{A-}]}{[\ce{HA}]}$ |
| Base ionization | $\ce{B + H2O <=> BH+ + OH-}$, $\;K_b = \dfrac{[\ce{BH+}][\ce{OH-}]}{[\ce{B}]}$ |
| Acid strength scale | bigger $K_a$ = stronger; $\text{p}K_a = -\log K_a$ (smaller = stronger) |
| Weak-acid pH | ICE → $K_a = \dfrac{x^2}{C_0 - x} \approx \dfrac{x^2}{C_0}$ → $x = [\ce{H+}]$ → pH |
| Validity (5% rule) | $\dfrac{x}{C_0}\times100 \le 5\%$; if not, use the quadratic |
| Weak-base pH | solve for $x = [\ce{OH-}]$ → pOH → $\text{pH} = 14 - \text{pOH}$ |
| Percent ionization | $\dfrac{[\ce{H+}]_{\text{eq}}}{[\ce{HA}]_0}\times100 \approx \sqrt{K_a/C_0}$ — **rises on dilution** |
| Conjugate pair | $K_a \times K_b = K_w = 1.0\times10^{-14}$; $\;\text{p}K_a + \text{p}K_b = 14$ |
| Salt: neutral | strong-base cation + strong-acid anion (e.g. $\ce{NaCl}$) |
| Salt: basic | anion of a weak acid (e.g. $\ce{NaC2H3O2}$, $\ce{NaHCO3}$) |
| Salt: acidic | cation of a weak base (e.g. $\ce{NH4Cl}$) |
| Salt: both weak | compare cation $K_a$ vs. anion $K_b$ — larger wins |

---

<div align="center">

[← pH, pOH, and Strong Acids](/chemistry/1001-ph-poh-strong-acids-bases) | [Acid Strength and Structure →](/chemistry/1003-molecular-structure-acid-strength)

</div>
