
# Riemann Sums 

## The Dream of Measuring the Curve

Since Antiquity, humans have known how to measure rectangles ($A = b \cdot h$). The problem arises when nature presents curves. How can we measure the area under a parabola or inside a circle?

**The Intuition:** If we cannot measure the curve directly, we "squeeze" it between shapes we already know. The integral is, in essence, the process of making this approximation so perfect that the error disappears.

---

## From the Method of Exhaustion to the Riemann Sum

### The Greek Heritage: The Method of Exhaustion

Before Newton and Leibniz, mathematicians like Archimedes used exhaustion.

- **The Process:** To measure the area of a circle, he drew polygons inside (inscribed) and outside (circumscribed).
    
- **The Logic:** As you increase the number of sides of the polygon (hexagon, octagon, dodecagon...), the polygon's area "occupies" almost the entire circle.
    
- **The Limit:** Archimedes "exhausted" the empty area. He came very close to the value of $\pi$ without possessing the formal concept of a "limit."
    

> [!TIP]
> 
> **Practical Example:** Imagine dividing a circle into several triangles (like pizza slices). Since the area of a triangle is known ($A = \frac{b \cdot h}{2}$), we can estimate the circle's area. As we increase the number of triangles, the sum of their areas approaches the real value of the circle's area.

### The Formalization: The Riemann Integral

In the 19th century, Bernhard Riemann refined this idea for functions on the Cartesian plane, replacing polygons with vertical rectangles.

**The Mechanics of the Sum:**

To calculate the area under a function $f(x)$ in the interval $[a, b]$:

1. **Partition:** We divide the interval into $n$ pieces of width $\Delta x = \frac{b-a}{n}$.
    
2. **Choosing the Height:** In each piece, we choose a point $x_i^*$ to determine the height of the rectangle $f(x_i^*)$.
    
3. **The Sum:** We sum the area of all $n$ rectangles:
    
    $$S_n = \sum_{i=1}^{n} f(x_i^*) \cdot \Delta x$$
    

---

## The Leap to the Integral

The actual area ($A$) is the limit of this sum as the number of rectangles tends to infinity and the width of each tends to zero:

$$A = \lim_{n \to \infty} \sum_{i=1}^{n} f(x_i^*) \cdot \Delta x = \int_{a}^{b} f(x) \, dx$$

### The "Magic" of the Long S

The integral notation $\int$ is actually a stylized **S** (for _Summa_).

- The $f(x)$ represents the **height** (the function value).
    
- The $dx$ represents the **infinitesimal base** (the $\Delta x$ that became infinitely thin).
    

---

## Conclusion: What Have We Learned?

- **Error Decreases:** The more rectangles we use, the more precise the sum becomes. At infinity, the error is zero.
    
- **Sign Matters:** Unlike Greek geometry (where area is always positive), the Riemann Integral considers position. If the rectangle is below the x-axis, the "height" $f(x)$ is negative, generating a negative area.
    
- **Net Area:** The integral calculates the balance between what is above (positive) and what is below (negative) the x-axis.