# Normal and Self-adjoint Operators

### Content Notes

#### Lemma

Let $\mathsf{T}$ be a linear operator on a finite-dimensional inner product space $\mathsf{V}$. If $\mathsf{T}$ has an eigenvector, then so does $\mathsf{T}^*$.

#### Theorem 6.14 (Schur)

Let $\mathsf{T}$ be a linear operator on a finite-dimensional inner product space $\mathsf{V}$. Suppose that the characteristic polynomial of $\mathsf{T}$ splits. Then there exists an orthonormal basis $\beta$ for $\mathsf{V}$ such that the matrix $[\mathsf{T}]_{\beta}$​ is upper triangular.

#### Definitions. (normal)

Let $\mathsf{V}$ be an inner product space, and let $\mathsf{T}$ be a linear operator on $\mathsf{V}$. We say that $\mathsf{T}$ is **normal** if $\mathsf{TT^*}=\mathsf{T^*T}$. An $n\times n$ real or complex matrix $A$ is **normal** if $AA^*=A^*A$.

#### Theorem 6.15

Let $\mathsf{V}$ be an inner product space, and let $\mathsf{T}$ be a normal operator on $\mathsf{V}$. Then the following statements are true.

(a) $\|\mathsf{T}(x)\|=\|\mathsf{T}^*(x)\|$ for all $x\in\mathsf{V}$.

(b) $\mathsf{T}-c\mathsf{I}$ is normal for every $c\in F$.

(c) If $x$ is an eigenvector of $\mathsf{T}$, then $x$ is also an eigenvector of $\mathsf{T}^*$. In fact, if $\mathsf{T}(x)=\lambda x$, then $\mathsf{T}^*(x)=\overline{\lambda}x$.

(d) If $\lambda_1$ and $\lambda_2$ are distinct eigenvalues of $\mathsf{T}$ with corresponding eigenvectors $x_1$ and $x_2$, then $x_1$ and $x_2$​ are orthogonal.

#### Theorem 6.16

Let $\mathsf{T}$ be a linear operator on a finite-dimensional complex inner product space $\mathsf{V}$. Then $\mathsf{T}$ is normal if and only if there exists an orthonormal basis for $\mathsf{V}$ consisting of eigenvectors of $\mathsf{T}$.

#### Definitions (self-adjoint)

Let $\mathsf{T}$ be a linear operator on an inner product space $\mathsf{V}$. We say that $\mathsf{T}$ is **self-adjoint (Hermitian)** if $\mathsf{T}=\mathsf{T}^*$. An $n\times n$ real or complex matrix $A$ is **self-adjoint (Hermitian)** if $A=A^*$.

#### Lemma

Let $\mathsf{T}$ be a self-adjoint operator on a finite-dimensional inner product space $\mathsf{V}$. Then

(a) Every eigenvalue of $\mathsf{T}$ is real.

(b) Suppose that $\mathsf{V}$ is a real inner product space. Then the characteristic polynomial of $\mathsf{T}$ splits.

#### Theorem 6.17

Let $\mathsf{T}$ be a linear operator on a finite-dimensional real inner product space $\mathsf{V}$. Then $\mathsf{T}$ is self-adjoint if and only if there exists an orthonormal basis for $\mathsf{V}$ consisting of eigenvectors of $\mathsf{T}$.

### Selected Exercises

#### 4

If $\mathsf{TU}$ is self-adjoint, then $\mathsf{TU}=(\mathsf{TU})^*=\mathsf{U^*T^*}=\mathsf{UT}$. Conversely if $\mathsf{TU}=\mathsf{UT}$, then $(\mathsf{TU})^*=(\mathsf{UT})^*=\mathsf{T}^*\mathsf{U}^*=\mathsf{TU}$.

#### 5

We have $(\mathsf{T}-c\mathsf{I})^*=\mathsf{T}^*-\overline{c}\mathsf{I}$ by Theorem 6.11, so
$$
(\mathsf{T}-c\mathsf{I})(\mathsf{T}-c\mathsf{I})^*=(\mathsf{T}-c\mathsf{I})(\mathsf{T}^*-\overline{c}\mathsf{I})=\mathsf{T}\mathsf{T}^*-c\mathsf{T}^*-\overline{c}\mathsf{T}+|c|^2\mathsf{I}
\\
(\mathsf{T}-c\mathsf{I})^*(\mathsf{T}-c\mathsf{I})=(\mathsf{T}^*-\overline{c}\mathsf{I})(\mathsf{T}-c\mathsf{I})=\mathsf{T}^*\mathsf{T}-\overline{c}\mathsf{T}-c\mathsf{T}^*+|c|^2\mathsf{I}
$$
and the conclusion follows since $\mathsf{T}$ is normal.

#### 6

(a) It is easy to prove $\mathsf{T}_1$ and $\mathsf{T}_2$ are self-adjoint, and
$$
\mathsf{T}_1+i\mathsf{T}_2=\frac{1}{2}(\mathsf{T}+\mathsf{T}^*)+\frac{i}{2i}(\mathsf{T}-\mathsf{T}^*)=\mathsf{T}
$$
(b) We have $\mathsf{T}=\mathsf{U}_1+i\mathsf{U}_2$ and $\mathsf{T}^*=(\mathsf{U}_1+i\mathsf{U}_2)^*=\mathsf{U}_1^*-i\mathsf{U}_2^*$, use the condition that $\mathsf{U}_1$ and $\mathsf{U}_2$ are self-adjoint, we have $\mathsf{T}^*=\mathsf{U}_1-i\mathsf{U}_2$, solve $\mathsf{U}_1$ and $\mathsf{U}_2$ in terms of $\mathsf{T}$ and $\mathsf{T}^*$, we can see that $\mathsf{U}_1=\mathsf{T}_1$ and $\mathsf{U}_2=\mathsf{T}_2$​.

