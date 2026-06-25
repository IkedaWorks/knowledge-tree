

# Derivatives of Inverse Trigonometric Functions

The study of inverse trigonometric derivatives requires a mastery of trigonometric functions, fundamental identities, and the application of the **Derivative of the Inverse Function**.

> [!CAUTION]
> 
> **RECOMMENDATION**
> 
> If studying for an upcoming evaluation, focus on memorizing the final formulas, as this topic appears less frequently in introductory exams.

---

## 1. Intuition: The Transition to Geometric Measures

Inverse functions shift the mathematical perspective:

- **Sine:** "Given the angle, what is the ratio (height)?"
    
- **Arcsine:** "Given the ratio, what is the angle?"
    

When differentiating the arcsine, we examine the rate of change of the angle relative to the change in height. The results are algebraic rather than trigonometric because right-triangle geometry is used to convert angular relationships into length measurements.

---

## 2. Proof and Formalization

The **Inverse Function Rule** and the **Pythagorean Theorem** are the primary tools used for these proofs.

### I. Derivative of Arcsine ($\arcsin x$)

**Definition:** $\frac{d}{dx}(\arcsin x) = \frac{1}{\sqrt{1-x^2}}$

**Proof:**

1. Let $y = \arcsin x$, which implies $\sin y = x$.
    
2. Apply the inverse rule: $\frac{dy}{dx} = \frac{1}{\frac{d}{dy}(\sin y)} = \frac{1}{\cos y}$.
    
3. To express $\cos y$ in terms of $x$, use the Fundamental Identity: $\sin^2 y + \cos^2 y = 1$.
    
4. Substitute $\sin y = x$: $x^2 + \cos^2 y = 1 \implies \cos y = \sqrt{1-x^2}$.
    
5. **Result:** $\frac{d}{dx}(\arcsin x) = \frac{1}{\sqrt{1-x^2}}$.
    

### II. Derivative of Arctangent ($\arctan x$)

**Definition:** $\frac{d}{dx}(\arctan x) = \frac{1}{1+x^2}$

**Proof:**

1. Let $y = \arctan x$, therefore $\tan y = x$.
    
2. By the inverse rule: $\frac{dy}{dx} = \frac{1}{\sec^2 y}$.
    
3. Use the identity derived from the fundamental relationship: $\sec^2 y = 1 + \tan^2 y$.
    
4. Since $\tan y = x$, then $\sec^2 y = 1 + x^2$.
    
5. **Result:** $\frac{d}{dx}(\arctan x) = \frac{1}{1+x^2}$.
    

---

## 3. Solved Exercises (Chain Rule)

Processing these expressions requires differentiating through layers.

- **Exercise 1: Arcsine Chain Rule**
    
    Derive $f(x) = \arcsin(e^x)$.
    
    - **Outer Layer (Arcsine):** $\frac{1}{\sqrt{1 - (e^x)^2}}$
        
    - **Inner Layer ($e^x$):** $e^x$
        
    - **Result:** $\frac{e^x}{\sqrt{1 - e^{2x}}}$
        
- **Exercise 2: Quadratic Argument**
    
    Derive $f(x) = \arctan(3x^2)$.
    
    - **Outer Layer (Arctangent):** $\frac{1}{1 + (3x^2)^2}$
        
    - **Inner Layer ($3x^2$):** $6x$
        
    - **Result:** $\frac{6x}{1 + 9x^4}$
        

---

## 4. Symmetry and Notation

### The "Co-function" Adjustment

Derivatives of inverse functions starting with "C" follow the same logic as direct functions: they are assigned a negative sign.

- If $(\arcsin x)' = \frac{1}{\sqrt{1-x^2}}$, then **$(\arccos x)' = -\frac{1}{\sqrt{1-x^2}}$**.
    
- If $(\arctan x)' = \frac{1}{1+x^2}$, then **$(\text{arccotg } x)' = -\frac{1}{1+x^2}$**.
    

### Notation Warning: $\sin^{-1}(x) \neq \csc(x)$

It is a common mistake to confuse the inverse function with the reciprocal. Cosecant is not the inverse of sine; it does not return the original angle. This confusion stems from historical conventions:

- **Positive Exponents (2, 3, 4...):** Indicate powers, such as $\sin^2(x)$.
    
- **Negative Exponent (-1):** By mathematical convention, a $-1$ superscript on a function name denotes the **Inverse Function (Arc)**, not an arithmetic reciprocal.
    

Therefore, $\sin^{-1}(x)$ should always be interpreted as $\arcsin x$.