# Scientific Notation
<p class="article-date">July 4, 2026</p>

*Last weekend I was at Torrey Pines, sitting on the sand after a hike, and I tried to guess how many grains of sand were just in the patch under my towel. I gave up somewhere around "a lot, times a lot." Then I got home, opened my chem textbook, and learned that a single drop of water contains about $1.67 \times 10^{21}$ molecules of $\ce{H2O}$ — more molecules in one drop than grains of sand on that entire beach. Chemistry lives at two absurd extremes: numbers so large they don't fit in your head (molecules per drop) and numbers so small they barely exist (one carbon atom has a mass of about $1.99 \times 10^{-23}$ grams). Scientific notation is the carrying case for these numbers, and it has exactly two parts: the **coefficient** holds the interesting digits, and the **exponent** records how far the decimal point traveled to get there. Master this one skill and every calculation in AP Chemistry — moles, wavelengths, atomic masses, equilibrium constants — stops being scary and starts being bookkeeping.*

---

## What You'll Learn

- Write any number in proper scientific notation, $a \times 10^n$ with $1 \le a < 10$
- Convert between standard form and scientific notation in both directions, for large and small numbers
- Use the metric prefixes from giga to pico (chemistry runs on nm, kJ, and mmol)
- Multiply and divide numbers in scientific notation by adding and subtracting exponents
- Raise a number in scientific notation to a power
- Add and subtract in scientific notation by matching exponents first — the step everyone forgets
- Use your calculator's EE/EXP button correctly and avoid the classic "×10^" order-of-operations trap
- Estimate answers to powers-of-ten problems in your head, AP-style, without a calculator

---

## The Core Concept

### Intuition First

Back to the beach. Suppose I somehow counted the grains of sand under my towel and got:

$$52{,}000{,}000{,}000$$

If I text that to you, you have to stop and count zeros to even read it. But notice that only two digits in that number actually carry information — the 5 and the 2. Everything else is just the decimal point being *far away* from them.

Scientific notation splits the number into those two jobs:

- The **coefficient** ($5.2$) — the interesting digits, the part you actually measured
- The **exponent** ($10^{10}$) — how far the decimal point traveled, i.e., how *big* the number is

$$52{,}000{,}000{,}000 = 5.2 \times 10^{10}$$

Same idea for tiny numbers. The mass of one carbon-12 atom is

$$0.0000000000000000000000199 \text{ g} = 1.99 \times 10^{-23} \text{ g}$$

The coefficient $1.99$ holds the measurement; the exponent $-23$ says the decimal traveled 23 places to the *left* of where it started — the number is small. One glance at the exponent tells you the scale; one glance at the coefficient tells you the value. That separation is the entire trick, and it's why chemists can compare a count of $6.022 \times 10^{23}$ atoms to a mass of $1.99 \times 10^{-23}$ g without their heads exploding.

### Anatomy of Scientific Notation

A number is in **proper scientific notation** when it's written as

$$a \times 10^n \quad \text{where} \quad 1 \le a < 10 \text{ and } n \text{ is an integer}$$

- $a$ is the **coefficient** (also called the mantissa). It must be at least 1 and strictly less than 10 — exactly one nonzero digit to the left of the decimal point.
- $n$ is the **exponent**. Positive $n$ means a large number ($\ge 10$); negative $n$ means a small number ($< 1$); $n = 0$ means the number is already between 1 and 10.

So $6.022 \times 10^{23}$ is proper. But $60.22 \times 10^{22}$ and $0.6022 \times 10^{24}$ are the same value written *improperly* — the coefficient is outside $[1, 10)$.

**Converting standard → scientific:** Move the decimal point until exactly one nonzero digit sits to its left. Count the moves.

- Decimal moved **left** (big number) → exponent is **positive**, equal to the number of moves
- Decimal moved **right** (small number) → exponent is **negative**

$$300{,}000{,}000 \text{ m/s} \;\to\; 3.00 \times 10^{8} \text{ m/s} \quad (\text{8 moves left})$$

$$0.00052 \text{ m} \;\to\; 5.2 \times 10^{-4} \text{ m} \quad (\text{4 moves right})$$

**Converting scientific → standard:** Reverse it. Positive exponent → move the decimal right (pad with zeros); negative exponent → move it left.

