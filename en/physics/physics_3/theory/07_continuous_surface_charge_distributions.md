
#  Theory: Surface Distributions — Generic Derivation of a Charged Disk

The calculation of the electric field for two-dimensional charged surfaces expands our infinitesimal modeling from a 1D line to a 2D surface. By building upon the cylindrical foundations established in line charge problems, we can resolve surface distributions with minimal algebraic friction. This document outlines the general derivation for a uniformly charged flat disk, a classic precursor to understanding infinite sheets and parallel-plate capacitors.

---

##  Analysis Scenario and Axis Selection

Imagine a flat, circular, non-conducting disk of radius $R$ carrying a uniform surface charge. To maximize geometric symmetry, we place the disk flat on the $xy$-plane, centered perfectly at the origin $(0, 0, 0)$. Our goal is to calculate the net electric field $\vec{E}$ at a target point $P$ located along the central symmetry axis (the $z$-axis) at a height $z$.



>  **Engineering Insight:** Why lock point $P$ strictly to the central $z$-axis? Just like with the wire, choosing the central axis builds a framework of rotational symmetry. If we tried to calculate the field at a point off the central axis, the azimuthal symmetry would break, forcing us to solve the problem using elliptic integrals that cannot be evaluated in terms of elementary functions. Keeping $P$ on the axis turns a potential nightmare into clean, manageable calculus.

---

##  The Resolution Pipeline (4-Step Algorithm)

### Step 1: Transitioning from the Line Model to the Surface Model (The Physics)

When dealing with a two-dimensional surface, we monitor charge distribution per unit area. We define the **Surface Charge Density ($\sigma$)**:

$$
\sigma = \frac{\text{Total Charge}}{\text{Total Area}} = \frac{Q}{A} \quad \left[\text{Unit: } \frac{\text{Coulomb}}{\text{meter}^2}\right]
$$

For a continuous, uniform distribution, this ratio scales down to an infinitesimal patch of area $dA$:

$$
\sigma = \frac{dq}{dA} \implies dq = \sigma \cdot dA
$$

To integrate across a circular disk, we do not slice it into Cartesian squares ($dx \cdot dy$), which would lead to miserable radical limits. Instead, we decompose the disk into concentric, microscopic **rings** of radius $r'$ and infinitesimal radial thickness $dr'$. 



