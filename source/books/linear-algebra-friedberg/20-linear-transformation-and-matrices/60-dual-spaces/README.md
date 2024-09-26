# Dual Spaces

### Content Notes

linear transformations from a vector space $\mathsf{V}$ into its field of scalars $F$ is called a **linear functional** on $\mathsf{V}$, we use the letters $\mathsf{f,g,h},\dots$​ to denote linear functionals.

#### Examples

The function $h:\mathsf{V}\to R$ defined by
$$
h(x)=\frac{1}{2\pi}\int_0^{2\pi}x(t)g(t)dt
$$
is called the **$n$th Fourier coefficient of** $x$.

Let $\mathsf{V}$ be finite-dimensional, let $\beta=\{x_1,\dots,x_n\}$ be an ordered basis for $\mathsf{V}$. Define $\mathsf{f}_i(x)=a_i$ where $[x]_{\beta}=(a_1,\dots,a_n)^t$ is the coordinate vector of $x$ relative to $\beta$. Then $\mathsf{f}_i$ is a linear functional on $\mathsf{V}$ called the **$i$th coordinate function with respect to the basis** $\beta$. Note that $\mathsf{f}_i(x_j)=\delta_{ij}$.

#### Definition (dual space)

For a vector space $\mathsf{V}$ over $F$, we define the **dual space** of $\mathsf{V}$ to be the vector space $\mathcal{L}(\mathsf{V},F)$, denoted by $\mathsf{V}^*$. We also define the **double dual** $\mathsf{V}^{**}$ of $\mathsf{V}$ to be the dual of $\mathsf{V}^*$​.

#### Theorem 2.24

Suppose $\mathsf{V}$ is a finite-dimensional vector space with the ordered basis $\beta=\{x_1,\dots,x_n\}$. Let $\mathsf{f}_i(1\le i\le n)$ be the $i$th coordinate function with respect to $\beta$ as defined above, and let $\beta^*=\{\mathsf{f}_1,\cdots,\mathsf{f}_n\}$. Then $\beta^*$ is an ordered basis for $\mathsf{V}^*$, and for any $\mathsf{f}\in\mathsf{V}^*$, we have $\mathsf{f}=\sum_{i=1}^n\mathsf{f}(x_i)\mathsf{f}_i$.

#### Definition (dual basis)

Using the notation of Theorem 2.24, we call the ordered basis $\beta^*=\{\mathsf{f}_1,\cdots,\mathsf{f}_n\}$ of $\mathsf{V}^*$ that satisfies $\mathsf{f}_i(x_j)=\delta_{ij}\quad(1\le i,j\le n)$ the **dual basis** of $\beta$.

#### Theorem 2.25

Let $\mathsf{V}$ and $\mathsf{W}$ be finite-dimensional vector spaces over $F$ with ordered bases $\beta$ and $\gamma$, respectively. For any linear transformation $\mathsf{T:V\to W}$, the mapping $\mathsf{T}^t:\mathsf{W}^*\to\mathsf{V}^*$ defined by $\mathsf{T}^t(g)=g\mathsf{T}$ for all $g\in\mathsf{W}^*$ is a linear transformation with the property that $[\mathsf{T}^t]_{\gamma^*}^{\beta^*}=([\mathsf{T}]_{\beta}^{\gamma})^t$.

The linear transformation $\mathsf{T}^t$ is called the **transpose** of $\mathsf{T}$.

#### Lemma

Let $\mathsf{V}$ be a finite-dimensional vector space, and let $x\in\mathsf{V}$. Define $\widehat{x}:\mathsf{V}^*\to F$ by $\widehat{x}(\mathsf{f})=\mathsf{f}(x),\mathsf{f}\in\mathsf{V}^*$. Then $\widehat{x}\in\mathsf{V}^{**}$. If $\widehat{x}(\mathsf{f})=0$ for all $\mathsf{f}\in\mathsf{V}^*$, then $x=0$.

#### Theorem 2.26

Let  $\mathsf{V}$ be a finite-dimensional vector space, and define $\psi:\mathsf{V}\to\mathsf{V}^{**}$ by $\psi(x)=\widehat{x}$. Then $\psi$​ is an isomorphism.

##### Corollary

Let $\mathsf{V}$ be a finite-dimensional vector space with dual space $\mathsf{V}^{*}$. Then every ordered basis for $\mathsf{V}^*$ is the dual basis for some basis for $\mathsf{V}$.

### Selected Exercises

#### 3

(b) $\beta^*=\{\mathsf{f}_1,\mathsf{f}_2,\mathsf{f}_3\}$ ，where
$$
\mathsf{f}_1(ax^2+bx+c)=c, \mathsf{f}_2(ax^2+bx+c)=b,\mathsf{f}_3(ax^2+bx+c)=a
$$

#### 4

