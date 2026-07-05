# Net Ionic Equations
<p class="article-date">July 5, 2026</p>

*I stayed up too late watching basketball highlights again. Here's the thing about a highlight reel: there are ten players on the court for the buzzer-beater, but the fifteen-second clip only shows three of them — the guy who steals the ball, the guy who throws the outlet pass, and the guy who dunks it at the horn. The other seven players were absolutely there. They ran up and down the court, they waved their arms, they existed. But the editor cropped them out, because they didn't do anything worth filming. A net ionic equation is chemistry's highlight reel. When you dump two solutions together, tons of ions are floating around in the beaker — but usually only two or three of them actually do anything. The rest just drift, unchanged, before and after. The net ionic equation strips out those bench-warmers (we call them **spectator ions** — I love that the real chemistry term is literally "spectator") and shows only the players in the actual scoring play. This is AP Unit 4, Topics 4.1–4.4, and it's the machinery every reaction problem for the rest of the year runs on. It's also worth real points on the free-response section every single year, so this one pays rent.*

---

## What You'll Learn
- Tell a **physical change** apart from a **chemical change**, and list the five classic pieces of evidence that a chemical reaction happened
- Apply the "was a *new substance* formed?" test to classify an everyday change
- Read a reaction in its three representations: the **molecular (formula) equation**, the **complete ionic equation**, and the **net ionic equation**
- Decide, for any species, whether it **splits into ions** or **stays together** — the single skill this whole topic rests on
- Identify the **spectator ions** in a reaction and cancel them correctly
- Write net ionic equations for **precipitation**, **acid–base**, and **gas-forming** reactions
- Audit a net ionic equation so that **both mass and charge** balance — the extra check beyond counting atoms
- Reason about **particulate (before/after) diagrams**: write the reaction they show, or spot what's drawn wrong
- Understand why **weak acids stay molecular** — the classic trap you'll see again in Unit 8

---

## Prerequisites
- [Balancing Equations](/chemistry/0206-balancing-equations) — a net ionic equation is still an equation; it must be atom-balanced first, and coefficients still mean the same thing
- [Solutions and Concentration](/chemistry/0506-solutions-and-concentration) — this is where you learned that soluble ionic compounds *dissociate* into free ions in water ($\ce{NaCl(s) -> Na+(aq) + Cl-(aq)}$); "splitting into ions" is that idea doing all the work here
- [Polyatomic Ions](/chemistry/0205-polyatomic-ions) — you can't split $\ce{Na2CO3}$ correctly if you don't know that $\ce{CO3^2-}$ travels as one intact unit with a $2-$ charge; these have to be automatic

---

## The Core Concept

### Intuition First

Let's roll the tape on a real beaker. I pour a clear solution of silver nitrate into a clear solution of sodium chloride, and *instantly* a cloudy white solid appears and starts sinking. That white solid is the buzzer-beater — the thing worth filming. But watch what's actually in the two beakers before I mix them.

Silver nitrate in water isn't sitting there as little $\ce{AgNO3}$ units. Back in [Solutions and Concentration](/chemistry/0506-solutions-and-concentration) we learned that soluble ionic compounds **dissociate** — water rips them into free, independently roaming ions. So the "silver nitrate" beaker is really a swarm of separate $\ce{Ag+}$ and $\ce{NO3^-}$ ions. The "sodium chloride" beaker is a swarm of separate $\ce{Na+}$ and $\ce{Cl-}$ ions. Now I pour them together and there are **four** different ions on the court:

$$\underbrace{\ce{Ag+}}_{\text{player}} \qquad \underbrace{\ce{NO3^-}}_{\text{bench}} \qquad \underbrace{\ce{Na+}}_{\text{bench}} \qquad \underbrace{\ce{Cl-}}_{\text{player}}$$

Here's the play. $\ce{Ag+}$ and $\ce{Cl-}$ find each other and lock together into a solid, $\ce{AgCl}$, which is not soluble — it drops out of solution as that white cloud (a **precipitate**). That's the dunk. Meanwhile $\ce{Na+}$ and $\ce{NO3^-}$? They were floating free before the pour, and they're *still* floating free after. Nothing happened to them. They're the seven players who ran around and got cropped out. They are **spectator ions**.

So the highlight reel — the net ionic equation — is just:

$$\ce{Ag+(aq) + Cl-(aq) -> AgCl(s)}$$

That's the entire event. Everything else was footage on the cutting-room floor. Hold onto this mapping, because it's the whole article:

| Basketball | Chemistry |
|---|---|
| All ten players on the court | The **molecular equation** (everything written as whole compounds) |
| The broadcast showing every player dissociated and visible | The **complete ionic equation** (every dissolved ionic compound split into ions) |
| The three players in the scoring play | The **net ionic equation** (only species that change) |
| The seven benchwarmers cropped from the clip | The **spectator ions** (present but unchanged) |

### First, a Step Back: Did a Reaction Even Happen? (Topic 4.4)

Before we film the highlight reel, we have to know a play *occurred*. Not everything that happens in a beaker is a chemical reaction. There are two categories of change:

- A **physical change** rearranges *where* the particles are, but the substance is still the same substance. Ice melting into water, sugar dissolving in tea, tearing paper, water boiling into steam — in every case, $\ce{H2O}$ is still $\ce{H2O}$, sugar is still sugar. Nothing new was made. (This ties straight back to the reflection question in [Why Chemistry Matters](/chemistry/0001-why-chemistry-matters): the shampoo one felt like a chemical change, but dissolving and foaming is mostly *physical*.)
- A **chemical change** (a reaction) produces **one or more genuinely new substances** with new properties. The atoms get rebonded into different molecules. That white $\ce{AgCl}$ cloud didn't exist before — it's new.