(c) If $\mathsf{T}$ is normal, then
$$
\mathsf{T}_1\mathsf{T}_2=\frac{1}{4i}(\mathsf{T}+\mathsf{T}^*)(\mathsf{T}-\mathsf{T}^*)=\frac{1}{4i}(\mathsf{T}^2+\mathsf{T}^*\mathsf{T}-\mathsf{T}\mathsf{T}^*-(\mathsf{T}^*)^2)=\frac{1}{4i}(\mathsf{T}^2-(\mathsf{T}^*)^2)
\\
\mathsf{T}_2\mathsf{T}_1=\frac{1}{4i}(\mathsf{T}-\mathsf{T}^*)(\mathsf{T}+\mathsf{T}^*)=\frac{1}{4i}(\mathsf{T}^2-(\mathsf{T}^*)^2)
$$
thus $\mathsf{T}_1\mathsf{T}_2=\mathsf{T}_2\mathsf{T}_1$. Conversely, if we have  $\mathsf{T}_1\mathsf{T}_2=\mathsf{T}_2\mathsf{T}_1$, then
$$
\mathsf{T}\mathsf{T}^*=(\mathsf{T}_1+i\mathsf{T}_2)(\mathsf{T}_1^*-i\mathsf{T}_2^*)=\mathsf{T}_1^2+i\mathsf{T}_2\mathsf{T}_1-i\mathsf{T}_1\mathsf{T}_2+\mathsf{T}_2^2=\mathsf{T}_1^2+\mathsf{T}_2^2
\\
\mathsf{T}^*\mathsf{T}=(\mathsf{T}_1^*-i\mathsf{T}_2^*)(\mathsf{T}_1+i\mathsf{T}_2)=\mathsf{T}_1^2+i\mathsf{T}_1\mathsf{T}_2-i\mathsf{T}_2\mathsf{T}_1+\mathsf{T}_2^2=\mathsf{T}_1^2+\mathsf{T}_2^2
$$

#### 7

(a) For any $w\in\mathsf{W}$, we have $\mathsf{T}^*(w)=\mathsf{T}(w)\in\mathsf{W}$, so $\mathsf{W}$ is also a $\mathsf{T}^*$-invariant subspace. Use the conclusion of (c) we have $(\mathsf{T_W})^*=(\mathsf{T}^*)_{\mathsf{W}}=\mathsf{T}_{\mathsf{W}}$, so $\mathsf{T}_{\mathsf{W}}$ is self-adjoint.

(b) Let $z\in\mathsf{W}^{\perp}$, for  any $w\in\mathsf{W}$, we have $\lang{w,\mathsf{T}^*(z)}\rang=\lang{\mathsf{T}(w),z}\rang=0$, so $\mathsf{T}^*(z)\in\mathsf{W}^{\perp}$.

(c) Let $\mathsf{U}=(\mathsf{T_W})^*$, then $\lang{\mathsf{T_W}(w),w'}\rang=\lang{w,\mathsf{U}(w')}\rang$ for any $w,w'\in\mathsf{W}$, as $\mathsf{{W}}\subset\mathsf{V}$, we have
$$
\lang{\mathsf{T_W}(w),w'}\rang=\lang{\mathsf{T}(w),w'}\rang=\lang{w,\mathsf{T^*}(w')}\rang=\lang{w,\mathsf{U}(w')}\rang
$$
which means $\mathsf{U}=\mathsf{T}^*$ on $\mathsf{W}$, or $\mathsf{U}=(\mathsf{T}^*)_{\mathsf{W}}$.

(d) For any $w\in\mathsf{W}$ we have
$$
\mathsf{T_W}(\mathsf{T_W})^*(w)=\mathsf{T_W}(\mathsf{T}^*)_{\mathsf{W}}(w)=\mathsf{T}\mathsf{T}^*(w)=\mathsf{T}^*\mathsf{T}(w)=(\mathsf{T}^*)_{\mathsf{W}}\mathsf{T_W}(w)=(\mathsf{T_W})^*\mathsf{T_W}(w)
$$
where the first and the last equality used the conclusion of (c).

#### 8

By Theorem 6.16, there exists an orthonormal basis for $\mathsf{V}$ consisting of eigenvectors of $\mathsf{T}$. If $\mathsf{W}$ is the zero subspace, then there is nothing to prove. Otherwise, use Exercise 24 of Section 5.4, we know that $\mathsf{T_W}$ is also diagonalizable, thus there exists an orthonormal basis $\beta=\{w_1,\dots,w_k\}$ for $\mathsf{W}$ consisting of eigenvectors of $\mathsf{T}$. We set $\mathsf{T_W}(w_i)=\lambda_i w_i$ for $i=1,\dots,k$, by Theorem 6.15(c) we have $\mathsf{T}^*(w_i)=\overline{\lambda_i}w_i$, this means $\mathsf{W}$ is $\mathsf{T}^*$ invariant.