Suppose $c_1\mathsf{f}_1+c_2\mathsf{f}_2+c_3\mathsf{f}_3=0$, which means for any $(x,y,z)\in\mathsf{R}^3$ we have
$$
\begin{aligned}
0&=(c_1\mathsf{f}_1+c_2\mathsf{f}_2+c_3\mathsf{f}_3)(x,y,z)=c_1\mathsf{f}_1(x,y,z)+c_2\mathsf{f}_2(x,y,z)+c_3\mathsf{f}_3(x,y,z)
\\&=c_1(x-2y)+c_2(x+y+z)+c_3(y-3z)
\\&=(c_1+c_2)x+(-2c_1+c_2+c_3)y+(c_2-3c_3)z
\end{aligned}
$$
this gives the system of equations
$$
\begin{cases}
c_1+c_2=0
\\
c_2+c_3-2c_1=0
\\
c_2-3c_3=0
\end{cases}\implies\begin{cases}c_1=0\\c_2=0\\c_3=0\end{cases}
$$
thus $\{\mathsf{f}_1,\mathsf{f}_2,\mathsf{f}_3\}$ is linearly independent, thus a basis for $\mathsf{V}^*$. To find a basis for $\mathsf{V}$ for which it is the dual basis, we let $\beta=\{\beta_1,\beta_2,\beta_3\}$ where each $\beta_i=(x_i,y_i,z_i)$ satisfy the equation $\mathsf{f}_i(\beta_j)=\delta_{ij}$ for $1\le i,j\le3$. So we solve
$$
\begin{cases}
\mathsf{f}_1(x,y,z)=x-2y=1
\\
\mathsf{f}_2(x,y,z)=x+y+z=0
\\
\mathsf{f}_3(x,y,z)=y-3z=0
\end{cases}\implies\begin{cases}x_1=0.4\\y_1=-0.3\\z_1=-0.1\end{cases}
$$
Thus $\beta_1=(0.4,-0.3,-0.1)$, similarly we get $\beta_2=(0.6,0.3,0.1)$ and $\beta_3=(0.2,0.1,-0.3)$.

#### 6

(a) By definition
$$
\mathsf{T}^t(\mathsf{f})(x,y)=\mathsf{f}\mathsf{T}(x,y)=\mathsf{f}(3x+2y,x)=2(3x+2y)+x=7x+4y
$$
(b) It is easy to see $\mathsf{f}_1(x,y)=x,\mathsf{f}_2(x,y)=y$. Then
$$
\mathsf{T}^t(\mathsf{f}_1)(x,y)=\mathsf{f}_1(3x+2y,x)=3x+2y=3\mathsf{f}_1(x,y)+2\mathsf{f}_2(x,y)
\\
\mathsf{T}^t(\mathsf{f}_2)(x,y)=\mathsf{f}_2(3x+2y,x)=x=\mathsf{f}_1(x,y)
$$
thus, we can see that $[\mathsf{T}^t]_{\beta^*}=\begin{pmatrix}3&1\\2&0\end{pmatrix}$.

(c) To compute $[\mathsf{T}]_{\beta}$, we have
$$
\mathsf{T}(\beta_1)=\mathsf{T}(1,0)=(3,1)=3\beta_1+\beta_2,\quad \mathsf{T}(\beta_2)=\mathsf{T}(0,1)=(2,0)=2\beta_1
$$
which gives $[\mathsf{T}]_{\beta}=\begin{pmatrix}3&2\\1&0\end{pmatrix}$, we can see that $([\mathsf{T}]_{\beta})^t=[\mathsf{T}^t]_{\beta^*}$.

#### 8

Use the plane equation in Chapter 1, every plane through the origin in $\mathsf{R}^3$ can be written in the form
$$
x=su+tv,\quad u,v\in\mathsf{R}^3
$$
in addition, the vectors $u$ and $v$ are not parallel, thus linearly independent, which means we can add a new vector $w\in\mathsf{R}^3$ such that $\beta=\{u,v,w\}$ is a basis for $\mathsf{R}^3$, choose its dual basis $\beta^*=\{\mathsf{f}_u,\mathsf{f}_v,\mathsf{f}_w\}$, then
$$
\mathsf{f}_w(u)=\mathsf{f}_w(v)=0\implies\mathsf{f}_w(su+tv)=s\mathsf{f}_w(u)+t\mathsf{f}_w(v)=0
$$
so the plane is the null space of $\mathsf{f}_w$.

An analogous result for $\mathsf{R}^2$ is: every line through the origin in $\mathsf{R}^2$ may be identified with the null space of a vector in $(\mathsf{R}^2)^*$.

#### 9

If $\mathsf{T}$ is linear, let $\{\mathsf{g}_1,\mathsf{g}_2,\dots,\mathsf{g}_m\}$ be the dual basis of the standard ordered basis $\beta=\{\beta_1,\dots,\beta_m\}$ for $\mathsf{F}^m$, define $\mathsf{f}_i(x)=\mathsf{T}^t(\mathsf{g}_i)=(\mathsf{g}_i\mathsf{T})(x)$ for $1\le i\le m$, then each $\mathsf{f}_i\in(\mathsf{F}^n)^*$, and let $\mathsf{T}(x)=(x_1,\dots,x_m)$ for $x\in\mathsf{F}^n$, then we have
$$
x_i=\mathsf{g}_i(x_1,\dots,x_m)=\mathsf{g}_i(\mathsf{T}(x))=\mathsf{f}_i(x),\quad 1\le i\le m
$$
The other direction is easy to prove.