The one test that always works: **was a new substance formed?** If yes, it's chemical. Dissolving salt is physical (you can boil the water off and get your exact salt back). Rusting iron is chemical (you cannot un-rust it by drying).

We can't always see the atoms rebonding, so chemists watch for **five classic pieces of evidence** that a chemical reaction happened:

| Evidence | What you see | Example |
|---|---|---|
| **Color change** | Solution or solid shifts color | $\ce{Fe}$ turning orange with rust |
| **Gas / bubbles** | Fizzing not from boiling | Baking soda + vinegar foaming |
| **Precipitate** | A solid appears in a clear liquid | $\ce{AgCl}$ clouding up |
| **Temperature change** | Beaker gets hot or cold on its own | A hand-warmer, or $\ce{HCl + NaOH}$ warming up |
| **Light / flame** | Energy released as light | A glow stick, burning magnesium |

One honest caution the AP exam loves: **bubbles alone don't guarantee a reaction.** Water boiling makes bubbles, but that's a physical change (steam is still water). The evidence is a *clue*, not a proof — the real test is always "new substance?"

### The Three Representations (Topics 4.1 and 4.3)

Every reaction in solution can be written three ways, and the exam expects you to move between them fluently. Let's build all three for the silver-chloride play.

**1. Molecular (formula) equation.** Everything written as complete, neutral compounds — the "all ten players on the court, in uniform" view. It's balanced and it uses correct states.

$$\ce{AgNO3(aq) + NaCl(aq) -> AgCl(s) + NaNO3(aq)}$$

**2. Complete ionic equation.** Now show what's *actually* floating in the beaker. Every species that dissolves as free ions gets **split apart**. Every species that stays intact — solids, liquids, gases, weak acids — stays whole.

$$\ce{Ag+(aq) + NO3^-(aq) + Na+(aq) + Cl-(aq) -> AgCl(s) + Na+(aq) + NO3^-(aq)}$$

**3. Net ionic equation.** Cancel anything that appears **identical on both sides** — the spectators — and write only what's left.

$$\ce{Ag+(aq) + Cl-(aq) -> AgCl(s)}$$

Notice $\ce{Na+}$ and $\ce{NO3^-}$ show up unchanged on both sides, so they cancel like terms on both sides of an algebra equation. What survives is the actual chemistry.

### The Rule That Decides Everything: Split or Stay?

This is the make-or-break skill. When you write the complete ionic equation, which species do you pull apart into ions, and which do you leave whole?

| SPLIT into ions | STAY together (write as one whole formula) |
|---|---|
| **Soluble ionic compounds** — labeled $(aq)$ | **Solids** — $(s)$, including precipitates |
| **Strong acids** — $\ce{HCl}$, $\ce{HBr}$, $\ce{HI}$, $\ce{HNO3}$, $\ce{H2SO4}$, $\ce{HClO4}$ | **Liquids** — $(l)$, like water $\ce{H2O}$ |
| **Strong bases** — group 1 hydroxides, plus $\ce{Ca(OH)2}$, $\ce{Ba(OH)2}$, $\ce{Sr(OH)2}$ | **Gases** — $(g)$, like $\ce{CO2}$ |
| | **Weak acids & weak bases** — $\ce{CH3COOH}$, $\ce{HF}$, $\ce{NH3}$ |
| | **Molecular (covalent) compounds** — like sugar $\ce{C12H22O11}$ |

The one-line memory hook: **only strong electrolytes that are dissolved ($aq$) split.** Everything that is *not* a free-floating dissolved strong electrolyte — anything solid, liquid, gaseous, weak, or molecular — stays glued together. The state symbol is doing most of the work: if it's $(aq)$ *and* it's a strong electrolyte, split it; otherwise, leave it whole.

Why does this rule exist? Because splitting a formula into ions is only honest if those ions *really are* floating around separately in the beaker. A precipitate isn't split because its ions locked back into a solid lattice. A weak acid isn't split because — as we'll see hard in Unit 8 — it stays mostly as whole molecules, only a tiny fraction ionizes. Water is a liquid, not a swarm of ions, so it stays as $\ce{H2O}$. You're only writing down what's genuinely there.

### Why Both Mass *and* Charge Must Balance

In [Balancing Equations](/chemistry/0206-balancing-equations), balancing meant one thing: the same number of each atom on both sides (conserve mass). Net ionic equations add a **second** requirement, because now we're writing charged particles: **the total charge must be equal on both sides too.**

Check our silver-chloride net ionic:

$$\ce{Ag+(aq) + Cl-(aq) -> AgCl(s)}$$

- **Mass:** left has 1 Ag, 1 Cl; right has 1 Ag, 1 Cl. ✓
- **Charge:** left is $(+1) + (-1) = 0$; right is $0$ (neutral solid). $0 = 0$. ✓

Both balance, so the equation is legitimate. If the charges *didn't* match, you'd know you either mis-split something or dropped an ion — it's a free error-check the exam graders use, so use it too.

---

## Worked Examples

### Example 1: Classify the Change — Physical or Chemical?

**Problem:** For each, state physical or chemical and give your reasoning: (a) an ice cube melts in your soda, (b) a nail left outside turns orange and flaky, (c) you dissolve sugar in iced tea, (d) a lit match burns down.

**Solution:**
- **(a) Physical.** Solid water becomes liquid water — still $\ce{H2O}$. A phase change is physical; no new substance.
- **(b) Chemical.** The orange flaky stuff is rust ($\ce{Fe2O3}\cdot x\ce{H2O}$), a brand-new substance with new properties. You can't dry it back into shiny iron. Color change is the giveaway.
- **(c) Physical.** Sugar molecules just spread out among the tea; boil the water off and you recover your sugar unchanged. Dissolving is physical.
- **(d) Chemical.** Combustion turns the matchwood into $\ce{CO2}$, water vapor, and ash — new substances — releasing light and heat.

