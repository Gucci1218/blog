# Acid-Base Reactions
<p class="article-date">July 5, 2026</p>

*Last night I made the mistake of ordering the "level 3 spicy" wings and then finishing the whole basket. Twenty minutes later my stomach felt like a lava lamp — that hot, sour, burning ache. My mom tossed me a chalky little tablet, I chewed it, it fizzed, I burped, and the misery just... melted away. That tablet was an antacid, and what happened inside me was a genuine chemical reaction. My stomach is full of hydrochloric acid — real $\ce{HCl}$, the same stuff on the strong-acid list — and it was winning. The antacid ($\ce{CaCO3}$, basically fancy chalk) is a **base**, and when acid meets base they cancel each other out in a **neutralization reaction**: the aggressive acid gets turned into a harmless salt, plain water, and a puff of $\ce{CO2}$ gas — that's the burp. Aggressor in, harmless stuff out. That's the whole personality of this unit. Every part of that Tums moment maps onto a piece of acid-base chemistry, and by the end of this article you'll be able to write the exact equation for what settled my stomach. This is Topic 4.8, our first real look at the reactions that run everything from your blood to your swimming pool — and the launchpad for all of Unit 8.*

---

## What You'll Learn
- State the **Arrhenius** definition of acids ($\ce{H+}$ producers) and bases ($\ce{OH-}$ producers) in water
- State the broader **Bronsted-Lowry** definition — acids are proton **donors**, bases are proton **acceptors** — and explain why AP prefers it
- Identify **conjugate acid-base pairs** in any reaction using the "differ by exactly one $\ce{H+}$" rule
- Recognize **amphoteric** species like water and $\ce{HCO3-}$ that can act as either acid or base
- Memorize the short list of **strong acids and strong bases**, and explain why everything else is weak
- Explain why "strong" is not the same as "concentrated"
- Write **molecular and net ionic equations** for neutralization, keeping weak acids intact
- Predict the products of acid + carbonate and acid + active metal reactions
- Use $\text{pH} = -\log[\ce{H+}]$ to find the pH of strong acids and bases (a preview of Unit 8)

---

## Prerequisites
- [Net Ionic Equations](/chemistry/0601-net-ionic-equations) — neutralization is written as a net ionic equation, and the single biggest trap (weak acids stay molecular) comes straight from here
- [Logarithms for Chemistry](/chemistry/0104-logarithms-for-chemistry) — pH is a logarithm, so $-\log$ and powers of ten need to feel automatic before we preview the pH scale

---

## The Core Concept

### Intuition First

Let's stay inside my stomach for a minute, because it's a perfect little acid-base lab.

Your stomach lining makes **hydrochloric acid**, $\ce{HCl}$, on purpose — it helps digest food and kills germs. Normally your stomach is fine with it. But eat something too spicy or greasy and you make *too much*, and it starts irritating you. That burning feeling is chemistry: $\ce{HCl}$ is an acid, which means it's throwing off **protons** — hydrogen ions, $\ce{H+}$ — into the fluid around it.

$$\ce{HCl -> H+ + Cl-}$$

Now the rescue. An antacid is a **base**: a substance that grabs those loose protons. Tums is calcium carbonate, $\ce{CaCO3}$; the carbonate part, $\ce{CO3^2-}$, is hungry for $\ce{H+}$. When they meet, the acid *donates* its proton and the base *accepts* it. That single handoff is the heart of every acid-base reaction:

$$\text{acid (proton donor)} \;\xrightarrow{\;\ce{H+}\;}\; \text{base (proton acceptor)}$$

Here's the map I want you to carry through the whole article:

| The Tums moment | The chemistry |
|---|---|
| Stomach acid, $\ce{HCl}$ | the **acid** — the proton **donor** |
| The antacid, $\ce{CaCO3}$ | the **base** — the proton **acceptor** |
| The relief | **neutralization** — acid + base cancel out |
| The harmless leftovers | a **salt** + **water** |
| The burp | $\ce{CO2}$ gas, released from the carbonate |

That's it. An acid hands off a proton, a base catches it, and if you started with an aggressive acid and a base, you end up with mild, harmless products. Everything else in this article is just learning to *write down* that handoff precisely.

### Definition 1: Arrhenius (the starter definition)

The oldest, simplest definition, from Svante Arrhenius, is about what things do **in water**:

- An **Arrhenius acid** dissolves in water and increases the concentration of $\ce{H+}$ (hydrogen ions).
- An **Arrhenius base** dissolves in water and increases the concentration of $\ce{OH-}$ (hydroxide ions).

$$\ce{HCl(aq) -> H+(aq) + Cl-(aq)} \qquad \text{(acid: makes } \ce{H+}\text{)}$$
$$\ce{NaOH(aq) -> Na+(aq) + OH-(aq)} \qquad \text{(base: makes } \ce{OH-}\text{)}$$

This is clean and correct — but it's too narrow. It only works in water, and it can't explain why something like ammonia, $\ce{NH3}$, is a base even though it has no $\ce{OH-}$ to give. We need something bigger.

> One quick honesty note: a bare proton $\ce{H+}$ doesn't really float around alone in water — it latches onto a water molecule to form the **hydronium ion**, $\ce{H3O+}$. So $\ce{H+(aq)}$ and $\ce{H3O+}$ mean the same thing, and AP accepts either. I'll mostly write $\ce{H+}$ for simplicity.

