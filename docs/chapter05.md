
# 第五讲：转换、置换、向量空间R 


## 置换矩阵（Permutation Matrix）

$P$为置换矩阵，对任意可逆矩阵$A$有：

$PA=LU$

$n$阶方阵的置换矩阵$P$有$\binom{n}{1}=n!$个

> 置换矩阵是一种系数只由0和1组成的方块矩阵。置换矩阵的每一行和每一列都恰好有一个1，其余元素都是0。在线性代数中，每个n阶的置换矩阵都代表了一个对n个元素的置换。当一个矩阵乘上一个置换矩阵时，所得到的是原来矩阵的横行或纵列经过置换后得到的矩阵。 
> 当一个矩阵乘上一个置换矩阵时，所得到的是原来矩阵的横行（置换矩阵在左）或纵列（置换矩阵在右）经过置换后得到的矩阵。-wikipedia

对置换矩阵$P$，有$P^{-1} = p^T$; $P^TP = I$


## 转置矩阵（Transpose Matrix）
When we take the transpose of a matrix, its rows become columns and its columns become rows.

$(A^T)_{ij} = (A)_{ji}$


## 对称矩阵 ()
For a symmetric matrix, $A$, 
$A^T = A$.

Given Any matrix R (not necessarily square) the product $R^TR$ is always symmetric.
$$
(R^TR)^T = R^T(R^T)^T = R^TR
$$



## 向量空间（Vector Space）

We can add vectors and multiply them by numbers, which means we can discuss **linear combinations** of vectors. These combinations follow the rules of a vector space.

> A **vector space** is a collection of vectors which is closed under linear combinations. In other words, for any two vectors $\vec v$ and $\vec w$ in the space and any two real numbers $c$ and $d$, the vector $c \vec v+d \vec w$ is also in the vector space.

One such vector space is $\R^2$, the set of all vectors with exactly two real number components. We depict the vector $\left[ \begin{matrix} 
a \\b \end{matrix} \right]$
by drawing an arrow from the origin to the point (a, b) which is a units to the right of the origin and b units above it, and we call $\R^2$ the “$x − y$ plane”.

Another example of a space is $\R^n$, the set of (column) vectors with $n$ real number components.

If a collection of vectors is closed under **linear combinations** (i.e. under addition and multiplication by any real numbers), and if multiplication and addition behave in a reasonable way, then we call that collection a vector space.

## 子空间 (Subspace)

A vector space that is contained inside of another vector space is called a **subspace** of that space.

> A subspace is a vector space contained inside a vector space.

Every subspace **must contain the zero vector** because vector spaces are closed under multiplication.

The subspaces of R2 are:

1. all of $\R^2$;
2. any line through $\left[ \begin{matrix}  0  \\ 0 \end{matrix} \right]$
3. the zero vector alone ($\Z$).

The subspaces of $\R^3$ are:
1. all of $\R^3$;
2. any plane through the origin;
3. any line through the origin;
4. the zero vector alone ($\Z$).

For two subspace $S$ and $T$，the intersection $S \cap T$ of two subspace is a subspace。But the union $S \cup T$ of two subspace is generally **not** a subspace. 

## 列空间 (Column space)
Given a matrix $A$ with columns in $\R^3$, these columns and all their linear combinations form a subspace of $\R^3$. This is the **column space** C(A).

If $A = \left[ \begin{matrix} 
1 & 3 \\
2 & 3  \\
4 & 1 
\end{matrix} \right]$,
the column space of $A$ is the plane through the origin in $\R^3$ containing $\left[ \begin{matrix} 
1  \\
2   \\
4 
\end{matrix} \right]$, and $\left[ \begin{matrix} 
 3 \\
 3  \\
 1 
\end{matrix} \right]$.

## solving $A \vec x = \vec b$
The system of linear equations $A \vec x = \vec b$ is solvable exactly when $\vec b$ is a vector in the column space of $A$.

## 核 Nullspace (Kernel) of $A$
The **nullspace** of a matrix $A$ is the collection of all solutions $\vec x$ to the equation $A \vec x = \vec 0$.

A nullspace is also a vector space: \
The sum of solutions is also a sultion:
$$ 
A(\vec x_1 + \vec x_2) = A\vec x_1 + A \vec x_2 = \vec 0 + \vec 0
$$
The multiple of solutions is also a solution:
$$
A(c \vec x) = cA \vec x = c (\vec0)
$$

if $\vec b$ is not $\vec 0$: \
The solutions to the equation $A \vec x = \vec b$ do **not** form a subspace. Becuase the $\vec 0$ is not a solution to this equation. 

## Rank
The rank of a matrix $A$ equals the number of **pivots** it has. 