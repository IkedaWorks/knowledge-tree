
# One-Sided Limits: The Consistency Test

**Definition and Intuition:**

One-sided limits are the investigation of a function's behavior when we approach a point  $a$  from only one side. It is mathematics' "agreement" test.

## 🌉 The Broken Bridge Intuition
Imagine a road leading to a bridge:

- **Scenario A:** If you come from the left and the road takes you to a height of 10 meters, and from the right it also takes you to 10 meters, the bridge exists and is continuous at that point.
    
- **Scenario B:** If the left side takes you to 10 meters and the right side takes you to a 2-meter abyss, there is a jump (discontinuity). You do not have a "single destination"; therefore, you do not have a global limit.
    

## 📐 Formalization and Examples

We say that a one-sided limit exists if the function tends toward a value as $x$ approaches $a$ through values strictly greater than $a$ ( $a^+$ ) or strictly smaller than  $a$  ( $a^-$ ).

### 🏆 The Existence Theorem

The global limit $\lim_{x \to a} f(x) = L$ exists if, and only if:

$$\lim_{x \to a^-} f(x) = \lim_{x \to a^+} f(x) = L$$

---

## 📝 Example 1: The Jump (Non-Existent Limit)

**Function:** $f(x) = \frac{|x-3|}{x-3}$ at point $a = 3$.

1. **From the Right ($3^+$):** For $x > 3$, the absolute value is positive:
    
    $$\lim_{x \to 3^+} \frac{x-3}{x-3} = 1$$
    
2. **From the Left ($3^-$):** For $x < 3$, the absolute value inverts the sign:
    
    $$\lim_{x \to 3^-} \frac{-(x-3)}{x-3} = -1$$
    
    **Verdict:** Since $1 \neq -1$, the limit $\lim_{x \to 3} f(x)$ **does not exist**.
    

## 📝 Example 2: The Connection (Existent Limit)

**Piecewise function:**

$$
f(x) = \begin{cases} 2x + 1, & x < 3 \\\\ x^2 - 2, & x \ge 3 \end{cases}
$$

1. **From the Left ($x \to 3^-$):** We use the first expression:
    
    $$\lim_{x \to 3^-} (2x + 1) = 2(3) + 1 = 7$$
    
2. **From the Right ($x \to 3^+$):** We use the second expression:
    
    $$\lim_{x \to 3^+} (x^2 - 2) = 3^2 - 2 = 7$$
    
    **Verdict:** Since both sides "aim" at 7, the global limit **exists and is 7**.
    

---

## 💡 Shortcuts

- **The Exponent Shortcut:** The minus ($-$) or plus ($+$) sign in the superscript of the number does not indicate the sign of the number itself, but the "direction of the wind."
    
    - $0^-$ means "coming from the left of zero" (e.g., $-0.001$).
        
    - $0^+$ means "coming from the right of zero" (e.g., $0.001$).
        
- **The Drawing Test:** If you can draw the graph without lifting your pencil from the paper at point $a$, the one-sided limits are definitely equal.
    

> [!IMPORTANT]
> 
> **Engineering Note:** One-sided limits are used to describe switches (on/off) and voltage steps in digital circuits. The exact moment of the transition is a discontinuity.
### 🔗 Connections
- [09. Continuity of Functions](09_continuity_of_functions.md)
- [07. Limits at Infinity](07_Limits_at_Infinity_and_Infinite_Limits.md)