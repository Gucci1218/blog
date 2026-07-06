# Titration Curves
<p class="article-date">July 5, 2026</p>

*There's a trail at Torrey Pines that runs along the top of a ridge, and the first time I hiked it I remember thinking it was almost boring — you walk and walk and the ground barely tilts, flat dirt for a long stretch, the ocean somewhere off to your right. And then, without much warning, the trail reaches the edge and the whole world DROPS: a sheer sandstone cliff falling straight down to the beach, a huge change in a few steps. Scramble down and within moments you're on flat sand again, level as the ridge you started on. That shape — long flat, sudden vertical plunge, flat again — is EXACTLY the shape of a titration curve. As you add base to an acid, the pH creeps along nearly flat for a long time, then rockets almost straight up in a near-vertical jump, then flattens out. This is AP Unit 8, Topic 8.10 — the Unit 8 capstone — and learning to read that cliff tells you the equivalence point and, secretly, the acid's pKa.*

---

## What You'll Learn

- Read the general shape of a **pH-vs-volume-of-titrant** curve and connect each region to the flat-trail-and-cliff picture
- Distinguish the **equivalence point** (moles acid = moles base, the steep midpoint) from the **endpoint** (the indicator's color flip)
- Compute pH at all four stages of a **strong acid–strong base** titration and explain why its equivalence pH is exactly $7$
- Compute pH at all five stages of a **weak acid–strong base** titration: initial ICE, buffer region, half-equivalence, equivalence, and past equivalence
- Use the **half-equivalence point** shortcut ($\text{pH} = \text{p}K_a$) to read a weak acid's $\text{p}K_a$ straight off the graph
- Explain and calculate why a **weak-acid equivalence pH is above $7$** using a conjugate-base hydrolysis ICE
- Sketch and interpret a **weak base–strong acid** curve (the mirror image, equivalence pH below $7$)
- **Select an indicator** whose color-change range brackets the equivalence pH, and explain why the wrong one causes error
- Identify **polyprotic** curves — one cliff (and one $\text{p}K_a$) per acidic proton

---

## Prerequisites

- [Buffers](/chemistry/1004-buffers) — the long flat stretch before the cliff *is* a buffer; you'll use **Henderson–Hasselbalch** ($\text{pH} = \text{p}K_a + \log\frac{[\text{A}^-]}{[\text{HA}]}$) to compute pH all through the buffer region
- [Titration](/chemistry/0604-titration) — the mechanics (buret, titrant, analyte) and the mole-ratio stoichiometry; this article adds the pH story to the lab you already know, and finally answers "why *that* indicator?"
- [Weak Acids and Bases](/chemistry/1002-weak-acids-and-bases) — you must be fluent with $K_a$, $K_b$, $\text{p}K_a = -\log K_a$, and the ICE-table method for a weak acid or a hydrolyzing conjugate base

---

## The Core Concept

### Intuition First

Stand at the start of that Torrey Pines ridge trail and let's name what happens as you walk, because every part maps onto adding base to an acid.

| On the trail | On the titration curve | What's happening |
|---|---|---|
| the long flat approach | the slow, gradual pH change (**buffer region**) | added base is being "soaked up" — pH barely moves |
| the halfway ledge before the edge | the **half-equivalence point** | exactly half the acid is neutralized; here $\text{pH} = \text{p}K_a$ |
| the sudden sheer cliff | the **equivalence point** | the last bit of acid is gone; one drop swings pH enormously |
| the midpoint of the cliff face | the **equivalence pH** | the pH value at the steepest, center point of the jump |
| flat sand at the bottom | leveling off past equivalence | now you're just adding excess base into lots of solution |

Here's the physical reason for the flatness. In the buffer region, the flask holds a mixture of a weak acid $\ce{HA}$ and its conjugate base $\ce{A^-}$. Every drop of $\ce{OH^-}$ you add just converts a little more $\ce{HA}$ into $\ce{A^-}$; the solution *resists* pH change because it has a reservoir of both partners. That's the flat ridge — plenty of ground under your feet.

Now think about what happens right at the edge. Once you've converted essentially *all* the $\ce{HA}$ to $\ce{A^-}$, there's nothing left to soak up the next drop of base. The buffer reservoir is empty. So each additional drop of $\ce{OH^-}$ has an outsized effect, and the pH shoots up almost vertically — the cliff. A tiny change in volume produces a huge change in pH. That steepness is not a flaw; it's the whole reason titration works. The cliff is so sharp that "one drop" reliably marks the equivalence point.

And the sneaky bonus: **the halfway ledge tells you the acid's identity for free.** At the exact halfway point of neutralization, you've converted half the $\ce{HA}$ to $\ce{A^-}$, so $[\ce{HA}] = [\ce{A^-}]$. Plug that into Henderson–Hasselbalch and the log term is $\log 1 = 0$, leaving $\text{pH} = \text{p}K_a$. Read the pH at half the equivalence volume and you've read the $\text{p}K_a$ right off the graph.

### The Anatomy of a Weak Acid–Strong Base Curve (in ASCII)

```
 pH
 14 |
    |                                   _____________  excess strong base
    |                                 /                (flat sand at the bottom
 11 |                                |                  of the cliff)
    |                                |
    |            EQUIVALENCE POINT →  •  <- equivalence pH (> 7 here!)
  8 |- - - - - - - - - - - - - - - -|- - - - - -   the CLIFF: near-vertical
  7 |- - - - - - - - - - - - - - - -|              jump; midpoint = equiv pH
    |                              /
    |     half-eq ledge          |
  5 |- - - - - - - -•___________/   <- pH = pKa here (buffer region = flat ridge)
    |            __/
  3 |  initial  /
    |_________/________________________________________  mL of base added
    0        Ve/2                Ve
       (buffer / flat ridge)  (equivalence / the cliff)
```

Four things to notice, because AP will test all four:

1. **The initial point** sits well above where a strong acid would start — a weak acid only partially ionizes, so its pH is higher (less acidic) to begin with.
2. **The buffer region** is the long, gentle, nearly flat ramp. Its midpoint (at half the equivalence volume) reads $\text{pH} = \text{p}K_a$.
3. **The equivalence point** is the middle of the steep jump, NOT where the curve crosses pH 7. For a weak acid it lands **above 7**.
4. **Past equivalence** the curve flattens again as you drown the solution in excess strong base.

### Equivalence Point vs. Endpoint (the distinction from Unit 4)

Back in [Titration](/chemistry/0604-titration) we split these two hairs, and the curve finally shows why it matters:

- The **equivalence point** is the *stoichiometric fact*: moles of added base equal moles of acid (scaled by the mole ratio). On the curve it's the steep midpoint of the cliff. It is invisible — you can't see moles.
- The **endpoint** is what you *observe*: an indicator flipping color. You choose an indicator so that the color flip happens as close to the equivalence point as possible.

The cliff is so steep that a well-chosen indicator changes color within a fraction of a drop of the true equivalence volume, so we treat the endpoint volume as the equivalence volume. Pick a bad indicator and the endpoint lands off the cliff — that's **titration error**.

### The Universal Two-Step: Stoichiometry, THEN Equilibrium

Every point on every acid–base titration curve is computed the same way. Do these two moves in this order and you cannot get lost:

1. **Stoichiometry first (a limiting-reactant problem).** Convert both species to *moles* (or millimoles), run the neutralization $\ce{HA + OH^- -> A^- + H2O}$ to completion, and see what's left standing.
2. **Equilibrium second (whatever the leftovers demand).** Depending on what remains after step 1, do the matching pH calculation:

| What's left after the stoichiometry | pH method |
|---|---|
| only weak acid $\ce{HA}$ (initial point) | weak-acid **ICE** with $K_a$ |
| a mix of $\ce{HA}$ **and** $\ce{A^-}$ (buffer region) | **Henderson–Hasselbalch** |
| only conjugate base $\ce{A^-}$ (equivalence) | weak-**base** ICE with $K_b = \frac{K_w}{K_a}$ |
| excess strong base $\ce{OH^-}$ (past equivalence) | $[\ce{OH^-}]$ directly $\to$ pOH $\to$ pH |
| excess strong acid $\ce{H^+}$ (strong–strong, before equiv) | $[\ce{H^+}]$ directly $\to$ pH |

Memorize the shape of that table and titration curves stop being scary — they're just five easy sub-problems wearing a trench coat.

---

## Worked Examples

### Example 1: Strong Acid–Strong Base — All Four Stages

**Problem:** $25.0\ \text{mL}$ of $0.100\ \text{M}\ \ce{HCl}$ is titrated with $0.100\ \text{M}\ \ce{NaOH}$. Find the pH (a) initially, (b) after $10.0\ \text{mL}$ base, (c) at equivalence, and (d) after $30.0\ \text{mL}$ base.

**Solution:**

Initial moles of acid: $0.0250\ \text{L} \times 0.100\ \text{M} = 2.50\ \text{mmol}\ \ce{HCl}$.

**Step 1 — (a) Initial.** $\ce{HCl}$ is a strong acid, fully ionized, so $[\ce{H+}] = 0.100\ \text{M}$.
$$\text{pH} = -\log(0.100) = 1.00$$

**Step 2 — (b) Before equivalence (excess strong acid).** Add $10.0\ \text{mL} \times 0.100\ \text{M} = 1.00\ \text{mmol}\ \ce{OH^-}$. It neutralizes $1.00\ \text{mmol}$ of acid, leaving $2.50 - 1.00 = 1.50\ \text{mmol}\ \ce{H+}$ in a total volume of $25.0 + 10.0 = 35.0\ \text{mL}$.
$$[\ce{H+}] = \frac{1.50\ \text{mmol}}{35.0\ \text{mL}} = 0.0429\ \text{M} \quad\Rightarrow\quad \text{pH} = -\log(0.0429) = 1.37$$

**Step 3 — (c) At equivalence.** Equal moles of strong acid and strong base react completely to give only $\ce{NaCl}$ and water. $\ce{Na+}$ and $\ce{Cl-}$ don't affect pH.
$$\text{pH} = 7.00$$

**Step 4 — (d) After equivalence (excess strong base).** Add $30.0\ \text{mL} \times 0.100\ \text{M} = 3.00\ \text{mmol}\ \ce{OH^-}$. Excess $= 3.00 - 2.50 = 0.50\ \text{mmol}$ in $25.0 + 30.0 = 55.0\ \text{mL}$.
$$[\ce{OH^-}] = \frac{0.50}{55.0} = 0.00909\ \text{M} \Rightarrow \text{pOH} = 2.04 \Rightarrow \text{pH} = 11.96$$

**Answer:** pH $= 1.00,\ 1.37,\ 7.00,\ 11.96$. Notice how little the pH moves early (the flat ridge) and how far it leaps across the equivalence point.

---

### Example 2: Weak Acid–Strong Base — The Full Five-Stage Calculation

**Problem:** $25.0\ \text{mL}$ of $0.100\ \text{M}$ acetic acid ($\ce{CH3COOH}$, $K_a = 1.8\times10^{-5}$) is titrated with $0.100\ \text{M}\ \ce{NaOH}$. Find the pH (a) initially, (b) after $10.0\ \text{mL}$, (c) at half-equivalence, (d) at equivalence, (e) after $35.0\ \text{mL}$.

**Solution:** Initial acid $= 0.0250\ \text{L}\times 0.100 = 2.50\ \text{mmol}$; equivalence needs $2.50\ \text{mmol}\ \ce{OH^-} = 25.0\ \text{mL}$. Note $\text{p}K_a = -\log(1.8\times10^{-5}) = 4.74$.

**(a) Initial — weak-acid ICE.** Nothing added; solve $\ce{CH3COOH <=> H+ + CH3COO^-}$:
$$[\ce{H+}] = \sqrt{K_a\,C} = \sqrt{(1.8\times10^{-5})(0.100)} = 1.34\times10^{-3}\ \text{M} \Rightarrow \text{pH} = 2.87$$

**(b) Buffer region ($10.0\ \text{mL}$) — Henderson–Hasselbalch.** Add $1.00\ \text{mmol}\ \ce{OH^-}$; it converts $1.00\ \text{mmol}$ acid to acetate. Left: $\ce{HA} = 1.50\ \text{mmol}$, $\ce{A^-} = 1.00\ \text{mmol}$.
$$\text{pH} = \text{p}K_a + \log\frac{[\ce{A^-}]}{[\ce{HA}]} = 4.74 + \log\frac{1.00}{1.50} = 4.74 - 0.18 = 4.57$$
(The volumes cancel in the ratio, so you can use millimoles directly — a huge time-saver.)

**(c) Half-equivalence ($12.5\ \text{mL}$) — the shortcut.** Half the acid ($1.25\ \text{mmol}$) is now acetate, half ($1.25\ \text{mmol}$) is still acid, so $[\ce{HA}] = [\ce{A^-}]$:
$$\text{pH} = \text{p}K_a + \log(1) = \text{p}K_a = 4.74$$

**(d) Equivalence ($25.0\ \text{mL}$) — weak-BASE ICE (the signature AP calc).** All $2.50\ \text{mmol}$ acid is now acetate in $50.0\ \text{mL}$: $[\ce{CH3COO^-}] = 2.50/50.0 = 0.0500\ \text{M}$. Acetate is a weak base that hydrolyzes: $\ce{CH3COO^- + H2O <=> CH3COOH + OH^-}$ with
$$K_b = \frac{K_w}{K_a} = \frac{1.0\times10^{-14}}{1.8\times10^{-5}} = 5.6\times10^{-10}$$
$$[\ce{OH^-}] = \sqrt{K_b\,C} = \sqrt{(5.6\times10^{-10})(0.0500)} = 5.3\times10^{-6}\ \text{M} \Rightarrow \text{pOH} = 5.28 \Rightarrow \text{pH} = 8.72$$

**(e) Past equivalence ($35.0\ \text{mL}$) — excess strong base.** Total base $= 3.50\ \text{mmol}$; excess $= 3.50 - 2.50 = 1.00\ \text{mmol}$ in $60.0\ \text{mL}$.
$$[\ce{OH^-}] = \frac{1.00}{60.0} = 0.0167\ \text{M} \Rightarrow \text{pOH} = 1.78 \Rightarrow \text{pH} = 12.22$$

**Answer:** pH $= 2.87,\ 4.57,\ 4.74,\ 8.72,\ 12.22$. The equivalence pH is **8.72 — above 7 — because the conjugate base makes the solution basic.**

---

### Example 3: Reading $\text{p}K_a$ Straight Off the Graph

**Problem:** A $0.100\ \text{M}$ solution of an unknown monoprotic weak acid is titrated with strong base. The curve shows a steep jump centered at $20.0\ \text{mL}$, and at $10.0\ \text{mL}$ the pH reads $3.75$. Find $K_a$ and identify the likely acid.

**Solution:**

**Step 1 — Locate half-equivalence.** The equivalence volume is $20.0\ \text{mL}$, so half-equivalence is at $10.0\ \text{mL}$.

**Step 2 — Read pKa.** At half-equivalence $\text{pH} = \text{p}K_a$, so $\text{p}K_a = 3.75$.

**Step 3 — Convert to $K_a$.** $K_a = 10^{-3.75} = 1.8\times10^{-4}$.

**Answer:** $K_a \approx 1.8\times10^{-4}$, which matches **formic acid** ($\ce{HCOOH}$). No ICE table needed — the graph handed us $\text{p}K_a$ for free.

---

### Example 4: Why Equivalence pH > 7 — A Standalone Hydrolysis ICE

**Problem:** $40.0\ \text{mL}$ of $0.100\ \text{M}\ \ce{HF}$ ($K_a = 6.8\times10^{-4}$) is titrated to the equivalence point with $0.100\ \text{M}\ \ce{NaOH}$. Find the equivalence pH.

**Solution:**

**Step 1 — Stoichiometry.** Moles $\ce{HF} = 4.00\ \text{mmol}$, requiring $40.0\ \text{mL}$ of base. At equivalence all of it is fluoride, $\ce{F^-} = 4.00\ \text{mmol}$ in $80.0\ \text{mL}$: $[\ce{F^-}] = 0.0500\ \text{M}$.

**Step 2 — Equilibrium (weak-base ICE).** $\ce{F^- + H2O <=> HF + OH^-}$, $K_b = \frac{1.0\times10^{-14}}{6.8\times10^{-4}} = 1.5\times10^{-11}$.
$$[\ce{OH^-}] = \sqrt{(1.5\times10^{-11})(0.0500)} = 8.6\times10^{-7}\ \text{M} \Rightarrow \text{pOH} = 6.07 \Rightarrow \text{pH} = 7.93$$

**Answer:** pH $= 7.93$. It's above 7 — even a fairly "strong" weak acid leaves a conjugate base that nudges the equivalence point basic. **A weak acid can NEVER have an equivalence pH of exactly 7.**

---

### Example 5: Weak Base–Strong Acid — The Mirror Image

**Problem:** $25.0\ \text{mL}$ of $0.100\ \text{M}$ ammonia ($\ce{NH3}$, $K_b = 1.8\times10^{-5}$) is titrated with $0.100\ \text{M}\ \ce{HCl}$. Find the equivalence pH.

**Solution:**

**Step 1 — Stoichiometry.** $\ce{NH3} = 2.50\ \text{mmol}$, neutralized by $25.0\ \text{mL}$ acid to give ammonium, $\ce{NH4+} = 2.50\ \text{mmol}$ in $50.0\ \text{mL}$: $[\ce{NH4+}] = 0.0500\ \text{M}$.

**Step 2 — Equilibrium (weak-ACID ICE).** $\ce{NH4+ <=> NH3 + H+}$, $K_a = \frac{1.0\times10^{-14}}{1.8\times10^{-5}} = 5.6\times10^{-10}$.
$$[\ce{H+}] = \sqrt{(5.6\times10^{-10})(0.0500)} = 5.3\times10^{-6}\ \text{M} \Rightarrow \text{pH} = 5.28$$

**Answer:** pH $= 5.28$. This whole curve is the flat-trail-and-cliff picture flipped upside down: pH starts high, steps *down* through a buffer region, and the equivalence point lands **below 7** because ammonium is a weak acid.

---

### Example 6: Choosing the Right Indicator

**Problem:** For the acetic acid–NaOH titration in Example 2 (equivalence pH $= 8.72$), which indicator is appropriate: methyl orange (flips over pH $3.1$–$4.4$) or phenolphthalein (flips over pH $8.2$–$10.0$)? What goes wrong with the other one?

**Solution:**

**Step 1 — Recall the rule.** The indicator's color-change range must *bracket* the equivalence pH so the endpoint lands on the cliff.

**Step 2 — Test each.** The equivalence pH is $8.72$. Phenolphthalein flips over $8.2$–$10.0$, which contains $8.72$ — it changes color right on the steep part. Methyl orange flips over $3.1$–$4.4$, which is way down in the *buffer region*, long before the cliff.

**Step 3 — The consequence.** Methyl orange would change color when you've added only a fraction of the base needed — a big **titration error** (you'd stop far short of equivalence).

