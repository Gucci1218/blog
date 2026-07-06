# Enthalpy of Formation
<p class="article-date">July 5, 2026</p>

*Last weekend we drove up to the IKEA in Mission Valley for a bookshelf, and I ended up thinking about chemistry the entire way home — which, okay, is a new personality trait I've developed. Here's what got me: everything in that giant warehouse is built from the same small pile of standard flat-pack parts. A \$40 BILLY bookcase is just particleboard panels, dowels, cam locks, and an Allen key. A desk is the same kind of parts, assembled a different way. Nobody sells you a "pre-built" bookcase — the baseline, the thing you start from, is always the flat pile of boxes on the cart. And assembling any piece of furniture from that flat pile releases (or costs) a very specific amount of effort you could write on a tag. That tag is exactly what a chemist calls the **enthalpy of formation**: the energy to assemble one mole of a compound out of its raw element-parts. Once every compound has a formation tag, any reaction becomes bookkeeping — disassemble the reactants back to parts, reassemble the parts into products, add up the tags. This is Topic 6.8, and it's the single most reusable trick in the whole thermochemistry unit, so let's build it.*

---

## What You'll Learn

- Define the **standard enthalpy of formation** $\Delta H_f^\circ$ as the energy to make **one mole** of a compound from its elements in their **standard states**, and state the standard conditions (1 atm, usually 25 °C, 1 M for solutions) and units (kJ/mol)
- Explain the **zero reference**: why $\Delta H_f^\circ = 0$ for an element in its standard state — and *only* its standard state
- Identify the correct **standard state** of an element ($\ce{O2}$ not $\ce{O}$ or $\ce{O3}$; carbon as **graphite**; $\ce{Br2}$ liquid; $\ce{Na}$ solid; $\ce{H2}$ gas) — the classic AP trap
- Write a **correct formation reaction** for any compound, using fractional coefficients so the product stays at exactly 1 mole
- Apply the master equation $\Delta H_{rxn}^\circ = \sum n\Delta H_f^\circ(\text{products}) - \sum n\Delta H_f^\circ(\text{reactants})$ to compute reaction enthalpies from a table
- Remember to **weight each $\Delta H_f^\circ$ by its coefficient** and to **skip elements** (their $\Delta H_f^\circ$ is zero)
- Solve the **reverse problem**: given $\Delta H_{rxn}^\circ$ and all-but-one formation enthalpy, find the missing $\Delta H_f^\circ$ (a guaranteed FRQ)
- Contrast this **exact, tabulated** method with the **approximate** bond-enthalpy route, and see why formation enthalpies are a Hess's-law shortcut

---

## Prerequisites

- [Enthalpy of Reaction](/chemistry/0803-enthalpy-of-reaction) — you must already know that $\Delta H$ is the heat of a reaction at constant pressure, that it's negative for exothermic and positive for endothermic, and that it scales with amount. This article is a *machine for computing that same $\Delta H$*, so it's non-negotiable.
- [Bond Enthalpies](/chemistry/0804-bond-enthalpies) — that article gave you one route to $\Delta H_{rxn}$ (break all bonds, make all bonds) that is only **approximate**, because a bond energy is an *average* over many molecules. Formation enthalpies are the **exact** route using tabulated real-compound values. Keep both in your pocket and know which is which.

---

## The Core Concept

### Intuition First

Let's stay in the IKEA warehouse, because it secretly contains every idea in this article.

Walk the aisles and notice something: every finished product is assembled from the **same standard parts**. Panels, dowels, screws, cam locks. Chemistry is identical — every compound in the universe is assembled from the **same standard parts**, which are the *elements*. Water is built from hydrogen and oxygen. Table salt is built from sodium and chlorine. Glucose is built from carbon, hydrogen, and oxygen. The elements are the flat-pack parts; the compounds are the furniture.

Now the crucial move. When you want to price a bookcase, you need a **baseline** — a zero to measure from. IKEA's baseline is the flat pile of unopened boxes sitting on your cart. That pile isn't "worth nothing," but it's the agreed-upon *starting point*, and the price tag measures the effort to go **from that pile to the finished shelf**. Chemists made the exact same choice: they declared that **an element in its standard state has an enthalpy of formation of exactly zero**. It's the reference floor. Not because elements have no energy, but because you have to measure *from* somewhere, and the raw parts are the natural place to start.

So here's the definition, in furniture terms:

> The **enthalpy of formation** of a compound, $\Delta H_f^\circ$, is the energy tag for **assembling one mole of that compound from its element-parts**, where every element-part starts at the zero baseline.

