
# Practice Exercises: Coulomb's Law

---

## Exercise 1

In vacuum ($k_0$), a point charge $q_1 = +5.0\ \mu\text{C}$ is fixed at the spatial coordinate $r_1 = (1, 2, -1)\text{ m}$ and a second point charge $q_2 = -3.0\ \mu\text{C}$ is fixed at $r_2 = (-1, 4, 2)\text{ m}$.

Using the vector formulation of Coulomb's Law:
$$\vec{F}_{1\rightarrow 2} = k_0 \frac{q_1 q_2}{|\vec{r}_2 - \vec{r}_1|^3} (\vec{r}_2 - \vec{r}_1)$$

a) Determine the relative displacement vector $\vec{r}_{12} = \vec{r}_2 - \vec{r}_1$ and its respective magnitude.
b) Calculate the electrostatic force vector $\vec{F}_{1\rightarrow 2}$ exerted by charge 1 on charge 2, expressing it analytically in Cartesian components ($i, j, k$).

---

## Exercise 2

Three point charges are statically arranged in the $xy$ plane configured as follows:
* $q_A = +2.0\ \mu\text{C}$ located at the origin $r_A = (0, 0)\text{ m}$
* $q_B = -4.0\ \mu\text{C}$ located at $r_B = (3, 0)\text{ m}$
* $q_C = +1.0\ \mu\text{C}$ located at $r_C = (0, 4)\text{ m}$

a) Determine the individual force vectors $\vec{F}_{A\rightarrow C}$ and $\vec{F}_{B\rightarrow C}$ acting on charge $q_C$.
b) Using the principle of linear superposition, calculate the net force vector $\vec{F}_{\text{res}}$ on charge $q_C$ and determine the inclination angle of this vector with respect to the positive x-axis.

---

## Exercise 3

An unknown point charge $q_1$ is positioned at $\vec{r}_1 = 2i - j\ (\text{m})$ and experiences an electrostatic force due to a charge $q_2 = +8.0\ \mu\text{C}$ located at position $\vec{r}_2 = 5i + 3j\ (\text{m})$. It is known that the vector force that $q_2$ exerts on $q_1$ is given by:
$$\vec{F}_{2\rightarrow 1} = (-2.4i - 3.2j) \times 10^{-3}\text{ N}$$

a) From the direction and sense of the given force vector, analytically deduce whether charge $q_1$ has a positive or negative sign.
b) Calculate the algebraic value and the sign of charge $q_1$.

---

## Exercise 4

Two fixed electric charges, $q_1 = +q$ and $q_2 = +4q$, are separated by a structural distance $d$ along the x-axis, with $q_1$ positioned at the origin $(0,0)$. A third generic charge $Q$ is positioned in space such that the entire system of three charges remains in synchronous static equilibrium (the net force on each of the three charges is strictly the null vector $\vec{0}$).

a) Prove vectorially why charge $Q$ cannot be located off the x-axis (meaning its y-coordinate must be 0).
b) Find the position vector $\vec{r}_Q$ and the magnitude of $Q$ (in terms of $q$) for the condition of complete static equilibrium to be satisfied.

---
---

## Section: Solved Answer Key

### Exercise 1

**a) Relative displacement vector $\vec{r}_{12}$ and its magnitude:**
The displacement vector is given by the positional difference:
$$\vec{r}_{12} = \vec{r}_2 - \vec{r}_1 = (-1 - 1)i + (4 - 2)j + (2 - (-1))k$$
$$\vec{r}_{12} = -2i + 2j + 3k\text{ m}$$

Magnitude calculation $|\vec{r}_{12}|$:
$$|\vec{r}_{12}| = \sqrt{(-2)^2 + (2)^2 + (3)^2} = \sqrt{4 + 4 + 9} = \sqrt{17}\text{ m} \approx 4.123\text{ m}$$

