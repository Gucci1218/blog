# The Mole
<p class="article-date">July 4, 2026</p>

*Last weekend Dad and I did a Costco run, and we grabbed one of those 25-pound bags of rice. Here's the thing nobody stops to think about: there are roughly 450,000 grains in that bag, and not one person at Costco ever counted them. The bag says 25 lb, and everyone — the farmer, the store, us — trusts the **weight** to stand in for the **count**, because rice grains are uniform enough that weighing IS counting. Chemists pull the exact same move. Atoms are absurdly too small and too numerous to count one by one, so chemistry invented a counting unit — the mole, just a number, $6.022 \times 10^{23}$, the way "a dozen" is just 12 — and sized it so cleverly that the periodic table becomes a price sheet for atoms: the atomic mass printed under each element is also its grams per mole. Weigh the sample, and you've counted the atoms. This article is the capstone of our foundations unit, and honestly the single most-used skill in all of AP Chemistry — every stoichiometry, gas law, solution, and thermochemistry problem you will ever do runs through the mole.*

---

## What You'll Learn

- State what a mole is (just a number!) and explain where $6.022 \times 10^{23}$ comes from — the 12 g of $\ce{^{12}C}$ definition
- Explain why molar mass in g/mol is numerically equal to atomic mass in amu, and why that makes the periodic table a "weigh-to-count" cheat sheet
- Compute molar masses of compounds, including formulas with parentheses like $\ce{Ca(NO3)2}$ and hydrates like $\ce{CuSO4 * 5H2O}$
- Convert between grams, moles, and particles in any direction using dimensional analysis chains
- Count atoms of a *single element* inside moles of a compound (the classic AP trap)
- Calculate percent composition by mass for any compound
- Determine an empirical formula from percent composition, and a molecular formula from the empirical formula plus a molar mass
- Use mole ratios from a balanced equation to preview stoichiometry (full treatment coming in AP Unit 4)

---

## Prerequisites

- [Scientific Notation](/chemistry/0101-scientific-notation) — every particle count is a number like $6.022 \times 10^{23}$; you'll multiply and divide these constantly
- [Dimensional Analysis](/chemistry/0103-dimensional-analysis) — every mole conversion is a railroad chain of unit fractions; this article is that skill's final boss
- [Balancing Equations](/chemistry/0206-balancing-equations) — coefficients in a balanced equation are mole ratios, which is where this article hands off to stoichiometry

---

## The Core Concept

### Intuition First

Back to the Costco rice bag. Ask yourself: why does *weighing* rice count it?

Two facts make it work:

1. **Rice grains are (nearly) uniform.** Every grain of the same variety weighs about the same — say 0.025 g.
2. **Somebody measured the grams-per-grain once**, so mass and count are locked together forever: 25 lb ≈ 11{,}340 g, and $11{,}340 \div 0.025 \approx 450{,}000$ grains. Nobody counts. Everybody weighs.

Atoms are even better behaved than rice. Every atom of $\ce{^{12}C}$ is *exactly* identical to every other one — not "close enough," but perfectly interchangeable. So if we know the mass of one atom, weighing a sample counts its atoms with total confidence.

Here's the structural map, and it's worth staring at:

| Costco rice | Chemistry |
|---|---|
| "a dozen" (just the number 12) | **a mole** (just the number $6.022 \times 10^{23}$) |
| grams per bag printed on the label | **molar mass** (grams per mole) |
| weighing the bag = counting the grains | weighing a sample = counting the atoms |
| the label was calibrated once at the factory | the periodic table was calibrated once, for every element |

And the genius part — the reason the whole system feels like a magic trick — is this: **the molar mass of an element in grams per mole is numerically equal to its atomic mass in amu.** Carbon's box on the periodic table says 12.01. That means one carbon atom weighs 12.01 amu, *and* one mole of carbon atoms weighs 12.01 g. Same number, two scales. The periodic table isn't just a list of atoms — it's the price sheet that converts between the atom-sized world and the gram-sized world you can put on a balance.

### The Mole Is Just a Number

A **mole** (symbol: mol) is a counting unit, exactly like "dozen" or "pair":

$$1 \text{ mole} = 6.022 \times 10^{23} \text{ things}$$

That number, $6.022 \times 10^{23}$, is **Avogadro's number** ($N_A$). A mole of eggs is $6.022 \times 10^{23}$ eggs. A mole of water molecules is $6.022 \times 10^{23}$ molecules of $\ce{H2O}$. The unit doesn't care what it's counting.

$$N_A = 6.022 \times 10^{23} \ \text{particles/mol}$$

"Particles" is deliberately vague — it means whatever the formula names: atoms of an element, molecules of a molecular compound, formula units of an ionic compound like $\ce{NaCl}$.

### Why $6.022 \times 10^{23}$? The amu ↔ Gram Bridge

Nobody picked $6.022 \times 10^{23}$ because it's pretty. It was *reverse-engineered*, and the definition tells you the whole story. Let's go slowly.