$\ce{H2O(l)}$ has $\Delta H_f^\circ = -285.8$ kJ/mol — assembling a mole of liquid water from hydrogen and oxygen parts *releases* 285.8 kJ, so water sits far *below* the baseline (very stable, hard to take apart — a well-built shelf). A few compounds have **positive** tags, like $\ce{NO}$ at $+90.3$ kJ/mol — assembling it *costs* energy, so it perches *above* the baseline (a wobbly, high-strung piece that's eager to fall apart).

Here's the payoff, and it's beautiful. Suppose you want the energy of some reaction — reactant-furniture turning into product-furniture. You could try to track it directly, but there's a slicker way. **Disassemble every reactant all the way back down to the flat pile of element-parts** (that's the *reverse* of forming them, so you flip the sign of their tags), then **reassemble those parts into the products** (their tags, forward). Everything routes through the same shared pile of parts in the middle, so the parts cancel and you're left with a clean formula:

$$\Delta H_{rxn}^\circ = \underbrace{\sum n\,\Delta H_f^\circ(\text{products})}_{\text{assemble the products}} - \underbrace{\sum n\,\Delta H_f^\circ(\text{reactants})}_{\text{disassemble the reactants}}$$

That's it. "Products minus reactants," each weighted by its coefficient. The whole article is learning to read energy tags off a table and plug them into that one line.

Here's the map, one-to-one:

| IKEA warehouse | Chemistry |
|---|---|
| flat-pack parts (panels, dowels, screws) | **elements in their standard states** |
| the flat pile of boxes = the baseline | $\Delta H_f^\circ(\text{element}) = 0$ |
| a finished piece of furniture | a **compound** |
| the assembly-effort tag on that furniture | its $\Delta H_f^\circ$ |
| building furniture from the parts pile | a **formation reaction** |
| disassemble old furniture, build new furniture | a **chemical reaction** |
| (effort to build new) − (effort you get back tearing down old) | $\Delta H_{rxn}^\circ = \sum \Delta H_f^\circ(\text{prod}) - \sum \Delta H_f^\circ(\text{react})$ |

### The Zero Baseline (and the AP Trap Hiding In It)

The rule "elements are zero" sounds easy, but it comes with a landmine: **it's only true for the element's *standard state*** — the one specific form the element naturally takes at 1 atm and 25 °C. IKEA sells a panel in *one* standard shape; a panel you've sawed in half is no longer a standard part. Same with elements.

| Element | Standard state (the zero) | *Not* zero |
|---|---|---|
| Oxygen | $\ce{O2(g)}$ | $\ce{O(g)}$ (atoms), $\ce{O3(g)}$ (ozone) |
| Hydrogen | $\ce{H2(g)}$ | $\ce{H(g)}$ |
| Nitrogen | $\ce{N2(g)}$ | $\ce{N(g)}$ |
| Carbon | $\ce{C(graphite)}$ | $\ce{C(diamond)}$ ($+1.9$ kJ/mol!) |
| Bromine | $\ce{Br2(l)}$ | $\ce{Br2(g)}$, $\ce{Br(g)}$ |
| Mercury | $\ce{Hg(l)}$ | $\ce{Hg(g)}$ |
| Sodium | $\ce{Na(s)}$ | $\ce{Na(g)}$ |
| Chlorine | $\ce{Cl2(g)}$ | $\ce{Cl(g)}$ |

Two things trip up everyone:

1. **The diatomic seven.** Seven elements exist as diatomic molecules in their standard state: $\ce{H2}$, $\ce{N2}$, $\ce{O2}$, $\ce{F2}$, $\ce{Cl2}$, $\ce{Br2}$, $\ce{I2}$. Their zero form is the *pair*, not the lone atom. So $\ce{O2(g)}$ is zero but $\ce{O(g)}$ is very much not.
2. **Allotropes and phases.** Carbon's standard state is **graphite**, so diamond has a nonzero $\Delta H_f^\circ$. Bromine's standard state is the **liquid**, so $\ce{Br2(g)}$ is nonzero. The AP exam loves handing you $\ce{C(diamond)}$ or $\ce{Br2(g)}$ and watching you write "0."

### Writing a Formation Reaction

A **formation reaction** builds exactly **one mole** of a single compound straight from its elements in their standard states. Two rules:

1. **Reactants are elements in standard-state form** (the diatomics as diatomics, carbon as graphite, etc.).
2. **The product is exactly 1 mole** of the target compound. To make the atoms balance with only 1 mole of product, you're allowed — even *required* — to use **fractional coefficients** on the elements. That's fine here, because $\Delta H_f^\circ$ is defined *per mole of product*.

Example: the formation reaction of $\ce{CO2(g)}$ is $\ce{C(graphite) + O2(g) -> CO2(g)}$. For $\ce{H2O(l)}$ it's $\ce{H2(g) + 1/2 O2(g) -> H2O(l)}$ — the $\tfrac12$ is what keeps water at one mole.

### The Reference Table (used throughout)

Standard enthalpies of formation, $\Delta H_f^\circ$ in kJ/mol at 25 °C. Elements in their standard state are $0$ by definition and aren't listed. On the real AP exam a table like this is **provided** — you don't memorize the numbers, you memorize the *method*.

