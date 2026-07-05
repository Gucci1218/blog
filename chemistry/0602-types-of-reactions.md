# Types of Reactions and Solubility Rules
<p class="article-date">July 5, 2026</p>

*The gym is dark, the playlist is loud, and I'm standing by the snack table watching the whole school dance play out — and I swear it's just chemistry with better lighting. Two people who came alone find each other and pair up into a couple (that's synthesis, $\ce{A + B -> AB}$). A couple that's been fighting all night finally splits and walks off in opposite directions (decomposition, $\ce{AB -> A + B}$). Somebody smooth cuts in, steals a partner, and leaves the original standing there alone (single replacement, $\ce{A + BC -> AC + B}$). Two couples meet, decide they'd rather trade, and swap partners entirely (double replacement, $\ce{AB + CD -> AD + CB}$). And once in a while a freshly-swapped pair turns out to be so awkward together that they storm straight off the dance floor and don't come back — that's a precipitate falling out of solution. Every reaction on the AP exam is one of these dance-floor moves, and this article teaches you to spot the move the instant the reactants walk in.*

---

## What You'll Learn
- Classify any reaction as **synthesis, decomposition, single replacement, double replacement, or combustion** from its skeleton pattern
- Write the general form and at least two balanced examples of each reaction type
- Use an **activity series** to decide whether a single-replacement reaction actually happens (a more reactive metal displaces a less reactive one)
- **Predict the products** of a reaction from the reactants alone — the exact skill the AP free-response section tests
- Rebuild product formulas with the criss-cross / charge-balance method so every predicted formula is charge-correct
- Apply the **solubility rules** to decide whether each product is aqueous or a solid
- Predict whether mixing two solutions produces a **precipitate**, and name that precipitate
- Write the **net ionic equation** for a precipitation reaction, tying straight back to spectator ions
- Recognize the complete-vs-incomplete distinction in combustion and produce the $\ce{CO2 + H2O}$ pattern automatically

---

## Prerequisites
- [Net Ionic Equations](/chemistry/0601-net-ionic-equations) — precipitation reactions are the whole reason net ionic equations exist; you must be able to split aqueous compounds into ions and cancel spectators before this article's payoff makes sense
- [Naming Compounds](/chemistry/0204-naming-compounds) — predicting products means *building* new formulas from ions, so the criss-cross charge-balance trick and ionic naming have to be automatic

---

## The Core Concept

### Intuition First

Stay with me at the dance. The single most useful habit in this entire unit is learning to **look at who walks onto the floor and predict the move before it happens.** In chemistry that's called *predicting products*, and it terrifies people only because they never built the right mental picture. So let's build it.

First, get the cast straight:

- A lone **dancer** = an element or a monatomic ion (one person, unattached)
- A **couple** = a compound (two ions holding hands — a cation and an anion)
- A **swap pattern** = the reaction type (who ends up with whom)
- A pair **leaving the floor** = a precipitate, a solid dropping out of the solution

Now the five moves, in the exact language a chemist uses:

**Two singles pair up → synthesis.** Two separate things combine into one. $\ce{A + B -> AB}$. On the floor: two people who arrived alone become one couple. In lab: $\ce{2Na + Cl2 -> 2NaCl}$.

**A couple splits up → decomposition.** One compound breaks into two or more pieces, usually because you dumped energy in (heat, electricity, a spark). $\ce{AB -> A + B}$. The fight, the breakup, both people walk away separately. In lab: $\ce{2H2O ->[\text{electricity}] 2H2 + O2}$.

**Someone cuts in → single replacement.** A lone dancer breaks into an existing couple, takes one partner, and leaves the other stranded alone. $\ce{A + BC -> AC + B}$. In lab, a reactive metal shoves a less reactive one out of its compound: $\ce{Zn + CuSO4 -> ZnSO4 + Cu}$. Zinc cut in, took the sulfate, and copper got left standing.

**Two couples trade → double replacement.** Two couples decide to swap partners cleanly. $\ce{AB + CD -> AD + CB}$. The cation of one pairs with the anion of the other, and vice versa. In lab: $\ce{AgNO3 + NaCl -> AgCl + NaNO3}$.

**A pair storms off → precipitation.** This isn't a *sixth* category — it's a double replacement where one of the new couples is so insoluble it refuses to stay dissolved and drops out as a solid $(s)$. That leaving-the-floor moment is the whole reason precipitation reactions matter, and it's where the solubility rules earn their keep.

(Combustion — a fuel meeting oxygen and burning — is the one move that doesn't fit the dance neatly. Think of it as the DJ's fog machine: fuel plus $\ce{O2}$ always coughs out $\ce{CO2}$ and $\ce{H2O}$. We'll treat it as its own thing.)

That's the entire mental model. The rest of this article is just learning to recognize each move fast and to write the products with correct formulas.

### The Five Reaction Types at a Glance

| Type | Skeleton | The dance move | Balanced example |
|---|---|---|---|
| **Synthesis** (combination) | $\ce{A + B -> AB}$ | Two singles become a couple | $\ce{2Mg + O2 -> 2MgO}$ |
| **Decomposition** | $\ce{AB -> A + B}$ | A couple breaks up | $\ce{2KClO3 ->[\Delta] 2KCl + 3O2}$ |
| **Single replacement** | $\ce{A + BC -> AC + B}$ | Someone cuts in, steals a partner | $\ce{Zn + 2HCl -> ZnCl2 + H2}$ |
| **Double replacement** | $\ce{AB + CD -> AD + CB}$ | Two couples swap partners | $\ce{AgNO3 + NaCl -> AgCl v + NaNO3}$ |
| **Combustion** | $\ce{fuel + O2 -> CO2 + H2O}$ | Fuel meets oxygen, burns | $\ce{CH4 + 2O2 -> CO2 + 2H2O}$ |

The down-arrow $\ce{v}$ next to $\ce{AgCl}$ is chemist shorthand for "this one leaves the floor" — a precipitate.

### Synthesis (Combination)

**Recognition cue:** the product side has *fewer* substances than the reactant side — usually two things become one. **General form:** $\ce{A + B -> AB}$.

Common flavors:
- metal + oxygen → metal oxide: $\ce{2Mg + O2 -> 2MgO}$
- nonmetal + oxygen → nonmetal oxide: $\ce{S + O2 -> SO2}$
- metal + nonmetal → ionic salt: $\ce{2Na + Cl2 -> 2NaCl}$
- oxide + water → acid or base: $\ce{CaO + H2O -> Ca(OH)2}$

### Decomposition

**Recognition cue:** a *single* reactant breaking into two or more products, almost always with an energy input written over the arrow — heat $\ce{->[\Delta]}$, light, or electricity (electrolysis). **General form:** $\ce{AB -> A + B}$.

Patterns worth memorizing:
- metal carbonates → metal oxide + $\ce{CO2}$: $\ce{CaCO3 ->[\Delta] CaO + CO2}$
- metal chlorates → metal chloride + $\ce{O2}$: $\ce{2KClO3 ->[\Delta] 2KCl + 3O2}$
- binary compounds → elements: $\ce{2H2O ->[\text{elec.}] 2H2 + O2}$

### Single Replacement — and the Activity Series

**Recognition cue:** a **lone element plus a compound** on the left. The element cuts in and displaces one partner, leaving *a different* lone element on the right. **General form:** $\ce{A + BC -> AC + B}$ (a metal displacing a cation) or $\ce{X + YZ -> YX + Z}$ (a halogen displacing an anion).

Here's the catch the dance analogy nails perfectly: **not everyone can cut in.** You can only steal a partner if you're "more attractive" than the person currently holding them. In chemistry, "more attractive" means **more reactive**, and reactivity is ranked by the **activity series**.

**Activity series (most reactive → least):**

$$\ce{Li > K > Ba > Ca > Na > Mg > Al > Zn > Fe > Ni > Sn > Pb > (H) > Cu > Ag > Au}$$

The rule: **a metal will displace any metal *below* it** on this list from a compound. A metal *cannot* displace one above it — that reaction simply doesn't happen (no reaction, "NR").

- $\ce{Zn + CuSO4 -> ZnSO4 + Cu}$ ✓ — zinc is above copper, so it cuts in
- $\ce{Cu + ZnSO4 -> }$ **NR** — copper is *below* zinc, can't steal the partner
- Metals above hydrogen (that $\ce{(H)}$ marker) displace $\ce{H2}$ from acids: $\ce{Zn + 2HCl -> ZnCl2 + H2}$; metals below H (Cu, Ag, Au) do *not* react with $\ce{HCl}$

Halogens have their own mini-series ($\ce{F2 > Cl2 > Br2 > I2}$): a halogen displaces any halide below it, e.g. $\ce{Cl2 + 2NaBr -> 2NaCl + Br2}$.

### Double Replacement (Metathesis)

**Recognition cue:** **two ionic compounds** (usually both aqueous) on the left. The two cations trade anions. **General form:** $\ce{AB + CD -> AD + CB}$.

Double replacements only actually *go* if the swap produces one of three "escape routes" — otherwise everything stays dissolved as free ions and nothing happens:

1. **A precipitate** (an insoluble solid) — the focus of the next section
2. **A gas** (e.g. $\ce{H2CO3}$ decomposing to $\ce{CO2 + H2O}$)
3. **A weak electrolyte / water** (acid–base neutralization, Unit 8)

The mechanics of the swap are pure [Naming Compounds](/chemistry/0204-naming-compounds): when you re-pair the ions, you must **rebuild each formula from scratch using charges** — you cannot just copy the old subscripts across. More on this in the worked examples.

### Combustion

**Recognition cue:** a fuel (usually a **hydrocarbon**, $\ce{C_xH_y}$, or a compound of just C, H, O) reacting with $\ce{O2}$. **The product pattern is fixed:** carbon becomes $\ce{CO2}$, hydrogen becomes $\ce{H2O}$.

$$\ce{C_xH_y + O2 -> CO2 + H2O}$$

Example: $\ce{C3H8 + 5O2 -> 3CO2 + 4H2O}$ (propane, the camping-stove fuel).

**Complete vs. incomplete:** with *plenty* of oxygen, combustion is **complete** → $\ce{CO2 + H2O}$. With *limited* oxygen it's **incomplete**, producing carbon monoxide $\ce{CO}$ (the deadly one) or soot ($\ce{C}$) instead of all $\ce{CO2}$. On the AP exam, "combustion" with no qualifier means the complete pattern.

---

## Precipitation Reactions and the Solubility Rules

This is the heart of Topic 4.7, so slow down here.

When you mix two solutions, all the ions are swimming around free. A **precipitate** forms only if two of them can pair into a compound that *refuses to dissolve*. To predict this, you need to know which ionic compounds are soluble (stay as free ions, $(aq)$) and which are insoluble (clump into a solid, $(s)$). That knowledge is the **solubility rules** — and here's the part your teacher will repeat until you dream about it: **the solubility rules are NOT on the AP periodic table or reference sheet. You must memorize them.**

### The Solubility Rules (memorize this table)

| Rule | Ion / compound class | Soluble? | Exceptions |
|---|---|---|---|
| 1 | Group 1 cations ($\ce{Li+, Na+, K+}$…) | **Always soluble** | none |
| 2 | Ammonium $\ce{NH4+}$ | **Always soluble** | none |
| 3 | Nitrates $\ce{NO3-}$, acetates $\ce{CH3COO-}$ | **Always soluble** | none (nitrates truly never fail) |
| 4 | Halides $\ce{Cl-, Br-, I-}$ | **Soluble** | except $\ce{Ag+}$, $\ce{Pb^2+}$, $\ce{Hg2^2+}$ |
| 5 | Sulfates $\ce{SO4^2-}$ | **Soluble** | except $\ce{Ba^2+}$, $\ce{Pb^2+}$, $\ce{Sr^2+}$, $\ce{Ca^2+}$ (slightly) |
| 6 | Carbonates $\ce{CO3^2-}$, phosphates $\ce{PO4^3-}$ | **Insoluble** | except Group 1 and $\ce{NH4+}$ |
| 7 | Hydroxides $\ce{OH-}$, sulfides $\ce{S^2-}$ | **Insoluble** | except Group 1 and $\ce{NH4+}$ (and $\ce{Ba(OH)2}$, $\ce{Sr(OH)2}$) |

**A memory ladder that actually sticks:** rules 1–3 are the "always yes" club (Group 1, ammonium, nitrates/acetates — *these override everything*). Rules 4–5 are "yes, except a short blacklist." Rules 6–7 are "no, except the always-yes club." When two rules seem to collide, **the always-soluble rules (1–3) win** — sodium anything and nitrate anything is dissolved, period.

### How to Predict a Precipitate (the 4-step routine)

Given "solution of X is mixed with solution of Y, does a precipitate form?", do this every single time:

1. **List the ions** present after mixing (split each compound into its cation and anion).
2. **Cross-pair** them into the two *possible* new products (this is the double-replacement swap).
3. **Check each new pair against the solubility rules.** If one is insoluble → precipitate. If both are soluble → no reaction (everything stays $(aq)$).
4. **Rebuild each product formula with correct charges** and label states.

### From Precipitate to Net Ionic Equation

Once you've found a precipitate, writing the **net ionic equation** is exactly the [Net Ionic Equations](/chemistry/0601-net-ionic-equations) skill: split every aqueous compound into ions, keep the solid $(s)$ intact, and cancel the **spectator ions** (the ones that appear unchanged on both sides). What's left is the real chemistry:

$$\ce{Ag+(aq) + Cl-(aq) -> AgCl(s)}$$

That two-ion line *is* the reaction. The $\ce{Na+}$ and $\ce{NO3-}$ just watched from the snack table.

> **🎬 Hollywood Chemistry: Real or Not?**
> *The scene:* The MythBusters build set out to test **mercury(II) fulminate**, $\ce{Hg(CNO)2}$ — a genuine primary explosive — to see whether a small amount could level an entire room.
> *The verdict:* Half real, half busted. The real part: mercury fulminate absolutely is a violent **contact explosive**. A single crystal, struck or tapped, undergoes a lightning-fast **decomposition reaction** ($\ce{AB -> A + B}$, the breakup move) — the unstable $\ce{Hg(CNO)2}$ shatters into hot gases ($\ce{CO2}$, $\ce{N2}$) plus mercury, all at once, which is exactly why it was used in old percussion caps to set off larger charges. The busted part: the idea that a tiny quantity could blow up a whole room. When the team tested a small sample, it produced a **sharp, startling bang** — impressive, but nothing close to a building-leveling blast. The energy in a few crystals is real but *small*: enough to trigger, not to demolish. Lesson: decomposition can be spectacularly fast without being spectacularly large.

---

## Worked Examples

### Example 1: Classify — Two Singles Pair Up

**Problem:** Classify $\ce{2Ca + O2 -> 2CaO}$.

**Solution:**

**Step 1:** Count substances — two reactants ($\ce{Ca}$, $\ce{O2}$) collapse into one product ($\ce{CaO}$).

**Step 2:** Two things becoming one is the signature of the "two singles become a couple" move.

**Answer:** **Synthesis** (metal + oxygen → metal oxide).

### Example 2: Classify — A Couple Breaks Up

**Problem:** Classify $\ce{2Ag2O ->[\Delta] 4Ag + O2}$.

**Solution:**

**Step 1:** One reactant, heated, splits into two products. That's a breakup driven by energy.

**Step 2:** The lone $\Delta$ over the arrow and the single-compound reactant confirm it.

**Answer:** **Decomposition** (a metal oxide breaking into its elements).

### Example 3: Classify — Someone Cuts In

**Problem:** Classify $\ce{Fe + CuSO4 -> FeSO4 + Cu}$.

**Solution:**

**Step 1:** The left side is a **lone element** ($\ce{Fe}$) plus a **compound** ($\ce{CuSO4}$). That combination is the single-replacement fingerprint.

**Step 2:** Iron takes the sulfate; copper is left standing alone. And iron *is* above copper on the activity series, so the cut-in is allowed.

**Answer:** **Single replacement** (iron displaces copper).

### Example 4: Will It React? Reading the Activity Series

**Problem:** Does $\ce{Ag + ZnCl2 ->}$ react? What about $\ce{Mg + ZnCl2 ->}$?

**Solution:**

**Step 1:** Both are single-replacement setups — a lone metal meeting a metal compound. The question is whether the newcomer is "attractive" enough to cut in.

**Step 2:** Silver sits *below* zinc on the activity series ($\ce{Zn > \ldots > Ag}$), so silver can't displace zinc → **no reaction**.

**Step 3:** Magnesium sits *above* zinc ($\ce{Mg > Zn}$), so it displaces zinc successfully:

$$\ce{Mg + ZnCl2 -> MgCl2 + Zn}$$

**Answer:** $\ce{Ag + ZnCl2}$ → **NR**; $\ce{Mg + ZnCl2 -> MgCl2 + Zn}$.

### Example 5: Predict the Products — Single Replacement in Acid

**Problem:** Predict the products of $\ce{Al + HCl ->}$ and balance.

**Solution:**

**Step 1:** Lone metal + acid → single replacement. Aluminum is above hydrogen on the activity series, so it displaces $\ce{H2}$ gas.

**Step 2:** Build the salt with correct charges: $\ce{Al^3+}$ and $\ce{Cl-}$ criss-cross to $\ce{AlCl3}$. Hydrogen leaves as diatomic $\ce{H2}$.

$$\ce{Al + HCl -> AlCl3 + H2}$$

**Step 3:** Balance. $\ce{AlCl3}$ needs 3 Cl; $\ce{H2}$ needs even H. Take $\ce{2Al}$, $\ce{6HCl}$, $\ce{2AlCl3}$, $\ce{3H2}$:

$$\ce{2Al + 6HCl -> 2AlCl3 + 3H2}$$

**Answer:** $\ce{2Al + 6HCl -> 2AlCl3 + 3H2}$

### Example 6: Predict the Products — Double Replacement Swap

**Problem:** Predict the products of $\ce{Na3PO4(aq) + CaCl2(aq) ->}$ and balance.

**Solution:**

**Step 1:** Two ionic compounds → double replacement. List the ions: $\ce{Na+}$, $\ce{PO4^3-}$, $\ce{Ca^2+}$, $\ce{Cl-}$.

**Step 2:** Swap partners: $\ce{Na+}$ pairs with $\ce{Cl-}$, and $\ce{Ca^2+}$ pairs with $\ce{PO4^3-}$. **Rebuild each formula from charges** (do NOT copy old subscripts):
- $\ce{Na+}$ + $\ce{Cl-}$ → $\ce{NaCl}$
- $\ce{Ca^2+}$ + $\ce{PO4^3-}$ → criss-cross to $\ce{Ca3(PO4)2}$

$$\ce{Na3PO4 + CaCl2 -> NaCl + Ca3(PO4)2}$$

**Step 3:** Balance. $\ce{Ca3(PO4)2}$ needs 3 Ca and 2 phosphate: take $\ce{2Na3PO4}$ and $\ce{3CaCl2}$, giving $\ce{6NaCl}$:

$$\ce{2Na3PO4 + 3CaCl2 -> 6NaCl + Ca3(PO4)2}$$

**Answer:** $\ce{2Na3PO4 + 3CaCl2 -> 6NaCl + Ca3(PO4)2}$

### Example 7: Predict the Products — Combustion

**Problem:** Predict the products of the complete combustion of butane, $\ce{C4H10}$, and balance.

**Solution:**

**Step 1:** Hydrocarbon + $\ce{O2}$ → the fixed pattern $\ce{CO2 + H2O}$.

$$\ce{C4H10 + O2 -> CO2 + H2O}$$

**Step 2:** Balance C → H → O. Carbon: 4 → $\ce{4CO2}$. Hydrogen: 10 → $\ce{5H2O}$. Oxygen on the right: $4(2) + 5 = 13$, odd → $\ce{\tfrac{13}{2}O2}$, then double everything:

$$\ce{2C4H10 + 13O2 -> 8CO2 + 10H2O}$$

**Answer:** $\ce{2C4H10 + 13O2 -> 8CO2 + 10H2O}$

### Example 8: Solubility Check — Does a Precipitate Form?

**Problem:** Solutions of $\ce{KNO3}$ and $\ce{NaCl}$ are mixed. Does a precipitate form?

**Solution:**

**Step 1:** Ions present: $\ce{K+}$, $\ce{NO3-}$, $\ce{Na+}$, $\ce{Cl-}$.

**Step 2:** Cross-pair the possible new products: $\ce{KCl}$ and $\ce{NaNO3}$.

**Step 3:** Check the rules. $\ce{KCl}$ — potassium is Group 1 → soluble (rule 1). $\ce{NaNO3}$ — sodium is Group 1 *and* nitrate is always soluble → soluble (rules 1 & 3). Both soluble.

**Answer:** **No precipitate — no reaction.** All four ions stay dissolved as spectators. (This is the classic "nothing happens" trap: every ion here is from the always-soluble club.)

### Example 9: Solubility Check — Identify the Precipitate

**Problem:** Solutions of $\ce{Pb(NO3)2}$ and $\ce{KI}$ are mixed. Predict and identify any precipitate.

**Solution:**

**Step 1:** Ions: $\ce{Pb^2+}$, $\ce{NO3-}$, $\ce{K+}$, $\ce{I-}$.

**Step 2:** Cross-pair: $\ce{PbI2}$ and $\ce{KNO3}$.

**Step 3:** Check the rules. $\ce{KNO3}$ → soluble (Group 1 + nitrate). $\ce{PbI2}$ → iodide is *usually* soluble, but $\ce{Pb^2+}$ is one of the three halide exceptions (rule 4) → **insoluble**. Precipitate!

**Step 4:** Charge-balance the solid: $\ce{Pb^2+}$ + $\ce{I-}$ → $\ce{PbI2}$.

**Answer:** A bright yellow precipitate of **$\ce{PbI2(s)}$** forms (the famous "golden rain" demo). Balanced molecular equation: $\ce{Pb(NO3)2 + 2KI -> PbI2 v + 2KNO3}$.

### Example 10: Write the Net Ionic Equation for a Precipitation

**Problem:** Silver nitrate and sodium chromate solutions are mixed: $\ce{2AgNO3(aq) + Na2CrO4(aq) -> Ag2CrO4 + 2NaNO3}$. Identify the precipitate and write the net ionic equation.

**Solution:**

**Step 1:** Check solubility of the products. $\ce{NaNO3}$ → soluble. $\ce{Ag2CrO4}$ → chromate is generally insoluble and silver isn't an exception → **precipitate** $(s)$.

**Step 2:** Write the full ionic equation, splitting every $(aq)$ compound into ions but keeping the solid whole:

$$\ce{2Ag+ + 2NO3- + 2Na+ + CrO4^2- -> Ag2CrO4(s) + 2Na+ + 2NO3-}$$

**Step 3:** Cancel spectators — $\ce{Na+}$ and $\ce{NO3-}$ appear unchanged on both sides:

$$\ce{2Ag+(aq) + CrO4^2-(aq) -> Ag2CrO4(s)}$$

**Answer:** Precipitate is dark-red $\ce{Ag2CrO4(s)}$; net ionic: $\ce{2Ag+(aq) + CrO4^2-(aq) -> Ag2CrO4(s)}$.

### Example 11: The Full Chain — Predict, Classify, Net Ionic

**Problem:** A student mixes barium chloride and sodium sulfate solutions. Classify the reaction, predict the precipitate, and write the net ionic equation.

**Solution:**

**Step 1:** Two ionic solutions → **double replacement**. Ions: $\ce{Ba^2+}$, $\ce{Cl-}$, $\ce{Na+}$, $\ce{SO4^2-}$.

**Step 2:** Cross-pair: $\ce{BaSO4}$ and $\ce{NaCl}$. Check rules: $\ce{NaCl}$ soluble; $\ce{BaSO4}$ — sulfate is soluble *except* with $\ce{Ba^2+}$ (rule 5) → **insoluble**. Precipitate is $\ce{BaSO4}$.

**Step 3:** Molecular equation (already balanced): $\ce{BaCl2 + Na2SO4 -> BaSO4 v + 2NaCl}$.

**Step 4:** Full ionic, then cancel $\ce{Na+}$ and $\ce{Cl-}$:

$$\ce{Ba^2+(aq) + SO4^2-(aq) -> BaSO4(s)}$$

**Answer:** Double replacement → precipitation; white $\ce{BaSO4(s)}$ forms; net ionic $\ce{Ba^2+(aq) + SO4^2-(aq) -> BaSO4(s)}$. (This is the reaction behind the "barium milkshake" doctors give before an X-ray — $\ce{BaSO4}$ is so insoluble it's safe to swallow.)

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Copying old subscripts into the swapped products | You see $\ce{CaCl2}$ and write $\ce{CaPO4}$ by reflex | Rebuild **every** product formula from ion charges (criss-cross). $\ce{Ca^2+}$ + $\ce{PO4^3-}$ is $\ce{Ca3(PO4)2}$, not $\ce{CaPO4}$ |
| Assuming every single-replacement reaction happens | You forget reactivity has a ranking | Check the **activity series**. A metal below the other one gives **no reaction** |
| Thinking the solubility rules are on the reference sheet | Wishful thinking under exam pressure | They are **not** provided. Memorize the 7-rule table before the exam |
| Calling "no precipitate" a reaction | Two solutions were mixed, so something *must* happen, right? | If both possible products are soluble, it's **NR** — the ions just coexist |
| Splitting a solid or a gas into ions in the net ionic | Habit of splitting everything aqueous | Only $(aq)$ strong electrolytes split. Solids $(s)$, gases $(g)$, and water stay whole |
| Combustion products other than $\ce{CO2}$ and $\ce{H2O}$ | Overthinking the fuel | Complete combustion of a C/H(/O) fuel **always** gives $\ce{CO2 + H2O}$. Balance C → H → O |
| Forgetting diatomic elements when a lone element is a product | Writing $\ce{H}$, $\ce{Cl}$, or $\ce{O}$ alone | Displaced nonmetals leave as $\ce{H2, O2, Cl2, Br2, I2, N2, F2}$ |
| Mixing up which ion is the exception | Rules 4 and 5 have blacklists | Memorize the short lists: halides fail with **Ag, Pb, Hg**; sulfates fail with **Ba, Pb, Sr, Ca** |

---

## AP Exam Tips

- **Predicting products is a guaranteed free-response task.** Every AP Chem exam includes a question that gives you reactants in words ("Solid zinc is added to a solution of copper(II) sulfate…") and asks for the balanced equation. You must (1) recognize the reaction type, (2) predict correctly-charged products, and (3) balance — all from memory.
- **Solubility rules are NOT on the AP periodic table or the equations sheet.** This is the single most-forgotten fact in Unit 4. If you can't recall that $\ce{BaSO4}$ and $\ce{AgCl}$ are insoluble, you can't predict precipitates. Memorize the table cold.
- **Precipitation questions almost always chain into net ionic equations.** The exam rewards the *net* ionic form: identify the precipitate, cancel spectators, and include state symbols. Leaving spectators in, or omitting $(s)$/$(aq)$, costs points.
- **Combustion has a fixed product pattern.** When you see a hydrocarbon + $\ce{O2}$, write $\ce{CO2 + H2O}$ immediately and balance C → H → O. Don't overthink it.
- **Charge-correct formulas earn the formula point.** Graders check that predicted formulas are electrically neutral. A single mis-charged formula ($\ce{NaCl2}$, $\ce{CaPO4}$) loses the point even if your reasoning was right.
- **"No reaction" is a valid, testable answer.** If the activity series forbids the displacement, or both double-replacement products are soluble, write **NR** and know *why*.

---

## Practice Problems

### Problem 1
Classify: $\ce{2H2 + O2 -> 2H2O}$

<details>
<summary><strong>Solution</strong></summary>

Two reactants combine into one product — two singles become a couple.

**Answer:** Synthesis (combination).

</details>

### Problem 2
Classify: $\ce{2NaHCO3 ->[\Delta] Na2CO3 + H2O + CO2}$ (baking soda in the oven)

<details>
<summary><strong>Solution</strong></summary>

A single compound, heated, breaks into three products — a heat-driven breakup.

**Answer:** Decomposition.

</details>

### Problem 3
Classify: $\ce{Cl2 + 2KBr -> 2KCl + Br2}$

<details>
<summary><strong>Solution</strong></summary>

A lone element ($\ce{Cl2}$) plus a compound; chlorine displaces bromide and a new lone element ($\ce{Br2}$) appears. Chlorine is above bromine in the halogen series, so it works.

**Answer:** Single replacement.

</details>

### Problem 4
Classify: $\ce{Pb(NO3)2 + 2KI -> PbI2 + 2KNO3}$

<details>
<summary><strong>Solution</strong></summary>

Two ionic compounds swap partners; $\ce{PbI2}$ is an insoluble precipitate.

**Answer:** Double replacement (specifically a precipitation reaction).

</details>

### Problem 5
Does $\ce{Cu + FeCl2 ->}$ react? Explain using the activity series.

<details>
<summary><strong>Solution</strong></summary>

Copper sits *below* iron on the activity series ($\ce{Fe > \ldots > Cu}$), so copper cannot displace iron.

**Answer:** No reaction (NR).

</details>

### Problem 6
Predict the products and balance: $\ce{Mg + O2 ->}$

<details>
<summary><strong>Solution</strong></summary>

Metal + oxygen → metal oxide (synthesis). $\ce{Mg^2+}$ + $\ce{O^2-}$ → $\ce{MgO}$.

Balance: $\ce{2Mg + O2 -> 2MgO}$.

**Answer:** $\ce{2Mg + O2 -> 2MgO}$

</details>

### Problem 7
Predict the products and balance: $\ce{Zn + AgNO3 ->}$

<details>
<summary><strong>Solution</strong></summary>

Lone metal + compound → single replacement. Zinc is above silver, so it displaces $\ce{Ag}$. Rebuild the salt: $\ce{Zn^2+}$ + $\ce{NO3-}$ → $\ce{Zn(NO3)2}$; silver leaves as solid $\ce{Ag}$.

$$\ce{Zn + 2AgNO3 -> Zn(NO3)2 + 2Ag}$$

**Answer:** $\ce{Zn + 2AgNO3 -> Zn(NO3)2 + 2Ag}$

</details>

### Problem 8
Predict the products and balance the complete combustion of ethanol, $\ce{C2H5OH}$.

<details>
<summary><strong>Solution</strong></summary>

Fuel + $\ce{O2}$ → $\ce{CO2 + H2O}$. Ethanol has 2 C, 6 H, and 1 O (which counts toward the oxygen tally).

C: 2 → $\ce{2CO2}$. H: 6 → $\ce{3H2O}$. Oxygen on the right: $2(2)+3 = 7$; the fuel already supplies 1 O, so $\ce{O2}$ must give 6 → $\ce{3O2}$.

$$\ce{C2H5OH + 3O2 -> 2CO2 + 3H2O}$$

**Answer:** $\ce{C2H5OH + 3O2 -> 2CO2 + 3H2O}$

</details>

### Problem 9
Solutions of $\ce{(NH4)2S}$ and $\ce{Cu(NO3)2}$ are mixed. Predict any precipitate.

<details>
<summary><strong>Solution</strong></summary>

Ions: $\ce{NH4+}$, $\ce{S^2-}$, $\ce{Cu^2+}$, $\ce{NO3-}$. Cross-pair: $\ce{NH4NO3}$ (soluble — ammonium and nitrate) and $\ce{CuS}$. Sulfides are insoluble except Group 1 and ammonium; copper isn't an exception → $\ce{CuS}$ precipitates.

**Answer:** Black $\ce{CuS(s)}$ precipitates.

</details>

### Problem 10
Solutions of $\ce{NaOH}$ and $\ce{MgCl2}$ are mixed. Predict the precipitate and write the net ionic equation.

<details>
<summary><strong>Solution</strong></summary>

Ions: $\ce{Na+}$, $\ce{OH-}$, $\ce{Mg^2+}$, $\ce{Cl-}$. Cross-pair: $\ce{NaCl}$ (soluble) and $\ce{Mg(OH)2}$. Hydroxides are insoluble except Group 1 and ammonium; $\ce{Mg^2+}$ is not an exception → precipitate.

Full ionic (molecular: $\ce{2NaOH + MgCl2 -> Mg(OH)2 v + 2NaCl}$), then cancel $\ce{Na+}$ and $\ce{Cl-}$:

$$\ce{Mg^2+(aq) + 2OH-(aq) -> Mg(OH)2(s)}$$

**Answer:** $\ce{Mg(OH)2(s)}$ (the active ingredient in milk of magnesia); net ionic $\ce{Mg^2+(aq) + 2OH-(aq) -> Mg(OH)2(s)}$.

</details>

### Problem 11
Solutions of $\ce{KNO3}$ and $\ce{(NH4)2SO4}$ are mixed. Does a precipitate form?

<details>
<summary><strong>Solution</strong></summary>

Ions: $\ce{K+}$, $\ce{NO3-}$, $\ce{NH4+}$, $\ce{SO4^2-}$. Cross-pair: $\ce{K2SO4}$ (Group 1 → soluble) and $\ce{NH4NO3}$ (ammonium + nitrate → soluble). Both soluble.

**Answer:** No precipitate — no reaction (all ions are spectators).

</details>

### Problem 12
Solutions of $\ce{AgNO3}$ and $\ce{CaCl2}$ are mixed. Predict the precipitate and write the net ionic equation.

<details>
<summary><strong>Solution</strong></summary>

Ions: $\ce{Ag+}$, $\ce{NO3-}$, $\ce{Ca^2+}$, $\ce{Cl-}$. Cross-pair: $\ce{Ca(NO3)2}$ (nitrate → soluble) and $\ce{AgCl}$ (halide, but $\ce{Ag+}$ is an exception → insoluble).

Molecular: $\ce{2AgNO3 + CaCl2 -> 2AgCl v + Ca(NO3)2}$. Cancel $\ce{Ca^2+}$ and $\ce{NO3-}$:

$$\ce{Ag+(aq) + Cl-(aq) -> AgCl(s)}$$

**Answer:** White $\ce{AgCl(s)}$; net ionic $\ce{Ag+(aq) + Cl-(aq) -> AgCl(s)}$.

</details>

### Problem 13
Predict the products and balance: $\ce{BaCO3 ->[\Delta]}$

<details>
<summary><strong>Solution</strong></summary>

Single compound + heat → decomposition. Metal carbonates decompose to the metal oxide + $\ce{CO2}$.

$$\ce{BaCO3 ->[\Delta] BaO + CO2}$$

Already balanced (1 Ba, 1 C, 3 O each side).

**Answer:** $\ce{BaCO3 ->[\Delta] BaO + CO2}$

</details>

### Problem 14
A lab tech adds solid aluminum to hydrochloric acid and sees bubbles. Predict the products, classify, and balance.

<details>
<summary><strong>Solution</strong></summary>

Lone metal + acid → single replacement; aluminum is above hydrogen, so it displaces $\ce{H2}$ gas (the bubbles). Salt: $\ce{Al^3+}$ + $\ce{Cl-}$ → $\ce{AlCl3}$.

$$\ce{2Al + 6HCl -> 2AlCl3 + 3H2}$$

**Answer:** $\ce{2Al + 6HCl -> 2AlCl3 + 3H2}$ (single replacement).

</details>

### Problem 15
Explain, using the "always-soluble" rules, why you can never make a precipitate by mixing two *sodium* salts — no matter which anions they carry.

<details>
<summary><strong>Solution</strong></summary>

After mixing two sodium salts, every possible new cation–anion pair still includes $\ce{Na+}$ on one side of the swap. But rule 1 says **all Group 1 salts are soluble** with no exceptions — so any sodium-containing product stays dissolved. Even if the two anions could form an insoluble compound, there's no *second* cation available to pair them with. The always-soluble club (Group 1, ammonium, nitrates/acetates) overrides every other rule, so at least one of the required cations refuses to leave solution.

**Answer:** Because every sodium compound is soluble (rule 1 has no exceptions), no product can precipitate — you'd need a non-Group-1 cation available to pair with an insoluble anion.

</details>

---

## Quick Reference

**The five reaction types:**

| Type | Skeleton | Spot it by |
|---|---|---|
| Synthesis | $\ce{A + B -> AB}$ | Two+ reactants → one product |
| Decomposition | $\ce{AB -> A + B}$ | One reactant + energy → many products |
| Single replacement | $\ce{A + BC -> AC + B}$ | Lone element + compound (check activity series) |
| Double replacement | $\ce{AB + CD -> AD + CB}$ | Two compounds swap partners |
| Combustion | $\ce{fuel + O2 -> CO2 + H2O}$ | Hydrocarbon + oxygen, burns |

**Activity series (more reactive displaces less):**
$$\ce{Li > K > Ba > Ca > Na > Mg > Al > Zn > Fe > Ni > Sn > Pb > (H) > Cu > Ag > Au}$$

**Solubility rules (memorize — not on the AP sheet):**

| Soluble | Insoluble |
|---|---|
| Group 1, $\ce{NH4+}$ (always) | Carbonates $\ce{CO3^2-}$ |
| Nitrates $\ce{NO3-}$, acetates (always) | Phosphates $\ce{PO4^3-}$ |
| Halides $\ce{Cl-,Br-,I-}$ — *except* $\ce{Ag+, Pb^2+, Hg2^2+}$ | Hydroxides $\ce{OH-}$ |
| Sulfates $\ce{SO4^2-}$ — *except* $\ce{Ba^2+, Pb^2+, Sr^2+, Ca^2+}$ | Sulfides $\ce{S^2-}$ |

*(Insoluble classes are still soluble with Group 1 and $\ce{NH4+}$ — the always-soluble club wins every tie.)*

**Precipitation routine:** list ions → cross-pair → check solubility → if one product insoluble, it precipitates → write net ionic (cancel spectators, keep the solid whole).

**Combustion:** always $\ce{CO2 + H2O}$; balance C → H → O.

---

<div align="center">

[← Net Ionic Equations](/chemistry/0601-net-ionic-equations) | [Stoichiometry →](/chemistry/0603-stoichiometry)

</div>