**Answer:** (a) physical, (b) chemical, (c) physical, (d) chemical.

### Example 2: Full Highlight Reel — A Precipitation Reaction

**Problem:** When lead(II) nitrate and potassium iodide solutions mix, a brilliant yellow solid, $\ce{PbI2}$, forms. Write all three representations.

**Solution:**

**Step 1 — Molecular equation (balanced, with states).** Swap partners (double replacement): $\ce{Pb^2+}$ pairs with $\ce{I-}$, $\ce{K+}$ pairs with $\ce{NO3^-}$.

$$\ce{Pb(NO3)2(aq) + 2KI(aq) -> PbI2(s) + 2KNO3(aq)}$$

**Step 2 — Complete ionic equation.** Split every soluble strong electrolyte $(aq)$; leave the $\ce{PbI2(s)}$ solid whole. Watch the coefficients — $2\ce{KI}$ gives $2\ce{K+}$ and $2\ce{I-}$.

$$\ce{Pb^2+(aq) + 2NO3^-(aq) + 2K+(aq) + 2I-(aq) -> PbI2(s) + 2K+(aq) + 2NO3^-(aq)}$$

**Step 3 — Cancel spectators.** $\ce{K+}$ (2 on each side) and $\ce{NO3^-}$ (2 on each side) are unchanged. Cancel them.

$$\ce{Pb^2+(aq) + 2I-(aq) -> PbI2(s)}$$

**Step 4 — Audit charge.** Left: $(+2) + 2(-1) = 0$. Right: $0$. ✓ Mass: 1 Pb, 2 I each side. ✓

**Answer:** $\ce{Pb^2+(aq) + 2I-(aq) -> PbI2(s)}$

### Example 3: The Classic Strong Acid + Strong Base

**Problem:** Write the net ionic equation for hydrochloric acid neutralizing sodium hydroxide.

**Solution:**

**Step 1 — Molecular:**
$$\ce{HCl(aq) + NaOH(aq) -> NaCl(aq) + H2O(l)}$$

**Step 2 — Complete ionic.** $\ce{HCl}$ is a strong acid → split. $\ce{NaOH}$ is a strong base → split. $\ce{NaCl}$ is soluble → split. But $\ce{H2O}$ is a **liquid** → stays whole.

$$\ce{H+(aq) + Cl-(aq) + Na+(aq) + OH-(aq) -> Na+(aq) + Cl-(aq) + H2O(l)}$$

**Step 3 — Cancel spectators.** $\ce{Na+}$ and $\ce{Cl-}$ appear unchanged on both sides.

$$\ce{H+(aq) + OH-(aq) -> H2O(l)}$$

**Answer:** $\ce{H+(aq) + OH-(aq) -> H2O(l)}$ — this is *the* net ionic for every strong acid + strong base neutralization. Memorize it; it recurs constantly.

### Example 4: A Gas-Forming Reaction

**Problem:** Sodium carbonate reacts with hydrochloric acid, and the mixture fizzes as $\ce{CO2}$ gas escapes. Write molecular, complete ionic, and net ionic equations.

**Solution:**

**Step 1 — Molecular.** Carbonate + acid produces water and carbon dioxide (a classic pattern: the unstable $\ce{H2CO3}$ that would form immediately falls apart into $\ce{H2O}$ and $\ce{CO2}$).

$$\ce{Na2CO3(aq) + 2HCl(aq) -> 2NaCl(aq) + H2O(l) + CO2(g)}$$

**Step 2 — Complete ionic.** Split $\ce{Na2CO3}$ (soluble), $\ce{HCl}$ (strong acid), and $\ce{NaCl}$ (soluble). Keep $\ce{H2O(l)}$ and $\ce{CO2(g)}$ whole — a liquid and a gas.

$$\ce{2Na+(aq) + CO3^2-(aq) + 2H+(aq) + 2Cl-(aq) -> 2Na+(aq) + 2Cl-(aq) + H2O(l) + CO2(g)}$$

**Step 3 — Cancel spectators.** $\ce{Na+}$ (2 each side) and $\ce{Cl-}$ (2 each side) drop out.

$$\ce{CO3^2-(aq) + 2H+(aq) -> H2O(l) + CO2(g)}$$

**Step 4 — Audit charge.** Left: $(-2) + 2(+1) = 0$. Right: $0$. ✓ Mass: C 1=1, O 3 = (1 + 2), H 2 = 2. ✓

**Answer:** $\ce{2H+(aq) + CO3^2-(aq) -> H2O(l) + CO2(g)}$

### Example 5: Spot the Spectators

**Problem:** In the reaction $\ce{BaCl2(aq) + Na2SO4(aq) -> BaSO4(s) + 2NaCl(aq)}$, name the spectator ions and the species that actually react.

**Solution:**

**Step 1 — Split the aqueous strong electrolytes; keep the precipitate whole.**
$$\ce{Ba^2+(aq) + 2Cl-(aq) + 2Na+(aq) + SO4^2-(aq) -> BaSO4(s) + 2Na+(aq) + 2Cl-(aq)}$$

**Step 2 — Find what's identical on both sides.** $\ce{Na+}$: 2 left, 2 right. $\ce{Cl-}$: 2 left, 2 right. Both unchanged → spectators.

**Step 3 — What's left are the players:** $\ce{Ba^2+}$ and $\ce{SO4^2-}$ combine into the solid.

