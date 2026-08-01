
# 1. What is an Implicit Equation?

We say a function is in **explicit form** when the output $y$ is isolated, similar to a variable assignment in programming: $y = f(x)$.

In **implicit form**, however, the variables $x$ and $y$ are intertwined in a relationship of dependence. You know that $y$ depends on $x$, but they are "trapped" within the same expression.

### Classic Examples:
*   **Trigonometric Circle:** $x^2 + y^2 = 1$
*   **General Linear Equation:** $ax + by + c = 0$
*   **Folium of Descartes:** $x^3 + y^3 - 3axy = 0$

> [!WARNING]
> 
> **Why not isolate "y"?**
> In high school, the strategy was always to isolate $y$. In higher-level Calculus, this is often:
> 1.  **Impossible:** Try to isolate $y$ in $y^5 + 3x^2y^2 + \sin(y) = 10$. No algebra exists that allows $y$ to be isolated.
> 2.  **Inefficient:** Even when isolatable (like in the circle, yielding $y = \pm\sqrt{1-x^2}$), the resulting derivative is much more complex than if we were to differentiate the original equation.

## 2. The "Stamp" Logic (Chain Rule)
The secret to implicit differentiation is treating $y$ as a function of $x$ that you don't fully know yet: $y = y(x)$.

Whenever we differentiate a term containing $y$, we must apply the **Chain Rule**. In practice, every time you derive a $y$, you must "stamp" the result with a $\frac{dy}{dx}$ (or $y'$).

---

## 3. Solved Exercises (Leibniz Notation)
Leibniz's notation ($\frac{dy}{dx}$) is the most common in Physics, Chemistry, and Differential Equations (ODE). Getting used to it now will ease your transition to natural science subjects.

### Exercise 1: The Unit Circle
**Problem:** Find the slope of the tangent line at any point on the circle $x^2 + y^2 = 1$.

1.  **Differentiate both sides with respect to $x$:**
    $$\frac{d}{dx}(x^2) + \frac{d}{dx}(y^2) = \frac{d}{dx}(1)$$
2.  **Applying the rules:**
    *   $\frac{d}{dx}(x^2) = 2x$
    *   $\frac{d}{dx}(y^2) = 2y \cdot \frac{dy}{dx}$ (The "stamp" appears here!)
    *   $\frac{d}{dx}(1) = 0$
3.  **Assembling and isolating:**
    $2x + 2y \frac{dy}{dx} = 0 \implies 2y \frac{dy}{dx} = -2x$

**Result:** $\frac{dy}{dx} = -\frac{x}{y}$

### Exercise 2: The "Mixed" Curve (Product of x and y)
**Problem:** Find $\frac{dy}{dx}$ for the equation $x^2 + xy + y^2 = 7$.
*This is a classic exam question, as the $xy$ term requires the **Product Rule**: $(uv)' = u'v + uv'$.*

1.  **Differentiating term by term:**
    *   $\frac{d}{dx}(x^2) = 2x$
    *   $\frac{d}{dx}(xy) = (1 \cdot y) + (x \cdot \frac{dy}{dx})$
    *   $\frac{d}{dx}(y^2) = 2y \frac{dy}{dx}$
2.  **Joining the equation:**
    $2x + y + x \frac{dy}{dx} + 2y \frac{dy}{dx} = 0$
3.  **Grouping terms with $\frac{dy}{dx}$:**
    $\frac{dy}{dx} (x + 2y) = -2x - y$

**Final Result:** $\frac{dy}{dx} = -\frac{2x + y}{x + 2y}$

### Exercise 3: The Hyperbola Challenge
**Problem:** Find the derivative of the unit hyperbola $x^2 - y^2 = 1$.

1.  **Direct derivative:**
    $2x - 2y \frac{dy}{dx} = 0$
2.  **Isolating the term:**
    $-2y \frac{dy}{dx} = -2x \implies \frac{dy}{dx} = \frac{-2x}{-2y}$

**Result:** $\frac{dy}{dx} = \frac{x}{y}$

> [!TIP]
> 
> **Geometric Difference**
> Note the symmetry:
> *   In the **Circle** ($x^2 + y^2 = 1$), the derivative is $-x/y$.
> *   In the **Hyperbola** ($x^2 - y^2 = 1$), the derivative is $x/y$.
>
> This small sign change in the graph completely alters the direction of the tangent lines!