**Step 1 — the problem.** Atomic masses are measured in **atomic mass units (amu)**. One atom of $\ce{^{12}C}$ is *defined* as exactly 12 amu. That's a lovely unit for one atom and a useless unit in the lab, because balances read grams. We need a bridge between amu-world and gram-world.

**Step 2 — the definition.** Chemists defined the mole like this:

> **One mole is the number of atoms in exactly 12 g of $\ce{^{12}C}$.**

Look at what that sentence does. It grabs the *same number* — 12 — from both worlds. One atom of $\ce{^{12}C}$ is 12 **amu**; one mole of $\ce{^{12}C}$ is 12 **g**. The definition forces the amu-scale and the gram-scale to line up number-for-number.

**Step 3 — count the atoms.** How many $\ce{^{12}C}$ atoms are in 12 g? One amu is $1.66054 \times 10^{-24}$ g, so one $\ce{^{12}C}$ atom weighs $12 \times 1.66054 \times 10^{-24}$ g. Divide:

$$\frac{12 \ \text{g}}{12 \times 1.66054 \times 10^{-24} \ \text{g/atom}} = \frac{1}{1.66054 \times 10^{-24}} = 6.022 \times 10^{23} \ \text{atoms}$$

So Avogadro's number is literally **the number of amu in one gram**. That's all it is. It's the exchange rate between the two mass scales:

$$1 \ \text{g} = 6.022 \times 10^{23} \ \text{amu}$$

**Step 4 — the payoff.** Because the scales line up at carbon, they line up *everywhere*. A magnesium atom weighs 24.31 amu — which is $24.31/12$ times heavier than a $\ce{^{12}C}$ atom — so a mole of magnesium weighs $24.31/12$ times more than a mole of carbon: exactly 24.31 g. For **every** element:

$$\text{atomic mass in amu (one atom)} \;=\; \text{molar mass in g/mol (one mole)}$$

One definition, one clever number, and the entire periodic table doubles as a gram-scale catalog. That is why chemists get emotional about the mole.

> **Note:** In 2019 the definition was updated so that a mole is *exactly* $6.02214076 \times 10^{23}$ particles, full stop. For AP purposes the "12 g of $\ce{^{12}C}$" story is still the right way to understand *why* the number has the value it has, and $6.022 \times 10^{23}$ is the precision you'll use.

### How Big Is a Mole, Really?

Time to cash in our [scientific notation](/chemistry/0101-scientific-notation) skills, because $6.022 \times 10^{23}$ refuses to be imagined without math.

**A mole of rice grains.** One grain of rice occupies roughly $0.03 \ \text{cm}^3 = 3 \times 10^{-8} \ \text{m}^3$. Earth's entire surface area (oceans included) is about $5.1 \times 10^{14} \ \text{m}^2$. Spread one mole of rice evenly over the whole planet:

$$\text{depth} = \frac{(6.022 \times 10^{23})(3 \times 10^{-8} \ \text{m}^3)}{5.1 \times 10^{14} \ \text{m}^2} \approx 3.5 \times 10^{1} \ \text{m}$$

**Thirty-five meters.** A ten-story building of rice, covering every square meter of Earth — the Pacific, Antarctica, downtown San Diego, everything. That's *one mole* of something as big as a rice grain.

**A mole of seconds.** One year is about $3.156 \times 10^7$ s, so a mole of seconds is

$$\frac{6.022 \times 10^{23} \ \text{s}}{3.156 \times 10^{7} \ \text{s/yr}} \approx 1.9 \times 10^{16} \ \text{years}$$

— about 1.4 *million* times the age of the universe.

And yet: 18 g of water — two sips — contains a full mole of $\ce{H2O}$ molecules. Atoms are just that small. This is exactly why we can't count them and *must* weigh them.

### Molar Mass: Reading the Price Sheet

The **molar mass** ($M$) of a substance is the mass in grams of one mole of it. Units: g/mol.

**For elements:** read it straight off the periodic table. The decimal number in each element's box is both the average atomic mass (amu) and the molar mass (g/mol).

| Element | Molar mass (g/mol) |
|---|---|
| $\ce{H}$ | 1.01 |
| $\ce{C}$ | 12.01 |
| $\ce{N}$ | 14.01 |
| $\ce{O}$ | 16.00 |
| $\ce{Na}$ | 22.99 |
| $\ce{S}$ | 32.07 |
| $\ce{Cl}$ | 35.45 |
| $\ce{Ca}$ | 40.08 |
| $\ce{Cu}$ | 63.55 |

(Standard practice: keep molar masses to **two decimal places**.)

**For compounds:** add up the molar masses of every atom in the formula. Subscripts multiply; parentheses multiply everything inside them; the dot in a hydrate means the water molecules ride along in the same formula unit. We'll grind through examples of each below.

### The Mole Map

Every mole problem in existence lives on this map:

```
              ÷ molar mass                    ÷ 6.022 × 10²³
             (g/mol)                          (particles/mol)
   ┌───────┐ ───────────────► ┌───────┐ ◄─────────────── ┌───────────┐
   │ GRAMS │                  │ MOLES │                   │ PARTICLES │
   └───────┘ ◄─────────────── └───────┘ ───────────────► └───────────┘
              × molar mass                    × 6.022 × 10²³
```

Three stations, and **moles is the central hub** — Grand Central Station. You cannot travel from grams to particles (or back) without passing through moles. Two exchange rates cover every trip:

$$\frac{1 \ \text{mol}}{M \ \text{g}} \quad \text{and} \quad \frac{6.022 \times 10^{23} \ \text{particles}}{1 \ \text{mol}}$$

And here's the key mental move: **every trip on this map is a railroad chain from [Dimensional Analysis](/chemistry/0103-dimensional-analysis)**. Start with your known quantity, multiply by conversion factors flipped so units cancel, and read the destination unit off the end. Grams to molecules? Two cars on the train:

$$\text{g} \times \frac{1 \ \text{mol}}{M \ \text{g}} \times \frac{6.022 \times 10^{23} \ \text{molecules}}{1 \ \text{mol}} = \text{molecules}$$

One optional side spur extends the map: from moles of a *compound* to moles of *one element inside it*, the conversion factor is the **subscript** — e.g., $\frac{2 \ \text{mol H}}{1 \ \text{mol } \ce{H2O}}$. That spur is where the AP exam hides its favorite trap, so we'll drill it hard.

---

## Worked Examples

### Example 1: Molar Mass of Simple Compounds

**Problem:** Calculate the molar mass of (a) $\ce{H2O}$ and (b) $\ce{CO2}$.

**Solution:**

**Step 1:** Inventory the atoms. $\ce{H2O}$: 2 H, 1 O. $\ce{CO2}$: 1 C, 2 O.

**Step 2:** Multiply each count by the element's molar mass and add.

(a) $\ce{H2O}$:

$$2(1.01) + 1(16.00) = 2.02 + 16.00 = 18.02 \ \text{g/mol}$$

(b) $\ce{CO2}$:

$$1(12.01) + 2(16.00) = 12.01 + 32.00 = 44.01 \ \text{g/mol}$$

**Answer: $M_{\ce{H2O}} = 18.02$ g/mol; $M_{\ce{CO2}} = 44.01$ g/mol.**

### Example 2: Molar Mass with Parentheses — $\ce{Ca(NO3)2}$

**Problem:** Calculate the molar mass of calcium nitrate, $\ce{Ca(NO3)2}$.

**Solution:**

**Step 1:** Handle the parentheses first. The subscript 2 outside multiplies *everything* inside: $\ce{(NO3)2}$ means 2 N and 6 O.

**Step 2:** Full inventory: 1 Ca, 2 N, 6 O.

**Step 3:** Add it up:

$$1(40.08) + 2(14.01) + 6(16.00) = 40.08 + 28.02 + 96.00 = 164.10 \ \text{g/mol}$$

**Answer: $M_{\ce{Ca(NO3)2}} = 164.10$ g/mol.**

The classic error is reading $\ce{(NO3)2}$ as 2 N and *3* O. The outside subscript multiplies the oxygen too: $3 \times 2 = 6$ O.

### Example 3: Molar Mass of a Hydrate — $\ce{CuSO4 * 5H2O}$ (Bonus)

**Problem:** Copper(II) sulfate pentahydrate, $\ce{CuSO4 * 5H2O}$, is the gorgeous blue crystal you'll meet in lab. Find its molar mass.

**Solution:**

**Step 1:** The dot means five whole $\ce{H2O}$ molecules are locked inside each formula unit of the crystal. They count fully toward the mass.

**Step 2:** Anhydrous part, $\ce{CuSO4}$:

$$63.55 + 32.07 + 4(16.00) = 159.62 \ \text{g/mol}$$

**Step 3:** Water part, $5 \times \ce{H2O}$:

$$5(18.02) = 90.10 \ \text{g/mol}$$

**Step 4:** Total:

$$159.62 + 90.10 = 249.72 \ \text{g/mol}$$

**Answer: $M_{\ce{CuSO4 * 5H2O}} = 249.72$ g/mol.**

### Example 4: Grams → Moles

**Problem:** The seashells scattered along Torrey Pines State Beach are mostly calcium carbonate, $\ce{CaCO3}$. How many moles are in a 50.0 g shell?

**Solution:**

**Step 1:** Molar mass of $\ce{CaCO3}$: $40.08 + 12.01 + 3(16.00) = 100.09$ g/mol.

**Step 2:** One railroad car — flip the molar mass so grams cancel:

$$50.0 \ \cancel{\text{g}} \times \frac{1 \ \text{mol}}{100.09 \ \cancel{\text{g}}} = 0.500 \ \text{mol}$$

