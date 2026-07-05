# Polarity and Hybridization
<p class="article-date">July 4, 2026</p>

*Last weekend we helped my aunt move, and I learned everything about molecular polarity from one dining table. Four of us grabbed the four corners, and as long as we lifted with equal strength from symmetric spots, the table floated dead level across the driveway — every pull canceled every other pull. Then my little cousin "helped" by replacing one corner-carrier, and the table instantly tilted toward the three strong sides: same table, same pulls, but now they didn't cancel, and the whole thing leaned one way. Molecules do exactly this — polar bonds are corner-carriers pulling on electrons, and whether the molecule as a whole "leans" (is polar) depends entirely on whether those pulls cancel by symmetry. And that night at dinner, Dad supplied the second half of this article without knowing it: his HP printers don't stock an orange cartridge — they blend standard inks into whatever color the page needs, which is precisely what carbon does when it blends its stock s and p orbitals into custom hybrid orbitals. Table-carrying plus ink-mixing is the whole of Topic 2.7 — the capstone of Unit 2, where Lewis structures, VSEPR, and electronegativity finally snap together into the full formula-to-properties pipeline the AP exam loves to test.*

---

## What You'll Learn

- Run the **two-question polarity test** on any molecule: are the bonds polar, and do the bond dipoles cancel by symmetry?
- Explain why molecules like $\ce{CO2}$, $\ce{BF3}$, and $\ce{CCl4}$ are **nonpolar despite having polar bonds**
- Explain why $\ce{H2O}$, $\ce{NH3}$, $\ce{SO2}$, and $\ce{CHCl3}$ are polar, using both bond dipoles *and* geometry in FRQ-ready language
- Use the "symmetric substitution" shortcut for polarity — and recognize where it breaks
- Assign hybridization ($sp$, $sp^2$, $sp^3$) to any atom by **counting electron domains**, never by memorizing molecules
- Explain hybridization as orbital mixing: one $s$ + some number of $p$ orbitals blend into identical hybrids
- Count sigma ($\sigma$) and pi ($\pi$) bonds in any molecule: single = $1\sigma$, double = $1\sigma + 1\pi$, triple = $1\sigma + 2\pi$
- Explain why $\pi$ bonds live in **unhybridized p orbitals** and why they prevent rotation around a double bond
- Run the complete Unit 2 pipeline — formula → Lewis → resonance → geometry → polarity → hybridization → $\sigma/\pi$ count — start to finish on one molecule

---

## Prerequisites

- [VSEPR and Molecular Geometry](/chemistry/0406-vsepr-molecular-geometry) — polarity is geometry plus bond dipoles; you cannot decide whether pulls cancel until you know the shape, and hybridization comes straight from the same electron-domain count
- [Bonds and Electronegativity](/chemistry/0401-bonds-and-electronegativity) — bond dipoles (the individual "pulls") come from electronegativity differences; this article asks whether those pulls cancel

---

## The Core Concept

### Intuition First

Back to the driveway, because the table has to earn its keep.

**Each polar bond is a corner-carrier.** In [Bonds and Electronegativity](/chemistry/0401-bonds-and-electronegativity) we saw that when two bonded atoms have different electronegativities, the shared electrons sit closer to the greedier atom — the bond has a **bond dipole**, a little pull with a size and a direction. One carrier gripping one corner, pulling up with some strength, in some direction.

**The molecule is the table.** The question that matters isn't "is any single carrier strong?" It's "do all the pulls, taken together, leave the table level?" Four equally strong people at four symmetric corners can pull as hard as they want — the table stays level, because every pull is exactly balanced by the pulls across from it. That's $\ce{CCl4}$: four strongly polar $\ce{C-Cl}$ bonds arranged in a perfect tetrahedron. Big pulls, perfect symmetry, zero net lean. **Nonpolar molecule.**

**Break the symmetry and the table tilts.** Swap one strong carrier for my little cousin — that's $\ce{CHCl3}$, where one $\ce{Cl}$ is replaced by $\ce{H}$. Three strong pulls on one side, one weak pull on the other. The pulls no longer cancel, and the table leans toward the three chlorines. That net lean is the **molecular dipole**, and the molecule is **polar**. Or keep all the carriers equally strong but make two of them stand on the same side of the table — that's bent $\ce{H2O}$: both $\ce{O-H}$ dipoles point up toward oxygen from the same side, so they *add* instead of canceling. Water leans hard.

Notice what we did NOT do: no vector components, no trigonometry. The AP exam wants exactly this level of reasoning — **equal pulls in symmetric directions cancel; unequal pulls, or symmetric pulls in an asymmetric shape, don't.** That's the entire vector math of Topic 2.7 in table-carrying language.

Then there's the second story. Hybridization answers a question Lewis structures quietly ignore: carbon's stock orbitals are one spherical $2s$ and three dumbbell-shaped $2p$ orbitals — different shapes, different energies. So why are the four $\ce{C-H}$ bonds in $\ce{CH4}$ **perfectly identical**, at perfect 109.5° angles? Dad's printers have the answer. A printer carries cyan, magenta, yellow, black — and when the page needs orange, it doesn't apologize for not stocking orange. It **mixes** standard inks into the exact color required. Carbon does the same: it blends its one $s$ and three $p$ stock orbitals into **four identical $sp^3$ hybrid orbitals**, custom-made for four identical bonds. Need only three bonds ($\ce{BF3}$, or a double-bonded carbon)? Mix $s$ with just two $p$'s → three $sp^2$ hybrids. Need two? Mix $s$ with one $p$ → two $sp$ hybrids. And the stock inks you *didn't* mix — the leftover unhybridized $p$ orbitals — are exactly where $\pi$ bonds come from. Keep that "leftover stock ink" idea; it's the key to the whole sigma/pi section.

### Part 1: Molecular Polarity — The Two-Question Test

A molecule is polar when it has a **net molecular dipole** — a permanent lopsided distribution of electron density, with a partially negative end ($\delta^-$) and a partially positive end ($\delta^+$). To decide, ask exactly two questions, in order:

$$\boxed{\textbf{Q1: Are the bonds polar?} \quad\longrightarrow\quad \textbf{Q2: Do the bond dipoles cancel by symmetry?}}$$

