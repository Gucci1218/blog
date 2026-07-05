# Bonds and Electronegativity
<p class="article-date">July 4, 2026</p>

*My friend Maya and I split a plate of fries after practice last week — one plate, two forks, \$4.50 between us — and I realized there are exactly three ways that can go. Way one: we're equally hungry, the plate sits dead center, and we eat evenly. Way two: Maya skipped lunch, so the plate drifts toward her side of the table — I still get fries, but she's clearly getting more. Way three: she's ravenous, I'm full, and she just slides the entire plate to her side. Same plate, same table, three totally different outcomes — and the only thing that decided which one happened was how hungry each of us was. Atoms sharing electrons play this exact game: equal hunger means equal sharing (nonpolar covalent), a hunger gap means lopsided sharing (polar covalent), and a huge hunger gap means the plate just gets taken (ionic). "Electron hunger" has a real name — electronegativity — and the hunger gap, $\Delta EN$, is the single number that places every bond on a smooth spectrum from even split to total plate theft. This is Topic 2.1, the official start of AP Unit 2, and it's the upgrade of everything we built in the foundations article: the clean ionic-vs-covalent boxes are about to melt into a continuum.*

---

## What You'll Learn
- Explain electronegativity in Coulomb terms — protons, distance, shielding — and state its periodic trends (with $\ce{F}$ as the reigning champion)
- Compute $\Delta EN$ for any bond and place it on the **bonding continuum**: nonpolar covalent → polar covalent → ionic
- Use the $\Delta EN$ guideposts ($< 0.4$, $0.4\text{–}1.7$, $> 1.7$) *and* explain why they're guideposts, not laws — and why "metal + nonmetal?" is the better first check
- Label partial charges $\delta+$ and $\delta-$ on a polar bond and draw the dipole arrow toward the more electronegative atom
- Rank a set of bonds by polarity and identify the most/least polar bond within a molecule
- Classify the bonding in real compounds — including gotchas like $\ce{NH4Cl}$ (both bond types in one compound) and metalloid boundary cases
- Describe metallic bonding as a "sea of electrons" and use it to predict conductivity and malleability
- Classify an unknown solid as ionic, molecular, metallic, or covalent-network from melting point and conductivity data — a genuine AP question type
- Write a full-credit AP justification for bond type using electronegativity data, not just periodic-table position

---

## Prerequisites
- [Ionic vs Covalent](/chemistry/0203-ionic-vs-covalent) — the foundations version of this story: transfer vs. sharing, lattices vs. molecules. This article is the AP-level upgrade of that one, so read it first
- [Periodic Trends](/chemistry/0305-periodic-trends) — electronegativity is a periodic trend, and we'll reuse the **protons–distance–shielding** checklist constantly

---

## The Core Concept

### Intuition First

Back to the fries. Let's make the analogy do real structural work, piece by piece:

| Fries at the table | Bonding | What it controls |
|---|---|---|
| The **plate of fries** | The **shared electron pair** (electron density) | The thing both atoms want |
| Each person's **hunger** | Each atom's **electronegativity (EN)** | How hard each nucleus pulls on the shared pair |
| The **hunger difference** | $\Delta EN$ (bigger EN minus smaller EN) | Decides how lopsided the sharing gets |
| The **plate's position** on the table | Where the **electron density** sits between the nuclei | Centered → nonpolar; shifted → polar; gone → ionic |
| **Even split → hogging → plate theft** | **Nonpolar covalent → polar covalent → ionic** | One smooth spectrum, not three boxes |

Here's the Unit 2 mindset shift, and it's the whole point of this article. In [Ionic vs Covalent](/chemistry/0203-ionic-vs-covalent), we treated bonding like a fork in the road: transfer *or* share, ionic *or* covalent, pick one. That was the right training-wheels version. But watch the fries carefully: there's no magic moment where "Maya is eating slightly more" suddenly becomes "Maya took the plate." The plate slides *continuously*. A tiny hunger gap shifts it a little. A bigger gap shifts it more. At some point the shift is so extreme that calling it "sharing" is silly — the fries are just hers — but that point is a judgment call, not a wall.

**Bonding is a continuum.** Every real bond lives somewhere on this slider:

$$\underbrace{\ce{Cl-Cl}}_{\text{plate centered}} \quad \longrightarrow \quad \underbrace{\ce{H-Cl}}_{\text{plate drifting}} \quad \longrightarrow \quad \underbrace{\ce{Na+ Cl-}}_{\text{plate stolen}}$$

Even $\ce{NaCl}$, the poster child of ionic bonding, isn't a *perfect* 100% transfer — it's about as close as bonds get, but a sliver of sharing remains. That's why AP questions say a bond has "**mostly ionic character**" or "significant covalent character" instead of slamming it into a box. The exam wants you thinking in percentages of plate theft, not in categories.

### Electronegativity: Hunger, Measured

**Electronegativity (EN)** is the ability of an atom *in a bond* to attract the shared electron pair toward itself. It's measured on the Pauling scale, which runs from about 0.7 (cesium, barely hungry) to 4.0 (fluorine, the hungriest atom in the universe — the undisputed champion).

Why is fluorine the champ? Run the [Periodic Trends](/chemistry/0305-periodic-trends) checklist — **protons, distance, shielding**:

- **Protons:** fluorine has a high effective nuclear charge ($Z_{eff} \approx +7$) for its size — lots of pull.
- **Distance:** its valence shell is $n = 2$, extremely close to the nucleus. Coulomb's law ($F \propto \frac{q_1 q_2}{r^2}$) says short distance = ferocious attraction.
- **Shielding:** only 2 core electrons stand in the way. Almost nothing blocks the pull.

High pull, short rope, few blockers: a bonding pair parked next to fluorine gets yanked hard. Same logic, run in reverse, explains cesium: low $Z_{eff}$ on the valence shell, enormous distance, tons of shielding — it barely tugs on shared electrons at all.