Unrolling one of these thin rings yields a rectangle of length equal to the circumference ($2\pi r'$) and width $dr'$. Therefore, our differential area element is:

$$
dA = 2\pi r' dr'
$$

Substituting this into our charge density equation gives the physics translation for our source:

$$
dq = \sigma (2\pi r' dr')
$$

---

### Step 2: The Conversion Kit (Reusing Cylindrical Frameworks)

Since we have already mastered the cylindrical conversion kit, we bypass the full derivation and directly map our position vectors. Because the source charges live entirely on the flat base of our cylinder ($xy$-plane at $z=0$) and the target point $P$ sits on the flagpole ($z$-axis), our spatial vectors simplify directly:

1. **Vector where the charge element is located ($\vec{r}'$):** The ring element sits on the plane at a radial distance $r'$ from the center, pointing in the dynamic radial direction $\hat{a}_\rho$. It has zero height: $\vec{r}' = r'\hat{a}_\rho$.
2. **Vector where the target point $P$ is located ($\vec{r}$):** Point $P$ has zero radial distance from the axis and sits entirely at height $z$: $\vec{r} = z\hat{k}$.

Subtracting these vectors yields the **Relative Position Vector ($\vec{r}_{\text{rel}}$)** pointing from the charge element to the target point:

$$
\vec{r}_{\text{rel}} = \vec{r} - \vec{r}' = -r'\hat{a}_\rho + z\hat{k}
$$

#### The Intensity Modulus (The Denominator):
Applying our backward conversion kit, the magnitude of this relative vector is found via a direct right triangle on our flagpole:

$$
|\vec{r}_{\text{rel}}| = \sqrt{(r')^2 + z^2}
$$

Assembling these components into the continuous infinitesimal form of Coulomb's Law gives our primary setup equation:

$$
\vec{E} = \frac{1}{4\pi\epsilon_0} \int_{0}^{R} \frac{\sigma (2\pi r' dr')}{[(r')^2 + z^2]^{3/2}} \left( -r'\hat{a}_\rho + z\hat{k} \right)
$$

---

### Step 3: The Vector Symmetry Filter

Expanding the integral exposes two distinct directional actions: a radial component ($-\hat{a}_\rho$) pulling inward/pushing outward parallel to the disk, and a vertical component ($\hat{k}$) pushing along the axis.

Because our ring element wraps a full $2\pi$ around the origin, every individual charge piece $dq$ on one side of the ring has a symmetric "twin" directly opposite it ($180^\circ$ away).



While their vertical contributions reinforce each other, their horizontal radial pushes ($\hat{a}_\rho$) point in diametrically opposed directions and cancel out completely over the full integration sweep:

$$
\int_{0}^{2\pi} \hat{a}_\rho d\phi = 0 \implies \vec{E}_\rho = 0
$$

The entire horizontal component vanishes, leaving exclusively the vertical axial projection:

$$
\vec{E} = \frac{2\pi\sigma z \hat{k}}{4\pi\epsilon_0} \int_{0}^{R} \frac{r' dr'}{[(r')^2 + z^2]^{3/2}}
$$

Simplifying the constants outside the integral block yields:

$$
\vec{E} = \frac{\sigma z \hat{k}}{2\epsilon_0} \int_{0}^{R} \frac{r' dr'}{[(r')^2 + z^2]^{3/2}}
$$

---

### Step 4: The Calculus Engine ($u$-Substitution)

Unlike the line charge problem which required a trigonometric substitution hack, this surface integral contains its own internal derivative tool. Because the numerator houses an $r' dr'$ term, we can solve this quickly using standard **$u$-substitution**.

Let our inner polynomial be $u$:

$$
u = (r')^2 + z^2
$$

Taking the differential with respect to our integration variable $r'$ (remembering that the height $z$ acts as a constant relative to the disk surface):

$$
du = 2r' dr' \implies r' dr' = \frac{du}{2}
$$

Now we map our boundary limits from $r'$ limits to $u$ limits:
* Lower limit: When $r' = 0 \implies u = z^2$
* Upper limit: When $r' = R \implies u = R^2 + z^2$

Substituting these translations into our calculus engine transforms the expression into a basic power rule integral:

$$
\int_{z^2}^{R^2 + z^2} \frac{1}{u^{3/2}} \frac{du}{2} = \frac{1}{2} \int_{z^2}^{R^2 + z^2} u^{-3/2} du
$$

Executing the integration:

$$
\frac{1}{2} \left[ \frac{u^{-1/2}}{-1/2} \right]_{z^2}^{R^2 + z^2} = -\left[ \frac{1}{\sqrt{u}} \right]_{z^2}^{R^2 + z^2} = \left[ \frac{1}{\sqrt{z^2}} - \frac{1}{\sqrt{R^2 + z^2}} \right]
$$

Since $\sqrt{z^2} = |z|$, and assuming we are analyzing a point on the positive $z$-axis ($z > 0$), this simplifies directly to:

$$
\left( \frac{1}{z} - \frac{1}{\sqrt{R^2 + z^2}} \right)
$$

---

##  The Final Leap: Boundary Contours

Recombining this completed integration value with the constants we isolated outside the block in **Step 3**, we get our consolidated engineering equation for the electric field of a finite disk:

$$
\vec{E} = \frac{\sigma z \hat{k}}{2\epsilon_0} \left( \frac{1}{z} - \frac{1}{\sqrt{R^2 + z^2}} \right)
$$

Distributing the $z$ term into the brackets yields the standard textbook form:

$$
\vec{E} = \frac{\sigma}{2\epsilon_0} \left( 1 - \frac{z}{\sqrt{R^2 + z^2}} \right) \hat{k}
$$

### Scenario A: The Infinite Sheet ($R \to \infty$)
If the radius of the disk expands infinitely, or if our target point $P$ is placed so incredibly close to the surface that the disk looks like an endless horizon ($z \ll R$), the fraction term drops to zero:

$$
\lim_{R \to \infty} \frac{z}{\sqrt{R^2 + z^2}} = 0
$$

This isolates the fundamental, constant field formula for an **Infinite Sheet of Charge**:

$$
\vec{E} = \frac{\sigma}{2\epsilon_0} \hat{k}
$$

> [!IMPORTANT]
> 
> **The Ultimate Gauss's Law Spoiler**
> 
> Notice that the electric field of an infinite sheet has no dependence on distance ($z$). Whether you are $1\text{ mm}$ or $10\text{ meters}$ away, the field pushing against you has the exact same strength.
> 
> You will find this exact same equation in the next chapter using **Gauss's Law** with a cylindrical pillbox. Deriving it here via brute-force integration proves *why* the geometry works and shows why Gauss's Law is such a powerful shortcut for engineers.