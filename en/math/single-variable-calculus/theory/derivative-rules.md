# Differentiation Rules

## 1. Definition and Intuition

Differentiation Rules are fundamental formulas derived from the repeated application of the formal definition of the derivative (Newton's limit). In practice, they function like a "dictionary": you identify the function's format and apply the corresponding rule to obtain the rate of change.

### The Shortcut Intuition

Instead of building a ladder (limit) every time you want to climb a step, you use an elevator (rule). The result is the same, but the calculation speed is infinitely higher.

---

## 2. The Golden Rules

Let $k$ be a constant and $u, v$ be functions of $x$.

### I. Constant Rule

If the function is a horizontal line, it has no slope.

- **Rule:** If $f(x) = k$, then $f'(x) = 0$.
    
- **Example:** If $f(x) = 10$, the variation is $0$.
    

### II. Power Rule

This is the most frequently used rule. The exponent "drops down" as a multiplier and decreases by one unit.

- **Rule:** If $f(x) = x^n$, then $f'(x) = n \cdot x^{n-1}$.
    
- **Example:** If $f(x) = x^3$, then $f'(x) = 3x^2$.
    

### III. Constant Multiple Rule

The constant "waits" for the differentiation to happen and then multiplies the final result.

- **Rule:** $\frac{d}{dx}[k \cdot u] = k \cdot u'$.
    
- **Example:** If $f(x) = 5x^4$, then $f'(x) = 5 \cdot (4x^3) = 20x^3$.
    

### IV. Sum and Difference Rule

The derivative of a sum is the sum of the derivatives (the derivative operator is linear).

- **Rule:** $(u \pm v)' = u' \pm v'$.
    
- **Example:** If $f(x) = x^2 + 3x$, then $f'(x) = 2x + 3$.
    

---

## 3. Practical Examples

### Example 1: Full Polynomial

**Calculate the derivative of** $f(x) = 4x^3 - 5x^2 + 8x - 12$.

- **Term 1 ($4x^3$):** The $3$ drops $\to 4 \cdot 3x^2 = 12x^2$.
    
- **Term 2 ($-5x^2$):** The $2$ drops $\to -5 \cdot 2x^1 = -10x$.
    
- **Term 3 ($8x$):** The $1$ drops $\to 8 \cdot 1x^0 = 8$ (Recall: $x^0 = 1$).
    
- **Term 4 ($-12$):** This is a constant $\to 0$.
    
- **Verdict:** $f'(x) = 12x^2 - 10x + 8$.
    

### Example 2: Root and Fraction (The Exponent Trick)

**Calculate the derivative of** $f(x) = \sqrt{x} + \frac{1}{x}$.

- **Transform to Power:** Rewrite as $f(x) = x^{1/2} + x^{-1}$.
    
- **Applying to $x^{1/2}$:** $\frac{1}{2}x^{(1/2 - 1)} = \frac{1}{2}x^{-1/2} = \frac{1}{2\sqrt{x}}$.
    
- **Applying to $x^{-1}$:** $-1x^{(-1 - 1)} = -1x^{-2} = -\frac{1}{x^2}$.
    
- **Verdict:** $f'(x) = \frac{1}{2\sqrt{x}} - \frac{1}{x^2}$.
    

---

## 4. The Concept of Interdependence

When two functions $u(x)$ and $v(x)$ are multiplied or divided, the variation of one affects the other. Therefore, the rule requires you to "take turns" differentiating: while one is differentiated, the other stays the same.

### I. Product Rule

Use this when one function is multiplied by another ($u \cdot v$).

- **Formula:** $(u \cdot v)' = u' \cdot v + u \cdot v'$.
    
- **Translation:** "Differentiate the first, keep the second + Keep the first, differentiate the second".
    
- **Example:** $f(x) = x^2 \cdot \sin(x)$.
    
    - **Identify:** $u = x^2$ and $v = \sin(x)$.
        
    - **Differentiate parts:** $u' = 2x$ and $v' = \cos(x)$.
        
    - **Result:** $f'(x) = 2x \cdot \sin(x) + x^2 \cdot \cos(x)$.
        

### II. Quotient Rule

Use this for the division of functions ($\frac{u}{v}$).

- **Formula:** $\left( \frac{u}{v} \right)' = \frac{u' \cdot v - u \cdot v'}{v^2}$.
    
- **Translation:** "Derivative of the top times the bottom minus the top times the derivative of the bottom, all over the bottom squared".
    
- **Example:** $f(x) = \frac{3x - 1}{x^2}$.
    
    - **Identify:** $u = 3x - 1$ and $v = x^2$.
        
    - **Differentiate parts:** $u' = 3$ and $v' = 2x$.
        
    - **Application:** $f'(x) = \frac{(3) \cdot (x^2) - (3x - 1) \cdot (2x)}{(x^2)^2}$.
        
    - **Simplification:** $f'(x) = \frac{3x^2 - (6x^2 - 2x)}{x^4} = \frac{-3x^2 + 2x}{x^4} = \frac{-3x + 2}{x^3}$.
        

---

## 5. Exercises Section

**Exercise 1 (Product):** $f(x) = e^x \cdot (x^3 + 2)$

- $u = e^x \to u' = e^x$
    
- $v = x^3 + 2 \to v' = 3x^2$
    
- **Result:** $f'(x) = e^x(x^3 + 2) + e^x(3x^2)$
    
- **Engineering Tip:** Factoring out: $f'(x) = e^x(x^3 + 3x^2 + 2)$.
    

**Exercise 2 (Quotient):** $f(x) = \frac{\ln(x)}{x}$

- $u = \ln(x) \to u' = 1/x$
    
- $v = x \to v' = 1$
    
- **Result:** $f'(x) = \frac{(1/x) \cdot x - \ln(x) \cdot 1}{x^2}$
    
- **Simplification:** $f'(x) = \frac{1 - \ln(x)}{x^2}$.