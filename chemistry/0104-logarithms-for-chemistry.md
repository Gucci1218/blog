# Logarithms for Chemistry
<p class="article-date">July 4, 2026</p>

*Everyone in San Diego has an earthquake story. Mine: I was doing homework at the kitchen table when everything did a little shimmy — a 4.2 centered out near Julian, barely enough to rattle my water glass. But here's the thing that messes with people: a 5.2 wouldn't have been "one notch worse." It would have been **ten times** the shaking, and a 6.2 would have been a hundred times. Earthquake magnitude is a logarithmic scale — each step of 1 means multiply by 10 — because the actual energy numbers run away so fast that raw units become useless. Chemistry has the exact same problem: hydrogen ion concentrations span from about $10^{-1}$ M in stomach acid down to $10^{-14}$ M in drain cleaner, thirteen powers of ten, and pH squashes that absurd range into a humane 1-to-14. The trick in both cases is identical: instead of counting units, a log scale counts **zeros**. Master that one idea and pH, pKa, pOH, first-order kinetics, and half the AP Chemistry formula sheet stop being mysterious symbols and become one skill you already have.*

---

## What You'll Learn

- Explain what $\log_{10} x$ actually asks ("10 to what power gives $x$?") and evaluate logs of powers of ten in your head
- Use the product, quotient, and power rules for logarithms on real chemistry numbers
- Undo a log with an antilog: solve equations like $-\log x = 4.7$ for $x$
- Convert between $\ln$ and $\log$ using $\ln x = 2.303 \log x$, and know which one shows up where in AP Chemistry
- Run the pH workflow in **both** directions: $\text{pH} = -\log[\ce{H+}]$ and $[\ce{H+}] = 10^{-\text{pH}}$
- Apply the special sig-fig rule for logarithms (only digits *after* the decimal count)
- Estimate pH from $[\ce{H+}]$ without a calculator — a skill AP multiple choice tests directly
- Recognize the log/ln machinery hiding inside first-order kinetics and the Arrhenius equation before you meet them formally

---

## Prerequisites

- [Scientific Notation](/chemistry/0101-scientific-notation) — logs and powers of ten are two sides of the same coin; you need to be fluent in $a \times 10^{n}$ form first

A note before we start: I already know logarithms from calculus — we differentiated $\ln x$ and integrated $\frac{1}{x}$ all year. This article is the **chemistry-flavored refresher**: the same math, but pointed at pH, concentrations, and the specific calculator-and-sig-fig habits the AP Chemistry exam expects. If logs are brand new to you, read slowly; if they're old friends, watch for the chemistry-specific traps (especially the sig-fig rule — nobody teaches it until it costs you points).

---

## The Core Concept

### Intuition First

Back to the earthquake. When a seismologist says "magnitude 6," they are not reporting the shaking directly — they're reporting the **exponent** of the shaking. Magnitude 6 means the ground motion is about $10^6$ times some reference wiggle. The scale doesn't count units of shaking; it counts *zeros*.

That's all a logarithm is. The expression $\log_{10} x$ asks one question:

> **"10 raised to what power gives me $x$?"**

- $\log 1000 = 3$, because $10^3 = 1000$. (Three zeros.)
- $\log 0.001 = -3$, because $10^{-3} = 0.001$. (Three hops *down* from 1.)
- $\log 1 = 0$, because $10^0 = 1$. (Zero hops.)

The log function and the function $10^x$ are inverses — each one undoes the other, exactly like squaring and square-rooting:

$$\log(10^x) = x \qquad \text{and} \qquad 10^{\log x} = x$$

Now the chemistry payoff. Hydrogen ion concentration $[\ce{H+}]$ in aqueous solutions ranges over thirteen powers of ten. Writing "the concentration went from $0.00001$ M to $0.00000001$ M" is how you get errors and eye strain. So chemists pull the earthquake trick — report the exponent instead of the number — with one twist. Since $[\ce{H+}]$ values are tiny, their logs are all *negative* ($\log 10^{-7} = -7$), and nobody wants a scale full of minus signs. So we flip the sign:

$$\boxed{\text{pH} = -\log[\ce{H+}]}$$

The "p" in pH literally means "take the negative log of." That's why the formula sheet also has pOH ($= -\log[\ce{OH-}]$), p$K_a$, and p$K_w$ — same operator, different victim.

