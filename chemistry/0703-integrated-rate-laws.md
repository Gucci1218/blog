# Integrated Rate Laws and Half-Life
<p class="article-date">July 5, 2026</p>

*This morning I poured myself a can of soda before an early study session — about 200 mg of caffeine, roughly a strong cup of coffee. Here's the wild part I only learned recently: my body doesn't burn through that caffeine at a steady "so-many-milligrams-per-hour" pace. Instead, every 5 hours or so, HALF of whatever is left disappears. Start at 200 mg, and 5 hours later I'm at 100 mg. Five more hours (now 10 hours in): 50 mg. At 15 hours: 25 mg. It keeps halving — 12.5, 6.25 — shrinking forever but never quite hitting zero, which is exactly why the coffee I drink at 4 p.m. is still keeping me up at midnight. That fixed "time to lose half," the same 5 hours no matter where you start, is the unmistakable fingerprint of a **first-order** reaction, and it's the reason doctors can predict drug levels in your blood hours in advance. This article is about turning a rate law into a formula for concentration at any time $t$ — and reading a reaction's order straight off a graph, which is the single most guaranteed graph question on the AP exam.*

---

## What You'll Learn
- Explain what an **integrated rate law** is and how it differs from the rate laws you met last article
- Write and use all three integrated rate laws — **zero**, **first**, and **second** order (they're on the AP formula sheet, so this is about *using* them, not memorizing them)
- Find $[\ce{A}]$ at any time $t$, or the time needed to reach a target concentration, for each order
- Match each order to its **straight-line plot** and read the rate constant $k$ from the slope (the big linearization payoff)
- Determine a reaction's order from a concentration-vs-time **data table** by testing which plot is linear
- Derive and use the three **half-life** formulas, and explain why first-order half-life is *constant*
- Compute how much reactant remains after $n$ half-lives with a fast doubling-down method
- Connect first-order kinetics to **radioactive decay** and carbon-14 dating

---

## Prerequisites
- [Rate Laws](/chemistry/0702-rate-laws) — this article integrates the rate law; you must already know what $k$, the order, and $\text{rate} = k[\ce{A}]^n$ mean
- [Graphing and Linearization](/chemistry/0105-graphing-linearization) — the entire "which plot is straight?" method lives here; slope-and-intercept thinking is the payoff of this whole topic
- [Logarithms for Chemistry](/chemistry/0104-logarithms-for-chemistry) — the first-order law is built on $\ln$, so you need to be comfortable taking and undoing natural logs

---

## The Core Concept

### Intuition First

Back in [Rate Laws](/chemistry/0702-rate-laws), a rate law told us how *fast* a reaction goes at a given instant: $\text{rate} = k[\ce{A}]^n$. That's a snapshot. It answers "how fast right now?" but not the question you actually care about with caffeine: **"how much is left at 11 p.m.?"**

To answer that, we need to add up all those instantaneous rates over time — which is exactly what "integrated" means. An **integrated rate law** takes the instantaneous rate law and turns it into a formula that gives concentration *as a function of time*: plug in $t$, get $[\ce{A}]_t$. (If you've done calculus, we literally integrate the differential rate law. If you haven't, no worries — the AP exam hands you the finished formulas.)

Here's the caffeine picture, made precise. Let $[\ce{A}]$ stand for the caffeine still in your bloodstream. The reason it halves on a fixed schedule is that caffeine clearance is **first order**: the rate at which it leaves is proportional to how much is there. Lots of caffeine → cleared fast. A little caffeine → cleared slowly. So the curve starts steep and flattens out, chasing zero but never arriving:

| Time (hours) | Caffeine left (mg) | What happened |
|---|---|---|
| 0 | 200 | you drink the soda |
| 5 | 100 | half gone |
| 10 | 50 | half of *that* gone |
| 15 | 25 | half again |
| 20 | 12.5 | and again... |

That constant **5-hour "time to lose half"** — the same whether you start at 200 mg or 100 mg or 25 mg — is called the **half-life**, $t_{1/2}$. The fact that it *doesn't* depend on how much you start with is the signature of first order, and it's the star of this whole article.

Now the structural map, so the story lines up with the math:

| Caffeine story | Kinetics concept |
|---|---|
| amount of caffeine in your body | concentration $[\ce{A}]$ |
| the fixed 5-hour "time to halve" | constant half-life $t_{1/2}$ |
| the smooth decay curve | the first-order integrated rate law |
| shrinking forever, never hitting zero | exponential decay |

But not every reaction is first order. Some clear at a *constant* rate regardless of concentration (zero order — think a bar with unlimited demand serving drinks as fast as the bartender can pour). Some slow down even more dramatically than caffeine (second order). Each order has its own integrated law, its own graph, and its own half-life behavior — and telling them apart from data is the skill AP loves to test.

### The Three Integrated Rate Laws

For a reaction $\ce{A -> products}$, here are all three. **The AP exam gives you every one of these on the formula sheet** — your job is to pick the right one and use it, not to recall it from memory.

**Zero order** — rate doesn't depend on $[\ce{A}]$ at all:

$$[\ce{A}]_t = [\ce{A}]_0 - kt$$

**First order** — rate is proportional to $[\ce{A}]$ (the caffeine case):

$$\ln[\ce{A}]_t = \ln[\ce{A}]_0 - kt$$

**Second order** — rate is proportional to $[\ce{A}]^2$:

$$\frac{1}{[\ce{A}]_t} = \frac{1}{[\ce{A}]_0} + kt$$

Notice the family resemblance: each one has the shape $y = (\text{start}) \pm kt$. That's not a coincidence — it's the key to the whole linearization trick. Each law is *already* a straight line $y = mx + b$ if you choose the right thing to put on the $y$-axis.

### The Master Table (the linearization payoff)

This is the table to burn into your memory — it turns [Graphing and Linearization](/chemistry/0105-graphing-linearization) into free points. Whichever of the three plots comes out as a **straight line** tells you the order, and the **slope** of that line hands you $k$.

| Order | Rate law | Integrated law | **Linear plot** ($y$ vs $x$) | Slope | $y$-intercept |
|---|---|---|---|---|---|
| Zero | $\text{rate}=k$ | $[\ce{A}]_t = [\ce{A}]_0 - kt$ | $[\ce{A}]$ vs $t$ | $-k$ | $[\ce{A}]_0$ |
| First | $\text{rate}=k[\ce{A}]$ | $\ln[\ce{A}]_t = \ln[\ce{A}]_0 - kt$ | $\ln[\ce{A}]$ vs $t$ | $-k$ | $\ln[\ce{A}]_0$ |
| Second | $\text{rate}=k[\ce{A}]^2$ | $\dfrac{1}{[\ce{A}]_t} = \dfrac{1}{[\ce{A}]_0} + kt$ | $\dfrac{1}{[\ce{A}]}$ vs $t$ | $+k$ | $\dfrac{1}{[\ce{A}]_0}$ |

Two things graders love to test hidden in that last column:

- **Zero and first order have a *negative* slope** ($-k$) because $[\ce{A}]$ is falling.
- **Second order has a *positive* slope** ($+k$) because as $[\ce{A}]$ drops, $\frac{1}{[\ce{A}]}$ *rises*. So for second order you read $k$ straight off the slope; for zero and first, $k$ is the *negative* of the slope.

### The Three Half-Life Formulas

The **half-life** $t_{1/2}$ is the time for concentration to fall to half its starting value. Set $[\ce{A}]_t = \tfrac{1}{2}[\ce{A}]_0$ in each integrated law and solve — you get three very different personalities. These are also on the formula sheet.

$$\underbrace{t_{1/2} = \frac{[\ce{A}]_0}{2k}}_{\text{zero order}} \qquad \underbrace{t_{1/2} = \frac{0.693}{k}}_{\text{first order}} \qquad \underbrace{t_{1/2} = \frac{1}{k[\ce{A}]_0}}_{\text{second order}}$$

Read the role of $[\ce{A}]_0$ in each — this is the whole conceptual game:

- **Zero order:** $t_{1/2} \propto [\ce{A}]_0$. Start with more, and each halving takes *longer*. As the reaction proceeds, successive half-lives get *shorter*.
- **First order:** $[\ce{A}]_0$ **isn't in the formula at all.** The half-life is constant — the same 5 hours forever. This is the caffeine fingerprint. (Where does $0.693$ come from? It's $\ln 2$. Solving $\ln\frac{1}{2} = -kt_{1/2}$ gives $t_{1/2} = \frac{\ln 2}{k} = \frac{0.693}{k}$.)
- **Second order:** $t_{1/2} \propto \frac{1}{[\ce{A}]_0}$. As $[\ce{A}]$ drops, each successive half-life takes *longer and longer* — the reaction crawls to a halt.

