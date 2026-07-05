# Titration
<p class="article-date">July 5, 2026</p>

*Last weekend I was making a big pot of soup and doing the thing everyone does with hot sauce: one drop, stir, taste. One more drop, stir, taste. For a long, boring stretch nothing happens — the soup just tastes like soup, then slightly warmer, then a little warmer still. And then out of nowhere ONE single drop tips it from "wow, perfect" to "okay that's too spicy," and there's no taking it back. That drop-by-drop, taste-as-you-go process — creeping up on an exact point and detecting the instant you hit it — is literally a lab technique called **titration**. Instead of hot sauce you add a solution whose concentration you know exactly, drop by drop, into a solution you're trying to measure, and instead of your tongue you watch an indicator that suddenly flips color the moment you've added just enough. This is AP Unit 4, Topic 4.6, and it's the single most testable lab on the whole exam — a titration FRQ is basically guaranteed, so the sooner the soup makes it click, the better.*

---

## What You'll Learn

- Explain what a **titration** is and why reacting a known solution with an unknown lets you measure the unknown
- Identify the equipment and roles: the **buret**, the **flask**, the **titrant** (known), the **analyte** (unknown), and the **indicator**
- Distinguish the **equivalence point** (the ideal stoichiometric point) from the **endpoint** (the observed color flip) and know why the AP exam cares about the difference
- Run the core calculation engine: convert volume to moles with $M \times V$, apply the **mole ratio**, then solve for the unknown
- Find an unknown **molarity** from titration data for both 1:1 and non-1:1 reactions (the $\ce{H2SO4}$/$\ce{NaOH}$ trap)
- Find **grams**, **percent purity**, or **molar mass** of an analyte from a titration
- Read a real **buret** (initial minus final volume) and report answers with correct **significant figures**
- Explain what **standardization** means and why you'd titrate to pin down a titrant's exact concentration

---

## Prerequisites

- [Stoichiometry](/chemistry/0603-stoichiometry) — a titration is a stoichiometry problem in a lab coat; the **mole ratio** from the balanced equation is the engine of every calculation here
- [Solutions and Concentration](/chemistry/0506-solutions-and-concentration) — you must be fluent in **molarity** ($M = \frac{\text{mol}}{\text{L}}$) and comfortable rearranging it to $\text{mol} = M \times V$; the dilution logic of $M_1V_1 = M_2V_2$ lives next door
- [Net Ionic Equations](/chemistry/0601-net-ionic-equations) — the reaction that actually happens in the flask (like $\ce{H+ + OH- -> H2O}$) is a net ionic equation, and it's where the mole ratio comes from

---

## The Core Concept

### Intuition First

Back to the soup. Let's name every part of what you were doing, because each one maps exactly onto a titration:

| Soup kitchen | Titration term | What it is |
|---|---|---|
| the hot sauce, whose exact heat you know | **titrant** | the solution of **known** concentration you add from the buret |
| the pot of soup you're seasoning | **analyte** | the solution of **unknown** amount/concentration you're measuring |
| the exact perfect-heat moment | **equivalence point** | when you've added *stoichiometrically exactly enough* titrant to react with all the analyte |
| the taste flip you actually notice | **endpoint** | the observable signal (color change) that tells you to STOP |
| one drop too far → too spicy | **titration error** | overshooting the equivalence point |

Here's why the technique works at all. You know the hot sauce's heat *per drop* exactly. So if you carefully count how many drops it took to reach the flip, you can work backward and figure out how much soup — how much "unknown" — was there to begin with. **Known concentration + measured volume = a way to count invisible particles.** That's the whole trick. You can't see moles of acid floating in a beaker, but you *can* read a volume off a buret, and volume times concentration gives you moles.

And notice the cruel part of the soup: for a long time, each drop barely changes anything, and then a single drop tips everything at once. Titrations do the same — you can dump in most of the titrant with nothing dramatic happening, and then right near the end **one drop** swings the indicator from clear to pink. That sensitivity is a feature: it's what makes the stopping point sharp enough to measure precisely. It's also why "one drop past perfect" is a real source of error.

### The Setup, Described Simply

Picture the bench:

- A tall, skinny glass tube marked with fine volume lines and a stopcock (a little valve) at the bottom — that's the **buret**. It holds the **titrant** and lets you add it literally drop by drop.
- A flask (usually an Erlenmeyer, the cone-shaped one) sitting underneath, holding a measured amount of the **analyte**.
- A few drops of an **indicator** stirred into the flask — a dye that is one color in the starting conditions and a different color once the reaction is complete.

You record the buret reading, open the stopcock, and add titrant slowly while swirling. Near the end you slow to one drop at a time. The instant the indicator changes color and *stays* changed, you close the stopcock and read the buret again. The **volume delivered** is your key measurement.

### Equivalence Point vs. Endpoint (the distinction AP loves)

