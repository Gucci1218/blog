# Solubility and Separations
<p class="article-date">July 5, 2026</p>

*Two kitchen experiments taught me this whole topic before I ever opened the textbook. First: I made salad dressing. Oil, vinegar, a pinch of salt — shake the jar hard and for about three seconds it looks like one cloudy liquid. Set it on the counter, count to thirty, and it splits back into two clean layers, oil floating on vinegar, every single time. But earlier that day I'd stirred sugar into iced tea and it vanished for good — it has NEVER once un-dissolved and settled back out. Same jar, same spoon, opposite endings. Second experiment, later that night: I drew a fat black dot on a coffee filter with a washable marker, stood the paper edge-down in a little water, and watched the "black" crawl upward and fan out into blue, then pink, then yellow bands, each racing up the paper at its own speed. The black was a lie — it was three pigments hiding together the whole time. Those two things — why oil refuses to mix while sugar mixes forever, and why "black" ink walks up wet paper and separates itself — are the exact same idea seen twice. It's all about which molecules grip which, and it's the heart of AP Chemistry Unit 3, Topics 3.9 and 3.10: solubility and separations.*

---

## What You'll Learn
- State and apply the **"like dissolves like"** rule using intermolecular forces (IMFs) as the *reason*, not just a slogan
- Predict whether a given solute (salt, sugar, $\ce{I2}$, oil, ethanol) dissolves in a **polar** solvent like water or a **nonpolar** solvent like hexane
- Explain why oil and water form separate layers, and tell **miscible** from **immiscible** liquids
- Explain how **soap and surfactants** bridge polar and nonpolar worlds to wash away grease
- Predict how **temperature** changes solubility — and why solids and gases respond in *opposite* directions
- Read a **solubility curve** to find how much dissolves at a temperature and classify a solution as saturated, unsaturated, or supersaturated
- Use **Henry's law** qualitatively to explain gas solubility and pressure (the soda-can fizz)
- Choose the right **separation technique** — filtration, distillation, or chromatography — and justify it with particle size, boiling point, or IMFs
- Calculate and interpret a **retention factor** $R_f = \dfrac{\text{distance traveled by spot}}{\text{distance traveled by solvent}}$

---

## Prerequisites
- [Intermolecular Forces](/chemistry/0501-intermolecular-forces) — the whole article rests on comparing London dispersion, dipole-dipole, hydrogen bonding, and ion-dipole attractions
- [Solutions and Concentration](/chemistry/0506-solutions-and-concentration) — you need "solute," "solvent," and "saturated" before we can bend those ideas

---

## The Core Concept

### Intuition First

Go back to the salad-dressing jar. Why does sugar disappear into tea forever while oil bounces right back out of vinegar?

Every liquid and every solute is a crowd of molecules holding hands with their neighbors through intermolecular forces. Water and vinegar (vinegar is mostly water with some acetic acid) are **polar** — each molecule has a slightly positive end and a slightly negative end, and they grip each other through **hydrogen bonding**, one of the strongest IMFs. Oil is a tangle of long **nonpolar** hydrocarbon chains; oil molecules hold onto each other only through weak **London dispersion forces (LDF)**.

For oil to dissolve in vinegar, oil molecules would have to shove their way between water molecules — which means *breaking* water's strong hydrogen-bond network and replacing it with feeble oil-to-water attractions. Water refuses. It's energetically far happier hydrogen-bonding to its own kind and squeezing the oil out. The oil, likewise, clumps back with oil. Shaking scatters them for a moment, but the instant you stop, each kind reunites with its own. Layers. Every time.

Sugar is different. A sugar molecule (sucrose) is *covered* in $\ce{-OH}$ groups, so it can hydrogen-bond to water just as well as water bonds to itself. When sugar dissolves, water isn't giving up its handshakes — it's just trading water-water handshakes for equally good water-sugar handshakes. Nobody loses. So sugar stays dissolved forever.

That's the rule, and here's the honest version of it:

> **Like dissolves like** — a solute dissolves in a solvent when their intermolecular forces are *similar in kind and strength*. Polar/ionic solutes dissolve in polar solvents; nonpolar solutes dissolve in nonpolar solvents. Mismatched forces stay apart.

Now the coffee filter. The black marker ink is a *mixture* of pigment molecules, and the wet paper is a tug-of-war arena. The paper (soaked with water) is the **stationary phase** — it stays put. The water climbing up the paper is the **mobile phase** — it moves. Each pigment is caught between two attractions: how strongly it sticks to the paper versus how strongly it travels along with the water. A pigment that clings to the paper barely moves; a pigment that prefers the water gets carried far up. Different pigments, different balances, different speeds — so "black" fans out into blue, pink, and yellow. That's **paper chromatography**, and it's the same IMF matchmaking as the salad dressing, just used *on purpose* to pull a mixture apart.

Solubility and chromatography are two faces of one coin: **solubility asks whether things mix; separation exploits the fact that different things mix to different degrees.**

### The IMF Ladder (your solubility toolkit)

To predict solubility you rank the attractions in play. From strongest to weakest:

| Force | Between what | Strength |
|---|---|---|
| Ion-dipole | An ion and a polar molecule (e.g. $\ce{Na+}$ and $\ce{H2O}$) | Strongest |
| Hydrogen bonding | $\ce{H}$ bonded to $\ce{N,O,F}$ near another $\ce{N,O,F}$ | Strong |
| Dipole-dipole | Two polar molecules | Medium |
| London dispersion (LDF) | Any molecules; the only force in nonpolar substances | Weakest (grows with size) |

**Water** dissolves ionic solids by surrounding each ion with oriented water molecules — **ion-dipole** attractions — and dissolves polar molecules through **hydrogen bonding / dipole-dipole**. A **nonpolar solvent** like hexane ($\ce{C6H14}$) offers only LDF, so it dissolves nonpolar solutes and snubs ionic ones.

### The retention factor

When we get to chromatography, one number does all the work:

$$R_f = \frac{\text{distance traveled by the spot}}{\text{distance traveled by the solvent front}}$$

