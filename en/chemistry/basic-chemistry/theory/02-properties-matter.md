---
id: properties_of_matter
title: Properties of Matter
---
# Properties of Matter and System Characterization

## Introduction

In the study of Chemistry, characterizing a material system requires determining how matter responds to physical and chemical stimuli. Although all matter occupies space and possesses mass, different materials exhibit unique behaviors when subjected to variations in temperature, pressure, or interactions with other substances.

To understand how materials are identified and applied, the analysis is organized around the distinction between general and specific properties, utilizing measurable quantities and conceptual models.

---

## Fundamental Classification of Properties

The properties of a material system are divided into two main categories based on their ability to identify the substance that constitutes the sample.

### General Properties

When comparing a concrete block and a gold bar of identical volume, both occupy space in the environment and offer resistance when attempting to alter their position. These characteristics confirm the presence of matter in both bodies, but they provide no information regarding their chemical composition.

General properties are inherent to any and all samples of matter, regardless of their chemical constitution. They vary directly with the amount of matter present in the system.

The primary general properties include:

* **Mass ($m$):** A quantitative measure of inertia and the amount of matter contained in a body.
* **Volume ($V$):** The amount of three-dimensional space occupied by the system.
* **Impenetrability:** The principle stating that two bodies cannot occupy the same place in space simultaneously.
* **Inertia:** The tendency of a body to maintain its state of rest or uniform linear motion unless acted upon by a non-zero net external force.
* **Compressibility and Elasticity:** The capacity of matter to reduce its volume under external forces and return to its original shape when those forces are removed.

Because they depend on the extent of the sample, general properties do not allow for the identification of the substance being analyzed. In formal and thermodynamic terms, they belong to the class of extensive properties. A property $P$ is extensive if its total value for the overall system equals the sum of its values for each of its component subsystems.

For a system partitioned into $n$ independent subsystems, the total extensive property $P_{\text{total}}$ is expressed as:

$$P_{\text{total}} = \sum_{i=1}^{n} P_i$$

>[!NOTE] 
>
>Continuous Media and Volume Integration
>
>Considering a continuous medium with local mass density $\rho(\mathbf{r})$ contained within a three-dimensional region of space $\Omega$, the total volume $V$ and total mass $m$ are formally defined by integrals over the domain:
>
>$$V = \iiint_{\Omega} dV$$
>
>$$m = \iiint_{\Omega} \rho(\mathbf{r}) \, dV$$
>
>Where $\mathbf{r}$ represents the position vector in Euclidean space.

---

### Specific Properties

If two identical containers hold colorless liquids with exactly equal volumes and masses, these basic measurements will not reveal which liquid is water and which is pure ethanol. However, measuring the temperature at which each liquid boils or determining the mass contained within a specific unit of volume provides immediate and precise differentiation.

Specific properties depend exclusively on the chemical identity and structural arrangement of matter. They remain unchanged regardless of the quantity or size of the analyzed sample, serving as fundamental criteria for characterizing and identifying pure substances.

They are classified as:

* **Physical Properties:** Can be measured or observed without altering the chemical composition of the substance (e.g., melting point, boiling point, density, electrical and thermal conductivity).
* **Chemical Properties:** Describe the ability of a substance to undergo reactions that transform its chemical identity (e.g., reactivity with acids, flammability, oxidation potential).
* **Organoleptic Properties:** Perceived through the sense organs (e.g., color, odor, taste, and luster).

Specific properties correspond to thermodynamic intensive properties, remaining invariant under division or changes in system scale. The most prominent parameter in material characterization is density ($\rho$), defined as the ratio between mass ($m$) and volume ($V$):

$$\rho = \frac{m}{V}$$

In the International System of Units (SI), density is expressed in $\text{kg/m}^3$, though practical units such as $\text{g/cm}^3$ and $\text{g/mL}$ are also common (where $1\text{ g/cm}^3 = 1000\text{ kg/m}^3$). Intensive physical properties are fixed thermodynamic constants for pure substances under standardized pressure and temperature conditions.

