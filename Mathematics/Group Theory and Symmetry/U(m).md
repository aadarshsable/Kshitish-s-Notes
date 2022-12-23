The set of all elements of $\mathbb{Z}/m\mathbb{Z}$ coprime to m is denoted by $U(m)$.

```ad-note
title: Note
color: 255,0,0
icon: exclamation

$1+m\mathbb{Z}$ is in $U(m)$ if $m>1$.
```

## Notation

If we *fix* the integer $m$, we may write the element $a+m\mathbb{Z}$ of $\mathbb{Z}/m\mathbb{Z}$ as $\bar{a}$. So, $\mathbb{Z}/m\mathbb{Z}=\{ \bar{0},\bar{1},\bar{2},\dots,\overline{m-1} \}$. Also, $\overline{m-1}=\bar{1}$, etc.

## Properties

1. If $a,b \in \mathbb{Z}$ such that $\bar{a},\bar{b} \in U(m)$ then $\overline{ab} \in U(m)$
2. Let $\bar{a},\bar{x},\bar{y} \in \mathbb{Z}/m\mathbb{Z}$ and $\bar{a} \in U(m)$ then if $\overline{ax}=\overline{ay}$, then $\bar{x}=\bar{y}$
3. Let $m$ be a positive integer. If $\bar{a} \in U(m)$, there exists $\bar{b}$ in $U(m)$ such that $\bar{a}.\bar{b}=1$
```ad-note
title: Theorem
icon: infinity
color: 0,255,255

Define:  $\phi: U(m) \to U(m)$ by $\phi(\bar{x})=\bar{a}.\bar{x}$.
According to property 2, $\phi$ is a $1-1$ function. As, $U(m)$ is a finite set, $\phi$ is a $1-1$ correspondence. Therefore $\phi$ is onto.
So, $\exists \text{ } \bar{b} \in U(m)$ such that $\phi(\bar{b})=1$.
So, $\bar{a}.\bar{b}=1$.
This proves the theorem corollary that:
$U(m)$ is a group under multiplication
```

## Examples

1. m=6
	$U(6)=\{ \bar{1}, \bar{5} \}$
	Note that $\bar{5}^{2}=\bar{25}=\bar{1}$
2. m=10
	$U(10)=\{ \bar{1},\bar{3},\bar{7},\bar{9} \}$
	$\bar{3}^{2}=\bar{9},\bar{3}^{3}=\overline{27}=\bar{7}$. So,
	$U(10)=\{ \bar{1},\bar{3},\bar{3}^{2},\bar{3}^{3} \}$

## Generators of $U(m)$
### The order of $U(m)$
$$
\begin{align}
|U(m)| &= \phi(m) \\
&= m \prod_{p_{i}|m}(1-\frac{1}{p_{i}})
\end{align}
$$
### Cyclicity of U(m)
$U(m)$ is cyclic if $m=1,2,4,p^{k},2p^{k}$ where $p$ is a odd prime number $k$ is any integer.
### Brute force one generator
In order to find rest of generators we need to brute force one generator at the very least.
Let the generator be $\langle g \rangle$
### Find all numbers coprime to $\phi(m)$
We find all numbers that are coprime to $\phi(m)$.
Let the set of all numbers be $\Sigma$
### Magic
All generators of $U(m)$ = $\{ \langle g \rangle ^{\sigma} \text{ } | \text{ } \sigma \in \Sigma\}$

### Example
Lets check if $U(27)$ is cyclic or not and if cyclic, we find its generators.
1. Check if $U(27)$ is cyclic.
	It is cyclic because $27 = 3^{3}$
2. Find $|U(27)|$
	$\phi(27)=27\left( 1-\frac{1}{3} \right)=27 \times \frac{2}{3} =18$
3. Try to brute force a generator
	In this case the easiest generator comes out to be $\langle 2 \rangle$
4. Find all numbers coprime to 18.
	$1,5,7,11,17$
5. Rest of generators
	$\langle g \rangle$ raised to powers $\{ 1,5,7,11,17 \}$ and then taking $mod(27)$.