| Q1: Polar bonds? | Q2: Dipoles cancel? | Verdict | Table picture |
|---|---|---|---|
| No | — | **Nonpolar** | Nobody is pulling at all |
| Yes | Yes (symmetric shape, identical outer atoms) | **Nonpolar** | Equal carriers, symmetric corners — level table |
| Yes | No (lone pairs bend the shape, or outer atoms differ) | **Polar** | The table tilts — net lean = molecular dipole |

**Q1 comes from electronegativity** (article 0401): a bond between atoms of different electronegativity is polar. $\ce{N-N}$ and $\ce{Cl-Cl}$ bonds are nonpolar (identical atoms); $\ce{C-H}$ is *nearly* nonpolar (electronegativity difference ≈ 0.4 — AP treats it as essentially nonpolar); $\ce{O-H}$, $\ce{C-O}$, $\ce{C-Cl}$, $\ce{N-H}$ are solidly polar.

**Q2 comes from geometry** (article 0406). Bond dipoles cancel when **both** of these hold:

1. The molecular shape is one of the fully symmetric ones — **linear ($\ce{AX2}$), trigonal planar ($\ce{AX3}$), or tetrahedral ($\ce{AX4}$)** with *no lone pairs on the central atom*, and
2. **All outer atoms are identical.**

Break either condition and the dipoles don't cancel.

### The Classification Gallery

Here is the whole AP cast of characters, sorted by how the two-question test plays out.

**Nonpolar despite polar bonds** (strong carriers, perfect symmetry — the classic AP trap):

| Molecule | Shape | Why the dipoles cancel |
|---|---|---|
| $\ce{CO2}$ | Linear | Two equal $\ce{C=O}$ dipoles point in exactly opposite directions |
| $\ce{BF3}$ | Trigonal planar | Three equal $\ce{B-F}$ dipoles at 120° — three equal carriers around a round table |
| $\ce{CCl4}$ | Tetrahedral | Four equal $\ce{C-Cl}$ dipoles at 109.5° — four equal carriers, four symmetric corners |
| $\ce{SO3}$ | Trigonal planar | Three equal $\ce{S=O}$ dipoles at 120° (resonance makes all three bonds identical) |

**Polar** (a lone pair bends the shape, or the outer atoms differ):

| Molecule | Shape | Why the dipoles don't cancel |
|---|---|---|
| $\ce{H2O}$ | Bent (104.5°) | Both $\ce{O-H}$ dipoles point toward O from the same side — they add |
| $\ce{SO2}$ | Bent (~119°) | Lone pair on S bends the molecule; the two $\ce{S=O}$ dipoles have a net resultant |
| $\ce{NH3}$ | Trigonal pyramidal | All three $\ce{N-H}$ dipoles point up toward N; the lone pair caps the pyramid |
| $\ce{CHCl3}$ | Tetrahedral (asymmetric) | Three strong $\ce{C-Cl}$ pulls vs. one weak $\ce{C-H}$ — the table tilts toward the chlorines |
| $\ce{CH3Cl}$ | Tetrahedral (asymmetric) | One strong $\ce{C-Cl}$ pull unopposed by the three near-nonpolar $\ce{C-H}$ bonds |

**Nonpolar because the bonds themselves are (nearly) nonpolar:**

| Molecule | Why |
|---|---|
| $\ce{N2}$, $\ce{O2}$, $\ce{Cl2}$ | Identical atoms — zero electronegativity difference, no pulls at all |
| $\ce{CH4}$ | $\ce{C-H}$ bonds nearly nonpolar *and* perfectly tetrahedral — nonpolar twice over |

**The "symmetric substitution" shortcut** — for tetrahedral carbons, if all four outer atoms match ($\ce{CCl4}$, $\ce{CH4}$, $\ce{CF4}$), the molecule is nonpolar; mix them ($\ce{CH3Cl}$, $\ce{CH2Cl2}$, $\ce{CHCl3}$) and it's polar. This shortcut is fast and almost always right, but it has a famous trap: **the same set of atoms can be arranged symmetrically or asymmetrically.** In 1,2-dichloroethene ($\ce{ClHC=CHCl}$), the *trans* isomer puts the two chlorines on opposite sides of the rigid double bond — dipoles cancel, nonpolar — while the *cis* isomer puts them on the same side — dipoles add, polar. Same formula, opposite verdicts. (Why can't the molecule just rotate to fix this? Hold that thought — the $\pi$-bond section answers it.)

### Why Polarity Matters (a one-paragraph trailer)

