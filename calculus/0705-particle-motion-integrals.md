# Particle Motion with Integrals
<p class="article-date">December 21, 2025</p>

## Prerequisites
Before diving in, make sure you're comfortable with:
- [Derivatives and Motion](/calculus/0501-motion)
- [Antiderivatives](/calculus/0601-antiderivatives)
- [Definite Integrals](/calculus/0603-definite-integrals)
- [Fundamental Theorem of Calculus](/calculus/0604-fundamental-theorem)

## Learning Objectives
By the end of this section, you will be able to:
- Find position from velocity using integration
- Find velocity from acceleration using integration
- Calculate displacement (net change in position)
- Calculate total distance traveled
- Solve initial value problems in motion contexts
- Interpret integral expressions in motion problems

## The Big Picture: Reversing Motion

In derivatives and motion, we learned that velocity is the derivative of position, and acceleration is the derivative of velocity:

$$v(t) = s'(t) \quad \text{and} \quad a(t) = v'(t)$$

Now we reverse the process using integrals:

$$s(t) = \int v(t) \, dt \quad \text{and} \quad v(t) = \int a(t) \, dt$$

**The Key Insight**: If derivatives tell us rates of change (how fast position changes), integrals tell us **accumulations** (how much position has changed).

## Core Concept: Displacement vs Total Distance

This is the most important distinction in motion problems with integrals:

### Displacement (Net Change in Position)
**Displacement** is the straight-line change from starting point to ending point:

$$\text{Displacement} = s(b) - s(a) = \int_a^b v(t) \, dt$$

- Can be **positive, negative, or zero**
- Measures "how far from where you started"
- Uses the signed area under the velocity curve

### Total Distance Traveled
**Total distance** is the actual path length traveled:

$$\text{Total Distance} = \int_a^b |v(t)| \, dt$$

- Always **positive or zero**
- Measures "how much ground you covered"
- Uses absolute value to count all movement as positive

> **Intuition**: If you walk 3 miles east, then 2 miles west:
> - Displacement = 1 mile east (net change)
> - Total distance = 5 miles (total walking)

## Worked Example 1: Displacement vs Total Distance

**Problem**: A particle moves along a line with velocity $v(t) = t^2 - 4t + 3$ m/s for $0 \le t \le 4$ seconds. Find the displacement and total distance traveled.

**Solution**:

**Step 1**: Find displacement using the definite integral.
$$\text{Displacement} = \int_0^4 (t^2 - 4t + 3) \, dt$$

$$= \left[\frac{t^3}{3} - 2t^2 + 3t\right]_0^4$$

$$= \left(\frac{64}{3} - 32 + 12\right) - 0 = \frac{64}{3} - 20 = \frac{64 - 60}{3} = \frac{4}{3} \text{ m}$$

**Step 2**: For total distance, find where velocity changes sign.
$$v(t) = t^2 - 4t + 3 = (t-1)(t-3) = 0$$
$$t = 1 \text{ and } t = 3$$

**Step 3**: Check the sign of velocity in each interval.
- $v(0.5) = 0.25 - 2 + 3 = 1.25 > 0$ (moving right on $[0,1]$)
- $v(2) = 4 - 8 + 3 = -1 < 0$ (moving left on $[1,3]$)
- $v(3.5) = 12.25 - 14 + 3 = 1.25 > 0$ (moving right on $[3,4]$)

**Step 4**: Calculate total distance.
$$\text{Total Distance} = \int_0^1 v(t) \, dt - \int_1^3 v(t) \, dt + \int_3^4 v(t) \, dt$$

For $[0,1]$:
$$\int_0^1 (t^2 - 4t + 3) \, dt = \left[\frac{t^3}{3} - 2t^2 + 3t\right]_0^1 = \frac{1}{3} - 2 + 3 = \frac{4}{3}$$

For $[1,3]$:
$$\int_1^3 (t^2 - 4t + 3) \, dt = \left[\frac{t^3}{3} - 2t^2 + 3t\right]_1^3 = (9 - 18 + 9) - \frac{4}{3} = -\frac{4}{3}$$

Since this is negative (particle moving left), the distance is $\frac{4}{3}$.

For $[3,4]$:
$$\int_3^4 (t^2 - 4t + 3) \, dt = \left[\frac{t^3}{3} - 2t^2 + 3t\right]_3^4 = \frac{4}{3} - 0 = \frac{4}{3}$$

