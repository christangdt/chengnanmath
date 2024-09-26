# Diagonalizability

### Content Notes

#### Theorem 5.5

Let $\mathsf{T}$ be a linear operator on a vector space $\mathsf{V}$, and let $\lambda_1,\lambda_2,\dots,\lambda_k$ be distinct eigenvalues of $\mathsf{T}$. If $v_1,v_2,\dots,v_k$ are eigenvectors of $\mathsf{T}$ such that $\lambda_i$ corresponds to $v_i(1\le i\le k)$, then $\{v_1,\dots,v_k\}$ is linearly independent.

##### Corollary

Let $\mathsf{T}$ be a linear operator on a $n$-dimensional vector space $\mathsf{V}$. If $\mathsf{T}$ has $n$ distinct eigenvalues, then $\mathsf{T}$ is diagonalizable.

#### Definition (polynomial split over $F$)

A polynomial $f(t)$ in $\mathsf{P(F)}$ **splits over** $F$ if there are scalars $c,a_1,\dots,a_n$ (not necessarily distinct) in $F$ such that
$$
f(t)=c(t-a_1)(t-a_2)\cdots(t-a_n).
$$

#### Theorem 5.6

The characteristic polynomial of any diagonalizable linear operator splits.

#### Definition (algebraic multiplicity)

Let $\lambda$ be an eigenvalue of a linear operator or matrix with characteristic polynomial $f(t)$. The **(algebraic) multiplicity** of $\lambda$ is the largest positive integer $k$ for which $(t-\lambda)^k$ is a factor of $f(t)$​.

#### Definition (eigenspace)

Let $\mathsf{T}$ be a linear operator on a vector space $\mathsf{V}$, and let $\lambda$ be an eigenvalue of $\mathsf{T}$. Define $\mathsf{E}_{\lambda}=\{x\in\mathsf{V}:\mathsf{T}(x)=\lambda{x}\}=\mathsf{N(T-\lambda I_{V})}$. The set $\mathsf{E}_{\lambda}$ is called the **eigenspace** of $\mathsf{T}$ corresponding to the eigenvalue $\lambda$. Analogously, we define the **eigenspace** of a square matrix $A$ to be the eigenspace of $\mathsf{L}_A$.

#### Theorem 5.7

Let $\mathsf{T}$ be a linear operator on a finite-dimensional vector space $\mathsf{V}$, and let $\lambda$ be an eigenvalue of $\mathsf{T}$ having multiplicity $m$. Then $1\le\dim(\mathsf{E}_{\lambda})\le{m}$​.

#### Lemma

Let $\mathsf{T}$ be a linear operator, and let $\lambda_1,\lambda_2,\dots,\lambda_k$ be distinct eigenvalues of $\mathsf{T}$. For each $i=1,2,\dots,k$, let $v_i\in\mathsf{E}_{\lambda_i}$, the eigenspace corresponding to $\lambda_i$. If
$$
v_1+v_2+\cdots+v_k=0
$$
then $v_i=0$ for all $i$.

#### Theorem 5.8

Let $\mathsf{T}$ be a linear operator on a vector space $\mathsf{V}$, and let $\lambda_1,\lambda_2,\dots,\lambda_k$ be distinct eigenvalues of $\mathsf{T}$. For each $i=1,2,\dots,k$, let $S_i$ be a finite linearly independent subset of the eigenspace $\mathsf{E}_{\lambda_i}$. Then $S=S_1\cup S_2\cup\cdots\cup S_k$ is a linearly independent subset of $\mathsf{V}$​.

#### Theorem 5.9

Let $\mathsf{T}$ be a linear operator on a finite-dimensional vector space $\mathsf{V}$ such that the characteristic polynomial of $\mathsf{T}$ splits. Let $\lambda_1,\lambda_2,\dots,\lambda_k$ be the distinct eigenvalues of $\mathsf{T}$. Then

(a) $\mathsf{T}$ is diagonalizable if and only if the multiplicity of $\lambda_i$ is equal to $\dim(\mathsf{E}_{\lambda_i})$ for all $i$.

