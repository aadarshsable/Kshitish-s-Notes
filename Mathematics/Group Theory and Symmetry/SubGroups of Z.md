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

Case 1:
>Suppose $a\geq 0$.
>Then $a=a-b.0 \in S$

Case 2:
>Suppose $a< 0$
>Then $a-b(2a)=a(1-2b)$. As $b \geq1, \text{ } 2b\geq 2$ and so $1-2b <0$. As $a<0, \text{ } a(1-2b)>0$.
>So, $a-b(2a) \in S$. Therefore $S$ is non empty in this case too

So $S$ has a smallest element, which we can denote by $r$. As $r \in S$, there exists some $q \in Z$ such that:
$a-bq=r$. If $r\geq b, r-b \geq 0\implies a -bq-r\geq 0$
This means $a-b(q+1) \in S$, but $a-b(q+1)<r$. Therefore the existence is proved by *contradiction*
```
### Uniqueness

Suppose we have two pairs $(q_{1},r_{1})$ and $q_{2},r_{2}$ with the required property. So, $a=bq_{1}+r_{1}$ and $a=bq_{2}+r_{2}$.
Then if $r_{1}=r_{2}$, $q_{1}=q_{2}$.

So, if possible, let $r_{1} \ne r_{2}$. Suppose $r_{1}<r_{2}$. So $r_{2}-r_{1}>0$. Then $bq_{1}-bq_{2}=r_{2}-r_{1} \implies b(q_{1}-q_{2})=r_{2}-r_{1}$. As $b>0$ and $r_{2}-r_{1}>0$, we see that $q_{1}-q_{2}>0$. So, $q_{1}-q_{2}\geq1 \implies r_{2}-r_{1}=b(q_{1}-q_{2})\geq b$. But $r_{2}<b$ and $r_{1} \geq0$
So $r_{2}-r_{1}<b$ which is a **contradiction**.
So, the case of $r_{1}=r_{2}$ is impossible. Thus, $r_{1}=r_{2}$ and so $q_{1}=q_{2}$. This therefore proves the uniqueness of the the ordered pair $(q,r)$

```ad-note
title: Theorem
icon: infinity
color: 0,255,255

Any subgroup $H$ of $\mathbb{Z}$ is of the form $m\mathbb{Z}$ for some $m \geq 0$.

Proof:
Let $H$ be a subgroup of $\mathbb{Z}$.
Let $S=\{ x \text{ }| \text{ } x \in H,x>0 \}$

Case 1:
>Suppose $S=\phi$.
>Thus all elements of $H$ are non positive. If $\exists \text{ } x \in H$ such that $x<0$, then $-x>0$. But $-x \in H \implies -x \in S$ which is a **contradiction**
>So $H$ has no negative elements, so $H=\{ 0 \}$, so we can take $m=0$


Case 2:
>Suppose $S \ne \phi$.
>Then, $S$ has a smallest element, which we denote by $m$. We claim that $H=m\mathbb{Z}$. Indeed, suppose $x \in H$ is any element. By division algorithm, $\exists \text{ } q,r \in \mathbb{Z}$ such that $x=qm+r$, $0\leq r < m$. 
>Then, as $x \in H$ and $qm\in H$, $r=x-qm \in H$. If $r>0, e \in S$.
>But $r<m$ and $m$ is the smallest element of $S$ which is a **contradiction**.
>So, $r=0$
Thus, $x=q.m \implies x \in m\mathbb{Z}$
Thus, $H \subseteq m\mathbb{Z}$
But, $m\mathbb{Z} \subseteq H \implies H=m\mathbb{Z}$  
```

## Cosets of Subgroup of $\mathbb{Z}$
