# The Rank of a Matrix and Matrix Inverses

### Content Notes

#### Definition (rank of matrix)

If $A\in\mathsf{M}_{m\times n}(F)$, we define the **rank** of $A$, denoted rank$(A)$, to be the rank of the linear transformation $\mathsf{L}_A:\mathsf{F}^n\to\mathsf{F}^m$.

#### Theorem 3.3

Let $\mathsf{T:V\to W}$ be a linear transformation between finite-dimensional vector spaces, and let $\beta$ and $\gamma$ be ordered bases for $\mathsf{V}$ and $\mathsf{W}$, respectively. Then rank$(\mathsf{T})=$rank$([\mathsf{T}]_{\beta}^{\gamma})$​.

#### Theorem 3.4

Let $A$ be an $m\times n$ matrix. If $P$ and $Q$ are invertible $m\times m$ and $n\times n$ matrices, respectively, then

(a) $\text{rank}(AQ)=\text{rank}(A)$,

(b) $\text{rank}(PA)=\text{rank}(A)$,

(c) $\text{rank}(PAQ)=\text{rank}(A)$.

##### Corollary

Elementary row and column operations on a matrix are rank-preserving.

#### Theorem 3.5

The rank of any matrix equals the maximum number of its linearly independent columns; that is, the rank of a matrix is the dimension of the subspace generated by its columns.

#### Theorem 3.6

Let $A$ be an $m\times n$ matrix of rank $r$. Then $r\le m,r\le n$, and by means of a finite number of elementary row and column operations, $A$ can be transformed into the matrix
$$
D=\begin{pmatrix}I_r&O_1\\O_2&O_3\end{pmatrix}
$$
where $O_1,O_2,O_3$ are zero matrices. Thus $D_{ii}=1$ for $i\le r$ and $D_{ij}=0$ otherwise.

##### Corollary 1

Let $A$ be an $m\times n$ matrix of rank $r$. Then there exist invertible matrices $B$ and $C$ of sizes $m\times n$ and $n\times n$, respectively, such that $D=BAC$​, where
$$
D=\begin{pmatrix}I_r&O_1\\O_2&O_3\end{pmatrix}
$$
is the $m\times n$ matrix in which $O_1,O_2,O_3$ are zero matrices.

##### Corollary 2

Let $A$ be an $m\times n$ matrix. Then

(a) $\text{rank}(A^t)=\text{rank}(A)$​.

(b) The rank of any matrix equals the maximum number of its linearly independent rows; that is, the rank of a matrix is the dimension of the subspace generated by its rows.

(c) The rows and columns of any matrix generate subspaces of the same dimension, numerically equal to the rank of the matrix.

##### Corollary 3

Every invertible matrix is a product of elementary matrices.

#### Theorem 3.7

Let $\mathsf{T:V\to W}$ and $\mathsf{U:W\to Z}$ be linear transformations on finite-dimensional vector spaces $\mathsf{V,W,Z}$, and let $A$ and $B$ be matrices such that the product $AB$ is defined. Then

(a) $\text{rank}(\mathsf{UT})\le\text{rank}(\mathsf{U})$.

(b) $\text{rank}(\mathsf{UT})\le\text{rank}(\mathsf{T})$.

(c) $\text{rank}(AB)\le\text{rank}(A)$​.

(d) $\text{rank}(AB)\le\text{rank}(B)$.

#### Definition (augmented matrix)

Let $A$ and $B$ be $m\times n$ and $m\times p$ matrices, respectively. By the **augmented matrix** $(A|B)$ we mean the $m\times(n+p)$ matrix $(A\text{ }B)$, that is, the matrix whose first $n$ columns are the columns of $A$, and whose last $p$ columns are the columns of $B$.

### Selected Exercises

#### 8

Let $Q_i$ denote the particular elementary matrix that multiply the $i$th row by $c$, then each $Q_i$ is invertible and
$$
cA=Q_1Q_2\cdots Q_mA
$$
and the result follows from a repeatedly use of Theorem 3.4(b).

#### 10

If $A$ is a zero $m\times 1$ matrix, then there is no need to prove. Suppose $A\ne O$, then suppose some $A_{i1}\ne0$, interchange it to the first row, multiply it by $1/A_{i1}$, then use it to make row 2-row $m$ all $0$, each step corresponding to an elementary matrix $B_j$, there are at most $m+1$ such $B_j$, let $B$ be the product of $B_j$ and $C=I_1$, we have
$$
BAC=\begin{pmatrix}1\\0\\{\vdots}\\0\end{pmatrix}
$$

#### 13

To prove (b), use Theorem 3.5 and (a). To prove (c), use use Theorem 3.5 and (a), (b).

#### 14

(a) Let $w\in\mathsf{R(T+U)}$, then there exists $v\in\mathsf{V}$ such that $w=(\mathsf{T+U})(v)=\mathsf{T}(v)+\mathsf{U}(v)$, this means $w\in\mathsf{R(T)}+\mathsf{R(U)}$.

(b) From (a) we have
$$
\dim(\mathsf{R(T+U)})\le\dim(\mathsf{R(T)}+\mathsf{R(U)})\le\dim(\mathsf{R(T)})+\dim(\mathsf{R(U)})
$$
(c) There exists linear transformation $\mathsf{T,U}$ such that $A=[\mathsf{T}]_{\beta}^{\gamma}$ and $B=[\mathsf{U}_{\beta}^{\gamma}]$ for suitable bases $\beta$ and $\gamma$, then the result follows from (b) and the fact that $[\mathsf{T+U}]_{\beta}^{\gamma}=[\mathsf{T}]_{\beta}^{\gamma}+[\mathsf{U}]_{\beta}^{\gamma}$.