**Answer: 0.500 mol of $\ce{CaCO3}$.**

### Example 5: Moles → Grams

**Problem:** A boba shop's syrup recipe calls for 0.125 mol of sucrose, $\ce{C12H22O11}$, per drink. How many grams of sugar is that?

**Solution:**

**Step 1:** Molar mass of $\ce{C12H22O11}$:

$$12(12.01) + 22(1.01) + 11(16.00) = 144.12 + 22.22 + 176.00 = 342.34 \ \text{g/mol}$$

**Step 2:** Multiply by molar mass (moles cancel):

$$0.125 \ \cancel{\text{mol}} \times \frac{342.34 \ \text{g}}{1 \ \cancel{\text{mol}}} = 42.8 \ \text{g}$$

**Answer: 42.8 g of sucrose.** (Almost 43 grams of sugar per drink. I know. I still ordered it.)

### Example 6: Grams → Molecules (the Two-Car Train)

**Problem:** How many molecules of water are in 10.0 g of $\ce{H2O}$?

**Solution:**

**Step 1:** Map the route: grams → moles → molecules. Two conversion factors, one chain.

**Step 2:**

$$10.0 \ \cancel{\text{g}} \times \frac{1 \ \cancel{\text{mol}}}{18.02 \ \cancel{\text{g}}} \times \frac{6.022 \times 10^{23} \ \text{molecules}}{1 \ \cancel{\text{mol}}}$$

**Step 3:** Arithmetic: $10.0 / 18.02 = 0.5549$ mol, then $0.5549 \times 6.022 \times 10^{23} = 3.34 \times 10^{23}$.

**Answer: $3.34 \times 10^{23}$ molecules of $\ce{H2O}$.**

Notice we never jumped straight from grams to molecules — the train always stops at Moles station.

### Example 7: Atoms → Grams (the Reverse Trip)

**Problem:** A gold nanoparticle sample contains $1.00 \times 10^{22}$ atoms of $\ce{Au}$. What is its mass?

**Solution:**

**Step 1:** Route: atoms → moles → grams. Same map, driven backwards.

**Step 2:**

$$1.00 \times 10^{22} \ \cancel{\text{atoms}} \times \frac{1 \ \cancel{\text{mol}}}{6.022 \times 10^{23} \ \cancel{\text{atoms}}} \times \frac{196.97 \ \text{g}}{1 \ \cancel{\text{mol}}}$$

**Step 3:** $1.00 \times 10^{22} / 6.022 \times 10^{23} = 1.661 \times 10^{-2}$ mol, then $\times \, 196.97 = 3.27$ g.

**Answer: 3.27 g of gold.**

### Example 8: Atoms of ONE Element in a Compound (the AP Trap)

**Problem:** How many oxygen **atoms** are in 2.00 mol of $\ce{Ca(NO3)2}$?

**Solution:**

**Step 1:** Don't touch Avogadro's number yet! First convert moles of *compound* to moles of *oxygen atoms* using the subscript. Each formula unit of $\ce{Ca(NO3)2}$ contains $3 \times 2 = 6$ oxygen atoms, so:

$$2.00 \ \cancel{\text{mol } \ce{Ca(NO3)2}} \times \frac{6 \ \text{mol O}}{1 \ \cancel{\text{mol } \ce{Ca(NO3)2}}} = 12.0 \ \text{mol O}$$

**Step 2:** *Now* convert moles of O atoms to atoms:

$$12.0 \ \cancel{\text{mol O}} \times \frac{6.022 \times 10^{23} \ \text{atoms}}{1 \ \cancel{\text{mol}}} = 7.23 \times 10^{24} \ \text{atoms O}$$

**Answer: $7.23 \times 10^{24}$ oxygen atoms.**

The trap has two teeth: forgetting that the outside subscript makes it 6 O (not 3), and answering "molecules of compound" when the question asked "atoms of one element." Read the question twice.

### Example 9: Percent Composition by Mass

**Problem:** (a) Find the percent composition of $\ce{H2O}$. (b) Fertilizer bags advertise their nitrogen content. What percent of ammonium nitrate, $\ce{NH4NO3}$, is nitrogen by mass?

**Solution:**

The formula:

$$\% \ \text{element} = \frac{(\text{atoms of element}) \times (\text{molar mass of element})}{\text{molar mass of compound}} \times 100\%$$

**(a) Water.** $M = 18.02$ g/mol.

$$\%\ce{H} = \frac{2(1.01)}{18.02} \times 100\% = 11.2\% \qquad \%\ce{O} = \frac{16.00}{18.02} \times 100\% = 88.8\%$$

(Check: $11.2 + 88.8 = 100.0$. ✓)

**(b) Ammonium nitrate.** Inventory: 2 N, 4 H, 3 O.

$$M = 2(14.01) + 4(1.01) + 3(16.00) = 28.02 + 4.04 + 48.00 = 80.06 \ \text{g/mol}$$

