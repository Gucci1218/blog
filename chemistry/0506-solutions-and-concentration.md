# Solutions and Concentration
<p class="article-date">July 5, 2026</p>

*At my boba shop the first question is never "what size?" — it's "what sweetness?" You pick 25%, 50%, 75%, or 100%, and here's the part that quietly blew my mind: it's the exact same drink, the exact same cup, the exact same amount of liquid. The only thing that changes is how much sugar syrup got stirred into it, and your tongue can measure that change with zero equipment. That's the whole idea of concentration — how much stuff is dissolved per amount of liquid — and it turns out chemists have a sweetness dial too. They call it molarity. The sugar is the solute, the tea is the solvent, the finished drink is the solution, and the sweetness you taste is the concentration. Once you see it this way, two drinks can hold the same total sugar and still taste completely different, because one is bigger and more watered-down. And when the barista over-ices your 50% drink and the ice melts, you can literally taste it fade to a 30% — that's dilution happening live. This is AP Unit 3, Topics 3.7 and 3.8, and it's the language every future lab, titration, and reaction-in-water problem will be written in.*

---

## What You'll Learn

- Use the vocabulary of solutions correctly: **solute**, **solvent**, **solution**, and **aqueous**
- Describe what happens at the molecular level when something dissolves (**solvation** / **hydration**), and why ionic solids get pulled apart by water
- Distinguish **electrolytes** from **nonelectrolytes**, and strong from weak, and explain why salt water conducts electricity but sugar water doesn't
- Calculate **molarity** ($M = \frac{\text{mol solute}}{\text{L solution}}$) in both directions — from grams and volume, and from a target concentration back to grams needed
- Describe how to prepare a solution of known molarity from a solid using a **volumetric flask**
- Solve **dilution** problems with $M_1V_1 = M_2V_2$, including serial dilutions and stock-solution prep
- Find the concentration of **each individual ion** produced when a salt dissolves, and write **net dissociation equations**
- Reason about **particulate (beaker) diagrams**: which drawing shows the higher concentration, and whether the ions are drawn in the correct ratio
- Compute other concentration measures — **mole fraction**, **molality**, **mass percent**, and **ppm** — and know when each shows up

---

## Prerequisites

- [The Mole](/chemistry/0207-the-mole) — molarity is *moles* per liter, so every concentration problem starts by converting grams to moles; this is that skill's home turf
- [Dimensional Analysis](/chemistry/0103-dimensional-analysis) — molarity is a conversion factor in disguise ($\frac{\text{mol}}{\text{L}}$), and every problem here is a railroad chain of canceling units

---

## The Core Concept

### Intuition First

Back to the boba counter. Let's freeze the moment you order a **50% sweetness large** and name every part, because these names are the whole game:

| Boba drink | Chemistry term | What it means |
|---|---|---|
| the sugar syrup you dissolve in | **solute** | the stuff being dissolved (usually the smaller amount) |
| the tea / water it dissolves into | **solvent** | the stuff doing the dissolving (usually the larger amount) |
| the finished drink in the cup | **solution** | the uniform mixture of the two |
| the sweetness your tongue reads | **concentration** | how much solute per amount of solution |

A **solution** is a *homogeneous* mixture — stir it and every sip tastes identical, top to bottom. That uniformity is the signature of a true solution: you can't see the sugar anymore, and no amount of sitting will let it settle back out. When the solvent is water — which is almost always in AP Chem — we call the solution **aqueous** and tag it with $(aq)$, like $\ce{NaCl(aq)}$.

Now the key insight the boba shop teaches for free: **concentration is a ratio, not an amount.** A 100% small and a 50% large might contain the *same total grams of sugar*, but they don't taste the same, because the large one spread that sugar through more liquid. Sweetness — concentration — depends on **sugar ÷ drink size**, not sugar alone. Hold that thought; it's the single most common trap in this entire unit.

And dilution? That's the melting ice. Your 50% drink sits too long, the ice melts, the sugar count never changes — but the *volume* creeps up, so the ratio drops and the drink fades toward 30%. Same sugar, bigger drink, weaker taste. We'll turn that exact picture into an equation.

### What "Dissolving" Actually Is (the molecular view)

Zoom into the cup as sugar dissolves. Water molecules are little bent magnets — one slightly positive end (the H side), one slightly negative end (the O side). They swarm each sugar molecule, latch on, and carry it away from its neighbors until it's completely surrounded and floating free. That surrounding process is called **solvation**; when the solvent is specifically water, we call it **hydration**.