**Total Distance** = $\frac{4}{3} + \frac{4}{3} + \frac{4}{3} = 4$ m

## Worked Example 2: Finding Position from Velocity (IVP)

**Problem**: A particle has velocity $v(t) = 3t^2 - 6t$ m/s and initial position $s(0) = 5$ m. Find the position function $s(t)$.

**Solution**:

**Step 1**: Integrate velocity to find position.
$$s(t) = \int v(t) \, dt = \int (3t^2 - 6t) \, dt = t^3 - 3t^2 + C$$

**Step 2**: Use the initial condition to find $C$.
$$s(0) = 0 - 0 + C = 5$$
$$C = 5$$

**Step 3**: Write the position function.
$$s(t) = t^3 - 3t^2 + 5$$

## Worked Example 3: Finding Velocity from Acceleration

**Problem**: A particle has acceleration $a(t) = 6t - 4$ m/s² with initial velocity $v(0) = 2$ m/s and initial position $s(0) = -1$ m. Find $v(t)$ and $s(t)$.

**Solution**:

**Step 1**: Integrate acceleration to find velocity.
$$v(t) = \int a(t) \, dt = \int (6t - 4) \, dt = 3t^2 - 4t + C_1$$

**Step 2**: Apply initial velocity condition.
$$v(0) = 0 - 0 + C_1 = 2 \implies C_1 = 2$$
$$v(t) = 3t^2 - 4t + 2$$

**Step 3**: Integrate velocity to find position.
$$s(t) = \int v(t) \, dt = \int (3t^2 - 4t + 2) \, dt = t^3 - 2t^2 + 2t + C_2$$

**Step 4**: Apply initial position condition.
$$s(0) = 0 - 0 + 0 + C_2 = -1 \implies C_2 = -1$$
$$s(t) = t^3 - 2t^2 + 2t - 1$$

## Worked Example 4: Using Definite Integrals for Position Change

**Problem**: A particle has velocity $v(t) = \cos(\pi t)$ m/s. If $s(0) = 2$ m, find $s(3)$.

**Solution**:

**Method 1: Using the Net Change Theorem**
$$s(3) - s(0) = \int_0^3 v(t) \, dt$$

$$s(3) = s(0) + \int_0^3 \cos(\pi t) \, dt = 2 + \left[\frac{\sin(\pi t)}{\pi}\right]_0^3$$

$$= 2 + \frac{\sin(3\pi) - \sin(0)}{\pi} = 2 + \frac{0 - 0}{\pi} = 2 \text{ m}$$

**Interpretation**: The particle oscillates back and forth, returning to its starting position!

## Key Formulas

| Concept | Formula |
|---------|---------|
| Position from velocity (indefinite) | $s(t) = \int v(t) \, dt + C$ |
| Velocity from acceleration (indefinite) | $v(t) = \int a(t) \, dt + C$ |
| Displacement | $\Delta s = \int_a^b v(t) \, dt$ |
| Total distance | $D = \int_a^b \|v(t)\| \, dt$ |
| Position at time $b$ | $s(b) = s(a) + \int_a^b v(t) \, dt$ |
| Velocity at time $b$ | $v(b) = v(a) + \int_a^b a(t) \, dt$ |

## Common Mistakes to Avoid

1. **Confusing displacement with total distance**
   - Displacement uses $\int v(t) \, dt$ (signed)
   - Total distance uses $\int |v(t)| \, dt$ (unsigned)

2. **Forgetting to find where velocity changes sign**
   - For total distance, you must split the integral at zeros of $v(t)$

3. **Dropping the constant of integration in IVPs**
   - Always write $+C$ and use initial conditions to find it

4. **Sign errors in velocity interpretation**
   - Positive $v(t)$ = moving in positive direction
   - Negative $v(t)$ = moving in negative direction
   - $v(t) = 0$ = momentarily at rest

5. **Confusing "at rest" with "at the origin"**
   - At rest: $v(t) = 0$ (not moving)
   - At origin: $s(t) = 0$ (at position zero)

## AP Exam Tips

1. **Read carefully**: "displacement" vs "distance traveled" vs "position" are all different!

2. **Calculator questions**: For total distance with complex $v(t)$:
   - Graph $v(t)$ to find zeros
   - Use $\int |v(t)| \, dt$ on your calculator

3. **Show your work**: On free response, always:
   - State what you're finding
   - Show the integral setup
   - Indicate how you handled sign changes

