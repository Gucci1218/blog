# Entropy
<p class="article-date">July 5, 2026</p>

*My room is a disaster right now, and my mom keeps saying I "let it get that way," like I made a decision one day to fling a hoodie over my desk chair and leave three water cups on the nightstand. But here's the thing I finally figured out: I never TRY to mess up my room. It just happens. Tidiness is the thing I have to work at — I have to spend a whole Sunday afternoon putting every book back in its one correct spot on the shelf. Messiness is free; it shows up on its own. And it's not because I'm lazy (okay, partly), it's pure odds: there is exactly ONE arrangement where every book is filed in order and the hoodie is on its hook, and there are literally millions of arrangements where stuff is scattered around the floor. If things drift randomly, they overwhelmingly land in "messy," just because there are so many more ways to be messy than to be neat. That single idea — nature drifts toward whatever state has the most ways to arrange things — turned into one of the deepest quantities in all of chemistry: **entropy**. This is Unit 9, Topics 9.1 and 9.2, and it's the piece that finally explains WHY some reactions happen on their own and others never do. Let's clean this up (ironically).*

---

## What You'll Learn

- Define **entropy** ($S$) as a measure of how spread out a system's energy and matter are — literally the number of ways (**microstates**) the particles and their energy can be arranged
- State the units of entropy, $\text{J/(mol·K)}$, and flag the classic trap that **entropy is in joules while enthalpy is in kilojoules**
- **Predict the sign of $\Delta S$** for a physical or chemical change — the single most tested entropy skill on the AP exam — using phase changes, moles of gas, dissolving, temperature, and volume
- Use **moles of gas** as the dominant tiebreaker for the sign of $\Delta S$ in a reaction
- **Rank substances** by absolute entropy: gas > liquid > solid, bigger/more complex > simpler, hotter > colder
- State the **third law of thermodynamics** ($S = 0$ for a perfect crystal at $0\text{ K}$) and explain why substances have **absolute** entropies — including elements, whose $S^\circ$ is **not** zero (unlike $\Delta H_f^\circ$)
- Calculate $\Delta S^\circ_{rxn}$ from a table of standard molar entropies using **products − reactants**, and check the answer against the moles-of-gas prediction
- Preview the **second law**: the entropy of the *universe* increases for any spontaneous process, and connect surroundings entropy to released heat via $\Delta S_{surr} = -\Delta H_{sys}/T$

---

## Prerequisites

- [Phase Changes](/chemistry/0503-phase-changes) — you need to already picture the states of matter as levels of molecular freedom: a solid's particles locked in a lattice, a liquid's particles sliding past each other, a gas's particles flying everywhere. That "how much can the molecules move around" ladder IS the entropy ladder, so this is the intuition entropy is built on.
- [Enthalpy of Formation](/chemistry/0805-enthalpy-of-formation) — that article drilled the "**products − reactants**, read off a table" pattern for $\Delta H^\circ$. Entropy of reaction uses the *exact same bookkeeping shape*, with one huge twist: elements are **not** zero here. Knowing the enthalpy version cold makes the contrast the whole point.

---

## The Core Concept

### Intuition First

Let's stay in my messy room, because it secretly contains the entire idea.

Think about what "messy" even means. It's not that the universe hates me. It's a **counting** fact. Imagine your room has spots for 20 things — books, hoodie, cups, chargers, shoes. There is exactly **one** arrangement we'd call "perfectly tidy": every book in its slot, hoodie on its hook, cups in the kitchen. But how many arrangements would we call "messy"? Astronomically many — hoodie on the chair OR the floor OR the bed, cup here OR there, book on the desk OR under it. Millions upon millions of scattered configurations, and we lump them all under one word: "messy."

So if stuff moves around at random — you grab a book, drop a sock, kick a shoe — where does the room end up? In "messy," basically every time. Not because messy is a goal, but because there are **vastly more ways to be messy than to be neat**. The odds are overwhelming. Neat is one lottery ticket; messy is all the other billions of tickets.

That's the whole concept. In chemistry we give the "number of ways to arrange things" a name — **microstates**, symbol $W$ — and **entropy** is a measure of it. A tidy room is *low entropy* (few arrangements). A messy room is *high entropy* (astronomically many arrangements). And the natural drift from tidy to messy, all on its own, is a **spontaneous increase in entropy**.

