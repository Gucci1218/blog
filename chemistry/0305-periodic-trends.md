# Periodic Trends
<p class="article-date">July 4, 2026</p>

*Every spring our PE department runs a tug-of-war tournament on the field, and by junior year you learn the three things that actually decide a match. First: how many people are pulling on your side — more pullers, stronger pull. Second: how long the rope is — a flag tied way out at the far end barely feels the anchor's yank, while a flag near the anchor gets whipped around instantly. Third: whether your strongest pullers are actually gripping the rope or standing in front of the anchor blocking him, soaking up his pull before it ever reaches the flag. It turns out every single periodic trend in AP Chemistry — atomic size, ionization energy, electronegativity, all of them — is that exact tug-of-war: the nucleus is the anchor pulling on the outer electrons, its proton count sets the pull strength, the shell number sets the rope length, and the inner electrons are the teammates standing in the way, blocking the pull. Learn to judge one match with the three-word checklist **protons, distance, shielding**, and you can answer every trend question the AP exam will ever throw at you — and I mean every one.*

---

## What You'll Learn
- Use Coulomb's law ($F \propto \frac{q_1 q_2}{r^2}$) as the single physical explanation behind every periodic trend
- Estimate effective nuclear charge with $Z_{eff} \approx Z - (\text{core electrons})$ and explain why it climbs across a period but stays roughly flat down a group
- Predict and explain the trends in atomic radius across a period and down a group using the protons–distance–shielding checklist
- Compare ionic radii: why cations shrink, why anions swell, and how to rank an isoelectronic series
- Predict trends in first ionization energy — and explain the two famous exceptions ($\ce{Be} \to \ce{B}$ and $\ce{N} \to \ce{O}$) with electron configurations
- Read a table of successive ionization energies and identify an element's group from the giant jump
- State the general trends in electron affinity and electronegativity, and explain why electron affinity is the messy one
- Connect metallic character to the same tug-of-war logic and back to the periodic table map
- Write a full-credit AP justification using the 3-sentence template: trend, protons/$Z_{eff}$, distance/shielding

---

## Prerequisites
- [Electron Configuration](/chemistry/0303-electron-configuration) — you need to know which electrons are core and which are valence, and what $2p$ vs. $2s$ means, before you can count shielders and spot the exceptions
- [Periodic Table Map](/chemistry/0202-periodic-table-map) — groups, periods, and the metal/nonmetal staircase; trends are directions on that map, so you need the map first

---

## The Core Concept

### Intuition First

Back to the field. Picture one atom as one tug-of-war setup:

| Tug-of-war | Atom | What it controls |
|---|---|---|
| The **anchor** pulling the rope | The **nucleus** | Source of all the attraction |
| **Number of pullers** on the anchor's side | **Number of protons** ($Z$) | Raw pull strength |
| **Length of rope** out to the flag | **Distance** to the outer electron (shell number $n$) | Attraction dies off fast with distance |
| **Teammates standing in front of the anchor**, absorbing the pull | **Core (inner) electrons** shielding the valence electrons | Blocked pull never reaches the flag |
| The **flag** at the far end | The **outermost (valence) electron** | The thing every trend is about |

Every trend question is asking one thing: *how tightly does this nucleus hold its outermost electron?* And the answer always comes from the same three-word checklist:

> **Protons. Distance. Shielding.**

- More **protons** → stronger pull on the flag.
- More **distance** → weaker pull (and it falls off *fast* — the rope gets longer and the flag barely twitches).
- More **shielding** → weaker pull (blockers soak up the attraction before it reaches the outer electron).

Hold an atom tightly and it's small, hard to ionize, and greedy in bonds. Hold it loosely and it's big, easy to ionize, and generous with its electrons. Same match, different scoreboard. We'll run this checklist in *every single section below* — the repetition is the point, because it's also exactly how you earn points on the AP exam.

### Coulomb's Law Made Usable

The physics under the tug-of-war is Coulomb's law, and the AP exam expects you to invoke it by name ("Coulombic attraction"):

$$F \propto \frac{q_1 q_2}{r^2}$$

Two things to read off this formula:

1. **Bigger charges pull harder.** Double the nuclear charge $q_1$, double the attraction on the electron.
2. **Distance kills attraction fast.** The $r^2$ in the denominator means doubling the distance cuts the force to a *quarter*. A valence electron one shell farther out isn't slightly looser — it's dramatically looser.

But the outer electron doesn't feel the full nuclear charge, because the core electrons stand between it and the nucleus, canceling part of the pull. The charge it *actually* feels is the **effective nuclear charge**, and AP uses a beautifully simple approximation:

$$Z_{eff} \approx Z - (\text{number of core electrons})$$

Core electrons are the inner-shell electrons (the noble-gas core from [Electron Configuration](/chemistry/0303-electron-configuration)); they're the blockers. Valence electrons in the *same* shell barely block each other — they're standing side by side at the flag, not in front of the anchor.

**Run the numbers across period 3** (core = the 10 electrons of the $\ce{Ne}$ core for all of them):

| Element | $\ce{Na}$ | $\ce{Mg}$ | $\ce{Al}$ | $\ce{Si}$ | $\ce{P}$ | $\ce{S}$ | $\ce{Cl}$ | $\ce{Ar}$ |
|---|---|---|---|---|---|---|---|---|
| $Z$ | 11 | 12 | 13 | 14 | 15 | 16 | 17 | 18 |
| Core electrons | 10 | 10 | 10 | 10 | 10 | 10 | 10 | 10 |
| $Z_{eff}$ (approx.) | +1 | +2 | +3 | +4 | +5 | +6 | +7 | +8 |

**Now run them down group 1:**

| Element | $\ce{Li}$ | $\ce{Na}$ | $\ce{K}$ |
|---|---|---|---|
| $Z$ | 3 | 11 | 19 |
| Core electrons | 2 | 10 | 18 |
| $Z_{eff}$ (approx.) | +1 | +1 | +1 |
| Valence shell $n$ | 2 | 3 | 4 |