4. **Units matter**: Include units in your final answer (m, m/s, m/s²)

5. **Graphical problems**: If given a velocity graph:
   - Displacement = net signed area
   - Distance = total area (all positive)
   - Acceleration = slope of velocity graph

---

## Practice Problems

### Basic (Computational)

**Problem 1**
A particle has velocity $v(t) = 4t - 6$ m/s. Find the displacement from $t = 0$ to $t = 3$ seconds.

<details>
<summary>Show Solution</summary>

**Solution**:
$$\text{Displacement} = \int_0^3 (4t - 6) \, dt = \left[2t^2 - 6t\right]_0^3$$
$$= (18 - 18) - 0 = 0 \text{ m}$$

The particle ends up exactly where it started.
</details>

---

**Problem 2**
A particle has velocity $v(t) = 4t - 6$ m/s. Find the total distance traveled from $t = 0$ to $t = 3$ seconds.

<details>
<summary>Show Solution</summary>

**Solution**:
First, find where $v(t) = 0$: $4t - 6 = 0 \implies t = 1.5$

Check signs:
- $v(1) = -2 < 0$ (moving left on $[0, 1.5]$)
- $v(2) = 2 > 0$ (moving right on $[1.5, 3]$)

$$\text{Distance} = \left|\int_0^{1.5} (4t-6) \, dt\right| + \int_{1.5}^3 (4t-6) \, dt$$

$$= \left|[2t^2 - 6t]_0^{1.5}\right| + [2t^2 - 6t]_{1.5}^3$$

$$= |4.5 - 9| + |(18-18) - (4.5-9)|$$

$$= |-4.5| + |4.5| = 4.5 + 4.5 = 9 \text{ m}$$
</details>

---

**Problem 3**
A particle has acceleration $a(t) = 6t$ m/s² with $v(0) = -4$ m/s. Find $v(t)$.

<details>
<summary>Show Solution</summary>

**Solution**:
$$v(t) = \int 6t \, dt = 3t^2 + C$$

Using $v(0) = -4$:
$$-4 = 3(0)^2 + C \implies C = -4$$

$$v(t) = 3t^2 - 4 \text{ m/s}$$
</details>

---

**Problem 4**
A particle has velocity $v(t) = t^2 - 1$ m/s with $s(0) = 3$ m. Find $s(2)$.

<details>
<summary>Show Solution</summary>

**Solution**:
$$s(2) = s(0) + \int_0^2 (t^2 - 1) \, dt$$

$$= 3 + \left[\frac{t^3}{3} - t\right]_0^2$$

$$= 3 + \left(\frac{8}{3} - 2\right) - 0$$

$$= 3 + \frac{8}{3} - 2 = 1 + \frac{8}{3} = \frac{11}{3} \text{ m}$$
</details>

---

**Problem 5**
A particle has velocity $v(t) = \sin(t)$ m/s. Find the displacement from $t = 0$ to $t = \pi$.

<details>
<summary>Show Solution</summary>

**Solution**:
$$\text{Displacement} = \int_0^\pi \sin(t) \, dt = [-\cos(t)]_0^\pi$$

$$= -\cos(\pi) - (-\cos(0)) = -(-1) + 1 = 2 \text{ m}$$
</details>

---

### Intermediate (Multi-step)

**Problem 6**
A particle moves with velocity $v(t) = t^2 - 4t$ m/s for $0 \le t \le 5$.
a) Find the displacement.
b) Find the total distance traveled.

<details>
<summary>Show Solution</summary>

**Solution**:

**Part a**: Displacement
$$\int_0^5 (t^2 - 4t) \, dt = \left[\frac{t^3}{3} - 2t^2\right]_0^5 = \frac{125}{3} - 50 = \frac{125 - 150}{3} = -\frac{25}{3} \text{ m}$$

**Part b**: Total distance
Find zeros: $t^2 - 4t = t(t-4) = 0 \implies t = 0, 4$

Sign check: $v(2) = 4 - 8 = -4 < 0$ and $v(4.5) = 20.25 - 18 = 2.25 > 0$

$$\text{Distance} = \left|\int_0^4 (t^2-4t) \, dt\right| + \int_4^5 (t^2-4t) \, dt$$

$$\int_0^4 (t^2-4t) \, dt = \left[\frac{t^3}{3} - 2t^2\right]_0^4 = \frac{64}{3} - 32 = -\frac{32}{3}$$

