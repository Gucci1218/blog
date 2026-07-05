# Photoelectron Spectroscopy
<p class="article-date">July 4, 2026</p>

*Last Saturday our neighbors moved out, and Dad volunteered us to help load the truck. Within an hour I'd noticed something: not all boxes cost the same effort. Boxes staged on the porch? Grab and go. Boxes from the upstairs bedroom? A whole stair-flight of work each. And the stuff locked in the basement safe — old documents, grandma's china — took two of us and serious grunting per box. Half-joking, I started logging the effort for every single box, and when I plotted my log that night, the data had clumps: one clump per storage spot, and the height of each clump told me how many boxes had lived there. Here's the wild part — a total stranger looking only at my plot could reconstruct the layout of a house they'd never seen. That is exactly what photoelectron spectroscopy (PES) does to an atom: light knocks electrons out, each electron's "effort cost" (binding energy) reveals which subshell it lived in, peak height reveals how many electrons that subshell held — and from the spectrum alone you can rebuild the whole electron configuration and name the element. In AP Unit 1, PES is the experimental receipt that proves shells and subshells are real, and it shows up on the exam every single year.*

---

## What You'll Learn

- Explain what PES measures: light ejects electrons from atoms, and we record the binding (ionization) energy of *every* electron — core and valence alike
- Read a PES spectrum: x-axis = binding energy (which **decreases** left to right on AP diagrams!), y-axis = relative number of electrons, one peak per subshell
- Use Coulomb's law logic to predict peak positions: closer to the nucleus = higher binding energy, more protons = every peak shifts to higher energy
- Identify an element from its full PES spectrum by matching peak count and height ratios to an electron configuration
- Predict the number of peaks and their height ratios for any element in Periods 1–4
- Explain the classic AP reasoning questions: why Ne's 1s peak sits at far higher energy than Li's, and why a 2p peak sits at lower binding energy than 2s in the same atom
- Verify a spectrum with the sanity check: sum of peak heights = number of electrons = atomic number (for a neutral atom)
- Argue how PES provides the experimental *evidence* for the shell/subshell model of the atom

---

## Prerequisites

- [Electron Configuration](/chemistry/0303-electron-configuration) — PES spectra are electron configurations drawn as data; you must be fluent in $1s^2 2s^2 2p^6\ldots$ before decoding them
- [Mass Spectrometry](/chemistry/0301-mass-spectrometry) — your first "read the peaks" instrument; the spectrum-reading reflexes (peak position = a property, peak height = how many) transfer directly

---

## The Core Concept

### Intuition First

Back to moving day. Let's make the map between the house and the atom precise, because it's structural, not decorative:

| Moving day | The atom |
|---|---|
| The house | One atom of an element |
| A storage spot (porch, upstairs, basement safe) | A **subshell** (1s, 2s, 2p, 3s, ...) |
| Deeper/harder-to-reach spot | Subshell **closer to the nucleus** |
| Effort to haul one box out | **Binding energy** to remove one electron |
| Number of boxes in a spot | Number of **electrons** in that subshell |
| My effort log, plotted | The **PES spectrum** |
| One clump in the plot | One **peak** |
| Clump height | Peak height = electron count |
| Stranger reconstructs the house from the plot | You reconstruct the electron configuration from the spectrum |

Two features of the house map onto everything that matters:

1. **Depth sets effort.** The basement safe (1s, hugging the nucleus) costs the most per box; the porch (the outermost subshell) costs the least. In Coulomb's-law terms: the closer an electron sits to the positive nucleus, the stronger the attraction, the more energy it takes to rip it out.
2. **Each spot holds a specific number of boxes.** The clump heights are a census: 2 boxes in the safe, 2 upstairs, 6 in the closet... read the heights and you've counted every electron.

And one upgrade the analogy needs: imagine comparing two houses with the *same floor plan* but one has a much stronger magnet in the basement pulling on every box. Every single haul gets harder. That's what adding protons does — more positive charge in the nucleus pulls **all** subshells in tighter, so **every peak shifts to higher binding energy**, even peaks for the same-named subshell. Neon's 1s electrons are vastly harder to remove than lithium's 1s electrons, because neon's nucleus has 10 protons pulling versus lithium's 3.

### What PES Actually Does

Photoelectron spectroscopy is beautifully brutal:

1. Shine **high-energy light** (X-ray or extreme UV photons) on a gas-phase sample of atoms.
2. Each absorbed photon can knock **one electron** clean out of an atom — any electron, from the deepest 1s core electron to the loosest valence electron.
3. A detector measures each ejected electron's **kinetic energy**. Since we know the photon's energy, subtraction tells us how much energy was *spent* freeing the electron:

$$E_{\text{binding}} = E_{\text{photon}} - KE_{\text{electron}}$$

That spent energy is the electron's **binding energy** (for AP purposes, the ionization energy of that specific electron). Do this for millions of atoms and you sample every subshell, building the full spectrum.

**One-line contrast with mass spec:** mass spectrometry sorts whole *atoms* by mass to reveal isotopes; PES reaches *inside* one element's atoms to reveal where the electrons live.

### Reading a PES Spectrum

A PES spectrum has:

- **x-axis: binding energy**, usually in MJ/mol (megajoules per mole of electrons).
- **y-axis: relative number of electrons** (peak height).
- **One peak per subshell.** Electrons in the same subshell have the same binding energy, so they pile into one peak.

> **THE #1 TRAP — the x-axis runs backwards.** On AP diagrams, binding energy conventionally **decreases from left to right**. The leftmost peak is the *hardest*-to-remove electrons (1s, the basement safe); the rightmost peak is the *easiest* (valence, the porch). Students who assume "right = bigger" read the entire spectrum upside down. Before you touch any PES question, look at the axis labels and find which end is high energy. Always.

Here's carbon ($\ce{C}$, $Z = 6$, configuration $1s^2 2s^2 2p^2$) as a table — three subshells, so three peaks:

| Peak (left → right on an AP diagram) | Binding energy (MJ/mol) | Relative height | Subshell |
|---|---|---|---|
| 1st | 28.6 | 2 | $1s$ |
| 2nd | 1.72 | 2 | $2s$ |
| 3rd | 1.09 | 2 | $2p$ |

Height pattern 2 : 2 : 2, heights sum to 6 = carbon's atomic number. The spectrum *is* the configuration.

### Where Peaks Sit: Coulomb's Law Does All the Work

Every peak-position question on the AP exam is answered by one relationship:

$$F \propto \frac{q_1 q_2}{r^2}$$

The attraction between an electron and the nucleus grows with nuclear charge ($q$) and shrinks with distance ($r$). Two consequences:

1. **Within one atom:** subshells closer to the nucleus (smaller $n$, and within a shell, $s$ before $p$) have higher binding energy. Order for any atom: $1s \gg 2s > 2p \gg 3s > 3p \ldots$ The gaps *between shells* are huge; the gaps *within a shell* (like $2s$ vs $2p$) are small. In house terms: the basement is far below the upstairs, but the two upstairs closets are just steps apart.
2. **Across elements:** more protons pulls *everything* tighter. Compare the $1s$ peak across Period 2 — it marches steadily to higher energy:

| Element | $Z$ | $1s$ binding energy (MJ/mol) |
|---|---|---|
| $\ce{Li}$ | 3 | 6.26 |
| $\ce{C}$ | 6 | 28.6 |
| $\ce{N}$ | 7 | 39.6 |
| $\ce{Ne}$ | 10 | 84.0 |

Same subshell, same distance-ish from the nucleus — but Ne's 10-proton "magnet" makes its 1s electrons roughly 13 times harder to remove than Li's.

### Why Is 2p Easier to Remove Than 2s?

Same shell, so why does the $2p$ peak always sit at *lower* binding energy than $2s$? Two AP-legal reasons:

- $2p$ electrons are, on average, **slightly farther** from the nucleus than $2s$ electrons ($r$ is bigger, attraction weaker).
- $2p$ electrons are **shielded** by the $2s$ electrons (and the core), so they feel a slightly smaller effective nuclear charge.

House version: the upstairs bedroom and the upstairs hallway closet are on the same floor, but the closet sits right at the top of the stairs — hauling a closet box costs just a *little* less than hauling a bedroom box. Same floor, small but real difference, and PES is sensitive enough to resolve it. That resolution is exactly why we believe subshells exist.

### The Decoding Recipe

Given an unknown spectrum:

1. **Orient the axis.** Find the high-binding-energy end (usually the left).
2. **Count the peaks** = number of occupied subshells.
3. **Read the heights** left to right (highest energy first) = electrons per subshell, in order $1s, 2s, 2p, 3s, \ldots$
4. **Sum the heights.** For a neutral atom, total electrons = atomic number = the element.
5. **Sanity-check** the pattern against the aufbau order (heights can't exceed 2 for $s$, 6 for $p$, 10 for $d$).

Heights are **relative** — a spectrum showing heights 1 : 1 : 3 is the same as 2 : 2 : 6. Only the *ratios* matter.

### PES Is the Evidence, Not Just an Application

Remember the models-and-evidence storyline from [the history article](/chemistry/0002-history-of-chemistry)? Every atomic model earned its keep by explaining an experiment. PES is the experiment that cements the quantum shell model:

- **If electrons were smeared randomly** (plum pudding), binding energies would form a continuous blur — no peaks.
- **If atoms had only shells** (Bohr), nitrogen would show **2** peaks (heights 2 : 5 — one clump per floor).
- **Reality:** nitrogen shows **3** peaks (2 : 2 : 3). The second shell resolves into two clumps — $2s$ and $2p$. Discrete peaks prove discrete energy levels; peaks *within* a shell prove subshells.

The stranger reading my effort log doesn't just learn the house has rooms — the log proves rooms exist at all.

---

## Worked Examples

### Example 1: Decoding a Full Spectrum

**Problem:** A neutral atom's PES spectrum shows three peaks:

| Binding energy (MJ/mol) | Relative height |
|---|---|
| 28.6 | 2 |
| 1.72 | 2 |
| 1.09 | 2 |

Identify the element.

**Solution:**

**Step 1:** Three peaks → three occupied subshells: $1s$, $2s$, $2p$ in order of decreasing energy.

**Step 2:** Heights give the configuration: $1s^2\,2s^2\,2p^2$.

**Step 3:** Total electrons $= 2 + 2 + 2 = 6$. Neutral atom → $Z = 6$.

**Answer: Carbon** ($1s^2 2s^2 2p^2$).

### Example 2: Predicting a Spectrum from the Element

**Problem:** Predict the PES spectrum of phosphorus ($Z = 15$): number of peaks, height ratios, and the order of peaks from highest to lowest binding energy.

**Solution:**

**Step 1:** Configuration: $\ce{P}$ is $1s^2\,2s^2\,2p^6\,3s^2\,3p^3$.

**Step 2:** Five occupied subshells → **5 peaks**.

**Step 3:** Order by distance from nucleus (deepest = highest energy): $1s$, then $2s$, then $2p$, then $3s$, then $3p$.

**Step 4:** Heights follow the superscripts.

**Answer: 5 peaks with height ratio 2 : 2 : 6 : 2 : 3** (from highest to lowest binding energy). Check: $2+2+6+2+3 = 15$ ✓

### Example 3: Assigning Peaks to Subshells

**Problem:** Sodium's PES spectrum shows peaks at 104, 6.84, 3.67, and 0.50 MJ/mol. Assign each peak to a subshell and give its expected height.

**Solution:**

**Step 1:** $\ce{Na}$ ($Z = 11$): $1s^2\,2s^2\,2p^6\,3s^1$. Four subshells, four peaks ✓

**Step 2:** Highest binding energy = deepest subshell:
- 104 MJ/mol → $1s$ (height 2)
- 6.84 MJ/mol → $2s$ (height 2)
- 3.67 MJ/mol → $2p$ (height 6)
- 0.50 MJ/mol → $3s$ (height 1)

**Step 3:** Notice the structure: a giant gap between shells (104 vs ~7 vs ~0.5), a small gap within shell 2 (6.84 vs 3.67). Basement vs upstairs vs porch.

**Answer:** 104 → $1s$ (2), 6.84 → $2s$ (2), 3.67 → $2p$ (6), 0.50 → $3s$ (1). That lone, easy-to-remove $3s$ electron is why sodium is so eager to form $\ce{Na+}$.

### Example 4: Identify from Heights Alone

**Problem:** A neutral element's spectrum has four peaks with relative heights 2 : 2 : 6 : 2 (highest binding energy to lowest). What is the element?

**Solution:**

**Step 1:** Map heights to subshells in aufbau order: $1s^2\,2s^2\,2p^6\,3s^2$.

**Step 2:** Total electrons $= 2+2+6+2 = 12 \Rightarrow Z = 12$.

**Answer: Magnesium.**

### Example 5: Why Is Ne's 1s Peak So Far Left of Li's?

**Problem:** Lithium's $1s$ peak sits at 6.26 MJ/mol; neon's $1s$ peak sits at 84.0 MJ/mol. Both are $1s$ electrons. Explain the difference in one or two sentences, AP-style.

**Solution:**

**Step 1:** Identify what's the same: both electrons are in the $1s$ subshell, closest to the nucleus, with no inner electrons shielding them.

**Step 2:** Identify what differs: $\ce{Ne}$ has 10 protons; $\ce{Li}$ has 3. By Coulomb's law, a larger nuclear charge exerts a stronger attractive force on an electron at a similar distance.

**Answer:** Ne's nucleus has 10 protons versus Li's 3, so Ne's $1s$ electrons experience a much greater nuclear attraction and require far more energy to remove. (Stronger magnet in the basement — same safe, harder haul.)

### Example 6: Why Does 2p Sit Right of 2s?

**Problem:** In nitrogen's spectrum, the $2s$ peak is at 2.45 MJ/mol and the $2p$ peak at 1.40 MJ/mol. Explain why $2p$ has the lower binding energy.

**Solution:**

**Step 1:** Both are in shell $n = 2$, so the difference is *within-shell*, and it's small compared to the $1s$–$2s$ gap (39.6 vs 2.45).

**Step 2:** $2p$ electrons are on average slightly farther from the nucleus and are shielded by the $2s$ electrons, so they feel a smaller effective nuclear charge.

**Answer:** The $2p$ electrons experience a weaker net attraction (greater average distance + more shielding), so less energy is needed to eject them — the $2p$ peak sits at lower binding energy than $2s$.

### Example 7: Comparing Two Elements' Spectra

**Problem:** Two spectra, A and B:

| | Peak heights (high → low energy) | Lowest-energy peak position |
|---|---|---|
| Spectrum A | 2 : 2 : 6 : 1 | 0.50 MJ/mol |
| Spectrum B | 2 : 2 : 6 : 2 | 0.74 MJ/mol |

Identify both elements and explain why B's peaks all sit at higher energies than A's corresponding peaks.

**Solution:**

**Step 1:** A: $2+2+6+1 = 11 \Rightarrow$ **sodium**. B: $2+2+6+2 = 12 \Rightarrow$ **magnesium**.

**Step 2:** Mg has one more proton than Na. That extra positive charge pulls on *every* subshell — $1s$ through $3s$ — so each of Mg's peaks appears at a higher binding energy than the same-named peak in Na.

**Answer:** A = Na, B = Mg; Mg's greater nuclear charge (12 vs 11 protons) increases the attraction on all electrons, shifting every peak to higher binding energy.

### Example 8: Relative Heights Are Relative

**Problem:** A spectrum shows three peaks with heights 1 : 1 : 3 (highest to lowest binding energy). The atom is neutral. Identify it.

**Solution:**

**Step 1:** Heights are relative, so 1 : 1 : 3 could be the pattern $2 : 2 : 6$ scaled by ½. Filled subshells cap the options: an $s$ peak can't hold more than 2, a $p$ peak no more than 6.

**Step 2:** Try 1 : 1 : 3 literally: $1s^1 2s^1 2p^3$? Impossible — a $1s^1$ atom wouldn't have filled higher subshells (violates aufbau for a ground-state neutral atom).

**Step 3:** Scale to $2 : 2 : 6 \Rightarrow 1s^2 2s^2 2p^6$, total 10 electrons.

**Answer: Neon.** Whenever raw heights don't build a legal ground-state configuration, scale them.

### Example 9: The Reversed-Axis Trap

**Problem:** An AP-style spectrum of boron is drawn with binding energy decreasing left to right. Three peaks appear at (left to right) 19.3, 1.36, and 0.80 MJ/mol with heights 2, 2, 1. A student says, "The tall peak on the left is the valence electron because it's first." Fix the reasoning.

**Solution:**

**Step 1:** On this axis, *left = highest binding energy* = hardest to remove = closest to the nucleus. The 19.3 MJ/mol peak is $1s$ — core, not valence.

**Step 2:** The valence electron is the *easiest* to remove: the rightmost peak, 0.80 MJ/mol, height 1 → $2p^1$.

**Answer:** Leftmost = $1s$ core electrons (highest binding energy). The valence $2p^1$ electron is the rightmost, smallest peak at 0.80 MJ/mol. Boron: $1s^2 2s^2 2p^1$ ✓

### Example 10: Neutral Atom or Ion?

**Problem:** A spectrum shows exactly the neon height pattern, 2 : 2 : 6, but every peak sits at noticeably *higher* binding energy than neon's known peaks (e.g., the $2p$ peak at 3.67 MJ/mol instead of Ne's 2.08). If the sample might be an ion, what is a likely identity?

