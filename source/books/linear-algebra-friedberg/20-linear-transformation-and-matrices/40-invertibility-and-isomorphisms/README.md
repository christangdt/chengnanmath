# Invertibility and Isomorphisms

### Content Notes

#### Definition

Let $\mathsf{V}$ and $\mathsf{W}$ be vector spaces, and let $\mathsf{T:V\to W}$ be linear. A function $\mathsf{U:W\to V}$ is said to be an **inverse** of $\mathsf{T}$ if $\mathsf{TU=I_W}$ and $\mathsf{UT=I_V}$. If $\mathsf{T}$ has an inverse, then $\mathsf{T}$ is said to be **invertible**, the inverse of $\mathsf{T}$ is unique and is denoted by $\mathsf{T}^{-1}$.

#### Theorem 2.17

Let $\mathsf{V}$ and $\mathsf{W}$ be vector spaces, and let $\mathsf{T:V\to W}$ be linear and invertible. Then $\mathsf{T^{-1}:W\to V}$ is linear.

#### Definition

Let $A$ be an $n\times n$ matrix. Then $A$ is **invertible** if there exists an $n\times n$ matrix $B$ such that $AB=BA=I$. The matrix $B$ is called the **inverse** of $A$ and is denoted by $A^{-1}$.

#### Lemma

Let $\mathsf{T}$ be an invertible linear transformation from $\mathsf{V}$ to $\mathsf{W}$. Then $\mathsf{V}$ is finite-dimensional if and only if $\mathsf{W}$ is finite-dimensional. In this case, $\dim(\mathsf{V})=\dim(\mathsf{W})$.

#### Theorem 2.18

Let $\mathsf{V}$ and $\mathsf{W}$ be finite-dimensional vector spaces with ordered bases $\beta$ and $\gamma$, respectively. Let $\mathsf{T:V\to W}$ be linear. Then $\mathsf{T}$ is invertible if and only if $[\mathsf{T}]_{\beta}^{\gamma}$ is invertible. Furthermore, $[\mathsf{T}^{-1}]_{\beta}^{\gamma}=([\mathsf{T}]_{\beta}^{\gamma})^{-1}$.

##### Corollary 1

Let $\mathsf{V}$ be a finite-dimensional vector space with an ordered basis $\beta$, and let $\mathsf{T:V\to V}$ be linear. Then $\mathsf{T}$ is invertible if and only if $[\mathsf{T}]_{\beta}$ is invertible. Furthermore, $[\mathsf{T}^{-1}]_{\beta}=([\mathsf{T}]_{\beta})^{-1}$.

##### Corollary 2

Let $A$ be an $n\times n$ matrix. Then $A$ is invertible if and only if $\mathsf{L}_A$ is invertible. Furthermore, $(\mathsf{L}_A)^{-1}=\mathsf{L}_{A^{-1}}$.

#### Definition

Let $\mathsf{V}$ and $\mathsf{W}$ be vector spaces. We say that $\mathsf{V}$ is **isomorphic** to $\mathsf{W}$ if there exists a linear transformation $\mathsf{T:V\to W}$ that is invertible. Such a linear transformation is called an **isomorphism** from $\mathsf{V}$ to $\mathsf{W}$.

#### Theorem 2.19

Let $\mathsf{V}$ and $\mathsf{W}$ be finite-dimensional vector spaces (over the same field). Then $\mathsf{V}$ is isomorphic to $\mathsf{W}$ if and only if $\dim({\mathsf{V}})=\dim(\mathsf{W})$.

##### Corollary

Let $\mathsf{V}$ be a vector space over $F$. Then $\mathsf{V}$ is isomorphic to $\mathsf{F}^n$ if and only if $\dim(\mathsf{V})=n$.

#### Theorem 2.20

Let $\mathsf{V}$ and $\mathsf{W}$ be finite-dimensional vector spaces over $F$ of dimension $n$ and $m$, respectively, and let $\beta$ and $\gamma$ be ordered bases for $\mathsf{V}$ and $\mathsf{W}$, respectively. Then the function $\Phi:\mathcal{L}(\mathsf{V,W})\to\mathsf{M}_{m\times n}(F)$, defined by $\Phi(\mathsf{T})=[\mathsf{T}]_{\beta}^{\gamma}$ for $\mathsf{T}\to\mathcal{L}(\mathsf{V,W})$, is an isomorphism.

