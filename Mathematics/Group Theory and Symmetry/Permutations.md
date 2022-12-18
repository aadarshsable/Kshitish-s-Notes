
## Introduction to Permutations

Given a set $A$, a permutation of $A$ is a $1-1$ correspondence from $A$ to itself. The set of all permutations of $A$ is denoted by $Perm(A)$

### Properties of Permutation

1. Identity Function:  $id_{A}: A \rightarrow A$ defined by $id_{A}(x) = x$ is an element of $Perm(A)$. For any $f$ in $Perm(A)$: $f \circ id_{A} = id_{A} \circ f = f$
2. If $f,g$ are in $Perm(A)$,the composition $g \circ f$ is also in $Perm(A)$
3. If $f$ is in $Perm(A)$, $f^{-1}$ is also in $Perm(A)$
4. If $f,g,h$ are in $Perm(A)$: $(f \circ g ) \circ h = f \circ ( g \circ h)$

## Perm(S)
Let $S$ be a set. 
Let $Perm(S)$ be the set of all permutations of $S$.
We know that $Perm(S)$ is a group under the binary operation of composition. 
We shall focus on the cases where $S$ is a finite set.

For any positive integer $n$, we define $S_{n}$ to be the group of permutations of $\{ 1,2,3,4\dots,n \}$

## Array Notation

Let $\sigma \in S_{n}$. Then, we can write $\sigma$ as a $2 \times n$ array as follows:
$$
\begin{bmatrix}
1 & 2 & 3 & 4 & 5 & \dots & n \\
\sigma(1) & \sigma(2) & \sigma(3) & \sigma(4)  & \sigma(5) & \dots & \sigma(n)
\end{bmatrix}
$$

