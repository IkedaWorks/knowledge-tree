---
id: "dielectrics"
title: "Dielectrics, Polarization Mechanisms, and Bound Charges"
domain: "physics"
module: "electromagnetism"
type: "concept"
schema_version: "2.0"
level: "intermediate"
language: "en"
prerequisites:
  - "capacitance"
  - "electric-dipole-moment"
  - "vector-calculus-divergence"
tags:
  - "electrostatics"
  - "dielectrics"
  - "polarization"
  - "bound-charges"
  - "susceptibility"
---


# Dielectrics, Polarization Mechanisms, and Bound Charges

## Context and Physical Foundations

Consider a parallel-plate capacitor in a vacuum subject to a free surface charge density $+\sigma$ on the left plate and $-\sigma$ on the right plate. These charges establish a uniform electric field $\mathbf{E}_0$ directed to the right.

When filling the volume between the plates with a perfect conducting material, free electrons instantly migrate to the boundaries until the electric field inside the material is completely canceled ($\mathbf{E} = 0$).

However, when the interposed medium is an electrical insulator (dielectric), the electrons remain bound to their respective atomic nuclei by attractive Coulomb forces. The external electric field $\mathbf{E}_0$ cannot produce macroscopic current conduction, but it deforms the atomic structure of the medium:
* The negative electron clouds undergo a displacement in the direction opposite to the field.
* The positive atomic nuclei are displaced in the direction of the field.

This micro-displacement transforms neutral atoms into induced electric dipoles. The sum of these microscopic dipole moments alters the net electrostatic field inside the medium, reducing the total field intensity without canceling it completely. The need to quantify and predict this attenuation of the electric field by matter motivated the formulation of the theory of dielectric media.

---

## Theoretical Formulation

### Polarization Mechanism and Field Opposition

Consider the atomic model where the positive nucleus and the negative electron cloud are connected by a linear restoring force (analogous to an atomic spring). In the absence of an external field, the center of positive charge coincides with the center of negative charge, resulting in a zero dipole moment.

Under the action of an external field $\mathbf{E}_0$, the induced dipole $\mathbf{p}$ aligns with the field. To describe the polarization state on a macroscopic scale, the **Polarization Vector ($\mathbf{P}$)** is defined as the volume density of electric dipole moments:

$$\mathbf{P} = \lim_{\Delta V \to 0} \frac{1}{\Delta V} \sum_{i=1}^{N \Delta V} \mathbf{p}_i = \frac{d\mathbf{p}}{dV}$$

In the International System of Units (SI), the dimension of $\mathbf{P}$ is expressed in Coulombs per square meter ($\text{C/m}^2$).

![Polarization mechanism in dielectrics.](./../../../../dielectric-polarization-mechanism.svg)
*Figure 1: Polarization mechanism in a homogeneous dielectric. Inside the volume, opposite charges of adjacent dipoles mutually neutralize. At the boundaries of the material, an uncompensated distribution of bound charges ($\sigma_b$) emerges.*

---

### Bound Charge Formation ($\sigma_b$ and $\rho_b$)

Inside the volume of a homogeneous and uniformly polarized dielectric, the positive pole of an atomic dipole lies adjacent to the negative pole of the contiguous dipole, maintaining volumetric charge neutrality. At the boundary surfaces of the material, however, this mutual compensation does not occur, resulting in an accumulation of **Surface Bound Charges ($\sigma_b$)**.

Unlike free charges, bound charges belong to the atomic structure of the insulator itself and cannot be removed by conduction or grounding.

#### Surface Bound Charge Density ($\sigma_b$)
The total charge passing through an area $A$ at the boundary of the dielectric is given by the dot product between the polarization vector and the unit normal vector $\hat{\mathbf{n}}$ pointing outward from the medium:

$$\sigma_b = \mathbf{P} \cdot \hat{\mathbf{n}}$$

#### Volume Bound Charge Density ($\rho_b$)
If the polarization is non-uniform in space, charge cancellation inside the volume fails, creating a volumetric accumulation of charge tied to the spatial divergence of the vector $\mathbf{P}$:

$$\rho_b = -\nabla \cdot \mathbf{P}$$

In homogeneous media subjected to uniform fields, $\nabla \cdot \mathbf{P} = 0$, which implies $\rho_b = 0$. Bound charges manifest solely on the surfaces of the dielectric.

---

### Net Electric Field and Linear Media

The surface bound charges $+\sigma_b$ and $-\sigma_b$ generate an internal induced electric field $\mathbf{E}_{\text{induced}}$ directed opposite to the applied field $\mathbf{E}_0$. The net electric field $\mathbf{E}$ inside the dielectric is given by superposition:

$$\mathbf{E} = \mathbf{E}_0 - \mathbf{E}_{\text{induced}}$$

For **Linear, Isotropic, and Homogeneous (LIH) Media**, the magnitude of polarization $\mathbf{P}$ is directly proportional to the internal net electric field $\mathbf{E}$:

$$\mathbf{P} = \varepsilon_0 \chi_e \mathbf{E}$$

where:
* $\chi_e$ is the **Electric Susceptibility** of the medium (a dimensionless constant).
* $\varepsilon_0$ is the vacuum permittivity ($\approx 8.854 \times 10^{-12} \text{ F/m}$).

The **Relative Permittivity ($\varepsilon_r$)** (or dielectric constant) is defined as:

$$\varepsilon_r = 1 + \chi_e$$

The relationship between the applied electric field and the resulting internal field in the dielectric simplifies to:

