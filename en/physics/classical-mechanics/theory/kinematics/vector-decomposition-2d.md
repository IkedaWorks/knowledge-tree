---
id: "vector-decomposition"
title: "Understanding Vector Decomposition"
domain: "physics"
module: "classical-mechanics"
type: "concept"
schema_version: "2.0"
level: "beginner"
language: "en"
prerequisites: []
tags:
  - "physics"
  - "kinematics"
  - "vectors"
  - "vector-decomposition"
  - "statics"
---

# Understanding Vector Decomposition

While geometric methods such as the Parallelogram Law and the Polygonal Rule are intuitive for combining a few forces, their graphical complexity escalates rapidly when evaluating concurrent systems with multiple forces. Vector **decomposition** (or resolution) resolves this limitation by projecting a single diagonal force into orthogonal scalar components along reference axes.

---

## Motivation and Formal Definition

Consider a diagonal pulling force applied to a rolling suitcase. Physically, this single vector induces two simultaneous effects: horizontal translation along the floor and vertical unloading of the normal force.

Decomposing a vector translates a single inclined force $\vec{F}$ into two mutually perpendicular component vectors—one along the horizontal axis ($\vec{F}_x$) and one along the vertical axis ($\vec{F}_y$)—whose vector sum is equivalent to the original force:

$$\vec{F} = \vec{F}_x + \vec{F}_y$$

---

## Classification and Boundary Cases

### Reference Angle Dependency

The trigonometric expression assigned to each component depends strictly on the geometric orientation of the reference angle $\theta$ relative to the coordinate axes:

- **Angle relative to the Horizontal Axis:** The horizontal component is adjacent to the angle ($\cos$), and the vertical component is opposite ($\sin$).
- **Angle relative to the Vertical Axis:** The vertical component is adjacent to the angle ($\cos$), and the horizontal component is opposite ($\sin$).

| Reference Angle Position | Horizontal Component ($F_x$) | Vertical Component ($F_y$) |
| :--- | :---: | :---: |
| **Measured from Horizontal ($x$-axis)** | $F_x = F \cdot \cos(\theta)$ | $F_y = F \cdot \sin(\theta)$ |
| **Measured from Vertical ($y$-axis)** | $F_x = F \cdot \sin(\phi)$ | $F_y = F \cdot \cos(\phi)$ |

![Vector Decomposition relative to Horizontal Axis](./../../../../../assets/physics/classical-mechanics/vector-decomposition-2d.svg)

![Vector Decomposition relative to Vertical Axis](./../../../../../assets/physics/classical-mechanics/vector-decomposition-2d-inverted.svg)

---

## Proof and Mathematical Formulation

### Trigonometric Derivation on the Cartesian Plane

Given a force vector $\vec{F}$ forming a right triangle with its projections on the Cartesian plane:

1. **Standard Case (Angle $\theta$ with the $x$-axis):**

Using fundamental trigonometric ratios:

$$\cos(\theta) = \frac{F_x}{F} \implies F_x = F \cdot \cos(\theta)$$

$$\sin(\theta) = \frac{F_y}{F} \implies F_y = F \cdot \sin(\theta)$$

2. **Inverted Case (Angle $\phi$ with the $y$-axis):**

When the angle $\phi$ is specified relative to the vertical axis, the adjacent leg corresponds to $F_y$ and the opposite leg corresponds to $F_x$:

$$\cos(\phi) = \frac{F_y}{F} \implies F_y = F \cdot \cos(\phi)$$

$$\sin(\phi) = \frac{F_x}{F} \implies F_x = F \cdot \sin(\phi)$$

---

## Practical Application and Worked Examples

### Unit Vector Representation and Equipollence

To express decomposed vectors algebraically without relying on diagrams, standard dimensionless unit vectors $\hat{i}$ and $\hat{j}$ (or $\vec{i}$ and $\vec{j}$) are defined along the positive $x$- and $y$-axes, respectively, with magnitude $\|\hat{i}\| = \|\hat{j}\| = 1$.

The complete Cartesian vector representation is formulated as:

$$\vec{F} = F_x \hat{i} + F_y \hat{j}$$

> [!NOTE]
> **Equipollence:** The components $F_x \hat{i}$ and $F_y \hat{j}$ represent equipollent free vectors. They carry identical magnitude, direction, and sense regardless of the application point on a rigid body.

---

### Conceptual Pitfall: Blind Memorization of Axis Projections

A frequent misconception is assuming that the $x$-axis component always uses the cosine function ($F_x = F \cos\theta$) and the $y$-axis component always uses the sine function ($F_y = F \sin\theta$).

$$\text{Incorrect (when angle is vertical): } F_x = F \cdot \cos(\phi)$$

#### Deconstruction

Cosine is strictly associated with the **adjacent leg** of the reference right triangle, not the horizontal spatial axis. If the reference angle is measured relative to the vertical line, the adjacent component becomes $F_y$, causing $F_x$ to depend on $\sin(\phi)$.

---

## Connections and Advanced Applications

> [!TIP]
> **Computational Applications:** Cartesian vector decomposition is essential for multi-body dynamic simulations and structural finite element analysis (FEA). By converting diagonal vector interactions into independent orthogonal scalar systems ($\sum F_x = m a_x$ and $\sum F_y = m a_y$), complex 2D and 3D mechanics problems become algebraically solvable by algorithms.