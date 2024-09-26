# Composition of Linear Transformations and Matrix Multiplication

### Content Notes

#### Theorem 2.9

Let $\mathsf{V,W,Z}$ be vector spaces over the same field $F$, and let $\mathsf{T:V\to W}$ and $\mathsf{U:W\to Z}$ be linear. Then $\mathsf{UT:V\to Z}$ is linear.

#### Theorem 2.10

Let $\mathsf{V}$ be a vector space. Let $\mathsf{T,U_1,U_2}\in\mathcal{L}(\mathsf{V})$. Then

(a) $\mathsf{T(U_1+U_2)=TU_1+TU_2}$ and $\mathsf{(U_1+U_2)T=U_1T+U_2T}$

(b) $\mathsf{T(U_1U_2)}=\mathsf{(TU_1)U_2}$

(c) $\mathsf{TI}=\mathsf{IT}=\mathsf{T}$

(d) $a(\mathsf{U_1U_2})=(a\mathsf{U_1})\mathsf{U}_2=\mathsf{U_1}(a\mathsf{U_2})$ for all scalar $a$.

#### Definition (Matrix multiplication)

Let $A$ be an $m\times n$ matrix and $B$ be an $n\times p$ matrix. We define the **product** of $A$ and $B$, denoted $AB$, to be the $m\times p$ matrix such that
$$
(AB)_{ij}=\sum_{k=1}^nA_{ik}B_{kj}\quad\text{for }1\le i\le m,\quad1\le j\le p.
$$

#### Theorem 2.11

Let $\mathsf{V,W,Z}$ be finite-dimensional vector spaces with ordered bases $\alpha,\beta,\gamma$ respectively. Let  $\mathsf{T:V\to W}$ and $\mathsf{U:W\to Z}$ be linear transformations. Then
$$
[\mathsf{UT}]_{\alpha}^{\gamma}=[\mathsf{U}]_{\beta}^{\gamma}[\mathsf{T}]_{\alpha}^{\beta}.
$$

##### Corollary

Let $\mathsf{V}$ be a finite-dimensional vector space with an ordered basis $\beta$. Let $\mathsf{T,U}\in\mathcal{L}(\mathsf{V})$. Then $[\mathsf{UT}]_{\beta}=[\mathsf{U}]_{\beta}[\mathsf{T}]_{\beta}$.

#### Definitions (Kronecker delta, identity matrix)

We define the **Kronecker delta** $\delta_{ij}$ by $\delta_{ij}=1$ if $i=j$ and $\delta_{ij}=0$ if $i\ne j$. The $n\times n$ **identity matrix** $I_n$ is defined by $(I_n)_{ij}=\delta_{ij}$.

#### Theorem 2.12

Let $A$ be an $m\times n$ matrix, $B$ and $C$ be $n\times p$ matrices, and $D$ and $E$ be $q\times m$ matrices. Then

(a) $A(B+C)=AB+AC$ and $(D+E)A=DA+EA$.

(b) $a(AB)=(aA)B=A(aB)$ for any scalar $a$.

(c) $I_mA=A=AI_n$.

(d) If $\mathsf{V}$ is an $n$-dimensional vector space with an ordered basis $\beta$, then $[\mathsf{I_V}]_{\beta}=I_n$.

##### Corollary

Let $A$ be an $m\times n$ matrix, $B_1,B_2,\dots,B_k$ be $n\times p$ matrices, $C_1,C_2,\dots,C_k$ be $q\times m$ matrices, and $a_1,a_2,\dots,a_k$ be scalars. Then
$$
A\left(\sum_{i=1}^ka_iB_i\right)=\sum_{i=1}^ka_iAB_i,\qquad\left(\sum_{i=1}^ka_iC_i\right)A=\sum_{i=1}^ka_iC_iA
$$


#### Theorem 2.13

Let $A$ be an $m\times n$ matrix, $B$ be an $n\times p$ matrix. For each $j(1\le j\le p)$ let $u_j$ and $v_j$ denote the $j$th columns of $AB$ and $B$, respectively. Then

(a) $u_j=Av_j$,

(b) $v_j=Be_j$, where $e_j$ is the $j$th standard vector of $\mathsf{F}^p$.

#### Theorem 2.14

Let $\mathsf{V}$ and $\mathsf{W}$ be finite-dimensional vector spaces having ordered bases $\beta$ and $\gamma$, respectively, and let $\mathsf{T:V\to W}$ be linear. Then, for each $u\in\mathsf{V}$, we have
$$
[\mathsf{T}(u)]_{\gamma}=[\mathsf{T}]_\beta^{\gamma}[u]_{\beta}.
$$

