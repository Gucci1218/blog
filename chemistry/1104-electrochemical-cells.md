# Electrochemical Cells
<p class="article-date">July 5, 2026</p>

*My phone hit 3% during lunch and I felt that little jolt of panic we all know. But think about what's actually happening inside that flat little slab: a chemical reaction is running, and it's literally shoving electrons out one terminal, through the phone's circuit, and back in the other terminal. That electron traffic IS the current lighting your screen and playing your music. Here's the secret the whole unit hangs on — a battery is just a redox reaction with its two halves pulled apart and wired together. Normally, when a substance loses electrons and another gains them, the electrons hop straight across, invisibly, and you get nothing useful (that's rusting). But if you physically separate the "loser" from the "gainer" and force the electrons to detour through a wire to get from one to the other, that detour is your circuit — and you can make it do work along the way. Discharging your phone runs a favorable redox reaction downhill to make electricity; plugging in the charger forces the same reaction back uphill with wall power. This is AP Unit 9, Topics 9.7–9.8, and it's where every idea from redox and free energy finally cashes out into something in your pocket.*

---

## What You'll Learn
- Explain how a battery is a redox reaction split into two half-cells, with the electrons forced through an external wire
- Identify the **anode** (oxidation) and **cathode** (reduction) in any cell, and state the direction of electron flow
- Describe the parts of a **galvanic (voltaic) cell** — electrodes, half-cells, wire, and salt bridge — and explain why the salt bridge is essential
- Read and write **line (cell) notation** like $\ce{Zn(s) | Zn^2+(aq) || Cu^2+(aq) | Cu(s)}$
- Use standard reduction potentials to compute $\ce{E^\circ_{cell} = E^\circ_{cathode} - E^\circ_{anode}}$ and decide which species is oxidized vs. reduced
- Connect a **positive** $\ce{E^\circ_{cell}}$ to spontaneity, and know that you never multiply $\ce{E^\circ}$ by stoichiometric coefficients
- Link cell potential to free energy with $\ce{\Delta G^\circ = -nFE^\circ_{cell}}$, and tie $\ce{E^\circ}$, $\ce{\Delta G^\circ}$, and $K$ together in one chain
- Distinguish **galvanic** from **electrolytic** cells, including how the electrode signs flip, and explain how a rechargeable battery does both

---

## Prerequisites
- [Redox Reactions](/chemistry/0606-redox-reactions) — this is the big payoff. You must be fluent in oxidation/reduction, half-reactions, and electron counting, because a cell is a redox reaction with its halves split apart
- [Free Energy and Equilibrium](/chemistry/1103-free-energy-equilibrium) — $\ce{\Delta G^\circ}$ tells you whether a reaction is favorable; here we'll see that favorability is exactly what makes a battery push electrons

---

## The Core Concept

### Intuition First

Let's zoom all the way into your phone battery and rebuild the idea from the apple in [Redox Reactions](/chemistry/0606-redox-reactions).

Remember: a redox reaction is one substance losing electrons while another gains them, always at the same time. When you drop zinc metal into copper solution, zinc's electrons jump *straight onto* the copper ions right there at the metal surface. Electrons transfer, heat comes out, and... that's it. The electrons took the shortest possible path — a millimeter — and you got nothing useful out of the trip. That's a wasted redox reaction, chemistry's version of rust.

Now here's the one clever move that turns that same reaction into a battery: **pull the two halves apart into two separate containers, and make the electrons travel through a wire to get from one to the other.** The zinc still *wants* to hand its electrons to the copper — that hunger doesn't go away just because we moved them apart. But now the only road connecting them runs through your wire. So the electrons are *forced* to march single-file through the circuit, and on the way we make them light up a screen, spin a motor, or charge a friend's phone. **That forced detour through the wire is the current. That current is the whole point.**

So map the phone battery onto the redox vocabulary you already own:

| Battery part | Redox role | What's happening |
|---|---|---|
| The substance losing electrons | **anode** (oxidation) | gives up electrons — the electron *source* |
| The substance gaining electrons | **cathode** (reduction) | accepts electrons — the electron *destination* |
| The electrons' forced detour through the wire | **the current / the work you get out** | this is what powers the phone |
| Discharging (using the phone) | **galvanic cell** | favorable redox running downhill, *making* electricity |
| Charging (plugged into the wall) | **electrolytic cell** | forced back *uphill* by outside power |

That's the entire unit in one table. Everything else — salt bridges, cell notation, cell potentials, $\ce{\Delta G^\circ}$ — is just the machinery that makes this picture precise and lets you calculate exactly how hard the electrons get pushed.

### Redox Recap: Anode, Cathode, and the Direction of Flow

Two half-reactions, same as always. One half *loses* electrons (oxidation), one half *gains* them (reduction). In a cell we give the two electrodes names based on which half happens there:

> **Anode** = the electrode where **oxidation** happens (electrons are lost).
> **Cathode** = the electrode where **reduction** happens (electrons are gained).

The mnemonics that will save you on the exam:

$$\textbf{AN OX} \;:\; \textbf{AN}\text{ode} = \textbf{OX}\text{idation} \qquad \textbf{RED CAT} \;:\; \textbf{RED}\text{uction} = \textbf{CAT}\text{hode}$$

And the direction is fixed, no matter what kind of cell: since the anode is where electrons are *released* and the cathode is where they're *consumed*,

$$\boxed{\text{electrons flow through the wire from } \textbf{anode} \longrightarrow \textbf{cathode}}$$

A memory hook: alphabetically, **A** comes before **C**, and electrons flow **A**node → **C**athode. Vowels **a**node/**o**xidation vs. consonants **c**athode/**r**eduction is another way people keep it straight. Whatever you use, burn in "AN OX, RED CAT" — it's true in *every* cell, galvanic or electrolytic.

### Galvanic (Voltaic) Cells: Harnessing a Favorable Reaction

A **galvanic cell** (also called a **voltaic cell**) is the discharging phone: a spontaneous redox reaction wired up so its electrons do work. The classic textbook example is the **Daniell cell**, built from the zinc/copper reaction you already know:

$$\ce{Zn(s) + Cu^2+(aq) -> Zn^2+(aq) + Cu(s)}$$

Split into halves and put each in its own beaker (each beaker + electrode is a **half-cell**):

- **Anode half-cell (oxidation):** a strip of zinc metal in $\ce{Zn^2+}$ solution. $\quad \ce{Zn(s) -> Zn^2+(aq) + 2e-}$
- **Cathode half-cell (reduction):** a strip of copper metal in $\ce{Cu^2+}$ solution. $\quad \ce{Cu^2+(aq) + 2e- -> Cu(s)}$

Wire the two metal strips (the **electrodes**) together, and electrons flow from the zinc (anode) through the wire to the copper (cathode). At the zinc electrode, atoms dissolve into solution as $\ce{Zn^2+}$, so the zinc strip slowly *shrinks*. At the copper electrode, $\ce{Cu^2+}$ ions grab those arriving electrons and plate out as solid copper, so the copper strip *grows*.

**Why you need a salt bridge.** There's a problem. As zinc dissolves, the anode beaker fills up with extra positive charge ($\ce{Zn^2+}$ ions piling up). As copper plates out, the cathode beaker loses positive charge (its $\ce{Cu^2+}$ is disappearing). Within a fraction of a second, the anode side is too positive and the cathode side is too negative — and that charge imbalance would instantly *stop* the electrons from flowing (they don't want to pile into an already-positive beaker). The reaction chokes itself off.

The **salt bridge** fixes this. It's a tube of inert electrolyte (say $\ce{KNO3}$) connecting the two beakers. It lets *ions* migrate to cancel the buildup: negative ions ($\ce{NO3-}$) drift toward the positive anode side, positive ions ($\ce{K+}$) drift toward the negative cathode side. This keeps both solutions electrically neutral and **completes the circuit** — electrons through the wire, ions through the bridge, current keeps flowing.

> **Two loops make a circuit:** electrons travel through the **wire** (anode → cathode); ions travel through the **solution and salt bridge** to keep both sides neutral. Cut either loop and everything stops.

**Electrode signs (galvanic).** In a galvanic cell the anode is labeled **negative ($-$)** and the cathode **positive ($+$)**. Why? The anode is *pumping electrons out* into the wire, so it's the source of negative charge — the $-$ terminal. The cathode is where electrons are pulled in, so it's the $+$ terminal. (This is literally why your battery has a $+$ end and a $-$ end.)

### Line (Cell) Notation: The Shorthand

Chemists write a whole cell on one line. The convention: **anode on the left, cathode on the right**, in the direction electrons flow.

$$\ce{Zn(s) | Zn^2+(aq) || Cu^2+(aq) | Cu(s)}$$

Reading it left to right:

- **$\ce{Zn(s)}$** — the anode electrode (solid metal).
- **$|$** (single bar) — a **phase boundary**, here between solid zinc and its solution.
- **$\ce{Zn^2+(aq)}$** — the ion in the anode half-cell.
- **$||$** (double bar) — the **salt bridge** separating the two half-cells.
- **$\ce{Cu^2+(aq)}$** — the ion in the cathode half-cell.
- **$|$** — phase boundary between copper solution and the copper electrode.
- **$\ce{Cu(s)}$** — the cathode electrode.

So the line reads: oxidation on the left ($\ce{Zn -> Zn^2+}$), reduction on the right ($\ce{Cu^2+ -> Cu}$). If a half-cell has no solid metal to serve as an electrode (e.g., $\ce{Fe^2+/Fe^3+}$, both dissolved), you use an **inert electrode** like platinum: $\ce{Pt(s) | Fe^2+, Fe^3+ || ...}$.

### Standard Reduction Potentials: Ranking the Hunger for Electrons

How do we *predict* which metal becomes the anode and which the cathode, and how hard the electrons get pushed? We use a table of **standard reduction potentials ($\ce{E^\circ}$)**. Every half-reaction is written as a *reduction* and given a voltage measured against a reference (the standard hydrogen electrode, defined as exactly $0.00\ \text{V}$). A few from the table:

| Reduction half-reaction | $\ce{E^\circ}$ (V) |
|---|---|
| $\ce{F2 + 2e- -> 2F-}$ | $+2.87$ |
| $\ce{Ag+ + e- -> Ag}$ | $+0.80$ |
| $\ce{Cu^2+ + 2e- -> Cu}$ | $+0.34$ |
| $\ce{2H+ + 2e- -> H2}$ | $0.00$ |
| $\ce{Ni^2+ + 2e- -> Ni}$ | $-0.25$ |
| $\ce{Zn^2+ + 2e- -> Zn}$ | $-0.76$ |
| $\ce{Al^3+ + 3e- -> Al}$ | $-1.66$ |
| $\ce{Li+ + e- -> Li}$ | $-3.04$ |

**The intuition:** $\ce{E^\circ}$ measures how badly a species *wants to be reduced* (to grab electrons). A big positive number = electron-hungry (fluorine, silver want electrons badly). A big negative number = electron-happy to *give them up* (lithium would rather be oxidized — which is exactly why lithium is a great battery anode).

**The rule for building a spontaneous cell:** the species with the **higher reduction potential wins the tug-of-war and gets reduced → it's the cathode.** The other one is forced to run backward (oxidation) → it's the anode. Between zinc ($-0.76$) and copper ($+0.34$), copper's potential is higher, so copper gets reduced (cathode) and zinc gets oxidized (anode). Exactly the Daniell cell.

**The reliable formula** (both values taken straight from the table as reduction potentials):

$$\boxed{\ce{E^\circ_{cell} = E^\circ_{cathode} - E^\circ_{anode}}}$$

For zinc/copper: $\ce{E^\circ_{cell}} = (+0.34) - (-0.76) = +1.10\ \text{V}$. A **positive $\ce{E^\circ_{cell}}$ means the cell is galvanic — the reaction is spontaneous** and will push electrons on its own. If you get a negative number, you assigned the electrodes backward (or the reaction as written is nonspontaneous and needs to be *forced* — that's electrolysis).

**The intensive-property trap.** Voltage is an **intensive** property — it does *not* depend on how much stuff you have. If you double a half-reaction to balance electrons, you do **NOT** double its $\ce{E^\circ}$. Ten AA batteries in a pile each still read 1.5 V; stacking them in *series* adds voltage, but scaling a chemical equation on paper never does. So when you multiply $\ce{Zn -> Zn^2+ + 2e-}$ by 3 to match electrons with an aluminum half-reaction, $\ce{E^\circ}$ stays put. **Never multiply $\ce{E^\circ}$ by a coefficient.**

### The Link to Free Energy: Where E°, ΔG°, and K All Meet

Back in [Free Energy and Equilibrium](/chemistry/1103-free-energy-equilibrium) you learned that $\ce{\Delta G^\circ}$ is the real judge of favorability: negative means spontaneous. Cell potential is just *the same information wearing a different outfit*. The bridge equation:

$$\boxed{\ce{\Delta G^\circ = -nFE^\circ_{cell}}}$$

where $n$ = moles of electrons transferred in the balanced reaction, and $F$ = **Faraday's constant** $= 96{,}485\ \text{C/mol e}^-$ (the charge on one mole of electrons). Because $n$ and $F$ are always positive, the *minus sign* does all the work:

$$\ce{E^\circ_{cell}} > 0 \;\;\Longleftrightarrow\;\; \ce{\Delta G^\circ} < 0 \;\;\Longleftrightarrow\;\; \textbf{spontaneous (galvanic)}$$

$$\ce{E^\circ_{cell}} < 0 \;\;\Longleftrightarrow\;\; \ce{\Delta G^\circ} > 0 \;\;\Longleftrightarrow\;\; \textbf{nonspontaneous (needs electrolysis)}$$

A positive voltage and a negative free energy are literally the same statement — one in volts, one in joules.

And it all interlocks with the equilibrium constant, because from Unit 8 you also have $\ce{\Delta G^\circ = -RT\ln K}$. Set the two expressions for $\ce{\Delta G^\circ}$ equal and you get a three-way bridge among $\ce{E^\circ}$, $\ce{\Delta G^\circ}$, and $K$:

$$-nF\ce{E^\circ_{cell}} = \ce{\Delta G^\circ} = -RT\ln K$$

So a positive $\ce{E^\circ}$ forces $\ce{\Delta G^\circ} < 0$ *and* $K > 1$ — the reaction favors products, releases energy, and pushes electrons. Three descriptions, one reality. (Example 8 walks the full chain end to end.)

### Electrolytic Cells: Forcing the Reaction Uphill

What if a reaction is *nonspontaneous* ($\ce{E^\circ_{cell} < 0}$, $\ce{\Delta G^\circ > 0}$)? It won't run on its own — but you can *force* it by plugging in an external power source that shoves electrons the wrong way. That's an **electrolytic cell**, and it's exactly what happens when you charge your phone: wall power pushes the battery's reaction back uphill, un-doing the discharge and reloading the chemistry so you can use it again.

Key contrasts with a galvanic cell:

- **Energy direction:** galvanic *releases* electrical energy; electrolytic *consumes* it from an outside source (the charger, a battery, a power supply).
- **Electrode signs flip.** In an electrolytic cell the power supply makes the anode **positive ($+$)** and the cathode **negative ($-$)** — the opposite of galvanic. The external source is pulling electrons *out* of the anode (so it's forced positive) and cramming them *into* the cathode (forced negative).
- **But the chemistry labels do NOT flip.** Oxidation *always* happens at the anode; reduction *always* at the cathode; electrons *always* flow anode → cathode. Those never change — only the $+/-$ signs do.

**Rechargeable batteries do both.** Your phone's lithium-ion battery is a galvanic cell while you use it (discharging, making electricity) and an electrolytic cell while it charges (forced backward by the wall). The *same* electrode is the anode during discharge and the cathode during charge — which is exactly why textbooks tell you to always define anode/cathode by *oxidation/reduction*, never by a fixed physical side.

Here's the master comparison:

| Feature | Galvanic (voltaic) cell | Electrolytic cell |
|---|---|---|
| Spontaneous? | Yes ($\ce{\Delta G^\circ} < 0$) | No ($\ce{\Delta G^\circ} > 0$) |
| $\ce{E^\circ_{cell}}$ | Positive ($> 0$) | Negative ($< 0$) |
| Energy | **Produces** electricity | **Consumes** electricity from an external source |
| Anode | Oxidation, labeled **$-$** | Oxidation, labeled **$+$** |
| Cathode | Reduction, labeled **$+$** | Reduction, labeled **$-$** |
| Electron flow | Anode → cathode | Anode → cathode |
| Phone analogy | **Discharging** (using it) | **Charging** (plugged in) |
| Example | Daniell cell; a battery running | Charging a battery; electroplating |

Notice the only rows that actually flip are "spontaneous," "$\ce{E^\circ}$ sign," "energy," and the electrode *signs*. Oxidation-at-anode and anode→cathode electron flow are rock-solid in both.

> **🎬 Hollywood Chemistry: Real or Not? — The Desert Battery**
> *The scene:* Stranded in the desert with a dead RV, a high-school chemistry teacher builds a battery from spare parts — a hunk of galvanized (zinc-coated) metal, some graphite, mercuric oxide, and a sponge soaked in electrolyte — to jump-start the engine.
> *The verdict:* **The concept is completely real.** He's building a **galvanic cell**, and a galvanic cell *is* a battery: two dissimilar materials (the zinc as the electron-losing anode, the mercuric oxide/graphite as the electron-gaining cathode) plus an electrolyte to carry ions and complete the circuit. Zinc's very negative reduction potential ($-0.76\ \text{V}$) makes it a textbook anode — the same reason it's in real dry cells — and the scene is honestly a beautiful illustration of anode, cathode, and electron flow. **But the drama is exaggerated.** A hand-assembled cell like that puts out a trickle: enough for a small voltage and a few milliamps, nowhere near the *hundreds of cranking amps* a starter motor demands to turn over an engine. The chemistry is legit; the "and it roars to life" ending is Hollywood. *(Compare Senku in* Dr. Stone*, who builds a battery from copper, zinc, and salt water to restart civilization — same from-scratch galvanic-cell idea, and refreshingly, the anime keeps the output realistically feeble.)*

---

## Worked Examples

### Example 1: Identify Anode, Cathode, and Electron Flow

**Problem:** A cell is built from nickel and silver: $\ce{Ni(s) + 2Ag+(aq) -> Ni^2+(aq) + 2Ag(s)}$. Which electrode is the anode, which is the cathode, and which way do electrons flow?

**Solution:**

**Step 1:** Assign oxidation numbers. $\ce{Ni}$ goes $0 \to +2$ (loses electrons → oxidized). $\ce{Ag+}$ goes $+1 \to 0$ (gains electrons → reduced).

**Step 2:** Apply AN OX / RED CAT. Nickel is oxidized → nickel is the **anode**. Silver is reduced → silver is the **cathode**.

**Step 3:** Electrons always flow anode → cathode.

**Answer:** **Anode: $\ce{Ni}$. Cathode: $\ce{Ag}$.** Electrons flow through the wire from the nickel electrode to the silver electrode.

### Example 2: Which Species Gets Reduced?

**Problem:** You have $\ce{Ni^2+/Ni}$ ($\ce{E^\circ} = -0.25\ \text{V}$) and $\ce{Cu^2+/Cu}$ ($\ce{E^\circ} = +0.34\ \text{V}$). If you build a spontaneous cell, which metal is the cathode?

**Solution:**

**Step 1:** The higher reduction potential wins the electrons and gets reduced. Copper's $+0.34 >$ nickel's $-0.25$.

**Step 2:** So copper is reduced → copper is the cathode; nickel is forced to oxidize → nickel is the anode.

**Answer:** **Copper is the cathode** (reduced); nickel is the anode (oxidized).

### Example 3: Compute E°cell

**Problem:** Find $\ce{E^\circ_{cell}}$ for the zinc/silver cell. Use $\ce{E^\circ(Ag+/Ag)} = +0.80\ \text{V}$ and $\ce{E^\circ(Zn^2+/Zn)} = -0.76\ \text{V}$.

**Solution:**

**Step 1:** Silver's potential is higher → silver is reduced (cathode); zinc is oxidized (anode).

**Step 2:** Apply $\ce{E^\circ_{cell} = E^\circ_{cathode} - E^\circ_{anode}}$, using both as reduction potentials straight from the table:

$$\ce{E^\circ_{cell}} = (+0.80) - (-0.76) = +1.56\ \text{V}$$

**Answer:** $\ce{E^\circ_{cell}} = +1.56\ \text{V}$. Positive → the cell is galvanic and spontaneous.

### Example 4: The Intensive-Property Trap

**Problem:** For the zinc/silver cell above, the balanced reaction is $\ce{Zn + 2Ag+ -> Zn^2+ + 2Ag}$ — silver's half-reaction had to be doubled to balance electrons. Does doubling it change $\ce{E^\circ_{cell}}$?

**Solution:**

**Step 1:** You *do* double the silver half-reaction ($\ce{2Ag+ + 2e- -> 2Ag}$) to match zinc's 2 electrons. But $\ce{E^\circ}$ is **intensive** — it doesn't scale with amount.

**Step 2:** So $\ce{E^\circ(Ag+/Ag)}$ stays $+0.80\ \text{V}$, not $+1.60$. The cell potential is still $(+0.80) - (-0.76) = +1.56\ \text{V}$, exactly as in Example 3.

**Answer:** **No.** $\ce{E^\circ_{cell}} = +1.56\ \text{V}$ regardless of coefficients. Never multiply $\ce{E^\circ}$ by a stoichiometric coefficient.

### Example 5: Predict Spontaneity from E°

**Problem:** Is the reaction $\ce{Cu(s) + Zn^2+(aq) -> Cu^2+(aq) + Zn(s)}$ spontaneous under standard conditions?

**Solution:**

**Step 1:** As written, copper is oxidized (anode) and zinc is reduced (cathode). So $\ce{E^\circ_{cathode}} = \ce{E^\circ(Zn^2+/Zn)} = -0.76$ and $\ce{E^\circ_{anode}} = \ce{E^\circ(Cu^2+/Cu)} = +0.34$.

**Step 2:** $\ce{E^\circ_{cell}} = (-0.76) - (+0.34) = -1.10\ \text{V}$.

**Answer:** Negative $\ce{E^\circ_{cell}}$ → **nonspontaneous.** This is just the Daniell cell run backward; it only happens if you force it (electrolysis). The spontaneous direction is the reverse ($+1.10\ \text{V}$).

### Example 6: Line Notation

**Problem:** Write the line notation for a cell where aluminum is oxidized and $\ce{Cu^2+}$ is reduced.

**Solution:**

**Step 1:** Anode (oxidation) goes on the left: $\ce{Al(s) | Al^3+(aq)}$. Cathode (reduction) on the right: $\ce{Cu^2+(aq) | Cu(s)}$.

**Step 2:** Separate the half-cells with the salt-bridge double bar, and put single bars at each solid–solution phase boundary.

**Answer:** $\ce{Al(s) | Al^3+(aq) || Cu^2+(aq) | Cu(s)}$.

### Example 7: ΔG° from E°

**Problem:** Compute $\ce{\Delta G^\circ}$ for the Daniell cell: $\ce{Zn + Cu^2+ -> Zn^2+ + Cu}$, $\ce{E^\circ_{cell}} = +1.10\ \text{V}$. Use $F = 96{,}485\ \text{C/mol}$.

**Solution:**

**Step 1:** Count electrons transferred. Zinc gives 2, copper takes 2 → $n = 2$.

**Step 2:** Apply $\ce{\Delta G^\circ = -nFE^\circ_{cell}}$:

$$\ce{\Delta G^\circ} = -(2)(96{,}485)(1.10) = -212{,}267\ \text{J} \approx -212\ \text{kJ}$$

**Answer:** $\ce{\Delta G^\circ} \approx -212\ \text{kJ/mol}$. Negative $\ce{\Delta G^\circ}$ confirms spontaneous — the same verdict the positive voltage gave (a volt-coulomb is a joule, so the units work out to joules).

### Example 8: The Full E° → ΔG° → K Chain

**Problem:** A cell has $\ce{E^\circ_{cell}} = +0.46\ \text{V}$ with $n = 2$ at $298\ \text{K}$. Find $\ce{\Delta G^\circ}$ and the equilibrium constant $K$. Use $R = 8.314\ \text{J/mol·K}$.

**Solution:**

**Step 1 — $\ce{E^\circ} \to \ce{\Delta G^\circ}$:**

$$\ce{\Delta G^\circ} = -nF\ce{E^\circ} = -(2)(96{,}485)(0.46) = -88{,}766\ \text{J} \approx -88.8\ \text{kJ}$$

**Step 2 — $\ce{\Delta G^\circ} \to K$** via $\ce{\Delta G^\circ = -RT\ln K}$, so $\ln K = -\ce{\Delta G^\circ}/RT$:

$$\ln K = \frac{-(-88{,}766)}{(8.314)(298)} = \frac{88{,}766}{2477.6} = 35.8$$

**Step 3:** $K = e^{35.8} \approx 3.5 \times 10^{15}$.

**Answer:** $\ce{\Delta G^\circ} \approx -88.8\ \text{kJ}$ and $K \approx 3.5 \times 10^{15}$. Positive $\ce{E^\circ}$ → negative $\ce{\Delta G^\circ}$ → huge $K$: all three say "products strongly favored, spontaneous." One reality, three languages.

### Example 9: Galvanic vs. Electrolytic Classification

**Problem:** A cell forces $\ce{2H2O -> 2H2 + O2}$ (splitting water), which has $\ce{E^\circ_{cell}} = -1.23\ \text{V}$. Is this galvanic or electrolytic? What signs are the electrodes?

**Solution:**

**Step 1:** $\ce{E^\circ_{cell}} < 0$ → nonspontaneous → it must be driven by an external power source → **electrolytic cell**.

**Step 2:** In an electrolytic cell the electrode signs flip: anode is **$+$**, cathode is **$-$**. Oxidation still happens at the anode (here $\ce{O2}$ is produced), reduction at the cathode ($\ce{H2}$).

**Answer:** **Electrolytic.** Anode $= +$ (oxidation, $\ce{O2}$), cathode $= -$ (reduction, $\ce{H2}$). This is electrolysis of water.

### Example 10: Electrode Signs in a Galvanic Cell

**Problem:** In the zinc/copper Daniell cell (galvanic, $+1.10\ \text{V}$), which electrode is the $+$ terminal and which is the $-$ terminal?

**Solution:**

**Step 1:** Zinc is the anode (oxidation), copper is the cathode (reduction).

**Step 2:** In a *galvanic* cell the anode is $-$ (it pumps electrons out) and the cathode is $+$ (electrons pour in).

**Answer:** **Zinc (anode) is the $-$ terminal; copper (cathode) is the $+$ terminal.** This is why the copper end would be the "positive terminal" if you wired this cell to a device.

### Example 11: Rechargeable Battery — Both Cells

**Problem:** A phone battery discharges while you scroll, then charges overnight. Classify each phase as galvanic or electrolytic, and describe the energy flow.

**Solution:**

**Step 1 — Discharging (using the phone):** the spontaneous redox reaction runs downhill and pushes electrons through the phone. Spontaneous, produces electricity → **galvanic cell**.

**Step 2 — Charging (plugged into the wall):** the charger forces the reaction backward, uphill, using external energy. Nonspontaneous, consumes electricity → **electrolytic cell**.

**Answer:** Discharge = **galvanic** (chemical → electrical, powers the phone); charge = **electrolytic** (electrical → chemical, reloads the battery). The same battery is both, depending on which way the electrons are being pushed.

### Example 12: Building the Most Powerful Cell

**Problem:** From lithium ($\ce{E^\circ} = -3.04$), zinc ($-0.76$), and fluorine ($+2.87$), which pair gives the largest $\ce{E^\circ_{cell}}$, and what is it?

**Solution:**

**Step 1:** To maximize $\ce{E^\circ_{cell} = E^\circ_{cathode} - E^\circ_{anode}}$, pick the highest potential as the cathode and the lowest as the anode. Cathode = fluorine ($+2.87$); anode = lithium ($-3.04$).

**Step 2:** $\ce{E^\circ_{cell}} = (+2.87) - (-3.04) = +5.91\ \text{V}$.

**Answer:** **Lithium anode + fluorine cathode**, giving $\ce{E^\circ_{cell}} = +5.91\ \text{V}$. This is why lithium (very negative $\ce{E^\circ}$, eager to give up electrons) is the star of high-energy batteries.

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Multiplying $\ce{E^\circ}$ by a coefficient when balancing electrons | Everything *else* scales, so it feels like $\ce{E^\circ}$ should too | $\ce{E^\circ}$ is **intensive** — voltage never depends on amount. Balance electrons, but leave $\ce{E^\circ}$ alone |
| Using $\ce{E^\circ_{cell} = E^\circ_{cathode} + E^\circ_{anode}}$ or flipping a sign | Half-remembered formulas | Memorize one reliable form: **cathode minus anode, both as reduction potentials from the table** |
| Thinking the anode is always $-$ | True for galvanic, drilled in early | Signs **flip** in electrolytic cells (anode $+$). Only oxidation-at-anode and anode→cathode flow are universal |
| Saying "the cathode is always the positive side of a battery" | Discharge experience | During *charging* (electrolytic) the same electrode is now negative. Define anode/cathode by oxidation/reduction, not by a fixed side |
| Forgetting why the salt bridge exists | It looks like a decorative tube | It maintains **charge neutrality** and **completes the circuit** by letting ions migrate. Without it, current stops in a fraction of a second |
| Mixing up the electron road and the ion road | Two things moving at once | **Electrons** move through the **wire**; **ions** move through **solution + salt bridge**. Electrons never travel through the solution |
| Getting the $\ce{\Delta G^\circ}$ sign backward | Forgetting the minus sign | $\ce{\Delta G^\circ = -nFE^\circ}$ — the minus flips the sign, so $\ce{E^\circ} > 0$ gives $\ce{\Delta G^\circ} < 0$ (spontaneous) |
| Writing line notation with cathode on the left | Reading habits vary | Convention is **anode `|` ... `||` ... `|` cathode** — oxidation on the left, reduction on the right |

---

## AP Exam Tips

- **Commit the master formula to memory: $\ce{E^\circ_{cell} = E^\circ_{cathode} - E^\circ_{anode}}$**, using both values as reduction potentials straight off the table. This is the single most reliable version — you never have to reverse a sign for the anode reaction.
- **Never multiply $\ce{E^\circ}$ by a stoichiometric coefficient.** Graders specifically look for this. Voltage is intensive; scaling a half-reaction to balance electrons does not scale its potential.
- **Know the $\ce{\Delta G^\circ = -nFE^\circ}$ sign logic cold.** $\ce{E^\circ} > 0 \Leftrightarrow \ce{\Delta G^\circ} < 0 \Leftrightarrow$ spontaneous (galvanic). $F = 96{,}485\ \text{C/mol e}^-$ is on the formula sheet; $n$ = moles of electrons in the balanced reaction.
- **Be ready to explain the salt bridge in words.** A classic free-response asks *why* it's needed: to maintain electrical neutrality in the half-cells and complete the circuit so current keeps flowing. "Allows ion flow" alone may not earn the point — say it keeps the solutions neutral.
- **Galvanic vs. electrolytic electrode signs are a favorite trap.** Remember: oxidation is *always* at the anode and electrons *always* flow anode → cathode, in **both** cell types. Only the $+/-$ labels flip (galvanic: anode $-$, cathode $+$; electrolytic: anode $+$, cathode $-$).
- **Positive $\ce{E^\circ_{cell}}$ = spontaneous = galvanic.** If your calculation comes out negative, you either assigned the electrodes backward or the reaction genuinely needs to be forced (electrolysis). Use the sign as a built-in check.
- **When they give you a table, the higher reduction potential gets reduced (cathode).** Use this to decide the electrodes *before* plugging into the formula.

---

## Practice Problems

### Problem 1
In a cell running $\ce{Mg(s) + Fe^2+(aq) -> Mg^2+(aq) + Fe(s)}$, identify the anode, the cathode, and the direction of electron flow.

<details>
<summary><strong>Solution</strong></summary>

$\ce{Mg}$: $0 \to +2$ (oxidized → **anode**). $\ce{Fe^2+}$: $+2 \to 0$ (reduced → **cathode**). Electrons flow anode → cathode.

**Answer:** Anode = $\ce{Mg}$, cathode = $\ce{Fe}$; electrons flow from magnesium to iron through the wire.

</details>

### Problem 2
Using $\ce{E^\circ(Cu^2+/Cu)} = +0.34\ \text{V}$ and $\ce{E^\circ(Ni^2+/Ni)} = -0.25\ \text{V}$, compute $\ce{E^\circ_{cell}}$ for the spontaneous cell and state which metal is oxidized.

<details>
<summary><strong>Solution</strong></summary>

Higher potential (copper) is reduced → cathode; nickel is oxidized → anode.

$$\ce{E^\circ_{cell}} = (+0.34) - (-0.25) = +0.59\ \text{V}$$

**Answer:** $\ce{E^\circ_{cell}} = +0.59\ \text{V}$; nickel is oxidized.

</details>

### Problem 3
Write the line notation for a cell in which magnesium is the anode and $\ce{Ag+}$ is reduced at a silver cathode.

<details>
<summary><strong>Solution</strong></summary>

Anode left, cathode right, salt-bridge double bar between:

**Answer:** $\ce{Mg(s) | Mg^2+(aq) || Ag+(aq) | Ag(s)}$.

</details>

### Problem 4
Explain in one or two sentences why a galvanic cell will not keep running if you remove the salt bridge.

<details>
<summary><strong>Solution</strong></summary>

As oxidation adds positive ions to the anode side and reduction removes them from the cathode side, charge builds up in each half-cell. Without the salt bridge to let ions migrate and restore neutrality, this charge imbalance halts electron flow almost immediately.

**Answer:** The salt bridge maintains charge neutrality and completes the circuit; without it, charge buildup stops the current.

</details>

### Problem 5
For a cell with $\ce{E^\circ_{cell}} = +0.80\ \text{V}$ and $n = 2$, calculate $\ce{\Delta G^\circ}$ in kJ. ($F = 96{,}485\ \text{C/mol}$.)

<details>
<summary><strong>Solution</strong></summary>

$$\ce{\Delta G^\circ} = -nF\ce{E^\circ} = -(2)(96{,}485)(0.80) = -154{,}376\ \text{J} \approx -154\ \text{kJ}$$

**Answer:** $\ce{\Delta G^\circ} \approx -154\ \text{kJ}$ (spontaneous, as expected from the positive voltage).

</details>

### Problem 6
A reaction has $\ce{E^\circ_{cell}} = -0.62\ \text{V}$. Is it galvanic or electrolytic? Is $\ce{\Delta G^\circ}$ positive or negative?

<details>
<summary><strong>Solution</strong></summary>

Negative $\ce{E^\circ_{cell}}$ → nonspontaneous → **electrolytic** (must be forced). By $\ce{\Delta G^\circ = -nFE^\circ}$, a negative $\ce{E^\circ}$ makes $\ce{\Delta G^\circ}$ **positive**.

**Answer:** Electrolytic; $\ce{\Delta G^\circ} > 0$.

</details>

### Problem 7
In an electrolytic cell used for electroplating, which electrode (anode or cathode) is positive, and where does oxidation occur?

<details>
<summary><strong>Solution</strong></summary>

In an electrolytic cell the external source makes the anode **positive** and the cathode negative. Oxidation always occurs at the anode, regardless of cell type.

**Answer:** The anode is positive; oxidation occurs at the anode.

</details>

### Problem 8
The balanced cell reaction $\ce{2Al + 3Cu^2+ -> 2Al^3+ + 3Cu}$ was built by tripling the copper half-reaction. Given $\ce{E^\circ(Cu^2+/Cu)} = +0.34$ and $\ce{E^\circ(Al^3+/Al)} = -1.66$, find $\ce{E^\circ_{cell}}$.

<details>
<summary><strong>Solution</strong></summary>

Copper reduced (cathode), aluminum oxidized (anode). Do **not** multiply $\ce{E^\circ}$ by 3 — it's intensive.

$$\ce{E^\circ_{cell}} = (+0.34) - (-1.66) = +2.00\ \text{V}$$

**Answer:** $\ce{E^\circ_{cell}} = +2.00\ \text{V}$ (coefficients don't change $\ce{E^\circ}$).

</details>

### Problem 9
Read the cell $\ce{Fe(s) | Fe^2+(aq) || Ag+(aq) | Ag(s)}$. Identify the anode, cathode, and the overall reaction.

<details>
<summary><strong>Solution</strong></summary>

Left = anode: $\ce{Fe -> Fe^2+ + 2e-}$. Right = cathode: $\ce{Ag+ + e- -> Ag}$ (double it to match 2 electrons).

Overall: $\ce{Fe + 2Ag+ -> Fe^2+ + 2Ag}$.

**Answer:** Anode = $\ce{Fe}$, cathode = $\ce{Ag}$; overall $\ce{Fe + 2Ag+ -> Fe^2+ + 2Ag}$.

</details>

### Problem 10
A galvanic cell has $\ce{E^\circ_{cell}} = +1.56\ \text{V}$ with $n = 2$. Find $K$ at $298\ \text{K}$. ($R = 8.314$, $F = 96{,}485$.)

<details>
<summary><strong>Solution</strong></summary>

$\ce{\Delta G^\circ} = -(2)(96{,}485)(1.56) = -301{,}033\ \text{J}$.

$\ln K = -\ce{\Delta G^\circ}/RT = 301{,}033 / [(8.314)(298)] = 301{,}033/2477.6 = 121.5$.

$K = e^{121.5}$ — astronomically large ($\sim 10^{52}$).

**Answer:** $K \approx e^{121.5} \approx 10^{52}$; essentially goes to completion.

</details>

### Problem 11
Map each phone action to a cell type: (a) watching a video until the battery drains; (b) plugging into the wall to charge.

<details>
<summary><strong>Solution</strong></summary>

(a) Draining = spontaneous redox producing electricity → **galvanic cell**. (b) Charging = external power forcing the reaction backward → **electrolytic cell**.

**Answer:** (a) galvanic; (b) electrolytic.

</details>

### Problem 12
Which way do electrons flow in an *electrolytic* cell — anode to cathode, or cathode to anode? Explain.

<details>
<summary><strong>Solution</strong></summary>

Electrons flow **anode → cathode** in *every* cell, galvanic or electrolytic. Oxidation (electron release) is at the anode and reduction (electron consumption) is at the cathode, so electrons always leave the anode and arrive at the cathode. Only the electrode *signs* differ between cell types.

**Answer:** Anode → cathode (same as galvanic; only the $+/-$ signs flip).

</details>

### Problem 13
Given $\ce{E^\circ(Zn^2+/Zn)} = -0.76$ and $\ce{E^\circ(Fe^2+/Fe)} = -0.44$, decide whether $\ce{Zn(s) + Fe^2+(aq) -> Zn^2+(aq) + Fe(s)}$ is spontaneous.

<details>
<summary><strong>Solution</strong></summary>

As written, iron is reduced (cathode), zinc oxidized (anode).

$$\ce{E^\circ_{cell}} = \ce{E^\circ_{cathode}} - \ce{E^\circ_{anode}} = (-0.44) - (-0.76) = +0.32\ \text{V}$$

Positive → spontaneous.

**Answer:** Spontaneous ($\ce{E^\circ_{cell}} = +0.32\ \text{V}$). Zinc's more negative potential makes it the natural anode — which is exactly why zinc coatings sacrificially protect iron from rusting.

</details>

### Problem 14
For the desert-battery scene, the teacher pairs zinc with a much higher-potential cathode material. In redox terms, which electrode is oxidized, which sign is it in the working (galvanic) battery, and what carries charge between the electrodes?

<details>
<summary><strong>Solution</strong></summary>

Zinc has a very negative reduction potential, so it is **oxidized** → it's the **anode**. In a working (galvanic) cell the anode is the **negative ($-$)** terminal. Inside the cell, the electrolyte-soaked sponge lets **ions** migrate to complete the circuit while electrons travel through the external wire.

**Answer:** Zinc is oxidized (anode, $-$ terminal); the electrolyte carries ions to complete the circuit. (Real chemistry — though the current is far too small to actually crank an engine.)

</details>

### Problem 15
A cell has $\ce{\Delta G^\circ} = -395\ \text{kJ}$ and transfers $n = 4$ electrons. Find $\ce{E^\circ_{cell}}$. ($F = 96{,}485$.)

<details>
<summary><strong>Solution</strong></summary>

Rearrange $\ce{\Delta G^\circ = -nFE^\circ}$ to $\ce{E^\circ} = -\ce{\Delta G^\circ}/(nF)$. Use joules: $\ce{\Delta G^\circ} = -395{,}000\ \text{J}$.

$$\ce{E^\circ_{cell}} = \frac{-(-395{,}000)}{(4)(96{,}485)} = \frac{395{,}000}{385{,}940} = +1.02\ \text{V}$$

**Answer:** $\ce{E^\circ_{cell}} \approx +1.02\ \text{V}$ (positive, consistent with the negative $\ce{\Delta G^\circ}$).

</details>

---

## Quick Reference

**The big idea:** a battery is a redox reaction with its two halves pulled apart, so electrons are forced through a wire — and that flow is the current.

$$\textbf{AN OX} \;:\; \text{Anode} = \text{Oxidation} \qquad \textbf{RED CAT} \;:\; \text{Reduction} = \text{Cathode}$$

$$\text{Electrons always flow: } \textbf{anode} \longrightarrow \textbf{cathode}$$

**Cell potential:**

$$\ce{E^\circ_{cell} = E^\circ_{cathode} - E^\circ_{anode}} \quad (\text{both as reduction potentials})$$

- Higher reduction potential → gets reduced → **cathode**.
- **Never** multiply $\ce{E^\circ}$ by a coefficient (intensive).
- $\ce{E^\circ_{cell}} > 0$ → galvanic / spontaneous.

**Line notation:** $\ce{anode | anode ion || cathode ion | cathode}$, e.g. $\ce{Zn(s) | Zn^2+(aq) || Cu^2+(aq) | Cu(s)}$.

**The free-energy bridge** ($F = 96{,}485\ \text{C/mol e}^-$):

$$\ce{\Delta G^\circ = -nFE^\circ_{cell}} \qquad -nF\ce{E^\circ_{cell}} = \ce{\Delta G^\circ} = -RT\ln K$$

$$\ce{E^\circ} > 0 \;\Leftrightarrow\; \ce{\Delta G^\circ} < 0 \;\Leftrightarrow\; K > 1 \;\Leftrightarrow\; \textbf{spontaneous}$$

**Galvanic vs. electrolytic:**

| | Galvanic | Electrolytic |
|---|---|---|
| Spontaneous? | Yes ($\ce{E^\circ} > 0$) | No ($\ce{E^\circ} < 0$) |
| Energy | Produces electricity | Consumes electricity |
| Anode sign | $-$ | $+$ |
| Cathode sign | $+$ | $-$ |
| Phone | Discharging | Charging |

**Universal in both:** oxidation at the anode, reduction at the cathode, electrons flow anode → cathode. Only the $+/-$ signs flip.

**Salt bridge:** maintains charge neutrality in each half-cell and completes the circuit by letting ions migrate.

---

<div align="center">

[← Free Energy and Equilibrium](/chemistry/1103-free-energy-equilibrium) | [Cell Potential and Electrolysis →](/chemistry/1105-cell-potential-electrolysis)

</div>
