Let $n$ be a positive integer. Our goal is:
- Find list of all symmetries
- Calculate composition of symmetries

## Types of Symmetry Example

Let $\Delta ABC$ be an equilateral triangle. It has 3 rotations and 3 reflections possible

### Rotation

There can be three rotations through $0,\frac{2\pi}{3},\frac{4\pi}{3}$ radians.
Rotation through 0 radians is the identity function or $id_{A}$.
Let rotation through $\frac{2\pi}{3}$ radians be $\rho$. Then the, rotation through $\frac{4\pi}{3}$ radians can be written as, $\rho \circ \rho$ or $\rho^{2}$.

Therefore the set of all possible rotational symmetry is $\set{id_{A},\rho,\rho^{2}}$

### Reflection

In $\Delta ABC$ join all three vertices with the centroid and extend each line till it hits the opposite side. Let the three new lines be: $v,l,r$. Let the reflection of the triangle through each line be represented by $\tau_{line}$. Therefore the set of all possible reflective symmetry is $\{ \tau_{l},\tau_{v},\tau_{r} \}$.

Therefore the set of all possible symmetries is $\{ id_{A}, \rho,\rho^{2},\tau_{l},\tau_{v},\tau_{r} \}$


### Compositions

Rotations: $\set{id_{A},\rho,\rho^{2}}$
Clearly, $\rho \circ \rho^{2} = \rho^{2} \circ \rho = \rho^{3} =id_{A}$ 

Reflections: $\{ \tau_{l},\tau_{v},\tau_{r} \}$
Clearly, $\tau_{l}^{2} = \tau_{v}^{2} = \tau_{r}^{2} =id_{A}$

### Basic Observation

In any n-sided polygon. Label vertices as $P_{0},P_{1}..P_{n-1}$ in anti-clockwise direction.
Let $\sigma$ be some symmetry.

If $\sigma(P_{0}) = P_{i}$, then $\sigma(P_{1}) =P_{i-1}\text{ or } P_{i+1}$

The  convention is:
If $i=0$, $P_{i-1}$ is understood as $P_{n-1}$.
If $i=n-1$, $P_{i+1}$ is understood as $P_{0}$
In general $P_{i}$ may also be called $P_{n+i} \text{ or } P_{i-n}$

1. Case I:
	If $\sigma(P_{1}) = P_{i+1}$ then $\sigma(P_{j}) = P_{i+j}$. Therefore, $\sigma = \text{rotation through } (\frac{2\pi i}{n})$
	In general, rotation preserves orientation, i.e. anticlockwise order of labels remains anticlockwise after rotation.

2. Case II:
	If $\sigma(P_{1}) = P_{i-1}$ then $\sigma(P_{j}) = P_{i-j}$. Now the labels run clockwise, therefore $\sigma$ can not be a rotation.
	.
	Let $l_{i}$ be the line segment joining midpoints of $P_{0}P_{i} \text{ and } P_{1}P_{i-1}$.
	If $P_{0}=P_{i}$, take the first midpoint to be $P_{0}$. SImilarly if $P_{1} = P_{i-1}$, take the second midpoint to be $P_{1}$. 
	.
	As such now its easy to see that the reflection in $l_{i}$ is a symmetry of the n-gon taking $P_{0} \to P_{1}, P_{1} \to P_{i-1} \text{ and in general, } P_{j} \to P_{i-j}$
	Thus $\sigma$ is a reflection in line $l_{i}$

### $2n$ symmetries

A regular n-sided polygon always has $2n$ number of symmetries.

This is because a symmetry can take $P_{0} \to P_{i}$.
If it takes $P_{1} \to P_{i+1}$, it is a rotation through $\frac{2 \pi i}{n}$ angle in anticlockwise direction.
If it takes $P_{1} \to P_{i-1}$, it must be a reflection in the line $l_{i}$ defined earlier.

Therfore there are $2n$ symmetries, $n$ rotations and $n$ reflections.

### Composition Calculations

Let $\rho = \text{ rotation through } \frac{2 \pi}{n}$, then $\rho^{i} = \text{ rotation through } \frac{2 \pi i}{n}$. So the set of possible rotations with $n$ elements is, $\{ id_{A},\rho,\rho^{2},\rho^{3}..\rho^{n-1} \}$

Let $\tau$  = reflection in $l_{0}$ ;where $l_{0}$ is the line joining $P_{0}$ to the midpoint of $P_{0}P_{n-1}$

#### Example case: $\rho^{i}\tau$

$\tau$ takes $P_{j} \to P_{n-j}$ for each $j$ and $\rho^{i}$ takes $P_{r} \to P_{r+i}$ for each $r$. So, $p^{i}\tau$ takes $P_{j} \to P_{(n-j) +i}$ for each $j$.
So, it takes $P_{0} \to P_{n-0+i} = P_{n+i} = P_{i}$,
$P_{1} \to P_{n-1+i} = P_{i-1}$, etc..

So, we see that $\rho^{i}\tau$ is the reflection in the line $l_{i}$. So, the $n$ reflections are $\{ \tau, \rho \tau,\rho^{2}\mathbf{\tau}\dots \rho^{n-1}\tau \}$.
Therefore all symmetries include:
$\{ id_{A}, \rho, \rho^{2}, \rho^{3},\dots,\rho^{n-1},\tau,\rho \tau,\rho^{2}\tau,\rho^{3}\tau\dots,\rho^{n-1}\tau \}$

#### Example case: $\tau \rho^{i}$

$p^{i}$ takes $P_{0} \to P_{i}$, $\tau$ takes $P_{i} \to P_{n-1}$
So $\tau \rho^{i}$ takes $P_{0} \to P_{n-i}$ so $\tau \rho^{i}$ is a reflection taking $P_{0} \to P_{n-1}$.
Therefore, $\tau \rho^{i} = \rho^{n-1}\tau$.
Since, $\rho^{n-i} . \rho^{i} = \rho^{n} = id_{A}$. So, $\rho^{n-1}$ = inverse of $\rho^{i}$. So, we will write $\rho^{-i}$ instead of $\rho^{n-i}$. So we have the rule $\tau \rho^{i} = \rho^{-i}\tau$

#### Composition Calculation Example:

$\rho \tau^{2} \circ \rho^{3}\tau$ = $\rho^{2}(\tau \rho^{3})\tau$ = $\rho^{2}(\rho^{-3}\tau)\tau$
= $(\rho^{2}\rho^{-3})(\tau \tau)$ = $\rho^{-1}$ = $\rho^{n-1}$
