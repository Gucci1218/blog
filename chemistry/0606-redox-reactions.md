# Redox Reactions
<p class="article-date">July 5, 2026</p>

*I sliced an apple for lunch, got distracted texting, and came back ten minutes later to find the flesh had gone brown and sad. Nobody spilled anything on it. Nothing touched it. So what happened? Oxygen in the air literally reached into the cut surface and **stole electrons** from molecules in the apple — and losing electrons is what turned them brown. Here's the cool part: squeeze a little lemon juice on the next slice and it stays bright white. The vitamin C in lemon juice is an "antioxidant," which is a fancy way of saying it throws its OWN electrons at the oxygen first, sacrificing itself so the apple's molecules keep theirs. That electron hand-off — one thing losing electrons, another gaining them, always at the same time, always as a pair — is a **redox reaction**. And it's not some niche kitchen trick: the exact same electron-transfer chemistry rusts your bike, powers the battery in your phone, and burns the gas in a car engine. This is AP Unit 4, Topic 4.9, and it's the gateway to all of electrochemistry in Unit 9.*

---

## What You'll Learn
- Explain what a redox reaction is: a **transfer of electrons**, where oxidation (electron loss) and reduction (electron gain) always happen together as a pair
- Use the mnemonic **OIL RIG** — *Oxidation Is Loss, Reduction Is Gain* (of electrons) — to keep the two halves straight
- Assign **oxidation numbers** to any atom in a compound or polyatomic ion using an ordered set of rules
- Identify whether a reaction is redox by watching for a **change in oxidation number**
- Distinguish redox reactions from non-redox reactions (like most acid–base and precipitation reactions)
- Identify the **oxidizing agent** and **reducing agent** in a reaction — and correctly state that the oxidizing agent is the species that gets *reduced*
- Split a redox reaction into **half-reactions**, balancing each for mass and charge with explicit electrons
- Combine half-reactions so that **electrons lost = electrons gained**, producing a balanced overall equation
- Recognize the common redox families — combustion, single replacement, corrosion, combination — and see how batteries (Unit 9) put redox to work

---

## Prerequisites
- [Net Ionic Equations](/chemistry/0601-net-ionic-equations) — redox is easiest to read once spectator ions are stripped away and you can see who actually trades electrons
- [Ions and Ionic Compounds](/chemistry/0306-valence-electrons-ionic-compounds) — oxidation numbers are basically "pretend charges," so you need to be fluent in real ionic charges first

---

## The Core Concept

### Intuition First