These two are almost the same, and that "almost" is exactly what gets tested.

- The **equivalence point** is the *ideal, theoretical* moment: the exact instant when moles of titrant, scaled by the mole ratio, precisely equal moles of analyte. Nothing about it is visible — it's a stoichiometric fact.
- The **endpoint** is what you actually *see*: the indicator flipping color. You choose an indicator whose flip happens *as close as possible* to the equivalence point, so the endpoint is your best real-world estimate of it.

In the soup: the equivalence point is the true "perfectly seasoned" moment; the endpoint is the drop where *you notice* it's perfect. A well-chosen indicator makes those two line up so tightly that we treat the endpoint volume as the equivalence volume. If they don't line up — bad indicator, or one drop too far — you get **titration error**.

**Indicators, in one paragraph:** an indicator is a dye that changes color over a specific range, and for acid–base titrations that range is a range of **pH**. Phenolphthalein, the classic, is colorless in acid and turns pink in base, so it "announces" when a solution has just become basic. You add only a couple of drops so the indicator itself doesn't consume meaningful titrant. *Why* a particular indicator matches a particular titration — and the full shape of the pH-vs-volume curve — is a deep topic we'll unpack in **Unit 8 (Acids and Bases)**; for now, just trust that the color flip marks "enough." → *(forward link: Unit 8 titration curves)*

### The Calculation Engine

Every titration calculation is the same four-move chain. Memorize the shape once and you can do all of them:

$$\text{Volume of titrant} \;\xrightarrow{\;\times\,M\;}\; \text{mol titrant} \;\xrightarrow{\;\text{mole ratio}\;}\; \text{mol analyte} \;\xrightarrow{\;\div\,V \text{ or } \div\,\mathcal{M}\;}\; \text{answer}$$

Written as the two workhorse equations:

$$\text{mol} = M \times V \qquad\qquad \text{mol analyte} = \text{mol titrant} \times \frac{\text{coeff. analyte}}{\text{coeff. titrant}}$$

The general **workflow**:

1. **Balance** the reaction (get the mole ratio — this is the step people skip and regret).
2. **Read the volume** of titrant delivered at the endpoint (final − initial buret reading).
3. **mol titrant** $= M_{\text{titrant}} \times V_{\text{titrant}}$ (volume in **liters**).
4. **mol analyte** $=$ mol titrant $\times$ the mole ratio (analyte over titrant).
5. **Finish**, depending on what's asked:
   - want the analyte's **molarity**? → divide mol analyte by the analyte's volume in liters.
   - want **grams / identity / purity**? → multiply mol analyte by its molar mass.

That's it. Same skeleton every time. The only thing that changes is which end of the chain the question hands you and which end it asks for.

---

## Worked Examples

### Example 1: The Simplest 1:1 Acid–Base Titration

**Problem:** You titrate $25.00 \text{ mL}$ of $\ce{HCl}$ of unknown concentration with $0.100 \text{ M } \ce{NaOH}$. It takes $32.15 \text{ mL}$ of the $\ce{NaOH}$ to reach the endpoint. What is the molarity of the $\ce{HCl}$?

**Solution:**

**Step 1 — Balance & get the ratio.**
$$\ce{HCl + NaOH -> NaCl + H2O}$$
The ratio is **1 mol $\ce{NaOH}$ : 1 mol $\ce{HCl}$**.

**Step 2 — mol of titrant ($\ce{NaOH}$).** Convert $32.15 \text{ mL} = 0.03215 \text{ L}$.
$$\text{mol }\ce{NaOH} = 0.100 \text{ M} \times 0.03215 \text{ L} = 3.215 \times 10^{-3} \text{ mol}$$

**Step 3 — mol of analyte ($\ce{HCl}$).** Ratio is 1:1, so
$$\text{mol }\ce{HCl} = 3.215 \times 10^{-3} \text{ mol} \times \frac{1}{1} = 3.215 \times 10^{-3} \text{ mol}$$

**Step 4 — divide by analyte volume** ($25.00 \text{ mL} = 0.02500 \text{ L}$):
$$M_{\ce{HCl}} = \frac{3.215 \times 10^{-3} \text{ mol}}{0.02500 \text{ L}} = 0.1286 \text{ M}$$

**Answer:** $M_{\ce{HCl}} = 0.129 \text{ M}$ (3 sig figs).

### Example 2: The Non-1:1 Trap ($\ce{H2SO4}$ + $\ce{NaOH}$)

**Problem:** It takes $40.00 \text{ mL}$ of $0.150 \text{ M } \ce{NaOH}$ to neutralize $20.00 \text{ mL}$ of sulfuric acid, $\ce{H2SO4}$. Find the molarity of the $\ce{H2SO4}$.

**Solution:**

**Step 1 — Balance.** Sulfuric acid has **two** acidic hydrogens:
$$\ce{H2SO4 + 2NaOH -> Na2SO4 + 2H2O}$$
The ratio is **2 mol $\ce{NaOH}$ : 1 mol $\ce{H2SO4}$** — this is the whole point of the problem.