**b) Electrostatic force vector $\vec{F}_{1\rightarrow 2}$:**
Applying Coulomb's Law with the cube of the magnitude in the denominator:
$$\vec{F}_{1\rightarrow 2} = k_0 \frac{q_1 q_2}{|\vec{r}_{12}|^3} \vec{r}_{12}$$
$$\vec{F}_{1\rightarrow 2} = (8.988 \times 10^9) \frac{(5.0 \times 10^{-6}) \cdot (-3.0 \times 10^{-6})}{(\sqrt{17})^3} (-2i + 2j + 3k)$$

Isolating the multiplying constant:
$$\text{Constant} = \frac{-0.13482}{17\sqrt{17}} = \frac{-0.13482}{70.093} \approx -1.9234 \times 10^{-3}\text{ N/m}$$

Distributing the constant across the vector components:
$$\vec{F}_{1\rightarrow 2} = 3.85i - 3.85j - 5.77k\text{ mN}$$

---

### Exercise 2

**a) Individual force vectors on $q_C$:**
First, we declare the relative position vectors from the coordinates:
* $\vec{r}_A = (0,0)$, $\vec{r}_B = (3,0)$, $\vec{r}_C = (0,4)$
* $\vec{r}_{AC} = \vec{r}_C - \vec{r}_A = (0-0)i + (4-0)j = 4j\text{ m} \implies |\vec{r}_{AC}| = 4\text{ m}$
* $\vec{r}_{BC} = \vec{r}_C - \vec{r}_B = (0-3)i + (4-0)j = -3i + 4j\text{ m} \implies |\vec{r}_{BC}| = \sqrt{(-3)^2 + 4^2} = 5\text{ m}$

Calculating $\vec{F}_{A\rightarrow C}$:
$$\vec{F}_{A\rightarrow C} = k_0 \frac{q_A q_C}{|\vec{r}_{AC}|^3} \vec{r}_{AC} = (8.988 \times 10^9) \frac{(2.0 \times 10^{-6})(1.0 \times 10^{-6})}{4^3} (4j)$$
$$\vec{F}_{A\rightarrow C} = (8.988 \times 10^9) \frac{2.0 \times 10^{-12}}{64} (4j) = 1.1235 \times 10^{-3} (4j) = 4.49j\text{ mN}$$

Calculating $\vec{F}_{B\rightarrow C}$:
$$\vec{F}_{B\rightarrow C} = k_0 \frac{q_B q_C}{|\vec{r}_{BC}|^3} \vec{r}_{BC} = (8.988 \times 10^9) \frac{(-4.0 \times 10^{-6})(1.0 \times 10^{-6})}{5^3} (-3i + 4j)$$
$$\vec{F}_{B\rightarrow C} = (8.988 \times 10^9) \frac{-4.0 \times 10^{-12}}{125} (-3i + 4j) = -0.2876 \times 10^{-3} (-3i + 4j)$$
$$\vec{F}_{B\rightarrow C} = 0.863i - 1.15j\text{ mN}$$

**b) Net force vector and inclination angle:**
By the superposition principle (using the summation index counter):
$$\vec{F}_{\text{res}} = \vec{F}_{A\rightarrow C} + \vec{F}_{B\rightarrow C} = (0.863)i + (4.49 - 1.15)j$$
$$\vec{F}_{\text{res}} = 0.863i + 3.34j\text{ mN}$$

To find the angle $\theta$ with the positive x-axis:
$$\tan(\theta) = \frac{F_y}{F_x} = \frac{3.34\text{ mN}}{0.863\text{ mN}} \approx 3.870$$
$$\theta = \arctan(3.870) \approx 75.5^\circ$$

---

### Exercise 3

**a) Analytical deduction of the sign of $q_1$:**
The displacement vector from 2 to 1 is:
$$\vec{r}_{21} = \vec{r}_1 - \vec{r}_2 = (2 - 5)i + (-1 - 3)j = -3i - 4j\text{ m}$$
The given force is $\vec{F}_{2\rightarrow 1} = -2.4i - 3.2j\text{ mN}$. We can observe that $\vec{F}_{2\rightarrow 1}$ points in the exact same direction and sense as $\vec{r}_{21}$ (both components are negative). Since the force is repulsive (pushing $q_1$ away from $q_2$), the charges must share the same sign. Given that $q_2$ is positive, **$q_1$ must be positive**.

