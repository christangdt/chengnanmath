# The Gram-Schmidt Orthogonalization Process and Orthogonal Complements

### Content Notes

#### Definition (orthonormal basis)

Let $\mathsf{V}$ be an inner product space. A subset of $\mathsf{V}$ is an **orthonormal basis** for $\mathsf{V}$ if it is an ordered basis that is orthonormal.

#### Theorem 6.3

Let $\mathsf{V}$ be an inner product space and $S=\{v_1,v_2,\dots,v_k\}$ be an orthogonal subset of $\mathsf{V}$ consisting of nonzero vectors. If $y\in\text{span}(S)$, then
$$
y=\sum_{i=1}^k\frac{\lang{y,v_i}\rang}{\|v_i\|^2}v_i.
$$

##### Corollary 1

If, in addition to the hypothesis of Theorem 6.3, $S$ is orthonormal and $y\in\text{span}(S)$, then $y=\sum_{i=1}^k\lang{y,v_i}\rang v_i$.

##### Corollary 2

Let $\mathsf{V}$ be an inner product space, and let $S$ be an orthogonal subset of $\mathsf{V}$ consisting of nonzero vectors. Then $S$ is linearly independent.

#### Theorem 6.4

Let $\mathsf{V}$ be an inner product space and $S=\{w_1,w_2,\dots,w_n\}$ be a linearly independent subset of $\mathsf{V}$. Define $S'=\{v_1,v_2,\dots,v_n\}$, where $v_1=w_1$ and
$$
v_k=w_k-\sum_{j=1}^{k-1}\frac{\lang{w_k,v_j}\rang}{\|v_j\|^2}v_i\quad\text{for }2\le k\le n.
$$
Then $S'$ is an orthogonal set of nonzero vectors such that $\text{span}(S')=\text{span}(S)$.

The construction of $\{v_1,v_2,\dots,v_n\}$ by the use of Theorem 6.4 is called the **Gram-Schmidt process**.

#### Theorem 6.5

Let $\mathsf{V}$ be a nonzero finite-dimensional inner product space. Then $\mathsf{V}$ has an orthonormal basis $\beta$. Furthermore, if $\beta=\{v_1,v_2,\dots,v_n\}$ and $x\in\mathsf{V}$, then
$$
x=\sum_{i=1}^n\lang{x,v_i}\rang v_i
$$

##### Corollary

Let $\mathsf{V}$ be a finite-dimensional inner product space with an orthonormal basis $\beta=\{v_1,v_2,\dots,v_n\}$. Let $\mathsf{T}$ be a linear operator on $\mathsf{V}$, and let $A=[\mathsf{T}]_{\beta}$. Then for any $i$ and $j$, $A_{ij}=\lang{\mathsf{T}(v_j),v_i}\rang$​.

#### Definition (Fourier coefficients)

Let $\beta$ be an orthonormal subset (possibly infinite) of an inner product space $\mathsf{V}$, and let $x\in\mathsf{V}$. We define the **Fourier coefficients** of $x$ relative to $\beta$ to be the scalars $\lang{x,y}\rang$, where $y\in\beta$.

#### Definition (orthogonal complement)

Let $S$ be a nonempty subset of an inner product space $\mathsf{V}$. We define $S^{\perp}$ to be the set of all vectors in $\mathsf{V}$ that are orthogonal to every vector in $S$; that is, $S^{\perp}=\{x\in\mathsf{V}:\lang{x,y}\rang=0\text{ for all }y\in S\}$. The set $S^{\perp}$ is called the **orthogonal complement** of $S$.

#### Theorem 6.6

Let $W$ be a finite-dimensional subspace of an inner product space $\mathsf{V}$, and let $y\in\mathsf{V}$. Then there exist unique vectors $u\in\mathsf{W}$ and $z\in\mathsf{W}^{\perp}$ such that $y=u+z$. Furthermore, if $\{v_1,v_2,\dots,v_k\}$ is an orthonormal basis for $\mathsf{W}$, then
$$
u=\sum_{i=1}^k\lang{y,v_i}\rang v_i.
$$

