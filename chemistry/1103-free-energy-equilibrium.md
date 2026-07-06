# Free Energy and Equilibrium
<p class="article-date">July 5, 2026</p>

*The best part of any roller coaster is the very first hill — that slow, clanking climb followed by the stomach-dropping plunge. But have you ever noticed that after the big drop, the coaster hauls itself right back up and over a second hill, then a third, then a corkscrew, all without an engine anywhere on the track? There's no motor pulling the cars up hill number two. So where does the "oomph" come from? It comes from that first giant drop. The coaster banks so much speed on the way down that it can spend it climbing the next hill — as long as the next hill is shorter than the drop it just took. Chemistry runs on the exact same trick. A reaction that badly *wants* to happen (a big energetic drop, a very negative $\Delta G$) can be hooked to a reaction that would *never* happen on its own (an uphill climb, a positive $\Delta G$) and drag it along for the ride. That's a **coupled reaction**, and it's literally how every cell in your body uses ATP to build things that would never build themselves. This article is where all of Unit 9 clicks together: $\Delta G$, $K$, and $Q$ turn out to be three views of the same coaster.*

---

## What You'll Learn

- Connect free energy to the equilibrium constant with the AP formula $\ce{\Delta G^\circ = -RT ln K}$
- Predict whether $K > 1$, $K < 1$, or $K = 1$ just from the **sign** of $\Delta G^\circ$
- Calculate $K$ from $\Delta G^\circ$ **and** calculate $\Delta G^\circ$ from $K$ (both directions), using $R = 8.314\ \text{J/(mol·K)}$ with correct units
- Distinguish $\Delta G^\circ$ (standard conditions) from $\Delta G$ (actual, right-now conditions) using $\ce{\Delta G = \Delta G^\circ + RT ln Q}$
- Compute $\Delta G$ under **nonstandard** conditions and predict which way a reaction runs by comparing $Q$ to $K$
- Explain why a "favorable" reaction ($\Delta G^\circ < 0$) still settles at equilibrium instead of going 100% to completion
- Add reactions and their $\Delta G$ values (Hess's law style) to build **coupled reactions** that make an unfavorable step happen
- Analyze real coupled systems — ore reduction in metallurgy and ATP driving biosynthesis
- Assemble the whole unit: how $\Delta H$, $\Delta S$, $T$, $\Delta G$, $Q$, and $K$ all interlock

---

## Prerequisites

- [Gibbs Free Energy](/chemistry/1102-gibbs-free-energy) — you must already be comfortable with $\ce{\Delta G = \Delta H - T\Delta S}$, that $\Delta G < 0$ means a reaction is thermodynamically favorable, and what the little $^\circ$ (standard conditions) means. This article takes that same $\Delta G$ and ties it to a number you already know.
- [The Equilibrium Constant](/chemistry/0902-equilibrium-constant) — you need to know what $K$ is (the products-over-reactants ratio a reaction settles into), what the reaction quotient $Q$ is (the same ratio *right now*, before equilibrium), and that comparing $Q$ to $K$ tells you which direction a reaction shifts. Free energy and $K$ turn out to be the same story told two ways.

---

## The Core Concept

### Intuition First

Let's stay on the coaster, because every piece of this topic is riding on that track.

**The big drop is a favorable reaction.** A reaction with a very negative $\Delta G^\circ$ is like the first towering hill — it releases a huge amount of usable "oomph" as the cars plunge. The more negative $\Delta G^\circ$ is, the taller the drop, and the more energy the reaction has to spend on whatever comes next.

**How far the coaster ends up is $K$.** Here's the beautiful part. The *size* of that first drop decides how far the whole ride gets — and in chemistry, "how far the reaction gets" is exactly what $K$ measures. A big drop (very negative $\Delta G^\circ$) means the reaction rolls way over to the products side: a **large $K$**. A tiny drop, or an uphill start (positive $\Delta G^\circ$), means the ride barely moves off the reactant side: a **small $K$**. The link between the drop and the distance is one clean equation:

$$\ce{\Delta G^\circ = -RT ln K}$$

Read the signs straight off the coaster:

- **Big drop** → $\Delta G^\circ < 0$ → $\ln K > 0$ → **$K > 1$**, products favored.
- **Uphill** → $\Delta G^\circ > 0$ → $\ln K < 0$ → **$K < 1$**, reactants favored.
- **Flat track** → $\Delta G^\circ = 0$ → $\ln K = 0$ → **$K = 1$**, an even split.

**$\Delta G$ vs. $\Delta G^\circ$ is "how much oomph is left *right now*."** The standard drop $\Delta G^\circ$ is a fixed property of the ride — it's the full drop measured from a standard starting height. But the actual push you feel, $\Delta G$, depends on where the cars are *at this instant* on the track. As the coaster rolls toward its resting point, it has less and less push left. That "where are we right now" information is carried by $Q$:

$$\ce{\Delta G = \Delta G^\circ + RT ln Q}$$

When the cars finally come to rest — equilibrium — there's no push left in either direction. $\Delta G = 0$, and $Q$ has become $K$. (Set $\Delta G = 0$ and $Q = K$ in that equation and you *derive* the first one. They're the same track.)