| Compound | $\Delta H_f^\circ$ (kJ/mol) | Compound | $\Delta H_f^\circ$ (kJ/mol) |
|---|---|---|---|
| $\ce{CO2(g)}$ | $-393.5$ | $\ce{NH3(g)}$ | $-45.9$ |
| $\ce{CO(g)}$ | $-110.5$ | $\ce{NO(g)}$ | $+90.3$ |
| $\ce{H2O(l)}$ | $-285.8$ | $\ce{NO2(g)}$ | $+33.2$ |
| $\ce{H2O(g)}$ | $-241.8$ | $\ce{CaCO3(s)}$ | $-1207.0$ |
| $\ce{H2O2(l)}$ | $-187.8$ | $\ce{CaO(s)}$ | $-635.1$ |
| $\ce{CH4(g)}$ | $-74.8$ | $\ce{SO2(g)}$ | $-296.8$ |
| $\ce{C3H8(g)}$ | $-103.8$ | $\ce{SO3(g)}$ | $-395.7$ |
| $\ce{C2H2(g)}$ | $+227.4$ | $\ce{Fe2O3(s)}$ | $-824.2$ |
| $\ce{CH3OH(l)}$ | $-238.6$ | $\ce{Al2O3(s)}$ | $-1675.7$ |
| $\ce{C2H5OH(l)}$ | $-277.6$ | $\ce{HCl(g)}$ | $-92.3$ |
| $\ce{C6H12O6(s)}$ | $-1273.3$ | $\ce{NaCl(s)}$ | $-411.2$ |

### Exact vs. Approximate: Why Two Methods?

In [Bond Enthalpies](/chemistry/0804-bond-enthalpies) you found $\Delta H_{rxn}$ by breaking every bond and making every bond. That method uses **average** bond energies — a single $\ce{C-H}$ number stands in for $\ce{C-H}$ bonds in thousands of different molecules — so its answers are ballpark, off by tens of kJ. It's the "eyeball the assembly effort" approach: fast, no table needed, roughly right.

Formation enthalpies are the opposite. Each $\Delta H_f^\circ$ is a **measured value for that exact compound**, so "products minus reactants" gives an **exact** answer (to the table's precision). It's the "read the real price tag off the box" approach. Both routes chase the same $\Delta H_{rxn}$; formation enthalpies win on accuracy, bond enthalpies win when you have no table. And structurally, the formation method is just **Hess's law** in disguise — every reaction routed through the shared pile of elements — which is exactly the idea the next article, [Hess's Law](/chemistry/0806-hess-law), makes fully general.

---

## Worked Examples

I'll use the reference table above and keep an extra digit through the middle, rounding at the end.

### Example 1: Which Substances Have $\Delta H_f^\circ = 0$?

**Problem:** For each, state whether $\Delta H_f^\circ = 0$: (a) $\ce{O2(g)}$, (b) $\ce{O3(g)}$, (c) $\ce{O(g)}$, (d) $\ce{C(graphite)}$, (e) $\ce{C(diamond)}$, (f) $\ce{Br2(l)}$, (g) $\ce{Br2(g)}$, (h) $\ce{Na(s)}$, (i) $\ce{H2(g)}$, (j) $\ce{Fe(s)}$.

**Solution:** Zero only if it's an **element in its standard state**.

- (a) $\ce{O2(g)}$ — **yes, 0.** Standard state of oxygen.
- (b) $\ce{O3(g)}$ — **no.** Ozone is an allotrope, not the standard state.
- (c) $\ce{O(g)}$ — **no.** Lone atoms, not the diatomic standard state.
- (d) $\ce{C(graphite)}$ — **yes, 0.** Carbon's standard state.
- (e) $\ce{C(diamond)}$ — **no.** Diamond is the non-standard allotrope.
- (f) $\ce{Br2(l)}$ — **yes, 0.** Bromine is a liquid at standard conditions.
- (g) $\ce{Br2(g)}$ — **no.** Wrong phase; the vapor isn't the standard state.
- (h) $\ce{Na(s)}$ — **yes, 0.** Solid metal.
- (i) $\ce{H2(g)}$ — **yes, 0.** Diatomic standard state.
- (j) $\ce{Fe(s)}$ — **yes, 0.** Solid metal.

**Answer:** Zero for **a, d, f, h, i, j**; nonzero for **b, c, e, g**.

### Example 2: Formation Reaction of $\ce{CO2(g)}$

**Problem:** Write the formation reaction for carbon dioxide.

**Solution:** Element-parts: carbon (as **graphite**) and oxygen (as $\ce{O2}$). Product is 1 mol $\ce{CO2}$. Balancing needs one C and two O, which one $\ce{O2}$ already supplies:

$$\ce{C(graphite) + O2(g) -> CO2(g)}$$

No fractions needed here. Note $\Delta H$ for *this* reaction **equals** $\Delta H_f^\circ(\ce{CO2}) = -393.5$ kJ/mol, by definition.

**Answer:** $\ce{C(graphite) + O2(g) -> CO2(g)}$.

### Example 3: Formation Reaction of $\ce{H2O(l)}$ (fraction required)

**Problem:** Write the formation reaction for liquid water.

