# Exercise 23-26 (Inequalities)

### 1.23

Prove Lagrange's identity for real numbers:
$$
\left(\sum_{k=1}^na_kb_k\right)^2=\left(\sum_{k=1}^na_k^2\right)\left(\sum_{k=1}^nb_k^2\right)-\sum_{1\leq k<j\leq n}(a_kb_j-a_jb_k)^2.
$$
Note that this identity implies the Cauchy-Schwarz inequality.

#### Proof

Use induction. For $n=1$, we have $(a_1b_1)^2=a_1^2b_1^2$ and the identity is valid.
Suppose the identity is valid for $n=m-1$, then
$$
\begin{aligned}
\left(\sum_{k=1}^{m}a_kb_k\right)^2&=\left(\sum_{k=1}^{m-1}a_kb_k+(a_{m}b_{m})\right)^2
\\&=\left(\sum_{k=1}^{m-1}a_kb_k\right)^2+a_{m}^2b_{m}^2+2a_{m}b_{m}\sum_{k=1}^{m-1}a_kb_k
\\&=\left(\sum_{k=1}^{m-1}a_k^2\right)\left(\sum_{k=1}^{m-1}b_k^2\right)+a_{m}^2b_{m}^2+2a_{m}b_{m}\sum_{k=1}^{m-1}a_kb_k-\sum_{1\leq k<j\leq m-1}(a_kb_j-a_jb_k)^2
\end{aligned}
$$
Denote $A_m=\sum_{k=1}^{m}a_k^2$ and $B_m=\sum_{k=1}^{m}b_k^2$, then
$$
A_mB_m=(A_{m-1}+a_m^2)(B_{m-1}+b_m^2)=A_{m-1}B_{m-1}+A_{m-1}b_m^2+B_{m-1}a_m^2+a_m^2b_m^2
$$
thus
$$
\begin{aligned}
&\quad A_{m-1}B_{m-1}+a_m^2b_m^2+2a_mb_m\sum_{k=1}^{m-1}a_kb_k
\\&=A_mB_m-A_{m-1}b_m^2-B_{m-1}a_m^2+2a_mb_m\sum_{k=1}^{m-1}a_kb_k
\\&=A_mB_m-\sum_{k=1}^{m-1}(a_kb_m-a_mb_k)^2
\end{aligned}
$$
which means
$$
\begin{aligned}
\left(\sum_{k=1}^{m}a_kb_k\right)^2&=A_mB_m-\sum_{k=1}^{m-1}(a_kb_m-a_mb_k)^2-\sum_{1\leq k<j\leq m-1}(a_kb_j-a_jb_k)^2
\\&=A_mB_m-\sum_{1\leq k<j\leq m}(a_kb_j-a_jb_k)^2
\end{aligned}
$$
thus the identity is valid for $n=m$.

### 1.24

Prove that for arbitrary real $a_k,b_k,c_k$ we have
$$
\left(\sum_{k=1}^na_kb_kc_k\right)^4\leq\left(\sum_{k=1}^na_k^4\right)\left(\sum_{k=1}^nb_k^2\right)^2\left(\sum_{k=1}^nc_k^4\right).
$$

#### Proof

use Theorem 1.23 (Cauchy-Schwarz inequality) twice, we have
$$
\begin{aligned}
\left(\sum_k{a_kb_kc_k}\right)^4&=\left(\left(\sum_k{a_kb_kc_k}\right)^2\right)^2\leq\left(\sum_k(a_kc_k)^2\sum_kb_k^2\right)^2
\\&=\left(\sum_k(a_k^2)(c_k)^2\right)^2\left(\sum_kb_k^2\right)^2
\\&\leq\left(\sum_ka_k^4\sum_kc_k^4\right)\left(\sum_kb_k^2\right)^2
\end{aligned}
$$

### 1.25

