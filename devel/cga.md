# Intuitive Reference for Conformal Geometric Algebra (G₄,₁)

## Foreword: A Language, Not a Toolbox

This document presents Conformal Geometric Algebra (CGA) in its 5D, $\mathbb{R}^{4,1}$ Minkowski spacetime, not as a mere collection of mathematical tools, but as a complete, interconnected, and intuitive **language for geometry**. Its power lies in fundamentally changing one's approach to geometric problems, moving from searching for the right formula to directly stating geometric intent as elegant algebraic expressions.

In this language:

- Its **nouns** are the multivectors (blades) that represent geometric entities.
- Its **verbs** are the operators (versors) that represent transformations.
- Its **grammar** is the **geometric product**, which dictates how nouns and verbs interact to form complete, meaningful geometric sentences.

Our journey through this algebra aims for a deep, intuitive saturation, revealing how seemingly disparate concepts in mathematics, physics, and computer science find a unified expression within this single, coherent framework.

## The Foundation - A 5D Relativistic Spacetime

### Why 5D? The Cost of Unification

In standard 3D geometry, rotation and translation are fundamentally different operations requiring different mathematical tools (matrices for rotation, vector addition for translation). CGA's first brilliant move is to embed our familiar 3D space into a 5D space with metric signature (4,1). This is the "price of admission" we pay in exchange for the unification of all geometric operations.

To achieve this unification, we extend our familiar 3D space by adding two special dimensions that encode the concepts of 'origin' and 'infinity.' These aren't spatial dimensions in the usual sense, but rather mathematical constructs that allow us to treat all transformations uniformly. Here's how this works mathematically.

### The Critical Ingredient: The Minkowski Metric

The real magic of the 5D space lies not in its dimension, but in its **metric**—the rule for how distances and angles are measured. Instead of a standard Euclidean metric where every basis vector squares to 1, CGA uses a Minkowski metric.

The Euclidean basis vectors ($e_1, e_2, e_3$) all square to 1:

$$e_i^2 = 1 \quad \text{and} \quad e_i \cdot e_j = \delta_{ij}$$

The two extra basis vectors represent the origin ($n_0$) and infinity ($n_\infty$). They are **null vectors**, meaning they square to zero:

$$n_0^2 = 0 \quad \text{and} \quad n_\infty^2 = 0$$

The single most important property that establishes the (4,1) Minkowski metric signature is their inner product:
$$n_0 \cdot n_\infty = -1$$

This single, non-Euclidean rule introduces a relativistic structure to the space, analogous to the spacetime of Einstein's theories. It has three consequences:

1. **Translation as Rotation:** It enables translation to be treated as a rotation in a higher-dimensional plane involving $n_0$ and $n_\infty$. This unifies all Euclidean isometries within a single algebraic framework.

2. **Light Cone Analogy:** The set of all points forms a **null cone** ($X^2 = 0$), mathematically identical to the light cone in Special Relativity. This is not merely an analogy but a formal identity, implying a deep geometric basis for causality.