Here's the map, one-to-one:

| Messy room | Entropy |
|---|---|
| A tidy room — one exact arrangement | **Low entropy** — few microstates |
| A messy room — millions of scattered arrangements | **High entropy** — many microstates |
| Rooms drift messy on their own | Processes drift toward **higher entropy** (spontaneous) |
| Cleaning up takes a whole afternoon of effort | Lowering entropy **always costs energy** |
| Cleaning your room heats you up / messes up the kitchen | Lowering entropy here **dumps disorder elsewhere** |

That last row is the sneaky-deep one. You *can* clean your room — entropy isn't a law that says mess always wins everywhere. But cleaning costs you energy (you get warm, you burn calories), and you make a mess somewhere else (dishes in the sink, trash bag filling up). You lowered the entropy of the *room* only by raising the entropy of the *rest of the world* by even more. Hold onto that; it becomes the **second law** at the end of this article.

### What entropy actually is

**Entropy ($S$)** is a measure of the **dispersal of energy and matter** in a system — equivalently, the number of microscopic arrangements (**microstates**) the system's particles and energy can take on while still looking the same on the outside. More ways to spread out = higher entropy.

Two flavors of "spreading out," and both count:

- **Matter dispersal** — are the particles crammed together (solid) or free to roam a big volume (gas)? More room to roam = more entropy.
- **Energy dispersal** — is the energy concentrated in a few particles, or shared across many? More sharing = more entropy.

Ludwig Boltzmann carved the connection onto his tombstone:

$$S = k_B \ln W$$

where $W$ is the number of microstates and $k_B$ is Boltzmann's constant. You will **not** compute entropy this way on the AP exam, but it tells you everything: entropy grows with the *number of ways* to arrange things, exactly like the room. Double-check the vibe — more ways, more entropy.

**Units — read this twice.** Entropy is measured in **joules per mole per kelvin**:

$$S : \text{J/(mol·K)} \qquad\qquad \Delta H : \text{kJ/mol}$$

Entropy uses **J**. Enthalpy uses **kJ**. This mismatch is a deliberate trap on the AP exam — when you later combine them into Gibbs free energy, forgetting to convert $S$ from J to kJ (or $\Delta H$ from kJ to J) is the #1 way to lose the point. Circle it now.

### The big skill: predicting the sign of $\Delta S$

For a change, $\Delta S = S_{final} - S_{after \; minus \; before}$... let me say it cleanly: $\Delta S = S_{final} - S_{initial}$. If the system ends up *more* spread out (messier), $\Delta S > 0$. If it ends up *more* ordered (tidier), $\Delta S < 0$. Here is the entire cheat sheet for the sign:

| Entropy goes **UP** ($\Delta S > 0$) when... | Why (in room terms) |
|---|---|
| Solid → liquid → gas (melting, boiling, subliming) | particles get more freedom to roam — more arrangements |
| A reaction makes **more moles of gas** than it consumes | gas is the messiest state; more gas molecules = way more microstates |
| A solid or liquid **dissolves** into a solution | packed particles scatter and mix through the solvent |
| **Temperature increases** | particles move faster, access more energy arrangements |
| A gas **expands into a larger volume** | more room to roam = more positions available |

Reverse any of these (gas → liquid → solid, more gas → less gas, precipitating out, cooling, compressing) and $\Delta S < 0$.

**The dominant rule for reactions:** if gases are involved, **count the moles of gas on each side**. More moles of gas on the product side → $\Delta S > 0$. Fewer → $\Delta S < 0$. This one factor usually overwhelms everything else, so check it first, every time.

### Ranking substances by absolute entropy

At the same temperature, you can rank pure substances:

- **State:** gas $\gg$ liquid > solid. (Gas is a huge jump — gas particles roam thousands of times more volume.)
- **Complexity/size:** more atoms and more mass → more entropy. $\ce{C2H6}$ has more $S^\circ$ than $\ce{CH4}$; a bigger molecule has more ways to vibrate and rotate.
- **Temperature:** hotter → more entropy for the *same* substance.

