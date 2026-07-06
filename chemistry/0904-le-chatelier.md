# Le Chatelier's Principle
<p class="article-date">July 5, 2026</p>

*Picture the 4:45 bus home from downtown San Diego — already packed, everyone wedged in, but somehow balanced. People near the front, people near the back, nobody moving, a weird kind of standstill. Then at the next stop three more riders cram in through the front door. Instantly, without anyone saying a word, the whole crowd shuffles toward the back to relieve the squeeze up front. The bus doesn't get bigger and nobody gets off — the people just redistribute until the crush eases and everything settles into a new standstill. That reflex is **Le Chatelier's principle**: stress an equilibrium — shove something in, pull something out, squeeze the volume, crank the heat — and the reaction shifts in whichever direction **relieves the stress**. This is Topics 7.9–7.10, and it's the payoff of the whole equilibrium unit: once you can read the stress, you can predict which way any reversible reaction will lean, and the AP exam asks you to do exactly that over and over.*

---

## What You'll Learn

- State **Le Chatelier's principle** and use the "system relieves the stress" logic to predict the direction of a shift
- Explain the single most important rule of the whole topic: adding/removing a substance or changing the volume shifts the **position** of equilibrium but does **not** change $K$ — **only temperature changes $K$**
- Predict concentration-stress shifts (add a reactant → shift right, remove a product → shift right, etc.) and justify each one rigorously through $Q$ vs $K$
- Predict volume/pressure-stress shifts for gases by **counting moles of gas** on each side
- Recognize the two classic pressure traps: **adding an inert gas at constant volume** does nothing, and a reaction with **equal moles of gas** on both sides doesn't shift
- Treat **heat as a reactant or a product** to predict temperature shifts, and determine whether $K$ increases or decreases from the sign of $\Delta H$
- Explain why a **catalyst causes no shift** and leaves $K$ unchanged (it only reaches equilibrium faster)
- Reason through a multi-stress, real-world optimization: the **Haber process** $\ce{N2 + 3H2 <=> 2NH3}$
- Predict the effect of a stress on the amount of a **specific species** and on the value of $K$

---

## Prerequisites

- [Introduction to Equilibrium](/chemistry/0901-introduction-to-equilibrium) — Le Chatelier's principle only makes sense once you know equilibrium is **dynamic**: the forward and reverse reactions never stop, so the system can always shift to a new balance point
- [The Equilibrium Constant](/chemistry/0902-equilibrium-constant) — the rigorous engine behind every prediction is the **reaction quotient $Q$ compared to $K$**. Every stress in this article works by moving $Q$ away from $K$, and the shift is just the system pushing $Q$ back to $K$

---

## The Core Concept

### Intuition First

Let's stay on that crowded bus, because every single rule in this topic is sitting right there in the aisle.

