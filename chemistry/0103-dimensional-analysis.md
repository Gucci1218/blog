# Dimensional Analysis
<p class="article-date">July 4, 2026</p>

*Every time Dad and I drive up to LA, the same mental math happens before we even leave the driveway: it's about 120 miles, the car gets 28 miles per gallon, gas is \$4.85 a gallon — so the trip costs about twenty bucks. Notice what just happened: miles became gallons, gallons became dollars, and I chained one conversion into the next without ever thinking "I am now performing unit conversions." Dimensional analysis is that exact chain, made explicit and bulletproof. Every conversion factor is secretly a fraction equal to 1, so multiplying by it changes the units without changing the actual quantity — and the units cancel exactly like factors cancel in an algebra fraction (the same canceling instinct that carried me through BC Calc). The known quantity is your starting city, each conversion factor is a highway segment, and the target unit is your destination. In AP Chemistry, this is not a side skill — it is THE skill. Every stoichiometry problem, every molarity calculation, every gas law FRQ is a road trip through units.*

---

## What You'll Learn

- Explain why every conversion factor is a fraction equal to 1, and why multiplying by 1 is always legal
- Flip conversion factors so the unit you want to eliminate cancels
- Set up single-step and multi-step conversions using the factor-label ("railroad") method
- Handle squared and cubed units correctly (the $\text{cm}^3 \to \text{m}^3$ trap)
- Convert within the metric system using prefixes, and between metric and English units using given factors
- Use derived units — density, rates, and percentages — as conversion factors
- Preview the chemistry chains you'll live in all year: grams → moles → particles, and molarity as mol/L
- Build any conversion by writing the target unit *first*, then sanity-checking the magnitude at the end

---

## Prerequisites

- [Scientific Notation](/chemistry/0101-scientific-notation) — conversion chains produce very large and very small numbers; you need to move powers of ten without flinching
- [Significant Figures](/chemistry/0102-significant-figures) — every answer in this article is rounded by the sig-fig rules, and exact conversion factors never limit your sig figs

---

## The Core Concept

### Intuition First

Back to the LA trip. Here's the chain I do in my head, written out the way a chemist would write it:

$$
120 \ \text{mi} \times \frac{1 \ \text{gal}}{28 \ \text{mi}} \times \frac{4.85 \ \text{dollars}}{1 \ \text{gal}} \approx 21 \ \text{dollars}
$$