##### Corollary

In the notation of Theorem 6.6, the vector $u$ is the unique vector in $\mathsf{W}$ that is "closest" to $y$; that is, for any $x\in\mathsf{W}$, $\|y-x\|\ge\|y-u\|$, and this inequality is an equality if and only if $x=u$. The vector $u$ is called the **orthogonal projection** of $y$ on $\mathsf{W}$.

#### Theorem 6.7

Suppose that $S=\{v_1,v_2,\dots,v_k\}$ is an orthonormal set in an $n$-dimensional inner product space $\mathsf{V}$. Then

(a) $S$ can be extended to an orthonormal basis $\{v_1,v_2,\dots,v_k,v_{k+1},\dots,v_n\}$ for $\mathsf{V}$.

(b) If $W=\text{span}(S)$, then $S_1=\{v_{k+1},v_{k+2},\dots,v_n\}$ is an orthonormal basis for $\mathsf{W}^{\perp}$.

(c) If $W$ is any subspace of $\mathsf{V}$, then $\dim(\mathsf{V})=\dim(\mathsf{W})+\dim(\mathsf{W}^{\perp})$​.

### Selected Exercises

#### 6

By Theorem 6.6, we can write $x=u+y$, where $u\in\mathsf{W}$ and $y\in\mathsf{W}^{\perp}$, since $x\notin\mathsf{W}$, we have $y\ne0$, and
$$
\lang{x,y}\rang=\lang{u,y}\rang+\lang{y,y}\rang=\lang{y,y}\rang\ne0
$$

#### 7

First suppose $z\in\mathsf{W}^{\perp}$, then $\lang{z,v}\rang=0$ for every $v\in\beta$ since $v\in\mathsf{W}$. Conversely, given any $w\in\mathsf{W}$, we can write $w=\sum_ia_iv_i$ with $v_i\in\beta$, then $\lang{w,z}\rang=\sum_ia_i\lang{v_i,z}\rang=\sum_ia_i\overline{\lang{z,v_i}\rang}=0$, this means $z\in\mathsf{W}^{\perp}$.

#### 8

Use mathematical induction, we already have $v_1=w_1$ in the Gram-Schmidt process. Now suppose the conclusion is true for orthogonal set consisting of $k-1$ vectors, consider the orthogonal set $\{w_1,\dots,w_k\}$, then use the induction hypothesis we have $v_i=w_i$ for $i=1,\dots,k-1$, and since $\lang{w_k,w_j}\rang=0$ for $j=1,\dots,k-1$, we have
$$
v_k=w_k-\sum_{j=1}^{k-1}\frac{\lang{w_k,v_j}\rang}{\|v_j\|^2}v_i=w_k-\sum_{j=1}^{k-1}\frac{\lang{w_k,w_j}\rang}{\|w_j\|^2}w_i=w_k
$$

#### 10

With the help of Theorem 6.6, for any $y\in\mathsf{V}$, there exist unique vectors $u\in\mathsf{W}$ and $z\in\mathsf{W}^{\perp}$ such that $y=u+z$, thus we can define $\mathsf{T}(y)=u$ for $y\in\mathsf{V}$.

To prove $\mathsf{T}$ is a projection on $\mathsf{W}$ along $\mathsf{W}^{\perp}$, we need to prove $\mathsf{T}$ is linear, let $y,y'\in\mathsf{V}$, then we have $y=u+z$ and $y'=u'+z'$ with unique $u,u'\in\mathsf{W}$ and $z,z'\in\mathsf{W}^{\perp}$, then for $cy+y'=cu+u'+cz+z'$, we can easily see $cu+u'\in\mathsf{W}$ and $cz+z'\in\mathsf{W}^{\perp}$, thus $\mathsf{T}(cy+y')=cu+u'$.

