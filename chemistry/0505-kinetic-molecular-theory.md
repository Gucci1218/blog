# Kinetic Molecular Theory and Real Gases
<p class="article-date">July 5, 2026</p>

*My little cousin's birthday was at one of those giant trampoline parks last weekend, and I spent an hour on the sidelines basically watching a gas law come to life. Picture it: dozens of kids bouncing all over a huge padded arena, each one flying in a straight line until — boing — they hit a wall or another kid, rebound, and shoot off in some brand-new random direction, never slowing down. The kids themselves are tiny specks compared to the enormous room, they barely notice each other between bounces, and when the DJ cranked the music the whole crowd bounced faster and slammed the walls harder. That, it turns out, is **exactly** the mental movie chemists use to explain why gases push on their containers, why helium leaks out of balloons first, and why $\ce{PV = nRT}$ works at all. The model is called **Kinetic Molecular Theory (KMT)**, and it's the "why" underneath every gas law you've met. But watch what happens when the park gets packed shoulder-to-shoulder or the kids get tired and clingy — the tidy picture breaks, and that break is the whole story of **real gases** (Topic 3.6).*

---

## What You'll Learn

- State the **five postulates of Kinetic Molecular Theory** and tie each one to the trampoline-park picture
- Explain how KMT accounts for gas **pressure** and for the behavior in the ideal gas law
- Connect **temperature to average kinetic energy** via $KE_{avg} = \tfrac{3}{2}kT$, and use it to argue that all gases at the same $T$ share the same average KE
- Explain why, at the same temperature, **lighter molecules move faster** than heavier ones
- **Read and sketch the Maxwell–Boltzmann speed distribution** — how it shifts and flattens with temperature and how it compares two gases at the same $T$
- Use the **root-mean-square speed** relationship $v_{rms} = \sqrt{\tfrac{3RT}{M}}$ to rank gas speeds
- Apply **Graham's law of effusion**, $\frac{r_1}{r_2} = \sqrt{\frac{M_2}{M_1}}$, to real situations
- Identify **when and why real gases deviate from ideal behavior** — high pressure, low temperature — and which gases deviate most
- Describe qualitatively how the **van der Waals** equation patches up the ideal gas law

---

## Prerequisites

- [Ideal Gas Law](/chemistry/0504-ideal-gas-law) — KMT is the *molecular story behind* $\ce{PV = nRT}$; this article explains **why** that equation works and **when** it stops working, so you need to already know what P, V, n, and T mean and how they trade off
- [Phase Changes](/chemistry/0503-phase-changes) — the low-temperature breakdown of ideal behavior is really intermolecular forces starting to win; if you remember why gases condense into liquids when cooled, real-gas deviations will feel obvious

---

## The Core Concept

### Intuition First

Let's stay in the trampoline park, because every single piece of gas theory is standing right there on the padded floor.

**The kids are the gas molecules.** A gas isn't a smooth fluid — it's a swarm of individual particles, and almost all of the "gas" is empty space. The kids never stop moving, they travel in straight lines until something hits them, and they fly in every possible direction with no plan. That is a gas in a container: particles in **constant, random, straight-line motion**.

**Pressure is the drumming of the walls.** Why does a gas push outward on its container? Because molecules are constantly slamming into the walls and bouncing off. Each hit is a tiny push. Add up billions of tiny pushes per second over every square centimeter and you get a steady, measurable force per area — **pressure**. Fewer kids, or a bigger arena, means fewer hits per patch of wall per second, which is lower pressure. That's already the intuition behind two gas laws: cram the same kids into a smaller room (lower $V$) and the wall gets hit more often (higher $P$) — Boyle's law falls right out.