##### Corollary

Let $\mathsf{V}$ and $\mathsf{W}$ be finite-dimensional vector spaces over $F$ of dimension $n$ and $m$, respectively. then $\mathcal{L}(\mathsf{V,W})$ is finite-dimensional of dimension $mn$.

#### Definition

Let $\beta$ be an ordered basis for an $n$ dimensional vector space $\mathsf{V}$ over the field $F$. The **standard representation of $\mathsf{V}$ with respect to $\beta$** is the function $\phi_{\beta}:\mathsf{V\to F^{n}}$ defined by $\phi_{\beta}(x)=[x]_{\beta}$ for each $x\in\mathsf{V}$.

#### Theorem 2.21

For any finite-dimensional vector space $\mathsf{V}$ with ordered basis $\beta$, $\phi_{\beta}$ is an isomorphism.

### Selected Exercises

#### 4

We have $(B^{-1}A^{-1})AB=B^{-1}B=I$ and $AB(B^{-1}A^{-1})=AA^{-1}=I$.

#### 5

We have $(A^{-1})^tA^t=(AA^{-1})^t=I^t=I$ and $A^t(A^{-1})^t=(A^{-1}A)^t=I^t=I$.

#### 6

We have $B=IB=(A^{-1}A)B=A^{-1}(AB)=A^{-1}O=O$.

#### 7

(a) Assume $A$ is invertible, then $A=IA=A^{-1}AA=A^{-1}A^2=O$, a contradiction.

(b) $A$ cannot be invertible.

#### 8

Corollary 1 is proved by let $\mathsf{V}=\mathsf{W}$ and $\beta=\gamma$ in Theorem 2.18. 

For Corollary 2, let $\beta$ be standard ordered basis of $\mathsf{F}^n$, then Theorem 2.15(a) gives $[\mathsf{L}_A]_{\beta}=A$, and Theorem 2.18 shows $A$ is invertible if and only if $\mathsf{L}_A$ is invertible. Since $\mathsf{L}_A\mathsf{L}_{A^{-1}}=\mathsf{L}_{AA^{-1}}=L_{I_n}=I_{\mathsf{F}^n}$ and $\mathsf{L}_{A^{-1}}\mathsf{L}_A=\mathsf{L}_{A^{-1}A}=L_{I_n}=I_{\mathsf{F}^n}$ by Theorem 2.15(e) and (f), we have $(\mathsf{L}_A)^{-1}=\mathsf{L}_{A^{-1}}$.

#### 9

Let $\mathsf{T}$ and $\mathsf{U}$ be linear transformation in a $n$ dimensional vector space with a standard basis $\beta$ such that $[\mathsf{T}]_{\beta}=A$ and $[\mathsf{U}]_{\beta}=B$, then $AB$ is invertible means $\mathsf{TU}$ is invertible, thus $\mathsf{T}$ is onto and $\mathsf{U}$ is one-to-one, so both $\mathsf{T}$ and $\mathsf{U}$ are invertible, so both $A$ and $B$ are invertible. 

If $A$ and $B$ are arbitrary matrices, then the conclusion is not true, for example, let
$$
A=\begin{pmatrix}1&1&0\end{pmatrix},B=\begin{pmatrix}1\\1\\0\end{pmatrix},\quad AB=(2)
$$

#### 10

(a) No need to prove.

(b) We have $A=AI=A(BB^{-1})=(AB)B^{-1}=IB^{-1}=B^{-1}$.

(c) If $\mathsf{V}$ is a finite-dimensional vector space and $\mathsf{T,U}\in\mathcal{L}(\mathsf{V})$ such that $\mathsf{TU}=\mathsf{I}$, then both $\mathsf{T}$ and $\mathsf{U}$ are invertible and $\mathsf{T}=\mathsf{U}^{-1}$. The proof is ommitted.

#### 11

