# Reaction Rates
<p class="article-date">July 5, 2026</p>

*My phone died on the bus this morning, so the second I got home I plugged it in and watched the battery icon like it owed me money. Here's the thing I've seen a thousand times but never really thought about: it charged FAST at first — 3%, 8%, 15%, racing up while I brushed my teeth — and then it just... crawled. The last stretch from 92% to 100% took longer than the whole first half. The charging rate isn't constant. It's quick when the battery has a long way to go, and it slows to a trickle as it fills up. That is EXACTLY how a chemical reaction behaves: it runs fastest at the very start, when there's tons of reactant sitting around ready to react, and it slows down as the reactant gets used up. And just like I could ask two different questions about my phone — "how fast did it charge on average from 20% to 80%?" versus "how fast is it charging RIGHT this second?" — a reaction has an average rate over a stretch of time and an instantaneous rate at a single moment. This is AP Unit 5, Topic 5.1, the front door to chemical kinetics: the study of how FAST chemistry happens, not just whether it happens.*

---

## What You'll Learn
- Define **reaction rate** as the change in concentration of a species per unit time, with units of $\text{M/s}$ (molarity per second)
- Explain why we attach a **minus sign** to reactant rates so the reported rate stays positive
- Distinguish **average rate** (over a time interval), **instantaneous rate** (the slope of the tangent at one moment), and **initial rate** (the instantaneous rate at $t = 0$)
- Read a **concentration-vs-time graph** to estimate average and instantaneous rates, connecting "slope of the curve" to what you learned about graphing
- Write the rate of a reaction in terms of **any** species using the stoichiometric coefficients, and convert a rate measured for one species into the rate for another
- Explain **why rate decreases over time** by tying the flattening curve back to depleting reactant
- Describe how rates are **measured experimentally** — color/absorbance, pressure, pH, and conductivity
- **Preview the four factors** that change reaction rate (concentration, temperature, surface area, catalyst) that the rest of Unit 5 unpacks

---

## Prerequisites
- [Balancing Equations](/chemistry/0206-balancing-equations) — the stoichiometric coefficients in a balanced equation are the exact numbers we divide by in a rate expression; if the coefficients are wrong, every rate conversion is wrong
- [Graphing and Linearization](/chemistry/0105-graphing-linearization) — reaction rate literally *is* a slope on a concentration-vs-time graph, so everything you know about slope, tangent lines, and reading curves cashes out here

---

## The Core Concept

### Intuition First

Back to the phone on my charger. Let's graph what I watched. Put **time** on the horizontal axis and **battery percentage** on the vertical axis. The curve shoots up steeply at first, then bends over and flattens as it approaches 100%. That bending-over shape — steep then shallow — is the single most important picture in this entire unit.

Now here's the structural map, because in this blog the analogy always has to line up part-for-part, not just "vibe" the same:

| Phone charging | Chemical reaction |
|---|---|
| Battery percentage | **Concentration** of a species (in $\text{M}$) |
| Time on the charger | Time $t$ (in seconds) |
| How fast the % is climbing | **Reaction rate** |
| Steepness of the curve at one instant | **Instantaneous rate** (slope of the tangent) |
| Average climb between two check-ins | **Average rate** (slope of the line between two points) |
| Charging fast at the start (far to go) | Reaction fast at the start (lots of reactant) |
| Crawling near 100% (almost full) | Reaction slowing as reactant runs low |

The reason my phone slows down near the top is basically that it has less "room" left to fill. The reason a reaction slows down is the mirror image: it has less **reactant** left to consume. Same flattening curve, same story — *the rate depends on how much stuff is left, and the stuff is always running out.*

There's one twist for reactions that phones don't have. In a reaction, some things go **down** (reactants get eaten) and some things go **up** (products get made). So we can watch the curve of a reactant *falling* or the curve of a product *rising* — and both describe the same reaction happening at the same speed. My phone only had one curve (the battery filling); a reaction has a whole family of curves that all move in lockstep. Pinning down that lockstep is the technical heart of this article.

### What "Rate" Actually Means

A **reaction rate** measures how fast a concentration changes. Concentration is measured in molarity ($\text{M} = \text{mol/L}$), and we track it over time (seconds), so:

$$\text{rate} = \frac{\text{change in concentration}}{\text{change in time}} \qquad \text{units: } \frac{\text{M}}{\text{s}} = \text{mol}\,\text{L}^{-1}\,\text{s}^{-1}$$

Square brackets mean "concentration of," so $[\ce{A}]$ is read "the concentration of A." A change is written with a $\Delta$ (delta), so $\Delta[\ce{A}] = [\ce{A}]_{\text{final}} - [\ce{A}]_{\text{initial}}$.

Here's the sign problem. Consider a reactant $\ce{A}$ getting used up. Its concentration goes DOWN, so $\Delta[\ce{A}]$ is **negative**. But it feels backwards to report a "speed" as a negative number — nobody says their phone charged at $-5\%$ per minute. By universal convention, **we want the reported rate to be positive**, so we stick a minus sign in front of any reactant term to flip its negative $\Delta$ into a positive rate:

$$\text{rate (from a reactant A)} = -\frac{\Delta[\ce{A}]}{\Delta t}$$

For a **product**, concentration goes UP, so $\Delta[\ce{product}]$ is already positive — no minus sign needed:

$$\text{rate (from a product C)} = +\frac{\Delta[\ce{C}]}{\Delta t}$$

> **The one-sentence rule:** minus sign for reactants (they disappear), plus sign for products (they appear), so that the rate always comes out positive.