**Answer:** Use **phenolphthalein**. (General rule of thumb: weak acid–strong base $\to$ phenolphthalein; strong acid–weak base $\to$ methyl orange; strong–strong $\to$ either works, because the cliff spans pH $\sim3$ to $\sim11$.)

---

### Example 7: Interpreting an Unlabeled Curve

**Problem:** Two curves each start at $25.0\ \text{mL}$ of a $0.100\ \text{M}$ acid and are titrated with $0.100\ \text{M}\ \ce{NaOH}$. Curve A starts at pH $1.0$ and its jump is centered at pH $7$. Curve B starts at pH $2.9$, has a flat buffer shelf, and its jump is centered at pH $\approx 8.7$. Which is the strong acid, and what is Curve B's $\text{p}K_a$ if its shelf midpoint is at pH $4.7$?

**Solution:**

**Step 1 — Compare starting points.** A strong acid is fully ionized, so it starts lower (pH $1.0$). Curve A is the strong acid; Curve B (higher initial pH, gentler start) is the weak acid.

**Step 2 — Compare equivalence pH.** Curve A crosses at pH $7$ (strong–strong). Curve B tops its cliff near $8.7$ (weak acid $\to$ basic salt) — consistent.

**Step 3 — Read pKa.** Curve B's buffer shelf midpoint (half-equivalence) is at pH $4.7$, so $\text{p}K_a = 4.7$.

