# The Change of Coordinate Matrix

### Content Notes

#### Theorem 2.22

Let $\beta$ and $\beta'$ be two ordered bases for a finite-dimensional vector space $\mathsf{V}$, and let $Q=[\mathsf{I_V}]_{\beta'}^{\beta}$. Then

(a) $Q$ is invertible.

(b) For any $v\in V$, $[v]_{\beta}=Q[v]_{\beta'}$.

The matrix $Q=[\mathsf{I_V}]_{\beta'}^{\beta}$ is called a **change of coordinate matrix**, we say that $Q$ **changes $\beta'$-coordinates into $\beta$-coordinates**. 

#### Theorem 2.23

Let $\mathsf{T}$ be a linear operator on a finite-dimensional vector space $\mathsf{V}$, and let $\beta$ and $\beta'$ be ordered bases for $\mathsf{V}$. Suppose that $Q$ is the change of coordinate matrix that changes $\beta'$-coordinates into $\beta$-coordinates. Then $[\mathsf{T}]_{\beta'}=Q^{-1}[\mathsf{T}]_{\beta}Q$.

##### Corollary

Let $A\in\mathsf{M}_{n\times n}(F)$, and let $\gamma$ be an ordered basis for $\mathsf{F}^n$. Then $[\mathsf{L}_A]_{\gamma}=Q^{-1}AQ$, where $Q$ is the $n\times n$ matrix whose $j$th column is  the $j$th vector of $\gamma$.

#### Definition

Let $A$ and $B$ be matrices in $\mathsf{M}_{n\times n}(F)$. We say that $B$ is **similar** to $A$ if there exists an invertible matrix $Q$ such that $B=Q^{-1}AQ$.

### Selected Exercises

#### 2

Recall that $Q=[\mathsf{I_V}]_{\beta'}^{\beta}$ and the $j$th column of $Q$ is $[x_j']_{\beta}$, so

(b) We have
$$
(0,10)=4(-1,3)+2(2,-1)
\\
(5,0)=(-1,3)+3(2,-1)
$$
thus $Q=\begin{pmatrix}4&-1\\2&3\end{pmatrix}$.

(d) We have
$$
(2,1)=2(-4,3)+5(2,-1),\quad (-4,1)=-(-4,3)-4(2,-1)
$$
thus $Q=\begin{pmatrix}2&-1\\5&-4\end{pmatrix}$.

#### 3

(b) It is easy to see that $Q=\begin{pmatrix}a_0&b_0&c_0\\a_1&b_1&c_1\\a_2&b_2&c_2\end{pmatrix}$.

(d) $Q=\begin{pmatrix}2&1&1\\3&-2&1\\-1&3&1\end{pmatrix}$.

(f) $Q=\begin{pmatrix}-2&1&2\\3&4&1\\-1&5&2\end{pmatrix}$.

#### 6

(b) We have
$$
A\beta_1=\begin{pmatrix}1&2\\2&1\end{pmatrix}\begin{pmatrix}1\\1\end{pmatrix}=\begin{pmatrix}3\\3\end{pmatrix}=3\begin{pmatrix}1\\1\end{pmatrix}+0\begin{pmatrix}1\\-1\end{pmatrix}
\\
A\beta_2=\begin{pmatrix}1&2\\2&1\end{pmatrix}\begin{pmatrix}1\\-1\end{pmatrix}=\begin{pmatrix}-1\\1\end{pmatrix}=0\begin{pmatrix}1\\1\end{pmatrix}+(-1)\begin{pmatrix}1\\-1\end{pmatrix}
$$
so $[\mathsf{L}_A]_{\beta}=\begin{pmatrix}3&0\\0&-1\end{pmatrix}$, and by corollary of Theorem 2.23, we have $Q=\begin{pmatrix}1&1\\1&-1\end{pmatrix}$.

(d) We have
$$
A\beta_1=\begin{pmatrix}13&1&4\\1&13&4\\4&4&10\end{pmatrix}\begin{pmatrix}1\\1\\-2\end{pmatrix}=\begin{pmatrix}6\\6\\-12\end{pmatrix}=6\beta_1
\\
A\beta_2=\begin{pmatrix}13&1&4\\1&13&4\\4&4&10\end{pmatrix}\begin{pmatrix}1\\-1\\0\end{pmatrix}=\begin{pmatrix}12\\-12\\0\end{pmatrix}=12\beta_2
\\
A\beta_3=\begin{pmatrix}13&1&4\\1&13&4\\4&4&10\end{pmatrix}\begin{pmatrix}1\\1\\1\end{pmatrix}=\begin{pmatrix}18\\18\\ 18\end{pmatrix}=18\beta_3
$$
so $[\mathsf{L}_A]_{\beta}=\begin{pmatrix}6&0&0\\0&12&0\\0&0&18\end{pmatrix}$, and $Q=\begin{pmatrix}1&1&1\\1&-1&1\\-2&0&1\end{pmatrix}$.

#### 7

(b) We have when $m>0$, 
$$
\mathsf{T}(1,0)=\left(\frac{\cos(\arctan(m))}{\sqrt{1+m^2}},\frac{m\cos(\arctan(m))}{\sqrt{1+m^2}}\right),\\
\mathsf{T}(0,1)=\left(\frac{\sin(\arctan(m))}{\sqrt{1+m^2}},\frac{m\sin(\arctan(m))}{\sqrt{1+m^2}}\right)
$$
thus 
$$
\mathsf{T}(x,y)=\left(\frac{x\cos(\arctan(m))+y\sin(\arctan(m))}{\sqrt{1+m^2}},\frac{mx\cos(\arctan(m))+my\sin(\arctan(m))}{\sqrt{1+m^2}}\right)
$$
the calculation is similar when $m<0$.

#### 8

By the definition of $Q$ and $P$ we can write $Q=[\mathsf{I_V}]_{\beta'}^{\beta}$ and $P=[\mathsf{I_W}]_{\gamma'}^{\gamma}$, and both $Q$ and $P$ are invertible. From $\mathsf{T}=\mathsf{I_W T I_V}$​ we have
$$
[\mathsf{T}]_{\beta'}^{\gamma'}=[\mathsf{I_W}]_{\gamma}^{\gamma'}[\mathsf{T}]_{\beta'}^{\gamma}=[\mathsf{I_W}]_{\gamma}^{\gamma'}[\mathsf{T}]_{\beta}^{\gamma}[\mathsf{I_V}]_{\beta}^{\beta'}=[[\mathsf{I_W}]_{\gamma'}^{\gamma}]^{-1}[\mathsf{T}]_{\beta}^{\gamma}[\mathsf{I_V}]_{\beta}^{\beta'}=P^{-1}[\mathsf{T}]_{\beta}^{\gamma}Q
$$

#### 9

Let $A,B,C\in\mathsf{M}_{n\times n}(F)$, then

$A$ is similar to $A$: we have $A=I_n^{-1}AI_n$.

$A$ is similar to $B$, then there exists invertible $Q$ such that $B=Q^{-1}AQ$, which means $A=QBQ^{-1}=(Q^{-1})^{-1}BQ^{-1}$, and since $Q^{-1}$ is invertible, $B$ is similar to $A$.

If $A$ is similar to $B$ and $B$ is similar to $C$, then there exists invertible $P,Q$ such that $B=Q^{-1}AQ,C=P^{-1}BP$, then we  have $C=P^{-1}(Q^{-1}AQ)P=(QP)^{-1}A(QP)$, the matrix $QP$ is invertible.

#### 10

Use Exercise 13 of Section 2.3 we have $\text{tr}(B)=\text{tr}(Q^{-1}AQ)=\text{tr}(AQQ^{-1})=\text{tr}(A)$.

#### 11

(a) By definition, $Q=[\mathsf{I_V}]_{\alpha}^{\beta}$ and $R=[\mathsf{I_V}]_{\beta}^{\gamma}$, then by Theorem 2.11 we have $RQ=[\mathsf{I_V}]_{\beta}^{\gamma}[\mathsf{I_V}]_{\alpha}^{\beta}=[\mathsf{I_V I_V}]_{\alpha}^{\gamma}=[\mathsf{I_V}]_{\alpha}^{\gamma}$, which is the matrix that change $\alpha$-coordinates into $\gamma$-coordinates.

(b) If $Q=[\mathsf{I_V}]_{\alpha}^{\beta}$, then $Q^{-1}=([\mathsf{I_V}]_{\alpha}^{\beta})^{-1}=[(\mathsf{I_V})^{-1}]_{\beta}^{\alpha}=[(\mathsf{I_V})]_{\beta}^{\alpha}$ by Theorem 2.18.

#### 12

Let $\beta$ be the standard ordered basis for $\mathsf{F}^n$, then Theorem 2.15(a) shows that $[\mathsf{L}_A]_{\beta}=A$, use Theorem 2.23, suppose that $Q$ is the change of coordinate matrix that changes $\gamma$-coordinates into $\beta$-coordinates. Then $[\mathsf{L}_A]_{\gamma}=Q^{-1}[\mathsf{L}_A]_{\beta}Q=Q^{-1}AQ$. And $Q=[\mathsf{I}]_{\gamma}^{\beta}$ is the $n\times n$ matrix whose $j$th column is  the $j$th vector of $\gamma$, since 
$$
\gamma_j=[\gamma_j]_{\beta}=Q[\gamma_j]_{\gamma}=Q\beta_j
$$
the equation above means the $j$th vector of $\gamma$, which remains itself under the standard ordered basis, equals $Q[\gamma_j]_{\gamma}$ by Theorem 2.22(b), and $[\gamma_j]_{\gamma}$ is in fact $\beta_j$, and then $Q\beta_j$ is the $j$th column of $Q$.

#### 13

It suffices to show that $\beta'$ is linearly independent. Let $c_1,\dots,c_n$ be scalars such that
$$
c_1x_1'+\cdots+c_nx_n'=0\implies\sum_{j=1}^nc_j\sum_{i=1}^nQ_{ij}x_i=\sum_{i=1}^n\left(\sum_{j=1}^nc_jQ_{ij}\right)x_i=0
$$
which means $\sum_{j=1}^nc_jQ_{ij}=0$ for $1\le i\le n$, this condition is equivalent to
$$
\begin{pmatrix}Q_{11}&\cdots&Q_{1n}\\&\cdots&\\Q_{n1}&\cdots&Q_{nn}\end{pmatrix}\begin{pmatrix}c_1\\{\vdots}\\c_n\end{pmatrix}=Q\begin{pmatrix}c_1\\{\vdots}\\c_n\end{pmatrix}=\begin{pmatrix}0\\{\vdots}\\0\end{pmatrix}
\implies\begin{pmatrix}c_1\\{\vdots}\\c_n\end{pmatrix}=Q^{-1}\begin{pmatrix}0\\{\vdots}\\0\end{pmatrix}=\begin{pmatrix}0\\{\vdots}\\0\end{pmatrix}
$$
and the proof is complete.

### Summary

本节名为如何转换系数矩阵，最后引出了相似这一重要概念。最开始通过一些例子说明系数矩阵的转换实质是一种可看作“换元”的东西。定理2.22详细说明了将$\beta'$坐标转换为$\beta$​坐标的矩阵是什么含义，这个矩阵是可逆的。定理2.23进一步说明这个转换不同基下坐标的矩阵还可以将线性变换在不同基下的矩阵表示联系起来。如果从矩阵视角看，可定义相似的概念。