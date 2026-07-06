# ICE Tables and Equilibrium Calculations
<p class="article-date">July 5, 2026</p>

*Every month my parents drop my allowance into my account, and I keep a little ledger to see where it all goes. The way I write it is always three rows. The top row is what I **started** the month with — say \$50 sitting there on the 1st. The middle row is everything that **changed** — the \$50 in, the \$6.25 boba, the movie ticket, the money I paid my brother back — deposits with a plus and withdrawals with a minus. And the bottom row is what I **end** with, which is just start plus change, line by line. Here's the thing I realized doing AP Chem this week: an equilibrium problem is literally that same ledger. A reaction "starts" with some concentrations (Initial), quantities shift as it runs toward equilibrium (Change), and it settles at final amounts (Equilibrium). Chemists even draw it as three stacked rows and call it an **ICE table** — Initial, Change, Equilibrium. Fill in the ledger, plug the bottom row into the equilibrium constant $K$, and solve. This is the single most-used calculation in all of AP equilibrium and acid–base chemistry, and once the ledger clicks, it never un-clicks.*

---

## What You'll Learn

- Build an **ICE table** for any reaction: rows for **I**nitial, **C**hange, and **E**quilibrium, with one column per species
- Write the **Change row** using a single unknown $x$ scaled by the balanced equation's **stoichiometric coefficients**, with the correct **signs** (reactants and products move in opposite directions)
- Run the full recipe: **set up ICE → write the $K$ expression from the Equilibrium row → solve for $x$ → back-substitute** to get every equilibrium concentration
- Solve the clean **perfect-square** case with no quadratic at all
- Use the **quadratic formula** when the algebra demands it
- Apply the **small-$x$ approximation** (the "5% rule") when $K$ is small, then **validate** it — and switch to the quadratic when the check fails
- Use the **reaction quotient $Q$** to decide the **direction** of the shift, which fixes the **sign of $x$** before you solve
- Set up an ICE table in terms of **partial pressures** for a $K_p$ problem
- Run the reverse problem: **calculate $K$** from the initial concentrations plus **one** measured equilibrium value

---

## Prerequisites

- [The Equilibrium Constant](/chemistry/0902-equilibrium-constant) — you must already know how to write a $K$ expression (products over reactants, each raised to its coefficient) and what $K$ *means*. The entire back half of every ICE problem is plugging the Equilibrium row into that expression, so this is non-negotiable groundwork.
- [Stoichiometry](/chemistry/0603-stoichiometry) — the **Change row lives and dies by mole ratios**. The coefficients that multiply $x$ ($-x$, $+2x$, $-3x$, …) are the exact same stoichiometric ratios you used to convert between reactants and products. If mole ratios feel shaky, the Change row will too.

---

## The Core Concept

### Intuition First

Let me stay with my allowance ledger, because every single part of an ICE table is sitting in it.

**The three rows are the same three rows.** My ledger has a *starting balance*, a *change*, and an *ending balance*. An ICE table has **I**nitial concentrations, the **C**hange, and the **E**quilibrium concentrations. Same idea, same order, top to bottom.