#### 10

(a) If we have $a_0\mathsf{f}_0+\cdots+a_n\mathsf{f}_n=0$, then let $p(x)=(x-c_1)\cdots(x-c_n)$ and we have
$$
0=(a_0\mathsf{f}_0+\cdots+a_n\mathsf{f}_n)(p(x))=a_0p(c_0)+\cdots+a_np(c_n)=a_0p(c_0)\implies a_0=0
$$
similarly, let $p(x)=(x-c_0)\cdots(x-c_{i-1})(x-c_{i+1})\cdots(x-c_n)$ and we can get $a_i=0$, eventually we have $a_0=\cdots=a_n=0$, thus the set $\{\mathsf{f}_0,\dots,\mathsf{f}_n\}$ is linearly independent, thus a basis for $\mathsf{V}^*$.

(b) Use the corollary to Theorem 2.26, since $\{\mathsf{f}_0,\dots,\mathsf{f}_n\}$ is a basis for $\mathsf{V}^*$, there exists a basis $\{p_0,p_1,\dots,p_n\}$ for $\mathsf{V}$ such that $\{\mathsf{f}_0,\dots,\mathsf{f}_n\}$ is the dual basis for it. Thus $\mathsf{f}_j(p_i(x))=p_i(c_j)=\delta_{ij}$ for $0\le i\le n$​.

(c) Let $q(x)=\sum_{i=0}^na_ip_i(x)$, then $\deg(q)\le n$ and $q(c_j)=\sum_{i=0}^na_i\delta_{ij}=a_j$ for $0\le j\le n$. Assume there exists another polynomial $q'(x)$ of degree at most $n$ such that $q(c_i)=a_i$ for $0\le i\le n$, then $q'(x)\in\mathsf{V}$ and we can use the basis $\{p_0,p_1,\dots,p_n\}$ for $\mathsf{V}$ to express $q'(x)$ as $q'(x)=\sum_{i=0}^nb_ip_i(x)$ for $b_0,\dots,b_n\in R$, then it is easy to see that $b_i=a_i$ and so $q'=q$.

(d) For $p(x)\in\mathsf{V}$, let $a_i=p(c_i)$ for $0\le i\le n$, then use (c) we have the result.

(e) Since $p$ is a polynomial we can have
$$
\int_a^bp(t)dt=\int_a^b\left(\sum_{i=0}^np(c_i)p_i(t)\right)dt=\sum_{i=0}^np(c_i)\int_a^bp_i(t)dt=\sum_{i=0}^np(c_i)d_i
$$

#### 11

The diagram is the key to prove this exercise, i.e. Figure 2.6
$$
\quad\mathsf{V}\stackrel{\mathsf{T}}{\longrightarrow}\mathsf{W}\quad\\
{\psi_1}\downarrow\quad\qquad\downarrow{\psi_2}
\\
\quad{\mathsf{V}^{**}}\stackrel{\mathsf{T}^{tt}}{\longrightarrow}{\mathsf{W}^{**}}
$$
Let $\beta=\{v_1,\dots,v_n\}$ be an ordered basis for $\mathsf{V}$, let $\gamma=\{w_1,\dots,w_m\}$ be an ordered basis for $\mathsf{W}$ and its dual basis in $\mathsf{W}^*$ to be $\gamma^*=\{\mathsf{g}_1,\dots,\mathsf{g}_m\}$, we prove $\psi_2\mathsf{T}=\mathsf{T}^{tt}\psi_1$ by showing that $\psi_2\mathsf{T}(v_i)=\mathsf{T}^{tt}\psi_1(v_i)$ for $1\le i\le n$, then the conclusion follows from corollary to Theorem 2.6. 

