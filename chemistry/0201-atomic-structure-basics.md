# Atomic Structure Basics
<p class="article-date">July 4, 2026</p>

*There's a giant LEGO bin in my closet — years of sets dumped into one plastic tub. Here's the wild part: every single build I've ever made, from a pirate ship to a moon base, came out of a surprisingly small catalog of brick types. The bricks don't care what you build; a 2×4 is a 2×4 whether it's a castle wall or a spaceship hull. The universe works exactly like that bin. Roughly 90 naturally occurring types of atoms build everything — boba pearls, smartphone chips, the cliffs at Torrey Pines, you. The brick type is the element, and it's defined by one number: the proton count. Same brick in a different color? That's an isotope — same protons, different neutrons. A brick with a missing or extra connector? That's an ion — the electron count changed, so it snaps onto other pieces differently. This article is the parts catalog for all of AP Chemistry: master it now, because Unit 1 (moles, mass spectrometry, electron structure) is built directly on top of it.*

---

## What You'll Learn
- Name the three subatomic particles and compare their charges, relative masses, and locations
- Explain why protons define an atom's identity but electrons control its chemistry
- Decode and write complete nuclear symbols in $\ce{^{A}_{Z}X}$ notation
- Define isotopes and count protons, neutrons, and electrons for any isotope
- Define cations and anions, and write ion symbols like $\ce{Ca^2+}$ and $\ce{Cl^-}$
- Fill out the classic AP-style particle-counting table for any isotope–ion combination
- Calculate average atomic mass from isotopic masses and abundances — and run the algebra backwards to find abundances from the average
- Read a mass spectrum of an element: peaks are isotopes, peak heights are abundances
- Use scientific notation to grasp the absurd size gap between the nucleus and the whole atom

---

## Prerequisites
- [Scientific Notation](/chemistry/0101-scientific-notation) — atomic sizes and masses live at $10^{-10}$ m and $10^{-27}$ kg; you cannot talk about atoms without it
- [Significant Figures](/chemistry/0102-significant-figures) — average atomic mass calculations must be rounded honestly

---

## The Core Concept

### Intuition First

Go back to the LEGO bin. When I sort it, I don't sort by color or by which set a piece came from — I sort by *stud count*, because that's what determines what a brick can do. Atoms have exactly one number like that: the **number of protons**. Change the proton count and you have changed the element, full stop. Six protons is carbon no matter what else is going on. Seven protons is nitrogen. There is no negotiation.

The other two particles are the "variants":

- **Neutrons** are the color of the brick. A red 2×4 and a blue 2×4 build the same wall — carbon with 6 neutrons and carbon with 8 neutrons do the same chemistry. But the color (neutron count) changes the *mass*, and sometimes the stability. These variants are **isotopes**.
- **Electrons** are the connectors. Add or remove studs and the brick suddenly snaps to different pieces. Add or remove electrons and the atom becomes an **ion** with completely different bonding behavior — it's still the same element (protons didn't change!), but how it connects to the world changed.

So the division of labor is clean: **protons define identity, neutrons define the mass variant, electrons define the chemistry.** Almost everything an atom *does* — bonding, reacting, conducting — is electron behavior, because electrons live on the outside where atoms actually touch each other. The nucleus just sits deep inside holding the ID card and nearly all the mass.

### The Three Subatomic Particles

| Particle | Symbol | Charge | Relative Mass (amu) | Location |
|---|---|---|---|---|
| Proton | $p^+$ | $+1$ | $\approx 1$ | Nucleus |
| Neutron | $n^0$ | $0$ | $\approx 1$ | Nucleus |
| Electron | $e^-$ | $-1$ | $\approx \dfrac{1}{1836} \approx 0.00055$ | Electron cloud (outside nucleus) |

Three takeaways from this table:

1. **Mass lives in the nucleus.** Protons and neutrons each weigh about 1 atomic mass unit (amu); an electron weighs about 1/1836 of that. Electrons are essentially massless for counting purposes.
2. **Charge balance.** A neutral atom has equal protons and electrons. The charges cancel.
3. **Chemistry happens at the surface.** Electrons are the only particles other atoms ever interact with directly. That's why gaining or losing electrons (ions) changes behavior so dramatically while gaining a neutron changes almost nothing.

