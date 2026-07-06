# Acid Strength and Molecular Structure
<p class="article-date">July 5, 2026</p>

*Last Sunday I lost a genuine fight with a jar of pickles. My mom walked over, gave the lid one lazy flick, and it popped right off — I'd been straining like it owed me money. That got me thinking about the drawer of jars in our fridge: some lids come off with a flick, some need a towel for grip, and there's one ancient jar of achaar that I'm pretty sure is welded shut for life. Same shape, same threads, wildly different grip. Acids are exactly this story, and the story is about one thing: how easily the molecule lets go of its $\ce{H+}$. A "strong" acid has a loose lid — the proton comes off effortlessly. A "weak" acid grips it tight. And here's the part nobody tells you up front: what decides the grip isn't luck, it's **structure** — how the bond to that $\ce{H}$ is built, and how comfortable the leftover jar is once the lid is gone. This is Topic 8.5, and it's where all the equilibrium machinery from the last article finally gets a "why": we stop memorizing which acids are strong and start predicting it from a Lewis structure.*

---

## What You'll Learn
- State the master principle: **acid strength = how easily $\ce{H+}$ leaves = how stable the conjugate base is** once it's gone
- Explain a binary acid trend **down a group** using bond strength and atomic size ($\ce{HF} < \ce{HCl} < \ce{HBr} < \ce{HI}$)
- Explain a binary acid trend **across a period** using electronegativity ($\ce{CH4} < \ce{NH3} < \ce{H2O} < \ce{HF}$)
- Rank oxyacids by **number of oxygens** ($\ce{HClO} < \ce{HClO2} < \ce{HClO3} < \ce{HClO4}$) and by **central-atom electronegativity** ($\ce{HClO} > \ce{HBrO} > \ce{HIO}$)
- Predict the effect of **electron-withdrawing groups** on carboxylic acid strength (trichloroacetic vs. acetic acid)
- Use **resonance / charge delocalization** to explain why carboxylate and oxyacid anions are extra stable
- Rank a set of acids by relative $K_a$ using structure alone, and write the AP-credit justification through **conjugate-base stability**
- Apply the same logic in reverse to compare **base strength** through conjugate-acid stability

---

## Prerequisites
- [Weak Acids and Bases](/chemistry/1002-weak-acids-and-bases) — you need $K_a$ as the number that measures acid strength, and the idea of a **conjugate base** as "what's left after $\ce{H+}$ leaves." This whole article explains *why* those $K_a$ values come out the way they do
- [Periodic Trends](/chemistry/0305-periodic-trends) — the two levers behind every trend here are **electronegativity** and **atomic size**, and we'll lean on the protons–distance–shielding checklist constantly
- [Bonds and Electronegativity](/chemistry/0401-bonds-and-electronegativity) — the $\ce{H-X}$ bond is a tug-of-war for electron density; whether the proton leaves cleanly depends on how that bond was built

---

## The Core Concept

### Intuition First

Back to the fridge drawer. Let's make the jars do real work, because every part of the analogy maps onto a real piece of the chemistry:

| Fridge drawer | Acid chemistry | What it controls |
|---|---|---|
| The **jar** | The **acid molecule** ($\ce{HA}$) | The thing holding the proton |
| The **lid** | The **$\ce{H+}$** being released | What comes off when the acid ionizes |
| **How easily the lid comes off** | **Acid strength** ($K_a$) | Loose lid = strong acid; welded lid = weak acid |
| A lid that **stays off comfortably** | A **stable conjugate base** ($\ce{A-}$) | The more content the leftover jar is, the more it *wanted* to lose the lid |

Here's the one sentence this entire topic hangs on:

> **An acid is strong when the conjugate base it leaves behind is stable.**

Think about *why* that has to be true. Ionizing an acid means ripping off the lid: $\ce{HA -> H+ + A-}$. That leftover piece $\ce{A-}$ carries a negative charge — it just inherited the electrons that used to be in the bond. If $\ce{A-}$ is a miserable, cramped, high-energy species that hates holding that negative charge, then the reaction doesn't want to happen — the lid stays on, and the acid is **weak**. But if $\ce{A-}$ is relaxed and stable — the negative charge sitting comfortably, spread out, well cared for — then the molecule is *happy* to let the proton go, the equilibrium runs forward, and the acid is **strong**.

So the trick to every single problem in this article is to stop staring at the acid and instead ask:

> **"How stable is the anion after the $\ce{H}$ leaves?"**

Everything else — bond strength, electronegativity, oxygen count, chlorine atoms hanging off the side — is just a different way that structure makes the conjugate base more or less comfortable. Answer the anion-stability question and you've answered the strength question.

### The stability question, in energy terms

Acid strength is really a statement about equilibrium position, which is a statement about energy:

$$\ce{HA(aq) <=> H+(aq) + A^-(aq)} \qquad K_a = \frac{[\ce{H+}][\ce{A-}]}{[\ce{HA}]}$$

A **large $K_a$** (strong acid) means the products — including that conjugate base $\ce{A-}$ — sit at *low* energy. Anything structural that lowers the energy of $\ce{A-}$ pushes $K_a$ up. There are only a few ways structure can do that, and this article is a tour of all of them:

1. **Weaker bond to $\ce{H}$** → easier to break → proton leaves more readily (dominates *down a group*).
2. **More electronegative atom holding the charge** → the negative charge is held by an atom that actually *likes* electrons (dominates *across a period*, and drives oxyacids).
3. **Spreading the charge out** — over more electronegative oxygens, or by **resonance/delocalization**, or by pulling it toward nearby electron-hungry atoms (**inductive effect**). A spread-out charge is a comfortable charge.

Keep those three in your pocket. Now let's watch them fight.

### Two families of acids

Almost every acid the AP exam throws at you is one of two structural types:

- **Binary acids**, $\ce{H-X}$: hydrogen bonded straight to one other element (the hydrogen halides $\ce{HF}$, $\ce{HCl}$, $\ce{HBr}$, $\ce{HI}$, plus things like $\ce{H2S}$).
- **Oxyacids**, $\ce{H-O-Y}$: the acidic hydrogen is bonded to an **oxygen**, which is bonded to some central atom $\ce{Y}$ (like $\ce{HClO4}$, $\ce{HNO3}$, $\ce{H2SO4}$). The proton never leaves from $\ce{Y}$ directly — it always leaves from an $\ce{O-H}$.

They follow different rules because the "loose lid" is built differently in each. Let's take them one at a time.

---

### Binary acids ($\ce{H-X}$): two competing levers

Binary acids have two things that can change as you move around the periodic table, and they pull in *opposite* directions. Knowing which one wins where is the whole game.

**Lever 1 — Bond strength (atomic size).** To lose the lid, you have to break the $\ce{H-X}$ bond. A weaker, longer bond breaks more easily. As you go **down a group**, $\ce{X}$ gets bigger, its valence orbital is farther out and more diffuse, and it overlaps poorly with hydrogen's tiny $1s$ orbital. So the $\ce{H-X}$ bond gets **longer and weaker** going down — and weaker bond = easier to release $\ce{H+}$ = **stronger acid**.

**Lever 2 — Electronegativity (charge stability).** Once the proton leaves, the electrons stay behind on $\ce{X}$, making $\ce{X-}$. A more electronegative $\ce{X}$ is happier holding that negative charge, so a more electronegative $\ce{X}$ gives a more stable conjugate base = **stronger acid**.

Now here's the beautiful part: these two levers dominate in *different directions*, so you use a different one depending on which way you're moving.

**DOWN a group → bond strength wins.** Electronegativity is changing only a little down a group, but bond strength is changing a *lot*. The bond gets dramatically weaker as $\ce{X}$ balloons in size, and that effect steamrolls everything else:

$$\underbrace{\ce{HF}}_{\text{strong bond, weak acid}} \;<\; \ce{HCl} \;<\; \ce{HBr} \;<\; \underbrace{\ce{HI}}_{\text{weak bond, strong acid}}$$

This is the trend that surprises everyone. Fluorine is the *most* electronegative atom in existence, so your gut screams "$\ce{HF}$ must be the strongest acid!" — and it's dead wrong. $\ce{HF}$ is a **weak acid** ($K_a \approx 7 \times 10^{-4}$) because the $\ce{H-F}$ bond is so short and strong that the lid is basically welded on. Meanwhile $\ce{HI}$, with its long floppy $\ce{H-I}$ bond, is one of the strongest acids there is. Down a group, **size and bond strength beat electronegativity.**

**ACROSS a period → electronegativity wins.** Now atomic size barely changes (same row, same shell), so the bond-strength lever goes quiet and electronegativity takes over. The more electronegative $\ce{X}$ is, the more stable $\ce{X-}$ is, the stronger the acid:

$$\underbrace{\ce{CH4}}_{\text{not acidic}} \;<\; \ce{NH3} \;<\; \ce{H2O} \;<\; \underbrace{\ce{HF}}_{\text{strongest of the row}}$$

Going left to right, $\ce{C < N < O < F}$ in electronegativity, so $\ce{CH3-}$, $\ce{NH2-}$, $\ce{OH-}$, $\ce{F-}$ get progressively more stable, and the acids get progressively stronger. $\ce{CH4}$ won't donate a proton to anything you'll meet in AP; $\ce{HF}$ genuinely will.

**The one-line summary you must own:**

> Binary acids: **DOWN a group, bond strength decides** (bigger atom → weaker bond → stronger acid). **ACROSS a period, electronegativity decides** (more electronegative → more stable $\ce{X-}$ → stronger acid).

---

### Oxyacids ($\ce{H-O-Y}$): pull the charge away and spread it out

In an oxyacid the proton always leaves from an $\ce{O-H}$ group, so the $\ce{O-H}$ bond strength is roughly similar across the whole family. What changes is what happens to the negative charge left on that oxygen after $\ce{H}$ departs. The whole trick is: **anything that pulls electron density away from the $\ce{O-H}$ oxygen and spreads the resulting negative charge out makes the conjugate base more stable and the acid stronger.** Two structural knobs do this.

