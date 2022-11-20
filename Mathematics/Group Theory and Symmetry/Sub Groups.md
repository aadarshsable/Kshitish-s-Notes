Let $(G,*)$ be a [group](Groups). A subgroup of $G$ is a subset $H \subseteq G$ such that $*$ gives a binary operation on $H$, which gives $H$ the structure of a group.
More precisely, we say that the subset $H$ is a subgroup if the following are true:
1. $1_{H}$ is in $H$. 
2. $x,y$ in $H \implies x*y$ in $H$.
3. $x$ in $H \implies x ^{-1}$ in $H$. 
Note that we do not need to check that the binary operation on $H$ is associative as $*$ is known to be associative.

## Examples

1. Let $A$ be a subset of the plane. Then, if $G$ is the group of all [isometries](Isometries.md) of $A$, $G$ is a subgroup of $Perm(A)$
2. Let $G$ be any group. Then $G$ is a subgroup of itself. Any subgroup of $G$ that is not equal to the whole of $G$ is called a proper subgroup of $G$.
3. Let $G$ be a group and let $x$ be any element of $G$. Then, the set:
	$<x> = \{ x^{n} | \text{ n is an integer} \} = \{ 1_{G},x,x ^{-1},x^{2},x^{-2},\dots \}$
	is a subgroup of $G$.
4. Let $m$ be any integer. We define $mZ$ to be the set of all integer multiples of m. Then $mZ$ is a subgroup of $Z$. Indeed any element $x$ of $mZ$ maybe written as $x=md$ for some integer $d$. So, $-x=m(-d)$ and so $-x$ is also in $mZ$. Let $x$ any $y$ be in $mZ$. There exists integers $d_{1} \text{ and } d_{2}$ such that $x=md_{1}$ and $y=md_{2}$. So $x+y =md_{1}+md_{2} =m(d_{1}+d_{2})$; therefore $x+y \in mZ$.

## A Test for Sub Groups

$Proposition:$ Let $G$ be a group. Let $H$ be a non-empty subset of $G$. Then $H$ is a subgroup of $G$ if and only if for any $x,y$ in $H$. The element of $xy^{-1}$ is in $H$.

### Proof

Suppose $H$ is a subgroup of $G$. Let $x,y$ be in $H$. Then, $y^{-1}$ is in $H$. So $xy^{-1}$ is in $H$. So $xy^{-1}$ is in $H$. Thus the condition in the statement of the proposition holds. Conversely, suppose we know that for any $x,y$ in $H$, the element $xy^{-1}$ is in $H$.

Let $x$ be any element of $H$. (Recall - $H$ is non empty). Thus, $x \circ x ^{-1}=1_{G}$ is in $H$.

#### Inverses
Now, let $x$ be any element of $H$. As $1_{G}$ and $x$ are in $H$, so is $1_{G} \circ x ^{-1} = x ^{-1}$.

#### Products
Let $x,y$ be in $H$. Then $y ^{-1}$ is in $H$. So $x \circ (y ^{-1}) ^{-1} = x \circ y$ is in $H$. Thus $H$ is a subgroup.

## Order of a Group

Let $G$ be a group. The cardinality of the set $G$ is called the *order* of $G$.

### Finite Groups

A *finite group* is a group having finite order.

Let $G$ be a finite group. Let $x$ be an element of $G$. Then, the set $<x>:\{ x^{n} |\text{ }n \text{ is an integer} \}$ is a subgroup of $G$.
Thus $<x>$ is also a finite set.

Let $|G| = r$,
In the sequence $1,x^{2},x^{3},\dots,x^{r}$ all elements can not be distinct. So for some positive integers, $m<n$, we have $x^{m}=x^{n}$. So $x^{m-n}=1_{G}$. Also,
$n\leq r \implies n-m\leq r$
Thus we have proved the following:
$Theorem:$ Let $G$ be a finite group. Then, for any element of $x$ of $G$, there exists a positive integer $d \leq |G|$ such that $x^{d}=1$