**Coupling is hooking two cars on one track.** Now the headline trick. Take a reaction that's an uphill climb by itself (positive $\Delta G$) — on its own it just won't go. Bolt it onto a reaction with a giant drop (very negative $\Delta G$) so they share the same track, and the drop drags the climb along. The whole train makes it over the hill **as long as the drop is bigger than the climb** — that is, as long as the *sum* of the two $\Delta G$ values is still negative. Linking reactions on one track = **adding the reactions**, and their $\Delta G$ values **add right along with them**. That's just Hess's law from [Hess's Law](/chemistry/0806-hess-law), now applied to $\Delta G$.

Carry this coaster all the way through the article: **drop = favorable reaction, hill = unfavorable reaction, hooking cars together = adding reactions and their $\Delta G$'s, and the ride only completes if the total $\Delta G$ stays negative.**

### The Three Key Equations

Two of these are on the AP formula sheet; the third is the definition of $Q$ you already own.

| Equation | What it links | When to use it |
|---|---|---|
| $\ce{\Delta G^\circ = -RT ln K}$ | standard free energy ↔ equilibrium constant | convert between $\Delta G^\circ$ and $K$ |
| $\ce{\Delta G = \Delta G^\circ + RT ln Q}$ | actual free energy at *current* conditions | find the real driving force away from standard state |
| $\Delta G_\text{total} = \sum \Delta G_i$ | coupled reactions | add reactions → add their $\Delta G$'s |

**About $R$ and units.** In these equations $R = 8.314\ \text{J/(mol·K)}$ — the *joule* gas constant, **not** the $0.0821\ \text{L·atm/(mol·K)}$ one from the gas laws. Temperature is always in **kelvin**. And watch the scale: $\Delta G^\circ$ values are usually quoted in **kJ/mol**, but $R$ is in **joules**, so you must convert kJ → J (multiply by 1000) or $R$ → kJ (use $0.008314$) before combining them. Mixing kJ and J is the single most common way to blow this calculation.

**Why $\ln$ and not $\log$?** These formulas use natural log ($\ln$). If a problem hands you a value in $\log_{10}$, convert with $\ln x = 2.303\log x$. On the calculator, the `ln` button is what you want here.

### What the Sign of $\Delta G^\circ$ Really Tells You

$\Delta G^\circ$ answers "which side is favored, and by how much" — it sets the *destination*, $K$. It does **not** tell you how fast you get there (that's kinetics — [Reaction Rates](/chemistry/0701-reaction-rates)). A reaction can have a wildly negative $\Delta G^\circ$ and still crawl. Free energy is about the *finish line*, never the *speed*.

---

## Worked Examples

### Example 1: Find $K$ from $\Delta G^\circ$ (favorable reaction)

**Problem:** At $298\ \text{K}$, a reaction has $\Delta G^\circ = -22.8\ \text{kJ/mol}$. Find $K$.

**Solution:**

**Step 1 — Rearrange** $\ce{\Delta G^\circ = -RT ln K}$ for $\ln K$:
$$\ln K = -\frac{\Delta G^\circ}{RT}$$

**Step 2 — Fix the units.** Convert $\Delta G^\circ$ to joules: $-22.8\ \text{kJ/mol} = -22{,}800\ \text{J/mol}$. Use $R = 8.314\ \text{J/(mol·K)}$, $T = 298\ \text{K}$.

**Step 3 — Plug in:**
$$\ln K = -\frac{-22{,}800}{(8.314)(298)} = \frac{22{,}800}{2477.6} = 9.20$$

**Step 4 — Exponentiate:** $K = e^{9.20} \approx 9.9 \times 10^{3}$.

Big negative drop → $K \gg 1$. The coaster rolled far to the product side, exactly as expected.

**Answer: $K \approx 9.9 \times 10^{3}$ (products strongly favored).**

### Example 2: Find $K$ from $\Delta G^\circ$ (unfavorable reaction)

**Problem:** At $298\ \text{K}$, $\Delta G^\circ = +15.0\ \text{kJ/mol}$. Find $K$.

**Solution:**

$$\ln K = -\frac{\Delta G^\circ}{RT} = -\frac{15{,}000}{(8.314)(298)} = -\frac{15{,}000}{2477.6} = -6.05$$

$$K = e^{-6.05} \approx 2.3 \times 10^{-3}$$

A positive $\Delta G^\circ$ (uphill start) gives $K < 1$ — reactants favored, the ride barely leaves the station.

**Answer: $K \approx 2.3 \times 10^{-3}$ (reactants favored).**

### Example 3: Find $\Delta G^\circ$ from $K$

**Problem:** For a reaction at $298\ \text{K}$, $K = 4.5 \times 10^{6}$. Find $\Delta G^\circ$ in kJ/mol.

**Solution:**

**Step 1 — Use the equation directly:**
$$\Delta G^\circ = -RT\ln K$$

**Step 2 — Compute $\ln K$:** $\ln(4.5 \times 10^{6}) = 15.32$.

**Step 3 — Plug in:**
$$\Delta G^\circ = -(8.314)(298)(15.32) = -37{,}950\ \text{J/mol}$$

**Step 4 — Convert to kJ:** $-37{,}950\ \text{J/mol} = -37.9\ \text{kJ/mol}$.

$K$ was huge, so $\Delta G^\circ$ came out strongly negative — a big drop. Consistent.

**Answer: $\Delta G^\circ \approx -37.9\ \text{kJ/mol}$.**

### Example 4: $K$ near 1 means $\Delta G^\circ$ near 0

**Problem:** A reaction has $K = 1.0$ at $350\ \text{K}$. What is $\Delta G^\circ$?

**Solution:** $\ln(1.0) = 0$, so
$$\Delta G^\circ = -RT\ln K = -(8.314)(350)(0) = 0\ \text{J/mol}$$

A flat track: neither side favored. This is the pivot point — the reason the sign of $\Delta G^\circ$ flips exactly where $K$ crosses 1.

**Answer: $\Delta G^\circ = 0$.**

### Example 5: $\Delta G$ under nonstandard conditions

**Problem:** For $\ce{N2(g) + 3H2(g) <=> 2NH3(g)}$ at $298\ \text{K}$, $\Delta G^\circ = -33.0\ \text{kJ/mol}$. At a moment when $Q = 8.0 \times 10^{2}$, what is the *actual* $\Delta G$?

**Solution:**

**Step 1 — Use** $\ce{\Delta G = \Delta G^\circ + RT ln Q}$.

**Step 2 — Compute $RT\ln Q$** (keep everything in joules): $\ln(8.0 \times 10^{2}) = 6.68$.
$$RT\ln Q = (8.314)(298)(6.68) = +16{,}550\ \text{J/mol} = +16.6\ \text{kJ/mol}$$

**Step 3 — Add:**
$$\Delta G = -33.0 + 16.6 = -16.4\ \text{kJ/mol}$$

**Step 4 — Interpret:** $\Delta G$ is still negative, so the reaction still runs **forward** at this instant — but it has less push left than the full standard drop of $-33.0$, because it's already partway down the track.

**Answer: $\Delta G \approx -16.4\ \text{kJ/mol}$; forward.**

### Example 6: Direction prediction from $Q$ vs. $K$

**Problem:** A reaction has $\Delta G^\circ = -5.0\ \text{kJ/mol}$ at $298\ \text{K}$ (so $K \approx 7.5$). At an instant when $Q = 50$, which way does the reaction run? Confirm with $\Delta G$.

**Solution:**

**Compare directly:** $Q = 50 > K = 7.5$. Too much product — the reaction must run **reverse** to bring $Q$ back down to $K$ (this is the $Q$-vs-$K$ rule from [The Equilibrium Constant](/chemistry/0902-equilibrium-constant)).

**Confirm with $\Delta G$:**
$$\Delta G = \Delta G^\circ + RT\ln Q = -5000 + (8.314)(298)(\ln 50)$$
$$= -5000 + (8.314)(298)(3.91) = -5000 + 9690 = +4690\ \text{J/mol}$$

$\Delta G > 0$ → the forward direction is uphill right now → the reaction runs **reverse**. The two methods agree, as they must: $Q > K$ *is* $\Delta G > 0$.

**Answer: Reverse ($Q > K$, $\Delta G > 0$).**

### Example 7: A favorable reaction that still isn't "complete"

**Problem:** A reaction has $\Delta G^\circ = -8.0\ \text{kJ/mol}$ at $298\ \text{K}$. Is it favorable? What fraction of the way to completion does its $K$ suggest?

**Solution:**

**Favorable?** Yes — $\Delta G^\circ < 0$, a downhill drop.

**But how big is $K$?**
$$\ln K = -\frac{-8000}{(8.314)(298)} = 3.23 \quad\Rightarrow\quad K = e^{3.23} \approx 25$$

$K = 25$ *does* favor products, but it's nowhere near "enormous." At equilibrium there will still be a meaningful amount of reactant left — the reaction settles at a mixture, not at 100% products. A modest drop lands the coaster comfortably on the product side but not slammed against the far wall. Only a *gigantic* $K$ (say $10^{10}$) — which needs a huge negative $\Delta G^\circ$ — corresponds to a reaction that runs essentially to completion.

**Answer: Favorable, but $K \approx 25$ — it reaches an equilibrium mixture, not 100% completion.**

### Example 8: Coupled reactions — is the sum favorable?

**Problem:** Reaction A is unfavorable: $\ce{X -> Y}$, $\Delta G^\circ_A = +20.0\ \text{kJ/mol}$. Reaction B is favorable: $\ce{Z -> W}$, $\Delta G^\circ_B = -35.0\ \text{kJ/mol}$. If they're coupled (added), is the overall process favorable, and what is the total $\Delta G^\circ$?

**Solution:**

**Step 1 — Add the reactions, add the $\Delta G$'s** (Hess's law for free energy):
$$\Delta G^\circ_\text{total} = \Delta G^\circ_A + \Delta G^\circ_B = (+20.0) + (-35.0) = -15.0\ \text{kJ/mol}$$

**Step 2 — Judge:** the drop ($-35.0$) is bigger than the climb ($+20.0$), so the total is negative. The coaster clears the second hill.

**Answer: Yes, favorable overall; $\Delta G^\circ_\text{total} = -15.0\ \text{kJ/mol}$.**

### Example 9: Coupled reactions — the ore-reduction (Dr. Stone) example

**Problem:** Pulling iron out of its ore means running $\ce{Fe2O3(s) -> 2Fe(s) + 3/2 O2(g)}$, which is badly uphill: $\Delta G^\circ = +742\ \text{kJ/mol}$. Iron won't just fall out of the rock. In a blast furnace we couple it to burning carbon monoxide, $\ce{3CO(g) + 3/2 O2(g) -> 3CO2(g)}$, $\Delta G^\circ = -771\ \text{kJ/mol}$. Is the coupled smelting reaction favorable?

**Solution:**

**Step 1 — Add the two reactions.** The $\ce{3/2 O2}$ cancels:
$$\ce{Fe2O3(s) + 3CO(g) -> 2Fe(s) + 3CO2(g)}$$

**Step 2 — Add the free energies:**
$$\Delta G^\circ_\text{total} = (+742) + (-771) = -29\ \text{kJ/mol}$$

**Step 3 — Interpret:** on its own, prying oxygen off iron oxide is a hopeless climb. But $\ce{CO}$'s hunger for that oxygen is an even bigger drop, and hooking them together drags the iron out. This is exactly the reasoning behind smelting iron from scratch — a huge downhill grabs the oxygen and hauls the uphill reduction over the top.

**Answer: Favorable; $\Delta G^\circ_\text{total} = -29\ \text{kJ/mol}$.**

### Example 10: Coupled reactions — ATP driving biosynthesis

**Problem:** Building a bond between two molecules — say gluing glutamate to ammonia to make glutamine — is uphill: $\Delta G^\circ = +14\ \text{kJ/mol}$. Your cells couple it to ATP hydrolysis, $\ce{ATP + H2O -> ADP + Pi}$, $\Delta G^\circ = -31\ \text{kJ/mol}$. Does coupling make the synthesis go?

**Solution:**

**Step 1 — Add the $\Delta G$'s:**
$$\Delta G^\circ_\text{total} = (+14) + (-31) = -17\ \text{kJ/mol}$$

**Step 2 — Interpret:** ATP hydrolysis is the big energetic drop your body keeps "charged up" like a coaster parked at the top of the first hill. Whenever a cell needs to force an uphill reaction — building a protein, pumping ions, contracting a muscle — it releases some ATP-drop to drag that climb along. The synthesis alone would never happen; coupled to ATP, the total is negative and it runs.

**Answer: Yes; $\Delta G^\circ_\text{total} = -17\ \text{kJ/mol}$. This is the universal way life powers unfavorable reactions.**

### Example 11: Coupling that *fails* (drop too small)

**Problem:** An uphill reaction has $\Delta G^\circ = +50.0\ \text{kJ/mol}$. Someone tries to power it by coupling to a reaction with $\Delta G^\circ = -30.0\ \text{kJ/mol}$. Does it work?

**Solution:**
$$\Delta G^\circ_\text{total} = (+50.0) + (-30.0) = +20.0\ \text{kJ/mol}$$

The drop ($-30$) is *smaller* than the climb ($+50$), so the total is still positive — the coaster stalls before it clears the hill. Coupling only works when the favorable drop **outweighs** the unfavorable climb.

**Answer: No — total $\Delta G^\circ = +20.0\ \text{kJ/mol}$, still unfavorable.**

### Example 12: Temperature changes $K$ through $\Delta G^\circ$

**Problem:** An endothermic reaction has $\Delta H^\circ = +40.0\ \text{kJ/mol}$ and $\Delta S^\circ = +150\ \text{J/(mol·K)}$. Find $K$ at $500\ \text{K}$.

**Solution:**

**Step 1 — Find $\Delta G^\circ$** with $\ce{\Delta G^\circ = \Delta H^\circ - T\Delta S^\circ}$ (units in joules):
$$\Delta G^\circ = 40{,}000 - (500)(150) = 40{,}000 - 75{,}000 = -35{,}000\ \text{J/mol}$$

At high $T$, the $-T\Delta S$ term wins and the drop turns negative.

**Step 2 — Convert to $K$:**
$$\ln K = -\frac{-35{,}000}{(8.314)(500)} = \frac{35{,}000}{4157} = 8.42 \quad\Rightarrow\quad K = e^{8.42} \approx 4.5 \times 10^{3}$$

**Answer: $\Delta G^\circ = -35.0\ \text{kJ/mol}$, $K \approx 4.5 \times 10^{3}$.** Raising $T$ turned an uphill reaction into a downhill one — and $K$ jumped past 1.

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Using $R = 0.0821$ | Muscle memory from the gas laws | For free energy, $R = 8.314\ \text{J/(mol·K)}$ — always the *joule* one |
| Mixing kJ and J | $\Delta G^\circ$ is in kJ, $R$ is in J | Convert $\Delta G^\circ$ to J (×1000) **before** dividing by $RT$ |
| Forgetting the minus sign in $\Delta G^\circ = -RT\ln K$ | The negative is easy to drop | Sanity-check signs: $\Delta G^\circ < 0$ must give $K > 1$ |
| Using $\log$ instead of $\ln$ | The formula sheet's $\ln$ looks like $\log$ | These equations use natural log; hit the `ln` key (or convert with $2.303$) |
| Using Celsius for $T$ | Forgetting the kelvin rule | Always $T$ in K: $T(\text{K}) = T(°\text{C}) + 273$ |
| Confusing $\Delta G$ with $\Delta G^\circ$ | They look almost identical | $^\circ$ = standard state; no $^\circ$ = actual current conditions (needs $Q$) |
| Thinking $\Delta G^\circ < 0$ means 100% completion | "Favorable" sounds like "goes all the way" | A modest negative $\Delta G^\circ$ gives a modest $K$ — an equilibrium *mixture* |
| Multiplying $\Delta G$'s when coupling | Confusing $\Delta G$ rules with $K$ rules | Coupled reactions **add** $\Delta G$ (Hess), but the $K$'s **multiply** |

---

## AP Exam Tips

- **Know both formula-sheet equations cold.** $\ce{\Delta G^\circ = -RT ln K}$ and $\ce{\Delta G = \Delta G^\circ + RT ln Q}$ are provided, but you must know *when* to use each. Standard, connecting to $K$? First one. Nonstandard, right-now push? Second one.
- **Sign of $\Delta G^\circ$ ↔ size of $K$.** This is a guaranteed conceptual point: $\Delta G^\circ < 0 \Rightarrow K > 1$ (products favored); $\Delta G^\circ > 0 \Rightarrow K < 1$; $\Delta G^\circ = 0 \Rightarrow K = 1$. You can often answer without any calculation.
- **At equilibrium, $\Delta G = 0$ and $Q = K$.** A classic free-response line. Plugging these into $\Delta G = \Delta G^\circ + RT\ln Q$ *derives* $\Delta G^\circ = -RT\ln K$ — graders love seeing you know they're the same relationship.
- **$Q$ vs. $K$ = sign of $\Delta G$.** $Q < K \Rightarrow \Delta G < 0 \Rightarrow$ forward; $Q > K \Rightarrow \Delta G > 0 \Rightarrow$ reverse. Two languages, one prediction.
- **Units, units, units.** $R = 8.314\ \text{J/(mol·K)}$, $T$ in kelvin, and convert kJ ↔ J. Watch that you use $\ln$, not $\log$. Most lost points here are unit slips, not concept errors.
- **Coupled reactions add $\Delta G$ (Hess-style).** If asked whether a nonspontaneous step can be driven, add its $\Delta G$ to a favorable partner's and check the sign of the sum. The favorable drop must **outweigh** the unfavorable climb.
- **Favorable ≠ complete.** If a reaction is favorable but you're asked why it doesn't go 100%, the answer is that $K$ isn't infinite — it's finite, so the reaction settles at an equilibrium mixture. Only an *enormous* $K$ (very large negative $\Delta G^\circ$) means near-complete.

---

## Practice Problems

### Problem 1
At $298\ \text{K}$, a reaction has $\Delta G^\circ = -18.0\ \text{kJ/mol}$. Find $K$.

<details>
<summary><strong>Solution</strong></summary>

$$\ln K = -\frac{\Delta G^\circ}{RT} = -\frac{-18{,}000}{(8.314)(298)} = \frac{18{,}000}{2477.6} = 7.27$$
$$K = e^{7.27} \approx 1.4 \times 10^{3}$$

**Answer: $K \approx 1.4 \times 10^{3}$ (products favored).**

</details>

---

### Problem 2
At $298\ \text{K}$, a reaction has $\Delta G^\circ = +12.5\ \text{kJ/mol}$. Find $K$ and state which side is favored.

<details>
<summary><strong>Solution</strong></summary>

$$\ln K = -\frac{12{,}500}{(8.314)(298)} = -5.04 \quad\Rightarrow\quad K = e^{-5.04} \approx 6.5 \times 10^{-3}$$

Positive $\Delta G^\circ$ → $K < 1$.

**Answer: $K \approx 6.5 \times 10^{-3}$; reactants favored.**

</details>

---

### Problem 3
A reaction has $K = 3.2 \times 10^{4}$ at $298\ \text{K}$. Find $\Delta G^\circ$ in kJ/mol.

<details>
<summary><strong>Solution</strong></summary>

$$\ln(3.2 \times 10^{4}) = 10.37$$
$$\Delta G^\circ = -RT\ln K = -(8.314)(298)(10.37) = -25{,}700\ \text{J/mol}$$

**Answer: $\Delta G^\circ \approx -25.7\ \text{kJ/mol}$.**

</details>

---

### Problem 4
A reaction has $K = 5.0 \times 10^{-8}$ at $298\ \text{K}$. Find $\Delta G^\circ$ and comment on the sign.

<details>
<summary><strong>Solution</strong></summary>

$$\ln(5.0 \times 10^{-8}) = -16.81$$
$$\Delta G^\circ = -(8.314)(298)(-16.81) = +41{,}650\ \text{J/mol} \approx +41.6\ \text{kJ/mol}$$

A very small $K$ (well below 1) gives a positive $\Delta G^\circ$ — an uphill reaction, reactants strongly favored.

**Answer: $\Delta G^\circ \approx +41.6\ \text{kJ/mol}$ (positive, as expected for $K \ll 1$).**

</details>

---

### Problem 5
Without a calculator: a reaction has $\Delta G^\circ = +3.0\ \text{kJ/mol}$. Is $K$ greater than, less than, or equal to 1?

<details>
<summary><strong>Solution</strong></summary>

$\Delta G^\circ > 0$ means $\ln K < 0$, so $K < 1$. No arithmetic needed — the sign is enough.

**Answer: $K < 1$ (reactants favored).**

</details>

---

### Problem 6
For $\ce{2SO2(g) + O2(g) <=> 2SO3(g)}$ at $298\ \text{K}$, $\Delta G^\circ = -142\ \text{kJ/mol}$. At a moment when $Q = 1.0 \times 10^{20}$, find $\Delta G$ and state the direction.

<details>
<summary><strong>Solution</strong></summary>

$$\ln(1.0 \times 10^{20}) = 46.05$$
$$RT\ln Q = (8.314)(298)(46.05) = +114{,}100\ \text{J/mol} = +114.1\ \text{kJ/mol}$$
$$\Delta G = -142 + 114.1 = -27.9\ \text{kJ/mol}$$

Still negative → forward, but much weaker push than the standard drop because $Q$ is already large (close to $K$).

**Answer: $\Delta G \approx -27.9\ \text{kJ/mol}$; forward.**

</details>

---

### Problem 7
A reaction has $\Delta G^\circ = +6.0\ \text{kJ/mol}$ at $298\ \text{K}$. At an instant when $Q = 0.010$, find $\Delta G$ and predict the direction.

<details>
<summary><strong>Solution</strong></summary>

$$\ln(0.010) = -4.61$$
$$RT\ln Q = (8.314)(298)(-4.61) = -11{,}420\ \text{J/mol} = -11.4\ \text{kJ/mol}$$
$$\Delta G = +6.0 + (-11.4) = -5.4\ \text{kJ/mol}$$

Even though $\Delta G^\circ$ is positive, the tiny $Q$ (very little product) makes the *actual* $\Delta G$ negative — so at this instant the reaction runs **forward**. This is the power of $Q$: current conditions can flip the driving force.

**Answer: $\Delta G \approx -5.4\ \text{kJ/mol}$; forward.**

</details>

---

### Problem 8
A reaction at $298\ \text{K}$ has $K = 20$ (so $Q$ can be compared to it). At an instant $Q = 200$. Use $Q$ vs. $K$ to predict direction, then confirm with the sign of $\Delta G$.

<details>
<summary><strong>Solution</strong></summary>

$Q = 200 > K = 20$ → too much product → runs **reverse**.

Confirm: $\Delta G^\circ = -RT\ln K = -(8.314)(298)(\ln 20) = -7420\ \text{J/mol}$.
$$\Delta G = -7420 + (8.314)(298)(\ln 200) = -7420 + 13{,}130 = +5710\ \text{J/mol} > 0$$

$\Delta G > 0$ confirms reverse.

**Answer: Reverse ($Q > K$, $\Delta G > 0$).**

</details>

---

### Problem 9
Reaction A: $\Delta G^\circ = +25.0\ \text{kJ/mol}$. Reaction B: $\Delta G^\circ = -40.0\ \text{kJ/mol}$. If coupled, is the overall reaction favorable? Give the total.

<details>
<summary><strong>Solution</strong></summary>

$$\Delta G^\circ_\text{total} = (+25.0) + (-40.0) = -15.0\ \text{kJ/mol}$$

The drop outweighs the climb, so the sum is negative.

**Answer: Favorable; $\Delta G^\circ_\text{total} = -15.0\ \text{kJ/mol}$.**

</details>

---

### Problem 10
Reducing copper oxide, $\ce{2Cu2O(s) -> 4Cu(s) + O2(g)}$, has $\Delta G^\circ = +291\ \text{kJ/mol}$. Coupling with $\ce{2CO(g) + O2(g) -> 2CO2(g)}$, $\Delta G^\circ = -257\ \text{kJ/mol}$. Add the reactions and decide if smelting copper this way is favorable.

<details>
<summary><strong>Solution</strong></summary>

Adding (the $\ce{O2}$ cancels): $\ce{2Cu2O(s) + 2CO(g) -> 4Cu(s) + 2CO2(g)}$.
$$\Delta G^\circ_\text{total} = (+291) + (-257) = +34\ \text{kJ/mol}$$

The $\ce{CO}$ drop is *not quite* big enough to overcome the copper-oxide climb at these standard values, so the coupled reaction is slightly **unfavorable** as written (in a real furnace, high temperature and nonstandard $Q$ push it over — but by these numbers alone it stalls).

**Answer: Not favorable as written; $\Delta G^\circ_\text{total} = +34\ \text{kJ/mol}$.**

</details>

---

### Problem 11
A biosynthesis step has $\Delta G^\circ = +23\ \text{kJ/mol}$. How many ATP hydrolysis reactions ($-31\ \text{kJ/mol}$ each) must be coupled to make the overall process favorable?

<details>
<summary><strong>Solution</strong></summary>

One ATP: $23 + (-31) = -8\ \text{kJ/mol}$ — already negative.

**Answer: One ATP hydrolysis is enough; total $\Delta G^\circ = -8\ \text{kJ/mol}$.**

</details>

---

### Problem 12
A reaction has $\Delta G^\circ = -6.0\ \text{kJ/mol}$ at $298\ \text{K}$. A student claims it will go 100% to completion because it's favorable. Compute $K$ and explain why they're wrong.

<details>
<summary><strong>Solution</strong></summary>

$$\ln K = -\frac{-6000}{(8.314)(298)} = 2.42 \quad\Rightarrow\quad K = e^{2.42} \approx 11$$

$K = 11$ favors products but is far from enormous — at equilibrium a real amount of reactant remains. Favorable means "products win the tug-of-war," not "reactant vanishes." Only a huge negative $\Delta G^\circ$ (giving $K$ like $10^{10}$) means near-complete.

**Answer: $K \approx 11$; the reaction reaches an equilibrium mixture, not 100% completion.**

</details>

---

### Problem 13
An endothermic reaction has $\Delta H^\circ = +60.0\ \text{kJ/mol}$ and $\Delta S^\circ = +200\ \text{J/(mol·K)}$. Find $\Delta G^\circ$ and $K$ at $400\ \text{K}$.

<details>
<summary><strong>Solution</strong></summary>

$$\Delta G^\circ = 60{,}000 - (400)(200) = 60{,}000 - 80{,}000 = -20{,}000\ \text{J/mol}$$
$$\ln K = -\frac{-20{,}000}{(8.314)(400)} = \frac{20{,}000}{3325.6} = 6.01 \quad\Rightarrow\quad K = e^{6.01} \approx 4.1 \times 10^{2}$$

**Answer: $\Delta G^\circ = -20.0\ \text{kJ/mol}$, $K \approx 4.1 \times 10^{2}$.**

</details>

---

### Problem 14
The same reaction from Problem 13 ($\Delta H^\circ = +60.0\ \text{kJ/mol}$, $\Delta S^\circ = +200\ \text{J/(mol·K)}$) — find $K$ at $200\ \text{K}$ instead. What happened to $K$, and why?

<details>
<summary><strong>Solution</strong></summary>

$$\Delta G^\circ = 60{,}000 - (200)(200) = 60{,}000 - 40{,}000 = +20{,}000\ \text{J/mol}$$
$$\ln K = -\frac{20{,}000}{(8.314)(200)} = -12.03 \quad\Rightarrow\quad K = e^{-12.03} \approx 6.0 \times 10^{-6}$$

At the lower temperature the $-T\Delta S$ term shrinks, so $\Delta G^\circ$ is now positive and $K$ collapses to far below 1. For an endothermic, entropy-driven reaction, cooling turns the drop back into a climb.

**Answer: $K \approx 6.0 \times 10^{-6}$ — tiny, because at low $T$ this reaction becomes unfavorable.**

</details>

---

### Problem 15
At equilibrium, $\Delta G = 0$ and $Q = K$. Starting from $\ce{\Delta G = \Delta G^\circ + RT ln Q}$, derive $\ce{\Delta G^\circ = -RT ln K}$.

<details>
<summary><strong>Solution</strong></summary>

At equilibrium substitute $\Delta G = 0$ and $Q = K$:
$$0 = \Delta G^\circ + RT\ln K$$
Solve for $\Delta G^\circ$:
$$\Delta G^\circ = -RT\ln K$$

The two formula-sheet equations are the same relationship — one is just the other evaluated at the resting point.

**Answer: $\Delta G^\circ = -RT\ln K$, exactly as required.**

</details>

---

## Quick Reference

**Core equations**

| Equation | Use |
|---|---|
| $\ce{\Delta G^\circ = -RT ln K}$ | convert between $\Delta G^\circ$ and $K$ |
| $\ce{\Delta G = \Delta G^\circ + RT ln Q}$ | actual driving force at current conditions |
| $\Delta G^\circ = \Delta H^\circ - T\Delta S^\circ$ | build $\Delta G^\circ$ from enthalpy & entropy |
| $\Delta G_\text{total} = \sum \Delta G_i$ | coupled reactions (add reactions → add $\Delta G$) |

**Sign map**

| $\Delta G^\circ$ | $\ln K$ | $K$ | Favored |
|---|---|---|---|
| $< 0$ | $> 0$ | $> 1$ | products |
| $= 0$ | $= 0$ | $= 1$ | neither |
| $> 0$ | $< 0$ | $< 1$ | reactants |

**Direction (right now)**

| Compare | $\Delta G$ | Runs |
|---|---|---|
| $Q < K$ | $< 0$ | forward |
| $Q = K$ | $= 0$ | at equilibrium |
| $Q > K$ | $> 0$ | reverse |

**The whole unit, interlocked**

| Quantity | Question it answers | Sign/size that's "good for products" |
|---|---|---|
| $\Delta H^\circ$ | heat released or absorbed? | negative (exothermic) helps |
| $\Delta S^\circ$ | disorder up or down? | positive (more disorder) helps |
| $T$ | how much does entropy count? | tilts $-T\Delta S$; sets which term wins |
| $\Delta G^\circ$ | favorable at standard state? | negative → favorable |
| $K$ | how far does it go? | large ($> 1$) → products |
| $Q$ | where is it right now? | compare to $K$ for direction |
| $\Delta G$ | push at this instant? | negative → forward |

**Constants:** $R = 8.314\ \text{J/(mol·K)}$; $T$ in kelvin; convert kJ ↔ J; use $\ln$, not $\log$.

---

<div align="center">

[← Gibbs Free Energy](/chemistry/1102-gibbs-free-energy) | [Electrochemical Cells →](/chemistry/1104-electrochemical-cells)

</div>
