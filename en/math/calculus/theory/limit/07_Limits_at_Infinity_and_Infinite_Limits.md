
# Limits at Infinity and Infinite Limits

This note explores the behavior of functions at their extremes: when the input ( $x$ ) grows without bound or when the output ( $f(x)$ ) explodes toward immeasurable values.

##  Fundamental Identities

To resolve these limits rigorously, we rely on two fundamental identities:

- **The Horizon Identity ($x \to \infty$):**
    
    $$\lim_{x \to \infty} \frac{k}{x^n} = 0$$
    
    (A fixed number $k$ divided by something that grows without bound tends toward zero).
    
- **The Explosion Identity ($x \to a$):**
    
    $$\lim_{x \to a} \frac{k}{(x-a)^n} = \pm \infty$$
    
    (A fixed number $k$ divided by something that decreases to almost zero explodes toward infinity).
    

---

##  How to Apply: Limits at Infinity ($x \to \infty$)

The objective here is to force the appearance of terms in the form $k/x^n$ so they become zero.

**Resolution Algorithm:**

1. **Identify** the highest power of $x$ present in the denominator.
    
2. **Divide** all terms in both the numerator and the denominator by that value.
    

**Example:** Calculate $\lim_{x \to \infty} \frac{2x^2 + 3}{5x^2 - x}$

- **Division by the highest power ($x^2$):**
    
    $$\lim_{x \to \infty} \frac{\frac{2x^2}{x^2} + \frac{3}{x^2}}{\frac{5x^2}{x^2} - \frac{x}{x^2}}$$
    
- **Simplification:**
    
    $$\lim_{x \to \infty} \frac{2 + \frac{3}{x^2}}{5 - \frac{1}{x}}$$
    
- **Identity Application:**
    
    $$\frac{2 + 0}{5 - 0} = \frac{2}{5}$$
    

---

##  How to Apply: Infinite Limits ($x \to a$)

In this case, $x$ tends toward a real number, but the denominator tends toward zero, resulting in division by "almost nothing".

**Example:** Calculate $\lim_{x \to 2^+} \frac{1}{x-2}$

1. **Trend Analysis:** If $x=2$, we have $1/0$, which indicates an infinite result ($\infty$).
    
2. **Sign Analysis (One-Sided):** Since $x \to 2^+$, we take values slightly larger than 2 (e.g., 2.1, 2.01).
    
3. **Formalization:** If $x > 2$, then $(x-2) > 0$.
    
4. **Result:** Therefore, $\frac{1}{\text{small positive}} \to +\infty$.
    

---

##  Shortcuts

- **At Infinity ($x \to \infty$):**
    
    - If the result is 0, it is because an $x$ remained in the denominator after simplification.
        
    - If the result is $\infty$, it is because an $x$ remained in the numerator.
        
- **At the Critical Point ($x \to a$):** The limit will only result in $\pm \infty$ if the numerator is not zero. If it is $0/0$, it is an indeterminate form requiring prior factoring.
    
- **The Even Power Rule:** $\lim_{x \to a} \frac{1}{(x-a)^n}$ where $n$ is even will always be $+\infty$, regardless of the side, because even powers eliminate negative signs.
    

> [!IMPORTANT]
> 
> **Definition of Asymptote:**
> 
> - If $\lim_{x \to \pm \infty} f(x) = L$, then **$y = L$** is a **Horizontal Asymptote**.
>     
> - If $\lim_{x \to a^{\pm}} f(x) = \pm \infty$, then **$x = a$** is a **Vertical Asymptote**.
>
