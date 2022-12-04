A group $G$ is said to be *abelian* or *commutative* if for any $x,y \in G$, we have $xy=yx$
Example: $\mathbb{Z},\mathbb{Z}/m\mathbb{Z}$ are abelian, $D_{n}$ is not abelian for $n \geq 3$.

```ad-note
title: Theorem
icon: infinity
color: 0,255,255

Let $(G,+)$ be an abelian group. Let $S \subseteq G$. Then $<S>$ is equal to the set of all elements of the form: $n_{1}x_{1}+n_{2}x_{2}+n_{3}x_{3}+\dots+n_{r}x_{r}$ where

$x_{1},x_{2},x_{3},\dots \in S$ and

$n_{1},n_{2},n_{3},\dots \in \mathbb{Z}$

```
```ad-note
title: Example
color: 125,255,125

Consider the group $(\mathbb{Z},+)$. Let $a,b \in \mathbb{Z}$. Then,

$<a,b>=\{ am+bn \text{ } | \text{ } m,n \in \mathbb{Z} \}$

But $<a,b>$ is a subgroup of $\mathbb{Z}$. So $<a,b>=<d>$ for some $d\geq 0$.
```

Since $a \in <a,b> = <d> \implies d|a$. Similarly, $d|b$. Let $g=gcd(a,b)$. Then, $d|g$. But $g|a$ and $g|b$ $\implies$ $g|am+bn$ for all $m,n \in Z$.
As $d \in <a,b>$, there exist integers $r,s$ such that $d=ar+bs$. So, $g|ar+bs=d$. So, $d|g$ and $g|d$. As $g\geq0$ and $d\geq0$, we see that $d=g$.

So we have proved that:
Let $a,b \in \mathbb{Z}$. Then there exists integers $r,s$ such that $gcd(a,b)=ar+bs$.