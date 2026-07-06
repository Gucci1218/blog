# Energy, Heat, and Enthalpy Direction
<p class="article-date">July 5, 2026</p>

*I went to my little brother's soccer game last winter and stuffed two things in my jacket pocket: an instant cold pack, in case someone twisted an ankle, and a hand warmer, because the metal bleachers were freezing. Halfway through, a kid went down on a bad tackle, so I cracked the cold pack — squeezed it, felt the little pouch inside pop, shook it — and within seconds it turned icy in my hand, sucking the warmth right out of my fingers. At the same time I shook the hand warmer in my other pocket, and it slowly turned toasty. Two little packs, opposite personalities. One PULLS heat out of your skin; the other PUSHES heat into it. And here's the part that melted my brain: from the pack's point of view, everything is backwards from what your hand feels. The cold pack feels cold to you because it's greedily absorbing your heat — the pack is gaining energy while you're losing it. This is the whole idea behind Topics 6.1–6.3: energy has a direction, heat always flows from hot to cold, and whether a process is **endothermic** or **exothermic** depends entirely on whose point of view you take. Get the point of view right, and thermochemistry stops being a sign-error minefield.*

---

## What You'll Learn

- Define the **system** and the **surroundings**, and explain why the universe = system + surroundings once you draw the boundary
- Distinguish **kinetic** from **potential** energy at the molecular level, and separate the three words students always blur: **thermal energy**, **temperature**, and **heat**
- State the **first-law preview** ($\ce{\Delta}E = q + w$) and explain why AP Chemistry keeps the spotlight on heat, $q$
- Assign the **sign of $q$ from the SYSTEM's perspective**: exothermic ($q < 0$, surroundings warm), endothermic ($q > 0$, surroundings cool) — and never again be fooled by "feels cold"
- Connect **enthalpy** $H$ and $\ce{\Delta}H$ to heat at constant pressure ($\ce{\Delta}H = q_p$), and read a $\ce{\Delta}H$ sign as endo or exo
- **Classify everyday processes** — dissolving, combustion, melting, freezing, evaporation, condensation, photosynthesis — as endothermic or exothermic and give the $\ce{\Delta}H$ sign
- **Read and label an energy diagram**: reactant and product energy levels, and $\ce{\Delta}H$ as the drop or rise between them
- Predict the **direction of heat flow** (always hot → cold) and identify which object warms and which cools on the way to **thermal equilibrium**
- Explain why thermal equilibrium means **equal temperatures**, not equal heat, and how "heat lost = heat gained" sets up calorimetry

---

## Prerequisites

- [Phase Changes](/chemistry/0503-phase-changes) — you already watched energy pour into ice to melt it and out of steam to condense it; melting, boiling, freezing, and condensing are the cleanest endothermic/exothermic examples there are, and this article gives them their signs
- [Collision Model and Arrhenius](/chemistry/0704-collision-model-arrhenius) — you drew reaction **energy profiles** with an activation-energy hump; here we reuse the exact same diagram but stop obsessing over the hump and stare at the **reactant-to-product drop or rise**, which is $\ce{\Delta}H$

---

## The Core Concept

### Intuition First

Let's stay in my jacket pocket, because both packs are hiding in there and they're a perfect matched pair.

**The pack is the SYSTEM. Your hand is the SURROUNDINGS.** The very first decision in every thermochemistry problem is where you draw the imaginary line — the **boundary** — between the thing you're studying and everything else. For the cold pack, "the system" is the chemicals inside the pouch. "The surroundings" is your skin, the air, the bleacher — everything outside that boundary. Draw that line and you've split the universe into exactly two pieces: **universe = system + surroundings.** Energy that leaves one has to show up in the other. It can't vanish.

**The cold pack PULLS heat in — it's endothermic.** Inside that pack is solid ammonium nitrate and a little water pouch. Crack it and the $\ce{NH4NO3}$ dissolves:

$$\ce{NH4NO3(s) ->[H2O] NH4+(aq) + NO3-(aq)}$$

Pulling those ions apart costs energy, and the pack pays for it by grabbing thermal energy from the nearest source — your hand. So heat flows **INTO the system** from you. The pack is *gaining* energy; your skin is *losing* it. Because you're the one losing heat, **you feel cold.** From the pack's point of view, it's the winner here — it's soaking up energy. This is **endothermic**: the system absorbs heat, and its surroundings (you) cool down.

**The hand warmer PUSHES heat out — it's exothermic.** Inside a hand warmer is iron powder that slowly rusts once air gets in:

$$\ce{4Fe(s) + 3O2(g) -> 2Fe2O3(s)}$$

Forming those iron-oxygen bonds *releases* energy, and that energy has nowhere to go but out — into your hand and the cold air. Heat flows **OUT of the system** into you. The pack is *losing* energy; your skin is *gaining* it. Because you're the one gaining heat, **you feel warm.** This is **exothermic**: the system releases heat, and its surroundings warm up.

**Here's the "backwards" trick that trips up literally everyone.** When something feels cold, your instinct screams "cold = losing heat." But *you're* the one losing heat, not the pack. The pack is doing the opposite of what you feel. So the rule to burn into your memory:

> **Feels cold → the system is ABSORBING heat from you → endothermic ($q > 0$ for the system).**
> **Feels warm → the system is RELEASING heat to you → exothermic ($q < 0$ for the system).**

You always feel it *backwards* from the system's sign. That single sentence is the most tested idea in Unit 6.

### Energy, at the molecular level

Zoom into the molecules and there are only two kinds of energy to track:

- **Kinetic energy (KE)** — the energy of *motion*. Molecules fly, spin, and vibrate. Faster motion = more KE. This is the energy of "how hot is it."
- **Potential energy (PE)** — the energy *stored in position and bonds*. Two atoms held in a bond, or two ions clinging together in a crystal, sit at some stored-energy level, like a ball perched on a shelf. Breaking that arrangement or building a new one changes the PE.

A chemical reaction is really just a bookkeeping swap between these two. When bonds rearrange, stored **potential** energy gets converted into (or out of) the **kinetic** energy of motion — and kinetic energy of motion is exactly what we sense as temperature.

### Three words people blur: thermal energy, temperature, heat

These are NOT the same thing, and the AP exam loves punishing students who treat them as synonyms.

| Word | What it actually is | Everyday feel |
|---|---|---|
| **Temperature** | The **average** kinetic energy of the particles (callback to [KMT, 0505](/chemistry/0505-kinetic-molecular-theory)) | "How hot is one particle, on average?" |
| **Thermal energy** | The **total** kinetic energy of *all* the particles added up | A bathtub of warm water has more thermal energy than a boiling teaspoon |
| **Heat ($q$)** | Energy **transferred** because of a temperature *difference* | Not something an object "has" — something that *flows* |

The killer distinction: **a teaspoon of boiling water is at a higher temperature than a warm bathtub, but the bathtub holds far more thermal energy** — because it has vastly more molecules. Temperature is an *average*; thermal energy is a *total*. And heat is neither — heat is energy *in transit*, and it only moves when there's a temperature gap.

### Heat, work, and a light first-law preview

There are two ways to move energy across the boundary:

- **Heat ($q$)** — energy transferred because of a temperature difference (the whole story of this unit).
- **Work ($w$)** — energy transferred by a push, most often a gas expanding or being compressed (a piston moving).

Add them up and you get the change in the system's total internal energy — the **first law of thermodynamics**:

$$\ce{\Delta}E = q + w$$

Energy is conserved: whatever the system gains as heat plus work, its internal energy goes up by exactly that. For AP Chemistry we keep this *light*. Almost every reaction we care about happens in an open beaker at constant pressure, where the work term is small and predictable — so we shift our attention almost entirely to $q$, the heat. That's what enthalpy is for.

### Enthalpy: heat with a name tag

**Enthalpy ($H$)** is a bookkeeping quantity defined so that, **at constant pressure**, its change equals the heat of the reaction:

$$\ce{\Delta}H = q_p$$

That subscript $p$ means "constant pressure." Since your beaker sits open to the room's constant atmospheric pressure, the heat you'd measure *is* $\ce{\Delta}H$. So enthalpy is just "the heat of the reaction" dressed up with a symbol — and it carries the same sign convention, from the **system's** point of view:

- $\ce{\Delta}H < 0$ (negative) → the system **releases** heat → **exothermic** → surroundings warm up
- $\ce{\Delta}H > 0$ (positive) → the system **absorbs** heat → **endothermic** → surroundings cool down