#### 9

Theorem 6.15(a) tells that 
$$
x\in\mathsf{N(T)}\Leftrightarrow\mathsf{T}(x)=0\Leftrightarrow\|\mathsf{T}(x)\|=0=\|\mathsf{T}^*(x)\|\Leftrightarrow\mathsf{T}^*(x)=0\Leftrightarrow x\in\mathsf{N(T^*)}
$$
then Exercise 12 of Section 6.3 shows $\mathsf{R(T^*)}=\mathsf{N(T)}^{\perp}$, thus
$$
\mathsf{R(T^*)}=\mathsf{N(T)}^{\perp}=[\mathsf{N(T^*)}]^{\perp}=\mathsf{R((T^*)^*)}=\mathsf{R(T)}
$$

#### 10

We have $\lang{\mathsf{T}(x),x}\rang=\lang{x,\mathsf{T}(x)}\rang$ for all $x\in\mathsf{V}$, thus
$$
\begin{aligned}
\|\mathsf{T}(x)-ix\|^2&=\lang{\mathsf{T}(x)-ix,\mathsf{T}(x)-ix}\rang\\&=\lang{\mathsf{T}(x),\mathsf{T}(x)}\rang-\lang{\mathsf{T}(x),ix}\rang-\lang{ix,\mathsf{T}(x)}\rang+\lang{ix,ix}\rang
\\&=\|\mathsf{T}(x)\|^2+i\lang{\mathsf{T}(x),x}\rang-i\lang{x,\mathsf{T}(x)}\rang-i^2\|x\|^2\\&=\|\mathsf{T}(x)\|^2+\|x\|^2
\end{aligned}
$$
and
$$
\begin{aligned}
\|\mathsf{T}(x)+ix\|^2&=\lang{\mathsf{T}(x)+ix,\mathsf{T}(x)+ix}\rang\\&=\lang{\mathsf{T}(x),\mathsf{T}(x)}\rang+\lang{\mathsf{T}(x),ix}\rang+\lang{ix,\mathsf{T}(x)}\rang+\lang{ix,ix}\rang
\\&=\|\mathsf{T}(x)\|^2-i\lang{\mathsf{T}(x),x}\rang+i\lang{x,\mathsf{T}(x)}\rang-i^2\|x\|^2\\&=\|\mathsf{T}(x)\|^2+\|x\|^2
\end{aligned}
$$
So if $(\mathsf{T}-i\mathsf{I})(x)=0$, we have $\|\mathsf{T}(x)\|=\|x\|=0$, or $x=0$, so $\mathsf{T}-i\mathsf{I}$ is one-to-one, thus invertible on $\mathsf{V}$. Since
$$
\mathsf{I}=\mathsf{I}^*=[(\mathsf{T}-i\mathsf{I})^{-1}(\mathsf{T}-i\mathsf{I})]^*=(\mathsf{T}-i\mathsf{I})^*[(\mathsf{T}-i\mathsf{I})^{-1}]^*=(\mathsf{T}+i\mathsf{I})[(\mathsf{T}-i\mathsf{I})^{-1}]^*
$$
we have $[(\mathsf{T}-i\mathsf{I})^{-1}]^*=(\mathsf{T}+i\mathsf{I})^{-1}$.

#### 11

(a) We have $\lang{\mathsf{T}(x),x}\rang=\lang{x,\mathsf{T}(x)}\rang=\overline{\lang{\mathsf{T}(x),x}\rang}$ for all $x\in\mathsf{V}$.

(b) We have
$$
\lang\mathsf{T}(x+y),x+y\rang=\lang{\mathsf{T}(x),y}\rang+\lang{\mathsf{T}(y),x}\rang=0
\\
\lang\mathsf{T}(x+iy),x+iy\rang=\lang{\mathsf{T}(x),iy}\rang+\lang{i\mathsf{T}(y),x}\rang=-i(\lang{\mathsf{T}(x),y}\rang-\lang{\mathsf{T}(y),x}\rang)=0
$$
which gives $\lang{\mathsf{T}(x),y}\rang=0$ for all $x,y\in\mathsf{V}$, so let $y=\mathsf{T}(x)$ we get $\mathsf{T}(x)=0$ for all $x\in\mathsf{V}$.

(c) Use similar technique in (b), we can have $\lang{\mathsf{T}(x),y}\rang+\lang{\mathsf{T}(y),x}\rang$ is real and $i(\lang{\mathsf{T}(x),y}\rang-\lang{\mathsf{T}(y),x}\rang)$ is real for all $x,y\in\mathsf{V}$. We set $\lang{\mathsf{T}(x),y}\rang=a+bi$ and $\lang{\mathsf{T}(y),x}\rang=c-bi$ with $a,b,c$ real numbers, then
$$
i(\lang{\mathsf{T}(x),y}\rang-\lang{\mathsf{T}(y),x}\rang)=i(a+bi-c+bi)=i(a-c)-2b\implies a=c
$$
so we conclude that $\lang{\mathsf{T}(x),y}\rang=\overline{\lang{\mathsf{T}(y),x}\rang}$, then
$$
\lang{x,\mathsf{T}^*(y)}\rang=\lang{\mathsf{T}(x),y}\rang=\overline{\lang{\mathsf{T}(y),x}\rang}=\lang{x,\mathsf{T}(y)}\rang\implies\lang{x,(\mathsf{T}-\mathsf{T}^*)(y)}\rang=0
$$
Let $x=(\mathsf{T}-\mathsf{T}^*)(y)$, we see that $(\mathsf{T}-\mathsf{T}^*)(y)=0$ for all $y\in\mathsf{V}$, so $\mathsf{T}=\mathsf{T}^*$.

