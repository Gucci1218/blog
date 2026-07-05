# Graphing and Linearization
<p class="article-date">July 4, 2026</p>

*I stayed up past midnight last month watching a rocket launch livestream — you know the little altitude and speed readouts climbing in the corner of the screen? Altitude vs time is this swooping curve, and staring at it I realized I had no idea whether the rocket was healthy. Is that curve too shallow? Too steep? Who can tell? Then a flight controller on the stream mentioned that mission control barely looks at that plot — they watch transformed versions where a nominal flight is a dead-straight line, because a line is the only shape a human can check at a glance, and its slope is a real physical number: burn rate, acceleration, fuel margin. (Mark Watney does the same thing in The Martian, plotting sols against potatoes remaining — the x-intercept is literally the day he starves.) That idea is this entire article. Nature almost never hands you a straight line — it hands you curves. But a line is the only shape you can summarize with just two numbers, slope and intercept, and read instantly. So chemists (and flight controllers, and stranded astronauts) play the same game: transform the axes until the truth becomes a line. In AP Chemistry this trick decides reaction orders in kinetics, finds concentrations with Beer's law, and extracts activation energies from Arrhenius plots. If you own $y = mx + b$ — and after a 5 on Calc BC, tangent-line thinking is basically my home address — you already own the hardest part.*

---

## What You'll Learn
- Read a chemistry graph the professional way: axis labels **with units**, slope **with units**, and an intercept that means something physical
- Compute the slope of a line from two points and attach the correct units ($\Delta y$ units per $\Delta x$ units)
- Draw and use a **best-fit line** instead of connecting the dots, and explain why
- Tell **interpolation** (safe) from **extrapolation** (risky) and know when each is allowed
- Recognize direct proportionality ($y = mx$) and inverse proportionality ($y = k/x$) from both a data table and a plot
- Linearize an inverse relationship by plotting $y$ vs $1/x$ (Boyle's law preview)
- Use the kinetics linearization table to decide reaction order from which plot is straight — $[\ce{A}]$ vs $t$, $\ln[\ce{A}]$ vs $t$, or $1/[\ce{A}]$ vs $t$ — and extract $k$ from the slope (Unit 5 preview)
- Read Beer's law calibration plots (absorbance vs concentration) to find unknown concentrations
- Interpret the statement "the graph of $\ln k$ vs $1/T$ is linear" without fear (Arrhenius teaser)

---

## Prerequisites
- [Dimensional Analysis](/chemistry/0103-dimensional-analysis) — slopes carry units, and you'll build them exactly the way you build conversion factors
- [Logarithms for Chemistry](/chemistry/0104-logarithms-for-chemistry) — the most important linearizations in AP Chem run through $\ln$, so you need to be comfortable taking logs of concentrations and rate constants

---

## The Core Concept

### Intuition First

Back to that launch stream. Why does mission control want a *line* so badly? Because a curve is a paragraph and a line is a sentence. To describe a curve you need the whole curve — every point matters. To describe a line you need exactly two numbers:

$$y = mx + b$$

The slope $m$ and the intercept $b$. That's it. And here's the part nobody tells you in algebra class: **in science, $m$ and $b$ are not just numbers — they are measurements.** The slope of mission control's transformed telemetry *is* the rocket's burn rate. The slope of a mass-vs-volume plot *is* the density. The slope of a $\ln[\ce{A}]$-vs-time plot *is* $-k$, the rate constant of a reaction. When you linearize data, you're not doing graph cosmetics; you're building a machine whose slope spits out a physical constant.

You already own this idea from calculus. A tangent line is the statement "zoomed in far enough, everything is $y = mx + b$." Linearization is the chemistry remix: instead of zooming in, we **change the variables on the axes** until the whole data set — not just a neighborhood — obeys $y = mx + b$. Same worship of the straight line, different trick to get there.

So the game has two moves, and the whole article is just these two moves practiced over and over:

1. **If the plot is curved, transform an axis** ($x \to 1/x$, $y \to \ln y$, $y \to 1/y$...) until it's straight.
2. **Once it's straight, read the slope and intercept — with units — and translate them into chemistry.**

### Reading a Graph Like a Chemist

Every graph you draw or read in AP Chemistry must have three things, and graders genuinely check all three:

1. **Axis labels with units.** Not "volume" — "$V$ (L)". Not "concentration" — "$[\ce{A}]$ (M)".
2. **A slope with units.** Slope is $\dfrac{\Delta y}{\Delta x}$, so its units are literally $\dfrac{\text{units of } y}{\text{units of } x}$. A slope of "2.7" is meaningless; a slope of $2.7~\text{g/mL}$ is a density.
3. **An intercept with a meaning.** The $y$-intercept is the value of $y$ when $x = 0$. Sometimes that's physically meaningful (initial concentration at $t = 0$), sometimes it's a red flag (a mass-vs-volume line that doesn't pass through the origin suggests a systematic error — maybe you forgot to zero the balance).

**Computing slope from two points.** Pick two points **on the best-fit line** (not two raw data points!), as far apart as practical:

$$m = \frac{y_2 - y_1}{x_2 - x_1}$$

Then attach units. Always. Every time. No exceptions.

### Best-Fit Line vs Connect-the-Dots

Real data has scatter — even a rocket's telemetry points never sit *exactly* on the nominal line; they buzz around it like flies, and lab measurements are worse. A **best-fit line** is a single straight line drawn so the points are balanced above and below it. Connecting the dots point-to-point produces a jagged zigzag that treats measurement noise as if it were real chemistry. It isn't.

- **Best-fit line:** smooths out random error; its slope is your best estimate of the true physical constant. ✓
- **Connect-the-dots:** memorializes your random error forever. ✗

Two related words:

- **Interpolation** — reading a value *between* your measured points, off the best-fit line. Generally safe: the line is well-supported there.
- **Extrapolation** — extending the line *beyond* your data and reading values out there. Risky: you're betting the relationship stays linear where you never looked. (A rocket's speed climbs on a beautiful line... right up until stage separation, where the physics changes completely and the old line becomes a lie. Extrapolate across that boundary and mission control would be predicting nonsense.)

### Direct vs Inverse Proportionality

Two relationships dominate intro chemistry, and you should recognize each on sight — from a table *or* a plot.

**Direct proportionality:** $y = mx$. Double $x$, double $y$. The test on a data table: $y/x$ is constant. The plot: a straight line **through the origin**.

**Inverse proportionality:** $y = \dfrac{k}{x}$. Double $x$, halve $y$. The test: the *product* $xy$ is constant. The plot: a hyperbola that hugs both axes and never touches either.

Here's the classic example, and a preview of Unit 3: for a fixed amount of gas at constant temperature, pressure and volume are inversely proportional (**Boyle's law**, $PV = \text{constant}$). Plot $P$ vs $V$ and you get an unreadable curve. But rewrite $P = k \cdot \dfrac{1}{V}$: that's $y = mx$ with $x = 1/V$. Plot $P$ vs $1/V$ and the data snaps to a straight line through the origin whose slope is the constant $k$ — units and all.

