# Parametric Derivatives
<p class="article-date">April 23, 2026</p>

*Picture a drone flying over Torrey Pines on a sunny San Diego afternoon. You're standing below, tracking it with your phone. At any moment, you can describe where the drone is by two separate numbers: how far east it is and how far north it is — both changing with time. That's a parametric curve. The drone's path isn't described by a single $y = f(x)$ equation. Instead, both $x$ and $y$ are controlled by a hidden puppeteer: the parameter $t$. Now here's the question that launches this entire article — if the drone is sweeping through the sky along some curved path, how do you find the slope of that path at any instant? You can't just take $\frac{dy}{dx}$ directly, because neither $x$ nor $y$ is written in terms of the other. You need parametric derivatives.*

---

## What You'll Learn
- Understand what parametric equations are and why we use them
- Compute the first derivative $\frac{dy}{dx}$ from parametric equations using $\frac{dy/dt}{dx/dt}$
- Compute the second derivative $\frac{d^2y}{dx^2}$ correctly (the formula is tricky!)
- Find equations of tangent lines to parametric curves
- Identify horizontal tangents ($dy/dt = 0$) and vertical tangents ($dx/dt = 0$)
- Calculate speed and arc length for parametric curves
- Work with common parametric curves: circles, ellipses, cycloids
- Connect parametric derivatives to particle motion problems
- Compute area under parametric curves
- Solve AP Calculus BC exam problems involving parametric derivatives

---

## Prerequisites
- [Derivative Definition](/calculus/0301-derivative-definition)
- [Chain Rule](/calculus/0307-chain-rule)
- [Tangent Lines](/calculus/0303-tangent-lines)

---

## The Core Concept

### Intuition First

Think about K-pop choreography. When you're learning a dance routine, every move you make on stage can be described by two things: your left-right position and your forward-backward position. Both change with time as you hit each beat. At beat 1, you might be at position $(2, 3)$ on the stage grid. At beat 2, you're at $(5, 1)$. At beat 3, you're at $(4, 6)$.

Your position at time $t$ is:
$$x = f(t) \quad \text{(left-right)} \qquad y = g(t) \quad \text{(forward-backward)}$$

If you traced your path on the floor, you'd get a curve. But this curve isn't described by "$y$ equals something in terms of $x$." It's described by *both* $x$ and $y$ being functions of time.

Now suppose someone asks: "At beat 2, what direction are you moving?" That's a slope question. But you can't just differentiate $y$ with respect to $x$ because you don't have $y$ written as a function of $x$. What you *do* know is:
- How fast your left-right position is changing: $\frac{dx}{dt}$
- How fast your forward-backward position is changing: $\frac{dy}{dt}$

The slope of your path is the ratio of how fast you're moving vertically to how fast you're moving horizontally:

$$\text{slope} = \frac{\text{vertical speed}}{\text{horizontal speed}} = \frac{dy/dt}{dx/dt}$$

That's the entire core idea. The chain rule makes it rigorous.

### The Formal Definition

Given parametric equations $x = f(t)$ and $y = g(t)$, where both $f$ and $g$ are differentiable:

**First Derivative:**

By the chain rule, $\frac{dy}{dt} = \frac{dy}{dx} \cdot \frac{dx}{dt}$. Solving for $\frac{dy}{dx}$:

$$\boxed{\frac{dy}{dx} = \frac{dy/dt}{dx/dt} = \frac{y'(t)}{x'(t)}, \quad \text{provided } x'(t) \neq 0}$$

**Second Derivative:**

This is where students get tripped up on the AP exam. The second derivative is *not* $\frac{d^2y/dt^2}{d^2x/dt^2}$. That's the most common mistake in this entire unit.

The correct formula comes from differentiating $\frac{dy}{dx}$ with respect to $x$ — but since everything is in terms of $t$, we use the chain rule again:

$$\frac{d^2y}{dx^2} = \frac{d}{dx}\left(\frac{dy}{dx}\right) = \frac{\frac{d}{dt}\left(\frac{dy}{dx}\right)}{\frac{dx}{dt}}$$

$$\boxed{\frac{d^2y}{dx^2} = \frac{\frac{d}{dt}\left[\frac{dy}{dx}\right]}{\frac{dx}{dt}}}$$

In words: take the derivative of the first derivative *with respect to $t$*, then divide by $\frac{dx}{dt}$.

### Horizontal and Vertical Tangents

- **Horizontal tangent:** $\frac{dy}{dt} = 0$ and $\frac{dx}{dt} \neq 0$ (numerator is zero, denominator isn't)
- **Vertical tangent:** $\frac{dx}{dt} = 0$ and $\frac{dy}{dt} \neq 0$ (denominator is zero, numerator isn't)
- If both $\frac{dy}{dt} = 0$ and $\frac{dx}{dt} = 0$ at the same time, the behavior is indeterminate — you'd need L'Hopital's Rule or further analysis.

### Speed and Arc Length

If a particle moves along a parametric curve, its **speed** at time $t$ is:

$$\boxed{\text{speed} = \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2}}$$

This is the magnitude of the velocity vector $\left\langle \frac{dx}{dt}, \frac{dy}{dt}\right\rangle$.

The **arc length** of the curve from $t = a$ to $t = b$ is:

$$\boxed{L = \int_a^b \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2} \, dt}$$

Notice this is just the integral of speed over time — total distance traveled. Think of it like a road trip along the Pacific Coast Highway: speed times time gives distance.

### Area Under a Parametric Curve

If a parametric curve traces out a path from left to right (meaning $x$ is increasing), the area between the curve and the $x$-axis is:

$$\boxed{A = \int_a^b y(t) \cdot x'(t) \, dt}$$

This comes from substituting $y = g(t)$ and $dx = x'(t)\,dt$ into $\int y \, dx$.

---

## Worked Examples

### Example 1: First Derivative — The Basics

**Find $\frac{dy}{dx}$ for** $x = t^2$, $y = t^3$.

**Step 1:** Compute the derivatives with respect to $t$:

$$\frac{dx}{dt} = 2t, \qquad \frac{dy}{dt} = 3t^2$$

**Step 2:** Apply the formula:

$$\frac{dy}{dx} = \frac{dy/dt}{dx/dt} = \frac{3t^2}{2t} = \boxed{\frac{3t}{2}}$$

**Interpretation:** At $t = 1$, the slope is $\frac{3}{2}$. At $t = 2$, the slope is $3$. The curve gets steeper as $t$ increases.

**Sanity check:** We can eliminate the parameter: from $x = t^2$, we get $t = \sqrt{x}$, so $y = t^3 = x^{3/2}$. Then $\frac{dy}{dx} = \frac{3}{2}x^{1/2} = \frac{3}{2}\sqrt{x} = \frac{3}{2}\sqrt{t^2} = \frac{3t}{2}$. It matches!

---

### Example 2: First Derivative with Trig

**Find $\frac{dy}{dx}$ for** $x = \cos t$, $y = \sin t$.

This parametrizes the unit circle (counterclockwise, starting at $(1, 0)$).

$$\frac{dx}{dt} = -\sin t, \qquad \frac{dy}{dt} = \cos t$$

$$\frac{dy}{dx} = \frac{\cos t}{-\sin t} = \boxed{-\cot t}$$

**Check at $t = \frac{\pi}{4}$:** The point is $\left(\frac{\sqrt{2}}{2}, \frac{\sqrt{2}}{2}\right)$, which is on the circle in the first quadrant. The slope should be $-1$ (tangent to a circle at 45 degrees). Indeed, $-\cot\frac{\pi}{4} = -1$. $\checkmark$

---

### Example 3: Tangent Line to a Parametric Curve

**Find the equation of the tangent line at $t = 1$ for** $x = t^2 + 1$, $y = t^3 - t$.

**Step 1:** Find the point. At $t = 1$:
$$x = 1 + 1 = 2, \qquad y = 1 - 1 = 0$$

The point is $(2, 0)$.

**Step 2:** Find the slope.
$$\frac{dx}{dt} = 2t \implies 2(1) = 2$$
$$\frac{dy}{dt} = 3t^2 - 1 \implies 3(1) - 1 = 2$$

$$\frac{dy}{dx}\bigg|_{t=1} = \frac{2}{2} = 1$$

**Step 3:** Write the tangent line equation using point-slope form:
$$y - 0 = 1(x - 2)$$

$$\boxed{y = x - 2}$$

Think of it this way: if a Robotics team drone is at position $(2, 0)$ at time $t = 1$, and it's heading in a direction with slope $1$, then the line $y = x - 2$ is the direction it would continue if it suddenly stopped turning.

---

### Example 4: Horizontal and Vertical Tangents

**Find all horizontal and vertical tangents for** $x = t^3 - 3t$, $y = t^2 - 4$.

**Step 1:** Compute derivatives.
$$\frac{dx}{dt} = 3t^2 - 3 = 3(t^2 - 1) = 3(t - 1)(t + 1)$$
$$\frac{dy}{dt} = 2t$$

**Horizontal tangents** occur when $\frac{dy}{dt} = 0$ and $\frac{dx}{dt} \neq 0$:

$2t = 0 \implies t = 0$

Check: $\frac{dx}{dt}\big|_{t=0} = -3 \neq 0$. $\checkmark$

At $t = 0$: $x = 0$, $y = -4$. **Horizontal tangent at $(0, -4)$.**

**Vertical tangents** occur when $\frac{dx}{dt} = 0$ and $\frac{dy}{dt} \neq 0$:

$3(t-1)(t+1) = 0 \implies t = 1$ or $t = -1$

At $t = 1$: $\frac{dy}{dt} = 2 \neq 0$ $\checkmark$. Point: $x = 1 - 3 = -2$, $y = 1 - 4 = -3$. **Vertical tangent at $(-2, -3)$.**

At $t = -1$: $\frac{dy}{dt} = -2 \neq 0$ $\checkmark$. Point: $x = -1 + 3 = 2$, $y = 1 - 4 = -3$. **Vertical tangent at $(2, -3)$.**

---

### Example 5: The Second Derivative (The Tricky One!)

**Find $\frac{d^2y}{dx^2}$ for** $x = t^2$, $y = t^3$.

**Step 1:** From Example 1, we already know $\frac{dy}{dx} = \frac{3t}{2}$.

**Step 2:** Differentiate $\frac{dy}{dx}$ with respect to $t$:

$$\frac{d}{dt}\left(\frac{3t}{2}\right) = \frac{3}{2}$$

**Step 3:** Divide by $\frac{dx}{dt} = 2t$:

$$\frac{d^2y}{dx^2} = \frac{3/2}{2t} = \boxed{\frac{3}{4t}}$$

**Check:** We showed $y = x^{3/2}$, so $\frac{dy}{dx} = \frac{3}{2}x^{1/2}$ and $\frac{d^2y}{dx^2} = \frac{3}{4}x^{-1/2} = \frac{3}{4\sqrt{x}} = \frac{3}{4\sqrt{t^2}} = \frac{3}{4|t|}$. For $t > 0$, this is $\frac{3}{4t}$. $\checkmark$

---

### Example 6: Second Derivative with Trig — Ellipse

**For the ellipse** $x = 3\cos t$, $y = 2\sin t$, **find $\frac{d^2y}{dx^2}$.**

Imagine this ellipse as the oval track your Robotics robot follows around a table.

**Step 1:** First derivative.
$$\frac{dx}{dt} = -3\sin t, \qquad \frac{dy}{dt} = 2\cos t$$
$$\frac{dy}{dx} = \frac{2\cos t}{-3\sin t} = -\frac{2}{3}\cot t$$

**Step 2:** Differentiate with respect to $t$:
$$\frac{d}{dt}\left(-\frac{2}{3}\cot t\right) = -\frac{2}{3}(-\csc^2 t) = \frac{2}{3}\csc^2 t$$

**Step 3:** Divide by $\frac{dx}{dt} = -3\sin t$:
$$\frac{d^2y}{dx^2} = \frac{\frac{2}{3}\csc^2 t}{-3\sin t} = \frac{2}{3} \cdot \frac{1}{\sin^2 t} \cdot \frac{1}{-3\sin t} = \frac{2}{-9\sin^3 t}$$

$$\boxed{\frac{d^2y}{dx^2} = -\frac{2}{9\sin^3 t}}$$

At $t = \frac{\pi}{2}$ (top of the ellipse, point $(0, 2)$): $\frac{d^2y}{dx^2} = -\frac{2}{9(1)^3} = -\frac{2}{9}$, which is negative — the curve is concave down at the top, as expected for an ellipse.

---

### Example 7: Speed and Arc Length

**A particle moves along** $x = 3t$, $y = 4t^2$ **for $0 \leq t \leq 2$. Find the speed at $t = 1$ and the total arc length.**

Picture yourself driving with Dad along Sunset Cliffs Boulevard. Your east-west position and north-south position both change with time — and you want to know how fast you're actually moving and how far you travel.

**Speed:**
$$\frac{dx}{dt} = 3, \qquad \frac{dy}{dt} = 8t$$

$$\text{speed} = \sqrt{3^2 + (8t)^2} = \sqrt{9 + 64t^2}$$

At $t = 1$: $\text{speed} = \sqrt{9 + 64} = \sqrt{73} \approx 8.54$

**Arc length:**
$$L = \int_0^2 \sqrt{9 + 64t^2}\,dt$$

Let $u = 8t$, so $du = 8\,dt$ and $dt = \frac{du}{8}$. When $t = 0$, $u = 0$; when $t = 2$, $u = 16$.

$$L = \int_0^{16} \sqrt{9 + u^2} \cdot \frac{du}{8} = \frac{1}{8}\int_0^{16}\sqrt{9 + u^2}\,du$$

Using the formula $\int \sqrt{a^2 + u^2}\,du = \frac{u}{2}\sqrt{a^2 + u^2} + \frac{a^2}{2}\ln\left|u + \sqrt{a^2 + u^2}\right| + C$ with $a = 3$:

$$= \frac{1}{8}\left[\frac{u}{2}\sqrt{9 + u^2} + \frac{9}{2}\ln\left|u + \sqrt{9 + u^2}\right|\right]_0^{16}$$

$$= \frac{1}{8}\left[\frac{16}{2}\sqrt{265} + \frac{9}{2}\ln\left(16 + \sqrt{265}\right) - 0 - \frac{9}{2}\ln 3\right]$$

$$= \frac{1}{8}\left[8\sqrt{265} + \frac{9}{2}\ln\left(\frac{16 + \sqrt{265}}{3}\right)\right]$$

$$\boxed{L = \sqrt{265} + \frac{9}{16}\ln\left(\frac{16 + \sqrt{265}}{3}\right) \approx 17.56}$$

On the AP exam, arc length integrals are often set up but left unevaluated, or evaluated with a calculator.

---

### Example 8: The Cycloid — A Classic Parametric Curve

**A cycloid is defined by** $x = t - \sin t$, $y = 1 - \cos t$. **Find $\frac{dy}{dx}$ and $\frac{d^2y}{dx^2}$.**

A cycloid is the curve traced by a point on the rim of a rolling wheel — like watching a reflector on a bicycle tire as someone rides along Coronado Beach.

**First derivative:**
$$\frac{dx}{dt} = 1 - \cos t, \qquad \frac{dy}{dt} = \sin t$$

$$\frac{dy}{dx} = \frac{\sin t}{1 - \cos t}$$

We can simplify using the identity $\frac{\sin t}{1 - \cos t} = \cot\frac{t}{2}$:

$$\frac{dy}{dx} = \cot\frac{t}{2}$$

**Second derivative:**

$$\frac{d}{dt}\left(\cot\frac{t}{2}\right) = -\csc^2\frac{t}{2} \cdot \frac{1}{2} = -\frac{1}{2}\csc^2\frac{t}{2}$$

$$\frac{d^2y}{dx^2} = \frac{-\frac{1}{2}\csc^2\frac{t}{2}}{1 - \cos t}$$

Using $1 - \cos t = 2\sin^2\frac{t}{2}$:

$$= \frac{-\frac{1}{2}\csc^2\frac{t}{2}}{2\sin^2\frac{t}{2}} = \frac{-1}{4\sin^4\frac{t}{2}} \cdot \frac{1}{\sin^{-2}\frac{t}{2}} \cdot \frac{1}{\sin^{2}\frac{t}{2}}$$

Let's redo this more carefully:

$$\frac{d^2y}{dx^2} = \frac{-\frac{1}{2} \cdot \frac{1}{\sin^2(t/2)}}{2\sin^2(t/2)} = \frac{-1}{4\sin^4(t/2)}$$

$$\boxed{\frac{d^2y}{dx^2} = -\frac{1}{4\sin^4(t/2)}}$$

Since $\sin^4(t/2) > 0$ (when $t \neq 2k\pi$), the second derivative is always negative between cusps. The cycloid is always concave down between the points where it touches the ground.

---

### Example 9: Area Under a Parametric Curve

**Find the area under one arch of the cycloid** $x = t - \sin t$, $y = 1 - \cos t$, **from $t = 0$ to $t = 2\pi$.**

$$A = \int_0^{2\pi} y(t) \cdot x'(t)\,dt = \int_0^{2\pi}(1 - \cos t)(1 - \cos t)\,dt = \int_0^{2\pi}(1 - \cos t)^2\,dt$$

Expand:

$$= \int_0^{2\pi}\left(1 - 2\cos t + \cos^2 t\right)dt$$

Use $\cos^2 t = \frac{1 + \cos 2t}{2}$:

$$= \int_0^{2\pi}\left(1 - 2\cos t + \frac{1}{2} + \frac{\cos 2t}{2}\right)dt$$

$$= \int_0^{2\pi}\left(\frac{3}{2} - 2\cos t + \frac{\cos 2t}{2}\right)dt$$

$$= \left[\frac{3}{2}t - 2\sin t + \frac{\sin 2t}{4}\right]_0^{2\pi}$$

$$= \frac{3}{2}(2\pi) - 0 + 0 - 0 = \boxed{3\pi}$$

The area under one arch of a cycloid is exactly $3\pi r^2$ (here $r = 1$) — three times the area of the generating circle. This beautiful result was discovered by several mathematicians in the 17th century.

---

## Key Formulas & Rules

| Formula | Expression | When to Use |
|---------|-----------|-------------|
| First derivative | $\dfrac{dy}{dx} = \dfrac{dy/dt}{dx/dt}$ | Finding slope of a parametric curve |
| Second derivative | $\dfrac{d^2y}{dx^2} = \dfrac{\frac{d}{dt}\left[\frac{dy}{dx}\right]}{\frac{dx}{dt}}$ | Concavity of parametric curves |
| Horizontal tangent | $\dfrac{dy}{dt} = 0$, $\dfrac{dx}{dt} \neq 0$ | Finding where the curve is flat |
| Vertical tangent | $\dfrac{dx}{dt} = 0$, $\dfrac{dy}{dt} \neq 0$ | Finding where the curve is vertical |
| Speed | $\sqrt{\left(\dfrac{dx}{dt}\right)^2 + \left(\dfrac{dy}{dt}\right)^2}$ | Particle motion problems |
| Arc length | $\displaystyle\int_a^b \sqrt{\left(\dfrac{dx}{dt}\right)^2 + \left(\dfrac{dy}{dt}\right)^2}\,dt$ | Total distance along a parametric curve |
| Area | $\displaystyle\int_a^b y(t) \cdot x'(t)\,dt$ | Area under a parametric curve |
| Distance traveled | $\displaystyle\int_a^b \text{speed}\,dt$ | Total distance (same as arc length) |

---

## Common Mistakes to Avoid

**1. Wrong second derivative formula**

> **Wrong:** $\dfrac{d^2y}{dx^2} = \dfrac{d^2y/dt^2}{d^2x/dt^2} = \dfrac{y''(t)}{x''(t)}$
>
> **Right:** $\dfrac{d^2y}{dx^2} = \dfrac{\frac{d}{dt}\left[\frac{dy}{dx}\right]}{\frac{dx}{dt}}$

This is the single most common error on parametric questions. The second derivative is NOT the ratio of the second derivatives with respect to $t$. You must differentiate the *first derivative* $\frac{dy}{dx}$ with respect to $t$, then divide by $\frac{dx}{dt}$.

**2. Confusing horizontal and vertical tangent conditions**

> **Wrong:** Horizontal tangent when $\frac{dx}{dt} = 0$
>
> **Right:** Horizontal tangent when $\frac{dy}{dt} = 0$ (and $\frac{dx}{dt} \neq 0$)

Remember: horizontal means the *numerator* of $\frac{dy}{dx}$ is zero. Vertical means the *denominator* is zero.

**3. Forgetting to check the other derivative at tangent points**

> **Wrong:** "$\frac{dy}{dt} = 0$ at $t = 2$, so there's a horizontal tangent."
>
> **Right:** "$\frac{dy}{dt} = 0$ at $t = 2$. Check: $\frac{dx}{dt}\big|_{t=2} = 5 \neq 0$. So yes, horizontal tangent."

If both derivatives are zero simultaneously, you can't conclude anything without further analysis.

**4. Confusing speed with velocity**

> **Wrong:** Speed $= \frac{dx}{dt}$ or speed $= \frac{dy}{dt}$
>
> **Right:** Speed $= \sqrt{(dx/dt)^2 + (dy/dt)^2}$

Speed is the *magnitude* of the velocity vector. It's always non-negative. It's like driving on the I-5 — your speedometer shows $|\vec{v}|$, not just the north-south or east-west component.

**5. Getting the arc length integrand wrong**

> **Wrong:** $L = \int_a^b \sqrt{1 + \left(\frac{dy}{dx}\right)^2}\,dx$ (this is the rectangular formula!)
>
> **Right:** $L = \int_a^b \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2}\,dt$ (parametric formula, integrate with respect to $t$)

Make sure the variable of integration matches your setup. For parametric curves, everything should be in terms of $t$.

**6. Not simplifying $\frac{dy}{dx}$ before computing the second derivative**

> **Wrong:** Plugging a messy unsimplified expression for $\frac{dy}{dx}$ into the second derivative formula.
>
> **Right:** Simplify $\frac{dy}{dx}$ first, *then* differentiate with respect to $t$.

Simplifying first makes the calculus cleaner and reduces the chance of algebraic errors.

---

## AP Exam Tips

1. **The second derivative is the #1 tested concept** in the parametric unit. The College Board loves testing whether you know the correct formula. Expect at least one MC or FR question where the wrong answer is $\frac{y''(t)}{x''(t)}$.

2. **Set up, don't always solve.** Many arc length integrals on the AP exam are meant to be set up, not evaluated by hand. If the problem says "set up an integral," write the full integral with limits and integrand, then stop.

3. **Calculator-active sections** may ask you to evaluate arc length or speed numerically. Know how to enter $\int_a^b \sqrt{(x'(t))^2 + (y'(t))^2}\,dt$ into your calculator.

4. **Particle motion + parametric = common combo.** A particle moves in the $xy$-plane with position $(x(t), y(t))$. The velocity vector is $\langle x'(t), y'(t)\rangle$. Speed is the magnitude. The slope of the path is $\frac{y'(t)}{x'(t)}$.

5. **Know your tangent conditions cold.** "At what time is the particle moving horizontally?" means $y'(t) = 0$ (and $x'(t) \neq 0$). "Vertically?" means $x'(t) = 0$ (and $y'(t) \neq 0$).

