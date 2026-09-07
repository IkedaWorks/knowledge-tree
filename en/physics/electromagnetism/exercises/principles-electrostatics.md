

# Exercises: Elementary Charge and Quantization

This note compiles practical problems designed to calibrate the concepts of charge quantization and the conservation of electrostatic systems.

---

##  Exercise Statements

### Question 01
An initially neutral conductive body is electrified and now exhibits a stable net electric charge of $Q = +4.8\ \mu\text{C}$.

**a)** Is this body experiencing an excess or a shortage of electrons? Justify microscopically.  
**b)** Determine the exact quantity of electrons ($n$) that were transferred during the electrification process.

### Question 02
A metallic conductor (copper wire) carries a stable electric current. A microscopic analysis reveals that exactly $5.0 \times 10^{18}$ electrons cross the cross-section of the wire every second.

**a)** What is the absolute value of the total electric charge ($Q$) flowing through this section each second?  
**b)** If the electric current intensity ($I$) is defined by the change in charge over time ($I = \Delta Q / \Delta t$), what is the current supplying this conductor in Amperes ($\text{A}$)?

### Question 03
Three identical conductive spheres, $A$, $B$, and $C$, are isolated. Initially, sphere $A$ has a charge of $Q_A = +12\ \mu\text{C}$, while $B$ and $C$ are completely neutral ($Q_B = 0$ and $Q_C = 0$).

1. Sphere $A$ is brought into contact with sphere $B$ and then separated.
2. Immediately after, sphere $A$ is brought into contact with sphere $C$ and separated.

Determine the final electric charge of each of the three spheres after these processes.

### Question 04
Two distant conductive spheres, $A$ and $B$, have different radii, where $R_A = 2R$ and $R_B = 3R$. Initially, sphere $A$ is charged with $Q_A = +20\ \mu\text{C}$ and sphere $B$ is neutral ($Q_B = 0$). The two spheres are interconnected by a long, thin conducting wire until electrostatic equilibrium is reached.

Determine the final charges $Q'_A$ and $Q'_B$ of each sphere after equilibrium.

---

##  Answer Key and Step-by-Step Solutions

### Solution to Question 01
**Item a):** There is a shortage of electrons. The positive sign of the net charge ($Q > 0$) indicates that the charge balance broke in favor of the protons, meaning the body lost electrons (the only charges with the mobility to leave the atomic lattice).

**Item b):** Converting the charge from microcoulombs to the standard unit:
$$Q = 4.8 \times 10^{-6}\text{ C}$$

Using the principle of charge quantization ($Q = n \cdot e$):
$$n = \frac{4.8 \times 10^{-6}\text{ C}}{1.6 \times 10^{-19}\text{ C}}$$
$$n = 3.0 \times 10^{13}\text{ electrons lost.}$$

---

### Solution to Question 02
**Item a):** Given data: $n = 5.0 \times 10^{18}$ electrons and $e = 1.6 \times 10^{-19}\text{ C}$. Applying the principle of quantization to find the total charge per second:
$$Q = n \cdot e$$
$$Q = (5.0 \times 10^{18}) \cdot (1.6 \times 10^{-19})$$
$$Q = 8.0 \times 10^{-1}\text{ C} = 0.8\text{ C}$$

**Item b):** Since the given time rate is $\Delta t = 1\text{ s}$, and the calculated charge was $\Delta Q = 0.8\text{ C}$:
$$I = \frac{\Delta Q}{\Delta t} = \frac{0.8\text{ C}}{1\text{ s}} = 0.8\text{ A}\ (800\text{ mA})$$

---

### Solution to Question 03
**Initial Data:** $Q_A = +12\ \mu\text{C}$, $Q_B = 0$, and $Q_C = 0$. Since the spheres are conductive and identical, the net charge divides equally upon each contact.

1. **First Contact ($A$ with $B$):**
   The total charge of the system is conserved and redistributed equally:
   $$Q'_A = Q'_B = \frac{Q_A + Q_B}{2} = \frac{12\ \mu\text{C} + 0}{2} = +6\ \mu\text{C}$$

2. **Second Contact ($A$ with $C$):**
   Now, sphere $A$ (carrying its new charge of $+6\ \mu\text{C}$) touches sphere $C$ (which remains neutral):
   $$Q''_A = Q'_C = \frac{Q'_A + Q_C}{2} = \frac{6\ \mu\text{C} + 0}{2} = +3\ \mu\text{C}$$

**Final Answer:**
* $Q_A = +3\ \mu\text{C} \text{ (or } 3.0 \times 10^{-6}\text{ C)}$
* $Q_B = +6\ \mu\text{C} \text{ (or } 6.0 \times 10^{-6}\text{ C)}$
* $Q_C = +3\ \mu\text{C} \text{ (or } 3.0 \times 10^{-6}\text{ C)}$

---

### Solution to Question 04
**Initial Data:** $R_A = 2R$, $R_B = 3R$, $Q_A = +20\ \mu\text{C}$, and $Q_B = 0$. Since the spheres have different radii, they reach equilibrium when their electric potentials equalize ($V_A = V_B$), resulting in final charges that are directly proportional to their respective radii.

1. **Law of Conservation of Charge:**
   The sum of the charges after contact must equal the initial total charge of the system:
   $$Q'_A + Q'_B = Q_A + Q_B$$
   $$Q'_A + Q'_B = 20\ \mu\text{C} \quad \text{--- (Equation I)}$$

2. **Equilibrium Condition (Equal Potentials):**
   $$\frac{Q'_A}{R_A} = \frac{Q'_B}{R_B}$$
   
   Substituting the radii values:
   $$\frac{Q'_A}{2R} = \frac{Q'_B}{3R}$$
   
   Simplifying the $R$ term and isolating $Q'_B$:
   $$Q'_B = \frac{3}{2}Q'_A \implies Q'_B = 1.5Q'_A \quad \text{--- (Equation II)}$$

3. **Solving the System of Equations:**
   Substituting Equation II into Equation I:
   $$Q'_A + 1.5Q'_A = 20$$
   $$2.5Q'_A = 20$$
   $$Q'_A = \frac{20}{2.5} = 8\ \mu\text{C}$$

   Now, determining the value of $Q'_B$:
   $$Q'_B = 1.5 \cdot 8 = 12\ \mu\text{C}$$

**Final Answer:**
After electrostatic and thermal equilibrium is achieved, the spheres assume the stable charge values of **$Q'_A = 8\ \mu\text{C}$** and **$Q'_B = 12\ \mu\text{C}$**.