**Temperature is the music.** When the DJ turns up the energy, the kids bounce *faster*. Hotter gas = faster molecules = harder, more frequent wall hits = more pressure (if you don't let the room expand). Temperature, in KMT, is nothing but a measure of how fast the particles are moving on average — more precisely, their average kinetic energy.

**The collisions are perfectly bouncy.** In our idealized park, when a kid hits a wall or another kid, no energy is lost — they rebound just as fast as they arrived. In physics language the collisions are **elastic**. That's why an ideal gas never "runs down" and settles to the floor; the total kinetic energy is conserved forever.

**The kids ignore each other between bounces.** Except at the instant of a collision, our idealized kids feel no pull toward or push away from one another — no hand-holding, no shoving. In gas terms: **no intermolecular forces** between particles.

Hold onto those five ideas. They're literally the five postulates, and the last two — bouncy collisions and no attractions — are exactly the two that break when the park gets packed or cold.

### The Five Postulates of KMT

Here is the formal list, each one mapped to the park and to a gas-law consequence.

| # | Postulate (formal) | Trampoline picture | Why it matters |
|---|---|---|---|
| 1 | Gas particles are in **constant, random, straight-line motion** | Kids bounce nonstop in every direction | Explains why gases fill any container and mix |
| 2 | The **volume of the particles is negligible** compared to the container | Kids are tiny specks vs. the huge arena; the gas is mostly empty space | Lets us treat molecules as points → the $V$ in $\ce{PV=nRT}$ is *free space* |
| 3 | Collisions are **perfectly elastic** (no kinetic energy lost) | Every rebound is as fast as the approach | Total KE is conserved; the gas never "settles" |
| 4 | There are **no intermolecular forces** between particles (no attractions or repulsions except during collision) | Kids ignore each other between bounces | Particles move independently; pressure comes only from wall hits |
| 5 | The **average kinetic energy is proportional to absolute temperature** ($T$ in kelvin) | Louder music → faster bouncing | Defines temperature molecularly; links $T$ to speed |

> **The single most important consequence:** postulate 5 says $KE_{avg}$ depends **only on temperature (in kelvin)** — not on what the gas is. So at a given $T$, a helium atom and a $\ce{CO2}$ molecule have the **same average kinetic energy**. Keep reading; this one fact powers half the exam questions.

### Temperature = Average Kinetic Energy

The precise statement of postulate 5 for the average translational kinetic energy of a single particle is:

$$KE_{avg} = \frac{3}{2} k T$$

where $k$ is the Boltzmann constant and $T$ is the **absolute temperature in kelvin**. You will not plug numbers into this on the AP exam — but you must understand what it says:

- $KE_{avg}$ depends **only on $T$**. Not on mass, not on the identity of the gas. Same $T$ → same average KE, period.
- Kinetic energy is $KE = \tfrac{1}{2} m v^2$. So if two gases have the **same** average KE but **different** masses, the lighter one must be moving **faster** to make up for its smaller $m$.

That second bullet is the punchline. At the same temperature:

$$\tfrac{1}{2} m_{\text{heavy}} v_{\text{heavy}}^2 = \tfrac{1}{2} m_{\text{light}} v_{\text{light}}^2 \quad\Rightarrow\quad \text{small } m \text{ needs big } v$$

In the park: imagine a room where a toddler and a big teenager somehow carry the *same* kinetic energy. The tiny toddler has to be *zipping* around while the heavy teen lumbers slowly. Light = fast, heavy = slow, **at the same temperature**.

### The Maxwell–Boltzmann Distribution

Here's the honest part: not every molecule moves at the same speed. At any instant some kids are barely hopping and a few are absolutely flying. If you counted how many molecules move at each speed and plotted it, you get the famous **Maxwell–Boltzmann distribution**.

**How to read the graph:**

- **x-axis** = molecular speed (slow on the left, fast on the right)
- **y-axis** = fraction (or relative number) of molecules moving at that speed
- The curve **starts at zero** (no molecules are perfectly still), rises to a **peak**, then trails off in a long tail to the right (a few very fast molecules)
- The curve is **not symmetric** — the right tail is longer than the left drop-off
- **Total area under the curve is fixed** (it represents all the molecules — 100%)

Three speeds live on this curve, and AP loves the ordering:

$$v_{\text{most probable}} \;<\; v_{\text{average}} \;<\; v_{rms}$$

The **most-probable speed** is the peak (the single most common speed). The **average speed** sits a bit to its right, and the **root-mean-square speed** a bit further right still, because the long high-speed tail drags these means rightward.

**What temperature does to the curve.** Turn up the music (raise $T$) and two things happen at once:

1. The peak **shifts right** — molecules are faster on average.
2. The curve **flattens and spreads out** (the peak gets shorter and wider) — there's a broader range of speeds and many more fast molecules in the tail.

Because the total area is fixed, a taller-narrower curve (cold) and a shorter-wider curve (hot) enclose the same area. **Lower $T$ = tall, narrow, shifted left. Higher $T$ = short, broad, shifted right.**

**Comparing two gases at the same temperature.** Same $T$ means same average KE — but the **lighter** gas moves faster, so its curve is **shifted right** (higher speeds) and is **broader/shorter**, while the **heavier** gas is **shifted left** (lower speeds) and is **taller/narrower**. Helium's curve sits far to the right of $\ce{CO2}$'s at the same temperature.

> **This graph is a guaranteed AP item.** You will be asked to sketch it, to redraw it at a second temperature, or to compare two gases. Practice drawing two curves that (a) keep the same total area and (b) move the peak the right direction.

### Root-Mean-Square Speed

We can make "lighter = faster" quantitative. The root-mean-square speed is:

$$v_{rms} = \sqrt{\frac{3RT}{M}}$$

where $R$ is the gas constant, $T$ is temperature in **kelvin**, and $M$ is the **molar mass in kg/mol**. You rarely compute a raw number on the AP exam — you use the *shape* of this relationship:

- $v_{rms} \propto \sqrt{T}$ → **hotter = faster** (quadruple the kelvin temperature → double the speed)
- $v_{rms} \propto \dfrac{1}{\sqrt{M}}$ → **heavier = slower** (four times the molar mass → half the speed)

So ranking gas speeds at the same temperature is just ranking molar masses **backward**: lightest gas is fastest.

### Effusion, Diffusion, and Graham's Law

**Diffusion** is a gas spreading out through a space (or through another gas) — the smell of cookies drifting from the kitchen to your room. **Effusion** is a gas escaping through a tiny pinhole — helium sneaking out through the micro-pores of a balloon. Both are faster for faster molecules, so both are faster for **lighter** gases.

**Graham's law** makes it exact. Because rate goes with speed, and speed goes with $1/\sqrt{M}$:

$$\frac{r_1}{r_2} = \sqrt{\frac{M_2}{M_1}}$$

The gas with the **smaller** molar mass has the **larger** rate. Note the flip: molar masses appear on the opposite side from the rate they belong to.

- **Why helium balloons deflate faster than air-filled ones:** helium ($\ce{He}$, 4 g/mol) effuses much faster than the $\ce{N2}$/$\ce{O2}$ in a normal balloon (~29 g/mol), so it leaks out sooner.
- **Why you smell cookies from across the house:** the light, volatile aroma molecules diffuse through the air and reach you before you ever walk into the kitchen.

### Real Gases: When the Model Breaks (Topic 3.6)

Everything above assumed our idealized park: point-sized kids, perfectly bouncy, ignoring each other. **Real** molecules aren't quite like that, and under two conditions the differences start to matter.

**Condition 1 — High pressure (postulate 2 breaks: volume is no longer negligible).** Cram the kids in until it's shoulder-to-shoulder. Now the space the *bodies* take up is a real fraction of the room — the "empty space" assumption fails. The actual free volume is *less* than the container volume, because the molecules themselves occupy room. Real gases at high pressure have a **larger volume than ideal predicts** (the particles' own size adds on).

