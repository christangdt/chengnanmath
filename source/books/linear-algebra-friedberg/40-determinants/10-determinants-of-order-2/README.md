# Determinants of Order 2

### Content Notes

#### Definition

If
$$
A=\begin{pmatrix}a&b\\c&d\end{pmatrix}
$$
is a $2\times 2$ matrix with entries from a field $F$, then we define the **determinant** of $A$, denoted $\det(A)$ or $|A|$, to be the scalar $ad-bc$.

#### Theorem 4.1

The function $\det:\mathsf{M}_{2\times2}\to{F}$ is a linear function of each row of a $2\times2$ matrix when the other row is held fixed. That is, if $u,v$ and $w$ are in $\mathsf{F}^2$ and $k$ is a scalar, then
$$
\det\begin{pmatrix}u+kv\\w\end{pmatrix}=\det\begin{pmatrix}u\\w\end{pmatrix}+k\det\begin{pmatrix}v\\w\end{pmatrix}
$$
and
$$
\det\begin{pmatrix}w\\u+kv\end{pmatrix}=\det\begin{pmatrix}w\\u\end{pmatrix}+k\det\begin{pmatrix}w\\v\end{pmatrix}.
$$

#### Theorem 4.2

Let $A\in\mathsf{M}_{2\times2}(F)$. Then the determinant of $A$ is nonzero if and only if $A$ is invertible. Moreover, if $A$ is invertible, then
$$
A^{-1}=\frac{1}{\det(A)}\begin{pmatrix}A_{22}&-A_{12}\\-A_{21}&A_{11}\end{pmatrix}.
$$

### Selected Exercises

#### 5

Let $A=\begin{pmatrix}a&b\\c&d\end{pmatrix}$, then $\det(A)=ad-bc$, thus $B=\begin{pmatrix}c&d\\a&b\end{pmatrix}$ and $\det(B)=bc-ad=-\det(A)$.

#### 6

Let $A=\begin{pmatrix}a&a\\c&c\end{pmatrix}$, then $\det(A)=ac-ac=0$.

#### 7

Let $A=\begin{pmatrix}a&b\\c&d\end{pmatrix}$, then $\det(A)=ad-bc$. We have $A^t=\begin{pmatrix}a&c\\b&d\end{pmatrix}$, then $\det(A^t)=ad-bc=\det(A)$.

#### 8

Let $A=\begin{pmatrix}a&b\\0&d\end{pmatrix}$, then $\det(A)=ad-b0=ad$.

#### 9

Let $A=\begin{pmatrix}a&b\\c&d\end{pmatrix}$, then $\det(A)=ad-bc$. Let $B=\begin{pmatrix}e&f\\g&h\end{pmatrix}$, then $\det(B)=eh-fg$. We have
$$
AB=\begin{pmatrix}a&b\\c&d\end{pmatrix}\begin{pmatrix}e&f\\g&h\end{pmatrix}=\begin{pmatrix}ae+bg&af+bh\\ce+dg&cf+dh\end{pmatrix}
$$
thus
$$
\begin{aligned}\det(AB)&=(ae+bg)(cf+dh)-(af+bh)(ce+dg)
\\&=acef+adeh+bcfg+bdgh-acef-adfg-bceh-bdgh
\\&=adeh+bcfg-adfg-bceh
\\&=(ad-bc)(eh-fg)=\det(A)\cdot\det(B)
\end{aligned}
$$

#### 10

Let $A=\begin{pmatrix}a&b\\c&d\end{pmatrix}$, then $C=\begin{pmatrix}d&-b\\-c&a\end{pmatrix}$, we use this notation to prove.

(a) We have
$$
CA=\begin{pmatrix}d&-b\\-c&a\end{pmatrix}\begin{pmatrix}a&b\\c&d\end{pmatrix}=\begin{pmatrix}ad-bc&0\\0&ad-bc\end{pmatrix}=[\det(A)]I
$$
and
$$
AC=\begin{pmatrix}a&b\\c&d\end{pmatrix}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}=\begin{pmatrix}ad-bc&0\\0&ad-bc\end{pmatrix}=[\det(A)]I
$$
(b) Direct verify
$$
\det(C)=da-(-b)(-c)=ad-bc=\det(A)
$$
(c) Since $A^t=\begin{pmatrix}a&c\\b&d\end{pmatrix}$, the classical adjoint of $A^t$ is $\begin{pmatrix}d&-c\\-b&a\end{pmatrix}$, which is $C^t$.

(d) $A$ is invertible means $\det(A)\ne0$, use (a) we have
$$
\frac{1}{\det(A)}CA=A\left(\frac{1}{\det(A)}C\right)=I
$$

#### 11

Let $A=\begin{pmatrix}a&b\\c&d\end{pmatrix}$ be any element in $\mathsf{M}_{2\times2}(F)$. We need to calculate $\delta(A)$. First we have
$$
\begin{aligned}0=\delta\begin{pmatrix}1&1\\1&1\end{pmatrix}&=\delta\begin{pmatrix}1&0\\1&1\end{pmatrix}+\delta\begin{pmatrix}0&1\\1&1\end{pmatrix}
\\&=\delta\begin{pmatrix}1&0\\1&0\end{pmatrix}+\delta\begin{pmatrix}1&0\\0&1\end{pmatrix}+\delta\begin{pmatrix}0&1\\1&0\end{pmatrix}+\delta\begin{pmatrix}0&1\\0&1\end{pmatrix}
\\&=1+\delta\begin{pmatrix}0&1\\1&0\end{pmatrix}
\end{aligned}
$$
which gives $\delta\begin{pmatrix}0&1\\1&0\end{pmatrix}=-1$, similarly we have
$$
\begin{aligned}\delta\begin{pmatrix}a&b\\c&d\end{pmatrix}&=a\delta\begin{pmatrix}1&0\\c&d\end{pmatrix}+b\delta\begin{pmatrix}0&1\\c&d\end{pmatrix}
\\&=a\left[c\delta\begin{pmatrix}1&0\\1&0\end{pmatrix}+d\delta\begin{pmatrix}1&0\\0&1\end{pmatrix}\right]+b\left[c\delta\begin{pmatrix}0&1\\1&0\end{pmatrix}+d\delta\begin{pmatrix}0&1\\0&1\end{pmatrix}\right]
\\&=ad\delta\begin{pmatrix}1&0\\0&1\end{pmatrix}+bc\delta\begin{pmatrix}0&1\\1&0\end{pmatrix}=ad-bc
\end{aligned}
$$
