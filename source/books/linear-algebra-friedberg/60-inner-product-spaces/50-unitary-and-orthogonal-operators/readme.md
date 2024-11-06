# Unitary and Orthogonal Operators and Their Matrices

We want to study linear operators on an inner product space that preserve length, we will see this condition guarantees the preserving of inner product.

### Content Notes

#### Definitions

Let $\mathsf{T}$ be a linear operator on a finite-dimensional inner product space $\mathsf{V}$ (over $F$). If $\|\mathsf{T}(x)\|=\|x\|$ for all $x\in\mathsf{V}$, we call $\mathsf{T}$ a **unitary operator** if $F=C$ and an **orthogonal operator** if $F=R$.

In the infinite-dimensional case, an operator satisfying the preceding norm requirement is generally called an **isometry**. If, in addition, the operator is onto (the condition guarantees one-to-one), then the operator is called a **unitary** or **orthogonal operator**.

#### Theorem 6.18

Let $\mathsf{T}$ be a linear operator on a finite-dimensional inner product space $\mathsf{V}$. Then the following statements are equivalent.

(a) $\mathsf{TT}^*=\mathsf{T}^*\mathsf{T}=\mathsf{I}$.

(b) $\lang\mathsf{T}(x),\mathsf{T}(y)\rang=\lang{x,y}\rang$ for all $x,y\in\mathsf{V}$.

(c) If $\beta$ is an orthonormal basis for $\mathsf{V}$, then $\mathsf{T}(\beta)$ is an orthonormal basis for $\mathsf{V}$.

(d) There exists an orthonormal basis $\beta$ for $\mathsf{V}$ such that $\mathsf{T}(\beta)$ is an orthnormal basis for $\mathsf{V}$.

(e) $\|\mathsf{T}(x)\|=\|x\|$ for all $x\in\mathsf{V}$.

#### Lemma

Let $\mathsf{U}$ be a self-adjoint operator on a finite-dimensional inner product space $\mathsf{V}$. If $\lang{x,\mathsf{U}(x)}\rang$ for  all $x\in\mathsf{V}$, then $\mathsf{U}=\mathsf{T}_0$.

##### Corollary 1

Let $\mathsf{T}$ be a linear operator on a finite-dimensional real inner product space $\mathsf{V}$. Then $\mathsf{V}$ has an orthonormal basis of eigenvectors of $\mathsf{T}$ with corresponding eigenvalues of absolute value $1$ if and only if $\mathsf{T}$ is both self-adjoint and orthogonal.

##### Corollary 2

Let $\mathsf{T}$ be a linear operator on a finite-dimensional complex inner product space $\mathsf{V}$. Then $\mathsf{V}$ has an orthonormal basis of eigenvectors of $\mathsf{T}$ with corresponding eigenvalues of absolute value $1$ if and only if $\mathsf{T}$ is unitary.

#### Definitions

A square matrix $A$ is called an **orthogonal matrix** if $A^tA=AA^t=I$ and **unitary** if $A^*A=AA^*=I$.

The condition $AA^*=I$ is equivalent to the statement that the rows of $A$ form an orthonormal basis for $\mathsf{F}^n$; The condition $A^*A=I$ is equivalent to the statement that the columns of $A$ form an orthonormal basis for $\mathsf{F}^n$.

For a complex normal [real symmetric] matrix $A$, there exists an orthonormal basis $\beta$ for $\mathsf{F}^n$ consisting of eigenvectors of $A$. Hence $A$ is similar to a diagonal matrix $D$, the matrix $Q$ whose columns are the vectors in $\beta$ is such that $D=Q^{-1}AQ$, thus are orthonormal basis for $\mathsf{F}^n$, which means $Q$ is unitary [orthogonal]. In this case, we say that $A$ is **unitarily equivalent** [**orthogonally equivalent**] to $D$.

More generally, *$A$ and $B$ are unitarily equivalent [orthogonally equivalent] if and only if there exists a unitary [orthogonal] matrix $P$ such that* $A=P^*BP$.

