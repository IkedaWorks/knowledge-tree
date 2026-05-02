
# Derivatives of Exponentials and Logarithms

The derivatives of exponential and logarithmic functions often involve a scale adjustment known as the **"$\ln(a)$ Toll"**. This adjustment ensures the growth rate is calibrated to the natural scale.

---

## 1. The General Exponential Function

For any base $a > 0$ and $a \neq 1$, the derivative follows this logic:

$$\frac{d}{dx}(a^x) = a^x \cdot \ln(a)$$

- **The Logic:** The function repeats itself ($a^x$), but we multiply by the natural logarithm of the base ($\ln(a)$) to adjust the growth rate.
    
- **The Specific Case ($e^x$):** If the base is $e$, the derivative would be $e^x \cdot \ln(e)$. Since $\ln(e) = 1$, the "toll" becomes invisible, making $e^x$ its own derivative.
    

> [!WARNING]
> 
> **Existence Condition:** The base $a$ must be greater than zero ($a > 0$) and not equal to 1 for the function to be well-defined and non-constant.

---

## 2. The General Logarithm

For any valid base $a$, the derivative is defined as:

$$\frac{d}{dx}(\log_a x) = \frac{1}{x \cdot \ln(a)}$$

- **The Logic:** The derivative is always the inverse of the variable ($1/x$), but we divide by $\ln(a)$ to adjust for the specific base.
    
- **The Specific Case ($\ln x$):** When the base is $e$, the formula results in $\frac{1}{x \cdot \ln(e)} = \frac{1}{x}$.
    

> [!NOTE]
> 
> **Domain and Conditions:**
> 
> - **Base ($a$):** Must be $a > 0$ and $a \neq 1$.
>     
> - **Argument ($x$):** Must be $x > 0$, as no real exponent results in zero or a negative number from a positive base.
>     

---

## 3. Practical Examples with "Non-Friendly" Bases

- **Example 1 (Base 10):** $f(x) = 10^x \implies f'(x) = 10^x \cdot \ln(10)$.
    
- **Example 2 (Base 2):** $f(x) = \log_2(x) \implies f'(x) = \frac{1}{x \ln(2)}$.
    
- **Example 3 (Chain Rule Mixture):** $f(x) = 3^{\sin(x)}$.
    
    - **Derivative of base 3:** $3^{\sin(x)} \cdot \ln(3)$.
        
    - **Multiply by the exponent's derivative (Chain Rule):** $\cos(x)$.
        
    - **Final Result:** $f'(x) = 3^{\sin(x)} \cdot \ln(3) \cdot \cos(x)$.
        

---

## 4. Structural Mental Filters

To avoid relying on limit deductions during exams, use these mental shortcuts:

- **The Multiplier Filter (Exponential):** If the variable $x$ is in the exponent, the function grows quickly.
    
    - **Action:** Copy the function and multiply by the "toll" $\ln(a)$.
        
- **The Divisor Filter (Logarithm):** If the variable $x$ is inside the logarithm, the function grows slowly.
    
    - **Action:** Use the inverse $1/x$ and divide by the "toll" $\ln(a)$ (putting $\ln(a)$ in the denominator).
        
- **The "Anchor" of $\ln(x)$:** If in doubt, remember that $\ln(x)$ has base $e$. Since its derivative is $1/x$, any other logarithm is just a "close relative" adjusted by the factor $\frac{1}{\ln(\text{base})}$.