**Solution:** Parts are $\ce{H2(g)}$ and $\ce{O2(g)}$. One mole of $\ce{H2O}$ has one O, but the standard part is $\ce{O2}$ — so we need **half** an $\ce{O2}$ to supply one O while keeping the product at 1 mol:

$$\ce{H2(g) + 1/2 O2(g) -> H2O(l)}$$

The $\tfrac12$ is not optional. If you wrote $\ce{2H2 + O2 -> 2H2O}$ you'd have a perfectly balanced equation, but it makes **2** mol of water, so its $\Delta H$ would be $2\Delta H_f^\circ$, not $\Delta H_f^\circ$.

**Answer:** $\ce{H2(g) + 1/2 O2(g) -> H2O(l)}$.

### Example 4: Formation Reaction of $\ce{NH3(g)}$

**Problem:** Write the formation reaction for ammonia.

**Solution:** Parts $\ce{N2(g)}$ and $\ce{H2(g)}$; product 1 mol $\ce{NH3}$ (one N, three H). Half an $\ce{N2}$ gives one N; three-halves $\ce{H2}$ gives three H:

$$\ce{1/2 N2(g) + 3/2 H2(g) -> NH3(g)}$$

**Answer:** $\ce{1/2 N2(g) + 3/2 H2(g) -> NH3(g)}$.

### Example 5: Formation Reaction of $\ce{C6H12O6(s)}$

**Problem:** Write the formation reaction for glucose.

**Solution:** Parts: $\ce{C(graphite)}$, $\ce{H2(g)}$, $\ce{O2(g)}$. Product 1 mol glucose has 6 C, 12 H, 6 O. That needs 6 graphite, 6 $\ce{H2}$ (= 12 H), and 3 $\ce{O2}$ (= 6 O):

$$\ce{6C(graphite) + 6H2(g) + 3O2(g) -> C6H12O6(s)}$$

These happen to all be whole numbers because glucose has even counts of each element.

**Answer:** $\ce{6C(graphite) + 6H2(g) + 3O2(g) -> C6H12O6(s)}$.

### Example 6: Formation Reaction of $\ce{CaCO3(s)}$

**Problem:** Write the formation reaction for calcium carbonate.

**Solution:** Parts: $\ce{Ca(s)}$, $\ce{C(graphite)}$, $\ce{O2(g)}$. Product 1 mol $\ce{CaCO3}$ has 1 Ca, 1 C, 3 O. One Ca, one graphite, and $\tfrac32\,\ce{O2}$ (= 3 O):

$$\ce{Ca(s) + C(graphite) + 3/2 O2(g) -> CaCO3(s)}$$

**Answer:** $\ce{Ca(s) + C(graphite) + 3/2 O2(g) -> CaCO3(s)}$.

### Example 7: $\Delta H_{rxn}$ for the Combustion of Methane

**Problem:** Find $\Delta H_{rxn}^\circ$ for $\ce{CH4(g) + 2O2(g) -> CO2(g) + 2H2O(l)}$.

**Solution:** Products minus reactants, each tag times its coefficient. **$\ce{O2}$ is an element — its tag is 0, so it drops out.**

$$\sum \text{products} = \underbrace{(1)(-393.5)}_{\ce{CO2}} + \underbrace{(2)(-285.8)}_{\ce{H2O}} = -393.5 - 571.6 = -965.1$$

$$\sum \text{reactants} = \underbrace{(1)(-74.8)}_{\ce{CH4}} + \underbrace{(2)(0)}_{\ce{O2}} = -74.8$$

$$\Delta H_{rxn}^\circ = -965.1 - (-74.8) = -890.3\ \text{kJ}$$

**Answer:** $-890.3$ kJ (exothermic — natural gas burning, as expected).

### Example 8: Combustion of Propane (watch the coefficients)

**Problem:** Find $\Delta H_{rxn}^\circ$ for $\ce{C3H8(g) + 5O2(g) -> 3CO2(g) + 4H2O(l)}$.

**Solution:** Every coefficient multiplies its tag — miss one and the whole answer is off.

$$\sum \text{products} = (3)(-393.5) + (4)(-285.8) = -1180.5 - 1143.2 = -2323.7$$

$$\sum \text{reactants} = (1)(-103.8) + (5)(0) = -103.8$$

$$\Delta H_{rxn}^\circ = -2323.7 - (-103.8) = -2219.9\ \text{kJ}$$

**Answer:** $-2219.9$ kJ. Propane packs a lot more energy per mole than methane — that's why the backyard grill runs on it.

### Example 9: Decomposition of Limestone (an endothermic case)

**Problem:** Find $\Delta H_{rxn}^\circ$ for $\ce{CaCO3(s) -> CaO(s) + CO2(g)}$ — the reaction that turns limestone into quicklime.

**Solution:**

$$\sum \text{products} = (1)(-635.1) + (1)(-393.5) = -1028.6$$

$$\sum \text{reactants} = (1)(-1207.0) = -1207.0$$

