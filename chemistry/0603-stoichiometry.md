# Stoichiometry
<p class="article-date">July 5, 2026</p>

*The junior class bake sale is in two days and I signed us up to bring 240 chocolate chip cookies, which — okay — was ambitious. My go-to recipe is basically a balanced equation: 2 cups flour + 1 cup sugar + 3 eggs makes 24 cookies. So 240 cookies is just ten batches, which means I scale every single ingredient by ten: 20 cups flour, 10 cups sugar, 30 eggs. Simple ratio, done. Except when I actually check the fridge, I have a giant bag of flour, a full canister of sugar... and only 6 eggs. It doesn't matter that I own a mountain of flour — 6 eggs caps me at 48 cookies, full stop, and I'll have leftover flour sitting on the counter mocking me. Then three cookies burn in the oven, so I pull out 45, not 48. Congratulations, you just did all of stoichiometry: the recipe ratios are mole ratios, the eggs are the limiting reactant, the leftover flour is excess, and 45-out-of-48 is percent yield. This is the beating heart of AP Chemistry Unit 4 — the skill that shows up on literally every FRQ — so let's actually nail it.*

---

## What You'll Learn

- Read the coefficients of a balanced equation as **mole ratios** and use them as the only bridge between one substance and another
- Run the full **mole map** for reactions: grams A → mol A → mol B → grams B, showing units at every step
- Solve **mole-to-mole**, **mass-to-mole**, and **mass-to-mass** stoichiometry problems fluently
- Convert to and from **particles** (using $N_A$) and **gas volumes** (using $PV = nRT$) inside a stoichiometry chain
- Identify the **limiting reactant** two reliable ways — the "compute the product from each" method and the "compare mole ratios" method
- Find the **excess reactant** and calculate exactly how much of it is left over
- Distinguish **theoretical yield** from **actual yield** and compute **percent yield** in both directions
- Attack a **multi-step FRQ** that combines limiting reactant *and* percent yield — the classic Unit 4 shape
- Show enough labeled work at each step to earn full AP work-shown credit

---

## Prerequisites

- [The Mole](/chemistry/0207-the-mole) — molar mass is your grams↔moles converter, and the "mole map" from that article is about to grow a whole new branch; this is non-negotiable
- [Balancing Equations](/chemistry/0206-balancing-equations) — a stoichiometry problem is worthless if the equation isn't balanced first, because the **coefficients ARE the mole ratios**
- [Dimensional Analysis](/chemistry/0103-dimensional-analysis) — every calculation here is a railroad of unit fractions where units cancel diagonally; if you trust the units, you cannot get lost

---

## The Core Concept

### Intuition First

Let's stay in the kitchen, because the cookie recipe secretly contains every idea in this article.

Here's the recipe written like a chemist would write it:

$$2\ \text{flour} + 1\ \text{sugar} + 3\ \text{egg} \longrightarrow 24\ \text{cookie}$$

The numbers in front are **ratios**, and ratios are the whole game. They tell you: for every 3 eggs you commit, you get 24 cookies. For every 2 cups of flour, 24 cookies. These aren't "amounts" — a recipe doesn't say you must bake exactly 24 cookies ever — they're *proportions*. Want ten times the cookies? Multiply every ingredient by ten. The **ratios never change**; only the scale does.

Now here's the leap. A balanced chemical equation is the exact same recipe card:

$$\ce{2H2 + O2 -> 2H2O}$$

reads as "**2** molecules of $\ce{H2}$ react with **1** molecule of $\ce{O2}$ to make **2** molecules of $\ce{H2O}$." And because a mole is just a (huge) count, the very same coefficients also read as "**2 moles** $\ce{H2}$ react with **1 mole** $\ce{O2}$ to make **2 moles** $\ce{H2O}$." The coefficients are mole ratios. That's the single most important sentence in Unit 4.

Map the kitchen onto the chemistry and it's one-to-one:

| Bake sale | Chemistry |
|---|---|
| recipe ratios (2 : 1 : 3 : 24) | **coefficients** of the balanced equation |
| scaling the recipe up ×10 | **mole ratios** (proportions hold at any scale) |
| the ingredient you run out of first (eggs) | **limiting reactant** |
| the flour left sitting on the counter | **excess reactant** |
| cookies you actually pulled out (45) vs. the recipe's promise (48) | **percent yield** |

Everything below is just making this table quantitative.

### The Only Bridge: The Mole Ratio

Here's the rule that trips up more students than anything else, so read it slowly:

> **You can never convert directly from grams of one substance to grams of another. The bridge between two different substances is ALWAYS a mole ratio — and mole ratios only exist in moles.**

Think about why. Grams are about *mass*; the coefficients in an equation count *particles*, not mass. 2 cups of flour and 1 cup of sugar are a 2:1 ratio *by cups*, not by weight — a cup of flour and a cup of sugar don't weigh the same. In chemistry it's identical: $\ce{2H2 + O2}$ is 2:1 *by molecules/moles*, and $\ce{H2}$ and $\ce{O2}$ have different molar masses. So you must be in "mole currency" before you're allowed to cross from one substance to another.

### The Master Mole Map (Extended to Reactions)

Back in [The Mole](/chemistry/0207-the-mole), you learned the local mole map for a single substance: **grams ↔ moles ↔ particles**, with molar mass and $N_A$ as the two converters. Stoichiometry bolts a *second copy* of that map onto the first and joins them with the mole-ratio bridge:

$$
\underbrace{\text{grams A}}_{\text{weigh it}}
\;\xrightarrow[\text{molar mass A}]{\div}\;
\underbrace{\text{mol A}}_{}
\;\xrightarrow[\text{mole ratio}]{\times \frac{\text{coeff B}}{\text{coeff A}}}\;
\underbrace{\text{mol B}}_{}
\;\xrightarrow[\text{molar mass B}]{\times}\;
\underbrace{\text{grams B}}_{\text{the answer}}
$$

That's the whole railroad. Three moves, always in this order:

1. **Get to moles of what you're given.** (Divide grams by molar mass of A, or use $N_A$ from particles, or use $PV=nRT$ from a gas.)
2. **Cross the bridge.** Multiply by the mole ratio $\dfrac{\text{coefficient of B}}{\text{coefficient of A}}$, taken straight off the balanced equation. **B on top, A on bottom** — the thing you *want* goes up top.
3. **Leave moles for whatever the question asked for.** (Multiply by molar mass of B for grams, or by $N_A$ for particles, or rearrange $PV=nRT$ for a gas volume.)

Every stoichiometry problem — mole-to-mole, mass-to-mass, mass-to-particles, gas volumes, all of it — is just a subset of this one diagram. You get on the railroad wherever your "given" lets you, and you get off wherever the question wants you. Notice steps 1 and 3 are exactly the mole-map conversions you already own; step 2 is the *only* genuinely new idea in this entire article.

Written as a dimensional-analysis chain, the flagship mass-to-mass problem looks like this:

$$
\text{g A} \times \frac{1\ \text{mol A}}{\text{molar mass A}} \times \frac{\text{coeff B}}{\text{coeff A}} \times \frac{\text{molar mass B}}{1\ \text{mol B}} = \text{g B}
$$

Watch the units cancel diagonally: grams A cancels, mol A cancels, mol B cancels, and you're left holding grams B. If your units don't cancel to the thing you want, you flipped a fraction — the units are your error-checker.

---

## Worked Examples

Unless a problem gives you a balanced equation, **balance it first** — every mole ratio depends on it. I'll use molar masses rounded to two decimals.

### Example 1: Mole-to-Mole (the pure bridge)

**Problem:** For $\ce{N2 + 3H2 -> 2NH3}$, how many moles of $\ce{NH3}$ form from 4.50 mol of $\ce{H2}$ (with plenty of $\ce{N2}$)?

**Solution:**

Already in moles, and already balanced — so we only need step 2, the bridge. Want $\ce{NH3}$ (coeff 2), given $\ce{H2}$ (coeff 3):

$$4.50\ \text{mol}\ \ce{H2} \times \frac{2\ \text{mol}\ \ce{NH3}}{3\ \text{mol}\ \ce{H2}} = 3.00\ \text{mol}\ \ce{NH3}$$

**Answer:** $3.00\ \text{mol}\ \ce{NH3}$.

### Example 2: Mole-to-Mole, the other direction

**Problem:** Same reaction. How many moles of $\ce{H2}$ are needed to *fully consume* 0.80 mol of $\ce{N2}$?

**Solution:**

Want $\ce{H2}$ (coeff 3), given $\ce{N2}$ (coeff 1). The wanted substance goes on top:

$$0.80\ \text{mol}\ \ce{N2} \times \frac{3\ \text{mol}\ \ce{H2}}{1\ \text{mol}\ \ce{N2}} = 2.40\ \text{mol}\ \ce{H2}$$

