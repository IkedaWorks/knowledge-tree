
# Immediate Integrals 

## Introduction and Definition
Immediate (or fundamental) integrals are those that can be solved directly because they are the exact inverse of well-known derivatives. They do not require complex algebraic tricks, only the recognition of the original function.

*   **The Intuition:** Imagine you have a "Forward" table (Derivatives) and a "Backward" table (Integrals). If you know that the derivative of $\sin(x)$ is $\cos(x)$, then the integral of $\cos(x)$ is "immediately" $\sin(x)$. 
*   **The Goal:** Memorize the most common paths so you don't have to deduce them from scratch every time.

---

## Formalization (The Function Dictionary)

### A. The General Power Rule
$$\int x^n \, dx = \frac{x^{n+1}}{n+1} + C \quad (n \neq -1)$$
> [!NOTE]
> You increase the exponent and divide by the new value. It is the inverse of the derivative's "Power Rule." **Order matters:** add 1 to the exponent first, then divide by that resulting number.

### B. The Logarithm Rule (The Exception)
$$\int \frac{1}{x} \, dx = \ln|x| + C \quad \text{or} \quad \int \frac{dx}{x} = \ln|x| + C$$
*   **Why the absolute value?** Logarithms do not accept negative values, but the function $1/x$ exists for $x < 0$. The $|x|$ ensures mathematical validity.
*   **Engineering Tip:** Whenever you identify that the numerator is the derivative of the denominator, the result involves a natural log.

### C. Exponential and Trigonometric Functions
*   **Natural Exponential:** $\int e^x \, dx = e^x + C$ (The "immortal" function that is its own integral/derivative).
*   **General Base:** $\int a^x \, dx = \frac{a^x}{\ln a} + C$.
*   **Sine/Cosine:** $\int \sin(x) \, dx = -\cos(x) + C$ and $\int \cos(x) \, dx = \sin(x) + C$.

---

## 3. Algebraic Setup (Preparing the Function)
Often, you must "prepare" the function algebraically before integrating:

*   **Example 1 (Roots):** $\int \sqrt{x} \, dx \rightarrow \int x^{1/2} \, dx = \frac{x^{3/2}}{3/2} + C = \frac{2}{3}x\sqrt{x} + C$.
*   **Example 2 (Denominators):** $\int \frac{1}{x^3} \, dx \rightarrow \int x^{-3} \, dx = \frac{x^{-2}}{-2} + C = -\frac{1}{2x^2} + C$.

---

## 📊 Table of Immediate Integrals

| Function $f(x)$  | Integral $\int f(x) \, dx$ | Observation                                          |
| :--------------- | :------------------------- | :--------------------------------------------------- |
| $k$ (Constant)   | $kx + C$                   | The integral of a constant generates a linear slope. |
| $x^n$            | $\frac{x^{n+1}}{n+1} + C$  | Valid for $n \neq -1$.                               |
| $1/x$            | $\ln\|x\| + C$             | Essential for fractional functions.                  |
| $e^x$            | $e^x + C$                  | Does not change during integration.                  |
| $a^x$            | $\frac{a^x}{\ln a} + C$    | Exponential with any base $a$.                       |
| $\sin(x)$        | $-\cos(x) + C$             | **Watch the negative sign!**                         |
| $\cos(x)$        | $\sin(x) + C$              | Direct inverse of the sine derivative.               |
| $\sec^2(x)$      | $\tan(x) + C$              | Fundamental for trigonometric substitutions.         |
| $\csc^2(x)$      | $-\cot(x) + C$             | Negative result for "co-" functions.                 |
| $\sec(x)\tan(x)$ | $\sec(x) + C$              | Common in advanced mechanics.                        |

> [!TIP]
> 
> **Pro Tip:** Before starting any integration, always ask yourself: "Is there a simple algebraic manipulation (like expanding a square or splitting a fraction) that can turn this into an immediate integral?" This will save you 90% of the effort.