$$\Delta H_{rxn}^\circ = -1028.6 - (-1207.0) = +178.4\ \text{kJ}$$

**Answer:** $+178.4$ kJ. **Positive** — endothermic. You have to pump heat *in* to break limestone apart, which is why cement kilns are furnaces.

### Example 10: Thermite (elements on both sides)

**Problem:** Find $\Delta H_{rxn}^\circ$ for $\ce{2Al(s) + Fe2O3(s) -> Al2O3(s) + 2Fe(s)}$.

**Solution:** Here **two** species are elements in their standard state — $\ce{Al(s)}$ (reactant) and $\ce{Fe(s)}$ (product) — so both are 0 and vanish. Only the two oxides matter.

$$\sum \text{products} = \underbrace{(1)(-1675.7)}_{\ce{Al2O3}} + \underbrace{(2)(0)}_{\ce{Fe}} = -1675.7$$

$$\sum \text{reactants} = \underbrace{(2)(0)}_{\ce{Al}} + \underbrace{(1)(-824.2)}_{\ce{Fe2O3}} = -824.2$$

$$\Delta H_{rxn}^\circ = -1675.7 - (-824.2) = -851.5\ \text{kJ}$$

**Answer:** $-851.5$ kJ. Wildly exothermic — thermite melts steel because aluminum grabs oxygen far more fiercely than iron holds it.

### Example 11: Burning Sugar (respiration in one line)

**Problem:** Find $\Delta H_{rxn}^\circ$ for $\ce{C6H12O6(s) + 6O2(g) -> 6CO2(g) + 6H2O(l)}$.

**Solution:**

$$\sum \text{products} = (6)(-393.5) + (6)(-285.8) = -2361.0 - 1714.8 = -4075.8$$

$$\sum \text{reactants} = (1)(-1273.3) + (6)(0) = -1273.3$$

$$\Delta H_{rxn}^\circ = -4075.8 - (-1273.3) = -2802.5\ \text{kJ}$$

**Answer:** $-2802.5$ kJ per mole of glucose. This is literally the energy your cells extract from sugar — the same number whether you burn it in a flame or metabolize it slowly, because $\Delta H$ is a state function.

### Example 12: The Reverse Problem — Solve for an Unknown $\Delta H_f^\circ$

**Problem:** The combustion of ethanol, $\ce{C2H5OH(l) + 3O2(g) -> 2CO2(g) + 3H2O(l)}$, releases $\Delta H_{rxn}^\circ = -1366.8$ kJ. Using the table, find $\Delta H_f^\circ$ of ethanol. (Pretend it's the one value you *don't* have.)

**Solution:** Write the master equation with the unknown as a symbol, then solve algebraically. Let $x = \Delta H_f^\circ(\ce{C2H5OH})$.

$$\Delta H_{rxn}^\circ = \big[\,(2)(-393.5) + (3)(-285.8)\,\big] - \big[\,(1)(x) + (3)(0)\,\big]$$

$$-1366.8 = \big[\,-787.0 - 857.4\,\big] - x = -1644.4 - x$$

Solve:

$$x = -1644.4 - (-1366.8) = -1644.4 + 1366.8 = -277.6\ \text{kJ/mol}$$

**Answer:** $\Delta H_f^\circ(\ce{C2H5OH}) = -277.6$ kJ/mol — matching the table. The move that matters: set up "products − reactants" as usual, put the unknown in its slot, and do the algebra. This is a guaranteed FRQ shape.

---

## Common Mistakes

| The mistake | Why it happens | How to avoid it |
|---|---|---|
| Writing $\Delta H_f^\circ = 0$ for $\ce{C(diamond)}$, $\ce{O3}$, $\ce{Br2(g)}$, $\ce{O(g)}$ | "It's an element, so it's zero" | Zero **only** in the *standard state*: graphite, $\ce{O2}$, $\ce{Br2(l)}$, the diatomic pair |
| Doing **reactants − products** | Reflex from other formulas | It's **products − reactants**, always. A sign flip = wrong answer |
| Forgetting to multiply by coefficients | You read the tag but skip the count | Every $\Delta H_f^\circ$ gets times its balancing coefficient before you sum |
| Including elements as nonzero | You look for every species in the table | Elements in standard state are 0 — cross them out ($\ce{O2}$, $\ce{N2}$, metals) |
| Formation reaction that makes 2+ mol of product | You cleared fractions to look "neat" | The product must be **exactly 1 mol**; fractional coefficients on the *elements* are correct |
| Using $\Delta H_f^\circ$ for the wrong **phase** | $\ce{H2O(l)}$ vs $\ce{H2O(g)}$ have different tags | Match the state symbol in the equation to the state in the table |
| Confusing this with bond enthalpies | Both give $\Delta H_{rxn}$ | Bond enthalpies = approximate averages; formation = exact tabulated values |
| Sign slip in the reverse problem | Minus-a-negative algebra | Write it symbolically, then move terms carefully: $x = \sum\text{prod} - \Delta H_{rxn}$ |

