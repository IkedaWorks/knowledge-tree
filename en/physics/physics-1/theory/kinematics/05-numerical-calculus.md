##  Numerical Calculus & SI — ( Precision and Representation Guidelines )

> [!IMPORTANT]
> 
> In engineering, an isolated number is insufficient. The integrity of a project depends on the correct manipulation of **Significant Figures (SF)** and the rigorous application of **International System (SI)** prefixes.

---

###  The Anatomy of Significant Figures ( SF )

In mechanical engineering, precision is standardized to **3 significant figures**.

- **Leading Zeros:** NEVER significant.
    
    - _Example:_ ( $0.002$ ) ( 1 SF ) | ( $0.000431$ ) ( 3 SF ).
        
- **Trailing Zeros ( after the decimal point ):** ALWAYS significant.
    
    - _Example:_ ( $4.00$ ) ( 3 SF ).
        
- **Zeros in the Middle:** ALWAYS significant.
    
    - _Example:_ ( $1.05$ ) ( 3 SF ).
        
- **Trailing Zeros ( in whole numbers ):** Use **Engineering Notation**.
    
    - _Example:_ ( $184,900 \rightarrow 185 \cdot 10^3$ ).
        

---

###  Reference Units in Mechanics ( SI )

- **Length:** Meter ( $\text{m}$ ).
    
- **Time:** Second ( $\text{s}$ ).
    
- **Mass:** Kilogram ( $\text{kg}$ ).
    
- **Force:** Newton ( $\text{N}$ ) $\rightarrow$ ( $1\text{ N} = 1\text{ kg} \cdot \text{m/s}^2$ ).
    

#### The Hierarchy of Prefixes ( Powers of ( $10^3$ ) )

- **Giga ( G ):** ( $10^9$ ) | **Mega ( M ):** ( $10^6$ ) | **Kilo ( k ):** ( $10^3$ )
    
- **Milli ( m ):** ( $10^{-3}$ ) | **Micro ( \mu ):** ( $10^{-6}$ ) | **Nano ( n ):** ( $10^{-9}$ )
    

---

###  Representation Protocol

1. **Final Rounding:** Reduce to **3 SF**. If the 4th digit is ( $\ge 5$ ), round up.
    
2. **Prefix Choice:** Adjust the power of ( $10^3$ ) so the number stays between ( $0.1$ ) and ( $1000$ ).
    
3. **Mass in Denominator:** Force the unit to ( $\text{kg}$ ).
    
    - _Example:_ ( $1\text{ N/(g}\cdot\text{s)}$ ). Since ( $1\text{ g} = 10^{-3}\text{ kg}$ ), the ( $10^{-3}$ ) moves up as ( $10^3$ ).
        
    - **Result:** ( $1\text{ kN/(kg}\cdot\text{s)}$ ).
        

> [!WARNING]
> 
> **NOTE:** In equations, always use ( $\text{kg}$ ). Using grams ( g ) creates serious scale problems.

---

###  Epiphany: The Scale Error

- When saying ( $1\text{ km}^2$ ), you are saying ( $(10^3\text{ m})^2 = 10^6\text{ m}^2$ ). **The exponent affects the prefix.**