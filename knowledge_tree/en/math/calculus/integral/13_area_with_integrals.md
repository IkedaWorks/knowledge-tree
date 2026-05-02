
# Practical Applications: Area Calculation 

## Guide for Exercises

To solve areas between complex functions, follow this protocol:

- **Graph Sketch:** Draw the functions. Identify roots and y-axis intercepts.
    
- **Points of Intersection:** Set the functions equal to each other ($f(x) = g(x)$) to find the **Limits of Integration**.
    
- **Identification of the Upper Function:** Check which function is "on top" within the interval. This defines the setup: $\int_{a}^{b} (\text{Upper} - \text{Lower}) \, dx$.
    
- **Interval Division:** If the "ceiling" or the "floor" of the region changes, divide the calculation into two or more integrals.
    

---

## Exercise 1: Area Bounded by a Parabola and a Line

**Problem:** Determine the area of the region enclosed by the functions $f(x) = x^2 - 4$ and $g(x) = 3x$.

1. **Finding the Limits (Intersection):**
    
    $x^2 - 4 = 3x \implies x^2 - 3x - 4 = 0$
    
    Roots (Sum and Product): $(x - 4)(x + 1) = 0 \implies \mathbf{a = -1}$ and $\mathbf{b = 4}$.
    
2. **Defining the Upper Function:**
    
    Testing $x = 0$ (inside the interval): $f(0) = -4$ and $g(0) = 0$. Since $0 > -4$, the line $g(x)$ is the upper function.
    
3. **Setup and Integration:**
    
    $\int_{-1}^{4} [3x - (x^2 - 4)] \, dx = \int_{-1}^{4} (-x^2 + 3x + 4) \, dx$
    
    Antiderivative: $F(x) = \left[ -\frac{x^3}{3} + \frac{3x^2}{2} + 4x \right]_{ -1}^{4}$
    
4. **Applying the FTC:**
    
    - For $x = 4$: $-\frac{64}{3} + 24 + 16 = \frac{56}{3}$
        
    - For $x = -1$: $\frac{1}{3} + \frac{3}{2} - 4 = -\frac{13}{6}$
        
    - **Result:** $\frac{56}{3} - (-\frac{13}{6}) = \frac{112 + 13}{6} = \mathbf{\frac{125}{6} \approx 20.83}$
        

---

## Exercise 2: Area Between Two Parabolas

**Problem:** Calculate the area between $f(x) = 2 - x^2$ and $g(x) = x^2$.

1. **Limits:** $2 - x^2 = x^2 \implies 2x^2 = 2 \implies x = \pm 1$.
    
2. **Upper Function:** For $x = 0$, $f(0) = 2$ and $g(0) = 0$. Therefore, $f(x)$ is on top.
    
3. **Integration:**
    
    $\int_{-1}^{1} (2 - x^2 - x^2) \, dx = \int_{-1}^{1} (2 - 2x^2) \, dx$
    
    Antiderivative: $\left[ 2x - \frac{2x^3}{3} \right]_{-1}^{1}$
    
4. **Applying the FTC:**
    
    - For $x = 1$: $2 - \frac{2}{3} = \frac{4}{3}$
        
    - For $x = -1$: $-2 + \frac{2}{3} = -\frac{4}{3}$
        
    - **Result:** $\frac{4}{3} - (-\frac{4}{3}) = \mathbf{\frac{8}{3} \approx 2.67}$
        

---

## Exercise 3: Area with Root and Line (Changing "Floor")

**Problem:** Area bounded by $y = \sqrt{x}$, $y = x - 2$, and the x-axis ($y = 0$).

1. **Critical Points:**
    
    - Intersection $\sqrt{x} = x - 2 \implies x = 4$.
        
    - Intersection $\sqrt{x} = 0 \implies x = 0$.
        
    - Intersection $x - 2 = 0 \implies x = 2$.
        
2. **Area Division:** In the graph, we notice that from $0$ to $2$ the lower limit is the x-axis, but from $2$ to $4$ the lower limit becomes the line $x - 2$.
    
3. **Part A (0 to 2):** $\int_{0}^{2} \sqrt{x} \, dx = \left[ \frac{2}{3}x^{3/2} \right]_0^2 = \frac{4\sqrt{2}}{3}$
    
4. **Part B (2 to 4):** $\int_{2}^{4} (\sqrt{x} - (x - 2)) \, dx = \left[ \frac{2}{3}x^{3/2} - \frac{x^2}{2} + 2x \right]_2^4$
    
5. **Calculation and Sum:**
    
    - Result Part B: $\left(\frac{16}{3} - 8 + 8\right) - \left(\frac{4\sqrt{2}}{3} - 2 + 4\right) = \frac{16}{3} - \frac{4\sqrt{2}}{3} - 2$
        
    - **Total Area:** $\frac{4\sqrt{2}}{3} + \frac{16}{3} - \frac{4\sqrt{2}}{3} - 2 = \frac{16}{3} - \frac{6}{3} = \mathbf{\frac{10}{3}}$