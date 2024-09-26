# Eigenvalues and eigenvectors

1.对角化：存在一组基向量，经变换后还在自己的指向上 —> 特征向量；以基向量为单位变动的幅度是特征值（scalar）

2.为什么？计算简单、很多应用……

3.如何得到特征值、特征向量

### Content Notes

#### Definition (diagonalizable)

A linear operator $\mathsf{T}$ on a finite-dimensional vector space $\mathsf{V}$ is called **diagonalizable** if there is an ordered basis $\beta$ for $\mathsf{V}$ such that $[\mathsf{T}]_{\beta}$ is a diagonal matrix. A square matrix $A$ is called **diagonalizable** if $\mathsf{L}_A$ is diagonalizable.

#### Definition (eigenvector, eigenvalue)

Let $\mathsf{T}$ be a linear operator on a vector space $\mathsf{V}$. A nonzero vector $v\in\mathsf{V}$ is called an **eigenvector** of $\mathsf{T}$ if there exists a scalar $\lambda$ such that $\mathsf{T}(v)=\lambda v$. The scalar $\lambda$ is called the **eigenvalue** corresponding to the eigenvector $v$.

Let $A$ be in $\mathsf{M}_{n\times n}(F)$. A nonzero vector $v\in\mathsf{F}^n$ is called an **eigenvector** of $A$ if $v$ is an eigenvector of $\mathsf{L}_A$; that is, if $Av=\lambda v$ for some scalar $\lambda$. The scalar $\lambda$ is called the **eigenvalue** of $A$ corresponding to the eigenvector $v$.

#### Theorem 5.1

A linear operator $\mathsf{T}$ on a finite-dimensional vector space $\mathsf{V}$ is diagonalizable if and only if there exists an ordered basis $\beta$ for $\mathsf{V}$ consisting of eigenvectors of $\mathsf{T}$. Furthermore, if $\mathsf{T}$ is diagonalizable, $\beta=\{v_1,v_2,\dots,v_n\}$ is an ordered basis of eigenvectors of $\mathsf{T}$, and $D=[\mathsf{T}]_{\beta}$, then $D$ is a diagonal matrix and $D_{jj}$ is the eigenvalue corresponding to $v_j$ for $1\le j\le n$.

#### Theorem 5.2

Let $A\in\mathsf{M}_{n\times n}(F)$. Then a scalar $\lambda$ is an eigenvalue of $A$ if and only if $\det(A-\lambda I_n)=0$.

#### Definition (characteristic polynomial of a matrix)

Let $A\in\mathsf{M}_{n\times n}(F)$. The polynomial $f(t)=\det(A-tI_n)$ is called the **characteristic polynomial** of $A$.

#### Definition (characteristic polynomial of a linear transformation)

Let $\mathsf{T}$ be a linear operator on an $n$-dimensional vector space $\mathsf{V}$ with ordered basis $\beta$. We define the **characteristic polynomial** $f(t)$ of $\mathsf{T}$ to be the characteristic polynomial of $A=[\mathsf{T}]_{\beta}$. That is,
$$
f(t)=\det(A-tI_n).
$$

#### Theorem 5.3

Let $A\in\mathsf{M}_{n\times n}(F)$.

(a) The characteristic polynomial of $A$ is a polynomial of degree $n$ with leading coefficient $(-1)^n$.

(b) $A$ has at most $n$ distinct eigenvalues.

#### Theorem 5.4

Let $\mathsf{T}$ be a linear operator on a vector space $\mathsf{V}$, and let $\lambda$ be an eigenvalue of $\mathsf{T}$. A vector $v\in\mathsf{V}$ is an eigenvector of $\mathsf{T}$ corresponding to $\lambda$ if and only if $v\ne0$ and $v\in\mathsf{N(T-\lambda I)}$.

### Selected Exercises

#### 5

If $v\in\mathsf{V}$ is an eigenvector of $\mathsf{T}$ corresponding to $\lambda$, then $v\ne0$ by definition, and $\mathsf{T}v=\lambda v$, so $(\mathsf{T}-\lambda\mathsf{I})v=0$, thus $v\in\mathsf{N(T-\lambda I)}$. The other direction is obvious.

#### 6

Use Theorem 2.15, we know that $\mathsf{T}=\mathsf{L}_{[\mathsf{T}]_{\beta}}$, combine the definition of eigenvalue of linear transformation and eigenvalue of matrix, we get the result.

#### 7

