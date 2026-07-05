# Naming Compounds
<p class="article-date">July 4, 2026</p>

*Yesterday I ordered an "iced venti oat-milk vanilla latte" at the Starbucks near Torrey Pines, and it hit me that the order isn't a random pile of words — it's a code. Each slot means something: temperature, size, milk, flavor, drink base. Any barista in any city on Earth could rebuild my exact drink from that string of words, and if I scramble the slots or drop one, I get the wrong drink. Chemical nomenclature is the exact same contract: one unambiguous name maps to one exact formula, worldwide. The cation is your drink base, the anion is your milk choice, the Roman numeral is your size — every slot carries information, and the grammar changes depending on what category of "drink" you ordered (a latte is built differently than a refresher). In this article we learn that grammar: ionic compounds, covalent compounds, and acids each have their own naming rules, and the first move is always figuring out which menu you're ordering from. This is quiet, foundational fluency — the AP exam almost never asks "name this compound" directly, but every stoichiometry FRQ assumes you can translate names to formulas instantly and flawlessly.*

---

## What You'll Learn
- Use a three-branch decision tree to classify any compound as ionic, covalent (molecular), or an acid before naming it
- Name Type I ionic compounds (fixed-charge metals) and write their formulas by balancing charges
- Name Type II ionic compounds (variable-charge metals) using Roman numerals, and reverse-engineer the metal's charge from the anion
- Identify the metals that do *not* need Roman numerals ($\ce{Ag+}$, $\ce{Zn^2+}$, $\ce{Cd^2+}$, $\ce{Al^3+}$)
- Name ionic compounds containing polyatomic ions by keeping the polyatomic name intact
- Apply the prefix system (mono- through deca-) to covalent compounds, including the "drop mono- on the first element" rule
- Name binary acids (hydro-\_\_\_-ic) and oxyacids (-ate → -ic, -ite → -ous)
- Translate fluently in *both* directions: name → formula and formula → name
- Recognize the handful of trivial names ($\ce{H2O}$, $\ce{NH3}$, $\ce{CH4}$) that ignore all the rules

---

## Prerequisites
- [Ionic vs Covalent](/chemistry/0203-ionic-vs-covalent) — the naming grammar splits on bond type, so you must be able to spot metal + nonmetal versus nonmetal + nonmetal on sight

---

## The Core Concept

### Intuition First

Back to the Starbucks counter. When you walk in, your *first* decision isn't "what flavor?" — it's "what category of drink?" Latte, refresher, or frappuccino? Each category has its own ordering grammar. Lattes care about milk type; refreshers don't even have a milk slot. If you try to order a refresher using latte grammar ("oat-milk strawberry açaí"?), the barista just stares at you.

Chemistry works the same way. Before you name anything, you ask: **which category am I in?** There are three menus:

1. **Ionic** (metal + nonmetal) — like a latte: name the base (cation), name the milk (anion with -ide), and if the metal is a "customizable size" transition metal, specify the size with a Roman numeral.
2. **Covalent / molecular** (two nonmetals) — like a frappuccino with pump counts: you literally *count* the atoms with Greek prefixes, because the same two elements can combine in several ratios ($\ce{CO}$ vs. $\ce{CO2}$ are as different as one pump vs. two pumps of syrup — one of them can kill you, which is more dramatic than any syrup).
3. **Acids** (starts with $\ce{H}$, dissolved in water) — the secret menu: its own vocabulary (hydro-, -ic, -ous) that remixes the anion's name.

Every slot in the name carries information, and no slot is decorative. "Iron(III) oxide" tells you the metal, its charge, and the anion — enough to rebuild $\ce{Fe2O3}$ from scratch. That's the contract: **one name ↔ one formula**, no ambiguity, anywhere on Earth.

### The Decision Tree (Memorize This First)

This is the flowchart you run *before anything else*:

```
                      What am I looking at?
                              |
        +---------------------+---------------------+
        |                     |                     |
  Metal + Nonmetal      Two Nonmetals        Starts with H,
  (or metal +           (or metalloid +      described as (aq)
  polyatomic ion)       nonmetal)            or called "acid"
        |                     |                     |
     IONIC RULES        COVALENT RULES         ACID RULES
        |                     |                     |
  Fixed-charge metal?   Greek prefixes        Anion has oxygen?
   Yes -> Type I        mono- ... deca-        No  -> hydro-__-ic
   No  -> Type II       (drop mono- on         Yes -> -ate  -> -ic
   (Roman numeral)       first element)               -ite -> -ous
```

