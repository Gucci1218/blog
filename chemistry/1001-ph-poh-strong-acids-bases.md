# pH, pOH, and Strong Acids and Bases
<p class="article-date">July 5, 2026</p>

*Last weekend I chopped up half a head of red cabbage, boiled it, and strained off this deep bruise-purple water — and it turned my kitchen into a chemistry lab. I poured a splash into three glasses. Into the first I squeezed lemon juice, and it flashed bright pink-red. Into the second I stirred a spoonful of baking soda, and it went blue, then almost green. The third I left alone and it stayed purple. Same juice, three colors, and the only thing that changed was how many hydrogen ions were floating around. That cabbage water is a crude sensor for $[\ce{H+}]$ — the red end means lots of $\ce{H+}$, the blue-green end means barely any. This article is about the precise number hiding behind those colors: pH. It's where Unit 8 begins, and it turns "kind of acidic" into an exact, calculable quantity.*

---

## What You'll Learn
- Explain the **autoionization of water** and what $K_w = 1.0\times10^{-14}$ means at 25°C
- Use $K_w = [\ce{H+}][\ce{OH-}]$ to convert between $[\ce{H+}]$ and $[\ce{OH-}]$
- Define **pH** and **pOH** as the "$-\log$ of" a concentration, and use $\text{pH} + \text{pOH} = 14$
- Convert freely among all four quantities: $[\ce{H+}] \leftrightarrow \text{pH} \leftrightarrow \text{pOH} \leftrightarrow [\ce{OH-}]$
- Apply the log **sig-fig rule** (decimal places in pH = sig figs in concentration)
- Place everyday liquids on the 0–14 pH scale and read each pH unit as a **factor of 10**
- Compute the pH of a **strong monoprotic acid** directly from its concentration
- Compute the pH of a **strong base**, handling the $\ce{Ca(OH)2}$ "times-two" trap
- Predict how **diluting** a strong acid or base changes its pH

---

## Prerequisites
- [Acid-Base Reactions](/chemistry/0605-acid-base-reactions) — Brønsted-Lowry proton transfer and the memorized strong-acid / strong-base lists; this article is the AP-depth upgrade of that intro
- [Logarithms for Chemistry](/chemistry/0104-logarithms-for-chemistry) — pH *is* a logarithm; the earthquake scale and the sig-fig rule from that article pay off here in full

---

## The Core Concept

### Intuition First

Back to my three glasses of cabbage juice. The purple pigment (a molecule called anthocyanin) physically changes shape depending on how many hydrogen ions surround it, and each shape reflects different light. So the color is a **rough readout of $[\ce{H+}]$**:

- **Red / pink** end → **high** $[\ce{H+}]$ → **acidic** → **low pH**
- **Purple** middle → $[\ce{H+}]$ near the neutral value → **neutral**
- **Blue / green** end → **low** $[\ce{H+}]$ → **basic** → **high pH**

The cabbage gives you a color. What it can't give you is a *number* — is this lemon juice pH 2.1 or pH 2.4? That precision is what pH provides. Think of the cabbage rainbow as the fuzzy analog dial and pH as the exact digital readout behind it. Everything in this article is just learning to read that dial precisely.

But before we can measure $[\ce{H+}]$, we have to answer a sneaky question: where do the hydrogen ions in *plain water* even come from? Because pure water — glass number three — isn't at zero $\ce{H+}$. It sits right in the purple middle for a reason.

### The Autoionization of Water

Water is quietly reacting with itself all the time. Every so often one water molecule hands a proton ($\ce{H+}$) to a neighbor:

$$\ce{2H2O <=> H3O+ + OH-}$$

One water becomes a **hydronium ion** ($\ce{H3O+}$) and the other becomes a **hydroxide ion** ($\ce{OH-}$). Chemists often abbreviate $\ce{H3O+}$ as just $\ce{H+}$ — they mean the same thing, "a loose proton in water." I'll write $\ce{H+}$ from here on.

This reaction barely happens (the double arrow leans hard left), but it never fully stops. At equilibrium the amounts are governed by a special constant, the **ion-product constant of water**:

$$K_w = [\ce{H+}][\ce{OH-}] = 1.0 \times 10^{-14} \quad (\text{at } 25°C)$$

