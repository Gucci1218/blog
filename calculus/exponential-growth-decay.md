# Exponential Growth and Decay
<p class="article-date">April 23, 2026</p>

*Your Starbucks caramel frappe is sitting on the dashboard, slowly warming up in the San Diego sun. A colony of bacteria is doubling every hour in a petri dish during Science Olympiad practice. The hype around a new K-pop comeback is spreading through your school like wildfire. What do all these have in common? They're all governed by the same elegant equation — the exponential model. One equation, endless applications.*

---

## What You'll Learn
- Derive the exponential growth/decay model from $\frac{dy}{dt} = ky$
- Distinguish between growth ($k > 0$) and decay ($k < 0$)
- Solve problems involving doubling time and half-life
- Apply Newton's Law of Cooling
- Set up and solve the logistic growth model (BC only)
- Interpret growth/decay models in real-world contexts

---

## Prerequisites
- [Separable DEs](/calculus/separable-de)
- [Exponential Functions](/calculus/0111-exponential-functions)
- [Logarithmic Functions](/calculus/0112-logarithmic-functions)

---

## The Core Concept

### The Big Idea

Many quantities in nature change at a rate **proportional to their current size**:

$$\frac{dy}{dt} = ky$$

- More bacteria → more reproduction → faster growth
- More radioactive atoms → more decay events → faster decay
- Bigger temperature difference → faster cooling

This single equation is arguably the most important DE in all of science.

### Solving It (One Last Time)

We solved this in the [previous article](/calculus/separable-de), but it's worth repeating because of how fundamental it is:

$$\frac{dy}{y} = k \, dt$$

$$\ln|y| = kt + C$$

$$y = Ae^{kt}$$

With initial condition $y(0) = y_0$: $A = y_0$

$$\boxed{y(t) = y_0 e^{kt}}$$

### Growth vs. Decay

| Condition | Behavior | Example |
|-----------|----------|---------|
| $k > 0$ | **Exponential growth** — $y$ increases without bound | Population, compound interest |
| $k < 0$ | **Exponential decay** — $y$ approaches $0$ | Radioactive decay, cooling |
| $k = 0$ | **Constant** — nothing changes | Equilibrium |

---

## Doubling Time and Half-Life

### Doubling Time ($k > 0$)

The **doubling time** $T_d$ is how long it takes for $y$ to double.

Set $y(T_d) = 2y_0$:

$$2y_0 = y_0 e^{kT_d}$$

$$2 = e^{kT_d}$$

$$\boxed{T_d = \frac{\ln 2}{k}}$$

**Key insight:** Doubling time depends only on $k$, not on the starting amount. Whether you start with 10 bacteria or 10 million, they all double in the same time.

### Half-Life ($k < 0$)

The **half-life** $T_{1/2}$ is how long it takes for $y$ to halve.

Set $y(T_{1/2}) = \frac{y_0}{2}$:

$$\frac{y_0}{2} = y_0 e^{kT_{1/2}}$$

$$\frac{1}{2} = e^{kT_{1/2}}$$

$$\boxed{T_{1/2} = \frac{\ln 2}{|k|} = -\frac{\ln 2}{k}}$$

Same formula (essentially), because $\ln 2$ is $\ln 2$ whether you're doubling or halving. It's symmetric.

---

## Worked Examples

### Example 1: Population Growth

**A colony of bacteria starts with 500 cells and grows to 1,500 cells in 4 hours. Find the population after 10 hours.**

**Step 1 — Set up the model:**

$$P(t) = P_0 e^{kt} = 500e^{kt}$$

**Step 2 — Find $k$ using the given data:**

$$1500 = 500e^{4k}$$

$$3 = e^{4k}$$

$$4k = \ln 3$$

$$k = \frac{\ln 3}{4} \approx 0.2747$$

**Step 3 — Answer the question:**

$$P(10) = 500e^{10 \cdot \frac{\ln 3}{4}} = 500e^{\frac{10\ln 3}{4}} = 500 \cdot 3^{10/4} = 500 \cdot 3^{2.5}$$

$$= 500 \cdot 3^2 \cdot 3^{0.5} = 500 \cdot 9 \cdot \sqrt{3} \approx 500 \cdot 15.588$$

$$\boxed{P(10) \approx 7{,}794 \text{ bacteria}}$$

---

### Example 2: Radioactive Decay

**Carbon-14 has a half-life of 5,730 years. A fossil contains 30% of its original Carbon-14. How old is it?**

**Step 1 — Find $k$:**

$$T_{1/2} = \frac{\ln 2}{|k|}$$

$$|k| = \frac{\ln 2}{5730} \approx 0.0001210$$