$$\mathbf{E} = \frac{\mathbf{E}_0}{\varepsilon_r}$$

---

## Examples and Solved Problems

### Determination of Field and Charges in a Linear Dielectric

**Problem:** A homogeneous slab of Teflon ($\varepsilon_r = 2.10$) is positioned perpendicular to an applied electric field in vacuum with magnitude $E_0 = 4.2 \times 10^4 \text{ V/m}$ oriented in the $+x$ direction. Determine:
* The net electric field $\mathbf{E}$ inside the teflon.
* The polarization vector $\mathbf{P}$ of the material.
* The surface bound charge densities $\sigma_b$ on both faces normal to the $x$-axis.

#### Solution:

##### Net Electric Field
The internal field is reduced by the factor of the relative permittivity $\varepsilon_r$:

$$\mathbf{E} = \frac{\mathbf{E}_0}{\varepsilon_r} = \frac{4.2 \times 10^4 \hat{\mathbf{a}}_x}{2.10} = 2.0 \times 10^4 \hat{\mathbf{a}}_x \text{ V/m}$$

##### Susceptibility and Polarization Vector
The susceptibility of teflon is given by:

$$\chi_e = \varepsilon_r - 1 = 2.10 - 1 = 1.10$$

Applying the constitutive relation for linear media:

$$\mathbf{P} = \varepsilon_0 \chi_e \mathbf{E}$$

$$\mathbf{P} = (8.854 \times 10^{-12} \text{ F/m}) \cdot (1.10) \cdot (2.0 \times 10^4 \hat{\mathbf{a}}_x \text{ V/m})$$

$$\mathbf{P} = 1.948 \times 10^{-7} \hat{\mathbf{a}}_x \text{ C/m}^2 \approx 0.195 \hat{\mathbf{a}}_x \, \mu\text{C/m}^2$$

##### Surface Bound Charge Densities
* **Right Face ($\hat{\mathbf{n}} = +\hat{\mathbf{a}}_x$):**
  $$\sigma_{b,\text{right}} = \mathbf{P} \cdot (+\hat{\mathbf{a}}_x) = +0.195 \, \mu\text{C/m}^2$$

* **Left Face ($\hat{\mathbf{n}} = -\hat{\mathbf{a}}_x$):**
  $$\sigma_{b,\text{left}} = \mathbf{P} \cdot (-\hat{\mathbf{a}}_x) = -0.195 \, \mu\text{C/m}^2$$

---

### Volume Charge Density in Non-Uniform Polarization

**Problem:** Consider a cylindrical region where the polarization vector of a dielectric varies radially according to the function $\mathbf{P}(r) = k r^2 \hat{\mathbf{a}}_r$ in cylindrical coordinates, where $k$ is a positive constant. Calculate the volume bound charge density $\rho_b$ inside the medium.

#### Solution:
The volume bound charge density is related to the divergence of the polarization vector:

$$\rho_b = -\nabla \cdot \mathbf{P}$$

In cylindrical coordinates, the divergence of a vector field with only a radial component $P_r(r) = k r^2$ is given by:

$$\nabla \cdot \mathbf{P} = \frac{1}{r} \frac{\partial}{\partial r} (r P_r) = \frac{1}{r} \frac{\partial}{\partial r} (r \cdot k r^2) = \frac{1}{r} \frac{\partial}{\partial r} (k r^3)$$

Evaluating the partial derivative:

$$\nabla \cdot \mathbf{P} = \frac{1}{r} (3 k r^2) = 3 k r$$

Substituting into the expression for volume bound charge:

$$\rho_b = -3 k r$$

The spatial dependence indicates a non-zero accumulation of negative bound charge in the volume of the medium, with its magnitude increasing linearly with radius $r$.

---

## Applications and Advanced Connections

### Dielectric Breakdown Limit and Dielectric Strength
The elastic response of polarization has a critical physical limit. If the intensity of the applied electric field exceeds the **Dielectric Strength ($E_{\text{max}}$)** of the insulator, the electrostatic force exerted on the electrons will overcome the nuclear attraction force. Dielectric breakdown (ionization) occurs, turning the insulator into a conductor and creating a destructive electrical discharge.

| Material | Relative Permittivity ($\varepsilon_r$) | Dielectric Strength ($E_{\text{max}}$ in $\text{kV/mm}$) |
| :--- | :--- | :--- |
| **Vacuum** | $1.00000$ | Infinity |
| **Dry Air (1 atm)** | $1.00059$ | $3.0$ |
| **Teflon (PTFE)** | $2.10$ | $60.0$ |
| **Transformer Paper** | $3.50$ | $16.0$ |
| **Pyrex Glass** | $4.70$ | $14.0$ |
| **Barium Titanate ($\text{BaTiO}_3$)** | $1250.00$ | $5.0$ |

### Reformulation of Gauss's Law and the Electric Displacement Vector ($\mathbf{D}$)
To circumvent the need to explicitly track bound charges in complex electrostatic problems, the **Electric Displacement Vector ($\mathbf{D}$)** is defined:

$$\mathbf{D} = \varepsilon_0 \mathbf{E} + \mathbf{P}$$

The differential form of Gauss's Law in matter depends exclusively on the **free charge density ($\rho_f$)**:

$$\nabla \cdot \mathbf{D} = \rho_f$$

In linear media, the relationship simplifies to $\mathbf{D} = \varepsilon \mathbf{E}$, allowing the calculation of electric fields in complex geometries with dielectrics using the same analytical methods applied to a vacuum.