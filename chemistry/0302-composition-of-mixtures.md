# Composition of Mixtures
<p class="article-date">July 4, 2026</p>

*Beach day at Torrey Pines yesterday, and here's the thing I noticed hauling my bag back to the car: my swimsuit weighed WAY more than it did when I pulled it out of the drawer that morning. Soaked through, it's heavy — full of water I can't see as separate droplets, just... in there, held in the fabric. So I hung it on the line in the backyard, and by dinner it was back to its normal featherweight self. Now here's the move that turns that into science: weigh the suit before the beach, weigh it after it dries, subtract. You know *exactly* how much water it was holding — without ever watching a single drop leave. That subtraction trick is the heart of one of the most famous labs in AP Chemistry: some crystals lock water molecules right into their structure in a fixed ratio (blue $\ce{CuSO4 * 5H2O}$ is the celebrity example), gentle heating drives the water off, and the before-minus-after mass difference tells you the formula. This article covers AP Unit 1, Topics 1.3 and 1.4 — how composition tells pure substances and mixtures apart, and how a balance plus subtraction can reveal what a sample is made of.*

---

## What You'll Learn

- Distinguish pure substances (fixed composition) from mixtures (variable composition) using the law of definite proportions
- Classify mixtures as homogeneous or heterogeneous, with everyday examples
- Use percent composition as a *fingerprint* to test whether two samples are the same compound
- Explain what a hydrate is, decode the $\ce{\cdot nH2O}$ dot notation, and name hydrates with Greek prefixes
- Perform the core hydrate lab calculation: mass before and after heating $\rightarrow$ moles of water and anhydrous salt $\rightarrow$ the whole-number ratio $n$
- Run the calculation in reverse: predict the percent mass loss when a known hydrate is heated
- Calculate the mass percent of a component in a mixture, and track masses through a dissolve–filter–evaporate separation
- Use light algebra to split a two-compound mixture when you know the total mass of one element
- Analyze hydrate-lab errors (stopping heating early, splattering) and predict whether each pushes $n$ too high or too low

---

## Prerequisites

- [The Mole](/chemistry/0207-the-mole) — percent composition, molar masses of hydrates, and empirical formulas all come from there; this article puts them to work
- [Dimensional Analysis](/chemistry/0103-dimensional-analysis) — every gram-to-mole conversion here is a unit-fraction chain

---

## The Core Concept

### Intuition First

Back to the swimsuit on the drying line. Map its parts onto the chemistry, because the mapping is exact:

| Beach laundry | Hydrate lab |
|---|---|
| dry swimsuit from the drawer | **anhydrous salt** ($\ce{CuSO4}$, bone-dry) |
| soaked swimsuit after the beach | **hydrate** ($\ce{CuSO4 * 5H2O}$, water locked inside) |
| the drying line in the sun | the **crucible over a burner** (heat drives water off as vapor) |
| weigh before − weigh after | **mass of water** the sample was holding |
| "it stopped getting lighter, it's dry" | heating to **constant mass** |

There's one huge difference, though, and it's the whole point of Topic 1.3. A swimsuit holds however much water happens to soak in — a quick dip versus an hour of bodysurfing gives different soak levels. **Variable composition.** A hydrate is pickier: the water molecules aren't soaked into the crystal randomly, they're *built into the crystal structure* at exact positions. Copper(II) sulfate pentahydrate is always exactly 5 water molecules per $\ce{CuSO4}$ — not 4.7, not 5.2, not "depends on the day." **Fixed composition.** That's what makes it a pure substance with a formula, and it's why the before-and-after weighing doesn't just tell you *how much* water was there — it tells you the *formula*.

And for the variable-composition side, meet my other beach-bag item: trail mix. Every handful is different. Dad's bag from Costco is heavy on peanuts; the fancy one from the co-op is mostly almonds and (tragically) raisins. Both are legitimately "trail mix." Nobody can write a chemical formula for trail mix, because there's no fixed ratio to write down. Compare that to water: every single water molecule that has ever existed — in the Pacific, in a glacier, in my water bottle — is exactly 2 hydrogen atoms to 1 oxygen atom. Trail mix is a mixture. Water is a compound. Composition is the dividing line.

### Pure Substances vs. Mixtures

A **pure substance** (an element or a compound) has a **fixed, definite composition**. This is the **law of definite proportions**: a given compound always contains the same elements in the same proportions by mass, no matter where the sample came from or how it was made.

$$\text{Water, always: } \%\ce{H} = \frac{2(1.008)}{18.02} \times 100\% = 11.19\%, \qquad \%\ce{O} = 88.81\%$$

A **mixture** is a physical blend of two or more substances, each keeping its own identity, in **variable proportions**. You can make trail mix with 30% peanuts or 60% peanuts and both are trail mix; you cannot make water with 15% hydrogen.

| | Trail mix (mixture) | Water (compound) |
|---|---|---|
| Composition | Variable — bag to bag, handful to handful | Fixed — always 2 H : 1 O |
| Has a formula? | No | Yes: $\ce{H2O}$ |
| Components keep their identity? | Yes (a peanut is still a peanut) | No ($\ce{H2}$ and $\ce{O2}$ gases are gone; water is a new substance) |
| Separable by physical means? | Yes (pick out the raisins) | No — requires a chemical change |