**Condition 2 — Low temperature (postulate 4 breaks: intermolecular forces now matter).** Cool the gas down and the kids get tired and *clingy*. Slow-moving molecules linger near each other long enough for their **intermolecular forces (IMFs)** to tug — the same attractions from [Phase Changes](/chemistry/0503-phase-changes) that eventually condense a gas into a liquid. Those inward tugs mean molecules hit the walls a little *softer* and a little *less often*, so the real **pressure is lower than ideal predicts**. Push far enough and the gas condenses entirely — the ultimate non-ideal move.

**Which gases deviate most?** The ones that are (a) **big** (more particle volume) and (b) have **strong IMFs** (large, polar, or hydrogen-bonding). So:

| Nearly ideal (deviate least) | Strongly non-ideal (deviate most) |
|---|---|
| $\ce{He}$, $\ce{H2}$, $\ce{Ne}$ — tiny, weak London forces | $\ce{CO2}$, $\ce{H2O}$, $\ce{NH3}$, $\ce{Cl2}$ — large and/or polar, strong IMFs |

Small nonpolar $\ce{He}$ and $\ce{H2}$ behave almost ideally under a huge range of conditions; polar $\ce{H2O}$ (hydrogen bonding) and big $\ce{CO2}$ deviate badly.

**The van der Waals patch (know this conceptually only).** The **van der Waals equation** repairs $\ce{PV=nRT}$ with two correction terms:

$$\left(P + \frac{an^2}{V^2}\right)(V - nb) = nRT$$