**Knob 1 — Number of oxygens on the central atom.** Adding more oxygen atoms (especially terminal $\ce{O}$ with double bonds) does two things: each extra electronegative oxygen tugs electron density away from the $\ce{O-H}$, weakening that bond, and — more importantly — once the proton is gone, the negative charge can be **spread across all those oxygens by resonance** instead of being stuck on one. Charge spread over four oxygens is far more comfortable than charge crammed onto one. So **more oxygens = stronger acid:**

$$\underbrace{\ce{HClO}}_{K_a \sim 10^{-8}} \;<\; \underbrace{\ce{HClO2}}_{K_a \sim 10^{-2}} \;<\; \underbrace{\ce{HClO3}}_{\text{strong}} \;<\; \underbrace{\ce{HClO4}}_{\text{strongest known}}$$

That's a jump of roughly a *hundred-million-fold* in $K_a$ from $\ce{HClO}$ to $\ce{HClO4}$, just by hanging more oxygens on the same chlorine. $\ce{HClO4}$ (perchloric acid) is one of the strongest acids that exists, and its conjugate base $\ce{ClO4-}$ is a textbook picture of stability: the negative charge is smeared evenly across four equivalent oxygens.

**Knob 2 — Electronegativity of the central atom $\ce{Y}$.** Hold the number of oxygens fixed and swap the central atom. A more electronegative $\ce{Y}$ pulls electron density toward itself, which pulls it off the $\ce{O-H}$ oxygen, stabilizing the negative charge in the conjugate base. So for the same number of oxygens, **more electronegative central atom = stronger acid:**

$$\underbrace{\ce{HClO}}_{\ce{Cl}\text{ most EN}} \;>\; \ce{HBrO} \;>\; \underbrace{\ce{HIO}}_{\ce{I}\text{ least EN}}$$

Careful with the direction here — this looks backwards next to the binary trend, but it isn't. In binary $\ce{H-X}$ acids, going down the halogens *strengthens* the acid because bond strength rules. In oxyacids the proton leaves from $\ce{O-H}$ (not from $\ce{Y-H}$), so bond strength to $\ce{Y}$ is irrelevant; all that matters is how hard $\ce{Y}$ pulls the charge, so the more electronegative (higher) halogen wins. Different lever, because the proton leaves from a different place.

**The one-line summary:**

> Oxyacids: strength goes up with **more oxygens** on the central atom, and with a **more electronegative central atom**. Both work by pulling the negative charge off the $\ce{O-H}$ oxygen and spreading it out.

---

### Carboxylic acids and electron-withdrawing groups

Carboxylic acids ($\ce{-COOH}$) are the organic cousins of oxyacids, and they show the "spread the charge out" principle in its cleanest form. Take **acetic acid**, $\ce{CH3COOH}$ (the acid in vinegar), $K_a \approx 1.8 \times 10^{-5}$. Now replace the three hydrogens on that methyl group with three chlorines to make **trichloroacetic acid**, $\ce{CCl3COOH}$, $K_a \approx 0.2$ — that's roughly **ten thousand times stronger.**

Nothing changed near the $\ce{O-H}$ itself. So why the enormous jump? The three electronegative chlorine atoms, even though they're several bonds away, tug electron density toward themselves through the sigma bonds — this is the **inductive effect**. When the proton leaves and the conjugate base $\ce{CCl3COO-}$ forms, those chlorines pull some of the excess negative charge away from the carboxylate oxygens and spread it down the chain. A spread-out charge is a stable charge, so the conjugate base is far more comfortable, and the acid is far stronger. Acetic acid's plain $\ce{CH3-}$ group has no such pull — the charge has to sit entirely on the carboxylate, so its conjugate base is less stable and the acid is weaker.

> **The pattern:** nearby **electron-withdrawing atoms** (halogens, especially several of them, and especially close to the $\ce{-COOH}$) stabilize the conjugate base and strengthen the acid. More of them, or more electronegative ones, or closer ones → stronger acid.

### Resonance: why carboxylate and oxyacid anions are so comfortable

There's a deeper reason carboxylate and oxyacid conjugate bases are stable, and it's worth naming because AP loves it: **resonance delocalization** (see [Resonance and Formal Charge](/chemistry/0405-resonance-formal-charge)).

When acetic acid loses its proton, you might think the negative charge is stuck on one oxygen. It isn't. The carboxylate ion $\ce{CH3COO-}$ has **two equivalent resonance structures** — the double bond and the negative charge can sit on either oxygen — so in reality the charge is **smeared equally across both oxygens**, and both $\ce{C-O}$ bonds are identical, halfway between single and double.

$$\ce{CH3COO-} \;=\; \text{[charge on left O]} \;\longleftrightarrow\; \text{[charge on right O]}$$

That delocalization is exactly what "spreading the charge out" means at the electron level, and it's a big part of *why* carboxylic acids are meaningfully acidic while ordinary alcohols (like the $\ce{O-H}$ in ethanol) are basically not — an alkoxide $\ce{CH3CH2O-}$ has no resonance escape hatch, so its charge is stuck on one oxygen and it's a lousy conjugate base. Same idea powers $\ce{NO3-}$, $\ce{SO4^2-}$, and $\ce{ClO4-}$: the more equivalent atoms the charge can spread across by resonance, the more stable the anion, the stronger the parent acid.