```text
   P (atm)                          P (atm)
    |*                               |            *
    | *                              |         *
    |  *                             |      *
    |    *                           |   *
    |       *   *                    |*
    +---------------- V (L)          +---------------- 1/V (L⁻¹)
      curve: hard to read              LINE: slope = PV constant
```

Same data. Different axis. Truth becomes readable.

### The Linearization Playbook (Kinetics Preview)

This is THE table of AP Chemistry Unit 5, and I'm showing it to you now — months early — because it is nothing but the axis-transformation game. When a reactant $\ce{A}$ disappears over time, the *shape* of the decay tells you the **reaction order**, and the way you detect the shape is to try three plots and see which one is straight:

| Order | Straight-line plot | Slope | Slope units (typical) |
|:---:|:---:|:---:|:---:|
| 0 | $[\ce{A}]$ vs $t$ | $-k$ | $\text{M/s}$ |
| 1 | $\ln[\ce{A}]$ vs $t$ | $-k$ | $\text{s}^{-1}$ |
| 2 | $1/[\ce{A}]$ vs $t$ | $k$ | $\text{M}^{-1}\text{s}^{-1}$ |

Read it as three rounds of the same game:

- **Zero order:** the raw data itself is already a line. $[\ce{A}]$ drops by the same *amount* every second. Slope is negative, and $k$ is its absolute value.
- **First order:** the raw data curves, but $\ln[\ce{A}]$ vs $t$ is a line. $[\ce{A}]$ drops by the same *factor* in equal times — the halving-forever behavior, which is exactly why first-order reactions have a constant half-life. (This is where [Logarithms for Chemistry](/chemistry/0104-logarithms-for-chemistry) pays rent: logs turn "multiply by the same factor" into "subtract the same amount," and constant subtraction *is* a line.)
- **Second order:** neither of those works, but $1/[\ce{A}]$ vs $t$ is a line — and this is the only one of the three with a **positive** slope, because as $[\ce{A}]$ shrinks, $1/[\ce{A}]$ grows.

You don't need to know *why* these work yet (that's Unit 5, and honestly a little calculus). You need the skill: **given a data table, transform, test for straightness, name the order, read $k$ from the slope — with units.**

A quick numerical straightness test, since you won't always have graph paper: on a straight line, **equal steps in $x$ produce equal steps in $y$.** Compute the differences down the transformed column; if they're constant, that plot is linear.

### Beer's Law Preview: Chemistry's Favorite Straight Line

In the spectrophotometry labs (Unit 1), you'll shine light through colored solutions and measure **absorbance** $A$. Beer's law says

$$A = \varepsilon b c$$

where $c$ is molar concentration, $b$ is the path length of the cuvette, and $\varepsilon$ is a constant for the compound. Look at the shape: $A = (\varepsilon b)\,c$ is $y = mx$ — a straight line through the origin, no transformation needed. Nature occasionally hands you a freebie. You measure absorbance for a few known concentrations (a **calibration curve**, which despite the name should be a *line*), fit the line, then use it in reverse: measure $A$ for your unknown, and interpolate its concentration. This is the single most common graph in AP Chem lab questions.

### Arrhenius Teaser: One More Transformed Line