#### Theorem 6.19

Let $A$ be a complex $n\times n$ matrix. Then $A$ is normal if and only if $A$ is unitarily equivalent to a diagonal matrix.

#### Theorem 6.20

Let $A$ be a real $n\times n$ matrix. Then $A$ is symmetric if and only if $A$ is orthogonally equivalent to a real diagonal matrix.

#### Theorem 6.21 (Schur)

Let $A\in\mathsf{M}_{n\times n}(\mathsf{F})$ be a matrix whose characteristic polynomial splits over $F$.

(a) If $F=C$, then $A$ is unitarily equivalent to a complex upper triangular matrix.

(b) If $F=R$, then $A$ is orthogonally equivalent to a real upper triangular matrix.

### Selected Exercises

#### 3

Let $\mathsf{T},\mathsf{U}$ be unitary [orthogonal] operators, then
$$
\|\mathsf{TU}(x)\|=\|\mathsf{U}(x)\|=\|x\|,\quad\forall x\in\mathsf{V}
$$
this means $\mathsf{TU}$ is unitary [orthogonal].

#### 6

Suppose $\mathsf{T}$ is unitary, then
$$
\|\mathsf{T}(f)\|^2=\int_0^1|f(t)|^2|h(t)|^2dt=\|f\|^2=\int_0^1|f(t)|^2dt,\quad\forall f\in\C[0,1]
$$
thus let $f(t)=h(t)-1$, we have
$$
\int_0^1[|h(t)|^2-1]^2dt=0\implies|h(t)|^2=1,\forall0\le t\le1
$$
Conversely, it is easy to see that $\|\mathsf{T}(f)\|^2=\|f\|^2$, thus $\|\mathsf{T}(f)\|=\|f\|$.

#### 7

Use Corollary 2 of Theorem 6.18, if $\mathsf{T}$ is unitary, then we can find an orthonormal basis $\beta=\{v_1,\dots,v_n\}$ of $\mathsf{V}$ consisting of eigenvectors of $\mathsf{T}$, with corresponding eigenvalues $\lambda_i$ and $|\lambda_i|=1$ for $i=1,\dots,n$. Let $\mathsf{U}$ be defined with
$$
\mathsf{U}(v_i)=\lambda_i^{1/2}v_i,\quad i=1,\dots,n
$$
Then $\mathsf{U}^2(v_i)=\lambda_iv_i=\mathsf{T}(v_i)$, thus $\mathsf{U}^2=\mathsf{T}$. To prove $\mathsf{U}$ is unitary, notice that $\lambda_i^{1/2}$ are eigenvalues of $\mathsf{U}$ and
$$
|\lambda_i^{1/2}|^2=|\lambda_i|=1\implies|\lambda_i^{1/2}|=1
$$
Then again use Corollary 2 of Theorem 6.18.

#### 8

Exercise 10 of Section 6.4 shows that if $\mathsf{T}$ is self-adjoint, then
$$
\|\mathsf{T}(x)\pm ix\|^2=\|\mathsf{T}(x)\|^2+\|x\|^2\implies\|\mathsf{T}(x)+ ix\|=\|\mathsf{T}(x)- ix\|
$$
then
$$
\|(\mathsf{T}+i\mathsf{I})(\mathsf{T}-i\mathsf{I})^{-1}(x)\|=\|(\mathsf{T}-i\mathsf{I})(\mathsf{T}-i\mathsf{I})^{-1}(x)\|=\|x\|
$$

#### 9

No. Suppose $\dim(\mathsf{V})=2$ and there is an orthonormal basis $\beta=\{v_1,v_2\}$ of $\mathsf{V}$, and $\mathsf{U}$ is defined with
$$
\mathsf{U}(v_1)=\mathsf{U}(v_2)=v_1
$$
then $\mathsf{U}$ is a linear operator, but not unitary, since $\|\mathsf{U}(v_1+v_2)\|=2$ and $\|v_1+v_2\|=\sqrt{2}$.

