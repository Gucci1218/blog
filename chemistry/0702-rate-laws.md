# Rate Laws and the Method of Initial Rates
<p class="article-date">July 5, 2026</p>

*My grandma makes a salsa that has ruined every jarred salsa for me forever, and she will NOT give up the recipe. "A little of this, a little of that," she says, smiling, knowing exactly what she's doing. So this summer I decided to reverse-engineer it like a detective. My rule: change exactly ONE ingredient per batch and hold everything else identical, then taste what happens. Batch with double the lime? Twice as tangy — lime clearly matters. Batch with double the jalapeño? Not twice as spicy, **four times** as spicy — jalapeño matters way more. Batch with double the salt? Tasted exactly the same — turns out the salt was already maxed out and doubling it did nothing. Without ever seeing her handwriting, I was measuring how strongly each ingredient controls the flavor. That is EXACTLY what chemists do to a reaction: change one reactant's concentration at a time, watch how fast the reaction responds, and deduce each reactant's "order." This is AP Unit 5, Topic 5.2 — the **rate law** — and it's the single most tested idea in all of kinetics.*

---

## What You'll Learn
- Write a rate law in the form $\text{rate} = k[\ce{A}]^m[\ce{B}]^n$ and explain what every symbol means
- Understand that the orders $m$ and $n$ are found **by experiment**, NOT read off the balanced equation's coefficients (the #1 misconception in this unit)
- Interpret zero, first, and second order using the "what happens when I double it" test
- Calculate the **overall order** of a reaction as the sum of the individual orders
- Use the **method of initial rates** — the ratio trick — to determine each reactant's order from a data table
- Solve for the rate constant $k$ and state it with the correct **units** (and know why the units reveal the overall order)
- Write the complete rate law and use it to **predict** the rate at brand-new concentrations
- Handle non-integer concentration ratios, using logarithms when the ratio isn't clean
- Explain, with a counterexample, why the rate law can never be trusted to the coefficients

---

## Prerequisites
- [Reaction Rates](/chemistry/0701-reaction-rates) — you need to know what "rate" means (change in concentration per unit time) before we can write a law that predicts it
- [Logarithms for Chemistry](/chemistry/0104-logarithms-for-chemistry) — for the messy tables where the order won't pop out by inspection, logs finish the job
- [Scientific Notation](/chemistry/0101-scientific-notation) — initial-rate data comes as tiny numbers like $2.4 \times 10^{-4}$, and you'll divide them constantly

---

## The Core Concept

### Intuition First

Back to Grandma's salsa. I want to know *how much each ingredient controls the final flavor*. The detective's trick is to be ruthlessly controlled: I brew batch after batch, and between any two batches I let **only one ingredient change** while everything else stays frozen. That way, whatever changes in the taste has to be caused by that one ingredient — nothing else could have done it.

Here's what my three key comparisons told me:

| Ingredient | What I did | What happened to the flavor | What it means |
|---|---|---|---|
| **Lime** | doubled it | flavor got **2×** stronger | doubling $\to 2\times$ effect: **first power** |
| **Jalapeño** | doubled it | flavor got **4×** stronger | doubling $\to 4\times$ effect: **second power** |
| **Salt** | doubled it | flavor **didn't change at all** | doubling $\to$ no effect: **zero power** |

Look at the numbers hiding in that last column. When I doubled the lime and the effect doubled, that's $2 = 2^1$ — an exponent of **1**. When I doubled the jalapeño and the effect quadrupled, that's $4 = 2^2$ — an exponent of **2**. When I doubled the salt and nothing happened, that's $1 = 2^0$ — an exponent of **0**. Every ingredient has a number that says how strongly doubling it matters, and that number lives in an exponent.

Now here is the beautiful part: a chemical reaction behaves *identically*. The "ingredients" are the **reactants**. The "flavor strength" is the **reaction rate** — how fast product appears. And the exponent that tells you how strongly doubling a reactant's concentration changes the rate is called that reactant's **order**. The whole recipe, written as a formula, is the **rate law**.

The salt lesson is the one students never forget: **some reactants don't affect the rate at all.** Just because a chemical is written on the left side of the equation does not mean cranking up its concentration speeds anything up. You cannot know a reactant's order until you *test* it — batch by batch — exactly like I couldn't guess the salt was maxed out until I tried doubling it and tasted nothing new.

### The Rate Law

For a general reaction $\ce{A + B -> products}$, the **rate law** is an experimentally determined equation of the form:

$$\text{rate} = k[\ce{A}]^m[\ce{B}]^n$$

Let's name every piece:

- $[\ce{A}]$ and $[\ce{B}]$ are the **molar concentrations** of the reactants (in $\text{M}$, i.e. $\text{mol/L}$).
- $m$ is the **order with respect to A**; $n$ is the **order with respect to B**. These are the exponents — the "how much doubling matters" numbers.
- $k$ is the **rate constant** — a fixed number (for a given temperature) that sets the overall speed. Bigger $k$ = faster reaction.
- The **overall order** is the sum of the individual orders: $m + n$.