> **🎬 Hollywood Chemistry: Real or Not?**
> *The scene:* In countless documentaries, scientists carbon-date a bone or a scroll and announce its age to the year.
> *The verdict:* Real chemistry, and it's *this exact math*. Living things absorb radioactive carbon-14; when they die, that $\ce{^{14}_{6}C}$ decays first-order with a constant half-life of 5730 years. Because half-life is concentration-independent (first order!), the fraction of $\ce{^{14}_{6}C}$ left is a clean clock: one half-life gone → 50% left, two → 25%, and so on. The "to the year" precision is the Hollywood exaggeration — real dates come with error bars — but the halving-on-a-schedule is completely legit, and it's the same physics as the caffeine in your blood.

---

## Worked Examples

### Example 1: First-Order Concentration at Time $t$ (the caffeine calc)

**Problem:** Caffeine clears from the body by first-order kinetics with $k = 0.14~\text{hr}^{-1}$. If you start with a blood concentration equivalent to $[\ce{A}]_0 = 200~\text{units}$, what's left after 8 hours?

**Solution:**

Step 1 — pick the first-order law: $\ln[\ce{A}]_t = \ln[\ce{A}]_0 - kt$.

Step 2 — plug in:
$$\ln[\ce{A}]_t = \ln(200) - (0.14)(8) = 5.298 - 1.12 = 4.178$$