(b) If $\mathsf{T}$ is diagonalizable and $\beta_i$ is an ordered basis for $\mathsf{E}_{\lambda_i}$ for each $i$, then $\beta=\beta_1\cup\beta_2\cup\cdots\cup\beta_k$ is an ordered basis for $\mathsf{V}$ consisting of eigenvectors of $\mathsf{T}$​.

#### Definition (sum of spaces)

Let $\mathsf{W}_1,\mathsf{W}_2,\dots,\mathsf{W}_k$ be subspaces of a vector space $\mathsf{V}$. We define the **sum** of these subspaces to be the set
$$
\{v_1+v_2+\cdots+v_k:v_i\in\mathsf{W}_i\text{ for }1\le i\le k\},
$$
which we denote by $\mathsf{W}_1+\mathsf{W}_2+\cdots+\mathsf{W}_k$ or $\sum_{i=1}^k\mathsf{W}_i$.

#### Definition (direct sum)

Let $\mathsf{W}_1,\mathsf{W}_2,\dots,\mathsf{W}_k$ be subspaces of a vector space $\mathsf{V}$. We call $\mathsf{V}$ the **direct sum** of the subspaces $\mathsf{W}_1,\mathsf{W}_2,\dots,\mathsf{W}_k$ and write $\mathsf{V}=\mathsf{W}_1\oplus\mathsf{W}_2\oplus\cdots\oplus\mathsf{W}_k$, if $\mathsf{V}=\sum_{i=1}^k\mathsf{W}_i$ and
$$
\mathsf{W}_j\cap\sum_{i\ne j}\mathsf{W}_i=\{0\}\text{ for each }j(1\le j\le k).
$$

#### Theorem 5.10

Let $\mathsf{W}_1,\mathsf{W}_2,\dots,\mathsf{W}_k$ be subspaces of a finite-dimensional vector space $\mathsf{V}$. The following conditions are equivalent.

(a) $\mathsf{V}=\mathsf{W}_1\oplus\mathsf{W}_2\oplus\cdots\oplus\mathsf{W}_k$.

(b) $\mathsf{V}=\sum_{i=1}^k\mathsf{W}_i$ and for any vectors $v_1,v_2,\dots,v_k$ such that $v_i\in\mathsf{W}_i$ ($1\le i\le k$), if $v_1+v_2+\cdots+v_k=0$, then $v_i=0$ for all $i$.

(c) Each vector $v\in\mathsf{V}$ can be uniquely written as $v=v_1+v_2+\cdots+v_k$, where $v_i\in\mathsf{W}_i$.

(d) If $\gamma_i$ is an ordered basis for $\mathsf{W}_i$ ($1\le i\le k$), then $\gamma_1\cup\gamma_2\cup\cdots\cup\gamma_k$ is an ordered basis for $\mathsf{V}$.

(e) For each $i=1,2,\dots,k$, there exists an ordered basis $\gamma_i$ for $\mathsf{W}_i$ such that $\gamma_1\cup\gamma_2\cup\cdots\cup\gamma_k$ is an ordered basis for $\mathsf{V}$.

#### Theorem 5.11

A linear operator $\mathsf{T}$ on a finite-dimensional vector space $\mathsf{V}$ is diagonalizable if and only if $\mathsf{V}$ is the direct sum of the eigenspaces of $\mathsf{T}$.

### Selected Exercises

#### 8

By Theorem 5.7, the multiplicity of $\lambda_1$ is no less than $n-1$, since the multiplicity of $\lambda_2$ is at least 1, we conclude that the multiplicity of $\lambda_1$ can only be $n-1$ and the multiplicity of $\lambda_2$ is equal to 1, this means the multiplicity of $\lambda_i$ is equal to $\dim(\mathsf{E}_{\lambda_i})$ for $i=1,2$. Thus $A$ is diagonalizable.

#### 9