So $\ce{H2O(g)} > \ce{H2O(l)} > \ce{H2O(s)}$, and $\ce{CO2(g)} > \ce{CO(g)}$ (more atoms), always at matched temperature.

### The third law and absolute entropy

Here's a distinction that trips people up, so tie it back to formation enthalpy. Enthalpy has no absolute zero — we *invented* a reference by declaring elements' $\Delta H_f^\circ = 0$. Entropy is different. The **third law of thermodynamics** gives a real, physical zero:

> A **perfect crystal at absolute zero ($0\text{ K}$)** has exactly one possible arrangement, so $W = 1$ and $S = k_B \ln 1 = 0$.

One arrangement — the ultimate tidy room, every particle frozen in its one lattice spot with zero thermal motion. From that true zero, you can measure the **absolute entropy** $S^\circ$ of any substance by warming it up and adding entropy along the way.

**The key contrast (this is an AP favorite):**

| | Formation enthalpy $\Delta H_f^\circ$ | Standard molar entropy $S^\circ$ |
|---|---|---|
| Elements in standard state | **exactly 0** (invented reference) | **NOT zero** — a positive absolute value |
| Nature of the value | a *change* relative to elements | an *absolute* amount from real zero ($0\text{ K}$) |
| Sign | can be $+$ or $-$ | almost always **positive** (anything above $0\text{ K}$ has some disorder) |

So $\ce{O2(g)}$ has $\Delta H_f^\circ = 0$ but $S^\circ = 205\ \text{J/(mol·K)}$. Elements carry real entropy. **Never** zero out an element in an entropy calculation the way you would in an enthalpy calculation.

### Entropy of reaction: products − reactants

To get the standard entropy change of a reaction, use the exact same shape as formation enthalpy — read absolute entropies off a table, weight by coefficients, subtract:

$$\Delta S^\circ_{rxn} = \sum n\,S^\circ(\text{products}) - \sum n\,S^\circ(\text{reactants})$$

The *only* difference from the enthalpy version: **every substance contributes, elements included**, because no $S^\circ$ is zero. After you compute a number, **sanity-check its sign against the moles-of-gas prediction** — if the math says $\Delta S < 0$ but you made more gas, you slipped somewhere.

A small table of standard molar entropies we'll reuse (all $S^\circ$ in J/(mol·K), at $298\text{ K}$):

| Substance | $S^\circ$ | Substance | $S^\circ$ |
|---|---|---|---|
| $\ce{H2(g)}$ | 130.7 | $\ce{H2O(l)}$ | 69.9 |
| $\ce{O2(g)}$ | 205.2 | $\ce{H2O(g)}$ | 188.8 |
| $\ce{N2(g)}$ | 191.6 | $\ce{NH3(g)}$ | 192.8 |
| $\ce{CO2(g)}$ | 213.8 | $\ce{CaCO3(s)}$ | 92.9 |
| $\ce{CO(g)}$ | 197.7 | $\ce{CaO(s)}$ | 38.1 |
| $\ce{CH4(g)}$ | 186.3 | $\ce{C(graphite)}$ | 5.7 |

### The second law (a preview of Gibbs)

Why does any of this predict *spontaneity*? Because of the **second law of thermodynamics**:

> For any **spontaneous** process, the total entropy of the **universe** increases.

$$\Delta S_{univ} = \Delta S_{sys} + \Delta S_{surr} > 0$$

The universe is your room *plus* everything outside it. You can tidy the room ($\Delta S_{sys} < 0$) only if you dump *more* disorder into the surroundings so the total still goes up. Where does that surroundings entropy come from? Mostly from **heat**. When a reaction releases heat (exothermic, $\Delta H < 0$), it pours energy into the surroundings and spreads it out there, raising $\Delta S_{surr}$:

$$\Delta S_{surr} = -\frac{\Delta H_{sys}}{T}$$

Exothermic ($\Delta H_{sys} < 0$) → $\Delta S_{surr} > 0$ (surroundings get messier). The colder it is (smaller $T$), the *bigger* that effect — a fixed chunk of heat matters more to a quiet, cold surroundings than to an already-hot one.