Look at the structure. The **starting city** is $120 \ \text{mi}$ — the one quantity I actually know. The **destination** is dollars — the unit I want. Each fraction in between is a **highway segment** that connects one unit to the next: miles connect to gallons (through the car's fuel efficiency), gallons connect to dollars (through the gas price). There's no highway that goes directly from miles to dollars, so I route through gallons.

And here's the algebra move you already trust from calculus: **units cancel like factors.** The "mi" on top of $120 \ \text{mi}$ cancels the "mi" on the bottom of the first fraction. The "gal" on top of that fraction cancels the "gal" on the bottom of the next one. When the dust settles, the only unit left standing is dollars — the destination. If the wrong unit survives, you took a wrong turn, and the units *tell you so before you've wasted arithmetic*.

Why is any of this legal? Because every conversion factor equals **1**.

### Conversion Factors Are Fractions Equal to 1

Start from a true equality:

$$1 \ \text{gal} = 28 \ \text{mi (for this car)}, \qquad 1 \ \text{m} = 100 \ \text{cm}, \qquad 1 \ \text{in} = 2.54 \ \text{cm}$$

Divide both sides of any equality by one side, and you get a fraction whose value is exactly 1:

$$
\frac{100 \ \text{cm}}{1 \ \text{m}} = 1 \qquad \text{and, flipped:} \qquad \frac{1 \ \text{m}}{100 \ \text{cm}} = 1
$$

Multiplying a quantity by 1 never changes what it *is* — only what it's *called*. That's the entire trick. Both orientations of the fraction equal 1, so **you choose the orientation that puts the unit you're killing on the bottom**:

- Converting meters → centimeters? Meters must die, so meters go on the bottom: use $\frac{100 \ \text{cm}}{1 \ \text{m}}$.
- Converting centimeters → meters? Flip it: use $\frac{1 \ \text{m}}{100 \ \text{cm}}$.

If you ever multiply and end up with units like $\text{cm}^2/\text{m}$, you grabbed the wrong orientation. Flip the fraction.

### The Factor-Label (Railroad) Setup

The standard way to write a chain is one long line of multiplied fractions — sometimes drawn as a "railroad track" with vertical bars, but in display math it looks like this:

$$
\underbrace{\text{known quantity}}_{\text{starting city}} \times \underbrace{\frac{\text{new unit}}{\text{old unit}} \times \frac{\text{newer unit}}{\text{new unit}} \times \cdots}_{\text{highway segments}} = \underbrace{\text{answer in target unit}}_{\text{destination}}
$$

A real one — converting 3.25 hours to seconds:

$$
3.25 \ \cancel{\text{h}} \times \frac{60 \ \cancel{\text{min}}}{1 \ \cancel{\text{h}}} \times \frac{60 \ \text{s}}{1 \ \cancel{\text{min}}} = 1.17 \times 10^4 \ \text{s}
$$

Every intermediate unit appears exactly twice — once on top, once on bottom — and cancels. Only seconds survive.

### The Strategy: Write the Destination First

This is the single best habit you can build, and it's backwards from how most people start:

1. **Write the target unit first**, off to the right: "$= \ ? \ \text{s}$". Know your destination before you drive.
2. **Write the known quantity** on the left. That's your starting city.
3. **Build the bridge** one factor at a time, each factor flipped so the previous unit cancels.
4. **Cancel units on paper** — actually draw the slashes. If the surviving unit isn't the target, fix the setup *before* touching your calculator.
5. **Sanity-check the magnitude.** Seconds are tiny compared to hours, so 3.25 hours should be a *big* number of seconds. If you'd gotten $0.00090 \ \text{s}$, you'd know a fraction was upside down.

### Metric Prefixes: The Free Highway System

Metric ↔ metric conversions need no memorized oddball numbers — just the prefix table. Each prefix is a power of ten attached to the base unit (meter, gram, liter, second):

| Prefix | Symbol | Meaning | Example equality |
|---|---|---|---|
| kilo- | k | $10^3$ | $1 \ \text{km} = 10^3 \ \text{m}$ |
| deci- | d | $10^{-1}$ | $1 \ \text{dm} = 10^{-1} \ \text{m}$ |
| centi- | c | $10^{-2}$ | $1 \ \text{cm} = 10^{-2} \ \text{m}$ |
| milli- | m | $10^{-3}$ | $1 \ \text{mm} = 10^{-3} \ \text{m}$ |
| micro- | µ | $10^{-6}$ | $1 \ \text{µg} = 10^{-6} \ \text{g}$ |
| nano- | n | $10^{-9}$ | $1 \ \text{nm} = 10^{-9} \ \text{m}$ |
| pico- | p | $10^{-12}$ | $1 \ \text{pm} = 10^{-12} \ \text{m}$ |

Pro move: to go from one prefix to another (mg → kg), route **through the base unit** — two easy segments instead of one error-prone shortcut.

Metric ↔ English factors ($1 \ \text{in} = 2.54 \ \text{cm}$, $1 \ \text{lb} = 453.6 \ \text{g}$, $1 \ \text{mi} = 1.609 \ \text{km}$) are **given** on AP-style problems. Don't memorize them; know how to use them.

### Squared and Cubed Units: Cube the Whole Factor

Here's the trap that catches everyone at least once. Since $1 \ \text{m} = 100 \ \text{cm}$, it is tempting to write $1 \ \text{m}^3 = 100 \ \text{cm}^3$. **Wrong.** Cube *both sides* of the equality — the number AND the unit:

$$
(1 \ \text{m})^3 = (100 \ \text{cm})^3 \quad \Longrightarrow \quad 1 \ \text{m}^3 = 10^6 \ \text{cm}^3
$$

A cubic meter is a box you could sit inside; a cubic centimeter is a sugar cube. Of course there are a *million* sugar cubes in the box — the sanity check catches this instantly. In a chain, cube the entire conversion factor:

$$
\left(\frac{1 \ \text{m}}{100 \ \text{cm}}\right)^3 = \frac{1 \ \text{m}^3}{10^6 \ \text{cm}^3}
$$

Same idea for squared units: $\left(\frac{100 \ \text{cm}}{1 \ \text{m}}\right)^2 = \frac{10^4 \ \text{cm}^2}{1 \ \text{m}^2}$.

Bonus fact you'll use constantly: $1 \ \text{cm}^3 = 1 \ \text{mL}$ exactly, so $1 \ \text{L} = 1000 \ \text{cm}^3$.

### Derived Units Are Conversion Factors Too

This is where dimensional analysis stops being "unit conversion" and becomes *chemistry*.

**Density connects mass and volume.** If ethanol's density is $0.789 \ \text{g/mL}$, that's the equality $0.789 \ \text{g} = 1 \ \text{mL}$ (for ethanol), which gives two usable fractions:

$$
\frac{0.789 \ \text{g}}{1 \ \text{mL}} \quad \text{(volume → mass)} \qquad \frac{1 \ \text{mL}}{0.789 \ \text{g}} \quad \text{(mass → volume)}
$$

**Rates connect two different units** the same way: $65 \ \text{mi/h}$ is the segment $\frac{65 \ \text{mi}}{1 \ \text{h}}$ or its flip.

**Percent is a fraction with a hidden "per 100."** A solution that is 12.0% sucrose by mass gives the factor

$$
\frac{12.0 \ \text{g sucrose}}{100 \ \text{g solution}}
$$

— which converts grams of solution into grams of sucrose. Percent problems are just one-segment road trips in disguise.

### The Chemistry Preview: Grams → Moles → Particles

The single most-traveled highway in AP Chemistry runs between three cities: **grams**, **moles**, and **particles**. You'll meet the mole properly in [The Mole](/chemistry/0207-the-mole), but the road map is pure dimensional analysis:

$$
\text{grams} \ \xrightarrow[\text{molar mass}]{\frac{1 \ \text{mol}}{M \ \text{g}}} \ \text{moles} \ \xrightarrow[\text{Avogadro}]{\frac{6.022 \times 10^{23} \ \text{particles}}{1 \ \text{mol}}} \ \text{particles}
$$

The molar mass (e.g., $18.02 \ \text{g/mol}$ for $\ce{H2O}$) is the segment between grams and moles; Avogadro's number is the segment between moles and particles. And **molarity** — coming soon — is just another rate-style factor, $\frac{\text{mol}}{\text{L}}$, connecting volume of solution to moles of solute. Every one of these is a fraction equal to 1 *for that substance*. Same highway system, new cities.

---

## Worked Examples

### Example 1: Single-Step Conversion

**Problem:** Convert $4.5 \ \text{min}$ to seconds.

**Solution:**

**Step 1:** Destination: seconds. Starting city: $4.5 \ \text{min}$.

**Step 2:** Minutes must cancel, so minutes go on the bottom:

$$
4.5 \ \cancel{\text{min}} \times \frac{60 \ \text{s}}{1 \ \cancel{\text{min}}} = 270 \ \text{s}
$$

**Step 3:** Sanity check: seconds are smaller than minutes, so the number should get bigger. It did. (The 60 is exact, so sig figs come from 4.5.)

**Answer:** $2.7 \times 10^2 \ \text{s}$

### Example 2: Choosing the Right Orientation

**Problem:** A house key is $87.3 \ \text{mm}$ long. Convert to meters — and show what happens if you flip the factor the wrong way.

**Solution:**

**Step 1:** The equality: $1 \ \text{mm} = 10^{-3} \ \text{m}$. Two possible fractions: $\frac{10^{-3} \ \text{m}}{1 \ \text{mm}}$ and $\frac{1 \ \text{mm}}{10^{-3} \ \text{m}}$.

**Step 2 (the wrong way first):**

$$
87.3 \ \text{mm} \times \frac{1 \ \text{mm}}{10^{-3} \ \text{m}} = 87\,300 \ \frac{\text{mm}^2}{\text{m}} \quad \text{✗}
$$

The units $\text{mm}^2/\text{m}$ are nonsense — nothing canceled. The units caught the error before the answer could.

**Step 3 (the right way):** mm must die, so mm goes on the bottom:

$$
87.3 \ \cancel{\text{mm}} \times \frac{10^{-3} \ \text{m}}{1 \ \cancel{\text{mm}}} = 0.0873 \ \text{m}
$$

**Answer:** $0.0873 \ \text{m}$

### Example 3: Multi-Step Chain (Time)

**Problem:** How many seconds are in $3.00 \ \text{days}$?

**Solution:**

**Step 1:** Route: days → hours → minutes → seconds. Three segments, each flipped so the previous unit cancels.

**Step 2:**

$$
3.00 \ \cancel{\text{d}} \times \frac{24 \ \cancel{\text{h}}}{1 \ \cancel{\text{d}}} \times \frac{60 \ \cancel{\text{min}}}{1 \ \cancel{\text{h}}} \times \frac{60 \ \text{s}}{1 \ \cancel{\text{min}}} = 259\,200 \ \text{s}
$$

**Step 3:** All conversion factors are exact; the 3.00 gives 3 sig figs.

**Answer:** $2.59 \times 10^5 \ \text{s}$

### Example 4: Metric Prefix to Prefix (Route Through the Base Unit)

**Problem:** Convert $0.0348 \ \text{km}$ to centimeters.

**Solution:**

**Step 1:** Route: km → m → cm. Through the base unit — always.

**Step 2:**

$$
0.0348 \ \cancel{\text{km}} \times \frac{10^3 \ \cancel{\text{m}}}{1 \ \cancel{\text{km}}} \times \frac{100 \ \text{cm}}{1 \ \cancel{\text{m}}} = 3480 \ \text{cm}
$$

**Step 3:** Sanity check: centimeters are much smaller than kilometers, so the number should grow enormously. $0.0348 \to 3480$. ✓

**Answer:** $3.48 \times 10^3 \ \text{cm}$

### Example 5: Metric ↔ English (Given Factor)

**Problem:** A boba drink is labeled $22.0 \ \text{oz}$. Given $1 \ \text{oz} = 29.57 \ \text{mL}$, find the volume in liters.

**Solution:**

**Step 1:** Route: oz → mL → L.

**Step 2:**

$$
22.0 \ \cancel{\text{oz}} \times \frac{29.57 \ \cancel{\text{mL}}}{1 \ \cancel{\text{oz}}} \times \frac{1 \ \text{L}}{1000 \ \cancel{\text{mL}}} = 0.65054 \ \text{L}
$$

**Step 3:** Three sig figs from 22.0 (the 29.57 has four; the 1000 is exact).

**Answer:** $0.651 \ \text{L}$

### Example 6: Squared Units

**Problem:** A solar panel has an area of $1.85 \ \text{m}^2$. Convert to $\text{cm}^2$.

**Solution:**

**Step 1:** The linear factor is $\frac{100 \ \text{cm}}{1 \ \text{m}}$. Area is length *squared*, so square the **whole factor** — number and unit:

$$
\left(\frac{100 \ \text{cm}}{1 \ \text{m}}\right)^2 = \frac{10^4 \ \text{cm}^2}{1 \ \text{m}^2}
$$

**Step 2:**

$$
1.85 \ \cancel{\text{m}^2} \times \frac{10^4 \ \text{cm}^2}{1 \ \cancel{\text{m}^2}} = 1.85 \times 10^4 \ \text{cm}^2
$$

**Answer:** $1.85 \times 10^4 \ \text{cm}^2$

### Example 7: Cubed Units — the Classic Trap

**Problem:** Convert $7.50 \times 10^5 \ \text{cm}^3$ to $\text{m}^3$.

**Solution:**

**Step 1:** Wrong (but tempting): divide by 100 to get $7500 \ \text{m}^3$. That's a warehouse of water from a bathtub's worth — the magnitude check screams.

**Step 2:** Cube the entire linear factor:

$$
7.50 \times 10^5 \ \cancel{\text{cm}^3} \times \left(\frac{1 \ \text{m}}{100 \ \cancel{\text{cm}}}\right)^3 = 7.50 \times 10^5 \ \cancel{\text{cm}^3} \times \frac{1 \ \text{m}^3}{10^6 \ \cancel{\text{cm}^3}} = 0.750 \ \text{m}^3
$$

**Step 3:** Sanity check: $\text{m}^3$ are giant units, so the number should shrink hard. $750\,000 \to 0.750$. ✓

**Answer:** $0.750 \ \text{m}^3$

### Example 8: Density as a Conversion Factor (Volume → Mass)

**Problem:** What is the mass of $250.0 \ \text{mL}$ of ethanol ($\ce{C2H5OH}$, density $= 0.789 \ \text{g/mL}$)?

**Solution:**

**Step 1:** Density is the segment between mL and g. Target is grams, so grams go on top:

$$
250.0 \ \cancel{\text{mL}} \times \frac{0.789 \ \text{g}}{1 \ \cancel{\text{mL}}} = 197.25 \ \text{g}
$$

**Step 2:** Three sig figs from the density (measured), even though 250.0 has four.

**Answer:** $197 \ \text{g}$

### Example 9: Density Flipped (Mass → Volume)

**Problem:** A jeweler has $500.0 \ \text{g}$ of gold ($\ce{Au}$, density $= 19.3 \ \text{g/mL}$). What volume does it occupy?

**Solution:**

**Step 1:** Now grams must cancel, so flip the density — grams on the bottom:

$$
500.0 \ \cancel{\text{g}} \times \frac{1 \ \text{mL}}{19.3 \ \cancel{\text{g}}} = 25.9 \ \text{mL}
$$

**Step 2:** Sanity check: gold is *dense*, so half a kilogram should be a small volume — about five teaspoons. ✓

**Answer:** $25.9 \ \text{mL}$

### Example 10: Converting a Rate

**Problem:** The speed limit on I-5 is $65 \ \text{mi/h}$. Convert to $\text{m/s}$. (Given: $1 \ \text{mi} = 1609 \ \text{m}$.)

**Solution:**

**Step 1:** Two units to convert — miles on top, hours on the bottom. Attack each separately:

$$
\frac{65 \ \cancel{\text{mi}}}{1 \ \cancel{\text{h}}} \times \frac{1609 \ \text{m}}{1 \ \cancel{\text{mi}}} \times \frac{1 \ \cancel{\text{h}}}{3600 \ \text{s}} = 29.05 \ \text{m/s}
$$

**Step 2:** Note the hour factor is written with hours on *top* so it cancels the hours on the *bottom* of the rate. Two sig figs from 65.

**Answer:** $29 \ \text{m/s}$

### Example 11: Percent as a Conversion Factor

**Problem:** A sports drink is $6.00\%$ sugar by mass. How many grams of sugar are in $355 \ \text{g}$ of the drink?

**Solution:**

**Step 1:** "6.00% by mass" means the factor $\frac{6.00 \ \text{g sugar}}{100 \ \text{g drink}}$ (the 100 is exact).

**Step 2:**

$$
355 \ \cancel{\text{g drink}} \times \frac{6.00 \ \text{g sugar}}{100 \ \cancel{\text{g drink}}} = 21.3 \ \text{g sugar}
$$

**Answer:** $21.3 \ \text{g}$ of sugar

### Example 12: Chemistry Preview — Grams to Molecules

**Problem:** How many molecules are in $36.0 \ \text{g}$ of water? (Molar mass of $\ce{H2O} = 18.02 \ \text{g/mol}$; Avogadro's number $= 6.022 \times 10^{23} \ \text{mol}^{-1}$.)

**Solution:**

**Step 1:** Route: g → mol → molecules. Molar mass is segment one; Avogadro is segment two.

**Step 2:**

$$
36.0 \ \cancel{\text{g}} \times \frac{1 \ \cancel{\text{mol}}}{18.02 \ \cancel{\text{g}}} \times \frac{6.022 \times 10^{23} \ \text{molecules}}{1 \ \cancel{\text{mol}}} = 1.203 \times 10^{24} \ \text{molecules}
$$

**Step 3:** This exact chain — with a mole-ratio segment spliced into the middle — is every stoichiometry problem you will ever do. Three sig figs.

**Answer:** $1.20 \times 10^{24}$ molecules of $\ce{H2O}$

---

## Common Mistakes

| The Mistake | Why It Happens | How to Avoid It |
|---|---|---|
| Flipping a factor upside down (multiplying when you should divide) | Plugging numbers before thinking about units | Write units in every factor and cancel on paper; if the target unit doesn't survive, flip |
| $1 \ \text{m}^3 = 100 \ \text{cm}^3$ | Cubing the unit but not the number | Cube the *entire* factor: $(100)^3 = 10^6$; sanity-check with the "box vs. sugar cube" picture |
| Treating conversion factors as sig-fig limiters | Forgetting that defined equalities are exact | $1 \ \text{m} = 100 \ \text{cm}$, $60 \ \text{s} = 1 \ \text{min}$, "per 100" in percent — all exact, infinite sig figs. Measured factors (density, molar mass) do count |
| Skipping the magnitude sanity check | Trusting the calculator | Ask "should this number get bigger or smaller?" *before* computing |
| One giant mental shortcut for prefix→prefix (mg → kg) | Overconfidence with powers of ten | Route through the base unit: mg → g → kg, two clean segments |
| Dropping units mid-problem and re-attaching them at the end | Speed | The units ARE the method. No units, no error-detection, no credit |
| Using density right-side up when it should be flipped | Memorizing "multiply by density" as a rule | There is no rule to memorize — orientation is dictated by which unit must cancel |

---

## AP Exam Tips

- **Dimensional analysis is the backbone of every stoichiometry FRQ.** Grams → moles → mole ratio → moles → grams is one long factor-label chain. Master the setup now and Unit 4 becomes bookkeeping.
- **Showing units earns work-shown credit.** On FRQs, a correct setup with units visible can earn points even if your final arithmetic slips. A bare number, even a correct one, can lose the "work" point.
- **Unit cancellation catches setup errors before they cost points.** If your chain for "grams of product" ends in $\text{mol}^2/\text{g}$, you know *during the exam* that a factor is flipped — free error-checking that takes five seconds.
- **Conversion factors between unit systems are given** (in the problem or on the reference sheet). Metric prefixes, however, are assumed knowledge — know kilo through pico cold.
- **Exact factors never limit sig figs.** Graders check final-answer sig figs on some FRQ parts; remember that only *measured* quantities (masses, volumes, densities, molar masses) count.
- **Calculator note:** enter a chain as one continuous computation (multiply across the top, divide by each bottom) rather than rounding at every step. Round once, at the destination.

---

## Practice Problems

### Problem 1
Convert $2.5 \ \text{h}$ to seconds.

<details>
<summary><strong>Solution</strong></summary>

$$
2.5 \ \cancel{\text{h}} \times \frac{60 \ \cancel{\text{min}}}{1 \ \cancel{\text{h}}} \times \frac{60 \ \text{s}}{1 \ \cancel{\text{min}}} = 9000 \ \text{s}
$$

Both factors are exact; 2.5 gives two sig figs.

**Answer: $9.0 \times 10^3 \ \text{s}$**

</details>

### Problem 2
Convert $875 \ \text{mm}$ to kilometers.

<details>
<summary><strong>Solution</strong></summary>

Route through the base unit: mm → m → km.

$$
875 \ \cancel{\text{mm}} \times \frac{10^{-3} \ \cancel{\text{m}}}{1 \ \cancel{\text{mm}}} \times \frac{1 \ \text{km}}{10^3 \ \cancel{\text{m}}} = 8.75 \times 10^{-4} \ \text{km}
$$

Sanity check: kilometers are huge compared to millimeters, so the number should shrink drastically. ✓

**Answer: $8.75 \times 10^{-4} \ \text{km}$**

</details>

### Problem 3
A package weighs $4.50 \ \text{lb}$. Given $1 \ \text{lb} = 453.6 \ \text{g}$, find its mass in grams.

<details>
<summary><strong>Solution</strong></summary>

$$
4.50 \ \cancel{\text{lb}} \times \frac{453.6 \ \text{g}}{1 \ \cancel{\text{lb}}} = 2041.2 \ \text{g}
$$

Three sig figs from 4.50.

**Answer: $2.04 \times 10^3 \ \text{g}$**

</details>

### Problem 4
Convert $65 \ \text{mi/h}$ to $\text{km/h}$. (Given: $1 \ \text{mi} = 1.609 \ \text{km}$.)

<details>
<summary><strong>Solution</strong></summary>

Only the distance unit changes; hours stay put.

$$
\frac{65 \ \cancel{\text{mi}}}{1 \ \text{h}} \times \frac{1.609 \ \text{km}}{1 \ \cancel{\text{mi}}} = 104.6 \ \text{km/h}
$$

Two sig figs from 65.

**Answer: $1.0 \times 10^2 \ \text{km/h}$ (about 105 km/h)**

</details>

### Problem 5
A whiteboard has an area of $0.35 \ \text{m}^2$. Convert to $\text{cm}^2$.

<details>
<summary><strong>Solution</strong></summary>

Square the whole linear factor:

$$
0.35 \ \cancel{\text{m}^2} \times \left(\frac{100 \ \text{cm}}{1 \ \cancel{\text{m}}}\right)^2 = 0.35 \times 10^4 \ \text{cm}^2 = 3500 \ \text{cm}^2
$$

**Answer: $3.5 \times 10^3 \ \text{cm}^2$**

</details>

### Problem 6
Aluminum ($\ce{Al}$) has a density of $2.70 \ \text{g/cm}^3$. Convert this density to $\text{kg/m}^3$.

<details>
<summary><strong>Solution</strong></summary>

Convert the top (g → kg) and the bottom ($\text{cm}^3 \to \text{m}^3$) separately — and remember to cube the length factor:

$$
\frac{2.70 \ \cancel{\text{g}}}{1 \ \cancel{\text{cm}^3}} \times \frac{1 \ \text{kg}}{1000 \ \cancel{\text{g}}} \times \left(\frac{100 \ \cancel{\text{cm}}}{1 \ \text{m}}\right)^3
= \frac{2.70 \times 10^6}{10^3} \ \frac{\text{kg}}{\text{m}^3} = 2700 \ \frac{\text{kg}}{\text{m}^3}
$$

**Answer: $2.70 \times 10^3 \ \text{kg/m}^3$**

</details>

### Problem 7
A can of soda contains $355 \ \text{mL}$ of liquid with a density of $1.04 \ \text{g/mL}$. What is the mass of the liquid?

<details>
<summary><strong>Solution</strong></summary>

Target is grams, so grams go on top:

$$
355 \ \cancel{\text{mL}} \times \frac{1.04 \ \text{g}}{1 \ \cancel{\text{mL}}} = 369.2 \ \text{g}
$$

Three sig figs.

**Answer: $369 \ \text{g}$**

</details>

### Problem 8
Mercury ($\ce{Hg}$) has a density of $13.6 \ \text{g/mL}$. What volume of mercury has a mass of $75.0 \ \text{g}$?

<details>
<summary><strong>Solution</strong></summary>

Grams must cancel, so flip the density:

$$
75.0 \ \cancel{\text{g}} \times \frac{1 \ \text{mL}}{13.6 \ \cancel{\text{g}}} = 5.51 \ \text{mL}
$$

Sanity check: mercury is extremely dense, so 75 g should be a small volume. ✓

**Answer: $5.51 \ \text{mL}$**

</details>

### Problem 9
Convert $1.50 \ \text{L}$ to $\text{m}^3$. (Hint: $1 \ \text{mL} = 1 \ \text{cm}^3$ exactly.)

<details>
<summary><strong>Solution</strong></summary>

Route: L → mL → $\text{cm}^3$ → $\text{m}^3$.

$$
1.50 \ \cancel{\text{L}} \times \frac{1000 \ \cancel{\text{mL}}}{1 \ \cancel{\text{L}}} \times \frac{1 \ \cancel{\text{cm}^3}}{1 \ \cancel{\text{mL}}} \times \frac{1 \ \text{m}^3}{10^6 \ \cancel{\text{cm}^3}} = 1.50 \times 10^{-3} \ \text{m}^3
$$

**Answer: $1.50 \times 10^{-3} \ \text{m}^3$**

</details>

### Problem 10
A sprinter runs $100.0 \ \text{m}$ in $9.58 \ \text{s}$. What is this speed in miles per hour? (Given: $1 \ \text{mi} = 1609 \ \text{m}$.)

<details>
<summary><strong>Solution</strong></summary>

Build the rate, then convert top and bottom:

$$
\frac{100.0 \ \cancel{\text{m}}}{9.58 \ \cancel{\text{s}}} \times \frac{1 \ \text{mi}}{1609 \ \cancel{\text{m}}} \times \frac{3600 \ \cancel{\text{s}}}{1 \ \text{h}} = 23.35 \ \text{mi/h}
$$

Three sig figs from 9.58.

**Answer: $23.4 \ \text{mi/h}$**

</details>

### Problem 11
How many molecules are in $18.0 \ \text{g}$ of water, $\ce{H2O}$? (Molar mass $= 18.02 \ \text{g/mol}$; $N_A = 6.022 \times 10^{23} \ \text{mol}^{-1}$.)

<details>
<summary><strong>Solution</strong></summary>

Grams → moles → molecules:

$$
18.0 \ \cancel{\text{g}} \times \frac{1 \ \cancel{\text{mol}}}{18.02 \ \cancel{\text{g}}} \times \frac{6.022 \times 10^{23} \ \text{molecules}}{1 \ \cancel{\text{mol}}} = 6.015 \times 10^{23} \ \text{molecules}
$$

Three sig figs.

**Answer: $6.01 \times 10^{23}$ molecules of $\ce{H2O}$**

</details>

### Problem 12
A solution of sodium chloride is labeled $2.00 \ \text{M}$ (that is, $2.00 \ \text{mol}$ of $\ce{NaCl}$ per liter of solution). How many moles of $\ce{NaCl}$ are in $0.250 \ \text{L}$ of this solution?

<details>
<summary><strong>Solution</strong></summary>

Molarity is a conversion factor between liters and moles:

$$
0.250 \ \cancel{\text{L}} \times \frac{2.00 \ \text{mol} \ \ce{NaCl}}{1 \ \cancel{\text{L}}} = 0.500 \ \text{mol}
$$

**Answer: $0.500 \ \text{mol}$ of $\ce{NaCl}$**

</details>

### Problem 13
I average 3 boba drinks per week at \$6.25 each. Treating both numbers as exact, how much do I spend on boba in one year (52 weeks)?

<details>
<summary><strong>Solution</strong></summary>

$$
1 \ \cancel{\text{yr}} \times \frac{52 \ \cancel{\text{wk}}}{1 \ \cancel{\text{yr}}} \times \frac{3 \ \cancel{\text{drinks}}}{1 \ \cancel{\text{wk}}} \times \frac{6.25 \ \text{dollars}}{1 \ \cancel{\text{drink}}} = 975 \ \text{dollars}
$$

(Don't tell Dad.)

**Answer: \$975 per year**

</details>

### Problem 14
The drive from San Diego to LA is $120 \ \text{mi}$. The car gets $28 \ \text{mi/gal}$ and gas costs $4.85 \ \text{dollars/gal}$. What does the one-way trip cost in gas?

<details>
<summary><strong>Solution</strong></summary>

The opener's chain, now official:

$$
120 \ \cancel{\text{mi}} \times \frac{1 \ \cancel{\text{gal}}}{28 \ \cancel{\text{mi}}} \times \frac{4.85 \ \text{dollars}}{1 \ \cancel{\text{gal}}} = 20.79 \ \text{dollars}
$$

Two sig figs from 28 mi/gal.

**Answer: about \$21**

</details>

### Problem 15
Normal saline is $0.90\%$ sodium chloride by mass. How many grams of $\ce{NaCl}$ are in $250.0 \ \text{g}$ of saline solution?

<details>
<summary><strong>Solution</strong></summary>

Percent is the factor $\frac{0.90 \ \text{g} \ \ce{NaCl}}{100 \ \text{g solution}}$ (the 100 is exact):

$$
250.0 \ \cancel{\text{g solution}} \times \frac{0.90 \ \text{g} \ \ce{NaCl}}{100 \ \cancel{\text{g solution}}} = 2.25 \ \text{g}
$$

Two sig figs from 0.90.

**Answer: $2.3 \ \text{g}$ of $\ce{NaCl}$**

</details>

---

## Quick Reference

| Item | The Rule |
|---|---|
| Why it works | Every conversion factor is a fraction equal to 1; multiplying by 1 changes the label, not the quantity |
| Orientation | Put the unit you're eliminating on the **bottom**; if the wrong unit survives, flip |
| Strategy | Write the **target unit first**, build the bridge, cancel on paper, sanity-check magnitude |
| Prefix → prefix | Route through the base unit (mg → g → kg) |
| Squared / cubed units | Raise the **entire** factor: $\left(\frac{100 \ \text{cm}}{1 \ \text{m}}\right)^3 = \frac{10^6 \ \text{cm}^3}{1 \ \text{m}^3}$ |
| Handy exact equalities | $1 \ \text{mL} = 1 \ \text{cm}^3$; $1 \ \text{L} = 1000 \ \text{mL}$; all metric prefixes |
| Density | $\frac{\text{g}}{\text{mL}}$ converts volume ↔ mass (flip as needed) |
| Percent (by mass) | $\frac{x \ \text{g part}}{100 \ \text{g whole}}$, the 100 is exact |
| Sig figs | Exact factors never limit sig figs; measured ones (density, molar mass) do |
| The big chemistry chain | $\text{g} \xrightarrow{\text{molar mass}} \text{mol} \xrightarrow{N_A} \text{particles}$; molarity $= \frac{\text{mol}}{\text{L}}$ |

---

<div align="center">

[← Significant Figures](/chemistry/0102-significant-figures) | [Logarithms for Chemistry →](/chemistry/0104-logarithms-for-chemistry)

</div>