6. **Free response scoring:** On FR questions, showing the formula before plugging in values earns method points even if your arithmetic is wrong. Always write $\frac{dy}{dx} = \frac{dy/dt}{dx/dt}$ before substituting.

7. **Connect to distance vs. displacement.** Total distance traveled is $\int_a^b \text{speed}\,dt$ (always positive). Displacement in the $x$-direction is $\int_a^b x'(t)\,dt = x(b) - x(a)$. These are different things.

8. **BC-specific:** Parametric derivatives appear only on the BC exam. They're typically worth 1-2 MC questions and part of one FR question, often combined with arc length or particle motion.

---

## Practice Problems

### Basic (1-5)

**Problem 1.** Given $x = 2t + 1$, $y = t^2 - 3$, find $\frac{dy}{dx}$.

**Problem 2.** Given $x = e^t$, $y = e^{2t}$, find $\frac{dy}{dx}$ and simplify.

**Problem 3.** Given $x = t^2$, $y = t^3 + t$, find the slope of the tangent line at $t = 2$.

**Problem 4.** Given $x = 5\cos t$, $y = 5\sin t$, find all values of $t$ in $[0, 2\pi)$ where the tangent is horizontal.

**Problem 5.** A particle moves with position $x = 4t$, $y = 3t$ for $t \geq 0$. Find the speed of the particle.