**Answer:** Curve A is the strong acid; Curve B is the weak acid with $\text{p}K_a \approx 4.7$ (acetic acid). The tell-tale signs of the weak acid: a higher starting pH, a flat buffer shelf, a *shorter* cliff, and an equivalence pH above 7.

---

### Example 8: How the Cliff Distinguishes Weak from Strong

**Problem:** Explain, using the curve shape only, two features that reveal whether the acid being titrated is weak or strong.

**Solution:**

1. **The buffer shelf.** A weak acid produces a long, flat region *before* the cliff (a mix of $\ce{HA}$ and $\ce{A^-}$ resisting change). A strong acid has no buffer region — its pH rises slowly but steadily with no flat shelf.
2. **The height and center of the cliff.** A strong-acid cliff is enormous (pH $\sim3 \to \sim11$) and centered on pH $7$. A weak-acid cliff is shorter and centered *above* 7. The weaker the acid, the shorter the cliff and the higher its center — very weak acids give a jump so small it's hard to see.

**Answer:** Look for (1) a flat buffer shelf and (2) an equivalence pH above 7 — both mean a weak acid. A tall cliff centered exactly at 7 with no shelf means a strong acid.

---

### Example 9: A Polyprotic Curve — One Cliff per Proton

**Problem:** Phosphoric acid $\ce{H3PO4}$ has $\text{p}K_{a1} = 2.15$, $\text{p}K_{a2} = 7.20$, $\text{p}K_{a3} = 12.35$. Sketch the shape of its titration with strong base and give the pH at the first two half-equivalence points.

