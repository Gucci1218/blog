# Ions and Ionic Compounds
<p class="article-date">July 4, 2026</p>

*Our fridge door is a physics experiment nobody asked for. The flimsy souvenir magnet from a Vegas gift shop holds exactly one photo, and it slides to the floor if you close the door too hard. The heavy-duty black magnet Dad brought home grips an entire stack of pizza menus and does not care how hard you slam anything. Two things decide a magnet's grip: how strong the magnet is, and how close it sits to the steel — slip a single sticky note between the strong magnet and the door, and even that one starts to slide. Here's the wild part: those same two dials — strength and distance — are the entire story of ionic compounds. Ion charge is the magnet's strength, ionic radius is the sticky-note gap, and "lattice energy" is how hard it is to strip everything off the fridge at once. That one idea predicts real, measurable numbers: it's why $\ce{MgO}$ holds itself together until 2852°C while $\ce{NaCl}$ gives up at 801°C. This article is the Unit 1 capstone — the place where electron configurations, periodic trends, and bonding all click together into one Coulomb's-law argument that AP graders reward over and over.*

---

## What You'll Learn

- Count valence electrons for any main-group element straight from its electron configuration
- Draw Lewis dot symbols for atoms and ions using dots and brackets
- Explain the octet "rule" the AP way — as an energy statement about filled shells, never as what an atom "wants"
- Write electron configurations for ions, including transition-metal cations (which lose $4s$ electrons first)
- Identify isoelectronic species and rank their radii using proton count
- Build ionic formulas from predicted charges, and say "formula unit," not "molecule"
- Define lattice energy and rank lattice energies using $E \propto \dfrac{|q_1 q_2|}{r}$ (charge first, then radius)
- Connect lattice energy to melting points and hardness with real numbers
- Explain brittleness and conductivity of ionic solids in FRQ-ready language

---

## Prerequisites

- [Periodic Trends](/chemistry/0305-periodic-trends) — atomic and ionic radius, effective nuclear charge, and the "Coulomb, not wants" justification style all carry over directly
- [Electron Configuration](/chemistry/0303-electron-configuration) — you can't write an ion's configuration until you can write the atom's
- [Ionic vs Covalent](/chemistry/0203-ionic-vs-covalent) — transfer vs. share, lattices, and formula units; this article upgrades that picture with energy

---

## The Core Concept

### Intuition First

Back to the fridge, because the analogy has to earn its keep.

**Magnet strength = ion charge.** The souvenir magnet is a $1+/1-$ pair like $\ce{Na+}$ and $\ce{Cl-}$: real attraction, holds one photo, nothing heroic. The heavy-duty magnet is a $2+/2-$ pair like $\ce{Mg^2+}$ and $\ce{O^2-}$. Coulomb's law multiplies the charges together, so doubling *both* charges makes the grip $2 \times 2 = 4$ times stronger — before we even talk about distance.

**The sticky-note gap = ionic radius.** A magnet grips hardest when it touches the steel directly. Slide a sticky note in between and the grip weakens fast, because magnetic (and electrostatic) attraction dies off with distance. Small ions like $\ce{Li+}$ and $\ce{F-}$ snuggle right up against each other — magnet flush on the door. Big puffy ions like $\ce{K+}$ and $\ce{Br-}$ hold each other at arm's length — there's a permanent sticky note built into the pair. Same charges, weaker grip.

**Lattice energy = stripping the whole fridge.** One magnet is a bond; the fully loaded fridge door is the crystal lattice — billions of magnets, all gripping at once. Lattice energy asks: how much energy does it take to pull *every* magnet off the door and leave them floating in the air, far apart? For the souvenir-magnet fridge ($\ce{NaCl}$), that costs about $786\ \text{kJ/mol}$. For the heavy-duty fridge ($\ce{MgO}$), about $3795\ \text{kJ/mol}$ — nearly five times more, exactly what "4× from charge, plus a bonus from smaller ions" predicts.

**Flipping a magnet = brittleness.** Push a row of fridge magnets sideways so a magnet's north pole lines up with another north pole, and they *shove each other off the door*. Ionic crystals do the same: shift one layer of ions by one position, like charges suddenly face each other, and the crystal doesn't bend — it shatters.

Keep those four mappings. Every ranking, every melting point, every "justify your answer" in this article is one of them in disguise.

### Step 1: Valence Electrons — Read Them Off the Configuration

**Valence electrons** are the electrons in the outermost shell (highest principal quantum number $n$). They're the only electrons far enough out to be transferred or shared — the business end of the atom.

For main-group elements, the configuration hands you the count:

| Element | Configuration | Outermost shell | Valence e⁻ |
|---|---|---|---|
| $\ce{Na}$ | $1s^2\,2s^2\,2p^6\,3s^1$ | $3s^1$ | 1 |
| $\ce{Mg}$ | $[\text{Ne}]\,3s^2$ | $3s^2$ | 2 |
| $\ce{Al}$ | $[\text{Ne}]\,3s^2\,3p^1$ | $3s^2 3p^1$ | 3 |
| $\ce{P}$ | $[\text{Ne}]\,3s^2\,3p^3$ | $3s^2 3p^3$ | 5 |
| $\ce{S}$ | $[\text{Ne}]\,3s^2\,3p^4$ | $3s^2 3p^4$ | 6 |
| $\ce{Cl}$ | $[\text{Ne}]\,3s^2\,3p^5$ | $3s^2 3p^5$ | 7 |
| $\ce{Ar}$ | $[\text{Ne}]\,3s^2\,3p^6$ | $3s^2 3p^6$ | 8 (full) |

Shortcut: for main groups, **valence electrons = the group's ones digit** (Group 1 → 1, Group 2 → 2, Group 13 → 3, ... Group 17 → 7, Group 18 → 8). The configuration is the *proof*; the group number is the *shortcut*. AP explanations should lean on the configuration.

### Step 2: Lewis Dot Symbols

A **Lewis dot symbol** is the element's symbol with one dot per valence electron. Place dots on the four sides, one per side before pairing:

```
                                     .            .           ..           ..           ..
  Na .       . Mg .      . Al .    . Si .       . P :       . S :        : Cl :       : Ar :
                            .        .            .           .            .            ..
```

Ions get dots adjusted and the charge shown. Cations usually lose *all* their dots; anions fill up to eight and wear brackets:

```
                        ..    -                ..    2-
  Na+        Mg 2+    [ : Cl : ]             [ : O : ]
                        ..                     ..
```

You'll draw these constantly in Unit 2 (Lewis structures of molecules). For now they're a bookkeeping tool: dots in = electrons available to lose, gaps = room to gain.

### Step 3: Why the Octet Works (Say "Energy," Never "Wants")

Here's the AP-critical part. The octet rule *observation*: main-group atoms tend to gain or lose electrons until they have the configuration of the nearest noble gas — a filled $ns^2 np^6$ shell.

The *reason* is energy, and you must phrase it that way:

- A filled shell is a **low-energy, extra-stable arrangement**: every electron in it feels a strong pull from the nucleus, and the next available orbital is a whole shell farther out.
- Removing an electron *beyond* the filled shell means ripping out a **core electron** — one that sits much closer to the nucleus and feels a much larger effective nuclear charge. Coulomb's law says that costs enormous energy. (You saw this cliff in [Periodic Trends](/chemistry/0305-periodic-trends) as the giant jump in successive ionization energies.)
- Adding an electron *past* a filled shell means parking it in a new, distant shell where the attraction is weak — barely worth anything energetically.

So sodium forms $\ce{Na+}$ and stops. Not because it "wants to be like neon" — because removing electron #1 is cheap (a lone, well-shielded $3s$ electron) and removing electron #2 would gouge into the neon core, costing about nine times more energy. **Atoms don't want anything. Systems settle into low-energy arrangements.** Write the second sentence on the exam, never the first.

### Step 4: Making Ions — Configurations Before and After

**Cations (metals lose):**

$$\ce{Na} \;(1s^2\,2s^2\,2p^6\,3s^1) \;\longrightarrow\; \ce{Na+} \;(1s^2\,2s^2\,2p^6) + e^-$$

$\ce{Na+}$ is *isoelectronic* with neon — same electron count, filled shell.

$$\ce{Mg} \;([\text{Ne}]\,3s^2) \;\longrightarrow\; \ce{Mg^2+} \;(1s^2\,2s^2\,2p^6) + 2e^-$$

**Anions (nonmetals gain):**

$$\ce{O} \;(1s^2\,2s^2\,2p^4) + 2e^- \;\longrightarrow\; \ce{O^2-} \;(1s^2\,2s^2\,2p^6)$$

$$\ce{Cl} \;([\text{Ne}]\,3s^2\,3p^5) + e^- \;\longrightarrow\; \ce{Cl-} \;([\text{Ne}]\,3s^2\,3p^6)$$

**Predicting the charge from the address** (this ties straight back to the [Periodic Table Map](/chemistry/0202-periodic-table-map)):

| Group | Typical ion | Why (energy version) |
|---|---|---|
| 1 | $1+$ | one cheap outer electron to remove |
| 2 | $2+$ | two; the third would come from the core |
| 13 | $3+$ | three |
| 15 | $3-$ | three vacancies complete the $p$ subshell |
| 16 | $2-$ | two vacancies |
| 17 | $1-$ | one vacancy |
| 18 | none | shell already filled — lowest energy as-is |

### Step 5: Transition Metals — $4s$ Leaves First

Transition metals break the pattern in one famous way. When building the atom, $4s$ fills before $3d$. But **when the atom ionizes, the $4s$ electrons leave first**, because in the neutral atom the $4s$ orbital ends up *higher* in energy than $3d$ once $3d$ starts filling (echo from [Electron Configuration](/chemistry/0303-electron-configuration)).

$$\ce{Fe}: [\text{Ar}]\,3d^6\,4s^2 \;\longrightarrow\; \ce{Fe^2+}: [\text{Ar}]\,3d^6 \;\longrightarrow\; \ce{Fe^3+}: [\text{Ar}]\,3d^5$$