> **The single most important sentence in this unit:** the orders $m$ and $n$ come from **EXPERIMENT**, not from the coefficients in the balanced equation. You must measure them. You cannot read them off the reaction.

### What each order *means* (the doubling test)

The cleanest way to feel an order is to ask: *if I double this reactant's concentration and hold everything else fixed, what does the rate do?* Because the reactant sits under an exponent, doubling it multiplies the rate by $2^{\text{order}}$.

| Order | Double the concentration $\to$ rate is multiplied by | Salsa analogy | In words |
|---|---|---|---|
| **0** (zero order) | $2^0 = 1$ (**no change**) | the maxed-out salt | rate doesn't depend on this reactant at all |
| **1** (first order) | $2^1 = 2$ (**doubles**) | the lime | rate scales in direct proportion |
| **2** (second order) | $2^2 = 4$ (**quadruples**) | the jalapeño | rate scales with the square |

The same idea works for any multiplier, not just doubling. If you **triple** a reactant ($\times 3$) and the rate goes up by $9 = 3^2$, the order is $2$. If you **halve** it ($\times \tfrac{1}{2}$) and the rate drops to a quarter ($\times \tfrac14 = (\tfrac12)^2$), again order $2$. The general relationship — the engine of every problem in this article — is:

$$\frac{\text{rate}_2}{\text{rate}_1} = \left(\frac{[\ce{A}]_2}{[\ce{A}]_1}\right)^{\!m}$$

This is the **ratio method**. Pick two experiments where only $\ce{A}$ changed, divide the rates, divide the concentrations, and solve for the exponent $m$.

### The units of *k* reveal the overall order

Here's a detail that scores easy AP points and catches lazy students: the **units of $k$ change depending on the overall order.** Rate always has units of $\text{M/s}$ (concentration per time). Concentration always has units of $\text{M}$. So we just solve for whatever units $k$ must carry to make the equation balance.

Rearrange the rate law to isolate $k$:

$$k = \frac{\text{rate}}{[\ce{A}]^m[\ce{B}]^n} \quad\Longrightarrow\quad [k] = \frac{\text{M}/\text{s}}{\text{M}^{(\text{overall order})}} = \text{M}^{\,1-(\text{overall order})}\cdot \text{s}^{-1}$$

Working it out for each overall order:

| Overall order | Units of $k$ | How to derive it |
|---|---|---|
| **0** | $\text{M}\cdot\text{s}^{-1}$ (i.e. $\text{M/s}$) | $\dfrac{\text{M/s}}{\text{M}^0} = \dfrac{\text{M/s}}{1}$ |
| **1** | $\text{s}^{-1}$ | $\dfrac{\text{M/s}}{\text{M}^1} = \dfrac{1}{\text{s}}$ |
| **2** | $\text{M}^{-1}\cdot\text{s}^{-1}$ | $\dfrac{\text{M/s}}{\text{M}^2} = \dfrac{1}{\text{M}\cdot\text{s}}$ |
| **3** | $\text{M}^{-2}\cdot\text{s}^{-1}$ | $\dfrac{\text{M/s}}{\text{M}^3} = \dfrac{1}{\text{M}^2\cdot\text{s}}$ |

The pattern: **each step up in overall order adds one more $\text{M}^{-1}$ to $k$.** This is a two-way street on the exam — if they hand you $k$ in $\text{M}^{-1}\text{s}^{-1}$, you can immediately announce "this is a second-order reaction overall" without any other information.

---

## Worked Examples

### Example 1: Reading a rate law

**Problem:** For a reaction, the experimentally determined rate law is $\text{rate} = k[\ce{NO}]^2[\ce{O2}]$. State the order in each reactant, the overall order, and predict what happens to the rate if you double $[\ce{NO}]$ while holding $[\ce{O2}]$ fixed.

**Solution:**
- Step 1 — Order in $\ce{NO}$: the exponent is $2$, so it's **second order** in $\ce{NO}$.
- Step 2 — Order in $\ce{O2}$: the exponent is $1$ (an unwritten exponent is always $1$), so it's **first order** in $\ce{O2}$.
- Step 3 — Overall order: $2 + 1 = 3$, **third order overall**.
- Step 4 — Double $[\ce{NO}]$: since $\ce{NO}$ is second order, rate is multiplied by $2^2 = 4$.

**Answer:** Second order in $\ce{NO}$, first order in $\ce{O2}$, third order overall; doubling $[\ce{NO}]$ makes the reaction **4× faster**.

### Example 2: Coefficients are NOT orders (the counterexample)

**Problem:** The balanced equation is $\ce{2NO2 + F2 -> 2NO2F}$. A student guesses the rate law is $\text{rate} = k[\ce{NO2}]^2[\ce{F2}]^1$ by copying the coefficients. Experiment, however, shows the rate law is $\text{rate} = k[\ce{NO2}][\ce{F2}]$. What went wrong, and what is the overall order?