Let $f\in\mathsf{P}_3(R)$ such that $\mathsf{T}(f)=O$, then $f(1)=f(2)=f(3)=f(4)=0$. Write $f$ as a linear combination of $f_1(x),f_2(x),f_3(x),f_4(x)$, where $f_i(x)$ is the Lagrange polynomials associated with $1,2,3,4$, suppose
$$
f=a_1f_1+a_2f_2+a_3f_3+a_4f_4
$$
then we can easily have $a_1=a_2=a_3=a_4=0$.

#### 12

That $\phi_{\beta}(x)=0$ means $x=0\beta_1+\cdots+0\beta_n=0$, which shows $\phi_{\beta}$ is one-to-one. For any $(x_1,\dots,x_n)\in\mathsf{F}^n$, let $x=x_1\beta_1+\cdots+x_n\beta_n$, then $\phi_{\beta}(x)=(x_1,\dots,x_n)$, which shows $\phi_{\beta}$ is onto.

#### 13

To prove reflexivity, notice the identity transformation is invertible.

To prove symmetry, use the fact that if $\mathsf{T}$ is invertible, then so is $\mathsf{T}^{-1}$ and $(\mathsf{T}^{-1})^{-1}=\mathsf{T}$.

to prove transitivity, use Theorem 2.18 and Exercise 4.

#### 14

Let $\mathsf{T}:\mathsf{V}\to\mathsf{F}^3$ be
$$
\mathsf{T}\left[\begin{pmatrix}a&a+b\\0&c\end{pmatrix}\right]=(a,b,c)
$$

#### 15

If $\mathsf{T}$ is an isomorphism, then $\dim(\mathsf{V})=\dim(\mathsf{W})$ by Theorem 2.19, and $\mathsf{T}(\beta)$ spans $\mathsf{W}$ since for any $w\in\mathsf{W}$, there is $v\in\mathsf{V}$ such that $\mathsf{T}(v)=w$, but obviously $\mathsf{T}(v)\in\mathsf{T}(\beta)$, thus  the latter a basis for $\mathsf{W}$.

Conversely, if $\mathsf{T}(\beta)$ is a basis for $\mathsf{W}$, then $\mathsf{T}$ is onto, and if we write $\beta=\{\beta_1,\dots,\beta_n\}$, then $\mathsf{T}(\beta_1),\dots,\mathsf{T}(\beta_n)$ is linearly independent, this shows $\dim(\mathsf{V})=\dim(\mathsf{W})$, and so $\mathsf{T}$ is one-to-one by Theorem 2.5.

#### 16

If $\Phi(A)=O$, then $B^{-1}AB=O$, which means $A=B(B^{-1}AB)B^{-1}=BOB^{-1}=O$, so $\Phi$ is one-to-one. For any  $M\in\mathsf{M}_{n\times n}(F)$, let $A=BMB^{-1}\in\mathsf{M}_{n\times n}(F)$, then $\Phi(A)=M$ and so $\Phi$ is onto.

#### 17

(a) For any $w_1,w_2\in\mathsf{T(V_0)}$, there exists $v_1,v_2\in\mathsf{V_0}$ such that $w_1=\mathsf{T}(v_1),w_2=\mathsf{T}(v_2)$, then
$$
cw_1+w_2=c\mathsf{T}(v_1)+\mathsf{T}(v_2)=\mathsf{T}(cv_1+v_2)\in\mathsf{T(V_0)}
$$
(b) $\mathsf{T}_{\mathsf{V_0}}$ is an isomorphism from $\mathsf{V_0}$ to $\mathsf{T(V_0)}$, and then use Theorem 2.19.

#### 20

