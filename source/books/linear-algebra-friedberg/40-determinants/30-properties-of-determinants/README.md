# Properties of Determinants

### Content Notes

#### Theorem 4.7

For any $A,B\in\mathsf{M}_{n\times n}(F)$, $\det(AB)=\det(A)\cdot\det(B)$​.

##### Corollary

A matrix $A\in\mathsf{M}_{n\times n}(F)$ is invertible if and only if $\det(A)\ne0$. Furthermore, if $A$ is invertible, then $\det(A^{-1})=\dfrac{1}{\det(A)}$.

#### Theorem 4.8

For any $A\in\mathsf{M}_{n\times n}(F)$, $\det(A^t)=\det(A)$​.

#### Theorem 4.9 (Cramer's Rule)

Let $Ax=b$ be the matrix form of a system of $n$ linear equations in $n$ unknowns, where $x=(x_1,x_2,\dots,x_n)^t$. If $\det(A)\ne0$, then this system has a unique solution, and for each $k(k=1,2,\dots,n)$, 
$$
x_k=\frac{\det(M_k)}{\det(A)},
$$
where $M_k$ is the $n\times n$ matrix obtained from $A$ by replacing column $k$ of $A$ by $b$.

### Selected Exercises

#### 10

Assume $\det(M)=a\ne0$, then $\det(M^k)=\det(M\cdot M\cdots M)=(\det(M))^k=a^k\ne0$, a contradiction.

#### 11

We have $\det(M)=\det(M^t)=\det(-M)=(-1)^n\det(M)=-\det(M)$, thus $\det(M)=0$.

If $n$ is even, then $M$ may be invertible, an example is $M=\begin{pmatrix}0&-1\\1&0\end{pmatrix}$.

#### 12

We have $\det(QQ^t)=[\det(Q)]^2=\det(I)=1$.

#### 13

(a) Recursively use of $\overline{a+b}=\overline{a}+\overline{b}$ and $\overline{ab}=\overline{a}\overline{b}$.

(b) $1=\det(I)=\det(QQ^*)=\det(Q)\det(\overline{Q^t})=\det(Q)\overline{\det(Q)}$, thus $|\det(Q)|=1$.

#### 14

That $\beta$ is a basis for $\mathsf{F}^n$ means $\beta$ is linearly independent, so the rank of $B$ is $n$ and $B$ is invertible, thus $\det(B)\ne0$, vise versa.

#### 15

Similar means there exists invertible $C\in\mathsf{M}_{n\times n}(F)$ such that $B=C^{-1}AC$, thus $\det(C)\ne0$ and
$$
\det(B)=\det(C^{-1})\det(A)\det(C)=\frac{1}{\det(C)}\det(A)\det(C)=\det(A)
$$

#### 16

$\det(AB)=1$ means $\det(A)\ne0$ and hence $A$ is invertible.

#### 17

From $AB=-BA$ we have
$$
\det(AB)=\det(A)\det(B)=\det(-BA)=(-1)^n\det(B)\det(A)\\\implies\det(A)\det(B)+\det(A)\det(B)=0
$$
since $F$ is not a field of characteristic two, we conclude $\det(A)\det(B)=0$, thus either $\det(A)=0$ or $\det(B)=0$.

#### 19

$\det(A)=\prod_{i=1}^nA_{ii}$.

#### 20

Use cofactor to expand $\det(M)$ from the $n$th row, then the $n-1$th row, until the last rows which the small unitary matrix $I$ lies in, we get
$$
\det(M)=(-1)^{n+n}\det(M_{nn})=\cdots=(-1)^{2n}(-1)^{2n-2}\cdots\det(A)=\det(A)
$$

#### 21

Let $C$ be $r\times r$. If $C$ is not invertible, then $\det(C)=0$, and in this case, the row rank of $C$ must be smaller than $r$, which means the row rank of $M$ must be smaller than $n-r+r=n$, so $\det(M)=0$.

