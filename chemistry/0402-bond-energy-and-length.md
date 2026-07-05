# Bond Energy and Length
<p class="article-date">July 4, 2026</p>

*I was babysitting my neighbor's kid last weekend, and she made me read Goldilocks three times in a row — so now the story is permanently burned into my brain. You know the drill: the first porridge is too hot, the second is too cold, the third is just right. The big chair is too hard, the small one is too soft, and one is just right. Here's the part that got me: two atoms drifting toward each other live out the exact same story. Too far apart and nothing holds them together — no attraction worth mentioning, energy basically zero. Too close and they shove each other away violently — two positive nuclei jammed together is a disaster. But at one particular distance, the energy hits its lowest possible point, and the atoms settle in like Goldilocks in the just-right chair. That valley in the energy IS the chemical bond, and the two numbers that describe it — how deep the valley is (bond energy) and where the bottom sits (bond length) — are the subject of AP Topic 2.2, one of the most reliably tested diagrams on the whole exam.*

---

## What You'll Learn
- Sketch and label the potential energy (PE) curve for two approaching atoms: axes, the zero line, the well, and the steep repulsion wall
- Explain why potential energy is *defined* as zero at infinite separation and why the well is *negative* — and stop the sign convention from ever tripping you up
- Read **bond length** off a PE curve (the distance at the minimum) and **bond energy** off the same curve (the depth of the well)
- Explain the shape of the curve using Coulomb's law: which attractions pull the atoms in, and which repulsions push them apart
- Compare two PE curves and decide which represents the stronger bond and which the longer bond — with full AP-style justification
- Use **bond order** (single vs. double vs. triple) to predict that more shared pairs means a shorter *and* stronger bond
- Use **atomic size** to predict that bigger atoms form longer, generally weaker bonds (the $\ce{H-F} > \ce{H-Cl} > \ce{H-Br} > \ce{H-I}$ ranking)
- State — and never forget — that **breaking bonds absorbs energy and forming bonds releases energy**, the single sentence that powers Unit 6 thermochemistry
- Preview how tables of bond energies estimate the energy of a whole reaction

---

## Prerequisites
- [Bonds and Electronegativity](/chemistry/0401-bonds-and-electronegativity) — you need to know what a covalent bond is (shared electrons between two nuclei) before we can ask how strong and how long it is
- [Periodic Trends](/chemistry/0305-periodic-trends) — atomic radius drives bond length, so the protons–distance–shielding logic comes straight back

---

## The Core Concept

### Intuition First

Run the Goldilocks story one more time, but let the main character be a hydrogen atom walking toward another hydrogen atom. The "porridge testing" is literally walking along a graph from right to left:

| Goldilocks | Two atoms | Energy |
|---|---|---|
| Wandering in the woods, house nowhere in sight | Atoms **infinitely far apart** — they don't feel each other at all | Defined as **zero** |
| Getting closer, things start looking good | Atoms close enough that **attraction** kicks in | Energy **drops** below zero |
| The **just-right chair** — settles in, totally comfortable | The **just-right distance** — bottom of the energy valley | **Lowest (most negative) energy** — this is the bond |
| Squeezing into a chair three sizes too small | Atoms **too close** — nuclei repel each other hard | Energy **skyrockets** |
| How comfy the just-right chair is — how hard it is to get her out of it | How **deep the valley** is | **Bond energy** — the energy needed to climb out (break the bond) |
| *Where* the just-right chair sits in the room | *Where* the valley bottom sits on the distance axis | **Bond length** |

Two atoms bond because sitting in the valley is more comfortable — lower energy — than wandering alone. And the two questions AP asks about any bond are exactly the two Goldilocks facts: *how deep is the valley?* (bond energy) and *where is its bottom?* (bond length).

### The Potential Energy Curve — THE Diagram of Topic 2.2

Put **internuclear distance** $r$ (the distance between the two nuclei) on the x-axis and **potential energy** on the y-axis. As two atoms approach from far away, the energy traces this shape:

```
 Potential energy (PE)
   ^
   |\
   | \        TOO CLOSE: the repulsion wall.
   |  \       Nuclei shove each other; energy skyrockets.
   |   \
 0 +----\-----------------------------------  <-- TOO FAR: atoms don't feel
   |     \                        ________        each other. PE defined = 0.
   |      \                  ____/
   |       \              __/    curve climbs back
   |        \           _/       toward 0 as atoms separate
   |         \        _/
   |          \_    _/
   |            \__/   <-- JUST RIGHT: bottom of the well
   |             |
   |             |  depth of well below zero = BOND ENERGY
   +-------------+---------------------------->
               r_0 = BOND LENGTH        internuclear distance r
```

Read it right to left, like Goldilocks walking into the house:

1. **Far right ($r \to \infty$): energy = 0.** The atoms are so far apart they don't interact. Nothing pulls, nothing pushes.
2. **Moving left: energy drops.** The atoms are close enough that each nucleus starts attracting the *other* atom's electrons. Attraction lowers the energy — the curve dips below zero.
3. **The minimum at $r_0$: the bottom of the well.** Attraction and repulsion balance perfectly. This is the most stable arrangement — the bond exists here.
4. **Far left ($r$ very small): the wall.** Push the atoms closer than $r_0$ and the two positive nuclei (and the two electron clouds) repel each other ferociously. The energy shoots up almost vertically.

Two numbers come off this graph, and they are the whole topic:

$$\text{Bond length } r_0 = \text{the distance at the minimum (read off the x-axis)}$$

