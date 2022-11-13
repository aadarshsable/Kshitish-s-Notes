Let $(G,*)$ be a group. A subgroup of $G$ is a subset $H \subseteq G$ such that $*$ gives a binary operation on $H$, which gives $H$ the structure of a group.
More precisely, we say that the subset $H$ is a subgroup if the following are true:
1. $1_{G}$ is in $H$.
2. $x,y$ in $H \implies x*y$ in $H$.
3. $x$ in $H \implies x ^{-1}$ in $H$. 
Note that we do not need to check that the binary operation on $H$ is associative as $*$ is known to be associative.

## Examples

1. Let $A$ be a subset of the plane. Then, if $G$ is the group of all isometries of $A$, $G$ is a subgroup of $Perm(A)$
2. Let $G$ be any group. Then $G$ is a subgroup of itself. Any subgroup of $G$ that is not equal to the whole of $G$ is called a proper subgroup of $G$.
3. Let $G$ be a group and let $x$ be any element of $G$. Then, the set:
	$<x> = \{ x^{n} | \text{ n is an integer} \} = \{ 1_{G},x,x ^{-1},x^{2},x^{-2},\dots \}$
	is a subgroup of $G$.
4. Let $m$ be any integer. We define $mZ$ to be the set of all integer multiples of m. Then $mZ$ is a subgroup of $Z$. Indeed any element $x$ of $mZ$ maybe written as $x=md$ for some integer $d$. So, $-x=m(-d)$ and so $-x$ is also in $mZ$. Let $x$ any $y$ be in $mZ$. There exists integers $d_{1} \text{ and } d_{2}$ such that $x=md_{1}$ and $y=md_{2}$. So $x+y =md_{1}+md_{2} =m(d_{1}+d_{2})$; therefore $x+y \in mZ$.

## A Test for Sub Groups

$Proposition:$ Let $G$ be a group. Let $H$ be a non-empty subset of $G$. Then $H$ is a subgroup of $G$ if and only if for any $x,y$ in $H$. The element of $xy^{-1}$ is in $H$.

### Proof

Suppose $H$ is a subgroup of $G$. Let $x,y$ be in $H$. Then, $y^{-1}$ is in $H$. So $xy^{-1}$ is in $H$. So $xy^{-1}$ is in $H$. Thus the condition in the statement of the proposition holds. Conversely, suppose we know that for any $x,y$ in $H$, the element $xy^{-1}$ is in $H$.

Let $x$ be any element of $H$. (Recall - $H$ is non empty). Thus, $x \circ x ^{-1}=1_{G}$ is in $H$.

#### Inverses
Now, let $x$ be any element of $H$. As $1_{G}$ and $x$ are in $H$, so is $1_{G} \circ x ^{-1} = x ^{-1}$.

#### Products
Let $x,y$ be in $H$. Then $y ^{-1}$ is in $H$. So $x \circ (y ^{-1}) ^{-1} = x \circ y$ is in $H$. Thus $H$ is a subgroup.


[Translational Symmetry](Geometrical Symmetry#Translational Symmetry)
