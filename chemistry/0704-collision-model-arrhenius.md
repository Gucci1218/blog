# Collision Model, Activation Energy, and Arrhenius
<p class="article-date">July 5, 2026</p>

*There's a little concrete skate park near my house, and the centerpiece is a ramp with a rounded hump right in the middle. All afternoon I watched skaters try to clear it. A kid would push off, roll toward the hump, and one of two things happened. If they were rolling too slow, they'd climb partway up, stall, and roll right back down to where they started — nothing accomplished. But if they came in fast enough, they'd sail up and over the top and coast down the far side to the other half of the park. Same hump, same ramp, totally different outcomes — and the only thing that decided it was whether the skater had enough speed to get over the top. That hump is the single best picture I know for **why chemical reactions happen (or don't)**. Molecules are the skaters, their speed is their energy, and the hump is the **activation energy** — an energy hill every reaction has to climb before reactants can become products. This is Topics 5.5 and 5.6, and it finally answers the question that's been hanging over all of kinetics: why does heating something up make it react faster?*

---

## What You'll Learn

- State the two requirements of **collision theory** — enough energy **and** correct orientation — and explain why most collisions don't lead to a reaction
- Define **activation energy** ($E_a$) as the energy hill separating reactants from products, and locate the **activated complex** (transition state) at the top
- **Read and label a reaction energy profile**: reactants, products, transition state, $E_a$ (forward and reverse), and $\Delta H$
- Compute $\Delta H$, the forward $E_a$, or the reverse $E_a$ from a diagram, using $E_{a,\text{rev}} = E_{a,\text{fwd}} - \Delta H$
- Distinguish **exothermic** (products lower) from **endothermic** (products higher) profiles at a glance
- Use the **Maxwell–Boltzmann distribution** to explain *precisely* why a small temperature rise causes a big rate increase — the fraction of molecules past $E_a$
- Interpret the **Arrhenius equation** $k = Ae^{-E_a/RT}$ qualitatively (how $E_a$, $T$, and $A$ each push $k$)
- Use the **two-point Arrhenius equation** to find $E_a$ from rate constants at two temperatures, or to find $k$ at a new temperature
- Extract $E_a$ from the **slope of an Arrhenius plot** ($\ln k$ vs. $1/T$)
- Unify the **four factors that speed up a reaction** — concentration, temperature, surface area, and catalyst — under one collision-based story

---

## Prerequisites

- [Kinetic Molecular Theory](/chemistry/0505-kinetic-molecular-theory) — the **Maxwell–Boltzmann distribution** is the whole payoff of this article; you need to already picture how the spread of molecular speeds shifts and flattens with temperature, because that curve is *literally* the reason heat speeds up reactions
- [Bond Energy and Length](/chemistry/0402-bond-energy-and-length) — a reaction energy profile is a **potential-energy curve** just like the one you drew for a bond; the "energy hill" here is the same idea as the "energy well" there, flipped into a barrier

---

## The Core Concept

### Intuition First

Let's stay at the skate park, because every piece of collision theory is sitting on that ramp.

**A skater rolling at the hump is a collision.** For anything to happen — for a skater to end up on the *far* side — they first have to actually roll up to the hump. In chemistry, before two molecules can react, they have to physically run into each other. No collision, no reaction. Ever. That's the first word in "collision theory."

**The skater's speed is the molecule's kinetic energy.** A slow skater doesn't have enough oomph to reach the top; a fast one does. Molecules carry **kinetic energy** ($KE = \tfrac{1}{2}mv^2$, straight from [KMT](/chemistry/0505-kinetic-molecular-theory)), and just like the skater's speed, it's the thing that decides whether a collision has what it takes.

**The height of the hump is the activation energy.** Every ramp has *some* hump — a minimum amount of speed you need to clear it. Chemistry calls that minimum energy the **activation energy**, $E_a$. Come in with less than $E_a$ and you stall out and slide back to reactants (no reaction). Come in with $E_a$ or more and you make it over the top to products.

**Clearing the hump is a successful reaction.** Getting over the top and coasting down the far side is the reaction actually happening — reactants have turned into products. Stalling and rolling back is a **failed collision**: the molecules bounce apart unchanged.

**But speed isn't the whole story — you have to hit the hump straight on.** Picture a skater who's rolling plenty fast but comes at the hump sideways, at a weird angle. They catch an edge and wipe out instead of clearing it. Molecules are the same: even a hard, energetic collision fails if the molecules are pointed the wrong way. This is the **orientation requirement**. A reaction needs the reactive parts of the molecules to actually meet.

**The crowd's spread of speeds is the Maxwell–Boltzmann distribution.** Here's the part that makes everything click. At the park, not everyone rolls at the same speed — there's a whole spread, from timid little kids barely moving to teenagers bombing the ramp. Only the ones rolling faster than the hump's threshold make it over. Now crank up the energy of the whole park — say everyone's hyped and pushing harder. The *whole crowd* speeds up, and suddenly a **much** bigger fraction of skaters can clear the same hump. That is exactly what raising temperature does to molecules, and it's the deep reason heat speeds up reactions.

Here's the map to carry through the whole article:

| The skate park | The chemistry |
|---|---|
| A skater rolling at the hump | a **collision** between molecules |
| The skater's speed | the molecules' **kinetic energy** |
| Height of the hump | the **activation energy**, $E_a$ |
| Needing to hit it straight on | the **orientation** requirement |
| Clearing the hump → far side | a **successful reaction** (products form) |
| Stalling and rolling back | a **failed collision** (no reaction) |
| The crowd's spread of speeds | the **Maxwell–Boltzmann distribution** |
| Hyping up the whole park | raising the **temperature** |

### Collision Theory, Formally

**Collision theory** says a reaction occurs only when reactant particles collide, and a collision leads to product *only if* it meets two conditions:

1. **Sufficient energy** — the combined kinetic energy of the colliding particles must be **at least the activation energy**, $E_a$. This energy is what breaks the old bonds so new ones can form.
2. **Correct orientation** — the particles must be lined up so the right atoms make contact.

A collision that satisfies both is called an **effective** (or successful) collision. Here's the humbling part: at any instant, molecules undergo an astronomical number of collisions per second, and the **overwhelming majority accomplish nothing** — they're either too gentle or badly aimed. Reactions seem fast to us, but on the molecular scale they're the rare lucky bounces.

$$\text{rate} \;\propto\; (\text{collision frequency}) \times (\text{fraction energetic enough}) \times (\text{fraction oriented right})$$

Every factor that speeds up a reaction works by pushing on one of those three terms — hold that thought for the end of the article.

### Activation Energy and the Reaction Energy Profile

Now let's draw the hump properly. A **reaction energy profile** (or reaction coordinate diagram) plots **potential energy** on the y-axis against **reaction progress** on the x-axis — the journey from reactants (left) to products (right).

This is the same idea as the potential-energy curve from [Bond Energy and Length](/chemistry/0402-bond-energy-and-length): energy stored in the arrangement of atoms, plotted as the atoms move. There, the curve dipped into a **well** (a stable bond). Here, the curve rises into a **hill** the reaction must climb.

Here's an **exothermic** profile (products end up *lower* than reactants), drawn in ASCII:

```
        PE
         |            /\   <-- activated complex (transition state)
         |           /  \
         |          /    \
         |  ___    /      \
         | react\_/        \        E_a(fwd) = peak - reactants
         |                  \___
         |                  products
         |________________________________  reaction progress
```

The features you must be able to label:

- **Reactants** — the starting energy level (left plateau).
- **Products** — the ending energy level (right plateau).
- **Activated complex / transition state** — the species at the very **top of the hump**. Bonds are half-broken and half-formed; it's the least stable point on the path and exists for only an instant. (On the ramp: the skater balanced right at the peak, about to tip one way or the other.)
- **Forward activation energy** $E_{a,\text{fwd}}$ — the climb **from reactants up to the peak**.
- **Reverse activation energy** $E_{a,\text{rev}}$ — the climb **from products up to the same peak** (running the reaction backward has to clear the hill too, just from the other side).
- **Enthalpy change** $\Delta H$ — the **net** drop or rise, measured from reactants to products:

$$\Delta H = E_{\text{products}} - E_{\text{reactants}}$$

**Exothermic vs. endothermic at a glance:**

| | Products vs. reactants | $\Delta H$ | Skate-park picture |
|---|---|---|---|
| **Exothermic** | products **lower** | $\Delta H < 0$ | far side of the ramp sits **below** the start — you coast out lower than you came in |
| **Endothermic** | products **higher** | $\Delta H > 0$ | far side sits **above** the start — you end up on a raised platform |

A relationship the AP exam loves — and one you can read straight off the diagram — connects the two barriers to $\Delta H$:

$$E_{a,\text{rev}} = E_{a,\text{fwd}} - \Delta H$$

Why? Both $E_a$'s are measured up to the same peak. Going forward you climb from the reactant level; going back you climb from the product level. The difference between those two starting levels is exactly $\Delta H$. For an exothermic reaction ($\Delta H < 0$), subtracting a negative makes $E_{a,\text{rev}}$ **larger** than $E_{a,\text{fwd}}$ — which makes sense: if products sat in a deep valley, climbing back out is a taller hill.

> **Key point:** $E_a$ and $\Delta H$ are *independent*. $E_a$ is about the **hump's height** (how hard the reaction is to start — a kinetics question); $\Delta H$ is about the **difference in the two plateaus** (how much energy is released or absorbed overall — a thermodynamics question). A reaction can be very exothermic yet painfully slow because its hump is enormous. Gasoline sitting in air is a perfect example: hugely exothermic, but it needs a spark because $E_a$ is high.

### The Maxwell–Boltzmann Payoff: Why Heat Speeds Things Up

This is the moment everything in [KMT](/chemistry/0505-kinetic-molecular-theory) pays off. Back there you learned that molecules in a sample don't all move at one speed — they have a whole spread, described by the **Maxwell–Boltzmann distribution**: a curve with molecular energy on the x-axis and *number (or fraction) of molecules* on the y-axis. It starts at the origin, rises to a peak, and trails off in a **long tail to the right** (a few molecules are always moving very fast).

Now overlay a vertical line at $x = E_a$ — the hump's height. **Only molecules to the right of that line have enough energy to react.** The shaded area under the tail past $E_a$ is the *fraction of molecules that can clear the hump*:

```
 fraction of
 molecules
    |        _
    |      /   \        E_a
    |     /     \        |
    |    /       \       |
    |   /         \::::  |  <- shaded tail = fraction with KE >= E_a
    |  /           \::::::::__
    | /             \::::::::::::___
    |/_____________________|__________  molecular kinetic energy
                          E_a
```

Here's the magic. Raise the temperature and the whole curve **shifts right and flattens out** — the peak drops and slides toward higher energy, while the long tail lifts up (the total area stays the same, since you still have the same number of molecules). The $E_a$ line doesn't move — the *hump is the same height* — but the shaded tail beyond it **grows dramatically**.

That growth is *not* proportional to the temperature bump. Because the tail is exponential, even a modest temperature increase — say 10 °C — can **roughly double** the fraction of molecules with $KE \ge E_a$, and therefore roughly double the rate. A little more heat, a *lot* more effective collisions.

That's the skate park cranked up: same hump, but hype the whole park and a far bigger slice of skaters comes in fast enough to clear it.

> **The one sentence that scores the point:** heating speeds up a reaction *mainly* because it increases the **fraction of molecules with kinetic energy greater than or equal to $E_a$** (the shaded tail grows). Molecules do move faster and collide a bit more often too — but on the AP exam, "molecules move faster" **alone is not enough credit**. You must name the fraction exceeding $E_a$.

### The Arrhenius Equation

Svante Arrhenius bottled this entire story into one equation for the **rate constant** $k$:

$$k = A\,e^{-E_a/RT}$$

- $k$ — the rate constant (bigger $k$ = faster reaction)
- $A$ — the **frequency factor** (a.k.a. pre-exponential factor): how often collisions happen **and** the fraction with the right **orientation**. This is where the orientation requirement lives.
- $E_a$ — activation energy (J/mol)
- $R$ — gas constant, $8.314\ \text{J mol}^{-1}\text{K}^{-1}$ (use the **joule** version here, not 0.08206)
- $T$ — absolute temperature in **kelvin**

The heart of it is the exponential term $e^{-E_a/RT}$, which is precisely the **fraction of molecules that clear the hump** — the shaded Maxwell–Boltzmann tail, written as a formula. Read the equation qualitatively:

| Change | Effect on $e^{-E_a/RT}$ | Effect on $k$ | Meaning |
|---|---|---|---|
| **Larger $E_a$** | smaller | $k$ **decreases** | taller hump → fewer molecules clear it → **slower** |
| **Higher $T$** | larger | $k$ **increases** | hotter → tail grows → **faster** |
| **Larger $A$** | (multiplies) | $k$ **increases** | more/better-aimed collisions → faster |

### The Linear Form and the Arrhenius Plot

Take the natural log of both sides and the equation turns into a **straight line** — the same linearization trick from [Graphing and Linearization](/chemistry/0105-graphing-linearization):

$$\ln k = \ln A - \frac{E_a}{R}\cdot\frac{1}{T}$$

Compare to $y = b + m x$:

- $y = \ln k$
- $x = \dfrac{1}{T}$
- slope $m = -\dfrac{E_a}{R}$
- intercept $b = \ln A$

So if you measure $k$ at several temperatures and plot $\ln k$ (y-axis) against $1/T$ (x-axis), you get a straight line with a **negative slope**, and:

$$E_a = -R \times (\text{slope}) \qquad\Longleftrightarrow\qquad \text{slope} = -\frac{E_a}{R}$$

A **steeper** (more negative) slope means a **larger** activation energy.

### The Two-Point Arrhenius Equation

Usually you don't have a whole plot — just $k$ at two temperatures. Write the linear form at $T_1$ and $T_2$ and subtract; the $\ln A$ cancels, leaving the workhorse formula:

$$\ln\!\left(\frac{k_2}{k_1}\right) = -\frac{E_a}{R}\left(\frac{1}{T_2} - \frac{1}{T_1}\right)$$

With this one equation you can (a) find $E_a$ from two rate constants, (b) find $k_2$ at a new temperature, or (c) find the missing temperature. Every term must use **kelvin** and $R = 8.314\ \text{J mol}^{-1}\text{K}^{-1}$, which gives $E_a$ in **joules per mole** (divide by 1000 for kJ/mol).

### The Four Factors That Speed Up a Reaction

Everything ties back to the collision equation: rate depends on collision **frequency**, the **energy** fraction, and the **orientation** fraction. Each factor pushes one of those levers.

| Factor | What it changes | Collision-theory reason | Everyday picture |
|---|---|---|---|
| **↑ Concentration** (or pressure for gases) | more particles per volume | more **collisions per second** (higher frequency) | a more crowded skate park = more skaters hitting the hump |
| **↑ Temperature** | molecular energy | bigger **fraction with $KE \ge E_a$** (the MB tail) *and* somewhat more frequent collisions | hype the whole park so more skaters clear the hump |
| **↑ Surface area** | exposed contact area of a solid | more sites for **collisions** to happen | see below |
| **Catalyst** | provides a new pathway with **lower $E_a$** | more molecules clear a **shorter** hump | a ramp with a smaller hump — everyone gets over |