**Solution:**

**Step 1 — Count protons.** Three acidic protons means the acid is neutralized in three steps: $\ce{H3PO4 -> H2PO4^- -> HPO4^2- -> PO4^3-}$. Each step is its own mini-titration with its own buffer region and its own cliff.

**Step 2 — Read the half-equivalence pHs.** At the first half-equivalence point, $[\ce{H3PO4}] = [\ce{H2PO4^-}]$, so $\text{pH} = \text{p}K_{a1} = 2.15$. At the second, $[\ce{H2PO4^-}] = [\ce{HPO4^2-}]$, so $\text{pH} = \text{p}K_{a2} = 7.20$.

**Step 3 — Sketch.** The curve climbs to a first cliff (near the first equivalence volume $V_e$), levels into a second buffer shelf, climbs a second cliff (near $2V_e$), and so on. The third proton ($\text{p}K_{a3} = 12.35$) is so weak its cliff is barely visible in water.

```
 pH
    |                         ______
    |                       _/  <- 2nd cliff (2nd equivalence)
    |          buffer 2 ___/
    |       ___________/  <- pH = pKa2 = 7.20 at 2nd half-eq
    |  ____/  <- 1st cliff (1st equivalence)
    | /  <- pH = pKa1 = 2.15 at 1st half-eq
    |/_______________________________  mL base
    0     Ve         2·Ve
```