You do **not** need to calculate with this on the AP exam. Just know the story: the $+\dfrac{an^2}{V^2}$ term **corrects the pressure upward** to account for the IMFs that were pulling molecules inward (the $a$ constant is bigger for stronger IMFs), and the $-nb$ term **corrects the volume downward** to subtract the space the molecules themselves occupy (the $b$ constant is bigger for larger molecules). Two postulates broke; two terms fix them.

---

## Worked Examples

### Example 1: Matching Each Postulate to Ideal Behavior

**Problem:** Which KMT postulate most directly explains why we can use the *container's* volume as $V$ in $\ce{PV=nRT}$ instead of subtracting the space the molecules occupy?

**Solution:**

- Step 1: The container volume equals the free space *only if* the molecules take up essentially no room themselves.
- Step 2: That is postulate 2 — the volume of the particles is negligible compared to the container.

**Answer:** Postulate 2 (negligible particle volume). It's also the postulate that fails at high pressure.

### Example 2: Same Temperature, Same KE

**Problem:** A container holds a mixture of $\ce{He}$ and $\ce{Xe}$ at $300\ \text{K}$. Compare (a) their average kinetic energies and (b) their average speeds.

**Solution:**

- Step 1: Average KE depends only on temperature ($KE_{avg} = \tfrac{3}{2}kT$). Same $T$ → **same average KE**.
- Step 2: Same KE but $\ce{Xe}$ (131 g/mol) is far heavier than $\ce{He}$ (4 g/mol). Since $KE = \tfrac{1}{2}mv^2$, the lighter atom must move faster.

**Answer:** (a) Equal average kinetic energies. (b) $\ce{He}$ moves much faster than $\ce{Xe}$.

### Example 3: Ranking Speeds at the Same Temperature

**Problem:** Rank $\ce{He}$, $\ce{N2}$, and $\ce{CO2}$ from fastest to slowest average molecular speed at the same temperature.

**Solution:**

- Step 1: Same $T$ → speed ranking is molar-mass ranking, backward ($v_{rms} \propto 1/\sqrt{M}$).
- Step 2: Molar masses: $\ce{He} = 4$, $\ce{N2} = 28$, $\ce{CO2} = 44$ g/mol.
- Step 3: Smallest mass = fastest.

**Answer:** $\ce{He} > \ce{N2} > \ce{CO2}$ (fastest to slowest).

### Example 4: Reading a Maxwell–Boltzmann Curve

**Problem:** On a single set of axes you're shown two Maxwell–Boltzmann curves for the *same* gas. Curve A has a tall, narrow peak far to the left; curve B is short, broad, and shifted right. Which curve is at the higher temperature, and why?

**Solution:**

- Step 1: Higher temperature means faster molecules (peak shifts right) and a wider spread of speeds (curve flattens).
- Step 2: Curve B is shifted right and flattened; curve A is left and sharp.

**Answer:** Curve B is the higher temperature. Its peak is at a higher speed and the distribution is broader, with a fatter high-speed tail — while both curves enclose the same total area.

### Example 5: Two Gases on One Curve

**Problem:** $\ce{O2}$ and $\ce{H2}$ are at the same temperature. Sketch-describe how their Maxwell–Boltzmann curves compare.

**Solution:**

- Step 1: Same $T$ → same average KE, but $\ce{H2}$ (2 g/mol) is far lighter than $\ce{O2}$ (32 g/mol).
- Step 2: Lighter → faster → curve shifted right and broader/shorter. Heavier → slower → curve shifted left and taller/narrower.

**Answer:** $\ce{H2}$'s curve peaks at a much higher speed and is broad and low; $\ce{O2}$'s curve peaks at a lower speed and is tall and narrow. Both enclose the same area.

### Example 6: Effect of Temperature on Speed

**Problem:** A sample of $\ce{N2}$ is heated from $300\ \text{K}$ to $1200\ \text{K}$. By what factor does its root-mean-square speed change?

**Solution:**

- Step 1: $v_{rms} \propto \sqrt{T}$ (same gas, so $M$ is constant).
- Step 2: Temperature ratio $= 1200/300 = 4$.
- Step 3: Speed factor $= \sqrt{4} = 2$.

**Answer:** The $v_{rms}$ **doubles**.

### Example 7: Graham's Law — Which Is Faster and By How Much

