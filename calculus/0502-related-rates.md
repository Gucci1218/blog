# Related Rates
<p class="article-date">May 11, 2025</p>

When two or more quantities are connected by an equation and change over time, their rates of change are also connected. **Related rates** problems ask you to find how fast one quantity is changing when you know how fast another is changing. These problems model real scenarios: a balloon inflating, a ladder sliding, a shadow lengthening.

---

## What You'll Learn

- Set up related rates problems from word descriptions
- Identify what's changing and write relationships between quantities
- Apply implicit differentiation with respect to time
- Solve for unknown rates using given information
- Master the most common related rates scenarios
- Tackle AP Calculus related rates problems

---

## Prerequisites

- [Implicit Differentiation](/calculus/0401-implicit-differentiation) — the key technique
- [Chain Rule](/calculus/0307-chain-rule) — essential for $\frac{d}{dt}$ of functions

---

## The Core Concept

### The Big Idea

If quantities $x$ and $y$ are related by an equation and both depend on time $t$, then their rates $\frac{dx}{dt}$ and $\frac{dy}{dt}$ are also related.

**Example:** For a circle, $A = \pi r^2$. If $r$ changes over time:

$$\frac{dA}{dt} = 2\pi r \cdot \frac{dr}{dt}$$

The rate of change of area is connected to the rate of change of radius!

### The General Process

1. **Draw a diagram** (if applicable)
2. **Label variables** for quantities that change with time
3. **Write an equation** relating the variables
4. **Differentiate both sides with respect to $t$** (implicit differentiation)
5. **Substitute known values** and solve for the unknown rate
6. **Include units** in your answer

---

## Key Formulas to Know

### Geometric Formulas

**Circles:**
- Circumference: $C = 2\pi r$
- Area: $A = \pi r^2$

**Spheres:**
- Surface area: $S = 4\pi r^2$
- Volume: $V = \frac{4}{3}\pi r^3$

**Cylinders:**
- Volume: $V = \pi r^2 h$
- Surface area: $S = 2\pi r^2 + 2\pi rh$

**Cones:**
- Volume: $V = \frac{1}{3}\pi r^2 h$

**Rectangular Prisms:**
- Volume: $V = lwh$

**Right Triangles:**
- Pythagorean theorem: $a^2 + b^2 = c^2$

**Similar Triangles:**
- Ratios are equal: $\frac{a_1}{b_1} = \frac{a_2}{b_2}$

---

## Worked Examples

### Example 1: Expanding Circle

**A circle's radius is increasing at 2 cm/s. How fast is the area increasing when $r = 5$ cm?**

**Solution:**

**Step 1:** Identify what's changing.
- $r$ = radius (changing)
- $A$ = area (changing)

**Step 2:** Write the relationship.
$$A = \pi r^2$$

**Step 3:** Differentiate with respect to $t$.
$$\frac{dA}{dt} = 2\pi r \cdot \frac{dr}{dt}$$

**Step 4:** Substitute known values.
- $r = 5$ cm
- $\frac{dr}{dt} = 2$ cm/s

$$\frac{dA}{dt} = 2\pi(5)(2) = 20\pi \text{ cm}^2/\text{s}$$

**Answer:** The area is increasing at $20\pi \approx 62.8$ cm²/s.

---

### Example 2: Inflating Balloon (Sphere)

**Air is pumped into a spherical balloon at 100 cm³/s. How fast is the radius increasing when $r = 5$ cm?**

**Solution:**

**Relationship:**
$$V = \frac{4}{3}\pi r^3$$

**Differentiate:**
$$\frac{dV}{dt} = 4\pi r^2 \cdot \frac{dr}{dt}$$

**Solve for $\frac{dr}{dt}$:**
$$\frac{dr}{dt} = \frac{1}{4\pi r^2} \cdot \frac{dV}{dt}$$

**Substitute:**
$$\frac{dr}{dt} = \frac{100}{4\pi(25)} = \frac{100}{100\pi} = \frac{1}{\pi} \text{ cm/s}$$

**Answer:** The radius is increasing at $\frac{1}{\pi} \approx 0.318$ cm/s.

---

### Example 3: The Classic Ladder Problem

**A 10-foot ladder leans against a wall. The bottom slides away from the wall at 2 ft/s. How fast is the top sliding down when the bottom is 6 feet from the wall?**

**Solution:**