For **ionic** solutes like table salt, $\ce{NaCl}$, it's even more dramatic. In the solid, $\ce{Na+}$ and $\ce{Cl-}$ are locked in a rigid lattice by their opposite charges. Water attacks that lattice with **ion–dipole forces**: the negative (oxygen) ends of many water molecules gang up on each $\ce{Na+}$, the positive (hydrogen) ends surround each $\ce{Cl-}$, and they pull the ions apart and cocoon them:

$$\ce{NaCl(s) -> Na+(aq) + Cl-(aq)}$$

That's **dissociation** — the salt splits into free, independently roaming ions. This is the payoff of everything we said about polarity and intermolecular forces: water dissolves ionic and polar things because it can grab their charges. "Like dissolves like."

### Electrolytes: Why Salt Water Zaps and Sugar Water Doesn't

Here's a demo worth picturing. Dip two wires from a battery and a lightbulb into a beaker.

- Dip them in **sugar water**: the bulb stays dark. Sugar ($\ce{C12H22O11}$) dissolves as whole, neutral molecules. No charged particles are free to move, so no current flows. Sugar is a **nonelectrolyte**.
- Dip them in **salt water**: the bulb glows. $\ce{NaCl}$ dissociated into mobile $\ce{Na+}$ and $\ce{Cl-}$ ions, and moving charges *are* an electric current. Salt is an **electrolyte**.

Same water, wildly different behavior — and the only difference is whether the dissolved particles carry charge. Electrolytes come in strengths:

| Type | What dissolves as | Conducts? | Examples |
|---|---|---|---|
| **Strong electrolyte** | (nearly) 100% ions | Brightly | $\ce{NaCl}$, $\ce{KNO3}$, strong acids ($\ce{HCl}$), soluble salts |
| **Weak electrolyte** | mostly molecules, a few ions | Dimly | weak acids like $\ce{CH3COOH}$ (acetic acid / vinegar) |
| **Nonelectrolyte** | 100% neutral molecules | Not at all | sugar, ethanol, most molecular compounds |

For AP Unit 3, the headline is: **soluble ionic compounds and strong acids are strong electrolytes** (they dissociate completely), and molecular compounds like sugar are usually nonelectrolytes.

### Molarity: the Chemist's Sweetness Dial

Molarity is *the* concentration unit of AP Chemistry. Its definition is exactly "sugar per drink":

$$M = \frac{\text{moles of solute}}{\text{liters of solution}} = \frac{n}{V}$$

The units of molarity are **mol/L**, abbreviated $M$ and read "molar." A "0.50 M $\ce{NaCl}$" solution is "0.50 molar sodium chloride" — half a mole of salt in every liter of solution.

Two things to burn in now, because the AP exam lives on them:

1. **It's moles on top, not grams.** If a problem hands you grams, your very first move is grams → moles using molar mass. That's the [mole](/chemistry/0207-the-mole) handoff.
2. **It's liters of *solution*, not solvent.** This is the boba insight in disguise. You don't measure how much *tea* you started with — you measure how much *finished drink* you ended with. When sugar dissolves it takes up a little room too, so the final volume is set by the whole solution, never by the water alone. Write it on your hand: **L of solution, not L of solvent.**

The formula rearranges three ways, and you'll use all three:

$$n = M \times V \qquad M = \frac{n}{V} \qquad V = \frac{n}{M}$$

### Dilution: the Melting-Ice Equation

When you add water to a solution, you add *solvent* but no new *solute*. The moles of solute stay frozen; only the volume grows. Since $n = M \times V$, and $n$ doesn't change:

$$\boxed{M_1 V_1 = M_2 V_2}$$

where subscript 1 is "before" (concentrated stock) and 2 is "after" (diluted). It's just "moles before = moles after." This is the melting ice: $M_1 V_1$ is your 50% drink, and as $V_2$ grows, $M_2$ has to shrink to keep the product constant. Same sugar, bigger drink, weaker sweetness.

### The Ion-Counting Trap (per-ion concentration)

Here's the classic AP curveball. When a salt dissolves, the concentration of the *salt* is not always the concentration of its *ions* — you have to count how many of each ion each formula unit releases. Calcium chloride is the poster child:

$$\ce{CaCl2(s) -> Ca^2+(aq) + 2Cl-(aq)}$$

One formula unit throws off **one** $\ce{Ca^2+}$ but **two** $\ce{Cl-}$. So a 0.10 M $\ce{CaCl2}$ solution is:

$$[\ce{Ca^2+}] = 0.10 \ M \qquad [\ce{Cl-}] = 2 \times 0.10 = 0.20 \ M$$

(Those square brackets, $[\ce{Cl-}]$, are shorthand for "molar concentration of.") Read the subscript. Two chlorides means double the chloride concentration.

---

## Worked Examples

