# The adjoint of a linear operator

### Content Notes

#### Theorem 6.8

Let $\mathsf{V}$ be a finite-dimensional inner product space over $F$, and let $\mathsf{g}:\mathsf{V}\to F$ be a linear transformation. Then there exists a unique vector $y\in\mathsf{V}$ such that $\mathsf{g}(x)=\lang{x,y}\rang$ for all $x\in\mathsf{V}$​.

#### Theorem 6.9

Let $\mathsf{V}$ be a finite-dimensional inner product space, and let $\mathsf{T}$ be a linear operator on $\mathsf{V}$. Then there exists a unique function $\mathsf{T}^*:\mathsf{V}\to\mathsf{V}$ such that $\lang{\mathsf{T}(x),y}\rang=\lang{x,\mathsf{T}^*(y)}\rang$ for all $x,y\in\mathsf{V}$. Furthermore, $\mathsf{T}^*$​ is linear.

#### Definition (adjoint)

The linear operator $\mathsf{T}^*$ described in Theorem 6.9 is called the **adjoint** of the operator $\mathsf{T}$​.

#### Theorem 6.10

Let $\mathsf{V}$ be a finite-dimensional inner product space, and let $\beta$ be an orthonormal basis for $\mathsf{V}$. If $\mathsf{T}$ is a linear operator on $\mathsf{V}$, then $[\mathsf{T}^*]_{\beta}=[\mathsf{T}]^*_{\beta}$.

##### Corollary

Let $A$ be an $n\times n$ matrix. Then $\mathsf{L}_{A^*}=(\mathsf{L}_A)^*$.

#### Theorem 6.11

Let $\mathsf{V}$ be an inner product space, and let $\mathsf{T}$ and $\mathsf{U}$ be linear operators on $\mathsf{V}$. Then

(a) $(\mathsf{T}+\mathsf{U})^*=\mathsf{T}^*+\mathsf{U}^*$;

(b) $(c\mathsf{T})^*=\overline{c}\mathsf{T}^*$ for any $c\in F$.

(c) $(\mathsf{T}\mathsf{U})^*=\mathsf{U}^*\mathsf{T}^*$;

(d) $\mathsf{T}^{**}=\mathsf{T}$;

(e) $\mathsf{I}^*=\mathsf{I}$.

##### Corollary

Let $A$ and $B$ be $n\times n$ matrices. Then

(a) $(A+B)^*=A^*+B^*$;

(b) $(cA)^*=\overline{c}A^*$ for all $c\in F$;

(c) $(AB)^*=B^*A^*$;

(d) $A^{**}=A$;

(e) $I^*=I$​.

#### Lemma 1

Let $A\in\mathsf{M}_{m\times n}(F)$, $x\in\mathsf{F}^n$ and $y\in\mathsf{F}^m$. Then $\lang{Ax,y}\rang_m=\lang{x,A^*y}\rang_n$, where $\lang{x,y}\rang_n$ denote the standard inner product of $x$ and $y$ in $\mathsf{F}^n$.

#### Lemma 2

Let $A\in\mathsf{M}_{m\times n}(F)$. Then $\text{rank}(A^*A)=\text{rank}(A)$.

##### Corollary

If $A$ is an $m\times n$ matrix such that $\text{rank}(A)=n$, then $A^*A$ is invertible.

#### Theorem 6.12 (Least Squares Approximation)

Let $A\in\mathsf{M}_{m\times n}(F)$ and $y\in\mathsf{F}^m$. Then there exists $x_0\in\mathsf{F}^n$ such that $(A^*A)x_0=A^*y$ and $\|Ax_0-y\|\le\|Ax-y\|$ for all $x\in\mathsf{F}^n$. Furthermore, if $\text{rank}(A)=n$, then $x_0=(A^*A)^{-1}A^*y$.

#### Definition (Minimal Solutions to Systems of Linear equations)

A solution $s$ to $Ax=b$ is called a **minimal solution** if $\|s\|\le\|u\|$ for all other solutions $u$.

#### Theorem 6.13

Let $A\in\mathsf{M}_{m\times n}(F)$ and $b\in\mathsf{F}^m$. Suppose that $Ax=b$ is consistent. Then the following statements are true.

(a) There exists exactly one minimal solution $s$ of $Ax=b$, and $s\in\mathsf{R}(\mathsf{L}_{A^*})$.

(b) The vector $s$ is the only solution to $Ax=b$ that lies in $\mathsf{R}(\mathsf{L}_{A^*})$; that is, if $u$ satisfies $(AA^*)u=b$, then $s=A^*u$.