### Intermediate (6-10)

**Problem 6.** Given $x = t^2 - 2t$, $y = t^3 - 3t$, find all points where the tangent line is horizontal and all points where it is vertical.

**Problem 7.** Given $x = \cos t$, $y = \sin(2t)$, find $\frac{dy}{dx}$ and evaluate it at $t = \frac{\pi}{6}$.

**Problem 8.** Given $x = t - \sin t$, $y = 1 - \cos t$, find the equation of the tangent line at $t = \frac{\pi}{2}$.

**Problem 9.** Given $x = t^2$, $y = t^3$, find $\frac{d^2y}{dx^2}$ using the correct parametric formula.

**Problem 10.** A particle moves along $x = 2\cos t$, $y = 3\sin t$ for $0 \leq t \leq \pi$. Set up (but do not evaluate) an integral for the arc length of this path.

### Advanced (11-15)

**Problem 11.** Given $x = e^t\cos t$, $y = e^t\sin t$, find $\frac{dy}{dx}$ at $t = \frac{\pi}{4}$.

**Problem 12.** For the curve $x = t^3 - 3t$, $y = t^4 - 2t^2$, find $\frac{d^2y}{dx^2}$ at $t = 1$.

**Problem 13.** A particle moves in the $xy$-plane with position $(x(t), y(t))$ where $x(t) = t^2 - 4t$ and $y(t) = \frac{1}{2}t^3 - 3t$ for $0 \leq t \leq 5$. Find the speed of the particle at $t = 2$ and determine whether the particle is speeding up or slowing down at that instant.

**Problem 14.** Find the total arc length of the curve $x = \cos^3 t$, $y = \sin^3 t$ for $0 \leq t \leq 2\pi$. (This is an astroid.)

**Problem 15.** Given $x = 3t^2$, $y = 2t^3$, find the area enclosed between the curve and the $x$-axis from $t = 0$ to $t = 2$ and back (assume the curve returns along the $x$-axis). Actually, compute $\int_0^2 y(t)\,x'(t)\,dt$.

### AP Exam Practice (16-20)

**Problem 16.** A particle moves in the $xy$-plane so that at time $t \geq 0$, its position is given by $x(t) = 3t^2 - 6t$ and $y(t) = t^3 - 6t$. At what time $t$ is the particle moving to the left?

| Choice | Answer |
|--------|--------|
| (A) | $0 < t < 1$ only |
| (B) | $0 < t < 2$ only |
| (C) | $0 < t < 1$ and $t > 2$ |
| (D) | $t > 2$ only |

**Problem 17.** A curve in the $xy$-plane is defined by $x = 2t + \sin t$ and $y = t^2 + \cos t$. What is $\frac{d^2y}{dx^2}$ at $t = 0$?

| Choice | Answer |
|--------|--------|
| (A) | $-\frac{1}{9}$ |
| (B) | $\frac{1}{9}$ |
| (C) | $\frac{1}{3}$ |
| (D) | $1$ |

**Problem 18.** A particle moves in the $xy$-plane so that its position at time $t$ is $(x(t), y(t)) = (t^2 - t, 2\sqrt{t})$ for $t > 0$. What is the speed of the particle at $t = 4$?

| Choice | Answer |
|--------|--------|
| (A) | $\frac{\sqrt{197}}{2}$ |
| (B) | $\sqrt{50}$ |
| (C) | $7.5$ |
| (D) | $\frac{\sqrt{197}}{4}$ |

**Problem 19.** (Free Response) A drone flies over Balboa Park. Its position at time $t$ seconds ($0 \leq t \leq 10$) is given by:
$$x(t) = 2t + \sin(\pi t), \qquad y(t) = t^2 - 3t + 5$$

> (a) Find the slope of the drone's path at $t = 1$.
>
> (b) Find all times $t$ in $(0, 10)$ when the drone is moving purely horizontally (i.e., the slope of its path is zero).
>
> (c) Is the path of the drone concave up or concave down at $t = 2$? Justify your answer.
>
> (d) Set up, but do not evaluate, an integral that gives the total distance the drone travels from $t = 0$ to $t = 5$.

**Problem 20.** (Free Response) A BBQ food truck drives through San Diego. At time $t$ hours, for $0 \leq t \leq 6$, the truck's position in miles is:
$$x(t) = t^3 - 9t, \qquad y(t) = t^2 - 4$$

> (a) At what time(s) does the truck have a vertical tangent to its path? Find the coordinates.
>
> (b) Find the equation of the tangent line to the truck's path at $t = 3$.
>
> (c) Find $\frac{d^2y}{dx^2}$ at $t = 3$. Is the path concave up or concave down at this point?
>
> (d) Find the speed of the truck at $t = 2$. Then find the total distance traveled by the truck from $t = 0$ to $t = 3$ using a calculator (set up the exact integral and give a decimal approximation).

---

## Answer Key

<details>
<summary><strong>Problem 1 Solution</strong></summary>

**Find $\frac{dy}{dx}$ for** $x = 2t + 1$, $y = t^2 - 3$.

