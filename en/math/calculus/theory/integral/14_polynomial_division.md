# Polynomial Division

## Introduction and Context

Polynomial division is an essential pre-calculus tool for integrating **Rational Functions** (fractions of polynomials).

- **When to use:** Whenever you have a fraction where the **degree of the Numerator $\ge$ degree of the Denominator**. In these cases, the fraction is called "improper" and must be simplified before integration.
    

---

## The Division Algorithm (Long Division Method)

The process seeks to write the relationship:

$$\frac{\text{Dividend}}{\text{Divisor}} = \text{Quotient} + \frac{\text{Remainder}}{\text{Divisor}}$$

**Step-by-Step:**

1. **Ordering:** Write the polynomials in descending order of power.
    
2. **Leading Division:** Divide the leading term (highest degree) of the dividend by the leading term of the divisor.
    
3. **Multiplication and Subtraction:** Multiply the result by the entire divisor and subtract it from the dividend (invert the signs).
    
4. **Repetition:** Repeat the process with the new resulting polynomial until the degree of the remainder is less than the degree of the divisor.
    

---

## Complete Example

Let's divide: $\frac{x^3 + 2x + 1}{x - 1}$

1. **First Term:** $x^3 \div x = \mathbf{x^2}$.
    
    - Multiply: $x^2(x - 1) = x^3 - x^2$.
        
    - Subtract: $(x^3 + 2x + 1) - (x^3 - x^2) = \mathbf{x^2 + 2x + 1}$.
        
2. **Second Term:** $x^2 \div x = \mathbf{x}$.
    
    - Multiply: $x(x - 1) = x^2 - x$.
        
    - Subtract: $(x^2 + 2x + 1) - (x^2 - x) = \mathbf{3x + 1}$.
        
3. **Third Term:** $3x \div x = \mathbf{3}$.
    
    - Multiply: $3(x - 1) = 3x - 3$.
        
    - Subtract: $(3x + 1) - (3x - 3) = \mathbf{4}$ (Remainder).
        

**Final Structure:**

$$\frac{x^3 + 2x + 1}{x - 1} = x^2 + x + 3 + \frac{4}{x - 1}$$

---

## Application in Integral Calculus

Division transforms an impossible integral into a sum of simple integrals:

- The **Quotient** becomes a polynomial integral (Power Rule).
    
- The **Remainder/Divisor** usually results in a Logarithm or Arctangent.
    

**Integration Example:**

$$\int \frac{x^3 + 2x + 1}{x - 1} \, dx = \int \left( x^2 + x + 3 + \frac{4}{x - 1} \right) \, dx$$

**Final Result:**

$$\frac{x^3}{3} + \frac{x^2}{2} + 3x + 4\ln|x - 1| + C$$

---

##  Tips and Curiosities

- **Synthetic Division (Briot-Ruffini):** If your divisor is of the type $(x - a)$, you can use the practical Briot-Ruffini device to save time. It is much faster than the long division method!
    
- **Factoring "Hacks":** If you notice that the numerator can be factored (e.g., a difference of squares), you can simplify the fraction directly without needing long division.
    
- **Fundamental Theorem of Algebra:** This theorem guarantees that every polynomial of degree $n$ has exactly $n$ roots (real or complex). This is the basis that allows us to factor any polynomial for use in Partial Fractions.