Or as a table:

| First question | Answer | Rulebook |
|---|---|---|
| Metal + nonmetal (or contains a polyatomic ion)? | Yes | **Ionic rules** — cation name + anion name; Roman numeral if the metal has variable charge |
| Two nonmetals only? | Yes | **Covalent rules** — Greek prefixes count atoms |
| Formula starts with $\ce{H}$ and it's aqueous / called an acid? | Yes | **Acid rules** — hydro-\_\_\_-ic or -ate/-ite conversion |

Get the category wrong and everything downstream is wrong — just like ordering a refresher with latte grammar.

### Ionic Type I: Fixed-Charge Metals

Group 1 metals are always $1+$, Group 2 are always $2+$, and aluminum is always $3+$. These metals have exactly one possible charge, so the name needs no size slot.

**Naming rule:** cation name (unchanged) + anion root + **-ide**.

$$\ce{NaCl} \rightarrow \text{sodium chloride} \qquad \ce{MgBr2} \rightarrow \text{magnesium bromide}$$

Notice the name *doesn't say* "magnesium dibromide." Ionic names never use prefixes, because the charges already lock in the ratio. The subscripts are recoverable: $\ce{Mg^2+}$ needs two $\ce{Br-}$ to balance. **The name states the ions; charge balance rebuilds the subscripts.**

**Formula-from-name rule (the criss-cross check):** write both ions with charges, then find the smallest ratio that makes the total charge zero.

$$\ce{Al^3+} + \ce{O^2-} \rightarrow \text{need } 2(3+) + 3(2-) = 0 \rightarrow \ce{Al2O3}$$

**Common monatomic anions (memorize):**

| Anion | Name | Anion | Name |
|---|---|---|---|
| $\ce{F-}$ | fluoride | $\ce{O^2-}$ | oxide |
| $\ce{Cl-}$ | chloride | $\ce{S^2-}$ | sulfide |
| $\ce{Br-}$ | bromide | $\ce{N^3-}$ | nitride |
| $\ce{I-}$ | iodide | $\ce{P^3-}$ | phosphide |
| $\ce{H-}$ | hydride | $\ce{C^4-}$ | carbide |

### Ionic Type II: Variable-Charge Metals and Roman Numerals

Transition metals (and heavy p-block metals like tin and lead) can carry *different* charges in different compounds. Iron can be $\ce{Fe^2+}$ or $\ce{Fe^3+}$. So the name needs a size slot — the Roman numeral — stating the cation's charge:

$$\ce{FeCl2} \rightarrow \text{iron(II) chloride} \qquad \ce{FeCl3} \rightarrow \text{iron(III) chloride}$$

**Critical:** the Roman numeral is the **charge on one metal ion**, *not* the subscript. To name a formula, you reverse-engineer the charge from the anion, whose charge you always know:

$$\ce{Fe2O3}: \quad 3 \times \ce{O^2-} = 6- \;\Rightarrow\; 2 \text{ Fe atoms must total } 6+ \;\Rightarrow\; \text{each Fe is } 3+ \;\Rightarrow\; \text{iron(III) oxide}$$

The anion is your anchor. Anions don't negotiate; metals do.

**Metals that skip the numeral** (only one charge in practice, so no size slot needed):

| Metal | Always | Metal | Always |
|---|---|---|---|
| $\ce{Ag+}$ | silver, $1+$ | $\ce{Cd^2+}$ | cadmium, $2+$ |
| $\ce{Zn^2+}$ | zinc, $2+$ | $\ce{Al^3+}$ | aluminum, $3+$ |

Writing "silver(I) chloride" isn't wrong-wrong, but it flags you as a tourist. "Silver chloride" is the fluent order.

### Ionic with Polyatomic Ions (Preview)

Some ions are whole molecular chunks carrying a charge — $\ce{SO4^2-}$ (sulfate), $\ce{NO3-}$ (nitrate), $\ce{NH4+}$ (ammonium). The rule is simple: **treat the polyatomic ion as a single unit and keep its name intact.**

$$\ce{Na2SO4} \rightarrow \text{sodium sulfate} \qquad \ce{NH4NO3} \rightarrow \text{ammonium nitrate}$$

No -ide ending, no prefixes — the polyatomic ion's name is its name. The full roster (and the -ate/-ite/per-/hypo- patterns) gets its own deep dive next article: [Polyatomic Ions](/chemistry/0205-polyatomic-ions). For now, know sulfate, nitrate, carbonate ($\ce{CO3^2-}$), hydroxide ($\ce{OH-}$), and ammonium.