**The trends** (same directions as ionization energy, for the same Coulombic reasons):

- **Across a period (left → right): EN increases.** More protons, same shell, same shielding → stronger pull on bonding electrons.
- **Down a group (top → bottom): EN decreases.** The valence shell gets farther away and more core electrons shield → weaker pull.
- **Grand conclusion:** EN peaks at the **top right** ($\ce{F} > \ce{O} > \ce{Cl} \approx \ce{N}$) and bottoms out at the **bottom left** ($\ce{Cs}$, $\ce{Fr}$). Noble gases usually sit out — they rarely bond, so they mostly don't get an EN value.

Values worth having in your head (Pauling scale):

| Atom | $\ce{F}$ | $\ce{O}$ | $\ce{Cl}$, $\ce{N}$ | $\ce{Br}$ | $\ce{C}$, $\ce{S}$, $\ce{I}$ | $\ce{H}$ | $\ce{Si}$ | $\ce{Al}$ | $\ce{Mg}$ | $\ce{Ca}$ | $\ce{Na}$ | $\ce{K}$ |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| EN | 4.0 | 3.5 | 3.0 | 2.8 | 2.5 | 2.1 | 1.8 | 1.5 | 1.2 | 1.0 | 0.9 | 0.8 |

You do **not** need to memorize these for the exam — EN data is given when needed. But knowing the *ordering* ($\ce{F} > \ce{O} > \ce{Cl}/\ce{N} > \ce{Br} > \ce{C} > \ce{H} > \text{metals}$) lets you sanity-check everything.

### The $\Delta EN$ Ruler (and Its Honest Fine Print)

To place a bond on the continuum, subtract the two electronegativities (big minus small — $\Delta EN$ is always positive) and read the guideposts:

$$\Delta EN = |EN_1 - EN_2|$$

| $\Delta EN$ | Bond type | Fries version | Example |
|---|---|---|---|
| $< 0.4$ | **Nonpolar covalent** | Even split — plate centered | $\ce{Cl-Cl}$ ($0$), $\ce{C-H}$ ($0.4$) |
| $0.4$ – $1.7$ | **Polar covalent** | Hogging — plate drifts | $\ce{H-Cl}$ ($0.9$), $\ce{O-H}$ ($1.4$) |
| $> 1.7$ | **Mostly ionic** | Plate theft | $\ce{NaCl}$ ($2.1$), $\ce{CaO}$ ($2.5$) |

**Now the AP-level fine print, and this matters:** those cutoffs are **guideposts, not laws**. They're fence posts hammered into a smooth hillside. Two rules of engagement:

1. **"Metal + nonmetal?" is the better first check.** $\ce{HF}$ has $\Delta EN = 4.0 - 2.1 = 1.9$, which is above 1.7 — yet $\ce{HF}$ is a molecular gas made of discrete covalent molecules, because it's two *nonmetals* sharing. Meanwhile $\ce{AlCl3}$ (metal + nonmetal) has $\Delta EN = 1.5$ and genuinely shows significant covalent character. The composition check (metal + nonmetal → expect ionic; nonmetal + nonmetal → expect covalent; metal + metal → metallic) gets the *category* right; $\Delta EN$ then tells you *how far along the continuum* the bond sits within that category.
2. **Speak in "character."** The AP exam's own language is "the bond in $\ce{NaCl}$ has mostly ionic character" — not "is 100% ionic." Larger $\Delta EN$ → greater ionic character → the electron density sits more completely on one atom. That phrasing earns points; absolute categories can lose them.

### Polar Covalent Bonds: Partial Charges and the Dipole Arrow

When the plate drifts but isn't stolen, we mark who's winning. In $\ce{H-Cl}$, chlorine ($EN = 3.0$) out-pulls hydrogen ($EN = 2.1$), so the shared pair spends more time near $\ce{Cl}$:

$$\overset{\delta+}{\text{H}} - \overset{\delta-}{\text{Cl}}$$

- $\delta-$ (**partial negative**) goes on the **more electronegative** atom — extra electron density piled up on its side.
- $\delta+$ (**partial positive**) goes on the less electronegative atom — it's been partially stripped.
- These are *partial* charges — fractions of a full $+1$/$-1$. Maya is eating most of the fries; she hasn't taken the plate.

A bond with separated $\delta+$/$\delta-$ ends is a **bond dipole**. We draw it as an arrow with a little plus sign on its tail, pointing **from the $\delta+$ atom toward the $\delta-$ (more electronegative) atom** — the arrow points where the electron density went, i.e., toward whoever's hogging the plate:

$$\text{H} \;\xrightarrow{\quad}\; \text{Cl} \qquad \text{(tail crossed at H: } \delta+ \text{; head at Cl: } \delta-\text{)}$$

Benchmarks to internalize:

| Bond | $\Delta EN$ | Verdict |
|---|---|---|
| $\ce{O-H}$ | $3.5 - 2.1 = 1.4$ | Very polar — the reason water does everything water does |
| $\ce{C-O}$ | $3.5 - 2.5 = 1.0$ | Solidly polar |
| $\ce{H-Cl}$ | $3.0 - 2.1 = 0.9$ | Polar |
| $\ce{C-H}$ | $2.5 - 2.1 = 0.4$ | Right on the fence — **treated as (nearly) nonpolar** in AP work |

That last row is a big deal: chemists (and the AP exam) treat $\ce{C-H}$ bonds as essentially nonpolar. It's why oils and fats — carbon-hydrogen skeletons — don't mix with water.

One more consequence for later: a molecule can contain polar *bonds* yet be a nonpolar *molecule* if the bond dipoles cancel by symmetry ($\ce{CO2}$ is the classic). That's the molecular-polarity story, and it gets its own article — here we care only about individual bonds.

