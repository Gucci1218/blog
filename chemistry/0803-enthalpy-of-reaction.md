# Enthalpy of Reaction
<p class="article-date">July 5, 2026</p>

*I was digging through my backpack for a snack before practice and found a granola bar, and right there on the wrapper it said **190 Calories**. I've read that number a thousand times without ever thinking about it — but I just spent a whole unit on heat, so it finally clicked: that "190" is a chemistry measurement. It's literally how much energy your body releases when it "burns" that bar with the oxygen you breathe — the same combustion reaction you'd get from setting it on fire, just slower and wetter. And here's the wild part: a nutritionist actually measured it by burning food inside a calorimeter and watching the temperature climb. So the granola bar is a reactant, the oxygen in your lungs is the other reactant, and the Calories are the energy released — the **enthalpy of combustion**. Eat two bars and you get 380 Calories, exactly double, because energy scales with how much you burn. That single idea — heat is tied to amount, the way price is tied to quantity — is the whole heart of enthalpy of reaction, and it's where AP Unit 6 turns thermochemistry into something you can actually calculate.*

---

## What You'll Learn

- Define the **enthalpy of reaction** $\Delta H_{rxn}$ as the heat exchanged at constant pressure for a reaction *exactly as written*
- Apply the sign convention with confidence: **exothermic is negative**, **endothermic is positive** (carrying over from [Energy and Heat](/chemistry/0801-energy-and-heat))
- Write **thermochemical equations** — a balanced equation with its $\Delta H$ attached — and read the units correctly (kJ per reaction vs. kJ/mol)
- Understand why $\Delta H$ is **tied to the coefficients**: **double the equation → double $\Delta H$**, **reverse it → flip the sign**
- Use $\Delta H$ as a **stoichiometric conversion factor** to convert between grams/moles of a substance and kilojoules of heat — in *both* directions
- Run the full **mole map with an energy stop**: g ↔ mol ↔ kJ, the single biggest skill in this topic
- Recognize enthalpy as a **state function** (path-independent) and see why constant pressure makes $\Delta H = q_p$
- Compare **fuels and foods by energy per gram**, and connect a food "Calorie" (kcal) back to the chemistry calorie
- Name the common enthalpies — **combustion, solution, neutralization** — and know what each one measures

---

## Prerequisites

- [Energy and Heat](/chemistry/0801-energy-and-heat) — you need the meaning of enthalpy and the $\Delta H$ **sign convention** (exo −, endo +) cold; this whole article is that convention put to work
- [Stoichiometry](/chemistry/0603-stoichiometry) — enthalpy is a **stoichiometric quantity**, so the mole map (g → mol → mol → g) is about to grow one more stop: **kilojoules**. If mole ratios feel shaky, patch that first
- [Dimensional Analysis](/chemistry/0103-dimensional-analysis) — every calculation here is a railroad of unit fractions; if the units cancel to the thing you want, you're right

---

## The Core Concept

### Intuition First

Let's stay with the granola bar, because it secretly contains this entire article.

When you eat that bar, your cells run a slow, controlled version of this reaction (glucose is the stand-in for "food"):

$$\ce{C6H12O6(s) + 6O2(g) -> 6CO2(g) + 6H2O(l)}$$

That's **combustion** — fuel plus oxygen makes carbon dioxide and water and, crucially, **releases energy**. The wrapper's "190 Calories" is the size of that energy release. And notice the two ingredients map exactly onto our reaction: the **food is one reactant**, the **oxygen you breathe is the other reactant**, and the **Calories are the enthalpy released**.

Now here's the leap that makes enthalpy *calculable*. What happens if you eat **two** granola bars? You get **380 Calories** — exactly double. Nobody's surprised by that. But sit with why: energy scales with **how much stuff you burn**. Twice the fuel, twice the moles reacting, twice the heat. Enthalpy is an **extensive** quantity — it depends on *amount*, the same way the total price of boba depends on how many cups you order, not just the price per cup.

That's the one sentence to tattoo on your brain:

> **Heat released is proportional to amount reacted.** So $\Delta H$ behaves *exactly* like a conversion factor — a fixed number of kilojoules per mole — that you can multiply through a stoichiometry problem.

Map the snack onto the chemistry and it's one-to-one:

| Nutrition label | Chemistry |
|---|---|
| the granola bar | a **reactant** (fuel) |
| oxygen you breathe in | the other **reactant** |
| "190 Calories" released | the **enthalpy of combustion**, $\Delta H_{rxn}$ (energy out) |
| eating **two** bars → 380 Cal | $\Delta H$ **scales with amount** (extensive) |
| burning food in a calorimeter to get the number | how $\Delta H$ is *measured* (see [Calorimetry](/chemistry/0802-calorimetry)) |