**Problem:** Compare the effusion rates of $\ce{H2}$ (2 g/mol) and $\ce{O2}$ (32 g/mol) at the same temperature.

**Solution:**

- Step 1: Graham's law: $\dfrac{r_{\ce{H2}}}{r_{\ce{O2}}} = \sqrt{\dfrac{M_{\ce{O2}}}{M_{\ce{H2}}}}$.
- Step 2: $= \sqrt{\dfrac{32}{2}} = \sqrt{16} = 4$.

**Answer:** $\ce{H2}$ effuses **4 times faster** than $\ce{O2}$.

### Example 8: Graham's Law — Finding an Unknown Molar Mass

**Problem:** An unknown gas effuses at half the rate of $\ce{He}$ (4.0 g/mol) at the same temperature. What is its molar mass?

**Solution:**

- Step 1: $\dfrac{r_{\text{unknown}}}{r_{\ce{He}}} = \dfrac{1}{2}$.
- Step 2: Graham's law: $\dfrac{r_{\text{unknown}}}{r_{\ce{He}}} = \sqrt{\dfrac{M_{\ce{He}}}{M_{\text{unknown}}}}$.
- Step 3: $\dfrac{1}{2} = \sqrt{\dfrac{4.0}{M}} \Rightarrow \dfrac{1}{4} = \dfrac{4.0}{M} \Rightarrow M = 16$ g/mol.

**Answer:** The unknown gas has molar mass $16$ g/mol (e.g., $\ce{CH4}$).

### Example 9: Why the Helium Balloon Wins the Sad Race

**Problem:** You blow up one balloon with helium and an identical one with air (mostly $\ce{N2}$, ~28 g/mol). The next morning one is noticeably more shrunken. Which one, and which KMT idea explains it?

**Solution:**

- Step 1: Balloon deflation is effusion through tiny pores. Rate $\propto 1/\sqrt{M}$.
- Step 2: $\ce{He}$ (4 g/mol) is much lighter than air (~28 g/mol), so it effuses faster: $\sqrt{28/4} \approx 2.6$ times faster.

**Answer:** The **helium** balloon shrivels first — lighter molecules move faster and escape through the balloon's pores more quickly (Graham's law).

### Example 10: Least Ideal Gas and Why

**Problem:** Among $\ce{He}$, $\ce{N2}$, and $\ce{H2O}$ (vapor), which behaves **least** ideally, and why?

**Solution:**

- Step 1: Deviations grow with molecular size and strength of intermolecular forces.
- Step 2: $\ce{He}$ is tiny with only weak London forces (very ideal). $\ce{N2}$ is small and nonpolar (fairly ideal). $\ce{H2O}$ is polar and **hydrogen-bonds** — strong IMFs.

**Answer:** $\ce{H2O}$ deviates most, because its strong hydrogen-bonding IMFs cause significant attractions between molecules (especially at lower temperatures), violating the "no intermolecular forces" postulate.

### Example 11: The Conditions for Ideal Behavior

**Problem:** Under what conditions does a real gas behave **most** ideally? Justify each with a postulate.

**Solution:**

- Step 1: **High temperature.** Fast molecules zip past each other before IMFs can act → the "no attractions" postulate holds well.
- Step 2: **Low pressure (large volume).** Molecules are far apart, so their own size is truly negligible compared to the space → the "negligible particle volume" postulate holds.

**Answer:** **High temperature and low pressure.** High $T$ overwhelms IMFs; low $P$ keeps particle volume negligible.

### Example 12: Direction of Deviation

**Problem:** At high pressure, real gases often occupy a *larger* volume than the ideal gas law predicts. Which postulate explains this, and why that direction?

**Solution:**

- Step 1: At high pressure, molecules are packed close and their own physical volume is no longer negligible (postulate 2 fails).
- Step 2: The molecules take up space, so the gas can't be squeezed down to the tiny volume $\ce{PV=nRT}$ predicts — the real volume is larger.

