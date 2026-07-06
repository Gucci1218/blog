# Introduction to Equilibrium
<p class="article-date">July 5, 2026</p>

*At the gym last weekend I hopped on a treadmill, cranked the belt up, and started sprinting. Legs pumping, arms swinging, sweat flying off my forehead — I was working as hard as I possibly could. And yet if you'd taken a photo, I looked completely frozen: I stayed pinned to the exact same spot on the machine the entire time. That's the whole trick of a treadmill. The belt drags me backward at precisely the speed I'm running forward, so my two motions cancel and my position never changes. But "not moving" is a total illusion — underneath that stillness there are two furious things happening at once, perfectly matched. Chemical equilibrium is that treadmill. A reaction at equilibrium looks dead: the color stops changing, the pressure holds steady, the concentrations flatline. But nothing has actually stopped. The forward reaction and the reverse reaction are both still running full speed — they've just tied. This is AP Unit 7, Topics 7.1, 7.2, and 7.8, and it reframes everything you learned about reactions: many of them don't run to completion and quit. They run to a two-way standoff and stay there, molecules converting back and forth forever.*

---

## What You'll Learn
- Explain what a **reversible reaction** is and why we write it with a double arrow $\ce{<=>}$ instead of a single arrow
- Describe **dynamic equilibrium** as the state where the **forward rate equals the reverse rate**, so concentrations stop changing while both reactions keep running
- Nail the single biggest distinction in the unit: at equilibrium the **rates** are equal, but the **concentrations** are almost never equal
- Trace the **approach to equilibrium** over time — how the forward rate falls, the reverse rate rises, and they meet — and sketch the rate-vs-time and concentration-vs-time graphs
- Distinguish the **macroscopic view** (what a person watching the flask sees) from the **particulate view** (what the molecules are actually doing)
- Interpret **particulate diagrams** of an equilibrium mixture and reason about the relative amounts of reactant and product
- Cite the evidence that equilibrium is **dynamic, not static** (isotope-labeling experiments)
- State the **conditions required** for equilibrium (closed system, constant temperature) and explain why equilibrium can be reached from **either direction**

---

## Prerequisites
- [Reaction Rates](/chemistry/0701-reaction-rates) — equilibrium is defined entirely in terms of a **forward rate** and a **reverse rate**, and it hinges on the fact that rates *change* as concentrations change; if "rate falls as reactant depletes" isn't automatic for you yet, start there
- [Catalysis](/chemistry/0706-catalysis) — that article introduced the idea that reactions can run **both ways** on the same energy landscape; equilibrium is what happens when we let the reverse trip matter as much as the forward one

---

## The Core Concept

### Intuition First

Back to me sweating on that treadmill. Let's map it part-for-part, because in this blog the analogy always has to line up exactly, not just *feel* similar:

| Treadmill | Chemical reaction |
|---|---|
| How fast I'm running forward | **Forward reaction rate** (reactants → products) |
| How fast the belt drags me back | **Reverse reaction rate** (products → reactants) |
| My position on the machine | **Concentrations** of reactants and products |
| Position stops changing (I hold one spot) | **Equilibrium reached** — concentrations constant |
| Still sweating, legs still pumping | The reaction is **dynamic** — both directions still running |
| Belt speed matching my run speed | Forward rate $=$ reverse rate |

When I first step on, the belt is slow and I'm running fast, so I lurch forward toward the front of the machine. As I drift forward, the treadmill's sensor speeds the belt up. Eventually the belt speed climbs to match my running speed exactly — and at that instant I stop drifting and lock into one spot. I haven't stopped running. The belt hasn't stopped moving. The two just became **equal**, so my *net* motion is zero.

That "net zero" is the entire concept. A reaction at equilibrium isn't a reaction that finished and switched off. It's a reaction where the trip forward (reactants turning into products) and the trip backward (products turning back into reactants) are happening at the **same rate**, so for every molecule of product made each second, one molecule of product is converted back — and the amounts of everything hold steady.

Here's the twist I want burned into your brain before we go one step further. Me holding my spot on the treadmill does **not** mean I'm standing in the exact center. I could be locked in place near the front, or locked in place near the back — anywhere the belt speed happens to match my run speed. "Not moving" tells you the speeds are equal; it tells you **nothing** about where I am. In the same way, equilibrium tells you the *rates* are equal. It says almost nothing about whether there's more reactant or more product sitting in the flask. Rates equal, concentrations frozen — but frozen concentrations are hardly ever *equal* concentrations. Hold that thought; it's the trap the AP exam sets on nearly every equilibrium question.

### Reversible Reactions and the Double Arrow

So far every reaction we've written used a single arrow, $\ce{->}$, which quietly promises "this runs left to right until the reactants are gone." Plenty of reactions really do that — they **go to completion**. But a huge number don't. Instead, as products build up, the products start reacting *back* into reactants, and the reaction settles at a mixture of both.

We flag these with a **double arrow**:

$$\ce{H2 + I2 <=> 2HI}$$

Read $\ce{<=>}$ as "reacts in both directions." The **forward reaction** ($\ce{H2 + I2 -> 2HI}$) and the **reverse reaction** ($\ce{2HI -> H2 + I2}$) are both real, both happening, in the same container at the same time.

Why don't these reactions just finish? Because the products are perfectly capable of colliding and reforming the reactants. As soon as any $\ce{HI}$ exists, some of it breaks back apart. The reaction can never "run out" and stop, because it's being fed from both ends.

