---
id: fundamental-number-systems
title: Fundamental Number Systems
domain: engineering
type: concept
language: en
tags:
  - digital-electronics
  - number-systems
  - binary
  - hexadecimal
prerequisites:
  - basic-arithmetic-operations
  - exponentiation
---
# Fundamental Number Systems

## Intuition and Physical Necessity

Counting in base $10$ (decimal) is a biological convention stemming from human anatomy (ten fingers), rather than an intrinsic law of mathematics or physics. In computer engineering, attempting to represent ten distinct electrical voltage levels (such as $0\text{V}, 0.5\text{V}, 1.0\text{V}, \dots, 4.5\text{V}$) inside an integrated circuit makes the system highly vulnerable to electrical noise, thermal fluctuations, and reading errors.

To guarantee noise immunity and high fault tolerance, digital electronics operate using the minimum possible number of stable physical states: **two** (switch open or closed, presence or absence of voltage).

> [!NOTE]
> This physical constraint necessitates the adoption of the **Binary System**, where the smallest unit of information (a bit) can only hold the values $0$ (LOW / Absence of Signal) or $1$ (HIGH / Presence of Signal).

---

## Structure of Positional Systems

All numerical systems used in computing are **positional**. This means that the numerical value assigned to a symbol depends strictly on its position within the sequence.

The total number of unique symbols available in a system defines its **Base** ($b$):

| System | Base ($b$) | Unique Symbols Used | Role in Computational Context |
| :--- | :--- | :--- | :--- |
| **Decimal** | $10$ | $\{0, 1, 2, 3, 4, 5, 6, 7, 8, 9\}$ | Human interface and general counting. |
| **Binary** | $2$ | $\{0, 1\}$ | Native hardware language and logic gates. |
| **Hexadecimal** | $16$ | $\{0, 1, \dots, 9, \text{A}, \text{B}, \text{C}, \text{D}, \text{E}, \text{F}\}$ | Compact human-readable representation for binary data. |
| **Octal** | $8$ | $\{0, 1, 2, 3, 4, 5, 6, 7\}$ | 3-bit grouping (historical systems and POSIX permissions). |

In the Hexadecimal system, letters **A** through **F** are used to represent decimal values $10$ through $15$ using a single character:

$$\text{A} = 10, \quad \text{B} = 11, \quad \text{C} = 12, \quad \text{D} = 13, \quad \text{E} = 14, \quad \text{F} = 15$$

---

## Formalization of Positional Notation

Any integer $N$ written in a base $b$, composed of $n$ digits ordered as $d_{n-1} d_{n-2} \dots d_1 d_0$, has its value determined by weighting each position $i$ with the corresponding power of the base:

$$N_{10} = \sum_{i=0}^{n-1} d_i \cdot b^i = d_{n-1} \cdot b^{n-1} + d_{n-2} \cdot b^{n-2} + \dots + d_1 \cdot b^1 + d_0 \cdot b^0$$

Where:
* $b$ is the **base** of the number system.
* $d_i$ is the **digit** at position $i$ (where $0 \le d_i < b$).
* $i$ is the **position index**, counted from right to left starting at zero.

---

## Rationale for Hexadecimal and Octal

Computers process and store data exclusively in binary. However, long bit sequences (such as $110101101011_2$) are difficult for humans to read and are prone to transcription errors.

Hexadecimal ($16 = 2^4$) and Octal ($8 = 2^3$) systems exist not to replace binary in hardware, but to serve as a **shorthand notation**:
* **1 Hexadecimal digit** represents the exact state of **4 bits** ($1$ Nibble).
* **1 Octal digit** represents the exact state of **3 bits**.

---

## Bridge to Systems Programming

> [!TIP]
> In programming languages such as C and Assembly, hardware registers and memory addresses use the `0x` prefix to denote Hexadecimal notation (e.g., `0xFF` or `0x20000000`). Using hexadecimal allows developers to inspect hardware bit patterns directly without cluttering source code with long sequences of zeros and ones. To learn arithmetic transition techniques between these bases, refer to the **base-conversion** note.