This is the master equation of the whole topic. Read it out loud: *the concentration of hydrogen ions times the concentration of hydroxide ions always equals $10^{-14}$.* Always — in lemon juice, in bleach, in blood. It's a seesaw. Push $[\ce{H+}]$ **up** and $[\ce{OH-}]$ must come **down** to keep the product fixed, and vice versa.

**Neutral** means the two are equal. Set $[\ce{H+}] = [\ce{OH-}] = x$:

$$x^2 = 1.0\times10^{-14} \implies x = 1.0\times10^{-7}$$

$$\boxed{[\ce{H+}] = [\ce{OH-}] = 1.0\times10^{-7}\ \text{M in neutral water}}$$

That's glass three, the purple middle. Not zero $\ce{H+}$ — a tiny, specific amount.

### pH and pOH: the "p" Operator

Concentrations like $1.0\times10^{-7}$ are annoying to say and compare. In [Logarithms for Chemistry](/chemistry/0104-logarithms-for-chemistry) we borrowed the earthquake trick: instead of reporting the shaking, report its **exponent**. The Richter scale counts zeros, not wiggles. pH does the exact same thing to $[\ce{H+}]$.

The little "**p**" in front of anything means "**take the negative base-10 log of it**":

$$\text{pH} = -\log[\ce{H+}] \qquad \text{pOH} = -\log[\ce{OH-}]$$

The minus sign is there because these concentrations are tiny, so their logs are negative, and nobody wants a scale full of minus signs. Flip the sign and neutral water becomes a friendly number:

$$\text{pH} = -\log(1.0\times10^{-7}) = 7.00$$

Apply the same "p" operator to $K_w$ itself:

$$\text{p}K_w = -\log(1.0\times10^{-14}) = 14.00$$

And because $K_w = [\ce{H+}][\ce{OH-}]$, taking $-\log$ of both sides turns the product into a sum (logs turn multiplication into addition — straight from article 0104):

$$\boxed{\text{pH} + \text{pOH} = 14.00 \quad (\text{at } 25°C)}$$

This is the second master equation. Now you have a full conversion web with four quantities:

$$[\ce{H+}] \;\underset{-\log}{\overset{10^{-x}}{\longleftrightarrow}}\; \text{pH} \;\underset{}{\overset{+\,\text{pOH}=14}{\longleftrightarrow}}\; \text{pOH} \;\underset{10^{-x}}{\overset{-\log}{\longleftrightarrow}}\; [\ce{OH-}]$$

Give me **any one** of these four and I can find the other three. That interconversion is the single most-tested skill in this section, so we'll drill it hard.

**The sig-fig rule (do not skip this).** From 0104: when you take a log, the **digits after the decimal point** in the answer equal the number of **sig figs** in the original number. The integer part of the pH is "free" — it just encodes the power of ten. So $[\ce{H+}] = 2.0\times10^{-5}$ M (2 sig figs) gives pH $= 4.70$ (2 digits after the decimal). The "4" is free; the "70" carries the precision. Graders check this line on the FRQ.

### The pH Scale, 0 to 14

Because pH runs opposite to $[\ce{H+}]$, the scale flips your intuition:

| pH | Meaning | $[\ce{H+}]$ | Cabbage color |
|---|---|---|---|
| **0–7** | Acidic | high ($> 10^{-7}$) | red → pink → purple |
| **7** | Neutral | $10^{-7}$ | purple |
| **7–14** | Basic | low ($< 10^{-7}$) | blue → green → yellow |

The crucial idea, straight from the earthquake analogy: **each pH unit is a factor of 10 in $[\ce{H+}]$.** A drop of 1 pH unit means ten times more $\ce{H+}$. Lemon juice at pH 2 isn't "a little more acidic" than coffee at pH 5 — it's $10^3 = 1000$ times more acidic. This is a log scale; think earthquakes, not rulers.

Here's the everyday world mapped onto the scale and the cabbage rainbow:

| Liquid | Approx. pH | Region | Cabbage color |
|---|---|---|---|
| Battery acid | ~0 | strongly acidic | bright red |
| Stomach acid | ~1.5 | strongly acidic | red |
| Lemon juice | ~2 | acidic | pink-red |
| Coffee | ~5 | weakly acidic | pinkish-purple |
| Pure water | 7 | neutral | purple |
| Blood | ~7.4 | very weakly basic | blue-purple |
| Baking soda | ~8.5 | basic | blue |
| Soap | ~10 | basic | blue-green |
| Bleach | ~13 | strongly basic | green-yellow |