**Answer:** Two clear cliffs; half-equivalence pHs of **2.15 and 7.20**. Each proton has its own $\text{p}K_a$ and its own cliff — count the cliffs to count the acidic protons.

---

### Example 10: Finding Concentration From the Equivalence Volume

**Problem:** It takes $18.5\ \text{mL}$ of $0.150\ \text{M}\ \ce{NaOH}$ to reach the equivalence point when titrating $25.0\ \text{mL}$ of a monoprotic weak acid. What is the acid's concentration?

**Solution:**

**Step 1 — Moles of base at equivalence.** $0.0185\ \text{L}\times 0.150\ \text{M} = 2.78\times10^{-3}\ \text{mol}\ \ce{OH^-}$.

**Step 2 — Mole ratio.** Monoprotic, 1:1, so moles of acid $= 2.78\times10^{-3}\ \text{mol}$.

**Step 3 — Divide by volume.** $[\ce{HA}] = \dfrac{2.78\times10^{-3}\ \text{mol}}{0.0250\ \text{L}} = 0.111\ \text{M}$.

**Answer:** $0.111\ \text{M}$. The equivalence *volume* gives concentration by pure stoichiometry — the same engine as [Titration](/chemistry/0604-titration); the pH curve just tells you *where* equivalence is.

---

### Example 11: Buffer-Region pH Without Recomputing Everything

**Problem:** During a weak-acid titration ($K_a = 1.8\times10^{-5}$), you've added enough base to convert $30\%$ of the acid to its conjugate base. What is the pH?

**Solution:**

**Step 1 — Set up the ratio.** If $30\%$ is converted, then $[\ce{A^-}] = 0.30$ (relative) and $[\ce{HA}] = 0.70$.

**Step 2 — Henderson–Hasselbalch.** $\text{p}K_a = 4.74$.
$$\text{pH} = 4.74 + \log\frac{0.30}{0.70} = 4.74 + \log(0.429) = 4.74 - 0.37 = 4.37$$