#### 12

If $\mathsf{T}$ is normal and the characteristic polynomial of $\mathsf{T}$ splits, then we can completely follow the proof of Theorem 6.16 to get an orthonormal basis for $\mathsf{V}$ consisting of eigenvectors of $\mathsf{T}$. Then use Theorem 6.17, $\mathsf{T}$ is self-adjoint.

#### 13

If $A$ is symmetric and all its eigenvalues are non-negative, then $\mathsf{T}=\mathsf{L}_A$ is self-adjoint since for standard ordered basis $\beta$ in $\mathsf{F}^n$ we have $[\mathsf{T}^*]_{\beta}=[\mathsf{T}]_{\beta}^*=A^*=A=[\mathsf{T}]_{\beta}$, which means $\mathsf{T}=\mathsf{T}^*$. Apply Theorem 6.17, we have an orthonormal basis $\alpha=\{v_1,\dots,v_n\}$ of eigenvectors with the associated eigenvalues $\lambda_1,\dots,\lambda_n$. Define $\mathsf{U}$ by $\mathsf{U}(v_i)=\sqrt{\lambda_i}v_i$ for $i=1,\dots,n$, then
$$
[\mathsf{U}]_{\alpha}=\begin{pmatrix}\sqrt{\lambda_1}&&\\&{\ddots}&\\&&\sqrt{\lambda_n}\end{pmatrix}\implies[\mathsf{U^*U}]_{\alpha}=[\mathsf{T}]_{\alpha}
$$
thus $\mathsf{T}=\mathsf{U^*U}$, let $B=[\mathsf{U}]_{\beta}$, we have $A=B^*B=B^tB$, which is a Gramian matrix.

Conversely, if $A=B^tB$ for some real square matrix $B$, then $A^t=(B^tB)^t=B^t(B^t)^t=B^tB=A$, and let $\lambda$ be an eigenvalue of $A$. We let $\mathsf{T}=\mathsf{L}_A$ and $\mathsf{U}=\mathsf{L}_B$, then $\lambda$ is an eigenvalue of $\mathsf{T}$, also we have
$$
\mathsf{U^*U}=(\mathsf{L}_B)^*\mathsf{L}_B=\mathsf{L}_{B^t}\mathsf{L}_B=\mathsf{L}_{B^tB}=\mathsf{L}_A=\mathsf{T}
$$
let $v$ be the eigenvalue of $\mathsf{T}$ corresponding to $\lambda$, then $v\ne0$ and
$$
\lambda\|v\|^2=\lambda\lang{v,v}\rang=\lang{\mathsf{T}(v),v}\rang=\lang{\mathsf{U^*U}(v),v}\rang=\lang{\mathsf{U}(v),\mathsf{U}(v)}\rang=\|\mathsf{U}(v)\|^2\implies\lambda=\frac{\|\mathsf{U}(v)\|^2}{\|v\|^2}\ge0
$$

#### 14

Suppose there is an eigenvalue $\lambda$ of $\mathsf{T}$, then we get an eigenspace $\mathsf{W}=\mathsf{E}_{\lambda}$. It is easy to see that $\mathsf{W}$ is $\mathsf{T}$-invariant. Also for any $w\in\mathsf{W}$ we have
$$
(\mathsf{T}-\lambda\mathsf{I})\mathsf{U}(w)=\mathsf{T}\mathsf{U}(w)-\lambda\mathsf{U}(w)=\mathsf{U}\mathsf{T}(w)-\lambda\mathsf{U}(w)=\mathsf{U}(\mathsf{T}-\lambda\mathsf{I})(w)=0
$$
this shows $\mathsf{U}(w)\in\mathsf{W}$, or $\mathsf{W}$ is $\mathsf{U}$-invariant. Apply Theorem 6.17 to $\mathsf{U_W}$, there exists an orthonormal basis for $\mathsf{W}$ consisting of eigenvectors of $\mathsf{U}$​.

Since $\mathsf{T}$ is self-adjoint, apply Theorem 6.17, we can have an orthonormal basis $\alpha=\{v_1,\dots,v_n\}$ for $\mathsf{V}$ consisting of eigenvectors with the associated eigenvalues. Let the different eigenvalues of $\mathsf{T}$ be $\lambda_1,\dots,\lambda_k$, we have
$$
\mathsf{V}=\mathsf{E}_{\lambda_1}\oplus\cdots\oplus\mathsf{E}_{\lambda_k}
$$
Now use the procedure above, we get an orthonormal basis $\alpha_i$ for $\mathsf{E}_{\lambda_i}$ consisting of eigenvectors of $\mathsf{U}$, then $\alpha_1\cup\cdots\cup\alpha_k$ is a basis for $\mathsf{V}$, which consists of eigenvectors of both $\mathsf{T}$ and $\mathsf{U}$.