One sentence you'll meet in Unit 5: *"the graph of $\ln k$ vs $1/T$ is linear."* Decode it with the playbook. Someone measured the rate constant $k$ at several temperatures $T$, found the raw plot hopelessly curved, and discovered that transforming **both** axes — $\ln$ on the $y$, reciprocal on the $x$ — produces a straight line:

$$\ln k = \underbrace{-\frac{E_a}{R}}_{\text{slope}} \cdot \frac{1}{T} + \underbrace{\ln A}_{\text{intercept}}$$

The slope of that line equals $-E_a/R$, so a graph hands you the **activation energy** of a reaction. No derivation now — just recognize the move: it's the same game, played with two transformations at once.

---

## Worked Examples

### Example 1: Slope With Units Is a Density

**Problem:** A student measures the mass of different volumes of a metal. The best-fit line of mass (g) vs volume (mL) passes through $(2.0~\text{mL}, 5.4~\text{g})$ and $(10.0~\text{mL}, 27.0~\text{g})$. Find the slope, with units, and interpret it.

**Solution:**

**Step 1:** Apply the slope formula with the units riding along:

$$m = \frac{27.0~\text{g} - 5.4~\text{g}}{10.0~\text{mL} - 2.0~\text{mL}} = \frac{21.6~\text{g}}{8.0~\text{mL}} = 2.7~\text{g/mL}$$

**Step 2:** Interpret. Grams per milliliter is mass per volume — that's a **density**. (And $2.7~\text{g/mL}$ happens to be aluminum.)

**Answer:** Slope $= 2.7~\text{g/mL}$; it is the density of the metal, likely aluminum.

### Example 2: The Intercept Has Meaning Too

**Problem:** The same experiment, done sloppily, gives a best-fit line $\text{mass} = (2.7~\text{g/mL})V + 1.5~\text{g}$. What does the intercept of $1.5~\text{g}$ suggest?

**Solution:**

**Step 1:** The intercept is the mass when $V = 0$. Zero metal should have zero mass, so physically the line *must* pass through the origin.

**Step 2:** A nonzero intercept therefore signals a **systematic error** — every reading shifted by the same amount. The classic culprit: the balance wasn't tared (zeroed), or the metal was weighed in a container whose mass never got subtracted.

**Answer:** All mass readings are offset by about $1.5~\text{g}$ — a systematic error such as an untared balance. The slope (density) is still trustworthy, because a constant offset doesn't change $\Delta y / \Delta x$.

### Example 3: Interpolation From a Best-Fit Line

**Problem:** Solubility of a salt vs temperature gives a nice best-fit line through $(20.0~\text{°C}, 34.0~\text{g}/100~\text{g}~\ce{H2O})$ and $(60.0~\text{°C}, 50.0~\text{g}/100~\text{g}~\ce{H2O})$. Estimate the solubility at $35.0~\text{°C}$.

**Solution:**

**Step 1:** Slope: $\dfrac{50.0 - 34.0}{60.0 - 20.0} = \dfrac{16.0}{40.0} = 0.400~\dfrac{\text{g}/100~\text{g}~\ce{H2O}}{\text{°C}}$.

**Step 2:** March from the known point: $35.0~\text{°C}$ is $15.0~\text{°C}$ above $20.0~\text{°C}$.

$$34.0 + (0.400)(15.0) = 34.0 + 6.0 = 40.0$$

**Step 3:** Sanity check: $35.0~\text{°C}$ is *between* measured temperatures, so this is interpolation — safe.

**Answer:** About $40.0~\text{g}$ per $100~\text{g}$ $\ce{H2O}$.

### Example 4: Direct or Inverse? Test the Table

**Problem:** For a fixed amount of gas at constant temperature:

| $V$ (L) | 1.00 | 2.00 | 4.00 | 5.00 |
|---|---|---|---|---|
| $P$ (atm) | 4.00 | 2.00 | 1.00 | 0.800 |

Is $P$ directly or inversely proportional to $V$? Prove it with the table.

**Solution:**

**Step 1:** Test direct proportionality — is $P/V$ constant? $4.00/1.00 = 4.00$; $2.00/2.00 = 1.00$. Not constant. ✗

**Step 2:** Test inverse proportionality — is $PV$ constant?

$$ (4.00)(1.00) = 4.00 \quad (2.00)(2.00) = 4.00 \quad (1.00)(4.00) = 4.00 \quad (0.800)(5.00) = 4.00 ~\text{L·atm}$$

Constant! ✓

