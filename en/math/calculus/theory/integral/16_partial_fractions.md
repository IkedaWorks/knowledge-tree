
# Partial Fraction Decomposition (PFD)

## Definition and Intuition

**PFD** is an algebraic technique used to "disassemble" a fraction whose denominator is a polynomial that is difficult to integrate. The objective is to transform a single complex fraction into a sum of simple fractions, typically of the form $1/(x+a)$, whose integral almost always results in a **Natural Logarithm** ($\ln$).

- **Condition for Use:** The degree of the numerator must be strictly less than the degree of the denominator. If the denominator can be factored, the technique is applicable.
    

---

## Resolution Protocol (Linear Factors)

1. **Factoring the Denominator:** Transform the polynomial into a product of simple terms.
    
    - _Example:_ $x^2 + x \implies x(x + 1)$.
        
2. **Setting up the Identity:** Assign a constant ($A, B, \dots$) to each factor.
    
    $$\frac{1}{x(x+1)} = \frac{A}{x} + \frac{B}{x+1}$$
    
3. **Calculating Coefficients (Method of Zeros):** Eliminate denominators by multiplying the entire equation by the LCD (Least Common Denominator) and choose values of $x$ that zero out terms to isolate the constants.
    
    $$1 = A(x+1) + Bx$$
    
    - If $x = 0 \implies \mathbf{A = 1}$
        
    - If $x = -1 \implies \mathbf{B = -1}$
        
4. **Final Integration:** Integrate the simplified terms.
    
    $$\int \frac{1}{x} \, dx - \int \frac{1}{x+1} \, dx = \ln|x| - \ln|x+1| + C$$
    

---

## The Degree Problem (Improper Fractions)

If the degree of the numerator is $\ge$ to the degree of the denominator, PFD cannot be applied directly. You must perform **Polynomial Division** first.

**The Identity Proof:**

You already know that: $\text{Dividend} = (\text{Divisor} \cdot \text{Quotient}) + \text{Remainder}$.

By dividing this entire equation by the Divisor, we obtain the identity used in Calculus:

$$\frac{P(x)}{Q(x)} = \text{Quotient}(x) + \frac{\text{Remainder}(x)}{Q(x)}$$

> [!NOTE]
> 
> Integrating the Quotient is simple (it is a polynomial). PFD only comes into play to solve the remaining fraction ($\frac{\text{Remainder}}{\text{Divisor}}$), which is now a proper fraction.

---

## Solved Exercise: Complete Integration

**Problem:** Calculate $\int \frac{x^2 + 1}{x^2 - x} \, dx$

1. **Division (Equal Degrees):**
    
    $$\frac{x^2 + 1}{x^2 - x} = 1 + \frac{x+1}{x^2-x}$$
    
2. **PFD on the Remainder:**
    
    $$\frac{x+1}{x(x-1)} = \frac{A}{x} + \frac{B}{x-1} \implies x+1 = A(x-1) + Bx$$
    
    - If $x = 0 \implies \mathbf{A = -1}$
        
    - If $x = 1 \implies \mathbf{B = 2}$
        
3. **Final Assembly:**
    
    $$\int 1 \, dx + \int \frac{-1}{x} \, dx + \int \frac{2}{x-1} \, dx$$
    
4. **Result:** $x - \ln|x| + 2\ln|x-1| + C$
    

---

## 💡 Special Cases: Arctangent

If the denominator is a second-degree polynomial that has no real roots (such as $x^2 + 4$), PFD does not result in a $\ln$, but rather an **Arctangent**:

$$\int \frac{1}{x^2 + a^2} \, dx = \frac{1}{a} \arctan\left(\frac{x}{a}\right) + C$$