Polarity is the property that decides how molecules *treat each other*. Polar molecules attract other polar molecules (their $\delta^+$ ends snuggle up to neighbors' $\delta^-$ ends), which is why polar substances tend to have higher boiling points than similar nonpolar ones, why water — small, bent, fiercely polar — dissolves salts and sugars and is called the universal solvent, and why oil (nonpolar) and water refuse to mix. "Like dissolves like" is really "similar polarity dissolves similar polarity." All of Unit 3 — intermolecular forces, boiling points, solubility, chromatography — is built directly on the polarity verdicts you learn to make in this article. This is the single most important forward link in the course.

### Part 2: Hybridization — Mixing the Stock Inks

Here's the puzzle Lewis structures skate past. Carbon's ground-state valence configuration is $2s^2\,2p^2$: one filled spherical $s$ orbital and two half-filled dumbbell $p$ orbitals at 90° to each other. If carbon bonded with those raw orbitals, methane's bonds would come in two different flavors at weird angles. But experiment is stubborn: **all four bonds in $\ce{CH4}$ are identical**, at 109.5°.

The resolution is **hybridization**: when an atom bonds, its valence $s$ and $p$ orbitals mathematically **mix into a new set of identical hybrid orbitals**, one hybrid per electron domain. Dad's printer, exactly: don't bond with the stock cartridges — blend them into the custom color the molecule needs. Three recipes, and the AP exam tests **only these three** ($sp^3d$ and $sp^3d^2$ were removed from the AP curriculum — never invoke them):

| Electron domains | Recipe (inks mixed) | Hybridization | Hybrids made | Leftover $p$ orbitals | Domain geometry |
|---|---|---|---|---|---|
| 2 | one $s$ + one $p$ | $sp$ | 2 (at 180°) | **2** | Linear |
| 3 | one $s$ + two $p$ | $sp^2$ | 3 (at 120°) | **1** | Trigonal planar |
| 4 | one $s$ + three $p$ | $sp^3$ | 4 (at 109.5°) | 0 | Tetrahedral |

The bookkeeping is beautiful: **orbitals in = orbitals out.** Mix 4 stock orbitals, get 4 hybrids ($sp^3$). Mix 3, get 3 hybrids plus one untouched $p$ ($sp^2$). Mix 2, get 2 hybrids plus two untouched $p$'s ($sp$). The exponents just record how many $p$ orbitals went into the blend.

And the method for assigning hybridization is one sentence long:

$$\boxed{\text{Count electron domains (from VSEPR)} \;\longrightarrow\; 2 = sp,\quad 3 = sp^2,\quad 4 = sp^3}$$

Two crucial fine points:

1. **Lone pairs occupy hybrid orbitals too.** The oxygen in $\ce{H2O}$ has 4 domains (2 bonds + 2 lone pairs) → $sp^3$, even though it only makes two bonds. Nitrogen in $\ce{NH3}$: 4 domains → $sp^3$. Count *domains*, not bonds.
2. **A double or triple bond is ONE domain** — the same rule as VSEPR. The carbon in $\ce{CO2}$ has 2 domains → $sp$, even though it makes four total bonds.

### Sigma and Pi Bonds

Hybrids explain single bonds. But what *is* a double bond, physically? Two different kinds of orbital overlap:

- A **sigma ($\sigma$) bond** is head-on overlap of two orbitals along the line between the nuclei — usually hybrid-to-hybrid. Every bond's first connection is a $\sigma$ bond. Strong, and the atoms can spin freely around it, like a rod.
- A **pi ($\pi$) bond** is side-by-side overlap of two **unhybridized $p$ orbitals** — the leftover stock inks. The electron density sits *above and below* the bond axis, not on it.

That gives the counting rule you'll use constantly:

$$\text{Single bond} = 1\sigma \qquad \text{Double bond} = 1\sigma + 1\pi \qquad \text{Triple bond} = 1\sigma + 2\pi$$

Check the ink bookkeeping against ethene, $\ce{H2C=CH2}$: each carbon has 3 domains → $sp^2$ → three hybrids for its three $\sigma$ bonds (two to H, one to the other C), leaving **one unhybridized $p$ orbital** sticking straight up. The two leftover $p$'s on the two carbons overlap side-by-side above and below the molecule — that's the $\pi$ bond, and that's the double bond's second stripe. Ethyne, $\ce{HC#CH}$: each carbon $sp$, **two** leftover $p$'s each, forming **two** $\pi$ bonds — the triple bond. The recipe always balances: the number of $\pi$ bonds an atom can form equals the number of stock $p$ orbitals it didn't mix.

**Why $\pi$ bonds forbid rotation.** A $\sigma$ bond is a rod — spin one end and the head-on overlap doesn't care. But a $\pi$ bond is two parallel $p$ orbitals overlapping side-by-side: twist one carbon 90° and the $p$ orbitals go perpendicular, the overlap vanishes, and the $\pi$ bond breaks. Rotating around a double bond costs a full bond's worth of energy, so at ordinary temperatures it simply doesn't happen. That rigidity is exactly why *cis*- and *trans*-1,2-dichloroethene are two genuinely different, separable molecules with different polarities — the double bond locks the chlorines in place.

### The Capstone Pipeline

Everything in Unit 2 is one assembly line, and the AP loves to run a single molecule down the whole line in one FRQ:

$$\text{Formula} \to \text{Lewis structure} \to \text{Resonance check} \to \text{Geometry} \to \text{Polarity} \to \text{Hybridization} \to \sigma/\pi \text{ count}$$

We'll run formaldehyde ($\ce{CH2O}$) through the entire pipeline as the final worked example. If you can do that unprompted, you are done with Unit 2.

---

## Worked Examples

### Example 1: The Classic Trap — $\ce{CO2}$

**Problem:** Is $\ce{CO2}$ polar or nonpolar? Justify with both bond polarity and geometry.

**Solution:**

**Step 1 — Q1: Are the bonds polar?** O (EN ≈ 3.5) vs. C (EN ≈ 2.5): yes, each $\ce{C=O}$ bond is quite polar, with the dipole pointing toward oxygen.

**Step 2 — Q2: Do they cancel?** Carbon has 2 electron domains (each double bond = one domain), no lone pairs → **linear**, 180°. The two equal dipoles point in exactly opposite directions — two equally strong carriers lifting opposite ends of a bench. Perfect cancellation.

**Step 3 — Verdict.** Polar bonds, symmetric arrangement → no net dipole.

**Answer: $\ce{CO2}$ is nonpolar — its two polar $\ce{C=O}$ bond dipoles are equal and opposite in the linear geometry, so they cancel.**

### Example 2: Water Leans — $\ce{H2O}$

**Problem:** Is $\ce{H2O}$ polar or nonpolar? Justify.

**Solution:**

**Step 1 — Q1.** O vs. H: EN difference ≈ 1.2 → each $\ce{O-H}$ bond is strongly polar, dipole toward O.

**Step 2 — Q2.** Oxygen has 4 domains (2 bonding + 2 lone pairs) → **bent**, ≈ 104.5°. Both $\ce{O-H}$ dipoles point up toward oxygen *from the same side* — two carriers standing on the same side of the table. They add, they don't cancel.

**Step 3 — Verdict.** Net dipole pointing from between the H's toward the O.

**Answer: $\ce{H2O}$ is polar — the bent geometry (from the two lone pairs) prevents the two polar $\ce{O-H}$ dipoles from canceling.**

### Example 3: Swap One Carrier — $\ce{CCl4}$ vs. $\ce{CHCl3}$

**Problem:** Both molecules are tetrahedral. Explain why $\ce{CCl4}$ is nonpolar but $\ce{CHCl3}$ is polar.

**Solution:**

**Step 1 — $\ce{CCl4}$.** Four polar $\ce{C-Cl}$ bonds, all identical, arranged in a perfect tetrahedron: four equally strong carriers at four symmetric corners. Every pull is balanced by the others → the table stays level. **Nonpolar.**

**Step 2 — $\ce{CHCl3}$.** Replace one $\ce{Cl}$ with $\ce{H}$. The $\ce{C-H}$ bond is nearly nonpolar, so one corner now has a much weaker carrier. Three strong $\ce{C-Cl}$ pulls on one side, essentially nothing opposing them → the pulls no longer cancel and there is a net dipole toward the three chlorines.

**Step 3 — The lesson.** Geometry alone doesn't decide polarity — the outer atoms must *also* be identical for cancellation.

**Answer: $\ce{CCl4}$ is nonpolar (equal dipoles cancel in the symmetric tetrahedron); $\ce{CHCl3}$ is polar (replacing one Cl with H breaks the symmetry, leaving a net dipole toward the Cl side).**

### Example 4: Lone Pair Tilts the Table — $\ce{BF3}$ vs. $\ce{NH3}$

**Problem:** Both molecules are $\ce{AX3}$-type formulas with polar bonds. Why is $\ce{BF3}$ nonpolar while $\ce{NH3}$ is polar?

**Solution:**

**Step 1 — Count domains.** B in $\ce{BF3}$: 3 bonding domains, 0 lone pairs → **trigonal planar** (120°, flat). N in $\ce{NH3}$: 3 bonding + 1 lone pair = 4 domains → **trigonal pyramidal**.

**Step 2 — $\ce{BF3}$.** Three equal $\ce{B-F}$ dipoles at perfect 120° in a plane: three equal carriers evenly spaced around a round tabletop. Cancel → **nonpolar**.

**Step 3 — $\ce{NH3}$.** The lone pair pushes the three $\ce{N-H}$ bonds down into a pyramid, so all three dipoles point partially *up* toward N — three carriers all lifting from below the same side. They add → net dipole along the pyramid's axis. **Polar.**

**Answer: $\ce{BF3}$ is nonpolar (flat, symmetric, dipoles cancel); $\ce{NH3}$ is polar (the lone pair makes the shape pyramidal, so the three $\ce{N-H}$ dipoles reinforce instead of canceling).**

### Example 5: Same Atoms, Different Verdicts — $\ce{SO3}$ vs. $\ce{SO2}$

**Problem:** Classify $\ce{SO3}$ and $\ce{SO2}$ as polar or nonpolar.

**Solution:**

**Step 1 — $\ce{SO3}$.** S has 3 bonding domains, 0 lone pairs → trigonal planar. Resonance makes all three $\ce{S-O}$ bonds identical (bond order $\tfrac{4}{3}$), so it's three *equal* dipoles at 120° → cancel. **Nonpolar.**

**Step 2 — $\ce{SO2}$.** S has 2 bonding domains + 1 lone pair = 3 domains → **bent** (~119°). The two $\ce{S-O}$ dipoles sit at an angle on the same side; the lone pair occupies the third corner. The pulls don't cancel. **Polar.**

**Step 3 — The pattern.** One lone pair is all it takes: it removes a carrier from one corner of the round table and everything tilts.

**Answer: $\ce{SO3}$ is nonpolar; $\ce{SO2}$ is polar — the lone pair on sulfur bends $\ce{SO2}$ so its bond dipoles cannot cancel.**

### Example 6: One Strong Pull — $\ce{CH3Cl}$

**Problem:** Is chloromethane, $\ce{CH3Cl}$, polar or nonpolar? Which end is $\delta^-$?

**Solution:**

**Step 1 — Geometry.** C: 4 bonding domains → tetrahedral.

**Step 2 — The pulls.** Three $\ce{C-H}$ bonds are essentially nonpolar; the single $\ce{C-Cl}$ bond is strongly polar, dipole toward Cl. One strong carrier hauling on one corner while the other three barely lift → the table tilts toward Cl.

**Step 3 — Assign the ends.** Net dipole points toward chlorine: Cl end is $\delta^-$, the $\ce{CH3}$ end is $\delta^+$.

**Answer: $\ce{CH3Cl}$ is polar, with the chlorine end partially negative — the lone $\ce{C-Cl}$ dipole has nothing to cancel it.**

### Example 7: Nonpolar Two Different Ways — $\ce{N2}$ and $\ce{CH4}$

**Problem:** Both $\ce{N2}$ and $\ce{CH4}$ are nonpolar. Show that they pass the two-question test at *different* questions.

**Solution:**

**Step 1 — $\ce{N2}$ fails Q1.** Two identical atoms → zero electronegativity difference → the bond itself is nonpolar. Nobody is pulling at all; the test ends at question 1.

**Step 2 — $\ce{CH4}$ passes Q1 barely, fails Q2 decisively.** $\ce{C-H}$ bonds are nearly nonpolar (ΔEN ≈ 0.4), and even those tiny dipoles sit in a perfect tetrahedron with four identical outer atoms → they cancel exactly.

**Step 3 — Why this matters.** On an FRQ, your justification must match the reason: don't say "$\ce{N2}$'s dipoles cancel" (there are no dipoles) and don't say "$\ce{CH4}$ has no polar bonds, period" without noting the symmetry that guarantees cancellation regardless.

**Answer: $\ce{N2}$ is nonpolar because its bond is nonpolar; $\ce{CH4}$ is nonpolar because its (nearly nonpolar) bond dipoles cancel in the symmetric tetrahedral geometry.**

### Example 8: Hybridization Speed Round

**Problem:** Assign the hybridization of the central atom in $\ce{CO2}$, $\ce{BF3}$, $\ce{CH4}$, $\ce{NH3}$, $\ce{H2O}$, and $\ce{SO2}$.

**Solution:**

**Step 1 — One rule.** Count electron domains on the atom (lone pairs count; a multiple bond counts once): 2 → $sp$, 3 → $sp^2$, 4 → $sp^3$.

**Step 2 — Apply it.**

| Molecule | Domains on central atom | Hybridization |
|---|---|---|
| $\ce{CO2}$ | 2 (two double bonds) | $sp$ |
| $\ce{BF3}$ | 3 (three bonds) | $sp^2$ |
| $\ce{CH4}$ | 4 (four bonds) | $sp^3$ |
| $\ce{NH3}$ | 4 (3 bonds + 1 lone pair) | $sp^3$ |
| $\ce{H2O}$ | 4 (2 bonds + 2 lone pairs) | $sp^3$ |
| $\ce{SO2}$ | 3 (2 bonds + 1 lone pair) | $sp^2$ |

**Step 3 — Notice the traps handled.** $\ce{CO2}$'s four total bonds are only 2 domains; $\ce{NH3}$ and $\ce{H2O}$ are $sp^3$ *because lone pairs occupy hybrid orbitals too*.

**Answer: $\ce{CO2}$: $sp$; $\ce{BF3}$: $sp^2$; $\ce{CH4}$: $sp^3$; $\ce{NH3}$: $sp^3$; $\ce{H2O}$: $sp^3$; $\ce{SO2}$: $sp^2$.**

### Example 9: Ethene — Where the Leftover Ink Goes

**Problem:** For ethene, $\ce{H2C=CH2}$: give the hybridization of each carbon, count the $\sigma$ and $\pi$ bonds, and state where the $\pi$ bond physically lives.

**Solution:**

**Step 1 — Hybridization.** Each carbon has 3 domains (two $\ce{C-H}$ bonds + the $\ce{C=C}$ counts once) → $sp^2$, trigonal planar, ~120° angles.

**Step 2 — Count $\sigma$.** Every connection contributes one $\sigma$: four $\ce{C-H}$ + one $\ce{C-C}$ = **5 $\sigma$ bonds**.

**Step 3 — Count $\pi$ and locate it.** The double bond adds **1 $\pi$ bond**. Each $sp^2$ carbon mixed only two of its three $p$ orbitals, leaving one unhybridized $p$ perpendicular to the molecular plane — the leftover stock ink. The two leftover $p$'s overlap side-by-side, putting the $\pi$ electron density above and below the plane.

**Answer: Both carbons are $sp^2$; ethene has 5 $\sigma$ and 1 $\pi$ bond, the $\pi$ bond formed by side-by-side overlap of the unhybridized $p$ orbitals.**

### Example 10: Ethyne — Two Stripes of Leftover Ink

**Problem:** For ethyne (acetylene), $\ce{HC#CH}$: hybridization of each carbon, $\sigma/\pi$ count, and the shape of the molecule.

**Solution:**

**Step 1 — Hybridization.** Each carbon: 2 domains (one $\ce{C-H}$, one $\ce{C#C}$ counted once) → $sp$, linear, 180°. The whole molecule is a straight line: $\ce{H-C#C-H}$.

**Step 2 — $\sigma$ count.** Two $\ce{C-H}$ + one $\ce{C-C}$ = **3 $\sigma$**.

**Step 3 — $\pi$ count.** The triple bond = $1\sigma + 2\pi$ → **2 $\pi$ bonds**. Bookkeeping check: each $sp$ carbon left **two** $p$ orbitals unmixed, and those two pairs of leftover $p$'s form the two perpendicular $\pi$ bonds wrapped around the axis.

**Answer: Both carbons are $sp$; ethyne is linear with 3 $\sigma$ and 2 $\pi$ bonds.**

### Example 11: Every Atom in Acetic Acid — $\ce{CH3COOH}$

**Problem:** Vinegar's active molecule is acetic acid. Its skeleton: a $\ce{CH3}$ carbon bonded to a second carbon, which has a double bond to one oxygen and a single bond to an $\ce{-OH}$ oxygen. Assign the hybridization of both carbons and both oxygens, then count all $\sigma$ and $\pi$ bonds.

**Solution:**

**Step 1 — The $\ce{CH3}$ carbon.** Four single bonds (3 H + 1 C) = 4 domains → $sp^3$.

**Step 2 — The carboxyl carbon.** Three connections (C, =O, –OH), the double bond counting once = 3 domains → $sp^2$. This end of the molecule is flat.

**Step 3 — The oxygens.** The double-bonded O: 1 bonding domain + 2 lone pairs = 3 domains → $sp^2$. The $\ce{-OH}$ oxygen: 2 bonds + 2 lone pairs = 4 domains → $sp^3$ (bent at that O, just like water). Lone pairs count!

**Step 4 — $\sigma/\pi$ census.** Connections: 3 $\ce{C-H}$, 1 $\ce{C-C}$, 1 $\ce{C=O}$, 1 $\ce{C-O}$, 1 $\ce{O-H}$ = 7 connections → **7 $\sigma$**. Only the $\ce{C=O}$ contributes a $\pi$ → **1 $\pi$**.

**Answer: $\ce{CH3}$ carbon $sp^3$; carboxyl carbon $sp^2$; carbonyl O $sp^2$; hydroxyl O $sp^3$; total 7 $\sigma$ and 1 $\pi$.**

### Example 12: The Full Pipeline — Formaldehyde, $\ce{CH2O}$

**Problem:** Run the complete Unit 2 pipeline on formaldehyde: Lewis structure → resonance → geometry → polarity → hybridization → $\sigma/\pi$ count.

**Solution:**

**Step 1 — Valence electron count.** C(4) + 2×H(1) + O(6) = **12 electrons** (6 pairs).

**Step 2 — Lewis structure.** C central (least electronegative, and H can't be central). Skeleton $\ce{H-C-H}$ with O attached uses 3 pairs; putting the remaining 3 pairs on O leaves carbon with only 6 electrons → promote one O lone pair into a $\ce{C=O}$ double bond. Final: C bonded to two H's and double-bonded to O, with 2 lone pairs on O. Formal charges all zero. ✓

**Step 3 — Resonance check.** Is there another placement of the double bond that keeps formal charges reasonable? No — $\ce{C=H}$ makes no sense and there's only one O. **One structure, no resonance.**

**Step 4 — Geometry.** C has 3 domains (H, H, =O), no lone pairs → **trigonal planar**, bond angles ≈ 120°.

**Step 5 — Polarity.** Q1: the $\ce{C=O}$ bond is strongly polar (toward O); $\ce{C-H}$ nearly nonpolar. Q2: one strong pull toward O with nothing opposite to cancel it — one strong carrier on a three-person table. **Polar**, with the O end $\delta^-$.

**Step 6 — Hybridization.** 3 domains on C → $sp^2$ (O, with 3 domains, is also $sp^2$).

**Step 7 — $\sigma/\pi$ count.** Connections: 2 $\ce{C-H}$ + 1 $\ce{C-O}$ = **3 $\sigma$**; the double bond adds **1 $\pi$**, living in the unhybridized $p$ orbitals of C and O.

**Answer: $\ce{CH2O}$ — one Lewis structure (no resonance), trigonal planar, polar (net dipole toward O), $sp^2$ carbon, 3 $\sigma$ + 1 $\pi$.** This seven-step chain *is* the Unit 2 FRQ. Practice it until it's automatic.

---

## Common Mistakes

| The Mistake | Why It Happens | The Fix |
|---|---|---|
| "It has polar bonds, so the molecule is polar" | Skipping Q2 entirely | Polar bonds are necessary but not sufficient — $\ce{CO2}$, $\ce{CCl4}$, $\ce{BF3}$, $\ce{SO3}$ all have polar bonds and are nonpolar. Always check cancellation |
| Judging polarity from the formula without drawing the shape | $\ce{CO2}$ and $\ce{H2O}$ are both $\ce{AX2}$-looking triatomics | One is linear, one is bent — you cannot answer Q2 without the VSEPR geometry. Draw first |
| Forgetting that lone pairs break symmetry | Lone pairs are invisible in the molecular formula | $\ce{SO2}$ vs. $\ce{SO3}$, $\ce{NH3}$ vs. $\ce{BF3}$: one lone pair flips the verdict. Count domains from the Lewis structure |
| Assigning hybridization from a memorized molecule list | It works until an unfamiliar molecule appears | Count electron domains, always: 2 = $sp$, 3 = $sp^2$, 4 = $sp^3$ |
| Counting a double bond as two domains | Confusing bonds with domains | A multiple bond is ONE electron domain — for geometry *and* hybridization. $\ce{CO2}$'s carbon: 2 domains, $sp$ |
| Forgetting lone pairs occupy hybrid orbitals | "Only bonds hybridize" feels intuitive | O in $\ce{H2O}$ is $sp^3$ (2 bonds + 2 lone pairs). The lone pairs sit *in* hybrid orbitals |
| Writing $sp^3d$ or $sp^3d^2$ | Older textbooks and videos still teach them | AP removed them. Five- and six-domain species exist, but the AP exam will not ask you to hybridize them |
| "A double bond = 2 $\pi$ bonds" | Mixing up the total count with the $\pi$ count | Double = $1\sigma + 1\pi$; triple = $1\sigma + 2\pi$. The *first* bond of any connection is always $\sigma$ |
| Polarity justification that names only electronegativity, or only shape | Half the argument feels like enough | Full credit needs BOTH: "the bonds are polar AND the geometry prevents the dipoles from canceling" |

---

## AP Exam Tips

1. **Polarity justifications need both halves, every time.** The scoring guidelines consistently require (a) identification of polar bonds via electronegativity difference and (b) a geometry statement about whether the dipoles cancel. The magic sentence: *"The molecule contains polar bonds, and because of its [bent/pyramidal/asymmetric] geometry the bond dipoles do not cancel, giving a net dipole."* For nonpolar: *"...the symmetric [linear/trigonal planar/tetrahedral] geometry causes the equal bond dipoles to cancel."*
2. **Hybridization comes from the domain count — show that reasoning.** "The carbon has three electron domains, so it is $sp^2$ hybridized" earns the point. A bare "$sp^2$" with no justification may not, on an explain-style FRQ.
3. **AP tests only $sp$, $sp^2$, $sp^3$.** The College Board removed $sp^3d$ and $sp^3d^2$ from the curriculum. If your answer invokes $d$-orbital hybridization, you've left the AP universe — stop and recount.
4. **Lone pairs occupy hybrid orbitals.** Expect a multiple-choice question where the trap answer assigns $sp^2$ to water's oxygen (counting only the two bonds). Domains, not bonds: $\ce{H2O}$'s O is $sp^3$.
5. **The $\sigma/\pi$ fast facts are free points.** Single = $1\sigma$; double = $1\sigma+1\pi$; triple = $1\sigma+2\pi$; the number of $\sigma$ bonds = the number of connections in the skeleton. Counting questions should take 20 seconds.
6. **Know the "pi bonds prevent rotation" sentence.** It shows up as an explain question: *rotation about a double bond would require breaking the side-by-side $p$-orbital overlap of the $\pi$ bond, which costs too much energy* — that's why cis and trans isomers are distinct.
7. **The pipeline is the Unit 2 FRQ.** A single molecule → draw the Lewis structure, identify resonance, name the geometry and angle, judge polarity, assign hybridization, count $\sigma/\pi$. Time yourself running strangers like $\ce{HCN}$, $\ce{CH3OH}$, or $\ce{CH2O}$ down the whole line in under five minutes.

---

## Practice Problems

### Problem 1

$\ce{CF4}$ contains four extremely polar $\ce{C-F}$ bonds (ΔEN ≈ 1.5, among the most polar bonds there are). Is the molecule polar or nonpolar? Justify fully.

<details>
<summary><strong>Solution</strong></summary>

Q1: yes, each $\ce{C-F}$ bond is strongly polar, dipole toward F.

Q2: carbon has 4 bonding domains, no lone pairs → tetrahedral, and all four outer atoms are identical. Four equal carriers at four symmetric corners — every pull cancels.

Bond polarity alone never decides the verdict; symmetry gets the final vote.

**$\ce{CF4}$ is nonpolar: its four equal $\ce{C-F}$ dipoles cancel in the symmetric tetrahedral geometry.**

</details>

### Problem 2

Write a full-credit AP justification for why $\ce{SO2}$ is a polar molecule.

<details>
<summary><strong>Solution</strong></summary>

Both halves must appear:

1. **Bond polarity:** oxygen is more electronegative than sulfur, so each $\ce{S-O}$ bond is polar with the bond dipole pointing toward O.
2. **Geometry:** sulfur has three electron domains (two bonding + one lone pair), giving a bent molecular geometry. Because of the bent shape, the two bond dipoles do not point in opposite directions and do not cancel.

**$\ce{SO2}$ is polar: it has polar $\ce{S-O}$ bonds, and its bent geometry (caused by the lone pair on S) prevents the bond dipoles from canceling, leaving a net dipole.**

</details>

### Problem 3

$\ce{CO2}$ is nonpolar, but $\ce{OCS}$ (carbon bonded to one O and one S, linear) is polar. Explain the difference.

<details>
<summary><strong>Solution</strong></summary>

Both molecules are linear with two double bonds on carbon. In $\ce{CO2}$ the two dipoles are *equal* and opposite → cancel.

In $\ce{OCS}$ the two ends differ: O is more electronegative than S, so the $\ce{C=O}$ dipole is stronger than the $\ce{C=S}$ dipole. Two carriers lifting opposite ends of a bench, but one is much stronger — the bench tilts toward the stronger carrier's side.

Cancellation needs symmetric directions AND equal pulls; $\ce{OCS}$ has the directions but not the equality.

**$\ce{OCS}$ is polar with the net dipole toward oxygen, because its two opposing bond dipoles are unequal.**

</details>

### Problem 4

Dichloromethane, $\ce{CH2Cl2}$, is tetrahedral around carbon. Polar or nonpolar?

<details>
<summary><strong>Solution</strong></summary>

Q1: the two $\ce{C-Cl}$ bonds are strongly polar; the two $\ce{C-H}$ bonds are nearly nonpolar.

Q2: tetrahedral shape, but the four outer atoms are NOT identical. In a tetrahedron, any two corners sit 109.5° apart — the two $\ce{C-Cl}$ dipoles always have a net resultant pointing between the chlorines, and the H's contribute almost nothing to oppose it. Two strong carriers bunched on one side of the table.

(Trap check: unlike a flat square, a tetrahedron has no way to place the two Cl's "opposite" each other — every arrangement of $\ce{CH2Cl2}$ is the same molecule, and it's asymmetric.)

**$\ce{CH2Cl2}$ is polar — the two $\ce{C-Cl}$ dipoles cannot cancel in the tetrahedral arrangement.**

</details>

### Problem 5

Assign the hybridization of the carbon atom in each: (a) $\ce{CH4}$, (b) $\ce{CO2}$, (c) $\ce{CH2O}$.

<details>
<summary><strong>Solution</strong></summary>

Count domains on carbon:

(a) $\ce{CH4}$: four single bonds = 4 domains → **$sp^3$**

(b) $\ce{CO2}$: two double bonds, each counting once = 2 domains → **$sp$**

(c) $\ce{CH2O}$: two C–H bonds + one C=O (counts once) = 3 domains → **$sp^2$**

**(a) $sp^3$, (b) $sp$, (c) $sp^2$** — total bonds don't matter; domains do.

</details>

### Problem 6

Assign the hybridization of the nitrogen atom in (a) $\ce{NH3}$ and (b) $\ce{HCN}$.

<details>
<summary><strong>Solution</strong></summary>

(a) $\ce{NH3}$: N has 3 bonds + 1 lone pair = 4 domains → **$sp^3$**. The lone pair occupies one of the four hybrid orbitals.

(b) $\ce{HCN}$ ($\ce{H-C#N}$): N has 1 triple bond (one domain) + 1 lone pair = 2 domains → **$sp$**. The lone pair points straight out along the axis in the second $sp$ hybrid.

**(a) $sp^3$; (b) $sp$.** Lone pairs count as domains and live in hybrid orbitals.

</details>

### Problem 7

Count the $\sigma$ and $\pi$ bonds in ethene, $\ce{H2C=CH2}$, and in propene, $\ce{CH3-CH=CH2}$.

<details>
<summary><strong>Solution</strong></summary>

Rule: every connection = 1 $\sigma$; each extra stripe of a multiple bond = 1 $\pi$.

**Ethene:** connections = 4 C–H + 1 C–C = 5 → 5 $\sigma$; one double bond → 1 $\pi$.

**Propene:** connections = 6 C–H + 2 C–C = 8 → 8 $\sigma$; one double bond → 1 $\pi$.

**Ethene: 5 $\sigma$, 1 $\pi$. Propene: 8 $\sigma$, 1 $\pi$.**

</details>

### Problem 8

Acetonitrile, $\ce{CH3CN}$, has the skeleton $\ce{H3C-C#N}$. Give the hybridization of each carbon and the nitrogen, and count all $\sigma$ and $\pi$ bonds.

<details>
<summary><strong>Solution</strong></summary>

- $\ce{CH3}$ carbon: 4 single bonds = 4 domains → $sp^3$
- Nitrile carbon: 1 single bond + 1 triple bond = 2 domains → $sp$
- N: 1 triple bond + 1 lone pair = 2 domains → $sp$

Bond census: 3 C–H + 1 C–C + 1 C–N connection = **5 $\sigma$**; the triple bond adds **2 $\pi$**.

**$\ce{CH3}$ carbon $sp^3$; nitrile carbon $sp$; nitrogen $sp$; 5 $\sigma$ and 2 $\pi$ bonds.**

</details>

### Problem 9

Explain, in terms of orbital overlap, why there is essentially free rotation around the $\ce{C-C}$ bond in ethane but not around the $\ce{C=C}$ bond in ethene.

<details>
<summary><strong>Solution</strong></summary>

Ethane's C–C bond is a single $\sigma$ bond: head-on overlap along the internuclear axis. Rotating one $\ce{CH3}$ group spins the bond like a rod around its own axis — the head-on overlap is unchanged, so rotation is nearly free.

Ethene's double bond includes a $\pi$ bond: side-by-side overlap of the two unhybridized $p$ orbitals, which must stay parallel. Twisting one $\ce{CH2}$ group 90° turns the $p$ orbitals perpendicular to each other, destroying the overlap — i.e., breaking the $\pi$ bond, which costs roughly a bond's worth of energy.

**Rotation about a $\sigma$ bond preserves its head-on overlap; rotation about a double bond would break the side-by-side $p$-orbital overlap of the $\pi$ bond, so the double bond is locked.**

</details>

### Problem 10

Run the full Unit 2 pipeline on $\ce{HCN}$: Lewis structure, resonance check, geometry, polarity, hybridization of C, and $\sigma/\pi$ count.

<details>
<summary><strong>Solution</strong></summary>

**Valence electrons:** 1 + 4 + 5 = 10 (5 pairs).

**Lewis:** skeleton $\ce{H-C-N}$ (C central). Two bonds use 2 pairs; giving N the remaining 3 pairs leaves C with 4 electrons → promote two N lone pairs: $\ce{H-C#N}$ with one lone pair on N. Formal charges all zero. ✓

**Resonance:** no equivalent alternative placement — one structure.

**Geometry:** C has 2 domains (H, and the triple bond counted once) → linear, 180°.

**Polarity:** the $\ce{C#N}$ bond is strongly polar toward N; the $\ce{C-H}$ bond is nearly nonpolar. One strong pull toward N, nothing canceling it → polar, N end $\delta^-$.

**Hybridization:** 2 domains on C → $sp$.

**$\sigma/\pi$:** 2 connections (H–C, C–N) = 2 $\sigma$; triple bond adds 2 $\pi$.

**$\ce{HCN}$: one Lewis structure, linear, polar (dipole toward N), $sp$ carbon, 2 $\sigma$ + 2 $\pi$.**

</details>

### Problem 11

Methanol, $\ce{CH3OH}$, is the simplest alcohol. Assign the hybridization of the carbon and the oxygen, count the $\sigma$ and $\pi$ bonds, and state whether the molecule is polar.

<details>
<summary><strong>Solution</strong></summary>

**Carbon:** 4 single bonds (3 H + O) = 4 domains → $sp^3$.

**Oxygen:** 2 bonds (C, H) + 2 lone pairs = 4 domains → $sp^3$; the molecule is bent at the O, like water wearing a $\ce{CH3}$ hat.

**Bond census:** 3 C–H + 1 C–O + 1 O–H = 5 connections → 5 $\sigma$, 0 $\pi$ (all single bonds).

**Polarity:** the $\ce{C-O}$ and especially $\ce{O-H}$ bonds are strongly polar, and the bent arrangement at oxygen means the dipoles can't cancel → polar (this is why methanol mixes with water in all proportions).

**C: $sp^3$; O: $sp^3$; 5 $\sigma$ and 0 $\pi$; the molecule is polar.**

</details>

### Problem 12

1,2-dichloroethene, $\ce{ClHC=CHCl}$, exists as two distinct molecules: one polar, one nonpolar. Explain how the same formula gives both verdicts, and why the two forms don't interconvert at room temperature.

<details>
<summary><strong>Solution</strong></summary>

Each carbon is $sp^2$ (3 domains) and the molecule is flat. The two chlorines can sit on the **same side** of the double bond (*cis*) or on **opposite sides** (*trans*).

- *Trans:* the two $\ce{C-Cl}$ dipoles point in opposite directions and cancel → **nonpolar**.
- *Cis:* both dipoles point toward the same side → they add → **polar**. Two carriers on the same side of the table.

They don't interconvert because switching sides requires rotating around the $\ce{C=C}$ bond, which would break the $\pi$ bond's side-by-side $p$-orbital overlap — far too costly at room temperature.

**Trans is nonpolar, cis is polar, and the rigid $\pi$ bond locks each isomer in place.** (This is the trap in the "identical outer atoms → nonpolar" shortcut: the *arrangement* matters, not just the inventory of atoms.)

</details>

### Problem 13

From this list, identify every nonpolar molecule: $\ce{CO2}$, $\ce{H2O}$, $\ce{BF3}$, $\ce{NH3}$, $\ce{CCl4}$, $\ce{CH3Cl}$, $\ce{N2}$.

<details>
<summary><strong>Solution</strong></summary>

Run the two-question test on each:

| Molecule | Shape | Verdict | Reason |
|---|---|---|---|
| $\ce{CO2}$ | Linear | **Nonpolar** | Equal opposite dipoles cancel |
| $\ce{H2O}$ | Bent | Polar | Dipoles add on the same side |
| $\ce{BF3}$ | Trigonal planar | **Nonpolar** | Three equal dipoles at 120° cancel |
| $\ce{NH3}$ | Trigonal pyramidal | Polar | Lone pair → dipoles reinforce upward |
| $\ce{CCl4}$ | Tetrahedral | **Nonpolar** | Four equal dipoles cancel |
| $\ce{CH3Cl}$ | Tetrahedral (asym.) | Polar | One unopposed $\ce{C-Cl}$ pull |
| $\ce{N2}$ | Linear | **Nonpolar** | The bond itself is nonpolar |

**Nonpolar: $\ce{CO2}$, $\ce{BF3}$, $\ce{CCl4}$, and $\ce{N2}$.**

</details>

### Problem 14

A student writes: "The oxygen in water is $sp^2$ hybridized because it forms two bonds and $2 \approx 3$ domains, and $\ce{CO2}$'s carbon is $sp^3$ because it forms four bonds." Find and fix both errors, stating the rule each one violates.

<details>
<summary><strong>Solution</strong></summary>

**Error 1 — water's oxygen.** Hybridization counts *electron domains*, and lone pairs are domains that occupy hybrid orbitals. O in $\ce{H2O}$ has 2 bonding domains + 2 lone pairs = 4 domains → **$sp^3$**, not $sp^2$. Rule violated: *lone pairs occupy hybrid orbitals too.*

**Error 2 — $\ce{CO2}$'s carbon.** Hybridization counts domains, not total bonds, and a multiple bond is ONE domain. C in $\ce{CO2}$ has two double bonds = 2 domains → **$sp$**, not $sp^3$. Rule violated: *a double or triple bond counts as a single electron domain.*

**Corrected: O in $\ce{H2O}$ is $sp^3$; C in $\ce{CO2}$ is $sp$. Count domains (lone pairs included, multiple bonds once) — never raw bonds.**

</details>

---

## Quick Reference

**The two-question polarity test**

| Question | Source | Tool |
|---|---|---|
| Q1: Are the bonds polar? | Electronegativity difference (0401) | ΔEN > ~0.4 → polar bond; identical atoms → nonpolar bond |
| Q2: Do the dipoles cancel? | Molecular geometry (0406) | Symmetric shape (linear/trig planar/tetrahedral, no lone pairs) + identical outer atoms → cancel |

**The polarity gallery**

| Nonpolar (dipoles cancel) | Polar (dipoles don't cancel) |
|---|---|
| $\ce{CO2}$, $\ce{BF3}$, $\ce{CCl4}$, $\ce{SO3}$, $\ce{CH4}$, $\ce{N2}$ | $\ce{H2O}$, $\ce{SO2}$, $\ce{NH3}$, $\ce{CHCl3}$, $\ce{CH3Cl}$, $\ce{HCN}$, $\ce{CH2O}$ |

**Hybridization from domains (AP tests only these three)**

| Domains | Hybridization | Angle | Leftover $p$ orbitals | Max $\pi$ bonds |
|---|---|---|---|---|
| 2 | $sp$ | 180° | 2 | 2 |
| 3 | $sp^2$ | 120° | 1 | 1 |
| 4 | $sp^3$ | 109.5° | 0 | 0 |

**Sigma and pi**

| Bond | Composition | Rotation? |
|---|---|---|
| Single | $1\sigma$ | Free |
| Double | $1\sigma + 1\pi$ | Locked |
| Triple | $1\sigma + 2\pi$ | Locked |

**The Unit 2 pipeline:** formula → Lewis → resonance check → geometry → polarity → hybridization → $\sigma/\pi$ count.

---

<div align="center">

[← VSEPR and Molecular Geometry](/chemistry/0406-vsepr-molecular-geometry) | [Intermolecular Forces →](/chemistry/0501-intermolecular-forces)

</div>