$$k = -0.0001210 \quad \text{(negative because decay)}$$

**Step 2 — Set up and solve:**

$$0.30 \cdot y_0 = y_0 e^{kt}$$

$$0.30 = e^{-0.0001210 \cdot t}$$

$$\ln(0.30) = -0.0001210 \cdot t$$

$$t = \frac{-\ln(0.30)}{0.0001210} = \frac{1.2040}{0.0001210}$$

$$\boxed{t \approx 9{,}950 \text{ years old}}$$

---

### Example 3: Compound Interest

**You invest $1,000 at 5% annual interest, compounded continuously. How long until your money doubles?**

Continuous compounding: $A(t) = A_0 e^{rt}$ where $r = 0.05$.

**Doubling time:**

$$T_d = \frac{\ln 2}{r} = \frac{0.6931}{0.05} = 13.86 \text{ years}$$

**The Rule of 70:** For a quick estimate, $T_d \approx \frac{70}{r\%}$. At 5%: $T_d \approx \frac{70}{5} = 14$ years. Close to the exact answer!

This is handy when you're doing mental math — like figuring out how long until you've saved enough for that Starbucks gift card to "double" in value (if only interest rates were that generous).

---

### Example 4: Finding the Rate

**A cup of Sesame Donuts coffee cools from $180°F$ to $150°F$ in 5 minutes. The room is $68°F$. Find the temperature after 15 minutes.**

This is **Newton's Law of Cooling** (see section below), but first let's set it up:

$$\frac{dT}{dt} = k(T - 68)$$

$$T(t) = 68 + (T_0 - 68)e^{kt} = 68 + 112e^{kt}$$

**Find $k$:** $T(5) = 150$:

$$150 = 68 + 112e^{5k}$$

$$82 = 112e^{5k}$$

$$e^{5k} = \frac{82}{112} = \frac{41}{56}$$

$$k = \frac{1}{5}\ln\left(\frac{41}{56}\right) \approx \frac{-0.3118}{5} \approx -0.06236$$

**Find $T(15)$:**

$$T(15) = 68 + 112e^{15(-0.06236)}$$

$$= 68 + 112e^{-0.9354}$$

$$= 68 + 112(0.3927)$$

$$= 68 + 43.98$$

$$\boxed{T(15) \approx 112°F}$$

By the time you've driven from Sesame Donuts back home to Rancho Bernardo, the coffee is a comfortable drinking temperature.

---

## Newton's Law of Cooling

### The Model

Newton's Law of Cooling states that the rate of temperature change is proportional to the difference between the object's temperature and the surrounding temperature:

$$\boxed{\frac{dT}{dt} = k(T - T_{\text{env}})}$$

where $T_{\text{env}}$ is the environmental (ambient) temperature.

### The Solution

This is separable:

$$\frac{dT}{T - T_{\text{env}}} = k \, dt$$

$$\ln|T - T_{\text{env}}| = kt + C$$

$$T - T_{\text{env}} = Ae^{kt}$$

$$\boxed{T(t) = T_{\text{env}} + (T_0 - T_{\text{env}})e^{kt}}$$

**Important:** $k < 0$ for cooling (hot object in cooler room) and $k < 0$ also for warming (cold object in warmer room). In both cases, the temperature approaches $T_{\text{env}}$.

### Why It Works Intuitively

The farther your temperature is from the room temperature, the faster it changes. A scorching $200°F$ BBQ brisket cools fast at first, then slower and slower as it approaches room temp. Your mint chocolate chip ice cream melts fast when you first pull it out of the freezer, then the melting slows as it nears room temperature.

The temperature *never actually reaches* $T_{\text{env}}$ — it approaches asymptotically, like a solution curve approaching an equilibrium in a slope field.

---

## Logistic Growth (BC Only)

### Why Exponential Growth Can't Last Forever

Pure exponential growth assumes unlimited resources — but in reality, populations run out of food, diseases run out of hosts, and viral K-pop dance challenges eventually reach everyone at school.

The **logistic model** accounts for a **carrying capacity** $M$ — a maximum sustainable population:

$$\boxed{\frac{dP}{dt} = kP(M - P)}$$

When $P$ is small: $M - P \approx M$, so $\frac{dP}{dt} \approx kMP$ (approximately exponential growth)

When $P$ is near $M$: $M - P \approx 0$, so $\frac{dP}{dt} \approx 0$ (growth stalls)

### The Solution

The logistic equation is separable (we solved $\frac{dy}{dx} = y(1-y)$ in the previous article using partial fractions):

$$\boxed{P(t) = \frac{M}{1 + Be^{-kMt}}}$$

where $B = \frac{M - P_0}{P_0}$.

### The S-Curve

