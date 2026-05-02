
### Chronicle of an Extraordinary "Discovery": Riccati and Trigonometric Derivatives

The journey of a focused student often leads to "discoveries" that reveal deep connections between algebra, calculus, and engineering. While standard textbooks prioritize the fundamental trigonometric identity to simplify results, alternative algebraic manipulations can lead to the world of **Ordinary Differential Equations (ODEs)**.

---

### 1. The Relationship Identified: The Tangent Case

During the demonstration of the derivative of the tangent, $\frac{d}{dx}(\tan x)$, a common final stage is reached:

$$\frac{d}{dx}(\tan x) = \frac{\cos^2(x) + \sin^2(x)}{\cos^2(x)}$$

Instead of substituting the numerator with $1$ (which leads to the standard $\sec^2 x$), one can decompose the fraction:

$$\frac{d}{dx}(\tan x) = \frac{\cos^2(x)}{\cos^2(x)} + \frac{\sin^2(x)}{\cos^2(x)}$$

This reveals an elegant identity:

$$\mathbf{\frac{d}{dx}(\tan x) = 1 + \tan^2(x)}$$

- **The ODE Connection:** If we define $y = \tan(x)$, this result forms the differential equation **$y' = 1 + y^2$**. This specific form is a cornerstone of the path traveled by the mathematician **Riccati** in the 18th century.
    

---

### 2. The Expansion for the Cotangente: Mathematical Symmetry

The same logic applies to the cotangent, following a precise mathematical aesthetic. When deriving $\frac{d}{dx}(\cot x)$, the process reaches a similar juncture:

$$\frac{d}{dx}(\cot x) = \frac{-\sin^2(x) - \cos^2(x)}{\sin^2(x)}$$

Applying the fractional separation reveals a mirror symmetry:

$$\frac{d}{dx}(\cot x) = \frac{-\sin^2(x)}{\sin^2(x)} + \frac{-\cos^2(x)}{\sin^2(x)}$$

$$\mathbf{\frac{d}{dx}(\cot x) = -(1 + \cot^2(x))}$$

- **Mirroring Riccati:** If $u = \cot(x)$, we obtain the ODE **$u' = -(1 + u^2)$**. This demonstrates that the rate of change of the "co-function" is the negative of the unit added to its own square.
    

---

### 3. Applications in Engineering

These "non-standard" results are far from academic curiosities; they govern real-world mechanisms:

- **Electrical Circuits:** These equations model the charging and discharging of capacitors in non-linear circuits.
    
- **Electromagnetism:** They describe wave propagation in guides.
    
- **Mathematical Modeling:** What may initially appear as a procedural error is often the gateway to understanding complex systems through modeling.
    

> [!TIP]
> 
> **A Final Word for Students:** If a result does not appear "standardized" according to your textbook, analyze it closely. It may not yield a Fields Medal today, but it brings you closer to the actual mechanisms of the physical world.