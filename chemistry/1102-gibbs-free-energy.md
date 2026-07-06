# Gibbs Free Energy
<p class="article-date">July 5, 2026</p>

*Last weekend I bought a pint of mint chip and completely forgot it on the counter while I got sucked into a movie. Two hours later it was a sad green puddle. But here's the thing that got me: the exact same pint, sitting in the freezer three feet away, would have stayed rock solid for months. Same substance, opposite fates — and the only difference was the temperature of the room it was sitting in. Melting is a tug-of-war between two urges: one urge wants the water molecules to stay locked in tidy, low-energy solid crystals (that's **enthalpy**, and it favors staying frozen), and the other urge wants them to break loose and spread out into a sloppy, disordered liquid (that's **entropy**, and it favors melting). On a hot counter the entropy side wins; in the freezer the enthalpy side wins. Temperature is the referee that decides how loud the entropy side gets to shout. And Gibbs free energy, $\Delta G = \Delta H - T\Delta S$, is the exact scoreboard for that tug-of-war — its sign tells you which way the process actually wants to go. This one little equation is the crown jewel of AP Unit 9: it's how chemists predict, before mixing a single thing, whether a reaction will run at all.*

---

## What You'll Learn

- State the **Gibbs free energy** equation $\Delta G = \Delta H - T\Delta S$ and explain what each term is doing in the tug-of-war
- Handle the two classic unit traps cold: **$\Delta H$ is in kJ, $\Delta S$ is in J**, and **$T$ must be in kelvin**
- Interpret the sign of $\Delta G$: **negative = thermodynamically favorable (spontaneous)**, positive = unfavorable (favorable in reverse), zero = equilibrium
- Nail the crucial distinction that **"favorable" does not mean "fast"**
- Classify any reaction into one of the **four sign cases** ($\Delta H$ vs. $\Delta S$) and say when it's favorable
- Solve $\Delta G = 0$ for the **crossover temperature** $T = \Delta H / \Delta S$ where favorability flips
- Compute $\Delta G^\circ$ **two ways** — from $\Delta H^\circ$ and $\Delta S^\circ$, and from **standard free energies of formation** $\Delta G_f^\circ$
- Explain **thermodynamic vs. kinetic control** — why a favorable reaction (like diamond turning to graphite) can still be immeasurably slow

---

## Prerequisites

- [Entropy](/chemistry/1101-entropy) — you need $\Delta S$, the measure of disorder, and its sign rules; it's one whole side of the tug-of-war
- [Enthalpy of Reaction](/chemistry/0803-enthalpy-of-reaction) — $\Delta H$ is the other side; you need its sign convention (exothermic −, endothermic +) cold
- [Enthalpy of Formation](/chemistry/0805-enthalpy-of-formation) — the "products − reactants, elements = 0" trick reappears exactly for free energies of formation
- [Collision Model and Arrhenius](/chemistry/0704-collision-model-arrhenius) — activation energy is why a favorable reaction can still be slow; it's the key to thermodynamic vs. kinetic control

---

## The Core Concept

### Intuition First

Let's stay with the melting pint, because it secretly contains this entire article.

When ice cream (basically frozen water plus sugar and fat) melts, two "urges" are fighting each other:

- **The enthalpy urge.** Molecules in a solid are held together by attractions — hydrogen bonds between water molecules, and so on. Breaking those to melt costs energy, so melting is **endothermic**: $\Delta H > 0$. Enthalpy *hates* melting. It wants the molecules to stay in low-energy, tidy solid bonds. **The enthalpy pull points toward freezing (order).**
- **The entropy urge.** A liquid is far more disordered than a solid — molecules can slide, tumble, and roam. Spreading out into a liquid is a huge jump in disorder, so melting has $\Delta S > 0$. Entropy *loves* melting. **The entropy pull points toward the disordered liquid.**

So who wins? That's where the referee walks in. Look at the scoreboard equation:

$$\Delta G = \Delta H - T\Delta S$$

Notice that the entropy term is multiplied by temperature $T$. **Temperature is the referee that decides how much the entropy pull counts.** On a hot counter, $T$ is large, so the $T\Delta S$ term is large — the entropy side shouts loud enough to overpower enthalpy, $\Delta G$ goes negative, and the ice cream melts. In the freezer, $T$ is small, so $T\Delta S$ is small — enthalpy wins the shouting match, $\Delta G$ stays positive, and it stays solid.

Here's the one-to-one map — tape this to your brain:

| Tug-of-war | Symbol | What it wants |
|---|---|---|
| Enthalpy pull | $\Delta H$ | low energy / order (freezing) |
| Entropy pull | $T\Delta S$ | disorder (melting) |
| The referee | $T$ | how loud the entropy side gets to shout |
| Who wins | sign of $\Delta G$ | **negative = the process happens** |

That's the whole idea. Gibbs free energy is just the enthalpy pull minus the (temperature-weighted) entropy pull, and its sign announces the winner.

### The Formula and the Sign of ΔG

$$\Delta G = \Delta H - T\Delta S \qquad\qquad \Delta G^\circ = \Delta H^\circ - T\Delta S^\circ$$

The little "$^\circ$" (naught) just means **standard conditions** (1 atm, 1 M solutions, usually 298 K). The word **free** in "free energy" means the energy that's actually *free to do useful work* — the rest gets lost to the entropy term.

The sign of $\Delta G$ is the entire payoff:

| $\Delta G$ | Meaning | Nickname |
|---|---|---|
| $\Delta G < 0$ | **Thermodynamically favorable** — proceeds as written | "spontaneous" |
| $\Delta G > 0$ | Unfavorable as written — **favorable in reverse** | "nonspontaneous" |
| $\Delta G = 0$ | Forward and reverse balanced | **equilibrium** |

> **Spontaneous ≠ fast.** In chemistry, "spontaneous" (favorable) only means the reaction is *downhill in free energy* — it has no comment on speed. A favorable reaction can take a microsecond or a billion years. Hold onto that; it's the whole point of Section 9.4 below.

### The Four Cases (The AP Sign Table)

Because $\Delta G = \Delta H - T\Delta S$, and $T$ is always positive (kelvin), the signs of $\Delta H$ and $\Delta S$ set up four possibilities:

| Case | $\Delta H$ | $\Delta S$ | $\Delta G = \Delta H - T\Delta S$ | Favorable? |
|---|---|---|---|---|
| **1** | $-$ (exo) | $+$ (disorder ↑) | $(-) - T(+) =$ always negative | **Always favorable** (any $T$) |
| **2** | $+$ (endo) | $-$ (disorder ↓) | $(+) - T(-) =$ always positive | **Never favorable** (any $T$) |
| **3** | $-$ (exo) | $-$ (disorder ↓) | negative only if $T$ is small | Favorable at **LOW $T$** |
| **4** | $+$ (endo) | $+$ (disorder ↑) | negative only if $T$ is large | Favorable at **HIGH $T$** |

Melting ice cream is **Case 4**: endothermic ($\Delta H > 0$) and more disordered ($\Delta S > 0$), so it only becomes favorable once the temperature is high enough — exactly why it melts on the counter but not in the freezer.

A memory trick: in Cases 1 and 2, $\Delta H$ and $\Delta S$ *agree* on the answer (both push the same way), so temperature can't change the verdict. In Cases 3 and 4, they *disagree*, so temperature is the tiebreaker — and there's a specific temperature where the tie flips.

### The Crossover Temperature

For the "it depends" cases (3 and 4), there's a threshold temperature where $\Delta G = 0$ — the moment the tug-of-war is perfectly balanced. Set $\Delta G = 0$ and solve:

$$0 = \Delta H - T\Delta S \quad\Longrightarrow\quad \boxed{\,T = \dfrac{\Delta H}{\Delta S}\,}$$

That $T$ is the **crossover** (or "flip") temperature. For melting, it's literally the melting point. Below it one side wins; above it the other side wins. This is how chemists find the exact temperature a decomposition, a boiling, or a phase change becomes favorable.

### Computing ΔG° from Free Energies of Formation

There's a second, table-based route that skips $\Delta H$ and $\Delta S$ entirely. Just like enthalpy of formation, every compound has a tabulated **standard free energy of formation** $\Delta G_f^\circ$ (kJ/mol), and:

$$\Delta G^\circ_{rxn} = \sum n\,\Delta G_f^\circ(\text{products}) - \sum n\,\Delta G_f^\circ(\text{reactants})$$

Same rules as [enthalpy of formation](/chemistry/0805-enthalpy-of-formation): weight each by its coefficient $n$, and **elements in their standard states have $\Delta G_f^\circ = 0$.** Products minus reactants — that's it.

---

## Worked Examples

### Example 1: The Basic ΔG Calculation (with the unit trap)

**Problem:** For a reaction at 298 K, $\Delta H^\circ = -92.2$ kJ and $\Delta S^\circ = -198.7$ J/K. Find $\Delta G^\circ$ and state whether it's favorable.

**Solution:**

**Step 1 — Fix the units first.** $\Delta H$ is in **kJ**, $\Delta S$ is in **J**. Convert $\Delta S$ to kJ:
$$\Delta S^\circ = -198.7 \text{ J/K} = -0.1987 \text{ kJ/K}$$

**Step 2 — Plug in ($T$ already in kelvin):**
$$\Delta G^\circ = \Delta H^\circ - T\Delta S^\circ = (-92.2) - (298)(-0.1987)$$
$$\Delta G^\circ = -92.2 + 59.2 = -33.0 \text{ kJ}$$

**Step 3 — Read the sign.** Negative.

**Answer:** $\Delta G^\circ = -33.0$ kJ; since it's **negative, the reaction is thermodynamically favorable** at 298 K.

---

### Example 2: Forgetting to Convert — See the Damage

**Problem:** Using the same numbers as Example 1, what wrong answer do you get if you *forget* to convert $\Delta S$ from J to kJ?

**Solution:** Plugging $\Delta S = -198.7$ (leaving it in J) directly:
$$\Delta G = -92.2 - (298)(-198.7) = -92.2 + 59{,}213 = +59{,}121$$

You'd get a huge **positive** number and conclude the reaction is unfavorable — the *opposite* of the truth. The entropy term is off by a factor of 1000, so it steamrolls everything.

**Answer:** You flip the verdict entirely. **Always convert $\Delta S$ to kJ (÷1000) before subtracting.** This is the single most common $\Delta G$ error on the AP exam.

---

### Example 3: Classifying — Case 1 (always favorable)

**Problem:** Combustion of propane, $\ce{C3H8(g) + 5O2(g) -> 3CO2(g) + 4H2O(g)}$, is exothermic and produces more gas molecules (6 → 7). At what temperatures is it favorable?

**Solution:**

- $\Delta H < 0$ (exothermic — combustion releases heat).
- $\Delta S > 0$ (7 mol gas from 6 mol gas → more disorder).
- $\Delta G = (-) - T(+) =$ negative minus positive = **always negative**.

**Answer:** **Case 1 — favorable at all temperatures.** Both urges push the same way, so temperature never changes the verdict. (Whether it's *fast* is a separate question — see Example 11.)

---

### Example 4: Classifying — Case 2 (never favorable)

**Problem:** Consider $\ce{3O2(g) -> 2O3(g)}$ (ozone formation), which is endothermic and decreases gas moles (3 → 2). When is it favorable?

**Solution:**

- $\Delta H > 0$ (endothermic).
- $\Delta S < 0$ (3 mol gas → 2 mol gas, less disorder).
- $\Delta G = (+) - T(-) = (+) + (\text{positive}) =$ **always positive**.

**Answer:** **Case 2 — never favorable** at any temperature (it's favorable in the reverse direction). Both urges oppose the forward reaction, so no temperature can rescue it.

---

### Example 5: Classifying — Case 3 (favorable at low T)

**Problem:** Freezing water, $\ce{H2O(l) -> H2O(s)}$, releases heat and lowers disorder. When is it favorable?

**Solution:**

- $\Delta H < 0$ (freezing is exothermic — the reverse of melting).
- $\Delta S < 0$ (liquid → solid is more ordered).
- $\Delta G = (-) - T(-) = (-) + T(\ldots)$: the $-T\Delta S$ term is *positive* and grows with $T$. Only when $T$ is **small** does the negative $\Delta H$ win.

**Answer:** **Case 3 — favorable at LOW temperature.** Water freezes in the freezer (low $T$), not on the counter. This is the exact mirror image of the ice-cream story.

---

### Example 6: Classifying — Case 4 (the ice-cream case, favorable at high T)

**Problem:** Melting ice cream, $\ce{H2O(s) -> H2O(l)}$, absorbs heat and raises disorder. When is it favorable?

**Solution:**

- $\Delta H > 0$ (melting is endothermic).
- $\Delta S > 0$ (solid → liquid is more disordered).
- $\Delta G = (+) - T(+)$: the $-T\Delta S$ term is negative and grows with $T$. Only when $T$ is **large** does it overpower the positive $\Delta H$.

**Answer:** **Case 4 — favorable at HIGH temperature.** Melts on the warm counter, stays solid in the freezer. Referee $T$ decides. This is our opening story in one line.

---

### Example 7: Finding the Crossover Temperature (melting point)

**Problem:** For melting a certain solid, $\Delta H^\circ = +6.01$ kJ/mol and $\Delta S^\circ = +22.0$ J/(mol·K). Above what temperature does melting become favorable?

**Solution:**

**Step 1 — Convert units.** $\Delta S = 22.0$ J/K $= 0.0220$ kJ/K.

**Step 2 — Set $\Delta G = 0$ and solve for $T$:**
$$T = \frac{\Delta H}{\Delta S} = \frac{6.01 \text{ kJ}}{0.0220 \text{ kJ/K}} = 273 \text{ K}$$

**Step 3 — Interpret.** This is Case 4, favorable at high $T$. So melting is favorable **above** 273 K.

**Answer:** $T = 273 \text{ K} = 0\,^\circ\text{C}$ — the melting point of ice, exactly. Above it, ice melts; below it, water freezes.

---

### Example 8: Crossover for a Decomposition Reaction

**Problem:** Limestone decomposes: $\ce{CaCO3(s) -> CaO(s) + CO2(g)}$, with $\Delta H^\circ = +178$ kJ and $\Delta S^\circ = +161$ J/K. Above what temperature is decomposition favorable?

**Solution:**

**Step 1 — Convert:** $\Delta S = 161$ J/K $= 0.161$ kJ/K.

**Step 2 — Crossover:**
$$T = \frac{\Delta H}{\Delta S} = \frac{178}{0.161} = 1106 \text{ K}$$

**Step 3 — Interpret.** $\Delta H > 0$ and $\Delta S > 0$ is Case 4 → favorable at high $T$.

**Answer:** Favorable **above ≈ 1106 K** ($\approx 833\,^\circ\text{C}$). This is exactly why industrial lime kilns run blisteringly hot — below that temperature the reaction simply won't go.

---

### Example 9: ΔG° from ΔH° and ΔS° at a Non-Standard Temperature

**Problem:** A reaction has $\Delta H^\circ = +131$ kJ and $\Delta S^\circ = +134$ J/K. Find $\Delta G$ at (a) 298 K and (b) 1200 K.

**Solution:** Convert $\Delta S = 0.134$ kJ/K.

**(a) At 298 K:**
$$\Delta G = 131 - (298)(0.134) = 131 - 39.9 = +91.1 \text{ kJ} \;\Rightarrow\; \text{unfavorable}$$

**(b) At 1200 K:**
$$\Delta G = 131 - (1200)(0.134) = 131 - 160.8 = -29.8 \text{ kJ} \;\Rightarrow\; \text{favorable}$$

**Answer:** Unfavorable at 298 K ($+91.1$ kJ), favorable at 1200 K ($-29.8$ kJ). The verdict flipped because $T$ crossed the crossover point ($T = 131/0.134 \approx 978$ K).

---

### Example 10: ΔG° from Free Energies of Formation

**Problem:** Compute $\Delta G^\circ$ for $\ce{2CO(g) + O2(g) -> 2CO2(g)}$ given $\Delta G_f^\circ$: $\ce{CO} = -137.2$ kJ/mol, $\ce{CO2} = -394.4$ kJ/mol.

**Solution:**

**Step 1 — Elements are zero.** $\ce{O2}$ is an element in its standard state, so $\Delta G_f^\circ(\ce{O2}) = 0$.

**Step 2 — Products − reactants, weighted by coefficients:**
$$\Delta G^\circ = \underbrace{[2(-394.4)]}_{\text{products}} - \underbrace{[2(-137.2) + 1(0)]}_{\text{reactants}}$$
$$\Delta G^\circ = (-788.8) - (-274.4) = -514.4 \text{ kJ}$$

**Answer:** $\Delta G^\circ = -514.4$ kJ — strongly **favorable**, which fits: $\ce{CO}$ burning to $\ce{CO2}$ is very downhill.

---

### Example 11: Thermodynamically Favorable but Kinetically Frozen

**Problem:** For $\ce{C(diamond) -> C(graphite)}$, $\Delta G^\circ = -2.9$ kJ. So why do diamonds last "forever"?

**Solution:** $\Delta G^\circ$ is negative, so converting diamond to graphite **is thermodynamically favorable** — graphite is genuinely the more stable form. But favorability only tells us the *direction*, not the *speed*. Rearranging every carbon atom in the rigid diamond lattice requires breaking extremely strong C–C bonds, which means an enormous **activation energy** (from [Collision Model and Arrhenius](/chemistry/0704-collision-model-arrhenius)). At room temperature essentially no molecules have enough energy to get over that barrier.

**Answer:** The reaction is favorable ($\Delta G < 0$) but under **kinetic control** — the rate is effectively zero because $E_a$ is huge. "Diamonds are forever" is a story about *kinetics*, not thermodynamics.

---

### Example 12: Combustion Needs a Spark

**Problem:** Gasoline–air combustion has a large negative $\Delta G$, yet a puddle of gasoline sits in air all day without bursting into flame. Why does it need a spark?

**Solution:** The reaction is wildly favorable, so thermodynamics says "go." But the reactant molecules must first collide with enough energy to clear the **activation-energy barrier**. At room temperature, almost none do, so the rate is negligible. A spark delivers a jolt of energy that pushes a batch of molecules over $E_a$; the heat they release then pushes their neighbors over, and it becomes self-sustaining.

**Answer:** Combustion is **thermodynamically favorable but kinetically blocked** by $E_a$ until a spark provides the initial activation energy. Once again: **favorable tells you *whether*; kinetics tells you *how fast*.**

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Leaving $\Delta S$ in **J** while $\Delta H$ is in **kJ** | The table hands you mixed units | **Always ÷ 1000** on $\Delta S$ (J → kJ) *before* subtracting. Circle the units. |
| Using **°C** instead of **K** for $T$ | Temperature feels like °C in daily life | Convert: $T(\text{K}) = T(^\circ\text{C}) + 273$. $T$ is *always* kelvin. |
| Thinking **favorable = fast** | "Spontaneous" sounds like "immediate" | $\Delta G$ is about *direction/extent* only. Speed lives in Unit 5 (kinetics, $E_a$). |
| Assuming temperature never matters | Only memorizing "$\Delta G<0$ = good" | Cases 3 & 4 flip with $T$; find the crossover $T = \Delta H/\Delta S$. |
| Flipping the formation formula | Confusing which is subtracted | It's **products − reactants**, same as $\Delta H_f^\circ$. |
| Forgetting **elements = 0** | Trying to look up $\Delta G_f^\circ$ of $\ce{O2}$, $\ce{N2}$ | Elements in standard states have $\Delta G_f^\circ = 0$; drop them. |
| Sign error on $-T\Delta S$ when $\Delta S<0$ | Two negatives | $-T\times(\text{negative}) = +$; it *adds* to $\Delta G$. |

---

## AP Exam Tips

- **Units are graded.** The number-one calculation error is the $\Delta H$(kJ)/$\Delta S$(J) mismatch, closely followed by using °C instead of K. Fix units *first*, every time.
- **Memorize the four-case table.** "$\Delta H<0, \Delta S>0$ → always favorable" and its three siblings show up as free multiple-choice points and as FRQ justification.
- **Crossover temperature.** If asked "above/below what temperature is this favorable?", set $\Delta G = 0$ and use $T = \Delta H / \Delta S$ (with $\Delta S$ in kJ/K). Then use the case to decide whether it's *above* or *below*.
- **Favorable ≠ fast.** Expect at least one conceptual question where a reaction has $\Delta G < 0$ but doesn't proceed — the answer is a **high activation energy / kinetic control** (tie it back to Unit 5). Say the words "activation energy."
- **$\Delta G_f^\circ$ route.** When a table of $\Delta G_f^\circ$ is given, use $\Delta G^\circ = \sum n\Delta G_f^\circ(\text{prod}) - \sum n\Delta G_f^\circ(\text{react})$ — **products − reactants, elements = 0.** Don't waste time going through $\Delta H$ and $\Delta S$.
- **Show the setup.** On FRQs, writing $\Delta G = \Delta H - T\Delta S$ with numbers plugged in earns setup points even if arithmetic slips.
- **Sign, then sentence.** After computing $\Delta G$, always write a sentence: "negative, so the reaction is thermodynamically favorable." The interpretation is worth a point.

---

## Practice Problems

### Problem 1
At 298 K, a reaction has $\Delta H^\circ = -46.2$ kJ and $\Delta S^\circ = -389$ J/K. Compute $\Delta G^\circ$ and state whether it is favorable.

<details>
<summary><strong>Solution</strong></summary>

Convert: $\Delta S = -0.389$ kJ/K.
$$\Delta G = -46.2 - (298)(-0.389) = -46.2 + 115.9 = +69.7 \text{ kJ}$$

**Answer:** $\Delta G^\circ = +69.7$ kJ — **positive, so unfavorable** at 298 K (favorable in reverse).

</details>

---

### Problem 2
A reaction has $\Delta H^\circ = +58$ kJ and $\Delta S^\circ = +176$ J/K. Find $\Delta G$ at 298 K.

<details>
<summary><strong>Solution</strong></summary>

$\Delta S = 0.176$ kJ/K.
$$\Delta G = 58 - (298)(0.176) = 58 - 52.4 = +5.6 \text{ kJ}$$

**Answer:** $+5.6$ kJ — just barely **unfavorable** at 298 K. (It becomes favorable a little above room temperature.)

</details>

---

### Problem 3
Classify each by case number and say when it's favorable:
(a) $\Delta H<0, \Delta S>0$ (b) $\Delta H>0, \Delta S>0$ (c) $\Delta H<0, \Delta S<0$ (d) $\Delta H>0, \Delta S<0$

<details>
<summary><strong>Solution</strong></summary>

- (a) **Case 1** — always favorable.
- (b) **Case 4** — favorable at high $T$.
- (c) **Case 3** — favorable at low $T$.
- (d) **Case 2** — never favorable.

</details>

---

### Problem 4
The reaction $\ce{2H2(g) + O2(g) -> 2H2O(l)}$ is exothermic and goes from 3 mol gas to 0 mol gas. Which case is it, and is it favorable at room temperature?

<details>
<summary><strong>Solution</strong></summary>

$\Delta H < 0$ (exothermic); $\Delta S < 0$ (gas → liquid, big drop in disorder). That's **Case 3 — favorable at low $T$.** Room temperature is low enough here (the strongly negative $\Delta H$ dominates), so yes, $\Delta G < 0$ and it's **favorable** at 298 K.

**Answer:** Case 3; favorable at room temperature.

</details>

---

### Problem 5
For a phase change, $\Delta H^\circ = +40.7$ kJ/mol and $\Delta S^\circ = +109$ J/(mol·K). Find the temperature at which $\Delta G = 0$.

<details>
<summary><strong>Solution</strong></summary>

$\Delta S = 0.109$ kJ/K.
$$T = \frac{\Delta H}{\Delta S} = \frac{40.7}{0.109} = 373 \text{ K}$$

**Answer:** $T = 373 \text{ K} = 100\,^\circ\text{C}$ — the boiling point of water. (This is the vaporization of water.)

</details>

---

### Problem 6
Using Problem 5's data, is boiling favorable at 350 K? At 400 K?

<details>
<summary><strong>Solution</strong></summary>

This is Case 4 (both positive) → favorable above the crossover, 373 K.

- 350 K < 373 K → **unfavorable** (water stays liquid).
- 400 K > 373 K → **favorable** (water boils to vapor).

Check at 400 K: $\Delta G = 40.7 - (400)(0.109) = 40.7 - 43.6 = -2.9$ kJ ✓ (negative).

**Answer:** Unfavorable at 350 K, favorable at 400 K.

</details>

---

### Problem 7
Compute $\Delta G^\circ$ for $\ce{N2(g) + 3H2(g) -> 2NH3(g)}$ given $\Delta G_f^\circ(\ce{NH3}) = -16.4$ kJ/mol.

<details>
<summary><strong>Solution</strong></summary>

$\ce{N2}$ and $\ce{H2}$ are elements → $\Delta G_f^\circ = 0$.
$$\Delta G^\circ = 2(-16.4) - [0 + 3(0)] = -32.8 \text{ kJ}$$

**Answer:** $-32.8$ kJ — **favorable** at standard conditions.

</details>

---

### Problem 8
Compute $\Delta G^\circ$ for $\ce{CH4(g) + 2O2(g) -> CO2(g) + 2H2O(l)}$ given $\Delta G_f^\circ$ (kJ/mol): $\ce{CH4}=-50.8$, $\ce{CO2}=-394.4$, $\ce{H2O(l)}=-237.1$.

<details>
<summary><strong>Solution</strong></summary>

$\ce{O2}$ is an element → 0.
$$\Delta G^\circ = [(-394.4) + 2(-237.1)] - [(-50.8) + 2(0)]$$
$$= (-868.6) - (-50.8) = -817.8 \text{ kJ}$$

**Answer:** $\Delta G^\circ = -817.8$ kJ — strongly **favorable** (methane combustion).

</details>

---

### Problem 9
A reaction is thermodynamically favorable ($\Delta G^\circ = -210$ kJ) but no observable reaction occurs when the reactants are mixed at room temperature. Give a chemistry-correct explanation.

<details>
<summary><strong>Solution</strong></summary>

Favorability ($\Delta G < 0$) only describes the *direction/extent*, not the *rate*. The reaction must be under **kinetic control**: it has a **high activation energy**, so at room temperature almost no molecules have enough energy to react, and the rate is immeasurably slow. Adding a catalyst or raising the temperature could speed it up without changing $\Delta G$.

**Answer:** High $E_a$ → kinetically controlled → slow, even though it's thermodynamically favorable.

</details>

---

### Problem 10
For $\ce{2NO2(g) -> N2O4(g)}$: $\Delta H^\circ = -57.2$ kJ, $\Delta S^\circ = -175.8$ J/K. Below what temperature is dimerization favorable?

<details>
<summary><strong>Solution</strong></summary>

Both negative → Case 3 (favorable at low $T$). Crossover:
$$T = \frac{\Delta H}{\Delta S} = \frac{-57.2}{-0.1758} = 325 \text{ K}$$

Case 3 → favorable **below** 325 K.

**Answer:** Favorable below ≈ 325 K ($\approx 52\,^\circ\text{C}$).

</details>

---

### Problem 11
Recompute $\Delta G$ for the reaction in Problem 10 at 400 K and confirm the verdict.

<details>
<summary><strong>Solution</strong></summary>

$$\Delta G = -57.2 - (400)(-0.1758) = -57.2 + 70.3 = +13.1 \text{ kJ}$$

Positive → **unfavorable**, consistent with 400 K being *above* the 325 K crossover.

**Answer:** $+13.1$ kJ, unfavorable at 400 K. ✓

</details>

---

### Problem 12
A student computes $\Delta G = -92.2 - (298)(-198.7) = +59{,}121$ and concludes a reaction is unfavorable. Find and fix the error.

<details>
<summary><strong>Solution</strong></summary>

The student left $\Delta S$ in **J/K** instead of converting to **kJ/K**. Correct it: $\Delta S = -0.1987$ kJ/K.
$$\Delta G = -92.2 - (298)(-0.1987) = -92.2 + 59.2 = -33.0 \text{ kJ}$$

**Answer:** The real answer is $-33.0$ kJ — **favorable.** The unit slip flipped the entire verdict.

</details>

---

### Problem 13
For $\ce{CaCO3(s) -> CaO(s) + CO2(g)}$, explain using $\Delta S$ why heating (high $T$) is needed to make decomposition favorable.

<details>
<summary><strong>Solution</strong></summary>

The reaction produces a gas ($\ce{CO2}$) from a solid, so $\Delta S > 0$ (disorder increases). It's also endothermic ($\Delta H > 0$). That's **Case 4** — the $-T\Delta S$ term only overpowers the positive $\Delta H$ once $T$ is large. So decomposition is favorable **only at high temperature** (above the crossover $T = \Delta H/\Delta S$).

**Answer:** Both $\Delta H$ and $\Delta S$ are positive (Case 4), so only a large $T$ makes $\Delta G < 0$.

</details>

---

### Problem 14
A reaction has $\Delta G^\circ = 0$ at 500 K. What does this tell you about the system, and what is $\Delta H^\circ$ in terms of $\Delta S^\circ$?

<details>
<summary><strong>Solution</strong></summary>

$\Delta G = 0$ means the forward and reverse processes are balanced — the system is at **equilibrium** (neither direction is favored). From $0 = \Delta H - T\Delta S$:
$$\Delta H^\circ = T\Delta S^\circ = 500\,\Delta S^\circ$$

**Answer:** At 500 K the system is at equilibrium, and $\Delta H^\circ = (500\text{ K})\Delta S^\circ$.

</details>

---

### Problem 15
Rank these by *whether temperature can change the verdict*: (a) exothermic + gas produced, (b) endothermic + gas consumed, (c) endothermic + gas produced.

<details>
<summary><strong>Solution</strong></summary>

- (a) $\Delta H<0, \Delta S>0$ → **Case 1**, always favorable — temperature *cannot* change it.
- (b) $\Delta H>0, \Delta S<0$ → **Case 2**, never favorable — temperature *cannot* change it.
- (c) $\Delta H>0, \Delta S>0$ → **Case 4**, favorable only at high $T$ — temperature *is* the deciding factor.

**Answer:** Only (c) is temperature-dependent; (a) and (b) are locked regardless of $T$.

</details>

---

## Quick Reference

| Concept | Rule |
|---|---|
| **Master equation** | $\Delta G = \Delta H - T\Delta S$ (standard: $\Delta G^\circ = \Delta H^\circ - T\Delta S^\circ$) |
| **Unit trap #1** | $\Delta H$ in **kJ**, $\Delta S$ in **J** — convert $\Delta S$ ÷ 1000 to kJ first |
| **Unit trap #2** | $T$ is **always kelvin**: $T(\text{K}) = T(^\circ\text{C}) + 273$ |
| **$\Delta G < 0$** | Thermodynamically **favorable** (spontaneous) |
| **$\Delta G > 0$** | Unfavorable (favorable in reverse) |
| **$\Delta G = 0$** | **Equilibrium** |
| **Case 1** ($-,+$) | Favorable at **all** temperatures |
| **Case 2** ($+,-$) | **Never** favorable |
| **Case 3** ($-,-$) | Favorable at **low** $T$ |
| **Case 4** ($+,+$) | Favorable at **high** $T$ (the melting case) |
| **Crossover $T$** | $T = \dfrac{\Delta H}{\Delta S}$ (set $\Delta G = 0$) |
| **From formation** | $\Delta G^\circ = \sum n\Delta G_f^\circ(\text{prod}) - \sum n\Delta G_f^\circ(\text{react})$; elements $= 0$ |
| **Favorable ≠ fast** | $\Delta G$ = direction/extent; speed = kinetics (activation energy) |

---

<div align="center">

[← Entropy](/chemistry/1101-entropy) | [Free Energy and Equilibrium →](/chemistry/1103-free-energy-equilibrium)

</div>
