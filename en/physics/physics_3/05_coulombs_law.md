
# Coulomb's Law (Electric Force)

Coulomb's Law describes the force interaction between stationary point electric charges. Since we are discussing the interaction between an electric field and an electric charge, we define this phenomenon as an **electric force**, which serves as the bedrock for all of electrostatics.

---

## 📜 Historical Context and the Torsion Balance

Formulated by the French physicist Charles Augustin de Coulomb in 1785, this law quantifies the attractive or repulsive force between two charges. Since advanced simulation software or multimeters did not exist at the time, Coulomb developed a highly sensitive mechanical apparatus known as a **Torsion Balance**.

### The Experimental Process: Measuring the Invisible Before the Electron

Charles Coulomb published his findings more than **110 years before** J.J. Thomson discovered the electron (1897). Instead of knowing the absolute quantity of elementary charges, Coulomb relied on **geometric symmetry and proportions** to isolate his variables:

1. **Controlling Charge Fractions ($q_1 \cdot q_2$):**
   To vary the charge without an absolute meter, he used the principle of conduction via contact. He would electrify a polished conductive sphere with an unknown charge $Q$, and then touch it against an identical, neutral sphere. Due to geometric symmetry, the net charge was forced to divide perfectly in half ($\frac{1}{2}Q$). By repeating this process, he could precisely manipulate charge fractions ($\frac{1}{2}, \frac{1}{4}, \frac{1}{8}$) without knowing the exact number of electrons involved.

2. **Dependency on Distance ($1/r^2$):**
   By keeping the charges constant and varying the distance ($r$) between the spheres, he measured the rotation angle of the suspension wire. He observed that:
   * Doubling the distance ($2r$) made the electrostatic force **4 times weaker** ($\frac{1}{4}F$).
   * Tripling the distance ($3r$) made the force **9 times weaker** ($\frac{1}{9}F$).
   * *Conclusion:* The force is inversely proportional to the square of the distance: $F \propto \frac{1}{r^2}$.

> [!NOTE]
> 
> Observe that the Force vs. Distance ($F \times r$) graph plots a **second-degree hyperbola** (inverse-square curve). This visually maps the indirect proportion and the sharp decay of force as distance increases.

### Mechanical Apparatus Mechanics

The torsion balance consisted of a fine silver or silk wire suspending a horizontal insulating rod:
* **One end** held a small conductive sphere (the target charge).
* **The opposite end** held a counterweight made of an uncharged insulating material (such as paper or wax), purely to maintain mechanical equilibrium without electrical interference.

When a second, identically charged fixed sphere was introduced into the system, the electrostatic repulsion pushed the movable sphere, twisting the suspension wire. The wire exerted a mechanical restoring torque proportional to the twist angle (Hooke's Law for torsion). By reading the stable angular displacement on a graduated glass scale, Coulomb calculated the exact electrostatic force.

Combining these empirical observations yielded the famous scalar relationship:
$$F = k \frac{|q_1 \cdot q_2|}{r^2}$$

---

## 🔬 The Mathematical Vector Concept

Although Coulomb deduced the relation in a scalar form, engineering and Multivariable Calculus (Calculus III) demand a vector approach to model complex three-dimensional systems.

The magnitude of the force is dictated by:
* **Electrostatic Constant ($k$):** $k = \frac{1}{4\pi\epsilon_0} \approx 8.99 \times 10^9 \text{ N}\cdot\text{m}^2/\text{C}^2$
* **Permittivity of Free Space ($\epsilon_0$):** $\epsilon_0 \approx 8.85 \times 10^{-12} \text{ C}^2/\text{N}\cdot\text{m}^2$

### 🎯 Vector Notation (Vector Calculus)

The vector force exerted by the source charge ($1$) onto the target charge ($2$) is written as:

$$\vec{F}_{1\to2} = k \frac{q_1 \cdot q_2}{r^2} \hat{r}_{1\to2}$$

Where $\hat{r}_{1 \to 2} = \frac{\vec{r}_{1 \to 2}}{r}$ is the unit vector (versor) pointing in a straight line from charge 1 to charge 2. If the product $q_1 \cdot q_2$ is positive, the force assumes the same direction and sense as the unit vector (repulsion); if it is negative, it assumes the opposite sense (attraction).

---

## 🧩 Principle of Superposition

In a system containing multiple charges operating in space, the net force acting on a specific charge is the **vector sum** of all individual forces exerted on it by the other charges:

$$\vec{F}_{res} = \vec{F}_{1} + \vec{F}_{2} + \vec{F}_{3} + \dots = \sum_{i=1}^{n} \vec{F}_{i}$$

> [!CAUTION]
> 
> **Classic Engineering Trap:** Never sum the magnitudes of the forces directly unless all charges are collinear (on the same straight line). Always decompose the forces into their Cartesian components ($\hat{i}, \hat{j}, \hat{k}$) before calculating the summation.