**Answer:** pH $= 4.37$. Anywhere in the buffer region you only need the *ratio* of conjugate base to acid — a fast move for FRQs that don't give you nice round volumes.

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Calling the equivalence point "pH 7" for a weak acid | Confusing equivalence with neutrality | Equivalence pH $= 7$ **only** for strong–strong; weak acid $\to$ **above 7**, weak base $\to$ **below 7** |
| Doing equilibrium before stoichiometry | Jumping straight to $K_a$ | ALWAYS run the neutralization to completion first, then see what's left and pick the matching pH method |
| Using $K_a$ at the equivalence point of a weak acid | Forgetting the leftover is a *base* | At equivalence only $\ce{A^-}$ remains — use $K_b = K_w/K_a$ in a base ICE |
| Reading $\text{p}K_a$ at the equivalence point | Mixing up half-equivalence and equivalence | $\text{pH} = \text{p}K_a$ at **half**-equivalence (half the volume of the cliff), not at the cliff itself |
| Forgetting the total volume grows | Dividing moles by the original volume | Always add titrant volume to analyte volume before finding a concentration |
| Picking an indicator by habit | Not matching to equivalence pH | The color-change range must **bracket** the equivalence pH; weak acid–strong base $\to$ phenolphthalein |
| Treating a polyprotic curve as one step | Overlooking multiple protons | Count the cliffs — one per acidic proton, each with its own $\text{p}K_a$ |
| Using Henderson–Hasselbalch at the initial or equivalence point | Applying it everywhere | H–H only works in the **buffer region**, where both $\ce{HA}$ and $\ce{A^-}$ are present |

---

## AP Exam Tips

- **A titration-curve FRQ is basically guaranteed** and worth a lot of points — this is one of the highest-yield topics in Unit 8. Learn to move fluently between the graph and the calculation.
- **Half-equivalence is a free $\text{p}K_a$.** If a question gives you a curve, the fastest way to $K_a$ is: find the equivalence volume, halve it, read the pH there — that pH *is* $\text{p}K_a$. No ICE table.
- **Weak-acid equivalence pH is greater than 7, every time.** Graders love this. Be ready to justify it: the only species left is the conjugate base, which hydrolyzes ($\ce{A^- + H2O <=> HA + OH^-}$) and makes the solution basic. Then back it with a $K_b$ ICE.
- **Stoichiometry before equilibrium, at every single stage.** Write the neutralization, find the limiting reactant, and only *then* choose your pH tool. This one discipline prevents most errors.
- **The indicator must bracket the equivalence pH.** State the equivalence pH, then name an indicator whose range contains it, then explain that a mismatched indicator changes color off the cliff and causes titration error (endpoint $\ne$ equivalence).
- **Polyprotic = one cliff per proton.** Count cliffs to count acidic protons; each half-equivalence gives that proton's $\text{p}K_a$.
- **In the buffer region, use millimoles or ratios directly** in Henderson–Hasselbalch — the volumes cancel, saving you time.
- **Sketching:** for a weak acid–strong base curve, draw a higher-than-strong initial point, a flat buffer shelf, a *shorter* cliff centered above 7, then a level tail. Label half-equivalence ($\text{pH} = \text{p}K_a$) and equivalence.

---

## Practice Problems

### Problem 1
$50.0\ \text{mL}$ of $0.200\ \text{M}\ \ce{HNO3}$ is titrated with $0.200\ \text{M}\ \ce{KOH}$. What is the initial pH?

<details>
<summary><strong>Solution</strong></summary>

$\ce{HNO3}$ is a strong acid, fully ionized: $[\ce{H+}] = 0.200\ \text{M}$.
$$\text{pH} = -\log(0.200) = 0.70$$

**Answer: pH $= 0.70$.**

</details>

---

### Problem 2
For the titration in Problem 1, what is the pH after $20.0\ \text{mL}$ of base is added?

<details>
<summary><strong>Solution</strong></summary>

Acid: $50.0\times0.200 = 10.0\ \text{mmol}$. Base added: $20.0\times0.200 = 4.00\ \text{mmol}$. Excess acid $= 10.0 - 4.00 = 6.00\ \text{mmol}$ in $70.0\ \text{mL}$.
$$[\ce{H+}] = \frac{6.00}{70.0} = 0.0857\ \text{M} \Rightarrow \text{pH} = -\log(0.0857) = 1.07$$

**Answer: pH $= 1.07$.**

</details>

---

### Problem 3
For Problem 1, what is the pH at the equivalence point, and what volume of base is needed to reach it?

<details>
<summary><strong>Solution</strong></summary>

Equivalence needs $10.0\ \text{mmol}\ \ce{OH^-}$: $V = 10.0\ \text{mmol}/0.200\ \text{M} = 50.0\ \text{mL}$. Strong acid + strong base gives a neutral salt ($\ce{KNO3}$).

**Answer: $50.0\ \text{mL}$ of base; pH $= 7.00$.**

</details>

---

### Problem 4
For Problem 1, find the pH after $60.0\ \text{mL}$ of base has been added.

<details>
<summary><strong>Solution</strong></summary>

