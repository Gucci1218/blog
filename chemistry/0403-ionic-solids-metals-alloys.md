# Ionic Solids, Metals, and Alloys
<p class="article-date">July 4, 2026</p>

*Fourth of July, Padres game, Petco Park — Dad splurged on a \$7 pretzel and we're people-watching more than baseball-watching. From our seats I can see two completely different crowds. Down in the reserved sections, everyone is locked into assigned seats, and one section is seated home-fan, away-fan, home-fan, away-fan in a strict checkerboard — nobody moves, and honestly nobody CAN move without chaos. Up on the standing-room concourse it's the opposite: a river of people flowing freely around the fixed taco stands, re-forming instantly every time someone pushes through with a tray of nachos. Then the gates open for late arrivals and the visitors mix in — adults take empty seats among the locals, while little kids slip into the gaps between grown-ups in the aisle. One stadium, three crowd arrangements — and they are, almost exactly, the three solid structures AP Chemistry Unit 2 asks you to master: the rigid alternating lattice of an ionic solid, the flowing electron sea of a metal, and the two kinds of alloys. Tonight's game explains why salt shatters, why gold bends, and why swords are made of steel instead of pure iron.*

---

## What You'll Learn

- Describe the structure of an ionic solid as a 3D lattice of alternating cations and anions held by Coulombic attraction
- Explain — from structure, not vibes — why ionic solids are brittle, high-melting, and conduct electricity only when molten or dissolved
- Describe the electron-sea model of metallic bonding: cation cores in a delocalized sea of valence electrons
- Explain why metals are malleable, ductile, shiny, and conduct electricity as solids
- Rank metallic bond strength (and melting behavior) using number of valence electrons and cation size ($\ce{Na}$ vs $\ce{Mg}$ vs $\ce{Al}$)
- Distinguish substitutional alloys (similar radii — brass, sterling silver) from interstitial alloys (small atoms in gaps — steel), and predict the type from an atomic-radii table
- Explain why alloys are usually harder than the pure metals they come from
- Classify an unknown solid as ionic, metallic, molecular covalent, or network covalent from melting point and conductivity data — the classic AP data-table question

---

## Prerequisites

- [Ions and Ionic Compounds](/chemistry/0306-valence-electrons-ionic-compounds) — lattice energy and the $E \propto \frac{|q_1 q_2|}{r}$ ranking argument; this article turns that energy into physical properties
- [Bonds and Electronegativity](/chemistry/0401-bonds-and-electronegativity) — the ionic / covalent / metallic triangle; here we zoom into what the ionic and metallic corners actually look like as solids

---

## The Core Concept

### Intuition First

Back to Petco Park, because each crowd is a solid.

**The seated checkerboard = an ionic solid.** In the reserved section, home fans ($+$) and away fans ($-$) alternate seat by seat, row by row, in every direction. Why that arrangement? Every fan is surrounded on all sides by fans of the *other* team (opposite charges attract — maximum attraction), and fans of the *same* team never sit next to each other (like charges repel — minimum repulsion). The arrangement is incredibly stable, but it's also rigid: every single person is locked in place by their neighbors. Nobody strolls around. And here's the disaster scenario — shove one entire row sideways by ONE seat, and suddenly home fans are face to face with home fans down the whole row. Repulsion everywhere at once. The section doesn't gently absorb the shove; it erupts, and the crowd splits apart along that row. That's brittleness: an ionic crystal doesn't dent, it **shatters along a plane**.

**The concourse = a metallic solid.** The taco stands are the metal cations — fixed, regularly spaced, not going anywhere. The crowd is the **sea of delocalized valence electrons** — it belongs to no single stand, it flows around all of them, and it fills every gap. Shove this crowd and nothing shatters, because there are no alternating charges to misalign; the sea simply *re-flows* around the disturbance. That's malleability. And because the crowd is mobile, anything you pass into it (a wave, a beach ball, an electric charge) travels across the whole concourse — metals conduct **as solids**.

**Late arrivals = alloys.** Mix a second element into a metal and you get an alloy — and the stadium predicts both kinds. Visiting adults are about the same size as the locals, so they take regular seats *in place of* home fans: a **substitutional alloy**, like zinc atoms replacing copper atoms in brass. Little kids are much smaller, so they don't take seats at all — they slip into the **gaps between** adults: an **interstitial alloy**, like small carbon atoms wedged between iron atoms in steel. Either way, the newcomers jam up the crowd: rows can no longer slide smoothly past each other, which is exactly why alloys are usually **harder** than pure metals.

Keep those three crowds in your head. Every property in this article is one of them in disguise.

### Ionic Solids: The Checkerboard Lattice

An ionic solid is a **three-dimensional lattice** of cations and anions arranged so that each ion is surrounded by ions of opposite charge. Here's a slice of $\ce{NaCl}$ — imagine this pattern extending in all three dimensions:

```
   Na+  Cl-  Na+  Cl-  Na+
   Cl-  Na+  Cl-  Na+  Cl-
   Na+  Cl-  Na+  Cl-  Na+
   Cl-  Na+  Cl-  Na+  Cl-
```

In real $\ce{NaCl}$, every $\ce{Na+}$ touches six $\ce{Cl-}$ neighbors (up, down, left, right, front, back), and every $\ce{Cl-}$ touches six $\ce{Na+}$. There is no "$\ce{NaCl}$ molecule" anywhere — just an endless alternating pattern, which is why we say **formula unit** for the 1:1 ratio.

Why this arrangement? Pure Coulomb's law:

$$E \propto \frac{|q_1 q_2|}{r}$$

Alternating charges put every attraction at the shortest possible distance and push every like–like repulsion farther away. The lattice is nature's answer to "maximize attraction, minimize repulsion."

