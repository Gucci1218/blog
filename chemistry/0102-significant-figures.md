# Significant Figures
<p class="article-date">July 4, 2026</p>

*Last week at dinner I told my dad my water bottle held "about 500 mL," and he laughed — because at HP, where he works on printer ink, "about" is a luxury nobody gets. A modern inkjet fires droplets of roughly 10 picoliters each. That's trillionths of a liter — my "about 500 mL" eyeball guess versus an instrument that can stand behind a number fifty billion times smaller. And here's what stuck with me: Dad says an engineer who wrote "10.00000 pL" off a rough gauge would get laughed out of the design review, because those extra zeros are a lie. Not a lie about the drop — a lie about the instrument, claiming a precision the gauge never gave them. That's the whole idea behind significant figures: every digit you write is a promise about how good your measurement was, the guaranteed digits come straight from the instrument, and the very last digit is the one honest estimate you're allowed to make. In AP Chemistry, where every lab and every free-response calculation starts with a measurement, sig figs are the honesty system that keeps your answers trustworthy — and yes, graders check.*

---

## What You'll Learn
- Distinguish measured numbers (which carry uncertainty) from exact numbers (which have unlimited sig figs)
- Count significant figures in any number using four rules: nonzero digits, captive zeros, leading zeros, and trailing zeros
- Explain why scientific notation eliminates every ambiguity about trailing zeros
- Apply the multiplication/division rule: round to the fewest **significant figures**
- Apply the addition/subtraction rule: round to the fewest **decimal places**
- Handle multi-step calculations correctly — keep guard digits and round only at the end
- Round numbers correctly, including the tricky "ends in 5" case
- Read a graduated cylinder and a balance to the correct number of digits (one estimated digit past the markings)
- Report chemistry results — density, molar mass arithmetic — with defensible precision

---

## Prerequisites
- [Scientific Notation](/chemistry/0101-scientific-notation) — sig figs and scientific notation are two halves of the same system; scientific notation is how we *display* exactly the sig figs we mean

---

## The Core Concept

### Intuition First

Back to my water bottle. I actually weighed it. Our old kitchen scale has a needle and markings every 10 g. I can *see* that the needle is past the 520 g line and not quite at the 530 g line — those digits are guaranteed by the instrument. Then I squint and estimate one more digit: "looks like 527 g." That estimated digit is a judgment call, but it's an honest one, and it's the *last* digit I'm allowed to write.