Note the classic trap: $\ce{Fe^2+}$ is **not** $[\text{Ar}]\,3d^4\,4s^2$. The $4s$ electrons go first, always. ($\ce{Fe^3+}$'s half-filled $3d^5$ is a symmetric, relatively low-energy arrangement — part of why iron(III) is so common.)

Transition metals also often form *more than one* stable cation ($\ce{Fe^2+}/\ce{Fe^3+}$, $\ce{Cu+}/\ce{Cu^2+}$), which is exactly why [Naming Compounds](/chemistry/0204-naming-compounds) makes you write Roman numerals.

### Step 6: Isoelectronic Species — Protons Decide the Size

Two species are **isoelectronic** if they have the same number of electrons. These six all have 10 electrons — the neon configuration:

$$\ce{N^3-}, \quad \ce{O^2-}, \quad \ce{F-}, \quad \ce{Na+}, \quad \ce{Mg^2+}, \quad \ce{Al^3+}$$

Same electrons, same shells, same electron–electron repulsion. The **only** variable left is the number of protons pulling inward. More protons → same electron cloud pulled in tighter → smaller ion. (This is the same "protons decide" logic from [Periodic Trends](/chemistry/0305-periodic-trends).)

| Species | Protons | Radius (pm) |
|---|---|---|
| $\ce{N^3-}$ | 7 | 146 |
| $\ce{O^2-}$ | 8 | 140 |
| $\ce{F-}$ | 9 | 133 |
| $\ce{Na+}$ | 11 | 102 |
| $\ce{Mg^2+}$ | 12 | 72 |
| $\ce{Al^3+}$ | 13 | 54 |

**Rule: in an isoelectronic series, radius decreases as proton count (atomic number) increases.** The trap answer — "more electrons means bigger" — is useless here because everyone has the same electrons.

### Step 7: From Ions to Formulas (Quick Review)

You already built this skill in [Ionic vs Covalent](/chemistry/0203-ionic-vs-covalent) and [Naming Compounds](/chemistry/0204-naming-compounds), so just the refresher: **total positive charge must cancel total negative charge**, then reduce to the smallest whole-number ratio.

- $\ce{Ca^2+}$ + $\ce{Cl-}$ → $\ce{CaCl2}$
- $\ce{Al^3+}$ + $\ce{O^2-}$ → $\ce{Al2O3}$ (criss-cross: $2 \times 3+ = 3 \times 2-$)
- $\ce{Mg^2+}$ + $\ce{O^2-}$ → $\ce{MgO}$ (criss-cross gives $\ce{Mg2O2}$ — reduce!)

And the vocabulary reminder that costs real AP points: $\ce{NaCl}$ is a **formula unit** — the simplest ratio of ions in a giant lattice. There is no $\ce{NaCl}$ molecule, the same way there's no "one magnet" that *is* the whole fridge door.

### Step 8: Lattice Energy — the Grip Strength of the Whole Fridge

**Definition:** lattice energy is the energy required to separate **one mole of an ionic solid into its gaseous ions**:

$$\ce{NaCl(s) -> Na+(g) + Cl-(g)} \qquad \Delta E = +786\ \text{kJ/mol}$$

It's the "strip every magnet off the door and carry them across the room" number. Bigger lattice energy = stronger grip = harder solid, higher melting point.

Coulomb's law tells us what controls it:

$$E \;\propto\; \frac{|q_1\, q_2|}{r}$$

where $q_1, q_2$ are the ion charges and $r$ is the distance between ion centers (the sum of the two ionic radii).

Two dials, in strict priority order:

1. **Charge (the magnet's strength) — dominates.** Charges multiply. Going from a $(1+)(1-)$ pair to a $(2+)(2-)$ pair quadruples the numerator. No realistic radius change can compete with a factor of 4.
2. **Radius (the sticky-note gap) — tiebreaker.** Smaller ions sit closer, $r$ shrinks, attraction grows. Use radius to rank compounds whose charge products are *equal*.

Watch it work on real compounds:

| Compound | Ions | $\lvert q_1 q_2 \rvert$ | Ion sizes | Lattice energy (kJ/mol) | Melting point |
|---|---|---|---|---|---|
| $\ce{MgO}$ | $\ce{Mg^2+}, \ce{O^2-}$ | 4 | small + small | $\approx 3795$ | 2852°C |
| $\ce{CaO}$ | $\ce{Ca^2+}, \ce{O^2-}$ | 4 | bigger cation | $\approx 3414$ | 2613°C |
| $\ce{LiF}$ | $\ce{Li+}, \ce{F-}$ | 1 | small + small | $\approx 1036$ | 845°C |
| $\ce{NaCl}$ | $\ce{Na+}, \ce{Cl-}$ | 1 | medium | $\approx 786$ | 801°C |
| $\ce{KBr}$ | $\ce{K+}, \ce{Br-}$ | 1 | big + big | $\approx 671$ | 734°C |

Read that table like a fridge inspection:

- **Charge sorts the leagues.** Every $2+/2-$ compound crushes every $1+/1-$ compound. $\ce{CaO}$'s ions are *bigger* than $\ce{LiF}$'s, and it still wins by a factor of three — heavy-duty magnet with a sticky note beats souvenir magnet flush on the door.
- **Radius sorts within a league.** Among the $1+/1-$ salts: $\ce{LiF} > \ce{NaCl} > \ce{KBr}$, because down a group the ions swell ($\ce{Li+} \to \ce{Na+} \to \ce{K+}$ and $\ce{F-} \to \ce{Cl-} \to \ce{Br-}$), $r$ grows, grip weakens.
- **Melting points track lattice energy.** Melting an ionic solid means shaking ions loose from the lattice. Stronger grip → more thermal energy needed → higher melting point. The 2852°C vs. 801°C gap between $\ce{MgO}$ and $\ce{NaCl}$ isn't trivia — it's Coulomb's law you can measure with a thermometer. (It's also why $\ce{MgO}$ lines the insides of high-temperature furnaces.)

### Step 9: Properties of Ionic Solids, AP Edition

**Brittleness — the flipped magnet.** In the intact lattice, every cation touches anions and vice versa — all attractions. Strike the crystal and one layer shifts by one ion-position: suddenly cations align with cations and anions with anions. Like-charge repulsion along that entire plane blows the layers apart, and the crystal **shatters** along clean flat faces instead of denting. Flip one fridge magnet around and it doesn't hold weakly — it actively shoves itself off the door.

**Conductivity — ions must MOVE.** Conducting electricity requires *mobile charged particles*.

| State | Are ions mobile? | Conducts? |
|---|---|---|
| Solid $\ce{NaCl}$ | No — locked in the lattice | No |
| Molten $\ce{NaCl}$ (>801°C) | Yes — lattice destroyed, ions flow | Yes |
| $\ce{NaCl(aq)}$ | Yes — $\ce{Na+}$ and $\ce{Cl-}$ drift freely in water | Yes |

The charges exist in all three states; only their **mobility** changes. On an FRQ, "ionic compounds conduct when dissolved because the ions are free to move" earns the point; "because it's ionic" does not.

---

## Worked Examples

**Example 1: Valence Electrons from a Configuration**

**Problem:** Sulfur's electron configuration is $1s^2\,2s^2\,2p^6\,3s^2\,3p^4$. How many valence electrons does sulfur have?

**Solution:**

Step 1: Find the highest principal quantum number: $n = 3$.

Step 2: Count all electrons with $n = 3$: the $3s^2$ (2 electrons) and the $3p^4$ (4 electrons).

Step 3: $2 + 4 = 6$. Check against the shortcut: sulfur is in Group 16, ones digit 6. ✓

**Answer: 6 valence electrons.**

---

**Example 2: Lewis Dot Symbols**

**Problem:** Draw Lewis dot symbols for $\ce{Mg}$, $\ce{P}$, and $\ce{Br}$.

**Solution:**

Step 1: Count valence electrons. $\ce{Mg}$ (Group 2): 2. $\ce{P}$ (Group 15): 5. $\ce{Br}$ (Group 17): 7.

Step 2: Place one dot per side before pairing any:

```
                  .              ..
   . Mg .       . P :          : Br :
                  .              .
```

**Answer: Mg shows 2 unpaired dots, P shows one pair + three singles, Br shows three pairs + one single.**

---

**Example 3: Why $\ce{Na+}$ and Not $\ce{Na^2+}$**

**Problem:** Sodium's first ionization energy is $496\ \text{kJ/mol}$; its second is $4562\ \text{kJ/mol}$. Explain why sodium forms $\ce{Na+}$ rather than $\ce{Na^2+}$ — without using the word "wants."

**Solution:**

Step 1: Write the configurations. $\ce{Na}$: $1s^2\,2s^2\,2p^6\,3s^1$. After losing one electron, $\ce{Na+}$: $1s^2\,2s^2\,2p^6$ — a filled $n=2$ shell.

Step 2: The first electron removed is the lone $3s$ electron — far from the nucleus, well shielded by 10 core electrons, so it experiences a small effective nuclear charge. Cheap to remove.

Step 3: The second electron would come from the filled $2p$ subshell — a **core** electron, much closer to the nucleus and far less shielded. By Coulomb's law the attraction on it is much larger, so removing it costs $\sim$9× the energy ($4562$ vs. $496\ \text{kJ/mol}$). That cost is never repaid by lattice formation.

**Answer: $\ce{Na+}$ forms because removing the single high-energy $3s$ electron is energetically cheap, while removing a second (core) electron from the filled $n=2$ shell costs prohibitively more energy.**

---

**Example 4: Configurations of Anions**

**Problem:** Write the electron configurations of $\ce{O^2-}$ and $\ce{P^3-}$, and name the noble gas each is isoelectronic with.

**Solution:**

Step 1: $\ce{O}$ is $1s^2\,2s^2\,2p^4$ (8 electrons). Add 2: $\ce{O^2-}$ is $1s^2\,2s^2\,2p^6$ (10 electrons) — isoelectronic with $\ce{Ne}$.

Step 2: $\ce{P}$ is $[\text{Ne}]\,3s^2\,3p^3$ (15 electrons). Add 3: $\ce{P^3-}$ is $[\text{Ne}]\,3s^2\,3p^6$ (18 electrons) — isoelectronic with $\ce{Ar}$.

**Answer: $\ce{O^2-}$: $1s^2\,2s^2\,2p^6$ (neon); $\ce{P^3-}$: $[\text{Ne}]\,3s^2\,3p^6$ (argon).**

---

**Example 5: Transition-Metal Cations ($4s$ First!)**

**Problem:** Write the electron configurations of $\ce{Fe^2+}$, $\ce{Fe^3+}$, and $\ce{Zn^2+}$.

**Solution:**

Step 1: Neutral atoms: $\ce{Fe}$ is $[\text{Ar}]\,3d^6\,4s^2$; $\ce{Zn}$ is $[\text{Ar}]\,3d^{10}\,4s^2$.

Step 2: Cations lose the $4s$ electrons **first** — they're the highest-energy, outermost electrons in the neutral atom.

Step 3:
- $\ce{Fe^2+}$: remove both $4s$ → $[\text{Ar}]\,3d^6$
- $\ce{Fe^3+}$: remove one more, from $3d$ → $[\text{Ar}]\,3d^5$ (half-filled subshell)
- $\ce{Zn^2+}$: remove both $4s$ → $[\text{Ar}]\,3d^{10}$

**Answer: $\ce{Fe^2+} = [\text{Ar}]\,3d^6$, $\ce{Fe^3+} = [\text{Ar}]\,3d^5$, $\ce{Zn^2+} = [\text{Ar}]\,3d^{10}$. Never leave $4s$ electrons behind while removing $3d$.**

---

**Example 6: Ranking an Isoelectronic Series**

**Problem:** Rank $\ce{S^2-}$, $\ce{Cl-}$, $\ce{K+}$, and $\ce{Ca^2+}$ from largest to smallest radius, and justify.

**Solution:**

Step 1: Count electrons: $\ce{S^2-}$: $16+2 = 18$; $\ce{Cl-}$: $17+1 = 18$; $\ce{K+}$: $19-1 = 18$; $\ce{Ca^2+}$: $20-2 = 18$. All isoelectronic (argon configuration).

Step 2: Same electron cloud, so proton count alone sets the size: S has 16, Cl has 17, K has 19, Ca has 20.

Step 3: More protons → stronger pull on the *same* 18 electrons → smaller radius.

**Answer: $\ce{S^2-} > \ce{Cl-} > \ce{K+} > \ce{Ca^2+}$. All four have 18 electrons; $\ce{Ca^2+}$'s 20 protons pull that cloud in tightest, $\ce{S^2-}$'s 16 protons pull weakest.**

---

**Example 7: Charges to Formulas**

**Problem:** Predict the formula of the compound formed by (a) calcium and nitrogen, (b) aluminum and sulfur.

**Solution:**

Step 1: Predict ions from group positions. $\ce{Ca}$ (Group 2) → $\ce{Ca^2+}$. $\ce{N}$ (Group 15) → $\ce{N^3-}$. $\ce{Al}$ (Group 13) → $\ce{Al^3+}$. $\ce{S}$ (Group 16) → $\ce{S^2-}$.

Step 2: Balance the charges (criss-cross, then reduce).
(a) $3 \times (2+) = 2 \times (3-)$ → $\ce{Ca3N2}$.
(b) $2 \times (3+) = 3 \times (2-)$ → $\ce{Al2S3}$.

**Answer: (a) $\ce{Ca3N2}$, (b) $\ce{Al2S3}$ — each written as a formula unit, the smallest neutral ratio of ions.**

---

**Example 8: Ranking Lattice Energies (Charge Dominates)**

**Problem:** Rank $\ce{NaCl}$, $\ce{MgO}$, $\ce{KBr}$, and $\ce{CaO}$ from largest to smallest lattice energy.

**Solution:**

Step 1: Sort by charge product first. $\ce{MgO}$ and $\ce{CaO}$ are $(2+)(2-)$: product 4. $\ce{NaCl}$ and $\ce{KBr}$ are $(1+)(1-)$: product 1. The oxides win the top two spots automatically — heavy-duty magnets beat souvenir magnets.

Step 2: Break ties with radius. $\ce{Mg^2+}$ (72 pm) is smaller than $\ce{Ca^2+}$ (100 pm), so $\ce{MgO}$ has smaller $r$ → $\ce{MgO} > \ce{CaO}$. Likewise $\ce{Na+}$ (102 pm) and $\ce{Cl-}$ (181 pm) are smaller than $\ce{K+}$ (138 pm) and $\ce{Br-}$ (196 pm), so $\ce{NaCl} > \ce{KBr}$.

Step 3: Check against measured values: $3795 > 3414 > 786 > 671\ \text{kJ/mol}$. ✓

**Answer: $\ce{MgO} > \ce{CaO} > \ce{NaCl} > \ce{KBr}$. Charge product sets the leagues; radius sorts within them.**

---

**Example 9: Lattice Energy Down a Group**

**Problem:** Without looking up numbers, rank $\ce{LiF}$, $\ce{NaCl}$, and $\ce{KBr}$ by lattice energy, and explain.

**Solution:**

Step 1: All three are $(1+)(1-)$ — identical charge products. Charge can't decide; radius must.

Step 2: Going down the groups, both ions swell: $\ce{Li+}(76) < \ce{Na+}(102) < \ce{K+}(138\ \text{pm})$ and $\ce{F-}(133) < \ce{Cl-}(181) < \ce{Br-}(196\ \text{pm})$.

Step 3: Larger ions → larger $r$ between centers → smaller $\dfrac{|q_1 q_2|}{r}$ → weaker lattice. Every pair adds a thicker sticky note.

**Answer: $\ce{LiF} > \ce{NaCl} > \ce{KBr}$ ($1036 > 786 > 671\ \text{kJ/mol}$). Equal charges, so the smallest ion pair grips hardest.**

---

**Example 10: Melting Points from Lattice Energy**

**Problem:** One of these solids melts at 2852°C, one at 801°C, one at 734°C: $\ce{KBr}$, $\ce{MgO}$, $\ce{NaCl}$. Match them and justify in one AP-ready sentence each.

**Solution:**

Step 1: Melting requires overcoming the lattice — melting point tracks lattice energy.

Step 2: $\ce{MgO}$: charges of $2+$ and $2-$ and small ionic radii give it by far the largest lattice energy → 2852°C.

Step 3: $\ce{NaCl}$ vs. $\ce{KBr}$: same $(1+)(1-)$ product, but $\ce{Na+}$ and $\ce{Cl-}$ are smaller than $\ce{K+}$ and $\ce{Br-}$, so $\ce{NaCl}$ has the stronger lattice → $\ce{NaCl}$ = 801°C, $\ce{KBr}$ = 734°C.

**Answer: $\ce{MgO}$ = 2852°C (charge product 4, small ions), $\ce{NaCl}$ = 801°C, $\ce{KBr}$ = 734°C (equal charges; larger ions → weaker attraction → lower melting point).**

---

**Example 11: Explaining Brittleness and Conductivity**

**Problem:** A student hits a crystal of $\ce{NaCl}$ with a hammer and it shatters; the same crystal doesn't conduct electricity, but conducts well after dissolving in water. Explain both observations.

**Solution:**

Step 1 (shattering): In the lattice, each ion is surrounded by oppositely charged neighbors. The hammer blow slides one layer of ions over by one position, aligning $\ce{Na+}$ with $\ce{Na+}$ and $\ce{Cl-}$ with $\ce{Cl-}$. The like-charge repulsion along that plane pushes the layers apart, so the crystal cleaves instead of bending — the flipped fridge magnet shoving itself off the door.

Step 2 (solid doesn't conduct): The ions are charged but **locked in fixed lattice positions** — no mobile charge carriers, no current.

Step 3 (solution conducts): Water pulls the lattice apart into free $\ce{Na+(aq)}$ and $\ce{Cl-(aq)}$; the ions are now **mobile** and carry charge toward the electrodes.

**Answer: Shattering — a shifted layer brings like charges face to face and they repel; conductivity — the ions must be free to move, which happens only when molten or dissolved.**

---

**Example 12: The Unit 1 Capstone Chain**

**Problem:** Element X is in Period 3, Group 2. Element Y is in Period 2, Group 16. (a) Write ground-state configurations for both atoms. (b) Predict the ion each forms, with configurations. (c) Write the formula of their compound. (d) Compare its lattice energy to $\ce{NaCl}$'s. (e) Predict which solid melts higher, and justify.

**Solution:**

Step 1 (identify + configure): X = $\ce{Mg}$: $1s^2\,2s^2\,2p^6\,3s^2$. Y = $\ce{O}$: $1s^2\,2s^2\,2p^4$.

Step 2 (ions): $\ce{Mg}$ loses its two $3s$ electrons (the third would be a core electron — energetically prohibitive): $\ce{Mg^2+} = 1s^2\,2s^2\,2p^6$. $\ce{O}$ gains two to fill $2p$: $\ce{O^2-} = 1s^2\,2s^2\,2p^6$. Both isoelectronic with neon.

Step 3 (formula): $(2+) + (2-) = 0$ in a 1:1 ratio → $\ce{MgO}$ (one formula unit).

Step 4 (lattice energy): $E \propto \dfrac{|q_1 q_2|}{r}$. $\ce{MgO}$: charge product $= 4$; $\ce{NaCl}$: product $= 1$. Also $\ce{Mg^2+}$ (72 pm) $<$ $\ce{Na+}$ (102 pm) and $\ce{O^2-}$ (140 pm) $<$ $\ce{Cl-}$ (181 pm), so $r$ is smaller too. Both factors point the same way: $\ce{MgO}$'s lattice energy is far larger ($3795$ vs. $786\ \text{kJ/mol}$).

Step 5 (melting point): Larger lattice energy → more energy required to disrupt the lattice → $\ce{MgO}$ melts far higher (2852°C vs. 801°C).

**Answer: $\ce{Mg^2+}$ and $\ce{O^2-}$ form $\ce{MgO}$, whose greater ion charges and smaller ionic radii give a much larger lattice energy than $\ce{NaCl}$, so $\ce{MgO}$ has the much higher melting point.** This five-step chain — position → configuration → ion → formula → Coulomb ranking — *is* the Unit 1 FRQ.

---

## Common Mistakes

| The Mistake | Why It Happens | The Fix |
|---|---|---|
| "Sodium loses an electron, so it's $\ce{Na-}$" | Losing feels like "minus" | Electrons are negative; **losing** a negative makes you **positive**. Count protons vs. electrons. |
| Writing $\ce{Fe^2+}$ as $[\text{Ar}]\,3d^4\,4s^2$ | Filling order ($4s$ before $3d$) applied to emptying | **$4s$ electrons leave first.** $\ce{Fe^2+} = [\text{Ar}]\,3d^6$. |
| Ranking isoelectronic ions by charge or "more electrons = bigger" | The usual radius trend reflex | Isoelectronic species have identical clouds — **only protons differ**. More protons = smaller. |
| "$\ce{MgO}$ has a high melting point because its bonds are strong" | True but scores zero | Name the *cause*: larger ion charges ($2+/2-$) and smaller radii → greater Coulombic attraction → larger lattice energy. |
| Using radius before charge in lattice-energy rankings | Both factors feel equal | Charge product **quadruples** the attraction; radius only nudges it. Sort by charge first, radius as tiebreaker. |
| "Chlorine wants an electron to complete its octet" | Everyday language | Atoms don't want. Say: gaining one electron fills the $3p$ subshell, a lower-energy arrangement. |
| "A molecule of $\ce{NaCl}$" | Molecule = generic word for particle in everyday speech | Ionic solids are lattices; $\ce{NaCl}$ is a **formula unit** (a ratio, not a particle). |
| Forgetting to reduce: $\ce{Mg2O2}$, $\ce{Ca2S2}$ | Criss-cross on autopilot | Criss-cross, then **reduce to smallest whole numbers**. |
| "Solid $\ce{NaCl}$ conducts because it has charges" | Charge vs. *mobile* charge | Conduction needs charges that **move**. Solid = locked lattice = no. Molten/dissolved = yes. |

---

## AP Exam Tips

1. **"Compare the melting points and justify" = a lattice-energy Coulomb argument, every single time.** The College Board grades a specific chain: identify the ion **charges** → compare **radii** if charges tie → cite $E \propto \frac{|q_1 q_2|}{r}$ → link larger lattice energy to more energy needed to separate ions. Skipping straight to "stronger bonds" without naming charges or sizes is the single most common lost point on this topic.

2. **Memorize the justification template:** "*Compound A has ions with larger charges ($n+$ and $n-$) [and/or smaller ionic radii], so by Coulomb's law the electrostatic attractions in the lattice are stronger. Its lattice energy is larger, so more energy is required to separate the ions, giving A the higher melting point.*" Swap in the actual ions and numbers.

3. **Charges before radii, always.** If the charge products differ, radius is optional garnish. If the charge products are equal, radius is the whole argument. State which case you're in.

4. **Ban "wants," "likes," "happy," and "desires" from every justification.** Graders are explicitly told these earn nothing. Translate to energy: "lower-energy arrangement," "greater Coulombic attraction," "energy required to remove a core electron is much larger."

5. **Transition-metal configurations are a favorite multiple-choice trap.** If a cation's configuration keeps its $4s$ electrons while dropping $3d$, it's wrong. Also expect "which species is isoelectronic with argon?" — just count electrons.

6. **Successive-ionization-energy tables identify the group.** A giant jump between the $n$th and $(n{+}1)$th ionization energies means the atom has $n$ valence electrons — the $(n{+}1)$th comes from the core. This crosses over from [Periodic Trends](/chemistry/0305-periodic-trends) and appears constantly.

7. **No calculator needed anywhere here.** Every lattice-energy question is a *ranking* or *justification*, never a computation. If you're crunching numbers, you've misread the question.

---

## Practice Problems

### Problem 1
Using their electron configurations, determine the number of valence electrons in (a) $\ce{K}$, (b) $\ce{As}$, (c) $\ce{Br}$.

<details>
<summary><strong>Solution</strong></summary>

(a) $\ce{K}$: $[\text{Ar}]\,4s^1$ → highest shell $n=4$ holds 1 electron → **1 valence electron**.

(b) $\ce{As}$: $[\text{Ar}]\,3d^{10}\,4s^2\,4p^3$ → count only $n=4$: $4s^2 4p^3$ → $2+3 =$ **5 valence electrons** (the filled $3d$ is not valence).

(c) $\ce{Br}$: $[\text{Ar}]\,3d^{10}\,4s^2\,4p^5$ → $4s^2 4p^5$ → **7 valence electrons**.

**Answers: 1, 5, 7.**

</details>

### Problem 2
Draw Lewis dot symbols for $\ce{Ca}$, $\ce{N}$, and $\ce{I}$, and for the ions $\ce{Ca^2+}$ and $\ce{I-}$.

<details>
<summary><strong>Solution</strong></summary>

Valence counts: $\ce{Ca}$ (Group 2) = 2, $\ce{N}$ (Group 15) = 5, $\ce{I}$ (Group 17) = 7.

```
                 .             ..                            ..    -
  . Ca .       . N :         : I :        Ca 2+          [ : I : ]
                 .             .                             ..
```

$\ce{Ca^2+}$ has lost both dots (bare symbol with the charge); $\ce{I-}$ has gained one dot to reach eight and wears brackets with the charge.

**Answer: as drawn — cations lose all dots, anions show a full octet in brackets.**

</details>

### Problem 3
Write ground-state electron configurations for $\ce{Al^3+}$, $\ce{S^2-}$, and $\ce{K+}$. Which noble gas is each isoelectronic with?

<details>
<summary><strong>Solution</strong></summary>

$\ce{Al}$ ($[\text{Ne}]\,3s^2\,3p^1$) loses 3: $\ce{Al^3+} = 1s^2\,2s^2\,2p^6$ — **neon**.

$\ce{S}$ ($[\text{Ne}]\,3s^2\,3p^4$) gains 2: $\ce{S^2-} = [\text{Ne}]\,3s^2\,3p^6$ — **argon**.

$\ce{K}$ ($[\text{Ar}]\,4s^1$) loses 1: $\ce{K+} = 1s^2\,2s^2\,2p^6\,3s^2\,3p^6$ — **argon**.

**Answer: $\ce{Al^3+}$ ↔ Ne; $\ce{S^2-}$ and $\ce{K+}$ ↔ Ar.**

</details>

### Problem 4
Predict the most common ion formed by each element, using its periodic-table position: $\ce{Ba}$, $\ce{I}$, $\ce{P}$, $\ce{Rb}$, $\ce{Se}$.

<details>
<summary><strong>Solution</strong></summary>

- $\ce{Ba}$ (Group 2): loses 2 → $\ce{Ba^2+}$
- $\ce{I}$ (Group 17): gains 1 → $\ce{I-}$
- $\ce{P}$ (Group 15): gains 3 → $\ce{P^3-}$
- $\ce{Rb}$ (Group 1): loses 1 → $\ce{Rb+}$
- $\ce{Se}$ (Group 16): gains 2 → $\ce{Se^2-}$

Each change produces a noble-gas (filled-shell) configuration — the low-energy arrangement.

**Answer: $\ce{Ba^2+}$, $\ce{I-}$, $\ce{P^3-}$, $\ce{Rb+}$, $\ce{Se^2-}$.**

</details>

### Problem 5
Write the electron configuration of $\ce{Cu+}$ and $\ce{Mn^2+}$. (Copper's neutral configuration is the exception $[\text{Ar}]\,3d^{10}\,4s^1$.)

<details>
<summary><strong>Solution</strong></summary>

$\ce{Cu}$: $[\text{Ar}]\,3d^{10}\,4s^1$. Remove the $4s$ electron first: $\ce{Cu+} = [\text{Ar}]\,3d^{10}$ — a filled $d$ subshell, which is why $\ce{Cu+}$ is stable.

$\ce{Mn}$: $[\text{Ar}]\,3d^5\,4s^2$. Remove both $4s$: $\ce{Mn^2+} = [\text{Ar}]\,3d^5$ — half-filled $d$ subshell.

**Answer: $\ce{Cu+} = [\text{Ar}]\,3d^{10}$; $\ce{Mn^2+} = [\text{Ar}]\,3d^5$. The $4s$ electrons always leave before $3d$.**

</details>

### Problem 6
Which of the following are isoelectronic with $\ce{Ar}$: $\ce{Na+}$, $\ce{Cl-}$, $\ce{Ca^2+}$, $\ce{O^2-}$, $\ce{K+}$?

<details>
<summary><strong>Solution</strong></summary>

Argon has 18 electrons. Count each:

- $\ce{Na+}$: $11-1 = 10$ — no (neon)
- $\ce{Cl-}$: $17+1 = 18$ — **yes**
- $\ce{Ca^2+}$: $20-2 = 18$ — **yes**
- $\ce{O^2-}$: $8+2 = 10$ — no (neon)
- $\ce{K+}$: $19-1 = 18$ — **yes**

**Answer: $\ce{Cl-}$, $\ce{Ca^2+}$, and $\ce{K+}$.**

</details>

### Problem 7
Rank from largest to smallest radius: $\ce{Mg^2+}$, $\ce{F-}$, $\ce{Na+}$, $\ce{O^2-}$, $\ce{Al^3+}$. Justify in one sentence.

<details>
<summary><strong>Solution</strong></summary>

All five have 10 electrons (isoelectronic with neon), so the only difference is proton count: O 8, F 9, Na 11, Mg 12, Al 13. More protons pull the identical electron cloud in tighter.

**Answer: $\ce{O^2-} > \ce{F-} > \ce{Na+} > \ce{Mg^2+} > \ce{Al^3+}$ — same electron cloud, so the species with the fewest protons holds it most loosely (largest), and the most protons squeeze it smallest.**

</details>

### Problem 8
Write the formula unit for the compound formed from (a) strontium and bromine, (b) aluminum and oxygen, (c) barium and sulfur.

<details>
<summary><strong>Solution</strong></summary>

(a) $\ce{Sr^2+}$ + $\ce{Br-}$ → need two bromides → $\ce{SrBr2}$.

(b) $\ce{Al^3+}$ + $\ce{O^2-}$ → criss-cross → $\ce{Al2O3}$ ($2 \times 3+ = 6+$ balances $3 \times 2- = 6-$).

(c) $\ce{Ba^2+}$ + $\ce{S^2-}$ → criss-cross gives $\ce{Ba2S2}$ → **reduce** → $\ce{BaS}$.

**Answer: (a) $\ce{SrBr2}$, (b) $\ce{Al2O3}$, (c) $\ce{BaS}$.**

</details>

### Problem 9
Rank $\ce{KCl}$, $\ce{CaO}$, and $\ce{NaF}$ from largest to smallest lattice energy.

<details>
<summary><strong>Solution</strong></summary>

Step 1 — charge products: $\ce{CaO}$ is $(2+)(2-) = 4$; $\ce{KCl}$ and $\ce{NaF}$ are both $(1+)(1-) = 1$. $\ce{CaO}$ wins outright.

Step 2 — radius tiebreaker for the $1{:}1$ salts: $\ce{Na+}$ (102 pm) $<$ $\ce{K+}$ (138 pm) and $\ce{F-}$ (133 pm) $<$ $\ce{Cl-}$ (181 pm), so $\ce{NaF}$ has the smaller inter-ionic distance → larger lattice energy than $\ce{KCl}$.

**Answer: $\ce{CaO} > \ce{NaF} > \ce{KCl}$. Charge dominates; radius breaks the tie.**

</details>

### Problem 10
The melting points 993°C, 2852°C, and 734°C belong to $\ce{KBr}$, $\ce{NaF}$, and $\ce{MgO}$ in some order. Match them and justify.

<details>
<summary><strong>Solution</strong></summary>

$\ce{MgO}$: charge product 4 with small ions → largest lattice energy → **2852°C**.

$\ce{NaF}$ vs. $\ce{KBr}$: both $(1+)(1-)$, but $\ce{Na+}$ and $\ce{F-}$ are much smaller than $\ce{K+}$ and $\ce{Br-}$ → stronger attraction → $\ce{NaF}$ = **993°C**, $\ce{KBr}$ = **734°C**.

**Answer: $\ce{MgO}$ 2852°C, $\ce{NaF}$ 993°C, $\ce{KBr}$ 734°C.**

</details>

### Problem 11
$\ce{MgO}$ melts at 2852°C; $\ce{NaCl}$ melts at 801°C. Write a full-credit AP justification for this difference.

<details>
<summary><strong>Solution</strong></summary>

Full-credit answer: "$\ce{MgO}$ consists of $\ce{Mg^2+}$ and $\ce{O^2-}$ ions, while $\ce{NaCl}$ consists of $\ce{Na+}$ and $\ce{Cl-}$ ions. Because lattice energy is proportional to $\frac{|q_1 q_2|}{r}$, the doubled charges in $\ce{MgO}$ make its Coulombic attractions roughly four times stronger, and its smaller ionic radii ($\ce{Mg^2+} < \ce{Na+}$, $\ce{O^2-} < \ce{Cl-}$) strengthen them further. $\ce{MgO}$ therefore has a much larger lattice energy, so much more thermal energy is required to separate its ions, giving it the far higher melting point."

Points earned by: naming the **charges**, comparing the **radii**, invoking **Coulomb's law / lattice energy**, and linking to **energy needed to separate ions**. "MgO has stronger bonds" alone earns nothing.

**Answer: see the template above — charges first, radii second, Coulomb connection explicit.**

</details>

### Problem 12
Both $\ce{LiF}$ and $\ce{KBr}$ contain $1+$ and $1-$ ions, yet their lattice energies are about $1036$ and $671\ \text{kJ/mol}$. Explain the difference.

<details>
<summary><strong>Solution</strong></summary>

The charge products are identical, so the difference is entirely inter-ionic distance $r$. $\ce{Li+}$ (76 pm) and $\ce{F-}$ (133 pm) are near the top of their groups; $\ce{K+}$ (138 pm) and $\ce{Br-}$ (196 pm) sit two rows lower with two extra electron shells each. Larger ions keep their charge centers farther apart, and since $E \propto \frac{|q_1 q_2|}{r}$, larger $r$ means weaker attraction throughout the lattice.

**Answer: with equal charges, the much smaller $\ce{Li+}$/$\ce{F-}$ pair sits closer together (smaller $r$), giving $\ce{LiF}$ the substantially larger lattice energy.**

</details>

### Problem 13
A crystal of $\ce{CaF2}$ shatters when struck, but a piece of copper metal just dents. Explain the shattering in terms of the ionic lattice.

<details>
<summary><strong>Solution</strong></summary>

In the intact $\ce{CaF2}$ lattice, each ion is surrounded by oppositely charged neighbors, so every close contact is attractive. A sharp blow slides one plane of ions relative to the next; the shift brings $\ce{Ca^2+}$ ions opposite $\ce{Ca^2+}$ and $\ce{F-}$ opposite $\ce{F-}$. Like charges repel along the entire plane at once, forcing the layers apart — the crystal cleaves rather than deforming. (In copper, the sea of delocalized electrons re-forms bonds as atoms slide, so it dents instead.)

**Answer: shifting a layer by one position aligns like charges, and their mutual repulsion splits the crystal — the flipped-fridge-magnet effect.**

</details>

### Problem 14
Solid $\ce{KCl}$ does not conduct electricity. Describe two different things you could do to the sample to make it conduct, and explain why each works.

<details>
<summary><strong>Solution</strong></summary>

Option 1 — **melt it** (heat above 770°C): the lattice breaks down and the $\ce{K+}$ and $\ce{Cl-}$ ions become free-flowing charged particles that can migrate and carry current.

Option 2 — **dissolve it in water**: $\ce{KCl(s) -> K+(aq) + Cl-(aq)}$; the hydrated ions move freely through the solution.

Both work for the same reason: conduction requires **mobile** charged particles. The ions exist in the solid too, but they are locked in fixed lattice positions and cannot move.

**Answer: melt it or dissolve it — either frees the ions to move, and mobile ions are what carry the current.**

</details>

### Problem 15
Element A is in Period 4, Group 2. Element B is in Period 3, Group 17. (a) Write both atoms' configurations. (b) Predict the ions and write their configurations. (c) Give the formula of the compound. (d) Predict whether its melting point is higher or lower than that of $\ce{CaO}$, and justify.

<details>
<summary><strong>Solution</strong></summary>

(a) A = $\ce{Ca}$: $[\text{Ar}]\,4s^2$. B = $\ce{Cl}$: $[\text{Ne}]\,3s^2\,3p^5$.

(b) $\ce{Ca}$ loses its two $4s$ electrons (a third would come from the argon core — prohibitively expensive): $\ce{Ca^2+} = [\text{Ar}]$, i.e. $1s^2\,2s^2\,2p^6\,3s^2\,3p^6$. $\ce{Cl}$ gains one: $\ce{Cl-} = [\text{Ne}]\,3s^2\,3p^6$. Both are isoelectronic with argon.

(c) $\ce{Ca^2+}$ needs two $\ce{Cl-}$ to balance: $\ce{CaCl2}$.

(d) Compare with $\ce{CaO}$: same cation, but $\ce{CaO}$ pairs it with $\ce{O^2-}$ (charge product 4) while $\ce{CaCl2}$ pairs it with $\ce{Cl-}$ (charge product 2). By $E \propto \frac{|q_1 q_2|}{r}$, $\ce{CaO}$'s lattice energy is much larger ($\ce{O^2-}$ is also smaller than $\ce{Cl-}$, reinforcing the gap). Larger lattice energy → more energy to separate the ions → higher melting point for $\ce{CaO}$. Reality check: $\ce{CaO}$ melts at 2613°C, $\ce{CaCl2}$ at about 775°C.

**Answer: $\ce{CaCl2}$, and it melts far *lower* than $\ce{CaO}$ because the smaller anion charge (1− vs. 2−) and larger anion radius both reduce the Coulombic attraction — smaller lattice energy, lower melting point.**

</details>

---

## Quick Reference

| Concept | The Rule | Fridge-Magnet Version |
|---|---|---|
| Valence electrons (main group) | Electrons in the highest $n$ shell = group's ones digit | Dots on the Lewis symbol |
| Cation formation | Metals lose all outer-shell electrons → noble-gas core | — |
| Anion formation | Nonmetals gain to fill $ns^2np^6$ | — |
| Transition-metal cations | **$4s$ leaves before $3d$** ($\ce{Fe^2+} = [\text{Ar}]3d^6$) | — |
| Isoelectronic radius | Same electrons → **more protons = smaller** | — |
| Formula unit | Smallest neutral ratio of ions; never "molecule" | The ratio of magnets to door area, not one magnet |
| Lattice energy | Energy to separate 1 mol of solid into gaseous ions; $E \propto \frac{\lvert q_1 q_2 \rvert}{r}$ | Energy to strip every magnet off the door |
| Ranking lattice energy | **Charge product first** (4 beats 1), radius as tiebreaker | Magnet strength first, sticky-note gap second |
| Down a group | Bigger ions → larger $r$ → weaker lattice ($\ce{LiF} > \ce{NaCl} > \ce{KBr}$) | Thicker sticky notes down the group |
| Melting point | Tracks lattice energy ($\ce{MgO}$ 2852°C vs. $\ce{NaCl}$ 801°C) | Strong-grip fridge takes more effort to clear |
| Brittleness | Shifted layer aligns like charges → repulsion → cleaves | Flip a magnet and it shoves itself off |
| Conductivity | Only with **mobile** ions: molten or dissolved, never solid | Magnets conduct the vibe only once they're off the door |
| Justification language | Energy and Coulomb's law — never "wants" | — |

---

<div align="center">

[← Periodic Trends](/chemistry/0305-periodic-trends) | [Bonds and Electronegativity →](/chemistry/0401-bonds-and-electronegativity)

</div>
