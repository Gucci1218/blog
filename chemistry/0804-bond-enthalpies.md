# Bond Enthalpies
<p class="article-date">July 5, 2026</p>

*Last summer at the beach bonfire, I finally noticed something I'd seen a hundred times without thinking about it: you can't just wave a stick of wood in the air and have it burst into flame. You need the match. You have to spend a spark — real energy — before the fire ever gives anything back. But once it catches, the flames pour out heat and light way beyond that tiny match. Where does all that extra energy come from? Here's the secret the whole fire is hiding: to burn, you first have to rip apart the bonds inside the fuel and inside the $\ce{O2}$ in the air (that costs energy — that's your match). Then the freed atoms snap into brand-new bonds — $\ce{CO2}$ and $\ce{H2O}$ — and forming bonds RELEASES energy. The magic is that the new bonds pay back MORE than the old ones cost, and the leftover pours out as the campfire. This is AP Topic 6.7, and it's the most literal payoff of everything you learned back in Unit 2 about breaking and forming bonds.*

---

## What You'll Learn
- State the master principle: **breaking bonds absorbs energy** (endothermic, $+$), **forming bonds releases energy** (exothermic, $-$)
- Define **bond enthalpy** as the energy to break one mole of a specific bond in the gas phase — and know it is always positive
- Apply the master formula $\ce{\Delta H_{rxn} \approx \Sigma(bonds\ broken) - \Sigma(bonds\ formed)}$ and explain *why* it has that exact form and sign
- Draw a correct **Lewis structure** first and count every bond — single, double, and triple — before plugging into the formula
- Calculate $\Delta H$ for combustion, hydrogenation, and synthesis reactions from a bond-enthalpy table
- Explain why bond enthalpies give only an **approximate**, **gas-phase** $\Delta H$ (averages + phase), and why that differs from formation-based methods
- Predict whether a reaction is exothermic or endothermic by comparing the strength of reactant bonds versus product bonds
- Back-calculate an unknown bond enthalpy when given the reaction's $\Delta H$

---

## Prerequisites
- [Bond Energy and Length](/chemistry/0402-bond-energy-and-length) — the one sentence this whole article rests on: **breaking a bond absorbs energy, forming a bond releases it.** This is the big payoff of that PE-well diagram.
- [Lewis Structures](/chemistry/0404-lewis-structures) — you can't count bonds you can't see. Every calculation starts by drawing the molecule and counting single/double/triple bonds correctly.
- [Enthalpy of Reaction](/chemistry/0803-enthalpy-of-reaction) — $\Delta H$, its sign convention, and what exothermic vs. endothermic means at the level of the whole reaction.

---

## The Core Concept

### Intuition First

Let's stay at the bonfire and go frame by frame, because the fire acts out the entire formula for us.

**Frame 1 — you strike the match (breaking bonds costs energy).** Wood is mostly molecules full of $\ce{C-H}$, $\ce{C-C}$, and $\ce{C-O}$ bonds; the air is full of $\ce{O=O}$. None of these atoms *want* to let go of their partners — remember the PE well from [Bond Energy and Length](/chemistry/0402-bond-energy-and-length)? Every bond is a valley, and climbing an atom out of that valley takes an energy *investment*. That's exactly why you need the match: you have to pay an up-front energy cost to break the first bonds. **Breaking bonds always absorbs energy. Always. No exceptions.**

**Frame 2 — the atoms snap into new partners (forming bonds pays out).** Once the atoms are free, they immediately fall into *new*, even deeper valleys — carbon grabs oxygen to make $\ce{CO2}$, hydrogen grabs oxygen to make $\ce{H2O}$. Falling into a valley releases energy, the same way a ball rolling into a ditch gives up energy. **Forming bonds always releases energy. Always.**

**Frame 3 — count the change (the net is the heat).** Here's the whole trick of fire: the new $\ce{CO2}$ and $\ce{H2O}$ bonds are *stronger* — deeper valleys — than the fuel and $\ce{O2}$ bonds we broke. So the energy paid out in Frame 2 is *bigger* than the energy invested in Frame 1. The difference has to go somewhere, and it leaves as heat and light. That's your campfire.

Map it one-to-one and you literally have the formula:

| Bonfire | Chemistry | Sign |
|---|---|---|
| Striking the match | **Breaking** the fuel + $\ce{O2}$ bonds — energy you *invest* | costs $\to$ endothermic, $+$ |
| Atoms snapping into $\ce{CO2}$ + $\ce{H2O}$ | **Forming** the product bonds — energy *returned* | releases $\to$ exothermic, $-$ |
| The heat you feel | The **net**: return minus investment | $\Delta H$ |

$$\Delta H_{rxn} \approx \underbrace{\Sigma(\text{bonds broken})}_{\text{energy in — reactants}} - \underbrace{\Sigma(\text{bonds formed})}_{\text{energy out — products}}$$

If breaking costs less than forming pays out, $\Delta H$ is negative — exothermic, you get a fire. If breaking costs *more* than forming returns, $\Delta H$ is positive — endothermic, and the reaction needs energy fed to it continuously.

### What "Bond Enthalpy" Actually Means

**Bond enthalpy** (also called bond energy or bond dissociation energy) is the energy required to break **one mole** of a particular bond in the **gas phase**, splitting the molecule into gaseous atoms:

$$\ce{H2(g) -> 2H(g)} \qquad \Delta H = +436 \text{ kJ/mol}$$

Three things to burn into memory:

1. **Bond enthalpies are always positive.** They measure *breaking*, and breaking always costs energy. You never see a negative bond enthalpy in a table.
2. **Forming the same bond releases the same magnitude, with a minus sign.** Making one mole of $\ce{H-H}$ releases $436$ kJ. Breaking and forming are exact opposites — this is why the master formula can use one table for both directions.
3. **A stronger bond = a bigger bond enthalpy = a deeper PE well.** A triple bond has a much larger bond enthalpy than a single bond between the same atoms ($\ce{C#C}$ at $839$ beats $\ce{C-C}$ at $347$ kJ/mol).

### The Master Formula and Why It Works

$$\boxed{\ \Delta H_{rxn} \approx \Sigma(\text{bonds broken in reactants}) - \Sigma(\text{bonds formed in products})\ }$$

Read it as **energy in minus energy out**. Every reaction is: tear the reactants apart (pay the sum of *all* reactant bond enthalpies), then assemble the products (get back the sum of *all* product bond enthalpies). The heat of the reaction is whatever's left over:

- The first sum is **positive** (breaking = absorbing).
- The second sum is what you *release*, so it gets **subtracted**.
- Net negative $\Rightarrow$ exothermic; net positive $\Rightarrow$ endothermic.

The single most common way to lose points here is flipping this to "formed − broken." Don't. It's **broken − formed**, because you pay first and collect second.

### The Bond-Enthalpy Table We'll Use

Average bond enthalpies, in kJ/mol (yours on the AP exam will be provided):

| Bond | kJ/mol | Bond | kJ/mol | Bond | kJ/mol |
|---|---|---|---|---|---|
| $\ce{H-H}$ | 436 | $\ce{C-H}$ | 413 | $\ce{O-H}$ | 463 |
| $\ce{C-C}$ | 347 | $\ce{C=C}$ | 614 | $\ce{C#C}$ | 839 |
| $\ce{C-O}$ | 358 | $\ce{C=O}$ | 799 | $\ce{O=O}$ | 498 |
| $\ce{N-H}$ | 391 | $\ce{N-N}$ | 163 | $\ce{N#N}$ | 941 |
| $\ce{O-O}$ | 146 | $\ce{C-Cl}$ | 328 | $\ce{C-F}$ | 485 |
| $\ce{Cl-Cl}$ | 243 | $\ce{Br-Br}$ | 193 | $\ce{I-I}$ | 151 |
| $\ce{F-F}$ | 155 | $\ce{H-Cl}$ | 431 | $\ce{H-Br}$ | 366 |
| $\ce{H-I}$ | 299 | $\ce{H-F}$ | 567 | | |

---

## Worked Examples

Every calculation follows the same three moves: **(1) draw Lewis structures and count all bonds, (2) sum broken and sum formed, (3) subtract broken − formed.**

### Example 1: The Campfire — Combustion of Methane

**Problem:** Estimate $\Delta H$ for $\ce{CH4 + 2O2 -> CO2 + 2H2O}$, the flagship reaction behind natural-gas flames and burning fuel.

**Solution:**

**Step 1 — Lewis structures, count bonds.**
- $\ce{CH4}$: carbon in the center, four $\ce{C-H}$ single bonds.
- $\ce{O2}$: a double bond, $\ce{O=O}$ (we have 2 of them).
- $\ce{CO2}$: $\ce{O=C=O}$, two $\ce{C=O}$ double bonds.
- $\ce{H2O}$: two $\ce{O-H}$ bonds each (we have 2 waters $\Rightarrow$ 4 $\ce{O-H}$).

**Step 2 — Sum bonds broken (reactants):**
$$4(\ce{C-H}) + 2(\ce{O=O}) = 4(413) + 2(498) = 1652 + 996 = 2648 \text{ kJ}$$

**Step 3 — Sum bonds formed (products):**
$$2(\ce{C=O}) + 4(\ce{O-H}) = 2(799) + 4(463) = 1598 + 1852 = 3450 \text{ kJ}$$

**Step 4 — Broken − formed:**
$$\Delta H = 2648 - 3450 = -802 \text{ kJ}$$

**Answer:** $\Delta H \approx -802 \text{ kJ/mol}$. Negative $\Rightarrow$ exothermic — the fire pours out heat because forming $\ce{CO2}$ and $\ce{H2O}$ ($3450$ kJ) pays back far more than breaking $\ce{CH4}$ and $\ce{O2}$ ($2648$ kJ) cost.

### Example 2: The Simplest Case — $\ce{H2 + Cl2 -> 2HCl}$

**Problem:** Estimate $\Delta H$ for $\ce{H2 + Cl2 -> 2HCl}$.

**Solution:**

**Broken:** one $\ce{H-H}$ and one $\ce{Cl-Cl}$:
$$436 + 243 = 679 \text{ kJ}$$

**Formed:** two $\ce{H-Cl}$ bonds:
$$2(431) = 862 \text{ kJ}$$

**Broken − formed:**
$$\Delta H = 679 - 862 = -183 \text{ kJ}$$

**Answer:** $\Delta H \approx -183 \text{ kJ}$, exothermic. Notice how clean this is when every species is a diatomic with exactly one bond — no counting traps.

### Example 3: Hydrogen Combustion — $\ce{2H2 + O2 -> 2H2O}$

**Problem:** Estimate $\Delta H$ for $\ce{2H2 + O2 -> 2H2O}$.

**Solution:**

**Broken:** two $\ce{H-H}$ and one $\ce{O=O}$:
$$2(436) + 498 = 872 + 498 = 1370 \text{ kJ}$$

**Formed:** two waters, four $\ce{O-H}$:
$$4(463) = 1852 \text{ kJ}$$

**Broken − formed:**
$$\Delta H = 1370 - 1852 = -482 \text{ kJ}$$

**Answer:** $\Delta H \approx -482 \text{ kJ}$ (for 2 mol of water). This is why a hydrogen flame is ferociously hot.

### Example 4: Watch the Triple Bond — Ammonia Synthesis

**Problem:** Estimate $\Delta H$ for $\ce{N2 + 3H2 -> 2NH3}$ (the Haber process that feeds the planet).

**Solution:**

**Step 1 — count carefully.** $\ce{N2}$ is $\ce{N#N}$, a **triple bond counted as one bond** with its own value ($941$), *not* three single bonds. Each $\ce{NH3}$ has three $\ce{N-H}$ bonds, so 2 ammonias give 6 $\ce{N-H}$.

**Broken:** one $\ce{N#N}$ and three $\ce{H-H}$:
$$941 + 3(436) = 941 + 1308 = 2249 \text{ kJ}$$

**Formed:** six $\ce{N-H}$:
$$6(391) = 2346 \text{ kJ}$$

**Broken − formed:**
$$\Delta H = 2249 - 2346 = -97 \text{ kJ}$$

**Answer:** $\Delta H \approx -97 \text{ kJ}$, mildly exothermic. The huge $\ce{N#N}$ bond ($941$ kJ/mol) is why nitrogen is so unreactive — breaking it is a massive up-front cost, which is why this reaction needs high temperature and a catalyst to get going.

### Example 5: A Double Bond and the Shortcut — Hydrogenation of Ethene

**Problem:** Estimate $\Delta H$ for $\ce{C2H4 + H2 -> C2H6}$ (turning ethene into ethane, the chemistry behind hydrogenating oils).

**Solution — full method:**

**Broken:** $\ce{C2H4}$ has one $\ce{C=C}$ and four $\ce{C-H}$; plus one $\ce{H-H}$:
$$614 + 4(413) + 436 = 614 + 1652 + 436 = 2702 \text{ kJ}$$

**Formed:** $\ce{C2H6}$ has one $\ce{C-C}$ and six $\ce{C-H}$:
$$347 + 6(413) = 347 + 2478 = 2825 \text{ kJ}$$

**Broken − formed:**
$$\Delta H = 2702 - 2825 = -123 \text{ kJ}$$

**The shortcut:** most $\ce{C-H}$ bonds are untouched — four of them exist on both sides. Only the bonds that actually *change* matter, so you can break just $\ce{C=C}$ and $\ce{H-H}$ and form $\ce{C-C}$ plus two new $\ce{C-H}$:
$$(614 + 436) - (347 + 2 \times 413) = 1050 - 1173 = -123 \text{ kJ}$$

**Answer:** $\Delta H \approx -123 \text{ kJ}$ either way. The unchanged bonds cancel — but on the exam, doing the full count is the safest way to avoid missing a bond.

### Example 6: The Gas Stove — Propane Combustion

**Problem:** Estimate $\Delta H$ for $\ce{C3H8 + 5O2 -> 3CO2 + 4H2O}$ (the propane in a camp stove or backyard grill).

**Solution:**

**Step 1 — count $\ce{C3H8}$.** Propane is $\ce{H3C-CH2-CH3}$: two $\ce{C-C}$ bonds and eight $\ce{C-H}$ bonds.

**Broken:** two $\ce{C-C}$, eight $\ce{C-H}$, five $\ce{O=O}$:
$$2(347) + 8(413) + 5(498) = 694 + 3304 + 2490 = 6488 \text{ kJ}$$

**Formed:** three $\ce{CO2}$ (six $\ce{C=O}$) and four $\ce{H2O}$ (eight $\ce{O-H}$):
$$6(799) + 8(463) = 4794 + 3704 = 8498 \text{ kJ}$$

**Broken − formed:**
$$\Delta H = 6488 - 8498 = -2010 \text{ kJ}$$

**Answer:** $\Delta H \approx -2010 \text{ kJ/mol}$. Propane packs even more punch than methane — that's why one small tank runs a stove all weekend.

### Example 7: Endothermic — Splitting $\ce{HF}$

**Problem:** Estimate $\Delta H$ for $\ce{2HF -> H2 + F2}$, and explain the sign.

**Solution:**

**Broken:** two $\ce{H-F}$ bonds:
$$2(567) = 1134 \text{ kJ}$$

**Formed:** one $\ce{H-H}$ and one $\ce{F-F}$:
$$436 + 155 = 591 \text{ kJ}$$

**Broken − formed:**
$$\Delta H = 1134 - 591 = +543 \text{ kJ}$$

**Answer:** $\Delta H \approx +543 \text{ kJ}$, **endothermic**. Here we're tearing apart the very strong $\ce{H-F}$ bonds and only making weaker $\ce{H-H}$ and $\ce{F-F}$ bonds — the investment beats the payout, so energy must be *added*. This is the fire running in reverse.

### Example 8: Back Out an Unknown Bond Enthalpy

**Problem:** For $\ce{H2 + Br2 -> 2HBr}$, the measured $\Delta H = -103 \text{ kJ}$. Given $\ce{H-H} = 436$ and $\ce{Br-Br} = 193$ kJ/mol, find the $\ce{H-Br}$ bond enthalpy.

**Solution:**

Set up the master formula with $x = \ce{H-Br}$:
$$\Delta H = \underbrace{(436 + 193)}_{\text{broken}} - \underbrace{2x}_{\text{formed}}$$
$$-103 = 629 - 2x$$
$$2x = 629 + 103 = 732 \quad\Rightarrow\quad x = 366 \text{ kJ/mol}$$

**Answer:** $\ce{H-Br} \approx 366 \text{ kJ/mol}$. Whenever you know $\Delta H$ and all but one bond, treat the missing bond as an unknown and solve algebraically.

### Example 9: Why the Answer Is Only Approximate

**Problem:** Our methane number from Example 1 was $-802$ kJ, but a data booklet lists the standard enthalpy of combustion of methane as $-890$ kJ. Explain the gap.

**Solution:**

Two reasons, and the AP exam loves both:

1. **Bond enthalpies are averages.** The table's $\ce{C-H}$ value ($413$) is an *average* of $\ce{C-H}$ bonds measured across thousands of different molecules. The actual $\ce{C-H}$ bonds in methane aren't exactly $413$ — they depend on what else the carbon is attached to. Averaging bakes in small errors.
2. **Bond enthalpies are strictly gas-phase.** The method assumes every product is a gas, so it gives $\ce{H2O(g)}$. But standard combustion is measured with **liquid** water, $\ce{H2O(l)}$. Condensing gas to liquid releases extra energy, making the *real* value more negative. Our all-gas $-802$ actually matches the gas-water value nicely; the $-890$ includes the extra condensation energy.

**Answer:** Bond-enthalpy $\Delta H$ is an **estimate** because tabulated values are averages and apply only to gas-phase species. For exact answers you need [Enthalpy of Formation](/chemistry/0805-enthalpy-of-formation) or Hess's Law, which use real, phase-specific data.

### Example 10: Predicting the Sign With No Numbers

**Problem:** Without calculating, decide whether the following is exothermic or endothermic, and justify: a reaction that breaks weak $\ce{O-O}$ and $\ce{N-N}$ single bonds and forms strong $\ce{N#N}$ triple bonds and $\ce{O=O}$ double bonds.

**Solution:**

Compare bond strength. The reactant bonds ($\ce{O-O}$, $\ce{N-N}$) are weak — cheap to break. The product bonds ($\ce{N#N}$, $\ce{O=O}$) are strong — they release a lot when they form. When **product bonds are stronger than reactant bonds**, the energy out beats the energy in.

**Answer:** **Exothermic** ($\Delta H < 0$). Stronger product bonds $\Rightarrow$ more stable products $\Rightarrow$ energy released. This is exactly why explosives that make $\ce{N2}$ are so violent — that ultra-strong triple bond dumps enormous energy on forming.

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Using **formed − broken** | Feels natural to put "products − reactants" like other $\Delta H$ methods | For *bonds* it's **broken − formed**: you spend to break, then collect. Write it at the top of your scratch work every time. |
| Counting a double/triple bond as multiple single bonds | Seeing "$=$" and multiplying by 2 | A double bond is **one** bond with its **own** value ($\ce{C=O} = 799$, not $2 \times 358$). Use the table entry for the exact bond order. |
| Not drawing a Lewis structure first | Trying to count bonds from the formula alone | You'll miss lone-pair-driven double bonds (like $\ce{O=C=O}$). Always sketch it, then count. |
| Forgetting to multiply by coefficients | Counting $\ce{H2O}$ once when the equation has $2\ce{H2O}$ | Multiply each molecule's bonds by its coefficient — 2 waters = 4 $\ce{O-H}$. |
| Calling the answer exact | Bond enthalpies look precise | It's an **estimate** — averages, gas-phase only. Say "approximately." |
| Making bond enthalpy negative | Confusing it with $\Delta H$ | Bond enthalpy (breaking) is *always positive*. The minus sign lives in the formula, not the table. |

---

## AP Exam Tips

- **The formula is $\Sigma(\text{broken}) - \Sigma(\text{formed})$ — never the reverse.** This is the number-one sign error graders see. Memorize "break first (cost), form second (payout)."
- **You must count bonds from a correct Lewis structure.** FRQs frequently hand you molecules where the bond order isn't obvious ($\ce{CO2}$, $\ce{N2}$, $\ce{C2H4}$). Draw before you count.
- **Double and triple bonds are counted once, with their own table value.** $\ce{C=C}$, $\ce{C#C}$, $\ce{O=O}$, $\ce{N#N}$ each have a single entry — don't decompose them.
- **Always call bond-enthalpy $\Delta H$ "approximate" and know why:** the values are *averages*, and they apply only to *gas-phase* species. This exact limitation is a recurring free-response question, and it's why the answer differs from formation/Hess's-Law values.
- **The sign-logic explanation earns points.** If asked *why* a reaction is exothermic, write: "The bonds formed in the products are stronger (release more energy) than the bonds broken in the reactants (which absorbed energy), so net energy is released." That sentence is worth a full point.
- **Watch coefficients and per-mole reporting.** If the balanced equation makes 2 mol of product, your $\Delta H$ is for that reaction as written unless asked "per mole of X."

---

## Practice Problems

Use the bond-enthalpy table above throughout.

### Problem 1
Estimate $\Delta H$ for $\ce{H2 + F2 -> 2HF}$.

<details>
<summary><strong>Solution</strong></summary>

Broken: $\ce{H-H} + \ce{F-F} = 436 + 155 = 591$ kJ.
Formed: $2(\ce{H-F}) = 2(567) = 1134$ kJ.
$$\Delta H = 591 - 1134 = -543 \text{ kJ}$$

**Answer:** $\approx -543 \text{ kJ}$, exothermic (this is Example 7 run forward).

</details>

### Problem 2
Estimate $\Delta H$ for the chlorination $\ce{CH4 + Cl2 -> CH3Cl + HCl}$.

<details>
<summary><strong>Solution</strong></summary>

Only one $\ce{C-H}$ is replaced, so the net change is: break one $\ce{C-H}$ and one $\ce{Cl-Cl}$; form one $\ce{C-Cl}$ and one $\ce{H-Cl}$.
Broken: $413 + 243 = 656$ kJ.
Formed: $328 + 431 = 759$ kJ.
$$\Delta H = 656 - 759 = -103 \text{ kJ}$$

**Answer:** $\approx -103 \text{ kJ}$, exothermic. (Full count gives the same: reactants $1652 + 243 = 1895$; products $[3(413)+328] + 431 = 1998$; $1895 - 1998 = -103$.)

</details>

### Problem 3
Estimate $\Delta H$ for the combustion of acetylene, $\ce{2C2H2 + 5O2 -> 4CO2 + 2H2O}$ (the fuel in a welding torch). Acetylene is $\ce{H-C#C-H}$.

<details>
<summary><strong>Solution</strong></summary>

Each $\ce{C2H2}$: two $\ce{C-H}$ + one $\ce{C#C}$ $= 2(413) + 839 = 1665$; for 2 molecules $= 3330$.
Broken: $3330 + 5(\ce{O=O}) = 3330 + 5(498) = 3330 + 2490 = 5820$ kJ.
Formed: $4\ce{CO2}$ = $8(\ce{C=O}) = 8(799) = 6392$; $2\ce{H2O}$ = $4(\ce{O-H}) = 4(463) = 1852$; total $8244$ kJ.
$$\Delta H = 5820 - 8244 = -2424 \text{ kJ}$$

**Answer:** $\approx -2424 \text{ kJ}$ (for 2 mol acetylene). The triple bond stores a lot of energy — welding torches burn hot.

</details>

### Problem 4
Estimate $\Delta H$ for $\ce{C2H2 + H2 -> C2H4}$ (partial hydrogenation of ethyne to ethene).

<details>
<summary><strong>Solution</strong></summary>

Shortcut — only the changing bonds: break one $\ce{C#C}$ and one $\ce{H-H}$; form one $\ce{C=C}$ and two new $\ce{C-H}$.
Broken: $839 + 436 = 1275$ kJ.
Formed: $614 + 2(413) = 614 + 826 = 1440$ kJ.
$$\Delta H = 1275 - 1440 = -165 \text{ kJ}$$

**Answer:** $\approx -165 \text{ kJ}$, exothermic.

</details>

### Problem 5
Estimate $\Delta H$ for the addition $\ce{C2H4 + Cl2 -> C2H4Cl2}$ (chlorine adding across the double bond).

<details>
<summary><strong>Solution</strong></summary>

The $\ce{C=C}$ becomes a $\ce{C-C}$, and the $\ce{Cl-Cl}$ becomes two $\ce{C-Cl}$; the four $\ce{C-H}$ are unchanged.
Broken: $\ce{C=C} + \ce{Cl-Cl} = 614 + 243 = 857$ kJ.
Formed: $\ce{C-C} + 2(\ce{C-Cl}) = 347 + 2(328) = 347 + 656 = 1003$ kJ.
$$\Delta H = 857 - 1003 = -146 \text{ kJ}$$

**Answer:** $\approx -146 \text{ kJ}$, exothermic.

</details>

### Problem 6
The gas-phase combustion of methane (Example 1) is $\Delta H = -802$ kJ. Using $\ce{C-H} = 413$, $\ce{O=O} = 498$, and $\ce{O-H} = 463$, back out the $\ce{C=O}$ bond enthalpy from $\ce{CH4 + 2O2 -> CO2 + 2H2O}$.

<details>
<summary><strong>Solution</strong></summary>

Let $x = \ce{C=O}$. Broken $= 4(413) + 2(498) = 2648$. Formed $= 2x + 4(463) = 2x + 1852$.
$$-802 = 2648 - (2x + 1852) = 796 - 2x$$
$$2x = 796 + 802 = 1598 \quad\Rightarrow\quad x = 799 \text{ kJ/mol}$$

**Answer:** $\ce{C=O} \approx 799 \text{ kJ/mol}$ — exactly the table value.

</details>

### Problem 7
Without any numbers, explain why *every* hydrocarbon combustion is exothermic, in terms of bond strengths.

<details>
<summary><strong>Solution</strong></summary>

Combustion breaks $\ce{C-H}$, $\ce{C-C}$, and $\ce{O=O}$ bonds and forms $\ce{C=O}$ (in $\ce{CO2}$) and $\ce{O-H}$ (in $\ce{H2O}$). The $\ce{C=O}$ and $\ce{O-H}$ product bonds are notably *stronger* than the reactant bonds broken. Because the bonds **formed** release more energy than the bonds **broken** absorb, the net is energy released.

**Answer:** Stronger product bonds $\Rightarrow$ more stable, lower-energy products $\Rightarrow$ $\Delta H < 0$, exothermic.

</details>

### Problem 8
Your friend calculates $\Delta H$ from bond enthalpies and gets $-137$ kJ, but the textbook lists $-125$ kJ. Give two reasons the two numbers legitimately differ.

<details>
<summary><strong>Solution</strong></summary>

1. **Averages:** tabulated bond enthalpies are averaged over many different molecules, so they don't exactly match the specific bonds in this reaction.
2. **Gas phase only:** bond enthalpies assume all species are gases; if the real reaction involves liquids or solids, phase-change energy isn't captured.

**Answer:** Bond-enthalpy $\Delta H$ is an approximation (averaged values, gas-phase assumption); exact values come from formation/Hess's-Law data.

</details>

### Problem 9
Estimate $\Delta H$ for the decomposition of hydrogen peroxide, $\ce{2H2O2 -> 2H2O + O2}$. Each $\ce{H2O2}$ is $\ce{H-O-O-H}$ (two $\ce{O-H}$ and one $\ce{O-O}$).

<details>
<summary><strong>Solution</strong></summary>

Each $\ce{H2O2}$: $2(\ce{O-H}) + \ce{O-O} = 2(463) + 146 = 1072$; for 2 molecules $= 2144$ kJ broken.
Formed: $2\ce{H2O}$ = $4(\ce{O-H}) = 4(463) = 1852$; $\ce{O2}$ = $\ce{O=O} = 498$; total $2350$ kJ.
$$\Delta H = 2144 - 2350 = -206 \text{ kJ}$$

**Answer:** $\approx -206 \text{ kJ}$, exothermic — which is why peroxide decomposes and fizzes on its own.

</details>

### Problem 10
Estimate $\Delta H$ for the decomposition of ammonia, $\ce{2NH3 -> N2 + 3H2}$. Is it exothermic or endothermic?

<details>
<summary><strong>Solution</strong></summary>

Broken: $6(\ce{N-H}) = 6(391) = 2346$ kJ.
Formed: $\ce{N#N} + 3(\ce{H-H}) = 941 + 3(436) = 941 + 1308 = 2249$ kJ.
$$\Delta H = 2346 - 2249 = +97 \text{ kJ}$$

**Answer:** $\approx +97 \text{ kJ}$, **endothermic** — exactly the reverse of Example 4, as it should be.

</details>

### Problem 11
Estimate $\Delta H$ for the combustion of methanol, $\ce{2CH3OH + 3O2 -> 2CO2 + 4H2O}$. Methanol is $\ce{H3C-O-H}$ (three $\ce{C-H}$, one $\ce{C-O}$, one $\ce{O-H}$).

<details>
<summary><strong>Solution</strong></summary>

Each $\ce{CH3OH}$: $3(413) + 358 + 463 = 1239 + 358 + 463 = 2060$; for 2 molecules $= 4120$.
Broken: $4120 + 3(\ce{O=O}) = 4120 + 3(498) = 4120 + 1494 = 5614$ kJ.
Formed: $2\ce{CO2}$ = $4(\ce{C=O}) = 4(799) = 3196$; $4\ce{H2O}$ = $8(\ce{O-H}) = 8(463) = 3704$; total $6900$ kJ.
$$\Delta H = 5614 - 6900 = -1286 \text{ kJ}$$

**Answer:** $\approx -1286 \text{ kJ}$ (for 2 mol methanol).

</details>

### Problem 12
For $\ce{H2 + I2 -> 2HI}$, given $\ce{H-H} = 436$ and $\ce{I-I} = 151$, the measured $\Delta H = -11$ kJ. Find the $\ce{H-I}$ bond enthalpy.

<details>
<summary><strong>Solution</strong></summary>

Let $x = \ce{H-I}$. Broken $= 436 + 151 = 587$; formed $= 2x$.
$$-11 = 587 - 2x \quad\Rightarrow\quad 2x = 598 \quad\Rightarrow\quad x = 299 \text{ kJ/mol}$$

**Answer:** $\ce{H-I} \approx 299 \text{ kJ/mol}$.

</details>

### Problem 13
On an FRQ you're asked to *explain*, in terms of bonds, why $\ce{2H2 + O2 -> 2H2O}$ releases energy. Write a complete, point-earning answer.

<details>
<summary><strong>Solution</strong></summary>

"Breaking the $\ce{H-H}$ and $\ce{O=O}$ bonds in the reactants **absorbs** energy. Forming the $\ce{O-H}$ bonds in the products **releases** energy. Because the total energy released when the product bonds form is **greater** than the total energy absorbed to break the reactant bonds, the reaction releases net energy — it is exothermic, $\Delta H < 0$."

**Answer:** The key scoring ideas: breaking absorbs, forming releases, and *formed > broken* in magnitude.

</details>

### Problem 14
Explain, using bond enthalpies, why you need a match or spark to start a campfire even though burning is exothermic overall.

<details>
<summary><strong>Solution</strong></summary>

Burning is exothermic *overall*, but the **first step is always breaking bonds**, which absorbs energy. Before any energy-releasing product bonds can form, you must invest energy to break the initial fuel and $\ce{O2}$ bonds. The match supplies that up-front energy (the activation energy). Once enough bonds break and $\ce{CO2}$/$\ce{H2O}$ bonds start forming, the released energy breaks more bonds and the fire sustains itself.

**Answer:** Breaking bonds absorbs energy, so a reaction needs an initial energy input (the match) even when the net $\Delta H$ is negative.

</details>

---

## Quick Reference

| Concept | The One-Liner |
|---|---|
| Breaking a bond | **Absorbs** energy — endothermic, $+$ (always) |
| Forming a bond | **Releases** energy — exothermic, $-$ (always) |
| Bond enthalpy | Energy to break 1 mol of a bond in the **gas phase**; always **positive** |
| Master formula | $\Delta H_{rxn} \approx \Sigma(\text{broken}) - \Sigma(\text{formed})$ |
| The order | **Broken minus formed** — spend first, collect second (never reversed) |
| First step | Draw the **Lewis structure**, count every bond |
| Multiple bonds | Counted **once** with their own value ($\ce{C=O}=799$, $\ce{N#N}=941$) |
| Coefficients | Multiply each molecule's bonds by its coefficient |
| $\Delta H < 0$ | Product bonds **stronger** than reactant bonds → exothermic |
| $\Delta H > 0$ | Reactant bonds **stronger** → endothermic |
| Why approximate | Values are **averages**, and apply to **gas-phase** species only |
| For exact $\Delta H$ | Use formation enthalpies / Hess's Law (next articles) |

---

<div align="center">

[← Enthalpy of Reaction](/chemistry/0803-enthalpy-of-reaction) | [Enthalpy of Formation →](/chemistry/0805-enthalpy-of-formation)

</div>