The logistic solution produces a characteristic **S-shaped (sigmoid) curve**:

```
P
M ──────────────────────────────
                         ·····
                      ··
                    ·
                  ·     ← Inflection point at P = M/2
                ·        (fastest growth)
              ·
           ··
       ····
───────────────────────────────→ t
```

### Key Properties of Logistic Growth

| Property | Value / Explanation |
|----------|-------------------|
| Equilibria | $P = 0$ (unstable) and $P = M$ (stable) |
| Fastest growth | At $P = \frac{M}{2}$ (inflection point) |
| Max growth rate | $\frac{dP}{dt}_{\max} = \frac{kM^2}{4}$ |
| Long-term behavior | $P \to M$ as $t \to \infty$ |
| Concavity change | Concave up for $P < \frac{M}{2}$, concave down for $P > \frac{M}{2}$ |

### Example 5: Logistic Growth Problem

**The spread of a dance trend at Rancho Bernardo High follows the logistic model:**

$$\frac{dP}{dt} = 0.001P(2000 - P)$$

**where $P$ is the number of students who've learned the dance and $2000$ is the school population. Initially, $P(0) = 50$ students know the dance.**

**(a) What is the carrying capacity?**

$M = 2000$ (the whole school)

**(b) At what population level is the dance spreading fastest?**

$P = \frac{M}{2} = 1000$ students

**(c) Find the maximum rate of spread.**

$$\frac{dP}{dt}\bigg|_{\max} = 0.001 \cdot 1000 \cdot (2000 - 1000) = 0.001 \cdot 1000 \cdot 1000 = 1000 \text{ students/unit time}$$

**(d) Write the solution.**

$B = \frac{M - P_0}{P_0} = \frac{2000 - 50}{50} = 39$

$kM = 0.001 \times 2000 = 2$

$$\boxed{P(t) = \frac{2000}{1 + 39e^{-2t}}}$$

---

### Example 6: Logistic with Given Data

**A lake can support 10,000 fish. Currently there are 2,000 fish, and the population is growing at 1,200 fish per year. Find $k$ in the logistic model.**

$$\frac{dP}{dt} = kP(M - P)$$

$$1200 = k \cdot 2000 \cdot (10000 - 2000)$$

$$1200 = k \cdot 2000 \cdot 8000$$

$$1200 = 16{,}000{,}000 \cdot k$$

$$k = \frac{1200}{16{,}000{,}000} = 0.000075$$

---

## Key Formulas & Rules

### Exponential Model

| Formula | Use |
|---------|-----|
| $y = y_0 e^{kt}$ | General exponential growth/decay |
| $T_d = \frac{\ln 2}{k}$ | Doubling time (when $k > 0$) |
| $T_{1/2} = \frac{\ln 2}{\|k\|}$ | Half-life (when $k < 0$) |
| Rule of 70: $T_d \approx \frac{70}{r\%}$ | Quick doubling time estimate |

### Newton's Law of Cooling

| Formula | Use |
|---------|-----|
| $\frac{dT}{dt} = k(T - T_{\text{env}})$ | The DE |
| $T(t) = T_{\text{env}} + (T_0 - T_{\text{env}})e^{kt}$ | The solution |

### Logistic Model (BC)

| Formula | Use |
|---------|-----|
| $\frac{dP}{dt} = kP(M - P)$ | The DE |
| $P(t) = \frac{M}{1 + Be^{-kMt}}$ | The solution |
| $B = \frac{M - P_0}{P_0}$ | Initial condition constant |
| Max growth at $P = \frac{M}{2}$ | Inflection point |

---

## Common Mistakes to Avoid

### Mistake 1: Confusing $k$ with the Growth Rate Percentage

If a population grows at 5% per year, then $k = 0.05$, not $k = 5$.

The percentage is $100k$, not $k$.

---

### Mistake 2: Using the Wrong Sign for $k$

- Growth: $k > 0$ (population, investment)
- Decay: $k < 0$ (radioactive decay, cooling)

If you get a positive $k$ for a cooling problem, something went wrong.

---

### Mistake 3: Newton's Law — Forgetting the Ambient Temperature

The solution is NOT $T = T_0 e^{kt}$. That would mean the temperature approaches $0°F$, which makes no sense physically.

The correct form is $T = T_{\text{env}} + (T_0 - T_{\text{env}})e^{kt}$, which approaches $T_{\text{env}}$.

Think of it this way: your mint chocolate chip ice cream left on the counter doesn't reach absolute zero — it warms up to room temperature and stops.

---

### Mistake 4: Logistic — Maximum Growth at $P = M$

The growth rate is NOT fastest when $P = M$. At $P = M$, the growth rate is **zero** (the population has reached capacity). Maximum growth occurs at $P = \frac{M}{2}$.

