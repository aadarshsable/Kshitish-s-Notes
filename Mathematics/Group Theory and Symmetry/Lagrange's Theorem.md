Let $G$ be a group such that $ord(x)=d$.
Partial List: $1,x,x^{2},x^{3},\dots,x^{d-1}$. Note that these are distinct elements.
Indeed, we suppose:
$x^{i}=x^{j}$ for some $i<j\leq d-1$
Then  $x^{j-1}=1$,
But $0<j-1 \leq d-1 < d$
But order of $x$ is $d$ and so, $x^{j-1} \neq 1 \rightarrow$ Contradiction

If $<x> = G$, we have listed all elements of $G$. Otherwise, suppose $y$ is such that $y \in G, y \notin <x>$. Then we could write the row as:
$y,yx,yx^{2},y^{3},\dots,yx^{d-1}$ below the first one.

Now we just need to check for 2 conditions:
1. Distinction of elements
		Assume $yx^{i}=yx^{j}$ for any $i<j \leq d-1$ we can see that $x^{i}=x^{j}$. But we already know that all compositions of $x$ are distinct. Therefore we get an contradiction, proving that all elements are distinct.
2. Overlap with first row
	Assume $x^{i}=yx^{j} \implies y=x^{j-i}$ but we have already assumed that $y \notin <x>$

So we can see that if $G \neq <x>$, we can add a complete row  underneath the first one:
$\{y,yx,yx^{2}\dots,yx^{d-1}\}=y<x>$ 

If this is the complete list of all elements of $G$ we can stop, otherwise there is some $z \in G$ such that $z \notin <x>, z \notin y<x>$. Then the third row can be written as a combination of $z \text{ and } <x>$.
$z<x> = \{ z,zx,zx^{2},zx^{3},\dots,zx^{d-1} \}$
By the same argument as before these are $d$ distinct elements.

We can also check for overlaps with first row by assuming and contradicting $zx^{i}=x^{j}$ for some $i,j$. Similarly we can do this for all other rows. The process will continue until we exhaust the group. This process will end if $|G|$ is finite. Then we can see that $d$ divides $|G|$. Thus we have proved Lagrange's theorem which states:

**Let $G$ be a finite group. Then, for any $x \in G$, order of $x$ divides $|G|$.**
