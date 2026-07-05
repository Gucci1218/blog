# Mass Spectrometry
<p class="article-date">July 4, 2026</p>

*Last weekend Dad and I finally hauled the giant coin jar to the Coinstar machine at Vons. You dump in years of mixed-up change, the machine rattles for a minute, and then — magic — it knows exactly what was in there: 212 pennies, 96 nickels, 54 dimes, 71 quarters. It never looks at the pictures on the coins. It sorts them by <strong>mass</strong>: a nickel is 5.00 g, a quarter is 5.67 g, a dime is only 2.27 g, and the machine drops each coin into the pile that matches its weight, then counts the piles. If it printed a bar chart — pile mass along the bottom, pile height showing how many — you could compute the average mass of "one coin from this jar," and honestly, you could probably tell whose jar it was. That machine is a mass spectrometer for money. A real mass spectrometer does the identical trick to a sample of atoms: sort them by mass, count how many land in each pile, and the weighted average of the piles tells you exactly which element you're holding. This is AP Unit 1, Topic 1.2 — the first place the College Board hands you a graph and asks you to read an element's identity straight off of it.*

---

## What You'll Learn
- Describe what a mass spectrometer does in four conceptual steps (vaporize → ionize → sort by mass → detect)
- Read a mass spectrum: identify what the x-axis (mass, in amu) and y-axis (relative abundance) each tell you
- Interpret each peak as one isotope and each peak height as that isotope's abundance
- Calculate average atomic mass from a spectrum with percent abundances
- Normalize relative peak heights into fractional abundances when the y-axis isn't in percent
- Identify an unknown element by matching your computed average to the periodic table
- Run the algebra in reverse: find a missing isotope mass or missing abundances from the average atomic mass
- Sketch a mass spectrum from a table of isotope data
- Explain why average atomic masses are almost never whole numbers — and why no single atom actually has the average mass

---

## Prerequisites
- [Atomic Structure Basics](/chemistry/0201-atomic-structure-basics) — isotopes and the average atomic mass calculation are the entire content of this topic; mass spectrometry is where that math meets real data
- [Graphing and Linearization](/chemistry/0105-graphing-linearization) — a mass spectrum is a graph, and reading axes carefully is the whole game

---

## The Core Concept

### Intuition First

Stay with the coin jar. The Coinstar machine gives you two pieces of information about every pile:

1. **Where the pile is** — which mass of coin it holds (2.27 g dimes, 2.50 g pennies, 5.00 g nickels, 5.67 g quarters)
2. **How tall the pile is** — how many coins of that mass showed up

