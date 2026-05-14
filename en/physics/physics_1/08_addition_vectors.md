
# 🏛️ Addition of Planar Forces: Geometry and Rigor

## Prerequisites

This note assumes you have mastered the following:

- **Plane Geometry:** Properties of parallelograms, alternating interior angles, and supplementary angles.
    
- **Trigonometry:** Direct application of the Law of Sines and Law of Cosines.
    
- **Vector Concept:** The fundamental distinction between scalar and vector quantities.
    

## The Problem of Force Composition

In statics, we rarely deal with a single isolated force. The need to find a resultant force arises to simplify complex systems into a single equivalent effect. However, the method you choose depends entirely on how many forces are at play and the geometry of the problem.

### The Parallelogram Law and Its Limitations

This is the fundamental method, but be careful: it is strictly restricted to the sum of only two forces acting from the same point. The resultant is the diagonal of the parallelogram formed by the components. If you have three forces, you must sum two, find a partial resultant, and then sum it with the third.

### The Triangle and Polygon Rules

To optimize calculations, we use the triangle rule, which is essentially half of a parallelogram. You place the tip of the first force at the origin of the second; the resultant will be the vector that closes this triangle.

When the system has multiple forces (three or more), we evolve to the **polygon rule**. The process is the same: you stack the vectors one after another ("tip-to-tail"). The resultant force will be the vector connecting the origin of the very first vector to the tip of the last one. If this polygon closes exactly at the starting point, you have graphically proven that the system is in equilibrium and the resultant is zero.

## Reasoning Dynamics

The mathematics behind this exists to validate what the drawing tells us. Imagine you are tracing a navigation route. Each force is a displacement. If you pull in one direction and then another, the final result is the direct displacement from the starting point to the final point.

The **Law of Cosines** is used here to measure the "length" of this final route when the angle between the pulls is not 90 degrees. Meanwhile, the **Law of Sines** serves to adjust the compass, determining the exact angle of the resultant direction. It is a game of geometry: you use the properties of parallel lines to "transport" the angles from the problem statement into your force triangle.

---

# 🔩 Exercise 01: Geometric Addition on a Fastening Bolt

> [!IMPORTANT] Requirements
> 
> - Identification of supplementary angles.
>     
> - Application of the Law of Cosines for magnitude.
>     
> - Terminal proficiency for asset conversion.
>     

### Problem Statement

A fastening bolt in a steel base is subjected to two pulling forces exerted by ropes, $\vec{F_1}$ and $\vec{F_2}$. Force $\vec{F_1}$ has a magnitude of $200\text{ N}$ at $20^\circ$ with the horizontal, while $\vec{F_2}$ has $300\text{ N}$ at $10^\circ$ with the vertical. Determine the magnitude of the resultant force ($\vec{F_R}$) that the bolt must support. Determine the direction of $\vec{F_R}$ relative to the positive x-axis.

### Visual Representation

### Solution: Vector Addition on the Bolt

**Problem Data:**

- $F_1 = 200\text{ N}$ at $20^\circ$ with the positive x-axis.
    
- $F_2 = 300\text{ N}$ at $10^\circ$ with the positive y-axis (vertical).
    

#### 1. Geometric Analysis (The Force Triangle)

To use the Law of Cosines, we need the internal angle of the triangle formed by placing $\vec{F_2}$ at the tip of $\vec{F_1}$.

- The angle between the two forces in the plane is: $90^\circ - (20^\circ + 10^\circ) = 60^\circ$.
    
- By transposing $\vec{F_2}$ to the tip of $\vec{F_1}$, the internal angle $\beta$ will be the supplement:
    
    $$\beta = 180^\circ - 60^\circ = 120^\circ$$
    

#### 2. Resultant Force Intensity ($F_R$)

Applying the **Law of Cosines**:

$$F_R = \sqrt{F_1^2 + F_2^2 - 2 \cdot F_1 \cdot F_2 \cdot \cos(\beta)}$$

$$F_R = \sqrt{200^2 + 300^2 - 2(200)(300) \cdot \cos(120^\circ)}$$

**$F_R \approx 435.9\text{ N}$**

#### 3. Direction of the Resultant relative to the Positive x-axis

Using the **Law of Sines**:

$$\frac{F_2}{\sin(\theta)} = \frac{F_R}{\sin(120^\circ)} \Rightarrow \theta \approx 36.6^\circ$$

The final direction $\phi$ relative to the positive x-axis is:

$$\phi = \theta + 20^\circ = 56.6^\circ$$

**Final Answer:**

The resultant force has a magnitude of **$435.9\text{ N}$** and its direction is **$56.6^\circ$** counter-clockwise from the positive x-axis.