### Groups of Small Order

#### Order 1
Order 1 groups are very simple as the only possible element in them is $\{ 1_{G} \}$. 

#### Order 2
Let $G$ be a group of order 2. Then, $G$ contains $1_{G}$ and some other element $x$. We already know $x \circ 1_{G}=1_{G} \circ x =x$. 
Then the next question we can ask is what is $x^{2}$.
$$
\text{If } x^{2}=x \implies x=1_{G} \implies \text{Contradiction}
$$
Therefore $x^{2}=1$.
So the multiplication table is,
|     | 1   | $x$   |
| --- | --- | --- |
| 1   | 1   | $x$   |
| $x$   | $x$   | 1   |    |     |     |

Thus there is only one group of order 2.

#### Order 3
Let $G$ be a group of order 3. Let all elements in the list: $\{ 1_{G},x,y \}$.
Next we must question what the value of $x^{2}$ could be.
- It can not be equal to one, as that would mean $x=1_{G}$.
- Suppose $x^{2}=1$. So $\{ 1,x^{2} \}$ is a subgroup of $G$.
	List: 1, $x$
	    $y$,
	We can now ponder about nature of $y \circ x$:
	- If $y \circ x =1$, $y=x ^{-1}$. But as $x^{2}=1 \implies x= x ^{-1}$ which means $y=x$ which is a contradiction.
	- If $y \circ x=x$ or $y \circ x=y$, $x=1 \text{ or } y=1$ which is a contradiction.
	Therefore $y \circ x$ can not be defined, therefore $x^{2} \neq 1$
- Therefore $x^{2}=y$.
	So, our list is $\{ 1,x,x^{2} \}$
	We can now ponder about nature of $x \circ x^{2}$.
	- If $x \circ x^{2}=1 \implies x^{2}=1$ which is a contradiction
	- If $x \circ x^{2}=x^{2} \implies x=1$ which is a contradiction
	So $x \circ x^{2}=1$. Therefore there is only 1 group of order 3.

#### Order 4
Let $G$ have order 4. Let $x$ be an element of $G$ such that $x \neq 1$. The list of all powers of $x$ is $1,x,x^{2},x^{3},\dots$
We know that there exists $d\leq4$, such that $x^{d}=1$. 
Since $x \neq 1$,
- Suppose $x^{2}=1$
	List: 1, $x$
	    $y$, $z$
	We have already seen in [[Sub Groups#Order 3 | order 3]] that $y \circ x$ can not be equal to $1, x \text{ or } y$. Therefore $y \circ x = z$.
	List: 1, $x$
	    $y$, $yx$
	$y^{2}$ can not be equal to $y$ or $yx$. Therefore it can only be $y^{2}=x \text{ or } y^{2}=1$
	- Case $y^{2}=x$
		So all the elements are $1,y,y^{2},y^{3}$ all distinct.
		Let $y^{4}$ be some element of this set.
		$y^{4} \ne y^{3} \neq y^{2} \neq y$ as that would lead to contradictions. So, $y^{4}=1$.
		Therefore one possible group is $\{ 1,y,y^{2},y^{3} \}$
	- Case $y^{2}=1$
		We can think about the $x \circ y$ next.
		If $x \circ y=1\implies y=x ^{-1}$ which is a contradiction as $x ^{2}= 1 \implies x = x ^{-1}$, which implies $x=y$.
		So $x \circ y \neq 1$.
		Similarly $x \circ y \neq x \neq y$.
		Therefore the only other possibility is $x \circ y=y \circ x$

		Now we can calculate all the products easily.
		Example:			$$
			\begin{align}
(x \circ y)(x \circ y) &= x (y \circ x) y \\
&=x(x \circ y)y \\
&=x^{2} \circ y^{2} \\
&=1
\end{align}
		$$
		Therefore we can say that $\{ 1, x, y, xy \}$ is a possible set.
		