**Solution:**
- Step 1 — Spot the error: the student read the exponents off the coefficients ($2$ and $1$). But orders are **experimental**, not structural.
- Step 2 — Trust the data: experiment says the exponent on $\ce{NO2}$ is $1$, not $2$. So the reaction is first order in $\ce{NO2}$, even though its coefficient is $2$.
- Step 3 — Overall order from the real law: $1 + 1 = 2$.

**Answer:** The coefficients ($2, 1$) do **not** match the true orders ($1, 1$). The real rate law is second order overall. *Coefficients tell you the stoichiometry; only experiment tells you the rate law.* (The deeper reason, coming in a later article: the rate law reflects the slow "bottleneck" step of the mechanism, which need not involve all the reactants at once.)

### Example 3: First order by inspection

**Problem:** For $\ce{A -> products}$, determine the order in $\ce{A}$.

| Experiment | $[\ce{A}]$ (M) | Initial rate (M/s) |
|---|---|---|
| 1 | 0.10 | $2.0 \times 10^{-3}$ |
| 2 | 0.20 | $4.0 \times 10^{-3}$ |

**Solution:**
- Step 1 — What changed? $[\ce{A}]$ doubled from $0.10$ to $0.20$ ($\times 2$).
- Step 2 — What did the rate do? It went from $2.0\times10^{-3}$ to $4.0\times10^{-3}$ ($\times 2$).
- Step 3 — Match the pattern: double the concentration $\to$ double the rate is $2^1$. Order $= 1$.