$$\%\ce{N} = \frac{2(14.01)}{80.06} \times 100\% = \frac{28.02}{80.06} \times 100\% = 35.00\%$$

**Answer: water is 11.2% H and 88.8% O; ammonium nitrate is 35.00% N by mass.**

Note the trap inside the trap: $\ce{NH4NO3}$ has **two** nitrogen atoms — one in the ammonium, one in the nitrate. Count them all before you divide.

### Example 10: Empirical Formula from Percent Composition

**Problem:** A phosphorus oxide is 43.6% P and 56.4% O by mass. Find its empirical formula.

**Solution:**

The mantra: **percent → grams → moles → smallest ratio.**

**Step 1 (percent → grams):** Assume a 100 g sample, so percents become grams: 43.6 g P, 56.4 g O.

**Step 2 (grams → moles):**

$$43.6 \ \text{g} \times \frac{1 \ \text{mol}}{30.97 \ \text{g}} = 1.408 \ \text{mol P} \qquad 56.4 \ \text{g} \times \frac{1 \ \text{mol}}{16.00 \ \text{g}} = 3.525 \ \text{mol O}$$

**Step 3 (divide by the smallest):**

$$\text{P}: \frac{1.408}{1.408} = 1.00 \qquad \text{O}: \frac{3.525}{1.408} = 2.50$$