$$\int_4^5 (t^2-4t) \, dt = \left[\frac{t^3}{3} - 2t^2\right]_4^5 = -\frac{25}{3} - \left(-\frac{32}{3}\right) = \frac{7}{3}$$

$$\text{Distance} = \frac{32}{3} + \frac{7}{3} = \frac{39}{3} = 13 \text{ m}$$
</details>

---

**Problem 7**
A particle has acceleration $a(t) = -10$ m/s² (constant), $v(0) = 20$ m/s, and $s(0) = 0$ m.
a) Find $v(t)$ and $s(t)$.
b) When does the particle reach its maximum height?
c) What is the maximum height?

<details>
<summary>Show Solution</summary>

**Solution**:

**Part a**:
$$v(t) = \int -10 \, dt = -10t + C_1$$
$$v(0) = 20 \implies C_1 = 20$$
$$v(t) = -10t + 20$$

$$s(t) = \int (-10t + 20) \, dt = -5t^2 + 20t + C_2$$
$$s(0) = 0 \implies C_2 = 0$$
$$s(t) = -5t^2 + 20t$$

**Part b**: Maximum height when $v(t) = 0$:
$$-10t + 20 = 0 \implies t = 2 \text{ seconds}$$

**Part c**:
$$s(2) = -5(4) + 20(2) = -20 + 40 = 20 \text{ m}$$
</details>

---

**Problem 8**
A particle moves with velocity $v(t) = 2\cos(t) - 1$ m/s on $[0, 2\pi]$.
a) When is the particle moving in the positive direction?
b) Find the total distance traveled.

<details>
<summary>Show Solution</summary>

**Solution**:

**Part a**: Moving in positive direction when $v(t) > 0$:
$$2\cos(t) - 1 > 0 \implies \cos(t) > \frac{1}{2}$$

On $[0, 2\pi]$: $\cos(t) > \frac{1}{2}$ when $t \in [0, \frac{\pi}{3}) \cup (\frac{5\pi}{3}, 2\pi]$

**Part b**: Sign changes at $t = \frac{\pi}{3}$ and $t = \frac{5\pi}{3}$

$$\text{Distance} = \int_0^{\pi/3} (2\cos t - 1) \, dt + \left|\int_{\pi/3}^{5\pi/3} (2\cos t - 1) \, dt\right| + \int_{5\pi/3}^{2\pi} (2\cos t - 1) \, dt$$

$$\int_0^{\pi/3} (2\cos t - 1) \, dt = [2\sin t - t]_0^{\pi/3} = \sqrt{3} - \frac{\pi}{3}$$

$$\int_{\pi/3}^{5\pi/3} (2\cos t - 1) \, dt = [2\sin t - t]_{\pi/3}^{5\pi/3} = (-\sqrt{3} - \frac{5\pi}{3}) - (\sqrt{3} - \frac{\pi}{3}) = -2\sqrt{3} - \frac{4\pi}{3}$$

$$\int_{5\pi/3}^{2\pi} (2\cos t - 1) \, dt = [2\sin t - t]_{5\pi/3}^{2\pi} = (0 - 2\pi) - (-\sqrt{3} - \frac{5\pi}{3}) = \sqrt{3} - \frac{\pi}{3}$$

$$\text{Distance} = (\sqrt{3} - \frac{\pi}{3}) + (2\sqrt{3} + \frac{4\pi}{3}) + (\sqrt{3} - \frac{\pi}{3}) = 4\sqrt{3} + \frac{2\pi}{3}$$
</details>

---

**Problem 9**
A particle starts at position $s = 2$ and moves with velocity $v(t) = e^{-t} - 0.5$ m/s.
a) Find $s(t)$.
b) As $t \to \infty$, what position does the particle approach?

<details>
<summary>Show Solution</summary>

**Solution**:

**Part a**:
$$s(t) = \int (e^{-t} - 0.5) \, dt = -e^{-t} - 0.5t + C$$

Using $s(0) = 2$:
$$2 = -e^0 - 0 + C = -1 + C \implies C = 3$$

$$s(t) = -e^{-t} - 0.5t + 3$$

**Part b**:
As $t \to \infty$: $e^{-t} \to 0$ and $-0.5t \to -\infty$

So $s(t) \to -\infty$ (the particle drifts toward $-\infty$)
</details>

---