---

### Mistake 5: Using Half-Life Formula for Non-Exponential Decay

The half-life formula $T_{1/2} = \frac{\ln 2}{|k|}$ only works for **exponential** decay ($\frac{dy}{dt} = ky$). If the DE is different (like logistic), you can't use this shortcut.

---

## AP Exam Tips

### For AB:
- Exponential growth/decay and Newton's Law of Cooling are heavily tested
- You must be able to set up the DE from a word problem
- Know how to find $k$ from two data points
- Practice converting between "doubling time" and "$k$" representations

### For BC (in addition to AB):
- Logistic growth is a BC-specific topic
- Know the inflection point is at $P = \frac{M}{2}$ — this is tested almost every year
- Be able to identify the carrying capacity from the DE
- Understand the S-curve shape and what it means

### Common Free Response Structure

1. "Write a DE for the situation described" → $\frac{dy}{dt} = ky$ or $\frac{dT}{dt} = k(T - T_{\text{env}})$
2. "Solve the DE with the given initial condition" → Separate and integrate
3. "Use the solution to answer a specific question" → Plug in values
4. "Interpret the result in context" → Write a sentence explaining what the math means

### Interpretation Sentences

The AP exam loves asking you to "interpret in context." Practice writing sentences like:

- "At $t = 10$ hours, the population is approximately 7,794 bacteria, meaning the colony has grown to about 15.6 times its original size."
- "The coffee will reach $100°F$ after approximately 22 minutes, meaning it takes about 22 minutes to cool to a drinkable temperature."

---

## Practice Problems

### Basic (Problems 1-5)

**1.** A population starts at 200 and grows exponentially with $k = 0.03$ per hour. Find the population after 24 hours.

---

**2.** A radioactive substance has a half-life of 10 days. If you start with 400 grams, how much remains after 25 days?

---

**3.** A quantity decays from 1000 to 600 in 8 hours. Find $k$ and the half-life.

---

**4.** An investment of $5,000 earns 4% interest compounded continuously. Find the value after 20 years.

---

**5.** A bacterial culture doubles every 3 hours. If it starts with 800 bacteria, find:
(a) The value of $k$
(b) The population after 10 hours

---

### Intermediate (Problems 6-10)

**6.** A cup of chai cools from $190°F$ to $160°F$ in 4 minutes. The room is $72°F$. Find:
(a) The cooling constant $k$
(b) The temperature after 12 minutes
(c) When the chai reaches $100°F$

---

**7.** A fossil contains 15% of its original Carbon-14 ($T_{1/2} = 5730$ years). How old is it?

---

**8.** Two substances have half-lives of 2 hours and 6 hours respectively. You start with equal amounts of each. After how many hours will the faster-decaying substance be one-quarter the amount of the slower-decaying substance?

---

**9.** The temperature of a frozen Starbucks frappe is $28°F$ when you take it out of the freezer. After 10 minutes in a $74°F$ room, it's $40°F$. When will it reach $60°F$?

---

**10.** A town's population is modeled by $P(t) = 25000e^{0.012t}$, where $t$ is years since 2020. In what year will the population reach 35,000?

---

### Advanced (Problems 11-15)

**11.** **(BC)** A rumor spreads through a school of 1,500 students according to:

$$\frac{dP}{dt} = 0.002P(1500 - P), \quad P(0) = 10$$

(a) Find $P(t)$.
(b) When is the rumor spreading fastest?
(c) How many students have heard it when the spread rate first exceeds 500 students per day?

---

**12.** **(BC)** A logistic population has $M = 800$ and $P(0) = 100$. After 5 years, $P(5) = 300$. Find the logistic model.

---

**13.** A hot BBQ brisket at $210°F$ is brought inside to a $70°F$ room. After 30 minutes it's $170°F$. Your friend arrives in 2 hours — what temperature will the brisket be?

---

**14.** **(BC)** For the logistic equation $\frac{dP}{dt} = 0.5P\left(1 - \frac{P}{100}\right)$:
(a) What is the carrying capacity?
(b) Find $\frac{d^2P}{dt^2}$ in terms of $P$.
(c) For what values of $P$ is the graph of $P(t)$ concave up?

---

**15.** Two cups of coffee are prepared at the same time: one at $200°F$ in a $68°F$ room ($k_1 = -0.08$), the other at $180°F$ in a $72°F$ room ($k_2 = -0.06$). Which one reaches $100°F$ first?

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

A population doubles every 5 years. What is the annual growth rate $k$?

