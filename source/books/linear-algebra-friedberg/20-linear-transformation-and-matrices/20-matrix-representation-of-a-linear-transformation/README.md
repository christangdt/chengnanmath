# The Matrix Representation of a Linear Transformation

### Content Notes

#### Definition (Ordered basis)

Let $\mathsf{V}$ be a finite-dimensional vector space. An ordered basis for $\mathsf{V}$ is a basis for $\mathsf{V}$ endowed with a specific order; that is, an ordered basis for $\mathsf{V}$ is a finite sequence of linearly independent vectors in $\mathsf{V}$ that generates $\mathsf{V}$. 

#### Definition (Coordinate vector)

Let $\beta=\{u_1,u_2,\dots,u_n\}$ be an ordered basis for a finite-dimensional vector space $\mathsf{V}$. For $x\in\mathsf{V}$, let $a_1,a_2,\dots,a_n$ be the unique scalars such that $x=\sum_{i=1}^na_iu_i$. We define the **coordinate vector of  $x$ relative to $\beta$**, denoted $[x]_{\beta}$, by
$$
[x]_{\beta}=\begin{pmatrix}a_1\\a_2\\{\vdots}\\a_n\end{pmatrix}.
$$

#### Definition (Matrix representation in the ordered bases)

Suppose $\mathsf{V}$ and $\mathsf{W}$ are finite-dimensional vector spaces with ordered bases $\beta=\{v_1,v_2,\dots,v_n\}$ and $\gamma=\{w_1,w_2\dots,w_m\}$, respectively. Let $\mathsf{T:V\to W}$ be linear. Then for each $j,1\le j\le n$, there exist unique scalars $a_{ij}\in F,1\le i\le m$, such that
$$
\mathsf{T}(v_j)=\sum_{i=1}^m a_{ij}w_j\quad\text{for }1\le j\le n.
$$
we call the $m\times n$ matrix $A$ defined by $A_{ij}=a_{ij}$ the **matrix representation of $\mathsf{T}$ in the ordered bases $\beta$ and $\gamma$** and write $A=[\mathsf{T}]_{\beta}^{\gamma}$. If $\mathsf{V}=\mathsf{W}$ and $\beta=\gamma$, then we write $A=[\mathsf{T}]_{\beta}$.

#### Definition (addition and scalar multiplication of linear transformations)

Let $\mathsf{T,U:V\to W}$ be arbitrary functions, where $\mathsf{V}$ and $\mathsf{W}$ are vector spaces over $F$, and let $a\in F$. We define $\mathsf{T+U:V\to W}$ by $\mathsf{(T+U)}(x)=\mathsf{T}(x)+\mathsf{U}(x)$ for all $x\in\mathsf{V}$, and $a\mathsf{T:V\to W}$ by $(a\mathsf{T})(x)=a\mathsf{T}(x)$ for all $x\in\mathsf{V}$.

#### Theorem 2.7

Let $\mathsf{V}$ and $\mathsf{W}$ be vector spaces over a field $F$, and let $\mathsf{T,U:V\to W}$ be linear.

(a) For all $a\in F,a\mathsf{T+U}$ is linear.

(b) Using the operations of addition and scalar multiplication in the preceding definition, the collection of all linear transformations from $\mathsf{V}$ to $\mathsf{W}$ is a vector spaces over $F$.

#### Definitions (vector space of linear transformations)

Let $\mathsf{V}$ and $\mathsf{W}$ be vector spaces over a field $F$. We denote the vector space of all linear transformations from $\mathsf{V}$ into $\mathsf{W}$ by $\mathcal{L}(\mathsf{V,W})$. In the case that $\mathsf{V}=\mathsf{W}$, we write $\mathcal{L}(\mathsf{V})$ instead of $\mathcal{L}(\mathsf{V,W})$.

#### Theorem 2.8

Let $\mathsf{V}$ and $\mathsf{W}$ be finite-dimensional vector spaces with ordered bases $\beta$ and $\gamma$, respectively, and let $\mathsf{T,U:V\to W}$ be linear transformations. Then

(a) $[\mathsf{T+U}]_{\beta}^{\gamma}=[\mathsf{T}]_{\beta}^{\gamma}+[\mathsf{U}]_{\beta}^{\gamma}$ and

(b) $[a\mathsf{T}]_{\beta}^{\gamma}=a[\mathsf{T}]_{\beta}^{\gamma}$ for all scalars $a$.

### Selected Exercises

#### 7

Use the symbols in the proof of Theorem 2.8, we have
$$
(a\mathsf{T})(v_j)=a\mathsf{T}(v_j)=a\sum_{i=1}^ma_{ij}w_i
$$
Thus
$$
([a\mathsf{T}]_{\beta}^{\gamma})_{ij}=aa_{ij}=a([\mathsf{T}]_{\beta}^{\gamma})_{ij}
$$

#### 8

Write $\beta=\{v_1,\dots,v_n\}$, then for $x,y\in\mathsf{V}$, we can write
$$
x=a_1v_1+\cdots+a_nv_n,y=b_1v_1+\cdots+b_nv_n
$$
which gives
$$
\mathsf{T}(x)=[x]_{\beta}=(a_1,\dots,a_n),\quad\mathsf{T}(y)=[y]_{\beta}=(b_1,\dots,b_n)
$$
notice that
$$
x+y=(a_1+b_1)v_1+\cdots+(a_n+b_n)v_n\\cx=ca_1v_1+\cdots+ca_nv_n
$$
hence
$$
\mathsf{T}(x+y)=[x+y]_{\beta}=(a_1+b_1,\dots,a_n+b_n)=[x]_{\beta}+[y]_{\beta}=\mathsf{T}(x)+\mathsf{T}(y)
\\
\mathsf{T}(cx)=(ca_1,\dots,ca_n)=c[x]_{\beta}=c\mathsf{T}(x)
$$