**Problem 10**
A particle has velocity given by the graph below: a triangle with vertices at $(0, 2)$, $(3, -1)$, and $(6, 2)$ (piecewise linear).
a) Find the displacement from $t = 0$ to $t = 6$.
b) Find the total distance traveled.

<details>
<summary>Show Solution</summary>

**Solution**:

The velocity function is piecewise linear:
- From $(0, 2)$ to $(3, -1)$: line with slope $\frac{-1-2}{3-0} = -1$, so $v = 2 - t$ for $t \in [0, 3]$
- From $(3, -1)$ to $(6, 2)$: line with slope $\frac{2-(-1)}{6-3} = 1$, so $v = t - 4$ for $t \in [3, 6]$

Zeros: $v = 2 - t = 0$ at $t = 2$; $v = t - 4 = 0$ at $t = 4$

**Part a**: Using geometric areas:
- Triangle from $t = 0$ to $t = 2$: positive, area = $\frac{1}{2}(2)(2) = 2$
- Triangle from $t = 2$ to $t = 4$: negative, area = $-\frac{1}{2}(2)(1+1) = -2$
- Triangle from $t = 4$ to $t = 6$: positive, area = $\frac{1}{2}(2)(2) = 2$

Displacement = $2 - 2 + 2 = 2$ m

**Part b**: Total distance = $|2| + |-2| + |2| = 2 + 2 + 2 = 6$ m
</details>

---

### Advanced (Complex Applications)

**Problem 11**
Two particles move along the same line. Particle A has velocity $v_A(t) = 3t$ and particle B has velocity $v_B(t) = 6 - t$. At $t = 0$, particle A is at position 0 and particle B is at position 1.
a) When do they have the same velocity?
b) When do they have the same position?

<details>
<summary>Show Solution</summary>

**Solution**:

**Part a**: Same velocity when $v_A(t) = v_B(t)$:
$$3t = 6 - t \implies 4t = 6 \implies t = 1.5$$

**Part b**: Find position functions:
$$s_A(t) = \int 3t \, dt = \frac{3t^2}{2} + C_1$$
$$s_A(0) = 0 \implies C_1 = 0$$
$$s_A(t) = \frac{3t^2}{2}$$

$$s_B(t) = \int (6-t) \, dt = 6t - \frac{t^2}{2} + C_2$$
$$s_B(0) = 1 \implies C_2 = 1$$
$$s_B(t) = 6t - \frac{t^2}{2} + 1$$

Same position when $s_A(t) = s_B(t)$:
$$\frac{3t^2}{2} = 6t - \frac{t^2}{2} + 1$$
$$2t^2 = 6t + 1$$
$$2t^2 - 6t - 1 = 0$$

$$t = \frac{6 \pm \sqrt{36 + 8}}{4} = \frac{6 \pm \sqrt{44}}{4} = \frac{6 \pm 2\sqrt{11}}{4} = \frac{3 \pm \sqrt{11}}{2}$$

Since $t \ge 0$: $t = \frac{3 + \sqrt{11}}{2} \approx 3.16$ seconds
</details>

---

**Problem 12**
A particle's velocity is given by $v(t) = t \cdot e^{-t/2}$ m/s for $t \ge 0$.
a) Find the total distance traveled as $t \to \infty$.
b) Find the position function if $s(0) = 0$.

<details>
<summary>Show Solution</summary>

**Solution**:

Note: $v(t) = te^{-t/2} \ge 0$ for all $t \ge 0$, so total distance = displacement.

**Part a**:
$$\text{Distance} = \int_0^\infty te^{-t/2} \, dt$$

Using integration by parts with $u = t$, $dv = e^{-t/2}dt$:
$$= \left[-2te^{-t/2}\right]_0^\infty + 2\int_0^\infty e^{-t/2} \, dt$$

$$= 0 + 2\left[-2e^{-t/2}\right]_0^\infty = -4(0 - 1) = 4 \text{ m}$$

**Part b**:
$$s(t) = \int te^{-t/2} \, dt$$

Using integration by parts:
$$= -2te^{-t/2} - 4e^{-t/2} + C = -2e^{-t/2}(t + 2) + C$$

$s(0) = 0 \implies -2e^0(0 + 2) + C = 0 \implies -4 + C = 0 \implies C = 4$

$$s(t) = 4 - 2e^{-t/2}(t + 2)$$
</details>

---

