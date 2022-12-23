The cosets of $m\mathbb{Z}$ are $m\mathbb{Z},1+m\mathbb{Z},\dots$
For integers $a$ and $b$, the following statements are equivalent:
1. $a+m\mathbb{Z}=b+m\mathbb{Z}$
2. $a-b$ is divisible by $m$
3. $a$ and $b$ leave the same remainder when divided by $m$

## Notation

1. If $m$ divides $a-b$, then we can write	$$
	a \equiv b \text{ } mod(m)
	$$This reads as "a is congruent to b modulo m". This essentially means that $a$ and $b$ are in the same coset of $m\mathbb{Z}$.
2. The statement "m divides x" will be symbolically written as $m|x$.

## Results

```ad-note
title: Addition
color: 0,255,255

$a \equiv b \text{ } mod(m)$ and
$c \equiv d \text{ } mod(m)$
$\implies a+c \equiv b+d \text{ } mod(m)$
Proof:
$m | a-b \implies a-b \equiv mx$ for some $x \in \mathbb{Z}$
$m | c-d \implies c-d \equiv my$ for some $y \in \mathbb{Z}$

So,
$$
\begin{align}
(a+c)-(b+d) &= (a-b) + (c-d) \\
&=mx+my \\
&=m(x+y) \\

\text{So, }  a+c=b+d \text{ } mod(m)
\end{align}
$$
```

```ad-note
title: Multiplication
color: 255,0,255
$a \equiv b \text{ } mod(m)$ and $c \equiv d \text{ } mod(m)$
$\implies ac \equiv bd \text{ } (mod \text{ } m)$

Proof:
	$a-b=mx$ and $c-d=my$ for some $x,y \in \mathbb{Z}$
	So,
	$$
	\begin{align}
ac-bd &=(b+mx)(d+my)-bd \\
&=m(xd+by+mxy)
\end{align}
	$$
This shows that,
$ac \equiv bd \text{ } mod(m)$
```

This means we can define binary operations $+$ and $\times$ on $Z/m\mathbb{Z}$.

## Binary Operations on $\mathbb{Z}/m\mathbb{Z}$

Given two cosets $a+m\mathbb{Z}$ and $b+m\mathbb{Z}$, we can define:
$(a+m\mathbb{Z})+(b+m\mathbb{Z})=(x+y)+m\mathbb{Z}$ where $x \in a +m\mathbb{Z} \text{ and } y \in b +m\mathbb{Z}$

```ad-note
title: Note
icon: exclamation
color: 125,0,0

The answer does not depend on the choice of $x$ and $y$.

Proof:
	Pick some element $x_{1} \in a+m\mathbb{Z}$ and $y_{1} \in b+m\mathbb{Z}$.
	
	Then as $x$ and $x_{1}$ lie in the same coset and $y$ and $y_{1}$ lie in the same coset.
	
	$x \equiv x_{1} \text{ } mod(m)$ and $y \equiv y_{1} \text{ } mod(m)$.
	
	So, $(x+y) \equiv (x_{1}+y_{1}) \text{ } mod(m)$.
	
	So, $(x+y)+m\mathbb{Z} = (x_{1}+y_{1})+m\mathbb{Z}$.
	
	Similarly we can define multiplication on $\mathbb{Z}/m\mathbb{Z}$
```

## Basic Properties

1. $m\mathbb{Z}$ is the identity:
		$(m\mathbb{Z})+(a+m\mathbb{Z})=(a+0)+m\mathbb{Z}=a+m\mathbb{Z}$
		
2. $(-a) +m\mathbb{Z}$ is the inverse:
		$(a+m\mathbb{Z})+(-a+m\mathbb{Z})=(a-a)+m\mathbb{Z}=m\mathbb{Z}$
		
3. Associativity:	$$
		\begin{align}
(a+m\mathbb{Z})+((b+m\mathbb{Z})+(c+m\mathbb{Z})) \\
= (a+m\mathbb{Z})+((b+c)+m\mathbb{Z}) \\
= (a+(b+c))+m\mathbb{Z} \\
= ((a+b)+c)+m\mathbb{Z} \\
= ((a+b)+m\mathbb{Z})+(c+m\mathbb{Z}) \\
= ((a+m\mathbb{Z})+(b+m\mathbb{Z}))+(c+m\mathbb{Z}) \\
= (a+m\mathbb{Z})+(b+m\mathbb{Z})+(c+m\mathbb{Z})
\end{align}
		$$
4. Distributivity:
	Recall that in $\mathbb{Z},\mathbb{Q},\mathbb{R}$; multiplication distributes over addition. In other words, $(a+b).c=ac+bc$ and $a.(b+c)=ab+ac$. We get such identities in $\mathbb{Z}/m\mathbb{Z}$ as well.
	
5. Multiplicative Inverses in $\mathbb{Z}/\mathbb{Z}$:
	We say that  an element $(a+m\mathbb{Z})$ on $(\mathbb{Z}/m\mathbb{Z})$ is invertible if it has a multiplicative inverse, i.e. if there exists an integer $b$ such that $(a+m\mathbb{Z}).(b+m\mathbb{Z})=1+m\mathbb{Z}$
	Suppose $a+m\mathbb{Z}$ has a multiplicative inverse $b+m\mathbb{Z}$. Then, $ab+m\mathbb{Z} =1 + m\mathbb{Z}$, i.e. $ab \equiv 1 \text{ } mod(m)$.
	Thus $m|ab-1$; Let $d$ be any common factor of $m$ and $a$. 
	Thus $m=dx$ and $a=dy$ for some $x,y \in \mathbb{Z}$
	As $m|ab-1$, $ab-1=mz$ for some $z \in \mathbb{Z}$.
	So, $$
	\begin{align}
1 &=ab-mz \\
&=(dy)b-(dx)z \\
&=d(yb-xz)
\end{align}
	$$
	So $d|1$, so $d=\pm1$. Thus we can see that the only common factors of $m$ and $a$ are $\pm1$.
	Hence, we have proved that $a+m\mathbb{Z}$ is invertible only if $gcd(a,m)=1$, i.e. $a$ and $m$ are coprime to each other.
	The reverse can also be said, if $gcd(a,m)=1$ then $a+m\mathbb{Z}$ is also invertible.
	
