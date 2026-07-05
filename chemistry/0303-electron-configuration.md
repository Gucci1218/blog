# Electron Configuration
<p class="article-date">July 4, 2026</p>

*Last Friday I got to a movie theater embarrassingly early — like, lights-still-on, screen-playing-trivia early — and I ended up watching strangers fill the empty room. It's weirdly predictable. Everyone grabs the best rows first, nobody argues about it. The seats come in pairs sharing an armrest, and here's the part that got me: strangers NEVER sit directly next to each other if an empty pair is available somewhere in the same section. Only when every pair in the section has one person does anyone finally double up. I was sitting there with my \$8 popcorn realizing I was watching a physics simulation: electrons fill atoms in exactly this way. Lowest-energy rows fill first, two electrons max per "seat pair," and no pairing up until they have to. That filling pattern is called an electron configuration, and it's the address book for every electron in every atom — the thing that will explain periodic trends, ion charges, and bonding for the rest of AP Chemistry.*

---

## What You'll Learn
- Define shells ($n$), subshells ($s, p, d, f$), and orbitals, and state how many electrons each can hold
- Use Coulomb's law *qualitatively* to explain why electrons closer to the nucleus have lower energy
- Write full ground-state electron configurations for any element from $\ce{H}$ to $\ce{Kr}$ using the Aufbau order
- Draw orbital diagrams with boxes and arrows, correctly applying the Pauli exclusion principle and Hund's rule
- Write noble-gas shorthand configurations like $[\ce{Ar}]\,4s^2 3d^7$
- Read an electron configuration straight off the periodic table using the $s$, $p$, and $d$ blocks
- Distinguish valence electrons from core electrons and count each
- Write configurations for ions — including the transition-metal trap where $4s$ electrons leave *before* $3d$
- Spot an excited-state configuration in a lineup (a favorite AP multiple-choice move)

---

## Prerequisites
- [Atomic Structure Basics](/chemistry/0201-atomic-structure-basics) — you need to know that electrons live outside the nucleus, that the proton count sets the electron count in a neutral atom, and what ions are
- [Periodic Table Map](/chemistry/0202-periodic-table-map) — the table's row/column layout is literally a seating chart for electrons; we'll read configurations directly off the map

---

## The Core Concept

### Intuition First

Back to the theater. Let me make the analogy load-bearing, because every piece of it maps onto a real rule:

| In the theater | In the atom |
|---|---|
| A **row** of seats | A **shell** — energy level $n = 1, 2, 3, \dots$ |
| A **section** within a row (left, center, right...) | A **subshell** — $s$, $p$, $d$, or $f$ |
| One **seat pair** sharing an armrest | One **orbital** |
| Max **2 people** per seat pair, facing opposite armrests | Max **2 electrons** per orbital, with **opposite spins** (Pauli exclusion) |
| Best (front-value) rows fill **first** | Lowest-**energy** orbitals fill first (Aufbau principle) |
| Strangers spread out — **one per seat pair** — until the section forces doubling | Electrons occupy orbitals in a subshell **singly** before any pairing (Hund's rule) |
| The theater's predictable filling pattern | The **electron configuration** |

Three named rules, three theater habits:

1. **Aufbau principle** — "best rows first." Electrons fill the lowest-energy orbitals available before touching higher ones. (*Aufbau* is German for "building up.")
2. **Pauli exclusion principle** — "two per seat pair, opposite armrests." An orbital holds at most 2 electrons, and they must have opposite spins ($\uparrow$ and $\downarrow$). No two electrons in an atom are identical in every way.
3. **Hund's rule** — "strangers don't sit together until they must." Within one subshell, every orbital gets one electron (all spinning the same way, $\uparrow$) before any orbital gets its second.

Everything else in this article is just learning the theater's floor plan — how many rows, how many sections per row, how many seat pairs per section — and then filling seats by the rules.

### The Floor Plan: Shells, Subshells, Orbitals

**Shells** are labeled by the principal quantum number $n = 1, 2, 3, 4, \dots$ Bigger $n$ means, on average, farther from the nucleus and higher energy — rows farther from the screen.

**Subshells** are the sections within a row. Shell $n$ contains $n$ types of subshell, drawn from the list $s, p, d, f$:

- $n = 1$: just $1s$
- $n = 2$: $2s$ and $2p$
- $n = 3$: $3s$, $3p$, $3d$
- $n = 4$: $4s$, $4p$, $4d$, $4f$

**Orbitals** are the seat pairs. Each subshell type has a fixed number of orbitals, and each orbital holds up to 2 electrons:

| Subshell | Orbitals (seat pairs) | Max electrons |
|:---:|:---:|:---:|
| $s$ | 1 | 2 |
| $p$ | 3 | 6 |
| $d$ | 5 | 10 |
| $f$ | 7 | 14 |

So a whole shell holds $2n^2$ electrons: shell 1 holds 2, shell 2 holds 8, shell 3 holds 18, shell 4 holds 32.

**Notation:** the expression $2p^4$ reads "shell 2, subshell $p$, containing 4 electrons." The superscript is a *count*, not an exponent — $2p^4$ means four electrons live in the $2p$ section, spread across its three seat pairs.

### Why Lower Rows Are Cheaper: Coulomb's Law (Qualitatively)

One physics idea powers this entire topic, and it comes back with a vengeance in Periodic Trends, so let's plant it now.

**Coulomb's law** says the attraction between two opposite charges is:

- **stronger when the charges are bigger** (more protons in the nucleus → stronger pull on each electron), and
- **stronger when the charges are closer** — dramatically so, since the force scales with $\dfrac{1}{r^2}$. Halve the distance and the attraction *quadruples*.

$$F \propto \frac{q_1 \, q_2}{r^2}$$

An electron near the nucleus is held tightly by a strong attraction — it sits in a deep energy well, meaning it has **low energy** and would take a lot of energy to remove. An electron far from the nucleus feels a weak pull — **high energy**, easy to remove.

That's the whole reason the theater has "best rows." The $1s$ orbital hugs the nucleus, so it's the lowest-energy seat in the house and fills first. Each successive shell sits farther out, feels a weaker Coulombic grip, and costs more energy to occupy. When AP asks *"why does sodium lose its $3s$ electron so easily?"* the answer is always some flavor of Coulomb: that electron is far from the nucleus and shielded by inner electrons, so the attraction holding it is weak.

### The Filling Order: Aufbau's Seating Chart

Here's the twist that makes this topic interesting: **rows overlap in price.** Once shells get big, a low subshell of a far row can be cheaper than a high subshell of a near row. Specifically, $4s$ is slightly lower in energy than $3d$, so $4s$ fills first. The actual filling order is:

$$1s \to 2s \to 2p \to 3s \to 3p \to \mathbf{4s} \to \mathbf{3d} \to 4p \to 5s \to 4d \to 5p \to 6s \to \dots$$

You don't memorize that list raw — you generate it with the **diagonal rule**. Write the subshells in a grid, each shell on its own line:

| | | | |
|---|---|---|---|
| $1s$ | | | |
| $2s$ | $2p$ | | |
| $3s$ | $3p$ | $3d$ | |
| $4s$ | $4p$ | $4d$ | $4f$ |
| $5s$ | $5p$ | $5d$ | $5f$ |
| $6s$ | $6p$ | $6d$ | |
| $7s$ | $7p$ | | |

Now read diagonal arrows running from **upper-right to lower-left**: the first diagonal hits $1s$; the next $2s$; then $2p, 3s$; then $3p, 4s$; then $3d, 4p, 5s$; then $4d, 5p, 6s$; and so on. Follow the diagonals and the order above falls out automatically.

**Writing a configuration** is then a three-step routine:

1. Count the electrons (atomic number $Z$ for a neutral atom).
2. Fill subshells in Aufbau order, each to its capacity ($s$: 2, $p$: 6, $d$: 10, $f$: 14).
3. Stop when the electrons run out; the last subshell may be partially full.

For example, phosphorus ($Z = 15$): $1s^2\, 2s^2\, 2p^6\, 3s^2\, 3p^3$. Check: $2+2+6+2+3 = 15$. ✓ Always check the sum — it's a free error detector.

### Orbital Diagrams: Seat Pairs, Drawn Out

A configuration like $2p^4$ tells you the section head-count but not *which seats*. An **orbital diagram** draws every orbital as a box and every electron as an arrow. The rules:

- **Pauli:** at most two arrows per box, and they must point opposite ways: $[\uparrow\downarrow]$. Never $[\uparrow\uparrow]$.
- **Hund:** within a subshell, place one $\uparrow$ in each box before any box gets its $\downarrow$.

Watch nitrogen ($Z = 7$, config $1s^2\, 2s^2\, 2p^3$) versus oxygen ($Z = 8$, config $1s^2\, 2s^2\, 2p^4$):

```text
Nitrogen:   1s [↑↓]   2s [↑↓]   2p [↑ ] [↑ ] [↑ ]      ← 3 unpaired
Oxygen:     1s [↑↓]   2s [↑↓]   2p [↑↓] [↑ ] [↑ ]      ← 2 unpaired
```

Nitrogen's three $2p$ electrons each take their own seat pair — strangers spreading out. Oxygen's fourth $2p$ electron has no empty pair left in the section, so it *must* double up, and it pairs with opposite spin. Counting **unpaired electrons** off a diagram like this is a standard AP skill (it's what makes a species paramagnetic — attracted to a magnet).

Why does Hund's rule exist? Electrons all carry negative charge and repel each other (Coulomb again!). Two electrons crammed into the same orbital repel more than two in separate orbitals — exactly why strangers leave a buffer seat when they can.

### Noble-Gas Shorthand

Writing $1s^2\, 2s^2\, 2p^6\, 3s^2\, 3p^6\, 4s^2\, 3d^7$ for cobalt gets old fast. The fix: everything up through the previous **noble gas** is a filled, chemically boring core — so abbreviate it with the noble gas in brackets.

Cobalt ($Z = 27$): the previous noble gas is argon ($Z = 18$), which covers $1s^2$ through $3p^6$. So:

$$\ce{Co}: \quad [\ce{Ar}]\, 4s^2\, 3d^7$$

Think of it as the theater's "already-full rows" sign: instead of describing 18 seated people, you just say "the first three rows are sold out — here's who came in after." Rules of thumb:

- Always jump back to the noble gas *before* the element ($\ce{Kr}$ is written $[\ce{Ar}]\,4s^2 3d^{10} 4p^6$, never $[\ce{Kr}]$).
- The shorthand shows the outer electrons explicitly — which is exactly the part chemistry cares about.

### Reading Configurations Straight Off the Periodic Table

Here's the payoff from [Periodic Table Map](/chemistry/0202-periodic-table-map): the periodic table **is** the diagonal chart, unrolled. The table splits into neighborhoods (blocks) by which subshell is filling:

| Block | Where on the table | Subshell filling | Width |
|---|---|---|:---:|
| $s$-block | Groups 1–2 (plus $\ce{He}$) | $ns$ | 2 columns |
| $p$-block | Groups 13–18 | $np$ | 6 columns |
| $d$-block | Groups 3–12 (the transition metals) | $(n-1)d$ | 10 columns |
| $f$-block | The two detached rows at the bottom | $(n-2)f$ | 14 columns |

The widths are no accident: 2, 6, 10, 14 are exactly the subshell capacities. To read a configuration, walk the table left to right, top to bottom, like reading a book, calling out each block as you cross it. Two adjustments:

- In the $d$-block, the $d$ subshell number is **one less than the row number** (row 4 fills $3d$).
- In the $f$-block, it's **two less** (row 6 fills $4f$).

Example: bromine is in row 4, $p$-block, 5th column of the block. Walk the table: rows 1–3 give $[\ce{Ar}]$, then row 4 crosses the $s$-block ($4s^2$), the $d$-block ($3d^{10}$), and 5 squares into the $p$-block ($4p^5$):

$$\ce{Br}: \quad [\ce{Ar}]\, 4s^2\, 3d^{10}\, 4p^5$$

No diagonal chart needed — the map does the work. This is the fastest and least error-prone method on the exam.

### Valence vs. Core Electrons

- **Valence electrons** = electrons in the **outermost shell** (highest $n$). For main-group elements, that's the $ns$ and $np$ electrons. These sit in the back rows, feel the weakest Coulombic pull, and do *all* the bonding and reacting.
- **Core electrons** = everything else — the sold-out inner rows, chemically inert.

Sulfur, $[\ce{Ne}]\, 3s^2\, 3p^4$: valence $= 2 + 4 = 6$, core $= 10$. Shortcut for main-group elements: **the valence count equals the group number's ones digit** (Group 16 → 6 valence electrons). This is why elements in the same column behave alike — same valence configuration, same chemistry.

### Configurations of Ions

**Main-group ions** are simple: atoms gain or lose electrons to reach the nearest **noble-gas configuration** (a completely sold-out outer row).

- $\ce{Ca^2+}$: calcium ($[\ce{Ar}]\,4s^2$) loses both $4s$ electrons → $[\ce{Ar}]$. Same configuration as argon.
- $\ce{S^2-}$: sulfur ($[\ce{Ne}]\,3s^2 3p^4$) gains 2 electrons → $[\ce{Ne}]\,3s^2 3p^6 = [\ce{Ar}]$. Also argon's configuration!

Species with identical electron configurations are called **isoelectronic**. $\ce{S^2-}$, $\ce{Cl^-}$, $\ce{Ar}$, $\ce{K+}$, and $\ce{Ca^2+}$ are all isoelectronic (18 electrons each) — same seating chart, different number of protons collecting tickets.

**Transition-metal ions** hide the classic trap. When a transition metal *loses* electrons, the **$4s$ electrons leave FIRST**, before any $3d$ electrons — even though $4s$ filled first.

$$\ce{Fe}: [\ce{Ar}]\,4s^2 3d^6 \quad\Rightarrow\quad \ce{Fe^2+}: [\ce{Ar}]\,3d^6 \quad\Rightarrow\quad \ce{Fe^3+}: [\ce{Ar}]\,3d^5$$

Why? Once $3d$ has electrons in it, the energy order shifts: $4s$ becomes the *outermost, highest-energy, least-held* shell — the very back row, farthest from the screen. When the theater asks people to leave, the back row goes first. **Rule: fill $4s$ before $3d$, but empty $4s$ before $3d$.**

### The Two Famous Exceptions: Cr and Cu

Chromium and copper break the plain Aufbau prediction:

| Element | Aufbau predicts | Actual |
|---|---|---|
| $\ce{Cr}$ ($Z=24$) | $[\ce{Ar}]\,4s^2 3d^4$ | $[\ce{Ar}]\,4s^1 3d^5$ |
| $\ce{Cu}$ ($Z=29$) | $[\ce{Ar}]\,4s^2 3d^{10}$... wait, predicts $4s^2 3d^9$ | $[\ce{Ar}]\,4s^1 3d^{10}$ |

An electron promotes itself from $4s$ into $3d$ because a **half-filled ($d^5$) or completely filled ($d^{10}$) $d$ subshell** is extra stable — the electron distribution is perfectly symmetric and electron–electron repulsion drops. Theater version: one person moves back a row so that a whole section ends up perfectly evenly spread — the room is "happier" that way.

**AP reality check:** the AP exam rarely tests these exceptions directly, and you won't lose points for the Aufbau version on most questions. Know that they exist, know the half-filled-stability reasoning, and move on.

### Ground State vs. Excited State

Everything above describes the **ground state** — the lowest-energy seating, every electron as close to the screen as the rules allow. But if an atom absorbs energy (light, heat, an electric discharge), an electron can jump to a higher-energy orbital. That's an **excited state**: same total electron count, illegal-looking seating.

$$\text{Ground-state }\ce{Na}: \; 1s^2\, 2s^2\, 2p^6\, 3s^1 \qquad \text{Excited }\ce{Na}: \; 1s^2\, 2s^2\, 2p^6\, 4s^1$$

Spot-the-excited-atom is an AP multiple-choice favorite. The tell: **a lower-energy subshell is left partially empty while a higher one has electrons** — someone skipped a cheap seat. Compare:

- $1s^2\, 2s^2\, 2p^5\, 3s^1$ → excited (that $3s$ electron should be finishing $2p$)
- $1s^2\, 2s^2\, 2p^6\, 3s^2$ → ground state (Aufbau obeyed)
- $1s^2\, 2s^3\, \dots$ → **impossible**, not excited — $2s$ can never hold 3 electrons (Pauli violation, three people on one seat pair)

Three categories, always: ground (legal and lowest), excited (legal but skipped a seat), impossible (breaks capacity rules).

---

## Worked Examples

### Example 1: The First Ten Seats

**Problem:** Write the full ground-state electron configurations for $\ce{H}$, $\ce{He}$, $\ce{Li}$, $\ce{C}$, and $\ce{Ne}$.

**Solution:**

**Step 1:** Count electrons: $Z = 1, 2, 3, 6, 10$.

**Step 2:** Fill in Aufbau order ($1s \to 2s \to 2p$), respecting capacities 2, 2, 6:

- $\ce{H}$ (1): $1s^1$
- $\ce{He}$ (2): $1s^2$ — shell 1 is now sold out
- $\ce{Li}$ (3): $1s^2\, 2s^1$ — first electron forced into row 2
- $\ce{C}$ (6): $1s^2\, 2s^2\, 2p^2$
- $\ce{Ne}$ (10): $1s^2\, 2s^2\, 2p^6$ — shell 2 sold out; that's why neon is inert

**Answer: $\ce{H}: 1s^1$; $\ce{He}: 1s^2$; $\ce{Li}: 1s^2 2s^1$; $\ce{C}: 1s^2 2s^2 2p^2$; $\ce{Ne}: 1s^2 2s^2 2p^6$**

### Example 2: Full Configuration of Sulfur

**Problem:** Write the complete ground-state electron configuration of sulfur and verify the electron count.

**Solution:**

**Step 1:** Sulfur is $Z = 16$, so place 16 electrons.

**Step 2:** Fill in order: $1s^2$ (2), $2s^2$ (4), $2p^6$ (10), $3s^2$ (12), $3p^4$ (16). Stop — electrons exhausted mid-$3p$.

**Step 3:** Check: $2+2+6+2+4 = 16$. ✓

**Answer: $\ce{S}: 1s^2\, 2s^2\, 2p^6\, 3s^2\, 3p^4$**

### Example 3: Crossing into the d-Block (Iron)

**Problem:** Write the full configuration of iron ($Z = 26$).

**Solution:**

**Step 1:** Fill through argon's 18: $1s^2\, 2s^2\, 2p^6\, 3s^2\, 3p^6$.

**Step 2:** Aufbau says $4s$ comes *before* $3d$ (the cheaper seat, even though it's a farther row): $4s^2$ brings us to 20.

**Step 3:** Remaining $26 - 20 = 6$ electrons enter $3d$: $3d^6$.

**Answer: $\ce{Fe}: 1s^2\, 2s^2\, 2p^6\, 3s^2\, 3p^6\, 4s^2\, 3d^6$**

### Example 4: Hund's Rule in Action (Nitrogen's Orbital Diagram)

**Problem:** Draw the orbital diagram for nitrogen and state the number of unpaired electrons.

**Solution:**

**Step 1:** Configuration: $\ce{N}$ ($Z=7$): $1s^2\, 2s^2\, 2p^3$.

**Step 2:** Fill boxes. $1s$ and $2s$ each take a full pair. The three $2p$ electrons spread out — one per orbital, parallel spins (strangers refusing to share armrests):

```text
1s [↑↓]   2s [↑↓]   2p [↑ ] [↑ ] [↑ ]
```

**Step 3:** Count boxes with a single arrow: all three $2p$ orbitals.

**Answer: 3 unpaired electrons.**

### Example 5: When Pairing Finally Starts (Oxygen)

**Problem:** Draw the orbital diagram for oxygen. How many unpaired electrons does it have?

**Solution:**

**Step 1:** $\ce{O}$ ($Z=8$): $1s^2\, 2s^2\, 2p^4$.

**Step 2:** The first three $2p$ electrons go one-per-orbital (Hund). The fourth finds every seat pair singly occupied — the section is out of empty pairs — so it must double up, spin-down (Pauli):

```text
1s [↑↓]   2s [↑↓]   2p [↑↓] [↑ ] [↑ ]
```

**Answer: 2 unpaired electrons.**

### Example 6: Noble-Gas Shorthand for Cobalt

**Problem:** Write the noble-gas shorthand configuration for cobalt ($Z = 27$).

**Solution:**

**Step 1:** The noble gas *before* cobalt is argon ($Z = 18$). Bracket it: $[\ce{Ar}]$ covers the first 18 electrons.

**Step 2:** Place the remaining $27 - 18 = 9$: $4s^2$ first, then $3d^7$.

**Answer: $\ce{Co}: [\ce{Ar}]\, 4s^2\, 3d^7$**

### Example 7: Reading Bromine Off the Table

**Problem:** Without the diagonal chart, use the periodic table's block structure to write the configuration of $\ce{Br}$ ($Z = 35$).

**Solution:**

**Step 1:** Bromine sits in row 4, $p$-block, group 17 — the 5th column of the $p$-block.

**Step 2:** Everything before row 4 is the argon core: $[\ce{Ar}]$.

**Step 3:** Walk row 4 left to right: $s$-block gives $4s^2$; $d$-block gives $3d^{10}$ (remember: $d$ subshell = row $-$ 1); then 5 squares into the $p$-block gives $4p^5$.

**Answer: $\ce{Br}: [\ce{Ar}]\, 4s^2\, 3d^{10}\, 4p^5$**

### Example 8: Valence vs. Core Count

**Problem:** How many valence electrons and how many core electrons does arsenic ($Z = 33$) have?

**Solution:**

**Step 1:** Configuration: $\ce{As}: [\ce{Ar}]\, 4s^2\, 3d^{10}\, 4p^3$.

**Step 2:** Valence electrons live in the outermost shell, $n = 4$: that's $4s^2$ and $4p^3$, so $2 + 3 = 5$. (The $3d^{10}$ electrons are $n = 3$ — inner row, core.) Sanity check: arsenic is Group 15 → ones digit 5. ✓

**Step 3:** Core $= 33 - 5 = 28$.

**Answer: 5 valence electrons, 28 core electrons.**

### Example 9: Main-Group Ions and Isoelectronic Species

**Problem:** Write configurations for $\ce{Ca^2+}$ and $\ce{S^2-}$, and name a noble gas isoelectronic with both.

**Solution:**

**Step 1:** $\ce{Ca}$: $[\ce{Ar}]\,4s^2$. The $2+$ ion loses both outermost ($4s$) electrons: $\ce{Ca^2+} = [\ce{Ar}]$ — 18 electrons.

**Step 2:** $\ce{S}$: $[\ce{Ne}]\,3s^2 3p^4$. The $2-$ ion gains 2 electrons, completing $3p$: $\ce{S^2-} = [\ce{Ne}]\,3s^2 3p^6$ — also 18 electrons, the argon configuration.

**Step 3:** Both match argon's seating chart exactly.

**Answer: $\ce{Ca^2+}: [\ce{Ar}]$; $\ce{S^2-}: 1s^2 2s^2 2p^6 3s^2 3p^6$; both are isoelectronic with $\ce{Ar}$.**

### Example 10: The Transition-Metal Trap (Fe²⁺ and Fe³⁺)

**Problem:** Write noble-gas configurations for $\ce{Fe^2+}$ and $\ce{Fe^3+}$.

**Solution:**

**Step 1:** Neutral iron: $[\ce{Ar}]\, 4s^2\, 3d^6$.

**Step 2:** Electrons leave the outermost shell first — that's $4s$ ($n = 4$ is farther out than $n = 3$). Remove both $4s$ electrons: $\ce{Fe^2+} = [\ce{Ar}]\, 3d^6$. **Not** $[\ce{Ar}]\,4s^2 3d^4$ — that's the classic wrong answer.

**Step 3:** For $\ce{Fe^3+}$, remove one more, now from $3d$: $[\ce{Ar}]\, 3d^5$. (A half-filled $d^5$ — pleasingly stable, which is partly why $\ce{Fe^3+}$ is so common.)

**Answer: $\ce{Fe^2+}: [\ce{Ar}]\,3d^6$; $\ce{Fe^3+}: [\ce{Ar}]\,3d^5$.**

### Example 11: Spot the Excited Atom

**Problem:** Each configuration below has 12 electrons. Classify each as ground state, excited state, or impossible.

(a) $1s^2\, 2s^2\, 2p^6\, 3s^2$  (b) $1s^2\, 2s^2\, 2p^6\, 3s^1\, 3p^1$  (c) $1s^2\, 2s^2\, 2p^8$

**Solution:**

**Step 1:** (a) follows Aufbau perfectly — this is magnesium's **ground state**.

**Step 2:** (b) has a legal seat map (no capacity violated) but $3p$ holds an electron while $3s$ is half empty — a skipped cheap seat. **Excited state** of magnesium.

**Step 3:** (c) claims 8 electrons in $2p$, which caps at 6. Three people on a seat pair — **impossible** (violates Pauli), not merely excited.

**Answer: (a) ground state; (b) excited state; (c) impossible.**

### Example 12: Identify the Element from Its Configuration

**Problem:** An element's ground-state configuration ends in $[\ce{Ar}]\, 4s^2\, 3d^{10}\, 4p^2$. Identify the element and predict its most common ion's charge.

**Solution:**

**Step 1:** Count: $18 + 2 + 10 + 2 = 32$ electrons → $Z = 32$, which is germanium. (Faster: row 4, $p$-block, 2nd column → Group 14.)

**Step 2:** Valence electrons: $4s^2 4p^2 = 4$. Group 14 elements like $\ce{Ge}$ typically share rather than fully transfer, but when germanium forms an ion it commonly loses the two $4p$ electrons (or all four valence) — AP-level answer: Group 14, 4 valence electrons.

**Answer: Germanium ($\ce{Ge}$), Group 14, with 4 valence electrons.**

---

## Common Mistakes

| The Mistake | Why It Happens | How to Avoid It |
|---|---|---|
| Filling $3d$ before $4s$ (writing $\ce{K}$ as $[\ce{Ar}]\,3d^1$) | "3 comes before 4" feels natural | Trust the diagonal rule or the table: potassium sits in the $s$-block of row 4, so it's $4s^1$ |
| Removing $3d$ electrons first when forming transition-metal ions | You just learned $4s$ fills first, so it "should" empty last | **Fill $4s$ first, empty $4s$ first.** Once $3d$ is occupied, $4s$ is the outermost (highest-energy) shell — back row leaves first |
| Pairing electrons too early: drawing $2p^3$ as $[\uparrow\downarrow][\uparrow\ ][\ \ ]$ | Filling boxes left to right feels tidy | Hund's rule: strangers spread out. One arrow per box across the whole subshell before any second arrows |
| Two arrows the same direction in one box: $[\uparrow\uparrow]$ | Forgetting spins must oppose | Pauli: a shared seat pair means opposite armrests — always $[\uparrow\downarrow]$ |
| Counting $3d^{10}$ electrons as valence for main-group elements like $\ce{Br}$ | The $3d$ electrons appear late in the configuration | Valence = **highest $n$ only**. For $\ce{Br}$, only $4s^2 4p^5 = 7$ count |
| Writing the superscript sum wrong (e.g., 17 electrons for $Z = 16$) | Arithmetic slip while filling | Always add the superscripts at the end and match against $Z$ (adjusting for ion charge) |
| Calling a Pauli-violating configuration ($2s^3$) "excited" | Both look "wrong" | Excited = legal seats, wrong order. Impossible = over capacity. Check capacity first |
| Shorthand with the wrong noble gas ($\ce{Cl}$ as $[\ce{Ar}]\,{-}1$ or $[\ce{He}]\,\dots$) | Grabbing the nearest noble gas instead of the previous one | Always bracket the noble gas that comes *before* the element in the table |

---

## AP Exam Tips

- **Configurations are almost never the whole question — they're the justification.** AP loves "explain why $\ce{Mg}$ forms a $2{+}$ ion" or "explain why $\ce{Cl}$ has a more negative electron affinity than $\ce{S}$." Your answer should cite the configuration *and* Coulomb's law: what the electron arrangement is, and how nuclear charge / distance / shielding makes it favorable. A configuration alone, with no Coulombic reasoning, usually earns partial credit at best.
- **Excited-state identification is a multiple-choice staple.** Scan for a skipped subshell ($3s^1 3p^1$ with $3s$ unfilled, or $2p^5 3s^1$). Also scan for over-capacity subshells — those choices are *impossible*, not excited, and AP loves including one as a distractor.
- **"Which species is isoelectronic with…"** — just count electrons: $Z$ minus the charge. $\ce{N^3-}$, $\ce{O^2-}$, $\ce{F^-}$, $\ce{Ne}$, $\ce{Na+}$, $\ce{Mg^2+}$, $\ce{Al^3+}$ all have 10. Follow-up questions ("which is smallest?") are answered with proton count: more protons pulling on the same 10 electrons → smaller — pure Coulomb.
- **Transition-metal ions:** if an FRQ asks for $\ce{Zn^2+}$, $\ce{Fe^2+}$, or $\ce{Mn^2+}$, remove $4s$ electrons first. Writing $[\ce{Ar}]\,4s^2 3d^4$ for $\ce{Fe^2+}$ is the single most common configuration error on the exam.
- **Cr and Cu exceptions:** know they exist and why (half-filled/full $d$ stability), but don't panic — AP rarely tests them, and question writers usually avoid those two elements in configuration items.
- **Use the periodic table you're given.** Every AP exam includes a periodic table; the block-reading method turns configuration questions into 15-second table walks. Practice reading configurations *off the table*, not off a memorized chart.
- This topic feeds directly into **photoelectron spectroscopy (next article!)** — PES questions are configuration questions wearing a lab coat. Nail shells/subshells/capacities now and PES becomes free points.

---

## Practice Problems

### Problem 1
Write the full ground-state electron configuration for sodium ($Z = 11$).

<details>
<summary><strong>Solution</strong></summary>

Fill in Aufbau order: $1s^2$ (2), $2s^2$ (4), $2p^6$ (10), and the last electron enters $3s$.

Check: $2 + 2 + 6 + 1 = 11$. ✓

**Answer: $\ce{Na}: 1s^2\, 2s^2\, 2p^6\, 3s^1$**

</details>

### Problem 2
Write the full ground-state electron configuration for chlorine ($Z = 17$).

<details>
<summary><strong>Solution</strong></summary>

$1s^2$ (2), $2s^2$ (4), $2p^6$ (10), $3s^2$ (12), then 5 electrons into $3p$.

Check: $2+2+6+2+5 = 17$. ✓

**Answer: $\ce{Cl}: 1s^2\, 2s^2\, 2p^6\, 3s^2\, 3p^5$**

</details>

### Problem 3
Write the full configuration for potassium ($Z = 19$), and explain in one sentence why its last electron enters $4s$ rather than $3d$.

<details>
<summary><strong>Solution</strong></summary>

Through argon: $1s^2\, 2s^2\, 2p^6\, 3s^2\, 3p^6$ (18 electrons). The 19th electron enters $4s$ because $4s$ is *lower in energy* than $3d$ at this point in the filling — the cheaper seat, even though it belongs to a farther row (the diagonal rule captures this).

**Answer: $\ce{K}: 1s^2\, 2s^2\, 2p^6\, 3s^2\, 3p^6\, 4s^1$ — because $4s$ lies below $3d$ in energy, Aufbau fills it first.**

</details>

### Problem 4
Draw the orbital diagram for carbon ($Z = 6$) and state how many unpaired electrons it has.

<details>
<summary><strong>Solution</strong></summary>

Configuration: $1s^2\, 2s^2\, 2p^2$. By Hund's rule, the two $2p$ electrons take separate orbitals with parallel spins:

```text
1s [↑↓]   2s [↑↓]   2p [↑ ] [↑ ] [  ]
```

**Answer: 2 unpaired electrons.**

</details>

### Problem 5
Write the full configuration of zinc ($Z = 30$). Which subshell(s) fill after $3p$ and in what order?

<details>
<summary><strong>Solution</strong></summary>

After $3p^6$ (18 electrons), Aufbau order continues $4s$ then $3d$: $4s^2$ (20), then $3d^{10}$ (30).

**Answer: $\ce{Zn}: 1s^2\, 2s^2\, 2p^6\, 3s^2\, 3p^6\, 4s^2\, 3d^{10}$; after $3p$, the order is $4s$ first, then $3d$.**

</details>

### Problem 6
Write the noble-gas shorthand configuration for nickel ($Z = 28$).

<details>
<summary><strong>Solution</strong></summary>

Previous noble gas: argon (18 electrons) → $[\ce{Ar}]$. Remaining $28 - 18 = 10$ electrons: $4s^2$ then $3d^8$.

**Answer: $\ce{Ni}: [\ce{Ar}]\, 4s^2\, 3d^8$**

</details>

### Problem 7
A neutral atom has the ground-state configuration $1s^2\, 2s^2\, 2p^6\, 3s^2\, 3p^4$. Identify the element, its group, and its number of valence electrons.

<details>
<summary><strong>Solution</strong></summary>

Electron count: $2+2+6+2+4 = 16$ → $Z = 16$, sulfur. Outermost shell is $n = 3$: $3s^2 3p^4$ gives $6$ valence electrons → Group 16.

**Answer: Sulfur ($\ce{S}$), Group 16, 6 valence electrons.**

</details>

### Problem 8
How many orbitals — and how many electrons maximum — can shell $n = 3$ hold? List the subshells.

<details>
<summary><strong>Solution</strong></summary>

Shell 3 contains subshells $3s$ (1 orbital), $3p$ (3 orbitals), $3d$ (5 orbitals): $1 + 3 + 5 = 9$ orbitals. Each holds 2 electrons: $9 \times 2 = 18$, matching $2n^2 = 2(3)^2 = 18$.

**Answer: Subshells $3s, 3p, 3d$; 9 orbitals; maximum 18 electrons.**

</details>

### Problem 9
Write the configurations of $\ce{Mg^2+}$ and $\ce{N^3-}$. Are they isoelectronic? With which noble gas?

<details>
<summary><strong>Solution</strong></summary>

$\ce{Mg}$ ($Z=12$): $1s^2 2s^2 2p^6 3s^2$. Losing 2 electrons removes $3s^2$: $\ce{Mg^2+} = 1s^2\, 2s^2\, 2p^6$ (10 electrons).

$\ce{N}$ ($Z=7$): $1s^2 2s^2 2p^3$. Gaining 3 electrons completes $2p$: $\ce{N^3-} = 1s^2\, 2s^2\, 2p^6$ (10 electrons).

Identical configurations → isoelectronic, both matching neon.

**Answer: Both are $1s^2\, 2s^2\, 2p^6$ — isoelectronic with each other and with $\ce{Ne}$.**

</details>

### Problem 10
Write the noble-gas configuration for $\ce{Mn^2+}$ ($Z = 25$ for $\ce{Mn}$). How many unpaired electrons does the ion have?

<details>
<summary><strong>Solution</strong></summary>

Neutral $\ce{Mn}$: $[\ce{Ar}]\, 4s^2\, 3d^5$. Forming the $2+$ ion removes the two $4s$ electrons first (outermost shell leaves first): $\ce{Mn^2+} = [\ce{Ar}]\, 3d^5$.

By Hund's rule, five $d$ electrons spread one per orbital:

```text
3d [↑ ] [↑ ] [↑ ] [↑ ] [↑ ]
```

**Answer: $\ce{Mn^2+}: [\ce{Ar}]\, 3d^5$, with 5 unpaired electrons.**

</details>

### Problem 11
Classify each 11-electron configuration as ground state, excited state, or impossible:

(a) $1s^2\, 2s^2\, 2p^6\, 3s^1$  (b) $1s^2\, 2s^2\, 2p^5\, 3s^2$  (c) $1s^2\, 2s^2\, 2p^7$

<details>
<summary><strong>Solution</strong></summary>

(a) Perfect Aufbau filling — **ground state** (sodium).

(b) All capacities legal, but $3s$ holds 2 while $2p$ sits one short of full — a skipped lower seat. **Excited state.**

(c) $2p$ caps at 6 electrons; 7 violates the Pauli exclusion principle. **Impossible.**

**Answer: (a) ground; (b) excited; (c) impossible.**

</details>

### Problem 12
Using only the periodic table's block structure, write the noble-gas configuration of tin ($\ce{Sn}$, $Z = 50$).

<details>
<summary><strong>Solution</strong></summary>

Tin: row 5, $p$-block, Group 14 → 2nd column of the $p$-block. Core: everything through krypton, $[\ce{Kr}]$ (36 electrons). Walk row 5: $s$-block → $5s^2$; $d$-block → $4d^{10}$ ($d$ = row $-$ 1); two squares into the $p$-block → $5p^2$. Check: $36+2+10+2 = 50$. ✓

**Answer: $\ce{Sn}: [\ce{Kr}]\, 5s^2\, 4d^{10}\, 5p^2$**

</details>

### Problem 13
Which of the following species is NOT isoelectronic with the others? $\ce{K+}$, $\ce{Cl^-}$, $\ce{Ca^2+}$, $\ce{Na+}$, $\ce{Ar}$

<details>
<summary><strong>Solution</strong></summary>

Count electrons ($Z$ minus charge): $\ce{K+}$: $19-1 = 18$; $\ce{Cl^-}$: $17+1 = 18$; $\ce{Ca^2+}$: $20-2 = 18$; $\ce{Ar}$: 18; $\ce{Na+}$: $11-1 = 10$.

**Answer: $\ce{Na+}$ (10 electrons; the rest have 18).**

</details>

### Problem 14
Chromium's actual configuration is $[\ce{Ar}]\,4s^1\,3d^5$, not the Aufbau-predicted $[\ce{Ar}]\,4s^2\,3d^4$. Explain why in one or two sentences.

<details>
<summary><strong>Solution</strong></summary>

A half-filled $d$ subshell ($3d^5$, one electron in each of the five orbitals) is unusually stable: the symmetric arrangement minimizes electron–electron repulsion. Promoting one $4s$ electron into $3d$ achieves this half-filled state at a lower total energy than the predicted $4s^2 3d^4$ arrangement. (Copper does the analogous move to reach a full $3d^{10}$.)

**Answer: The half-filled $3d^5$ arrangement is extra stable (symmetric, lower repulsion), so one $4s$ electron shifts into $3d$.**

</details>

### Problem 15
An FRQ shows that magnesium forms $\ce{Mg^2+}$ but never $\ce{Mg^3+}$ in ordinary chemistry. Use electron configuration and Coulomb's law to explain why.

<details>
<summary><strong>Solution</strong></summary>

$\ce{Mg}$: $1s^2\, 2s^2\, 2p^6\, 3s^2$. The two $3s$ valence electrons are in the outermost shell, far from the nucleus and shielded by 10 core electrons — the Coulombic attraction holding them is weak, so both are removed relatively easily, giving $\ce{Mg^2+}$ with the stable neon core $1s^2 2s^2 2p^6$.

A third electron would have to come from $2p$ — a **core** electron, one full shell closer to the nucleus with far less shielding. By Coulomb's law (attraction grows sharply as $r$ shrinks), that electron is held enormously more tightly, so the energy cost of forming $\ce{Mg^3+}$ is prohibitive.

**Answer: Removing two $3s$ electrons yields a noble-gas core; a third removal would take a tightly held $2p$ core electron (much closer to the nucleus, much stronger Coulombic attraction), which is energetically prohibitive.**

</details>

---

## Quick Reference

| Concept | The Rule | Theater Version |
|---|---|---|
| Shell ($n$) | Energy level; holds $2n^2$ electrons | A row of seats |
| Subshell | $s$ (2), $p$ (6), $d$ (10), $f$ (14) electrons max | A section within a row |
| Orbital | Holds max 2 electrons | One seat pair |
| Coulomb's law | Attraction $\propto \dfrac{q_1 q_2}{r^2}$; closer + more protons = lower energy, harder to remove | Front rows are the best seats |
| Aufbau | Fill order: $1s\,2s\,2p\,3s\,3p\,4s\,3d\,4p\,5s\,4d\,5p\,6s\dots$ | Best rows fill first |
| Pauli exclusion | Max 2 per orbital, opposite spins $[\uparrow\downarrow]$ | Two per seat pair, opposite armrests |
| Hund's rule | One electron per orbital in a subshell before pairing | Strangers spread out first |
| Noble-gas shorthand | Bracket the *previous* noble gas: $\ce{Co} = [\ce{Ar}]\,4s^2 3d^7$ | "First rows sold out" |
| Blocks | $s$: Groups 1–2; $p$: 13–18; $d$: 3–12 (subshell = row $-$ 1); $f$: bottom rows (row $-$ 2) | Theater floor plan = the periodic table |
| Valence electrons | Highest-$n$ electrons only ($ns + np$ for main group) | The back row — where all the action is |
| Ions (main group) | Gain/lose to the nearest noble-gas configuration | Fill or empty the outer row completely |
| Ions (transition metals) | $4s$ leaves **before** $3d$ | Back row exits first |
| Exceptions | $\ce{Cr}: [\ce{Ar}]4s^1 3d^5$; $\ce{Cu}: [\ce{Ar}]4s^1 3d^{10}$ (half/full $d$ stability) | One mover, perfectly even section |
| Excited state | Legal capacities, but a lower subshell skipped | Someone ignored a cheap open seat |
| Impossible | A subshell over capacity (e.g., $2s^3$) | Three people on one seat pair |

---

<div align="center">

[← Composition of Mixtures](/chemistry/0302-composition-of-mixtures) | [Photoelectron Spectroscopy →](/chemistry/0304-photoelectron-spectroscopy)

</div>
