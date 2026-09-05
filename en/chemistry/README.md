---
id: chemistry
title: Chemistry Domain
type: domain
language: en
tags:
  - chemistry
  - natural-sciences
  - matter
modules:
  - basic-chemistry
---
# General Chemistry Domain

> "Nothing in life is to be feared, it is only to be understood. Now is the time to understand more, so that we may fear less." — Marie Curie

## Overview

This domain serves as the primary entry point for the study of chemical science. It organizes core chemical principles into structured learning modules, covering everything from fundamental atomic structure to specialized advanced disciplines.

## Domain Roadmap

```mermaid
flowchart LR
    %% Core Module
    subgraph L1 [Level 1 · Core]
        BC([Basic Chemistry])
    end

    %% Foundation Modules
    subgraph L2 [Level 2 · Foundations]
        IC[Inorganic Chemistry]
        OC[Organic Chemistry]
        PC[Physical Chemistry]
        AC[Analytical Chemistry]
    end

    %% Specializations
    subgraph L3 [Level 3 · Specializations]
        BIO[Biochemistry]
    end

    %% Connections
    BC ==> IC
    BC ==> OC
    BC ==> PC
    BC ==> AC

    OC --> BIO

    %% Estilização Místico-Minimalista de Alto Contraste
    style BC fill:#18181b,stroke:#d4d4d4,stroke-width:2px,color:#ffffff
    style IC fill:#0f172a,stroke:#475569,stroke-width:1px,color:#f8fafc
    style OC fill:#0f172a,stroke:#475569,stroke-width:1px,color:#f8fafc
    style PC fill:#0f172a,stroke:#475569,stroke-width:1px,color:#f8fafc
    style AC fill:#0f172a,stroke:#475569,stroke-width:1px,color:#f8fafc
    style BIO fill:#0f172a,stroke:#475569,stroke-width:1px,color:#f8fafc
```

## Modules

| Module                                       | Description                                                                    | Level        | Status        |
| :------------------------------------------- | :----------------------------------------------------------------------------- | :----------- | :------------ |
| [Basic Chemistry](basic-chemistry/README.md) | Foundational principles, atomic theory, states of matter, and stoichiometry.   | Beginner     | **Available** |
| Inorganic Chemistry                          | Study of inorganic compounds, transition metals, and coordination chemistry.   | Intermediate | *Planned*     |
| Organic Chemistry                            | Carbon-based chemistry, functional groups, reaction mechanisms, and synthesis. | Intermediate | *Planned*     |
| Physical Chemistry                           | Chemical thermodynamics, kinetics, quantum mechanics, and electrochemistry.    | Advanced     | *Planned*     |
| Analytical Chemistry                         | Qualitative and quantitative analysis methods, titrimetry, and spectrometry.   | Advanced     | *Planned*     |
| Biochemistry                                 | Chemical processes within and relating to living organisms.                    | Advanced     | *Planned*     |

## Prerequisites

* **Mathematics**: Elementary algebra, basic logarithms, and introductory calculus.
* **Physics**: Fundamentals of energy, work, and electrostatics.