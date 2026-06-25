
# Improper Integrals

## The Concept of Impropriety

An integral is said to be **improper** when either the interval of integration or the function itself challenges the standard rules of the Riemann Integral (which requires a closed interval and a bounded function). In calculus, we do not operate directly with infinity; instead, we use **Limits** to describe the behavior of the area as we approach the "forbidden" boundary.

---

## Classification of Improper Integrals

### Type 1: Infinite Intervals

Occurs when one or both limits of integration are infinite ($\infty$ or $-\infty$).

- **Formalism:** $\int_{a}^{\infty} f(x) \, dx = \lim_{t \to \infty} \int_{a}^{t} f(x) \, dx$
    

### Type 2: Infinite Discontinuities (Asymptotes)

Occurs when the interval $[a, b]$ is finite, but the function $f(x)$ explodes to infinity at some point (usually at the endpoints or in the middle of the interval).

- **Formalism:** $\int_{0}^{1} \frac{1}{\sqrt{x}} \, dx = \lim_{t \to 0^{+}} \int_{t}^{1} \frac{1}{\sqrt{x}} \, dx$
    

---

## The Verdict: Convergence vs. Divergence

After applying the limit to the result of the integral, we have two possible outcomes:

- **Convergent:** The limit results in a finite real number. The "tail" of the function decreases fast enough that the total accumulated area is bounded.
    
- **Divergent:** The limit results in $\pm\infty$ or does not exist. The function does not decay sufficiently, and the area "escapes."
    

> [!TIP]
> 
> **The p-series Rule (p-test):** For $\int_{1}^{\infty} \frac{1}{x^p} \, dx$:
> 
> - If **$p > 1$**, the integral **converges**. (e.g., $1/x^2$ goes to zero fast enough).
>     
> - If **$p \leq 1$**, the integral **diverges**. (e.g., $1/x$ is too "slow" and accumulates infinite area).
>     

---

## Solved Example 1: Convergence (Type 1)

**Problem:** Calculate the area under $f(x) = \frac{1}{x^2}$ for $x \ge 1/2$.

1. **Setup:** $\int_{1/2}^{\infty} \frac{1}{x^2} \, dx$
    
2. **Limit:** $\lim_{b \to \infty} \int_{1/2}^{b} x^{-2} \, dx$
    
3. **Integral:** $\lim_{b \to \infty} \left[ -\frac{1}{x} \right]_{1/2}^{b}$
    
4. **Application:** $\lim_{b \to \infty} \left( -\frac{1}{b} - (-\frac{1}{1/2}) \right) = \lim_{b \to \infty} \left( -\frac{1}{b} + 2 \right)$
    
5. **Result:** Since $1/b \to 0$ as $b \to \infty$, the result is **2**.
    
6. **Conclusion:** The integral converges to 2. Even though the interval is infinite, the area is finite!
    

---

## Solved Example 2: Infinite Integrand (Type 2)

**Problem:** $\int_{0}^{16} \frac{1}{\sqrt[4]{x}} \, dx$

_Here, the problem is at zero, as $1/0$ is a vertical asymptote._

1. **Limit:** $\lim_{t \to 0^{+}} \int_{t}^{16} x^{-1/4} \, dx$
    
2. **Antiderivative:** $\lim_{t \to 0^{+}} \left[ \frac{x^{3/4}}{3/4} \right]_{t}^{16} = \lim_{t \to 0^{+}} \left[ \frac{4\sqrt[4]{x^3}}{3} \right]_{t}^{16}$
    
3. **Calculation:** $\frac{4\sqrt[4]{16^3}}{3} - \frac{4\sqrt[4]{t^3}}{3}$
    
    - $\sqrt[4]{16^3} = (\sqrt[4]{16})^3 = 2^3 = 8$.
        
    - $\lim_{t \to 0} \sqrt[4]{t^3} = 0$.
        
4. **Result:** $\frac{4 \cdot 8}{3} = \mathbf{\frac{32}{3} \approx 10.66}$
    
5. **Conclusion:** The function explodes at zero, but the area beneath it is finite. **Convergent!**
    

---

## ⚠️ Engineering Observations

- **Vertical Asymptotes:** Always use one-sided limits ($t \to a^+$ or $t \to b^-$) to ensure you remain within the function's domain.
    
- **Oblique Asymptotes:** As you correctly noted, if a function follows an inclined line toward infinity, the area will never "close." The result will always be divergent.