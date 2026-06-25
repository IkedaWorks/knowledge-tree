
# Limit Laws: The "Decomposition" Strategy

Limit laws are the rules that allow you to "slice" a complex function into simple pieces. They prove that the limit is a predictable operator: it distributes across basic arithmetic operations without altering the final result.

## 🧠 The Intuition of "Independence"

If you have two events happening simultaneously, the overall trend is simply the combination of individual trends. The limit "enters" the sum, the root, the exponent, and the cosine as if they were transparent.

## 📐 Fundamental Properties

Assume that $\lim_{x \to a} f(x) = L$ and $\lim_{x \to a} g(x) = M$.

- **Sum and Difference:** The limit of the sum is the sum of the limits.
    
    $$\lim_{x \to a} [f(x) \pm g(x)] = L \pm M$$
    
- **Constant Multiple:** Numbers multiplying a function "jump" outside the limit.
    
    $$\lim_{x \to a} [k \cdot f(x)] = k \cdot L$$
    
- **Product and Quotient:** The limit distributes to both top and bottom.
    
    $$\lim_{x \to a} [f(x) \cdot g(x)] = L \cdot M$$
    
    $$\lim_{x \to a} \frac{f(x)}{g(x)} = \frac{L}{M} \quad (\text{Provided } M \neq 0)$$
    
- **Power and Root:** The limit ignores the "shell" and goes straight to the core.
    
    $$\lim_{x \to a} [f(x)]^n = L^n$$
    
    $$\lim_{x \to a} \sqrt[n]{f(x)} = \sqrt[n]{L}$$
    
- **Transcendental Functions (Sine, Cosine, Log):** The limit enters the argument.
    
    $$\lim_{x \to a} \cos(f(x)) = \cos(L)$$
    
    $$\lim_{x \to a} \ln(f(x)) = \ln(L)$$
    

## 🏆 The Golden Rule (Polynomials)

For any polynomial $P(x)$, the limit is simply found through **direct substitution**:

$$\lim_{x \to a} P(x) = P(a)$$

> [!NOTE]
> 
> This is the most frequently used property, as many complex functions can be treated as local polynomials.

---

## 📝 Step-by-Step Examples

### Example 1: The "Combo" (Root + Polynomial)

**Calculate:** $\lim_{x \to 4} \sqrt{3x^2 - 11x + 2}$.

1. **Opening:** The limit enters the root: $\sqrt{\lim_{x \to 4} (3x^2 - 11x + 2)}$.
    
2. **Substitution:** Since it is a polynomial, we replace $x$ with $4$:
    
    $$\sqrt{3(4)^2 - 11(4) + 2} = \sqrt{48 - 44 + 2} = \sqrt{6}$$
    

### Example 2: The Trigonometric Limit

**Calculate:** $\lim_{x \to 0} \cos(x^2 + \pi)$.

1. **Opening:** The limit enters the cosine: $\cos(\lim_{x \to 0} (x^2 + \pi))$.
    
2. **Substitution:** $\cos(0^2 + \pi) = \cos(\pi) = -1$.
    

---

## 💡 Survival Strategies

- **The Substitution Mantra:** Your first attempt should always be substituting $x$ for the target value ($a$). If the result is a real number, you are finished. The laws guarantee this works for polynomials, sines, and roots.
    
- **The Red Light ($0/0$):** If substituting results in an indeterminate form $0/0$:
    
    - **STOP:** The quotient properties do not work here (because $M$ is zero!).
        
    - **ACTION:** Use algebraic manipulation (factoring or simplifying) to "clean" the function and try substituting again.
        
- **Constants are "Invisible":** Fixed numbers have no trend; they just multiply the final result. Move them outside the limit to simplify your view.

---

