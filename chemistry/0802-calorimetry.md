# Calorimetry and Specific Heat
<p class="article-date">July 5, 2026</p>

*Last week we drove up to Torrey Pines and got there around noon, and by 2pm the beach had split into two completely different worlds. The dry sand up by the trail was a foot-scorching griddle — I did the little hopping run to the water that everyone does, towel-to-towel, hissing the whole way. But the second my feet hit the ocean, it was still cold enough to make me gasp. Same sun. Same afternoon. Same hours of light pouring straight down on both the sand and the water, side by side. So why is one a frying pan and the other a refrigerator? The answer is a single number called **specific heat**, and it measures how *stubborn* a material's temperature is — how much energy you have to pump in to warm one gram by one degree. Water is famously, ridiculously stubborn: it drinks up a huge amount of sunlight for only a tiny temperature rise. Sand barely resists at all, so the same sunlight sends its temperature rocketing. It's the same reason coastal San Diego never bakes like the inland desert — the ocean sitting off our coast is a giant heat sponge, soaking up warmth all day and barely changing temperature. This whole article is about that number, $c$, and about the clever trick chemists use to run it *backward*: if you know exactly how stubborn water is, you can watch a known amount of water warm up and work out exactly how much heat a mystery reaction released. That trick is called **calorimetry**, and it's how we actually measure energy in the lab.*

---

## What You'll Learn

- Distinguish **heat capacity** (a whole object) from **specific heat capacity** $c$ (per gram) and **molar heat capacity** (per mole)
- Use $\ce{q = mc\Delta T}$ fluently — solving for $q$, for $\Delta T$, for $m$, or for $c$ — and get the **sign of $q$** right from the sign of $\Delta T$
- Explain what water's high specific heat ($4.18\ \text{J/g}\cdot^\circ\text{C}$) means physically, and why it moderates coastal climate
- Compare metals (low $c$, heat and cool fast) with water (high $c$) and explain everyday effects like a metal spoon burning you in hot soup
- State the calorimetry principle from conservation of energy: $\ce{q_{lost} = -q_{gained}}$, and describe a coffee-cup (constant-pressure) calorimeter
- Solve the classic **"identify the metal"** problem — hot metal dropped into water — and the **hot-meets-cold** mixing problem for a final temperature
- Turn a measured $q_\text{rxn}$ into $\Delta H$ in **kJ/mol** with the correct endothermic/exothermic sign
- Fold **phase-change energy** (heat of fusion and vaporization) into calorimetry, including the multi-step ice-into-warm-water problem
- Reason about **calorimetry error** — heat lost to the room, incomplete transfer — and predict how each shifts the computed answer

---

## Prerequisites

- [Energy and Heat](/chemistry/0801-energy-and-heat) — you need to know what heat is, the joule, and the endothermic/exothermic sign convention ($q > 0$ absorbed, $q < 0$ released) before any of this makes sense; this article turns that vocabulary into measured numbers
- [Phase Changes](/chemistry/0503-phase-changes) — heat of fusion/vaporization, the two-formula ($q=mc\Delta T$ vs. $q=m\Delta H$) split, and the heating curve all come back the moment a calorimetry problem crosses a melting or boiling point
- [Significant Figures](/chemistry/0102-significant-figures) — calorimetry is a lab measurement, so the error analysis and sig-fig rules from Unit 0 decide how you report and critique a result

---

## The Core Concept

### Intuition First

Let's stay on the beach at Torrey Pines, because the burning sand and the cool ocean are going to teach the entire topic.

The sun is dumping energy onto both surfaces at basically the same rate — call it the same number of joules per second landing on every square meter of sand and every square meter of water. If both materials responded to energy the same way, they'd end the afternoon at the same temperature. They don't, and the reason is that **temperature rise depends on more than just how much energy you add — it depends on how hard the material resists warming up.**

That resistance is **specific heat**, $c$. Think of it as stubbornness per gram:

- **Water has a high specific heat.** It is *stubborn*. You can pour a mountain of energy into water and its temperature barely creeps up, because a huge fraction of that energy goes into jostling water's hydrogen bonds around instead of speeding the molecules up. High $c$ = small $\Delta T$ for a given amount of heat. The ocean soaks up sunlight all afternoon and stays refreshing.
- **Sand has a low specific heat.** It is *easy*. The same sunlight that barely moved the water's temperature sends the sand's temperature shooting up, because sand doesn't have much capacity to hide the energy — it all goes straight into faster-jiggling atoms, which is exactly what a thermometer reads. Low $c$ = big $\Delta T$ for the same heat. Hence the griddle.

So here's the map for the whole article:

- **Specific heat $c$ = how stubborn a material's temperature is** — the energy needed to raise one gram by one degree. High $c$ (water) resists; low $c$ (sand, metals) gives in.
- **$\ce{q = mc\Delta T}$ is that idea as an equation:** the heat $q$ you need equals the mass $m$, times the stubbornness $c$, times the temperature change $\Delta T$ you want.
- **Calorimetry flips the arrow.** Instead of asking "how much will the temperature rise?", we *measure* the temperature rise of a known water sample and run the equation backward to find the heat a reaction dumped in — because water's $c$ is a number we trust down to the decimal.

Keep the two beaches in mind. Every equation below is bookkeeping for why your feet burned but your gasp was cold.

### Heat Capacity vs. Specific Heat Capacity

Three closely related words trip people up, so let's pin them down.

- **Heat capacity** (symbol $C$, capital) belongs to a *whole object*: the joules needed to raise *that entire thing* by one degree. A cast-iron pan and a teaspoon made of the same iron have different heat capacities, because the pan has more stuff. Units: $\text{J}/^\circ\text{C}$.
- **Specific heat capacity** (symbol $c$, lowercase — often just "specific heat") is heat capacity *per gram*, so it's a property of the **material**, not the object. Iron is iron whether it's a pan or a spoon. Units: $\text{J}/(\text{g}\cdot^\circ\text{C})$.
- **Molar heat capacity** is heat capacity *per mole* — same idea, but counting particles instead of grams. Units: $\text{J}/(\text{mol}\cdot^\circ\text{C})$.

For AP Chemistry, $c$ (specific heat, per gram) is the workhorse. The master equation is:

$$\ce{q = mc\Delta T}$$

where