>[!NOTE] 
>
>Differential Limit Definition in Heterogeneous Media
>An intensive property $y(\mathbf{r})$ can be defined mathematically as the limit ratio between two extensive properties $P_1$ and $P_2$ as the sampling volume approaches a differential element $dV$:
>
>$$y(\mathbf{r}) = \lim_{\Delta V \to 0} \frac{\Delta P_1}{\Delta P_2}$$
>
>Thus, in non-homogeneous systems, density is defined locally by the differential ratio between mass $dm$ and volume $dV$:
>
>$$\rho = \frac{dm}{dV}$$

---

## Comparative Synthesis of Properties

| Classification Criterion | Extensive Properties (General) | Intensive Properties (Specific / State) |
| :--- | :--- | :--- |
| **Dependence on Mass/Size** | Depend on the amount of matter in the sample. | Independent of the amount of matter in the sample. |
| **Behavior Upon Sample Division** | Total value is the sum of parts ($P_{\text{total}} = \sum P_i$). | Value remains invariant in any fraction of the sample. |
| **Identification Capacity** | Cannot identify the substance (measures dimensions only). | Identifies the substance (acts as a "fingerprint"). |
| **Direct Physical Examples** | Mass ($m$), Volume ($V$), Heat capacity ($C$), Internal energy ($U$). | Density ($\rho$), Melting point ($\text{MP}$), Boiling point ($\text{BP}$), Solubility ($C_s$). |
| **System State Examples** | Amount of substance ($n$), Surface area ($A$). | Temperature ($T$), Pressure ($P$), Viscosity ($\eta$). |

---

## Quantitative Measurements and Specific Physical Properties

Rigorous material characterization requires quantifying physical properties using standardized quantities.

### Phase Transition Points

When heating a lead bar and an aluminum block, each metal transitions to the liquid state at entirely different temperatures. These fixed temperatures act as distinctive hallmarks for each element or compound.

* **Melting Point ($\text{MP}$):** The exact temperature at which a pure substance transitions from solid to liquid under a given atmospheric pressure.
* **Boiling Point ($\text{BP}$):** The temperature at which the vapor pressure of a liquid equals the external pressure exerted on its surface, causing the transition to the gaseous state throughout the entire mass of the system.

During a phase transition of a pure substance at constant pressure, the temperature remains strictly constant. The amount of heat $q$ required to induce the phase change is directly proportional to the sample mass $m$ and the specific latent heat $L$:

$$q = m \cdot L$$

Where $L$ is a specific property expressed in SI units as Joules per kilogram ($\text{J/kg}$) or practically as calories per gram ($\text{cal/g}$).

>[!NOTE] 
>
>Statistical Mechanics Perspective
>From a statistical viewpoint, melting and boiling points represent critical temperatures where the average thermal agitation energy ($k_B T$) reaches the value necessary to overcome the potential energies of intermolecular attraction within the crystal lattice or liquid phase.

---

### Solubility as a Specific Property

Adding table salt to water causes the solid to dissolve up to a specific limit. Beyond a certain point, no matter how vigorously the system is stirred, additional salt collects at the bottom of the container. There is a maximum dissolution capacity dictated by the nature of both solute and solvent.

Solubility is the maximum amount of a substance (solute) capable of dissolving in a fixed quantity of another substance (solvent) at a specified temperature and pressure, forming a homogeneous system. Systems that have reached this limit are termed saturated solutions.

The solubility coefficient ($C_s$) is defined quantitatively as the maximum mass of solute ($m_{\text{solute, max}}$) soluble in a fixed mass of solvent ($m_{\text{solvent}}$) at temperature $T$:

$$C_s(T) = \frac{m_{\text{solute, max}}}{m_{\text{solvent}}}$$

Typically, the coefficient is expressed in the practical unit of grams of solute per $100\text{ g}$ of solvent ($\text{g solute} / 100\text{ g } \text{H}_2\text{O}$).

>[!NOTE] 
>
>Thermodynamic Equilibrium of Phases
>Thermodynamically, solubility equilibrium occurs when the chemical potential of the solute in the solid phase ($\mu_{\text{solid}}$) equals its chemical potential in the solution phase ($\mu_{\text{solution}}$):
>
>$$\mu_{\text{solid}}(T, P) = \mu_{\text{solution}}(T, P, x)$$
>
>Where $x$ represents the mole fraction of the dissolved solute.
