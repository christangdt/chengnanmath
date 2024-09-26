# Determinants of Order n

### Content Notes

#### Definitions

Let $A\in\mathsf{M}_{n\times n}(F)$. If $n=1$, so that $A=(A_{11})$, we define $\det(A)=A_{11}$. For $n\ge2$, we define $\det(A)$ recursively as
$$
\det(A)=\sum_{j=1}^n(-1)^{i+j}A_{1j}\cdot\det(\tilde{A}_{1j})
$$
The scalar $\det(A)$ is called the **determinant** of $A$ and is also denoted by $|A|$. The scalar $(-1)^{i+j}\det(\tilde{A}_{ij})$ is called the **cofactor** of the entry of $A$ in row $i$, column $j$​.

#### Theorem 4.3

The determinant of an $n\times n$ matrix is a linear function of each row when the remaining rows are held fixed. That is, for $1\le r\le n$, we have
$$
\det\begin{pmatrix}a_1\\{\vdots}\\a_{r-1}\\u+kv\\a_{r+1}\\{\vdots}\\a_n\end{pmatrix}=\det\begin{pmatrix}a_1\\{\vdots}\\a_{r-1}\\u\\a_{r+1}\\{\vdots}\\a_n\end{pmatrix}+k\det\begin{pmatrix}a_1\\{\vdots}\\a_{r-1}\\v\\a_{r+1}\\{\vdots}\\a_n\end{pmatrix}
$$
whenever $k$ is a scalar and $u,v$ and each $a_i$ are row vectors in $\mathsf{F}^n$.

##### Corollary

If $A\in\mathsf{M}_{n\times n}(F)$ has a row consisting entirely of zeros, then $\det(A)=0$.

#### Lemma

Let $B\in\mathsf{M}_{n\times n}(F)$, where $n\ge2$. If row $i$ of $B$ equals $e_k$ for some $k(1\le k\le n)$, then $\det(B)=(-1)^{i+k}\det(\tilde{B}_{ik})$​.

#### Theorem 4.4

The determinant of a square matrix can be evaluated by cofactor expansion along any row. That is, if $A\in\mathsf{M}_{n\times n}(F)$, then for any integer $i(1\le i\le n)$, 
$$
\det(A)=\sum_{j=1}^n(-1)^{i+j}A_{ij}\cdot\det(\tilde{A}_{ij})
$$

##### Corollary

If $A\in\mathsf{M}_{n\times n}(F)$ has two identical rows, then $\det(A)=0$​.

#### Theorem 4.5

If $A\in\mathsf{M}_{n\times n}(F)$ and $B$ is a matrix obtained from $A$ by interchanging any two rows of $A$, then $\det(B)=-\det(A)$.

#### Theorem 4.6

Let $A\in\mathsf{M}_{n\times n}(F)$, and let $B$ be a matrix obtained by adding a multiple of one row of $A$ to another row of $A$. Then $\det(B)=\det(A)$​.

##### Corollary

If $A\in\mathsf{M}_{n\times n}(F)$ has rank less than $n$, then $\det(A)=0$.

### Selected Exercises

#### 24

Suppose row $r$ of $A$ is entirely zero, then we have
$$
\det(A)=\det\begin{pmatrix}a_1\\{\vdots}\\a_{r-1}\\0\\a_{r+1}\\{\vdots}\\a_n\end{pmatrix}=\det\begin{pmatrix}a_1\\{\vdots}\\a_{r-1}\\0+(-1)\cdot0\\a_{r+1}\\{\vdots}\\a_n\end{pmatrix}=\det\begin{pmatrix}a_1\\{\vdots}\\a_{r-1}\\0\\a_{r+1}\\{\vdots}\\a_n\end{pmatrix}+(-1)\det\begin{pmatrix}a_1\\{\vdots}\\a_{r-1}\\0\\a_{r+1}\\{\vdots}\\a_n\end{pmatrix}=0
$$

#### 25

If $k=0$, then $kA=O$ and one row of $kA$ is entirely zero, thus $\det(kA)=0$, and $k^n\det(A)=0^n\det(A)=0$.

If $k\ne0$, then $kA$ can be seen as multiplying row $1,2,\dots,n$ of $A$ by $k$, which gives the result.

#### 26

Use Exercise 25, $\det(-A)=(-1)^n\det(A)$, thus if $n$ is even, then $\det(-A)=\det(A)$.

#### 27

$A$ has two identical columns means the rank of $A$ is less than $n$, then use corollary to Theorem 4.6.

#### 28

$\det(E_1)=-1$, $\det(E_2)=k$ if $E_2$ is multiplying any row of $I$ by scalar $k$, and $\det(E_3)=1$​.

#### 29

For each of the three cases, we can see that $E^t$ can be regarded as the same type of elementary matrix (with row operation).

#### 30

If $n$ is even, then $B$ is obtained from $A$ by interchanging $a_1$ with $a_n$, interchanging $a_2$ with $a_{n-1}$, etc, until interchanging $a_{n/2}$ with $a_{n/2+1}$, which is $n/2$ times, thus $\det(B)=(-1)^{n/2}\det(A)$.

If $n$ is odd, similarly $B$ is obtained from $A$ by interchanging rows $(n-1)/2$ times, thus $\det(B)=(-1)^{(n-1)/2}\det(A)$.