**b) Algebraic calculation of charge $q_1$:**
Magnitude of $\vec{r}_{21}$: $|\vec{r}_{21}| = \sqrt{(-3)^2 + (-4)^2} = 5\text{ m}$.
Taking the magnitude of the force: $|\vec{F}_{2\rightarrow 1}| = \sqrt{(-2.4)^2 + (-3.2)^2} \times 10^{-3} = 4.0 \times 10^{-3}\text{ N}$.

By the magnitude of Coulomb's Law:
$$|\vec{F}_{2\rightarrow 1}| = k_0 \frac{|q_1 q_2|}{r^2} \implies 4.0 \times 10^{-3} = (8.988 \times 10^9) \frac{|q_1| \cdot (8.0 \times 10^{-6})}{5^2}$$
$$4.0 \times 10^{-3} = 2.87616 \times 10^3 \cdot |q_1| \implies |q_1| = \frac{4.0 \times 10^{-3}}{2.87616 \times 10^3} \approx 1.39 \times 10^{-6}\text{ C}$$
Since it was deduced that $q_1 > 0$: **$q_1 \approx +1.39\ \mu\text{C}$**.
*(Note: If the book adopts $k_0 = 9 \times 10^9$, the value targets exactly $+1.39\ \mu\text{C}$ or $25/18\ \mu\text{C}$)*.

---

### Exercise 4

**a) Vector proof of collinear equilibrium:**
Assume charge $Q$ is located at a coordinate off the x-axis, meaning $\vec{r}_Q = (x_Q, y_Q)$ with $y_Q \neq 0$. The forces exerted by $q_1$ (at the origin) and $q_2$ (on the x-axis) on $Q$ will have y-axis components given by:
$$F_{1\rightarrow Q, y} = k_0 \frac{q Q}{|\vec{r}_Q|^3} y_Q \quad \text{and} \quad F_{2\rightarrow Q, y} = k_0 \frac{4q Q}{|\vec{r}_Q - d i|^3} y_Q$$
Since $q_1$ and $q_2$ have the same sign ($+q$ and $+4q$), the forces they exert on $Q$ along the y-direction will share the same sense (both push or both pull along the y-axis). Therefore, the sum of the y-components can never be zero:
$$F_{\text{res, } y} = F_{1\rightarrow Q, y} + F_{2\rightarrow Q, y} \neq 0 \quad (\text{for } y_Q \neq 0)$$
For $\vec{F}_{\text{res}} = \vec{0}$, the y-component must be zero, proving that **$Q$ must lie on the x-axis**.

**b) Determination of $\vec{r}_Q$ and the magnitude of $Q$:**
For $Q$ to balance two charges of the same sign, it must be positioned **between** them ($0 < x_Q < d$) and possess an **opposite sign (negative)**.

Equating the magnitudes of the forces that $q_1$ and $q_2$ exert on $Q$:
$$k_0 \frac{q |Q|}{x_Q^2} = k_0 \frac{4q |Q|}{(d - x_Q)^2} \implies \frac{1}{x_Q^2} = \frac{4}{(d - x_Q)^2}$$
Taking the square root of both sides:
$$\frac{1}{x_Q} = \frac{2}{d - x_Q} \implies d - x_Q = 2x_Q \implies 3x_Q = d \implies x_Q = \frac{d}{3}$$
Therefore, the position vector is **$\vec{r}_Q = \frac{d}{3}i$**.

Now, for the entire system to be in equilibrium, the net force on $q_1$ (at the origin) must also be zero due to the action of $q_2$ and $Q$:
$$F_{\text{res on } q_1} = k_0 \frac{q \cdot 4q}{d^2} + k_0 \frac{q \cdot Q}{(d/3)^2} = 0$$
$$\frac{4q^2}{d^2} + \frac{9qQ}{d^2} = 0 \implies 4q + 9Q = 0 \implies Q = -\frac{4}{9}q$$