### Homogeneous vs. Heterogeneous (Quick and Painless)

Mixtures come in two textures:

- **Homogeneous** — uniform throughout; every sample of it has the same composition as every other sample *from that batch*. Salt water, sweet tea, air, brass. Also called **solutions**.
- **Heterogeneous** — visibly (or microscopically) non-uniform; different scoops differ. Trail mix, orange juice with pulp, salad, sand-and-salt.

The AP-level catch: homogeneous does **not** mean pure. A pitcher of lemonade is perfectly uniform, but *this* pitcher might be 8% sugar and the next one 12%. Uniform within the batch, variable between batches — still a mixture.

### Percent Composition Is a Fingerprint

From [The Mole](/chemistry/0207-the-mole), percent composition of a compound:

$$\%\text{ element} = \frac{(\text{atoms of element in formula}) \times (\text{atomic mass})}{\text{molar mass of compound}} \times 100\%$$

Because a compound's composition is fixed, its percent composition is a **fingerprint**. Every sample of $\ce{NaCl}$ on Earth is 39.34% Na and 60.66% Cl. So if a lab hands you two white powders and their measured percent compositions *differ*, they cannot be the same pure substance. If the percents *match*, the samples have the same empirical formula — a strong clue they're the same compound (with one subtlety we'll hit in Example 2 and Common Mistakes: matching percents guarantee the same *empirical* formula, not necessarily the same *molecular* formula).

### Hydrates: Crystals That Pack Water

A **hydrate** is an ionic compound with a fixed number of water molecules locked into its crystal lattice. The formula uses a **dot**:

$$\ce{CuSO4 * 5H2O}$$

Read it as "$\ce{CuSO4}$ *plus* 5 waters per formula unit." The dot means **and**, not "times" — the molar mass is a **sum**:

$$M(\ce{CuSO4 * 5H2O}) = 159.62 + 5(18.02) = 249.72 \ \text{g/mol}$$

Strip the water out (by heating) and what's left is the **anhydrous** salt — "anhydrous" literally means *without water*. The water that leaves is called the **water of hydration**.

**Naming:** name the salt, then a Greek prefix + "hydrate" for $n$:

| $n$ | Prefix | Example |
|---|---|---|
| 1 | mono- | — |
| 2 | di- | $\ce{CaCl2 * 2H2O}$ — calcium chloride dihydrate |
| 3 | tri- | — |
| 4 | tetra- | — |
| 5 | penta- | $\ce{CuSO4 * 5H2O}$ — copper(II) sulfate pentahydrate |
| 6 | hexa- | $\ce{CoCl2 * 6H2O}$ — cobalt(II) chloride hexahydrate |
| 7 | hepta- | $\ce{MgSO4 * 7H2O}$ — magnesium sulfate heptahydrate (Epsom salt) |
| 10 | deca- | $\ce{Na2CO3 * 10H2O}$ — sodium carbonate decahydrate (washing soda) |

These aren't lab curiosities — Epsom salt is in the medicine cabinet, washing soda is in the laundry room, and $\ce{CaCl2}$ hydrates are the "DampRid" moisture absorbers in closets.

### The Hydrate Lab: Weigh, Heat, Weigh, Subtract

This is the swimsuit move, formalized. The classic AP lab: you're given a hydrate of known salt but unknown $n$, written $\ce{Salt * nH2O}$, and asked to find $n$.

$$\ce{Salt * nH2O ->[\Delta] Salt + nH2O ^}$$

**The four-step recipe:**

1. **Mass of water** = (mass of hydrate before heating) − (mass of anhydrous salt after heating). *Before minus after.*
2. **Moles of water** = mass of water ÷ 18.02 g/mol.
3. **Moles of anhydrous salt** = mass after heating ÷ molar mass of the *anhydrous* salt.
4. **$n$** = moles of water ÷ moles of anhydrous salt, rounded to the nearest sensible whole number.

$$n = \frac{\text{mol } \ce{H2O}}{\text{mol anhydrous salt}}$$

**How do you know the suit is dry?** In the lab you can't see the water leave, so you heat, cool, weigh — then heat *again*, cool, weigh. When two consecutive weighings agree, you've reached **constant mass**: all the water is gone. Stop early and leftover water hides in the solid, corrupting both subtraction and formula (we'll quantify exactly how in AP Exam Tips).

### Mixtures by Mass

Since a mixture has no formula, we describe it with **mass percent of each component**:

$$\%\text{ component} = \frac{\text{mass of component}}{\text{total mass of mixture}} \times 100\%$$

Same-shaped formula as percent composition — but the meaning flips. A compound's percents are *fixed by nature*; a mixture's percents are *whatever you blended*, so they must be **measured for each sample**.

To measure them, chemists separate the mixture using differences in physical properties. The classic: **salt and sand**.

1. **Dissolve** — add water; salt dissolves, sand doesn't.
2. **Filter** — sand stays on the filter paper; salt water passes through.
3. **Evaporate** — boil off the water; salt crystals remain.

Weigh the recovered sand and salt, divide each by the *original* mixture mass, and you've got the composition. No chemical reactions anywhere — the salt and sand never stopped being salt and sand. That's the signature of a mixture.

One more tool for the kit: sometimes you can't physically separate a mixture, but you know its total mass and the total mass of one *element* inside it. Then a little algebra splits the mixture on paper — let $x$ be the grams of one component, write the element's mass as a sum of contributions, and solve. Example 9 does this with fertilizer.

---

## Worked Examples

### Example 1: Percent Composition as a Fingerprint

**Problem:** Calculate the percent composition of calcium carbonate, $\ce{CaCO3}$ (the compound in seashells and chalk).

**Solution:**

**Step 1 — Molar mass.**
$$M = 40.08 + 12.01 + 3(16.00) = 100.09 \ \text{g/mol}$$

**Step 2 — Each element's share.**
$$\%\ce{Ca} = \frac{40.08}{100.09} \times 100\% = 40.04\% \qquad \%\ce{C} = \frac{12.01}{100.09} \times 100\% = 12.00\%$$
$$\%\ce{O} = \frac{48.00}{100.09} \times 100\% = 47.96\%$$

**Step 3 — Sanity check.** $40.04 + 12.00 + 47.96 = 100.00\%$. ✓

**Answer: $\ce{CaCO3}$ is 40.04% Ca, 12.00% C, 47.96% O — for every sample, everywhere, always.**

### Example 2: Two White Powders — Same Substance?

**Problem:** Two unlabeled white powders are analyzed. Powder A: 39.3% Na, 60.7% Cl. Powder B: 43.7% Na, 56.3% Cl. Could either one be pure sodium chloride? Could they be the same substance?

**Solution:**

**Step 1 — Compute the fingerprint for $\ce{NaCl}$.** $M = 22.99 + 35.45 = 58.44$ g/mol.
$$\%\ce{Na} = \frac{22.99}{58.44} \times 100\% = 39.34\% \qquad \%\ce{Cl} = \frac{35.45}{58.44} \times 100\% = 60.66\%$$

**Step 2 — Compare.** Powder A (39.3%, 60.7%) matches within measurement error — consistent with pure $\ce{NaCl}$. Powder B (43.7%, 56.3%) does **not** match. By the law of definite proportions, B cannot be pure $\ce{NaCl}$.

**Step 3 — What could B be?** Something with a genuinely different formula, or a *mixture* (e.g., $\ce{NaCl}$ contaminated with a second sodium compound, dragging the %Na up). Percents alone can't say which — but they *can* say B ≠ A.

**Answer: A is consistent with pure $\ce{NaCl}$; B is definitely not pure $\ce{NaCl}$, so A and B are different materials.** (Fine print: matching percents prove matching *empirical* formulas. Glucose $\ce{C6H12O6}$ and formaldehyde $\ce{CH2O}$ have identical percent compositions — to tell them apart you'd also need a molar mass, e.g., from mass spectrometry.)

### Example 3: Mass Percent in a Mixture (Trail Mix)

**Problem:** A bag of trail mix contains 62.0 g peanuts, 41.0 g raisins, and 22.0 g chocolate pieces. What is the mass percent of peanuts?

**Solution:**

**Step 1 — Total mass.** $62.0 + 41.0 + 22.0 = 125.0$ g.

**Step 2 — Peanut share.**
$$\%\text{ peanuts} = \frac{62.0 \ \text{g}}{125.0 \ \text{g}} \times 100\% = 49.6\%$$

**Answer: 49.6% peanuts by mass** — *for this bag*. A different bag can be 30% or 70% peanuts and still be trail mix. That's variable composition; contrast Example 1, where $\ce{CaCO3}$ had no choice about its 40.04% Ca.

### Example 4: The Hydrate Lab — Blue Crystals

**Problem:** A 2.50 g sample of hydrated copper(II) sulfate, $\ce{CuSO4 * nH2O}$, is heated to constant mass. The white anhydrous solid that remains weighs 1.60 g. Find $n$ and write the formula.

**Solution:**

**Step 1 — Mass of water (before minus after).**
$$2.50 \ \text{g} - 1.60 \ \text{g} = 0.90 \ \text{g } \ce{H2O}$$

**Step 2 — Moles of each part.**
$$\text{mol } \ce{H2O} = \frac{0.90}{18.02} = 0.0499 \ \text{mol} \qquad \text{mol } \ce{CuSO4} = \frac{1.60}{159.62} = 0.0100 \ \text{mol}$$

(Note the anhydrous molar mass, 159.62 g/mol — the 1.60 g remaining is dry $\ce{CuSO4}$, the swimsuit back from the line.)

**Step 3 — Ratio.**
$$n = \frac{0.0499}{0.0100} = 4.98 \approx 5$$

**Answer: $n = 5$; the hydrate is $\ce{CuSO4 * 5H2O}$, copper(II) sulfate pentahydrate.** (Bonus lab detail: the color flips from brilliant blue to chalky white as the water leaves — the blue literally belongs to the water-bound copper.)

### Example 5: Epsom Salt

**Problem:** A 4.93 g sample of Epsom salt, $\ce{MgSO4 * nH2O}$, is heated to constant mass, leaving 2.41 g of anhydrous $\ce{MgSO4}$. Find $n$.

**Solution:**

**Step 1 — Water mass.** $4.93 - 2.41 = 2.52$ g $\ce{H2O}$.

**Step 2 — Moles.** $M(\ce{MgSO4}) = 24.31 + 32.07 + 4(16.00) = 120.38$ g/mol.
$$\text{mol } \ce{H2O} = \frac{2.52}{18.02} = 0.1398 \ \text{mol} \qquad \text{mol } \ce{MgSO4} = \frac{2.41}{120.38} = 0.0200 \ \text{mol}$$

**Step 3 — Ratio.**
$$n = \frac{0.1398}{0.0200} = 6.99 \approx 7$$

**Answer: $\ce{MgSO4 * 7H2O}$ — magnesium sulfate heptahydrate.** More than half the mass of the Epsom salt you pour in a bath is water that was riding inside the crystals.

### Example 6: The Closet Moisture Absorber

**Problem:** A 3.68 g sample of hydrated calcium chloride, $\ce{CaCl2 * nH2O}$, is heated to constant mass, leaving 2.78 g of $\ce{CaCl2}$. Find $n$.

**Solution:**

**Step 1 — Water mass.** $3.68 - 2.78 = 0.90$ g $\ce{H2O}$.

**Step 2 — Moles.** $M(\ce{CaCl2}) = 40.08 + 2(35.45) = 110.98$ g/mol.
$$\text{mol } \ce{H2O} = \frac{0.90}{18.02} = 0.0499 \ \text{mol} \qquad \text{mol } \ce{CaCl2} = \frac{2.78}{110.98} = 0.0251 \ \text{mol}$$

**Step 3 — Ratio.**
$$n = \frac{0.0499}{0.0251} = 1.99 \approx 2$$

**Answer: $\ce{CaCl2 * 2H2O}$ — calcium chloride dihydrate.**

### Example 7: Reverse Direction — Predict the Mass Loss

**Problem:** What percent of the mass of $\ce{CuSO4 * 5H2O}$ is water? If 10.00 g of the hydrate is heated to constant mass, what mass remains?

**Solution:**

**Step 1 — Molar masses.** Hydrate: $159.62 + 5(18.02) = 249.72$ g/mol. Water portion: $5 \times 18.02 = 90.10$ g/mol.

**Step 2 — Percent water.**
$$\%\ce{H2O} = \frac{90.10}{249.72} \times 100\% = 36.08\%$$

**Step 3 — Apply to 10.00 g.** Mass lost $= 10.00 \times 0.3608 = 3.61$ g, so mass remaining $= 10.00 - 3.61 = 6.39$ g.

**Answer: the hydrate is 36.08% water; 6.39 g of anhydrous $\ce{CuSO4}$ remains.** This is the "predict before you heat" direction — great for checking your lab data before you leave the bench.

### Example 8: Salt and Sand, With Real Masses

**Problem:** A student receives 10.00 g of a salt–sand mixture. She adds water, stirs, filters, and dries the sand: 6.35 g. She evaporates the filtrate to dryness and recovers 3.62 g of salt. Find the mass percent of each component, and account for the totals.

**Solution:**

**Step 1 — Percents, each based on the ORIGINAL 10.00 g.**
$$\%\text{ sand} = \frac{6.35}{10.00} \times 100\% = 63.5\% \qquad \%\text{ salt} = \frac{3.62}{10.00} \times 100\% = 36.2\%$$

**Step 2 — Account for the total.** $63.5\% + 36.2\% = 99.7\%$. The missing 0.3% (0.03 g) is normal handling loss — grains stuck to the beaker, a bit of solution left in the filter paper. Real separations rarely recover 100.0%.

**Step 3 — Why this worked.** Salt dissolves in water; sand doesn't (different physical properties). No chemical change occurred — which is exactly why "separable by physical means" is the test for a mixture.

**Answer: 63.5% sand, 36.2% salt by mass (≈0.3% handling loss).**

### Example 9: Splitting a Fertilizer Blend with Algebra

**Problem:** A 10.00 g fertilizer sample is a mixture of only $\ce{NH4NO3}$ and $\ce{(NH4)2SO4}$. Analysis shows it contains 3.00 g of nitrogen in total. Find the mass of each compound.

**Solution:**

**Step 1 — Nitrogen fingerprint of each compound.**
$$\ce{NH4NO3}: M = 80.05 \ \text{g/mol}, \quad \%\ce{N} = \frac{2(14.01)}{80.05} = 35.00\%$$
$$\ce{(NH4)2SO4}: M = 132.15 \ \text{g/mol}, \quad \%\ce{N} = \frac{2(14.01)}{132.15} = 21.20\%$$

**Step 2 — Set up the split.** Let $x$ = grams of $\ce{NH4NO3}$; then $(10.00 - x)$ = grams of $\ce{(NH4)2SO4}$. Each contributes its own fixed fraction of nitrogen:
$$0.3500x + 0.2120(10.00 - x) = 3.00$$

**Step 3 — Solve.**
$$0.3500x + 2.120 - 0.2120x = 3.00 \implies 0.1380x = 0.880 \implies x = 6.38 \ \text{g}$$

**Step 4 — Check.** $0.3500(6.38) + 0.2120(3.62) = 2.23 + 0.77 = 3.00$ g N. ✓

**Answer: 6.38 g of $\ce{NH4NO3}$ and 3.62 g of $\ce{(NH4)2SO4}$.** Notice the engine under the hood: the *mixture's* ratio was unknown, but each *compound's* nitrogen percent is locked by the law of definite proportions — fixed percents inside, variable blend outside.

### Example 10: Element Mass in an Impure Sample

**Problem:** A crusty lab-shelf sample is only 80.0% $\ce{CuSO4 * 5H2O}$ by mass (the rest is inert junk). How many grams of copper are in 5.00 g of the sample?

**Solution:**

**Step 1 — Mass of actual hydrate.**
$$5.00 \ \text{g sample} \times \frac{80.0 \ \text{g hydrate}}{100 \ \text{g sample}} = 4.00 \ \text{g } \ce{CuSO4 * 5H2O}$$

**Step 2 — Copper's fixed share of the hydrate.**
$$4.00 \ \text{g} \times \frac{63.55 \ \text{g Cu}}{249.72 \ \text{g hydrate}} = 1.02 \ \text{g Cu}$$

**Answer: 1.02 g of copper.** Two percent-style steps chained: mixture percent (measured, variable) first, then compound percent (fixed fingerprint) — a very AP-flavored combo.

### Example 11: Empirical Formula from Percents (Refresher)

**Problem:** A pure oxide of sulfur is 40.05% S and 59.95% O by mass. Find its empirical formula. (Full method in [The Mole](/chemistry/0207-the-mole) — this is a one-example tune-up.)

**Solution:**

**Step 1 — Percent to mass.** Assume a 100.0 g sample: 40.05 g S, 59.95 g O.

**Step 2 — Mass to moles.**
$$\frac{40.05}{32.07} = 1.249 \ \text{mol S} \qquad \frac{59.95}{16.00} = 3.747 \ \text{mol O}$$

**Step 3 — Divide by the smaller.**
$$\text{S}: \frac{1.249}{1.249} = 1 \qquad \text{O}: \frac{3.747}{1.249} = 3.00$$

**Answer: $\ce{SO3}$.** Same pipeline as the hydrate lab, if you squint — masses $\rightarrow$ moles $\rightarrow$ smallest whole-number ratio. The hydrate problem is just an empirical-formula problem where one "element" is a whole water molecule.

---

## Common Mistakes

| The mistake | Why it happens | How to avoid it |
|---|---|---|
| Dividing the leftover solid by the *hydrate's* molar mass | The problem statement names the hydrate, so it feels natural | The solid remaining after heating is **anhydrous** — always use the anhydrous molar mass in Step 3 |
| Treating the dot in $\ce{CuSO4 * 5H2O}$ as multiplication | It looks like a multiplication dot | The dot means "plus 5 waters": **add** $5 \times 18.02$ to the salt's molar mass |
| Using the final mass as the water mass | Rushing the subtraction | Water = **before − after**. The final mass is the salt, not the water |
| Computing % water with the anhydrous mass in the denominator | Percent problems blur together | % water $= \dfrac{\text{mass of water}}{\text{mass of hydrate}} \times 100\%$ — denominator is the whole original sample |
| Rounding $n = 2.5$ "up to 3" | Whole-number reflex | Ratios like 2.5 or 1.33 mean multiply through (×2, ×3) or re-check your arithmetic — only round when you're within a few hundredths (4.98 → 5) |
| Assuming matching percent composition proves the same molecular formula | The fingerprint idea, over-applied | Matching percents ⇒ same **empirical** formula. $\ce{CH2O}$ and $\ce{C6H12O6}$ share percents; a molar mass breaks the tie |
| Saying a homogeneous mixture is a pure substance | "Uniform" feels like "pure" | Uniform within the batch ≠ fixed by nature. Salt water is homogeneous *and* variable — a mixture |
| Stopping the heating after one round | Impatience (and hot crucibles) | Heat–cool–weigh, repeat until two weighings agree: **constant mass** |

---

## AP Exam Tips

- **Where this lives:** Topics 1.3–1.4 show up as multiple-choice conceptual questions (fixed vs. variable composition) and as the beloved **hydrate lab FRQ** — often a full lab-based free response with data tables and error analysis.
- **The conceptual money question, in all its costumes:** "Can two samples of a *compound* have different percent compositions?" (No — definite proportions.) "Can two samples of a *mixture*?" (Yes.) "A sample's %Na doesn't match $\ce{NaCl}$'s — what can you conclude?" (Not pure $\ce{NaCl}$.) Same idea, many phrasings — recognize the costume.
- **"Heated to constant mass" is a signal phrase.** It means *all* the water is gone, so the after-mass is trustworthy. If an FRQ asks *why* the student heats, cools, and weighs repeatedly, the scored answer is: to confirm mass no longer changes, showing all water of hydration has been removed.
- **Error analysis is where the points hide.** Reason it through the subtraction, don't memorize blindly:

| Lab error | Effect on masses | Effect on calculated $n$ |
|---|---|---|
| Stopped heating too soon (water remains) | "Anhydrous" mass too **high** → water mass too **low** | $n$ too **low** |
| Solid splatters out of the crucible during heating | Final mass too **low** → apparent water loss too **high** | $n$ too **high** |
| Overheating decomposes the salt itself (e.g., $\ce{CuSO4}$ losing $\ce{SO3}$) | Extra mass loss blamed on water | $n$ too **high** |
| Hot crucible cools uncovered; anhydrous salt reabsorbs moisture from air | Final mass creeps back **up** | $n$ too **low** |

- **Show the mole division explicitly** on FRQs: mol water over mol anhydrous salt, then the rounding to a whole number. Skipping the ratio step costs points even if your final formula is right.
- **Both exam sections are fair game:** the arithmetic here (subtract, divide by molar mass, divide moles) is very doable without a calculator in Section I, and the periodic table is always provided — no molar masses need memorizing.
- **Units and sig figs:** lab-data FRQs expect answers to sensible sig figs (your masses have 3, so $n = 4.98$ before rounding is exactly the kind of work they want to see).

---

## Practice Problems

### Problem 1

Classify each as a pure substance or a mixture; classify mixtures as homogeneous or heterogeneous: (a) trail mix, (b) distilled water, (c) salt water, (d) brass (a uniform copper–zinc alloy), (e) orange juice with pulp.

<details>
<summary><strong>Solution</strong></summary>

- (a) Trail mix — **mixture, heterogeneous** (different handfuls differ; components visible).
- (b) Distilled water — **pure substance** (compound, $\ce{H2O}$; fixed 2 H : 1 O).
- (c) Salt water — **mixture, homogeneous** (uniform throughout, but the salt fraction is variable batch to batch).
- (d) Brass — **mixture, homogeneous** (a solid solution; Cu:Zn ratio varies by alloy — that's why it can't be a compound).
- (e) OJ with pulp — **mixture, heterogeneous** (pulp settles; scoops differ).

**Answer: (b) is the only pure substance; (c) and (d) are homogeneous mixtures; (a) and (e) are heterogeneous.**

</details>

### Problem 2

Calculate the percent composition of potassium chlorate, $\ce{KClO3}$.

<details>
<summary><strong>Solution</strong></summary>

Molar mass: $39.10 + 35.45 + 3(16.00) = 122.55$ g/mol.

$$\%\ce{K} = \frac{39.10}{122.55} \times 100\% = 31.91\% \qquad \%\ce{Cl} = \frac{35.45}{122.55} \times 100\% = 28.93\%$$
$$\%\ce{O} = \frac{48.00}{122.55} \times 100\% = 39.17\%$$

Check: $31.91 + 28.93 + 39.17 = 100.01\%$ ✓ (rounding).

**Answer: 31.91% K, 28.93% Cl, 39.17% O.**

</details>

### Problem 3

One water sample comes from a San Diego tap, another from a melted Alaskan glacier. After purification, both are pure $\ce{H2O}$. Will their percent hydrogen by mass differ? What law answers this?

<details>
<summary><strong>Solution</strong></summary>

No. Pure water is a compound, so its composition is fixed regardless of source:

$$\%\ce{H} = \frac{2(1.008)}{18.02} \times 100\% = 11.19\%$$

for both samples. This is the **law of definite proportions**: a compound always contains the same elements in the same mass ratio.

**Answer: identical — 11.19% H in both, by the law of definite proportions.**

</details>

### Problem 4

A 2.443 g sample of $\ce{BaCl2 * nH2O}$ is heated to constant mass, leaving 2.082 g of anhydrous $\ce{BaCl2}$. Find $n$.

<details>
<summary><strong>Solution</strong></summary>

Water: $2.443 - 2.082 = 0.361$ g.

$M(\ce{BaCl2}) = 137.33 + 2(35.45) = 208.23$ g/mol.

$$\text{mol } \ce{BaCl2} = \frac{2.082}{208.23} = 0.01000 \ \text{mol} \qquad \text{mol } \ce{H2O} = \frac{0.361}{18.02} = 0.02003 \ \text{mol}$$

$$n = \frac{0.02003}{0.01000} = 2.00$$

**Answer: $n = 2$; the hydrate is $\ce{BaCl2 * 2H2O}$, barium chloride dihydrate.**

</details>

### Problem 5

Washing soda is $\ce{Na2CO3 * nH2O}$. A 5.724 g sample heated to constant mass leaves 2.120 g of $\ce{Na2CO3}$. Find $n$ and name the hydrate.

<details>
<summary><strong>Solution</strong></summary>

Water: $5.724 - 2.120 = 3.604$ g.

$M(\ce{Na2CO3}) = 2(22.99) + 12.01 + 3(16.00) = 105.99$ g/mol.

$$\text{mol } \ce{Na2CO3} = \frac{2.120}{105.99} = 0.02000 \ \text{mol} \qquad \text{mol } \ce{H2O} = \frac{3.604}{18.02} = 0.2000 \ \text{mol}$$

$$n = \frac{0.2000}{0.02000} = 10.0$$

**Answer: $\ce{Na2CO3 * 10H2O}$ — sodium carbonate decahydrate.** (More than 60% of washing soda's mass is water!)

</details>

### Problem 6

What percent of Epsom salt, $\ce{MgSO4 * 7H2O}$, is water? How many grams of water are locked inside a 25.0 g scoop?

<details>
<summary><strong>Solution</strong></summary>

Molar masses: anhydrous $\ce{MgSO4} = 120.38$ g/mol; water portion $= 7(18.02) = 126.14$ g/mol; hydrate $= 120.38 + 126.14 = 246.52$ g/mol.

$$\%\ce{H2O} = \frac{126.14}{246.52} \times 100\% = 51.17\%$$

$$25.0 \ \text{g} \times 0.5117 = 12.8 \ \text{g}$$

**Answer: 51.17% water; a 25.0 g scoop carries 12.8 g of water.**

</details>

### Problem 7

If 8.00 g of cobalt(II) chloride hexahydrate, $\ce{CoCl2 * 6H2O}$, is heated to constant mass, what mass of solid remains?

<details>
<summary><strong>Solution</strong></summary>

$M(\ce{CoCl2}) = 58.93 + 2(35.45) = 129.83$ g/mol; hydrate $= 129.83 + 6(18.02) = 237.95$ g/mol.

Anhydrous fraction: $\dfrac{129.83}{237.95} = 0.5457$.

$$8.00 \ \text{g} \times 0.5457 = 4.37 \ \text{g}$$

**Answer: 4.37 g of anhydrous $\ce{CoCl2}$ remains** (and the solid turns from pink to blue — this hydrate is the classic color-changing humidity indicator).

</details>

### Problem 8

A homemade sports-drink batch is mixed from 21.0 g sugar, 1.5 g salt, and 477.5 g water. Find the mass percent of sugar and of salt. Is this drink a pure substance?

<details>
<summary><strong>Solution</strong></summary>

Total mass: $21.0 + 1.5 + 477.5 = 500.0$ g.

$$\%\text{ sugar} = \frac{21.0}{500.0} \times 100\% = 4.20\% \qquad \%\text{ salt} = \frac{1.5}{500.0} \times 100\% = 0.30\%$$

Not a pure substance: it's a **homogeneous mixture**. It looks uniform, but tomorrow's batch could be 5% sugar and still be "sports drink" — composition is variable, so no formula exists.

**Answer: 4.20% sugar, 0.30% salt; a homogeneous mixture, not a pure substance.**

</details>

### Problem 9

A student separates an 8.40 g salt–sand mixture by dissolving, filtering, and drying. The recovered sand weighs 5.71 g. Assuming the rest is salt, find the mass percent of salt.

<details>
<summary><strong>Solution</strong></summary>

Salt mass: $8.40 - 5.71 = 2.69$ g.

$$\%\text{ salt} = \frac{2.69}{8.40} \times 100\% = 32.0\%$$

(And % sand $= 5.71/8.40 = 68.0\%$.) Note the denominator is the *original* mixture mass — the same before-minus-after logic as the hydrate lab, applied to a filter paper instead of a crucible.

**Answer: 32.0% salt (68.0% sand) by mass.**

</details>

### Problem 10

A 20.00 g mixture contains only $\ce{KCl}$ and $\ce{KNO3}$, and analysis shows 10.00 g of potassium in total. Find the mass of each compound. ($\%\ce{K}$ in $\ce{KCl} = 52.45\%$; $\%\ce{K}$ in $\ce{KNO3} = 38.67\%$.)

<details>
<summary><strong>Solution</strong></summary>

Let $x$ = grams of $\ce{KCl}$; then $(20.00 - x)$ = grams of $\ce{KNO3}$.

$$0.5245x + 0.3867(20.00 - x) = 10.00$$
$$0.5245x + 7.734 - 0.3867x = 10.00 \implies 0.1378x = 2.266 \implies x = 16.4 \ \text{g}$$

So $\ce{KNO3} = 20.00 - 16.4 = 3.6$ g. Check: $0.5245(16.4) + 0.3867(3.6) = 8.60 + 1.39 = 9.99 \approx 10.00$ g K ✓.

**Answer: 16.4 g $\ce{KCl}$ and 3.6 g $\ce{KNO3}$.**

</details>

### Problem 11

A pure compound is 63.65% N and 36.35% O by mass. Find its empirical formula.

<details>
<summary><strong>Solution</strong></summary>

In 100.0 g: 63.65 g N and 36.35 g O.

$$\frac{63.65}{14.01} = 4.543 \ \text{mol N} \qquad \frac{36.35}{16.00} = 2.272 \ \text{mol O}$$

Divide by the smaller: N $= 4.543/2.272 = 2.00$, O $= 1$.

**Answer: $\ce{N2O}$** (dinitrogen monoxide — laughing gas).

</details>

### Problem 12

In a hydrate lab, a student heats her sample once, sees it looks "dry and powdery," and stops without re-heating to check for constant mass. Will her calculated $n$ be too high, too low, or unaffected? Explain using the masses.

<details>
<summary><strong>Solution</strong></summary>

Some water of hydration likely remains in the solid. Trace the subtraction:

- Measured "anhydrous" mass is too **high** (it still contains water).
- Water mass (before − after) is therefore too **low** → moles of water too low.
- Moles of "anhydrous salt" computed from the inflated mass are too **high**.
- $n = \dfrac{\text{mol water (too low)}}{\text{mol salt (too high)}}$ — both errors push the same direction.

**Answer: $n$ comes out too LOW.** (The swimsuit version: taking the suit off the line while it's still damp makes you underestimate how much water it held.)

</details>

### Problem 13

During heating, another student's sample crackles and some solid splatters out of the crucible. How does this affect the calculated $n$?

<details>
<summary><strong>Solution</strong></summary>

Solid that splatters out is mass lost that was **not** water, but the calculation blames all mass loss on water:

- Final mass is too **low** → apparent water mass (before − after) is too **high** → mol water inflated.
- Moles of anhydrous salt (from the too-small final mass) come out too **low**.
- $n = \dfrac{\text{mol water (too high)}}{\text{mol salt (too low)}}$ — again both errors push together.

**Answer: $n$ comes out too HIGH.** (Same verdict if overheating decomposes the salt itself — any non-water mass loss masquerades as water.)

</details>

### Problem 14

Which of these percentages can differ between two correctly measured samples? (a) % O in pure $\ce{CO2}$, (b) % $\ce{NaCl}$ in ocean water, (c) % N in pure $\ce{NH3}$, (d) % peanuts in trail mix. Explain in one sentence.

<details>
<summary><strong>Solution</strong></summary>

Compounds have fixed composition (law of definite proportions); mixtures don't.

- (a) $\ce{CO2}$ is a compound → % O fixed (72.7%) everywhere. Cannot differ.
- (b) Ocean water is a mixture → salinity varies (the Mediterranean is saltier than the Pacific). **Can differ.**
- (c) $\ce{NH3}$ is a compound → % N fixed (82.2%). Cannot differ.
- (d) Trail mix is a mixture → peanut fraction is whatever got blended. **Can differ.**

**Answer: (b) and (d) can vary; (a) and (c) cannot.**

</details>

### Problem 15

A 50.0 g fertilizer sample is 60.0% $\ce{NH4NO3}$ and 40.0% $\ce{(NH4)2SO4}$ by mass. How many grams of nitrogen does it contain? (Use $\%\ce{N} = 35.00\%$ in $\ce{NH4NO3}$ and $21.20\%$ in $\ce{(NH4)2SO4}$.)

<details>
<summary><strong>Solution</strong></summary>

Mass of each compound:

$$50.0 \times 0.600 = 30.0 \ \text{g } \ce{NH4NO3} \qquad 50.0 \times 0.400 = 20.0 \ \text{g } \ce{(NH4)2SO4}$$

Nitrogen from each (fixed compound percents):

$$30.0 \times 0.3500 = 10.5 \ \text{g N} \qquad 20.0 \times 0.2120 = 4.24 \ \text{g N}$$

Total: $10.5 + 4.24 = 14.7$ g.

**Answer: 14.7 g of nitrogen.** (This is Example 9 run forward instead of backward — mixture percents first, compound fingerprints second.)

</details>

---

## Quick Reference

| Concept | The one-liner |
|---|---|
| Law of definite proportions | A compound's percent composition is fixed — same everywhere, always |
| Mixture | Variable composition, no formula, separable by physical means |
| Homogeneous vs. heterogeneous | Uniform throughout vs. different scoop-to-scoop; homogeneous ≠ pure |
| Percent composition (compound) | $\dfrac{\text{atoms} \times \text{atomic mass}}{\text{molar mass}} \times 100\%$ — the fingerprint |
| Mass percent (mixture) | $\dfrac{\text{mass of component}}{\text{total mass}} \times 100\%$ — measured per sample |
| Hydrate dot | $\ce{CuSO4 * 5H2O}$: dot means "plus," molar mass is a **sum** ($249.72$ g/mol) |
| Finding $n$ | water mass = before − after; $n = \dfrac{\text{mol } \ce{H2O}}{\text{mol anhydrous salt}}$ |
| % water in a hydrate | $\dfrac{n \times 18.02}{M_{\text{hydrate}}} \times 100\%$ |
| Constant mass | Heat–cool–weigh until two weighings agree → all water is gone |
| Under-heated | $n$ too low · Splattered/decomposed: $n$ too high |
| Two-compound split | Let $x$ = g of one compound; sum the element contributions; solve |

---

<div align="center">

[← Mass Spectrometry](/chemistry/0301-mass-spectrometry) | [Electron Configuration →](/chemistry/0303-electron-configuration)

</div>