Step 3 — undo the log by exponentiating:
$$[\ce{A}]_t = e^{4.178} = 65.2~\text{units}$$

**Answer:** About **65 units** remain after 8 hours.

### Example 2: Finding the Time to Reach a Target (First Order)

**Problem:** Using the same caffeine constant $k = 0.14~\text{hr}^{-1}$ and $[\ce{A}]_0 = 200$, how long until you're down to 25 units — roughly the level where most people can fall asleep?

**Solution:**

Step 1 — first-order law, solve for $t$:
$$\ln[\ce{A}]_t = \ln[\ce{A}]_0 - kt \;\Rightarrow\; t = \frac{\ln[\ce{A}]_0 - \ln[\ce{A}]_t}{k}$$

Step 2 — substitute:
$$t = \frac{\ln(200) - \ln(25)}{0.14} = \frac{5.298 - 3.219}{0.14} = \frac{2.079}{0.14}$$

Step 3 — divide:
$$t = 14.85~\text{hr}$$

**Answer:** About **15 hours** — a 4 p.m. coffee is still buzzing at 7 a.m.

### Example 3: Finding $k$ from a Half-Life

**Problem:** The caffeine half-life is measured at 5.0 hours. Find the first-order rate constant $k$.

**Solution:**

Step 1 — first-order half-life formula: $t_{1/2} = \dfrac{0.693}{k}$.

Step 2 — solve for $k$:
$$k = \frac{0.693}{t_{1/2}} = \frac{0.693}{5.0~\text{hr}}$$

Step 3:
$$k = 0.139~\text{hr}^{-1}$$

**Answer:** $k \approx \mathbf{0.14~\text{hr}^{-1}}$ — matching the value we used above. Notice we never needed a starting concentration; first-order $k$ and $t_{1/2}$ are locked together no matter the dose.

### Example 4: The "How Much After $n$ Half-Lives" Fast Method

**Problem:** A radioactive isotope has $t_{1/2} = 8.0$ days. A sample starts at $80~\text{mg}$. How much remains after 32 days?

**Solution:**

Step 1 — count the half-lives: $n = \dfrac{32~\text{days}}{8.0~\text{days}} = 4$ half-lives.

Step 2 — halve four times (just divide by 2 repeatedly):
$$80 \to 40 \to 20 \to 10 \to 5~\text{mg}$$

Or use the formula directly:
$$[\ce{A}]_t = [\ce{A}]_0 \left(\tfrac{1}{2}\right)^n = 80\left(\tfrac{1}{2}\right)^4 = 80 \times \tfrac{1}{16} = 5~\text{mg}$$

**Answer:** **5 mg** remain. When $t$ is a whole number of half-lives, don't touch the log formula — just halve.

### Example 5: Determine the Order from Data (the money problem)

**Problem:** The decomposition of $\ce{N2O5}$ is followed over time:

| $t$ (s) | $[\ce{N2O5}]$ (M) | $\ln[\ce{N2O5}]$ | $1/[\ce{N2O5}]$ |
|---|---|---|---|
| 0 | 0.100 | $-2.303$ | 10.0 |
| 50 | 0.0707 | $-2.649$ | 14.1 |
| 100 | 0.0500 | $-2.996$ | 20.0 |
| 150 | 0.0354 | $-3.342$ | 28.2 |
| 200 | 0.0250 | $-3.689$ | 40.0 |

