# Change of Variables in Definite Integrals

## Definition
When performing a variable substitution ( $u = g(x)$ ) in a **definite integral**, the original limits of integration ($a$ and $b$) must be updated to the corresponding values in the new variable ( $u(a)$ and $u(b)$ ). This allows you to solve the integral and apply the Fundamental Theorem of Calculus (FTC) directly, without needing to switch back to the original variable $x$.

### Strategic Advantages
*   **Mathematical Consistency:** Prevents notation errors like writing $x$-limits on a function of $u$.
*   **Speed:** Eliminates the "back-substitution" step at the end of the calculation.
*   **Simplification:** New $u$-limits often result in cleaner numbers (such as $0, 1$, or $e$).

---

## Execution Protocol (Step-by-Step)

1.  **Choose $u$:** Identify the inner function $g(x)$ whose derivative $g'(x)$ is also present.
2.  **Differential:** Calculate $du = g'(x) \, dx$.
3.  **Update the Limits (Crucial):**
    *   Substitute the original lower limit ($x = a$) into the $u$ formula: $u_{lower} = g(a)$.
    *   Substitute the original upper limit ($x = b$) into the $u$ formula: $u_{upper} = g(b)$.
4.  **Rewrite:** Set up the new integral using only $u, du$, and the new limits $u_{lower}$ and $u_{upper}$.
5.  **Direct Resolution:** Find the antiderivative in $u$ and apply the new limits.

---

##  Practical Solved Example
**Problem:** Calculate $\int_{1}^{2} (2x + 1)^2 \, dx$

1.  **Choice of $u$ and Differential:**
    *   $u = 2x + 1$
    *   $du = 2 \, dx \implies dx = \frac{du}{2}$
2.  **Change of Limits:**
    *   If $x = 1$: $u = 2(1) + 1 = \mathbf{3}$.
    *   If $x = 2$: $u = 2(2) + 1 = \mathbf{5}$.
3.  **New Definite Integral:**
    $$\frac{1}{2} \int_{3}^{5} u^2 \, du$$
4.  **Resolution:**
    $$\frac{1}{2} \left[ \frac{u^3}{3} \right]_{3}^{5} = \frac{1}{6} (5^3 - 3^3) = \frac{1}{6} (125 - 27) = \mathbf{\frac{49}{3}}$$

> [!NOTE]
> 
> By using the direct method, you solved a much simpler integral. Since the limits were rewritten, there is no need to replace $u$ back with $x$ at the end.

---

## Geometric "Magic" and Scale Change
When you set $u = g(x)$, you are changing the "ruler" used to measure the horizontal axis. If the original function is in a "tight" interval but the $u$ function expands it, the differential $du$ compensates for this expansion or contraction perfectly.

The Change of Variables Theorem guarantees that:
$$\int_{a}^{b} f(g(x)) \cdot g'(x) \, dx = \int_{g(a)}^{g(b)} f(u) \, du$$

### The Currency Analogy
Think of it as different currencies:
*   You can have 10 Dollars in a single 10-dollar bill (**Simple integral in $x$**).
*   You can have 10 Dollars in two 5-dollar bills (**Substituted integral in $u$**).
*   The final value (purchasing power / area) remains the same, but the "face" of the calculation has changed. Updating the limits is simply adjusting your "wallet" to the new currency.

> [!TIP]
> 
> **The FTC in the $u$-Universe**
> Once the integral is transformed, the variable $x$ effectively ceases to exist for that problem. The FTC works perfectly in any "universe" (variable), provided the function is continuous within that specific interval.