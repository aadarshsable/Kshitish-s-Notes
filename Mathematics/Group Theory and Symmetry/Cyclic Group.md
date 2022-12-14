A group $G$ is said to be **cyclic** if there exists an element $a \in G$ such that $G = \langle a \rangle$.

Examples: $\mathbb{Z}$ is cyclic. $\mathbb{Z}/m\mathbb{Z}$ is cyclic for any $m>0$.

## Structure of Cyclic Group

Let $G$ be a cyclic group. Suppose $G=\langle a \rangle$
We have two possibilities:
1. $ord(a)$ is finite
2. $ord(a)$ is infinite

## $ord(a)$ is not finite

This means that there does not exist any positive integer $m$ such that $a^{m}=1$
Consider the sequence (extending in both directions)
$$
\dots,a^{-2},a^{-1},1,a,a^{2},\dots
$$
We claim that all these elements are distinct. In other words, we claim that if $i,j$ are **distinct** integers, then $a^{i} \ne a^{j}$. Suppose this is not true.

Then there exists some integers $i,j$ for which $a^{i}=a^{j}$ such that $i<j$. Then $a^{j-i}=1$.
As $j-i>0$, this contradicts our assumption that $ord(a)$ is not finite.

Let $\phi: \mathbb{Z} \to G$ be the function defined by $\phi(n)=a^{n}$. We have proved above that $\phi$ is a $1-1$ function. $\phi$ is also onto as $G = <a>$. Thus we can say that $\phi$ is a $1-1$ correspondence.

Also, $$
\begin{align}
\phi(m+n) &= a^{m+n} \\
&=a^{m}.a^{n} \\
&=\phi(m).\phi(n)
\end{align}
$$
Thus, $\phi$ is a group isomorphism.

## $ord(a)=m$ for some $m \in \mathbb{Z}$

Lemma:
Suppose $a^{n}=1$ for some integer $n$. Then, $m|n$

Proof:
using the division algorithm, we write
$n=mq+r$ where $0 \leq r < m$
Then $1=a^{n}=a^{mq+r}=(a^{m})^{q}.a^{r}=1.a^{r}=a^{r}$
But $r<m$, so $a^{r}=1$ is impossible unless $r=0$.

Suppose $i$ and $j$ are distinct integers such that $a^{i}=a^{j}$. Then $a^{i-j}$ =1. So, $m|i-j$, i.e. $i \equiv j \text{ } mod(m)$. Conversely, if $i \equiv j \text{ } mod(m)$ then  $i=j+mx$ for some $x \in \mathbb{Z}$
So, $a^{i}=a^{mx+j}=(a^{m})^{x}.a^{j}=a^{j}$
Thus, $a^{i}=a^{j}$ if and only if $i$ and $j$ lie in the same coset of $m\mathbb{Z}$.

We define
$\phi: \mathbb{Z}/m\mathbb{Z} \to <a>$ by
$\phi(\bar{n})=a^{n}$
This is well defined because if $\bar{n_{1}}=\bar{n_{2}}$, then $n_{1} \equiv n_{2} \text{ } mod(m)$ and so $a^{n_{1}}=a^{n_{2}}$
Also, if $\phi(\bar{n_{1}})=\phi(\bar{n_{2}})$, we have seen that $n_{1} \equiv n_{2} \text{ } mod(m)$, i.e. $\bar{n_{1}}=\bar{n_{2}}$.
So $\phi$ is a $1-1$ function and is indeed onto for any $n \in \mathbb{Z}$, $\phi(\bar{n})=a^{n}$.
Thus $\phi$ is a $1-1$ correspondence.
$$
\begin{align}
\phi(\bar{n_{1}}+\bar{n_{2}}) &= a^{n_{1}+n_{2}} \\
&= a^{n_{1}}.a^{n_{2}} \\
&= \phi(\bar{n_{1}}).\phi(\bar{n_{2}})
\end{align}
$$
Thus, $\phi$ is a group isomorphism.