| Choice | Answer |
|--------|--------|
| **(A)** | $\frac{1}{5}$ |
| **(B)** | $\frac{\ln 2}{5}$ |
| **(C)** | $\frac{2}{5}$ |
| **(D)** | $5\ln 2$ |

---

#### Problem 17 (Multiple Choice)

**(BC)** For the logistic equation $\frac{dP}{dt} = 3P - 0.01P^2$, the carrying capacity is:

| Choice | Answer |
|--------|--------|
| **(A)** | $3$ |
| **(B)** | $30$ |
| **(C)** | $300$ |
| **(D)** | $3000$ |

---

#### Problem 18 (Free Response)

A freshly baked batch of cookies is removed from the oven at $350°F$ and placed on the kitchen counter where the room temperature is $70°F$. After 10 minutes, the cookies are $250°F$.

> **(a)** Write a differential equation that models the temperature $T$ of the cookies.
>
> **(b)** Solve the DE with the initial condition $T(0) = 350$.
>
> **(c)** Find the temperature of the cookies after 30 minutes.
>
> **(d)** You want to eat the cookies when they cool to $100°F$. How long must you wait? (To the nearest minute.)

---

#### Problem 19 (Multiple Choice)

**(BC)** A population follows the logistic model with carrying capacity $M = 500$. If $P(0) = 100$, the population is growing fastest when:

| Choice | Answer |
|--------|--------|
| **(A)** | $P = 100$ |
| **(B)** | $P = 250$ |
| **(C)** | $P = 400$ |
| **(D)** | $P = 500$ |

---

#### Problem 20 (Free Response — Challenging)

You're on a road trip from San Diego to LA with Dad (you're practicing freeway driving on the I-5). You stop at a gas station and buy two drinks:
- A hot coffee at $175°F$
- A frozen slushie at $20°F$

The car's AC keeps the interior at $68°F$. Both drinks cool/warm according to Newton's Law of Cooling with the same $|k| = 0.05$ per minute.

> **(a)** Write and solve the DE for the coffee temperature $T_c(t)$ and the slushie temperature $T_s(t)$.
>
> **(b)** At what time will the coffee and slushie be the same temperature? What is that temperature?
>
> **(c)** Is this result surprising? Explain why or why not using the structure of the solution.
>
> **(d)** At $t = 20$ minutes, which drink is closer to the car's ambient temperature? How much closer?
>
> **(e)** Will either drink ever actually reach exactly $68°F$? Explain.

---

## Answer Key

<details>
<summary><strong>Problem 1 Solution</strong></summary>

$P(t) = 200e^{0.03t}$

$P(24) = 200e^{0.03 \times 24} = 200e^{0.72} = 200(2.0544) \approx 411$

$$\boxed{P(24) \approx 411}$$

</details>

---

<details>
<summary><strong>Problem 2 Solution</strong></summary>

$k = -\frac{\ln 2}{10} \approx -0.06931$

$y(t) = 400e^{kt}$

$y(25) = 400e^{-0.06931 \times 25} = 400e^{-1.7329} = 400(0.17678)$

$$\boxed{y(25) \approx 70.7 \text{ grams}}$$

Or using half-lives: 25 days = 2.5 half-lives

$400 \times \left(\frac{1}{2}\right)^{2.5} = 400 \times \frac{1}{4\sqrt{2}} = \frac{400}{5.657} \approx 70.7$ grams ✓

</details>

---

<details>
<summary><strong>Problem 3 Solution</strong></summary>

$600 = 1000e^{8k}$

$0.6 = e^{8k}$

$8k = \ln(0.6) = -0.5108$

$k = -0.06386$

Half-life: $T_{1/2} = \frac{\ln 2}{|k|} = \frac{0.6931}{0.06386} \approx 10.85$ hours

$$\boxed{k \approx -0.0639, \quad T_{1/2} \approx 10.85 \text{ hours}}$$

</details>

---

<details>
<summary><strong>Problem 4 Solution</strong></summary>

$A(t) = 5000e^{0.04t}$

$A(20) = 5000e^{0.8} = 5000(2.2255) \approx 11{,}128$

$$\boxed{A(20) \approx \$11{,}128}$$

</details>

---

<details>
<summary><strong>Problem 5 Solution</strong></summary>

**(a)** Doubling time $= 3$ hours:

$k = \frac{\ln 2}{3} \approx 0.2310$

**(b)** $P(10) = 800e^{0.2310 \times 10} = 800e^{2.310} = 800(10.074)$

$$\boxed{P(10) \approx 8{,}059 \text{ bacteria}}$$

</details>

---

<details>
<summary><strong>Problem 6 Solution</strong></summary>

$T(t) = 72 + 118e^{kt}$ (since $T_0 - T_{\text{env}} = 190 - 72 = 118$)