A quick sanity check that never fails: after converting, ask "is this a big number or a small number?" Big numbers get positive exponents. Small numbers get negative exponents. If $0.00052$ somehow became $5.2 \times 10^{4}$, the sign is screaming at you that something went wrong.

### Metric Prefixes: Scientific Notation with Names

Chemistry doesn't just use powers of ten — it *names* them. A wavelength of $5.32 \times 10^{-7}$ m is announced as 532 **nano**meters. An energy of $2.45 \times 10^{5}$ J is 245 **kilo**joules. Learn this table cold; it comes up in literally every unit of the course.

| Prefix | Symbol | Power of 10 | Meaning | Chemistry sighting |
|---|---|---|---|---|
| giga | G | $10^{9}$ | billion | GHz (spectroscopy frequencies) |
| mega | M | $10^{6}$ | million | MJ (large energy changes) |
| kilo | k | $10^{3}$ | thousand | kJ/mol (bond energies, $\Delta H$) |
| — | — | $10^{0}$ | base unit | g, m, s, J, mol |
| deci | d | $10^{-1}$ | tenth | dm³ (1 dm³ = 1 L) |
| centi | c | $10^{-2}$ | hundredth | cm (glassware) |
| milli | m | $10^{-3}$ | thousandth | mL, mmol (titrations) |
| micro | µ | $10^{-6}$ | millionth | µg, µm (trace amounts) |
| nano | n | $10^{-9}$ | billionth | nm (wavelengths of light) |
| pico | p | $10^{-12}$ | trillionth | pm (atomic radii) |

The conversion move: replace the prefix with its power of ten.

$$532 \text{ nm} = 532 \times 10^{-9} \text{ m} = 5.32 \times 10^{-7} \text{ m}$$

### Multiplying and Dividing: Exponents Add and Subtract

This is where scientific notation pays rent. Because $10^m \times 10^n = 10^{m+n}$:

$$(a \times 10^m)(b \times 10^n) = (a \cdot b) \times 10^{m+n}$$

$$\frac{a \times 10^m}{b \times 10^n} = \frac{a}{b} \times 10^{m-n}$$

Multiply/divide the coefficients like normal numbers; **add** exponents when multiplying, **subtract** when dividing. If the resulting coefficient falls outside $[1, 10)$, slide the decimal one spot and fix the exponent.

**Raising to a power** distributes over both parts:

$$(a \times 10^n)^p = a^p \times 10^{n \cdot p}$$

Note the exponent gets *multiplied* by $p$, not raised to it.

### Adding and Subtracting: Match Exponents First

Here's the step students forget. You can only add coefficients when the exponents **match**, because you can only add quantities measured on the same scale. It's like adding money: you can't add "4.5 thousand dollars" to "3.2 hundred dollars" until you express both in the same unit.

$$4.5 \times 10^{3} + 3.2 \times 10^{2} = 4.5 \times 10^{3} + 0.32 \times 10^{3} = 4.82 \times 10^{3}$$

