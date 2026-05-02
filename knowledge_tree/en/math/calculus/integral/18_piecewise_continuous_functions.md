
# Integrability vs. Differentiability

## The Fundamental Difference

- **Derivative (Local Operation):** Requires the function to be "smooth." If there is a "corner" (like in $|x|$) or a jump, the derivative ceases to exist at that exact point.
    
- **Integral (Global Operation):** This is an accumulation of area. It is much more resilient. An isolated point or a finite jump cannot "empty" the total area under the curve.
    

---

## The Continuity Myth

- **Differentiable $\implies$ Continuous:** Absolute truth. Every differentiable function is necessarily continuous.
    
- **Integrable $\implies$ Continuous:** **False.** A function can have several discontinuities (finite jumps) and still have a perfectly calculable definite integral.
    

> [!TIP]
> 
> **Example: Heaviside Function (Unit Step)**
> 
> Used in electrical systems: 0 when the light is off, 1 when you flip the switch. There is a sharp jump, but the area (accumulated energy) can be calculated normally.

---

## Piecewise Continuous Functions

We say a function $f(x)$ is **piecewise continuous** on an interval $[a, b]$ when:

1. It is continuous at almost all points, except at a finite number of places.
    
2. At these "jump" points, the one-sided limits exist and are real (the function does not explode to infinity).
    

**When does the Integral fail?**

An integral only becomes **Improper** if the discontinuity is infinite (a vertical asymptote). _Example:_ $\int \frac{1}{x} \, dx$ passing through zero. The area "escapes" to infinity.

---

## Practice: Solving Modular Functions

To integrate functions with absolute values or multiple rules, we use the **Additivity Property**:

$$\int_{a}^{b} f(x) \, dx = \int_{a}^{c} f_1(x) \, dx + \int_{c}^{b} f_2(x) \, dx$$

**Problem:** Calculate $\int_{-1}^{3} f(x) \, dx$, where $f(x)$ changes behavior.

### Step 1: Definition of the Absolute Value

Recalling the definition:

- $|x| = x$ if $x \geq 0$ and $-x$ if $x < 0$.
    
- $|x-2| = (x-2)$ if $x \geq 2$ and $-(x-2)$ if $x < 2$.
    

### Step 2: Breaking the Intervals

We need to respect the points where the function changes its "law" (at $x=0$ and $x=2$):

$$\int_{-1}^{3} f(x) \, dx = \int_{-1}^{0} (-x) \, dx + \int_{0}^{2} (x) \, dx + \int_{2}^{3} (x - 2) \, dx$$

### Step 3: Applying the FTC

1. $\left[-\frac{x^2}{2}\right]_{-1}^{0} = 0 - \left(-\frac{1}{2}\right) = \mathbf{0.5}$
    
2. $\left[\frac{x^2}{2}\right]_{0}^{2} = \frac{4}{2} - 0 = \mathbf{2}$
    
3. $\left[\frac{x^2}{2} - 2x\right]_{2}^{3} = \left(\frac{9}{2} - 6\right) - (2 - 4) = (-1.5) - (-2) = \mathbf{0.5}$
    

**Final Result:** $0.5 + 2 + 0.5 = \mathbf{3}$

---

## 💡 Geometric Verification Tip

To confirm the result, sketch the graph. In this case, you will see three triangles formed between the function and the x-axis. Calculate the area of each one ($\text{Base} \cdot \text{Height} / 2$) and sum them up. The result should be exactly 3.