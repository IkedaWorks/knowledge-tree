
# Curve Sketching Guide (Graphical Construction)

## Objective
To transform algebraic analysis ($f$, $f'$, and $f''$) into a precise visual representation, identifying turning points, growth trends, and system limits.

---

## Step-by-Step Pipeline

### Step 1: Domain and Intercepts
*   **Determine the Domain:** Where does the function exist? (Be careful with division by zero or negative square roots).
*   **y-intercept:** Calculate $f(0)$.
*   **x-intercepts:** Solve $f(x) = 0$ (find the roots).

### Step 2: Symmetry
*   **Even Function:** If $f(-x) = f(x)$, the function is symmetric with respect to the **y-axis**.
*   **Odd Function:** If $f(-x) = -f(x)$, the function is symmetric with respect to the **origin**.
* 
> [!TIP]
> 
>  **Efficiency Hack:** Identifying symmetry saves half the drawing effort.

### Step 3: Asymptotes
*   **Horizontal Asymptotes:** Calculate the limits of $f(x)$ as $x \to \infty$ and $x \to -\infty$.
*   **Vertical Asymptotes:** Check the points where the function "explodes" (typically where the denominator equals zero).

### Step 4: Intervals of Increase and Decrease
*   Calculate the first derivative $f'(x)$.
*   Find the **Critical Points** ($f'(x) = 0$ or where $f'(x)$ is undefined).
*   Create a **Sign Chart** for $f'(x)$ to identify where the function rises or falls.

### Step 5: Local Maxima and Minima
*   Use the critical points from Step 4.
*   Check for a change in the sign of $f'$ or apply the **Second Derivative Test** to classify the points.

### Step 6: Concavity and Inflection Points
*   Calculate the second derivative $f''(x)$.
*   Find where $f''(x) = 0$.
*   Analyze the sign:
    *   $f''(x) > 0$: **Concave up** (smile).
    *   $f''(x) < 0$: **Concave down** (umbrella).

### Step 7: The Final Sketch
1.  Mark all identified key points (intercepts, maxima, minima, and inflection).
2.  Draw asymptotes as **dashed/dotted lines**.
3.  Connect the points strictly respecting the growth intervals and the defined concavities.

---

> [!IMPORTANT]
> 
> **Engineering Logic**
> In signal processing or structural analysis, the "sketch" is more than a drawing—it is a map of system stability. Points where the curve changes concavity often represent transitions in physical states (like the elastic limit of a material).