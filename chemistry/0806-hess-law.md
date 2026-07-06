# Hess's Law
<p class="article-date">July 5, 2026</p>

*Every summer Dad and I drive up to Big Bear, and it starts at the beach. We leave our sea-level street in San Diego, wind through traffic, and a couple hours later we're standing in pine trees at about 6,750 feet, ears popping the whole way. Here's the thing I finally noticed this year: it doesn't matter HOW we get there. Some years Dad takes the fast freeway straight up the mountain. Other years he insists on a scenic backroad detour that dips into a valley, climbs a ridge, drops again, and doubles the drive time. Different roads, different ups and downs, wildly different mileage — but the net elevation gain from our front door to the cabin is exactly the same 6,750 feet every single time. Because elevation only cares about where you START and where you END, not the path you took to connect them. That one idea — that some quantities depend only on the endpoints — is the entire secret of **Hess's Law**, the capstone of AP Unit 6. Enthalpy behaves exactly like elevation, and that lets us calculate the heat of a reaction we could never measure in the lab, just by stitching together reactions we already know.*

---

## What You'll Learn

- State **Hess's Law**: if a reaction can be written as the sum of two or more steps, its $\Delta H$ is the **sum of the steps' $\Delta H$ values**
- Explain *why* Hess's Law works by identifying enthalpy as a **state function** — a quantity that is **path-independent**, like elevation
- Explain *why it's useful* — it delivers $\Delta H$ for reactions that are too slow, too dangerous, or impossible to measure directly
- Apply the two manipulation rules: **reverse** a reaction → **flip the sign** of $\Delta H$; **scale** a reaction by a factor → **multiply** $\Delta H$ by that factor
- **Align and add** thermochemical equations so that intermediates **cancel**, leaving the exact target equation
- Run the full **flip / scale / add** recipe on 2- and 3-equation problems, showing every canceled species
- Recognize that the **formation-enthalpy formula** $\Delta H_\text{rxn} = \sum \Delta H_f^\circ(\text{products}) - \sum \Delta H_f^\circ(\text{reactants})$ **is Hess's Law** applied to formation reactions
- Read a **multi-level energy diagram** and see the total $\Delta H$ as the sum of the individual level changes
- Decide **when to use which method** — bond enthalpy (estimate), formation tables (exact), or Hess's Law (from given steps)

---

## Prerequisites

- [Enthalpy of Reaction](/chemistry/0803-enthalpy-of-reaction) — Hess's Law is built entirely on the two rules you learned there: **reversing** a reaction flips the sign of $\Delta H$, and **scaling** a reaction scales $\Delta H$. You must be fluent in those before anything here makes sense.
- [Enthalpy of Formation](/chemistry/0805-enthalpy-of-formation) — the "products minus reactants" formation shortcut is secretly *one specific application* of Hess's Law; this article is where the two ideas finally click together.

---

## The Core Concept

### Intuition First

Let's stay in Dad's car on the drive to Big Bear, because every piece of Hess's Law is sitting on that mountain road.

**Elevation is a "state function."** Our cabin is at 6,750 feet and our house is at 0 feet (sea level). The **change** in elevation for the trip is $6{,}750 - 0 = 6{,}750$ feet. That number is fixed. It's a property of the two *locations* — it does not know or care what road connected them. A quantity like this, one that depends only on the start and end states and not on the path, is called a **state function**. Elevation is the friendliest state function there is.

**The driving route is the reaction pathway.** The freeway is one route; the scenic backroad is another. In chemistry, there are many possible "routes" to turn a set of reactants into a set of products — you can go directly, or you can go through a chain of intermediate reactions. Each route is a different sequence of steps.

**Net elevation change is $\Delta H_\text{rxn}$.** Just as the net climb from home to cabin is 6,750 feet no matter the road, the net enthalpy change from reactants to products, $\Delta H_\text{rxn}$, is the same no matter which sequence of reactions you route through. **Enthalpy is a state function, so $\Delta H$ is path-independent.** That single sentence is the whole law.

**Stitching road segments together is adding thermochemical equations.** On the scenic route, Dad connects a bunch of individual road segments: climb this ridge (+2,000 ft), drop into that valley (−1,500 ft), grind up the final grade (+6,250 ft). Add those segment-by-segment elevation changes and you get the total: $+2{,}000 - 1{,}500 + 6{,}250 = +6{,}750$ ft — the same net climb. In chemistry, we connect known reaction steps end to end, and the total $\Delta H$ is just the sum of the steps' $\Delta H$ values.

**Driving a segment backward flips its sign.** If one leg of the trip is a road we *descend* on the way up (say the road normally goes downhill in the "forward" direction but we drive it in reverse to gain 1,500 ft), the elevation change flips sign. Same road, opposite direction, opposite sign. In chemistry, **reversing a reaction flips the sign of its $\Delta H$**: if forward releases 200 kJ ($\Delta H = -200$), backward absorbs 200 kJ ($\Delta H = +200$).

**Driving a segment twice doubles it.** If we had to climb the same 1,000-ft grade twice (loop back and do it again), that leg contributes +2,000 ft. In chemistry, **doubling a reaction doubles its $\Delta H$**; tripling triples it; halving halves it. Whatever factor you scale the equation by, you scale $\Delta H$ by the same factor.

Here's the map to carry through the whole article:

| The drive to Big Bear | The chemistry |
|---|---|
| **Elevation** (depends only on location) | **Enthalpy**, $H$ — a **state function** |
| Net climb, home → cabin | $\Delta H_\text{rxn}$ (reactants → products) |
| Fast freeway vs. scenic backroad | different **reaction pathways** |
| Net climb is the same on either road | $\Delta H$ is **path-independent** |
| Stitching road segments together | **adding** thermochemical equations |
| Driving a segment **backward** | **reversing** a reaction → flip sign of $\Delta H$ |
| Driving a segment **twice** | **doubling** a reaction → double $\Delta H$ |
| A ridge you climb and later re-descend | an **intermediate** that cancels out |

That last row is the payoff. On the scenic route Dad sometimes climbs a ridge and then comes right back down the other side. That ridge's up-and-down **cancels** — it adds nothing to the net climb. In Hess's Law, chemical species that show up as a *product* in one step and a *reactant* in another **cancel** exactly the same way. They're intermediates: places the route passes through but the endpoints never see.