**Surface area — the Alka-Seltzer demo.** Drop a *whole* Alka-Seltzer tablet in water and it fizzes steadily. Drop a *crushed* one and it erupts almost instantly. Same amount of chemical, same temperature — but crushing it exposes vastly more surface for water molecules to collide with. Reactions between a solid and a fluid happen only at the surface, so more surface = more collision area = faster.

**Catalyst — a preview.** A **catalyst** speeds a reaction by opening an alternate route with a **lower activation energy** — it shrinks the hump without being consumed. On the Maxwell–Boltzmann curve, lowering $E_a$ slides the cutoff line *left*, so a bigger tail (more molecules) suddenly qualifies — even at the *same* temperature. Notice a catalyst does **not** change $\Delta H$: the two plateaus stay put; only the hump between them gets shorter. We give catalysts the full treatment next → [Catalysis](/chemistry/0706-catalysis).

---

## Worked Examples

### Example 1: The Two Requirements

**Problem:** Two $\ce{NO}$ molecules collide with more than enough energy to react, yet no reaction occurs. Give a specific reason and name the general requirement it illustrates.

**Solution:**
- Collision theory needs **both** sufficient energy **and** correct orientation.
- Here the energy condition is met, so the failure must be **orientation** — the molecules were aligned so the atoms that need to bond didn't make contact (e.g., they hit oxygen-to-oxygen instead of the reactive positions).

**Answer:** The collision had enough energy but the **wrong orientation**, so it was ineffective — this is the **orientation requirement**.

### Example 2: Labeling an Energy Profile

**Problem:** A reaction profile shows reactants at 30 kJ/mol, a peak at 90 kJ/mol, and products at 50 kJ/mol. Find $E_{a,\text{fwd}}$, $\Delta H$, and state whether the reaction is exo- or endothermic.

**Solution:**
- **Step 1 — Forward $E_a$:** climb from reactants to peak = $90 - 30 = 60$ kJ/mol.
- **Step 2 — $\Delta H$:** products minus reactants = $50 - 30 = +20$ kJ/mol.
- **Step 3 — Classify:** products are *higher* than reactants and $\Delta H > 0$ → **endothermic**.

**Answer:** $E_{a,\text{fwd}} = 60$ kJ/mol, $\Delta H = +20$ kJ/mol, **endothermic**.

### Example 3: Reverse Activation Energy

**Problem:** Using the same diagram (reactants 30, peak 90, products 50 kJ/mol), find the reverse activation energy two ways.

**Solution:**
- **Direct read:** reverse climbs from products (50) to the peak (90): $90 - 50 = 40$ kJ/mol.
- **Formula check:** $E_{a,\text{rev}} = E_{a,\text{fwd}} - \Delta H = 60 - (+20) = 40$ kJ/mol. ✓

**Answer:** $E_{a,\text{rev}} = 40$ kJ/mol (both methods agree).

### Example 4: Exothermic Reverse Barrier

**Problem:** An exothermic reaction has $E_{a,\text{fwd}} = 45$ kJ/mol and $\Delta H = -80$ kJ/mol. Find $E_{a,\text{rev}}$ and comment on which direction is harder to start.

**Solution:**
- $E_{a,\text{rev}} = E_{a,\text{fwd}} - \Delta H = 45 - (-80) = 45 + 80 = 125$ kJ/mol.
- The reverse barrier (125) is much taller than the forward one (45).

**Answer:** $E_{a,\text{rev}} = 125$ kJ/mol. Because products sit in a deep valley (very exothermic), running the reaction **backward** is far harder — a much taller hump to climb.

### Example 5: Reading Maxwell–Boltzmann

**Problem:** On one set of axes you're shown the Maxwell–Boltzmann curve for a gas at two temperatures, with a fixed $E_a$ line drawn in. Curve B's peak is lower and shifted right of curve A's. Which curve is at the higher temperature, and which has more molecules able to react?

**Solution:**
- Higher temperature → curve shifts **right** (higher average energy) and **flattens** (lower, broader peak). That's curve **B**.
- More molecules past the $E_a$ line = larger shaded tail. B's tail extends further right, so **B** has more molecules with $KE \ge E_a$.

**Answer:** **Curve B** is hotter and has the larger fraction of molecules able to react — so the reaction is faster at B's temperature.

### Example 6: Why Temperature Increases Rate (AP wording)

**Problem:** In terms of collision theory, explain why raising the temperature from 25 °C to 35 °C speeds up a reaction. Write the answer as the AP rubric wants it.

**Solution / Answer:** Raising the temperature increases the average kinetic energy of the molecules, which **increases the fraction of molecules with kinetic energy greater than or equal to the activation energy** (the Maxwell–Boltzmann tail past $E_a$ grows). More collisions are therefore energetic enough to be effective, so the rate increases. (Collisions also become slightly more frequent, but the dominant effect is the larger fraction exceeding $E_a$.)

### Example 7: Arrhenius — Qualitative

**Problem:** Reaction X and reaction Y run at the same temperature with the same frequency factor $A$, but $E_a(\text{X}) = 40$ kJ/mol and $E_a(\text{Y}) = 80$ kJ/mol. Which has the larger rate constant?

**Solution:**
- In $k = A e^{-E_a/RT}$, a **larger** $E_a$ makes the exponent more negative → smaller $e^{-E_a/RT}$ → smaller $k$.
- X has the smaller barrier.

