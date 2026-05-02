
# Proof: Fundamental Theorem of Calculus 

## The Intuition Behind the Proof
To prove that the derivative of the accumulated area is the function itself ($A'(x) = f(x)$), we must return to the **Limit Definition of the Derivative**.

*   **The Concept:** Imagine an accumulated area $A(x)$ under a curve. If you move a tiny step $h$ along the x-axis, you add a small "slice" of area.
*   **The Geometry:** 
    *   This slice has a width $h$ and a height approximately equal to $f(x)$.
    *   The change in area ($\Delta A$) is roughly a rectangle: $\Delta A \approx \text{base} \cdot \text{height} = h \cdot f(x)$.
    *   If the rate of change of the area is $\frac{\Delta A}{h}$, then $\frac{h \cdot f(x)}{h} = f(x)$.

---

##  Mathematical Formalization
Let’s define the area function as $A(x) = \int_{a}^{x} f(t) \, dt$. By the definition of the derivative:
$$A'(x) = \lim_{h \to 0} \frac{A(x+h) - A(x)}{h}$$

### Step 1: Subtraction of Integrals
Using integral properties, the difference between the total area up to $x+h$ and the area up to $x$ is exactly the integral over the small interval $[x, x+h]$:
$$A(x+h) - A(x) = \int_{x}^{x+h} f(t) \, dt$$

### Step 2: Mean Value Theorem (MVT) for Integrals
The MVT for integrals guarantees that there exists a value $c$ within the interval $[x, x+h]$ such that the area of the slice is exactly equal to a rectangle with height $f(c)$ and width $h$:
$$\int_{x}^{x+h} f(t) \, dt = f(c) \cdot h$$

### Step 3: Applying the Limit
Substituting this back into the derivative formula:
$$A'(x) = \lim_{h \to 0} \frac{f(c) \cdot h}{h} = \lim_{h \to 0} f(c)$$
As $h \to 0$, the interval $[x, x+h]$ "squeezes" point $c$ until it is forced to become $x$ itself (by the **Squeeze Theorem**). Therefore, $f(c) \to f(x)$.

**Result:** $A'(x) = f(x)$

---

## Conclusion
This proof confirms that the integral "stores" the original function within itself. By differentiating the accumulation, you remove the "shell" of the sum and reveal the height of the function at that exact instant.

*   **Differentiating the Integral:** Like taking a "snapshot" of the instantaneous speed of a filling process.
*   **Integrating the Derivative:** Like summing all those snapshots to reconstruct the entire movie.

> [!IMPORTANT]
> 
> This proof is what validates the use of **Part 2 of the FTC** ($\int_{a}^{b} f = F(b) - F(a)$), as we now know for certain that integration and differentiation are operations that cancel each other out.