**The packed, balanced bus is the equilibrium system.** Nobody's moving, but that's not because the bus is empty — it's because the crowd has settled into a distribution where the push forward and the push backward cancel out. That's exactly a chemical equilibrium: the forward and reverse reactions are both running (it's *dynamic*, from [Introduction to Equilibrium](/chemistry/0901-introduction-to-equilibrium)), and they're running at equal rates, so the concentrations hold steady.

**Cramming riders in the front door is a stress.** You've suddenly overloaded one region. Something has to give. In chemistry, a stress is anything you do to the system from the outside: add a reactant or product, remove a reactant or product, squeeze the volume, or change the temperature.

**Everyone shuffling toward the roomier back is the shift.** The crowd doesn't fight the crush — it flows *away* from it, toward wherever there's space. The system consumes the crowding by redistributing. That's the heart of Le Chatelier: **the reaction shifts in whichever direction relieves the stress you applied.** Cram in more of one thing, and the system shifts *away* from that thing, consuming it.

**The bus re-settling into a new standstill is the new equilibrium.** After the shuffle, the bus is balanced again — but it's a *different* arrangement than before. More people are in the back now. In chemistry, the system reaches a new equilibrium with **new concentrations**, but here's the beautiful part: as long as you didn't change the temperature, the *rule* governing the balance — the ratio $K$ — is exactly the same. The bus is still a bus. Same capacity, same rules, new seating.

That last point is the thing to tattoo on your brain: **adding, removing, or squeezing changes where the equilibrium sits, not the value of $K$.** The only stress that actually rewrites the rulebook — that changes $K$ itself — is **temperature**. Heating or cooling isn't just crowding the bus; it's changing how the bus itself behaves. We'll hammer this again and again.

### The Formal Statement

> **Le Chatelier's Principle:** When a system at equilibrium is disturbed by a change in concentration, volume/pressure, or temperature, the system responds by shifting its equilibrium position in the direction that **partially counteracts** the disturbance.

"Shift right" means the forward reaction runs a bit more, making **more products** and using up reactants. "Shift left" means the reverse reaction runs a bit more, making **more reactants** and using up products.

### The Rigorous Engine: $Q$ vs $K$

The bus gives you the intuition; $Q$ vs $K$ gives you the *proof*, and it's how you earn full credit on the AP exam. Recall from [The Equilibrium Constant](/chemistry/0902-equilibrium-constant) that the reaction quotient $Q$ has the exact same form as $K$ but uses the concentrations **right now**, whatever they happen to be:

$$Q = \frac{[\text{products}]^{\text{coeffs}}}{[\text{reactants}]^{\text{coeffs}}}$$

Comparing $Q$ to $K$ tells you which way the reaction must go to reach equilibrium:

| Comparison | Meaning | Direction of shift |
|---|---|---|
| $Q < K$ | too few products relative to equilibrium | shift **right** (forward, make products) |
| $Q = K$ | at equilibrium | **no shift** |
| $Q > K$ | too many products relative to equilibrium | shift **left** (reverse, make reactants) |

Every stress in this article works the same way: **the stress knocks $Q$ off the value of $K$, and the system shifts to drive $Q$ back to $K$.** If you ever forget which way a reaction shifts, write out $Q$, figure out what the stress did to it, and compare it to $K$. The bus tells you the answer fast; $Q$ vs $K$ proves it.

### The Four Stresses at a Glance

| Stress | What the system does | Does $K$ change? |
|---|---|---|
| Add a substance | shifts **away** from the added substance (consumes it) | **No** |
| Remove a substance | shifts **toward** the removed substance (replaces it) | **No** |
| Decrease volume (↑ pressure) | shifts toward the side with **fewer** moles of gas | **No** |
| Increase temperature | shifts in the **endothermic** direction (heat is consumed) | **Yes** |

Notice the pattern: three of the four stresses leave $K$ alone. Only temperature changes $K$. Let's build each one.

### Stress 1: Concentration

Add a reactant, and the system shifts **right** to consume it. Remove a product, and the system shifts **right** to replace it. In both cases the system moves *away* from what you added and *toward* what you removed.

Why, rigorously? Take $\ce{A <=> B}$ with $Q = \dfrac{[\ce{B}]}{[\ce{A}]}$.

- **Add $\ce{A}$:** the denominator jumps, so $Q$ drops below $K$ → $Q < K$ → shift **right**. The system makes $\ce{B}$ and eats the extra $\ce{A}$.
- **Remove $\ce{B}$:** the numerator drops, so $Q$ falls below $K$ → $Q < K$ → shift **right** to remake $\ce{B}$.
- **Add $\ce{B}$:** numerator jumps → $Q > K$ → shift **left**.
- **Remove $\ce{A}$:** denominator drops → $Q > K$ → shift **left** to remake $\ce{A}$.

The bus check: cram riders in the "A" door and the crowd flows toward "B." Pull riders out the "B" door and the crowd flows back to fill the gap. Every time, the system moves to undo what you did — but only *partially*. It never fully cancels the stress, and it never overshoots.

### Stress 2: Volume and Pressure (gases only)

This one is pure **mole-counting**. When you shrink the container (which raises the pressure), the gas gets crowded — so the system shifts toward whichever side has **fewer moles of gas**, because fewer gas molecules take up less room and relieve the pressure.

> **Decrease volume / increase pressure → shift toward FEWER moles of gas.**
> **Increase volume / decrease pressure → shift toward MORE moles of gas.**
> **Equal moles of gas on both sides → no shift.**

Count only the **gas-phase** coefficients (solids and liquids don't count — they barely change volume). For the Haber process:

$$\ce{N2(g) + 3H2(g) <=> 2NH3(g)}$$

Left side: $1 + 3 = 4$ moles of gas. Right side: $2$ moles of gas. Squeeze the volume, and the system shifts **right** toward the 2-mole side, because packing 4 crowded molecules into 2 relieves the pressure. It's the bus again: when the aisle gets tight, people consolidate onto fewer seats.

**The inert-gas trap.** If you add an *unreactive* gas (like argon) while keeping the **volume constant**, nothing shifts. The total pressure goes up, but the inert gas doesn't change the concentration (mol/L) of any reactant or product, and $Q$ is built from concentrations. No change in $Q$ → no shift. It's like a new passenger who boards but stands frozen on the steps — the total headcount rises, but the actual crowd distribution in the aisle is untouched, so nobody shuffles. (If instead you add inert gas by *increasing the volume* at constant pressure, that's really a volume increase, and normal volume rules apply.)

### Stress 3: Temperature — the ONLY stress that changes $K$

Here's the trick that makes temperature easy: **write heat as if it were a reactant or a product**, using the sign of $\Delta H$.

- **Exothermic** reaction ($\Delta H < 0$) → heat is a **product**:
$$\ce{A <=> B} + \text{heat}$$
- **Endothermic** reaction ($\Delta H > 0$) → heat is a **reactant**:
$$\text{heat} + \ce{A <=> B}$$

Now treat "heat" like any other substance and use your concentration logic. **Raising the temperature = adding heat**; **lowering the temperature = removing heat.**

- **Heat an exothermic reaction:** you're adding heat to the *product* side → shift **away** from products → shift **left**. Fewer products at equilibrium means $K$ **decreases**.
- **Heat an endothermic reaction:** you're adding heat to the *reactant* side → shift **away** from reactants → shift **right**. More products means $K$ **increases**.

And here's the part that separates temperature from every other stress: because the shift changes the products-to-reactants ratio *at the new temperature*, the value of $K$ itself moves.

> **Only temperature changes $K$.** Adding/removing substances and changing volume shift the *position* while $K$ stays fixed. Temperature rewrites $K$.

Bus version: crowding a door just makes people shuffle within the same bus. Changing the temperature is like swapping the bus itself for a bigger or smaller one — the fundamental rules change, not just the seating.

### Stress 4: Catalyst — the "no-op"

A **catalyst does not shift equilibrium at all.** From [Catalysis](/chemistry/0706-catalysis), a catalyst speeds up the forward and reverse reactions by the **same** factor, so it can't favor one side. The equilibrium position is unchanged, the amount of every species at equilibrium is unchanged, and $K$ is unchanged. The only thing a catalyst does is get the system to equilibrium **faster**.

This is a guaranteed conceptual question. If a prompt asks what a catalyst does to the position of equilibrium or to $K$, the answer is **nothing** — it just shortens the wait.

---

## Worked Examples

### Example 1: Adding a Reactant (Concentration)

**Problem:** For $\ce{N2(g) + 3H2(g) <=> 2NH3(g)}$ at equilibrium, more $\ce{H2}$ is injected. Which way does the equilibrium shift, and what happens to the amount of $\ce{NH3}$?

**Solution:**

- Step 1: $\ce{H2}$ is a reactant. Le Chatelier: the system shifts **away** from the added substance.
- Step 2: $Q$ check — adding $\ce{H2}$ raises the denominator of $Q = \dfrac{[\ce{NH3}]^2}{[\ce{N2}][\ce{H2}]^3}$, so $Q < K$ → shift **right**.
- Step 3: Shifting right makes more product.

**Answer:** The equilibrium shifts **right (toward products)**; the amount of $\ce{NH3}$ **increases**. $K$ is unchanged (concentration stress).

### Example 2: Removing a Product (Concentration)

**Problem:** For $\ce{CaCO3(s) <=> CaO(s) + CO2(g)}$, the $\ce{CO2}$ gas is continuously pumped out. Which way does the reaction shift?

**Solution:**

- Step 1: $\ce{CO2}$ is a product. Removing a product makes the system shift **toward** it to replace it → shift **right**.
- Step 2: $Q$ check — only $\ce{CO2}$ appears in the expression ($Q = [\ce{CO2}]$, since solids are excluded). Removing $\ce{CO2}$ lowers $Q$ below $K$ → shift **right**.

**Answer:** Shifts **right**; more $\ce{CaCO3}$ decomposes. (This is why lime kilns vent the $\ce{CO2}$ — it drives the reaction forward.)

### Example 3: Justifying with $Q$ vs $K$

**Problem:** For $\ce{H2(g) + I2(g) <=> 2HI(g)}$, $K = 50$ at some temperature. At a given instant $[\ce{H2}] = 0.10$, $[\ce{I2}] = 0.10$, $[\ce{HI}] = 0.10$ M. Which way does the reaction proceed?

**Solution:**

- Step 1: $Q = \dfrac{[\ce{HI}]^2}{[\ce{H2}][\ce{I2}]} = \dfrac{(0.10)^2}{(0.10)(0.10)} = \dfrac{0.010}{0.010} = 1.0$.
- Step 2: Compare: $Q = 1.0 < K = 50$.
- Step 3: $Q < K$ means too few products → the reaction runs **forward** to raise $Q$ up to $K$.

**Answer:** $Q < K$, so the reaction shifts **right (forward)**, making more $\ce{HI}$ until $Q = 50$.

### Example 4: Decreasing Volume (Mole-Counting)

**Problem:** For $\ce{2SO2(g) + O2(g) <=> 2SO3(g)}$, the container volume is cut in half. Which way does the equilibrium shift?

**Solution:**

- Step 1: Count gas moles. Left: $2 + 1 = 3$. Right: $2$.
- Step 2: Decreasing volume (raising pressure) shifts toward **fewer** moles of gas.
- Step 3: The right side has fewer moles (2 < 3).

**Answer:** Shifts **right (toward $\ce{SO3}$)**. $K$ unchanged (volume stress).

### Example 5: Increasing Volume

**Problem:** For $\ce{N2O4(g) <=> 2NO2(g)}$, the container is expanded to twice its volume. Which way does it shift?

**Solution:**

- Step 1: Count gas moles. Left: $1$. Right: $2$.
- Step 2: Increasing volume (lowering pressure) shifts toward **more** moles of gas.
- Step 3: The right side has more moles (2 > 1).

**Answer:** Shifts **right (toward $\ce{NO2}$)**. The pale mixture darkens as more brown $\ce{NO2}$ forms.

### Example 6: Equal Moles — No Shift

**Problem:** For $\ce{H2(g) + I2(g) <=> 2HI(g)}$, the volume is decreased. Which way does the equilibrium shift?

**Solution:**

- Step 1: Count gas moles. Left: $1 + 1 = 2$. Right: $2$.
- Step 2: Equal moles of gas on both sides → volume/pressure changes have **no** side to favor.

**Answer:** **No shift.** When the moles of gas are equal, squeezing or expanding the volume doesn't move the equilibrium position.

### Example 7: The Inert-Gas Trap

**Problem:** For $\ce{N2(g) + 3H2(g) <=> 2NH3(g)}$ at equilibrium, argon gas is added while the **volume is held constant**. Which way does the equilibrium shift?

**Solution:**

- Step 1: Argon is inert — it doesn't react with anything.
- Step 2: At constant volume, adding argon does **not** change the concentration (mol/L) of $\ce{N2}$, $\ce{H2}$, or $\ce{NH3}$.
- Step 3: $Q$ depends only on those concentrations, so $Q$ is unchanged → $Q = K$ still.

**Answer:** **No shift.** Total pressure rises, but the partial pressures/concentrations of the reacting gases are untouched. This is a classic trap — "pressure increased" does **not** automatically mean a shift.

### Example 8: Heating an Exothermic Reaction

**Problem:** For $\ce{N2(g) + 3H2(g) <=> 2NH3(g)}$, $\Delta H = -92\ \text{kJ/mol}$ (exothermic). The temperature is raised. Which way does the equilibrium shift, and what happens to $K$?

**Solution:**

- Step 1: Exothermic → write heat as a **product**: $\ce{N2 + 3H2 <=> 2NH3} + \text{heat}$.
- Step 2: Raising $T$ = adding heat to the **product** side → shift **away** from products → shift **left**.
- Step 3: Fewer products at the new equilibrium → $K$ **decreases**.

**Answer:** Shifts **left**; $\ce{NH3}$ decreases; $K$ **decreases**. (This is temperature — the only stress that changes $K$.)

### Example 9: Heating an Endothermic Reaction

**Problem:** For $\ce{N2O4(g) <=> 2NO2(g)}$, $\Delta H = +57\ \text{kJ/mol}$ (endothermic). The mixture is heated. Predict the shift and the effect on $K$.

**Solution:**

- Step 1: Endothermic → write heat as a **reactant**: $\text{heat} + \ce{N2O4} <=> \ce{2NO2}$.
- Step 2: Raising $T$ = adding heat to the **reactant** side → shift **away** from reactants → shift **right**.
- Step 3: More products → $K$ **increases**.

**Answer:** Shifts **right (more $\ce{NO2}$)**; $K$ **increases**. Heating a sealed tube of this gas visibly darkens it — a real demo of an endothermic shift.

### Example 10: Which Change Alters $K$?

**Problem:** For a gaseous exothermic equilibrium at equilibrium, which of these changes will change the value of $K$? (a) adding more reactant; (b) halving the volume; (c) adding a catalyst; (d) raising the temperature.

**Solution:**

- Step 1: (a) Concentration stress → shifts position, $K$ unchanged.
- Step 2: (b) Volume stress → shifts position, $K$ unchanged.
- Step 3: (c) Catalyst → no shift at all, $K$ unchanged.
- Step 4: (d) Temperature → the *only* stress that changes $K$.

**Answer:** Only **(d) raising the temperature** changes $K$. (a), (b), and (c) leave $K$ exactly the same.

### Example 11: The Catalyst Non-Effect

**Problem:** A catalyst is added to $\ce{N2(g) + 3H2(g) <=> 2NH3(g)}$ already at equilibrium. State the effect on (a) the position of equilibrium, (b) the amount of $\ce{NH3}$ at equilibrium, (c) $K$, (d) the time to reach equilibrium.

**Solution:**

- Step 1: A catalyst speeds forward and reverse **equally** → it can't favor either side.
- Step 2: (a) No shift; (b) no change in $\ce{NH3}$; (c) $K$ unchanged.
- Step 3: (d) Both directions are faster, so equilibrium arrives **sooner**.

**Answer:** (a) No shift; (b) unchanged; (c) unchanged; (d) reached **faster**. A catalyst changes only the *rate*, never the equilibrium.

### Example 12: Multi-Stress on the Haber Process

**Problem:** Industrial ammonia synthesis $\ce{N2(g) + 3H2(g) <=> 2NH3(g)}$ ($\Delta H = -92\ \text{kJ/mol}$) needs to **maximize $\ce{NH3}$ yield**. For each change, state whether it increases yield: (a) high pressure; (b) high temperature; (c) removing $\ce{NH3}$ as it forms; (d) adding a catalyst.

**Solution:**

- Step 1: (a) Left = 4 mol gas, right = 2 mol gas. High pressure shifts toward fewer moles → **right** → more $\ce{NH3}$. **Increases yield.**
- Step 2: (b) Exothermic; heating shifts **left** and lowers $K$ → **decreases yield.** (But low $T$ makes the reaction too slow — so industry uses a *moderate* ~450 °C compromise: some yield traded for acceptable speed.)
- Step 3: (c) Removing product shifts **right** to replace it → **increases yield** (this is done continuously in real plants).
- Step 4: (d) Catalyst (iron) → no shift, no yield change, but reaches equilibrium **faster** — essential for practical rates.

**Answer:** (a) increases, (b) decreases (hence a temperature compromise), (c) increases, (d) no yield change but faster. The Haber process is a live tug-of-war between yield and speed.

### Example 13: Predicting a Specific Species

**Problem:** For $\ce{CO(g) + 2H2(g) <=> CH3OH(g)}$ at equilibrium, more $\ce{CO}$ is added. What happens to the amount of $\ce{H2}$?

**Solution:**

- Step 1: Adding $\ce{CO}$ (a reactant) → $Q < K$ → shift **right**.
- Step 2: Shifting right **consumes** reactants, including $\ce{H2}$.

**Answer:** The amount of $\ce{H2}$ **decreases** (it gets consumed as the system shifts right to relieve the added $\ce{CO}$). A nice reminder: adding one reactant can *lower* another reactant.

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Thinking adding a substance or changing volume changes $K$ | Confusing "the position moved" with "$K$ moved" | **Only temperature changes $K$.** Every other stress shifts the position while $K$ stays fixed |
| "Increasing pressure always shifts the equilibrium" | Assuming any pressure change forces a shift | Adding an **inert gas at constant volume** raises pressure but changes no concentration → **no shift**. And if moles of gas are **equal** on both sides, volume changes do nothing |
| Counting solids and liquids in mole-counting | Treating every coefficient as a gas | Only **gas-phase** species count for volume/pressure shifts. $\ce{(s)}$ and $\ce{(l)}$ are ignored |
| Getting the temperature direction backwards | Not writing heat into the equation | **Write heat as a product (exo) or reactant (endo)**, then treat it like a concentration stress. Heating = adding heat |
| Saying a catalyst increases yield | "Faster reaction = more product" | A catalyst speeds **both** directions equally → **no shift**, same $K$, same yield; only **faster** to get there |
| Forgetting the shift is only *partial* | Thinking the system fully cancels the stress | Le Chatelier shifts to **partially** counteract — it never restores the original concentration exactly, and never overshoots |
| Not justifying with $Q$ vs $K$ | Relying on memorized rules alone | On free-response, **compute or reason about $Q$ vs $K$** — that's the reasoning the rubric rewards |

---

## AP Exam Tips

- **Only temperature changes $K$.** This is the single most tested idea in the topic. If a question asks what a concentration change, a volume change, a catalyst, or an inert gas does to $K$, the answer is **nothing**. If it's a temperature change, $K$ moves.
- **For pressure shifts, count moles of gas.** Decrease volume → shift toward **fewer** moles of gas; increase volume → toward **more**; equal moles → **no shift**. Ignore solids and liquids.
- **The inert-gas-at-constant-volume trap is a favorite.** Adding argon (or any inert gas) at constant volume does **not** shift the equilibrium, because concentrations — and therefore $Q$ — don't change.
- **Treat heat as a reactant or product.** Exothermic → heat is a product (heating shifts left, $K$ down). Endothermic → heat is a reactant (heating shifts right, $K$ up). Write it into the equation and reason like a concentration change.
- **A catalyst does NOT shift equilibrium and does NOT change $K$** — it only reaches equilibrium faster. This is a guaranteed conceptual point.
- **Justify shifts with $Q$ vs $K$.** For full credit on free-response, state how the stress changes $Q$ relative to $K$ and conclude the direction ("$Q$ becomes less than $K$, so the reaction shifts right"). Memorized rules get the answer; $Q$ vs $K$ gets the points.
- **The shift is partial.** The system relieves the stress but never fully cancels it — don't claim concentrations return to their original values.

---

## Practice Problems

### Problem 1
State Le Chatelier's principle in one sentence, using the word "stress."

<details>
<summary><strong>Solution</strong></summary>

When a system at equilibrium is disturbed by a stress (a change in concentration, volume/pressure, or temperature), it shifts its equilibrium position in the direction that partially counteracts (relieves) that stress.

**Stress the system, and it shifts to relieve the stress.**

</details>

---

### Problem 2
Which of the following change the value of $K$? (a) adding a reactant; (b) removing a product; (c) decreasing the volume; (d) adding a catalyst; (e) increasing the temperature.

<details>
<summary><strong>Solution</strong></summary>

Only **(e) increasing the temperature** changes $K$. Adding/removing substances (a, b) and changing volume (c) shift the *position* but leave $K$ fixed; a catalyst (d) causes no shift and no change in $K$.

**Only temperature changes $K$ — answer (e).**

</details>

---

### Problem 3
For $\ce{2SO2(g) + O2(g) <=> 2SO3(g)}$ at equilibrium, more $\ce{O2}$ is added. Which way does the equilibrium shift, and what happens to $[\ce{SO3}]$?

<details>
<summary><strong>Solution</strong></summary>

$\ce{O2}$ is a reactant. Adding it makes $Q = \dfrac{[\ce{SO3}]^2}{[\ce{SO2}]^2[\ce{O2}]}$ smaller (bigger denominator), so $Q < K$ → shift **right**. Shifting right makes more product.

**Shifts right; $[\ce{SO3}]$ increases. $K$ unchanged.**

</details>

---

### Problem 4
For $\ce{PCl5(g) <=> PCl3(g) + Cl2(g)}$, the container volume is decreased. Predict the shift.

<details>
<summary><strong>Solution</strong></summary>

Count gas moles: left = 1, right = 1 + 1 = 2. Decreasing volume (increasing pressure) shifts toward **fewer** moles of gas → the **left** side.

**Shifts left (toward $\ce{PCl5}$). $K$ unchanged.**

</details>

---

### Problem 5
For $\ce{H2(g) + Cl2(g) <=> 2HCl(g)}$, the volume is doubled. Predict the shift.

<details>
<summary><strong>Solution</strong></summary>

Count gas moles: left = 1 + 1 = 2, right = 2. Equal moles of gas on both sides → volume/pressure changes have no side to favor.

**No shift.**

</details>

---

### Problem 6
For $\ce{N2(g) + 3H2(g) <=> 2NH3(g)}$ at equilibrium in a rigid container, neon gas is added (volume constant). Which way does the equilibrium shift?

<details>
<summary><strong>Solution</strong></summary>

Neon is inert and the volume is fixed, so the concentrations of $\ce{N2}$, $\ce{H2}$, and $\ce{NH3}$ are unchanged. $Q$ depends only on those concentrations, so $Q$ stays equal to $K$.

**No shift** — the classic inert-gas-at-constant-volume trap. (Total pressure rises, but partial pressures don't.)

</details>

---

### Problem 7
For $\ce{2NO2(g) <=> N2O4(g)}$, $\Delta H = -57\ \text{kJ/mol}$ (exothermic). The mixture is cooled. Predict the shift and the effect on $K$.

<details>
<summary><strong>Solution</strong></summary>

Exothermic → heat is a product: $\ce{2NO2 <=> N2O4} + \text{heat}$. Cooling = **removing** heat from the product side → shift **toward** products → shift **right**. More products at the lower temperature → $K$ **increases**.

**Shifts right; $K$ increases.** (Cooling this gas makes it turn colorless as brown $\ce{NO2}$ converts to $\ce{N2O4}$.)

</details>

---

### Problem 8
For $\ce{CaCO3(s) <=> CaO(s) + CO2(g)}$, $\Delta H = +178\ \text{kJ/mol}$. State the effect of (a) increasing temperature, (b) removing $\ce{CO2}$, (c) decreasing the volume.

<details>
<summary><strong>Solution</strong></summary>

(a) Endothermic → heat is a reactant; heating shifts **right**, $K$ **increases**. (b) Removing product $\ce{CO2}$ → shift **right** to replace it, $K$ unchanged. (c) Only $\ce{CO2}$ is a gas (1 mol on the right, 0 on the left); decreasing volume shifts toward fewer gas moles → the **left** side, $K$ unchanged.

**(a) right, $K$↑; (b) right, $K$ same; (c) left, $K$ same.**

</details>

---

### Problem 9
For $\ce{H2(g) + I2(g) <=> 2HI(g)}$, $K = 50$. At an instant, $Q = 80$. Which way does the reaction proceed, and toward more or less $\ce{HI}$?

<details>
<summary><strong>Solution</strong></summary>

$Q = 80 > K = 50$: too many products. The reaction shifts **left (reverse)** to lower $Q$ back to $K$, consuming $\ce{HI}$.

**Shifts left; $\ce{HI}$ decreases.**

</details>

---

### Problem 10
Explain why adding a catalyst to a reaction at equilibrium does not change the amount of product present at equilibrium.

<details>
<summary><strong>Solution</strong></summary>

A catalyst lowers the activation energy for both the forward and reverse reactions by the same factor, so it speeds them up equally. Since neither direction is favored, the equilibrium position and $K$ are unchanged — only the time to reach equilibrium is shortened.

**Equal speed-up of both directions → no shift → same amount of product; just reached faster.**

</details>

---

### Problem 11
For $\ce{CO(g) + 2H2(g) <=> CH3OH(g)}$, list every change you could make to increase the equilibrium yield of $\ce{CH3OH}$ (the reaction is exothermic).

<details>
<summary><strong>Solution</strong></summary>

Shift right by: **adding $\ce{CO}$ or $\ce{H2}$** (reactants); **removing $\ce{CH3OH}$** (product); **decreasing the volume / increasing pressure** (left = 3 mol gas, right = 1 mol gas → shifts toward fewer moles = right); and **lowering the temperature** (exothermic → cooling shifts right and raises $K$).

**Add reactants, remove product, raise pressure, lower temperature.**

</details>

---

### Problem 12
A student says: "I added argon to my gas equilibrium, the pressure went up, so the reaction must have shifted toward fewer moles of gas." What's wrong?

<details>
<summary><strong>Solution</strong></summary>

If the argon was added at **constant volume**, the concentrations (partial pressures) of the actual reactants and products don't change, so $Q$ doesn't change and there is **no shift** — even though total pressure rose. A pressure increase only causes a shift when it comes from a **volume decrease**, which raises the concentrations of the reacting gases.

**No shift — inert gas at constant volume raises total pressure but doesn't change $Q$.**

</details>

---

### Problem 13
For $\ce{2SO2(g) + O2(g) <=> 2SO3(g)}$, $\Delta H = -198\ \text{kJ/mol}$, predict the direction of shift and the effect on $K$ for: (a) increasing temperature; (b) adding $\ce{SO3}$; (c) increasing the volume.

<details>
<summary><strong>Solution</strong></summary>

(a) Exothermic → heat is a product; heating shifts **left**, $K$ **decreases**. (b) Adding product $\ce{SO3}$ → $Q > K$ → shift **left**, $K$ unchanged. (c) Left = 3 mol gas, right = 2 mol gas; increasing volume shifts toward **more** moles of gas → the **left** side, $K$ unchanged.

**(a) left, $K$↓; (b) left, $K$ same; (c) left, $K$ same.**

</details>

---

### Problem 14
In the Haber process, industry runs the reaction at a moderate temperature (~450 °C) rather than a low one, even though a low temperature would give a higher yield. Explain the tradeoff.

<details>
<summary><strong>Solution</strong></summary>

The reaction $\ce{N2 + 3H2 <=> 2NH3}$ is exothermic, so **low temperature maximizes yield** (shifts right, higher $K$). But low temperature also makes the reaction **very slow**, so equilibrium takes too long to be practical. A moderate temperature sacrifices some equilibrium yield in exchange for a fast enough rate — a compromise between thermodynamics (yield) and kinetics (speed). A catalyst helps by speeding things up without touching the equilibrium.

**Low $T$ = high yield but too slow; moderate $T$ trades a little yield for a workable rate.**

</details>

---

### Problem 15
For $\ce{Fe^{3+}(aq) + SCN^-(aq) <=> FeSCN^{2+}(aq)}$ (the deep-red thiocyanate complex) at equilibrium, predict what happens to the red color when: (a) more $\ce{Fe^{3+}}$ is added; (b) $\ce{SCN^-}$ is removed by adding a reagent that ties it up.

<details>
<summary><strong>Solution</strong></summary>

The red color tracks $[\ce{FeSCN^{2+}}]$. (a) Adding reactant $\ce{Fe^{3+}}$ → $Q < K$ → shift **right** → more $\ce{FeSCN^{2+}}$ → **darker red**. (b) Removing reactant $\ce{SCN^-}$ → $Q > K$ → shift **left** → less $\ce{FeSCN^{2+}}$ → **lighter red**.

**(a) darker red (shift right); (b) lighter red (shift left).** ($K$ unchanged in both — concentration stress.)

</details>

---

## Quick Reference

**The four stresses**

| Stress | Direction of shift | Effect on $K$ |
|---|---|---|
| Add a substance | away from it (consume it) | none |
| Remove a substance | toward it (replace it) | none |
| Decrease volume / ↑ pressure | toward **fewer** moles of gas | none |
| Increase volume / ↓ pressure | toward **more** moles of gas | none |
| Increase temperature (exothermic) | left | **$K$ decreases** |
| Increase temperature (endothermic) | right | **$K$ increases** |
| Add inert gas at constant volume | **no shift** | none |
| Add a catalyst | **no shift** (faster only) | none |

**The one rule to memorize:** only **temperature** changes $K$. Everything else shifts the position while $K$ stays put.

**$Q$ vs $K$ — the engine behind every shift**

| Comparison | Shift |
|---|---|
| $Q < K$ | right (forward) |
| $Q = K$ | none (at equilibrium) |
| $Q > K$ | left (reverse) |

**Temperature trick:** write heat as a **product** (exothermic) or a **reactant** (endothermic), then treat heating/cooling like adding/removing that "substance."

**Mole-counting:** count only **gas-phase** coefficients; equal moles of gas → no volume shift.

---

<div align="center">

[← ICE Tables](/chemistry/0903-ice-tables) | [Solubility Equilibria →](/chemistry/0905-solubility-equilibria)

</div>