**Problem 13**
A ball is thrown upward with initial velocity $v_0$ from height $h_0$. Acceleration due to gravity is $-g$.
a) Derive the formulas $v(t) = v_0 - gt$ and $s(t) = h_0 + v_0 t - \frac{1}{2}gt^2$.
b) Derive the formula $v^2 = v_0^2 - 2g(s - h_0)$.

<details>
<summary>Show Solution</summary>

**Solution**:

**Part a**:
From $a(t) = -g$:
$$v(t) = \int -g \, dt = -gt + C_1$$
$$v(0) = v_0 \implies C_1 = v_0$$
$$v(t) = v_0 - gt$$

$$s(t) = \int (v_0 - gt) \, dt = v_0 t - \frac{1}{2}gt^2 + C_2$$
$$s(0) = h_0 \implies C_2 = h_0$$
$$s(t) = h_0 + v_0 t - \frac{1}{2}gt^2$$

**Part b**:
From $v = v_0 - gt$, we get $t = \frac{v_0 - v}{g}$

Substitute into position equation:
$$s - h_0 = v_0 \cdot \frac{v_0 - v}{g} - \frac{1}{2}g \cdot \frac{(v_0 - v)^2}{g^2}$$

$$s - h_0 = \frac{v_0(v_0 - v)}{g} - \frac{(v_0 - v)^2}{2g}$$

$$s - h_0 = \frac{2v_0(v_0 - v) - (v_0 - v)^2}{2g} = \frac{(v_0 - v)(2v_0 - v_0 + v)}{2g} = \frac{(v_0 - v)(v_0 + v)}{2g}$$

$$s - h_0 = \frac{v_0^2 - v^2}{2g}$$

$$2g(s - h_0) = v_0^2 - v^2$$

$$v^2 = v_0^2 - 2g(s - h_0)$$
</details>

---

**Problem 14**
A car's velocity (in ft/s) at various times is given in the table:

| $t$ (s) | 0 | 2 | 4 | 6 | 8 | 10 |
|---------|---|---|---|---|---|----|
| $v(t)$ (ft/s) | 0 | 15 | 25 | 30 | 28 | 22 |

Using a trapezoidal sum, estimate the total distance traveled.

<details>
<summary>Show Solution</summary>

**Solution**:

Since all velocities are positive, total distance equals displacement.

Trapezoidal sum with $\Delta t = 2$:

$$\text{Distance} \approx \sum \frac{v(t_i) + v(t_{i+1})}{2} \cdot \Delta t$$

$$= \frac{0+15}{2}(2) + \frac{15+25}{2}(2) + \frac{25+30}{2}(2) + \frac{30+28}{2}(2) + \frac{28+22}{2}(2)$$

$$= 15 + 40 + 55 + 58 + 50 = 218 \text{ ft}$$
</details>

---

**Problem 15**
A particle oscillates with velocity $v(t) = A\sin(\omega t)$ where $A = 4$ m/s and $\omega = 2$ rad/s.
a) Find the amplitude of position oscillation (maximum displacement from equilibrium).
b) Find the total distance traveled in one complete period.

<details>
<summary>Show Solution</summary>

**Solution**:

$v(t) = 4\sin(2t)$

Period: $T = \frac{2\pi}{\omega} = \frac{2\pi}{2} = \pi$ seconds

**Part a**:
$$s(t) = \int 4\sin(2t) \, dt = -2\cos(2t) + C$$

The amplitude of $-2\cos(2t)$ is $2$ m.

**Part b**:
One complete period: $[0, \pi]$
Velocity changes sign at $2t = 0, \pi, 2\pi$, i.e., $t = 0, \frac{\pi}{2}, \pi$

$$\text{Distance} = \int_0^{\pi/2} 4\sin(2t) \, dt + \left|\int_{\pi/2}^\pi 4\sin(2t) \, dt\right|$$

$$\int_0^{\pi/2} 4\sin(2t) \, dt = [-2\cos(2t)]_0^{\pi/2} = -2\cos(\pi) + 2\cos(0) = 2 + 2 = 4$$

$$\int_{\pi/2}^\pi 4\sin(2t) \, dt = [-2\cos(2t)]_{\pi/2}^\pi = -2\cos(2\pi) + 2\cos(\pi) = -2 - 2 = -4$$

$$\text{Distance} = 4 + |-4| = 8 \text{ m}$$
</details>

---

### AP Exam Style

**Problem 16** *(Calculator Active)*
A particle moves along the x-axis with velocity $v(t) = \sin(t^2)$ for $0 \le t \le 3$.
a) Find the total distance traveled.
b) Find the acceleration at $t = 2$.

