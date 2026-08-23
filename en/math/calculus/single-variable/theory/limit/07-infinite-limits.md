---
id: infinite_limits
title: Limits at Infinity and Infinite Limits
---
# Limits at Infinity and Infinite Limits

The study of limits involving infinity analyzes two fundamental conditions: the trend of the output values $f(x)$ as the independent variable grows or decreases without bound ($x \to \pm\infty$), and the unbounded growth of $f(x)$ as the input approaches a critical point $a$ ($x \to a$).

> [!NOTE]
> 
> This graph node analyzes the algebraic behavior of functions in regions of infinite accumulation and infinite discontinuities:
> 
> - Indeterminate forms of type $\frac{\infty}{\infty}$ and $\infty - \infty$ are resolved through algebraic dominance analysis.
>     
> - The geometric interpretation of these results in function graphs is addressed in the **Asymptotes** node.
>     
> - For indeterminate forms of the type $1^\infty$, refer to the **Fundamental Exponential Limits** node.
>     

## Limits at Infinity ($x \to \pm\infty$) and Dominance Analysis

When the variable $x$ assumes arbitrarily large magnitude values, evaluating the limit requires identifying the dominant term within the expression.

### The Fundamental Identity of Zero Limits

For any real constant $k$ and any rational exponent $n > 0$, the limiting behavior of a ratio whose denominator grows without bound is given by:

$$\lim_{x \to \pm\infty} \frac{k}{x^n} = 0$$

This relation establishes that dividing a fixed quantity by an infinitely large quantity approaches zero.

### Method of Division by the Dominant Term

Indeterminate forms of the type $\frac{\infty}{\infty}$ in rational functions are resolved by factoring or dividing both the numerator and the denominator by the highest power of $x$ present in the denominator.

Consider evaluating the following limit:

$$\lim_{x \to \infty} \frac{2x^2 + 3}{5x^2 - x}$$

1. **Identifying the Highest Power in the Denominator:**
    
    The highest power of $x$ in the denominator is $x^2$.
    
2. **Normalizing the Ratio:**
    
    Divide every term in the numerator and denominator by $x^2$:
    
    $$\lim_{x \to \infty} \frac{\frac{2x^2}{x^2} + \frac{3}{x^2}}{\frac{5x^2}{x^2} - \frac{x}{x^2}} = \lim_{x \to \infty} \frac{2 + \frac{3}{x^2}}{5 - \frac{1}{x}}$$
    
3. **Applying Limit Properties:**
    
    Since $\lim_{x \to \infty} \frac{3}{x^2} = 0$ and $\lim_{x \to \infty} \frac{1}{x} = 0$:
    
    $$\frac{\lim_{x \to \infty} 2 + \lim_{x \to \infty} \frac{3}{x^2}}{\lim_{x \to \infty} 5 - \lim_{x \to \infty} \frac{1}{x}} = \frac{2 + 0}{5 - 0} = \frac{2}{5}$$
    

## Infinite Limits ($x \to a$) and One-Sided Sign Analysis

An infinite limit occurs when $f(x)$ grows or decreases without bound in the neighborhood of a point $x = a$. In these cases, the denominator approaches zero while the numerator approaches a non-zero constant $k \neq 0$.

### The Identity of Unbounded Growth

If $k > 0$, the behavior of the limit depends strictly on the sign of the denominator as it approaches zero:

$$\lim_{x \to a} \frac{k}{(x - a)^n} = \pm\infty$$

> [!IMPORTANT]
> 
> The expression $\frac{k}{0}$ (with $k \neq 0$) is not an algebraic indeterminate form. It signals divergence toward $+\infty$ or $-\infty$. The correct sign of infinity is determined strictly through one-sided limit analysis.

### One-Sided Limit Analysis

Consider evaluating the one-sided limit:

$$\lim_{x \to 2^+} \frac{1}{x - 2}$$

1. **Analyzing Denominator Behavior:**
    
    As $x \to 2^+$, the variable $x$ approaches $2$ strictly from values greater than $2$ ($x > 2$).
    
2. **Determining Neighborhood Sign:**
    
    Under the condition $x > 2$, the difference $(x - 2)$ is strictly positive ($x - 2 > 0$). The denominator is noted to approach zero through positive values ($0^+$).
    
3. **Formal Conclusion:**
    
    The ratio between a positive constant and a positive infinitesimal quantity results in positive divergence:
    
    $$\lim_{x \to 2^+} \frac{1}{x - 2} = +\infty$$
    

For even powers in the denominator, the term $(x - a)^n$ yields strictly positive values for all $x \neq a$, ensuring that $\lim_{x \to a} \frac{1}{(x - a)^n} = +\infty$ for even $n$, regardless of whether the approach occurs from the left or the right.

## Worked Examples and Boundary Cases

### Example 1: Dominance with Radicals and Critical Sign Analysis ($x \to -\infty$)

Evaluate the limit:

$$\lim_{x \to -\infty} \frac{\sqrt{4x^2 + 1}}{3x - 2}$$

1. **Dominance Analysis:**
    
    Under the radical, the dominant term is $x^2$. Since $\sqrt{x^2} = \vert{}x\vert{}$, the expression behaves linearly at infinity.
    
2. **Factorization and Radical Extraction:**
    
    Factor $x^2$ inside the root:
    
    $$\sqrt{4x^2 + 1} = \sqrt{x^2 \left(4 + \frac{1}{x^2}\right)} = \vert{}x\vert{} \sqrt{4 + \frac{1}{x^2}}$$
    
3. **Applying the Negative Domain ($x \to -\infty$):**
    
    Since $x$ takes strictly negative values ($x < 0$), we apply the definition $\vert{}x\vert{} = -x$:
    
    $$\lim_{x \to -\infty} \frac{-x \sqrt{4 + \frac{1}{x^2}}}{x \left(3 - \frac{2}{x}\right)}$$
    
4. **Simplification and Re-evaluation:**
    
    Canceling the factor $x \neq 0$:
    
    $$\lim_{x \to -\infty} \frac{-\sqrt{4 + \frac{1}{x^2}}}{3 - \frac{2}{x}} = \frac{-\sqrt{4 + 0}}{3 - 0} = -\frac{2}{3}$$
    

### Example 2: One-Sided Infinite Limit with Polynomial Factorization

Evaluate the one-sided limit:

$$\lim_{x \to 3^-} \frac{2x}{x^2 - 5x + 6}$$

1. **Direct Substitution Test:**
    
    Substituting $x = 3$ yields $\frac{2(3)}{3^2 - 5(3) + 6} = \frac{6}{0}$, confirming infinite divergence.
    
2. **Factoring the Denominator:**
    
    Factor the quadratic into its roots: $x^2 - 5x + 6 = (x - 3)(x - 2)$.
    
    $$\lim_{x \to 3^-} \frac{2x}{(x - 3)(x - 2)}$$
    
3. **Neighborhood Sign Analysis ($x \to 3^-$):**
    
    For $x \to 3^-$, consider $x < 3$:
    
    - Numerator: $2x \to 6 > 0$ (positive).
        
    - Factor $(x - 2) \to (3 - 2) = 1 > 0$ (positive).
        
    - Factor $(x - 3)$: since $x < 3$, the difference is strictly negative ($x - 3 < 0$), approaching zero through negative values ($0^-$).
        
4. **Conclusion by Resulting Sign:**
    
    The denominator is the product of a positive number and a negative infinitesimal, resulting in $0^-$:
    
    $$\lim_{x \to 3^-} \frac{2x}{(x - 3)(x - 2)} = \frac{+6}{0^-} = -\infty$$