Blood sitting at 7.4 — just barely basic — is not an accident; your body defends that number ferociously (that's buffers, coming in Unit 8). For now, notice the whole rainbow lives inside this one scale.

### Strong Acids and Bases: pH You Can Read Straight Off

Here's where the memorized lists from [Acid-Base Reactions](/chemistry/0605-acid-base-reactions) cash in. A **strong acid fully ionizes** — every molecule dumps its proton into the water. There's no equilibrium to solve, no leftover intact molecules. So for a **strong monoprotic acid**:

$$[\ce{H+}] = \text{acid concentration}$$

That's it. A $0.010$ M $\ce{HCl}$ solution has $[\ce{H+}] = 0.010$ M, so pH $= 2.00$. One line.

Recall the lists (memorize cold):

| The 6 strong acids | The strong bases |
|---|---|
| $\ce{HCl}$, $\ce{HBr}$, $\ce{HI}$ | Group 1 hydroxides: $\ce{LiOH}$, $\ce{NaOH}$, $\ce{KOH}$, … |
| $\ce{HNO3}$, $\ce{HClO4}$, $\ce{H2SO4}$ | Heavy Group 2: $\ce{Ca(OH)2}$, $\ce{Sr(OH)2}$, $\ce{Ba(OH)2}$ |

Anything **not** on the list is weak, and weak acids do **not** give $[\ce{H+}] =$ concentration (they need $K_a$ — that's the [next article](/chemistry/1002-weak-acids-and-bases)). Strong only, for now.

**Strong bases fully dissociate** the same way — but watch the subscripts. $\ce{NaOH}$ releases one $\ce{OH-}$ per formula unit:

$$\ce{NaOH(s) -> Na+(aq) + OH-(aq)}$$

But $\ce{Ca(OH)2}$ releases **two**:

$$\ce{Ca(OH)2(s) -> Ca^2+(aq) + 2OH-(aq)}$$

So a $0.010$ M $\ce{Ca(OH)2}$ solution has $[\ce{OH-}] = 2 \times 0.010 = 0.020$ M, **not** $0.010$ M. Forgetting that factor of two is the single most common strong-base mistake on the exam, and we'll hit it head-on in the worked examples.

The game plan for **any** strong base: find $[\ce{OH-}]$ (remember the subscript), take pOH $= -\log[\ce{OH-}]$, then pH $= 14 - \text{pOH}$.

### A Few Fine Points

**Dilution.** Adding water spreads the ions out, lowering their concentration. Dilute a strong **acid** and $[\ce{H+}]$ drops, so pH **rises** toward 7. Dilute a strong **base** and $[\ce{OH-}]$ drops, so pH **falls** toward 7. Diluting always nudges you *toward neutral*, never past it.

**The pH-7 limit for dilute acid.** Keep diluting a strong acid — 10×, 100×, a million× — and its pH climbs toward 7 but **can't cross it**. You can't make an acid basic by adding water. (The reason: at extreme dilution the water's own $10^{-7}$ M of $\ce{H+}$ starts to dominate, so it takes over as the floor. A brief conceptual note — you won't compute this in Unit 8.)

**Temperature.** $K_w$ is only $1.0\times10^{-14}$ **at 25°C**. Autoionization is endothermic, so heating water makes more ions, raising $K_w$ and lowering the neutral pH below 7. Neutral water at body temperature is about pH 6.8 — and it's still *neutral*, because $[\ce{H+}]$ still equals $[\ce{OH-}]$. Neutral means "equal," not "exactly 7." On the AP exam, unless told otherwise, assume 25°C and use 14.

---

## Worked Examples

### Example 1: $[\ce{H+}] \to$ pH

**Problem:** A solution has $[\ce{H+}] = 3.5\times10^{-4}$ M. Find its pH.

**Solution:**
- **Step 1:** Apply the definition: $\text{pH} = -\log(3.5\times10^{-4})$.
- **Step 2:** $\log(3.5\times10^{-4}) = -3.46$, so pH $= 3.46$.
- **Step 3:** Sig figs — the concentration has **2** sig figs, so keep **2** digits after the decimal.

**Answer: pH $= 3.46$** (acidic — cabbage would run pink-red).

### Example 2: pH $\to [\ce{H+}]$

**Problem:** A cup of coffee has pH $= 5.00$. Find $[\ce{H+}]$.

**Solution:**
- **Step 1:** Invert the definition. If $\text{pH} = -\log[\ce{H+}]$, then $[\ce{H+}] = 10^{-\text{pH}}$.
- **Step 2:** $[\ce{H+}] = 10^{-5.00} = 1.0\times10^{-5}$ M.
- **Step 3:** pH 5.00 has 2 decimals → 2 sig figs in the concentration. ✓

**Answer: $[\ce{H+}] = 1.0\times10^{-5}$ M.**

### Example 3: The Full Four-Way Interconversion

**Problem:** A solution has $[\ce{H+}] = 2.0\times10^{-3}$ M. Find pH, pOH, and $[\ce{OH-}]$.

**Solution:**
- **Step 1 (pH):** $\text{pH} = -\log(2.0\times10^{-3}) = 2.70$.
- **Step 2 (pOH):** $\text{pOH} = 14.00 - 2.70 = 11.30$.
- **Step 3 ($[\ce{OH-}]$):** $[\ce{OH-}] = 10^{-\text{pOH}} = 10^{-11.30} = 5.0\times10^{-12}$ M.
- **Step 4 (check):** $[\ce{H+}][\ce{OH-}] = (2.0\times10^{-3})(5.0\times10^{-12}) = 1.0\times10^{-14} = K_w$. ✓

**Answer: pH $= 2.70$, pOH $= 11.30$, $[\ce{OH-}] = 5.0\times10^{-12}$ M.** (Strongly acidic — high $\ce{H+}$, vanishing $\ce{OH-}$, exactly the seesaw.)

### Example 4: $[\ce{OH-}] \to$ Everything

**Problem:** A cleaning solution has $[\ce{OH-}] = 4.0\times10^{-3}$ M. Find pOH, pH, and $[\ce{H+}]$.

**Solution:**
- **Step 1 (pOH):** $\text{pOH} = -\log(4.0\times10^{-3}) = 2.40$.
- **Step 2 (pH):** $\text{pH} = 14.00 - 2.40 = 11.60$.
- **Step 3 ($[\ce{H+}]$):** $[\ce{H+}] = 10^{-11.60} = 2.5\times10^{-12}$ M. (Or use $K_w$: $[\ce{H+}] = \frac{10^{-14}}{4.0\times10^{-3}} = 2.5\times10^{-12}$.)

**Answer: pOH $= 2.40$, pH $= 11.60$, $[\ce{H+}] = 2.5\times10^{-12}$ M** (basic — cabbage blue-green).

### Example 5: pH of a Strong Monoprotic Acid

**Problem:** Find the pH of $0.025$ M $\ce{HNO3}$.

**Solution:**
- **Step 1:** $\ce{HNO3}$ is on the strong-acid list and it's monoprotic → it fully ionizes, so $[\ce{H+}] = 0.025$ M.
- **Step 2:** $\text{pH} = -\log(0.025) = 1.60$.
- **Step 3:** $0.025$ has 2 sig figs → 2 decimals. ✓

**Answer: pH $= 1.60$.** No equilibrium, no $K_a$ — strong means you read $[\ce{H+}]$ straight off the concentration.

### Example 6: pH of a Strong Base ($\ce{NaOH}$)

**Problem:** Find the pH of $0.0040$ M $\ce{NaOH}$.

**Solution:**
- **Step 1:** $\ce{NaOH}$ is a strong base, one $\ce{OH-}$ per unit → $[\ce{OH-}] = 0.0040$ M.
- **Step 2:** $\text{pOH} = -\log(0.0040) = 2.40$.
- **Step 3:** $\text{pH} = 14.00 - 2.40 = 11.60$.

**Answer: pH $= 11.60$.**

### Example 7: The $\ce{Ca(OH)2}$ Times-Two Trap

**Problem:** Find the pH of $0.0050$ M $\ce{Ca(OH)2}$.

**Solution:**
- **Step 1:** $\ce{Ca(OH)2}$ is a strong base, but each formula unit releases **two** hydroxides: $\ce{Ca(OH)2 -> Ca^2+ + 2OH-}$.
- **Step 2:** $[\ce{OH-}] = 2 \times 0.0050 = 0.010$ M. (This is the step everyone skips.)
- **Step 3:** $\text{pOH} = -\log(0.010) = 2.00$.
- **Step 4:** $\text{pH} = 14.00 - 2.00 = 12.00$.

**Answer: pH $= 12.00$.** Had you forgotten the 2 and used $[\ce{OH-}] = 0.0050$, you'd have gotten pH $11.70$ — wrong by 0.30, and it's a guaranteed lost point.

### Example 8: Working Backward from pH to Concentration

**Problem:** A strong monoprotic acid solution has pH $= 3.00$. What was the acid's concentration? What is $[\ce{OH-}]$?

**Solution:**
- **Step 1:** $[\ce{H+}] = 10^{-3.00} = 1.0\times10^{-3}$ M. Since the acid is strong and monoprotic, that **is** the acid concentration: $1.0\times10^{-3}$ M.
- **Step 2:** $[\ce{OH-}] = \dfrac{K_w}{[\ce{H+}]} = \dfrac{1.0\times10^{-14}}{1.0\times10^{-3}} = 1.0\times10^{-11}$ M.

**Answer: acid concentration $= 1.0\times10^{-3}$ M; $[\ce{OH-}] = 1.0\times10^{-11}$ M.**

### Example 9: Diluting a Strong Acid

**Problem:** You take $10.0$ mL of $0.10$ M $\ce{HCl}$ and add water up to $100.0$ mL. What is the new pH?

**Solution:**
- **Step 1:** Dilution formula $M_1V_1 = M_2V_2$: $\;M_2 = \dfrac{(0.10)(10.0)}{100.0} = 0.010$ M.
- **Step 2:** $\ce{HCl}$ is strong and monoprotic → $[\ce{H+}] = 0.010$ M.
- **Step 3:** $\text{pH} = -\log(0.010) = 2.00$.
- **Step 4 (sense check):** Original pH was $-\log(0.10) = 1.00$. Diluting 10× raised the pH by exactly **1 unit** — a factor of 10 in $[\ce{H+}]$, one pH unit. The earthquake rule in action.

**Answer: pH $= 2.00$** (up from 1.00, moving toward neutral as expected).

### Example 10: The Sig-Fig Subtlety

**Problem:** Report the pH of $[\ce{H+}] = 6.7\times10^{-9}$ M with correct sig figs, and say whether the solution is acidic or basic.

**Solution:**
- **Step 1:** $\text{pH} = -\log(6.7\times10^{-9}) = 8.17$.
- **Step 2:** 2 sig figs in the concentration → 2 decimals in the pH → **8.17** (the "8" is free, from the $10^{-9}$).
- **Step 3:** pH $> 7$ → **basic**. Sanity check with the seesaw: $[\ce{H+}] = 6.7\times10^{-9}$ is *below* $10^{-7}$, so hydroxide dominates. Basic. ✓

**Answer: pH $= 8.17$, basic** (cabbage would drift blue).

### Example 11: Comparing Acidity with the Factor-of-10 Rule

**Problem:** Lemon juice is about pH 2 and black coffee is about pH 5. How many times more concentrated in $\ce{H+}$ is the lemon juice?

**Solution:**
- **Step 1:** The pH difference is $5 - 2 = 3$ units.
- **Step 2:** Each unit is a factor of 10, so the ratio is $10^3 = 1000$.

**Answer: lemon juice has about $1000\times$ more $\ce{H+}$ than coffee.** A "3 unit" gap on a log scale is a thousandfold gap in reality — never read pH like a ruler.

### Example 12: Which Is More Basic?

**Problem:** Solution A has pOH $= 3.0$; solution B has pH $= 9.0$. Which has the higher $[\ce{OH-}]$?

**Solution:**
- **Step 1 (A):** $[\ce{OH-}]_A = 10^{-3.0} = 1.0\times10^{-3}$ M.
- **Step 2 (B):** pOH$_B = 14.0 - 9.0 = 5.0$, so $[\ce{OH-}]_B = 10^{-5.0} = 1.0\times10^{-5}$ M.
- **Step 3:** $10^{-3} > 10^{-5}$.

**Answer: Solution A** is more basic — its $[\ce{OH-}]$ is $100\times$ higher, even though B's pH "9" *looks* like the bigger number. Convert to a common quantity before comparing.

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Forgetting the **2** in $\ce{Ca(OH)2}$ (also $\ce{Ba(OH)2}$, $\ce{Sr(OH)2}$) | You read the concentration as $[\ce{OH-}]$ directly | Always write the dissociation equation first; count the $\ce{OH-}$ per formula unit |
| Using $[\ce{H+}] =$ concentration for a **weak** acid | The strong-acid formula looks universal | Only strong acids fully ionize. Weak acids need $K_a$ (next article) — check the memorized list first |
| Wrong sig figs: pH "4.7" or "4.699" from $2.0\times10^{-5}$ M | Applying normal sig-fig counting to a log | Sig figs in the number = digits **after** the decimal in the pH; the integer part is free |
| Thinking pH 3 is "twice as acidic" as pH 6 | Treating a log scale as linear | Each unit is $\times 10$; a 3-unit gap is $10^3 = 1000\times$. Earthquakes, not rulers |
| Assuming neutral is *always* pH 7 | Memorizing "7" instead of "$[\ce{H+}]=[\ce{OH-}]$" | Neutral means equal; $K_w$ (and thus 7) is only fixed at 25°C |
| Diluting an acid "past" pH 7 into basic | Extrapolating the dilution trend too far | Water can only push you *toward* 7, never across it |
| Mixing up pH and pOH signs | Both use $-\log$; easy to swap | pH pairs with $[\ce{H+}]$, pOH with $[\ce{OH-}]$; they sum to 14 |

---

## AP Exam Tips

- **Memorize the two master equations:** $K_w = [\ce{H+}][\ce{OH-}] = 1.0\times10^{-14}$ and $\text{pH} + \text{pOH} = 14$ (at 25°C). Half of this unit's questions are one substitution away from these.
- **Strong = fully ionized = one-line pH.** If the problem names a strong acid/base and gives a concentration, $[\ce{H+}]$ (or $[\ce{OH-}]$) *equals* that concentration for monoprotic species — no ICE table, no $K_a$. Recognizing "strong" instantly is the whole trick.
- **The $\ce{Ca(OH)2}$ 2×$\ce{OH-}$ trap is a favorite.** Any Group 2 hydroxide gives **two** hydroxides per unit. Write the dissociation equation so the coefficient can't hide from you.
- **The pH sig-fig rule is a real scoring line.** From a 2-sig-fig concentration, report pH to **2 decimal places**. Zero or one decimal from good data can cost the point on the FRQ.
- **Each pH unit is a factor of 10.** Comparison questions ("how many times more acidic?") are just the pH difference turned into a power of ten — no calculator gymnastics.
- **Watch for "neutral isn't 7" curveballs.** If a problem gives a $K_w$ other than $10^{-14}$ (a hotter temperature), neutral pH is $\frac{1}{2}\text{p}K_w$, not 7. Rare, but it separates the 5s.

---

## Practice Problems

### Problem 1
A solution has $[\ce{H+}] = 8.0\times10^{-6}$ M. Find its pH and state whether it's acidic, neutral, or basic.

<details>
<summary><strong>Solution</strong></summary>

$\text{pH} = -\log(8.0\times10^{-6}) = 5.10$ (2 sig figs → 2 decimals).

pH $< 7$ → **acidic**.

**Answer: pH $= 5.10$, acidic.**

</details>

---

### Problem 2
A solution has pH $= 4.20$. Find $[\ce{H+}]$ with correct sig figs.

<details>
<summary><strong>Solution</strong></summary>

$[\ce{H+}] = 10^{-4.20} = 6.3\times10^{-5}$ M.

pH 4.20 has 2 decimals → 2 sig figs. ✓

**Answer: $[\ce{H+}] = 6.3\times10^{-5}$ M.**

</details>

---

### Problem 3
A solution has $[\ce{OH-}] = 2.5\times10^{-4}$ M. Find pOH, pH, and $[\ce{H+}]$.

<details>
<summary><strong>Solution</strong></summary>

$\text{pOH} = -\log(2.5\times10^{-4}) = 3.60$.

$\text{pH} = 14.00 - 3.60 = 10.40$.

$[\ce{H+}] = 10^{-10.40} = 4.0\times10^{-11}$ M (or $K_w / [\ce{OH-}] = 10^{-14}/2.5\times10^{-4}$).

**Answer: pOH $= 3.60$, pH $= 10.40$, $[\ce{H+}] = 4.0\times10^{-11}$ M.**

</details>

---

### Problem 4
Find the pH of $0.015$ M $\ce{HCl}$.

<details>
<summary><strong>Solution</strong></summary>

$\ce{HCl}$ is strong and monoprotic → $[\ce{H+}] = 0.015$ M.

$\text{pH} = -\log(0.015) = 1.82$.

**Answer: pH $= 1.82$.**

</details>

---

### Problem 5
Find the pH of $0.020$ M $\ce{KOH}$.

<details>
<summary><strong>Solution</strong></summary>

$\ce{KOH}$ is a strong base, one $\ce{OH-}$ per unit → $[\ce{OH-}] = 0.020$ M.

$\text{pOH} = -\log(0.020) = 1.70$.

$\text{pH} = 14.00 - 1.70 = 12.30$.

**Answer: pH $= 12.30$.**

</details>

---

### Problem 6
Find the pH of $0.010$ M $\ce{Ba(OH)2}$.

<details>
<summary><strong>Solution</strong></summary>

$\ce{Ba(OH)2 -> Ba^2+ + 2OH-}$, so $[\ce{OH-}] = 2 \times 0.010 = 0.020$ M.

$\text{pOH} = -\log(0.020) = 1.70$, so $\text{pH} = 14.00 - 1.70 = 12.30$.

**Answer: pH $= 12.30$** (forgetting the 2 would give the wrong 12.00).

</details>

---

### Problem 7
Pure water at some elevated temperature has $K_w = 1.0\times10^{-13}$. What is the neutral pH there? Is the water still neutral?

<details>
<summary><strong>Solution</strong></summary>

Neutral: $[\ce{H+}] = [\ce{OH-}] = x$, so $x^2 = 1.0\times10^{-13}$, giving $x = 3.16\times10^{-7}$ M.

$\text{pH} = -\log(3.16\times10^{-7}) = 6.50$.

It **is** still neutral — $[\ce{H+}] = [\ce{OH-}]$ — even though the pH is 6.50, not 7. Neutral means *equal*, not *7*.

**Answer: neutral pH $= 6.50$; still neutral.**

</details>

---

### Problem 8
You dilute $25.0$ mL of $0.20$ M $\ce{HNO3}$ to a final volume of $250.0$ mL. Find the new pH.

<details>
<summary><strong>Solution</strong></summary>

$M_2 = \dfrac{(0.20)(25.0)}{250.0} = 0.020$ M.

$\ce{HNO3}$ strong, monoprotic → $[\ce{H+}] = 0.020$ M.

$\text{pH} = -\log(0.020) = 1.70$.

(Original pH was $-\log(0.20) = 0.70$; a 10× dilution raised it by exactly 1 unit.)

**Answer: pH $= 1.70$.**

</details>

---

### Problem 9
Milk has pH about 6.5 and household ammonia about pH 11.5. How many times more $\ce{H+}$ is in the milk?

<details>
<summary><strong>Solution</strong></summary>

Difference $= 11.5 - 6.5 = 5$ pH units; each unit is $\times 10$.

Ratio $= 10^5 = 100{,}000$.

**Answer: milk has about $100{,}000\times$ more $\ce{H+}$ than ammonia.**

</details>

---

### Problem 10
A strong monoprotic acid solution has pOH $= 11.40$. Find the acid concentration.

<details>
<summary><strong>Solution</strong></summary>

$\text{pH} = 14.00 - 11.40 = 2.60$.

$[\ce{H+}] = 10^{-2.60} = 2.5\times10^{-3}$ M.

Strong + monoprotic → concentration $= [\ce{H+}] = 2.5\times10^{-3}$ M.

**Answer: $2.5\times10^{-3}$ M.**

</details>

---

### Problem 11
I dip cabbage-juice paper into an unknown and it flashes deep pink. A pH meter reads 2.30. Find $[\ce{H+}]$ and $[\ce{OH-}]$.

<details>
<summary><strong>Solution</strong></summary>

$[\ce{H+}] = 10^{-2.30} = 5.0\times10^{-3}$ M.

$[\ce{OH-}] = \dfrac{K_w}{[\ce{H+}]} = \dfrac{1.0\times10^{-14}}{5.0\times10^{-3}} = 2.0\times10^{-12}$ M.

Deep pink = acidic = high $[\ce{H+}]$, consistent with pH 2.30. ✓

**Answer: $[\ce{H+}] = 5.0\times10^{-3}$ M, $[\ce{OH-}] = 2.0\times10^{-12}$ M.**

</details>

---

### Problem 12
How many sig figs are in each? (a) pH $= 8.20$, (b) pH $= 3.5$, (c) pOH $= 11.400$. Then, does pH 8.20 correspond to an acidic or basic solution?

<details>
<summary><strong>Solution</strong></summary>

Sig figs in a log = digits after the decimal:
- (a) 8.20 → 2 decimals → **2 sig figs**
- (b) 3.5 → 1 decimal → **1 sig fig**
- (c) 11.400 → 3 decimals → **3 sig figs**

pH 8.20 $> 7$ → **basic**.

**Answer: (a) 2, (b) 1, (c) 3; pH 8.20 is basic.**

</details>

---

### Problem 13
A student dissolves $0.0050$ mol of $\ce{Ca(OH)2}$ in enough water to make $500.0$ mL of solution. Find the pH.

<details>
<summary><strong>Solution</strong></summary>

Molarity of $\ce{Ca(OH)2}$: $\dfrac{0.0050\ \text{mol}}{0.5000\ \text{L}} = 0.010$ M.

Each unit gives 2 $\ce{OH-}$: $[\ce{OH-}] = 2 \times 0.010 = 0.020$ M.

$\text{pOH} = -\log(0.020) = 1.70$, so $\text{pH} = 14.00 - 1.70 = 12.30$.

**Answer: pH $= 12.30$.**

</details>

---

### Problem 14
A strong acid solution at pH 3.00 is diluted with water by a factor of 100. Estimate the new pH, and explain why you can't just keep going to pH 9.

<details>
<summary><strong>Solution</strong></summary>

Diluting 100× lowers $[\ce{H+}]$ by $10^2$, raising pH by 2 units: $3.00 + 2.00 = 5.00$.

**Answer: pH $\approx 5.00$.** You can't push a strong acid past pH 7 by dilution — as $[\ce{H+}]$ from the acid drops toward $10^{-7}$, the water's own autoionization ($10^{-7}$ M) becomes the floor and keeps the solution on the acidic side of neutral. Water can only move you toward 7, never across it.

</details>

---

### Problem 15
Rank these by increasing acidity (least to most acidic): Solution A pH $= 9.0$; Solution B $[\ce{H+}] = 1.0\times10^{-3}$ M; Solution C pOH $= 12.0$; Solution D $[\ce{OH-}] = 1.0\times10^{-6}$ M.

<details>
<summary><strong>Solution</strong></summary>

Convert everything to pH:
- A: pH $= 9.0$
- B: pH $= -\log(1.0\times10^{-3}) = 3.0$
- C: pH $= 14.0 - 12.0 = 2.0$
- D: pOH $= -\log(1.0\times10^{-6}) = 6.0$, so pH $= 14.0 - 6.0 = 8.0$

Least acidic = highest pH. Order of increasing acidity: **A (9.0) < D (8.0) < B (3.0) < C (2.0)**.

**Answer: A < D < B < C** (C is most acidic).

</details>

---

## Quick Reference

| Quantity | Definition | Neutral value (25°C) |
|---|---|---|
| $K_w$ | $[\ce{H+}][\ce{OH-}]$ | $1.0\times10^{-14}$ |
| pH | $-\log[\ce{H+}]$ | 7.00 |
| pOH | $-\log[\ce{OH-}]$ | 7.00 |
| pH + pOH | $= 14.00$ | — |
| $[\ce{H+}]$ from pH | $10^{-\text{pH}}$ | $1.0\times10^{-7}$ M |
| $[\ce{OH-}]$ from pOH | $10^{-\text{pOH}}$ | $1.0\times10^{-7}$ M |

| Rule | What to remember |
|---|---|
| Strong monoprotic acid | $[\ce{H+}] =$ concentration |
| Strong base | $[\ce{OH-}] =$ (moles $\ce{OH-}$ per unit) × concentration |
| $\ce{Ca(OH)2}$, $\ce{Ba(OH)2}$, $\ce{Sr(OH)2}$ | $[\ce{OH-}] = 2\times$ concentration |
| Sig figs | decimal places in pH = sig figs in concentration |
| Each pH unit | a factor of 10 in $[\ce{H+}]$ |
| Dilution | moves pH toward 7, never past it |
| Strong acids | $\ce{HCl}$, $\ce{HBr}$, $\ce{HI}$, $\ce{HNO3}$, $\ce{H2SO4}$, $\ce{HClO4}$ |
| Strong bases | Group 1 hydroxides + $\ce{Ca(OH)2}$, $\ce{Sr(OH)2}$, $\ce{Ba(OH)2}$ |

---

<div align="center">

[← Solubility Equilibria](/chemistry/0905-solubility-equilibria) | [Weak Acids and Bases →](/chemistry/1002-weak-acids-and-bases)

</div>