Each property of an ionic solid is a direct consequence of this structure:

| Property | Structural reason (the AP-credit sentence) |
|---|---|
| **High melting point** | Melting requires overcoming strong Coulombic attractions between many oppositely charged ions throughout the lattice (this is the lattice energy from [0306](/chemistry/0306-valence-electrons-ionic-compounds)) |
| **Brittle / shatters** | An applied force shifts a layer of ions so that **like charges align and repel**; the crystal fractures along that plane instead of bending |
| **Does NOT conduct as a solid** | Ions are charged, but they are **locked in fixed lattice positions** — no mobile charged particles |
| **Conducts when molten or dissolved** | Melting or dissolving frees the ions to **move**; mobile ions carry charge |

The brittleness picture, in ASCII — one row shoved one position to the right:

```
   Before the shove:              After the shove:

   Na+  Cl-  Na+  Cl-             Na+  Cl-  Na+  Cl-
   Cl-  Na+  Cl-  Na+        →         Na+  Cl-  Na+  Cl-
   Na+  Cl-  Na+  Cl-             Na+  Cl-  Na+  Cl-
                                   ↑ now Na+ sits ABOVE Na+ and
                                     Cl- above Cl-: repulsion along
                                     the whole plane → CRACK
```

That's the fans-face-off moment. One shove, like charges aligned, crystal splits.

**The conductivity fingerprint.** This one idea identifies ionic compounds on sight:

| State | Conducts? | Why |
|---|---|---|
| $\ce{NaCl(s)}$ | No | Ions locked in the lattice — the seated crowd |
| $\ce{NaCl(l)}$ (molten, above 801°C) | Yes | Lattice destroyed; ions free to move |
| $\ce{NaCl(aq)}$ | Yes | Ions separated and mobile in water |

Conduction always needs **mobile charged particles**. Ionic solids have the charges but not the mobility — until you melt or dissolve them.

### Metallic Solids: Cations in an Electron Sea

The **electron-sea model**: a metal is a lattice of **cation cores** (the nucleus plus inner electrons) sitting in a **sea of delocalized valence electrons**. Each metal atom donates its valence electrons to the collective; the electrons belong to the entire crystal, not to any one atom. The bonding is the attraction between the positive cores and the surrounding negative sea — taco stands held in place by the crowd pressing around them.

Every metallic property comes straight from that picture:

| Property | Structural reason |
|---|---|
| **Conducts as a SOLID** | Delocalized valence electrons are mobile and carry charge — no melting required |
| **Malleable & ductile** | When layers of cations shift, the electron sea **re-flows** around the new arrangement; cations are never forced to face cations directly, so the metal deforms instead of shattering |
| **Luster (shiny)** | The mobile electrons interact with and re-emit light across a wide range of wavelengths |
| **Thermal conductor** | Mobile electrons carry kinetic energy quickly through the solid |

Compare the shove test: shove an ionic lattice → like charges align → shatter. Shove a metal → the sea flows around the shove → dent. Same push, opposite outcomes, all structure.

**How strong is a metallic bond?** Two dials, both Coulombic:

1. **More valence electrons in the sea** → denser sea → stronger attraction.
2. **Smaller, more highly charged cation** → shorter distance, bigger $|q_1 q_2|$ → stronger attraction.

Period 3 is the textbook demonstration:

| Metal | Cation in the lattice | e⁻ contributed to sea | Melting point |
|---|---|---|---|
| $\ce{Na}$ | $\ce{Na+}$ (large, 1+) | 1 | 98°C |
| $\ce{Mg}$ | $\ce{Mg^2+}$ (smaller, 2+) | 2 | 650°C |
| $\ce{Al}$ | $\ce{Al^3+}$ (smallest, 3+) | 3 | 660°C |