**Answer:** **First order** in $\ce{A}$. (Just like doubling Grandma's lime and getting twice the tang.)

### Example 4: Second order by inspection

**Problem:** For $\ce{A -> products}$, determine the order in $\ce{A}$.

| Experiment | $[\ce{A}]$ (M) | Initial rate (M/s) |
|---|---|---|
| 1 | 0.15 | $1.0 \times 10^{-2}$ |
| 2 | 0.30 | $4.0 \times 10^{-2}$ |

**Solution:**
- Step 1 — $[\ce{A}]$ doubled ($0.15 \to 0.30$).
- Step 2 — Rate went $\times 4$ ($1.0\times10^{-2} \to 4.0\times10^{-2}$).
- Step 3 — Double $\to$ quadruple is $2^2$. Order $= 2$.

**Answer:** **Second order** in $\ce{A}$. (The jalapeño: double it, get four times the kick.)

### Example 5: Zero order by inspection

**Problem:** For $\ce{A -> products}$, determine the order in $\ce{A}$.

| Experiment | $[\ce{A}]$ (M) | Initial rate (M/s) |
|---|---|---|
| 1 | 0.20 | $5.0 \times 10^{-4}$ |
| 2 | 0.60 | $5.0 \times 10^{-4}$ |

**Solution:**
- Step 1 — $[\ce{A}]$ tripled ($0.20 \to 0.60$).
- Step 2 — Rate didn't budge (still $5.0\times10^{-4}$).
- Step 3 — Any change in concentration produces $\times 1$ in the rate: $3^0 = 1$. Order $= 0$.

**Answer:** **Zero order** in $\ce{A}$. The rate ignores $[\ce{A}]$ completely — this is the maxed-out salt.

### Example 6: Two reactants — the full method of initial rates

**Problem:** For $\ce{A + B -> products}$, find the rate law.

| Experiment | $[\ce{A}]$ (M) | $[\ce{B}]$ (M) | Initial rate (M/s) |
|---|---|---|---|
| 1 | 0.10 | 0.10 | $2.0 \times 10^{-3}$ |
| 2 | 0.20 | 0.10 | $4.0 \times 10^{-3}$ |
| 3 | 0.10 | 0.20 | $8.0 \times 10^{-3}$ |

**Solution:**
- Step 1 — Order in $\ce{A}$: **compare experiments 1 and 2**, where $[\ce{B}]$ is held fixed at $0.10$ and only $[\ce{A}]$ changes.

$$\frac{\text{rate}_2}{\text{rate}_1} = \left(\frac{[\ce{A}]_2}{[\ce{A}]_1}\right)^{m} \;\Longrightarrow\; \frac{4.0\times10^{-3}}{2.0\times10^{-3}} = \left(\frac{0.20}{0.10}\right)^{m} \;\Longrightarrow\; 2 = 2^m \;\Longrightarrow\; m = 1$$

- Step 2 — Order in $\ce{B}$: **compare experiments 1 and 3**, where $[\ce{A}]$ is held fixed and only $[\ce{B}]$ changes.

$$\frac{\text{rate}_3}{\text{rate}_1} = \left(\frac{[\ce{B}]_3}{[\ce{B}]_1}\right)^{n} \;\Longrightarrow\; \frac{8.0\times10^{-3}}{2.0\times10^{-3}} = \left(\frac{0.20}{0.10}\right)^{n} \;\Longrightarrow\; 4 = 2^n \;\Longrightarrow\; n = 2$$

- Step 3 — Assemble the rate law: $\text{rate} = k[\ce{A}][\ce{B}]^2$, overall order $1 + 2 = 3$.

**Answer:** $\text{rate} = k[\ce{A}][\ce{B}]^2$; first order in $\ce{A}$, second order in $\ce{B}$, **third order overall**. Notice how each order came from the ONE pair of experiments where that reactant was the only thing changing — the controlled-batch trick.

### Example 7: Solving for *k* with correct units

**Problem:** Using the rate law $\text{rate} = k[\ce{A}][\ce{B}]^2$ from Example 6, solve for $k$ (with units) using the data from Experiment 1.

**Solution:**
- Step 1 — Rearrange: $k = \dfrac{\text{rate}}{[\ce{A}][\ce{B}]^2}$.
- Step 2 — Plug in Experiment 1 ($\text{rate}=2.0\times10^{-3}$, $[\ce{A}]=0.10$, $[\ce{B}]=0.10$):

$$k = \frac{2.0\times10^{-3}\ \text{M/s}}{(0.10\ \text{M})(0.10\ \text{M})^2} = \frac{2.0\times10^{-3}}{(0.10)(0.010)} = \frac{2.0\times10^{-3}}{1.0\times10^{-3}} = 2.0$$

- Step 3 — Units: overall order is $3$, so $k$ has units $\text{M}^{1-3}\text{s}^{-1} = \text{M}^{-2}\text{s}^{-1}$.

**Answer:** $k = 2.0\ \text{M}^{-2}\text{s}^{-1}$. (Always verify $k$ against a *second* row — plugging Experiment 2 or 3 in should give the same $2.0$. It does.)

### Example 8: Using the complete rate law to predict a rate

**Problem:** With $\text{rate} = k[\ce{A}][\ce{B}]^2$ and $k = 2.0\ \text{M}^{-2}\text{s}^{-1}$, predict the initial rate when $[\ce{A}] = 0.30\ \text{M}$ and $[\ce{B}] = 0.40\ \text{M}$.

**Solution:**
- Step 1 — Plug into the complete law:

$$\text{rate} = (2.0)(0.30)(0.40)^2 = (2.0)(0.30)(0.16)$$

- Step 2 — Multiply: $(2.0)(0.30) = 0.60$; then $0.60 \times 0.16 = 0.096$.

**Answer:** $\text{rate} = 0.096\ \text{M/s} = 9.6\times10^{-2}\ \text{M/s}$. Once you have the full rate law, it's a prediction machine for any concentrations you like.

### Example 9: A tricky pair of rows (concentrations change in unfriendly places)

**Problem:** For $\ce{A + B -> products}$, find both orders.

| Experiment | $[\ce{A}]$ (M) | $[\ce{B}]$ (M) | Initial rate (M/s) |
|---|---|---|---|
| 1 | 0.10 | 0.20 | $1.5 \times 10^{-3}$ |
| 2 | 0.20 | 0.20 | $3.0 \times 10^{-3}$ |
| 3 | 0.20 | 0.40 | $3.0 \times 10^{-3}$ |

**Solution:**
- Step 1 — Order in $\ce{A}$: compare 1 and 2 ($[\ce{B}]$ fixed at $0.20$). $[\ce{A}]$ doubles, rate doubles: $2 = 2^m \Rightarrow m = 1$.
- Step 2 — Order in $\ce{B}$: compare 2 and 3 ($[\ce{A}]$ fixed at $0.20$). $[\ce{B}]$ doubles ($0.20 \to 0.40$), but rate is **unchanged** ($3.0\times10^{-3}$ both times): $1 = 2^n \Rightarrow n = 0$.
- Step 3 — Assemble: $\text{rate} = k[\ce{A}][\ce{B}]^0 = k[\ce{A}]$.

**Answer:** $\text{rate} = k[\ce{A}]$; first order in $\ce{A}$, **zero order in $\ce{B}$**, first order overall. The lesson: you MUST pick the correct pair — for $\ce{B}$ you had to use rows 2 and 3 (not 1 and 3, where *both* concentrations changed and you'd learn nothing clean).

### Example 10: Non-integer ratio — tripling gives 9×

**Problem:** For $\ce{A -> products}$, determine the order in $\ce{A}$.

| Experiment | $[\ce{A}]$ (M) | Initial rate (M/s) |
|---|---|---|
| 1 | 0.050 | $1.0 \times 10^{-4}$ |
| 2 | 0.15 | $9.0 \times 10^{-4}$ |

**Solution:**
- Step 1 — Concentration ratio: $\dfrac{0.15}{0.050} = 3$ (tripled).
- Step 2 — Rate ratio: $\dfrac{9.0\times10^{-4}}{1.0\times10^{-4}} = 9$.
- Step 3 — Solve $9 = 3^m$. Since $3^2 = 9$, we get $m = 2$.

**Answer:** **Second order** in $\ce{A}$. Doubling isn't the only test — tripling and getting $9\times$ ($=3^2$) is the same second-order fingerprint.

### Example 11: When the ratio isn't clean — bring in logarithms

**Problem:** A reaction $\ce{A -> products}$ is studied (think of a light-driven reaction where you can't pick round concentrations). Determine the order.

| Experiment | $[\ce{A}]$ (M) | Initial rate (M/s) |
|---|---|---|
| 1 | 0.025 | $4.0 \times 10^{-5}$ |
| 2 | 0.040 | $1.024 \times 10^{-4}$ |

**Solution:**
- Step 1 — Concentration ratio: $\dfrac{0.040}{0.025} = 1.6$ (not a nice $2$ or $3$).
- Step 2 — Rate ratio: $\dfrac{1.024\times10^{-4}}{4.0\times10^{-5}} = 2.56$.
- Step 3 — Set up $2.56 = (1.6)^m$ and take logs of both sides (this is the [logarithm](/chemistry/0104-logarithms-for-chemistry) skill paying off):

$$\log(2.56) = m\,\log(1.6) \;\Longrightarrow\; m = \frac{\log(2.56)}{\log(1.6)} = \frac{0.4082}{0.2041} = 2.00$$

**Answer:** **Second order** in $\ce{A}$. When the ratio isn't a clean power, the universal move is $m = \dfrac{\log(\text{rate ratio})}{\log(\text{concentration ratio})}$.

### Example 12: A three-reactant table (full FRQ-style problem)

**Problem:** For $\ce{A + B + C -> products}$, find the complete rate law, the value of $k$ with units, and predict the rate when all three are $0.50\ \text{M}$.

| Experiment | $[\ce{A}]$ (M) | $[\ce{B}]$ (M) | $[\ce{C}]$ (M) | Initial rate (M/s) |
|---|---|---|---|---|
| 1 | 0.10 | 0.10 | 0.10 | $1.0 \times 10^{-3}$ |
| 2 | 0.20 | 0.10 | 0.10 | $2.0 \times 10^{-3}$ |
| 3 | 0.10 | 0.20 | 0.10 | $4.0 \times 10^{-3}$ |
| 4 | 0.10 | 0.10 | 0.20 | $1.0 \times 10^{-3}$ |

**Solution:**
- Step 1 — Order in $\ce{A}$ (exp 1 vs 2, only $\ce{A}$ changes): $\dfrac{2.0\times10^{-3}}{1.0\times10^{-3}} = 2 = 2^m \Rightarrow m = 1$.
- Step 2 — Order in $\ce{B}$ (exp 1 vs 3, only $\ce{B}$ changes): $\dfrac{4.0\times10^{-3}}{1.0\times10^{-3}} = 4 = 2^n \Rightarrow n = 2$.
- Step 3 — Order in $\ce{C}$ (exp 1 vs 4, only $\ce{C}$ changes): $\dfrac{1.0\times10^{-3}}{1.0\times10^{-3}} = 1 = 2^p \Rightarrow p = 0$.
- Step 4 — Rate law: $\text{rate} = k[\ce{A}][\ce{B}]^2[\ce{C}]^0 = k[\ce{A}][\ce{B}]^2$. Overall order $= 1 + 2 + 0 = 3$.
- Step 5 — Solve for $k$ using Experiment 1: $k = \dfrac{1.0\times10^{-3}}{(0.10)(0.10)^2} = \dfrac{1.0\times10^{-3}}{1.0\times10^{-3}} = 1.0\ \text{M}^{-2}\text{s}^{-1}$ (overall order 3 $\to$ $\text{M}^{-2}\text{s}^{-1}$).
- Step 6 — Predict at $[\ce{A}]=[\ce{B}]=[\ce{C}]=0.50$: $\text{rate} = (1.0)(0.50)(0.50)^2 = (1.0)(0.50)(0.25) = 0.125\ \text{M/s}$. ($\ce{C}$ is ignored — it's zero order.)

**Answer:** $\text{rate} = k[\ce{A}][\ce{B}]^2$, $k = 1.0\ \text{M}^{-2}\text{s}^{-1}$, predicted rate $= 0.125\ \text{M/s}$.

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Reading orders off the balanced-equation **coefficients** | The rate law *looks* like it should mirror the equation, and sometimes it coincidentally does | Orders are **always experimental**. Never write an order you didn't extract from data — this is the guaranteed FRQ trap |
| Comparing two experiments where **more than one** concentration changed | You grab the first two rows without checking | Deliberately pick the pair where every reactant EXCEPT the one you're studying is held constant — the controlled-batch rule |
| Forgetting the **units** on $k$ (or writing $\text{s}^{-1}$ for everything) | Students memorize "first order $= \text{s}^{-1}$" and stop | Derive units each time from overall order: $k$ has units $\text{M}^{1-\text{(overall order)}}\text{s}^{-1}$ |
| Treating a **zero-order** reactant as if doubling helps | Everything on the reactant side "should" matter, right? | Remember the maxed-out salt: $2^0 = 1$. Some reactants change nothing |
| Mixing up "doubles" with "$+2$" | Additive vs multiplicative thinking | Orders are about *multiplying*: rate $\times\,2^{\text{order}}$, never rate $+\,2$ |
| Not simplifying the rate ratio before matching a power | Big scientific-notation numbers look scary | Divide the rates FIRST to get a clean number ($2$, $4$, $9$, $1$), then match it to $2^m$ or use logs |
| Leaving $[\ce{X}]^0$ in the final rate law | It feels wrong to "drop" a reactant | $[\ce{X}]^0 = 1$, so write $\text{rate} = k[\ce{A}]$, not $k[\ce{A}][\ce{X}]^0$ |

---

## AP Exam Tips

- **"Orders are experimental, not the coefficients" is a guaranteed point.** If a free-response question hands you a balanced equation AND a data table, they are testing exactly this. Any student who copies the coefficients loses the point. Always extract orders from the table.
- **Show which two experiments you compared.** Graders want to see your reasoning: write "comparing Experiments 1 and 3, where only $[\ce{B}]$ changes." Naming the controlled pair earns method points even if arithmetic slips.
- **The ratio method is the whole game.** $\dfrac{\text{rate}_2}{\text{rate}_1} = \left(\dfrac{[\ce{X}]_2}{[\ce{X}]_1}\right)^{\text{order}}$. Memorize it cold; every initial-rates problem is one application per reactant.
- **$k$'s units are a free answer.** If asked for the overall order and you're only given $k$'s units, read it straight off: $\text{s}^{-1}\Rightarrow$ first order, $\text{M}^{-1}\text{s}^{-1}\Rightarrow$ second order, $\text{M}^{-2}\text{s}^{-1}\Rightarrow$ third order. And when you report $k$, **always attach units** — a bare number is often marked wrong.
- **Verify $k$ with a second row.** Solve for $k$ using one experiment, then plug a different experiment in to confirm you get the same value. This catches an order error before it costs you.
- **Initial-rates tables appear essentially every year** — in both the multiple-choice and the free-response sections. Getting fast and clean at them is one of the highest-return kinetics skills.
- **Use logs when the ratio isn't clean.** No graphing needed: $\text{order} = \dfrac{\log(\text{rate ratio})}{\log(\text{concentration ratio})}$. Bring it out only when inspection fails.

---

## Practice Problems

### Problem 1
The rate law for a reaction is $\text{rate} = k[\ce{A}]^2[\ce{B}]$. State the order in $\ce{A}$, the order in $\ce{B}$, and the overall order.

<details>
<summary><strong>Solution</strong></summary>

The exponent on $\ce{A}$ is $2$ (second order); on $\ce{B}$ it's $1$ (first order). Overall order $= 2 + 1 = 3$.

**Answer: second order in $\ce{A}$, first order in $\ce{B}$, third order overall.**

</details>

---

### Problem 2
For the rate law in Problem 1, what happens to the rate if you (a) double $[\ce{A}]$ alone, (b) triple $[\ce{B}]$ alone?

<details>
<summary><strong>Solution</strong></summary>

(a) $\ce{A}$ is second order: rate $\times\,2^2 = 4$. **Rate quadruples.**
(b) $\ce{B}$ is first order: rate $\times\,3^1 = 3$. **Rate triples.**

</details>

---

### Problem 3
Give the units of $k$ for a reaction that is (a) zero order overall, (b) first order overall, (c) second order overall.

<details>
<summary><strong>Solution</strong></summary>

Use $[k] = \text{M}^{1-\text{(overall order)}}\text{s}^{-1}$:
(a) zero order: $\text{M}^{1}\text{s}^{-1} = \text{M/s}$.
(b) first order: $\text{M}^{0}\text{s}^{-1} = \text{s}^{-1}$.
(c) second order: $\text{M}^{-1}\text{s}^{-1}$.

</details>

---

### Problem 4
A rate constant is reported as $k = 0.045\ \text{M}^{-1}\text{s}^{-1}$. What is the overall order of the reaction?

<details>
<summary><strong>Solution</strong></summary>

Solve $\text{M}^{1-x}\text{s}^{-1} = \text{M}^{-1}\text{s}^{-1}$, so $1 - x = -1 \Rightarrow x = 2$.

**Answer: second order overall.**

</details>

---

### Problem 5
For $\ce{A -> products}$: when $[\ce{A}] = 0.10\ \text{M}$ the rate is $3.0\times10^{-3}\ \text{M/s}$; when $[\ce{A}] = 0.30\ \text{M}$ the rate is $9.0\times10^{-3}\ \text{M/s}$. Find the order in $\ce{A}$.

<details>
<summary><strong>Solution</strong></summary>

Concentration ratio $= 0.30/0.10 = 3$. Rate ratio $= 9.0\times10^{-3} / 3.0\times10^{-3} = 3$. So $3 = 3^m \Rightarrow m = 1$.

**Answer: first order.**

</details>

---

### Problem 6
For $\ce{A -> products}$: at $[\ce{A}] = 0.20\ \text{M}$, rate $= 8.0\times10^{-4}\ \text{M/s}$; at $[\ce{A}] = 0.40\ \text{M}$, rate $= 3.2\times10^{-3}\ \text{M/s}$. Find the order.

<details>
<summary><strong>Solution</strong></summary>

Concentration ratio $= 0.40/0.20 = 2$. Rate ratio $= 3.2\times10^{-3}/8.0\times10^{-4} = 4$. So $4 = 2^m \Rightarrow m = 2$.

**Answer: second order.**

</details>

---

### Problem 7
For $\ce{A -> products}$: at $[\ce{A}] = 0.25\ \text{M}$, rate $= 6.0\times10^{-4}\ \text{M/s}$; at $[\ce{A}] = 0.75\ \text{M}$, rate $= 6.0\times10^{-4}\ \text{M/s}$. Find the order, and explain in one sentence what it means.

<details>
<summary><strong>Solution</strong></summary>

Concentration tripled but the rate didn't change: $1 = 3^m \Rightarrow m = 0$.

**Answer: zero order** — the rate does not depend on $[\ce{A}]$ at all (the maxed-out salt).

</details>

---

### Problem 8
For $\ce{A + B -> products}$, find the complete rate law.

| Experiment | $[\ce{A}]$ (M) | $[\ce{B}]$ (M) | Initial rate (M/s) |
|---|---|---|---|
| 1 | 0.10 | 0.10 | $4.0 \times 10^{-3}$ |
| 2 | 0.20 | 0.10 | $8.0 \times 10^{-3}$ |
| 3 | 0.20 | 0.30 | $7.2 \times 10^{-2}$ |

<details>
<summary><strong>Solution</strong></summary>

Order in $\ce{A}$ (exp 1 vs 2, $[\ce{B}]$ fixed): $8.0\times10^{-3}/4.0\times10^{-3} = 2 = 2^m \Rightarrow m = 1$.
Order in $\ce{B}$ (exp 2 vs 3, $[\ce{A}]$ fixed at $0.20$): concentration ratio $0.30/0.10 = 3$; rate ratio $7.2\times10^{-2}/8.0\times10^{-3} = 9$; so $9 = 3^n \Rightarrow n = 2$.

**Answer: $\text{rate} = k[\ce{A}][\ce{B}]^2$ (third order overall).**

</details>

---

### Problem 9
Using the data and rate law from Problem 8, calculate $k$ with units (use Experiment 1).

<details>
<summary><strong>Solution</strong></summary>

$$k = \frac{\text{rate}}{[\ce{A}][\ce{B}]^2} = \frac{4.0\times10^{-3}}{(0.10)(0.10)^2} = \frac{4.0\times10^{-3}}{1.0\times10^{-3}} = 4.0$$

Overall order 3 $\Rightarrow$ units $\text{M}^{-2}\text{s}^{-1}$.

**Answer: $k = 4.0\ \text{M}^{-2}\text{s}^{-1}$.**

</details>

---

### Problem 10
Using $\text{rate} = k[\ce{A}][\ce{B}]^2$ with $k = 4.0\ \text{M}^{-2}\text{s}^{-1}$, predict the initial rate when $[\ce{A}] = 0.50\ \text{M}$ and $[\ce{B}] = 0.20\ \text{M}$.

<details>
<summary><strong>Solution</strong></summary>

$$\text{rate} = (4.0)(0.50)(0.20)^2 = (4.0)(0.50)(0.040) = 0.080\ \text{M/s}$$

**Answer: $8.0\times10^{-2}\ \text{M/s}$.**

</details>

---

### Problem 11
The balanced equation is $\ce{2NO + 2H2 -> N2 + 2H2O}$, and experiment gives $\text{rate} = k[\ce{NO}]^2[\ce{H2}]$. A classmate insists the order in $\ce{H2}$ "must be 2 because of the coefficient." Correct them, and give the overall order.

<details>
<summary><strong>Solution</strong></summary>

Orders come from experiment, not coefficients. The measured exponent on $\ce{H2}$ is $1$, so it is **first order in $\ce{H2}$** despite the coefficient of $2$. Overall order $= 2 + 1 = 3$.

**Answer: first order in $\ce{H2}$; third order overall. Never use coefficients as orders.**

</details>

---

### Problem 12
For $\ce{A -> products}$: at $[\ce{A}] = 0.020\ \text{M}$, rate $= 5.0\times10^{-5}\ \text{M/s}$; at $[\ce{A}] = 0.050\ \text{M}$, rate $= 3.125\times10^{-4}\ \text{M/s}$. Use logarithms to find the order.

<details>
<summary><strong>Solution</strong></summary>

Concentration ratio $= 0.050/0.020 = 2.5$. Rate ratio $= 3.125\times10^{-4}/5.0\times10^{-5} = 6.25$.

$$m = \frac{\log(6.25)}{\log(2.5)} = \frac{0.7959}{0.3979} = 2.00$$

**Answer: second order.** (Check: $2.5^2 = 6.25$ ✓.)

</details>

---

### Problem 13
For $\ce{A + B + C -> products}$, find the complete rate law and $k$ (with units).

| Experiment | $[\ce{A}]$ (M) | $[\ce{B}]$ (M) | $[\ce{C}]$ (M) | Initial rate (M/s) |
|---|---|---|---|---|
| 1 | 0.10 | 0.10 | 0.10 | $2.0 \times 10^{-2}$ |
| 2 | 0.20 | 0.10 | 0.10 | $2.0 \times 10^{-2}$ |
| 3 | 0.10 | 0.20 | 0.10 | $4.0 \times 10^{-2}$ |
| 4 | 0.10 | 0.10 | 0.30 | $1.8 \times 10^{-1}$ |

<details>
<summary><strong>Solution</strong></summary>

Order in $\ce{A}$ (exp 1 vs 2): $2.0\times10^{-2}/2.0\times10^{-2} = 1 = 2^m \Rightarrow m = 0$ (zero order).
Order in $\ce{B}$ (exp 1 vs 3): $4.0\times10^{-2}/2.0\times10^{-2} = 2 = 2^n \Rightarrow n = 1$.
Order in $\ce{C}$ (exp 1 vs 4): concentration ratio $0.30/0.10 = 3$; rate ratio $1.8\times10^{-1}/2.0\times10^{-2} = 9 = 3^p \Rightarrow p = 2$.
Rate law: $\text{rate} = k[\ce{B}][\ce{C}]^2$, overall order $0 + 1 + 2 = 3$.
Solve $k$ (exp 1): $k = \dfrac{2.0\times10^{-2}}{(0.10)(0.10)^2} = \dfrac{2.0\times10^{-2}}{1.0\times10^{-3}} = 20\ \text{M}^{-2}\text{s}^{-1}$.

**Answer: $\text{rate} = k[\ce{B}][\ce{C}]^2$, $k = 20\ \text{M}^{-2}\text{s}^{-1}$ ($\ce{A}$ is zero order and drops out).**

</details>

---

### Problem 14
A reaction is first order in $\ce{A}$ and second order in $\ce{B}$. If you **triple** $[\ce{A}]$ and **halve** $[\ce{B}]$ at the same time, by what factor does the rate change?

<details>
<summary><strong>Solution</strong></summary>

$\ce{A}$: factor $3^1 = 3$. $\ce{B}$: factor $\left(\tfrac{1}{2}\right)^2 = \tfrac14$. Combined: $3 \times \tfrac14 = \tfrac34 = 0.75$.

**Answer: the rate becomes $0.75\times$ (drops to three-quarters) of the original.**

</details>

---

### Problem 15
A reaction has $\text{rate} = k[\ce{A}]^2$ with $k = 0.50\ \text{M}^{-1}\text{s}^{-1}$. (a) What is the overall order? (b) Confirm the units make sense. (c) Find the rate when $[\ce{A}] = 0.40\ \text{M}$.

<details>
<summary><strong>Solution</strong></summary>

(a) The exponent is $2$, so **second order overall**.
(b) Second order $\Rightarrow$ units should be $\text{M}^{-1}\text{s}^{-1}$, which matches ✓.
(c) $\text{rate} = (0.50)(0.40)^2 = (0.50)(0.16) = 0.080\ \text{M/s}$.

**Answer: (a) second order, (b) units consistent, (c) $8.0\times10^{-2}\ \text{M/s}$.**

</details>

---

## Quick Reference

| Concept | Formula / Rule |
|---|---|
| Rate law form | $\text{rate} = k[\ce{A}]^m[\ce{B}]^n$ |
| Orders $m, n$ | **experimental** — never from coefficients |
| Overall order | $m + n$ (sum of all individual orders) |
| Doubling test | double a reactant $\to$ rate $\times\,2^{\text{order}}$ |
| Zero order | double $\to \times 1$ (no change) |
| First order | double $\to \times 2$ |
| Second order | double $\to \times 4$; triple $\to \times 9$ |
| Ratio method | $\dfrac{\text{rate}_2}{\text{rate}_1} = \left(\dfrac{[\ce{X}]_2}{[\ce{X}]_1}\right)^{\text{order}}$ (only that reactant changes) |
| Order via logs | $\text{order} = \dfrac{\log(\text{rate ratio})}{\log(\text{concentration ratio})}$ |
| Solve for $k$ | $k = \dfrac{\text{rate}}{[\ce{A}]^m[\ce{B}]^n}$ (plug in any one row; verify with another) |
| Units of $k$ | $\text{M}^{1-\text{(overall order)}}\,\text{s}^{-1}$ |
| $k$ units cheat | $\text{M/s} \to$ 0th, $\text{s}^{-1} \to$ 1st, $\text{M}^{-1}\text{s}^{-1} \to$ 2nd, $\text{M}^{-2}\text{s}^{-1} \to$ 3rd |

---

<div align="center">

[← Reaction Rates](/chemistry/0701-reaction-rates) | [Integrated Rate Laws →](/chemistry/0703-integrated-rate-laws)

</div>
