
# Probability, Statistics, and Stochastic Modeling

This module consolidates the mathematical and computational framework required to quantify uncertainty, analyze experimental data dispersion, and model probabilistic phenomena. Rather than taking a purely theoretical approach, topics are dissected through the anatomy of their equations, connecting statistical formalism to the practical realities of engineering and algorithm development.

##  Prerequisites

* **Discrete Mathematics & Algebra:** Mastery of summations ($\sum$), set theory, and elementary algebra.
* **Vector & Differential Calculus:** Partial derivatives, total differentials (essential for error propagation), and definite integrals (for continuous distributions).

##  Learning Roadmap & Note Structure

The module is structured chronologically and incrementally, divided into the following analytical fronts:

### 01. Central Tendency Measures and Sample Behavior
* **Focus:** Determining the center of gravity of raw data sets.
* **Concepts:** Arithmetic mean, median, and mode. Analysis of symmetry and the impact of outliers on central tendency metrics.

### 02. Data Dispersion and the Anatomy of RMS
* **Focus:** Quantifying the variability and noise inherent in any measurement process.
* **Concepts:** Variance, Sample Standard Deviation ($N-1$) vs. Population Standard Deviation ($\sigma$). The formalism of Bessel's Correction (degrees of freedom) and the mathematical bridge to statistical effective value (Root Mean Square - RMS).

### 03. Theoretical Metrology and Measurement Uncertainty
* **Focus:** Calculating the reliability parameter and the geometric margin of doubt of an experimental result.
* **Concepts:** Type A Uncertainty (statistical fluctuation dampened by $\sqrt{n}$), Type B Uncertainty (hardware limits normalized by $\sqrt{3}$), and Combined Quadratic Uncertainty ($u_c$). Expansion formalism ($U = k \cdot u_c$) and differential equations for Uncertainty Propagation in indirect measurements.

### 04. Multivariate Analysis and Data Synchronicity
* **Focus:** Mapping the joint behavior between two or more independent variables.
* **Concepts:** Geometry of Sample Covariance, Pearson's Correlation Coefficient ($r$) as a vector normalization metric, and an introduction to linear regression models.

### 05. Probability Theory and Stochastic Models
* **Focus:** Transitioning from static data analysis to predictive modeling of random events.
* **Concepts:** Sample space, axioms of probability, discrete random variables (Binomial, Poisson), and continuous random variables (Normal / Gaussian Distribution).