Structural map, so the analogy earns its keep:

| Earthquake world | Chemistry world |
|---|---|
| Ground shaking amplitude | $[\ce{H+}]$ concentration |
| Magnitude | pH (with a sign flip) |
| +1 magnitude = 10× shaking | −1 pH unit = 10× more acidic |
| Magnitude counts zeros of shaking | pH counts zeros of concentration |

One consequence you must internalize: **pH differences are multiplicative, not additive.** A soda at pH 3 is not "twice as acidic" as blood at pH 7.4 — it has roughly $10^{4.4} \approx 25{,}000$ times the $[\ce{H+}]$. Just like the 4.2 that rattled my water glass versus a 6.2 that would have knocked it off the table.

### The Definition and the Rules

**Definition.** For $x > 0$:

$$\log_{10} x = y \quad \Longleftrightarrow \quad 10^y = x$$

In chemistry, "$\log$" with no base written always means base 10 (the **common log**), matching the LOG button on your calculator.

**The three log rules.** These follow directly from exponent rules, because logs *are* exponents:

| Rule | Statement | Exponent fact behind it |
|---|---|---|
| Product | $\log(ab) = \log a + \log b$ | $10^m \cdot 10^n = 10^{m+n}$ |
| Quotient | $\log\left(\dfrac{a}{b}\right) = \log a - \log b$ | $\dfrac{10^m}{10^n} = 10^{m-n}$ |
| Power | $\log(a^n) = n \log a$ | $(10^m)^n = 10^{mn}$ |

The product rule is the reason scientific notation and logs get along so well:

$$\log(a \times 10^{n}) = \log a + n$$

The coefficient contributes a small decimal ($\log a$ is between 0 and 1 when $1 \le a < 10$), and the power of ten contributes the integer. This one identity powers every mental pH estimate you'll ever make.

**Antilogs.** To undo a log, raise 10 to it. If $\log x = y$, then $x = 10^y$. On your calculator that's the $10^x$ button (usually 2nd + LOG).

**Natural log.** The other log on your calculator, $\ln$ (base $e \approx 2.718$), is calculus's favorite child. The conversion between them is a fixed constant:

$$\ln x = 2.303 \log x$$

Division of labor in AP Chemistry:

| Uses $\log$ (base 10) | Uses $\ln$ (base $e$) |
|---|---|
| pH, pOH, p$K_a$, p$K_b$ | First-order integrated rate law |
| pH = p$K_a$ + $\log\frac{[\ce{A-}]}{[\ce{HA}]}$ (buffers, later) | Arrhenius equation ($\ln k$ vs $1/T$) |
| Estimation from powers of ten | $\Delta G^\circ = -RT\ln K$ (thermo, later) |

Preview of coming attractions: in kinetics, a first-order reaction $\ce{A -> products}$ obeys

$$\ln[\ce{A}]_t = \ln[\ce{A}]_0 - kt$$

which is a straight line of $\ln[\ce{A}]$ versus $t$ — and turning curves into straight lines is exactly what the next article, [Graphing and Linearization](/chemistry/0105-graphing-linearization), is about. The Arrhenius equation plays the same game with $\ln k$ versus $1/T$. Logs aren't just for pH; they're chemistry's universal curve-straightener.

**The pH workflow, both directions:**

$$\text{concentration} \xrightarrow{\;-\log\;} \text{pH} \qquad \qquad \text{pH} \xrightarrow{\;10^{-\text{pH}}\;} \text{concentration}$$

$$\text{pH} = -\log[\ce{H+}] \qquad \qquad [\ce{H+}] = 10^{-\text{pH}}$$

You must be able to sprint both directions without hesitation. The AP exam tests each direction, sometimes in the same problem.

**The sig-fig rule for logs (learn it now, thank me in May):**

> The number of **digits after the decimal point** in a log equals the number of **significant figures** in the original number. Digits *before* the decimal point don't count — they only record the power of ten.

So $[\ce{H+}] = 2.0 \times 10^{-5}$ M (2 sig figs) gives pH $= 4.70$ (2 digits after the decimal). The "4" is free — it comes from the exponent $-5$, which is exact, the same way the "6" in magnitude 6.2 just locates which power of ten you're in.