### Dynamic Equilibrium: The Formal Definition

**Dynamic equilibrium** is the state a reversible reaction reaches when:

$$\text{rate}_{\text{forward}} = \text{rate}_{\text{reverse}}$$

At that moment, and from then on:

- **Concentrations stop changing.** $[\ce{H2}]$, $[\ce{I2}]$, and $[\ce{HI}]$ each settle at some constant value and stay there.
- **Nothing is "used up."** There is always reactant left and always product present — the reaction does not consume itself to zero.
- **Molecules keep converting both ways.** Reactant is still turning into product and product is still turning back into reactant — just at matched speeds, so the *net* change is zero.

The word **dynamic** is doing enormous work. "Static" would mean everything froze and stopped. That is **not** what happens. The machinery never stops; it's balanced. Every second, some $\ce{H2}$ and $\ce{I2}$ combine into $\ce{HI}$, and in that same second an equal amount of $\ce{HI}$ splits back into $\ce{H2}$ and $\ce{I2}$. The books balance to zero, but the transactions never stop.

> **Equal rates, NOT equal concentrations.** Say it out loud. At equilibrium, forward rate $=$ reverse rate. That does **not** mean $[\text{reactant}] = [\text{product}]$. A flask at equilibrium can be 99% product and 1% reactant, or the reverse, or anything in between — the point is only that whatever the amounts are, they've stopped changing. This is the single most tested misconception in the entire unit.

### The Approach to Equilibrium (Tie It Back to Rates)

Let's watch a reaction get to equilibrium, starting from **pure reactants** — say we dump $\ce{H2}$ and $\ce{I2}$ into a sealed flask with zero $\ce{HI}$. Everything you learned in [Reaction Rates](/chemistry/0701-reaction-rates) about "rate depends on how much stuff is left" is about to pay off.

**At the very start ($t = 0$):**
- Reactant concentration is at its *maximum*, so the **forward rate is at its maximum** — lots of $\ce{H2}$ and $\ce{I2}$ colliding.
- There is *no* $\ce{HI}$ yet, so the **reverse rate is zero** — nothing to react backward.

**As time passes:**
- $\ce{H2}$ and $\ce{I2}$ get consumed, so the **forward rate falls** (fewer reactant collisions — the flattening curve from the rates article).
- $\ce{HI}$ builds up, so the **reverse rate rises** (more product means more backward collisions).

**Eventually:**
- The falling forward rate and the rising reverse rate **meet**. From that instant on, they stay locked together, and the concentrations go flat. **That's equilibrium.**

Here's the **rate-vs-time** picture in ASCII. The forward rate starts high and drops; the reverse rate starts at zero and climbs; they merge and run together:

```
 rate
  |\
  | \  forward rate (starts high, falls)
  |  \___
  |      \_____
  |            \=================  <- equal from here on: EQUILIBRIUM
  |        _____/
  |   ____/
  |  /  reverse rate (starts at 0, rises)
  | /
  |/________________________________ time
  0          t_eq
```

And here's the matching **concentration-vs-time** picture. Reactants fall from their starting value and level off; product rises from zero and levels off. Everything goes flat at $t_{eq}$ — but notice the flat lines sit at *different heights*, because the concentrations are constant, not equal:

```
 conc
  |
  |‾‾‾\___                 [product] rises, then flat
  |       ‾‾‾----________
  |                      ============  <- flat: constant
  |       ______________
  |   ___/               ============  <- flat: constant (different height!)
  |__/                    [reactant] falls, then flat
  |________________________________ time
  0          t_eq
```

The two curves flatten at the *same time* (that's equilibrium being reached) but at *different heights* (that's concentrations being constant, not equal). Both pictures tell the same story the treadmill did: the moment the two rates match, the position stops changing.

### Macroscopic vs Particulate: Two Views of the Same Flask (7.8)

There are two completely different ways to "look at" a reaction, and AP loves to make you switch between them.

**The macroscopic view** is what a person standing at the lab bench sees with their eyes and instruments — bulk properties averaged over trillions of molecules:

- **Color** stops changing (if a species is colored)
- **Pressure** holds steady (for gas reactions where mole count differs)
- **Concentration**, **pH**, **mass**, **density** — all constant

To this observer, the reaction looks **finished and dead**. Nothing is happening.

**The particulate view** is what you'd see if you could shrink down and watch individual molecules. Down here it's chaos: molecules are constantly colliding, reactants are turning into products, products are turning back into reactants, every single second. **Nothing is still.**

Both descriptions are true *at the same time*. That's the entire point of the word "dynamic." Macroscopically constant, particulately frantic. The treadmill photo looks frozen (macroscopic); the runner is drenched in sweat (particulate).

**Reading particulate diagrams.** The exam will show you a box of circles representing molecules and ask you to reason about it. Suppose $\ce{A2}$ (drawn as two joined circles) converts to $2\,\ce{A}$ (single circles): $\ce{A2 <=> 2A}$. Consider three snapshots of the *same* container over time:

```
 t = 0 (start)      t = middle         t = equilibrium & later
 +-----------+      +-----------+      +-----------+   +-----------+
 | (00) (00) |      | (00)  o o |      | (00)  o   |   |  o   (00) |
 | (00) (00) |      |  o  (00)  |      |  o  o (00)|   |(00) o   o |
 | (00) (00) |      | (00) o  o |      | o  (00) o |   | o (00)  o |
 +-----------+      +-----------+      +-----------+   +-----------+
 all A2, no A       some A2 split      A2 & A steady   SAME counts,
                    into A atoms       (say 3 A2, 6 A) rearranged
```