**Solution:**

**Step 1:** Height pattern 2 : 2 : 6 means 10 electrons in $1s^2 2s^2 2p^6$. If neutral → Ne. But positions don't match Ne.

**Step 2:** An ion with 10 electrons and *more* protons — like $\ce{Na+}$ (11 p⁺) or $\ce{Mg^2+}$ (12 p⁺) — has the same configuration but a stronger pull on it, shifting all peaks to higher energy. (In fact, 3.67 MJ/mol matches sodium's $2p$.)

**Answer:** Likely $\ce{Na+}$ — same electron count as Ne, but one extra proton pulls the identical configuration harder, shifting every peak to higher binding energy. Peak *pattern* gives the electron count; peak *positions* reveal the nuclear charge. (AP note: exam spectra are almost always neutral atoms, so "sum of heights = atomic number" is your default.)

### Example 11: A Bigger Atom — Counting Peaks for Calcium

**Problem:** How many peaks does calcium's PES spectrum show, and what are the height ratios?

**Solution:**

**Step 1:** $\ce{Ca}$ ($Z = 20$): $1s^2\,2s^2\,2p^6\,3s^2\,3p^6\,4s^2$.

**Step 2:** Six occupied subshells → 6 peaks, ordered $1s, 2s, 2p, 3s, 3p, 4s$ from highest binding energy down.

**Step 3:** Heights: 2, 2, 6, 2, 6, 2. Check: sums to 20 ✓

**Answer: 6 peaks, ratio 2 : 2 : 6 : 2 : 6 : 2.** Note the fingerprint: two same-height $s$–$p$ "floors" (2 : 6 twice) plus the basement and the porch pair.

### Example 12: PES as Evidence for Subshells

**Problem:** If the Bohr shell-only model were correct, how many peaks would nitrogen's PES spectrum show, and with what heights? Compare with the actual spectrum and state what the difference proves.

**Solution:**

**Step 1:** Bohr model: electrons live in shells only. Nitrogen ($Z=7$) would have shell 1 (2 electrons) and shell 2 (5 electrons) → **2 peaks**, heights 2 : 5.

**Step 2:** Actual spectrum: **3 peaks** — 39.6 (height 2), 2.45 (height 2), 1.40 (height 3) MJ/mol.

**Step 3:** The second shell's electrons split into two distinct binding energies (2.45 and 1.40) — close together compared to the $1s$ gap, but clearly resolved.

**Answer:** Bohr predicts 2 peaks (2 : 5); experiment shows 3 (2 : 2 : 3). The splitting of shell 2 into two nearby peaks is direct experimental evidence that shells contain **subshells** ($2s$ and $2p$) with slightly different energies.

---

## Common Mistakes

| The mistake | Why it happens | How to avoid it |
|---|---|---|
| Reading the x-axis left-to-right as increasing energy | Every other graph you've ever met increases rightward | AP PES axes conventionally **decrease** rightward — check the axis label first, every time |
| Thinking taller peak = more tightly bound | Confusing the two axes | Height = **how many** electrons; position = **how hard** to remove. The tall $2p^6$ peak is often among the *easiest* |
| Peak = shell instead of peak = subshell | Bohr-model habit | Count subshells: nitrogen has 3 peaks, not 2 |
| Forgetting heights are relative | Expecting literal electron counts on the y-axis | Work with **ratios** (1 : 1 : 3 = 2 : 2 : 6); scale until you get a legal configuration |
| Not checking the total | Pattern-matching the first plausible element | Sum of heights must equal $Z$ for a neutral atom — a 10-second check that catches most errors |
| Mixing up PES with mass spectrometry | Both are "peaks on a graph" instruments | Mass spec: x-axis = mass, sorts **atoms** (isotopes). PES: x-axis = binding energy, sorts **electrons** (subshells) |
| Saying Ne's 1s is higher "because Ne has more electrons" | Right answer, wrong reason | The cause is **protons** (nuclear charge), not electron count — FRQ graders want Coulomb's law language |
| Explaining $2s > 2p$ with "2p has more electrons" | Confusing occupancy with attraction | Use distance + shielding: $2p$ is slightly farther on average and shielded by $2s$ |

---

## AP Exam Tips

- **Where it appears:** PES is Topic 1.6 and shows up in both multiple choice and FRQs — usually "identify the element," "assign the peaks," or "explain the position of peak X" (a Coulomb's law justification).
- **Pattern-match with height ratios.** The fastest MC move: read heights high-energy-first (2 : 2 : 5 → $1s^2 2s^2 2p^5$ → fluorine), then confirm with the sum.
- **Always run the sum check:** total relative height = number of electrons = atomic number for a neutral atom. It's free points insurance.
- **The reversed axis is the graders' favorite trap.** Before answering anything, mark which end of the x-axis is high binding energy and label the leftmost peak $1s$.
- **Explanation questions demand Coulomb's law vocabulary:** "greater nuclear charge," "smaller distance from the nucleus," "greater shielding by inner electrons." Answers like "it's bigger" or "it has more electrons" score zero.
- **Compare like with like.** When contrasting two elements, compare the *same subshell* (1s vs 1s), and attribute shifts to the difference in protons.
- **Units:** binding energies are typically in MJ/mol. You won't compute $E = h\nu$ arithmetic here — PES questions are about *reading and reasoning*, not calculators.
- **Know the shape of a shell gap:** peaks within a shell sit close together; the jump to the next inner shell is enormous. That visual instantly separates $2p$ from $3s$.

---

## Practice Problems

### Problem 1
Sulfur is bombarded with X-rays in a PES experiment. How many peaks appear in its spectrum, and what are the relative heights (highest binding energy first)?

<details>
<summary><strong>Solution</strong></summary>

$\ce{S}$ ($Z = 16$): $1s^2\,2s^2\,2p^6\,3s^2\,3p^4$.

Five occupied subshells → 5 peaks: $1s, 2s, 2p, 3s, 3p$.

Heights follow the superscripts: 2, 2, 6, 2, 4. Check: $2+2+6+2+4 = 16$ ✓

**Answer: 5 peaks, heights 2 : 2 : 6 : 2 : 4.**

</details>

### Problem 2
A neutral atom's spectrum shows exactly two peaks with heights in ratio 2 : 1, the taller at much higher binding energy. Identify the element.

<details>
<summary><strong>Solution</strong></summary>

Two peaks → two subshells. Heights 2 : 1 → $1s^2\,2s^1$.

Total electrons $= 3 \Rightarrow Z = 3$.

**Answer: Lithium.** (The height-2 peak is the deep $1s$ pair; the lone easy $2s$ electron is the small peak — and the reason Li forms $\ce{Li+}$.)

</details>

### Problem 3
A spectrum shows peaks at 39.6, 2.45, and 1.40 MJ/mol with relative heights 2, 2, 3. Identify the element and write its electron configuration.

<details>
<summary><strong>Solution</strong></summary>

Three peaks: $1s$ (39.6), $2s$ (2.45), $2p$ (1.40).

Configuration from heights: $1s^2\,2s^2\,2p^3$. Total $= 7$.

**Answer: Nitrogen, $1s^2 2s^2 2p^3$.**

</details>

### Problem 4
In potassium's PES spectrum, which subshell does the peak at the *lowest* binding energy correspond to, and what is its relative height?

<details>
<summary><strong>Solution</strong></summary>

$\ce{K}$ ($Z = 19$): $1s^2\,2s^2\,2p^6\,3s^2\,3p^6\,4s^1$.

Lowest binding energy = outermost subshell = $4s$, holding 1 electron.

**Answer: the $4s$ peak, relative height 1.** (That's the porch box — and why potassium ionizes so easily.)

</details>

### Problem 5
Boron's $1s$ peak appears at 19.3 MJ/mol; fluorine's $1s$ peak appears at 67.2 MJ/mol. Explain the difference using Coulomb's law.

<details>
<summary><strong>Solution</strong></summary>

Both peaks are $1s$ electrons — same subshell, similar distance, no inner shielding.

Fluorine's nucleus has 9 protons; boron's has 5. The greater nuclear charge exerts a stronger attractive force on the $1s$ electrons, so more energy is required to remove them.

**Answer: F's larger nuclear charge (9 p⁺ vs 5 p⁺) binds its $1s$ electrons more strongly, shifting the peak to higher binding energy.**

</details>

### Problem 6
A neutral atom's spectrum shows three peaks with heights in the ratio 1 : 1 : 3. Identify the element. (Careful — think about what heights mean.)

<details>
<summary><strong>Solution</strong></summary>

Heights are *relative*. Literal $1s^1 2s^1 2p^3$ is not a legal ground state (aufbau violation).

Scale by 2: $2 : 2 : 6 \Rightarrow 1s^2\,2s^2\,2p^6$, total 10 electrons.

**Answer: Neon.**

</details>

### Problem 7
A neutral element's spectrum has six peaks, heights 2 : 2 : 6 : 2 : 6 : 1 from highest binding energy to lowest. Identify the element and state which peak represents its valence electron(s).

<details>
<summary><strong>Solution</strong></summary>

Configuration: $1s^2\,2s^2\,2p^6\,3s^2\,3p^6\,4s^1$. Total $= 19 \Rightarrow Z = 19$.

**Answer: Potassium; the height-1 peak at the lowest binding energy is the $4s^1$ valence electron.**

</details>

### Problem 8
In any atom with both subshells occupied, the $2s$ peak sits at higher binding energy than the $2p$ peak. Give the two-part AP-approved explanation.

<details>
<summary><strong>Solution</strong></summary>

1. **Distance:** $2p$ electrons are on average slightly farther from the nucleus than $2s$ electrons, weakening the Coulombic attraction.
2. **Shielding:** $2p$ electrons are shielded by the $2s$ electrons, reducing the effective nuclear charge they experience.

**Answer: $2p$ electrons feel a weaker net attraction (greater average distance + more shielding), so they take less energy to remove — lower binding energy than $2s$.**

</details>

### Problem 9
Hydrogen and helium each produce a one-peak PES spectrum. Describe two differences between the spectra.

<details>
<summary><strong>Solution</strong></summary>

$\ce{H}$: $1s^1$ — one peak, height 1, at 1.31 MJ/mol. $\ce{He}$: $1s^2$ — one peak, height 2, at 2.37 MJ/mol.

Differences:
1. **Position:** He's peak sits at higher binding energy (2 protons pull the $1s$ electrons harder than H's 1 proton).
2. **Height:** He's peak is twice as tall (2 electrons vs 1).

**Answer: He's single peak is both taller (height 2 vs 1) and at higher binding energy (greater nuclear charge).**

</details>

### Problem 10
For aluminum: how many peaks appear, and which peak is the tallest?

<details>
<summary><strong>Solution</strong></summary>

$\ce{Al}$ ($Z = 13$): $1s^2\,2s^2\,2p^6\,3s^2\,3p^1$ → **5 peaks**, heights 2 : 2 : 6 : 2 : 1.

The tallest is the height-6 peak: $2p^6$.

**Answer: 5 peaks; the $2p$ peak (6 electrons) is tallest.** Note it's tall but *not* the hardest to remove — height and position are independent.

</details>

### Problem 11
Describe the two changes you'd see going from neon's spectrum to sodium's spectrum.

<details>
<summary><strong>Solution</strong></summary>

$\ce{Ne}$: 3 peaks, 2 : 2 : 6. $\ce{Na}$: 4 peaks, 2 : 2 : 6 : 1.

1. **A new small peak appears** at very low binding energy — the $3s^1$ electron (a new, farther "floor" opens with one box in it).
2. **All three original peaks shift to higher binding energy** — sodium's 11th proton pulls every subshell in tighter (Ne $1s$: 84.0 → Na $1s$: 104 MJ/mol).

**Answer: one added low-energy peak of height 1 ($3s$), and every shared peak shifted to higher binding energy because of the extra proton.**

</details>

### Problem 12
Moving across Period 2 from Li to Ne, the $1s$ peak marches steadily to higher binding energy even though the $1s$ electrons aren't the valence electrons. Explain why in one sentence.

<details>
<summary><strong>Solution</strong></summary>

Each step across the period adds a proton, and nuclear charge acts on **all** electrons, not just valence ones — so the attraction on the $1s$ pair grows steadily.

**Answer: increasing nuclear charge (more protons) strengthens the Coulombic attraction on every subshell, including the core $1s$, shifting its peak to higher binding energy across the period.**

</details>

### Problem 13
An unknown neutral element shows 4 peaks with relative heights 2 : 2 : 6 : 2. Identify the element and state the total number of electrons.

<details>
<summary><strong>Solution</strong></summary>

Heights map to $1s^2\,2s^2\,2p^6\,3s^2$.

Total $= 2 + 2 + 6 + 2 = 12$ electrons $\Rightarrow Z = 12$.

**Answer: Magnesium, 12 electrons.**

</details>

### Problem 14
A three-peak spectrum has heights 2 : 2 : 5. A classmate says, "Five electrons in the last peak — that's boron, group 15, something like that." Straighten this out: identify the element correctly.

<details>
<summary><strong>Solution</strong></summary>

Heights high-energy-first: $1s^2\,2s^2\,2p^5$. Total $= 2+2+5 = 9 \Rightarrow Z = 9$.

Boron is $Z=5$ ($1s^2 2s^2 2p^1$, heights 2 : 2 : 1) — the classmate matched one number instead of summing all of them.

**Answer: Fluorine ($1s^2 2s^2 2p^5$).** Always decode *all* the heights and sum them.

</details>

### Problem 15
Your friend asks why chemists believe in subshells at all — "you can't see them." Using beryllium (2 peaks, 2 : 2) and boron (3 peaks, 2 : 2 : 1), build the evidence argument.

<details>
<summary><strong>Solution</strong></summary>

- Beryllium ($1s^2 2s^2$) shows 2 peaks: two distinct binding energies → two distinct energy levels (shells 1 and 2).
- Boron adds just **one** electron, yet a **whole new peak** appears at 0.80 MJ/mol, clearly separate from the $2s$ peak at 1.36 — the new electron occupies a *different* energy level within the same shell.
- If shell 2 were a single level (Bohr), boron's outer three electrons would form one peak of height 3. They don't — they split 2 : 1.

**Answer: the discrete peaks prove quantized energy levels, and the small-but-real splitting of shell 2 into $2s$ and $2p$ peaks is direct experimental evidence for subshells.** PES turns the shell model from a nice idea into measured data.

</details>

---

## Quick Reference

| Item | The rule |
|---|---|
| What PES measures | Binding (ionization) energy of **every** electron in an atom |
| x-axis | Binding energy, **decreasing left → right** on AP diagrams (check every time!) |
| y-axis | *Relative* number of electrons |
| One peak = | One occupied **subshell** |
| Peak height | Electrons in that subshell (ratios only: 1 : 1 : 3 ≡ 2 : 2 : 6) |
| Peak position (within an atom) | Closer to nucleus → higher binding energy: $1s \gg 2s > 2p \gg 3s > 3p \ldots$ |
| Peak position (across elements) | More protons → **all** peaks shift to higher binding energy |
| Sanity check | Sum of heights = electrons = $Z$ (neutral atom) |
| $2s$ vs $2p$ | $2p$ lower: slightly farther on average + shielded by $2s$ |
| Shell gaps | Huge *between* shells, small *within* a shell |
| vs mass spec | Mass spec sorts atoms by mass (isotopes); PES probes electrons (subshells) |
| Big picture | PES = experimental evidence for the shell/subshell model |

| Element | Peaks | Heights (high → low BE) |
|---|---|---|
| $\ce{H}$ | 1 | 1 |
| $\ce{He}$ | 1 | 2 |
| $\ce{Li}$ | 2 | 2 : 1 |
| $\ce{C}$ | 3 | 2 : 2 : 2 |
| $\ce{N}$ | 3 | 2 : 2 : 3 |
| $\ce{O}$ | 3 | 2 : 2 : 4 |
| $\ce{F}$ | 3 | 2 : 2 : 5 |
| $\ce{Ne}$ | 3 | 2 : 2 : 6 |
| $\ce{Na}$ | 4 | 2 : 2 : 6 : 1 |
| $\ce{Mg}$ | 4 | 2 : 2 : 6 : 2 |
| $\ce{Al}$ | 5 | 2 : 2 : 6 : 2 : 1 |
| $\ce{P}$ | 5 | 2 : 2 : 6 : 2 : 3 |
| $\ce{S}$ | 5 | 2 : 2 : 6 : 2 : 4 |
| $\ce{Ar}$ | 5 | 2 : 2 : 6 : 2 : 6 |
| $\ce{K}$ | 6 | 2 : 2 : 6 : 2 : 6 : 1 |
| $\ce{Ca}$ | 6 | 2 : 2 : 6 : 2 : 6 : 2 |

---

<div align="center">

[← Electron Configuration](/chemistry/0303-electron-configuration) | [Periodic Trends →](/chemistry/0305-periodic-trends)

</div>