- $q$ = heat absorbed or released, in joules ($\text{J}$),
- $m$ = mass of the sample, in grams ($\text{g}$),
- $c$ = specific heat, in $\text{J}/(\text{g}\cdot^\circ\text{C})$,
- $\Delta T = T_\text{final} - T_\text{initial}$, in $^\circ\text{C}$ (or $\text{K}$ — a *change* is the same size either way).

**The sign takes care of itself.** If the sample warms up, $T_\text{final} > T_\text{initial}$, so $\Delta T > 0$ and $q > 0$ (heat absorbed — the sample gained energy). If it cools, $\Delta T < 0$ and $q < 0$ (heat released). You never guess the sign; you read it off $\Delta T$.

### Water's Famously High Specific Heat

Here is the table of numbers you'll use all unit. AP gives you $c_\text{water}$ on the exam.

| Material | Specific heat $c$ ($\text{J/g}\cdot^\circ\text{C}$) | Personality |
|---|---|---|
| **Liquid water** | **4.18** | The stubborn one |
| Ethanol | 2.44 | Fairly stubborn |
| Ice | 2.09 | — |
| Steam | 2.01 | — |
| Aluminum | 0.897 | Easy |
| Iron | 0.449 | Easy |
| Copper | 0.385 | Easy |
| Silver / gold | ~0.24 / 0.13 | Very easy |
| Sand (silica) | ~0.84 | Easy (why the beach burns) |

Look at how water dwarfs everything else. Water's $c = 4.18$ means it takes $4.18\ \text{J}$ to warm a single gram by a single degree — about **ten times** what copper needs, and about five times what sand needs. That one fact is responsible for a startling amount of the world:

- **Coastal climate.** The Pacific off San Diego is a colossal heat reservoir. It warms slowly in summer and cools slowly in winter, holding our coast in a narrow, mild band while El Cajon and the desert swing hot and cold. The ocean is the heat sponge; we live next to it.
- **Your body.** You're mostly water, so your temperature is stable even as you generate and lose heat all day. High $c$ is thermal ballast.
- **Why water is the calorimetry fluid of choice.** Precisely *because* its $c$ is large and extremely well-known, a small, easily measured temperature change in water corresponds to a reliable, sizable amount of heat. Water is the ruler we measure reactions against.

### Metals: Low $c$, Fast to Heat and Cool

Metals sit at the opposite end of the table — small $c$, so their temperatures move *easily*. Two everyday consequences:

- **The metal spoon in the soup.** Leave a metal spoon in a bowl of hot soup and the handle gets too hot to hold fast; leave a wooden or plastic spoon and it stays comfortable. The metal's low specific heat (and high conductivity) means little energy warms it a lot, quickly. Same reason a metal seatbelt buckle in a parked car burns your hand while the fabric seat doesn't.
- **Cooling fast, too.** Low $c$ cuts both ways: a metal pan pulled off the stove cools down far faster than the same mass of water, which clings to its heat. Stubbornness is symmetric.

This is also the physics behind the "identify the metal" lab: because each metal has its own signature $c$, measuring how much a hot metal sample warms a known mass of water lets you back out $c$ and name the metal.

### The Calorimetry Principle: Conservation of Energy

Calorimetry is nothing more than **energy bookkeeping in an insulated box.** The core idea is conservation of energy: if a hot object and cold water are sealed together and no energy leaks out, then every joule the hot object loses is a joule the water gains. Nothing vanishes.

$$\ce{q_{lost} + q_{gained} = 0} \qquad\Longrightarrow\qquad \ce{q_{lost} = -q_{gained}}$$

The minus sign is the whole game: the hot thing's $q$ is **negative** (it releases heat, cools down) and the cold thing's $q$ is **positive** (it absorbs heat, warms up), and they're equal in magnitude. In practice we write it as:

$$\ce{q_{hot} = -q_{cold}} \qquad\text{i.e.}\qquad m_\text{hot}\,c_\text{hot}\,\Delta T_\text{hot} = -\,m_\text{cold}\,c_\text{cold}\,\Delta T_\text{cold}$$