### Definition 2: Bronsted-Lowry (the AP-preferred definition)

Johannes Bronsted and Thomas Lowry zoomed out to the actual event — the **proton handoff** — and stopped caring about water specifically:

- A **Bronsted-Lowry acid** is a **proton ($\ce{H+}$) donor**.
- A **Bronsted-Lowry base** is a **proton ($\ce{H+}$) acceptor**.

This is the definition AP Chemistry lives by, so burn it in: **acid donates, base accepts.** Watch ammonia finally make sense — it's a base because it *accepts* a proton, even with no hydroxide anywhere in sight:

$$\ce{NH3 + H2O <=> NH4+ + OH-}$$

Here $\ce{NH3}$ grabbed an $\ce{H+}$ from water to become $\ce{NH4+}$. Ammonia accepted a proton — base. Water donated one — acid. Every Bronsted-Lowry reaction is one species handing a proton to another.

### Conjugate Acid-Base Pairs

Here's the elegant part. When an acid donates its proton, what's left behind is itself a base — because it could, in principle, grab a proton right back. That "leftover" is called the **conjugate base**. Likewise, when a base accepts a proton, the thing it becomes is a **conjugate acid**.

The rule that makes them trivial to spot:

> **Members of a conjugate pair differ by exactly one $\ce{H+}$.** The one *with* the extra proton is the acid; the one *without* it is the base.

Look at the ammonia reaction again, this time tagging everyone:

$$\underset{\text{acid}}{\ce{HCl}} + \underset{\text{base}}{\ce{H2O}} \longrightarrow \underset{\text{conj. acid}}{\ce{H3O+}} + \underset{\text{conj. base}}{\ce{Cl-}}$$

Two pairs hide in there, each differing by one proton:

| Acid | ⇌ | Conjugate base | Differ by |
|---|---|---|---|
| $\ce{HCl}$ | | $\ce{Cl-}$ | one $\ce{H+}$ |
| $\ce{H3O+}$ | | $\ce{H2O}$ | one $\ce{H+}$ |

To find any conjugate: **add** one $\ce{H+}$ (and raise the charge by +1) to go base → acid, or **remove** one $\ce{H+}$ (and lower the charge by 1) to go acid → base. That's the entire skill.

### Amphoteric Species (the both-ways players)

Notice that **water** was an acid in one reaction (donating to $\ce{NH3}$) and could be a base in another (accepting from $\ce{HCl}$). A species that can act as **either** an acid or a base is called **amphoteric** (or amphiprotic). Water is the classic example. So is the **bicarbonate** ion, $\ce{HCO3-}$ — the one in baking soda and, not coincidentally, in your blood:

$$\ce{HCO3- + H+ -> H2CO3} \qquad \text{(acting as a base — accepts } \ce{H+}\text{)}$$
$$\ce{HCO3- -> H+ + CO3^2-} \qquad \text{(acting as an acid — donates } \ce{H+}\text{)}$$

Your blood uses this two-faced ability to hold its pH steady — that's a **buffer**, and it's a big Unit 8 payoff. For now just recognize the word: amphoteric = plays both positions.

### Strong vs. Weak: Fully vs. Partially

This is the distinction that decides how you write every equation, so slow down here.

- A **strong** acid or base **dissociates completely** in water — essentially every molecule breaks apart into ions. We write it with a one-way arrow $\ce{->}$.
- A **weak** acid or base **dissociates only partially** — most molecules stay intact, and only a small fraction ionize at any moment. We write it with an equilibrium arrow $\ce{<=>}$.

$$\ce{HCl -> H+ + Cl-} \qquad \text{(strong: goes all the way)}$$
$$\ce{CH3COOH <=> H+ + CH3COO-} \qquad \text{(weak: mostly stays whole)}$$

There is a **short list of strong acids and strong bases**. Memorize it. If an acid or base is **not** on the list, treat it as weak. This is one of the highest-value memorizations in AP Chemistry:

| The 6 strong acids | The strong bases |
|---|---|
| $\ce{HCl}$ (hydrochloric) | Group 1 hydroxides: $\ce{LiOH}$, $\ce{NaOH}$, $\ce{KOH}$, $\ce{RbOH}$, $\ce{CsOH}$ |
| $\ce{HBr}$ (hydrobromic) | Heavy Group 2 hydroxides: $\ce{Ca(OH)2}$, $\ce{Sr(OH)2}$, $\ce{Ba(OH)2}$ |
| $\ce{HI}$ (hydroiodic) | |
| $\ce{HNO3}$ (nitric) | |
| $\ce{H2SO4}$ (sulfuric) | |
| $\ce{HClO4}$ (perchloric) | |

A mnemonic for the acids I use: **"I Bring No Clear Sulfuric Perchloric"** is clunky, so honestly just drill the six. Everything else — $\ce{HF}$, acetic acid $\ce{CH3COOH}$, carbonic acid $\ce{H2CO3}$, $\ce{NH3}$ as a base — is **weak**.

**Why does this matter so much?** Because in a [net ionic equation](/chemistry/0601-net-ionic-equations), only substances that actually break into ions get split apart. A strong acid fully dissociates, so you split it. A **weak acid stays as an intact molecule** — it barely ionizes, so you write it whole. This is the single most-tested trap in this whole area, and we'll hit it head-on in the neutralization section.