If $C$ is invertible, we have
$$
M=\begin{pmatrix}A&B\\O&C\end{pmatrix}=\begin{pmatrix}A&BC^{-1}\\O&I_{r}\end{pmatrix}\begin{pmatrix}I_{n-r}&O\\O&C\end{pmatrix}
$$
Use the technique from Exercise 20, we can have
$$
\det\begin{pmatrix}A&BC^{-1}\\O&I_{r}\end{pmatrix}=\det(A),\quad\det\begin{pmatrix}I_{n-r}&O\\O&C\end{pmatrix}=\det(C)
$$

#### 22

We have $\beta=\{1,x,\dots,x^n\}$ and $\gamma=\{e_1,\dots,e_{n+1}\}$. Thus $\mathsf{T}(x^i)=(c_0^i,c_1^i,\dots,c_n^i)$ for $i=0,1,\dots,n$, which gives (a). To prove (b), Exercise 22 of Section 2.4 shows that $\mathsf{T}$ is an isomorphism, thus $M$ is invertible and $\det(M)\ne0$. To prove (c), use induction on $n$, when $n=1$, we have $M=\begin{pmatrix}1&c_0\\1&c_1\end{pmatrix}$ and $\det(M)=c_1-c_0$, suppose the conclusion is true for $n=k-1$, consider a Vandermonde matrix with $n=k+1$, we subtract column $i$ by $c_0$ times column $i-1$ for $i=k,k-1,\dots,2$, and get
$$
\begin{aligned}
\det\begin{pmatrix}
1&c_0&c_0^2&\cdots&c_0^{k}
\\
1&c_1&c_1^2&\cdots&c_1^{k}
\\
\vdots&\vdots&\vdots&&\vdots
\\
1&c_{k}&c_k^2&\cdots&c_k^{k}
\end{pmatrix}&=
\det\begin{pmatrix}
1&0&0&\cdots&0
\\
1&c_1-c_0&c_1^2-c_0c_1&\cdots&c_1^{k}-c_0c_1^{k-1}
\\
\vdots&\vdots&\vdots&&\vdots
\\
1&c_{k}-c_0&c_k^2-c_0c_k&\cdots&c_k^{k}-c_0c_k^{k-1}
\end{pmatrix}\\&=
(c_1-c_0)\cdots(c_k-c_0)\det\begin{pmatrix}
1&c_1&\cdots&c_1^{k-1}
\\
\vdots&\vdots&&\vdots
\\
1&c_k&\cdots&c_k^{k-1}
\end{pmatrix}\\&=(c_1-c_0)\cdots(c_k-c_0)\prod_{1\le i<j\le k}(c_j-c_i)
\\&=\prod_{0\le i<j\le k}(c_j-c_i)
\end{aligned}
$$

#### 23

(a) The rows that some particular $k\times k$ submatrix which has a nonzero determinant lies in the original matrix are linearly independent, thus rank$(A)\ge k$. On the other hand, assume rank$(A)>k$, then we can find some  $(k+1)\times(k+1)$ submatrix which has a nonzero determinant, a contradiction, so we must have rank$(A)=k$.

(b) Find $k$ rows of $A$ which are linearly independent to form a new $k\times n$ matrix $A'$, then rank$(A')=k$, which means there are $k$ columns of $A'$ are linearly independent, choose the $k$ columns to form a new $k\times k$ matrix, this matrix is a submatrix of $A$ and has rank $k$, thus invertible and has nonzero determinant.

#### 24