### Metallic Bonding: The Communal Fry Pile

Two metals bonding is a third arrangement entirely — nobody transfers, nobody pairs up. Every metal atom tosses its valence electrons into a shared communal pile, becoming a lattice of **cations sitting in a delocalized "sea of electrons"** that belongs to the whole table at once, not to any pair of atoms.

Two famous properties fall straight out of this picture:

- **Electrical conductivity (even as a solid):** the sea electrons are mobile — apply a voltage and they flow. Ionic solids can't do this; their charges are locked in the lattice.
- **Malleability:** hammer a metal and the cation layers slide, but the electron sea flows around the new arrangement and keeps gluing everything together. No specific bond breaks, so the metal dents instead of shattering. (Hit an ionic crystal and like charges get shoved next to like charges → repulsion → it cracks.)

Alloys like brass ($\ce{Cu}$ + $\ce{Zn}$) are two metals sharing one electron sea. That's the headline version — the full story (lattice energy, interstitial vs. substitutional alloys) lives in [Ionic Solids, Metals, and Alloys](/chemistry/0403-ionic-solids-metals-alloys).

### Reading the Table Backwards: Properties → Bond Type

The AP exam loves running this article in reverse: instead of "predict the properties from the bond type," it hands you a data table and asks **"what kind of solid is this?"** Four suspects, four fingerprints:

| Solid type | Particles & glue | Melting point | Conducts as solid? | Conducts molten / dissolved? | Example |
|---|---|---|---|---|---|
| **Ionic** | Ions in a lattice; electrostatic attraction | High (hundreds of °C) | **No** (ions locked) | **Yes** (ions freed) | $\ce{NaCl}$, 801°C |
| **Molecular (covalent)** | Discrete molecules; weak forces *between* them | Low (often below ~200°C) | No | No | Ice, 0°C |
| **Metallic** | Cations in an electron sea | Varies (usually high) | **Yes** | Yes | $\ce{Cu}$, 1085°C |
| **Covalent-network** | Atoms covalently bonded in one giant lattice | Extremely high (1000s of °C) | No (graphite is the famous exception) | Doesn't dissolve | $\ce{SiO2}$ (quartz), ~1710°C |

The killer diagnostic is the **conductivity pattern**: conducts as a solid → metallic; conducts *only* when melted or dissolved → ionic; never conducts and melts low → molecular; never conducts and melts absurdly high → covalent-network. We'll drill this in the worked examples, because it's worth real FRQ points.

---

## Worked Examples

### Example 1: Placing a Bond on the Continuum

**Problem:** Using EN values $\ce{H} = 2.1$ and $\ce{Cl} = 3.0$, classify the bond in $\ce{HCl}$ and label the partial charges.

**Solution:**

**Step 1:** Composition check first: hydrogen and chlorine are both nonmetals → expect covalent sharing.

**Step 2:** Compute the hunger gap: $\Delta EN = 3.0 - 2.1 = 0.9$.

**Step 3:** Read the ruler: $0.4 < 0.9 < 1.7$ → polar covalent. The plate drifts toward chlorine but stays shared.

**Step 4:** Chlorine is more electronegative → $\delta-$ on $\ce{Cl}$, $\delta+$ on $\ce{H}$.

**Answer:** **Polar covalent**, written $\overset{\delta+}{\text{H}}-\overset{\delta-}{\text{Cl}}$, with the dipole arrow pointing toward $\ce{Cl}$.

### Example 2: The Even Split

**Problem:** Classify the bond in $\ce{Cl2}$.

**Solution:**

**Step 1:** Two chlorine atoms: identical hunger, $EN = 3.0$ for both.

**Step 2:** $\Delta EN = 3.0 - 3.0 = 0$. The plate sits exactly centered — neither atom can out-pull its identical twin.

**Step 3:** $0 < 0.4$ → nonpolar covalent. Every homonuclear diatomic ($\ce{H2}$, $\ce{N2}$, $\ce{O2}$, $\ce{F2}$, …) works this way.

**Answer:** **Nonpolar covalent** — perfectly equal sharing, no partial charges, no dipole.

### Example 3: The Plate Theft

**Problem:** Classify the bonding in $\ce{NaCl}$ ($EN$: $\ce{Na} = 0.9$, $\ce{Cl} = 3.0$) using AP-appropriate language.

**Solution:**

**Step 1:** Composition: metal + nonmetal → expect ionic.

**Step 2:** $\Delta EN = 3.0 - 0.9 = 2.1 > 1.7$ → the electron density transfers essentially completely to chlorine. Both checks agree.

**Step 3:** Phrase it the AP way: the bond has **mostly ionic character**. Sodium's valence electron is effectively transferred, giving $\ce{Na+}$ and $\ce{Cl-}$ held in a lattice by Coulombic attraction — but no bond is 100% ionic, so "mostly" is the honest word.

**Answer:** **Mostly ionic** — large $\Delta EN$ (2.1) plus metal + nonmetal composition means essentially complete electron transfer.

### Example 4: Ranking Bond Polarity

**Problem:** Rank $\ce{C-F}$, $\ce{C-Cl}$, and $\ce{C-Br}$ from most to least polar. ($EN$: $\ce{C} = 2.5$, $\ce{F} = 4.0$, $\ce{Cl} = 3.0$, $\ce{Br} = 2.8$.)

**Solution:**

**Step 1:** Same eater on one side ($\ce{C}$) in every bond, so polarity is decided entirely by the halogen's hunger.

**Step 2:** Compute each gap:
- $\ce{C-F}$: $\Delta EN = 4.0 - 2.5 = 1.5$
- $\ce{C-Cl}$: $\Delta EN = 3.0 - 2.5 = 0.5$
- $\ce{C-Br}$: $\Delta EN = 2.8 - 2.5 = 0.3$