#### 15

Let $\mathsf{T}=\mathsf{L}_A$ and $\mathsf{U}=\mathsf{L}_B$, then $\mathsf{TU}=\mathsf{UT}$ and both $\mathsf{T}$ and $\mathsf{U}$ are self-adjoint. Use Exercise 14, there is an orthonormal basis $\alpha=\{v_1,\dots,v_n\}$ for $\mathsf{V}$ consisting of eigenvectors of both $\mathsf{T}$ and $\mathsf{U}$. Let $P=(v_1,\dots,v_n)$, where each $v_i$ is viewed as a column vector in $\mathsf{F}^n$, then $P^tP=I$, so $P$ is an orthogonal matrix, and it is easy to verify that $P^tAP$ and $P^tBP$ are diagonal. (NOTE: this exercise requires that $A$ and $B$ are real, and the definition of orthogonal matrix is officially given in Sec 6.5 )

#### 17

(a) Suppose $\lambda$ is an eigenvalue of $\mathsf{T}$, and $v$ is one eigenvector corresponding to $\lambda$, then $\lang{\mathsf{T}(v),v}\rang=\lambda\lang{v,v}\rang$, thus if $\mathsf{T}$ is positive definite[semidefinite], then $\lambda\lang{v,v}\rang>0(\ge0)$, since $v\ne0$ we see $\lang{v,v}\rang>0$, so $\lambda>0(\ge0)$, which means any eigenvalue of $\mathsf{T}$ is positive [nonnegative]. Conversely, if all eigenvalues of $\mathsf{T}$ is positive [nonnegative], let $\alpha=\{v_1,\dots,v_n\}$ be an orthonormal basis for $\mathsf{V}$ consisting of eigenvectors of $\mathsf{T}$ and suppose $\mathsf{T}(v_i)=\lambda_i v_i$ for $i=1,\dots,n$, we see that each $\lambda_i>0(\ge0)$, consider any $x=\sum_ic_i v_i\ne0$, then at least one $c_i\ne0$, and
$$
\lang{\mathsf{T}(x),x}\rang=\left<\sum_{i=1}^nc_i\lambda_i v_i,\sum_{i=1}^nc_i v_i\right>=\sum_{i=1}^n\lambda_i|c_i|^2>0(\ge0)
$$
(b) Write $\beta=\{v_1,\dots,v_n\}$ and $x=\sum_ia_i v_i$ for nonzero $n$-tuple $(a_1,a_2,\dots,a_n)$. Then
$$
\begin{aligned}
\mathsf{T}\text{ is positive definite}&\Leftrightarrow\lang{\mathsf{T}(x),x}\rang>0
\\&\Leftrightarrow\left<\sum_{j=1}^na_j\mathsf{T}(v_j),\sum_{i=1}^na_i v_i\right>>0
\\&\Leftrightarrow\left<\sum_{j=1}^na_j\sum_{i=1}^nA_{ij}v_i,\sum_{i=1}^na_i v_i\right>>0
\\&\Leftrightarrow\sum_{i=1}^n\sum_{j=1}^nA_{ij}a_j\overline{a_i}>0
\end{aligned}
$$
(c) If $A=B^*B$, let $\mathsf{R}$ be the linear operator such that $[\mathsf{R}]_{\beta}=B$, then 
$$
[\mathsf{T}]_{\beta}=A=([\mathsf{R}]_{\beta})^*[\mathsf{R}]_{\beta}=[\mathsf{R}^*]_{\beta}[\mathsf{R}]_{\beta}=[\mathsf{R}^*\mathsf{R}]_{\beta}\implies\mathsf{T}=\mathsf{R}^*\mathsf{R}
$$
thus for any $x\ne0$ we have
$$
\lang{\mathsf{T}(x),x}\rang=\lang{(\mathsf{R^*R})(x),x}\rang=\lang{\mathsf{R}(x),\mathsf{R}(x)}\rang\ge0
$$
which means $\mathsf{T}$ is a positive semidefinite operator. Conversely, suppose $\mathsf{T}$ is positive semidefinite, then there exists an orthonormal basis $\alpha$ for $\mathsf{V}$ consisting of eigenvectors of $\mathsf{T}$, which means $[\mathsf{T}]_{\alpha}$ is diagonal and each diagonal entry is nonnegative. Write
$$
[\mathsf{T}]_{\alpha}=\begin{pmatrix}\lambda_1&&
\\
&\ddots&
\\&&\lambda_n
\end{pmatrix},\quad\lambda_i\ge0\text{ for }i=1,\dots,n
$$
Since each $\lambda_i$ is real, we can get a non-negative square root of $\lambda_i$ to be $\sqrt{\lambda_i}$, and let 
$$
M=\begin{pmatrix}\sqrt{\lambda_1}&&
\\
&\ddots&
\\&&\sqrt{\lambda_n}
\end{pmatrix}
$$
and let $\mathsf{R}$ be the linear transformation such that $[\mathsf{R}]_{\alpha}=M$, then we have
$$
[\mathsf{T}]_{\alpha}=M^*M=([\mathsf{R}]_{\alpha})^*[\mathsf{R}]_{\alpha}=[\mathsf{R}^*]_{\alpha}[\mathsf{R}]_{\alpha}=[\mathsf{R}^*\mathsf{R}]_{\alpha}\implies\mathsf{T}=\mathsf{R}^*\mathsf{R}
$$
let $B=[\mathsf{R}]_{\beta}$, we have $A=[\mathsf{T}]_{\beta}=[\mathsf{R}^*\mathsf{R}]_{\beta}=[\mathsf{R}^*]_{\beta}[\mathsf{R}]_{\beta}=B^*B$​.