### Selected Exercises

#### 4

We prove (b), (c) and (e). Let $x,y\in\mathsf{V}$.

(b) Since
$$
\lang{x,(c\mathsf{T})^*(y)}\rang=\lang{c\mathsf{T}(x),y}\rang=c\lang{\mathsf{T}(x),y}\rang=c\lang{x,\mathsf{T}^*(y)}\rang=\lang{x,\overline{c}\mathsf{T}^*(y)}\rang=\lang{x,(\overline{c}\mathsf{T}^*)(y)}\rang
$$
(c) Since
$$
\lang{x,(\mathsf{TU})^*(y)}\rang=\lang{(\mathsf{TU})(x),y}\rang=\lang\mathsf{T}(\mathsf{U}(x)),y\rang=\lang{\mathsf{U}(x),\mathsf{T}^*(y)}\rang=\lang{x,\mathsf{U}^*[\mathsf{T}^*(y)]}\rang=\lang{x,(\mathsf{U^*T^*})(y)}\rang
$$
(e) Since
$$
\lang{x,\mathsf{I}^*(y)}\rang=\lang{\mathsf{I}(x),y}\rang=\lang{x,y}\rang=\lang{x,\mathsf{I}(y)}\rang
$$

#### 5

We first prove corollary to Theorem 6.11 (a)(b)(d)(e).

For (a), since $\mathsf{L}_{(A+B)^*}=(\mathsf{L}_{A+B})^*=(\mathsf{L}_A+\mathsf{L}_B)^*=(\mathsf{L}_A)^*+(\mathsf{L}_B)^*=\mathsf{L}_{A^*}+\mathsf{L}_{B^*}=\mathsf{L}_{A^*+B^*}$, we have $(A+B)^*=B^*A^*$.

For (b), since $\mathsf{L}_{(cA)^*}=(\mathsf{L}_{cA})^*=(c\mathsf{L}_A)^*=\overline{c}(\mathsf{L}_A)^*=\overline{c}\mathsf{L}_{A^*}=\mathsf{L}_{\overline{c}A^*}$, we have $(cA)^*=\overline{c}A^*$.

For (d), since $\mathsf{L}_{A^{**}}=(\mathsf{L}_{A^*})^*=(\mathsf{L}_{A})^{**}=\mathsf{L}_{A}$, we have $A^{**}=A$.

For (e), since $\mathsf{L}_{I^*}=(\mathsf{L}_{I})^*=\mathsf{I}^*=\mathsf{I}=\mathsf{L}_{I}$, we have $I^*=I$.

Next, we prove that if $A$ and $B$ are $m\times n$ matrix, then the conclusions in corollary to Theorem 6.11 still holds. Let $1\le i\le m$ and $1\le j\le n$.

For (a), since $(A+B)^*_{ji}=\overline{(A+B)_{ij}}=\overline{A_{ij}}+\overline{B_{ij}}=A^*_{ji}+B^*_{ji}=(A^*+B^*)_{ji}$, we have $(A+B)^*=B^*A^*$.

For (b), since $(cA)^*_{ji}=\overline{(cA)_{ij}}=\overline{c}\overline{A_{ij}}=\overline{c}A^*_{ji}=(\overline{c}A^*)_{ji}$, we have $(cA)^*=\overline{c}A^*$.

if $A$ is $m\times n$ matrix and $B$ is $n\times p$ matrix, then let $1\le i\le m$ and $1\le j\le p$. For (c) we have
$$
(AB)^*_{ji}=\overline{(AB)_{ij}}=\overline{\sum_{k=1}^nA_{ik}B_{kj}}=\sum_{k=1}^n\overline{A_{ik}}\overline{B_{kj}}=\sum_{k=1}^nB^*_{jk}A^*_{ki}=(B^*A^*)_{ji}
$$
For (d), let $1\le i\le m$ and $1\le j\le n$, since $(A^{**})_{ij}=\overline{A^*_{ji}}=\overline{\overline{A_{ij}}}=A_{ij}$, we have $A^{**}=A$.

The proof of (e) is omitted.

#### 6

We have
$$
(\mathsf{U}_1)^*=(\mathsf{T}+\mathsf{T}^*)^*=\mathsf{T}^*+\mathsf{T}^{**}=\mathsf{T}+\mathsf{T}^*=\mathsf{U}_1
\\
(\mathsf{U}_2)^*=(\mathsf{T}\mathsf{T}^*)^*=\mathsf{T}^{**}\mathsf{T}^*=\mathsf{T}\mathsf{T}^*=\mathsf{U}_2
$$