### Hess's Law, Formally

> **Hess's Law of Constant Heat Summation:** If a chemical reaction can be expressed as the sum of a series of steps, then the enthalpy change of the overall reaction equals the sum of the enthalpy changes of the individual steps.

$$\Delta H_\text{rxn} = \sum_i \Delta H_i$$

It works because **enthalpy is a state function**: $\Delta H$ depends only on the identity and amount of the reactants and products, not on the mechanism or route taken to get from one to the other. Whether a reaction happens in one violent step or fifty gentle ones, the total heat is fixed.

**Why we care.** Some reactions can't be measured directly in a calorimeter:

- **Too slow.** Carbon and oxygen forming *exactly* $\ce{CO}$ (carbon monoxide) and stopping there is impossible — you always get some $\ce{CO2}$ too. You can't cleanly measure that heat.
- **Too dangerous or messy.** Many reactions produce side products, need extreme conditions, or explode.
- **Impossible to isolate.** You may want the enthalpy of forming a compound directly from its elements, but the elements might refuse to react that way.

Hess's Law is the workaround: measure the easy reactions, then **algebraically combine** them to reach the hard one. It's the freeway being closed, so you take three backroads that happen to connect the same two points.

### The Two Manipulation Rules (straight from [Enthalpy of Reaction](/chemistry/0803-enthalpy-of-reaction))

You already own both of these:

**Rule 1 — Reverse → flip the sign.**

$$\ce{A -> B}, \ \Delta H = -x \quad\Longrightarrow\quad \ce{B -> A}, \ \Delta H = +x$$

Running a reaction backward absorbs exactly the heat the forward direction released (and vice versa).

**Rule 2 — Scale → multiply $\Delta H$ by the same factor.**

$$\ce{A -> B}, \ \Delta H = y \quad\Longrightarrow\quad \ce{2A -> 2B}, \ \Delta H = 2y \quad\text{and}\quad \ce{1/2 A -> 1/2 B}, \ \Delta H = \tfrac{1}{2}y$$

$\Delta H$ is an **extensive** quantity — twice the stuff, twice the heat.

**Then: align and ADD.** Once each given equation is flipped and/or scaled so its species land on the correct sides, stack them up and add. Any species appearing as a reactant in one line and a product in another (in equal amounts) **cancels**. What survives must be exactly the target equation, and the sum of the manipulated $\Delta H$ values is your answer.

### The Systematic Recipe

Here is the step-by-step method to run on every Hess's Law problem:

1. **Write the target equation** clearly, and mark which side each species needs to end up on.
2. **Look at each given equation** and ask, for each species that appears in the target: is it on the correct side already? If not, **reverse** that equation (flip $\Delta H$'s sign).
3. **Match the coefficients.** If the target needs 2 mol of something but a given equation has 1 mol, **scale** that equation (and its $\Delta H$) by the needed factor.
4. **Check the intermediates.** Species *not* in the target must appear on opposite sides across your manipulated equations so they **cancel**. If they don't cancel, re-examine your flipping/scaling.
5. **Add the manipulated equations**, cancel the intermediates, and confirm the leftover equation is *exactly* the target.
6. **Add the manipulated $\Delta H$ values** — that sum is $\Delta H_\text{rxn}$.

> **Pro tip:** Start from the *target* and work outward. Pick the given equation that contains a species appearing in only ONE place across all the givens — that species' position forces whether you flip or scale, and everything else falls into line from there.

### An Energy-Diagram View

Hess's Law is easiest to *see* on a multi-level energy diagram. Picture the reaction $\ce{A -> C}$ that we route through an intermediate $\ce{B}$:

```
  enthalpy
     |
  A  |____
     |    \   step 1: A -> B, ΔH1 = -50 kJ
     |     \
  B  |      \____
     |           \   step 2: B -> C, ΔH2 = -30 kJ
     |            \
  C  |             \____
     |________________________  reaction progress

   Total: A -> C, ΔH = ΔH1 + ΔH2 = -50 + (-30) = -80 kJ
```

The molecule drops 50 kJ from $\ce{A}$ down to $\ce{B}$, then another 30 kJ from $\ce{B}$ down to $\ce{C}$. The **total** drop from $\ce{A}$ to $\ce{C}$ is 80 kJ — the sum of the two level changes. It's Dad's scenic route drawn sideways: the elevation of the endpoints is fixed, and the little climbs and drops in between always add up to the same net change. If a step went *up* instead of down, its $\Delta H$ would be positive and you'd *subtract* that height — exactly the reversing rule.

### The Formation Connection (why [0805](/chemistry/0805-enthalpy-of-formation)'s formula IS Hess's Law)

In [Enthalpy of Formation](/chemistry/0805-enthalpy-of-formation) you used this shortcut:

$$\Delta H_\text{rxn}^\circ = \sum n\,\Delta H_f^\circ(\text{products}) - \sum n\,\Delta H_f^\circ(\text{reactants})$$

That "products minus reactants" formula isn't a separate law — **it is Hess's Law in disguise.** Here's the route it secretly takes:

1. **Disassemble every reactant into its elements.** A formation reaction *builds* a compound from its elements, so running it **backward** (reactant → elements) is a *reversed* formation reaction — and reversing flips the sign. That's where the **minus** on reactants comes from: $-\sum \Delta H_f^\circ(\text{reactants})$.
2. **Assemble every product from those elements.** Building each product *is* its formation reaction, run forward: $+\sum \Delta H_f^\circ(\text{products})$.

So the actual path is **reactants → bare elements → products**. The elements are the "sea-level base camp" every compound is measured from (their $\Delta H_f^\circ = 0$). Add the disassembly step (reversed formations, sign flipped) to the assembly step (forward formations), the elements cancel as intermediates, and you're left with reactants → products. That sum is precisely $\sum \Delta H_f^\circ(\text{prod}) - \sum \Delta H_f^\circ(\text{react})$. Same law, dressed up as a table lookup.

### Three Roads to the Same $\Delta H$

You now have three ways to find a reaction's enthalpy. In principle they **all agree** (Hess's Law guarantees it, since $\Delta H$ is path-independent):