$R_f$ is always between 0 and 1 (a spot can't outrun the solvent carrying it). A **high $R_f$** means the component loves the mobile phase and rides far; a **low $R_f$** means it clings to the stationary phase and lags behind. Under identical conditions, a given compound always gives the same $R_f$ — so $R_f$ is a fingerprint.

---

## Worked Examples

### Example 1: Will table salt dissolve in water?

**Problem:** Predict whether $\ce{NaCl}$ dissolves in water, and name the force responsible.

**Solution:**
- Step 1: Identify the solute. $\ce{NaCl}$ is **ionic** — it's a lattice of $\ce{Na+}$ and $\ce{Cl-}$ ions.
- Step 2: Identify the solvent. Water is **polar** with strong hydrogen bonding and a large dipole.
- Step 3: Match forces. Water's negative (oxygen) end surrounds $\ce{Na+}$; its positive (hydrogen) ends surround $\ce{Cl-}$. These **ion-dipole** attractions are strong enough to pull ions out of the lattice.

**Answer:** Yes — $\ce{NaCl}$ dissolves in water via **ion-dipole** forces: $\ce{NaCl(s) -> Na+(aq) + Cl-(aq)}$.

### Example 2: Will sugar dissolve in water?

**Problem:** Explain, in IMF terms, why sucrose (a molecule loaded with $\ce{-OH}$ groups) dissolves in water.

**Solution:**
- Step 1: Sucrose is a **polar molecular** solid with many $\ce{-OH}$ groups.
- Step 2: Water is polar and hydrogen-bonds.
- Step 3: Every $\ce{-OH}$ on sucrose can **hydrogen-bond** to water. Water trades water-water H-bonds for equally strong water-sugar H-bonds, so dissolving costs almost nothing energetically.

**Answer:** Yes — sucrose dissolves through extensive **hydrogen bonding**. (No ions form; it dissolves as whole neutral molecules.)

### Example 3: Where does iodine dissolve — water or hexane?

**Problem:** Iodine, $\ce{I2}$, is a nonpolar molecule. Does it dissolve better in water or in hexane ($\ce{C6H14}$)?

**Solution:**
- Step 1: $\ce{I2}$ is nonpolar — its only IMF is **LDF**.
- Step 2: To dissolve in water, $\ce{I2}$ would have to break water's hydrogen bonds and offer only weak LDF in return. Bad trade — water squeezes it out.
- Step 3: Hexane is nonpolar (LDF only). $\ce{I2}$ and hexane attract each other with LDF of similar strength to hexane's own — a fair trade.

**Answer:** $\ce{I2}$ dissolves far better in **hexane**. (In fact, shake iodine's brown water solution with hexane and the purple $\ce{I2}$ migrates into the hexane layer — a real lab demo of "like dissolves like.")

### Example 4: Why the vinaigrette splits

**Problem:** Explain, using IMFs, why oil and vinegar separate into layers while sugar in tea never does.

**Solution:**
- Step 1: Vinegar is essentially water — polar, hydrogen-bonding. Oil is nonpolar — LDF only.
- Step 2: Mixing them would force water to swap strong H-bonds for weak oil-water LDF. Energetically unfavorable, so the system minimizes oil-water contact by pooling the oil into one layer.
- Step 3: Sugar, by contrast, matches water's H-bonding, so no penalty — it stays mixed.

**Answer:** Oil and water are **immiscible** because their IMFs don't match; sugar and water are compatible, so sugar dissolves permanently. Shaking only *temporarily* increases surface contact; the mismatch reasserts itself the moment you stop.

### Example 5: Ethanol — the molecule that goes both ways

**Problem:** Ethanol, $\ce{CH3CH2OH}$, mixes with water in *any* ratio and also dissolves many nonpolar substances. Explain.

**Solution:**
- Step 1: Ethanol has two personalities. The $\ce{-OH}$ end is polar and **hydrogen-bonds** (like water). The $\ce{CH3CH2-}$ end is a small nonpolar hydrocarbon (LDF, like oil).
- Step 2: The $\ce{-OH}$ end lets it hydrogen-bond fully with water → **miscible** with water.
- Step 3: The hydrocarbon end lets it use LDF with nonpolar solutes → dissolves some nonpolar things too.

**Answer:** Ethanol is soluble both ways because it carries **both** a polar H-bonding group and a nonpolar tail. (This is why ethanol is such a common solvent — it bridges the two worlds. It's also why longer alcohols like 1-octanol, with big greasy tails, stop mixing with water: the nonpolar part wins.)

### Example 6: Vitamin C vs vitamin A

**Problem:** Vitamin C (ascorbic acid) is covered in $\ce{-OH}$ groups; vitamin A (retinol) is mostly a long hydrocarbon chain. One is "water-soluble," one is "fat-soluble." Match them and explain.

**Solution:**
- Step 1: Vitamin C — many $\ce{-OH}$ groups → strong H-bonding → dissolves in water (polar).
- Step 2: Vitamin A — long nonpolar chain → LDF dominates → dissolves in fats/oils (nonpolar).

**Answer:** Vitamin **C is water-soluble** (H-bonding), vitamin **A is fat-soluble** (LDF). This is why your body can flush excess vitamin C in urine but *stores* excess vitamin A in fatty tissue — a real "like dissolves like" consequence.

### Example 7: How soap washes grease

**Problem:** Grease is nonpolar and water is polar, so water alone can't rinse grease off a plate. Explain how soap fixes this.

**Solution:**
- Step 1: A soap/surfactant molecule is **two-faced**: a polar (often ionic) **head** that loves water, and a long nonpolar **tail** that loves grease. (This is the split-personality molecule from [Why Chemistry Matters](/chemistry/0001-why-chemistry-matters) that makes shampoo foam.)
- Step 2: The nonpolar **tails** bury themselves in the grease; the polar **heads** point outward into the water, forming a tiny ball (a **micelle**) with grease trapped inside.
- Step 3: The micelle's outside is now water-friendly, so the whole grease-filled bundle rinses away with the water.

**Answer:** Soap works because each molecule bridges polar and nonpolar worlds — tail grabs grease, head grabs water — so grease that water could never touch alone gets carried off inside micelles.

### Example 8: Reading a solubility curve (solid)

**Problem:** A potassium nitrate solubility curve reads: $\ce{KNO3}$ dissolves to about $32~\text{g}$ per $100~\text{g}$ water at $20^\circ\text{C}$ and about $110~\text{g}$ at $60^\circ\text{C}$. (a) You stir $80~\text{g}$ of $\ce{KNO3}$ into $100~\text{g}$ water at $60^\circ\text{C}$ — saturated or unsaturated? (b) You cool that solution to $20^\circ\text{C}$ without disturbing it. What can happen?

**Solution:**
- Step 1 (a): At $60^\circ\text{C}$ the max is $110~\text{g}$. You added only $80~\text{g} < 110~\text{g}$, so it all dissolves and could hold more.
- Step 2 (b): At $20^\circ\text{C}$ the max is only $32~\text{g}$, but the beaker holds $80~\text{g}$ dissolved. That's $80 - 32 = 48~\text{g}$ *more* than should fit.
- Step 3: If cooled gently and undisturbed, the extra $48~\text{g}$ can stay dissolved as a shaky **supersaturated** solution; a seed crystal or a bump makes it crash out.

**Answer:** (a) **Unsaturated** at $60^\circ\text{C}$. (b) It becomes **supersaturated** at $20^\circ\text{C}$; disturbing it precipitates about **$48~\text{g}$** of $\ce{KNO3}$. (This is exactly how **rock candy** grows — supersaturate hot sugar-water, then let crystals build as it cools.)

### Example 9: Warm soda goes flat (gas + temperature)

**Problem:** A cold soda is fizzy; a warm one is flat. Explain in terms of gas solubility and temperature.

**Solution:**
- Step 1: Soda is $\ce{CO2}$ gas dissolved in water: $\ce{CO2(g) <=> CO2(aq)}$.
- Step 2: Unlike solids, **gases become LESS soluble as temperature rises** — warmer molecules have more kinetic energy and escape the liquid more easily.
- Step 3: Warm the can and dissolved $\ce{CO2}$ leaves solution faster, so a warm soda loses its fizz.

**Answer:** Higher temperature **lowers** gas solubility, so warm soda goes flat. (Same reason warm river or ocean water holds **less dissolved oxygen** — a real problem for fish near power-plant outflows.)

### Example 10: The soda-can fizz (gas + pressure, Henry's law)

**Problem:** Why does a sealed soda look still, but hiss and erupt in bubbles the instant you crack it open?

**Solution:**
- Step 1: Soda is canned under **high $\ce{CO2}$ pressure**. **Henry's law** says gas solubility rises with the pressure of that gas above the liquid — high pressure forces lots of $\ce{CO2}$ into solution.
- Step 2: Opening the can drops the pressure to atmospheric almost instantly.
- Step 3: The liquid is now holding far more $\ce{CO2}$ than it can at the lower pressure, so $\ce{CO2}$ rushes out as bubbles: $\ce{CO2(aq) -> CO2(g)}$.

**Answer:** Under Henry's law, **more pressure = more dissolved gas**; releasing the pressure makes the excess gas fizz out. (This is the very first "chemistry in real life" example from [Why Chemistry Matters](/chemistry/0001-why-chemistry-matters) — now you can justify it with IMFs and Henry's law.)

### Example 11: Calculating $R_f$

**Problem:** On a chromatogram, the solvent front rises $8.0~\text{cm}$ up the paper. A blue pigment spot ends up $4.0~\text{cm}$ from the start line. Find its $R_f$.

**Solution:**
- Step 1: Identify the two distances, both measured from the *start line*: spot $= 4.0~\text{cm}$, solvent front $= 8.0~\text{cm}$.
- Step 2: Apply $R_f = \dfrac{\text{distance spot}}{\text{distance solvent}} = \dfrac{4.0}{8.0}$.
- Step 3: $R_f = 0.50$ (unitless — the cm cancel).

**Answer:** $R_f = 0.50$. The blue pigment split its time evenly between clinging to the paper and riding with the water.

### Example 12: Comparing pigments and interpreting a chromatogram

**Problem:** Running the black marker, the solvent front travels $10.0~\text{cm}$. Yellow reaches $8.0~\text{cm}$, pink reaches $5.0~\text{cm}$, blue reaches $2.0~\text{cm}$. (a) Find each $R_f$. (b) Which pigment is most attracted to the paper? (c) What does the result prove about the "black" ink?

**Solution:**
- Step 1 (a): $R_f(\text{yellow}) = 8.0/10.0 = 0.80$; $R_f(\text{pink}) = 5.0/10.0 = 0.50$; $R_f(\text{blue}) = 2.0/10.0 = 0.20$.
- Step 2 (b): The **lowest** $R_f$ means it moved least → most attracted to the stationary phase (paper). That's **blue** ($R_f = 0.20$).
- Step 3 (c): Three distinct spots at three $R_f$ values means three different substances were present.

**Answer:** (a) Yellow $0.80$, pink $0.50$, blue $0.20$. (b) **Blue** sticks to the paper most. (c) "Black" ink is a **mixture** of at least three pigments — chromatography separated and revealed them.

### Example 13: Choose the technique (the decision set)

**Problem:** Name the best separation method for each mixture and justify it: (a) salt + sand, (b) salt dissolved in water, (c) two food dyes in one drop of solution, (d) oil + water.

**Solution:**
- (a) **Salt + sand → filtration after dissolving.** Add water: salt dissolves, sand doesn't. **Filter** out the sand (particle size — sand grains can't pass the filter), then evaporate the water to recover salt.
- (b) **Salt water → distillation (or evaporation).** Water boils at $100^\circ\text{C}$; salt is nonvolatile. **Boil off** the water (collect it by condensing = distillation) and salt stays behind. Uses the huge **boiling-point / volatility** difference.
- (c) **Two dyes → chromatography.** They're both dissolved, so filtration and distillation won't split them; but they have different affinities for paper vs solvent, so they travel at different rates.
- (d) **Oil + water → separation by a separating funnel (decanting).** They're **immiscible** and have different densities, so they form layers you can physically drain apart — no dissolving needed.

**Answer:** (a) filtration, (b) distillation, (c) chromatography, (d) let them layer and separate — each choice is set by particle size, boiling point, IMF affinity, or immiscibility.

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Saying "it just dissolves" or "salt likes water" | Skipping the mechanism | On the AP exam, *name the IMF*: ion-dipole for ionic in water, H-bonding/dipole-dipole for polar, LDF for nonpolar |
| Thinking dissolving breaks a molecule apart | Confusing molecular with ionic solutes | Only **ionic** solutes split into ions; sugar dissolves as **whole molecules** |
| Assuming heat increases solubility of everything | Overgeneralizing from solids | Solids: usually **more** soluble hot. Gases: **less** soluble hot. They're opposite. |
| Flipping the $R_f$ ratio | Forgetting which distance is on top | Spot distance is always on **top**; $R_f \le 1$ always. If you get a number $>1$, you inverted it |
| Measuring $R_f$ from the bottom of the paper | Wrong reference point | Measure both distances from the **start (pencil) line**, not the paper edge |
| Using filtration to separate salt from water | Salt particles are dissolved (ion-sized) | Filtration only catches **undissolved** particles; dissolved salt sails through — use distillation |
| Confusing stationary and mobile phases | New vocabulary | **Stationary** = the paper (stays put). **Mobile** = the solvent (moves). High affinity for stationary → low $R_f$ |
| Writing "$6.25 boba" with a bare dollar sign | KaTeX pairs `$` across the whole page | Always escape currency as `\$6.25` in prose |

---

## AP Exam Tips

- **Justify solubility with IMFs, never with a slogan.** A free-response answer that says "polar dissolves polar" earns little; one that says "water's dipole forms **ion-dipole** attractions with $\ce{Na+}$ and $\ce{Cl-}$, strong enough to overcome the lattice" earns the point. Always identify the specific force: **ion-dipole, hydrogen bonding, dipole-dipole, or LDF**.
- **Structure → IMF → solubility is the graded chain.** Given a structure, spot the polar groups ($\ce{-OH}$, $\ce{-NH2}$) or the nonpolar chains, decide the dominant IMF, *then* predict the solvent. Show all three links.
- **Know the temperature reversal cold.** "Solids generally get **more** soluble as $T$ rises; gases get **less** soluble." The gas-flat-soda / warm-water-holds-less-oxygen example is a classic FRQ prompt.
- **$R_f$ is a fingerprint.** Under identical conditions, the same compound gives the same $R_f$, so you can identify a component by matching its $R_f$ to a known. $R_f$ has **no units** and is **always $\le 1$**.
- **Match technique to property.** Filtration = **particle size**; distillation = **boiling point / volatility**; chromatography = **relative affinity (IMFs) for stationary vs mobile phase**. Name the property the method exploits.
- **Distillation logic:** the component with the **lower boiling point (more volatile)** vaporizes first and is collected; the less volatile one stays behind. Salt (nonvolatile) never leaves the flask.
- **Henry's law is qualitative on the AP exam:** more gas pressure → more dissolved gas. You won't usually compute a constant, but you must reason with it (the soda can).

---

## Practice Problems

### Problem 1
Predict whether ammonium chloride, $\ce{NH4Cl}$ (ionic), dissolves in water, and name the force.

<details>
<summary><strong>Solution</strong></summary>

$\ce{NH4Cl}$ is ionic. Water surrounds $\ce{NH4+}$ and $\ce{Cl-}$ with oriented dipoles.

**Answer:** Yes — it dissolves via **ion-dipole** attractions: $\ce{NH4Cl(s) -> NH4+(aq) + Cl-(aq)}$.

</details>

### Problem 2
Will methane, $\ce{CH4}$ (nonpolar), dissolve well in water? Justify with IMFs.

<details>
<summary><strong>Solution</strong></summary>

$\ce{CH4}$ has only LDF. Dissolving it would break water's strong hydrogen bonds and replace them with weak LDF — an unfavorable trade.

**Answer:** No — $\ce{CH4}$ is nearly insoluble in water because its weak LDF can't compensate for disrupting water's hydrogen-bond network.

</details>

### Problem 3
Ammonia, $\ce{NH3}$, is extremely soluble in water. Explain why.

<details>
<summary><strong>Solution</strong></summary>

$\ce{NH3}$ is polar and has $\ce{N-H}$ bonds plus a lone pair, so it **hydrogen-bonds** with water (both as donor and acceptor).

**Answer:** $\ce{NH3}$ dissolves readily through **hydrogen bonding** with water.

</details>

### Problem 4
You shake $\ce{I2}$-in-water (brown) with hexane and let it settle. Two layers form: a nearly colorless lower layer and a purple upper layer. Explain where the iodine went and why.

<details>
<summary><strong>Solution</strong></summary>

$\ce{I2}$ is nonpolar (LDF only). Hexane is nonpolar; water is polar. "Like dissolves like" sends $\ce{I2}$ into the hexane. Hexane is less dense, so it's on top.

**Answer:** The iodine migrated into the **upper hexane layer** (turning it purple) because nonpolar $\ce{I2}$ prefers the nonpolar solvent.

</details>

### Problem 5
Explain why 1-butanol ($\ce{CH3CH2CH2CH2OH}$) is only partly soluble in water, while methanol ($\ce{CH3OH}$) is completely miscible.

<details>
<summary><strong>Solution</strong></summary>

Both have an $\ce{-OH}$ group that hydrogen-bonds to water. But 1-butanol has a longer nonpolar carbon chain, so its LDF-driven "greasy" character is a bigger fraction of the molecule; methanol's chain is tiny.

**Answer:** The bigger the nonpolar tail, the less water-soluble the alcohol. Methanol's small tail keeps it fully miscible; 1-butanol's longer tail makes it only partly soluble.

</details>

### Problem 6
In one or two sentences, explain how soap removes bacon grease from a pan, using the words *polar head*, *nonpolar tail*, and *micelle*.

<details>
<summary><strong>Solution</strong></summary>

The **nonpolar tails** dissolve into the grease while the **polar heads** face the water, wrapping the grease in a **micelle** whose water-friendly outside rinses away.

**Answer:** Soap surrounds grease in micelles — tails in, heads out — so grease that water can't touch alone washes off.

</details>

### Problem 7
A student says, "I'll separate salt from water by filtering it." What's wrong, and what should they do?

<details>
<summary><strong>Solution</strong></summary>

Dissolved salt exists as individual $\ce{Na+}$ and $\ce{Cl-}$ ions, far smaller than any filter pore, so they pass straight through. Filtration only removes undissolved particles.

**Answer:** Filtration fails; use **distillation/evaporation** — boil off the water (nonvolatile salt stays behind) and condense the vapor to recover pure water.

</details>

### Problem 8
Sodium chloride dissolves to about $36~\text{g}/100~\text{g}$ water at $20^\circ\text{C}$ and about $39~\text{g}/100~\text{g}$ at $100^\circ\text{C}$. How does $\ce{NaCl}$ solubility compare with a salt like $\ce{KNO3}$ (which jumps from $32$ to $\sim 245~\text{g}$ over the same range)?

<details>
<summary><strong>Solution</strong></summary>

$\ce{NaCl}$'s solubility barely changes with temperature (a nearly flat curve), while $\ce{KNO3}$'s rises steeply.

**Answer:** Both are solids that increase slightly-to-steeply with $T$, but $\ce{NaCl}$ is nearly temperature-independent whereas $\ce{KNO3}$ is strongly temperature-dependent — which is why you can't grow rock candy easily from table salt but you can from $\ce{KNO3}$ or sugar.

</details>

### Problem 9
Using the $\ce{KNO3}$ values from Example 8 ($32~\text{g}$ at $20^\circ\text{C}$, $110~\text{g}$ at $60^\circ\text{C}$ per $100~\text{g}$ water): you dissolve $32~\text{g}$ in $100~\text{g}$ water at $20^\circ\text{C}$. Is the solution saturated, unsaturated, or supersaturated?

<details>
<summary><strong>Solution</strong></summary>

At $20^\circ\text{C}$ the maximum is exactly $32~\text{g}$, and you dissolved exactly $32~\text{g}$.

**Answer:** **Saturated** — it holds precisely the maximum amount, with no excess and no room for more.

</details>

### Problem 10
Fish struggle in warm water. Explain using gas solubility and temperature.

<details>
<summary><strong>Solution</strong></summary>

Gases become **less** soluble as temperature increases. Warm water holds less dissolved $\ce{O2}$, so fish have less oxygen to breathe.

**Answer:** Warmer water retains less dissolved oxygen (gas solubility drops with heat), stressing fish. This is why thermal pollution from power plants can suffocate aquatic life.

</details>

### Problem 11
Why do deep-sea divers who surface too quickly risk "the bends" (nitrogen bubbles in the blood)? Relate it to the soda can.

<details>
<summary><strong>Solution</strong></summary>

At depth, high pressure forces extra $\ce{N2}$ to dissolve in the blood (Henry's law). Surfacing too fast drops the pressure suddenly, and — exactly like opening a soda can — the excess $\ce{N2}$ comes out of solution as bubbles.

**Answer:** Rapid pressure drop makes dissolved $\ce{N2}$ fizz out of the blood (Henry's law), the same physics as a soda can erupting when opened.

</details>

### Problem 12
On a chromatogram the solvent front travels $12.0~\text{cm}$ and a green spot travels $9.0~\text{cm}$ from the start line. Calculate $R_f$.

<details>
<summary><strong>Solution</strong></summary>

$$R_f = \frac{9.0}{12.0} = 0.75$$

**Answer:** $R_f = 0.75$ — the green component strongly prefers the mobile phase.

</details>

### Problem 13
Two inks are run side by side. Ink A gives a single spot at $R_f = 0.60$. Ink B gives two spots at $R_f = 0.60$ and $R_f = 0.35$. What can you conclude?

<details>
<summary><strong>Solution</strong></summary>

Ink A is a single pure substance ($R_f = 0.60$). Ink B is a mixture; one of its components matches ink A's $R_f = 0.60$ (likely the same compound), plus a second component at $R_f = 0.35$.

**Answer:** Ink B is a **mixture** containing a component identical to ink A (same $R_f = 0.60$) plus a second, more paper-attracted component ($R_f = 0.35$).

</details>

### Problem 14
Two spots have $R_f = 0.20$ and $R_f = 0.85$. Which is more attracted to the paper (stationary phase)? Explain.

<details>
<summary><strong>Solution</strong></summary>

Low $R_f$ means the spot barely moved, so it spent most of its time stuck to the paper.

**Answer:** The $R_f = 0.20$ spot is **more attracted to the stationary phase**; the $R_f = 0.85$ spot preferred the mobile solvent and traveled far.

</details>

### Problem 15
For each mixture, name the best separation technique and the property it exploits: (a) sand + iron filings, (b) alcohol + water, (c) chalk powder stirred in water, (d) the pigments in spinach-leaf extract.

<details>
<summary><strong>Solution</strong></summary>

- (a) A **magnet** — iron is magnetic, sand isn't (a physical property).
- (b) **Distillation** — different **boiling points** (ethanol $\sim 78^\circ\text{C}$, water $100^\circ\text{C}$); the more volatile ethanol vaporizes first.
- (c) **Filtration** — chalk is insoluble, so **particle size** lets you filter it out.
- (d) **Chromatography** — the plant pigments (chlorophylls, carotenes) have different **affinities (IMFs)** for stationary vs mobile phase and separate into colored bands.

**Answer:** (a) magnet, (b) distillation, (c) filtration, (d) chromatography.

</details>

---

## Quick Reference

| Concept | Rule / Formula | Everyday anchor |
|---|---|---|
| Like dissolves like | Match IMFs: polar↔polar/ionic, nonpolar↔nonpolar | Sugar mixes forever; oil + vinegar split |
| Ionic solute in water | Ion-dipole; splits into ions | $\ce{NaCl(s) -> Na+(aq) + Cl-(aq)}$ |
| Polar solute in water | Hydrogen bonding / dipole-dipole; stays whole | Sugar, ethanol, $\ce{NH3}$ |
| Nonpolar solute | LDF; dissolves in nonpolar solvent only | $\ce{I2}$ in hexane, not water |
| Surfactant | Polar head + nonpolar tail → micelle | Soap lifting grease |
| Miscible vs immiscible | Fully mix vs form layers | Ethanol + water vs oil + water |
| Solids + temperature | Usually **more** soluble when hot | Rock candy, supersaturation |
| Gases + temperature | **Less** soluble when hot | Warm soda goes flat |
| Gases + pressure (Henry) | More pressure → more dissolved gas | Soda-can fizz, the bends |
| Saturation | Below / at / above max = unsat / sat / supersat | Cooling a hot solution |
| Filtration | Separates by **particle size** | Salt + sand (after dissolving) |
| Distillation | Separates by **boiling point / volatility** | Salt water; alcohol + water |
| Chromatography | Separates by **affinity** (stationary vs mobile) | Marker on wet coffee filter |
| Retention factor | $R_f = \dfrac{\text{spot distance}}{\text{solvent distance}}$, $0 \le R_f \le 1$ | Low $R_f$ = clings to paper |

---

<div align="center">

[← Solutions and Concentration](/chemistry/0506-solutions-and-concentration) | [Spectroscopy and Beer's Law →](/chemistry/0508-spectroscopy-beer-lambert)

</div>
