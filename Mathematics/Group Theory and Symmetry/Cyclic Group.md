A group $G$ is said to be **cyclic** if there exists an element $a \in G$ such that $G = <a>$.

Examples: $\mathbb{Z}$ is cyclic. $\mathbb{Z}/m\mathbb{Z}$ is cyclic for any $m>0$.

## Structure of Cyclic Group

Let $G$ be a cyclic group. Suppose $G=<a>$
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