$$\frac{dx}{dt} = 2, \qquad \frac{dy}{dt} = 2t$$

$$\frac{dy}{dx} = \frac{dy/dt}{dx/dt} = \frac{2t}{2} = \boxed{t}$$

</details>

---

<details>
<summary><strong>Problem 2 Solution</strong></summary>

**Find $\frac{dy}{dx}$ for** $x = e^t$, $y = e^{2t}$.

$$\frac{dx}{dt} = e^t, \qquad \frac{dy}{dt} = 2e^{2t}$$

$$\frac{dy}{dx} = \frac{2e^{2t}}{e^t} = 2e^t$$

$$\boxed{\frac{dy}{dx} = 2e^t}$$

**Verification:** Eliminating the parameter, $x = e^t \implies t = \ln x$, so $y = e^{2t} = (e^t)^2 = x^2$. Then $\frac{dy}{dx} = 2x = 2e^t$. $\checkmark$

</details>

---

<details>
<summary><strong>Problem 3 Solution</strong></summary>

**Find the slope at $t = 2$ for** $x = t^2$, $y = t^3 + t$.

$$\frac{dx}{dt} = 2t, \qquad \frac{dy}{dt} = 3t^2 + 1$$

$$\frac{dy}{dx} = \frac{3t^2 + 1}{2t}$$

At $t = 2$:

$$\frac{dy}{dx}\bigg|_{t=2} = \frac{3(4) + 1}{2(2)} = \frac{13}{4}$$

$$\boxed{\frac{dy}{dx}\bigg|_{t=2} = \frac{13}{4}}$$

</details>

---

<details>
<summary><strong>Problem 4 Solution</strong></summary>

**Find horizontal tangents for** $x = 5\cos t$, $y = 5\sin t$ **on $[0, 2\pi)$.**

Horizontal tangents occur when $\frac{dy}{dt} = 0$ and $\frac{dx}{dt} \neq 0$.

$$\frac{dy}{dt} = 5\cos t = 0 \implies \cos t = 0 \implies t = \frac{\pi}{2}, \frac{3\pi}{2}$$

Check that $\frac{dx}{dt} = -5\sin t \neq 0$ at these values:

- At $t = \frac{\pi}{2}$: $\frac{dx}{dt} = -5\sin\frac{\pi}{2} = -5 \neq 0$ $\checkmark$
- At $t = \frac{3\pi}{2}$: $\frac{dx}{dt} = -5\sin\frac{3\pi}{2} = 5 \neq 0$ $\checkmark$

$$\boxed{t = \frac{\pi}{2} \text{ and } t = \frac{3\pi}{2}}$$

These correspond to the points $(0, 5)$ (top of the circle) and $(0, -5)$ (bottom of the circle), which makes geometric sense.

</details>

---

<details>
<summary><strong>Problem 5 Solution</strong></summary>

**Find the speed for** $x = 4t$, $y = 3t$.

$$\frac{dx}{dt} = 4, \qquad \frac{dy}{dt} = 3$$

$$\text{speed} = \sqrt{4^2 + 3^2} = \sqrt{16 + 9} = \sqrt{25} = \boxed{5}$$

The speed is constant at 5. The particle moves in a straight line (slope $= \frac{3}{4}$) at a constant rate. It's like driving on a straight highway at a steady 5 units per second.

</details>

---

<details>
<summary><strong>Problem 6 Solution</strong></summary>

**Find horizontal and vertical tangent points for** $x = t^2 - 2t$, $y = t^3 - 3t$.

$$\frac{dx}{dt} = 2t - 2 = 2(t - 1), \qquad \frac{dy}{dt} = 3t^2 - 3 = 3(t - 1)(t + 1)$$

**Horizontal tangents** ($\frac{dy}{dt} = 0$, $\frac{dx}{dt} \neq 0$):

$3(t-1)(t+1) = 0 \implies t = 1$ or $t = -1$.

- At $t = 1$: $\frac{dx}{dt} = 2(0) = 0$. Both derivatives are zero! This is **not** a simple horizontal tangent — it's an indeterminate case. We skip this.
- At $t = -1$: $\frac{dx}{dt} = 2(-2) = -4 \neq 0$. $\checkmark$

At $t = -1$: $x = 1 + 2 = 3$, $y = -1 + 3 = 2$.

**Horizontal tangent at $(3, 2)$.**

**Vertical tangents** ($\frac{dx}{dt} = 0$, $\frac{dy}{dt} \neq 0$):

$2(t-1) = 0 \implies t = 1$.

At $t = 1$: $\frac{dy}{dt} = 3(0)(2) = 0$. Both derivatives are zero again! This is the same indeterminate point.

Since both derivatives vanish at $t = 1$, we need further analysis. We can compute $\lim_{t \to 1} \frac{dy/dt}{dx/dt} = \lim_{t \to 1}\frac{3(t-1)(t+1)}{2(t-1)} = \lim_{t \to 1}\frac{3(t+1)}{2} = \frac{6}{2} = 3$.

So the curve has a well-defined tangent at $t = 1$ with slope 3, but it is neither horizontal nor vertical.

At $t = 1$: $x = 1 - 2 = -1$, $y = 1 - 3 = -2$. Point $(-1, -2)$ with slope 3.

$$\boxed{\text{Horizontal tangent at } (3, 2); \text{ no vertical tangent}}$$

</details>

---

<details>
<summary><strong>Problem 7 Solution</strong></summary>

**Find $\frac{dy}{dx}$ for** $x = \cos t$, $y = \sin(2t)$ **and evaluate at $t = \frac{\pi}{6}$.**

$$\frac{dx}{dt} = -\sin t, \qquad \frac{dy}{dt} = 2\cos(2t)$$

$$\frac{dy}{dx} = \frac{2\cos(2t)}{-\sin t} = -\frac{2\cos(2t)}{\sin t}$$

At $t = \frac{\pi}{6}$:

$$\cos\frac{\pi}{3} = \frac{1}{2}, \qquad \sin\frac{\pi}{6} = \frac{1}{2}$$

$$\frac{dy}{dx}\bigg|_{t=\pi/6} = -\frac{2 \cdot \frac{1}{2}}{\frac{1}{2}} = -\frac{1}{1/2} = \boxed{-2}$$

</details>

---

<details>
<summary><strong>Problem 8 Solution</strong></summary>

**Find the tangent line at $t = \frac{\pi}{2}$ for** $x = t - \sin t$, $y = 1 - \cos t$.

**Step 1: Find the point.**

At $t = \frac{\pi}{2}$:
$$x = \frac{\pi}{2} - \sin\frac{\pi}{2} = \frac{\pi}{2} - 1$$
$$y = 1 - \cos\frac{\pi}{2} = 1 - 0 = 1$$

Point: $\left(\frac{\pi}{2} - 1, 1\right)$

**Step 2: Find the slope.**

$$\frac{dx}{dt} = 1 - \cos t \implies 1 - \cos\frac{\pi}{2} = 1 - 0 = 1$$

$$\frac{dy}{dt} = \sin t \implies \sin\frac{\pi}{2} = 1$$

$$\frac{dy}{dx}\bigg|_{t=\pi/2} = \frac{1}{1} = 1$$

**Step 3: Write the tangent line.**

$$y - 1 = 1\left(x - \left(\frac{\pi}{2} - 1\right)\right)$$

$$\boxed{y = x - \frac{\pi}{2} + 2}$$

</details>

---

<details>
<summary><strong>Problem 9 Solution</strong></summary>

