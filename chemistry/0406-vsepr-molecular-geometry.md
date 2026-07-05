# VSEPR and Molecular Geometry
<p class="article-date">July 4, 2026</p>

*Fourth of July party at our house, and Dad put me in charge of balloon decorations. Here's the thing nobody tells you about balloons: tie two of them together at the knot and you don't get to choose how they sit — they instantly point in exactly opposite directions, a perfect straight line. Tie a third one into the same knot and the bundle snaps into a flat Y, each balloon 120° from its neighbors. Add a fourth and something wilder happens: the bundle refuses to stay flat and pops out into 3D, a spiky caltrop shape where every balloon is 109.5° from every other. I didn't arrange any of that — the balloons did it themselves, because each one shoves the others as far away as space allows. Molecules do the exact same thing: the electron groups around a central atom repel each other and spread out to maximum separation, and that one shoving rule predicts the 3D shape of almost any molecule you'll meet in AP Chemistry. This is Topic 2.7, VSEPR — the moment your flat Lewis structures stand up off the page — and it's the key that unlocks polarity, intermolecular forces, and basically all of Unit 3.*

---

## What You'll Learn

- State the single VSEPR principle — electron domains repel to maximum separation — and use it to derive every geometry instead of memorizing blindly
- Count electron domains from a Lewis structure, treating a double or triple bond as **one** domain
- Distinguish **electron-domain geometry** from **molecular geometry**, and explain why AP questions ask for both names
- Predict the geometry and ideal bond angles for any central atom with 2, 3, or 4 electron domains
- Explain, in FRQ-ready language, why lone pairs compress bond angles: $\ce{CH4}$ (109.5°) → $\ce{NH3}$ (107°) → $\ce{H2O}$ (104.5°)
- Run the full pipeline — Lewis structure → count domains → both geometry names → approximate angles — for real molecules and polyatomic ions
- Explain why resonance does **not** change a molecule's geometry
- Describe 3D shapes clearly in words and read wedge-dash drawings
- Recognize the 5- and 6-domain shapes (seesaw, T-shape, square planar) as beyond-the-CED bonus knowledge

---

## Prerequisites

- [Lewis Structures](/chemistry/0404-lewis-structures) — VSEPR starts from a **correct** Lewis structure; if your dot structure is wrong, every prediction after it collapses
- [Resonance and Formal Charge](/chemistry/0405-resonance-formal-charge) — you'll need to trust that equivalent resonance structures describe one real molecule, which is exactly why resonance never changes the geometry

---

## The Core Concept

### Intuition First

Back to the balloon bundle, because every piece of it maps onto the chemistry.

**The knot = the central atom.** Everything is tied to one point. VSEPR is always a question about *one central atom at a time*: what's attached to it, and how does that stuff arrange itself?