### The Coefficient Problem: One Reaction, One Rate

Now the part that trips up almost everyone. Take the ammonia synthesis (the Haber process — this reaction literally feeds the planet through fertilizer):

$$\ce{N2 + 3H2 -> 2NH3}$$

For every **1** $\ce{N2}$ that disappears, **3** $\ce{H2}$ disappear and **2** $\ce{NH3}$ appear. So $\ce{H2}$ vanishes three times faster than $\ce{N2}$, and $\ce{NH3}$ appears twice as fast as $\ce{N2}$ vanishes. If I just measured "$\Delta[\ce{H2}]/\Delta t$" and "$\Delta[\ce{N2}]/\Delta t$," I'd get two different numbers for the *same reaction*. That's confusing — a single reaction should have a single rate.

The fix is to **divide each species' rate by its own stoichiometric coefficient**. That rescaling cancels out the "3-for-1, 2-for-1" mismatch and forces every species to report the identical number, called the **rate of reaction**:

$$\boxed{\text{rate} = -\frac{1}{1}\frac{\Delta[\ce{N2}]}{\Delta t} = -\frac{1}{3}\frac{\Delta[\ce{H2}]}{\Delta t} = +\frac{1}{2}\frac{\Delta[\ce{NH3}]}{\Delta t}}$$

In general, for the balanced reaction

$$\ce{aA + bB -> cC + dD}$$

the unique rate of reaction is:

$$\text{rate} = -\frac{1}{a}\frac{\Delta[\ce{A}]}{\Delta t} = -\frac{1}{b}\frac{\Delta[\ce{B}]}{\Delta t} = +\frac{1}{c}\frac{\Delta[\ce{C}]}{\Delta t} = +\frac{1}{d}\frac{\Delta[\ce{D}]}{\Delta t}$$

This single chain of equalities is the workhorse of the whole topic. Read it as a **conversion machine**: if you know how fast any one species is changing, you can find how fast any other one is changing, using nothing but the balanced coefficients.

### Average, Instantaneous, and Initial Rate

These three words describe *when* you're measuring the rate, and the AP exam loves to test whether you know the difference. Lean on the phone graph.

**Average rate** is the rate over a whole interval — like asking "how fast did my phone climb from 20% to 80%?" You take the two endpoints and find the slope of the straight line connecting them (a *secant line*, if you remember that word from graphing):

$$\text{average rate} = -\frac{[\ce{A}]_{t_2} - [\ce{A}]_{t_1}}{t_2 - t_1}$$

It's a single number that smooths over everything that happened in between.

**Instantaneous rate** is the rate at one exact moment — "how fast is it charging *right now*?" On the curve, that's the slope of the **tangent line** touching the curve at that single point. (My AP Calc BC brain is very happy here: the instantaneous rate is the derivative $-\frac{d[\ce{A}]}{dt}$, the limit of the average rate as the interval shrinks to zero. You do not need calculus for AP Chem — but if you've seen it, this is exactly the tangent-slope idea wearing a lab coat.) Since the curve is steep early and shallow late, the instantaneous rate is **large at the start and shrinks over time.**

**Initial rate** is the special, most-useful instantaneous rate: the slope of the tangent **at $t = 0$**, the instant you mix everything together. Why is it the favorite? Because at $t = 0$ you know the concentrations exactly (you just made the solution), and no product has built up yet to complicate things by running the reaction backward. Almost every kinetics experiment in Unit 5 is built on measuring initial rates — hold that thought for the next article on rate laws.

### Why the Rate Falls Off

Put the pieces together. At the start, reactant concentration is at its highest, so collisions between reactant particles are most frequent, so the reaction is fastest — the concentration curve is steepest. As reactant gets consumed, there's less of it, fewer collisions happen per second, and the reaction slows — the curve bends and flattens. The tangent line goes from steep to nearly horizontal. That's the phone crawling toward 100%, and it's why **average rate over a long interval is always smaller than the initial rate**: the average includes all the sluggish late-stage behavior.

### Measuring Rates in the Lab

You can't clock a rate unless you can *watch a concentration change over time*. Chemists pick whatever property tracks concentration for a given reaction:

- **Color / absorbance** — if a reactant or product is colored, shine light through it and use a spectrophotometer; Beer's law ($A = \varepsilon b c$, from [Spectroscopy and Beer's Law](/chemistry/0508-spectroscopy-beer-lambert)) converts the absorbance reading straight into concentration at each time point. This is the cleanest method and an AP-lab favorite.
- **Pressure** — for reactions where the number of gas molecules changes, total pressure rises or falls with the mole count; a pressure gauge becomes a concentration meter.
- **pH** — if $\ce{H+}$ is produced or consumed, a pH probe tracks $[\ce{H+}]$ over time.
- **Conductivity** — if the number of dissolved ions changes, the solution's electrical conductivity changes right along with it.

The theme is always the same: find a measurable property that rides along with concentration, log it against time, and the slope gives you the rate.

### Preview: The Four Factors That Change Rate

The rest of Unit 5 is basically "what knobs speed a reaction up or slow it down?" Here's the trailer — one line each:

- **Concentration.** More reactant crammed into the same volume means more collisions per second, so faster. (This is why the reaction slows as it depletes — it's this same knob turning itself down.) The exact math becomes the **rate law**, our very next article.
- **Temperature.** Hotter particles move faster and hit harder, so a bigger fraction of collisions has enough energy to react. A rough rule of thumb: every $10\,^\circ\text{C}$ can roughly double the rate. This becomes the **Arrhenius equation** and activation energy.
- **Surface area.** For a solid reactant, only the surface is exposed to react. Grinding it into powder exposes vastly more surface — steel wool burns, a steel beam doesn't. (Same reason sawdust or flour clouds can explode.)
- **Catalyst.** A catalyst offers an easier pathway with lower activation energy and comes out unchanged at the end. It speeds the reaction without being consumed — the enzymes in your body are catalysts that let life run at $37\,^\circ\text{C}$ instead of over a Bunsen burner.

> **🎬 Hollywood Chemistry: Real or Not?**
> *The scene:* Action movies love a slow-motion shot of a single spark drifting toward a grain silo, which then detonates in a colossal fireball.
> *The verdict:* Surprisingly real — this is the surface-area factor at its most dramatic. Bulk grain barely burns, but grain *dust* suspended in air has enormous surface area exposed to oxygen, so the reaction rate skyrockets and the combustion becomes explosive. Real grain-elevator dust explosions are a genuine industrial hazard. The movie exaggerates the cinematic timing, not the chemistry.

---

## Worked Examples

**Example 1: Writing the Rate Expression from a Balanced Equation**

**Problem:** Write the full rate-of-reaction expression (in terms of every species) for
$$\ce{2N2O5 -> 4NO2 + O2}$$

**Solution:**
- *Step 1 — read the coefficients:* $\ce{N2O5}$ has 2, $\ce{NO2}$ has 4, $\ce{O2}$ has 1.
- *Step 2 — signs:* $\ce{N2O5}$ is a reactant (minus), $\ce{NO2}$ and $\ce{O2}$ are products (plus).
- *Step 3 — divide each by its coefficient:*

$$\text{rate} = -\frac{1}{2}\frac{\Delta[\ce{N2O5}]}{\Delta t} = +\frac{1}{4}\frac{\Delta[\ce{NO2}]}{\Delta t} = +\frac{1}{1}\frac{\Delta[\ce{O2}]}{\Delta t}$$

**Answer:** $\displaystyle \text{rate} = -\frac{1}{2}\frac{\Delta[\ce{N2O5}]}{\Delta t} = \frac{1}{4}\frac{\Delta[\ce{NO2}]}{\Delta t} = \frac{\Delta[\ce{O2}]}{\Delta t}$

---

**Example 2: Converting One Species' Rate into Another's (Haber Process)**

**Problem:** For $\ce{N2 + 3H2 -> 2NH3}$, $\ce{H2}$ is disappearing at $0.060\ \text{M/s}$. How fast is $\ce{NH3}$ being formed?

**Solution:**
- *Step 1 — set up the equality* between the $\ce{H2}$ term and the $\ce{NH3}$ term:
$$-\frac{1}{3}\frac{\Delta[\ce{H2}]}{\Delta t} = +\frac{1}{2}\frac{\Delta[\ce{NH3}]}{\Delta t}$$
- *Step 2 — plug in* the disappearance of $\ce{H2}$: $-\dfrac{\Delta[\ce{H2}]}{\Delta t} = 0.060\ \text{M/s}$ (the rate of *disappearance* is already positive), so $-\frac{1}{3}\frac{\Delta[\ce{H2}]}{\Delta t} = \frac{1}{3}(0.060) = 0.020\ \text{M/s}$.
- *Step 3 — solve for the $\ce{NH3}$ term:*
$$\frac{1}{2}\frac{\Delta[\ce{NH3}]}{\Delta t} = 0.020 \quad\Rightarrow\quad \frac{\Delta[\ce{NH3}]}{\Delta t} = 0.040\ \text{M/s}$$

**Answer:** $\ce{NH3}$ forms at $0.040\ \text{M/s}$. (Sanity check: $\ce{NH3}$ has coefficient 2 vs $\ce{H2}$'s 3, so it should form slower than $\ce{H2}$ vanishes — and $0.040 < 0.060$. Good.)

---

**Example 3: Ratio Shortcut for Rate Conversions**

**Problem:** For the same reaction $\ce{N2 + 3H2 -> 2NH3}$, if $\ce{N2}$ is consumed at $0.015\ \text{M/s}$, how fast are $\ce{H2}$ consumed and $\ce{NH3}$ produced?

**Solution:**
- *Step 1 — the fast way.* Rates of change scale directly with the coefficients. So take the known species' rate and multiply by (target coefficient / known coefficient).
- *Step 2 — $\ce{H2}$* has coefficient 3 vs $\ce{N2}$'s 1:
$$\text{rate of }\ce{H2}\text{ consumption} = 0.015 \times \frac{3}{1} = 0.045\ \text{M/s}$$
- *Step 3 — $\ce{NH3}$* has coefficient 2 vs $\ce{N2}$'s 1:
$$\text{rate of }\ce{NH3}\text{ formation} = 0.015 \times \frac{2}{1} = 0.030\ \text{M/s}$$

**Answer:** $\ce{H2}$ is consumed at $0.045\ \text{M/s}$; $\ce{NH3}$ is formed at $0.030\ \text{M/s}$.

---

**Example 4: Computing Average Rate from a Data Table**

**Problem:** For $\ce{A -> products}$, the following $[\ce{A}]$ was recorded:

| Time (s) | $[\ce{A}]$ (M) |
|---|---|
| 0 | 0.500 |
| 20 | 0.380 |
| 40 | 0.300 |
| 60 | 0.250 |

Find the average rate of disappearance of $\ce{A}$ over the interval $t = 0$ to $t = 40\ \text{s}$.

**Solution:**
- *Step 1 — pick the endpoints:* at $t=0$, $[\ce{A}]=0.500$; at $t=40$, $[\ce{A}]=0.300$.
- *Step 2 — compute $\Delta[\ce{A}]$ and $\Delta t$:* $\Delta[\ce{A}] = 0.300 - 0.500 = -0.200\ \text{M}$; $\Delta t = 40 - 0 = 40\ \text{s}$.
- *Step 3 — apply the minus sign* (A is a reactant):
$$\text{average rate} = -\frac{\Delta[\ce{A}]}{\Delta t} = -\frac{-0.200}{40} = 0.0050\ \text{M/s}$$

**Answer:** $0.0050\ \text{M/s}$ (i.e., $5.0 \times 10^{-3}\ \text{M/s}$).

---

**Example 5: Watching the Average Rate Shrink Over Time**

**Problem:** Using the same table from Example 4, find the average rate of disappearance of $\ce{A}$ over $t = 40$ to $t = 60\ \text{s}$, and compare it to the $0$–$20\ \text{s}$ interval.

**Solution:**
- *Step 1 — interval 40–60 s:* $\Delta[\ce{A}] = 0.250 - 0.300 = -0.050\ \text{M}$ over $\Delta t = 20\ \text{s}$:
$$-\frac{-0.050}{20} = 0.0025\ \text{M/s}$$
- *Step 2 — interval 0–20 s:* $\Delta[\ce{A}] = 0.380 - 0.500 = -0.120\ \text{M}$ over $\Delta t = 20\ \text{s}$:
$$-\frac{-0.120}{20} = 0.0060\ \text{M/s}$$
- *Step 3 — compare:* the early interval ($0.0060\ \text{M/s}$) is more than double the late interval ($0.0025\ \text{M/s}$).

**Answer:** Late-interval rate $= 0.0025\ \text{M/s}$, less than half the early $0.0060\ \text{M/s}$ — exactly the phone slowing as it fills: rate drops as reactant depletes.

---

**Example 6: Estimating Instantaneous Rate from a Tangent**

**Problem:** On a concentration-vs-time graph, the tangent line drawn to the $[\ce{A}]$ curve at $t = 30\ \text{s}$ passes through the points $(10\ \text{s},\ 0.440\ \text{M})$ and $(50\ \text{s},\ 0.280\ \text{M})$. Estimate the instantaneous rate of disappearance of $\ce{A}$ at $t = 30\ \text{s}$.

**Solution:**
- *Step 1 — the instantaneous rate is the slope of the tangent line*, so use those two points on the tangent (NOT on the curve).
- *Step 2 — slope:*
$$\text{slope} = \frac{0.280 - 0.440}{50 - 10} = \frac{-0.160}{40} = -0.0040\ \text{M/s}$$
- *Step 3 — apply the minus sign for a reactant* to report a positive rate:
$$\text{instantaneous rate} = -(-0.0040) = 0.0040\ \text{M/s}$$

**Answer:** About $0.0040\ \text{M/s}$ at $t = 30\ \text{s}$.

---

**Example 7: Relating Appearance and Disappearance Rates**

**Problem:** For $\ce{2NO + O2 -> 2NO2}$, at a certain instant $\ce{O2}$ is being consumed at $0.024\ \text{M/s}$. Find the rate of disappearance of $\ce{NO}$ and the rate of appearance of $\ce{NO2}$.

**Solution:**
- *Step 1 — write the equalities:*
$$\text{rate} = -\frac{1}{2}\frac{\Delta[\ce{NO}]}{\Delta t} = -\frac{1}{1}\frac{\Delta[\ce{O2}]}{\Delta t} = +\frac{1}{2}\frac{\Delta[\ce{NO2}]}{\Delta t}$$
- *Step 2 — anchor on $\ce{O2}$:* its rate of disappearance is $0.024\ \text{M/s}$, and its coefficient is 1, so $\text{rate} = 0.024\ \text{M/s}$.
- *Step 3 — scale by coefficients* (both $\ce{NO}$ and $\ce{NO2}$ have coefficient 2, so both change twice as fast as $\ce{O2}$):
$$\text{rate of }\ce{NO}\text{ disappearance} = 2 \times 0.024 = 0.048\ \text{M/s}$$
$$\text{rate of }\ce{NO2}\text{ appearance} = 2 \times 0.024 = 0.048\ \text{M/s}$$

**Answer:** $\ce{NO}$ disappears at $0.048\ \text{M/s}$; $\ce{NO2}$ appears at $0.048\ \text{M/s}$.

---

**Example 8: Back-Solving for a Coefficient's Effect**

**Problem:** In the reaction $\ce{2A + B -> 3C}$, $\ce{C}$ is being produced at $0.90\ \text{M/s}$. How fast is $\ce{A}$ being consumed?

**Solution:**
- *Step 1 — equality between $\ce{A}$ and $\ce{C}$:*
$$-\frac{1}{2}\frac{\Delta[\ce{A}]}{\Delta t} = +\frac{1}{3}\frac{\Delta[\ce{C}]}{\Delta t}$$
- *Step 2 — plug in* the $\ce{C}$ formation rate ($\frac{\Delta[\ce{C}]}{\Delta t} = 0.90\ \text{M/s}$):
$$-\frac{1}{2}\frac{\Delta[\ce{A}]}{\Delta t} = \frac{1}{3}(0.90) = 0.30\ \text{M/s}$$
- *Step 3 — solve for the disappearance rate of $\ce{A}$* (which is $-\frac{\Delta[\ce{A}]}{\Delta t}$):
$$-\frac{\Delta[\ce{A}]}{\Delta t} = 2 \times 0.30 = 0.60\ \text{M/s}$$

**Answer:** $\ce{A}$ is consumed at $0.60\ \text{M/s}$.

---

**Example 9: Rate of Reaction vs Rate of a Species**

**Problem:** For $\ce{2HI -> H2 + I2}$, $\ce{HI}$ disappears at $0.040\ \text{M/s}$. What is the **rate of reaction**?

**Solution:**
- *Step 1 — recall* the rate of reaction divides each species' rate by its coefficient. For $\ce{HI}$ (coefficient 2):
$$\text{rate of reaction} = -\frac{1}{2}\frac{\Delta[\ce{HI}]}{\Delta t}$$
- *Step 2 — the disappearance rate of $\ce{HI}$ is* $-\frac{\Delta[\ce{HI}]}{\Delta t} = 0.040\ \text{M/s}$, so:
$$\text{rate of reaction} = \frac{1}{2}(0.040) = 0.020\ \text{M/s}$$

**Answer:** The rate of reaction is $0.020\ \text{M/s}$ — half the rate at which $\ce{HI}$ disappears. Note $\ce{H2}$ and $\ce{I2}$ each appear at $0.020\ \text{M/s}$ too (coefficient 1), which equals the reaction rate.

---

**Example 10: Finding a Concentration Change Over Time**

**Problem:** For $\ce{2N2O5 -> 4NO2 + O2}$, the reaction proceeds at a rate of $1.5 \times 10^{-3}\ \text{M/s}$ (the rate of reaction). If this rate held roughly constant for $10.0\ \text{s}$, how much would $[\ce{NO2}]$ increase?

**Solution:**
- *Step 1 — relate rate of reaction to $\ce{NO2}$:* $\text{rate} = +\frac{1}{4}\frac{\Delta[\ce{NO2}]}{\Delta t}$, so $\frac{\Delta[\ce{NO2}]}{\Delta t} = 4 \times \text{rate} = 4(1.5\times10^{-3}) = 6.0\times10^{-3}\ \text{M/s}$.
- *Step 2 — multiply by the time interval:*
$$\Delta[\ce{NO2}] = (6.0\times10^{-3}\ \text{M/s})(10.0\ \text{s}) = 6.0\times10^{-2}\ \text{M}$$

**Answer:** $[\ce{NO2}]$ rises by about $0.060\ \text{M}$. (In reality the rate drops as reactant depletes, so this is an over-estimate — a good reason initial rates and short intervals are preferred.)

---

**Example 11: Reading Which Curve Is Steeper**

**Problem:** For $\ce{N2 + 3H2 -> 2NH3}$, three curves are plotted on one concentration-vs-time graph: $[\ce{N2}]$, $[\ce{H2}]$, and $[\ce{NH3}]$. Two fall and one rises. Which falling curve is steeper, and why?

**Solution:**
- *Step 1 — identify the fallers:* $\ce{N2}$ and $\ce{H2}$ are reactants (falling); $\ce{NH3}$ rises.
- *Step 2 — compare their rates of change* using coefficients: $\ce{H2}$ disappears 3× as fast as $\ce{N2}$ (coefficients 3 vs 1).
- *Step 3 — steeper slope = faster change:* the $\ce{H2}$ curve is three times as steep (falling) as the $\ce{N2}$ curve.

**Answer:** The $\ce{H2}$ curve is steepest of the two fallers, dropping 3× faster than $\ce{N2}$; the rising $\ce{NH3}$ curve climbs 2× as fast as $\ce{N2}$ falls.

---

**Example 12: Average Rate for a Species with a Coefficient**

**Problem:** For $\ce{2NOBr -> 2NO + Br2}$, $[\ce{NOBr}]$ drops from $0.0100\ \text{M}$ to $0.0072\ \text{M}$ between $t = 0$ and $t = 40\ \text{s}$. Find (a) the average rate of disappearance of $\ce{NOBr}$ and (b) the average rate of reaction.

**Solution:**
- *Step 1 — (a) disappearance of $\ce{NOBr}$:*
$$-\frac{\Delta[\ce{NOBr}]}{\Delta t} = -\frac{0.0072 - 0.0100}{40} = -\frac{-0.0028}{40} = 7.0\times10^{-5}\ \text{M/s}$$
- *Step 2 — (b) rate of reaction* divides by the coefficient of $\ce{NOBr}$ (which is 2):
$$\text{rate of reaction} = \frac{1}{2}(7.0\times10^{-5}) = 3.5\times10^{-5}\ \text{M/s}$$

**Answer:** (a) $7.0\times10^{-5}\ \text{M/s}$; (b) $3.5\times10^{-5}\ \text{M/s}$.

---

## Common Mistakes

| The mistake | Why it happens | How to avoid it |
|---|---|---|
| **Forgetting the $\frac{1}{\text{coefficient}}$ factor** | Students write $\text{rate} = -\frac{\Delta[\ce{H2}]}{\Delta t}$ instead of $-\frac{1}{3}\frac{\Delta[\ce{H2}]}{\Delta t}$ | Always divide each term by that species' coefficient. If the coefficient is 1, dividing changes nothing — but write it anyway so you never forget. |
| **Dropping (or double-counting) the minus sign** | Reactant $\Delta$ is negative; students either report a negative rate or add a minus sign to a product too | Minus for reactants, plus for products. The final reported rate should be **positive**. |
| **Confusing average with instantaneous** | Both are "slopes," so they blur together | Average = slope of the line **between two points**; instantaneous = slope of the **tangent** at one point. Two points → average; one point → tangent. |
| **Using points on the curve to find an instantaneous rate** | The tangent looks close to the curve | For an instantaneous rate, read two points that lie **on the drawn tangent line**, not on the curve itself. |
| **Assuming rate is constant** | The formula looks like it gives one number | Rate falls as reactant depletes (the flattening curve). An average rate is only an approximation over an interval; the true rate is highest at $t=0$. |
| **Wrong or missing units** | Forgetting concentration is per liter and time is per second | Reaction rate is always $\text{M/s} = \text{mol}\,\text{L}^{-1}\,\text{s}^{-1}$. Write the units every time. |
| **Mixing up "rate of a species" and "rate of reaction"** | They differ by exactly the coefficient factor | The *rate of reaction* is the single number all species agree on after dividing by coefficients; the *rate of a species* is that species' own $\Delta/\Delta t$. |

---

## AP Exam Tips

- **The $\frac{1}{\text{coefficient}}$ factor and the signs are a guaranteed trap.** Nearly every rate question hinges on correctly writing $-\frac{1}{a}\frac{\Delta[\ce{A}]}{\Delta t} = +\frac{1}{c}\frac{\Delta[\ce{C}]}{\Delta t}$. Set up that equality FIRST, before plugging in numbers, and points take care of themselves.
- **Know average vs instantaneous vs initial cold.** If a question gives you two data points (a table), it wants an **average** rate. If it references a tangent line or "at this instant" or "at $t=0$," it wants an **instantaneous** (or **initial**) rate. The initial rate is the instantaneous rate at $t=0$ and is the one used to build rate laws (next unit).
- **Reading rates off graphs is a classic FRQ skill.** For an instantaneous rate, they may ask you to *draw a tangent line* and compute its slope — pick two clearly-readable points **on your tangent**, and remember the minus sign for a reactant. Steeper curve = faster rate.
- **Units are free points and a free error.** Reaction rate is $\text{M/s}$. If your answer comes out in $\text{mol/s}$ or $\text{M}$, you dropped a liter or a second somewhere — go back.
- **Watch the direction of the arrow in a table.** A reactant concentration should *decrease* down the table; a product should *increase*. If you're computing a rate and get a negative number for a "rate," you probably forgot the sign convention.
- **Rate of reaction is always positive** and is the same for the whole reaction. Reporting a negative rate loses the point even if the magnitude is right.

---

## Practice Problems

### Problem 1
Write the complete rate-of-reaction expression for $\ce{4NH3 + 5O2 -> 4NO + 6H2O}$.

<details>
<summary><strong>Solution</strong></summary>

Divide each term by its coefficient; minus for reactants, plus for products:
$$\text{rate} = -\frac{1}{4}\frac{\Delta[\ce{NH3}]}{\Delta t} = -\frac{1}{5}\frac{\Delta[\ce{O2}]}{\Delta t} = +\frac{1}{4}\frac{\Delta[\ce{NO}]}{\Delta t} = +\frac{1}{6}\frac{\Delta[\ce{H2O}]}{\Delta t}$$

**Answer:** the boxed expression above.

</details>

---

### Problem 2
For $\ce{N2 + 3H2 -> 2NH3}$, $\ce{N2}$ is consumed at $0.010\ \text{M/s}$. How fast is $\ce{H2}$ consumed?

<details>
<summary><strong>Solution</strong></summary>

$\ce{H2}$ (coefficient 3) changes 3× as fast as $\ce{N2}$ (coefficient 1):
$$0.010 \times \frac{3}{1} = 0.030\ \text{M/s}$$

**Answer:** $0.030\ \text{M/s}$.

</details>

---

### Problem 3
For $\ce{2SO2 + O2 -> 2SO3}$, $\ce{SO3}$ forms at $0.048\ \text{M/s}$. Find the rate of consumption of $\ce{O2}$.

<details>
<summary><strong>Solution</strong></summary>

$$-\frac{1}{1}\frac{\Delta[\ce{O2}]}{\Delta t} = +\frac{1}{2}\frac{\Delta[\ce{SO3}]}{\Delta t} = \frac{1}{2}(0.048) = 0.024\ \text{M/s}$$

**Answer:** $\ce{O2}$ is consumed at $0.024\ \text{M/s}$.

</details>

---

### Problem 4
A reactant $\ce{X}$ drops from $0.750\ \text{M}$ to $0.510\ \text{M}$ over $30.0\ \text{s}$ in $\ce{X -> products}$. Find the average rate of disappearance of $\ce{X}$.

<details>
<summary><strong>Solution</strong></summary>

$$-\frac{\Delta[\ce{X}]}{\Delta t} = -\frac{0.510 - 0.750}{30.0} = -\frac{-0.240}{30.0} = 8.0\times10^{-3}\ \text{M/s}$$

**Answer:** $8.0\times10^{-3}\ \text{M/s}$.

</details>

---

### Problem 5
Using the table below for $\ce{A -> B}$, find the average rate of appearance of $\ce{B}$ from $t = 0$ to $t = 50\ \text{s}$.

| Time (s) | $[\ce{B}]$ (M) |
|---|---|
| 0 | 0.000 |
| 50 | 0.180 |
| 100 | 0.290 |

<details>
<summary><strong>Solution</strong></summary>

$\ce{B}$ is a product (plus sign, and $\Delta$ is already positive):
$$+\frac{\Delta[\ce{B}]}{\Delta t} = \frac{0.180 - 0.000}{50} = 3.6\times10^{-3}\ \text{M/s}$$

**Answer:** $3.6\times10^{-3}\ \text{M/s}$.

</details>

---

### Problem 6
Using the same table in Problem 5, find the average rate of appearance of $\ce{B}$ from $t = 50$ to $t = 100\ \text{s}$, and state whether the reaction sped up or slowed down.

<details>
<summary><strong>Solution</strong></summary>

$$\frac{0.290 - 0.180}{100 - 50} = \frac{0.110}{50} = 2.2\times10^{-3}\ \text{M/s}$$

This is smaller than the $3.6\times10^{-3}\ \text{M/s}$ from the first interval.

**Answer:** $2.2\times10^{-3}\ \text{M/s}$; the reaction **slowed down** as reactant depleted (the phone crawling toward full).

</details>

---

### Problem 7
On a $[\ce{A}]$-vs-time graph, the tangent at $t = 25\ \text{s}$ passes through $(5\ \text{s},\ 0.600\ \text{M})$ and $(45\ \text{s},\ 0.360\ \text{M})$. Find the instantaneous rate of disappearance of $\ce{A}$ at $t = 25\ \text{s}$.

<details>
<summary><strong>Solution</strong></summary>

Slope of the tangent:
$$\frac{0.360 - 0.600}{45 - 5} = \frac{-0.240}{40} = -6.0\times10^{-3}\ \text{M/s}$$
Apply the minus sign for a reactant:
$$-(-6.0\times10^{-3}) = 6.0\times10^{-3}\ \text{M/s}$$

**Answer:** $6.0\times10^{-3}\ \text{M/s}$.

</details>

---

### Problem 8
For $\ce{2N2O5 -> 4NO2 + O2}$, $\ce{O2}$ appears at $2.5\times10^{-4}\ \text{M/s}$. Find the rate of disappearance of $\ce{N2O5}$ and the rate of appearance of $\ce{NO2}$.

<details>
<summary><strong>Solution</strong></summary>

Rate of reaction $= +\frac{1}{1}\frac{\Delta[\ce{O2}]}{\Delta t} = 2.5\times10^{-4}\ \text{M/s}$.

$\ce{N2O5}$ (coeff 2): $-\frac{\Delta[\ce{N2O5}]}{\Delta t} = 2 \times 2.5\times10^{-4} = 5.0\times10^{-4}\ \text{M/s}$.

$\ce{NO2}$ (coeff 4): $+\frac{\Delta[\ce{NO2}]}{\Delta t} = 4 \times 2.5\times10^{-4} = 1.0\times10^{-3}\ \text{M/s}$.

**Answer:** $\ce{N2O5}$ disappears at $5.0\times10^{-4}\ \text{M/s}$; $\ce{NO2}$ appears at $1.0\times10^{-3}\ \text{M/s}$.

</details>

---

### Problem 9
For $\ce{H2 + I2 -> 2HI}$, the rate of reaction at some instant is $0.012\ \text{M/s}$. How fast is $\ce{HI}$ being produced?

<details>
<summary><strong>Solution</strong></summary>

$$\text{rate} = +\frac{1}{2}\frac{\Delta[\ce{HI}]}{\Delta t} \quad\Rightarrow\quad \frac{\Delta[\ce{HI}]}{\Delta t} = 2 \times 0.012 = 0.024\ \text{M/s}$$

**Answer:** $\ce{HI}$ forms at $0.024\ \text{M/s}$.

</details>

---

### Problem 10
For $\ce{2NOBr -> 2NO + Br2}$, $\ce{NO}$ is produced at $0.016\ \text{M/s}$. Find the rate of production of $\ce{Br2}$.

<details>
<summary><strong>Solution</strong></summary>

$$+\frac{1}{2}\frac{\Delta[\ce{NO}]}{\Delta t} = +\frac{1}{1}\frac{\Delta[\ce{Br2}]}{\Delta t}$$
$$\frac{\Delta[\ce{Br2}]}{\Delta t} = \frac{1}{2}(0.016) = 0.0080\ \text{M/s}$$

**Answer:** $\ce{Br2}$ forms at $8.0\times10^{-3}\ \text{M/s}$ (half the $\ce{NO}$ rate, since $\ce{Br2}$'s coefficient is half of $\ce{NO}$'s).

</details>

---

### Problem 11
A student measures the initial rate of a reaction as $0.050\ \text{M/s}$ and the average rate over the first two minutes as $0.020\ \text{M/s}$. Explain why the two differ, and which is larger.

<details>
<summary><strong>Solution</strong></summary>

The **initial rate** ($0.050\ \text{M/s}$) is measured at $t=0$ when reactant concentration is highest, so the reaction is fastest. Over the next two minutes reactant depletes and the rate falls, so the **average** rate ($0.020\ \text{M/s}$) — which folds in all that slower late-stage behavior — is smaller.

**Answer:** The initial rate is larger; the average is smaller because rate decreases as reactant is consumed (the flattening curve).

</details>

---

### Problem 12
For $\ce{2A + 3B -> C}$, $\ce{B}$ disappears at $0.090\ \text{M/s}$. Find (a) the rate of reaction and (b) the rate of disappearance of $\ce{A}$.

<details>
<summary><strong>Solution</strong></summary>

(a) Rate of reaction $= -\frac{1}{3}\frac{\Delta[\ce{B}]}{\Delta t} = \frac{1}{3}(0.090) = 0.030\ \text{M/s}$.

(b) $\ce{A}$ (coeff 2): $-\frac{\Delta[\ce{A}]}{\Delta t} = 2 \times 0.030 = 0.060\ \text{M/s}$. (Or directly: $\ce{A}$ changes $\frac{2}{3}$ as fast as $\ce{B}$: $0.090 \times \frac{2}{3} = 0.060$.)

**Answer:** (a) $0.030\ \text{M/s}$; (b) $\ce{A}$ disappears at $0.060\ \text{M/s}$.

</details>

---

### Problem 13
Which experimental method would best track the rate of $\ce{CaCO3(s) + 2HCl(aq) -> CaCl2(aq) + H2O(l) + CO2(g)}$, and why?

<details>
<summary><strong>Solution</strong></summary>

$\ce{CO2}$ gas is produced, so the number of gas molecules (and thus the pressure in a closed vessel, or the mass lost from an open flask as gas escapes) changes over time. Monitoring **pressure** (or mass loss) tracks the reaction. A **pH** probe would also work, since $\ce{HCl}$ (acid) is consumed and $[\ce{H+}]$ falls.

**Answer:** Pressure/gas-volume (or mass loss) is ideal because a gas is produced; pH also works because acid is consumed. Color/absorbance is a poor fit here since none of the species is strongly colored.

</details>

---

### Problem 14
For $\ce{4Fe + 3O2 -> 2Fe2O3}$, $\ce{Fe}$ is consumed at $1.2\times10^{-3}\ \text{M/s}$. Find the rate of consumption of $\ce{O2}$ and the rate of formation of $\ce{Fe2O3}$.

<details>
<summary><strong>Solution</strong></summary>

Rate of reaction $= \frac{1}{4}(1.2\times10^{-3}) = 3.0\times10^{-4}\ \text{M/s}$.

$\ce{O2}$ (coeff 3): $3 \times 3.0\times10^{-4} = 9.0\times10^{-4}\ \text{M/s}$.

$\ce{Fe2O3}$ (coeff 2): $2 \times 3.0\times10^{-4} = 6.0\times10^{-4}\ \text{M/s}$.

**Answer:** $\ce{O2}$ consumed at $9.0\times10^{-4}\ \text{M/s}$; $\ce{Fe2O3}$ formed at $6.0\times10^{-4}\ \text{M/s}$.

</details>

---

### Problem 15
A reaction $\ce{A -> products}$ has $[\ce{A}]$ falling as: $t=0\text{ s} \to 1.00\ \text{M}$, $t=10\text{ s} \to 0.60\ \text{M}$, $t=20\text{ s} \to 0.36\ \text{M}$, $t=30\text{ s} \to 0.22\ \text{M}$. Compute the average rate over each 10-second interval and describe the trend in words, connecting it to the phone analogy.

<details>
<summary><strong>Solution</strong></summary>

- $0$–$10\ \text{s}$: $-\frac{0.60-1.00}{10} = 0.040\ \text{M/s}$
- $10$–$20\ \text{s}$: $-\frac{0.36-0.60}{10} = 0.024\ \text{M/s}$
- $20$–$30\ \text{s}$: $-\frac{0.22-0.36}{10} = 0.014\ \text{M/s}$

The rate keeps dropping ($0.040 \to 0.024 \to 0.014\ \text{M/s}$) as $\ce{A}$ depletes.

**Answer:** The average rate falls each interval — exactly like the phone charging fast at first (lots of reactant / far to go) and crawling as it runs low (little reactant / nearly full). Fewer $\ce{A}$ particles means fewer collisions per second, so the reaction slows.

</details>

---

## Quick Reference

| Concept | Formula / Rule | Notes |
|---|---|---|
| Reaction rate (general) | $\text{rate} = \dfrac{\Delta[\text{species}]}{\Delta t}$ | Units always $\text{M/s}$ |
| Reactant term | $-\dfrac{\Delta[\ce{reactant}]}{\Delta t}$ | Minus sign keeps rate positive |
| Product term | $+\dfrac{\Delta[\ce{product}]}{\Delta t}$ | Already positive |
| Rate of reaction for $\ce{aA + bB -> cC + dD}$ | $-\dfrac{1}{a}\dfrac{\Delta[\ce{A}]}{\Delta t} = -\dfrac{1}{b}\dfrac{\Delta[\ce{B}]}{\Delta t} = +\dfrac{1}{c}\dfrac{\Delta[\ce{C}]}{\Delta t} = +\dfrac{1}{d}\dfrac{\Delta[\ce{D}]}{\Delta t}$ | Divide each by its coefficient — one number for the whole reaction |
| Convert species rates | (rate of X) $= $ (rate of Y) $\times \dfrac{\text{coeff of X}}{\text{coeff of Y}}$ | Fast shortcut |
| Average rate | slope of the line between two points | Needs two $(t, [\,])$ points |
| Instantaneous rate | slope of the **tangent** at one point | One point; read two points *on the tangent* |
| Initial rate | instantaneous rate at $t = 0$ | Most useful; basis of rate laws |
| Why rate falls | reactant depletes → fewer collisions | The flattening curve |
| Measuring rates | color/absorbance, pressure, pH, conductivity | Pick the property that tracks concentration |
| Four factors (Unit 5 preview) | concentration, temperature, surface area, catalyst | Each speeds reactions up |

---

<div align="center">

[← Redox Reactions](/chemistry/0606-redox-reactions) | [Rate Laws →](/chemistry/0702-rate-laws)

</div>