---

## Worked Examples

### Example 1: Logs of Powers of Ten in Your Head

**Problem:** Without a calculator, evaluate (a) $\log 1000$, (b) $\log 10^{-7}$, (c) $\log 1$, (d) $\log 0.0001$.

**Solution:**

**Step 1:** Translate each into the question "10 to what power?"

**Step 2:**
- (a) $10^3 = 1000$, so $\log 1000 = 3$
- (b) $\log 10^{-7} = -7$ directly (log and $10^x$ cancel)
- (c) $10^0 = 1$, so $\log 1 = 0$
- (d) $0.0001 = 10^{-4}$, so $\log 0.0001 = -4$

**Answer: (a) 3, (b) −7, (c) 0, (d) −4.** If the number is a pure power of ten, the log is just the exponent.

### Example 2: The Product Rule on a Real Concentration

**Problem:** Use the product rule (and the fact that $\log 2.0 = 0.30$) to evaluate $\log(2.0 \times 10^{-3})$ without a calculator.

**Solution:**

**Step 1:** Split with the product rule:
$$\log(2.0 \times 10^{-3}) = \log 2.0 + \log 10^{-3}$$

**Step 2:** Evaluate each piece: $\log 2.0 = 0.30$ and $\log 10^{-3} = -3$.

**Step 3:** Add: $0.30 + (-3) = -2.70$.

**Answer: $\log(2.0 \times 10^{-3}) = -2.70$.** Coefficient gives the decimal, exponent gives the integer. (And if this were an $[\ce{H+}]$, the pH would be $+2.70$.)

### Example 3: The Quotient Rule — How Many Times More Acidic?

**Problem:** Stomach acid has $[\ce{H+}] \approx 1 \times 10^{-2}$ M; black coffee has $[\ce{H+}] \approx 1 \times 10^{-5}$ M. Use the quotient rule to find how many times more acidic stomach acid is.

**Solution:**

**Step 1:** The ratio of concentrations is what "times more acidic" means:
$$\frac{[\ce{H+}]_{\text{stomach}}}{[\ce{H+}]_{\text{coffee}}} = \frac{1 \times 10^{-2}}{1 \times 10^{-5}}$$

**Step 2:** Take the log using the quotient rule:
$$\log\left(\frac{10^{-2}}{10^{-5}}\right) = \log 10^{-2} - \log 10^{-5} = -2 - (-5) = 3$$

**Step 3:** A log of 3 means the ratio itself is $10^3$.

**Answer: Stomach acid is $10^3 = 1000$ times more acidic.** Notice this is just the pH difference ($5 - 2 = 3$) turned back into a power of ten — the earthquake rule again.

### Example 4: The Power Rule in a Weak-Acid Setup

**Problem:** For a weak acid where $[\ce{H+}] = [\ce{A-}]$, expressions like $[\ce{H+}]^2$ appear inside $K_a = \dfrac{[\ce{H+}][\ce{A-}]}{[\ce{HA}]}$. If $[\ce{H+}] = 2.0 \times 10^{-4}$ M, evaluate $\log\left([\ce{H+}]^2\right)$ without a calculator.

**Solution:**

**Step 1:** Power rule first:
$$\log\left([\ce{H+}]^2\right) = 2\log[\ce{H+}]$$

**Step 2:** Product rule on the inside: $\log(2.0 \times 10^{-4}) = 0.30 - 4 = -3.70$.

**Step 3:** Multiply: $2 \times (-3.70) = -7.40$.

**Answer: $\log\left([\ce{H+}]^2\right) = -7.40$.** The exponent 2 walks out front as a multiplier — that's the whole power rule.

### Example 5: Antilogs — Solving $-\log x = 4.7$

**Problem:** Solve $-\log x = 4.7$ for $x$ (this is exactly "find $[\ce{H+}]$ given pH 4.7").

**Solution:**

**Step 1:** Isolate the log: $\log x = -4.7$.

**Step 2:** Undo the log by raising 10 to both sides:
$$x = 10^{-4.7}$$

**Step 3:** To evaluate mentally, split the exponent into an integer and a positive decimal:
$$10^{-4.7} = 10^{0.3} \times 10^{-5}$$
Since $\log 2 = 0.30$, we know $10^{0.3} = 2$.

