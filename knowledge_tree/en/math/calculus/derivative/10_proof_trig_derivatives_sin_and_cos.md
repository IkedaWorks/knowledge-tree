
# Proof: Fundamental Trigonometric Derivatives

This section constructs the derivatives of sine and cosine from "absolute zero" using the formal limit definition. The algebra is based on two essential tools from analytical geometry and calculus.

---

## 1. Necessary Tools

### I. Fundamental Limits

- **The Fundamental Trigonometric Limit:** When an angle $h$ (in radians) approaches zero, the sine of that angle approaches the value of the angle itself: $\lim_{h \to 0} \frac{\sin h}{h} = 1$.
    
- **The Cosine Limit:** Derived from the same geometric logic: $\lim_{h \to 0} \frac{\cos h - 1}{h} = 0$.
    

### II. Angle Addition Identities

These relationships are crucial for expanding the terms during the proof:

- $\sin(a \pm b) = \sin a \cdot \cos b \pm \sin b \cdot \cos a$
    
- $\cos(a \pm b) = \cos a \cdot \cos b \mp \sin a \cdot \sin b$
    

---

## 2. Proof: Derivative of Sine

**Rule:** $\frac{d}{dx}(\sin x) = \cos x$

1. **Formal Limit Application:** Apply the definition $f'(x) = \lim_{h \to 0} \frac{\sin(x+h) - \sin(x)}{h}$.
    
2. **Expansion:** Use the angle addition identity to expand $\sin(x+h)$: $\lim_{h \to 0} \frac{\sin(x)\cos(h) + \sin(h)\cos(x) - \sin(x)}{h}$.
    
3. **Grouping:** Group by common terms ($\sin x$): $\lim_{h \to 0} \left[ \sin(x) \cdot \frac{\cos(h) - 1}{h} + \cos(x) \cdot \frac{\sin(h)}{h} \right]$.
    
4. **Applying Fundamental Limits:**
    
    - The term $\frac{\cos(h) - 1}{h}$ tends to $0$.
        
    - The term $\frac{\sin(h)}{h}$ tends to $1$.
        
5. **Result:** $f'(x) = \sin(x) \cdot (0) + \cos(x) \cdot (1) = \cos x$.
    

---

## 3. Proof: Derivative of Cosine

**Rule:** $\frac{d}{dx}(\cos x) = -\sin x$

1. **Formal Limit Application:** Apply the definition $f'(x) = \lim_{h \to 0} \frac{\cos(x+h) - \cos(x)}{h}$.
    
2. **Expansion:** Use the angle addition identity: $\lim_{h \to 0} \frac{\cos(x)\cos(h) - \sin(x)\sin(h) - \cos(x)}{h}$.
    
3. **Grouping:** Group by common terms ($\cos x$): $\lim_{h \to 0} \left[ \cos(x) \cdot \frac{\cos(h) - 1}{h} - \sin(x) \cdot \frac{\sin(h)}{h} \right]$.
    
4. **Applying Fundamental Limits:**
    
    - The term $\frac{\cos(h) - 1}{h}$ tends to $0$.
        
    - The term $\frac{\sin(h)}{h}$ tends to $1$.
        
5. **Result:** $f'(x) = \cos(x) \cdot (0) - \sin(x) \cdot (1) = -\sin x$.
    

> [!NOTE]
> 
> **Engineering Observation:** For very small angles ($h \approx 0$), sine behaves linearly (like $y=x$), while cosine behaves like a constant near $1$. This explains why the rate of change (derivative) of sine is at its maximum at the origin, while the rate of change of cosine is zero.