---

## AP Exam Tips

- **Elements in their standard state are zero — and know your standard states cold.** The diatomic seven ($\ce{H2, N2, O2, F2, Cl2, Br2, I2}$), carbon as **graphite**, $\ce{Br2}$ and $\ce{Hg}$ as **liquids**, metals as solids. The exam plants a $\ce{C(diamond)}$ or an $\ce{O3}$ specifically to catch "it's an element, so 0."
- **The formula is products minus reactants — never reversed.** $\Delta H_{rxn}^\circ = \sum n\Delta H_f^\circ(\text{products}) - \sum n\Delta H_f^\circ(\text{reactants})$. Write it at the top of your work every time so you can't flip it under pressure.
- **Multiply each $\Delta H_f^\circ$ by its coefficient.** This is the most common silent error. In $\ce{2CO2}$, the tag is $2 \times (-393.5)$, not $-393.5$.
- **The solve-for-unknown-$\Delta H_f^\circ$ FRQ is a lock.** They give you $\Delta H_{rxn}$ and every formation value but one. Set up the master equation, put the unknown in its slot, solve algebraically. Practice the "$x = \sum\text{prod} - \Delta H_{rxn}$" rearrangement until it's automatic.
- **A formation reaction makes exactly 1 mole of product**, elements in standard states on the left, **fractions allowed**. If your product coefficient isn't 1, it isn't a formation reaction.
- **Show the substitution for work-shown credit.** Write out the full "$[\text{sum of products}] - [\text{sum of reactants}]$" with numbers plugged in. Graders award points for the correct setup even if the arithmetic slips.
- **You get the table.** Don't waste memory on values — memorize the *method* and the *standard states*.

---

## Practice Problems

Use the reference table. Carry an extra digit and round at the end.

### Problem 1
Which of these have $\Delta H_f^\circ = 0$? $\ce{N2(g)}$, $\ce{O3(g)}$, $\ce{Hg(l)}$, $\ce{C(diamond)}$, $\ce{Fe(s)}$, $\ce{Cl(g)}$.

<details>
<summary><strong>Solution</strong></summary>

Zero only for elements in their **standard state**:

- $\ce{N2(g)}$ — **0** (diatomic standard state).
- $\ce{O3(g)}$ — not 0 (ozone, an allotrope).
- $\ce{Hg(l)}$ — **0** (mercury is a liquid at standard conditions).
- $\ce{C(diamond)}$ — not 0 (standard state is graphite).
- $\ce{Fe(s)}$ — **0** (solid metal).
- $\ce{Cl(g)}$ — not 0 (standard state is $\ce{Cl2}$, not lone atoms).

**Answer:** $\ce{N2(g)}$, $\ce{Hg(l)}$, and $\ce{Fe(s)}$.

</details>

---

### Problem 2
Write the formation reaction for $\ce{HCl(g)}$.

<details>
<summary><strong>Solution</strong></summary>

Parts $\ce{H2(g)}$ and $\ce{Cl2(g)}$; product 1 mol $\ce{HCl}$ (one H, one Cl). Half of each diatomic:

$$\ce{1/2 H2(g) + 1/2 Cl2(g) -> HCl(g)}$$

**Answer:** $\ce{1/2 H2(g) + 1/2 Cl2(g) -> HCl(g)}$.

</details>

---

### Problem 3
Write the formation reaction for $\ce{NaCl(s)}$.

<details>
<summary><strong>Solution</strong></summary>

Parts $\ce{Na(s)}$ (solid metal) and $\ce{Cl2(g)}$. One mole $\ce{NaCl}$ needs one Na and one Cl:

$$\ce{Na(s) + 1/2 Cl2(g) -> NaCl(s)}$$

**Answer:** $\ce{Na(s) + 1/2 Cl2(g) -> NaCl(s)}$.

</details>

---

### Problem 4
Write the formation reaction for $\ce{Fe2O3(s)}$.

<details>
<summary><strong>Solution</strong></summary>

Parts $\ce{Fe(s)}$ and $\ce{O2(g)}$; product 1 mol $\ce{Fe2O3}$ (2 Fe, 3 O). Two Fe and $\tfrac32\,\ce{O2}$ (= 3 O):

$$\ce{2Fe(s) + 3/2 O2(g) -> Fe2O3(s)}$$

**Answer:** $\ce{2Fe(s) + 3/2 O2(g) -> Fe2O3(s)}$.

</details>

---

### Problem 5
Write the formation reaction for $\ce{C2H5OH(l)}$ (ethanol).

<details>
<summary><strong>Solution</strong></summary>

Parts $\ce{C(graphite)}$, $\ce{H2(g)}$, $\ce{O2(g)}$; product 1 mol has 2 C, 6 H, 1 O. Two graphite, three $\ce{H2}$ (= 6 H), half $\ce{O2}$ (= 1 O):

$$\ce{2C(graphite) + 3H2(g) + 1/2 O2(g) -> C2H5OH(l)}$$