**Answer:** Postulate 2 (negligible particle volume). Because the molecules occupy real space, the actual volume exceeds the ideal prediction at high pressure.

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Thinking hotter gas means *more* kinetic energy for a heavier molecule than a lighter one at the same $T$ | Confusing speed with energy | At the same $T$, **all** gases have the **same** average KE; only the *speeds* differ (light = fast) |
| Using temperature in °C in speed or KE reasoning | Forgetting that KMT relations use absolute temperature | Always convert to **kelvin** before comparing energies or speeds |
| Drawing the Maxwell–Boltzmann curve as a symmetric bell | It looks bell-ish near the peak | It has a **long right tail** and starts at the origin — it is skewed, not symmetric |
| Making the higher-$T$ curve *taller* | Assuming "more energy = bigger everything" | Higher $T$ curves are **shorter and broader** — total area is conserved |
| Flipping Graham's law upside down | The molar masses appear on the opposite side from their rate | Remember: **lighter gas = faster**, so the heavier mass goes *on top* under the root for the faster gas's ratio |
| Saying real gases deviate because "the ideal gas law is wrong" | Not connecting to postulates | Name the **specific postulate** that breaks: particle volume (high $P$) or IMFs (low $T$) |
| Claiming $\ce{He}$ deviates a lot because it's a noble gas | Confusing "inert" with "non-ideal" | $\ce{He}$ is one of the **most ideal** gases — tiny and weak IMFs |

---

## AP Exam Tips

- **The Maxwell–Boltzmann sketch is nearly guaranteed.** Practice two moves: (1) redraw the curve at a higher/lower temperature (shift the peak the right way, flatten or sharpen it, **keep the area the same**); (2) draw two gases at the same $T$ (lighter = shifted right and broader). Label axes: *speed* on x, *fraction/number of molecules* on y.
- **"Same temperature" is a trigger phrase.** It should immediately make you write: *same average kinetic energy*. Then reason from there — lighter molecules must be moving faster.
- **Kelvin, always.** Any speed, KE, or Maxwell–Boltzmann comparison uses absolute temperature. A question that switches to Celsius is testing whether you'll convert.
- **Real-gas deviations want a molecular justification, not a formula.** Full-credit FRQ language names the **condition** (high pressure or low temperature) **and** the **postulate** it violates (negligible volume or no IMFs). "At low temperature, molecules move slowly enough that intermolecular attractions become significant, so the gas deviates from ideal" earns the point.
- **Connect low-temperature deviation back to IMFs** — this is the Unit 3 through-line. The gases that deviate most (polar, hydrogen-bonding, large) are exactly the ones with the strongest IMFs from [Phase Changes](/chemistry/0503-phase-changes). Examiners reward that link.
- **Graham's law is a plug-and-chug gift.** Memorize $\frac{r_1}{r_2} = \sqrt{\frac{M_2}{M_1}}$ and be careful which gas is 1 and which is 2. The faster gas is always the lighter one — sanity-check your answer against that.
- **You will not need the van der Waals equation numerically** — but you may be asked what its two correction terms *mean* (pressure up for IMFs, volume down for particle size).

---

## Practice Problems

### Problem 1
State all five postulates of Kinetic Molecular Theory in your own words.

<details>
<summary><strong>Solution</strong></summary>

(1) Gas particles are in constant, random, straight-line motion. (2) The volume of the particles is negligible compared to the container. (3) Collisions are perfectly elastic — no kinetic energy is lost. (4) There are no intermolecular forces between particles except during collisions. (5) The average kinetic energy of the particles is proportional to the absolute (kelvin) temperature.

**All five, in any equivalent wording.**

</details>

---

### Problem 2
At $500\ \text{K}$, which has the greater average kinetic energy: $\ce{O2}$ or $\ce{SO2}$? Which moves faster on average?

<details>
<summary><strong>Solution</strong></summary>

Average KE depends only on temperature, and both are at $500\ \text{K}$, so they have **equal average kinetic energies**. Since $\ce{O2}$ (32 g/mol) is lighter than $\ce{SO2}$ (64 g/mol), **$\ce{O2}$ moves faster**.

**Equal KE; $\ce{O2}$ is faster.**

</details>

---

### Problem 3
Rank these gases by average molecular speed at the same temperature, fastest to slowest: $\ce{CH4}$, $\ce{Ne}$, $\ce{Ar}$, $\ce{Cl2}$.

<details>
<summary><strong>Solution</strong></summary>

Speed goes as $1/\sqrt{M}$, so rank by molar mass, backward. Molar masses: $\ce{CH4} = 16$, $\ce{Ne} = 20$, $\ce{Ar} = 40$, $\ce{Cl2} = 71$ g/mol.

**Fastest → slowest: $\ce{CH4} > \ce{Ne} > \ce{Ar} > \ce{Cl2}$.**