**Each balloon = one electron domain.** An **electron domain** (the AP-preferred phrase; you'll also hear "electron group") is one *region* of electron density around the central atom. A single bond is one balloon. A lone pair is one balloon. And here's the trap AP loves: a double bond or triple bond is still just **one balloon** — all those shared electrons live in the same region of space, pointing at the same neighbor atom. Two balloons tied to the same spot on the knot don't count twice; they're one fat balloon.

**The shoving = electron–electron repulsion.** Balloons squish each other because they take up space. Electron domains repel each other because they're all negatively charged. Either way, the bundle settles into the arrangement with **maximum separation**: 2 domains → opposite directions (180°), 3 domains → flat Y (120°), 4 domains → the 3D caltrop (109.5°). That's the entire theory. VSEPR stands for **Valence Shell Electron Pair Repulsion**, but honestly it should stand for "balloons shove."

**The invisible balloon = a lone pair.** Now the twist that makes this topic interesting. Imagine one of the four balloons is painted the exact same color as the wall behind it — invisible in photos. It's still there. It still shoves. In fact, a lone pair is a *fatter* balloon than a bonding pair: bonding electrons are stretched out between two nuclei and held tight, but lone-pair electrons belong to the central atom alone and spread out wide, squishing their neighbors harder.

**The photo = molecular geometry.** When you photograph the bundle, you can only see the visible balloons — so you name the *shape in the photo* using only what shows up. Chemistry does the same: **molecular geometry is named using atoms only**, even though the invisible lone pairs dictated where everything sits. That's why water — which has four domains arranged tetrahedrally — gets photographed as a little bent V. Two of its four balloons are invisible.

Keep this picture running. Every geometry, every squeezed angle, every "explain why" in this article is one of these four mappings.

### The One Principle

> **VSEPR:** Electron domains around a central atom repel one another and arrange themselves as far apart as possible. The 3D shape of the molecule follows from that arrangement.

Counting domains from a Lewis structure:

| Thing attached to the central atom | Domains it counts as |
|---|---|
| Single bond | 1 |
| Double bond | **1** |
| Triple bond | **1** |
| Lone pair on the central atom | 1 |
| Lone pairs on *outer* atoms | **0** — they never count |

Two rules students forget:

1. **A multiple bond is one domain.** $\ce{CO2}$ has two double bonds → 2 domains → linear. It is *not* bent, no matter how many electrons live in those double bonds.
2. **Only the central atom's lone pairs matter.** The three lone pairs on each $\ce{Cl}$ in $\ce{CCl4}$ do nothing to the shape. Only what's tied into *the knot* shoves.

### Two Names for Every Molecule

AP Chemistry uses a two-name system, and questions can ask for either one:

- **Electron-domain geometry** — the arrangement of **all** domains, lone pairs included. This is the balloon bundle itself, invisible balloons and all. Only three answers matter on the AP exam: linear, trigonal planar, tetrahedral.
- **Molecular geometry** — the shape named from **atom positions only**. This is the photograph, where invisible balloons don't show.

If there are no lone pairs on the central atom, the two names are identical. Every lone pair makes the photo differ from the bundle.

Why does AP ask for both? Because the two names test different skills. The electron-domain geometry proves you counted domains correctly; the molecular geometry proves you know lone pairs occupy space but don't get photographed. An answer of "tetrahedral" for the *molecular* geometry of $\ce{NH3}$ is wrong even though its four domains genuinely sit tetrahedrally — the photo shows a tripod, not a caltrop.

### The Complete AP Table (2–4 Domains — Know This Cold)

| Domains | Electron-domain geometry | Lone pairs | Molecular geometry | Bond angle | Example |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 2 | Linear | 0 | **Linear** | 180° | $\ce{CO2}$ |
| 3 | Trigonal planar | 0 | **Trigonal planar** | 120° | $\ce{BF3}$ |
| 3 | Trigonal planar | 1 | **Bent** | slightly < 120° | $\ce{SO2}$ |
| 4 | Tetrahedral | 0 | **Tetrahedral** | 109.5° | $\ce{CH4}$ |
| 4 | Tetrahedral | 1 | **Trigonal pyramidal** | ≈ 107° | $\ce{NH3}$ |
| 4 | Tetrahedral | 2 | **Bent** | ≈ 104.5° | $\ce{H2O}$ |

Six rows. That's the entire AP-required table. Notice the pattern in each block: the electron-domain geometry stays put (the bundle doesn't care which balloons are painted invisible), while the molecular geometry loses a vertex every time a balloon goes invisible.

Also notice **"bent" appears twice** — once at ~120° (from a trigonal planar bundle, like $\ce{SO2}$) and once at ~104.5° (from a tetrahedral bundle, like $\ce{H2O}$). Same photo name, different bundle, different angle. If a question asks for the approximate angle in a bent molecule, you *must* know which bundle it came from.

### Lone Pairs Squeeze: 109.5° → 107° → 104.5°

Line up three molecules that all have exactly **four electron domains**:

| Molecule | Bonding pairs | Lone pairs | Molecular geometry | Actual angle |
|:---:|:---:|:---:|:---:|:---:|
| $\ce{CH4}$ | 4 | 0 | Tetrahedral | 109.5° |
| $\ce{NH3}$ | 3 | 1 | Trigonal pyramidal | 107° |
| $\ce{H2O}$ | 2 | 2 | Bent | 104.5° |

Same bundle, same electron-domain geometry (tetrahedral, all three) — yet the angle between the *visible* balloons shrinks with every invisible one. Here's the balloon reasoning, which is exactly the argument the AP rubric wants:

A lone pair is held by **one** nucleus, so its electron cloud spreads wide and hugs close to the central atom — a fatter balloon. A bonding pair is stretched between **two** nuclei — a longer, skinnier balloon. Fatter balloons shove harder. So the repulsion order is:

$$\text{lone pair–lone pair} > \text{lone pair–bonding pair} > \text{bonding pair–bonding pair}$$

Each lone pair you add shoves the remaining bonding pairs closer together: one fat balloon in $\ce{NH3}$ squeezes the $\ce{H-N-H}$ angles from 109.5° down to about 107°; two fat balloons in $\ce{H2O}$ squeeze the $\ce{H-O-H}$ angle down to about 104.5°.

**FRQ-ready sentence:** *"Lone pairs occupy more space around the central atom than bonding pairs, so lone pair–bonding pair repulsions are greater than bonding pair–bonding pair repulsions, compressing the bond angle below the ideal 109.5°."*