Now we choose one fixed $1\le i\le n$, if we denote the matrix $A=[\mathsf{T}]_{\beta}^{\gamma}$, then we have $\mathsf{T}(v_i)=\sum_{j=1}^mA_{ji}w_j$, thus
$$
\psi_2\mathsf{T}(v_i)=\psi_2\left(\sum_{j=1}^mA_{ji}w_j\right)=\sum_{j=1}^mA_{ji}\psi_2(w_j)=\sum_{j=1}^mA_{ji}\widehat{w_j}\in\mathsf{W}^{**}
$$
and
$$
\mathsf{T}^{tt}\psi_1(v_i)=\mathsf{T}^{tt}(\widehat{v_i})=\widehat{v_i}\mathsf{T}^t\in\mathsf{W}^{**}
$$
To prove the two elements are equal in $\mathsf{W}^{**}$, we need to show for any vector $\mathsf{g}$ in $\mathsf{W}^*$, each element, when functioned on $\mathsf{g}$, produces the same scalar in $F$. Since $\gamma^*$ is a basis for $\mathsf{W}^*$, we only need to prove each element produces the same scalar in $F$ when functioned on each vector $\mathsf{g}_k$ in  $\gamma^*$. Now for $1\le k\le m$ we have
$$
\sum_{j=1}^mA_{ji}\widehat{w_j}(\mathsf{g}_k)=\sum_{j=1}^mA_{ji}\mathsf{g}_k(w_j)=A_{ki}\mathsf{g}_k(w_k)=A_{ki}
\\
\widehat{v_i}\mathsf{T}^t(\mathsf{g}_k)=(\mathsf{T}^t(\mathsf{g}_k))(v_i)=\mathsf{g}_k(\mathsf{T}(v_i))=\mathsf{g}_k\left(\sum_{j=1}^mA_{ji}w_j\right)=\sum_{j=1}^mA_{ji}\mathsf{g}_k(w_j)=A_{ki}
$$
So we can prove $\widehat{v_i}\mathsf{T}^t=\sum_{j=1}^mA_{ji}\widehat{w_j}$, which means $\psi_2\mathsf{T}(v_i)=\mathsf{T}^{tt}\psi_1(v_i)$.

#### 12

We denote $\beta=\{\beta_1,\dots,\beta_n\}$ and $\beta^*=\{\mathsf{f}_1,\dots,\mathsf{f}_n\}$, by definition, $\psi(\beta_i)=\widehat{\beta_i}$, and we have
$$
\psi(\beta_i)(\mathsf{f}_j)=\widehat{\beta_i}(\mathsf{f}_j)=\mathsf{f}_j(\beta_i)=\delta_{ji},\quad 1\le i,j\le n
$$
This shows that $\{\psi(\beta_1),\dots,\psi(\beta_n)\}$ is the dual basis for $\beta^*$, or $\psi(\beta)=\beta^{**}$.

#### 13

(a) Let $\mathsf{f},\mathsf{g}\in S^0$, we shall show that $c\mathsf{f}+\mathsf{g}\in S^0$, choose any $x\in S$, we have
$$
(c\mathsf{f}+\mathsf{g})(x)=c\mathsf{f}(x)+\mathsf{g}(x)=0\implies c\mathsf{f}+\mathsf{g}\in S^0
$$
This shows $S^0$ is a subspace of $\mathsf{V}^*$.

(b) Since $V$ is finite-dimensional, we see that $W$ is finite-dimensional, let $\beta'=\{w_1,\dots,w_m\}$ be a basis for $W$, since $x\notin W$, we have $\beta'\cup\{x\}$ is linearly independent, thus can be extended to a basis $\beta$ for $V$, we can write $\beta=\beta'\cup\{x,u_0,\dots,u_k\}$ where $k\ge0$. Let $\beta^*$ be the dual basis for $\beta$, let $\mathsf{f}$ be the vector in $\beta^*$ such that $\mathsf{f}(x)=1$ and $\mathsf{f}(v)=0$ for any $v\in\beta,v\ne x$, then we have $\mathsf{f}(w_i)=0$ for all $w_i\in\beta'$, this means $\mathsf{f}\in\mathsf{W}^0$.

(c) Notice that $(S^0)^0=\{\phi\in\mathsf{V}^{**}:\phi(\mathsf{f})=0\text{ for all }\mathsf{f}\in S^0\}$. If $\phi\in\text{span}(\psi(S))$, then there exists $x_1,\dots,x_n\in S$ such that
$$
\phi=c_1\psi(x_1)+\cdots+c_n\psi(x_n)=c_1\widehat{x_1}+\cdots+c_n\widehat{x_n},\quad c_1,\dots,c_n\in F
$$
thus for any $\mathsf{f}\in S^0$, we have
$$
\phi(\mathsf{f})=c_1\widehat{x_1}(\mathsf{f})+\cdots+c_n\widehat{x_n}(\mathsf{f})=c_1\mathsf{f}(x_1)+\cdots+c_n\mathsf{f}(x_n)=0
$$
which means $\phi\in(S^0)^0$, and so we get $\text{span}(\psi(S))\subseteq(S^0)^0$. Conversely, let $\phi\in(S^0)^0$, assume that $\phi\notin\text{span}(\psi(S))$, since $\psi$ is an isomorphism, we can find a $x\in\mathsf{V}$ such that $\phi=\psi(x)$, it is clear that $x\notin\text{span}(S)$ from our assumption, use (b) we see that there exists $\mathsf{f}\in(\text{span}(S))^0$ such that $\mathsf{f}(x)\ne0$, this means $\mathsf{f}\in{S^0}$ and $\phi(\mathsf{f})=0$, on the other hand we have
$$
\phi(\mathsf{f})=\psi(x)(\mathsf{f})=\widehat{x}(\mathsf{f})=\mathsf{f}(x)\ne0
$$
this is a contradiction, so we must have $\phi\in\text{span}(\psi(S))$, thus $(S^0)^0\subseteq\text{span}(\psi(S))$.