Back to the browning apple. Zoom in on the cut surface. The apple flesh is full of molecules (an enzyme-driven story involving compounds called polyphenols, but you don't need the biochem for AP) that are perfectly happy holding onto their electrons. Then oxygen shows up. Oxygen is *greedy* for electrons — it's one of the most electron-hungry elements on the periodic table (remember electronegativity?). So oxygen grabs electrons off the apple molecules, and that electron theft chemically changes them into brown pigments.

Let's name the roles, because these exact names are the whole vocabulary of this topic:

- The **apple molecules lose electrons** → they are **oxidized**. Because they *hand over* electrons that let oxygen react, they are also the **reducing agent** (they "reduce" the oxygen by feeding it electrons).
- The **oxygen gains electrons** → it is **reduced**. Because it *causes* the apple to be oxidized, oxygen is the **oxidizing agent**.

Notice something that trips up literally every AP student: the oxygen is the oxidiz**ing** agent, and yet oxygen itself gets **reduced**. The agent does the opposite of its name. Hold that thought — we'll hammer it later.

Now the lemon-juice trick. Vitamin C (ascorbic acid) is an **antioxidant**. When you squeeze it on, it donates its own electrons to the oxygen *before* the apple molecules have to. The oxygen still gets reduced — it still gets fed — but now it's eating vitamin C's electrons instead of the apple's. Vitamin C is a **sacrificial reducing agent**: it throws itself in front of the oxygen to protect the apple. (This is exactly why "antioxidants" are a health buzzword — in your body they intercept electron-stealing oxygen species before those species damage your cells.)

So the whole scene is one redox reaction with three characters:

| Kitchen role | Chemistry role | What happens to its electrons |
|---|---|---|
| Apple flesh molecules | substance oxidized = **reducing agent** | **loses** electrons (turns brown) |
| Oxygen from the air | substance reduced = **oxidizing agent** | **gains** electrons |
| Vitamin C (lemon juice) | sacrificial reducing agent (antioxidant) | **loses** electrons *instead of* the apple |

Every redox reaction in this article — rusting bikes, burning fuel, thermite, batteries — is this same three-word story: **someone loses electrons, someone gains them, at the same time.** Let's make it precise.

### Redox = Reduction + Oxidation

"Redox" is just a mashup of **RED**uction and **OX**idation. The two always occur together, because electrons don't just vanish — if one species loses them, another must be there to catch them.

> **Oxidation** = loss of electrons.
> **Reduction** = gain of electrons.

The mnemonic that will save you on the exam:

$$\boxed{\textbf{OIL RIG}} \quad\Longrightarrow\quad \textbf{O}xidation \textbf{I}s \textbf{L}oss, \quad \textbf{R}eduction \textbf{I}s \textbf{G}ain$$

(If you prefer, the other common version is **LEO the lion says GER**: *Lose Electrons = Oxidation, Gain Electrons = Reduction.* Pick one and stick with it — this article uses OIL RIG throughout.)

A quick warning on the word "reduction." It sounds like something is getting bigger or smaller in size — it isn't. "Reduction" refers to the **charge** going down (getting *more negative*) as the atom gains negatively-charged electrons. $\ce{Cu^2+}$ gaining 2 electrons to become $\ce{Cu}$ went from $+2$ to $0$ — the charge was *reduced*. That's the origin of the name.

### Oxidation Numbers: Bookkeeping for Electrons

To *track* electron transfer we need a bookkeeping device: the **oxidation number** (also called oxidation state). It's the charge an atom *would* have if we pretended every bond were fully ionic — that is, if we handed each shared electron pair entirely to the more electronegative atom. It's a fiction, but a spectacularly useful one, because **a change in oxidation number is the fingerprint of redox.**

Apply these rules **in order** — when two rules seem to conflict, the higher one wins:

1. **A pure element has an oxidation number of 0.** This includes diatomics: $\ce{Na}$, $\ce{O2}$, $\ce{Cl2}$, $\ce{P4}$ are all $0$.
2. **A monatomic ion's oxidation number equals its charge.** $\ce{Na+}$ is $+1$, $\ce{Cl-}$ is $-1$, $\ce{Al^3+}$ is $+3$.
3. **Fluorine is always $-1$** in compounds (it's the most electronegative element, so it never shares generously).
4. **Oxygen is usually $-2$.** Exceptions: in **peroxides** (like $\ce{H2O2}$) it's $-1$; when bonded to fluorine (like $\ce{OF2}$) it's positive.
5. **Hydrogen is usually $+1$** (when bonded to nonmetals). Exception: in **metal hydrides** (like $\ce{NaH}$, $\ce{CaH2}$) it's $-1$.
6. **The oxidation numbers in a species must sum to the overall charge.** For a neutral compound the sum is $0$; for a polyatomic ion the sum equals the ion's charge.

Rule 6 is the workhorse — it's the algebra that lets you solve for the one unknown (usually a metal or a central atom) once the others are pinned down by rules 1–5. Notice the priority order: F beats O beats H. So in $\ce{OF2}$, fluorine claims $-1$ (rule 3 is higher), forcing oxygen to be $+2$.

### Oxidizing Agent vs. Reducing Agent

This is the single most-tested confusion in the whole topic, so let's be surgical about it. The **agent** is the *entire species* — the whole molecule or ion, not just the atom that changes.

| Term | Definition | What happens to IT | Kitchen example |
|---|---|---|---|
| **Oxidizing agent** | the species that *causes* oxidation by taking electrons | it is itself **reduced** (gains electrons) | oxygen (steals the apple's electrons) |
| **Reducing agent** | the species that *causes* reduction by giving electrons | it is itself **oxidized** (loses electrons) | the apple flesh (and vitamin C) |

The mind-bender, said plainly: **the oxidizing agent gets reduced, and the reducing agent gets oxidized.** Each agent does the *opposite* of its name to itself. Why? Because you name an agent by what it does to its *partner*, not to itself. Oxygen is the oxidizing agent because it *oxidizes the apple* — and to do that, it must *accept* the apple's electrons, which means oxygen is reduced.

A memory hook: an oxidizing agent is an **electron thief** (it takes them and is reduced); a reducing agent is an **electron donor** (it gives them and is oxidized). The apple donates; the oxygen steals.

### Half-Reactions: Splitting the Trade in Two

A redox reaction is a single event, but it's clarifying to split it into two **half-reactions** — one for oxidation, one for reduction — each showing the electrons explicitly. Take zinc metal dropped into copper(II) sulfate solution (a classic single-replacement redox):

$$\ce{Zn + Cu^2+ -> Zn^2+ + Cu}$$

Split it:

- **Oxidation half** (zinc loses 2 electrons, $0 \to +2$): $\qquad \ce{Zn -> Zn^2+ + 2e-}$
- **Reduction half** (copper gains 2 electrons, $+2 \to 0$): $\quad \ce{Cu^2+ + 2e- -> Cu}$

Two rules make a half-reaction correct:

1. **Balance mass** — same atoms of each element on both sides.
2. **Balance charge** — add electrons ($\ce{e-}$) to whichever side needs them so the total charge matches on both sides. Electrons appear on the **right** for oxidation (they're lost) and on the **left** for reduction (they're gained).

The bridge principle for combining halves:

> **Electrons lost must equal electrons gained.** No electrons are left floating.

Here zinc loses 2 and copper gains 2 — already equal, so we just add the halves and the electrons cancel, recovering the overall equation. When the numbers *don't* match, you scale each half by a whole number to reach a common multiple of electrons (see Example 11), exactly like finding a common denominator.

**Balancing in acidic solution (the fuller method).** When oxygen and hydrogen don't balance on their own — common for polyatomic ions like $\ce{MnO4-}$ — AP uses this recipe on each half-reaction: (1) balance the main element, (2) balance O by adding $\ce{H2O}$, (3) balance H by adding $\ce{H+}$, (4) balance charge by adding $\ce{e-}$. Example 12 walks through it once in full.

### The Redox Family Album

Once you can spot oxidation-number changes, you'll notice redox everywhere. Several reaction types you already know are *always* redox:

| Family | Example | Why it's redox |
|---|---|---|
| **Combustion** | $\ce{CH4 + 2O2 -> CO2 + 2H2O}$ | carbon and oxygen both change oxidation state; fuel is oxidized |
| **Single replacement** | $\ce{Zn + 2HCl -> ZnCl2 + H2}$ | a free element becomes an ion (and vice versa) — states must change |
| **Corrosion / rusting** | $\ce{4Fe + 3O2 -> 2Fe2O3}$ | iron $0 \to +3$, oxygen $0 \to -2$ (your bike, from [Why Chemistry Matters](/chemistry/0001-why-chemistry-matters)) |
| **Combination of elements** | $\ce{2Mg + O2 -> 2MgO}$ | two pure elements ($0$) become ions in a compound |

And the big forward link: a **battery** is just a redox reaction with the two half-reactions physically *separated* so the electrons are forced to travel through a wire to get from the reducing agent to the oxidizing agent — and that moving electron stream is electric current. Rust wastes redox; a battery harnesses it. That's the entire subject of **Unit 9 (Electrochemistry)** — cells, cell potential, and electrolysis. For now, just master identifying the players.

> **🎬 Hollywood Chemistry: Real or Not? — The Thermite Reaction**
> *The scene:* A pile of grey powder is lit, and it erupts into a blinding white-hot cascade that melts straight through a car engine block (or, in *Dr. Stone*, Senku uses it to smelt iron and rebuild civilization from raw ore).
> *The verdict:* **100% real, and genuinely that violent.** Thermite is powdered aluminum mixed with iron(III) oxide (rust): $\ce{2Al + Fe2O3 -> 2Fe + Al2O3}$. It's a textbook **single-replacement redox** — aluminum is such a hungry reducing agent that it rips the oxygen away from iron, getting oxidized from $0$ to $+3$ while iron is reduced from $+3$ back to molten metal ($0$). The reaction hits temperatures over $2500\,^\circ\text{C}$ — hot enough to produce liquid iron, which is exactly why real welders use thermite to fuse railroad track in the field. The anime version (making iron to advance the tech tree) is chemically legit; the movie version (melting an engine in seconds) is also legit. This one's real.

---

## Worked Examples

### Example 1: Oxidation Number of a Lone Element

**Problem:** What is the oxidation number of sulfur in $\ce{S8}$ (a ring of eight sulfur atoms)?

**Solution:**

**Step 1:** $\ce{S8}$ is a pure element — no other element is present.

**Step 2:** Rule 1 says any pure element is $0$, regardless of how many atoms cluster together.

**Answer:** $\ce{S} = 0$.

### Example 2: The Easy Cases — Ions and Simple Salts

**Problem:** Assign oxidation numbers to every atom in (a) $\ce{Al^3+}$, (b) $\ce{NaCl}$, (c) $\ce{MgBr2}$.

**Solution:**

**(a)** Monatomic ion → oxidation number = charge (rule 2). $\ce{Al^3+} = +3$.

**(b)** $\ce{Na}$ is a group-1 metal, so $+1$; the compound is neutral, so $\ce{Cl}$ must be $-1$ (rule 6). $\ce{Na} = +1$, $\ce{Cl} = -1$.

**(c)** $\ce{Br}$ is a halogen acting like a $-1$ ion here, and there are two of them ($-2$ total). To sum to $0$, $\ce{Mg} = +2$.

**Answer:** (a) $\ce{Al}=+3$; (b) $\ce{Na}=+1$, $\ce{Cl}=-1$; (c) $\ce{Mg}=+2$, $\ce{Br}=-1$.

### Example 3: Solving for the Unknown — Chromium in Dichromate

**Problem:** Find the oxidation number of chromium in the dichromate ion, $\ce{Cr2O7^2-}$.

**Solution:**

**Step 1:** Oxygen is $-2$ (rule 4, no peroxide or fluorine here). There are 7 oxygens: $7 \times (-2) = -14$.

**Step 2:** This is a polyatomic ion with charge $-2$, so all oxidation numbers must sum to $-2$ (rule 6). Let each chromium be $x$; there are 2 of them:

$$2x + (-14) = -2$$

**Step 3:** Solve: $2x = +12$, so $x = +6$.

**Answer:** $\ce{Cr} = +6$. (Chromium loves the $+6$ state — that's why dichromate is such a strong oxidizing agent.)

### Example 4: Sulfur in Sulfate

**Problem:** Find the oxidation number of sulfur in $\ce{SO4^2-}$.

**Solution:**

**Step 1:** Oxygen $= -2$; four of them give $-8$.

**Step 2:** Sum must equal the ion charge, $-2$: $\;x + (-8) = -2$.

**Step 3:** $x = +6$.

**Answer:** $\ce{S} = +6$.

### Example 5: Same Element, Wildly Different States — Carbon

**Problem:** Find carbon's oxidation number in (a) $\ce{CO2}$ and (b) $\ce{CH4}$.

**Solution:**

**(a)** In $\ce{CO2}$: oxygen is $-2 \times 2 = -4$; neutral molecule sums to $0$, so $\ce{C} = +4$.

**(b)** In $\ce{CH4}$: hydrogen bonded to a nonmetal is $+1$, and $4 \times (+1) = +4$; neutral molecule sums to $0$, so $\ce{C} = -4$.

**Answer:** $\ce{C} = +4$ in $\ce{CO2}$ but $\ce{C} = -4$ in $\ce{CH4}$. Same element, an 8-unit swing — this is exactly why burning $\ce{CH4}$ into $\ce{CO2}$ (combustion) is such a dramatic oxidation of carbon.

### Example 6: The Tricky One — Manganese in Permanganate

**Problem:** Find manganese's oxidation number in $\ce{MnO4-}$.

**Solution:**

**Step 1:** Oxygen $= -2$; four oxygens give $-8$.

**Step 2:** Ion charge is $-1$, so the sum must be $-1$: $\;x + (-8) = -1$.

**Step 3:** $x = +7$.

**Answer:** $\ce{Mn} = +7$ — its maximum possible state. Permanganate is a famously powerful oxidizing agent (that intense purple color you may have seen in labs).

### Example 7: An Exception Case — Peroxide

**Problem:** Find oxygen's oxidation number in hydrogen peroxide, $\ce{H2O2}$.

**Solution:**

**Step 1:** Hydrogen is $+1$ (bonded to a nonmetal); two of them give $+2$.

**Step 2:** Neutral molecule sums to $0$. Two oxygens: $2 + 2y = 0 \Rightarrow y = -1$.

**Answer:** $\ce{O} = -1$. This is the peroxide exception in action — *don't* reflexively write $-2$ for oxygen. (Check: had you forced $-2$, the sum would be $+2 - 4 = -2 \ne 0$, an immediate red flag.)

### Example 8: Is This Reaction Redox? — Yes

**Problem:** Determine whether $\ce{Zn + 2HCl -> ZnCl2 + H2}$ is a redox reaction. If so, identify what's oxidized and what's reduced.

**Solution:**

**Step 1:** Assign oxidation numbers on both sides.

| Atom | Reactant side | Product side |
|---|---|---|
| $\ce{Zn}$ | $0$ (element) | $+2$ (in $\ce{ZnCl2}$) |
| $\ce{H}$ | $+1$ (in $\ce{HCl}$) | $0$ (in $\ce{H2}$) |
| $\ce{Cl}$ | $-1$ | $-1$ (unchanged) |

**Step 2:** Two atoms changed: $\ce{Zn}$ went $0 \to +2$ (lost electrons → **oxidized**, OIL); $\ce{H}$ went $+1 \to 0$ (gained electrons → **reduced**, RIG). Chlorine never changed — it's a **spectator**.

**Answer:** **Yes, it's redox.** Zinc is oxidized; hydrogen is reduced.

### Example 9: Is This Reaction Redox? — No

**Problem:** Determine whether $\ce{AgNO3 + NaCl -> AgCl + NaNO3}$ is a redox reaction.

**Solution:**

**Step 1:** Check every element's oxidation number. $\ce{Ag}=+1$ on both sides; $\ce{Na}=+1$ on both sides; $\ce{Cl}=-1$ on both sides; nitrate ($\ce{NO3-}$) travels intact, so $\ce{N}=+5$ and $\ce{O}=-2$ throughout.

**Step 2:** *Nothing* changed oxidation number — the ions just swapped partners.

**Answer:** **Not redox.** This is a double-replacement / precipitation reaction. Key takeaway: **no oxidation-number change → not redox**, no matter how dramatic the precipitate.

### Example 10: Naming Both Agents

**Problem:** In $\ce{2Al + 3Cl2 -> 2AlCl3}$, identify the substance oxidized, the substance reduced, the oxidizing agent, and the reducing agent.

**Solution:**

**Step 1:** Oxidation numbers: $\ce{Al}$ goes $0 \to +3$ (loses electrons → **oxidized**). $\ce{Cl}$ goes $0 \to -1$ (gains electrons → **reduced**).

**Step 2:** Map to agents. Aluminum is oxidized, so aluminum is the **reducing agent** (the electron donor). Chlorine is reduced, so chlorine is the **oxidizing agent** (the electron thief).

**Answer:** Oxidized: $\ce{Al}$. Reduced: $\ce{Cl2}$. **Reducing agent: $\ce{Al}$. Oxidizing agent: $\ce{Cl2}$.** (Remember: each agent is named for what it does to its partner and undergoes the *opposite* itself.)

### Example 11: Writing and Combining Half-Reactions

**Problem:** For $\ce{Al + Cu^2+ -> Al^3+ + Cu}$, write the two half-reactions, balance the electrons, and give the balanced net equation.

**Solution:**

**Step 1 — split:**

- Oxidation: $\ce{Al -> Al^3+ + 3e-}$ (aluminum loses 3 electrons, $0 \to +3$)
- Reduction: $\ce{Cu^2+ + 2e- -> Cu}$ (copper gains 2 electrons, $+2 \to 0$)

**Step 2 — make electrons equal.** Lost = 3, gained = 2. The least common multiple is 6. Multiply the oxidation half by 2 and the reduction half by 3:

- $\ce{2Al -> 2Al^3+ + 6e-}$
- $\ce{3Cu^2+ + 6e- -> 3Cu}$

**Step 3 — add and cancel the 6 electrons:**

$$\ce{2Al + 3Cu^2+ -> 2Al^3+ + 3Cu}$$

**Answer:** $\ce{2Al + 3Cu^2+ -> 2Al^3+ + 3Cu}$. Check charge: left $= 3(+2) = +6$; right $= 2(+3) = +6$. Balanced in both mass and charge.

### Example 12: Full Acidic-Solution Half-Reaction

**Problem:** Balance the reduction half-reaction for permanganate becoming $\ce{Mn^2+}$ in acidic solution: $\ce{MnO4- -> Mn^2+}$.

**Solution:** Use the four-step acidic recipe.

**Step 1 — balance the main element.** Mn is already 1-to-1.

**Step 2 — balance O with water.** Left has 4 O, right has 0. Add 4 $\ce{H2O}$ to the right: $\ce{MnO4- -> Mn^2+ + 4H2O}$.

**Step 3 — balance H with $\ce{H+}$.** Right now has $4 \times 2 = 8$ H. Add 8 $\ce{H+}$ to the left: $\ce{MnO4- + 8H+ -> Mn^2+ + 4H2O}$.

**Step 4 — balance charge with electrons.** Left charge: $(-1) + 8(+1) = +7$. Right charge: $+2$. Add 5 $\ce{e-}$ to the *left* to drag $+7$ down to $+2$:

$$\ce{MnO4- + 8H+ + 5e- -> Mn^2+ + 4H2O}$$

**Answer:** $\ce{MnO4- + 8H+ + 5e- -> Mn^2+ + 4H2O}$. Manganese went $+7 \to +2$, gaining 5 electrons — consistent with the 5 electrons on the left. (To finish a *full* reaction, you'd pair this with an oxidation half scaled so electrons cancel — same principle as Example 11.)

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Saying the oxidizing agent is oxidized | The name *sounds* like it should be | The agent does the **opposite** to itself: oxidizing agent is **reduced**, reducing agent is **oxidized**. Oxygen (oxidizing agent) gets reduced |
| Naming only the changing *atom* as the agent | Focusing on the atom that moved | The agent is the **whole species**. In $\ce{Cu^2+ + ...}$, the oxidizing agent is $\ce{Cu^2+}$, not just "Cu" |
| Forcing oxygen to $-2$ always | Rule 4 feels absolute | Watch for **peroxides** ($\ce{H2O2}$, O is $-1$) and O–F bonds. Always confirm the sum works out |
| Forcing hydrogen to $+1$ always | Same over-generalizing | In **metal hydrides** ($\ce{NaH}$, $\ce{CaH2}$) hydrogen is $-1$ |
| Calling a precipitation or acid–base swap "redox" | It looks like a big reaction | **No oxidation-number change = not redox.** Check every element before deciding |
| Putting electrons on the wrong side | Rushing the half-reaction | Oxidation *loses* electrons → $\ce{e-}$ on the **right**. Reduction *gains* → $\ce{e-}$ on the **left** (OIL RIG) |
| Adding half-reactions without matching electrons | Skipping the scaling step | Scale each half to a **common multiple** of electrons first, so they cancel completely |
| Confusing "reduction" with getting smaller | The everyday meaning of the word | Reduction = the **charge** is reduced (more negative) as electrons are gained |

---

## AP Exam Tips

- **Memorize the oxidation-number rules cold.** They're not on the formula sheet. Drill the priority order (element $= 0$; ion $=$ charge; F $=-1$; O $=-2$ except peroxides/F; H $=+1$ except metal hydrides; sum $=$ overall charge) until assigning states is reflexive.
- **"Identify the oxidizing agent" is a near-guaranteed question — and the #1 trap.** The oxidizing agent is the species that gets **reduced**. If you can answer this correctly under pressure, you're ahead of most of the class. Write "OIL RIG" in the margin the moment the section starts.
- **Redox recognition = look for an oxidation-number change.** The fastest way to classify a reaction as redox is to assign states to a couple of suspicious atoms (free elements and transition metals are prime suspects) and check if any changed.
- **Half-reaction balancing must satisfy BOTH mass and charge.** Graders check that atoms balance *and* that electrons make the charges equal. Forgetting the electrons is an easy lost point.
- **Free elements are giveaways.** Any equation with a pure element ($\ce{O2}$, $\ce{Zn}$, $\ce{H2}$, $\ce{Cl2}$) on one side and that element combined on the other is almost certainly redox — its state changed from $0$.
- **This topic feeds Unit 9.** Everything here — half-reactions, agents, electron counting — becomes the machinery of galvanic cells, cell potential, and electrolysis. Solid footing now pays off enormously later.

---

## Practice Problems

### Problem 1
Assign the oxidation number of nitrogen in $\ce{NO3-}$.

<details>
<summary><strong>Solution</strong></summary>

Oxygen $= -2$, three of them $= -6$. Ion charge $= -1$, so $x + (-6) = -1 \Rightarrow x = +5$.

**Answer:** $\ce{N} = +5$.

</details>

### Problem 2
Assign the oxidation number of phosphorus in $\ce{PO4^3-}$.

<details>
<summary><strong>Solution</strong></summary>

Oxygen $= -2 \times 4 = -8$. Sum must equal $-3$: $x - 8 = -3 \Rightarrow x = +5$.

**Answer:** $\ce{P} = +5$.

</details>

### Problem 3
Assign the oxidation number of chlorine in $\ce{ClO3-}$ (chlorate).

<details>
<summary><strong>Solution</strong></summary>

Oxygen $= -6$ total. Ion charge $-1$: $x - 6 = -1 \Rightarrow x = +5$.

**Answer:** $\ce{Cl} = +5$. (Chlorine's oxidation number is very flexible — it ranges from $-1$ to $+7$.)

</details>

### Problem 4
Assign the oxidation number of hydrogen in calcium hydride, $\ce{CaH2}$.

<details>
<summary><strong>Solution</strong></summary>

$\ce{Ca}$ is a group-2 metal, so $+2$. This is a **metal hydride** — the exception — so hydrogen is $-1$. Check: $+2 + 2(-1) = 0$ ✓.

**Answer:** $\ce{H} = -1$.

</details>

### Problem 5
Assign the oxidation number of sulfur in $\ce{S2O3^2-}$ (thiosulfate).

<details>
<summary><strong>Solution</strong></summary>

Oxygen $= -2 \times 3 = -6$. Ion charge $-2$, and there are 2 sulfurs: $2x - 6 = -2 \Rightarrow 2x = +4 \Rightarrow x = +2$.

**Answer:** average $\ce{S} = +2$. (Oxidation number can be a non-integer average when identical atoms sit in different environments — perfectly fine for AP.)

</details>

### Problem 6
Is $\ce{2H2 + O2 -> 2H2O}$ a redox reaction? Identify the oxidizing and reducing agents.

<details>
<summary><strong>Solution</strong></summary>

$\ce{H}$: $0 \to +1$ (oxidized, loses electrons). $\ce{O}$: $0 \to -2$ (reduced, gains electrons). Both changed → redox.

Hydrogen is oxidized → $\ce{H2}$ is the **reducing agent**. Oxygen is reduced → $\ce{O2}$ is the **oxidizing agent**.

**Answer:** Yes, redox. Reducing agent $\ce{H2}$; oxidizing agent $\ce{O2}$.

</details>

### Problem 7
Is $\ce{HCl + NaOH -> NaCl + H2O}$ a redox reaction? Explain.

<details>
<summary><strong>Solution</strong></summary>

Check states: $\ce{H}=+1$, $\ce{Cl}=-1$, $\ce{Na}=+1$, $\ce{O}=-2$ — every atom keeps its oxidation number from reactants to products.

**Answer:** **Not redox.** It's an acid–base neutralization; no electrons are transferred.

</details>

### Problem 8
In the rusting reaction $\ce{4Fe + 3O2 -> 2Fe2O3}$, identify what is oxidized, what is reduced, and both agents.

<details>
<summary><strong>Solution</strong></summary>

$\ce{Fe}$: $0 \to +3$ (oxidized). $\ce{O}$: $0 \to -2$ (reduced).

Iron oxidized → iron is the **reducing agent**. Oxygen reduced → oxygen is the **oxidizing agent** (the same electron-thief role it plays on the apple).

**Answer:** Oxidized: $\ce{Fe}$; reduced: $\ce{O2}$. Reducing agent $\ce{Fe}$; oxidizing agent $\ce{O2}$.

</details>

### Problem 9
Write the oxidation and reduction half-reactions for $\ce{Mg + 2H+ -> Mg^2+ + H2}$.

<details>
<summary><strong>Solution</strong></summary>

Magnesium $0 \to +2$ (oxidation, loses 2 e⁻); hydrogen $+1 \to 0$ (reduction, gains electrons).

Oxidation: $\ce{Mg -> Mg^2+ + 2e-}$

Reduction: $\ce{2H+ + 2e- -> H2}$

**Answer:** as above; electrons lost (2) = electrons gained (2), so the halves add directly back to the given equation.

</details>

### Problem 10
Balance the oxidation half-reaction $\ce{Fe^2+ -> Fe^3+}$ for charge (add electrons).

<details>
<summary><strong>Solution</strong></summary>

Mass is already balanced (one Fe each side). Charge: left $+2$, right $+3$. Iron loses 1 electron, so the electron goes on the **right** (oxidation):

$$\ce{Fe^2+ -> Fe^3+ + e-}$$

Check charge: left $+2$; right $+3 + (-1) = +2$ ✓.

**Answer:** $\ce{Fe^2+ -> Fe^3+ + e-}$.

</details>

### Problem 11
Combine the half-reactions $\ce{Fe^2+ -> Fe^3+ + e-}$ and $\ce{Cl2 + 2e- -> 2Cl-}$ into a balanced overall equation.

<details>
<summary><strong>Solution</strong></summary>

Electrons: oxidation gives 1, reduction takes 2. LCM is 2 — double the oxidation half:

$$\ce{2Fe^2+ -> 2Fe^3+ + 2e-}$$

Add to $\ce{Cl2 + 2e- -> 2Cl-}$ and cancel the 2 electrons:

$$\ce{2Fe^2+ + Cl2 -> 2Fe^3+ + 2Cl-}$$

Check charge: left $2(+2) + 0 = +4$; right $2(+3) + 2(-1) = +4$ ✓.

**Answer:** $\ce{2Fe^2+ + Cl2 -> 2Fe^3+ + 2Cl-}$.

</details>

### Problem 12
The apple-browning story in miniature: an antioxidant molecule $\ce{A}$ donates electrons to oxygen so the apple stays white. In redox language, is $\ce{A}$ oxidized or reduced, and is it acting as an oxidizing or reducing agent?

<details>
<summary><strong>Solution</strong></summary>

$\ce{A}$ **donates** (loses) electrons → it is **oxidized** (OIL). Because it gives electrons to reduce the oxygen, it is a **reducing agent** — specifically a sacrificial one, taking the hit so the apple doesn't.

**Answer:** $\ce{A}$ is oxidized and acts as a (sacrificial) reducing agent. This is exactly vitamin C protecting your apple.

</details>

### Problem 13
Determine the oxidation number of carbon in each and rank from most reduced to most oxidized: $\ce{CH4}$, $\ce{CO}$, $\ce{CO2}$.

<details>
<summary><strong>Solution</strong></summary>

$\ce{CH4}$: H is $+1 \times 4 = +4$, so $\ce{C} = -4$.
$\ce{CO}$: O is $-2$, so $\ce{C} = +2$.
$\ce{CO2}$: O is $-4$ total, so $\ce{C} = +4$.

Most reduced (lowest state) → most oxidized (highest state):

**Answer:** $\ce{CH4}\,(-4) < \ce{CO}\,(+2) < \ce{CO2}\,(+4)$. Burning fuel marches carbon up this ladder.

</details>

### Problem 14
A student claims $\ce{Cl2 + 2KBr -> 2KCl + Br2}$ is redox and names $\ce{K}$ as the element oxidized. Are they right? Correct any error.

<details>
<summary><strong>Solution</strong></summary>

Check states. $\ce{K}$: $+1 \to +1$ (unchanged — spectator!). $\ce{Cl}$: $0 \to -1$ (reduced). $\ce{Br}$: $-1 \to 0$ (oxidized).

The reaction *is* redox, but potassium doesn't change. **Bromine** is oxidized (loses electrons); **chlorine** is reduced.

**Answer:** Redox: yes. But $\ce{Br}$ is oxidized (not K), and $\ce{Cl2}$ is reduced. $\ce{Cl2}$ is the oxidizing agent; $\ce{KBr}$ (via bromide) is the reducing agent.

</details>

### Problem 15
Balance the thermite reaction and identify both agents: $\ce{Al + Fe2O3 -> Al2O3 + Fe}$.

<details>
<summary><strong>Solution</strong></summary>

Balance: oxygen matches at 3, so $\ce{Al2O3}$ needs 2 Al → $\ce{2Al}$, and $\ce{Fe2O3}$ gives 2 Fe → $\ce{2Fe}$:

$$\ce{2Al + Fe2O3 -> Al2O3 + 2Fe}$$

States: $\ce{Al}$ $0 \to +3$ (oxidized → reducing agent). $\ce{Fe}$ $+3 \to 0$ (reduced). So $\ce{Fe2O3}$ is the **oxidizing agent** and $\ce{Al}$ is the **reducing agent**.

**Answer:** $\ce{2Al + Fe2O3 -> Al2O3 + 2Fe}$; oxidizing agent $\ce{Fe2O3}$, reducing agent $\ce{Al}$. (Aluminum's hunger for oxygen is what makes thermite melt iron.)

</details>

---

## Quick Reference

**The core idea:** redox = electron transfer. Oxidation and reduction always happen **together**.

$$\textbf{OIL RIG} \;:\; \text{Oxidation Is Loss}, \quad \text{Reduction Is Gain (of electrons)}$$

**Oxidation-number rules (apply in order; higher rule wins):**

| # | Rule |
|---|---|
| 1 | Pure element $= 0$ (including $\ce{O2}$, $\ce{Cl2}$, $\ce{P4}$) |
| 2 | Monatomic ion $=$ its charge |
| 3 | Fluorine $= -1$ always |
| 4 | Oxygen $= -2$ (peroxides $-1$; with F, positive) |
| 5 | Hydrogen $= +1$ (metal hydrides $-1$) |
| 6 | Sum $= 0$ (neutral) or $=$ charge (ion) |

**Agents (the confusing part):**

| Species | Does what to itself | Role |
|---|---|---|
| Loses electrons | **oxidized** | **reducing agent** (electron donor) |
| Gains electrons | **reduced** | **oxidizing agent** (electron thief) |

*The agent undergoes the opposite of its name.* Oxidizing agent → gets reduced.

**Half-reactions:**
- Oxidation: electrons on the **right** ($\ce{Zn -> Zn^2+ + 2e-}$)
- Reduction: electrons on the **left** ($\ce{Cu^2+ + 2e- -> Cu}$)
- Balance mass **and** charge; scale so **electrons lost = electrons gained**, then add.

**Is it redox?** → Did any oxidation number **change**? If no change, it's not redox.

**Always-redox families:** combustion, single replacement, corrosion/rusting, combination of elements. **Next stop:** Unit 9 — batteries are redox with the electrons routed through a wire.

---

<div align="center">

[← Acid-Base Reactions](/chemistry/0605-acid-base-reactions)

</div>