#### 8

That $\mathsf{T}$ is invertible means $\mathsf{T}\mathsf{T}^{-1}=\mathsf{I}$, thus
$$
\mathsf{I}=\mathsf{I}^*=(\mathsf{T}\mathsf{T}^{-1})^*=(\mathsf{T}^{-1})^*\mathsf{T}^*
$$
this means $\mathsf{T}^*$ is invertible and $(\mathsf{T}^*)^{-1}$ has the desired form.

#### 9

For any $x,y\in\mathsf{V}$, we can find $w_1,w_2\in\mathsf{W}$ and $z_1,z_2\in\mathsf{W}^{\perp}$, such that $x=w_1+z_1$ and $y=w_2+z_2$, thus
$$
\lang{\mathsf{T}(x),y}\rang=\lang{w_1,w_2+z_2}\rang=\lang{w_1,w_2}\rang=\lang{w_1,w_2}\rang+\lang{z_1,w_2}\rang=\lang{w_1+z
_1,w_2}\rang=\lang{x,\mathsf{T}(y)}\rang
$$
so we have $\lang{x,\mathsf{T}^*(y)}\rang=\lang{x,\mathsf{T}(y)}\rang$ for all $x,y$, this means $\mathsf{T}=\mathsf{T}^*$.

#### 10

First suppose $\|\mathsf{T}(x)\|=\|x\|$ for all $x\in\mathsf{V}$, then use Exercise 20 of Section 6.1, we have
$$
\lang{\mathsf{T}(x),\mathsf{T}(y)}\rang=\frac{1}{4}\sum_{k=1}^4i^k\|\mathsf{T}(x)+i^k\mathsf{T}(y)\|^2=\frac{1}{4}\sum_{k=1}^4i^k\|\mathsf{T}(x+i^ky)\|^2=\frac{1}{4}\sum_{k=1}^4i^k\|x+i^ky\|^2=\lang{x,y}\rang
$$
The other direction is obvious.

#### 11

Assume $\mathsf{T}\ne\mathsf{T}_0$, then there exists $x\in\mathsf{V}$ such that $\mathsf{T}(x)\ne0$, then
$$
0\ne\lang{\mathsf{T}(x),\mathsf{T}(x)}\rang=\lang{x,\mathsf{T}^*\mathsf{T}(x)}\rang=\lang{x,0}\rang=0
$$
which is a contradiction. If we assume $\mathsf{TT^*}=\mathsf{T}_0$, then we still have $\mathsf{T}=\mathsf{T}_0$.

#### 12

(a) Let $x\in\mathsf{N(T)}$, then for any $y\in\mathsf{R(T^*)}$, let $z\in\mathsf{V}$ such that $\mathsf{T}^*(z)=y$, we have
$$
\lang{x,y}\rang=\lang{x,\mathsf{T}^*(z)}\rang=\lang{\mathsf{T}(x),z}\rang=\lang{0,z}\rang=0\implies x\in\mathsf{R(T^*)}^{\perp}
$$
Conversely, let $v\in\mathsf{R(T^*)}^{\perp}$, then we have $\lang{v,y}\rang=0$ for any $y\in\mathsf{R(T^*)}$, let $\mathsf{T}(v)=w$ and let $y=\mathsf{T}^*(w)$, we have
$$
\lang{v,\mathsf{T}^*(w)}\rang=\lang{\mathsf{T}(v),w}\rang=\lang{w,w}\rang=0\implies w=0\implies v\in\mathsf{N(T)}
$$
(b) If $\mathsf{V}$ is finite-dimensional, then $\mathsf{N(T)}$ and $\mathsf{R(T^*)}$ are finite-dimensional, use Exercise 13(c) of Section 6.2, we have
$$
\mathsf{N(T)}^{\perp}=[\mathsf{R(T^*)}^{\perp}]^{\perp}=\mathsf{R(T^*)}
$$

#### 13

(a) We have
$$
\begin{aligned}
x\in\mathsf{N(T^*T)}&\Leftrightarrow\mathsf{T^*T}(x)=0
\\&\Leftrightarrow\lang{x,\mathsf{T^*T}(x)}\rang=0
\\&\Leftrightarrow\lang{\mathsf{T}(x),\mathsf{T}(x)}\rang=0
\\&\Leftrightarrow\mathsf{T}(x)=0
\\&\Leftrightarrow x\in\mathsf{N(T)}
\end{aligned}
$$
thus $\mathsf{N(T^*T)}=\mathsf{N(T)}$, and so $\dim(\mathsf{N(T^*T)})=\dim(\mathsf{N(T)})$, then use dimension theorem to get $\text{rank}(\mathsf{T^*T})=\text{rank}(\mathsf{T})$​.