#### 10

By Theorem 6.19 and 6.20, $A$ is unitary/orthogonal equivalent to a diagonal matrix $D$, whose diagonal entries consists of eigenvalues of $A$. Write $A=P^*DP$, where $P$ is unitary/orthogonal and
$$
D=\begin{bmatrix}\lambda_1&&
\\
&\ddots&
\\
&&\lambda_n
\end{bmatrix}
$$
Then we have $A^*=P^*D^*P$ and so
$$
\text{tr}(A)=\text{tr}(P^*DP)=\text{tr}(DPP^*)=\text{tr}(D)=\sum_{i=1}^n\lambda_i
\\
\text{tr}(A^*A)=\text{tr}(P^*D^*PP^*DP)=\text{tr}(P^*D^*DP)=\text{tr}(D^*D)=\sum_{i=1}^n|\lambda_i|^2
$$

#### 12

Refer to symbol of Exercise 10, we have
$$
\det(A)=\det(P^*)\det(D)\det(P)=\det(P^{-1})\det(D)\det(P)=\det(D)=\prod_{i=1}^n\lambda_i
$$

#### 14

Suppose $A=P^*BP$ for some unitary matrix $B$, then $A$ is positive definite means $\lang{Ax,x}\rang>0$ for all $x\ne0$, thus $\lang{P^*BPx,x}\rang>0$ for all $x\ne0$, this means $\lang{BPx,Px\rang}>0$ for all $x\ne0$, since $P$ is invertible, the range of $Px$ is $\mathsf{F}^n$, thus $B$ is also positive definite. Interchange the row of $A$ and $B$ we see that the converse is also true. The case of semidefinite can be similarly proved.

#### 15

(a) That $\mathsf{W}$ is $\mathsf{U}$-invariant means $\mathsf{U}(\mathsf{W})\subseteq\mathsf{W}$, let $\beta=\{w_1,\dots,w_k\}$ be an orthonormal basis for $\mathsf{W}$, by Theorem 6.18(c), we have $\mathsf{U}(\beta)$ an orthonormal basis for $\mathsf{W}$, this means $\mathsf{W}\subseteq\mathsf{U}(\mathsf{W})$.