### Example 1: Naming the Parts

**Problem:** You dissolve 15 g of table salt in 500 mL of water to make a brine for pickling. Identify the solute, the solvent, and the solution, and write whether it's aqueous.

**Solution:**

**Step 1:** The thing being dissolved, present in the smaller amount, is the **solute** — the salt, $\ce{NaCl}$.

**Step 2:** The thing doing the dissolving, in the larger amount, is the **solvent** — water.

**Step 3:** The uniform salty mixture that results is the **solution** — brine. Because the solvent is water, it is **aqueous**: $\ce{NaCl(aq)}$.

**Answer: solute = $\ce{NaCl}$; solvent = water; solution = the aqueous brine, $\ce{NaCl(aq)}$.**

### Example 2: Molarity from Grams and Volume

**Problem:** A sports drink contains 6.84 g of table sugar, $\ce{C12H22O11}$, dissolved to make 250. mL of drink. What is the molarity of the sugar?

**Solution:**

**Step 1 (grams → moles):** Molar mass of $\ce{C12H22O11}$ is $12(12.01) + 22(1.01) + 11(16.00) = 342.34$ g/mol.

$$6.84 \ \cancel{\text{g}} \times \frac{1 \ \text{mol}}{342.34 \ \cancel{\text{g}}} = 0.0200 \ \text{mol}$$

**Step 2 (mL → L):** Molarity needs *liters*: $250. \ \text{mL} = 0.250 \ \text{L}$.

**Step 3 (divide):**

$$M = \frac{0.0200 \ \text{mol}}{0.250 \ \text{L}} = 0.0800 \ M$$

**Answer: 0.0800 M sucrose.** Notice the two rookie-proofing moves: convert grams to moles first, and convert mL to L before dividing.

### Example 3: Grams Needed to Make a Solution (reverse direction)

**Problem:** Your lab calls for 2.00 L of 0.150 M $\ce{NaCl}$. How many grams of salt do you weigh out?

**Solution:**

**Step 1 (M and V → moles):** Rearrange to $n = M \times V$:

$$n = 0.150 \ \frac{\text{mol}}{\cancel{\text{L}}} \times 2.00 \ \cancel{\text{L}} = 0.300 \ \text{mol} \ \ce{NaCl}$$

**Step 2 (moles → grams):** Molar mass of $\ce{NaCl}$ is $22.99 + 35.45 = 58.44$ g/mol.

$$0.300 \ \cancel{\text{mol}} \times \frac{58.44 \ \text{g}}{1 \ \cancel{\text{mol}}} = 17.5 \ \text{g}$$

**Answer: weigh out 17.5 g of $\ce{NaCl}$.**

### Example 4: Preparing the Solution (the volumetric flask)

**Problem:** Describe how you would actually make the 2.00 L of 0.150 M $\ce{NaCl}$ from Example 3 in the lab.

**Solution:**

**Step 1:** Weigh **17.5 g** of $\ce{NaCl}$ on a balance (the arithmetic from Example 3).

**Step 2:** Add the salt to a **2.00 L volumetric flask** — a flask with a single etched line on its neck marking exactly 2.00 L. Add *some* water, maybe half-full, and swirl until every crystal dissolves.

**Step 3:** Now the crucial part — the "L of solution" rule made physical. Carefully add water until the bottom of the meniscus sits **right on the 2.00 L line**, then stopper and invert to mix.

You do **not** measure 2.00 L of water and dump the salt in. You dissolve the salt, *then* fill to the line, so the final *solution* volume is exactly 2.00 L. The volumetric flask is engineered to enforce the definition of molarity.

**Answer: dissolve 17.5 g $\ce{NaCl}$ in a 2.00 L volumetric flask, then fill with water to the 2.00 L calibration line.**

### Example 5: Molarity → Moles in a Given Volume

**Problem:** How many moles of $\ce{HCl}$ are in 45.0 mL of 3.00 M hydrochloric acid? How many grams?

**Solution:**

**Step 1 (mL → L):** $45.0 \ \text{mL} = 0.0450 \ \text{L}$.

**Step 2 ($n = M \times V$):**

$$n = 3.00 \ \frac{\text{mol}}{\cancel{\text{L}}} \times 0.0450 \ \cancel{\text{L}} = 0.135 \ \text{mol} \ \ce{HCl}$$

**Step 3 (moles → grams):** $M_{\ce{HCl}} = 1.01 + 35.45 = 36.46$ g/mol.

$$0.135 \ \cancel{\text{mol}} \times \frac{36.46 \ \text{g}}{1 \ \cancel{\text{mol}}} = 4.92 \ \text{g}$$

