
# Sequential Increases and Decreases

This topic is subtle and often misleads many. Intuitively, one might think: _"If a product's price increases by $20\%$ and then decreases by $20\%$, it returns to its original value"_.

However, financial mathematics demonstrates that **applying sequential increases or decreases using the exact same percentage never returns the value to its starting point**.

## The Calculus Book Paradox

To comprehend the mechanics behind this behavior, let us analyze a practical scenario: a calculus book costing $\$100.00$ undergoes a $10\%$ increase, immediately followed by a $10\%$ decrease.

### Step 1: The Increase

Applying the compounding multiplier factor for growth ($1 + 0.1 = 1.1$):

$$\text{Price After Increase} = 100 \cdot 1.1 = 110$$

### Step 2: The Decrease

This is where the most common conceptual error occurs. The $10\%$ decrease will not be applied to the original $\$100.00$ , but rather to the new market value. **The baseline reference has shifted; the new "100%" is now $\$110.00$.**

Applying the decay multiplier factor ($1 - 0.1 = 0.9$):

$$\text{Final Price} = 110 \cdot 0.9 = 99$$

### Analysis of the Outcome

The final price obtained is $\$99.00$, failing to return to the initial $\$100.00$. Utilizing the percentage variation equation to analyze the scenario from a global perspective yields:

$$\text{Variation Factor} = \frac{\text{Final Value}}{\text{Initial Value}} = \frac{99}{100} = 0.99$$

Since $0.99$ represents $99\%$ of the original value, it proves that the net effect of a $10\%$ increase followed by a $10\%$ decrease is, in reality, a **net $1\%$ decrease** ($1 - 0.99 = 0.01$).

> ⚠️ **Cumulative Law:** Whenever percentages are applied sequentially to the same quantity, the effects compound because the calculation baseline is dynamic:
> 
> - Sequential increases accumulate **more** than the simple arithmetic sum of the rates.
>     
> - Sequential decreases reduce **less** than the simple arithmetic sum of the rates.
>     

## Algorithmic Generalization (The Product of Factors)

Computationally, to calculate the impact of $n$ sequential variations, one discards the use of cross-multiplication or complex, repetitive code loops. The behavior is modeled linearly by the product of the variation factors ($f_1, f_2, \dots, f_n$):

$$\text{Final Value} = \text{Initial Value} \cdot (f_1 \cdot f_2 \cdots f_n)$$

In the case of the calculus book example:

$$\text{Final Value} = 100 \cdot (1.1 \cdot 0.9) = 100 \cdot 0.99 = 99$$

## Reverse Engineering: How to return to the original value?

To force a value to return exactly to its original equilibrium point after a percentage change, it is necessary to calculate the **compensation rate** using the multiplicative inverse of the current factor.

If an asset undergoes a change and is now valued by a factor $f$, to return it to the original baseline of equilibrium ($1$), it must be multiplied by its inverse: $\frac{1}{f}$.

### Application Example:

A calculus book priced at $\$100.00$ undergoes a $25\%$ increase ($f = 1,25$), now costing $\$125.00$. What exact discount rate must be applied to the new price to bring it back to the original $\$100.00$?

1. Find the return factor:
    
    $$\text{Return Factor} = \frac{1}{1.25} = 0.80$$
    
2. Analyze the resulting factor:
    
    Since $0.80$ is less than $1$, a decrease (discount) is required. The exact discount rate will be the difference needed to reach unity:
    
    $$\text{Discount} = 1 - 0.80 = 0.20 \implies 20\%$$
    

> 🎯 **Conclusion:** To nullify a $25\%$ increase, one does not apply a $25\%$ discount, but rather an exact discount of $20\%$. Structured percentage variation ensures mathematical control and predictability over dynamic pricing pipelines.