#### 9

We have
$$
\mathsf{T}(z_1+z_2)=\overline{z_1+z_2}=\overline{z_1}+\overline{z_2}=\mathsf{T}(z_1)+\mathsf{T}(z_2)
\\
\mathsf{T}(cz)=\overline{cz}=c\overline{z}=c\mathsf{T}(z)
$$
To compute $[\mathsf{T}]_{\beta}$, we have $\mathsf{T}(1)=1=1\cdot 1+0\cdot i$ and $\mathsf{T}(i)=-i=0\cdot 1+(-1)\cdot i$, thus
$$
[\mathsf{T}]_{\beta}=\begin{pmatrix}1&0\\0&-1\end{pmatrix}
$$

#### 11

Let $\{w_1,\dots,w_k\}$ be a basis for $\mathsf{W}$, extending it to a basis for $\mathsf{V}$ by adding $n-k$ vectors $v_{k+1},\dots,v_{n}$, since $\mathsf{W}$ is $\mathsf{T}$-invariant, we have
$$
\mathsf{T}(w_j)=\sum_{i=1}^ka_{ij}w_i,\quad \mathsf{T}(v_j)=\sum_{i=1}^kb_{ij}w_i+\sum_{i=k+1}^nc_{ij}v_i
$$

#### 12

Since $\mathsf{V}=\mathsf{W}\oplus\mathsf{W'}$, we choose a basis for $\mathsf{W}$ and a basis for $\mathsf{W'}$, merge to get a basis $\beta$ for $\mathsf{V}$. Then for any $v\in\beta$ we have either $\mathsf{T}(v)=v$ or $\mathsf{T}(v)=0$.

#### 13

 Nonzero means there exist $v,v'\in\mathsf{V}$ such that $\mathsf{T}v\ne0,\mathsf{U}v'\ne0$. Let $a,b$ be scalars such that $a\mathsf{T}+b\mathsf{U}=0\in\mathcal{L}(\mathsf{V,W})$. Assume $a\ne0$, then
$$
(a\mathsf{T}+b\mathsf{U})v=a\mathsf{T}v+b\mathsf{U}v=0\implies\mathsf{T}v=-\frac{b}{a}\mathsf{U}v\ne0\\\implies\mathsf{T}v\in\mathsf{R(T)}\cap\mathsf{R(U)}
$$
which is a contradiction. 

Assume $b\ne0$, then similarly we have $\mathsf{U}v'\in\mathsf{R(T)}\cap\mathsf{R(U)}$, a contradiction. Thus $a=b=0$.

#### 14

For any positive integer $n$, suppose we have scalars $a_1,\dots,a_n$ such that
$$
\mathsf{T}:=a_1\mathsf{T}_1+\cdots+a_n\mathsf{T}_n=0\in\mathcal{L}(\mathsf{V})
$$
then $\mathsf{T}(x)=0$ gives $a_1=0$, $\mathsf{T}(x^2)=0$ gives $a_2=0$, continue we can get $a_1=\cdots=a_n=0$.

#### 15

(a) Let $\mathsf{T,U}\in S^0$, then $(c\mathsf{T+U})(x)=c\mathsf{T}(x)+\mathsf{U}(x)=0$ for all $x\in S$.

(b) Let $\forall\mathsf{T}\in S_2^0$, then
$$
x\in S_1\implies x\in S_2\implies\mathsf{T}(x)=0\implies\mathsf{T}\in S_1^0
$$
(c) That $\mathsf{V}_1^0\cap\mathsf{V}_2^0\subseteq(\mathsf{V_1+V_2})^0$ is obvious. Let $\mathsf{T}\in(\mathsf{V_1+V_2})^0$, then $\mathsf{T}(x)=0$ for all $x\in\mathsf{V_1+V_2}$, since $\mathsf{V_1}\subset\mathsf{V_1+V_2}$ and $\mathsf{V_2}\subset\mathsf{V_1+V_2}$, we have $\mathsf{T}\in\mathsf{V}_1^0\cap\mathsf{V}_2^0$.

#### 16

Let $\dim(\mathsf{V})=\dim(\mathsf{W})=n$, choose a basis for $\mathsf{N(T)}$ to be $\{v_1,\dots,v_k\}$ with $0\le k\le n$, extend it to a basis $\{v_1,\dots,v_n\}$ for $\mathsf{V}$, let it be $\beta$. We already know that $\{\mathsf{T}(v_{k+1}),\dots,\mathsf{T}(v_{n})\}$ is a basis for $\mathsf{R(T)}$, extend it to an ordered basis $\gamma=\{w_1,\dots,w_k,\mathsf{T}(v_{k+1}),\dots,\mathsf{T}(v_{n})\}$ for $\mathsf{W}$, then $[\mathsf{T}]_{\beta}^{\gamma}$ is diagonal.

### Summary

本节介绍线性变换的矩阵表示，可以理解为将抽象的线性变换具象化、数字化，但这种数字化并非唯一，要在已确定源空间和目标空间的一组有序基之后才可具象化这个线性变换。如果确定了有序基，那么线性变换的加法和数乘就等同于对应矩阵的加法和数乘，也即线性变换和矩阵在给定的一组有序基之下是一一对应的两个空间。