Base $= 60.0\times0.200 = 12.0\ \text{mmol}$. Excess $\ce{OH^-} = 12.0 - 10.0 = 2.00\ \text{mmol}$ in $50.0 + 60.0 = 110.0\ \text{mL}$.
$$[\ce{OH^-}] = \frac{2.00}{110.0} = 0.0182\ \text{M} \Rightarrow \text{pOH} = 1.74 \Rightarrow \text{pH} = 12.26$$

**Answer: pH $= 12.26$.**

</details>

---

### Problem 5
$25.0\ \text{mL}$ of $0.100\ \text{M}$ propanoic acid ($K_a = 1.3\times10^{-5}$) is titrated with $0.100\ \text{M}\ \ce{NaOH}$. What is the initial pH?

<details>
<summary><strong>Solution</strong></summary>

Weak-acid ICE: $[\ce{H+}] = \sqrt{K_a\,C} = \sqrt{(1.3\times10^{-5})(0.100)} = \sqrt{1.3\times10^{-6}} = 1.14\times10^{-3}\ \text{M}$.
$$\text{pH} = -\log(1.14\times10^{-3}) = 2.94$$

**Answer: pH $= 2.94$.**

</details>

---

### Problem 6
For the propanoic acid titration in Problem 5, what is the pH at the half-equivalence point?

<details>
<summary><strong>Solution</strong></summary>

At half-equivalence $[\ce{HA}] = [\ce{A^-}]$, so $\text{pH} = \text{p}K_a$.
$$\text{p}K_a = -\log(1.3\times10^{-5}) = 4.89$$

**Answer: pH $= 4.89$.**

</details>

---

### Problem 7
For Problem 5, what is the pH after $15.0\ \text{mL}$ of $\ce{NaOH}$ is added?

<details>
<summary><strong>Solution</strong></summary>

Acid $= 2.50\ \text{mmol}$; equivalence at $25.0\ \text{mL}$, so $15.0\ \text{mL}$ is in the buffer region. Base added $= 1.50\ \text{mmol}$: converts $1.50\ \text{mmol}$ acid to conjugate base. Left: $\ce{HA} = 1.00\ \text{mmol}$, $\ce{A^-} = 1.50\ \text{mmol}$.
$$\text{pH} = 4.89 + \log\frac{1.50}{1.00} = 4.89 + 0.18 = 5.07$$

**Answer: pH $= 5.07$.**

</details>

---

### Problem 8
For Problem 5, find the pH at the equivalence point.

<details>
<summary><strong>Solution</strong></summary>

At equivalence all $2.50\ \text{mmol}$ is propanoate in $50.0\ \text{mL}$: $C = 0.0500\ \text{M}$. This conjugate base hydrolyzes; $K_b = \frac{1.0\times10^{-14}}{1.3\times10^{-5}} = 7.7\times10^{-10}$.
$$[\ce{OH^-}] = \sqrt{(7.7\times10^{-10})(0.0500)} = 6.2\times10^{-6}\ \text{M} \Rightarrow \text{pOH} = 5.21 \Rightarrow \text{pH} = 8.79$$

**Answer: pH $= 8.79$ (above 7, as expected for a weak acid).**

</details>

---

### Problem 9
A monoprotic weak acid is titrated with strong base. The pH at the equivalence point is $9.0$ and at half-equivalence it is $5.3$. Estimate $K_a$ and state whether phenolphthalein (range $8.2$–$10.0$) is a good indicator.

<details>
<summary><strong>Solution</strong></summary>

At half-equivalence $\text{pH} = \text{p}K_a = 5.3$, so $K_a = 10^{-5.3} = 5\times10^{-6}$. The equivalence pH is $9.0$, which falls inside phenolphthalein's range ($8.2$–$10.0$), so it changes color right on the cliff.

**Answer: $K_a \approx 5\times10^{-6}$; yes, phenolphthalein is appropriate.**

</details>

---

### Problem 10
$30.0\ \text{mL}$ of $0.100\ \text{M}$ methylamine ($\ce{CH3NH2}$, $K_b = 4.4\times10^{-4}$) is titrated with $0.100\ \text{M}\ \ce{HCl}$. What is the pH at the equivalence point, and is it above or below 7?

<details>
<summary><strong>Solution</strong></summary>

At equivalence all base is converted to $\ce{CH3NH3+}$: $3.00\ \text{mmol}$ in $60.0\ \text{mL}$ $= 0.0500\ \text{M}$. It's a weak acid; $K_a = \frac{1.0\times10^{-14}}{4.4\times10^{-4}} = 2.3\times10^{-11}$.
$$[\ce{H+}] = \sqrt{(2.3\times10^{-11})(0.0500)} = 1.1\times10^{-6}\ \text{M} \Rightarrow \text{pH} = 5.98$$

**Answer: pH $\approx 5.96$–$5.98$, below 7 (weak base titrated by strong acid).**

</details>

---

### Problem 11
Sketch (describe) the curve for titrating a strong acid with a strong base, and explain why the "cliff" is taller than for a weak acid.

<details>
<summary><strong>Solution</strong></summary>