### Covalent (Molecular): Count the Atoms

Two nonmetals can bond in multiple ratios, so charge balance can't rebuild the formula — the name must *count atoms explicitly* with Greek prefixes:

| # | Prefix | # | Prefix |
|---|---|---|---|
| 1 | mono- | 6 | hexa- |
| 2 | di- | 7 | hepta- |
| 3 | tri- | 8 | octa- |
| 4 | tetra- | 9 | nona- |
| 5 | penta- | 10 | deca- |

**Rules:**
1. Prefix + first element name, prefix + second element root + **-ide**.
2. **Drop mono- on the first element only.** $\ce{CO}$ is *carbon monoxide*, not "monocarbon monoxide."
3. Vowel smoothing: "monooxide" → "monoxide," "pentaoxide" → often written "pentoxide."

$$\ce{CO} \rightarrow \text{carbon monoxide} \qquad \ce{CO2} \rightarrow \text{carbon dioxide}$$
$$\ce{N2O4} \rightarrow \text{dinitrogen tetroxide} \qquad \ce{P4O10} \rightarrow \text{tetraphosphorus decoxide}$$

One-pump versus two-pump matters here more than anywhere: $\ce{CO}$ binds your hemoglobin and is lethal; $\ce{CO2}$ is what you exhale. The prefix is doing life-or-death work.

### Acids: The Secret Menu

An acid is a hydrogen-containing compound dissolved in water ($\ce{HCl(g)}$ is "hydrogen chloride," but $\ce{HCl(aq)}$ is *hydrochloric acid* — same molecules, different context, different name).

**Binary acids** ($\ce{H}$ + one other element, no oxygen): **hydro-** + root + **-ic acid**.

$$\ce{HCl(aq)} \rightarrow \text{hydrochloric acid} \qquad \ce{H2S(aq)} \rightarrow \text{hydrosulfuric acid}$$

**Oxyacids** ($\ce{H}$ + polyatomic ion containing oxygen): no hydro- prefix. Convert the anion suffix:

$$\text{-ate} \rightarrow \text{-ic acid} \qquad \text{-ite} \rightarrow \text{-ous acid}$$

Mnemonic: "I **ate** something **ic**ky; the sprite was right**eous**."

| Anion | Acid |
|---|---|
| $\ce{SO4^2-}$ sulf**ate** | $\ce{H2SO4}$ sulfur**ic** acid |
| $\ce{SO3^2-}$ sulf**ite** | $\ce{H2SO3}$ sulfur**ous** acid |
| $\ce{NO3-}$ nitr**ate** | $\ce{HNO3}$ nitr**ic** acid |
| $\ce{NO2-}$ nitr**ite** | $\ce{HNO2}$ nitr**ous** acid |

### The Trivial Names You Just Have to Know

A few compounds predate the systematic rules and kept their street names. Nobody says "dihydrogen monoxide":

| Formula | Name (never anything else) |
|---|---|
| $\ce{H2O}$ | water |
| $\ce{NH3}$ | ammonia |
| $\ce{CH4}$ | methane |
| $\ce{N2O}$ | usually "dinitrogen monoxide," but famously **laughing gas** (nitrous oxide) |

---

## Worked Examples

### Example 1: Type I Ionic, Formula → Name

**Problem:** Name $\ce{K2S}$.

**Solution:**

**Step 1:** Run the decision tree. Potassium is a metal, sulfur a nonmetal → ionic rules.

**Step 2:** Potassium is Group 1 → fixed charge ($1+$) → Type I, no Roman numeral.

**Step 3:** Cation name + anion root + -ide: potassium + sulfide. Ignore the subscript 2 — ionic names never count atoms.

**Answer: potassium sulfide**

### Example 2: Type I Ionic, Name → Formula

**Problem:** Write the formula for calcium nitride.

**Solution:**

**Step 1:** Identify the ions: $\ce{Ca^2+}$ (Group 2, always $2+$) and nitride $= \ce{N^3-}$.

**Step 2:** Balance charge to zero. Least common multiple of 2 and 3 is 6: three $\ce{Ca^2+}$ gives $6+$, two $\ce{N^3-}$ gives $6-$.

**Step 3:** Write subscripts: $\ce{Ca3N2}$.

**Answer: $\ce{Ca3N2}$**