**(a)** $T(4) = 160$:

$160 = 72 + 118e^{4k}$

$88 = 118e^{4k}$

$e^{4k} = \frac{88}{118} = \frac{44}{59}$

$k = \frac{1}{4}\ln\left(\frac{44}{59}\right) \approx \frac{-0.2939}{4} \approx -0.07347$

**(b)** $T(12) = 72 + 118e^{12(-0.07347)} = 72 + 118e^{-0.8817} = 72 + 118(0.4137) = 72 + 48.8$

$$\boxed{T(12) \approx 120.8°F}$$

**(c)** Set $T = 100$:

$100 = 72 + 118e^{-0.07347t}$

$28 = 118e^{-0.07347t}$

$e^{-0.07347t} = \frac{28}{118}$

$t = \frac{-\ln(28/118)}{0.07347} = \frac{1.4388}{0.07347} \approx 19.6$ minutes

$$\boxed{t \approx 19.6 \text{ minutes}}$$

</details>

---

<details>
<summary><strong>Problem 7 Solution</strong></summary>

$k = -\frac{\ln 2}{5730} \approx -0.0001210$

$0.15 = e^{kt}$

$t = \frac{\ln(0.15)}{k} = \frac{-1.8971}{-0.0001210} \approx 15{,}680$ years

$$\boxed{t \approx 15{,}680 \text{ years old}}$$

</details>

---

<details>
<summary><strong>Problem 8 Solution</strong></summary>

Let $A_0$ be the starting amount of each.

Substance 1: $y_1(t) = A_0 e^{-\frac{\ln 2}{2} \cdot t}$

Substance 2: $y_2(t) = A_0 e^{-\frac{\ln 2}{6} \cdot t}$

We want $y_1 = \frac{1}{4} y_2$:

$$A_0 e^{-\frac{\ln 2}{2} t} = \frac{1}{4} A_0 e^{-\frac{\ln 2}{6} t}$$

$$e^{-\frac{\ln 2}{2} t + \frac{\ln 2}{6} t} = \frac{1}{4}$$

$$e^{-\frac{\ln 2}{3} t} = \frac{1}{4}$$

$$-\frac{\ln 2}{3} t = \ln\left(\frac{1}{4}\right) = -2\ln 2$$

$$t = \frac{3 \cdot 2\ln 2}{\ln 2} = 6$$

$$\boxed{t = 6 \text{ hours}}$$

</details>

---

<details>
<summary><strong>Problem 9 Solution</strong></summary>

$T(t) = 74 + (28 - 74)e^{kt} = 74 - 46e^{kt}$

$T(10) = 40$:

$40 = 74 - 46e^{10k}$

$-34 = -46e^{10k}$

$e^{10k} = \frac{34}{46} = \frac{17}{23}$

$k = \frac{1}{10}\ln\left(\frac{17}{23}\right) \approx -0.03016$

Set $T = 60$:

$60 = 74 - 46e^{-0.03016t}$

$-14 = -46e^{-0.03016t}$

$e^{-0.03016t} = \frac{14}{46} = \frac{7}{23}$

$t = \frac{-\ln(7/23)}{0.03016} = \frac{1.1895}{0.03016} \approx 39.4$ minutes

$$\boxed{t \approx 39.4 \text{ minutes}}$$

</details>

---

<details>
<summary><strong>Problem 10 Solution</strong></summary>

$35000 = 25000e^{0.012t}$

$\frac{7}{5} = e^{0.012t}$

$t = \frac{\ln(7/5)}{0.012} = \frac{0.3365}{0.012} \approx 28.0$ years

Year: $2020 + 28 = 2048$

$$\boxed{\text{Year } 2048}$$

</details>

---

<details>
<summary><strong>Problem 11 Solution</strong></summary>

**(a)** $M = 1500$, $P_0 = 10$, $kM = 0.002 \times 1500 = 3$

$B = \frac{1500 - 10}{10} = 149$

$$\boxed{P(t) = \frac{1500}{1 + 149e^{-3t}}}$$

**(b)** Fastest at $P = \frac{M}{2} = 750$ students.

Set $P = 750$: $750 = \frac{1500}{1 + 149e^{-3t}}$

$1 + 149e^{-3t} = 2$

$e^{-3t} = \frac{1}{149}$

$t = \frac{\ln 149}{3} \approx \frac{5.003}{3} \approx 1.67$ days

**(c)** Set $\frac{dP}{dt} = 500$:

$0.002P(1500 - P) = 500$

$P(1500 - P) = 250{,}000$

$P^2 - 1500P + 250{,}000 = 0$

