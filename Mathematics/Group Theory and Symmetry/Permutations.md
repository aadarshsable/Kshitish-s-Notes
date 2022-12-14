
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