The next day I put the same bottle on the digital balance in my chem class, which reads to the hundredth of a gram. It guarantees "527.3" and estimates the "6" internally. So the lab balance earns five digits: 527.36 g. (Dad's ink lab plays the exact same game, just at a scale that makes my head spin — their instruments earn enough digits to stand behind a 10 pL drop.)

Here's the structural map, and it's the key to this whole article:

| Measurement part | What it means |
|---|---|
| **Certain digits** | What the instrument's markings guarantee |
| **Last (estimated) digit** | Your one honest guess, one place past the finest marking |
| **Anything beyond that** | A lie about your instrument |

So a measurement of 527.36 g is really saying: "I am confident about 527.3, my best estimate for the next digit is 6, and I make no claims beyond that." The number of significant figures is simply the count of digits you're standing behind — certain digits plus the single estimated one.

Writing "527.36000 g" from the kitchen scale isn't extra credit for enthusiasm. It's a false promise: it claims your instrument could distinguish 527.36000 from 527.36001, and a \$10 kitchen scale absolutely cannot. It's the "10.00000 pL" move that gets you laughed out of the design review. Sig figs exist to keep the promise matched to the tool.

### Measured Numbers vs. Exact Numbers

Not every number in chemistry is a measurement.

**Measured numbers** come from an instrument and carry uncertainty: 527.36 g from a lab balance, 25.0 mL from a graduated cylinder, 3.5482 g from an analytical balance. These have a limited number of significant figures.

**Exact numbers** have *unlimited* significant figures because there is zero uncertainty in them. They never limit your answer's precision. Exact numbers include:

- **Counting numbers:** 24 students in the lab, 3 trials, 2 atoms of $\ce{H}$ in one molecule of $\ce{H2O}$. You can't have 24.3 students.
- **Defined conversion factors:** 1 in = 2.54 cm (exact, by definition), 1000 mL = 1 L, 1 km = 1000 m, 60 s = 1 min.
- **Coefficients and subscripts in chemical equations:** the 2 in $\ce{2H2 + O2 -> 2H2O}$ is exactly 2.

When you compute, exact numbers are invisible to the sig-fig count — only the measured numbers vote.

### The Counting Rules

Four rules cover every case:

**Rule 1 — Nonzero digits are always significant.**
$457$ has 3 sig figs. $2.38$ has 3 sig figs.

**Rule 2 — Captive zeros (zeros between nonzero digits) are always significant.**
$1002$ has 4 sig figs. $3.07$ has 3 sig figs. Those zeros were *measured* — the instrument had to read past them.

**Rule 3 — Leading zeros are never significant.**
$0.0025$ has 2 sig figs. Leading zeros are just placeholders that locate the decimal point. Proof: write $0.0025$ in scientific notation and they vanish — $2.5 \times 10^{-3}$. If a digit disappears when you change units or notation, it was never a promise about the measurement.

**Rule 4 — Trailing zeros are significant only if the number contains a decimal point.**
- $2.500$ has 4 sig figs — someone measured those zeros and is standing behind them.
- $25.0$ has 3 sig figs.
- $2500$ is **ambiguous** — 2, 3, or 4 sig figs? Can't tell.
- $2500.$ (with the decimal point) has 4 sig figs, though this notation is rare.

### Why Scientific Notation Fixes Everything

That ambiguous $2500$ is exactly why [Scientific Notation](/chemistry/0101-scientific-notation) comes first in this toolkit. In scientific notation, *every digit you write in the coefficient is significant* — no exceptions, no ambiguity:

$$2.5 \times 10^3 \;\; \text{(2 sig figs)} \qquad 2.50 \times 10^3 \;\; \text{(3 sig figs)} \qquad 2.500 \times 10^3 \;\; \text{(4 sig figs)}$$

Same value, three different promises about the instrument. When in doubt — especially with big round-looking numbers — report in scientific notation and the ambiguity disappears.

### Operations Rule 1: Multiplication and Division

> **The result keeps as many significant figures as the measurement with the FEWEST significant figures.**

A chain is as strong as its weakest link. If one input was eyeballed on a kitchen scale, no amount of analytical-balance partners can rescue the product — Dad's team specs *every* gauge on the line for exactly this reason.

$$4.56 \times 1.4 = 6.384 \longrightarrow \boxed{6.4}$$

$4.56$ has 3 sig figs, $1.4$ has 2, so the answer gets 2.

### Operations Rule 2: Addition and Subtraction

> **The result keeps as many DECIMAL PLACES as the measurement with the fewest decimal places.**

This is a different rule — decimal places, not sig figs — and mixing them up is the single most common sig-fig error. The logic: when you add, uncertainty lives at a *position*. If one number is fuzzy in the tenths place, the sum is fuzzy in the tenths place, period.

$$12.11 + 18.0 + 1.013 = 31.123 \longrightarrow \boxed{31.1}$$

$18.0$ only knows itself to the tenths place, so the sum only knows itself to the tenths place. (Notice the answer happens to have 3 sig figs while $1.013$ had 4 — that's fine. The rule counted decimal places, and sig figs just fell where they fell.)

### Rounding Rules (Including the 5)

To round to $n$ sig figs, look at the first digit you're dropping:

1. **Less than 5:** round down (truncate). $6.34 \to 6.3$
2. **Greater than 5, or 5 followed by anything nonzero:** round up. $6.36 \to 6.4$; $6.351 \to 6.4$
3. **Exactly 5 (nothing after it, or only zeros):** the AP-safe convention is to round up: $6.35 \to 6.4$. (Some labs use "round half to even" — $6.35 \to 6.4$ but $6.45 \to 6.4$ — to avoid systematic bias. Know it exists; use round-up on the exam.)

### Multi-Step Calculations: Round Once, at the End

If you round after every intermediate step, small errors compound and your final answer drifts. The professional habit:

1. **Track** the sig figs each step *would* allow (jot it in the margin).
2. **Carry** at least one or two extra digits — **guard digits** — through every intermediate step (or better, leave everything in your calculator).
3. **Round once**, at the very end, to the correct count.

$$\underbrace{\text{calculate with guard digits}}_{\text{full precision}} \longrightarrow \underbrace{\text{round at the end}}_{\text{correct sig figs}}$$

One subtlety: in a multi-step problem that mixes operations, the addition/subtraction steps are judged by decimal places and the multiplication/division steps by sig figs — you determine the final count by walking the rules through in order (Example 10 shows this).

### Reading Instruments: Where the Digits Come From

**Graduated cylinder.** Read the bottom of the meniscus at eye level. Record every digit the markings guarantee, **then estimate exactly one more digit** between the lines. A cylinder marked every 1 mL, with the meniscus between 36 and 37 mL and sitting about halfway: record **36.5 mL** (3 sig figs). Recording "36 mL" throws away information; recording "36.50 mL" invents it.

**Digital balance.** The estimation is done for you — record *every* digit on the display, including trailing zeros. If the balance reads $2.3400$ g, write $2.3400$ g (5 sig figs), not $2.34$ g. Dropping the zeros downgrades your own instrument.

**Rule of thumb:** analog instruments → all certain digits + one estimated digit. Digital instruments → copy the whole display.

---

## Worked Examples

### Example 1: Counting Sig Figs — The Full Gauntlet

**Problem:** How many significant figures are in each? (a) $407.2$  (b) $0.00380$  (c) $52{,}000$  (d) $1.030 \times 10^4$

**Solution:**

**Step 1 (a):** $407.2$ — nonzero digits (4, 7, 2) are significant; the 0 is captive (between nonzeros), so it counts. **4 sig figs.**

**Step 2 (b):** $0.00380$ — leading zeros (0.00) never count; 3 and 8 count; the trailing zero counts because there's a decimal point. **3 sig figs.**

**Step 3 (c):** $52{,}000$ — 5 and 2 count; the trailing zeros have no decimal point, so they're ambiguous placeholders. By convention, **2 sig figs** (and this is exactly the case scientific notation exists to fix).

**Step 4 (d):** $1.030 \times 10^4$ — in scientific notation every coefficient digit is significant. **4 sig figs.**

**Answer: (a) 4, (b) 3, (c) 2, (d) 4.**

### Example 2: Measured or Exact?

**Problem:** Classify each number as measured or exact: (a) 18 students titrated today; (b) a pipet delivered 25.00 mL; (c) 1 in = 2.54 cm; (d) there are 3 oxygen atoms in one formula unit of $\ce{CaCO3}$.

**Solution:**

**Step 1 (a):** Counted whole objects — **exact** (unlimited sig figs).

**Step 2 (b):** An instrument delivered it and the instrument has tolerance — **measured** (4 sig figs).

**Step 3 (c):** The inch is *defined* as exactly 2.54 cm — **exact**.

**Step 4 (d):** A subscript in a formula — **exact**. The formula $\ce{CaCO3}$ means exactly 3 oxygens, always.

**Answer: (a) exact, (b) measured, (c) exact, (d) exact.**

### Example 3: Scientific Notation Kills the Ambiguity

**Problem:** A student reports a mass as $1200$ g. Express this value in scientific notation assuming (a) 2 sig figs, (b) 3 sig figs, (c) 4 sig figs.

**Solution:**

**Step 1:** Move the decimal 3 places left: coefficient $1.2$, power $10^3$.

**Step 2:** Write exactly as many coefficient digits as sig figs claimed:

- (a) $1.2 \times 10^3$ g
- (b) $1.20 \times 10^3$ g
- (c) $1.200 \times 10^3$ g

**Step 3:** Notice all three are the *same value* but three different promises about the balance used. That's the whole point.

**Answer: (a) $1.2 \times 10^3$ g, (b) $1.20 \times 10^3$ g, (c) $1.200 \times 10^3$ g.**

### Example 4: Multiplication/Division

**Problem:** Compute $\dfrac{6.023 \times 2.1}{4.582}$ to the correct number of sig figs.

**Solution:**

**Step 1:** Count sig figs on each input: $6.023$ → 4, $2.1$ → 2, $4.582$ → 4. Weakest link: **2 sig figs**.

**Step 2:** Calculate with full precision: $\dfrac{6.023 \times 2.1}{4.582} = \dfrac{12.6483}{4.582} = 2.76044...$

**Step 3:** Round to 2 sig figs. The first dropped digit is 6, so round up: $2.8$.

**Answer: $2.8$**

### Example 5: Addition/Subtraction — Decimal Places Rule

**Problem:** A beaker has mass $52.31$ g. After adding salt, the total is $53.4467$ g (analytical balance for the second reading). What mass of salt was added?

**Solution:**

**Step 1:** Subtract with full precision: $53.4467 - 52.31 = 1.1367$ g.

**Step 2:** Decimal places: $53.4467$ has 4; $52.31$ has 2. The answer is only trustworthy to **2 decimal places** — the fuzzier balance sets the floor.

**Step 3:** Round: $1.1367 \to 1.14$ g.

**Answer: $1.14$ g** — note the fancy balance couldn't rescue the measurement, because the *difference* inherits the worse uncertainty.

### Example 6: Rounding at the 5

**Problem:** Round each to 3 sig figs: (a) $2.345$  (b) $2.3451$  (c) $0.086450$

**Solution:**

**Step 1 (a):** Dropping the 5, with nothing after it. AP-safe convention: round up. $2.345 \to 2.35$. (Round-half-to-even would give $2.34$; on the AP exam, round up.)

**Step 2 (b):** Dropping "51" — that's a 5 followed by nonzero, so unambiguously round up: $2.3451 \to 2.35$.

**Step 3 (c):** Sig figs are 8, 6, 4 (leading zeros don't count); the dropped part is "50" — a bare 5 case, round up: $0.086450 \to 0.0865$.

**Answer: (a) $2.35$, (b) $2.35$, (c) $0.0865$.**

### Example 7: Density from Mass and Volume

**Problem:** A metal slug has mass $27.834$ g (analytical balance). It's dropped into a graduated cylinder reading $21.5$ mL; the water rises to $24.7$ mL. Find the density with correct sig figs.

**Solution:**

**Step 1 (subtraction — decimal places):** $V = 24.7 - 21.5 = 3.2$ mL. Both readings have 1 decimal place, so the volume keeps 1 decimal place: $3.2$ mL, which is 2 sig figs.

**Step 2 (division — sig figs):** 

$$d = \frac{m}{V} = \frac{27.834 \text{ g}}{3.2 \text{ mL}} = 8.6981...\text{ g/mL}$$

**Step 3:** Weakest link is the volume (2 sig figs) — the 5-sig-fig balance can't save us. Round: $8.7$ g/mL.

**Answer: $d = 8.7$ g/mL.** (That's consistent with several metals; a 2-sig-fig density can't distinguish them — a real lesson in why volume by displacement is the precision bottleneck.)

### Example 8: Molar-Mass-Style Addition

**Problem:** Compute the molar mass of $\ce{H2SO4}$ from atomic masses $\ce{H} = 1.008$, $\ce{S} = 32.06$, $\ce{O} = 16.00$ (all in g/mol), reporting with correct precision.

**Solution:**

**Step 1:** The subscripts 2, 1, 4 are **exact** — they don't limit anything.

**Step 2:** Multiply each atomic mass by its exact count (the products keep their decimal precision since the counts are exact):

$$2(1.008) = 2.016 \qquad 1(32.06) = 32.06 \qquad 4(16.00) = 64.00$$

**Step 3:** Add — decimal places rule. Contributions have 3, 2, and 2 decimal places; the sum keeps **2 decimal places**:

$$2.016 + 32.06 + 64.00 = 98.076 \longrightarrow 98.08 \text{ g/mol}$$

**Answer: $98.08$ g/mol.**

### Example 9: Exact Numbers Don't Vote

**Problem:** Three trials of a titration used $24.31$ mL, $24.35$ mL, and $24.27$ mL of $\ce{NaOH}$ solution. Report the average volume.

**Solution:**

**Step 1 (addition — decimal places):** $24.31 + 24.35 + 24.27 = 72.93$ mL. All inputs have 2 decimal places → the sum keeps 2 decimal places.

**Step 2 (divide by 3):** The 3 is a **counted, exact** number — unlimited sig figs, so it doesn't limit the result:

$$\frac{72.93}{3} = 24.31 \text{ mL}$$

**Step 3:** The average keeps the precision of the data: $24.31$ mL (4 sig figs).

**Answer: $24.31$ mL.** If you'd treated "3" as 1 sig fig, you'd have butchered this to "20 mL" — exact numbers never vote.

### Example 10: Multi-Step with Guard Digits

**Problem:** Compute $(14.84 - 14.2) \times 3.955$ with correct sig figs.

**Solution:**

**Step 1 (subtraction — decimal places):** $14.84 - 14.2 = 0.64$. Fewest decimal places is 1 ($14.2$), so this step is *worth* 1 decimal place: $0.6$ — just **1 sig fig**. But don't round yet! Keep $0.64$ as a guard-digit value and jot "(1 sf)" in the margin.

**Step 2 (multiplication — sig figs):** $0.64 \times 3.955 = 2.5312$. The sig-fig budget: the subtraction result carries 1 sig fig, $3.955$ carries 4. Weakest link: **1 sig fig**.

**Step 3:** Round once, at the end: $2.5312 \to 3$.

**Answer: $3$** — and note the trap: rounding early to $0.6$ would give $0.6 \times 3.955 = 2.373 \to 2$. Premature rounding changed the answer entirely. Track the count early, round late.

### Example 11: Reading a Graduated Cylinder

**Problem:** A 50-mL graduated cylinder is marked every 1 mL. The bottom of the meniscus sits between the 43 and 44 mL lines, roughly one-quarter of the way up. What volume do you record, and with how many sig figs?

**Solution:**

**Step 1:** Certain digits from the markings: the meniscus is definitely past 43 and not at 44, so "43" is guaranteed.

**Step 2:** Estimate **exactly one** digit between the lines: about a quarter of the way → estimate 0.2 or 0.3 mL. Record $43.3$ mL (your estimate; a labmate honestly reading $43.2$ mL is also right — that last digit is the acknowledged uncertainty).

**Step 3:** Count: 4, 3, 3 → **3 sig figs**. Recording "43 mL" wastes information the instrument gave you; "43.25 mL" claims precision it didn't.

**Answer: $43.3$ mL, 3 sig figs (certain "43" + one estimated digit).**

### Example 12: Percent Error, Start to Finish

**Problem:** Ganga measures the density of aluminum as $2.71$ g/mL. The accepted value is $2.6989$ g/mL. Compute the percent error with correct sig figs.

**Solution:**

**Step 1 (subtraction — decimal places):** $2.71 - 2.6989 = 0.0111$. Fewest decimal places is 2 → worth $0.01$, i.e., **1 sig fig**. Keep $0.0111$ as guard digits.

**Step 2 (divide and scale):** 

$$\%\text{ error} = \frac{0.0111}{2.6989} \times 100\% = 0.41128...\%$$

The 100% is exact; the budget is 1 sig fig from Step 1.

**Step 3:** Round at the end: $0.4\%$.

**Answer: $0.4\%$** — small differences between close numbers hemorrhage sig figs. This is called *subtractive cancellation*, and it's why percent-error answers often deserve fewer digits than you'd guess.

---

## Common Mistakes

| The Mistake | Why It Happens | How to Avoid It |
|---|---|---|
| Using the sig-fig rule for addition (or the decimal-place rule for multiplication) | There are two rules and they look interchangeable | Say it out loud: **×/÷ → sig figs; +/− → decimal places.** Different operations, different rules |
| Counting leading zeros as significant ($0.0052$ ≠ 4 sig figs) | Zeros "look" like digits you wrote | Convert to scientific notation — if a zero vanishes ($5.2 \times 10^{-3}$), it was never significant |
| Treating $2500$ as definitely 4 sig figs | Trailing zeros feel deliberate | No decimal point → ambiguous, assume the fewest; write $2.500 \times 10^3$ if you mean 4 |
| Letting exact numbers limit the answer (dividing by 3 trials → 1 sig fig) | Forgetting counted/defined numbers are exact | Ask: "Did an instrument produce this number?" If not, it has unlimited sig figs |
| Rounding after every intermediate step | Feels tidy | Keep guard digits (or full calculator precision); track the count in the margin; round **once** at the end |
| Dropping trailing zeros from a balance readout ($2.3400 \to 2.34$ g) | Zeros feel optional | Digital display digits are all significant — copy every one |
| Recording a graduated cylinder to the marking only (no estimated digit) | "Between the lines" feels like guessing | One estimated digit past the finest marking is *required* — it's data, not a guess |
| Forgetting that subtraction of close numbers destroys precision | The inputs had lots of sig figs | After any subtraction, re-count what's left — the difference can have far fewer sig figs than the inputs |

---

## AP Exam Tips

- **The grading tolerance is real but not infinite.** On most AP Chemistry free-response parts, graders accept answers within **±1 significant figure** of the expected count — so if the ideal answer is $2.74$ g and you write $2.7$ g or $2.741$ g, you're typically fine. But report $2.7413628$ g (calculator vomit) or $3$ g (over-rounded), and the wildly wrong precision **can cost you the point**, usually on the one part of the question that explicitly grades sig figs.
- **One part per FRQ often targets sig figs directly.** Lab-based free-response questions frequently include a part that hinges on correct precision (often a mass-difference or volume-difference calculation). Subtraction steps are the favorite trap — recount decimal places after every subtraction.
- **Show the unrounded value, then the rounded one.** Writing $d = 8.6981 \to 8.7$ g/mL costs three seconds and shows the grader you rounded deliberately, not luckily.
- **Multiple choice rarely tests sig figs directly**, but answer choices are usually written with sensible precision — a choice with absurdly many digits is often a distractor.
- **Know your exact numbers.** Stoichiometric coefficients, subscripts, counted trials, and defined conversions (1 in = 2.54 cm exactly) never limit sig figs. The exam loves burying an exact "3" in an averaging step.
- **Logarithms play by different rules.** For pH and other logs, only the digits *after* the decimal point count as significant — $\text{pH} = 4.72$ has 2 sig figs, not 3. That's its own story, covered in [Logarithms for Chemistry](/chemistry/0104-logarithms-for-chemistry).
- **Calculator habit:** chain the whole computation in one line (or use the Ans key) so guard digits ride along automatically; only the final displayed number gets rounded onto your paper.

---

## Practice Problems

### Problem 1
How many significant figures are in each? (a) $305.0$  (b) $0.00047$  (c) $8.100 \times 10^{-2}$  (d) $90{,}600$

<details>
<summary><strong>Solution</strong></summary>

(a) $305.0$ — 3 and 5 count, the captive 0 counts, and the trailing zero counts because there's a decimal point → **4 sig figs**

(b) $0.00047$ — leading zeros never count → **2 sig figs**

(c) $8.100 \times 10^{-2}$ — scientific notation: every coefficient digit counts → **4 sig figs**

(d) $90{,}600$ — 9, captive 0, 6 count; the two trailing zeros have no decimal point → ambiguous, conventionally **3 sig figs**

**Answer: (a) 4, (b) 2, (c) 4, (d) 3.**

</details>

### Problem 2
Which of these are exact numbers? (a) The 2 in $\ce{2H2O}$; (b) a pipet's 10.00 mL delivery; (c) 12 eggs in a dozen; (d) 1 mile = 1.609 km (rounded); (e) 1000 m = 1 km.

<details>
<summary><strong>Solution</strong></summary>

(a) Coefficient in a chemical equation → **exact**

(b) An instrument delivered it (with tolerance) → **measured**, 4 sig figs

(c) Counted definition → **exact**

(d) $1.609$ is a *rounded* conversion, not a definition → **measured/limited**, 4 sig figs

(e) Metric prefixes are defined → **exact**

**Answer: (a), (c), and (e) are exact.**

</details>

### Problem 3
Round each to 3 sig figs: (a) $45.6712$  (b) $0.0039947$  (c) $7.1250$  (d) $124{,}500$

<details>
<summary><strong>Solution</strong></summary>

(a) Fourth digit is 7 → round up: **$45.7$**

(b) Sig figs start at 3: $3.9947 \times 10^{-3}$; fourth digit is 4 → keep: **$0.00399$**

(c) Dropping "50" — bare 5 case → round up: **$7.13$**

(d) $1.245 \times 10^5$; dropping the bare 5 → round up: **$1.25 \times 10^5$** (scientific notation avoids the trailing-zero ambiguity of writing $125{,}000$)

**Answer: (a) $45.7$, (b) $0.00399$, (c) $7.13$, (d) $1.25 \times 10^5$.**

</details>

### Problem 4
Compute with correct sig figs: $12.6 \times 0.53$

<details>
<summary><strong>Solution</strong></summary>

Multiplication → fewest sig figs rule. $12.6$ has 3; $0.53$ has 2 → answer gets 2.

$$12.6 \times 0.53 = 6.678 \longrightarrow 6.7$$

**Answer: $6.7$**

</details>

### Problem 5
Compute with correct sig figs: $108.71 + 0.6 + 15.882$

<details>
<summary><strong>Solution</strong></summary>

Addition → fewest **decimal places** rule. Decimal places: 2, 1, 3 → answer keeps 1.

$$108.71 + 0.6 + 15.882 = 125.192 \longrightarrow 125.2$$

**Answer: $125.2$**

</details>

### Problem 6
Compute with correct sig figs: $\dfrac{0.0450}{7.2}$

<details>
<summary><strong>Solution</strong></summary>

Sig figs: $0.0450$ has 3 (leading zeros don't count; the trailing zero does, decimal point present); $7.2$ has 2 → answer gets 2.

$$\frac{0.0450}{7.2} = 0.00625 \longrightarrow 0.0063$$

**Answer: $0.0063$** (or $6.3 \times 10^{-3}$)

</details>

### Problem 7
A watch glass has mass $32.115$ g. With a sample of $\ce{KNO3}$ on it, the total mass is $33.7$ g (read on a cheaper balance). What is the mass of the $\ce{KNO3}$?

<details>
<summary><strong>Solution</strong></summary>

Subtraction → decimal places rule.

$$33.7 - 32.115 = 1.585 \text{ g}$$

Decimal places: 1 and 3 → keep 1: $1.585 \to 1.6$ g.

**Answer: $1.6$ g** — the cheaper balance sets the precision of the difference, no matter how good the first reading was.

</details>

### Problem 8
A rectangular bar measures $2.15$ cm $\times$ $1.2$ cm $\times$ $0.85$ cm and has mass $5.4361$ g. Compute its density with correct sig figs.

<details>
<summary><strong>Solution</strong></summary>

**Volume (multiplication):** $2.15 \times 1.2 \times 0.85 = 2.193$ cm³ (keep guard digits). Sig-fig budget so far: fewest is 2 (both $1.2$ and $0.85$).

**Density (division):**

$$d = \frac{5.4361}{2.193} = 2.4788... \text{ g/cm}^3$$

Budget: 2 sig figs (from the volume inputs) vs. 5 (mass) → 2.

$$2.4788 \longrightarrow 2.5 \text{ g/cm}^3$$

**Answer: $2.5$ g/cm³**

</details>

### Problem 9
Four titration trials used $31.22$, $31.18$, $31.25$, and $31.19$ mL of titrant. Report the average with correct sig figs.

<details>
<summary><strong>Solution</strong></summary>

**Sum (addition):** $31.22 + 31.18 + 31.25 + 31.19 = 124.84$ mL — all inputs have 2 decimal places, so the sum keeps 2.

**Divide by 4:** the 4 is a counted, **exact** number — it doesn't limit precision.

$$\frac{124.84}{4} = 31.21 \text{ mL}$$

**Answer: $31.21$ mL** (4 sig figs, matching the data — the exact 4 never voted).

</details>

### Problem 10
Compute $(9.875 - 9.7) \div 0.4185$ with correct sig figs.

<details>
<summary><strong>Solution</strong></summary>

**Step 1 (subtraction):** $9.875 - 9.7 = 0.175$. Fewest decimal places is 1 → this is worth $0.2$: **1 sig fig**. Keep $0.175$ as guard digits.

**Step 2 (division):** $0.175 \div 0.4185 = 0.41816...$ Budget: 1 sig fig (from Step 1) vs. 4 → 1.

**Step 3 (round once):** $0.41816 \to 0.4$.

**Answer: $0.4$** — rounding early ($0.2 \div 0.4185 = 0.478 \to 0.5$) gives a different, wrong answer. Guard digits matter.

</details>

### Problem 11
A graduated cylinder marked every 0.1 mL shows the meniscus between the 8.6 and 8.7 mL lines, about halfway. (a) What do you record? (b) How many sig figs? (c) A labmate records "8.6 mL" — what did they do wrong?

<details>
<summary><strong>Solution</strong></summary>

(a) Certain digits: 8.6 (guaranteed by the markings). Estimate one digit between the lines: halfway → 0.05. Record **$8.65$ mL**.

(b) **3 sig figs** — 8 and 6 certain, 5 estimated.

(c) They stopped at the markings and skipped the required estimated digit — throwing away real information the instrument provides. Analog instruments are always read to one digit *past* the finest marking.

**Answer: (a) $8.65$ mL, (b) 3 sig figs, (c) they omitted the estimated digit.**

</details>

### Problem 12
Compute the molar mass of $\ce{Ca(OH)2}$ using $\ce{Ca} = 40.08$, $\ce{O} = 16.00$, $\ce{H} = 1.008$ (g/mol), with correct precision.

<details>
<summary><strong>Solution</strong></summary>

Subscripts are exact. Contributions:

$$1(40.08) = 40.08 \qquad 2(16.00) = 32.00 \qquad 2(1.008) = 2.016$$

Addition → decimal places: 2, 2, 3 → keep 2.

$$40.08 + 32.00 + 2.016 = 74.096 \longrightarrow 74.10 \text{ g/mol}$$

**Answer: $74.10$ g/mol**

</details>

### Problem 13
A digital balance displays $0.5200$ g for a sample of $\ce{NaCl}$. (a) How many sig figs should you record? (b) A student writes "0.52 g" in their notebook. On a later calculation dividing this mass by a volume of $4.815$ mL, how does that sloppy recording change the reported density?

<details>
<summary><strong>Solution</strong></summary>

(a) Digital display → copy every digit: $0.5200$ g has **4 sig figs** (leading zero doesn't count; both trailing zeros do).

(b) Correct: $0.5200 / 4.815 = 0.10800...$ → 4 sig figs → **$0.1080$ g/mL**.
Sloppy: $0.52$ g is 2 sig figs → $0.52/4.815 = 0.10800...$ → **$0.11$ g/mL**.

Same arithmetic, but the sloppy version *reports* half the precision the balance actually delivered — a self-inflicted downgrade.

**Answer: (a) 4 sig figs; (b) the honest report drops from $0.1080$ to $0.11$ g/mL — two digits of real information lost.**

</details>

### Problem 14
Dad's lab micrometer says a single sheet of printer paper is $0.104$ mm thick. A stack of 12 identical sheets (counted) should be how thick? Report with correct sig figs.

<details>
<summary><strong>Solution</strong></summary>

The 12 is a **counted, exact** number — unlimited sig figs. The measurement $0.104$ mm has 3 (the leading zero never counts; the captive zero does).

$$12 \times 0.104 = 1.248 \longrightarrow 1.25 \text{ mm}$$

The answer keeps 3 sig figs (from the measurement, the only voter).

**Answer: $1.25$ mm** — if you'd treated 12 as 2 sig figs, you'd have written 1.2 mm and thrown away a digit for no reason.

</details>

### Problem 15
An experiment gives a measured value of $1.362$ g/mL against an accepted value of $1.3584$ g/mL. Compute the percent error with correct sig figs, and explain why the answer has fewer sig figs than either input.

<details>
<summary><strong>Solution</strong></summary>

**Step 1 (subtraction — decimal places):** $1.362 - 1.3584 = 0.0036$. Fewest decimal places is 3 → worth $0.004$: **1 sig fig**. Keep $0.0036$ as guard digits.

**Step 2 (divide and scale; 100% is exact):**

$$\%\text{ error} = \frac{0.0036}{1.3584} \times 100\% = 0.26502...\%$$

**Step 3 (round once):** budget is 1 sig fig → $0.3\%$.

Why so few digits? Subtracting two nearly equal numbers cancels their shared leading digits, leaving only the uncertain tail — *subtractive cancellation*. Both inputs had 4–5 sig figs, but their *difference* only had 1.

**Answer: $0.3\%$**

</details>

---

## Quick Reference

| Situation | Rule |
|---|---|
| Nonzero digits | Always significant |
| Captive zeros ($3.07$) | Always significant |
| Leading zeros ($0.0025$) | **Never** significant |
| Trailing zeros, decimal point present ($2.500$) | Significant |
| Trailing zeros, no decimal point ($2500$) | Ambiguous — use scientific notation |
| Scientific notation | Every coefficient digit is significant |
| Exact numbers (counts, definitions, subscripts) | Unlimited sig figs — never limit the answer |
| Multiplication / division | Fewest **sig figs** among inputs |
| Addition / subtraction | Fewest **decimal places** among inputs |
| Multi-step calculations | Keep guard digits; track the count; round **once** at the end |
| Rounding a bare 5 | Round up (AP-safe convention) |
| Analog instrument (ruler, graduated cylinder) | All certain digits + **one** estimated digit past the finest marking |
| Digital instrument (balance) | Record **every** displayed digit, including trailing zeros |
| Logs and pH | Different rules — see [Logarithms for Chemistry](/chemistry/0104-logarithms-for-chemistry) |

---

<div align="center">

[← Scientific Notation](/chemistry/0101-scientific-notation) | [Dimensional Analysis →](/chemistry/0103-dimensional-analysis)

</div>