(b) Use Exercise 12(b) we have $\text{rank}(\mathsf{T^*})=\dim(\mathsf{R(T^*)})=\dim(\mathsf{N(T)}^{\perp})$, since
$$
\dim(\mathsf{V})=\dim(\mathsf{N(T)})+\dim(\mathsf{N(T)}^{\perp})=\dim(\mathsf{N(T)})+\text{rank}(\mathsf{T})
$$
we have $\text{rank}(\mathsf{T})=\text{rank}(\mathsf{T}^*)$, then, use (a) we have
$$
\text{rank}(\mathsf{TT^*})=\text{rank}[\mathsf{(T^*)^*T^*}]=\text{rank}(\mathsf{T}^*)=\text{rank}(\mathsf{T})
$$
(c) We have 
$$
\text{rank}(\mathsf{L}_{A^*A})=\text{rank}(\mathsf{L}_{A^*}\mathsf{L}_A)=\text{rank}[(\mathsf{L}_{A})^*\mathsf{L}_{A}]=\text{rank}[\mathsf{L}_{A}(\mathsf{L}_{A})^*]=\text{rank}(\mathsf{L}_{A}\mathsf{L}_{A^*})=\text{rank}(\mathsf{L}_{AA^*})
$$
which means $\text{rank}(A^*A)=\text{rank}(AA^*)$, also we have
$$
\text{rank}(A^*A)=\text{rank}(\mathsf{L}_{A^*A})=\text{rank}(\mathsf{L}_{A^*}\mathsf{L}_A)=\text{rank}[(\mathsf{L}_{A})^*\mathsf{L}_{A}]=\text{rank}(\mathsf{L}_A)=\text{rank}(A)
$$

#### 14