**Find $\frac{d^2y}{dx^2}$ for** $x = t^2$, $y = t^3$.

**Step 1:** Find the first derivative.

$$\frac{dx}{dt} = 2t, \qquad \frac{dy}{dt} = 3t^2$$

$$\frac{dy}{dx} = \frac{3t^2}{2t} = \frac{3t}{2}$$

**Step 2:** Differentiate $\frac{dy}{dx}$ with respect to $t$:

$$\frac{d}{dt}\left(\frac{3t}{2}\right) = \frac{3}{2}$$

**Step 3:** Divide by $\frac{dx}{dt}$:

$$\frac{d^2y}{dx^2} = \frac{3/2}{2t} = \boxed{\frac{3}{4t}}$$

**Common wrong answer:** $\frac{d^2y/dt^2}{d^2x/dt^2} = \frac{6t}{2} = 3t$. This is INCORRECT. Don't fall for it!

</details>

---

<details>
<summary><strong>Problem 10 Solution</strong></summary>

**Set up the arc length integral for** $x = 2\cos t$, $y = 3\sin t$, $0 \leq t \leq \pi$.

$$\frac{dx}{dt} = -2\sin t, \qquad \frac{dy}{dt} = 3\cos t$$

$$\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2 = 4\sin^2 t + 9\cos^2 t$$

We can simplify: $4\sin^2 t + 9\cos^2 t = 4\sin^2 t + 4\cos^2 t + 5\cos^2 t = 4 + 5\cos^2 t$.

$$\boxed{L = \int_0^{\pi} \sqrt{4 + 5\cos^2 t}\,dt}$$

This is an elliptic integral — it cannot be evaluated in closed form with elementary functions. On the AP exam, you'd either leave it in this form or use a calculator to approximate it ($L \approx 7.933$).

</details>

---

<details>
<summary><strong>Problem 11 Solution</strong></summary>

**Find $\frac{dy}{dx}$ at $t = \frac{\pi}{4}$ for** $x = e^t\cos t$, $y = e^t\sin t$.

Use the product rule for each derivative:

$$\frac{dx}{dt} = e^t\cos t + e^t(-\sin t) = e^t(\cos t - \sin t)$$

$$\frac{dy}{dt} = e^t\sin t + e^t\cos t = e^t(\sin t + \cos t)$$

$$\frac{dy}{dx} = \frac{e^t(\sin t + \cos t)}{e^t(\cos t - \sin t)} = \frac{\sin t + \cos t}{\cos t - \sin t}$$

At $t = \frac{\pi}{4}$:

$$\sin\frac{\pi}{4} = \cos\frac{\pi}{4} = \frac{\sqrt{2}}{2}$$

$$\frac{dy}{dx}\bigg|_{t=\pi/4} = \frac{\frac{\sqrt{2}}{2} + \frac{\sqrt{2}}{2}}{\frac{\sqrt{2}}{2} - \frac{\sqrt{2}}{2}} = \frac{\sqrt{2}}{0}$$

The denominator is zero and the numerator is nonzero, so the tangent is **vertical**.

$$\boxed{\frac{dy}{dx} \text{ is undefined — vertical tangent at } t = \frac{\pi}{4}}$$

The point is $\left(e^{\pi/4} \cdot \frac{\sqrt{2}}{2}, \, e^{\pi/4} \cdot \frac{\sqrt{2}}{2}\right)$.

</details>

---

<details>
<summary><strong>Problem 12 Solution</strong></summary>

**Find $\frac{d^2y}{dx^2}$ at $t = 1$ for** $x = t^3 - 3t$, $y = t^4 - 2t^2$.

**Step 1:** First derivative.

$$\frac{dx}{dt} = 3t^2 - 3, \qquad \frac{dy}{dt} = 4t^3 - 4t$$

$$\frac{dy}{dx} = \frac{4t^3 - 4t}{3t^2 - 3} = \frac{4t(t^2 - 1)}{3(t^2 - 1)} = \frac{4t}{3} \quad \text{(for } t \neq \pm 1\text{)}$$

**Step 2:** Differentiate $\frac{dy}{dx} = \frac{4t}{3}$ with respect to $t$:

$$\frac{d}{dt}\left(\frac{4t}{3}\right) = \frac{4}{3}$$

**Step 3:** Divide by $\frac{dx}{dt} = 3t^2 - 3$.

At $t = 1$: $\frac{dx}{dt} = 3(1) - 3 = 0$.

Since $\frac{dx}{dt} = 0$ at $t = 1$, we cannot directly compute $\frac{d^2y}{dx^2}$ at $t = 1$ using the simplified form. Let's go back to the unsimplified first derivative and use L'Hopital's Rule to find $\frac{dy}{dx}$ at $t = 1$:

$$\frac{dy}{dx}\bigg|_{t=1} = \lim_{t \to 1}\frac{4t^3 - 4t}{3t^2 - 3} = \lim_{t \to 1}\frac{4t(t-1)(t+1)}{3(t-1)(t+1)} = \frac{4}{3}$$

Now for the second derivative, we need $\frac{d}{dx}\left(\frac{dy}{dx}\right)$ near $t = 1$. Using the unsimplified $\frac{dy}{dx}$, we already showed it simplifies to $\frac{4t}{3}$ near $t = 1$ (after cancellation). Since $\frac{d}{dt}\left(\frac{4t}{3}\right) = \frac{4}{3}$ and $\frac{dx}{dt} = 3(t^2 - 1) \to 0$ as $t \to 1$:

$$\frac{d^2y}{dx^2}\bigg|_{t=1} = \lim_{t \to 1}\frac{4/3}{3(t^2-1)}$$

This limit does not exist (it diverges), which means the curve has a cusp or unusual behavior at $t = 1$.

Let's verify: at $t = 1$, $x = 1 - 3 = -2$, $y = 1 - 2 = -1$. Both $\frac{dx}{dt}$ and $\frac{dy}{dt}$ are zero, indicating the particle momentarily stops. The second derivative is:

$$\boxed{\frac{d^2y}{dx^2} \text{ is undefined at } t = 1}$$

The curve has a cusp at $(-2, -1)$ where the particle reverses direction.

</details>

---

<details>
<summary><strong>Problem 13 Solution</strong></summary>

**Speed at $t = 2$ and speeding up/slowing down for** $x(t) = t^2 - 4t$, $y(t) = \frac{1}{2}t^3 - 3t$.

**Velocity components:**

$$x'(t) = 2t - 4, \qquad y'(t) = \frac{3}{2}t^2 - 3$$

At $t = 2$:

$$x'(2) = 4 - 4 = 0, \qquad y'(2) = \frac{3}{2}(4) - 3 = 6 - 3 = 3$$

**Speed at $t = 2$:**

$$\text{speed} = \sqrt{0^2 + 3^2} = \sqrt{9} = \boxed{3}$$

**Is the particle speeding up or slowing down?**

We need $\frac{d}{dt}(\text{speed})$ at $t = 2$.

$$\text{speed}(t) = \sqrt{(2t-4)^2 + \left(\frac{3}{2}t^2 - 3\right)^2}$$

Let's compute $\frac{d}{dt}[\text{speed}^2] = \frac{d}{dt}\left[(2t-4)^2 + \left(\frac{3t^2}{2} - 3\right)^2\right]$

Since $\frac{d}{dt}[\text{speed}^2] = 2 \cdot \text{speed} \cdot \frac{d}{dt}[\text{speed}]$, we get:

$$\frac{d}{dt}[\text{speed}] = \frac{1}{2\cdot\text{speed}} \cdot \frac{d}{dt}[\text{speed}^2]$$

Compute $\frac{d}{dt}[\text{speed}^2]$:

$$= 2(2t-4)(2) + 2\left(\frac{3t^2}{2} - 3\right)(3t)$$

At $t = 2$:

$$= 2(0)(2) + 2(3)(6) = 0 + 36 = 36$$

$$\frac{d}{dt}[\text{speed}]\bigg|_{t=2} = \frac{36}{2(3)} = \frac{36}{6} = 6 > 0$$

Since $\frac{d}{dt}[\text{speed}] > 0$, the particle is **speeding up** at $t = 2$.

$$\boxed{\text{Speed} = 3; \text{ the particle is speeding up.}}$$

</details>

---

<details>
<summary><strong>Problem 14 Solution</strong></summary>

**Arc length of the astroid** $x = \cos^3 t$, $y = \sin^3 t$ **for $0 \leq t \leq 2\pi$.**

**Step 1:** Compute derivatives.

$$\frac{dx}{dt} = 3\cos^2 t(-\sin t) = -3\cos^2 t\sin t$$

$$\frac{dy}{dt} = 3\sin^2 t(\cos t) = 3\sin^2 t\cos t$$

**Step 2:** Compute the speed squared.

$$\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2 = 9\cos^4 t\sin^2 t + 9\sin^4 t\cos^2 t$$

$$= 9\cos^2 t\sin^2 t(\cos^2 t + \sin^2 t) = 9\cos^2 t\sin^2 t$$

**Step 3:** Speed.

$$\sqrt{9\cos^2 t\sin^2 t} = 3|\cos t\sin t| = \frac{3}{2}|\sin 2t|$$

**Step 4:** Arc length.

$$L = \int_0^{2\pi}\frac{3}{2}|\sin 2t|\,dt$$

By symmetry, $|\sin 2t|$ has period $\frac{\pi}{2}$, and the integral over one period $[0, \pi/2]$ is $\int_0^{\pi/2}\sin 2t\,dt = \left[-\frac{\cos 2t}{2}\right]_0^{\pi/2} = \frac{1}{2} + \frac{1}{2} = 1$.

There are 4 such periods in $[0, 2\pi]$:

$$L = \frac{3}{2} \cdot 4 \cdot 1 = \boxed{6}$$

</details>

---

<details>
<summary><strong>Problem 15 Solution</strong></summary>

**Compute** $\displaystyle\int_0^2 y(t)\,x'(t)\,dt$ **for** $x = 3t^2$, $y = 2t^3$.

$$x'(t) = 6t$$

$$\int_0^2 y(t)\cdot x'(t)\,dt = \int_0^2 2t^3 \cdot 6t\,dt = \int_0^2 12t^4\,dt$$

$$= 12\left[\frac{t^5}{5}\right]_0^2 = 12 \cdot \frac{32}{5} = \frac{384}{5}$$

$$\boxed{\int_0^2 y(t)\,x'(t)\,dt = \frac{384}{5} = 76.8}$$

</details>

---

<details>
<summary><strong>Problem 16 Solution</strong></summary>

**When is the particle moving to the left?**

A particle moves to the left when $x'(t) < 0$.

$$x(t) = 3t^2 - 6t \implies x'(t) = 6t - 6 = 6(t - 1)$$

$x'(t) < 0$ when $t - 1 < 0$, i.e., $t < 1$.

Since we need $t \geq 0$, the particle moves to the left for $0 < t < 1$.

At $t = 1$, $x'(1) = 0$ (momentarily stopped horizontally). For $t > 1$, $x'(t) > 0$ (moving right).

$\boxed{\text{(A)} \quad 0 < t < 1 \text{ only}}$

</details>

---

<details>
<summary><strong>Problem 17 Solution</strong></summary>

**Find $\frac{d^2y}{dx^2}$ at $t = 0$ for** $x = 2t + \sin t$, $y = t^2 + \cos t$.

**Step 1:** First derivative.

$$\frac{dx}{dt} = 2 + \cos t, \qquad \frac{dy}{dt} = 2t - \sin t$$

$$\frac{dy}{dx} = \frac{2t - \sin t}{2 + \cos t}$$

At $t = 0$: $\frac{dy}{dx} = \frac{0 - 0}{2 + 1} = 0$.

**Step 2:** Differentiate $\frac{dy}{dx}$ with respect to $t$ using the quotient rule.

$$\frac{d}{dt}\left(\frac{2t - \sin t}{2 + \cos t}\right) = \frac{(2 - \cos t)(2 + \cos t) - (2t - \sin t)(-\sin t)}{(2 + \cos t)^2}$$

At $t = 0$:

Numerator: $(2 - 1)(2 + 1) - (0)(0) = (1)(3) - 0 = 3$

Denominator: $(2 + 1)^2 = 9$

$$\frac{d}{dt}\left(\frac{dy}{dx}\right)\bigg|_{t=0} = \frac{3}{9} = \frac{1}{3}$$

**Step 3:** Divide by $\frac{dx}{dt}\big|_{t=0} = 2 + \cos 0 = 3$:

$$\frac{d^2y}{dx^2}\bigg|_{t=0} = \frac{1/3}{3} = \frac{1}{9}$$

$\boxed{\text{(B)} \quad \frac{1}{9}}$

</details>

---

<details>
<summary><strong>Problem 18 Solution</strong></summary>

**Find the speed at $t = 4$ for** $(x(t), y(t)) = (t^2 - t, \, 2\sqrt{t})$.

**Step 1:** Compute velocity components.

$$x'(t) = 2t - 1, \qquad y'(t) = 2 \cdot \frac{1}{2\sqrt{t}} = \frac{1}{\sqrt{t}}$$

At $t = 4$:

$$x'(4) = 8 - 1 = 7, \qquad y'(4) = \frac{1}{\sqrt{4}} = \frac{1}{2}$$

**Step 2:** Speed.

$$\text{speed} = \sqrt{7^2 + \left(\frac{1}{2}\right)^2} = \sqrt{49 + \frac{1}{4}} = \sqrt{\frac{197}{4}} = \frac{\sqrt{197}}{2}$$

$\boxed{\text{(A)} \quad \frac{\sqrt{197}}{2}}$

</details>

---

<details>
<summary><strong>Problem 19 Solution</strong></summary>

**Drone over Balboa Park:** $x(t) = 2t + \sin(\pi t)$, $y(t) = t^2 - 3t + 5$, $0 \leq t \leq 10$.

**(a) Slope at $t = 1$.**

$$x'(t) = 2 + \pi\cos(\pi t), \qquad y'(t) = 2t - 3$$

At $t = 1$:

$$x'(1) = 2 + \pi\cos\pi = 2 + \pi(-1) = 2 - \pi$$

$$y'(1) = 2(1) - 3 = -1$$

$$\frac{dy}{dx}\bigg|_{t=1} = \frac{-1}{2 - \pi}$$

Since $2 - \pi < 0$:

$$= \frac{-1}{2 - \pi} = \frac{1}{\pi - 2}$$

$$\boxed{\text{Slope at } t = 1: \frac{1}{\pi - 2} \approx 0.876}$$

**(b) When is the drone moving horizontally?**

The slope is zero when $y'(t) = 0$ (and $x'(t) \neq 0$):

$$2t - 3 = 0 \implies t = \frac{3}{2}$$

Check: $x'(3/2) = 2 + \pi\cos\frac{3\pi}{2} = 2 + \pi(0) = 2 \neq 0$. $\checkmark$