Everything below is just making this table quantitative.

### What $\Delta H_{rxn}$ Actually Means

The **enthalpy of reaction**, written $\Delta H_{rxn}$, is the heat exchanged with the surroundings when a reaction runs **at constant pressure**, for the amounts shown in the **balanced equation as written**.

Two pieces of that definition earn their keep:

**"At constant pressure."** Almost every reaction you'll meet — in a beaker, in your stomach, on the lab bench — happens open to the atmosphere, so the pressure is just fixed at whatever the room is. Under that condition, the heat flow *is* the enthalpy change:

$$\Delta H = q_p$$

That's why enthalpy is the star of the unit: it's the version of energy that matches how real reactions actually run. (If you instead held the *volume* constant in a sealed bomb, you'd measure a slightly different quantity, internal energy — but AP centers on $\Delta H$.)

**"As written."** $\Delta H$ is glued to the specific coefficients of the equation you wrote down. Change the coefficients and you change $\Delta H$.

### The Sign Convention (recap from 0801)

Enthalpy is bookkeeping from the **system's** point of view:

| Type | What you feel/see | Sign of $\Delta H$ | Where energy goes |
|---|---|---|---|
| **Exothermic** | flask gets **hot**; heat pours out | $\Delta H < 0$ (**negative**) | system → surroundings |
| **Endothermic** | flask gets **cold**; heat is pulled in | $\Delta H > 0$ (**positive**) | surroundings → system |

Combustion — the granola bar, methane in a stove, propane in a grill — is exothermic, so its $\Delta H$ is **negative**. A negative sign means "energy left the system," i.e., was *released*. When a nutrition label says "190 Calories," a chemist writes that as $\Delta H = -190\ \text{Cal} = -794\ \text{kJ}$: the minus sign is the "released" part.

### Thermochemical Equations

A **thermochemical equation** is just a balanced equation with its enthalpy stapled on:

$$\ce{CH4(g) + 2O2(g) -> CO2(g) + 2H2O(l)} \qquad \Delta H = -890\ \text{kJ}$$

Read it out loud: "When **1 mol** $\ce{CH4}$ burns with **2 mol** $\ce{O2}$ to make **1 mol** $\ce{CO2}$ and **2 mol** $\ce{H2O}$, **890 kJ** of heat is released." The $-890\ \text{kJ}$ is **per mole of reaction as written** — meaning per the exact bundle of coefficients shown. Physical states $\ce{(g)}, \ce{(l)}, \ce{(s)}$ matter here: making liquid water releases more heat than making steam, so the states are part of the number.

**kJ vs. kJ/mol — a precision that trips everyone.** You'll see $\Delta H$ written two ways:

- **kJ (per reaction as written):** $-890\ \text{kJ}$ means "for this whole equation." If you doubled every coefficient, this number would double.
- **kJ/mol:** "per mole of a *specified* substance." Here it's $-890\ \text{kJ/mol}$ **of $\ce{CH4}$**, because the equation has 1 mol of $\ce{CH4}$. Always ask **"per mole of *what*?"** — per mole of $\ce{CO2}$ it's still $-890$, but per mole of $\ce{H2O}$ it's $-890/2 = -445\ \text{kJ}$.

### The Two Rules That Run Everything

Because $\Delta H$ is tied to the coefficients, only two moves matter:

**Rule 1 — Scaling: multiply the equation, multiply $\Delta H$ by the same factor.** Double the reaction, double the heat (eat two granola bars). Halve it, halve the heat.

$$\ce{2CH4(g) + 4O2(g) -> 2CO2(g) + 4H2O(l)} \qquad \Delta H = 2(-890) = -1780\ \text{kJ}$$

**Rule 2 — Reversing: flip the equation, flip the sign of $\Delta H$.** If forming water from its elements *releases* energy, then tearing water apart must *cost* that same energy back. Energy is conserved — you can't get a discount by going backward.

$$\ce{CO2(g) + 2H2O(l) -> CH4(g) + 2O2(g)} \qquad \Delta H = +890\ \text{kJ}$$

These two rules (scale, reverse) are the seed of **Hess's law**, coming in [0806](/chemistry/0806-hess-law).

### Enthalpy as a Stoichiometric Conversion Factor (the big skill)

Here's the payoff. Since $\Delta H$ is "so many kJ per so many moles," it's just **another ratio you can bolt onto the mole map**. Remember the stoichiometry railroad from [0603](/chemistry/0603-stoichiometry): grams ↔ moles ↔ (mole ratio) ↔ moles. Now we add a final stop — **kilojoules**:

$$
\underbrace{\text{grams of substance}}_{\text{weigh it}}
\;\xrightarrow[\text{molar mass}]{\div}\;
\underbrace{\text{moles of substance}}_{}
\;\xrightarrow[\text{from the thermochemical eqn}]{\times \frac{\Delta H}{\text{coeff}}}\;
\underbrace{\text{kilojoules of heat}}_{\text{the answer}}
$$

The new conversion factor comes straight off the thermochemical equation:

$$\frac{\Delta H\ (\text{kJ})}{\text{moles of that substance in the equation}}$$

For methane, that factor is $\dfrac{-890\ \text{kJ}}{1\ \text{mol}\ \ce{CH4}}$. Multiply moles of $\ce{CH4}$ by it and moles cancel, leaving kJ. And because it's just a ratio, it runs **both directions**: given kJ, flip the factor to find moles (then grams). That's the entire game.

### The Named Enthalpies (one quick orientation)

Chemists give $\Delta H$ a first name based on *what kind of change* it measures. They all obey the exact same rules above — these are just labels for common reactions:

| Name | What reacts | Symbol | Example |
|---|---|---|---|
| **Enthalpy of combustion** | 1 mol fuel burns completely in $\ce{O2}$ | $\Delta H_{comb}$ | the granola bar; $\ce{CH4} + 2\ce{O2} \to \ce{CO2} + 2\ce{H2O}$ |
| **Enthalpy of solution** | 1 mol solute dissolves | $\Delta H_{soln}$ | an instant cold pack: $\ce{NH4NO3(s) -> NH4+(aq) + NO3-(aq)}$ (endothermic) |
| **Enthalpy of neutralization** | acid + base make water | $\Delta H_{neut}$ | $\ce{HCl + NaOH -> NaCl + H2O}$ (exothermic) |

The nutrition-label number is specifically a **molar enthalpy of combustion** — how much heat one mole (or gram) of food releases when fully burned. We'll meet a very special named enthalpy — the enthalpy of *formation* — in [0805](/chemistry/0805-enthalpy-of-formation).

---

## Worked Examples

I'll round molar masses to two decimals. Watch the units cancel — they're your error-checker.

### Example 1: Reading a Thermochemical Equation

**Problem:** For $\ce{2H2(g) + O2(g) -> 2H2O(l)},\ \Delta H = -572\ \text{kJ}$, is this exothermic or endothermic, and how much heat is released per mole of $\ce{H2}$ burned?

**Solution:**

$\Delta H$ is negative → **exothermic** (heat released). The $-572\ \text{kJ}$ is for the equation as written, which burns **2 mol** $\ce{H2}$. Per mole of $\ce{H2}$:

$$\frac{-572\ \text{kJ}}{2\ \text{mol}\ \ce{H2}} = -286\ \text{kJ/mol}\ \ce{H2}$$

**Answer:** Exothermic; $-286\ \text{kJ}$ per mole of $\ce{H2}$. (Always anchor "per mole of *what*.")

### Example 2: Scaling a Reaction

**Problem:** Given $\ce{N2(g) + 3H2(g) -> 2NH3(g)},\ \Delta H = -92\ \text{kJ}$, find $\Delta H$ for $\ce{3N2(g) + 9H2(g) -> 6NH3(g)}$.

**Solution:**

The second equation is the first multiplied by **3** (check: $\ce{N2}$ went 1→3). By Rule 1, multiply $\Delta H$ by 3:

$$\Delta H = 3 \times (-92\ \text{kJ}) = -276\ \text{kJ}$$

**Answer:** $-276\ \text{kJ}$.

### Example 3: Reversing a Reaction

**Problem:** The formation of ammonia has $\Delta H = -92\ \text{kJ}$ (Example 2). What is $\Delta H$ for the *decomposition* $\ce{2NH3(g) -> N2(g) + 3H2(g)}$?

**Solution:**

This is the original equation run **backward**, same coefficients. By Rule 2, flip the sign:

$$\Delta H = +92\ \text{kJ}$$

**Answer:** $+92\ \text{kJ}$ (endothermic — you must *pay* energy to rip $\ce{NH3}$ apart, exactly what you got out when it formed).

### Example 4: Scale AND Reverse Together

**Problem:** Given $\ce{2SO2(g) + O2(g) -> 2SO3(g)},\ \Delta H = -198\ \text{kJ}$, find $\Delta H$ for $\ce{SO3(g) -> SO2(g) + 1/2 O2(g)}$.

**Solution:** Two moves. First **halve** the original (divide coefficients by 2): $\Delta H = -198/2 = -99\ \text{kJ}$ for $\ce{2SO2 + O2 -> 2SO3}$ becoming $\ce{SO2 + 1/2 O2 -> SO3}$. Then **reverse** it (we want $\ce{SO3}$ decomposing): flip the sign.

$$\Delta H = -(-99\ \text{kJ}) = +99\ \text{kJ}$$

**Answer:** $+99\ \text{kJ}$.

### Example 5: Heat from a Given Number of Moles

**Problem:** For $\ce{CH4(g) + 2O2(g) -> CO2(g) + 2H2O(l)},\ \Delta H = -890\ \text{kJ}$, how much heat is released when **0.500 mol** of $\ce{CH4}$ burns?

**Solution:** Use $\Delta H$ as a conversion factor. The equation has 1 mol $\ce{CH4}$ per $-890\ \text{kJ}$:

$$0.500\ \text{mol}\ \ce{CH4} \times \frac{-890\ \text{kJ}}{1\ \text{mol}\ \ce{CH4}} = -445\ \text{kJ}$$

**Answer:** $-445\ \text{kJ}$ (445 kJ released).

### Example 6: Heat from a Given Mass (the flagship: g → mol → kJ)

**Problem:** Propane burns in a grill: $\ce{C3H8(g) + 5O2(g) -> 3CO2(g) + 4H2O(l)},\ \Delta H = -2220\ \text{kJ}$. How much heat is released when **22.0 g** of propane burns completely?

**Solution:** Run the railroad — grams to moles, then moles to kJ.

**Step 1 — g → mol.** Molar mass $\ce{C3H8} = 3(12.01) + 8(1.008) = 44.09\ \text{g/mol}$.

**Step 2 — mol → kJ** using the factor $\dfrac{-2220\ \text{kJ}}{1\ \text{mol}\ \ce{C3H8}}$:

$$22.0\ \text{g}\ \ce{C3H8} \times \frac{1\ \text{mol}}{44.09\ \text{g}} \times \frac{-2220\ \text{kJ}}{1\ \text{mol}\ \ce{C3H8}} = -1108\ \text{kJ}$$

**Answer:** $\approx -1110\ \text{kJ}$ (about 1110 kJ released). Every unit except kJ cancels — that's your proof the chain is right.

### Example 7: Mass of Fuel Needed for a Target Heat (running it backward)

**Problem:** Using the propane reaction ($\Delta H = -2220\ \text{kJ}$), what mass of propane must burn to release **555 kJ** of heat?

**Solution:** Now we start from kJ and go *backward* to grams: kJ → mol → g. Flip the enthalpy factor so kJ cancels.

$$555\ \text{kJ} \times \frac{1\ \text{mol}\ \ce{C3H8}}{2220\ \text{kJ}} \times \frac{44.09\ \text{g}}{1\ \text{mol}} = 11.0\ \text{g}\ \ce{C3H8}$$

(I used 555 kJ as the magnitude released; the reaction's $\Delta H$ supplies the "2220 kJ per mole" ratio.)

**Answer:** $11.0\ \text{g}$ of propane.

### Example 8: Heat Absorbed by an Endothermic Reaction

**Problem:** The decomposition of limestone is endothermic: $\ce{CaCO3(s) -> CaO(s) + CO2(g)},\ \Delta H = +178\ \text{kJ}$. How much heat must be supplied to decompose **50.0 g** of $\ce{CaCO3}$?

**Solution:** Same railroad; the positive sign just means heat goes *in*. $\ce{CaCO3} = 40.08 + 12.01 + 3(16.00) = 100.09\ \text{g/mol}$.

$$50.0\ \text{g} \times \frac{1\ \text{mol}}{100.09\ \text{g}} \times \frac{+178\ \text{kJ}}{1\ \text{mol}\ \ce{CaCO3}} = +88.9\ \text{kJ}$$

**Answer:** $+88.9\ \text{kJ}$ must be absorbed (supplied).

### Example 9: Heat Released Per Gram (comparing fuels)

**Problem:** Compare methane ($\ce{CH4}$, $\Delta H = -890\ \text{kJ/mol}$) and propane ($\ce{C3H8}$, $\Delta H = -2220\ \text{kJ/mol}$) on a **per-gram** basis. Which packs more energy per gram?

**Solution:** Convert each "per mole" to "per gram" by dividing by molar mass.

*Methane* ($16.04\ \text{g/mol}$): $\dfrac{890\ \text{kJ}}{16.04\ \text{g}} = 55.5\ \text{kJ/g}$.

*Propane* ($44.09\ \text{g/mol}$): $\dfrac{2220\ \text{kJ}}{44.09\ \text{g}} = 50.4\ \text{kJ/g}$.

**Answer:** Methane wins at **55.5 kJ/g** vs propane's 50.4 kJ/g. Propane releases more *per mole* only because each molecule is bigger — per gram, lighter methane edges ahead. (This is exactly the "energy density" nutritionists and rocket engineers care about.)

### Example 10: The Granola Bar in a Calorimeter

**Problem:** A nutrition lab burns a **25.0 g** granola bar and finds it releases **794 kJ** of heat. (a) Express this in food Calories. (b) The label says "190 Calories" — does the measurement match?

**Solution:**

**(a)** A food **Calorie** (capital C) is a **kilocalorie** = 1000 chemistry calories, and $1\ \text{cal} = 4.184\ \text{J}$, so $1\ \text{Cal} = 4.184\ \text{kJ}$.

$$794\ \text{kJ} \times \frac{1\ \text{Cal}}{4.184\ \text{kJ}} = 190\ \text{Cal}$$

**(b)** It matches the label's **190 Calories** exactly. That "190" on the wrapper *is* a $\Delta H_{combustion}$ — measured by literally burning the bar in a calorimeter (see [Calorimetry](/chemistry/0802-calorimetry)) and watching a known mass of water heat up.

**Answer:** (a) $190\ \text{Cal}$; (b) yes — the label number is the combustion enthalpy in disguise.

### Example 11: Sugar — From Calories on the Label to Moles Reacted

**Problem:** Glucose combusts by $\ce{C6H12O6(s) + 6O2(g) -> 6CO2(g) + 6H2O(l)},\ \Delta H = -2803\ \text{kJ}$. A teaspoon of sugar is about **4.0 g**. How many **food Calories** does it deliver?

**Solution:** g → mol → kJ → Cal. $\ce{C6H12O6} = 6(12.01) + 12(1.008) + 6(16.00) = 180.16\ \text{g/mol}$.

$$4.0\ \text{g} \times \frac{1\ \text{mol}}{180.16\ \text{g}} \times \frac{2803\ \text{kJ}}{1\ \text{mol}} = 62.2\ \text{kJ}$$

$$62.2\ \text{kJ} \times \frac{1\ \text{Cal}}{4.184\ \text{kJ}} = 14.9\ \text{Cal}$$

**Answer:** About **15 Calories** per teaspoon — right in line with the ~16 Cal you'll see quoted for sugar. The mole map runs straight from "grams on a spoon" to "Calories on a label."

### Example 12: Two-Substance Bookkeeping

**Problem:** For $\ce{2C8H18(l) + 25O2(g) -> 16CO2(g) + 18H2O(l)},\ \Delta H = -10940\ \text{kJ}$ (octane, a gasoline component), how much heat is released per mole of $\ce{CO2}$ produced?

**Solution:** The equation makes **16 mol** $\ce{CO2}$ per $-10940\ \text{kJ}$:

$$\frac{-10940\ \text{kJ}}{16\ \text{mol}\ \ce{CO2}} = -683.8\ \text{kJ/mol}\ \ce{CO2}$$

**Answer:** $-684\ \text{kJ}$ per mole of $\ce{CO2}$. The enthalpy factor can be built from *any* substance in the equation — pick the one the question names.

### Example 13: Enthalpy as a State Function

**Problem:** You can turn carbon into $\ce{CO2}$ two ways: **(Path A)** burn it directly, $\ce{C(s) + O2(g) -> CO2(g)},\ \Delta H = -394\ \text{kJ}$; or **(Path B)** first make $\ce{CO}$, $\ce{C(s) + 1/2 O2(g) -> CO(g)},\ \Delta H = -111\ \text{kJ}$, then burn that, $\ce{CO(g) + 1/2 O2(g) -> CO2(g)},\ \Delta H = -283\ \text{kJ}$. Compare the total for each path.

**Solution:**

*Path A:* $-394\ \text{kJ}$.

*Path B:* $-111 + (-283) = -394\ \text{kJ}$.

**Answer:** Identical, $-394\ \text{kJ}$. Enthalpy is a **state function** — it depends only on the **start** ($\ce{C} + \ce{O2}$) and **end** ($\ce{CO2}$) states, not the route between them. That's the whole idea behind Hess's law ([0806](/chemistry/0806-hess-law)): if two roads share the same endpoints, they cost the same total enthalpy. (You can't "burn carbon the long way" to squeeze out extra energy — energy bookkeeping always balances.)

---

## Common Mistakes

| The mistake | Why it happens | How to avoid it |
|---|---|---|
| Forgetting to scale $\Delta H$ when you scale the equation | You change coefficients but leave $\Delta H$ alone | $\Delta H$ is glued to the coefficients — multiply it by the **same** factor |
| Not flipping the **sign** when reversing a reaction | Reversing feels like it shouldn't change the number | Reverse ⇒ flip sign. Forward-exo becomes backward-endo, every time |
| Losing the sign entirely (dropping the −) | "Released" and "absorbed" feel like just words | Keep the sign in every step; − means out, + means in. A missing sign is a wrong answer on the AP |
| Confusing **kJ** with **kJ/mol** | The two look similar and both appear | Ask **"per mole of *what*?"** — kJ/mol needs a named substance |
| Trying to go **grams → kJ directly** | Grams feel like the natural unit | You must pass through **moles** first; the $\Delta H$ factor is per *mole* |
| Building the enthalpy factor with the wrong coefficient | You grab "1 mol" out of habit | Use the coefficient of the substance the problem gives, straight from the balanced equation |
| Mixing up food **Calorie** and chemistry **calorie** | Same word, 1000× apart | Capital-C Calorie = kcal = 1000 cal = 4.184 kJ |
| Ignoring physical **states** $\ce{(l)}$ vs $\ce{(g)}$ | They look like decoration | Making liquid water vs. steam gives different $\Delta H$ — states are part of the number |

---

## AP Exam Tips

- **$\Delta H$ scales with coefficients and flips on reversal.** These two rules power almost every Unit 6 enthalpy question and set up Hess's law. Double the equation → double $\Delta H$; reverse it → change the sign. Practice until it's automatic.
- **Use $\Delta H$ exactly like a mole-ratio conversion factor.** A thermochemical equation gives you "$X$ kJ per $n$ mol of substance." Drop that fraction into the mole map and let units cancel — g → mol → kJ forward, or kJ → mol → g backward.
- **Be ruthless about "per mole of what."** $-890\ \text{kJ}$ for methane combustion is per mole of $\ce{CH4}$ *and* per mole of $\ce{CO2}$, but per mole of $\ce{H2O}$ it's half that. Free-response graders check this.
- **Sign discipline is worth points.** Carry the + or − through every line. A negative $\Delta H$ means exothermic/heat-released; a bare positive number where a negative belongs loses credit even if the magnitude is right.
- **Show units at every railroad step.** A labeled chain (g → mol → kJ) earns work-shown credit even if the final arithmetic slips. A naked string of numbers does not.
- **State-function preview.** If a problem hints that "the value doesn't depend on the path," that's the state-function property — the doorway to Hess's law ([0806](/chemistry/0806-hess-law)) and formation enthalpies ([0805](/chemistry/0805-enthalpy-of-formation)). Remember $\Delta H = q_p$: enthalpy is the constant-pressure heat.

---

## Practice Problems

Round molar masses to two decimals. Keep the sign of $\Delta H$ in every step. Use $1\ \text{Cal} = 4.184\ \text{kJ}$ when needed.

### Problem 1
For $\ce{2H2(g) + O2(g) -> 2H2O(l)},\ \Delta H = -572\ \text{kJ}$, is the reaction exothermic or endothermic, and does the flask get hot or cold?

<details>
<summary><strong>Solution</strong></summary>

$\Delta H < 0$ → **exothermic**; heat flows out, so the flask (and surroundings) gets **hot**.

**Answer:** Exothermic; the flask gets hot.

</details>

---

### Problem 2
Given $\ce{C(s) + O2(g) -> CO2(g)},\ \Delta H = -394\ \text{kJ}$, find $\Delta H$ for $\ce{2C(s) + 2O2(g) -> 2CO2(g)}$.

<details>
<summary><strong>Solution</strong></summary>

Equation is doubled → multiply $\Delta H$ by 2 (Rule 1):

$$\Delta H = 2(-394) = -788\ \text{kJ}$$

**Answer:** $-788\ \text{kJ}$.

</details>

---

### Problem 3
The synthesis $\ce{N2(g) + 3H2(g) -> 2NH3(g)}$ has $\Delta H = -92\ \text{kJ}$. Find $\Delta H$ for $\ce{2NH3(g) -> N2(g) + 3H2(g)}$.

<details>
<summary><strong>Solution</strong></summary>

Reverse the reaction → flip the sign (Rule 2):

$$\Delta H = +92\ \text{kJ}$$

**Answer:** $+92\ \text{kJ}$ (now endothermic).

</details>

---

### Problem 4
For $\ce{CH4(g) + 2O2(g) -> CO2(g) + 2H2O(l)},\ \Delta H = -890\ \text{kJ}$, how much heat is released when **3.00 mol** of $\ce{CH4}$ burns?

<details>
<summary><strong>Solution</strong></summary>

$$3.00\ \text{mol}\ \ce{CH4} \times \frac{-890\ \text{kJ}}{1\ \text{mol}\ \ce{CH4}} = -2670\ \text{kJ}$$

**Answer:** $-2670\ \text{kJ}$ (2670 kJ released).

</details>

---

### Problem 5
Using the methane reaction above ($\Delta H = -890\ \text{kJ}$), how much heat is released when **8.00 g** of $\ce{CH4}$ burns?

<details>
<summary><strong>Solution</strong></summary>

$\ce{CH4} = 16.04\ \text{g/mol}$.

$$8.00\ \text{g} \times \frac{1\ \text{mol}}{16.04\ \text{g}} \times \frac{-890\ \text{kJ}}{1\ \text{mol}} = -444\ \text{kJ}$$

**Answer:** $\approx -444\ \text{kJ}$.

</details>

---

### Problem 6
Propane: $\ce{C3H8(g) + 5O2(g) -> 3CO2(g) + 4H2O(l)},\ \Delta H = -2220\ \text{kJ}$. What mass of propane must burn to release **4440 kJ**?

<details>
<summary><strong>Solution</strong></summary>

$4440\ \text{kJ}$ is exactly $2 \times 2220$, so **2 mol** propane. $\ce{C3H8} = 44.09\ \text{g/mol}$:

$$4440\ \text{kJ} \times \frac{1\ \text{mol}}{2220\ \text{kJ}} \times \frac{44.09\ \text{g}}{1\ \text{mol}} = 88.2\ \text{g}$$

**Answer:** $88.2\ \text{g}$ of propane.

</details>

---

### Problem 7
For the endothermic decomposition $\ce{CaCO3(s) -> CaO(s) + CO2(g)},\ \Delta H = +178\ \text{kJ}$, how much heat is needed to decompose **200.0 g** of $\ce{CaCO3}$?

<details>
<summary><strong>Solution</strong></summary>

$\ce{CaCO3} = 100.09\ \text{g/mol}$.

$$200.0\ \text{g} \times \frac{1\ \text{mol}}{100.09\ \text{g}} \times \frac{+178\ \text{kJ}}{1\ \text{mol}} = +356\ \text{kJ}$$

**Answer:** $+356\ \text{kJ}$ absorbed.

</details>

---

### Problem 8
For $\ce{2SO2(g) + O2(g) -> 2SO3(g)},\ \Delta H = -198\ \text{kJ}$, what is $\Delta H$ for $\ce{2SO3(g) -> 2SO2(g) + O2(g)}$?

<details>
<summary><strong>Solution</strong></summary>

Same coefficients, run backward → flip sign:

$$\Delta H = +198\ \text{kJ}$$

**Answer:** $+198\ \text{kJ}$.

</details>

---

### Problem 9
Glucose combustion: $\ce{C6H12O6(s) + 6O2(g) -> 6CO2(g) + 6H2O(l)},\ \Delta H = -2803\ \text{kJ}$. How much heat is released when **90.0 g** of glucose is metabolized?

<details>
<summary><strong>Solution</strong></summary>

$\ce{C6H12O6} = 180.16\ \text{g/mol}$.

$$90.0\ \text{g} \times \frac{1\ \text{mol}}{180.16\ \text{g}} \times \frac{-2803\ \text{kJ}}{1\ \text{mol}} = -1400\ \text{kJ}$$

**Answer:** $\approx -1400\ \text{kJ}$.

</details>

---

### Problem 10
A candy bar lists **240 Calories**. Convert that combustion enthalpy to kilojoules, with the correct sign.

<details>
<summary><strong>Solution</strong></summary>

Combustion is exothermic (energy released), so the sign is negative:

$$240\ \text{Cal} \times \frac{4.184\ \text{kJ}}{1\ \text{Cal}} = 1004\ \text{kJ} \;\Rightarrow\; \Delta H = -1004\ \text{kJ}$$

**Answer:** $\Delta H \approx -1000\ \text{kJ}$ (about $-1.00 \times 10^3\ \text{kJ}$).

</details>

---

### Problem 11
Ethanol burns: $\ce{C2H5OH(l) + 3O2(g) -> 2CO2(g) + 3H2O(l)},\ \Delta H = -1367\ \text{kJ}$. Find the heat released **per gram** of ethanol ($46.07\ \text{g/mol}$).

<details>
<summary><strong>Solution</strong></summary>

$$\frac{1367\ \text{kJ}}{46.07\ \text{g}} = 29.7\ \text{kJ/g}$$

**Answer:** $\approx 29.7\ \text{kJ/g}$ released. (Less energy-dense than propane's 50 kJ/g — one reason gasoline out-punches ethanol per gram.)

</details>

---

### Problem 12
Hydrogen is proposed as a clean fuel: $\ce{2H2(g) + O2(g) -> 2H2O(l)},\ \Delta H = -572\ \text{kJ}$. How much heat is released when **10.0 g** of $\ce{H2}$ burns?

<details>
<summary><strong>Solution</strong></summary>

$\ce{H2} = 2.016\ \text{g/mol}$. Factor: $-572\ \text{kJ}$ per **2 mol** $\ce{H2}$.

$$10.0\ \text{g} \times \frac{1\ \text{mol}}{2.016\ \text{g}} \times \frac{-572\ \text{kJ}}{2\ \text{mol}\ \ce{H2}} = -1419\ \text{kJ}$$

**Answer:** $\approx -1420\ \text{kJ}$. (That's ~142 kJ/g — hydrogen is the champ per gram, which is why rockets love it.)

</details>

---

### Problem 13
For octane $\ce{2C8H18(l) + 25O2(g) -> 16CO2(g) + 18H2O(l)},\ \Delta H = -10940\ \text{kJ}$, how much heat is released per mole of $\ce{H2O}$ formed?

<details>
<summary><strong>Solution</strong></summary>

The equation makes **18 mol** $\ce{H2O}$ per $-10940\ \text{kJ}$:

$$\frac{-10940\ \text{kJ}}{18\ \text{mol}\ \ce{H2O}} = -607.8\ \text{kJ/mol}\ \ce{H2O}$$

**Answer:** $\approx -608\ \text{kJ}$ per mole of $\ce{H2O}$.

</details>

---

### Problem 14
A peanut ($\approx 0.60\ \text{g}$ of fat/oil, treat as releasing $38\ \text{kJ/g}$ when burned) is combusted under a can of water in a classic lab. How many **kilojoules** and how many **food Calories** does it release?

<details>
<summary><strong>Solution</strong></summary>

$$0.60\ \text{g} \times 38\ \text{kJ/g} = 22.8\ \text{kJ}$$

$$22.8\ \text{kJ} \times \frac{1\ \text{Cal}}{4.184\ \text{kJ}} = 5.4\ \text{Cal}$$

**Answer:** $\approx 23\ \text{kJ} \approx 5.4\ \text{Calories}$ — a single peanut is a few food Calories, exactly the calorimetry idea behind a nutrition label.

</details>

---

### Problem 15
Given $\ce{C(s) + 1/2 O2(g) -> CO(g)},\ \Delta H = -111\ \text{kJ}$ and $\ce{CO(g) + 1/2 O2(g) -> CO2(g)},\ \Delta H = -283\ \text{kJ}$, what is $\Delta H$ for the direct reaction $\ce{C(s) + O2(g) -> CO2(g)}$, and what principle lets you add them?

<details>
<summary><strong>Solution</strong></summary>

The two steps start at $\ce{C} + \ce{O2}$ and end at $\ce{CO2}$, so add their enthalpies:

$$\Delta H = -111 + (-283) = -394\ \text{kJ}$$

This works because **enthalpy is a state function** — the total depends only on start and end states, not the path (Hess's law).

**Answer:** $-394\ \text{kJ}$; justified by enthalpy being a state function.

</details>

---

## Quick Reference

| Concept | Rule / Formula |
|---|---|
| **Enthalpy of reaction** | $\Delta H_{rxn}$ = heat at constant pressure for the equation *as written* |
| **Constant pressure** | $\Delta H = q_p$ |
| **Sign convention** | exothermic $\Delta H < 0$ (heat out); endothermic $\Delta H > 0$ (heat in) |
| **Scaling (Rule 1)** | multiply equation by $n$ → multiply $\Delta H$ by $n$ |
| **Reversing (Rule 2)** | reverse equation → flip sign of $\Delta H$ |
| **Enthalpy factor** | $\dfrac{\Delta H\ (\text{kJ})}{\text{mol of substance in equation}}$ |
| **Mole map + energy** | g $\xrightarrow{\div\text{MM}}$ mol $\xrightarrow{\times\frac{\Delta H}{\text{coeff}}}$ kJ (runs both ways) |
| **kJ vs kJ/mol** | kJ = whole reaction; kJ/mol = per mole of a *named* substance |
| **State function** | $\Delta H$ depends only on start/end states, not path (→ Hess's law) |
| **Energy per gram** | $\dfrac{|\Delta H|}{\text{molar mass}}$ = fuel/food energy density |
| **Food Calorie** | $1\ \text{Cal} = 1\ \text{kcal} = 1000\ \text{cal} = 4.184\ \text{kJ}$ |
| **Named enthalpies** | combustion (burn in $\ce{O2}$), solution (dissolve), neutralization (acid + base) |

---

<div align="center">

[← Calorimetry](/chemistry/0802-calorimetry) | [Bond Enthalpies →](/chemistry/0804-bond-enthalpies)

</div>