$P = \frac{1500 \pm \sqrt{2{,}250{,}000 - 1{,}000{,}000}}{2} = \frac{1500 \pm \sqrt{1{,}250{,}000}}{2} = \frac{1500 \pm 1118.0}{2}$

$P \approx 191$ or $P \approx 1309$

The spread rate first exceeds 500 when $P \approx 191$ students (on the way up).

</details>

---

<details>
<summary><strong>Problem 12 Solution</strong></summary>

$M = 800$, $P_0 = 100$

$B = \frac{800 - 100}{100} = 7$

$P(t) = \frac{800}{1 + 7e^{-800kt}}$

Use $P(5) = 300$:

$300 = \frac{800}{1 + 7e^{-4000k}}$

$1 + 7e^{-4000k} = \frac{800}{300} = \frac{8}{3}$

$7e^{-4000k} = \frac{8}{3} - 1 = \frac{5}{3}$

$e^{-4000k} = \frac{5}{21}$

$k = \frac{-\ln(5/21)}{4000} = \frac{\ln(21/5)}{4000} = \frac{1.4351}{4000} \approx 0.000359$

$$\boxed{P(t) = \frac{800}{1 + 7e^{-0.2871t}}}$$

(where $kM = 800 \times 0.000359 \approx 0.2871$)

</details>

---

<details>
<summary><strong>Problem 13 Solution</strong></summary>

$T(t) = 70 + 140e^{kt}$ (since $210 - 70 = 140$)

$T(30) = 170$:

$170 = 70 + 140e^{30k}$

$100 = 140e^{30k}$

$e^{30k} = \frac{5}{7}$

$k = \frac{\ln(5/7)}{30} \approx \frac{-0.3365}{30} \approx -0.01122$

$T(120) = 70 + 140e^{120(-0.01122)} = 70 + 140e^{-1.346} = 70 + 140(0.2601) = 70 + 36.4$

$$\boxed{T(120) \approx 106°F}$$

After 2 hours, the brisket is about $106°F$ — perfect for slicing if your friend doesn't mind it on the cooler side.

</details>

---

<details>
<summary><strong>Problem 14 Solution</strong></summary>

$\frac{dP}{dt} = 0.5P\left(1 - \frac{P}{100}\right) = 0.5P - 0.005P^2$

**(a)** Carrying capacity: rewrite as $\frac{dP}{dt} = 0.005P(100 - P)$

$$M = 100$$

**(b)** $\frac{d^2P}{dt^2} = \frac{d}{dt}\left[0.5P - 0.005P^2\right] = (0.5 - 0.01P)\frac{dP}{dt}$

$$= (0.5 - 0.01P) \cdot 0.5P\left(1 - \frac{P}{100}\right)$$

**(c)** Concave up when $\frac{d^2P}{dt^2} > 0$.

Since $\frac{dP}{dt} > 0$ for $0 < P < 100$, we need $0.5 - 0.01P > 0$:

$P < 50$

$$\boxed{\text{Concave up for } 0 < P < 50 = \frac{M}{2}}$$

This confirms: the inflection point is at $P = \frac{M}{2}$.

</details>

---

<details>
<summary><strong>Problem 15 Solution</strong></summary>

**Coffee:** $T_c(t) = 68 + 132e^{-0.08t}$

Set $T_c = 100$: $32 = 132e^{-0.08t}$

$t_c = \frac{-\ln(32/132)}{0.08} = \frac{\ln(132/32)}{0.08} = \frac{1.417}{0.08} \approx 17.7$ minutes

**Other coffee:** $T_2(t) = 72 + 108e^{-0.06t}$

Set $T_2 = 100$: $28 = 108e^{-0.06t}$

$t_2 = \frac{-\ln(28/108)}{0.06} = \frac{\ln(108/28)}{0.06} = \frac{1.350}{0.06} \approx 22.5$ minutes

$$\boxed{\text{The first coffee (200°F) reaches 100°F first, at about 17.7 minutes vs. 22.5 minutes.}}$$

Even though the first coffee starts hotter, it cools faster (larger $|k|$ and bigger temperature difference), reaching $100°F$ about 5 minutes sooner.

</details>

---

<details>
<summary><strong>Problem 16 Solution</strong></summary>

**Answer: (B)** $\frac{\ln 2}{5}$

$T_d = \frac{\ln 2}{k}$ → $k = \frac{\ln 2}{T_d} = \frac{\ln 2}{5}$

</details>

---

<details>
<summary><strong>Problem 17 Solution</strong></summary>

**Answer: (C)** $300$

Rewrite: $\frac{dP}{dt} = 3P - 0.01P^2 = 0.01P(300 - P)$

This is logistic with $k = 0.01$ and $M = 300$.

</details>

---

