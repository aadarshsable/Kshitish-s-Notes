## Order of an element

Suppose $G = <a>$. Then, a typical element of $G$ is of the form $a^{k}$ where $k \in \mathbb{Z}$.
If $ord(a)$ is not finite, then $G$ is isomorphic to $\mathbb{Z}$. In this case, any non-identity element has **infinite** order.

So, now suppose $ord(a) =m$, where $m$ is a positive integer. Suppose $k$ is positive. We consider the sequence:
$a^{k},a^{2k},a^{3k},\dots$
The first time $1$ will occur in this sequence at $a^{kd}$, where $kd$ is the smallest multiple of $k$ which is also a multiple of $m$. So, $kd=lcm(k,m)$

Recall: $k.m=gcd(k,m).lcm(k,m)$
So we can see that:
$$
\begin{align}
ord(a^{k})=d &=\frac{lcm(k,m)}{k} \\
&= \frac{m}{gcd(k,m)}
\end{align}
$$
If $k$ is negative, we can apply this argument to $-k$ to get 
$ord(a^{-k})=\frac{m}{gcd(-k,m)}$
However, $ord(a^{k})=ord(a^{-k})$
and $gcd(k,m)=gcd(-k,m)$
So, $ord(a^{k})=\frac{m}{gcd(k,m)}$
We have proved:
Theorem 1: Suppose $G=<a>$ and $ord(a)=m$, where $m \in \mathbb{Z}$. Then, $ord(a^{k})=\frac{m}{gcd(k,m)}$ for any integer $k$.

Note that for any element $x$ of a group, $|<x>|=ord(x)$. So we have:
**Corollary 1**: Under the above hypothesis, $|<a^{k}>|=\frac{m}{gcd(k,m)}$
**Corollary 2**: Under the above hypothesis, $a^{k}$ is a generator of $G=<a>$ if and only if $gcd(k,m)=1$,i.e. $\bar{k} \in U(m)$

More generally, we see that $a^{k}$ and $a^{l}$ have the same order $\iff$ $gcd(k,m)=gcd(l,m)$. Now, for a fixed integer $k$, let $d=gcd(k,m)$. So, $ord(a^{d})=ord(a^{k})=m/d$.
So, $|<a^{d}>|=m/d$
However, we also see that $a^{k}=(a^{d})^{k/d}$ is an element of $<a^{d}>$.
As $ord(a^{k})=m/d=|<a^{d}>|$,
we see that $a^{k}$ generates the subgroup $<a^{d}>$. So we have proved that:
Suppose $G = <a>$ with $ord(a)=m \in \mathbb{Z}$. Then, for any $k \in \mathbb{Z}$, $<a^{k}>=<a^{gcd(k,m)}>$