(d) Let $\alpha$ be an orthonormal basis for $\mathsf{V}$ consisting of eigenvectors of $\mathsf{T}$, assume $\mathsf{T}\ne\mathsf{U}$, then there exists at least one $v\in\alpha$ such that $\mathsf{T}(v)=\lambda v\ne\mathsf{U}(v)$, since $\mathsf{T}$ is positive semidefinite, we have $\lambda\ge0$, now
$$
\mathsf{T}^2(v)=\lambda^2v=\mathsf{U}^2(v)\implies(\mathsf{U}+\lambda\mathsf{I})(\mathsf{U}-\lambda\mathsf{I})(v)=0
$$
since we assume $\lambda v\ne\mathsf{U}(v)$, we must have $w=(\mathsf{U}-\lambda\mathsf{I})(v)\ne0$, thus $(\mathsf{U}+\lambda\mathsf{I})(w)=0$, so $-\lambda$ is an eigenvalue of $\mathsf{U}$, by (a), we have $-\lambda\ge0$ or $\lambda\le0$, this means $\lambda=0$, then $\mathsf{U}^2(v)=0$, this means
$$
0=\lang{\mathsf{U}^2(v),v}\rang=\lang{(\mathsf{U}^*\mathsf{U})(v),v}\rang=\lang{\mathsf{U}(v),\mathsf{U}(v)}\rang\implies\mathsf{U}(v)=0=\mathsf{T}(v)
$$
this is a contradiction.

(e) Use Exercise 14, there exists an orthonormal basis $\alpha$ for $\mathsf{V}$ consisting of vectors that are eigenvectors of both $\mathsf{T}$ and $\mathsf{U}$, we denote
$$
[\mathsf{T}]_{\alpha}=\begin{pmatrix}\lambda_1&&
\\
&\ddots&
\\&&\lambda_n
\end{pmatrix},\quad [\mathsf{U}]_{\alpha}=\begin{pmatrix}\lambda_1'&&
\\
&\ddots&
\\&&\lambda_n'
\end{pmatrix}
$$
it follows that all $\lambda_i$s and all $\lambda_i'$s are positive, we have
$$
[\mathsf{TU}]_{\alpha}=[\mathsf{T}]_{\alpha}[\mathsf{U}]_{\alpha}=\begin{pmatrix}\lambda_1\lambda_1'&&
\\
&\ddots&
\\&&\lambda_n\lambda_n'
\end{pmatrix}
$$
so all eigenvalues of $\mathsf{TU}$ are positive, use (a) we see that $\mathsf{TU}$ is positive definite.

(f) The eigenvalues of $\mathsf{T}$ are the same as the eigenvalues of $A$.

#### 18

(a) First we have $(\mathsf{T^*T})^*=\mathsf{T}^*(\mathsf{T}^*)^*=\mathsf{T^*T}$, thus $\mathsf{T^*T}$ is self-adjoint. Suppose $\lambda$ is an eigenvalue of $\mathsf{T^*T}$ and $v$ is the corresponding eigenvalue, then $v\ne0$ and
$$
\lambda\lang{v,v}\rang=\lang{\mathsf{T^*T}(v),v}\rang=\lang{\mathsf{T}(v),\mathsf{T}(v)}\rang\implies\lambda=\frac{\lang{\mathsf{T}(v),\mathsf{T}(v)}\rang}{\|v\|^2}\ge0
$$
use Exercise 17(a) we have $\mathsf{T^*T}$ is positive semidefinite. The proof of $\mathsf{TT^*}$ being positive semidefinite is similar.

(b) Let $v\in\mathsf{V}$, then
$$
\mathsf{T^*T}(v)=0\implies\lang{\mathsf{T^*T}(v),v}\rang=0\implies\lang{\mathsf{T}(v),\mathsf{T}(v)}\rang=0\implies\mathsf{T}(v)=0
$$
and obviously $\mathsf{T}(v)=0$ implies $\mathsf{T^*T}(v)=0$, so we see $\mathsf{N(T)}=\mathsf{N(T^*T)}$, similarly we can have $\mathsf{N(T^*)}=\mathsf{N(TT^*)}$, use dimension theorem we have
$$
\dim(\mathsf{V})=\text{rank}(\mathsf{T})+\text{nullity}(\mathsf{T})=\text{rank}(\mathsf{T^*T})+\text{nullity}(\mathsf{T^*T})\\\implies\text{rank}(\mathsf{T})=\text{rank}(\mathsf{T^*T})
\\
\dim(\mathsf{W})=\text{rank}(\mathsf{T^*})+\text{nullity}(\mathsf{T^*})=\text{rank}(\mathsf{TT^*})+\text{nullity}(\mathsf{TT^*})\\\implies\text{rank}(\mathsf{T^*})=\text{rank}(\mathsf{TT^*})
$$
Exercise 15(c) of Section 6.3 shows that $\text{rank}(\mathsf{T}^*)=\text{rank}(\mathsf{T})$.

