
# Limits Review: Step-by-Step Resolutions

This note contains detailed resolutions for problems ranging from easy to medium difficulty. The focus is on the **attack strategy** rather than just the final result.

---

###  1. The Geometric Limit (Arc-Chord Connection)

**Problem:** Calculate $\lim_{x \to 0} \frac{1 - \cos(x)}{x^2}$

- **The Strategy:** Multiply by the conjugate to transform cosine into sine.
    
- **Step-by-Step:**
    
    1. Multiply the numerator and denominator by $(1 + \cos x)$:
        
        $$\lim_{x \to 0} \frac{(1 - \cos x)(1 + \cos x)}{x^2(1 + \cos x)}$$
        
    2. Use the Trigonometric Identity $(1 - \cos^2 x = \sin^2 x)$:
        
        $$\lim_{x \to 0} \frac{\sin^2 x}{x^2(1 + \cos x)}$$
        
    3. Isolate the Fundamental Limit:
        
        $$\left( \lim_{x \to 0} \frac{\sin x}{x} \right)^2 \cdot \lim_{x \to 0} \frac{1}{1 + \cos x}$$
        
    4. Apply the values: $(1)^2 \cdot \frac{1}{1 + 1} = 1 \cdot \frac{1}{2}$.
        
- **Verdict:** **1/2** (this value is the basis for proving the derivative of the cosine).
    

---

###  2. The "Magic" of Euler Substitution

**Problem:** Calculate $\lim_{x \to \infty} \left( \frac{x + 6}{x + 1} \right)^{x+3}$

- **The Strategy:** Transform into base $e$ using the form $\lim (1 + 1/u)^u$.
    
- **Step-by-Step:**
    
    1. Manipulate the interior fraction: $\frac{x+1+5}{x+1} = 1 + \frac{5}{x+1}$.
        
    2. We now have $\lim_{x \to \infty} (1 + \frac{5}{x+1})^{x+3}$.
        
    3. Force the exponent to be the inverse of the internal term ($\frac{x+1}{5}$):
        
        $$\left[ \left( 1 + \frac{5}{x+1} \right)^{\frac{x+1}{5}} \right]^{\frac{5}{x+1} \cdot (x+3)}$$
        
    4. The term inside the brackets tends toward $e$. Now, calculate the limit of the new exponent:
        
        $$\lim_{x \to \infty} \frac{5(x+3)}{x+1} = \lim_{x \to \infty} \frac{5x+15}{x+1} = 5$$
        
- **Verdict:** **$e^5$**.
    

---

###  3. Double Exponential Manipulation

**Problem:** Calculate $\lim_{x \to 0} \frac{a^x - b^x}{x}$

- **The Strategy:** Make the structure of the Fundamental Exponential Limit ($\frac{a^x-1}{x}$) appear.
    
- **Step-by-Step:**
    
    1. **"Zero Addition Trick"**: Subtract and add 1 in the numerator:
        
        $$\lim_{x \to 0} \frac{(a^x - 1) - (b^x - 1)}{x}$$
        
    2. Separate into two fractions:
        
        $$\lim_{x \to 0} \frac{a^x - 1}{x} - \lim_{x \to 0} \frac{b^x - 1}{x}$$
        
    3. Apply the definition ($\ln a$ and $\ln b$): $\ln(a) - \ln(b)$.
        
    4. Use logarithmic properties: $\ln(a/b)$.
        
- **Verdict:** **$\ln(a/b)$**.
    

---

###  4. The Squeeze Theorem with Floor Function (JEE Standard)

**Problem:** Calculate $\lim_{x \to \infty} \frac{\lfloor x \rfloor}{x}$, where $\lfloor x \rfloor$ is the floor (integer part) of $x$.

- **The Strategy:** Use the definition of the step function to squeeze the limit.
    
- **Step-by-Step:**
    
    1. Definition: $x - 1 < \lfloor x \rfloor \le x$.
        
    2. Divide everything by $x$ (since $x \to \infty$, $x$ is positive):
        
        $$\frac{x-1}{x} < \frac{\lfloor x \rfloor}{x} \le \frac{x}{x}$$
        
    3. Calculate the limits at the endpoints:
        
        - Left: $\lim_{x \to \infty} \frac{x-1}{x} = 1$.
            
        - Right: $\lim_{x \to \infty} \frac{x}{x} = 1$.
            
- **Verdict:** By the Squeeze Theorem, the limit is **1**.
    

---

###  5. Limit with High-Order Conjugate Root

**Problem:** Calculate $\lim_{x \to 7} \frac{\sqrt{x+2} - 3}{x - 7}$

- **The Strategy:** Eliminate the root causing the $0/0$ form using the conjugate.
    
- **Step-by-Step:**
    
    1. Multiply by the conjugate $\sqrt{x+2} + 3$:
        
        $$\lim_{x \to 7} \frac{(\sqrt{x+2} - 3)(\sqrt{x+2} + 3)}{(x - 7)(\sqrt{x+2} + 3)}$$
        
    2. The numerator becomes a Difference of Squares: $(x+2) - 9 = x - 7$.
        
    3. Simplify the problematic term:
        
        $$\lim_{x \to 7} \frac{x - 7}{(x - 7)(\sqrt{x+2} + 3)} = \lim_{x \to 7} \frac{1}{\sqrt{x+2} + 3}$$
        
    4. Substitute $x=7$: $\frac{1}{\sqrt{9} + 3} = \frac{1}{3+3}$.
        
- **Verdict:** **1/6**.