$$\text{Bond energy} = \text{the depth of the well (read off the y-axis, from the minimum up to zero)}$$

For $\ce{H2}$: the minimum sits at $r_0 = 74$ pm with a well depth of $436$ kJ/mol. So the $\ce{H-H}$ bond length is **74 pm** and the bond energy is **436 kJ/mol** — it takes 436 kJ to break one mole of $\ce{H-H}$ bonds and haul the atoms back out to "infinitely far apart."

### The Sign Convention — Why the Well Is *Negative*

This confuses everyone, so let's kill it now.

**Energy is measured relative to a chosen zero, and chemists choose "two atoms infinitely far apart" as zero.** That's a *convention*, like calling sea level "elevation zero." Death Valley isn't a mathematical impossibility just because it's below sea level — it's just lower than the reference point.

Once you set that zero:

- **Lower energy = more stable.** Systems roll downhill. A bonded pair of atoms is *more stable* than two free atoms, so its energy must be *lower* than the free atoms' energy — lower than zero — **negative**.
- The minimum of the $\ce{H2}$ curve sits at $-436$ kJ/mol. That means the bonded molecule is 436 kJ/mol *downhill* from the separated atoms.
- **Bond energy itself is always reported as a positive number** — it's the *size of the climb* out of the well, an amount of energy you must add. "The potential energy at the minimum is $-436$ kJ/mol" and "the bond energy is $436$ kJ/mol" are two phrasings of the same fact.

> **The Goldilocks version:** sitting in the just-right chair is "negative effort" compared to standing — she sank *down* into it. Getting her out requires someone to supply the effort. The depth she sank = the effort to extract her. Negative position, positive extraction cost.

### Why the Curve Has That Shape: Coulomb's Law

Everything on this graph is Coulombic — charges attracting and repelling, exactly the physics from [Periodic Trends](/chemistry/0305-periodic-trends). Between two approaching atoms there are competing interactions:

| Interaction | Charges | Effect |
|---|---|---|
| Each **nucleus** ↔ the *other atom's* **electrons** | $(+)$ and $(-)$ | **Attraction** — pulls the atoms together, lowers PE |
| **Nucleus** ↔ **nucleus** | $(+)$ and $(+)$ | **Repulsion** — pushes apart, raises PE |
| **Electrons** ↔ **electrons** | $(-)$ and $(-)$ | **Repulsion** — pushes apart, raises PE |

At long range, the nucleus–electron attractions dominate — that's the gentle dip as the atoms approach. At very short range, the nucleus–nucleus repulsion explodes (the $r^2$ in the denominator of Coulomb's law means tiny distances create enormous forces) — that's the near-vertical wall. At exactly $r_0$, the pulls and pushes balance: the **net force is zero**, which is precisely why the energy curve is flat (at a minimum) there.

- At $r > r_0$: attraction wins → atoms pulled *inward*.
- At $r < r_0$: repulsion wins → atoms pushed *outward*.
- At $r = r_0$: perfect balance → the just-right chair.

(A real bonded molecule actually vibrates back and forth around $r_0$ like a ball rolling in the valley, so bond length is technically the *average* distance — a nice detail for FRQ answers.)

### Reading and Comparing PE Curves

AP loves showing you two or three unlabeled curves and asking which is which. Two rules answer everything:

> **Deeper well ⇒ stronger bond** (more energy to climb out).
> **Minimum farther right ⇒ longer bond** (bigger equilibrium distance).

Some real anchor values to calibrate your instincts:

| Bond | Bond energy (kJ/mol) | Bond length (pm) |
|---|---|---|
| $\ce{H-H}$ | 436 | 74 |
| $\ce{H-Cl}$ | 431 | 127 |
| $\ce{Cl-Cl}$ | 242 | 199 |
| $\ce{I-I}$ | 151 | 267 |
| $\ce{F-F}$ | 159 | 142 |
| $\ce{N#N}$ | 945 | 110 |

### Bond Order: More Shared Pairs = Shorter AND Stronger

**Bond order** is the number of shared electron pairs: single bond = order 1, double = 2, triple = 3. More shared electrons between the nuclei means more $(+)/(-)$ attraction glue, which pulls the nuclei closer *and* digs the well deeper:

| Bond | Bond order | Bond energy (kJ/mol) | Bond length (pm) |
|---|---|---|---|
| $\ce{C-C}$ | 1 | 347 | 154 |
| $\ce{C=C}$ | 2 | 614 | 134 |
| $\ce{C#C}$ | 3 | 839 | 120 |

Notice the **inverse relationship**: as bond energy goes *up*, bond length goes *down*. Shorter and stronger travel together; longer and weaker travel together. (You'll count these shared pairs systematically once we draw [Lewis structures](/chemistry/0404-lewis-structures) — for now, trust the formulas.)

One caution: doubling the bond order does *not* double the energy ($614 \ne 2 \times 347$). The second and third "glue layers" ($\pi$ bonds, if you want the college word) are individually weaker than the first. AP only needs the ranking, not the arithmetic.

### Atomic Size: Bigger Atoms → Longer, Generally Weaker Bonds

Bond length is roughly the sum of the two atoms' radii — two big atoms simply can't get their nuclei as close together. And Coulomb's law says greater distance between the charges means weaker attraction, so the well is shallower. Watch it happen down Group 17:

| Bond | Bond energy (kJ/mol) | Bond length (pm) |
|---|---|---|
| $\ce{H-F}$ | 565 | 92 |
| $\ce{H-Cl}$ | 431 | 127 |
| $\ce{H-Br}$ | 364 | 141 |
| $\ce{H-I}$ | 297 | 161 |

$$\text{Bond strength: } \ce{H-F} > \ce{H-Cl} > \ce{H-Br} > \ce{H-I}$$

The halogen gets bigger down the group (more shells — [Periodic Trends](/chemistry/0305-periodic-trends)), the bond gets longer, the shared electrons sit farther from the halogen nucleus, and the bond weakens. The word "generally" matters: for atoms of *similar* size, bond order dominates ($\ce{N#N}$ crushes $\ce{F-F}$ despite nitrogen being the slightly bigger atom).

### The Most Important Sentence in This Article

> **Breaking a bond always ABSORBS energy. Forming a bond always RELEASES energy.**

Always. No exceptions. Bonded atoms sit at the bottom of an energy valley; hauling them out of the valley (breaking the bond) requires an energy *input* equal to the well depth, and falling into the valley (forming the bond) *releases* that same amount.

This murders a famous misconception: **bonds do not "store energy" like little batteries.** You've probably heard "energy is stored in the bonds of ATP" or "breaking down food releases the energy in its bonds." Chemically, that phrasing is backwards. A bond is a *low*-energy, stable arrangement — breaking it *costs* energy. Reactions like burning food release energy only because the **new bonds formed in the products release MORE energy than it cost to break the old bonds in the reactants**. The energy comes from the *difference*, not from cracking bonds open like piñatas.

Flag this paragraph. It is the foundation of Unit 6 (thermochemistry), where we'll compute reaction energies all day, and it's a favorite AP trap.

### Sneak Preview: Estimating a Reaction's Energy

Since breaking absorbs and forming releases, you can estimate the energy of a whole reaction from a bond-energy table. Take

$$\ce{H2 + Cl2 -> 2HCl}$$

- **Break:** one $\ce{H-H}$ (436 kJ) and one $\ce{Cl-Cl}$ (242 kJ) → absorb $436 + 242 = 678$ kJ
- **Form:** two $\ce{H-Cl}$ (431 kJ each) → release $2 \times 431 = 862$ kJ

$$\Delta E \approx 678 - 862 = -184 \text{ kJ per mole of reaction}$$

Released energy exceeds absorbed energy, so the reaction gives off energy overall (it's *exothermic* — vocabulary word coming in Unit 6, where this gets the full treatment).

---

## Worked Examples

### Example 1: Labeling the Curve

**Problem:** A PE curve for two $\ce{H}$ atoms has these features: (a) the curve flattens to a constant value at very large $r$; (b) the curve has a minimum at $r = 74$ pm, where PE $= -436$ kJ/mol; (c) the curve rises steeply for $r < 74$ pm. State what each feature represents physically.

**Solution:**

**Step 1 — Feature (a):** At large separation the atoms don't interact, so the PE approaches the reference value of **zero** — this flat region *defines* the energy of two free, separated atoms.

**Step 2 — Feature (b):** The minimum is the most stable arrangement: the bonded molecule. The x-coordinate, 74 pm, is the **bond length**; the depth below zero, 436 kJ/mol, is the **bond energy**.

**Step 3 — Feature (c):** At distances shorter than 74 pm, nucleus–nucleus (and electron–electron) repulsion dominates, so the energy climbs steeply — the repulsion wall.

**Answer:** (a) zero-energy reference of separated atoms; (b) the bond — length 74 pm, energy 436 kJ/mol; (c) the repulsion-dominated region.

### Example 2: The Sign Convention

**Problem:** A student says: "The potential energy of $\ce{H2}$ at its bond length is $-436$ kJ/mol. Negative energy makes no sense, so the diagram must be wrong." Straighten them out.

**Solution:**

**Step 1:** Potential energy is always measured *relative to a chosen zero*. Chemists choose PE $= 0$ for atoms at infinite separation — a convention, like calling sea level zero elevation.

**Step 2:** A bonded molecule is more *stable* than separated atoms, and more stable means *lower* energy. Lower than zero is negative. The negative sign literally says "the molecule is 436 kJ/mol downhill from free atoms."

**Step 3:** The bond energy quoted in tables is the positive climb out: $0 - (-436) = +436$ kJ/mol.

**Answer:** The diagram is right. Negative PE means "more stable than the separated-atom reference," and **the bond energy is the positive quantity 436 kJ/mol** needed to climb from the well back to zero.

### Example 3: Which Force Wins Where?

**Problem:** For two atoms whose PE curve has a minimum at $r_0 = 199$ pm ($\ce{Cl2}$), describe the *net* force between the atoms at (a) $r = 300$ pm, (b) $r = 199$ pm, (c) $r = 120$ pm.

**Solution:**

**Step 1 — (a) $r > r_0$:** Right of the minimum, the curve slopes downhill toward $r_0$: nucleus–electron **attraction dominates**, and the net force pulls the atoms *together*.

**Step 2 — (b) $r = r_0$:** At the minimum, attraction and repulsion **balance exactly** — net force is zero. That's why this is the equilibrium bond length.

**Step 3 — (c) $r < r_0$:** Left of the minimum, nucleus–nucleus and electron–electron **repulsion dominates**; the net force shoves the atoms *apart*.

**Answer:** (a) net attraction inward; (b) zero net force; (c) net repulsion outward.

### Example 4: Two Curves, Two Questions

**Problem:** Curve A has its minimum at $(74 \text{ pm}, -436 \text{ kJ/mol})$. Curve B has its minimum at $(267 \text{ pm}, -151 \text{ kJ/mol})$. Which curve shows the stronger bond? The longer bond? Which real molecules might these be?

**Solution:**

**Step 1 — Strength = well depth.** Curve A's well ($436$ kJ/mol deep) is much deeper than B's ($151$ kJ/mol). **A is the stronger bond.**

**Step 2 — Length = minimum position.** Curve B's minimum sits far to the right (267 pm vs. 74 pm). **B is the longer bond.**

**Step 3 — Identify.** A tiny, strong bond at 74 pm/436 kJ/mol is $\ce{H2}$ — two of the smallest atoms in existence. A long, weak bond at 267 pm/151 kJ/mol fits $\ce{I2}$ — two huge atoms.

**Answer:** A = stronger ($\ce{H2}$); B = longer ($\ce{I2}$). Notice longer went with weaker, as usual.

### Example 5: Matching Three Curves (Classic FRQ Setup)

**Problem:** Three PE curves have minima at (i) $(74 \text{ pm}, -436 \text{ kJ/mol})$, (ii) $(127 \text{ pm}, -431 \text{ kJ/mol})$, (iii) $(267 \text{ pm}, -151 \text{ kJ/mol})$. Match them to $\ce{H2}$, $\ce{HCl}$, and $\ce{I2}$, and justify using atomic size.

**Solution:**

**Step 1 — Rank by atomic size.** Bond length ≈ sum of radii: $\ce{H + H}$ (tiny + tiny) < $\ce{H + Cl}$ (tiny + medium) < $\ce{I + I}$ (huge + huge).

**Step 2 — Match lengths.** Shortest minimum (74 pm) → $\ce{H2}$; middle (127 pm) → $\ce{HCl}$; longest (267 pm) → $\ce{I2}$.

**Step 3 — Sanity-check with depth.** The two short bonds are deep (~430 kJ/mol); the giant $\ce{I-I}$ bond is shallow (151 kJ/mol). Longer tracked with weaker. ✓

**Answer:** (i) $\ce{H2}$, (ii) $\ce{HCl}$, (iii) $\ce{I2}$ — assigned by minimum position, since bond length grows with the size of the bonded atoms.

### Example 6: $\ce{F2}$ vs. $\ce{N2}$ — When Bond Order Rules

**Problem:** One curve has a minimum at $(142 \text{ pm}, -159 \text{ kJ/mol})$ and another at $(110 \text{ pm}, -945 \text{ kJ/mol})$. Match them to $\ce{F2}$ and $\ce{N2}$ and explain why the atoms' similar sizes can't be the deciding factor.

**Solution:**

**Step 1:** $\ce{N}$ and $\ce{F}$ sit in the same period, two boxes apart — nearly the same atomic radius. Size alone can't explain a well that's *six times* deeper.

**Step 2:** Bond order can. $\ce{N2}$ has a triple bond ($\ce{N#N}$, three shared pairs); $\ce{F2}$ has a single bond ($\ce{F-F}$). Three pairs of shared electrons between the nuclei = far more Coulombic glue = much deeper well *and* nuclei pulled closer.

**Step 3:** Match: deep-and-short $(110 \text{ pm}, -945)$ → $\ce{N2}$; shallow-and-longer $(142 \text{ pm}, -159)$ → $\ce{F2}$.

**Answer:** $\ce{N2}$ is the deep, left-shifted curve because its bond order of 3 makes the bond both much stronger and shorter; $\ce{F2}$, with bond order 1, is the shallow curve. (This is why $\ce{N2}$ is famously inert — 945 kJ/mol is a brutal climb.)

### Example 7: Ranking Carbon–Carbon Bonds

**Problem:** Rank $\ce{C-C}$, $\ce{C=C}$, and $\ce{C#C}$ from longest to shortest, and from weakest to strongest. Then check against the real values.

**Solution:**

**Step 1 — Bond order:** 1, 2, 3 respectively. More shared pairs → shorter and stronger.

**Step 2 — Length (longest → shortest):** $\ce{C-C} > \ce{C=C} > \ce{C#C}$. Real values: $154 > 134 > 120$ pm. ✓

**Step 3 — Strength (weakest → strongest):** $\ce{C-C} < \ce{C=C} < \ce{C#C}$. Real values: $347 < 614 < 839$ kJ/mol. ✓

**Answer:** Longest to shortest: $\ce{C-C} > \ce{C=C} > \ce{C#C}$; weakest to strongest: $\ce{C-C} < \ce{C=C} < \ce{C#C}$ — length and strength always run opposite.

### Example 8: The Hydrogen Halides

**Problem:** Without a data table, rank the bonds $\ce{H-F}$, $\ce{H-Cl}$, $\ce{H-Br}$, $\ce{H-I}$ by (a) length and (b) strength, and justify in one AP-worthy sentence.

**Solution:**

**Step 1 — Size trend:** Down Group 17, each halogen adds a shell: radius $\ce{F} < \ce{Cl} < \ce{Br} < \ce{I}$.

**Step 2 — Length:** Bond length grows with atomic size: $\ce{H-F} < \ce{H-Cl} < \ce{H-Br} < \ce{H-I}$ (real: 92, 127, 141, 161 pm).

**Step 3 — Strength:** Longer bond = shared electrons farther from the nuclei = weaker Coulombic attraction: $\ce{H-F} > \ce{H-Cl} > \ce{H-Br} > \ce{H-I}$ (real: 565, 431, 364, 297 kJ/mol).

**Answer:** Length increases and strength decreases down the series; justification: *the halogen's atomic radius increases down the group, increasing the internuclear distance, which by Coulomb's law weakens the attraction between the shared electrons and the nuclei.*

### Example 9: Climbing Out of the Well

**Problem:** The PE curve for $\ce{Cl2}$ bottoms out at $-242$ kJ/mol. (a) How much energy must be supplied to break one mole of $\ce{Cl-Cl}$ bonds? (b) How much energy is released when one mole of $\ce{Cl-Cl}$ bonds *forms* from free atoms?

**Solution:**

**Step 1 — (a):** Breaking the bond means climbing from $-242$ kJ/mol up to $0$. Energy required $= 0 - (-242) = +242$ kJ — an absorption.

**Step 2 — (b):** Forming the bond is the same trip downhill: the system drops 242 kJ/mol into the well, releasing 242 kJ.

**Step 3 — The symmetry:** Breaking and forming the *same* bond always involve the *same amount* of energy, just absorbed vs. released.

**Answer:** (a) **242 kJ absorbed** to break; (b) **242 kJ released** to form. Same number, opposite direction.

### Example 10: Killing the "Energy Stored in Bonds" Myth

**Problem:** A biology textbook says "ATP releases energy when its phosphate bond is broken." Explain what's chemically wrong with this phrasing and what actually happens.

**Solution:**

**Step 1:** Breaking any bond, including the one in ATP, *absorbs* energy — atoms must be lifted out of an energy well. A bond is a stable, low-energy state, not a loaded spring.

**Step 2:** What actually happens: ATP reacts with water, and the **new bonds formed in the products** (ADP and phosphate) are collectively lower in energy — deeper wells — than the bonds that were broken.

**Step 3:** Net accounting: energy released by forming the new bonds exceeds energy absorbed breaking the old ones, so the overall *reaction* releases energy. The energy comes from the difference, not from the broken bond itself.

**Answer:** Bonds don't store energy like batteries; **the reaction releases energy because forming the product bonds releases more energy than breaking the reactant bonds absorbs.**

### Example 11: Sneak-Preview Reaction Estimate

**Problem:** Using bond energies $\ce{H-H} = 436$, $\ce{F-F} = 159$, and $\ce{H-F} = 565$ kJ/mol, estimate the energy change of $\ce{H2 + F2 -> 2HF}$.

**Solution:**

**Step 1 — Energy absorbed (bonds broken):** one $\ce{H-H}$ + one $\ce{F-F}$ $= 436 + 159 = 595$ kJ.

**Step 2 — Energy released (bonds formed):** two $\ce{H-F}$ $= 2 \times 565 = 1130$ kJ.

**Step 3 — Net:** $\Delta E \approx 595 - 1130 = -535$ kJ per mole of reaction. Negative sign: more released than absorbed → energy flows out.

**Answer:** **About $-535$ kJ/mol — the reaction releases roughly 535 kJ per mole**, mostly because $\ce{H-F}$ is such a deep well to fall into. (Full method with all the vocabulary lands in Unit 6.)

### Example 12: Sketch the Change

**Problem:** On one set of axes you have the PE curve for $\ce{C-C}$ (minimum at 154 pm, depth 347 kJ/mol). Describe how the curve for $\ce{C#C}$ would differ.

**Solution:**

**Step 1 — Depth:** Triple bond, bond order 3 → much stronger bond → **deeper well**: minimum near $-839$ kJ/mol instead of $-347$.

**Step 2 — Position:** Stronger attraction pulls the nuclei closer → **minimum shifted left**, to about 120 pm instead of 154 pm.

**Step 3 — Everything else:** Both curves still approach zero at large $r$ and still have a steep repulsion wall at small $r$ — those features are universal.

**Answer:** The $\ce{C#C}$ curve has its minimum **deeper (−839 kJ/mol) and farther left (120 pm)** than the $\ce{C-C}$ curve — shorter and stronger, moving together as always.

---

## Common Mistakes

| The Mistake | Why It Happens | The Fix |
|---|---|---|
| Saying bond energy is "$-436$ kJ/mol" | Reading the well's y-coordinate directly | The well *position* is negative; **bond energy is the positive depth** — the climb out |
| "Breaking bonds releases energy" | Biology-class phrasing about ATP and food | Breaking **absorbs**, forming **releases** — always; reactions release energy only when product bonds release more than reactant bonds cost |
| Confusing well depth with well position | Both are "read off the graph" | Depth (y-axis) = bond **energy**; position of minimum (x-axis) = bond **length** |
| Assuming longer bond = stronger bond | "Bigger must be better" instinct | It's inverse: **shorter bonds are stronger**, for both the bond-order and atomic-size trends |
| Thinking the curve's minimum sits *at* zero energy | Forgetting the reference convention | Zero is defined at **infinite separation**; the bonded state must be *below* zero or there'd be no reason to bond |
| Reading the x-axis as time or "reaction progress" | It looks like a reaction-coordinate diagram (coming in kinetics) | The x-axis here is **internuclear distance** — a geometry, not a timeline |
| Comparing curves by width or shape instead of the minimum | Distracting visual features | Only two readings matter: **how deep** (strength) and **how far right** (length) |
| Expecting a double bond to be exactly twice a single bond's energy | Linear thinking | $\ce{C=C}$ (614) $\ne 2 \times \ce{C-C}$ (694); each extra shared pair adds *less* — AP only needs the ranking |

---

## AP Exam Tips

- **The PE curve is a Unit 2 multiple-choice staple.** Expect: "At which labeled point is the net force between the atoms zero?" (the minimum), "What does the y-value of the minimum represent?" (the negative of the bond energy), and "What happens at distances shorter than the minimum?" (repulsion dominates).
- **FRQs love "which curve corresponds to X — justify."** Use this two-sentence template: *Curve ___ corresponds to ___ because its minimum occurs at a smaller/larger internuclear distance, consistent with the smaller/larger atomic radii (or higher/lower bond order). Its deeper/shallower well indicates a stronger/weaker bond, consistent with ___.* Naming **Coulombic attraction** explicitly earns justification points.
- **State the reference convention when explaining signs:** "Potential energy is defined as zero for the separated atoms; the negative value at the minimum indicates the bonded atoms are lower in energy and therefore more stable." That sentence is basically free points.
- **Bond order arguments require evidence.** On the real exam you justify bond order by drawing the Lewis structure ($\ce{N2}$ has a triple bond, $\ce{F2}$ a single) — that skill arrives in [Lewis Structures](/chemistry/0404-lewis-structures). Until then, memorize the anchor cases $\ce{N2}$, $\ce{O2}$, $\ce{F2}$.
- **Watch the units.** Bond lengths come in picometers (pm) or sometimes angstroms ($1$ Å $= 100$ pm); bond energies in kJ/mol. Mixing them up in an FRQ answer costs credit.
- **"Breaking absorbs, forming releases" is tested in Unit 2 AND Unit 6.** Any answer implying a broken bond releases energy is wrong every single time it appears.
- No calculator needed for any of this — it's a reading-and-reasoning topic.

---

## Practice Problems

### Problem 1
On a potential energy curve for two approaching atoms, what physical quantity is on each axis, and what do (a) the flat region at the far right, (b) the minimum, and (c) the steep rise at the far left each represent?

<details>
<summary><strong>Solution</strong></summary>

x-axis: **internuclear distance** $r$; y-axis: **potential energy**.

(a) The flat region at large $r$ is the **zero-energy reference** — two atoms so far apart they don't interact.

(b) The minimum is the **bond**: its x-coordinate is the bond length, and its depth below zero is the bond energy.

(c) The steep rise at small $r$ is the **repulsion wall** — nucleus–nucleus and electron–electron repulsion dominating when the atoms are squeezed too close.

**Answer: distance vs. potential energy; (a) separated atoms (PE = 0), (b) the bonded state (bond length and energy), (c) repulsion-dominated region.**

</details>

### Problem 2
Why do chemists define the potential energy of two atoms at infinite separation as zero, and why must the bonded molecule's energy then be negative?

<details>
<summary><strong>Solution</strong></summary>

Energy must be measured from *some* reference, and "no interaction at all" is the natural zero — like sea level for elevation. Given that choice, a bonded molecule is **more stable** than the free atoms, and more stable means **lower energy**. Lower than zero is negative. The negative value doesn't mean anything spooky — it just says the bonded state sits *downhill* from the separated-atom reference, which is exactly why the bond forms.

**Answer: zero at infinite separation is a convention (no interaction = reference point); bonding lowers the energy below that reference, so the well is negative — negative = more stable than free atoms.**

</details>

### Problem 3
The PE curve for $\ce{H2}$ has its minimum at $(74 \text{ pm}, -436 \text{ kJ/mol})$. State the bond length and the bond energy of $\ce{H2}$, with correct signs and units.

<details>
<summary><strong>Solution</strong></summary>

Bond length = the x-coordinate of the minimum = **74 pm**.

Bond energy = the depth of the well = the climb from $-436$ kJ/mol up to $0$ = **$+436$ kJ/mol** (reported as a positive number, since it's energy that must be *added* to break the bond).

**Answer: bond length 74 pm; bond energy 436 kJ/mol (positive — the well position is $-436$ kJ/mol, but the bond energy is the positive depth).**

</details>

### Problem 4
Two unlabeled PE curves: Curve A has a deeper minimum located farther left; Curve B has a shallower minimum located farther right. Which curve represents the stronger bond? The longer bond?

<details>
<summary><strong>Solution</strong></summary>

Strength = well depth: Curve A's deeper well means more energy to separate the atoms → **A is the stronger bond**.

Length = minimum position on the x-axis: Curve B's minimum at larger $r$ → **B is the longer bond**.

**Answer: A is stronger; B is longer.** (Typical pattern — shorter and stronger travel together.)

</details>

### Problem 5
Three PE curves have minima at $(74 \text{ pm}, -436 \text{ kJ/mol})$, $(127 \text{ pm}, -431 \text{ kJ/mol})$, and $(267 \text{ pm}, -151 \text{ kJ/mol})$. Assign them to $\ce{H2}$, $\ce{HCl}$, and $\ce{I2}$ and justify.

<details>
<summary><strong>Solution</strong></summary>

Bond length tracks atomic size: $\ce{H+H}$ (two tiny atoms) gives the shortest bond, $\ce{H+Cl}$ intermediate, $\ce{I+I}$ (two of the largest common atoms) the longest.

- $(74, -436)$ → $\ce{H2}$
- $(127, -431)$ → $\ce{HCl}$
- $(267, -151)$ → $\ce{I2}$

Depth check: the long $\ce{I-I}$ bond is also the weakest (151 kJ/mol), consistent with the greater internuclear distance weakening the Coulombic attraction.

**Answer: 74 pm = $\ce{H2}$, 127 pm = $\ce{HCl}$, 267 pm = $\ce{I2}$, assigned by increasing atomic radii of the bonded atoms.**

</details>

### Problem 6
One diatomic curve bottoms out at $(110 \text{ pm}, -945 \text{ kJ/mol})$, another at $(142 \text{ pm}, -159 \text{ kJ/mol})$. One is $\ce{N2}$, the other $\ce{F2}$. Match and justify — and explain why atomic size is NOT the main reason here.

<details>
<summary><strong>Solution</strong></summary>

$\ce{N}$ and $\ce{F}$ are nearly the same size (same period), so size can't explain a six-fold difference in well depth. **Bond order** can: $\ce{N2}$ contains a triple bond ($\ce{N#N}$, 3 shared pairs) while $\ce{F2}$ contains a single bond. Three shared pairs put far more negative charge between the two nuclei, strengthening the Coulombic attraction — a much deeper well AND nuclei pulled closer together.

**Answer: $(110 \text{ pm}, -945)$ = $\ce{N2}$ (triple bond: shorter, far stronger); $(142 \text{ pm}, -159)$ = $\ce{F2}$ (single bond). The deciding factor is bond order, not size.**

</details>

### Problem 7
Rank $\ce{C-C}$, $\ce{C=C}$, and $\ce{C#C}$ (a) from shortest to longest and (b) from strongest to weakest, and state the approximate bond energies.

<details>
<summary><strong>Solution</strong></summary>

Bond orders are 1, 2, 3. More shared pairs → shorter and stronger.

(a) Shortest → longest: $\ce{C#C}$ (120 pm) $< \ce{C=C}$ (134 pm) $< \ce{C-C}$ (154 pm).

(b) Strongest → weakest: $\ce{C#C}$ (≈839 kJ/mol) $> \ce{C=C}$ (≈614 kJ/mol) $> \ce{C-C}$ (≈347 kJ/mol).

**Answer: $\ce{C#C}$ is shortest and strongest (120 pm, 839 kJ/mol); $\ce{C-C}$ is longest and weakest (154 pm, 347 kJ/mol) — length and strength are inverse.**

</details>

### Problem 8
The nitrogen–nitrogen bond energies are roughly: $\ce{N-N}$ 163 kJ/mol, $\ce{N=N}$ 418 kJ/mol, $\ce{N#N}$ 945 kJ/mol. Which has its PE-curve minimum farthest to the left, and why?

<details>
<summary><strong>Solution</strong></summary>

Highest bond order = strongest bond = deepest well = nuclei pulled closest together = **minimum farthest left**. That's $\ce{N#N}$: its three shared pairs create the strongest internuclear attraction, giving both the deepest well ($-945$ kJ/mol) and the shortest equilibrium distance.

**Answer: $\ce{N#N}$ — bond order 3 makes it both the strongest (deepest well) and the shortest (leftmost minimum).**

</details>

### Problem 9
Rank $\ce{H-F}$, $\ce{H-Cl}$, $\ce{H-Br}$, $\ce{H-I}$ by bond length (shortest first) and by bond energy (largest first). Justify with one sentence invoking atomic radius and Coulomb's law.

<details>
<summary><strong>Solution</strong></summary>

Length (shortest → longest): $\ce{H-F} < \ce{H-Cl} < \ce{H-Br} < \ce{H-I}$ (92, 127, 141, 161 pm) — the halogen adds a shell each step down the group.

Energy (largest → smallest): $\ce{H-F} > \ce{H-Cl} > \ce{H-Br} > \ce{H-I}$ (565, 431, 364, 297 kJ/mol).

Justification sentence: *As the halogen's atomic radius increases down the group, the internuclear distance increases, and by Coulomb's law the attraction between the shared electrons and the nuclei weakens, so the bond becomes longer and weaker.*

**Answer: length increases and strength decreases from $\ce{H-F}$ to $\ce{H-I}$.**

</details>

### Problem 10
True or false, then fix if false: "When the $\ce{Cl-Cl}$ bond in $\ce{Cl2}$ breaks, 242 kJ/mol of energy is released."

<details>
<summary><strong>Solution</strong></summary>

**False.** Breaking a bond means lifting the atoms out of the potential energy well — from $-242$ kJ/mol up to $0$ — which requires an energy **input**. Corrected: *breaking one mole of $\ce{Cl-Cl}$ bonds **absorbs** 242 kJ; **forming** one mole of $\ce{Cl-Cl}$ bonds from free atoms releases 242 kJ.*

**Answer: False — bond breaking always absorbs energy; 242 kJ/mol is absorbed on breaking and released on forming.**

</details>

### Problem 11
For a bond with equilibrium length $r_0$: at a distance $r < r_0$, which interactions dominate, and what does the net force do? Name the specific Coulombic players.

<details>
<summary><strong>Solution</strong></summary>

At $r < r_0$ the atoms are compressed past the balance point. The **repulsions dominate**: nucleus–nucleus repulsion ($+$ vs. $+$) plus electron cloud–electron cloud repulsion ($-$ vs. $-$). These outweigh the nucleus–electron attractions, so the net force pushes the atoms **apart**, back toward $r_0$ — which is why the PE curve rises so steeply there.

**Answer: nucleus–nucleus and electron–electron repulsion dominate; the net force is outward (repulsive), driving the atoms back toward the equilibrium distance.**

</details>

### Problem 12
Why is "bond length" reported as an *average* distance rather than a fixed one? (Think about a ball resting in a valley — does it ever sit perfectly still?)

<details>
<summary><strong>Solution</strong></summary>

A real bonded molecule always has some energy above the very bottom of the well, so the atoms **vibrate** — the internuclear distance oscillates back and forth around $r_0$ like a ball rolling side to side in a valley. Stretch past $r_0$ and net attraction pulls the atoms back; compress below $r_0$ and net repulsion pushes them out. The reported bond length is the **average** internuclear distance of that vibration, centered on the well minimum.

**Answer: the atoms constantly vibrate around the equilibrium distance, so bond length is the average internuclear distance, centered at the PE-curve minimum.**

</details>

### Problem 13
Using bond energies $\ce{H-H} = 436$, $\ce{Cl-Cl} = 242$, and $\ce{H-Cl} = 431$ kJ/mol, estimate the energy change for $\ce{H2 + Cl2 -> 2HCl}$ and state whether energy is absorbed or released overall.

<details>
<summary><strong>Solution</strong></summary>

Bonds broken (energy absorbed): $\ce{H-H} + \ce{Cl-Cl} = 436 + 242 = 678$ kJ.

Bonds formed (energy released): $2 \times \ce{H-Cl} = 2 \times 431 = 862$ kJ.

Net: $\Delta E \approx 678 - 862 = -184$ kJ per mole of reaction. More energy is released forming the two $\ce{H-Cl}$ bonds than was absorbed breaking the reactant bonds.

**Answer: $\Delta E \approx -184$ kJ/mol — energy is released overall (the reaction is exothermic).**

</details>

### Problem 14
FRQ-style: Two PE curves are shown for $\ce{Br2}$ and $\ce{F2}$. Curve 1 has its minimum at a larger internuclear distance and a shallower depth than Curve 2. Assign the curves and write a two-sentence justification worthy of full credit.

<details>
<summary><strong>Solution</strong></summary>

$\ce{Br}$ is larger than $\ce{F}$ (more occupied shells), so $\ce{Br-Br}$ has the greater internuclear distance → **Curve 1 = $\ce{Br2}$**, **Curve 2 = $\ce{F2}$**.

Model justification: *"Curve 1 corresponds to $\ce{Br2}$ because its minimum occurs at a larger internuclear distance, consistent with the larger atomic radius of bromine. The greater distance between the shared electrons and the nuclei weakens the Coulombic attraction, consistent with Curve 1's shallower well (weaker bond)."*

(Fun wrinkle: $\ce{F-F}$ at 159 kJ/mol is actually slightly *weaker* than $\ce{Br-Br}$ at 193 kJ/mol in real data — fluorine's lone pairs crowd each other at such a short distance. AP questions are built to avoid this anomaly, so answer with the general trend unless data says otherwise.)

**Answer: Curve 1 = $\ce{Br2}$ (larger atoms → longer bond), Curve 2 = $\ce{F2}$; justify via atomic radius → internuclear distance → Coulombic attraction.**

</details>

### Problem 15
A classmate looks at a PE curve and says, "The bond energy is where the curve crosses zero." Identify both things wrong with this reading and give the correct procedure.

<details>
<summary><strong>Solution</strong></summary>

Two errors:

1. **Wrong feature.** The zero-crossing is just a point where PE happens to equal the separated-atom reference — it has no special chemical meaning. The bond lives at the **minimum**.
2. **Wrong axis logic.** Bond energy is a *depth* (a y-axis difference), not a location.

Correct procedure: find the minimum of the curve. Read the **x-coordinate** → bond length. Read the **y-coordinate** and take its distance below zero → bond energy (a positive number: $0 - E_{min}$).

**Answer: bond energy is the depth of the well below the zero line (measured at the minimum), and bond length is the x-position of that minimum — the zero-crossing is meaningless for both.**

</details>

---

## Quick Reference

| Concept | The One-Liner |
|---|---|
| PE curve axes | x = internuclear distance $r$; y = potential energy |
| Zero of energy | Defined at infinite separation (no interaction) — a convention |
| Well is negative | Bonded state is *lower* energy = more stable than free atoms |
| **Bond length** | x-position of the curve's minimum (where net force = 0) |
| **Bond energy** | Depth of the well below zero — always reported positive |
| Pulls inward | Nucleus ↔ other atom's electrons ($+/-$ attraction) |
| Pushes outward | Nucleus ↔ nucleus and electrons ↔ electrons ($+/+$, $-/-$ repulsion) |
| Deeper well | Stronger bond |
| Minimum farther right | Longer bond |
| Bond order ↑ | Shorter AND stronger ($\ce{C-C}$ 347/154 → $\ce{C=C}$ 614/134 → $\ce{C#C}$ 839/120, in kJ/mol and pm) |
| Atom size ↑ | Longer, generally weaker ($\ce{H-F} > \ce{H-Cl} > \ce{H-Br} > \ce{H-I}$ in strength) |
| Breaking bonds | **Absorbs** energy — always |
| Forming bonds | **Releases** energy — always |
| Reaction energy (preview) | ≈ (energy to break reactant bonds) − (energy released forming product bonds) |

---

<div align="center">

[← Bonds and Electronegativity](/chemistry/0401-bonds-and-electronegativity) | [Ionic Solids, Metals, Alloys →](/chemistry/0403-ionic-solids-metals-alloys)

</div>