**Step 1:** Draw and label.
- $x$ = distance from wall to bottom of ladder
- $y$ = height of top of ladder
- Ladder length = 10 ft (constant)

**Step 2:** Write relationship (Pythagorean theorem).
$$x^2 + y^2 = 100$$

**Step 3:** Differentiate with respect to $t$.
$$2x\frac{dx}{dt} + 2y\frac{dy}{dt} = 0$$

**Step 4:** Find $y$ when $x = 6$.
$$36 + y^2 = 100 \Rightarrow y^2 = 64 \Rightarrow y = 8$$

**Step 5:** Substitute and solve.
$$2(6)(2) + 2(8)\frac{dy}{dt} = 0$$
$$24 + 16\frac{dy}{dt} = 0$$
$$\frac{dy}{dt} = -\frac{24}{16} = -\frac{3}{2} \text{ ft/s}$$

**Answer:** The top is sliding down at $\frac{3}{2}$ ft/s.

*(The negative sign indicates the height is decreasing.)*

---

### Example 4: Conical Tank (Similar Triangles)

**Water drains from a conical tank at 3 ft³/min. The tank has radius 4 ft and height 8 ft at the top. How fast is the water level dropping when the water is 4 ft deep?**

**Solution:**

**Step 1:** Set up similar triangles.

At any water level, the radius $r$ and height $h$ maintain the same ratio as the full cone:

$$\frac{r}{h} = \frac{4}{8} = \frac{1}{2}$$

So $r = \frac{h}{2}$

**Step 2:** Write volume in terms of one variable.
$$V = \frac{1}{3}\pi r^2 h = \frac{1}{3}\pi \left(\frac{h}{2}\right)^2 h = \frac{1}{3}\pi \cdot \frac{h^2}{4} \cdot h = \frac{\pi h^3}{12}$$

**Step 3:** Differentiate.
$$\frac{dV}{dt} = \frac{\pi}{12} \cdot 3h^2 \cdot \frac{dh}{dt} = \frac{\pi h^2}{4} \cdot \frac{dh}{dt}$$

**Step 4:** Substitute.
- $\frac{dV}{dt} = -3$ ft³/min (negative because draining)
- $h = 4$ ft

$$-3 = \frac{\pi(16)}{4} \cdot \frac{dh}{dt} = 4\pi \cdot \frac{dh}{dt}$$

$$\frac{dh}{dt} = -\frac{3}{4\pi} \text{ ft/min}$$

**Answer:** The water level is dropping at $\frac{3}{4\pi} \approx 0.239$ ft/min.

---

### Example 5: Shadow Problem

**A 6-foot person walks away from a 15-foot lamppost at 4 ft/s. How fast is the shadow lengthening?**

**Solution:**

**Step 1:** Draw and use similar triangles.

Let $x$ = distance from person to lamppost, $s$ = length of shadow.

By similar triangles (comparing lamppost triangle to person triangle):

$$\frac{15}{x + s} = \frac{6}{s}$$

**Step 2:** Solve for $s$ in terms of $x$.
$$15s = 6(x + s)$$
$$15s = 6x + 6s$$
$$9s = 6x$$
$$s = \frac{2x}{3}$$

**Step 3:** Differentiate.
$$\frac{ds}{dt} = \frac{2}{3} \cdot \frac{dx}{dt}$$

**Step 4:** Substitute.
$$\frac{ds}{dt} = \frac{2}{3}(4) = \frac{8}{3} \text{ ft/s}$$

**Answer:** The shadow is lengthening at $\frac{8}{3} \approx 2.67$ ft/s.

---

### Example 6: Two Cars Approaching

**Car A travels north at 60 mph. Car B travels east at 80 mph. Both approach an intersection. How fast is the distance between them decreasing when A is 3 miles south and B is 4 miles west of the intersection?**

**Solution:**

**Step 1:** Set up coordinates.
- Let $a$ = distance of Car A from intersection (decreasing)
- Let $b$ = distance of Car B from intersection (decreasing)
- Let $d$ = distance between cars

**Step 2:** Relationship (Pythagorean theorem).
$$d^2 = a^2 + b^2$$

**Step 3:** Differentiate.
$$2d\frac{dd}{dt} = 2a\frac{da}{dt} + 2b\frac{db}{dt}$$

$$d\frac{dd}{dt} = a\frac{da}{dt} + b\frac{db}{dt}$$

