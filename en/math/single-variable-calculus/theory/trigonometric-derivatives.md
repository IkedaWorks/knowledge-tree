
# Derivatives of Trigonometric Functions

Mastering trigonometric derivatives requires a solid understanding of fundamental trigonometric identities and relationships.

---

## 1. Study Orientation

It is highly recommended to memorize the derivatives of **sine**, **cosine**, and **tangent**, as these serve as the building blocks for all other trigonometric functions. Avoid mechanical memorization of every formula; instead, prioritize understanding the derivation logic so you can reconstruct them if necessary.

---

## 2. Fundamental Premises

The following derivatives are assumed as known premises derived from fundamental limits:

- **Sine:** $\frac{d}{dx}(\sin x) = \cos x$
    
- **Cosine:** $\frac{d}{dx}(\cos x) = -\sin x$
    

---

## 3. Proofs of Derivative Functions

Using the Quotient and Chain rules, we can derive the remaining trigonometric functions:

### I. Derivative of Tangent

**Rule:** $\frac{d}{dx}(\tan x) = \sec^2 x$

- **Proof:** Use $\tan x = \frac{\sin x}{\cos x}$ and the Quotient Rule.
    
- The derivative of the numerator ($\cos x$) times the denominator ($\cos x$) gives $\cos^2 x$.
    
- Subtract the numerator ($\sin x$) times the derivative of the denominator ($-\sin x$), resulting in $+ \sin^2 x$.
    
- The denominator becomes $\cos^2 x$.
    
- By the Fundamental Trigonometric Identity ($\cos^2 x + \sin^2 x = 1$), the expression simplifies to $\frac{1}{\cos^2 x}$, which equals $\sec^2 x$.
    

### II. Derivative of Secant

**Rule:** $\frac{d}{dx}(\sec x) = \sec x \cdot \tan x$

- **Proof:** Rewrite $\sec x$ as $(\cos x)^{-1}$ and apply the Chain Rule.
    
- Differentiate the power: $-1 \cdot (\cos x)^{-2}$.
    
- Multiply by the inner derivative ($-\sin x$) to get $\frac{\sin x}{\cos^2 x}$.
    
- Decomposition: $\frac{1}{\cos x} \cdot \frac{\sin x}{\cos x} = \mathbf{\sec x \cdot \tan x}$.
    

### III. Derivative of Cotangent

**Rule:** $\frac{d}{dx}(\cot x) = -\csc^2 x$

- **Proof:** Apply the Quotient Rule to $\cot x = \frac{\cos x}{\sin x}$.
    
- The numerator becomes $(-\sin x \cdot \sin x) - (\cos x \cdot \cos x) = -(\sin^2 x + \cos^2 x) = -1$.
    
- With the denominator as $\sin^2 x$, the result is $\frac{-1}{\sin^2 x} = \mathbf{-\csc^2 x}$.
    

### IV. Derivative of Cosecant

**Rule:** $\frac{d}{dx}(\csc x) = -\csc x \cdot \cot x$

- **Proof:** Rewrite as $(\sin x)^{-1}$ and apply the Chain Rule.
    
- Differentiate the power: $-1 \cdot (\sin x)^{-2}$.
    
- Multiply by the inner derivative ($\cos x$) to get $-\frac{\cos x}{\sin^2 x}$.
    
- Decomposition: $-\frac{1}{\sin x} \cdot \frac{\cos x}{\sin x} = \mathbf{-\csc x \cdot \cot x}$.
    

---

## 4. Technical Exercises

### Exercise 1: Triple Chain Rule

**Function:** $f(x) = \sin^3(4x)$

- **Layer 1 (Power):** $3 \cdot [\sin(4x)]^2$
    
- **Layer 2 (Sine):** $\cos(4x)$
    
- **Layer 3 (Argument):** $4$
    
- **Result:** $f'(x) = 12 \sin^2(4x) \cos(4x)$
    

### Exercise 2: Product Rule

**Function:** $y = e^{x} \cdot \sec(2x)$

- **Application:** Apply the Product Rule and the Chain Rule to the secant term.
    
- **Result:** $y' = e^x \sec(2x) [1 + 2\tan(2x)]$
    

### Exercise 3: Composition with Radicals

**Function:** $f(x) = \sqrt{\tan(x^2)}$

- **Step 1 (Power):** $\frac{1}{2\sqrt{\tan(x^2)}}$
    
- **Step 2 (Tangent):** $\sec^2(x^2)$
    
- **Step 3 (Internal):** $2x$
    
- **Final Result:** $f'(x) = \frac{x \cdot \sec^2(x^2)}{\sqrt{\tan(x^2)}}$