#### 19

(a) We have $(\mathsf{T}+\mathsf{U})^*=\mathsf{T}^*+\mathsf{U}^*=\mathsf{T}+\mathsf{U}$, thus $\mathsf{T}+\mathsf{U}$ is self-adjoint. Let $x\ne0$, we have
$$
\lang(\mathsf{T}+\mathsf{U})(x),x\rang=\lang\mathsf{T}(x),x\rang+\lang\mathsf{U}(x),x\rang>0
$$
this means $\mathsf{T}+\mathsf{U}$ is positive definite.

(b) $c>0$ means that $c$ is a real number, so $(c\mathsf{T})^*=\bar{c}\mathsf{T}^*=c\mathsf{T}$ is self-adjoint, and
$$
\lang(c\mathsf{T})(x),x\rang=c\lang\mathsf{T}(x),x\rang>0
$$
 this means $c\mathsf{T}$ is positive definite.

(c) From $(\mathsf{TT^{-1}})^*=(\mathsf{T}^{-1})^*\mathsf{T}^*=\mathsf{I}^*=\mathsf{I}$ we know that $(\mathsf{T}^*)^{-1}=(\mathsf{T}^{-1})^*=\mathsf{T}^{-1}$, so $\mathsf{T}^{-1}$ is self-adjoint, by Exercise 17(a), all eigenvalues of $\mathsf{T}$ are positive, for any $\lambda$ being an eigenvalue of $\mathsf{T}^{-1}$, we have $\mathsf{T}^{-1}v=\lambda v$ for some $v\ne0$, or $v=\lambda\mathsf{T}v$, this means $\lambda^{-1}$ is an eigenvalue of $\mathsf{T}$, thus positive, and so $\lambda$ is positive. We can conclude all eigenvalues of $\mathsf{T}^{-1}$ is positive, use Exercise 17(a) again, $\mathsf{T}^{-1}$ is positive definite.

#### 20

We first have, for $x,z,y\in\mathsf{V}$ and $c$ a scalar, that
$$
\lang{cx+z,y}\rang'=\lang\mathsf{T}(cx+z),y\rang=c\lang\mathsf{T}(x),y\rang+\lang\mathsf{T}(z),y\rang=c\lang{x,y}\rang'+\lang{z,y}\rang'
$$
 Next,
$$
\lang{y,x}\rang'=\lang\mathsf{T}(y),x\rang=\lang{y,\mathsf{T}(x)}\rang=\overline{\lang\mathsf{T}(x),y\rang}=\overline{\lang{x,y}\rang'}
$$
Finally, if $x\ne0$, then use the property of $\mathsf{T}$ being positive definite we have
$$
\lang{x,x}\rang'=\lang{\mathsf{T}(x),x}\rang>0
$$

#### 21

That $\mathsf{T}$ is positive definite means $\lang{x,y}\rang'=\lang\mathsf{T}(x),y\rang$ is an inner product, thus
$$
\lang{x,(\mathsf{UT})^*(y)}\rang'=\lang{\mathsf{UT}(x),y}\rang'=\lang\mathsf{TUT}(x),y\rang=\lang{\mathsf{T}(x),\mathsf{UT}(y)}\rang=\lang{x,\mathsf{UT}(y)}\rang'
$$
thus $\mathsf{UT}$ is self-adjoint with respect to the inner product $\lang{\cdot,\cdot}\rang'$, thus there is an orthonormal basis (in the context of the inner product $\lang{\cdot,\cdot}\rang'$) of $\mathsf{V}$ consisting of eigenvectors of $\mathsf{UT}$ with real eigenvalues.

For $\mathsf{TU}$, notice that $\mathsf{T}^{-1}$ is positive definite by Exercise 19(c), redefine $\lang{\cdot,\cdot}\rang'$ by $\lang{x,y}\rang'=\lang\mathsf{T}^{-1}(x),y\rang$, which is still an inner product, then
$$
\lang{x,(\mathsf{TU})^*(y)}\rang'=\lang{\mathsf{TU}(x),y}\rang'=\lang\mathsf{U}(x),y\rang=\lang{\mathsf{TT}^{-1}(x),\mathsf{U}(y)}\rang=\lang{x,\mathsf{TU}(y)}\rang'
$$
thus $\mathsf{TU}$ is self-adjoint with respect to the inner product $\lang{\cdot,\cdot}\rang'$, and the rest is similar.

#### 22