Hand warmer: $\ce{\Delta}H < 0$. Cold pack: $\ce{\Delta}H > 0$. (How you actually *calculate* a number for $\ce{\Delta}H$ — from calorimetry, bond energies, formation enthalpies, and Hess's law — is the whole rest of Unit 6. This article is only about getting the **direction** and the **sign** right. Forward links: [Calorimetry](/chemistry/0802-calorimetry), and bond-energy $\ce{\Delta}H$ in 0804.)

### Energy diagrams (Topic 6.2)

An energy diagram plots **potential energy on the y-axis** as a reaction moves from reactants (left) to products (right). You drew these back in [0704](/chemistry/0704-collision-model-arrhenius) with an activation-energy hump in the middle. Same diagram — but now ignore the hump and stare only at the **starting height vs. the ending height**. That difference is $\ce{\Delta}H$.

**Exothermic — products sit LOWER than reactants:**

```
 PE │  reactants
    │  ┌────┐
    │  │    │        ΔH < 0
    │  │    └────┐   (energy released)
    │  │         │
    │  │      products
    └──┴──────────────── reaction progress →
```

The system falls to a lower, more stable energy level, and the leftover energy is dumped into the surroundings as heat. $\ce{\Delta}H = H_{\text{products}} - H_{\text{reactants}} < 0$.

**Endothermic — products sit HIGHER than reactants:**

```
 PE │              products
    │           ┌────
    │      ┌────┘        ΔH > 0
    │  ┌───┘             (energy absorbed)
    │  │  reactants
    └──┴──────────────── reaction progress →
```

The system climbs to a higher energy level, and it had to pull that extra energy in from the surroundings. $\ce{\Delta}H = H_{\text{products}} - H_{\text{reactants}} > 0$.

Always compute $\ce{\Delta}H$ the same way — **products minus reactants**:

$$\ce{\Delta}H = H_{\text{products}} - H_{\text{reactants}}$$

Products lower → negative → exothermic. Products higher → positive → endothermic.

**Why bonds decide the direction (a preview).** Breaking bonds always *costs* energy (endothermic); forming bonds always *releases* energy (exothermic). A whole reaction is a tug-of-war between the two. If forming the new bonds releases more than breaking the old ones cost, energy comes out and the reaction is exothermic. If breaking costs more, energy goes in and it's endothermic. We'll turn that into actual numbers in **0804 (bond enthalpy)** — for now just hold the slogan: **breaking absorbs, forming releases.**

### Heat transfer and thermal equilibrium (Topic 6.3)

Two rules run everything here, and they're both things you already know from real life.

**Rule 1: Heat spontaneously flows from HOT to COLD. Never the reverse.** Drop a hot spoon into cold water and the spoon cools while the water warms. You have never once seen the spoon get hotter and the water get colder on its own. Energy flows *downhill* in temperature, exactly like water flows downhill in height.

**Rule 2: Flow stops at THERMAL EQUILIBRIUM — when the temperatures are EQUAL.** The hot object keeps handing energy to the cold one until there's no temperature gap left. At that point they're at the *same temperature*, and net heat flow stops.

Picture a hot metal block dropped into a beaker of cool water:

1. The block (hot) is the source; the water (cold) is the sink. Heat flows **block → water**.
2. The block **cools down**; the water **warms up**.
3. They meet in the middle at a single **final temperature** somewhere between the two starting temperatures.
4. At that final temperature the gap is zero, so net heat flow stops. That's thermal equilibrium.

**The trap: equal temperature does NOT mean equal energy.** At equilibrium the block and the water are at the *same temperature*, but they don't hold the *same amount of thermal energy* — that depends on how much of each substance there is and how "energy-thirsty" each one is (its heat capacity). Equilibrium equalizes temperature, not energy.

**Conservation — the bridge to calorimetry.** Because energy is conserved and (in an ideal insulated setup) none leaks out, every joule the hot object loses is a joule the cold object gains:

$$q_{\text{lost by hot}} = -\,q_{\text{gained by cold}}$$

The minus sign is that "backwards" idea again: one loses ($q<0$) exactly what the other gains ($q>0$). This single equation is the engine of **calorimetry** — measuring $\ce{\Delta}H$ by watching a temperature change. That's the next article: [Calorimetry](/chemistry/0802-calorimetry).

> **🎬 Hollywood Chemistry: Real or Not?**
> *The scene:* In survival movies, someone shivering in the snow cracks a chemical hand warmer and it instantly glows red-hot.
> *The verdict:* The chemistry is real — iron powder oxidizing ($\ce{4Fe + 3O2 -> 2Fe2O3}$) is genuinely exothermic and is exactly how commercial warmers work. But "instantly red-hot" is Hollywood. Real air-activated warmers top out around 55–65 °C (warm, not glowing) and take several minutes to ramp up, because the reaction is throttled by how fast oxygen can seep through the pouch. Exothermic, yes; dramatic fireball, no.

---

## Worked Examples

### Example 1: Classify dissolving ammonium nitrate

**Problem:** An instant cold pack works by dissolving $\ce{NH4NO3}$ in water, and the pack turns icy. Is the dissolving endothermic or exothermic? Give the sign of $q$ (for the system) and of $\ce{\Delta}H$.

**Solution:**
- Step 1: Identify the feel. The pack turns **cold**.
- Step 2: Apply the backwards rule. "Feels cold" means the system is *absorbing* heat from the surroundings (your hand), which cool.
- Step 3: Assign signs from the system's view. Absorbing heat → **endothermic**, $q > 0$, $\ce{\Delta}H > 0$.

**Answer:** Endothermic; $q > 0$ and $\ce{\Delta}H > 0$.

### Example 2: Classify combustion

**Problem:** Natural gas burns on a stove: $\ce{CH4(g) + 2O2(g) -> CO2(g) + 2H2O(g)}$, and the flame is hot. Endo or exo? Sign of $\ce{\Delta}H$?

**Solution:**
- Step 1: The surroundings (the pan, the air, your hand near the burner) get **hotter**.
- Step 2: If the surroundings warm up, the system is *releasing* heat.
- Step 3: Releasing heat → **exothermic**, $\ce{\Delta}H < 0$.

**Answer:** Exothermic; $\ce{\Delta}H < 0$. (Combustion is *always* exothermic — that's the whole point of a fuel.)

### Example 3: Melting ice

**Problem:** An ice cube melts on the kitchen counter. Take the ice as the system. Endo or exo, and what's the sign of $\ce{\Delta}H$?

**Solution:**
- Step 1: For ice to melt, energy has to flow *into* it — that's why melting ice cools your drink; it pulls heat from the drink.
- Step 2: System absorbs heat → **endothermic**.
- Step 3: $\ce{\Delta}H > 0$. (From [Phase Changes, 0503](/chemistry/0503-phase-changes): $\ce{H2O(s) -> H2O(l)}$ costs energy, the heat of fusion.)

**Answer:** Endothermic; $\ce{\Delta}H > 0$.

### Example 4: Freezing water

**Problem:** Water freezes into ice cubes in the freezer. Take the water as the system. Endo or exo? Sign of $\ce{\Delta}H$?

**Solution:**
- Step 1: Freezing is the *reverse* of melting: $\ce{H2O(l) -> H2O(s)}$.
- Step 2: To lock molecules into a rigid crystal, the water must *release* energy (that's the heat the freezer's coils carry away).
- Step 3: Releasing heat → **exothermic**, $\ce{\Delta}H < 0$.

**Answer:** Exothermic; $\ce{\Delta}H < 0$. Note it's the exact opposite sign of melting — reversing a process flips the sign of $\ce{\Delta}H$.

### Example 5: Evaporation vs. condensation

**Problem:** (a) Sweat evaporating off your skin after a run. (b) Steam condensing on a cold bathroom mirror. Classify each and give the $\ce{\Delta}H$ sign.

**Solution:**
- (a) Evaporation, $\ce{H2O(l) -> H2O(g)}$: pulling molecules apart into a gas *costs* energy, taken from your skin — which is exactly why sweating cools you. **Endothermic, $\ce{\Delta}H > 0$.**
- (b) Condensation, $\ce{H2O(g) -> H2O(l)}$: molecules coming together *release* energy into the mirror. **Exothermic, $\ce{\Delta}H < 0$.**

**Answer:** Evaporation endothermic ($\ce{\Delta}H > 0$); condensation exothermic ($\ce{\Delta}H < 0$). They're a reversed pair, so their signs are opposite.

### Example 6: Photosynthesis

**Problem:** Plants build glucose from carbon dioxide and water using sunlight: $\ce{6CO2 + 6H2O -> C6H12O6 + 6O2}$. Endo or exo? Sign of $\ce{\Delta}H$?

**Solution:**
- Step 1: The reaction only runs *because* the plant pumps in light energy — energy is being *absorbed*, stored in the glucose's bonds.
- Step 2: Absorbing energy → **endothermic**.
- Step 3: $\ce{\Delta}H > 0$. (This is why glucose is fuel: burning it later *reverses* this and releases that stored energy — respiration is exothermic.)

**Answer:** Endothermic; $\ce{\Delta}H > 0$.

### Example 7: Reading an energy diagram

**Problem:** On an energy diagram, the reactants sit at 150 kJ and the products sit at 90 kJ (both potential-energy levels). Is the reaction endo or exo, and what is $\ce{\Delta}H$?

**Solution:**
- Step 1: Use $\ce{\Delta}H = H_{\text{products}} - H_{\text{reactants}}$.
- Step 2: $\ce{\Delta}H = 90 - 150 = -60$ kJ.
- Step 3: Products are *lower* and $\ce{\Delta}H$ is negative → **exothermic**.

**Answer:** Exothermic, $\ce{\Delta}H = -60$ kJ.

### Example 8: Labeling ΔH on a diagram

**Problem:** A diagram shows reactants at 40 kJ, a transition-state peak at 120 kJ, and products at 100 kJ. Which arrow is $\ce{\Delta}H$, and what is its value and sign?

**Solution:**
- Step 1: $\ce{\Delta}H$ is the vertical gap between **reactants and products only** — ignore the 120 kJ peak (that's activation energy from [0704](/chemistry/0704-collision-model-arrhenius)).
- Step 2: $\ce{\Delta}H = H_{\text{products}} - H_{\text{reactants}} = 100 - 40 = +60$ kJ.
- Step 3: Products higher, $\ce{\Delta}H$ positive → **endothermic**.

**Answer:** $\ce{\Delta}H = +60$ kJ, endothermic. Draw the $\ce{\Delta}H$ arrow from the reactant level (40) up to the product level (100), *not* up to the peak.

### Example 9: Direction of heat flow

**Problem:** You drop a 300 °C steel bearing into a cup of 20 °C water. Which way does heat flow, which object warms, which cools, and where does it end up?

**Solution:**
- Step 1: Heat flows hot → cold, so **bearing → water**.
- Step 2: The bearing (source) **cools**; the water (sink) **warms**.
- Step 3: They stop exchanging when temperatures are equal — the final temperature lands somewhere **between 20 °C and 300 °C** (much closer to 20 °C, since there's far more water than steel).

**Answer:** Heat flows from bearing to water; the bearing cools, the water warms, and both settle at one common final temperature between 20 and 300 °C.

### Example 10: Thermal equilibrium — equal T, not equal energy

**Problem:** A tiny copper block at 90 °C is dropped into a large tub of water at 20 °C. At thermal equilibrium, is the block's temperature equal to the water's? Do they hold equal amounts of thermal energy?

**Solution:**
- Step 1: At equilibrium, net heat flow has stopped, which happens only when there's no temperature gap — so **temperatures are equal**.
- Step 2: Thermal energy is the *total* KE of all particles; the huge tub of water has vastly more particles than the little block.
- Step 3: Same temperature, but the water holds far more total thermal energy.

**Answer:** Temperatures are equal at equilibrium; thermal energies are **not** — the large water tub holds much more. Equilibrium equalizes temperature, not energy.

### Example 11: Conservation of heat

**Problem:** A hot rock loses 500 J of heat to the water it's dropped into, with no heat escaping to the room. How much heat does the water gain? Write the relationship.

**Solution:**
- Step 1: Energy is conserved and nothing leaks out, so heat lost by the rock = heat gained by the water.
- Step 2: In signed terms, $q_{\text{rock}} = -500$ J (it loses), so $q_{\text{water}} = +500$ J (it gains).
- Step 3: The relationship: $q_{\text{lost by hot}} = -\,q_{\text{gained by cold}}$.

**Answer:** The water gains 500 J. This "lost = gained" balance is exactly what calorimetry ([0802](/chemistry/0802-calorimetry)) is built on.

### Example 12: The backwards feeling, stated as signs

**Problem:** A reaction in a beaker makes the beaker feel **warm** to your palm. From the **system's** perspective, what are the signs of $q$ and $\ce{\Delta}H$, and is it endo or exo?

**Solution:**
- Step 1: Your palm (surroundings) warms up → the system released heat *to* it.
- Step 2: System releasing heat → $q < 0$ and $\ce{\Delta}H < 0$.
- Step 3: That's the definition of **exothermic**.

**Answer:** $q < 0$, $\ce{\Delta}H < 0$, exothermic. You felt warm, but the *system's* sign is negative — always read it backwards from your hand.

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| "It feels cold, so it's losing heat / exothermic." | You confuse *your* feeling with the *system's* sign. | **You feel it backwards.** Feels cold = system *absorbs* = endothermic ($q>0$). Feels warm = exothermic. |
| Assigning signs from your hand's point of view. | Forgetting to fix the boundary first. | Always name the **system** explicitly, then ask "does the *system* gain or lose heat?" |
| Treating temperature and thermal energy as the same thing. | They both go up when you heat something. | Temperature = *average* KE (per particle); thermal energy = *total* KE (all particles). Boiling teaspoon < warm bathtub in energy. |
| Calling heat something an object "contains." | "The stove has a lot of heat." | Heat is energy *in transit* due to a temperature difference. Objects contain thermal energy; heat only exists while it *flows*. |
| Computing $\ce{\Delta}H$ as reactants − products. | Sign feels arbitrary. | It's always **products − reactants**. Products lower → negative → exo. |
| Measuring $\ce{\Delta}H$ up to the activation-energy peak. | The peak is the tallest thing on the diagram. | $\ce{\Delta}H$ is reactants-to-products *only*. The peak is $E_a$ (from 0704), a different quantity. |
| "Thermal equilibrium means equal amounts of heat/energy." | "Equal" sounds like equal everything. | Equilibrium = equal **temperature**. Amounts of thermal energy can differ wildly. |
| Forgetting reversing a process flips the sign. | Melting and freezing feel like "the same water stuff." | Reverse a process → flip the sign of $\ce{\Delta}H$. Melting $+$, freezing $-$. |

---

## AP Exam Tips

- **Every sign is from the SYSTEM's viewpoint.** The exam will describe a beaker that "feels warm" or "feels cold" and ask for the sign of $q$ or $\ce{\Delta}H$. Translate: *feels cold* = endothermic = $q>0$, $\ce{\Delta}H>0$; *feels warm* = exothermic = $q<0$, $\ce{\Delta}H<0$. This "read it backwards" move is the single most tested idea in Topic 6.1.
- **Endo vs. exo from a description or a diagram, fast.** From words: does the *surroundings* get hotter (exo) or colder (endo)? From a diagram: are products lower (exo, $\ce{\Delta}H<0$) or higher (endo, $\ce{\Delta}H>0$)?
- **$\ce{\Delta}H$ sign = direction, memorized.** Negative = exothermic = releases heat. Positive = endothermic = absorbs heat. If you flip these you'll miss a chain of downstream points in later Unit 6 problems.
- **$\ce{\Delta}H$ is reactants → products, not up to the peak.** On a labeled energy profile, the arrow you want is between the two flat levels. Don't include the activation-energy hump.
- **Heat flows to thermal equilibrium (equal T).** If a free-response asks for the "final temperature," they want a value *between* the two starting temperatures where both objects sit at the *same* T. Equal temperature, not equal energy — say so explicitly for the point.
- **"Which warms, which cools?"** The hotter object always cools, the colder always warms, because heat flows hot → cold. State the direction of flow first, then the temperature changes follow automatically.
- **Watch your currency and units.** Enthalpies are in kJ (or kJ/mol); an instant cold pack costs about \$4 at the pharmacy, but that dollar sign is prose, not chemistry.

---

## Practice Problems

### Problem 1
A hand warmer relies on iron rusting, $\ce{4Fe(s) + 3O2(g) -> 2Fe2O3(s)}$, and it gets warm in your pocket. Is this endothermic or exothermic? Give the signs of $q$ and $\ce{\Delta}H$ for the system.

<details>
<summary><strong>Solution</strong></summary>

It warms your hand → the surroundings gain heat → the system *releases* heat. That's **exothermic**, with $q < 0$ and $\ce{\Delta}H < 0$.

**Answer:** Exothermic; $q < 0$, $\ce{\Delta}H < 0$.

</details>

### Problem 2
Define, in one sentence each, the difference between **temperature**, **thermal energy**, and **heat**.

<details>
<summary><strong>Solution</strong></summary>

- **Temperature** = the *average* kinetic energy per particle.
- **Thermal energy** = the *total* kinetic energy of all the particles combined.
- **Heat ($q$)** = energy *transferred* from one object to another because of a temperature difference.

**Answer:** Temperature is an average, thermal energy is a total, and heat is energy in transit due to a temperature gap.

</details>

### Problem 3
You define the reacting chemicals in a flask as "the system." Everything else — the flask, the water bath, the air — is what?

<details>
<summary><strong>Solution</strong></summary>

Everything outside the boundary you drew is the **surroundings**. Together, system + surroundings = the **universe**.

**Answer:** The surroundings; system + surroundings = the universe.

</details>

### Problem 4
Dry ice ($\ce{CO2(s)}$) sublimes: $\ce{CO2(s) -> CO2(g)}$, and it makes everything around it frost over and go cold. Endo or exo? Sign of $\ce{\Delta}H$?

<details>
<summary><strong>Solution</strong></summary>

It chills its surroundings, so the surroundings *lose* heat to the dry ice → the system *absorbs* heat. Turning a solid straight into a gas requires pulling molecules fully apart, which costs energy. **Endothermic, $\ce{\Delta}H > 0$.**

**Answer:** Endothermic; $\ce{\Delta}H > 0$.

</details>

### Problem 5
An energy diagram shows reactants at 200 kJ and products at 275 kJ. Compute $\ce{\Delta}H$ and state whether the reaction is endo or exo.

<details>
<summary><strong>Solution</strong></summary>

$\ce{\Delta}H = H_{\text{products}} - H_{\text{reactants}} = 275 - 200 = +75$ kJ. Products are higher and $\ce{\Delta}H$ is positive → **endothermic**.

**Answer:** $\ce{\Delta}H = +75$ kJ, endothermic.

</details>

### Problem 6
A spoon at 80 °C is placed in soup at 40 °C. State the direction of heat flow, which object warms, which cools, and roughly where the final temperature lands.

<details>
<summary><strong>Solution</strong></summary>

Heat flows hot → cold, so **spoon → soup**. The spoon **cools**, the soup **warms** (barely, since there's much more soup). Final temperature is between 40 and 80 °C, very close to 40 °C.

**Answer:** Heat flows spoon → soup; spoon cools, soup warms; final T just above 40 °C.

</details>

### Problem 7
Two identical metal blocks, one at 100 °C and one at 20 °C, touch and are perfectly insulated from everything else. What is the approximate final temperature, and why?

<details>
<summary><strong>Solution</strong></summary>

They're identical, so they meet halfway: about **60 °C**, the average. Heat flows from the 100 °C block to the 20 °C block until temperatures are equal (thermal equilibrium). Equal masses of the same metal split the difference evenly.

**Answer:** About 60 °C, because equal blocks reach equilibrium at the midpoint temperature.

</details>

### Problem 8
Rewrite the "feels cold means endothermic" idea as a rule about the sign of $q$ for the system, and explain why the feeling is "backwards."

<details>
<summary><strong>Solution</strong></summary>

When something feels cold, *your skin* is losing heat *to* the system, so the system is **gaining** heat: $q > 0$ (endothermic). It feels backwards because your sensation reports what happens to *you* (the surroundings), which is always the opposite of what happens to the *system*.

**Answer:** Feels cold → system gains heat → $q > 0$ (endothermic); the feeling reflects the surroundings, whose energy change is opposite the system's.

</details>

### Problem 9
Respiration burns glucose: $\ce{C6H12O6 + 6O2 -> 6CO2 + 6H2O}$, releasing the energy your cells run on. Endo or exo? How does its $\ce{\Delta}H$ sign compare to photosynthesis (Example 6)?

<details>
<summary><strong>Solution</strong></summary>

Respiration *releases* energy → **exothermic, $\ce{\Delta}H < 0$.** It's the reverse of photosynthesis ($\ce{\Delta}H > 0$), so it has the opposite sign. Photosynthesis stores energy; respiration releases it.

**Answer:** Exothermic, $\ce{\Delta}H < 0$ — opposite sign to photosynthesis.

</details>

### Problem 10
On a labeled energy profile, reactants are at 30 kJ, the peak is at 110 kJ, and products are at 70 kJ. (a) What is $E_a$ (forward)? (b) What is $\ce{\Delta}H$? (c) Endo or exo?

<details>
<summary><strong>Solution</strong></summary>

- (a) $E_a$ = peak − reactants = $110 - 30 = 80$ kJ.
- (b) $\ce{\Delta}H$ = products − reactants = $70 - 30 = +40$ kJ.
- (c) Products higher, $\ce{\Delta}H$ positive → **endothermic**.

**Answer:** $E_a = 80$ kJ, $\ce{\Delta}H = +40$ kJ, endothermic. ($E_a$ and $\ce{\Delta}H$ are different arrows — don't confuse them.)

</details>

### Problem 11
Explain why a small teaspoon of boiling water (100 °C) can hold *less* thermal energy than a full bathtub of warm water (40 °C).

<details>
<summary><strong>Solution</strong></summary>

Temperature (100 °C vs. 40 °C) is the *average* KE per molecule, but thermal energy is the *total* over all molecules. The bathtub has enormously more water molecules, so even though each one moves a bit slower on average, the *sum* of all their kinetic energies far exceeds the teaspoon's.

**Answer:** Because thermal energy is a total over all particles, and the bathtub has vastly more particles than the teaspoon.

</details>

### Problem 12
For the neutralization $\ce{HCl(aq) + NaOH(aq) -> NaCl(aq) + H2O(l)}$, the beaker gets noticeably warmer. State the sign of $\ce{\Delta}H$ and classify the reaction.

<details>
<summary><strong>Solution</strong></summary>

The beaker (surroundings) warms → the system releases heat → **exothermic**, $\ce{\Delta}H < 0$. (Strong acid–base neutralizations are reliably exothermic.)

**Answer:** $\ce{\Delta}H < 0$; exothermic.

</details>

### Problem 13
A hot 60 g iron nail is dropped into insulated water and loses 420 J of heat before everything reaches thermal equilibrium. (a) How much heat does the water gain? (b) Write the conservation relationship. (c) At equilibrium, are the nail and water at the same temperature?

<details>
<summary><strong>Solution</strong></summary>

- (a) No heat escapes, so the water gains exactly what the nail loses: **420 J**.
- (b) $q_{\text{lost by hot}} = -\,q_{\text{gained by cold}}$, i.e., $q_{\text{nail}} = -420$ J and $q_{\text{water}} = +420$ J.
- (c) Yes — thermal equilibrium means their temperatures are equal (though their thermal energies differ).

**Answer:** Water gains 420 J; $q_{\text{nail}} = -q_{\text{water}}$; equal temperatures at equilibrium.

</details>

### Problem 14
A student writes: "Breaking bonds releases energy, so bond breaking is exothermic." Correct the statement and give the correct rule for bond breaking and forming.

<details>
<summary><strong>Solution</strong></summary>

It's backwards. **Breaking bonds absorbs energy (endothermic); forming bonds releases energy (exothermic).** A reaction's overall $\ce{\Delta}H$ depends on the balance: if forming the new bonds releases more than breaking the old ones cost, the reaction is exothermic overall.

**Answer:** Breaking absorbs, forming releases; the net $\ce{\Delta}H$ is the balance of the two (see 0804).

</details>

### Problem 15
An instant cold pack is applied to a swollen ankle. Using the words *system, surroundings, heat flow,* and *endothermic*, describe what happens energetically and why the ankle feels cold.

<details>
<summary><strong>Solution</strong></summary>

The dissolving $\ce{NH4NO3}$ is the **system**; the ankle and skin are the **surroundings**. The dissolving is **endothermic**, so **heat flows from the surroundings (ankle) into the system (pack)**. Because the ankle is *losing* heat to the pack, it feels cold — the sensation is the surroundings' energy loss, opposite to the system's gain. Heat keeps flowing until pack and skin approach thermal equilibrium.

**Answer:** Endothermic dissolving pulls heat from the ankle (surroundings) into the pack (system); the ankle feels cold because it's the one losing heat, and flow continues toward thermal equilibrium.

</details>

---

## Quick Reference

| Concept | Rule |
|---|---|
| **Universe** | System + surroundings (once you draw the boundary) |
| **Temperature** | *Average* KE per particle (from KMT, 0505) |
| **Thermal energy** | *Total* KE of all particles |
| **Heat ($q$)** | Energy transferred due to a temperature difference |
| **First law (light)** | $\ce{\Delta}E = q + w$; AP focuses on $q$ |
| **Enthalpy** | At constant $P$: $\ce{\Delta}H = q_p$ |
| **Exothermic** | System *releases* heat; $q<0$, $\ce{\Delta}H<0$; surroundings warm; products lower |
| **Endothermic** | System *absorbs* heat; $q>0$, $\ce{\Delta}H>0$; surroundings cool; products higher |
| **"Backwards" rule** | Feels warm → exo; feels cold → endo (you sense the surroundings) |
| **$\ce{\Delta}H$ from diagram** | $H_{\text{products}} - H_{\text{reactants}}$ (not up to the peak) |
| **Bonds** | Breaking absorbs; forming releases (→ 0804) |
| **Heat flow** | Always hot → cold, until thermal equilibrium |
| **Thermal equilibrium** | Equal *temperature* (not equal energy) |
| **Conservation** | $q_{\text{lost by hot}} = -\,q_{\text{gained by cold}}$ (→ calorimetry, 0802) |
| **Reverse a process** | Flips the sign of $\ce{\Delta}H$ |

---

<div align="center">

[← Catalysis](/chemistry/0706-catalysis) | [Calorimetry →](/chemistry/0802-calorimetry)

</div>
