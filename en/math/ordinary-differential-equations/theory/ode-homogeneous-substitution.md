---
id: ode-homogeneous-substitution
title: Homogeneous Differential Equations by Substitution
domain: math
module: ordinary-differential-equations
type: method
schema_version: "2.0"
level: advanced
language: en
prerequisites:
  - ode-separable
tags:
  - differential-equations
  - homogeneous-substitution
  - separation-of-variables
  - scale-invariance
---

# Homogeneous Differential Equations by Substitution

## The Rigorous Concept of Homogeneity (Scale Symmetry)

In differential equations, the term "homogeneous" carries distinct meanings depending on the context. While in higher-order linear ODEs it denotes the absence of a forcing term ($L[y] = 0$), in the context of first-order ODEs covered in this module, **homogeneity is an algebraic-geometric property of scale invariance of the coefficients**.

### Formal Definition of a Homogeneous Function

A multivariate function $f(x,y)$ is said to be **homogeneous of degree $k$** if, when simultaneously rescaling all its arguments by a real scalar factor $\lambda \neq 0$, the resulting function is multiplied by the scaling factor $\lambda^k$:

$$f(\lambda x, \lambda y) = \lambda^k f(x,y)$$

#### The Formal Constant Test

To verify whether a function is homogeneous of degree $k$, apply the substitution $x \to \lambda x$ and $y \to \lambda y$:

* If it is possible to factor out $\lambda^k$ as a global common factor and restore the original expression $f(x,y)$, the function is homogeneous of degree $k$.
* If the scalar term $\lambda$ remains trapped inside transcendental functions (such as $\sin(\lambda x)$, $e^{\lambda y}$, or $\ln(\lambda x)$) without the possibility of factorization, the function is **not** homogeneous.

### The ODE in Homogeneous Form

An ordinary differential equation in differential form:

$$M(x,y) \, dx + N(x,y) \, dy = 0$$

is said to be **homogeneous** if both coefficients $M(x,y)$ and $N(x,y)$ are homogeneous functions of the **same degree $k$**.

Alternatively, isolating the derivative $y' = \frac{dy}{dx} = -\frac{M(x,y)}{N(x,y)}$, the quotient of two homogeneous functions of the same degree yields a zero-degree function ($k - k = 0$). This implies that the rate of change depends exclusively on the **dimensionless ratio** of the variables:

$$y' = F\left(\frac{y}{x}\right)$$

---

## Structural Comparison: Homogeneous ODE vs. Exact ODE

Although both are expressed in the universal form $M(x,y) \, dx + N(x,y) \, dy = 0$, the underlying properties tested and their geometric natures are entirely distinct:

* **Exact ODE:** Evaluates whether $M\,dx + N\,dy$ is the total differential $dF$ of a potential surface $z = F(x,y)$. The validation test is Schwarz's symmetry ($\frac{\partial M}{\partial y} = \frac{\partial N}{\partial x}$).
* **Homogeneous ODE:** Evaluates whether the direction field is invariant under radial dilation. The validation test is the equality of scale degrees of $M$ and $N$ ($M(\lambda x, \lambda y) = \lambda^k M$ and $N(\lambda x, \lambda y) = \lambda^k N$).

---

## Geometric Foundations: Radial Dilation Invariance

The geometric foundation underlying First-Order Homogeneous ODEs by Substitution lies in the concept of **scale invariance (radial dilation symmetry)**.

### Families of Solutions and Radial Ray Lines

When $M(x,y)$ and $N(x,y)$ share the same degree of homogeneity $k$, the slope of the direction field depends exclusively on the ratio of the variables rather than the radial distance from the origin:

$$y' = -\frac{M(x,y)}{N(x,y)} = F\left(\frac{y}{x}\right)$$

Geometrically, this property implies that:

* **Constant slopes along rays:** Along any radial line $y = c \cdot x$ passing through the origin, the ratio $y/x = c$ remains strictly constant. Consequently, all solution curves crossing this line exhibit the exact same slope at that intersection point.
* **Dilation symmetry:** If $y = \phi(x)$ is a solution curve, any rescaled version $y = \frac{1}{\lambda} \phi(\lambda x)$ is also a valid solution to the same ODE.

The substitution $u = y/x$ uncouples $x$ and $y$ precisely because it replaces the Cartesian coordinate $y$ with a variable $u$ representing the slope of the polar ray, converting the radial symmetry into a separable differential equation.

---

## The Substitution Algorithm and Order Reduction

The core strategy for solving a Homogeneous ODE consists of transforming it into a **Separable Variable ODE** via the substitution $y = u \cdot x$.

### Derivation of the Substitution Differential

Considering $u = u(x)$ as a new dependent function of $x$, apply the **Product Rule** to obtain the total differential:

$$dy = d(u \cdot x) = u \, dx + x \, du$$

### Steps for Resolution

* **Substitution of Terms:** Replace $y$ with $u \cdot x$ and $dy$ with $u \, dx + x \, du$ in the original ODE.
* **Factorization and Cancellation of Degree $k$:** The term $x^k$ factors out universally from both coefficients and cancels out.
* **Grouping Like Terms:** Regroup terms in $dx$ and $du$.
* **Separation of Variables:** Isolate variable $u$ on one side and $x$ on the other.
* **Integration and Reversion to Original Variable:** Integrate both sides and substitute $u = \frac{y}{x}$ back.

---

## Worked Examples

### Example: Solving a Degree 2 Homogeneous ODE

Find the general solution of the ordinary differential equation:

$$(x^2 + y^2) \, dx - 2xy \, dy = 0$$

**Resolution:**

#### Verification of Homogeneity Degree
* $M(x,y) = x^2 + y^2 \implies M(\lambda x, \lambda y) = \lambda^2 x^2 + \lambda^2 y^2 = \lambda^2 M(x,y)$ (Degree 2).
* $N(x,y) = -2xy \implies N(\lambda x, \lambda y) = -2(\lambda x)(\lambda y) = \lambda^2 (-2xy) = \lambda^2 N(x,y)$ (Degree 2).

Since both functions are homogeneous of degree $k = 2$, the ODE is homogeneous by substitution (even though $\frac{\partial M}{\partial y} = 2y \neq -2y = \frac{\partial N}{\partial x}$, proving it is not exact).

#### Application of Substitution
Apply $y = u \cdot x$ and $dy = u \, dx + x \, du$:

$$(x^2 + (ux)^2) \, dx - 2x(ux) (u \, dx + x \, du) = 0$$

$$(x^2 + u^2 x^2) \, dx - 2u x^2 (u \, dx + x \, du) = 0$$

Factor out $x^2$:

$$x^2 \left[ (1 + u^2) \, dx - 2u (u \, dx + x \, du) \right] = 0$$

Divide by $x^2$ ($x \neq 0$):

$$(1 + u^2) \, dx - 2u^2 \, dx - 2u x \, du = 0$$

$$(1 - u^2) \, dx - 2u x \, du = 0$$

#### Separation of Variables

$$\frac{1}{x} \, dx = \frac{2u}{1 - u^2} \, du$$

#### Integration of Both Sides

$$\int \frac{1}{x} \, dx = \int \frac{2u}{1 - u^2} \, du$$

$$\ln|x| = -\ln|1 - u^2| + C_1 \implies \ln|x(1 - u^2)| = C_1$$

$$x(1 - u^2) = C$$

#### Reversion to Original Variable ($u = y/x$)

$$x \left( 1 - \frac{y^2}{x^2} \right) = C \implies x^2 - y^2 = C x$$