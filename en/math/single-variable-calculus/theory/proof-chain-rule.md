
# Proof of the Chain Rule

## 1. Objective

The goal is to formally prove that if a function $y$ depends on $u$ and $u$ depends on $x$ (forming the composite function $y = f(g(x))$, then the derivative of $y$ with respect to $x$ is the product of the derivatives of the component functions:

$$\frac{dy}{dx} = f'(g(x)) \cdot g'(x)$$

---

## 2. Initial Definitions

- **Internal Function:** Let $u = g(x)$. When the independent variable $x$ increases by $\Delta x$, the internal function $u$ undergoes a proportional increase $\Delta u$:
    
    $$\Delta u = g(x + \Delta x) - g(x)$$
    
- **External Function:** Consequently, the external function $y$ undergoes an increase $\Delta y$:
    
    $$\Delta y = f(u + \Delta u) - f(u)$$
    

---

## 3. The Incremental Ratio

The core strategy is to express the variation of $y$ relative to $x$ by using the variation of $u$ as an intermediary. We multiply and divide the incremental ratio by $\Delta u$:

$$\frac{\Delta y}{\Delta x} = \frac{\Delta y}{\Delta u} \cdot \frac{\Delta u}{\Delta x}$$

> [!IMPORTANT]
> 
> **Note on Rigor:** This manipulation assumes that $\Delta u \neq 0$ in an interval near $x$. While 100% rigorous mathematical analysis uses an auxiliary function to handle cases where $g(x)$ is constant, the limit logic remains the same for engineering applications.

---

## 4. Application of the Limit

We apply the limit as $\Delta x \to 0$. Since the function $g$ is differentiable (and therefore continuous), the increase $\Delta u$ will also tend toward zero as $\Delta x$ decreases:

$$\lim_{\Delta x \to 0} \frac{\Delta y}{\Delta x} = \lim_{\Delta x \to 0} \left( \frac{\Delta y}{\Delta u} \cdot \frac{\Delta u}{\Delta x} \right)$$

Using the property that the limit of a product is the product of the limits:

$$\frac{dy}{dx} = \left( \lim_{\Delta u \to 0} \frac{\Delta y}{\Delta u} \right) \cdot \left( \lim_{\Delta x \to 0} \frac{\Delta u}{\Delta x} \right)$$

---

## 5. Identifying the Derivatives

By observing the resulting limits, we recognize the formal definitions of the derivative:

- The first term $\lim_{\Delta u \to 0} \frac{\Delta y}{\Delta u}$ is the derivative of $f$ with respect to $u$, which is $f'(u)$.
    
- The second term $\lim_{\Delta x \to 0} \frac{\Delta u}{\Delta x}$ is the derivative of $g$ with respect to $x$, which is $g'(x)$.
    

---

## 6. Conclusion

By substituting $u$ with its original definition $g(x)$, we arrive at the final formula:

$$\frac{dy}{dx} = f'(g(x)) \cdot g'(x)$$

**The proof is complete.**