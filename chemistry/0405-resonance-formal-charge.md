# Resonance and Formal Charge
<p class="article-date">July 4, 2026</p>

*Saturday morning smoothie run with my friends, and I'm watching the guy behind the counter drop strawberries and a banana into the blender. Here's the thing nobody ever worries about: the drink that comes out is not going to flicker back and forth — strawberry! banana! strawberry! — like a haunted milkshake. It's one steady, in-between drink that is neither pure strawberry nor pure banana, and it's *both* the whole time. Hold that thought, because it is the single most-tested idea in this topic: when a molecule has more than one valid Lewis structure, the real molecule is the smoothie — one permanent blend — not a movie alternating between frames. Then the bill came, six of us, one receipt, and we had to split it fairly: everyone pays for what they personally ate, shared appetizers split down the middle. That's formal charge — chemistry's bill-splitting algorithm — and it's how you decide which Lewis structure is the "fairest" picture of a molecule. Together, resonance and formal charge finish the Lewis-structure story from last article and set up everything about molecular shape and reactivity in the rest of Unit 2.*

---

## What You'll Learn

- Recognize the "where do I put the double bond?" moment that signals resonance, and draw all resonance structures for species like $\ce{O3}$, $\ce{NO2-}$, $\ce{NO3-}$, and $\ce{CO3^2-}$
- Explain what resonance actually *means* — one delocalized hybrid, never a molecule flipping between structures — in AP-scoring language
- Use experimental bond lengths (all equal, in between single and double) as *evidence* for resonance in data-based questions
- Compute fractional bond orders like $\frac{4}{3}$ for $\ce{NO3-}$ and $\frac{3}{2}$ for $\ce{O3}$ using bonding pairs ÷ positions
- Rank bond lengths across species ($\ce{NO+}$ vs. $\ce{NO2-}$ vs. $\ce{NO3-}$) using bond order
- Calculate formal charge for every atom in a structure with $\text{FC} = \text{valence} - \text{nonbonding} - \frac{1}{2}(\text{bonding})$, and verify with the sum check
- Use the fast mental version — FC = valence − dots − sticks — under exam time pressure
- Pick the best Lewis structure using formal charge: charges near zero, negatives on the most electronegative atom (the $\ce{OCN-}$ classic)
- Tell formal charge apart from oxidation state — two different bookkeeping systems that AP loves to cross-examine

---

## Prerequisites

- [Lewis Structures](/chemistry/0404-lewis-structures) — you need the full drawing algorithm cold: count valence electrons, build the skeleton, place lone pairs, promote to multiple bonds. Resonance is what happens when that algorithm gives more than one right answer
- [Bond Energy and Length](/chemistry/0402-bond-energy-and-length) — bond order is the dial: higher order → shorter, stronger bond. Resonance turns that dial to fractions like $\frac{4}{3}$

---

## The Core Concept

### Intuition First

Back to the blender, because this analogy has to do real work.

**The two fruits = the individual Lewis structures.** For ozone, $\ce{O3}$, the drawing algorithm forces you to put one double bond somewhere — and there are two equally valid places for it: left or right. Neither drawing is wrong. Neither drawing is the molecule.

**The smoothie = the real molecule.** Blend strawberry and banana and you get one steady drink that tastes like *both at once* — not a drink that alternates flavors. Real $\ce{O3}$ has two identical bonds, each halfway between a single and a double bond, all the time. The molecule never "switches." There is nothing to switch between. The two drawings are our limitation (Lewis dots can only show whole bonds), not the molecule's behavior.

**Blending = delocalization.** In the smoothie, you can't point to "the strawberry part" anymore — it's spread through the whole cup. In ozone, you can't point to "the double bond" anymore — that extra pair of electrons is spread (*delocalized*) over both bonding positions.

**And the bill-split?** When the drawing algorithm gives you *several different-looking* candidate structures (not just mirror images), you need a referee to pick the best one. Formal charge is that referee: charge every atom for the electrons it personally used, compare to what it walked in with, and prefer the structure where nobody's tab is wildly unfair. We'll get there — resonance first.

### When One Lewis Structure Isn't Enough

Run the [Lewis Structures](/chemistry/0404-lewis-structures) algorithm on ozone, $\ce{O3}$: $3 \times 6 = 18$ valence electrons, bent chain skeleton $\ce{O-O-O}$, distribute lone pairs, and the central atom comes up short — you must promote one lone pair into a double bond. But *which side?*

```
   O=O–O:          :O–O=O
  (double on       (double on
    the left)        the right)
```

That "where do I put the double bond?" moment is the signal. Both structures are legal: same atom skeleton, same 18 electrons, every atom with an octet. When two or more valid Lewis structures differ **only in the placement of electrons** (not atoms!), they are called **resonance structures**, and chemists connect them with a **double-headed arrow** ($\leftrightarrow$) inside square brackets:

$$\left[\; \ce{O=O-O} \;\leftrightarrow\; \ce{O-O=O} \;\right]^{\vphantom{1}}$$

Three rules govern every set of resonance structures:

1. **Only electrons move.** The atom skeleton is frozen. If you moved an atom, you drew a different molecule (an *isomer*), not a resonance structure.
2. **Same total electron count** in every structure — same charge, same number of dots and sticks overall.
3. **Every structure must be valid on its own** — octets satisfied (duet for H), electrons all accounted for.

**Warning about that arrow:** the double-headed arrow $\leftrightarrow$ does **not** mean the molecule goes back and forth. It is not an equilibrium arrow ($\ce{<=>}$) and not a reaction arrow ($\ce{->}$). It means "these drawings are partial views of one real thing." Strawberry photo $\leftrightarrow$ banana photo, one smoothie.

The same moment happens in:

- $\ce{NO2-}$ — 18 electrons, one double bond, two equivalent N–O positions → **2 resonance structures**
- $\ce{NO3-}$ — 24 electrons, one double bond, three equivalent positions → **3 resonance structures**
- $\ce{CO3^2-}$ — 24 electrons, one double bond, three equivalent positions → **3 resonance structures**

**The benzene cameo.** The most famous resonance molecule in chemistry is benzene, $\ce{C6H6}$ — a six-carbon ring where the drawing algorithm demands three double bonds, alternating around the ring, and there are two ways to alternate them. The real molecule is the blend: six *identical* C–C bonds of 139 pm each, squarely between a C–C single bond (154 pm) and a C=C double bond (134 pm). Chemists literally draw benzene as a hexagon with a circle inside — the circle *is* the smoothie, six delocalized electrons smeared evenly around the ring. You won't draw benzene's structures on the AP exam, but it's the poster child for everything in this article.

### What Resonance Means: The Hybrid

The real molecule is called the **resonance hybrid** — the blend of all the resonance structures. Get these statements exam-ready:

- The electrons that "moved" between drawings are **delocalized**: spread over several positions instead of pinned between two atoms.
- The molecule exists as **one structure at all times** — the hybrid. It does **not** alternate, flip, oscillate, or "resonate back and forth" between the drawn structures. (Yes, "resonance" is a terrible name. Blame history, not the molecule.)
- Every equivalent bond in the hybrid is **identical**: same length, same strength, in between a pure single and a pure double bond.

And here is the beautiful part — the molecule itself testifies. If ozone really flickered between $\ce{O=O-O}$ and $\ce{O-O=O}$, careful measurement would catch one short bond and one long bond. Instead:

| Species | Measured bonds | Single-bond length | Double-bond length |
|---|---|---|---|
| $\ce{O3}$ | **both 128 pm — identical** | $\ce{O-O}$: 148 pm | $\ce{O=O}$: 121 pm |
| $\ce{NO3-}$ | **all three ≈ 124 pm — identical** | $\ce{N-O}$: ~136 pm | $\ce{N=O}$: ~120 pm |
| $\ce{CO3^2-}$ | **all three 129 pm — identical** | $\ce{C-O}$: 143 pm | $\ce{C=O}$: 123 pm |
| $\ce{C6H6}$ | **all six 139 pm — identical** | $\ce{C-C}$: 154 pm | $\ce{C=C}$: 134 pm |

Every bond equal, every bond *in between* single and double. That is exactly what a blend predicts and exactly what a flickering movie would fail to explain. When an AP question hands you a bond-length data table, "all bonds are equal in length, intermediate between single and double bond lengths, consistent with resonance/delocalized electrons" is the scoring sentence.

### Fractional Bond Order

From [Bond Energy and Length](/chemistry/0402-bond-energy-and-length): bond order counts shared pairs (single = 1, double = 2, triple = 3), and higher order means shorter and stronger. Resonance hybrids have **fractional** bond orders, and there's a clean recipe:

$$\text{bond order} = \frac{\text{total bonding pairs spread over the equivalent positions}}{\text{number of equivalent positions}}$$

Count the sticks in any *one* resonance structure, divide by the number of bonding positions:

| Species | Bonding pairs in one structure | Positions | Bond order |
|---|---|---|---|
| $\ce{O3}$ | $2 + 1 = 3$ | 2 | $\frac{3}{2} = 1.5$ |
| $\ce{NO2-}$ | $2 + 1 = 3$ | 2 | $\frac{3}{2} = 1.5$ |
| $\ce{NO3-}$ | $2 + 1 + 1 = 4$ | 3 | $\frac{4}{3} \approx 1.33$ |
| $\ce{CO3^2-}$ | $2 + 1 + 1 = 4$ | 3 | $\frac{4}{3} \approx 1.33$ |
| $\ce{C6H6}$ (ring bonds) | $3(2) + 3(1) = 9$ | 6 | $\frac{9}{6} = 1.5$ |

The smoothie again: 3 "cups of bond" poured evenly into 2 glasses gives 1.5 cups per glass. And bond order 1.5 predicts a length *between* single and double — which is precisely what the table above measured. Theory and experiment shake hands.

**Bond-length ranking with resonance** is now a two-step move: compute each species' bond order, then apply "higher order → shorter." Compare the N–O bond in three ions:

- $\ce{NO+}$: 10 valence electrons → triple bond, order **3**
- $\ce{NO2-}$: order $\frac{3}{2}$ = **1.5**
- $\ce{NO3-}$: order $\frac{4}{3}$ ≈ **1.33**

Shortest to longest: $\ce{NO+} < \ce{NO2-} < \ce{NO3-}$. This exact comparison family is an AP favorite — see Worked Example 8.

### Formal Charge: Splitting the Bill

Now the second half of the story. Sometimes the drawing algorithm produces candidate structures that are *not* equivalent mirror images — genuinely different pictures, like "$\ce{CO2}$ with two double bonds" versus "$\ce{CO2}$ with a triple and a single." Both satisfy octets. Which one is the molecule? We need the bill-split.

Six friends, one receipt. The fair split: each person pays for **everything they ordered just for themselves, plus half of every dish they shared**. Then compare what each person *owes* to the cash they *walked in with*. Atoms work the same way:

- **Lone-pair electrons** = dishes you ordered for yourself. You're charged for all of them.
- **Bonding electrons** = shared appetizers. Split every bond 50/50 — one electron of each bonding pair to each atom.
- **Valence electrons** = the cash you brought (the free atom's valence count).

$$\text{Formal charge} = (\text{valence } e^-) \;-\; (\text{nonbonding } e^-) \;-\; \frac{1}{2}(\text{bonding } e^-)$$

And the speed-run version you should actually use on the exam, since every bond stick is one electron of your share:

$$\boxed{\text{FC} = \text{valence} - \text{dots} - \text{sticks}}$$

where *dots* = lone-pair electrons on the atom (count individual dots) and *sticks* = number of bonds touching the atom (count a double bond as 2 sticks, a triple as 3).

Read the sign like a dinner tab: **FC = 0** means you used exactly what you brought — a perfectly fair split. **FC = −1** means the structure assigns you one electron *more* than you brought — you came out ahead on the deal. **FC = +1** means you got shorted by one. If dinner was \$120 for six people, the fair-split instinct says everyone should land near \$20 — nobody should quietly get stuck paying \$45 while someone else pays \$5. Structures feel the same way about charge.

**The sum check (always do this):** the formal charges in any structure must add up to the species' overall charge. For a neutral molecule, they sum to 0; for $\ce{CO3^2-}$, they sum to −2; for $\ce{NO3-}$, to −1. The receipt has to total the bill. If your formal charges don't sum correctly, you miscounted — go back.

### Using Formal Charge to Pick the Best Structure

When candidate structures compete, rank them with three guidelines, in order:

1. **Smallest charges win.** The best structure has formal charges as close to zero as possible (fairest split).
2. **Negative charges belong on the most electronegative atom.** If *someone* must end up ahead on electrons, it should be the atom that hogs electrons anyway. (At dinner: if the split can't be perfectly even, let the minus land on the friend who ordered the expensive stuff.)
3. **Avoid large charges and same-sign charges on adjacent atoms.** A structure with +2 next to +1 is fighting itself.

**The classic: cyanate, $\ce{OCN-}$** (16 electrons, skeleton O–C–N). Three octet-satisfying structures exist, and formal charge cleanly ranks them — Worked Example 9 does the full arithmetic. Spoiler: the winner puts the −1 on oxygen, the most electronegative atom in the ion. Its sulfur cousin thiocyanate, $\ce{SCN-}$, plays the same game with a twist: there the most electronegative atom is *nitrogen* ($\ce{N}$ ≈ 3.0 vs. $\ce{S}$ ≈ 2.6), so the minus prefers N. Same referee, different roster.

**$\ce{CO2}$:** the symmetric $\ce{O=C=O}$ structure gives every atom FC = 0 — a perfect split. The alternative with a triple bond on one side gives one oxygen +1 and the other −1. A *positive* formal charge on oxygen — the second-most electronegative element — is the bill-split equivalent of charging the friend who only had water for the steak. The symmetric structure dominates.

**The $\ce{SO4^2-}$ asterisk.** Some textbooks draw sulfate with two S=O double bonds so that sulfur's formal charge drops from +2 to 0, giving sulfur an "expanded octet" of 12 electrons. Here's the deal for the AP exam: **the College Board accepts — and current evidence supports — the all-single-bond structure that obeys the octet rule** (S at +2, each O at −1, sum = −2 ✓). Modern calculations show the S–O bonds are highly polar single-ish bonds, not true doubles, and sulfur's d-orbitals don't meaningfully participate. If a question hands you the expanded-octet version, you can work with it, but you will never lose points for the octet-obeying structure. Know both exist, draw the octet one, and don't die on this hill.

### Formal Charge vs. Oxidation State (Don't Mix the Ledgers)

One clarifying paragraph, because AP loves to cross-examine this. Formal charge and **oxidation state** are two *different bookkeeping systems* applied to the same molecule. Formal charge splits every shared bond **50/50** — the fair dinner split. Oxidation state is winner-take-all: it hands **both** electrons of every bond to the more electronegative atom, as if bonds were fully ionic. Same molecule, different rules, different numbers: in $\ce{CO2}$, carbon's formal charge is 0 but its oxidation state is +4, because oxygen "takes everything" in the oxidation-state ledger. Neither number is the atom's real charge — both are accounting fictions with different jobs. Formal charge's job is judging Lewis structures (this article). Oxidation state's job is tracking electron transfer in redox reactions — the full treatment arrives in Unit 4, where that winner-take-all ledger becomes the whole game.

---

## Worked Examples

### Example 1: The Two Faces of Ozone

**Problem:** Draw all resonance structures of $\ce{O3}$ and determine the O–O bond order in the real molecule.

**Solution:**

**Step 1 — Electron count.** $3 \times 6 = 18$ valence electrons.

**Step 2 — Skeleton and octets.** Chain $\ce{O-O-O}$ uses 4 electrons; placing lone pairs leaves the central O one pair short of an octet, so promote one terminal lone pair into a double bond. Two equally valid choices:

$$\left[\;\ce{O=O-O} \;\leftrightarrow\; \ce{O-O=O}\;\right]$$

(Left structure: the double-bonded O carries 2 lone pairs, central O carries 1, single-bonded O carries 3.)

**Step 3 — Bond order.** One structure holds $2 + 1 = 3$ bonding pairs spread over 2 equivalent positions:

$$\text{bond order} = \frac{3}{2} = 1.5$$

**Answer: Two resonance structures; each O–O bond in the hybrid has order 1.5 — both bonds identical, between single and double.**

### Example 2: Nitrate's Three Frames

**Problem:** Draw the resonance structures of $\ce{NO3-}$ and compute the N–O bond order.

**Solution:**

**Step 1 — Electron count.** $5 + 3(6) + 1 = 24$ valence electrons.

**Step 2 — Skeleton.** N central, three O around it: 3 bonds (6 e⁻), then 18 e⁻ as lone pairs fills each O — but N has only 6 electrons. Promote one O lone pair to a double bond. Three equivalent choices → **three resonance structures**, one per N=O position, connected by $\leftrightarrow$ in brackets.

**Step 3 — Bond order.** Each structure: $2 + 1 + 1 = 4$ bonding pairs over 3 positions:

$$\text{bond order} = \frac{4}{3} \approx 1.33$$

**Answer: Three resonance structures; every N–O bond is identical with order $\frac{4}{3}$ — slightly more than a single bond, and all three measured lengths agree at ~124 pm.**

### Example 3: Carbonate, Nitrate's Twin

**Problem:** How many resonance structures does $\ce{CO3^2-}$ have, and how do its C–O bond lengths compare to a C–O single bond (143 pm) and a C=O double bond (123 pm)?

**Solution:**

**Step 1.** $4 + 3(6) + 2 = 24$ valence electrons — same count, same layout as nitrate: one C=O double bond, two C–O single bonds, **three resonance structures**.

**Step 2.** Bond order $= \frac{4}{3}$, so the hybrid's bonds should be equal to each other and closer to single than double.

**Step 3.** Experiment: all three C–O bonds measure **129 pm** — identical, and sitting between 143 pm and 123 pm (a bit nearer the single, matching order 1.33).

**Answer: Three resonance structures; all three C–O bonds are identical at 129 pm, intermediate between single and double — direct evidence for the delocalized hybrid.**

### Example 4: Nitrite in Two Strokes

**Problem:** Draw the resonance structures of $\ce{NO2-}$ and find the bond order.

**Solution:**

**Step 1.** $5 + 2(6) + 1 = 18$ valence electrons.

**Step 2.** Bent skeleton $\ce{O-N-O}$; after lone pairs, N needs one more pair → one N=O double bond, placeable on either side:

$$\left[\;\ce{O=N-O} \;\leftrightarrow\; \ce{O-N=O}\;\right]^{-}$$

(N keeps one lone pair in both structures.)

**Step 3.** $\frac{2+1}{2} = \frac{3}{2}$.

**Answer: Two resonance structures; both N–O bonds identical with bond order 1.5.**

### Example 5: Splitting Ozone's Bill (Formal Charge on Every Atom)

**Problem:** Assign a formal charge to each oxygen in one resonance structure of $\ce{O3}$ ($\ce{O_a=O_b-O_c}$) and verify the sum check.

**Solution:** Use FC = valence − dots − sticks. Oxygen brings 6 valence electrons everywhere.

**Step 1 — $\ce{O_a}$** (double-bonded end): 2 lone pairs = 4 dots; double bond = 2 sticks.
$$\text{FC} = 6 - 4 - 2 = 0$$

**Step 2 — $\ce{O_b}$** (center): 1 lone pair = 2 dots; one double + one single = 3 sticks.
$$\text{FC} = 6 - 2 - 3 = +1$$

**Step 3 — $\ce{O_c}$** (single-bonded end): 3 lone pairs = 6 dots; 1 stick.
$$\text{FC} = 6 - 6 - 1 = -1$$

**Step 4 — Sum check.** $0 + 1 + (-1) = 0$ = overall charge of neutral $\ce{O3}$. ✓

**Answer: FC = 0 (double-bonded O), +1 (central O), −1 (single-bonded O); sum = 0.** Fun fact: even "best" structures sometimes can't avoid charges — ozone's bill never splits perfectly.

### Example 6: Nitrate's Receipt

**Problem:** Compute the formal charge on every atom in one resonance structure of $\ce{NO3-}$ and confirm the total.

**Solution:**

**Step 1 — N** (0 lone pairs; one double + two singles = 4 sticks):
$$\text{FC} = 5 - 0 - 4 = +1$$

**Step 2 — the double-bonded O** (4 dots, 2 sticks):
$$\text{FC} = 6 - 4 - 2 = 0$$

**Step 3 — each single-bonded O** (6 dots, 1 stick):
$$\text{FC} = 6 - 6 - 1 = -1 \quad (\times 2)$$

**Step 4 — Sum check.** $+1 + 0 + (-1) + (-1) = -1$ = the ion's charge. ✓

**Answer: N = +1, double-bonded O = 0, each single-bonded O = −1; total = −1.**

### Example 7: The 20-Second Version (Dots and Sticks on Carbonate)

**Problem:** Under time pressure, find all formal charges in one structure of $\ce{CO3^2-}$.

**Solution:** No half-counting — dots and sticks only.

**Step 1 — C:** 4 valence, 0 dots, 4 sticks (one double + two singles) → $4 - 0 - 4 = \mathbf{0}$.

**Step 2 — double-bonded O:** 6 valence, 4 dots, 2 sticks → $6 - 4 - 2 = \mathbf{0}$.

**Step 3 — each single-bonded O:** 6 valence, 6 dots, 1 stick → $6 - 6 - 1 = \mathbf{-1}$.

**Step 4 — Sum:** $0 + 0 - 1 - 1 = -2$. ✓ Matches $\ce{CO3^2-}$.

**Answer: C = 0, double-bonded O = 0, single-bonded Os = −1 each.** Total time: about as long as it took to read this.

### Example 8: Ranking N–O Bond Lengths

**Problem:** Rank the N–O bond length in $\ce{NO+}$, $\ce{NO2-}$, and $\ce{NO3-}$ from shortest to longest. Justify with bond order.

**Solution:**

**Step 1 — $\ce{NO+}$.** $5 + 6 - 1 = 10$ valence electrons — same count as $\ce{N2}$, so a triple bond: bond order **3**.

**Step 2 — $\ce{NO2-}$.** From Example 4: bond order $\frac{3}{2}$ = **1.5**.

**Step 3 — $\ce{NO3-}$.** From Example 2: bond order $\frac{4}{3}$ ≈ **1.33**.

**Step 4 — Apply the dial.** Higher bond order → more shared electron density pulling the nuclei together → shorter bond:

$$\ce{NO+} \;(3) \;<\; \ce{NO2-} \;(1.5) \;<\; \ce{NO3-} \;(1.33)$$

**Answer: $\ce{NO+}$ shortest, then $\ce{NO2-}$, then $\ce{NO3-}$ longest — bond order decreases left to right, so length increases.**

### Example 9: The Cyanate Classic — Formal Charge Picks a Winner

**Problem:** The cyanate ion, $\ce{OCN-}$ (skeleton O–C–N), has three Lewis structures that satisfy every octet. Use formal charge to rank them.

**Solution:** 16 valence electrons ($6 + 4 + 5 + 1$). The three octet-complete structures and their FC bills:

**Structure A: $\ce{O#C-N}$** (triple to O, single to N; O has 1 lone pair, N has 3)
- O: $6 - 2 - 3 = +1$  |  C: $4 - 0 - 4 = 0$  |  N: $5 - 6 - 1 = -2$
- Charges: $+1, 0, -2$. Sum $= -1$ ✓ — but big charges, and a *plus* on oxygen. Terrible split.

**Structure B: $\ce{O=C=N}$** (two doubles; O and N each have 2 lone pairs)
- O: $6 - 4 - 2 = 0$  |  C: $4 - 0 - 4 = 0$  |  N: $5 - 4 - 2 = -1$
- Charges: $0, 0, -1$. Sum $= -1$ ✓ — small charges, minus on N.

**Structure C: $\ce{O-C#N}$** (single to O, triple to N; O has 3 lone pairs, N has 1)
- O: $6 - 6 - 1 = -1$  |  C: $4 - 0 - 4 = 0$  |  N: $5 - 2 - 3 = 0$
- Charges: $-1, 0, 0$. Sum $= -1$ ✓ — small charges, minus on **O, the most electronegative atom**.

**Ranking:** C is best (minimal charges *and* the −1 sits on oxygen), B is a close second and still contributes to the hybrid, A is a minor bit player.

**Answer: $\ce{O-C#N^-}$ is the best structure — smallest formal charges with the negative charge on the most electronegative atom. Structure A (+1 on O, −2 on N) is the worst.**

For thiocyanate $\ce{SCN-}$, rerun the same logic with N as the most electronegative atom — the best structure parks the −1 on nitrogen. (Practice Problem 10.)

### Example 10: Why $\ce{CO2}$ Isn't Drawn with a Triple Bond

**Problem:** Both $\ce{O=C=O}$ and $\ce{O#C-O}$ satisfy all octets with 16 electrons. Show with formal charge why the symmetric structure dominates.

**Solution:**

**Step 1 — Symmetric structure $\ce{O=C=O}$.** Each O: $6 - 4 - 2 = 0$. C: $4 - 0 - 4 = 0$. All zeros — a perfect bill split.

**Step 2 — Triple-single structure $\ce{O#C-O}$.** Triple-bonded O: $6 - 2 - 3 = +1$. C: $4 - 0 - 4 = 0$. Single-bonded O: $6 - 6 - 1 = -1$. Sum $= 0$ ✓, but it saddles one oxygen with +1.

**Step 3 — Judge.** Rule 1: all-zero beats $\pm 1$. Rule 2: a positive charge on oxygen — nearly the most electronegative element there is — is exactly backwards. Both experiments agree: $\ce{CO2}$'s two bonds are identical at 116 pm.

**Answer: $\ce{O=C=O}$ (all formal charges zero) is overwhelmingly the best structure; the triple-bond version is a negligible contributor.**

### Example 11: Sulfate and the Octet-Rule Peace Treaty

**Problem:** Compute the formal charges in the all-single-bond Lewis structure of $\ce{SO4^2-}$ and explain why AP accepts this structure even though some textbooks draw double bonds.

**Solution:**

**Step 1 — Electron count.** $6 + 4(6) + 2 = 32$: four S–O single bonds (8 e⁻) plus 3 lone pairs on each O (24 e⁻). Every atom has an octet.

**Step 2 — Formal charges.**
- S: $6 - 0 - 4 = +2$
- Each O: $6 - 6 - 1 = -1$

**Step 3 — Sum check.** $+2 + 4(-1) = -2$. ✓

**Step 4 — The textbook fight.** Drawing two S=O double bonds lowers S to 0 and two O's to 0 — a "better" bill split — but it gives sulfur 12 electrons (an expanded octet). Modern computational work says sulfur's d-orbitals don't really participate and the octet structure is the more honest picture. **AP's stance: the octet-obeying, all-single-bond structure is fully accepted; you will never be penalized for it.**

**Answer: S = +2, each O = −1, sum = −2. Draw the octet version on the exam and move on.**

### Example 12: Resonance or Not?

**Problem:** Which of these species require resonance structures: $\ce{CO2}$, $\ce{SO2}$, $\ce{CCl4}$, $\ce{CO3^2-}$?

**Solution:**

**Step 1 — $\ce{CO2}$.** Best structure $\ce{O=C=O}$ is symmetric with all FC = 0 — there is no "where do I put it?" ambiguity worth blending. **No resonance needed.**

**Step 2 — $\ce{SO2}$.** 18 electrons, bent $\ce{O-S-O}$, one double bond with two equivalent homes — ozone's exact situation. **Resonance: 2 structures, bond order 1.5.**

**Step 3 — $\ce{CCl4}$.** Four identical single bonds, all octets, no multiple bonds to relocate. **No resonance.**

**Step 4 — $\ce{CO3^2-}$.** One double bond, three equivalent positions. **Resonance: 3 structures.**

**Answer: $\ce{SO2}$ and $\ce{CO3^2-}$ require resonance; $\ce{CO2}$ and $\ce{CCl4}$ do not.** The tell: a multiple bond (or lone pair) with more than one equivalent place to live.

---

## Common Mistakes

| The mistake | Why it happens | How to avoid it |
|---|---|---|
| Saying the molecule "switches" or "alternates" between resonance structures | The word "resonance" and the $\leftrightarrow$ arrow both *sound* like motion | The molecule is ONE permanent hybrid — the smoothie, not a flickering movie. Writing "alternates" on an FRQ loses the point |
| Moving *atoms* between "resonance structures" | Confusing resonance with isomers | Resonance structures share one frozen skeleton; only electrons (lone pairs and multiple bonds) relocate |
| Using $\ce{<=>}$ (equilibrium) instead of $\leftrightarrow$ | The arrows look similar | Equilibrium is two real species interconverting; resonance is multiple drawings of one species |
| Forgetting the sum check | Rushing the arithmetic | Formal charges MUST total the overall charge ($-1$ for $\ce{NO3-}$, $-2$ for $\ce{CO3^2-}$, 0 for neutrals). Ten seconds, catches most errors |
| Counting a double bond as 1 stick in FC = valence − dots − sticks | Thinking "one bond = one stick" | Sticks = bonding *lines* touching the atom: double = 2, triple = 3 |
| Putting the negative formal charge on the *least* electronegative atom and calling it "best" | Applying rule 1 (small charges) but forgetting rule 2 | Tie-breaker: minus signs go to the electron hog — the most electronegative atom ($\ce{OCN-}$ → O; $\ce{SCN-}$ → N) |
| Treating formal charge as the atom's real charge | The name says "charge" | It's bookkeeping under a 50/50 rule. The real charge is smeared by delocalization; FC just referees structures |
| Confusing formal charge with oxidation state | Both are per-atom numbers | FC splits bonds 50/50; oxidation state gives both electrons to the more electronegative atom. C in $\ce{CO2}$: FC 0, oxidation state +4 |
| Averaging wrong for bond order | Dividing by structures instead of positions | Bond order = bonding pairs in ONE structure ÷ number of equivalent *positions* ($\ce{NO3-}$: $4/3$, not $4/2$ or $3/3$) |

---

## AP Exam Tips

- **"Does NOT alternate" is a scored sentence.** FRQs ask why all bonds in $\ce{NO3-}$ or $\ce{CO3^2-}$ are the same length. Full credit requires the hybrid idea: *"the actual structure is a resonance hybrid; the bonding electrons are delocalized over all three N–O positions, so all bonds are identical with a bond order of 4/3."* Any phrasing that implies flipping between structures ("the double bond moves around") can cost the point.
- **Equal bond lengths = evidence.** Data-based questions hand you measured lengths and ask what they support. The template: *all X–Y bonds are equal in length AND intermediate between the known single- and double-bond lengths, consistent with resonance (delocalized electrons)*. Cite both halves — equal *and* intermediate.
- **Formal charge under time pressure:** FC = valence − dots − sticks. No fractions, no ½ × anything — the sticks already are your half-share of the bonding electrons. Then run the sum check (total FC = overall charge) before moving on; it's the fastest error detector on the exam.
- **Best-structure justifications need both rules:** (1) formal charges closest to zero, (2) negative formal charge on the most electronegative atom. The $\ce{OCN-}$/$\ce{SCN-}$ family is the classic vehicle — know it cold.
- **Bond-order ranking questions** ($\ce{NO+}$ vs. $\ce{NO2-}$ vs. $\ce{NO3-}$ style) want the chain: count electrons → draw/recall structures → compute (fractional) bond order → higher order = shorter, stronger bond. Show the bond orders explicitly.
- **Sulfate and friends:** if you're asked to draw $\ce{SO4^2-}$, $\ce{PO4^3-}$, or $\ce{ClO4-}$, the octet-rule structure with single bonds is always accepted. Don't burn time optimizing formal charge into an expanded octet.
- **No calculator needed anywhere in this topic** — it's all integer arithmetic and justification sentences. The points are in the words, not the numbers.

---

## Practice Problems

### Problem 1

Draw (or describe) all resonance structures of $\ce{SO2}$ and determine the S–O bond order in the hybrid.

<details>
<summary><strong>Solution</strong></summary>

Valence electrons: $6 + 2(6) = 18$. Bent skeleton $\ce{O-S-O}$; sulfur needs one more pair, so promote a lone pair to form one S=O double bond — two equivalent choices:

$$\left[\;\ce{O=S-O} \;\leftrightarrow\; \ce{O-S=O}\;\right]$$

(S keeps one lone pair in each structure.) Bond order $= \frac{2+1}{2} = \frac{3}{2}$.

**Answer: Two resonance structures; both S–O bonds identical with bond order 1.5.**

</details>

### Problem 2

Predict which has the longer N–O bonds: $\ce{NO2-}$ or $\ce{NO3-}$. Justify with bond orders.

<details>
<summary><strong>Solution</strong></summary>

$\ce{NO2-}$: 3 bonding pairs over 2 positions → order $\frac{3}{2} = 1.5$.

$\ce{NO3-}$: 4 bonding pairs over 3 positions → order $\frac{4}{3} \approx 1.33$.

Lower bond order → longer bond.

**Answer: $\ce{NO3-}$ has the longer N–O bonds (order 1.33 < 1.5).**

</details>

### Problem 3

Carbon monoxide's best Lewis structure is $\ce{:C#O:}$. Compute the formal charge on each atom and run the sum check. What's odd about the result?

<details>
<summary><strong>Solution</strong></summary>

C: $4 - 2 - 3 = -1$. O: $6 - 2 - 3 = +1$. Sum: $-1 + 1 = 0$ ✓ (neutral molecule).

The oddity: the *negative* charge sits on carbon, the **less** electronegative atom — and the alternatives are worse (the double-bond structure leaves C with only 6 electrons). $\ce{CO}$ is the famous case where you can't have everything: the octet rule wins, and the imperfect bill split stands.

**Answer: FC(C) = −1, FC(O) = +1, sum = 0. The best available structure still puts − on the less electronegative atom.**

</details>

### Problem 4

The formate ion, $\ce{HCO2-}$, has the skeleton H–C with two O's on carbon. Describe its resonance structures and find the C–O bond order.

<details>
<summary><strong>Solution</strong></summary>

Valence electrons: $1 + 4 + 2(6) + 1 = 18$. Carbon bonds to H, one O by a double bond, the other O by a single bond — and the double bond has two equivalent homes → **two resonance structures**.

C–O bond order $= \frac{2+1}{2} = \frac{3}{2} = 1.5$. (The C–H bond isn't part of the resonance.)

**Answer: Two resonance structures; both C–O bonds identical with order 1.5 — and experiment confirms two equal C–O lengths.**

</details>

### Problem 5

Without drawing anything new, state what the formal charges in any valid structure of $\ce{CO3^2-}$ must sum to, then verify using the structure's charges from the article.

<details>
<summary><strong>Solution</strong></summary>

The sum must equal the overall charge: **−2**.

From Worked Example 7: C = 0, double-bonded O = 0, each single-bonded O = −1. Sum: $0 + 0 + (-1) + (-1) = -2$ ✓.

**Answer: Total formal charge = −2, matching the 2− charge of carbonate.**

</details>

### Problem 6

Dinitrogen monoxide, $\ce{N2O}$, has the skeleton N–N–O. Two octet-complete structures are $\ce{N#N-O}$ and $\ce{N=N=O}$. Use formal charge to decide which is the better contributor.

<details>
<summary><strong>Solution</strong></summary>

16 valence electrons ($5 + 5 + 6$).

**$\ce{N#N-O}$:** terminal N: $5 - 2 - 3 = 0$; central N: $5 - 0 - 4 = +1$; O: $6 - 6 - 1 = -1$. Charges $0, +1, -1$; sum 0 ✓.

**$\ce{N=N=O}$:** terminal N: $5 - 4 - 2 = -1$; central N: $5 - 0 - 4 = +1$; O: $6 - 4 - 2 = 0$. Charges $-1, +1, 0$; sum 0 ✓.

Both have the same charge magnitudes, so the tie-breaker is electronegativity: the −1 should sit on O (3.4), not N (3.0).

**Answer: $\ce{N#N-O}$ (−1 on oxygen) is the better contributor.**

</details>

### Problem 7

Rank the C–O bond length, shortest to longest: $\ce{CO}$, $\ce{CO2}$, $\ce{CO3^2-}$, $\ce{CH3OH}$ (methanol's C–O is a pure single bond).

<details>
<summary><strong>Solution</strong></summary>

Bond orders: $\ce{CO}$ triple → 3; $\ce{CO2}$ double → 2; $\ce{CO3^2-}$ resonance → $\frac{4}{3} \approx 1.33$; $\ce{CH3OH}$ single → 1.

Higher order → shorter:

$$\ce{CO} < \ce{CO2} < \ce{CO3^2-} < \ce{CH3OH}$$

**Answer: $\ce{CO}$ (shortest, order 3) < $\ce{CO2}$ (2) < $\ce{CO3^2-}$ (4/3) < $\ce{CH3OH}$ (1, longest).**

</details>

### Problem 8

Benzene's C–C bonds all measure 139 pm, while a normal C–C single bond is 154 pm and a C=C double bond is 134 pm. Explain these data in one or two exam-ready sentences.

<details>
<summary><strong>Solution</strong></summary>

Benzene is a resonance hybrid of two structures with alternating double bonds; the six extra bonding electrons are delocalized evenly around the ring. Each C–C bond therefore has order $\frac{9}{6} = 1.5$, so all six bonds are identical, with a length intermediate between single (154 pm) and double (134 pm) — exactly the 139 pm observed.

**Answer: Equal, intermediate bond lengths are evidence of a delocalized resonance hybrid with C–C bond order 1.5 — not alternating single and double bonds.**

</details>

### Problem 9

A classmate writes: "In $\ce{NO3-}$, the double bond rapidly jumps between the three N–O positions, so on average each bond acts like $\frac{4}{3}$ of a bond." Grade this answer: what's right, and what would lose the point on an FRQ?

<details>
<summary><strong>Solution</strong></summary>

**Right:** the $\frac{4}{3}$ bond order and the idea that all three positions share the double-bond character.

**Wrong (and point-losing):** "rapidly jumps." The molecule does **not** alternate between resonance structures — there is no motion to average. The ion exists as a single, permanent hybrid in which the bonding electrons are *delocalized* over all three positions simultaneously. Smoothie, not a flickering movie.

**Answer: Correct bond order, incorrect mechanism — replace "the double bond jumps" with "the electrons are delocalized over all three equivalent positions in one static hybrid."**

</details>

### Problem 10

Thiocyanate, $\ce{SCN-}$ (skeleton S–C–N), has three octet-complete structures: $\ce{S#C-N}$, $\ce{S=C=N}$, and $\ce{S-C#N}$. Assign formal charges to all atoms in each and identify the best structure. (Electronegativities: S ≈ 2.6, N ≈ 3.0.)

<details>
<summary><strong>Solution</strong></summary>

16 valence electrons ($6 + 4 + 5 + 1$). Carbon is $4 - 0 - 4 = 0$ in all three.

**$\ce{S#C-N}$:** S: $6 - 2 - 3 = +1$; N: $5 - 6 - 1 = -2$. Charges $+1, 0, -2$ — big charges, worst.

**$\ce{S=C=N}$:** S: $6 - 4 - 2 = 0$; N: $5 - 4 - 2 = -1$. Charges $0, 0, -1$ with − on N.

**$\ce{S-C#N}$:** S: $6 - 6 - 1 = -1$; N: $5 - 2 - 3 = 0$. Charges $-1, 0, 0$ with − on S.

All sums $= -1$ ✓. The last two tie on magnitude; nitrogen is more electronegative than sulfur, so the −1 belongs on N.

**Answer: $\ce{S=C=N^-}$ (formal charges 0, 0, −1 with the negative on nitrogen, the most electronegative atom) is the best structure; $\ce{S#C-N}$ is the worst.** Note the contrast with $\ce{OCN-}$, where oxygen outranks nitrogen and claims the minus.

</details>

### Problem 11

A student measures the two S–O bonds in gaseous $\ce{SO2}$ and finds both are 143 pm. Reference values: S–O single ≈ 157 pm, S=O double ≈ 143 pm... wait — the measured value *equals* the double-bond reference. Does this disprove resonance in $\ce{SO2}$? What's the stronger AP-safe statement about resonance evidence?

<details>
<summary><strong>Solution</strong></summary>

No. The decisive observation is that **both bonds are identical** — a single frozen structure $\ce{O=S-O}$ would show one short bond and one long bond, which is never observed. Reference "single" and "double" lengths come from *other* molecules and shift with context, so the safest exam claim leads with equality: *the two S–O bonds are experimentally identical, which a single Lewis structure cannot explain; the ion is a resonance hybrid with both bonds equivalent (order 1.5).* When your data do fall neatly between the references (as in $\ce{O3}$: 128 pm between 121 and 148), cite that too.

**Answer: Equal bond lengths are the core evidence for resonance; intermediate length is supporting evidence when the reference values cooperate.**

</details>

### Problem 12

For the octet-obeying structure of $\ce{SO4^2-}$ (four S–O single bonds), compute every formal charge and run the sum check. Then state, in one sentence, AP's position on this structure versus the expanded-octet version.

<details>
<summary><strong>Solution</strong></summary>

S: $6 - 0 - 4 = +2$. Each O: $6 - 6 - 1 = -1$.

Sum check: $+2 + 4(-1) = -2$ ✓ matches the 2− charge.

AP position: the octet-rule structure (all single bonds) is fully accepted and never penalized, even though some textbooks draw two S=O double bonds to shrink the formal charges — the expanded octet is not required and current evidence doesn't support d-orbital bonding in sulfate.

**Answer: FC(S) = +2, FC(O) = −1 each, total −2; draw the octet version on the AP exam with confidence.**

</details>

### Problem 13

For carbon in $\ce{CO2}$, compute (a) the formal charge and (b) the oxidation state, and explain in one sentence why the two numbers differ.

<details>
<summary><strong>Solution</strong></summary>

(a) Formal charge: C has 0 dots and 4 sticks → $4 - 0 - 4 = \mathbf{0}$.

(b) Oxidation state: give **both** electrons of every C–O bond to oxygen (more electronegative). Carbon keeps 0 of its bonding electrons: oxidation state $= 4 - 0 = \mathbf{+4}$.

They differ because the two ledgers split shared electrons differently: formal charge divides every bond 50/50, while oxidation state awards the whole bond to the more electronegative atom.

**Answer: FC = 0, oxidation state = +4 — same atom, two different electron-bookkeeping rules.** (Oxidation states run the show in Unit 4's redox chemistry.)

</details>

### Problem 14

The acetate ion, $\ce{CH3COO-}$, has two C–O bonds on its second carbon, and both measure 126 pm (C–O single: 143 pm; C=O double: 123 pm). Explain the data, give the C–O bond order, and describe the resonance structures.

<details>
<summary><strong>Solution</strong></summary>

Acetate's carboxylate carbon bonds to one O by a double bond and one O by a single bond — with two equivalent ways to assign them → **two resonance structures** (the $\ce{CH3}$ group is a spectator). The real ion is the hybrid: the second bonding pair is delocalized over both C–O positions.

Bond order $= \frac{2+1}{2} = 1.5$, predicting two identical bonds between 143 pm and 123 pm — matching the measured 126 pm for both.

**Answer: Two resonance structures; both C–O bonds identical with order 1.5, and the equal, intermediate 126 pm lengths are direct evidence of the delocalized hybrid.**

</details>

---

## Quick Reference

| Idea | The rule | The one-liner |
|---|---|---|
| Resonance trigger | A multiple bond (or lone pair) with ≥ 2 equivalent homes | "Where do I put the double bond?" |
| Resonance structures | Same skeleton, same electron count, only electrons move; joined by $\leftrightarrow$ | Frames, not phases |
| The hybrid | ONE permanent blend; electrons delocalized | Smoothie, never a flickering movie |
| Evidence | All equivalent bonds equal in length, intermediate between single and double | Equal + in-between = resonance |
| Fractional bond order | (bonding pairs in one structure) ÷ (equivalent positions) | $\ce{NO3-}$: $\frac{4}{3}$; $\ce{O3}$, $\ce{NO2-}$, benzene: $\frac{3}{2}$ |
| Length ranking | Higher bond order → shorter, stronger | $\ce{NO+}(3) < \ce{NO2-}(1.5) < \ce{NO3-}(1.33)$ |
| Formal charge | $\text{FC} = \text{valence} - \text{nonbonding} - \frac{1}{2}(\text{bonding})$ | Fast: valence − dots − sticks |
| Sum check | $\sum \text{FC} =$ overall charge | The receipt must total the bill |
| Best structure | Charges nearest zero; negatives on most electronegative atom | Fairest split wins ($\ce{OCN-}$: − on O; $\ce{SCN-}$: − on N) |
| $\ce{SO4^2-}$ on AP | All-single-bond octet structure (S: +2, O: −1) is always accepted | Don't chase the expanded octet |
| FC vs. oxidation state | FC splits bonds 50/50; oxidation state is winner-take-all to the electronegative atom | C in $\ce{CO2}$: FC 0, ox. state +4 → Unit 4 |

---

<div align="center">

[← Lewis Structures](/chemistry/0404-lewis-structures) | [VSEPR and Molecular Geometry →](/chemistry/0406-vsepr-molecular-geometry)

</div>