#### Definition (Left-multiplication transformation)

Let $A$ be an $m\times n$ matrix with entries from a field $F$. We denote by $\mathsf{L}_A$ the mapping $\mathsf{L}_A:\mathsf{F}^n\to\mathsf{F}^m$ defined by $\mathsf{L}_A(x)=Ax$ (the matrix product of $A$ and $x$) for each column vector $x\in\mathsf{F}^n$. We call $\mathsf{L}_A$ a **left-multiplication transformation**.

#### Theorem 2.15

Let $A$ be an $m\times n$ matrix with entries from a field $F$. Then the left-multiplication transformation $\mathsf{L}_A:\mathsf{F}^n\to\mathsf{F}^m$ is linear. Furthermore, if $B$ is any other $m\times n$ matrix (with entires from $F$) and $\beta$ and $\gamma$ are the standard ordered bases for $\mathsf{F}^n$ and $\mathsf{F}^m$ respectively, then we have the following properties.

(a) $[\mathsf{L}_A]_{\beta}^{\gamma}=A$.

(b) $\mathsf{L}_A=\mathsf{L}_B$ if and only if $A=B$.

(c) $\mathsf{L}_{A+B}=\mathsf{L}_A+\mathsf{L}_B$ and $\mathsf{L}_{aA}=a\mathsf{L}_A$ for all $a\in F$.

(d) If $\mathsf{T}:\mathsf{F}^n\to\mathsf{F}^m$ is linear, then there exists a unique $m\times n$ matrix $C$ such that $\mathsf{T}=\mathsf{L}_C$. In fact, $C=[\mathsf{T}]_{\beta}^{\gamma}$.

(e) If $E$ is an $n\times p$ matrix, then $\mathsf{L}_{AE}=\mathsf{L}_{A}\mathsf{L}_{E}$.

(f) If $m=n$, then $\mathsf{L}_{I_n}=\mathsf{I}_{\mathsf{F}^n}$.

#### Theorem 2.16

Let $A, B$, and $C$ be matrices such that $A(BC)$ is defined. Then $(AB)C$ is also defined and $A(BC) = (AB)C$; that is, matrix multiplication is associative.  

### Selected Exercises

#### 5

The second half of Theorem 2.12(a): we have
$$
[(D+E)A]_{ij}=\sum_{k=1}^n(D+E)_{ik}A_{kj}=\sum_{k=1}^n(D_{ik}A_{kj}+E_{ik}A_{kj})\\=\sum_{k=1}^nD_{ik}A_{kj}+\sum_{k=1}^nE_{ik}A_{kj}=(DA)_{ij}+(EA)_{ij}=[DA+EA]_{ij}
$$
so $(D+E)A=DA+EA$.

Theorem 2.12(b): we have
$$
[a(AB)]_{ij}=a\sum_{k=1}^nA_{ik}B_{kj}=\sum_{k=1}^n(aA_{ik})B_{kj}=[(aA)B]_{ij}
\\
[a(AB)]_{ij}=a\sum_{k=1}^nA_{ik}B_{kj}=\sum_{k=1}^nA_{ik}(aB_{kj})=[A(aB)]_{ij}
$$


The second half of Theorem 2.12(c): we have
$$
(AI_n)_{ij}=\sum_{k=1}^nA_{ik}(I_n)_{kj}=\sum_{k=1}^nA_{ik}\delta_{kj}=A_{ij}
$$
Theorem 2.12(d): let $\beta=(\beta_1,\dots,\beta_n)$, then
$$
(\mathsf{I_V})(\beta_j)=\beta_j\implies[(\mathsf{I_V})(\beta_j)]_{\beta}=e_j\implies[(\mathsf{I_V})]_{\beta}=I_n
$$
Corollary: we have
$$
\left[A\left(\sum_{i=1}^ka_iB_i\right)\right]_{ij}=\sum_{m=1}^nA_{im}\left(\sum_{i=1}^ka_iB_i\right)_{mj}=\sum_{i=1}^ka\sum_{m=1}^nA_{im}(B_i)_{mj}=\sum_{i=1}^ka_iAB_i
$$
the next equation can be similarly proved.

#### 6

We have
$$
v_j=\begin{pmatrix}B_{1j}\\{\vdots}\\B_{nj}\end{pmatrix}=\begin{pmatrix}\sum_{k=1}^nB_{1k}\delta_{kj}\\{\vdots}\\\sum_{k=1}^nB_{nk}\delta_{kj}\end{pmatrix}=B\begin{pmatrix}\delta_{kj}\\{\vdots}\\{\delta_{kj}}\end{pmatrix}=Be_j
$$

