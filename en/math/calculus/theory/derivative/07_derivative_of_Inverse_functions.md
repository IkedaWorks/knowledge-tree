
# Derivative of the Inverse Function

## 1. The Concept: Derivative as "Inverse Speed"

The derivative of a function represents an instantaneous rate of change. If a function $f(x)$ transforms **Time ($x$)** into **Position ($y$)**, its derivative $f'(x)$ is the velocity (meters gained per second). The **inverse function** $f^{-1}(y)$ performs the opposite task, transforming **Position ($y$)** back into **Time ($x$)**. Its derivative measures how many seconds are spent per meter.

### Reciprocity Relationship

- Geometrically, the slope of one function is the **multiplicative inverse** of the slope of the other at the corresponding point.
    
- If you run at 10 m/s (high speed), you spend 1/10 s/m (low time).
    

---

## 2. Proof via the Chain Rule

The proof relies on the fact that an inverse function "undoes" the original function, resulting in the identity function:

$$f(f^{-1}(x)) = x \text{}$$

**The Derivation:**

1. **Differentiate both sides** with respect to $x$. The right side (derivative of $x$) is 1.
    
2. **Apply the Chain Rule** to the left side:
    
    $$\frac{d}{dx}[f(f^{-1}(x))] = 1 \text{}$$
    
    $$f'(f^{-1}(x)) \cdot (f^{-1})'(x) = 1 \text{}$$
    
3. **Isolate the target term**, which is the derivative of the inverse $(f^{-1})'(x)$:
    
    $$(f^{-1})'(x) = \frac{1}{f'(f^{-1}(x))} \text{}$$
    

---

## 3. Practical Example: The Origin of $1/x$

We can prove why the derivative of $\ln(x)$ is $1/x$ by using its inverse, the exponential function ($e^y$).

- Let $f(y) = e^y$. We know $f'(y) = e^y$.
    
- The inverse is $f^{-1}(x) = \ln(x)$.
    
- **Applying the formula:**
    
    $$(\ln x)' = \frac{1}{f'(\ln x)} = \frac{1}{e^{\ln x}} \text{}$$
    
- Since $e$ and $\ln$ are inverse operations, they cancel out:
    
    $$(\ln x)' = \frac{1}{x} \text{}$$
    

---

## 4. Summary and Mental Rules

- **The Master Formula:** $(f^{-1})'(x) = \frac{1}{f'(y)}$, where $y = f^{-1}(x)$.
    
- **Verbal Rule:** The derivative of the inverse at a point is "one over the derivative of the original function applied to the inverse itself".
    
- **Geometry:** If the tangent line of $f$ has a slope $m$, the tangent line of $f^{-1}$ at the reflected point (across the line $y=x$) will have a slope of $1/m$.
    

---

## 5. Condition of Existence: Bijectivity

The derivative of the inverse function only exists if the original function is **bijective** (injective and surjective) within the considered interval.

### Why is this mandatory?

- **Injective Requirement:** If a function is not injective (like $f(x) = x^2$ across all real numbers), a single $y$ value could come from two different $x$ values. In this case, the "inverse" would not be a function as it would have multiple results for one input.
    
- **Non-Zero Derivative:** According to the formula $(f^{-1})'(x) = \frac{1}{f'(y)}$, if the original function's derivative is zero ($f'(y) = 0$), the inverse derivative becomes undefined (division by zero). Geometrically, a horizontal tangent on the original function becomes a vertical tangent on the inverse.
    
- **Engineering Example:** Trigonometric functions are periodic and not bijective over the real domain. We must restrict their domain (e.g., $-\pi/2$ to $\pi/2$ for sine) so the inverse ($\arcsin$) can exist and be differentiable.