(a) By Theorem 2.22 and 2.23, let $Q=[\mathsf{I_V}]_{\gamma}^{\beta}$, we have $Q$ invertible and $[\mathsf{T}]_{\gamma}=Q^{-1}[\mathsf{T}]_{\beta}Q$, which gives
$$
\det([\mathsf{T}]_{\gamma})=\det(Q^{-1}[\mathsf{T}]_{\beta}Q)=\det(Q^{-1})\det([\mathsf{T}]_{\beta})\det(Q)\\=\frac{1}{\det(Q)}\det([\mathsf{T}]_{\beta})\det(Q)=\det([\mathsf{T}]_{\beta})
$$
(b) $\mathsf{T}$ is invertible if and only if $[\mathsf{T}]_{\beta}$ is invertible, if and only if $\det([\mathsf{T}]_{\beta})\ne0$.

(c) Since $I=[\mathsf{I_V}]_{\beta}=[\mathsf{TT^{-1}}]_{\beta}=[\mathsf{T}]_{\beta}[\mathsf{T^{-1}}]_{\beta}$, we have
$$
1=\det(I)=\det(\mathsf{T})\det(\mathsf{T}^{-1})\implies\det(\mathsf{T}^{-1})=[\det(\mathsf{T})]^{-1}
$$
(d) By definition, $\det(\mathsf{TU})=\det([\mathsf{TU}]_{\beta})=\det([\mathsf{T}]_{\beta}[\mathsf{U}]_{\beta})=\det([\mathsf{T}]_{\beta})\det([\mathsf{U}]_{\beta})=\det(\mathsf{T})\det(\mathsf{U})$​.

(e) We have, by definition and Theorem 2.8, for any $\lambda\in F$ and any ordered basis $\beta$ for $\mathsf{V}$:
$$
\det(\mathsf{T-\lambda I_V})=\det([\mathsf{T-\lambda I_V}]_{\beta})=\det([\mathsf{T}]_{\beta}-\lambda[\mathsf{I_V}]_{\beta})=\det([\mathsf{T}]_{\beta}-\lambda I)
$$

#### 8

(a) Suppose $\mathsf{T}$ is invertible, assume zero is an eigenvalue of $\mathsf{T}$, then there exists $v\ne0$ such that $\mathsf{T}v=0v=0$, this means $\mathsf{T}$ is not one-to-one, a contradiction to $\mathsf{T}$ being invertible. Conversely, if zero is not an eigenvalue of $\mathsf{T}$, then no $v\ne0$ can make $\mathsf{T}v=0$, thus $\mathsf{N(T)}=\{0\}$ and $\mathsf{T}$ is invertible.

(b) Use (a) we know the eigenvalue of $\mathsf{T}$ is nonzero. Then $\lambda$ is an eigenvalue of $\mathsf{T}$ if and only if $\mathsf{T}v=\lambda v$ for $v\ne0$, this is equivalent to $\mathsf{T}^{-1}v=\lambda^{-1}v$ for $v\ne0$, this is true if and only if $\lambda^{-1}$ is an eigenvalue of $\mathsf{T}^{-1}$.

#### 9

We have
$$
A=\begin{pmatrix}A_{11}&A_{12}&\cdots&A_{1n}\\&A_{22}&\cdots&A_{2n}\\&&{\ddots}&{\vdots}\\&&&A_{nn}\end{pmatrix}\implies A-\lambda I_n=\begin{pmatrix}A_{11}-\lambda&A_{12}&\cdots&A_{1n}\\&A_{22}-\lambda&\cdots&A_{2n}\\&&{\ddots}&{\vdots}\\&&&A_{nn}-\lambda\end{pmatrix}
$$
thus $\det(A-\lambda I_n)=\prod_{i=1}^n(A_{ii}-\lambda)$, use Theorem 5.2 we get the result.

#### 10

(a) Write $\beta=\{\beta_1,\dots,\beta_n\}$, then $(\lambda\mathsf{I_V})(\beta_i)=\lambda\beta_i$ shows $[(\lambda\mathsf{I_V})(\beta_i)]_\beta=\lambda e_i$.

(b) $f(t)=(\lambda-t)^{\dim(\mathsf{V})}$.

(c) Since $\lambda I$ is a diagonal matrix, $\lambda\mathsf{I_V}$ is diagonalizable. The only eigenvalue of $\lambda\mathsf{I_V}$ is $\lambda$​.

#### 11

