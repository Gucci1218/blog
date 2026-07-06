# Cell Potential and Electrolysis
<p class="article-date">July 5, 2026</p>

*Two things happened to me on the same ordinary Tuesday, and it turns out they're the same physics wearing different outfits. First: my little sister's cheap earrings — the dull silver-gray kind from the mall — came back from a jewelry kiosk looking like real gold. The guy had dunked them in a tank, clipped on a wire, flipped a switch, and let current run for a while. The longer he ran it, the thicker the gold. That's **electrolysis**: push electrons in with an outside power source and gold atoms literally plate out of solution onto the metal, one atom per few electrons delivered. Second: my phone. It read 100% and a punchy voltage that morning, and by the time I got home it was sagging at 12%, the screen dimmer, the voltage lower. Nobody changed the phone — the **chemistry inside just drained toward equilibrium**, and as the reactants got used up the cell's voltage fell. A dead battery isn't broken; it's a reaction that has finished, sitting at $E = 0$. Here's the beautiful part: counting gold atoms by counting electrons (Faraday's law) and watching a battery fade as $Q$ climbs toward $K$ are the two halves of AP Unit 9's finale — Topics 9.9 and 9.10 — and they pull in stoichiometry, the mole, gas laws, redox, and thermodynamics all at once. This is the last topic of AP Chemistry, and it's where the whole course finally shakes hands with itself.*

---

## What You'll Learn

- Explain **qualitatively** why a running cell's voltage drifts away from $E^\circ$ as concentrations change, using $Q$ and Le Châtelier's reasoning
- State the direction rule: $E < E^\circ$ when $Q > 1$, $E > E^\circ$ when $Q < 1$, and $E = E^\circ$ when $Q = 1$
- Explain why a **dead battery is a cell at equilibrium** — $Q = K$, $E = 0$, and $\Delta G = 0$ all at once
- Predict how raising or lowering the concentration of a reactant or product changes the measured cell voltage
- Reason through a **concentration cell** — same species on both sides, $E^\circ = 0$ yet $E \neq 0$ — and predict its polarity and direction of current
- Describe **electrolysis** as forcing a nonspontaneous redox reaction with an external power source, and name real uses (electroplating, water splitting, aluminum production, recharging batteries)
- Use **Faraday's law** as a railroad: current and time $\to$ charge $q = It$ $\to$ moles of electrons $q/F$ $\to$ moles (and grams) of substance, or gas volume via $PV = nRT$
- Solve Faraday problems in **both directions** — mass deposited from a given current/time, and the current or time needed to deposit a target mass
- Connect the four capstone relationships: $E^\circ$, $\Delta G^\circ = -nFE^\circ$, $\Delta G^\circ = -RT\ln K$, and Faraday stoichiometry — and see electrochemistry as the meeting point of the whole course

---

## Prerequisites

