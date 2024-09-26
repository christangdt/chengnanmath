# Matrix Limits and Markov Chains

### Content Notes

#### Definition (converge)

Let $L,A_1,A_2,\dots$ be $n\times p$ matrices having complex entries. The sequence $A_1,A_2,\dots$ is said to **converge** to the $n\times p$ matrix $L$, called the **limit** of the sequence, if
$$
\lim_{m\to\infty}(A_m)_{ij}=L_{ij}
$$
for all $1\le i\le n$ and $1\le j\le p$. We write $\lim_{m\to\infty}A_m=L$.

#### Theorem 5.12

Let $A_1,A_2,\dots$ be a sequence of $n\times p$ matrices with complex entries that converges to the matrix $L$. Then for any $P\in\mathsf{M}_{r\times n}(C)$ and $Q\in\mathsf{M}_{p\times s}(C)$, 
$$
\lim_{m\to\infty}PA_m=PL,\quad\lim_{m\to\infty}A_mQ=LQ
$$

##### Corollary

Let $A\in\mathsf{M}_{n\times n}(C)$ be such that $\lim_{m\to\infty}A^m=L$. Then for any invertible matrix $Q\in\mathsf{M}_{n\times n}(C)$, 
$$
\lim_{m\to\infty}(QAQ^{-1})^m=QLQ^{-1}.
$$

#### Theorem 5.13

Let $A$ be a square matrix with complex entries. Then $\lim_{m\to\infty}A^m$ exists if and only if both of the following conditions holds.

(a) Every eigenvalue of $A$ is contained in $S$.

(b) If $1$ is an eigenvalue of $A$, then the dimension of the eigenspace corresponding to $1$ equals the multiplicity of $1$ as an eigenvalue of $A$.

#### Theorem 5.14

Let $A\in\mathsf{M}_{n\times n}(C)$ satisfying the following two conditions.

(i) Every eigenvalue of $A$ is contained in $S$.

(ii) $A$ is diagonalizable.

Then $\lim_{m\to\infty}A^m$ exists.



### Temp: Exercise of 5.2

#### 21

Denote $\mathsf{W}_i=\text{span}(\beta_i)$ for $i=1,\dots,k$, then each $\beta_i$ is a basis for $\mathsf{W}_i$, 