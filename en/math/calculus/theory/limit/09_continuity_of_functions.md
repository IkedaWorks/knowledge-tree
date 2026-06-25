
# Continuity of Functions: The Seamless Flow

**Definition and Intuition:**

A function is **continuous** if you can draw its graph without lifting your pen from the paper. If there is a hole, a jump, or a vertical explosion, the continuity is broken.

## 💡 The Switch Intuition 

- **Continuous:** Like a light dimmer. You turn it, and the brightness increases smoothly from 0% to 100%, passing through all intermediate values.
    
- **Discontinuous:** Like a standard on/off switch. You are at 0 and, in a snap, jump to 1. There is no "0.5" at the moment of the click—there is a jump.
    

---

## 📐 Formalization (The 3-Step Test)

To state that a function is continuous at a specific point $x = a$, it must pass three mandatory tests:

1. **Does the function exist at the point?** $f(a)$ must be defined (it cannot result in $0/0$ or the square root of a negative number).
    
2. **Does the limit exist at the point?** $\lim_{x \to a} f(x)$ must exist (meaning one-sided limits are equal).
    
3. **Is the limit equal to the function's value?** $\lim_{x \to a} f(x) = f(a)$. The "target" of the trend must be exactly where the actual point is drawn.
    

---

## 📝 Step-by-Step Example: Verifying Continuity

**Verify if** $f(x) = \frac{x^2 - 1}{x - 1}$ **is continuous at** $x = 1$.

- **Step 1 ($f(1)$ exists?):** $f(1) = \frac{1^2 - 1}{1 - 1} = \frac{0}{0}$. It does not exist.
    
- **Verdict:** The function is **discontinuous** at $x = 1$. There is a "hole" in the graph.
    

---

## 🛠️ Types of Discontinuity and Shortcuts

There are three main ways to "break" a function:

- **Removable (Hole):** The limit exists, but the point is either missing or in the wrong place.
    
    - _Shortcut:_ This occurs when you can simplify the fraction (cancel out terms).
        
- **Jump:** The one-sided limits are different. Common in piecewise functions.
    
    - _Shortcut:_ The "train" from the left arrives at one height, and the one from the right arrives at another.
        
- **Infinite (Asymptote):** The function explodes toward infinity.
    
    - _Shortcut:_ Division by zero where the numerator is not zero.
        

---

## 📝 Examples and Exercises Section

### Example 1: "Fixing" a Function

**Determine $k$ so that $f(x)$ is continuous at $x = 2$:**

$$
f(x) = \begin{cases} x + 3, & x < 2 \\\\ k, & x = 2 \\\\ 3x - 1, & x > 2 \end{cases}
$$

1. **Limit from the left:** $2 + 3 = 5$.
    
2. **Limit from the right:** $3(2) - 1 = 5$.
    
3. **Verdict:** The global limit is 5. To "plug the hole" and be continuous, the point $f(2)$ must equal the limit. Therefore, **$k = 5$**.
    

### Example 2: The Function with a "Hole"

**Verify if** $f(x) = \frac{x^2 - 4}{x - 2}$ **is continuous at** $x = 2$.

1. **Test 1 ($f(2)$ exists?):** $f(2) = 0/0$. Undefined.
    
2. **Test 2 (Does the limit exist?):** $\lim_{x \to 2} \frac{(x-2)(x+2)}{x-2} = \lim_{x \to 2} (x+2) = 4$.
    
3. **Verdict:** Discontinuous at $x = 2$, but the limit exists and equals 4.
    

### Example 3: Finding the Unknown $k$

**Determine $k$ so that $f(x)$ is continuous across its entire domain:**

$$
f(x) = \begin{cases} kx^2, & x \le 2 \\\\ 10 - kx, & x > 2 \end{cases}
$$

1. **Equating the sides at the transition point ($x=2$):**
    
    - Left side: $k(2)^2 = 4k$.
        
    - Right side: $10 - k(2) = 10 - 2k$.
        
2. **Solving:** $4k = 10 - 2k \implies 6k = 10 \implies \mathbf{k = 5/3}$.
    

---

## 📜 The Intermediate Value Theorem (IVT)

If a function is continuous on an interval and it starts at $y = -2$ and ends at $y = 5$, it **must** have passed through zero (or any value between -2 and 5) at some point.

- **Shortcut:** If you crossed the street, at some point you were exactly in the middle of it. This proves equations have roots without needing to solve them.
    

---

## 💡 Resolution Shortcuts

- **Polynomials are "Well-Behaved":** If the function is just a simple polynomial, it is continuous along the entire real line.
    
- **Where to look for trouble:** Discontinuities live where the denominator becomes zero or where the function "changes rules."
    
- **Visual Cue:** If the one-sided limits are different, it is a **Jump**. If the limits are equal but the function doesn't exist there, it is a **Hole**.

