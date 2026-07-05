# The Ideal Gas Law
<p class="article-date">July 5, 2026</p>

*Last summer Dad and I drove up from San Diego toward Big Bear, and I bought a fat bag of chips at a gas station near the coast. We tossed it in the cupholder, sealed and forgetting about it. An hour later, climbing the mountain switchbacks, the bag was puffed up like a little pillow — tight as a drum, ready to pop. Nobody added any air. What changed was the world outside: at sea level the air presses hard on the bag, but a mile up the outside air is thinner and pushes back less, so the gas trapped inside expanded to shove the bag walls outward until things balanced again. That's Boyle's law happening live in the cupholder. Then that night, camping in the freezing dark, the same bag looked a little shrunken and floppy — the cold air inside had lost energy and pulled in. One snack bag, sealed the whole trip, quietly demonstrated the entire gas law: pressure, volume, temperature, all wired together. This article is where all of that becomes a single equation, $\ce{PV=nRT}$, the most-used formula in AP Chemistry after the mole itself.*

---

## What You'll Learn

- Identify the four gas variables — pressure $P$, volume $V$, moles $n$, temperature $T$ — and state the correct units for each, always converting temperature to **Kelvin**
- Convert between pressure units: atm, kPa, mmHg, and torr
- Explain why the value of the gas constant $R$ depends on which units you use, and pick the right $R$ for a problem
- Use the simple gas laws — Boyle's, Charles's, Gay-Lussac's, and Avogadro's — as special cases where two variables are held constant
- Apply the combined gas law $\dfrac{P_1V_1}{T_1}=\dfrac{P_2V_2}{T_2}$ to before-and-after problems
- Solve the ideal gas law $\ce{PV=nRT}$ for any one of its four variables
- Define STP and use the molar volume $22.4$ L/mol
- Find gas density and molar mass from $M = \dfrac{dRT}{P}$, and identify an unknown gas
- Preview gas stoichiometry, and apply Dalton's law of partial pressures — including collecting a gas over water

---

## Prerequisites

- [Dimensional Analysis](/chemistry/0103-dimensional-analysis) — every gas problem is a unit war; you'll be converting mL to L, torr to atm, and °C to K on nearly every line
- [The Mole](/chemistry/0207-the-mole) — the $n$ in $\ce{PV=nRT}$ is moles, and to get molar mass or run stoichiometry you'll convert to and from moles constantly

---

## The Core Concept

### Intuition First

Go back to that chip bag in the cupholder. The bag is sealed, so the *amount* of gas trapped inside never changes the whole trip — same molecules the entire time. What changes is everything around them.

Here's the mental model that makes gases click: picture **four dials wired together on a control panel** — pressure ($P$), volume ($V$), moles ($n$), and temperature ($T$). They aren't independent. Turn one dial and at least one other dial *must* respond, because the wiring won't let all four move freely. The equation $\ce{PV=nRT}$ is the wiring diagram — it's the exact rule for how the dials are connected.

Watch the chip bag turn the dials:

- **Driving up the mountain (Boyle).** The moles $n$ are locked (sealed bag). The temperature $T$ barely changes over one hour. But the outside pressure drops, so the pressure balance shifts and the volume $V$ expands — the bag puffs up. Pressure down, volume up. Two dials moving in opposite directions.
- **That freezing night (Charles / Gay-Lussac).** Now the temperature dial drops hard. Cold gas molecules move slower and hit the bag walls less often and less hard, so either the volume shrinks (floppy bag) or, if the bag were rigid, the internal pressure would fall. The temperature dial dragged another dial down with it.

No air was ever added or removed. The bag is a little laboratory proving that $P$, $V$, and $T$ are chained together. The rest of this article is just learning to read the wiring diagram in every direction.

A quick, honest caveat: the "ideal" gas law is a *model*. It assumes gas particles are tiny points that don't attract each other and bounce perfectly. Real gases fudge this a little (we'll see how in Kinetic Molecular Theory), but for the temperatures and pressures on the AP exam, the model is excellent — treat $\ce{PV=nRT}$ as the truth.

### The Four Variables and Their Units

Every gas problem is really a units problem in disguise. Get these right and half the battle is over.

| Variable | Symbol | Standard unit | Watch out for |
|---|---|---|---|
| Pressure | $P$ | atmospheres (atm) | Problems love to give kPa, mmHg, or torr instead |
| Volume | $V$ | liters (L) | mL is everywhere — divide by 1000 |
| Moles | $n$ | moles (mol) | Often you're given grams — convert with molar mass first |
| Temperature | $T$ | **Kelvin (K)** | **NEVER Celsius.** This is the #1 killer |

**Temperature — always Kelvin.** I'm putting this in its own paragraph because it is the single most common way to blow a gas problem. The gas laws work with *absolute* temperature, measured from absolute zero. To convert:

$$T(\text{K}) = T(\text{°C}) + 273.15$$

On the AP exam, using $+273$ is fine. If a problem hands you $25\,\text{°C}$ and you plug in $25$, you will get a wrong answer every time. Convert first, then breathe, then solve.