### Base strength: the same story, read backwards

Everything above flips cleanly for bases. A base grabs a proton to form its **conjugate acid**, so:

> **A base is strong when its conjugate acid is stable — equivalently, a strong base is the conjugate of a very weak acid.**

This is just the conjugate seesaw from [Weak Acids and Bases](/chemistry/1002-weak-acids-and-bases): strong acid ⇒ weak conjugate base, and weak acid ⇒ strong conjugate base ($K_a \times K_b = K_w$). So $\ce{HI}$ being a strong acid tells you $\ce{I-}$ is a pathetically weak base — it has no interest in taking a proton back. And $\ce{HF}$ being weak tells you $\ce{F-}$ is a comparatively decent base. You never need a separate theory for bases: figure out how stable the anion is *as a conjugate base*, and you've simultaneously figured out how weak it is *as a base*. Stable anion = strong parent acid = weak base.

---

## Worked Examples

### Example 1: Rank the hydrogen halides (down a group)
**Problem:** Rank $\ce{HF}$, $\ce{HCl}$, $\ce{HBr}$, $\ce{HI}$ from weakest to strongest acid, and justify.

**Solution:**
- **Step 1 — Identify the move.** These are binary $\ce{H-X}$ acids and we're going *down* a group (F → I).
- **Step 2 — Pick the winning lever.** Down a group, **bond strength dominates.** As $\ce{X}$ gets larger, the $\ce{H-X}$ bond gets longer and weaker.
- **Step 3 — Weaker bond = easier to release $\ce{H+}$ = stronger acid.** So strength increases down the group.

**Answer:** $\ce{HF} < \ce{HCl} < \ce{HBr} < \ce{HI}$. Don't be fooled by fluorine's high electronegativity — down a group, the weak $\ce{H-I}$ bond makes $\ce{HI}$ the strongest.

### Example 2: Rank across a period
**Problem:** Rank $\ce{CH4}$, $\ce{NH3}$, $\ce{H2O}$, $\ce{HF}$ by acid strength and justify through the conjugate base.

**Solution:**
- **Step 1 — The move.** Same row of the periodic table (C, N, O, F), so we're going *across a period*.
- **Step 2 — Winning lever.** Across a period, atomic size barely changes, so **electronegativity dominates.** Order: $\ce{C} < \ce{N} < \ce{O} < \ce{F}$.
- **Step 3 — Conjugate-base stability.** After $\ce{H+}$ leaves, the charge sits on the central atom: $\ce{CH3-}$, $\ce{NH2-}$, $\ce{OH-}$, $\ce{F-}$. The more electronegative the atom, the more stable that anion.

**Answer:** $\ce{CH4} < \ce{NH3} < \ce{H2O} < \ce{HF}$. $\ce{F-}$ is the most stable conjugate base, so $\ce{HF}$ is the strongest.

### Example 3: The "reconcile the two trends" trap
**Problem:** In Example 1 you said $\ce{HF}$ is the *weakest* halogen acid, but fluorine is the *most* electronegative atom. Why doesn't electronegativity win here?

**Solution:**
- Both levers exist for $\ce{HF}$ vs. $\ce{HI}$: electronegativity *favors* $\ce{HF}$ being stronger, but bond strength *favors* $\ce{HI}$ being stronger.
- Going down a group, atomic size changes enormously, so the bond-strength effect is huge; electronegativity changes comparatively little. The large effect wins.
- Across a period the sizes are similar, bond-strength differences shrink, and electronegativity is left as the deciding factor.

**Answer:** Both trends are real; they just dominate in different directions. **Down a group → bond strength. Across a period → electronegativity.** For $\ce{HF}$ vs. $\ce{HI}$ we're going down, so bond strength wins and $\ce{HF}$ is weaker.

### Example 4: Oxyacids — count the oxygens
**Problem:** Rank $\ce{HClO}$, $\ce{HClO2}$, $\ce{HClO3}$, $\ce{HClO4}$ by acid strength.

**Solution:**
- **Step 1 — Same central atom** ($\ce{Cl}$), so the electronegativity knob is fixed; only the **number of oxygens** changes.
- **Step 2 — More oxygens** pull more electron density off the $\ce{O-H}$ and, after ionization, let the negative charge delocalize over more oxygens by resonance.
- **Step 3 — More spread-out charge = more stable conjugate base = stronger acid.**

**Answer:** $\ce{HClO} < \ce{HClO2} < \ce{HClO3} < \ce{HClO4}$. Perchloric acid ($\ce{HClO4}$) is the strongest: its conjugate base $\ce{ClO4-}$ spreads the charge over four equivalent oxygens.

### Example 5: Oxyacids — vary the central atom
**Problem:** Rank $\ce{HClO}$, $\ce{HBrO}$, $\ce{HIO}$ by acid strength and justify.