3. **Pseudoscalar Property:** The **pseudoscalar** of the space, $I = e_1 e_2 e_3 n_0 n_\infty$, squares to $I^2 = -1$. This property governs the nature of duality in the algebra. (The pseudoscalar $I$ represents the oriented 5D volume element of the space—a concept we'll explore in detail later).

### The Fundamental "Atom": The Point on the Null Cone

A 3D Euclidean vector $p = xe_1 + ye_2 + ze_3$ is "lifted" or embedded into a 5D CGA vector $P$ on the null cone via the formula:

$$P = p + \frac{1}{2}p^2 n_\infty + n_0$$

This formula looks complex, but its result is simple. The defining algebraic property of any such point $P$ in CGA is that it squares to zero:

$$P^2 = 0$$

This means all points are **null vectors**, and therefore they are **not invertible** in the algebra—you cannot divide by a point.

> **Visualizing the Null Cone**
>
> While we can't truly visualize 5D, we can use an analogy. Imagine the null cone as the 5D analog of a light cone in spacetime. Just as light rays trace out a cone in 4D spacetime, all 3D Euclidean points, when lifted into CGA, trace out a 4D cone-like surface in the 5D space. This "cone" is defined by the simple condition $X^2 = 0$.

**Algebraic Verification of $P^2=0$:**

Let's expand $P^2 = P \cdot P$ using the properties $p \cdot n_0 = 0$, $p \cdot n_\infty = 0$, $n_0^2=0$, $n_\infty^2=0$, and $n_0 \cdot n_\infty = -1$:

$$P^2 = \left(p + \frac{1}{2}p^2 n_\infty + n_0\right)^2$$

$$P^2 = p^2 + \left(\frac{1}{2}p^2\right)^2 n_\infty^2 + n_0^2 + 2\left(\frac{1}{2}p^2\right)(p \cdot n_\infty) + 2(p \cdot n_0) + 2\left(\frac{1}{2}p^2\right) (n_\infty \cdot n_0)$$

Substituting the basis vector properties:

$$P^2 = p^2 + 0 + 0 + 0 + 0 + p^2 (n_\infty \cdot n_0)$$

Since $n_\infty \cdot n_0 = -1$:

$$P^2 = p^2 + p^2(-1) = p^2 - p^2 = 0$$

This demonstrates how each term meticulously contributes to ensuring the point correctly lies on the null cone. The $n_0$ term is critical as a "bias" or "gauge" component that correctly positions the Euclidean space onto the null cone and ensures this fundamental null property holds for all points $p$.

> **Point of Common Confusion: The Nature of Infinity ($n_\infty$)**
>
> A frequent source of confusion is viewing $n_\infty$ as merely an abstract concept. In CGA, $n_\infty$ is a **basis vector** that explicitly represents the *concept* of infinity. This allows for a **structured subspace at infinity**, meaning that operations involving parallel objects yield well-defined geometric results at infinity, unlike in traditional Euclidean geometry where such cases might be undefined. This is crucial for achieving full geometric closure and robustness.

## The Grammar - One Product to Rule Them All

All geometric relationships and operations in CGA are described by one fundamental product and its constituent parts.

### The Full Story: The Geometric Product

The **geometric product** ($AB$) is the fundamental grammar of CGA. It encapsulates the complete relationship between any two multivectors $A$ and $B$—their angle, distance, and transformation potential. It is the single source from which all other products are derived, unifying both the "measurement" and "construction" aspects of geometric interaction.

### The Core Identity

For any two vectors, the geometric product decomposes into symmetric and anti-symmetric parts:

$$AB = A \cdot B + A \wedge B$$

- $A \cdot B = \frac{1}{2}(AB + BA)$ (the symmetric **inner product**)
- $A \wedge B = \frac{1}{2}(AB - BA)$ (the anti-symmetric **outer product**)

### The "Construction" Tool: The Outer Product (∧)

The **outer product** is for **construction**. It creates the smallest geometric object that contains both $A$ and $B$. It is fundamentally **grade-raising**: for linearly independent inputs, the grade of the result is the sum of the input grades. If the inputs are linearly dependent (e.g., two parallel lines), the outer product is zero, signifying they don't span a higher-dimensional object.

**Examples:**

- $P_1 \wedge P_2$: The object containing two points (a point pair).
- $P_1 \wedge P_2 \wedge P_3$: The circle passing through three points.
- $P_1 \wedge P_2 \wedge n_\infty$: The line passing through two points.

### The "Measurement" Tool: The Inner Product (·)

The **inner product** is for **measurement**. It reveals "how much" of one object aligns with another. It's used for angles, distances, and testing for perpendicularity. The inner product is fundamentally **grade-lowering**. For two vectors, it results in a scalar measuring their projection.

**Examples:**

- $\pi_1 \cdot \pi_2$: The cosine of the angle between two normalized planes.
- $P \cdot \pi$: A value related to the distance of point $P$ from plane $\pi$.
- $L_1 \cdot L_2$: A measure of the alignment between two lines.

## Substance and Action - The Unity of Objects and Operators

In CGA, there's no hard line between "things" (geometric objects) and "actions" (transformations). **Operators (versors) are literally made of the geometric objects they relate to.**

This distinction is crucial for understanding transformations:

- **Object (e.g., a Plane $\pi$):** A full geometric entity with both **position and orientation**. In CGA, a plane is a **grade-1 vector** ($\pi = n + d n_\infty$). Think of this as a physical **dinner plate**: it has an orientation ("facing up") *and* a location (on the table).
- **Orientation (e.g., a Bivector B):** A pure orientation, like "facing north." In CGA, this is typically a **grade-2 bivector** ($B = e_1 \wedge e_2$). It has no position and is the *generator* of rotations (i.e., it defines the plane of rotation).

A plane object **has** an orientation, but it **is not** its orientation. A **translation** on a plane object will change its position (its $d$ term) but will **not** change its pure orientation bivector.

### The Universal Law of Transformation: The Sandwich Product

All transformations are applied with the universal **sandwich product**:

$$X' = VXV^{-1}$$

Where $V$ is an invertible multivector (a **versor**) representing the transformation, $X$ is the object to be transformed, and $X'$ is the transformed object.

The sandwich structure is essential because every transformation can be viewed as a sequence of reflections. A single reflection flips an object's orientation (handedness). The sandwich product represents two reflections, which performs the transformation while preserving the object's fundamental type and orientation.

> **In Practice: A 90-Degree Rotation**
>
> To perform a 90-degree rotation in the $e_1e_2$ plane, the rotor is $R = e_2e_1$. To rotate the vector $v = e_1$:
>
> $$v' = R v R^{-1} = (e_2e_1)(e_1)(-e_1e_2)$$
>
> $$v' = e_2(e_1e_1)(-e_1e_2) = e_2(1)(-e_1e_2) = -e_2e_1e_2$$
>
> Since basis vectors anticommute, $-e_2e_1e_2 = e_2e_2e_1 = (1)e_1 = e_2$.
>
> The vector $e_1$ is correctly rotated to $e_2$.

### The "Socks and Shoes" Principle

The inverse of a composite transformation is the product of the individual inverses in the **reverse order**: $(AB)^{-1} = B^{-1}A^{-1}$. This elegantly models real-world logic. Think of putting on your socks (A) and then your shoes (B); to undo this, you must first take off your shoes ($B^{-1}$) and then your socks ($A^{-1}$).

### A Table of Transformations

| Transformation | Operator (Versor) V | Construction (The Action is the Substance) |
| :--- | :--- | :--- |
| **Rotation** | Rotor | $\pi_2 \pi_1$ (the geometric product of two intersecting planes) |
| **Translation** | Translator | $S_2 S_1$ (the geometric product of two same-sized spheres) |
| **Screw Motion** | Motor | $L_2 L_1$ (the geometric product of two lines) |
| **Scaling** | Dilator | $S_2 S_1$ (the geometric product of two concentric spheres) |
| **Scaling-Rotation** | Conformal Rotor | $S\pi$ (the geometric product of a sphere and a plane) |

This principle simplifies geometric programming. A rotation isn't an abstract matrix operation; it's the result of successive reflections across specific planes, and the Rotor itself encapsulates the relationship of those planes.

## The Primitives - A Multivector Bestiary

Geometric primitives in CGA are represented as **blades**—multivectors constructed with the **outer product (∧)**. Their **grade** often corresponds to their **codimension** (the number of constraints needed to define them in the ambient 5D space), not their Euclidean dimension.

### Grade, Dimension, and Codimension

The **grade** of a blade (the number of vectors in its outer product construction) often corresponds to its **codimension** (the number of constraints needed to define it in 5D space), not its intuitive Euclidean dimension. This relationship can be subtle.

| Object | Grade | Euclidean Dimension | Codimension in 5D | Grade = Codimension? |
| :--- | :--- | :--- | :--- | :--- |
| Point | 1 | 0 | 4 | No (special case) |
| Plane | 1 | 2 | 1 | Yes |
| Sphere | 1 | 2 | 1 | Yes |
| Line | 2 | 1 | 3 | No |
| Circle | 2 | 1 | 3 | No |

### Grade-1 Primitives (Vectors)

| Primitive | Algebraic Construction | Defining Algebraic Property |
| :--- | :--- | :--- |
| **Point** | $P = p + \frac{1}{2}p^2 n_\infty + n_0$ | $P^2 = 0$ (null vector) |
| **Sphere** | $S = c - \frac{1}{2}r^2 n_\infty$ | $S^2 = r^2 > 0$ (squared radius) |
| **Plane** | $\pi = n + d n_\infty$ | $\pi^2 = n^2 > 0$ (normalized to $\pi^2=1$) |

**Verification of Sphere Property $S^2=r^2$:**

Given a sphere $S = c - \frac{1}{2}r^2 n_\infty$, where $c$ is its CGA center point ($c^2=0$) and normalized such that $c \cdot n_\infty = -1$:

$$S^2 = \left(c - \frac{1}{2}r^2 n_\infty\right)^2 = c^2 - r^2(c \cdot n_\infty) + \frac{1}{4}r^4 n_\infty^2$$

$$S^2 = 0 - r^2(-1) + 0 = r^2$$

### Higher-Grade Primitives

| Primitive | Grade | Algebraic Construction | Defining Algebraic Property |
| :--- | :--- | :--- | :--- |
| **Circle** | 2 | $S_1 \wedge S_2$ or $P_1 \wedge P_2 \wedge P_3$ | $C^2 = r^2 > 0$ (squared radius) |
| **Line** | 2 | $P_1 \wedge P_2 \wedge n_\infty$ | $L^2 = -d^2 \leq 0$ (negative squared distance from origin) |
| **Point Pair** | 2 | $P_1 \wedge P_2$ | $PP^2 > 0$ |

The inclusion of $n_\infty$ in the line construction forces the object to be straight (infinite radius circle).

## Duality - The Algebra's Mirror

**Duality** ($*$), which is multiplication by the inverse of the pseudoscalar ($A^* = AI^{-1}$), is the algebra's capacity for introspection. It allows an object to be defined in two complementary ways.

### Two Ways of Seeing: OPNS vs. IPNS

- **By what it is (Span / OPNS):** **Outer Product Null Space**. This approach builds an object from its constituent elements using the **outer product (∧)**. An object $A$ is defined by the set of all points $X$ such that $X \wedge A = 0$.
    - **Example (OPNS):** A line can be defined as the span of two points and infinity: $L = P_1 \wedge P_2 \wedge n_\infty$. Any point $X$ on the line will make $X \wedge L = 0$.

- **By what it is not (Intersection / IPNS):** **Inner Product Null Space**. This approach carves an object from space by defining the intersection of constraints. An object $A$ is defined by the set of all points $X$ for which $X \cdot A = 0$.
    - **Example (IPNS):** A plane can be defined by its normal vector $n$ and distance $d$ from the origin as $\pi = n + d n_\infty$. A point $X$ is on the plane if $X \cdot \pi = 0$. A line can also be seen as the intersection of two planes, $\pi_1$ and $\pi_2$. Its dual representation would be $L^* = \pi_1 \wedge \pi_2$.

### Deep Dive: Consequences of the Metric and Handedness

Because the pseudoscalar $I$ of $\mathbb{G}_{4,1}$ squares to $I^2 = -1$, duality is an **anti-involution**:

$$(A^*)^* = (AI^{-1})I^{-1} = A(I^{-1})^2 = A(I^2)^{-1} = A(-1)^{-1} = A(-1) = -A$$

Applying the dual operation twice results in the original object with a sign flip, which implies that duality inherently flips the 'handedness' or intrinsic orientation of the object.

### The Covariance of the Dual

The dual of a transformed object is the same as transforming the dual. This **covariance of the dual** is a powerful computational tool:

$$(VAV^{-1})^* = V(A^*)V^{-1}$$

This property means you can choose to transform an object and then dualize the result, or dualize the original object first and then apply the same transformation to its dual. One of CGA's most powerful patterns is performing operations in one space to get results in the other.

Consider finding the intersection of two planes $\pi_1$ and $\pi_2$:
- Planes are naturally IPNS objects (grade-1 vectors)
- Their intersection line is naturally an OPNS object (grade-2 bivector)
- The operation $L = \pi_1 \wedge \pi_2$ uses the OPNS construction tool on IPNS objects

This isn't a contradiction—it's a feature. You're using the construction tool on the *constraints* to find the object that satisfies them both.

## The Engine of Dynamics - The Commutator

The **commutator**, $[A,B] = \frac{1}{2}(AB - BA)$, is the universal algebraic expression for **infinitesimal change** (the Lie derivative). It measures the "gap" or "hinge" between two operations. If the operations are aligned, there is no gap, and the commutator is zero.

### The Engine of Change

Imagine an operation "witnessed" from two sides. $AB$ is the result of applying B then A. $BA$ is the result of applying A then B. If these results are different, there is a "gap" between them. The commutator is the algebraic object that precisely measures this gap, representing the "hinge" or axis of relative motion. If the operations are aligned (e.g., two parallel vectors), there is no gap, and the commutator is zero.

This single concept manifests across numerous fields:

- **Classical Kinematics:** Velocity is $v = [P, B]$. Acceleration is $a = [[P, B], B]$.
- **Quantum Mechanics:** The time evolution of angular momentum $L$ is torque $\tau$, expressed as $\tau = [L, H]$.
- **Geometric Construction:** The commutator $[\pi_1, \pi_2]$ directly constructs the bivector representing the **intersection line** of two planes.

### The Great Divide: Meet, Commutator, and Outer Product

This table clarifies the distinct roles of key operators, especially for parallel objects.

| Scenario | Meet (A∨B) - Geometric Intersection | Commutator ([A,B]) - Rotational Engagement | Outer Product (A∧B) - Span/Join |
| :--- | :--- | :--- | :--- |
| **Two Intersecting Planes** | **Intersection Line** | **Intersection Line** (the 'hinge') | **Intersection Line** |
| **Two Parallel Planes** | **Line at Infinity** | **Zero** (no rotational axis) | **Zero** (linearly dependent) |
| **Two Perpendicular Planes** | **Intersection Line** | **Intersection Line** (non-zero) | **Intersection Line** |
| **Two Intersecting Lines** | **Intersection Point** | **Screw Motion Generator** | **Grade-4 Object** |
| **Two Parallel Lines** | **Point at Infinity** | **Zero** (no rotational engagement) | **Zero** (linearly dependent) |
| **Two Skew Lines** | **Zero** (truly disjoint) | **Screw Motion Generator** (non-zero) | **Grade-4 Object** |

**Key Takeaway:**
- **Meet (∨):** Answers "What is the common geometric element or intersection?" A zero meet means **no intersection at all** (they are disjoint).
- **Commutator ([]):** Answers "What is the infinitesimal transformation/rotation between them?" A zero commutator means **no rotational engagement**.
- **Outer Product (∧):** Answers "What space do they span together?"

### The Transformation Workflow: From Generator to Action

The commutator often serves as the 'blueprint' for transformations. The general workflow is universal in CGA:

**Step 1: Find the Generator.** The "blueprint" for the transformation is often found via the commutator of the two objects: $B = [L_2, L_1]$ for transforming lines, for instance. This $B$ represents the *infinitesimal change* required.

**Step 2: Construct the Operator.** Use the **exponential map** to build the full, finite operator (versor) from the generator blueprint: $M = \exp(B)$.

- **Intuition for Exponential Map:** In Lie theory, the exponential map bridges the gap between a Lie algebra (where elements like $B$ represent infinitesimal transformations or "velocities") and a Lie group (where elements like $M$ represent finite transformations or "trajectories"). It effectively "integrates" the infinitesimal change into a complete transformation.

**Step 3: Apply the Operator.** Transform the object using the universal sandwich product: $L_2 = ML_1M^{-1}$.

**Interpolation:** To interpolate a transformation $M$ by a factor $t \in [0,1]$ along its continuous path, one first recovers the generator using the **logarithm**: $B = \log(M)$. Then, scale the generator by $t$ and re-exponentiate: $M_t = \exp(tB)$.

## The Algebra in Action

CGA's power is best illustrated by its directness in solving geometric problems, allowing us to state geometric intent directly as algebraic expressions.

### Geometric Construction - Intersection Circle of Two Spheres

**Goal:** Find the intersection circle C of two spheres, $S_1$ and $S_2$.

- $S_1$: Centered at origin, radius 2. Algebraically: $S_1 = n_0 - \frac{1}{2}(2^2) n_\infty = n_0 - 2n_\infty$
- $S_2$: Centered at (1,0,0), radius 2. Algebraically: $S_2 = (e_1 + \frac{1}{2}(1^2) n_\infty + n_0) - \frac{1}{2}(2^2) n_\infty = e_1 - \frac{3}{2}n_\infty + n_0$

**Action:** State the geometric intent directly: the intersection is found by the **outer product** (span/join).

$$C = S_1 \wedge S_2 = (n_0 - 2n_\infty) \wedge (e_1 - \frac{3}{2}n_\infty + n_0)$$

**Result:** Expanding this outer product yields a grade-2 bivector $C$ that directly represents the intersection circle.

### Transformation Workflow: Motor from Line $L_1$ to Line $L_2$

**Goal:** Find the motor M that transforms line $L_1$ to line $L_2$.

**Step 1:** Find the Generator. The "blueprint" for the transformation is the commutator of the two lines.
$$B = [L_2, L_1]$$

**Step 2:** Construct the Operator. Use the exponential map to build the motor from the generator blueprint.
$$M = \exp(B)$$

**Step 3:** Apply the Operator. Transform $L_1$ using the sandwich product.
$$L_2 = ML_1M^{-1}$$

This workflow—finding a generator via a product, building an operator with exp, and applying it with the sandwich product—is a universal pattern in CGA, unifying seemingly disparate transformations under a single elegant framework.

## The Great Unification

CGA acts as a unifying language, revealing deep isomorphisms between fields of mathematics and physics.

### Sub-Geometries

Other geometries exist as sub-manifolds within the 5D CGA space. A point $X$ in a given geometry is defined by its algebraic square:

| Geometry | Condition | Physical Analogy |
| :--- | :--- | :--- |
| **Spherical** | $X^2 > 0$ | Space-like separation (causally disconnected) |
| **Euclidean (Conformal)** | $X^2 = 0$ | Light-like separation (causal boundary) |
| **Hyperbolic** | $X^2 < 0$ | Time-like separation (causally connected) |

This means that CGA provides a single algebraic framework to describe and transition between Euclidean, spherical, and hyperbolic geometries.

### Physics

The connection between CGA and physics is not merely an analogy; it is a **formal identity**, implying shared mathematical structures at a fundamental level.

**Special Relativity:** The CGA space $\mathbb{R}^{4,1}$ has the exact same metric signature as the spacetime used to model particle physics (Minkowski spacetime). Crucially, the **null cone of CGA is formally identical to the light cone in Special Relativity**. This implies that the causal structure of spacetime (events connected by light rays or timelike paths) is intrinsically encoded in the algebraic structure of the null cone itself, providing a fundamental geometric foundation for causality. The operators of CGA are a superset of Lorentz transformations.

**Quantum Mechanics:** The algebra of rotors in 3D Euclidean space (Euclidean Geometric Algebra) is **isomorphic** to the group SU(2), which describes quantum spin. Furthermore, the bivector generators of rotation are a direct representation of the Pauli spin matrices. This signifies that seemingly abstract quantum concepts like electron spin might have a deep, intrinsic geometric reality rooted in the structure of spacetime itself, unified within the language of CGA.

### Logic and Computer Science

The algebra of subspaces formed by the meet (∨) and join (∧) operators is formally a **lattice structure**, directly analogous to the logical operators **AND** and **OR** used in computation and set theory.

**Meet (∨):** Analogous to logical **AND** (set intersection), as it finds the common geometric subspace. This provides a robust mechanism for geometric intersection queries.

**Join (∧):** Analogous to logical **OR** (set union/span), as it creates the smallest geometric object that contains all inputs. This provides a powerful tool for geometric construction.

This direct mapping to lattice theory provides a powerful algebraic language for geometric queries, enabling complex geometric relationships (e.g., "point on line AND line in plane") to be expressed and processed elegantly. This reduces the need for extensive conditional logic and case distinctions in geometric algorithms.

## Quick Reference

### Essential Formulas

| Operation | Formula | Result | Notes |
| :--- | :--- | :--- | :--- |
| **3D → CGA Point** | $P = p + \frac{1}{2}p^2n_\infty + n_0$ | Point ($P^2=0$) | Lifts onto null cone |
| **Test Incidence** | $X \wedge A = 0$ | Boolean | Is X part of A? (OPNS) |
| **Point-Plane Distance** | $d = \frac{P \cdot \pi}{-P \cdot n_\infty}$ | Scalar | For normalized P and $\pi$ |
| **Project Point to Plane** | $P_{\text{proj}} = P - (P \cdot \pi)\pi$ | Point | Requires normalized plane $\pi^2=1$ |
| **Reflect Point in Plane** | $P' = \pi P \pi$ | Point | Requires normalized plane $\pi^2=1$ |
| **Extract Sphere Center** | $c = S n_\infty S$ | Point | A specific sandwich-like product |
| **Sphere/Circle Radius** | $r = \sqrt{S^2}$ or $r = \sqrt{C^2}$ | Scalar | Direct from the object's square |
| **Angle Between Planes** | $\theta = \arccos(\pi_1 \cdot \pi_2)$ | Scalar | For normalized planes |
| **Interpolate Motor** | $M_t = \exp(t \cdot \log(M))$ | Motor | Smooth transformation |

**Note on Distance Formula Denominator:** The term $-P \cdot n_\infty$ in the distance formula for point to plane is crucial for proper normalization. For a normalized CGA point $P$, $P \cdot n_\infty = -1$. This denominator ensures the distance calculation is correctly scaled to yield a direct Euclidean distance, effectively "un-conformalizing" the point's representation for a familiar interpretation.

### Construction Patterns

| To Create | Use | Example |
| :--- | :--- | :--- |
| **Line through 2 points** | Outer product with infinity | $L = P_1 \wedge P_2 \wedge n_\infty$ |
| **Circle through 3 points** | Outer product | $C = P_1 \wedge P_2 \wedge P_3$ |
| **Sphere through 4 points** | Dual of outer product | $S = (P_1 \wedge P_2 \wedge P_3 \wedge P_4)^*$ |
| **Plane from point and normal** | Direct construction | $\pi = n + (p \cdot n) n_\infty$ |

### Transformation Generators

| From → To | Generator Construction |
| :--- | :--- |
| **Plane → Plane** | $R = \pi_2\pi_1$ (rotor) |
| **Line → Line** | $B = [L_2, L_1]$ (motor generator) |
| **Point → Point** | $T = 1 - \frac{1}{2}(p_2 - p_1)n_\infty$ (translator) |

**Remember: In CGA, geometric intent becomes algebraic expression. State what you want, not how to calculate it.**
