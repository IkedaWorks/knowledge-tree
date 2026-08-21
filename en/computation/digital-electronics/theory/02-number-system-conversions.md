---
id: number_system_conversions
title: Number Systems and Conversions
---
# Number Systems and Conversions

Human mathematics was shaped by a biological accident: the fact that we have ten fingers on our hands. This led us to create a counting system based on cycles of ten. However, when we started building machines to calculate for us, we realized that physics does not have "ten fingers." The nature of electrical circuits is binary: there is either voltage or no voltage; the switch is either open or closed.

The fundamental problem of digital electronics stems from this physical constraint. How can we represent any magnitude in the universe, from the color of a pixel to a bank account balance, using only two fundamental states? And, more importantly: how can we humans read and design these representations without getting lost in an endless sea of ones and zeros?

## The Direct Bridge: The Decimal System as Our Mirror

Before looking at circuits, let's look at what we already do every day. When we say the number $17_{10}$ in decimal, our brain doesn't think of complex formulas, but what we are actually doing is grouping quantities into powers of ten:

$$
17_{10} = (1 \times 10^1) + (7 \times 10^0)
$$

This means: we have **1** group of ten and **7** loose units. The small subscript $_10$ at the end of the number is just a formal notice indicating: "hey, this number is written using groups of ten."

Any base's number system works on this exact same grouping principle. The only difference is the "group size." In decimal, the group is ten; in binary, the group is two; in hexadecimal, the group is sixteen.

## The Formalism of Positional Notation and Base Notations

Any number, in any mathematical base, can be decomposed into a sum of powers of its base. This hidden structure is what allows us to jump from one system to another without losing information integrity.

To avoid confusion, we use very clear notation conventions:
- **Binary:** Digits $0$ and $1$, frequently accompanied by the subscript $_2$ (e.g., $10001_2$) or the prefix `0b`.
- **Decimal:** Digits from $0$ to $9$, subscript $_{10}$ (e.g., $17_{10}$).
- **Hexadecimal:** Digits $0-9$ and letters $A-F$ ($A=10, B=11, C=12, D=13, E=14, F=15$). We indicate this base with the subscript $_{16}$ (e.g., $11_{16}$) or with the prefix `0x` (e.g., $0x11$).

## Conversion Mechanisms: The Logic of Packing

Converting between bases is the process of "unpacking" a number from its current base and "repacking" it into the target base.

### Why do we divide the number by the target base?
When you successively divide a number (like $17_{10}$) by the target base ($2$), you are answering a fundamental mechanical question: **"How many complete groups of the new base's size fit in here?"** The quotient is what remains for the next level of grouping, and the remainder is precisely the amount left over (the digit of that position).

### Conversion Practical Matrix

Here is the map to navigate between bases:

| Conversion | Method |
| :--- | :--- |
| **Decimal to Any Base** | Successive divisions by the target base. |
| **Any Base to Decimal** | Sum of powers (Multiply each digit by the position weight). |
| **Binary to Hexadecimal** | Grouping into blocks of $4$ bits (*nibbles*), from right to left. |
| **Hexadecimal to Binary** | Expansion of each hexadecimal digit into $4$ binary bits. |

### Practical Conversion Examples

**1. From Decimal ($17_{10}$) to Binary ($2$):**
Divide by $2$ and note the remainders:
- $17 \div 2 = 8$ (Remainder **$1$**)
- $8 \div 2 = 4$ (Remainder **$0$**)
- $4 \div 2 = 2$ (Remainder **$0$**)
- $2 \div 2 = 1$ (Remainder **$0$**)
- $1 \div 2 = 0$ (Remainder **$1$**)
Reading the remainders from bottom to top: **$10001_2$**.

**2. From Binary ($10001_2$) to Decimal ($10$):**
Multiply each bit by its weight ($2^n$):
- $(1 \times 2^4) + (0 \times 2^3) + (0 \times 2^2) + (0 \times 2^1) + (1 \times 2^0)$
- $16 + 0 + 0 + 0 + 1 = \mathbf{17_{10}}$.

**3. From Binary ($11001011_2$) to Hexadecimal ($16$):**
Group into $4$ bits (from right to left):
- $1100_2 \rightarrow 12 \rightarrow \mathbf{C}$
- $1011_2 \rightarrow 11 \rightarrow \mathbf{B}$
Result: **$0xCB_{16}$**.

**4. From Hexadecimal ($0xCB$) to Decimal ($10$):**
Multiply by the weight of each position ($16^n$):
- $(C \times 16^1) + (B \times 16^0)$
- $(12 \times 16) + (11 \times 1) = 192 + 11 = \mathbf{203_{10}}$.

> [!TIP]
> In practical hardware projects, such as configuring microcontroller I/O ports, we rarely write configuration in pure binary. We group logic switches in sets of four and write in hexadecimal, fusing fundamental machine precision with human readability.