**Step 4 (clear the .5 — multiply, don't round!):** 2.50 is nowhere near a whole number, and rounding it to 2 or 3 would be fabricating data. Multiply *both* by 2:

$$\text{P}: 1.00 \times 2 = 2 \qquad \text{O}: 2.50 \times 2 = 5$$

**Answer: $\ce{P2O5}$.**

Rule of thumb for clearing decimals: ratio ends in .50 → multiply by 2; ends in .33 or .67 → multiply by 3; ends in .25 or .75 → multiply by 4. Only round when you're within about 0.05 of a whole number.

### Example 11: Molecular Formula from Empirical Formula + Molar Mass

**Problem:** A sugar has empirical formula $\ce{CH2O}$ and a molar mass of 180.18 g/mol. Find its molecular formula.

**Solution:**

**Step 1:** The molecular formula is a whole-number multiple of the empirical formula: $(\ce{CH2O})_n$.

**Step 2:** Empirical formula mass:

$$12.01 + 2(1.01) + 16.00 = 30.03 \ \text{g/mol}$$

**Step 3:** Find the multiplier:

$$n = \frac{\text{molar mass}}{\text{empirical mass}} = \frac{180.18}{30.03} = 6.00$$

**Step 4:** Multiply every subscript by 6: $\ce{C6H12O6}$.

**Answer: $\ce{C6H12O6}$ — glucose.** Same 1:2:1 recipe as formaldehyde ($\ce{CH2O}$) and acetic acid ($\ce{C2H4O2}$), completely different molecules. That's exactly why the empirical formula alone isn't enough — you need the molar mass to know how many times the recipe repeats.

### Example 12: Stoichiometry Teaser — Mole Ratios from a Balanced Equation

**Problem:** Hydrogen fuel cells run on $\ce{2H2 + O2 -> 2H2O}$. If a fuel cell consumes 4.00 mol of $\ce{H2}$, how many grams of water does it produce?

**Solution:**

**Step 1:** Back in [Balancing Equations](/chemistry/0206-balancing-equations) we said coefficients count *particles*. But if the ratio holds particle-for-particle, it holds dozen-for-dozen and mole-for-mole too. So the coefficients hand us a brand-new conversion factor:

$$\frac{2 \ \text{mol} \ \ce{H2O}}{2 \ \text{mol} \ \ce{H2}}$$

**Step 2:** Chain it — moles of $\ce{H2}$ → moles of $\ce{H2O}$ → grams of $\ce{H2O}$:

$$4.00 \ \cancel{\text{mol} \ \ce{H2}} \times \frac{2 \ \cancel{\text{mol} \ \ce{H2O}}}{2 \ \cancel{\text{mol} \ \ce{H2}}} \times \frac{18.02 \ \text{g}}{1 \ \cancel{\text{mol} \ \ce{H2O}}} = 72.1 \ \text{g}$$

**Answer: 72.1 g of $\ce{H2O}$.**

That right there — grams of one substance to grams of another, via moles and a coefficient ratio — is **stoichiometry**, the beating heart of AP Unit 4. We just did it with one extra railroad car. Everything in that unit is this map plus one bridge.

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Using the **atomic number** instead of the atomic mass | Both numbers sit in the element's box | Molar mass is the decimal number (carbon: 12.01, not 6) |
| Ignoring parentheses: reading $\ce{Ca(NO3)2}$ as 2 N, 3 O | Outside subscript looks like it only touches the last atom | It multiplies *everything* inside: 2 N and 6 O |
| Forgetting the water in hydrates like $\ce{CuSO4 * 5H2O}$ | The dot looks decorative | Those 5 waters are 90.10 g/mol — over a third of the mass |
| Jumping grams → particles directly | Impatience | Every trip passes through Moles station. No exceptions |
| Multiplying by $N_A$ when you should divide (or vice versa) | Memorizing "the formula" instead of tracking units | Write the railroad chain; if units don't cancel, flip the factor |
| Answering "molecules of compound" when asked for "atoms of one element" | Not reading the question twice | Insert the subscript factor (e.g., $\frac{6 \ \text{mol O}}{1 \ \text{mol} \ \ce{Ca(NO3)2}}$) *before* Avogadro's number |
| Rounding a mole ratio of 2.50 to 2 or 3 | Wanting whole numbers *now* | Multiply the whole ratio to clear the decimal (.5 → ×2, .33 → ×3, .25 → ×4) |
| Rounding molar masses to whole numbers (Cl = 35?) | Laziness | Two decimal places is standard; $\ce{Cl}$ is 35.45, and the difference shows up in your final sig figs |
| Mixing amu and grams mid-problem | The numbers are numerically equal | amu is per *atom*, g/mol is per *mole*. Pick the lane the problem lives in |

---

## AP Exam Tips

- **The mole is everywhere.** Mole conversions appear inside nearly every FRQ — stoichiometry, gas laws, titrations, thermochemistry, electrochemistry. It's rarely "the question"; it's the toll you pay to *start* the question. If this article's map isn't automatic, every later unit gets harder.
- **Show units at every step.** FRQ graders award work-shown credit, and a railroad chain with visible, canceling units is the clearest possible work. A bare number with no units can lose you the point even when the arithmetic is right.
- **Two decimal places on molar masses** is standard practice ($\ce{H}$ = 1.01, $\ce{O}$ = 16.00, $\ce{Cl}$ = 35.45). It keeps your answer safely inside sig-fig tolerance on grid-ins and FRQs.
- **Avogadro's number and $n = m/M$ are on the AP reference sheet** — you don't memorize the constant, but you absolutely must know *when* to multiply vs. divide by it. Units decide, every time.
- **Empirical/molecular formula questions** live in AP Unit 1, often dressed up with mass spectrometry or combustion data. The skeleton is always: percent → grams → moles → smallest ratio → clear decimals → (if given molar mass) find $n$.
- **Percent composition checks**: your percents must sum to 100% (within rounding). Free error detection — use it.
- **Watch for "atoms of X" vs. "molecules of Y"** in multiple choice. The wrong answers are precision-engineered from exactly the mistakes in the table above.

---

## Practice Problems

### Problem 1

Calculate the molar mass of sodium chloride, $\ce{NaCl}$.

<details>
<summary><strong>Solution</strong></summary>

One Na and one Cl:

$$22.99 + 35.45 = 58.44 \ \text{g/mol}$$

**Answer: 58.44 g/mol.**

</details>

### Problem 2

Calculate the molar mass of aluminum sulfate, $\ce{Al2(SO4)3}$.

<details>
<summary><strong>Solution</strong></summary>

Parentheses first: $\ce{(SO4)3}$ = 3 S and 12 O. Full inventory: 2 Al, 3 S, 12 O.

$$2(26.98) + 3(32.07) + 12(16.00) = 53.96 + 96.21 + 192.00 = 342.17 \ \text{g/mol}$$

**Answer: 342.17 g/mol.**

</details>

### Problem 3

Epsom salt is magnesium sulfate heptahydrate, $\ce{MgSO4 * 7H2O}$. Find its molar mass.

<details>
<summary><strong>Solution</strong></summary>

Anhydrous part: $24.31 + 32.07 + 4(16.00) = 120.38$ g/mol.

Water part: $7(18.02) = 126.14$ g/mol.

$$120.38 + 126.14 = 246.52 \ \text{g/mol}$$

**Answer: 246.52 g/mol.** (Notice the water is *more than half* the mass of the crystal.)

</details>

### Problem 4

How many moles of glucose, $\ce{C6H12O6}$, are in a 100.0 g sample?

<details>
<summary><strong>Solution</strong></summary>

$M_{\ce{C6H12O6}} = 6(12.01) + 12(1.01) + 6(16.00) = 72.06 + 12.12 + 96.00 = 180.18$ g/mol.

$$100.0 \ \cancel{\text{g}} \times \frac{1 \ \text{mol}}{180.18 \ \cancel{\text{g}}} = 0.5550 \ \text{mol}$$

**Answer: 0.5550 mol of glucose.**

</details>

### Problem 5

What is the mass of 0.750 mol of baking soda, $\ce{NaHCO3}$?

<details>
<summary><strong>Solution</strong></summary>

$M_{\ce{NaHCO3}} = 22.99 + 1.01 + 12.01 + 3(16.00) = 84.01$ g/mol.

$$0.750 \ \cancel{\text{mol}} \times \frac{84.01 \ \text{g}}{1 \ \cancel{\text{mol}}} = 63.0 \ \text{g}$$

**Answer: 63.0 g of $\ce{NaHCO3}$.**

</details>

### Problem 6

How many molecules of $\ce{CO2}$ are in 10.0 g of dry ice?

<details>
<summary><strong>Solution</strong></summary>

Route: grams → moles → molecules. $M_{\ce{CO2}} = 44.01$ g/mol.

$$10.0 \ \cancel{\text{g}} \times \frac{1 \ \cancel{\text{mol}}}{44.01 \ \cancel{\text{g}}} \times \frac{6.022 \times 10^{23} \ \text{molecules}}{1 \ \cancel{\text{mol}}} = 1.37 \times 10^{23} \ \text{molecules}$$

**Answer: $1.37 \times 10^{23}$ molecules of $\ce{CO2}$.**

</details>

### Problem 7

A sample contains $3.01 \times 10^{22}$ atoms of gold ($\ce{Au}$, 196.97 g/mol). What is its mass in grams?

<details>
<summary><strong>Solution</strong></summary>

Route: atoms → moles → grams.

$$3.01 \times 10^{22} \ \cancel{\text{atoms}} \times \frac{1 \ \cancel{\text{mol}}}{6.022 \times 10^{23} \ \cancel{\text{atoms}}} \times \frac{196.97 \ \text{g}}{1 \ \cancel{\text{mol}}}$$

$3.01 \times 10^{22} / 6.022 \times 10^{23} = 0.0500$ mol, then $0.0500 \times 196.97 = 9.85$ g.

**Answer: 9.85 g of gold.**

</details>

### Problem 8

How many hydrogen **atoms** are in 2.50 mol of ammonia, $\ce{NH3}$?

<details>
<summary><strong>Solution</strong></summary>

Subscript first, Avogadro second:

$$2.50 \ \cancel{\text{mol} \ \ce{NH3}} \times \frac{3 \ \text{mol H}}{1 \ \cancel{\text{mol} \ \ce{NH3}}} = 7.50 \ \text{mol H}$$

$$7.50 \ \cancel{\text{mol}} \times \frac{6.022 \times 10^{23} \ \text{atoms}}{1 \ \cancel{\text{mol}}} = 4.52 \times 10^{24} \ \text{atoms}$$

**Answer: $4.52 \times 10^{24}$ hydrogen atoms.**

</details>

### Problem 9

How many hydrogen atoms are in 36.04 g of water? (This one runs the full map: grams → moles of compound → moles of element → atoms.)

<details>
<summary><strong>Solution</strong></summary>

One chain, three cars:

$$36.04 \ \cancel{\text{g}} \times \frac{1 \ \cancel{\text{mol} \ \ce{H2O}}}{18.02 \ \cancel{\text{g}}} \times \frac{2 \ \cancel{\text{mol H}}}{1 \ \cancel{\text{mol} \ \ce{H2O}}} \times \frac{6.022 \times 10^{23} \ \text{atoms}}{1 \ \cancel{\text{mol H}}}$$

$36.04 / 18.02 = 2.000$ mol $\ce{H2O}$ → $4.000$ mol H → $2.409 \times 10^{24}$ atoms.

**Answer: $2.409 \times 10^{24}$ hydrogen atoms.**

</details>

### Problem 10

What is the percent nitrogen by mass in potassium nitrate, $\ce{KNO3}$?

<details>
<summary><strong>Solution</strong></summary>

$M_{\ce{KNO3}} = 39.10 + 14.01 + 3(16.00) = 101.11$ g/mol.

$$\%\ce{N} = \frac{14.01}{101.11} \times 100\% = 13.86\%$$

**Answer: 13.86% N.**

</details>

### Problem 11

A farmer is choosing between two fertilizers: ammonium nitrate, $\ce{NH4NO3}$, and urea, $\ce{CO(NH2)2}$. Which delivers more nitrogen per gram? Support your answer with percent-composition calculations.

<details>
<summary><strong>Solution</strong></summary>

**Ammonium nitrate** (from Example 9): $M = 80.06$ g/mol, 2 N per formula unit.

$$\%\ce{N} = \frac{28.02}{80.06} \times 100\% = 35.00\%$$

**Urea:** inventory 1 C, 1 O, 2 N, 4 H.

$$M = 12.01 + 16.00 + 2(14.01) + 4(1.01) = 60.07 \ \text{g/mol}$$

$$\%\ce{N} = \frac{28.02}{60.07} \times 100\% = 46.65\%$$

**Answer: urea, at 46.65% N vs. 35.00% N — nearly half of every gram of urea is nitrogen.**

</details>

### Problem 12

A compound is 40.0% C, 6.7% H, and 53.3% O by mass. Find its empirical formula.

<details>
<summary><strong>Solution</strong></summary>

Percent → grams (assume 100 g): 40.0 g C, 6.7 g H, 53.3 g O.

Grams → moles:

$$\frac{40.0}{12.01} = 3.33 \ \text{mol C} \qquad \frac{6.7}{1.01} = 6.6 \ \text{mol H} \qquad \frac{53.3}{16.00} = 3.33 \ \text{mol O}$$

Divide by the smallest (3.33):

$$\text{C}: 1.00 \qquad \text{H}: 2.0 \qquad \text{O}: 1.00$$

**Answer: $\ce{CH2O}$.**

</details>

### Problem 13

An iron oxide is 69.9% Fe and 30.1% O by mass. Find its empirical formula. ($\ce{Fe}$: 55.85 g/mol)

<details>
<summary><strong>Solution</strong></summary>

Assume 100 g: 69.9 g Fe, 30.1 g O.

$$\frac{69.9}{55.85} = 1.252 \ \text{mol Fe} \qquad \frac{30.1}{16.00} = 1.881 \ \text{mol O}$$

Divide by the smallest:

$$\text{Fe}: 1.00 \qquad \text{O}: \frac{1.881}{1.252} = 1.50$$

Don't round 1.50! Multiply both by 2: Fe = 2, O = 3.

**Answer: $\ce{Fe2O3}$** (rust).

</details>

### Problem 14

A hydrocarbon has empirical formula $\ce{CH}$ and a molar mass of 78.12 g/mol. Find its molecular formula.

<details>
<summary><strong>Solution</strong></summary>

Empirical formula mass: $12.01 + 1.01 = 13.02$ g/mol.

$$n = \frac{78.12}{13.02} = 6.00$$

Multiply subscripts by 6: $\ce{C6H6}$.

**Answer: $\ce{C6H6}$ — benzene.**

</details>

### Problem 15

(Stoichiometry capstone.) Potassium chlorate decomposes when heated: $\ce{2KClO3 ->[\Delta] 2KCl + 3O2}$. If 61.28 g of $\ce{KClO3}$ decomposes completely, how many grams of $\ce{O2}$ gas are produced?

<details>
<summary><strong>Solution</strong></summary>

$M_{\ce{KClO3}} = 39.10 + 35.45 + 3(16.00) = 122.55$ g/mol; $M_{\ce{O2}} = 32.00$ g/mol.

Full chain: grams $\ce{KClO3}$ → moles $\ce{KClO3}$ → moles $\ce{O2}$ (coefficient ratio) → grams $\ce{O2}$:

$$61.28 \ \cancel{\text{g}} \times \frac{1 \ \cancel{\text{mol} \ \ce{KClO3}}}{122.55 \ \cancel{\text{g}}} \times \frac{3 \ \cancel{\text{mol} \ \ce{O2}}}{2 \ \cancel{\text{mol} \ \ce{KClO3}}} \times \frac{32.00 \ \text{g}}{1 \ \cancel{\text{mol} \ \ce{O2}}}$$

$61.28 / 122.55 = 0.5000$ mol $\ce{KClO3}$ → $0.7500$ mol $\ce{O2}$ → $24.0$ g.

**Answer: 24.0 g of $\ce{O2}$.** You just did a full mass-to-mass stoichiometry problem — welcome to AP Unit 4, a few months early.

</details>

---

## Quick Reference

| Quantity | Symbol / Value | Meaning |
|---|---|---|
| Avogadro's number | $N_A = 6.022 \times 10^{23}$ /mol | Particles per mole; also the number of amu in 1 g |
| Mole definition | 12 g of $\ce{^{12}C}$ = 1 mol | Locks the amu scale to the gram scale |
| Molar mass | $M$ (g/mol) | Numerically equals atomic/formula mass in amu |
| Moles from mass | $n = \dfrac{m}{M}$ | On the AP reference sheet |
| Grams → moles | $\times \dfrac{1 \ \text{mol}}{M \ \text{g}}$ | First railroad car |
| Moles → particles | $\times \dfrac{6.022 \times 10^{23}}{1 \ \text{mol}}$ | Second railroad car |
| Element within compound | $\times \dfrac{\text{subscript mol element}}{1 \ \text{mol compound}}$ | Apply *before* Avogadro's number |
| Percent composition | $\dfrac{(\text{count})(M_{\text{element}})}{M_{\text{compound}}} \times 100\%$ | Percents must total 100% |
| Empirical formula | percent → grams → moles → smallest ratio | Clear .5 with ×2, .33 with ×3, .25 with ×4 |
| Molecular formula | $n = \dfrac{\text{molar mass}}{\text{empirical mass}}$, multiply subscripts by $n$ | e.g., $\ce{CH2O} \to \ce{C6H12O6}$ |
| Mole ratio (stoichiometry) | $\dfrac{\text{coef. of B mol}}{\text{coef. of A mol}}$ | From the balanced equation — full story in AP Unit 4 |

---

<div align="center">

[← Balancing Equations](/chemistry/0206-balancing-equations) | [Mass Spectrometry →](/chemistry/0301-mass-spectrometry)

</div>