**Solution:**
- **Step 1 — Same number of oxygens** (one each), so the oxygen-count knob is fixed; only the **central atom $\ce{Y}$** changes.
- **Step 2 — Electronegativity of $\ce{Y}$:** $\ce{Cl} > \ce{Br} > \ce{I}$.
- **Step 3 — A more electronegative $\ce{Y}$** pulls charge off the $\ce{O-H}$ oxygen, stabilizing the conjugate base ($\ce{ClO-} > \ce{BrO-} > \ce{IO-}$ in stability).

**Answer:** $\ce{HClO} > \ce{HBrO} > \ce{HIO}$. Note this goes the *opposite* direction from binary $\ce{HX}$ acids — because here the proton leaves from $\ce{O-H}$, so central-atom electronegativity (not $\ce{Y-H}$ bond strength) is the deciding factor.

### Example 6: Mixed oxyacid ranking
**Problem:** Rank $\ce{H2SO4}$, $\ce{H2SO3}$, $\ce{HClO4}$ and give the reasoning.

**Solution:**
- $\ce{H2SO3}$ vs. $\ce{H2SO4}$: same central atom ($\ce{S}$), and $\ce{H2SO4}$ has **more oxygens** → stronger. So $\ce{H2SO3} < \ce{H2SO4}$.
- $\ce{HClO4}$ vs. $\ce{H2SO4}$: both have four oxygens per central atom, but $\ce{Cl}$ is **more electronegative** than $\ce{S}$ → $\ce{HClO4}$ is stronger.

**Answer:** $\ce{H2SO3} < \ce{H2SO4} < \ce{HClO4}$. (Oxygen count first, then central-atom electronegativity as the tiebreaker.)

### Example 7: Electron-withdrawing groups
**Problem:** Which is the stronger acid, acetic acid $\ce{CH3COOH}$ or trichloroacetic acid $\ce{CCl3COOH}$? Justify through conjugate-base stability.

**Solution:**
- **Step 1 — Same acidic group** ($\ce{-COOH}$); the difference is $\ce{CH3-}$ vs. $\ce{CCl3-}$.
- **Step 2 — The three electronegative $\ce{Cl}$ atoms** withdraw electron density through the bonds (inductive effect).
- **Step 3 — In the conjugate base** $\ce{CCl3COO-}$, those chlorines pull the negative charge away from the carboxylate and spread it out, stabilizing the anion; $\ce{CH3COO-}$ has no such help.

**Answer:** **Trichloroacetic acid is much stronger** (about $10^4\times$). Electron-withdrawing groups stabilize the conjugate base, which strengthens the acid.

### Example 8: How many electron-withdrawing atoms?
**Problem:** Rank acetic acid $\ce{CH3COOH}$, chloroacetic acid $\ce{CH2ClCOOH}$, and trichloroacetic acid $\ce{CCl3COOH}$.

**Solution:**
- More electronegative atoms withdrawing charge → more stable conjugate base → stronger acid.
- Number of $\ce{Cl}$ atoms: $0 < 1 < 3$.

**Answer:** $\ce{CH3COOH} < \ce{CH2ClCOOH} < \ce{CCl3COOH}$. Each added chlorine spreads the anion's charge a bit more, so each step up is a stronger acid.

### Example 9: Fluorine vs. chlorine on the chain
**Problem:** Which is the stronger acid, fluoroacetic acid $\ce{CH2FCOOH}$ or chloroacetic acid $\ce{CH2ClCOOH}$?

**Solution:**
- Same structure, one electron-withdrawing atom each; the difference is $\ce{F}$ vs. $\ce{Cl}$.
- $\ce{F}$ is **more electronegative** than $\ce{Cl}$, so it withdraws more strongly and stabilizes the conjugate base more.

**Answer:** $\ce{CH2FCOOH}$ is the stronger acid. More electronegative withdrawing group = more anion stabilization = stronger acid.

### Example 10: Resonance vs. no resonance
**Problem:** Acetic acid $\ce{CH3COOH}$ ($K_a \approx 1.8\times10^{-5}$) is far more acidic than ethanol $\ce{CH3CH2OH}$ ($K_a \approx 10^{-16}$), even though both donate an $\ce{O-H}$ proton. Why?

**Solution:**
- **Step 1 — Compare the conjugate bases.** Acetic acid gives carboxylate $\ce{CH3COO-}$; ethanol gives alkoxide $\ce{CH3CH2O-}$.
- **Step 2 — Resonance.** Carboxylate has two equivalent resonance forms, so the charge is delocalized over **two** oxygens. Alkoxide has no resonance — the charge is stuck on **one** oxygen.
- **Step 3 — Delocalized charge = far more stable anion.**

**Answer:** The carboxylate conjugate base is resonance-stabilized (charge spread over two oxygens); the alkoxide isn't. A more stable conjugate base means acetic acid is the vastly stronger acid.

### Example 11: Predict relative $K_a$ from structure alone
**Problem:** Without any tables, which has the larger $K_a$: $\ce{HNO3}$ or $\ce{HNO2}$? Justify.

