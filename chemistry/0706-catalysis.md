# Catalysis
<p class="article-date">July 5, 2026</p>

*Every summer my dad and I drive up to LA, and there's this one mountain pass on the old route that I dread. The road climbs and climbs, switchback after switchback, all the way up over the ridge and then all the way back down — engine straining, everybody carsick, maybe one car every few seconds crawling over the top. Then one year they finished the tunnel. Same starting town, same LA on the other side, but instead of going over the mountain you shoot straight through its base. It's a much lower climb over a much smaller rise, so cars pour through way faster — more of them per hour, none of them exhausted. And here's the part that blew my mind: the tunnel isn't used up. After my dad's car goes through, it's still sitting there, wide open, for the next car and the next. That tunnel is a **catalyst** — a brand-new, lower-effort pathway from reactants to products that speeds everything up without ever being consumed. This is Topic 5.11, the capstone of Unit 5, and it's the idea that quietly runs your whole body, your car's exhaust, and half of modern industry.*

---

## What You'll Learn

- Define a **catalyst** as a substance that speeds up a reaction by providing an **alternative mechanism with a lower activation energy** ($E_a$), without being consumed overall
- Explain why a catalyst speeds up **both** the forward and reverse reactions — and therefore does **not** change $\Delta H$, the products, or the equilibrium position (the Unit 7 connection)
- Draw and label a **reaction energy profile** showing the uncatalyzed and catalyzed paths on the same axes, and show that $\Delta H$ is unchanged
- Identify a catalyst inside a **multi-step mechanism** — consumed in an early step, regenerated in a later step — and distinguish it from an **intermediate**
- Use the **Maxwell–Boltzmann distribution** to explain *why* lowering $E_a$ increases the fraction of effective collisions
- Classify catalysts as **homogeneous**, **heterogeneous**, or **enzymes**, with a real example of each
- Explain how **inhibitors and catalyst poisons** shut a catalyst down

---

## Prerequisites

- [Collision Model and Arrhenius](/chemistry/0704-collision-model-arrhenius) — a catalyst works by lowering the **activation energy** $E_a$; you need to already know what $E_a$ is, how it sits as a barrier between reactants and products, and how the Maxwell–Boltzmann curve decides what fraction of collisions clear it
- [Reaction Mechanisms](/chemistry/0705-reaction-mechanisms) — a catalyst does its job *inside a mechanism*: it's used up in one elementary step and **regenerated** in a later one, so you need to be comfortable reading elementary steps and spotting intermediates

---

## The Core Concept

### Intuition First

Let's stay on that drive to LA, because the whole topic is sitting right there in the mountain.

**The trailheads are the reactants and products.** The starting town is where every car begins (the reactants); LA is where every car ends up (the products). That never changes. Whether you crawl over the pass or shoot through the tunnel, you start in the *same* place and finish in the *same* place. In chemistry terms: the catalyst changes **how** you get from reactants to products, never **what** the reactants and products are.

**Going over the pass is the uncatalyzed reaction.** The old road climbs to a punishingly high point before it can come down the other side. That high point is the **activation energy** — the energy hump every reaction has to get over from [Collision Model and Arrhenius](/chemistry/0704-collision-model-arrhenius). A tall pass means only a few cars make it over per hour: a slow reaction.

**The tunnel is the catalyzed reaction.** Same start, same finish, but the tunnel gives you a *completely different route* over a *much lower* rise. A lower barrier means way more cars get through per hour: a faster reaction. That is the entire definition — **a catalyst provides an alternative pathway with a lower activation energy.** It does *not* shove cars over the old pass; it *opens a new road*.

**The tunnel surviving is the catalyst being regenerated.** This is the piece people forget. The tunnel doesn't wear out when a car drives through — it's still there, unchanged, for the next car. A catalyst is chemically used up early in the mechanism and then handed *back* later, so at the end you have exactly as much of it as you started with. It's a participant that comes out clean.

**And here's the subtle, exam-critical part: the elevation of the trailheads doesn't move.** The starting town is at some altitude; LA is at some altitude. The tunnel changes the *hump between them* — it does **not** raise or lower either endpoint. So the *difference* in elevation between start and finish is exactly the same with the tunnel as without it. That elevation difference is $\Delta H$, the enthalpy change. **A catalyst never changes $\Delta H$.** It only changes how hard the trip in the middle is.

