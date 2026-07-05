# Lewis Structures
<p class="article-date">July 4, 2026</p>

*Last month Mom put me in charge of my little cousin's birthday party and handed me exactly \$60 — "come back with receipts." Rule one of party planning on a budget: count your money FIRST, before you buy a single thing, because every decision downstream depends on that number. Then you buy the essentials that make it a party at all — a cake, and one goodie bag for every kid. Whatever's left over goes to extras, guests first: candy for the kids before decorations for the host table. And if the budget runs short at the end? You don't invent money — you get creative and make things do double duty, like the cake becoming the centerpiece. It turns out this is exactly how you draw a Lewis structure: the budget is the total valence electron count, the essentials are single bonds, the extras are lone pairs (outer atoms first), and double duty is a double or triple bond. Overspend or underspend by even one dollar and the plan is wrong — which is why every Lewis structure ends with an audit. Master this recipe and you've unlocked the front door to Unit 2: molecular shapes, polarity, and half the FRQs on the exam all start with a correct Lewis structure.*

---

## What You'll Learn

- Count the total valence electrons for any molecule or polyatomic ion — including the charge adjustment for ions
- Apply the same 5-step recipe to draw the Lewis structure of any molecule, every single time
- Pick the correct central atom (least electronegative, never hydrogen)
- Place lone pairs in the right order: outer atoms first, central atom last — and never on hydrogen
- Convert lone pairs into double and triple bonds when the central atom comes up short
- Draw polyatomic ions correctly with brackets and the charge outside
- Recognize the three families of octet-rule exceptions: incomplete octets, expanded octets (period 3+), and odd-electron radicals
- Count bonding vs. nonbonding electrons in a finished structure — a question AP asks directly
- Read bond order off a Lewis structure and use it to rank bond lengths and strengths

---

## Prerequisites

- [Ions and Ionic Compounds](/chemistry/0306-valence-electrons-ionic-compounds) — Lewis dot symbols and counting valence electrons from the group number; that skill is Step 1 of everything here
- [Bonds and Electronegativity](/chemistry/0401-bonds-and-electronegativity) — what a covalent bond *is* (a shared pair) and which atoms are more electronegative, which decides who sits in the center

---

## The Core Concept

### Intuition First

Back to the party, because the analogy has to earn its keep. Here's the full mapping — memorize it once and the whole recipe follows:

| Party planning | Lewis structures |
|---|---|
| Count your total money first, before buying anything | Sum ALL valence electrons — the non-negotiable first step |
| A relative slips you extra cash / someone borrows from the fund | Add electrons for negative charge, subtract for positive |
| Essentials: cake + one goodie bag per guest — it's not a party without them | One single bond from the central atom to every outer atom |
| Extras go to guests first, host last | Lone pairs on outer atoms first, then leftovers on the central atom |
| The toddler guest who's already full gets no extras | Hydrogen never gets lone pairs — it's full at 2 electrons |
| Budget runs short for the host? Make things do double duty | Convert an outer atom's lone pair into a double or triple bond |
| The receipt audit — every dollar accounted for | Recount all electrons in the finished structure |

The audit is the part people skip, and it's the part that saves you. If the party budget was \$60 and your receipts total \$58 or \$62, something is wrong — no exceptions, no "close enough." Same with electrons: if you counted 24 in Step 1 and your drawing shows 22 or 26, the structure is wrong, full stop. Electron count is the audit that catches every Lewis structure error.

### What a Lewis Structure Is

A **Lewis structure** (or Lewis diagram) shows how the valence electrons in a molecule are arranged: which atoms are bonded to which, with how many bonds, and where the unshared electrons sit.

Two kinds of electron real estate:

- A **bonding pair** — 2 electrons shared between two atoms, drawn as a line: $\ce{H-H}$
- A **lone pair** (nonbonding pair) — 2 electrons parked on one atom, drawn as two dots

Every line = 2 electrons. Every pair of dots = 2 electrons. That's the whole accounting system.

**Our text-drawing convention (used all article):** inside code blocks, a dash `-` is a single bond, `=` is a double bond, `≡` is a triple bond, and each `..` or `:` is one lone pair (2 electrons). In regular prose I'll write structures like $\ce{O=C=O}$ and describe the lone pairs in words. For example, water:

```
      ..
  H - O - H        ← two lone pairs on O (drawn above/below),
      ..              two bonding pairs to the H's
```

### The 5-Step Recipe

Here it is — the exact same recipe, every molecule, every time. On the AP exam you will run this recipe on autopilot, so we drill it identically in every worked example below.

