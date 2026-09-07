
# Parametric Derivatives

## 1. Explanation and Intuition
In the traditional model, $y$ depends directly on $x$. In **parametric form**, both $x$ and $y$ are functions of a third independent variable: the **parameter ($t$)**, which usually symbolizes time or an angle.

> [!TIP]
> 
> **Developer's Vision**
> Imagine the movement of a cursor or a projectile in a game engine. Instead of a static trajectory, we describe the particle's position at every instant:
> *   $x = f(t)$ (Horizontal position at time $t$)
> *   $y = g(t)$ (Vertical position at time $t$)
>
> This representation allows us to describe curves that "loop back on themselves" (like spirals or orbital trajectories), something common functions fail to do because they don't pass the vertical line test.

## 2. Differentiation Rules
To find the slope of the tangent line ($\frac{dy}{dx}$) in the $xy$-plane from parameters, we use the **Chain Rule**.

### I. First Derivative (Slope)
The change in $y$ relative to $x$ is the ratio of their temporal rates of change:
$$\frac{dy}{dx} = \frac{\frac{dy}{dt}}{\frac{dx}{dt}}, \quad \text{provided that } \frac{dx}{dt} \neq 0$$

### II. Second Derivative (Concavity)
This is where the most common error occurs: it is not enough to simply differentiate the previous result again with respect to $t$. You must normalize the result by the speed at which $x$ is changing:
$$\frac{d^2y}{dx^2} = \frac{\frac{d}{dt} \left( \frac{dy}{dx} \right)}{\frac{dx}{dt}}$$

---

## 3. Solved Exercises

### Exercise 1: The Cycloid (The Tire Curve)
A cycloid is the path traced by a point on a moving bicycle tire.
Given the curve: $x = 2(t - \sin t)$ and $y = 2(1 - \cos t)$, find the slope of the tangent at $t = \pi/2$.

1.  **Temporal derivatives:**
    *   $\frac{dx}{dt} = 2(1 - \cos t)$
    *   $\frac{dy}{dt} = 2(\sin t)$
2.  **Rate ratio:**
    $$\frac{dy}{dx} = \frac{2\sin t}{2(1 - \cos t)} = \frac{\sin t}{1 - \cos t}$$
3.  **Evaluation at $t = \pi/2$:**
    $$\frac{\sin(\pi/2)}{1 - \cos(\pi/2)} = \frac{1}{1 - 0} = 1$$

**Result:** The slope is $1$ (which corresponds to a 45° angle).

### Exercise 2: Concavity in the Astroid
An astroid resembles a square with inward-curving sides. Its equations are: $x = \cos^3 t$ and $y = \sin^3 t$.

1.  **First Derivative:**
    *   $\frac{dx}{dt} = -3\cos^2 t \cdot \sin t$
    *   $\frac{dy}{dt} = 3\sin^2 t \cdot \cos t$
    *   $\frac{dy}{dx} = \frac{3\sin^2 t \cos t}{-3\cos^2 t \sin t} = -\tan t$
2.  **Second Derivative:**
    *   Derivative of the result with respect to $t$: $\frac{d}{dt}(-\tan t) = -\sec^2 t$
    *   Dividing by the rate of $x$ ($\frac{dx}{dt}$):
    $$\frac{d^2y}{dx^2} = \frac{-\sec^2 t}{-3\cos^2 t \cdot \sin t}$$

**Result:** $\frac{d^2y}{dx^2} = \frac{1}{3\cos^4 t \cdot \sin t}$

---

> [!NOTE]
> 
> **Application in Electromagnetism (Physics III)**
> Although it may seem abstract, using parametrization drastically simplifies equations involving charged particles in magnetic fields. Instead of dealing with "monstrous" Cartesian equations, you solve for $x(t)$ and $y(t)$ separately, which is the gold standard in modern physical modeling.
>
> This is just one example I found relevant; you will use this in various fields of knowledge, especially in Physics.