**Answer: $x = 2 \times 10^{-5}$.** (Calculator check: $10^{-4.7} = 1.995 \times 10^{-5}$. ✓) The move $10^{-4.7} = 10^{0.3} \times 10^{-5}$ — always splitting so the leftover power of ten is an integer — is the antilog workhorse.

### Example 6: pH from Concentration — Lemon Juice

**Problem:** Lemon juice has $[\ce{H+}] = 5.0 \times 10^{-3}$ M. Find its pH with correct sig figs.

**Solution:**

**Step 1:** Apply the definition:
$$\text{pH} = -\log(5.0 \times 10^{-3})$$

**Step 2:** Product rule: $\log(5.0 \times 10^{-3}) = \log 5.0 + (-3) = 0.70 - 3 = -2.30$.

**Step 3:** Flip the sign: pH $= 2.30$.

**Step 4:** Sig figs: $5.0 \times 10^{-3}$ has 2 sig figs, so the pH keeps 2 digits *after* the decimal.

**Answer: pH = 2.30.** Sour enough to make you wince, about ten thousand times more acidic than pure water.

### Example 7: Concentration from pH — Blood

**Problem:** Healthy blood has pH 7.40. Find $[\ce{H+}]$.

**Solution:**

**Step 1:** Invert the pH definition:
$$[\ce{H+}] = 10^{-\text{pH}} = 10^{-7.40}$$

**Step 2:** Split the exponent: $10^{-7.40} = 10^{0.60} \times 10^{-8}$.

**Step 3:** Recognize $10^{0.60}$: since $\log 4 = 2\log 2 = 0.60$, we get $10^{0.60} = 4.0$.

**Step 4:** Sig figs: pH 7.40 has 2 digits after the decimal, so the answer gets 2 sig figs.

**Answer: $[\ce{H+}] = 4.0 \times 10^{-8}$ M.** (Calculator: $3.98 \times 10^{-8}$. ✓) Your body holds this within about ±0.05 pH units — enzymes are picky.

### Example 8: Concentration from pH — Household Ammonia

**Problem:** A bottle of household ammonia cleaner ($\ce{NH3(aq)}$) has pH 11.60. Find $[\ce{H+}]$.

**Solution:**

**Step 1:** $[\ce{H+}] = 10^{-11.60}$.

**Step 2:** Split: $10^{-11.60} = 10^{0.40} \times 10^{-12}$.

**Step 3:** $10^{0.40} \approx 2.5$ (worth memorizing: $10^{0.3} \approx 2$, $10^{0.4} \approx 2.5$, $10^{0.5} \approx 3.2$, $10^{0.6} \approx 4$, $10^{0.7} \approx 5$).

**Answer: $[\ce{H+}] = 2.5 \times 10^{-12}$ M.** Wildly basic — the $[\ce{H+}]$ is about four powers of ten *below* neutral water's $10^{-7}$ M.

### Example 9: The Sig-Fig Rule in Action

**Problem:** A student measures $[\ce{H+}] = 2.0 \times 10^{-5}$ M and reports "pH = 4.7." Another reports "pH = 4.699." Who's right, and why?

**Solution:**

**Step 1:** Compute: $\text{pH} = -\log(2.0 \times 10^{-5}) = -(0.301 - 5) = 4.69897\ldots$

**Step 2:** Count sig figs in the input: $2.0 \times 10^{-5}$ has **2** sig figs.

**Step 3:** Apply the log rule: 2 sig figs in the concentration → **2 digits after the decimal** in the pH. The leading "4" doesn't count; it just encodes the $10^{-5}$.

**Answer: pH = 4.70.** Neither student is right — "4.7" has too few decimal digits (1), "4.699" has too many (3). This exact rounding decision shows up in AP FRQ scoring guidelines.

### Example 10: Converting Between ln and log

**Problem:** A kinetics experiment gives $\log k = -3.20$. Find $\ln k$.

**Solution:**

**Step 1:** Use the conversion $\ln x = 2.303 \log x$.

**Step 2:** Multiply: $\ln k = 2.303 \times (-3.20) = -7.37$.

**Answer: $\ln k = -7.37$.** The 2.303 is just $\ln 10$ — natural-log steps are "shorter" than base-10 steps, so you need 2.303 of them per power of ten.