| My allowance ledger | The ICE table |
|---|---|
| **Starting balance** (money on the 1st) | **Initial** row — concentrations before the reaction shifts |
| **Change** (deposits $+$, withdrawals $-$) | **Change** row — how much each species gains or loses |
| **Ending balance** = start + change | **Equilibrium** row — Initial + Change, line by line |
| Every deposit/withdrawal is *linked* (I can't spend \$6.25 without \$6.25 leaving) | Every change is *linked* by the balanced equation's coefficients |
| Checking the ending balance is right | Plugging the Equilibrium row into $K$ and solving |

**The columns are the "accounts."** In my ledger I might track cash, my debit card, and what my brother owes me as separate columns. In an ICE table each **species gets its own column** — one for every reactant and every product. The Initial, Change, and Equilibrium values for that species stack vertically in its column.

**The Change row is where the money is *linked*.** Here's the part that trips people up, and the allowance ledger fixes it instantly. When I buy boba, one thing happens with two linked sides: \$6.25 *leaves* my cash and the boba *arrives*. I don't get to pick those independently — they're the same event. In a reaction, the same is true: as reactants are *consumed*, products are *produced*, all locked together by the balanced equation. So we pick **one unknown, $x$**, for how far the reaction runs, and every other change is $x$ scaled by that species' coefficient:

- **Reactants get consumed → their change is negative** (a withdrawal): $-x$, $-2x$, $-3x$, …
- **Products get produced → their change is positive** (a deposit): $+x$, $+2x$, …
- **The multiplier is the coefficient.** A species with coefficient 3 changes by $3x$, because for every "unit" of reaction, three of that species move — the exact mole ratio from stoichiometry.

For $\ce{N2 + 3H2 <=> 2NH3}$, the Change row is $-x,\ -3x,\ +2x$. The $\ce{H2}$ moves three times as fast as $\ce{N2}$, and $\ce{NH3}$ twice as fast — just like buying three boba drains cash three times as fast as buying one.

**The Equilibrium row is the ending balance: Initial + Change.** Nothing fancy. Add each column straight down: $[\ce{N2}]_0 - x$, and so on. That bottom row is the whole reason we built the table.

**Solving is balancing the checkbook.** My ledger is only useful if the ending balance is *right* — if it matches reality. For a reaction, "reality" is the equilibrium constant $K$: at equilibrium the Equilibrium row, plugged into the $K$ expression, must equal the known value of $K$. That single equation is what we solve for $x$. Setting the ending balance equal to $K$ **is** balancing the checkbook. Once we have $x$, we drop it back into the Equilibrium row and read off every concentration.

That's the whole method. The rest of this article is just running that ledger in every situation the AP exam can throw at it.

### The ICE Table, Formally

For a general reaction $\ce{aA + bB <=> cC + dD}$ shifting **forward** (toward products), the table is:

| | $\ce{A}$ | $\ce{B}$ | $\ce{C}$ | $\ce{D}$ |
|---|---|---|---|---|
| **I**nitial | $[\ce{A}]_0$ | $[\ce{B}]_0$ | $[\ce{C}]_0$ | $[\ce{D}]_0$ |
| **C**hange | $-ax$ | $-bx$ | $+cx$ | $+dx$ |
| **E**quilibrium | $[\ce{A}]_0-ax$ | $[\ce{B}]_0-bx$ | $[\ce{C}]_0+cx$ | $[\ce{D}]_0+dx$ |

Then the equilibrium condition is:

$$K_c = \frac{[\ce{C}]^c\,[\ce{D}]^d}{[\ce{A}]^a\,[\ce{B}]^b} = \frac{([\ce{C}]_0+cx)^c\,([\ce{D}]_0+dx)^d}{([\ce{A}]_0-ax)^a\,([\ce{B}]_0-bx)^b}$$

Solve that for $x$, back-substitute, done. (Pure solids and liquids never appear in $K$, so they get **no column** — you don't track them, just like I don't put "the couch" in my money ledger.)

### The Recipe

1. **Write the balanced equation** and its $K$ expression.
2. **Decide the direction** of the shift. If you start with reactants only, it goes forward. If you start with a mix, compute $Q$ and compare to $K$ (details below) — this sets the **sign of $x$**.
3. **Build the ICE table.** Fill Initial. Fill Change using coefficients $\times\, x$ with signs from the direction. Add to get Equilibrium.
4. **Plug the Equilibrium row into $K$.** Now it's pure algebra in one unknown.
5. **Solve for $x$** — by perfect square, small-$x$ approximation, or the quadratic formula, whichever the numbers allow.
6. **Back-substitute** $x$ into the Equilibrium row to get every concentration. **Sanity-check** by plugging them back into $K$.

### Choosing the Shift Direction with $Q$

The **reaction quotient** $Q$ is computed with the *exact same expression* as $K$, but using the **current (initial) concentrations** instead of equilibrium ones. Comparing $Q$ to $K$ tells you which way the reaction must move to reach equilibrium:

- $Q < K$ → too few products → **shift forward** (products $+x$, reactants $-x$)
- $Q > K$ → too many products → **shift reverse** (products $-x$, reactants $+x$)
- $Q = K$ → already at equilibrium → no change

If you start with **reactants only**, $Q = 0 < K$, so it *always* shifts forward — no calculation needed. If you start with **products only**, $Q = \infty > K$, so it shifts reverse. You only need to actually compute $Q$ when you start with a **mix** of both.

### The Small-$x$ Approximation (the "5% Rule")

When $K$ is very small (say $< 10^{-3}$), the reaction barely runs, so $x$ is tiny compared to the initial concentrations. In a term like $[\ce{A}]_0 - x$, subtracting a tiny $x$ from a big number barely changes it, so we **approximate** $[\ce{A}]_0 - x \approx [\ce{A}]_0$. That kills the quadratic and lets you solve by a quick square root. Then you **must validate**:

$$\text{percent change} = \frac{x}{[\ce{A}]_0}\times 100\% \le 5\% \ \Rightarrow\ \text{approximation OK}$$

If it's over 5%, the approximation was too crude — **throw it out and solve the full quadratic.** (Full worked examples of both outcomes below.)

---

## Worked Examples

### Example 1: Setting Up the Ledger (coefficients on the Change row)

**Problem:** Write the ICE table (in terms of $x$) and the $K_c$ expression for the Haber process, $\ce{N2(g) + 3H2(g) <=> 2NH3(g)}$, starting with $[\ce{N2}]_0 = 1.00\ \text{M}$, $[\ce{H2}]_0 = 3.00\ \text{M}$, and no $\ce{NH3}$.

**Solution:**
- **Step 1 — Direction.** Products start at zero, so the reaction can only go **forward**. Reactants get $-$, product gets $+$.
- **Step 2 — Change row uses coefficients $\times\, x$.** $\ce{N2}$ has coefficient 1 → $-x$; $\ce{H2}$ has coefficient 3 → $-3x$; $\ce{NH3}$ has coefficient 2 → $+2x$. (The $\ce{H2}$ is spent three times as fast as $\ce{N2}$ — pure mole ratio.)

| | $\ce{N2}$ | $\ce{H2}$ | $\ce{NH3}$ |
|---|---|---|---|
| **I** | $1.00$ | $3.00$ | $0$ |
| **C** | $-x$ | $-3x$ | $+2x$ |
| **E** | $1.00-x$ | $3.00-3x$ | $2x$ |

- **Step 3 — $K$ expression from the Equilibrium row:**

$$K_c = \frac{[\ce{NH3}]^2}{[\ce{N2}][\ce{H2}]^3} = \frac{(2x)^2}{(1.00-x)(3.00-3x)^3}$$

**Answer:** The Change row is $-x,\ -3x,\ +2x$; the setup is shown above. This is the skeleton every equilibrium calculation hangs on — get the signs and coefficient multipliers right here and the rest is algebra.

### Example 2: Perfect Square — No Quadratic Needed

**Problem:** For $\ce{H2(g) + I2(g) <=> 2HI(g)}$, $K_c = 49.0$. You start with $1.00\ \text{M}$ each of $\ce{H2}$ and $\ce{I2}$ and no $\ce{HI}$. Find all equilibrium concentrations.

**Solution:**
- **Direction:** products at zero → forward.

| | $\ce{H2}$ | $\ce{I2}$ | $\ce{HI}$ |
|---|---|---|---|
| **I** | $1.00$ | $1.00$ | $0$ |
| **C** | $-x$ | $-x$ | $+2x$ |
| **E** | $1.00-x$ | $1.00-x$ | $2x$ |

- **Plug into $K$:**

$$49.0 = \frac{(2x)^2}{(1.00-x)(1.00-x)} = \frac{(2x)^2}{(1.00-x)^2}$$

- **Notice both sides are perfect squares.** Take the square root of the whole equation:

$$\sqrt{49.0} = \frac{2x}{1.00-x} \quad\Rightarrow\quad 7.00 = \frac{2x}{1.00-x}$$

- **Solve linearly:** $7.00(1.00-x) = 2x \Rightarrow 7.00 - 7.00x = 2x \Rightarrow 9.00x = 7.00 \Rightarrow x = 0.778$.
- **Back-substitute:** $[\ce{H2}] = [\ce{I2}] = 1.00 - 0.778 = 0.222\ \text{M}$; $[\ce{HI}] = 2(0.778) = 1.556\ \text{M}$.
- **Check:** $\dfrac{(1.556)^2}{(0.222)^2} = 49.1 \approx 49.0$ ✓

**Answer:** $[\ce{H2}] = [\ce{I2}] = 0.222\ \text{M}$, $[\ce{HI}] = 1.56\ \text{M}$. Whenever the denominator is a perfect square and $K$ is too, the square-root trick beats the quadratic every time.

### Example 3: When You Need the Quadratic Formula

**Problem:** For the water–gas shift $\ce{CO(g) + H2O(g) <=> CO2(g) + H2(g)}$, $K_c = 5.10$. You start with $[\ce{CO}]_0 = 2.00\ \text{M}$, $[\ce{H2O}]_0 = 1.00\ \text{M}$, no products. Find the equilibrium concentrations.

**Solution:**
- **Direction:** products at zero → forward.

| | $\ce{CO}$ | $\ce{H2O}$ | $\ce{CO2}$ | $\ce{H2}$ |
|---|---|---|---|---|
| **I** | $2.00$ | $1.00$ | $0$ | $0$ |
| **C** | $-x$ | $-x$ | $+x$ | $+x$ |
| **E** | $2.00-x$ | $1.00-x$ | $x$ | $x$ |

- **Plug into $K$:**

$$5.10 = \frac{(x)(x)}{(2.00-x)(1.00-x)} = \frac{x^2}{(2.00-x)(1.00-x)}$$

The initial amounts are unequal, so the denominator is **not** a perfect square — the square-root shortcut is dead. Expand and use the quadratic formula. (Honestly, after AP Calc BC the quadratic formula feels like a warm hug — it's the one Algebra 2 tool that never left.)

- **Expand:** $5.10(2.00 - 3.00x + x^2) = x^2 \Rightarrow 10.2 - 15.3x + 5.10x^2 = x^2$.
- **Standard form:** $4.10x^2 - 15.3x + 10.2 = 0$.
- **Quadratic formula:** $x = \dfrac{15.3 \pm \sqrt{(15.3)^2 - 4(4.10)(10.2)}}{2(4.10)} = \dfrac{15.3 \pm \sqrt{66.81}}{8.20} = \dfrac{15.3 \pm 8.17}{8.20}$.
- **Two roots:** $x = 2.86$ or $x = 0.869$. **Reject $x = 2.86$** — it would make $[\ce{H2O}] = 1.00 - 2.86 < 0$, a negative concentration (impossible). Keep $x = 0.869$.
- **Back-substitute:** $[\ce{CO}] = 1.13\ \text{M}$, $[\ce{H2O}] = 0.131\ \text{M}$, $[\ce{CO2}] = [\ce{H2}] = 0.869\ \text{M}$.
- **Check:** $\dfrac{(0.869)^2}{(1.13)(0.131)} = 5.10$ ✓

**Answer:** $[\ce{CO}] = 1.13\ \text{M}$, $[\ce{H2O}] = 0.131\ \text{M}$, $[\ce{CO2}] = [\ce{H2}] = 0.869\ \text{M}$. **Always discard the root that gives a negative concentration** — only one root is physically real.

### Example 4: The Small-$x$ Approximation — and the 5% Check That Passes

**Problem:** Phosgene decomposes: $\ce{COCl2(g) <=> CO(g) + Cl2(g)}$, $K_c = 2.2\times 10^{-10}$. Starting with $[\ce{COCl2}]_0 = 0.25\ \text{M}$ and no products, find the equilibrium concentrations.

**Solution:**
- **Direction:** products at zero → forward.

| | $\ce{COCl2}$ | $\ce{CO}$ | $\ce{Cl2}$ |
|---|---|---|---|
| **I** | $0.25$ | $0$ | $0$ |
| **C** | $-x$ | $+x$ | $+x$ |
| **E** | $0.25-x$ | $x$ | $x$ |

- **Plug into $K$:**

$$2.2\times 10^{-10} = \frac{x^2}{0.25 - x}$$

- **Approximate.** $K$ is *tiny*, so the reaction barely proceeds — $x$ will be minuscule next to $0.25$. Assume $0.25 - x \approx 0.25$:

$$2.2\times 10^{-10} \approx \frac{x^2}{0.25} \Rightarrow x^2 = (2.2\times 10^{-10})(0.25) = 5.5\times 10^{-11} \Rightarrow x = 7.4\times 10^{-6}$$

- **Validate with the 5% rule:** $\dfrac{x}{0.25}\times 100\% = \dfrac{7.4\times 10^{-6}}{0.25}\times 100\% = 0.0030\% \le 5\%$ ✓ The approximation is excellent.
- **Back-substitute:** $[\ce{COCl2}] \approx 0.25\ \text{M}$, $[\ce{CO}] = [\ce{Cl2}] = 7.4\times 10^{-6}\ \text{M}$.

**Answer:** $[\ce{COCl2}] \approx 0.25\ \text{M}$, $[\ce{CO}] = [\ce{Cl2}] = 7.4\times 10^{-6}\ \text{M}$. When $K$ is this small, dropping $x$ from the denominator turns a quadratic into a one-line square root — and the 5% check confirms it cost you nothing.

### Example 5: When the 5% Check *Fails* — Fall Back to the Quadratic

**Problem:** For $\ce{PCl5(g) <=> PCl3(g) + Cl2(g)}$, $K_c = 1.0\times 10^{-2}$. Start with $[\ce{PCl5}]_0 = 0.100\ \text{M}$, no products. Find the equilibrium concentrations.

**Solution:**
- **Direction:** forward. Table:

| | $\ce{PCl5}$ | $\ce{PCl3}$ | $\ce{Cl2}$ |
|---|---|---|---|
| **I** | $0.100$ | $0$ | $0$ |
| **C** | $-x$ | $+x$ | $+x$ |
| **E** | $0.100-x$ | $x$ | $x$ |

- **Try the approximation first:** $0.010 \approx \dfrac{x^2}{0.100} \Rightarrow x^2 = 0.0010 \Rightarrow x = 0.0316$.
- **Run the 5% check:** $\dfrac{0.0316}{0.100}\times 100\% = 31.6\% > 5\%$ ❌ **Fails badly.** $K$ wasn't small enough relative to the initial concentration, so we can't drop $x$. Redo it honestly.
- **Full quadratic:** $0.010 = \dfrac{x^2}{0.100 - x} \Rightarrow x^2 = 0.010(0.100 - x) = 0.0010 - 0.010x$.

$$x^2 + 0.010x - 0.0010 = 0$$

$$x = \frac{-0.010 + \sqrt{(0.010)^2 + 4(0.0010)}}{2} = \frac{-0.010 + \sqrt{0.0041}}{2} = \frac{-0.010 + 0.0640}{2} = 0.0270$$

- **Back-substitute:** $[\ce{PCl5}] = 0.100 - 0.0270 = 0.073\ \text{M}$, $[\ce{PCl3}] = [\ce{Cl2}] = 0.0270\ \text{M}$.
- **Check:** $\dfrac{(0.0270)^2}{0.073} = 0.0100$ ✓

**Answer:** $[\ce{PCl5}] = 0.073\ \text{M}$, $[\ce{PCl3}] = [\ce{Cl2}] = 0.0270\ \text{M}$. Notice the approximation's $0.0316$ was ~17% too high — that's exactly the error the 5% check exists to catch. **Always run the check; when it fails, the quadratic is mandatory.**

### Example 6: Use $Q$ to Pick the Direction (starting from a mix)

**Problem:** For $\ce{H2(g) + I2(g) <=> 2HI(g)}$, $K_c = 50.0$. A flask already contains $[\ce{H2}]_0 = 0.500\ \text{M}$, $[\ce{I2}]_0 = 0.500\ \text{M}$, and $[\ce{HI}]_0 = 1.00\ \text{M}$. Find the equilibrium concentrations.

**Solution:**
- **Step 1 — Which way does it go?** You start with a *mix*, so compute $Q$:

$$Q = \frac{[\ce{HI}]_0^2}{[\ce{H2}]_0[\ce{I2}]_0} = \frac{(1.00)^2}{(0.500)(0.500)} = 4.0$$

Since $Q = 4.0 < K = 50.0$, there are too few products → the reaction shifts **forward**. So $\ce{H2}$ and $\ce{I2}$ get $-x$, $\ce{HI}$ gets $+2x$.

| | $\ce{H2}$ | $\ce{I2}$ | $\ce{HI}$ |
|---|---|---|---|
| **I** | $0.500$ | $0.500$ | $1.00$ |
| **C** | $-x$ | $-x$ | $+2x$ |
| **E** | $0.500-x$ | $0.500-x$ | $1.00+2x$ |

- **Plug into $K$** (perfect square again — symmetric reactants):

$$50.0 = \frac{(1.00+2x)^2}{(0.500-x)^2} \Rightarrow \sqrt{50.0} = \frac{1.00+2x}{0.500-x} \Rightarrow 7.07 = \frac{1.00+2x}{0.500-x}$$

- **Solve:** $7.07(0.500 - x) = 1.00 + 2x \Rightarrow 3.54 - 7.07x = 1.00 + 2x \Rightarrow 2.54 = 9.07x \Rightarrow x = 0.280$.
- **Back-substitute:** $[\ce{H2}] = [\ce{I2}] = 0.220\ \text{M}$, $[\ce{HI}] = 1.00 + 2(0.280) = 1.56\ \text{M}$.
- **Check:** $\dfrac{(1.56)^2}{(0.220)^2} = 50.3 \approx 50.0$ ✓

**Answer:** $[\ce{H2}] = [\ce{I2}] = 0.220\ \text{M}$, $[\ce{HI}] = 1.56\ \text{M}$. Had you skipped $Q$ and guessed the wrong direction, every sign in the Change row would flip and you'd get a nonsense answer.

### Example 7: A $K_p$ (Gas-Pressure) Version

**Problem:** $\ce{N2O4(g) <=> 2NO2(g)}$ with $K_p = 0.150$. A flask starts with $P_{\ce{N2O4}} = 1.00\ \text{atm}$ and no $\ce{NO2}$. Find the equilibrium partial pressures.

**Solution:**
- ICE tables work identically for pressures — just use partial pressures in atm instead of molarities.

| | $\ce{N2O4}$ | $\ce{NO2}$ |
|---|---|---|
| **I** | $1.00$ | $0$ |
| **C** | $-x$ | $+2x$ |
| **E** | $1.00-x$ | $2x$ |

- **Plug into $K_p$:**

$$0.150 = \frac{(P_{\ce{NO2}})^2}{P_{\ce{N2O4}}} = \frac{(2x)^2}{1.00-x} = \frac{4x^2}{1.00-x}$$

- **Solve (quadratic):** $4x^2 = 0.150(1.00 - x) = 0.150 - 0.150x \Rightarrow 4x^2 + 0.150x - 0.150 = 0$.

$$x = \frac{-0.150 + \sqrt{(0.150)^2 + 4(4)(0.150)}}{2(4)} = \frac{-0.150 + \sqrt{2.4225}}{8} = \frac{-0.150 + 1.557}{8} = 0.176$$

- **Back-substitute:** $P_{\ce{N2O4}} = 1.00 - 0.176 = 0.824\ \text{atm}$, $P_{\ce{NO2}} = 2(0.176) = 0.352\ \text{atm}$.
- **Check:** $\dfrac{(0.352)^2}{0.824} = 0.150$ ✓

**Answer:** $P_{\ce{N2O4}} = 0.824\ \text{atm}$, $P_{\ce{NO2}} = 0.352\ \text{atm}$. Same ledger, same recipe — the only change is the units in the boxes.

### Example 8: Reverse Problem — Find $K$ from One Equilibrium Value

**Problem:** For $\ce{H2(g) + I2(g) <=> 2HI(g)}$, you start with $1.00\ \text{M}$ each of $\ce{H2}$ and $\ce{I2}$ and no $\ce{HI}$. At equilibrium you *measure* $[\ce{HI}] = 1.56\ \text{M}$. Find $K_c$.

**Solution:**
- **Step 1 — Use the one known value to find $x$.** The change in $\ce{HI}$ is $+2x$, and it went from $0$ to $1.56\ \text{M}$, so $2x = 1.56 \Rightarrow x = 0.780$.
- **Step 2 — Complete the ledger** with that $x$:

| | $\ce{H2}$ | $\ce{I2}$ | $\ce{HI}$ |
|---|---|---|---|
| **I** | $1.00$ | $1.00$ | $0$ |
| **C** | $-0.780$ | $-0.780$ | $+1.56$ |
| **E** | $0.220$ | $0.220$ | $1.56$ |

- **Step 3 — Plug the finished Equilibrium row into $K$:**

$$K_c = \frac{(1.56)^2}{(0.220)(0.220)} = \frac{2.43}{0.0484} = 50.3$$

**Answer:** $K_c \approx 50.3$. The reverse problem is *easier* — one measured value gives you $x$, you fill the whole table, and $K$ falls right out. No quadratic, ever.

### Example 9: Starting From Products (decomposition, coefficient $-2x$)

**Problem:** For $\ce{2HI(g) <=> H2(g) + I2(g)}$, $K_c = 0.0200$. Start with pure $\ce{HI}$ at $1.00\ \text{M}$ and no $\ce{H2}$ or $\ce{I2}$. Find the equilibrium concentrations.

**Solution:**
- **Direction:** only $\ce{HI}$ (the reactant here) is present, so it must decompose — shift **forward** as written. $\ce{HI}$ has coefficient 2 → $-2x$; the products get $+x$ each.

| | $\ce{HI}$ | $\ce{H2}$ | $\ce{I2}$ |
|---|---|---|---|
| **I** | $1.00$ | $0$ | $0$ |
| **C** | $-2x$ | $+x$ | $+x$ |
| **E** | $1.00-2x$ | $x$ | $x$ |

- **Plug into $K$:**

$$0.0200 = \frac{(x)(x)}{(1.00-2x)^2} = \frac{x^2}{(1.00-2x)^2}$$

- **Perfect square** → take the root: $\sqrt{0.0200} = \dfrac{x}{1.00-2x} \Rightarrow 0.1414 = \dfrac{x}{1.00-2x}$.
- **Solve:** $0.1414(1.00 - 2x) = x \Rightarrow 0.1414 - 0.2828x = x \Rightarrow 0.1414 = 1.283x \Rightarrow x = 0.110$.
- **Back-substitute:** $[\ce{HI}] = 1.00 - 2(0.110) = 0.780\ \text{M}$, $[\ce{H2}] = [\ce{I2}] = 0.110\ \text{M}$.
- **Check:** $\dfrac{(0.110)^2}{(0.780)^2} = 0.0199 \approx 0.0200$ ✓

**Answer:** $[\ce{HI}] = 0.780\ \text{M}$, $[\ce{H2}] = [\ce{I2}] = 0.110\ \text{M}$. The coefficient-2 reactant means the Change row is $-2x$, **not** $-x$ — the single most common ICE slip.

### Example 10: Find $K$ When the Measured Value Is a Reactant

**Problem:** For $\ce{PCl5(g) <=> PCl3(g) + Cl2(g)}$, you start with $[\ce{PCl5}]_0 = 1.00\ \text{M}$ and no products. At equilibrium, $[\ce{PCl5}] = 0.60\ \text{M}$. Find $K_c$.

**Solution:**
- **Step 1 — Find $x$ from the reactant's drop.** $\ce{PCl5}$ changed by $-x$: it fell from $1.00$ to $0.60$, so $x = 1.00 - 0.60 = 0.40$.
- **Step 2 — Complete the table:**

| | $\ce{PCl5}$ | $\ce{PCl3}$ | $\ce{Cl2}$ |
|---|---|---|---|
| **I** | $1.00$ | $0$ | $0$ |
| **C** | $-0.40$ | $+0.40$ | $+0.40$ |
| **E** | $0.60$ | $0.40$ | $0.40$ |

- **Step 3 — Compute $K$:**

$$K_c = \frac{(0.40)(0.40)}{0.60} = \frac{0.16}{0.60} = 0.27$$

**Answer:** $K_c = 0.27$. Whether the given equilibrium value is a reactant or a product, the move is identical: use it to pin down $x$, fill the ledger, then read $K$.

### Example 11: $Q > K$ — the Reaction Runs *Backward* (sign of $x$ flips)

**Problem:** For $\ce{PCl5(g) <=> PCl3(g) + Cl2(g)}$, $K_c = 0.040$. A flask contains $[\ce{PCl5}]_0 = 0.10\ \text{M}$, $[\ce{PCl3}]_0 = 0.20\ \text{M}$, $[\ce{Cl2}]_0 = 0.20\ \text{M}$. Find the equilibrium concentrations.

**Solution:**
- **Step 1 — Compute $Q$:**

$$Q = \frac{[\ce{PCl3}]_0[\ce{Cl2}]_0}{[\ce{PCl5}]_0} = \frac{(0.20)(0.20)}{0.10} = 0.40$$

Since $Q = 0.40 > K = 0.040$, there are **too many products** → the reaction shifts **reverse**. That flips every sign: the products get $-x$ and the reactant $\ce{PCl5}$ gets $+x$.

| | $\ce{PCl5}$ | $\ce{PCl3}$ | $\ce{Cl2}$ |
|---|---|---|---|
| **I** | $0.10$ | $0.20$ | $0.20$ |
| **C** | $+x$ | $-x$ | $-x$ |
| **E** | $0.10+x$ | $0.20-x$ | $0.20-x$ |

- **Plug into $K$:**

$$0.040 = \frac{(0.20-x)^2}{0.10+x}$$

- **Solve (quadratic):** $(0.20 - x)^2 = 0.040(0.10 + x) \Rightarrow 0.040 - 0.40x + x^2 = 0.0040 + 0.040x$.

$$x^2 - 0.44x + 0.036 = 0 \Rightarrow x = \frac{0.44 \pm \sqrt{(0.44)^2 - 4(0.036)}}{2} = \frac{0.44 \pm \sqrt{0.0496}}{2} = \frac{0.44 \pm 0.223}{2}$$

- **Two roots:** $x = 0.331$ or $x = 0.109$. **Reject $x = 0.331$** — it makes $[\ce{Cl2}] = 0.20 - 0.331 < 0$. Keep $x = 0.109$.
- **Back-substitute:** $[\ce{PCl5}] = 0.10 + 0.109 = 0.209\ \text{M}$, $[\ce{PCl3}] = [\ce{Cl2}] = 0.20 - 0.109 = 0.091\ \text{M}$.
- **Check:** $\dfrac{(0.091)^2}{0.209} = 0.040$ ✓

**Answer:** $[\ce{PCl5}] = 0.209\ \text{M}$, $[\ce{PCl3}] = [\ce{Cl2}] = 0.091\ \text{M}$. This is the whole reason we compute $Q$ first: it decided that $x$ subtracts from the products and adds to the reactant, not the other way around.

---

## Common Mistakes

| Mistake | Why it happens | How to avoid it |
|---|---|---|
| Forgetting the coefficient multiplier on $x$ (writing $-x$ where it should be $-2x$ or $-3x$) | You focus on "the change is $x$" and ignore stoichiometry | The multiplier on $x$ **is** the balanced coefficient — copy it straight from the equation, same as any mole ratio |
| Wrong **sign** of $x$ (running the reaction the wrong direction) | Assuming it always shifts forward | If you start with a *mix*, **compute $Q$ and compare to $K$** first; $Q<K$ forward, $Q>K$ reverse |
| Applying the small-$x$ approximation when $K$ isn't small enough | The setup *looks* like other approximation problems | **Always run the 5% check.** If $x/[\text{initial}] > 5\%$, discard it and solve the quadratic |
| Keeping the negative (or physically impossible) root of the quadratic | Both roots are "valid" algebraically | **Reject any root that makes a concentration negative** — only one root is real |
| Putting pure **solids or liquids** in the table / $K$ expression | Habit of listing every species | Solids and liquids get **no column** and never appear in $K$ — only gases and aqueous species |
| Mixing up $Q$ and $K$ | They use the identical expression | $Q$ uses **current/initial** concentrations; $K$ uses **equilibrium** concentrations — $Q$ tells you which way to move |
| Forgetting to convert given moles to **molarity** (or moles-to-pressure) | The problem hands you moles and a volume | Divide by volume to get concentration **before** filling the Initial row; ICE runs on M (or atm), not moles |
| Not sanity-checking the answer | Rushing to the final number | Plug your equilibrium concentrations back into $K$ — it should reproduce the given value |

---

## AP Exam Tips

- **ICE tables are everywhere.** Nearly every equilibrium *and* acid–base FRQ (Units 7 and 8) is built on an ICE table. This is the single highest-leverage calculation skill in the back half of the course — drill it until it's automatic.
- **Coefficient multipliers and the sign of $x$ are the two points graders love to dock.** Copy coefficients straight onto the Change row; use $-$ for consumed, $+$ for produced. Show the Change row explicitly — it earns method points even if the arithmetic slips.
- **Master the small-$x$ approximation *with* the 5% validation.** This is a signature AP move, especially for weak acids/bases where $K_a$ or $K_b$ is tiny. Write the approximation, solve, then *show* the $\dfrac{x}{[\text{initial}]}\times 100\%$ check. If it exceeds 5%, state that and redo with the quadratic — graders want to see the check, not just the shortcut.
- **When they give you a mix, they're testing $Q$.** Compute $Q$, compare to $K$, and *state the direction in words* ("since $Q < K$, the reaction proceeds forward"). That sentence is often worth its own point and it fixes your signs.
- **Keep the quadratic formula ready.** No approximation, no perfect square? Go straight to $x = \dfrac{-b \pm \sqrt{b^2-4ac}}{2a}$ and reject the root that gives a negative concentration. A graphing calculator is allowed on the calculator sections — use it.
- **Convert to concentration (or pressure) first.** If the problem gives grams or moles plus a volume, get to molarity before the Initial row. $K_p$ problems run on atm; the ICE machinery is identical.
- **Always back-check.** Time permitting, plug your final concentrations into $K$. If it reproduces the given constant, you're done and confident.

---

## Practice Problems

### Problem 1
Write the Change row (in terms of $x$, forward direction) for $\ce{2SO2(g) + O2(g) <=> 2SO3(g)}$, starting with only reactants.

<details>
<summary><strong>Solution</strong></summary>

Reactants are consumed ($-$), product is produced ($+$), each scaled by its coefficient: $\ce{SO2}$ is $-2x$, $\ce{O2}$ is $-x$, $\ce{SO3}$ is $+2x$.

**Answer:** $\ce{SO2}: -2x$, $\ce{O2}: -x$, $\ce{SO3}: +2x$.

</details>

---

### Problem 2
For $\ce{H2(g) + I2(g) <=> 2HI(g)}$, $K_c = 64.0$. Start with $1.00\ \text{M}$ each of $\ce{H2}$ and $\ce{I2}$, no $\ce{HI}$. Find all equilibrium concentrations.

<details>
<summary><strong>Solution</strong></summary>

ICE: $\ce{H2} = \ce{I2} = 1.00 - x$, $\ce{HI} = 2x$. Then $64.0 = \dfrac{(2x)^2}{(1.00-x)^2}$. Perfect square → $\sqrt{64.0} = 8.00 = \dfrac{2x}{1.00-x}$. So $8.00 - 8.00x = 2x \Rightarrow 8.00 = 10.0x \Rightarrow x = 0.800$.

$[\ce{H2}] = [\ce{I2}] = 0.200\ \text{M}$, $[\ce{HI}] = 1.60\ \text{M}$. Check: $(1.60)^2/(0.200)^2 = 64$ ✓

**Answer:** $[\ce{H2}] = [\ce{I2}] = 0.200\ \text{M}$, $[\ce{HI}] = 1.60\ \text{M}$.

</details>

---

### Problem 3
For $\ce{PCl5(g) <=> PCl3(g) + Cl2(g)}$, $K_c = 0.040$. Start with $[\ce{PCl5}]_0 = 0.50\ \text{M}$, no products. Find the equilibrium concentrations.

<details>
<summary><strong>Solution</strong></summary>

ICE: $\ce{PCl5} = 0.50 - x$, $\ce{PCl3} = \ce{Cl2} = x$. Then $0.040 = \dfrac{x^2}{0.50 - x}$.

Quick approximation check: $x \approx \sqrt{0.040 \times 0.50} = \sqrt{0.020} = 0.141$; $0.141/0.50 = 28\% > 5\%$ → fails, use the quadratic.

$x^2 = 0.040(0.50 - x) \Rightarrow x^2 + 0.040x - 0.020 = 0$. $x = \dfrac{-0.040 + \sqrt{0.0016 + 0.080}}{2} = \dfrac{-0.040 + 0.2857}{2} = 0.123$.

$[\ce{PCl5}] = 0.377\ \text{M}$, $[\ce{PCl3}] = [\ce{Cl2}] = 0.123\ \text{M}$. Check: $(0.123)^2/0.377 = 0.040$ ✓

**Answer:** $[\ce{PCl5}] = 0.38\ \text{M}$, $[\ce{PCl3}] = [\ce{Cl2}] = 0.12\ \text{M}$.

</details>

---

### Problem 4
$\ce{A(g) <=> B(g) + C(g)}$, $K_c = 3.0\times 10^{-12}$, $[\ce{A}]_0 = 0.50\ \text{M}$, no products. Find $[\ce{B}]$ at equilibrium, and confirm the approximation is valid.

<details>
<summary><strong>Solution</strong></summary>

ICE: $\ce{A} = 0.50 - x \approx 0.50$, $\ce{B} = \ce{C} = x$. Then $3.0\times 10^{-12} \approx \dfrac{x^2}{0.50} \Rightarrow x^2 = 1.5\times 10^{-12} \Rightarrow x = 1.2\times 10^{-6}$.

5% check: $\dfrac{1.2\times 10^{-6}}{0.50}\times 100\% = 2.4\times 10^{-4}\% \le 5\%$ ✓

**Answer:** $[\ce{B}] = 1.2\times 10^{-6}\ \text{M}$; the approximation is valid (well under 5%).

</details>

---

### Problem 5
For $\ce{N2O4(g) <=> 2NO2(g)}$, $K_c = 0.36$, $[\ce{N2O4}]_0 = 0.100\ \text{M}$, no $\ce{NO2}$. Find the equilibrium concentrations.

<details>
<summary><strong>Solution</strong></summary>

ICE: $\ce{N2O4} = 0.100 - x$, $\ce{NO2} = 2x$. Then $0.36 = \dfrac{(2x)^2}{0.100 - x} = \dfrac{4x^2}{0.100 - x}$.

$4x^2 = 0.36(0.100 - x) = 0.036 - 0.36x \Rightarrow 4x^2 + 0.36x - 0.036 = 0$. $x = \dfrac{-0.36 + \sqrt{0.1296 + 0.576}}{8} = \dfrac{-0.36 + 0.840}{8} = 0.0600$.

$[\ce{N2O4}] = 0.040\ \text{M}$, $[\ce{NO2}] = 0.120\ \text{M}$. Check: $(0.120)^2/0.040 = 0.36$ ✓

**Answer:** $[\ce{N2O4}] = 0.040\ \text{M}$, $[\ce{NO2}] = 0.120\ \text{M}$.

</details>

---

### Problem 6
For $\ce{CO(g) + Cl2(g) <=> COCl2(g)}$, $K_c = 5.0$. A flask has $[\ce{CO}]_0 = 1.00\ \text{M}$, $[\ce{Cl2}]_0 = 1.00\ \text{M}$, $[\ce{COCl2}]_0 = 0$. Find equilibrium concentrations.

<details>
<summary><strong>Solution</strong></summary>

ICE: $\ce{CO} = \ce{Cl2} = 1.00 - x$, $\ce{COCl2} = x$. Then $5.0 = \dfrac{x}{(1.00-x)^2}$.

$5.0(1.00 - x)^2 = x \Rightarrow 5.0(1 - 2x + x^2) = x \Rightarrow 5.0x^2 - 11x + 5.0 = 0$. $x = \dfrac{11 \pm \sqrt{121 - 100}}{10} = \dfrac{11 \pm 4.58}{10}$. Roots: $1.56$ (rejected, gives negative $\ce{CO}$) or $0.642$.

$[\ce{CO}] = [\ce{Cl2}] = 0.358\ \text{M}$, $[\ce{COCl2}] = 0.642\ \text{M}$. Check: $0.642/(0.358)^2 = 5.0$ ✓

**Answer:** $[\ce{CO}] = [\ce{Cl2}] = 0.358\ \text{M}$, $[\ce{COCl2}] = 0.642\ \text{M}$.

</details>

---

### Problem 7
For $\ce{H2(g) + I2(g) <=> 2HI(g)}$, $K_c = 50.0$. A flask starts with $[\ce{H2}]_0 = 0.200\ \text{M}$, $[\ce{I2}]_0 = 0.200\ \text{M}$, $[\ce{HI}]_0 = 2.00\ \text{M}$. Which direction does the reaction shift?

<details>
<summary><strong>Solution</strong></summary>

$Q = \dfrac{(2.00)^2}{(0.200)(0.200)} = \dfrac{4.00}{0.0400} = 100$. Since $Q = 100 > K = 50.0$, there are too many products → the reaction shifts **reverse** (to the left). So $\ce{HI}$ would get $-2x$ and $\ce{H2}$, $\ce{I2}$ would get $+x$.

**Answer:** Reverse (toward reactants), because $Q > K$.

</details>

---

### Problem 8
For $\ce{2NOBr(g) <=> 2NO(g) + Br2(g)}$, you start with $[\ce{NOBr}]_0 = 0.80\ \text{M}$, no products. At equilibrium, $[\ce{Br2}] = 0.10\ \text{M}$. Find $K_c$.

<details>
<summary><strong>Solution</strong></summary>

$\ce{Br2}$ changed by $+x$ from 0, so $x = 0.10$. Change row: $\ce{NOBr} = -2x = -0.20$, $\ce{NO} = +2x = +0.20$, $\ce{Br2} = +x = +0.10$.

Equilibrium: $[\ce{NOBr}] = 0.80 - 0.20 = 0.60$, $[\ce{NO}] = 0.20$, $[\ce{Br2}] = 0.10$.

$K_c = \dfrac{[\ce{NO}]^2[\ce{Br2}]}{[\ce{NOBr}]^2} = \dfrac{(0.20)^2(0.10)}{(0.60)^2} = \dfrac{0.0040}{0.36} = 0.011$.

**Answer:** $K_c = 0.011$.

</details>

---

### Problem 9
For $\ce{2HI(g) <=> H2(g) + I2(g)}$, $K_c = 0.0625$, start with $[\ce{HI}]_0 = 2.00\ \text{M}$, no products. Find the equilibrium concentrations.

<details>
<summary><strong>Solution</strong></summary>

ICE: $\ce{HI} = 2.00 - 2x$, $\ce{H2} = \ce{I2} = x$. Then $0.0625 = \dfrac{x^2}{(2.00-2x)^2}$. Perfect square → $\sqrt{0.0625} = 0.250 = \dfrac{x}{2.00 - 2x}$.

$0.250(2.00 - 2x) = x \Rightarrow 0.500 - 0.500x = x \Rightarrow 0.500 = 1.50x \Rightarrow x = 0.333$.

$[\ce{HI}] = 2.00 - 0.667 = 1.33\ \text{M}$, $[\ce{H2}] = [\ce{I2}] = 0.333\ \text{M}$. Check: $(0.333)^2/(1.33)^2 = 0.0627$ ✓

**Answer:** $[\ce{HI}] = 1.33\ \text{M}$, $[\ce{H2}] = [\ce{I2}] = 0.333\ \text{M}$.

</details>

---

### Problem 10
For $\ce{N2O4(g) <=> 2NO2(g)}$, $K_p = 0.66\ \text{atm}$. Start with $P_{\ce{N2O4}} = 0.50\ \text{atm}$, no $\ce{NO2}$. Find the equilibrium partial pressures.

<details>
<summary><strong>Solution</strong></summary>

ICE (atm): $\ce{N2O4} = 0.50 - x$, $\ce{NO2} = 2x$. Then $0.66 = \dfrac{4x^2}{0.50 - x}$.

$4x^2 = 0.66(0.50 - x) = 0.33 - 0.66x \Rightarrow 4x^2 + 0.66x - 0.33 = 0$. $x = \dfrac{-0.66 + \sqrt{0.4356 + 5.28}}{8} = \dfrac{-0.66 + 2.391}{8} = 0.216$.

$P_{\ce{N2O4}} = 0.284\ \text{atm}$, $P_{\ce{NO2}} = 0.433\ \text{atm}$. Check: $(0.433)^2/0.284 = 0.66$ ✓

**Answer:** $P_{\ce{N2O4}} = 0.28\ \text{atm}$, $P_{\ce{NO2}} = 0.43\ \text{atm}$.

</details>

---

### Problem 11
For $\ce{PCl5(g) <=> PCl3(g) + Cl2(g)}$, $K_c = 0.040$, a flask contains $[\ce{PCl5}]_0 = 0.50\ \text{M}$, $[\ce{PCl3}]_0 = 0.50\ \text{M}$, $[\ce{Cl2}]_0 = 0.50\ \text{M}$. Which way does it shift, and by how much (find $x$)?

<details>
<summary><strong>Solution</strong></summary>

$Q = \dfrac{(0.50)(0.50)}{0.50} = 0.50$. Since $Q = 0.50 > K = 0.040$, shift **reverse**: $\ce{PCl5} = +x$, $\ce{PCl3} = \ce{Cl2} = -x$.

$0.040 = \dfrac{(0.50-x)^2}{0.50+x} \Rightarrow (0.50 - x)^2 = 0.040(0.50 + x) \Rightarrow 0.25 - 1.00x + x^2 = 0.020 + 0.040x$.

$x^2 - 1.04x + 0.23 = 0 \Rightarrow x = \dfrac{1.04 \pm \sqrt{1.0816 - 0.92}}{2} = \dfrac{1.04 \pm 0.402}{2}$. Roots: $0.721$ (rejected, negative $\ce{Cl2}$) or $0.319$.

$[\ce{PCl5}] = 0.82\ \text{M}$, $[\ce{PCl3}] = [\ce{Cl2}] = 0.18\ \text{M}$. Check: $(0.18)^2/0.82 = 0.040$ ✓

**Answer:** Reverse shift; $x = 0.319$, giving $[\ce{PCl5}] = 0.82\ \text{M}$, $[\ce{PCl3}] = [\ce{Cl2}] = 0.18\ \text{M}$.

</details>

---

### Problem 12
A student writes the Change row for $\ce{N2 + 3H2 <=> 2NH3}$ (forward) as $\ce{N2}: -x$, $\ce{H2}: -x$, $\ce{NH3}: +x$. Identify every error.

<details>
<summary><strong>Solution</strong></summary>

Two coefficient-multiplier errors: $\ce{H2}$ has coefficient 3, so its change is $-3x$ (not $-x$), and $\ce{NH3}$ has coefficient 2, so its change is $+2x$ (not $+x$). Only $\ce{N2}$ ($-x$) is correct.

**Answer:** Correct Change row is $\ce{N2}: -x$, $\ce{H2}: -3x$, $\ce{NH3}: +2x$. The student ignored the stoichiometric coefficients on $\ce{H2}$ and $\ce{NH3}$.

</details>

---

### Problem 13
For $\ce{H2(g) + I2(g) <=> 2HI(g)}$, $K_c = 50.0$, a flask starts with $[\ce{H2}]_0 = 1.00\ \text{M}$, $[\ce{I2}]_0 = 2.00\ \text{M}$, no $\ce{HI}$. Find the equilibrium concentrations. (Unequal starts — expect the quadratic.)

<details>
<summary><strong>Solution</strong></summary>

ICE: $\ce{H2} = 1.00 - x$, $\ce{I2} = 2.00 - x$, $\ce{HI} = 2x$. Then $50.0 = \dfrac{(2x)^2}{(1.00-x)(2.00-x)}$ (not a perfect square — unequal denominator).

$4x^2 = 50.0(2.00 - 3.00x + x^2) = 100 - 150x + 50.0x^2 \Rightarrow 46.0x^2 - 150x + 100 = 0$.

$x = \dfrac{150 \pm \sqrt{22500 - 18400}}{92.0} = \dfrac{150 \pm 64.0}{92.0}$. Roots: $2.33$ (rejected, negative $\ce{H2}$) or $0.935$.

$[\ce{H2}] = 0.065\ \text{M}$, $[\ce{I2}] = 1.065\ \text{M}$, $[\ce{HI}] = 1.87\ \text{M}$. Check: $(1.87)^2/(0.065 \times 1.065) = 50.5$ ✓

**Answer:** $[\ce{H2}] = 0.065\ \text{M}$, $[\ce{I2}] = 1.07\ \text{M}$, $[\ce{HI}] = 1.87\ \text{M}$.

</details>

---

### Problem 14
For $\ce{CaCO3(s) <=> CaO(s) + CO2(g)}$, $K_p = 0.20$. If you put solid $\ce{CaCO3}$ in an empty sealed flask, what is the equilibrium pressure of $\ce{CO2}$? Explain why no ICE algebra is needed.

<details>
<summary><strong>Solution</strong></summary>

Solids don't appear in $K$, so $K_p = P_{\ce{CO2}}$ directly. There's only one gas and its pressure equals $K_p$ regardless of how much solid is present.

$P_{\ce{CO2}} = 0.20\ \text{atm}$.

**Answer:** $P_{\ce{CO2}} = 0.20\ \text{atm}$. The two solids get no columns and cancel out of the expression, so $K_p$ *is* the answer — no $x$ to solve for.

</details>

---

### Problem 15
For $\ce{2SO2(g) + O2(g) <=> 2SO3(g)}$, you start with $[\ce{SO2}]_0 = 2.00\ \text{M}$, $[\ce{O2}]_0 = 1.00\ \text{M}$, no $\ce{SO3}$. At equilibrium, $[\ce{SO3}] = 1.50\ \text{M}$. Find $K_c$.

<details>
<summary><strong>Solution</strong></summary>

$\ce{SO3}$ changed by $+2x$ from 0, so $2x = 1.50 \Rightarrow x = 0.75$. Change row: $\ce{SO2} = -2x = -1.50$, $\ce{O2} = -x = -0.75$, $\ce{SO3} = +1.50$.

Equilibrium: $[\ce{SO2}] = 2.00 - 1.50 = 0.50$, $[\ce{O2}] = 1.00 - 0.75 = 0.25$, $[\ce{SO3}] = 1.50$.

$K_c = \dfrac{[\ce{SO3}]^2}{[\ce{SO2}]^2[\ce{O2}]} = \dfrac{(1.50)^2}{(0.50)^2(0.25)} = \dfrac{2.25}{0.0625} = 36$.

**Answer:** $K_c = 36$.

</details>

---

## Quick Reference

| Concept | Key idea |
|---|---|
| **ICE table** | Three rows — **I**nitial, **C**hange, **E**quilibrium — one **column per species** (gases/aqueous only) |
| **Allowance-ledger map** | Initial = starting balance · Change = linked deposits/withdrawals · Equilibrium = ending balance · plug into $K$ = balancing the checkbook |
| **Change row** | Coefficient $\times\, x$; reactants **negative**, products **positive** (for a forward shift) |
| **Equilibrium row** | Initial $+$ Change, down each column |
| **The recipe** | Balance → direction → build ICE → plug into $K$ → solve for $x$ → back-substitute → check |
| **Reaction quotient $Q$** | Same expression as $K$ but with **current** concentrations; sets the shift direction |
| **Direction rule** | $Q<K$ → forward ($+x$ products) · $Q>K$ → reverse ($-x$ products) · $Q=K$ → no change |
| **Perfect square** | If both sides are squares, take $\sqrt{\ }$ of the whole equation — no quadratic |
| **Small-$x$ approximation** | If $K$ is small, assume $[\text{A}]_0 - x \approx [\text{A}]_0$; solve by square root |
| **5% validation** | $\dfrac{x}{[\text{initial}]}\times 100\% \le 5\%$ → keep it; **else use the quadratic** |
| **Quadratic formula** | $x = \dfrac{-b \pm \sqrt{b^2 - 4ac}}{2a}$; **reject** the root giving a negative concentration |
| **Reverse problem (find $K$)** | Use one measured equilibrium value to get $x$, complete the table, compute $K$ |
| **$K_p$ version** | Identical method with partial pressures (atm) instead of molarities |

---

<div align="center">

[← The Equilibrium Constant](/chemistry/0902-equilibrium-constant) | [Le Chatelier's Principle →](/chemistry/0904-le-chatelier)

</div>
