
# Differentiation Rules: Mathematical Proofs

These proofs transform "memorized rules" into fundamental mathematical truths by utilizing the formal definition of a derivative:

$$f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$$

---

### ➕ Sum Rule

**Rule:** $(u + v)' = u' + v'$

**Objective:** To prove that the derivative distributes over a sum.

**Step-by-Step Proof:**

- **Define the function:** Let $F(x) = u(x) + v(x)$.
    
- **Apply the definition:** $\lim_{h \to 0} \frac{[u(x+h) + v(x+h)] - [u(x) + v(x)]}{h}$.
    
- **Group the terms:** $\lim_{h \to 0} \left( \frac{u(x+h) - u(x)}{h} + \frac{v(x+h) - v(x)}{h} \right)$.
    
- **Limit properties:** Use the property that the limit of a sum is the sum of the limits: $\lim_{h \to 0} \frac{u(x+h) - u(x)}{h} + \lim_{h \to 0} \frac{v(x+h) - v(x)}{h}$.
    
- **Conclusion:** $F'(x) = u'(x) + v'(x)$.
    

---

### ✖️ Product Rule

**Rule:** $(u \cdot v)' = u'v + uv'$

**Objective:** To understand why we do not simply multiply the two individual derivatives.

**Step-by-Step Proof:**

- **Formal Definition:** $\lim_{h \to 0} \frac{u(x+h)v(x+h) - u(x)v(x)}{h}$.
    
- **Algebraic Trick:** Add and subtract the term $u(x+h)v(x)$ in the numerator:
    
    $$\lim_{h \to 0} \frac{u(x+h)v(x+h) - u(x+h)v(x) + u(x+h)v(x) - u(x)v(x)}{h}$$
    
- **Factoring:** Group common terms to isolate the difference quotients:
    
    $$\lim_{h \to 0} \left[ u(x+h)\frac{v(x+h) - v(x)}{h} + v(x)\frac{u(x+h) - u(x)}{h} \right]$$
    
- **Apply the Limit:** As $h \to 0$:
    
    - $u(x+h) \to u(x)$.
        
    - $\frac{v(x+h) - v(x)}{h} \to v'(x)$.
        
    - $\frac{u(x+h) - u(x)}{h} \to u'(x)$.
        
- **Conclusion:** $(u \cdot v)' = u(x)v'(x) + v(x)u'(x)$.
    

---

### 📉 Power Rule (Example for $n = 2$)

**Rule Example:** $(x^2)' = 2x$

**Step-by-Step Proof:**

- **Apply the definition:** $\lim_{h \to 0} \frac{(x+h)^2 - x^2}{h}$.
    
- **Expand the term:** $\lim_{h \to 0} \frac{x^2 + 2xh + h^2 - x^2}{h}$.
    
- **Simplify:** $\lim_{h \to 0} \frac{2xh + h^2}{h} = \lim_{h \to 0} (2x + h) = 2x$.
    

> [!NOTE]
> 
> For the general case of $x^n$, the proof utilizes **Newton's Binomial Theorem**. This requires familiarity with combinatorics to understand how higher-order terms of $h$ cancel out.

---

### ➗ Quotient Rule

**Rule:** $\left( \frac{f}{g} \right)' = \frac{f'g - fg'}{g^2}$

**Step-by-Step Proof:**

- **Reorganization:** Use a common denominator:
    
    $$\lim_{h \to 0} \frac{f(x+h)g(x) - f(x)g(x+h)}{h \cdot g(x+h)g(x)}$$
    
- **Add and Subtract:** Insert the term $f(x)g(x)$ in the numerator:
    
    $$\lim_{h \to 0} \frac{g(x)[f(x+h) - f(x)] - f(x)[g(x+h) - g(x)]}{h \cdot g(x+h)g(x)}$$
    
- **Final Limit:** As $h \to 0$, the denominator $g(x+h)g(x)$ becomes $g(x)^2$.
    
- **Final Result:** $\frac{g(x)f'(x) - f(x)g'(x)}{g(x)^2}$.