(a) Let $\beta=\{v_1,\dots,v_n\}$ be an orthonormal basis for $\mathsf{V}$ with respect to $\lang{\cdot,\cdot}\rang$, define $A$ by $A_{ij}=\lang{v_j,v_i}\rang'$ for all $i$ and $j$, let $\mathsf{T}$ be the operator such that $[\mathsf{T}]_{\beta}=A$, then for all $x$ and $y$ in $\mathsf{V}$ we have
$$
x=\sum_{i=1}^n\lang{x,v_i}\rang v_i=\sum_{i=1}^nc_iv_i,\quad y=\sum_{i=1}^n\lang{y,v_i}\rang v_i=\sum_{i=1}^nd_iv_i
$$
and
$$
\mathsf{T}(v_j)=\sum_{i=1}^nA_{ij}v_i,\quad j=1,\dots,n
$$
thus
$$
\lang{x,y}\rang'=\sum_{i=1}^n\sum_{j=1}^nc_j\overline{d_i}\lang{v_j,v_i}\rang'=\sum_{i=1}^n\sum_{j=1}^nc_j\overline{d_i}A_{ij}=\sum_{i=1}^n\sum_{j=1}^nA_{ij}\lang{x,d_iv_j}\rang
$$
and
$$
\lang\mathsf{T}(x),y\rang=\left<\sum_{i=1}^n\sum_{j=1}^nc_jA_{ij}v_i,\sum_{k=1}^nd_kv_k\right>\\=\sum_{i=1}^n\sum_{j=1}^nc_jA_{ij}\left< v_i,\sum_{k=1}^nd_kv_k\right>=\sum_{i=1}^n\sum_{j=1}^nc_j\overline{d_i}A_{ij}
$$
it is easy to see they are equal.

(b) From
$$
\lang{x,\mathsf{T}^*(y)}\rang=\lang{\mathsf{T}(x),y}\rang=\lang{x,y}\rang'=\overline{\lang{y,x}\rang}=\overline{\lang\mathsf{T}(y),x\rang}=\lang{x,\mathsf{T}(y)}\rang
$$
we see that $\mathsf{T}=\mathsf{T}^*$, and $\lang\mathsf{T}(x),x\rang=\lang{x,x}\rang'>0$ for $x\ne0$, so $\mathsf{T}$ is positive definite with $\lang{\cdot,\cdot}\rang$. By Exercise 17(a), all eigenvalues of $\mathsf{T}$ are positive, so $\mathsf{T}$ is invertible, since $\mathsf{T}^{-1}$ satisfy the relation
$$
\lang\mathsf{T}^{-1}(x),y\rang'=\lang\mathsf{TT}^{-1}(x),y\rang=\lang{x,y}\rang,\quad\forall x,y\in\mathsf{V}
$$
use (a) we know that $\mathsf{T}^{-1}$ is the unique linear operator satisfy the relation, with similar proof above we can prove $\mathsf{T}^{-1}$ is positive definite with $\lang{\cdot,\cdot}\rang'$, then use Exercise 19(c) we get $\mathsf{T}$ is positive definite with $\lang{\cdot,\cdot}\rang'$.

#### 24

(a) Suppose $\beta=\{v_1,\dots,v_n\}$ and $\gamma=\{w_1,\dots,w_n\}$. The Gram-Schmidt orthogonalization process to $\beta$ has the property that
$$
\text{span}(v_1,\dots,v_k)=\text{span}(w_1,\dots,w_k),\quad k=1,\dots,n
$$
for any $k=1,\dots,n$, we have
$$
\mathsf{T}(v_j)\subseteq\text{span}(v_1,\dots,v_k),\quad\forall j\le k
$$
and the Gram-Schmidt process shows that $w_k\subseteq\text{span}(v_1,\dots,v_k)$, thus
$$
\mathsf{T}(w_k)\subseteq\text{span}(\mathsf{T}(v_1),\dots,\mathsf{T}(v_k))\subseteq\text{span}(v_1,\dots,v_k)=\text{span}(w_1,\dots,w_k)
$$
this means $[\mathsf{T}]_{\gamma}$ is upper-triangular.

(b) By Exercise 32 of Section 5.4, if the characteristic polynomial of $\mathsf{T}$ splits, then there is an ordered basis $\beta$ for $\mathsf{V}$ such that $[\mathsf{T}]_{\beta}$ is an upper triangular matrix. Then use (a).

### Summary

第五章已经研究过可对角化线性变换的充要条件是V有一组全部由该线性变换特征向量组成的基，这一章引入了内积，我们自然想进一步寻找V是否能有一组全部由该线性变换特征向量组成的标准正交基。本节首先证明引理：$\mathsf{T}$有特征向量则$\mathsf{T}^*$一定也有（不一定是同一个向量），接着证明定理6.14，即Schur定理，只要$\mathsf{T}$的特征多项式split，那么存在一组标准正交基使得$\mathsf{T}$在此基下有上三角矩阵表示。下一步，如果我们真的找到了一组由$\mathsf{T}$特征向量组成的标准正交基，那么可知$\mathsf{T}$和$\mathsf{T}^*$在该组基下均有对角矩阵表示，因此可交换，受此启发，我们定义所谓normal的线性变换和矩阵，即满足$\mathsf{TT}^*=\mathsf{T}^*\mathsf{T}$的条件。定理6.15提供了normal线性变换的性质，定理6.16说明normal是复数空间V存在一组由$\mathsf{T}$特征向量组成的标准正交基的充要条件，重点是从normal可以推出一组由$\mathsf{T}$特征向量组成的标准正交基的存在性，证明用到Schur定理。但实数空间需要施加更强的限制条件，即线性变换要是self-adjoint（Hermitian）的，即满足$\mathsf{T}=\mathsf{T}^*$的条件，在实数矩阵空间上这个条件简化成对应矩阵对称。利用一个引理给出一些self-adjoint的性质：特征值必为实数、特征多项式在实空间上必split，接下来定理6.17就证明实数空间V存在一组由$\mathsf{T}$特征向量组成的标准正交基的充要条件是$\mathsf{T}$是self-adjoint。