Sodium melts below the boiling point of water — you could melt it in a saucepan (please don't). Magnesium and aluminum hold on hundreds of degrees longer. (Aluminum's *melting* point barely edges out magnesium's, but its boiling point — 2519°C vs 1091°C — and its hardness show how much stronger the 3+/three-electron bonding really is.) The AP sentence: *"$\ce{Al}$ contributes more valence electrons to the sea and has a smaller, more highly charged cation, so the Coulombic attraction between cations and the electron sea is stronger."*

### Alloys: Mixing the Crowd

An **alloy** is a mixture of a metal with one or more other elements that keeps metallic properties (it still has an electron sea, so it still conducts and still shines). AP Chemistry cares about two types, and **atomic radius decides which one forms**:

**Substitutional alloy — same-size visitors take seats.** When the added atoms are **similar in size** to the host atoms (radii within roughly 15%), they substitute directly into lattice positions.

```
   Cu  Cu  Cu  Cu  Cu          Cu  Zn  Cu  Cu  Zn
   Cu  Cu  Cu  Cu  Cu    →     Cu  Cu  Zn  Cu  Cu
   Cu  Cu  Cu  Cu  Cu          Zn  Cu  Cu  Zn  Cu
      pure copper                 brass (Cu/Zn)
```

Examples: **brass** ($\ce{Cu}$, 128 pm + $\ce{Zn}$, 134 pm — under 5% different), **bronze** ($\ce{Cu}$ + $\ce{Sn}$), **sterling silver** (92.5% $\ce{Ag}$ + 7.5% $\ce{Cu}$; 144 pm vs 128 pm — about 11%).

**Interstitial alloy — kids slip into the gaps.** When the added atoms are **much smaller** than the host (roughly 60% of the host radius or less), they don't take lattice positions at all — they wedge into the **interstices**, the natural holes between host atoms.

```
   Fe   Fe   Fe   Fe
      c    c                  ← tiny C atoms in the gaps
   Fe   Fe   Fe   Fe
           c
   Fe   Fe   Fe   Fe
       steel (Fe/C)
```

The classic example: **steel** — carbon (77 pm) tucked between iron atoms (126 pm); carbon is only ~61% of iron's size.

**Why alloys are harder than pure metals.** A pure metal is malleable because identical layers slide past each other easily while the sea re-flows. Foreign atoms **disrupt the sliding planes**: substituted atoms of a different size make the layers bumpy, and interstitial atoms physically **pin neighboring layers together**. At the stadium: once the kids fill the aisles, the crowd can't re-flow — the flow jams. That's why pure gold is too soft for a ring (jewelers cut it with copper), why pure iron bends but steel holds an edge, and why sterling silver survives daily life better than pure silver.

### The Master Table: Four Kinds of Solids

AP Unit 2 wants you to classify **four** solid types from properties. Two we've built tonight; two get a preview:

| Solid type | Particles at lattice points | Force holding it together | Melting point | Conducts as solid? | Molten/aq? | Examples |
|---|---|---|---|---|---|---|
| **Ionic** | Cations + anions, alternating | Coulombic attraction between ions | High (700–3000°C) | No | **Yes** (molten or dissolved) | $\ce{NaCl}$, $\ce{MgO}$, $\ce{CaF2}$ |
| **Metallic** | Cation cores in electron sea | Attraction of cations to delocalized e⁻ | Varies, often high | **Yes** | Yes | $\ce{Cu}$, $\ce{Fe}$, brass, steel |
| **Molecular covalent** | Discrete molecules | *Weak forces between molecules* (Unit 3!) | **Low** (often below ~300°C) | No | No | $\ce{H2O}$ (ice), $\ce{CO2}$ (dry ice), $\ce{I2}$ |
| **Network covalent** | Atoms, covalently bonded in all directions | Covalent bonds throughout the crystal | **Extremely high** | No (except graphite) | No | diamond ($\ce{C}$), quartz ($\ce{SiO2}$) |

Two quick notes on the newcomers:

- **Molecular covalent solids** (teaser — all of Unit 3): the covalent bonds *inside* each molecule are strong, but melting only has to overcome the weak attractions *between* molecules. That's why ice melts in your hand while $\ce{NaCl}$ needs 801°C. Details next unit.
- **Network covalent solids** (one paragraph is all AP requires): in diamond, every carbon is covalently bonded to four others in an endless 3D web — the whole crystal is effectively one molecule. Melting means breaking actual covalent bonds, so melting points are enormous (quartz, $\ce{SiO2}$, melts around 1610°C; diamond doesn't melt at ordinary pressure). No ions, no free electrons → no conductivity in any state (graphite, with its delocalized electrons, is the famous exception).

**The classification algorithm** for data-table questions:

1. **Conducts as a solid?** → Metallic. Done.
2. **Doesn't conduct as solid, but DOES conduct molten or dissolved?** → Ionic. (This is the fingerprint.)
3. **Never conducts, low melting point?** → Molecular covalent.
4. **Never conducts, extremely high melting point?** → Network covalent.

---

## Worked Examples

### Example 1: Why Salt Shatters and Copper Dents

**Problem:** A hammer strikes a crystal of $\ce{NaCl}$ and it shatters. The same hammer strikes a piece of $\ce{Cu}$ and it flattens. Explain both observations in terms of structure.

**Solution:**

**Step 1 — $\ce{NaCl}$:** In the ionic lattice, cations and anions alternate. The hammer blow shifts one layer of ions relative to the next, so $\ce{Na+}$ ions align with $\ce{Na+}$ ions and $\ce{Cl-}$ with $\ce{Cl-}$ across the slip plane.

**Step 2:** Like charges repel, so the layers push apart and the crystal fractures along that plane — it cannot deform without creating repulsion.

**Step 3 — $\ce{Cu}$:** In a metal, cation cores sit in a delocalized electron sea. When layers of $\ce{Cu}$ cations shift, the sea redistributes around the new arrangement; every cation is still surrounded by electron density, so no repulsive alignment ever occurs.

**Answer:** **$\ce{NaCl}$ shatters because shifting layers aligns like charges, which repel; $\ce{Cu}$ deforms because the electron sea re-flows around displaced cations, so metallic bonding survives the shift.**

### Example 2: Ranking Ionic Melting Points

**Problem:** Rank $\ce{NaCl}$, $\ce{MgO}$, and $\ce{KBr}$ from lowest to highest melting point. Justify with Coulomb's law.

**Solution:**

**Step 1 — Charges first.** $E \propto \frac{|q_1 q_2|}{r}$. $\ce{MgO}$ is $(2+)(2-)$: $|q_1q_2| = 4$. $\ce{NaCl}$ and $\ce{KBr}$ are both $(1+)(1-)$: $|q_1q_2| = 1$. So $\ce{MgO}$ is far above both.

**Step 2 — Then radius.** $\ce{K+}$ is larger than $\ce{Na+}$, and $\ce{Br-}$ is larger than $\ce{Cl-}$, so the interionic distance $r$ is larger in $\ce{KBr}$ → weaker attraction → lower melting point than $\ce{NaCl}$.

**Step 3 — Reality check.** Actual values: $\ce{KBr}$ 734°C < $\ce{NaCl}$ 801°C ≪ $\ce{MgO}$ 2852°C. Charge dominates, radius fine-tunes.

**Answer:** **$\ce{KBr} < \ce{NaCl} < \ce{MgO}$ — higher charge product (then smaller interionic distance) means stronger Coulombic attraction and a higher melting point.**

### Example 3: The Conductivity Fingerprint

**Problem:** Solid $\ce{KCl}$ does not conduct electricity. Molten $\ce{KCl}$ and aqueous $\ce{KCl}$ both conduct well. Explain all three observations with one principle.

**Solution:**

**Step 1 — The principle:** conduction requires **mobile charged particles**.

**Step 2 — Solid:** $\ce{K+}$ and $\ce{Cl-}$ are charged, but each is locked in a fixed lattice position by its oppositely charged neighbors. Charges present, mobility absent → no conduction. (The seated crowd can't do the wave one seat at a time — no one can leave their seat.)

**Step 3 — Molten:** heating past 770°C breaks down the lattice; the ions themselves flow and carry charge.

**Step 4 — Aqueous:** $\ce{KCl(s) -> K+(aq) + Cl-(aq)}$ — water separates the ions, which then move freely.

**Answer:** **Conduction needs mobile charged particles: in the solid the ions are fixed in the lattice; melting or dissolving frees the ions to move and carry charge.**

### Example 4: Na vs Mg vs Al

**Problem:** Melting points: $\ce{Na}$ = 98°C, $\ce{Mg}$ = 650°C, $\ce{Al}$ = 660°C. Explain the trend using the electron-sea model.

**Solution:**

**Step 1:** Each metal contributes its valence electrons to the sea: $\ce{Na}$ gives 1, $\ce{Mg}$ gives 2, $\ce{Al}$ gives 3. More electrons → denser sea → more "glue."

**Step 2:** The cation cores grow in charge and shrink in size across the period: $\ce{Na+}$ (large, 1+) → $\ce{Mg^2+}$ → $\ce{Al^3+}$ (small, 3+). By $E \propto \frac{|q_1 q_2|}{r}$, higher core charge and shorter distance both strengthen the attraction to the sea.

**Step 3:** Stronger cation–sea attraction → more energy needed to loosen the lattice → higher melting point. The huge jump is from $\ce{Na}$ to $\ce{Mg}$ (98 → 650°C); $\ce{Al}$'s edge over $\ce{Mg}$ shows up more dramatically in hardness and boiling point (2519°C vs 1091°C).

**Answer:** **Melting point rises from $\ce{Na}$ to $\ce{Mg}$ to $\ce{Al}$ because each successive metal puts more valence electrons into the sea AND has a smaller, more highly charged cation — both effects strengthen the Coulombic attraction holding the lattice together.**

### Example 5: Predicting Alloy Type — Brass

**Problem:** Atomic radii: $\ce{Cu}$ = 128 pm, $\ce{Zn}$ = 134 pm. Predict the type of alloy zinc forms with copper, and justify.

**Solution:**

**Step 1 — Compare the radii.** $\frac{134 - 128}{128} \times 100\% \approx 4.7\%$ — nearly the same size.

**Step 2 — Apply the rule.** Similar radii (within ~15%) → the added atom can occupy a regular lattice position in place of a host atom.

**Step 3 — Name it.** $\ce{Zn}$ atoms substitute for $\ce{Cu}$ atoms throughout the lattice: a substitutional alloy — brass. (Same-size visitors take regular seats.)

**Answer:** **Substitutional alloy — $\ce{Zn}$ and $\ce{Cu}$ atoms are within ~5% in radius, so $\ce{Zn}$ replaces $\ce{Cu}$ at lattice positions.**

### Example 6: Predicting Alloy Type — Steel

**Problem:** Atomic radii: $\ce{Fe}$ = 126 pm, $\ce{C}$ = 77 pm. Predict the type of alloy carbon forms with iron, and justify.

**Solution:**

**Step 1 — Compare the radii.** $\frac{77}{126} \approx 0.61$ — carbon is only about 61% the size of iron, far outside the "similar size" window.

**Step 2 — Apply the rule.** An atom that small cannot substitute cleanly, but it CAN fit into the interstices — the gaps between iron atoms in the lattice.

**Step 3 — Name it.** Carbon occupies interstitial holes between $\ce{Fe}$ atoms: an interstitial alloy — steel. (Little kids slipping into the gaps between adults.)

**Answer:** **Interstitial alloy — $\ce{C}$ is much smaller than $\ce{Fe}$ (~61% of its radius), so carbon atoms fit into the holes between iron atoms rather than replacing them.**

### Example 7: Why Steel Beats Pure Iron

**Problem:** Steel (iron + a few percent carbon) is significantly harder and less malleable than pure iron. Explain using the structures of both solids.

**Solution:**

**Step 1 — Pure iron:** identical $\ce{Fe}$ layers slide past one another with relative ease while the electron sea re-flows — that's why pure iron is malleable.

**Step 2 — Add carbon:** the small $\ce{C}$ atoms sit in the interstices *between* iron layers. When a force tries to slide one layer over the next, the carbon atoms physically obstruct the motion — they **pin adjacent layers together**.

**Step 3 — Stadium check:** the aisles used to be empty, so rows of the crowd could shuffle past each other. Now kids fill every gap — the shuffle jams.

**Answer:** **Interstitial carbon atoms disrupt the slip planes of the iron lattice, pinning layers so they cannot slide past each other; deformation gets harder, so steel is harder and less malleable than pure iron.**

### Example 8: Sterling Silver

**Problem:** Sterling silver is 92.5% $\ce{Ag}$ (radius 144 pm) and 7.5% $\ce{Cu}$ (radius 128 pm). (a) What type of alloy is it? (b) Why is it harder than pure silver? (c) Does it still conduct electricity?

**Solution:**

**Step 1 — (a):** $\frac{144 - 128}{144} \times 100\% \approx 11\%$ — within the ~15% similarity window, so $\ce{Cu}$ substitutes for $\ce{Ag}$ at lattice positions: **substitutional alloy**.

**Step 2 — (b):** The slightly smaller $\ce{Cu}$ atoms make the silver layers uneven; sliding planes catch on the size mismatch instead of gliding smoothly. Harder to deform → harder metal. That's why jewelry is sterling rather than pure (too-soft) silver.

**Step 3 — (c):** The alloy is still metallic — the delocalized electron sea is intact — so yes, it conducts as a solid.

**Answer:** **(a) Substitutional (radii within ~11%); (b) mismatched atom sizes disrupt the slip planes, so layers can't slide as easily; (c) yes — the electron sea remains, so sterling silver conducts.**

### Example 9: The Classic Data-Table Classification

**Problem:** Identify the solid type of each substance and justify:

| Substance | Melting point | Conducts as solid? | Conducts molten? |
|---|---|---|---|
| W | 801°C | No | Yes |
| X | 1085°C | Yes | Yes |
| Y | 115°C | No | No |
| Z | 1610°C | No | No |

**Solution:**

**Step 1 — W:** nonconductor as a solid but conductor when molten — the ionic fingerprint. Ions locked in the lattice, freed by melting. **Ionic** (it's $\ce{NaCl}$).

**Step 2 — X:** conducts *as a solid* — only delocalized electrons can do that. **Metallic** (it's $\ce{Cu}$).

**Step 3 — Y:** never conducts and melts at a low 115°C — discrete molecules held by weak intermolecular forces. **Molecular covalent** (it's sulfur, $\ce{S8}$).

**Step 4 — Z:** never conducts, yet the melting point is enormous — melting must break covalent bonds throughout a network. **Network covalent** (it's quartz, $\ce{SiO2}$).

**Answer:** **W ionic (conducts only when molten), X metallic (conducts as solid), Y molecular covalent (low mp, never conducts), Z network covalent (very high mp, never conducts).**

### Example 10: Particulate Diagrams of Alloys

**Problem:** Diagram 1 shows a lattice of large spheres with a few *equal-size* spheres of a different shade at lattice positions. Diagram 2 shows the same lattice with *tiny* spheres tucked between the large ones. Match each diagram to brass or steel, and to an alloy type.

**Solution:**

**Step 1 — Diagram 1:** foreign atoms the same size, sitting AT lattice positions → substitution. Same-size atoms = $\ce{Cu}$/$\ce{Zn}$ → **brass, substitutional**.

**Step 2 — Diagram 2:** foreign atoms much smaller, sitting BETWEEN lattice positions → interstitial. Tiny atom in an iron lattice = $\ce{C}$ in $\ce{Fe}$ → **steel, interstitial**.

**Step 3 — AP habit:** on particulate-diagram questions, always name BOTH the location (at vs between lattice sites) and the relative size — that's the reasoning the rubric wants.

**Answer:** **Diagram 1 = brass, substitutional (similar-size atoms replace host atoms at lattice sites); Diagram 2 = steel, interstitial (much smaller atoms occupy gaps between host atoms).**

### Example 11: Why Metals Conduct but Ionic Solids Don't

**Problem:** Both solid copper and solid $\ce{NaCl}$ are full of charged particles. Only copper conducts electricity. Resolve the paradox.

**Solution:**

**Step 1:** Conduction requires charged particles that are **mobile**, not merely present.

**Step 2 — Copper:** the charged particles that move are not the $\ce{Cu^2+}$-like cores (those are fixed) but the **delocalized valence electrons**, free to drift through the entire crystal the moment a voltage is applied.

**Step 3 — $\ce{NaCl}$:** every electron is localized on a specific ion, and every ion is fixed in the lattice. Nothing charged can travel.

**Answer:** **Copper conducts because its valence electrons are delocalized and mobile; solid $\ce{NaCl}$ does not because its ions (and their electrons) are locked in fixed lattice positions — charge without mobility can't carry current.**

### Example 12: Choosing an Alloying Element from a Radii Table

**Problem:** A metallurgist wants a *substitutional* alloy of iron ($\ce{Fe}$, 126 pm). Candidates: $\ce{Ni}$ (124 pm), $\ce{C}$ (77 pm), $\ce{H}$ (37 pm). Which element should she choose, and what would the other two form instead?

**Solution:**

**Step 1 — Test each ratio against iron.** $\ce{Ni}$: $\frac{126-124}{126} \approx 1.6\%$ — essentially identical. $\ce{C}$: $77/126 \approx 61\%$ of iron's radius. $\ce{H}$: $37/126 \approx 29\%$ — tiny.

**Step 2 — Apply the rules.** Substitutional needs similar radii → $\ce{Ni}$ qualifies (this is real: stainless steels contain substitutional nickel and chromium). $\ce{C}$ and $\ce{H}$ are far too small to substitute — they would slot into interstices.

**Answer:** **Choose $\ce{Ni}$ (radius within ~2% of $\ce{Fe}$ → substitutional). $\ce{C}$ and $\ce{H}$ are much smaller than $\ce{Fe}$ and would form interstitial alloys instead.**

---

## Common Mistakes

| The mistake | Why it happens | How to avoid it |
|---|---|---|
| "Ionic solids are brittle because ionic bonds are weak" | Confusing brittleness with weakness | The bonds are STRONG (high mp!). Brittleness is about *geometry*: shifting aligns like charges, which repel. Strong and brittle coexist. |
| "Solid $\ce{NaCl}$ conducts because it contains ions" | Forgetting that conduction needs *mobile* charge | Always write both words: charged **and** mobile. Solid = locked seats; molten/aqueous = free to move. |
| Saying metals are "sharing electrons like covalent bonds" | Blurring the bonding models | Metallic electrons are **delocalized over the whole crystal**, not shared between two specific atoms. Say "electron sea." |
| "Alloys are compounds like $\ce{CuZn}$" | Treating an alloy as a fixed-formula substance | Alloys are **mixtures** — compositions vary (brass can be 5–40% zinc). No subscripts, no formula units. |
| Guessing alloy type without using the radii | Skipping the data the question hands you | Compute the comparison: within ~15% → substitutional; much smaller (≲60% of host) → interstitial. Cite the numbers. |
| "Diamond has high melting point because of strong intermolecular forces" | Mixing up network and molecular solids | Diamond has NO molecules — melting breaks actual **covalent bonds** throughout the network. Reserve "intermolecular" for molecular solids (Unit 3). |
| Explaining metallic melting trends by atomic mass | Reaching for the easiest number in the table | Mass is irrelevant. Use valence electrons contributed + cation charge and size — Coulomb, always Coulomb. |

---

## AP Exam Tips

- **Justify properties from STRUCTURE, not vibes.** "Ionic solids are brittle" earns nothing. "When a force displaces one layer of the ionic lattice, ions of like charge align and repel, fracturing the crystal along that plane" earns the point. Every property answer should name the particles, the force, and what moves (or can't).
- **Conductivity conditions are the fingerprint.** A table showing "no as solid / yes when molten" is the College Board announcing IONIC. "Yes as solid" announces METALLIC. "No in every state" splits into molecular (low mp) vs network covalent (huge mp). Memorize the algorithm in the master table above.
- **Alloy questions almost always hand you a radii table.** Use it explicitly: quote both radii, compare them, then conclude substitutional (similar) or interstitial (much smaller). An answer that never cites the numbers usually misses the reasoning point.
- **"Explain why the alloy is harder"** wants the slip-plane sentence: foreign atoms (substituted or interstitial) disrupt the regular layers so they can no longer slide past one another easily.
- **Electron-sea trend questions ($\ce{Na}$ vs $\ce{Mg}$ vs $\ce{Al}$)** want TWO factors: more valence electrons donated to the sea, and a smaller/more-highly-charged cation. Give both.
- **Vocabulary that costs points if sloppy:** ionic compounds come in *formula units*, not molecules; electrons in metals are *delocalized*; alloys are *mixtures*. Say "Coulombic attraction," not "the atoms want to stick."
- This topic is FRQ gold — particulate diagrams of alloys and property-classification tables appear constantly in Section II. Practice writing three-sentence structural justifications until they're automatic.

---

## Practice Problems

### Problem 1
Classify each solid as ionic, metallic, molecular covalent, or network covalent: (a) $\ce{MgCl2}$, (b) brass, (c) diamond, (d) dry ice ($\ce{CO2}$).

<details>
<summary><strong>Solution</strong></summary>

(a) $\ce{MgCl2}$ — metal cation + nonmetal anion in a lattice → **ionic**.

(b) Brass — a $\ce{Cu}$/$\ce{Zn}$ mixture with an intact electron sea → **metallic** (a substitutional alloy).

(c) Diamond — carbon atoms covalently bonded in an endless 3D network → **network covalent**.

(d) Dry ice — discrete $\ce{CO2}$ molecules held together by weak intermolecular forces → **molecular covalent**.

**Answer: (a) ionic, (b) metallic (substitutional alloy), (c) network covalent, (d) molecular covalent.**

</details>

### Problem 2
Rank $\ce{NaF}$, $\ce{MgO}$, and $\ce{KCl}$ from lowest to highest melting point and justify with Coulomb's law.

<details>
<summary><strong>Solution</strong></summary>

Charges first: $\ce{MgO}$ is $(2+)(2-)$, charge product 4; $\ce{NaF}$ and $\ce{KCl}$ are $(1+)(1-)$, charge product 1. $\ce{MgO}$ is highest by far.

Radius next: $\ce{K+}$ > $\ce{Na+}$ and $\ce{Cl-}$ > $\ce{F-}$, so $\ce{KCl}$ has the larger interionic distance $r$ → weaker attraction → lower melting point than $\ce{NaF}$.

(Actual values: $\ce{KCl}$ 770°C < $\ce{NaF}$ 993°C < $\ce{MgO}$ 2852°C.)

**Answer: $\ce{KCl} < \ce{NaF} < \ce{MgO}$ — larger charge product, then smaller interionic distance, gives stronger Coulombic attraction ($E \propto |q_1q_2|/r$) and a higher melting point.**

</details>

### Problem 3
A student melts $\ce{KBr}$ in a crucible and finds that the liquid conducts electricity, though the solid did not. Explain both observations.

<details>
<summary><strong>Solution</strong></summary>

Conduction requires mobile charged particles.

Solid $\ce{KBr}$: the $\ce{K+}$ and $\ce{Br-}$ ions are charged but held in fixed positions in the lattice by Coulombic attraction to their oppositely charged neighbors — no mobility, no conduction.

Molten $\ce{KBr}$: melting breaks down the lattice; the ions themselves are now free to move and carry charge through the liquid.

**Answer: The ions are immobile in the solid lattice but become mobile charge carriers when the lattice is destroyed by melting.**

</details>

### Problem 4
Bronze is an alloy of $\ce{Cu}$ (radius 128 pm) and $\ce{Sn}$ (radius 140 pm). Predict its type and justify with the radii.

<details>
<summary><strong>Solution</strong></summary>

Compare radii: $\frac{140 - 128}{128} \times 100\% \approx 9\%$ — similar sizes, within the ~15% window.

Similar-size atoms occupy regular lattice positions in place of host atoms.

**Answer: Substitutional alloy — $\ce{Sn}$ atoms (within ~9% of copper's radius) replace $\ce{Cu}$ atoms at lattice sites.**

</details>

### Problem 5
Titanium nitride is used to coat drill bits. Radii: $\ce{Ti}$ = 147 pm, $\ce{N}$ = 75 pm. If nitrogen atoms are incorporated into the titanium lattice, what type of alloy results? Why does the coating resist deformation?

<details>
<summary><strong>Solution</strong></summary>

Compare radii: $75/147 \approx 51\%$ — nitrogen is about half titanium's size, far too small to substitute.

The small $\ce{N}$ atoms occupy interstitial holes between $\ce{Ti}$ atoms → **interstitial alloy**.

Hardness: the interstitial atoms pin adjacent titanium layers, preventing them from sliding past one another, so the material resists deformation — ideal for a cutting surface.

**Answer: Interstitial — $\ce{N}$ (~51% of Ti's radius) fills gaps between $\ce{Ti}$ atoms and pins the slip planes, making the coating very hard.**

</details>

### Problem 6
Explain, using the electron-sea model, why a gold ring can be resized by bending without breaking.

<details>
<summary><strong>Solution</strong></summary>

Gold consists of $\ce{Au}$ cation cores in a sea of delocalized valence electrons.

When the jeweler bends the ring, layers of gold cations slide to new positions — but the electron sea immediately redistributes around them. Every cation stays surrounded by electron density, so the metallic bonding is maintained in the new shape; no like-charge alignment ever occurs.

**Answer: The delocalized electron sea re-flows around displaced cations, so gold deforms (malleable/ductile) instead of fracturing.**

</details>

### Problem 7
Pure gold is 24-karat; 14-karat gold is roughly 58% $\ce{Au}$ (radius 144 pm) alloyed with metals such as $\ce{Cu}$ (radius 128 pm). Why is 14-karat gold the better choice for everyday jewelry?

<details>
<summary><strong>Solution</strong></summary>

Radius check: $\frac{144-128}{144} \approx 11\%$ → copper forms a **substitutional** alloy with gold.

Pure gold's identical layers slide past each other very easily, so it scratches and bends — too soft for daily wear.

In 14-karat gold, the smaller $\ce{Cu}$ atoms at lattice sites make the layers uneven; slip planes catch on the size mismatch and can no longer glide smoothly. The alloy is harder and holds its shape.

**Answer: Substituted copper atoms disrupt the sliding planes of the gold lattice, making 14-karat gold significantly harder (and more scratch-resistant) than soft pure gold.**

</details>

### Problem 8
Sodium melts at 98°C; magnesium melts at 650°C. Give a two-part structural explanation.

<details>
<summary><strong>Solution</strong></summary>

Part 1 — sea density: each $\ce{Mg}$ atom contributes 2 valence electrons to the delocalized sea versus 1 from $\ce{Na}$, so magnesium's sea is denser.

Part 2 — cation: $\ce{Mg^2+}$ carries twice the charge of $\ce{Na+}$ and is smaller, so by $E \propto |q_1q_2|/r$ the attraction between cores and sea is much stronger.

Stronger metallic bonding → far more thermal energy needed to loosen the lattice.

**Answer: $\ce{Mg}$ has more valence electrons in the electron sea AND a smaller, more highly charged cation, so its metallic bonds are stronger and its melting point is much higher.**

</details>

### Problem 9
An unknown white solid melts at 996°C, does not conduct electricity as a solid, but conducts well when dissolved in water. Identify the solid type and justify.

<details>
<summary><strong>Solution</strong></summary>

High melting point → strong forces between particles. Nonconductor as a solid but conductor in solution → charged particles exist but are only mobile once freed from the lattice.

That combination — conduction ONLY when molten or dissolved — is the ionic fingerprint. (The solid is $\ce{NaF}$.)

**Answer: Ionic solid — the high melting point reflects strong Coulombic attractions, and conduction only in solution shows the charge carriers are ions that are locked in the solid lattice but mobile when dissolved.**

</details>

### Problem 10
A hammer blow flattens an aluminum can but shatters a rock-salt crystal. In one or two sentences each, connect both outcomes to what happens along the slip plane.

<details>
<summary><strong>Solution</strong></summary>

Aluminum: displaced layers of $\ce{Al^3+}$ cores remain surrounded by the delocalized electron sea, which re-flows around the new arrangement — bonding survives the slip, so the metal dents.

Rock salt: displacing a layer by one ion position puts $\ce{Na+}$ next to $\ce{Na+}$ and $\ce{Cl-}$ next to $\ce{Cl-}$ across the slip plane; the like-charge repulsion drives the layers apart and the crystal fractures.

**Answer: The metal's electron sea accommodates the slip (malleable); the ionic lattice's slip aligns like charges that repel (brittle fracture).**

</details>

### Problem 11
Which of the following conduct electricity in the solid state: $\ce{KCl}$, $\ce{Cu}$, $\ce{S8}$, $\ce{SiO2}$? Explain each briefly.

<details>
<summary><strong>Solution</strong></summary>

$\ce{KCl}$ — no: ions are fixed at lattice positions (would conduct molten/aqueous).

$\ce{Cu}$ — **yes**: delocalized valence electrons are mobile throughout the solid.

$\ce{S8}$ — no: neutral molecules, no charged particles at all; electrons localized in bonds.

$\ce{SiO2}$ — no: all electrons locked in covalent bonds throughout the network; no ions, no free electrons.

**Answer: Only $\ce{Cu}$ — it alone has mobile charge carriers (delocalized electrons) in the solid state.**

</details>

### Problem 12
Palladium metal ($\ce{Pd}$, radius 137 pm) can absorb large amounts of hydrogen ($\ce{H}$, radius 37 pm) into its lattice. What type of alloy forms, and why doesn't hydrogen substitute for palladium atoms?

<details>
<summary><strong>Solution</strong></summary>

Radius comparison: $37/137 \approx 27\%$ — hydrogen is nowhere near palladium's size.

Substitution requires atoms of similar radius so the lattice geometry is preserved; an atom that small would leave a huge, unstable hole at a lattice site. Instead, hydrogen slips into the interstitial holes that already exist between $\ce{Pd}$ atoms.

**Answer: Interstitial alloy — at ~27% of palladium's radius, $\ce{H}$ atoms occupy the gaps between $\ce{Pd}$ atoms rather than lattice positions.**

</details>

### Problem 13
Complete the comparison: for $\ce{NaCl}$ and $\ce{Cu}$, state whether each conducts (i) as a solid, (ii) molten, (iii) dissolved in water — and name the mobile species in every "yes."

<details>
<summary><strong>Solution</strong></summary>

$\ce{NaCl}$: (i) solid — no (ions fixed); (ii) molten — yes, mobile species = $\ce{Na+}$ and $\ce{Cl-}$ ions; (iii) aqueous — yes, mobile species = hydrated $\ce{Na+}$ and $\ce{Cl-}$ ions.

$\ce{Cu}$: (i) solid — yes, mobile species = delocalized valence electrons; (ii) molten — yes, still the electrons; (iii) copper does not dissolve in water, so (iii) doesn't apply.

**Answer: $\ce{NaCl}$ conducts only molten or aqueous (via mobile ions); $\ce{Cu}$ conducts as a solid and liquid (via delocalized electrons).**

</details>

### Problem 14
A data table gives four solids: A melts at −78°C and never conducts; B melts at 1538°C and conducts in all states; C melts at 2072°C and conducts only when molten; D sublimes intact and never conducts, but survives to over 3500°C before subliming. Classify A–D.

<details>
<summary><strong>Solution</strong></summary>

A — very low melting point, never conducts → discrete molecules, weak forces between them → **molecular covalent** (dry ice, $\ce{CO2}$).

B — conducts as a solid → **metallic** (iron).

C — very high melting point, conducts ONLY molten → ions freed by melting → **ionic** ($\ce{Al2O3}$).

D — never conducts, stable to extreme temperature → covalent bonds throughout → **network covalent** (graphite is the conducting exception, so this one is diamond-like).

**Answer: A molecular covalent, B metallic, C ionic, D network covalent.**

</details>

### Problem 15
FRQ-style: A materials lab wants to strengthen iron ($\ce{Fe}$, 126 pm) two different ways. Available additives: $\ce{Cr}$ (128 pm), $\ce{C}$ (77 pm). (a) Which additive gives a substitutional alloy and which gives an interstitial alloy? Cite the radii. (b) Explain why BOTH alloys are harder than pure iron.

<details>
<summary><strong>Solution</strong></summary>

(a) $\ce{Cr}$: $\frac{128-126}{126} \approx 1.6\%$ — nearly identical radius → substitutes for $\ce{Fe}$ at lattice positions → **substitutional** (this is the chromium in stainless steel). $\ce{C}$: $77/126 \approx 61\%$ of iron's radius → far too small to substitute; fits into the holes between $\ce{Fe}$ atoms → **interstitial** (carbon steel).

(b) Both additives disrupt the slip planes of the iron lattice. Substitutional $\ce{Cr}$ atoms introduce slight size irregularities that keep layers from gliding smoothly; interstitial $\ce{C}$ atoms sit between layers and pin them together. In both cases the layers of iron atoms can no longer slide past one another easily, so the alloy resists deformation more than pure iron.

**Answer: (a) $\ce{Cr}$ → substitutional (radii within ~2%); $\ce{C}$ → interstitial (~61% of iron's radius, fits in gaps). (b) Both foreign atoms obstruct the sliding of iron layers — irregular substituted atoms roughen the slip planes and interstitial carbon pins layers together — so both alloys are harder than pure iron.**

</details>

---

## Quick Reference

| Concept | The one-liner |
|---|---|
| Ionic solid structure | 3D lattice of alternating cations and anions; maximizes attraction, minimizes repulsion ($E \propto \|q_1q_2\|/r$) |
| Ionic brittleness | Shifting a layer aligns like charges → repulsion → fracture along the plane |
| Ionic conductivity | Solid: NO (ions fixed). Molten/aqueous: YES (ions mobile) — the fingerprint |
| Metallic solid structure | Cation cores in a sea of delocalized valence electrons |
| Metallic malleability | Electron sea re-flows around displaced cations — deforms, never shatters |
| Metallic conductivity | YES as a solid — delocalized electrons are mobile |
| Metallic bond strength | More valence e⁻ in the sea + smaller, higher-charge cation → stronger ($\ce{Na} < \ce{Mg} < \ce{Al}$) |
| Substitutional alloy | Similar radii (within ~15%) → replaces host atoms at lattice sites — brass ($\ce{Cu}$/$\ce{Zn}$), sterling silver, bronze |
| Interstitial alloy | Much smaller atom (≲60% of host radius) → fills gaps — steel ($\ce{Fe}$/$\ce{C}$) |
| Why alloys are harder | Foreign atoms disrupt/pin the slip planes so layers can't slide |
| Molecular covalent (Unit 3 teaser) | Discrete molecules, weak forces between them → low mp, never conducts |
| Network covalent | Covalent bonds throughout (diamond, $\ce{SiO2}$) → extreme mp, never conducts (except graphite) |
| Classification algorithm | Conducts solid → metallic; conducts only molten/aq → ionic; never conducts: low mp → molecular, huge mp → network |

---

<div align="center">

[← Bond Energy and Length](/chemistry/0402-bond-energy-and-length) | [Lewis Structures →](/chemistry/0404-lewis-structures)

</div>
