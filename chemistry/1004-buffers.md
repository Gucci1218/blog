# Buffers
<p class="article-date">July 5, 2026</p>

*Right now, without you doing a single thing about it, your blood is sitting at a pH of about **7.4** — and it is not allowed to wander. Drop below 7.0 or climb above 7.8 for long and you are in a hospital, or worse. Yet think about what you put your body through: you eat acidic oranges, chug soda, and go for a run, and running literally dumps lactic acid straight into your bloodstream. Every one of those should crash your pH. It doesn't. It barely twitches. The reason is a **buffer** — a pair of dissolved molecules working as a chemical shock absorber, catching added acid or base and neutralizing it before it can move the pH. The pair in your blood is carbonic acid, $\ce{H2CO3}$, and bicarbonate, $\ce{HCO3-}$: the bicarbonate mops up any acid you throw at it, the carbonic acid mops up any base, and together they hold the line at 7.4. This article is about how that shock absorber works, how to build one, how to predict its pH with one clean equation, and how hard you can hit it before it finally gives out.*

---

## What You'll Learn

- Define a **buffer** as a solution containing comparable amounts of a **weak acid and its conjugate base** (or a weak base and its conjugate acid), and explain why that pairing is the whole point
- Write the **neutralization reactions** that happen when strong acid or strong base is added to a buffer, and see them as a **Le Chatelier** shift
- **Recognize** whether a given mixture is a buffer (and rule out mixtures that aren't)
- **Make** a buffer three ways: weak acid + its salt, partial neutralization of a weak acid, or weak base + its salt
- Derive and use the **Henderson-Hasselbalch equation**, $\text{pH} = \text{p}K_a + \log\frac{[\ce{A-}]}{[\ce{HA}]}$, to compute a buffer's pH
- Use the key insight $\text{pH} = \text{p}K_a$ **when the components are equal**, and use it to **choose** the right acid for a target pH
- Do the **stoichiometry first, then Henderson-Hasselbalch** to find the new pH after adding strong acid or base to a buffer
- Contrast the tiny pH change of a buffer with the huge change in pure water for the *same* addition
- Explain **buffer capacity**: what makes a buffer strong, why it works best within $\pm 1$ pH unit of $\text{p}K_a$, and what it means to "use up" a buffer

---

## Prerequisites

- [Weak Acids and Bases](/chemistry/1002-weak-acids-and-bases) — this is the big one. A buffer **is** a weak acid living next to its **conjugate base**, so you must already be fluent with $K_a$, $\text{p}K_a = -\log K_a$, and what a **conjugate acid-base pair** is ($\ce{HA}$ and $\ce{A-}$ differ by one proton). Every equation below is just $K_a$ rearranged.
- [Le Chatelier's Principle](/chemistry/0904-le-chatelier) — a buffer's resistance is Le Chatelier in action. The weak acid sits at equilibrium, $\ce{HA <=> H+ + A-}$; when you add $\ce{H+}$ or $\ce{OH-}$, the system **shifts to relieve the stress** and absorbs most of the change. If "shift left / shift right to undo a disturbance" isn't automatic yet, patch it here first.

---

## The Core Concept

### Intuition First

Let me stay with your bloodstream, because everything about buffers lives inside it.

Picture your blood as a room with **two kinds of workers** standing around, waiting. One crew, the **bicarbonate** ions $\ce{HCO3-}$, are trained to grab **acid**. The other crew, the **carbonic acid** molecules $\ce{H2CO3}$, are trained to grab **base**. As long as both crews are on the clock in decent numbers, the room's pH cannot move much, because whatever intruder walks in — acid *or* base — there is a crew standing by to tackle it.

Here's the map that made it click for me:

| In your bloodstream | In the chemistry |
|---|---|
| Bicarbonate $\ce{HCO3-}$, the crew that grabs acid | The **conjugate base** component, $\ce{A-}$ |
| Carbonic acid $\ce{H2CO3}$, the crew that grabs base | The **weak acid** component, $\ce{HA}$ |
| Both crews on the clock together | The **buffer** |
| A gulp of acidic soda | Added $\ce{H+}$ |
| The acid crew tackling it before pH moves | $\ce{HCO3- + H+ -> H2CO3}$ |
| How many intruders they can handle before losing control | **Buffer capacity** |

Now watch the two tackles. When you add **acid** (extra $\ce{H+}$), the bicarbonate crew grabs it:

$$\ce{HCO3- + H+ -> H2CO3}$$

The stray $\ce{H+}$ that *would* have lowered your pH is converted into plain weak carbonic acid, which barely ionizes. Crisis absorbed.

When you add **base** (extra $\ce{OH-}$), the carbonic acid crew grabs it:

$$\ce{H2CO3 + OH- -> HCO3- + H2O}$$

The $\ce{OH-}$ that *would* have raised your pH is turned into harmless water. Crisis absorbed again.

That two-sided coverage — a crew for acid *and* a crew for base — is why a buffer needs **both** the weak acid and its conjugate base present at the same time. Miss one crew and the room is only protected against one kind of intruder.

### The Le Chatelier framing

Why is a buffer so much more stubborn than plain water? Because the weak acid sits at equilibrium:

$$\ce{HA <=> H+ + A-}$$

When you dump in extra $\ce{H+}$, you've stressed the right side, so [Le Chatelier](/chemistry/0904-le-chatelier) says the reaction **shifts left** — the added $\ce{H+}$ combines with $\ce{A-}$ to remake $\ce{HA}$, swallowing most of the disturbance. When you dump in $\ce{OH-}$, it pulls $\ce{H+}$ out of solution (making water), the stress is on the left, and the reaction **shifts right** to replace the lost $\ce{H+}$. Either way the system fights the change. A buffer is just Le Chatelier with a big reservoir of both $\ce{HA}$ and $\ce{A-}$ on hand to do the shifting.

### What actually makes a buffer

A buffer is a solution that contains, in **comparable amounts**:

- a **weak acid** $\ce{HA}$ **and** its **conjugate base** $\ce{A-}$ (e.g., $\ce{CH3COOH}$ and $\ce{CH3COO-}$), **or**
- a **weak base** $\ce{B}$ **and** its **conjugate acid** $\ce{BH+}$ (e.g., $\ce{NH3}$ and $\ce{NH4+}$).

Two words carry all the weight. **Weak** — a strong acid ionizes completely, so there's no un-ionized reservoir to do any shifting; strong acids and their "conjugates" cannot buffer. **Comparable** — you need a real stockpile of *both* partners, because one handles added base and the other handles added acid.

### The Henderson-Hasselbalch equation

Start from the definition of $K_a$ for the weak acid:

$$K_a = \frac{[\ce{H+}][\ce{A-}]}{[\ce{HA}]}$$

Solve for $[\ce{H+}]$:

$$[\ce{H+}] = K_a \cdot \frac{[\ce{HA}]}{[\ce{A-}]}$$

Take $-\log$ of both sides. Since $\text{pH} = -\log[\ce{H+}]$ and $\text{p}K_a = -\log K_a$, the product becomes a sum and the fraction flips when the sign flips:

$$\boxed{\ \text{pH} = \text{p}K_a + \log\frac{[\ce{A-}]}{[\ce{HA}]}\ }$$

That's the **Henderson-Hasselbalch equation**. Read it out loud: a buffer's pH is its $\text{p}K_a$ nudged up or down by the log of the **base-to-acid ratio**. Three consequences fall right out:

- **Equal components ($[\ce{A-}] = [\ce{HA}]$):** the ratio is 1, $\log 1 = 0$, so $\text{pH} = \text{p}K_a$. This is the single most useful fact about buffers.
- **More base than acid:** the ratio exceeds 1, the log is positive, $\text{pH} > \text{p}K_a$.
- **More acid than base:** the ratio is below 1, the log is negative, $\text{pH} < \text{p}K_a$.

**One huge convenience:** the ratio $\frac{[\ce{A-}]}{[\ce{HA}]}$ is a ratio, and since both live in the *same* solution with the *same* volume, the volume cancels. So you can plug in **moles instead of concentrations** — $\log\frac{n_{\ce{A-}}}{n_{\ce{HA}}}$ — and get the same answer. That trick is what makes the "stoichiometry then H-H" method below so clean.

### Choosing a buffer

Because $\text{pH} = \text{p}K_a$ when the components are equal, building a buffer for a target pH is mostly one decision: **pick a weak acid whose $\text{p}K_a$ is close to the pH you want** (within about $\pm 1$), then fine-tune with the ratio. Want pH 4.7? Acetic acid ($\text{p}K_a \approx 4.74$) is nearly perfect with a 1:1 mix. Want pH 7.4, like blood? You want an acid with $\text{p}K_a$ near 7.4 — and the carbonic acid system ($\text{p}K_a \approx 6.1$ for the relevant step, pushed up by the body keeping lots of bicarbonate around) is what nature reached for.

---

## Worked Examples

### Example 1: Is it a buffer? (identification)

**Problem:** Which of these are buffers?
(a) $\ce{CH3COOH}$ + $\ce{CH3COONa}$  (b) $\ce{HCl}$ + $\ce{NaCl}$  (c) $\ce{NH3}$ + $\ce{NH4Cl}$  (d) $\ce{HCl}$ + $\ce{NaOH}$ (equal moles)

**Solution:**
- **(a)** Weak acid ($\ce{CH3COOH}$) + its conjugate base (from $\ce{CH3COONa}$, which provides $\ce{CH3COO-}$). **Buffer.** ✅
- **(b)** $\ce{HCl}$ is a **strong** acid, and $\ce{Cl-}$ is the conjugate base of a strong acid, so it's a spectator with no buffering power. **Not a buffer.** ❌
- **(c)** Weak base ($\ce{NH3}$) + its conjugate acid ($\ce{NH4+}$ from $\ce{NH4Cl}$). **Buffer.** ✅
- **(d)** Strong acid + strong base in equal moles just neutralize to salt water. Nothing weak survives. **Not a buffer.** ❌

**Answer:** (a) and (c) are buffers; (b) and (d) are not.

---

### Example 2: Basic Henderson-Hasselbalch pH

**Problem:** A buffer is $0.20\ \text{M}$ acetic acid ($\ce{CH3COOH}$, $K_a = 1.8\times10^{-5}$) and $0.20\ \text{M}$ sodium acetate ($\ce{CH3COONa}$). Find the pH.

**Solution:**
**Step 1 — get $\text{p}K_a$:** $\text{p}K_a = -\log(1.8\times10^{-5}) = 4.74$.
**Step 2 — identify the pair:** $\ce{HA} = \ce{CH3COOH}$ at $0.20\ \text{M}$; $\ce{A-} = \ce{CH3COO-}$ at $0.20\ \text{M}$.
**Step 3 — Henderson-Hasselbalch:**

$$\text{pH} = 4.74 + \log\frac{0.20}{0.20} = 4.74 + \log(1) = 4.74 + 0 = 4.74$$

**Answer:** $\text{pH} = 4.74$. Equal components, so pH equals $\text{p}K_a$ exactly.

---

### Example 3: Unequal components

**Problem:** Same acetic acid system, but now $0.30\ \text{M}$ $\ce{CH3COO-}$ and $0.10\ \text{M}$ $\ce{CH3COOH}$. Find the pH.

**Solution:**

$$\text{pH} = 4.74 + \log\frac{0.30}{0.10} = 4.74 + \log(3) = 4.74 + 0.48 = 5.22$$

**Answer:** $\text{pH} = 5.22$. More conjugate base than acid, so pH rose above $\text{p}K_a$ — exactly as predicted.

---

### Example 4: A basic buffer (weak base + conjugate acid)

**Problem:** A buffer contains $0.25\ \text{M}$ $\ce{NH3}$ ($K_b = 1.8\times10^{-5}$) and $0.40\ \text{M}$ $\ce{NH4Cl}$. Find the pH.

**Solution:**
**Step 1 — Henderson-Hasselbalch needs $\text{p}K_a$ of the acid.** Here the acid is $\ce{NH4+}$; the base is $\ce{NH3}$. Convert: $K_a = \dfrac{K_w}{K_b} = \dfrac{1.0\times10^{-14}}{1.8\times10^{-5}} = 5.6\times10^{-10}$, so $\text{p}K_a = 9.26$.
**Step 2 — set the pair:** $\ce{HA} = \ce{NH4+}$ at $0.40\ \text{M}$; $\ce{A-} = \ce{NH3}$ at $0.25\ \text{M}$.
**Step 3 — plug in:**

$$\text{pH} = 9.26 + \log\frac{0.25}{0.40} = 9.26 + \log(0.625) = 9.26 - 0.20 = 9.06$$

**Answer:** $\text{pH} = 9.06$. (A basic buffer, as expected for an ammonia system.)

---

### Example 5: Find the ratio for a target pH

**Problem:** You need an acetate buffer ($\text{p}K_a = 4.74$) at exactly $\text{pH} = 5.00$. What ratio $\frac{[\ce{A-}]}{[\ce{HA}]}$ do you need?

**Solution:**
**Step 1 — write H-H and isolate the log:**

$$5.00 = 4.74 + \log\frac{[\ce{A-}]}{[\ce{HA}]} \quad\Rightarrow\quad \log\frac{[\ce{A-}]}{[\ce{HA}]} = 0.26$$

**Step 2 — undo the log:**

$$\frac{[\ce{A-}]}{[\ce{HA}]} = 10^{0.26} = 1.8$$

**Answer:** You need about **1.8 mol of acetate per 1 mol of acetic acid**. (More base than acid, since 5.00 > 4.74 — sanity check passes.)

---

### Example 6: Grams of salt to add

**Problem:** You have $1.0\ \text{L}$ of $0.15\ \text{M}$ acetic acid ($\text{p}K_a = 4.74$). How many **grams of sodium acetate** ($\ce{CH3COONa}$, molar mass $82.0\ \text{g/mol}$) must you dissolve in it to make a buffer of $\text{pH} = 4.90$? (Assume no volume change.)

**Solution:**
**Step 1 — find the needed ratio:**

$$4.90 = 4.74 + \log\frac{[\ce{A-}]}{[\ce{HA}]} \Rightarrow \log\frac{[\ce{A-}]}{[\ce{HA}]} = 0.16 \Rightarrow \frac{[\ce{A-}]}{[\ce{HA}]} = 10^{0.16} = 1.45$$

**Step 2 — solve for $[\ce{A-}]$:** with $[\ce{HA}] = 0.15\ \text{M}$, $[\ce{A-}] = 1.45 \times 0.15 = 0.218\ \text{M}$.
**Step 3 — moles then grams:** in $1.0\ \text{L}$, that's $0.218\ \text{mol}$ of acetate.

$$0.218\ \text{mol} \times 82.0\ \text{g/mol} = 17.9\ \text{g}$$

**Answer:** Dissolve about **18 g** of sodium acetate.

---

### Example 7: Making a buffer by partial neutralization

**Problem:** You mix $50.0\ \text{mL}$ of $0.40\ \text{M}$ acetic acid with $20.0\ \text{mL}$ of $0.40\ \text{M}$ $\ce{NaOH}$. Is the result a buffer, and what is its pH? ($\text{p}K_a = 4.74$.)

**Solution:**
**Step 1 — initial moles:**
$\ce{CH3COOH}$: $0.0500\ \text{L} \times 0.40\ \text{M} = 0.020\ \text{mol}$.
$\ce{NaOH}$: $0.0200\ \text{L} \times 0.40\ \text{M} = 0.0080\ \text{mol}$.
**Step 2 — strong base reacts completely, converting acid to its conjugate base:**

$$\ce{CH3COOH + OH- -> CH3COO- + H2O}$$

| | $\ce{CH3COOH}$ | $\ce{OH-}$ | $\ce{CH3COO-}$ |
|---|---|---|---|
| Start | 0.020 | 0.0080 | 0 |
| Change | $-0.0080$ | $-0.0080$ | $+0.0080$ |
| End | **0.012** | 0 | **0.0080** |

Both a weak acid ($0.012\ \text{mol}$) and its conjugate base ($0.0080\ \text{mol}$) remain — **yes, it's a buffer.**
**Step 3 — Henderson-Hasselbalch (moles are fine, volume cancels):**

$$\text{pH} = 4.74 + \log\frac{0.0080}{0.012} = 4.74 + \log(0.667) = 4.74 - 0.18 = 4.56$$

**Answer:** It's a buffer at $\text{pH} = 4.56$. (This is exactly the chemistry of a titration before the equivalence point — see [Titration Curves](/chemistry/1005-titration-curves).)

---

### Example 8: Adding strong acid to a buffer (the main event)

**Problem:** A buffer contains $0.50\ \text{mol}$ $\ce{CH3COOH}$ and $0.50\ \text{mol}$ $\ce{CH3COO-}$ in $1.0\ \text{L}$ ($\text{p}K_a = 4.74$). You add $0.10\ \text{mol}$ of $\ce{HCl}$ (assume no volume change). Find the new pH.

**Solution:**
**Step 1 — Stoichiometry FIRST.** Strong acid $\ce{H+}$ reacts completely with the base component:

$$\ce{CH3COO- + H+ -> CH3COOH}$$

| | $\ce{CH3COO-}$ | $\ce{H+}$ | $\ce{CH3COOH}$ |
|---|---|---|---|
| Start | 0.50 | 0.10 | 0.50 |
| Change | $-0.10$ | $-0.10$ | $+0.10$ |
| End | **0.40** | 0 | **0.60** |

**Step 2 — THEN Henderson-Hasselbalch with the new amounts:**

$$\text{pH} = 4.74 + \log\frac{0.40}{0.60} = 4.74 + \log(0.667) = 4.74 - 0.18 = 4.56$$

**Answer:** $\text{pH} = 4.56$. The pH dropped only **0.18** despite adding a slug of strong acid. Compare that to the next example.

---

### Example 9: The dramatic contrast — same acid, pure water

**Problem:** Add that same $0.10\ \text{mol}$ of $\ce{HCl}$ to $1.0\ \text{L}$ of **pure water** (starting $\text{pH} = 7.00$). What's the new pH?

**Solution:**
**Step 1 —** $\ce{HCl}$ is strong, so $[\ce{H+}] = 0.10\ \text{mol} / 1.0\ \text{L} = 0.10\ \text{M}$.
**Step 2 —** $\text{pH} = -\log(0.10) = 1.00$.

**Answer:** $\text{pH} = 1.00$. The pH plunged **6 full units** (7.00 → 1.00). The identical acid dose moved the buffer only 0.18. **That gap — 6.0 vs. 0.18 — is the entire reason buffers exist.**

---

### Example 10: Adding strong base to a buffer

**Problem:** Same starting buffer as Example 8 ($0.50\ \text{mol}$ $\ce{HA}$, $0.50\ \text{mol}$ $\ce{A-}$, $1.0\ \text{L}$). Now add $0.10\ \text{mol}$ of $\ce{NaOH}$. Find the new pH.

**Solution:**
**Step 1 — Stoichiometry first.** Strong base $\ce{OH-}$ reacts with the acid component:

$$\ce{CH3COOH + OH- -> CH3COO- + H2O}$$

| | $\ce{CH3COOH}$ | $\ce{OH-}$ | $\ce{CH3COO-}$ |
|---|---|---|---|
| Start | 0.50 | 0.10 | 0.50 |
| Change | $-0.10$ | $-0.10$ | $+0.10$ |
| End | **0.40** | 0 | **0.60** |

**Step 2 — Henderson-Hasselbalch:**

$$\text{pH} = 4.74 + \log\frac{0.60}{0.40} = 4.74 + \log(1.5) = 4.74 + 0.18 = 4.92$$

**Answer:** $\text{pH} = 4.92$, a rise of just 0.18. Note it moved **up** this time — added base consumes acid and makes more conjugate base. (Contrast: $0.10\ \text{mol}$ $\ce{NaOH}$ in pure water gives $[\ce{OH-}] = 0.10$, $\text{pOH} = 1$, $\text{pH} = 13$ — a 6-unit jump.)

---

### Example 11: Choosing the right acid for a target pH

**Problem:** You need a buffer at $\text{pH} = 7.20$. You have four acids available: formic ($\text{p}K_a = 3.75$), acetic ($4.74$), dihydrogen phosphate $\ce{H2PO4-}$ ($7.21$), and ammonium $\ce{NH4+}$ ($9.25$). Which do you choose, and roughly what ratio?

**Solution:**
**Step 1 — pick the $\text{p}K_a$ closest to the target.** $7.21$ (dihydrogen phosphate) is essentially on top of 7.20. The others are more than a full unit away and would need extreme ratios (weak capacity).
**Step 2 — ratio:** $7.20 = 7.21 + \log\frac{[\ce{A-}]}{[\ce{HA}]} \Rightarrow \log(\ldots) = -0.01 \Rightarrow$ ratio $= 10^{-0.01} \approx 0.98 \approx 1$.

**Answer:** Use the $\ce{H2PO4-}/\ce{HPO4^2-}$ pair at a **~1:1 ratio**. (This is exactly why phosphate buffers are a lab favorite for near-neutral pH — and why the body uses a phosphate buffer inside cells.)

---

### Example 12: Pushing a buffer past its limit ("using it up")

**Problem:** A buffer has $0.10\ \text{mol}$ $\ce{CH3COOH}$ and $0.10\ \text{mol}$ $\ce{CH3COO-}$ in $1.0\ \text{L}$. You add $0.12\ \text{mol}$ of $\ce{HCl}$. Find the pH.

**Solution:**
**Step 1 — Stoichiometry.** $\ce{H+}$ attacks the base component, but there's only $0.10\ \text{mol}$ of $\ce{CH3COO-}$ and $0.12\ \text{mol}$ of $\ce{H+}$:

| | $\ce{CH3COO-}$ | $\ce{H+}$ | $\ce{CH3COOH}$ |
|---|---|---|---|
| Start | 0.10 | 0.12 | 0.10 |
| End | 0 | **0.02 left over** | 0.20 |

The base component is **completely consumed** — the buffer is broken. There is $0.02\ \text{mol}$ of leftover strong $\ce{H+}$.
**Step 2 — no buffer left; the leftover strong acid sets the pH** (the small extra from acetic acid is negligible): $[\ce{H+}] = 0.02\ \text{M}$.

$$\text{pH} = -\log(0.02) = 1.70$$

**Answer:** $\text{pH} = 1.70$. Once you exceed the buffer's capacity, pH crashes almost like there was no buffer at all. **That's what "using up" a buffer means.**

---

### Example 13: Buffer capacity comparison

**Problem:** Buffer A is $1.0\ \text{M}$ $\ce{HA}$ / $1.0\ \text{M}$ $\ce{A-}$. Buffer B is $0.010\ \text{M}$ $\ce{HA}$ / $0.010\ \text{M}$ $\ce{A-}$. Same $\text{p}K_a = 4.74$, same 1:1 ratio, so both start at $\text{pH} = 4.74$. Add $0.10\ \text{mol}$ of $\ce{HCl}$ to $1.0\ \text{L}$ of each. Which holds pH better?

**Solution:**
**Buffer A:** ends $0.90\ \text{mol}$ $\ce{A-}$, $1.10\ \text{mol}$ $\ce{HA}$ → $\text{pH} = 4.74 + \log\frac{0.90}{1.10} = 4.74 - 0.09 = 4.65$. Change: **0.09**.
**Buffer B:** only $0.010\ \text{mol}$ of $\ce{A-}$ exists — $0.10\ \text{mol}$ of $\ce{H+}$ obliterates it instantly, leaving $0.09\ \text{mol}$ excess strong acid → $\text{pH} \approx -\log(0.09) = 1.05$. Change: **3.7**.

**Answer:** Buffer A barely moves; Buffer B is destroyed. **Same pH, same ratio — but the concentrated buffer has far greater capacity.** Capacity scales with how *much* of each component you have, not just the ratio.

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Doing Henderson-Hasselbalch **before** the strong-acid/base stoichiometry | Rushing to the "buffer equation" | **Stoichiometry always comes first.** Strong acid/base reacts 100%; update the $\ce{HA}$ and $\ce{A-}$ amounts, *then* plug into H-H. |
| Calling a strong acid + its salt a buffer (e.g. $\ce{HCl}$ + $\ce{NaCl}$) | "Acid and its conjugate base" sounds right | The acid must be **weak**. $\ce{Cl-}$ is the useless conjugate of a strong acid — no reservoir, no buffering. |
| Flipping the ratio to $\frac{[\ce{HA}]}{[\ce{A-}]}$ | Misremembering the equation | It's **base over acid**: $\log\frac{[\ce{A-}]}{[\ce{HA}]}$. Sanity check: more base ⇒ higher pH. |
| Converting moles to molarity before H-H (extra work + error) | Habit from other pH problems | In H-H the volume cancels — use **moles directly** for the ratio. (You still need volume if you must find an actual $[\ce{H+}]$.) |
| Using $K_b$ directly in H-H for a basic buffer | The equation is written in $K_a$ terms | Convert first: $\text{p}K_a = 14 - \text{p}K_b$, or $K_a = K_w/K_b$. H-H always uses $\text{p}K_a$. |
| Assuming the pH after adding acid/base is *unchanged* | "Buffers resist change" gets over-read | Buffers **reduce** change, they don't eliminate it. The ratio shifts, so the pH shifts a little. |
| Forgetting a buffer can be exhausted | Treating capacity as infinite | If added strong acid/base **exceeds** a component, that component hits zero and the leftover strong reagent sets the pH. |

---

## AP Exam Tips

- **Stoichiometry first, Henderson-Hasselbalch second.** This is the #1 graded skill in buffer FRQs. Show the reaction, show a before/after table, *then* the equation. Points are awarded for the sequence, not just the final number.
- **Memorize $\text{pH} = \text{p}K_a$ when components are equal.** It's an instant answer and a built-in sanity check on everything else.
- **Choosing a buffer = matching $\text{p}K_a$ to target pH.** Pick the acid whose $\text{p}K_a$ is within $\pm 1$ of the desired pH; then the ratio does the fine-tuning.
- **Buffer capacity is greatest at a 1:1 ratio and high concentration.** Expect a conceptual question comparing two buffers — the more concentrated one (and the one nearer 1:1) wins.
- **A buffer works best within $\pm 1$ pH unit of its $\text{p}K_a$.** Outside that window one component is too scarce to absorb much.
- **Know the two neutralization reactions cold:** added $\ce{H+}$ → reacts with $\ce{A-}$; added $\ce{OH-}$ → reacts with $\ce{HA}$. You'll be asked to write these.
- **Buffers are top-weighted.** They show up in the acid-base FRQ nearly every year and connect directly to titration curves. Do not skimp here.
- **Calculator note:** you'll need $\log$ and $10^x$. Practice both directions (pH → ratio and ratio → pH) so the antilog step is automatic.

---

## Practice Problems

### Problem 1
Which of the following pairs can form a buffer? (a) $\ce{HNO3}$ / $\ce{NaNO3}$, (b) $\ce{HF}$ / $\ce{NaF}$, (c) $\ce{HCN}$ / $\ce{KCN}$, (d) $\ce{NaOH}$ / $\ce{NaCl}$.

<details>
<summary><strong>Solution</strong></summary>

A buffer needs a **weak** acid + its conjugate base (or weak base + conjugate acid).
- (a) $\ce{HNO3}$ is strong → **not a buffer.**
- (b) $\ce{HF}$ is weak, $\ce{F-}$ is its conjugate base → **buffer.**
- (c) $\ce{HCN}$ is weak, $\ce{CN-}$ is its conjugate base → **buffer.**
- (d) A strong base and a spectator salt → **not a buffer.**

**Answer: (b) and (c).**

</details>

---

### Problem 2
A buffer is $0.15\ \text{M}$ $\ce{HF}$ ($K_a = 6.8\times10^{-4}$) and $0.15\ \text{M}$ $\ce{NaF}$. Find the pH.

<details>
<summary><strong>Solution</strong></summary>

$\text{p}K_a = -\log(6.8\times10^{-4}) = 3.17$. Equal components ⇒ ratio 1 ⇒ $\log 1 = 0$.

$$\text{pH} = 3.17 + \log\frac{0.15}{0.15} = 3.17$$

**Answer: $\text{pH} = 3.17$.**

</details>

---

### Problem 3
A buffer contains $0.30\ \text{M}$ $\ce{HF}$ and $0.20\ \text{M}$ $\ce{F-}$ ($\text{p}K_a = 3.17$). Find the pH.

<details>
<summary><strong>Solution</strong></summary>

$$\text{pH} = 3.17 + \log\frac{0.20}{0.30} = 3.17 + \log(0.667) = 3.17 - 0.18 = 2.99$$

More acid than base ⇒ pH below $\text{p}K_a$. ✅

**Answer: $\text{pH} = 2.99$.**

</details>

---

### Problem 4
A buffer is $0.50\ \text{M}$ $\ce{NH3}$ ($K_b = 1.8\times10^{-5}$) and $0.50\ \text{M}$ $\ce{NH4Cl}$. Find the pH.

<details>
<summary><strong>Solution</strong></summary>

Convert to $\text{p}K_a$ of $\ce{NH4+}$: $K_a = \dfrac{1.0\times10^{-14}}{1.8\times10^{-5}} = 5.6\times10^{-10}$, $\text{p}K_a = 9.26$. Equal components:

$$\text{pH} = 9.26 + \log(1) = 9.26$$

**Answer: $\text{pH} = 9.26$.**

</details>

---

### Problem 5
You want a formate buffer ($\text{p}K_a = 3.75$) at $\text{pH} = 4.00$. What ratio $\frac{[\ce{A-}]}{[\ce{HA}]}$ is required?

<details>
<summary><strong>Solution</strong></summary>

$$4.00 = 3.75 + \log\frac{[\ce{A-}]}{[\ce{HA}]} \Rightarrow \log(\ldots) = 0.25 \Rightarrow \frac{[\ce{A-}]}{[\ce{HA}]} = 10^{0.25} = 1.78$$

**Answer: about 1.8 mol formate per 1 mol formic acid.**

</details>

---

### Problem 6
$1.0\ \text{L}$ of a buffer holds $0.40\ \text{mol}$ $\ce{CH3COOH}$ and $0.40\ \text{mol}$ $\ce{CH3COO-}$ ($\text{p}K_a = 4.74$). Add $0.050\ \text{mol}$ of $\ce{HCl}$. Find the new pH.

<details>
<summary><strong>Solution</strong></summary>

**Stoichiometry first:** $\ce{H+}$ + $\ce{CH3COO-} -> \ce{CH3COOH}$.
$\ce{CH3COO-}$: $0.40 - 0.050 = 0.35$. $\ce{CH3COOH}$: $0.40 + 0.050 = 0.45$.

$$\text{pH} = 4.74 + \log\frac{0.35}{0.45} = 4.74 - 0.11 = 4.63$$

**Answer: $\text{pH} = 4.63$** (dropped only 0.11 from 4.74).

</details>

---

### Problem 7
Same buffer as Problem 6 ($0.40\ \text{mol}$ each, $1.0\ \text{L}$). Instead add $0.050\ \text{mol}$ of $\ce{KOH}$. Find the new pH.

<details>
<summary><strong>Solution</strong></summary>

**Stoichiometry:** $\ce{OH-}$ + $\ce{CH3COOH} -> \ce{CH3COO-}$ + $\ce{H2O}$.
$\ce{CH3COOH}$: $0.40 - 0.050 = 0.35$. $\ce{CH3COO-}$: $0.40 + 0.050 = 0.45$.

$$\text{pH} = 4.74 + \log\frac{0.45}{0.35} = 4.74 + 0.11 = 4.85$$

**Answer: $\text{pH} = 4.85$** (rose 0.11; added base ⇒ pH up).

</details>

---

### Problem 8
Add $0.050\ \text{mol}$ of $\ce{HCl}$ to $1.0\ \text{L}$ of **pure water**. Find the pH, and compare with Problem 6.

<details>
<summary><strong>Solution</strong></summary>

$\ce{HCl}$ is strong: $[\ce{H+}] = 0.050\ \text{M}$, $\text{pH} = -\log(0.050) = 1.30$.

Water went from 7.00 to 1.30 — a **5.7-unit** crash. The identical dose moved the buffer only 0.11 (Problem 6).

**Answer: $\text{pH} = 1.30$; the buffer resists ~50× better.**

</details>

---

### Problem 9
Mix $100.0\ \text{mL}$ of $0.50\ \text{M}$ $\ce{CH3COOH}$ with $40.0\ \text{mL}$ of $0.50\ \text{M}$ $\ce{NaOH}$. Is it a buffer? Find the pH ($\text{p}K_a = 4.74$).

<details>
<summary><strong>Solution</strong></summary>

Moles: $\ce{CH3COOH} = 0.100 \times 0.50 = 0.050$; $\ce{NaOH} = 0.040 \times 0.50 = 0.020$.
Reaction $\ce{CH3COOH + OH- -> CH3COO- + H2O}$:
$\ce{CH3COOH} = 0.050 - 0.020 = 0.030$; $\ce{CH3COO-} = 0.020$. Both present ⇒ **buffer.**

$$\text{pH} = 4.74 + \log\frac{0.020}{0.030} = 4.74 - 0.18 = 4.56$$

**Answer: yes, a buffer; $\text{pH} = 4.56$.**

</details>

---

### Problem 10
How many grams of $\ce{NH4Cl}$ ($M = 53.5\ \text{g/mol}$) must be added to $1.0\ \text{L}$ of $0.20\ \text{M}$ $\ce{NH3}$ to make a $\text{pH} = 9.00$ buffer? ($\ce{NH4+}$: $\text{p}K_a = 9.26$, no volume change.)

<details>
<summary><strong>Solution</strong></summary>

H-H: $\ce{A-} = \ce{NH3}$, $\ce{HA} = \ce{NH4+}$.

$$9.00 = 9.26 + \log\frac{0.20}{[\ce{NH4+}]} \Rightarrow \log\frac{0.20}{[\ce{NH4+}]} = -0.26 \Rightarrow \frac{0.20}{[\ce{NH4+}]} = 10^{-0.26} = 0.55$$

So $[\ce{NH4+}] = 0.20/0.55 = 0.36\ \text{M}$ ⇒ $0.36\ \text{mol}$ in $1.0\ \text{L}$.
Mass $= 0.36 \times 53.5 = 19.3\ \text{g}$.

**Answer: about 19 g of $\ce{NH4Cl}$.**

</details>

---

### Problem 11
A buffer has $0.20\ \text{mol}$ $\ce{HA}$ and $0.20\ \text{mol}$ $\ce{A-}$ in $1.0\ \text{L}$ ($\text{p}K_a = 4.74$). You add $0.25\ \text{mol}$ of $\ce{HCl}$. Find the pH.

<details>
<summary><strong>Solution</strong></summary>

$\ce{H+}$ ($0.25$) attacks $\ce{A-}$ ($0.20$) — but there's only $0.20\ \text{mol}$ of base. It's fully consumed; $0.05\ \text{mol}$ of strong $\ce{H+}$ is left over. **Buffer destroyed.**

$[\ce{H+}] = 0.05\ \text{M}$ ⇒ $\text{pH} = -\log(0.05) = 1.30$.

**Answer: $\text{pH} = 1.30$ — capacity exceeded.**

</details>

---

### Problem 12
Two buffers both start at $\text{pH} = 4.74$ (1:1, $\text{p}K_a = 4.74$). Buffer X is $2.0\ \text{M}$/$2.0\ \text{M}$; Buffer Y is $0.20\ \text{M}$/$0.20\ \text{M}$. Add $0.10\ \text{mol}$ $\ce{HCl}$ to $1.0\ \text{L}$ of each. Which resists better, and why?

<details>
<summary><strong>Solution</strong></summary>

**X:** $\ce{A-}: 2.00 \to 1.90$, $\ce{HA}: 2.00 \to 2.10$. $\text{pH} = 4.74 + \log\frac{1.90}{2.10} = 4.74 - 0.04 = 4.70$. Change 0.04.
**Y:** $\ce{A-}: 0.20 \to 0.10$, $\ce{HA}: 0.20 \to 0.30$. $\text{pH} = 4.74 + \log\frac{0.10}{0.30} = 4.74 - 0.48 = 4.26$. Change 0.48.

**Answer: X resists ~10× better — higher concentration means greater buffer capacity**, even at the same ratio and starting pH.

</details>

---

### Problem 13
Explain, using Le Chatelier, why adding a little $\ce{NaOH}$ to an acetic-acid/acetate buffer barely changes the pH.

<details>
<summary><strong>Solution</strong></summary>

The equilibrium is $\ce{CH3COOH <=> H+ + CH3COO-}$. Added $\ce{OH-}$ consumes $\ce{H+}$ (forming water), which is a stress removing product $\ce{H+}$. By Le Chatelier the system **shifts right**, ionizing more $\ce{CH3COOH}$ to replace the lost $\ce{H+}$. Because there's a large reservoir of un-ionized $\ce{CH3COOH}$ ready to do this, most of the added base is absorbed and $[\ce{H+}]$ — hence pH — barely moves.

**Answer: the buffer shifts to replace consumed $\ce{H+}$, so pH holds nearly steady.**

</details>

---

### Problem 14
Your blood buffer is $\ce{H2CO3}/\ce{HCO3-}$. When you **hold your breath**, $\ce{CO2}$ builds up, and $\ce{CO2 + H2O <=> H2CO3 <=> H+ + HCO3-}$. Predict what happens to blood pH, and what happens if you **hyperventilate** (blow off $\ce{CO2}$).

<details>
<summary><strong>Solution</strong></summary>

**Holding breath:** $\ce{CO2}$ accumulates, pushing $\ce{CO2 + H2O <=> H2CO3 <=> H+ + HCO3-}$ to the **right**, raising $[\ce{H+}]$ → **blood pH drops** (more acidic; "respiratory acidosis").

**Hyperventilating:** you exhale $\ce{CO2}$ faster than it's made, removing reactant, so the equilibrium shifts **left**, lowering $[\ce{H+}]$ → **blood pH rises** (more basic; "respiratory alkalosis"), which is why over-breathing can make you lightheaded.

**Answer: hold breath → pH down; hyperventilate → pH up.** Your breathing rate is a live control knob on the buffer.

</details>

---

### Problem 15
A buffer is designed for $\text{pH} = 5.0$. You have acids with $\text{p}K_a$ values 2.0, 4.9, 7.2, and 9.3. (a) Which is the best choice? (b) Roughly what ratio $\frac{[\ce{A-}]}{[\ce{HA}]}$ does it need?

<details>
<summary><strong>Solution</strong></summary>

(a) Pick the $\text{p}K_a$ closest to the target: **4.9** (within 0.1 of 5.0). The others are $\ge 2$ units off and would need extreme ratios with poor capacity.
(b) $5.0 = 4.9 + \log\frac{[\ce{A-}]}{[\ce{HA}]} \Rightarrow \log(\ldots) = 0.1 \Rightarrow$ ratio $= 10^{0.1} = 1.26 \approx 1.3$.

**Answer: use the $\text{p}K_a = 4.9$ acid at about a 1.3:1 base:acid ratio.**

</details>

---

## Quick Reference

| Concept | Key fact |
|---|---|
| What a buffer is | Weak acid $\ce{HA}$ **+** its conjugate base $\ce{A-}$ (or weak base + conjugate acid) in comparable amounts |
| Absorbs added acid | $\ce{A- + H+ -> HA}$ (base component reacts) |
| Absorbs added base | $\ce{HA + OH- -> A- + H2O}$ (acid component reacts) |
| Henderson-Hasselbalch | $\text{pH} = \text{p}K_a + \log\dfrac{[\ce{A-}]}{[\ce{HA}]}$ (moles OK — volume cancels) |
| Equal components | $[\ce{A-}] = [\ce{HA}] \Rightarrow \text{pH} = \text{p}K_a$ |
| Choosing a buffer | Pick acid with $\text{p}K_a$ within $\pm 1$ of target pH |
| Adding strong acid/base | **Stoichiometry first** (reacts 100%), **then** Henderson-Hasselbalch |
| Effective range | Buffers best within $\text{p}K_a \pm 1$ |
| Buffer capacity | Greatest at **1:1 ratio** and **high concentration**; exceeded when a component hits zero |
| Basic buffer in H-H | Convert first: $\text{p}K_a = 14 - \text{p}K_b$ |
| Blood buffer | $\ce{H2CO3}/\ce{HCO3-}$ holds blood at pH ≈ 7.4; breathing rate tunes it |

---

<div align="center">

[← Acid Strength and Structure](/chemistry/1003-molecular-structure-acid-strength) | [Titration Curves →](/chemistry/1005-titration-curves)

</div>