Denote $[\mathsf{T}]_{\beta}=A$, which is upper triangular, and denote $f(t)$ to be the characteristic polynomial of $\mathsf{T}$, to prove (a), we have
$$
f(t)=\det(A-tI_n)=\prod_{i=1}^n(A_{ii}-t)
$$
which splits. This procedure also verifies (b).

#### 10

Use Exercise 9, we know the eigenvalues of $\mathsf{T}$ must be the diagonal entires of $[\mathsf{T}]_{\beta}$, and the next conclusion follows from the expression of  the characteristic polynomial of $\mathsf{T}$ in $t$ and entries of $[\mathsf{T}]_{\beta}$.

#### 11

The characteristic polynomial of $A$ has the form $(x-\lambda_1)^{m_1}\cdots(x-\lambda_k)^{m_k}$, which is also the characteristic of the upper triangular matrix $A'$ that $A$ is similar to. Notice that $\text{tr}(A)=\text{tr}(A')$ and $\det(A)=\det(A')$. Use exercise 10, the diagonal entries of $A'$ are $\lambda_1,\dots,\lambda_k$ and each $\lambda_i$ occur $m_i$ times, this means $\text{tr}(A')=\sum_{i=1}^km_i\lambda_i$ and $\det(A')=\prod_{i=1}^k(\lambda_i)^{m_i}$.

#### 12

$\mathsf{T}$ is invertible guarantees that all eigenvalues of $\mathsf{T}$ are nonzero.

(a) We denote $\mathsf{E}_{\lambda}^{\mathsf{T}}$ to be the eigenspace of $\mathsf{T}$ corresponding to $\lambda$ and  $\mathsf{E}_{\lambda^{-1}}^{\mathsf{T}^{-1}}$ to be the eigenspace of $\mathsf{T}^{-1}$ corresponding to $\lambda^{-1}$.   then
$$
v\in\mathsf{E}_{\lambda}^{\mathsf{T}}\iff\mathsf{T}(v)=\lambda v\iff\mathsf{T}^{-1}(v)=\lambda^{-1} v\iff v\in\mathsf{E}_{\lambda^{-1}}^{\mathsf{T}^{-1}}
$$
(b) If $\mathsf{T}$ is diagonalizable, then the characteristic polynomial of $\mathsf{T}$ splits, let $\lambda_1,\lambda_2,\dots,\lambda_k$ be the distinct eigenvalues of $\mathsf{T}$, choose  $\beta_i$ as an ordered basis for $\mathsf{E}_{\lambda_i}$ for each $i$, then $\beta=\beta_1\cup\beta_2\cup\cdots\cup\beta_k$ is an ordered basis for $\mathsf{V}$, use (a) we see that $\beta_i$ is an ordered basis for $\mathsf{E}_{\lambda^{-1}}^{\mathsf{T}^{-1}}$ for each $i$, thus $\beta$ consists of eigenvectors of $\mathsf{T}^{-1}$, this means $\mathsf{T}^{-1}$ is diagonalizable.

#### 13

(a) Let $A=\begin{pmatrix}1&1\\0&1\end{pmatrix}$, then $\mathsf{E}_1=\{(a,0):a\ne0\}$, and $\mathsf{E}'_1=\{(0,a):a\ne0\}$.

(b) Since $(A^t-\lambda I_n)=(A-\lambda I_n)^t$, we see than $\text{rank}(A^t-\lambda I_n)=\text{rank}(A-\lambda I_n)$, thus
$$
\dim(\mathsf{E}_{\lambda})=n-\text{rank}(A-\lambda I_n)=n-\text{rank}(A^t-\lambda I_n)=\dim(\mathsf{E}'_{\lambda})
$$
(c) If $A$ is diagonalizable, then the multiplicity of $\lambda_i$ is equal to $\dim(\mathsf{E}_{\lambda_i})$ for all $i$, which means the multiplicity of $\lambda_i$ is equal to $\dim(\mathsf{E}'_{\lambda_i})$ for all $i$, thus $A^t$ is diagonalizable.

#### 17

(a) Let $\gamma$ be the ordered basis for $\mathsf{V}$ such that $[\mathsf{T}]_{\gamma}$ and $[\mathsf{U}]_{\gamma}$ are diagonal, for any ordered basis $\beta$, let $Q=[\mathsf{I_V}]_{\gamma}^{\beta}$, then we see that $Q^{-1}[\mathsf{T}]_{\beta}Q=[\mathsf{T}]_{\gamma}$ and $Q^{-1}[\mathsf{U}]_{\beta}Q=[\mathsf{U}]_{\gamma}$ are both diagonal.

(b) Let $Q$ be the invertible $n\times n$ matrix such that $A'=Q^{-1}AQ$ and $B'=Q^{-1}BQ$ are diagonal, let $q_i$ be the $i$th column of $Q$, then $\beta=\{q_1,\dots,q_n\}$ is linearly independent and thus a basis for $\mathsf{F}^n$, then we have
$$
\begin{aligned}
&\qquad AQ=Q\begin{pmatrix}
A'_{11}&&
\\&{\ddots}&
\\&&A'_{nn}
\end{pmatrix}\\&\implies\begin{pmatrix}Aq_1&\cdots&Aq_n\end{pmatrix}=\begin{pmatrix}A'_{11}q_1&\cdots&A'_{nn}q_n\end{pmatrix}\\&\implies\mathsf{L}_A(q_i)=A'_{ii}q_i
\end{aligned}
$$
and similarly, $\mathsf{L}_B(q_i)=B'_{ii}q_i$ for all $i$, so $\mathsf{L}_A$ and $\mathsf{L}_B$ are simultaneously diagonalizable.

#### 18

(a) Let $\beta=\{\beta_1,\dots,\beta_n\}$ be the basis such that $A=[\mathsf{T}]_{\beta}$ and $B=[\mathsf{U}]_{\beta}$ are diagonal, then $\mathsf{T}(\beta_i)=A_{ii}\beta_i$ and $\mathsf{U}(\beta_i)=B_{ii}\beta_i$ for all $i$. For any $v\in\mathsf{V}$, write $v=\sum_{i=1}^nc_i\beta_i$ for scalars $c_i$, then
$$
\begin{aligned}
\mathsf{TU}(v)&=\sum_{i=1}^nc_i\mathsf{TU}(\beta_i)=\sum_{i=1}^nc_iA_{ii}B_{ii}\beta_i\\&=\sum_{i=1}^nc_iB_{ii}A_{ii}\beta_i=\sum_{i=1}^nc_i\mathsf{UT}(\beta_i)=\mathsf{UT}(v)
\end{aligned}
$$
(b) Let $Q$ be the invertible $n\times n$ matrix such that $A'=Q^{-1}AQ$ and $B'=Q^{-1}BQ$ are diagonal, notice that $A'B'=B'A'$, thus
$$
Q^{-1}ABQ=Q^{-1}AQQ^{-1}BQ=A'B'=B'A'=Q^{-1}BAQ\implies AB=BA
$$

#### 19

Let $\beta=\{\beta_1,\dots,\beta_n\}$ be the basis such that $A=[\mathsf{T}]_{\beta}$ is diagonal, then $\mathsf{T}(\beta_i)=A_{ii}\beta_i$ for all $i$, this means $\mathsf{T}^m(\beta_i)=A_{ii}^m\beta_i$ for all $i$, thus $[\mathsf{T}^m]_{\beta}$​ is a diagonal matrix.

#### 20

Suppose $\mathsf{V}$ is the direct sum of $\mathsf{W}_1,\dots,\mathsf{W}_k$, by Theorem 5.10(e), there exists an ordered basis $\gamma_i$ for $\mathsf{W}_i$ such that $\gamma_1\cup\gamma_2\cup\cdots\cup\gamma_k$ is an ordered basis for $\mathsf{V}$, this shows $\dim(\mathsf{V})=\sum_{i=1}^k\dim(\mathsf{W}_i)$. Conversely, if $\dim(\mathsf{V})=\sum_{i=1}^k\dim(\mathsf{W}_i)$, let $\gamma_i$ be an ordered basis for $\mathsf{W}_i$ ($1\le i\le k$), then $\gamma_1\cup\gamma_2\cup\cdots\cup\gamma_k$ spans $\mathsf{V}$, but the set has number of $\dim(\mathsf{V})$ vectors, thus is a basis for $\mathsf{V}$, by Theorem 5.10(d),  $\mathsf{V}$ is the direct sum of $\mathsf{W}_1,\dots,\mathsf{W}_k$​.

#### 21

Denote $\mathsf{W}_i=\text{span}(\beta_i)$ for $i=1,\dots,k$, then each $\beta_i$ is a basis for $\mathsf{W}_i$, by Theorem 5.10(d) we can deduce (a).

#### 22

Let $\mathsf{W}=\text{span}\{x\in\mathsf{V}:x\text{ is an eigenvector of }\mathsf{T}\}$. If $v\in\mathsf{W}$, then $v$ must belong to one $\mathsf{E}_{\lambda_i}$ for $i=1,\dots,k$, thus $W=\sum_{i=1}^k\mathsf{E}_{\lambda_i}$. Then use Lemma before Theorem 5.8 and Theorem 5.10(b), we get the result.

#### 23

It is easy to see that $\mathsf{W}_1+\mathsf{W}_2=\mathsf{W}_1\oplus\mathsf{W}_2$ by definition. We prove $\mathsf{W}_1+\mathsf{W}_2$ is the direct sum of $\mathsf{K}_i$ and $\mathsf{M}_j$ use Theorem 5.10(b). Let $v_i\in\mathsf{K}_i$ and $u_j\in\mathsf{M}_j$ for $1\le i\le p$ and $1\le j\le q$ such that 
$$
v_1+\cdots+v_p+u_1+\cdots+u_q=0
$$
let $v=\sum_{i=1}^pv_i$ and $u=\sum_{j=1}^qu_j$, we have $v\in\mathsf{W}_1$ and $u\in\mathsf{W}_2$ and $v=-u$, thus $v=u=0$. Since $\mathsf{W}_1$ is the direct sum of $\mathsf{K}_i$ and $\mathsf{W}_2$ is the direct sum of $\mathsf{M}_j$, we can conclude $v_1=\cdots=v_p=0$ and $u_1=\cdots=u_q=0$. Then use Theorem 5.10(b) we get the result.

### Summary

对角化问题在5.1节只有初步的探讨，即如果存在全部由特征向量组成的基，则线性变换是对角化的。但反方向的讨论，即给定一个线性变换，如何判断其是否能对角化，并且如果可对角化时如何找出全部由特征向量组成的基，会在本节展开。定理5.5证明属于不同特征值的特征向量是线性无关的。由此推论在n维空间有n个特征值的线性变换是可对角化的。但是如果特征值较少，也有可能对角化，定理5.6证明，可对角化线性变换的特征多项式是split的，也即没有二次项以上的因式。如果特征值不够n，且特征多项式split，那么一部分特征值的对应因式就会在特征多项式中出现多次，这个出现的次数称为该特征值的multiplicity，而属于每一个特征值的特征向量从属于一个子空间，即$T-\lambda I$的零空间，这个空间称为该特征向量的特征空间，定理5.7证明，特征空间的维数在1和特征值的multiplicity之间。通过一些例子（例3和例4）说明，一个特征多项式split的线性变换是否可对角化，每个特征空间维数是否等于对应特征值multiplicity似乎是一个判断方式。定理5.8给出了一个构造线性无关特征向量集的方式，即把每个特征空间的基组合起来，定理5.9证明这种组合起来的集合恰是整个空间的一组基。至此，T对角化的判别条件出炉：T的特征多项式split且每个特征值的multiplicity等于特征空间的维数$n-\text{rank}(T-\lambda I)$。本节最后一部分内容介绍了对角化的一些应用，例如解微分方程，研究直和结构，其中直和结构的定理5.11给出了对角化的另一个等价条件，即V是T特征空间的直和。