</details>

---

### Problem 4
A gas is heated from $250\ \text{K}$ to $1000\ \text{K}$. By what factor does its $v_{rms}$ change?

<details>
<summary><strong>Solution</strong></summary>

$v_{rms} \propto \sqrt{T}$. Temperature ratio $= 1000/250 = 4$, so speed factor $= \sqrt{4} = 2$.

**The $v_{rms}$ doubles.**

</details>

---

### Problem 5
Sketch, in words, how the Maxwell–Boltzmann distribution for a fixed gas sample changes when you *lower* the temperature.

<details>
<summary><strong>Solution</strong></summary>

Lowering the temperature shifts the peak **left** (molecules are slower), makes the curve **taller and narrower** (speeds cluster in a smaller range), and shrinks the high-speed tail. The total area under the curve stays the same because the number of molecules is unchanged.

**Peak shifts left, curve gets taller and narrower, same total area.**

</details>

---

### Problem 6
On one graph, curve X peaks at a low speed and is tall/narrow; curve Y peaks at a high speed and is short/broad — both for the same gas. Which is hotter?

<details>
<summary><strong>Solution</strong></summary>

Higher temperature → faster molecules (peak right) and broader spread (flatter). Curve Y matches both.

**Curve Y is the higher temperature.**

</details>

---

### Problem 7
$\ce{NH3}$ and $\ce{HCl}$ are released from opposite ends of a tube at the same time. Which gas travels farther before they meet, and why?

<details>
<summary><strong>Solution</strong></summary>

Diffusion rate $\propto 1/\sqrt{M}$. $\ce{NH3} = 17$ g/mol, $\ce{HCl} = 36.5$ g/mol. $\ce{NH3}$ is lighter, so it diffuses faster and travels **farther** before the two meet. Their rate ratio is $\sqrt{36.5/17} \approx 1.46$, so $\ce{NH3}$ covers about 1.46 times the distance.

**$\ce{NH3}$ travels farther — it's lighter and diffuses faster.**

</details>

---

### Problem 8
An unknown gas effuses $1.5$ times faster than $\ce{CO2}$ (44 g/mol) at the same temperature. Find its molar mass.

<details>
<summary><strong>Solution</strong></summary>

$\dfrac{r_{\text{unknown}}}{r_{\ce{CO2}}} = 1.5 = \sqrt{\dfrac{44}{M}}$. Square: $2.25 = \dfrac{44}{M}$, so $M = \dfrac{44}{2.25} \approx 19.6$ g/mol.

**About $20$ g/mol** (e.g., $\ce{HF}$).

</details>

---

### Problem 9
Explain, using KMT, why increasing the temperature of a gas at constant volume increases its pressure.

<details>
<summary><strong>Solution</strong></summary>

Higher temperature means greater average kinetic energy, so molecules move faster. Faster molecules hit the container walls **more often** and with **greater force** per hit. More frequent, harder collisions per unit area = higher pressure.

**Faster molecules → more frequent, harder wall collisions → higher pressure.**

</details>

---

### Problem 10
Which gas behaves most ideally: $\ce{H2}$, $\ce{CO2}$, or $\ce{H2O}$ vapor? Justify.

<details>
<summary><strong>Solution</strong></summary>

Ideality is best for small molecules with weak IMFs. $\ce{H2}$ is tiny with only weak London forces. $\ce{CO2}$ is larger; $\ce{H2O}$ is polar and hydrogen-bonds (strong IMFs).

**$\ce{H2}$ behaves most ideally — smallest particle volume and weakest intermolecular forces.**

</details>

---

### Problem 11
Under what two conditions do real gases deviate *most* from ideal behavior, and which postulate fails in each case?

<details>
<summary><strong>Solution</strong></summary>

**High pressure:** molecules are packed close, so their own volume is no longer negligible → postulate 2 (negligible particle volume) fails. **Low temperature:** molecules move slowly, so intermolecular attractions become significant → postulate 4 (no intermolecular forces) fails.

**High pressure (particle-volume postulate) and low temperature (no-IMF postulate).**

</details>

---

### Problem 12
At high pressure, does a real gas typically occupy a larger or smaller volume than the ideal gas law predicts? Explain.

<details>
<summary><strong>Solution</strong></summary>

**Larger.** At high pressure the molecules' own finite volume matters; they occupy real space and cannot be compressed into the tiny volume $\ce{PV=nRT}$ predicts, so the observed volume exceeds the ideal value.