**Answer:** Inversely proportional: $PV = 4.00~\text{L·atm}$ (Boyle's law behavior).

### Example 5: Linearizing Boyle's Law

**Problem:** Using the data from Example 4, what should you plot to get a straight line, and what is its slope (with units)?

**Solution:**

**Step 1:** $P = \dfrac{4.00}{V}$ has the form $y = m \cdot \dfrac{1}{x}$, so plot $P$ (y-axis) vs $1/V$ (x-axis).

**Step 2:** Build the transformed column:

| $1/V$ (L⁻¹) | 1.00 | 0.500 | 0.250 | 0.200 |
|---|---|---|---|---|
| $P$ (atm) | 4.00 | 2.00 | 1.00 | 0.800 |

**Step 3:** Slope from the extreme points: $\dfrac{4.00 - 0.800~\text{atm}}{1.00 - 0.200~\text{L}^{-1}} = \dfrac{3.20}{0.800} = 4.00~\text{atm·L}$, and the line passes through the origin.

**Answer:** Plot $P$ vs $1/V$; it is linear through the origin with slope $4.00~\text{atm·L}$ (the constant $PV$).

### Example 6: Which Plot Is Straight? (Zero Order)

**Problem:** A dye decomposes on a surface:

| $t$ (s) | 0 | 100 | 200 | 300 |
|---|---|---|---|---|
| $[\ce{A}]$ (M) | 0.800 | 0.600 | 0.400 | 0.200 |

Determine the reaction order and the rate constant $k$.

**Solution:**

**Step 1:** Equal time steps (100 s each) — so check whether the *raw* concentration column changes by equal amounts: $-0.200$, $-0.200$, $-0.200~\text{M}$. Constant differences → $[\ce{A}]$ vs $t$ is already a straight line. No transformation needed.

**Step 2:** From the playbook: a linear $[\ce{A}]$ vs $t$ plot means **zero order**, and slope $= -k$.

**Step 3:** Slope $= \dfrac{0.200 - 0.800~\text{M}}{300 - 0~\text{s}} = -2.00 \times 10^{-3}~\text{M/s}$.

**Answer:** Zero order; $k = 2.00 \times 10^{-3}~\text{M/s}$.

### Example 7: Which Plot Is Straight? (First Order)

**Problem:** Decomposition of hydrogen peroxide, $\ce{2H2O2 -> 2H2O + O2}$:

| $t$ (s) | 0 | 200 | 400 | 600 |
|---|---|---|---|---|
| $[\ce{H2O2}]$ (M) | 0.500 | 0.250 | 0.125 | 0.0625 |

Show the reaction is first order and find $k$.

**Solution:**

**Step 1:** Raw differences: $-0.250, -0.125, -0.0625$ — not constant, so not zero order. But notice the *pattern*: the concentration halves every 200 s. Same **factor** in equal times is the first-order fingerprint.

**Step 2:** Confirm with the transformation. Build $\ln[\ce{H2O2}]$:

| $t$ (s) | 0 | 200 | 400 | 600 |
|---|---|---|---|---|
| $\ln[\ce{H2O2}]$ | $-0.693$ | $-1.386$ | $-2.079$ | $-2.773$ |

Differences: $-0.693$ each step. Constant → $\ln[\ce{H2O2}]$ vs $t$ is linear → **first order**.

**Step 3:** Slope $= \dfrac{-2.773 - (-0.693)}{600 - 0~\text{s}} = \dfrac{-2.080}{600~\text{s}} = -3.47 \times 10^{-3}~\text{s}^{-1}$, and $k = -\text{slope}$.

**Answer:** First order; $k = 3.47 \times 10^{-3}~\text{s}^{-1}$. (Note the units: first-order $k$ has no concentration in it — pure per-second.)

### Example 8: Half-Life Straight Off the Graph

**Problem:** Using the Example 7 data, what is the half-life of $\ce{H2O2}$ under these conditions, and how does it confirm first order?

**Solution:**

**Step 1:** Read halvings from the table: $0.500 \to 0.250$ M takes 200 s. Then $0.250 \to 0.125$ M takes another 200 s. Then $0.125 \to 0.0625$: 200 s again.

**Step 2:** The half-life is **constant** at 200 s no matter where you start. Only first-order processes do this — a zero-order half-life shrinks as the reaction proceeds, and a second-order half-life grows.

**Step 3:** Consistency check with $k$: for first order, $t_{1/2} = \dfrac{\ln 2}{k} = \dfrac{0.693}{3.47 \times 10^{-3}~\text{s}^{-1}} \approx 200~\text{s}$. ✓

**Answer:** $t_{1/2} = 200~\text{s}$; its constancy across the data is itself proof of first-order behavior.

### Example 9: Which Plot Is Straight? (Second Order)

**Problem:** Decomposition of $\ce{NO2}$ at high temperature:

| $t$ (s) | 0 | 50 | 100 | 150 |
|---|---|---|---|---|
| $[\ce{NO2}]$ (M) | 0.500 | 0.250 | 0.167 | 0.125 |

Determine the order and $k$.

**Solution:**

**Step 1:** Zero-order test — raw differences: $-0.250, -0.083, -0.042$. Not constant. ✗

**Step 2:** First-order test — halvings: $0.500 \to 0.250$ takes 50 s, but $0.250 \to 0.125$ takes 100 s. The half-life is *growing*, so not first order. ✗

**Step 3:** Second-order test — build $1/[\ce{NO2}]$:

| $t$ (s) | 0 | 50 | 100 | 150 |
|---|---|---|---|---|
| $1/[\ce{NO2}]$ (M⁻¹) | 2.00 | 4.00 | 6.00 | 8.00 |

Differences: $+2.00~\text{M}^{-1}$ every 50 s. Constant → linear → **second order**, and this slope is positive, as the playbook promised.

**Step 4:** Slope $= \dfrac{8.00 - 2.00~\text{M}^{-1}}{150 - 0~\text{s}} = 0.0400~\text{M}^{-1}\text{s}^{-1} = k$.

**Answer:** Second order; $k = 0.0400~\text{M}^{-1}\text{s}^{-1}$.

### Example 10: Beer's Law Calibration

**Problem:** A student measures absorbance of $\ce{CuSO4}$ solutions at 635 nm:

| $c$ (M) | 0.100 | 0.200 | 0.300 |
|---|---|---|---|
| $A$ (unitless) | 0.250 | 0.500 | 0.750 |

An unknown solution reads $A = 0.625$. Find its concentration.

**Solution:**

**Step 1:** Check linearity through the origin: $A/c = 2.50$ for every row. Direct proportionality — $A = (2.50~\text{M}^{-1})\,c$. (Absorbance is unitless, so the slope's units are $1/\text{M}$.)

**Step 2:** Use the line in reverse for the unknown:

$$c = \frac{A}{\text{slope}} = \frac{0.625}{2.50~\text{M}^{-1}} = 0.250~\text{M}$$

**Step 3:** Sanity check: $0.625$ lies between measured absorbances $0.500$ and $0.750$, so this is interpolation — trustworthy.

**Answer:** $[\ce{CuSO4}] = 0.250~\text{M}$.

### Example 11: Reading an Arrhenius Plot (Teaser)

**Problem:** For a reaction, a plot of $\ln k$ (y-axis) vs $1/T$ in $\text{K}^{-1}$ (x-axis) is a straight line with slope $-1.00 \times 10^{4}~\text{K}$. Given that the slope equals $-E_a/R$ with $R = 8.314~\text{J/(mol·K)}$, find the activation energy.

**Solution:**

**Step 1:** Set slope $= -E_a/R$ and solve:

$$E_a = -(\text{slope}) \times R = -(-1.00 \times 10^{4}~\text{K})(8.314~\text{J/(mol·K)}) $$

**Step 2:** Multiply, watching units cancel: $\text{K} \times \dfrac{\text{J}}{\text{mol·K}} = \dfrac{\text{J}}{\text{mol}}$.

$$E_a = 8.31 \times 10^{4}~\text{J/mol} = 83.1~\text{kJ/mol}$$

**Answer:** $E_a \approx 83~\text{kJ/mol}$. The whole "derivation" was: someone linearized $k$-vs-$T$ data, and the slope of the resulting line is a disguised activation energy.

### Example 12: Spotting the Trap — Two Points vs Best Fit

**Problem:** Five data points for a Beer's law lab lie almost perfectly on a line, except the $0.400~\text{M}$ reading is visibly high (a smudged cuvette). A student computes the slope using the origin and that smudged point. What went wrong, and what's the right procedure?

**Solution:**

**Step 1:** Using one flawed point to define the line imports its entire error into the slope — the calibration, and every unknown read from it, is now wrong.

**Step 2:** Correct procedure: plot all five points, draw the **best-fit line** balancing the four good points (the outlier gets outvoted, or is excluded with justification), then compute slope from **two widely separated points on the line itself** — not from raw data points.

**Answer:** Never compute slope from individual data points, and never let one suspicious point steer the fit; use two far-apart points *on the best-fit line*.

---

## Common Mistakes

| The Mistake | Why It Happens | How to Avoid It |
|---|---|---|
| Reporting a slope as a bare number ("slope = 0.04") | Algebra class trained you on unitless graphs | Slope units are always $\frac{\text{y units}}{\text{x units}}$ — write them the moment you write the number |
| Computing slope from two raw data points | It's faster | Use two well-separated points **on the best-fit line** |
| Connecting the dots instead of drawing a best-fit line | Feels more "faithful" to the data | Scatter is noise, not chemistry; one straight line, points balanced above and below |
| Extrapolating far beyond the data and trusting it | The line looks so confident | Label predictions outside the data range as extrapolation and treat them skeptically |
| Confusing direct with inverse proportionality | Both "relate" $x$ and $y$ | Table test: constant $y/x$ → direct; constant $xy$ → inverse |
| Plotting $\ln[\ce{A}]$ but calling the slope $k$ instead of $-k$ | Sign carelessness | For orders 0 and 1 the slope is $-k$ (line goes down); only second order gives slope $= +k$ |
| Mixing up the kinetics plots (e.g., "1st order → $1/[\ce{A}]$") | Memorizing without a hook | Order 0 = raw, order 1 = $\ln$, order 2 = reciprocal — the transformation "escalates" with order |
| Forgetting that first-order $k$ has units of $\text{s}^{-1}$ while zero order is $\text{M/s}$ and second order is $\text{M}^{-1}\text{s}^{-1}$ | Units feel like an afterthought | Get them free from the graph: slope units = y-axis units ÷ x-axis units |
| Extrapolating a Beer's law line to absorbances way above the calibration range | The unknown "should" fit | High absorbances go nonlinear; dilute the sample instead |

---

## AP Exam Tips

- **The exam gives you data tables, not equations.** A classic FRQ move: here are $t$, $[\ce{A}]$, $\ln[\ce{A}]$, and $1/[\ce{A}]$ columns (they often pre-compute the transforms for you!) — *which plot is linear, and what does that tell you about the order?* Answer in two clauses: name the straight plot, then name the order. "The plot of $\ln[\ce{A}]$ vs $t$ is linear, therefore the reaction is first order in $\ce{A}$."
- **Always state the slope with units,** and state the sign relationship: "slope $= -k$, so $k = 3.5 \times 10^{-3}~\text{s}^{-1}$." Points have been lost for the sign and for missing units.
- **Rate-constant units identify the order by themselves:** $\text{M/s}$ → zero, $\text{s}^{-1}$ → first, $\text{M}^{-1}\text{s}^{-1}$ → second. This is a free cross-check on multiple choice.
- **Constant half-life in a table screams first order.** If concentration halves in equal time intervals, you can skip the plotting entirely.
- If asked to *sketch* a graph, label both axes **with units**, and if the relationship passes through the origin (Beer's law, $P$ vs $1/V$), draw it through the origin.
- Beer's law questions love the reverse read: given a calibration line and an unknown's absorbance, interpolate the concentration. Show the slope calculation even if you can eyeball it.
- For Arrhenius questions at this level, you're expected to *interpret*, not derive: linear $\ln k$ vs $1/T$, slope $= -E_a/R$, steeper slope = larger activation energy = rate more sensitive to temperature.
- No calculator on the multiple-choice section — exam data tables use friendly numbers (halvings, constant differences) precisely so you can run the straightness tests in your head.

---

## Practice Problems

### Problem 1
A best-fit line of mass (g) vs volume (cm³) for a mystery solid passes through $(4.0~\text{cm}^3, 8.4~\text{g})$ and $(20.0~\text{cm}^3, 42.0~\text{g})$. Compute the slope with units and interpret it.

<details>
<summary><strong>Solution</strong></summary>

$$m = \frac{42.0 - 8.4~\text{g}}{20.0 - 4.0~\text{cm}^3} = \frac{33.6~\text{g}}{16.0~\text{cm}^3} = 2.1~\text{g/cm}^3$$

Mass per volume is density.

**Answer: slope $= 2.1~\text{g/cm}^3$, the density of the solid.**

</details>

### Problem 2
A student's mass-vs-volume best-fit line has the equation $m = (1.00~\text{g/mL})V - 2.0~\text{g}$ for water samples. What does the intercept indicate, and is the slope still usable?

<details>
<summary><strong>Solution</strong></summary>

At $V = 0$ the mass should be zero; an intercept of $-2.0~\text{g}$ means every reading is low by the same $2.0~\text{g}$ — a systematic error (e.g., the balance was tared with something on it). Because the offset is constant, it cancels in $\Delta y/\Delta x$.

**Answer: a systematic offset of $-2.0~\text{g}$ in every mass reading; yes, the slope ($1.00~\text{g/mL}$, the density of water) is still valid.**

</details>

### Problem 3
Solubility data for $\ce{KNO3}$ is measured at 10 °C, 30 °C, and 50 °C. A student uses the best-fit line to predict solubility at 40 °C and at 95 °C. Which prediction is more trustworthy, and why?

<details>
<summary><strong>Solution</strong></summary>

40 °C lies between measured points — that's interpolation, well supported by the data. 95 °C is far outside the measured range — extrapolation, which assumes the linear trend continues where nothing was measured (and solubility curves often bend at higher temperatures).

**Answer: the 40 °C prediction (interpolation) is trustworthy; the 95 °C prediction (extrapolation) is not.**

</details>

### Problem 4
For each data set, decide whether $y$ is directly proportional, inversely proportional, or neither with respect to $x$:

(a) $(x, y) = (2, 6), (4, 12), (10, 30)$
(b) $(x, y) = (2, 12), (4, 6), (8, 3)$
(c) $(x, y) = (1, 5), (2, 7), (3, 9)$

<details>
<summary><strong>Solution</strong></summary>

(a) $y/x = 3, 3, 3$ — constant ratio → **direct** ($y = 3x$).
(b) $xy = 24, 24, 24$ — constant product → **inverse** ($y = 24/x$).
(c) $y/x = 5, 3.5, 3$ — not constant; $xy = 5, 14, 27$ — not constant. But differences are constant ($+2$ per step), so it's linear with a nonzero intercept: $y = 2x + 3$ — linear, yet **neither** proportionality.

**Answer: (a) direct; (b) inverse; (c) neither (linear but not through the origin).**

</details>

### Problem 5
A gas sample at constant temperature gives $P = 6.00~\text{atm}$ at $V = 0.500~\text{L}$ and $P = 1.50~\text{atm}$ at $V = 2.00~\text{L}$. What should be plotted against what to obtain a straight line through the origin, and what is the slope with units?

<details>
<summary><strong>Solution</strong></summary>

Check inverse behavior: $PV = (6.00)(0.500) = 3.00$ and $(1.50)(2.00) = 3.00~\text{L·atm}$ — constant, so $P = \dfrac{3.00}{V}$. Plot $P$ vs $1/V$:

At $1/V = 2.00~\text{L}^{-1}$, $P = 6.00$; at $1/V = 0.500~\text{L}^{-1}$, $P = 1.50$. Slope $= \dfrac{6.00 - 1.50}{2.00 - 0.500} = 3.00~\text{atm·L}$.

**Answer: plot $P$ vs $1/V$; slope $= 3.00~\text{atm·L}$ (the constant $PV$).**

</details>

### Problem 6
A reactant $\ce{A}$ decomposes:

| $t$ (min) | 0 | 10 | 20 | 30 |
|---|---|---|---|---|
| $[\ce{A}]$ (M) | 1.20 | 0.90 | 0.60 | 0.30 |

Determine the order and the rate constant.

<details>
<summary><strong>Solution</strong></summary>

Raw differences: $-0.30~\text{M}$ every 10 min — constant, so $[\ce{A}]$ vs $t$ is already linear: **zero order**.

Slope $= \dfrac{0.30 - 1.20~\text{M}}{30 - 0~\text{min}} = -0.030~\text{M/min}$, and $k = -\text{slope}$.

**Answer: zero order; $k = 0.030~\text{M/min}$ (equivalently $5.0 \times 10^{-4}~\text{M/s}$).**

</details>

### Problem 7
For the decomposition of $\ce{N2O5}$, a plot of $\ln[\ce{N2O5}]$ vs $t$ is a straight line with slope $-5.0 \times 10^{-4}~\text{s}^{-1}$. State the order, the value of $k$ with units, and the half-life.

<details>
<summary><strong>Solution</strong></summary>

Linear $\ln[\ce{A}]$ vs $t$ → **first order**, with slope $= -k$, so $k = 5.0 \times 10^{-4}~\text{s}^{-1}$.

$$t_{1/2} = \frac{\ln 2}{k} = \frac{0.693}{5.0 \times 10^{-4}~\text{s}^{-1}} = 1.4 \times 10^{3}~\text{s}$$

**Answer: first order; $k = 5.0 \times 10^{-4}~\text{s}^{-1}$; $t_{1/2} \approx 1.4 \times 10^{3}~\text{s}$ (about 23 minutes).**

</details>

### Problem 8
A data table shows $[\ce{A}]$ falling from $0.80~\text{M}$ to $0.40~\text{M}$ in the first 25 s, and from $0.40~\text{M}$ to $0.20~\text{M}$ in the next 25 s. Without plotting anything, identify the order and $k$.

<details>
<summary><strong>Solution</strong></summary>

The concentration halves in equal 25 s intervals — a **constant half-life**, the fingerprint of first order.

$$k = \frac{\ln 2}{t_{1/2}} = \frac{0.693}{25~\text{s}} = 0.028~\text{s}^{-1}$$

**Answer: first order; $k \approx 0.028~\text{s}^{-1}$.**

</details>

### Problem 9
For a reaction $\ce{2A -> products}$:

| $t$ (s) | 0 | 100 | 200 | 300 |
|---|---|---|---|---|
| $1/[\ce{A}]$ (M⁻¹) | 5.0 | 7.5 | 10.0 | 12.5 |

The $[\ce{A}]$ vs $t$ and $\ln[\ce{A}]$ vs $t$ plots are both curved. State the order, $k$ with units, and the initial concentration $[\ce{A}]_0$.

<details>
<summary><strong>Solution</strong></summary>

Linear $1/[\ce{A}]$ vs $t$ → **second order**. Slope $= \dfrac{12.5 - 5.0~\text{M}^{-1}}{300 - 0~\text{s}} = 0.025~\text{M}^{-1}\text{s}^{-1} = k$ (positive slope, so $k$ = slope directly).

The intercept is $1/[\ce{A}]_0 = 5.0~\text{M}^{-1}$, so $[\ce{A}]_0 = 0.20~\text{M}$.

**Answer: second order; $k = 0.025~\text{M}^{-1}\text{s}^{-1}$; $[\ce{A}]_0 = 0.20~\text{M}$.**

</details>

### Problem 10
A rate constant is reported as $k = 4.2 \times 10^{-2}~\text{M}^{-1}\text{s}^{-1}$. Without any graph, what is the reaction order, and which plot of concentration data would be linear?

<details>
<summary><strong>Solution</strong></summary>

Units $\text{M}^{-1}\text{s}^{-1}$ belong to second order (zero order is $\text{M/s}$; first order is $\text{s}^{-1}$). The corresponding straight-line plot is $1/[\ce{A}]$ vs $t$, with slope $+k$.

**Answer: second order; $1/[\ce{A}]$ vs $t$ is linear with slope $= k$.**

</details>

### Problem 11
A Beer's law calibration for a blue dye gives a best-fit line $A = (145~\text{M}^{-1})\,c$ passing through the origin. An unknown sample reads $A = 0.435$. Find its concentration, and state one condition required for this answer to be trustworthy.

<details>
<summary><strong>Solution</strong></summary>

$$c = \frac{A}{145~\text{M}^{-1}} = \frac{0.435}{145~\text{M}^{-1}} = 3.00 \times 10^{-3}~\text{M}$$

Trustworthy only if $A = 0.435$ falls **within** the calibrated absorbance range (interpolation, not extrapolation). If the unknown reads above the highest standard, dilute it and remeasure.

**Answer: $c = 3.00 \times 10^{-3}~\text{M}$, valid provided the reading lies inside the calibration range.**

</details>

### Problem 12
In a Beer's law plot of absorbance (unitless) vs concentration (M), what are the units of the slope, and what physical quantities does the slope combine?

<details>
<summary><strong>Solution</strong></summary>

Slope units $= \dfrac{\text{unitless}}{\text{M}} = \text{M}^{-1}$. From $A = \varepsilon b c$, the slope equals $\varepsilon b$: the molar absorptivity of the compound times the cuvette path length. Fixed compound, wavelength, and cuvette → fixed slope, which is why one calibration line serves a whole lab.

**Answer: units of $\text{M}^{-1}$ (or $\text{L·mol}^{-1}\text{cm}^{-1}$ times cm); slope $= \varepsilon b$.**

</details>

### Problem 13
For a reaction, the plot of $\ln k$ vs $1/T$ is linear with slope $-6.0 \times 10^{3}~\text{K}$. Using slope $= -E_a/R$ with $R = 8.314~\text{J/(mol·K)}$, compute $E_a$ in kJ/mol.

<details>
<summary><strong>Solution</strong></summary>

$$E_a = -(\text{slope}) \cdot R = (6.0 \times 10^{3}~\text{K})\left(8.314~\frac{\text{J}}{\text{mol·K}}\right) = 5.0 \times 10^{4}~\text{J/mol}$$

Units: $\text{K} \times \text{J/(mol·K)} = \text{J/mol}$. Convert: $5.0 \times 10^{4}~\text{J/mol} = 50.~\text{kJ/mol}$.

**Answer: $E_a \approx 50.~\text{kJ/mol}$.**

</details>

### Problem 14
Two students process the same slightly scattered kinetics data. Student 1 connects consecutive points and reports "the slope" of one segment. Student 2 draws a best-fit line and computes the slope from two well-separated points on it. Whose $k$ is more reliable, and why?

<details>
<summary><strong>Solution</strong></summary>

Student 2. Each individual segment's slope is dominated by the random error of just two measurements; different segments would give wildly different "$k$" values. A best-fit line averages the noise across all points, and taking widely separated points on that line minimizes the effect of reading error on $\Delta y/\Delta x$.

**Answer: Student 2 — best-fit slopes average out random error; connect-the-dots slopes amplify it.**

</details>

### Problem 15
An FRQ provides this table for $\ce{A -> products}$ and asks for the order:

| $t$ (s) | $[\ce{A}]$ (M) | $\ln[\ce{A}]$ | $1/[\ce{A}]$ (M⁻¹) |
|---|---|---|---|
| 0 | 0.100 | $-2.303$ | 10.0 |
| 40 | 0.050 | $-2.996$ | 20.0 |
| 80 | 0.025 | $-3.689$ | 40.0 |

Which column is linear in $t$, what is the order, and what is $k$?

<details>
<summary><strong>Solution</strong></summary>

Equal 40 s steps. Test each column's differences:

- $[\ce{A}]$: $-0.050$, then $-0.025$ — not constant.
- $\ln[\ce{A}]$: $-0.693$, then $-0.693$ — **constant** → linear.
- $1/[\ce{A}]$: $+10.0$, then $+20.0$ — not constant.

Linear $\ln[\ce{A}]$ vs $t$ → first order. Slope $= \dfrac{-3.689 - (-2.303)}{80 - 0~\text{s}} = \dfrac{-1.386}{80~\text{s}} = -0.0173~\text{s}^{-1}$, so $k = 0.0173~\text{s}^{-1}$. (Cross-check: the half-life is a constant 40 s, and $0.693/40 = 0.0173~\text{s}^{-1}$. ✓)

**Answer: $\ln[\ce{A}]$ vs $t$ is linear; first order; $k = 1.7 \times 10^{-2}~\text{s}^{-1}$.**

</details>

---

## Quick Reference

| Situation | What to plot | Slope means | Slope units |
|---|---|---|---|
| Any straight line | $y$ vs $x$ | $m$ in $y = mx + b$ | $\frac{\text{y units}}{\text{x units}}$ |
| Mass vs volume | $m$ vs $V$ | density | g/mL |
| Inverse proportion ($xy = $ const) | $y$ vs $1/x$ | the constant | (y units)(x units) |
| Boyle's law | $P$ vs $1/V$ | $PV$ constant | atm·L |
| Zero-order kinetics | $[\ce{A}]$ vs $t$ | $-k$ | M/s |
| First-order kinetics | $\ln[\ce{A}]$ vs $t$ | $-k$ | s⁻¹ |
| Second-order kinetics | $1/[\ce{A}]$ vs $t$ | $+k$ | M⁻¹s⁻¹ |
| Beer's law | $A$ vs $c$ | $\varepsilon b$ | M⁻¹ |
| Arrhenius | $\ln k$ vs $1/T$ | $-E_a/R$ | K |

**Table tests (no graph needed):** constant $y/x$ → direct proportion; constant $xy$ → inverse proportion; constant differences of a (transformed) column over equal $x$ steps → that plot is linear. Constant half-life → first order.

**The two moves, forever:** curve → transform an axis until it's a line; line → read slope and intercept **with units** and translate them into chemistry.

---

<div align="center">

[← Logarithms for Chemistry](/chemistry/0104-logarithms-for-chemistry) | [Atomic Structure Basics →](/chemistry/0201-atomic-structure-basics)

</div>