- **At $t = 0$:** all $\ce{A2}$, no $\ce{A}$. The reaction can only go forward.
- **In the middle:** some $\ce{A2}$ has split. Both forward and reverse are now happening, but they haven't matched yet, so the counts are still shifting.
- **At equilibrium and beyond:** compare the last two boxes. The *number* of $\ce{A2}$ and the *number* of $\ce{A}$ are the **same** in both boxes — that's equilibrium. But look closely: the individual molecules are in *different positions and pairings*. Specific $\ce{A2}$ molecules broke apart and different $\ce{A}$ atoms paired up. The totals froze; the identities kept churning. That side-by-side "same counts, different arrangement" is the visual fingerprint of dynamic equilibrium.

To judge which direction a reaction "favors," just count: if an equilibrium box is mostly product particles, the forward reaction is favored (lots of product); if it's mostly reactant particles, the reverse is favored. And notice — you can read that off the picture *without the amounts being equal*. Once again: constant, not equal.

### Evidence That Equilibrium Is Really Dynamic

If the concentrations never change, how do we *know* molecules are still swapping back and forth? Maybe the reaction genuinely stopped and it just happens to have leftover reactant.

The cleanest proof is an **isotope-labeling experiment**. Take a reaction sitting quietly at equilibrium, then add a tiny amount of reactant made with a heavier isotope — for example, feed in some $\ce{H2}$ where the hydrogens are the heavy isotope deuterium ($\ce{D}$, or $\ce{^2H}$). The bulk concentrations don't shift at all; the system is still at equilibrium. But when you analyze the mixture a while later, you find the heavy label has **spread into the product** — you now detect labeled $\ce{HI}$ (as $\ce{DI}$) even though the total amount of $\ce{HI}$ never changed.

The only way the label could migrate from reactant into product is if reactant molecules are *still* converting into product (and product back into reactant) the whole time. If the reaction had truly stopped, the label would sit inertly in the reactant pool forever. The exchange is the smoking gun: **equilibrium is a two-way traffic jam, not an empty road.**

### Conditions for Equilibrium

A system only reaches (and holds) equilibrium under two conditions:

1. **Closed system.** Nothing can enter or leave — no reactants added, no products escaping. On the treadmill, this is the machine's frame keeping me on the belt. A sealed soda bottle is closed; an open glass of soda is *not* (the $\ce{CO2}$ escapes into the room and never comes back, so it never balances). This is why an open flask of a gas-producing reaction runs to completion — the product leaves and can't react backward.
2. **Constant temperature.** Temperature sets *how fast* both the forward and reverse reactions run (recall the temperature factor from kinetics). Change the temperature and you change the balance point itself. Equilibrium is defined *at a specified temperature*.

### Equilibrium From Either Direction

Here's a genuinely beautiful fact. For a given reaction at a given temperature in a closed container, you reach the **same** equilibrium state whether you start with **all reactants** or **all products**.

Start with pure $\ce{H2 + I2}$: the reaction runs forward, making $\ce{HI}$, until the rates match. Start instead with pure $\ce{HI}$: the reaction runs *backward*, breaking down into $\ce{H2}$ and $\ce{I2}$, until the rates match — and it lands on the *identical* final mixture. Same concentrations, same everything.

On the treadmill: I lock into the same spot whether I stepped on near the front and drifted back, or stepped on near the back and drifted forward. The final resting position is set by the machine, not by where I started. Equilibrium is a *destination*, and the reaction can drive there from either side.

### Real Everyday Equilibria

- **A sealed soda** (callback to [Why Chemistry Matters](/chemistry/0001-why-chemistry-matters) and [Solubility and Separation](/chemistry/0507-solubility-and-separation)): inside a capped bottle, dissolved carbon dioxide and gaseous carbon dioxide sit in equilibrium, $\ce{CO2(aq) <=> CO2(g)}$. Dissolved gas escapes into the headspace as fast as gas from the headspace redissolves — constant fizz potential, no visible change. Crack the cap and you *break the closed system*: gas escapes into the room, the reverse trip can't keep up, and the soda slowly goes flat.
- **Sweat in a closed room:** water evaporating off your skin and water vapor condensing back reach a balance, $\ce{H2O(l) <=> H2O(g)}$, once the air's humidity stops rising. In a *sealed* room, evaporation rate finally equals condensation rate and the humidity holds steady — a phase equilibrium, same idea as the soda.
- **The $\ce{N2O4}$/$\ce{NO2}$ color demo** (a classic lecture-hall favorite): colorless dinitrogen tetroxide is in equilibrium with brown nitrogen dioxide, $\ce{N2O4(g) <=> 2NO2(g)}$. In a sealed tube the brown color holds perfectly steady — macroscopically frozen — even though molecules are joining and splitting nonstop. It's the treadmill you can literally see: nothing changes, everything is happening.

---

## Worked Examples

**Example 1: Single Arrow or Double Arrow?**

**Problem:** A reaction is placed in a sealed flask and, over time, settles into a mixture that still contains a measurable amount of *both* reactant and product, with concentrations that stop changing. Should it be written with $\ce{->}$ or $\ce{<=>}$?