**Step 4:** Find $d$ and substitute.

When $a = 3$, $b = 4$: $d = \sqrt{9 + 16} = 5$

Since cars are approaching: $\frac{da}{dt} = -60$ mph, $\frac{db}{dt} = -80$ mph

$$5\frac{dd}{dt} = 3(-60) + 4(-80) = -180 - 320 = -500$$

$$\frac{dd}{dt} = -100 \text{ mph}$$

**Answer:** The distance is decreasing at 100 mph.

---

### Example 7: Filling a Trough

**A trough is 10 ft long. Its cross-section is an isosceles triangle with top width 4 ft and height 2 ft. Water fills at 2 ft³/min. How fast is the water level rising when the water is 1 ft deep?**

**Solution:**

**Step 1:** Use similar triangles for the cross-section.

At water depth $h$, the water surface width $w$ satisfies:
$$\frac{w}{h} = \frac{4}{2} = 2$$
So $w = 2h$

**Step 2:** Volume of water.
$$V = \frac{1}{2} \cdot w \cdot h \cdot 10 = \frac{1}{2}(2h)(h)(10) = 10h^2$$

**Step 3:** Differentiate.
$$\frac{dV}{dt} = 20h \cdot \frac{dh}{dt}$$

**Step 4:** Substitute.
$$2 = 20(1) \cdot \frac{dh}{dt}$$
$$\frac{dh}{dt} = \frac{2}{20} = \frac{1}{10} \text{ ft/min}$$

**Answer:** The water level is rising at $\frac{1}{10} = 0.1$ ft/min.

---

### Example 8: Angle of Elevation

**A rocket rises vertically at 500 ft/s. An observer stands 2000 ft from the launch pad. How fast is the angle of elevation changing when the rocket is 1500 ft high?**

**Solution:**

**Step 1:** Identify variables.
- $h$ = height of rocket
- $\theta$ = angle of elevation
- Distance to pad = 2000 ft (constant)

**Step 2:** Relationship.
$$\tan(\theta) = \frac{h}{2000}$$

**Step 3:** Differentiate.
$$\sec^2(\theta) \cdot \frac{d\theta}{dt} = \frac{1}{2000} \cdot \frac{dh}{dt}$$

**Step 4:** Find $\sec(\theta)$ when $h = 1500$.

$$\tan(\theta) = \frac{1500}{2000} = \frac{3}{4}$$

Using $\sec^2(\theta) = 1 + \tan^2(\theta) = 1 + \frac{9}{16} = \frac{25}{16}$

**Step 5:** Substitute.
$$\frac{25}{16} \cdot \frac{d\theta}{dt} = \frac{500}{2000} = \frac{1}{4}$$

$$\frac{d\theta}{dt} = \frac{1}{4} \cdot \frac{16}{25} = \frac{4}{25} = 0.16 \text{ rad/s}$$

**Answer:** The angle is increasing at $\frac{4}{25} = 0.16$ rad/s.

---

## Key Problem Types

### Type 1: Expanding/Contracting Shapes
- Circles, spheres, cubes
- Use area/volume formulas
- Often straightforward chain rule

### Type 2: Ladder/Sliding Problems
- Pythagorean theorem: $x^2 + y^2 = L^2$
- One quantity increasing, another decreasing

### Type 3: Conical/Cylindrical Tanks
- Similar triangles to relate $r$ and $h$
- Substitute to get volume in one variable

### Type 4: Shadow Problems
- Similar triangles are key
- Relate shadow length to person's distance

### Type 5: Distance Between Moving Objects
- Pythagorean theorem for distance
- Watch signs (approaching vs. separating)

### Type 6: Angle Problems
- Use trig relationships
- Remember: $\frac{d}{dt}[\tan\theta] = \sec^2\theta \cdot \frac{d\theta}{dt}$

---

## Common Mistakes to Avoid

### Mistake 1: Substituting Values Too Early

**Wrong:** Plugging in $r = 5$ before differentiating

**Right:** Differentiate first, then substitute values

---

### Mistake 2: Forgetting the Chain Rule

**Wrong:** $\frac{d}{dt}[r^2] = 2r$

**Right:** $\frac{d}{dt}[r^2] = 2r \cdot \frac{dr}{dt}$

---

### Mistake 3: Wrong Sign for Decreasing Quantities

