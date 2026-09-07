
# Chain Rule (Composite Functions)

The **Chain Rule** is used to differentiate functions that are nested within one another (composition). It establishes that the total rate of change is the product of the rates of change for each layer.

## 1. Intuition: The Russian Doll Analogy (Matryoshkas)

To reach the smallest doll (the inner function), you must first open the larger doll (the outer function). The total derivative is the "opening speed" of the outer doll multiplied by the "speed" of the inner doll.

---

## 2. The Rule and Notations

If $y = f(u)$ and $u = g(x)$, we have the composite function $y = f(g(x))$.

### I. Lagrange's Notation

$$(f \circ g)'(x) = f'(g(x)) \cdot g'(x)$$

- **Translation:** "Differentiate the outside (keeping the inside intact) and multiply by the derivative of the inside".
    

### II. Leibniz's Notation

$$\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx}$$

- **Engineering Tip:** This notation is extremely useful because it visually resembles fraction simplification where $du$ "cancels out," leaving $\frac{dy}{dx}$.
    

---

## 3. Step-by-Step Examples

### Example 1: Power of a Function ($f(x) = (3x^2 + 1)^5$)

1. **Identify the layers:**
    
    - **Outside:** $(u)^5 \to$ Derivative: $5u^4$.
        
    - **Inside:** $3x^2 + 1 \to$ Derivative: $6x$.
        
2. **Apply the Chain Rule:** $f'(x) = 5(3x^2 + 1)^4 \cdot (6x)$.
    
3. **Simplify:** $f'(x) = 30x(3x^2 + 1)^4$.
    

### Example 2: Composite Trigonometric Function ($f(x) = \sin(x^3)$)

1. **Identify the layers:**
    
    - **Outside:** $\sin(u) \to$ Derivative: $\cos(u)$.
        
    - **Inside:** $x^3 \to$ Derivative: $3x^2$.
        
2. **Apply the Chain Rule:** $f'(x) = \cos(x^3) \cdot 3x^2$.
    
3. **Result:** $f'(x) = 3x^2 \cos(x^3)$.
    

### Example 3: The "Triple Chain" ($f(x) = e^{\sin(5x)}$)

1. **Exponential (Outer):** $e^{\sin(5x)} \cdot (\text{derivative of the exponent})$.
    
2. **Sine (Middle):** $\cos(5x) \cdot (\text{derivative of the argument})$.
    
3. **Polynomial (Inner):** $5$.
    
4. **Verdict:** $f'(x) = 5 \cos(5x) e^{\sin(5x)}$.
    

---

## 4. Tips and Cautions

- **The Fatal Error:** Trying to differentiate the inside at the same time as the outside.
    
    - **Wrong:** $(\sin(x^2))' = \cos(2x)$.
        
    - **Correct:** You keep the $x^2$ intact while changing sine to cosine, and only then multiply by $2x$.
        
- **Onion Skin:** Always work from the outermost operation to the innermost.
    
- **Roots are Chains:** Remember that $\sqrt{g(x)} = [g(x)]^{1/2}$.
    
    - **Useful Shortcut:** $(\sqrt{u})' = \frac{u'}{2\sqrt{u}}$.
        

---

## 5. Intuitive Proof via Leibniz

While a rigorous proof involves Newton's limits and adjustments to avoid division by zero, the clearest way to visualize it is through ratios of change:

$$\frac{\Delta y}{\Delta x} = \frac{\Delta y}{\Delta u} \cdot \frac{\Delta u}{\Delta x}$$

As we apply the limit $\Delta x \to 0$ (which implies $\Delta u \to 0$ in continuous functions), these average ratios become instantaneous derivatives:

$$\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx}$$