### Example 3: Type II Ionic, Reverse-Engineering the Charge

**Problem:** Name $\ce{Fe2O3}$.

**Solution:**

**Step 1:** Metal + nonmetal → ionic. Iron is a transition metal → Type II, Roman numeral required.

**Step 2:** Anchor on the anion: oxide is always $\ce{O^2-}$. Three oxides = $6-$ total.

**Step 3:** Two iron atoms must supply $6+$ total → each iron is $3+$.

**Step 4:** Roman numeral states the *per-ion* charge, not the subscript: iron(III).

**Answer: iron(III) oxide**

### Example 4: The Classic Trap — $\ce{Cu2O}$

**Problem:** Name $\ce{Cu2O}$.

**Solution:**

**Step 1:** Copper is a transition metal → Type II.

**Step 2:** Anchor: one $\ce{O^2-}$ = $2-$ total.

**Step 3:** Two coppers share $2+$ → each copper is only $1+$. The subscript 2 tempts you toward copper(II) — that's the trap. Copper(II) oxide would be $\ce{CuO}$.

**Answer: copper(I) oxide**

### Example 5: Type II, Name → Formula — $\ce{SnCl4}$'s Sibling Pair

**Problem:** Write formulas for tin(II) chloride and tin(IV) chloride.

**Solution:**

**Step 1:** The Roman numeral hands you the cation charge directly: $\ce{Sn^2+}$ and $\ce{Sn^4+}$. Chloride is $\ce{Cl-}$.

**Step 2:** Balance each: $\ce{Sn^2+}$ needs 2 chlorides → $\ce{SnCl2}$; $\ce{Sn^4+}$ needs 4 → $\ce{SnCl4}$.

**Step 3:** Sanity check: same two elements, two legit compounds — exactly *why* Type II metals need the numeral.

**Answer: $\ce{SnCl2}$ and $\ce{SnCl4}$**

### Example 6: No-Numeral Metals

**Problem:** Name $\ce{ZnCl2}$ and $\ce{AgNO3}$.

**Solution:**

**Step 1:** Zinc and silver are transition metals, but they're on the fixed-charge exception list: $\ce{Zn^2+}$ always, $\ce{Ag+}$ always. No Roman numeral.

**Step 2:** $\ce{ZnCl2}$: zinc + chloride → zinc chloride.

**Step 3:** $\ce{AgNO3}$: silver + the intact polyatomic name nitrate → silver nitrate.

**Answer: zinc chloride; silver nitrate**

### Example 7: Polyatomic Ions, Both Directions

**Problem:** (a) Name $\ce{Na2SO4}$. (b) Write the formula for ammonium nitrate.

**Solution:**

**Step 1 (a):** Sodium (Group 1, $1+$) + sulfate ($\ce{SO4^2-}$) — keep the polyatomic name intact, no -ide: sodium sulfate.

**Step 2 (b):** Ammonium is $\ce{NH4+}$, nitrate is $\ce{NO3-}$. Charges are $1+$ and $1-$ → 1:1 ratio.

**Step 3 (b):** Write the units side by side: $\ce{NH4NO3}$. Do *not* merge the atoms into $\ce{N2H4O3}$ — the ion identities must stay visible.

**Answer: (a) sodium sulfate; (b) $\ce{NH4NO3}$**

### Example 8: Covalent, Formula → Name

**Problem:** Name $\ce{N2O4}$ and $\ce{P4O10}$.

**Solution:**

**Step 1:** Two nonmetals each → covalent prefix rules.

**Step 2:** $\ce{N2O4}$: di- (2 N) + nitrogen, tetra- (4 O) + oxide, vowel-smoothed → dinitrogen tetroxide.

**Step 3:** $\ce{P4O10}$: tetra- (4 P) + phosphorus, deca- (10 O) + oxide → tetraphosphorus decoxide.

**Answer: dinitrogen tetroxide; tetraphosphorus decoxide**

### Example 9: Covalent, Name → Formula (and the mono- rule)

**Problem:** Write formulas for carbon monoxide, sulfur hexafluoride, and dinitrogen monoxide.

**Solution:**

**Step 1:** Carbon monoxide: no prefix on carbon means one C (mono- dropped on first element); mon(o)- oxide = one O → $\ce{CO}$.

**Step 2:** Sulfur hexafluoride: one S, hexa- = six F → $\ce{SF6}$.

**Step 3:** Dinitrogen monoxide: two N, one O → $\ce{N2O}$ — laughing gas, the anesthetic at the dentist's office.

