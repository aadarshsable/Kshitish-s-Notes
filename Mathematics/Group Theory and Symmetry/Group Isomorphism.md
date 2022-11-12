Let $(G,*)$ and $(H,\circ)$ be two groups. A group isomorphism from $(G,*) \to (h,\circ)$ is a $1-1$ correspondence $\phi:G \to H$ such that:
$\phi(x*y) = \phi(x) \circ \phi(y)$ for all $x,y$ in $G$.

We say that two groups are isomorphic if there exists a group isomorphism from one to other.

### Example

Let $R^{+}$ denote the set of positive real numbers. $R^{+}$ is a group under binary operation of multiplication.

We can denote this group by $(R^{+},.)$. Fix some real number $a>1$. Consider the function, $\phi: R \to R^{+}$ given by$\phi(x) = a^{x}$. it can be shown that $\phi$ is a $1-1$ correspondence.
$\phi(x+y) =a^{x+y} = a^{x}.a^{y}=\phi(x).\phi(y)$

Thus, $\phi$ is a group isomorphism. So $(R,.)$ is isomorphic to $(R,+)$.

## Isomorphisms preserve Identity and Inverses

$Theorem:$ Let $G$ and $H$ be groups. Let $\phi: G \to H$ be an isomorphism. Then:
1. $\phi(1_{G}) = 1_{H}$
2. For any $x \in G \text{, } \phi(x ^{-1})=\phi(x)^{-1}$

##### Proof

$\phi(1_{G}) =\phi(1_{G}.1_{G}) =\phi(1_{G}).\phi(1_{G})$
So by cancelling $\phi(1_{G})$ from both sides, we get $\phi(1_{G}) =1_{H}$. This proves (1)

Then $\phi(x.x ^{-1} = \phi(x).\phi(x^{-1})$.
But, $\phi(x.x ^{-1})=\phi(1_{G})=1_{H}$
So $\phi(x).\phi(x ^{-1}) =1_{H}$
So, $\phi(x ^{-1})=\phi(x)^{-1}$

##### Example

$G =$ Group of rottational symmetries of a regular hexagon.
$H =$ Group of isometries of an equilateral triangle.

$G \text{ and } H$ are not isomorphic. There are 2 ways of seeing this:

$G$ contains the rotation $\rho$ through $\frac{2\pi}{6}$ radians.
Then $\rho^{6}=1_{G}$. Also, $\rho^{2}$ and $\rho^{3}$ are not equal to $1_{G}$. There are no  such elements in $H$. Indeed if $x$ is any element of $H$, either $x^{2} =1_{H} \text{ or } x^{3}=1_{H}$.
If $\phi: G \to H$ were an isomorphism, $\phi(P)^{2}= \phi(P^{2})$ and $\phi(P)^{3} =\phi(P^{3})$ must both be distinct from $1_{H}$ which is a $Contradiction$.

