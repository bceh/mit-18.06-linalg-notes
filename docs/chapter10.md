
# 第十讲 四个基本子空间

对于$m \times n$矩阵$A$，$rank(A)=r$有：

* 列空间 $C(A) \in \mathbb{R}^m, \text{dim } C(A)=r$。

    > The **column space**, $C(A)$, consists of all combinations of the columns of $A$ and is a vector space in $\R^m$.

* 零空间 $N(A) \in \mathbb{R}^n, \text{dim } N(A)=n-r$。

    > The **nullspace**, $N(A)$ consists of all solutions $x$ of the equation $Ax = 0$ and lies in $\R^n$.

* 行空间 $C(A^T) \in \R^n, \text{dim } C(A^T)=r$。

    > The **Row space**, $C(A^T)$, is the combinations of the row vectors of $A$ form a subspace of $\R^n$. We equate this with $C(A^T)$, the column space of the transpose of $A$.

* 左零空间 $N(A^T) \in \mathbb{R}^m, \text{dim } N(A^T)=m-r$，
    
    > the nullspace of $A^T$ the **left nullspace** of $A$. This is a subspace of $\R^m$


例1，对于行空间
$
A=
\begin{bmatrix}
1 & 2 & 3 & 1 \\
1 & 1 & 2 & 1 \\
1 & 2 & 3 & 1 \\
\end{bmatrix}
\underrightarrow{消元、化简}
\begin{bmatrix}
1 & 0 & 1 & 1 \\
0 & 1 & 1 & 0 \\
0 & 0 & 0 & 0 \\
\end{bmatrix}
=R
$

由于我们做了行变换，所以A的列空间受到影响，$C(R) \neq C(A)$，而行变换并不影响行空间，所以可以在$R$中看出前两行就是行空间的一组基。

所以，可以得出无论对于矩阵$A$还是$R$，其行空间的一组基，可以由$R$矩阵的前$r$行向量组成（这里的$R$就是第七讲提到的简化行阶梯形式）。

例2，对于左零空间，有$A^Ty=0 \rightarrow (A^Ty)^T=0^T\rightarrow y^TA=0^T$，因此得名。

采用Gauss-Jordan消元，将增广矩阵$\left[\begin{array}{c|c}A_{m \times n} & I_{m \times m}\end{array}\right]$中$A$的部分划为简化行阶梯形式$\left[\begin{array}{c|c}R_{m \times n} & E_{m \times m}\end{array}\right]$，此时矩阵$E$会将所有的行变换记录下来。

则$EA=R$，而在前几讲中，有当$A'$是$m$阶可逆方阵时，$R'$即是$I$，所以$E$就是$A^{-1}$。

本例中

$$
\left[\begin{array}{c|c}A_{m \times n} & I_{m \times m}\end{array}\right]=
\left[
\begin{array}
{c c c c|c c c}
1 & 2 & 3 & 1 & 1 & 0 & 0 \\
1 & 1 & 2 & 1 & 0 & 1 & 0 \\
1 & 2 & 3 & 1 & 0 & 0 & 1 \\
\end{array}
\right]
\underrightarrow{消元、化简}
\left[
\begin{array}
{c c c c|c c c}
1 & 0 & 1 & 1 & -1 & 2 & 0 \\
0 & 1 & 1 & 0 & 1 & -1 & 0 \\
0 & 0 & 0 & 0 & -1 & 0 & 1 \\
\end{array}
\right]
=\left[\begin{array}{c|c}R_{m \times n} & E_{m \times m}\end{array}\right]
$$

则

$$
EA=
\begin{bmatrix}
-1 & 2  & 0 \\
1  & -1 & 0 \\
-1 & 0  & 1 \\
\end{bmatrix}
\cdot
\begin{bmatrix}
1 & 2 & 3 & 1 \\
1 & 1 & 2 & 1 \\
1 & 2 & 3 & 1 \\
\end{bmatrix}
=
\begin{bmatrix}
1 & 0 & 1 & 1 \\
0 & 1 & 1 & 0 \\
0 & 0 & 0 & 0 \\
\end{bmatrix}
=R
$$


很明显，式中$E$的最后一行对$A$的行做线性组合后，得到$R$的最后一行，即$0$向量，也就是$y^TA=0^T$。

## A new vector space (M)
> The collection of all $3 × 3$ matrices forms a vector space; call it $M$.

We can add matrices and multiply them by scalars and there’s a zero matrix (additive identity). If we ignore the fact that we can multiply matrices by each other, they behave just like vectors.

Some subspaces of $M$ include:

* all upper triangular matrices (上三角矩阵)
* all symmetric matrices （对称矩阵）
* D, all diagonal matrices （对角矩阵）

D is the *intersection* of the first two spaces. Its dimension is 3; one basis for D is:


$$
\begin{bmatrix}
1 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 0 \\
\end{bmatrix}, \quad

\begin{bmatrix}
1 & 0 & 0 \\
0 & 3 & 0 \\
0 & 0 & 0 \\
\end{bmatrix}, \quad

\begin{bmatrix}
0 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 7 \\
\end{bmatrix}
$$

