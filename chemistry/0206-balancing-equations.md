# Balancing Equations
<p class="article-date">July 4, 2026</p>

*Beach day at Torrey Pines, and I'm on sandwich duty. The recipe is non-negotiable: 2 slices of bread + 1 slice of cheese = 1 sandwich. I open the fridge and find 10 slices of bread and 3 slices of cheese — and no matter how hungry everyone is, I can only build 3 sandwiches, because ingredients don't appear out of nowhere and they don't vanish. They just get recombined. A chemical equation is exactly this: a recipe card. The reactants are the ingredients, the products are the sandwiches, and the coefficients are the recipe ratios — 2 bread : 1 cheese : 1 sandwich. Balancing an equation is just the bookkeeping that Lavoisier's conservation of mass forces on us (remember him from [History of Chemistry](/chemistry/0002-history-of-chemistry)? "matter is neither created nor destroyed" — he proved it with a sealed flask and a very good balance). And here's the one rule that keeps everything honest: you can adjust how many of each ingredient you grab, but you can never change the recipe card mid-build. In chemistry terms — change coefficients freely, never touch subscripts. Master this skill now, because coefficients are secretly mole ratios, and every stoichiometry problem for the rest of the year is built on top of them.*

---

## What You'll Learn
- Read every part of a chemical equation: reactants, products, the arrow, and the state symbols $(s)$, $(l)$, $(g)$, $(aq)$
- Explain the difference between a coefficient and a subscript — and why changing a subscript changes a substance's identity
- State the law of conservation of mass and translate it into "atoms of each element must match on both sides"
- Balance any equation using a reliable algorithm: most complex molecule first, lone elements last, polyatomic ions as units, fractions cleared by doubling
- Handle the combustion pattern ($\ce{C -> H -> O}$ order) including the fraction-clearing trick for odd hydrogen counts
- Treat polyatomic ions like $\ce{NO3^-}$ and $\ce{SO4^2-}$ as single unbreakable units when they appear intact on both sides
- Recognize and classify the five reaction types: synthesis, decomposition, combustion, single replacement, and double replacement
- Verify a balanced equation with a final atom-count check table
- Explain why coefficients are mole ratios — the bridge to stoichiometry

---

## Prerequisites
- [Naming Compounds](/chemistry/0204-naming-compounds) — you can't balance $\ce{Fe2O3}$ if you can't read the formula; names and formulas must be automatic first
- [Polyatomic Ions](/chemistry/0205-polyatomic-ions) — nitrate, sulfate, and friends travel as intact units through most reactions, and treating them that way makes balancing dramatically easier

---

## The Core Concept

### Intuition First

Back to the sandwich station. Here's the recipe written the way a chemist would write it:

$$2\ \text{bread} + 1\ \text{cheese} \longrightarrow 1\ \text{sandwich}$$

Look at what each part is doing:

- **Ingredients on the left** (bread, cheese) = **reactants**
- **Finished sandwich on the right** = **product**
- **The arrow** = "gets transformed into" (assembly happens here)
- **The numbers in front** (2, 1, 1) = **coefficients** — how many of each thing you grab

Now the deep part. Count the bread on each side: 2 slices go in, and the finished sandwich *contains* 2 slices. Count the cheese: 1 in, 1 inside the sandwich. Nothing appeared, nothing vanished — the ingredients just recombined into a new arrangement. That's **conservation of mass**, and it's the entire reason balancing exists. Lavoisier sealed reactions in flasks, weighed everything before and after, and got the same mass every time. Atoms are just rearranged, never created or destroyed.

And the rule I keep repeating at the sandwich station: if the recipe card says 2 slices of bread per sandwich, I can't "fix" a bread shortage by declaring that sandwiches now use 1 slice. That's not the same sandwich anymore — that's an open-face melt, a *different product*. In chemistry, the recipe card is the **subscript**. $\ce{H2O}$ is water; change one subscript and $\ce{H2O2}$ is hydrogen peroxide — the stuff that bleaches hair and stings in cuts. Same elements, different substance. **Balancing only ever changes coefficients (how many you grab), never subscripts (what the thing is).**

One more sandwich fact for later: with 10 bread and 3 cheese, bread is plentiful but cheese runs out after 3 sandwiches. Chemists call that a **limiting reactant**, and we'll do the full math in a couple of articles. For today, just notice that the *ratio* in the recipe is what decides everything — which is exactly why coefficients matter so much.

### Anatomy of a Chemical Equation

Here's a real equation with every part labeled:

$$\ce{CH4(g) + 2O2(g) -> CO2(g) + 2H2O(g)}$$

