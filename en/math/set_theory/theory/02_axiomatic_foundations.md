## The Axiomatic Construction of Sets (ZFC)

### Overview

Modern Set Theory does not attempt to reflect physical reality, but rather to establish a rigorous, non-contradictory formal system. The axioms presented are deliberate formal conventions designed to construct all mathematical objects from a single primitive concept: the **Set**.

### Formal Axioms

#### 1. Axiom of the Empty Set

Guarantees the existence of at least one set containing no elements.

- **Formal Definition**
    
    $$\exists x \forall y (y \notin x)$$
    
- **Notation:** Denoted by $\emptyset$ or $\{\}$.
    
- **Property:** The unique set with cardinality equal to zero ($\vert{}\emptyset\vert{} = 0$).
    

#### 2. Axiom of Pairing and Von Neumann Ordinals

Allows the creation of a new set containing exactly two given elements.

- **Formal Definition**
    
    $$\forall a \forall b \exists c \forall x (x \in c \iff (x = a \lor x = b))$$
    
- **Construction of Natural Numbers ($\mathbb{N}$)**
    
    - $0 \equiv \emptyset$
        
    - $1 \equiv \{0\} = \{\emptyset\}$
        
    - $2 \equiv \{0, 1\} = \{\emptyset, \{\emptyset\}\}$
        
    - $3 \equiv \{0, 1, 2\} = \{\emptyset, \{\emptyset\}, \{\emptyset, \{\emptyset\}\}\}$
        
    - $n + 1 \equiv n \cup \{n\}$
        

#### 3. Formal Definition of the Ordered Pair (Kuratowski)

Standard sets are unordered ($\{a, b\} = \{b, a\}$). To formalize order and precedence without introducing new primitive concepts, Kazimierz Kuratowski's definition is used.

- **Formal Definition**
    
    $$(a, b) \equiv \{\{a\}, \{a, b\}\}$$
    
- **Pair Equality Theorem**
    
    $$(a, b) = (c, d) \iff (a = c \land b = d)$$
    
- **Mechanics:** The structural asymmetry allows extracting the first element $a$ (intersection of the elements of $(a,b)$) and the second element $b$.
    

#### 4. Axiom of Foundation (Regularity)

Ensures that the membership relation $\in$ is well-founded, preventing infinite descending chains and self-membership.

- **Formal Definition**
    
    $$\forall x (x \neq \emptyset \implies \exists y (y \in x \land y \cap x = \emptyset))$$
    
- **Theoretical Consequence:** Explicitly forbids $A \in A$. Every set has a finite structural depth ending at the empty set $\emptyset$.
    

#### 5. Axiom of Union

Allows extracting elements from a collection of sets and grouping them into a single level.

- **Formal Definition**
    
    $$\forall A \exists U \forall x (x \in U \iff \exists B (x \in B \land B \in A))$$
    
- **Notation:** $U = \bigcup A$
    
- **Example:** If $A = \{\{1, 2\}, \{3, 4\}\}$, then $\bigcup A = \{1, 2, 3, 4\}$.
    

### Technical Summary

The choice of these axioms serves operational rigor. From these formal definitions, relations, functions, the Cartesian Product $A \times B$, and real arithmetic are derived.