Prove Minkowski's inequality:
$$
\left(\sum_{k=1}^n(a_k+b_k)^2\right)^{1/2}\leq\left(\sum_{k=1}^na_k^2\right)^{1/2}+\left(\sum_{k=1}^nb_k^2\right)^{1/2}.
$$
This is the triangle inequality $\|{a+b}\|\leq\|{a}\|+\|{b}\|$ for $n$-dimensional vectors.

#### Proof

From Cauchy-Schwarz inequality we have
$$
2\sum_k{(a_kb_k)}\leq 2\left(\sum_ka_k^2\right)^{1/2}\left(\sum_kb_k^2\right)^{1/2}
$$
thus
$$
\begin{aligned}
\sum_k(a_k+b_k)^2&=\sum_ka_k^2+\sum_kb_k^2+2\sum_k(a_kb_k)
\\&\leq\sum_ka_k^2+\sum_kb_k^2+2\left(\sum_ka_k^2\right)^{1/2}\left(\sum_kb_k^2\right)^{1/2}
\\&=\left(\left(\sum_ka_k^2\right)^{1/2}+\left(\sum_kb_k^2\right)^{1/2}\right)^2
\end{aligned}
$$
the inequality follows by taking square roots at both sides.

### 1.26

If $a_1\geq a_2\geq\cdots\geq a_n$ and $b_1\geq b_2\geq\cdots\geq b_n$, prove that
$$
\left(\sum_{k=1}^na_k\right)\left(\sum_{k=1}^nb_k\right)\leq n\sum_{k=1}^na_kb_k.
$$

#### Proof

Use the notation $[(A_{ij})]$ to define the expression which add all element of the matrix $A_{ij}$. From the condition given, we have $\sum_{1\leq j\leq k\leq n}(a_k-a_j)(b_k-b_j)\geq 0$, which means
$$
\sum_{1\leq j\leq k\leq n}(a_kb_k+a_jb_j)\geq\sum_{1\leq j\leq k\leq n}(a_kb_j+a_jb_k)\tag{1}
$$
Next some simple calculation shows
$$
\left(\sum_{k=1}^na_k\right)\left(\sum_{k=1}^nb_k\right)=\left[\begin{pmatrix}a_1b_1&{\cdots}&a_1b_n
\\{\vdots}&&{\vdots}
\\a_nb_1&{\cdots}&a_nb_n
\end{pmatrix}\right]
$$
and still simple calculation shows
$$
\sum_{1\leq j\leq k\leq n}a_kb_j=\left[\begin{pmatrix}a_1b_1&&
\\{\vdots}&{\ddots}&
\\a_nb_1&{\cdots}&a_nb_n
\end{pmatrix}\right],\\
\sum_{1\leq j\leq k\leq n}a_jb_k=\left[\begin{pmatrix}a_1b_1&{\cdots}&a_1b_n
\\&{\ddots}&{\vdots}
\\&&a_nb_n
\end{pmatrix}\right]
$$
thus
$$
\begin{aligned}
\sum_{1\leq j\leq k\leq n}(a_kb_j+a_jb_k)&=\left[\begin{pmatrix}a_1b_1&{\cdots}&a_1b_n
\\{\vdots}&&{\vdots}
\\a_nb_1&{\cdots}&a_nb_n
\end{pmatrix}\right]+\sum_{k=1}^na_kb_k
\\&=\left(\sum_{k=1}^na_k\right)\left(\sum_{k=1}^nb_k\right)+\sum_{k=1}^na_kb_k
\end{aligned}\tag{2}
$$
Also, we have
$$
\begin{aligned}
&\quad\sum_{1\leq j\leq k\leq n}(a_kb_k+a_jb_j)\\&=\left[\begin{pmatrix}
a_1b_1+a_1b_1&a_1b_1+a_2b_2&{\cdots}&a_1b_1+a_nb_n
\\&a_2b_2+a_2b_2&{\cdots}&a_2b_2+a_nb_n
\\&&{\ddots}&
\\&&&a_nb_n+a_nb_n
\end{pmatrix}\right]
\\&=(n+1)\sum_{k=1}^na_kb_k\end{aligned}\tag{3}
$$
Combine expression 1,2,3, we get the result.