| Part | In this equation | Meaning |
|---|---|---|
| Reactants | $\ce{CH4}$ and $\ce{O2}$ | Starting substances (left of arrow) |
| Products | $\ce{CO2}$ and $\ce{H2O}$ | Substances formed (right of arrow) |
| Arrow $\ce{->}$ | between them | "reacts to produce" |
| Coefficients | the 2 in $\ce{2O2}$, the 2 in $\ce{2H2O}$ | How many units of each substance (1 is implied when blank) |
| Subscripts | the 4 in $\ce{CH4}$, the 2 in $\ce{H2O}$ | How many atoms *inside* one unit — part of the substance's identity |
| State symbols | $(g)$ | Physical state of each substance |

The four state symbols:

| Symbol | State | Example |
|---|---|---|
| $(s)$ | solid | $\ce{NaCl(s)}$ — a solid crystal, or a precipitate |
| $(l)$ | liquid | $\ce{H2O(l)}$ — pure liquid, not a solution |
| $(g)$ | gas | $\ce{CO2(g)}$ |
| $(aq)$ | aqueous (dissolved in water) | $\ce{NaCl(aq)}$ — salt water |

### Coefficients vs. Subscripts — THE Distinction

This is the single most important idea in this article, so let's hammer it.

| | Coefficient | Subscript |
|---|---|---|
| Where it sits | In front of a whole formula | Inside a formula, after an atom or parenthesis |
| What it means | How many copies of the substance | How many atoms in one copy — the substance's *identity* |
| Can you change it while balancing? | **Yes — this is the only thing you may change** | **Never** |
| Example | $\ce{2H2O}$ = two water molecules | $\ce{H2O2}$ = hydrogen peroxide, a different compound entirely |

A coefficient **multiplies everything in the formula behind it**:

$$\ce{2H2O} \;=\; 2 \times (\text{2 H} + \text{1 O}) \;=\; 4\ \text{H atoms} + 2\ \text{O atoms}$$

$$\ce{3Ba(NO3)2} \;=\; 3\ \text{Ba},\quad 3 \times 2 = 6\ \text{N},\quad 3 \times 2 \times 3 = 18\ \text{O}$$

If you can count atoms in $\ce{3Ba(NO3)2}$ without breaking a sweat, you can balance anything.

### Conservation of Mass, Operationally

The law of conservation of mass sounds philosophical, but for balancing it becomes a blunt checklist:

> **For every element, the number of atoms on the left must equal the number of atoms on the right.**

That's it. An equation is balanced when the atom count of *each element* matches across the arrow. Mass takes care of itself, because atoms carry the mass and no atoms went missing.

### The Balancing Algorithm

You could balance by random trial and error, but here's the algorithm that works fast and never spirals:

**Step 1 — Write correct formulas first, then freeze them.** Get every formula right (this is where [Naming Compounds](/chemistry/0204-naming-compounds) pays off). From this moment on, subscripts are locked.

**Step 2 — Start with the most complex molecule.** The one with the most atoms or the most different elements. Give it a coefficient of 1 (mentally) and let it dictate the others.

**Step 3 — Save lone elements for last.** Pure elements like $\ce{O2}$, $\ce{Fe}$, $\ce{Na}$, $\ce{Cl2}$ have no other element attached — you can change their coefficient without disturbing anything else. They're your free adjustment knobs, so turn them last.

**Step 4 — Treat polyatomic ions as intact units.** If $\ce{SO4^2-}$ or $\ce{NO3^-}$ appears unchanged on both sides, don't count individual S, O, and N atoms — count "sulfates" and "nitrates" like they're single atoms. Huge time-saver.

**Step 5 — If you end up with a fraction, double everything.** A coefficient of $\frac{7}{2}$ is fine mid-work, but final answers need whole numbers: multiply *every* coefficient by 2.

