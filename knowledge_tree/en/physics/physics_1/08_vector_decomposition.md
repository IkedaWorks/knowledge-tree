## 🏛️ Vector Decomposition & Sum — ( The Engineer's Guide )

> [!IMPORTANT]
> 
> **The Fundamental Concept**
> 
> - **What is decomposing?** It is projecting a tilted vector onto reference axes ( usually ( $x$ ) and ( $y$ ) ).
>     
> - **Why do we do it?** To transform complex two-dimensional problems into two simple, independent one-dimensional problems. Decomposing is "seeing" the hypotenuse of a right triangle.
>     

---

### 📐 Orthogonal Method ( Cosine and Sine )

**Setup:** Vector ( $\vec{V}$ ) making an angle ( $\theta$ ) with the horizontal axis.

- **Adjacent Component ( $V_x$ ):** ( $V \cdot \cos(\theta)$ ) ( "With" the angle $\rightarrow$ Cosine ).
    
- **Opposite Component ( $V_y$ ):** ( $V \cdot \sin(\theta)$ ) ( "Without" the angle $\rightarrow$ Sine ).
    
- **Verification ( Pythagoras ):** To validate the decomposition: ( $V = \sqrt{V_x^2 + V_y^2}$ ).
    

---

### ⛓️ Summation Methods ( Resultant )

#### 1. Polygon Method ( The "Path" )

- **Application:** Useful for summing several vectors sequentially ( $\vec{A} + \vec{B} + \vec{C}$ ).
    
- **Procedure:** Place the origin of the second at the tip of the first. The resultant ( $\vec{R}$ ) connects the origin of the first to the tip of the last.
    
- **Study Tip:** If the polygon closes, the resultant force is zero ( equilibrium ).
    

#### 2. Parallelogram Method ( The "Common Origin" )

- **Application:** Summing two vectors that start from the same point.
    
- **Intensity ( Extended Law of Cosines ):**
    
    ( $R = \sqrt{A^2 + B^2 + 2AB\cos(\theta)}$ )
    
- **Note:** In physics, we often use the ( $+$ ) sign because ( $\theta$ ) is the angle between the origins, not the internal angle of the triangle. Understanding the geometry is key to not getting the sign wrong.
    

---

### 🏔️ Practical Application: Inclined Plane

This is the "final boss" of decomposition in Engineering.

- **Weight ( $P$ ):** Always vertical, pointing downwards.
    
- **Tangential Component ( $P_x$ ):** Responsible for accelerating the block $\rightarrow$ ( $P \cdot \sin(\alpha)$ ).
    
- **Normal Component ( $P_y$ ):** Responsible for pressing the block against the surface $\rightarrow$ ( $P \cdot \cos(\alpha)$ ).
    
- **The Insight:** The angle of the inclined plane ( $\alpha$ ) is the same as the angle between the Weight and the Normal.
    

---

### 🏆 Exercise Section: Elite Problem

**Statement:** A block of weight ( $W$ ) is in equilibrium suspended by a knot at point ( $C$ ), supported by a rope ( $BC$ ) ( fixed angle $\phi$ with the vertical ). An external force ( $F$ ) is applied to the knot with inclination ( $\theta$ ) ( horizontal ). Determine ( $\theta$ ) so that ( $F$ ) is minimal and calculate ( $F_{min}$ ).

**Resolution via First Principles:**

1. **FBD:** Forces ( $W$ ) ( vertical ), ( $T$ ) ( rope ), and ( $F$ ) ( external ).
    
2. **Triangle of Forces:** Since there is equilibrium, ( $\vec{W} + \vec{T} + \vec{F} = 0$ ) ( closed triangle ).
    
3. **Law of Sines:**
    
    ( $\frac{F}{\sin(\phi)} = \frac{W}{\sin(\alpha)}$ )
    
    Where ( $\alpha$ ) is the angle between ( $F$ ) and ( $T$ ).
    
4. **Optimization:** For ( $F$ ) to be minimal, ( $\sin(\alpha)$ ) must be maximal ( $1$ ). Therefore, ( $\alpha = 90^\circ$ ).
    
5. **Conclusion:** ( $F$ ) is minimal when it is perpendicular to the rope.
    
6. **Calculating ( $\theta$ ):** If ( $F \perp T$ ) and ( $T$ ) makes ( $\phi$ ) with the vertical, then ( $F$ ) must make the same angle ( $\phi$ ) with the horizontal.
    
7. **Result 1:** ( $\theta = \phi$ ).
    
8. **Value of ( $F_{min}$ ):** Substituting ( $\sin(\alpha) = 1$ ):
    
    ( $F_{min} = W \cdot \sin(\phi)$ )
    

> [!NOTE]
> 
> **Reflection:** Notice how Geometry ( Law of Sines ) solved an optimization problem that many would try to solve with complex derivatives. This is understanding the "gears of the clock."