One more thing the tunnel makes obvious. A tunnel is a two-way road. It helps cars going *to* LA and cars coming *back* equally well — the lowered barrier is lowered for both directions. That's why a catalyst speeds up the **forward and reverse reactions by the same factor**, which (jump ahead to Unit 7) is exactly why it reaches equilibrium **faster** but lands on the **same** equilibrium position.

### The Formal Definition

A **catalyst** is a substance that:

1. **Increases the reaction rate** by providing an **alternative reaction mechanism** with a **lower activation energy** $E_a$.
2. Is **not consumed** in the overall reaction — it is regenerated, so it does not appear in the overall balanced equation (it's often written over the arrow instead).
3. Speeds up the **forward and reverse** reactions equally.
4. Does **not** change $\Delta H$, the identity of the products, the amount of product at equilibrium, or the **equilibrium constant** $K$.

Written over the arrow, a catalyzed reaction looks like this:

$$\ce{2H2O2 ->[\ce{MnO2}] 2H2O + O2}$$

The $\ce{MnO2}$ sits *over* the arrow, not in it, precisely because it comes out at the end exactly as it went in.

> **The one-sentence version:** A catalyst lowers the activation energy by opening a new pathway, speeds up both directions, and is regenerated — so it changes the **rate** but never the **thermodynamics**.

### The Energy-Profile Picture

This is the single most tested diagram in Unit 5, so let's build it carefully — it's just the mountain-and-tunnel drawn as a graph. Recall the reaction energy profile from [Collision Model and Arrhenius](/chemistry/0704-collision-model-arrhenius): energy on the y-axis, reaction progress on the x-axis, reactants on the left, products on the right, and a hump in between whose height (measured up from the reactants) is $E_a$.

Now draw **two** curves on the **same** axes:

- **The uncatalyzed path (over the pass):** one **tall** hump. Its peak is high; $E_a$ is large.
- **The catalyzed path (through the tunnel):** a **lower** hump — or, very commonly, the *one* big hump splits into **two smaller humps** with a little dip between them. That dip is an **intermediate** the catalyst forms along the new route. Either way, the highest point the catalyzed path has to clear is **lower** than the uncatalyzed peak.

Three features **must** be identical on both curves, and this is where points are won and lost:

| Feature | Uncatalyzed | Catalyzed | Why |
|---|---|---|---|
| Reactant energy (left height) | same | **same** | Same starting town |
| Product energy (right height) | same | **same** | Same LA |
| $\Delta H$ = (products − reactants) | same | **same** | Endpoints didn't move |
| Peak height / $E_a$ | high | **lower** | The tunnel |

So the *only* thing the catalyst moves is the **top of the hump**. The left end, the right end, and therefore the vertical gap between them ($\Delta H$) are untouched. If your two curves start and end at different heights, you've drawn it wrong.

### The Maxwell–Boltzmann View

Here's *why* a lower hump means a faster reaction, told through the Maxwell–Boltzmann distribution from [Collision Model and Arrhenius](/chemistry/0704-collision-model-arrhenius) and [Kinetic Molecular Theory](/chemistry/0505-kinetic-molecular-theory).

That curve plots the fraction of molecules against their kinetic energy: a peak, then a long tail of high-energy molecules to the right. Somewhere on the energy axis is a vertical line at $E_a$ — the barrier. **Only the molecules to the right of that line** (in the shaded tail) have enough energy to react on any given collision. The area of that tail is the fraction of successful collisions.

There are two ways to fatten that tail:

1. **Heat the gas up** (from [Collision Model and Arrhenius](/chemistry/0704-collision-model-arrhenius)): the whole curve shifts and spreads to the right, so more molecules end up past the line. You moved the *molecules* toward the barrier.
2. **Add a catalyst:** the curve stays put, but the **$E_a$ line slides to the left** (lower barrier). Now a much bigger slice of the *same* distribution sits to the right of it. You moved the *barrier* toward the molecules.

Different mechanism, identical payoff: a **larger fraction of molecules clears the barrier**, so the rate goes up. Heating and catalyzing are two roads to the same shaded-tail destination.

### A Catalyst Inside a Mechanism

A catalyst isn't magic — it participates in real elementary steps from [Reaction Mechanisms](/chemistry/0705-reaction-mechanisms). The tell is simple:

> A **catalyst** is a species that is **consumed in an early step and regenerated in a later step**, so it cancels out of the overall reaction.

Contrast it with an **intermediate**, which is the mirror image:

| Species | Life cycle | Appears in overall equation? |
|---|---|---|
| **Catalyst** | Present at start → **used up first**, then **remade** | No — it's regenerated |
| **Intermediate** | Not present at start → **made first**, then **used up** | No — it's consumed |

Say it out loud and the difference sticks: a **catalyst is used, then remade**; an **intermediate is made, then used**. Both cancel when you add the steps, but one was in your hand at the beginning (catalyst) and the other was never there until the reaction created it (intermediate).

Example mechanism:

$$\text{Step 1: } \ce{NO2 + NO2 -> NO3 + NO}$$
$$\text{Step 2: } \ce{NO3 + CO -> NO2 + CO2}$$

Add them and cancel: $\ce{NO3}$ appears in step 1 as a product and step 2 as a reactant — it's **made then used**, so $\ce{NO3}$ is an **intermediate**. Now consider a different reaction where $\ce{NO}$ shows up first as a reactant and is spat back out at the end — that would be the catalyst. The habit to build: line up the steps, cancel, and label who was used-then-remade versus made-then-used.

---

## Worked Examples

### Example 1: What a Catalyst Actually Changes

**Problem:** A student says, "Adding a catalyst gives the reactant molecules extra energy so they can get over the activation-energy hump." What's wrong with this, and what's the correct statement?

**Solution:**

- Step 1: A catalyst does **not** add energy to molecules. It doesn't push cars over the old pass.
- Step 2: It provides a **new mechanism** with a **lower** $E_a$ — a tunnel through the mountain, not a boost over it.

**Answer:** A catalyst lowers the activation energy by opening an alternative pathway; it does not give molecules energy. The molecules' energy distribution is unchanged — the *barrier* is what moves.

### Example 2: Reading the Two-Curve Diagram

**Problem:** On one set of axes you see two curves for the same reaction. Curve A peaks at $150\ \text{kJ}$ above the reactants; curve B has two small humps, the taller reaching $60\ \text{kJ}$ above the reactants. Both curves start and end at the same heights. Which is catalyzed, and what is each activation energy?

**Solution:**

- Step 1: The catalyzed path has the **lower** overall barrier and often shows **multiple** small humps (an intermediate).
- Step 2: Curve B tops out at $60\ \text{kJ}$; curve A at $150\ \text{kJ}$. $E_a$ is the peak height above reactants.

**Answer:** Curve B is catalyzed. $E_{a,\text{uncat}} = 150\ \text{kJ/mol}$, $E_{a,\text{cat}} = 60\ \text{kJ/mol}$.

### Example 3: Does the Catalyst Change $\Delta H$?

**Problem:** For the reaction in Example 2, the reactants sit at $0\ \text{kJ}$ and the products at $-40\ \text{kJ}$ on the uncatalyzed curve. What is $\Delta H$ on the catalyzed curve?

**Solution:**

- Step 1: $\Delta H = (\text{products}) - (\text{reactants}) = -40 - 0 = -40\ \text{kJ/mol}$ uncatalyzed.
- Step 2: A catalyst never moves the endpoints — same start, same finish.

**Answer:** $\Delta H = -40\ \text{kJ/mol}$, exactly the same as uncatalyzed. The reaction is exothermic either way.

### Example 4: Catalyst or Intermediate?

**Problem:** In the mechanism below, identify the catalyst and the intermediate.

$$\text{Step 1: } \ce{H2O2 + I- -> H2O + IO-}$$
$$\text{Step 2: } \ce{H2O2 + IO- -> H2O + O2 + I-}$$

**Solution:**

- Step 1: Add the steps. $\ce{I-}$ is a **reactant in step 1** and a **product in step 2** → present at the start, used, then remade → **catalyst**.
- Step 2: $\ce{IO-}$ is a **product in step 1** and a **reactant in step 2** → made first, then used → **intermediate**.
- Step 3: Overall: $\ce{2H2O2 -> 2H2O + O2}$. Both $\ce{I-}$ and $\ce{IO-}$ cancel.

**Answer:** $\ce{I-}$ is the catalyst (used then regenerated); $\ce{IO-}$ is the intermediate (made then consumed).

### Example 5: Writing the Catalyzed Overall Equation

**Problem:** Hydrogen peroxide decomposes with manganese(IV) oxide as a catalyst. Write the overall equation showing the catalyst correctly.

**Solution:**

- Step 1: The products of $\ce{H2O2}$ decomposition are water and oxygen gas.
- Step 2: A catalyst is regenerated, so it goes **over the arrow**, not in the equation.

**Answer:** $\ce{2H2O2 ->[\ce{MnO2}] 2H2O + O2}$. The $\ce{MnO2}$ is recovered unchanged.

### Example 6: The Maxwell–Boltzmann Explanation

**Problem:** Using the Maxwell–Boltzmann distribution, explain in full-credit language why a catalyst increases the reaction rate.

**Solution:**

- Step 1: The rate depends on the fraction of collisions with energy $\geq E_a$ — the area of the distribution's tail to the right of the $E_a$ line.
- Step 2: A catalyst lowers $E_a$, sliding that line to the **left**.
- Step 3: The same distribution now has a **larger fraction** of molecules to the right of the line.

**Answer:** By lowering $E_a$, the catalyst increases the fraction of molecular collisions that have enough energy to react; more effective collisions per second means a faster rate. The distribution itself is unchanged — only the threshold moves.

### Example 7: Catalyst and Equilibrium (Unit 7 Preview)

**Problem:** A reversible reaction reaches equilibrium in 2 hours. A catalyst is added. Does the equilibrium shift? Does it change how much product forms at equilibrium? Does it change how *fast* equilibrium is reached?

**Solution:**

- Step 1: A catalyst speeds forward and reverse **equally**, so it can't favor one side — no shift, same $K$.
- Step 2: Same $K$ and same conditions → same equilibrium amounts of product.
- Step 3: But both directions are faster, so equilibrium arrives sooner.

**Answer:** No shift and no change in the amount of product at equilibrium (or in $K$); the system simply **reaches** equilibrium faster. (This is a Unit 7 staple.)

### Example 8: Classifying — Homogeneous or Heterogeneous?

**Problem:** Classify each: (a) $\ce{Cl}$ radicals (gas) speeding up the destruction of ozone $\ce{O3}$ (gas); (b) solid $\ce{Pt}$ speeding up the reaction of $\ce{CO}$ (gas) with $\ce{NO}$ (gas) in a car's exhaust.

**Solution:**

- Step 1: **Homogeneous** = catalyst in the **same phase** as the reactants. **Heterogeneous** = **different phase**.
- Step 2: (a) $\ce{Cl}$ and $\ce{O3}$ are both gases → same phase → homogeneous.
- Step 3: (b) Solid $\ce{Pt}$ with gaseous reactants → different phase → heterogeneous.

**Answer:** (a) Homogeneous; (b) heterogeneous.

### Example 8b: The Catalytic Converter, Step by Step

**Problem:** In the catalytic converter in Ganga and Dad's car, a $\ce{Pt}$/$\ce{Pd}$ surface turns toxic $\ce{CO}$ and $\ce{NO}$ from the engine into harmless $\ce{CO2}$ and $\ce{N2}$. Write the reaction, state the catalyst type, and explain what the surface does.

**Solution:**

- Step 1: The reaction: $\ce{2CO + 2NO ->[\ce{Pt}/\ce{Pd}] 2CO2 + N2}$.
- Step 2: The catalyst is a **solid** metal; the reactants are **gases** → different phases → **heterogeneous**.
- Step 3: The gas molecules **adsorb** (stick) onto the metal surface, which weakens their bonds and holds them close in the right orientation — a lower-$E_a$ pathway. Products then desorb, leaving the surface free for the next molecules (regenerated).

**Answer:** $\ce{2CO + 2NO ->[\ce{Pt}/\ce{Pd}] 2CO2 + N2}$; a heterogeneous catalyst that works by surface adsorption, and the metal is left unchanged for the next cycle.

### Example 9: The Cracker Test (Enzymes)

**Problem:** You chew a plain saltine cracker slowly and after about 30 seconds it tastes sweet, even though you added no sugar. Explain using catalysis vocabulary.

**Solution:**

- Step 1: Saliva contains **amylase**, an **enzyme** — a biological catalyst (a protein).
- Step 2: Amylase provides a low-$E_a$ pathway that breaks **starch** (tasteless long chains) into **sugars** (sweet) far faster than it would happen on its own.
- Step 3: The amylase isn't used up — each molecule breaks down starch after starch, so a tiny amount converts a lot.

**Answer:** Amylase, an enzyme, catalyzes the breakdown of starch into sugar in your mouth; it's regenerated, so a small amount keeps working — hence the growing sweetness.

### Example 10: Why Enzymes Care About Temperature and pH

**Problem:** Why does a fever or a very acidic environment slow or stop an enzyme, even though "more heat usually means faster reactions"?

**Solution:**

- Step 1: An enzyme works by its **active site** — a specifically shaped pocket that fits the reactant (**lock-and-key**).
- Step 2: Too much heat or the wrong pH **denatures** the enzyme: the protein loses its shape, so the active site no longer fits the reactant.
- Step 3: A catalyst with a broken active site can't lower $E_a$ anymore, so the rate crashes despite the higher temperature.

**Answer:** Enzymes depend on a precise 3-D shape; extreme temperature or pH denatures them and destroys the active site, so they stop catalyzing — the shape matters more than the extra thermal energy.

### Example 11: Spotting the Poisoned Catalyst

**Problem:** Cars with catalytic converters must use **unleaded** gasoline. Leaded gas ruins the converter permanently. What's happening, in catalysis terms?

**Solution:**

- Step 1: The converter works because reactant gases adsorb onto the $\ce{Pt}$/$\ce{Pd}$ surface.
- Step 2: **Lead** binds tightly to those surface sites and doesn't leave — it **poisons** the catalyst by blocking the active sites.
- Step 3: With the sites occupied, no reactant can adsorb, so the low-$E_a$ pathway is gone.

**Answer:** Lead is a catalyst poison: it permanently blocks the surface sites, so the catalyst can no longer provide its pathway — the reason leaded gas is banned for these cars.

### Example 12: Everything Together

**Problem:** A catalyzed reaction has $E_{a,\text{forward}} = 30\ \text{kJ}$ and $E_{a,\text{reverse}} = 50\ \text{kJ}$. (a) Is it exothermic or endothermic? (b) What is $\Delta H$? (c) If a *better* catalyst dropped $E_{a,\text{forward}}$ to $20\ \text{kJ}$, what would $\Delta H$ become?

**Solution:**

- Step 1: $\Delta H = E_{a,\text{forward}} - E_{a,\text{reverse}} = 30 - 50 = -20\ \text{kJ}$ → negative → **exothermic**.
- Step 2: (b) $\Delta H = -20\ \text{kJ/mol}$.
- Step 3: (c) A catalyst never changes $\Delta H$ — it only lowers the humps. The endpoints don't move.

**Answer:** (a) Exothermic; (b) $\Delta H = -20\ \text{kJ/mol}$; (c) still $-20\ \text{kJ/mol}$ — a better catalyst lowers $E_a$ further but leaves $\Delta H$ untouched.

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| "A catalyst gives molecules energy to get over the barrier" | Confusing lowering the barrier with pushing molecules | A catalyst **lowers $E_a$ / opens a new pathway** — it never adds energy. The tunnel doesn't push cars; it's a lower road |
| Drawing catalyzed and uncatalyzed curves ending at **different** product heights | Thinking the catalyst changes the products or $\Delta H$ | Both curves share the **same** reactant and product levels; only the **peak** differs. $\Delta H$ is identical |
| "A catalyst shifts the equilibrium toward products" | Assuming faster = more product | It speeds **both** directions equally → **no shift**, same $K$, same amount of product; only **faster** to get there (Unit 7) |
| Calling the catalyst an intermediate (or vice versa) | Both cancel from the overall equation | **Catalyst = used then remade** (there at the start). **Intermediate = made then used** (not there at the start) |
| Saying a catalyst is "used up" | It reacts in an early step, so it looks consumed | It's **regenerated** in a later step; it goes **over the arrow**, not in the overall equation |
| Mixing up homogeneous and heterogeneous | The words are long and similar | **Homo = same** phase; **hetero = different** phase (like a solid catalyst with gas reactants) |
| Forgetting enzymes are catalysts | They have their own biology vocabulary | An **enzyme is just a biological catalyst** (a protein); lock-and-key active site, denatured by heat/pH |

---

## AP Exam Tips

- **The two-curve energy diagram is nearly guaranteed.** Practice drawing uncatalyzed (tall hump) and catalyzed (lower hump, often split into two) on the **same** axes with the **same** reactant and product energies. Label both $E_a$ values and show that $\Delta H$ is unchanged. Different endpoints = lost points.
- **Say the magic words: "lowers the activation energy by providing an alternative pathway/mechanism."** Never write "gives the molecules energy" or "makes the molecules move faster" — those earn zero.
- **$\Delta H$, products, and equilibrium position are all unchanged.** If a question asks what a catalyst does to $\Delta H$, $K$, or the amount of product at equilibrium, the answer is **nothing** — it only changes the **rate**. This is a direct Unit 7 tie-in.
- **A catalyst speeds up both directions.** Full-credit reasoning for "no equilibrium shift" is that forward and reverse rates increase by the same factor.
- **Regenerated, not consumed.** To identify a catalyst in a mechanism, find the species that's a **reactant in an early step and a product in a later step**. It won't appear in the overall equation.
- **Enzyme = biological catalyst.** If a biology-flavored question mentions an enzyme, active site, or "-ase," treat it exactly like any catalyst: it lowers $E_a$ and is regenerated.
- **Maxwell–Boltzmann justification.** If asked *why* a lower $E_a$ speeds things up, reference the distribution: lowering $E_a$ moves the threshold left, so a **larger fraction of collisions** has enough energy to react.

---

## Practice Problems

### Problem 1
In one sentence, define a catalyst using the words "pathway" and "activation energy."

<details>
<summary><strong>Solution</strong></summary>

A catalyst is a substance that speeds up a reaction by providing an alternative **pathway** (mechanism) with a lower **activation energy**, and it is regenerated rather than consumed.

**A lower-$E_a$ alternative pathway; not used up overall.**

</details>

---

### Problem 2
On a reaction energy profile, name the one and only feature a catalyst changes, and name three features it leaves alone.

<details>
<summary><strong>Solution</strong></summary>

A catalyst lowers the **peak height** (the activation energy). It leaves unchanged the **reactant energy**, the **product energy**, and therefore **$\Delta H$**.

**Changes: the hump ($E_a$). Unchanged: reactant level, product level, $\Delta H$.**

</details>

---

### Problem 3
A reaction has $E_a = 120\ \text{kJ/mol}$ uncatalyzed and $\Delta H = +25\ \text{kJ/mol}$. A catalyst lowers $E_a$ to $70\ \text{kJ/mol}$. What is $\Delta H$ for the catalyzed reaction?

<details>
<summary><strong>Solution</strong></summary>

A catalyst never changes $\Delta H$. It only lowers the activation energy.

**$\Delta H = +25\ \text{kJ/mol}$ (unchanged; still endothermic).**

</details>

---

### Problem 4
Identify the catalyst and the intermediate in this mechanism:

$$\text{Step 1: } \ce{O3 + Cl -> O2 + ClO}$$
$$\text{Step 2: } \ce{ClO + O -> O2 + Cl}$$

<details>
<summary><strong>Solution</strong></summary>

$\ce{Cl}$ is a reactant in step 1 and a product in step 2 → present at the start, used then remade → **catalyst**. $\ce{ClO}$ is a product in step 1 and a reactant in step 2 → made then used → **intermediate**. Overall: $\ce{O3 + O -> 2O2}$.

**Catalyst: $\ce{Cl}$. Intermediate: $\ce{ClO}$.** (This is real ozone-layer chemistry.)

</details>

---

### Problem 5
Classify each catalyst as homogeneous or heterogeneous: (a) an aqueous acid catalyzing an aqueous reaction; (b) solid iron catalyzing the reaction of $\ce{N2}$ and $\ce{H2}$ gases into ammonia.

<details>
<summary><strong>Solution</strong></summary>

(a) Acid and reactants are both aqueous → same phase → **homogeneous**. (b) Solid iron with gaseous reactants → different phases → **heterogeneous** (this is the Haber process).

**(a) Homogeneous; (b) heterogeneous.**

</details>

---

### Problem 6
Explain, using the Maxwell–Boltzmann distribution, why lowering $E_a$ increases the reaction rate.

<details>
<summary><strong>Solution</strong></summary>

The rate depends on the fraction of molecules with energy at least $E_a$ — the tail of the distribution to the right of the $E_a$ line. Lowering $E_a$ slides that line to the left, so a **larger fraction** of the (unchanged) distribution lies past it. More collisions have enough energy to react, so the rate increases.

**Lower $E_a$ → threshold line moves left → bigger fraction of effective collisions → faster.**

</details>

---

### Problem 7
A catalyst is added to a system already at equilibrium. State the effect (if any) on: (a) the position of equilibrium, (b) the value of $K$, (c) the time to reach equilibrium, (d) the amount of product at equilibrium.

<details>
<summary><strong>Solution</strong></summary>

A catalyst speeds forward and reverse equally. (a) **No shift.** (b) **No change** in $K$. (c) Equilibrium is reached **faster**. (d) **No change** in the amount of product.

**Only the speed to equilibrium changes; everything about the equilibrium state is unchanged.**

</details>

---

### Problem 8
Why is a catalyst written over the reaction arrow rather than as a reactant or product?

<details>
<summary><strong>Solution</strong></summary>

Because it is regenerated — consumed in an early step and remade in a later step — it comes out at the end in the same amount and form it went in. It therefore cancels from the overall balanced equation and is shown over the arrow.

**It's not consumed overall, so it doesn't belong in the overall equation.**

</details>

---

### Problem 9
Chewing a plain cracker for 30 seconds makes it taste sweet. Name the catalyst, its type, and what reaction it speeds up.

<details>
<summary><strong>Solution</strong></summary>

The catalyst is **amylase**, an **enzyme** (biological catalyst) in saliva. It speeds the breakdown of **starch** into **sugars**, which taste sweet. The amylase is regenerated, so a little keeps converting starch.

**Amylase (an enzyme); it catalyzes starch → sugar.**

</details>

---

### Problem 10
A reaction is catalyzed by a solid metal surface. State the catalyst type and describe, in two steps, how the surface speeds up the reaction.

<details>
<summary><strong>Solution</strong></summary>

Type: **heterogeneous** (solid catalyst, fluid reactants). Mechanism: (1) reactant molecules **adsorb** onto the surface, which weakens their bonds and holds them in a favorable orientation, lowering $E_a$; (2) the products then **desorb**, freeing the surface for the next molecules (the catalyst is regenerated).

**Heterogeneous; adsorption weakens/orients bonds, then products desorb and the surface is reused.**

</details>

---

### Problem 11
Why must a car with a catalytic converter use unleaded gasoline?

<details>
<summary><strong>Solution</strong></summary>

Lead is a **catalyst poison**: it binds tightly to the active sites on the $\ce{Pt}$/$\ce{Pd}$ surface and doesn't leave, blocking reactant molecules from adsorbing. With the sites blocked, the low-$E_a$ pathway is destroyed and the converter stops working — permanently.

**Lead poisons the catalyst by permanently blocking its surface active sites.**

</details>

---

### Problem 12
A friend claims, "A catalyst can turn an endothermic reaction into an exothermic one if it lowers the barrier enough." Correct them.

<details>
<summary><strong>Solution</strong></summary>

The sign of $\Delta H$ depends only on the relative energies of reactants and products — the endpoints. A catalyst lowers the barrier (the peak) but never moves the endpoints, so $\Delta H$ and its sign are unchanged. An endothermic reaction stays endothermic.

**No — a catalyst changes $E_a$, never $\Delta H$; it can't flip endothermic to exothermic.**

</details>

---

### Problem 13
The forward activation energy of a catalyzed reaction is $40\ \text{kJ/mol}$ and the reverse is $65\ \text{kJ/mol}$. (a) Find $\Delta H$. (b) Is the reaction exothermic or endothermic? (c) By how much did a catalyst change $\Delta H$ compared to the uncatalyzed reaction?

<details>
<summary><strong>Solution</strong></summary>

(a) $\Delta H = E_{a,\text{fwd}} - E_{a,\text{rev}} = 40 - 65 = -25\ \text{kJ/mol}$. (b) Negative → **exothermic**. (c) A catalyst never changes $\Delta H$, so the change is **zero** — $\Delta H$ is the same as uncatalyzed.

**(a) $-25\ \text{kJ/mol}$; (b) exothermic; (c) no change — catalysts don't affect $\Delta H$.**

</details>

---

### Problem 14
Both raising the temperature and adding a catalyst increase a reaction's rate. Using the Maxwell–Boltzmann picture, explain how the *mechanism* of the speed-up differs between the two.

<details>
<summary><strong>Solution</strong></summary>

Raising the temperature **shifts and spreads the distribution to the right**, moving the molecules toward higher energies so more of them exceed the fixed $E_a$ line. Adding a catalyst leaves the distribution fixed but **moves the $E_a$ line to the left** (lower barrier), so more of the same molecules exceed it. One moves the molecules; the other moves the barrier — both enlarge the fraction of effective collisions.

**Heat moves the molecules toward the barrier; a catalyst moves the barrier toward the molecules.**

</details>

---

### Problem 15
Sketch-describe (in words) the two curves you would draw for a reaction with and without a catalyst, and list the labels that must appear for full credit.

<details>
<summary><strong>Solution</strong></summary>

On one set of axes (energy vs. reaction progress): both curves **start at the same reactant energy** on the left and **end at the same product energy** on the right. The **uncatalyzed** curve has a single **tall** hump; the **catalyzed** curve has a **lower** hump (often two smaller humps with a dip for an intermediate). Labels required: the axes (energy, reaction progress), reactants, products, **$E_{a,\text{uncatalyzed}}$**, **$E_{a,\text{catalyzed}}$**, and **$\Delta H$** (the same vertical gap between reactants and products for both curves).

**Same endpoints, tall hump vs. lower hump, both $E_a$ values labeled, one shared $\Delta H$.**

</details>

---

## Quick Reference

**What a catalyst does — and doesn't**

| A catalyst DOES | A catalyst does NOT |
|---|---|
| Lower the activation energy $E_a$ | Add energy to molecules |
| Provide an alternative mechanism/pathway | Change the products |
| Speed up forward **and** reverse equally | Shift the equilibrium position or change $K$ |
| Get regenerated (not consumed overall) | Change $\Delta H$ |
| Increase the **rate** | Change the amount of product at equilibrium |

**Catalyst vs. intermediate**

| | Life cycle | In overall equation? |
|---|---|---|
| **Catalyst** | Used first, then remade (present at start) | No — over the arrow |
| **Intermediate** | Made first, then used (not present at start) | No — cancels out |

**Types of catalysts**

| Type | Phase relationship | Real example |
|---|---|---|
| **Homogeneous** | Same phase as reactants | $\ce{Cl}$ radicals destroying ozone; aqueous acid catalysis |
| **Heterogeneous** | Different phase (usually solid + gas/liquid) | $\ce{Pt}$/$\ce{Pd}$ catalytic converter: $\ce{2CO + 2NO -> 2CO2 + N2}$ |
| **Enzyme** | Biological catalyst (protein) | Amylase breaking starch → sugar; lock-and-key active site |

**Key facts**

- Energy diagram: two curves, **same** reactant and product levels, **lower** hump for catalyzed, **same $\Delta H$**.
- Maxwell–Boltzmann: lowering $E_a$ moves the threshold left → larger fraction of effective collisions → faster rate.
- Enzymes need the right **temperature** and **pH**; extremes **denature** them (active site loses shape).
- **Inhibitor / poison:** blocks or destroys the catalyst (e.g., lead poisoning a catalytic converter).

---

<div align="center">

[← Reaction Mechanisms](/chemistry/0705-reaction-mechanisms) | [Energy and Heat →](/chemistry/0801-energy-and-heat)

</div>