**Step 6 — Final check table.** Count every element on both sides. Every row must match, and the coefficients must be in lowest whole-number form (if they're all divisible by 2, divide).

Memorize the flow: **complex first → lone elements last → polyatomics as units → clear fractions → check table.**

### The Five Reaction Types: A Spotter's Guide

Knowing the pattern tells you what products to expect *before* you balance — and the AP exam loves asking you to predict products.

| Type | Pattern | Recognition cue | Balanced example |
|---|---|---|---|
| **Synthesis** | $\ce{A + B -> AB}$ | Two things become one | $\ce{2Mg(s) + O2(g) -> 2MgO(s)}$ |
| **Decomposition** | $\ce{AB -> A + B}$ | One thing becomes several (often with heat $\Delta$) | $\ce{2KClO3(s) ->[\Delta] 2KCl(s) + 3O2(g)}$ |
| **Combustion** | $\ce{C_xH_y + O2 -> CO2 + H2O}$ | A fuel + oxygen; products are always $\ce{CO2}$ and $\ce{H2O}$ | $\ce{CH4(g) + 2O2(g) -> CO2(g) + 2H2O(g)}$ |
| **Single replacement** | $\ce{A + BC -> AC + B}$ | Lone element + compound → different lone element + compound | $\ce{Zn(s) + 2HCl(aq) -> ZnCl2(aq) + H2(g)}$ |
| **Double replacement** | $\ce{AB + CD -> AD + CB}$ | Two compounds swap partners; often makes a precipitate | $\ce{AgNO3(aq) + NaCl(aq) -> AgCl(s) + NaNO3(aq)}$ |

Sandwich translation: synthesis is assembling a sandwich, decomposition is taking one apart, single replacement is swapping the cheddar for pepper jack, and double replacement is two sandwiches trading fillings.

### Why Balancing Matters: Coefficients Are Mole Ratios

Here's the payoff. The coefficients in

$$\ce{2H2 + O2 -> 2H2O}$$

don't just mean "2 molecules of hydrogen react with 1 molecule of oxygen." Scale it up by any factor and the ratio holds — including scaling up by $6.022 \times 10^{23}$. So the equation *also* reads:

> **2 moles of $\ce{H2}$ react with 1 mole of $\ce{O2}$ to make 2 moles of $\ce{H2O}$.**

Coefficients are **mole ratios** — the recipe scaled to lab-sized amounts. Every "how many grams of product?" problem you'll ever do starts by reading the mole ratio off a balanced equation. That's the entire subject of stoichiometry, and it begins in the next article, [The Mole](/chemistry/0207-the-mole). An unbalanced equation gives wrong ratios, which gives wrong answers to *everything downstream*. That's why AP graders treat balancing as automatic.

---

## Worked Examples

### Example 1: The Classic — Water

**Problem:** Balance $\ce{H2 + O2 -> H2O}$.

**Solution:**

**Step 1:** Count atoms as written: left has 2 H, 2 O; right has 2 H, 1 O. Oxygen is off.

**Step 2:** $\ce{H2O}$ is the most complex molecule. Its subscript locks oxygen in odd steps of 1 per molecule, while $\ce{O2}$ supplies oxygen in 2s. Fix oxygen by taking two waters: $\ce{H2 + O2 -> 2H2O}$. Now right side: 4 H, 2 O.

**Step 3:** $\ce{H2}$ is a lone element — adjust it last and freely: $\ce{2H2 + O2 -> 2H2O}$.

**Step 4:** Check table.

| Element | Left | Right |
|---|---|---|
| H | $2 \times 2 = 4$ | $2 \times 2 = 4$ ✓ |
| O | $2$ | $2 \times 1 = 2$ ✓ |

**Answer:** $\ce{2H2 + O2 -> 2H2O}$

Note what we did *not* do: write $\ce{H2 + O2 -> H2O2}$. That balances the atom count but changes the product from water to hydrogen peroxide — we rewrote the recipe card, which is illegal.

### Example 2: Ammonia Synthesis

**Problem:** Balance $\ce{N2 + H2 -> NH3}$.

**Solution:**

**Step 1:** Most complex molecule: $\ce{NH3}$. Left has 2 N, so we need $\ce{2NH3}$ to match nitrogen: $\ce{N2 + H2 -> 2NH3}$.

**Step 2:** Right side now has $2 \times 3 = 6$ H. $\ce{H2}$ is a lone element — set it to 3: $\ce{N2 + 3H2 -> 2NH3}$.

**Step 3:** Check: N is $2 = 2$ ✓, H is $6 = 6$ ✓.

**Answer:** $\ce{N2 + 3H2 -> 2NH3}$ (a synthesis reaction)

### Example 3: Rust — When Two Elements Fight Over Evenness

**Problem:** Balance $\ce{Fe + O2 -> Fe2O3}$.

**Solution:**

**Step 1:** Most complex: $\ce{Fe2O3}$. It has 3 oxygens (odd), but $\ce{O2}$ delivers oxygen in 2s (even). The fix: find the least common multiple of 3 and 2, which is 6. Take $\ce{2Fe2O3}$ (6 O) and $\ce{3O2}$ (6 O):

$$\ce{Fe + 3O2 -> 2Fe2O3}$$

**Step 2:** Iron is a lone element — save it for last. Right side has $2 \times 2 = 4$ Fe, so:

$$\ce{4Fe + 3O2 -> 2Fe2O3}$$

**Step 3:** Check table.

| Element | Left | Right |
|---|---|---|
| Fe | $4$ | $2 \times 2 = 4$ ✓ |
| O | $3 \times 2 = 6$ | $2 \times 3 = 6$ ✓ |

**Answer:** $\ce{4Fe + 3O2 -> 2Fe2O3}$

The LCM trick (odd subscript meets $\ce{O2}$? think LCM of the oxygen counts) shows up constantly.

### Example 4: Decomposition with Heat

**Problem:** Balance $\ce{KClO3 ->[\Delta] KCl + O2}$.

**Solution:**

**Step 1:** Most complex: $\ce{KClO3}$, with 3 oxygens — odd again, versus $\ce{O2}$'s even 2. LCM of 3 and 2 is 6, so take $\ce{2KClO3}$ and $\ce{3O2}$:

$$\ce{2KClO3 ->[\Delta] KCl + 3O2}$$

**Step 2:** Now match K and Cl: left has 2 of each, so $\ce{2KCl}$.

**Step 3:** Check: K $2=2$ ✓, Cl $2=2$ ✓, O $6 = 6$ ✓.

**Answer:** $\ce{2KClO3 ->[\Delta] 2KCl + 3O2}$ (a decomposition reaction)

### Example 5: The Combustion Pattern — Propane

**Problem:** Balance $\ce{C3H8 + O2 -> CO2 + H2O}$ (propane, the camping-stove fuel).

**Solution:** Combustion has its own sub-algorithm: balance **C, then H, then O** — carbon and hydrogen each appear in only one product, and oxygen is a lone element you save for last.

**Step 1 (C):** 3 carbons on the left → $\ce{3CO2}$.

**Step 2 (H):** 8 hydrogens on the left → $\ce{4H2O}$ (each water carries 2 H).

$$\ce{C3H8 + O2 -> 3CO2 + 4H2O}$$

**Step 3 (O):** Count oxygen on the right: $3 \times 2 + 4 \times 1 = 10$. The lone element $\ce{O2}$ delivers 2 per molecule, so we need 5:

$$\ce{C3H8 + 5O2 -> 3CO2 + 4H2O}$$

**Step 4:** Check table.

| Element | Left | Right |
|---|---|---|
| C | $3$ | $3$ ✓ |
| H | $8$ | $4 \times 2 = 8$ ✓ |
| O | $5 \times 2 = 10$ | $6 + 4 = 10$ ✓ |

**Answer:** $\ce{C3H8 + 5O2 -> 3CO2 + 4H2O}$

### Example 6: Fraction Clearing — Ethane Combustion

**Problem:** Balance $\ce{C2H6 + O2 -> CO2 + H2O}$.

**Solution:**

**Step 1 (C):** 2 carbons → $\ce{2CO2}$.

**Step 2 (H):** 6 hydrogens → $\ce{3H2O}$.

**Step 3 (O):** Right side oxygen: $2 \times 2 + 3 \times 1 = 7$ — an **odd** number, but $\ce{O2}$ only comes in 2s. Mid-work, a fraction is legal:

$$\ce{C2H6 + \tfrac{7}{2}O2 -> 2CO2 + 3H2O}$$

**Step 4 (clear the fraction):** Multiply *every* coefficient by 2:

$$\ce{2C2H6 + 7O2 -> 4CO2 + 6H2O}$$

**Step 5:** Check: C $4 = 4$ ✓, H $12 = 12$ ✓, O $14 = 8 + 6$ ✓.

**Answer:** $\ce{2C2H6 + 7O2 -> 4CO2 + 6H2O}$

Rule of thumb: any hydrocarbon $\ce{C_xH_y}$ with an even carbon count and $y$ giving an odd oxygen total will need the doubling trick. It feels like cheating; it's just algebra.

### Example 7: Polyatomic Ions as Intact Units

**Problem:** Balance $\ce{Ba(NO3)2 + Na2SO4 -> BaSO4 + NaNO3}$.

**Solution:** Both $\ce{NO3^-}$ and $\ce{SO4^2-}$ appear unchanged on both sides — so don't count N, S, and O separately. Count **nitrates** and **sulfates** as units.

**Step 1:** Inventory as written:

| Unit | Left | Right |
|---|---|---|
| Ba | 1 | 1 ✓ |
| $\ce{NO3}$ | 2 | 1 ✗ |
| Na | 2 | 1 ✗ |
| $\ce{SO4}$ | 1 | 1 ✓ |

**Step 2:** One coefficient fixes both problems: $\ce{2NaNO3}$ gives 2 Na and 2 $\ce{NO3}$.

**Step 3:** Re-check: Ba $1=1$, $\ce{NO3}$ $2=2$, Na $2=2$, $\ce{SO4}$ $1=1$. All ✓.

**Answer:** $\ce{Ba(NO3)2 + Na2SO4 -> BaSO4 + 2NaNO3}$ (a double replacement — barium sulfate is the precipitate)

Counting 4 units instead of 5 elements (with oxygen scattered across three compounds!) turned a mess into a 30-second problem.

### Example 8: Single Replacement with a Polyatomic Twist

**Problem:** Balance $\ce{Al + CuSO4 -> Al2(SO4)3 + Cu}$.

**Solution:**

**Step 1:** Most complex: $\ce{Al2(SO4)3}$ — it demands 2 Al and 3 sulfate units per formula. Treat $\ce{SO4}$ as a unit.

**Step 2:** Sulfate: right needs 3, left has 1 per $\ce{CuSO4}$ → coefficient 3:

$$\ce{Al + 3CuSO4 -> Al2(SO4)3 + Cu}$$

**Step 3:** Lone elements last. Al: right has 2 → $\ce{2Al}$. Cu: left has 3 → $\ce{3Cu}$:

$$\ce{2Al + 3CuSO4 -> Al2(SO4)3 + 3Cu}$$

**Step 4:** Check: Al $2=2$ ✓, Cu $3=3$ ✓, $\ce{SO4}$ $3=3$ ✓.

**Answer:** $\ce{2Al + 3CuSO4 -> Al2(SO4)3 + 3Cu}$ (single replacement — aluminum kicks copper out)

### Example 9: Double Replacement, Both Sides Loaded

**Problem:** Balance $\ce{Al2(SO4)3 + Ca(OH)2 -> Al(OH)3 + CaSO4}$.

**Solution:** Two polyatomic units to track — $\ce{SO4^2-}$ and $\ce{OH^-}$ — plus Al and Ca. Four "elements" total.

**Step 1:** Most complex: $\ce{Al2(SO4)3}$. Set it to 1 and let it dictate: we need 2 Al and 3 $\ce{SO4}$ on the right.

**Step 2:** Al → $\ce{2Al(OH)3}$. Sulfate → $\ce{3CaSO4}$:

$$\ce{Al2(SO4)3 + Ca(OH)2 -> 2Al(OH)3 + 3CaSO4}$$

**Step 3:** Now sweep back to the left. Ca: right has 3 → $\ce{3Ca(OH)2}$. That brings $3 \times 2 = 6$ hydroxides, and the right has $2 \times 3 = 6$. Everything clicks:

$$\ce{Al2(SO4)3 + 3Ca(OH)2 -> 2Al(OH)3 + 3CaSO4}$$

**Step 4:** Check table.

| Unit | Left | Right |
|---|---|---|
| Al | $2$ | $2$ ✓ |
| $\ce{SO4}$ | $3$ | $3$ ✓ |
| Ca | $3$ | $3$ ✓ |
| $\ce{OH}$ | $3 \times 2 = 6$ | $2 \times 3 = 6$ ✓ |

**Answer:** $\ce{Al2(SO4)3 + 3Ca(OH)2 -> 2Al(OH)3 + 3CaSO4}$

### Example 10: The Nasty One — Roasting Pyrite

**Problem:** Balance $\ce{FeS2 + O2 -> Fe2O3 + SO2}$ (fool's gold burning in a smelter).

**Solution:** No polyatomic shortcuts here — oxygen appears in two products, and both Fe and S live in the same reactant. This is the full algorithm under stress.

**Step 1:** Most complex is a tie; start from $\ce{Fe2O3}$ since it forces evenness. It needs 2 Fe, so $\ce{2FeS2}$:

$$\ce{2FeS2 + O2 -> Fe2O3 + SO2}$$

**Step 2:** Sulfur: left now has $2 \times 2 = 4$ → $\ce{4SO2}$:

$$\ce{2FeS2 + O2 -> Fe2O3 + 4SO2}$$

**Step 3:** Oxygen last (lone element). Right side: $3 + 4 \times 2 = 11$ — odd. Allow the fraction:

$$\ce{2FeS2 + \tfrac{11}{2}O2 -> Fe2O3 + 4SO2}$$

**Step 4:** Double everything:

$$\ce{4FeS2 + 11O2 -> 2Fe2O3 + 8SO2}$$

**Step 5:** Check table.

| Element | Left | Right |
|---|---|---|
| Fe | $4$ | $2 \times 2 = 4$ ✓ |
| S | $4 \times 2 = 8$ | $8$ ✓ |
| O | $11 \times 2 = 22$ | $2 \times 3 + 8 \times 2 = 22$ ✓ |

**Answer:** $\ce{4FeS2 + 11O2 -> 2Fe2O3 + 8SO2}$

If you stayed calm through the $\frac{11}{2}$, you can balance anything AP Chemistry throws at you.

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Changing a subscript to balance (e.g., $\ce{H2O -> H2O2}$) | It "fixes" the atom count with one keystroke | Subscripts are the recipe card — locked. Say it out loud: **coefficients only.** $\ce{H2O2}$ is a different substance |
| Forgetting a coefficient multiplies *everything* | Reading $\ce{2Ba(NO3)2}$ as 2 Ba but only 2 O | Distribute fully: $\ce{2Ba(NO3)2}$ = 2 Ba, 4 N, **12** O |
| Balancing O or H first in a combustion | They look like the biggest problem | Follow C → H → O; oxygen is a lone element, always last |
| Leaving a fraction in the final answer | $\frac{7}{2}$ genuinely balances | Fractions are scratch work; double every coefficient before boxing the answer |
| Not reducing to lowest whole numbers | $\ce{4H2 + 2O2 -> 4H2O}$ *is* balanced | Final scan: if all coefficients share a factor, divide it out. AP wants $\ce{2H2 + O2 -> 2H2O}$ |
| Breaking polyatomic ions apart unnecessarily | Habit of counting every element | If the ion is intact on both sides, count it as one unit — fewer rows in your check table, fewer mistakes |
| Forgetting the diatomic elements | Writing "$\ce{O}$" or "$\ce{H}$" as a reactant | The seven diatomics — $\ce{H2, N2, O2, F2, Cl2, Br2, I2}$ — never appear alone as single atoms in equations |
| Skipping the final check table | Confidence | Two columns, thirty seconds. Every element (or unit), both sides. Non-negotiable |

---

## AP Exam Tips

- **Lowest whole-number coefficients are the expected form.** On FRQs, $\ce{4H2 + 2O2 -> 4H2O}$ can cost you the point even though the atoms balance. Reduce.
- **Balancing is assumed automatic by exam day.** The AP exam almost never asks "balance this equation" as a standalone question — instead, an *unbalanced* or partially-given equation is embedded inside a stoichiometry, thermochemistry, or electrochemistry problem, and a wrong balance silently poisons every later part. Treat balancing like arithmetic: fast, silent, correct.
- **Net ionic equations (Unit 4) are built directly on this skill.** You'll balance the full molecular equation first, then split aqueous species into ions and cancel spectators. If Example 7 felt comfortable, you're already halfway to net ionics.
- **Reaction-type recognition earns prediction points.** FRQs say things like "solid magnesium is burned in air — write the balanced equation." You must recognize *synthesis*, recall $\ce{O2}$ is diatomic, and produce $\ce{2Mg + O2 -> 2MgO}$ from scratch.
- **Coefficients are mole ratios, never mass ratios.** A favorite multiple-choice trap: $\ce{2H2 + O2}$ does **not** mean 2 grams of hydrogen per 1 gram of oxygen. Moles, always.
- **State symbols matter on FRQs** when the question hinges on them (precipitates $(s)$, gases escaping $(g)$). Writing $\ce{AgCl(aq)}$ for a precipitate can cost the point.
- **No calculator needed, no calculator allowed** for the multiple-choice section where these appear — balancing is pure counting, which is exactly why it has to be automatic.

---

## Practice Problems

### Problem 1
Balance: $\ce{Na + Cl2 -> NaCl}$

<details>
<summary><strong>Solution</strong></summary>

$\ce{Cl2}$ delivers chlorine in 2s, so take $\ce{2NaCl}$; then match sodium with $\ce{2Na}$.

Check: Na $2 = 2$ ✓, Cl $2 = 2$ ✓.

**Answer:** $\ce{2Na + Cl2 -> 2NaCl}$ (synthesis)

</details>

### Problem 2
Balance: $\ce{Mg + O2 -> MgO}$

<details>
<summary><strong>Solution</strong></summary>

Oxygen: left has 2, right has 1 → $\ce{2MgO}$. Then magnesium: $\ce{2Mg}$.

Check: Mg $2 = 2$ ✓, O $2 = 2$ ✓.

**Answer:** $\ce{2Mg + O2 -> 2MgO}$ (synthesis)

</details>

### Problem 3
Balance: $\ce{P4 + O2 -> P2O5}$

<details>
<summary><strong>Solution</strong></summary>

Phosphorus: left has 4, each product carries 2 → $\ce{2P2O5}$.

Oxygen: right now has $2 \times 5 = 10$ → $\ce{5O2}$.

Check: P $4 = 4$ ✓, O $10 = 10$ ✓.

**Answer:** $\ce{P4 + 5O2 -> 2P2O5}$ (synthesis)

</details>

### Problem 4
Balance the combustion of methane: $\ce{CH4 + O2 -> CO2 + H2O}$

<details>
<summary><strong>Solution</strong></summary>

C → H → O order.

C: $1 = 1$ already. H: 4 on the left → $\ce{2H2O}$. O: right has $2 + 2 = 4$ → $\ce{2O2}$.

Check: C $1=1$ ✓, H $4=4$ ✓, O $4=4$ ✓.

**Answer:** $\ce{CH4 + 2O2 -> CO2 + 2H2O}$ (combustion)

</details>

### Problem 5
Balance the combustion of butane (lighter fluid): $\ce{C4H10 + O2 -> CO2 + H2O}$

<details>
<summary><strong>Solution</strong></summary>

C: 4 → $\ce{4CO2}$. H: 10 → $\ce{5H2O}$.

O on the right: $8 + 5 = 13$, odd → $\ce{\tfrac{13}{2}O2}$, then double everything:

$$\ce{2C4H10 + 13O2 -> 8CO2 + 10H2O}$$

Check: C $8 = 8$ ✓, H $20 = 20$ ✓, O $26 = 16 + 10$ ✓.

**Answer:** $\ce{2C4H10 + 13O2 -> 8CO2 + 10H2O}$ (combustion, fraction-clearing)

</details>

### Problem 6
Balance: $\ce{Zn + HCl -> ZnCl2 + H2}$

<details>
<summary><strong>Solution</strong></summary>

$\ce{ZnCl2}$ needs 2 Cl, and $\ce{H2}$ needs 2 H — one coefficient serves both: $\ce{2HCl}$.

Check: Zn $1=1$ ✓, H $2=2$ ✓, Cl $2=2$ ✓.

**Answer:** $\ce{Zn + 2HCl -> ZnCl2 + H2}$ (single replacement — zinc displaces hydrogen)

</details>

### Problem 7
Balance: $\ce{AgNO3 + CaCl2 -> AgCl + Ca(NO3)2}$

<details>
<summary><strong>Solution</strong></summary>

Treat $\ce{NO3}$ as a unit. Right side needs 2 nitrates → $\ce{2AgNO3}$. That brings 2 Ag → $\ce{2AgCl}$, which also matches the 2 Cl from $\ce{CaCl2}$.

Check: Ag $2=2$ ✓, $\ce{NO3}$ $2=2$ ✓, Ca $1=1$ ✓, Cl $2=2$ ✓.

**Answer:** $\ce{2AgNO3 + CaCl2 -> 2AgCl + Ca(NO3)2}$ (double replacement)

</details>

### Problem 8
Balance: $\ce{Pb(NO3)2 + KI -> PbI2 + KNO3}$

<details>
<summary><strong>Solution</strong></summary>

Nitrate as a unit: left has 2 → $\ce{2KNO3}$. Potassium: right now has 2 → $\ce{2KI}$, which also supplies the 2 iodines that $\ce{PbI2}$ needs.

Check: Pb $1=1$ ✓, $\ce{NO3}$ $2=2$ ✓, K $2=2$ ✓, I $2=2$ ✓.

**Answer:** $\ce{Pb(NO3)2 + 2KI -> PbI2 + 2KNO3}$ (double replacement — the golden precipitate demo)

</details>

### Problem 9
Balance: $\ce{NH3 + O2 -> NO + H2O}$

<details>
<summary><strong>Solution</strong></summary>

No polyatomic shortcut — oxygen is in both products. Start with H: LCM of 3 (in $\ce{NH3}$) and 2 (in $\ce{H2O}$) is 6 → $\ce{2NH3}$ and $\ce{3H2O}$. Nitrogen follows: $\ce{2NO}$.

Oxygen on the right: $2 + 3 = 5$, odd → $\ce{\tfrac{5}{2}O2}$, then double:

$$\ce{4NH3 + 5O2 -> 4NO + 6H2O}$$

Check: N $4=4$ ✓, H $12=12$ ✓, O $10 = 4 + 6$ ✓.

**Answer:** $\ce{4NH3 + 5O2 -> 4NO + 6H2O}$

</details>

### Problem 10
Balance: $\ce{Fe2O3 + CO -> Fe + CO2}$ (iron smelting in a blast furnace)

<details>
<summary><strong>Solution</strong></summary>

Iron: $\ce{Fe2O3}$ has 2 → $\ce{2Fe}$. Now oxygen: left has $3 + 1x$ (from $x\,\ce{CO}$), right has $2x$ (from $x\,\ce{CO2}$, since carbon forces the $\ce{CO}$ and $\ce{CO2}$ coefficients to match). Solve $3 + x = 2x$ → $x = 3$.

Check: Fe $2=2$ ✓, C $3=3$ ✓, O $3 + 3 = 6$, right $3 \times 2 = 6$ ✓.

**Answer:** $\ce{Fe2O3 + 3CO -> 2Fe + 3CO2}$

</details>

### Problem 11
Balance the decomposition: $\ce{(NH4)2CO3 ->[\Delta] NH3 + H2O + CO2}$

<details>
<summary><strong>Solution</strong></summary>

Nitrogen: left has 2 → $\ce{2NH3}$.

Hydrogen check: left has $2 \times 4 = 8$; right has $2 \times 3 + 2 = 8$ ✓ already.

Carbon $1=1$ ✓, Oxygen $3 = 1 + 2$ ✓.

**Answer:** $\ce{(NH4)2CO3 ->[\Delta] 2NH3 + H2O + CO2}$ (decomposition)

</details>

### Problem 12
Balance the thermite reaction: $\ce{Al + Fe2O3 -> Al2O3 + Fe}$

<details>
<summary><strong>Solution</strong></summary>

Both metals are lone elements — the oxides set the ratio. Oxygen already matches ($3 = 3$). Aluminum: right has 2 → $\ce{2Al}$. Iron: left has 2 → $\ce{2Fe}$.

Check: Al $2=2$ ✓, Fe $2=2$ ✓, O $3=3$ ✓.

**Answer:** $\ce{2Al + Fe2O3 -> Al2O3 + 2Fe}$ (single replacement — hot enough to weld railroad track)

</details>

### Problem 13
Balance the combustion of glucose (this is respiration — you are running this reaction right now): $\ce{C6H12O6 + O2 -> CO2 + H2O}$

<details>
<summary><strong>Solution</strong></summary>

C: 6 → $\ce{6CO2}$. H: 12 → $\ce{6H2O}$.

O on the right: $12 + 6 = 18$. The left already has 6 O inside glucose, so $\ce{O2}$ must supply $18 - 6 = 12$ → $\ce{6O2}$. (Watch for oxygen hiding *inside* the fuel!)

Check: C $6=6$ ✓, H $12=12$ ✓, O $6 + 12 = 18$, right $12 + 6 = 18$ ✓.

**Answer:** $\ce{C6H12O6 + 6O2 -> 6CO2 + 6H2O}$

</details>

### Problem 14
Balance and classify: $\ce{Ca + H2O -> Ca(OH)2 + H2}$

<details>
<summary><strong>Solution</strong></summary>

Hydroxide can't be treated as a unit here ($\ce{H2O}$ isn't hydroxide), so count elements. $\ce{Ca(OH)2}$ needs 2 O → $\ce{2H2O}$.

Hydrogen check: left $2 \times 2 = 4$; right $2 + 2 = 4$ ✓.

Check: Ca $1=1$ ✓, O $2=2$ ✓, H $4=4$ ✓.

**Answer:** $\ce{Ca + 2H2O -> Ca(OH)2 + H2}$ — single replacement (calcium displaces hydrogen from water)

</details>

### Problem 15
A classmate balances $\ce{H2 + O2 -> H2O}$ by changing the product to $\ce{H2O2}$ and declares victory: "$\ce{H2 + O2 -> H2O2}$ — every atom matches!" Explain, using the coefficient/subscript distinction, why this is wrong even though the atoms count out.

<details>
<summary><strong>Solution</strong></summary>

The atom bookkeeping does work: 2 H and 2 O on each side. But balancing must describe the *actual reaction* — hydrogen burning in oxygen produces **water**, $\ce{H2O}$. By changing the subscript, the classmate changed the recipe card itself: $\ce{H2O2}$ is hydrogen peroxide, a completely different compound with different properties (it's a reactive bleaching agent, not the stuff you drink). The equation they wrote is a perfectly balanced equation *for a different reaction that isn't happening*.

The legal fix adjusts only coefficients — how many of each fixed substance participates:

$$\ce{2H2 + O2 -> 2H2O}$$

**Answer:** Subscripts define a substance's identity and are fixed by the actual chemistry; only coefficients (the counts of each substance) may be adjusted. **$\ce{2H2 + O2 -> 2H2O}$** is the balanced equation for the real reaction.

</details>

---

## Quick Reference

**The algorithm:**

| Step | Action |
|---|---|
| 1 | Write correct formulas, then lock all subscripts |
| 2 | Balance the most complex molecule first |
| 3 | Save lone elements ($\ce{O2}$, metals) for last |
| 4 | Count intact polyatomic ions ($\ce{NO3^-}$, $\ce{SO4^2-}$, $\ce{OH^-}$) as single units |
| 5 | Clear fractions by multiplying every coefficient (usually by 2) |
| 6 | Final check table; reduce to lowest whole numbers |

**Combustion sub-rule:** balance $\ce{C -> H -> O}$, in that order.

**The seven diatomic elements:** $\ce{H2, N2, O2, F2, Cl2, Br2, I2}$

**Coefficient vs. subscript:** coefficient = how many copies (changeable); subscript = what the substance *is* (untouchable). $\ce{2H2O} \ne \ce{H2O2}$.

**The five reaction types:**

| Type | Skeleton |
|---|---|
| Synthesis | $\ce{A + B -> AB}$ |
| Decomposition | $\ce{AB -> A + B}$ |
| Combustion | $\ce{fuel + O2 -> CO2 + H2O}$ |
| Single replacement | $\ce{A + BC -> AC + B}$ |
| Double replacement | $\ce{AB + CD -> AD + CB}$ |

**The payoff:** coefficients are **mole ratios** — the recipe that all of stoichiometry reads from.

---

<div align="center">

[← Polyatomic Ions](/chemistry/0205-polyatomic-ions) | [The Mole →](/chemistry/0207-the-mole)

</div>
