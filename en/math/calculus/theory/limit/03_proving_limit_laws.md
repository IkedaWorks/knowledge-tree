
# Proving Limit Laws: The Formal Foundation

Proving limit laws means demonstrating that controlling the input error ($\delta$) is sufficient to guarantee output precision ($\epsilon$), even when combining two different functions.

##  The "Coupled Gear" Intuition

Imagine two independent machines ($f$ and $g$). If both are precise, their combination (sum or product) must also be precise. The challenge of a formal proof is discovering the new "adjustment" ($\delta_{total}$) that satisfies the requirements of both machines simultaneously.

##  Formalization of Proofs

For all proofs below, we start with the premise that the individual limits exist:

- $\lim_{x \to a} f(x) = L$ (For any $\epsilon_f > 0$, there exists $\delta_f$).
    
- $\lim_{x \to a} g(x) = M$ (For any $\epsilon_g > 0$, there exists $\delta_g$).
    

### 1. Sum Law Proof: $\lim [f(x) + g(x)] = L + M$

- **The Target:** We want to guarantee that $|(f(x) + g(x)) - (L + M)| < \epsilon$.
    
- **The Maneuver (Triangle Inequality):** We use the mathematical property stating that the absolute value of a sum is less than or equal to the sum of the absolute values: $|(f(x) - L) + (g(x) - M)| \leq |f(x) - L| + |g(x) - M|$.
    
- **The Proof:**
    
    - We choose an individual error of $\epsilon/2$ for each function.
        
    - By definition, there exist $\delta_1$ and $\delta_2$ such that $|f(x)-L| < \epsilon/2$ and $|g(x)-M| < \epsilon/2$.
        
    - By choosing the most restrictive one, $\delta = \min(\delta_1, \delta_2)$, we guarantee that both conditions are satisfied: $|f(x)-L| + |g(x)-M| < \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon$.
        
- **Conclusion:** The limit of a sum is rigorously the sum of the limits.
    

### 2. Constant Multiple Law Proof: $\lim [k \cdot f(x)] = k \cdot L$

- **The Target:** $|k \cdot f(x) - k \cdot L| < \epsilon$.
    
- **The Maneuver:** We factor out the constant: $|k| \cdot |f(x) - L| < \epsilon$.
    
- **The Proof:**
    
    - We need the distance between the function and its target to be: $|f(x) - L| < \frac{\epsilon}{|k|}$.
        
    - Since we know that $\lim f(x) = L$, the limit definition guarantees that a $\delta$ exists for any error challenge, including the specific value $\frac{\epsilon}{|k|}$.
        
- **Conclusion:** The constant merely scales the error (like amplifier gain), but it does not prevent the limit's convergence.
    

##  Engineer's Insight

In formal proofs, using $\min(\delta_1, \delta_2, \dots)$ is like designing a fault-tolerant system: you identify the most sensitive component (the smallest delta) and adjust the entire system based on it to ensure everything stays within the safety margin ($\epsilon$).

> [!TIP]
> 
> **Feynman Style:** The Triangle Inequality basically says that "the direct path between two points is always less than or equal to the sum of the deviations". If the deviations are small, the total distance will be as well.