To show $\mathsf{T}$ is linear, we choose any scalar $c\in F$ and $x,x'\in\mathsf{V}$, then
$$
\mathsf{T}(cx+x')=\lang{cx+x',y}\rang{z}=c\lang{x,y}\rang{z}+\lang{x',y}\rang{z}=c\mathsf{T}(x)+\mathsf{T}(x')
$$
To show $\mathsf{T}^*$ exists, notice that
$$
\lang{\mathsf{T}(x),x'}\rang=\lang{\lang{x,y}\rang{z},x'}\rang=\lang{x,y}\rang\lang{z,x'}\rang=\lang{x,\overline{\lang{z.x'}\rang}y}\rang=\lang{x,\lang{x',z}\rang{y}}\rang
$$
we can have $\mathsf{T}^*(x)=\lang{x,z}\rang{y}$.

#### 18

By definition of $\det$ and $A^*$ is the conjugate transpose of $A$, we have $\det(A^*)=\overline{\det(A^t)}=\overline{\det(A)}$.

#### 19

Write $A=(c_1,\dots,c_n)$ where each $c_i\in\mathsf{F}^m$, then $c_i\ne c_j$ for all $1\le i,j\le n$. Then
$$
A^*A=\begin{pmatrix}\overline{c_1}\\{\overline{c_2}}\\{\vdots}\\{\overline{c_n}}\end{pmatrix}\begin{pmatrix}c_1,c_2,\dots,c_n\end{pmatrix}=
\begin{pmatrix}\lang{c_1,c_1}\rang&\lang{c_1,c_2}\rang&\dots&\lang{c_1,c_n}\rang
\\
\lang{c_2,c_1}\rang&\lang{c_2,c_2}\rang&\dots&\lang{c_2,c_n}\rang
\\
{\vdots}&\vdots&&\vdots
\\
\lang{c_n,c_1}\rang&\lang{c_n,c_2}\rang&\dots&\lang{c_n,c_n}\rang
\end{pmatrix}
$$
then $A^*A$ is diagonal if and only if $\lang{c_i,c_j}\rang=0$ for $i\ne j$, or every pair of columns of $A$ is orthogonal.

#### 23

(a) For this problem we have
$$
A=\begin{pmatrix}t_1&1\\t_2&1\\{\vdots}&{\vdots}\\t_m&1\end{pmatrix},\quad x_0=(c,d),\quad y=\begin{pmatrix}y_1\\y_2\\{\vdots}\\y_m\end{pmatrix}
$$
thus the equation $(A^*A)x_0=A^*y$ can be written as
$$
(A^*A)x_0=\begin{pmatrix}t_1&\cdots&t_m\\1&\cdots&1\end{pmatrix}\begin{pmatrix}t_1&1\\t_2&1\\{\vdots}&{\vdots}\\t_m&1\end{pmatrix}(c,d)\\=
\begin{pmatrix}\sum_{i=1}^mt_i^2&\sum_{i=1}^mt_i
\\
\sum_{i=1}^mt_i&m
\end{pmatrix}(c,d)=
\begin{pmatrix}\left(\sum_{i=1}^mt_i^2\right)c+(\sum_{i=1}^mt_i)d
\\
(\sum_{i=1}^mt_i)c+md
\end{pmatrix}
\\
A^*y=\begin{pmatrix}t_1&t_2&\cdots&t_m\\1&1&\cdots&1\end{pmatrix}\begin{pmatrix}y_1\\y_2\\{\vdots}\\y_m\end{pmatrix}=
\begin{pmatrix}
\sum_{i=1}^mt_iy_i
\\
\sum_{i=1}^my_i
\end{pmatrix}
$$
which gives the desired form.

(b) From the second equation we get
$$
c\overline{t}+d=\frac{1}{m}\left(\sum_{i=1}^mt_i\right)c+d=\frac{1}{m}\left(\sum_{i=1}^my_i\right)=\overline{y}
$$

#### 24

(a) Let $\sigma_1=(a_1,a_2,\dots)$ and $\sigma_2=(b_1,b_2,\dots)$ be elements in $\mathsf{V}$, then
$$
\begin{aligned}\mathsf{T}(c\sigma_1+\sigma_2)(k)&=\sum_{i=k}^{\infty}(c\sigma_1+\sigma_2)(i)
=c\sum_{i=k}^{\infty}\sigma_1(i)+\sum_{i=k}^{\infty}\sigma_2(i)
\\&=c\mathsf{T}(\sigma_1)(k)+\mathsf{T}(\sigma_2)(k)
\end{aligned}
$$
this means $\mathsf{T}(c\sigma_1+\sigma_2)=c\mathsf{T}(\sigma_1)+\mathsf{T}(\sigma_2)$.

(b) If $n$ is a positive integer, then
$$
\mathsf{T}(e_n)(k)=\sum_{i=k}^{\infty}e_n(k)=\begin{cases}1,&k\le n\\0,&k>n\end{cases}
$$
thus $\mathsf{T}(e_n)$ has its first $n$ entires to be 1 and entries starting from position $n+1$ to be $0$, it is easy to see that $\mathsf{T}(e_n)=\sum_{i=1}^ne_i$.

(c) Assume that $\mathsf{T}^*$ exists,  choose an integer $n$, let $k$ be the largest integer such that $\mathsf{T}^*(e_n)(k)\ne0$, let $m=\max(k,n)+1$, then
$$
0=\lang{e_m,\mathsf{T}^*(e_n)}\rang=\lang{\mathsf{T}(e_m),e_n}\rang=\sum_{i=1}^m\lang{e_i,e_n}\rang=1
$$
which is a contradiction.

### Summary

这一节的目的是引入线性变换的adjoint，其类似于复数的共轭，且能够证明Tadjoint在一组标准正交基β下的矩阵是T在β下矩阵的共轭转置conjugate transpose。理解Tadjoint如何从原有的T导出是关键。定理6.8证明，任何一个线性泛函g都与V中的一个向量是一一对应的（这也是定义对偶空间的基础），这个特定向量其实是利用g在一组标准正交基下的取值作为线性组合系数得到。定理6.9说明Tadjoint的存在性、线性性和唯一性，存在性是给定y后将g定义为T(x)和y的内积，因此g是一个线性泛函，再寻找g对应的特定向量y'，作为Tadjoint作用在y上的值；线性性和唯一性则通过其满足的核心性质<T(x),y>=<x,T*(y)>来证明。有定理6.9后就可正式定义Tadjoint。定理6.10是Tadjoint的一个重要性质，即Tadjoint在一组标准正交基β下的矩阵是T在β下矩阵的共轭转置conjugate transpose。定理6.11是adjoint变换的一些其他性质，adjoint兼有转置和共轭的性质。本节后半部分提供了adjoint变换的两个具体应用：最小二乘估计和线性方程组系统的最小解。