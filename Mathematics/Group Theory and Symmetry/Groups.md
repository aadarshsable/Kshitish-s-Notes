A group consists of a set $G$ with a given binary operation:
$*: G$ x $G$ $\rightarrow$ $G$ that follows the properties of the group

## Properties of $G$

- $id_{G}$ is in $G$
- $f,g$ in $G$ $\implies$ $g \circ f$ is in $G$
- $f$ in $G$ $\implies$ $f^{-1}$ in $G$
- If $f,g,h$ are in $G$, then $f \circ (g \circ h) = (f \circ g) \circ h$

## Identity Element

Let $a,b,c$ be elements of a group $G$.
If either $ab = ac$ or $ba =ca$, then $b = c$.
In other words, we can cancel c either on the left or the right. Therefore this property can be also called "cancelation" property.

### Proof

Suppose $ab = ac$, then:
$a^{-1}(ab) = a^{-1}(ac)$. So, by associativity,
$(a^{-1}a)b = (a^{-1}a)c$
So, $id_{G}.b = id_{G}.c$, i.e. b = c.

If $ba=ca$, the proof is similar.

Remark: It is not true in general that $ab =ca \implies b=c$. For example, in the diheadral group $D_{3},\text{ } \rho^{2}\tau=\tau \rho$. 
However we can not just cancel $\tau$ as that would mean $\rho^{2} = \rho$  which is false.

### Uniqueness of the Identity Element

$Theorem :$ Let $G$ be a groupand let $f$ be an element of $G$ such that $fx = x$ for some $x$ in group $G$. Then $f = 1_{G}$.

#### Proof

$fx = x \implies f =1_{G}$ by "cancelling" $x$ on the right.

We only need to assume $fx=x$ for some $x$ in $G$ and not necessarily for all $x$ in $G$. Also we do not need to assume: $xf=x$.


## Inverses

In case of inverses, the axiom only states that for any $f$ in $G$, there exists some inverse $f^{-1}$ such that $f \circ f^{-1}=f^{-1}\circ f=1_{G}$. However it is easy to deduce a much stronger statement out of this.

### Uniqueness of Inverse

$Theorem:$ Let $G$ be a group and let $f$ be an element of $G$. If $h$ is an element of such that: $f \circ h=1_{G}$, then $h=f^{-1}$. Similarly, if $h$ satisfies $h \circ f=1_{G}$ then $h= f^{-1}$.

#### Proof

$h = 1_{G} \circ h = (f \circ f^{-1})\circ h= f^{-1}(f \circ h)=f^{-1}\circ 1_{G}=f^{-1}$

The proof in the case of $hf=1_{G}$ is also similar.

#### Inverses of a Product

Note that if $a,b$ are in a group $G$:
$(ab)^{-1} = b^{-1} \circ a^{-1}$

The order of operation for this operation is essential. As the reverse is not true.

Indeed,
$ab(a^{-1}b^{-1}) = a (bb^{-1})a^{-1}=a.1_{G}.a^{-1}=aa^{-1}=1_{G}$

In general,  $a^{-1}b^{-1}\neq b^{-1}a^{-1}$.

## Notation

If the binary operation in a group is being written like multiplication, we write $f^{n}$ for $f. f\dots f$  for $n$ times where   is a positive number.

We can also write $f^{-n}$ for $(f^{-1})^{n}$. One can check that this behaves as expected, i.e. $f^{m}.f^{n} =f^{m+n}$ for any integers $m$ and $n$.

[[Isometeries]]