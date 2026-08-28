---
id: "base-conversion"
title: "Number Base Conversion"
domain: "engineering"
type: "method"
language: "en"
tags:
  - "digital-electronics"
  - "number-systems"
  - "base-conversion"
  - "binary"
  - "hexadecimal"
prerequisites:
  - "fundamental-number-systems"
---
# Number Base Conversion

## Overview of Methods

Transitioning numerical representations between different bases is a fundamental operation in low-level programming, hardware design, and digital system analysis. Conversion algorithms fall into two primary categories:

1. **Arithmetic Methods:** Used when one of the bases involved is Decimal ($b=10$). These require explicit division operations or polynomial expansions.
2. **Direct Mapping Methods (Grouping):** Used between bases that are exact powers of $2$ ($2^1$ Binary, $2^3$ Octal, $2^4$ Hexadecimal). These require no complex arithmetic, relying solely on block substitution of bits.

---

## Conversion from Any Base to Decimal

To convert a number from an arbitrary base $b$ to Decimal ($10$), the **Polynomial Positional Expansion** method is applied.

### Algorithm
Multiply each digit $d_i$ by base $b$ raised to its positional index $i$, then sum all terms:

$$N_{10} = \sum_{i=0}^{n-1} d_i \cdot b^i = d_{n-1} \cdot b^{n-1} + \dots + d_1 \cdot b^1 + d_0 \cdot b^0$$

### Application Across All Three Bases ($b=2, b=8, b=16$)

The same polynomial expansion solves the conversion to decimal regardless of the source base:

#### 1. From Binary ($b=2$) to Decimal
Convert $1101_2$ to decimal:

$$N_{10} = (1 \cdot 2^3) + (1 \cdot 2^2) + (0 \cdot 2^1) + (1 \cdot 2^0)$$
$$N_{10} = 8 + 4 + 0 + 1 = 13_{10}$$

#### 2. From Octal ($b=8$) to Decimal
Convert $157_8$ to decimal:

$$N_{10} = (1 \cdot 8^2) + (5 \cdot 8^1) + (7 \cdot 8^0)$$
$$N_{10} = 64 + 40 + 7 = 111_{10}$$

#### 3. From Hexadecimal ($b=16$) to Decimal
Convert $3\text{F}_{16}$ to decimal (where $\text{F} = 15$):

$$N_{10} = (3 \cdot 16^1) + (\text{F} \cdot 16^0)$$
$$N_{10} = (3 \cdot 16) + (15 \cdot 1)$$
$$N_{10} = 48 + 15 = 63_{10}$$

---

## Conversion from Decimal to Any Base

To convert an integer decimal number to a target base $b$, the **Successive Division by $b$** algorithm is applied.

### Algorithm
1. Divide the decimal number $N$ by the target base $b$.
2. Record the **remainder** of the division.
3. Take the **integer quotient** and divide it again by $b$.
4. Repeat this process until the quotient reaches zero.
5. The number in the target base is constructed by reading the remainders in **reverse order** (from the last remainder to the first).

### Worked Example: Decimal to Binary
Convert $25_{10}$ to Binary ($b=2$):

| Division | Integer Quotient | Remainder | Position in Result |
| :--- | :--- | :--- | :--- |
| $25 \div 2$ | $12$ | **1** | LSB (Least Significant Bit) |
| $12 \div 2$ | $6$ | **0** | |
| $6 \div 2$ | $3$ | **0** | |
| $3 \div 2$ | $1$ | **1** | |
| $1 \div 2$ | $0$ | **1** | MSB (Most Significant Bit) |

Reading remainders from bottom to top: $25_{10} = 11001_2$.

---

## Direct Conversion Between Binary, Hexadecimal, and Octal

Because $16 = 2^4$ and $8 = 2^3$, conversions between these bases bypass successive divisions and rely on **static bit grouping**.

> [!NOTE]
> If the total number of bits is not an exact multiple of the block size (4 bits for Hexadecimal or 3 bits for Octal), **pad the most significant block (MSB) with zeros on the left** until complete.

---

### Binary $\leftrightarrow$ Hexadecimal Grouping (4-bit Blocks)

Each hexadecimal digit corresponds exactly to a 4-bit group (nibble).

#### Worked Example: 10-bit Number Non-Multiple of 4
Convert the 10-bit binary value $1101011001_2$ to Hexadecimal:

1. **Splitting from the right (LSB):** `11` | `0101` | `1001`
2. **Zero Padding (Left-padding):** The leftmost block has only 2 bits (`11`). Two leading zeros are added to complete the 4-bit nibble: **`0011`** | `0101` | `1001`
3. **Nibble Mapping:**
   * `0011` $\rightarrow 0 + 0 + 2 + 1 = 3_{16}$
   * `0101` $\rightarrow 0 + 4 + 0 + 1 = 5_{16}$
   * `1001` $\rightarrow 8 + 0 + 0 + 1 = 9_{16}$
4. **Final Result:** $1101011001_2 = 359_{16}$

---

### Binary $\leftrightarrow$ Octal Grouping (3-bit Blocks)

Each octal digit corresponds exactly to a 3-bit group.

#### Worked Example: 10-bit Number Non-Multiple of 3
Convert the same 10-bit binary value $1101011001_2$ to Octal:

1. **Splitting from the right (LSB):** `1` | `101` | `011` | `001`
2. **Zero Padding (Left-padding):** The leftmost block has only 1 bit (`1`). Two leading zeros are added to complete the 3-bit block: **`001`** | `101` | `011` | `001`
3. **Triplet Mapping (3 bits):**
   * `001` $\rightarrow 0 + 0 + 1 = 1_8$
   * `101` $\rightarrow 4 + 0 + 1 = 5_8$
   * `011` $\rightarrow 0 + 2 + 1 = 3_8$
   * `001` $\rightarrow 0 + 0 + 1 = 1_8$
4. **Final Result:** $1101011001_2 = 1531_8$

---

## Bridge to Systems Programming

> [!TIP]
> In programming languages such as C and Assembly, prefixes like `0x359` (Hexadecimal) and `01531` (Octal) are used strictly in source code. Compilers convert these values directly into equivalent binary representations in memory. When inspecting registers and raw memory dumps, the ability to mentally group bits into blocks of 3 or 4 eliminates the need for intermediate decimal conversions.