To see $\mathsf{N(T)}=\mathsf{W}^{\perp}$, it is easy to see that $\mathsf{W}^{\perp}\subseteq\mathsf{N(T)}$, if $v\in\mathsf{N(T)}$, write $v=u+z$ with $u\in\mathsf{W}$ and $z\in\mathsf{W}^{\perp}$, we have $\mathsf{T}(v)=u=0$, thus $v=z\in\mathsf{W}^{\perp}$.

To see $\|\mathsf{T}(x)\|\le\|x\|$ for all $x\in\mathsf{V}$, we see there exist unique vectors $u\in\mathsf{W}$ and $z\in\mathsf{W}^{\perp}$ such that $x=u+z$, thus
$$
\|\mathsf{T}(x)\|^2=\|u\|^2=\|u+z\|^2-\|z\|^2=\|x\|^2-\|z\|^2\le\|x\|^2
$$

#### 11

Let the rows of $A$ be $\alpha_1,\dots,\alpha_n$, then it is easy to see that $(AA^*)_{ij}=\lang{\alpha_i,\alpha_j}\rang$, so $AA^*=I$ is equivalent to $\lang{\alpha_i,\alpha_j}\rang=\delta_{ij}$, which is equivalent to $\{\alpha_1,\dots,\alpha_n\}$ being orthonormal.

#### 12

Let $x\in\mathsf{F}^n$, then
$$
\begin{aligned}
x\in[\mathsf{R}(\mathsf{L}_{A^*})]^{\perp}&\Leftrightarrow\lang{x,y}\rang=0,\quad\forall y\in\mathsf{R}(\mathsf{L}_{A^*})
\\&\Leftrightarrow\lang{x,A^*z}\rang=0,\quad\forall z\in\mathsf{F}^m
\\&\Leftrightarrow\lang{Ax,z}\rang=0,\quad\forall z\in\mathsf{F}^m
\\&\Leftrightarrow\mathsf{L}_A(x)=Ax=0
\\&\Leftrightarrow x\in\mathsf{N}(\mathsf{L}_A)
\end{aligned}
$$

#### 13

(a) $v\in S^{\perp}$ means $\lang{v,s}\rang=0$ for all $s\in S$, which means $\lang{v,s}\rang=0$ for all $s\in S_0$, which means $v\in S_0^{\perp}$.

(b) If $s\in S$, choose any $v\in S^{\perp}$, we have $\lang{v,s}\rang=0$, thus $s\in(S^{\perp})^{\perp}$, the next conclusion follows from $(S^{\perp})^{\perp}$ itself a subspace, and $\text{span}(S)$ is contained in any subspace that contains $S$.

(c) Use (b) we can get $\mathsf{W}\subseteq(\mathsf{W}^{\perp})^{\perp}$, to prove the converse inclusion, let $x\in(\mathsf{W}^{\perp})^{\perp}$ but $x\notin\mathsf{W}$, then Exercise 6 shows that there exists $y\in\mathsf{W}^{\perp}$ such that $\lang{x,y}\rang\ne0$, this contradicts $x\in(\mathsf{W}^{\perp})^{\perp}$.

(d) We already have Theorem 6.7(c), let $x\in\mathsf{W}\cap\mathsf{W}^{\perp}$, then $\lang{x,x}\rang=0$ while the first $x$ is considered elements in $\mathsf{W}$ and the second $x$ is considered elements in $\mathsf{W}^{\perp}$, this means $x=0$.

#### 14