**Solution:**
- *Step 1 — what does leftover reactant tell us?* If the reaction had gone to completion, essentially no reactant would remain. Measurable reactant left over means it stopped short of completion.
- *Step 2 — what stops it short?* The product must be reacting back into reactant, balancing the forward trip. That's a reversible reaction.

**Answer:** Use the double arrow, $\ce{<=>}$ — the coexistence of reactant and product at unchanging concentrations is the signature of equilibrium.

---

**Example 2: The Core Distinction — Rates vs Concentrations**

**Problem:** A student says, "At equilibrium, the concentration of reactants equals the concentration of products." Is this right? If not, fix the statement.

**Solution:**
- *Step 1 — identify the error.* Equilibrium is defined by equal *rates*, not equal *concentrations*.
- *Step 2 — state what's actually equal.* The forward rate equals the reverse rate.
- *Step 3 — state what's actually true of concentrations.* They become *constant* (stop changing), but they are almost never equal to each other.

**Answer:** Wrong. Correct version: "At equilibrium, the forward and reverse **rates** are equal, so the concentrations become **constant** — but the reactant and product concentrations are generally **not** equal to each other."

---

**Example 3: Reading the Rate-vs-Time Graph**

**Problem:** A reaction starts from pure reactants. Describe how the forward rate and the reverse rate each behave from $t = 0$ until equilibrium, and identify what's true of the two rates at equilibrium.

**Solution:**
- *Step 1 — forward rate.* Starts at its **maximum** (reactant concentration highest) and **decreases** as reactant is consumed.
- *Step 2 — reverse rate.* Starts at **zero** (no product yet) and **increases** as product builds up.
- *Step 3 — equilibrium.* The decreasing forward rate meets the increasing reverse rate; from there they are **equal** and stay equal.

**Answer:** Forward rate falls from a maximum; reverse rate rises from zero; at equilibrium they are equal (and nonzero) — both reactions are still running.

---

**Example 4: Finding Equilibrium on a Concentration-vs-Time Graph**

**Problem:** For $\ce{A <=> B}$ (starting from pure $\ce{A}$), the following data are collected. At what time has the system reached equilibrium?

| Time (s) | $[\ce{A}]$ (M) | $[\ce{B}]$ (M) |
|---|---|---|
| 0 | 1.00 | 0.00 |
| 20 | 0.70 | 0.30 |
| 40 | 0.55 | 0.45 |
| 60 | 0.50 | 0.50 |
| 80 | 0.50 | 0.50 |
| 100 | 0.50 | 0.50 |

**Solution:**
- *Step 1 — find where concentrations stop changing.* Both $[\ce{A}]$ and $[\ce{B}]$ are still moving through $t = 40$, but from $t = 60$ onward they hold at $0.50$ and $0.50$.
- *Step 2 — earliest flat point.* The values first become constant at $t = 60\ \text{s}$.

**Answer:** Equilibrium is reached at $t = 60\ \text{s}$ (the first time both concentrations stop changing). *Note:* here they happen to be equal at $0.50$ each — that's a coincidence of this particular reaction, not a requirement of equilibrium.

---

**Example 5: Constant Doesn't Mean Equal**

**Problem:** For $\ce{X <=> Y}$ starting from pure $\ce{X}$, the concentrations level off at $[\ce{X}] = 0.80\ \text{M}$ and $[\ce{Y}] = 0.20\ \text{M}$ and stay there. Is the system at equilibrium? Which reaction is favored?

**Solution:**
- *Step 1 — is it equilibrium?* The concentrations have stopped changing, so yes — the forward and reverse rates are equal.
- *Step 2 — equal concentrations?* No: $0.80 \neq 0.20$. That's fine — equilibrium requires equal *rates*, not equal amounts.
- *Step 3 — which side is favored?* More reactant ($\ce{X}$) remains than product ($\ce{Y}$), so the mixture favors reactants.

**Answer:** Yes, it's at equilibrium (constant concentrations). The concentrations are *not* equal, and the reaction favors the **reactant** side ($\ce{X}$).

---

**Example 6: Interpreting a Particulate Diagram**

**Problem:** For $\ce{A2 <=> 2A}$ at equilibrium, a particulate snapshot of the box contains 4 intact $\ce{A2}$ molecules and 8 single $\ce{A}$ atoms. Describe what's happening at the particle level and state whether the amounts are changing.

**Solution:**
- *Step 1 — read the counts.* 4 $\ce{A2}$ and 8 $\ce{A}$ coexist.
- *Step 2 — macroscopic view.* Because it's at equilibrium, these counts stay steady — a person measuring would see no change.
- *Step 3 — particulate view.* Individual $\ce{A2}$ molecules are still splitting into $\ce{A}$ atoms, and pairs of $\ce{A}$ atoms are still recombining into $\ce{A2}$, at equal rates. The *specific* molecules keep changing even though the *totals* don't.

**Answer:** The overall counts (4 $\ce{A2}$, 8 $\ce{A}$) are constant, but at the particle level $\ce{A2}$ is continuously splitting and $\ce{A}$ atoms are continuously recombining at matched rates — dynamic, not static.

---

**Example 7: Comparing Two Particulate Boxes**

**Problem:** Two boxes show the *same* reaction $\ce{A2 <=> 2A}$ at two later times. Box 1 (at $t = 50\ \text{s}$): 5 $\ce{A2}$, 6 $\ce{A}$. Box 2 (at $t = 70\ \text{s}$): 5 $\ce{A2}$, 6 $\ce{A}$, with the molecules in different positions. Has equilibrium been reached by $t = 50\ \text{s}$? How do you know?

