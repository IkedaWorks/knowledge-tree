
# Application in Percentage Increases and Decreases

These two mechanisms are widely used in "part-of-a-whole" problems, most commonly associated with money, which represents their primary practical application.

## What is an Increase?

Imagine you work at a technology company and, during a specific month, you performed extraordinarily well. As a reward, you receive an extra amount added to your base salary. This is known as an **increase**.

In other words, an increase is an addition relative to the whole, which we reference as $100\%$, $\frac{100}{100}$, or simply $1$. Ultimately, the final value is modeled as:

$$\text{Final Value} = 100\% + \text{increase} \quad \text{or} \quad 1 + \text{increase rate}$$

### Practical Example:

Suppose your base salary is $\$1000.00$ and you receive a $10\%$ increase. Your final salary will be your baseline whole ($100\%$) plus $10\%$ of that whole (which means $0.1$ of $\$1000.00$).

You can calculate the $10\%$ increase in isolation and then add it to the base:

$$\text{Final Salary} = \text{Initial Salary} + \text{Increase}$$

$$\text{Final Salary} = 1000 + (1000 \cdot 10\%) = 1000 + (1000 \cdot 0.1) = 1000 + 100 = 1100$$

Alternatively, you can be more clever and compute it directly via the **Multiplier Factor**:

- If $\$1000.00$ is your whole ($100\%$ or $1$).
    
- And your increase is $10\%$.
    

This means that relative to your original salary, you now have a total portion of $110\%$ ($100\% + 10\%$) or $1.1$ ($1 + 0.1$). Therefore, you can multiply this factor directly by your baseline whole to find the final salary:

$$\text{Final Salary} = 1000 \cdot 1.1 = 1100$$

You achieve the exact same result with a single operation.

> [!NOTE]
> 
> 💡 **Developer Note:** If you are programming a simulation or financial API, you should always use this second method. By reducing the number of arithmetic operations inside your code, you eliminate redundant computational steps, leading to a faster and more efficient execution.



## What is a Decrease?

Now let us consider the opposite scenario: you did not perform well at the company, acted irresponsibly, and missed your shifts. As a consequence, a portion representing $10\%$ of the $\$1000.00$ you were supposed to receive is deducted. This is called a **decrease (or discount)**—when you lose or subtract a portion from your original whole.

Decreases follow the exact same mathematical logic as increases:

$$\text{Final Salary} = 1000 - (1000 \cdot 10\%) = 1000 - 100 = 900$$

From a much more practical and linear perspective, if the whole was $100\%$ ($1$) and you lost $10\%$ ($0.1$), you effectively retain $90\%$ ($0.9$) of the original value:

$$\text{Final Salary} = 1000 \cdot (100\% - 10\%) = 1000 \cdot 90\% = 1000 \cdot 0.9 = 900$$

## Percentage Variation (The Inverse Path)

There is a concept known as **Percentage Variation** that applies this exact logic in reverse. If you already know both the final value and the initial value, how can you determine the exact percentage of the increase or decrease?

You simply compute the ratio between the two states:

$$\text{Variation Factor} = \frac{\text{Final Value}}{\text{Initial Value}}$$

Analyzing the output is straightforward, using the baseline reference of $1$:

- **If the result is greater than 1 (Increase):** If the ratio yields $1.25$, you subtract $1$ to find the variation of $0.25$, which equals a $25\%$ increase.
    
- **If the result is less than 1 (Decrease):** If the ratio yields $0.80$, you calculate how much it deviates from $1$ ($1 - 0.80 = 0.20$), indicating a $20\%$ decrease.