**Answer: $\ce{CO}$, $\ce{SF6}$, $\ce{N2O}$**

### Example 10: Binary Acid

**Problem:** Name $\ce{HBr(aq)}$, and write the formula for hydrofluoric acid.

**Solution:**

**Step 1:** Starts with $\ce{H}$, aqueous → acid rules. No oxygen → binary acid: hydro- + root + -ic.

**Step 2:** $\ce{HBr(aq)}$ → hydrobromic acid. (Pure gas $\ce{HBr(g)}$ would be "hydrogen bromide.")

**Step 3:** Hydrofluoric acid → fluoride is $\ce{F-}$, so one $\ce{H+}$ balances it → $\ce{HF}$.

**Answer: hydrobromic acid; $\ce{HF}$**

### Example 11: Oxyacid Pairs

**Problem:** Name $\ce{H2SO4}$ and $\ce{H2SO3}$.

**Solution:**

**Step 1:** Starts with $\ce{H}$, contains oxygen → oxyacid rules (no hydro-).

**Step 2:** $\ce{H2SO4}$ contains sulf**ate** ($\ce{SO4^2-}$): -ate → -ic → sulfuric acid.

**Step 3:** $\ce{H2SO3}$ contains sulf**ite** ($\ce{SO3^2-}$): -ite → -ous → sulfurous acid.

**Answer: sulfuric acid; sulfurous acid**

### Example 12: Full Decision-Tree Gauntlet

**Problem:** Classify and name: (a) $\ce{BaF2}$, (b) $\ce{Cl2O7}$, (c) $\ce{HNO2(aq)}$.

**Solution:**

**Step 1 (a):** Barium = metal, fluorine = nonmetal → ionic Type I (Ba is Group 2, always $2+$) → barium fluoride.

**Step 2 (b):** Chlorine and oxygen are both nonmetals → covalent → dichlorine heptoxide.

**Step 3 (c):** Starts with $\ce{H}$, aqueous, contains oxygen → oxyacid. Contains nitr**ite** ($\ce{NO2-}$) → -ite → -ous → nitrous acid.

**Answer: (a) barium fluoride, (b) dichlorine heptoxide, (c) nitrous acid**

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Using prefixes on ionic compounds ("magnesium dichloride") | Covalent grammar leaking into the ionic menu | Run the decision tree *first*; ionic names never count atoms |
| Reading the Roman numeral as a subscript (iron(III) chloride → "$\ce{Fe3Cl}$") | The numeral *looks* like a count | The numeral is the **charge per metal ion**; balance it against the anion |
| Copying the subscript into the numeral ($\ce{Cu2O}$ → "copper(II) oxide") | Subscript 2 sits right there, begging | Reverse-engineer: total anion charge ÷ number of metal atoms |
| Roman numerals on Ag, Zn, Cd, Al ("aluminum(III) oxide") | Overgeneralizing the transition-metal rule | Memorize the four no-numeral metals: $\ce{Ag+}, \ce{Zn^2+}, \ce{Cd^2+}, \ce{Al^3+}$ |
| Adding -ide to polyatomic ions ("sodium sulfide" for $\ce{Na2SO4}$) | -ide reflex from monatomic anions | -ide is for single-element anions; polyatomic names stay intact (sulfate ≠ sulfide!) |
| Forgetting to drop mono- on the first element ("monocarbon dioxide") | Applying the prefix table too literally | mono- is dropped on the first element only, kept on the second ($\ce{CO}$ = carbon **mon**oxide) |
| "Hydrosulfuric" vs. "sulfuric" confusion | Both are acids of sulfur | hydro- means **no oxygen**: $\ce{H2S(aq)}$ hydrosulfuric; $\ce{H2SO4}$ sulfuric |
| Merging polyatomic ions when writing formulas ($\ce{NH4NO3}$ → "$\ce{N2H4O3}$") | Treating the formula as an atom inventory | Polyatomic ions are sealed units — write them intact |

---

## AP Exam Tips

