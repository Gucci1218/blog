# Spectroscopy and Beer's Law
<p class="article-date">July 5, 2026</p>

*Yesterday I made two glasses of iced tea from the same pitcher of concentrate — one weak (a splash of concentrate, then water to the brim) and one I'll call the triple-strength monster (three big pours, barely any water). I hadn't tasted either yet, but standing at the kitchen counter I already knew which was which: the strong one was a deep, dark amber you could barely see your finger through, and the weak one was a pale, sunlit gold. That's the whole idea of today's article. **The darker the drink, the more concentrated it is, because the more stuff is dissolved, the more light gets swallowed on its way through the glass.** A spectrophotometer is just a machine that does my eyeball trick with numbers: it shines a known beam of light through the liquid and measures exactly how much gets absorbed, and Beer's law is the precise straight-line rule that turns "how dark" into "how concentrated." This is the capstone of Unit 3 — where light and matter finally shake hands — and once you see that Beer's law is nothing but $y = mx$ wearing a lab coat, it stops being scary and starts being free points on the AP exam.*

> **Bonus garnish (the same trick in reverse):** absorption tells you *how much* stuff is there; **emission** tells you *what* the stuff is. Heat an element and it glows a signature color — strontium's firework red, copper's blue-green, the orange of a sodium streetlamp. Those colors are atomic fingerprints. Light *absorbed* maps to **concentration** (Beer's law, a line through the origin); light *emitted at specific colors* maps to **electron energy jumps** (spectroscopy, an element's ID card). Two sides of one coin, and we'll handle both.

---

## What You'll Learn
- Place the regions of the electromagnetic spectrum in order (radio → gamma) and state which kind of chemistry each region probes — microwave (molecular rotations), infrared (bond vibrations), UV-Vis (electronic transitions)
- Convert fluently among wavelength, frequency, and energy using $c = \lambda\nu$ and $E = h\nu = \dfrac{hc}{\lambda}$, with careful unit handling (nm → m, output in joules)
- Explain why high frequency / short wavelength means high energy — and why UV gives you a sunburn while a warm infrared heat lamp never does
- Describe absorption and emission as electrons jumping *up* by swallowing a photon and falling *down* by emitting one, and connect discrete line spectra to quantized energy levels (the Bohr-model evidence)
- Read flame-test and fireworks colors as element fingerprints, and compute the wavelength emitted from a given energy gap $\Delta E$
- State what the photoelectric effect showed: electrons are ejected only above a **threshold frequency**, not by cranking up brightness — proof that light comes in quantized photons
- Apply the Beer-Lambert law $A = \varepsilon b c$ to find an unknown concentration, a molar absorptivity $\varepsilon$, or a predicted absorbance
- Build and read a **calibration curve** (absorbance vs concentration, a line through the origin with slope $\varepsilon b$) and use it to solve a real AP-FRQ-shaped lab problem — including the "dilute it if the absorbance is off the chart" logic

---

## Prerequisites
- [Graphing and Linearization](/chemistry/0105-graphing-linearization) — Beer's law *is* a straight line through the origin; everything you learned about slope, best-fit lines, and interpolation cashes out here
- [Solutions and Concentration](/chemistry/0506-solutions-and-concentration) — the "how concentrated" side of the story; you need molarity in your bones before you can measure it with light

---

## The Core Concept

### Intuition First

Back to my two glasses of iced tea. Picture shining a flashlight straight through each one at eye level. Through the pale weak tea, almost all the light punches through — the far side of the glass looks bright. Through the dark triple-strength monster, the beam struggles; only a little light makes it out the other side. Nothing mysterious is happening: each dissolved tea molecule is a tiny light-catcher, and the more of them crammed into the path of the beam, the more photons get caught. **More concentration → more absorbers in the way → less light out → a bigger "absorbance" reading.** That is Beer's law in one breath.

Let's make the map precise, because — like every good opener in this blog — it's structural, not decorative:

| Iced tea at the counter | The spectrophotometer |
|---|---|
| The glass of tea | The **cuvette** (the sample cell) |
| One dissolved tea molecule | One **absorbing particle** |
| How strong I mixed it | **Concentration** $c$ (molarity) |
| How wide the glass is (light's path through it) | **Path length** $b$ (usually 1.00 cm) |
| How "grabby" tea is for light per molecule | **Molar absorptivity** $\varepsilon$ |
| How dark it looks / how little light gets through | **Absorbance** $A$ |
| My eyeball guess "that one's stronger" | The machine's precise reading |

Two knobs control the darkness, and Beer's law says the darkness scales with **both**, multiplied together:

1. **More molecules in the path** — either by making it more concentrated (bigger $c$) *or* by using a wider glass so the light travels farther through the liquid (bigger $b$). Either way, more absorbers to run into.
2. **How good each molecule is at catching this particular color** — that's $\varepsilon$, a property of *what* is dissolved and *which color* you shine. Deep-purple $\ce{KMnO4}$ has a huge $\varepsilon$; plain water has essentially zero.

Now flip the coin. When you *heat* those molecules or atoms instead of shining light through them, they hand energy *back* as light — and not just any light, but sharp, specific colors. Sodium always glows the same orange (that's why old streetlamps are that exact hue), strontium always burns firework-red. Why so picky about color? Because an atom's electrons can only sit on specific energy "shelves" (quantized levels), and the color of light emitted is set *exactly* by the size of the jump between two shelves. Absorption fills the same shelves from the light; emission empties them back into light. Same shelves, opposite direction.

### Light Is Energy: The Electromagnetic Spectrum

All light — radio waves, the orange of that streetlamp, X-rays at the dentist — is the same stuff (electromagnetic radiation) traveling at the same speed in a vacuum:

$$c = 3.00 \times 10^{8} \ \text{m/s}$$

What makes "colors" different is the **wavelength** $\lambda$ (crest-to-crest distance, in meters) and the **frequency** $\nu$ (waves passing per second, in $\text{s}^{-1}$ or hertz, Hz). They're locked together because the speed is fixed:

$$c = \lambda\nu \qquad\Longrightarrow\qquad \nu = \frac{c}{\lambda}$$

Long wavelength ⟷ low frequency, and short wavelength ⟷ high frequency. They trade off, because their product is always the same $c$.

And here's the piece that makes light *chemical*: the energy carried by a single packet of light (a **photon**) is set by its frequency through Planck's constant $h$:

$$E = h\nu = \frac{hc}{\lambda}, \qquad h = 6.626 \times 10^{-34}\ \text{J·s}$$

Read those two equations together and the headline falls out:

$$\boxed{\text{high frequency} \;=\; \text{short wavelength} \;=\; \text{high energy}}$$

The spectrum, from lowest energy to highest:

| Region | Wavelength (rough) | Energy | What chemistry it probes |
|---|---|---|---|
| **Radio** | > 1 m | lowest | nuclear spins (this is MRI/NMR) |
| **Microwave** | mm–cm | low | molecular **rotations** (also how your microwave spins water molecules) |
| **Infrared (IR)** | ~700 nm – 1 mm | low-medium | **bond vibrations** — stretching/bending; an IR spectrum is a bond fingerprint |
| **Visible** | ~400–700 nm | medium | **electronic transitions** in colored compounds — the region Beer's law lives in |
| **Ultraviolet (UV)** | ~10–400 nm | high | higher-energy **electronic transitions**; enough to break bonds and damage skin |
| **X-ray** | ~0.01–10 nm | very high | knocks out core electrons (this powers PES from Topic 3.10) |
| **Gamma** | < 0.01 nm | highest | nuclear reactions |

The **sunburn-not-heat-lamp** intuition nails why energy — not brightness — is what matters. Sit under a warm infrared heat lamp all afternoon and you'll feel toasty but you will *never* burn, no matter how bright it is. Step into ten minutes of midday UV and you're pink. Infrared photons, one at a time, simply don't carry enough energy to damage a skin molecule; UV photons do. Cranking the heat lamp brighter just sends *more* too-weak photons — a million gentle taps still won't break down a door that needs one hard kick. Hold onto that image; it's literally the photoelectric effect, coming up.

### Absorption and Emission: Electrons on Shelves

An atom's electrons live on discrete energy levels — think shelves at fixed heights, with *nothing* in between (this is the quantized picture Bohr proposed; see the [History of Chemistry](/chemistry/0002-history-of-chemistry) for how the neat lines in hydrogen's spectrum forced physicists to accept it).

- **Absorption:** a photon whose energy *exactly* matches the gap between two shelves gets swallowed, and an electron jumps **up**. Photons of the wrong energy sail right through — untouched.
- **Emission:** an electron that's been kicked up (by heat, electricity, a flame) falls back **down** and spits the energy out as a photon of *exactly* the gap energy.

Either way, the photon energy equals the gap:

$$\Delta E = h\nu = \frac{hc}{\lambda}$$

Because the shelves sit at fixed heights, only certain gaps exist, so only certain photon energies — certain **colors** — show up. That's why you get sharp bright **line spectra**, not a smeared rainbow. And since every element has its own unique shelf arrangement, every element emits its own unique set of lines. That's the fingerprint:

| Element | Flame / firework color | Roughly |
|---|---|---|
| $\ce{Li}$ | crimson red | ~671 nm |
| $\ce{Na}$ | orange-yellow (streetlamps!) | 589 nm |
| $\ce{K}$ | lilac / pale violet | ~404, 767 nm |
| $\ce{Sr}$ | scarlet red (fireworks) | ~605–680 nm |
| $\ce{Cu}$ | blue-green | ~510–525 nm |

When you see a fireworks show, you are literally reading emission spectra with your eyes. The chemist who lit them chose salts by their line colors.

### Which Region Probes Which Motion (the "beyond Beer's law" part)

The AP curriculum wants you to know that *different amounts of energy excite different kinds of motion in molecules*. Bigger jump, bigger photon needed:

| Photon energy (region) | What it excites | Everyday analogy |
|---|---|---|
| Low (microwave) | whole-molecule **rotation** — the molecule tumbles faster | giving a top a light spin |
| Medium (infrared) | **bond vibration** — bonds stretch and bend like springs | plucking a guitar string |
| High (UV-Vis) | **electronic transition** — an electron jumps to a higher level | launching a ball to a higher shelf |

Rotations are the cheapest motion to excite, so they need the wimpiest photons (microwave). Vibrating a bond costs more (infrared). Actually promoting an electron is the priciest, so it takes visible or UV light — which is exactly why the *colored* compounds you measure with Beer's law absorb in the visible range.

### The Photoelectric Effect (Topic 3.12): Light Comes in Packets

Shine light on a clean metal surface and, if the light is energetic enough, electrons come flying off. The shocking experimental result — the one that won Einstein his Nobel Prize — is *how* it depends on the light:

- Below a certain **threshold frequency**, **no** electrons come off — *no matter how bright* you make the light. You can blast the metal with a blinding beam of red light and get nothing.
- Above the threshold frequency, electrons come off **instantly**, even from a very dim beam. Turn up the brightness and you get *more* electrons, but not more energetic ones.

If light were just a continuous wave, brightness (more energy poured in) should eventually knock electrons loose. It doesn't. The only way this makes sense: **light arrives in individual packets — photons — each carrying energy $E = h\nu$, and one photon hits one electron.** If a single photon doesn't have enough energy (frequency too low) to pay the electron's "escape fee," the electron stays put — and sending a flood of too-weak photons doesn't help, because the electron can't save up several hits. That's our heat-lamp-vs-sunburn image made into a lab result: it's the *energy per photon* (frequency) that matters, not the total pile of light (brightness). This is the experiment that turned light into photons and made all of Beer's law and spectroscopy possible.

### The Beer-Lambert Law (Topic 3.13): Turning Color into a Number

Finally, the star of the show. When monochromatic light (one wavelength) passes through a solution, the **absorbance** $A$ obeys:

$$\boxed{A = \varepsilon\, b\, c}$$

| Symbol | Name | Units | What it is |
|---|---|---|---|
| $A$ | absorbance | none (unitless) | how much light is swallowed |
| $\varepsilon$ | molar absorptivity | $\text{M}^{-1}\text{cm}^{-1}$ | how grabby *this* species is for *this* wavelength |
| $b$ | path length | cm | how far the light travels through the sample (usually 1.00 cm) |
| $c$ | concentration | M (mol/L) | how much is dissolved |

For a fixed compound, fixed wavelength, and fixed cuvette, $\varepsilon$ and $b$ are constants — so $A$ is just a constant times $c$:

$$A = \underbrace{(\varepsilon b)}_{\text{slope}} \cdot\, c$$

**That is $y = mx$** — a straight line through the origin, with $c$ on the x-axis, $A$ on the y-axis, and slope $\varepsilon b$. (At $c = 0$, pure solvent, $A = 0$: no absorbers, no absorbance. That's why the line goes through the origin.) This is precisely the linearization game from [Graphing and Linearization](/chemistry/0105-graphing-linearization): plot your data as a line, read the slope, and the slope *is* a physical constant — here, $\varepsilon b$.

**Why we pick $\lambda_{\text{max}}$.** You run Beer's law at the wavelength the compound absorbs *most strongly* — its $\lambda_{\text{max}}$ (the color it grabs hardest). Two reasons: the absorbance is biggest there, so the same change in concentration causes the biggest change in reading (maximum sensitivity), and the absorbance changes slowly with wavelength near a peak, so tiny wavelength errors barely matter. For purple $\ce{KMnO4}$, $\lambda_{\text{max}} \approx 525$ nm (it absorbs green, so we *see* purple).

**Why absorbance and not "percent light through."** The raw thing the machine sees is **transmittance** $T$ — the fraction of light that makes it through. Absorbance is defined as $A = -\log_{10} T$, and that logarithm is exactly what makes $A$ come out linear in $c$. You don't need the log formula for most AP problems; just know that the machine reports $A$, and $A$ is the quantity that behaves like a nice straight line.

---

## Worked Examples

### Example 1: Wavelength → Frequency
**Problem:** Green light has a wavelength of $\lambda = 500$ nm. Find its frequency.

**Solution:**
- **Step 1 — units.** Convert nm to m: $500 \ \text{nm} = 500 \times 10^{-9}\ \text{m} = 5.00 \times 10^{-7}\ \text{m}$.
- **Step 2 — rearrange** $c = \lambda\nu$: $\nu = \dfrac{c}{\lambda}$.
- **Step 3 — plug in:** $\nu = \dfrac{3.00 \times 10^{8}\ \text{m/s}}{5.00 \times 10^{-7}\ \text{m}} = 6.00 \times 10^{14}\ \text{s}^{-1}$.

**Answer:** $\nu = 6.00 \times 10^{14}\ \text{Hz}$.

### Example 2: Wavelength → Energy of One Photon
**Problem:** Find the energy of a single photon of that same 500 nm green light.

**Solution:**
- **Step 1 — pick the formula** that goes straight from wavelength to energy: $E = \dfrac{hc}{\lambda}$.
- **Step 2 — plug in** (using $\lambda = 5.00 \times 10^{-7}$ m):
$$E = \frac{(6.626 \times 10^{-34}\ \text{J·s})(3.00 \times 10^{8}\ \text{m/s})}{5.00 \times 10^{-7}\ \text{m}}$$
- **Step 3 — arithmetic:** numerator $= 1.988 \times 10^{-25}\ \text{J·m}$; divide by $5.00 \times 10^{-7}\ \text{m}$.

**Answer:** $E = 3.98 \times 10^{-19}\ \text{J}$ per photon.

### Example 3: Energy per Mole of Photons
**Problem:** How much energy is in *one mole* of those 500 nm photons?

**Solution:**
- **Step 1 — start from one photon:** $3.98 \times 10^{-19}\ \text{J}$ (Example 2).
- **Step 2 — multiply by Avogadro's number:**
$$E_{\text{mol}} = (3.98 \times 10^{-19}\ \text{J})(6.022 \times 10^{23}\ \text{mol}^{-1}) = 2.40 \times 10^{5}\ \text{J/mol}$$

**Answer:** $E_{\text{mol}} = 2.40 \times 10^{5}\ \text{J/mol} = 240\ \text{kJ/mol}$ — comparable to a chemical bond energy, which is why visible/UV light can drive chemistry.

### Example 4: Ranking Photons by Energy
**Problem:** Order these by increasing photon energy: an infrared photon ($\lambda = 1000$ nm), a blue photon ($\lambda = 450$ nm), and a UV photon ($\lambda = 250$ nm).

**Solution:**
- **Step 1 — the rule:** $E = \dfrac{hc}{\lambda}$, so energy is *inversely* proportional to wavelength. **Shortest wavelength wins.**
- **Step 2 — order the wavelengths:** $1000\ \text{nm} > 450\ \text{nm} > 250\ \text{nm}$, so the energy order is the reverse.

**Answer:** infrared (1000 nm) < blue (450 nm) < UV (250 nm). This is the sunburn story: the UV photon packs the most punch.

### Example 5: Frequency → Energy
**Problem:** A microwave oven emits radiation at $\nu = 2.45 \times 10^{9}\ \text{Hz}$. Find the energy of one such photon.

**Solution:**
- **Step 1 — use** $E = h\nu$ directly (frequency is given).
- **Step 2 — plug in:** $E = (6.626 \times 10^{-34}\ \text{J·s})(2.45 \times 10^{9}\ \text{s}^{-1})$.

**Answer:** $E = 1.62 \times 10^{-24}\ \text{J}$ — tiny, which is why microwaves only spin water molecules (rotations), never break bonds.

### Example 6: Emission Line → Wavelength (the Fingerprint)
**Problem:** When an excited hydrogen electron drops between two levels, it releases $\Delta E = 3.03 \times 10^{-19}\ \text{J}$. What wavelength (and color) is emitted?

**Solution:**
- **Step 1 — the emitted photon carries the whole gap:** $\dfrac{hc}{\lambda} = \Delta E$.
- **Step 2 — solve for** $\lambda$: $\lambda = \dfrac{hc}{\Delta E}$.
- **Step 3 — plug in:**
$$\lambda = \frac{(6.626 \times 10^{-34})(3.00 \times 10^{8})}{3.03 \times 10^{-19}} = 6.56 \times 10^{-7}\ \text{m} = 656\ \text{nm}$$

**Answer:** $\lambda = 656$ nm — the famous red line of hydrogen's Balmer series. A fixed energy gap gives a fixed color: that's the fingerprint.

### Example 7: Photoelectric Reasoning (Qualitative)
**Problem:** A metal ejects electrons when hit with green light. A student shines a *very bright* red light on it (lower frequency than green) and sees no electrons at all. They conclude the red beam "wasn't bright enough." Are they right?

**Solution:**
- **Step 1 — identify what matters.** Electron ejection depends on the **frequency** (energy *per photon*), not brightness (number of photons).
- **Step 2 — apply it.** Red light is below green in frequency, so each red photon is below the metal's **threshold frequency** — no single photon can pay the escape fee.
- **Step 3 — brightness can't fix it.** A brighter red beam is just *more* too-weak photons; an electron can't add up several photons.

**Answer:** The student is wrong. No amount of brightness ejects electrons below the threshold frequency — the problem is photon energy, not quantity. (This is the experiment that proved light is quantized into photons.)

### Example 8: Find an Unknown Concentration from Beer's Law
**Problem:** A solution of $\ce{KMnO4}$ has $\varepsilon = 2000\ \text{M}^{-1}\text{cm}^{-1}$ at 525 nm, measured in a 1.00 cm cuvette. Its absorbance reads $A = 0.52$. What is its concentration?

**Solution:**
- **Step 1 — solve** $A = \varepsilon b c$ **for** $c$: $c = \dfrac{A}{\varepsilon b}$.
- **Step 2 — plug in:** $c = \dfrac{0.52}{(2000\ \text{M}^{-1}\text{cm}^{-1})(1.00\ \text{cm})}$.

**Answer:** $c = 2.6 \times 10^{-4}\ \text{M}$.

### Example 9: Find the Molar Absorptivity
**Problem:** A $3.0 \times 10^{-4}\ \text{M}$ standard of $\ce{KMnO4}$ in a 1.00 cm cuvette gives $A = 0.60$. Find $\varepsilon$.

**Solution:**
- **Step 1 — solve for** $\varepsilon$: $\varepsilon = \dfrac{A}{b c}$.
- **Step 2 — plug in:** $\varepsilon = \dfrac{0.60}{(1.00\ \text{cm})(3.0 \times 10^{-4}\ \text{M})}$.

**Answer:** $\varepsilon = 2.0 \times 10^{3}\ \text{M}^{-1}\text{cm}^{-1}$. (Notice the units are exactly what's needed to cancel M and cm and leave $A$ unitless.)

### Example 10: Predict an Absorbance
**Problem:** Using $\varepsilon = 2000\ \text{M}^{-1}\text{cm}^{-1}$ and $b = 1.00$ cm, predict the absorbance of a $4.0 \times 10^{-4}\ \text{M}$ $\ce{KMnO4}$ solution.

**Solution:**
- **Step 1 — use** $A = \varepsilon b c$ **directly.**
- **Step 2 — plug in:** $A = (2000)(1.00)(4.0 \times 10^{-4})$.

**Answer:** $A = 0.80$. (Double the concentration of Example 8's ballpark, roughly double the absorbance — the line through the origin at work.)

### Example 11: Path Length Matters
**Problem:** A solution reads $A = 0.30$ in a 1.00 cm cuvette. If you pour the *same solution* into a 5.00 cm cuvette and remeasure at the same wavelength, what absorbance do you expect?

**Solution:**
- **Step 1 — only** $b$ **changed** in $A = \varepsilon b c$; $\varepsilon$ and $c$ are the same. So $A \propto b$.
- **Step 2 — scale:** the path length went up by a factor of 5, so $A = 0.30 \times 5 = 1.50$.

**Answer:** $A = 1.50$. Same drink, wider glass, darker reading — more liquid for the light to cross.

### Example 12: The "Dilute It" Lab Logic
**Problem:** An unknown $\ce{KMnO4}$ sample reads $A = 1.85$ — way above the top of your calibration line, in the region where the spectrophotometer is unreliable. You dilute exactly 5.00 mL of it up to 25.00 mL and remeasure: the diluted sample reads $A = 0.37$, which off your calibration curve corresponds to $c = 1.85 \times 10^{-4}\ \text{M}$. What was the original concentration?

**Solution:**
- **Step 1 — why dilute?** Reliable Beer's law readings sit roughly in $A \approx 0.1$–$1.0$. An $A$ of 1.85 means almost no light gets through, so the reading is untrustworthy — dilute until it drops into range.
- **Step 2 — find the dilution factor:** $\dfrac{25.00\ \text{mL}}{5.00\ \text{mL}} = 5.00$. You diluted 5-fold, so the true sample is 5× more concentrated than what you measured.
- **Step 3 — scale back up:** $c_{\text{original}} = 5.00 \times (1.85 \times 10^{-4}\ \text{M})$.

**Answer:** $c_{\text{original}} = 9.3 \times 10^{-4}\ \text{M}$. Measure diluted, then multiply back by the dilution factor.

### Example 13: The Full Calibration-Curve FRQ
**Problem:** You prepare five $\ce{KMnO4}$ standards and measure each in a 1.00 cm cuvette at 525 nm:

| Standard $c$ (M) | Absorbance $A$ |
|---|---|
| $1.0 \times 10^{-4}$ | 0.20 |
| $2.0 \times 10^{-4}$ | 0.40 |
| $3.0 \times 10^{-4}$ | 0.60 |
| $4.0 \times 10^{-4}$ | 0.80 |
| $5.0 \times 10^{-4}$ | 1.00 |

(a) Find the slope of the calibration line. (b) Find $\varepsilon$. (c) An unknown reads $A = 0.50$. Find its concentration.

**Solution:**
- **Step 1 — confirm it's linear through the origin.** Every point has $A / c = 2000$, and $c = 0$ would give $A = 0$. Good — it's $y = mx$.
- **Step 2 — (a) slope** from two points, say $(1.0\times10^{-4},\, 0.20)$ and $(5.0\times10^{-4},\, 1.00)$:
$$\text{slope} = \frac{1.00 - 0.20}{5.0\times10^{-4} - 1.0\times10^{-4}} = \frac{0.80}{4.0\times10^{-4}} = 2.0 \times 10^{3}\ \text{M}^{-1}$$
- **Step 3 — (b)** the slope *is* $\varepsilon b$. With $b = 1.00$ cm: $\varepsilon = \dfrac{\text{slope}}{b} = \dfrac{2.0 \times 10^{3}\ \text{M}^{-1}}{1.00\ \text{cm}} = 2.0 \times 10^{3}\ \text{M}^{-1}\text{cm}^{-1}$.
- **Step 4 — (c)** read the unknown off the line: $c = \dfrac{A}{\text{slope}} = \dfrac{0.50}{2.0 \times 10^{3}\ \text{M}^{-1}}$.

**Answer:** (a) slope $= 2.0 \times 10^{3}\ \text{M}^{-1}$; (b) $\varepsilon = 2.0 \times 10^{3}\ \text{M}^{-1}\text{cm}^{-1}$; (c) $c = 2.5 \times 10^{-4}\ \text{M}$ — safely *between* two standards, so this is **interpolation** (trustworthy), not extrapolation.

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Forgetting to convert nm → m | Wavelengths are quoted in nm, but $c$ and $h$ use meters | Always write $\lambda$ in meters ($1\ \text{nm} = 10^{-9}\ \text{m}$) *before* plugging in |
| Thinking longer wavelength = more energy | "Bigger number sounds bigger" | $E = hc/\lambda$: energy is *inversely* proportional to $\lambda$. Short = high |
| Saying brightness ejects electrons | Wave intuition says "more light = more push" | It's **frequency** (energy per photon), not brightness, that beats the threshold |
| Giving absorbance units | It looks like a measurement | $A$ is **unitless** — the units in $\varepsilon b c$ cancel exactly |
| Using $\varepsilon$ from a different wavelength or compound | $\varepsilon$ feels like a universal constant | $\varepsilon$ depends on *both* the species *and* the wavelength — it's only valid at the $\lambda$ it was measured at |
| Trusting an off-scale reading ($A > \sim 1.5$) | The machine still prints a number | Dilute until $A$ is in range, then multiply the result by the dilution factor |
| Extrapolating far past your standards | The line "keeps going" | Beer's law goes non-linear at high $c$; only interpolate within your standards |
| Confusing absorption with emission | Both involve light and energy gaps | Absorption = electron jumps **up** (light in); emission = falls **down** (light out) |

---

## AP Exam Tips

- **Unit discipline on $c = \lambda\nu$ and $E = hc/\lambda$.** The single most common lost point: leaving $\lambda$ in nm. Convert to meters first, keep $c = 3.00 \times 10^{8}\ \text{m/s}$ and $h = 6.626 \times 10^{-34}\ \text{J·s}$, and your energy comes out in joules. Both constants are on the AP formula/constants sheet — you don't memorize them, but you must use them correctly.
- **"Which has more energy?" is a wavelength/frequency question.** Shortest wavelength (or highest frequency) = highest energy, every time. Expect a ranking question.
- **Photoelectric effect = threshold *frequency*, not brightness.** If a free-response asks why increasing intensity doesn't eject electrons below threshold, the answer is: light is quantized into photons of energy $E = h\nu$; one photon ejects one electron; below threshold no single photon has enough energy, and more photons don't help.
- **Emission line spectra = evidence for quantized energy levels.** If asked why atoms emit *discrete lines* rather than a continuous rainbow, say: electrons occupy only specific (quantized) energy levels, so only specific gap energies — specific colors — can be emitted.
- **Beer's law is a linear calibration.** Know that $A = \varepsilon b c$ plots as a line **through the origin** with slope $\varepsilon b$. You'll be asked to find slope, extract $\varepsilon$, and **interpolate** an unknown. Reading between your standards = good; extrapolating beyond them = flagged as unreliable.
- **Explain $\lambda_{\text{max}}$ if asked.** You choose the wavelength of maximum absorbance for maximum sensitivity (biggest signal per unit concentration).
- **Dilution logic scores points.** If told an absorbance is off-scale, the expected move is: dilute, remeasure in range, then multiply back by the dilution factor.

---

## Practice Problems

### Problem 1
Red light has a wavelength of 700 nm. What is its frequency?

<details>
<summary><strong>Solution</strong></summary>

$\lambda = 700\ \text{nm} = 7.00 \times 10^{-7}\ \text{m}$. Then $\nu = \dfrac{c}{\lambda} = \dfrac{3.00 \times 10^{8}}{7.00 \times 10^{-7}}$.

**Answer:** $\nu = 4.29 \times 10^{14}\ \text{Hz}$.

</details>

---

### Problem 2
Find the energy of one photon of that 700 nm red light.

<details>
<summary><strong>Solution</strong></summary>

$E = \dfrac{hc}{\lambda} = \dfrac{(6.626 \times 10^{-34})(3.00 \times 10^{8})}{7.00 \times 10^{-7}}$.

**Answer:** $E = 2.84 \times 10^{-19}\ \text{J}$.

</details>

---

### Problem 3
A radio station broadcasts at $\nu = 98.5\ \text{MHz} = 9.85 \times 10^{7}\ \text{Hz}$. What is its wavelength?

<details>
<summary><strong>Solution</strong></summary>

$\lambda = \dfrac{c}{\nu} = \dfrac{3.00 \times 10^{8}}{9.85 \times 10^{7}}$.

**Answer:** $\lambda = 3.05\ \text{m}$ (radio waves are meters long — lowest energy end of the spectrum).

</details>

---

### Problem 4
Rank these three photons by increasing energy: $\lambda = 200\ \text{nm}$ (UV), $\lambda = 600\ \text{nm}$ (orange), $\nu = 5.0 \times 10^{12}\ \text{Hz}$ (infrared).

<details>
<summary><strong>Solution</strong></summary>

Convert the IR one to wavelength: $\lambda = c/\nu = (3.00\times10^{8})/(5.0\times10^{12}) = 6.0 \times 10^{-5}\ \text{m} = 60{,}000\ \text{nm}$. Now compare wavelengths: 200 nm < 600 nm < 60,000 nm, and energy is inverse to $\lambda$.

**Answer (increasing energy):** infrared < orange (600 nm) < UV (200 nm).

</details>

---

### Problem 5
Which probes bond *vibrations*: microwave, infrared, or ultraviolet radiation? Which probes *electronic transitions*?

<details>
<summary><strong>Solution</strong></summary>

**Infrared** excites bond vibrations (medium energy). **Ultraviolet** (and visible) excites electronic transitions (high energy). Microwave excites molecular rotations (low energy).

</details>

---

### Problem 6
Explain, in terms of photon energy, why a very bright infrared heat lamp will never give you a sunburn but ten minutes of midday sun will.

<details>
<summary><strong>Solution</strong></summary>

Sunburn requires photons energetic enough to damage skin molecules, which takes **UV** photons ($E = h\nu$, high frequency). Infrared photons have too low a frequency, so each one carries too little energy — and making the lamp brighter just sends *more* too-weak photons, not more energetic ones. The sun delivers genuine UV; the heat lamp doesn't.

**Answer:** Energy depends on frequency per photon, not brightness; IR photons are below the energy needed, UV photons aren't.

</details>

---

### Problem 7
An electron falls between two levels and emits a photon with $\Delta E = 4.58 \times 10^{-19}\ \text{J}$. What is the wavelength and roughly what color?

<details>
<summary><strong>Solution</strong></summary>

$\lambda = \dfrac{hc}{\Delta E} = \dfrac{(6.626 \times 10^{-34})(3.00 \times 10^{8})}{4.58 \times 10^{-19}} = 4.34 \times 10^{-7}\ \text{m} = 434\ \text{nm}$.

**Answer:** $\lambda = 434\ \text{nm}$ — blue-violet (this is another hydrogen Balmer line).

</details>

---

### Problem 8
Why do heated elements emit sharp bright lines of specific colors instead of a smooth continuous rainbow?

<details>
<summary><strong>Solution</strong></summary>

Electrons occupy only **quantized** (specific, discrete) energy levels. When an electron falls, the photon's energy equals the exact gap between two levels, $\Delta E = hc/\lambda$. Since only certain gaps exist, only certain photon energies — certain colors — are emitted, producing sharp lines. This discreteness is the experimental evidence for quantized energy levels (the Bohr model).

</details>

---

### Problem 9
A metal has a threshold frequency of $6.0 \times 10^{14}\ \text{Hz}$. You shine light of frequency $4.0 \times 10^{14}\ \text{Hz}$ on it at very high intensity. Do electrons eject? Explain.

<details>
<summary><strong>Solution</strong></summary>

No. The incoming frequency ($4.0 \times 10^{14}$ Hz) is **below** the threshold ($6.0 \times 10^{14}$ Hz), so each photon's energy $E = h\nu$ is too small to eject an electron. High intensity only means more photons, and an electron can't combine several sub-threshold photons.

**Answer:** No electrons ejected — frequency is below threshold, and brightness doesn't matter.

</details>

---

### Problem 10
A solution has $\varepsilon = 1500\ \text{M}^{-1}\text{cm}^{-1}$ at its $\lambda_{\text{max}}$. In a 1.00 cm cuvette it reads $A = 0.45$. Find the concentration.

<details>
<summary><strong>Solution</strong></summary>

$c = \dfrac{A}{\varepsilon b} = \dfrac{0.45}{(1500)(1.00)}$.

**Answer:** $c = 3.0 \times 10^{-4}\ \text{M}$.

</details>

---

### Problem 11
A $2.5 \times 10^{-4}\ \text{M}$ standard of a blue dye reads $A = 0.75$ in a 1.00 cm cell. Find $\varepsilon$, then predict $A$ for a $4.0 \times 10^{-4}\ \text{M}$ solution of the same dye in the same cell.

<details>
<summary><strong>Solution</strong></summary>

$\varepsilon = \dfrac{A}{bc} = \dfrac{0.75}{(1.00)(2.5\times10^{-4})} = 3.0 \times 10^{3}\ \text{M}^{-1}\text{cm}^{-1}$.

Predict: $A = \varepsilon b c = (3.0\times10^{3})(1.00)(4.0\times10^{-4}) = 1.2$.

**Answer:** $\varepsilon = 3.0 \times 10^{3}\ \text{M}^{-1}\text{cm}^{-1}$; predicted $A = 1.2$.

</details>

---

### Problem 12
The same solution reads $A = 0.24$ in a 1.00 cm cuvette. What would it read in a 2.50 cm cuvette at the same wavelength?

<details>
<summary><strong>Solution</strong></summary>

Only $b$ changes, and $A \propto b$: $A = 0.24 \times \dfrac{2.50}{1.00} = 0.24 \times 2.50$.

**Answer:** $A = 0.60$.

</details>

---

### Problem 13
Why do chemists run Beer's law measurements at the wavelength of maximum absorbance ($\lambda_{\text{max}}$)?

<details>
<summary><strong>Solution</strong></summary>

At $\lambda_{\text{max}}$ the molar absorptivity $\varepsilon$ is largest, so absorbance changes the most per unit concentration — maximum **sensitivity**. Also, the absorbance curve is flat near its peak, so small errors in setting the wavelength barely affect the reading.

</details>

---

### Problem 14
You build a calibration curve for a red food dye and get a best-fit line $A = 4.0 \times 10^{3}\,c$ (with $c$ in M, 1.00 cm cell). (a) What is $\varepsilon$? (b) An unknown reads $A = 0.68$. Find $c$. (c) Another sample reads $A = 2.9$ — should you trust a concentration read off this line? What should you do?

<details>
<summary><strong>Solution</strong></summary>

(a) Slope $= \varepsilon b = 4.0 \times 10^{3}\ \text{M}^{-1}$, and $b = 1.00$ cm, so $\varepsilon = 4.0 \times 10^{3}\ \text{M}^{-1}\text{cm}^{-1}$.

(b) $c = \dfrac{A}{4.0\times10^{3}} = \dfrac{0.68}{4.0\times10^{3}} = 1.7 \times 10^{-4}\ \text{M}$.

(c) No — $A = 2.9$ is far off-scale (well above ~1.5), where the reading is unreliable and beyond the calibrated range (extrapolation). **Dilute** the sample by a known factor, remeasure so $A$ falls in range, read $c$ off the line, then multiply back by the dilution factor.

</details>

---

### Problem 15
An unknown $\ce{KMnO4}$ solution reads $A = 2.1$ (off-scale). You dilute 10.00 mL to 50.00 mL and remeasure: $A = 0.42$, which corresponds to $c = 2.1 \times 10^{-4}\ \text{M}$ on the calibration curve. What was the original concentration?

<details>
<summary><strong>Solution</strong></summary>

Dilution factor $= \dfrac{50.00\ \text{mL}}{10.00\ \text{mL}} = 5.00$. The original is 5× more concentrated than the diluted reading:

$c_{\text{original}} = 5.00 \times (2.1 \times 10^{-4}\ \text{M})$.

**Answer:** $c_{\text{original}} = 1.05 \times 10^{-3}\ \text{M} \approx 1.1 \times 10^{-3}\ \text{M}$.

</details>

---

## Quick Reference

| Concept | Formula / Rule | Notes |
|---|---|---|
| Speed of light | $c = \lambda\nu = 3.00 \times 10^{8}\ \text{m/s}$ | $\lambda$ and $\nu$ trade off |
| Photon energy | $E = h\nu = \dfrac{hc}{\lambda}$ | $h = 6.626 \times 10^{-34}\ \text{J·s}$ |
| Energy vs wavelength | short $\lambda$ = high $\nu$ = high $E$ | UV burns, IR doesn't |
| Spectrum order (low→high $E$) | radio, microwave, IR, visible, UV, X-ray, gamma | rotations, vibrations, electronic... |
| Absorption / emission | $\Delta E = hc/\lambda$ | up = absorb, down = emit; lines = quantized levels |
| Photoelectric effect | threshold **frequency**, not brightness | proof light = photons |
| Beer-Lambert law | $A = \varepsilon b c$ | $A$ unitless; $\varepsilon$ in $\text{M}^{-1}\text{cm}^{-1}$; $b$ in cm |
| Calibration curve | $A$ vs $c$: line through origin, slope $= \varepsilon b$ | interpolate, don't extrapolate |
| Best wavelength | run at $\lambda_{\text{max}}$ | maximum sensitivity |
| Off-scale reading | dilute, remeasure, multiply back | keep $A$ roughly 0.1–1.0 |

---

<div align="center">

[← Solubility and Separation](/chemistry/0507-solubility-and-separation) | [Net Ionic Equations →](/chemistry/0601-net-ionic-equations)

</div>
