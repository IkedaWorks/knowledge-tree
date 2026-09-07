
# Briot-Ruffini & Polynomial Reduction

## Recommendations and Context

Briot-Ruffini is a tool for agility. It is extremely useful for saving time during exams, but it is a specialist: it only works for divisions by a linear binomial $(x - a)$.

> [!IMPORTANT]
> 
> **Golden Rule:** For the general case (dividing by any polynomial), master **Long Division**. Briot-Ruffini is your shortcut when you already know a root of the denominator and need to factor it to apply Partial Fraction Decomposition (PFD).

---

## Hunting for the Root: Where It All Begins

Before using the device, you need a root ($a$). How do you find it without struggling?

- **Master Tip (Sum of Coefficients):** If the sum of all coefficients of the polynomial is zero, then the number **1** is a guaranteed root.
    
    - _Why?_ Because $P(1)$ results in the sum of the coefficients. If $P(1) = 0$, then 1 is a root.
        
- **Rational Root Theorem:** If the sum is not zero, look at the constant term (the number without $x$). Possible integer roots are the divisors of that number.
    
    - _Example:_ For $P(x) = x^3 - 6x^2 + 11x - 6$, test the divisors of $-6$: $\{\pm 1, \pm 2, \pm 3, \pm 6\}$.
        
- **Remainder Theorem (Validation):** To confirm if a candidate is a root before setting up the device, simply calculate $P(a)$. If the result is 0, the root is valid.
    

---

## The Algorithm (Step-by-Step)

Let's divide $P(x) = x^3 - 6x^2 + 11x - 6$ by $(x - 1)$. Root $a = 1$.

### The Structure

Organize the root on the left and the coefficients of the dividend on the right:

|**Root (a)**|**x3**|**x2**|**x1**|**Constant**|
|---|---|---|---|---|
|**1**|1|-6|11|-6|
||↓||||
||**1**||||

### The Process: Drop, Multiply, and Add

1. **Drop:** The first coefficient (1) drops straight down.
    
2. **Multiply and Add:** Multiply the number that dropped by the root and add it to the next neighbor above.
    
    - $1 \cdot (1) + (-6) = \mathbf{-5}$
        
    - $-5 \cdot (1) + 11 = \mathbf{6}$
        
    - $6 \cdot (1) + (-6) = \mathbf{0}$ (The last number is always the **Remainder**).
        

### Reading the Result

The bottom line contains the coefficients of the new polynomial, which will always have **one degree less** than the original:

- **Coefficients:** $1, -5, 6$
    
- **New Polynomial:** $1x^2 - 5x + 6$
    

Now, the original expression $x^3 - 6x^2 + 11x - 6$ can be written as:

$$(x - 1)(x^2 - 5x + 6)$$

---

## The Workflow for Integration

This is the actual process for a Calculus problem:

1. **Investigation:** Is the denominator degree 3? Find the first root by inspection or the Rational Root Theorem.
    
2. **Execution:** Use Briot-Ruffini to reduce it to degree 2.
    
3. **Final Factoring:** Use the Quadratic Formula (Bhaskara) or Sum and Product on the resulting degree 2 polynomial.
    
    - _In our example:_ $x^2 - 5x + 6 \implies$ roots 2 and 3.
        
4. **PFD Setup:** Now you have three linear factors:
    
    $$\frac{\text{Numerator}}{(x-1)(x-2)(x-3)} = \frac{A}{x-1} + \frac{B}{x-2} + \frac{C}{x-3}$$
    
5. **Integration:** Solve as a sum of simple logarithms.