We have
$$
\begin{aligned}
\det(A+tI)&=\det\begin{pmatrix}
t&0&0&\cdots&0&a_0
\\
-1&t&0&\cdots&0&a_1
\\0&-1&t&\cdots&0&a_2
\\
{\vdots}&{\vdots}&{\vdots}&&{\vdots}&{\vdots}
\\
0&0&0&\cdots&-1&t+a_{n-1}
\end{pmatrix}\\&=\det\begin{pmatrix}
0&0&0&\cdots&0&a_0+a_1t+\cdots+a_{n-1}t^{n-1}+t^{n}
\\
-1&0&0&\cdots&0&a_1+a_2t+\cdots+a_{n-1}t^{n-2}+t^{n-1}
\\0&-1&0&\cdots&0&a_2+a_3t+\cdots+a_{n-1}t^{n-3}+t^{n-2}
\\
{\vdots}&{\vdots}&{\vdots}&&{\vdots}&{\vdots}
\\
0&0&0&\cdots&-1&t+a_{n-1}
\end{pmatrix}\\&=(-1)^{n+1}\left(\sum_{i=0}^{n-1}a_it^{i}+t^n\right)\det\begin{pmatrix}
-1&0&0&\cdots&0
\\
0&-1&0&\cdots&0
\\
{\vdots}&{\vdots}&{\vdots}&&{\vdots}
\\
0&0&0&\cdots&-1
\end{pmatrix}
\\&=(-1)^{n+1}(-1)^{n-1}\left(\sum_{i=0}^{n-1}a_it^{i}+t^n\right)=\sum_{i=0}^{n-1}a_it^{i}+t^n
\end{aligned}
$$

#### 25

(a) Compute $\det(B)$ by expansion with column $k$.

(b) By Definition of $\det(A)$ and Theorem 4.4, $\det(A)=\sum_{i=1}^nA_{ji}c_{ji}$, and if $k\ne j$, the expression $\sum_{i=1}^nA_{ki}c_{ji}$ is equivalent to the determinant of $A'$ which comes from $A$ by interchanging the $j$th row with the $k$th row, i.e, $A'$ has two equivalent rows, thus we have
$$
A\begin{pmatrix}c_{j1}\\c_{j2}\\{\vdots}\\c_{jn}\end{pmatrix}=
\begin{pmatrix}
A_{11}&A_{12}&\cdots&A_{1n}
\\
A_{21}&A_{22}&\cdots&A_{2n}
\\
\vdots&\vdots&&\vdots
\\
A_{n1}&A_{n2}&\cdots&A_{nn}
\end{pmatrix}
\begin{pmatrix}c_{j1}\\c_{j2}\\{\vdots}\\c_{jn}\end{pmatrix}
=\begin{pmatrix}\sum_{i}A_{1i}c_{ji}\\\sum_{i}A_{2i}c_{ji}\\{\vdots}\\\sum_{i}A_{ni}c_{ji}\end{pmatrix}
=\begin{pmatrix}
0\\{\vdots}\\\det(A)\\{\vdots}\\0
\end{pmatrix}=\det(A)e_j
$$
(c) use the result of (b).

(d) If $\det(A)\ne0$, then $A$ is invertible, we have
$$
AC=[\det(A)]I\implies [\det(A)]A^{-1}=A^{-1}(AC)=C\implies A^{-1}=[\det(A)]^{-1}C
$$

#### 27

(a) Use Exercise 25(c) we have $AC=[\det(A)]I$. First consider the case if $\det(A)=0$, assume $C$ is invertible, then from $AC=O$ we get $A=ACC^{-1}=OC^{-1}=O$, but this means $C=O$ since each $ij$-cofactor of the zero matrix is zero, a contradiction, thus we must have $C$ not invertible, thus $\det(C)=0=[\det(A)]^{n-1}$. Next consider the case $\det(A)\ne0$, then
$$
\det(A)\det(C)=\det(AC)=[\det(A)]^n\implies \det(C)=[\det(A)]^{n-1}
$$
(b) Since $C_{ij}=c_{ji}$, we have $C^t_{ij}=C_{ji}=c_{ij}$, while the classical adjoint of $A^t$ is the transpose of the matrix whose $ij$-th entry is $c_{ji}$, which means the $ij$-th entry of the classical adjoint of $A^t$ is just $c_{ij}$, which equals $C^t$.