| Method | What you need | Accuracy | Use when |
|---|---|---|---|
| **Bond enthalpies** | average bond-energy table | **Approximate** (averages) | you only have bond energies; gas-phase reactions; a quick estimate |
| **Formation enthalpies** | $\Delta H_f^\circ$ table | **Exact** (tabulated) | a formation table is provided — fastest exact route |
| **Hess's Law (given steps)** | 2–3 measured reactions | **Exact** | the problem hands you a set of reactions to combine |

Bond enthalpy is the estimate (it uses *average* bond strengths, so it's a little off); formation and Hess give exact answers. If a problem gives you a set of equations, it wants **Hess's Law**.

---

## Worked Examples

### Example 1: The Simplest Combine — Just Add

**Problem:** Given the two steps below, find $\Delta H$ for $\ce{N2(g) + 2O2(g) -> 2NO2(g)}$.

$$\ce{N2(g) + O2(g) -> 2NO(g)} \qquad \Delta H_1 = +180.5\ \text{kJ}$$
$$\ce{2NO(g) + O2(g) -> 2NO2(g)} \qquad \Delta H_2 = -114.1\ \text{kJ}$$

**Solution:**
- **Step 1 — Check sides.** Target has $\ce{N2}$ and $\ce{O2}$ as reactants, $\ce{NO2}$ as product. Equation 1 has $\ce{N2}$ on the left (good); equation 2 has $\ce{NO2}$ on the right (good). No flipping needed.
- **Step 2 — Check coefficients.** They already match. No scaling needed.
- **Step 3 — Add and cancel.** The intermediate is $\ce{NO}$: it's a *product* in eq 1 (2 mol) and a *reactant* in eq 2 (2 mol) — they cancel.

$$\ce{N2 + O2 + \cancel{2NO} + O2 -> \cancel{2NO} + 2NO2}$$

Combining the two $\ce{O2}$ on the left gives $\ce{N2 + 2O2 -> 2NO2}$. ✓ (exactly the target)
- **Step 4 — Add the $\Delta H$ values:** $\Delta H = +180.5 + (-114.1) = +66.4\ \text{kJ}$.

**Answer:** $\Delta H = +66.4\ \text{kJ}$.

### Example 2: Scaling a Single Reaction

**Problem:** Using $\ce{N2(g) + O2(g) -> 2NO(g)}$, $\Delta H = +180.5\ \text{kJ}$, find $\Delta H$ for $\ce{1/2 N2(g) + 1/2 O2(g) -> NO(g)}$.

**Solution:**
- The target is the given reaction scaled by $\tfrac{1}{2}$ (half of everything, giving 1 mol $\ce{NO}$).
- Scale $\Delta H$ by the same $\tfrac{1}{2}$: $\Delta H = \tfrac{1}{2}(+180.5) = +90.25\ \text{kJ}$.

**Answer:** $\Delta H = +90.3\ \text{kJ}$.

### Example 3: Reversing a Single Reaction

**Problem:** The combustion $\ce{C(s) + O2(g) -> CO2(g)}$ has $\Delta H = -393.5\ \text{kJ}$. Find $\Delta H$ for the decomposition $\ce{CO2(g) -> C(s) + O2(g)}$.

**Solution:**
- The target is the given reaction run **backward**.
- Reversing flips the sign: $\Delta H = -(-393.5) = +393.5\ \text{kJ}$.

**Answer:** $\Delta H = +393.5\ \text{kJ}$ (endothermic — it takes energy to pull $\ce{CO2}$ apart, exactly as much as burning released).

### Example 4: The Classic Carbon-Monoxide Problem (reverse one, then add)

**Problem:** You can't burn carbon to make *pure* $\ce{CO}$ — you always get some $\ce{CO2}$ — so $\Delta H$ for $\ce{C(s) + 1/2 O2(g) -> CO(g)}$ can't be measured directly. Find it from these two reactions you *can* measure:

$$\text{(i)}\quad \ce{C(s) + O2(g) -> CO2(g)} \qquad \Delta H_\text{i} = -393.5\ \text{kJ}$$
$$\text{(ii)}\quad \ce{CO(g) + 1/2 O2(g) -> CO2(g)} \qquad \Delta H_\text{ii} = -283.0\ \text{kJ}$$

**Solution:**
- **Step 1 — Target sides.** Target: $\ce{C}$ (reactant), $\ce{CO}$ (product). 
- **Step 2 — Place $\ce{C}$.** Equation (i) has $\ce{C}$ on the left, where we need it. **Keep (i) as-is.**
- **Step 3 — Place $\ce{CO}$.** We need $\ce{CO}$ as a *product*, but equation (ii) has it as a *reactant*. **Reverse (ii)** → flip its sign:

$$\ce{CO2(g) -> CO(g) + 1/2 O2(g)} \qquad \Delta H = +283.0\ \text{kJ}$$
- **Step 4 — Add and cancel.** Stack (i) and the reversed (ii):

$$\ce{C + O2 -> \cancel{CO2}}$$
$$\ce{\cancel{CO2} -> CO + 1/2 O2}$$

$\ce{CO2}$ cancels (product of one, reactant of the other). On the left we have $\ce{O2}$; on the right a $\ce{1/2 O2}$ — subtract to leave $\ce{1/2 O2}$ on the left:

$$\ce{C(s) + 1/2 O2(g) -> CO(g)} \checkmark$$
- **Step 5 — Add the $\Delta H$:** $\Delta H = -393.5 + (+283.0) = -110.5\ \text{kJ}$.

**Answer:** $\Delta H = -110.5\ \text{kJ}$.

### Example 5: Three Equations — Reverse One AND Double Another (formation of methane)

**Problem:** Find $\Delta H_f^\circ$ for methane, $\ce{C(s) + 2H2(g) -> CH4(g)}$, from these combustion data:

$$\text{(i)}\quad \ce{C(s) + O2(g) -> CO2(g)} \qquad \Delta H_\text{i} = -393.5\ \text{kJ}$$
$$\text{(ii)}\quad \ce{H2(g) + 1/2 O2(g) -> H2O(l)} \qquad \Delta H_\text{ii} = -285.8\ \text{kJ}$$
$$\text{(iii)}\quad \ce{CH4(g) + 2O2(g) -> CO2(g) + 2H2O(l)} \qquad \Delta H_\text{iii} = -890.4\ \text{kJ}$$

**Solution:**
- **Step 1 — Place $\ce{C}$.** Target needs $\ce{C}$ as a reactant. Equation (i) has it there. **Keep (i).**
- **Step 2 — Place $\ce{H2}$ and match its coefficient.** Target needs $\ce{2H2}$ as a reactant. Equation (ii) has $\ce{H2}$ on the left but only 1 mol. **Double (ii)** (and its $\Delta H$):

$$\ce{2H2(g) + O2(g) -> 2H2O(l)} \qquad \Delta H = 2(-285.8) = -571.6\ \text{kJ}$$
- **Step 3 — Place $\ce{CH4}$.** Target needs $\ce{CH4}$ as a *product*, but (iii) has it as a *reactant*. **Reverse (iii)** → flip sign:

$$\ce{CO2(g) + 2H2O(l) -> CH4(g) + 2O2(g)} \qquad \Delta H = +890.4\ \text{kJ}$$
- **Step 4 — Add and cancel the intermediates.** Stack the three manipulated equations. The intermediates $\ce{CO2}$, $\ce{H2O}$, and $\ce{O2}$ all cancel:
  - $\ce{CO2}$: product of (i), reactant of reversed (iii) — cancels.
  - $\ce{2H2O}$: product of doubled (ii), reactant of reversed (iii) — cancels.
  - $\ce{O2}$: left side has $\ce{O2}$ (from i) $+\ \ce{O2}$ (from doubled ii) $=\ce{2O2}$; right side has $\ce{2O2}$ (from reversed iii) — cancels.

  What survives: $\ce{C(s) + 2H2(g) -> CH4(g)}$ ✓
- **Step 5 — Sum the $\Delta H$ values:**

$$\Delta H = \underbrace{-393.5}_{\text{(i)}} + \underbrace{(-571.6)}_{2\times\text{(ii)}} + \underbrace{(+890.4)}_{-\text{(iii)}} = -74.7\ \text{kJ}$$

**Answer:** $\Delta H_f^\circ(\ce{CH4}) = -74.7\ \text{kJ/mol}$ — matches the accepted table value, and we never had to react carbon and hydrogen directly (which barely works).

### Example 6: Three-Equation Combine (formation of acetylene)

**Problem:** Find $\Delta H$ for $\ce{2C(s) + H2(g) -> C2H2(g)}$ (acetylene) from:

$$\text{(i)}\quad \ce{C(s) + O2(g) -> CO2(g)} \qquad \Delta H_\text{i} = -393.5\ \text{kJ}$$
$$\text{(ii)}\quad \ce{H2(g) + 1/2 O2(g) -> H2O(l)} \qquad \Delta H_\text{ii} = -285.8\ \text{kJ}$$
$$\text{(iii)}\quad \ce{2C2H2(g) + 5O2(g) -> 4CO2(g) + 2H2O(l)} \qquad \Delta H_\text{iii} = -2600.\ \text{kJ}$$

**Solution:**
- **Place $\ce{C}$:** target needs $\ce{2C}$ (reactant). **Double (i):** $\ce{2C + 2O2 -> 2CO2}$, $\Delta H = 2(-393.5) = -787.0$.
- **Place $\ce{H2}$:** target needs $\ce{H2}$ (reactant), 1 mol. **Keep (ii):** $\Delta H = -285.8$.
- **Place $\ce{C2H2}$:** target needs 1 mol $\ce{C2H2}$ as a *product*; (iii) has 2 mol as a *reactant*. **Reverse AND halve (iii)** (scale by $-\tfrac{1}{2}$):

$$\ce{2CO2(g) + H2O(l) -> C2H2(g) + 5/2 O2(g)} \qquad \Delta H = -\tfrac{1}{2}(-2600.) = +1300.\ \text{kJ}$$
- **Add and cancel.** $\ce{2CO2}$ cancels (product of doubled i, reactant of scaled iii). $\ce{H2O}$ cancels (product of ii, reactant of scaled iii). $\ce{O2}$: left has $\ce{2O2} + \ce{1/2 O2} = \ce{5/2 O2}$; right has $\ce{5/2 O2}$ — cancels. Left with $\ce{2C + H2 -> C2H2}$ ✓
- **Sum:** $\Delta H = -787.0 + (-285.8) + (+1300.) = +227.2\ \text{kJ}$.

**Answer:** $\Delta H = +227\ \text{kJ}$ (endothermic — acetylene stores energy, which is why it burns so hot).

### Example 7: Formation-of-a-Compound Target from Combustion Data (ethanol)

**Problem:** Find $\Delta H_f^\circ$ for liquid ethanol, $\ce{2C(s) + 3H2(g) + 1/2 O2(g) -> C2H5OH(l)}$, from:

$$\text{(i)}\quad \ce{C(s) + O2(g) -> CO2(g)} \qquad -393.5\ \text{kJ}$$
$$\text{(ii)}\quad \ce{H2(g) + 1/2 O2(g) -> H2O(l)} \qquad -285.8\ \text{kJ}$$
$$\text{(iii)}\quad \ce{C2H5OH(l) + 3O2(g) -> 2CO2(g) + 3H2O(l)} \qquad -1367\ \text{kJ}$$

**Solution:**
- **Double (i)** for $\ce{2C}$: $\Delta H = 2(-393.5) = -787.0$.
- **Triple (ii)** for $\ce{3H2}$: $\Delta H = 3(-285.8) = -857.4$.
- **Reverse (iii)** to put $\ce{C2H5OH}$ on the product side: $\Delta H = +1367$.
- **Cancel:** $\ce{2CO2}$ and $\ce{3H2O}$ cancel against the reversed combustion; the $\ce{O2}$ terms reconcile to leave a net $\ce{1/2 O2}$ on the left, exactly as the target requires.
- **Sum:** $\Delta H = -787.0 + (-857.4) + (+1367) = -277.4\ \text{kJ}$.

**Answer:** $\Delta H_f^\circ(\ce{C2H5OH}, l) \approx -277\ \text{kJ/mol}$.

### Example 8: The Formation Formula IS Hess's Law

**Problem:** Using $\Delta H_f^\circ$ values — $\ce{CH4(g)} = -74.8$, $\ce{CO2(g)} = -393.5$, $\ce{H2O(l)} = -285.8\ \text{kJ/mol}$ (and $\ce{O2}=0$) — find $\Delta H_\text{rxn}$ for $\ce{CH4(g) + 2O2(g) -> CO2(g) + 2H2O(l)}$, then explain how this *is* Hess's Law.

**Solution:**
- **Apply the formula** (products − reactants):

$$\Delta H_\text{rxn} = \big[(-393.5) + 2(-285.8)\big] - \big[(-74.8) + 2(0)\big]$$
$$= (-965.1) - (-74.8) = -890.3\ \text{kJ}$$
- **Why it's Hess's Law:** the formula is really routing through the elements. Step A: **disassemble** $\ce{CH4}$ into $\ce{C}$ and $\ce{2H2}$ — that's the reversed formation of methane, $\Delta H = -(-74.8) = +74.8$ (the sign flip is the *minus* on the reactant). Step B: **assemble** $\ce{CO2}$ and $\ce{2H2O}$ from those elements — forward formations, $\Delta H = -393.5 + 2(-285.8) = -965.1$. Add the two steps (the bare elements cancel as intermediates): $+74.8 + (-965.1) = -890.3\ \text{kJ}$. Identical.

**Answer:** $\Delta H_\text{rxn} = -890.3\ \text{kJ}$ — and "products minus reactants" is just Hess's Law routed **reactants → elements → products**.

### Example 9: Fractional Scaling

**Problem:** Given $\ce{2SO2(g) + O2(g) -> 2SO3(g)}$, $\Delta H = -198\ \text{kJ}$, find $\Delta H$ for $\ce{SO3(g) -> SO2(g) + 1/2 O2(g)}$.

**Solution:**
- **Step 1 — Scale.** The target involves 1 mol $\ce{SO3}$, but the given has 2 mol. Halve everything → scale $\Delta H$ by $\tfrac{1}{2}$: $-198 \times \tfrac{1}{2} = -99\ \text{kJ}$ for $\ce{SO2 + 1/2 O2 -> SO3}$.
- **Step 2 — Reverse.** The target runs that backward ($\ce{SO3}$ on the left). Flip the sign: $\Delta H = +99\ \text{kJ}$.

**Answer:** $\Delta H = +99\ \text{kJ}$ (you can flip and scale in either order — the result is the same).

### Example 10: Reading the Energy Diagram

**Problem:** A reaction goes $\ce{A -> C}$ through intermediate $\ce{B}$. Step 1 ($\ce{A -> B}$) has $\Delta H_1 = +40\ \text{kJ}$; step 2 ($\ce{B -> C}$) has $\Delta H_2 = -110\ \text{kJ}$. Sketch-describe the diagram and give $\Delta H$ for $\ce{A -> C}$.

**Solution:**
- From $\ce{A}$, the level rises 40 kJ up to $\ce{B}$ (endothermic step — a climb), then falls 110 kJ down to $\ce{C}$ (exothermic step — a drop). $\ce{C}$ ends up $40 - 110 = 70\ \text{kJ}$ *below* $\ce{A}$.
- Hess's Law: $\Delta H_\text{total} = \Delta H_1 + \Delta H_2 = +40 + (-110) = -70\ \text{kJ}$.

```
 A __
     \  +40      B
      \   ____/\
       \_/      \  -110
                 \____ C     net: A -> C, ΔH = -70 kJ
```

**Answer:** $\Delta H(\ce{A -> C}) = -70\ \text{kJ}$ — the net drop, exactly the ridge-then-valley picture from the mountain road.

### Example 11: Confirm by Reconstructing the Target

**Problem:** A student combines equations and gets $\Delta H = +66.4\ \text{kJ}$ for a target, but isn't sure the algebra was right. Their manipulated set is:

$$\ce{N2 + O2 -> 2NO} \qquad \ce{2NO + O2 -> 2NO2}$$

Show the check that confirms (or refutes) the target $\ce{N2 + 2O2 -> 2NO2}$.

**Solution:**
- **Add left sides:** $\ce{N2 + O2 + 2NO + O2} = \ce{N2 + 2O2 + 2NO}$.
- **Add right sides:** $\ce{2NO + 2NO2}$.
- **Cancel species on both sides:** $\ce{2NO}$ appears on both → cancel.
- **Remaining:** $\ce{N2 + 2O2 -> 2NO2}$ ✓ — matches the target exactly, so the combination (and its $\Delta H$) is valid.

**Answer:** The reconstructed equation equals the target, so $\Delta H = +66.4\ \text{kJ}$ is confirmed. **Always do this check on the exam.**

### Example 12: Which Method Should You Use?

**Problem:** For each situation, name the best method (bond enthalpy, formation table, or Hess's Law from given steps): (a) the problem gives you three combustion reactions to combine; (b) you're handed a full $\Delta H_f^\circ$ table and asked for a reaction's $\Delta H$; (c) you only have a table of average bond energies for a gas-phase reaction.

**Solution:**
- **(a)** Given a *set of reactions to combine* → **Hess's Law** (flip/scale/add). Exact.
- **(b)** Given a *formation table* → **formation formula** $\sum\Delta H_f^\circ(\text{prod}) - \sum\Delta H_f^\circ(\text{react})$. Exact and fastest.
- **(c)** Only *bond energies* → **bond enthalpy** method ($\sum$ bonds broken $- \sum$ bonds formed). Approximate, since it uses averages.

**Answer:** (a) Hess's Law; (b) formation table; (c) bond enthalpy. In principle all three agree, because enthalpy is a state function.

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Reversing a reaction but forgetting to flip the sign of $\Delta H$ | You focus on the arrow, not the number | Every time you write a reaction backward, immediately change the sign of its $\Delta H$ before moving on |
| Scaling the equation but not the $\Delta H$ (or vice versa) | The two feel like separate steps | Do them together: multiply coefficients AND $\Delta H$ by the same factor in one motion |
| Only scaling $\Delta H$ by part of the factor | Forgetting $\Delta H$ is fully extensive | If you doubled the whole equation, double *all* of $\Delta H$ — every coefficient scaled means the enthalpy scales too |
| Species that should be intermediates don't cancel | Wrong flip or wrong scale somewhere | If an intermediate survives, a given equation is on the wrong side or has the wrong coefficient — re-check step by step |
| Not verifying the summed equation equals the target | Rushing to add the numbers | Always reconstruct: add all left sides, all right sides, cancel, and confirm it's the target *before* trusting your $\Delta H$ |
| Thinking $\Delta H$ depends on the route | Forgetting the state-function idea | Enthalpy is a **state function**; $\Delta H$ is **path-independent** — any valid route gives the same answer |
| Mixing up which side gets the minus in the formation formula | "Products minus reactants" is easy to flip | Products get $+$ (you *build* them = forward formation); reactants get $-$ (you *disassemble* them = reversed formation) |
| Losing a fraction when halving an equation | $\ce{1/2 O2}$ looks wrong so students "fix" it | Fractional coefficients are perfectly legal in thermochemistry — keep the $\tfrac{1}{2}$ |

---

## AP Exam Tips

- **The two rules are the whole game.** Reverse a reaction → **flip the sign** of $\Delta H$. Scale a reaction by a factor → **multiply $\Delta H$** by that same factor. Nearly every Hess's Law question is just repeated application of these two moves plus adding.
- **Align so intermediates cancel.** Set each given equation so the target species land on the correct sides; everything *not* in the target must appear on opposite sides across your equations so it cancels. If something doesn't cancel, you flipped or scaled wrong.
- **Memorize the justification wording.** When asked *why* Hess's Law works, write: *"Enthalpy is a state function, so $\Delta H$ is path-independent — it depends only on the initial and final states, not the reaction pathway."* That exact phrasing earns the point.
- **FRQs hand you 2–3 equations to combine.** Expect a short list of reactions with $\Delta H$ values and one target. Work from the target: place the "rare" species first (the one appearing in only one given), then let the rest follow.
- **Always double-check by reconstructing the target.** After flipping/scaling, add all the left sides and all the right sides, cancel, and confirm the leftover equation is *exactly* the target. This single check catches almost every error and is fast.
- **Show every manipulated equation and its $\Delta H$.** AP graders give method points. Write each reversed/scaled reaction with its adjusted $\Delta H$, then the sum — don't just write a final number.
- **The formation formula is Hess's Law.** If a problem gives a $\Delta H_f^\circ$ table, use $\sum \Delta H_f^\circ(\text{products}) - \sum \Delta H_f^\circ(\text{reactants})$ — and remember elements in their standard state have $\Delta H_f^\circ = 0$.
- **Units and sign of the final answer.** Report kJ (or kJ/mol for a formation), and let the sign tell the story: negative = exothermic, positive = endothermic.

---

## Practice Problems

### Problem 1
State Hess's Law in one sentence, and explain the property of enthalpy that makes it true.

<details>
<summary><strong>Solution</strong></summary>

Hess's Law: if a reaction is the sum of two or more steps, its enthalpy change equals the sum of the steps' enthalpy changes. It's true because **enthalpy is a state function** — $\Delta H$ depends only on the initial and final states, not on the path (pathway) taken between them.

**Answer:** $\Delta H_\text{rxn} = \sum \Delta H_\text{steps}$; true because enthalpy is a state function (path-independent).

</details>

---

### Problem 2
Given $\ce{C(s) + O2(g) -> CO2(g)}$, $\Delta H = -393.5\ \text{kJ}$, find $\Delta H$ for $\ce{CO2(g) -> C(s) + O2(g)}$.

<details>
<summary><strong>Solution</strong></summary>

The target is the given reaction reversed. Reversing flips the sign: $\Delta H = +393.5\ \text{kJ}$.

**Answer:** $+393.5\ \text{kJ}$.

</details>

---

### Problem 3
Given $\ce{2H2(g) + O2(g) -> 2H2O(l)}$, $\Delta H = -571.6\ \text{kJ}$, find $\Delta H$ for $\ce{H2(g) + 1/2 O2(g) -> H2O(l)}$.

<details>
<summary><strong>Solution</strong></summary>

The target is the given reaction scaled by $\tfrac{1}{2}$, so scale $\Delta H$ by $\tfrac{1}{2}$: $-571.6 \times \tfrac{1}{2} = -285.8\ \text{kJ}$.

**Answer:** $-285.8\ \text{kJ}$.

</details>

---

### Problem 4
Given $\ce{N2(g) + 3H2(g) -> 2NH3(g)}$, $\Delta H = -92.2\ \text{kJ}$, find $\Delta H$ for $\ce{4NH3(g) -> 2N2(g) + 6H2(g)}$.

<details>
<summary><strong>Solution</strong></summary>

The target is the given reaction **reversed** (so $\ce{NH3}$ is on the left) **and doubled** (4 mol $\ce{NH3}$ instead of 2).

- Reverse: sign flips to $+92.2$.
- Double: multiply by 2 → $+92.2 \times 2 = +184.4\ \text{kJ}$.

**Answer:** $+184.4\ \text{kJ}$.

</details>

---

### Problem 5
Combine the two reactions to find $\Delta H$ for $\ce{2S(s) + 3O2(g) -> 2SO3(g)}$:

$$\ce{S(s) + O2(g) -> SO2(g)} \quad \Delta H = -297\ \text{kJ}$$
$$\ce{2SO2(g) + O2(g) -> 2SO3(g)} \quad \Delta H = -198\ \text{kJ}$$

<details>
<summary><strong>Solution</strong></summary>

- Target needs $\ce{2S}$ and $\ce{2SO3}$. Double the first equation: $\ce{2S + 2O2 -> 2SO2}$, $\Delta H = 2(-297) = -594\ \text{kJ}$. Keep the second as-is.
- Add: $\ce{2S + 2O2 + 2SO2 + O2 -> 2SO2 + 2SO3}$. The $\ce{2SO2}$ cancels; combining $\ce{O2}$ gives $\ce{2S + 3O2 -> 2SO3}$ ✓
- Sum: $\Delta H = -594 + (-198) = -792\ \text{kJ}$.

**Answer:** $-792\ \text{kJ}$.

</details>

---

### Problem 6
Find $\Delta H$ for $\ce{NO(g) + 1/2 O2(g) -> NO2(g)}$ from:

$$\ce{N2(g) + O2(g) -> 2NO(g)} \quad \Delta H = +180.5\ \text{kJ}$$
$$\ce{N2(g) + 2O2(g) -> 2NO2(g)} \quad \Delta H = +66.4\ \text{kJ}$$

<details>
<summary><strong>Solution</strong></summary>

- Target has $\ce{NO}$ (reactant) and $\ce{NO2}$ (product), 1 mol each.
- **Reverse and halve** the first (so $\ce{NO}$ ends on the left, 1 mol): $\ce{NO -> 1/2 N2 + 1/2 O2}$, $\Delta H = -\tfrac{1}{2}(+180.5) = -90.25\ \text{kJ}$.
- **Halve** the second (1 mol $\ce{NO2}$): $\ce{1/2 N2 + O2 -> NO2}$, $\Delta H = \tfrac{1}{2}(+66.4) = +33.2\ \text{kJ}$.
- Add: $\ce{1/2 N2}$ cancels; the $\ce{O2}$ terms leave $\ce{1/2 O2}$ on the left. Result: $\ce{NO + 1/2 O2 -> NO2}$ ✓
- Sum: $\Delta H = -90.25 + 33.2 = -57.05\ \text{kJ}$.

**Answer:** $\approx -57.1\ \text{kJ}$.

</details>

---

### Problem 7
Find $\Delta H$ for $\ce{C(s) + 1/2 O2(g) -> CO(g)}$ given:

$$\ce{2C(s) + O2(g) -> 2CO(g)} \quad \Delta H = -221.0\ \text{kJ}$$

<details>
<summary><strong>Solution</strong></summary>

The target is the given reaction halved. Scale $\Delta H$ by $\tfrac{1}{2}$: $-221.0 \times \tfrac{1}{2} = -110.5\ \text{kJ}$.

**Answer:** $-110.5\ \text{kJ}$ (consistent with Example 4 — different route, same $\Delta H$, because enthalpy is a state function).

</details>

---

### Problem 8
Find $\Delta H$ for $\ce{2NO(g) + O2(g) -> 2NO2(g)}$ using these formation-style reactions:

$$\ce{1/2 N2(g) + 1/2 O2(g) -> NO(g)} \quad \Delta H = +90.3\ \text{kJ}$$
$$\ce{1/2 N2(g) + O2(g) -> NO2(g)} \quad \Delta H = +33.2\ \text{kJ}$$

<details>
<summary><strong>Solution</strong></summary>

- Target needs $\ce{2NO}$ as a *reactant* and $\ce{2NO2}$ as a *product*.
- **Reverse and double** the first: $\ce{2NO -> N2 + O2}$, $\Delta H = -2(+90.3) = -180.6\ \text{kJ}$.
- **Double** the second: $\ce{N2 + 2O2 -> 2NO2}$, $\Delta H = 2(+33.2) = +66.4\ \text{kJ}$.
- Add: $\ce{N2}$ cancels; $\ce{O2}$: left has $\ce{2O2}$ from the doubled second, right has $\ce{O2}$ from the reversed first — net $\ce{O2}$ on the left. Result: $\ce{2NO + O2 -> 2NO2}$ ✓
- Sum: $\Delta H = -180.6 + 66.4 = -114.2\ \text{kJ}$.

**Answer:** $\approx -114.2\ \text{kJ}$.

</details>

---

### Problem 9
Find $\Delta H_f^\circ$ for $\ce{CS2(l)}$: $\ce{C(s) + 2S(s) -> CS2(l)}$, from:

$$\text{(i)}\quad \ce{C(s) + O2(g) -> CO2(g)} \quad -393.5\ \text{kJ}$$
$$\text{(ii)}\quad \ce{S(s) + O2(g) -> SO2(g)} \quad -296.8\ \text{kJ}$$
$$\text{(iii)}\quad \ce{CS2(l) + 3O2(g) -> CO2(g) + 2SO2(g)} \quad -1072\ \text{kJ}$$

<details>
<summary><strong>Solution</strong></summary>

- **Keep (i)** ($\ce{C}$ reactant, 1 mol): $-393.5$.
- **Double (ii)** ($\ce{2S}$ reactant): $2(-296.8) = -593.6$.
- **Reverse (iii)** ($\ce{CS2}$ product): $+1072$.
- Cancel: $\ce{CO2}$ (from i) and $\ce{2SO2}$ (from doubled ii) cancel against reversed (iii); the $\ce{O2}$ terms cancel ($\ce{O2} + \ce{2O2} = \ce{3O2}$ on left vs. $\ce{3O2}$ on right). Left: $\ce{C + 2S -> CS2}$ ✓
- Sum: $\Delta H = -393.5 + (-593.6) + (+1072) = +84.9\ \text{kJ}$.

**Answer:** $\Delta H_f^\circ(\ce{CS2}, l) \approx +85\ \text{kJ/mol}$ (endothermic formation).

</details>

---

### Problem 10
A reaction proceeds $\ce{X -> Y -> Z}$. Step 1 ($\ce{X -> Y}$): $\Delta H = -25\ \text{kJ}$. Step 2 ($\ce{Y -> Z}$): $\Delta H = +60\ \text{kJ}$. Find $\Delta H$ for $\ce{X -> Z}$ and state whether it's exo- or endothermic.

<details>
<summary><strong>Solution</strong></summary>

Sum the steps: $\Delta H = -25 + (+60) = +35\ \text{kJ}$. Positive → **endothermic** ($\ce{Z}$ ends up above $\ce{X}$).

**Answer:** $+35\ \text{kJ}$, endothermic.

</details>

---

### Problem 11
Using $\Delta H_f^\circ$ values $\ce{NH3(g)} = -46.1$, $\ce{NO(g)} = +90.3$, $\ce{H2O(g)} = -241.8\ \text{kJ/mol}$ (and $\ce{O2} = 0$), find $\Delta H_\text{rxn}$ for $\ce{4NH3(g) + 5O2(g) -> 4NO(g) + 6H2O(g)}$.

<details>
<summary><strong>Solution</strong></summary>

$$\Delta H = \big[4(+90.3) + 6(-241.8)\big] - \big[4(-46.1) + 5(0)\big]$$
$$= \big[361.2 - 1450.8\big] - \big[-184.4\big] = -1089.6 + 184.4 = -905.2\ \text{kJ}$$

**Answer:** $\Delta H_\text{rxn} = -905.2\ \text{kJ}$ (this is the Ostwald process — strongly exothermic).

</details>

---

### Problem 12
Explain, using Hess's Law reasoning, *why* the formula $\Delta H_\text{rxn} = \sum \Delta H_f^\circ(\text{products}) - \sum \Delta H_f^\circ(\text{reactants})$ has a **minus sign** in front of the reactants.

<details>
<summary><strong>Solution</strong></summary>

The formula secretly routes the reaction **reactants → elements → products**. To go from reactants to bare elements you must *undo* each reactant's formation reaction — i.e., run its formation **backward**. Reversing a reaction flips the sign of $\Delta H$, so each reactant's $\Delta H_f^\circ$ enters as a **negative**. Building the products from those elements uses forward formations (positive contributions). The elements cancel as intermediates, leaving $\sum \Delta H_f^\circ(\text{prod}) - \sum \Delta H_f^\circ(\text{react})$.

**Answer:** The minus comes from *reversing* the reactants' formation reactions (disassembling them into elements), which flips the sign of their $\Delta H_f^\circ$.

</details>

---

### Problem 13
Find $\Delta H$ for $\ce{H2(g) + Cl2(g) -> 2HCl(g)}$ from:

$$\ce{H2(g) + F2(g) -> 2HF(g)} \quad \Delta H = -537\ \text{kJ}$$
$$\ce{2HCl(g) + F2(g) -> 2HF(g) + Cl2(g)} \quad \Delta H = -352\ \text{kJ}$$

<details>
<summary><strong>Solution</strong></summary>

- Target: $\ce{H2}$, $\ce{Cl2}$ reactants; $\ce{2HCl}$ product.
- **Keep the first** ($\ce{H2}$ on left): $-537$.
- **Reverse the second** (to put $\ce{2HCl}$ on the right and $\ce{Cl2}$ on the left): $\ce{2HF + Cl2 -> 2HCl + F2}$, $\Delta H = +352$.
- Add: $\ce{2HF}$ cancels (product of first, reactant of reversed second); $\ce{F2}$ cancels (reactant of first, product of reversed second). Left: $\ce{H2 + Cl2 -> 2HCl}$ ✓
- Sum: $\Delta H = -537 + (+352) = -185\ \text{kJ}$.

**Answer:** $-185\ \text{kJ}$.

</details>

---

### Problem 14
You need $\Delta H$ for a reaction, and the problem provides only a table of **average bond energies**. Your friend used a **formation table** and got a slightly different number. Who is more accurate, and why must the two answers be *close*?

<details>
<summary><strong>Solution</strong></summary>

The **formation table** answer is more accurate, because tabulated $\Delta H_f^\circ$ values are exact for the specific compounds. Bond-energy calculations use **average** bond strengths (a $\ce{C-H}$ bond is not identical in every molecule), so they give an **estimate**. The two must be *close* because enthalpy is a **state function** — every valid method computes the same $\Delta H$ in principle; bond enthalpy just introduces averaging error.

**Answer:** The formation-table result is more accurate (exact vs. averaged); both are close because $\Delta H$ is path-independent.

</details>

---

### Problem 15
A student combines equations for a target and reports $\Delta H$, but when they reconstruct the summed equation they get $\ce{2A + B -> C + D}$ while the target is $\ce{2A + B -> C}$. What went wrong, and what should they do?

<details>
<summary><strong>Solution</strong></summary>

An extra species $\ce{D}$ survived on the product side, which means $\ce{D}$ was supposed to be an **intermediate** that cancels — but it didn't. One of the given equations was placed on the wrong side (should have been reversed) or has the wrong coefficient (needs scaling) so that $\ce{D}$ appears on opposite sides in equal amounts. The student should re-examine each equation containing $\ce{D}$, flip or scale it so $\ce{D}$ cancels, then re-sum both the equations and the $\Delta H$ values.

**Answer:** An intermediate failed to cancel — a given equation needs reversing or rescaling so $\ce{D}$ appears on opposite sides; fix that and recompute.

</details>

---

## Quick Reference

| Concept | Key idea / formula |
|---|---|
| **Hess's Law** | $\Delta H_\text{rxn} = \sum \Delta H_\text{steps}$ |
| **Why it works** | Enthalpy is a **state function** → $\Delta H$ is **path-independent** |
| **Big Bear analogy** | Net elevation gain is the same on any road; net $\Delta H$ is the same on any pathway |
| **Reverse a reaction** | **Flip the sign** of $\Delta H$ |
| **Scale a reaction** | **Multiply** $\Delta H$ by the same factor (extensive) |
| **Combine** | Flip/scale each given so reactants & products land right → **add** → intermediates **cancel** |
| **Intermediates** | Species that are a product in one step and reactant in another cancel (the "ridge you re-descend") |
| **Formation formula** | $\Delta H_\text{rxn}^\circ = \sum \Delta H_f^\circ(\text{prod}) - \sum \Delta H_f^\circ(\text{react})$ — this **IS** Hess's Law (route through elements) |
| **Standard-state elements** | $\Delta H_f^\circ = 0$ |
| **Verify** | Reconstruct: add all left sides, all right sides, cancel — must equal the target |
| **Three methods** | Bond enthalpy (estimate) · formation (exact table) · Hess (exact, from steps) — all agree in principle |
| **AP justification phrase** | "Enthalpy is a state function, so $\Delta H$ is path-independent." |

---

<div align="center">

[← Enthalpy of Formation](/chemistry/0805-enthalpy-of-formation) | [Introduction to Equilibrium →](/chemistry/0901-introduction-to-equilibrium)

</div>