**Answer: 0.135 mol, which is 4.92 g of $\ce{HCl}$.**

### Example 6: Dilution — the Melting Ice

**Problem:** You have 100. mL of a 0.50 M sugar solution (your "50% sweet" drink). The barista adds ice that melts into 66 mL of extra water. What is the new concentration? (Assume volumes add.)

**Solution:**

**Step 1:** Identify before-and-after. $M_1 = 0.50 \ M$, $V_1 = 100. \ \text{mL}$. The new volume is $V_2 = 100 + 66 = 166 \ \text{mL}$.

**Step 2:** Solve $M_1 V_1 = M_2 V_2$ for $M_2$ (volumes can stay in mL as long as both match — the units cancel):

$$M_2 = \frac{M_1 V_1}{V_2} = \frac{(0.50 \ M)(100. \ \text{mL})}{166 \ \text{mL}} = 0.30 \ M$$

**Answer: 0.30 M.** Your 50%-sweet drink literally faded to 30%. Same sugar, bigger drink, weaker taste — exactly the boba prediction.

### Example 7: Dilution — How Much Stock Do I Need?

**Problem:** You need 500. mL of 0.100 M $\ce{HCl}$, and all you have is a 6.00 M stock bottle. What volume of stock do you measure out, and how do you make it?

**Solution:**

**Step 1:** Here the *diluted* solution is the target: $M_2 = 0.100 \ M$, $V_2 = 500. \ \text{mL}$. The stock is side 1: $M_1 = 6.00 \ M$, $V_1 = ?$

**Step 2:** Solve for $V_1$:

$$V_1 = \frac{M_2 V_2}{M_1} = \frac{(0.100 \ M)(500. \ \text{mL})}{6.00 \ M} = 8.33 \ \text{mL}$$

**Step 3 (procedure):** Measure **8.33 mL** of the 6.00 M stock, add it to a 500. mL volumetric flask, then fill with water to the 500. mL line.

**Answer: measure 8.33 mL of stock and dilute up to 500. mL.** Safety note that AP loves: always add acid *to* water, never water to acid.

### Example 8: Serial Dilution

**Problem:** You start with 10.0 mL of 1.00 M dye. You dilute it to 100. mL, then take 10.0 mL of *that* and dilute again to 100. mL. What's the final concentration?

**Solution:**

**Step 1 (first dilution):** $M_2 = \dfrac{(1.00 \ M)(10.0 \ \text{mL})}{100. \ \text{mL}} = 0.100 \ M$. Each 10-into-100 step is a 10× dilution.

**Step 2 (second dilution):** Take that 0.100 M and do it again:

$$M_3 = \frac{(0.100 \ M)(10.0 \ \text{mL})}{100. \ \text{mL}} = 0.0100 \ M$$

**Answer: 0.0100 M** — a 100× total dilution ($10 \times 10$). Serial dilutions are how labs reach tiny, precise concentrations without measuring impossibly small volumes.

### Example 9: Concentration of Each Ion (the AP trap)

**Problem:** What is the concentration of each ion in 0.10 M $\ce{CaCl2}$? In 0.25 M $\ce{Al2(SO4)3}$?

**Solution:**

**Step 1 (write the dissociation):**

$$\ce{CaCl2(s) -> Ca^2+(aq) + 2Cl-(aq)}$$

One $\ce{Ca^2+}$ and two $\ce{Cl-}$ per formula unit, so:

$$[\ce{Ca^2+}] = 1 \times 0.10 = 0.10 \ M \qquad [\ce{Cl-}] = 2 \times 0.10 = 0.20 \ M$$

**Step 2 (repeat for the aluminum salt):**

$$\ce{Al2(SO4)3(s) -> 2Al^3+(aq) + 3SO4^2-(aq)}$$

$$[\ce{Al^3+}] = 2 \times 0.25 = 0.50 \ M \qquad [\ce{SO4^2-}] = 3 \times 0.25 = 0.75 \ M$$

**Answer:** In $\ce{CaCl2}$: $[\ce{Ca^2+}] = 0.10 \ M$, $[\ce{Cl-}] = 0.20 \ M$. In $\ce{Al2(SO4)3}$: $[\ce{Al^3+}] = 0.50 \ M$, $[\ce{SO4^2-}] = 0.75 \ M$. Always let the subscripts multiply the concentration.

### Example 10: Net Dissociation and Total Ion Concentration

**Problem:** Write the dissociation of $\ce{Na3PO4}$ and find the *total* concentration of all ions in a 0.20 M solution.

**Solution:**

**Step 1 (dissociation):** Sodium phosphate splits into 3 sodium ions and 1 phosphate ion:

$$\ce{Na3PO4(s) -> 3Na+(aq) + PO4^3-(aq)}$$

**Step 2 (each ion):** $[\ce{Na+}] = 3 \times 0.20 = 0.60 \ M$ and $[\ce{PO4^3-}] = 1 \times 0.20 = 0.20 \ M$.

**Step 3 (total ions):** Add them up:

$$0.60 + 0.20 = 0.80 \ M \ \text{total ions}$$

**Answer: $[\ce{Na+}] = 0.60 \ M$, $[\ce{PO4^3-}] = 0.20 \ M$, total ion concentration = 0.80 M.** Four ions come off each formula unit, so the total is $4 \times 0.20$ — a good sanity check.

### Example 11: Reading a Particulate (Beaker) Diagram

**Problem:** Two beakers each hold the same volume of solution. Below, each ● is one dissolved particle. Which beaker is more concentrated, and by what factor?

```
   Beaker A            Beaker B
 +-----------+       +-----------+
 |  ●   ●    |       |  ● ● ● ●  |
 |     ●     |       |  ● ● ● ●  |
 |  ●        |       |  ● ● ● ●  |
 +-----------+       +-----------+
   4 particles         12 particles
```

**Solution:**

**Step 1:** Same volume, so concentration is set purely by the particle *count*.

**Step 2:** Beaker A has 4 particles; Beaker B has 12. The ratio is $12 / 4 = 3$.

**Answer: Beaker B is 3× more concentrated than Beaker A.** This is exactly the boba logic — same cup size, so whoever has more dissolved stuff is "sweeter." On the AP exam, if A were 0.1 M, B would be drawn as 0.3 M, and a correct diagram must show *three times as many* dots, not just "more."

### Example 12: Drawing Dissolved Ions in the Right Ratio

**Problem:** A student must draw a particulate diagram of dissolved $\ce{MgCl2}$. They draw 3 magnesium ions and 3 chloride ions. What's wrong, and what should it look like?

**Solution:**

**Step 1:** Write the dissociation to get the correct ratio:

$$\ce{MgCl2(s) -> Mg^2+(aq) + 2Cl-(aq)}$$

Every $\ce{Mg^2+}$ must be accompanied by **two** $\ce{Cl-}$.

**Step 2:** The student drew a 1:1 ratio (3 and 3). That's the error — it should be 1:2. For 3 magnesiums, you need **6** chlorides:

```
 +-------------------------+
 |  [Mg2+]  Cl-   Cl-      |
 |     Cl-    [Mg2+]  Cl-  |
 |  [Mg2+]   Cl-    Cl-    |
 +-------------------------+
   3 Mg2+  :  6 Cl-   (1 : 2)
```

**Answer: the diagram must show twice as many chloride ions as magnesium ions (here, 3 $\ce{Mg^2+}$ and 6 $\ce{Cl-}$).** Wrong ion ratios are the number-one way to lose the point on Unit 3.8 drawing questions.

### Example 13: Mass Percent and ppm (water quality)

**Problem:** A city water report says the tap water contains 25 mg of dissolved calcium per liter of water. Express this as (a) parts per million and (b) mass percent. (Take 1 L of water ≈ 1000 g.)

**Solution:**

**Step 1 (ppm):** For dilute water solutions, **ppm = mg of solute per liter** (because 1 L of water ≈ $10^6$ mg):

$$\text{ppm} = \frac{25 \ \text{mg}}{1 \ \text{L}} = 25 \ \text{ppm}$$

**Step 2 (mass percent):** Mass percent is $\dfrac{\text{mass solute}}{\text{mass solution}} \times 100\%$. Here $25 \ \text{mg} = 0.025 \ \text{g}$ in $\approx 1000 \ \text{g}$:

$$\text{mass \%} = \frac{0.025 \ \text{g}}{1000 \ \text{g}} \times 100\% = 0.0025\%$$

**Answer: 25 ppm, or 0.0025% by mass.** ppm is just a convenient magnifying glass for concentrations too tiny to write comfortably as percents — perfect for pollutants and minerals in water.

### Example 14: Mole Fraction and Molality

**Problem:** You dissolve 0.500 mol of ethanol in 2.00 kg of water (water: 55.5 mol). Find (a) the mole fraction of ethanol and (b) the molality of the solution.

**Solution:**

**Step 1 (mole fraction):** Mole fraction $X$ is moles of one component ÷ total moles:

$$X_{\text{ethanol}} = \frac{0.500}{0.500 + 55.5} = \frac{0.500}{56.0} = 0.00893$$

**Step 2 (molality):** Molality $m$ is moles of solute per **kilogram of solvent** (note: kg of solvent, not L of solution):

