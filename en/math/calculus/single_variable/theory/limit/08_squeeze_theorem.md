
# Squeeze Theorem: The Sandwich Strategy

**Definition and Intuition:**

The **Squeeze Theorem** (also known as the **Sandwich Theorem** or **Confrontation Theorem**) is used to find the limit of a "complicated" function by compressing it between two "simple" functions that share the same limit.

##  The Hallway Intuition (Reality)

Imagine you are walking down a narrow hallway:

- To your left is a moving wall ( $g(x)$ ) .
    
- To your right is another moving wall ( $h(x)$ ).
    
- If both walls taper and meet exactly at a door ( $L$ ), you, who are in the middle ( $f(x)$ ), have no choice but to pass through that same door.
    

##  Formalization and the Classic Example

**The Mathematical Rule:**

If $g(x) \leq f(x) \leq h(x)$ for all values near $a$, and if:

$$\lim_{x \to a} g(x) = L \quad \text{and} \quad \lim_{x \to a} h(x) = L$$

Then, it is mandatory that:

$$\lim_{x \to a} f(x) = L$$

---

##  Step-by-Step Example: $\lim_{x \to \infty} \frac{\sin(x)}{x}$

1. **Identify the oscillation:** $\sin(x)$ has no limit at infinity (it keeps rising and falling between $-1$ and $1$).
    
2. **Create the "Sandwich" (Physical Limits):** We know that sine is always trapped:
    
    $$-1 \leq \sin(x) \leq 1$$
    
3. **Build the target function:** Divide all sides by $x$ (assuming $x > 0$):
    
    $$\frac{-1}{x} \leq \frac{\sin(x)}{x} \leq \frac{1}{x}$$
    
4. **Apply the limit to the "bread" (the ends):**
    
    $$\lim_{x \to \infty} \frac{-1}{x} = 0 \quad \text{and} \quad \lim_{x \to \infty} \frac{1}{x} = 0$$
    
5. **Conclusion:** Since the middle function is squeezed between $0$ and $0$, the limit is **$0$**.
    

---

##  Shortcuts and Exam Cases

- **The "Bounded $\times$ Zero" Shortcut:** Whenever you have a **bounded function** (like sine or cosine) multiplied by something that **goes to zero**, the result of the limit will always be **Zero**.
    
- **How to identify it on paper:** If you try to substitute and get "Oscillation / Infinity", it is almost certainly a Squeeze Theorem case.
    
- **Watch the Sign:** If you are dividing by $x$ and the limit goes to $-\infty$, the inequality sign flips, but the "crushing" result is usually the same.
    

> [!TIP]
> 
> **Conclusion:**
> 
> The Squeeze Theorem is the mathematical proof that a finite oscillation cannot resist being "crushed" toward a point or toward zero at infinity. It is the rigorous way of saying that "zero" wins against any bounded oscillation.

---

##  Practical Examples Section

### Example 1: Squared Cosine (Interval 0 to 1)

**Calculate:** $\lim_{x \to \infty} \frac{\cos^2(x)}{x^2 + 5}$

1. **Set up the Sandwich:** $\cos^2(x)$ is trapped between $0$ and $1$ (because it is squared): $0 \leq \cos^2(x) \leq 1$.
    
2. **Construct the Function:** $\frac{0}{x^2 + 5} \leq \frac{\cos^2(x)}{x^2 + 5} \leq \frac{1}{x^2 + 5}$.
    
3. **Verdict:** As the ends go to $0$ when $x \to \infty$, the limit is **$0$**.
    

### Example 2: The Absolute Value Function

**Calculate:** $\lim_{x \to 0} x^4 \cdot \sin\left(\frac{1}{x}\right)$

1. **Set up the Sandwich:** $-1 \leq \sin(1/x) \leq 1$.
    
2. **Multiply by $x^4$:** $-x^4 \leq x^4 \cdot \sin(1/x) \leq x^4$.
    
3. **Verdict:** Since $-x^4$ and $x^4$ go to $0$ when $x \to 0$, the limit is **$0$**.
    

### Example 3: Inverse Tangent (Arctan)

**Calculate:** $\lim_{x \to \infty} \frac{\arctan(x)}{x}$

1. **Identify the Bound:** The function $\arctan(x)$ is bounded between $-\pi/2$ and $\pi/2$.
    
2. **Divide by $x$:** $\frac{-\pi/2}{x} \leq \frac{\arctan(x)}{x} \leq \frac{\pi/2}{x}$.
    
3. **Verdict:** A constant divided by infinity is $0$. The limit is **$0$**.
    

---

##  Attention: Why Tangent and Cosecant do NOT fit the Sandwich?

- **Tangent ($\tan x$):** Explodes to infinity at multiple points ($\pi/2, 3\pi/2$). It is **not bounded**.
    
- **Cosecant ($\csc x$):** This is $1/\sin x$. If the sine goes to zero, the cosecant explodes.
    

The Sandwich only accepts "fillings" that actually fit inside the "bread" (**bounded functions**).