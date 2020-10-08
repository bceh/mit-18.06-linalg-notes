
# 第九讲：线性相关性、基、维数

## 线性无关 (Linear Independence)

$v_1,\ v_2,\ \cdots,\ v_n$是$m\times n$矩阵$A$的列向量：

如果$A$零空间中有且仅有$0$向量，则各向量线性无关，$rank(A)=n$。

如果存在非零向量$c$使得$Ac=0$，则存在线性相关向量，$rank(A)\lt n$。

## 线性生成空间 (Linear Span)

Vectors $\vec v_1, \vec v_2, ... \vec v_k$ span a space when the space consists of all combinations of those vectors.

If vectors $\vec v_1, \vec v_2, ... \vec v_k$ span a space S, then S is **the smallest space** containing those vectors.

## 基和维数 (Basis and dimension)

向量空间$S$中的一组基（basis），具有两个性质：

1. 他们线性无关；
2. 他们可以生成$S$。

对于向量空间$\R^n$，如果$n$个向量组成的矩阵为可逆矩阵，则这$n$个向量为该空间的一组基。 $n$ 这该空间的维数。

> Given a space, every basis for that space has the same number of vectors; that number is the **dimension** of the space. So there are exactly $n$ vectors in every basis for $\R^n$.

## Bases of a column space and nullspace 

举例：
$
A=
\begin{bmatrix}
1 & 2 & 3 & 1 \\
1 & 1 & 2 & 1 \\
1 & 2 & 3 & 1 \\
\end{bmatrix}
$
，A的列向量线性相关，其零空间中有非零向量，所以

$$
\text{rank} (A) = \text {number of pivot columns of } A = \text {dimension of }C(A)
$$
Here $C(A)$ is the column space of the matrix $A$.

> Note that matrices have a rank but not a dimension. Subspaces have a dimension but not a rank.

可以很容易的求得$Ax=0$的两个解，如
$
x_1=
\begin{bmatrix}
-1 \\
-1 \\
1 \\
0 \\
\end{bmatrix}, 
x_2=
\begin{bmatrix}
-1 \\
0 \\
0 \\
1 \\
\end{bmatrix}
$，根据前几讲，我们知道特解的个数就是自由变量的个数，这两个特解形成了一个零空间的一组基。

我们得到：
$$
\text{dimension of } N(A) = \text {number of free variables} = n - r
$$