### Example 11: Preview — First-Order Decay Uses ln

**Problem:** $\ce{N2O5}$ decomposes by first-order kinetics with $k = 0.0231\ \text{s}^{-1}$. If $[\ce{N2O5}]_0 = 0.100$ M, find $[\ce{N2O5}]$ after 30.0 s using $\ln[\ce{A}]_t = \ln[\ce{A}]_0 - kt$.

**Solution:**

**Step 1:** Compute the pieces: $\ln(0.100) = -2.303$ and $kt = (0.0231)(30.0) = 0.693$.

**Step 2:** Substitute:
$$\ln[\ce{A}]_t = -2.303 - 0.693 = -2.996$$

**Step 3:** Antilog with $e$ this time (the $e^x$ button, not $10^x$):
$$[\ce{A}]_t = e^{-2.996} = 0.0500 \text{ M}$$

**Answer: $[\ce{N2O5}] = 0.0500$ M** — exactly half the starting amount, because $0.693/k$ is the half-life and we waited exactly one of them. Full story in the kinetics unit; for now, notice the workflow is pH's twin with $e$ swapped in for 10.

### Example 12: Estimating pH Without a Calculator

**Problem:** Estimate the pH of a solution with $[\ce{H+}] = 3 \times 10^{-5}$ M. No calculator.

**Solution:**

**Step 1:** Bracket with powers of ten: $1 \times 10^{-5} < 3 \times 10^{-5} < 1 \times 10^{-4}$. Taking negative logs *flips* the inequality:
$$5 > \text{pH} > 4$$

**Step 2:** Refine using the coefficient: pH $= 5 - \log 3 = 5 - 0.48 = 4.52$. Even without memorizing $\log 3$, note that 3 is (log-wise) about halfway between 1 and 10, so the pH sits near the middle of the bracket, a touch below 4.5.

**Answer: pH ≈ 4.5 (between 4 and 5, closer to the middle).** The bracketing step alone — "coefficient bigger than 1 means pH is *less than* the bare exponent" — answers most AP multiple-choice estimation questions in under ten seconds.

---

## Common Mistakes

| The mistake | Why it happens | How to avoid it |
|---|---|---|
| Reporting pH as negative: "pH = −4.70" | Forgetting the minus sign in $\text{pH} = -\log[\ce{H+}]$ | For typical dilute acids/bases, $[\ce{H+}] < 1$ M, so the log is negative and the pH is **positive**. Sanity-check the sign every time. |
| Thinking pH 3 is "twice as acidic" as pH 6 | Treating a log scale as linear | Each pH unit is a factor of 10. A difference of 3 units is $10^3 = 1000\times$. Think earthquakes, not rulers. |
| Computing $[\ce{H+}] = 10^{+\text{pH}}$ | Dropping the negative in the antilog | Say it as a sentence: "concentration is ten to the *minus* pH." A pH of 7 must give a tiny number ($10^{-7}$), not ten million. |
| Wrong sig figs: pH "4.7" or "4.699" from $2.0 \times 10^{-5}$ M | Applying normal sig-fig counting to logs | Sig figs in the number = digits **after the decimal** in the log. The integer part is free. |
| Writing $\log(a + b) = \log a + \log b$ | Pattern-matching the product rule onto a sum | The product rule needs *multiplication* inside: $\log(ab) = \log a + \log b$. There is **no** rule for the log of a sum. |
| Pressing LN when the formula says log (or vice versa) | The buttons are neighbors and the symbols look alike | pH/pOH/p$K_a$ → LOG and $10^x$. Kinetics/Arrhenius/thermo → LN and $e^x$. Match the undo button to the log you used. |
| Estimating pH of $3 \times 10^{-5}$ M as "about 5" | Ignoring the coefficient | Any coefficient bigger than 1 *lowers* the pH below the bare exponent: the answer is between 4 and 5, not "basically 5." |

---

## AP Exam Tips