(b) Let $v\in\mathsf{W}^{\perp}$, for any $w\in\mathsf{W}$, there exists $w'\in\mathsf{W}$ such that $w=\mathsf{U}(w')$, by Theorem 6.18(b), we have
$$
\lang{\mathsf{U}(v),w}\rang=\lang{\mathsf{U}(v),\mathsf{U}(w')}\rang=\lang{v,w'}\rang=0\implies\mathsf{U}(v)\in\mathsf{W}^{\perp}
$$

#### 17

Let $A$ be a unitary matrix which is upper triangular, say
$$
A=\begin{bmatrix}
a_{11}&a_{12}&\cdots&a_{1n}
\\
0&a_{22}&\cdots&a_{2n}
\\
&&\ddots&
\\
0&0&\cdots&a_{nn}
\end{bmatrix}=[\alpha_1&\cdots&\alpha_n]
$$
Then $\alpha_1,\dots,\alpha_n$ form an orthonormal basis for $\mathsf{F}^n$, we can immediately get $|a_{11}|=1$, and $\lang\alpha_1,\alpha_j\rang=0$ for $j=2,\dots,n$ gives $a_{12}=\cdots=a_{1n}=0$, now $\alpha_2$ reduces to the column vector $[0,a_{22},0,\dots,0]^{\mathsf{T}}$, thus we get $|a_{22}|=1$ and $\lang\alpha_2,\alpha_j\rang=0$ for $j=3,\dots,n$ gives $a_{23}=\cdots=a_{1n}=0$, continue this process, we have $a_{ij}=0$ for $i<j$, and so $A$ is diagonal.

#### 19

For any $x,y\in\mathsf{V}$, then we can write $x=v_1+v_2$ and $y=v_1'+v_2'$, where $v_1,v_1'\in\mathsf{W}$ and $v_2,v_2'\in\mathsf{W}^{\perp}$, notice that
$$
\lang\mathsf{U}(x),y\rang=\lang v_1-v_2,v_1'+v_2'\rang=\lang{v_1,v_1'}\rang-\lang{v_2,v_2'}\rang
\\
\lang\mathsf{U}^*(x),y\rang=\lang{x,\mathsf{U}(y)\rang}=\lang v_1+v_2,v_1'-v_2'\rang=\lang{v_1,v_1'}\rang-\lang{v_2,v_2'}\rang
$$
so we conclude $\lang\mathsf{U}(x),y\rang=\lang\mathsf{U}^*(x),y\rang$, or $\lang(\mathsf{U}-\mathsf{U}^*)(x),y\rang=0$ for any $x,y\in\mathsf{V}$, let $y=(\mathsf{U}-\mathsf{U}^*)(x)$ we see that $(\mathsf{U}-\mathsf{U}^*)(x)=0$ for all $x\in\mathsf{V}$, so $\mathsf{U}=\mathsf{U}^*$ and $\mathsf{U}$ is self-adjoint. To show $\mathsf{U}$ is unitary, notice that
$$
\|\mathsf{U}(x)\|^2=\lang{v_1-v_2,v_1-v_2}\rang=\|v_1\|^2+\|v_2\|^2=\|x\|^2
$$

#### 21

(a) Let $P$ be the unitary matrix such that $A=P^*BP$, then $A^*=P^*B^*P$ and then
$$
\text{tr}(A^*A)=\text{tr}(P^*B^*PP^*BP)=\text{tr}(P^*B^*BP)=\text{tr}(B^*BPP^*)=\text{tr}(B^*B)
$$
(b) We have
$$
\text{tr}(A^*A)=\sum_{i=1}^n(A^*A)_{ii}=\sum_{i=1}^n\sum_{j=1}^n(A^*)_{ij}A_{ji}=\sum_{i,j=1}^n|A_{ij}|^2
$$
similarly $\text{tr}(B^*B)=\sum_{i,j=1}^n|B_{ij}|^2$, then use (a).

(c) Compute the squared norm sum of the two matrices and see they are not equal.

### Summary

本节在前述章节的基础上进一步讨论unitary/orthogonal线性变换，之前对线性变换的限制是要求其为normal的，即$TT^*=T^*T$，如果再进一步限制$TT^*=T^*T=I$，这些线性变换能够有“保留模长”的性质，此外如果在有限维复空间上，这样的线性变换是特征值绝对值全为1的normal变换。为何要关注保留模长的性质？之前习题中有揭示过模长和内积的相互决定关系，我们可以证明保留模长的线性变换就能保证内积在此线性变换下不变。

本节先定义unitary/orthogonal线性变换是什么：具有保留模长性质的线性变换在C/R下分别称为unitary/orthogonal线性变换。定理6.18给出一系列共5个与前述定义等价的条件，实质是提供unitary/orthonomal能够推导出的性质。这个定理的推论1加强了上一节在实空间上的schur定理，Schur定理保证了self-adjoint线性变换和一组该线性变换特征向量基（可对角化）的等价关系，推论1增加了线性变换orthogonal和特征向量基对应特征值长度全为1的等价关系。推论2可以看作推论1在复空间上的版本。

本节接下来的内容将研究对象从线性变换改为矩阵，首先定义unitary/orthogonal矩阵是什么，以及什么是两个矩阵的unitary/orthogonal等价，这个等价关系（可以证明是确一个“等价”关系）是刻画unitary/orthogonal矩阵性质的基础。定理6.19和6.20所说的就是unitary/orthogonal矩阵有用的地方：他们会unitary/orthogonal等价于对角矩阵。定理6.21是矩阵版本的Schur定理。