**Answer:** $\ce{2C(graphite) + 3H2(g) + 1/2 O2(g) -> C2H5OH(l)}$.

</details>

---

### Problem 6
Find $\Delta H_{rxn}^\circ$ for $\ce{2CO(g) + O2(g) -> 2CO2(g)}$.

<details>
<summary><strong>Solution</strong></summary>

$$\sum\text{prod} = (2)(-393.5) = -787.0$$
$$\sum\text{react} = (2)(-110.5) + (1)(0) = -221.0$$
$$\Delta H_{rxn}^\circ = -787.0 - (-221.0) = -566.0\ \text{kJ}$$

**Answer:** $-566.0$ kJ.

</details>

---

### Problem 7
Find $\Delta H_{rxn}^\circ$ for the decomposition of hydrogen peroxide, $\ce{2H2O2(l) -> 2H2O(l) + O2(g)}$.

<details>
<summary><strong>Solution</strong></summary>

$$\sum\text{prod} = (2)(-285.8) + (1)(0) = -571.6$$
$$\sum\text{react} = (2)(-187.8) = -375.6$$
$$\Delta H_{rxn}^\circ = -571.6 - (-375.6) = -196.0\ \text{kJ}$$

**Answer:** $-196.0$ kJ (exothermic — why peroxide fizzes and warms as it breaks down).

</details>

---

### Problem 8
Find $\Delta H_{rxn}^\circ$ for $\ce{CH4(g) + 2O2(g) -> CO2(g) + 2H2O(g)}$ — note the water is now a **gas**. Compare to Example 7.

<details>
<summary><strong>Solution</strong></summary>

Use $\ce{H2O(g)} = -241.8$, not the liquid value.

$$\sum\text{prod} = (1)(-393.5) + (2)(-241.8) = -393.5 - 483.6 = -877.1$$
$$\sum\text{react} = (1)(-74.8) + (2)(0) = -74.8$$
$$\Delta H_{rxn}^\circ = -877.1 - (-74.8) = -802.3\ \text{kJ}$$

**Answer:** $-802.3$ kJ — less exothermic than Example 7's $-890.3$ kJ, because making water *vapor* instead of *liquid* leaves out the condensation energy. Phase matters.

</details>

---

### Problem 9
Find $\Delta H_{rxn}^\circ$ for $\ce{2SO2(g) + O2(g) -> 2SO3(g)}$.

<details>
<summary><strong>Solution</strong></summary>

$$\sum\text{prod} = (2)(-395.7) = -791.4$$
$$\sum\text{react} = (2)(-296.8) + (1)(0) = -593.6$$
$$\Delta H_{rxn}^\circ = -791.4 - (-593.6) = -197.8\ \text{kJ}$$

**Answer:** $-197.8$ kJ.

</details>

---

### Problem 10
Find $\Delta H_{rxn}^\circ$ for $\ce{N2(g) + O2(g) -> 2NO(g)}$.

<details>
<summary><strong>Solution</strong></summary>

Both reactants are elements → 0.

$$\sum\text{prod} = (2)(+90.3) = +180.6$$
$$\sum\text{react} = (1)(0) + (1)(0) = 0$$
$$\Delta H_{rxn}^\circ = +180.6 - 0 = +180.6\ \text{kJ}$$

**Answer:** $+180.6$ kJ — **endothermic**. It takes hot engine/lightning conditions to force nitrogen and oxygen together, which is exactly why $\ce{NO}$ has a positive formation tag.

</details>

---

### Problem 11
Find $\Delta H_{rxn}^\circ$ for the Haber process $\ce{N2(g) + 3H2(g) -> 2NH3(g)}$.

<details>
<summary><strong>Solution</strong></summary>

$$\sum\text{prod} = (2)(-45.9) = -91.8$$
$$\sum\text{react} = (1)(0) + (3)(0) = 0$$
$$\Delta H_{rxn}^\circ = -91.8 - 0 = -91.8\ \text{kJ}$$

Notice: because both reactants are elements, $\Delta H_{rxn}$ equals $2\times\Delta H_f^\circ(\ce{NH3})$ — a formation reaction scaled to 2 mol.

**Answer:** $-91.8$ kJ.

</details>

---

### Problem 12
The combustion of methanol, $\ce{2CH3OH(l) + 3O2(g) -> 2CO2(g) + 4H2O(l)}$, has $\Delta H_{rxn}^\circ = -1452.8$ kJ. Use it to find $\Delta H_f^\circ$ of methanol (treat it as unknown, $x$).

<details>
<summary><strong>Solution</strong></summary>

$$-1452.8 = \big[(2)(-393.5) + (4)(-285.8)\big] - \big[(2)x + (3)(0)\big]$$
$$-1452.8 = [-787.0 - 1143.2] - 2x = -1930.2 - 2x$$
$$2x = -1930.2 - (-1452.8) = -1930.2 + 1452.8 = -477.4$$
$$x = -238.7\ \text{kJ/mol}$$