- **Naming is almost never a question — it's the price of admission.** The AP exam rarely asks "name this compound" outright, but nearly every FRQ hands you compounds *by name*. Misread "iron(II) sulfate" as $\ce{Fe2(SO4)3}$ instead of $\ce{FeSO4}$ and your molar mass is wrong, your moles are wrong, and an entire stoichiometry FRQ torpedoes itself in line one — with no partial credit rescuing a wrong formula.
- **The Roman numeral trap is the #1 killer.** Drill the pairs until automatic: iron(II)/iron(III), copper(I)/copper(II), tin(II)/tin(IV), lead(II)/lead(IV).
- **Net ionic equations (Unit 4) require instant ion recognition.** When a question says "aqueous silver nitrate is added to sodium chloride solution," you must produce $\ce{Ag+ + Cl- -> AgCl(s)}$ in seconds. That speed starts here.
- **Acid names appear constantly in Units 4 and 8.** "Nitrous acid" vs. "nitric acid" is a one-letter difference between a weak acid and a strong acid — and weak-vs-strong changes the entire equilibrium setup.
- **Writing answers:** if you're asked for a formula, give the formula with correct subscripts; if asked for a name, spell it out. Readers do accept minor spelling wobbles, but "sulfate" written as "sulfide" is a chemistry error, not a spelling error.

---

## Practice Problems

### Problem 1
Name the following: (a) $\ce{LiF}$, (b) $\ce{CaO}$, (c) $\ce{K3N}$.

<details>
<summary><strong>Solution</strong></summary>

All are metal + nonmetal with fixed-charge metals → Type I ionic (no numerals, no prefixes).

(a) lithium + fluoride
(b) calcium + oxide
(c) potassium + nitride (subscript 3 is not named)

**Answer: (a) lithium fluoride, (b) calcium oxide, (c) potassium nitride**

</details>

### Problem 2
Write formulas for: (a) sodium oxide, (b) aluminum chloride, (c) magnesium phosphide.

<details>
<summary><strong>Solution</strong></summary>

Balance each pair of charges to zero.

(a) $\ce{Na+}$ and $\ce{O^2-}$: two sodiums per oxide → $\ce{Na2O}$
(b) $\ce{Al^3+}$ and $\ce{Cl-}$: three chlorides per aluminum → $\ce{AlCl3}$
(c) $\ce{Mg^2+}$ and $\ce{P^3-}$: LCM of 2 and 3 is 6 → three Mg ($6+$), two P ($6-$) → $\ce{Mg3P2}$

**Answer: (a) $\ce{Na2O}$, (b) $\ce{AlCl3}$, (c) $\ce{Mg3P2}$**

</details>

### Problem 3
Name $\ce{PbO2}$.

<details>
<summary><strong>Solution</strong></summary>

Lead is a variable-charge metal → Type II. Anchor on the anion: two $\ce{O^2-}$ = $4-$ total. One lead atom must be $4+$ → lead(IV).

**Answer: lead(IV) oxide**

</details>

### Problem 4
Name $\ce{Cu2S}$ and $\ce{CuS}$.

<details>
<summary><strong>Solution</strong></summary>

Sulfide is always $\ce{S^2-}$.

$\ce{Cu2S}$: two coppers share $2+$ → each is $1+$ → copper(I) sulfide.
$\ce{CuS}$: one copper balances $2-$ → copper is $2+$ → copper(II) sulfide.

Note how the *smaller* subscript on copper means the *larger* charge — the inverse relationship that trips everyone.

**Answer: $\ce{Cu2S}$ = copper(I) sulfide; $\ce{CuS}$ = copper(II) sulfide**

</details>

### Problem 5
Write formulas for: (a) iron(II) sulfate, (b) iron(III) sulfate.

<details>
<summary><strong>Solution</strong></summary>

Sulfate is $\ce{SO4^2-}$.

(a) $\ce{Fe^2+}$ with $\ce{SO4^2-}$: charges match 1:1 → $\ce{FeSO4}$
(b) $\ce{Fe^3+}$ with $\ce{SO4^2-}$: LCM of 3 and 2 is 6 → two Fe ($6+$), three sulfates ($6-$), parentheses required → $\ce{Fe2(SO4)3}$

This is *the* pair from the AP Exam Tips — get these backwards and a whole stoichiometry FRQ collapses.

**Answer: (a) $\ce{FeSO4}$, (b) $\ce{Fe2(SO4)3}$**

</details>

### Problem 6
Name $\ce{AgCl}$, $\ce{ZnO}$, and $\ce{Al2S3}$. Explain why none of them takes a Roman numeral.

<details>
<summary><strong>Solution</strong></summary>

Silver, zinc, and aluminum are on the fixed-charge exception list ($\ce{Ag+}$, $\ce{Zn^2+}$, $\ce{Al^3+}$), so there is no ambiguity for a numeral to resolve.