$$\boxed{t = \frac{3}{2}}$$

This is the only time in $(0, 10)$ when the path is horizontal.

**(c) Concavity at $t = 2$.**

**Step 1:** First derivative:

$$\frac{dy}{dx} = \frac{2t - 3}{2 + \pi\cos(\pi t)}$$

**Step 2:** Differentiate with respect to $t$ using the quotient rule.

Let $u = 2t - 3$ and $v = 2 + \pi\cos(\pi t)$.

$u' = 2$, $v' = -\pi^2\sin(\pi t)$.

$$\frac{d}{dt}\left[\frac{dy}{dx}\right] = \frac{u'v - uv'}{v^2} = \frac{2(2 + \pi\cos\pi t) - (2t-3)(-\pi^2\sin\pi t)}{(2 + \pi\cos\pi t)^2}$$

At $t = 2$: $\cos(2\pi) = 1$, $\sin(2\pi) = 0$, $u = 1$, $v = 2 + \pi$.

$$\frac{d}{dt}\left[\frac{dy}{dx}\right]\bigg|_{t=2} = \frac{2(2 + \pi) - (1)(0)}{(2 + \pi)^2} = \frac{2(2 + \pi)}{(2 + \pi)^2} = \frac{2}{2 + \pi}$$

**Step 3:** Divide by $x'(2) = 2 + \pi\cos(2\pi) = 2 + \pi$:

$$\frac{d^2y}{dx^2}\bigg|_{t=2} = \frac{2/(2+\pi)}{2 + \pi} = \frac{2}{(2 + \pi)^2}$$

Since $\frac{2}{(2+\pi)^2} > 0$, the path is **concave up** at $t = 2$.

$$\boxed{\frac{d^2y}{dx^2}\bigg|_{t=2} = \frac{2}{(2+\pi)^2} \approx 0.076 > 0 \implies \text{concave up}}$$

**(d) Total distance from $t = 0$ to $t = 5$.**

$$x'(t) = 2 + \pi\cos(\pi t), \qquad y'(t) = 2t - 3$$

$$\boxed{D = \int_0^5 \sqrt{\left(2 + \pi\cos(\pi t)\right)^2 + (2t - 3)^2}\,dt}$$

</details>

---

<details>
<summary><strong>Problem 20 Solution</strong></summary>

**BBQ food truck:** $x(t) = t^3 - 9t$, $y(t) = t^2 - 4$, $0 \leq t \leq 6$.

**(a) Vertical tangents.**

Vertical tangents occur when $x'(t) = 0$ and $y'(t) \neq 0$.

$$x'(t) = 3t^2 - 9 = 3(t^2 - 3) = 0 \implies t = \sqrt{3} \approx 1.732$$

(We discard $t = -\sqrt{3}$ since $t \geq 0$.)

Check: $y'(\sqrt{3}) = 2\sqrt{3} \neq 0$. $\checkmark$

Coordinates at $t = \sqrt{3}$:

$$x = (\sqrt{3})^3 - 9\sqrt{3} = 3\sqrt{3} - 9\sqrt{3} = -6\sqrt{3}$$

$$y = 3 - 4 = -1$$

$$\boxed{\text{Vertical tangent at } t = \sqrt{3}, \text{ point } (-6\sqrt{3}, -1)}$$

**(b) Tangent line at $t = 3$.**

**Point:** $x = 27 - 27 = 0$, $y = 9 - 4 = 5$. Point: $(0, 5)$.

**Slope:**

$$x'(3) = 27 - 9 = 18, \qquad y'(3) = 6$$

$$\frac{dy}{dx}\bigg|_{t=3} = \frac{6}{18} = \frac{1}{3}$$

**Tangent line:**

$$y - 5 = \frac{1}{3}(x - 0) \implies \boxed{y = \frac{1}{3}x + 5}$$

Think of it this way: at $t = 3$ hours, the BBQ truck is at the origin of our coordinate system, heading northeast with a gentle slope of $\frac{1}{3}$. If it kept going straight, it would follow $y = \frac{1}{3}x + 5$.

**(c) Second derivative at $t = 3$.**

**Step 1:** $\frac{dy}{dx} = \frac{2t}{3t^2 - 9} = \frac{2t}{3(t^2 - 3)}$

**Step 2:** Differentiate with respect to $t$ using the quotient rule.

Let $u = 2t$, $v = 3t^2 - 9$.

$u' = 2$, $v' = 6t$.

$$\frac{d}{dt}\left[\frac{dy}{dx}\right] = \frac{2(3t^2 - 9) - 2t(6t)}{(3t^2 - 9)^2} = \frac{6t^2 - 18 - 12t^2}{(3t^2 - 9)^2} = \frac{-6t^2 - 18}{(3t^2 - 9)^2}$$

$$= \frac{-6(t^2 + 3)}{9(t^2 - 3)^2}  = \frac{-2(t^2 + 3)}{3(t^2 - 3)^2}$$

At $t = 3$:

$$\frac{d}{dt}\left[\frac{dy}{dx}\right]\bigg|_{t=3} = \frac{-2(9 + 3)}{3(9 - 3)^2} = \frac{-2(12)}{3(36)} = \frac{-24}{108} = -\frac{2}{9}$$

**Step 3:** Divide by $x'(3) = 18$:

$$\frac{d^2y}{dx^2}\bigg|_{t=3} = \frac{-2/9}{18} = -\frac{2}{162} = -\frac{1}{81}$$

Since $\frac{d^2y}{dx^2} < 0$, the path is **concave down** at $t = 3$.

$$\boxed{\frac{d^2y}{dx^2}\bigg|_{t=3} = -\frac{1}{81} < 0 \implies \text{concave down}}$$

**(d) Speed at $t = 2$ and total distance from $t = 0$ to $t = 3$.**

**Speed at $t = 2$:**

$$x'(2) = 12 - 9 = 3, \qquad y'(2) = 4$$

$$\text{speed} = \sqrt{3^2 + 4^2} = \sqrt{9 + 16} = \sqrt{25} = \boxed{5}$$

(A nice 3-4-5 right triangle! Like driving exactly 5 mph through Balboa Park.)

**Total distance from $t = 0$ to $t = 3$:**

$$D = \int_0^3 \sqrt{(3t^2 - 9)^2 + (2t)^2}\,dt = \int_0^3 \sqrt{9t^4 - 54t^2 + 81 + 4t^2}\,dt$$

$$= \int_0^3 \sqrt{9t^4 - 50t^2 + 81}\,dt$$

This integral doesn't have a nice closed form, so we evaluate with a calculator:

$$\boxed{D = \int_0^3 \sqrt{9t^4 - 50t^2 + 81}\,dt \approx 19.609}$$

</details>

---

## What's Next

You now have the tools to analyze curves that can't be expressed as simple $y = f(x)$ equations. Parametric derivatives let you find slopes, concavity, speed, and arc length for any path described by $x(t)$ and $y(t)$ — from a drone circling over Torrey Pines to a bicycle reflector tracing a cycloid along Coronado Beach. Next up, we'll enter the world of **polar coordinates**, where curves are described by a distance from the origin as a function of angle: $r = f(\theta)$. We'll learn how to find [areas enclosed by polar curves](/calculus/polar) — roses, cardioids, limacons — and connect everything back to the parametric framework you've just mastered.

---

<div align="center">

[← Improper Integrals](/calculus/improper-integrals) | [Polar Curves →](/calculus/polar)

</div>