**Solution:**
- *Step 1 — compare totals.* Box 1 and Box 2 have identical counts of each species (5 and 6).
- *Step 2 — interpret.* Between $t = 50$ and $t = 70\ \text{s}$ the composition did not change, so concentrations are constant across that span.
- *Step 3 — the rearrangement.* The molecules moved and re-paired (different specific $\ce{A2}$ and $\ce{A}$), confirming the reaction is still running both ways.

**Answer:** Yes — equilibrium was reached by $t = 50\ \text{s}$, because the counts are unchanged from $t = 50$ to $t = 70\ \text{s}$. The rearranged positions confirm it's *dynamic* equilibrium (molecules still converting), not a dead reaction.

---

**Example 8: What's Constant and What's Changing?**

**Problem:** For the sealed-tube demo $\ce{N2O4(g) <=> 2NO2(g)}$ (colorless $\ce{N2O4}$, brown $\ce{NO2}$) held at constant temperature and at equilibrium, sort these into "constant" and "still changing": (a) the brown color intensity, (b) individual molecules converting, (c) total pressure, (d) which specific molecules are $\ce{N2O4}$ vs $\ce{NO2}$.

**Solution:**
- *Step 1 — macroscopic (bulk) properties:* color intensity (a) and total pressure (c) are averaged over all molecules → **constant** at equilibrium.
- *Step 2 — particulate (molecular) events:* individual conversions (b) and the identity of which molecules are which (d) → **constantly changing**.

**Answer:** Constant: color intensity and total pressure. Still changing: individual molecule conversions and the identities of specific molecules. (Macroscopically frozen, particulately busy.)

---

**Example 9: Approach From Either Direction**

**Problem:** In one sealed flask you start with pure $\ce{HI}$; in an identical flask at the same temperature you start with the stoichiometrically equivalent amount of pure $\ce{H2} + \ce{I2}$ for $\ce{H2 + I2 <=> 2HI}$. Compare the two final equilibrium mixtures.

**Solution:**
- *Step 1 — flask A (pure $\ce{HI}$).* No $\ce{H2}$ or $\ce{I2}$ yet, so only the reverse reaction can run at first; $\ce{HI}$ decomposes until rates match.
- *Step 2 — flask B (pure $\ce{H2} + \ce{I2}$).* No $\ce{HI}$ yet, so only the forward reaction runs at first; $\ce{HI}$ forms until rates match.
- *Step 3 — compare.* Same reaction, same temperature, same closed system, equivalent total amounts of atoms → they arrive at the **identical** equilibrium concentrations, just approached from opposite sides.

**Answer:** The two flasks end up with the *same* equilibrium concentrations of $\ce{H2}$, $\ce{I2}$, and $\ce{HI}$. Equilibrium is a destination reachable from either direction.

---

**Example 10: Why the Open Soda Goes Flat**

**Problem:** A capped bottle of soda holds $\ce{CO2(aq) <=> CO2(g)}$ at equilibrium. Explain, using the conditions for equilibrium, why an *open* bottle eventually goes completely flat instead of reaching equilibrium.

**Solution:**
- *Step 1 — the capped bottle.* It's a **closed system**: $\ce{CO2}$ gas leaving the liquid is trapped in the headspace and redissolves as fast as it escapes → equilibrium, constant fizz.
- *Step 2 — open it.* The system is no longer closed. $\ce{CO2(g)}$ escapes into the room and disperses; it can't return to redissolve.
- *Step 3 — consequence.* The reverse trip (gas → dissolved) is starved, so the forward trip (dissolved → gas) keeps winning. Dissolved $\ce{CO2}$ steadily leaves until essentially none is left.

**Answer:** An open bottle violates the **closed-system** requirement — escaping $\ce{CO2}$ can't come back, so the reaction runs to completion (goes flat) instead of balancing at equilibrium.

---

**Example 11: Static vs Dynamic**

**Problem:** Two students describe a reaction at equilibrium. Student 1: "The reaction has stopped — that's why nothing changes." Student 2: "The reaction is still going both ways at equal rates — that's why nothing changes." Which is correct, and what experiment settles it?

**Solution:**
- *Step 1 — evaluate.* Student 2 is correct: equilibrium is *dynamic*. Concentrations are constant because forward and reverse rates are equal, not because motion stopped.
- *Step 2 — the deciding experiment.* Add an isotope-labeled reactant to a system already at equilibrium. If the label later shows up in the products (without the bulk concentrations changing), molecules must still be converting — proving the reaction never stopped.

**Answer:** Student 2. An isotope-labeling (tracer) experiment settles it: the label migrates into the products, proving conversions continue at equilibrium.

---

**Example 12: Sketching the Curves From a Description**

**Problem:** For $\ce{2A <=> B}$ starting from pure $\ce{A}$, describe the shape of the $[\ce{A}]$ curve and the $[\ce{B}]$ curve versus time, and where they end up relative to each other if the equilibrium mixture is mostly $\ce{A}$.