<details>
<summary><strong>Problem 18 Solution</strong></summary>

**(a)** $\frac{dT}{dt} = k(T - 70)$, where $k < 0$

**(b)** Separate: $\frac{dT}{T - 70} = k \, dt$ → $\ln|T - 70| = kt + C$

$T = 70 + Ae^{kt}$

$T(0) = 350$: $A = 280$

$T(t) = 70 + 280e^{kt}$

Find $k$: $T(10) = 250$ → $180 = 280e^{10k}$ → $e^{10k} = \frac{9}{14}$

$k = \frac{1}{10}\ln\left(\frac{9}{14}\right) \approx -0.04418$

$$\boxed{T(t) = 70 + 280e^{-0.04418t}}$$

**(c)** $T(30) = 70 + 280e^{-0.04418 \times 30} = 70 + 280e^{-1.3254} = 70 + 280(0.2656) = 70 + 74.4$

$$\boxed{T(30) \approx 144°F}$$

**(d)** Set $T = 100$:

$30 = 280e^{-0.04418t}$

$e^{-0.04418t} = \frac{30}{280} = \frac{3}{28}$

$t = \frac{\ln(28/3)}{0.04418} = \frac{2.2336}{0.04418} \approx 50.6$ minutes

$$\boxed{t \approx 51 \text{ minutes}}$$

</details>

---

<details>
<summary><strong>Problem 19 Solution</strong></summary>

**Answer: (B)** $P = 250$

The population grows fastest at $P = \frac{M}{2} = \frac{500}{2} = 250$.

This is independent of the initial condition.

</details>

---

<details>
<summary><strong>Problem 20 Solution</strong></summary>

**(a)** Coffee: $\frac{dT_c}{dt} = -0.05(T_c - 68)$, $T_c(0) = 175$

$$T_c(t) = 68 + 107e^{-0.05t}$$

Slushie: $\frac{dT_s}{dt} = -0.05(T_s - 68)$

Wait — the slushie is *warming up*, so: $\frac{dT_s}{dt} = 0.05(68 - T_s) = -0.05(T_s - 68)$

Same equation! $T_s(0) = 20$:

$$T_s(t) = 68 + (20 - 68)e^{-0.05t} = 68 - 48e^{-0.05t}$$

**(b)** Set $T_c = T_s$:

$68 + 107e^{-0.05t} = 68 - 48e^{-0.05t}$

$107e^{-0.05t} = -48e^{-0.05t}$

$155e^{-0.05t} = 0$

$e^{-0.05t} = 0$

This never happens for finite $t$!

**The coffee and slushie never reach the same temperature at any finite time.** They both approach $68°F$ asymptotically but never actually meet.

**(c)** Not surprising when you look at the math:

$T_c - T_s = 107e^{-0.05t} - (-48e^{-0.05t}) = 155e^{-0.05t}$

The temperature difference is always $155e^{-0.05t} > 0$. The coffee is always warmer than the slushie — the gap shrinks but never closes. Both approach $68°F$, but the coffee from above and the slushie from below.

**(d)** At $t = 20$:

$T_c(20) = 68 + 107e^{-1} = 68 + 107(0.3679) = 68 + 39.37 = 107.37°F$

Distance from 68: $|107.37 - 68| = 39.37°F$

$T_s(20) = 68 - 48e^{-1} = 68 - 48(0.3679) = 68 - 17.66 = 50.34°F$

Distance from 68: $|50.34 - 68| = 17.66°F$

The slushie is closer to $68°F$ by $39.37 - 17.66 = 21.71°F$.

This makes sense: the slushie started $48°F$ away from ambient, while the coffee started $107°F$ away — more than double the gap. With the same $|k|$, the coffee has more ground to cover.

**(e)** Neither drink ever reaches exactly $68°F$. The exponential term $e^{-0.05t}$ approaches $0$ but never equals $0$ for any finite $t$. Mathematically, $T_c(t) > 68$ and $T_s(t) < 68$ for all $t$. They get infinitely close but never arrive — like an asymptote. In practice, after about an hour they'd both feel like room temperature, but technically they're always a tiny fraction of a degree off.

</details>

---

## What's Next

Congratulations — you've completed **Unit 7: Differential Equations**! You can now visualize DEs with slope fields, approximate them with Euler's Method, solve them exactly with separation of variables, and model real-world phenomena with exponential and logistic growth.

Next up: **Unit 8: Advanced Integration Techniques** (BC only), starting with [Integration by Parts](/calculus/integration-by-parts), where you'll learn a powerful method for integrating products of functions.

---

<div align="center">

[← Separable DEs](/calculus/separable-de) | [Integration by Parts →](/calculus/integration-by-parts)

</div>