### Example
If $n=5$:
$$
\sigma = \begin{bmatrix}
1 & 2 & 3 & 4 & 5 \\
2 & 5 & 4 & 3 & 1
\end{bmatrix}
$$
Then,
$$
\sigma ^{-1}= \begin{bmatrix}
1 & 2 & 3 & 4 & 5 \\
5 & 1 & 4 & 3 & 2
\end{bmatrix}
$$
Suppose
$$
\tau=\begin{bmatrix}
1 & 2 & 3 & 4 & 5 \\
3 & 2 & 1 & 5 & 4
\end{bmatrix}
$$
Then,
![Sigma compose Tau](https://i.imgur.com/ApUf1yf.png)

## Order of $S_{n}$

Suppose we want to construct a permutation of the set $\{ 1,2,3,4,\dots,n \}$. Let us denote the permutation by $\sigma$.

We will construct $\sigma$ by choosing the elements of $\sigma(1),\sigma(2),\dots$.
After we have $n$ choices for $\sigma(1)$. After $\sigma(1)$ is chosen, we have $(n-1)$ choices for $\sigma(2)$ as $\sigma(1) \ne \sigma(2)$. And so on we have $n-2$ choices for $\sigma(3)$. Continuing in this manner, it can be seen that $\sigma$ can be constructed in $n(n-1)(n-2)(n-3)\dots2.1$ ways.
We call this number the factorial of $n$ and write it as $n!$. Thus $|S_{n}|=n!$

### Example:

![Example of Order](https://i.imgur.com/bxgfcmI.png)

## Cycle Decomposition

Let $\sigma$ be a permutation of $\{ 1,2,3,4,\dots,n \}$. Consider the sequence $1,\sigma(1),\sigma^{2}(2),\dots$
Since $ord(\sigma)$ is finite, we know that there exists a positive integer $m$ such that $\sigma^{m}(1)=1$. Let $r$ be the smallest positive integer such that $\sigma^{r}(1)=1$.

```ad-note
title: Note
color: 255,0,0
icon: exclamation

We do not need $\sigma^{r}=1$, only that $\sigma^{r}(1)=1$. So, $r$ maybe smaller than $ord(\sigma)$
```

We claim that the elements $1,\sigma(1),\dots,\sigma^{r-1}(1)$ are all distinct.

If not, there exists non-negative integers $i<j$ such that $\sigma^{i}(1)=\sigma^{j}(1)$. Composing with $\sigma^{-i}$ on both sides, we get $\sigma^{j-i}(1)=1$. But $j-i>0$ and $j-i<r$. This contradicts the minimality of $r$. Thus, the elements $1,\sigma(1),\dots,\sigma^{r-1}(1)$ are all distinct.

If not, there exist non negative integers $i<j$ such that $\sigma^{i}(1)=\sigma^{j}(1)$. Composing with $\sigma ^{-i}$ on both sides we get $\sigma^{j-i}(1)=1$.
But $j-i>0$ and $j-i<r$. This contradicts the minimality of $r$.

Thus the elements $1,\sigma(1),\dots,\sigma^{r-1}(1)$ are all distinct. In fact, the infinite sequence $\dots,\sigma^{-2}(1),\sigma^{-1}(1),1,\sigma(1),\sigma^{2}(1),\dots$ consists of the pattern $1,\sigma(1),\dots$ repeating infinitely (in both direction).

![Pictorial Representation](https://i.imgur.com/XLYPmza.png)

Let $A_{1}= \{ 1, \sigma(1), \dots,\sigma^{r-1}(1) \}$
If $A_{1} \ne \{ 1,2,3,\dots,n \}$, choose some $x \notin A_{1}$ and repeat the process to obtain a cycle:
$x,\sigma(x),\dots,\sigma^{s-1}(x)$ for some integer value of $s$.

Let $A_{2}=\{ x, \sigma(x), \dots, \sigma^{s-1}(x) \}$
![Pictorial Represenattion 2](https://i.imgur.com/ZeDJXnX.png)

Observer that $A_{1}$ and $A_{2}$ are disjoint. If $A_{1} \cup A_{2} =\{ 1,2,3,\dots,n \}$, we stop. Otherwise, we choose some $y \notin A_{1} \cup A_{2}$ and repeat the process. 
This process must end in at most $n$ steps.

Suppose, after $p$ steps, we have disjoint sets $A_{1},A_{2},\dots,A_{p}$ such that $\sigma$ acts on the elements of each $A_{i}$ "cyclically".

## Cycle

A permutation $\sigma$ of a set $S$ is called a cycle if there exists a finite set $A=\{ a_{1},\dots,a_{r} \}$ such that $\sigma(a_{1})=a_{2},\sigma(a_{2})=a_{3},\dots,\sigma(a_{r})=a_{1}$.
The integer $r$ is called the **length of the cycle**. The cycle $\sigma$ is then written as $(a_{1},a_{2},\dots,a_{r})$.
Two cycles $(a_{1},a_{2},\dots,a_{r})$ and $(b_{1},b_{2},\dots,b_{r})$ are said to be disjoint if $a_{k} \ne b_{l}$ for any $k,l$. 

Recall that we have partitioned the set $\{ 1,2,3,\dots,n \}$ into $p$ *disjoint* subsets $A_{1},A_{2},A_{3},\dots,A_{p}$ such that for each $i$, $1 \leq i \leq p$, $A_{i}= \{ a_{i_{1}},a_{i_{2}},\dots,a_{i_{r_{i}}} \}$ and $\sigma(a_{i_{1}})=a_{i_{2}},\dots,\sigma(a_{i_{r_{i}}})=a_{i_{1}}$.
Then, we observe that if $\sigma_{i}=(a_{i_{1}},a_{i_{2}},\dots)$ then
$\sigma= \sigma_{1} \circ \sigma_{2} \circ \sigma_{3}\dots \circ \sigma_{p}$. Indeed for any $x \in \{ 1,2,\dots,n \}$ there is some $i$ such that $x \in A_{i}$. Let us compute $\sigma_{1} \circ \sigma_{2}\dots \circ \sigma_{p}(x)$.

Thus, $\sigma = \sigma_{1} \circ \sigma_{2} \circ \sigma_{3} \circ \dots \circ \sigma_{p}$.
This is called cycle decomposition of $\sigma$. For example:
$$
\begin{align}
n=8 &,\sigma(1)=5,\sigma(2)=4,\sigma(3)=7,\sigma(4)=6 \\
&,\sigma(5)=3,\sigma(6)=2,\sigma(7)=1,\sigma(8)=8
\end{align}
$$
Then $\sigma=(1,5,3,7)(2,4,6)(8)$
The cycle decomposition of any permutation is unique, however a cycle can be written in many different ways. For example:
$(a,b,c)=(b,c,a)$
Secondly disjoint cycles commute, they can be composed in any order. $(1,3,4)(2,5)=(2,5)(1,3,4)$

```ad-note
title: Note
color: 255,0,0
symbol: exclamation
Note that the cycle of length $1$ is just the identity element. So, we often choose not to write 1-cycles in a cycle decomposition.
```

### Examples

**Elements of $S_{4}$:**
1. *Identity element*: $id$

2. *$2$-cycles*: $(1,2),(1,3),(1,4),(2,3),(2,4),(3,4)$

3. *$3$-cycles*: 	$(1,2,3),(1,3,2),(1,2,4),(1,4,2),(1,3,4),(1,4,3),(2,3,4),(2,4,3)$
4. *$4$-cycles*: $(1,2,3,4),(1,2,4,3),(1,3,2,4),(1,3,4,2),(1,4,2,3),(1,4,3,2)$

##### Product of $2$ cycles:
$(1,2)(3,4),(1,4)(2,3),(1,3)(2,4)$

### Order of the Permutation
Let $S$ be a set. Let $\sigma=(a_{1},a_{2},\dots,a_{m})$ and $\tau=(b_{1},b_{2},\dots,b_{n})$ be disjoint cycle in $Perm(S)$. Then, we will prove that
$ord(\sigma \tau)=lcm(m,n)$

Example:
$n=10$
$\sigma= (1,4,7,2,9,3)(5,8,6,10)$
Then $ord(\sigma)=lcm(6,4)=12$