The dimension Theorem shows that $n=\dim{\mathsf{V}}=\text{rank}(\mathsf{T})+\text{nullity}(\mathsf{T})$ and $n=\dim{\mathsf{F}^n}=\text{rank}(\mathsf{L}_A)+\text{nullity}(\mathsf{L}_A)$. Let $\mathsf{V_0}$ be the null space of $\mathsf{T}$, then it is a subspace of $\mathsf{V}$ by Theorem 2.1, so $\text{nullity}(\mathsf{T})=\dim(\mathsf{V_0})=\dim(\phi_{\beta}(\mathsf{V_0}))$ by Exercise 17. We can also prove that $\phi_{\beta}(\mathsf{V_0})$ is the null space of $\mathsf{L}_A$ since if we write $\beta=\{\beta_1,\dots,\beta_n\}$, then
$$
\begin{aligned}
(x_1,\dots,x_n)\in\phi_{\beta}(\mathsf{V_0})&\Leftrightarrow\sum_{i=1}^nx_i\beta_i\in\mathsf{V_0}
\\&\Leftrightarrow\mathsf{T}\left(\sum_{i=1}^nx_i\beta_i\right)=0
\\&\Leftrightarrow[\mathsf{T}]_{\beta}^{\gamma}\left[\sum_{i=1}^nx_i\beta_i\right]_{\beta}=[0]_\gamma=\phi_{\gamma}(0)
\\&\Leftrightarrow\mathsf{L}_A(x_1,\dots,x_n)=0
\end{aligned}
$$

#### 21

To prove $\{\mathsf{T}_{ij}:1\le i\le m,1\le j\le n\}$ is a basis for $\mathcal{L}(\mathsf{V,W})$, we only need to show they are linearly independent. Let $\{a_{ij}:1\le i\le m,1\le j\le n\} $ be a set of scalars such that $\sum_{1\le i\le m,1\le j\le n}a_{ij}\mathsf{T}_{ij}=0$, then for $1\le k\le n$ we have
$$
\sum_{1\le i\le m,1\le j\le n}a_{ij}\mathsf{T}_{ij}(v_k)=\sum_{i=1}^ma_{ik}w_i=0\implies a_{1k}=\cdots=a_{mk}=0,\quad k=1,\dots,n
$$
This shows $\{\mathsf{T}_{ij}:1\le i\le m,1\le j\le n\}$ is linearly independent.

To prove $[\mathsf{T}_{ij}]_{\beta}^{\gamma}=M^{ij}$, just follow the definition of $[\mathsf{T}_{ij}]_{\beta}^{\gamma}$. Thus the last statement can be proved by Theorem 2.20.

#### 22

If $\mathsf{T}(f)=0$, then $f(c_0)=\cdots=f(c_n)=0$, since $f\in\mathsf{P}_n(\mathsf{F})$ and $c_0,\dots,c_n$ are distinct, we have $f=0$, so $\mathsf{T}$ is one-to-one.

Let $f_0(x),\dots,f_n(x)$ be the Lagrange polynomials associated with $c_0,c_1,\dots,c_n$, then $\mathsf{T}(f_i)=e_{i+1}$ for $i=0,\dots,n$, where $e_j$ is the $j$th unit vector in $\mathsf{F}^{n+1}$, so $\mathsf{T}$ is onto.

#### 23

If $\mathsf{T}(\sigma)=0$, then we can conclude $\sigma(i)=0$ for $i=0,\dots,n$, this means $\sigma=\{0,0,\dots\}$, or $0\in\mathsf{V}$, so $\mathsf{T}$ is one-to-one.

For any $p\in\mathsf{P(F)}$, let $\deg(p)=n$, then we can write $p=\sum_{i=0}^nc_ix^i$ for scalars $c_0,\dots,c_n\in\mathsf{F}$, consider the sequence
$$
\sigma=(c_0,c_1,\dots,c_n,0,0,\dots)\in\mathsf{V}
$$
then $\mathsf{T}(\sigma)=p$, so $\mathsf{T}$ is onto.

#### 24

(a) That $v+\mathsf{N(T)}=v'+\mathsf{N(T)}$ means $v-v'\in\mathsf{N(T)}$, thus $\mathsf{T}(v-v')=\mathsf{T}(v)-\mathsf{T}(v')=0$.