**Answer:** Reaction **X** has the larger $k$ (lower hump → more molecules clear it → faster).

### Example 8: Two-Point Arrhenius — Find $E_a$

**Problem:** A reaction has $k_1 = 2.5\times10^{-3}\ \text{s}^{-1}$ at $T_1 = 300\ \text{K}$ and $k_2 = 2.0\times10^{-2}\ \text{s}^{-1}$ at $T_2 = 320\ \text{K}$. Find $E_a$ in kJ/mol.

**Solution:**
- **Step 1 — Ratio:** $\dfrac{k_2}{k_1} = \dfrac{2.0\times10^{-2}}{2.5\times10^{-3}} = 8.0$, so $\ln(8.0) = 2.079$.
- **Step 2 — The temperature term:**
$$\frac{1}{T_2} - \frac{1}{T_1} = \frac{1}{320} - \frac{1}{300} = 0.0031250 - 0.0033333 = -2.083\times10^{-4}\ \text{K}^{-1}$$
- **Step 3 — Solve** $\ln\!\frac{k_2}{k_1} = -\dfrac{E_a}{R}\left(\frac{1}{T_2}-\frac{1}{T_1}\right)$ for $E_a$:
$$E_a = -\frac{R\,\ln(k_2/k_1)}{\left(\frac{1}{T_2}-\frac{1}{T_1}\right)} = -\frac{(8.314)(2.079)}{-2.083\times10^{-4}} = 8.30\times10^{4}\ \text{J/mol}$$

**Answer:** $E_a \approx 83\ \text{kJ/mol}$.

### Example 9: Two-Point Arrhenius — Find a New $k$

**Problem:** A reaction has $E_a = 50.0\ \text{kJ/mol}$ and $k_1 = 1.0\times10^{-2}\ \text{s}^{-1}$ at $T_1 = 298\ \text{K}$. Find $k_2$ at $T_2 = 350\ \text{K}$.

**Solution:**
- **Step 1 — Temperature term:** $\dfrac{1}{350} - \dfrac{1}{298} = 0.0028571 - 0.0033557 = -4.986\times10^{-4}\ \text{K}^{-1}$.
- **Step 2 — Right side** (use $E_a = 50000\ \text{J/mol}$):
$$-\frac{E_a}{R}\left(\frac{1}{T_2}-\frac{1}{T_1}\right) = -\frac{50000}{8.314}\left(-4.986\times10^{-4}\right) = +2.998$$
- **Step 3 — Exponentiate:** $\dfrac{k_2}{k_1} = e^{2.998} = 20.0$, so $k_2 = 20.0 \times (1.0\times10^{-2}) = 0.20\ \text{s}^{-1}$.

**Answer:** $k_2 \approx 0.20\ \text{s}^{-1}$ — a ~52 °C jump multiplied the rate constant about **20-fold**.

### Example 10: $E_a$ from an Arrhenius Plot Slope

**Problem:** A plot of $\ln k$ vs. $1/T$ is a straight line with slope $= -6.5\times10^{3}\ \text{K}$. Find $E_a$.

**Solution:**
- Slope $= -\dfrac{E_a}{R}$, so $E_a = -R \times \text{slope} = -(8.314)(-6.5\times10^{3}) = 5.4\times10^{4}\ \text{J/mol}$.

**Answer:** $E_a \approx 54\ \text{kJ/mol}$.

### Example 11: Which Factor, Which Lever

**Problem:** For each change, name whether the rate rises and which collision-theory term it affects: (a) crushing a solid reactant, (b) adding a catalyst, (c) diluting a solution with water.

**Solution:**
- **(a)** Crushing increases **surface area** → more collision sites → rate **up** (collision frequency/area).
- **(b)** Catalyst gives a path with **lower $E_a$** → bigger fraction clears the hump → rate **up** (energy fraction), and $\Delta H$ unchanged.
- **(c)** Diluting lowers **concentration** → fewer collisions per second → rate **down** (collision frequency).

**Answer:** (a) faster, surface area; (b) faster, lower $E_a$; (c) slower, lower concentration.

### Example 12: Catalyst on the Diagram

**Problem:** A reaction has $E_{a,\text{fwd}} = 75$ kJ/mol and $\Delta H = -30$ kJ/mol. A catalyst lowers the forward barrier to 40 kJ/mol. Find the new **reverse** barrier, and state what happens to $\Delta H$.