**Solution:**
- *Step 1 — $[\ce{A}]$ curve.* Starts high, *decreases* (steeply at first, then more gently as the forward rate drops), then goes **flat** at equilibrium.
- *Step 2 — $[\ce{B}]$ curve.* Starts at zero, *increases* (steeply at first as product forms, then leveling), then goes **flat** at equilibrium.
- *Step 3 — final heights.* Both flatten at the same time $t_{eq}$. Since the mixture is "mostly $\ce{A}$," the flat $[\ce{A}]$ line sits **higher** than the flat $[\ce{B}]$ line.

**Answer:** $[\ce{A}]$ falls then flattens; $[\ce{B}]$ rises then flattens; they level off at the same time but at different heights, with $[\ce{A}]$ higher (reactant-favored). Constant, not equal.

---

## Common Mistakes

| The mistake | Why it happens | How to avoid it |
|---|---|---|
| **"Equal rates" → "equal concentrations"** | The word "equilibrium" *sounds* like "equal amounts" | Equilibrium means forward **rate** = reverse **rate**. Concentrations become *constant*, essentially never *equal*. Repeat it until it's reflex. |
| **Thinking the reaction stopped** | Nothing visible changes, so it looks dead | Equilibrium is **dynamic** — both reactions run full speed, just matched. The isotope experiment proves molecules keep converting. |
| **Saying reactants get "used up"** | Habit from single-arrow, go-to-completion reactions | At equilibrium there's always reactant *and* product present. Nothing runs out. |
| **Reverse rate starts high** | Students mirror the forward rate | Starting from pure reactants, the reverse rate begins at **zero** (no product exists yet) and *rises*. |
| **Forgetting the closed-system requirement** | Everyday reactions often lose gas or product to the surroundings | Equilibrium needs a closed system at constant temperature. An open container lets product escape, so the reaction runs to completion instead. |
| **Thinking start-side matters** | Feels like starting with products should give a different end | Same $T$, same closed system, equivalent atoms → identical equilibrium either way. Equilibrium is a destination. |
| **Confusing macroscopic and particulate** | Both describe "the same flask" | Macroscopic = bulk properties (color, pressure) → constant. Particulate = individual molecules → constantly reacting. Both true at once. |

---

## AP Exam Tips

- **"Equal rates, NOT equal concentrations" is a guaranteed trap.** Every exam includes at least one item that rewards knowing equilibrium means matched forward/reverse *rates*, while concentrations are merely *constant*. If an answer choice says "concentrations of reactants and products are equal," it's almost always the wrong choice.
- **Dynamic, not static — and know the evidence.** Be ready to explain that both reactions continue at equilibrium and to cite the **isotope-labeling** experiment as proof. A common FRQ asks you to justify that equilibrium is dynamic; "the label appears in the products without the concentrations changing" earns the point.
- **Read approach-to-equilibrium graphs fluently.** Given concentration-vs-time curves, equilibrium is where the curves **go flat** (stop changing). Given rate-vs-time curves, equilibrium is where the falling forward-rate curve **meets** the rising reverse-rate curve. Don't say equilibrium is where the curves *cross zero* — the rates are equal and *nonzero*.
- **Particulate representations show up every year.** You'll be asked to pick the box that represents equilibrium, or to compare two boxes. Look for *unchanging counts* between successive snapshots — and remember the winning box need not have equal numbers of reactant and product particles.
- **Equilibrium is reachable from either direction.** If a question starts one flask with reactants and another with products (at the same $T$), the equilibrium mixtures are identical. Don't be fooled into thinking the starting side changes the destination.
- **Watch for the closed-system / constant-temperature setup.** If a prompt describes an open container or a gas escaping, the reaction won't sit at equilibrium — it'll run to completion. Constant temperature is also assumed; changing $T$ moves the balance point itself (a Unit 7 topic still to come).

---

## Practice Problems

### Problem 1
Explain in one or two sentences why the reaction $\ce{H2 + I2 <=> 2HI}$ is written with a double arrow instead of a single arrow.

<details>
<summary><strong>Solution</strong></summary>

The reaction is reversible: as $\ce{HI}$ builds up, it reacts back into $\ce{H2}$ and $\ce{I2}$. So the reaction doesn't go to completion — it settles into a mixture of all three species at equilibrium. The double arrow $\ce{<=>}$ signals that both the forward and reverse reactions occur.

**Answer:** Because it's reversible and reaches equilibrium (both reactants and products remain), not completion.

</details>

---

### Problem 2
A reaction at equilibrium has $[\text{reactant}] = 0.90\ \text{M}$ and $[\text{product}] = 0.10\ \text{M}$, both constant. A classmate insists it can't be at equilibrium because the concentrations aren't equal. Are they right?

<details>
<summary><strong>Solution</strong></summary>

No. Equilibrium requires the forward and reverse *rates* to be equal, which makes the concentrations *constant* — it does **not** require the concentrations themselves to be equal. Constant, unequal concentrations (0.90 and 0.10) are perfectly consistent with equilibrium; this mixture simply favors the reactant.

**Answer:** The classmate is wrong. Equal *rates*, not equal *concentrations*, define equilibrium.

</details>

---

### Problem 3
Starting from pure reactants, describe what happens to (a) the forward rate and (b) the reverse rate from $t = 0$ until equilibrium.

<details>
<summary><strong>Solution</strong></summary>

(a) The forward rate starts at its maximum (reactant concentration is highest) and **decreases** as reactant is consumed.

(b) The reverse rate starts at **zero** (no product exists yet) and **increases** as product builds up.

They meet at equilibrium and stay equal (and nonzero) thereafter.