(You don't need to memorize 107° and 104.5° to the decimal — but you must know the *direction*: slightly less than ideal, and more lone pairs means more squeeze.)

### Putting Shapes on Paper: Wedge-Dash in Words

Your paper is flat; tetrahedral molecules aren't. Chemists fake the third dimension with the **wedge-dash convention**:

- A **plain line** is a bond lying flat in the plane of the paper.
- A **solid wedge** (fat triangle) is a bond poking **out of the page toward you**.
- A **dashed wedge** (hashed lines) is a bond poking **behind the page away from you**.

For methane, the standard drawing puts two $\ce{C-H}$ bonds flat in the paper (one up, one down-left), one on a solid wedge (toward you), and one on a dashed wedge (away from you). In words: *"a carbon at the center of a caltrop, with the four hydrogens at the corners of a tetrahedron."* A rough ASCII impression:

```
        H                 the up-and-back leg
        |
        C                 central atom (the knot)
      / | \
     H  H  H              three legs splayed down like a tripod
   (flat, toward you, away from you)
```

If you're ever asked to *describe* a shape in an FRQ, name the geometry and the angle: "trigonal pyramidal, with $\ce{H-N-H}$ angles of approximately 107°" beats any drawing.

### Bonus Round: 5 and 6 Domains (Beyond the AP CED)

The current AP course description only requires geometries up to four domains — but the 5- and 6-domain shapes show up constantly in honors classes and college chemistry, and knowing they exist makes the pattern click. Treat this table as **bonus material, not exam-required**:

| Domains | Electron-domain geometry | Lone pairs | Molecular geometry | Angles | Example |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 5 | Trigonal bipyramidal | 0 | Trigonal bipyramidal | 90°, 120° | $\ce{PCl5}$ |
| 5 | Trigonal bipyramidal | 1 | Seesaw | ≈ 90°, ≈ 120° | $\ce{SF4}$ |
| 5 | Trigonal bipyramidal | 2 | T-shaped | ≈ 90° | $\ce{ClF3}$ |
| 5 | Trigonal bipyramidal | 3 | Linear | 180° | $\ce{XeF2}$ |
| 6 | Octahedral | 0 | Octahedral | 90° | $\ce{SF6}$ |
| 6 | Octahedral | 1 | Square pyramidal | ≈ 90° | $\ce{BrF5}$ |
| 6 | Octahedral | 2 | Square planar | 90° | $\ce{XeF4}$ |

Fun details if you're curious: with five balloons, not all positions are equal — there are two "axial" spots (up/down) and three "equatorial" spots (around the waist), and lone pairs always grab the roomier equatorial spots. That's why two lone pairs on $\ce{XeF2}$ leave the atoms perfectly **linear**. But again: if it has 5 or 6 domains, it won't be *required* on the AP exam.

### Why Shape Matters (The Teaser)

So why does AP Chemistry care this much about pictures of balloons? Because **shape decides behavior**:

- **Polarity.** Whether a molecule's bond dipoles cancel or add up depends entirely on geometry — $\ce{CO2}$'s two polar bonds cancel because it's linear; $\ce{H2O}$'s don't because it's bent. That single fact controls boiling points, solubility, and all of Unit 3. It's the whole subject of the next article, [Polarity and Hybridization](/chemistry/0407-polarity-hybridization).
- **Molecular recognition.** Your nose, your taste buds, your enzymes, and every drug in the pharmacy work by *shape-matching* — a molecule fits its protein target like a hand fits a glove. Change the 3D shape without changing a single bond, and the biology changes completely.

> **🎬 Hollywood Chemistry: Real or Not?**
> *The scene:* In a famous Breaking Bad classroom moment, a high-school chemistry teacher holds up his hands to explain **chirality**: some molecules come in mirror-image twins — same formula, same bonds — that can't be superimposed on each other, just like your left and right hands.
> *The verdict:* Real chemistry, and taught almost exactly right. Mirror-image molecules (enantiomers) really do exist, and because your body's proteins are themselves "handed," the twins can behave completely differently in you — one form of the molecule carvone smells like spearmint while its mirror twin smells like caraway seeds, and the two mirror forms of a drug can differ from medicine to danger. It's geometry, not composition, doing all of that — which is exactly why this article exists.

---

## Worked Examples

Every example runs the same pipeline: **(1)** draw the Lewis structure, **(2)** count electron domains on the central atom, **(3)** name both geometries, **(4)** predict the bond angle.

---

### Example 1: $\ce{CO2}$ — The Multiple-Bond Trap

**Problem:** Determine the electron-domain geometry, molecular geometry, and bond angle of carbon dioxide.

**Solution:**

**Step 1 — Lewis structure.** Valence electrons: $4 + 2(6) = 16$. The structure that satisfies all octets is $\ce{O=C=O}$, with two lone pairs on each oxygen and none on carbon.

**Step 2 — Count domains on C.** Two double bonds. Each double bond = **one** domain. Carbon has no lone pairs. Total: **2 domains**.

**Step 3 — Geometries.** Two balloons point opposite ways: electron-domain geometry = **linear**. No lone pairs on C, so molecular geometry = **linear** too.

**Step 4 — Angle.** $\ce{O-C-O} = 180°$.

**Answer: Linear / linear, 180°.** Sixteen electrons in those double bonds, and the shape is decided by counting to two.

---

### Example 2: $\ce{BF3}$ — Three Balloons, Flat Y

**Problem:** Determine both geometries and the bond angle of boron trifluoride.

**Solution:**

**Step 1 — Lewis structure.** Valence electrons: $3 + 3(7) = 24$. Boron bonds singly to each F; each F carries three lone pairs. Boron ends up with only 6 electrons — it's a famous, legitimate octet exception.

**Step 2 — Count domains on B.** Three single bonds, zero lone pairs: **3 domains**.

**Step 3 — Geometries.** Three balloons spread into a flat Y: electron-domain geometry = **trigonal planar**. No invisible balloons, so molecular geometry = **trigonal planar**.

**Step 4 — Angle.** $\ce{F-B-F} = 120°$, and the whole molecule is flat.

**Answer: Trigonal planar / trigonal planar, 120°.** (The 9 lone pairs on the fluorines never entered the count — they're not tied into the knot.)

---

### Example 3: $\ce{SO2}$ — Bent at 120°, Not 104.5°

**Problem:** Determine both geometries and the approximate bond angle of sulfur dioxide.

**Solution:**

**Step 1 — Lewis structure.** Valence electrons: $6 + 2(6) = 18$. Drawing $\ce{O=S-O}$ (with the single-bonded O carrying a negative formal charge region) gives resonance structures; either way, sulfur carries **one lone pair** plus bonds to two oxygens.

**Step 2 — Count domains on S.** One double bond (1 domain) + one single/double bond to the other O (1 domain) + one lone pair (1 domain) = **3 domains**. Remember: a bond to a neighbor counts once whether it's single or double.

**Step 3 — Geometries.** Three balloons → electron-domain geometry = **trigonal planar**. One balloon is invisible → the photo shows two atoms in a V: molecular geometry = **bent**.

**Step 4 — Angle.** Ideal trigonal planar is 120°; the fat lone-pair balloon squeezes it slightly. Actual: about 119°. AP answer: **slightly less than 120°**.

**Answer: Trigonal planar / bent, ≈ 120° (slightly less).** This is the "other bent" — do not answer 104.5° here; that number belongs to a four-domain bundle.

---

### Example 4: $\ce{CH4}$ — The Full Caltrop

**Problem:** Determine both geometries and the bond angle of methane.

**Solution:**

**Step 1 — Lewis structure.** Valence electrons: $4 + 4(1) = 8$. Carbon single-bonds to four hydrogens; no lone pairs anywhere on C.

**Step 2 — Count domains on C.** Four single bonds: **4 domains**.

**Step 3 — Geometries.** Four balloons pop into 3D: electron-domain geometry = **tetrahedral**. All four balloons visible → molecular geometry = **tetrahedral**.

**Step 4 — Angle.** $\ce{H-C-H} = 109.5°$ — the famous tetrahedral angle. Note it is *more* than the 90° you'd guess from flat drawing: 3D gives the balloons extra room.

**Answer: Tetrahedral / tetrahedral, 109.5°.**

---

### Example 5: $\ce{NH3}$ — One Invisible Balloon

**Problem:** Determine both geometries and the approximate bond angle of ammonia.

**Solution:**

**Step 1 — Lewis structure.** Valence electrons: $5 + 3(1) = 8$. Nitrogen single-bonds to three hydrogens and keeps **one lone pair**.

**Step 2 — Count domains on N.** 3 bonds + 1 lone pair = **4 domains**.

**Step 3 — Geometries.** Four balloons → electron-domain geometry = **tetrahedral**. One balloon invisible → the photo is a tripod: molecular geometry = **trigonal pyramidal**.

**Step 4 — Angle.** Ideal 109.5°, squeezed by the fatter lone-pair balloon down to **≈ 107°**.

**Answer: Tetrahedral / trigonal pyramidal, ≈ 107°.** Writing "tetrahedral" as the *molecular* geometry is the single most common wrong answer on this topic.

---

### Example 6: $\ce{H2O}$ — Two Invisible Balloons

**Problem:** Determine both geometries and the approximate bond angle of water.

**Solution:**

**Step 1 — Lewis structure.** Valence electrons: $6 + 2(1) = 8$. Oxygen single-bonds to two hydrogens and keeps **two lone pairs**.

**Step 2 — Count domains on O.** 2 bonds + 2 lone pairs = **4 domains**.

**Step 3 — Geometries.** Four balloons → electron-domain geometry = **tetrahedral**. Two balloons invisible → the photo shows just a V of three atoms: molecular geometry = **bent**.

**Step 4 — Angle.** Two fat lone-pair balloons squeeze the ideal 109.5° down to **≈ 104.5°**.

**Answer: Tetrahedral / bent, ≈ 104.5°.** Water is *not* linear — and that bend is why water is polar, why ice floats, and why you exist. More in the next article.

---

### Example 7: $\ce{NH4+}$ — Ions Play by the Same Rules

**Problem:** Determine both geometries and the bond angle of the ammonium ion.

**Solution:**

**Step 1 — Lewis structure.** Valence electrons: $5 + 4(1) - 1 = 8$ (subtract one for the $1+$ charge). Nitrogen single-bonds to four hydrogens; the lone pair from $\ce{NH3}$ is now a bonding pair. No lone pairs remain on N.

**Step 2 — Count domains on N.** Four single bonds: **4 domains**.

**Step 3 — Geometries.** Tetrahedral bundle, all balloons visible: **tetrahedral / tetrahedral**.

**Step 4 — Angle.** $\ce{H-N-H} = 109.5°$ — back up from 107°, because the squeezing lone pair became an ordinary bond.

**Answer: Tetrahedral / tetrahedral, 109.5°.** Compare $\ce{NH3}$ (107°) with $\ce{NH4+}$ (109.5°): converting the fat balloon into a regular one releases the squeeze. Great compare-and-contrast FRQ material.

---

### Example 8: $\ce{CO3^2-}$ — Resonance Doesn't Bend Anything

**Problem:** The carbonate ion has three resonance structures. Determine its geometry and bond angle, and explain why resonance doesn't change the answer.

**Solution:**

**Step 1 — Lewis structure.** Valence electrons: $4 + 3(6) + 2 = 24$. Each resonance structure shows one $\ce{C=O}$ and two $\ce{C-O}$ single bonds; the double bond rotates among the three positions across the structures. Carbon has no lone pairs.

**Step 2 — Count domains on C.** In *every* resonance structure: three bonded neighbors, zero lone pairs = **3 domains**. Whether a given bond is drawn single or double never changes the count, because a multiple bond is still one domain.

**Step 3 — Geometries.** **Trigonal planar / trigonal planar.**

**Step 4 — Angle.** All three $\ce{O-C-O}$ angles are exactly **120°** — and because the real ion is the average of the resonance structures, all three bonds are identical in length too.

**Answer: Trigonal planar, 120°.** Resonance changes how we *draw* electrons, never how many *regions* of electrons surround the central atom — so geometry is resonance-proof.

---

### Example 9: $\ce{HCN}$ — Triple Bond, Still One Balloon

**Problem:** Determine the geometry and bond angle of hydrogen cyanide.

**Solution:**

**Step 1 — Lewis structure.** Valence electrons: $1 + 4 + 5 = 10$. Structure: $\ce{H-C#N}$ with one lone pair on N. The triple bond is required to complete both octets.

**Step 2 — Count domains on C** (the central atom). One single bond to H (1 domain) + one triple bond to N (**1** domain) = **2 domains**. Six electrons in that triple bond; it still counts once.

**Step 3 — Geometries.** **Linear / linear.**

**Step 4 — Angle.** $\ce{H-C-N} = 180°$.

**Answer: Linear / linear, 180°.**

---

### Example 10 (Bonus): $\ce{SF4}$ — The Seesaw

**Problem:** *(Beyond the AP CED — for the curious.)* Predict the molecular geometry of sulfur tetrafluoride.

**Solution:**

**Step 1 — Lewis structure.** Valence electrons: $6 + 4(7) = 34$. Four $\ce{S-F}$ single bonds use 8; the fluorines' lone pairs use 24; the last 2 sit as a **lone pair on sulfur** (an expanded octet — allowed for period-3 elements).

**Step 2 — Count domains on S.** 4 bonds + 1 lone pair = **5 domains**.

**Step 3 — Geometries.** Five domains → electron-domain geometry = **trigonal bipyramidal**. The lone pair grabs a roomy equatorial spot, leaving the four F atoms in a shape like a playground seesaw: molecular geometry = **seesaw**.

**Step 4 — Angles.** Roughly 90° (axial–equatorial) and slightly under 120° (equatorial–equatorial), both squeezed by the lone pair.

**Answer: Trigonal bipyramidal / seesaw.** You won't be required to produce this on the AP exam — but notice the logic is *identical* to the 4-domain cases: count, arrange, hide the lone pairs, name the photo.

---

## Common Mistakes

| The mistake | Why it happens | How to avoid it |
|---|---|---|
| Calling $\ce{CO2}$ bent | "Double bonds are big, so they must count double" | A multiple bond is **one domain** — one balloon, one neighbor, one direction. Count neighbors + central lone pairs, never electrons |
| Giving "tetrahedral" as the *molecular* geometry of $\ce{NH3}$ or $\ce{H2O}$ | Confusing the bundle with the photo | Two-name system: *electron-domain* geometry counts every balloon; *molecular* geometry names only visible atoms |
| Counting lone pairs on **outer** atoms | The Lewis structure is covered in dots and they all look important | Only domains tied to the **central atom's** knot shove the shape. Outer-atom lone pairs: ignore |
| Answering "104.5°" for every bent molecule | Memorizing "bent = 104.5" | Bent comes in two flavors: from a trigonal planar bundle (≈ 120°, like $\ce{SO2}$) and from a tetrahedral bundle (≈ 104.5°, like $\ce{H2O}$). Check the domain count first |
| Predicting geometry from a wrong Lewis structure | Skipping the electron count to save time | The cascade: wrong electron count → wrong lone pairs → wrong domain count → wrong geometry → wrong angle → wrong polarity. Thirty seconds of counting protects five answers |
| Saying lone pairs "don't matter" because they're not in the name | The photo hides them, so students forget them | Lone pairs are the *fattest* balloons — they set the arrangement AND squeeze the angles. Invisible ≠ absent |
| Claiming resonance makes a molecule "flip between shapes" | Treating resonance structures as real alternating molecules | Every resonance structure has the same domain count, so the geometry is one fixed shape. $\ce{CO3^2-}$ is trigonal planar, period |
| Expecting exactly 109.5° in $\ce{NH3}$ and $\ce{H2O}$ | Reading the ideal angle straight off the table | Lone pairs repel more than bonding pairs — angles are *slightly less than* ideal. Know the direction of the squeeze |

---

## AP Exam Tips

1. **Use AP's exact vocabulary.** The graders' answer keys say *linear, trigonal planar, bent, tetrahedral, trigonal pyramidal*. "Pyramid-shaped," "triangle," "V-shaped," or "angular" may not earn the point. Spelling doesn't have to be perfect; the *term* does.
2. **Read whether the question wants electron-domain or molecular geometry.** FRQs often ask for both in back-to-back parts, precisely to catch students who only know one name. If it says "geometry of the molecule" or "shape," give the molecular geometry.
3. **"Predict the approximate bond angle" is a multiple-choice staple.** The choices are usually 90°, 104.5°/107°, 109.5°, 120°, 180°. Route: Lewis structure → domain count → ideal angle → subtract a little if there are central lone pairs. "Slightly less than 109.5°" is exactly the level of precision expected.
4. **Beware the wrong-Lewis-structure cascade.** A geometry FRQ is really a Lewis-structure FRQ in disguise. If you miscount valence electrons (especially for ions — add for negative charge, subtract for positive), everything downstream dies. Double-check the electron count *before* naming anything.
5. **The multiple-bond trap is guaranteed to appear somewhere.** $\ce{CO2}$ is linear. $\ce{HCN}$ is linear. $\ce{CH2O}$ is trigonal planar. If you catch yourself counting a double bond as two domains, stop and recount.
6. **Justifications must cite repulsion, not "wanting."** Write "lone pair–bonding pair repulsion exceeds bonding pair–bonding pair repulsion, compressing the angle" — never "the lone pair wants more space." Anthropomorphic answers lose justification points across all of AP Chemistry.
7. **Resonance questions love to pair with geometry.** A classic two-parter: draw the resonance structures of $\ce{NO3-}$ or $\ce{CO3^2-}$, then give the geometry and explain why all bonds are equal length. Answer: same domain count in every structure → one geometry; the true structure is an average → identical bonds.
8. **Don't volunteer 5- and 6-domain shapes.** The current CED caps required geometries at four domains. If an exam question somehow involves a bigger molecule, the geometry will be given — your job will be using it, not naming it.

---

## Practice Problems

### Problem 1

Determine the electron-domain geometry, molecular geometry, and approximate bond angle of $\ce{PCl3}$.

<details>
<summary><strong>Solution</strong></summary>

**Lewis structure:** Valence electrons: $5 + 3(7) = 26$. Phosphorus single-bonds to three chlorines and keeps one lone pair (each Cl carries three lone pairs, which don't count).

**Domains on P:** 3 bonds + 1 lone pair = 4 domains.

**Geometries:** Four balloons → electron-domain geometry = tetrahedral. One invisible → molecular geometry = trigonal pyramidal.

**Angle:** Slightly less than 109.5° (≈ 100°–107°; "slightly less than 109.5°" earns the point).

**Answer: Tetrahedral / trigonal pyramidal, slightly less than 109.5°.**

</details>

### Problem 2

Determine both geometries and the bond angle of $\ce{SO3}$.

<details>
<summary><strong>Solution</strong></summary>

**Lewis structure:** Valence electrons: $6 + 3(6) = 24$. Sulfur bonds to three oxygens (resonance structures exist); sulfur has **no lone pairs**.

**Domains on S:** 3 bonded neighbors + 0 lone pairs = 3 domains — the same in every resonance structure.

**Geometries:** Trigonal planar / trigonal planar.

**Angle:** Exactly 120°, all bonds identical (resonance average).

**Answer: Trigonal planar / trigonal planar, 120°.** Compare with $\ce{SO2}$: one lone pair on S turned that one bent.

</details>

### Problem 3

Predict the molecular geometry and approximate bond angle of $\ce{H2S}$.

<details>
<summary><strong>Solution</strong></summary>

**Lewis structure:** Valence electrons: $6 + 2(1) = 8$. Sulfur (same group as oxygen) bonds to two hydrogens and keeps two lone pairs — a sulfur version of water.

**Domains on S:** 2 bonds + 2 lone pairs = 4 domains.

**Geometries:** Tetrahedral / **bent**.

**Angle:** Less than 109.5° — the two fat lone-pair balloons squeeze the $\ce{H-S-H}$ angle. (Measured: about 92°, even tighter than water's, but "less than 109.5°" is the AP-level answer.)

**Answer: Bent, less than 109.5°.**

</details>

### Problem 4

The nitrate ion $\ce{NO3-}$ has three resonance structures. Give its molecular geometry and bond angle, and explain in one sentence why the three $\ce{N-O}$ bonds are all the same length.

<details>
<summary><strong>Solution</strong></summary>

**Lewis structure:** Valence electrons: $5 + 3(6) + 1 = 24$. Each resonance structure: one $\ce{N=O}$, two $\ce{N-O}$, no lone pairs on N.

**Domains on N:** 3 in every resonance structure.

**Geometry:** Trigonal planar, 120°.

**Bond lengths:** The true ion is the average of the three equivalent resonance structures, so each bond has the same intermediate character (bond order $\tfrac{4}{3}$) and the same length.

**Answer: Trigonal planar, 120°; resonance averaging makes all three bonds identical.**

</details>

### Problem 5

Determine both geometries and the bond angle of $\ce{CS2}$.

<details>
<summary><strong>Solution</strong></summary>

**Lewis structure:** Valence electrons: $4 + 2(6) = 16$ — isoelectronic with $\ce{CO2}$. Structure: $\ce{S=C=S}$, no lone pairs on C.

**Domains on C:** two double bonds = **2 domains** (each multiple bond counts once).

**Geometries:** Linear / linear.

**Answer: Linear / linear, 180°.**

</details>

### Problem 6

Determine the molecular geometry and approximate bond angle of the hydronium ion, $\ce{H3O+}$.

<details>
<summary><strong>Solution</strong></summary>

**Lewis structure:** Valence electrons: $6 + 3(1) - 1 = 8$ (subtract one for the positive charge). Oxygen bonds to three hydrogens and keeps **one** lone pair.

**Domains on O:** 3 bonds + 1 lone pair = 4 domains.

**Geometries:** Tetrahedral / **trigonal pyramidal** — the ammonia shape, not the water shape. Water gained a proton and one of its two lone pairs became a bond.

**Angle:** Slightly less than 109.5° (≈ 107°).

**Answer: Trigonal pyramidal, ≈ 107°.**

</details>

### Problem 7

$\ce{CO2}$ and $\ce{SO2}$ are both "a central atom bonded to two oxygens" — yet one is linear and the other is bent. Explain why, in two or three sentences a grader would accept.

<details>
<summary><strong>Solution</strong></summary>

In $\ce{CO2}$, carbon has two double bonds and **no lone pairs**: 2 electron domains, which repel to opposite sides, giving a linear molecule (180°).

In $\ce{SO2}$, sulfur is bonded to two oxygens **and carries one lone pair**: 3 electron domains, which arrange trigonal planar (~120°). The lone pair occupies one corner of the triangle but isn't counted in the molecular shape, so the atoms form a bent molecule with an angle of slightly less than 120°.

**Answer: The lone pair on sulfur is the entire difference — same visible atoms, different domain count, different shape.**

</details>

### Problem 8

Rank $\ce{CH4}$, $\ce{NH3}$, and $\ce{H2O}$ from largest to smallest bond angle, and justify the ranking with a repulsion argument.

<details>
<summary><strong>Solution</strong></summary>

All three have **4 electron domains** (tetrahedral electron-domain geometry), so all start from an ideal 109.5°.

Lone pairs are held by only one nucleus, so they occupy more space than bonding pairs; lone pair–bonding pair repulsion exceeds bonding pair–bonding pair repulsion. Each additional lone pair squeezes the remaining bond angles further:

- $\ce{CH4}$: 0 lone pairs → 109.5°
- $\ce{NH3}$: 1 lone pair → ≈ 107°
- $\ce{H2O}$: 2 lone pairs → ≈ 104.5°

**Answer: $\ce{CH4} > \ce{NH3} > \ce{H2O}$, because each added lone pair increases the compression of the bond angles below the ideal 109.5°.**

</details>

### Problem 9

Formaldehyde, $\ce{CH2O}$, has carbon as its central atom. Determine both geometries and the approximate bond angles.

<details>
<summary><strong>Solution</strong></summary>

**Lewis structure:** Valence electrons: $4 + 2(1) + 6 = 12$. Carbon forms two $\ce{C-H}$ single bonds and one $\ce{C=O}$ double bond; the two remaining lone pairs sit on oxygen. No lone pairs on C.

**Domains on C:** 2 single bonds + 1 double bond (counts once) = **3 domains**.

**Geometries:** Trigonal planar / trigonal planar — the molecule is flat.

**Angles:** Approximately 120°. (In reality the fat double-bond domain pushes the $\ce{H-C-H}$ angle slightly below 120° — a nice detail, but "≈ 120°" is the expected answer.)

**Answer: Trigonal planar / trigonal planar, ≈ 120°.**

</details>

### Problem 10

Determine the molecular geometry and approximate bond angle of the nitrite ion, $\ce{NO2-}$.

<details>
<summary><strong>Solution</strong></summary>

**Lewis structure:** Valence electrons: $5 + 2(6) + 1 = 18$. Two resonance structures: $\ce{O=N-O^-}$ ↔ $\ce{^-O-N=O}$, each with **one lone pair on nitrogen**.

**Domains on N:** 2 bonded oxygens + 1 lone pair = 3 domains (same in both resonance structures).

**Geometries:** Trigonal planar / **bent**.

**Angle:** Slightly less than 120° (measured ≈ 115°). This is the $\ce{SO2}$-style bent, *not* the water-style bent.

**Answer: Bent, slightly less than 120°.**

</details>

### Problem 11

Determine both geometries and the bond angle of $\ce{SiCl4}$.

<details>
<summary><strong>Solution</strong></summary>

**Lewis structure:** Valence electrons: $4 + 4(7) = 32$. Silicon (carbon's downstairs neighbor) single-bonds to four chlorines; no lone pairs on Si. The twelve lone pairs on the chlorines don't count — they're not on the central atom.

**Domains on Si:** 4 bonds + 0 lone pairs = 4 domains.

**Geometries:** Tetrahedral / tetrahedral.

**Answer: Tetrahedral / tetrahedral, 109.5°.**

</details>

### Problem 12

A molecule's central atom has three bonding domains and one lone pair. Without knowing the element, give the electron-domain geometry, the molecular geometry, and the approximate bond angle.

<details>
<summary><strong>Solution</strong></summary>

Total domains: $3 + 1 = 4$ → electron-domain geometry = **tetrahedral**.

One domain is invisible in the photo → molecular geometry = **trigonal pyramidal**.

Angle: slightly less than 109.5° (≈ 107°), because the lone pair repels the bonding pairs more strongly than they repel each other.

**Answer: Tetrahedral / trigonal pyramidal, slightly less than 109.5°.** VSEPR never needed the element's name — only the domain count.

</details>

### Problem 13

Ozone, $\ce{O3}$, protects you from UV light every time you're outside at Torrey Pines. Determine its molecular geometry, approximate bond angle, and whether its two bonds are the same length.

<details>
<summary><strong>Solution</strong></summary>

**Lewis structure:** Valence electrons: $3(6) = 18$. Two resonance structures: $\ce{O=O-O}$ ↔ $\ce{O-O=O}$, with **one lone pair on the central oxygen** (plus lone pairs on the outer oxygens, which don't count).

**Domains on central O:** 2 bonded neighbors + 1 lone pair = 3 domains.

**Geometries:** Trigonal planar / **bent**, angle slightly less than 120° (measured ≈ 117°).

**Bond lengths:** Equal — the real molecule is the resonance average, each bond of order 1.5.

**Answer: Bent, ≈ 117° (slightly less than 120°), with two identical bonds.**

</details>

### Problem 14 (Bonus — beyond the AP CED)

Xenon tetrafluoride, $\ce{XeF4}$, was one of the first noble-gas compounds ever made. Its xenon atom holds four bonding pairs and two lone pairs. Predict the electron-domain geometry and the molecular geometry.

<details>
<summary><strong>Solution</strong></summary>

**Domains on Xe:** 4 bonds + 2 lone pairs = **6 domains** → electron-domain geometry = **octahedral** (all angles 90°).

**Placing the lone pairs:** The two fat lone-pair balloons repel each other most, so they take positions **180° apart** — straight up and straight down. The four fluorines are left in a flat square around the middle.

**Molecular geometry:** **Square planar**, with $\ce{F-Xe-F}$ angles of 90°.

**Answer: Octahedral / square planar.** Not required on the AP exam — but the reasoning (count, arrange, park the fat balloons far apart, photograph the rest) is pure VSEPR.

</details>

---

## Quick Reference

**The pipeline:** correct Lewis structure → count domains on the central atom (multiple bond = 1; central lone pairs count; outer lone pairs don't) → electron-domain geometry from the count → molecular geometry from the visible atoms → angle = ideal, minus a squeeze per central lone pair.

| Domains | LP | Electron-domain geom. | Molecular geom. | Angle | Example |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 2 | 0 | Linear | Linear | 180° | $\ce{CO2}$, $\ce{HCN}$ |
| 3 | 0 | Trigonal planar | Trigonal planar | 120° | $\ce{BF3}$, $\ce{CO3^2-}$ |
| 3 | 1 | Trigonal planar | Bent | < 120° | $\ce{SO2}$, $\ce{O3}$, $\ce{NO2-}$ |
| 4 | 0 | Tetrahedral | Tetrahedral | 109.5° | $\ce{CH4}$, $\ce{NH4+}$ |
| 4 | 1 | Tetrahedral | Trigonal pyramidal | ≈ 107° | $\ce{NH3}$, $\ce{H3O+}$ |
| 4 | 2 | Tetrahedral | Bent | ≈ 104.5° | $\ce{H2O}$, $\ce{H2S}$ |

**Repulsion order:** lone–lone > lone–bond > bond–bond ⟹ every central lone pair squeezes the visible angles below ideal.

**Balloon dictionary:** knot = central atom · balloon = electron domain · fat invisible balloon = lone pair · the photo = molecular geometry (atoms only).

---

<div align="center">

[← Resonance and Formal Charge](/chemistry/0405-resonance-formal-charge) | [Polarity and Hybridization →](/chemistry/0407-polarity-hybridization)

</div>