**Larger than ideal — because particle volume is no longer negligible.**

</details>

---

### Problem 13
Explain qualitatively what the two correction terms in the van der Waals equation $\left(P + \frac{an^2}{V^2}\right)(V - nb) = nRT$ account for.

<details>
<summary><strong>Solution</strong></summary>

The $+\dfrac{an^2}{V^2}$ term corrects **pressure upward** to compensate for intermolecular attractions (IMFs) that pull molecules inward and reduce the measured pressure; the constant $a$ is larger for gases with stronger IMFs. The $-nb$ term corrects **volume downward** to subtract the space the molecules themselves occupy; the constant $b$ is larger for bigger molecules.

**$a$-term = pressure correction for IMFs; $b$-term = volume correction for particle size.**

</details>

---

### Problem 14
Two identical balloons are filled to the same size, one with $\ce{He}$ and one with $\ce{CO2}$. After a day, which is smaller, and by roughly what speed ratio do their gases effuse?

<details>
<summary><strong>Solution</strong></summary>

Effusion rate $\propto 1/\sqrt{M}$. $\ce{He} = 4$ g/mol, $\ce{CO2} = 44$ g/mol. Ratio $= \sqrt{44/4} = \sqrt{11} \approx 3.3$. Helium effuses about 3.3 times faster, so the **helium balloon** shrinks noticeably while the $\ce{CO2}$ one barely changes.

**The helium balloon is smaller; $\ce{He}$ effuses ~3.3 times faster than $\ce{CO2}$.**

</details>

---

### Problem 15
A friend says, "At the same temperature, heavier gas molecules have more kinetic energy because they have more mass." Correct the statement.

<details>
<summary><strong>Solution</strong></summary>

At the same temperature, **all** gases have the **same average kinetic energy** ($KE_{avg} = \tfrac{3}{2}kT$ depends only on $T$). Because $KE = \tfrac{1}{2}mv^2$, a heavier molecule with the *same* KE must move **more slowly**, not carry more energy.

**Same temperature → same average KE; the heavier gas is slower, not more energetic.**

</details>

---

## Quick Reference

**The five KMT postulates**

| # | Postulate | Trampoline picture |
|---|---|---|
| 1 | Constant, random, straight-line motion | Kids bounce nonstop, every direction |
| 2 | Negligible particle volume | Kids are specks in a huge arena |
| 3 | Elastic collisions (no KE lost) | Every rebound is as fast as the approach |
| 4 | No intermolecular forces | Kids ignore each other between bounces |
| 5 | Average KE ∝ absolute temperature | Louder music → faster bouncing |

**Key relationships**

| Idea | Relationship | Takeaway |
|---|---|---|
| Temperature & energy | $KE_{avg} = \tfrac{3}{2}kT$ | Same $T$ → same average KE for all gases |
| Speed | $v_{rms} = \sqrt{\tfrac{3RT}{M}}$ | Hotter = faster; heavier = slower |
| Effusion/diffusion | $\dfrac{r_1}{r_2} = \sqrt{\dfrac{M_2}{M_1}}$ | Lighter gas escapes/spreads faster |

**Maxwell–Boltzmann curve**

| Change | Peak | Shape | Area |
|---|---|---|---|
| Higher $T$ | Shifts right | Shorter, broader | Same |
| Lower $T$ | Shifts left | Taller, narrower | Same |
| Lighter gas (same $T$) | Shifts right | Broader | Same |
| Heavier gas (same $T$) | Shifts left | Narrower | Same |

Speed order on the curve: $v_{\text{most probable}} < v_{\text{average}} < v_{rms}$.

**Real-gas deviations (Topic 3.6)**

| Condition | Postulate that fails | Result |
|---|---|---|
| High pressure | Negligible particle volume | Real volume larger than ideal |
| Low temperature | No intermolecular forces | Real pressure lower than ideal; can condense |

Most ideal: small, nonpolar ($\ce{He}$, $\ce{H2}$). Least ideal: large/polar/H-bonding ($\ce{CO2}$, $\ce{H2O}$, $\ce{NH3}$). **Most ideal conditions: high temperature, low pressure.**

---

<div align="center">

[← Ideal Gas Law](/chemistry/0504-ideal-gas-law) | [Solutions and Concentration →](/chemistry/0506-solutions-and-concentration)

</div>