**Answer: silver chloride, zinc oxide, aluminum sulfide — each metal has only one possible charge, so no Roman numeral is needed**

</details>

### Problem 7
Name $\ce{K2CO3}$ and write the formula for calcium hydroxide.

<details>
<summary><strong>Solution</strong></summary>

$\ce{K2CO3}$: potassium + carbonate ($\ce{CO3^2-}$, name kept intact) → potassium carbonate.

Calcium hydroxide: $\ce{Ca^2+}$ needs two $\ce{OH-}$ → parentheses around the polyatomic unit → $\ce{Ca(OH)2}$.

**Answer: potassium carbonate; $\ce{Ca(OH)2}$**

</details>

### Problem 8
Name the following covalent compounds: (a) $\ce{CO}$, (b) $\ce{CO2}$, (c) $\ce{CCl4}$.

<details>
<summary><strong>Solution</strong></summary>

Two nonmetals each → prefix rules; drop mono- on the first element.

(a) one C (mono- dropped), one O → carbon monoxide
(b) one C, two O → carbon dioxide
(c) one C, four Cl → carbon tetrachloride

**Answer: (a) carbon monoxide, (b) carbon dioxide, (c) carbon tetrachloride**

</details>

### Problem 9
Write formulas for: (a) dinitrogen pentoxide, (b) diphosphorus trisulfide, (c) xenon hexafluoride.

<details>
<summary><strong>Solution</strong></summary>

Prefixes translate directly to subscripts.

(a) di-N, pent(a)-O → $\ce{N2O5}$
(b) di-P, tri-S → $\ce{P2S3}$
(c) one Xe, hexa-F → $\ce{XeF6}$

**Answer: (a) $\ce{N2O5}$, (b) $\ce{P2S3}$, (c) $\ce{XeF6}$**

</details>

### Problem 10
$\ce{N2O}$ is "laughing gas." Give its systematic name, and explain why "nitrogen oxide" would be an unacceptable name.

<details>
<summary><strong>Solution</strong></summary>

Two N, one O → di- + nitrogen, mon- + oxide → dinitrogen monoxide.

"Nitrogen oxide" is ambiguous: $\ce{N2O}$, $\ce{NO}$, $\ce{NO2}$, $\ce{N2O3}$, $\ce{N2O4}$, and $\ce{N2O5}$ all exist. Covalent compounds *must* count atoms with prefixes precisely because the same two nonmetals combine in many ratios — the one-name-one-formula contract would break otherwise.

**Answer: dinitrogen monoxide (nitrous oxide); the name must specify the ratio because multiple nitrogen oxides exist**

</details>

### Problem 11
Name: (a) $\ce{HI(aq)}$, (b) $\ce{HNO3(aq)}$, (c) $\ce{H2SO3(aq)}$.

<details>
<summary><strong>Solution</strong></summary>

All start with $\ce{H}$ and are aqueous → acid rules.

(a) No oxygen → binary: hydro- + iod + -ic → hydroiodic acid
(b) Contains nitr**ate** ($\ce{NO3-}$) → -ate → -ic → nitric acid
(c) Contains sulf**ite** ($\ce{SO3^2-}$) → -ite → -ous → sulfurous acid

**Answer: (a) hydroiodic acid, (b) nitric acid, (c) sulfurous acid**

</details>

### Problem 12
Write formulas for: (a) hydrochloric acid, (b) nitrous acid, (c) carbonic acid (carbonate is $\ce{CO3^2-}$).

<details>
<summary><strong>Solution</strong></summary>

(a) hydro- = no oxygen; chloride $\ce{Cl-}$ + one $\ce{H+}$ → $\ce{HCl}$
(b) -ous → -ite anion: nitrite $\ce{NO2-}$ + one $\ce{H+}$ → $\ce{HNO2}$
(c) -ic → -ate anion: carbonate $\ce{CO3^2-}$ needs two $\ce{H+}$ → $\ce{H2CO3}$

**Answer: (a) $\ce{HCl}$, (b) $\ce{HNO2}$, (c) $\ce{H2CO3}$**

</details>

### Problem 13
Explain why $\ce{HCl}$ has two different names depending on its state, and give both.

<details>
<summary><strong>Solution</strong></summary>

As a pure gas, $\ce{HCl(g)}$ is a covalent molecule named like one: **hydrogen chloride**. Dissolved in water, it ionizes to $\ce{H+(aq)}$ and $\ce{Cl-(aq)}$ and behaves as an acid, earning the acid name: **hydrochloric acid**. Same molecule, different menu — the (aq) is the signal that flips you to acid rules.