(d) One direction is obvious. Now suppose $\mathsf{W}_1^0=\mathsf{W}_2^0$, assume $\mathsf{W}_1\ne\mathsf{W}_2$, then we can find one $x\in\mathsf{V}$ such that $x\in\mathsf{W}_1\backslash\mathsf{W}_2$ or $x\in\mathsf{W}_2\backslash\mathsf{W}_1$, in either case we can use (b) to get a contradiction, for example if $x\in\mathsf{W}_1\backslash\mathsf{W}_2$, then there exists $\mathsf{f}\in\mathsf{W}_2^0$ such that $\mathsf{f}(x)\ne0$, which means $\mathsf{f}\notin\mathsf{W}_1^0$, a contradiction to $\mathsf{W}_1^0=\mathsf{W}_2^0$.

(e) First suppose $\mathsf{f}\in\mathsf{W}_1^0\cap\mathsf{W}_2^0$, for any $x\in\mathsf{W}_1+\mathsf{W}_2$ we can write $x=w_1+w_2$ with $w_1\in\mathsf{W}_1$ and $w_2\in\mathsf{W}_2$​, then
$$
\mathsf{f}(x)=\mathsf{f}(w_1+w_2)=\mathsf{f}(w_1)+\mathsf{f}(w_2)=0
$$
thus $\mathsf{f}\in(\mathsf{W}_1+\mathsf{W}_2)^0$ and $\mathsf{W}_1^0\cap\mathsf{W}_2^0\subseteq(\mathsf{W}_1+\mathsf{W}_2)^0$.

Conversely, suppose $\mathsf{f}\in(\mathsf{W}_1+\mathsf{W}_2)^0$, since $\mathsf{W}_1\subseteq\mathsf{W}_1+\mathsf{W}_2$ and $\mathsf{W}_2\subseteq\mathsf{W}_1+\mathsf{W}_2$, we obviously have $\mathsf{f}\in\mathsf{W}_1^0$ and $\mathsf{f}\in\mathsf{W}_2^0$, this means $\mathsf{f}\in\mathsf{W}_1^0\cap\mathsf{W}_2^0$ and $\mathsf{W}_1^0\cap\mathsf{W}_2^0\supseteq(\mathsf{W}_1+\mathsf{W}_2)^0$.

#### 14

Extend an ordered basis $\{x_1,\dots,x_k\}$ of $\mathsf{W}$ to an ordered basis $\beta=\{x_1,x_2,\dots,x_n\}$ of $\mathsf{V}$. Let $\beta^*=\{\mathsf{f}_1,\dots,\mathsf{f}_n\}$, consider the linearly independent set $\gamma=\{\mathsf{f}_{k+1},\dots,\mathsf{f}_n\}$, then each $\mathsf{f}_j\in\gamma$ satisfy the equality $\mathsf{f}_j(x_i)=0$ for $1\le i\le k$, thus each $\mathsf{f}_j\in\mathsf{W}^0$. On the other hand, for any $\mathsf{f}\in\mathsf{W}^0$, write $\mathsf{f}=\sum_{i=1}^nc_i\mathsf{f}_i$, then for $1\le i\le k$, $\mathsf{f}(x_i)=0$ means $c_i=0$, so $\mathsf{f}=\sum_{i=k+1}^nc_i\mathsf{f}_i$, this means $\gamma$ spans $\mathsf{W}^0$, thus a basis for $\mathsf{W}^0$, and the conclusion follows.

#### 15

Suppose $\mathsf{f}\in\mathsf{N}(\mathsf{T}^t)$, then $\mathsf{T}^t\mathsf{f}=0$, which means $\mathsf{fT}(v)=\mathsf{f}(\mathsf{T(v)})=0$ for all $v\in\mathsf{V}$, or $\mathsf{f}(w)=0$ for all $w\in\mathsf{R(T)}$, thus $\mathsf{f}\in(\mathsf{R(T)})^0$. Conversely, suppose $\mathsf{f}\in(\mathsf{R(T)})^0$, then for any $v\in\mathsf{V}$, we have $\mathsf{T}(v)\in\mathsf{R(T)}$, thus 
$$
0=\mathsf{f}(\mathsf{T(v)})=\mathsf{fT}(v)=(\mathsf{T}^t\mathsf{f})(v)\implies\mathsf{T}^t\mathsf{f}=0\implies\mathsf{f}\in\mathsf{N}(\mathsf{T}^t)
$$

#### 16