**Step 2 — mol $\ce{NaOH}$.**
$$0.150 \text{ M} \times 0.04000 \text{ L} = 6.00 \times 10^{-3} \text{ mol }\ce{NaOH}$$

**Step 3 — apply the ratio.** For every 2 $\ce{NaOH}$ we consume 1 $\ce{H2SO4}$, so *halve* it:
$$\text{mol }\ce{H2SO4} = 6.00 \times 10^{-3} \times \frac{1 \text{ mol }\ce{H2SO4}}{2 \text{ mol }\ce{NaOH}} = 3.00 \times 10^{-3} \text{ mol}$$

**Step 4 — divide by analyte volume** ($0.02000 \text{ L}$):
$$M_{\ce{H2SO4}} = \frac{3.00 \times 10^{-3} \text{ mol}}{0.02000 \text{ L}} = 0.150 \text{ M}$$

**Answer:** $M_{\ce{H2SO4}} = 0.150 \text{ M}$. (If you had forgotten the ratio and used 1:1, you'd have gotten $0.300 \text{ M}$ — exactly double, and exactly the wrong answer the exam is baiting you toward.)

### Example 3: Finding Grams of Analyte

**Problem:** A sample of solid $\ce{KOH}$ is dissolved in water and titrated with $0.250 \text{ M } \ce{HCl}$. Reaching the endpoint takes $28.60 \text{ mL}$ of the acid. How many grams of $\ce{KOH}$ were in the sample?

**Solution:**

**Step 1 — Balance.** $\ce{HCl + KOH -> KCl + H2O}$, ratio **1:1**.

**Step 2 — mol $\ce{HCl}$.** $0.250 \text{ M} \times 0.02860 \text{ L} = 7.15 \times 10^{-3} \text{ mol}$.

**Step 3 — mol $\ce{KOH}$.** Ratio 1:1, so $7.15 \times 10^{-3} \text{ mol}$.

**Step 4 — convert to grams.** Molar mass of $\ce{KOH} = 39.10 + 16.00 + 1.01 = 56.11 \text{ g/mol}$.
$$7.15 \times 10^{-3} \text{ mol} \times 56.11 \text{ g/mol} = 0.401 \text{ g}$$

**Answer:** $0.401 \text{ g of } \ce{KOH}$.

### Example 4: Percent Purity of an Impure Sample

**Problem:** A $0.500 \text{ g}$ sample of impure oxalic acid, $\ce{H2C2O4}$ (a diprotic acid, molar mass $90.04 \text{ g/mol}$), is titrated with $0.200 \text{ M } \ce{NaOH}$. It takes $48.00 \text{ mL}$ to reach the endpoint. What is the percent purity of the sample (assume only the oxalic acid reacts)?

**Solution:**

**Step 1 — Balance.** Diprotic acid → 2 $\ce{OH-}$ per acid:
$$\ce{H2C2O4 + 2NaOH -> Na2C2O4 + 2H2O}$$
Ratio **2 $\ce{NaOH}$ : 1 $\ce{H2C2O4}$**.

**Step 2 — mol $\ce{NaOH}$.** $0.200 \text{ M} \times 0.04800 \text{ L} = 9.60 \times 10^{-3} \text{ mol}$.

**Step 3 — mol $\ce{H2C2O4}$.** Halve it: $9.60 \times 10^{-3} \times \frac{1}{2} = 4.80 \times 10^{-3} \text{ mol}$.

**Step 4 — grams of pure acid.** $4.80 \times 10^{-3} \text{ mol} \times 90.04 \text{ g/mol} = 0.432 \text{ g}$.

**Step 5 — percent purity.**
$$\%\text{ purity} = \frac{0.432 \text{ g pure acid}}{0.500 \text{ g sample}} \times 100\% = 86.4\%$$

**Answer:** the sample is **86.4% oxalic acid**.

### Example 5: Finding the Molar Mass of an Unknown Acid

**Problem:** A $0.612 \text{ g}$ sample of a pure, **monoprotic** solid acid (call it $\ce{HA}$) is dissolved in water and titrated with $0.150 \text{ M } \ce{NaOH}$. The endpoint is reached after $34.00 \text{ mL}$. What is the molar mass of the acid?

**Solution:**

**Step 1 — Balance.** Monoprotic: $\ce{HA + NaOH -> NaA + H2O}$, ratio **1:1**.

**Step 2 — mol $\ce{NaOH}$.** $0.150 \text{ M} \times 0.03400 \text{ L} = 5.10 \times 10^{-3} \text{ mol}$.

**Step 3 — mol $\ce{HA}$.** Ratio 1:1 → $5.10 \times 10^{-3} \text{ mol}$ of acid.

**Step 4 — molar mass** $= \dfrac{\text{grams}}{\text{moles}}$:
$$\mathcal{M} = \frac{0.612 \text{ g}}{5.10 \times 10^{-3} \text{ mol}} = 120. \text{ g/mol}$$

**Answer:** $\mathcal{M} \approx 120 \text{ g/mol}$. (This is how you *identify* an unknown — match that molar mass to a candidate, like benzoic acid at $122 \text{ g/mol}$.)

### Example 6: Solving for Titrant Volume Instead

**Problem:** How many milliliters of $0.500 \text{ M } \ce{HCl}$ are needed to completely neutralize $30.00 \text{ mL}$ of $0.200 \text{ M } \ce{Ba(OH)2}$?

**Solution:**

**Step 1 — Balance.** Barium hydroxide releases 2 $\ce{OH-}$:
$$\ce{2HCl + Ba(OH)2 -> BaCl2 + 2H2O}$$
Ratio **2 $\ce{HCl}$ : 1 $\ce{Ba(OH)2}$**.

**Step 2 — mol $\ce{Ba(OH)2}$.** $0.200 \text{ M} \times 0.03000 \text{ L} = 6.00 \times 10^{-3} \text{ mol}$.

**Step 3 — mol $\ce{HCl}$ needed.** This time we scale *up* (2 acid per base): $6.00 \times 10^{-3} \times \frac{2}{1} = 1.20 \times 10^{-2} \text{ mol}$.

**Step 4 — solve for volume** from $V = \frac{\text{mol}}{M}$:
$$V = \frac{1.20 \times 10^{-2} \text{ mol}}{0.500 \text{ M}} = 0.0240 \text{ L} = 24.0 \text{ mL}$$

**Answer:** $24.0 \text{ mL of } \ce{HCl}$.

### Example 7: The Shortcut Formula (and when it's safe)

**Problem:** $\ce{HNO3}$ and $\ce{NaOH}$ react 1:1. It takes $18.75 \text{ mL}$ of $0.220 \text{ M } \ce{NaOH}$ to titrate $25.00 \text{ mL}$ of $\ce{HNO3}$. Use the 1:1 shortcut to find $M_{\ce{HNO3}}$.

**Solution:** For a strictly **1:1** reaction, mol titrant = mol analyte, so $M_aV_a = M_bV_b$ works directly:
$$M_a V_a = M_b V_b \;\Rightarrow\; M_{\ce{HNO3}} = \frac{M_b V_b}{V_a} = \frac{(0.220)(18.75)}{25.00} = 0.165 \text{ M}$$
(Volumes can stay in mL here because they appear on both sides and cancel.)

**Answer:** $0.165 \text{ M}$.

> **Warning:** $M_aV_a = M_bV_b$ **only** works when the ratio is 1:1. For $\ce{H2SO4}$ + $\ce{NaOH}$ or anything non-1:1, you must use the full mole-ratio chain (Example 2). When in doubt, don't use the shortcut — the chain never lies.

### Example 8: A Full Lab-Style FRQ (buret readings + sig figs)

**Problem:** A student standardizes an $\ce{NaOH}$ solution against $\ce{HCl}$. She pipets $25.00 \text{ mL}$ of $0.1050 \text{ M } \ce{HCl}$ into a flask with 2 drops of phenolphthalein. Her buret readings for the $\ce{NaOH}$:

- Initial reading: $1.24 \text{ mL}$
- Final reading (first faint pink that lasts 30 s): $27.68 \text{ mL}$

Find the exact concentration of the $\ce{NaOH}$.

**Solution:**

**Step 1 — Volume delivered.** Always **final − initial**:
$$V_{\ce{NaOH}} = 27.68 - 1.24 = 26.44 \text{ mL} = 0.02644 \text{ L}$$
(Both readings have 2 decimal places, so the difference keeps 2 decimals — see [Significant Figures](/chemistry/0102-significant-figures).)

**Step 2 — mol $\ce{HCl}$ (the known analyte here).**
$$0.1050 \text{ M} \times 0.02500 \text{ L} = 2.625 \times 10^{-3} \text{ mol}$$

**Step 3 — mol $\ce{NaOH}$.** $\ce{HCl + NaOH -> NaCl + H2O}$, ratio 1:1 → $2.625 \times 10^{-3} \text{ mol}$.

**Step 4 — molarity of $\ce{NaOH}$.**
$$M_{\ce{NaOH}} = \frac{2.625 \times 10^{-3} \text{ mol}}{0.02644 \text{ L}} = 0.09928 \text{ M}$$

**Answer:** $M_{\ce{NaOH}} = 0.09928 \text{ M}$, or $9.928 \times 10^{-2} \text{ M}$ (4 sig figs, matching the data). Notice this problem ran the chain "backward" — the *analyte* was the known one and we solved for the *titrant's* concentration. That's exactly what **standardization** is (next section).

### Example 9: A Light Back-Titration

**Problem (concept + numbers):** A chunk of solid $\ce{CaCO3}$ (limestone, $100.09 \text{ g/mol}$) is too slow to titrate directly, so a chemist dissolves it in **excess** $\ce{HCl}$, then titrates the **leftover** acid with base.

The reaction: $\ce{CaCO3 + 2HCl -> CaCl2 + H2O + CO2}$.

She adds $50.00 \text{ mL}$ of $0.500 \text{ M } \ce{HCl}$ ($= 2.50 \times 10^{-2} \text{ mol}$ total acid). After the limestone reacts, the excess $\ce{HCl}$ requires $16.00 \text{ mL}$ of $0.250 \text{ M } \ce{NaOH}$ to neutralize. How many grams of $\ce{CaCO3}$ were there?

**Solution:**

**Step 1 — leftover acid.** mol $\ce{NaOH} = 0.250 \times 0.01600 = 4.00 \times 10^{-3} \text{ mol}$; ratio 1:1 with $\ce{HCl}$, so **excess $\ce{HCl}$** $= 4.00 \times 10^{-3} \text{ mol}$.

**Step 2 — acid that reacted with the limestone.** Total − excess:
$$2.50 \times 10^{-2} - 4.00 \times 10^{-3} = 2.10 \times 10^{-2} \text{ mol }\ce{HCl}$$

**Step 3 — mol $\ce{CaCO3}$.** Ratio is 1 $\ce{CaCO3}$ : 2 $\ce{HCl}$, so halve: $2.10 \times 10^{-2} \times \frac{1}{2} = 1.05 \times 10^{-2} \text{ mol}$.

**Step 4 — grams.** $1.05 \times 10^{-2} \text{ mol} \times 100.09 \text{ g/mol} = 1.05 \text{ g}$.

**Answer:** $1.05 \text{ g of } \ce{CaCO3}$. **Back-titration idea:** measure a *known excess*, titrate what's *left over*, and subtract to find what got used up — handy when the analyte is slow, solid, or won't titrate cleanly on its own.

### Example 10: Diluted-Down "Gotcha" — Which Volume Is Which?

**Problem:** A titration uses $22.00 \text{ mL}$ of $0.125 \text{ M } \ce{NaOH}$ to reach the endpoint against a $10.00 \text{ mL}$ sample of vinegar (acetic acid, $\ce{CH3COOH}$, monoprotic, 1:1). Find the molarity of acetic acid in the vinegar.

**Solution:**

**Step 1 — mol $\ce{NaOH}$ (titrant).** $0.125 \times 0.02200 = 2.75 \times 10^{-3} \text{ mol}$.

**Step 2 — mol acid.** 1:1 → $2.75 \times 10^{-3} \text{ mol}$.

**Step 3 — divide by the ANALYTE's volume**, which is the $10.00 \text{ mL}$ vinegar, **not** the $22.00 \text{ mL}$ of base:
$$M = \frac{2.75 \times 10^{-3} \text{ mol}}{0.01000 \text{ L}} = 0.275 \text{ M}$$

**Answer:** $0.275 \text{ M}$ acetic acid. The single most common slip here is dividing by the titrant volume ($22.00 \text{ mL}$) out of habit — always divide by the volume of the substance whose concentration you want.

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| **Forgetting the mole ratio** (the #1 error) | Assuming every titration is 1:1 because acid–base "feels" one-to-one | Always **balance first** and write the ratio down before touching numbers. If a reagent is diprotic ($\ce{H2SO4}$, $\ce{H2C2O4}$) or has $\ce{2 OH-}$ ($\ce{Ba(OH)2}$), the ratio is NOT 1:1 |
| **Dividing by the wrong volume** | Using the titrant's buret volume where the analyte's volume belongs | Ask: "whose concentration am I solving for?" Divide by *that* substance's volume (Example 10) |
| **Confusing equivalence point and endpoint** | They're numerically almost identical, so the wording feels interchangeable | Equivalence = ideal stoichiometric point (invisible); endpoint = the color flip you *observe*. On the exam, use the exact word the question uses |
| **Forgetting to subtract buret readings** | Reading only the final number off the buret | Volume delivered is always **final − initial**; the buret often doesn't start at 0.00 |
| **Using mL as L in $M \times V$** | Molarity is mol **per liter**, but data comes in mL | Convert mL → L (÷1000) *before* multiplying, every time |
| **Sloppy significant figures** | Rounding mid-problem or ignoring the data's precision | Carry extra digits through, round only at the end, and match the least-precise measurement ([sig figs](/chemistry/0102-significant-figures)) |
| **Blaming a bad titration on math** | A one-drop overshoot changes the answer | Recognize **titration error**: overshooting the endpoint by a drop inflates your titrant volume and skews the result |

---

## AP Exam Tips

- **A titration FRQ is essentially guaranteed.** Every recent AP Chemistry exam has a lab-based question, and titration is the most common. Nail this skill and you've banked points.
- **ALWAYS apply the mole ratio.** Graders are watching for it. Write the balanced equation, circle the ratio, and use it explicitly — even a correct-looking 1:1 answer can lose the ratio point if you never showed it. The $\ce{H2SO4}$ + $\ce{NaOH}$ **1:2 trap** is a favorite; halving (or doubling) at the ratio step is where careless students lose everything.
- **Set it up as $\text{mol} = M \times V$** and show the unit conversion mL → L. Free-response is graded on the setup, so a clearly labeled chain earns credit even if your arithmetic slips.
- **Know equivalence vs. endpoint cold.** A short-answer part often asks you to define or distinguish them, or to say why an indicator was chosen. Equivalence = stoichiometrically exact (theoretical); endpoint = observed color change. The indicator is picked so the endpoint sits at the equivalence point.
- **Report the correct significant figures**, and for buret-based problems, remember volume = final − initial. Sig-fig points are cheap to earn and cheap to lose.
- **Standardization language** shows up: "the $\ce{NaOH}$ was standardized against KHP." That just means they titrated to find the base's *exact* concentration first. Don't let the vocabulary throw you — it's the same calculation run to solve for the titrant's molarity.
- **The deeper pH-curve stuff (why phenolphthalein? what's the shape?) is Unit 8** — Topic 4.6 only wants the stoichiometry. Don't over-answer.

---

## Practice Problems

### Problem 1
$28.50 \text{ mL}$ of $0.100 \text{ M } \ce{NaOH}$ neutralizes $25.00 \text{ mL}$ of $\ce{HCl}$. Find $M_{\ce{HCl}}$.

<details>
<summary><strong>Solution</strong></summary>

$\ce{HCl + NaOH -> NaCl + H2O}$, ratio 1:1.
mol $\ce{NaOH} = 0.100 \times 0.02850 = 2.85 \times 10^{-3}$ mol → same mol $\ce{HCl}$.
$$M_{\ce{HCl}} = \frac{2.85 \times 10^{-3}}{0.02500} = 0.114 \text{ M}$$

**Answer: $0.114 \text{ M}$.**

</details>

### Problem 2
It takes $36.00 \text{ mL}$ of $0.200 \text{ M } \ce{NaOH}$ to titrate $20.00 \text{ mL}$ of $\ce{H2SO4}$. Find $M_{\ce{H2SO4}}$.

<details>
<summary><strong>Solution</strong></summary>

$\ce{H2SO4 + 2NaOH -> Na2SO4 + 2H2O}$, ratio **2 $\ce{NaOH}$ : 1 $\ce{H2SO4}$**.
mol $\ce{NaOH} = 0.200 \times 0.03600 = 7.20 \times 10^{-3}$ mol.
mol $\ce{H2SO4} = 7.20 \times 10^{-3} \times \frac{1}{2} = 3.60 \times 10^{-3}$ mol.
$$M = \frac{3.60 \times 10^{-3}}{0.02000} = 0.180 \text{ M}$$

**Answer: $0.180 \text{ M}$.** (1:1 would wrongly give $0.360 \text{ M}$.)

</details>

### Problem 3
How many mL of $0.250 \text{ M } \ce{HCl}$ are needed to neutralize $40.00 \text{ mL}$ of $0.150 \text{ M } \ce{NaOH}$?

<details>
<summary><strong>Solution</strong></summary>

1:1. mol $\ce{NaOH} = 0.150 \times 0.04000 = 6.00 \times 10^{-3}$ mol = mol $\ce{HCl}$ needed.
$$V = \frac{6.00 \times 10^{-3}}{0.250} = 0.0240 \text{ L} = 24.0 \text{ mL}$$

**Answer: $24.0 \text{ mL}$.**

</details>

### Problem 4
A $0.750 \text{ g}$ sample of pure $\ce{NaOH}$ ($40.00 \text{ g/mol}$) is titrated with $0.500 \text{ M } \ce{HCl}$. What volume of acid is required?

<details>
<summary><strong>Solution</strong></summary>

mol $\ce{NaOH} = \frac{0.750}{40.00} = 1.875 \times 10^{-2}$ mol. Ratio 1:1 → same mol $\ce{HCl}$.
$$V = \frac{1.875 \times 10^{-2}}{0.500} = 0.0375 \text{ L} = 37.5 \text{ mL}$$

**Answer: $37.5 \text{ mL}$.**

</details>

### Problem 5
$25.00 \text{ mL}$ of $0.180 \text{ M } \ce{Ba(OH)2}$ is titrated with $0.300 \text{ M } \ce{HCl}$. What volume of $\ce{HCl}$ is needed?

<details>
<summary><strong>Solution</strong></summary>

$\ce{2HCl + Ba(OH)2 -> BaCl2 + 2H2O}$, ratio **2 $\ce{HCl}$ : 1 $\ce{Ba(OH)2}$**.
mol $\ce{Ba(OH)2} = 0.180 \times 0.02500 = 4.50 \times 10^{-3}$ mol.
mol $\ce{HCl} = 4.50 \times 10^{-3} \times 2 = 9.00 \times 10^{-3}$ mol.
$$V = \frac{9.00 \times 10^{-3}}{0.300} = 0.0300 \text{ L} = 30.0 \text{ mL}$$

**Answer: $30.0 \text{ mL}$.**

</details>

### Problem 6
A $0.400 \text{ g}$ impure sample of $\ce{KOH}$ ($56.11 \text{ g/mol}$) is titrated with $0.250 \text{ M } \ce{HCl}$, requiring $22.40 \text{ mL}$. Find the percent purity.

<details>
<summary><strong>Solution</strong></summary>

1:1. mol $\ce{HCl} = 0.250 \times 0.02240 = 5.60 \times 10^{-3}$ mol → mol $\ce{KOH}$.
mass pure $\ce{KOH} = 5.60 \times 10^{-3} \times 56.11 = 0.314 \text{ g}$.
$$\% = \frac{0.314}{0.400} \times 100 = 78.5\%$$

**Answer: $78.5\%$ pure.**

</details>

### Problem 7
A $0.500 \text{ g}$ sample of a pure monoprotic acid $\ce{HA}$ needs $41.20 \text{ mL}$ of $0.100 \text{ M } \ce{NaOH}$. Find the molar mass of $\ce{HA}$.

<details>
<summary><strong>Solution</strong></summary>

1:1. mol $\ce{NaOH} = 0.100 \times 0.04120 = 4.120 \times 10^{-3}$ mol = mol $\ce{HA}$.
$$\mathcal{M} = \frac{0.500}{4.120 \times 10^{-3}} = 121 \text{ g/mol}$$

**Answer: $\approx 121 \text{ g/mol}$** (consistent with benzoic acid, $122 \text{ g/mol}$).

</details>

### Problem 8
Distinguish the **equivalence point** from the **endpoint** in one sentence each.

<details>
<summary><strong>Solution</strong></summary>

**Equivalence point:** the theoretical moment when the moles of titrant added exactly satisfy the stoichiometry (mole ratio) to react with all the analyte — it's invisible.
**Endpoint:** the experimentally observed signal (usually an indicator color change) used to estimate the equivalence point — it's what you actually see and where you stop.

</details>

### Problem 9
A buret reads $2.15 \text{ mL}$ initially and $38.90 \text{ mL}$ at the endpoint while titrating $25.00 \text{ mL}$ of $0.1200 \text{ M } \ce{HCl}$ with $\ce{NaOH}$ (1:1). Find $M_{\ce{NaOH}}$.

<details>
<summary><strong>Solution</strong></summary>

$V_{\ce{NaOH}} = 38.90 - 2.15 = 36.75 \text{ mL} = 0.03675 \text{ L}$.
mol $\ce{HCl} = 0.1200 \times 0.02500 = 3.000 \times 10^{-3}$ mol → mol $\ce{NaOH}$.
$$M_{\ce{NaOH}} = \frac{3.000 \times 10^{-3}}{0.03675} = 0.08163 \text{ M}$$

**Answer: $0.08163 \text{ M}$** ($8.163 \times 10^{-2} \text{ M}$, 4 sig figs).

</details>

### Problem 10
$15.00 \text{ mL}$ of phosphoric acid $\ce{H3PO4}$ requires $45.00 \text{ mL}$ of $0.200 \text{ M } \ce{NaOH}$ to fully neutralize all three protons. Find $M_{\ce{H3PO4}}$.

<details>
<summary><strong>Solution</strong></summary>

$\ce{H3PO4 + 3NaOH -> Na3PO4 + 3H2O}$, ratio **3 $\ce{NaOH}$ : 1 $\ce{H3PO4}$**.
mol $\ce{NaOH} = 0.200 \times 0.04500 = 9.00 \times 10^{-3}$ mol.
mol $\ce{H3PO4} = 9.00 \times 10^{-3} \times \frac{1}{3} = 3.00 \times 10^{-3}$ mol.
$$M = \frac{3.00 \times 10^{-3}}{0.01500} = 0.200 \text{ M}$$

**Answer: $0.200 \text{ M}$.**

</details>

### Problem 11
Why do you add only 2–3 drops of indicator to the flask, rather than a big squirt?

<details>
<summary><strong>Solution</strong></summary>

Indicators are themselves weak acids/bases, so they consume a tiny amount of titrant when they change color. Using only a couple of drops keeps that consumption negligible, so the endpoint stays as close as possible to the true equivalence point and doesn't distort the volume you measure.

</details>

### Problem 12
A student overshoots the endpoint, adding one extra drop of $\ce{NaOH}$ past the color change. Does their calculated concentration of the acid come out **too high** or **too low**? Explain.

<details>
<summary><strong>Solution</strong></summary>

Too **high**. Extra titrant volume → more calculated mol $\ce{NaOH}$ → more calculated mol acid → dividing by the same (unchanged) acid volume gives a larger molarity than the true value. This is classic **titration error** from overshooting the endpoint.

</details>

### Problem 13
Back-titration: $2.00 \times 10^{-2} \text{ mol}$ of $\ce{HCl}$ is added to a solid antacid containing $\ce{CaCO3}$ ($\ce{CaCO3 + 2HCl -> CaCl2 + H2O + CO2}$). The leftover $\ce{HCl}$ needs $12.00 \text{ mL}$ of $0.500 \text{ M } \ce{NaOH}$. Find mol of $\ce{CaCO3}$ that reacted.

<details>
<summary><strong>Solution</strong></summary>

Excess $\ce{HCl}$ = mol $\ce{NaOH} = 0.500 \times 0.01200 = 6.00 \times 10^{-3}$ mol (1:1).
Reacted $\ce{HCl} = 2.00 \times 10^{-2} - 6.00 \times 10^{-3} = 1.40 \times 10^{-2}$ mol.
mol $\ce{CaCO3} = 1.40 \times 10^{-2} \times \frac{1}{2} = 7.00 \times 10^{-3}$ mol.

**Answer: $7.00 \times 10^{-3} \text{ mol } \ce{CaCO3}$.**

</details>

### Problem 14
$30.00 \text{ mL}$ of $0.150 \text{ M } \ce{HCl}$ is titrated with $0.100 \text{ M } \ce{NaOH}$ (1:1). Use the shortcut $M_aV_a = M_bV_b$ to find the volume of base needed, then say whether the shortcut would have been safe if the acid were $\ce{H2SO4}$.

<details>
<summary><strong>Solution</strong></summary>

$V_b = \frac{M_a V_a}{M_b} = \frac{0.150 \times 30.00}{0.100} = 45.0 \text{ mL}$.
No — the shortcut assumes 1:1. For $\ce{H2SO4}$ (ratio 1:2) you'd need the full mole-ratio chain, and the shortcut would underestimate the base by half.

**Answer: $45.0 \text{ mL}$; not safe for $\ce{H2SO4}$.**

</details>

### Problem 15
A $10.00 \text{ mL}$ sample of vinegar is diluted, then titrated: it takes $34.20 \text{ mL}$ of $0.500 \text{ M } \ce{NaOH}$ to reach the endpoint. Acetic acid is monoprotic (1:1). Find the molarity of acetic acid in the original vinegar, and identify which volume you divide by.

<details>
<summary><strong>Solution</strong></summary>

mol $\ce{NaOH} = 0.500 \times 0.03420 = 1.710 \times 10^{-2}$ mol → mol acid (1:1).
Divide by the **analyte** volume, the $10.00 \text{ mL}$ vinegar (not the $34.20 \text{ mL}$ of titrant):
$$M = \frac{1.710 \times 10^{-2}}{0.01000} = 1.71 \text{ M}$$

**Answer: $1.71 \text{ M}$; divide by the $10.00 \text{ mL}$ analyte volume.**

</details>

---

## Quick Reference

| Term | Meaning |
|---|---|
| **Titrant** | Known-concentration solution added from the buret (the "hot sauce") |
| **Analyte** | Unknown solution being measured, in the flask (the "soup") |
| **Equivalence point** | Stoichiometrically exact point (theoretical, invisible) |
| **Endpoint** | Observed indicator color change (your estimate of equivalence) |
| **Standardization** | Titrating to find a titrant's *exact* concentration |
| **Back-titration** | Add known excess reagent, titrate the leftover, subtract |
| **Titration error** | Overshooting the endpoint → titrant volume too high |

| Step | Equation |
|---|---|
| Volume delivered | $V = V_{\text{final}} - V_{\text{initial}}$ |
| Moles from molarity | $\text{mol} = M \times V_{(\text{L})}$ |
| Apply mole ratio | $\text{mol analyte} = \text{mol titrant} \times \dfrac{\text{coeff analyte}}{\text{coeff titrant}}$ |
| Analyte molarity | $M = \dfrac{\text{mol analyte}}{V_{\text{analyte (L)}}}$ |
| Analyte mass / molar mass | $\text{grams} = \text{mol} \times \mathcal{M}$, or $\mathcal{M} = \dfrac{\text{grams}}{\text{mol}}$ |
| 1:1 shortcut **only** | $M_a V_a = M_b V_b$ |

**The one rule to never forget:** balance the equation and apply the mole ratio — every single time.

---

<div align="center">

[← Stoichiometry](/chemistry/0603-stoichiometry) | [Acid-Base Reactions →](/chemistry/0605-acid-base-reactions)

</div>
