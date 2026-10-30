---
id: "ode-exact"
title: "Exact Differential Equations and Integrating Factors"
domain: "math"
module: "ordinary-differential-equations"
type: "method"
schema_version: "2.0"
level: "advanced"
language: "en"
prerequisites:
  - "single-variable-calculus"
  - "ode-fundamental-concepts"
  - "ode-solutions"
tags:
  - "differential-equations"
  - "exact-odes"
  - "integrating-factor"
  - "partial-derivatives"
  - "potential-function"
  - "level-curves"
---

# Exact Differential Equations and Integrating Factors

## Differential Form and the Exactness Criterion

A first-order ordinary differential equation written in differential form:

$$M(x,y) \, dx + N(x,y) \, dy = 0$$

is said to be **exact** in a simply connected region $R \subset \mathbb{R}^2$ if the left-hand side expression is the total differential $dF$ of some multivariate function $F(x,y)$, termed the **potential function**.

If such a function $F(x,y)$ exists, its total differential is defined by:

$$dF = \frac{\partial F}{\partial x} dx + \frac{\partial F}{\partial y} dy = M(x,y) dx + N(x,y) dy$$

establishing a direct correspondence between the functions in the ODE and the partial derivatives of the potential:

$$\frac{\partial F}{\partial x} = M(x,y) \quad \text{and} \quad \frac{\partial F}{\partial y} = N(x,y)$$

Consequently, the ODE reduces to the statement $dF = 0$, whose general solution is given by the family of implicit relations $F(x,y) = C$.

---

## Geometric Foundations: Implicit Solutions and Level Curves

A frequent conceptual misconception when studying Exact ODEs is confusing the **potential function $F(x,y)$** with the **solution of the differential equation**.

### The Difference Between the 3D Surface and the ODE Solution

The potential function $z = F(x,y)$ belongs to Multivariable Calculus and defines a **three-dimensional surface** in space $\mathbb{R}^3$, where each pair $(x,y)$ is assigned a height $z$. However, the differential equation being addressed is **ordinary** (describing the variation of a single dependent variable $y$ with respect to $x$).

The function $F(x,y)$ itself is not the solution of the ODE, but rather an auxiliary geometric construct.

### The Secant Plane and the Level Curve

Imposing the exactness condition $dF = 0$ requires the value of $F(x,y)$ to remain strictly constant. Graphically, this is equivalent to intersecting the three-dimensional surface $z = F(x,y)$ with a **horizontal plane** fixed at height $z = C$.

If we imagine this horizontal plane $z = C$ slicing through the surface $z = F(x,y)$, the contour or trace left by this intersection is a one-dimensional line: the **level curve** $F(x,y) = C$.

The projection of this line onto the Cartesian plane $xy$ is the true solution to the Ordinary Differential Equation. It describes the trajectory $y(x)$ of a particle moving along the surface while maintaining a constant altitude ($dz = 0$).

For this reason, the solution to an Exact ODE is expressed in **implicit form** $F(x,y) = C$.

### Intuitive Numerical Example (Without ODE)

To visualize this concept in isolation, consider the simple multivariate function:

$$F(x,y) = x^2 + y^2$$

In three-dimensional space $\mathbb{R}^3$, the equation $z = x^2 + y^2$ describes a **paraboloid of revolution** (a bowl-shaped surface).

When we fix a specific height, for instance $z = 4$, we intersect this bowl with the horizontal plane at height $4$:

$$x^2 + y^2 = 4$$

The intersection of the 3D surface with the plane $z = 4$ yields a circle of radius $2$. The equation $x^2 + y^2 = 4$ does not describe the 3D bowl, but rather the two-dimensional circle in the $xy$ plane.

If we isolate $y$, we obtain the explicit solutions $y(x) = \pm\sqrt{4 - x^2}$. It is this one-dimensional relation $y(x)$ (the mark left by the cut) that corresponds to the object of study of an ordinary differential equation.

![Geometric Interpretation of Exact ODEs: Slice of potential surface z = F(x,y) by plane z = C generating level curves x^2 + y^2 = C on the xy-plane](./../../../../../assets/math/ordinary-differential-equations/exact-ode-level-curve.svg)


### Algebraic-Geometric Connection: Case Study

To visualize the direct correspondence between the ODE and the three-dimensional illustration above, consider the exact differential equation:

$$x \, dx + y \, dy = 0$$

#### Reconstruction of the Potential Function

Applying the reconstruction method via union of terms:

* $I_1 = \int x \, dx = \frac{x^2}{2}$
* $I_2 = \int y \, dy = \frac{y^2}{2}$

Combining terms and rescaling the arbitrary integration constant yields the potential function:

$$F(x,y) = x^2 + y^2$$

#### Physical and Geometric Interpretation