That's as far as we go today. In the next article, [Gibbs Free Energy](/chemistry/1102-gibbs-free-energy), we roll $\Delta S_{sys}$, $\Delta S_{surr}$, $\Delta H$, and $T$ into a single quantity $\Delta G$ that tells you spontaneity from the system alone. Everything here is the setup for that payoff.

---

## Worked Examples

### Example 1: Predict the sign of $\Delta S$ — melting ice

**Problem:** Predict the sign of $\Delta S$ for $\ce{H2O(s) -> H2O(l)}$.

**Solution:**
- Step 1: Identify the change of state. Solid → liquid.
- Step 2: Liquid particles have more freedom to move than particles locked in a crystal lattice — more microstates.
- Step 3: More disorder in the final state means entropy rises.

**Answer:** $\Delta S > 0$ (positive).

### Example 2: Predict the sign of $\Delta S$ — boiling water

**Problem:** Predict the sign of $\Delta S$ for $\ce{H2O(l) -> H2O(g)}$.

**Solution:**
- Step 1: Liquid → gas. This is the *biggest* entropy jump of all the phase changes.
- Step 2: Gas particles roam a volume thousands of times larger — a huge explosion in the number of arrangements.

**Answer:** $\Delta S > 0$ (strongly positive).

### Example 3: The dominant factor — moles of gas

**Problem:** Predict the sign of $\Delta S$ for $\ce{2SO2(g) + O2(g) -> 2SO3(g)}$.

**Solution:**
- Step 1: Count moles of gas. Reactants: $2 + 1 = 3$ mol gas. Products: $2$ mol gas.
- Step 2: Gas moles *decrease* from 3 to 2. Fewer gas molecules = fewer ways to spread out.
- Step 3: Moles of gas is the dominant factor, so this decides it.

**Answer:** $\Delta S < 0$ (negative).

### Example 4: More moles of gas produced

**Problem:** Predict the sign of $\Delta S$ for the decomposition $\ce{2H2O2(l) -> 2H2O(l) + O2(g)}$.

**Solution:**
- Step 1: Count moles of gas. Reactants: $0$ mol gas (both liquid). Products: $1$ mol gas.
- Step 2: We *create* gas from a liquid — a huge increase in disorder.