**Answer:** $\Delta H_f^\circ(\ce{CH3OH}) \approx -238.6$ kJ/mol (matches the table; the $0.1$ is rounding). Watch the **coefficient of 2** on methanol — forgetting it doubles your error.

</details>

---

### Problem 13
For $\ce{4NH3(g) + 5O2(g) -> 4NO(g) + 6H2O(g)}$, the measured $\Delta H_{rxn}^\circ = -906.0$ kJ. Given $\Delta H_f^\circ(\ce{NH3}) = -45.9$ and $\Delta H_f^\circ(\ce{H2O(g)}) = -241.8$, solve for $\Delta H_f^\circ$ of $\ce{NO}$.

<details>
<summary><strong>Solution</strong></summary>

Let $x = \Delta H_f^\circ(\ce{NO})$.

$$-906.0 = \big[(4)x + (6)(-241.8)\big] - \big[(4)(-45.9) + (5)(0)\big]$$
$$-906.0 = [4x - 1450.8] - [-183.6] = 4x - 1450.8 + 183.6 = 4x - 1267.2$$
$$4x = -906.0 + 1267.2 = 361.2$$
$$x = +90.3\ \text{kJ/mol}$$

**Answer:** $\Delta H_f^\circ(\ce{NO}) = +90.3$ kJ/mol — the unknown was a **product**, and it still comes straight out of the algebra.

</details>

---

### Problem 14
**Capstone.** Acetylene (welding-torch fuel) burns: $\ce{2C2H2(g) + 5O2(g) -> 4CO2(g) + 2H2O(l)}$. (a) Compute $\Delta H_{rxn}^\circ$. (b) Explain, using its $\Delta H_f^\circ$, why acetylene releases so much energy.

<details>
<summary><strong>Solution</strong></summary>

**(a)** With $\ce{C2H2} = +227.4$:

$$\sum\text{prod} = (4)(-393.5) + (2)(-285.8) = -1574.0 - 571.6 = -2145.6$$
$$\sum\text{react} = (2)(+227.4) + (5)(0) = +454.8$$
$$\Delta H_{rxn}^\circ = -2145.6 - (+454.8) = -2600.4\ \text{kJ}$$

**(b)** Acetylene has a **positive** $\Delta H_f^\circ$ ($+227.4$ kJ/mol) — it sits *above* the element baseline, a high-energy, "wound-up" molecule. In the master equation that positive reactant tag gets **subtracted**, which *adds* to the energy released. So its instability at formation is exactly what makes its combustion so fierce — hot enough to weld steel.

**Answer:** (a) $-2600.4$ kJ; (b) its positive formation enthalpy means it stores extra energy that's dumped out on burning.

</details>

---

### Problem 15
Find $\Delta H_{rxn}^\circ$ for $\ce{CaO(s) + CO2(g) -> CaCO3(s)}$, then state how it relates to Example 9.

<details>
<summary><strong>Solution</strong></summary>

$$\sum\text{prod} = (1)(-1207.0) = -1207.0$$
$$\sum\text{react} = (1)(-635.1) + (1)(-393.5) = -1028.6$$
$$\Delta H_{rxn}^\circ = -1207.0 - (-1028.6) = -178.4\ \text{kJ}$$

**Answer:** $-178.4$ kJ. This is the **exact reverse** of Example 9 ($+178.4$ kJ), so its $\Delta H$ is the same magnitude with the opposite sign — reversing a reaction flips the sign of $\Delta H$, a preview of Hess's law.

</details>

---

## Quick Reference

| Concept | Rule |
|---|---|
| **Standard enthalpy of formation** | Energy to form **1 mol** of a compound from its elements in their standard states; units **kJ/mol** |
| **Standard conditions** | 1 atm, usually 25 °C, 1 M for solutions |
| **Zero baseline** | $\Delta H_f^\circ = 0$ for an element **in its standard state only** |
| **Standard states to know** | $\ce{H2, N2, O2, F2, Cl2}$ gas; $\ce{Br2}$ liq; $\ce{I2}$ solid; $\ce{C}$ = graphite; $\ce{Hg}$ liq; metals solid |
| **Formation reaction** | elements (standard states) $\to$ **1 mol** compound; fractional coefficients allowed |
| **Master equation** | $\Delta H_{rxn}^\circ = \sum n\Delta H_f^\circ(\text{prod}) - \sum n\Delta H_f^\circ(\text{react})$ |
| **Weighting** | multiply each $\Delta H_f^\circ$ by its balancing coefficient |
| **Elements** | drop out (their $\Delta H_f^\circ = 0$) |
| **Reverse problem** | put the unknown as $x$ in the master equation and solve algebraically |
| **Reverse a reaction** | flip the sign of $\Delta H$ |
| **vs. bond enthalpies** | formation = **exact** (tabulated); bond enthalpy = **approximate** (averages) |

---

<div align="center">

[← Bond Enthalpies](/chemistry/0804-bond-enthalpies) | [Hess's Law →](/chemistry/0806-hess-law)

</div>