**Pressure — one quantity, four costumes.** Pressure is force per area, and it shows up dressed in several unit systems. Memorize this equivalence chain:

$$1 \ \text{atm} = 760 \ \text{mmHg} = 760 \ \text{torr} = 101.325 \ \text{kPa} = 760 \ \text{Torr}$$

So mmHg and torr are the *same size* (1 mmHg = 1 torr), and there are 760 of each in one atmosphere. kPa is the metric/SI unit, with 101.325 kPa per atm (round to 101.3 for AP work).

### The Gas Constant $R$ — and Why Units Dictate Its Value

The $R$ in $\ce{PV=nRT}$ is the proportionality constant that makes the wiring exact. Here's the subtle part: **$R$ has units, and its numerical value depends entirely on what units you use for $P$ and $V$.** It's the same physical constant, just wearing different clothes to match the room.

| Value of $R$ | Units | Use when pressure is in... |
|---|---|---|
| $0.08206$ | $\dfrac{\text{L·atm}}{\text{mol·K}}$ | **atm** (the one to memorize) |
| $8.314$ | $\dfrac{\text{L·kPa}}{\text{mol·K}}$ | kPa (also $\text{J/(mol·K)}$) |
| $62.36$ | $\dfrac{\text{L·mmHg}}{\text{mol·K}}$ | mmHg or torr |

For AP Chemistry, memorize $R = 0.08206 \ \dfrac{\text{L·atm}}{\text{mol·K}}$. Then **the rule is simple: convert your pressure to atm and your volume to L, and this $R$ always works.** The units inside $R$ literally tell you what units the rest of the equation must be in — L, atm, mol, K. If your numbers don't match those, convert until they do.

### The Ideal Gas Law and Its Special Cases

Here is the master equation — the full wiring diagram:

$$\ce{PV = nRT}$$

Every "simple" gas law is just this equation with two dials **taped down** (held constant). When you freeze two variables, $R$ and the frozen values fold into a single constant, and you're left with a clean relationship between the two dials that can still move.

$$\underbrace{\ce{PV=nRT}}_{\text{turn all four dials}} \quad\longrightarrow\quad \underbrace{\text{Boyle, Charles, Gay-Lussac, Avogadro}}_{\text{tape two down, watch the other two}}$$

Let's meet them one at a time.

### Boyle's Law — $P$ and $V$ (the chip bag)

**Hold $n$ and $T$ constant.** Then $PV = \text{constant}$, so pressure and volume are *inversely* related — squeeze one, the other grows:

$$P_1 V_1 = P_2 V_2$$

**The graph:** plot $P$ vs. $V$ and you get a downward-sweeping curve (a hyperbola) — as volume rises, pressure falls. Plot $P$ vs. $1/V$ and you get a straight line through the origin, because $P \propto 1/V$.

This is the chip bag driving up the mountain: same gas, same temperature, outside pressure drops → the trapped gas volume expands.

### Charles's Law — $V$ and $T$ (a balloon in the freezer)

**Hold $n$ and $P$ constant.** Then $V/T = \text{constant}$, so volume and Kelvin temperature are *directly* related — heat it, it grows:

$$\frac{V_1}{T_1} = \frac{V_2}{T_2}$$

**The graph:** $V$ vs. $T$ (in Kelvin) is a straight line that, extended backward, hits zero volume at $0$ K — that's absolute zero, the reason Kelvin exists.

Stuff an inflated balloon in the freezer and it visibly deflates; pull it into a warm room and it re-inflates. Same air, just colder or warmer molecules.

### Gay-Lussac's Law — $P$ and $T$ (tire pressure on a cold morning)

**Hold $n$ and $V$ constant** (a rigid container). Then $P/T = \text{constant}$ — pressure and Kelvin temperature rise and fall together:

$$\frac{P_1}{T_1} = \frac{P_2}{T_2}$$

**The graph:** $P$ vs. $T$ (Kelvin) is a straight line through the origin.

This is why the "check tire pressure" light glows on the first freezing morning of winter. Your tires are a fixed volume of gas; overnight the temperature dropped, so the pressure inside dropped too — nothing leaked. Drive a while, the tires warm up, the light often goes off.

### Avogadro's Law — $V$ and $n$

**Hold $P$ and $T$ constant.** Then $V/n = \text{constant}$ — more gas molecules take up proportionally more volume:

$$\frac{V_1}{n_1} = \frac{V_2}{n_2}$$

**The graph:** $V$ vs. $n$ is a straight line through the origin. This is just blowing up a balloon — every breath adds moles and adds volume.

---

## Worked Examples

### Example 1: Converting Pressure Units

**Problem:** The weather app says the pressure at the Julian summit is $88.5 \ \text{kPa}$. Express this in (a) atm and (b) mmHg.

**Solution:**

**Step 1:** Use the chain $1 \ \text{atm} = 101.325 \ \text{kPa} = 760 \ \text{mmHg}$ as conversion factors.

(a) kPa → atm:

$$88.5 \ \cancel{\text{kPa}} \times \frac{1 \ \text{atm}}{101.325 \ \cancel{\text{kPa}}} = 0.873 \ \text{atm}$$

(b) atm → mmHg:

$$0.873 \ \cancel{\text{atm}} \times \frac{760 \ \text{mmHg}}{1 \ \cancel{\text{atm}}} = 664 \ \text{mmHg}$$

**Answer: 0.873 atm, which is 664 mmHg (≈ 664 torr).**

### Example 2: Boyle's Law — the Chip Bag

**Problem:** A sealed chip bag holds $250 \ \text{mL}$ of gas at sea level ($1.00 \ \text{atm}$). We drive to Big Bear, where the pressure is $0.80 \ \text{atm}$. Assuming the temperature doesn't change, what's the new volume of gas in the bag?

**Solution:**

**Step 1:** Only $P$ and $V$ change; $n$ and $T$ are constant → Boyle's law. Use $P_1V_1 = P_2V_2$.

**Step 2:** Solve for $V_2$:

$$V_2 = \frac{P_1 V_1}{P_2} = \frac{(1.00 \ \text{atm})(250 \ \text{mL})}{0.80 \ \text{atm}} = 313 \ \text{mL}$$

**Answer: 313 mL.** The bag swells by about 25% — exactly the puffed-up pillow we saw. (Units of mL are fine here since they appear on both sides and cancel.)

### Example 3: Charles's Law — the Freezer Balloon

**Problem:** A balloon has a volume of $2.0 \ \text{L}$ in a $27 \ \text{°C}$ room. I put it in the freezer at $-18 \ \text{°C}$. What's its new volume (pressure constant)?

**Solution:**

**Step 1:** $V$ and $T$ change, $P$ and $n$ constant → Charles's law. **Convert to Kelvin first:**

$$T_1 = 27 + 273 = 300 \ \text{K}, \qquad T_2 = -18 + 273 = 255 \ \text{K}$$

**Step 2:** Solve $\dfrac{V_1}{T_1} = \dfrac{V_2}{T_2}$ for $V_2$:

$$V_2 = V_1 \cdot \frac{T_2}{T_1} = 2.0 \ \text{L} \times \frac{255 \ \text{K}}{300 \ \text{K}} = 1.7 \ \text{L}$$

**Answer: 1.7 L.** Colder gas, smaller balloon. If you'd left the temperatures in Celsius you'd have gotten $2.0 \times (-18/27) = -1.3$ L — a *negative volume*, which is nonsense and a giant red flag that you forgot Kelvin.

### Example 4: Gay-Lussac's Law — Cold-Morning Tires

**Problem:** A car tire is filled to $32.0 \ \text{psi}$ (a pressure unit) at $25 \ \text{°C}$. Overnight the temperature drops to $-5 \ \text{°C}$. The tire is essentially rigid. What's the new pressure?

**Solution:**

**Step 1:** $P$ and $T$ change, $V$ and $n$ constant → Gay-Lussac. Convert to Kelvin:

$$T_1 = 25 + 273 = 298 \ \text{K}, \qquad T_2 = -5 + 273 = 268 \ \text{K}$$

**Step 2:** Solve $\dfrac{P_1}{T_1} = \dfrac{P_2}{T_2}$:

$$P_2 = P_1 \cdot \frac{T_2}{T_1} = 32.0 \ \text{psi} \times \frac{268 \ \text{K}}{298 \ \text{K}} = 28.8 \ \text{psi}$$

**Answer: 28.8 psi.** The pressure dropped over 3 psi with nothing leaking — that's the "check tire pressure" light. (psi cancels, so no conversion needed here.)

### Example 5: Combined Gas Law — Before and After

**Problem:** A weather balloon holds $15.0 \ \text{L}$ of helium at ground level: $1.00 \ \text{atm}$ and $20.0 \ \text{°C}$. It rises to where the pressure is $0.500 \ \text{atm}$ and the temperature is $-30.0 \ \text{°C}$. Find the new volume.

**Solution:**

**Step 1:** Three variables change ($P$, $V$, $T$), $n$ is constant → combined gas law:

$$\frac{P_1 V_1}{T_1} = \frac{P_2 V_2}{T_2}$$

**Step 2:** Convert temperatures to Kelvin:

$$T_1 = 20.0 + 273 = 293 \ \text{K}, \qquad T_2 = -30.0 + 273 = 243 \ \text{K}$$

**Step 3:** Solve for $V_2$:

$$V_2 = V_1 \cdot \frac{P_1}{P_2} \cdot \frac{T_2}{T_1} = 15.0 \ \text{L} \times \frac{1.00}{0.500} \times \frac{243}{293} = 24.9 \ \text{L}$$

**Answer: 24.9 L.** Lower pressure pushes the volume up; lower temperature tugs it back down a bit — the two effects fight, and pressure wins.

### Example 6: Combined Gas Law — Solving for Temperature