Exercise 15 shows $(\mathsf{R}(\mathsf{L}_A))^0=\mathsf{N}(\mathsf{L}_A^t)$, and Exercise 14 shows that
$$
\dim(\mathsf{R}(\mathsf{L}_A))+\dim((\mathsf{R}(\mathsf{L}_A))^0)=\dim(\mathsf{F}^m)=\dim(\mathsf{R}(\mathsf{L}_A))+\dim(\mathsf{N}(\mathsf{L}_A^t))
$$
and the dimension theorem gives
$$
\dim((\mathsf{F}^m)^*)=\dim(\mathsf{R}(\mathsf{L}_A^t))+\dim(\mathsf{N}(\mathsf{L}_A^t))\implies\dim(\mathsf{R}(\mathsf{L}_A^t))=\dim(\mathsf{R}(\mathsf{L}_A))=\text{rank}(\mathsf{L}_A)
$$
thus we only need to prove $\dim(\mathsf{R}(\mathsf{L}_A^t))=\dim(\mathsf{R}(\mathsf{L}_{A^t}))=\text{rank}(\mathsf{L}_{A^t})$. Use Theorem 2.25, let $\beta$ and $\gamma$ be standard ordered bases for $\mathsf{F}^n$ and $\mathsf{F}^m$, then we have
$$
[\mathsf{L}_A^t]_{\gamma^*}^{\beta^*}=([\mathsf{L}_A]_{\beta}^{\gamma})^t=A^t
$$
Let $\phi_{\beta^*}$ be the standard representation of $(\mathsf{F}^n)^*$ with respect to $\beta^*$, then $\dim(\mathsf{R}(\mathsf{L}_A^t))=\dim(\phi_{\beta^*}(\mathsf{R}(\mathsf{L}_A^t)))$ since $\phi_{\beta^*}$ is an isomorphism. To finish the proof, we consider two subspaces of $\mathsf{F}^n$:  $\phi_{\beta^*}(\mathsf{R}(\mathsf{L}_A^t))$ and $\mathsf{R}(\mathsf{L}_{A^t})$, we write $\beta^*=\{\mathsf{f}_1,\dots,\mathsf{f}_n\}$ and $\gamma^*=\{\mathsf{g}_1,\dots,\mathsf{g}_m\}$, then
$$
\begin{aligned}
\begin{pmatrix}x_1\\{\vdots}\\x_n\end{pmatrix}\in\phi_{\beta^*}(\mathsf{R}(\mathsf{L}_A^t))&\Leftrightarrow
\sum_{i=1}^nx_i\mathsf{f}_i\in\mathsf{R}(\mathsf{L}_A^t)
\\&\Leftrightarrow\exists\mathsf{g}\in(\mathsf{F}^m)^*,s.t.\mathsf{L}_A^t(\mathsf{g})=\sum_{i=1}^nx_i\mathsf{f}_i
\\&\Leftrightarrow\exists\begin{pmatrix}y_1\\{\vdots}\\y_m\end{pmatrix}\in\mathsf{F}^m,s.t.\mathsf{L}_A^t(y_1\mathsf{g}_1+\cdots+y_m\mathsf{g}_m)=\sum_{i=1}^nx_i\mathsf{f}_i
\\&\Leftrightarrow\exists\begin{pmatrix}y_1\\{\vdots}\\y_m\end{pmatrix}\in\mathsf{F}^m,s.t.\sum_{j=1}^my_j(\mathsf{L}_A^t(\mathsf{g}_j))=\sum_{j=1}^my_j\sum_{i=1}^nA^t_{ij}\mathsf{f}_i=\sum_{i=1}^nx_i\mathsf{f}_i
\\&\Leftrightarrow\exists\begin{pmatrix}y_1\\{\vdots}\\y_m\end{pmatrix}\in\mathsf{F}^m,s.t.\sum_{j=1}^mA^t_{ij}y_j=x_i\text{ for }1\le i\le n
\\&\Leftrightarrow\exists\begin{pmatrix}y_1\\{\vdots}\\y_m\end{pmatrix}\in\mathsf{F}^m,s.t.A^t\begin{pmatrix}y_1\\{\vdots}\\y_m\end{pmatrix}=\begin{pmatrix}x_1\\{\vdots}\\x_n\end{pmatrix}
\\&\Leftrightarrow\begin{pmatrix}x_1\\{\vdots}\\x_n\end{pmatrix}\in\mathsf{R}(\mathsf{L}_{A^t})
\end{aligned}
$$
this gives $\phi_{\beta^*}(\mathsf{R}(\mathsf{L}_A^t))=\mathsf{R}(\mathsf{L}_{A^t})$, thus  $\dim(\mathsf{R}(\mathsf{L}_A^t))=\dim(\phi_{\beta^*}(\mathsf{R}(\mathsf{L}_A^t)))=\dim(\mathsf{R}(\mathsf{L}_{A^t}))$.

#### 17

First suppose $\mathsf{W}$ is $\mathsf{T}$-invariant, let $\mathsf{f}\in\mathsf{W}^0$, consider $\mathsf{T}^t\mathsf{f}$, for any $w\in\mathsf{W}$ we have $(\mathsf{T}^t\mathsf{f})(w)=\mathsf{f}(\mathsf{T}(w))=0$, the first equality follows from definition, the second equality follows from $\mathsf{T}(w)\in\mathsf{W}$ and $\mathsf{f}\in\mathsf{W}^0$. This equality shows $\mathsf{T}^t\mathsf{f}\in\mathsf{W}^0$, so $\mathsf{W}^0$ is $\mathsf{T}^t$-invariant.