Neither piece alone identifies the jar. Knowing the jar contains quarters tells you almost nothing; knowing it's "mostly one kind of coin" without knowing which kind tells you nothing either. But together — *which masses, in what proportions* — they pin the jar down completely. You can even compute one summary number: the average mass of a randomly grabbed coin. If pennies dominate the jar, the average sits near 2.5 g. If it's quarter-heavy (Dad's jar, because he never spends quarters), the average gets pulled up toward 5.67 g.

Now swap coins for atoms:

| Coin jar | Mass spectrometry |
|---|---|
| Coin denominations (penny, nickel, dime, quarter) | Isotopes of one element ($\ce{^{35}Cl}$, $\ce{^{37}Cl}$, ...) |
| Mass of each coin type | Mass of each isotope (in amu) |
| Height of each pile | Relative abundance of each isotope |
| Average mass of "one coin from this jar" | Average atomic mass (the number on the periodic table) |
| "This is definitely Dad's jar" | "This element is definitely chlorine" |

One important difference: the machine never weighs "an average coin," because no coin weighs the average. It weighs *individual* coins, each landing in its own exact pile. Same with atoms — every single chlorine atom is either 35 amu or 37 amu. The 35.45 on the periodic table is a bookkeeping number describing the whole jar, not any one coin in it.

### What a Mass Spectrometer Actually Does (4 Steps)

The AP exam will never ask you to build one — you just need the conceptual flow:

1. **Vaporize.** Turn the sample into a gas, so atoms fly one at a time instead of clumping. (Dump the coins loose into the machine — no coin rolls allowed.)
2. **Ionize.** Knock an electron off each atom so it becomes a $1+$ ion. Charged particles can be steered; neutral ones can't. (Give each coin a push onto the sorting track.)
3. **Deflect and sort by mass.** Send the ions through a field that bends their paths. Lighter ions bend more, heavier ions bend less, so ions of different masses land in different spots — one "pile" per isotope. (The sorting slots: each coin rolls until it drops into the slot matching its size and weight.)
4. **Detect and count.** A detector counts how many ions land at each spot and plots the result. (The machine counts each pile and prints the receipt.)

The printout is the **mass spectrum** — the bar chart of the atomic coin jar.

### Reading a Mass Spectrum

$$\text{x-axis: mass (amu)} \qquad \text{y-axis: relative abundance}$$

- **Each peak = one isotope.** A spectrum of magnesium shows three peaks (at 24, 25, 26 amu) because magnesium has three naturally occurring isotopes.
- **The x-position of a peak = that isotope's mass.** Technically the axis is *mass-to-charge ratio* ($m/z$), but since ionization makes $1+$ ions, $z = 1$ and $m/z$ is just the mass. AP questions assume this.
- **The height of a peak = how abundant that isotope is.** The y-axis might be labeled in percent (heights sum to 100), or as unitless "relative abundance" (heights are just ratios — often the tallest peak is set to 100). If the heights don't sum to 100, **you must normalize**: divide each height by the total of all heights to get fractional abundances.

### The One Formula

Everything in this topic is a single weighted average:

$$\text{average atomic mass} = \sum (\text{isotope mass}) \times (\text{fractional abundance})$$

Fractional abundance means the decimal form: 78.99% → 0.7899. The fractions must sum to 1 (abundances sum to 100%).

**Three sanity checks** worth doing on every problem:

1. The average must land **between the lightest and heaviest peaks**.
2. The average sits **closest to the tallest peak** — the majority coin pulls the average toward itself.
3. The abundances must **sum to 100%** (or the fractions to 1). If they don't, normalize.

---

## Worked Examples

### Example 1: Reading a Spectrum Cold

**Problem:** A mass spectrum of a pure element shows three peaks:

| Mass (amu) | Relative abundance (%) |
|---|---|
| 24 | 78.99 |
| 25 | 10.00 |
| 26 | 11.01 |

Without calculating anything, what does each peak represent, and what can you already say about this element?

**Solution:**

**Step 1:** Three peaks = three naturally occurring isotopes, with mass numbers 24, 25, and 26.

**Step 2:** The heights say roughly 79% of all atoms in the sample are the mass-24 isotope, 10% are mass-25, and 11% are mass-26.

**Step 3:** Sanity-check predictions: the average atomic mass must land between 24 and 26, and since the 24 peak towers over the others, the average will sit just above 24.

**Answer:** Three isotopes (masses 24, 25, 26 amu) with abundances 78.99%, 10.00%, 11.01%; the average atomic mass will be slightly greater than 24 amu.

### Example 2: Average Atomic Mass from Percent Abundances

**Problem:** Using the spectrum from Example 1, calculate the average atomic mass and identify the element.

**Solution:**

**Step 1:** Convert percents to fractions: 0.7899, 0.1000, 0.1101.

**Step 2:** Weight each mass by its fraction:

$$24 \times 0.7899 = 18.958$$
$$25 \times 0.1000 = 2.500$$
$$26 \times 0.1101 = 2.863$$

**Step 3:** Add:

$$18.958 + 2.500 + 2.863 = 24.32 \text{ amu}$$

**Step 4:** Scan the periodic table for an element with mass ≈ 24.32: magnesium (24.31 amu).

**Answer:** Average atomic mass ≈ **24.32 amu; the element is magnesium** ($\ce{^{24}Mg}$, $\ce{^{25}Mg}$, $\ce{^{26}Mg}$).

*(The tiny mismatch with the table's 24.31 comes from using whole-number masses; the true isotope masses are 23.985, 24.986, and 25.983 amu. Whole numbers are fine on the AP unless exact masses are given.)*

### Example 3: A Two-Peak Element

**Problem:** An element's spectrum shows peaks at 63 amu (69.15%) and 65 amu (30.85%). Identify the element.

**Solution:**

**Step 1:** $63 \times 0.6915 = 43.56$

**Step 2:** $65 \times 0.3085 = 20.05$

**Step 3:** $43.56 + 20.05 = 63.62$ amu.

**Step 4:** Check: 63.62 is between 63 and 65, closer to the taller 63 peak. ✓ The periodic table shows copper at 63.55 amu — the only element near this value.

**Answer:** **Copper** ($\ce{^{63}Cu}$ and $\ce{^{65}Cu}$), average ≈ 63.62 amu with integer masses (63.55 with exact masses).

### Example 4: When the Heights Aren't Percentages

**Problem:** A spectrum shows two peaks: one at 35 amu with height 3.0, and one at 37 amu with height 1.0 (unitless relative heights). Find the average atomic mass and identify the element.

**Solution:**

**Step 1:** The heights sum to $3.0 + 1.0 = 4.0$, not 100 — these are relative heights, so normalize.

**Step 2:** Fractional abundances:

$$\frac{3.0}{4.0} = 0.75 \qquad \frac{1.0}{4.0} = 0.25$$

**Step 3:** Weighted average:

$$35 \times 0.75 + 37 \times 0.25 = 26.25 + 9.25 = 35.5 \text{ amu}$$

**Answer:** **Chlorine** (35.45 amu on the table) — the classic 3 : 1 pile ratio of $\ce{^{35}Cl}$ to $\ce{^{37}Cl}$.

### Example 5: Identify the Element from Raw Heights

**Problem:** Peaks at 10 amu (height 5.0) and 11 amu (height 20.0). Which element is this?

**Solution:**

**Step 1:** Total height $= 5.0 + 20.0 = 25.0$.

**Step 2:** Fractions: $\dfrac{5.0}{25.0} = 0.20$ and $\dfrac{20.0}{25.0} = 0.80$.

**Step 3:** Average:

$$10 \times 0.20 + 11 \times 0.80 = 2.0 + 8.8 = 10.8 \text{ amu}$$

**Step 4:** Periodic table: boron is 10.81 amu.

**Answer:** **Boron** ($\ce{^{10}B}$ at 20%, $\ce{^{11}B}$ at 80%). Note the average (10.8) hugs the tall peak at 11 — sanity check passed.

### Example 6: Three Peaks, Tallest Set to 100

**Problem:** A spectrum's tallest peak is scaled to 100:

| Mass (amu) | Relative height |
|---|---|
| 28 | 100.0 |
| 29 | 5.06 |
| 30 | 3.36 |

Identify the element.

**Solution:**

**Step 1:** Total height $= 100.0 + 5.06 + 3.36 = 108.42$.

**Step 2:** Fractions: $\dfrac{100.0}{108.42} = 0.9223$, $\dfrac{5.06}{108.42} = 0.0467$, $\dfrac{3.36}{108.42} = 0.0310$.

**Step 3:** Weighted average:

$$28(0.9223) + 29(0.0467) + 30(0.0310) = 25.82 + 1.35 + 0.93 = 28.10 \text{ amu}$$

**Answer:** **Silicon** (28.09 amu) — isotopes $\ce{^{28}Si}$, $\ce{^{29}Si}$, $\ce{^{30}Si}$.

### Example 7: A Five-Peak Monster

**Problem:** An element shows five peaks: 90 amu (51.45%), 91 amu (11.22%), 92 amu (17.15%), 94 amu (17.38%), 96 amu (2.80%). Identify it.

**Solution:**

**Step 1:** Verify the abundances sum to 100: $51.45 + 11.22 + 17.15 + 17.38 + 2.80 = 100.00$. ✓ Already percentages — no normalizing needed.

**Step 2:** Weight and add:

$$90(0.5145) + 91(0.1122) + 92(0.1715) + 94(0.1738) + 96(0.0280)$$
$$= 46.31 + 10.21 + 15.78 + 16.34 + 2.69 = 91.33 \text{ amu}$$

**Step 3:** Periodic table: zirconium sits at 91.22 amu — the only element in that neighborhood. (Integer masses overshoot slightly; exact masses give 91.22.)

**Answer:** **Zirconium.** More piles, same recipe: mass × fraction, then add.

### Example 8: Reverse Problem — Find the Missing Isotope's Mass

**Problem:** Lithium's average atomic mass is 6.94 amu. It has two isotopes: $\ce{^{7}Li}$ (mass 7.016 amu, abundance 92.41%) and one other. Find the mass of the other isotope.

**Solution:**

**Step 1:** The other isotope's abundance: $100\% - 92.41\% = 7.59\%$, so its fraction is 0.0759.

**Step 2:** Set up the weighted average with the unknown mass $m$:

$$6.94 = (7.016)(0.9241) + m(0.0759)$$

**Step 3:** Compute the known piece: $(7.016)(0.9241) = 6.484$.

**Step 4:** Solve:

$$6.94 - 6.484 = 0.0759\,m \implies m = \frac{0.456}{0.0759} = 6.01 \text{ amu}$$

**Answer:** **6.01 amu — the isotope is $\ce{^{6}Li}$.** Sanity check: the average 6.94 sits between 6.01 and 7.016, snuggled up against the abundant heavy isotope. ✓

### Example 9: Reverse Problem — Find Both Abundances (Let x = Fraction)

**Problem:** Copper (average atomic mass 63.55 amu) has exactly two isotopes: $\ce{^{63}Cu}$ (62.93 amu) and $\ce{^{65}Cu}$ (64.93 amu). Find the percent abundance of each.

**Solution:**

**Step 1:** Let $x$ = fraction of $\ce{^{63}Cu}$. Then the fraction of $\ce{^{65}Cu}$ is $1 - x$ (two piles, fractions sum to 1).

**Step 2:** Write the weighted average:

$$62.93x + 64.93(1 - x) = 63.55$$

**Step 3:** Expand and collect:

$$62.93x + 64.93 - 64.93x = 63.55$$
$$-2.00x = 63.55 - 64.93 = -1.38$$

**Step 4:** Solve:

$$x = \frac{1.38}{2.00} = 0.690$$

**Answer:** **$\ce{^{63}Cu}$: 69.0%, $\ce{^{65}Cu}$: 31.0%.** Check: the average 63.55 is much closer to 62.93 than to 64.93, so the light isotope should dominate. ✓

### Example 10: Two-Isotope Algebra with Uglier Numbers

**Problem:** Gallium (average 69.72 amu) has isotopes $\ce{^{69}Ga}$ (68.926 amu) and $\ce{^{71}Ga}$ (70.925 amu). Find both percent abundances.

**Solution:**

**Step 1:** Let $x$ = fraction of $\ce{^{69}Ga}$:

$$68.926x + 70.925(1 - x) = 69.72$$

**Step 2:** Expand:

$$68.926x + 70.925 - 70.925x = 69.72$$
$$-1.999x = -1.205$$

**Step 3:** Solve (keep all digits until the end — rounding early wrecks these):

$$x = \frac{1.205}{1.999} = 0.6028$$

**Answer:** **$\ce{^{69}Ga}$: 60.3%, $\ce{^{71}Ga}$: 39.7%.** Notice the denominator is the *gap between the two isotope masses* — that's always what you divide by in a two-isotope problem.

### Example 11: Sketching a Spectrum from Data

**Problem:** Bromine has two isotopes: $\ce{^{79}Br}$ (50.69%) and $\ce{^{81}Br}$ (49.31%). Sketch its mass spectrum.

**Solution:**

**Step 1:** Two isotopes → two peaks, at x = 79 and x = 81 amu.

**Step 2:** Heights are the abundances: 50.69 and 49.31 — nearly equal, with 79 a hair taller.

**Step 3:** Draw:

```text
Relative
abundance (%)
  50 |   █           █
  40 |   █           █
  30 |   █           █
  20 |   █           █
  10 |   █           █
   0 +---+---+---+---+---
        79  80  81      mass (amu)
```

**Answer:** **Two nearly equal peaks at 79 and 81 amu, the 79 peak very slightly taller.** (This near-50/50 split is why bromine's table mass, 79.90, sits almost exactly halfway between the isotopes — an evenly mixed coin jar averages to the middle.)

### Example 12: The Classic Conceptual Trap

**Problem:** Chlorine's periodic-table mass is 35.45 amu. A student claims, "This means a typical chlorine atom has a mass of 35.45 amu." Explain what's wrong, and why the table value isn't a whole number.

**Solution:**

**Step 1:** Look at chlorine's actual spectrum: peaks at 35 and 37 only. **No atom ever lands at 35.45** — just like no coin in the jar weighs the jar's average of 3.87 g. Every individual chlorine atom is either $\ce{^{35}Cl}$ (≈35 amu) or $\ce{^{37}Cl}$ (≈37 amu).

**Step 2:** The 35.45 is a **weighted average across the natural mixture**: $35(0.75) + 37(0.25) = 35.5$. It describes a huge population, not any single atom.

**Step 3:** That's also why table masses aren't whole numbers: they're averages over isotopes with different whole-ish mass numbers, blended in uneven proportions. A whole-number-looking table mass (like fluorine's 19.00) just means one isotope utterly dominates — a jar that's essentially all nickels.

**Answer:** **35.45 amu is the abundance-weighted average of $\ce{^{35}Cl}$ and $\ce{^{37}Cl}$; no individual atom has that mass, and the mixing of isotopes is exactly why periodic-table masses are rarely whole numbers.**

### A One-Paragraph Preview: Molecules Get Spectra Too

Mass spectrometers don't only sort atoms — feed one a *molecular* sample and it sorts whole molecules by mass. A spectrum of $\ce{CO2}$ shows its main peak at 44 amu (the mass of the whole molecule), and heavier molecules show correspondingly heavier peaks; chemists use this to identify unknown compounds and even to spot isotope patterns *inside* molecules (a compound containing chlorine shows tell-tale twin peaks 2 amu apart, in that famous 3 : 1 ratio). That's beyond Topic 1.2 — for now, AP Unit 1 keeps the machine pointed at single elements — but it's the same coin-sorting idea scaled up from coins to whole rolls of coins.

---

## Common Mistakes

| The Mistake | Why It Happens | How to Avoid It |
|---|---|---|
| Using relative heights directly as percents | The y-axis said "relative abundance," so it *looks* percent-ish | Add up all heights first. If the total isn't 100, divide each height by the total before averaging |
| Taking a simple average of the peak masses (e.g., $\frac{35+37}{2} = 36$ for Cl) | Averages from math class are unweighted | Every mass must be multiplied by its abundance fraction — the tall pile counts more |
| Multiplying by the percent instead of the fraction ($35 \times 75$ instead of $35 \times 0.75$) | Skipped the percent→decimal conversion | If your "average" is 50× too big, you know exactly what happened |
| Swapping the axes | Reading fast under time pressure | x-axis = mass (amu), y-axis = abundance. The peak's *position* is what kind of atom; its *height* is how many |
| Believing the tallest peak equals the average atomic mass | The tallest peak is the "most typical" atom | The average is *pulled toward* the tallest peak but is a blend of all peaks |
| Expecting some atoms to have the average mass | The periodic table prints one number per element | No atom has the average mass — it's a population statistic, like "the average household has 2.5 people" |
| Rounding mid-calculation in reverse problems | The numbers get ugly | Carry all digits; in two-isotope algebra you divide by a small mass gap (~2 amu), which magnifies rounding errors |
| Abundances that don't sum to 100% | Copying numbers wrong, or a missing isotope | Always check the sum first — the AP loves hiding a third isotope whose abundance you must find by subtraction |

---

## AP Exam Tips

- **Multiple choice adores "which element does this spectrum represent?"** You get a spectrum with 2–3 peaks and four element choices. Fast path: estimate the weighted average (it lives between the peaks, near the tallest one) and match to the periodic table. With Cl-style 3 : 1 peaks at 35/37, you don't even need arithmetic — the answer is just above 35.
- **No calculator on the MC section**, so practice estimating: for boron's peaks at 10 (20%) and 11 (80%), think "$10.8$-ish" and move on. Exact decimals are for FRQs.
- **FRQs demand justification via the weighted average.** "Identify the element AND justify your answer" means: show the mass × fraction products, show the sum, and explicitly compare to the periodic table value. A bare element name earns the identification point but drops the justification point.
- **Watch the y-axis label like a hawk.** If heights are given as raw relative values (say, 100 and 32.5), the very first scored step is normalizing to fractions. Skipping it is the single most common point loss on this topic.
- **Know the conceptual traps cold:** why the table mass isn't a whole number, why no atom has the average mass, and why the average sits closest to the most abundant isotope. These appear as one-point "explain" parts and as MC distractors.
- **The x-axis may be labeled $m/z$** (mass-to-charge ratio). AP questions use $1+$ ions, so $z = 1$ and you can read it as plain mass in amu.
- **Sanity checks are free points insurance:** average between lightest and heaviest peak, closest to tallest peak, abundances summing to 100%. If your answer violates any of these, you made an arithmetic slip — fix it before moving on.

---

## Practice Problems

### Problem 1
Neon's mass spectrum shows peaks at 20 amu (90.48%), 21 amu (0.27%), and 22 amu (9.25%). Calculate the average atomic mass and confirm the element's identity.

<details>
<summary><strong>Solution</strong></summary>

Abundances sum to $90.48 + 0.27 + 9.25 = 100.00$ ✓ — already percentages.

$$20(0.9048) + 21(0.0027) + 22(0.0925)$$
$$= 18.096 + 0.057 + 2.035 = 20.19 \text{ amu}$$

The periodic table lists neon at 20.18 amu. ✓

**Average atomic mass ≈ 20.19 amu — neon.**

</details>

### Problem 2
A spectrum of a pure element shows peaks at 24, 25, and 26 amu with relative heights 7.10, 0.90, and 1.00 (not percentages). Identify the element.

<details>
<summary><strong>Solution</strong></summary>

Total height: $7.10 + 0.90 + 1.00 = 9.00$.

Fractions: $\frac{7.10}{9.00} = 0.789$, $\frac{0.90}{9.00} = 0.100$, $\frac{1.00}{9.00} = 0.111$.

$$24(0.789) + 25(0.100) + 26(0.111) = 18.94 + 2.50 + 2.89 = 24.33 \text{ amu}$$

Periodic table: magnesium, 24.31 amu.

**Magnesium** ($\ce{^{24}Mg}$, $\ce{^{25}Mg}$, $\ce{^{26}Mg}$).

</details>

### Problem 3
Two peaks: 6 amu with height 1.0, and 7 amu with height 12.2. Find the average atomic mass and identify the element.

<details>
<summary><strong>Solution</strong></summary>

Total height: $1.0 + 12.2 = 13.2$.

Fractions: $\frac{1.0}{13.2} = 0.0758$ and $\frac{12.2}{13.2} = 0.9242$.

$$6(0.0758) + 7(0.9242) = 0.455 + 6.469 = 6.92 \text{ amu}$$

Periodic table: lithium, 6.94 amu.

**Lithium** ($\ce{^{6}Li}$ and $\ce{^{7}Li}$).

</details>

### Problem 4
An element shows exactly two peaks, at 63 and 65 amu, with the 63 peak roughly 2.2 times taller. Without a calculator, decide which of these elements it is: Ni (58.69), Cu (63.55), Zn (65.38), Ga (69.72). Justify briefly.

<details>
<summary><strong>Solution</strong></summary>

The average must land between 63 and 65, and closer to 63 (the taller peak). A quick estimate: fractions are roughly $\frac{2.2}{3.2} \approx 0.69$ and $0.31$, so the average is about $63 + 0.31(2) \approx 63.6$.

Only copper (63.55) is between 63 and 65.

**Copper** — the average of any 63/65 mixture must lie between 63 and 65 amu, and 63.55 is the only listed value in that window.

</details>

### Problem 5
Silicon's isotopes: $\ce{^{28}Si}$ (27.977 amu, 92.23%), $\ce{^{29}Si}$ (28.976 amu, 4.68%), and $\ce{^{30}Si}$ (29.974 amu, unknown abundance). Find the abundance of $\ce{^{30}Si}$ and then calculate silicon's average atomic mass with exact masses.

<details>
<summary><strong>Solution</strong></summary>

Abundances sum to 100%:

$$100 - 92.23 - 4.68 = 3.09\% \text{ for } \ce{^{30}Si}$$

Weighted average:

$$27.977(0.9223) + 28.976(0.0468) + 29.974(0.0309)$$
$$= 25.803 + 1.356 + 0.926 = 28.09 \text{ amu}$$

**$\ce{^{30}Si}$ abundance = 3.09%; average atomic mass = 28.09 amu** (matches the periodic table). ✓

</details>

### Problem 6
Titanium shows five peaks: 46 amu (8.25%), 47 amu (7.44%), 48 amu (73.72%), 49 amu (5.41%), 50 amu (5.18%). Calculate the average atomic mass.

<details>
<summary><strong>Solution</strong></summary>

Check the sum: $8.25 + 7.44 + 73.72 + 5.41 + 5.18 = 100.00$ ✓

$$46(0.0825) + 47(0.0744) + 48(0.7372) + 49(0.0541) + 50(0.0518)$$
$$= 3.795 + 3.497 + 35.386 + 2.651 + 2.590 = 47.92 \text{ amu}$$

Sanity check: between 46 and 50, hugging the dominant 48 peak. ✓ (Periodic table: 47.87 — integer masses overshoot slightly.)

**Average atomic mass ≈ 47.92 amu (titanium).**

</details>

### Problem 7
Silver's average atomic mass is 107.87 amu. One isotope is $\ce{^{107}Ag}$ (106.905 amu, 51.84% abundant). Silver has exactly two isotopes. Find the mass of the second isotope and identify it.

<details>
<summary><strong>Solution</strong></summary>

Second isotope's fraction: $1 - 0.5184 = 0.4816$.

$$107.87 = (106.905)(0.5184) + m(0.4816)$$
$$107.87 = 55.420 + 0.4816\,m$$
$$m = \frac{107.87 - 55.420}{0.4816} = \frac{52.450}{0.4816} = 108.9 \text{ amu}$$

**The second isotope has mass ≈ 108.9 amu — it is $\ce{^{109}Ag}$.**

</details>

### Problem 8
Bromine's average atomic mass is 79.90 amu, and its two isotopes have masses 78.918 amu and 80.916 amu. Find the percent abundance of each isotope.

<details>
<summary><strong>Solution</strong></summary>

Let $x$ = fraction of $\ce{^{79}Br}$:

$$78.918x + 80.916(1 - x) = 79.90$$
$$78.918x + 80.916 - 80.916x = 79.90$$
$$-1.998x = -1.016$$
$$x = \frac{1.016}{1.998} = 0.5085$$

**$\ce{^{79}Br}$: 50.9%, $\ce{^{81}Br}$: 49.1%.** The near-even split is why bromine's average sits almost dead center between the isotope masses.

</details>

### Problem 9
Rubidium has isotopes $\ce{^{85}Rb}$ (72.17%) and $\ce{^{87}Rb}$ (27.83%). Sketch its mass spectrum (ASCII bars or a table is fine), then compute the average atomic mass using integer masses.

<details>
<summary><strong>Solution</strong></summary>

Two peaks, at 85 and 87 amu, with the 85 peak about 2.6 times taller:

```text
Relative
abundance (%)
  70 |   █
  60 |   █
  50 |   █
  40 |   █
  30 |   █           █
  20 |   █           █
  10 |   █           █
   0 +---+---+---+---+---
        85  86  87      mass (amu)
```

Average:

$$85(0.7217) + 87(0.2783) = 61.34 + 24.21 = 85.56 \text{ amu}$$

**Two peaks (85 tall, 87 short, ratio ≈ 2.6 : 1); average atomic mass ≈ 85.56 amu** (table: 85.47).

</details>

### Problem 10
Antimony's average atomic mass is 121.76 amu, with isotopes $\ce{^{121}Sb}$ and $\ce{^{123}Sb}$ (use integer masses). What ratio of peak heights (121-peak : 123-peak) would its mass spectrum show?

<details>
<summary><strong>Solution</strong></summary>

Let $x$ = fraction of $\ce{^{121}Sb}$:

$$121x + 123(1 - x) = 121.76$$
$$123 - 2x = 121.76$$
$$x = \frac{1.24}{2} = 0.62$$

So the abundances are 62% and 38%, and peak heights are in the same ratio as abundances:

$$\frac{62}{38} \approx 1.6$$

**The 121 peak is about 1.6 times taller than the 123 peak (62 : 38).**

</details>

### Problem 11
A student looks at chlorine's spectrum (peaks at 35 and 37 amu) and reports: "The spectrum shows that most chlorine atoms have a mass of 35.45 amu, with some variation." Identify **two** errors in this statement.

<details>
<summary><strong>Solution</strong></summary>

**Error 1:** No chlorine atom has a mass of 35.45 amu. The spectrum shows atoms only at 35 and 37 amu; 35.45 is the abundance-weighted *average* of the whole sample, a population statistic that no individual atom possesses.

**Error 2:** "Some variation" misrepresents isotopes. Atoms don't vary continuously around an average — they come in exactly two discrete masses ($\ce{^{35}Cl}$ and $\ce{^{37}Cl}$), determined by neutron count. The correct statement: about 76% of atoms are $\ce{^{35}Cl}$ and 24% are $\ce{^{37}Cl}$, giving a weighted average of 35.45 amu.

**No atom has the average mass, and isotope masses are discrete values (35 or 37), not a spread around 35.45.**

</details>

### Problem 12
Explain why fluorine's periodic-table mass (19.00 amu) looks like a whole number while chlorine's (35.45 amu) does not, in terms of what their mass spectra must look like.

<details>
<summary><strong>Solution</strong></summary>

The table mass is a weighted average over isotopes. Chlorine's spectrum has two substantial peaks (35 at ~76%, 37 at ~24%), so the average is dragged to a decidedly non-whole 35.45 — a jar of mixed coins averages to an in-between value.

Fluorine's spectrum has essentially **one peak**: $\ce{^{19}F}$ is 100% of natural fluorine. A one-isotope element's "average" is just that isotope's mass, so it lands almost exactly on a whole-ish number.

**Fluorine is monoisotopic (single peak at 19), so its average equals its only isotope's mass; chlorine's two abundant isotopes blend to a clearly fractional average.**

</details>

### Problem 13
(FRQ-style) The mass spectrum of element X shows two peaks: 63 amu at 69.2% and 65 amu at 30.8%.
**(a)** Calculate the average atomic mass of X.
**(b)** Identify X, justifying your answer with the calculation from (a).
**(c)** A single atom of X is selected at random. What are the possible masses of this atom?

<details>
<summary><strong>Solution</strong></summary>

**(a)**

$$63(0.692) + 65(0.308) = 43.60 + 20.02 = 63.62 \text{ amu}$$

**(b)** The computed average, 63.62 amu, matches copper's periodic-table value (63.55 amu) far better than any neighboring element (Ni 58.69, Zn 65.38). Because the abundance-weighted average of the spectrum's peaks reproduces copper's listed atomic mass, **X is copper**. (On the real FRQ, showing the products, the sum, and the comparison to the table earns the justification point.)

**(c)** The atom is either $\ce{^{63}Cu}$ (≈63 amu, probability 69.2%) or $\ce{^{65}Cu}$ (≈65 amu, probability 30.8%). **It can never have the average mass of 63.62 amu** — only the two discrete isotope masses are possible.

</details>

### Problem 14
Europium has two isotopes: $\ce{^{151}Eu}$ (150.920 amu) and $\ce{^{153}Eu}$ (152.921 amu). Its average atomic mass is 151.96 amu. Find both percent abundances, keeping all digits until the final step.

<details>
<summary><strong>Solution</strong></summary>

Let $x$ = fraction of $\ce{^{151}Eu}$:

$$150.920x + 152.921(1 - x) = 151.96$$
$$150.920x + 152.921 - 152.921x = 151.96$$
$$-2.001x = 151.96 - 152.921 = -0.961$$
$$x = \frac{0.961}{2.001} = 0.4803$$

**$\ce{^{151}Eu}$: 48.0%, $\ce{^{153}Eu}$: 52.0%.** Check: the average (151.96) is just barely closer to 153 than to 151, consistent with the heavy isotope having the slight edge. ✓

</details>

### Problem 15
Describe, in the four conceptual steps, what happens to a sample of magnesium metal from the moment it enters a mass spectrometer to the moment the spectrum prints — and state what the instrument's output would show for natural magnesium.

<details>
<summary><strong>Solution</strong></summary>

1. **Vaporize:** the magnesium is heated into a gas so individual atoms travel separately.
2. **Ionize:** each atom loses one electron, becoming $\ce{Mg+}$ — charged, so a field can steer it.
3. **Deflect/sort by mass:** the ions pass through a field that bends light ions more than heavy ones; $\ce{^{24}Mg+}$, $\ce{^{25}Mg+}$, and $\ce{^{26}Mg+}$ follow three different paths.
4. **Detect:** a detector counts the ions arriving at each landing spot and plots counts vs. mass.

**Output: three peaks at 24, 25, and 26 amu with heights ≈ 79%, 10%, and 11% — three isotope "piles" whose weighted average, 24.31 amu, is magnesium's periodic-table mass.**

</details>

---

## Quick Reference

| Concept | The Essentials |
|---|---|
| The 4 machine steps | Vaporize → ionize ($1+$) → deflect/sort by mass → detect and count |
| x-axis | Mass in amu (technically $m/z$, but $z = 1$ on the AP) |
| y-axis | Relative abundance — percent, or raw heights that need normalizing |
| Each peak | One isotope; position = mass, height = abundance |
| The formula | $\text{avg mass} = \sum (\text{mass} \times \text{fractional abundance})$ |
| Normalizing heights | fraction = (this peak's height) ÷ (sum of all heights) |
| Reverse (missing mass) | avg = (known mass)(known fraction) + $m$(remaining fraction); solve for $m$ |
| Reverse (two abundances) | Let $x$ = one fraction, other = $1-x$; you'll divide by the isotope mass gap |
| Sanity checks | Average between lightest/heaviest peak; nearest the tallest peak; abundances sum to 100% |
| The trap | No atom has the average mass — it's a population statistic (nobody's coin weighs the jar average) |

---

<div align="center">

[← The Mole](/chemistry/0207-the-mole) | [Composition of Mixtures →](/chemistry/0302-composition-of-mixtures)

</div>