**The coffee-cup calorimeter.** The AP workhorse is delightfully low-tech: two nested Styrofoam coffee cups with a lid, a thermometer poked through the top, and a stirrer. It runs at **constant pressure** (it's open to the air through the lid), so the heat it measures is $q_p = \Delta H$ — exactly the enthalpy change we want (more on that in [Enthalpy of Reaction](/chemistry/0803-enthalpy-of-reaction)). You dissolve a salt or mix two solutions inside, watch the water temperature change, and compute the heat.

**The key assumption:** the Styrofoam is a good enough insulator that the *calorimeter itself absorbs negligible heat* and *no heat leaks to the room.* Under that assumption, all the reaction's heat goes into (or comes out of) the water. Every calorimetry calculation you'll do rides on this idealization — and every calorimetry error you'll analyze is a way that idealization fails.

> **A quick note on the bomb calorimeter.** For combustion, chemists use a **bomb calorimeter**: the sample is sealed in a sturdy steel "bomb" immersed in water and ignited electrically. Because the steel bomb has a *fixed volume*, it measures heat at **constant volume** ($q_v = \Delta E$, the internal-energy change) rather than constant pressure. It's built to capture *all* the heat — the whole assembly, water plus bomb, has a known total heat capacity — which is why it's the tool for precise "Calories per serving" food-energy measurements. Coffee cup = constant pressure = $\Delta H$; bomb = constant volume = $\Delta E$.

### Phase Changes Inside Calorimetry

Everything above assumes the water just warms or cools smoothly. But the instant a process **crosses a phase boundary** — you drop *ice* into the cup, or a product boils — plain $q = mc\Delta T$ is no longer enough. You have to add the **latent heat** of the phase change, exactly as in [Phase Changes](/chemistry/0503-phase-changes):

$$q = m\,\Delta H_\text{fus}\quad(\text{melting/freezing}) \qquad\qquad q = m\,\Delta H_\text{vap}\quad(\text{boiling/condensing})$$

with, for water, $\Delta H_\text{fus} = 334\ \text{J/g}$ ($6.01\ \text{kJ/mol}$) and $\Delta H_\text{vap} = 2260\ \text{J/g}$ ($40.7\ \text{kJ/mol}$).

The classic case is **ice dropped into warm water.** The ice doesn't just warm up — it first has to *melt* (soaking up $\Delta H_\text{fus}$ at $0\,^\circ\text{C}$ without any temperature change), and *then* the resulting cold water warms toward the final temperature. That's why adding ice makes a drink so much colder than adding the same mass of $0\,^\circ\text{C}$ water: melting the ice steals a large chunk of heat out of the warm water before the temperatures even start to converge. In a calorimeter, that stolen heat is exactly why the measured temperature **drops** so far when ice is added. We'll do the full multi-step version in Example 9.

---

## Worked Examples

### Example 1: Straight $q = mc\Delta T$ (solve for $q$)

**Problem:** How much heat is needed to warm $250.\ \text{g}$ of water (about a tall glass) from $22.0\,^\circ\text{C}$ to $95.0\,^\circ\text{C}$ for a cup of tea? ($c_\text{water} = 4.18\ \text{J/g}\cdot^\circ\text{C}$)

**Solution:**

**Step 1 — Pick the formula.** Temperature changes, no phase change: $q = mc\Delta T$.

**Step 2 — Find $\Delta T$.** $\Delta T = 95.0 - 22.0 = 73.0\,^\circ\text{C}$.

**Step 3 — Plug in.**
$$q = (250.\ \text{g})(4.18\ \tfrac{\text{J}}{\text{g}\cdot^\circ\text{C}})(73.0\,^\circ\text{C}) = 76{,}285\ \text{J}$$

**Step 4 — Round and interpret.** $\approx 7.63 \times 10^4\ \text{J} = 76.3\ \text{kJ}$. Positive, because the water absorbs heat.

**Answer: about $76.3\ \text{kJ}$ absorbed.**

### Example 2: Solve for $c$ (identify a mystery material)

**Problem:** A $125\ \text{g}$ chunk of metal absorbs $2350\ \text{J}$ of heat and its temperature rises from $25.0\,^\circ\text{C}$ to $67.8\,^\circ\text{C}$. What is the metal's specific heat, and (using the table) what might the metal be?

**Solution:**

**Step 1 — Rearrange $q = mc\Delta T$ for $c$.** $c = \dfrac{q}{m\,\Delta T}$.

**Step 2 — Compute $\Delta T$.** $\Delta T = 67.8 - 25.0 = 42.8\,^\circ\text{C}$.

**Step 3 — Plug in.**
$$c = \frac{2350\ \text{J}}{(125\ \text{g})(42.8\,^\circ\text{C})} = 0.439\ \tfrac{\text{J}}{\text{g}\cdot^\circ\text{C}}$$

**Step 4 — Match.** That's very close to iron ($0.449$). Low $c$ — an "easy," fast-heating metal, as expected.

**Answer: $c \approx 0.439\ \text{J/g}\cdot^\circ\text{C}$; the metal is most likely iron.**

### Example 3: Solve for $\Delta T$ (and final temperature)

**Problem:** You add $1500\ \text{J}$ of heat to $40.0\ \text{g}$ of aluminum starting at $20.0\,^\circ\text{C}$. What's the final temperature? ($c_\text{Al} = 0.897\ \text{J/g}\cdot^\circ\text{C}$)

**Solution:**

**Step 1 — Solve $q = mc\Delta T$ for $\Delta T$.** $\Delta T = \dfrac{q}{mc}$.

**Step 2 — Plug in.**
$$\Delta T = \frac{1500\ \text{J}}{(40.0\ \text{g})(0.897\ \tfrac{\text{J}}{\text{g}\cdot^\circ\text{C}})} = 41.8\,^\circ\text{C}$$

**Step 3 — Add to the start.** $T_\text{final} = 20.0 + 41.8 = 61.8\,^\circ\text{C}$.

**Step 4 — Sanity check.** The same $1500\ \text{J}$ into $40\ \text{g}$ of *water* would raise it only $\Delta T = 1500/(40.0 \cdot 4.18) = 9.0\,^\circ\text{C}$ — water's stubbornness in action.

**Answer: $T_\text{final} \approx 61.8\,^\circ\text{C}$.**

### Example 4: Sand vs. Water (the beach, quantified)

**Problem:** The noon sun delivers about $500\ \text{J}$ to the top $100\ \text{g}$ of dry sand ($c \approx 0.84\ \text{J/g}\cdot^\circ\text{C}$) and the same $500\ \text{J}$ to $100\ \text{g}$ of ocean water ($c = 4.18$). How much does each warm up?

**Solution:**

**Step 1 — Sand, solve for $\Delta T$.**
$$\Delta T_\text{sand} = \frac{500\ \text{J}}{(100\ \text{g})(0.84)} = 6.0\,^\circ\text{C}$$

**Step 2 — Water, same heat.**
$$\Delta T_\text{water} = \frac{500\ \text{J}}{(100\ \text{g})(4.18)} = 1.2\,^\circ\text{C}$$

**Step 3 — Compare.** The identical sunlight warms the sand **five times more** than the water ($6.0$ vs. $1.2\,^\circ\text{C}$) — the exact ratio of their specific heats ($4.18/0.84 \approx 5$).

**Answer: sand rises $\approx 6.0\,^\circ\text{C}$, water only $\approx 1.2\,^\circ\text{C}$ — griddle vs. refrigerator, from the same sun.**

### Example 5: Hot Metal into Water — Find the Final Temperature

**Problem:** A $95.0\ \text{g}$ block of copper ($c = 0.385$) is heated to $250.0\,^\circ\text{C}$ and dropped into $150.0\ \text{g}$ of water at $22.0\,^\circ\text{C}$ in a coffee-cup calorimeter. Assuming no heat is lost, what final temperature $T_f$ do they reach?

**Solution:**

**Step 1 — Set up conservation.** Heat lost by copper = heat gained by water: $\ce{q_{Cu} = -q_{water}}$. Both share the same unknown $T_f$.

**Step 2 — Write each side** (let $T_f$ be the common final temperature):
$$m_\text{Cu}\,c_\text{Cu}(T_f - 250.0) = -\,m_\text{w}\,c_\text{w}(T_f - 22.0)$$

**Step 3 — Plug in the numbers.**
$$(95.0)(0.385)(T_f - 250.0) = -(150.0)(4.18)(T_f - 22.0)$$
$$36.58(T_f - 250.0) = -627.0(T_f - 22.0)$$

**Step 4 — Expand and solve.**
$$36.58\,T_f - 9145 = -627.0\,T_f + 13{,}794$$
$$663.6\,T_f = 22{,}939 \quad\Rightarrow\quad T_f = 34.6\,^\circ\text{C}$$

**Step 5 — Sanity check.** $T_f$ lands between $22$ and $250$, but much closer to the water's start — because there's more water and its $c$ is far larger. The stubborn, heavy water barely budges. 

**Answer: $T_f \approx 34.6\,^\circ\text{C}$.**

### Example 6: Identify the Metal (find $c$ from a water bath)

**Problem:** A $50.0\ \text{g}$ metal sample is heated in boiling water to $99.5\,^\circ\text{C}$, then dropped into $100.0\ \text{g}$ of water at $21.0\,^\circ\text{C}$. The water warms to a final $24.6\,^\circ\text{C}$. What is the metal's specific heat, and what is it?

**Solution:**

**Step 1 — Conservation.** $\ce{q_{metal} = -q_{water}}$.

**Step 2 — The water side is fully known.** $\Delta T_\text{w} = 24.6 - 21.0 = 3.6\,^\circ\text{C}$.
$$q_\text{water} = (100.0)(4.18)(3.6) = 1505\ \text{J}$$

**Step 3 — The metal released that much.** $q_\text{metal} = -1505\ \text{J}$, with $\Delta T_\text{metal} = 24.6 - 99.5 = -74.9\,^\circ\text{C}$.

**Step 4 — Solve for $c_\text{metal}$.**
$$c = \frac{q_\text{metal}}{m\,\Delta T} = \frac{-1505\ \text{J}}{(50.0\ \text{g})(-74.9\,^\circ\text{C})} = 0.402\ \tfrac{\text{J}}{\text{g}\cdot^\circ\text{C}}$$

**Step 5 — Match.** Closest to iron ($0.449$) or copper ($0.385$) — around $0.40$, so likely **iron or a similar transition metal**. (On the AP exam you'd pick the nearest tabulated value.)

**Answer: $c \approx 0.40\ \text{J/g}\cdot^\circ\text{C}$ — consistent with iron/copper-range metals.**

### Example 7: Two Water Samples Mixed — Final Temperature

**Problem:** You mix $200.0\ \text{g}$ of water at $80.0\,^\circ\text{C}$ with $300.0\ \text{g}$ of water at $20.0\,^\circ\text{C}$. What's the final temperature? (No heat lost.)

**Solution:**

**Step 1 — Conservation, same $c$ both sides.** $\ce{q_{hot} = -q_{cold}}$. Because both are water, $c$ cancels:
$$m_\text{hot}(T_f - 80.0) = -\,m_\text{cold}(T_f - 20.0)$$

**Step 2 — Plug in.**
$$200.0(T_f - 80.0) = -300.0(T_f - 20.0)$$

**Step 3 — Expand and solve.**
$$200\,T_f - 16{,}000 = -300\,T_f + 6000$$
$$500\,T_f = 22{,}000 \quad\Rightarrow\quad T_f = 44.0\,^\circ\text{C}$$

**Step 4 — Sanity check.** With more cold water than hot, $T_f$ should sit *below* the midpoint ($50\,^\circ\text{C}$). It does — $44.0\,^\circ\text{C}$, pulled toward the larger cold mass.

**Answer: $T_f = 44.0\,^\circ\text{C}$.**

### Example 8: A Reaction in Solution — Find $q_\text{rxn}$ and $\Delta H$ per Mole

**Problem:** In a coffee-cup calorimeter, $3.50\ \text{g}$ of $\ce{NH4NO3}$ (molar mass $80.0\ \text{g/mol}$) is dissolved in $100.0\ \text{g}$ of water. The temperature *drops* from $23.0\,^\circ\text{C}$ to $18.6\,^\circ\text{C}$. Find $q_\text{rxn}$ and $\Delta H_\text{soln}$ in kJ/mol. Is dissolving $\ce{NH4NO3}$ endo- or exothermic? (Assume the solution's $c = 4.18$ and mass $\approx 100.0\ \text{g}$.)

**Solution:**

**Step 1 — Heat absorbed by the solution.** $\Delta T = 18.6 - 23.0 = -4.4\,^\circ\text{C}$.
$$q_\text{solution} = (100.0)(4.18)(-4.4) = -1839\ \text{J}$$
The solution *lost* $1839\ \text{J}$ (it cooled).

**Step 2 — Flip the sign for the reaction.** The dissolving *took* that heat from the water:
$$q_\text{rxn} = -q_\text{solution} = +1839\ \text{J} = +1.84\ \text{kJ}$$
Positive $q_\text{rxn}$ → the process **absorbed** heat → **endothermic** (that's why the water got colder — this is literally how instant cold packs work).

**Step 3 — Moles of $\ce{NH4NO3}$.**
$$n = \frac{3.50\ \text{g}}{80.0\ \text{g/mol}} = 0.04375\ \text{mol}$$

**Step 4 — $\Delta H$ per mole.**
$$\Delta H = \frac{+1.84\ \text{kJ}}{0.04375\ \text{mol}} = +42.0\ \text{kJ/mol}$$

**Answer: $q_\text{rxn} = +1.84\ \text{kJ}$; $\Delta H_\text{soln} = +42.0\ \text{kJ/mol}$; endothermic (positive sign, water cooled).**

### Example 9: Neutralization — $\ce{HCl + NaOH}$

**Problem:** $50.0\ \text{mL}$ of $1.00\ \text{M}\ \ce{HCl}$ is mixed with $50.0\ \text{mL}$ of $1.00\ \text{M}\ \ce{NaOH}$ in a coffee cup. The temperature rises from $21.0\,^\circ\text{C}$ to $27.8\,^\circ\text{C}$. Find $\Delta H$ per mole of water formed. (Total mass $100.0\ \text{g}$, $c = 4.18$; the reaction is $\ce{HCl + NaOH -> NaCl + H2O}$.)

**Solution:**

**Step 1 — Heat gained by the solution.** $\Delta T = 27.8 - 21.0 = 6.8\,^\circ\text{C}$.
$$q_\text{solution} = (100.0)(4.18)(6.8) = 2842\ \text{J} = 2.84\ \text{kJ}$$

**Step 2 — Reaction released it.** $q_\text{rxn} = -q_\text{solution} = -2.84\ \text{kJ}$. Negative → **exothermic** (the water warmed).

**Step 3 — Moles of water formed.** $\ce{HCl}$: $(0.0500\ \text{L})(1.00\ \text{M}) = 0.0500\ \text{mol}$; $\ce{NaOH}$ likewise $0.0500\ \text{mol}$. They react 1:1 to make $0.0500\ \text{mol}$ of $\ce{H2O}$.

**Step 4 — $\Delta H$ per mole.**
$$\Delta H = \frac{-2.84\ \text{kJ}}{0.0500\ \text{mol}} = -56.8\ \text{kJ/mol}$$

**Answer: $\Delta H \approx -56.8\ \text{kJ/mol}$ of water — exothermic, close to the accepted $-57.3\ \text{kJ/mol}$ for strong acid–base neutralization.**

### Example 10: Ice into Warm Water — The Full Multi-Step Problem

**Problem:** A $25.0\ \text{g}$ ice cube at $0.0\,^\circ\text{C}$ is dropped into $200.0\ \text{g}$ of water at $30.0\,^\circ\text{C}$ in an insulated cup. Find the final temperature. ($\Delta H_\text{fus} = 334\ \text{J/g}$, $c_\text{water} = 4.18$.) Assume all the ice melts.

**Solution:**

**Step 1 — Account for every energy transfer.** The ice does *two* things: (a) **melt** at $0\,^\circ\text{C}$ (latent heat, $q = m\Delta H_\text{fus}$), then (b) the melted water **warms** from $0\,^\circ\text{C}$ to $T_f$. The warm water only cools from $30\,^\circ\text{C}$ to $T_f$. Conservation: heat lost by warm water = heat gained by (melting + warming the ice-water).

**Step 2 — Write the balance.**
$$\underbrace{(200.0)(4.18)(30.0 - T_f)}_{\text{warm water cools}} = \underbrace{(25.0)(334)}_{\text{melt the ice}} + \underbrace{(25.0)(4.18)(T_f - 0)}_{\text{melted water warms}}$$

**Step 3 — Compute the constants.**
$$836.0(30.0 - T_f) = 8350 + 104.5\,T_f$$
$$25{,}080 - 836.0\,T_f = 8350 + 104.5\,T_f$$

**Step 4 — Solve.**
$$25{,}080 - 8350 = 104.5\,T_f + 836.0\,T_f$$
$$16{,}730 = 940.5\,T_f \quad\Rightarrow\quad T_f = 17.8\,^\circ\text{C}$$

**Step 5 — Interpret.** Adding $25\ \text{g}$ of *ice* drove the temperature from $30\,^\circ\text{C}$ down to $17.8\,^\circ\text{C}$. Most of that drop came from the $8350\ \text{J}$ spent just *melting* the ice — melting steals a big block of heat before any warming happens, which is exactly why ice cools a drink so much more than cold water does. In a calorimeter this is why the reading plunges when ice is added.

**Answer: $T_f \approx 17.8\,^\circ\text{C}$.**

### Example 11: Molar Heat Capacity Comparison

**Problem:** Copper has $c = 0.385\ \text{J/g}\cdot^\circ\text{C}$ and molar mass $63.5\ \text{g/mol}$. What is its molar heat capacity? Compare it with water's ($c = 4.18$, molar mass $18.0$).

**Solution:**

**Step 1 — Convert per-gram to per-mole.** Multiply $c$ by the molar mass:
$$C_\text{m,Cu} = (0.385\ \tfrac{\text{J}}{\text{g}\cdot^\circ\text{C}})(63.5\ \tfrac{\text{g}}{\text{mol}}) = 24.4\ \tfrac{\text{J}}{\text{mol}\cdot^\circ\text{C}}$$

**Step 2 — Water.**
$$C_\text{m,water} = (4.18)(18.0) = 75.2\ \tfrac{\text{J}}{\text{mol}\cdot^\circ\text{C}}$$

**Step 3 — Compare.** Per mole, water still needs about three times more energy per degree — its hydrogen bonds are the reason. (Interesting aside: many solid metals cluster near $\sim25\ \text{J/mol}\cdot^\circ\text{C}$, the Dulong–Petit value, even though their *per-gram* $c$ values differ a lot.)

**Answer: $C_\text{m,Cu} \approx 24.4\ \text{J/mol}\cdot^\circ\text{C}$ vs. water's $75.2\ \text{J/mol}\cdot^\circ\text{C}$.**

### Example 12: Calorimetry Error — Heat Lost to the Room

**Problem:** In Example 6, suppose the cheap calorimeter actually let some heat leak to the room air during the transfer. Would the *computed* specific heat of the metal come out too high or too low? Explain.

**Solution:**

**Step 1 — What leaking does.** If heat escapes to the room, the water ends up *cooler* than it should — the measured final temperature is too low, so the observed $\Delta T_\text{water}$ is too small.

**Step 2 — Trace it through $q_\text{water}$.** A smaller $\Delta T_\text{water}$ makes the calculated $q_\text{water}$ too small, so we *think* the metal released less heat than it truly did.

**Step 3 — Trace it into $c$.** Since $c_\text{metal} = q/(m\,\Delta T_\text{metal})$ with a too-small $q$, the computed $c$ comes out **too low**.

**Step 4 — General lesson.** Real coffee-cup calorimeters always lose *some* heat, so measured exothermic outputs and derived $c$ values are typically **underestimates**. Better insulation and quick transfer shrink the error.

**Answer: too low — heat loss shrinks the measured $\Delta T_\text{water}$, shrinking the computed $q$ and therefore the computed $c$.**

---

## Common Mistakes

| The Mistake | Why It Happens | The Fix |
|---|---|---|
| Forgetting the minus sign in $\ce{q_{lost} = -q_{gained}}$ | Rushing the setup | The hot object's $q$ is negative, the cold's is positive. Write the minus sign *first*, before numbers |
| Using $q = mc\Delta T$ across a phase change | Auto-piloting the "heat" formula | If the process melts, freezes, or boils, add $q = m\Delta H$ for that step. $mc\Delta T$ alone misses the latent heat |
| Mixing up $C$ (whole object) and $c$ (per gram) | Similar symbols | $c$ has grams in the unit ($\text{J/g}\cdot^\circ\text{C}$); $C$ does not ($\text{J}/^\circ\text{C}$). Check the units |
| Wrong sign on $\Delta T$ | Writing $T_i - T_f$ instead of $T_f - T_i$ | Always $\Delta T = T_\text{final} - T_\text{initial}$. Cooling gives a negative $\Delta T$ and a negative $q$ |
| Reporting $q_\text{rxn}$ with the same sign as $q_\text{water}$ | Forgetting the flip | The reaction and the water have **opposite** signs: $q_\text{rxn} = -q_\text{water}$. Water warms → reaction is exothermic ($q_\text{rxn}<0$) |
| Mixing joules and kilojoules | $c$ is in J, $\Delta H$ often in kJ | Convert everything to one unit first. $1\ \text{kJ} = 1000\ \text{J}$ |
| Using grams as kilograms (or vice versa) | $c$ is per *gram* | $c_\text{water}=4.18\ \text{J/g}\cdot^\circ\text{C}$ needs mass in grams. A $0.150\ \text{kg}$ sample is $150\ \text{g}$ |
| Forgetting to divide by moles for $\Delta H$ | Stopping at $q_\text{rxn}$ | $\Delta H$ (kJ/mol) $= q_\text{rxn} \div$ moles of the limiting/specified substance. Find moles, then divide |
| Assuming the calorimeter absorbs zero heat is always exact | Taking the ideal literally | It's an *assumption*; real cups leak. On error questions, say which way the leak pushes the answer |

---

## AP Exam Tips

1. **$q = mc\Delta T$ is a guaranteed appearance.** Know it cold and be ready to solve for any of the four variables. Watch which quantity is unknown and rearrange *before* plugging in.
2. **The lost = −gained setup earns the points.** For any "hot meets cold" problem, write $\ce{q_{hot} = -q_{cold}}$ explicitly, expand both $mc\Delta T$ expressions with the *same* $T_f$, and solve the linear equation. Graders give partial credit for the correct setup even if arithmetic slips.
3. **Convert $q_\text{rxn}$ to $\Delta H$ per mole, with the right sign.** The recipe: (1) $q_\text{solution} = mc\Delta T$; (2) $q_\text{rxn} = -q_\text{solution}$; (3) $\Delta H = q_\text{rxn}/\text{moles}$. Temperature **up** → exothermic → **negative** $\Delta H$. Temperature **down** → endothermic → **positive**.
4. **Watch units — J vs. kJ, g vs. kg.** A huge fraction of lost points are unit slips. Specific heat is per gram and in joules; $\Delta H$ is usually reported in kJ/mol. Line up units before you compute.
5. **Include phase-change heat whenever a boundary is crossed.** If ice is involved, melt it first ($q = m\Delta H_\text{fus}$) *then* warm the water. Miss the latent-heat term and every downstream number is wrong. Sketch the mini heating curve to catch every segment.
6. **Calorimetry-error reasoning is a common FRQ.** Expect "the student's value was too high/low — explain." Trace the flaw through the equation: heat lost to the room → smaller measured $\Delta T$ → smaller $q$ → underestimate. Always state the *direction* of the error and *why*.
7. **Assumptions are worth naming.** Good FRQ answers state "assume no heat lost to the calorimeter or surroundings" and "assume the solution has the density and specific heat of water." Naming the assumption shows you understand the idealization.
8. **Sig figs still count.** This is a measured lab quantity — match the least-precise measurement, usually the temperature reading (see [Significant Figures](/chemistry/0102-significant-figures)).

---

## Practice Problems

### Problem 1

How much heat is required to raise the temperature of $500.\ \text{g}$ of water from $18.0\,^\circ\text{C}$ to $88.0\,^\circ\text{C}$? ($c_\text{water} = 4.18$)

<details>
<summary><strong>Solution</strong></summary>

Single phase, temperature changes: $q = mc\Delta T$. $\Delta T = 88.0 - 18.0 = 70.0\,^\circ\text{C}$.

$$q = (500.)(4.18)(70.0) = 146{,}300\ \text{J} \approx 146\ \text{kJ}$$

**About $146\ \text{kJ}$ absorbed.**

</details>

### Problem 2

A $200.\ \text{g}$ block of aluminum ($c = 0.897$) cools from $150.0\,^\circ\text{C}$ to $30.0\,^\circ\text{C}$. How much heat does it release?

<details>
<summary><strong>Solution</strong></summary>

$\Delta T = 30.0 - 150.0 = -120.0\,^\circ\text{C}$.

$$q = (200.)(0.897)(-120.0) = -21{,}528\ \text{J} \approx -21.5\ \text{kJ}$$

Negative = released.

**About $21.5\ \text{kJ}$ released ($q = -21.5\ \text{kJ}$).**

</details>

### Problem 3

A $60.0\ \text{g}$ sample of metal absorbs $1200\ \text{J}$ as it warms from $20.0\,^\circ\text{C}$ to $58.4\,^\circ\text{C}$. Find its specific heat and identify it (table in the article).

<details>
<summary><strong>Solution</strong></summary>

$\Delta T = 58.4 - 20.0 = 38.4\,^\circ\text{C}$.

$$c = \frac{q}{m\,\Delta T} = \frac{1200}{(60.0)(38.4)} = 0.521\ \tfrac{\text{J}}{\text{g}\cdot^\circ\text{C}}$$

Closest tabulated value is iron ($0.449$) — a bit high, but in the low-$c$ metal range.

**$c \approx 0.521\ \text{J/g}\cdot^\circ\text{C}$; a low-specific-heat metal, nearest to iron.**

</details>

### Problem 4

You add $5000\ \text{J}$ of heat to $250.\ \text{g}$ of water at $15.0\,^\circ\text{C}$. What is the final temperature?

<details>
<summary><strong>Solution</strong></summary>

$$\Delta T = \frac{q}{mc} = \frac{5000}{(250.)(4.18)} = 4.78\,^\circ\text{C}$$

$$T_f = 15.0 + 4.78 = 19.8\,^\circ\text{C}$$

**About $19.8\,^\circ\text{C}$.**

</details>

### Problem 5

Why does the wooden handle of a pot stay cool enough to grab while the metal pot itself is scorching, even though both have been on the stove the same length of time? Answer in terms of specific heat.

<details>
<summary><strong>Solution</strong></summary>

Metal has a **low specific heat** (and high conductivity), so a small amount of heat sends its temperature way up quickly — it heats fast and gets hot. Wood has a higher specific heat and conducts poorly, so it resists warming and stays cool to the touch.

**Low-$c$ metal heats fast and hot; higher-$c$, poorly conducting wood resists warming and stays grabbable.**

</details>

### Problem 6

A $75.0\ \text{g}$ piece of iron ($c = 0.449$) at $200.0\,^\circ\text{C}$ is dropped into $120.0\ \text{g}$ of water at $20.0\,^\circ\text{C}$. Find the final temperature (no heat lost).

<details>
<summary><strong>Solution</strong></summary>

$\ce{q_{Fe} = -q_{water}}$:

$$(75.0)(0.449)(T_f - 200.0) = -(120.0)(4.18)(T_f - 20.0)$$
$$33.68(T_f - 200.0) = -501.6(T_f - 20.0)$$
$$33.68\,T_f - 6735 = -501.6\,T_f + 10{,}032$$
$$535.3\,T_f = 16{,}767 \quad\Rightarrow\quad T_f = 31.3\,^\circ\text{C}$$

**About $31.3\,^\circ\text{C}$** (close to the water's start — water's high $c$ and larger mass dominate).

</details>

### Problem 7

A metal sample ($40.0\ \text{g}$) is heated to $100.0\,^\circ\text{C}$ and placed in $80.0\ \text{g}$ of water at $19.0\,^\circ\text{C}$; the water warms to $23.2\,^\circ\text{C}$. Find the metal's specific heat.

<details>
<summary><strong>Solution</strong></summary>

Water: $\Delta T = 23.2 - 19.0 = 4.2\,^\circ\text{C}$, so $q_\text{water} = (80.0)(4.18)(4.2) = 1404\ \text{J}$.

Metal released it: $q_\text{metal} = -1404\ \text{J}$, $\Delta T_\text{metal} = 23.2 - 100.0 = -76.8\,^\circ\text{C}$.

$$c = \frac{-1404}{(40.0)(-76.8)} = 0.457\ \tfrac{\text{J}}{\text{g}\cdot^\circ\text{C}}$$

**$c \approx 0.457\ \text{J/g}\cdot^\circ\text{C}$ — essentially iron.**

</details>

### Problem 8

Mix $150.0\ \text{g}$ of water at $75.0\,^\circ\text{C}$ with $250.0\ \text{g}$ of water at $15.0\,^\circ\text{C}$. Find the final temperature.

<details>
<summary><strong>Solution</strong></summary>

$c$ cancels:

$$150.0(T_f - 75.0) = -250.0(T_f - 15.0)$$
$$150\,T_f - 11{,}250 = -250\,T_f + 3750$$
$$400\,T_f = 15{,}000 \quad\Rightarrow\quad T_f = 37.5\,^\circ\text{C}$$

Below the midpoint ($45\,^\circ\text{C}$) because there's more cold water.

**$T_f = 37.5\,^\circ\text{C}$.**

</details>

### Problem 9

Dissolving $4.00\ \text{g}$ of $\ce{NH4NO3}$ ($80.0\ \text{g/mol}$) in $150.0\ \text{g}$ of water drops the temperature from $22.5\,^\circ\text{C}$ to $18.9\,^\circ\text{C}$. Find $\Delta H_\text{soln}$ in kJ/mol and state endo/exo. (Solution mass $\approx 150.0\ \text{g}$, $c = 4.18$.)

<details>
<summary><strong>Solution</strong></summary>

$\Delta T = 18.9 - 22.5 = -3.6\,^\circ\text{C}$.

$q_\text{solution} = (150.0)(4.18)(-3.6) = -2257\ \text{J}$ (solution cooled).

$q_\text{rxn} = -q_\text{solution} = +2257\ \text{J} = +2.26\ \text{kJ}$ → **endothermic**.

Moles: $4.00/80.0 = 0.0500\ \text{mol}$.

$$\Delta H = \frac{+2.26\ \text{kJ}}{0.0500\ \text{mol}} = +45.1\ \text{kJ/mol}$$

**$\Delta H_\text{soln} \approx +45\ \text{kJ/mol}$; endothermic (the water cooled).**

</details>

### Problem 10

$50.0\ \text{mL}$ of $2.00\ \text{M}\ \ce{HCl}$ is mixed with $50.0\ \text{mL}$ of $2.00\ \text{M}\ \ce{NaOH}$; the temperature rises from $22.0\,^\circ\text{C}$ to $35.5\,^\circ\text{C}$. Find $\Delta H$ per mole of water formed. (Total mass $100.0\ \text{g}$, $c = 4.18$.)

<details>
<summary><strong>Solution</strong></summary>

$\Delta T = 35.5 - 22.0 = 13.5\,^\circ\text{C}$.

$q_\text{solution} = (100.0)(4.18)(13.5) = 5643\ \text{J} = 5.64\ \text{kJ}$.

$q_\text{rxn} = -5.64\ \text{kJ}$ → **exothermic**.

Moles water: $\ce{HCl} = (0.0500)(2.00) = 0.100\ \text{mol}$; matches $\ce{NaOH}$; forms $0.100\ \text{mol}\ \ce{H2O}$.

$$\Delta H = \frac{-5.64\ \text{kJ}}{0.100\ \text{mol}} = -56.4\ \text{kJ/mol}$$

**$\Delta H \approx -56.4\ \text{kJ/mol}$ — exothermic.**

</details>

### Problem 11

A $30.0\ \text{g}$ ice cube at $0.0\,^\circ\text{C}$ is added to $250.0\ \text{g}$ of water at $25.0\,^\circ\text{C}$ in an insulated cup. Find the final temperature. ($\Delta H_\text{fus} = 334\ \text{J/g}$, $c = 4.18$; assume all ice melts.)

<details>
<summary><strong>Solution</strong></summary>

Warm water cools; ice melts then warms:

$$(250.0)(4.18)(25.0 - T_f) = (30.0)(334) + (30.0)(4.18)(T_f - 0)$$
$$1045(25.0 - T_f) = 10{,}020 + 125.4\,T_f$$
$$26{,}125 - 1045\,T_f = 10{,}020 + 125.4\,T_f$$
$$16{,}105 = 1170.4\,T_f \quad\Rightarrow\quad T_f = 13.8\,^\circ\text{C}$$

**About $13.8\,^\circ\text{C}$** — the temperature drops far more than adding $30\ \text{g}$ of cold water would, because melting the ice absorbs $10{,}020\ \text{J}$ first.

</details>

### Problem 12

Explain why adding a $50\ \text{g}$ ice cube at $0\,^\circ\text{C}$ cools your soda much more than adding $50\ \text{g}$ of liquid water at $0\,^\circ\text{C}$.

<details>
<summary><strong>Solution</strong></summary>

The ice must first **melt** before it can warm up, absorbing its heat of fusion: $q = (50)(334) = 16{,}700\ \text{J}$ pulled out of the soda *at $0\,^\circ\text{C}$*, before the melted water even starts warming. The $0\,^\circ\text{C}$ liquid water skips that step and only warms up.

So the ice removes an extra ~$16.7\ \text{kJ}$ of latent heat, cooling the drink much more.

**Ice absorbs $\Delta H_\text{fus}$ (~$16.7\ \text{kJ}$) to melt before warming, stealing far more heat than cold water, which only warms.**

</details>

### Problem 13

A student measures a neutralization and computes $\Delta H = -48\ \text{kJ/mol}$, but the accepted value is $-57\ \text{kJ/mol}$. Give one calorimetry error that would explain the too-small magnitude, and show how it propagates.

<details>
<summary><strong>Solution</strong></summary>

**Heat lost to the surroundings** (a leaky Styrofoam cup, no lid, slow reading). Some reaction heat escapes to the room instead of warming the solution, so the measured $\Delta T$ is **too small**.

Smaller $\Delta T$ → smaller $q_\text{solution} = mc\Delta T$ → smaller $|q_\text{rxn}|$ → smaller $|\Delta H|$ when divided by moles. The computed magnitude comes out below the true value — exactly the $-48$ vs. $-57$ gap.

**Heat leaking to the room shrinks $\Delta T$, hence $q$ and $|\Delta H|$ — giving a value too small in magnitude.**

</details>

### Problem 14

The specific heat of ethanol is $2.44\ \text{J/g}\cdot^\circ\text{C}$ and of water is $4.18$. Equal masses of each absorb the same amount of heat. Which warms up more, and by what factor?

<details>
<summary><strong>Solution</strong></summary>

For fixed $q$ and $m$, $\Delta T = q/(mc)$, so $\Delta T$ is *inversely* proportional to $c$. Ethanol has the smaller $c$, so it warms **more**.

Factor: $\dfrac{\Delta T_\text{ethanol}}{\Delta T_\text{water}} = \dfrac{c_\text{water}}{c_\text{ethanol}} = \dfrac{4.18}{2.44} = 1.71$.

**Ethanol warms about 1.7 times more than water for the same heat — it's the less stubborn liquid.**

</details>

### Problem 15

A $40.0\ \text{g}$ copper cube ($c = 0.385$) at $95.0\,^\circ\text{C}$ is dropped into $40.0\ \text{g}$ of water at $10.0\,^\circ\text{C}$. Before calculating, predict whether $T_f$ lands nearer $10\,^\circ\text{C}$ or nearer $95\,^\circ\text{C}$, then compute it.

<details>
<summary><strong>Solution</strong></summary>

**Prediction:** equal masses, but water's $c$ is ~11× copper's, so water dominates and $T_f$ should land close to $10\,^\circ\text{C}$.

$$(40.0)(0.385)(T_f - 95.0) = -(40.0)(4.18)(T_f - 10.0)$$
$$15.4(T_f - 95.0) = -167.2(T_f - 10.0)$$
$$15.4\,T_f - 1463 = -167.2\,T_f + 1672$$
$$182.6\,T_f = 3135 \quad\Rightarrow\quad T_f = 17.2\,^\circ\text{C}$$

Just as predicted — barely above the water's start.

**$T_f \approx 17.2\,^\circ\text{C}$, near the water's initial temperature (water's high $c$ wins).**

</details>

---

## Quick Reference

**The master equation**

$$\ce{q = mc\Delta T} \qquad \Delta T = T_\text{final} - T_\text{initial}$$

$q$ in J, $m$ in g, $c$ in $\text{J/g}\cdot^\circ\text{C}$. $\Delta T > 0 \Rightarrow q > 0$ (absorbed); $\Delta T < 0 \Rightarrow q < 0$ (released).

**Three "capacities"**

| Term | Symbol | Per what | Units |
|---|---|---|---|
| Heat capacity | $C$ | whole object | $\text{J}/^\circ\text{C}$ |
| Specific heat | $c$ | gram | $\text{J/g}\cdot^\circ\text{C}$ |
| Molar heat capacity | $C_\text{m}$ | mole | $\text{J/mol}\cdot^\circ\text{C}$ |

**Calorimetry (conservation of energy)**

$$\ce{q_{lost} = -q_{gained}} \qquad m_\text{hot}c_\text{hot}\Delta T_\text{hot} = -\,m_\text{cold}c_\text{cold}\Delta T_\text{cold}$$

Coffee cup = **constant pressure** → $q = \Delta H$. Bomb = **constant volume** → $q = \Delta E$. Assume no heat lost to cup/room.

**Reaction $\to \Delta H$ per mole**

1. $q_\text{solution} = mc\Delta T$  2. $q_\text{rxn} = -q_\text{solution}$  3. $\Delta H = q_\text{rxn}/\text{mol}$.

Temp **up** → exothermic ($\Delta H < 0$); temp **down** → endothermic ($\Delta H > 0$).

**When a phase change is crossed**, add latent heat: $q = m\Delta H_\text{fus}$ (melt/freeze) or $q = m\Delta H_\text{vap}$ (boil/condense). Water: $\Delta H_\text{fus} = 334\ \text{J/g}$, $\Delta H_\text{vap} = 2260\ \text{J/g}$.

**Key numbers:** $c_\text{water} = 4.18\ \text{J/g}\cdot^\circ\text{C}$ (high — the stubborn one); metals ~$0.1$–$0.9$ (low — heat/cool fast). High $c$ = small $\Delta T$ (water, ocean); low $c$ = big $\Delta T$ (sand, metal spoon).

**Error reasoning:** heat lost to the room → measured $\Delta T$ too small → computed $q$ and $|\Delta H|$ (or $c$) come out **too low**.

---

<div align="center">

[← Energy and Heat](/chemistry/0801-energy-and-heat) | [Enthalpy of Reaction →](/chemistry/0803-enthalpy-of-reaction)

</div>
