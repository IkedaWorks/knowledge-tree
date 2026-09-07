
# Proof: Validity of Partial Fraction Decomposition

## The Intuition: The Reverse LCD

In primary school, we learn to combine distinct fractions into a single expression using the Least Common Denominator (LCD). In Calculus, Partial Fractions do the opposite: they "disassemble" a final result to find the original pieces.

- **The Analogy:** Imagine the integral as a machine that cannot process "glued objects" (fractions with complex denominators). PFD is the tool that unglues these objects into simple pieces (first-degree fractions) that the machine processes instantly as **Natural Logarithms** ($\ln$).
    

> [!IMPORTANT]
> 
> **The Guarantee:** If algebra allows us to sum two fractions to arrive at one, it also guarantees that a unique path back exists.

---

## The Formal Proof: Two Pillars

The validity of the method rests on the combination of an algebraic theorem and a fundamental property of calculus.

### Pillar A: Fundamental Theorem of Algebra (Existence and Uniqueness)

Given a rational function $f(x) = \frac{P(x)}{Q(x)}$, where $\text{degree of } P < \text{degree of } Q$:

1. **Factorization:** The Fundamental Theorem of Algebra guarantees that every polynomial $Q(x)$ can be factored into linear terms $(x - r)$ or irreducible quadratic terms.
    
2. **Algebraic Identity:** The Partial Fraction Theorem states that there exists a unique set of constants ($A, B, C...$) such that:
    
    $$\frac{P(x)}{(x-r_1)(x-r_2)} \equiv \frac{A}{x-r_1} + \frac{B}{x-r_2}$$
    
3. **Proof of Uniqueness:** By multiplying by the common denominator, we arrive at a system of $n$ linear equations with $n$ unknowns. Since the terms $(x-r)$ are linearly independent, this system always possesses a **unique solution**.
    

### Pillar B: Linearity of the Integral Operator

Once it is algebraically proven that the complex fraction is identically equal to the sum of simple fractions, we apply the property of **linearity of the integral**:

$$\int \left( \sum_{i=1}^{n} \frac{A_i}{x-r_i} \right) dx = \sum_{i=1}^{n} \int \frac{A_i}{x-r_i} \, dx$$

Since the integral of a sum is the sum of the integrals, and the antiderivative of $\frac{1}{x-r}$ is proven to be $\ln|x-r|$ (via simple $u$-substitution where $u = x-r$), the technique is formally validated.

---

## Conclusion: Why is this proof complex?

This demonstration requires you to connect three different worlds:

- **Polynomial Algebra:** To factor and guarantee the existence of roots.
    
- **Linear Algebra:** To understand that the coefficients $A, B, C$ come from a system that always has a solution.
    
- **Integral Calculus:** To apply linearity and the FTC.