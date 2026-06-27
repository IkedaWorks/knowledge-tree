
# Understanding Vector Decomposition

Have you ever stopped to reflect on how the parallelogram and polygon laws are extremely useful for solving problems involving only a few forces?

The issue arises when the number of forces in the system increases; these geometric methods begin to create a spiderweb of drawings that makes analysis absurdly difficult. This is exactly why we need a method to resolve this impasse: **decomposition**.

To grasp the physics behind this concept, imagine pulling a rolling suitcase at the airport using an inclined handle. You are applying a single diagonal force.

If we observe the practical effect of this force in the real world, we notice two things happening simultaneously: the suitcase moves forward horizontally, and at the same time, it feels a bit lighter, almost lifting off the ground vertically.

This means your diagonal force, on its own, is playing two roles at once. Decomposing a force is simply the process of translating this diagonal force into two separate, imaginary forces—one purely horizontal and another purely vertical—which, together, cause the exact same practical effect.

To discover the exact magnitude of these partial forces, we need to look at the hidden geometry that emerges when we sketch these effects onto the Cartesian plane. If we project the tip of the original force vector onto both the horizontal and vertical axes, we enclose a perfect geometric shape.

![first example of vector decomposition](../../../../assets/fis1-decomposicao-2d.svg)

If you look closely at this drawing, you will see a right triangle where the actual force is the hypotenuse, and the effects we want to discover are the legs (catheti). Our ancestors realized that the ratio between the sides of a right triangle never changes if the angle remains the same. They assigned names to these fixed proportions.

Cosine is simply the ratio between the shadow adjacent to the angle (adjacent leg) and the total length of the hypotenuse:

$$\cos(\theta) = \frac{F_x}{F}$$

By isolating the component we want to find using basic algebra, we arrive at the equation:

$$F_x = F \cdot \cos(\theta)$$

The same reasoning applies to the vertical component. Sine is the ratio between the shadow that is opposite to the angle and the hypotenuse:

$$\operatorname{sen}(\theta) = \frac{F_y}{F}$$

Isolating the vertical component, we obtain:

$$F_y = F \cdot \operatorname{sen}(\theta)$$

Notice that the formula is not a physical dogma or a magical property of mechanics, but rather the direct consequence of stretching or shrinking the proportions of a right triangle.

This is why memorizing that the horizontal axis always takes the cosine and the vertical axis always takes the sine is a mistake that usually costs students dearly on exams. The cosine is strictly tied to the adjacent leg—meaning the one attached to the angle. If the scenario changes and the problem provides the angle measured from the vertical axis, that entire memorized rule collapses.

![second example of vector decomposition](../../../../assets/fis1-decomposicao-2d-invertida.svg)

Looking at the geometry of this new scenario, we notice that the component attached to the angle is now the vertical one. Therefore, the cosine relationship belongs to it:

$$F_y = F \cdot \cos(\phi)$$

On the other hand, the horizontal component has become the opposite leg, away from the angle, which causes it to receive the sine relationship:

$$F_x = F \cdot \operatorname{sen}(\phi)$$

As you can see, the resultant component on the horizontal axis came from a sine projection, not a cosine. If we understand the triangle behind the phenomenon, we can set up the correct equation for any situation, regardless of where the book's author decided to place the angle.

It remains to be seen how to record these calculated forces in a way that any person or computer can understand without needing to see our drawing. To avoid lengthy written descriptions, physics adopted two standard, small guide arrows that are exactly one unit in length: the unit vectors $\vec{i}$ and $\vec{j}$, which point in the positive horizontal and vertical directions, respectively.

A crucial piece of geometric caution is warranted here: these unit vectors are fixed and, by definition, have a magnitude equal to one. When we write the Cartesian components of a force in the form:

$$\vec{F} = F_x\vec{i} + F_y\vec{j}$$

We are not altering the size of these unit vectors. What we are actually doing is creating **equipollent vectors in the plane**. This means that the terms $F_x\vec{i}$ and $F_y\vec{j}$ are new vectors that possess the same direction, sense, and intensity as the projections of our force, regardless of where it is applied on the rigid body. They do not need to originate at the Cartesian center; they carry free vector information through space.

This notation eliminates any ambiguity from the problem. If the scalar value multiplying the horizontal unit vector is negative, we instantly know that the component acts to the left. If the vertical component is positive, it acts upward. We thus trade the complexity of a diagonal line for the predictability of two well-defined orthogonal directions, represented by a pair of perfectly transportable vectors.