If something is decreasing, its rate is negative!
- Draining water: $\frac{dV}{dt} < 0$
- Approaching car: $\frac{dx}{dt} < 0$

---

### Mistake 4: Forgetting Units

Always include units in your final answer. Related rates answers should have units like:
- ft/s, m/s (lengths per time)
- ft²/s (areas per time)
- rad/s (angles per time)

---

### Mistake 5: Not Using Similar Triangles

In cone/triangle problems, you often need to relate variables using similar triangles before differentiating.

---

## AP Exam Tips

### The Setup Is Half the Battle

- Read carefully: what's given? what's asked?
- Draw and label a diagram
- Identify which quantities are constant vs. changing

### Common Given Information

- "$\frac{dr}{dt} = 3$ ft/s" — radius increasing at 3 ft/s
- "draining at 5 ft³/min" — $\frac{dV}{dt} = -5$ ft³/min
- "at the moment when $x = 4$" — this is when to evaluate

### Show Your Work

On free response:
1. State the relationship equation
2. Show the differentiation step
3. Substitute values clearly
4. Box your final answer with units

### Speed Tips

1. Memorize common formulas (circle, sphere, cone, Pythagorean)
2. Know that similar triangles often eliminate a variable
3. Practice the ladder problem until it's automatic

---

## Practice Problems

### Basic (Problems 1-5)

**1.** A circle's radius increases at 3 cm/s. Find:

$$\frac{dA}{dt} \text{ when } r = 4 \text{ cm}$$

---

**2.** A sphere's volume increases at $10\pi$ cm³/s. Find:

$$\frac{dr}{dt} \text{ when } r = 5 \text{ cm}$$

---

**3.** A square's side length increases at 2 in/s. How fast is the area increasing when the side is 10 inches?

---

**4.** A cube's edge grows at 0.5 cm/s. Find the rate of change of volume when the edge is 8 cm.

---

**5.** For a rectangle with constant width 5 and increasing length, if $\frac{dl}{dt} = 2$, find $\frac{dA}{dt}$.

---

### Intermediate (Problems 6-10)

**6.** A 13-foot ladder leans against a wall. The bottom moves away from the wall at 3 ft/s. How fast is the top sliding down when the bottom is 5 feet from the wall?

---

**7.** A conical pile of sand has height equal to diameter. Sand is added at 5 ft³/min. How fast is the height increasing when $h = 6$ ft?

---

**8.** A person 5 ft tall walks toward a 20-ft lamppost at 3 ft/s. How fast is the person's shadow shrinking?

---

**9.** Water is pumped into a cylindrical tank (radius 3 ft) at 10 ft³/min. How fast is the water level rising?

---

**10.** Two sides of a triangle are 5 and 8, with the included angle $\theta$ increasing at 0.1 rad/s. Find the rate of change of the third side when $\theta = \frac{\pi}{3}$.

*(Hint: Law of Cosines)*

---

### Advanced (Problems 11-15)

**11.** A spotlight on the ground shines on a wall 30 ft away. A person 6 ft tall walks from the spotlight toward the wall at 4 ft/s. How fast is the shadow on the wall decreasing when the person is 10 ft from the spotlight?

---

**12.** Oil spills and spreads as a circle. The area increases at 9 m²/s. How fast is the radius increasing when $r = 3$ m?

---

**13.** A boat is pulled toward a dock by a rope through a pulley 10 ft above the water. The rope is pulled in at 2 ft/s. How fast is the boat approaching when it's 24 ft from the dock?

---

**14.** Air escapes from a spherical balloon at 2 cm³/s. How fast is the surface area decreasing when $r = 3$ cm?

---

**15.** A camera tracks a car traveling at 80 ft/s along a straight road. The camera is 50 ft from the road. Find how fast the camera must rotate when the car is 120 ft from the point on the road closest to the camera.

---

### AP Exam Practice (Problems 16-20)

---

#### Problem 16 (Multiple Choice)

A spherical balloon is inflated at a rate of $12\pi$ cubic inches per second. How fast is the radius increasing when $r = 2$ inches?

| Choice | Answer |
|--------|--------|
| **(A)** | $\frac{1}{4}$ in/s |
| **(B)** | $\frac{3}{4}$ in/s |
| **(C)** | $3$ in/s |
| **(D)** | $12$ in/s |

---

#### Problem 17 (Multiple Choice)

