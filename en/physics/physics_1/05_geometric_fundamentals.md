## 🏛️ Geometric Fundamentals — (Geometric Foundations for Higher Physics)

> [!IMPORTANT]
> 
> This is a mini-review for those who need a refresher on the mathematics required for higher education. These are concepts you don't just memorize, but understand. Understanding the process is what makes studying efficient and long-lasting. Have fun.

---

### 1. The Universe of Angles (Sums and Constraints)

#### 1.1. Sum of Interior Angles ( $S_i$ )

- **Intuition:** A triangle is simply a "fold" of a straight line. By the parallel postulate, when we draw a line $r \parallel$ to the base, the alternate interior angles equal those of the base.
    
- **Formalization:** $S_i = (n-2) \cdot 180^\circ$
    

> [!NOTE]
> 
> **Triangulation by Vertex:** Any convex polygon with $n > 3$ can be divided into $(n-2)$ triangles by drawing diagonals from a single vertex.
> 
> **Triangulation by Center:** Useful for areas. A regular hexagon can be divided into 6 equilateral triangles from the center. This logic of "breaking" complex figures (like trapezoids) into elementary shapes (squares and triangles) is essential in Calculus and Physics.

#### 1.2. Sum of Exterior Angles ( $S_e$ )

- **Intuition:** Walking along the perimeter of any closed polygon and returning to the initial orientation requires a complete rotation of $360^\circ$. No matter the number of sides, the "lap" is always just one.
    
- **Formalization:** Since $a_i + a_e = 180^\circ$, summing the $n$ vertices:
    
    $n \cdot 180^\circ = S_i + S_e \implies n \cdot 180^\circ = (n-2) \cdot 180^\circ + S_e \implies S_e = 360^\circ$
    

---

### 2. The Right Triangle (The most important figure in the universe)

#### 2.1. Metric Properties and Pythagorean Theorem

- **Intuition:** It's not about numbers; it's about areas. The area of the square built on the hypotenuse is the sum of the areas of the squares of the legs.
    
- **Formalization:** $a^2 = b^2 + c^2$
    

> [!NOTE]
> 
> **Try it out:** If you draw a right triangle and measure the areas of the squares formed by each side, you will see that the sum of the areas of the "squares of the legs" results exactly in the area of the "square of the hypotenuse."

#### 2.2. Triangle Similarity

- **AA Criterion (Angle-Angle):** The most used in Physics. If two angles are equal, the third one is too ($S_i = 180^\circ$), and the sides become proportional.
    
- **SSS Criterion (Side-Side-Side):** $\frac{a}{a'} = \frac{b}{b'} = \frac{c}{c'} = k$
    
- **SAS Criterion (Side-Angle-Side):** One equal angle between two proportional sides.
    
- **Mental Trigger:** In physics (such as on an inclined plane), identify alternate interior or vertically opposite angles first; side similarity will follow as a consequence.
    

---

### 3. The Exterior Angle Theorem (Deflection Trigger)

- **Intuition:** The external "turning" angle of a particle is the sum of the internal "curves" the triangle had to make at the other vertices to close the cycle.
    
- **Formalization:** $\theta_{ext} = \alpha + \beta$
    

---

### 4. Proportionality and Laws of Resolution

#### 4.1. Law of Sines (Balance of Proportions)

- **Intuition:** The larger the angle opening, the larger the side it projects.
    
- **Formalization:** $\frac{a}{\sin(A)} = \frac{b}{\sin(B)} = \frac{c}{\sin(C)} = 2R$
    

#### 4.2. Law of Cosines (The Orthogonality Corrector)

- **Intuition:** It is the Pythagorean Theorem with an "adjustment factor" for angles that are not $90^\circ$.
    
- **Formalization (Via Vector Algebra):** $c^2 = a^2 + b^2 - 2ab\cos(\gamma)$
    

---

### 5. Vector Decomposition (Linear Projection)

- **Intuition:** Discovering how much of the "total force" actually acts horizontally and vertically.
    
- **Formalization:**
    
    - **Horizontal (Adjacent):** $V_x = V \cdot \cos(\theta)$
        
    - **Vertical (Opposite):** $V_y = V \cdot \sin(\theta)$
        
    - **Magnitude:** $V = \sqrt{V_x^2 + V_y^2}$
        
    - **Direction:** $\theta = \arctan\left(\frac{V_y}{V_x}\right)$
        

> [!NOTE]
> 
> These topics are the foundation for any STEM course. You may question my method, but never the result.