If $v\in(\mathsf{W}_1+\mathsf{W}_2)^{\perp}$, then $\lang{v,w}\rang=0$ for any $w\in\mathsf{W}_1+\mathsf{W}_2$, this means $\lang{v,w}\rang=0$ for any $w_1\in\mathsf{W}_1$ and any $w_2\in\mathsf{W}_2$, since $\mathsf{W}_1\subseteq\mathsf{W}_1+\mathsf{W}_2$ and $\mathsf{W}_2\subseteq\mathsf{W}_1+\mathsf{W}_2$. Thus we have $v\in\mathsf{W}_1^{\perp}\cap\mathsf{W}_2^{\perp}$. Conversely, we have
$$
\begin{aligned}
v\in\mathsf{W}_1^{\perp}\cap\mathsf{W}_2^{\perp}&\implies(\lang{v,w_1}\rang=0,\forall w_1\in\mathsf{W}_1)\wedge(\lang{v,w_2}\rang=0,\forall w_2\in\mathsf{W}_2)
\\&\implies\lang{v,w}\rang=\lang{v,w_1}\rang+\lang{v,w_2}\rang=0,\forall w=w_1+w_2\in\mathsf{W}_1+\mathsf{W}_2
\\&\implies v\in(\mathsf{W}_1+\mathsf{W}_2)^{\perp}
\end{aligned}
$$
For the second equation, we use Exercise 13(c) to get
$$
\mathsf{W}_1^{\perp}+\mathsf{W}_2^{\perp}=[(\mathsf{W}_1^{\perp}+\mathsf{W}_2^{\perp})^{\perp}]^{\perp}=[(\mathsf{W}_1^{\perp})^{\perp}\cap(\mathsf{W}_2^{\perp})^{\perp}]^{\perp}=(\mathsf{W}_1\cap\mathsf{W}_2)^{\perp}
$$

#### 15

(a) By Theorem 6.5, we can write $x=\sum_{i=1}^n\lang{x,v_i}\rang v_i$ and $y=\sum_{i=1}^n\lang{y,v_i}\rang v_i$, then
$$
\begin{aligned}
\lang{x,y}\rang&=\Big<{\sum_{i=1}^n\lang{x,v_i}\rang v_i,\sum_{i=1}^n\lang{y,v_i}\rang v_i}\Big>\\&=\sum_{i=1}^n\lang{x,v_i}\rang\lang v_i,\lang{y,v_1}\rang v_1+\cdots+\lang{y,v_n}\rang v_n\rang\\&=\sum_{i=1}^n\lang{x,v_i}\rang\overline{\lang{y,v_i}\rang}
\end{aligned}
$$
(b) Suppose $\beta=\{v_1,v_2,\dots,v_n\}$, then we have $\phi_{\beta}(x)=(\lang{x,v_1}\rang,\dots,\lang{x,v_n}\rang)$ and $\phi_{\beta}(y)=(\lang{y,v_1}\rang,\dots,\lang{y,v_n}\rang)$, and the conclusion is obvious.

#### 16

(a) Let $\mathsf{W}=\text{span}(S)$, then $x\in\mathsf{V}$ can be written as $x=u+z$ with $u\in\mathsf{W}$ and $z\in\mathsf{W}^{\perp}$, also $u=\sum_{i=1}^n\lang{x,v_i}\rang v_i$, thus we have
$$
\begin{aligned}
\|x\|^2&=\|u+z\|^2=\|u\|^2+\|z\|^2\ge\|u\|^2\\&=\Big<\sum_{i=1}^n\lang{x,v_i}\rang v_i,\sum_{i=1}^n\lang{x,v_i}\rang v_i\Big>
\\&=\sum_{i=1}^n\lang{x,v_i}\rang\overline{\lang{x,v_i}\rang}=\sum_{i=1}^n|\lang{x,v_i}\rang|^2
\end{aligned}
$$
(b) The inequality is an equality if and only if $z=0$ above, that is $x=u\in\mathsf{W}$.

#### 17

For all $x\in\mathsf{V}$, let $y=\mathsf{T}(x)$, then $\lang{\mathsf{T}(x),y}\rang=0$ gives $\mathsf{T}(x)=0$, thus $\mathsf{T}=\mathsf{T}_0$.

#### 18

