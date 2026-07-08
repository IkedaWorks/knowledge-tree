
# Capitalization Regimes: Simple and Compound Interest

The concept of interest corresponds, in simple terms, to a "rent" charged on capital that has been entrusted to someone. Since this money is not with its rightful owner, it cannot be deployed in other ways (opportunity cost).

In other words, interest represents the yield obtained when lending monetary value or making investments (where the money returns increased by a portion). Conversely, in scenarios like credit card usage or bank loans, interest compensates the institution for advancing capital that it could otherwise use for different purposes.

---

## Simple Interest

This is the most basic capitalization regime. The increase always occurs relative to the **initial value (capital)**. Regardless of the yield accumulated over the months, the interest rate will be calculated strictly based on the baseline of the first month.

### Deduction and Mathematical Pattern

Suppose an initial capital of  $1000.00$  is invested at a simple interest rate of 2.5% per month ($i = 0.025$ ). The behavior of the balance evolution can be mapped cycle by cycle:

* **Month 1:** $1000 + 1000 \cdot 0.025 = 1025$
* **Month 2:** $1025 + 1000 \cdot 0.025 = 1050$
* **Month 3:** $1050 + 1000 \cdot 0.025 = 1075$

It is clear that the portion of interest added each month is constant ($1000 \cdot 0.025 = 25$). Generalizing this pattern for any given time $n$, we define the variables:
* **Amount ($M$):** The total value returned after the application period.
* **Capital ($C$):** The monetary value initially invested.
* **Interest Rate ($i$):** The percentage rate applied per cycle.
* **Time ($n$):** The number of accumulated periods.

Thus, the general equation for the final amount under simple interest is modeled by:

$$M = C \cdot ( 1 + i \cdot n )$$

Through algebraic distribution, the equation can be remodeled as:

$$M = C + C \cdot i \cdot n$$

This second form clearly shows that the final amount depends directly on the initial capital plus the amount of fixed profits earned at each cycle of time.

---

## Compound Interest

This capitalization regime is considerably more aggressive and models most operations in the real financial market (such as financing, long-term investments, and credit card debt).

Unlike the simple regime, the increase is applied directly to the **updated value from the previous period**, rather than the initial capital.

### The "Motor" of Sequential Multiplication
Using the same example of $1000.00 under a 2.5% monthly rate, but now in the compound regime, the individual variation factor for each month is $1 + 0.025 = 1.025$. The evolution behaves as follows:

* **Month 0 (Start):** $1000$
* **Month 1:** $1000 \cdot 1.025 = 1025$
* **Month 2:** $1025 \cdot 1.025 = 1050.625$
* **Month 3:** $1050.625 \cdot 1.025 = 1076.89$

Substituting the variables analytically reveals the compounding chain effect:

* **Month 1:** $$M_1 = C \cdot 1.025$$

* **Month 2:** The "new whole" becomes $M_1$. Applying the factor to it yields:
$$M_2 = M_1 \cdot 1.025 \implies ( C \cdot 1.025 ) \cdot 1.025 = C \cdot ( 1.025 )^2$$

* **Month 3:** The "new whole" is now $M_2$:
$$M_3 = M_2 \cdot 1.025 \implies ( C \cdot ( 1.025 )^2 ) \cdot 1.025 = C \cdot ( 1.025 )^3$$

Repeated multiplication by the factor $( 1 + i )$ ensures that the value accumulated up to that point is preserved (guaranteed by the number 1) and calculates the new interest on top of the already inflated base.

---

## The Connection to Geometry (AP vs GP)

The growth mechanics of both regimes can be mapped directly within the mathematical progressions studied in algebra:

* **Simple Interest as an Arithmetic Progression (AP):** Since the interest reason is fixedly added to the initial capital each cycle, the growth is linear. The equation simulates the general term of an AP.
* **Compound Interest as a Geometric Progression (GP):** Since the reason (variation factor) is sequentially multiplied by the amount of the previous period, the growth is exponential.

The classic compound interest equation:

$$M = C \cdot ( 1 + i )^t$$

Is simply the direct application of the general term of an exponential GP, where each new financial tier is constructed based on the accumulated structure of the immediately preceding period.
