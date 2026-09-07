
# Related Rates: Calculus in Motion

## 1. Concept and Intuition
Until now, we have analyzed how $y$ changes relative to $x$. In **Related Rates**, the scenario shifts: we have two or more variables (such as radius, volume, height, or distance) that depend on a third, invisible, and omnipresent variable: **time ($t$)**.

> [!TIP]
> 
> **The Balloon Intuition**
> Imagine inflating a spherical balloon. As you pump air into it (change in Volume over time: $dV/dt$), the balloon's radius increases ($dr/dt$).
> These rates are "tied together" by geometry. If you know the speed of the air pump, you can discover the expansion speed of the rubber.

## 2. The Resolution Algorithm (Pipeline)
To solve rate problems, an Engineer follows a logical flow:

1.  **Identify Variables:** List the known rates and the desired rate (e.g., "I have $dV/dt$, I want $dh/dt$").
2.  **Connection Equation:** Find the geometric formula that connects the variables (Volume, Area, Pythagorean Theorem).
3.  **Implicit Differentiation with respect to Time:** Differentiate both sides relative to $t$.
4.  **The "Stamp":** Since all variables depend on $t$, every derivative gets Leibniz's "stamp" ($\frac{dV}{dt}, \frac{dr}{dt}, \frac{dh}{dt}$).
5.  **Instantaneous Substitution:** Plug in the known values for the exact moment requested and isolate the unknown.

---

## 3. Exercise 1: The Conical Tank (Sensor Classic)
**Problem:** An inverted conical tank is $10\text{m}$ high and has a $4\text{m}$ radius at the top. Water is pumped in at $2\text{ m}^3/\text{min}$. What is the rising speed of the water level ($\frac{dh}{dt}$) when the depth $h$ is $5\text{m}$?

**Step-by-Step Resolution:**
1.  **Data:** $\frac{dV}{dt} = 2$. We want $\frac{dh}{dt}$ when $h = 5$.
2.  **Equation:** $V = \frac{1}{3}\pi r^2 h$.
3.  **Variable Reduction (Similar Triangles):**
    The radius and height maintain the tank's proportion: $\frac{r}{h} = \frac{4}{10} \implies r = 0.4h$.
    Substituting into the volume: $V = \frac{1}{3}\pi (0.4h)^2 h \implies V = \frac{0.16\pi}{3} h^3$.
4.  **Differentiating with respect to Time:**
    $$\frac{dV}{dt} = \frac{0.16\pi}{3} \cdot 3h^2 \cdot \frac{dh}{dt} \implies \frac{dV}{dt} = 0.16\pi h^2 \frac{dh}{dt}$$
5.  **Final Calculation:**
    $2 = 0.16\pi (5^2) \frac{dh}{dt} \implies 2 = 4\pi \frac{dh}{dt}$

**Result:** $\frac{dh}{dt} = \frac{1}{2\pi} \approx 0.16\text{ m/min}$

---

## 4. Exercise 2: The Oil Spill
**Scenario:** Oil leaks in a circular shape. The area increases at a constant rate of $6\pi \text{ km}^2/\text{h}$. How fast is the radius growing ($\frac{dr}{dt}$) when $r = 3 \text{ km}$?

1.  **Equation:** $A = \pi r^2$.
2.  **Implicit Differentiation:**
    $$\frac{dA}{dt} = 2\pi r \frac{dr}{dt}$$
3.  **Substitution:**
    $6\pi = 2\pi (3) \frac{dr}{dt} \implies 6\pi = 6\pi \frac{dr}{dt}$

**Result:** $\frac{dr}{dt} = 1 \text{ km/h}$.

> [!IMPORTANT]
> 
> **Engineering Interpretation**
> Note that if the area rate ($\frac{dA}{dt}$) is constant, the radial velocity ($\frac{dr}{dt}$) decreases as the circle grows. This happens because maintaining the same area increase in a giant circle requires much less radial advancement than in a small circle.

---

## 5. Study Hacks
*   **Abstraction:** Calculus is not static. Don't see the circle as a drawing; see it as an "event" that is happening.
*   **Geometry is the Base:** If you don't know the formulas for volume ($V_{\text{sphere}} = \frac{4}{3}\pi r^3$) or area, you will get stuck before the calculus even begins.
*   **Constant Rates:** When a problem says something varies at a constant rate, ask yourself: "Who needs to change speed for this proportion to be maintained?". In the cone, as it gets wider at the top, the water must rise slower to maintain the same inflow.