A 10-foot ladder slides down a wall. When the bottom is 8 feet from the wall, it's moving at 3 ft/s. How fast is the top of the ladder falling?

| Choice | Answer |
|--------|--------|
| **(A)** | $3$ ft/s |
| **(B)** | $4$ ft/s |
| **(C)** | $5$ ft/s |
| **(D)** | $6$ ft/s |

---

#### Problem 18 (Free Response)

A tank has the shape of an inverted cone with height 10 m and radius 5 m at the top. Water flows into the tank at 3 m³/min.

> **(a)** Express the volume of water in terms of the water depth $h$.
>
> **(b)** Find the rate at which the water level is rising when $h = 4$ m.
>
> **(c)** At what depth is the water level rising at 0.1 m/min?

---

#### Problem 19 (Multiple Choice)

Two cars leave an intersection at the same time. One travels north at 40 mph, the other travels east at 30 mph. How fast is the distance between them increasing after 2 hours?

| Choice | Answer |
|--------|--------|
| **(A)** | $30$ mph |
| **(B)** | $40$ mph |
| **(C)** | $50$ mph |
| **(D)** | $70$ mph |

---

#### Problem 20 (Free Response - Challenging)

A trough is 8 feet long and has a cross-section that is an isosceles trapezoid with bottom width 2 ft, top width 4 ft, and height 2 ft. Water flows in at 2 ft³/min.

> **(a)** Find the width of the water surface when the water is $h$ feet deep.
>
> **(b)** Find the volume of water when the depth is $h$ feet.
>
> **(c)** How fast is the water level rising when $h = 1$ foot?

---

## Solutions

<details>
<summary><strong>Solution 1</strong></summary>

$A = \pi r^2$

$\frac{dA}{dt} = 2\pi r \cdot \frac{dr}{dt} = 2\pi(4)(3) = 24\pi$ cm²/s

**Answer:** $24\pi$ cm²/s

</details>

---

<details>
<summary><strong>Solution 2</strong></summary>

$V = \frac{4}{3}\pi r^3$

$\frac{dV}{dt} = 4\pi r^2 \cdot \frac{dr}{dt}$

$10\pi = 4\pi(25) \cdot \frac{dr}{dt}$

$\frac{dr}{dt} = \frac{10\pi}{100\pi} = \frac{1}{10}$ cm/s

**Answer:** $\frac{1}{10}$ cm/s

</details>

---

<details>
<summary><strong>Solution 3</strong></summary>

$A = s^2$

$\frac{dA}{dt} = 2s \cdot \frac{ds}{dt} = 2(10)(2) = 40$ in²/s

**Answer:** $40$ in²/s

</details>

---

<details>
<summary><strong>Solution 4</strong></summary>

$V = s^3$

$\frac{dV}{dt} = 3s^2 \cdot \frac{ds}{dt} = 3(64)(0.5) = 96$ cm³/s

**Answer:** $96$ cm³/s

</details>

---

<details>
<summary><strong>Solution 5</strong></summary>

$A = 5l$

$\frac{dA}{dt} = 5 \cdot \frac{dl}{dt} = 5(2) = 10$ square units/s

**Answer:** $10$ square units per second

</details>

---

<details>
<summary><strong>Solution 6</strong></summary>

$x^2 + y^2 = 169$

When $x = 5$: $y = \sqrt{169 - 25} = 12$

$2x\frac{dx}{dt} + 2y\frac{dy}{dt} = 0$

$2(5)(3) + 2(12)\frac{dy}{dt} = 0$

$\frac{dy}{dt} = -\frac{30}{24} = -\frac{5}{4}$ ft/s

**Answer:** Top slides down at $\frac{5}{4}$ ft/s

</details>

---

<details>
<summary><strong>Solution 7</strong></summary>

Height = diameter, so $d = h$, thus $r = \frac{h}{2}$

$V = \frac{1}{3}\pi r^2 h = \frac{1}{3}\pi \left(\frac{h}{2}\right)^2 h = \frac{\pi h^3}{12}$

$\frac{dV}{dt} = \frac{\pi h^2}{4} \cdot \frac{dh}{dt}$

$5 = \frac{\pi(36)}{4} \cdot \frac{dh}{dt} = 9\pi \cdot \frac{dh}{dt}$

$\frac{dh}{dt} = \frac{5}{9\pi}$ ft/min

**Answer:** $\frac{5}{9\pi}$ ft/min

</details>

---