**Problem:** A rigid $2.00 \ \text{L}$ steel cylinder holds gas at $3.0 \ \text{atm}$ and $300 \ \text{K}$. We compress and heat it until it reads $9.0 \ \text{atm}$; the volume is still $2.00 \ \text{L}$ (rigid). What's the new temperature?

**Solution:**

**Step 1:** Volume is constant, so it cancels — this collapses to Gay-Lussac, but let's use the combined law to see it:

$$\frac{P_1 \cancel{V}}{T_1} = \frac{P_2 \cancel{V}}{T_2} \;\Rightarrow\; T_2 = T_1 \cdot \frac{P_2}{P_1}$$

**Step 2:** Plug in:

$$T_2 = 300 \ \text{K} \times \frac{9.0 \ \text{atm}}{3.0 \ \text{atm}} = 900 \ \text{K}$$

**Answer: 900 K.** Tripling the pressure at fixed volume triples the Kelvin temperature.

### Example 7: Ideal Gas Law — Solving for Pressure

**Problem:** What pressure does $0.500 \ \text{mol}$ of $\ce{O2}$ exert in a $2.00 \ \text{L}$ container at $25.0 \ \text{°C}$?

**Solution:**

**Step 1:** We know $n$, $V$, $T$ and want $P$ → use $\ce{PV=nRT}$, solve for $P$:

$$P = \frac{nRT}{V}$$

**Step 2:** Convert temperature: $T = 25.0 + 273 = 298 \ \text{K}$. Because pressure is unknown and we want atm, use $R = 0.08206$.

**Step 3:** Plug in:

$$P = \frac{(0.500 \ \text{mol})(0.08206 \ \tfrac{\text{L·atm}}{\text{mol·K}})(298 \ \text{K})}{2.00 \ \text{L}} = 6.11 \ \text{atm}$$

**Answer: 6.11 atm.** Notice how mol, L, and K all cancel against the units inside $R$, leaving atm — that's your check that you set it up right.

### Example 8: Ideal Gas Law — Solving for Moles (and grams)

**Problem:** A $5.00 \ \text{L}$ tank holds $\ce{N2}$ at $2.50 \ \text{atm}$ and $310 \ \text{K}$. How many moles are in the tank? How many grams?

**Solution:**

**Step 1:** Want $n$ → solve $\ce{PV=nRT}$ for $n$:

$$n = \frac{PV}{RT} = \frac{(2.50 \ \text{atm})(5.00 \ \text{L})}{(0.08206 \ \tfrac{\text{L·atm}}{\text{mol·K}})(310 \ \text{K})} = 0.491 \ \text{mol}$$

**Step 2:** Convert to grams using the molar mass of $\ce{N2}$ ($28.02$ g/mol):

$$0.491 \ \cancel{\text{mol}} \times \frac{28.02 \ \text{g}}{1 \ \cancel{\text{mol}}} = 13.8 \ \text{g}$$

**Answer: 0.491 mol, which is 13.8 g of $\ce{N2}$.**

### Example 9: STP and Molar Volume

**Problem:** What volume does $3.00 \ \text{mol}$ of any ideal gas occupy at STP?

**Solution:**

**Step 1:** **STP** (Standard Temperature and Pressure) on the AP exam means $0 \ \text{°C} = 273.15 \ \text{K}$ and $1 \ \text{atm}$. At STP, one mole of *any* ideal gas occupies the **molar volume**:

$$V_m = \frac{RT}{P} = \frac{(0.08206)(273.15)}{1.00} = 22.4 \ \text{L/mol}$$

**Step 2:** Multiply:

$$3.00 \ \cancel{\text{mol}} \times \frac{22.4 \ \text{L}}{1 \ \cancel{\text{mol}}} = 67.2 \ \text{L}$$

**Answer: 67.2 L.** The $22.4$ L/mol shortcut only works *at STP* — the moment temperature or pressure changes, go back to $\ce{PV=nRT}$.

### Example 10: Molar Mass from Gas Density

**Problem:** An unknown gas has a density of $1.96 \ \text{g/L}$ at $1.00 \ \text{atm}$ and $273 \ \text{K}$ (STP). What is its molar mass, and what might the gas be?

**Solution:**

**Step 1:** Start from $\ce{PV=nRT}$ and remember that $n = \dfrac{m}{M}$ (moles = mass ÷ molar mass). Substitute:

$$PV = \frac{m}{M}RT \;\Rightarrow\; M = \frac{m}{V}\cdot\frac{RT}{P} = \frac{dRT}{P}$$

where $d = m/V$ is the density. This is the density–molar mass formula.

**Step 2:** Plug in $d = 1.96$ g/L, $T = 273$ K, $P = 1.00$ atm:

$$M = \frac{(1.96 \ \tfrac{\text{g}}{\text{L}})(0.08206 \ \tfrac{\text{L·atm}}{\text{mol·K}})(273 \ \text{K})}{1.00 \ \text{atm}} = 43.9 \ \text{g/mol}$$

**Step 3:** Identify it. $43.9$ g/mol is very close to $\ce{CO2}$ ($44.01$ g/mol).