<details>
<summary>Show Solution</summary>

**Solution**:

**Part a**:
$$\text{Distance} = \int_0^3 |\sin(t^2)| \, dt \approx 1.702 \text{ (by calculator)}$$

**Part b**:
$$a(t) = v'(t) = \cos(t^2) \cdot 2t = 2t\cos(t^2)$$
$$a(2) = 4\cos(4) \approx 4(-0.6536) \approx -2.614$$
</details>

---

**Problem 17** *(Calculator Active)*
The velocity of a particle is $v(t) = t^2 e^{-t}$ for $t \ge 0$. The particle is at position $x = 3$ when $t = 0$.
a) Is the particle speeding up or slowing down at $t = 1$? Justify.
b) Find the position of the particle at $t = 5$.

<details>
<summary>Show Solution</summary>

**Solution**:

**Part a**:
$v(1) = 1 \cdot e^{-1} = \frac{1}{e} > 0$

$a(t) = v'(t) = 2te^{-t} + t^2(-e^{-t}) = e^{-t}(2t - t^2) = te^{-t}(2 - t)$

$a(1) = e^{-1}(2 - 1) = \frac{1}{e} > 0$

Since $v(1) > 0$ and $a(1) > 0$, velocity and acceleration have the same sign.

**The particle is speeding up at $t = 1$.**

**Part b**:
$$x(5) = x(0) + \int_0^5 t^2 e^{-t} \, dt = 3 + \int_0^5 t^2 e^{-t} \, dt$$

By calculator: $\int_0^5 t^2 e^{-t} \, dt \approx 1.9537$

$$x(5) \approx 3 + 1.954 = 4.954$$
</details>

---

**Problem 18** *(No Calculator)*
A particle moves along the x-axis with velocity $v(t) = 3t^2 - 12t + 9$ for $t \ge 0$.
a) For what values of $t$ is the particle at rest?
b) For what values of $t$ is the particle moving to the left?
c) Find the total distance traveled from $t = 0$ to $t = 4$.

<details>
<summary>Show Solution</summary>

**Solution**:

**Part a**: At rest when $v(t) = 0$:
$$3t^2 - 12t + 9 = 0 \implies t^2 - 4t + 3 = 0 \implies (t-1)(t-3) = 0$$
$$t = 1 \text{ and } t = 3$$

**Part b**: Moving left when $v(t) < 0$:
$v(t) = 3(t-1)(t-3) < 0$ when $(t-1)$ and $(t-3)$ have opposite signs.
This occurs when $1 < t < 3$.

**Part c**:
$$\int_0^1 (3t^2-12t+9) \, dt = [t^3 - 6t^2 + 9t]_0^1 = 1 - 6 + 9 = 4$$

$$\int_1^3 (3t^2-12t+9) \, dt = [t^3 - 6t^2 + 9t]_1^3 = (27-54+27) - 4 = -4$$

$$\int_3^4 (3t^2-12t+9) \, dt = [t^3 - 6t^2 + 9t]_3^4 = (64-96+36) - 0 = 4$$

$$\text{Total distance} = |4| + |-4| + |4| = 12$$
</details>

---

**Problem 19** *(Free Response Style)*
The graph of the velocity $v(t)$, in ft/sec, of a particle moving along the x-axis is shown. The graph consists of two line segments. At time $t = 0$, the particle is at position $x = -2$.

[Graph: Line from $(0, 4)$ to $(3, -2)$, then line from $(3, -2)$ to $(5, 2)$]

a) Find the position of the particle at $t = 3$.
b) Find the total distance traveled by the particle over the interval $0 \le t \le 5$.
c) Find the acceleration of the particle at $t = 4$.

<details>
<summary>Show Solution</summary>

**Solution**:

First, establish the velocity function:
- From $(0, 4)$ to $(3, -2)$: slope = $\frac{-2-4}{3-0} = -2$, so $v(t) = 4 - 2t$ for $0 \le t \le 3$
- From $(3, -2)$ to $(5, 2)$: slope = $\frac{2-(-2)}{5-3} = 2$, so $v(t) = -2 + 2(t-3) = 2t - 8$ for $3 \le t \le 5$

**Part a**:
$$x(3) = x(0) + \int_0^3 v(t) \, dt = -2 + \int_0^3 (4-2t) \, dt$$
$$= -2 + [4t - t^2]_0^3 = -2 + (12 - 9) = -2 + 3 = 1$$