* **The Potential Surface:** The equation $z = x^2 + y^2$ defines the paraboloid of revolution displayed in the 3D plot.
* **The Secant Plane:** The condition $dF = 0$ requires the altitude to remain strictly constant. For constant $C = 1$, the paraboloid is sliced by the horizontal plane at height $z = 1$.
* **The Implicit Solution:** The intersection trace projected onto the Cartesian $xy$-plane is the level curve:

$$x^2 + y^2 = 1$$

Isolating $y$ yields explicit solutions $y(x) = \pm\sqrt{1 - x^2}$, describing the one-dimensional trajectory along which the differential $dF$ vanishes.

---

## Theorem of the Exactness Criterion

By Schwarz's Theorem on the symmetry of mixed partial derivatives, if $F(x,y)$ is smooth, its second-order partial derivatives satisfy $\frac{\partial^2 F}{\partial y \partial x} = \frac{\partial^2 F}{\partial x \partial y}$.

Since $M = \frac{\partial F}{\partial x}$ and $N = \frac{\partial F}{\partial y}$, substituting these equalities yields the necessary and sufficient condition for $M dx + N dy = 0$ to be exact:

$$\frac{\partial M}{\partial y} = \frac{\partial N}{\partial x}$$

---

## Methods for Reconstructing the Potential Function $F(x,y)$

There are two equivalent approaches for reconstructing $F(x,y)$ once exactness is confirmed.

### Method 1: Construction by Partial Integration and Boundary Adjustment

1. **Partial Integration in $x$:** Integrate $M(x,y)$ with respect to $x$, treating $y$ as a constant:
   $$F(x,y) = \int M(x,y) \, dx + g(y)$$
   where $g(y)$ represents terms depending exclusively on $y$ that were eliminated during partial differentiation with respect to $x$.

2. **Determination of $g(y)$:** Differentiate the resulting expression with respect to $y$ and set it equal to the known term $N(x,y)$:
   $$\frac{\partial F}{\partial y} = \frac{\partial}{\partial y}\left( \int M(x,y) \, dx \right) + g'(y) = N(x,y)$$
   Isolate $g'(y)$ and integrate with respect to $y$ to determine $g(y)$.

3. **Assembling the Solution:** Substitute $g(y)$ back into $F(x,y)$ and set it equal to constant $C$:
   $$F(x,y) = C$$

---

### Method 2: Reconstruction by Union of Non-Repeating Terms

#### Theoretical Justification

When partially differentiating $F(x,y)$ with respect to $x$, terms depending exclusively on $y$ vanish. When differentiating with respect to $y$, terms depending exclusively on $x$ vanish. Mixed terms survive in both partial derivatives.

Thus, integrating $M(x,y)$ in $x$ and $N(x,y)$ in $y$ independently recovers all components of function $F(x,y)$, with the sole caveat that mixed terms appear duplicated.

#### Method Algorithm

1. Calculate the indefinite integral of $M(x,y)$ with respect to $x$:
   $$I_1(x,y) = \int M(x,y) \, dx$$

2. Calculate the indefinite integral of $N(x,y)$ with respect to $y$:
   $$I_2(x,y) = \int N(x,y) \, dy$$

3. Construct $F(x,y)$ by taking the union of all terms in $I_1$ and $I_2$, writing identical terms only once:
   $$F(x,y) = \text{Union without repetition of } \{I_1(x,y), I_2(x,y)\}$$

4. Formulate the general solution by setting the resulting union equal to $C$.

---

## Integrating Factors: The Origin of the Product Rule

When $\frac{\partial M}{\partial y} \neq \frac{\partial N}{\partial x}$, the ODE is not exact. We search for a function $\mu(x,y)$ to rescale the equation, making it exact:

$$\mu(x,y) M(x,y) \, dx + \mu(x,y) N(x,y) \, dy = 0$$

The new equation must satisfy Schwarz's criterion:

$$\frac{\partial}{\partial y}\bigl[ \mu M \bigr] = \frac{\partial}{\partial x}\bigl[ \mu N \bigr]$$

Applying the **Product Rule for Partial Derivatives** on both sides:

$$\mu \frac{\partial M}{\partial y} + M \frac{\partial \mu}{\partial y} = \mu \frac{\partial N}{\partial x} + N \frac{\partial \mu}{\partial x}$$

Rearranging terms containing $\mu$:

$$\mu \left( \frac{\partial M}{\partial y} - \frac{\partial N}{\partial x} \right) = N \frac{\partial \mu}{\partial x} - M \frac{\partial \mu}{\partial y}$$

This equality is a Partial Differential Equation (PDE). To transform it into an Ordinary Differential Equation solvable by separation of variables, we assume that $\mu$ depends on only one of the variables:

### Case 1: Integrating Factor Depending Only on $x$
If $\mu = \mu(x)$, then $\frac{\partial \mu}{\partial y} = 0$ and partial derivative $\frac{\partial \mu}{\partial x}$ becomes ordinary derivative $\frac{d\mu}{dx}$. The equation reduces to:

$$\mu \left( \frac{\partial M}{\partial y} - \frac{\partial N}{\partial x} \right) = N \frac{d\mu}{dx} \implies \frac{1}{\mu} \frac{d\mu}{dx} = \frac{\dfrac{\partial M}{\partial y} - \dfrac{\partial N}{\partial x}}{N}$$

For $\mu(x)$ to be determined exclusively as a function of $x$, the right-hand side ratio **must depend solely on $x$**. Denoting this ratio by $f(x)$:

$$f(x) = \frac{\dfrac{\partial M}{\partial y} - \dfrac{\partial N}{\partial x}}{N} \implies \mu(x) = e^{\int f(x) \, dx}$$

### Case 2: Integrating Factor Depending Only on $y$
If $\mu = \mu(y)$, then $\frac{\partial \mu}{\partial x} = 0$. By analogous reasoning:

$$g(y) = \frac{\dfrac{\partial N}{\partial x} - \dfrac{\partial M}{\partial y}}{M} \implies \mu(y) = e^{\int g(y) \, dy}$$

---

## Worked Examples

### Example 1: Direct Exact Equation
Find the general solution of the ordinary differential equation:

$$(2x y + 3) \, dx + (x^2 - 1) \, dy = 0$$

**Resolution:**

**1. Verification of the Exactness Criterion:**
$M(x,y) = 2xy + 3$ and $N(x,y) = x^2 - 1$.

$$\frac{\partial M}{\partial y} = 2x, \quad \frac{\partial N}{\partial x} = 2x$$

Since $\dfrac{\partial M}{\partial y} = \dfrac{\partial N}{\partial x} = 2x$, Schwarz's criterion is satisfied and the ODE is exact.

**2. Reconstruction of $F(x,y)$ via the Union of Terms Method:**
- $I_1 = \int (2xy + 3) \, dx = x^2 y + 3x$
- $I_2 = \int (x^2 - 1) \, dy = x^2 y - y$

Taking the union of terms without repetition: $F(x,y) = x^2 y + 3x - y$.

**3. General Solution:**

$$x^2 y + 3x - y = C$$

---

### Example 2: Equation with Single-Variable Integrating Factor

**Find the general solution of the ordinary differential equation:**

$$(2y + x^2) \, dx + x \, dy = 0, \quad (x > 0)$$

**Resolution:**

**1. Verification of the Exactness Criterion:**

Identify $M(x,y) = 2y + x^2$ and $N(x,y) = x$.

$$\frac{\partial M}{\partial y} = 2, \quad \frac{\partial N}{\partial x} = 1$$

Since $\dfrac{\partial M}{\partial y} = 2 \neq 1 = \dfrac{\partial N}{\partial x}$, the equation is not exact.

**2. Determination of Integrating Factor $\mu(x)$:**

Calculate the dependency ratio relative to $N(x,y)$:

$$\frac{\dfrac{\partial M}{\partial y} - \dfrac{\partial N}{\partial x}}{N} = \frac{2 - 1}{x} = \frac{1}{x}$$

Since result $f(x) = \dfrac{1}{x}$ depends **exclusively on $x$**, integrating factor $\mu(x)$ is calculated directly by:

$$\mu(x) = e^{\int f(x) \, dx} = e^{\int \frac{1}{x} \, dx} = e^{\ln x} = x$$

Multiplying the entire original ODE by $\mu(x) = x$:

$$x(2y + x^2) \, dx + x(x) \, dy = 0 \implies (2xy + x^3) \, dx + x^2 \, dy = 0$$

**3. Verification of the New Exact ODE:**

For the new equation, $M_1(x,y) = 2xy + x^3$ and $N_1(x,y) = x^2$:

$$\frac{\partial M_1}{\partial y} = 2x, \quad \frac{\partial N_1}{\partial x} = 2x$$

The new equation is strictly exact.

**4. Reconstruction of Potential $F(x,y)$ (Union of Terms Method):**

- Integrating $M_1$ with respect to $x$:
  $$I_1 = \int (2xy + x^3) \, dx = x^2 y + \frac{x^4}{4}$$

- Integrating $N_1$ with respect to $y$:
  $$I_2 = \int x^2 \, dy = x^2 y$$

Taking the union of terms from $I_1$ and $I_2$ without repetition:

$$F(x,y) = x^2 y + \frac{x^4}{4}$$

**5. General Solution:**

Setting the potential function equal to constant $C$:

$$x^2 y + \frac{x^4}{4} = C \implies y(x) = \frac{C}{x^2} - \frac{x^2}{4}$$