(a) $A$ is similar to $\lambda I$ means there exists invertible $Q$ such that $A=Q^{-1}(\lambda I)Q=\lambda Q^{-1}Q=\lambda I$.

(b) Suppose $A$ is a diagonalizable matrix, then $\mathsf{L}_A$ is diagonalizable, we suppose $A$ is $n\times n$ for some positive integer $n$, then by Theorem 5.1, there exists an ordered basis $\beta$ for $\mathsf{F}^n$ consisting of eigenvectors of $\mathsf{L}_A$. Since $A$ has only one eigenvalue, let it be $\lambda$, then $\mathsf{L}_A(\beta_i)=A\beta_i=\lambda\beta_i$ for $\beta_i\in\beta$, thus $[\mathsf{L}_A]_{\beta}=\lambda I$, this means $A$ is similar to $\lambda I$, then use (a).

(c) This matrix has only one eigenvalue $\lambda =1$​, if it is diagonalizable, then it must be a scalar matrix, but it is not.

#### 12

(a) Suppose $A,B\in\mathsf{M}_{n\times n}(F)$ are similar, then there is invertible $Q$ which makes $B=Q^{-1}AQ$, the characteristic polynomial of $A$ is $f(t)=\det(A-tI_n)$, the characteristic polynomial of $B$ is $g(t)=\det(B-tI_n)$​, we have
$$
g(t)=\det(Q^{-1}AQ-tQ^{-1}Q)=\det(Q^{-1})\det(A-tI_n)\det(Q)=\det(A-tI_n)=f(t)
$$
(b) Use Theorem 2.23, we know that for a linear operator, its matrices under different basis are similar, then (a) gives the conclusion.

#### 13

Figure 5.1 is
$$
\begin{aligned}
&\mathsf{V}\stackrel{\mathsf{T}}{\longrightarrow}\mathsf{V}
\\
\phi_{\beta}&\downarrow\qquad\downarrow\phi_{\beta}
\\
&\mathsf{F^n}\stackrel{\mathsf{L}_A}{\longrightarrow}\mathsf{F^n}
\end{aligned}
$$
(a) Since $A\phi_{\beta}(v)=\lambda\phi_{\beta}(v)=\mathsf{L}_A\phi_{\beta}(v)$, use Figure 5.1 we have $\mathsf{L}_A\phi_{\beta}(v)=\phi_{\beta}(\mathsf{T}(v))$, since $\phi_{\beta}$ is an isomorphism, we have
$$
\lambda\phi_{\beta}(v)=\phi_{\beta}(\lambda v)=\phi_{\beta}(\mathsf{T}(v))\implies\mathsf{T}(v)=\lambda v
$$
(b) That $y$ is an eigenvector of $A$ corresponding to $\lambda$ if and only if $Ay=\lambda y$, if and only if $A\phi_{\beta}(\phi_{\beta}^{-1}(y))=\lambda\phi_{\beta}(\phi_{\beta}^{-1}(y))$, use (a) we first get $\phi_{\beta}^{-1}(y)$ is an eigenvector of $\mathsf{T}$ corresponding to $\lambda$. Conversely, suppose we already have $\mathsf{T}(\phi_{\beta}^{-1}(y))=\lambda\phi_{\beta}^{-1}(y)$, then use the relation $\phi_{\beta}\mathsf{T}=\mathsf{L}_A\phi_{\beta}$, we have
$$
Ay=\mathsf{L}_A\phi_{\beta}(\phi_{\beta}^{-1}(y))=\phi_{\beta}\mathsf{T}(\phi_{\beta}^{-1}(y))=\phi_{\beta}(\lambda\phi_{\beta}^{-1}(y))=\lambda{y}
$$

#### 14

We have $\det(A-\lambda I_n)=\det(A-\lambda I_n)^t=\det(A^t-\lambda I_n)$ for all $\lambda\in F$, then use Theorem 5.2.

#### 15

(a) We have $\mathsf{T}(x)=\lambda x$ with $x\ne0$, thus
$$
\mathsf{T}^m(x)=\mathsf{T}^{m-1}(\mathsf{T}(x))=\mathsf{T}^{m-1}(\lambda x)=\lambda\mathsf{T}^{m-1}(x)=\cdots=\lambda^{m-1}\mathsf{T}(x)=\lambda^m{x}
$$
(b) If $A$ is a square matrix, and $x$ is an eigenvector of $A$ corresponding to eigenvalue $\lambda$, then $x$ is an eigenvector of $A^m$ corresponding to eigenvalue $\lambda^m$. The proof is ommited.