#### 7

Theorem 2.15 (c): Let $C$ be any element in $\mathsf{F}^n$, then 
$$
\mathsf{L}_{A+B}(C)=(A+B)C=AC+BC=\mathsf{L}_A(C)+\mathsf{L}_B(C)=(\mathsf{L}_A+\mathsf{L}_B)(C)\\\mathsf{L}_{aA}(C)=aAC=a(AC)=a(\mathsf{L}_A(C))
$$
Theorem 2.15(f): for $e_i\in\beta$ with $i=1,\dots,n$, we have
$$
\mathsf{L}_{I_n}(e_i)=I_n(e_i)=e_i=\mathsf{I}_{\mathsf{F}^n}(e_i)
$$

#### 9

Let $\mathsf{U}(a,b)=(b,0)$ and $\mathsf{T}(a,b)=(a,0)$, then
$$
\mathsf{UT}(a,b)=\mathsf{U}(a,0)=(0,0),\quad\mathsf{TU}(a,b)=\mathsf{T}(b,0)=(b,0)
$$

#### 10

If $A$ is diagonal, then $A_{ij}=0$ if $i\ne j$, and $A_{ii}=\delta_{ii}A_{ii}$ for $i=1,\dots,n$.

Conversely, if $i\ne j$, then $\delta_{ij}=0$, which means $A_{ij}=0$, thus $A$ is diagonal.

#### 11

If $\mathsf{T}^2=\mathsf{T}_0$, let $w\in\mathsf{R(T)}$, then there exist $v\in\mathsf{V}$ such that $\mathsf{T}v=w$, so
$$
\mathsf{T}w=\mathsf{T}(\mathsf{T}v)=\mathsf{T}^2v=\mathsf{T}_0v=0\implies w\in\mathsf{N(T)}
$$
The other direction is obvious.

#### 12

(a) If $\mathsf{UT}$ is one-to-one, then $\mathsf{UT}(v)=0\implies v=0$, let $\mathsf{T}(v)=0$, then $\mathsf{U}(0)=0$, so $\mathsf{UT}(v)=0$, which means $v=0$, so $\mathsf{T}$ is one-to-one, $\mathsf{U}$ need not be one-to-one.

(b) Let $z\in\mathsf{Z}$, since $\mathsf{UT}$ is onto, there exist $v\in\mathsf{V}$ such that $\mathsf{UT}(v)=z$, this means the vector $w=\mathsf{T}(v)\in\mathsf{W}$ can make $\mathsf{U}(w)=z$, thus $\mathsf{U}$ is onto. $\mathsf{T}$ need not be onto.

#### 13

We have
$$
\text{tr}(AB)=\sum_{i=1}^n(AB)_{ii}=\sum_{i=1}^n\left(\sum_{k=1}^nA_{ik}B_{ki}\right)=\sum_{k=1}^n\left(\sum_{i=1}^nB_{ki}A_{ik}\right)\\=\sum_{k=1}^n(BA)_{kk}=\text{tr}(BA)
$$

#### 14

(a) We have
$$
Bz=B\sum_{j=1}^pa_je_j=\sum_{j=1}^pa_j(Be_j)=\sum_{j=1}^pa_jv_j
$$
(b) Use Theorem 2.13(a) we can have $u_j=Av_j$, then use (a) on $Av_j$.

(c) Transpose on (a)

(d) Mimic the procedure of (b)

#### 15

Let $M$ be $m\times n$ and $A$ be $n\times p$, write $v_1,\dots,v_p$ as columns of $A$, so $A=(v_1,\dots,v_p)$, the condition says $v_j=\sum_{i\ne j}a_iv_i$ for scalars $a_i$, we prove first that $MA=(Mv_1,\dots,Mv_p)$, the $j$th column of $MA$ can be written as
$$
(MA)_j=\begin{pmatrix}(MA)_{1j}\\{\vdots}\\(MA)_{mj}\end{pmatrix}=\begin{pmatrix}\sum_{k=1}^nM_{1k}A_{kj}\\{\vdots}\\\sum_{k=1}^nM_{mk}A_{kj}\end{pmatrix}=M\begin{pmatrix}A_{1j}\\{\vdots}\\A_{nj}\end{pmatrix}=Mv_j
$$
Next use corollary of Theorem 2.12 we have $Mv_j=\sum_{i\ne j}a_iMv_i$.

#### 16