**Answer:** $\Delta S > 0$ (positive). (This is exactly why hydrogen peroxide fizzes and foams — it's manufacturing gas.)

### Example 5: A tricky one — count carefully

**Problem:** Predict the sign of $\Delta S$ for $\ce{N2(g) + 3H2(g) -> 2NH3(g)}$ (ammonia synthesis).

**Solution:**
- Step 1: Reactant gas: $1 + 3 = 4$ mol. Product gas: $2$ mol.
- Step 2: Gas moles drop from 4 to 2 — a big decrease.

**Answer:** $\Delta S < 0$ (negative). Don't be fooled that "a reaction happens" — making a molecule out of more molecules *orders* the system.

### Example 6: Dissolving a solid

**Problem:** Predict the sign of $\Delta S$ for $\ce{NaCl(s) -> Na+(aq) + Cl-(aq)}$.

**Solution:**
- Step 1: A tightly packed ionic crystal breaks apart into ions dispersed throughout the water.
- Step 2: Scattering ordered lattice particles into solution generally raises the number of arrangements.

**Answer:** $\Delta S > 0$ (positive) — dissolving a solid usually increases entropy.

### Example 7: Rank by absolute entropy

**Problem:** Rank these by increasing $S^\circ$: $\ce{H2O(l)}$, $\ce{H2O(s)}$, $\ce{H2O(g)}$.

**Solution:**
- Step 1: Same substance, so state alone decides it.
- Step 2: gas > liquid > solid.

**Answer:** $\ce{H2O(s)} < \ce{H2O(l)} < \ce{H2O(g)}$.

### Example 8: Rank by complexity

**Problem:** Which has the higher standard molar entropy, $\ce{CH4(g)}$ or $\ce{C2H6(g)}$? Both are gases.

**Solution:**
- Step 1: Same state (gas), so break the tie with size/complexity.
- Step 2: $\ce{C2H6}$ is the bigger molecule (more atoms, more mass, more ways to vibrate and rotate).

**Answer:** $\ce{C2H6(g)}$ has the higher $S^\circ$.

### Example 9: Absolute entropy vs. formation enthalpy contrast

**Problem:** For $\ce{N2(g)}$ in its standard state, state $\Delta H_f^\circ$ and whether $S^\circ$ is zero.

**Solution:**
- Step 1: $\ce{N2(g)}$ is an element in its standard state, so by the invented enthalpy reference, $\Delta H_f^\circ = 0$.
- Step 2: Entropy uses a *real* zero (perfect crystal at $0\text{ K}$). $\ce{N2}$ at $298\text{ K}$ is a freely flying gas — enormous disorder. Its $S^\circ = 191.6\ \text{J/(mol·K)}$, nowhere near zero.

**Answer:** $\Delta H_f^\circ = 0$, but $S^\circ = 191.6\ \text{J/(mol·K)} \neq 0$. Elements have zero formation enthalpy but nonzero absolute entropy.

### Example 10: Compute $\Delta S^\circ_{rxn}$ from a table

**Problem:** Find $\Delta S^\circ_{rxn}$ for $\ce{2H2(g) + O2(g) -> 2H2O(g)}$ using the table above.

**Solution:**
- Step 1: Write products − reactants, weighting by coefficients:
$$\Delta S^\circ = [\,2\,S^\circ(\ce{H2O,g})\,] - [\,2\,S^\circ(\ce{H2,g}) + 1\,S^\circ(\ce{O2,g})\,]$$
- Step 2: Plug in values: products $= 2(188.8) = 377.6$. Reactants $= 2(130.7) + 205.2 = 261.4 + 205.2 = 466.6$.
- Step 3: Subtract: $377.6 - 466.6 = -89.0\ \text{J/(mol·K)}$.
- Step 4: Sign check — gas moles go from $3$ to $2$, a decrease, so $\Delta S < 0$. Matches.

**Answer:** $\Delta S^\circ_{rxn} = -89.0\ \text{J/(mol·K)}$.

### Example 11: Compute $\Delta S^\circ_{rxn}$ — decomposition

**Problem:** Find $\Delta S^\circ_{rxn}$ for $\ce{CaCO3(s) -> CaO(s) + CO2(g)}$ using the table.

**Solution:**
- Step 1: Products − reactants:
$$\Delta S^\circ = [\,S^\circ(\ce{CaO,s}) + S^\circ(\ce{CO2,g})\,] - [\,S^\circ(\ce{CaCO3,s})\,]$$
- Step 2: Plug in: products $= 38.1 + 213.8 = 251.9$. Reactants $= 92.9$.
- Step 3: Subtract: $251.9 - 92.9 = +159.0\ \text{J/(mol·K)}$.
- Step 4: Sign check — we create $1$ mol of gas from a solid, so $\Delta S > 0$. Matches.

**Answer:** $\Delta S^\circ_{rxn} = +159.0\ \text{J/(mol·K)}$.

### Example 12: Surroundings entropy from released heat

**Problem:** A reaction releases heat with $\Delta H_{sys} = -286\ \text{kJ}$ at $298\text{ K}$. Find $\Delta S_{surr}$.

**Solution:**
- Step 1: Use $\Delta S_{surr} = -\dfrac{\Delta H_{sys}}{T}$. Keep units consistent — convert $\Delta H$ to joules: $-286\ \text{kJ} = -286000\ \text{J}$.
- Step 2: $\Delta S_{surr} = -\dfrac{-286000\ \text{J}}{298\ \text{K}} = +\dfrac{286000}{298} = +960\ \text{J/K}$.
- Step 3: Sign check — exothermic reaction dumps heat into the surroundings and spreads it out, so surroundings entropy should rise. Positive. Matches.

**Answer:** $\Delta S_{surr} = +960\ \text{J/K}$ (the surroundings get messier).

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Mixing J and kJ | Entropy is in J, enthalpy in kJ — they *look* like they should match | Before combining $\Delta H$ and $\Delta S$, convert one so both are in J (or both in kJ). Write the unit next to every number. |
| Treating elements' $S^\circ$ as zero | Muscle memory from $\Delta H_f^\circ = 0$ for elements | Elements have **nonzero** absolute entropy. Every substance contributes to $\Delta S^\circ_{rxn}$ — no exceptions. |
| Counting all species instead of gases for the sign | Forgetting gas dominates | For $\Delta S$ sign, count **moles of gas** first; solids and liquids barely move the needle. |
| Forgetting coefficients | Rushing the table lookup | Weight each $S^\circ$ by its balanced coefficient, just like the enthalpy formula. |
| Reversing products − reactants | Sign slips | It's always **products − reactants**. Same order as $\Delta H^\circ_{rxn}$. |
| Saying "spontaneous means $\Delta S_{sys} > 0$" | Confusing system with universe | Spontaneity is about $\Delta S_{univ} = \Delta S_{sys} + \Delta S_{surr}$. The system can order itself if the surroundings disorder more. |
| Assuming dissolving always raises $S$ | Overgeneralizing | Usually true, but some ions organize water so tightly that $\Delta S$ can be slightly negative. On AP, "dissolving raises entropy" is the safe default unless told otherwise. |

---

## AP Exam Tips

- **Sign of $\Delta S$ from moles of gas is the money skill.** When a reaction has gases, count moles of gas on each side *first*. More gas → $\Delta S > 0$; less gas → $\Delta S < 0$. This decides most multiple-choice entropy questions in one step.
- **gas > liquid > solid**, always, for ranking or predicting. Phase change to a gas is the biggest entropy jump.
- **Entropy is in J, enthalpy in kJ.** This unit mismatch is a deliberate trap, especially when Gibbs free energy asks you to combine them. Convert before you combine.
- **Elements have nonzero $S^\circ$** — this is the favorite "gotcha" contrasting entropy with $\Delta H_f^\circ = 0$. On an FRQ, never drop an element from an entropy sum.
- **$\Delta S^\circ_{rxn}$ = products − reactants**, each weighted by coefficient — identical shape to the formation-enthalpy formula, but *no* term is zero.
- **The second law = the entropy of the universe increases** for any spontaneous change. If a free-response asks *why* an ordering reaction is still spontaneous, the answer is the surroundings gained more entropy (from released heat) than the system lost.
- **Always sanity-check a computed $\Delta S^\circ$ against the gas count.** If the sign disagrees, you made an arithmetic or lookup error.

---

## Practice Problems

### Problem 1
Predict the sign of $\Delta S$ for $\ce{CO2(s) -> CO2(g)}$ (dry ice subliming).

<details>
<summary><strong>Solution</strong></summary>

Solid → gas (sublimation) skips the liquid entirely and is a massive increase in molecular freedom.

**Answer:** $\Delta S > 0$ (strongly positive).

</details>

---

### Problem 2
Predict the sign of $\Delta S$ for $\ce{2NO2(g) -> N2O4(g)}$.

<details>
<summary><strong>Solution</strong></summary>

Gas moles: reactants $= 2$, products $= 1$. Fewer gas molecules means fewer arrangements.

**Answer:** $\Delta S < 0$ (negative).

</details>

---

### Problem 3
Predict the sign of $\Delta S$ for $\ce{H2O(g) -> H2O(l)}$ (steam condensing).

<details>
<summary><strong>Solution</strong></summary>

Gas → liquid removes the enormous freedom of gas particles; the system becomes more ordered.

**Answer:** $\Delta S < 0$ (negative).

</details>

---

### Problem 4
Predict the sign of $\Delta S$ for $\ce{C(s) + O2(g) -> CO2(g)}$.

<details>
<summary><strong>Solution</strong></summary>

Gas moles: reactants $= 1$ ($\ce{O2}$), products $= 1$ ($\ce{CO2}$). Gas moles are equal, so the dominant factor is a wash. The tiebreaker: a solid ($\ce{C}$) is consumed and folded into a gas product, a slight increase in disorder, plus $\ce{CO2}$ is more complex than $\ce{O2}$. Expect a small positive value.

**Answer:** $\Delta S > 0$ (small positive). Actual $\approx +2.9\ \text{J/(mol·K)}$ — close to zero, exactly because gas moles don't change.

</details>

---

### Problem 5
Predict the sign of $\Delta S$ for $\ce{2Na(s) + Cl2(g) -> 2NaCl(s)}$.

<details>
<summary><strong>Solution</strong></summary>

Gas moles: reactants $= 1$ ($\ce{Cl2}$), products $= 0$ (solid $\ce{NaCl}$). Gas is consumed and locked into a solid lattice.

**Answer:** $\Delta S < 0$ (negative).

</details>

---

### Problem 6
Rank by increasing $S^\circ$ at the same temperature: $\ce{Br2(l)}$, $\ce{Br2(g)}$, $\ce{Br2(s)}$.

<details>
<summary><strong>Solution</strong></summary>

Same substance, so state decides: gas > liquid > solid.

**Answer:** $\ce{Br2(s)} < \ce{Br2(l)} < \ce{Br2(g)}$.

</details>

---

### Problem 7
Which has higher $S^\circ$: $\ce{CO(g)}$ or $\ce{CO2(g)}$?

<details>
<summary><strong>Solution</strong></summary>

Both gases, so break the tie by complexity. $\ce{CO2}$ has more atoms (3 vs 2) and more ways to vibrate/rotate.

**Answer:** $\ce{CO2(g)}$ has higher $S^\circ$.

</details>

---

### Problem 8
Explain why a perfect crystal at $0\text{ K}$ has $S = 0$, and why almost nothing in a real lab does.

<details>
<summary><strong>Solution</strong></summary>

At $0\text{ K}$ a perfect crystal has every particle frozen in exactly one lattice position with no thermal motion — only one possible microstate ($W = 1$), so $S = k_B \ln 1 = 0$. Any real sample is above $0\text{ K}$, so its particles vibrate and can occupy many arrangements ($W > 1$), giving positive entropy.

**Answer:** $S = 0$ requires the single-microstate perfection of a flawless crystal at absolute zero; real substances are warmer and disordered, so $S > 0$.

</details>

---

### Problem 9
True or false: an element in its standard state has $S^\circ = 0$. Explain.

<details>
<summary><strong>Solution</strong></summary>

False. That's the rule for $\Delta H_f^\circ$ (an invented reference), not entropy. Entropy is measured from a *real* zero at $0\text{ K}$, and any element at $298\text{ K}$ has real thermal disorder, so $S^\circ > 0$. For example, $\ce{O2(g)}$ has $\Delta H_f^\circ = 0$ but $S^\circ = 205\ \text{J/(mol·K)}$.

**Answer:** False — elements have zero formation enthalpy but nonzero absolute entropy.

</details>

---

### Problem 10
Compute $\Delta S^\circ_{rxn}$ for $\ce{N2(g) + 3H2(g) -> 2NH3(g)}$ using the table.

<details>
<summary><strong>Solution</strong></summary>

Products − reactants:
$$\Delta S^\circ = 2\,S^\circ(\ce{NH3}) - [\,S^\circ(\ce{N2}) + 3\,S^\circ(\ce{H2})\,]$$
Products $= 2(192.8) = 385.6$. Reactants $= 191.6 + 3(130.7) = 191.6 + 392.1 = 583.7$.
$\Delta S^\circ = 385.6 - 583.7 = -198.1\ \text{J/(mol·K)}$.
Sign check: gas moles $4 \to 2$, decrease, so negative. Matches.

**Answer:** $\Delta S^\circ_{rxn} = -198.1\ \text{J/(mol·K)}$.

</details>

---

### Problem 11
Compute $\Delta S^\circ_{rxn}$ for $\ce{2CO(g) + O2(g) -> 2CO2(g)}$ using the table.

<details>
<summary><strong>Solution</strong></summary>

$$\Delta S^\circ = 2\,S^\circ(\ce{CO2}) - [\,2\,S^\circ(\ce{CO}) + S^\circ(\ce{O2})\,]$$
Products $= 2(213.8) = 427.6$. Reactants $= 2(197.7) + 205.2 = 395.4 + 205.2 = 600.6$.
$\Delta S^\circ = 427.6 - 600.6 = -173.0\ \text{J/(mol·K)}$.
Sign check: gas moles $3 \to 2$, decrease, so negative. Matches.

**Answer:** $\Delta S^\circ_{rxn} = -173.0\ \text{J/(mol·K)}$.

</details>

---

### Problem 12
A combustion releases $\Delta H_{sys} = -890\ \text{kJ}$ at $298\text{ K}$. Find $\Delta S_{surr}$.

<details>
<summary><strong>Solution</strong></summary>

Convert: $-890\ \text{kJ} = -890000\ \text{J}$.
$$\Delta S_{surr} = -\frac{\Delta H_{sys}}{T} = -\frac{-890000}{298} = +2987\ \text{J/K}$$
Exothermic → surroundings gain entropy → positive. Matches.

**Answer:** $\Delta S_{surr} = +2987\ \text{J/K}$ (about $+2990\ \text{J/K}$).

</details>

---

### Problem 13
For the same amount of heat released, is $\Delta S_{surr}$ larger at $250\text{ K}$ or at $500\text{ K}$? Explain.

<details>
<summary><strong>Solution</strong></summary>

$\Delta S_{surr} = -\Delta H_{sys}/T$. With $\Delta H$ fixed, a smaller $T$ in the denominator gives a larger magnitude. A fixed chunk of heat matters more to cold, quiet surroundings than to already-hot ones.

**Answer:** Larger at $250\text{ K}$.

</details>

---

### Problem 14
A reaction has $\Delta S_{sys} = -50\ \text{J/K}$ but is observed to be spontaneous. What must be true about the surroundings?

<details>
<summary><strong>Solution</strong></summary>

By the second law, spontaneity requires $\Delta S_{univ} = \Delta S_{sys} + \Delta S_{surr} > 0$. Since $\Delta S_{sys} = -50\ \text{J/K}$, we need $\Delta S_{surr} > +50\ \text{J/K}$ so the total is positive. The surroundings must gain more than $50\ \text{J/K}$ — typically because the reaction is exothermic and dumps heat outward.

**Answer:** $\Delta S_{surr} > +50\ \text{J/K}$, so that $\Delta S_{univ} > 0$.

</details>

---

### Problem 15
Predict the sign of $\Delta S$ for $\ce{NH4NO3(s) -> NH4+(aq) + NO3-(aq)}$ (the reaction inside an instant cold pack), then use it to argue how such a pack can still activate on its own even though it feels cold (endothermic).

<details>
<summary><strong>Solution</strong></summary>

A solid dissolving into dispersed ions in solution scatters ordered lattice particles throughout the water, so $\Delta S_{sys} > 0$ (positive). The pack feels cold because dissolving *absorbs* heat (endothermic, $\Delta H > 0$), which by itself would *lower* $\Delta S_{surr}$. But the large positive $\Delta S_{sys}$ from dissolving can outweigh the surroundings' loss, keeping $\Delta S_{univ} > 0$, so the process is spontaneous even while cooling down.

**Answer:** $\Delta S_{sys} > 0$; the entropy gain from dissolving drives the process despite it being endothermic.

</details>

---

## Quick Reference

| Concept | Key fact |
|---|---|
| Entropy $S$ | Measure of energy/matter dispersal = number of microstates; more spread out = higher $S$ |
| Units | $\text{J/(mol·K)}$ — **joules**, while enthalpy is in **kJ** (unit trap) |
| $\Delta S > 0$ when | solid→liquid→gas, more moles of gas, dissolving, higher $T$, gas expands |
| Dominant sign rule | Count **moles of gas**: more gas → $\Delta S > 0$ |
| State ranking | gas $\gg$ liquid > solid; bigger/more complex > simpler; hotter > colder |
| Third law | Perfect crystal at $0\text{ K}$ has $S = 0$ (one microstate) |
| Absolute entropy | Every substance has $S^\circ > 0$ — **elements are NOT zero** (unlike $\Delta H_f^\circ$) |
| Reaction entropy | $\Delta S^\circ_{rxn} = \sum n\,S^\circ(\text{products}) - \sum n\,S^\circ(\text{reactants})$, every term counts |
| Second law | Spontaneous ⟺ $\Delta S_{univ} = \Delta S_{sys} + \Delta S_{surr} > 0$ |
| Surroundings | $\Delta S_{surr} = -\dfrac{\Delta H_{sys}}{T}$ — exothermic raises it |

---

<div align="center">

[← Titration Curves](/chemistry/1005-titration-curves) | [Gibbs Free Energy →](/chemistry/1102-gibbs-free-energy)

</div>