#### 16

Suppose $A,B\in\mathsf{M}_{n\times n}(F)$ are similar, then there is invertible $Q$ which makes $B=Q^{-1}AQ$, thus
$$
\text{tr}(B)=\text{tr}(Q^{-1}AQ)=\text{tr}(AQQ^{-1})=\text{tr}(A)
$$
Thus, let $\mathsf{T}$ be a linear operator on an $n$-dimensional vector space $\mathsf{V}$ with ordered basis $\beta$. the trace of $\mathsf{T}$ on $\mathsf{V}$ is defined to be the trace of the matrix $A=[\mathsf{T}]_{\beta}$.

#### 17

(a) If $\mathsf{T}(A)=\lambda{A}$, we have $A^t=\lambda A$, thus we have $A^t_{ij}=\lambda A_{ij}$ for all $i,j$, choose some $i,j$ such that $A_{ji}\ne0$, then
$$
A^t_{ij}=A_{ji}=\lambda A_{ij}=\lambda(\lambda A_{ji})\implies\lambda^2=1\implies\lambda=\pm1
$$
(b) All eigenvectors of $\lambda=1$ satisfy $A^t=A$, which is a symmetric matrix. All eigenvectors of $\lambda=-1$ satisfy $A^t=-A$​, which is a skew-symmetric matrix. 

(c) That $\beta$ can consist $\begin{pmatrix}1&0\\0&0\end{pmatrix}$, $\begin{pmatrix}0&0\\0&1\end{pmatrix}$, $\begin{pmatrix}0&1\\1&0\end{pmatrix}$ and $\begin{pmatrix}0&1\\-1&0\end{pmatrix}$.

(d) That $\beta$ can consist of a basis for all symmetric matrix, and a basis for all skew-symmetric matrix.

#### 18

(a) Since $B$ is invertible, we have $\det(B)\ne0$ and
$$
\det(A+cB)=\det(AB^{-1}+cI_n)\det(B)
$$
Let $f(c)=\det(AB^{-1}+cI_n)$, then $f(c)$ is a polynomial on $C$, thus $f(c)=0$ has at least one root, i.e, there exists $c\in C$ such that $f(c)=0$, which gives $\det(A+cB)=0$.

(b) Let $A=\begin{pmatrix}1&0\\0&1\end{pmatrix}$ and $B=\begin{pmatrix}i&-i\\i&-i\end{pmatrix}$, then $A+cB=\begin{pmatrix}1+ci&-ci\\ci&1-ci\end{pmatrix}$, we have $A$ is invertible and
$$
\det(A+cB)=(1+ci)(1-ci)-(-ci)(ci)=1-c^2i^2+c^2i^2=1\ne0
$$
thus $A+cB$ is invertible for all $c\in C$.

#### 19

Use Exercise 14 of Section 2.5.

#### 20

Since $f(t)=\det(A-tI_n)$, we see that $a_0=f(0)=\det(A)$. $A$ is invertible if and only if $\det(A)\ne0$.

#### 21

(a) Induction on $n$, when $n=1$, $A=(A_{11})$, and $f(t)=A_{11}-t$, the conclusion is valid, when $n=2$, we have $A=\begin{pmatrix}A_{11}&A_{12}\\A_{21}&A_{22}\end{pmatrix}$, and $f(t)=(A_{11}-t)(A_{22}-t)-A_{12}A_{21}$, since $q(t)=-A_{12}A_{21}$ is a polynomial of degree $0=2-2$, the conclusion is valid. Now suppose the conclusion is true for $n\le k-1$, consider $A$ being a $k\times k$ matrix, then
$$
f(t)=\det\begin{pmatrix}A_{11}-t&A_{12}&\cdots&A_{1k}
\\
A_{21}&A_{22}-t&\cdots&A_{2k}
\\
{\vdots}&{\vdots}&&{\vdots}
\\
A_{k1}&A_{k2}&\cdots&A_{kk}-t
\end{pmatrix}\\=(A_{11}-t)\det\begin{pmatrix}
A_{22}-t&\cdots&A_{2k}
\\
{\vdots}&&{\vdots}
\\
A_{k2}&\cdots&A_{kk}-t
\end{pmatrix}+\sum_{i=2}^kA_{1i}\tilde{A}_{1i}
$$
by expanding $f(t)$ with the first row, use the induction hypothesis, we have
$$
(A_{11}-t)\det\begin{pmatrix}
A_{22}-t&\cdots&A_{2k}
\\
{\vdots}&&{\vdots}
\\
A_{k2}&\cdots&A_{kk}-t
\end{pmatrix}=(A_{11}-t)[(A_{22}-t)\cdots(A_{kk}-t)+q(t)]
$$
with $\deg(q)\le k-3$. Also notice that $\deg(\tilde{A}_{1i})\le k-2$ for $i=2,\dots,k$, thus the polynomial
$$
(A_{11}-t)q(t)+\sum_{i=2}^kA_{1i}\tilde{A}_{1i}
$$
has degree at most $k-2$. Thus the conclusion remains valid for $n=k$.