Here is the **key insight of the whole article**, the one every trend hangs on:

> **Across a period:** each step right adds a proton, but the new electron joins the *same* shell — the number of blockers doesn't change. $Z$ goes up, shielding stays flat, so $Z_{eff}$ climbs and the pull gets stronger. More pullers, same rope, same blockers → the flag gets yanked in.
>
> **Down a group:** each step down adds a whole new shell. $Z_{eff}$ stays roughly the same (the extra protons are canceled by extra core blockers), but the distance grows — and the previous valence shell becomes a fresh wall of shielders. Same net pull strength, much longer rope, more blockers → the flag barely feels the anchor.

That's it. That's the machinery. Everything from here on is just pointing this machine at different scoreboards.

### Trend 1: Atomic Radius

**The trend:** atomic radius **decreases across a period** (left → right) and **increases down a group** (top → bottom). Smallest atoms: top right (helium, then fluorine among atoms you'll be asked about). Biggest: bottom left (cesium and francium).

**Checklist — across a period (say $\ce{Na} \to \ce{Cl}$):**
- **Protons:** up from 11 to 17 — more pullers.
- **Distance:** valence electrons stay in shell $n = 3$ — same rope.
- **Shielding:** the $\ce{Ne}$ core (10 blockers) the whole way — unchanged.

Stronger pull, same rope, same blockers → the electron cloud gets reeled **in**. Radius shrinks.

**Checklist — down a group (say $\ce{Li} \to \ce{Na} \to \ce{K}$):**
- **Protons:** up, sure — but…
- **Distance:** the outermost electron sits in a brand-new, farther shell ($n = 2 \to 3 \to 4$) — much longer rope, and Coulomb's $r^2$ punishes distance brutally.
- **Shielding:** every filled shell becomes another row of blockers (2 → 10 → 18 core electrons), canceling the extra protons.

Longer rope *and* more blockers overwhelm the extra pullers → the atom swells. Radius grows.

Real numbers for flavor: $\ce{Na}$ ≈ 186 pm, $\ce{Mg}$ ≈ 160 pm, $\ce{Cl}$ ≈ 100 pm across period 3; going down group 1, $\ce{Li}$ ≈ 152 pm, $\ce{Na}$ ≈ 186 pm, $\ce{K}$ ≈ 227 pm. (You never need to memorize values — only directions and reasons.)

### Trend 2: Ionic Radius

Ions are atoms after a trade, and the tug-of-war re-balances instantly.

**Cations are smaller than their parent atoms.** When $\ce{Na}$ becomes $\ce{Na+}$, it loses its entire $n = 3$ shell — the flag isn't just pulled closer, the whole far end of the rope is gone. On top of that, 11 protons that used to share their pull among 11 electrons now pull on only 10: more pull per electron. $\ce{Na}$ ≈ 186 pm collapses to $\ce{Na+}$ ≈ 102 pm.

**Anions are larger than their parent atoms.** When $\ce{Cl}$ becomes $\ce{Cl-}$, an 18th electron crowds into a shell built for 17 protons' worth of pull. Same anchor, more flags to hold, plus extra electron–electron repulsion pushing the cloud outward. $\ce{Cl}$ ≈ 100 pm swells to $\ce{Cl-}$ ≈ 181 pm.

**Isoelectronic series — the purest tug-of-war on the exam.** Consider $\ce{O^2-}$, $\ce{F-}$, $\ce{Na+}$, $\ce{Mg^2+}$: all four have **exactly 10 electrons** in exactly the same configuration ($1s^2 2s^2 2p^6$). Run the checklist:
- **Distance:** same shells for everyone — tie.
- **Shielding:** same 2 core electrons for everyone — tie.
- **Protons:** 8, 9, 11, 12 — this is the *only* difference.

Same team of flags, same rope, same blockers — the match is decided purely by how many pullers the anchor has. More protons = tighter grip = smaller ion:

$$\ce{O^2-} \; (140\text{ pm}) > \ce{F-} \; (133\text{ pm}) > \ce{Na+} \; (102\text{ pm}) > \ce{Mg^2+} \; (72\text{ pm})$$

Same electrons, more protons, smaller ion. The AP exam *loves* isoelectronic rankings because they force you to use protons instead of vague hand-waving.

### Trend 3: Ionization Energy

**Definition:** the first ionization energy ($IE_1$) is the energy required to remove the outermost electron from a gaseous atom:

$$\ce{X(g) -> X+(g) + e-} \qquad \Delta E = IE_1 > 0 \text{ (always endothermic)}$$

In tug-of-war terms: $IE_1$ is *how hard you have to yank to rip the flag away from the anchor*. So the trend is just the atomic-radius trend read in reverse — whatever the nucleus holds tightly costs a lot to steal.

**The trend:** $IE_1$ **increases across a period** and **decreases down a group**.

**Checklist — across:** protons up, distance same, shielding same → $Z_{eff}$ climbs, the outer electron is held tighter, and ripping it away costs more. **Checklist — down:** distance up, shielding up, $Z_{eff}$ roughly flat → the outer electron is far and well-blocked, and it comes off cheap. That's why cesium ionizes with a gentle tug (376 kJ/mol) while helium takes a truck (2372 kJ/mol).

#### The Two Famous Exceptions

A smooth trend would be boring, and the AP exam knows exactly where the two dips are. Both are explained by electron *configurations*, not by the checklist — these are the two places where the fine structure of subshells overrides the proton count.

**Exception 1: $\ce{Be} \to \ce{B}$ (the new-subshell dip).**

$$\ce{Be}: 1s^2\,2s^2 \qquad \ce{B}: 1s^2\,2s^2\,2p^1$$

Boron has one more proton than beryllium, so the trend predicts a higher $IE_1$. But boron's outermost electron is the first one in the $2p$ subshell, which is **higher in energy than $2s$** (and slightly better shielded by the $2s$ pair). An electron that starts in a higher-energy seat needs *less* energy to leave. Result: $IE_1(\ce{B}) = 801$ kJ/mol $<$ $IE_1(\ce{Be}) = 899$ kJ/mol. The same dip repeats at $\ce{Mg} \to \ce{Al}$ ($3s \to 3p$).

**Exception 2: $\ce{N} \to \ce{O}$ (the pairing-repulsion dip).**

$$\ce{N}: 1s^2\,2s^2\,2p^3 \; (\uparrow)(\uparrow)(\uparrow) \qquad \ce{O}: 1s^2\,2s^2\,2p^4 \; (\uparrow\downarrow)(\uparrow)(\uparrow)$$

Nitrogen's three $2p$ electrons each get their own orbital — three flags on three separate ropes, no crowding. Oxygen's fourth $2p$ electron is forced to **pair up** in an already-occupied orbital, and two electrons crammed into the same orbital repel each other. That repulsion gives the paired electron a head start out the door. Result: $IE_1(\ce{O}) = 1314$ kJ/mol $<$ $IE_1(\ce{N}) = 1402$ kJ/mol. Repeats at $\ce{P} \to \ce{S}$.

Memorize both dips *with their reasons* — "new $p$ subshell" and "pairing repulsion." Naming the dip without the mechanism scores nothing.

#### Successive Ionization Energies: The Giant Jump

You can keep ripping electrons off: $IE_1, IE_2, IE_3, \ldots$ Each one costs more than the last (fewer electrons sharing the same protons → each survivor is held tighter). But somewhere in the sequence there's a **giant jump** — not a polite increase, a cliff. That's the moment you've run out of valence electrons and you're trying to pull a *core* electron.

In tug-of-war terms: the valence electrons are flags out on the rope — expensive but gettable. The core electrons are the blockers standing right next to the anchor, one shell closer ($r$ drops, and $\frac{1}{r^2}$ explodes) and barely shielded at all. Yanking one of *them* away is pulling a player off the core team — a completely different class of effort.

**Worked data.** A mystery element has:

| | $IE_1$ | $IE_2$ | $IE_3$ | $IE_4$ | $IE_5$ |
|---|---|---|---|---|---|
| kJ/mol | 738 | 1451 | **7733** | 10 543 | 13 630 |

$IE_2 \to IE_3$ jumps by a factor of ~5 while every other step is modest. So the atom gave up **2 electrons easily**, then hit the core wall → **2 valence electrons → Group 2** (this is magnesium). Rule: *the jump comes after the last valence electron; count the cheap ones and you've counted the group number (for main-group elements).*

### Trend 4: Electron Affinity (the messy one)

Electron affinity is the energy change when a gaseous atom **gains** an electron: $\ce{X(g) + e- -> X-(g)}$. If the nucleus holds electrons tightly (high $Z_{eff}$, short rope, few blockers), grabbing one more releases a lot of energy — so the general trend follows the checklist: **more energy released across a period, less down a group**. Halogens are the champions of *wanting* one more electron.

But EA is messier than the other trends, and AP treats it lightly. Two glitches worth knowing: adding an electron to a small $n = 2$ atom means stuffing it into a crowded room, so $\ce{Cl}$ actually releases *more* energy than $\ce{F}$; and atoms with filled or half-filled subshells ($\ce{Be}$, $\ce{N}$, noble gases) resist gaining at all. On the exam: know the general direction, know it has exceptions, and never build a whole justification on EA when IE or radius will do.

### Trend 5: Electronegativity — the Tug-of-War *Within* a Bond

Everything so far was one anchor pulling its own flag. **Electronegativity** previews Unit 2: it's how hard an atom pulls on **shared** electrons when it's bonded to another atom — two anchors, one rope, and the shared electron pair is the flag in the middle.

Same checklist decides the winner. Across a period: protons up, distance same, shielding same → stronger pull on the shared pair → **electronegativity increases across**. Down a group: longer rope, more blockers → **decreases down**. So the strongest puller in the whole league sits at the top right: **fluorine, the undefeated champion** (EN = 4.0 on the Pauling scale), with oxygen (3.5) and nitrogen/chlorine (~3.0) behind it. Noble gases mostly sit out — they rarely bond, so they usually aren't ranked.

Hold this thought for Unit 2: when two bonded atoms have *unequal* electronegativity, the shared flag sits closer to the stronger anchor — that lopsided rope is a **polar bond**, and it explains everything from why water dissolves salt to why oil doesn't. This one trend powers half of the bonding unit.

### Trend 6: Metallic Character

Remember the staircase from [Periodic Table Map](/chemistry/0202-periodic-table-map)? Metals are the elements that *lose* electrons easily. Now you know why the map looks the way it does: an element acts metallic when its grip on valence electrons is **weak** — low $Z_{eff}$, long rope, lots of blockers. So metallic character is the anti-trend: it **decreases across a period** (grip tightening → less willing to lose electrons) and **increases down a group** (grip loosening → happily loses them). Cesium, bottom left, is the most metallic element you'll be asked about; fluorine, top right, is the least. Same checklist, scoreboard flipped.

### How to Write an AP-Grade Justification: The 3-Sentence Template

Here's the secret about trend FRQs: **graders award points for the mechanism, not the trend name.** "Chlorine is smaller because radius decreases across a period" restates the question — zero points. The rubric wants Coulombic reasoning. Use this template every time:

1. **State the comparison/trend** (what is bigger/higher and in which direction).
2. **Cite protons / $Z_{eff}$** (which atom has more protons; whether $Z_{eff}$ is larger).
3. **Cite distance and/or shielding** (same shell + same shielding across; more shells + more shielding down) and tie it to Coulombic attraction.

**Model answer** — *"Explain why a chlorine atom is smaller than a sulfur atom."*

> Chlorine has a smaller atomic radius than sulfur. Chlorine has 17 protons while sulfur has 16, and since both atoms' valence electrons are in the same $n = 3$ shell shielded by the same 10 core electrons, chlorine's effective nuclear charge is greater. The stronger Coulombic attraction pulls chlorine's valence electrons closer to the nucleus, giving it the smaller radius.

Three sentences: trend, protons, distance/shielding. That's a full-credit answer, and it's the same three words as the checklist. Protons. Distance. Shielding.

---

## Worked Examples

### Example 1: Calculating Effective Nuclear Charge

**Problem:** Estimate $Z_{eff}$ for the valence electrons of $\ce{P}$ and $\ce{Al}$, and state which atom holds its valence electrons more tightly.

**Solution:**

**Step 1:** Write configurations to identify core electrons. $\ce{Al}: [\ce{Ne}]\,3s^2\,3p^1$ and $\ce{P}: [\ce{Ne}]\,3s^2\,3p^3$. Both have the 10-electron neon core.

**Step 2:** Apply $Z_{eff} \approx Z - \text{core}$. For $\ce{Al}$: $13 - 10 = +3$. For $\ce{P}$: $15 - 10 = +5$.

**Step 3:** Run the checklist. Protons: $\ce{P}$ has more. Distance: both valence shells are $n = 3$ — tie. Shielding: both shielded by 10 core electrons — tie. The only difference is pull strength.

**Answer:** $Z_{eff}(\ce{Al}) \approx +3$, $Z_{eff}(\ce{P}) \approx +5$; **phosphorus holds its valence electrons more tightly.**

### Example 2: Ranking Atomic Radii Across a Period

**Problem:** Rank $\ce{Na}$, $\ce{Al}$, and $\ce{Cl}$ from largest to smallest atomic radius, and justify.

**Solution:**

**Step 1:** Locate them: all period 3, valence shell $n = 3$, all shielded by the same $\ce{Ne}$ core.

**Step 2:** Checklist. Distance: tie. Shielding: tie. Protons: 11, 13, 17 — the deciding factor. $Z_{eff}$ runs $+1, +3, +7$.

**Step 3:** Stronger effective pull reels the electron cloud in, so radius falls as $Z_{eff}$ rises.

**Answer:** $\ce{Na} > \ce{Al} > \ce{Cl}$ — same shell and shielding, increasing protons, increasing Coulombic attraction, shrinking radius.

### Example 3: Ranking Atomic Radii in Mixed Directions

**Problem:** Rank $\ce{Na}$, $\ce{Mg}$, and $\ce{K}$ from largest to smallest atomic radius.

**Solution:**

**Step 1:** Map positions. $\ce{Na}$ and $\ce{Mg}$: period 3 neighbors. $\ce{K}$: period 4, directly below $\ce{Na}$.

**Step 2:** Down beats across for size. $\ce{K}$'s valence electron is in $n = 4$ — longer rope AND 18 core blockers instead of 10. Distance and shielding both favor $\ce{K}$ being biggest, and $Z_{eff}$ is no higher (+1). $\ce{K}$ wins.

**Step 3:** Between $\ce{Na}$ and $\ce{Mg}$: same shell, same shielding, $\ce{Mg}$ has one more proton → $\ce{Mg}$ smaller.

**Answer:** $\ce{K} > \ce{Na} > \ce{Mg}$.

### Example 4: Cation vs. Parent Atom

**Problem:** Which is larger, $\ce{Na}$ or $\ce{Na+}$? Explain with the checklist.

**Solution:**

**Step 1:** Configurations: $\ce{Na}: [\ce{Ne}]\,3s^1 \to \ce{Na+}: [\ce{Ne}]$, i.e., $1s^2 2s^2 2p^6$.

**Step 2:** Distance: the entire $n = 3$ shell is gone — the outermost electrons are now in $n = 2$. Massive distance decrease.

**Step 3:** Protons per electron: 11 protons pulled 11 electrons; now 11 protons pull only 10 — each remaining electron feels more pull, and there is less electron–electron repulsion.

**Answer:** $\ce{Na}$ (≈186 pm) is much larger than $\ce{Na+}$ (≈102 pm) — **the cation loses its outer shell and the remaining electrons are held tighter.**

### Example 5: Anion vs. Parent Atom

**Problem:** Which is larger, $\ce{Cl}$ or $\ce{Cl-}$? Explain.

**Solution:**

**Step 1:** Protons: 17 in both — the anchor's team doesn't change.

**Step 2:** Electrons: 17 → 18, all in the same $n = 3$ shell. Same number of pullers now stretched across more flags: less attraction per electron.

**Step 3:** The added electron also increases electron–electron repulsion inside the valence shell, pushing the cloud outward.

**Answer:** $\ce{Cl-}$ (≈181 pm) is larger than $\ce{Cl}$ (≈100 pm) — **same protons, more electrons, more repulsion, weaker grip per electron.**

### Example 6: Ranking an Isoelectronic Series

**Problem:** Rank $\ce{O^2-}$, $\ce{F-}$, $\ce{Na+}$, and $\ce{Mg^2+}$ from largest to smallest radius, and justify in one sentence.

**Solution:**

**Step 1:** Count electrons: $8+2$, $9+1$, $11-1$, $12-2$ — all have 10 electrons, all with configuration $1s^2 2s^2 2p^6$. Isoelectronic.

**Step 2:** Checklist: distance — identical shells, tie. Shielding — identical, tie. Protons — 8, 9, 11, 12. The match is decided *purely* by pull strength.

**Step 3:** More protons pulling the same 10 electrons → tighter, smaller ion.

**Answer:** $\ce{O^2-} > \ce{F-} > \ce{Na+} > \ce{Mg^2+}$ — **same electrons and shielding, so the ion with the most protons pulls the shared cloud in tightest.**

### Example 7: Ranking First Ionization Energies

**Problem:** Rank $\ce{Ne}$, $\ce{Na}$, and $\ce{Mg}$ from highest to lowest first ionization energy.

**Solution:**

**Step 1:** $\ce{Ne}$ ($1s^2 2s^2 2p^6$): valence electron in $n = 2$, shielded by only 2 core electrons, $Z_{eff} \approx 10 - 2 = +8$. Short rope, few blockers, huge pull — extremely hard to ionize.

**Step 2:** $\ce{Na}$ vs. $\ce{Mg}$: both lose an $n = 3$ electron shielded by 10 core electrons; $Z_{eff}$ is $+1$ vs. $+2$. Same rope, same blockers, magnesium has more pull → $\ce{Mg}$ costs more.

**Step 3:** Assemble: $\ce{Ne}$ (2081 kJ/mol) crushes both; then $\ce{Mg}$ (738) over $\ce{Na}$ (496).

**Answer:** $\ce{Ne} > \ce{Mg} > \ce{Na}$.

### Example 8: The $\ce{Be} \to \ce{B}$ Exception

**Problem:** The first ionization energy of $\ce{B}$ (801 kJ/mol) is *lower* than that of $\ce{Be}$ (899 kJ/mol), even though boron has more protons. Explain using electron configurations.

**Solution:**

**Step 1:** Configurations: $\ce{Be}: 1s^2\,2s^2$; $\ce{B}: 1s^2\,2s^2\,2p^1$.

**Step 2:** The electron removed from $\ce{Be}$ comes from the $2s$ subshell. The electron removed from $\ce{B}$ is the lone $2p$ electron — and the $2p$ subshell is **higher in energy** than $2s$ (it is also shielded slightly by the $2s^2$ pair).

**Step 3:** An electron starting from a higher-energy subshell needs less added energy to escape, and this subshell effect outweighs boron's one extra proton.

**Answer:** **Boron's outermost electron occupies the higher-energy $2p$ subshell, so despite the larger nuclear charge it is easier to remove than beryllium's $2s$ electron.**

### Example 9: The $\ce{N} \to \ce{O}$ Exception

**Problem:** Explain why $IE_1(\ce{O}) = 1314$ kJ/mol is less than $IE_1(\ce{N}) = 1402$ kJ/mol.

**Solution:**

**Step 1:** Orbital diagrams for the $2p$ subshell. $\ce{N}\;(2p^3)$: $(\uparrow)(\uparrow)(\uparrow)$ — one electron per orbital (Hund's rule), no pairing. $\ce{O}\;(2p^4)$: $(\uparrow\downarrow)(\uparrow)(\uparrow)$ — one orbital holds a pair.

**Step 2:** The two electrons sharing one orbital in oxygen repel each other strongly — that **pairing repulsion** raises the energy of the paired electron, partially offsetting the nuclear attraction.

**Step 3:** Removing that destabilized paired electron takes less energy than removing one of nitrogen's unpaired, unbothered electrons — even though oxygen has one more proton.

**Answer:** **Electron–electron repulsion in oxygen's doubly occupied $2p$ orbital makes its fourth $p$ electron easier to remove, so oxygen's first ionization energy dips below nitrogen's.**

### Example 10: Identifying a Group from Successive Ionization Energies

**Problem:** An unknown main-group element has $IE_1 = 578$, $IE_2 = 1817$, $IE_3 = 2745$, and $IE_4 = 11{,}577$ kJ/mol. What group is it in, and could it be $\ce{Al}$ or $\ce{Si}$?

**Solution:**

**Step 1:** Scan for the cliff. $IE_1 \to IE_2$ triples (normal-ish), $IE_2 \to IE_3$ is modest, but $IE_3 \to IE_4$ jumps by a factor of **4+** — that's the wall.

**Step 2:** The jump comes when the fourth electron must be ripped from the *core* — one full shell closer to the nucleus (tiny $r$, so Coulombic attraction explodes) and barely shielded. Three electrons came off at valence prices → **3 valence electrons**.

**Step 3:** Three valence electrons → Group 13. $\ce{Al}$ ($[\ce{Ne}]\,3s^2 3p^1$) fits; $\ce{Si}$ has 4 valence electrons and would jump after $IE_4$, not $IE_3$.

**Answer:** **Group 13 — consistent with $\ce{Al}$, not $\ce{Si}$.**

### Example 11: Ranking Electronegativities

**Problem:** Rank $\ce{C}$, $\ce{O}$, $\ce{F}$, and $\ce{S}$ from most to least electronegative, and state which atom would win the pull for shared electrons in a $\ce{C-O}$ bond.

**Solution:**

**Step 1:** Across period 2: $\ce{C} < \ce{O} < \ce{F}$ — protons increase, same $n = 2$ shell, same 2-electron shielding, so the pull on shared electrons strengthens rightward. $\ce{F}$ is the overall champion (4.0).

**Step 2:** $\ce{S}$ vs. $\ce{O}$: same group, but sulfur's bonding electrons are in $n = 3$ with 10 blockers instead of 2 — longer rope, more shielding, weaker pull. $\ce{O} > \ce{S}$. Sulfur (2.6) lands near carbon (2.5), just above it.

**Step 3:** In a $\ce{C-O}$ bond, the two anchors pull the same shared pair; oxygen's higher electronegativity means the pair sits closer to oxygen.

**Answer:** $\ce{F} > \ce{O} > \ce{S} > \ce{C}$; **oxygen wins the shared-electron tug-of-war in $\ce{C-O}$** — a preview of bond polarity in Unit 2.

### Example 12: Writing the Full 3-Sentence Justification

**Problem:** *AP-style:* "Rubidium has a larger atomic radius than lithium. Justify this statement in terms of Coulombic attraction."

**Solution:**

**Step 1 (state the trend):** Identify the comparison — radius increases down group 1 from $\ce{Li}$ to $\ce{Rb}$.

**Step 2 (protons/$Z_{eff}$):** Note that although $\ce{Rb}$ has more protons, its effective nuclear charge is about the same as lithium's (~$+1$) because each added shell of core electrons cancels the added protons.

**Step 3 (distance/shielding):** Cite the deciding factors — $\ce{Rb}$'s valence electron is in $n = 5$ vs. lithium's $n = 2$, and it is shielded by 36 core electrons vs. 2.

**Answer (model response):** **"Rubidium's valence electron occupies the $n = 5$ shell, much farther from the nucleus than lithium's $n = 2$ electron. Although rubidium has more protons, its 36 core electrons shield the valence electron, so the effective nuclear charge felt is similar to lithium's. Because Coulombic attraction weakens rapidly with distance, rubidium's valence electron is held more loosely and its radius is larger."** — trend, protons, distance/shielding: full credit.

---

## Common Mistakes

| The mistake | Why it happens | How to avoid it |
|---|---|---|
| Justifying with "it wants a full octet" | Octets feel like an explanation | Octet-talk earns **zero points** on trend FRQs. The rubric wants Coulombic attraction: protons, distance, shielding. |
| Restating the trend as the reason ("smaller because radius decreases across") | The trend *sounds* like a why | The trend is the *what*. Always follow with the 3-sentence template. |
| Saying shielding increases across a period | "More electrons = more shielding" feels natural | Added electrons across a period join the **same valence shell** — they barely shield each other. Core count (and thus shielding) stays flat across; it jumps only when you drop a row. |
| Ranking isoelectronic ions by "more electrons = bigger" | Works for atoms vs. their own ions, so students overapply it | In an isoelectronic series everyone has the *same* electrons — only proton count differs. More protons = smaller. |
| Forgetting the $\ce{Be}\to\ce{B}$ and $\ce{N}\to\ce{O}$ dips | The general trend is easier to remember | Flag columns 2→13 (new $p$ subshell) and 15→16 (pairing repulsion). The exam tests exactly these. |
| Naming the exception without the mechanism | "B is an exception" feels complete | Say *why*: "$2p$ is higher in energy than $2s$" / "pairing repulsion in the doubly occupied $2p$ orbital." |
| Comparing $Z_{eff}$ alone for atoms in *different* periods | The across-period habit | Down a group, $Z_{eff}$ is roughly constant; **distance and shielding** decide. Always check whether the shell number changed. |
| Claiming $\ce{F}$ releases the most energy on gaining an electron | F is the electronegativity champ, so it "should" win EA too | Electron affinity is the messy trend — $\ce{Cl}$ beats $\ce{F}$ because fluorine's tiny $n=2$ shell is crowded. Keep EA claims general. |
| Confusing ionization energy (removing) with electron affinity (adding) | Both are "energy + electron" ideas | IE: yank the flag away (always costs energy). EA: hand the anchor an extra flag (often releases energy). |

---

## AP Exam Tips

- **"In terms of Coulombic attraction" is mandatory language.** When an FRQ says *justify in terms of Coulombic attraction* (and even when it doesn't), your answer must reference nuclear charge/protons and distance/shielding. The three-word checklist *is* the rubric: **protons, distance, shielding**.
- **Never justify with octets.** "Sodium wants to lose an electron to achieve a full octet" is an automatic lost point. Atoms don't want anything; nuclei pull and electrons sit where the energy is lowest.
- **Rank-and-justify is the standard FRQ format.** You'll be given 2–4 species and asked to order them *and* explain. The ranking alone is usually worth little — the mechanism sentence carries the points. Use the 3-sentence template every time.
- **The two IE exceptions are exam favorites.** $\ce{Be}\to\ce{B}$ / $\ce{Mg}\to\ce{Al}$ (new $p$ subshell) and $\ce{N}\to\ce{O}$ / $\ce{P}\to\ce{S}$ (pairing repulsion). Be ready to draw the orbital diagram for the pairing argument.
- **Successive IE tables appear on both multiple choice and FRQs.** Find the giant jump; the number of "cheap" electrons before it equals the number of valence electrons, which identifies the group.
- **This topic chains directly to PES** ([Photoelectron Spectroscopy](/chemistry/0304-photoelectron-spectroscopy)): binding energies in a PES spectrum are ionization energies, subshell by subshell. A question can hand you a spectrum and ask a trends question about it.
- **You get the periodic table but no trend arrows.** The AP reference table gives positions only — directions and mechanisms live in your head.
- **Isoelectronic rankings must cite protons.** If every species has the same configuration, the *only* legal argument is nuclear charge.

---

## Practice Problems

### Problem 1
Rank $\ce{Mg}$, $\ce{Si}$, and $\ce{S}$ from largest to smallest atomic radius and justify in one sentence using the checklist.

<details>
<summary><strong>Solution</strong></summary>

All three are period 3: valence electrons in $n = 3$ (distance — tie), shielded by the same 10-electron $\ce{Ne}$ core (shielding — tie). Protons: 12, 14, 16, so $Z_{eff} \approx +2, +4, +6$. More protons with the same distance and shielding → stronger Coulombic attraction → smaller atom.

**Answer: $\ce{Mg} > \ce{Si} > \ce{S}$ — same shell and shielding, increasing nuclear charge pulls the valence electrons in tighter.**

</details>

### Problem 2
Rank $\ce{F}$, $\ce{Cl}$, and $\ce{Br}$ from smallest to largest atomic radius, and identify which checklist factors decide it.

<details>
<summary><strong>Solution</strong></summary>

Same group (17), so $Z_{eff}$ is roughly the same (~$+7$) all the way down — protons are canceled by core blockers. The deciding factors are **distance** (valence shells $n = 2, 3, 4$) and **shielding** (2, 10, 28 core electrons). Longer rope plus more blockers → weaker hold → bigger atom going down.

**Answer: $\ce{F} < \ce{Cl} < \ce{Br}$, decided by distance and shielding (protons are a wash down a group).**

</details>

### Problem 3
Which atom is larger: $\ce{O}$ or $\ce{S}$? Which is more electronegative? Explain why the same checklist gives opposite-sounding answers.

<details>
<summary><strong>Solution</strong></summary>

$\ce{S}$ is larger: its valence electrons are in $n = 3$ with 10 core blockers, vs. oxygen's $n = 2$ with 2 — longer rope, more shielding, looser hold.

$\ce{O}$ is more electronegative: the *same* facts (shorter rope, fewer blockers) mean oxygen's nucleus pulls **shared bonding electrons** harder.

They're not opposite answers — they're the same answer read off two scoreboards: a loose grip makes you big and a weak sharer; a tight grip makes you small and a strong sharer.

**Answer: $\ce{S}$ is larger; $\ce{O}$ is more electronegative — both follow from oxygen's shorter distance and lower shielding.**

</details>

### Problem 4
Estimate $Z_{eff}$ for the valence electrons of $\ce{K}$ and $\ce{Ca}$, then explain why $\ce{Ca}$ is smaller even though both have valence electrons in $n = 4$.

<details>
<summary><strong>Solution</strong></summary>

Both have the 18-electron argon core. $Z_{eff}(\ce{K}) \approx 19 - 18 = +1$; $Z_{eff}(\ce{Ca}) \approx 20 - 18 = +2$.

Checklist: distance — both $n = 4$, tie. Shielding — both 18 core electrons, tie. Protons — calcium has one more, doubling the effective pull on the valence electrons.

**Answer: $Z_{eff} \approx +1$ for $\ce{K}$ and $+2$ for $\ce{Ca}$; with distance and shielding tied, calcium's greater effective nuclear charge pulls its valence electrons closer, making it smaller.**

</details>

### Problem 5
Explain why $\ce{Mg^2+}$ is much smaller than $\ce{Mg}$, citing at least two factors.

<details>
<summary><strong>Solution</strong></summary>

$\ce{Mg}: [\ce{Ne}]\,3s^2 \to \ce{Mg^2+}: 1s^2 2s^2 2p^6$.

Factor 1 (distance): losing both $3s$ electrons removes the entire $n = 3$ shell — the outermost electrons drop to $n = 2$, drastically shortening the rope.

Factor 2 (pull per electron): 12 protons now pull only 10 electrons instead of 12, so each remaining electron feels more attraction and less electron–electron repulsion.

**Answer: the cation loses its whole outer shell and the remaining electrons are pulled in harder by the unchanged 12-proton nucleus — $\ce{Mg^2+}$ (≈72 pm) is far smaller than $\ce{Mg}$ (≈160 pm).**

</details>

### Problem 6
Which is larger, $\ce{O}$ or $\ce{O^2-}$? Justify without using the word "octet."

<details>
<summary><strong>Solution</strong></summary>

Both have 8 protons — pull strength unchanged. $\ce{O^2-}$ has 10 electrons instead of 8, all packed into the same $n = 2$ shell: the same 8 pullers are now stretched across more flags (less attraction per electron), and the extra electrons repel each other, pushing the cloud outward.

**Answer: $\ce{O^2-}$ is larger — same nuclear charge spread over more mutually repelling electrons weakens the grip on each one.**

</details>

### Problem 7
Rank the isoelectronic series $\ce{S^2-}$, $\ce{Cl-}$, $\ce{K+}$, $\ce{Ca^2+}$ from largest to smallest radius and justify.

<details>
<summary><strong>Solution</strong></summary>

Count electrons: $16+2 = 18$, $17+1 = 18$, $19-1 = 18$, $20-2 = 18$ — all isoelectronic with $\ce{Ar}$ ($1s^2 2s^2 2p^6 3s^2 3p^6$).

Checklist: distance — identical shells, tie. Shielding — identical, tie. Protons: 16, 17, 19, 20 — the only difference. More protons pulling the same 18 electrons → smaller ion.

**Answer: $\ce{S^2-} > \ce{Cl-} > \ce{K+} > \ce{Ca^2+}$ — same electron cloud, so the nucleus with the most protons reels it in tightest.**

</details>

### Problem 8
Rank $\ce{Ar}$, $\ce{Cl}$, and $\ce{S}$ from highest to lowest first ionization energy and justify with the checklist.

<details>
<summary><strong>Solution</strong></summary>

All period 3: valence electrons in $n = 3$ (tie), shielded by 10 core electrons (tie). Protons: 16, 17, 18 → $Z_{eff} \approx +6, +7, +8$. The tighter the hold, the more energy to rip an electron away.

**Answer: $\ce{Ar} > \ce{Cl} > \ce{S}$ — same distance and shielding, so increasing nuclear charge means increasing Coulombic attraction and a higher cost to remove the outer electron.**

</details>

### Problem 9
The first ionization energy of aluminum (578 kJ/mol) is lower than that of magnesium (738 kJ/mol), breaking the across-the-period trend. Explain with electron configurations.

<details>
<summary><strong>Solution</strong></summary>

$\ce{Mg}: [\ce{Ne}]\,3s^2$; $\ce{Al}: [\ce{Ne}]\,3s^2\,3p^1$.

The electron removed from aluminum is its lone $3p$ electron. The $3p$ subshell is higher in energy than $3s$ (and slightly shielded by the $3s^2$ pair), so that electron starts closer to the exit — it needs less energy to remove, and this subshell effect outweighs aluminum's one extra proton. This is the same mechanism as the $\ce{Be} \to \ce{B}$ dip, one period down.

**Answer: aluminum's outermost electron occupies the higher-energy $3p$ subshell, so it is easier to remove than one of magnesium's $3s$ electrons despite aluminum's greater nuclear charge.**

</details>

### Problem 10
Explain why sulfur's first ionization energy (1000 kJ/mol) is lower than phosphorus's (1012 kJ/mol). Include orbital diagrams for the $3p$ electrons.

<details>
<summary><strong>Solution</strong></summary>

$\ce{P}\;(3p^3)$: $(\uparrow)(\uparrow)(\uparrow)$ — each $3p$ electron alone in its orbital.
$\ce{S}\;(3p^4)$: $(\uparrow\downarrow)(\uparrow)(\uparrow)$ — one orbital forced to hold a pair.

The two electrons sharing one orbital in sulfur repel each other, raising the paired electron's energy and partially offsetting the extra proton's pull. That destabilized electron leaves more easily. Same mechanism as $\ce{N} \to \ce{O}$.

**Answer: pairing repulsion in sulfur's doubly occupied $3p$ orbital makes its fourth $p$ electron easier to remove, so $IE_1(\ce{S}) < IE_1(\ce{P})$.**

</details>

### Problem 11
A main-group element has successive ionization energies (kJ/mol): $IE_1 = 590$, $IE_2 = 1145$, $IE_3 = 4912$, $IE_4 = 6491$. Identify its group and name one period-4 element it could be.

<details>
<summary><strong>Solution</strong></summary>

Look for the cliff: $IE_1 \to IE_2$ roughly doubles (normal), but $IE_2 \to IE_3$ jumps by more than a factor of 4 — that's the core wall. Two electrons came off at valence prices, so the element has **2 valence electrons** → Group 2. The third electron must be torn from the core: a full shell closer (Coulombic attraction soars as $r$ shrinks) and barely shielded.

**Answer: Group 2; the period-4 member is $\ce{Ca}$.**

</details>

### Problem 12
Without looking up any values, predict which is larger: $IE_2$ of $\ce{Na}$ or $IE_2$ of $\ce{Mg}$. Justify.

<details>
<summary><strong>Solution</strong></summary>

$IE_2$ removes the *second* electron. For $\ce{Mg}$ ($[\ce{Ne}]\,3s^2$), the second electron is still a valence $3s$ electron — pricey but normal. For $\ce{Na}$ ($[\ce{Ne}]\,3s^1$), the first electron already emptied the valence shell, so the second must come from the $n = 2$ **core**: one shell closer to the nucleus and shielded by only 2 electrons instead of 10 — pulling a player off the core team.

**Answer: $IE_2(\ce{Na}) \gg IE_2(\ce{Mg})$ (about 4562 vs. 1451 kJ/mol) — sodium's second electron is a core electron, held at a far shorter distance with far less shielding.**

</details>

### Problem 13
Rank $\ce{N}$, $\ce{O}$, and $\ce{P}$ from most to least electronegative, and explain each comparison with one checklist factor.

<details>
<summary><strong>Solution</strong></summary>

$\ce{O}$ vs. $\ce{N}$: same period, same shell and shielding — oxygen has one more proton, so it pulls shared electrons harder (protons). $\ce{N}$ vs. $\ce{P}$: same group — phosphorus bonds using $n = 3$ electrons shielded by 10 core electrons vs. nitrogen's $n = 2$ and 2 (distance and shielding). Note the IE exception at $\ce{N} \to \ce{O}$ does *not* carry over — electronegativity rises smoothly across because it's about pulling *shared* electrons, not removing one.

**Answer: $\ce{O} > \ce{N} > \ce{P}$ (Pauling values ≈ 3.5, 3.0, 2.2).**

</details>

### Problem 14
Rank $\ce{Na}$, $\ce{Al}$, and $\ce{Cs}$ from most to least metallic, and connect your answer to ionization energy.

<details>
<summary><strong>Solution</strong></summary>

Metallic character = willingness to lose valence electrons = *low* ionization energy. $\ce{Cs}$: valence electron in $n = 6$, 54 core blockers, $Z_{eff} \approx +1$ — the loosest grip of the three, most metallic. $\ce{Na}$ vs. $\ce{Al}$: same shell and shielding, but aluminum's $Z_{eff} \approx +3$ vs. sodium's $+1$ — aluminum grips harder, so it is less metallic.

**Answer: $\ce{Cs} > \ce{Na} > \ce{Al}$ — metallic character tracks weak Coulombic hold on valence electrons, so it increases down and decreases across, opposite to ionization energy.**

</details>

### Problem 15
*Full FRQ practice.* Write a complete 3-sentence AP justification for: "A fluorine atom has a smaller atomic radius than an oxygen atom."

<details>
<summary><strong>Solution</strong></summary>

Grade yourself against the template — (1) trend, (2) protons/$Z_{eff}$, (3) distance/shielding + Coulombic language:

**Model answer: "Fluorine has a smaller atomic radius than oxygen. Fluorine has 9 protons while oxygen has 8, and since both atoms' valence electrons occupy the same $n = 2$ shell shielded by the same 2 core electrons, fluorine's effective nuclear charge is greater. The stronger Coulombic attraction pulls fluorine's valence electrons closer to the nucleus, resulting in a smaller radius."**

If your answer named the trend, cited the proton difference with equal shielding, and tied the size to Coulombic attraction at fixed distance — full credit.

</details>

---

## Quick Reference

**The checklist (every trend, every time): protons, distance, shielding.**

| Trend | Across a period → | Down a group ↓ | One-line why |
|---|---|---|---|
| $Z_{eff} \approx Z - \text{core}$ | Increases | ~Constant | Across: protons up, shielding flat. Down: new protons canceled by new core blockers. |
| Atomic radius | Decreases | Increases | Across: stronger pull, same rope. Down: longer rope + more blockers. |
| Ionic radius | Cations ≪ parent; anions ≫ parent | Increases | Isoelectronic series: same electrons, most protons = smallest. |
| First ionization energy | Increases | Decreases | Cost of ripping the flag away tracks how tightly it's held. |
| Successive IEs | — | — | Giant jump = first core electron; cheap electrons before the jump = valence count = group. |
| Electron affinity | Generally more energy released | Generally less | Messy: $\ce{Cl}$ beats $\ce{F}$; filled/half-filled subshells resist. |
| Electronegativity | Increases | Decreases | Pull on *shared* electrons; $\ce{F}$ = 4.0 is the champion. |
| Metallic character | Decreases | Increases | Weak grip on valence electrons = metal behavior. |

**IE exceptions:** $\ce{Be} \to \ce{B}$ and $\ce{Mg} \to \ce{Al}$ (new, higher-energy $p$ subshell); $\ce{N} \to \ce{O}$ and $\ce{P} \to \ce{S}$ (pairing repulsion in a doubly occupied $p$ orbital).

**The 3-sentence FRQ template:** (1) state the trend/comparison → (2) cite protons/$Z_{eff}$ → (3) cite distance/shielding and say "Coulombic attraction." Never say "octet."

---

<div align="center">

[← Photoelectron Spectroscopy](/chemistry/0304-photoelectron-spectroscopy) | [Ions and Ionic Compounds →](/chemistry/0306-valence-electrons-ionic-compounds)

</div>