**Solution:**
- Same central atom ($\ce{N}$); $\ce{HNO3}$ has three oxygens, $\ce{HNO2}$ has two.
- More oxygens → charge in the conjugate base ($\ce{NO3-}$ spreads over three O; $\ce{NO2-}$ over two) is more delocalized → more stable.

**Answer:** $\ce{HNO3}$ has the larger $K_a$ (it's a strong acid; $\ce{HNO2}$ is weak). More oxygens, more resonance stabilization, stronger acid.

### Example 12: Base strength by conjugate-acid logic
**Problem:** Which is the stronger base, $\ce{F-}$ or $\ce{I-}$?

**Solution:**
- **Step 1 — Look at the conjugate acids.** $\ce{F-}$ comes from $\ce{HF}$ (weak acid); $\ce{I-}$ comes from $\ce{HI}$ (strong acid).
- **Step 2 — Apply the seesaw.** The weaker the acid, the stronger its conjugate base.
- **Step 3 — $\ce{HF}$ is weaker than $\ce{HI}$**, so $\ce{F-}$ is the stronger base.

**Answer:** $\ce{F-}$ is the stronger base. (Equivalently: $\ce{I-}$ is an extremely stable, comfortable anion — that same stability makes $\ce{HI}$ a strong acid *and* makes $\ce{I-}$ a weak base.)

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| "$\ce{HF}$ must be the strongest halogen acid — fluorine is most electronegative!" | Reaching for electronegativity everywhere | Down a group, **bond strength wins**. $\ce{HF}$ is weak because the $\ce{H-F}$ bond is short and strong |
| Using bond strength across a period, or electronegativity down a group | Not tracking *which direction* you're moving | Down = bond strength; across = electronegativity. Say the direction out loud first |
| Thinking the oxyacid proton leaves from the central atom $\ce{Y}$ | The formula $\ce{HClO4}$ hides the structure | It's $\ce{H-O-Y}$; the proton **always** leaves an $\ce{O-H}$. That's why bond strength to $\ce{Y}$ doesn't matter |
| Getting the $\ce{HClO} > \ce{HBrO} > \ce{HIO}$ direction backwards | Confusing it with the binary $\ce{HX}$ trend | Different leaving spot: here it's $\ce{O-H}$, so **more electronegative central atom = stronger**, which is the higher (not lower) halogen |
| Justifying strength by "the bond is polar" or "it has lots of $\ce{H}$" | Guessing at plausible-sounding reasons | AP wants **conjugate-base stability**. Always end with "...so the conjugate base is more/less stable" |
| Forgetting resonance when comparing carboxylic acids to alcohols | Both have $\ce{O-H}$, so they look similar | Ask: can the anion delocalize by resonance? Carboxylate yes, alkoxide no |
| Treating base strength as a brand-new topic | Feels separate from acids | It's the same anion-stability question read backwards: stable anion = strong acid = weak base |

---

## AP Exam Tips

- **The phrase that earns points is "conjugate-base stability."** Free-response graders look for a justification that ends at the anion. "$\ce{HClO4}$ is a stronger acid than $\ce{HClO}$ **because its conjugate base $\ce{ClO4-}$ is more stable** — the negative charge is delocalized over more electronegative oxygen atoms." That sentence structure scores.
- **State the direction, then the lever.** For binary acids write it explicitly: "**down a group, bond strength decides**; **across a period, electronegativity decides**." Naming the correct lever is often the point being awarded.
- **Oxyacids = oxygen count + central-atom electronegativity.** More oxygens → stronger; more electronegative central atom → stronger. Both because the negative charge gets pulled off the $\ce{O-H}$ and spread out.
- **Use the "spreads/stabilizes the negative charge" language.** Phrases like "more electronegative atoms **withdraw electron density**," "the charge is **delocalized** by resonance," and "the negative charge is **stabilized/spread out**" are exactly the wording rubrics reward.
- **This topic is qualitative.** The AP exam almost never gives you $K_a$ values to memorize for these comparisons — it tests whether you can *reason* from structure. Don't try to memorize numbers; master the levers.
- **Watch for the $\ce{HF}$ trap.** It's the single most common "gotcha" — a strong-electronegativity atom in a *weak* acid. If you see fluorine and think "strong acid," slow down and check whether you're moving down a group.
- **Bases: convert to the conjugate acid.** If asked to rank bases, rank the conjugate acids' strengths and flip. It's faster and less error-prone than reasoning about the base directly.

---

## Practice Problems

### Problem 1
Rank $\ce{H2O}$, $\ce{H2S}$, $\ce{H2Se}$ from weakest to strongest acid, and state which lever you used.

<details>
<summary><strong>Solution</strong></summary>

These are binary acids and we're going **down** group 16 (O → S → Se). Down a group, **bond strength** dominates: the $\ce{H-X}$ bond gets longer and weaker, so the proton leaves more easily.

**Answer:** $\ce{H2O} < \ce{H2S} < \ce{H2Se}$ (strength increases down the group because of decreasing bond strength).

</details>

### Problem 2
$\ce{NH3}$ and $\ce{HF}$ are in the same period. Which is the stronger acid, and why (through the conjugate base)?

<details>
<summary><strong>Solution</strong></summary>

Across a period, **electronegativity** decides. $\ce{F}$ is more electronegative than $\ce{N}$, so the conjugate base $\ce{F-}$ is more stable than $\ce{NH2-}$.

**Answer:** $\ce{HF}$ is stronger, because its conjugate base $\ce{F-}$ is more stable (the charge sits on a more electronegative atom).

</details>

### Problem 3
Explain in one or two sentences why $\ce{HI}$ is a stronger acid than $\ce{HCl}$, even though chlorine is more electronegative than iodine.

<details>
<summary><strong>Solution</strong></summary>

Going down group 17, atomic size increases dramatically, so the $\ce{H-I}$ bond is longer and much weaker than $\ce{H-Cl}$. Down a group, this bond-strength effect outweighs the electronegativity difference.

**Answer:** The weaker $\ce{H-I}$ bond releases $\ce{H+}$ more easily; down a group bond strength beats electronegativity, so $\ce{HI} > \ce{HCl}$.

</details>

### Problem 4
Rank $\ce{HBrO}$, $\ce{HBrO2}$, $\ce{HBrO3}$ by acid strength.

<details>
<summary><strong>Solution</strong></summary>

Same central atom ($\ce{Br}$); only the **oxygen count** changes. More oxygens pull charge off the $\ce{O-H}$ and delocalize the conjugate base's charge over more oxygens.

**Answer:** $\ce{HBrO} < \ce{HBrO2} < \ce{HBrO3}$ (more oxygens = more stable conjugate base = stronger acid).

</details>

### Problem 5
Rank $\ce{H2SeO4}$ and $\ce{H2SO4}$. Which is stronger and why?

<details>
<summary><strong>Solution</strong></summary>

Same number of oxygens (four) and same group; the central atoms differ. $\ce{S}$ is more electronegative than $\ce{Se}$, so it pulls charge off the $\ce{O-H}$ oxygen more effectively, giving a more stable conjugate base.

**Answer:** $\ce{H2SO4} > \ce{H2SeO4}$ (more electronegative central atom → more stable conjugate base → stronger acid).

</details>

### Problem 6
Which is the stronger acid: acetic acid $\ce{CH3COOH}$ or bromoacetic acid $\ce{CH2BrCOOH}$? Justify.

<details>
<summary><strong>Solution</strong></summary>

Bromoacetic acid has an electronegative $\ce{Br}$ that withdraws electron density (inductive effect). In its conjugate base $\ce{CH2BrCOO-}$, the bromine helps pull the negative charge away and spread it out, stabilizing the anion. Acetic acid's $\ce{CH3-}$ group offers no such stabilization.

**Answer:** $\ce{CH2BrCOOH}$ is stronger — the electron-withdrawing $\ce{Br}$ stabilizes the conjugate base.

</details>

### Problem 7
Put these in order of increasing acid strength: $\ce{CH3COOH}$, $\ce{CHCl2COOH}$, $\ce{CCl3COOH}$.

<details>
<summary><strong>Solution</strong></summary>

More electron-withdrawing chlorines → more conjugate-base stabilization → stronger acid. Chlorine count: $0 < 2 < 3$.

**Answer:** $\ce{CH3COOH} < \ce{CHCl2COOH} < \ce{CCl3COOH}$.

</details>

### Problem 8
Why is a carboxylic acid ($\ce{RCOOH}$) so much more acidic than an alcohol ($\ce{ROH}$)? Use the word "resonance."

<details>
<summary><strong>Solution</strong></summary>

The carboxylate conjugate base $\ce{RCOO-}$ has two equivalent resonance structures, so the negative charge is delocalized over two oxygens — a very stable anion. The alkoxide $\ce{RO-}$ has no resonance; its charge is localized on one oxygen, making it much less stable.

**Answer:** Resonance delocalization stabilizes the carboxylate conjugate base, so the carboxylic acid is far stronger.

</details>

### Problem 9
Which has the larger $K_a$: $\ce{HClO3}$ or $\ce{HClO}$? Explain through conjugate-base stability.

<details>
<summary><strong>Solution</strong></summary>

Same central atom; $\ce{HClO3}$ has three oxygens vs. one. The conjugate base $\ce{ClO3-}$ delocalizes its charge over three oxygens, while $\ce{ClO-}$ has it on one. More delocalization = more stable = stronger acid.

**Answer:** $\ce{HClO3}$ has the larger $K_a$ (more stable conjugate base).

</details>

### Problem 10
Rank the conjugate bases $\ce{Cl-}$, $\ce{Br-}$, $\ce{I-}$ from strongest to weakest base.

<details>
<summary><strong>Solution</strong></summary>

Look at the conjugate acids: $\ce{HCl} < \ce{HBr} < \ce{HI}$ in strength. The weaker the acid, the stronger the conjugate base — so reverse the order.

**Answer:** $\ce{Cl-} > \ce{Br-} > \ce{I-}$ in base strength. (The strongest acid $\ce{HI}$ has the weakest conjugate base $\ce{I-}$.)

</details>

### Problem 11
A student claims "$\ce{HF}$ is the strongest acid of the hydrogen halides because $\ce{F}$ is the most electronegative element." Identify the error and give the correct answer with justification.

<details>
<summary><strong>Solution</strong></summary>

The error is applying the electronegativity lever when moving **down a group**. Down a group, bond strength dominates: the $\ce{H-F}$ bond is the shortest and strongest of the halides, so $\ce{HF}$ releases $\ce{H+}$ least easily.

**Answer:** $\ce{HF}$ is actually the **weakest** of the four; $\ce{HI}$ is the strongest because the $\ce{H-I}$ bond is longest/weakest. Down a group, bond strength beats electronegativity.

</details>

### Problem 12
Rank $\ce{H3PO4}$, $\ce{H3AsO4}$ by acid strength (both have the same number of oxygens).

<details>
<summary><strong>Solution</strong></summary>

Same oxygen count, same group (15). The central atoms differ: $\ce{P}$ is more electronegative than $\ce{As}$. More electronegative central atom → charge pulled off $\ce{O-H}$ → more stable conjugate base → stronger acid.

**Answer:** $\ce{H3PO4} > \ce{H3AsO4}$.

</details>

### Problem 13
Order these four acids from weakest to strongest and give a one-line reason for each step: $\ce{HIO}$, $\ce{HClO}$, $\ce{HClO2}$, $\ce{HClO4}$.

<details>
<summary><strong>Solution</strong></summary>

- $\ce{HIO}$ vs. $\ce{HClO}$: same oxygen count; $\ce{Cl}$ more electronegative than $\ce{I}$ → $\ce{HIO} < \ce{HClO}$.
- $\ce{HClO}$ vs. $\ce{HClO2}$ vs. $\ce{HClO4}$: same central atom, increasing oxygens → increasing strength.

**Answer:** $\ce{HIO} < \ce{HClO} < \ce{HClO2} < \ce{HClO4}$.

</details>

### Problem 14
On a free-response question you're asked to justify why $\ce{HClO4}$ is a stronger acid than $\ce{HClO3}$. Write a full-credit two-sentence justification.

<details>
<summary><strong>Solution</strong></summary>

**Answer:** "$\ce{HClO4}$ has more oxygen atoms bonded to the central chlorine than $\ce{HClO3}$. This lets the negative charge of the conjugate base $\ce{ClO4-}$ be delocalized (spread out) over more electronegative oxygen atoms, making the conjugate base more stable, so $\ce{HClO4}$ is the stronger acid."

(Note the scoring anatomy: structural difference → charge delocalization → conjugate-base stability → stronger acid.)

</details>

### Problem 15
Which is the stronger base, $\ce{CH3COO-}$ (acetate) or $\ce{CCl3COO-}$ (trichloroacetate)? Justify through the conjugate acids.

<details>
<summary><strong>Solution</strong></summary>

The conjugate acids are acetic acid ($\ce{CH3COOH}$, weak) and trichloroacetic acid ($\ce{CCl3COOH}$, much stronger). The stronger the acid, the weaker the conjugate base. Since trichloroacetic acid is the stronger acid, trichloroacetate is the weaker base.

**Answer:** $\ce{CH3COO-}$ (acetate) is the stronger base. The electron-withdrawing chlorines make $\ce{CCl3COO-}$ a very stable, weak base.

</details>

---

## Quick Reference

| Situation | What decides strength | Rule of thumb |
|---|---|---|
| Binary $\ce{H-X}$, **down a group** | **Bond strength** (size) | Bigger $\ce{X}$ → weaker bond → **stronger** acid ($\ce{HF}<\ce{HCl}<\ce{HBr}<\ce{HI}$) |
| Binary $\ce{H-X}$, **across a period** | **Electronegativity** | More electronegative $\ce{X}$ → stabler $\ce{X-}$ → **stronger** acid ($\ce{CH4}<\ce{NH3}<\ce{H2O}<\ce{HF}$) |
| Oxyacid, vary **# of O** | Oxygen count | More O → charge spread over more O → **stronger** ($\ce{HClO}<\ce{HClO2}<\ce{HClO3}<\ce{HClO4}$) |
| Oxyacid, vary **central atom** | Central-atom EN | More electronegative $\ce{Y}$ → **stronger** ($\ce{HClO}>\ce{HBrO}>\ce{HIO}$) |
| Carboxylic acid + nearby groups | Inductive (electron-withdrawing) | More/closer/more-EN withdrawing atoms → **stronger** (acetic $<$ trichloroacetic) |
| Resonance in the anion | Charge delocalization | Charge spread over equivalent atoms → stabler anion → **stronger** acid |
| Base strength | Conjugate-**acid** strength | Weak conjugate acid → **strong** base (flip the acid ranking) |

**The one principle behind all of it:** acid strength = ease of releasing $\ce{H+}$ = **stability of the conjugate base**. When in doubt, ask *"how stable is the anion after the $\ce{H}$ leaves?"* and justify with the words **"conjugate-base stability."**

---

<div align="center">

[← Weak Acids and Bases](/chemistry/1002-weak-acids-and-bases) | [Buffers →](/chemistry/1004-buffers)

</div>