#### 16

Let $\mathsf{V}_0=\mathsf{R}(\mathsf{L}_A)$, then $\text{rank}(A)=\dim(\mathsf{V}_0)$. Exercise 17 of Section 2.4 says for $\mathsf{T}=\mathsf{L}_P$, which is an isomorphism since $P$ is invertible, we can have $\dim(\mathsf{V}_0)=\dim(\mathsf{T(V_0)})$, and it is easy to see 
$$
\mathsf{T(V_0)}=\mathsf{L}_P(\mathsf{V}_0)=\mathsf{L}_P\mathsf{L}_A(\mathsf{F}^n)=\mathsf{L}_{PA}(\mathsf{F}^n)=\mathsf{R}(\mathsf{L}_{PA})
$$

which means $\dim(\mathsf{T(V_0)})=\text{rank}(\mathsf{L}_{PA})=\text{rank}(PA)$.

#### 17

We have $\text{rank}(B)=\text{rank}(C)=1$, thus $\text{rank}(BC)\le\text{rank}(B)=1$. If $A$ is a $3\times3$ matrix having rank $1$, then the rows of $A$ has dimension $1$, thus if we let $\alpha=(A_{11},A_{12},A_{13})$, then we can find scalars $c_2,c_3$ such that
$$
(A_{21},A_{22},A_{23})=c_2\alpha,\quad(A_{31},A_{32},A_{33})=c_3\alpha
$$
so we have
$$
A=\begin{pmatrix}1\\c_2\\c_3\end{pmatrix}\alpha=\begin{pmatrix}1\\c_2\\c_3\end{pmatrix}(A_{11},A_{12},A_{13})\implies B=\begin{pmatrix}1\\c_2\\c_3\end{pmatrix},C=(A_{11},A_{12},A_{13})
$$

#### 18

Write $A=(A_{ij})$ and $B=(B_{ij})$, then the $i$th row and the $j$th column of $AB$ is $\sum_{k=1}^nA_{ik}B_{kj}$, take the $k$th element of this sum for $1\le i\le m,1\le j\le p$ to form a matrix $C_k$, which is a $m\times p$ matrix, from the construction we can have $AB=\sum_{k=1}^nC_k$, to see that each $C_k$ has rank $1$, notice that
$$
C_k=\begin{pmatrix}A_{1k}B_{k1}&\cdots&A_{1k}B_{kp}
\\{\cdots}&&{\cdots}
\\A_{mk}B_{k1}&\cdots&A_{mk}B_{kp}
\end{pmatrix}=\begin{pmatrix}A_{1k}\\{\vdots}\\A_{mk}\end{pmatrix}\begin{pmatrix}B_{k1}&\cdots&B_{kp}\end{pmatrix}
$$
Thus $\text{rank}(C_k)\le\text{rank}\begin{pmatrix}B_{k1}&\cdots&B_{kp}\end{pmatrix}\le1$.

#### 19

We have $m\le n$ and $n\le p$, since $\text{rank}(A)=m$, we can perform elementary row operations, i.e. find an invertible $m\times m$ elementary matrix $E$ such that
$$
EA=\begin{pmatrix}I_m&A'_{m\times(n-m)}\end{pmatrix}
$$
since $\text{rank}(B)=n$, we can perform elementary column operations, i.e. find an invertible $p\times p$ elementary matrix $E'$ such that
$$
BE'=\begin{pmatrix}I_n&O_{n\times(p-n)}\end{pmatrix}
$$
thus
$$
EABE'=\begin{pmatrix}I_m&A'_{m\times(n-m)}\end{pmatrix}\begin{pmatrix}I_n&O_{n\times(p-n)}\end{pmatrix}=\begin{pmatrix}I_m&A'_{m\times(n-m)}&O_{n\times(p-n)}\end{pmatrix}
$$
which means $\text{rank}(EABE')=m$, now use Theorem 3.4(c) to get $\text{rank}(AB)=m$.


#### 21

Since $m\le n$, we can perform elementary column operations, i.e. find an invertible $n\times n$ elementary matrix $E$​ such that
$$
AE=\begin{pmatrix}I_m&O_{m\times(n-m)}\end{pmatrix}\implies AE\begin{pmatrix}I_m\\O_{(n-m)\times m}\end{pmatrix}=I_m
$$
thus we can let $B=E\begin{pmatrix}I_m\\O_{(n-m)\times m}\end{pmatrix}$.

#### 22

Since $m\le n$, we can perform elementary row operations, i.e. find an invertible $n\times n$ elementary matrix $E$​ such that
$$
EB=\begin{pmatrix}I_m\\O_{(n-m)\times m}\end{pmatrix}\implies\begin{pmatrix}I_m&O_{m\times(n-m)}\end{pmatrix}EB=I_m
$$
thus we can let $A=\begin{pmatrix}I_m&O_{m\times(n-m)}\end{pmatrix}E$.

#### Summary

本节为矩阵的秩和矩阵的逆。一些重要的结论为：左乘/右乘可逆矩阵不改变原矩阵的秩，矩阵的秩就是对应线性变换的秩，也即线性变换range空间的dimension；复合线性变换的秩（矩阵相乘的秩）不大于任一个线性变换的秩（乘数矩阵的秩）；矩阵的行列秩相等。