The rule: rewrite the smaller-exponent number so its exponent matches the larger one (its coefficient temporarily leaves the $[1,10)$ range — that's fine mid-calculation), add or subtract the coefficients, then re-normalize if needed.

### Calculator Skills: The EE Button Is Your Friend

Every scientific calculator has a button labeled **EE**, **EXP**, or **×10ⁿ**. It means "times ten to the." To enter $6.022 \times 10^{23}$, press:

$$6.022 \;\; \boxed{\text{EE}} \;\; 23$$

The calculator treats the whole thing as **one number**. That's the crucial part.

**The trap:** typing it out as `6.022 × 10 ^ 23` creates *three* numbers glued together by operations, and order of operations will betray you the moment you divide. Watch:

$$\text{You want: } \frac{8.0 \times 10^3}{2.0 \times 10^3} = 4.0$$

But if you type `8.0 × 10^3 ÷ 2.0 × 10^3`, the calculator computes left to right: $8000 \div 2 = 4000$, then $\times 10^3 = 4{,}000{,}000$. You wanted $4.0$ and got $4.0 \times 10^{6}$ — off by six orders of magnitude, and the calculator never blinked. With EE, the denominator stays a single package and the answer comes out right. On the AP exam this single habit prevents an entire category of wrong answers.

### Estimation: Powers-of-Ten Mental Math

AP Chemistry loves asking "which is the best estimate?" questions where the answer choices differ by factors of 10 — no precise arithmetic needed, just exponent bookkeeping. The method:

1. Round every coefficient to one digit ($6.022 \to 6$, $2.9 \to 3$)
2. Multiply/divide the little coefficients in your head
3. Add/subtract the exponents
4. Re-normalize

Estimate $\dfrac{(6 \times 10^{23})(3 \times 10^{-11})}{2 \times 10^{6}}$: coefficients give $6 \times 3 / 2 = 9$; exponents give $23 + (-11) - 6 = 6$. Answer: about $9 \times 10^{6}$. Ten seconds, no calculator. This is the same skill you'll use constantly to *check* calculator answers — if your estimate says $\sim 10^{6}$ and the screen says $10^{12}$, you mistyped something.

---

## Worked Examples

### Example 1: Large Number → Scientific Notation

**Problem:** A single drop of water contains about $1{,}670{,}000{,}000{,}000{,}000{,}000{,}000$ molecules of $\ce{H2O}$. Express this in scientific notation.

**Solution:**

**Step 1:** Place the decimal after the first nonzero digit: $1.67$.

**Step 2:** Count how many places the decimal moved from the end of the number to that position: 21 places to the left.

**Step 3:** Left movement on a big number → positive exponent.

**Answer:** $1.67 \times 10^{21}$ molecules

### Example 2: Small Number → Scientific Notation

**Problem:** One carbon-12 atom has a mass of $0.0000000000000000000000199$ g. Express this in scientific notation.

**Solution:**

**Step 1:** Move the decimal right until one nonzero digit is to its left: $1.99$.

**Step 2:** Count the moves: 23 places to the right.

**Step 3:** Right movement on a small number → negative exponent.

**Answer:** $1.99 \times 10^{-23}$ g

### Example 3: Scientific Notation → Standard Form (Both Directions)

**Problem:** Write (a) the speed of light, $3.00 \times 10^{8}$ m/s, and (b) a hydrogen ion concentration of $2.5 \times 10^{-4}$ M in standard decimal form.

**Solution:**

**Step 1 (a):** Positive exponent 8 → move the decimal 8 places right, padding zeros: $3.00 \to 300{,}000{,}000$.

**Step 2 (b):** Negative exponent 4 → move the decimal 4 places left: $2.5 \to 0.00025$.

**Answer:** (a) $300{,}000{,}000$ m/s  (b) $0.00025$ M

### Example 4: Fixing Improper Notation

**Problem:** Rewrite $47.5 \times 10^{3}$ and $0.082 \times 10^{-2}$ in proper scientific notation.

**Solution:**

**Step 1:** $47.5$ is too big (must be $< 10$). Move the decimal 1 place left, which multiplies the exponent's job by 10, so add 1 to the exponent: $47.5 \times 10^{3} = 4.75 \times 10^{4}$.

**Step 2:** $0.082$ is too small (must be $\ge 1$). Move the decimal 2 places right, so subtract 2 from the exponent: $0.082 \times 10^{-2} = 8.2 \times 10^{-4}$.

**Step 3:** Check both coefficients now sit in $[1, 10)$. ✓

**Answer:** $4.75 \times 10^{4}$ and $8.2 \times 10^{-4}$

### Example 5: Metric Prefix Conversions

**Problem:** (a) A green laser pointer emits light of wavelength 532 nm. Express this in meters. (b) A reaction releases $2.45 \times 10^{5}$ J. Express this in kJ.

**Solution:**

**Step 1 (a):** Replace the prefix: $532 \text{ nm} = 532 \times 10^{-9}$ m.

**Step 2 (a):** Normalize the coefficient: $532 = 5.32 \times 10^{2}$, so $5.32 \times 10^{2} \times 10^{-9} = 5.32 \times 10^{-7}$ m.

**Step 3 (b):** kilo means $10^{3}$, so divide by $10^{3}$ (subtract 3 from the exponent): $2.45 \times 10^{5} \text{ J} = 2.45 \times 10^{2}$ kJ.

**Answer:** (a) $5.32 \times 10^{-7}$ m  (b) $245$ kJ

### Example 6: Multiplication (Add the Exponents)

**Problem:** A sample contains $2.5 \times 10^{-3}$ mol of gold. Given that one mole contains $6.022 \times 10^{23}$ atoms (full story in [The Mole](/chemistry/0207-the-mole)), how many gold atoms is that?

**Solution:**

**Step 1:** Multiply the coefficients: $2.5 \times 6.022 = 15.055 \approx 15.1$.

**Step 2:** Add the exponents: $-3 + 23 = 20$.

**Step 3:** Combine and normalize: $15.1 \times 10^{20} = 1.51 \times 10^{21}$.

**Answer:** $1.51 \times 10^{21}$ atoms of $\ce{Au}$

### Example 7: Division (Subtract the Exponents)

**Problem:** One mole of carbon-12 has a mass of exactly 12.0 g and contains $6.022 \times 10^{23}$ atoms. Find the mass of a single $\ce{^{12}_{6}C}$ atom.

**Solution:**

**Step 1:** Set up the division: $\dfrac{12.0}{6.022 \times 10^{23}} = \dfrac{1.20 \times 10^{1}}{6.022 \times 10^{23}}$.

**Step 2:** Divide the coefficients: $1.20 / 6.022 = 0.199$.

**Step 3:** Subtract the exponents: $1 - 23 = -22$, giving $0.199 \times 10^{-22}$.

**Step 4:** Normalize: $0.199 \times 10^{-22} = 1.99 \times 10^{-23}$.

**Answer:** $1.99 \times 10^{-23}$ g per atom — matching our beach-day number from the opener.

### Example 8: Raising to a Power

**Problem:** A cubic salt crystal has an edge length of $2.0 \times 10^{-3}$ m. Find its volume.

**Solution:**

**Step 1:** Volume of a cube: $V = s^3 = (2.0 \times 10^{-3})^3$.

**Step 2:** Cube the coefficient: $2.0^3 = 8.0$.

**Step 3:** Multiply the exponent by 3: $10^{(-3) \times 3} = 10^{-9}$.

**Answer:** $V = 8.0 \times 10^{-9}$ m³

### Example 9: Addition (Match Exponents First)

**Problem:** A calorimetry setup absorbs $4.5 \times 10^{3}$ J in one stage and $3.2 \times 10^{2}$ J in a second stage. Find the total energy absorbed.

**Solution:**

**Step 1:** Exponents don't match (3 vs 2) — do NOT add $4.5 + 3.2$.

**Step 2:** Rewrite the smaller one to match the larger exponent: $3.2 \times 10^{2} = 0.32 \times 10^{3}$.

**Step 3:** Now add coefficients: $4.5 + 0.32 = 4.82$.

**Answer:** $4.82 \times 10^{3}$ J

### Example 10: Subtraction Across Scales

**Problem:** Two spectral lines have wavelengths $6.02 \times 10^{-7}$ m and $4.8 \times 10^{-8}$ m. Find the difference between them.

**Solution:**

**Step 1:** Match exponents — convert the second value: $4.8 \times 10^{-8} = 0.48 \times 10^{-7}$.

**Step 2:** Subtract coefficients: $6.02 - 0.48 = 5.54$.

**Step 3:** Keep the shared exponent: $10^{-7}$.

**Answer:** $5.54 \times 10^{-7}$ m

### Example 11: A Full Chemistry Calculation (Frequency of Light)

**Problem:** Calculate the frequency of the 532 nm green laser light from Example 5, using $\nu = \dfrac{c}{\lambda}$ with $c = 3.00 \times 10^{8}$ m/s.

**Solution:**

**Step 1:** Convert the wavelength (done in Example 5): $\lambda = 5.32 \times 10^{-7}$ m.

**Step 2:** Divide coefficients: $3.00 / 5.32 = 0.564$.

**Step 3:** Subtract exponents: $8 - (-7) = 15$, giving $0.564 \times 10^{15}$.

**Step 4:** Normalize: $5.64 \times 10^{14}$.

**Step 5:** Sanity check: visible light frequencies are $\sim 10^{14}$–$10^{15}$ Hz. ✓

**Answer:** $\nu = 5.64 \times 10^{14}$ Hz

### Example 12: No-Calculator Estimation

**Problem:** Without a calculator, estimate $\dfrac{(5.9 \times 10^{23})(3.1 \times 10^{-11})}{1.9 \times 10^{6}}$.

**Solution:**

**Step 1:** Round the coefficients: $5.9 \to 6$, $3.1 \to 3$, $1.9 \to 2$.

**Step 2:** Coefficients: $\dfrac{6 \times 3}{2} = 9$.

**Step 3:** Exponents: $23 + (-11) - 6 = 6$.

**Step 4:** Combine: about $9 \times 10^{6}$. (Exact answer: $9.6 \times 10^{6}$ — the estimate lands within 10%.)

**Answer:** $\approx 9 \times 10^{6}$

---

## Common Mistakes

| The Mistake | Why It Happens | How to Avoid It |
|---|---|---|
| Writing $34.5 \times 10^{4}$ as a final answer | Forgetting the coefficient must satisfy $1 \le a < 10$ | Always re-normalize at the end: $3.45 \times 10^{5}$ |
| Wrong exponent sign ($0.0005 \to 5 \times 10^{4}$) | Memorizing "left/right" rules without meaning | Sanity check: small numbers get *negative* exponents, big numbers get *positive* ones |
| Adding coefficients with mismatched exponents ($4.5 \times 10^3 + 3.2 \times 10^2 = 7.7 \times 10^?$) | Applying the multiplication shortcut to addition | Addition/subtraction requires **matching exponents first** — no exceptions |
| Multiplying exponents when multiplying numbers ($10^3 \times 10^2 = 10^6$) | Mixing up the rules for $\times$ and powers | Multiplying numbers → **add** exponents; raising to a power → **multiply** the exponent |
| Typing `× 10 ^` on the calculator instead of EE | The keystrokes *look* like the written math | Use EE/EXP always; it packages the value as one number and dodges order-of-operations disasters |
| Converting nm → m by multiplying by $10^{9}$ | Prefix direction confusion | Substitute the prefix's value: nano *is* $10^{-9}$, so $532 \text{ nm} = 532 \times 10^{-9}$ m |
| Dropping a negative sign when subtracting exponents ($10^{8} / 10^{-7} = 10^{1}$) | Rushing the arithmetic $8 - (-7)$ | Write the subtraction out: $8 - (-7) = 15$. Two seconds of care saves the whole problem |

---

## AP Exam Tips

- **You get a calculator on the entire AP Chemistry exam** (both multiple-choice and free-response) — but many multiple-choice questions are deliberately built so estimation is *faster* than typing. Answer choices often differ by powers of ten; nail the exponent and you're done.
- **Use the EE button, every time.** Graders never see your keystrokes, but a $10^6$-sized order-of-operations error turns a 4-point FRQ answer into zero points fast. When dividing by a number in scientific notation without EE, you'd need parentheses around the whole denominator — EE makes that automatic.
- **Report FRQ answers in proper scientific notation with units.** $1.99 \times 10^{-23}$ g earns the point; a string of 22 zeros invites transcription errors, and a missing unit can cost you.
- **Estimate before you calculate.** Jot the rounded powers-of-ten version in the margin ($\sim 9 \times 10^6$), then verify the calculator agrees to the right order of magnitude. This catches mistyped exponents instantly.
- **Know your magnitude landmarks:** Avogadro's number $\approx 6 \times 10^{23}$, atomic masses $\sim 10^{-23}$–$10^{-22}$ g, visible wavelengths 400–700 nm ($\sim 10^{-7}$ m), $c = 3.00 \times 10^{8}$ m/s. If an answer lands wildly off these scales, recheck.
- **Coefficient digits are where sig figs live** — the exponent never counts toward significant figures. That story continues in [Significant Figures](/chemistry/0102-significant-figures).

---

## Practice Problems

### Problem 1
Write $602{,}000{,}000{,}000{,}000{,}000{,}000{,}000$ in scientific notation.

<details>
<summary><strong>Solution</strong></summary>

Place the decimal after the first nonzero digit: $6.02$. The decimal moved 23 places left, so the exponent is $+23$.

**Answer: $6.02 \times 10^{23}$** (you'll be seeing this one again in [The Mole](/chemistry/0207-the-mole))

</details>

### Problem 2
Write $0.000000000167$ m (the approximate radius of a large atom family, in meters) in scientific notation.

<details>
<summary><strong>Solution</strong></summary>

Move the decimal right until one nonzero digit leads: $1.67$. That took 10 moves right, so the exponent is $-10$.

**Answer: $1.67 \times 10^{-10}$ m**

</details>

### Problem 3
The mass of an electron is $9.11 \times 10^{-28}$ g. Write this in standard decimal form.

<details>
<summary><strong>Solution</strong></summary>

Negative exponent 28 → move the decimal 28 places left, padding with zeros:

$$0.000000000000000000000000000911 \text{ g}$$

(Now you see why nobody writes it this way.)

**Answer: $0.000000000000000000000000000911$ g**

</details>

### Problem 4
Rewrite in proper scientific notation: (a) $0.36 \times 10^{5}$  (b) $125.6 \times 10^{-8}$

<details>
<summary><strong>Solution</strong></summary>

(a) Coefficient too small — move the decimal 1 right, subtract 1 from the exponent: $3.6 \times 10^{4}$.

(b) Coefficient too big — move the decimal 2 left, add 2 to the exponent: $1.256 \times 10^{-6}$.

**Answer: (a) $3.6 \times 10^{4}$  (b) $1.256 \times 10^{-6}$**

</details>

### Problem 5
Red light from a helium-neon laser has a wavelength of 633 nm. Express this in meters, in proper scientific notation.

<details>
<summary><strong>Solution</strong></summary>

Substitute the prefix: $633 \text{ nm} = 633 \times 10^{-9}$ m.

Normalize: $633 = 6.33 \times 10^{2}$, so $6.33 \times 10^{2-9} = 6.33 \times 10^{-7}$ m.

**Answer: $6.33 \times 10^{-7}$ m**

</details>

### Problem 6
A combustion reaction releases $6.5 \times 10^{4}$ J of energy. Express this in kJ.

<details>
<summary><strong>Solution</strong></summary>

kilo $= 10^{3}$, so divide by $10^{3}$: subtract 3 from the exponent.

$$6.5 \times 10^{4} \text{ J} = 6.5 \times 10^{1} \text{ kJ} = 65 \text{ kJ}$$

**Answer: $65$ kJ**

</details>

### Problem 7
A titration uses $2.4 \times 10^{-6}$ mol of indicator. Express this in µmol.

<details>
<summary><strong>Solution</strong></summary>

micro $= 10^{-6}$, so $2.4 \times 10^{-6}$ mol is exactly $2.4$ µmol — the exponent and the prefix cancel perfectly.

**Answer: $2.4$ µmol**

</details>

### Problem 8
Compute $(4.0 \times 10^{5})(2.0 \times 10^{-9})$.

<details>
<summary><strong>Solution</strong></summary>

Coefficients: $4.0 \times 2.0 = 8.0$. Exponents: $5 + (-9) = -4$.

**Answer: $8.0 \times 10^{-4}$**

</details>

### Problem 9
One mole of gold ($\ce{Au}$) has a mass of 197 g and contains $6.022 \times 10^{23}$ atoms. Find the mass of one gold atom.

<details>
<summary><strong>Solution</strong></summary>

$$\frac{197}{6.022 \times 10^{23}} = \frac{1.97 \times 10^{2}}{6.022 \times 10^{23}}$$

Coefficients: $1.97 / 6.022 = 0.327$. Exponents: $2 - 23 = -21$.

Normalize: $0.327 \times 10^{-21} = 3.27 \times 10^{-22}$.

**Answer: $3.27 \times 10^{-22}$ g**

</details>

### Problem 10
Compute $(3.0 \times 10^{4})^2$.

<details>
<summary><strong>Solution</strong></summary>

Square the coefficient: $3.0^2 = 9.0$. Multiply the exponent by 2: $4 \times 2 = 8$.

**Answer: $9.0 \times 10^{8}$**

</details>

### Problem 11
Add: $7.2 \times 10^{5} + 5.0 \times 10^{4}$.

<details>
<summary><strong>Solution</strong></summary>

Match exponents first: $5.0 \times 10^{4} = 0.50 \times 10^{5}$.

Add coefficients: $7.2 + 0.50 = 7.7$.

**Answer: $7.7 \times 10^{5}$**

</details>

### Problem 12
Subtract: $1.20 \times 10^{-3} - 4.0 \times 10^{-5}$.

<details>
<summary><strong>Solution</strong></summary>

Match exponents: $4.0 \times 10^{-5} = 0.040 \times 10^{-3}$.

Subtract coefficients: $1.20 - 0.040 = 1.16$.

**Answer: $1.16 \times 10^{-3}$**

</details>

### Problem 13
A hydrogen emission line has wavelength 486 nm. Calculate its frequency using $\nu = c/\lambda$ with $c = 3.00 \times 10^{8}$ m/s.

<details>
<summary><strong>Solution</strong></summary>

Convert: $486 \text{ nm} = 4.86 \times 10^{-7}$ m.

Coefficients: $3.00 / 4.86 = 0.617$. Exponents: $8 - (-7) = 15$.

Normalize: $0.617 \times 10^{15} = 6.17 \times 10^{14}$.

Sanity check: visible light lives around $10^{14}$–$10^{15}$ Hz. ✓

**Answer: $\nu = 6.17 \times 10^{14}$ Hz**

</details>

### Problem 14
Without a calculator, estimate the number of molecules in $2.0 \times 10^{-3}$ mol of $\ce{CO2}$ (one mole $\approx 6 \times 10^{23}$ molecules). Which power of ten is your answer closest to?

<details>
<summary><strong>Solution</strong></summary>

Coefficients: $2 \times 6 = 12$. Exponents: $-3 + 23 = 20$.

Combine: $12 \times 10^{20} = 1.2 \times 10^{21}$.

**Answer: about $1.2 \times 10^{21}$ molecules — closest to $10^{21}$**

</details>

### Problem 15
A student computes $\dfrac{8.0 \times 10^{3}}{2.0 \times 10^{3}}$ by typing `8.0 × 10^3 ÷ 2.0 × 10^3` into a calculator and gets $4{,}000{,}000$. (a) What is the correct answer? (b) Explain exactly what the calculator did wrong — or rather, what the student did wrong.

<details>
<summary><strong>Solution</strong></summary>

(a) Exponents subtract: $3 - 3 = 0$, and $8.0/2.0 = 4.0$, so the answer is $4.0 \times 10^{0} = 4.0$.

(b) The calculator worked left to right: $8.0 \times 10^{3} = 8000$, then $\div\, 2.0 = 4000$, then $\times\, 10^{3} = 4{,}000{,}000$. The trailing $10^{3}$ ended up *multiplying* instead of staying attached to the denominator. Entering each value with the EE button ($8.0\,\text{EE}\,3 \div 2.0\,\text{EE}\,3$) keeps each quantity packaged as a single number and gives $4.0$.

**Answer: $4.0$ — and always use EE, never a typed-out $\times 10^{\wedge}$**

</details>

---

## Quick Reference

| Task | Rule |
|---|---|
| Proper form | $a \times 10^n$ with $1 \le a < 10$, $n$ an integer |
| Big number ($\ge 10$) | Positive exponent; decimal moved left |
| Small number ($< 1$) | Negative exponent; decimal moved right |
| Multiply | Multiply coefficients, **add** exponents |
| Divide | Divide coefficients, **subtract** exponents |
| Power | Raise coefficient to the power, **multiply** the exponent by it |
| Add / subtract | **Match exponents first**, then combine coefficients |
| Calculator entry | Use **EE / EXP**, never a typed `× 10 ^` |
| Sanity check | Estimate with rounded coefficients + exponent arithmetic |

| Prefix | G | M | k | (base) | d | c | m | µ | n | p |
|---|---|---|---|---|---|---|---|---|---|---|
| Power | $10^{9}$ | $10^{6}$ | $10^{3}$ | $10^{0}$ | $10^{-1}$ | $10^{-2}$ | $10^{-3}$ | $10^{-6}$ | $10^{-9}$ | $10^{-12}$ |

---

<div align="center">

[← History of Chemistry](/chemistry/0002-history-of-chemistry) | [Significant Figures →](/chemistry/0102-significant-figures)

</div>
