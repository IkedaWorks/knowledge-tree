
# Measures of Central Tendency

Imagine you have a massive volume of data. Looking at thousands of rows in a table tells you nothing at first glance. We need a mechanism to reduce this pile of numbers into a **single value** that represents the behavior of the entire group. That is where measures of central tendency come in: they pinpoint the "center of gravity" of your data.

---

## 1. Arithmetic Mean

### The Intuition

Imagine 5 friends go out for dinner and the total bill comes to R$ 250. If we split it perfectly equally, everyone pays R$ 50. 

However, in reality, one person might have ordered just water (R$ 10) while another ordered the most expensive steak (R$ 110). The mean ignores these individual nuances and focuses on an idealized scenario: *"if everyone had the exact same share, how much would it be?"*.

**The weakness:** Because it adds everything together, if a billionaire steps onto a public bus, the "average income" of the passengers spikes into millions of dollars. The mean is easily distorted by extreme values (*outliers*).

### My Intuition

I understand the arithmetic mean as a measure of central tendency that manages to guarantee that the data I measured is close to the true value. Think about it: when you measure something, you have no guarantee that the measured value is close to the real value. Several factors can contribute to this—the environment, the state of the equipment, your mental state, or you could simply be tired and make a mistake, and all of this is normal. 

But to obtain precise measurements, we need to reduce these minor errors, and that is where the idea of the arithmetic mean came from. Knowing that we can make errors in every measurement—whether they are above or below the true value—we measure the exact same quantity multiple times, disregarding the small errors made during those individual readings. Afterward, we sum all these measurements because the sum of the errors committed above the true value and the errors committed below the true value will cancel each other out—if one falls short, the other compensates. Finally, we divide this sum by the quantity of elements you added, because you want to know the value of a single measurement, not the sum of them. Notice that the value you find comes very close to the true value.

Notice that the arithmetic mean works for values whose pattern resembles an Arithmetic Progression (A.P.), where the elements do not exhibit a massive disparity among themselves. If you notice other patterns in the analyzed problem, you probably will not use this type of mean. Furthermore, if you notice high disparity between the terms, you will have to use another statistical tool—the **Standard Deviation**—to show how much this mean deviated from the true value; if you find a very high deviation value, you cannot trust the mean as a whole.

> [!NOTE]
> 
> If you have ever studied arithmetic progressions in your life, you probably used the arithmetic mean to find the middle term between two equidistant points in a sequence. This shows the intimate relationship between A.P. and the arithmetic mean.

### The Formalization

To calculate this idealized value, we sum all elements of the set ( $X_i$ ) and divide by the total number of elements ( $n$  or  $N$ ).

* **Population Mean ($\mu$):** Used when we use all existing data.
$$\mu = \frac{\sum_{i=1}^{N} X_i}{N}$$

* **Sample Mean ($\bar{x}$):** Used when we use only a slice (sample) of the whole.
$$\bar{x} = \frac{\sum_{i=1}^{n} x_i}{n}$$

---

## 2. Weighted Mean

### The Intuition

Imagine you are at university and you have two assessments: a simple homework assignment and a final engineering project that took the whole semester to complete. Would it be fair for both to have the exact same impact on your final grade? Of course not.

The final project has more "weight" — meaning it needs to pull your final grade harder than the homework assignment. The weighted mean is the calculation that respects the importance (weight) that each data point holds in the real scenario.

### The Formalization

We multiply each value ( $x_i$ ) by its respective weight ( $w_i$ ), sum all these products, and divide by the sum of all weights (ensuring the scale returns to normal).

$$\bar{x}_w = \frac{\sum_{i=1}^{n} w_i \cdot x_i}{\sum_{i=1}^{n} w_i}$$

> [!Note] 
> 
> Notice that this equation is identical to the arithmetic mean—it might not look like it, but it is! 
> 
> To understand this, answer this question: *What is multiplication?*
> 
> Multiplication is the successive addition of the same number $n$ times. The weighted mean is an upgraded arithmetic mean, because when you have: *Grade 1: 10, Weight: 30*, you are adding 10 thirty times!!! In the denominator, it is the exact same thing: when you sum the weights, you obtain precisely the total quantity of elements that were added.

---

## 3. Median

### The Intuition

Remember the billionaire on the bus distorting the mean? To solve this, we need a metric focused on **position** rather than the sum.

Imagine lining up everyone on the bus in a single file, ordered strictly from lowest income to highest. The person standing exactly in the **middle of the line** represents the Median. If a billionaire boards, they go straight to the end of the line, but the person in the middle remains a regular passenger. This makes the median robust against outliers.

### The Formalization

To find the central element, we must first sort the data (create an ordered array, or **Rol**). The calculation depends on the dataset size ( $n$ ):

* **If $n$ is Odd:** There is a single element perfectly at the center.
$$\text{Position} = \frac{n + 1}{2}$$

* **If $n$ is Even:** There is no single person at the exact center, but two. We take the arithmetic mean of these two central positions:
* 
$$\text{Median} = \frac{x_{n/2} + x_{(n/2) + 1}}{2}$$

---

## 4. Mode

### The Intuition

This is the most visual and straightforward measure. Think of fashion trends: if you walk outside and see most people wearing a specific style of sneakers, you say those sneakers are "in mode" (trendy). Statistics works the same way. The mode is the value that has the highest peak of repetition — the one that shows up most frequently in your dataset.

### The Formalization

Unlike the others, the mode does not require a complex algebraic equation, but rather an absolute frequency count. A dataset can be:

* **Amodal:** No values repeat (all values appear only once).
* **Unimodal / Bimodal / Multimodal:** Has one, two, or multiple values tied for the highest frequency in the dataset.