**Answer:** Spectators: $\ce{Na+}$ and $\ce{Cl-}$. Reacting species (net ionic): $\ce{Ba^2+(aq) + SO4^2-(aq) -> BaSO4(s)}$.

### Example 6: The Weak-Acid Trap

**Problem:** Acetic acid (the acid in vinegar, $\ce{CH3COOH}$) reacts with sodium hydroxide. Write the net ionic equation. Be careful.

**Solution:**

**Step 1 — Molecular:**
$$\ce{CH3COOH(aq) + NaOH(aq) -> CH3COONa(aq) + H2O(l)}$$

**Step 2 — Complete ionic. Here's the trap.** $\ce{CH3COOH}$ is a **weak acid** — it stays mostly as whole molecules in solution, so it does **NOT** split. $\ce{NaOH}$ (strong base) splits, and the salt $\ce{CH3COONa}$ (soluble) splits into $\ce{CH3COO-}$ and $\ce{Na+}$.

$$\ce{CH3COOH(aq) + Na+(aq) + OH-(aq) -> CH3COO-(aq) + Na+(aq) + H2O(l)}$$

**Step 3 — Cancel spectators.** Only $\ce{Na+}$ is unchanged.

$$\ce{CH3COOH(aq) + OH-(aq) -> CH3COO-(aq) + H2O(l)}$$