$$m = \frac{0.500 \ \text{mol}}{2.00 \ \text{kg}} = 0.250 \ m$$

**Answer: $X_{\text{ethanol}} = 0.00893$; molality = 0.250 m.** Molarity is still king on the AP exam, but molality returns later for colligative properties (like why salt lowers water's freezing point), because it doesn't change when temperature swells the volume.

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Dividing by liters of **solvent** instead of **solution** | "It's dissolved *in* water, so I use the water volume" | Molarity is per L of *finished solution*; fill to the flask line, don't measure the water |
| Using **grams** in the molarity formula | Forgetting the "moles" in mol/L | Convert grams → moles *first*, every time |
| Leaving volume in **mL** | Molarity's unit is mol/**L** | Convert mL → L (÷1000) before dividing |
| Giving the salt's molarity as each ion's molarity | Not reading the subscripts | 0.10 M $\ce{CaCl2}$ → $[\ce{Cl-}] = 0.20 \ M$; the 2 doubles it |
| Drawing ions in a 1:1 ratio in particle diagrams | Copying the count, not the formula | Write the dissociation first; $\ce{MgCl2}$ needs 2 $\ce{Cl-}$ per $\ce{Mg^2+}$ |
| Thinking dilution changes the moles of solute | "I added water, so there's more stuff" | Adding solvent changes *volume only*; moles are frozen — that's why $M_1V_1 = M_2V_2$ works |
| Calling sugar water an electrolyte | "It's dissolved, so it must conduct" | Only **ions** conduct; sugar dissolves as neutral molecules (nonelectrolyte) |
| Mixing up molarity and molality | The names are one letter apart | Mol**a**rity = per **L of solution**; mol**a**lity = per **kg of solvent** |

---

## AP Exam Tips

- **"L of solution, not solvent" is tested directly.** FRQs describing a volumetric flask procedure award the point for *filling to the calibration line after dissolving*, not for measuring the solvent first. Say it explicitly in your answer.
- **Per-ion concentration is a guaranteed appearance.** Any time a soluble salt dissolves, expect to be asked for $[\ce{ion}]$. Write the balanced dissociation equation, then multiply each ion's concentration by its coefficient. $\ce{CaCl2}$, $\ce{Na2SO4}$, $\ce{Al2(SO4)3}$ are perennial favorites.
- **Particulate diagrams (Topic 3.8) reward correct ratios.** When you draw dissolved ions, get the *stoichiometric ratio* right (2 anions per cation for $\ce{MgCl2}$) and the *relative amount* right (0.2 M shows twice the dots of 0.1 M at equal volume). Graders check both.
- **$M_1V_1 = M_2V_2$ is a speed tool.** For any "dilute this / how much stock" problem, reach for it immediately — no need to compute moles separately. Volumes can stay in mL as long as both sides match.
- **Show units and canceling.** Molarity problems are dimensional-analysis problems; visible unit cancellation earns work-shown credit and catches your own errors.
- **Molarity dominates; molality is a cameo.** Nearly every solution FRQ uses molarity. Molality shows up only in the colligative-properties context. Don't reach for molality unless the problem mentions freezing/boiling points or specifically asks for it.
- **Strong vs. weak vs. non-electrolyte** shows up in conductivity questions: strong = many ions = bright bulb; weak = few ions = dim; nonelectrolyte = no ions = dark.

---

## Practice Problems

### Problem 1

A solution is made by dissolving iodine crystals in ethanol (to make tincture of iodine). Identify the solute and the solvent.

<details>
<summary><strong>Solution</strong></summary>

The iodine is present in the smaller amount and is being dissolved — it's the **solute**. Ethanol, the larger amount doing the dissolving, is the **solvent**. (Note the solvent here is *not* water, so this solution is not aqueous.)

**Answer: solute = iodine; solvent = ethanol.**

</details>

### Problem 2

Calculate the molarity of a solution made by dissolving 4.00 g of $\ce{NaOH}$ to a total volume of 500. mL.

<details>
<summary><strong>Solution</strong></summary>

Molar mass of $\ce{NaOH} = 22.99 + 16.00 + 1.01 = 40.00$ g/mol.

$$4.00 \ \cancel{\text{g}} \times \frac{1 \ \text{mol}}{40.00 \ \cancel{\text{g}}} = 0.100 \ \text{mol}$$

Convert volume: $500. \ \text{mL} = 0.500 \ \text{L}$.

$$M = \frac{0.100 \ \text{mol}}{0.500 \ \text{L}} = 0.200 \ M$$

**Answer: 0.200 M $\ce{NaOH}$.**

</details>

### Problem 3

How many grams of $\ce{KNO3}$ are needed to prepare 250. mL of 0.400 M $\ce{KNO3}$?

<details>
<summary><strong>Solution</strong></summary>

Moles needed: $n = M \times V = 0.400 \ \frac{\text{mol}}{\text{L}} \times 0.250 \ \text{L} = 0.100 \ \text{mol}$.

Molar mass of $\ce{KNO3} = 39.10 + 14.01 + 3(16.00) = 101.11$ g/mol.

$$0.100 \ \cancel{\text{mol}} \times \frac{101.11 \ \text{g}}{1 \ \cancel{\text{mol}}} = 10.1 \ \text{g}$$

**Answer: 10.1 g of $\ce{KNO3}$.**

</details>

### Problem 4

Describe, in steps, how you would prepare the solution in Problem 3 using a volumetric flask.

<details>
<summary><strong>Solution</strong></summary>

1. Weigh out **10.1 g** of $\ce{KNO3}$.
2. Add it to a **250. mL volumetric flask** with some water, and swirl until fully dissolved.
3. Add water until the meniscus rests exactly on the **250. mL line**, then stopper and invert to mix.

Key point: fill to the line *after* dissolving, so the final *solution* volume is 250. mL.

**Answer: dissolve 10.1 g $\ce{KNO3}$ in a 250. mL volumetric flask, then fill to the calibration line.**

</details>

### Problem 5

How many moles of solute are in 75.0 mL of 0.250 M $\ce{Na2CO3}$?

<details>
<summary><strong>Solution</strong></summary>

$$n = M \times V = 0.250 \ \frac{\text{mol}}{\cancel{\text{L}}} \times 0.0750 \ \cancel{\text{L}} = 0.0188 \ \text{mol}$$

**Answer: 0.0188 mol (i.e., $1.88 \times 10^{-2}$ mol) $\ce{Na2CO3}$.**

</details>

### Problem 6

You dilute 25.0 mL of 2.00 M $\ce{HCl}$ to a final volume of 250. mL. What is the new concentration?

<details>
<summary><strong>Solution</strong></summary>

$$M_2 = \frac{M_1 V_1}{V_2} = \frac{(2.00 \ M)(25.0 \ \text{mL})}{250. \ \text{mL}} = 0.200 \ M$$

**Answer: 0.200 M $\ce{HCl}$** (a 10× dilution).

</details>

### Problem 7

What volume of 12.0 M stock $\ce{HCl}$ is needed to make 1.00 L of 0.500 M $\ce{HCl}$?

<details>
<summary><strong>Solution</strong></summary>

$$V_1 = \frac{M_2 V_2}{M_1} = \frac{(0.500 \ M)(1.00 \ \text{L})}{12.0 \ M} = 0.0417 \ \text{L} = 41.7 \ \text{mL}$$

**Answer: 41.7 mL of stock, diluted up to 1.00 L** (add acid to water!).

</details>

### Problem 8

Starting from 5.0 mL of 0.20 M solution, you dilute to 50.0 mL, then take 5.0 mL of that and dilute to 50.0 mL again. Find the final concentration.

<details>
<summary><strong>Solution</strong></summary>

First 10× dilution: $\dfrac{(0.20)(5.0)}{50.0} = 0.020 \ M$.

Second 10× dilution: $\dfrac{(0.020)(5.0)}{50.0} = 0.0020 \ M$.

**Answer: 0.0020 M** (a 100× total dilution).

</details>

### Problem 9

Give the concentration of each ion in 0.15 M $\ce{K2SO4}$.

<details>
<summary><strong>Solution</strong></summary>

$$\ce{K2SO4(s) -> 2K+(aq) + SO4^2-(aq)}$$

$$[\ce{K+}] = 2 \times 0.15 = 0.30 \ M \qquad [\ce{SO4^2-}] = 1 \times 0.15 = 0.15 \ M$$

**Answer: $[\ce{K+}] = 0.30 \ M$, $[\ce{SO4^2-}] = 0.15 \ M$.**

</details>

### Problem 10

A solution is 0.050 M in $\ce{AlCl3}$. What is $[\ce{Cl-}]$? Write the dissociation equation.

<details>
<summary><strong>Solution</strong></summary>

$$\ce{AlCl3(s) -> Al^3+(aq) + 3Cl-(aq)}$$

Three chlorides per formula unit:

$$[\ce{Cl-}] = 3 \times 0.050 = 0.15 \ M$$

**Answer: $[\ce{Cl-}] = 0.15 \ M$.**

</details>

### Problem 11

Which represents the higher concentration at equal volume: a beaker with 6 dissolved particles, or one with 2? By what factor? If the dilute one is 0.05 M, what is the other?

<details>
<summary><strong>Solution</strong></summary>

Equal volume means count decides. $6 / 2 = 3$, so the 6-particle beaker is **3× more concentrated**. If the dilute one is 0.05 M, the other is $3 \times 0.05 = 0.15 \ M$.

**Answer: the 6-particle beaker, 3× higher, at 0.15 M.**

</details>

### Problem 12

A student draws dissolved $\ce{Na2S}$ as 4 sodium ions and 4 sulfide ions. What is the error, and what is the correct ratio?

<details>
<summary><strong>Solution</strong></summary>

$$\ce{Na2S(s) -> 2Na+(aq) + S^2-(aq)}$$

The correct ratio is **2 $\ce{Na+}$ per 1 $\ce{S^2-}$**, i.e., 2:1 — not the 1:1 the student drew. For 4 sulfides you'd need 8 sodiums; or for 4 sodiums, only 2 sulfides.

**Answer: the ratio must be 2 $\ce{Na+}$ : 1 $\ce{S^2-}$, not 1:1.**

</details>

### Problem 13

A pool test shows 3.0 mg of chlorine per liter of water. Express this in ppm. (1 L water ≈ $10^6$ mg.)

<details>
<summary><strong>Solution</strong></summary>

For dilute aqueous solutions, ppm = mg solute per L of water:

$$\frac{3.0 \ \text{mg}}{1 \ \text{L}} = 3.0 \ \text{ppm}$$

**Answer: 3.0 ppm.**

</details>

### Problem 14

Dissolving 0.20 mol of glucose in 0.80 kg of water (44.4 mol $\ce{H2O}$), find (a) the mole fraction of glucose and (b) the molality.

<details>
<summary><strong>Solution</strong></summary>

**(a) Mole fraction:**

$$X_{\text{glucose}} = \frac{0.20}{0.20 + 44.4} = \frac{0.20}{44.6} = 0.0045$$

**(b) Molality** (mol solute per kg solvent):

$$m = \frac{0.20 \ \text{mol}}{0.80 \ \text{kg}} = 0.25 \ m$$

**Answer: $X_{\text{glucose}} = 0.0045$; molality = 0.25 m.**

</details>

### Problem 15

You mix 100. mL of 0.20 M $\ce{NaCl}$ with 100. mL of 0.40 M $\ce{NaCl}$. What is the final $[\ce{NaCl}]$? (Assume volumes add.)

<details>
<summary><strong>Solution</strong></summary>

Total moles of $\ce{NaCl}$: $(0.20)(0.100) + (0.40)(0.100) = 0.020 + 0.040 = 0.060 \ \text{mol}$.

Total volume: $100 + 100 = 200. \ \text{mL} = 0.200 \ \text{L}$.

$$M = \frac{0.060 \ \text{mol}}{0.200 \ \text{L}} = 0.30 \ M$$

**Answer: 0.30 M** — the concentration-weighted average, which lands between 0.20 and 0.40 as expected.

</details>

---

## Quick Reference

| Quantity | Formula / Rule | Notes |
|---|---|---|
| Molarity | $M = \dfrac{\text{mol solute}}{\text{L solution}}$ | The AP concentration unit; **L of solution, not solvent** |
| Moles from molarity | $n = M \times V$ | $V$ in liters |
| Grams needed | grams → moles → $M \times V$ | Convert grams to moles *first* |
| Dilution | $M_1 V_1 = M_2 V_2$ | Moles frozen; only volume changes |
| Per-ion concentration | $[\text{ion}] = (\text{coefficient}) \times M_{\text{salt}}$ | Write the dissociation first |
| Dissociation (example) | $\ce{CaCl2 -> Ca^2+ + 2Cl-}$ | 0.10 M → $[\ce{Cl-}] = 0.20$ M |
| Particle diagram | more dots = more concentrated (equal volume) | Keep ion ratios correct (2:1, 3:1, ...) |
| Mole fraction | $X_A = \dfrac{n_A}{n_{\text{total}}}$ | Unitless; all fractions sum to 1 |
| Molality | $m = \dfrac{\text{mol solute}}{\text{kg solvent}}$ | Per **kg solvent**; colligative properties |
| Mass percent | $\dfrac{\text{mass solute}}{\text{mass solution}} \times 100\%$ | — |
| ppm (dilute water) | mg solute per L water | Magnifying glass for tiny concentrations |
| Electrolyte | ions in solution → conducts | Ionic/strong acid = strong; sugar = non |

---

<div align="center">

[← Kinetic Molecular Theory](/chemistry/0505-kinetic-molecular-theory) | [Solubility and Separation →](/chemistry/0507-solubility-and-separation)

</div>
