
# Derivative Applications: Maxima and Minima

## 1. Explanation and Intuition
Imagine you are hiking in a mountain range.

*   **The Maximum** is the mountain peak.
*   **The Minimum** is the bottom of the valley.
*   **The Calculus Insight:** What happens to your slope (tangent) exactly when you are at the very top of a peak or the very bottom of a valley? You are neither going up nor down. For a brief instant, you are "flat."
*   **Mathematically:** This means your derivative is zero ($f'(x) = 0$).

---

## 2. The Optimization Algorithm
To find these points in any function, we follow three fundamental steps:

1.  **Find Critical Points:** We differentiate the function and set it to zero ($f'(x) = 0$). This tells us where the curve "stalls."
2.  **The Second Derivative Test ($f''(x)$):** How do we know if a point is a peak (maximum) or a valley (minimum) without looking at a graph?
    *   If $f''(x) > 0$: Concave up (smile). The point is a **Minimum**.
    *   If $f''(x) < 0$: Concave down (frown). The point is a **Maximum**.
3.  **Check Boundaries:** If the problem provides a closed interval (e.g., from $x=0$ to $x=10$), you must test the values at these limits, as the highest value could be right at "the edge."

---

## 3. Practical Example: Engineering Design

> [!NOTE]
> 
> **Server Chassis Scenario**
> You are designing a new server cabinet. Due to space constraints, the base must be square, and the total volume must be exactly 128 liters ($128,000 \text{ cm}^3$). What should the base side ($x$) and height ($h$) dimensions be to use the **minimum** amount of metal for the surface area?

**Resolution:**
1.  **Equations:**
    *   **Volume:** $V = x^2 \cdot h = 128 \implies h = \frac{128}{x^2}$
    *   **Total Area (to minimize):** $A = x^2 \text{ (base)} + 4xh \text{ (sides)}$
2.  **Refactoring (The Trick):** Substitute $h$ into the area equation:
    $$A(x) = x^2 + 4x\left(\frac{128}{x^2}\right) = x^2 + \frac{512}{x}$$
3.  **Derivative to find the critical point:**
    $$A'(x) = 2x - \frac{512}{x^2}$$
    $$0 = 2x - \frac{512}{x^2} \implies 2x^3 = 512 \implies x^3 = 256$$
    $$x \approx 6.35 \text{ cm}$$

> [!TIP]
> 
> **Optimization Insight**
> This calculation ensures that you are reaching the peak efficiency of your materials. In large-scale manufacturing, using calculus to find the minimum surface area can save companies millions in raw material costs.