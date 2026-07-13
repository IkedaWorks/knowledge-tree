
# Introduction to Numerical Sequences

A numerical sequence is an ordered list of elements arranged in a discrete structure. Unlike a standard set in set theory — where the order of elements does not alter the object —, the position occupied by each element in a sequence is fundamental to its definition.

Every sequence is a function. However, the converse is not true, since not every function is a sequence.

## Formal Definition

Formally, a real sequence is defined as a function whose domain is the set of non-zero Natural Numbers and whose codomain is the set of Real Numbers:

$$f: \mathbb{N}^* \to \mathbb{R}$$

- **Domain ($\mathbb{N}^*$):** Represents the set of positions or indices of the terms ($1, 2, 3, \dots$).
    
- **Codomain ($\mathbb{R}$):** Represents the values assumed by each term ($a_n = f(n)$).
    

## Why is the Mapping from $\mathbb{N}^*$ to $\mathbb{R}$?

The choice of input and output sets addresses specific structural requirements:

### Why is the Domain Discrete ($\mathbb{N}^*$)?

If the domain were the set of real numbers ($\mathbb{R} \to \mathbb{R}$), the object would cease to be a sequence and become a **continuous function**. In a continuous function, there are no "steps," but rather an uninterrupted flow of values along the line.

Choosing $\mathbb{N}^*$ guarantees **discretization**: the transition from the first term ($a_1$) to the second ($a_2$) occurs without any intermediate positions (there is no "position $1.5$" in a line).

### Why is the Codomain Continuous ($\mathbb{R}$)?

While the position index must be a counting integer, the value of the term itself can be any number on the real plane: integers, fractions, repeating decimals, or irrational numbers such as $\pi$ and $\sqrt{2}$.

## Forms of Sequence Representation

A sequence can be constructed through different explicit rules or formation laws:

### By Explicit Formula

The value of the term is calculated directly as a function of its position $n$:

$$a_n = 2n + 1 \implies (3, 5, 7, 9, \dots)$$

### By Recurrence

Each term is defined based on previous terms. For a recurrent sequence to function properly without entering an infinite loop, a **Base Case (Anchor) is mandatory** to define the starting point:

$$a_1 = 2 \quad \text{(Base Case)}$$

$$a_n = a_{n-1} + 4 \quad \text{for } n \ge 2 \implies (2, 6, 10, 14, \dots)$$

Without the prior definition of $a_1$, the formula cannot calculate any numerical term.

### By Descriptive Property

The terms follow a logical pattern or rule without necessarily having a direct algebraic formula:

$$\text{Sequence of Prime Numbers} \implies (2, 3, 5, 7, 11, \dots)$$

## Initial Indexing: Mathematical Convention vs. Computing

Using $\mathbb{N}^*$ (starting at $n = 1$) is the standard in classical academic mathematics due to its direct alignment with ordinal numbers in human language (first term $a_1$, second term $a_2$).

However, the choice of the initial element is flexible and varies depending on the context:

- **Systems and Programming:** In programming languages and data structures (such as arrays), indexing starts at $0$. This occurs because the index represents a **memory offset** from the pointer's base address, rather than the ordinal position of the element.
    
- **Financial Applications and Physics:** In problems involving compound interest or temporal physics, it is common to define the initial term at $n = 0$ ($a_0$) to represent the state of the system at the initial time ($t = 0$), prior to any period of variation.
    

## Mathematical Recurrence and the Execution Stack (Call Stack)

The definition by recurrence in mathematics serves as the direct conceptual foundation for **recursion** in computer science. The mathematically defined **Base Case** acts as the **stop condition** in code.

### The Connection to Memory and Stack Overflow

At the software execution level, resolving a recursive sequence uses the **Stack** data structure operating on a LIFO (_Last In, First Out_) model:

- **Pushing Phase (Unwinding Down):** To compute $a_4$, the system looks for $a_3$, which looks for $a_2$, which looks for $a_1$. Each pending call is pushed onto the stack memory (_Call Stack_).
    
- **Popping Phase (Resolving Up):** Upon reaching the base case ($a_1$), values are resolved from top to bottom on the stack and returned.
    

If the anchor ($a_1$) is omitted, the stack consumes all allocated memory attempting to resolve previous instances indefinitely, resulting in the memory overflow known as a **_Stack Overflow_**.

## The Limitation in Complex Numbers ($\mathbb{C}$)

Although the default codomain is $\mathbb{R}$, one might question expanding sequences to the set of Complex Numbers ($\mathbb{C}$).

The most critical property preserved in the set of Reais ($\mathbb{R}$) that is lost in Complex Numbers ($\mathbb{C}$) is the **order relation**.

- In $\mathbb{R}$, the set is ordered. It is possible to categorically state the order between two terms ($a_{n+1} > a_n$). This allows defining concepts such as **increasing**, **decreasing**, **monotonic**, and **bounded** sequences.
    
- In $\mathbb{C}$, there is no natural order relation ($i > 0$ or $i < 0$ leads to algebraic contradictions).
    

Without the ability to order terms, concepts of growth, monotonicity, and certain types of boundedness that anchor real sequence analysis cease to exist in the traditional sense.