**Answer:** Forward rate falls from a maximum; reverse rate rises from zero; they become equal at equilibrium.

</details>

---

### Problem 4
For $\ce{A <=> B}$ (pure $\ce{A}$ at start), the data below are recorded. At what time is equilibrium first reached?

| Time (s) | $[\ce{A}]$ (M) | $[\ce{B}]$ (M) |
|---|---|---|
| 0 | 0.80 | 0.00 |
| 30 | 0.60 | 0.20 |
| 60 | 0.48 | 0.32 |
| 90 | 0.45 | 0.35 |
| 120 | 0.45 | 0.35 |
| 150 | 0.45 | 0.35 |

<details>
<summary><strong>Solution</strong></summary>

Track when the concentrations stop changing. They're still moving through $t = 60$, but from $t = 90$ onward both hold at $0.45$ and $0.35$.

**Answer:** Equilibrium is first reached at $t = 90\ \text{s}$. (Note the concentrations are constant but *not* equal — reactant-favored.)

</details>

---

### Problem 5
At equilibrium, is a reaction still occurring? Justify your answer and name an experiment that supports it.

<details>
<summary><strong>Solution</strong></summary>

Yes. Equilibrium is *dynamic*: the forward and reverse reactions both continue, at equal rates, so the net change is zero even though molecules keep converting. An **isotope-labeling** experiment supports this — adding a labeled reactant to a system at equilibrium causes the label to appear in the products over time, even though the bulk concentrations never change, proving conversions continue.

**Answer:** Yes, it's dynamic; the isotope-tracer experiment (label migrates into products) is the evidence.

</details>

---

### Problem 6
List three macroscopic properties that stay constant at equilibrium, and state what is happening at the particle (particulate) level meanwhile.

<details>
<summary><strong>Solution</strong></summary>

Macroscopic constants (any three): color intensity, total pressure, concentration of each species, pH, density, mass. Meanwhile, at the particle level, individual molecules are continuously reacting in both directions — reactants forming products and products reforming reactants — at equal rates.

**Answer:** Constant: e.g., color, pressure, concentration. Particulate: molecules keep converting both ways at matched rates (dynamic).

</details>

---

### Problem 7
For $\ce{A2 <=> 2A}$, a particulate box at equilibrium shows 3 $\ce{A2}$ molecules and 10 $\ce{A}$ atoms. Which reaction (forward or reverse) does this equilibrium favor, and are the counts changing?

<details>
<summary><strong>Solution</strong></summary>

There's far more product ($\ce{A}$, count 10) than reactant ($\ce{A2}$, count 3), so the equilibrium **favors the products** (the forward reaction). Because it's at equilibrium, the totals (3 and 10) stay constant — but individual $\ce{A2}$ molecules keep splitting and $\ce{A}$ atoms keep recombining at equal rates.

**Answer:** Favors products (forward); the counts are constant, though molecules keep converting.

</details>

---

### Problem 8
Two identical sealed flasks at the same temperature run $\ce{N2O4 <=> 2NO2}$. Flask A starts with pure $\ce{N2O4}$; flask B starts with pure $\ce{NO2}$ (equivalent amount of nitrogen and oxygen atoms). Compare their final equilibrium mixtures.

<details>
<summary><strong>Solution</strong></summary>

Flask A can only go forward at first ($\ce{N2O4}$ decomposing to $\ce{NO2}$); flask B can only go reverse at first ($\ce{NO2}$ combining to $\ce{N2O4}$). Since it's the same reaction, same temperature, same closed system, and the same total atoms, both reach the **identical** equilibrium concentrations — just approached from opposite directions.

**Answer:** The two flasks end at the same equilibrium mixture; equilibrium is reachable from either direction.

</details>

---

### Problem 9
Explain why a cup of soda left open on the counter eventually goes completely flat, in terms of the conditions required for equilibrium.

<details>
<summary><strong>Solution</strong></summary>

Equilibrium $\ce{CO2(aq) <=> CO2(g)}$ requires a **closed system**. An open cup isn't closed: $\ce{CO2}$ gas escapes into the room and can't redissolve, starving the reverse reaction. So the forward reaction (dissolved → gas) keeps winning until essentially all the dissolved $\ce{CO2}$ has left — the soda goes flat instead of reaching equilibrium.

**Answer:** It's an open (non-closed) system, so escaping $\ce{CO2}$ can't return; the reaction runs to completion (flat) rather than balancing.

</details>

---

### Problem 10
On a rate-vs-time graph for a reaction starting from pure reactants, one curve starts high and falls while another starts at zero and rises. Where on the graph is equilibrium, and are the rates zero there?

<details>
<summary><strong>Solution</strong></summary>

The falling curve is the forward rate; the rising curve is the reverse rate. Equilibrium is where the two curves **meet and then run together** — the point where forward rate = reverse rate. The rates are **not** zero there; they're equal and nonzero (both reactions still running).

**Answer:** Equilibrium is where the two rate curves meet and stay equal; the rates are equal and nonzero, not zero.

</details>

---

### Problem 11
A student writes: "At equilibrium, the reaction stops and the reactants are all used up." Identify every error and rewrite the sentence correctly.

<details>
<summary><strong>Solution</strong></summary>

Errors: (1) the reaction does **not** stop — it's dynamic, running both ways at equal rates; (2) the reactants are **not** all used up — reactant and product both remain present at constant concentrations.