**Part b**:
$v(t) = 4 - 2t = 0$ at $t = 2$ (on first segment)
$v(t) = 2t - 8 = 0$ at $t = 4$ (on second segment)

Distance from geometric areas:
- $[0, 2]$: Triangle with base 2 and height 4: Area = $\frac{1}{2}(2)(4) = 4$
- $[2, 3]$: Triangle with base 1 and height 2: Area = $\frac{1}{2}(1)(2) = 1$ (below axis)
- $[3, 4]$: Triangle with base 1 and height 2: Area = $\frac{1}{2}(1)(2) = 1$ (below axis)
- $[4, 5]$: Triangle with base 1 and height 2: Area = $\frac{1}{2}(1)(2) = 1$

Total distance = $4 + 1 + 1 + 1 = 7$ ft

**Part c**:
For $3 < t < 5$, $v(t) = 2t - 8$, so $a(t) = 2$ ft/s²

At $t = 4$: $a(4) = 2$ ft/s²
</details>

---

**Problem 20** *(Free Response Style)*
A particle moves along the y-axis so that its velocity at time $t$ is given by $v(t) = t\cos(t^2)$.
At time $t = 0$, the particle is at $y = 1$.

a) Find the acceleration of the particle at time $t = 2$.
b) Is the speed of the particle increasing or decreasing at time $t = 2$? Give a reason for your answer.
c) Find the position of the particle at time $t = 2$.
d) Find the total distance traveled by the particle from time $t = 0$ to $t = 2$.

<details>
<summary>Show Solution</summary>

**Solution**:

**Part a**:
$$a(t) = v'(t) = \cos(t^2) + t \cdot (-\sin(t^2)) \cdot 2t = \cos(t^2) - 2t^2\sin(t^2)$$

$$a(2) = \cos(4) - 8\sin(4) \approx -0.654 - 8(-0.757) \approx -0.654 + 6.056 \approx 5.402$$

**Part b**:
$v(2) = 2\cos(4) \approx 2(-0.654) \approx -1.307 < 0$
$a(2) \approx 5.402 > 0$

Since velocity is negative and acceleration is positive, they have opposite signs.
**The speed is decreasing at $t = 2$.**

**Part c**:
$$y(2) = y(0) + \int_0^2 t\cos(t^2) \, dt$$

Let $u = t^2$, $du = 2t \, dt$:
$$\int t\cos(t^2) \, dt = \frac{1}{2}\int \cos(u) \, du = \frac{1}{2}\sin(u) = \frac{1}{2}\sin(t^2)$$

$$y(2) = 1 + \left[\frac{1}{2}\sin(t^2)\right]_0^2 = 1 + \frac{1}{2}\sin(4) - 0 = 1 + \frac{1}{2}(-0.757) \approx 0.621$$

**Part d**:
$v(t) = t\cos(t^2) = 0$ when $t = 0$ or $\cos(t^2) = 0$

$\cos(t^2) = 0$ when $t^2 = \frac{\pi}{2}, \frac{3\pi}{2}, ...$

$t = \sqrt{\frac{\pi}{2}} \approx 1.253$ is in $[0, 2]$

$$\text{Distance} = \left|\int_0^{\sqrt{\pi/2}} t\cos(t^2) \, dt\right| + \left|\int_{\sqrt{\pi/2}}^2 t\cos(t^2) \, dt\right|$$

$$= \left|\frac{1}{2}\sin(t^2)\right|_0^{\sqrt{\pi/2}} + \left|\frac{1}{2}\sin(t^2)\right|_{\sqrt{\pi/2}}^2$$

$$= \left|\frac{1}{2}\sin(\frac{\pi}{2}) - 0\right| + \left|\frac{1}{2}\sin(4) - \frac{1}{2}\sin(\frac{\pi}{2})\right|$$

$$= \frac{1}{2} + \left|-0.379 - 0.5\right| = 0.5 + 0.879 = 1.379$$
</details>

---

## What's Next

Congratulations! You've completed Unit 6 on Integral Applications. These techniques for analyzing motion using integrals are essential for the AP exam. Next, explore [Differential Equations](/calculus/differential-equations) to begin Unit 7, where you'll learn to solve equations involving derivatives.

<div align="center">
[← Average Value](/calculus/0704-average-value) | [Differential Equations →](/calculus/differential-equations)
</div>