(b) Let $v,v'\in\mathsf{V}$, then
$$
\begin{aligned}
\overline{\mathsf{T}}(v+\mathsf{N(T)}+v'+\mathsf{N(T)})&=\overline{\mathsf{T}}(v+v'+\mathsf{N(T)})\\&=\mathsf{T}(v+v')
\\&=\mathsf{T}(v)+\mathsf{T}(v')
\\&=\overline{\mathsf{T}}(v+\mathsf{N(T)})+\overline{\mathsf{T}}(v'+\mathsf{N(T)})
\end{aligned}
$$
and
$$
\begin{aligned}
\overline{\mathsf{T}}(c(v+\mathsf{N(T)}))&=\overline{\mathsf{T}}(cv+\mathsf{N(T)})
\\&=\mathsf{T}(cv)=c\mathsf{T}(v)=c\overline{\mathsf{T}}(v+\mathsf{N(T)})
\end{aligned}
$$
(c) Let $\overline{\mathsf{T}}(v+\mathsf{N(T)})=0$, then $\mathsf{T}(v)=0$ and $v\in\mathsf{N(T)}$, thus $v+\mathsf{N(T)}=\mathsf{N(T)}=0+\mathsf{N(T)}$, which is the zero element of $\mathsf{V/N(T)}$, so $\overline{\mathsf{T}}$ is one-to-one. For any $z\in Z$, since $\mathsf{T}$ is onto, we can find $v\in\mathsf{V}$ such that $z=\mathsf{T}(v)=\overline{\mathsf{T}}(v+\mathsf{N(T)})$, this means  $\overline{\mathsf{T}}$ is onto.

(d) For any $v\in\mathsf{V}$, we have $[\overline{\mathsf{T}}\eta](v)=\overline{\mathsf{T}}(\eta(v))=\overline{\mathsf{T}}(v+\mathsf{N(T)})=\mathsf{T}(v)$.

#### 25

Let $\Psi(f)=0$,  then there are some $s\in S$ such that $\sum_{s\in S}f(s)s=0$, but $S$ is a basis for $\mathsf{V}$ means that all $f(s)=0$ by the linearly independence of $s$ in $S$, so $f=0$ and $\Psi$ is one-to-one. Next for any $v\in\mathsf{V}$, we can express $v$ as a linear combination of finitely many vectors in $S$, suppose we have $v=c_1s_1+\cdots+v_ns_n$ with $c_1,\dots,c_n\in F$ and $s_1,\dots,s_n\in S$, define $f$ with $f(s_i)=v_i$ for $i=1,\dots,n$ and $f(s)=0$ otherwise, then $f\in\mathcal{C}(S,F)$ and $\Psi(f)=v$.

### Summary

本节的两个核心概念是可逆和同构。首先需注意可逆的定义是左结合和右结合均等于各自空间上的单位变换才可以。定理2.17说明如果线性变换T可逆，那么其逆变换是线性的。紧接着就定义矩阵的逆矩阵，并开始介绍一系列将逆矩阵和逆变换结合起来的结果，定理2.18说明矩阵可逆和线性变换可逆等价，且逆变换的矩阵等于变换矩阵的逆。本节第二部分开始讲同构的概念，如果两个空间之间存在一个可逆线性变换，那么这两个空间同构，所找到的这个可逆线性变换称为同构映射。定理2.19说明在有限维空间的前提下，同构只与维数有关，维数相同与同构等价！这进一步说明了向量空间的抽象性，两个空间的同构只取决于两空间是否存在相同数量的“代表”。定理2.20在单个线性变换与单个矩阵的基础上再向上抽象了一层，证明在两个向量空间之间的所有线性变换组成的向量空间与由所有合适维数矩阵构成的向量空间是同构的，也就是将单个线性变换与单个矩阵的同构关系上升到了线性变换集体与矩阵集体之间的同构关系。本节最后一部分引入一个“V按某组基的标准表示”这样的概念，实质是通过一个线性变换为空间中的每个向量x赋予一个类似坐标的东西，并且（定理2.21）这个线性变换是一个同构映射。基于这个同构映射，我们有能力把任意一个n维抽象向量空间转为一个熟悉的n维数值空间，也有能力把任意一个从n维抽象空间到m维抽象空间的线性变换转为一个从n维数值空间到m维数值空间的矩阵左乘变换，而后者是一个具体的数值型变换。