Corrected: "At equilibrium, the forward and reverse reactions continue at equal rates, so the concentrations of both reactants and products stay constant (and neither is fully used up)."

**Answer:** Both claims are wrong; see corrected sentence above.

</details>

---

### Problem 12
For $\ce{2SO2 + O2 <=> 2SO3}$ in a sealed rigid container at constant temperature, the total pressure is measured over time. What will the pressure reading look like as the system approaches and then reaches equilibrium, and what does a constant reading indicate at the particle level?

<details>
<summary><strong>Solution</strong></summary>

As the reaction proceeds, the moles of gas change (3 mol reactant gas → 2 mol product gas per reaction), so the pressure shifts over time — then **levels off and stays constant** once equilibrium is reached. A constant pressure macroscopically corresponds to equal forward and reverse rates; at the particle level, $\ce{SO2}$ and $\ce{O2}$ are still combining into $\ce{SO3}$ while $\ce{SO3}$ is still decomposing, at matched rates.

**Answer:** Pressure changes, then goes flat at equilibrium; the constant reading means equal forward/reverse rates while molecules keep converting (dynamic).

</details>

---

### Problem 13
For $\ce{X <=> Y}$, two particulate snapshots of the same flask are taken. Snapshot 1 ($t = 40\ \text{s}$): 7 $\ce{X}$, 5 $\ce{Y}$. Snapshot 2 ($t = 55\ \text{s}$): 6 $\ce{X}$, 6 $\ce{Y}$. Has equilibrium been reached by $t = 40\ \text{s}$? Explain.

<details>
<summary><strong>Solution</strong></summary>

No. The counts changed between the two snapshots (7 $\ce{X}$/5 $\ce{Y}$ → 6 $\ce{X}$/6 $\ce{Y}$), which means the concentrations were still changing during that interval. Equilibrium requires the counts to stop changing between successive snapshots.

**Answer:** No — the composition changed from $t = 40$ to $t = 55\ \text{s}$, so it was not yet at equilibrium at $t = 40\ \text{s}$.

</details>

---

### Problem 14
Using the treadmill analogy, explain (a) what corresponds to reaching equilibrium and (b) why "reaching equilibrium" doesn't tell you whether there's more reactant or more product.

<details>
<summary><strong>Solution</strong></summary>

(a) Reaching equilibrium corresponds to the moment the belt speed matches your running speed, so you stop drifting and hold one spot on the machine — your position (the concentrations) stops changing while you keep running (both reactions keep going).

(b) Holding a spot tells you only that the two speeds are *equal*; you could be locked in place near the front or near the back of the belt. Likewise, equal rates tell you concentrations are constant but say nothing about whether reactant or product dominates — that depends on *where* the balance happens to lock in.

**Answer:** (a) Belt speed = run speed → position (concentration) frozen while both keep moving. (b) Equal speeds fix that you've stopped drifting, not *where* you stopped — so equilibrium fixes equal rates, not the reactant/product ratio.

</details>

---

### Problem 15
Sketch (in words) the concentration-vs-time curves for $\ce{A <=> 2B}$ starting from pure $\ce{A}$, if the final mixture is product-favored. State what's true of the two curves at the moment equilibrium is reached.

<details>
<summary><strong>Solution</strong></summary>

$[\ce{A}]$ starts at its maximum and **decreases** (steeply at first, then leveling), going flat at equilibrium. $[\ce{B}]$ starts at zero and **increases** (steeply at first, then leveling), going flat at equilibrium. Because the mixture is product-favored, the flat $[\ce{B}]$ line sits **higher** than the flat $[\ce{A}]$ line. At the moment equilibrium is reached, both curves simultaneously **stop changing (go flat)** — that shared flattening *is* equilibrium — even though they level off at different heights.

**Answer:** $[\ce{A}]$ falls then flattens; $[\ce{B}]$ rises then flattens (higher, since product-favored); at equilibrium both curves go flat at the same time but at different heights.

</details>

---

## Quick Reference

| Concept | Key idea |
|---|---|
| Reversible reaction | Runs both ways; written with $\ce{<=>}$; reaches equilibrium, not completion |
| Dynamic equilibrium | $\text{rate}_{\text{forward}} = \text{rate}_{\text{reverse}}$; concentrations constant; both reactions still running |
| **Equal rates, NOT equal concentrations** | The #1 trap — rates match, amounts merely stop changing (rarely equal) |
| Approach from pure reactants | Forward rate: high → falls; reverse rate: 0 → rises; they meet at equilibrium |
| Concentration-vs-time | Curves flatten at $t_{eq}$ (same time, generally different heights) |
| Rate-vs-time | Equilibrium where forward and reverse curves meet — equal and **nonzero** |
| Macroscopic view | Bulk properties (color, pressure, concentration) are **constant** |
| Particulate view | Individual molecules keep converting both ways — **never still** |
| Evidence it's dynamic | Isotope-labeling: label migrates into products with no bulk change |
| Conditions | **Closed system** + **constant temperature** |
| Either direction | Same $T$ + same atoms → identical equilibrium from reactants OR products |
| Everyday examples | Sealed soda $\ce{CO2(aq) <=> CO2(g)}$; sweat $\ce{H2O(l) <=> H2O(g)}$; $\ce{N2O4 <=> 2NO2}$ color |

---

<div align="center">

[← Hess's Law](/chemistry/0806-hess-law) | [The Equilibrium Constant →](/chemistry/0902-equilibrium-constant)

</div>