**Solution:**
- $\Delta H$ is unchanged by a catalyst: still $-30$ kJ/mol (the plateaus don't move).
- New $E_{a,\text{rev}} = E_{a,\text{fwd}} - \Delta H = 40 - (-30) = 70$ kJ/mol (was $75-(-30)=105$; the catalyst lowered **both** barriers by the same 35 kJ/mol).

**Answer:** New $E_{a,\text{rev}} = 70$ kJ/mol; **$\Delta H$ stays $-30$ kJ/mol** — a catalyst shrinks the hump, never the plateaus.

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Saying heat speeds reactions because "molecules move faster" | It's *partly* true, so it feels complete | Always finish the sentence: it raises the **fraction of molecules with $KE \ge E_a$**. That phrase earns the point. |
| Confusing $E_a$ with $\Delta H$ | Both are "energies" on the same diagram | $E_a$ = height of the **hump** (start to reach); $\Delta H$ = difference between the two **plateaus** (start to finish). They're independent. |
| Reading $\Delta H$ from the peak | The peak is the biggest number on the graph | $\Delta H$ **never** touches the peak: $\Delta H = E_{\text{products}} - E_{\text{reactants}}$, plateau to plateau. |
| Thinking a catalyst changes $\Delta H$ | It clearly changes the picture | A catalyst lowers **$E_a$ only**. Reactant and product levels — and thus $\Delta H$ — are untouched. |
| Using $R = 0.08206$ in Arrhenius | It's the $R$ you memorized for gases | Arrhenius uses energy units: $R = 8.314\ \text{J mol}^{-1}\text{K}^{-1}$, giving $E_a$ in **joules**/mol. |
| Forgetting kelvin, or leaving $E_a$ in kJ | Data is often given in °C and kJ | Convert to **K** ($+273$) and to **J/mol** ($\times 1000$) before plugging in. |
| Dropping the minus sign in the two-point equation | The $-E_a/R$ is easy to lose | Sanity check: if $T_2 > T_1$ then $k_2 > k_1$, so $\ln(k_2/k_1)$ must come out **positive**. |
| Drawing the MB curve as a symmetric bell | It looks bell-ish near the top | It starts at the origin and has a **long right tail** — that tail *is* the reactive fraction. |

---

## AP Exam Tips

- **Energy-profile labeling is basically guaranteed.** Be able to mark, on a given diagram: **reactants, products, transition state (activated complex)**, **$E_a$ forward**, **$E_a$ reverse**, and **$\Delta H$**. Practice the arrows: $E_a$ arrows go from a plateau **up to the peak**; the $\Delta H$ arrow goes **plateau to plateau**.
- **Know the sign story cold.** Exothermic → products **lower**, $\Delta H < 0$. Endothermic → products **higher**, $\Delta H > 0$. And $E_{a,\text{rev}} = E_{a,\text{fwd}} - \Delta H$.
- **The Maxwell–Boltzmann sketch shows up in free response.** Practice: draw the curve, drop a vertical $E_a$ line, shade the tail beyond it, then redraw at higher $T$ (peak lower and shifted right, tail bigger, **same total area**). Label axes: energy on x, number/fraction of molecules on y.
- **"Why does temperature increase the rate?" has a required phrase.** You must cite the **increased fraction of molecules with kinetic energy $\ge E_a$**. "Molecules move faster" alone will *not* get full credit.
- **The two-point Arrhenius calc is a standard problem.** Memorize $\ln\frac{k_2}{k_1} = -\frac{E_a}{R}\left(\frac{1}{T_2}-\frac{1}{T_1}\right)$, use $R = 8.314$, and work in kelvin. Show every step — the AP graders give method points.
- **Arrhenius plot direction.** $\ln k$ vs. $1/T$ gives slope $= -E_a/R$, so $E_a = -R(\text{slope})$. Steeper (more negative) slope = larger $E_a$.
- **Catalyst answers must say "lowers $E_a$, provides an alternate pathway, is not consumed, does not change $\Delta H$."** Those are the point-earning phrases.
- **Calculator note:** you'll need $\ln$ and $e^x$ fluently. When solving for $E_a$, isolate it *symbolically* first, then plug in — it prevents sign slips.

---

## Practice Problems

### Problem 1
State the two conditions a collision must satisfy to produce a reaction, and explain why the vast majority of collisions fail.

<details>
<summary><strong>Solution</strong></summary>

A collision leads to reaction only if it has (1) **energy** at least equal to the activation energy $E_a$, **and** (2) the **correct orientation** of the colliding particles. Most collisions fail because at ordinary temperatures only a small fraction of molecules carry $KE \ge E_a$, and of those, many are still aimed wrong. Both conditions must be met at once, so effective collisions are relatively rare.

**Answer:** Sufficient energy ($\ge E_a$) **and** correct orientation; most collisions lack one or both.

</details>

---

### Problem 2
A reaction profile shows reactants at 40 kJ/mol, the peak at 110 kJ/mol, and products at 25 kJ/mol. Find $E_{a,\text{fwd}}$, $\Delta H$, and classify the reaction.

<details>
<summary><strong>Solution</strong></summary>

- $E_{a,\text{fwd}} = 110 - 40 = 70$ kJ/mol.
- $\Delta H = 25 - 40 = -15$ kJ/mol.
- Products lower, $\Delta H < 0$ → **exothermic**.

**Answer:** $E_{a,\text{fwd}} = 70$ kJ/mol, $\Delta H = -15$ kJ/mol, **exothermic**.

</details>

---

### Problem 3
Using the diagram in Problem 2, find the reverse activation energy.

<details>
<summary><strong>Solution</strong></summary>

Direct: $E_{a,\text{rev}} = 110 - 25 = 85$ kJ/mol.
Check: $E_{a,\text{rev}} = E_{a,\text{fwd}} - \Delta H = 70 - (-15) = 85$ kJ/mol. ✓

**Answer:** 85 kJ/mol.

</details>

---

### Problem 4
An endothermic reaction has $E_{a,\text{fwd}} = 120$ kJ/mol and $\Delta H = +35$ kJ/mol. Find $E_{a,\text{rev}}$.

<details>
<summary><strong>Solution</strong></summary>

$E_{a,\text{rev}} = E_{a,\text{fwd}} - \Delta H = 120 - (+35) = 85$ kJ/mol.

For an endothermic reaction the forward barrier is the taller one, which checks out ($120 > 85$).

**Answer:** 85 kJ/mol.

</details>

---

### Problem 5
Explain, in the exact way the AP rubric wants, why a reaction runs faster at 60 °C than at 20 °C.

<details>
<summary><strong>Solution</strong></summary>

At the higher temperature the molecules have greater average kinetic energy, so a **larger fraction of molecules have kinetic energy greater than or equal to the activation energy** (the Maxwell–Boltzmann tail beyond $E_a$ is bigger). A greater fraction of collisions is therefore effective, increasing the rate. (Collision frequency also rises slightly, but the fraction exceeding $E_a$ is the dominant effect.)

**Answer:** Higher $T$ → bigger fraction of molecules with $KE \ge E_a$ → more effective collisions → faster.

</details>

---

### Problem 6
Sketch-describe how the Maxwell–Boltzmann distribution for a reacting gas changes when the temperature is **lowered**, and what that does to the reaction rate.

<details>
<summary><strong>Solution</strong></summary>

Lowering $T$ shifts the curve **left** (lower average energy) and makes the peak **taller and narrower**; the total area under the curve stays the same. The $E_a$ line is unchanged, but the shaded tail beyond it **shrinks**, so fewer molecules have $KE \ge E_a$. The fraction of effective collisions drops and the **rate decreases**.

**Answer:** Curve shifts left and sharpens; tail past $E_a$ shrinks; rate goes down.

</details>

---

### Problem 7
In $k = Ae^{-E_a/RT}$, describe what happens to $k$ if (a) $E_a$ doubles (all else fixed) and (b) $T$ increases.

<details>
<summary><strong>Solution</strong></summary>

- **(a)** Doubling $E_a$ makes the exponent $-E_a/RT$ twice as negative, so $e^{-E_a/RT}$ shrinks and $k$ **decreases** (much slower — the effect is exponential).
- **(b)** Increasing $T$ makes $-E_a/RT$ less negative (closer to 0), so $e^{-E_a/RT}$ grows and $k$ **increases** (faster).

**Answer:** (a) $k$ decreases; (b) $k$ increases.

</details>

---

### Problem 8
A reaction has $k_1 = 4.0\times10^{-4}\ \text{s}^{-1}$ at 310 K and $k_2 = 3.2\times10^{-3}\ \text{s}^{-1}$ at 330 K. Find $E_a$ in kJ/mol.

<details>
<summary><strong>Solution</strong></summary>

- $\dfrac{k_2}{k_1} = \dfrac{3.2\times10^{-3}}{4.0\times10^{-4}} = 8.0$, so $\ln 8.0 = 2.079$.
- $\dfrac{1}{330} - \dfrac{1}{310} = 0.0030303 - 0.0032258 = -1.955\times10^{-4}\ \text{K}^{-1}$.
- $E_a = -\dfrac{R\ln(k_2/k_1)}{\left(\frac{1}{T_2}-\frac{1}{T_1}\right)} = -\dfrac{(8.314)(2.079)}{-1.955\times10^{-4}} = 8.84\times10^{4}\ \text{J/mol}$.

**Answer:** $E_a \approx 88\ \text{kJ/mol}$.

</details>

---

### Problem 9
A reaction has $E_a = 75.0$ kJ/mol and $k_1 = 5.0\times10^{-3}\ \text{s}^{-1}$ at 300 K. Find $k_2$ at 340 K.

<details>
<summary><strong>Solution</strong></summary>

- $\dfrac{1}{340} - \dfrac{1}{300} = 0.0029412 - 0.0033333 = -3.922\times10^{-4}\ \text{K}^{-1}$.
- $-\dfrac{E_a}{R}\left(\frac{1}{T_2}-\frac{1}{T_1}\right) = -\dfrac{75000}{8.314}(-3.922\times10^{-4}) = +3.539$.
- $\dfrac{k_2}{k_1} = e^{3.539} = 34.4$, so $k_2 = 34.4 \times 5.0\times10^{-3} = 0.17\ \text{s}^{-1}$.

**Answer:** $k_2 \approx 0.17\ \text{s}^{-1}$.

</details>

---

### Problem 10
An Arrhenius plot ($\ln k$ vs. $1/T$) has slope $-1.05\times10^{4}\ \text{K}$. Find $E_a$ in kJ/mol.

<details>
<summary><strong>Solution</strong></summary>

$E_a = -R \times \text{slope} = -(8.314)(-1.05\times10^{4}) = 8.73\times10^{4}\ \text{J/mol}$.

**Answer:** $E_a \approx 87\ \text{kJ/mol}$.

</details>

---

### Problem 11
Two reactions are studied at the same temperature. Reaction P has the steeper (more negative) slope on its Arrhenius plot. Which reaction has the larger activation energy, and which is more sensitive to a temperature change?

<details>
<summary><strong>Solution</strong></summary>

Slope $= -E_a/R$, so a steeper (more negative) slope means a **larger $E_a$** — reaction **P**. Reactions with larger $E_a$ are **more sensitive** to temperature changes (their rate constants change more for a given $\Delta T$, because the exponential term responds more strongly). So P is also the more temperature-sensitive.

**Answer:** P has the larger $E_a$ and is more temperature-sensitive.

</details>

---

### Problem 12
Explain, using collision theory, why a whole Alka-Seltzer tablet fizzes slowly but a crushed one fizzes violently in the same amount of water at the same temperature.

<details>
<summary><strong>Solution</strong></summary>

The reaction happens where the solid meets the water, i.e., at the tablet's **surface**. Crushing the tablet dramatically increases its **surface area**, exposing far more solid to collide with water molecules. More collision area means more effective collisions per second, so the rate rises sharply — even though the amount of reactant, concentration, and temperature are all unchanged.

**Answer:** Crushing increases surface area → more collision sites → faster reaction.

</details>

---

### Problem 13
A reaction has $E_{a,\text{fwd}} = 90$ kJ/mol and $\Delta H = -40$ kJ/mol. A catalyst lowers the forward barrier to 55 kJ/mol. (a) What is the new reverse barrier? (b) What is $\Delta H$ after adding the catalyst?

<details>
<summary><strong>Solution</strong></summary>

- **(a)** New $E_{a,\text{rev}} = E_{a,\text{fwd}} - \Delta H = 55 - (-40) = 95$ kJ/mol.
- **(b)** A catalyst does not change $\Delta H$: still $-40$ kJ/mol. (The forward barrier dropped by 35 kJ/mol, and so did the reverse: it went from $90-(-40)=130$ down to 95.)

**Answer:** (a) 95 kJ/mol; (b) $\Delta H = -40$ kJ/mol (unchanged).

</details>

---

### Problem 14
For the reaction $\ce{2NO2 -> 2NO + O2}$, list four separate changes that would increase the rate, and name the collision-theory reason for each.

<details>
<summary><strong>Solution</strong></summary>

1. **Increase the concentration (pressure) of $\ce{NO2}$** → more collisions per second (higher frequency).
2. **Increase temperature** → larger fraction of molecules with $KE \ge E_a$ (and slightly more frequent collisions).
3. **Add a catalyst** → lower $E_a$, so a bigger fraction clears the barrier.
4. **Increase surface area** (if a solid catalyst/surface is involved) → more sites for effective collisions.

**Answer:** ↑concentration, ↑temperature, catalyst, ↑surface area — each raising the number of effective collisions.

</details>

---

### Problem 15
A student claims: "Since this reaction is very exothermic, it must be very fast." Evaluate the claim.

<details>
<summary><strong>Solution</strong></summary>

The claim is **false**. Being exothermic ($\Delta H < 0$) describes the **energy difference between products and reactants** — a thermodynamic fact about *how much* energy is released. Reaction **speed** depends on the **activation energy** $E_a$ — the height of the hump the reaction must climb, a kinetic quantity. A reaction can be extremely exothermic yet very slow if $E_a$ is large (e.g., gasoline is stable in air until a spark supplies the activation energy). $\Delta H$ and $E_a$ are independent.

**Answer:** False — speed is set by $E_a$ (kinetics), not by $\Delta H$ (thermodynamics).

</details>

---

## Quick Reference

| Concept | Key idea / formula |
|---|---|
| **Collision theory** | Reaction needs a collision with **energy $\ge E_a$** *and* **correct orientation** |
| **Activation energy $E_a$** | Height of the energy hump; reactants → transition state |
| **Transition state** | Least-stable species at the **peak** (activated complex) |
| **$\Delta H$** | $E_{\text{products}} - E_{\text{reactants}}$ (plateau to plateau) |
| **Exothermic** | products lower, $\Delta H < 0$ |
| **Endothermic** | products higher, $\Delta H > 0$ |
| **Reverse barrier** | $E_{a,\text{rev}} = E_{a,\text{fwd}} - \Delta H$ |
| **Why heat speeds rate** | ↑ fraction of molecules with $KE \ge E_a$ (Maxwell–Boltzmann tail grows) |
| **Arrhenius** | $k = Ae^{-E_a/RT}$ — ↑$E_a$ → ↓$k$; ↑$T$ → ↑$k$ |
| **Frequency factor $A$** | collision frequency × orientation factor |
| **Linear form** | $\ln k = \ln A - \dfrac{E_a}{R}\cdot\dfrac{1}{T}$ |
| **Arrhenius plot** | $\ln k$ vs. $1/T$; slope $= -E_a/R$, so $E_a = -R(\text{slope})$ |
| **Two-point form** | $\ln\dfrac{k_2}{k_1} = -\dfrac{E_a}{R}\left(\dfrac{1}{T_2}-\dfrac{1}{T_1}\right)$ |
| **Constants** | $R = 8.314\ \text{J mol}^{-1}\text{K}^{-1}$; use **kelvin**, $E_a$ in **J/mol** |
| **Four rate factors** | concentration, temperature, surface area, catalyst |
| **Catalyst** | lowers $E_a$ (new pathway); **does not** change $\Delta H$ |

---

<div align="center">

[← Integrated Rate Laws](/chemistry/0703-integrated-rate-laws) | [Reaction Mechanisms →](/chemistry/0705-reaction-mechanisms)

</div>
