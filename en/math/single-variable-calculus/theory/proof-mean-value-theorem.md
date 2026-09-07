
# Proofs: Why Rolle and MVT are True

## 1. Why is Rolle's Theorem True?
Before proving the MVT, we must accept Rolle's Theorem.  
**The Logic:** If you leave the ground, climb, and then return to the ground ($f(a) = f(b)$), and you do so smoothly (differentiably), at some point you had to stop climbing to start descending.

### Logical Proof:
1.  **Constant Case:** If the function is constant (a horizontal straight line), the derivative is zero at all points. **Proven.**
2.  **Non-Constant Case:** If it is not constant, it must go up or down. If it rises, it must reach a maximum or minimum value at a point $c$.
3.  **Extreme Point:** Since $c$ is a maximum or minimum point and the function is differentiable, the tangent line there must be horizontal ($f'(c) = 0$). If the slope were positive, you would still be climbing; if it were negative, you would already be past the peak.

---

## 2. Proof of the Mean Value Theorem (MVT)
Now, let's prove the MVT using Rolle's Theorem. The trick here is to "tilt" our perspective so that the average secant line looks horizontal.

### Step-by-Step:
1.  **Define the Secant Line:**  
    The line connecting points $(a, f(a))$ and $(b, f(b))$ has the equation:
    $$y = f(a) + \frac{f(b) - f(a)}{b - a}(x - a)$$

2.  **Create the Auxiliary Function ($h(x)$):**  
    Imagine a new function that measures the vertical distance between our complex curve $f(x)$ and the secant line:
    $$h(x) = f(x) - \left[ f(a) + \frac{f(b) - f(a)}{b - a}(x - a) \right]$$

3.  **Test the Boundaries of $h(x)$:**  
    *   If you plug in $x = a$, the result is $0$.
    *   If you plug in $x = b$, the result is also $0$.  
    **Conclusion:** $h(a) = h(b)$. The function $h(x)$ starts and ends at "zero"!

4.  **Invoke Rolle's Theorem:**  
    Since $h(x)$ is continuous, differentiable, and $h(a) = h(b)$, Rolle's Theorem guarantees that there is a point $c$ where the derivative of $h$ is zero: $h'(c) = 0$.

5.  **Finalize the Algebra:**  
    Differentiating $h(x)$ with respect to $x$:
    $$h'(x) = f'(x) - \frac{f(b) - f(a)}{b - a}$$
    At point $c$, where $h'(c) = 0$:
    $$0 = f'(c) - \frac{f(b) - f(a)}{b - a} \implies f'(c) = \frac{f(b) - f(a)}{b - a}$$

---

## 3. Why does this make sense now?
Imagine the secant line (the average) is your horizon.

*   **Rolle** says that if you rise and return to the horizon, there was a peak.
*   **MVT** says that it doesn't matter if your horizon is tilted or flat; if you move away from it and then return, at some point you had to move parallel to it.

> [!IMPORTANT]
> 
> **Engineering Takeaway**
> This proof is the mathematical foundation for safety sensors. For instance, if an elevator's average speed exceeded safety limits, the MVT proves that at some specific moment, the instantaneous speed was also unsafe, allowing for precise event logging in black boxes.