**Answer:** $\ce{CH3COOH(aq) + OH-(aq) -> CH3COO-(aq) + H2O(l)}$. Note the acetic acid stays whole on the left — writing it as $\ce{H+ + CH3COO-}$ would be *wrong* and would cost the FRQ point. Weak acids stay molecular. (We'll prove exactly why in Unit 8.)

### Example 7: Charge-Balance Audit as a Catch

**Problem:** A student writes $\ce{Ag+(aq) + Cl-(aq) -> AgCl2(s)}$ as a net ionic equation. Use a mass-and-charge audit to show it's wrong.

**Solution:**

**Step 1 — Mass check.** Left: 1 Ag, 1 Cl. Right: 1 Ag, **2** Cl. The chlorines don't match — mass fails immediately.

**Step 2 — Charge check (for practice).** Left: $(+1) + (-1) = 0$. Right: neutral solid $= 0$. Charge *happens* to balance, but mass doesn't, so the equation is still invalid.

**Step 3 — Fix it.** The real precipitate is $\ce{AgCl}$ (silver is $+1$, chloride is $-1$, so one each): $\ce{Ag+(aq) + Cl-(aq) -> AgCl(s)}$.

**Answer:** The student's formula $\ce{AgCl2}$ is wrong; mass isn't conserved. Correct: $\ce{Ag+(aq) + Cl-(aq) -> AgCl(s)}$.

### Example 8: Read a Particulate Diagram, Write the Reaction

**Problem:** A before/after particle picture shows this. Write the net ionic equation and name the spectators.

```
   BEFORE (mixed)                AFTER
   ●=Ag+  ○=NO3-              ▓ = AgCl solid (clumped)
   ■=Na+  □=Cl-

   ● ○ ■ □                     ▓▓
   □ ● ○ ■        ---->        ▓▓     ○ ■
   ■ ○ □ ●                     ▓▓   ■ ○  ○ ■
   (3 Ag+, 3 Cl-,             (3 AgCl units clumped
    3 Na+, 3 NO3-)             as solid; 3 Na+ and
                               3 NO3- still floating)
```

**Solution:**

**Step 1 — Read "before."** Four kinds of free ions: $\ce{Ag+}$, $\ce{Cl-}$, $\ce{Na+}$, $\ce{NO3^-}$, three of each.

**Step 2 — Read "after."** The $\ce{Ag+}$ and $\ce{Cl-}$ are gone from solution — they've clumped into a solid ($\ce{AgCl}$). The $\ce{Na+}$ and $\ce{NO3^-}$ are still drawn floating, same count as before → unchanged → spectators.

**Step 3 — Write the net ionic** from what left solution and became solid:
$$\ce{Ag+(aq) + Cl-(aq) -> AgCl(s)}$$

**Answer:** Net ionic $\ce{Ag+(aq) + Cl-(aq) -> AgCl(s)}$; spectators are $\ce{Na+}$ and $\ce{NO3^-}$ (still free in the "after" frame).

### Example 9: Spot What's Wrong with a Diagram

**Problem:** A student draws the "after" frame of the $\ce{Pb(NO3)2 + KI}$ reaction with the solid shown as *one* $\ce{Pb}$ paired with *one* $\ce{I}$ (a 1:1 clump), and shows the $\ce{K+}$ ions clumped together into a solid too. Name two errors.

**Solution:**

**Error 1 — Wrong ratio in the solid.** Lead is $\ce{Pb^2+}$ and iodide is $\ce{I-}$, so the precipitate must be $\ce{PbI2}$ — **two** iodides per lead, not 1:1. The drawing must show clumps of one $\ce{Pb}$ with two $\ce{I}$.

**Error 2 — Spectators shouldn't clump.** $\ce{K+}$ and $\ce{NO3^-}$ are spectators; $\ce{KNO3}$ is soluble, so they must stay drawn as *separate free ions* floating in the "after" frame, not as a solid.

**Answer:** (1) The solid should be $\ce{PbI2}$ (1 Pb : 2 I), not 1:1; (2) the $\ce{K+}$ (and $\ce{NO3^-}$) spectators must remain free ions, not a clumped solid.

### Example 10: Another Precipitation, Full Chain

**Problem:** Silver nitrate reacts with sodium phosphate to precipitate silver phosphate, $\ce{Ag3PO4}$. Write all three equations.

**Solution:**

**Step 1 — Molecular** (balance: 3 silvers needed per phosphate):
$$\ce{3AgNO3(aq) + Na3PO4(aq) -> Ag3PO4(s) + 3NaNO3(aq)}$$

**Step 2 — Complete ionic.** Split all soluble strong electrolytes; keep $\ce{Ag3PO4(s)}$ whole. Note $\ce{PO4^3-}$ travels as one intact polyatomic unit.
$$\ce{3Ag+(aq) + 3NO3^-(aq) + 3Na+(aq) + PO4^3-(aq) -> Ag3PO4(s) + 3Na+(aq) + 3NO3^-(aq)}$$

**Step 3 — Cancel spectators** $\ce{Na+}$ (3 each side) and $\ce{NO3^-}$ (3 each side):
$$\ce{3Ag+(aq) + PO4^3-(aq) -> Ag3PO4(s)}$$

**Step 4 — Audit charge.** Left: $3(+1) + (-3) = 0$. Right: $0$. ✓ Mass: 3 Ag, 1 P, 4 O each side. ✓

**Answer:** $\ce{3Ag+(aq) + PO4^3-(aq) -> Ag3PO4(s)}$

### Example 11: When There's No Reaction (Empty Highlight Reel)

**Problem:** Mix sodium chloride solution and potassium nitrate solution. Write the net ionic equation.

**Solution:**

**Step 1 — Molecular (swap partners):** the possible products are $\ce{NaNO3}$ and $\ce{KCl}$ — both soluble, so nothing leaves solution.
$$\ce{NaCl(aq) + KNO3(aq) -> NaNO3(aq) + KCl(aq)}$$

**Step 2 — Complete ionic:** split everything, since it's all soluble.
$$\ce{Na+(aq) + Cl-(aq) + K+(aq) + NO3^-(aq) -> Na+(aq) + NO3^-(aq) + K+(aq) + Cl-(aq)}$$

**Step 3 — Cancel.** *Every* ion is identical on both sides — all four are spectators. Nothing is left.

**Answer:** **No reaction** ($\ce{NR}$). The highlight reel is empty — every player was a benchwarmer. When all ions cancel, no chemical change occurred.

### Example 12: Gas-Forming with a Metal — Single Replacement

**Problem:** Zinc metal is dropped into hydrochloric acid; bubbles of $\ce{H2}$ rise off the metal. Write the net ionic equation.

**Solution:**

**Step 1 — Molecular:**
$$\ce{Zn(s) + 2HCl(aq) -> ZnCl2(aq) + H2(g)}$$

**Step 2 — Complete ionic.** $\ce{Zn}$ is a solid → stays whole. $\ce{HCl}$ (strong acid) and $\ce{ZnCl2}$ (soluble) → split. $\ce{H2(g)}$ → stays whole.
$$\ce{Zn(s) + 2H+(aq) + 2Cl-(aq) -> Zn^2+(aq) + 2Cl-(aq) + H2(g)}$$

**Step 3 — Cancel** the spectator $\ce{Cl-}$ (2 each side):
$$\ce{Zn(s) + 2H+(aq) -> Zn^2+(aq) + H2(g)}$$

**Step 4 — Audit charge.** Left: $0 + 2(+1) = +2$. Right: $(+2) + 0 = +2$. ✓ Mass: 1 Zn, 2 H each side. ✓

**Answer:** $\ce{Zn(s) + 2H+(aq) -> Zn^2+(aq) + H2(g)}$ — a great example where charge is *not* zero but still balances ($+2 = +2$).

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Splitting a **precipitate** or solid into ions | Habit — you split the same formula on the reactant side, so you split it on the product side too | The state symbol is law: $(s)$ **never** splits. Ions in a solid are locked in a lattice, not floating |
| Splitting a **weak acid** like $\ce{CH3COOH}$ or $\ce{HF}$ | It's an acid and it's aqueous, so it *looks* splittable | Only **strong** acids split. Memorize the short strong-acid list; everything else acidic stays whole |
| Splitting **water** into $\ce{H+ + OH-}$ | It contains H and O ions in your mind | Water is a **liquid** $(l)$; it stays $\ce{H2O}$. Same for any $(l)$ or $(g)$ |
| Forgetting to distribute **coefficients** when splitting | $2\ce{KI}$ becoming "$\ce{K+ + I-}$" instead of $2\ce{K+} + 2\ce{I-}$ | Multiply the coefficient through both ions *before* cancelling |
| Cancelling ions that **aren't actually identical** | $\ce{Cl-}$ appears on both sides but in different amounts | Only cancel a species where the **same number** appears on both sides; cancel the smaller amount, keep the leftover |
| Leaving **charge unbalanced** | You only checked atoms, like in a molecular equation | Always run the extra **charge audit**: total charge left = total charge right |
| Dropping **state symbols** | Rushing | States are graded on the FRQ — $(aq)$, $(s)$, $(l)$, $(g)$ every time |
| Calling dissolving or boiling a **chemical** change | Bubbles/disappearing *look* dramatic | Ask "is it a *new substance*?" Boiling water is still water; dissolved salt is still salt |

---

## AP Exam Tips

- **This is a guaranteed points topic.** The AP Chemistry free-response section asks you to write a net ionic equation almost every year (historically its own reaction-prediction question). It's low-effort, high-reward if you drilled the split-vs-stay rules — so drill them cold.
- **Write only the net ionic** unless the problem explicitly asks for molecular or complete ionic. The graders want the highlight reel, not the full broadcast. Extra spectator ions left in can cost the point.
- **Include state symbols.** $(aq)$, $(s)$, $(l)$, $(g)$ are part of a correct answer on the rubric. Forgetting the $(s)$ on a precipitate is a common silent point-loss.
- **Balance BOTH mass and charge.** Run the two-line audit every time. Graders check charge; if your charges don't match, the equation is wrong even if the atoms balance.
- **Weak acids stay molecular — the #1 trap.** $\ce{HF}$, $\ce{CH3COOH}$, $\ce{H2CO3}$, $\ce{HCN}$, $\ce{H3PO4}$ do *not* split. Only the seven-ish strong acids do. This exact trap comes back in Unit 8 (acids and bases), so lock it in now.
- **This topic leans on two others.** You *cannot* decide what splits without solubility fluency and [Polyatomic Ions](/chemistry/0205-polyatomic-ions) mastery. If you're shaky on $\ce{SO4^2-}$, $\ce{NO3^-}$, $\ce{CO3^2-}$, $\ce{PO4^3-}$ charges, fix that first — it's the bottleneck.
- **"No reaction" is a valid answer.** If every ion cancels (all products soluble, no gas, no water, no precipitate), the correct response is $\ce{NR}$. Don't invent a reaction that isn't there.
- **Particulate diagrams reward the same thinking.** For a before/after picture, the spectators appear *unchanged in count* on both sides; the reacting ions disappear from solution (into a solid or gas). Check that ion ratios in any drawn solid match the formula (e.g., $\ce{PbI2}$ is 1:2).

> **🎬 Hollywood Chemistry: Real or Not?**
> *The scene:* In movies, dumping two clear liquids together makes an instant, dramatic color-swirl or a cloud of "smoke."
> *The verdict:* Half real. A precipitation reaction genuinely *can* turn two clear solutions instantly cloudy — pour $\ce{AgNO3}$ into $\ce{NaCl}$ and you really do get an immediate white cloud of $\ce{AgCl(s)}$. What's Hollywood is the billowing *smoke* and neon glow; most real precipitates are just a quiet milky haze that slowly settles to the bottom. The net ionic equation, $\ce{Ag+(aq) + Cl-(aq) -> AgCl(s)}$, is the whole "special effect" — three species, one solid, no pyrotechnics.

---

## Practice Problems

### Problem 1
Classify each as physical or chemical change: (a) a candle's wax melting, (b) the same candle's wick burning, (c) chopping firewood, (d) milk going sour.

<details>
<summary><strong>Solution</strong></summary>

- **(a) Physical** — solid wax to liquid wax, still wax (phase change).
- **(b) Chemical** — combustion makes $\ce{CO2}$, water, and light; new substances.
- **(c) Physical** — smaller pieces of wood, still wood.
- **(d) Chemical** — bacteria produce new acidic substances; you can't un-sour milk.

**Answer:** (a) physical, (b) chemical, (c) physical, (d) chemical.
</details>

### Problem 2
List the five common pieces of evidence that a chemical reaction has occurred, and explain why "bubbles" alone isn't proof.

<details>
<summary><strong>Solution</strong></summary>

Color change, gas/bubbles, precipitate (solid forming), temperature change, and light/flame. Bubbles alone aren't proof because **boiling** also makes bubbles, yet boiling is a *physical* change — steam is still $\ce{H2O}$. The only sure test is: *was a new substance formed?*

**Answer:** The five: color change, gas formation, precipitate, temperature change, light. Bubbles can be physical (boiling), so they're a clue, not proof.
</details>

### Problem 3
For $\ce{HNO3(aq) + KOH(aq) -> KNO3(aq) + H2O(l)}$, write the complete ionic and net ionic equations.

<details>
<summary><strong>Solution</strong></summary>

$\ce{HNO3}$ (strong acid), $\ce{KOH}$ (strong base), $\ce{KNO3}$ (soluble) all split; $\ce{H2O(l)}$ stays whole.

Complete ionic:
$$\ce{H+(aq) + NO3^-(aq) + K+(aq) + OH-(aq) -> K+(aq) + NO3^-(aq) + H2O(l)}$$

Cancel spectators $\ce{K+}$ and $\ce{NO3^-}$:

**Answer:** $\ce{H+(aq) + OH-(aq) -> H2O(l)}$
</details>

### Problem 4
Barium chloride reacts with sodium sulfate to precipitate barium sulfate. Write the molecular, complete ionic, and net ionic equations.

<details>
<summary><strong>Solution</strong></summary>

Molecular:
$$\ce{BaCl2(aq) + Na2SO4(aq) -> BaSO4(s) + 2NaCl(aq)}$$

Complete ionic (split all aqueous; keep $\ce{BaSO4(s)}$ whole):
$$\ce{Ba^2+(aq) + 2Cl-(aq) + 2Na+(aq) + SO4^2-(aq) -> BaSO4(s) + 2Na+(aq) + 2Cl-(aq)}$$

Cancel $\ce{Na+}$ and $\ce{Cl-}$:

**Answer:** $\ce{Ba^2+(aq) + SO4^2-(aq) -> BaSO4(s)}$. Charge check: $(+2)+(-2)=0=0$. ✓
</details>

### Problem 5
Identify the spectator ions in: $\ce{2AgNO3(aq) + CaCl2(aq) -> 2AgCl(s) + Ca(NO3)2(aq)}$.

<details>
<summary><strong>Solution</strong></summary>

Complete ionic:
$$\ce{2Ag+(aq) + 2NO3^-(aq) + Ca^2+(aq) + 2Cl-(aq) -> 2AgCl(s) + Ca^2+(aq) + 2NO3^-(aq)}$$

$\ce{Ca^2+}$ (1 each side) and $\ce{NO3^-}$ (2 each side) are unchanged.

**Answer:** Spectators are $\ce{Ca^2+}$ and $\ce{NO3^-}$. Net ionic: $\ce{Ag+(aq) + Cl-(aq) -> AgCl(s)}$.
</details>

### Problem 6
Write the net ionic equation for hydrofluoric acid ($\ce{HF}$, a **weak** acid) reacting with potassium hydroxide. Watch the trap.

<details>
<summary><strong>Solution</strong></summary>

$\ce{HF}$ is a *weak* acid → stays molecular. $\ce{KOH}$ (strong base) and $\ce{KF}$ (soluble salt) split.

Molecular: $\ce{HF(aq) + KOH(aq) -> KF(aq) + H2O(l)}$

Complete ionic: $\ce{HF(aq) + K+(aq) + OH-(aq) -> K+(aq) + F-(aq) + H2O(l)}$

Cancel $\ce{K+}$:

**Answer:** $\ce{HF(aq) + OH-(aq) -> F-(aq) + H2O(l)}$. $\ce{HF}$ stays whole — writing $\ce{H+ + F-}$ would be wrong.
</details>

### Problem 7
Potassium carbonate reacts with nitric acid, releasing $\ce{CO2}$ gas. Write molecular and net ionic equations.

<details>
<summary><strong>Solution</strong></summary>

Molecular:
$$\ce{K2CO3(aq) + 2HNO3(aq) -> 2KNO3(aq) + H2O(l) + CO2(g)}$$

Complete ionic (split $\ce{K2CO3}$, $\ce{HNO3}$, $\ce{KNO3}$; keep $\ce{H2O(l)}$, $\ce{CO2(g)}$):
$$\ce{2K+(aq) + CO3^2-(aq) + 2H+(aq) + 2NO3^-(aq) -> 2K+(aq) + 2NO3^-(aq) + H2O(l) + CO2(g)}$$

Cancel $\ce{K+}$ and $\ce{NO3^-}$:

**Answer:** $\ce{2H+(aq) + CO3^2-(aq) -> H2O(l) + CO2(g)}$. Charge: $2(+1)+(-2)=0=0$. ✓
</details>

### Problem 8
A student writes the net ionic $\ce{Ca^2+(aq) + OH-(aq) -> Ca(OH)2(s)}$. Show it fails the audit and fix it.

<details>
<summary><strong>Solution</strong></summary>

- **Charge:** left $(+2) + (-1) = +1$; right $= 0$. $+1 \ne 0$ → **charge fails**.
- **Mass:** left 1 Ca, 1 O, 1 H; right 1 Ca, 2 O, 2 H → **mass fails** too.

Both fail because there's only one $\ce{OH-}$. You need two hydroxides to balance the $2+$ calcium.

**Answer:** $\ce{Ca^2+(aq) + 2OH-(aq) -> Ca(OH)2(s)}$. Now charge: $(+2)+2(-1)=0=0$ ✓ and mass balances.
</details>

### Problem 9
Mix sodium sulfate and potassium chloride solutions. Write the net ionic equation (think about whether anything happens).

<details>
<summary><strong>Solution</strong></summary>

Possible products from swapping partners: $\ce{NaCl}$ and $\ce{K2SO4}$ — both soluble. Nothing leaves solution; every ion is a spectator.

**Answer:** **No reaction** ($\ce{NR}$). All four ions ($\ce{Na+}$, $\ce{SO4^2-}$, $\ce{K+}$, $\ce{Cl-}$) cancel.
</details>

### Problem 10
Magnesium metal reacts with hydrochloric acid to release hydrogen gas. Write the net ionic equation and verify charge balance.

<details>
<summary><strong>Solution</strong></summary>

Molecular: $\ce{Mg(s) + 2HCl(aq) -> MgCl2(aq) + H2(g)}$

Complete ionic (Mg solid and $\ce{H2}$ gas stay whole; $\ce{HCl}$ and $\ce{MgCl2}$ split):
$$\ce{Mg(s) + 2H+(aq) + 2Cl-(aq) -> Mg^2+(aq) + 2Cl-(aq) + H2(g)}$$

Cancel $\ce{Cl-}$:

**Answer:** $\ce{Mg(s) + 2H+(aq) -> Mg^2+(aq) + H2(g)}$. Charge: left $2(+1)=+2$; right $+2$. ✓
</details>

### Problem 11
A before/after particle diagram is described below. Write the net ionic equation and name the spectators.

```
BEFORE (mixed solution)          AFTER
● = Cu2+   ○ = SO4^2-            ▒ = Cu(OH)2 solid
■ = Na+    □ = OH-

  ● ○ ■ □ □                       ▒▒▒
  ■ □ ○ ● □          --->         ▒▒▒     ■ ○
  ● ○ ■ □ □                       ▒▒▒   ■ ○  ■ ○
 (3 Cu2+, 6 OH-,                 (3 Cu(OH)2 clumped
  3 Na+, 3 SO4^2-... )            as solid; Na+ and
                                  SO4^2- still free)
```

<details>
<summary><strong>Solution</strong></summary>

Before: free $\ce{Cu^2+}$, $\ce{OH-}$, $\ce{Na+}$, $\ce{SO4^2-}$. After: $\ce{Cu^2+}$ and $\ce{OH-}$ have left solution as solid $\ce{Cu(OH)2}$ (note the 1:2 ratio — 3 Cu paired with 6 OH); $\ce{Na+}$ and $\ce{SO4^2-}$ are still floating unchanged → spectators.

**Answer:** $\ce{Cu^2+(aq) + 2OH-(aq) -> Cu(OH)2(s)}$; spectators $\ce{Na+}$ and $\ce{SO4^2-}$. Charge: $(+2)+2(-1)=0=0$ ✓.
</details>

### Problem 12
Convert this molecular equation to its net ionic form: $\ce{3NaOH(aq) + FeCl3(aq) -> Fe(OH)3(s) + 3NaCl(aq)}$.

<details>
<summary><strong>Solution</strong></summary>

Split $\ce{NaOH}$, $\ce{FeCl3}$, $\ce{NaCl}$ (all aqueous strong electrolytes); keep $\ce{Fe(OH)3(s)}$ whole.

Complete ionic:
$$\ce{3Na+(aq) + 3OH-(aq) + Fe^3+(aq) + 3Cl-(aq) -> Fe(OH)3(s) + 3Na+(aq) + 3Cl-(aq)}$$

Cancel $\ce{Na+}$ (3 each) and $\ce{Cl-}$ (3 each):

**Answer:** $\ce{Fe^3+(aq) + 3OH-(aq) -> Fe(OH)3(s)}$. Charge: $(+3)+3(-1)=0=0$ ✓.
</details>

### Problem 13
Ammonia ($\ce{NH3}$, a **weak base**) reacts with hydrochloric acid to form ammonium chloride. Write the net ionic equation.

<details>
<summary><strong>Solution</strong></summary>

$\ce{HCl}$ is a strong acid → splits. $\ce{NH3}$ is a weak base → stays whole. $\ce{NH4Cl}$ is soluble → splits.

Molecular: $\ce{NH3(aq) + HCl(aq) -> NH4Cl(aq)}$

Complete ionic: $\ce{NH3(aq) + H+(aq) + Cl-(aq) -> NH4+(aq) + Cl-(aq)}$

Cancel $\ce{Cl-}$:

**Answer:** $\ce{NH3(aq) + H+(aq) -> NH4+(aq)}$. Charge: left $+1$, right $+1$ ✓. ($\ce{NH3}$ stays molecular — the weak-base version of the same trap.)
</details>

### Problem 14
A student claims that mixing $\ce{KNO3(aq)}$ and $\ce{NaCl(aq)}$ produces the precipitate $\ce{NaNO3(s)}$. Explain what's wrong.

<details>
<summary><strong>Solution</strong></summary>

$\ce{NaNO3}$ is a **soluble** salt — sodium compounds and nitrate compounds are always soluble, so it would stay dissolved as $\ce{Na+(aq)}$ and $\ce{NO3^-(aq)}$, not fall out as a solid. In fact both possible products ($\ce{NaNO3}$ and $\ce{KCl}$) are soluble, so no precipitate forms at all.

**Answer:** Wrong — $\ce{NaNO3}$ is soluble and doesn't precipitate. This is a **no-reaction** mixture; all ions are spectators. (Solubility rules that make this automatic come next, in [Types of Reactions](/chemistry/0602-types-of-reactions).)
</details>

### Problem 15
Write the net ionic equation for solid calcium carbonate (chalk, $\ce{CaCO3}$, insoluble) dissolving in hydrochloric acid to give $\ce{CO2}$ gas.

<details>
<summary><strong>Solution</strong></summary>

Here the reactant $\ce{CaCO3}$ is a **solid** → it stays whole (it's not dissolved!). $\ce{HCl}$ splits; $\ce{CaCl2}$ (soluble) splits; $\ce{H2O(l)}$ and $\ce{CO2(g)}$ stay whole.

Molecular: $\ce{CaCO3(s) + 2HCl(aq) -> CaCl2(aq) + H2O(l) + CO2(g)}$

Complete ionic: $\ce{CaCO3(s) + 2H+(aq) + 2Cl-(aq) -> Ca^2+(aq) + 2Cl-(aq) + H2O(l) + CO2(g)}$

Cancel $\ce{Cl-}$:

**Answer:** $\ce{CaCO3(s) + 2H+(aq) -> Ca^2+(aq) + H2O(l) + CO2(g)}$. Note $\ce{CaCO3}$ stays whole because it's a solid — a great reminder that the state symbol, not the compound type, decides. Charge: left $2(+1)=+2$; right $+2$ ✓.
</details>

---

## Quick Reference

| Representation | What it shows | Basketball |
|---|---|---|
| **Molecular equation** | All whole compounds, balanced, with states | All ten players on court |
| **Complete ionic equation** | Every soluble strong electrolyte split into ions | Full broadcast, everyone visible |
| **Net ionic equation** | Only species that change; spectators cancelled | The 15-second highlight clip |
| **Spectator ions** | Identical on both sides, unchanged | Cropped-out benchwarmers |

**SPLIT into ions** (write separately): soluble ionic compounds $(aq)$ · strong acids ($\ce{HCl, HBr, HI, HNO3, H2SO4, HClO4}$) · strong bases (group 1 hydroxides, $\ce{Ca(OH)2, Ba(OH)2, Sr(OH)2}$).

**STAY together** (write whole): solids $(s)$ incl. precipitates · liquids $(l)$ incl. $\ce{H2O}$ · gases $(g)$ · weak acids/bases ($\ce{CH3COOH, HF, NH3}$) · molecular compounds.

**The two-line audit** every net ionic must pass:
1. **Mass** — same count of each atom on both sides.
2. **Charge** — same total charge on both sides.

**Key net ionics to know cold:**
- Strong acid + strong base: $\ce{H+(aq) + OH-(aq) -> H2O(l)}$
- Silver + halide: $\ce{Ag+(aq) + Cl-(aq) -> AgCl(s)}$
- Carbonate + strong acid: $\ce{2H+(aq) + CO3^2-(aq) -> H2O(l) + CO2(g)}$

---

<div align="center">

[← Spectroscopy and Beer's Law](/chemistry/0508-spectroscopy-beer-lambert) | [Types of Reactions →](/chemistry/0602-types-of-reactions)

</div>