### "Strong" Does NOT Mean "Concentrated"

This trips up everyone, so let's kill it now. **Strong** describes *how completely* an acid dissociates — a fixed property of the substance. **Concentrated** describes *how much* acid is dissolved per liter — how many moles you dumped in.

- A drop of pure $\ce{HCl}$ in a swimming pool is **strong but dilute**: it fully dissociates, but there's barely any of it.
- A jar of concentrated vinegar (acetic acid) is **weak but concentrated**: tons of it per liter, but only a sliver ionizes at a time.

Strong is about *quality* (does it fully break apart?); concentrated is about *quantity* (how much is there?). They're independent knobs. My stomach acid is actually a strong acid at a fairly modest concentration — plenty to make me miserable.

### Neutralization: acid + base → salt + water

When an acid and a base react, they cancel each other's chemistry. The general pattern:

$$\text{acid} + \text{base} \longrightarrow \text{salt} + \text{water}$$

A **salt** here just means an ionic compound made from the acid's anion and the base's cation — not necessarily table salt. The famous strong-acid + strong-base example:

$$\ce{HCl(aq) + NaOH(aq) -> NaCl(aq) + H2O(l)} \qquad \text{(molecular)}$$

Now write the **net ionic** version. Split every strong, soluble, aqueous species into ions, then cancel the spectators ($\ce{Na+}$ and $\ce{Cl-}$ appear on both sides):

$$\ce{H+(aq) + OH-(aq) -> H2O(l)} \qquad \text{(net ionic)}$$

This tiny equation — $\ce{H+ + OH- -> H2O}$ — is the net ionic equation for **every** strong acid + strong base neutralization. Memorize it. The proton from the acid and the hydroxide from the base combine into water, and that's the whole story.

### The Weak-Acid Twist (the recurring trap)