### Atomic Number, Mass Number, and Nuclear Symbols

Two numbers describe any nucleus:

$$Z = \text{atomic number} = \text{number of protons}$$

$$A = \text{mass number} = \text{protons} + \text{neutrons}$$

which immediately gives you the neutron count:

$$N = A - Z$$

We package all of it into one symbol:

$$\ce{^{A}_{Z}X}$$

For example, $\ce{^{14}_{6}C}$ is carbon-14: $Z = 6$ protons (that's what makes it carbon), $A = 14$ total nucleons, so $14 - 6 = 8$ neutrons.

Because the element's name already tells you $Z$ (look it up on the periodic table), you'll often see the shorthand $\ce{^{14}C}$ or just "carbon-14." Same information.

### Isotopes: Same Element, Different Mass

**Isotopes** are atoms with the same $Z$ but different $N$ — same brick, different color. Hydrogen is the celebrity example because its three isotopes are the only ones with their own names:

| Isotope | Symbol | Protons | Neutrons | Nickname |
|---|---|---|---|---|
| Hydrogen-1 | $\ce{^{1}_{1}H}$ | 1 | 0 | Protium (99.98% of all H) |
| Hydrogen-2 | $\ce{^{2}_{1}H}$ | 1 | 1 | Deuterium |
| Hydrogen-3 | $\ce{^{3}_{1}H}$ | 1 | 2 | Tritium (radioactive) |

Carbon tells the same story: $\ce{^{12}_{6}C}$ is the stable, boring isotope that makes up 98.9% of the carbon in your boba straw, while $\ce{^{14}_{6}C}$ is the rare radioactive one that archaeologists use to date ancient artifacts. Chemically they behave identically — both form $\ce{CO2}$, both build proteins — because chemistry only sees the electrons, and both have 6.

### Ions: Cations and Anions

When an atom gains or loses **electrons** (never protons — that would change the element), it becomes an ion:

- **Cation**: *lost* electrons, net **positive** charge. Example: $\ce{Ca^2+}$ lost 2 electrons.
- **Anion**: *gained* electrons, net **negative** charge. Example: $\ce{Cl^-}$ gained 1 electron.

Memory hook: ca**t**ion has a "t" that looks like a plus sign; and cats are pawsitive.

The charge is written as a superscript after the symbol, and it counts *missing or extra electrons*:

$$\text{charge} = (\text{protons}) - (\text{electrons}) \quad \Longrightarrow \quad \text{electrons} = Z - \text{charge}$$

Check it: $\ce{Ca^2+}$ has $Z = 20$, charge $= +2$, so electrons $= 20 - 2 = 18$. $\ce{N^3-}$ has $Z = 7$, charge $= -3$, so electrons $= 7 - (-3) = 10$.

### The Complete Bookkeeping (The AP Counting Table)

Put it all together and any particle — isotope, ion, or both at once — is fully described by three equations:

$$\text{protons} = Z \qquad \text{neutrons} = A - Z \qquad \text{electrons} = Z - \text{charge}$$

This is the single most-tested piece of bookkeeping in early AP Chemistry. Practice until the three lines are automatic.

### Average Atomic Mass: The Weighted Average

Look at chlorine on the periodic table: 35.45 amu. But no chlorine atom weighs 35.45 amu — real atoms are $\ce{^{35}Cl}$ (34.969 amu) or $\ce{^{37}Cl}$ (36.966 amu). The periodic table reports the **weighted average** over the natural mix, exactly like a grade that's 75% tests and 25% homework:

$$\text{average atomic mass} = \sum_i (\text{fractional abundance}_i) \times (\text{isotopic mass}_i)$$

For chlorine (75.76% $\ce{^{35}Cl}$, 24.24% $\ce{^{37}Cl}$):

$$(0.7576)(34.969) + (0.2424)(36.966) = 26.49 + 8.961 = 35.45 \text{ amu}$$

Notice the answer is closer to 35 than to 37 — the average always leans toward the more abundant isotope. That's your built-in sanity check.

And here's where your algebra earns its keep: for a **two-isotope element**, if you know the average and both isotopic masses, you can solve for the abundances. Let $x$ = fraction of the lighter isotope; then $(1 - x)$ = fraction of the heavier one:

$$x \cdot m_1 + (1 - x) \cdot m_2 = \text{average mass}$$

One equation, one unknown. AP loves this in both directions.

### Mass Spectrometry: How We Actually Know (Unit 1 Bridge)

How did anyone measure that chlorine is 75.76% $\ce{^{35}Cl}$? A **mass spectrometer**: vaporize the sample, ionize the atoms, fling them through a magnetic field, and sort them by mass. The output is a **mass spectrum** — a bar graph where:

- **Position of each peak (x-axis)** = the mass of one isotope
- **Height of each peak (y-axis)** = the relative abundance of that isotope

So chlorine's spectrum shows two peaks: a tall one at 35 (height ≈ 76) and a shorter one at 37 (height ≈ 24). Read the peaks, and you can compute the average atomic mass; compute the average, and you can identify the element off the periodic table.

**This is not a preview of "someday" material — interpreting mass spectra of elements is literally AP Chemistry Unit 1, Topic 1.2.** Everything in this article is the on-ramp to it.

### How Small Is Small? (The Scientific Notation Payoff)

A typical atom has a radius around $1 \times 10^{-10}$ m. Its nucleus? Around $1 \times 10^{-15}$ m. Divide:

$$\frac{1 \times 10^{-10} \text{ m}}{1 \times 10^{-15} \text{ m}} = 10^{5}$$

The atom is about **100,000 times wider than its nucleus**. If the nucleus were a marble sitting on the 50-yard line, the electron cloud would end somewhere past the stadium parking lot — the atom is almost entirely empty space, with 99.97% of its mass crammed into a dot at the center. And since volume scales as radius cubed, the nucleus occupies roughly $1/(10^5)^3 = 10^{-15}$ of the atom's volume. This is exactly the kind of number that's meaningless without scientific notation — and effortless with it.

---

## Worked Examples

### Example 1: Reading a Nuclear Symbol

**Problem:** How many protons, neutrons, and electrons are in a neutral atom of $\ce{^{14}_{6}C}$?

**Solution:**

**Step 1:** The subscript is $Z$: protons $= 6$.

**Step 2:** Neutrons $= A - Z = 14 - 6 = 8$.

**Step 3:** The atom is neutral, so electrons $=$ protons $= 6$.

**Answer: 6 protons, 8 neutrons, 6 electrons.**

### Example 2: Writing the Nuclear Symbol

**Problem:** Write the full nuclear symbol for potassium-40.

**Solution:**

**Step 1:** "Potassium" fixes the identity: from the periodic table, $Z = 19$.

**Step 2:** The "-40" is the mass number: $A = 40$.

**Step 3:** Assemble as $\ce{^{A}_{Z}X}$.

**Answer: $\ce{^{40}_{19}K}$ (19 protons, $40 - 19 = 21$ neutrons).**

### Example 3: Hydrogen's Three Isotopes

**Problem:** Protium, deuterium, and tritium are $\ce{^{1}_{1}H}$, $\ce{^{2}_{1}H}$, and $\ce{^{3}_{1}H}$. What do they share, and what differs?

**Solution:**

**Step 1:** All three have $Z = 1$ — one proton each. That's what makes them all hydrogen (and, as neutral atoms, they each have 1 electron, so their chemistry is essentially identical).

**Step 2:** Neutrons $= A - Z$: protium has $1 - 1 = 0$, deuterium has $2 - 1 = 1$, tritium has $3 - 1 = 2$.

**Step 3:** Different neutron counts mean different masses: tritium is roughly three times as massive as protium.

**Answer: Same protons and electrons (identical chemistry); different neutrons — 0, 1, and 2 — giving different masses.**

### Example 4: Counting Particles in a Cation

**Problem:** How many protons, neutrons, and electrons are in $\ce{^{40}_{20}Ca^2+}$?

**Solution:**

**Step 1:** Protons $= Z = 20$. The $2+$ charge does *not* touch the proton count.

**Step 2:** Neutrons $= A - Z = 40 - 20 = 20$.

**Step 3:** Electrons $= Z - \text{charge} = 20 - (+2) = 18$. A cation *lost* electrons.

**Answer: 20 protons, 20 neutrons, 18 electrons.**

### Example 5: Isotope–Ion Combo (Anion)

**Problem:** Count the protons, neutrons, and electrons in $\ce{^{37}_{17}Cl^-}$.

**Solution:**

**Step 1:** Protons $= Z = 17$.

**Step 2:** Neutrons $= A - Z = 37 - 17 = 20$. (Careful: this heavy isotope has 20 neutrons, not the 18 you'd get from $\ce{^{35}Cl}$.)

**Step 3:** Electrons $= Z - \text{charge} = 17 - (-1) = 18$. An anion *gained* an electron.

**Answer: 17 protons, 20 neutrons, 18 electrons.**

### Example 6: The Mystery Particle (Classic AP Table)

**Problem:** A particle has 26 protons, 30 neutrons, and 24 electrons. Identify it and write its full symbol.

**Solution:**

**Step 1:** 26 protons means $Z = 26$: the element is iron, $\ce{Fe}$. Protons alone decide this.

**Step 2:** $A = Z + N = 26 + 30 = 56$.

**Step 3:** Charge $=$ protons $-$ electrons $= 26 - 24 = +2$.

**Answer: $\ce{^{56}_{26}Fe^2+}$ — an iron-56 cation.**

### Example 7: Average Atomic Mass from Abundances (Two Isotopes)

**Problem:** Chlorine is 75.76% $\ce{^{35}Cl}$ (mass 34.969 amu) and 24.24% $\ce{^{37}Cl}$ (mass 36.966 amu). Calculate its average atomic mass.

**Solution:**

**Step 1:** Convert percentages to fractional abundances: $0.7576$ and $0.2424$. (Quick check: they sum to 1.)

**Step 2:** Multiply each mass by its fraction:

$$(0.7576)(34.969) = 26.49 \text{ amu} \qquad (0.2424)(36.966) = 8.961 \text{ amu}$$

**Step 3:** Add: $26.49 + 8.961 = 35.45$ amu.

**Step 4:** Sanity check: 35.45 is much closer to 35 than 37, matching the fact that $\ce{^{35}Cl}$ dominates. ✓

**Answer: 35.45 amu — exactly the value printed on the periodic table.**

### Example 8: Average Atomic Mass with Three Isotopes

**Problem:** Magnesium has three isotopes: $\ce{^{24}Mg}$ (23.985 amu, 78.99%), $\ce{^{25}Mg}$ (24.986 amu, 10.00%), and $\ce{^{26}Mg}$ (25.983 amu, 11.01%). Find the average atomic mass.

**Solution:**

**Step 1:** Same formula, just three terms:

$$(0.7899)(23.985) + (0.1000)(24.986) + (0.1101)(25.983)$$

**Step 2:** Compute each product: $18.95 + 2.499 + 2.861$.

**Step 3:** Add: $24.31$ amu.

**Answer: 24.31 amu (periodic table: 24.31 ✓). The average sits just above 24 because $\ce{^{24}Mg}$ carries almost 79% of the weight.**

### Example 9: Reverse Problem — Abundances from the Average (Boron)

**Problem:** Boron's average atomic mass is 10.81 amu. Its isotopes are $\ce{^{10}B}$ (10.013 amu) and $\ce{^{11}B}$ (11.009 amu). Find the percent abundance of each.

**Solution:**

**Step 1:** Let $x$ = fraction of $\ce{^{10}B}$. Then the fraction of $\ce{^{11}B}$ is $1 - x$ (they must sum to 1).

**Step 2:** Set up the weighted average:

$$x(10.013) + (1 - x)(11.009) = 10.81$$

**Step 3:** Distribute and collect:

$$10.013x + 11.009 - 11.009x = 10.81 \implies -0.996x = -0.199 \implies x = 0.200$$

**Step 4:** So $\ce{^{10}B}$ is 20.0% and $\ce{^{11}B}$ is 80.0%. Sanity check: 10.81 is much closer to 11 than to 10, so the heavier isotope should dominate. ✓

**Answer: about 20.0% $\ce{^{10}B}$ and 80.0% $\ce{^{11}B}$.**

### Example 10: Reverse Problem — Copper

**Problem:** Copper (average mass 63.55 amu) has two isotopes: $\ce{^{63}Cu}$ (62.930 amu) and $\ce{^{65}Cu}$ (64.928 amu). Find both abundances.

**Solution:**

**Step 1:** Let $x$ = fraction of $\ce{^{63}Cu}$:

$$x(62.930) + (1 - x)(64.928) = 63.55$$

**Step 2:** Simplify:

$$64.928 - 1.998x = 63.55 \implies 1.998x = 1.378 \implies x = 0.6897$$

**Step 3:** Convert to percentages: 68.97% and $100 - 68.97 = 31.03\%$.

**Step 4:** Check: 63.55 leans strongly toward 63, so the light isotope should dominate. ✓

**Answer: about 69.0% $\ce{^{63}Cu}$ and 31.0% $\ce{^{65}Cu}$.**

### Example 11: Reading a Mass Spectrum

**Problem:** The mass spectrum of an unknown element shows exactly two peaks:

| Peak position (amu) | Relative height (%) |
|---|---|
| 85 | 72.2 |
| 87 | 27.8 |

Identify the element and estimate its average atomic mass.

**Solution:**

**Step 1:** Translate the spectrum: two peaks = two isotopes, with masses 85 and 87 amu and abundances 72.2% and 27.8%.

**Step 2:** Compute the weighted average:

$$(0.722)(85) + (0.278)(87) = 61.37 + 24.19 = 85.6 \text{ amu}$$

**Step 3:** Scan the periodic table for an average atomic mass near 85.6: rubidium ($\ce{Rb}$, 85.47 amu). (Our answer is slightly high only because we used whole-number peak masses.)

**Answer: The element is rubidium; average atomic mass ≈ 85.6 amu (accepted value 85.47 amu).**

### Example 12: The Scale of the Atom

**Problem:** A gold atom has a radius of about $1.44 \times 10^{-10}$ m; its nucleus has a radius of about $7.3 \times 10^{-15}$ m. How many times wider is the atom than its nucleus?

**Solution:**

**Step 1:** Set up the ratio:

$$\frac{1.44 \times 10^{-10}}{7.3 \times 10^{-15}}$$

**Step 2:** Divide the coefficients: $1.44 / 7.3 = 0.197$. Subtract the exponents: $10^{-10 - (-15)} = 10^{5}$.

**Step 3:** Combine and normalize: $0.197 \times 10^{5} = 1.97 \times 10^{4} \approx 2.0 \times 10^4$.

**Answer: The gold atom is about $2.0 \times 10^4$ (20,000) times wider than its nucleus — a marble in a stadium, with the rest empty space.**

---

## Common Mistakes

| The Mistake | Why It Happens | How to Avoid It |
|---|---|---|
| Changing the *proton* count when forming an ion | "Charge changed, so a charged particle count changed" — true, but it's the electrons | Ions are always electron gain/loss. Protons never change in chemistry. |
| Electrons $= Z + \text{charge}$ sign errors (e.g., $\ce{Ca^2+}$ → 22 electrons) | Adding the charge instead of subtracting | Use electrons $= Z - \text{charge}$, and gut-check: cation → *fewer* electrons, anion → *more* |
| Reading 35.45 off the periodic table and computing "neutrons $= 35.45 - 17 = 18.45$" | Confusing average atomic mass (a decimal average) with mass number $A$ (a whole-number count) | Neutrons come only from a *specific isotope's* mass number: $N = A - Z$. If no isotope is given, the neutron count is not defined. |
| Forgetting to convert % to a fraction in weighted averages | Plugging 75.76 instead of 0.7576 | If your "average atomic mass" comes out around 3,500 amu, you forgot to divide by 100 |
| Letting abundances not sum to 100% in reverse problems | Treating the two abundances as independent unknowns | Always define the second abundance as $1 - x$ — one unknown, one equation |
| Expecting the average atomic mass to be the midpoint of the isotope masses | Ignoring the weighting | The average is pulled toward the *more abundant* isotope; use that as a sanity check every time |
| Thinking isotopes have different chemical behavior | Mass feels important | Chemistry is electrons. Isotopes have identical electron counts, hence (essentially) identical chemistry — only mass-dependent physical properties differ. |

---

## AP Exam Tips

- **This is Unit 1 bread and butter.** Topic 1.2 (Mass Spectrometry of Elements) tests exactly the skills above: peaks → isotopes, heights → abundances, weighted average → identify the element. Expect at least one multiple-choice question showing a spectrum.
- **The "number of neutrons" trick.** If a question gives you only the element (no mass number), you *cannot* find the neutron count — and answer choices computed from the periodic-table average (like "18.45 neutrons") are traps. Neutrons require a specific isotope: $N = A - Z$.
- **Electrons contribute (almost) nothing to mass.** If asked why $\ce{Ca}$ and $\ce{Ca^2+}$ have essentially the same mass, the answer is that the two missing electrons carry a negligible fraction ($\sim 1/1836$ amu each) of the atom's mass. Never attribute mass differences to electrons.
- **Charge bookkeeping shows up inside bigger problems.** Later units assume you can instantly say $\ce{^{37}Cl^-}$ has 18 electrons. Drill it now so it costs you zero seconds in May.
- **Reverse-abundance problems are calculator-friendly algebra.** Set up $x \cdot m_1 + (1-x) \cdot m_2 = \bar{m}$, solve, and *always* sanity-check that the heavier-leaning average matches the heavier isotope dominating.
- **Justify with abundance language on FRQs.** A one-sentence answer like "the average atomic mass is closer to 63 than 65 because $\ce{^{63}Cu}$ has the greater natural abundance" is exactly the reasoning the rubric wants.
- **Sig figs still apply** to average atomic mass calculations — carry guard digits, round at the end.

---

## Practice Problems

### Problem 1
How many protons, neutrons, and electrons are in a neutral atom of $\ce{^{31}_{15}P}$?

<details>
<summary><strong>Solution</strong></summary>

Protons $= Z = 15$.

Neutrons $= A - Z = 31 - 15 = 16$.

Neutral atom: electrons $=$ protons $= 15$.

**Answer: 15 protons, 16 neutrons, 15 electrons.**

</details>

### Problem 2
Write the full nuclear symbol for uranium-238, and state its neutron count.

<details>
<summary><strong>Solution</strong></summary>

Uranium has $Z = 92$; the mass number is $A = 238$.

Symbol: $\ce{^{238}_{92}U}$.

Neutrons $= 238 - 92 = 146$.

**Answer: $\ce{^{238}_{92}U}$, with 146 neutrons.**

</details>

### Problem 3
Which of the following pairs are isotopes of each other? (a) $\ce{^{14}_{6}C}$ and $\ce{^{14}_{7}N}$; (b) $\ce{^{16}_{8}O}$ and $\ce{^{18}_{8}O}$; (c) $\ce{^{40}_{18}Ar}$ and $\ce{^{40}_{20}Ca}$.

<details>
<summary><strong>Solution</strong></summary>

Isotopes require the **same $Z$** and different $A$.

(a) $Z = 6$ vs $Z = 7$ — different elements (same $A$ is irrelevant). Not isotopes.

(b) Both have $Z = 8$, with $A = 16$ and $18$ — same element, different neutron counts (8 vs 10). **Isotopes.** ✓

(c) $Z = 18$ vs $Z = 20$ — different elements that happen to share $A = 40$. Not isotopes.

**Answer: Only pair (b).**

</details>

### Problem 4
Count the protons, neutrons, and electrons in $\ce{^{27}_{13}Al^3+}$.

<details>
<summary><strong>Solution</strong></summary>

Protons $= 13$.

Neutrons $= 27 - 13 = 14$.

Electrons $= Z - \text{charge} = 13 - (+3) = 10$.

**Answer: 13 protons, 14 neutrons, 10 electrons.**

</details>

### Problem 5
Count the protons, neutrons, and electrons in $\ce{^{34}_{16}S^2-}$.

<details>
<summary><strong>Solution</strong></summary>

Protons $= 16$.

Neutrons $= 34 - 16 = 18$.

Electrons $= 16 - (-2) = 18$.

**Answer: 16 protons, 18 neutrons, 18 electrons.**

</details>

### Problem 6
A particle contains 35 protons, 44 neutrons, and 36 electrons. Write its full symbol.

<details>
<summary><strong>Solution</strong></summary>

$Z = 35$ → bromine, $\ce{Br}$.

$A = 35 + 44 = 79$.

Charge $= 35 - 36 = -1$ (one extra electron → anion).

**Answer: $\ce{^{79}_{35}Br^-}$.**

</details>

### Problem 7
Complete the table:

| Symbol | Protons | Neutrons | Electrons |
|---|---|---|---|
| $\ce{^{65}_{30}Zn^2+}$ | ? | ? | ? |
| ? | 7 | 8 | 10 |
| $\ce{^{88}_{38}Sr^2+}$ | ? | ? | ? |

<details>
<summary><strong>Solution</strong></summary>

Row 1: protons $= 30$; neutrons $= 65 - 30 = 35$; electrons $= 30 - 2 = 28$.

Row 2: $Z = 7$ → nitrogen; $A = 7 + 8 = 15$; charge $= 7 - 10 = -3$ → $\ce{^{15}_{7}N^3-}$.

Row 3: protons $= 38$; neutrons $= 88 - 38 = 50$; electrons $= 38 - 2 = 36$.

**Answer: Row 1: 30 p, 35 n, 28 e. Row 2: $\ce{^{15}_{7}N^3-}$. Row 3: 38 p, 50 n, 36 e.**

</details>

### Problem 8
Lithium is 7.59% $\ce{^{6}Li}$ (6.015 amu) and 92.41% $\ce{^{7}Li}$ (7.016 amu). Calculate its average atomic mass.

<details>
<summary><strong>Solution</strong></summary>

$$(0.0759)(6.015) + (0.9241)(7.016) = 0.4565 + 6.484 = 6.94 \text{ amu}$$

Sanity check: dominated by $\ce{^{7}Li}$, so the average should hug 7 from below. ✓

**Answer: 6.94 amu.**

</details>

### Problem 9
Silver has two isotopes: $\ce{^{107}Ag}$ (106.905 amu, 51.84%) and $\ce{^{109}Ag}$ (108.905 amu, 48.16%). Find silver's average atomic mass.

<details>
<summary><strong>Solution</strong></summary>

$$(0.5184)(106.905) + (0.4816)(108.905) = 55.42 + 52.45 = 107.87 \text{ amu}$$

The abundances are nearly 50/50, so the average lands near the midpoint (108), leaning slightly toward 107. ✓

**Answer: 107.87 amu.**

</details>

### Problem 10
Bromine (average atomic mass 79.904 amu) has isotopes $\ce{^{79}Br}$ (78.918 amu) and $\ce{^{81}Br}$ (80.916 amu). Find the percent abundance of each isotope.

<details>
<summary><strong>Solution</strong></summary>

Let $x$ = fraction of $\ce{^{79}Br}$:

$$x(78.918) + (1 - x)(80.916) = 79.904$$

$$80.916 - 1.998x = 79.904 \implies 1.998x = 1.012 \implies x = 0.5065$$

So $\ce{^{79}Br}$ is 50.65% and $\ce{^{81}Br}$ is 49.35% — bromine is famously an almost even split, which is why its average sits near 80, halfway between the isotopes.

**Answer: 50.65% $\ce{^{79}Br}$, 49.35% $\ce{^{81}Br}$.**

</details>

### Problem 11
Europium (average atomic mass 151.96 amu) has isotopes $\ce{^{151}Eu}$ (150.920 amu) and $\ce{^{153}Eu}$ (152.921 amu). Which isotope is more abundant, and by how much? Solve for both abundances.

<details>
<summary><strong>Solution</strong></summary>

Before any algebra: 151.96 is a bit past the midpoint (151.92) toward 153, so $\ce{^{153}Eu}$ should be slightly more abundant.

Let $x$ = fraction of $\ce{^{151}Eu}$:

$$x(150.920) + (1 - x)(152.921) = 151.96$$

$$152.921 - 2.001x = 151.96 \implies 2.001x = 0.961 \implies x = 0.480$$

So $\ce{^{151}Eu}$ ≈ 48.0% and $\ce{^{153}Eu}$ ≈ 52.0% — matching the prediction. ✓

**Answer: $\ce{^{153}Eu}$ is more abundant: about 52.0% vs 48.0%.**

</details>

### Problem 12
The mass spectrum of gallium shows two peaks: mass 68.926 amu with relative abundance 60.11%, and mass 70.925 amu with relative abundance 39.89%. Identify the two isotopes in symbol form and compute the average atomic mass.

<details>
<summary><strong>Solution</strong></summary>

Gallium has $Z = 31$, and the peak masses round to mass numbers 69 and 71: the isotopes are $\ce{^{69}_{31}Ga}$ and $\ce{^{71}_{31}Ga}$.

$$(0.6011)(68.926) + (0.3989)(70.925) = 41.43 + 28.29 = 69.72 \text{ amu}$$

**Answer: $\ce{^{69}_{31}Ga}$ and $\ce{^{71}_{31}Ga}$; average atomic mass = 69.72 amu.**

</details>

### Problem 13
An element's mass spectrum shows three peaks: at 24 amu (height 79), 25 amu (height 10), and 26 amu (height 11). Identify the element and estimate its average atomic mass.

<details>
<summary><strong>Solution</strong></summary>

Three peaks = three isotopes with masses ≈ 24, 25, 26 amu and abundances 79%, 10%, 11% (heights already sum to 100).

$$(0.79)(24) + (0.10)(25) + (0.11)(26) = 18.96 + 2.50 + 2.86 = 24.3 \text{ amu}$$

An average atomic mass of 24.3 amu matches magnesium ($\ce{Mg}$, 24.31 amu) on the periodic table.

**Answer: Magnesium; average atomic mass ≈ 24.3 amu.**

</details>

### Problem 14
(a) A carbon atom has a radius of about $7.0 \times 10^{-11}$ m and its nucleus a radius of about $2.7 \times 10^{-15}$ m. How many times wider is the atom than its nucleus? (b) A $\ce{^{12}C}$ atom has 6 protons, 6 neutrons (≈1 amu each), and 6 electrons (≈1/1836 amu each). Approximately what *fraction* of the atom's mass do the electrons contribute?

<details>
<summary><strong>Solution</strong></summary>

**(a)** Ratio:

$$\frac{7.0 \times 10^{-11}}{2.7 \times 10^{-15}} = \frac{7.0}{2.7} \times 10^{4} = 2.6 \times 10^{4}$$

The atom is about 26,000 times wider than its nucleus.

**(b)** Electron mass: $6 \times \frac{1}{1836} = 3.27 \times 10^{-3}$ amu. Total mass ≈ 12 amu.

$$\frac{3.27 \times 10^{-3}}{12} = 2.7 \times 10^{-4} \approx 0.03\%$$

**Answer: (a) about $2.6 \times 10^4$ times wider; (b) electrons contribute only ≈ 0.03% of the mass — the nucleus holds 99.97% of it.**

</details>

---

## Quick Reference

| Concept | Formula / Rule |
|---|---|
| Proton | charge $+1$, mass $\approx 1$ amu, in nucleus — **defines the element** |
| Neutron | charge $0$, mass $\approx 1$ amu, in nucleus — defines the isotope |
| Electron | charge $-1$, mass $\approx \frac{1}{1836}$ amu, outside nucleus — **does the chemistry** |
| Nuclear symbol | $\ce{^{A}_{Z}X}$, e.g. $\ce{^{14}_{6}C}$ |
| Atomic number | $Z =$ protons |
| Mass number | $A =$ protons $+$ neutrons (whole number, per isotope) |
| Neutrons | $N = A - Z$ |
| Electrons (in an ion) | $Z - \text{charge}$ (cation: fewer $e^-$; anion: more $e^-$) |
| Isotopes | same $Z$, different $N$ — identical chemistry, different mass |
| Average atomic mass | $\sum (\text{fractional abundance}) \times (\text{isotopic mass})$ |
| Two-isotope reverse solve | $x\, m_1 + (1 - x)\, m_2 = \bar{m}$, solve for $x$ |
| Mass spectrum | peak position $=$ isotope mass; peak height $=$ abundance |
| Scale | atom $\sim 10^{-10}$ m, nucleus $\sim 10^{-15}$ m — a $10^5$ size gap |

---

<div align="center">

[← Graphing and Linearization](/chemistry/0105-graphing-linearization) | [Periodic Table Map →](/chemistry/0202-periodic-table-map)

</div>