**Answer:** $2.40\ \text{mol}\ \ce{H2}$. (Flip the ratio and you'd get 0.27 — the units would still say mol, which is why students miss it. Always ask: *am I making more of the small-coefficient thing or the big one?*)

### Example 3: Mass-to-Mole

**Problem:** For $\ce{2KClO3 -> 2KCl + 3O2}$, how many moles of $\ce{O2}$ are produced by decomposing 24.5 g of $\ce{KClO3}$?

**Solution:**

**Step 1 — grams A to moles A.** Molar mass of $\ce{KClO3}$ = $39.10 + 35.45 + 3(16.00) = 122.55\ \text{g/mol}$.

$$24.5\ \text{g}\ \ce{KClO3} \times \frac{1\ \text{mol}}{122.55\ \text{g}} = 0.1999\ \text{mol}\ \ce{KClO3}$$

**Step 2 — bridge.** Want $\ce{O2}$ (coeff 3), given $\ce{KClO3}$ (coeff 2):

$$0.1999\ \text{mol}\ \ce{KClO3} \times \frac{3\ \text{mol}\ \ce{O2}}{2\ \text{mol}\ \ce{KClO3}} = 0.300\ \text{mol}\ \ce{O2}$$

**Answer:** $0.300\ \text{mol}\ \ce{O2}$.

### Example 4: Mass-to-Mass (the flagship)

**Problem:** In the thermite reaction $\ce{2Al + Fe2O3 -> Al2O3 + 2Fe}$, what mass of iron is produced from 15.0 g of aluminum (excess $\ce{Fe2O3}$)?

**Solution:** Run the full railroad, all three moves in one chain.

**Step 1 — g Al → mol Al.** Molar mass $\ce{Al}$ = 26.98 g/mol.

**Step 2 — mole ratio.** Want $\ce{Fe}$ (coeff 2), given $\ce{Al}$ (coeff 2), so the ratio is 2/2 = 1.

**Step 3 — mol Fe → g Fe.** Molar mass $\ce{Fe}$ = 55.85 g/mol.

$$15.0\ \text{g}\ \ce{Al} \times \frac{1\ \text{mol}\ \ce{Al}}{26.98\ \text{g}} \times \frac{2\ \text{mol}\ \ce{Fe}}{2\ \text{mol}\ \ce{Al}} \times \frac{55.85\ \text{g}\ \ce{Fe}}{1\ \text{mol}\ \ce{Fe}} = 31.0\ \text{g}\ \ce{Fe}$$

**Answer:** $31.0\ \text{g}\ \ce{Fe}$. Notice how every unit except "g Fe" cancels — that's your proof the chain is set up right.

### Example 5: Mass-to-Mass with a non-trivial ratio

**Problem:** Ammonia burns: $\ce{4NH3 + 5O2 -> 4NO + 6H2O}$. What mass of $\ce{NO}$ forms from 34.0 g of $\ce{NH3}$ (excess $\ce{O2}$)?

**Solution:**

Molar masses: $\ce{NH3} = 14.01 + 3(1.008) = 17.03\ \text{g/mol}$; $\ce{NO} = 14.01 + 16.00 = 30.01\ \text{g/mol}$. Ratio: want $\ce{NO}$ (4), given $\ce{NH3}$ (4) → 4/4 = 1.

$$34.0\ \text{g}\ \ce{NH3} \times \frac{1\ \text{mol}}{17.03\ \text{g}} \times \frac{4\ \text{mol}\ \ce{NO}}{4\ \text{mol}\ \ce{NH3}} \times \frac{30.01\ \text{g}}{1\ \text{mol}} = 59.9\ \text{g}\ \ce{NO}$$

**Answer:** $59.9\ \text{g}\ \ce{NO}$.

### Example 6: Mass-to-Mass with a 2:3 ratio

**Problem:** Rust forms by $\ce{4Fe + 3O2 -> 2Fe2O3}$. What mass of $\ce{O2}$ is consumed when 100.0 g of $\ce{Fe}$ fully rusts?

**Solution:**

$\ce{Fe}$ = 55.85 g/mol; $\ce{O2}$ = 32.00 g/mol. Want $\ce{O2}$ (3), given $\ce{Fe}$ (4):

$$100.0\ \text{g}\ \ce{Fe} \times \frac{1\ \text{mol}}{55.85\ \text{g}} \times \frac{3\ \text{mol}\ \ce{O2}}{4\ \text{mol}\ \ce{Fe}} \times \frac{32.00\ \text{g}}{1\ \text{mol}} = 43.0\ \text{g}\ \ce{O2}$$

**Answer:** $43.0\ \text{g}\ \ce{O2}$.

### Example 7: Mass-to-Particles

**Problem:** For $\ce{CaCO3 -> CaO + CO2}$, how many molecules of $\ce{CO2}$ are released by decomposing 50.0 g of $\ce{CaCO3}$?

**Solution:**

Same railroad, but the last stop is particles (use $N_A$) instead of grams. $\ce{CaCO3}$ = $40.08 + 12.01 + 3(16.00) = 100.09\ \text{g/mol}$; ratio 1:1.

$$50.0\ \text{g}\ \ce{CaCO3} \times \frac{1\ \text{mol}}{100.09\ \text{g}} \times \frac{1\ \text{mol}\ \ce{CO2}}{1\ \text{mol}\ \ce{CaCO3}} \times \frac{6.022 \times 10^{23}\ \text{molec}}{1\ \text{mol}} = 3.01 \times 10^{23}\ \text{molecules}$$

**Answer:** $3.01 \times 10^{23}$ molecules of $\ce{CO2}$.

### Example 8: Gas-Volume Stoichiometry via $PV = nRT$

**Problem:** Zinc reacts with acid: $\ce{Zn + 2HCl -> ZnCl2 + H2}$. If 6.54 g of $\ce{Zn}$ reacts completely, what **volume** of $\ce{H2}$ gas is collected at $P = 1.00\ \text{atm}$ and $T = 298\ \text{K}$?

**Solution:** Get to moles of the gas the normal way, then jump off the railroad using the [ideal gas law](/chemistry/0504-ideal-gas-law) instead of a molar mass.

**Step 1 — g Zn → mol Zn.** $\ce{Zn}$ = 65.38 g/mol → $6.54 / 65.38 = 0.1000\ \text{mol}\ \ce{Zn}$.

**Step 2 — bridge.** Want $\ce{H2}$ (1), given $\ce{Zn}$ (1) → ratio 1, so $0.1000\ \text{mol}\ \ce{H2}$.

**Step 3 — moles → volume with $PV = nRT$.** Solve for $V$, using $R = 0.08206\ \frac{\text{L·atm}}{\text{mol·K}}$:

$$V = \frac{nRT}{P} = \frac{(0.1000\ \text{mol})(0.08206\ \tfrac{\text{L·atm}}{\text{mol·K}})(298\ \text{K})}{1.00\ \text{atm}} = 2.45\ \text{L}$$

**Answer:** $2.45\ \text{L}$ of $\ce{H2}$. The mole map handed off to $PV=nRT$ at exactly the "moles" stop.

### Example 9: Limiting Reactant — Method A (compute product from each)

**Problem:** $\ce{N2 + 3H2 -> 2NH3}$. You mix 2.0 mol $\ce{N2}$ with 3.0 mol $\ce{H2}$. Which is limiting, and how many moles of $\ce{NH3}$ form?

**Solution:** This is the eggs-and-flour problem. **Method A: pretend each reactant is the one that runs out, compute how much product it would make, and the *smaller* answer wins** (because you can't make more product than your scarcest ingredient allows).

*If $\ce{N2}$ ran out:* $2.0\ \text{mol}\ \ce{N2} \times \dfrac{2\ \text{mol}\ \ce{NH3}}{1\ \text{mol}\ \ce{N2}} = 4.0\ \text{mol}\ \ce{NH3}$.

*If $\ce{H2}$ ran out:* $3.0\ \text{mol}\ \ce{H2} \times \dfrac{2\ \text{mol}\ \ce{NH3}}{3\ \text{mol}\ \ce{H2}} = 2.0\ \text{mol}\ \ce{NH3}$.

The $\ce{H2}$ path gives less (2.0 < 4.0), so **$\ce{H2}$ is the limiting reactant** — it's the eggs. It caps the yield.

**Answer:** $\ce{H2}$ is limiting; $2.0\ \text{mol}\ \ce{NH3}$ forms. ($\ce{N2}$ is in excess.)

### Example 10: Limiting Reactant — Method B (compare mole ratios)

**Problem:** Same numbers as Example 9 (2.0 mol $\ce{N2}$, 3.0 mol $\ce{H2}$), but let's confirm with the other method.

**Solution:** **Method B: compare what you *have* to what the recipe *demands*.** The equation demands $\ce{H2}:\ce{N2} = 3:1$. What do you actually have?

$$\frac{\text{mol}\ \ce{H2}}{\text{mol}\ \ce{N2}} = \frac{3.0}{2.0} = 1.5$$

You have 1.5 mol $\ce{H2}$ per mol $\ce{N2}$, but the recipe needs 3. You're **short on $\ce{H2}$** relative to the recipe → **$\ce{H2}$ is limiting.** Same verdict as Method A. Method B is faster once you trust it; Method A also *hands you the product amount for free*, which is why I default to A on FRQs.

**Answer:** $\ce{H2}$ limiting — consistent with Example 9.

### Example 11: Limiting Reactant from Masses + How Much Excess Is Left

**Problem:** $\ce{2Al + 3Cl2 -> 2AlCl3}$. You react 5.40 g $\ce{Al}$ with 21.3 g $\ce{Cl2}$. (a) What mass of $\ce{AlCl3}$ forms? (b) How much of the excess reactant remains?

**Solution:**

**Step 1 — moles of each.** $\ce{Al}$: $5.40 / 26.98 = 0.2001\ \text{mol}$. $\ce{Cl2}$: $21.3 / 70.90 = 0.3004\ \text{mol}$.

**Step 2 — limiting reactant (Method A), in moles of product.**

*From $\ce{Al}$:* $0.2001 \times \dfrac{2\ \ce{AlCl3}}{2\ \ce{Al}} = 0.2001\ \text{mol}\ \ce{AlCl3}$.

*From $\ce{Cl2}$:* $0.3004 \times \dfrac{2\ \ce{AlCl3}}{3\ \ce{Cl2}} = 0.2003\ \text{mol}\ \ce{AlCl3}$.

Nearly a tie, but $\ce{Al}$ gives *slightly* less → **$\ce{Al}$ is limiting**, and $\ce{Cl2}$ is in excess. Product = 0.2001 mol $\ce{AlCl3}$.

**(a)** Convert to grams. $\ce{AlCl3}$ = $26.98 + 3(35.45) = 133.33\ \text{g/mol}$:

$$0.2001\ \text{mol} \times 133.33\ \text{g/mol} = 26.7\ \text{g}\ \ce{AlCl3}$$

**(b) Excess left over — the follow-up AP loves.** Find how much $\ce{Cl2}$ the limiting $\ce{Al}$ actually *used*, then subtract from what you started with.

$$\text{used: } 0.2001\ \text{mol}\ \ce{Al} \times \frac{3\ \text{mol}\ \ce{Cl2}}{2\ \text{mol}\ \ce{Al}} = 0.3002\ \text{mol}\ \ce{Cl2}$$

$$\text{left: } 0.3004 - 0.3002 = 0.0002\ \text{mol}\ \ce{Cl2}\ \text{... essentially all consumed here.}$$

Let me redo with cleaner numbers so the leftover is visible — suppose instead you had **30.0 g $\ce{Cl2}$** ($= 0.4231\ \text{mol}$) with the same 5.40 g $\ce{Al}$. Then $\ce{Al}$ is clearly limiting, it still uses $0.3002\ \text{mol}\ \ce{Cl2}$, and:

$$\text{left: } 0.4231 - 0.3002 = 0.1229\ \text{mol}\ \ce{Cl2} \times 70.90\ \text{g/mol} = 8.71\ \text{g}\ \ce{Cl2}\ \text{remaining}$$

**Answer:** (a) $26.7\ \text{g}\ \ce{AlCl3}$; (b) with 30.0 g $\ce{Cl2}$ supplied, **8.71 g $\ce{Cl2}$ is left over**. The recipe for "excess remaining" is always: *(started) − (used by the limiting reactant)*.

### Example 12: Percent Yield (forward)

**Problem:** A reaction has a **theoretical yield** of 26.7 g $\ce{AlCl3}$ (from Example 11a), but you actually isolate 23.4 g. What is the percent yield?

**Solution:** This is the burned-cookies step. Theoretical yield is what the stoichiometry *promised* (48 cookies); actual yield is what you *pulled out of the oven* (45).

$$\%\ \text{yield} = \frac{\text{actual yield}}{\text{theoretical yield}} \times 100\% = \frac{23.4\ \text{g}}{26.7\ \text{g}} \times 100\% = 87.6\%$$

**Answer:** $87.6\%$. (Actual is always ≤ theoretical, so a legit percent yield is ≤ 100%. If you get 130%, you divided upside-down or your product is wet/impure.)

### Example 13: Percent Yield (back-calculating actual yield)

**Problem:** The reaction $\ce{CaCO3 -> CaO + CO2}$ has a theoretical yield of 40.0 g $\ce{CaO}$ and runs at **85.0% yield**. How many grams of $\ce{CaO}$ do you actually get?

**Solution:** Rearrange the percent-yield formula for actual yield:

$$\text{actual} = \frac{\%\ \text{yield}}{100} \times \text{theoretical} = 0.850 \times 40.0\ \text{g} = 34.0\ \text{g}\ \ce{CaO}$$

**Answer:** $34.0\ \text{g}\ \ce{CaO}$.

### Example 14: Percent Yield (working backward to required starting mass)

**Problem:** You need to *actually produce* 50.0 g of $\ce{CaO}$ from $\ce{CaCO3 -> CaO + CO2}$, but your setup only runs at **80.0% yield**. What mass of $\ce{CaCO3}$ must you start with?

**Solution:** Two moves: first inflate the target to a *theoretical* target (since you'll lose 20%), then run the mole map backward from $\ce{CaO}$ to $\ce{CaCO3}$.

**Step 1 — required theoretical yield.** $\text{theoretical} = \dfrac{\text{actual}}{\%/100} = \dfrac{50.0}{0.800} = 62.5\ \text{g}\ \ce{CaO}$.

**Step 2 — mass-to-mass, product → reactant.** $\ce{CaO}$ = 56.08 g/mol; $\ce{CaCO3}$ = 100.09 g/mol; ratio 1:1:

$$62.5\ \text{g}\ \ce{CaO} \times \frac{1\ \text{mol}}{56.08\ \text{g}} \times \frac{1\ \text{mol}\ \ce{CaCO3}}{1\ \text{mol}\ \ce{CaO}} \times \frac{100.09\ \text{g}}{1\ \text{mol}} = 112\ \text{g}\ \ce{CaCO3}$$

**Answer:** You must start with $112\ \text{g}\ \ce{CaCO3}$. (Notice you'd need *more* starting material than a perfect reaction would require — that's the cost of an 80% yield.)

### Example 15: The Capstone — Limiting Reactant *and* Percent Yield Together

**Problem:** This is the shape of a real Unit 4 FRQ. Ammonia is made by $\ce{N2 + 3H2 -> 2NH3}$. A reactor is charged with **28.0 g $\ce{N2}$** and **7.50 g $\ce{H2}$**, and it produces **26.0 g $\ce{NH3}$**. (a) Identify the limiting reactant. (b) Find the theoretical yield of $\ce{NH3}$. (c) Calculate the percent yield.

**Solution:**

**Step 1 — moles of each reactant.**
$\ce{N2}$: $28.0 / 28.02 = 0.9993\ \text{mol}$.
$\ce{H2}$: $7.50 / 2.016 = 3.720\ \text{mol}$.

**Step 2 — (a) limiting reactant, Method A.**

*From $\ce{N2}$:* $0.9993 \times \dfrac{2\ \ce{NH3}}{1\ \ce{N2}} = 1.999\ \text{mol}\ \ce{NH3}$.

*From $\ce{H2}$:* $3.720 \times \dfrac{2\ \ce{NH3}}{3\ \ce{H2}} = 2.480\ \text{mol}\ \ce{NH3}$.

$\ce{N2}$ gives less → **$\ce{N2}$ is limiting** (it's the eggs); $\ce{H2}$ is in excess.

**Step 3 — (b) theoretical yield.** Use the limiting-reactant product, 1.999 mol $\ce{NH3}$. Molar mass $\ce{NH3}$ = 17.03 g/mol:

$$1.999\ \text{mol} \times 17.03\ \text{g/mol} = 34.0\ \text{g}\ \ce{NH3}\ \text{(theoretical)}$$

**Step 4 — (c) percent yield.** Actual = 26.0 g:

$$\%\ \text{yield} = \frac{26.0\ \text{g}}{34.0\ \text{g}} \times 100\% = 76.5\%$$

**Answer:** (a) $\ce{N2}$ is limiting; (b) theoretical yield = $34.0\ \text{g}\ \ce{NH3}$; (c) percent yield = $76.5\%$. That three-part structure — *limiting → theoretical → percent* — is the skeleton of almost every stoichiometry FRQ. Memorize the order.

---

> **🎬 Hollywood Chemistry: Real or Not?**
> *The scene:* In *The Martian*, stranded astronaut Mark Watney needs liquid water to grow potatoes, so he makes it from scratch — he burns leftover rocket fuel hydrazine ($\ce{N2H4}$) over an iridium catalyst to liberate hydrogen, then carefully ignites that hydrogen with oxygen from his habitat so it combines into water.
> *The verdict:* The **stoichiometry is completely real**, and it's the exact accounting this article teaches. Splitting hydrazine gives hydrogen, $\ce{N2H4 -> N2 + 2H2}$, and then $\ce{2H2 + O2 -> 2H2O}$ — hydrogen and oxygen combine in a fixed 2:1 mole ratio, so Watney has to bookkeep how much $\ce{H2}$ he's releasing against how much $\ce{O2}$ he can spare, or someone becomes the limiting reactant and he either wastes fuel or blows up the hab. That's *literally* limiting-reactant reasoning done to stay alive. What the movie soft-pedals is the danger: hydrazine is brutally toxic and the $\ce{H2}$–$\ce{O2}$ reaction is explosively fast (Watney does, in the book, nearly blow himself up). So: the chemical *accounting* is legit AP-Chem-grade stoichiometry; the "calmly do this in your living-room-sized habitat" part is the Hollywood liberty. Real chemistry, dramatized safety.

---

## Common Mistakes

| The mistake | Why it happens | How to avoid it |
|---|---|---|
| Using an **unbalanced** equation | You dive into the numbers before checking coefficients | Balance first, every time — the mole ratio is *only* valid for a balanced equation |
| Trying to go **grams → grams directly** | Grams feel like the "real" unit | You must pass through moles; the mole ratio bridge only works in moles |
| **Flipping the mole ratio** | Not tracking which substance is wanted vs. given | Wanted substance on **top**, given on **bottom**; check that the "given" unit cancels |
| Picking the limiting reactant by **which mass is smaller** | Mass ≠ moles ≠ recipe demand | Convert to moles first; a small mass of a light molecule can be a *large* number of moles |
| Computing theoretical yield from the **excess** reactant | You grabbed the wrong number | Theoretical yield always comes from the **limiting** reactant |
| Percent yield **over 100%** | Divided theoretical by actual, or product was impure/wet | Formula is actual ÷ theoretical; a clean answer is ≤ 100% |
| Forgetting the **"how much excess is left"** part | You stopped at the product | Excess remaining = (started) − (used by limiting reactant) |
| Dropping **units** mid-chain | Rushing the algebra | Write the unit on every number; if units don't cancel to the target, you set it up wrong |

---

## AP Exam Tips

- **Show units at every railroad step.** On the free-response section, work-shown credit is real: a labeled chain (g → mol → mol → g) with units that visibly cancel earns points even if your final arithmetic slips. A bare string of numbers does not.
- **Limiting reactant appears on nearly every stoichiometry FRQ.** If a problem hands you *masses of two or more reactants*, that's the signal — you're expected to determine the limiting reactant, not assume one. Never skip that check.
- **Theoretical yield always comes from the limiting reactant.** Compute the product from the limiting reactant *only*; the excess reactant's number is a trap.
- **Percent yield direction matters.** It's $\dfrac{\text{actual}}{\text{theoretical}} \times 100\%$. Actual is what you measured/collected; theoretical is what the stoichiometry predicts. Given a percent yield, you can go *either* way — inflate a target up to a theoretical, or discount a theoretical down to an actual.
- **Watch for the "how much excess is left?" follow-up.** It's an easy add-on that students forget. Remaining excess = started − used-by-limiting-reactant. It's worth its own point.
- **Gas stoichiometry = normal stoichiometry + $PV = nRT$.** If a reactant or product is a gas given by volume/pressure/temperature, use the [ideal gas law](/chemistry/0504-ideal-gas-law) to enter or exit the mole map at the "moles" stop. Don't reach for 22.4 L/mol unless the problem is explicitly at STP.
- **Round molar masses consistently** (usually 2 decimals) and don't round intermediate steps hard — carry an extra digit and round only the final answer to the right sig figs.

---

## Practice Problems

Balance any equation that isn't balanced before you start. Molar masses: use two decimals from the periodic table.

### Problem 1
For $\ce{2H2 + O2 -> 2H2O}$, how many moles of water form from 5.0 mol of $\ce{O2}$ (excess $\ce{H2}$)?

<details>
<summary><strong>Solution</strong></summary>

Want $\ce{H2O}$ (coeff 2), given $\ce{O2}$ (coeff 1):

$$5.0\ \text{mol}\ \ce{O2} \times \frac{2\ \text{mol}\ \ce{H2O}}{1\ \text{mol}\ \ce{O2}} = 10.0\ \text{mol}\ \ce{H2O}$$

**Answer:** $10.\ \text{mol}\ \ce{H2O}$.

</details>

---

### Problem 2
$\ce{C3H8 + 5O2 -> 3CO2 + 4H2O}$. How many moles of $\ce{CO2}$ come from 2.5 mol of propane $\ce{C3H8}$?

<details>
<summary><strong>Solution</strong></summary>

Want $\ce{CO2}$ (3), given $\ce{C3H8}$ (1):

$$2.5\ \text{mol}\ \ce{C3H8} \times \frac{3\ \text{mol}\ \ce{CO2}}{1\ \text{mol}\ \ce{C3H8}} = 7.5\ \text{mol}\ \ce{CO2}$$

**Answer:** $7.5\ \text{mol}\ \ce{CO2}$.

</details>

---

### Problem 3
For $\ce{2Na + Cl2 -> 2NaCl}$, how many grams of $\ce{NaCl}$ form from 4.60 g of $\ce{Na}$ (excess $\ce{Cl2}$)?

<details>
<summary><strong>Solution</strong></summary>

$\ce{Na}$ = 22.99 g/mol; $\ce{NaCl}$ = 58.44 g/mol; ratio 2:2 = 1.

$$4.60\ \text{g}\ \ce{Na} \times \frac{1\ \text{mol}}{22.99\ \text{g}} \times \frac{2\ \ce{NaCl}}{2\ \ce{Na}} \times \frac{58.44\ \text{g}}{1\ \text{mol}} = 11.7\ \text{g}\ \ce{NaCl}$$

**Answer:** $11.7\ \text{g}\ \ce{NaCl}$.

</details>

---

### Problem 4
Iron(III) oxide is reduced: $\ce{Fe2O3 + 3CO -> 2Fe + 3CO2}$. What mass of iron is produced from 160.0 g of $\ce{Fe2O3}$ (excess $\ce{CO}$)?

<details>
<summary><strong>Solution</strong></summary>

$\ce{Fe2O3}$ = $2(55.85) + 3(16.00) = 159.70\ \text{g/mol}$; $\ce{Fe}$ = 55.85 g/mol; ratio want $\ce{Fe}$ (2) / given $\ce{Fe2O3}$ (1).

$$160.0\ \text{g} \times \frac{1\ \text{mol}}{159.70\ \text{g}} \times \frac{2\ \ce{Fe}}{1\ \ce{Fe2O3}} \times \frac{55.85\ \text{g}}{1\ \text{mol}} = 111.9\ \text{g}\ \ce{Fe}$$

**Answer:** $\approx 112\ \text{g}\ \ce{Fe}$.

</details>

---

### Problem 5
For $\ce{2KClO3 -> 2KCl + 3O2}$, how many grams of $\ce{KClO3}$ are needed to produce 96.0 g of $\ce{O2}$?

<details>
<summary><strong>Solution</strong></summary>

$\ce{O2}$ = 32.00 g/mol → $96.0 / 32.00 = 3.00\ \text{mol}\ \ce{O2}$. Want $\ce{KClO3}$ (2) / given $\ce{O2}$ (3). $\ce{KClO3}$ = 122.55 g/mol.

$$3.00\ \text{mol}\ \ce{O2} \times \frac{2\ \ce{KClO3}}{3\ \ce{O2}} \times \frac{122.55\ \text{g}}{1\ \text{mol}} = 245\ \text{g}\ \ce{KClO3}$$

**Answer:** $245\ \text{g}\ \ce{KClO3}$.

</details>

---

### Problem 6
How many molecules of $\ce{H2O}$ are produced when 8.00 g of $\ce{CH4}$ combusts fully? $\ce{CH4 + 2O2 -> CO2 + 2H2O}$.

<details>
<summary><strong>Solution</strong></summary>

$\ce{CH4}$ = 16.04 g/mol → $8.00 / 16.04 = 0.4988\ \text{mol}$. Want $\ce{H2O}$ (2) / given $\ce{CH4}$ (1), then use $N_A$.

$$0.4988\ \text{mol}\ \ce{CH4} \times \frac{2\ \ce{H2O}}{1\ \ce{CH4}} \times 6.022 \times 10^{23} = 6.01 \times 10^{23}\ \text{molecules}$$

**Answer:** $6.01 \times 10^{23}$ molecules of $\ce{H2O}$.

</details>

---

### Problem 7
$\ce{CaCO3 + 2HCl -> CaCl2 + H2O + CO2}$. What volume of $\ce{CO2}$ gas (at 1.00 atm, 273 K) forms from 25.0 g of $\ce{CaCO3}$ (excess acid)?

<details>
<summary><strong>Solution</strong></summary>

$\ce{CaCO3}$ = 100.09 g/mol → $25.0/100.09 = 0.2498\ \text{mol}$. Ratio 1:1 → 0.2498 mol $\ce{CO2}$. Then $PV=nRT$:

$$V = \frac{nRT}{P} = \frac{(0.2498)(0.08206)(273)}{1.00} = 5.60\ \text{L}$$

**Answer:** $5.60\ \text{L}\ \ce{CO2}$.

</details>

---

### Problem 8
$\ce{2H2 + O2 -> 2H2O}$. You mix 4.0 mol $\ce{H2}$ with 3.0 mol $\ce{O2}$. Which is limiting, and how many moles of water form?

<details>
<summary><strong>Solution</strong></summary>

Method A. *From $\ce{H2}$:* $4.0 \times \frac{2}{2} = 4.0\ \text{mol}\ \ce{H2O}$. *From $\ce{O2}$:* $3.0 \times \frac{2}{1} = 6.0\ \text{mol}\ \ce{H2O}$. Smaller is 4.0 → **$\ce{H2}$ is limiting**.

**Answer:** $\ce{H2}$ limiting; $4.0\ \text{mol}\ \ce{H2O}$ ($\ce{O2}$ in excess).

</details>

---

### Problem 9
$\ce{N2 + 3H2 -> 2NH3}$. Mix 1.0 mol $\ce{N2}$ and 4.0 mol $\ce{H2}$. Find the limiting reactant and the moles of the excess reactant left over.

<details>
<summary><strong>Solution</strong></summary>

Method B: recipe needs $\ce{H2}:\ce{N2} = 3:1$; you have $4.0/1.0 = 4$, more $\ce{H2}$ than required → **$\ce{N2}$ is limiting**. $\ce{N2}$ uses $1.0 \times \frac{3}{1} = 3.0\ \text{mol}\ \ce{H2}$. Left over: $4.0 - 3.0 = 1.0\ \text{mol}\ \ce{H2}$.

**Answer:** $\ce{N2}$ limiting; $1.0\ \text{mol}\ \ce{H2}$ remains.

</details>

---

### Problem 10
$\ce{2Al + 3Cl2 -> 2AlCl3}$. React 8.10 g $\ce{Al}$ with 42.0 g $\ce{Cl2}$. (a) Limiting reactant? (b) Mass of $\ce{AlCl3}$ formed?

<details>
<summary><strong>Solution</strong></summary>

$\ce{Al}$: $8.10/26.98 = 0.3002\ \text{mol}$. $\ce{Cl2}$: $42.0/70.90 = 0.5924\ \text{mol}$.

*From $\ce{Al}$:* $0.3002 \times \frac{2}{2} = 0.3002\ \text{mol}\ \ce{AlCl3}$. *From $\ce{Cl2}$:* $0.5924 \times \frac{2}{3} = 0.3949\ \text{mol}$. Smaller → **$\ce{Al}$ limiting**.

$\ce{AlCl3}$ = 133.33 g/mol: $0.3002 \times 133.33 = 40.0\ \text{g}$.

**Answer:** (a) $\ce{Al}$ limiting; (b) $40.0\ \text{g}\ \ce{AlCl3}$.

</details>

---

### Problem 11
Using Problem 10's numbers, how many grams of the excess reactant ($\ce{Cl2}$) remain?

<details>
<summary><strong>Solution</strong></summary>

$\ce{Al}$ (limiting, 0.3002 mol) uses $0.3002 \times \frac{3\ \ce{Cl2}}{2\ \ce{Al}} = 0.4503\ \text{mol}\ \ce{Cl2}$. Started with 0.5924 mol.

Left: $0.5924 - 0.4503 = 0.1421\ \text{mol} \times 70.90\ \text{g/mol} = 10.1\ \text{g}\ \ce{Cl2}$.

**Answer:** $10.1\ \text{g}\ \ce{Cl2}$ remains.

</details>

---

### Problem 12
A reaction's theoretical yield is 55.0 g of product, but only 48.4 g is isolated. What is the percent yield?

<details>
<summary><strong>Solution</strong></summary>

$$\%\ \text{yield} = \frac{48.4}{55.0} \times 100\% = 88.0\%$$

**Answer:** $88.0\%$.

</details>

---

### Problem 13
The synthesis of aspirin has a theoretical yield of 12.0 g and runs at 92.0% yield. How many grams of aspirin do you actually collect?

<details>
<summary><strong>Solution</strong></summary>

$$\text{actual} = 0.920 \times 12.0\ \text{g} = 11.0\ \text{g}$$

**Answer:** $11.0\ \text{g}$ of aspirin.

</details>

---

### Problem 14
You need to actually produce 30.0 g of $\ce{NH3}$ from $\ce{N2 + 3H2 -> 2NH3}$ at 75.0% yield. What theoretical yield of $\ce{NH3}$ must the reaction be designed for, and what mass of $\ce{N2}$ does that require (excess $\ce{H2}$)?

<details>
<summary><strong>Solution</strong></summary>

Theoretical needed: $30.0 / 0.750 = 40.0\ \text{g}\ \ce{NH3}$. Then map $\ce{NH3} \to \ce{N2}$. $\ce{NH3}$ = 17.03 g/mol → $40.0/17.03 = 2.349\ \text{mol}$. Want $\ce{N2}$ (1) / given $\ce{NH3}$ (2). $\ce{N2}$ = 28.02 g/mol:

$$2.349\ \text{mol}\ \ce{NH3} \times \frac{1\ \ce{N2}}{2\ \ce{NH3}} \times 28.02\ \text{g/mol} = 32.9\ \text{g}\ \ce{N2}$$

**Answer:** theoretical yield = $40.0\ \text{g}\ \ce{NH3}$; requires $32.9\ \text{g}\ \ce{N2}$.

</details>

---

### Problem 15
**Capstone.** $\ce{Fe2O3 + 3CO -> 2Fe + 3CO2}$. A furnace is loaded with 320.0 g $\ce{Fe2O3}$ and 140.0 g $\ce{CO}$, and produces 190.0 g of $\ce{Fe}$. (a) Which reactant is limiting? (b) What is the theoretical yield of iron? (c) What is the percent yield?

<details>
<summary><strong>Solution</strong></summary>

**Moles:** $\ce{Fe2O3}$: $320.0/159.70 = 2.004\ \text{mol}$. $\ce{CO}$: $140.0/28.01 = 4.998\ \text{mol}$.

**(a) Limiting (Method A):** *From $\ce{Fe2O3}$:* $2.004 \times \frac{2}{1} = 4.008\ \text{mol}\ \ce{Fe}$. *From $\ce{CO}$:* $4.998 \times \frac{2}{3} = 3.332\ \text{mol}\ \ce{Fe}$. Smaller → **$\ce{CO}$ is limiting**.

**(b) Theoretical yield:** $3.332\ \text{mol}\ \ce{Fe} \times 55.85\ \text{g/mol} = 186.1\ \text{g}\ \ce{Fe}$.

**(c) Percent yield:** $\dfrac{190.0}{186.1} \times 100\% = 102\%$ — over 100%, which flags a real-world issue: the isolated iron is probably impure (unreacted material or slag weighed with it). On paper the arithmetic is correct; the takeaway is that >100% signals contamination or measurement error, not magic.

**Answer:** (a) $\ce{CO}$ limiting; (b) $186\ \text{g}\ \ce{Fe}$ theoretical; (c) $\approx 102\%$ (physically impossible → impure product).

</details>

---

## Quick Reference

| Concept | Formula / Rule |
|---|---|
| **Mole map (reactions)** | g A $\xrightarrow{\div\text{MM}_A}$ mol A $\xrightarrow{\times\frac{\text{coeff B}}{\text{coeff A}}}$ mol B $\xrightarrow{\times\text{MM}_B}$ g B |
| **Mole ratio** | $\dfrac{\text{coefficient of wanted}}{\text{coefficient of given}}$ (wanted on top) |
| **grams → moles** | $\text{mol} = \dfrac{\text{grams}}{\text{molar mass}}$ |
| **moles → particles** | $\text{particles} = \text{mol} \times 6.022\times10^{23}$ |
| **moles ↔ gas volume** | $PV = nRT$, $R = 0.08206\ \tfrac{\text{L·atm}}{\text{mol·K}}$ |
| **Limiting reactant (A)** | compute product from each reactant; **smallest product wins** |
| **Limiting reactant (B)** | compare have-ratio to recipe-ratio; short one is limiting |
| **Excess remaining** | (started) $-$ (used by limiting reactant) |
| **Theoretical yield** | product computed from the **limiting** reactant |
| **Percent yield** | $\%\ \text{yield} = \dfrac{\text{actual}}{\text{theoretical}} \times 100\%$ |
| **Actual from %** | $\text{actual} = \dfrac{\%}{100}\times\text{theoretical}$ |
| **Theoretical from %** | $\text{theoretical} = \dfrac{\text{actual}}{\%/100}$ |

---

<div align="center">

[← Types of Reactions](/chemistry/0602-types-of-reactions) | [Titration →](/chemistry/0604-titration)

</div>
