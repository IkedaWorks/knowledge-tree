---
id: indeterminate-forms-limits
title: Indeterminate Forms in Limits
---

# Indeterminate Forms in Limits and Algebraic Techniques

When applying the operational properties of limits, direct evaluation by simple substitution in a function can result in an expression whose numerical value cannot be determined immediately. This occurrence is referred to as a mathematical indeterminate form.

An indeterminate form does not indicate that the limit does not exist or that the problem is unsolvable. It merely represents a failure of the direct substitution method, signaling that the function must be rewritten in an algebraically equivalent form within a neighborhood of the point to reveal its true limiting behavior.

> [!NOTE]
> 
> This graph node strictly focuses on the local algebraic indeterminate form $\frac{0}{0}$ and its resolution techniques via factorization and rationalization. Other indeterminate forms are analyzed in specific downstream nodes:
> 
> - Forms $\frac{\infty}{\infty}$ and $\infty - \infty$: developed in the **Infinite Limits and Asymptotes** node.
>     
> - Form $1^\infty$: developed in the **Fundamental Exponential Limits** node.
>     
> - Forms $0^0$, $\infty^0$, and $0 \cdot \infty$: developed in the **Derivatives** module via L'Hôpital's Rule.
>     

## Diagnosing the $\frac{0}{0}$ Indeterminate Form

In the study of local limits, the most fundamental indeterminate form occurs in the ratio of two functions when direct substitution at $x = a$ yields:

$$\lim_{x \to a} \frac{f(x)}{g(x)} = \frac{0}{0}$$

This expression indicates that both the numerator $f(x)$ and the denominator $g(x)$ approach zero simultaneously as $x$ approaches $a$.

> [!IMPORTANT]
> 
> The expression $\frac{0}{0}$ is not a real number, nor is it equal to $1$ or $0$. It represents a limiting ratio between two infinitesimal quantities. The value of the limit depends on which of the two functions approaches zero faster in the neighborhood of $a$.

Because the formal definition of a limit strictly analyzes points in the domain where $x \neq a$, we can algebraically manipulate the function to eliminate the factors responsible for the simultaneous vanishing before re-evaluating the limit.

## Resolution via Polynomial Factorization

When $f(x)$ and $g(x)$ are polynomials and direct substitution at $x = a$ results in the indeterminate form $\frac{0}{0}$, the Factor Theorem guarantees that the term $(x - a)$ is a common factor of both polynomials.

This property allows factoring the numerator and the denominator to simplify the critical term $(x - a)$, an operation that is perfectly valid for all $x \neq a$.

### Practical Application: Polynomial Factorization

Consider evaluating the following limit:

$$\lim_{x \to 2} \frac{x^2 - 4}{x^2 - 3x + 2}$$

1. **Direct Substitution Test:**
    
    Substituting $x = 2$ yields $\frac{2^2 - 4}{2^2 - 3(2) + 2} = \frac{0}{0}$, confirming the indeterminate form.
    
2. **Factorization of Terms:**
    
    We factor the numerator as a difference of squares and the denominator by identifying its roots:
    
    $$x^2 - 4 = (x - 2)(x + 2)$$
    
    $$x^2 - 3x + 2 = (x - 2)(x - 1)$$
    
3. **Cancellation of the Critical Factor:**
    
    Because the condition $x \to 2$ establishes that $x \neq 2$, dividing by the term $(x - 2)$ is algebraically valid:
    
    $$\lim_{x \to 2} \frac{(x - 2)(x + 2)}{(x - 2)(x - 1)} = \lim_{x \to 2} \frac{x + 2}{x - 1}$$
    
4. **Re-evaluation of the Limit:**
    
    Applying direct substitution to the simplified expression:
    
    $$\lim_{x \to 2} \frac{x + 2}{x - 1} = \frac{2 + 2}{2 - 1} = 4$$
    

## Resolution via Radical Rationalization

The $\frac{0}{0}$ indeterminate form also frequently arises in irrational expressions containing radicals in the numerator or denominator. In these cases, factorization by direct inspection is not applicable.

The rationalization technique consists of multiplying the numerator and the denominator by the conjugate of the radical expression. This procedure uses the difference of squares identity, $(A - B)(A + B) = A^2 - B^2$, to eliminate the radical and expose the critical factor responsible for the indeterminacy.

### Practical Application: Rationalization with Conjugates

Consider evaluating the following limit:

$$\lim_{x \to 0} \frac{\sqrt{x + 9} - 3}{x}$$

1. **Direct Substitution Test:**
    
    Substituting $x = 0$ yields $\frac{\sqrt{0 + 9} - 3}{0} = \frac{0}{0}$.
    
2. **Multiplication by the Conjugate:**
    
    The conjugate of the numerator expression $(\sqrt{x + 9} - 3)$ is $(\sqrt{x + 9} + 3)$. We multiply the numerator and denominator by this term:
    
    $$\lim_{x \to 0} \left( \frac{\sqrt{x + 9} - 3}{x} \cdot \frac{\sqrt{x + 9} + 3}{\sqrt{x + 9} + 3} \right)$$
    
3. **Algebraic Expansion:**
    
    Applying the special product formula in the numerator:
    
    $$\lim_{x \to 0} \frac{(\sqrt{x + 9})^2 - (3)^2}{x(\sqrt{x + 9} + 3)} = \lim_{x \to 0} \frac{(x + 9) - 9}{x(\sqrt{x + 9} + 3)} = \lim_{x \to 0} \frac{x}{x(\sqrt{x + 9} + 3)}$$
    
4. **Cancellation of the Critical Factor and Final Evaluation:**
    
    Simplifying the factor $x$ for the condition $x \neq 0$:
    
    $$\lim_{x \to 0} \frac{1}{\sqrt{x + 9} + 3} = \frac{1}{\sqrt{0 + 9} + 3} = \frac{1}{3 + 3} = \frac{1}{6}$$