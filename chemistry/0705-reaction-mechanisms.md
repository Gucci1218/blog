# Reaction Mechanisms
<p class="article-date">July 5, 2026</p>

*Last week I grabbed a \$5 sandwich at the Subway near school, and I finally paid attention to the assembly line instead of my phone. My sandwich slid down a row of workers: the first person laid out the bread, the next slapped on the turkey, the next piled on lettuce and tomatoes, and the last one wrapped it up. Here's the thing that stuck with me — the whole line moved only as fast as the SLOWEST worker. The bread person was lightning quick, but the veggie person was carefully arranging every single spinach leaf, and the entire line just... waited. It didn't matter how fast anyone else worked; that one slow station set the pace for my whole order. That is exactly how a chemical reaction actually happens: not in one magic leap from reactants to products, but as a sequence of tiny steps, and the slowest step controls the speed of everything. This is AP Unit 5 (Topics 5.4, 5.7, 5.8, and 5.10), and it's where kinetics finally tells you the true story of HOW a reaction happens, molecule by molecule.*

---

## What You'll Learn
- Explain what a **reaction mechanism** is: the actual step-by-step sequence of **elementary reactions** that add up to the overall reaction
- Classify an elementary step by its **molecularity** (unimolecular, bimolecular, or the rare termolecular)
- Write the rate law of an **elementary step directly from its coefficients** — the *only* time you can do that — and see why this contrasts sharply with overall reactions
- Add elementary steps to recover the **overall balanced equation**, and identify **intermediates** (made then consumed) and **catalysts** (consumed then regenerated)
- Identify the **rate-determining step (RDS)** — the slowest step — and derive the overall rate law when the **first step is slow**
- Handle the trickier case where a **fast equilibrium** precedes the slow step, and eliminate an **intermediate** from the rate law by substitution
- **Validate a proposed mechanism** by checking that it both sums to the overall equation *and* predicts the experimental rate law
- Read a **multistep reaction energy profile**: match each hump to a step, spot intermediates in the valleys, and find the RDS as the **tallest hump**

---

## Prerequisites
- [Rate Laws](/chemistry/0702-rate-laws) — you must be fluent that for an *overall* reaction the rate law comes from **experiment, not coefficients**; this article reveals the one exception (elementary steps) and why it exists
- [Collision Model and Arrhenius](/chemistry/0704-collision-model-arrhenius) — the energy profiles here are just several collision-model "hills" chained together, so you need activation energy and the reaction-coordinate diagram first

---

## The Core Concept

### Intuition First

Let's stay in the sandwich shop, because the whole topic lives in that assembly line.

When you look at the overall reaction — say, $\ce{A + B -> products}$ — you're only reading the **order ticket**: "one turkey footlong, done." But nobody makes a footlong in a single instant. Behind the counter, the sandwich moves through a line of workers, and *each worker does exactly one small job*. That hidden sequence of jobs is the **mechanism**, and each individual job is an **elementary step** — a single molecular event that happens exactly as written, with nothing hidden inside it.

Now map the pieces, because this mapping is the entire chapter:

| Sandwich shop | Chemistry | 
|---|---|
| One worker doing one job | one **elementary step** |
| The slowest worker | the **rate-determining step (RDS)** |
| The half-made sandwich passed between workers (bread + meat, not done) | a **reaction intermediate** |
| A worker who grabs a tool, uses it, and puts it back for the next order | a **catalyst** |
| The final order ticket ("turkey footlong") | the **overall balanced equation** |

Three ideas fall right out of this picture:

**1. The slowest worker sets the pace.** If the veggie station takes 40 seconds and every other station takes 2 seconds, the line produces one sandwich roughly every 40 seconds. Speeding up the bread person does *nothing*. In chemistry, the **slowest elementary step is the rate-determining step**, and it controls the overall rate. Want a faster reaction? You have to speed up the *bottleneck*, not the steps that were already fast.

**2. The half-made sandwich never shows up on the ticket or in the leftovers.** The bread-plus-meat handoff is *made* by worker 1 and *used up* by worker 2. It's real — it exists for a moment on the counter — but it isn't an ingredient you ordered and it isn't in the final wrapped sandwich. That's an **intermediate**: produced in one step, consumed in a later step, so it **cancels out** of the overall equation and never appears in it.

**3. A borrowed tool comes back.** Imagine one worker who grabs the cheese slicer, uses it, and sets it back down ready for the next sandwich. The slicer is *used* but not *used up* — it's there at the start and there again at the end. That's a **catalyst**: consumed in an early step and **regenerated** in a later one. Opposite bookkeeping from an intermediate.

Everything below is just making these three sentences precise. Let's go.

### Elementary Reactions and Molecularity (Topic 5.4)

An **elementary reaction** (elementary step) is a reaction that occurs in a **single molecular event** — one collision, or one molecule falling apart — exactly as the equation is written. There are no hidden sub-steps. A worker laying the bread does one thing; that's it.

Because an elementary step *is* the actual molecular event, we classify it by **molecularity** = the number of reactant particles that must come together in that step:

| Molecularity | Meaning | Elementary step | Rate law |
|---|---|---|---|
| **Unimolecular** | one particle rearranges or breaks apart | $\ce{A -> products}$ | $\text{rate} = k[\ce{A}]$ |
| **Bimolecular** | two particles collide | $\ce{A + B -> products}$ | $\text{rate} = k[\ce{A}][\ce{B}]$ |
| **Bimolecular** | two identical particles collide | $\ce{2A -> products}$ | $\text{rate} = k[\ce{A}]^2$ |
| **Termolecular** | three particles collide at once (**rare**) | $\ce{A + B + C -> products}$ | $\text{rate} = k[\ce{A}][\ce{B}][\ce{C}]$ |

Termolecular steps are rare because getting **three** particles to hit simultaneously — the same instant, correct orientation, enough energy — is wildly unlikely (imagine three sandwich workers' hands landing on the exact same spot at the exact same moment). Nature almost always finds a route through one- and two-particle steps instead.

> **THE ONE KEY RULE.** For an **elementary step only**, the rate law comes *directly* from the molecularity — you use the reactant coefficients as the exponents.

This is the single most important — and most abused — rule in the whole unit, so let me draw the contrast in bright red:

| | Overall reaction (from [Rate Laws](/chemistry/0702-rate-laws)) | Elementary step (this article) |
|---|---|---|
| Where does the rate law come from? | **experiment only** — you must measure it | **the coefficients** — read straight off the step |
| Can you use coefficients as exponents? | **NO, never** | **YES** — that's the whole point |

Why the difference? An elementary step *is* the real collision, so its coefficients literally count the particles that must meet — and rate depends on how often they meet, which depends on their concentrations. An *overall* equation, by contrast, is just the summary ticket; its coefficients tell you nothing about the hidden bottleneck, so you can't guess exponents from them. **Coefficients give the rate law only when the equation is an elementary step.** Tattoo that somewhere.

### Adding Steps: Intermediates and Catalysts

A mechanism is a list of elementary steps. **Add them up** (cancel anything identical on both sides) and you must recover the **overall balanced equation** — the order ticket. Along the way, two kinds of "temporary" species show up:

- An **intermediate** is **produced in an earlier step and consumed in a later step**. It appears on the *right* of one step and the *left* of a later one, so it **cancels** — it is NOT in the overall equation. (The half-made sandwich.)
- A **catalyst** is **consumed in an earlier step and regenerated in a later step**. It appears on the *left* of an early step and the *right* of a later one, so it **also cancels** — it too is absent from the overall equation, but it was there at the very start and returns at the very end. (The borrowed cheese slicer.)

The quick test: both cancel out, so look at the **order** they appear. Intermediate = *made first, used later* (up-then-down). Catalyst = *used first, made back later* (down-then-up, appears at the start).

### The Rate-Determining Step (Topics 5.7 & 5.8)

The **rate-determining step (RDS)** is the **slowest elementary step**. Just like the slowest worker caps the sandwich line, the RDS caps the reaction: the overall rate equals the rate of the RDS.

**Easy case — the first step is the slow one.** Then:

$$\text{overall rate} = \text{rate of the RDS} = k[\text{reactants of the slow step}]$$

and since it's an elementary step, you read that rate law straight off its coefficients. Clean. If the slow step is $\ce{2NO2 -> NO3 + NO}$, the overall rate is $k[\ce{NO2}]^2$, full stop — even if some *other* reactant (like $\ce{CO}$) appears in the overall equation, it isn't in the slow step, so it isn't in the rate law.

**Hard case — the slow step is NOT first.** Here a **fast step reaches equilibrium before the slow step**, and the slow step's rate law contains an **intermediate** — a species you can never put in a final rate law (you can't measure the concentration of a fleeting half-made sandwich). The fix, kept at AP level, is the **fast-equilibrium approximation**:

1. Write the rate law of the slow step from its coefficients (it will contain an intermediate).
2. Take the fast step *before* it and set its forward rate equal to its reverse rate (it's at equilibrium): $\;k_1[\text{reactants}] = k_{-1}[\text{intermediate}]$.
3. Solve that for the **intermediate's concentration** in terms of real reactants.
4. **Substitute** to eliminate the intermediate. What's left — real reactants only — is the predicted overall rate law.

(There's a fancier method called the steady-state approximation, but **you do not need it for AP**. Fast-equilibrium substitution is the AP tool.)

### Validating a Mechanism (Topic 5.7)

A proposed mechanism is a *hypothesis*. To be acceptable it must pass **two independent tests**:

> **Test 1 — Mass:** the steps must **add up to the overall balanced equation**.
> **Test 2 — Rate:** the mechanism must **predict a rate law that matches the experimental one**.

Fail either test and the mechanism is wrong. Pass both and the mechanism is *consistent* (still not "proven" — another mechanism might also fit — but it's a valid candidate). This is the classic "Is this mechanism consistent with the data?" AP question.

### Multistep Reaction Energy Profiles (Topic 5.10)

Back in [Collision Model and Arrhenius](/chemistry/0704-collision-model-arrhenius), a one-step reaction had a single hill — one activation-energy "hump" with the transition state at the top. A **multistep** reaction has **one hump per elementary step**, chained together, with a **valley between each pair of humps**.

Reading the diagram:

- **Each hump = one elementary step.** The top of a hump is that step's **transition state**; the height from the starting valley up to the peak is that step's **activation energy $E_a$**.
- **Each valley (dip) between humps = an intermediate.** It's a real, momentarily-stable species (the half-made sandwich resting on the counter) — lower in energy than the transition states on either side, but not the final product.
- **The tallest hump = the rate-determining step.** The highest transition state is the biggest energy barrier, the hardest jump to make, so it's the slowest step — the bottleneck.

Here's a two-step profile in ASCII (step 1 is slow, step 2 is fast — the first hump is taller):

```
Energy
  ^                TS1  (tallest peak = RDS)
  |               .-''-.
  |              /      \
  |             /        \          TS2
  |            /          \       .-''-.
  |  reactants/            \     /      \
  |  '-------'              \   /        \
  |                          '-'          '------ products
  |                       intermediate
  |                        (valley)
  +--------------------------------------------------> reaction progress
```

Two humps, one valley. TS1 is higher than TS2, so **step 1 is rate-determining**. The dip labeled *intermediate* is the species made by step 1 and eaten by step 2. If instead the **second** hump were the taller one, step 2 would be the RDS — you find the bottleneck by eye, just by asking "which peak is highest?"

One more read-off: the overall reaction is exothermic here because the products sit *lower* than the reactants (energy released), exactly as in the single-step profiles from Unit 5's energy diagrams. Multistep profiles carry all the same information — they just have more than one hill.

---

## Worked Examples

### Example 1: Molecularity and Rate Law of a Single Elementary Step

**Problem:** The elementary step $\ce{O3 -> O2 + O}$ is one stage of ozone breakdown. State its molecularity and write its rate law.

**Solution:**

**Step 1:** Count reactant particles: exactly one, $\ce{O3}$. One particle → **unimolecular**.

**Step 2:** Because it's an elementary step, read the rate law off the coefficient: rate $= k[\ce{O3}]^1$.

**Answer:** Unimolecular; $\text{rate} = k[\ce{O3}]$.

### Example 2: A Bimolecular Step

**Problem:** For the elementary step $\ce{NO + O3 -> NO2 + O2}$, give the molecularity and rate law.

**Solution:**

**Step 1:** Two reactant particles collide ($\ce{NO}$ and $\ce{O3}$) → **bimolecular**.

**Step 2:** Elementary, so use the coefficients (both 1): rate $= k[\ce{NO}][\ce{O3}]$.

**Answer:** Bimolecular; $\text{rate} = k[\ce{NO}][\ce{O3}]$.

### Example 3: The Coefficient Trap — Elementary vs. Overall

**Problem:** The **overall** reaction $\ce{2NO2 + F2 -> 2NO2F}$ is *not* an elementary step. A student writes rate $= k[\ce{NO2}]^2[\ce{F2}]$ straight from the coefficients. What's wrong?

**Solution:**

**Step 1:** This is an *overall* equation, not an elementary step. The one key rule ("coefficients give the rate law") applies **only to elementary steps**.

**Step 2:** For an overall reaction, the rate law must come from **experiment** (see [Rate Laws](/chemistry/0702-rate-laws)). You cannot read exponents off overall coefficients.

**Answer:** The student illegally used overall coefficients as exponents. The true rate law (experimentally, rate $= k[\ce{NO2}][\ce{F2}]$) can only be found by measurement, not by copying coefficients.

### Example 4: Identifying an Intermediate and a Catalyst

**Problem:** A proposed mechanism:

$$\text{Step 1: } \ce{NO2 + NO2 -> NO3 + NO}$$
$$\text{Step 2: } \ce{NO3 + CO -> NO2 + CO2}$$

Find the overall equation, the intermediate, and any catalyst.

**Solution:**

**Step 1 — add the steps:**

$$\ce{NO2 + NO2 + NO3 + CO -> NO3 + NO + NO2 + CO2}$$

**Step 2 — cancel species on both sides.** $\ce{NO3}$ appears on both sides → cancel. One $\ce{NO2}$ appears on both sides → cancel one from each side.

$$\ce{NO2 + CO -> NO + CO2}$$

**Step 3 — classify.** $\ce{NO3}$ was **produced** in step 1 and **consumed** in step 2 (up-then-down) → **intermediate**. Nothing was consumed-first-then-regenerated, so there's no catalyst here.

**Answer:** Overall: $\ce{NO2 + CO -> NO + CO2}$. Intermediate: $\ce{NO3}$. No catalyst.

### Example 5: Spotting a Catalyst

**Problem:** In the ozone-depletion mechanism

$$\text{Step 1: } \ce{Cl + O3 -> ClO + O2}$$
$$\text{Step 2: } \ce{ClO + O -> Cl + O2}$$

identify the overall reaction, the intermediate, and the catalyst.

**Solution:**

**Step 1 — add and cancel.** $\ce{ClO}$ cancels (right of step 1, left of step 2). $\ce{Cl}$ cancels (left of step 1, right of step 2).

$$\ce{O3 + O -> 2O2}$$

**Step 2 — classify.** $\ce{ClO}$ is produced then consumed (up-then-down) → **intermediate**. $\ce{Cl}$ is *consumed* first (step 1) then *regenerated* (step 2) and is present at the very start → **catalyst**.

**Answer:** Overall $\ce{O3 + O -> 2O2}$; intermediate $\ce{ClO}$; catalyst $\ce{Cl}$. (This is exactly why one chlorine atom can destroy thousands of ozone molecules — it keeps coming back, like a cheese slicer reused all shift.)

### Example 6: Rate Law When the FIRST Step Is Slow

**Problem:** For $\ce{NO2 + CO -> NO + CO2}$, the mechanism is

$$\text{Step 1 (slow): } \ce{NO2 + NO2 -> NO3 + NO}$$
$$\text{Step 2 (fast): } \ce{NO3 + CO -> NO2 + CO2}$$

Derive the overall rate law.

**Solution:**

**Step 1:** The RDS is the slow step, and it's **first**, so overall rate = rate of step 1.

**Step 2:** Step 1 is elementary — read its rate law off the coefficients: two $\ce{NO2}$ collide, so rate $= k[\ce{NO2}]^2$.

**Step 3:** No intermediate appears (both reactants are real), so we're done.

**Answer:** $\text{rate} = k[\ce{NO2}]^2$. Notice $\ce{CO}$ is **absent** — it only shows up in the fast step *after* the bottleneck, so it can't affect the rate, exactly like the fast bread station not affecting the slow veggie station.

### Example 7: Another RDS-First Derivation

**Problem:** The mechanism for $\ce{2H2O2 -> 2H2O + O2}$ (iodide-catalyzed) is

$$\text{Step 1 (slow): } \ce{H2O2 + I- -> H2O + IO-}$$
$$\text{Step 2 (fast): } \ce{H2O2 + IO- -> H2O + O2 + I-}$$

Give the overall rate law and identify the catalyst.

**Solution:**

**Step 1:** Slow step is first → overall rate = rate of step 1 (elementary): rate $= k[\ce{H2O2}][\ce{I-}]$.

**Step 2:** Classify $\ce{I-}$: consumed in step 1, regenerated in step 2, present at the start → **catalyst**. ($\ce{IO-}$ is the intermediate.)

**Answer:** $\text{rate} = k[\ce{H2O2}][\ce{I-}]$; catalyst $\ce{I-}$. (A catalyst can legitimately appear in the rate law even though it cancels from the overall equation — it speeds the reaction and its concentration matters.)

### Example 8: Fast Equilibrium Before the Slow Step ($\ce{2NO + O2}$)

**Problem:** For $\ce{2NO + O2 -> 2NO2}$, the proposed mechanism is

$$\text{Step 1 (fast, equilibrium): } \ce{2NO <=> N2O2}$$
$$\text{Step 2 (slow): } \ce{N2O2 + O2 -> 2NO2}$$

Derive the overall rate law.

**Solution:**

**Step 1 — rate law of the slow step (RDS), from its coefficients:**

$$\text{rate} = k_2[\ce{N2O2}][\ce{O2}]$$

But $\ce{N2O2}$ is an **intermediate** — it can't stay in the answer.

**Step 2 — use the fast equilibrium (step 1).** Forward rate = reverse rate:

$$k_1[\ce{NO}]^2 = k_{-1}[\ce{N2O2}]$$

**Step 3 — solve for the intermediate:**

$$[\ce{N2O2}] = \frac{k_1}{k_{-1}}[\ce{NO}]^2$$

**Step 4 — substitute back:**

$$\text{rate} = k_2 \cdot \frac{k_1}{k_{-1}}[\ce{NO}]^2 [\ce{O2}] = k[\ce{NO}]^2[\ce{O2}]$$

where $k = \dfrac{k_2 k_1}{k_{-1}}$.

**Answer:** $\text{rate} = k[\ce{NO}]^2[\ce{O2}]$ — second order in $\ce{NO}$, first order in $\ce{O2}$, third order overall. The intermediate is gone.

### Example 9: Fast Equilibrium ($\ce{2NO + Br2}$)

**Problem:** For $\ce{2NO + Br2 -> 2NOBr}$:

$$\text{Step 1 (fast, equilibrium): } \ce{NO + Br2 <=> NOBr2}$$
$$\text{Step 2 (slow): } \ce{NOBr2 + NO -> 2NOBr}$$

Find the overall rate law.

**Solution:**

**Step 1 — RDS rate law from coefficients:** $\text{rate} = k_2[\ce{NOBr2}][\ce{NO}]$. The intermediate $\ce{NOBr2}$ must go.

**Step 2 — equilibrium on step 1:** $k_1[\ce{NO}][\ce{Br2}] = k_{-1}[\ce{NOBr2}]$.

**Step 3 — solve:** $[\ce{NOBr2}] = \dfrac{k_1}{k_{-1}}[\ce{NO}][\ce{Br2}]$.

**Step 4 — substitute:**

$$\text{rate} = k_2 \cdot \frac{k_1}{k_{-1}}[\ce{NO}][\ce{Br2}] \cdot [\ce{NO}] = k[\ce{NO}]^2[\ce{Br2}]$$

**Answer:** $\text{rate} = k[\ce{NO}]^2[\ce{Br2}]$ — third order overall.

### Example 10: Fast Equilibrium With a Product in the Denominator (Ozone)

**Problem:** For $\ce{2O3 -> 3O2}$:

$$\text{Step 1 (fast, equilibrium): } \ce{O3 <=> O2 + O}$$
$$\text{Step 2 (slow): } \ce{O + O3 -> 2O2}$$

Derive the rate law.

**Solution:**

**Step 1 — RDS rate law:** $\text{rate} = k_2[\ce{O}][\ce{O3}]$; the intermediate is the oxygen atom $\ce{O}$.

**Step 2 — equilibrium on step 1** (note $\ce{O2}$ is on the reverse side):

$$k_1[\ce{O3}] = k_{-1}[\ce{O2}][\ce{O}]$$

**Step 3 — solve for $\ce{O}$:**

$$[\ce{O}] = \frac{k_1[\ce{O3}]}{k_{-1}[\ce{O2}]}$$

**Step 4 — substitute:**

$$\text{rate} = k_2 \cdot \frac{k_1[\ce{O3}]}{k_{-1}[\ce{O2}]}\cdot[\ce{O3}] = k\,\frac{[\ce{O3}]^2}{[\ce{O2}]}$$

**Answer:** $\text{rate} = k\dfrac{[\ce{O3}]^2}{[\ce{O2}]} = k[\ce{O3}]^2[\ce{O2}]^{-1}$. The product $\ce{O2}$ appears with a **negative order** — adding more $\ce{O2}$ *slows* the reaction, because it pushes the fast equilibrium backward and starves the slow step of its intermediate.

### Example 11: Is This Mechanism Consistent?

**Problem:** For $\ce{NO2 + CO -> NO + CO2}$, experiments give rate $= k[\ce{NO2}]^2$. A student proposes a **single elementary step**: $\ce{NO2 + CO -> NO + CO2}$. Is this mechanism consistent with the data?

**Solution:**

**Test 1 (mass):** A single step obviously sums to the overall equation. ✔

**Test 2 (rate):** If it were elementary, its rate law (from coefficients) would be rate $= k[\ce{NO2}][\ce{CO}]$. But experiment says rate $= k[\ce{NO2}]^2$ — no $\ce{CO}$, and *second* order in $\ce{NO2}$. These don't match. �’

**Answer:** **Not consistent.** It passes the mass test but fails the rate test, so the one-step mechanism is rejected. (The two-step mechanism in Example 6 passes both — that's the accepted one.)

### Example 12: Reading a Multistep Energy Profile

**Problem:** A reaction has this profile (energies of the transition states, in kJ):

```
Energy
  ^          TS1 = 60
  |          .-''-.               TS2 = 90
  |         /      \            .-''''-.
  |  react /        \          /        \
  | (20)--'          \        /          \
  |                   '------'            '---- products (10)
  |                  intermediate (35)
  +------------------------------------------------> progress
```

(a) How many elementary steps? (b) Which is rate-determining? (c) Is the overall reaction exo- or endothermic?

**Solution:**

**(a)** Two humps → **two elementary steps**.

**(b)** The RDS is the step with the **tallest transition state**. TS2 (90 kJ) is higher than TS1 (60 kJ), so **step 2 is rate-determining**. (Measured as a barrier, step 2's $E_a$ is $90 - 35 = 55$ kJ from the intermediate valley, versus step 1's $60 - 20 = 40$ kJ — step 2 has the bigger climb.)

**(c)** Products (10 kJ) sit **lower** than reactants (20 kJ), so energy is released → **exothermic**.

**Answer:** (a) two steps; (b) step 2 (tallest hump, TS2 = 90 kJ) is the RDS; (c) exothermic.

### Example 13: Full "Consistent Mechanism" Check With Fast Equilibrium

**Problem:** For $\ce{2NO + O2 -> 2NO2}$, experiment gives rate $= k[\ce{NO}]^2[\ce{O2}]$. Does the two-step mechanism of Example 8 (fast $\ce{2NO <=> N2O2}$, then slow $\ce{N2O2 + O2 -> 2NO2}$) fit?

**Solution:**

**Test 1 (mass):** Add the steps: $\ce{2NO + N2O2 + O2 -> N2O2 + 2NO2}$; $\ce{N2O2}$ cancels → $\ce{2NO + O2 -> 2NO2}$. Matches the overall equation. ✔

**Test 2 (rate):** From Example 8, this mechanism predicts rate $= k[\ce{NO}]^2[\ce{O2}]$, which matches experiment exactly. ✔

**Answer:** **Consistent** — passes both tests, so it's an acceptable mechanism.

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Using coefficients as exponents for an **overall** reaction | The elementary-step rule leaks over | Coefficients → rate law **only for elementary steps**. Overall rate laws come from **experiment** |
| Leaving an **intermediate** in the final rate law | You wrote the RDS rate law and stopped | If an intermediate appears, you MUST eliminate it using the fast equilibrium before it |
| Confusing **intermediate** and **catalyst** | Both cancel from the overall equation | Intermediate = made-then-used (appears on a *right* side first). Catalyst = used-then-remade (appears on a *left* side first, present at the start) |
| Thinking a **fast** step controls the rate | "Fast" sounds important | The **slowest** step is the bottleneck. Speeding up fast steps changes nothing, like rushing the bread station |
| Putting a reactant in the rate law just because it's in the overall equation | It "should" matter | If a reactant only enters *after* the RDS, it's **not** in the rate law (e.g., $\ce{CO}$ in Example 6) |
| Picking the RDS as the tallest **hump measured from zero** instead of the highest **transition-state energy** | Misreading the diagram | The RDS is the step with the **highest transition state (peak)** — the hardest absolute point to reach |
| Accepting a mechanism because it just sums correctly | Forgetting test 2 | A valid mechanism must **both** sum to the overall equation **and** match the experimental rate law |
| Calling a valid mechanism "proven" | It fit the data | A consistent mechanism is only a **candidate** — other mechanisms might also fit |

---

## AP Exam Tips

- **The single most tested idea: coefficients give the rate law ONLY for elementary steps.** If a step is labeled "elementary" (or is a step in a mechanism), read the exponents off its coefficients. If it's an *overall* reaction, you need experimental data — never copy coefficients.
- **Intermediate vs. catalyst is a guaranteed identification question.** Intermediate = produced then consumed (shows up on a product side first). Catalyst = consumed then regenerated (present at the start, comes back at the end). Both cancel from the overall equation — use the *order* to tell them apart.
- **"Slowest = rate-determining = tallest hump."** Memorize this three-way link. On an energy diagram, the RDS is the step with the **highest transition state**; on a mechanism, it's the step labeled "slow."
- **Deriving the rate law from a mechanism:** if the **first step is slow**, rate = rate of that step (coefficients), and any reactant appearing only later is absent from the rate law. If a **fast equilibrium precedes the slow step**, write the slow step's rate law, then set forward = reverse for the fast step and **substitute to eliminate the intermediate**. Steady-state is NOT required on the AP exam.
- **A rate law must contain only reactants (and sometimes catalysts) — never an intermediate.** If your derived rate law has an intermediate in it, you're not finished.
- **"Is this mechanism consistent?" needs BOTH checks:** (1) the steps add to the overall balanced equation, and (2) the predicted rate law matches the experimental one. State both explicitly for full credit.
- **A catalyst can appear in the rate law** even though it's not in the overall equation — don't reflexively delete it. Adding catalyst genuinely speeds the reaction.

---

## Practice Problems

### Problem 1
State the molecularity and rate law of the elementary step $\ce{N2O4 -> 2NO2}$.

<details>
<summary><strong>Solution</strong></summary>

One reactant particle → **unimolecular**. Elementary, so read the coefficient: rate $= k[\ce{N2O4}]$.

**Answer:** Unimolecular; $\text{rate} = k[\ce{N2O4}]$.

</details>

### Problem 2
State the molecularity and rate law of the elementary step $\ce{2NO2 -> NO3 + NO}$.

<details>
<summary><strong>Solution</strong></summary>

Two identical particles collide → **bimolecular**. Rate law from coefficients: rate $= k[\ce{NO2}]^2$.

**Answer:** Bimolecular; $\text{rate} = k[\ce{NO2}]^2$.

</details>

### Problem 3
The overall reaction $\ce{H2 + Br2 -> 2HBr}$ has the experimental rate law rate $= k[\ce{H2}][\ce{Br2}]^{1/2}$. A classmate says "the coefficients are 1 and 1, so rate $= k[\ce{H2}][\ce{Br2}]$." What's the flaw?

<details>
<summary><strong>Solution</strong></summary>

This is an **overall** reaction, not an elementary step, so coefficients can't be used as exponents. The real rate law (note the $\tfrac{1}{2}$ order — impossible to get from a single elementary step) proves the reaction is multistep and must be found by experiment.

**Answer:** They illegally used overall coefficients as exponents; overall rate laws come from experiment. The half-order confirms a multistep mechanism.

</details>

### Problem 4
For the mechanism
$$\text{Step 1: } \ce{H2O2 + Br- -> H2O + BrO-}$$
$$\text{Step 2: } \ce{H2O2 + BrO- -> H2O + O2 + Br-}$$
give the overall equation, the intermediate, and the catalyst.

<details>
<summary><strong>Solution</strong></summary>

Add and cancel: $\ce{BrO-}$ cancels (made in 1, used in 2); $\ce{Br-}$ cancels (used in 1, remade in 2).

$$\ce{2H2O2 -> 2H2O + O2}$$

$\ce{BrO-}$ = made-then-used → **intermediate**. $\ce{Br-}$ = used-then-remade, present at start → **catalyst**.

**Answer:** Overall $\ce{2H2O2 -> 2H2O + O2}$; intermediate $\ce{BrO-}$; catalyst $\ce{Br-}$.

</details>

### Problem 5
In the mechanism
$$\text{Step 1: } \ce{NO + NO -> N2O2}$$
$$\text{Step 2: } \ce{N2O2 + H2 -> N2O + H2O}$$
$$\text{Step 3: } \ce{N2O + H2 -> N2 + H2O}$$
identify all intermediates and the overall equation.

<details>
<summary><strong>Solution</strong></summary>

Add all three. $\ce{N2O2}$ cancels (made in 1, used in 2). $\ce{N2O}$ cancels (made in 2, used in 3).

$$\ce{2NO + 2H2 -> N2 + 2H2O}$$

**Answer:** Intermediates $\ce{N2O2}$ and $\ce{N2O}$; overall $\ce{2NO + 2H2 -> N2 + 2H2O}$. No catalyst.

</details>

### Problem 6
For a reaction with mechanism
$$\text{Step 1 (slow): } \ce{Cl2 -> 2Cl}$$
$$\text{Step 2 (fast): } \ce{2Cl + 2CO -> 2COCl}$$
write the overall rate law.

<details>
<summary><strong>Solution</strong></summary>

The slow step is **first**, so overall rate = rate of step 1 (elementary, unimolecular): rate $= k[\ce{Cl2}]$. $\ce{CO}$ enters only after the bottleneck, so it's absent.

**Answer:** $\text{rate} = k[\ce{Cl2}]$.

</details>

### Problem 7
The reaction $\ce{2NO2 + F2 -> 2NO2F}$ has mechanism
$$\text{Step 1 (slow): } \ce{NO2 + F2 -> NO2F + F}$$
$$\text{Step 2 (fast): } \ce{NO2 + F -> NO2F}$$
Give the rate law and name the intermediate.

<details>
<summary><strong>Solution</strong></summary>

Slow step first → rate = rate of step 1 (elementary, bimolecular): rate $= k[\ce{NO2}][\ce{F2}]$. The $\ce{F}$ atom is made in step 1, consumed in step 2 → **intermediate**.

**Answer:** $\text{rate} = k[\ce{NO2}][\ce{F2}]$; intermediate $\ce{F}$.

</details>

### Problem 8
For $\ce{2NO + Cl2 -> 2NOCl}$ with mechanism
$$\text{Step 1 (fast eq): } \ce{NO + Cl2 <=> NOCl2}$$
$$\text{Step 2 (slow): } \ce{NOCl2 + NO -> 2NOCl}$$
derive the overall rate law.

<details>
<summary><strong>Solution</strong></summary>

RDS rate law: rate $= k_2[\ce{NOCl2}][\ce{NO}]$; intermediate $\ce{NOCl2}$.

Fast equilibrium: $k_1[\ce{NO}][\ce{Cl2}] = k_{-1}[\ce{NOCl2}]$, so $[\ce{NOCl2}] = \frac{k_1}{k_{-1}}[\ce{NO}][\ce{Cl2}]$.

Substitute: rate $= k_2\frac{k_1}{k_{-1}}[\ce{NO}][\ce{Cl2}][\ce{NO}] = k[\ce{NO}]^2[\ce{Cl2}]$.

**Answer:** $\text{rate} = k[\ce{NO}]^2[\ce{Cl2}]$ (third order overall).

</details>

### Problem 9
For $\ce{H2 + 2ICl -> I2 + 2HCl}$ with mechanism
$$\text{Step 1 (slow): } \ce{H2 + ICl -> HI + HCl}$$
$$\text{Step 2 (fast): } \ce{HI + ICl -> I2 + HCl}$$
give the rate law, the intermediate, and the overall equation.

<details>
<summary><strong>Solution</strong></summary>

Slow step first → rate $= k[\ce{H2}][\ce{ICl}]$ (elementary, bimolecular). $\ce{HI}$ is made then used → **intermediate**. Adding steps ($\ce{HI}$ cancels): $\ce{H2 + 2ICl -> I2 + 2HCl}$.

**Answer:** $\text{rate} = k[\ce{H2}][\ce{ICl}]$; intermediate $\ce{HI}$; overall as given.

</details>

### Problem 10
The reaction $\ce{2NO2 + F2 -> 2NO2F}$ was tested and found to be rate $= k[\ce{NO2}][\ce{F2}]$. Is the **single-step elementary** mechanism $\ce{2NO2 + F2 -> 2NO2F}$ consistent with this?

<details>
<summary><strong>Solution</strong></summary>

Mass test: a single step sums to the overall equation. ✔ Rate test: as an elementary step it would predict rate $= k[\ce{NO2}]^2[\ce{F2}]$ (termolecular), but experiment gives rate $= k[\ce{NO2}][\ce{F2}]$. Mismatch. ✗

**Answer:** **Not consistent** — fails the rate test (and a termolecular step would be very unlikely anyway). The two-step mechanism in Problem 7 fits instead.

</details>

### Problem 11
A two-step energy profile has transition states TS1 = 75 kJ and TS2 = 45 kJ, reactants at 30 kJ, an intermediate valley at 40 kJ, and products at 15 kJ. (a) Which step is rate-determining? (b) Is the reaction exo- or endothermic?

<details>
<summary><strong>Solution</strong></summary>

(a) Highest transition state = RDS. TS1 (75) > TS2 (45), so **step 1** is rate-determining. (b) Products (15) below reactants (30) → energy released → **exothermic**.

**Answer:** (a) step 1; (b) exothermic.

</details>

### Problem 12
Sketch-in-words: describe the energy profile of a **two-step** reaction whose **second** step is rate-determining and which is overall **endothermic**.

<details>
<summary><strong>Solution</strong></summary>

Two humps with one valley between them. For step 2 to be rate-determining, the **second hump's transition state must be the tallest** (higher than the first). For the reaction to be endothermic, the **products end up higher than the reactants** (energy absorbed). So: reactants low, a first (shorter) hump, dip down to the intermediate valley, then a second (taller) hump, ending at products that sit *above* the starting reactants.

**Answer:** First hump shorter, second hump tallest (= RDS), products higher than reactants (endothermic).

</details>

### Problem 13
For $\ce{2O3 -> 3O2}$ with the mechanism $\ce{O3 <=> O2 + O}$ (fast eq) then $\ce{O + O3 -> 2O2}$ (slow), a student writes the final rate law as rate $= k[\ce{O}][\ce{O3}]$. Why is this unacceptable, and what is the correct rate law?

<details>
<summary><strong>Solution</strong></summary>

$\ce{O}$ is an **intermediate**, and a rate law may never contain an intermediate. Use the fast equilibrium: $k_1[\ce{O3}] = k_{-1}[\ce{O2}][\ce{O}]$, so $[\ce{O}] = \frac{k_1[\ce{O3}]}{k_{-1}[\ce{O2}]}$. Substitute: rate $= k_2\frac{k_1[\ce{O3}]}{k_{-1}[\ce{O2}]}[\ce{O3}] = k\frac{[\ce{O3}]^2}{[\ce{O2}]}$.

**Answer:** The rate law can't contain the intermediate $\ce{O}$. Correct: $\text{rate} = k\dfrac{[\ce{O3}]^2}{[\ce{O2}]}$.

</details>

### Problem 14
The reaction $\ce{NO2 + CO -> NO + CO2}$ has experimental rate law rate $= k[\ce{NO2}]^2$. Which of these mechanisms is consistent? (A) single step $\ce{NO2 + CO -> NO + CO2}$; (B) slow $\ce{NO2 + NO2 -> NO3 + NO}$, fast $\ce{NO3 + CO -> NO2 + CO2}$.

<details>
<summary><strong>Solution</strong></summary>

**A:** elementary → predicts rate $= k[\ce{NO2}][\ce{CO}]$. Doesn't match (data has no $\ce{CO}$ and is 2nd order in $\ce{NO2}$). ✗

**B:** mass — steps add to $\ce{NO2 + CO -> NO + CO2}$ ✔; rate — slow step is first, elementary, so rate $= k[\ce{NO2}]^2$, matching experiment ✔.

**Answer:** **Mechanism B** is consistent (passes both tests); A is not.

</details>

### Problem 15
In the mechanism of Problem 14 (B), classify $\ce{NO3}$ and explain why $\ce{CO}$ is absent from the rate law even though it's a reactant in the overall equation.

<details>
<summary><strong>Solution</strong></summary>

$\ce{NO3}$ is produced in step 1 and consumed in step 2 → **intermediate**. $\ce{CO}$ reacts only in the **fast** second step, *after* the rate-determining first step — so it can't influence the overall speed, exactly like the fast bread station not affecting the slow veggie station.

**Answer:** $\ce{NO3}$ is an intermediate; $\ce{CO}$ enters only after the RDS, so it doesn't appear in the rate law.

</details>

---

## Quick Reference

**Mechanism** = the real step-by-step sequence of **elementary reactions** that sums to the overall equation.

**Molecularity of an elementary step → its rate law (the ONE time coefficients work):**

| Elementary step | Molecularity | Rate law |
|---|---|---|
| $\ce{A -> products}$ | unimolecular | $k[\ce{A}]$ |
| $\ce{A + B -> products}$ | bimolecular | $k[\ce{A}][\ce{B}]$ |
| $\ce{2A -> products}$ | bimolecular | $k[\ce{A}]^2$ |
| $\ce{A + B + C -> products}$ | termolecular (rare) | $k[\ce{A}][\ce{B}][\ce{C}]$ |

> **Elementary step → coefficients ARE the exponents. Overall reaction → rate law from EXPERIMENT only.**

**Temporary species (both cancel from the overall equation):**

| Species | Pattern | Appears... |
|---|---|---|
| **Intermediate** | made then consumed | product side first (up-then-down) |
| **Catalyst** | consumed then regenerated | reactant side first; present at start & end |

**Rate-determining step (RDS)** = **slowest** step = **tallest hump** on the energy profile.

**Deriving the overall rate law:**
- **Slow step first:** rate = rate law of that step (from its coefficients). Species entering only later are absent.
- **Fast equilibrium, then slow step:** write the slow step's rate law → set forward = reverse for the fast step → solve for the intermediate → **substitute** to eliminate it. (No steady-state needed.)
- **A rate law never contains an intermediate.**

**Valid mechanism = passes BOTH:** (1) steps **sum to the overall equation**, and (2) predicted rate law **matches experiment**.

**Multistep energy profile:** one hump per step; valleys between humps = intermediates; **tallest transition state = RDS**; products below reactants = exothermic, above = endothermic.

---

<div align="center">

[← Collision Model and Arrhenius](/chemistry/0704-collision-model-arrhenius) | [Catalysis →](/chemistry/0706-catalysis)

</div>