Let $f$ be an odd function, then given any $g\in\mathsf{W}_e$, we have $fg$ an odd function, thus $\lang{f,g}\rang=0$, so $f\in(\mathsf{W}_e)^{\perp}$. Conversely, suppose $f\in(\mathsf{W}_e)^{\perp}$, let $F(t)=f(t)+f(-t)$, then $F\in\mathsf{V}$ and in addition $F$ is an even function, thus we have
$$
\lang{f,F}\rang=\int_{-1}^1f(t)[f(-t)+f(t)]dt=0
$$
let $u=-t$ we can get
$$
\int_1^{-1}f(-u)[f(u)+f(-u)]d(-u)=\int_{-1}^1f(-u)[f(u)+f(-u)]du=0
$$
add the two integrals together, we get
$$
\int_{-1}^1[f(t)+f(-t)][f(t)+f(-t)]dt=\lang{F,F}\rang=0\implies F=0
$$
thus $f(t)+f(-t)=0$ on $[-1,1]$, this means $f\in\mathsf{W}_o$.

#### 23

(a) The first three conditions are easy to verify, for the last condition, we have $\lang{\sigma,\sigma}\rang=\sum_{n=1}^{\infty}|\sigma(n)|^2$, thus if $\sigma\ne0$, at least one $\sigma(n)\ne0$, which means $\lang{\sigma,\sigma}\rang\ne0$.

(b) Since $\lang{e_i,e_j}\rang=\sum_{k=1}^{\infty}e_i(k)\overline{e_j(k)}=\sum_{k=1}^{\infty}\delta_{i,k}\delta_{j,k}$, it is easy to see that $\lang{e_i,e_j}\rang=0$ when $i\ne j$, if $i=j$, then $\lang{e_i,e_j}\rang=\delta_{i,i}\delta_{i,i}=1$.

(c) If assume $e_1\in\mathsf{W}$, then we have $e_1=\sum_{n=2}^{\infty}c_n\sigma_n$ for scalars $c_i\in F$, then
$$
\begin{aligned}
e_1=\sum_{n=2}^{\infty}c_n(e_1+e_n)&\implies\left(\sum_{n=2}^{\infty}c_n-1\right)e_1+\sum_{n=2}^{\infty}c_ne_n=0\\&\implies\left(\sum_{n=2}^{\infty}c_n=1\right)\wedge(c_i=0,i\ge2)
\end{aligned}
$$
this is a contradiction. Thus $e_1\notin\mathsf{W}$.

If $\sigma\in\mathsf{W}^{\perp}$, then $\lang{\sigma,\sigma_n}\rang=0$ for all $n\ge2$, which we yield $\sigma(1)+\sigma(n)=0$ for all $n\ge2$, this means $\sigma$ has the form
$$
\sigma=(\sigma(1),-\sigma(1),-\sigma(1),\dots)
$$
If $\sigma(1)\ne0$, then $\sigma\notin\mathsf{V}$, thus we must have $\sigma(1)=0$, but this means $\sigma=0$. Thus $\mathsf{W}^{\perp}=\{0\}$, whence $(\mathsf{W}^{\perp})^{\perp}=\mathsf{V}$, which is not equal to $\mathsf{W}$​.

### Summary

本节包括两部分内容，第一部分Gram-Schmidt正交化过程主要讨论如何得到一组标准正交基。首先定义什么是标准正交基，即两两正交、模长为1的向量组成的基。定理6.3说明正交向量组的作用：表示任意向量线性组合的系数非常便利，如果是标准正交向量组，则线性组合系数表示能进一步化简（推论1），且正交的向量组一定线性无关（推论2）。定理6.4是Gram-Schmidt正交化的具体过程和算法。定理6.5说明有限维空间一定有一组标准正交基，且任意向量都可以用Fourier系数表示成该标准正交基的线性组合。其推论是标准正交基下的矩阵表示可以很简单的用内积算出。第二部分是垂直补集，是针对内积空间V的某一个子集定义的，一般而言讨论的是子空间的垂直补。定理6.6说明某一子空间和垂直补可以用来分解任一给定向量，并引出投影的概念（推论）。定理6.7是垂直补集和标准正交基综合起来的一些性质，包括任意标准正交集合能够扩展为一组标准正交基，扩展过程中自然形成一个子空间（原有标准正交集合的span）和该子空间的垂直补（为扩展而新增的基向量集合的span），同时V的维数正是二者维数之和。