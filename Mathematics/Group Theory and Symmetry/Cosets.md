Let $H$ be a subgroup of $G$. If $g$ is any element of $G$, the set:
$gH= \{gh | h \in H \}$ is called a *left coset* of $H$.
Similarly, the set:
$Hg = \{ hg | h \in H \}$ is called a *right coset* of $H$.

Let $G$ be a group and let $H$ be a subgroup. Then, given two left cosets $g_{1}H$ and $g_{2}H$ of $H$, either $g_{1}H \cap g_{2}H=\phi$ or $g_{1}H=g_{2}H$.

The set of all left cosets of $H$ is denoted by $G/H$. Therefore $G / H = \{ H,aH,bH,cH,\dots \}$. Similarly the set of all right cosets of $H$ is denoted by $H \textbackslash G$. Therefore: $H\textbackslash G= \{ H,aH,bH,cH, \dots \}$
One can observe that the union of all cosets of $H$ is $G$.


## Properties

1. The union of all left cosets of $H$ is $G$.
2. Two distinct left cosets do not intersect.

So, the left cosets of $H$ give a partition of $G$.

## Cardinality

We saw earlier that there is a $1-1$ correspondence from $H$ to $gH$ for any $g \in G$. So if $H$ is infinite, we can see that $|gH| =|H|$ for any $g \in G$.

$Theorem:$ Let $G$ be a finite group and let $H$ be a subgroup of $G$. Then $|H|$ divides $|G|$
$Proof:$ As $G$ is a set of a finite set, the set $G/H$ is also finite.
$G$ is the union of all the left cosets of $H$. Any two distinct cosets are disjoint. For any coset $gH$, we have $|gH|=|H|$.

So $|G|=|G/H|.|H|$ 
So $|H|$ divides $|G|$.

$Corollary:$ Let $G$ be a finite group. Then, for any $x \in G$, $ord(x)$ divides $|G|$.
$Proof:$ Apply the theorem with $H= <x>$.