<details>
<summary><strong>Solution 8</strong></summary>

Similar triangles: $\frac{20}{x + s} = \frac{5}{s}$

$20s = 5(x + s)$
$20s = 5x + 5s$
$15s = 5x$
$s = \frac{x}{3}$

$\frac{ds}{dt} = \frac{1}{3} \cdot \frac{dx}{dt}$

Walking toward: $\frac{dx}{dt} = -3$ ft/s

$\frac{ds}{dt} = \frac{1}{3}(-3) = -1$ ft/s

**Answer:** Shadow shrinking at $1$ ft/s

</details>

---

<details>
<summary><strong>Solution 9</strong></summary>

$V = \pi r^2 h = 9\pi h$

$\frac{dV}{dt} = 9\pi \cdot \frac{dh}{dt}$

$10 = 9\pi \cdot \frac{dh}{dt}$

$\frac{dh}{dt} = \frac{10}{9\pi}$ ft/min

**Answer:** $\frac{10}{9\pi}$ ft/min

</details>

---

<details>
<summary><strong>Solution 10</strong></summary>

Law of Cosines: $c^2 = 25 + 64 - 80\cos\theta = 89 - 80\cos\theta$

$2c\frac{dc}{dt} = 80\sin\theta \cdot \frac{d\theta}{dt}$

At $\theta = \frac{\pi}{3}$: $c^2 = 89 - 80(\frac{1}{2}) = 49$, so $c = 7$

$2(7)\frac{dc}{dt} = 80 \cdot \frac{\sqrt{3}}{2} \cdot 0.1$

$14\frac{dc}{dt} = 4\sqrt{3}$

$\frac{dc}{dt} = \frac{2\sqrt{3}}{7}$

**Answer:** $\frac{2\sqrt{3}}{7}$ units/s

</details>

---

<details>
<summary><strong>Solution 11</strong></summary>

Let $x$ = distance from person to spotlight, $s$ = shadow height

Similar triangles: $\frac{s}{30} = \frac{6}{x}$, so $s = \frac{180}{x}$

$\frac{ds}{dt} = -\frac{180}{x^2} \cdot \frac{dx}{dt}$

At $x = 10$, $\frac{dx}{dt} = 4$:

$\frac{ds}{dt} = -\frac{180}{100}(4) = -7.2$ ft/s

**Answer:** Shadow decreasing at $7.2$ ft/s

</details>

---

<details>
<summary><strong>Solution 12</strong></summary>

$A = \pi r^2$

$\frac{dA}{dt} = 2\pi r \cdot \frac{dr}{dt}$

$9 = 2\pi(3) \cdot \frac{dr}{dt}$

$\frac{dr}{dt} = \frac{9}{6\pi} = \frac{3}{2\pi}$ m/s

**Answer:** $\frac{3}{2\pi}$ m/s

</details>

---

<details>
<summary><strong>Solution 13</strong></summary>

Let $x$ = horizontal distance, $r$ = rope length

$r^2 = x^2 + 100$

When $x = 24$: $r = \sqrt{576 + 100} = 26$

$2r\frac{dr}{dt} = 2x\frac{dx}{dt}$

$26(-2) = 24 \cdot \frac{dx}{dt}$

$\frac{dx}{dt} = -\frac{52}{24} = -\frac{13}{6}$ ft/s

**Answer:** Boat approaching at $\frac{13}{6}$ ft/s

</details>

---

<details>
<summary><strong>Solution 14</strong></summary>

$V = \frac{4}{3}\pi r^3$, $S = 4\pi r^2$

From $\frac{dV}{dt} = 4\pi r^2 \cdot \frac{dr}{dt}$:

$-2 = 4\pi(9) \cdot \frac{dr}{dt}$

$\frac{dr}{dt} = -\frac{2}{36\pi} = -\frac{1}{18\pi}$

$\frac{dS}{dt} = 8\pi r \cdot \frac{dr}{dt} = 8\pi(3)\left(-\frac{1}{18\pi}\right) = -\frac{24\pi}{18\pi} = -\frac{4}{3}$ cm²/s

**Answer:** Surface area decreasing at $\frac{4}{3}$ cm²/s

</details>

---

<details>
<summary><strong>Solution 15</strong></summary>

Let $x$ = distance from closest point, $\theta$ = angle

$\tan\theta = \frac{x}{50}$