Change the acid to a **weak** one, like acetic acid, and the net ionic equation changes fundamentally. Because a weak acid **stays molecular** (it doesn't fully dissociate), you may **not** split it into ions:

$$\ce{CH3COOH(aq) + NaOH(aq) -> CH3COONa(aq) + H2O(l)} \qquad \text{(molecular)}$$
$$\ce{CH3COOH(aq) + OH-(aq) -> CH3COO-(aq) + H2O(l)} \qquad \text{(net ionic)}$$

See the difference? The strong base $\ce{NaOH}$ still splits (so $\ce{Na+}$ is a spectator and drops out), but the weak acid $\ce{CH3COOH}$ is written **whole** on the left, and its conjugate base $\ce{CH3COO-}$ appears on the right. If you had wrongly split the weak acid, you'd have gotten the plain $\ce{H+ + OH- -> H2O}$ and lost points. **Weak acids and weak bases stay intact in net ionic equations.** Tattoo it.

### The Antacid Reaction: acid + carbonate → salt + water + $\ce{CO2}$

Back to my stomach. Tums is $\ce{CaCO3}$, a carbonate. When a carbonate (or bicarbonate) meets an acid, you get the usual salt + water **plus a bonus product**: carbon dioxide gas. That's the fizz and the burp.

$$\ce{CaCO3(s) + 2HCl(aq) -> CaCl2(aq) + H2O(l) + CO2(g)}$$

What actually happens: the carbonate grabs protons to form carbonic acid, $\ce{H2CO3}$, which is unstable and immediately falls apart into water and $\ce{CO2}$:

$$\ce{CO3^2- + 2H+ -> H2CO3 -> H2O + CO2 ^}$$

That's why every acid-plus-carbonate reaction bubbles. The exact same thing happens in the baking-soda-and-vinegar volcano from every science fair — sodium **bicarbonate** meets acetic acid:

$$\ce{NaHCO3(s) + CH3COOH(aq) -> CH3COONa(aq) + H2O(l) + CO2(g)}$$

Pattern to memorize: **acid + carbonate (or bicarbonate) → salt + water + $\ce{CO2}$.**

### Acid + Active Metal → salt + $\ce{H2}$

One more reaction pattern lives in this neighborhood. Drop an **active metal** (like zinc or magnesium) into an acid and it fizzes too — but this time the gas is **hydrogen**, not $\ce{CO2}$. This is a **single-replacement** reaction (remember those from [Net Ionic Equations](/chemistry/0601-net-ionic-equations)): the metal kicks $\ce{H+}$ out of its spot and takes over.

$$\ce{Zn(s) + 2HCl(aq) -> ZnCl2(aq) + H2(g) ^}$$
$$\ce{Mg(s) + H2SO4(aq) -> MgSO4(aq) + H2(g) ^}$$

Pattern: **acid + active metal → salt + $\ce{H2}$.** The metal is oxidized and the $\ce{H+}$ is reduced — which means this is secretly a redox reaction, the exact bridge to our [next article](/chemistry/0606-redox-reactions).

### pH: A Preview Only

We keep talking about how much $\ce{H+}$ an acid throws off. The **pH scale** is just a compact way to report that concentration. Because $\ce{H+}$ concentrations span a huge range (from about $1$ down to $10^{-14}$ mol/L), we take a logarithm:

$$\text{pH} = -\log[\ce{H+}]$$

The square brackets $[\ce{H+}]$ mean "molar concentration of $\ce{H+}$." Here's the whole map:

| pH | $[\ce{H+}]$ | Meaning | Everyday example |
|---|---|---|---|
| $0$–$7$ (low) | high | **acidic** | stomach acid (~1–2), lemon (~2), coffee (~5) |
| $7$ | $10^{-7}$ | **neutral** | pure water |
| $7$–$14$ (high) | low | **basic** (alkaline) | baking soda (~9), bleach (~13), antacid |

Two facts to carry:

1. **Lower pH = more acidic** (more $\ce{H+}$). Each pH unit is a **factor of 10** in $\ce{H+}$ — pH 2 is ten times more acidic than pH 3.
2. In any water solution at 25 °C, $\ce{H+}$ and $\ce{OH-}$ are locked together by:
$$[\ce{H+}][\ce{OH-}] = 1.0 \times 10^{-14}$$
So if you know one, you know the other. This also gives a partner formula, $\text{pOH} = -\log[\ce{OH-}]$, with $\text{pH} + \text{pOH} = 14$.

**Big honest limit — read this.** You can only compute pH *this simply* for **strong** acids and bases, because they fully dissociate, so $[\ce{H+}]$ just equals the acid's concentration. For a **weak** acid, only a fraction ionizes, so $[\ce{H+}]$ is *less* than the concentration and you need an equilibrium constant called $K_a$ to find it. **We are explicitly not doing weak-acid pH here** — that's the core of Unit 8. Everything below is strong-only.

### The Titration Connection

If you've read [Titration](/chemistry/0604-titration), you've already met the lab technique for finding an unknown concentration by reacting it with a known one. The most common titrations in all of chemistry are **acid-base titrations**: you slowly add a strong base to an acid (or vice versa) until neutralization is exactly complete at the **equivalence point**. Every drop is running the $\ce{H+ + OH- -> H2O}$ reaction you just learned. The full titration *curves* — the S-shaped pH-vs-volume graphs, indicators, buffers — come together in Unit 8, but the reaction underneath them is this one.

---

## Worked Examples

### Example 1: Classify Acid or Base (Arrhenius)
**Problem:** For each, say whether it's an Arrhenius acid or base and why: (a) $\ce{HNO3}$, (b) $\ce{KOH}$, (c) $\ce{H2SO4}$.

**Solution:**
- (a) $\ce{HNO3 -> H+ + NO3-}$ — produces $\ce{H+}$ → **acid**.
- (b) $\ce{KOH -> K+ + OH-}$ — produces $\ce{OH-}$ → **base**.
- (c) $\ce{H2SO4 -> 2H+ + SO4^2-}$ — produces $\ce{H+}$ → **acid** (a diprotic one, two protons to give).

**Answer:** (a) acid, (b) base, (c) acid.

### Example 2: Identify the Bronsted-Lowry Acid and Base
**Problem:** In $\ce{HF + H2O <=> H3O+ + F-}$, identify the Bronsted-Lowry acid and base on the left.

**Solution:** Follow the proton. $\ce{HF}$ loses an $\ce{H+}$ to become $\ce{F-}$ — it **donated** a proton, so $\ce{HF}$ is the acid. $\ce{H2O}$ gains that $\ce{H+}$ to become $\ce{H3O+}$ — it **accepted**, so water is the base.

**Answer:** Acid = $\ce{HF}$ (proton donor); base = $\ce{H2O}$ (proton acceptor).

### Example 3: Write a Conjugate Base
**Problem:** Give the conjugate base of (a) $\ce{HNO3}$, (b) $\ce{H2CO3}$, (c) $\ce{NH4+}$.

**Solution:** Remove one $\ce{H+}$ and lower the charge by 1.
- (a) $\ce{HNO3}$ → remove $\ce{H+}$ → $\ce{NO3-}$.
- (b) $\ce{H2CO3}$ → remove one $\ce{H+}$ → $\ce{HCO3-}$.
- (c) $\ce{NH4+}$ → remove $\ce{H+}$, charge $+1 \to 0$ → $\ce{NH3}$.

**Answer:** (a) $\ce{NO3-}$, (b) $\ce{HCO3-}$, (c) $\ce{NH3}$.

### Example 4: Write a Conjugate Acid
**Problem:** Give the conjugate acid of (a) $\ce{OH-}$, (b) $\ce{CO3^2-}$, (c) $\ce{NH3}$.

**Solution:** Add one $\ce{H+}$ and raise the charge by +1.
- (a) $\ce{OH-}$ → add $\ce{H+}$, charge $-1 \to 0$ → $\ce{H2O}$.
- (b) $\ce{CO3^2-}$ → add $\ce{H+}$, charge $-2 \to -1$ → $\ce{HCO3-}$.
- (c) $\ce{NH3}$ → add $\ce{H+}$, charge $0 \to +1$ → $\ce{NH4+}$.

**Answer:** (a) $\ce{H2O}$, (b) $\ce{HCO3-}$, (c) $\ce{NH4+}$.

### Example 5: Both Conjugate Pairs in a Reaction
**Problem:** Identify both conjugate acid-base pairs in $\ce{HCO3- + H2O <=> H2CO3 + OH-}$.

**Solution:** Find who differs by one proton.
- $\ce{HCO3-}$ gained a proton to become $\ce{H2CO3}$ → pair: $\ce{H2CO3}$ (acid) / $\ce{HCO3-}$ (base).
- $\ce{H2O}$ lost a proton to become $\ce{OH-}$ → pair: $\ce{H2O}$ (acid) / $\ce{OH-}$ (base).

Here $\ce{HCO3-}$ acted as a **base** (accepted $\ce{H+}$) — proof it's amphoteric.

**Answer:** Pair 1: $\ce{H2CO3}$/$\ce{HCO3-}$. Pair 2: $\ce{H2O}$/$\ce{OH-}$.

### Example 6: Strong or Weak?
**Problem:** Classify each as strong or weak: (a) $\ce{HBr}$, (b) $\ce{HF}$, (c) $\ce{Ba(OH)2}$, (d) $\ce{NH3}$, (e) $\ce{CH3COOH}$.

**Solution:** Check against the memorized lists.
- (a) $\ce{HBr}$ — on the strong-acid list → **strong acid**.
- (b) $\ce{HF}$ — *not* on the list (only $\ce{HCl}$, $\ce{HBr}$, $\ce{HI}$ are strong; fluorine is the odd one out) → **weak acid**.
- (c) $\ce{Ba(OH)2}$ — heavy Group 2 hydroxide → **strong base**.
- (d) $\ce{NH3}$ — ammonia, not a hydroxide → **weak base**.
- (e) $\ce{CH3COOH}$ — acetic acid, not on the list → **weak acid**.

**Answer:** (a) strong, (b) weak, (c) strong, (d) weak, (e) weak.

### Example 7: Net Ionic for Strong Acid + Strong Base
**Problem:** Write the molecular and net ionic equations for nitric acid reacting with potassium hydroxide.

**Solution:**
Step 1 — Molecular (acid + base → salt + water):
$$\ce{HNO3(aq) + KOH(aq) -> KNO3(aq) + H2O(l)}$$
Step 2 — Both are strong and soluble, so split them into ions:
$$\ce{H+ + NO3- + K+ + OH- -> K+ + NO3- + H2O}$$
Step 3 — Cancel spectators $\ce{K+}$ and $\ce{NO3-}$:
$$\ce{H+(aq) + OH-(aq) -> H2O(l)}$$

**Answer:** Net ionic: $\ce{H+ + OH- -> H2O}$ — the universal strong-strong result.

### Example 8: Net Ionic for Weak Acid + Strong Base (the trap)
**Problem:** Write the net ionic equation for hydrofluoric acid (weak) reacting with sodium hydroxide.

**Solution:**
Step 1 — Molecular:
$$\ce{HF(aq) + NaOH(aq) -> NaF(aq) + H2O(l)}$$
Step 2 — $\ce{NaOH}$ is strong (split it), but $\ce{HF}$ is **weak** — keep it whole. $\ce{NaF}$ is soluble, so split it:
$$\ce{HF + Na+ + OH- -> Na+ + F- + H2O}$$
Step 3 — Cancel the spectator $\ce{Na+}$:
$$\ce{HF(aq) + OH-(aq) -> F-(aq) + H2O(l)}$$

**Answer:** $\ce{HF + OH- -> F- + H2O}$. Notice $\ce{HF}$ never split — that's the whole point.

### Example 9: Predict Products — Acid + Carbonate
**Problem:** Predict the products and write the balanced molecular equation for $\ce{HCl}$ reacting with $\ce{CaCO3}$ (the Tums reaction).

**Solution:** Acid + carbonate → salt + water + $\ce{CO2}$. The salt pairs $\ce{Ca^2+}$ with $\ce{Cl-}$ → $\ce{CaCl2}$. Balance: two $\ce{HCl}$ are needed for the +2 calcium.
$$\ce{CaCO3(s) + 2HCl(aq) -> CaCl2(aq) + H2O(l) + CO2(g)}$$

**Answer:** $\ce{CaCl2}$, water, and $\ce{CO2}$ gas — the burp.

### Example 10: Predict Products — Acid + Active Metal
**Problem:** Predict the products of magnesium metal in hydrochloric acid and balance it.

**Solution:** Acid + active metal → salt + $\ce{H2}$. The salt pairs $\ce{Mg^2+}$ with $\ce{Cl-}$ → $\ce{MgCl2}$, which needs two $\ce{HCl}$:
$$\ce{Mg(s) + 2HCl(aq) -> MgCl2(aq) + H2(g)}$$

**Answer:** $\ce{MgCl2}$ and hydrogen gas, $\ce{H2}$.

### Example 11: pH of a Strong Acid
**Problem:** Find the pH of a $0.010\ \text{M}$ solution of $\ce{HCl}$.

**Solution:** $\ce{HCl}$ is strong, so it fully dissociates and $[\ce{H+}] = 0.010\ \text{M} = 1.0 \times 10^{-2}\ \text{M}$.
$$\text{pH} = -\log(1.0 \times 10^{-2}) = 2.0$$

**Answer:** pH $= 2.0$ (acidic, as expected). Because it's strong, no $K_a$ needed.

### Example 12: pH of a Strong Base
**Problem:** Find the pH of a $0.0010\ \text{M}$ solution of $\ce{NaOH}$.

**Solution:**
Step 1 — $\ce{NaOH}$ is strong → $[\ce{OH-}] = 1.0 \times 10^{-3}\ \text{M}$.
Step 2 — Use $[\ce{H+}][\ce{OH-}] = 1.0 \times 10^{-14}$:
$$[\ce{H+}] = \frac{1.0 \times 10^{-14}}{1.0 \times 10^{-3}} = 1.0 \times 10^{-11}\ \text{M}$$
Step 3 — $\text{pH} = -\log(1.0 \times 10^{-11}) = 11.0$.

(Shortcut check: $\text{pOH} = -\log(10^{-3}) = 3$, and $\text{pH} = 14 - 3 = 11$. ✓)

**Answer:** pH $= 11.0$ (basic, as expected).

---

## Common Mistakes

| The mistake | Why it happens | How to avoid it |
|---|---|---|
| Splitting a **weak acid** into ions in a net ionic equation | You forget that weak = barely dissociates | If it's not on the six-strong-acid list, write it **whole** as a molecule |
| Confusing **strong** with **concentrated** | Both words sound "powerful" | Strong = *fully dissociates* (quality); concentrated = *lots per liter* (quantity) — independent |
| Thinking $\ce{HF}$ is a strong acid | $\ce{HCl}$, $\ce{HBr}$, $\ce{HI}$ are strong, so fluorine "should" be too | $\ce{HF}$ is the one halogen acid that's **weak** — memorize the exclusion |
| Getting the conjugate charge wrong | Adding/removing $\ce{H+}$ but forgetting the charge shifts | Add $\ce{H+}$ → charge $+1$; remove $\ce{H+}$ → charge $-1$ |
| Forgetting $\ce{CO2}$ (or $\ce{H2}$) in the products | Only writing "salt + water" out of habit | Carbonate → also $\ce{CO2}$; active metal → also $\ce{H2}$ |
| Using $\text{pH} = -\log[\ce{H+}]$ with $[\ce{H+}] =$ concentration for a **weak** acid | The formula looks the same for everyone | Only strong acids have $[\ce{H+}] =$ concentration; weak acids need $K_a$ (Unit 8) |
| Reporting pH sig figs from the whole number | Treating "2" in $10^{-2}$ as the sig fig | In pH, only the **decimal digits** count as sig figs: $[\ce{H+}]$ with 2 sig figs → pH to 2 decimals |

---

## AP Exam Tips

- **Bronsted-Lowry is king.** When asked to identify an acid or base, describe it as a proton **donor** or **acceptor** — not "makes $\ce{H+}$/$\ce{OH-}$." The conjugate-pair question ("identify the conjugate base of X") is nearly guaranteed points; practice until "add/remove one $\ce{H+}$" is reflex.
- **Memorize the six strong acids and the strong-base rule cold.** $\ce{HCl}$, $\ce{HBr}$, $\ce{HI}$, $\ce{HNO3}$, $\ce{H2SO4}$, $\ce{HClO4}$; strong bases = Group 1 hydroxides + heavy Group 2 hydroxides. Anything else is weak. This one fact silently decides half of acid-base questions.
- **The weak-acid net-ionic trap is the highest-value gotcha in this unit.** On free response, a weak acid (or weak base) must stay **intact/molecular** in the net ionic equation; splitting it is an automatic lost point. Strong acid + strong base always reduces to $\ce{H+ + OH- -> H2O}$.
- **pH here is strong-only.** If the exam gives you a strong acid/base and a concentration, $[\ce{H+}]$ (or $[\ce{OH-}]$) equals that concentration and pH is a one-line calculation. If it's a **weak** acid, you cannot use $[\ce{H+}] =$ concentration — that requires $K_a$ and an equilibrium (ICE) table, which is Unit 8.
- **Know the gas-producing patterns.** Acid + carbonate/bicarbonate → salt + water + $\ce{CO2}$; acid + active metal → salt + $\ce{H2}$. The "fizzing gas" is a classic lab-observation prompt.
- **Sig figs in pH:** the digits *after* the decimal point are the significant ones. $[\ce{H+}] = 1.0\times10^{-2}$ (2 sig figs) → pH $= 2.00$.

---

## Practice Problems

### Problem 1
Define, in your own words, a Bronsted-Lowry acid and a Bronsted-Lowry base.

<details>
<summary><strong>Solution</strong></summary>

A Bronsted-Lowry **acid** is a proton ($\ce{H+}$) **donor** — it gives away a hydrogen ion. A Bronsted-Lowry **base** is a proton **acceptor** — it takes a hydrogen ion.

**Answer:** Acid = proton donor; base = proton acceptor.

</details>

### Problem 2
Give the conjugate base of each: (a) $\ce{H2SO4}$, (b) $\ce{HSO4-}$, (c) $\ce{H3O+}$, (d) $\ce{HCl}$.

<details>
<summary><strong>Solution</strong></summary>

Remove one $\ce{H+}$ and lower the charge by 1:
- (a) $\ce{H2SO4} \to \ce{HSO4-}$
- (b) $\ce{HSO4-} \to \ce{SO4^2-}$
- (c) $\ce{H3O+} \to \ce{H2O}$
- (d) $\ce{HCl} \to \ce{Cl-}$

**Answer:** (a) $\ce{HSO4-}$, (b) $\ce{SO4^2-}$, (c) $\ce{H2O}$, (d) $\ce{Cl-}$.

</details>

### Problem 3
Give the conjugate acid of each: (a) $\ce{F-}$, (b) $\ce{HCO3-}$, (c) $\ce{H2O}$, (d) $\ce{SO4^2-}$.

<details>
<summary><strong>Solution</strong></summary>

Add one $\ce{H+}$ and raise the charge by +1:
- (a) $\ce{F-} \to \ce{HF}$
- (b) $\ce{HCO3-} \to \ce{H2CO3}$
- (c) $\ce{H2O} \to \ce{H3O+}$
- (d) $\ce{SO4^2-} \to \ce{HSO4-}$

**Answer:** (a) $\ce{HF}$, (b) $\ce{H2CO3}$, (c) $\ce{H3O+}$, (d) $\ce{HSO4-}$.

</details>

### Problem 4
In the reaction $\ce{NH3 + H2O <=> NH4+ + OH-}$, identify both conjugate acid-base pairs and state which reactant is the base.

<details>
<summary><strong>Solution</strong></summary>

- $\ce{NH3}$ gains a proton → $\ce{NH4+}$: pair $\ce{NH4+}$ (acid)/$\ce{NH3}$ (base).
- $\ce{H2O}$ loses a proton → $\ce{OH-}$: pair $\ce{H2O}$ (acid)/$\ce{OH-}$ (base).

$\ce{NH3}$ accepted the proton, so it's the base.

**Answer:** Pairs: $\ce{NH4+}$/$\ce{NH3}$ and $\ce{H2O}$/$\ce{OH-}$; $\ce{NH3}$ is the base.

</details>

### Problem 5
Classify each as strong or weak: (a) $\ce{HClO4}$, (b) $\ce{HNO2}$, (c) $\ce{LiOH}$, (d) $\ce{HI}$, (e) $\ce{H2CO3}$.

<details>
<summary><strong>Solution</strong></summary>

- (a) $\ce{HClO4}$ — on the list → **strong acid**
- (b) $\ce{HNO2}$ (nitrous acid — note the "-ous", not nitric) — not on the list → **weak acid**
- (c) $\ce{LiOH}$ — Group 1 hydroxide → **strong base**
- (d) $\ce{HI}$ — on the list → **strong acid**
- (e) $\ce{H2CO3}$ — carbonic acid, not on the list → **weak acid**

**Answer:** (a) strong, (b) weak, (c) strong, (d) strong, (e) weak.

</details>

### Problem 6
Explain the difference between a *strong* acid and a *concentrated* acid, with an example of something that is weak but concentrated.

<details>
<summary><strong>Solution</strong></summary>

**Strong** = the acid dissociates *completely* into ions (a property of the substance). **Concentrated** = there are *many moles* of acid per liter (a property of the solution). They're independent. Glacial (nearly pure) acetic acid is highly **concentrated** but still a **weak** acid — only a small fraction of its molecules ionize at any moment.

**Answer:** Strong describes completeness of dissociation; concentrated describes amount per volume. Concentrated acetic acid is weak-but-concentrated.

</details>

### Problem 7
Write the balanced molecular and the net ionic equation for $\ce{HBr}$ reacting with $\ce{NaOH}$.

<details>
<summary><strong>Solution</strong></summary>

Molecular:
$$\ce{HBr(aq) + NaOH(aq) -> NaBr(aq) + H2O(l)}$$
Both strong and soluble → split all; cancel spectators $\ce{Na+}$ and $\ce{Br-}$:
$$\ce{H+(aq) + OH-(aq) -> H2O(l)}$$

**Answer:** Net ionic: $\ce{H+ + OH- -> H2O}$.

</details>

### Problem 8
Write the net ionic equation for acetic acid, $\ce{CH3COOH}$ (weak), reacting with $\ce{KOH}$ (strong). Explain what stays intact.

<details>
<summary><strong>Solution</strong></summary>

$\ce{KOH}$ is strong → split it. $\ce{CH3COOH}$ is **weak** → keep it whole. The salt $\ce{CH3COOK}$ is soluble → split it. $\ce{K+}$ is the spectator:
$$\ce{CH3COOH(aq) + OH-(aq) -> CH3COO-(aq) + H2O(l)}$$
The weak acid $\ce{CH3COOH}$ stays intact (undissociated); its conjugate base $\ce{CH3COO-}$ appears on the right.

**Answer:** $\ce{CH3COOH + OH- -> CH3COO- + H2O}$; the weak acid stays molecular.

</details>

### Problem 9
Predict the products and write the balanced equation for nitric acid reacting with solid sodium bicarbonate, $\ce{NaHCO3}$.

<details>
<summary><strong>Solution</strong></summary>

Acid + bicarbonate → salt + water + $\ce{CO2}$. Salt pairs $\ce{Na+}$ with $\ce{NO3-}$ → $\ce{NaNO3}$:
$$\ce{NaHCO3(s) + HNO3(aq) -> NaNO3(aq) + H2O(l) + CO2(g)}$$
(Already balanced — 1:1.)

**Answer:** $\ce{NaNO3}$, water, and $\ce{CO2}$ gas.

</details>

### Problem 10
Predict the products and balance: solid zinc dropped into sulfuric acid, $\ce{H2SO4}$.

<details>
<summary><strong>Solution</strong></summary>

Acid + active metal → salt + $\ce{H2}$. Salt pairs $\ce{Zn^2+}$ with $\ce{SO4^2-}$ → $\ce{ZnSO4}$:
$$\ce{Zn(s) + H2SO4(aq) -> ZnSO4(aq) + H2(g)}$$
(Balanced 1:1 since both ion charges are 2.)

**Answer:** $\ce{ZnSO4}$ and hydrogen gas, $\ce{H2}$.

</details>

### Problem 11
Find the pH of a $0.025\ \text{M}$ solution of $\ce{HNO3}$.

<details>
<summary><strong>Solution</strong></summary>

$\ce{HNO3}$ is strong → $[\ce{H+}] = 0.025\ \text{M}$.
$$\text{pH} = -\log(0.025) = 1.60$$

**Answer:** pH $= 1.60$ (strongly acidic).

</details>

### Problem 12
A strong acid solution has pH $= 3.00$. What is $[\ce{H+}]$? What is $[\ce{OH-}]$?

<details>
<summary><strong>Solution</strong></summary>

From $\text{pH} = -\log[\ce{H+}]$: $[\ce{H+}] = 10^{-3.00} = 1.0 \times 10^{-3}\ \text{M}$.
Then $[\ce{OH-}] = \dfrac{1.0\times10^{-14}}{1.0\times10^{-3}} = 1.0 \times 10^{-11}\ \text{M}$.

**Answer:** $[\ce{H+}] = 1.0\times10^{-3}\ \text{M}$, $[\ce{OH-}] = 1.0\times10^{-11}\ \text{M}$.

</details>

### Problem 13
Find the pH of a $0.050\ \text{M}$ solution of $\ce{KOH}$.

<details>
<summary><strong>Solution</strong></summary>

$\ce{KOH}$ is strong → $[\ce{OH-}] = 0.050\ \text{M}$.
$\text{pOH} = -\log(0.050) = 1.30$, so $\text{pH} = 14.00 - 1.30 = 12.70$.

**Answer:** pH $= 12.70$ (strongly basic).

</details>

### Problem 14
Explain why you can calculate the pH of $0.10\ \text{M}\ \ce{HCl}$ in one line, but **not** the pH of $0.10\ \text{M}\ \ce{HF}$ with the same method.

<details>
<summary><strong>Solution</strong></summary>

$\ce{HCl}$ is a **strong** acid, so it fully dissociates: $[\ce{H+}] = 0.10\ \text{M}$ exactly, and $\text{pH} = -\log(0.10) = 1.00$. $\ce{HF}$ is a **weak** acid: only a small fraction ionizes, so $[\ce{H+}] < 0.10\ \text{M}$. You'd need the equilibrium constant $K_a$ and an ICE table to find the actual $[\ce{H+}]$ — that's a Unit 8 calculation.

**Answer:** Strong acids fully dissociate ($[\ce{H+}] =$ concentration); weak acids don't, so they require $K_a$ (Unit 8).

</details>

### Problem 15
$\ce{HCO3-}$ (bicarbonate) is amphoteric. Write one equation where it acts as an acid and one where it acts as a base.

<details>
<summary><strong>Solution</strong></summary>

As an **acid** (donates $\ce{H+}$):
$$\ce{HCO3- -> H+ + CO3^2-}$$
As a **base** (accepts $\ce{H+}$):
$$\ce{HCO3- + H+ -> H2CO3}$$

**Answer:** Acid: $\ce{HCO3- -> H+ + CO3^2-}$; base: $\ce{HCO3- + H+ -> H2CO3}$.

</details>

---

## Quick Reference

| Concept | Key idea |
|---|---|
| Arrhenius acid/base | makes $\ce{H+}$ / makes $\ce{OH-}$ in water |
| Bronsted-Lowry acid/base | proton **donor** / proton **acceptor** (AP-preferred) |
| Conjugate pair | differ by exactly one $\ce{H+}$ (add/remove $\ce{H+}$, shift charge) |
| Amphoteric | can act as acid **or** base (e.g. $\ce{H2O}$, $\ce{HCO3-}$) |
| Strong acids (6) | $\ce{HCl}$, $\ce{HBr}$, $\ce{HI}$, $\ce{HNO3}$, $\ce{H2SO4}$, $\ce{HClO4}$ |
| Strong bases | Group 1 hydroxides + $\ce{Ca(OH)2}$, $\ce{Sr(OH)2}$, $\ce{Ba(OH)2}$ |
| Strong vs weak | full dissociation ($\ce{->}$) vs partial ($\ce{<=>}$) |
| Strong ≠ concentrated | quality (dissociation) vs quantity (moles/L) |
| Neutralization | acid + base → salt + water |
| Strong+strong net ionic | $\ce{H+ + OH- -> H2O}$ (always) |
| Weak acid net ionic | weak acid stays **molecular** (intact) |
| Acid + carbonate | → salt + water + $\ce{CO2}$ |
| Acid + active metal | → salt + $\ce{H2}$ |
| pH | $\text{pH} = -\log[\ce{H+}]$; 0–7 acidic, 7 neutral, 7–14 basic |
| Water constant | $[\ce{H+}][\ce{OH-}] = 1.0\times10^{-14}$; $\text{pH}+\text{pOH}=14$ |
| pH here is | **strong-only**; weak acids need $K_a$ → Unit 8 |

---

<div align="center">

[← Titration](/chemistry/0604-titration) | [Redox Reactions →](/chemistry/0606-redox-reactions)

</div>