Conversely, suppose $\mathsf{W}^0$ is $\mathsf{T}^t$-invariant. Assume there exists some $w\in\mathsf{W}$ such that $\mathsf{T}(w)\notin\mathsf{W}$, let $\{w_1,\dots,w_m\}$ be a basis for $\mathsf{W}$, then we can claim $\{w_1,\dots,w_m,\mathsf{T}(w)\}$ is linearly independent, thus can be extended to a basis $\beta$ of $\mathsf{V}$, let the dual basis of $\beta$ be $\beta^*$, and $\mathsf{f}$ is the linear functional in $\beta^*$ such that $\mathsf{f}(\mathsf{T}(w))=1$, since $\mathsf{f}(w_i)=0$ for $1\le i\le m$, we have $\mathsf{f}\in\mathsf{W}^0$, but $(\mathsf{T}^t\mathsf{f})(w)=\mathsf{f}(\mathsf{T}(w))=1\ne0$, this means $\mathsf{T}^t\mathsf{f}\notin\mathsf{W}^0$, a contradiction to $\mathsf{W}^0$ being $\mathsf{T}^t$-invariant. Thus for any $w\in\mathsf{W}$ we must have $\mathsf{T}(w)\in\mathsf{W}$, thus $\mathsf{W}$ is $\mathsf{T}$-invariant.

#### 18

First we prove $\Phi$ is linear. Let $\mathsf{f},\mathsf{g}\in\mathsf{V}^*$, then
$$
\begin{aligned}
\Phi(c\mathsf{f}+\mathsf{g})(s)&=(c\mathsf{f}+\mathsf{g})_S(s)=(c\mathsf{f}+\mathsf{g})(s)
\\&=c\mathsf{f}(s)+\mathsf{g}(s)=c\mathsf{f}_S(s)+\mathsf{g}_S(s)
\\&=c\Phi(\mathsf{f})(s)+\Phi(\mathsf{g})(s)=\left(c\Phi(\mathsf{f})+\Phi(\mathsf{g})\right)(s),\quad\forall{s\in S}
\end{aligned}
$$
thus $\Phi(c\mathsf{f}+\mathsf{g})=c\Phi(\mathsf{f})+\Phi(\mathsf{g})$, which means $\Phi$ is linear.

Next, for any $\mathsf{h}\in\mathcal{L}(S,F)$, use Exercise 34 of Section 2.1, there exists exactly one linear transformation $\mathsf{h}'\in\mathsf{V}^*$ such that $\mathsf{h}'(s)=\mathsf{h}(s)$ for all $s\in S$, define the function $\Psi:\mathcal{L}(S,F)\to\mathsf{V}^*$ by $\Psi(\mathsf{h})=\mathsf{h}'$, we can prove $\Psi$ is linear with similar technique to the proof that $\Phi$ is similar. Since $S$ is a basis for $\mathsf{V}$, any vector $v\in\mathsf{V}$ can be written as $v=\sum_{i=1}^nc_is_i$ with $c_i\in F$ and $s_i\in S$, the number $n,c_i,s_i$ all depends on $v$.