Start very low (e.g., pH $\sim1$), rise slowly and steadily with **no** flat buffer shelf, jump nearly vertically through pH $7$ at equivalence, then level off high (pH $\sim12$). The cliff is taller because a strong acid has a very low starting pH and a strong base pushes to a very high ending pH, with no conjugate pair to buffer either side — so the vertical jump spans roughly pH $3$ to $11$, versus a shorter, higher-centered jump for a weak acid.

**Answer: Tall symmetric jump centered on pH 7, no buffer shelf.**

</details>

---

### Problem 12
Carbonic acid $\ce{H2CO3}$ has $\text{p}K_{a1} = 6.35$ and $\text{p}K_{a2} = 10.33$. How many equivalence points appear on its titration curve with strong base, and what pH would you read at the first half-equivalence point?

<details>
<summary><strong>Solution</strong></summary>

$\ce{H2CO3}$ is diprotic, so there are **two** equivalence points (two cliffs), corresponding to $\ce{H2CO3 -> HCO3^- -> CO3^2-}$. At the first half-equivalence point $[\ce{H2CO3}] = [\ce{HCO3^-}]$, so $\text{pH} = \text{p}K_{a1} = 6.35$.

**Answer: Two equivalence points; first half-equivalence pH $= 6.35$.**

</details>

---

### Problem 13
Why can't you use methyl orange (range $3.1$–$4.4$) to detect the equivalence point of an acetic acid–NaOH titration (equivalence pH $\approx 8.7$)? What error results?

<details>
<summary><strong>Solution</strong></summary>

Methyl orange changes color at pH $3.1$–$4.4$, which is deep in the *buffer region*, long before the equivalence cliff at pH $8.7$. It would flip while much acid remains unreacted, so you'd stop far short of equivalence and report too small a base volume — a large titration error (endpoint $\ne$ equivalence).

**Answer: Its range is below the cliff; you'd stop early and underestimate the acid.**

</details>

---

### Problem 14
A $0.100\ \text{M}$ weak acid is titrated to a point where $\frac{2}{3}$ of it has been converted to conjugate base. If $\text{p}K_a = 4.20$, what is the pH?

<details>
<summary><strong>Solution</strong></summary>

$[\ce{A^-}] : [\ce{HA}] = 2 : 1$.
$$\text{pH} = 4.20 + \log\frac{2}{1} = 4.20 + 0.30 = 4.50$$

**Answer: pH $= 4.50$.**

</details>

---

### Problem 15
It takes exactly $22.4\ \text{mL}$ of $0.125\ \text{M}\ \ce{NaOH}$ to reach the equivalence point of $20.0\ \text{mL}$ of a monoprotic acid. If the half-equivalence pH is $3.90$, find the acid's molarity and its $K_a$.

<details>
<summary><strong>Solution</strong></summary>

Moles base at equivalence $= 0.0224\times0.125 = 2.80\times10^{-3}\ \text{mol}$; 1:1 ratio gives the same moles of acid. Molarity $= \frac{2.80\times10^{-3}}{0.0200} = 0.140\ \text{M}$. Half-equivalence pH $= \text{p}K_a = 3.90$, so $K_a = 10^{-3.90} = 1.3\times10^{-4}$.

**Answer: $[\ce{HA}] = 0.140\ \text{M}$; $K_a = 1.3\times10^{-4}$.**

</details>

---

## Quick Reference

| Stage of the curve | Trail picture | What's in the flask | pH method |
|---|---|---|---|
| Initial (weak acid) | start of flat ridge | only $\ce{HA}$ | weak-acid ICE, $[\ce{H+}] = \sqrt{K_a C}$ |
| Buffer region | the long flat ridge | $\ce{HA}$ + $\ce{A^-}$ | $\text{pH} = \text{p}K_a + \log\frac{[\ce{A^-}]}{[\ce{HA}]}$ |
| Half-equivalence | halfway ledge | $[\ce{HA}] = [\ce{A^-}]$ | $\text{pH} = \text{p}K_a$ |
| Equivalence (weak acid) | midpoint of the cliff | only $\ce{A^-}$ | weak-base ICE, $K_b = K_w/K_a$; **pH > 7** |
| Past equivalence | flat sand below | excess $\ce{OH^-}$ | $[\ce{OH^-}] \to \text{pOH} \to \text{pH}$ |

| Titration type | Equivalence pH | Best indicator |
|---|---|---|
| Strong acid–strong base | $= 7$ | phenolphthalein or methyl orange |
| Weak acid–strong base | $> 7$ | **phenolphthalein** |
| Strong acid–weak base | $< 7$ | **methyl orange** |

**Key equations**
$$\text{pH} = -\log[\ce{H+}] \qquad \text{pH} = \text{p}K_a + \log\frac{[\ce{A^-}]}{[\ce{HA}]} \qquad K_a K_b = K_w = 1.0\times10^{-14}$$

- **Golden rules:** stoichiometry *before* equilibrium at every stage; half-equivalence pH $= \text{p}K_a$; weak-acid equivalence pH $> 7$; count cliffs to count protons; the indicator range must bracket the equivalence pH.

---

<div align="center">

[← Buffers](/chemistry/1004-buffers) | [Entropy →](/chemistry/1101-entropy)

</div>