**Step 3:** Bigger gap = more lopsided plate. Notice this is just the group trend in disguise: going down group 17, EN falls, so the gap with carbon shrinks.

**Answer:** $\ce{C-F} > \ce{C-Cl} > \ce{C-Br}$ — and $\ce{C-Br}$ ($\Delta EN = 0.3$) is technically in the *nonpolar* zone.

### Example 5: Most Polar Bond in a Molecule

**Problem:** Ethanol contains $\ce{C-H}$, $\ce{C-C}$, $\ce{C-O}$, and $\ce{O-H}$ bonds. Identify the most and least polar bonds.

**Solution:**

**Step 1:** Compute each gap ($EN$: $\ce{H} = 2.1$, $\ce{C} = 2.5$, $\ce{O} = 3.5$):
- $\ce{C-C}$: $\Delta EN = 0$ — identical twins, perfectly nonpolar
- $\ce{C-H}$: $\Delta EN = 0.4$ — nearly nonpolar
- $\ce{C-O}$: $\Delta EN = 1.0$ — polar
- $\ce{O-H}$: $\Delta EN = 1.4$ — very polar

**Step 2:** The pattern to remember: bonds *to oxygen* dominate the polarity of organic molecules; the hydrocarbon skeleton is electrically boring.

**Answer:** Most polar: $\ce{O-H}$ ($\Delta EN = 1.4$). Least polar: $\ce{C-C}$ ($\Delta EN = 0$).

### Example 6: Drawing the Dipole

**Problem:** For the $\ce{C-O}$ bond in $\ce{CO2}$, assign partial charges and state which way the dipole arrow points.

**Solution:**

**Step 1:** $EN(\ce{O}) = 3.5 > EN(\ce{C}) = 2.5$: oxygen hogs the shared pairs.

**Step 2:** So oxygen carries $\delta-$ and carbon carries $\delta+$:

$$\overset{\delta+}{\text{C}} = \overset{\delta-}{\text{O}}$$

**Step 3:** The dipole arrow points from C toward O — toward the more electronegative atom, following the electron density.

**Answer:** $\delta+$ on $\ce{C}$, $\delta-$ on $\ce{O}$; **arrow points toward oxygen.** (Each $\ce{C=O}$ bond is polar even though the whole $\ce{CO2}$ molecule ends up nonpolar by symmetry — bond polarity and molecular polarity are different questions.)

### Example 7: The Guidepost Gotcha — $\ce{HF}$

**Problem:** For $\ce{HF}$, $\Delta EN = 4.0 - 2.1 = 1.9 > 1.7$. Is $\ce{HF}$ an ionic compound?

**Solution:**

**Step 1:** Run the *first* check: hydrogen and fluorine are both **nonmetals**. Two nonmetals share — there's no metal willing to surrender electrons outright.

**Step 2:** Reality agrees: $\ce{HF}$ is a gas at room temperature made of discrete molecules — nothing like a brittle high-melting ionic lattice.

**Step 3:** Reconcile: the huge $\Delta EN$ means $\ce{HF}$ is an *extremely polar covalent* bond — enormous ionic **character** — but the plate, however far it slides toward fluorine, is still on the table between two people who are both eating. The 1.7 cutoff is a guidepost, and this is exactly the case where it misleads.

**Answer:** **No — $\ce{HF}$ is polar covalent** (with very high ionic character). Composition check beats the numeric cutoff.

### Example 8: High Ionic Character — $\ce{CaO}$

**Problem:** Compare the ionic character of $\ce{CaO}$ ($EN$: $\ce{Ca} = 1.0$, $\ce{O} = 3.5$) with $\ce{NaCl}$ ($\Delta EN = 2.1$).

**Solution:**

**Step 1:** $\Delta EN$ for $\ce{CaO}$: $3.5 - 1.0 = 2.5$.

**Step 2:** $2.5 > 2.1$, so $\ce{CaO}$ sits even farther toward the ionic end of the continuum than $\ce{NaCl}$ — greater ionic character.

**Step 3:** Bonus insight for later units: $\ce{CaO}$ is also $2+/2-$ ions instead of $1+/1-$, so its lattice is held by roughly four times the Coulombic attraction — which is why $\ce{CaO}$ melts at ~2600°C vs. $\ce{NaCl}$'s 801°C.

**Answer:** **$\ce{CaO}$ has greater ionic character** ($\Delta EN = 2.5 > 2.1$), and its doubled charges make the lattice dramatically stronger.

### Example 9: One Compound, Both Bond Types — $\ce{NH4Cl}$

**Problem:** Classify the bonding in ammonium chloride, $\ce{NH4Cl}$.

**Solution:**

**Step 1:** Spot the polyatomic ion: $\ce{NH4+}$. *Within* it, nitrogen and hydrogen (two nonmetals, $\Delta EN = 3.0 - 2.1 = 0.9$) share electrons → the four $\ce{N-H}$ bonds are **polar covalent**.

**Step 2:** The $\ce{NH4+}$ cation and the $\ce{Cl-}$ anion are oppositely charged particles held in a lattice by electrostatic attraction → the bonding *between* them is **ionic**.

**Step 3:** Fries version: four friends covalently sharing one plate at their table (the $\ce{NH4+}$ group) — and their whole table owes money to the next table over (the ionic attraction to $\ce{Cl-}$).

**Answer:** **Both:** covalent $\ce{N-H}$ bonds inside the ammonium ion, ionic bonding between $\ce{NH4+}$ and $\ce{Cl-}$. Any compound containing a polyatomic ion ($\ce{NaNO3}$, $\ce{K2SO4}$, …) plays this same trick.

### Example 10: Two Metals — Brass

**Problem:** Brass is a solid solution of copper and zinc. What type of bonding holds it together, and what properties follow?

