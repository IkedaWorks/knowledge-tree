
# Proof: Derivatives of Logarithm and Exponential Functions

The following proofs rely on fundamental limits and the properties of logarithms and powers.

## 1. The Foundation: The Definition of $e$

Before differentiating, we must establish the fundamental definition of the mathematical constant $e$ as a limit:

$$\lim_{u \to 0} (1+u)^{1/u} = e \text{}$$

Equivalently, using the natural logarithm:

$$\lim_{u \to 0} \frac{\ln(1+u)}{u} = 1 \text{}$$

---

## 2. Proof of the Logarithm: $\frac{d}{dx}(\log_a x)$

To find the derivative of $f(x) = \log_a x$, we apply the formal definition of the derivative:

- **The Limit:** We start with the difference quotient:
    
    $$f'(x) = \lim_{h \to 0} \frac{\log_a(x+h) - \log_a(x)}{h} \text{}$$
    
- **Property of Logarithmic Division:** We rewrite the difference using the quotient property of logarithms:
    
    $$f'(x) = \lim_{h \to 0} \frac{1}{h} \log_a\left(\frac{x+h}{x}\right) = \lim_{h \to 0} \frac{1}{h} \log_a\left(1 + \frac{h}{x}\right) \text{}$$
    
- **Algebraic Adjustment:** To match the definition of $e$, we multiply the expression by $x/x$:
    
    $$f'(x) = \lim_{h \to 0} \frac{1}{x} \cdot \frac{x}{h} \log_a\left(1 + \frac{h}{x}\right) \text{}$$
    
- **Logarithmic Power Property:** Move the factor $\frac{x}{h}$ into the exponent of the argument:
    
    $$f'(x) = \frac{1}{x} \lim_{h \to 0} \log_a\left[\left(1 + \frac{h}{x}\right)^{x/h}\right] \text{}$$
    
- **Identifying $e$:** Let $u = h/x$. As $h \to 0$, then $u \to 0$. The limit within the logarithm is the definition of $e$:
    
    $$f'(x) = \frac{1}{x} \log_a(e) \text{}$$
    
- **Change of Base:** Since $\log_a(e) = \frac{1}{\ln a}$, we arrive at the general rule:
    
    $$\frac{d}{dx}(\log_a x) = \frac{1}{x \ln a} \text{}$$
    

---

## 3. Proof of the Exponential: $\frac{d}{dx}(a^x)$

For the exponential function, we utilize the result of the logarithmic derivative and the **Derivative of the Inverse Function**:

- **Define the Inverse:** If $y = a^x$, then its inverse is $x = \log_a y$.
    
- **Apply the Inverse Rule:** Use the relationship between the derivatives of inverse functions:
    
    $$\frac{dy}{dx} = \frac{1}{\frac{dx}{dy}} \text{}$$
    
- **Substitute the Logarithmic Derivative:** From the previous proof, we know that $\frac{dx}{dy} = \frac{1}{y \ln a}$.
    
- **Inverting the Fraction:**
    
    $$\frac{dy}{dx} = y \ln a \text{}$$
    
- **Return to Original Variable:** Since $y = a^x$, we substitute it back:
    
    $$\frac{d}{dx}(a^x) = a^x \ln a \text{}$$
    

> [!TIP]
> 
> **Recommendation:** If you are studying this at the last minute, it may be more efficient to memorize the final formulas and move to the next topic.