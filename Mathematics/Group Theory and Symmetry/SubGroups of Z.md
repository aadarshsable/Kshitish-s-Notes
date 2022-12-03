We know that if $m$ is any integer, the set
$m\mathbb{Z}=\{ mx | x \in \mathbb{Z} \}$
is a subgroup of $\mathbb{Z}$

## A small generalization

Let $S \subseteq \mathbb{Z}$ be a non empty subset with a lower bound, i.e. there exists some element $x_{0} \in \mathbb{Z}$ such that $x \geq x_{0} \text{ } \forall \text{ } x \in S$. Then $S$ has a smallest element.

```ad-note
title: Proof
color: 0,255,255
icon: infinity
Let $T=\{ x-x_{0}+1 \text{ }| \text{ }x \in S \}$
Then $T$ consists of *positive integers*. Also, $T$ is non-empty. So, $T$ has a smallest element $z$. Then $z=y-x_{0}+1$ for some $y \in S$
```

We claim that $y$ is the smallest element of $S$. If not, suppose there exists some $x \in S, \text{ } x<y$.
Then, $x-x_{0}+1 < y-x_{0}+1 = z$. But $x-x_{0}+1 \in T$ and $z$ is the smallest element of $T$ which is a **contradiction**.

Conclusion: The well ordering principle applies to non-empty subsets of *non-negative* integers as well.

## Division Algorithm

Let $a,b \text{ } \in \mathbb{Z}, \text{ } b>0$. Then, there exists *unique* integers $q,r$ such that $a=bq+r$ and $0 \leq r < b$.

```ad-note
title: Warning
icon: exclamation
color: 255,0,0
Note the conditions on $r$ carefully. We have $0\leq r$ and $r<b$
```

```ad-note
title: Proof
color: 0,255,255
icon: infinity

Consider the set $S=\{ a-bm \text{ }| \text{ }m \in \mathbb{Z}, \text{ } a-bm \geq 0 \}$
We claim that $S$ is non-empty.
```
```ad-note
title: Case 1
color: 255,0,255
Suppose $a\geq 0$.
Then $a=a-b.0 \in S$
```
```ad-note
title: Case 2
color: 255, 255, 0
Suppose $a< 0$
Then $a-b(2a)=a(1-2b)$. As $b \geq1, \text{ } 2b\geq 2$ and so $1-2b <0$. As $a<0, \text{ } a(1-2b)>0$.
So, $a-b(2a) \in S$. Therefore $S$ is non empty in this case too
```

So $S$ has a smallest element, which we can denote by $r$. As $r \in S$, there exists some $q \in Z$ such that:
$a-bq=r$. If $r\geq b, r-b \geq 0\implies a -bq-r\geq 0$
This means $a-b(q+1) \in S$, but $a-b(q+1)<r$. Therefore the existence is proved by *contradiction*