**Solution:**

**Step 1:** Composition check: metal + metal. Neither atom is hungry enough to steal ($\Delta EN \approx 0.3$ — tiny), and neither wants to form the fixed shared pairs of covalent bonding.

**Step 2:** Instead, both metals contribute valence electrons to a delocalized sea; $\ce{Cu}$ and $\ce{Zn}$ cations sit together in one communal lattice.

**Step 3:** Predict properties from the model: mobile sea electrons → conducts electricity as a solid; the sea re-glues sliding cation layers → malleable, so brass can be hammered and machined.

**Answer:** **Metallic bonding** — a shared electron sea over mixed $\ce{Cu}$/$\ce{Zn}$ cations, predicting solid-state conductivity and malleability. (More on alloys in [Ionic Solids, Metals, and Alloys](/chemistry/0403-ionic-solids-metals-alloys).)

### Example 11: Classify the Solid from Data (Real AP Question Type)

**Problem:** Identify the bonding type in each unknown solid:

| Solid | Melting point | Conducts as solid? | Conducts when molten? |
|---|---|---|---|
| A | 808°C | No | Yes |
| B | 44°C | No | No |
| C | 1064°C | Yes | Yes |
| D | ~2700°C | No | (doesn't melt easily) |

**Solution:**

**Step 1 — Solid A:** high melting point, insulator as a solid but conductor when molten. Charged particles exist but are locked in place until melting frees them → **ions**. A is an **ionic solid** (those numbers are roughly $\ce{NaBr}$).

**Step 2 — Solid B:** melts at 44°C — barely above a hot day — and never conducts. Weakly-held discrete molecules, no mobile charges ever → **molecular solid** (that's white phosphorus, $\ce{P4}$).

**Step 3 — Solid C:** conducts *as a solid* — the single most diagnostic clue in the whole table. Only a delocalized electron sea does that → **metallic** (gold, in fact).

**Step 4 — Solid D:** astronomically high melting point, no conductivity: one continuous lattice of covalent bonds that must all break to melt → **covalent-network solid** (diamond-like).

**Answer:** **A ionic, B molecular, C metallic, D covalent-network.** Diagnose with conductivity first, melting point second.

### Example 12: The Full-Credit Justification

**Problem:** *(FRQ-style)* "A student claims the bond in $\ce{MgO}$ is ionic. Using the electronegativity values $\ce{Mg} = 1.2$ and $\ce{O} = 3.5$, justify the claim."

**Solution:**

**Step 1:** Use the data you're given — that's what it's there for: $\Delta EN = 3.5 - 1.2 = 2.3$.

**Step 2:** State the criterion and apply it: a $\Delta EN$ this large means the shared electron density shifts essentially completely to the more electronegative atom.

**Step 3:** Write the full-credit sentence chain: *"The electronegativity difference is $3.5 - 1.2 = 2.3$. This large difference means oxygen attracts the bonding electrons so much more strongly than magnesium that the electrons are effectively transferred, forming $\ce{Mg^2+}$ and $\ce{O^2-}$ ions held together by Coulombic attraction — a bond with mostly ionic character."*

**Step 4:** Note what would **not** earn full credit: "$\ce{Mg}$ is a metal and $\ce{O}$ is a nonmetal, so it's ionic." When EN data is given, the question is testing whether you can *use* it — position alone is an incomplete justification.

**Answer:** **Claim justified: $\Delta EN = 2.3$ → essentially complete electron transfer → mostly ionic character.** Always cite the numbers when the numbers are on the page.

---

## Common Mistakes

| The mistake | Why it happens | How to avoid it |
|---|---|---|
| Treating the $\Delta EN$ cutoffs (0.4, 1.7) as laws of nature | The table looks authoritative | They're guideposts on a **continuum**. Run "metal + nonmetal?" first; use $\Delta EN$ for *degree* of character ($\ce{HF}$: $\Delta EN = 1.9$, still covalent) |
| Calling $\ce{NaCl}$ "100% ionic" or a bond "purely covalent" | The foundations-level boxes die hard | AP language is "mostly ionic character" / "significant covalent character" — every bond is a mix |
| Pointing the dipole arrow at the **less** electronegative atom | Confusing "who lost electrons" with "where they went" | The arrow follows the electron density: it points **toward** the hungrier ($\delta-$) atom |
| Putting $\delta-$ on the less electronegative atom | Mixing up hog and hogged | $\delta-$ = more electron density = the atom that *wins* the tug-of-war |
| Writing full charges ($+1$, $-1$) on a polar covalent bond | Blurring polar covalent into ionic | Partial charges are $\delta+$/$\delta-$ — fractions. Full charges belong to actual ions |
| Treating $\ce{C-H}$ as strongly polar | $\Delta EN = 0.4$ is *technically* the fence | Convention (and the AP exam) treats $\ce{C-H}$ as essentially nonpolar |
| Missing that $\ce{NH4Cl}$-type compounds contain **both** bond types | Only checking the overall formula | Any compound with a polyatomic ion: covalent bonds *inside* the ion, ionic bonding *between* ions |
| Saying an ionic solid "conducts electricity" with no conditions | Half-remembered fact | Ionic solids conduct **only when molten or dissolved** — solids have locked ions. Conducting *as a solid* means metallic |
| Justifying bond type only by "metal + nonmetal" when EN values are printed on the page | It feels sufficient | If the exam gives numbers, it's grading your use of them: compute $\Delta EN$, then conclude |

---

## AP Exam Tips

1. **Know the FRQ stem: "Identify the type of bonding in X and justify your answer."** The scored answer has two parts — the identification *and* a justification that cites electronegativity. Template: *state $\Delta EN$ (or compare EN values) → say what the electrons do (shared equally / shared unequally / effectively transferred) → name the bond type.* Three sentences, full credit.
2. **When EN data appears in the question, it is not decoration.** "Sodium is a metal and chlorine is a nonmetal, so ionic" will read as incomplete when the table of EN values is sitting right there. Subtract, cite, conclude.
3. **Data-table classification is a recurring multiple-choice AND FRQ format.** Memorize the conductivity fingerprint: conducts as solid → metallic; conducts only molten/aqueous → ionic; never conducts + low melting → molecular; never conducts + extreme melting → covalent-network.
4. **Use "character" language.** "The bond has mostly ionic character" is exam-proof phrasing; the College Board itself frames bonding as a continuum. Absolute claims ("completely ionic") invite lost points on boundary cases.
5. **Electronegativity justifications ultimately trace to Coulomb's law.** If asked *why* fluorine's EN beats iodine's, deploy the [Periodic Trends](/chemistry/0305-periodic-trends) checklist: comparable $Z_{eff}$, but fluorine's valence shell is much closer with far less shielding → stronger attraction on bonding electrons.
6. **No calculator drama here** — every $\Delta EN$ is a one-decimal subtraction. The traps are conceptual, not arithmetic.
7. **Watch for polyatomic-ion compounds** in "select the compound with both ionic and covalent bonding" questions — scan the formula for $\ce{NH4+}$, $\ce{NO3-}$, $\ce{SO4^2-}$, $\ce{OH-}$, etc.

---

## Practice Problems

### Problem 1
Using $EN$ values ($\ce{K} = 0.8$, $\ce{Br} = 2.8$), classify the bond in $\ce{KBr}$ and justify with both available checks.

<details>
<summary><strong>Solution</strong></summary>

Composition check: potassium is a metal, bromine a nonmetal → expect ionic.

$\Delta EN = 2.8 - 0.8 = 2.0 > 1.7$ → mostly ionic character. Both checks agree: potassium's valence electron is effectively transferred to bromine, giving $\ce{K+}$ and $\ce{Br-}$ held by Coulombic attraction.

**Answer: mostly ionic ($\Delta EN = 2.0$; metal + nonmetal).**

</details>

### Problem 2
Classify the bond in $\ce{Br2}$ and in $\ce{H-Br}$ ($EN$: $\ce{H} = 2.1$, $\ce{Br} = 2.8$).

<details>
<summary><strong>Solution</strong></summary>

$\ce{Br2}$: identical atoms, $\Delta EN = 0$ → **nonpolar covalent** — perfectly even sharing.

$\ce{H-Br}$: $\Delta EN = 2.8 - 2.1 = 0.7$, two nonmetals → **polar covalent**, with $\delta-$ on $\ce{Br}$ and $\delta+$ on $\ce{H}$.

**Answer: $\ce{Br2}$ nonpolar covalent; $\ce{HBr}$ polar covalent ($\delta-$ on Br).**

</details>

### Problem 3
Rank these bonds from least to most polar: $\ce{O-H}$, $\ce{C-H}$, $\ce{N-H}$, $\ce{F-H}$. ($EN$: $\ce{H} = 2.1$, $\ce{C} = 2.5$, $\ce{N} = 3.0$, $\ce{O} = 3.5$, $\ce{F} = 4.0$.)

<details>
<summary><strong>Solution</strong></summary>

Hydrogen is the fixed partner, so rank by the other atom's EN:

- $\ce{C-H}$: $\Delta EN = 0.4$
- $\ce{N-H}$: $\Delta EN = 0.9$
- $\ce{O-H}$: $\Delta EN = 1.4$
- $\ce{F-H}$: $\Delta EN = 1.9$

This mirrors the period-2 EN trend: $\ce{C} < \ce{N} < \ce{O} < \ce{F}$.

**Answer: $\ce{C-H} < \ce{N-H} < \ce{O-H} < \ce{F-H}$.**

</details>

### Problem 4
For the $\ce{S-O}$ bond ($EN$: $\ce{S} = 2.5$, $\ce{O} = 3.5$): classify it, assign partial charges, and state the dipole arrow's direction.

<details>
<summary><strong>Solution</strong></summary>

$\Delta EN = 3.5 - 2.5 = 1.0$, two nonmetals → polar covalent.

Oxygen is more electronegative → $\delta-$ on $\ce{O}$, $\delta+$ on $\ce{S}$. The dipole arrow points from S toward O — toward the atom hogging the electron density.

**Answer: polar covalent; $\overset{\delta+}{\text{S}}-\overset{\delta-}{\text{O}}$; arrow points toward O.**

</details>

### Problem 5
$\ce{CsF}$ is often called "the most ionic compound." Use EN reasoning ($\ce{Cs} \approx 0.7$, $\ce{F} = 4.0$) to explain why — and explain why even $\ce{CsF}$ isn't *100%* ionic.

<details>
<summary><strong>Solution</strong></summary>

$\Delta EN = 4.0 - 0.7 = 3.3$ — the largest gap the periodic table can produce, pairing the least electronegative common metal (bottom left) with the most electronegative atom (top right). The bonding electron density shifts about as completely to fluorine as nature allows.

But bonding is a continuum: even here, a small amount of electron density remains shared between the ions, so the honest description is "the highest ionic character of any bond," not "purely ionic." No real bond reaches either perfect end of the spectrum.

**Answer: $\Delta EN = 3.3$ is the maximum possible → highest ionic character known; but all bonds retain some covalent character, so 100% ionic doesn't exist.**

</details>

### Problem 6
Which compound contains *both* ionic and covalent bonding: $\ce{CaCl2}$, $\ce{CCl4}$, $\ce{KNO3}$, or $\ce{Fe}$? Explain where each bond type lives.

<details>
<summary><strong>Solution</strong></summary>

- $\ce{CaCl2}$: metal + nonmetal, simple ions → ionic only.
- $\ce{CCl4}$: two nonmetals → covalent only.
- $\ce{Fe}$: pure metal → metallic only.
- $\ce{KNO3}$: contains the polyatomic ion $\ce{NO3-}$. *Within* the nitrate ion, $\ce{N-O}$ bonds are covalent ($\Delta EN = 0.5$, two nonmetals). *Between* $\ce{K+}$ and $\ce{NO3-}$, the attraction is ionic.

**Answer: $\ce{KNO3}$ — covalent bonds inside $\ce{NO3-}$, ionic bonding between $\ce{K+}$ and $\ce{NO3-}$.**

</details>

### Problem 7
A student writes: "$\ce{AlCl3}$ contains a metal and a nonmetal, so its bonding is purely ionic." Using $EN(\ce{Al}) = 1.5$ and $EN(\ce{Cl}) = 3.0$, improve this answer to AP level.

<details>
<summary><strong>Solution</strong></summary>

$\Delta EN = 3.0 - 1.5 = 1.5$ — *below* the 1.7 guidepost, in the polar-covalent range, even though the composition is metal + nonmetal.

AP-level answer: $\ce{AlCl3}$ has bonding intermediate on the continuum — substantial ionic character (metal + nonmetal) but also **significant covalent character** ($\Delta EN$ only 1.5; aluminum's small, highly charged cation polarizes chloride's electron cloud, pulling shared density back). Experimentally, $\ce{AlCl3}$ behaves partly covalently (it sublimes near 180°C — far too low for a purely ionic lattice). This is a classic metalloid-boundary-region case where the clean boxes fail.

**Answer: not "purely ionic" — bonding with intermediate character ($\Delta EN = 1.5$); the continuum picture, not a box, is required.**

</details>

### Problem 8
Silicon sits on the metalloid staircase. Classify the bonding in $\ce{SiO2}$ ($EN$: $\ce{Si} = 1.8$, $\ce{O} = 3.5$) and reconcile it with quartz's extreme melting point (~1710°C).

<details>
<summary><strong>Solution</strong></summary>

$\Delta EN = 3.5 - 1.8 = 1.7$ — sitting exactly on the guidepost. Composition check: silicon is a metalloid bonding to a nonmetal → lean covalent. Indeed, $\ce{SiO2}$ forms **polar covalent** $\ce{Si-O}$ bonds.

The huge melting point is *not* evidence of ionic bonding — it's because quartz is a **covalent-network solid**: every Si bonded to 4 O's in one continuous lattice, so melting requires breaking actual covalent bonds throughout the crystal.

**Answer: polar covalent bonds ($\Delta EN = 1.7$, metalloid + nonmetal) arranged in a covalent network — high melting point comes from the network structure, not from ionic character.**

</details>

### Problem 9
Explain, using Coulombic reasoning (protons, distance, shielding), why fluorine's electronegativity (4.0) is so much larger than iodine's (2.5) even though iodine has far more protons.

<details>
<summary><strong>Solution</strong></summary>

Total protons don't matter — *effective* pull on the bonding electrons does.

- **Protons ($Z_{eff}$):** both are group 17, feeling a comparable effective nuclear charge of roughly $+7$ at the valence shell.
- **Distance:** fluorine's bonding electrons sit in $n = 2$, extremely close to the nucleus; iodine's sit in $n = 5$, far away — and Coulomb's law ($F \propto \frac{q_1 q_2}{r^2}$) punishes distance quadratically.
- **Shielding:** fluorine has 2 core electrons blocking; iodine has 46. Most of iodine's proton pull never reaches the bonding pair.

Similar effective charge, far shorter distance, far less shielding → fluorine attracts shared electrons much more strongly.

**Answer: comparable $Z_{eff}$, but F's bonding electrons are much closer with far less shielding → much stronger Coulombic attraction → higher EN.**

</details>

### Problem 10
Identify each solid from the data:

| Solid | Melting point | Conducts as solid? | Conducts molten/dissolved? |
|---|---|---|---|
| X | 660°C | Yes | Yes |
| Y | 714°C | No | Yes |
| Z | −23°C (liquid at room temp) | No | No |

<details>
<summary><strong>Solution</strong></summary>

- **X** conducts as a solid — the metallic fingerprint (delocalized electron sea). **Metallic** (it's aluminum).
- **Y** conducts only when molten or dissolved: charged particles locked in a lattice until freed → **ionic** (it's $\ce{MgCl2}$).
- **Z** melts below room temperature and never conducts: weakly-held neutral molecules → **molecular** (it's $\ce{CCl4}$).

**Answer: X metallic, Y ionic, Z molecular.**

</details>

### Problem 11
Copper is drawn into wires; rock salt shatters under the same hammer. Explain both behaviors from the bonding models.

<details>
<summary><strong>Solution</strong></summary>

**Copper (metallic):** cations sit in a delocalized electron sea. When layers of cations slide under stress, the sea instantly flows around the new arrangement and keeps binding everything — no specific bond breaks, so copper deforms (malleable/ductile) instead of cracking.

**Rock salt (ionic):** ions occupy fixed lattice positions with alternating charges. A hammer blow shifts one layer, suddenly aligning $\ce{Na+}$ next to $\ce{Na+}$ and $\ce{Cl-}$ next to $\ce{Cl-}$ — massive like-charge repulsion along the slip plane splits the crystal.

**Answer: the mobile electron sea lets metals deform without breaking bonds; shifting an ionic lattice creates like-charge repulsion → brittle fracture.**

</details>

### Problem 12
*(FRQ-style)* Write a three-sentence, full-credit justification: "Identify the type of bonding in $\ce{Cl2O}$ and justify your answer using electronegativity." ($EN$: $\ce{Cl} = 3.0$, $\ce{O} = 3.5$.)

<details>
<summary><strong>Solution</strong></summary>

Model answer: "The electronegativity difference between oxygen and chlorine is $3.5 - 3.0 = 0.5$. Because this difference is small but nonzero, the bonding electrons are shared unequally, with electron density shifted slightly toward the more electronegative oxygen ($\delta-$ on O, $\delta+$ on Cl). Therefore each $\ce{Cl-O}$ bond is polar covalent."

Structure to copy: **cite the numbers → describe what the electrons do → name the type.**

**Answer: polar covalent — justified via $\Delta EN = 0.5$ and unequal sharing toward oxygen.**

</details>

### Problem 13
Rank $\ce{NaF}$, $\ce{MgO}$, and $\ce{HCl}$ by ionic character, greatest to least. ($EN$: $\ce{Na} = 0.9$, $\ce{F} = 4.0$, $\ce{Mg} = 1.2$, $\ce{O} = 3.5$, $\ce{H} = 2.1$, $\ce{Cl} = 3.0$.)

<details>
<summary><strong>Solution</strong></summary>

Ionic character tracks $\Delta EN$:

- $\ce{NaF}$: $4.0 - 0.9 = 3.1$
- $\ce{MgO}$: $3.5 - 1.2 = 2.3$
- $\ce{HCl}$: $3.0 - 2.1 = 0.9$

$\ce{NaF}$ and $\ce{MgO}$ are mostly ionic (both metal + nonmetal, agreeing with composition); $\ce{HCl}$ is polar covalent with modest ionic character.

**Answer: $\ce{NaF} > \ce{MgO} > \ce{HCl}$.**

</details>

### Problem 14
Why do chemists treat the $\ce{C-H}$ bond as essentially nonpolar even though $\Delta EN = 0.4$ technically touches the polar guidepost? Give one real-world consequence.

<details>
<summary><strong>Solution</strong></summary>

$\Delta EN = 2.5 - 2.1 = 0.4$ sits exactly on the fence, and the resulting partial charges are tiny — the plate has barely drifted. Since the guideposts are conventions on a continuum anyway, the working convention (used by the AP exam) rounds $\ce{C-H}$ down to nonpolar.

Consequence: hydrocarbons — oils, fats, waxes, gasoline — are built almost entirely of $\ce{C-H}$ and $\ce{C-C}$ bonds, so they carry essentially no partial charges. That's why oil and water refuse to mix: water's very polar $\ce{O-H}$ bonds ($\Delta EN = 1.4$) have nothing to grab onto.

**Answer: the $\delta$ charges are negligible, so $\ce{C-H}$ is treated as nonpolar — which is why hydrocarbon oils don't mix with water.**

</details>

### Problem 15
*(Continuum synthesis)* Place these five substances in order along the bonding continuum from "perfectly even split" to "plate completely stolen," and add brass ($\ce{Cu/Zn}$) wherever it belongs: $\ce{F2}$, $\ce{CaO}$, $\ce{H2O}$'s $\ce{O-H}$ bond, $\ce{HCl}$, $\ce{CsF}$.

<details>
<summary><strong>Solution</strong></summary>

Compute/recall the gaps: $\ce{F2}$ ($0$) → $\ce{HCl}$ ($0.9$) → $\ce{O-H}$ ($1.4$) → $\ce{CaO}$ ($2.5$) → $\ce{CsF}$ ($3.3$).

$$\ce{F2} \;<\; \ce{HCl} \;<\; \ce{O-H} \;<\; \ce{CaO} \;<\; \ce{CsF}$$

Brass doesn't belong on this axis at all: the continuum runs between *localized* sharing and *complete transfer* between two atoms, while metallic bonding delocalizes electrons over the entire lattice — a communal fry pile for the whole cafeteria, not a two-person plate. It's the third bonding regime, off to the side.

**Answer: $\ce{F2} < \ce{HCl} < \ce{O-H} < \ce{CaO} < \ce{CsF}$; brass is metallic — a different axis entirely, not a point on this continuum.**

</details>

---

## Quick Reference

| Concept | The rule |
|---|---|
| Electronegativity (EN) | An atom's pull on a *shared* bonding pair; peaks top-right ($\ce{F} = 4.0$), bottoms out bottom-left ($\ce{Cs} \approx 0.7$) |
| Why the trend | Coulomb: protons ($Z_{eff}$), distance ($n$), shielding (core $e^-$) |
| $\Delta EN < 0.4$ | Nonpolar covalent — even split ($\ce{Cl2}$, $\ce{C-H}$) |
| $\Delta EN$ 0.4–1.7 | Polar covalent — lopsided sharing ($\ce{H-Cl}$, $\ce{O-H}$) |
| $\Delta EN > 1.7$ | Mostly ionic — effective transfer ($\ce{NaCl}$, $\ce{CaO}$) |
| Fine print | Guideposts, not laws — check metal + nonmetal first ($\ce{HF}$: $\Delta EN = 1.9$, still covalent) |
| Partial charges | $\delta-$ on the more electronegative atom; $\delta+$ on the other |
| Dipole arrow | Points **toward** the more electronegative ($\delta-$) atom |
| Both bond types | Polyatomic-ion compounds: covalent inside the ion, ionic between ions ($\ce{NH4Cl}$, $\ce{KNO3}$) |
| Metallic bonding | Cations in a delocalized electron sea → conducts as solid, malleable |
| Solid ID by conductivity | Solid conducts → metallic; only molten/aqueous → ionic; never + low mp → molecular; never + extreme mp → covalent-network |
| FRQ template | Cite $\Delta EN$ → describe electron behavior → name the bond type |

---

<div align="center">

[← Ions and Ionic Compounds](/chemistry/0306-valence-electrons-ionic-compounds) | [Bond Energy and Length →](/chemistry/0402-bond-energy-and-length)

</div>