- **Calculators are allowed on the entire AP Chemistry exam** (unlike Calc BC's no-calculator sections). But the College Board knows this — pH estimation multiple-choice questions are written so the mental method (bracket by powers of ten, adjust for the coefficient) is *faster* than typing. Answer choices are usually spaced like "between 3 and 4 / between 4 and 5 / ...", so bracketing alone finishes the problem.
- The equation sheet hands you $\text{pH} = -\log[\ce{H+}]$, $\text{pOH} = -\log[\ce{OH-}]$, and $\text{pH} + \text{pOH} = 14.00$ (at 25 °C). It also gives the first-order law $\ln[\ce{A}]_t - \ln[\ce{A}]_0 = -kt$ with $\ln$, not $\log$. You don't memorize the formulas — you memorize *which log* each one uses.
- On FRQs, the log sig-fig rule is a real scoring line: pH from a 2-sig-fig concentration should have 2 decimal places. Graders routinely accept a small range, but a pH reported to zero or one decimal from good data can cost the point.
- Expect "ranking" MC questions: *which solution is most acidic / how many times more acidic is X than Y?* These are pure log-scale reasoning — difference in pH → power of ten. No calculator needed, and none should be used.
- When a question gives you pH and asks for a concentration mid-calculation (e.g., feed $[\ce{H+}]$ into a $K_a$ expression), do the antilog **first** and keep an extra guard digit until the final answer.
- Memorize the mini-table $10^{0.3} \approx 2$, $10^{0.5} \approx 3$, $10^{0.7} \approx 5$. Those three anchors (plus their flips $\log 2 = 0.3$, $\log 3 = 0.48$, $\log 5 = 0.7$) cover essentially every estimation question the exam can throw at you.

---

## Practice Problems

### Problem 1
Without a calculator, evaluate: (a) $\log 10^{6}$, (b) $\log 0.000001$, (c) $\log 1$, (d) $\log \sqrt{10}$.

<details>
<summary><strong>Solution</strong></summary>

Each is the question "10 to what power?"

- (a) $\log 10^6 = 6$
- (b) $0.000001 = 10^{-6}$, so the log is $-6$
- (c) $10^0 = 1$, so $\log 1 = 0$
- (d) $\sqrt{10} = 10^{1/2}$, so $\log \sqrt{10} = \frac{1}{2}$

**Answers: (a) 6, (b) −6, (c) 0, (d) 0.5.**

</details>

### Problem 2
Using $\log 4.0 = 0.60$, evaluate $\log(4.0 \times 10^{-6})$ without a calculator.

<details>
<summary><strong>Solution</strong></summary>

Product rule:
$$\log(4.0 \times 10^{-6}) = \log 4.0 + \log 10^{-6} = 0.60 + (-6) = -5.40$$

**Answer: −5.40.**

</details>

### Problem 3
Two solutions have $[\ce{H+}] = 6.0 \times 10^{-3}$ M and $[\ce{H+}] = 6.0 \times 10^{-8}$ M. Use the quotient rule to find the log of their ratio, then state the ratio itself.

<details>
<summary><strong>Solution</strong></summary>

$$\log\left(\frac{6.0 \times 10^{-3}}{6.0 \times 10^{-8}}\right) = \log(6.0 \times 10^{-3}) - \log(6.0 \times 10^{-8})$$

The $\log 6.0$ pieces cancel, leaving $(-3) - (-8) = 5$.

A log of 5 means the ratio is $10^5$.

**Answer: $\log(\text{ratio}) = 5$; the first solution is $10^5 = 100{,}000$ times more concentrated in $\ce{H+}$.**

</details>

### Problem 4
Use the power rule and $\log 2 = 0.30$ to evaluate $\log\left[(2.0 \times 10^{-3})^2\right]$ without a calculator.

<details>
<summary><strong>Solution</strong></summary>

Power rule first:
$$\log\left[(2.0 \times 10^{-3})^2\right] = 2\log(2.0 \times 10^{-3})$$

Inner log by the product rule: $0.30 - 3 = -2.70$.

Multiply: $2 \times (-2.70) = -5.40$.

**Answer: −5.40.**

</details>

### Problem 5
Solve for $x$: $-\log x = 3.25$. Give $x$ in scientific notation with 2 sig figs.

<details>
<summary><strong>Solution</strong></summary>

$$\log x = -3.25 \quad\Rightarrow\quad x = 10^{-3.25}$$

Split the exponent: $10^{-3.25} = 10^{0.75} \times 10^{-4}$.

$10^{0.75} \approx 5.6$ (between $10^{0.7} \approx 5$ and $10^{0.8} \approx 6.3$).

**Answer: $x = 5.6 \times 10^{-4}$.**

(Sig-fig check: 3.25 has 2 digits after the decimal → 2 sig figs in $x$. ✓)

</details>

### Problem 6
A cola has $[\ce{H+}] = 7.1 \times 10^{-4}$ M. Calculate its pH with correct sig figs.

<details>
<summary><strong>Solution</strong></summary>

$$\text{pH} = -\log(7.1 \times 10^{-4}) = -(\log 7.1 - 4) = -(0.851 - 4) = 3.149$$

$7.1 \times 10^{-4}$ has 2 sig figs → 2 digits after the decimal.

**Answer: pH = 3.15.**

</details>

### Problem 7
An acid rain sample has pH 5.30. Find $[\ce{H+}]$ with correct sig figs.

<details>
<summary><strong>Solution</strong></summary>

$$[\ce{H+}] = 10^{-5.30} = 10^{0.70} \times 10^{-6}$$

$10^{0.70} = 5.0$ (since $\log 5 = 0.70$).

pH 5.30 has 2 digits after the decimal → 2 sig figs.

**Answer: $[\ce{H+}] = 5.0 \times 10^{-6}$ M.**

</details>

### Problem 8
A drain-cleaner solution has $[\ce{OH-}] = 4.0 \times 10^{-2}$ M. Calculate the pOH ($= -\log[\ce{OH-}]$), then use $\text{pH} + \text{pOH} = 14.00$ to find the pH.

<details>
<summary><strong>Solution</strong></summary>

$$\text{pOH} = -\log(4.0 \times 10^{-2}) = -(0.60 - 2) = 1.40$$

$$\text{pH} = 14.00 - \text{pOH} = 14.00 - 1.40 = 12.60$$

**Answer: pOH = 1.40, pH = 12.60.** Same log machinery, different ion.

</details>

### Problem 9
Solution A has pH 3.0; solution B has pH 6.0. How many times greater is $[\ce{H+}]$ in A than in B? No calculator.

<details>
<summary><strong>Solution</strong></summary>

The pH difference is $6.0 - 3.0 = 3.0$ units. Each unit is a factor of 10:

$$\frac{[\ce{H+}]_A}{[\ce{H+}]_B} = 10^{3} = 1000$$

**Answer: 1000 times.** Not "twice" — log scales multiply.

</details>

### Problem 10
**(No calculator — AP style.)** A solution has $[\ce{H+}] = 6 \times 10^{-9}$ M. Its pH is:
(A) between 5 and 6  (B) between 8 and 9  (C) between 9 and 10  (D) exactly 9

<details>
<summary><strong>Solution</strong></summary>

Bracket: $1 \times 10^{-9} < 6 \times 10^{-9} < 1 \times 10^{-8}$, and negative logs flip the inequality, so the pH is between 8 and 9.

Refine: pH $= 9 - \log 6 = 9 - 0.78 = 8.22$, closer to 8. Either way, only one choice fits.

**Answer: (B) between 8 and 9.**

</details>

### Problem 11
How many sig figs are in each measurement? (a) pH = 9.115, (b) pH = 3.4, (c) pOH = 10.60.

<details>
<summary><strong>Solution</strong></summary>

Count only the digits **after** the decimal point:

- (a) 9.115 → three digits after the decimal → **3 sig figs**
- (b) 3.4 → one digit after the decimal → **1 sig fig**
- (c) 10.60 → two digits after the decimal → **2 sig figs** (the trailing zero counts; the "10" doesn't)

**Answers: (a) 3, (b) 1, (c) 2.**

</details>

### Problem 12
An equilibrium constant satisfies $\log K = 5.0$. Find (a) $K$ itself and (b) $\ln K$.

<details>
<summary><strong>Solution</strong></summary>

(a) Antilog: $K = 10^{5.0} = 1.0 \times 10^{5}$.

(b) Convert: $\ln K = 2.303 \log K = 2.303 \times 5.0 = 11.5$.

**Answers: (a) $K = 1.0 \times 10^5$, (b) $\ln K = 11.5$.**

</details>

### Problem 13
A first-order reaction has $k = 0.0347\ \text{min}^{-1}$ and $[\ce{A}]_0 = 0.500$ M. Use $\ln[\ce{A}]_t = \ln[\ce{A}]_0 - kt$ to find $[\ce{A}]$ after 40.0 min.

<details>
<summary><strong>Solution</strong></summary>

Pieces: $\ln(0.500) = -0.693$ and $kt = (0.0347)(40.0) = 1.388$.

$$\ln[\ce{A}]_t = -0.693 - 1.388 = -2.081$$

Antilog with $e$: $[\ce{A}]_t = e^{-2.081} = 0.125$ M.

**Answer: $[\ce{A}] = 0.125$ M** — two half-lives have passed ($0.500 \to 0.250 \to 0.125$), which is a nice built-in check.

</details>

### Problem 14
During an earthquake drill my little cousin asked whether a magnitude 7 is "three worse" than a magnitude 4. Using log-scale reasoning, how many times greater is the ground shaking in a magnitude 7?

<details>
<summary><strong>Solution</strong></summary>

Each magnitude unit is a factor of 10 in shaking amplitude. A difference of $7 - 4 = 3$ units means:

$$10^{3} = 1000$$

**Answer: about 1000 times more shaking.** Identical math to Problem 9 — pH and magnitude are the same scale wearing different lab coats.

</details>

### Problem 15
Healthy blood pH ranges from 7.35 to 7.45. Compute $[\ce{H+}]$ at both ends and show the concentration only changes by about 25% across this range.

<details>
<summary><strong>Solution</strong></summary>

At pH 7.35: $[\ce{H+}] = 10^{-7.35} = 10^{0.65} \times 10^{-8} = 4.5 \times 10^{-8}$ M.

At pH 7.45: $[\ce{H+}] = 10^{-7.45} = 10^{0.55} \times 10^{-8} = 3.5 \times 10^{-8}$ M.

Ratio: $\dfrac{4.5}{3.5} = 1.26$ — about a 25–30% swing in $[\ce{H+}]$ compressed into just 0.10 pH units.

**Answer: $[\ce{H+}]$ ranges from about $3.5 \times 10^{-8}$ M to $4.5 \times 10^{-8}$ M (~25% change).** Log scales make tight biological control look deceptively boring.

</details>

---

## Quick Reference

| Concept | Formula / Rule | Notes |
|---|---|---|
| Definition | $\log x = y \iff 10^y = x$ | The log asks "10 to what power?" |
| Inverse pair | $\log(10^x) = x$, $\ \ 10^{\log x} = x$ | LOG and $10^x$ undo each other |
| Product rule | $\log(ab) = \log a + \log b$ | So $\log(a \times 10^n) = \log a + n$ |
| Quotient rule | $\log(a/b) = \log a - \log b$ | Ratios → pH differences |
| Power rule | $\log(a^n) = n\log a$ | Exponent walks out front |
| pH forward | $\text{pH} = -\log[\ce{H+}]$ | Also pOH $= -\log[\ce{OH-}]$ |
| pH backward | $[\ce{H+}] = 10^{-\text{pH}}$ | Split: $10^{-4.7} = 10^{0.3}\times 10^{-5}$ |
| ln ↔ log | $\ln x = 2.303 \log x$ | 2.303 is $\ln 10$ |
| Which log where | pH/pOH/p$K_a$ → $\log$; kinetics/Arrhenius/thermo → $\ln$ | Match the undo: $10^x$ vs $e^x$ |
| Sig figs for logs | Sig figs in $x$ = digits **after** the decimal in $\log x$ | pH 4.70 ↔ 2 sig figs |
| Mental anchors | $\log 2 = 0.30$, $\log 3 = 0.48$, $\log 5 = 0.70$ | Flips: $10^{0.3}\!\approx\!2$, $10^{0.5}\!\approx\!3.2$, $10^{0.7}\!\approx\!5$ |
| Estimation | $[\ce{H+}] = a \times 10^{-n}$ with $a>1$ → pH between $n-1$ and $n$ | Coefficient $>1$ pulls pH *below* $n$ |

---

<div align="center">

[← Dimensional Analysis](/chemistry/0103-dimensional-analysis) | [Graphing and Linearization →](/chemistry/0105-graphing-linearization)

</div>