$\sec^2\theta \cdot \frac{d\theta}{dt} = \frac{1}{50} \cdot \frac{dx}{dt}$

When $x = 120$: $\tan\theta = \frac{120}{50} = 2.4$

$\sec^2\theta = 1 + \tan^2\theta = 1 + 5.76 = 6.76$

$6.76 \cdot \frac{d\theta}{dt} = \frac{80}{50} = 1.6$

$\frac{d\theta}{dt} = \frac{1.6}{6.76} \approx 0.237$ rad/s

**Answer:** About $0.24$ rad/s

</details>

---

<details>
<summary><strong>Solution 16</strong></summary>

$V = \frac{4}{3}\pi r^3$

$\frac{dV}{dt} = 4\pi r^2 \cdot \frac{dr}{dt}$

$12\pi = 4\pi(4) \cdot \frac{dr}{dt}$

$\frac{dr}{dt} = \frac{12\pi}{16\pi} = \frac{3}{4}$

**Answer:** **(B)** $\frac{3}{4}$ in/s

</details>

---

<details>
<summary><strong>Solution 17</strong></summary>

$x^2 + y^2 = 100$

When $x = 8$: $y = 6$

$2x\frac{dx}{dt} + 2y\frac{dy}{dt} = 0$

$2(8)(3) + 2(6)\frac{dy}{dt} = 0$

$\frac{dy}{dt} = -\frac{48}{12} = -4$ ft/s

**Answer:** **(B)** $4$ ft/s (falling)

</details>

---

<details>
<summary><strong>Solution 18</strong></summary>

**(a)** Similar triangles: $\frac{r}{h} = \frac{5}{10} = \frac{1}{2}$, so $r = \frac{h}{2}$

$V = \frac{1}{3}\pi r^2 h = \frac{1}{3}\pi \left(\frac{h}{2}\right)^2 h = \frac{\pi h^3}{12}$

**(b)** $\frac{dV}{dt} = \frac{\pi h^2}{4} \cdot \frac{dh}{dt}$

$3 = \frac{\pi(16)}{4} \cdot \frac{dh}{dt} = 4\pi \cdot \frac{dh}{dt}$

$\frac{dh}{dt} = \frac{3}{4\pi}$ m/min

**(c)** $3 = \frac{\pi h^2}{4}(0.1)$

$h^2 = \frac{12}{0.1\pi} = \frac{120}{\pi}$

$h = \sqrt{\frac{120}{\pi}} \approx 6.18$ m

</details>

---

<details>
<summary><strong>Solution 19</strong></summary>

After 2 hours: north car at $y = 80$ mi, east car at $x = 60$ mi

$d = \sqrt{x^2 + y^2} = \sqrt{3600 + 6400} = 100$ mi

$d\frac{dd}{dt} = x\frac{dx}{dt} + y\frac{dy}{dt}$

$100 \cdot \frac{dd}{dt} = 60(30) + 80(40) = 1800 + 3200 = 5000$

$\frac{dd}{dt} = 50$ mph

**Answer:** **(C)** $50$ mph

</details>

---

<details>
<summary><strong>Solution 20</strong></summary>

**(a)** The trapezoid widens linearly. Width at depth $h$:

Bottom = 2, top = 4 at height 2. Rate of widening = $\frac{4-2}{2} = 1$ per unit height

Width at depth $h$: $w = 2 + h$

**(b)** Cross-sectional area at depth $h$: trapezoid with bases 2 and $(2 + h)$

$A = \frac{1}{2}(2 + (2 + h))h = \frac{1}{2}(4 + h)h = 2h + \frac{h^2}{2}$

Volume = $8A = 8\left(2h + \frac{h^2}{2}\right) = 16h + 4h^2$

**(c)** $\frac{dV}{dt} = 16\frac{dh}{dt} + 8h\frac{dh}{dt} = (16 + 8h)\frac{dh}{dt}$

$2 = (16 + 8)\frac{dh}{dt} = 24\frac{dh}{dt}$

$\frac{dh}{dt} = \frac{2}{24} = \frac{1}{12}$ ft/min

</details>

---

## What's Next

Now that you can solve related rates problems, you're ready for [Optimization](/calculus/0503-optimization), where you'll use derivatives to find maximum and minimum values in real-world applications.

---

<div align="center">

[← Motion](/calculus/0501-motion) | [Optimization →](/calculus/0503-optimization)

</div>