Given $\mathsf{f}\in\mathsf{V}^*$, let $\mathsf{g}=\Psi\Phi(\mathsf{f})$, for each $s_i$ we have
$$
\mathsf{g}(s_i)=\Psi\Phi(\mathsf{f})(s_i)=\Psi[(\mathsf{f}_S)(s_i)]=\Psi(\mathsf{f}(s_i))=\mathsf{f'}(s_i)=\mathsf{f}(s_i)
$$
which means $\mathsf{g}(v)=\mathsf{f}(v)$, thus $\mathsf{g}=\mathsf{f}$ in $\mathsf{V}^*$. Conversely, given $\mathsf{h}\in\mathcal{L}(S,F)$, let $\mathsf{g}=\Phi\Psi(\mathsf{h})$, for each $s\in S$ we have
$$
\mathsf{g}(s)=\Phi\Psi(\mathsf{h})(s)=\Phi(\mathsf{h}'(s))=\mathsf{h}'_S(s)=\mathsf{h}(s)
$$
which means $\mathsf{g}=\mathsf{h}$ in $\mathcal{L}(S,F)$, thus $\Psi$ is the inverse of $\Phi$, which means $\Phi$ is an isomorphism.

#### 19

Let $\beta_0$ be a basis for $\mathsf{W}$. Since $\mathsf{W}\ne\mathsf{V}$, we can find $v\in\mathsf{V}$ such that $v\ne\mathsf{W}$, that $\mathsf{W}$ is a subspace means $v\ne0$, and the set $\beta=\beta_0\cup\{v\}$ is linearly independent. By the replacement theorem (generalized replacement theorem if deal with the infinite-dimensional case), we can find a set $S$ such that $S\cup\beta$ is a basis for $\mathsf{V}$. Let $f:S\cup\beta\to{F}$ be the mapping defined by $f(v)=1$ and $f(u)=0$ for $u\in{S}\cup\beta,u\ne{v}$, Use Exercise 34 of Section 2.1, there exists a linear functional $\mathsf{f}\in\mathsf{V}^*$ such that $\mathsf{f}(x)=f(x)$ on $S\cup\beta$, notice that $\mathsf{f}(v)=1$, so $\mathsf{f}$ is nonzero, for any $x\in\mathsf{W}$, we can find vectors $x_i$s in $\beta_0$ such that $x=\sum_ic_ix_i$ for scalars $c_i\in{F}$, this means $\mathsf{f}(x)=\sum_ic_i\mathsf{f}(x_i)=0$.

#### 20

(a) Suppose $\mathsf{T}$ is onto, consider $\mathsf{T}^t\mathsf{g}=0$ for $\mathsf{g}\in\mathsf{W}^*$, we have $\mathsf{T}^t\mathsf{g}(x)=\mathsf{g}(\mathsf{T}(x))=0$ for any $x\in\mathsf{V}$, then this means $\mathsf{g}(w)=0$ for any $\mathsf{w}\in\mathsf{W}$, thus $\mathsf{g}=0$ and $\mathsf{T}^t$ is one-to-one. Conversely, suppose $\mathsf{T}^t$ is one-to-one, assume $\mathsf{T}$ is not onto, then $\mathsf{R(T)}$ is a proper subspace of $\mathsf{W}$, use Exercise 19, there exists a nonzero $\mathsf{f}\in\mathsf{W}^*$ such that $\mathsf{f}(x)=0$ for all $x\in\mathsf{R(T)}$, this means $\mathsf{T}^t\mathsf{f}(v)=\mathsf{f}(\mathsf{T}(v))=0$ for all $v\in\mathsf{V}$, so $\mathsf{T}^t\mathsf{f}=0$, a contradiction since $\mathsf{T}^t$ is one-to-one.

(b) Suppose $\mathsf{T}^t$ is onto, let $v\in\mathsf{V}$ with $\mathsf{T}(v)=0$, if we assume $v\ne0$, then $\{v\}$ is a linearly independent set, which means we can find a linearly independent subset $S$ of $\mathsf{V}$ such that $S\cup\{v\}$ is a basis for $\mathsf{V}$, so $\text{span}(S)$ is a proper subset of $\mathsf{V}$, use Exercise 19, there exists a nonzero $\mathsf{f}\in\mathsf{V}^*$ such that $\mathsf{f}(x)=0$ for all $x\in\text{span}(S)$, for this $\mathsf{f}$, there exists a $\mathsf{g}\in\mathsf{W}^*$ such that $\mathsf{f}=\mathsf{T}^t\mathsf{g}$, now for any $v'\in\mathsf{V}$ we can express $v'=v_1+cv$, where $v_1\in\text{span}(S)$ and $c\in{F}$, the field which $\mathsf{V}$ and $\mathsf{W}$ lies over. Then we have 
$$
\mathsf{f}(v')=\mathsf{f}(v_1)+c\mathsf{f}(v)=c\mathsf{g}(\mathsf{T}(v))=c\mathsf{g}(0)=0
$$
this gives $\mathsf{f}=0$, a contradiction to $\mathsf{f}$ being nonzero. Thus $v=0$ and $\mathsf{T}$ is one-to-one.

Conversely, suppose $\mathsf{T}$ is one-to-one, let $S$ be a basis for $\mathsf{V}$, for any $\mathsf{f}\in\mathsf{V}^*$, we define a function $g:\mathsf{T}(S)\to{F}$ as follows:
$$
g(\mathsf{T}(s))=\mathsf{f}(s),\quad\forall{s\in{S}}
$$
this function is well-defined since $\mathsf{T}$ is one-to-one, use Exercise 34 of Section 2.1, there exists a linear functional $\mathsf{g}\in\mathsf{W}^*$ such that $\mathsf{g}(x)=g(x)$ on $\mathsf{T}(S)$, we claim that $\mathsf{T}^t\mathsf{g}=\mathsf{f}$, for any $v\in\mathsf{V}$, we can write $v$ as a linear combination of vectors in $S$, namely $v=\sum_ic_is_i$ for $c_i\in{F},s_i\in{S}$, then
$$
\mathsf{T}^t\mathsf{g}(v)=\mathsf{g}(\mathsf{T}(v))=\sum_ic_i\mathsf{g}(\mathsf{T}(s_i))=\sum_ic_i\mathsf{f}(s_i)=\mathsf{f}\left(\sum_ic_is_i\right)=\mathsf{f}(v)
$$
this shows $\mathsf{T}^t$ is onto.

### Summary

本节讲对偶空间，V的对偶空间是从V到F的线性泛函，定理2.24证明V的每一组基都有一组对偶基，定理2.25定义了一个线性变换的转置变换，称其为转置变换的原因是该变换在对偶基下的矩阵是原线性变换在原基下矩阵的转置。定理2.26证明双对偶空间和原空间是同构的，借此可证明对偶空间中的每一组基都是原空间里某一组基的对偶基。