- [Electrochemical Cells](/chemistry/1104-electrochemical-cells) — you must already know galvanic vs. electrolytic cells, half-reactions, anode/cathode, and how $E^\circ$ is built from standard reduction potentials. **This article is the sequel; start there.**
- [Free Energy and Equilibrium](/chemistry/1103-free-energy-equilibrium) — the reaction quotient $Q$, the sign of $\Delta G$, and $\Delta G^\circ = -RT\ln K$ are the engine behind "nonstandard" cell potential
- [Le Châtelier's Principle](/chemistry/0904-le-chatelier) — a cell that drains is a stressed equilibrium; predicting the voltage shift is just predicting the direction the reaction "wants" to go
- [The Mole](/chemistry/0207-the-mole) — Faraday's law is stoichiometry where **electrons are a reactant**, so grams $\leftrightarrow$ moles $\leftrightarrow$ particles fluency is non-negotiable

---

## The Core Concept

### Intuition First

Keep both images side by side, because they are mirror twins.

**The gold-plated earring (electrolysis — Topic 9.10).** Drop the cheap earring into a bath of gold ions, $\ce{Au^3+}$, and hook it to the *negative* terminal of a power supply so electrons are shoved onto it. Now the earring surface is a crowd of free electrons, and any $\ce{Au^3+}$ that drifts by grabs three of them and sticks:

$$\ce{Au^3+ + 3e^- -> Au(s)}$$

Every three electrons the power supply delivers plants exactly one gold atom on the earring. So the coating's thickness is nothing more than an **electron head-count**. Run more current (more electrons per second) or run it longer (more seconds), and you plate more atoms. That's the entire idea of **Faraday's law**: *charge counts atoms.* The reaction is nonspontaneous — gold ions don't leap onto cheap metal for free — so we have to *pay* for it with an external power source. That "paying to force a reaction backward" is what makes it electrolysis.

**The dying phone battery (nonstandard potential — Topic 9.9).** A fresh battery is a galvanic cell loaded with reactants and almost no products. It runs *spontaneously* and hands you a strong voltage. But every second it runs, it eats reactants and spits out products. By Le Châtelier's logic, the reaction has less "push" left — it's closer to being satisfied. The measured voltage $E$ sags below the fresh-cell value $E^\circ$, and keeps sagging. When the reactants and products finally reach the ratio the reaction is happy with — **equilibrium**, $Q = K$ — there is no push left at all. The voltage hits zero. That's a dead battery: not broken, just *done*.

Here is the structural map, twin to twin:

| Gold earring (electrolysis) | Phone battery (nonstandard $E$) |
|---|---|
| We **push** electrons in with a power supply | The cell **pushes** electrons out on its own |
| Reaction is **nonspontaneous** ($\Delta G > 0$, forced) | Reaction is **spontaneous** ($\Delta G < 0$, until it isn't) |
| $\text{current} \times \text{time} = \text{charge} = $ electrons $=$ atoms plated | $E$ falls below $E^\circ$ as $Q$ rises toward $K$ |
| Thicker coat = more charge delivered | Deader battery = $Q$ closer to $K$ |
| Faraday's law is the **quantitative** capstone | $Q$ vs. $K$ is the **qualitative** capstone |

Two topics, one idea seen from opposite ends: **electrons are the currency, and charge is how you count them.**

### Part 1 — Cell Potential Under Nonstandard Conditions (9.9)

Standard potential $E^\circ$ is measured under *standard conditions*: every solute at $1\,\text{M}$, every gas at $1\,\text{bar}$, at a stated temperature. Real cells almost never sit there. The moment a cell operates, concentrations move, so the *actual* potential $E$ differs from $E^\circ$.

**The reaction quotient does the bookkeeping.** Recall $Q$ from [Free Energy and Equilibrium](/chemistry/1103-free-energy-equilibrium): the same "products over reactants" expression as $K$, but evaluated at the *current* concentrations. For a cell reaction, $Q$ tells you how far along the reaction has run.

The exact relationship is the **Nernst equation** (AP treats it *qualitatively* — you will not have to plug into it, but you must reason with it):

$$E = E^\circ - \frac{RT}{nF}\ln Q$$

You only need the *sign logic* buried in that minus sign:

| Situation | What it means | Effect on $E$ |
|---|---|---|
| $Q < 1$ | more reactants than products (fresh cell) | $\ln Q < 0$, so $E > E^\circ$ |
| $Q = 1$ | standard conditions | $E = E^\circ$ |
| $Q > 1$ | more products than reactants (draining cell) | $\ln Q > 0$, so $E < E^\circ$ |
| $Q = K$ | equilibrium (dead battery) | $E = 0$ |

Read it in one sentence: **as a cell runs, $Q$ rises toward $K$, and $E$ falls toward $0$.** That is the whole story of a battery dying over a day.

**The dead-battery triple point.** At equilibrium everything zeroes out together, and you should be able to recite why:

- $Q = K$ (concentrations reached the equilibrium ratio)
- $E = 0$ (no potential difference left to drive electrons)
- $\Delta G = 0$ (no free energy left to release)

These are three sentences describing one moment. Connect them through the two capstone bridges $\Delta G = -nFE$ and, at standard state, $\Delta G^\circ = -nFE^\circ = -RT\ln K$.

**Predicting a voltage shift by Le Châtelier.** You don't need numbers to say which way $E$ moves — just think of the cell reaction as a stressed equilibrium:

- **Increase a reactant concentration** $\Rightarrow$ $Q$ drops $\Rightarrow$ more forward push $\Rightarrow$ **$E$ goes up.**
- **Increase a product concentration** (or the product-side ion) $\Rightarrow$ $Q$ rises $\Rightarrow$ less push $\Rightarrow$ **$E$ goes down.**
- **Remove a product** $\Rightarrow$ $Q$ drops $\Rightarrow$ **$E$ goes up.**

Same reflex you built in [Le Châtelier's Principle](/chemistry/0904-le-chatelier), now reading out as a voltmeter needle.

### Concentration Cells — the Signature AP Trick

Here's the one that looks impossible until it clicks. Build a cell with the **same species on both sides** — say copper metal in $\ce{Cu^2+}$ solution on the left *and* copper metal in $\ce{Cu^2+}$ solution on the right. Since both electrodes are identical, $E^\circ_{\text{cell}} = E^\circ_{\text{cathode}} - E^\circ_{\text{anode}} = 0$.

So the cell is dead, right? **No.** If the two $\ce{Cu^2+}$ concentrations *differ*, there's still a voltage — a small but real one — driven purely by the concentration difference. Nature wants the two sides to become equal, exactly like a drop of dye spreading until the water is one uniform color.

- The **dilute** side wants *more* $\ce{Cu^2+}$, so its copper electrode dissolves: $\ce{Cu -> Cu^2+ + 2e^-}$. That's oxidation $\Rightarrow$ **anode**.
- The **concentrated** side wants *less* $\ce{Cu^2+}$, so ions plate out: $\ce{Cu^2+ + 2e^- -> Cu}$. That's reduction $\Rightarrow$ **cathode**.

Current flows until both concentrations match; then $Q = 1$, $E = 0$, and the cell truly dies. A concentration cell is a machine that runs on *nothing but* the difference between two numbers — $E^\circ = 0$, yet $E \neq 0$. If you can explain that on the exam, you own Topic 9.9.

### Part 2 — Electrolysis (9.10)

An **electrolytic cell** is a galvanic cell run in reverse by brute force. Instead of letting a spontaneous reaction *push out* electrons, you connect an external power supply and *shove electrons in* to drive a **nonspontaneous** reaction ($E^\circ_{\text{cell}} < 0$, $\Delta G > 0$). You are paying, in electrical energy, to make chemistry go uphill.

Same electrode vocabulary, same rules ("**an ox, red cat**" — **an**ode = **ox**idation, **red**uction = **cat**hode), but the power supply sets the polarity:

| | Galvanic (battery, phone) | Electrolytic (plating, forced) |
|---|---|---|
| Spontaneous? | yes, $\Delta G < 0$ | no, $\Delta G > 0$ (forced) |
| Energy | releases electrical energy | consumes electrical energy |
| Cathode (reduction) | $+$ terminal | $-$ terminal (electrons pushed in) |
| Anode (oxidation) | $-$ terminal | $+$ terminal |

**Where you meet it in real life:**

- **Electroplating** — the gold earring. A thin, even metal coat deposited from solution onto an object at the cathode.
- **Electrolysis of water** — split $\ce{H2O}$ into $\ce{H2}$ and $\ce{O2}$: $\ce{2H2O(l) -> 2H2(g) + O2(g)}$. Hydrogen bubbles off the cathode, oxygen off the anode.
- **Producing/purifying metals** — reactive metals like aluminum can't be smelted with heat cheaply, so industry electrolyzes molten $\ce{Al2O3}$ (the Hall–Héroult process). Copper is refined the same way.
- **Recharging a battery** — plugging in your phone forces the drained reaction *backward*, rebuilding the reactants. Charging is electrolysis; discharging is galvanic.

### Part 3 — Faraday's Law: Charge Counts Atoms (the Quantitative Capstone)

This is the calculation the whole course was building toward. It's just stoichiometry — with **electrons as the reactant you can measure with a stopwatch and an ammeter.**

**Step 1 — Charge from current and time.** Current $I$ is charge per second (amperes = coulombs/second). So total charge is

$$q = I \times t \qquad (\text{coulombs} = \text{amperes} \times \text{seconds})$$

Guard your units like your grade depends on it — because it does. **$I$ in amperes, $t$ in seconds.** A time in minutes or hours must be converted first: $A \cdot s = C$.

**Step 2 — Moles of electrons from charge.** One mole of electrons carries a fixed charge called the **Faraday constant**:

$$F = 96485\ \text{C/mol e}^-$$

So

$$n_{e^-} = \frac{q}{F} = \frac{It}{F}$$

**Step 3 — Moles of substance from the half-reaction ratio.** The balanced half-reaction gives electrons per atom. For $\ce{Au^3+ + 3e^- -> Au}$, it's $3$ electrons per gold. For $\ce{Cu^2+ + 2e^- -> Cu}$, $2$ per copper. For $\ce{Ag+ + e^- -> Ag}$, $1$ per silver.

$$n_{\text{substance}} = n_{e^-} \times \frac{1\ \text{mol substance}}{z\ \text{mol e}^-}$$

where $z$ is the electrons in the half-reaction.

**Step 4 — Finish the railroad.** From moles, go wherever the question points, using the tools from [The Mole](/chemistry/0207-the-mole) and [Dimensional Analysis](/chemistry/0103-dimensional-analysis):

- moles $\times$ molar mass $\to$ **grams** of metal plated
- moles $\to$ **volume of gas** via $PV = nRT$ (the [Ideal Gas Law](/chemistry/0504-ideal-gas-law))

The full chain, all in one line — this is the "electrons are the bridge" idea made concrete:

$$I,\,t \;\xrightarrow{\;q=It\;}\; q \;\xrightarrow{\;\div F\;}\; \text{mol }e^- \;\xrightarrow{\;\text{half-rxn ratio}\;}\; \text{mol substance} \;\xrightarrow{\;M \text{ or } PV=nRT\;}\; \text{grams or liters}$$

Every arrow is a unit conversion you already know. Faraday's law just adds the electron as the connecting piece.

---

## Worked Examples

### Example 1: Which way does the voltage move? (qualitative $Q$)

**Problem:** A galvanic cell runs on $\ce{Zn(s) + Cu^2+(aq) -> Zn^2+(aq) + Cu(s)}$, with $E^\circ = +1.10\ \text{V}$. You *increase* the $\ce{Cu^2+}$ concentration. Does the measured voltage rise or fall?

**Solution:**
- Step 1: Write $Q = \dfrac{[\ce{Zn^2+}]}{[\ce{Cu^2+}]}$ (solids don't appear).
- Step 2: Raising $[\ce{Cu^2+}]$ makes the denominator bigger, so **$Q$ decreases**.
- Step 3: Smaller $Q$ ($Q < 1$ region) means $E > E^\circ$. More reactant = more push.

**Answer:** The voltage **rises above** $1.10\ \text{V}$. (Adding reactant strengthens the cell — exactly Le Châtelier.)

### Example 2: The battery draining over the day

**Problem:** Explain, in terms of $Q$ and $K$, why the same $\ce{Zn}/\ce{Cu^2+}$ cell reads a lower voltage after running for hours, and what a reading of exactly $0\ \text{V}$ would mean.

**Solution:**
- As it runs, $\ce{Cu^2+}$ is consumed and $\ce{Zn^2+}$ is produced, so $Q = \frac{[\ce{Zn^2+}]}{[\ce{Cu^2+}]}$ climbs.
- Rising $Q$ pushes $E = E^\circ - \frac{RT}{nF}\ln Q$ downward — the voltage sags.
- When $Q$ finally equals $K$, the reaction is at equilibrium: no net drive.

**Answer:** The voltage falls because $Q$ rises toward $K$. A reading of $0\ \text{V}$ means $Q = K$ — the cell is at **equilibrium** ($\Delta G = 0$): a **dead battery**.

### Example 3: Reasoning through a concentration cell

**Problem:** A cell has a silver electrode in $0.010\ \text{M}\ \ce{Ag+}$ on the left and a silver electrode in $1.0\ \text{M}\ \ce{Ag+}$ on the right. What is $E^\circ_{\text{cell}}$? Which electrode is the cathode, and which way do electrons flow?

**Solution:**
- Step 1: Both half-cells are the same reaction $\ce{Ag+ + e^- -> Ag}$, so $E^\circ_{\text{cell}} = E^\circ_{\text{cat}} - E^\circ_{\text{an}} = 0$.
- Step 2: Nature wants the concentrations equal. The **dilute** ($0.010\ \text{M}$) side needs *more* $\ce{Ag+}$ $\Rightarrow$ its silver dissolves, $\ce{Ag -> Ag+ + e^-}$ $\Rightarrow$ that's the **anode**.
- Step 3: The **concentrated** ($1.0\ \text{M}$) side plates out $\ce{Ag+ + e^- -> Ag}$ $\Rightarrow$ **cathode**.

**Answer:** $E^\circ_{\text{cell}} = 0$, but $E > 0$ because the concentrations differ. The **concentrated side is the cathode**; electrons flow through the wire **from the dilute side to the concentrated side**, until both reach the same concentration and $E \to 0$.

### Example 4: Gold on the earring — mass plated

**Problem:** An earring is plated from $\ce{Au^3+}$ solution at a current of $0.50\ \text{A}$ for $20.0\ \text{minutes}$. What mass of gold is deposited? ($M_{\ce{Au}} = 197.0\ \text{g/mol}$.)

**Solution:**
- Step 1 — charge: $t = 20.0\ \text{min} \times 60 = 1200\ \text{s}$, so $q = It = 0.50 \times 1200 = 600\ \text{C}$.
- Step 2 — moles of electrons: $n_{e^-} = \dfrac{600}{96485} = 6.22 \times 10^{-3}\ \text{mol e}^-$.
- Step 3 — half-reaction ratio: $\ce{Au^3+ + 3e^- -> Au}$, so $n_{\ce{Au}} = \dfrac{6.22 \times 10^{-3}}{3} = 2.07 \times 10^{-3}\ \text{mol}$.
- Step 4 — grams: $m = 2.07 \times 10^{-3} \times 197.0 = 0.408\ \text{g}$.

**Answer:** About **$0.41\ \text{g}$ of gold** plates onto the earring.

### Example 5: Run it stronger, run it longer

**Problem:** Using the same setup as Example 4, your sister wants a *thicker* coat — double the current (to $1.0\ \text{A}$) **and** double the time (to $40.0\ \text{min}$). How much gold now?

**Solution:**
- Charge scales with both: $q = It = 1.0 \times 2400 = 2400\ \text{C}$ — that's $4\times$ the original $600\ \text{C}$.
- Since mass is directly proportional to charge, the gold is $4 \times 0.408 = 1.63\ \text{g}$.

**Answer:** **$1.63\ \text{g}$** — four times as much. This is the whole point of Faraday's law: *stronger and longer* both add charge, and charge counts atoms.

### Example 6: How long to plate a target mass?

**Problem:** You want to deposit exactly $1.00\ \text{g}$ of silver from $\ce{Ag+}$ at a current of $2.00\ \text{A}$. How long must the current run? ($M_{\ce{Ag}} = 107.9\ \text{g/mol}$; $\ce{Ag+ + e^- -> Ag}$.)

**Solution:**
- Step 1 — moles of silver: $n_{\ce{Ag}} = \dfrac{1.00}{107.9} = 9.27 \times 10^{-3}\ \text{mol}$.
- Step 2 — moles of electrons: ratio is $1:1$, so $n_{e^-} = 9.27 \times 10^{-3}\ \text{mol}$.
- Step 3 — charge: $q = n_{e^-} \times F = 9.27 \times 10^{-3} \times 96485 = 894\ \text{C}$.
- Step 4 — time: $t = \dfrac{q}{I} = \dfrac{894}{2.00} = 447\ \text{s} \approx 7.5\ \text{min}$.

**Answer:** About **$447\ \text{s}$ (≈ 7.5 minutes)**. Notice we ran the railroad *backward* — target mass $\to$ moles $\to$ electrons $\to$ charge $\to$ time.

### Example 7: What current do I need?

**Problem:** A factory must plate $5.00\ \text{g}$ of copper from $\ce{Cu^2+}$ in exactly $30.0\ \text{minutes}$. What constant current is required? ($M_{\ce{Cu}} = 63.55\ \text{g/mol}$; $\ce{Cu^2+ + 2e^- -> Cu}$.)

**Solution:**
- Step 1 — moles of copper: $n_{\ce{Cu}} = \dfrac{5.00}{63.55} = 0.0787\ \text{mol}$.
- Step 2 — moles of electrons: ratio $2:1$, so $n_{e^-} = 2 \times 0.0787 = 0.1574\ \text{mol}$.
- Step 3 — charge: $q = 0.1574 \times 96485 = 1.519 \times 10^{4}\ \text{C}$.
- Step 4 — current: $t = 30.0\ \text{min} \times 60 = 1800\ \text{s}$, so $I = \dfrac{q}{t} = \dfrac{1.519 \times 10^{4}}{1800} = 8.44\ \text{A}$.

**Answer:** About **$8.44\ \text{A}$.**

### Example 8: The electron ratio matters — same charge, different metals

**Problem:** The same charge of $9.65 \times 10^{4}\ \text{C}$ (that's exactly $1\ \text{mol e}^-$) is passed separately through solutions of $\ce{Ag+}$, $\ce{Cu^2+}$, and $\ce{Al^3+}$. How many moles of each metal deposit?

**Solution:**
- $1\ \text{mol e}^-$ delivered (since $q/F = 96500/96485 \approx 1.00$).
- $\ce{Ag+ + e^- -> Ag}$: $1\ \text{mol e}^- \to 1\ \text{mol Ag}$.
- $\ce{Cu^2+ + 2e^- -> Cu}$: $1\ \text{mol e}^- \to 0.500\ \text{mol Cu}$.
- $\ce{Al^3+ + 3e^- -> Al}$: $1\ \text{mol e}^- \to 0.333\ \text{mol Al}$.

**Answer:** $1.00\ \text{mol Ag}$, $0.500\ \text{mol Cu}$, $0.333\ \text{mol Al}$. **The charge is identical, but the half-reaction ratio changes the atom count** — never skip Step 3.

### Example 9: Gas volume from electrolysis of water

**Problem:** Water is electrolyzed at $1.50\ \text{A}$ for $1.00\ \text{hour}$. What volume of $\ce{H2}$ gas is produced at STP? (Cathode: $\ce{2H2O + 2e^- -> H2 + 2OH^-}$.)

**Solution:**
- Step 1 — charge: $t = 3600\ \text{s}$, $q = 1.50 \times 3600 = 5400\ \text{C}$.
- Step 2 — moles of electrons: $n_{e^-} = \dfrac{5400}{96485} = 0.0560\ \text{mol}$.
- Step 3 — moles of $\ce{H2}$: ratio is $2\ \text{e}^-$ per $\ce{H2}$, so $n_{\ce{H2}} = \dfrac{0.0560}{2} = 0.0280\ \text{mol}$.
- Step 4 — volume via $PV = nRT$ at STP ($P = 1.00\ \text{atm}$, $T = 273\ \text{K}$): $V = \dfrac{nRT}{P} = \dfrac{(0.0280)(0.0821)(273)}{1.00} = 0.627\ \text{L}$.

**Answer:** About **$0.63\ \text{L}$ of $\ce{H2}$** (≈ 630 mL). This is the [gas law](/chemistry/0504-ideal-gas-law) tacked onto the end of the Faraday railroad.

### Example 10: The $E^\circ$ / $\Delta G^\circ$ / $K$ / Faraday web

**Problem:** A cell reaction transfers $n = 2$ mol of electrons and has $E^\circ = +0.80\ \text{V}$. Find $\Delta G^\circ$, and state whether $K$ is greater than or less than $1$.

**Solution:**
- Step 1 — free energy: $\Delta G^\circ = -nFE^\circ = -(2)(96485)(0.80) = -1.54 \times 10^{5}\ \text{J} = -154\ \text{kJ}$.
- Step 2 — spontaneity: $E^\circ > 0 \Rightarrow \Delta G^\circ < 0 \Rightarrow$ reaction is spontaneous under standard conditions.
- Step 3 — link to $K$: since $\Delta G^\circ = -RT\ln K < 0$, we need $\ln K > 0$, so $K > 1$.

**Answer:** $\Delta G^\circ = -154\ \text{kJ}$, and $K > 1$. The three descriptions — positive $E^\circ$, negative $\Delta G^\circ$, and $K > 1$ — are one fact in three languages.

### Example 11: Electrolysis is forced — the sign flip

**Problem:** The reaction $\ce{2H2O -> 2H2 + O2}$ has $E^\circ_{\text{cell}} = -1.23\ \text{V}$. What does the negative sign tell you, and what is the minimum voltage needed to drive it?

**Solution:**
- $E^\circ_{\text{cell}} < 0$ means $\Delta G^\circ = -nFE^\circ > 0$: the reaction is **nonspontaneous**. Water will not split on its own.
- To force it, the external power supply must apply a voltage that overcomes $1.23\ \text{V}$ (in practice, more, due to real-world overpotential).

**Answer:** The negative $E^\circ$ marks a nonspontaneous reaction; you must supply **at least $1.23\ \text{V}$** from an external source. That "supplying voltage to force it uphill" is the definition of electrolysis.

### Example 12: The whole-course capstone in one problem

**Problem:** How many grams of aluminum are produced when a current of $1.00 \times 10^{4}\ \text{A}$ runs through molten $\ce{Al2O3}$ for $2.00\ \text{hours}$? ($\ce{Al^3+ + 3e^- -> Al}$; $M_{\ce{Al}} = 26.98\ \text{g/mol}$.) Then name the units of the course this single calculation touched.

**Solution:**
- Step 1 — charge: $t = 2.00\ \text{h} \times 3600 = 7200\ \text{s}$; $q = It = (1.00 \times 10^{4})(7200) = 7.20 \times 10^{7}\ \text{C}$.
- Step 2 — moles of electrons: $n_{e^-} = \dfrac{7.20 \times 10^{7}}{96485} = 746\ \text{mol e}^-$.
- Step 3 — moles of Al: $\dfrac{746}{3} = 249\ \text{mol Al}$.
- Step 4 — grams: $m = 249 \times 26.98 = 6.71 \times 10^{3}\ \text{g} \approx 6.71\ \text{kg}$.

**Answer:** About **$6.71\ \text{kg}$ of aluminum.** This one problem used **dimensional analysis** (U0), **the mole** (U0), **redox half-reactions** (U4), **stoichiometry** (U4), and **thermodynamics** (U9, via the forced nonspontaneous reaction) — electrochemistry is where the entire course meets.

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Forgetting to convert time to **seconds** | Problems give minutes or hours; $I$ is coulombs *per second* | Convert first: $q = It$ needs $t$ in **seconds**. $A \cdot s = C$. |
| Skipping the half-reaction electron ratio | Treating moles of electrons as moles of metal | Always divide by $z$ (electrons per atom): $\ce{Au^3+}$ needs $\div 3$, $\ce{Cu^2+}$ needs $\div 2$. |
| Saying a concentration cell has $E = 0$ | "Same species both sides, so no voltage" | $E^\circ = 0$, but $E \neq 0$ whenever the **concentrations differ**. |
| Getting the voltage-shift direction backward | Confusing "add reactant" with "add product" | Write $Q$, see which way it moves; more reactant $\Rightarrow$ smaller $Q$ $\Rightarrow$ higher $E$. |
| Thinking a dead battery is "broken" | Everyday intuition | A dead battery is at **equilibrium**: $Q = K$, $E = 0$, $\Delta G = 0$. |
| Mixing up electrolytic and galvanic cathode polarity | Memorizing "cathode = +" from batteries | Cathode is always **reduction**; its *sign* flips ($-$ in electrolytic, $+$ in galvanic). |
| Using $F$ as $96485\ \text{J}$ | Confusing coulombs with joules | $F = 96485\ \text{C/mol e}^-$. Joules only appear via $\Delta G = -nFE$ (C × V = J). |
| Forgetting that charging = electrolysis | Thinking a battery only ever discharges | Recharging **forces the reaction backward** with external power — it's electrolysis. |

---

## AP Exam Tips

- **$E$ drops as $Q$ rises.** The single most-tested 9.9 idea: as a cell operates, products build up, $Q$ increases, and the voltage falls. A **dead battery is at equilibrium** ($Q = K$, $E = 0$, $\Delta G = 0$) — be ready to write all three.
- **Nernst is qualitative on AP.** You won't plug into $E = E^\circ - \frac{RT}{nF}\ln Q$, but you must reason with its sign: $Q > 1 \Rightarrow E < E^\circ$; $Q < 1 \Rightarrow E > E^\circ$.
- **Concentration cells are a signature question.** $E^\circ = 0$ but $E \neq 0$; the **dilute side is the anode** (dissolves to make ions), the **concentrated side is the cathode** (ions plate out). Current flows until concentrations equalize.
- **Faraday discipline: $q = It$, then $\div F$, then the half-reaction ratio.** Keep units clean — **amperes × seconds = coulombs**. A minutes/hours slip is the most common lost point on the whole FRQ.
- **Electrons are the stoichiometric bridge.** Treat $\text{e}^-$ like any reactant in a mole-ratio problem. The chain is charge $\to$ mol e$^-$ $\to$ mol substance $\to$ grams (or liters via $PV = nRT$).
- **Electrolysis = forced.** Negative $E^\circ_{\text{cell}}$ means nonspontaneous ($\Delta G > 0$); an external power source is *required*. Watch for the polarity flip in electrolytic cells.
- **Know the four-way web cold:** $\Delta G^\circ = -nFE^\circ$ and $\Delta G^\circ = -RT\ln K$. Positive $E^\circ$ $\Leftrightarrow$ negative $\Delta G^\circ$ $\Leftrightarrow$ $K > 1$ $\Leftrightarrow$ spontaneous. FRQs love making you cross between them.
- **This is the course finale.** Electrochemistry FRQs deliberately fold in stoichiometry, the mole, gas laws, and thermodynamics — expect a multi-part problem that walks the whole railroad.

---

## Practice Problems

### Problem 1
A galvanic cell runs on $\ce{Zn + Cu^2+ -> Zn^2+ + Cu}$. You *increase* $[\ce{Zn^2+}]$. Does the cell voltage rise, fall, or stay the same? Explain using $Q$.

<details>
<summary><strong>Solution</strong></summary>

$Q = \dfrac{[\ce{Zn^2+}]}{[\ce{Cu^2+}]}$. Raising $[\ce{Zn^2+}]$ increases the numerator, so $Q$ **increases**. Larger $Q$ means $E < E^\circ$.

**Answer: The voltage falls** — you added product, which pushes the reaction backward.

</details>

---

### Problem 2
In one or two sentences, explain why a battery that reads $0\ \text{V}$ is said to be "at equilibrium." Give the values of $Q$, $E$, and $\Delta G$.

<details>
<summary><strong>Solution</strong></summary>

As the cell runs, reactants convert to products until the concentrations reach the equilibrium ratio. At that point there is no net driving force.

**Answer: $Q = K$, $E = 0$, and $\Delta G = 0$** — the reaction has finished; the "dead" battery is simply at equilibrium.

</details>

---

### Problem 3
A cell is built with a copper electrode in $0.0010\ \text{M}\ \ce{Cu^2+}$ and another copper electrode in $1.0\ \text{M}\ \ce{Cu^2+}$. What is $E^\circ_{\text{cell}}$? Which electrode is the anode?

<details>
<summary><strong>Solution</strong></summary>

Identical half-cells $\Rightarrow E^\circ_{\text{cell}} = 0$. The dilute ($0.0010\ \text{M}$) side wants more $\ce{Cu^2+}$, so its electrode dissolves ($\ce{Cu -> Cu^2+ + 2e^-}$) — oxidation.

**Answer: $E^\circ_{\text{cell}} = 0$; the dilute-side electrode is the anode.** (But $E \neq 0$ because the concentrations differ.)

</details>

---

### Problem 4
A current of $1.20\ \text{A}$ flows for $15.0\ \text{minutes}$. How many coulombs of charge is that, and how many moles of electrons?

<details>
<summary><strong>Solution</strong></summary>

$t = 15.0 \times 60 = 900\ \text{s}$. $q = It = 1.20 \times 900 = 1080\ \text{C}$.

$n_{e^-} = \dfrac{1080}{96485} = 1.12 \times 10^{-2}\ \text{mol e}^-$.

**Answer: $1080\ \text{C}$ and $1.12 \times 10^{-2}\ \text{mol e}^-$.**

</details>

---

### Problem 5
How many grams of silver are deposited from $\ce{Ag+}$ by a current of $3.00\ \text{A}$ running for $10.0\ \text{minutes}$? ($M_{\ce{Ag}} = 107.9\ \text{g/mol}$.)

<details>
<summary><strong>Solution</strong></summary>

$q = 3.00 \times 600 = 1800\ \text{C}$. $n_{e^-} = \dfrac{1800}{96485} = 0.01866\ \text{mol}$. Ratio $1:1$ for $\ce{Ag+ + e^- -> Ag}$, so $n_{\ce{Ag}} = 0.01866\ \text{mol}$. $m = 0.01866 \times 107.9 = 2.01\ \text{g}$.

**Answer: about $2.01\ \text{g}$ of silver.**

</details>

---

### Problem 6
How long must a $2.50\ \text{A}$ current run to plate $2.00\ \text{g}$ of copper from $\ce{Cu^2+}$? ($M_{\ce{Cu}} = 63.55\ \text{g/mol}$.)

<details>
<summary><strong>Solution</strong></summary>

$n_{\ce{Cu}} = \dfrac{2.00}{63.55} = 0.03147\ \text{mol}$. Ratio $2:1$, so $n_{e^-} = 0.06294\ \text{mol}$. $q = 0.06294 \times 96485 = 6073\ \text{C}$. $t = \dfrac{q}{I} = \dfrac{6073}{2.50} = 2429\ \text{s} \approx 40.5\ \text{min}$.

**Answer: about $2429\ \text{s}$ (≈ 40.5 minutes).**

</details>

---

### Problem 7
What constant current will deposit $0.500\ \text{g}$ of gold from $\ce{Au^3+}$ in exactly $10.0\ \text{minutes}$? ($M_{\ce{Au}} = 197.0\ \text{g/mol}$.)

<details>
<summary><strong>Solution</strong></summary>

$n_{\ce{Au}} = \dfrac{0.500}{197.0} = 2.538 \times 10^{-3}\ \text{mol}$. Ratio $3:1$, so $n_{e^-} = 7.614 \times 10^{-3}\ \text{mol}$. $q = 7.614 \times 10^{-3} \times 96485 = 734.6\ \text{C}$. $t = 600\ \text{s}$, so $I = \dfrac{734.6}{600} = 1.22\ \text{A}$.

**Answer: about $1.22\ \text{A}$.**

</details>

---

### Problem 8
The same charge of $2.00\ \text{mol e}^-$ is passed through separate solutions of $\ce{Ag+}$, $\ce{Ni^2+}$, and $\ce{Cr^3+}$. Find the moles of each metal deposited.

<details>
<summary><strong>Solution</strong></summary>

- $\ce{Ag+ + e^- -> Ag}$: $2.00\ \text{mol e}^- \to 2.00\ \text{mol Ag}$.
- $\ce{Ni^2+ + 2e^- -> Ni}$: $\to 1.00\ \text{mol Ni}$.
- $\ce{Cr^3+ + 3e^- -> Cr}$: $\to 0.667\ \text{mol Cr}$.

**Answer: $2.00\ \text{mol Ag}$, $1.00\ \text{mol Ni}$, $0.667\ \text{mol Cr}$** — same charge, different atom counts because of the electron ratio.

</details>

---

### Problem 9
Molten $\ce{NaCl}$ is electrolyzed at the cathode ($\ce{Na+ + e^- -> Na}$). A current of $5.00\ \text{A}$ runs for $2.00\ \text{hours}$. What mass of sodium is produced? ($M_{\ce{Na}} = 22.99\ \text{g/mol}$.)

<details>
<summary><strong>Solution</strong></summary>

$t = 7200\ \text{s}$; $q = 5.00 \times 7200 = 36000\ \text{C}$. $n_{e^-} = \dfrac{36000}{96485} = 0.3731\ \text{mol}$. Ratio $1:1$, so $n_{\ce{Na}} = 0.3731\ \text{mol}$. $m = 0.3731 \times 22.99 = 8.58\ \text{g}$.

**Answer: about $8.58\ \text{g}$ of sodium.**

</details>

---

### Problem 10
During the electrolysis of water, a current of $2.00\ \text{A}$ runs for $30.0\ \text{minutes}$. What volume of $\ce{O2}$ gas forms at STP? (Anode: $\ce{2H2O -> O2 + 4H^+ + 4e^-}$.)

<details>
<summary><strong>Solution</strong></summary>

$q = 2.00 \times 1800 = 3600\ \text{C}$. $n_{e^-} = \dfrac{3600}{96485} = 0.03731\ \text{mol}$. Ratio: $4\ \text{e}^-$ per $\ce{O2}$, so $n_{\ce{O2}} = \dfrac{0.03731}{4} = 9.328 \times 10^{-3}\ \text{mol}$. At STP: $V = \dfrac{nRT}{P} = \dfrac{(9.328 \times 10^{-3})(0.0821)(273)}{1.00} = 0.209\ \text{L}$.

**Answer: about $0.209\ \text{L}$ (≈ 209 mL) of $\ce{O2}$.**

</details>

---

### Problem 11
A cell reaction has $n = 2$ and $E^\circ = -0.45\ \text{V}$. Compute $\Delta G^\circ$. Is the reaction spontaneous? Is $K$ greater or less than $1$?

<details>
<summary><strong>Solution</strong></summary>

$\Delta G^\circ = -nFE^\circ = -(2)(96485)(-0.45) = +8.68 \times 10^{4}\ \text{J} = +86.8\ \text{kJ}$.

$\Delta G^\circ > 0 \Rightarrow$ **nonspontaneous**. Since $\Delta G^\circ = -RT\ln K > 0$, $\ln K < 0$, so **$K < 1$**.

**Answer: $\Delta G^\circ = +86.8\ \text{kJ}$; nonspontaneous; $K < 1$.**

</details>

---

### Problem 12
Explain why recharging your phone is an example of electrolysis, and identify whether the internal reaction is spontaneous during charging.

<details>
<summary><strong>Solution</strong></summary>

While discharging, the battery runs a spontaneous galvanic reaction ($\Delta G < 0$). Charging forces that reaction *backward* — rebuilding the reactants — which is nonspontaneous ($\Delta G > 0$) and requires the wall charger to push electrons uphill.

**Answer: Charging drives a nonspontaneous reaction with an external power source — the definition of electrolysis.** The internal reaction during charging is nonspontaneous.

</details>

---

### Problem 13
Two hydrogen electrodes sit in solutions of different $[\ce{H+}]$: one at pH 1 and one at pH 4. Treating this as a concentration cell, which electrode (low pH or high pH) is the cathode? Briefly justify.

<details>
<summary><strong>Solution</strong></summary>

The cell drives toward equal $[\ce{H+}]$. The **high-$[\ce{H+}]$** side (pH 1) reduces $\ce{H+}$ ($\ce{2H+ + 2e^- -> H2}$) to consume its excess ions — that's reduction, the **cathode**. The low-$[\ce{H+}]$ side (pH 4) is the anode.

**Answer: the pH 1 (high $[\ce{H+}]$) electrode is the cathode.** $E^\circ = 0$, but the pH difference gives a real $E > 0$.

</details>

---

### Problem 14
A copper-plating tank runs at $10.0\ \text{A}$. Your boss wants $50.0\ \text{g}$ of copper plated. How many minutes will it take? ($M_{\ce{Cu}} = 63.55\ \text{g/mol}$, $\ce{Cu^2+ + 2e^- -> Cu}$.)

<details>
<summary><strong>Solution</strong></summary>

$n_{\ce{Cu}} = \dfrac{50.0}{63.55} = 0.7868\ \text{mol}$. $n_{e^-} = 2 \times 0.7868 = 1.5736\ \text{mol}$. $q = 1.5736 \times 96485 = 1.518 \times 10^{5}\ \text{C}$. $t = \dfrac{q}{I} = \dfrac{1.518 \times 10^{5}}{10.0} = 1.518 \times 10^{4}\ \text{s} = 253\ \text{min} \approx 4.2\ \text{h}$.

**Answer: about $1.52 \times 10^{4}\ \text{s}$, i.e. roughly 253 minutes (≈ 4.2 hours).**

</details>

---

### Problem 15
A galvanic cell has $E^\circ = +1.10\ \text{V}$ with $n = 2$. (a) Find $\Delta G^\circ$. (b) A student increases the product-ion concentration mid-run. State qualitatively what happens to the measured cell voltage and to $Q$.

<details>
<summary><strong>Solution</strong></summary>

(a) $\Delta G^\circ = -nFE^\circ = -(2)(96485)(1.10) = -2.12 \times 10^{5}\ \text{J} = -212\ \text{kJ}$ (spontaneous).

(b) Adding product raises $Q$. From $E = E^\circ - \frac{RT}{nF}\ln Q$, a larger $Q$ lowers $E$.

**Answer: (a) $\Delta G^\circ = -212\ \text{kJ}$. (b) $Q$ increases and the measured voltage falls below $1.10\ \text{V}$.**

</details>

---

## Quick Reference

**Nonstandard potential (Topic 9.9) — qualitative**

| Condition | Relationship | Meaning |
|---|---|---|
| $Q < 1$ | $E > E^\circ$ | more reactants; extra push (fresh cell) |
| $Q = 1$ | $E = E^\circ$ | standard conditions |
| $Q > 1$ | $E < E^\circ$ | more products; weaker (draining) |
| $Q = K$ | $E = 0$ | equilibrium — **dead battery**, $\Delta G = 0$ |

**Concentration cell:** same species both sides $\Rightarrow E^\circ = 0$, but $E \neq 0$ if concentrations differ. Dilute side = **anode** (dissolves); concentrated side = **cathode** (plates). Runs until concentrations equalize.

**Faraday's law railroad (Topic 9.10)**

$$q = It \quad\to\quad n_{e^-} = \frac{q}{F} \quad\to\quad n_{\text{sub}} = \frac{n_{e^-}}{z} \quad\to\quad \text{grams } (\times M) \text{ or liters } (PV=nRT)$$

- $F = 96485\ \text{C/mol e}^-$
- Units: **amperes × seconds = coulombs**; convert minutes/hours to seconds first
- $z$ = electrons per atom from the half-reaction ($\ce{Ag+}\!:1$, $\ce{Cu^2+}\!:2$, $\ce{Au^3+},\ce{Al^3+}\!:3$)

**The capstone web**

$$\Delta G^\circ = -nFE^\circ \qquad \Delta G^\circ = -RT\ln K \qquad \Rightarrow \qquad E^\circ = \frac{RT}{nF}\ln K$$

| $E^\circ$ | $\Delta G^\circ$ | $K$ | Reaction |
|---|---|---|---|
| $> 0$ | $< 0$ | $> 1$ | spontaneous (galvanic) |
| $= 0$ | $= 0$ | $= 1$ | at equilibrium |
| $< 0$ | $> 0$ | $< 1$ | nonspontaneous (needs electrolysis) |

**Electrolysis:** forces a nonspontaneous reaction with external power. Cathode is still reduction (but the $-$ terminal); anode is still oxidation (the $+$ terminal). Charging a battery = electrolysis.

> **The finish line.** This is the last topic of AP Chemistry. Faraday's law alone touches the mole (U0), dimensional analysis (U0), gas laws (U3), redox and stoichiometry (U4), and thermodynamics (U9). Electrochemistry is where the whole course meets — congratulations on making it here.

---

<div align="center">

[← Electrochemical Cells](/chemistry/1104-electrochemical-cells)

</div>