(b) Compare different forms of $f(t)$, we see that the coefficient of $t^{n-1}$ is $(-1)^{n-1}\sum_{i=1}^nA_{ii}$.

#### 22

(a) Since $\mathsf{T}(x)=\lambda x$, then $\mathsf{T}^k(x)=\lambda^kx$ for all $k$. if we suppose $g(t)=a_nt^n+a_{n-1}t^{n-1}+\cdots+a_1t+a_0$, then
$$
\begin{aligned}
g(\mathsf{T})(x)&=(a_n\mathsf{T}^n+a_{n-1}\mathsf{T}^{n-1}+\cdots+a_1\mathsf{T}+a_0I)(x)
\\&=a_n\mathsf{T}^n(x)+a_{n-1}\mathsf{T}^{n-1}(x)+\cdots+a_1\mathsf{T}(x)+a_0x
\\&=a_n\lambda^nx+a_{n-1}\lambda^{n-1}x+\cdots+a_1\lambda x+a_0x
\\&=(a_n\lambda^n+a_{n-1}\lambda^{n-1}+\cdots+a_1\lambda+a_0)x
\\&=g(\lambda)x
\end{aligned}
$$
(b) If $x$ is an eigenvector of $A$ with eigenvalue $\lambda$ and $g(t)\in\mathsf{P(F)}$, then $g(A)(x)=g(\lambda)x$.

#### 23

By Theorem 5.1, $\mathsf{T}$ is diagonalizable means there exists an ordered basis $\beta=\{v_1,v_2,\dots,v_n\}$ for $\mathsf{V}$ consisting of eigenvectors of $\mathsf{T}$. Let $\lambda_1,\dots,\lambda_n$ be eigenvalues corresponding to $v_1,v_2,\dots,v_n$ respectively, then $f(\lambda_i)=0$. Exercise 22(a) shows that $f(\mathsf{T})(v_i)=f(\lambda_i)v_i=0$ for $i=1,\dots,n$, thus $f(\mathsf{T})=\mathsf{T}_0$, the zero operator.

#### 24

Use Exercise 21(a), we know that $f(t)$ has the form $(A_{11}-t)(A_{22}-t)\cdots(A_{nn}-t)+q(t)$, thus the leading coefficient of $f(t)$ is the coefficient of $t^n$, which is $(-1)^n$, and $f(t)$ has at most $n$ distinct zeros by Corollary 2 of Appendix E, thus $A$ has at most $n$ distinct eigenvalues.

#### 26

Any element in $\mathsf{M}_{2\times2}(Z_2)$ can be written as $A=\begin{pmatrix}a&b\\ c&d\end{pmatrix}$ where $a,b,c,d$ is $0$ or $1$, thus a characteristic polynomial is
$$
f(t)=\det(A-tI_2)=(a-t)(d-t)-bc=t^2-(a+d)t+ad-bc
$$
Now in $Z_2$, the number $-(a+d)$ and $ad-bc$ has only two possible choices: $0$ or $1$. Thus there are 4 characteristic polynomials in $\mathsf{M}_{2\times2}(Z_2)$, namely: $t^2,t^2+t,t^2+1$ and $t^2+t+1$.

### Summary

一个线性变换diagonalizable的定义是有一组有序基下的矩阵是对角阵。为了更好描述此定义，引入特征值和特征向量的定义。定理5.1将这两个定义关联起来，对角化的充要条件是存在一组特征向量基。因此对角化的问题转化为求特征值和特征向量的问题。如何求？定理5.2先论述矩阵确定特征值的条件，并引入特征多项式这一新的定义，矩阵特征多项式通过行列式计算得到，线性变换的特征多项式是其任意表示矩阵的特征多项式。定理5.3描述了特征多项式的性质，以及由多项式得到的特征值个数上限。定理5.4说明特征值、特征向量与一个特定核空间的关系。