Find the order and the rate constant $k$.

**Solution:**

Step 1 — test each column for a **constant** rate of change (that's what "linear vs $t$" means; each step here is $\Delta t = 50~\text{s}$).

- $[\ce{N2O5}]$ column: drops by 0.0293, then 0.0207, then 0.0146... **not** constant → not zero order.
- $\ln[\ce{N2O5}]$ column: changes by $-0.346$, $-0.347$, $-0.346$, $-0.347$ → **constant!** → first order.
- $1/[\ce{N2O5}]$ column: changes by 4.1, 5.9, 8.2... not constant → not second order.

Step 2 — the $\ln[\ce{A}]$-vs-$t$ plot is the straight one, so it's **first order**. Slope $= -k$:
$$\text{slope} = \frac{-3.689 - (-2.303)}{200 - 0} = \frac{-1.386}{200} = -6.93\times10^{-3}~\text{s}^{-1}$$

Step 3 — $k = -\text{slope} = 6.93\times10^{-3}~\text{s}^{-1}$.

**Answer:** The reaction is **first order** with $k = 6.93\times10^{-3}~\text{s}^{-1}$. (Sanity check: $t_{1/2} = 0.693/k = 100~\text{s}$, and sure enough $[\ce{N2O5}]$ falls from 0.100 to 0.050 M in exactly 100 s.)

### Example 6: Zero-Order Concentration and Half-Life

**Problem:** A zero-order reaction has $k = 0.025~\text{M/s}$ and $[\ce{A}]_0 = 0.50~\text{M}$. Find $[\ce{A}]$ after 10 s, and find the half-life.

**Solution:**

Step 1 — zero-order law: $[\ce{A}]_t = [\ce{A}]_0 - kt$.
$$[\ce{A}]_{10} = 0.50 - (0.025)(10) = 0.50 - 0.25 = 0.25~\text{M}$$

Step 2 — half-life: $t_{1/2} = \dfrac{[\ce{A}]_0}{2k} = \dfrac{0.50}{2(0.025)} = 10~\text{s}$.

**Answer:** $[\ce{A}] = \mathbf{0.25~M}$ after 10 s, and $t_{1/2} = \mathbf{10~s}$. Note these agree — half of 0.50 M is 0.25 M — and that this half-life *depends* on the 0.50 M start.

### Example 7: Second-Order Concentration at Time $t$

**Problem:** A second-order reaction has $k = 0.20~\text{M}^{-1}\text{s}^{-1}$ and $[\ce{A}]_0 = 0.40~\text{M}$. Find $[\ce{A}]$ after 30 s.

**Solution:**

Step 1 — second-order law: $\dfrac{1}{[\ce{A}]_t} = \dfrac{1}{[\ce{A}]_0} + kt$.

Step 2 — plug in:
$$\frac{1}{[\ce{A}]_t} = \frac{1}{0.40} + (0.20)(30) = 2.5 + 6.0 = 8.5~\text{M}^{-1}$$

Step 3 — flip to get the concentration:
$$[\ce{A}]_t = \frac{1}{8.5} = 0.118~\text{M}$$

**Answer:** $[\ce{A}] \approx \mathbf{0.12~M}$. Watch the trap: the law gives you $\frac{1}{[\ce{A}]}$, so you must take the reciprocal at the end.

### Example 8: Second-Order Half-Life Grows

**Problem:** For the reaction in Example 7 ($k = 0.20~\text{M}^{-1}\text{s}^{-1}$, $[\ce{A}]_0 = 0.40~\text{M}$), find the first half-life, then the half-life of the *next* halving.

**Solution:**

Step 1 — first half-life uses $[\ce{A}]_0 = 0.40~\text{M}$:
$$t_{1/2} = \frac{1}{k[\ce{A}]_0} = \frac{1}{(0.20)(0.40)} = 12.5~\text{s}$$

Step 2 — after that halving, the new starting concentration is $0.20~\text{M}$:
$$t_{1/2}' = \frac{1}{(0.20)(0.20)} = 25~\text{s}$$

**Answer:** The first half-life is **12.5 s**, the next is **25 s** — it *doubled*. Second-order reactions drag out more and more as they proceed, the opposite of the constant first-order clock.

### Example 9: Finding $k$ from Two Data Points (First Order)

**Problem:** A first-order reaction has $[\ce{A}] = 0.800~\text{M}$ at $t = 0$ and $[\ce{A}] = 0.200~\text{M}$ at $t = 60~\text{s}$. Find $k$.

**Solution:**

Step 1 — first-order law rearranged:
$$k = \frac{\ln[\ce{A}]_0 - \ln[\ce{A}]_t}{t} = \frac{1}{t}\ln\frac{[\ce{A}]_0}{[\ce{A}]_t}$$

Step 2 — substitute:
$$k = \frac{1}{60}\ln\frac{0.800}{0.200} = \frac{1}{60}\ln(4) = \frac{1.386}{60}$$

Step 3:
$$k = 0.0231~\text{s}^{-1}$$

**Answer:** $k = \mathbf{0.023~s^{-1}}$. (Shortcut check: $0.800 \to 0.400 \to 0.200$ is exactly 2 half-lives in 60 s, so $t_{1/2} = 30~\text{s}$ and $k = 0.693/30 = 0.0231~\text{s}^{-1}$. )

### Example 10: Carbon-14 Dating (First Order in the Wild)

**Problem:** $\ce{^{14}_{6}C}$ decays first-order with $t_{1/2} = 5730~\text{yr}$. A wooden artifact has 25% of the $\ce{^{14}_{6}C}$ a living tree would have. How old is it?

**Solution:**

Step 1 — 25% left means two halvings ($100\% \to 50\% \to 25\%$), so $n = 2$ half-lives.

Step 2 — age $= n \times t_{1/2} = 2 \times 5730 = 11{,}460~\text{yr}$.

(General method for a non-whole number: $k = \frac{0.693}{5730} = 1.21\times10^{-4}~\text{yr}^{-1}$, then $t = \frac{1}{k}\ln\frac{100}{25} = \frac{\ln 4}{1.21\times10^{-4}} = 11{,}500~\text{yr}$ — same answer.)

**Answer:** About **11,500 years old**. Because half-life is concentration-independent, the *fraction* remaining is all you need — the same reason the caffeine clock works.

### Example 11: Reading $k$ Straight Off a Graph

**Problem:** For a reaction $\ce{A -> products}$, a plot of $\dfrac{1}{[\ce{A}]}$ vs $t$ is a straight line with slope $+0.045~\text{M}^{-1}\text{s}^{-1}$ and $y$-intercept $2.0~\text{M}^{-1}$. State the order, $k$, and $[\ce{A}]_0$.

**Solution:**

Step 1 — the *straight* plot is $\frac{1}{[\ce{A}]}$ vs $t$ → **second order** (master table).

Step 2 — for second order, slope $= +k$, so $k = 0.045~\text{M}^{-1}\text{s}^{-1}$.

Step 3 — the intercept is $\frac{1}{[\ce{A}]_0} = 2.0~\text{M}^{-1}$, so $[\ce{A}]_0 = \frac{1}{2.0} = 0.50~\text{M}$.

**Answer:** **Second order**, $k = 0.045~\text{M}^{-1}\text{s}^{-1}$, $[\ce{A}]_0 = 0.50~\text{M}$.

### Example 12: Percent Remaining After a Given Time (First Order)

**Problem:** A drug clears first-order with $k = 0.30~\text{hr}^{-1}$. What percentage of the dose remains after 4.0 hours?

**Solution:**

Step 1 — use the ratio form of the first-order law:
$$\ln\frac{[\ce{A}]_t}{[\ce{A}]_0} = -kt = -(0.30)(4.0) = -1.20$$

Step 2 — exponentiate:
$$\frac{[\ce{A}]_t}{[\ce{A}]_0} = e^{-1.20} = 0.301$$

**Answer:** About **30%** of the dose is left after 4 hours. Working with the *ratio* means you never need the actual starting amount.

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Using the wrong integrated law | Three formulas look similar | First identify the **order** (from the graph/data or the problem), *then* pick the matching law |
| Forgetting to flip the second-order result | The law gives $\frac{1}{[\ce{A}]}$, not $[\ce{A}]$ | After solving, always ask "did I compute a reciprocal?" and take $1/x$ at the end |
| Sign error on the slope | Zero/first have slope $-k$, second has $+k$ | Remember: falling quantities ($[\ce{A}]$, $\ln[\ce{A}]$) give negative slopes; the *rising* $\frac{1}{[\ce{A}]}$ gives positive |
| Assuming half-life is always constant | The caffeine story makes "constant" feel universal | Constant $t_{1/2}$ is a **first-order-only** property; zero and second order have changing half-lives |
| Mixing up $\ln$ and $\log$ | The formula uses natural log | The first-order law always uses $\ln$ (base $e$); using $\log_{10}$ gives an answer off by a factor of 2.303 |
| Plugging a non-whole $t$ into "halve repeatedly" | The shortcut only works for whole numbers of half-lives | Use $\left(\tfrac12\right)^n$ or the halving trick **only** when $n$ is an integer; otherwise use the log formula |
| Units on $k$ ignored | All three $k$'s have different units | Zero: $\text{M/s}$; first: $\text{s}^{-1}$; second: $\text{M}^{-1}\text{s}^{-1}$ — the units alone reveal the order |

---

## AP Exam Tips

- **Match order to the linear plot — this is a guaranteed graph question.** You will be handed a set of axes or a "which plot is straight?" prompt. Memorize the master table cold: $[\ce{A}]$ vs $t$ (zero), $\ln[\ce{A}]$ vs $t$ (first), $\frac{1}{[\ce{A}]}$ vs $t$ (second).
- **First-order half-life is concentration-INDEPENDENT** — this is the single most-tested conceptual fact in the topic. If a problem says "the half-life is the same regardless of starting concentration," the answer is *first order*, full stop.
- **The formulas are given, but choosing is on you.** The AP formula sheet lists all three integrated laws and half-life formulas. You lose points not by forgetting them but by grabbing the wrong one — so nail down the order first.
- **Watch the slope signs.** For zero and first order, $k = -\text{slope}$. For second order, $k = +\text{slope}$. A student who reports a negative $k$ has almost certainly dropped a sign.
- **$\ln$ vs $\frac{1}{[\ce{A}]}$ is the classic distractor.** Both give "curved-then-straight" transformations; don't confuse the first-order log plot with the second-order reciprocal plot.
- **Show the ratio form** $\ln\frac{[\ce{A}]_t}{[\ce{A}]_0} = -kt$ on FRQs — it earns setup points even before you compute.
- **Half-life shortcuts save time:** for whole numbers of half-lives, halve repeatedly instead of reaching for the calculator and $\ln$.

---

## Practice Problems

### Problem 1
A first-order reaction has $k = 0.050~\text{s}^{-1}$ and $[\ce{A}]_0 = 1.0~\text{M}$. What is $[\ce{A}]$ after 20 s?

<details>
<summary><strong>Solution</strong></summary>

$\ln[\ce{A}]_t = \ln(1.0) - (0.050)(20) = 0 - 1.0 = -1.0$, so $[\ce{A}]_t = e^{-1.0} = 0.368~\text{M}$.

**Answer: $[\ce{A}] = 0.37~\text{M}$.**

</details>

---

### Problem 2
The half-life of a first-order reaction is 40 s. Find the rate constant $k$.

<details>
<summary><strong>Solution</strong></summary>

$k = \dfrac{0.693}{t_{1/2}} = \dfrac{0.693}{40} = 0.0173~\text{s}^{-1}$.

**Answer: $k = 0.017~\text{s}^{-1}$.**

</details>

---

### Problem 3
A radioactive sample of $\ce{^{131}_{53}I}$ ($t_{1/2} = 8.0~\text{days}$) starts at $160~\text{mg}$. How much remains after 24 days?

<details>
<summary><strong>Solution</strong></summary>

$n = 24/8.0 = 3$ half-lives. Halve three times: $160 \to 80 \to 40 \to 20~\text{mg}$. (Or $160(\tfrac12)^3 = 160/8 = 20$.)

**Answer: $20~\text{mg}$.**

</details>

---

### Problem 4
The following data are collected for $\ce{A -> products}$:

| $t$ (s) | 0 | 20 | 40 | 60 |
|---|---|---|---|---|
| $[\ce{A}]$ (M) | 0.500 | 0.400 | 0.300 | 0.200 |

Determine the order and $k$.

<details>
<summary><strong>Solution</strong></summary>

$[\ce{A}]$ drops by a constant 0.100 M every 20 s → the $[\ce{A}]$-vs-$t$ plot is straight → **zero order**.

Slope $= \dfrac{0.200 - 0.500}{60 - 0} = \dfrac{-0.300}{60} = -5.0\times10^{-3}~\text{M/s}$, so $k = 5.0\times10^{-3}~\text{M/s}$.

**Answer: zero order, $k = 5.0\times10^{-3}~\text{M/s}$.**

</details>

---

### Problem 5
A second-order reaction has $k = 0.10~\text{M}^{-1}\text{s}^{-1}$ and $[\ce{A}]_0 = 0.25~\text{M}$. Find $[\ce{A}]$ after 40 s.

<details>
<summary><strong>Solution</strong></summary>

$\dfrac{1}{[\ce{A}]_t} = \dfrac{1}{0.25} + (0.10)(40) = 4.0 + 4.0 = 8.0~\text{M}^{-1}$. Flip: $[\ce{A}]_t = 1/8.0 = 0.125~\text{M}$.

**Answer: $[\ce{A}] = 0.13~\text{M}$.**

</details>

---

### Problem 6
Caffeine clears first-order with $t_{1/2} = 5.0~\text{hr}$. Starting at 300 mg, how much is left after 15 hours — without a calculator?

<details>
<summary><strong>Solution</strong></summary>

$15~\text{hr} = 3$ half-lives. Halve three times: $300 \to 150 \to 75 \to 37.5~\text{mg}$.

**Answer: $37.5~\text{mg}$.**

</details>

---

### Problem 7
A first-order reaction goes from $0.600~\text{M}$ to $0.150~\text{M}$ in 90 s. Find $k$ and the half-life.

<details>
<summary><strong>Solution</strong></summary>

$k = \dfrac{1}{90}\ln\dfrac{0.600}{0.150} = \dfrac{\ln 4}{90} = \dfrac{1.386}{90} = 0.0154~\text{s}^{-1}$.

$t_{1/2} = \dfrac{0.693}{0.0154} = 45~\text{s}$. (Check: $0.600 \to 0.300 \to 0.150$ is 2 half-lives in 90 s.)

**Answer: $k = 0.015~\text{s}^{-1}$, $t_{1/2} = 45~\text{s}$.**

</details>

---

### Problem 8
For a reaction, a plot of $\ln[\ce{A}]$ vs $t$ is linear with slope $-0.012~\text{s}^{-1}$. What is the order, and what is $k$?

<details>
<summary><strong>Solution</strong></summary>

Linear $\ln[\ce{A}]$-vs-$t$ plot → **first order**. Slope $= -k$, so $k = 0.012~\text{s}^{-1}$.

**Answer: first order, $k = 0.012~\text{s}^{-1}$.**

</details>

---

### Problem 9
A zero-order reaction has $k = 0.030~\text{M/s}$ and $[\ce{A}]_0 = 0.60~\text{M}$. How long until $[\ce{A}] = 0$? What is $t_{1/2}$?

<details>
<summary><strong>Solution</strong></summary>

$[\ce{A}]_t = [\ce{A}]_0 - kt$. Set to 0: $t = \dfrac{[\ce{A}]_0}{k} = \dfrac{0.60}{0.030} = 20~\text{s}$.

$t_{1/2} = \dfrac{[\ce{A}]_0}{2k} = \dfrac{0.60}{0.060} = 10~\text{s}$.

**Answer: reaches 0 at 20 s; $t_{1/2} = 10~\text{s}$.**

</details>

---

### Problem 10
The data below are for $\ce{2NO2 -> 2NO + O2}$:

| $t$ (s) | $[\ce{NO2}]$ (M) | $1/[\ce{NO2}]$ (M$^{-1}$) |
|---|---|---|
| 0 | 0.0100 | 100 |
| 60 | 0.00625 | 160 |
| 120 | 0.00455 | 220 |
| 180 | 0.00357 | 280 |

Determine the order and $k$.

<details>
<summary><strong>Solution</strong></summary>

$1/[\ce{NO2}]$ rises by a constant 60 M$^{-1}$ every 60 s → the $\frac{1}{[\ce{A}]}$-vs-$t$ plot is straight → **second order**.

Slope $= \dfrac{280 - 100}{180 - 0} = \dfrac{180}{180} = 1.0~\text{M}^{-1}\text{s}^{-1} = +k$.

**Answer: second order, $k = 1.0~\text{M}^{-1}\text{s}^{-1}$.**

</details>

---

### Problem 11
A drug is eliminated first-order with $k = 0.25~\text{hr}^{-1}$. What fraction of a dose remains after 6.0 hours?

<details>
<summary><strong>Solution</strong></summary>

$\ln\dfrac{[\ce{A}]_t}{[\ce{A}]_0} = -kt = -(0.25)(6.0) = -1.5$. So $\dfrac{[\ce{A}]_t}{[\ce{A}]_0} = e^{-1.5} = 0.223$.

**Answer: about 22% remains.**

</details>

---

### Problem 12
An artifact contains 12.5% of the $\ce{^{14}_{6}C}$ found in living material ($t_{1/2} = 5730~\text{yr}$). How old is it?

<details>
<summary><strong>Solution</strong></summary>

$12.5\% = \tfrac{1}{8} = \left(\tfrac12\right)^3$, so $n = 3$ half-lives. Age $= 3 \times 5730 = 17{,}190~\text{yr}$.

**Answer: about 17,200 years.**

</details>

---

### Problem 13
Two reactions each start at $[\ce{A}]_0 = 0.40~\text{M}$. Reaction X is first order ($k = 0.10~\text{s}^{-1}$); reaction Y is second order ($k = 0.10~\text{M}^{-1}\text{s}^{-1}$). Which has the shorter first half-life?

<details>
<summary><strong>Solution</strong></summary>

X (first order): $t_{1/2} = \dfrac{0.693}{0.10} = 6.93~\text{s}$.

Y (second order): $t_{1/2} = \dfrac{1}{(0.10)(0.40)} = 25~\text{s}$.

**Answer: Reaction X (first order) has the shorter half-life, 6.9 s vs 25 s.**

</details>

---

### Problem 14
A first-order reaction is 75% complete in 60 s. Find $k$.

<details>
<summary><strong>Solution</strong></summary>

75% complete → 25% remains, so $\dfrac{[\ce{A}]_t}{[\ce{A}]_0} = 0.25$.

$k = \dfrac{1}{t}\ln\dfrac{[\ce{A}]_0}{[\ce{A}]_t} = \dfrac{1}{60}\ln(4) = \dfrac{1.386}{60} = 0.0231~\text{s}^{-1}$.

(Check: 25% left = 2 half-lives, so $t_{1/2} = 30~\text{s}$, $k = 0.693/30 = 0.0231~\text{s}^{-1}$.)

**Answer: $k = 0.023~\text{s}^{-1}$.**

</details>

---

### Problem 15
A reaction's half-life *doubles* each time the concentration halves. What is the order? Explain using a half-life formula.

<details>
<summary><strong>Solution</strong></summary>

$t_{1/2}$ growing as $[\ce{A}]$ falls points to **second order**, where $t_{1/2} = \dfrac{1}{k[\ce{A}]_0}$. Since $t_{1/2} \propto \dfrac{1}{[\ce{A}]_0}$, halving $[\ce{A}]_0$ exactly doubles the half-life.

**Answer: second order.** (First order would keep $t_{1/2}$ constant; zero order would *halve* it.)

</details>

---

## Quick Reference

| Order | Integrated law | Linear plot | Slope | Half-life | $k$ units |
|---|---|---|---|---|---|
| **0** | $[\ce{A}]_t = [\ce{A}]_0 - kt$ | $[\ce{A}]$ vs $t$ | $-k$ | $t_{1/2} = \dfrac{[\ce{A}]_0}{2k}$ (shrinks) | $\text{M/s}$ |
| **1** | $\ln[\ce{A}]_t = \ln[\ce{A}]_0 - kt$ | $\ln[\ce{A}]$ vs $t$ | $-k$ | $t_{1/2} = \dfrac{0.693}{k}$ (constant) | $\text{s}^{-1}$ |
| **2** | $\dfrac{1}{[\ce{A}]_t} = \dfrac{1}{[\ce{A}]_0} + kt$ | $\dfrac{1}{[\ce{A}]}$ vs $t$ | $+k$ | $t_{1/2} = \dfrac{1}{k[\ce{A}]_0}$ (grows) | $\text{M}^{-1}\text{s}^{-1}$ |

**Key ideas:**
- Whole number of half-lives? Just halve repeatedly: $[\ce{A}]_t = [\ce{A}]_0\left(\tfrac12\right)^n$.
- **First-order half-life is constant** — the caffeine/carbon-14 fingerprint.
- Identify order from **which plot is straight**, then read $k$ from the slope (sign matters!).
- Ratio form for first order: $\ln\dfrac{[\ce{A}]_t}{[\ce{A}]_0} = -kt$.

---

<div align="center">

[← Rate Laws](/chemistry/0702-rate-laws) | [Collision Model and Arrhenius →](/chemistry/0704-collision-model-arrhenius)

</div>