**Answer: $\ce{HCl(g)}$ = hydrogen chloride; $\ce{HCl(aq)}$ = hydrochloric acid**

</details>

### Problem 14
Classify each compound (ionic Type I, ionic Type II, covalent, or acid) and name it: (a) $\ce{SnCl4}$, (b) $\ce{SCl4}$, (c) $\ce{SrCl2}$, (d) $\ce{HCl(aq)}$.

<details>
<summary><strong>Solution</strong></summary>

The pair (a)/(b) is the classic trap — one letter apart, different menus.

(a) $\ce{SnCl4}$: tin is a *metal* → ionic Type II. Four $\ce{Cl-}$ = $4-$ → tin is $4+$ → **tin(IV) chloride** (never "tin tetrachloride").
(b) $\ce{SCl4}$: sulfur is a *nonmetal* → covalent → **sulfur tetrachloride** (prefixes required).
(c) $\ce{SrCl2}$: strontium is Group 2 → ionic Type I → **strontium chloride**.
(d) $\ce{HCl(aq)}$: acid, no oxygen → **hydrochloric acid**.

**Answer: (a) ionic Type II, tin(IV) chloride; (b) covalent, sulfur tetrachloride; (c) ionic Type I, strontium chloride; (d) acid, hydrochloric acid**

</details>

### Problem 15
A stoichiometry FRQ begins: "A student dissolves 15.2 g of iron(II) sulfate in water..." Your friend writes $\ce{Fe2(SO4)3}$ (molar mass $399.9$ g/mol) instead of the correct formula (molar mass $151.9$ g/mol). By what factor is your friend's mole calculation off?

<details>
<summary><strong>Solution</strong></summary>

Correct: iron(II) means $\ce{Fe^2+}$, which pairs 1:1 with $\ce{SO4^2-}$ → $\ce{FeSO4}$, molar mass $55.85 + 32.07 + 4(16.00) = 151.9$ g/mol.

$$n_{\text{correct}} = \frac{15.2}{151.9} = 0.100 \text{ mol} \qquad n_{\text{friend}} = \frac{15.2}{399.9} = 0.0380 \text{ mol}$$

$$\frac{0.100}{0.0380} \approx 2.63$$

Every downstream answer — limiting reactant, mass of product, concentration — inherits this factor. One misread Roman numeral, entire FRQ torpedoed.

**Answer: the mole count is too small by a factor of about 2.6 ($399.9/151.9 \approx 2.63$)**

</details>

---

## Quick Reference

| Category | How to spot it | Naming rule | Example |
|---|---|---|---|
| Ionic Type I | Metal (Group 1, 2, Al, Zn, Ag, Cd) + nonmetal | cation + anion-ide; no prefixes, no numerals | $\ce{CaO}$ = calcium oxide |
| Ionic Type II | Transition/variable metal + nonmetal | cation + (charge in Roman numerals) + anion-ide | $\ce{Fe2O3}$ = iron(III) oxide |
| Ionic w/ polyatomic | Contains $\ce{SO4^2-}$, $\ce{NO3-}$, $\ce{NH4+}$, etc. | keep polyatomic name intact | $\ce{Na2SO4}$ = sodium sulfate |
| Covalent | Two nonmetals | Greek prefixes count atoms; drop mono- on first element | $\ce{N2O4}$ = dinitrogen tetroxide |
| Binary acid | $\ce{H}$ + nonmetal, (aq), no oxygen | hydro-\_\_\_-ic acid | $\ce{HCl(aq)}$ = hydrochloric acid |
| Oxyacid | $\ce{H}$ + oxygen-containing anion, (aq) | -ate → -ic acid; -ite → -ous acid | $\ce{H2SO4}$ = sulfuric acid |
| Trivial names | Just memorize | — | $\ce{H2O}$ water, $\ce{NH3}$ ammonia, $\ce{CH4}$ methane |

**No-numeral metals:** $\ce{Ag+}$, $\ce{Zn^2+}$, $\ce{Cd^2+}$, $\ce{Al^3+}$
**Prefixes:** mono, di, tri, tetra, penta, hexa, hepta, octa, nona, deca

---

<div align="center">

[← Ionic vs Covalent](/chemistry/0203-ionic-vs-covalent) | [Polyatomic Ions →](/chemistry/0205-polyatomic-ions)

</div>