(c) From Exercise 25(d) it suffices to show that $C$ is upper-triangular. Consider $C_{ij}=c_{ji}$ with $i>j$, then $c_{ji}=(-1)^{i+j}\det(\tilde{A}_{ji})$, since $A$ is upper-triangular, $\tilde{A}_{ji}$ is upper-triangular with at least one zero on the diagonal, thus $c_{ji}=0$.

#### 28

(a) Let $y,z\in\mathsf{C}^{\infty}$, then
$$
\begin{aligned}
&[\mathsf{T}(y+z)](t)=\det\begin{pmatrix}
(y+z)(t)&y_1(t)&y_2(t)&\cdots&y_n(t)
\\
(y+z)'(t)&y_1'(t)&y_2'(t)&\cdots&y_n'(t)
\\
{\vdots}&{\vdots}&{\vdots}&&{\vdots}
\\
(y+z)^{(n)}(t)&y_1^{(n)}(t)&y_2^{(n)}(t)&\cdots&y_n^{(n)}(t)
\end{pmatrix}
\\&=\det\begin{pmatrix}
y(t)&y_1(t)&y_2(t)&\cdots&y_n(t)
\\
y'(t)&y_1'(t)&y_2'(t)&\cdots&y_n'(t)
\\
{\vdots}&{\vdots}&{\vdots}&&{\vdots}
\\
y^{(n)}(t)&y_1^{(n)}(t)&y_2^{(n)}(t)&\cdots&y_n^{(n)}(t)
\end{pmatrix}+\det\begin{pmatrix}
z(t)&y_1(t)&y_2(t)&\cdots&y_n(t)
\\
z'(t)&y_1'(t)&y_2'(t)&\cdots&y_n'(t)
\\
{\vdots}&{\vdots}&{\vdots}&&{\vdots}
\\
z^{(n)}(t)&y_1^{(n)}(t)&y_2^{(n)}(t)&\cdots&y_n^{(n)}(t)
\end{pmatrix}
\\&=[\mathsf{T}(y)](t)+[\mathsf{T}(z)](t)
\end{aligned}
$$
and $[\mathsf{T}(cy)](t)=c[\mathsf{T}(y)](t)$ can be similarly proved using the properties of determinants.

(b) If $y\in\mathsf{N(T)}$, then $[\mathsf{T}(y)](t)=0$, thus the matrix
$$
A=\begin{pmatrix}
y(t)&y_1(t)&y_2(t)&\cdots&y_n(t)
\\
y'(t)&y_1'(t)&y_2'(t)&\cdots&y_n'(t)
\\
{\vdots}&{\vdots}&{\vdots}&&{\vdots}
\\
y^{(n)}(t)&y_1^{(n)}(t)&y_2^{(n)}(t)&\cdots&y_n^{(n)}(t)
\end{pmatrix}
$$
has rank less than $n+1$, the columns are linearly dependent, since $y_1,\dots,y_n$ are linearly independent, column $2$ to column $n+1$ are linearly independent, so we must have column $1$ in the span of column $2$ to column $n+1$, this means $y\in\text{span}\{(y_1,\dots,y_n)\}$. Conversely, if $y\in\text{span}\{(y_1,\dots,y_n)\}$, we can express $y$ as linear combinations of $y_1,\dots,y_n$, namely $y=c_1y_1+\cdots+c_ny_n$ for $c_1,\dots,c_n\in\mathsf{C}$, thus
$$
y^{(k)}=c_1y_1^{(k)}+\cdots+c_ny_n^{(k)},\quad k=1,\dots,n
$$
we can conclude in the matrix $A$, use elementary column operations several times, we can make the first column of $A$ all zero, thus $A$ is not invertible and $\det(A)=0$, which means $y\in\mathsf{N(T)}$.