(a) Use Dimension Theorem we have $\dim(\mathsf{V})=\text{nullity}(\mathsf{T})+\text{rank}(\mathsf{T})$ and $\dim(\mathsf{V})=\text{nullity}(\mathsf{T}^2)+\text{rank}(\mathsf{T}^2)$, this shows $\text{nullity}(\mathsf{T})=\text{nullity}(\mathsf{T}^2)$. Since $\mathsf{N(T)}\subseteq\mathsf{N(T^2)}$, we have $\mathsf{N(T)}=\mathsf{N(T^2)}$. Let $w\in\mathsf{R(T)}\cap\mathsf{N(T)}$, then there exists some $v\in\mathsf{V}$ such that $\mathsf{T}(v)=w$, and $\mathsf{T}(w)=0$, this means $\mathsf{T}^2(v)=0$ and thus $v\in\mathsf{N(T^2)}=\mathsf{N(T)}$, so we get $0=\mathsf{T}(v)=w$.

That $\mathsf{R(T)}\cap\mathsf{N(T)}=\{0\}$ and $\dim(\mathsf{V})=\text{nullity}(\mathsf{T})+\text{rank}(\mathsf{T})$ together gives $\mathsf{V}=\mathsf{R(T)}\oplus\mathsf{N(T)}$.

(b) Since We have $\mathsf{R(T^{k+1})}\subseteq\mathsf{R(T^k)}$ for all positive integers $k$, Since $\mathsf{V}$ is finite dimensional, $\dim(\mathsf{V})=n>0$ and thus $\text{rank}(\mathsf{T})=r_1\le n$, define $\text{rank}(\mathsf{T}^k)=r_k$ for $k>1$, then $\{r_k\}$ is monotonic decreasing, we only need to find some $k$ such that $r_{k+1}=r_k$, if we find, then we are done. If not, then $r_{k+1}<r_k<\cdots<r_1\le n$, so after at most $n$ steps, we shall make $r_k=0$, this gives $\mathsf{R(T^k)}=\{0\}$ and $\mathsf{V}=\mathsf{N(T^k)}$.

#### 17

Follow the Hint, if a linear transformation $\mathsf{T:V\to V}$ satisfies $\mathsf{T^2}=\mathsf{T}$, then $\mathsf{T}$ shall be the identity transformation on its nonzero range.

### Summary

本节讲线性变换的结合和矩阵乘法的关联。首先是线性变换的组合的一些性质：定理2.9说明两个线性变换组成的变换仍是线性的，定理2.10说明同一线性空间内的线性变换满足结合律、分配律，与单位变换可交换、数乘任意结合。矩阵乘法的定义是从线性变换的矩阵表示“自然地”衍生而来，这也是引入矩阵乘法一种通用的做法，与上来直接丢一个乘法的定义相比，显得不那么生硬。定理2.11揭示了“线性变换的组合”和“矩阵乘法”之间的联系，即线性变换组合的表示矩阵等于线性变换各自矩阵表示的乘积。本节的第二部分更多介绍矩阵运算的一些性质，由于有了第一部分证明线性变换的基础，可以简化部分关于矩阵性质的证明，在介绍之前本书引入了一个很传统的概念：Kronecker积，在现代的线性代数书中已很少见。定理2.12几乎是定理2.10的矩阵翻版，缺了一个矩阵的结合律，将在定理2.16中叙述。定理2.13提供另一个看待矩阵的视角：矩阵是一行列向量的排列，矩阵乘法可以看作列向量的左乘，每个矩阵内的第j个列向量又是该矩阵本身与一个j单位列向量（即第j个元素为1其他为0）的左乘。这个视角的引入是为了帮助理解定理2.14的重要结论，即线性变换的结果也可以用矩阵的方式“计算”出来，一个向量被线性变换以后在目标空间的坐标，等于线性变换对应矩阵左乘该向量在原空间的坐标。本节的最后一部分介绍“左乘变换”，这是一个从n维列向量空间到m维列向量空间的变换，任何一个m行n列矩阵都派生一个左乘变换，可以通过定理2.15证明：某矩阵A派生的左乘变换在标准基下的矩阵表示就是矩阵A本身；左乘变换相同意味着派生矩阵相同；左乘变换关于派生矩阵是线性的；任意一个从n维列向量空间到m维列向量空间的线性变换都可以写成左乘变换；两矩阵相乘派生的左乘变换等于两矩阵分别派生左乘变换后再组合；单位矩阵的左乘变换是n维列向量空间上的单位变换。有了定理2.15的工具，再证明定理2.16，即矩阵的乘法结合律就会很简单。本节在理论介绍后增加了一个介绍incidence matrices的应用章节，内容并不影响后续章节的学习，有兴趣可研读。