> **Step 1 — Count the budget.** Add up the valence electrons of every atom (group number's ones digit). **Add** one electron per unit of negative charge; **subtract** one per unit of positive charge.
>
> **Step 2 — Buy the essentials.** Pick the central atom — the **least electronegative** atom, and **never hydrogen** — and draw a single bond to every outer atom. Subtract 2 electrons per bond.
>
> **Step 3 — Extras for the guests.** Complete the octets of the **outer atoms** with lone pairs (hydrogen is already full with its one bond — it gets nothing).
>
> **Step 4 — Extras for the host.** Any leftover electrons go on the **central atom** as lone pairs.
>
> **Step 5 — Double duty.** If the central atom still lacks an octet, convert a lone pair from an outer atom into an extra bonding pair (making a double or triple bond) until the octet is complete.
>
> **The audit (always).** Recount every electron in the finished structure — bonds count 2 each, lone pairs count 2 each. The total must equal Step 1 **exactly**.

Two quick justifications so this isn't magic:

- **Why is the central atom the least electronegative?** The central atom shares its electrons with the most neighbors. The atom least greedy about electrons ([Bonds and Electronegativity](/chemistry/0401-bonds-and-electronegativity)) tolerates that best. Hydrogen can never be central because it can only form **one** bond — one shared pair fills its only shell ($1s$) at 2 electrons.
- **Why octets at all?** Main-group atoms are at lowest energy with a filled $s + p$ valence set — 8 electrons ($ns^2np^6$). Not a "want," an energy statement — same as in [Ions and Ionic Compounds](/chemistry/0306-valence-electrons-ionic-compounds).

### Ions Get Brackets

For a polyatomic ion, the finished structure goes in **square brackets with the charge outside**, top right:

```
        ..    -
  [ H - O : ]        ← hydroxide, OH⁻
        ..
```

Forgetting the brackets-and-charge costs points on FRQs. Forgetting to adjust the budget for the charge costs the entire structure.

---

## Worked Examples

Watch the recipe run *identically* every time. The molecules get harder; the steps never change.

### Example 1: Water — $\ce{H2O}$

**Problem:** Draw the Lewis structure of $\ce{H2O}$.

**Solution:**

**Step 1 — Count the budget.** O has 6 valence electrons; each H has 1.
$$6 + 2(1) = 8 \text{ electrons}$$

**Step 2 — Buy the essentials.** O is the central atom (H can never be central). Two $\ce{O-H}$ single bonds use $2 \times 2 = 4$ electrons. Remaining: $8 - 4 = 4$.

**Step 3 — Extras for the guests.** The outer atoms are both hydrogens — full at 2 electrons each. They get nothing.

**Step 4 — Extras for the host.** All 4 leftover electrons go on O as two lone pairs.

**Step 5 — Double duty?** O has 2 bonds + 2 lone pairs = 8 electrons. Octet complete — no multiple bonds needed.

```
      ..
  H - O - H
      ..
```

**The audit:** 2 bonds (4 e⁻) + 2 lone pairs (4 e⁻) = 8. Matches Step 1. ✓

**Answer: $\ce{H-O-H}$ with two lone pairs on oxygen.**

### Example 2: Ammonia — $\ce{NH3}$

**Problem:** Draw the Lewis structure of $\ce{NH3}$.

**Solution:**

**Step 1 — Count the budget.** $5 + 3(1) = 8$ electrons.

**Step 2 — Buy the essentials.** N is central. Three $\ce{N-H}$ bonds use 6 electrons. Remaining: 2.

**Step 3 — Extras for the guests.** All outer atoms are H — nothing needed.

**Step 4 — Extras for the host.** The last 2 electrons become one lone pair on N.

**Step 5 — Double duty?** N has 3 bonds + 1 lone pair = 8. Complete.

```
      ..
  H - N - H
      |
      H
```

**The audit:** 3 bonds (6) + 1 lone pair (2) = 8. ✓

**Answer: N bonded to three H's, with one lone pair on N.** (That lone pair will matter enormously when we get to molecular shapes.)

### Example 3: Methane — $\ce{CH4}$

**Problem:** Draw the Lewis structure of $\ce{CH4}$.

**Solution:**

**Step 1 — Count the budget.** $4 + 4(1) = 8$ electrons.

**Step 2 — Buy the essentials.** C is central; four $\ce{C-H}$ bonds use all 8 electrons. Remaining: 0.

**Step 3 — Extras for the guests.** Hydrogens need nothing.

**Step 4 — Extras for the host.** Nothing left — and C already has 4 bonds = 8 electrons.

**Step 5 — Double duty?** Not needed.

```
      H
      |
  H - C - H
      |
      H
```

**The audit:** 4 bonds (8) + 0 lone pairs = 8. ✓

**Answer: C bonded to four H's, zero lone pairs anywhere.** The whole budget went to essentials — a party that's all cake and goodie bags, no decorations.

### Example 4: Carbon Dioxide — $\ce{CO2}$ (first double bonds)

**Problem:** Draw the Lewis structure of $\ce{CO2}$.

**Solution:**

**Step 1 — Count the budget.** $4 + 2(6) = 16$ electrons.

**Step 2 — Buy the essentials.** C is central (less electronegative than O). Two $\ce{C-O}$ bonds use 4. Remaining: 12.

**Step 3 — Extras for the guests.** Each O gets 3 lone pairs (6 electrons each) to complete its octet: $12 - 12 = 0$ left.

**Step 4 — Extras for the host.** Nothing left for C.

**Step 5 — Double duty.** Audit the host: C has only 2 bonds = 4 electrons. Short by 4. Convert **one lone pair from each oxygen** into an extra bonding pair — two double bonds. Now C has $2 \times 4 = 8$. ✓

```
  ..           ..
  O = C = O          ← each O keeps two lone pairs
  ..           ..
```

**The audit:** 2 double bonds ($2 \times 4 = 8$) + 4 lone pairs ($4 \times 2 = 8$) = 16. ✓

**Answer: $\ce{O=C=O}$, two lone pairs on each oxygen.** Note the key move: converting a lone pair to a bond doesn't change the total — it just makes existing electrons do double duty, exactly like the cake becoming the centerpiece. The budget never grows.

### Example 5: Hydrogen Cyanide — $\ce{HCN}$ (a triple bond)

**Problem:** Draw the Lewis structure of $\ce{HCN}$.

**Solution:**

**Step 1 — Count the budget.** $1 + 4 + 5 = 10$ electrons.

**Step 2 — Buy the essentials.** C is central (less electronegative than N; H can't be). Bonds $\ce{H-C}$ and $\ce{C-N}$ use 4. Remaining: 6.

**Step 3 — Extras for the guests.** H needs nothing; N takes all 6 as three lone pairs. Remaining: 0.

**Step 4 — Extras for the host.** Nothing left.

**Step 5 — Double duty.** C has 2 bonds = 4 electrons — short by 4. Convert **two** lone pairs from N into bonding pairs: a triple bond.

```
  H - C ≡ N :
```

**The audit:** $\ce{H-C}$ (2) + $\ce{C#N}$ triple (6) + 1 lone pair on N (2) = 10. ✓

**Answer: $\ce{H-C#N}$ with one lone pair on N.**

### Example 6: Nitrogen Gas — $\ce{N2}$

**Problem:** Draw the Lewis structure of $\ce{N2}$.

**Solution:**

**Step 1 — Count the budget.** $2(5) = 10$ electrons.

**Step 2 — Buy the essentials.** Only two atoms, so no "central" atom — one $\ce{N-N}$ bond uses 2. Remaining: 8.

**Step 3 — Extras for the guests.** Try to complete both octets: that would take $6 + 6 = 12$ electrons, but only 8 remain. Give each N what we can — say 3 lone pairs on one, 1 on the other.

**Step 4 — Extras for the host.** (Merged with Step 3 for a diatomic.)

**Step 5 — Double duty.** At least one N lacks an octet. Convert lone pairs into bonds until both octets close — it takes a **triple bond**:

```
  : N ≡ N :
```

**The audit:** triple bond (6) + 2 lone pairs (4) = 10. ✓

**Answer: $\ce{:N#N:}$ — one lone pair on each nitrogen.** That triple bond is why $\ce{N2}$ is famously unreactive: it's one of the strongest bonds in chemistry (see [Bond Energy and Length](/chemistry/0402-bond-energy-and-length)).

### Example 7: Hydroxide — $\ce{OH-}$ (first ion)

**Problem:** Draw the Lewis structure of $\ce{OH-}$.

**Solution:**

**Step 1 — Count the budget.** $6 + 1 = 7$... **plus 1 for the negative charge** $= 8$ electrons. (A relative slipped an extra dollar into the party fund — count it or everything downstream is wrong.)

**Step 2 — Buy the essentials.** One $\ce{O-H}$ bond uses 2. Remaining: 6.

**Step 3 — Extras for the guests.** H needs nothing.

**Step 4 — Extras for the host.** All 6 go on O: three lone pairs. O has 1 bond + 3 lone pairs = 8. ✓

**Step 5 — Double duty?** Not needed.

```
        ..    -
  [ H - O : ]
        ..
```

**The audit:** 1 bond (2) + 3 lone pairs (6) = 8. ✓ Brackets on, charge outside.

**Answer: $\ce{[H-O:]^-}$ with three lone pairs on O, in brackets with the $-$ charge.**

### Example 8: Ammonium — $\ce{NH4+}$

**Problem:** Draw the Lewis structure of $\ce{NH4+}$.

**Solution:**

**Step 1 — Count the budget.** $5 + 4(1) = 9$, **minus 1 for the positive charge** $= 8$ electrons. (Somebody borrowed a dollar from the fund.)

**Step 2 — Buy the essentials.** N is central; four $\ce{N-H}$ bonds use all 8. Remaining: 0.

**Step 3 — Extras for the guests.** Hydrogens need nothing.

**Step 4 — Extras for the host.** Nothing left; N has 4 bonds = 8. ✓

**Step 5 — Double duty?** Not needed.

```
        H      +
        |
  [ H - N - H ]
        |
        H
```

**The audit:** 4 bonds (8) = 8. ✓

**Answer: N bonded to four H's, no lone pairs, brackets with $+$.** Compare with Example 2: ammonia's lone pair became a fourth bond. Same 8-electron budget — the $+1$ charge and the extra H canceled out.

### Example 9: Carbonate — $\ce{CO3^2-}$

**Problem:** Draw the Lewis structure of $\ce{CO3^2-}$.

**Solution:**

**Step 1 — Count the budget.** $4 + 3(6) = 22$, **plus 2** for the $2-$ charge $= 24$ electrons.

**Step 2 — Buy the essentials.** C is central; three $\ce{C-O}$ bonds use 6. Remaining: 18.

**Step 3 — Extras for the guests.** Each O gets 3 lone pairs: $3 \times 6 = 18$. Remaining: 0.

**Step 4 — Extras for the host.** Nothing left.

**Step 5 — Double duty.** C has only 3 bonds = 6 electrons. Short by 2 — convert **one** lone pair from **one** oxygen into a second bonding pair: one $\ce{C=O}$ double bond.

```
          ..        2-
        [ O           ← this O: two lone pairs, double-bonded
          ‖
    : O - C - O : ]   ← these two O's: three lone pairs each
      ..       ..
```

**The audit:** 1 double bond (4) + 2 single bonds (4) + two O's with 3 lone pairs ($2 \times 6 = 12$) + one O with 2 lone pairs (4) = 24. ✓

**Answer: one $\ce{C=O}$ and two $\ce{C-O}$ bonds, in brackets with $2-$.**

### Example 10: Nitrate — $\ce{NO3-}$ (and a teaser)

**Problem:** Draw the Lewis structure of $\ce{NO3-}$.

**Solution:**

**Step 1 — Count the budget.** $5 + 3(6) = 23$, **plus 1** $= 24$ electrons.

**Step 2 — Buy the essentials.** N is central; three $\ce{N-O}$ bonds use 6. Remaining: 18.

**Step 3 — Extras for the guests.** Three lone pairs per O: 18 used. Remaining: 0.

**Step 4 — Extras for the host.** Nothing left.

**Step 5 — Double duty.** N has 6 — short by 2. Convert one lone pair from one O into a second bond: one $\ce{N=O}$ double bond.

```
          ..        -
        [ O
          ‖
    : O - N - O : ]
      ..       ..
```

**The audit:** 1 double bond (4) + 2 single bonds (4) + $12 + 4$ lone-pair electrons = 24. ✓

**Answer: one $\ce{N=O}$ and two $\ce{N-O}$ bonds, brackets, charge $-$.**

*Teaser:* wait — **which** oxygen gets the double bond? Any of the three works, and experimentally all three $\ce{N-O}$ bonds are identical. Nitrate has *options*, and the resolution is called **resonance** — the whole story of the [next article](/chemistry/0405-resonance-formal-charge). For now: any one correct structure earns the AP point.

### Example 11: Sulfate — $\ce{SO4^2-}$

**Problem:** Draw the Lewis structure of $\ce{SO4^2-}$.

**Solution:**

**Step 1 — Count the budget.** $6 + 4(6) = 30$, **plus 2** $= 32$ electrons.

**Step 2 — Buy the essentials.** S is central (less electronegative than O); four $\ce{S-O}$ bonds use 8. Remaining: 24.

**Step 3 — Extras for the guests.** Three lone pairs per O: $4 \times 6 = 24$. Remaining: 0.

**Step 4 — Extras for the host.** Nothing left — and S already has 4 bonds = 8 electrons. ✓

**Step 5 — Double duty?** Not needed. Everything closes on the first pass.

```
          ..        2-
        [ O :
          |
    : O - S - O : ]     ← every O: three lone pairs
      ..  |    ..
        : O :
          ..
```

**The audit:** 4 bonds (8) + 12 lone pairs (24) = 32. ✓

**Answer: S with four single bonds to O, three lone pairs on each O, brackets with $2-$.** (You may see textbook versions with $\ce{S=O}$ double bonds — that's a formal-charge argument, and it needs sulfur's expanded-octet privilege. Next article. The all-single-bond octet structure above is fully AP-legal.)

### Example 12: Reading a Finished Structure — Bonding vs. Nonbonding Electrons

**Problem:** For the $\ce{CO2}$ structure from Example 4, how many electrons are **bonding** and how many are **nonbonding**? Then do the same for $\ce{NH3}$.

**Solution:**

**Step 1:** $\ce{O=C=O}$ has 2 double bonds = 4 bonding pairs $= 8$ **bonding electrons**.

**Step 2:** Each O carries 2 lone pairs → 4 lone pairs total $= 8$ **nonbonding electrons**.

**Step 3:** Audit: $8 + 8 = 16$. Matches the budget. ✓

**Step 4:** $\ce{NH3}$: 3 bonds = 6 bonding electrons; 1 lone pair on N = 2 nonbonding electrons. Audit: $6 + 2 = 8$. ✓

**Answer: $\ce{CO2}$ — 8 bonding, 8 nonbonding. $\ce{NH3}$ — 6 bonding, 2 nonbonding.** AP multiple-choice asks this *exact* question. It's a receipts problem: sort every electron into one of two piles, and the piles must sum to the budget.

---

## Octet Rule Exceptions

The recipe covers 90% of AP molecules. Three families break it — like party guests with special requirements.

### 1. Incomplete Octets (the minimalist hosts)

**Beryllium and boron** are stable with *fewer* than 8 electrons — Be with 4, B with 6.

- $\ce{BeH2}$: budget $2 + 2(1) = 4$. Two bonds use it all: $\ce{H-Be-H}$. Be sits at 4 electrons. Done — there are no lone pairs anywhere to promote.
- $\ce{BF3}$: budget $3 + 3(7) = 24$. Three $\ce{B-F}$ bonds (6) + three lone pairs on each F (18) = 24. Boron has only 6 electrons — **and that's the accepted structure.** (Making a $\ce{B=F}$ double bond would put a positive formal charge on fluorine, the most electronegative element — a worse deal, as the next article shows.) $\ce{BF3}$'s hunger for one more pair is exactly why it's a classic Lewis *acid* later in the course.

### 2. Expanded Octets (the hosts with a bigger house) — period 3 and below ONLY

Atoms in **period 3 or lower** (P, S, Cl, Xe, ...) can hold **more** than 8 electrons when they're the central atom. The simple why: their valence shell ($n = 3$ or higher) is physically bigger and has room beyond the $s$ and $p$ orbitals, so it can accommodate extra pairs. Period 2 atoms (C, N, O, F) have only $2s$ and $2p$ — four orbitals, eight electrons, hard ceiling. **Never expand a period-2 octet.**

- $\ce{PCl5}$: budget $5 + 5(7) = 40$. Five bonds (10) + 3 lone pairs on each Cl (30) = 40. P holds 10 electrons.
- $\ce{SF6}$: budget $6 + 6(7) = 48$. Six bonds (12) + 3 lone pairs per F (36) = 48. S holds 12.
- $\ce{XeF4}$: budget $8 + 4(7) = 36$. Four bonds (8) + 3 lone pairs per F (24) = 32... audit says 4 electrons remain, so Step 4 parks **two lone pairs on Xe**: $32 + 4 = 36$. ✓ Xe holds 12 electrons. Yes, a noble gas bonding — the recipe doesn't flinch.

Notice: the recipe *still works* for expanded octets. Steps 1–4 run normally; the central atom simply ends up holding more than 8. The audit still balances.

### 3. Odd-Electron Radicals (one paragraph, promise)

If the Step-1 budget is an **odd number**, no arrangement gives everyone a pair — someone ends up with a single unpaired electron, and the species is called a **free radical**. $\ce{NO}$ has $5 + 6 = 11$ electrons; $\ce{NO2}$ has $5 + 2(6) = 17$. Draw the best structure you can (in $\ce{NO}$, a double bond with the odd electron on N) and don't panic: radicals are reactive precisely *because* of that unpaired electron. On the AP exam, the usual ask is just to **recognize** that an odd total means a radical and no octet is possible.

---

## Bond Order: Reading Length and Strength Off the Picture

**Bond order** = the number of shared pairs between two atoms. Single bond → 1, double → 2, triple → 3. From [Bond Energy and Length](/chemistry/0402-bond-energy-and-length):

$$\text{higher bond order} \;\Rightarrow\; \text{shorter bond} \;\Rightarrow\; \text{stronger bond}$$

**Classic AP ranking:** compare the carbon–oxygen bond in methanol ($\ce{CH3OH}$), carbon dioxide ($\ce{CO2}$), and carbon monoxide ($\ce{CO}$).

| Species | C–O bond in the Lewis structure | Bond order | Length |
|---|---|---|---|
| $\ce{CH3OH}$ | $\ce{C-O}$ single | 1 | longest (~143 pm) |
| $\ce{CO2}$ | $\ce{C=O}$ double | 2 | middle (~116 pm) |
| $\ce{CO}$ | $\ce{C#O}$ triple | 3 | shortest (~113 pm) |

So the length ranking is $\ce{CH3OH} > \ce{CO2} > \ce{CO}$, and bond strength runs exactly the other way. One correct Lewis structure per molecule, and the ranking falls out for free — this is why the College Board keeps asking it.

---

## Common Mistakes

| The mistake | Why it happens | How to avoid it |
|---|---|---|
| Forgetting the ion charge in Step 1 | You're focused on the atoms and ignore the superscript | Say it out loud: "$2-$ means the fund got **2 extra dollars**." Add for negative, subtract for positive — *before* anything else |
| Skipping the final audit | The structure "looks right" | The audit takes 10 seconds and catches every miscount. Receipts, always |
| Lone pairs on hydrogen, or $\ce{H}$ double-bonded | Treating H like every other atom | H's shell holds 2 electrons, period. One bond, zero extras — the toddler is full |
| Making H the central atom | It's written first in formulas like $\ce{H2O}$ | H forms exactly one bond; it *can't* hold a molecule together |
| Expanding a period-2 octet ($\ce{C, N, O, F}$ with 10+ electrons) | Copying the $\ce{SF6}$ move onto nitrogen | Legality check first: expanded octets are **period 3+** only |
| Putting leftover electrons on outer atoms whose octets are done | Dumping extras anywhere | Order matters: guests first, but once a guest's octet is full, everything remaining goes to the **host** (Step 4) |
| No brackets/charge on a polyatomic ion | Rushing the final drawing | Brackets + charge is part of the answer, not decoration |
| Adding new electrons in Step 5 instead of converting | The central atom "needs more," so you invent them | Double duty means **sharing existing** lone pairs. The budget never grows |

---

## AP Exam Tips

- **Electron miscounts are the #1 self-inflicted wound** on this topic. A wrong Step-1 count guarantees a wrong structure no matter how well you run Steps 2–5. Count twice, then **audit the finished drawing** — the College Board's own scoring notes dock structures with the wrong electron total even when the connectivity is right.
- **Ion charges change the budget.** $\ce{CO3^2-}$ has 24 electrons, not 22. When an FRQ hands you a polyatomic ion, the charge adjustment is the first thing graders check. Add for negative, subtract for positive.
- **Run the legality check before expanding an octet.** Central atom in period 3 or lower → expansion allowed ($\ce{PCl5}$, $\ce{SF6}$, $\ce{XeF4}$). Period 2 → hard ceiling of 8. "Nitrogen with five bonds" is an automatic lost point.
- **Lewis structures are the ENTRY POINT to VSEPR.** The classic Unit 2 FRQ chain is: draw the Lewis structure → predict geometry → predict bond angle → decide polarity. A wrong structure poisons every downstream part — that's 3–4 points riding on your Step-1 count. This is the single best reason to build the audit habit now.
- **Know the direct-count questions:** "How many bonding electrons? How many lone pairs on the central atom?" These are free points if your structure is right (see Example 12).
- **Bond-order rankings** ("rank these C–O bonds by length") are answered entirely from Lewis structures — no memorized lengths needed, just bond orders and the rule *higher order = shorter = stronger*.

---

## Practice Problems

Run the full recipe on every one — and write the audit line. That habit is the whole point.

### Problem 1
Draw the Lewis structure of $\ce{HF}$.

<details>
<summary><strong>Solution</strong></summary>

**Step 1:** $1 + 7 = 8$ electrons.
**Step 2:** One $\ce{H-F}$ bond: 2 used, 6 remain.
**Step 3:** H is full; F takes three lone pairs (6). 0 remain.
**Steps 4–5:** Nothing left; F has $2 + 6 = 8$. ✓

```
        ..
  H - F :
        ..
```

**Audit:** $2 + 6 = 8$. ✓

**Answer: $\ce{H-F}$ with three lone pairs on F.**

</details>

### Problem 2
Draw the Lewis structure of $\ce{H2S}$.

<details>
<summary><strong>Solution</strong></summary>

**Step 1:** $2(1) + 6 = 8$ electrons.
**Step 2:** S central; two $\ce{S-H}$ bonds: 4 used, 4 remain.
**Step 3:** H's are full.
**Step 4:** Two lone pairs on S. S has 8. ✓
**Step 5:** Not needed.

**Audit:** $4 + 4 = 8$. ✓

**Answer: $\ce{H-S-H}$ with two lone pairs on S — water's structure with S swapped in.**

</details>

### Problem 3
Draw the Lewis structure of $\ce{PH3}$.

<details>
<summary><strong>Solution</strong></summary>

**Step 1:** $5 + 3(1) = 8$ electrons.
**Step 2:** P central; three bonds use 6, leaving 2.
**Step 3:** H's full.
**Step 4:** One lone pair on P. P has 8. ✓

**Audit:** $6 + 2 = 8$. ✓

**Answer: P bonded to three H's with one lone pair on P — ammonia's twin.**

</details>

### Problem 4
Draw the Lewis structure of $\ce{CCl4}$.

<details>
<summary><strong>Solution</strong></summary>

**Step 1:** $4 + 4(7) = 32$ electrons.
**Step 2:** C central (less electronegative); four $\ce{C-Cl}$ bonds use 8, leaving 24.
**Step 3:** Three lone pairs on each Cl: 24 used. 0 remain.
**Step 4:** Nothing left; C has 4 bonds = 8. ✓
**Step 5:** Not needed.

**Audit:** $8 + 24 = 32$. ✓

**Answer: C with four single bonds to Cl, three lone pairs on each Cl.**

</details>

### Problem 5
Draw the Lewis structure of $\ce{SiH4}$.

<details>
<summary><strong>Solution</strong></summary>

**Step 1:** $4 + 4(1) = 8$ electrons.
**Step 2:** Si central; four bonds use all 8.
**Steps 3–5:** H's full, nothing left, Si has 8. ✓

**Audit:** $8 = 8$. ✓

**Answer: Si bonded to four H's, no lone pairs — methane's structure one row down.**

</details>

### Problem 6
Draw the Lewis structure of $\ce{O2}$.

<details>
<summary><strong>Solution</strong></summary>

**Step 1:** $2(6) = 12$ electrons.
**Step 2:** One $\ce{O-O}$ bond: 2 used, 10 remain.
**Step 3:** Completing both octets would need 12 — only 10 available.
**Step 5:** Convert a lone pair into a second bond: $\ce{O=O}$, then each O gets 2 lone pairs.

```
  ..         ..
  O = O
  ..         ..
```

**Audit:** double bond (4) + 4 lone pairs (8) = 12. ✓

**Answer: $\ce{O=O}$ with two lone pairs on each oxygen.**

</details>

### Problem 7
Draw the Lewis structure of $\ce{CO}$.

<details>
<summary><strong>Solution</strong></summary>

**Step 1:** $4 + 6 = 10$ electrons.
**Step 2:** One bond: 2 used, 8 remain.
**Step 3:** Give O three lone pairs (6), C one lone pair (2). C has only 4 — badly short.
**Step 5:** Convert two of O's lone pairs into bonds: a triple bond.

```
  : C ≡ O :
```

**Audit:** triple bond (6) + 2 lone pairs (4) = 10. ✓

**Answer: $\ce{:C#O:}$ — one lone pair on each atom.** Same electron count and same structure pattern as $\ce{N2}$ (they're isoelectronic).

</details>

### Problem 8
Draw the Lewis structure of ethene, $\ce{C2H4}$ (the two carbons are bonded to each other, two H's on each).

<details>
<summary><strong>Solution</strong></summary>

**Step 1:** $2(4) + 4(1) = 12$ electrons.
**Step 2:** Skeleton: $\ce{C-C}$ plus four $\ce{C-H}$ bonds = 5 bonds = 10 used, 2 remain.
**Step 3:** H's full.
**Step 4:** One lone pair on a carbon — but then the other C has only 6.
**Step 5:** Convert that lone pair into a second $\ce{C-C}$ bond. Both carbons now have 4 bonds = 8. ✓

```
  H       H
    \    /
     C = C
    /    \
  H       H
```

**Audit:** 6 bonding pairs = 12. ✓

**Answer: $\ce{H2C=CH2}$ — a $\ce{C=C}$ double bond, no lone pairs.**

</details>

### Problem 9
Draw the Lewis structure of nitrite, $\ce{NO2-}$.

<details>
<summary><strong>Solution</strong></summary>

**Step 1:** $5 + 2(6) = 17$, **plus 1** for the charge $= 18$ electrons.
**Step 2:** N central; two $\ce{N-O}$ bonds: 4 used, 14 remain.
**Step 3:** Three lone pairs per O: 12 used, 2 remain.
**Step 4:** One lone pair on N. N has $4 + 2 = 6$ — short.
**Step 5:** Convert one O lone pair into a second bond: one $\ce{N=O}$.

```
    ..            -
  [ O = N - O : ]     ← N keeps its lone pair;
    ..    ..   ..        double-bonded O has 2 lone pairs, single-bonded O has 3
```

**Audit:** double bond (4) + single bond (2) + N lone pair (2) + O lone pairs ($4 + 6$) = 18. ✓

**Answer: $\ce{[O=N-O]^-}$ with a lone pair on N, brackets and charge.** (Either oxygen can take the double bond — resonance again, next article.)

</details>

### Problem 10
Draw the Lewis structure of phosphate, $\ce{PO4^3-}$.

<details>
<summary><strong>Solution</strong></summary>

**Step 1:** $5 + 4(6) = 29$, **plus 3** $= 32$ electrons.
**Step 2:** P central; four bonds: 8 used, 24 remain.
**Step 3:** Three lone pairs per O: 24 used. 0 remain.
**Step 4:** P has 4 bonds = 8. ✓
**Step 5:** Not needed.

**Audit:** $8 + 24 = 32$. ✓

**Answer: P with four single bonds to O, three lone pairs per O, brackets with $3-$ — sulfate's structure with one more unit of charge.**

</details>

### Problem 11
Draw the Lewis structure of sulfite, $\ce{SO3^2-}$.

<details>
<summary><strong>Solution</strong></summary>

**Step 1:** $6 + 3(6) = 24$, **plus 2** $= 26$ electrons.
**Step 2:** S central; three bonds: 6 used, 20 remain.
**Step 3:** Three lone pairs per O: 18 used, 2 remain.
**Step 4:** One lone pair on S. S has $6 + 2 = 8$. ✓
**Step 5:** Not needed.

**Audit:** $6 + 18 + 2 = 26$. ✓

**Answer: S with three single bonds to O and one lone pair on S; three lone pairs per O; brackets with $2-$.** That lone pair on S is the structural difference between sulfite and (flat, lone-pair-free) nitrate-style ions — it will bend the shape in the VSEPR article.

</details>

### Problem 12
Draw the Lewis structure of $\ce{BF3}$ and explain why boron does not get a full octet.

<details>
<summary><strong>Solution</strong></summary>

**Step 1:** $3 + 3(7) = 24$ electrons.
**Step 2:** B central; three bonds: 6 used, 18 remain.
**Step 3:** Three lone pairs per F: 18 used. 0 remain.
**Step 4:** Nothing left; B has only 6.
**Step 5:** We *could* force a $\ce{B=F}$ double bond — but fluorine, the most electronegative element, refuses to share extra density toward boron (formally: it would put a positive formal charge on F). The accepted structure leaves boron at 6.

**Audit:** $6 + 18 = 24$. ✓

**Answer: B with three single bonds to F, three lone pairs per F, and an incomplete octet (6 electrons) on boron — a legitimate octet exception.**

</details>

### Problem 13
Draw the Lewis structure of $\ce{XeF2}$, and state why xenon is allowed to exceed an octet while oxygen never is.

<details>
<summary><strong>Solution</strong></summary>

**Step 1:** $8 + 2(7) = 22$ electrons.
**Step 2:** Xe central; two bonds: 4 used, 18 remain.
**Step 3:** Three lone pairs per F: 12 used, 6 remain.
**Step 4:** All 6 go on Xe as **three lone pairs**. Xe holds $4 + 6 = 10$ electrons — an expanded octet.
**Step 5:** Not needed.

**Audit:** $4 + 12 + 6 = 22$. ✓

**Why it's legal:** Xe is in period 5 — its valence shell is large enough to hold more than four pairs. Oxygen is period 2: only the $2s$ and $2p$ orbitals exist, four orbitals, hard cap of 8 electrons. Expanded octets are a **period 3+** privilege only.

**Answer: $\ce{F-Xe-F}$ with three lone pairs on Xe and three on each F.**

</details>

### Problem 14
For the carbonate ion $\ce{CO3^2-}$ (Example 9), how many electrons are bonding and how many are nonbonding? Verify with the audit.

<details>
<summary><strong>Solution</strong></summary>

**Step 1:** Bonds: one $\ce{C=O}$ double (2 pairs) + two $\ce{C-O}$ singles (2 pairs) = 4 bonding pairs = **8 bonding electrons**.

**Step 2:** Lone pairs: two single-bonded O's with 3 each + the double-bonded O with 2 = 8 lone pairs = **16 nonbonding electrons**.

**Step 3 — Audit:** $8 + 16 = 24$ = the Step-1 budget ($22 + 2$). ✓ Every electron in one of the two piles, piles sum to the budget.

**Answer: 8 bonding electrons, 16 nonbonding electrons.**

</details>

### Problem 15
Rank the nitrogen–nitrogen bond length in hydrazine ($\ce{H2N-NH2}$), diazene ($\ce{HN=NH}$), and nitrogen gas ($\ce{N2}$) from longest to shortest, using Lewis structures.

<details>
<summary><strong>Solution</strong></summary>

**Step 1:** Draw (or recall) the structures and read the N–N bond order from each:

- Hydrazine: budget $2(5) + 4(1) = 14$; skeleton uses 5 bonds (10), one lone pair on each N (4). $\ce{N-N}$ single → bond order 1.
- Diazene: budget $2(5) + 2(1) = 12$; the recipe forces $\ce{HN=NH}$ with a lone pair on each N → bond order 2.
- $\ce{N2}$: $\ce{:N#N:}$ → bond order 3 (Example 6).

**Step 2:** Higher bond order → shorter bond.

**Answer: $\ce{H2N-NH2} > \ce{HN=NH} > \ce{N2}$ (longest to shortest); bond strength runs in the reverse order.**

</details>

---

## Quick Reference

**The 5-step recipe (+ audit):**

| Step | Party version | Chemistry version |
|---|---|---|
| 1 | Count ALL the money first | Sum valence electrons; **+1 per negative charge, −1 per positive** |
| 2 | Buy the essentials | Central atom = least electronegative, never H; single bond to every outer atom |
| 3 | Extras for the guests | Complete outer atoms' octets (H gets nothing) |
| 4 | Extras for the host | Leftovers become lone pairs on the central atom |
| 5 | Make things do double duty | Central atom short? Convert outer lone pairs → double/triple bonds |
| ✓ | Check the receipts | **Recount every electron — must equal Step 1 exactly** |

**Electron accounting:** each bond line = 2 e⁻; each lone pair = 2 e⁻; double bond = 4 e⁻; triple = 6 e⁻.

**Octet exceptions:**

| Exception | Examples | Rule |
|---|---|---|
| Incomplete octet | $\ce{BeH2}$ (4 e⁻ on Be), $\ce{BF3}$ (6 e⁻ on B) | Be and B are stable short |
| Expanded octet | $\ce{PCl5}$ (10), $\ce{SF6}$ (12), $\ce{XeF4}$ (12) | **Period 3+ central atoms only** |
| Odd-electron radical | $\ce{NO}$ (11 e⁻), $\ce{NO2}$ (17 e⁻) | Odd budget → one unpaired electron, no full octet possible |

**Bond order:** single = 1, double = 2, triple = 3; higher order → shorter, stronger bond ($\ce{CH3OH} > \ce{CO2} > \ce{CO}$ in C–O length).

---

<div align="center">

[← Ionic Solids, Metals, Alloys](/chemistry/0403-ionic-solids-metals-alloys) | [Resonance and Formal Charge →](/chemistry/0405-resonance-formal-charge)

</div>