**Answer: $M \approx 43.9$ g/mol — the gas is carbon dioxide, $\ce{CO2}$.**

### Example 11: Identifying an Unknown Gas (not at STP)

**Problem:** A gas has a density of $1.34 \ \text{g/L}$ at $27 \ \text{°C}$ and $0.987 \ \text{atm}$. Identify it.

**Solution:**

**Step 1:** Convert temperature: $T = 27 + 273 = 300 \ \text{K}$. Since we're not at STP, we *must* use $M = \dfrac{dRT}{P}$.

**Step 2:** Plug in:

$$M = \frac{(1.34)(0.08206)(300)}{0.987} = 33.4 \ \text{g/mol}$$

**Step 3:** What's near 33 g/mol? Oxygen ($\ce{O2}$) is 32.00; hydrogen sulfide ($\ce{H2S}$) is 34.08. The closest common gas is $\ce{H2S}$.

**Answer: $M \approx 33.4$ g/mol — most likely $\ce{H2S}$ (or $\ce{O2}$ if the context is a rounding-heavy problem).**

### Example 12: Gas Stoichiometry Teaser

**Problem:** Zinc reacts with acid to make hydrogen gas: $\ce{Zn(s) + 2HCl(aq) -> ZnCl2(aq) + H2(g)}$. If $0.150 \ \text{mol}$ of $\ce{Zn}$ fully reacts, what volume of $\ce{H2}$ is produced at $25 \ \text{°C}$ and $1.00 \ \text{atm}$?

**Solution:**

**Step 1:** Use the mole ratio from the balanced equation. 1 mol $\ce{Zn}$ makes 1 mol $\ce{H2}$:

$$0.150 \ \cancel{\text{mol Zn}} \times \frac{1 \ \text{mol } \ce{H2}}{1 \ \cancel{\text{mol Zn}}} = 0.150 \ \text{mol } \ce{H2}$$

**Step 2:** Now turn moles of gas into a volume with $\ce{PV=nRT}$. Convert temperature: $T = 298$ K.

$$V = \frac{nRT}{P} = \frac{(0.150)(0.08206)(298)}{1.00} = 3.67 \ \text{L}$$

**Answer: 3.67 L of $\ce{H2}$.** This is the whole idea of gas stoichiometry: use a mole ratio to get moles of gas, then $\ce{PV=nRT}$ to get its volume. The full treatment is coming in [Kinetic Molecular Theory](/chemistry/0505-kinetic-molecular-theory) and AP Unit 4.

### Example 13: Dalton's Law — Total Pressure from Partials

**Problem:** A container holds three gases: $\ce{N2}$ at $0.60 \ \text{atm}$, $\ce{O2}$ at $0.25 \ \text{atm}$, and $\ce{CO2}$ at $0.10 \ \text{atm}$. What is the total pressure? What is the mole fraction of $\ce{O2}$?

**Solution:**

**Step 1:** Dalton's law: the total pressure is just the sum of the individual (partial) pressures:

$$P_\text{total} = P_{\ce{N2}} + P_{\ce{O2}} + P_{\ce{CO2}} = 0.60 + 0.25 + 0.10 = 0.95 \ \text{atm}$$

**Step 2:** The **mole fraction** of a gas is its partial pressure over the total (equivalently, its moles over total moles):

$$X_{\ce{O2}} = \frac{P_{\ce{O2}}}{P_\text{total}} = \frac{0.25}{0.95} = 0.26$$

**Answer: $P_\text{total} = 0.95$ atm; the mole fraction of $\ce{O2}$ is $0.26$.**

### Example 14: Dalton's Law — Partial Pressure from Mole Fraction

**Problem:** A gas mixture is $75\%$ $\ce{N2}$ and $25\%$ $\ce{O2}$ by moles, at a total pressure of $2.00 \ \text{atm}$. Find each partial pressure.

**Solution:**

**Step 1:** The partial pressure equals the mole fraction times the total pressure: $P_i = X_i \cdot P_\text{total}$.

**Step 2:**

$$P_{\ce{N2}} = 0.75 \times 2.00 = 1.50 \ \text{atm}, \qquad P_{\ce{O2}} = 0.25 \times 2.00 = 0.50 \ \text{atm}$$

**Answer: $P_{\ce{N2}} = 1.50$ atm, $P_{\ce{O2}} = 0.50$ atm.** (They sum back to 2.00 atm — always check.)

### Example 15: Collecting a Gas Over Water

**Problem:** Hydrogen gas is collected over water at $25 \ \text{°C}$. The total pressure in the collection tube is $755 \ \text{mmHg}$. At $25 \ \text{°C}$, the vapor pressure of water is $23.8 \ \text{mmHg}$. What is the pressure of the *dry* $\ce{H2}$ gas, and how many moles were collected if the volume is $0.250 \ \text{L}$?

**Solution:**

**Step 1:** When you bubble a gas up through water, it mixes with water vapor. By Dalton's law, the measured total pressure is the gas *plus* water vapor. Subtract the water's contribution:

$$P_{\ce{H2}} = P_\text{total} - P_{\ce{H2O}} = 755 - 23.8 = 731 \ \text{mmHg}$$

**Step 2:** Convert to atm for our $R$:

$$731 \ \cancel{\text{mmHg}} \times \frac{1 \ \text{atm}}{760 \ \cancel{\text{mmHg}}} = 0.962 \ \text{atm}$$

**Step 3:** Convert temperature ($T = 298$ K) and solve $\ce{PV=nRT}$ for $n$:

$$n = \frac{PV}{RT} = \frac{(0.962)(0.250)}{(0.08206)(298)} = 9.83 \times 10^{-3} \ \text{mol}$$

**Answer: The dry $\ce{H2}$ pressure is 731 mmHg (0.962 atm), and $9.83 \times 10^{-3}$ mol was collected.** Forgetting to subtract the water vapor is the classic gas-over-water mistake — and it's a favorite AP setup.

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| **Using Celsius instead of Kelvin** (the #1 killer) | Habit — we live in Celsius/Fahrenheit | *Before anything else,* convert every temperature: $T(\text{K}) = T(\text{°C}) + 273$. A negative or absurd answer is your warning siren |
| **Mismatched $R$ units** | Grabbing $0.08206$ while pressure is in kPa or mmHg | Pick $R$ to match the pressure unit — or better, convert pressure to atm and always use $0.08206$ |
| **Leaving volume in mL** | Problems give mL, syringes, tubes | Convert mL → L (÷1000) before plugging in; $R$ demands liters |
| **Leaving pressure in mmHg/torr/kPa** | The problem states it that way | Convert to atm first: $\div 760$ (mmHg/torr) or $\div 101.3$ (kPa) |
| **Using $22.4$ L/mol when NOT at STP** | It's a comforting shortcut | Molar volume is $22.4$ L/mol *only* at $0\,\text{°C}$ and $1$ atm; otherwise use $\ce{PV=nRT}$ |
| **Forgetting to subtract water vapor** | "Total pressure" looks like the answer | Gas over water: $P_\text{gas} = P_\text{total} - P_{\ce{H2O}}$, always |
| **Reversing a direct/inverse relationship** | Panic-guessing which way $V$ moves | Ask: does the wiring make them move together (direct) or opposite (inverse)? $P$–$V$ opposite; $V$–$T$, $P$–$T$, $V$–$n$ together |

---

## AP Exam Tips

- **Always Kelvin, no exceptions.** Graders see thousands of gas-law FRQs sunk by a Celsius plug-in. Convert temperature the instant you read it, and write "K" next to the number.
- **Pick $R$ by the pressure unit.** The reference sheet gives you $R = 0.08206 \ \frac{\text{L·atm}}{\text{mol·K}}$ and $R = 8.314 \ \frac{\text{J}}{\text{mol·K}}$. For ordinary $\ce{PV=nRT}$ problems in atm and L, use $0.08206$. Match units or convert.
- **Carry units through the whole calculation.** If your units don't cancel down to what you want (atm, L, mol, or K), you've made a setup error — units are a free error-checker.
- **Dalton's law and gas-over-water show up on FRQs constantly.** Expect a lab scenario where a gas is collected over water and you must subtract the water's vapor pressure before using $\ce{PV=nRT}$. Know this cold.
- **Density and molar mass link gases to identity.** The $M = \frac{dRT}{P}$ move — "here's a density, name the gas" — is a common multiple-choice and FRQ task. Recognize it instantly.
- **STP is $0\,\text{°C}$ and $1$ atm** on the AP exam, giving molar volume $22.4$ L/mol. Use the shortcut only when the problem is *at* STP.
- **Show the plug-in.** On FRQs, writing the equation with numbers and units substituted earns setup points even if your arithmetic slips.

---

## Practice Problems

### Problem 1
Convert $2.5 \ \text{atm}$ into (a) mmHg, (b) kPa, and (c) torr.

<details>
<summary><strong>Solution</strong></summary>

(a) $2.5 \times 760 = 1900 \ \text{mmHg}$
(b) $2.5 \times 101.325 = 253 \ \text{kPa}$
(c) mmHg and torr are equal, so **1900 torr**.

**Answer: 1900 mmHg, 253 kPa, 1900 torr.**

</details>

---

### Problem 2
Convert $37\,\text{°C}$ (human body temperature) to Kelvin, and convert $500 \ \text{K}$ back to °C.

<details>
<summary><strong>Solution</strong></summary>

$37 + 273 = 310 \ \text{K}$.

$500 - 273 = 227 \ \text{°C}$.

**Answer: 310 K; 227 °C.**

</details>

---

### Problem 3
A gas occupies $4.0 \ \text{L}$ at $2.0 \ \text{atm}$. If the temperature and amount stay constant, what volume will it occupy at $5.0 \ \text{atm}$?

<details>
<summary><strong>Solution</strong></summary>

Boyle's law, $P_1V_1 = P_2V_2$:

$$V_2 = \frac{P_1V_1}{P_2} = \frac{(2.0)(4.0)}{5.0} = 1.6 \ \text{L}$$

**Answer: 1.6 L.** Higher pressure, smaller volume — inverse, as expected.

</details>

---

### Problem 4
A balloon is $3.5 \ \text{L}$ at $300 \ \text{K}$. At constant pressure, what is its volume at $450 \ \text{K}$?

<details>
<summary><strong>Solution</strong></summary>

Charles's law, $\dfrac{V_1}{T_1} = \dfrac{V_2}{T_2}$ (already in Kelvin):

$$V_2 = 3.5 \times \frac{450}{300} = 5.25 \ \text{L} \approx 5.3 \ \text{L}$$

**Answer: 5.3 L.**

</details>

---

### Problem 5
A rigid canister reads $1.8 \ \text{atm}$ at $20\,\text{°C}$. What pressure will it read at $80\,\text{°C}$?

<details>
<summary><strong>Solution</strong></summary>

Gay-Lussac. Convert: $T_1 = 293$ K, $T_2 = 353$ K.

$$P_2 = P_1 \cdot \frac{T_2}{T_1} = 1.8 \times \frac{353}{293} = 2.2 \ \text{atm}$$

**Answer: 2.2 atm.**

</details>

---

### Problem 6
A gas is $6.0 \ \text{L}$ at $2.0 \ \text{atm}$ and $300 \ \text{K}$. What volume does it occupy at $1.5 \ \text{atm}$ and $350 \ \text{K}$?

<details>
<summary><strong>Solution</strong></summary>

Combined gas law:

$$V_2 = V_1 \cdot \frac{P_1}{P_2} \cdot \frac{T_2}{T_1} = 6.0 \times \frac{2.0}{1.5} \times \frac{350}{300} = 9.3 \ \text{L}$$

**Answer: 9.3 L.**

</details>

---

### Problem 7
How many moles of gas are in a $10.0 \ \text{L}$ container at $1.50 \ \text{atm}$ and $273 \ \text{K}$?

<details>
<summary><strong>Solution</strong></summary>

$$n = \frac{PV}{RT} = \frac{(1.50)(10.0)}{(0.08206)(273)} = 0.670 \ \text{mol}$$

**Answer: 0.670 mol.**

</details>

---

### Problem 8
What is the temperature (in °C) of $0.50 \ \text{mol}$ of gas that occupies $12.0 \ \text{L}$ at $1.00 \ \text{atm}$?

<details>
<summary><strong>Solution</strong></summary>

$$T = \frac{PV}{nR} = \frac{(1.00)(12.0)}{(0.50)(0.08206)} = 293 \ \text{K}$$

Convert back: $293 - 273 = 20\,\text{°C}$.

**Answer: 293 K, or 20 °C.**

</details>

---

### Problem 9
What volume does $0.750 \ \text{mol}$ of gas occupy at STP?

<details>
<summary><strong>Solution</strong></summary>

At STP, molar volume is $22.4$ L/mol:

$$0.750 \ \text{mol} \times 22.4 \ \text{L/mol} = 16.8 \ \text{L}$$

**Answer: 16.8 L.**

</details>

---

### Problem 10
A $0.500 \ \text{L}$ flask contains $1.25 \ \text{g}$ of a gas at $1.00 \ \text{atm}$ and $300 \ \text{K}$. Find the molar mass and identify the gas.

<details>
<summary><strong>Solution</strong></summary>

First find moles: $n = \dfrac{PV}{RT} = \dfrac{(1.00)(0.500)}{(0.08206)(300)} = 0.0203 \ \text{mol}$.

Molar mass: $M = \dfrac{m}{n} = \dfrac{1.25}{0.0203} = 61.6 \ \text{g/mol}$.

That's close to $\ce{NO2}$ (46.0) — no; to $\ce{CS2}$... actually $\approx 62$ matches nothing tidy, but nearest common lab gas near 62 is a stretch; report the number. (Using $M=\frac{dRT}{P}$ with $d = 1.25/0.500 = 2.50$ g/L gives the same $61.6$ g/mol.)

**Answer: $M \approx 61.6$ g/mol.**

</details>

---

### Problem 11
A gas has a density of $0.714 \ \text{g/L}$ at STP. What is its molar mass, and what is the gas?

<details>
<summary><strong>Solution</strong></summary>

At STP, $M = d \times 22.4 = 0.714 \times 22.4 = 16.0 \ \text{g/mol}$.

That's methane, $\ce{CH4}$ (16.04 g/mol).

**Answer: $M = 16.0$ g/mol — the gas is $\ce{CH4}$.**

</details>

---

### Problem 12
A gas has density $1.78 \ \text{g/L}$ at $25\,\text{°C}$ and $1.00 \ \text{atm}$. Identify it.

<details>
<summary><strong>Solution</strong></summary>

$T = 298$ K. Use $M = \dfrac{dRT}{P}$:

$$M = \frac{(1.78)(0.08206)(298)}{1.00} = 43.5 \ \text{g/mol}$$

Close to $\ce{CO2}$ (44.0) or propane $\ce{C3H8}$ (44.1).

**Answer: $M \approx 43.5$ g/mol — likely $\ce{CO2}$.**

</details>

---

### Problem 13
Magnesium reacts with acid: $\ce{Mg(s) + 2HCl(aq) -> MgCl2(aq) + H2(g)}$. If $0.200 \ \text{mol}$ of $\ce{Mg}$ reacts completely, what volume of $\ce{H2}$ forms at $30\,\text{°C}$ and $0.950 \ \text{atm}$?

<details>
<summary><strong>Solution</strong></summary>

Mole ratio: 1 mol $\ce{Mg}$ → 1 mol $\ce{H2}$, so $0.200$ mol $\ce{H2}$.

Convert $T = 303$ K, then:

$$V = \frac{nRT}{P} = \frac{(0.200)(0.08206)(303)}{0.950} = 5.23 \ \text{L}$$

**Answer: 5.23 L of $\ce{H2}$.**

</details>

---

### Problem 14
A tank contains $\ce{He}$ at $1.2 \ \text{atm}$, $\ce{Ne}$ at $0.8 \ \text{atm}$, and $\ce{Ar}$ at $0.5 \ \text{atm}$. Find the total pressure and the mole fraction of $\ce{Ne}$.

<details>
<summary><strong>Solution</strong></summary>

$$P_\text{total} = 1.2 + 0.8 + 0.5 = 2.5 \ \text{atm}$$

$$X_{\ce{Ne}} = \frac{0.8}{2.5} = 0.32$$

**Answer: $P_\text{total} = 2.5$ atm; $X_{\ce{Ne}} = 0.32$.**

</details>

---

### Problem 15
Oxygen is collected over water at $22\,\text{°C}$. The total pressure is $748 \ \text{mmHg}$; the vapor pressure of water at $22\,\text{°C}$ is $19.8 \ \text{mmHg}$. The collected volume is $0.300 \ \text{L}$. How many moles of dry $\ce{O2}$ were collected?

<details>
<summary><strong>Solution</strong></summary>

Subtract water vapor:

$$P_{\ce{O2}} = 748 - 19.8 = 728 \ \text{mmHg} \times \frac{1 \ \text{atm}}{760 \ \text{mmHg}} = 0.958 \ \text{atm}$$

Convert $T = 295$ K, then:

$$n = \frac{PV}{RT} = \frac{(0.958)(0.300)}{(0.08206)(295)} = 0.0119 \ \text{mol}$$

**Answer: $0.0119 \ \text{mol}$ of $\ce{O2}$.**

</details>

---

## Quick Reference

| Concept | Formula / Value | Notes |
|---|---|---|
| Ideal gas law | $\ce{PV = nRT}$ | The master wiring diagram |
| Gas constant | $R = 0.08206 \ \dfrac{\text{L·atm}}{\text{mol·K}}$ | Also $8.314 \ \frac{\text{J}}{\text{mol·K}}$ for kPa |
| Temperature | $T(\text{K}) = T(\text{°C}) + 273.15$ | **Always Kelvin** — the #1 rule |
| Pressure chain | $1 \ \text{atm} = 760 \ \text{mmHg} = 760 \ \text{torr} = 101.3 \ \text{kPa}$ | mmHg = torr |
| Boyle's law | $P_1V_1 = P_2V_2$ | Constant $n$, $T$; $P$–$V$ inverse |
| Charles's law | $\dfrac{V_1}{T_1} = \dfrac{V_2}{T_2}$ | Constant $n$, $P$; $V$–$T$ direct |
| Gay-Lussac's law | $\dfrac{P_1}{T_1} = \dfrac{P_2}{T_2}$ | Constant $n$, $V$; $P$–$T$ direct |
| Avogadro's law | $\dfrac{V_1}{n_1} = \dfrac{V_2}{n_2}$ | Constant $P$, $T$; $V$–$n$ direct |
| Combined gas law | $\dfrac{P_1V_1}{T_1} = \dfrac{P_2V_2}{T_2}$ | Before/after, constant $n$ |
| STP | $0\,\text{°C}$, $1$ atm | AP definition |
| Molar volume | $22.4$ L/mol | Only at STP! |
| Molar mass from density | $M = \dfrac{dRT}{P}$ | Identify an unknown gas |
| Dalton's law | $P_\text{total} = P_1 + P_2 + \cdots$ | Partial pressures add |
| Mole fraction | $X_i = \dfrac{P_i}{P_\text{total}} = \dfrac{n_i}{n_\text{total}}$ | And $P_i = X_i P_\text{total}$ |
| Gas over water | $P_\text{gas} = P_\text{total} - P_{\ce{H2O}}$ | Subtract water vapor pressure |

---

<div align="center">

[← Phase Changes](/chemistry/0503-phase-changes) | [Kinetic Molecular Theory →](/chemistry/0505-kinetic-molecular-theory)

</div>
