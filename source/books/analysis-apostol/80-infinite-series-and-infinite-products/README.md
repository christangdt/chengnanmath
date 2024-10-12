# Infinite Series and Infinite Products

## Sequences

#### Definition 8.1

首先给出在复数域上的序列收敛的定义：

*A sequence of points in $\mathbf{C}$ is said to converge if there is a point $p$ in $\mathbf{C}$ with the following property: For every $\varepsilon>0$ there is an integer $N$ (depending on $\varepsilon$) such that $|a_n-p|<\varepsilon$ whenever $n\ge N$.*

#### Definition 8.2

序列的上极限和下极限，并不是很好理解的定义，上极限是指序列最终会始终不大于U，但是有无穷多个元素能够无限接近U。

*Let $\{a_n\}$ be a sequence of real numbers. Suppose there is a real number $U$ satisfying the following two conditions:*

*i) For every $\varepsilon>0$ there exists an integer $N$ such that $n>N$ implies $a_n<U+\varepsilon$.*

*ii) Given $\varepsilon>0$ and given $m>0$, there exists an integer $n>m$ such that $a_n>U-\varepsilon$.*

*Then $U$ is called the limit superior (or upper limit) of $\{a_n\}$ and we write*
$$
U=\limsup_{n\to\infty}a_n.
$$
*Statement (i) implies that the set $\{a_1,a_2,\dots\}$ is bounded above. If this set is not bounded above, we define*
$$
\limsup_{n\to\infty}a_n=+\infty.
$$
*If the set is bounded above but not bounded below and if $\{a_n\}$ has no finite limit superior, then we say $\limsup_{n\to\infty}a_n=-\infty$. The limit inferior (or lower limit) of $\{a_n\}$ is defined as follows*
$$
\liminf_{n\to\infty}a_n=-\limsup_{n\to\infty}b_n,\quad\text{where }b_n=-a_n\quad\text{for }n=1,2,\dots
$$
条件i和ii说明U是唯一的。习题8.1可以说明，在广义实数系$\mathbf{R}^*$中，任何序列都有一个上极限和一个下极限。

#### Theorem 8.3

*Let $\{a_n\}$ be a sequence of real numbers. Then we have:*

*a) $\liminf_{n\to\infty}a_n\le\limsup_{n\to\infty}a_n$.*

*b) The sequence converges if and only if, $\limsup_{n\to\infty}a_n$ and $\liminf_{n\to\infty}a_n$ are both finite and equal, in which case $\lim_{n\to\infty}a_n=\limsup_{n\to\infty}a_n=\liminf_{n\to\infty}a_n$.*

*c) The sequence diverges to $+\infty$ if and only if $\limsup_{n\to\infty}a_n=\liminf_{n\to\infty}a_n=+\infty$.*

*d) The sequence diverges to $-\infty$ if and only if $\limsup_{n\to\infty}a_n=\liminf_{n\to\infty}a_n=-\infty$.*

#### Theorem 8.4

Assume that $a_n\le b_n$ for each $n=1,2,\dots$. Then we have:
$$
\liminf_{n\to\infty}a_n\le\liminf_{n\to\infty}b_n,\qquad\limsup_{n\to\infty}a_n\le\limsup_{n\to\infty}b_n
$$

#### Definition 8.5

*Let $\{a_n\}$ be a sequence of real numbers. We say the sequence is increasing and we write $a_n\nearrow$ if $a_n\le a_{n+1}$ for $n=1,2,\dots$. We say the sequence is decreasing and we write $a_n\searrow$ if $a_n\ge a_{n+1}$ for all $n$. A sequence is called monotonic if it is increasing or if it is decreasing.*  

#### Theorem 8.6

*A monotonic sequence converges if, and only if, it is bounded.*

## Series

### Infinite series

对于给定的序列$\{a_n\}$， 定义一个新的序列$\{s_n\}$，其中$s_n=\sum_{k=1}^na_k$, 则：

#### Definition 8.7

*The ordered pair of sequences ($\{a_n\}, \{s_n\})$ is called an infinite series. The number $s_n$ is called the $n$th partial sum of the series. The series is said to converge or to diverge according as $\{s_n\}$ is convergent or divergent.*

#### Theorem 8.8

*Let $a=\sum a_n$ and $b=\sum b_n$ be convergent series. Then, for every pari of constants $\alpha$ and $\beta$, the series $\sum(\alpha a_n+\beta b_n)$ converges to the sum $\alpha a+\beta b$.*

#### Theorem 8.9

*Assume that $a_n\ge0$ for each $n = 1, 2, \dots$. Then $\sum a_n$ converges if, and only if, the sequence of partial sums is bounded above.*  

#### Theorem 8.10 (Telescoping series)

*Let $\{a_n\}$ and $\{b_n\}$ be two sequences such that $a_n=b_{n+1}-b_n$ for $n=1,2,\dots$. Then $\sum a_n$ converges if, and only if, $\lim_{n\to\infty}b_n$ exists, in which case we have $\sum_{n=1}^{\infty}a_n=\lim_{n\to\infty}b_n-b_1$.*

#### Theorem 8.11 (Cauchy condition for series)

*The series $\sum a_n$ converges if and only if for every $\varepsilon>0$ there exists an integer $N$ such that $n>N$ implies*
$$
|a_{n+1}+\cdots+a_{n+p}|<\varepsilon\quad\text{for each }p=1,2,\dots
$$

### About parentheses

#### Definition 8.12

*Let $p$ be a function whose domain is the set of positive integers and whose range is a subset of the positive integers such that $p(n)<p(m)$ if $n<m$. Let $\sum a_n$ and $\sum b_n$ be two series related as follows:*
$$
b_1=a_1+a_2+\cdots+a_{p(1)},
\\
b_{n+1}=a_{p(n)+1}+a_{p(n)+2}+\cdots+a_{p(n+1)},\quad\text{if }n=1,2,\dots
$$
*Then we say that $\sum b_n$ is obtained from $\sum a_n$ by inserting parentheses, and that $\sum a_n$ is obtained from $\sum b_n$ by removing parentheses.*

#### Theorem 8.13

*If $\sum a_n$ converges to $s$, every series $\sum b_n$ obtained from $\sum a_n$ by inserting parentheses also converges to $s$.*

#### Theorem 8.14

*Let $\sum a_n$, $\sum b_n$ be related as in Definition 8.12. Assume that there exists a constant $M>0$ such that $p(n+1)-p(n)<M$ for all $n$, and assume that $\lim_{n\to\infty}a_n=0$. Then $\sum a_n$ converges if and only if $\sum b_n$ converges and they have the same sum.*

### Alternating series

#### Definition 8.15

*If $a_n>0$ for each $n$, the series $\sum_{n=1}^{\infty}(-1)^{n+1}a_n$ is called an alternating series.*

#### Theorem 8.16

*If $\{a_n\}$ is a decreasing sequence converging to $0$, the alternating series $\sum(-1)^{n+1}a_n$ converges. If $s$ denote its sum and $s_n$ its $n$th partial sum, we have the inequality*
$$
0<(-1)^n(s-s_n)<a_{n+1},\quad n=1,2,\dots
$$

### Absolute and conditional convergence

#### Definition 8.17

*A series $\sum a_n$ is called absolutely convergent if $\sum |a_n|$ converges. It is called conditionally convergent if $\sum a_n$ converges but $\sum |a_n|$ diverges.*  

#### Theorem 8.18

*Absolute convergence of $\sum a_n$ implies convergence.* 

#### Theorem 8.19

*Let $\sum a_n$ be a given series with real-valued terms and define*
$$
p_n=\frac{|a_n|+a_n}{2},\quad q_n=\frac{|a_n|-a_n}{2},\quad (n=1,2,\dots)
$$
*Then*

*i) If $\sum a_n$ is conditionally convergent, both $\sum p_n$ and $\sum q_n$ diverge.*

*ii) If $\sum |a_n|$ converges, both $\sum p_n$ and $\sum q_n$ converge and we have $\sum_{n=1}^{\infty}a_n=\sum_{n=1}^{\infty}p_n-\sum_{n=1}^{\infty}q_n$.*

### Tests for convergence of series with positive terms

#### Theorem 8.20 (Comparision test)

*If $a_n>0$ and $b_n>0$ for $n=1,2,\dots$, and if there exist positive constants $c$ and $N$ such that $a_n<cb_n$ for $n\ge N$, then convergence of $\sum b_n$ implies convergence of $\sum a_n$.*

#### Theorem 8.21 (Limit comparison test)

*Assume that $a_n>0$ and $b_n>0$ for $n=1,2,\dots$, and suppose that $\lim_{n\to\infty}\dfrac{a_n}{b_n}=1$. Then $\sum a_n$ converges if and only if $\sum b_n$ converges.*

#### Theorem 8.22

*If $|x|<1$, the series $1+x+x^2+\cdots$ converges and has sum $1/(1-x)$. If $|x|\ge1$, the series diverges.*

### Integral test

#### Theorem 8.23 (Integral test)

*Let $f$ be a positive decreasing function defined on $[1,+\infty)$ such that $\lim_{x\to+\infty}f(x)=0$. For $n=1,2,\dots$, define*
$$
s_n=\sum_{k=1}^nf(k),\quad t_n=\int_1^nf(x)dx,\quad d_n=s_n-t_n
$$
*Then we have:*

*i) $0<f(n+1)\le d_{n+1}\le d_n\le f(1)$, for $n=1,2,\dots$.*

*ii) $\lim_{n\to\infty}d_n$ exists.*

*iii) $\sum_{n=1}^{\infty}f(n)$ converges if, and only if, the sequence $\{t_n\}$ converges.*

*iv) $0\le d_k-\lim_{n\to\infty}d_n\le f(k)$ for $k=1,2,\dots$.*

### Ration test and Root test

#### Definition 8.24

*Given two sequence $\{a_n\}$ and $\{b_n\}$ such that $b_n\ge0$ for all $n$. We write $a_n=O(b_n)$ if there exists a constant $M>0$ such that $|a_n|\le Mb_n$ for all $n$. We write $a_n=o(b_n)$ as $n\to\infty$ if $\lim_{n\to\infty}a_n/b_n=0$.*

#### Theorem 8.25 (Ratio test)

*Given a series $\sum a_n$ of nonzero complex terms, let*
$$
r=\liminf_{n\to\infty}\left|\frac{a_{n+1}}{a_n}\right|,\quad R=\limsup_{n\to\infty}\left|\frac{a_{n+1}}{a_n}\right|.
$$
*a) The series $\sum a_n$ converges absolutely if $R<1$.*

*b) The series $\sum a_n$ diverges if $r>1$.*

*c) The test is inconclusive if $r\le1\le R$.*

#### Theorem 8.26 (Root test)

*Given a series $\sum a_n$ of complex terms, let*
$$
\rho=\limsup_{n\to\infty}\sqrt[n]{a_n}
$$
*a) The series $\sum a_n$ converges absolutely if $\rho<1$.*

*b) The series $\sum a_n$ diverges if $\rho>1$.*

*c) The test is inconclusive if $\rho=1$.*

### Dirichlet's test and abel's test

#### Theorem 8.27

*If $\{a_n\}$ and $\{b_n\}$ are two sequences of complex numbers, define $A_n=a_1+\cdots+a_n$. Then we have the identity*
$$
\sum_{k=1}^na_kb_k=A_nb_{n+1}-\sum_{k=1}^nA_k(b_{k+1}-b_k).\tag{9}
$$
*Therefore, $\sum_{k=1}^{\infty}a_kb_k$ converges if both the series $\sum_{k=1}^{\infty}A_k(b_{k+1}-b_k)$ and the sequence $\{A_nb_{n+1}\}$ converge.*

NOTE: (9) is called the *partial summation formula* of Abel.

#### Theorem 8.28 (Dirichlet's test)

*Let $\sum a_n$ be a series of complex terms whose partial sums form a bounded sequence. Let $\{b_n\}$ be a decreasing sequence which converges to $0$. Then $\sum a_nb_n$ converges.*

#### Theorem 8.29 (Abel's test)

*The series $\sum a_nb_n$ converges if $\sum a_n$ converges and if $\{b_n\}$ is a monotonic convergent sequence.*



作为使用Dirichlet's test的一个场景，考虑几何级数$\sum z^n$，其中$|z|=1$，这个级数发散但部分和是有界的。

#### Theorem 8.30

*For every real $x\ne2m\pi$ ($m$ is an integer), we have*
$$
\sum_{k=1}^ne^{ikx}=e^{ix}\frac{1-e^{inx}}{1-e^{ix}}=\frac{\sin(nx/2)}{\sin(x/2)}e^{i(n+1)x/2}
$$

### Rearrangements of series

#### Definition 8.31

*Let $f$ be a function whose domain is $\mathbf{Z}^+$ and whose range is $\mathbf{Z}^+$, and assume that $f$ is one-to-one on $\mathbf{Z}^+$. Let $\sum a_n$ and $\sum b_n$ be two series such that $b_n=a_{f(n)}$ for $n=1,2,\dots$. Then $\sum b_n$ is said to be a rearrangement of $\sum a_n$.*

#### Theorem 8.32

*Let $\sum a_n$ be an absolutely convergent series having sum $s$. Then every rearrangement of $\sum a_n$ also converges absolutely and has sum $s$.*

定理8.32的要求是绝对收敛，Riemann证明一个条件收敛级数可以重排为一个收敛至任意值的级数。也就是下面的定理8.33

#### Theorem 8.33

*Let $\sum a_n$ be a conditionally convergent series with real-valued terms. Let $x$ and $y$ be given numbers in the closed interval $[-\infty,+\infty]$, with $x\le y$. Then there exists a rearrangement $\sum b_n$ of $\sum a_n$ such that*
$$
\liminf_{n\to\infty}t_n=x,\quad\limsup_{n\to\infty}t_n=y
$$
*where $t_n=b_1+\cdots+b_n$.*

### Subseries

#### Definition 8.34

*Let $f$ be a function whose domain is $\mathbf{Z}^+$ and whose range is an infinite subset of $\mathbf{Z}^+$, and assume that $f$ is one-to-one on $\mathbf{Z}^+$. Let $\sum a_n$ and $\sum b_n$ be two series such that $b_n=a_{f(n)}$ if $n\in\mathbf{Z}^+$. Then $\sum b_n$ is said to be a subseries of $\sum a_n$.*

#### Theorem 8.35

*If $\sum a_n$ converges absolutely, every subseries $\sum b_n$ also converges absolutely. Moreover, we have*
$$
\left|\sum_{n=1}^{\infty}b_n\right|\le\sum_{n=1}^{\infty}|b_n|\le\sum_{n=1}^{\infty}|a_n|.
$$

#### Theorem 8.36

*Let $\{f_1,f_2,\dots\}$ be a countable collection of functions, each defined on $\mathbf{Z}^+$, having the following properties:*

*a) Each $f_n$ is one-to-one on $\mathbf{Z}^+$.*

*b) The range $f_n(\mathbf{Z}^+)$ is a subset $Q_n$ of $\mathbf{Z}^+$.*

*c) $\{Q_1,Q_2,\dots\}$ is a collection of disjoint sets whose union is $\mathbf{Z}^+$.*

*Let $\sum a_n$ be an absolutely convergent series and define*
$$
b_k(n)=a_{f_k(n)},\quad\text{if }n\in\mathbf{Z}^+,k\in\mathbf{Z}^+.
$$
*Then:*

*i) For each $k$, $\sum_{n=1}^{\infty}b_k(n)$ is an absolutely convergent subseries of $\sum a_n$.*

*ii) If $s_k=\sum_{n=1}^{\infty}b_k(n)$, the series $\sum_{k=1}^{\infty}s_k$ converges absolutely and has the same sum as $\sum_{k=1}^{\infty}a_k$.*


## Double sequences and double series

### Double sequences

#### Definition 8.37

A function $f$ whose domain is $\mathbf{Z}^+\times\mathbf{Z}^+$ is called a double sequence.  

#### Definition 8.38

If $a\in\mathbf{C}$, we write $\lim_{p,q\to\infty}f(p,q)=a$ and we say that the double sequence $f$ converges to $a$, provided that the following conditions is satisfied: For every $\varepsilon>0$, there exists an $N$ such that $|f(p,q)-a|<\varepsilon$ whenever both $p>N$ and $q>N$.

#### Theorem 8.39

Assume that $\lim_{p,q\to\infty}f(p,q)=a$. For each fixed $p$, assume that the limit $\lim_{q\to\infty}f(p,q)$ exists. Then the limit $\lim_{p\to\infty}(\lim_{q\to\infty}f(p,q))$ also exists and has the value $a$. 

### Double series

#### Definition 8.40

Let $f$ be a double sequence and let $s$ be the double sequence defined by the equation
$$
s(p,q)=\sum_{m=1}^p\sum_{n=1}^qf(m,n)
$$
The pair $(f,s)$ is called a double series and is denoted by the symbol $\sum_{m,n}f(m,n)$ or, more briefly, by $\sum f(m,n)$. The double series is said to converge to the sum $a$ if
$$
\lim_{p,q\to\infty} s(p,q)=a
$$

#### Definition 8.41

Let $f$ be a double sequence and let $g$ be a one-to-one function defined on $\mathbf{Z}^+$ with range $\mathbf{Z}^+\times\mathbf{Z}^+$. Let $G$ be the sequence defined by
$$
G(n)=f[g(n)]\quad\text{if }n\in\mathbf{Z}^+
$$
Then $g$ is said to be an arrangement of the double sequence $f$ into the sequence $G$.

#### Theorem 8.42

Let $\sum f(m,n)$ be a given double series and let $g$ be an arrangement of the double sequence $f$ into a sequence $G$. Then

a) $\sum G(n)$ converges absolutely if and only if $\sum f(m,n)$ converges absolutely.

Assuming that $\sum f(m,n)$ does converge absolutely with sum $S$, we have further:

b) $\sum_{n=1}^{\infty}G(n)=S$.

c) $\sum_{n=1}^{\infty}f(m,n)$ and $\sum_{m=1}^{\infty}f(m,n)$ both converge absolutely.

d) If $A_m=\sum_{n=1}^{\infty}f(m,n)$ and $B_n=\sum_{m=1}^{\infty}f(m,n)$, both series $\sum A_m$ and $\sum B_n$ converge absolutely and both have sum $S$. That is
$$
\sum_{m=1}^{\infty}\sum_{n=1}^{\infty}f(m,n)=\sum_{n=1}^{\infty}\sum_{m=1}^{\infty}f(m,n)=S.
$$

#### Theorem 8.43

Let $f$ be a complex-valued double sequence. Assume that $\sum_{n=1}^{\infty}f(m,n)$ converges absolutely for each fixed $m$ and that $\sum_{m=1}^{\infty}\sum_{n=1}^{\infty}|f(m,n)|$ converges. Then

a) The double series $\sum_{m,n}f(m,n)$ converges absolutely.

b) The series $\sum_{m=1}^{\infty}f(m,n)$ converges abosultely for each $n$.

c) Both iterated series $\sum_{m=1}^{\infty}\sum_{n=1}^{\infty}f(m,n)$ and $\sum_{n=1}^{\infty}\sum_{m=1}^{\infty}f(m,n)$ converges absolutely and we have
$$
\sum_{m=1}^{\infty}\sum_{n=1}^{\infty}f(m,n)=\sum_{n=1}^{\infty}\sum_{m=1}^{\infty}f(m,n)=\sum_{m,n}f(m,n).
$$

#### Theorem 8.44

Let $\sum a_m$ and $\sum b_n$ be two absolutely convergent series with sums $A$ and $B$, respectively. Let $f$ be the double sequence defined by the equation
$$
f(m,n)=a_mb_n,\quad\text{if }(m,n)\in\mathbf{Z}^+\times\mathbf{Z}^+.
$$
Then $\sum_{m,n}f(m,n)$ converges absolutely and has the sum $AB$.

#### Definition 8.45

Given two series $\sum_{n=0}^{\infty}a_n$ and $\sum_{m=0}^{\infty}b_n$, define
$$
c_n=\sum_{k=0}^na_kb_{n-k},\text{if }n=0,1,2,\dots
$$
The series $\sum_{n=0}^{\infty}c_n$ is called the Cauchy product of $\sum a_n$ and $\sum b_n$.

#### Theorem 8.46 (Mertens)

Assume that $\sum_{n=0}^{\infty}a_n$ converges absolutely and has sum $A$, and suppose $\sum_{n=0}^{\infty}b_n$ converges with sum $B$. Then the Cauchy product of these two series converges and has sum $AB$.

## Cesàro summability

这一节讨论级数部分和$s_n$的算数平均数$\sigma_n$构成的序列，这个序列收敛性和原有级数收敛性的关系。

#### Definition 8.47

Let $s_n$ denote the $n$th partial sum of the series $\sum a_n$, and let $\{\sigma_n\}$ be the sequence of arithmetic means defined by
$$
\sigma_n=\dfrac{s_1+\dots+s_n}{n},\quad\text{if }n=1,2,\dots
$$
The series $\sum a_n$ is said to be Cesàro summable (or (C,1) summable) if $\{\sigma_n\}$ converges. If $\lim_{n\to\infty}\sigma_n=S$, then $S$ is called the Cesàro sum (or (C,1) sum) of $\sum a_n$, and we write
$$
\sum a_n=S\qquad(C,1).
$$

#### Theorem 8.48

If a series is convergent with sum $S$, then it is also (C,1) summable with Cesàro sum $S$.

## Infinite products

本节内容简单的讨论一下无穷乘积，其中需要利用到无穷级数已有的结论。无穷乘积的“收敛”定义有点不一样（定义8.50），收敛和发散的无穷乘积结果都可能是0。是否收敛的判断条件是Cauchy condition for products （定理8.51）

#### Definition 8.49

given a sequence $\{u_n\}$ of real or complex numbers, let
$$
p_1=u_1,\quad p_2=u_1u_2,\quad p_n=u_1u_2\cdots u_n=\prod_{k=1}^nu_k
$$
The ordered pair of sequences $(\{u_n\},\{p_n\})$ is called an infinite product (or simply, a product). The number $p_n$ is called the $n$th partial product and $u_n$ is called the $n$th factor of the product. The following symbols are used to denote the product defined above
$$
u_1u_2\cdots u_n\cdots,\quad\prod_{n=1}^{\infty}u_n.
$$

#### Definition 8.50

Given an infinite product $\prod_{n=1}^{\infty}u_n$, let $p_n=\prod_{k=1}^nu_k$.

a) If infinitely many factors $u_n$ are zero, we say the product diverges to zero.

b) If no factor $u_n$ is zero, we say the product converges if there exists a number $p\ne0$ such that $\{p_n\}$ converges to $p$. In this case, $p$ is called the value of the product and we write $p=\prod_{n=1}^{\infty}u_n$. If $\{p_n\}$ converges to zero, we say the product diverges to zero.

c) If there exists an $N$ such that $n>N$ implies $u_n\ne0$, we say $\prod_{n=1}^{\infty}u_n$ converges, provided that $\prod_{n=N+1}^{\infty}u_n$ converges as described in (b). In this case, the value of the product $\prod_{n=1}^{\infty}u_n$ is
$$
u_1u_2\cdots u_N\prod_{n=N+1}^{\infty}u_n.
$$
d) $\prod_{n=1}^{\infty}u_n$ is called divergent if it does not converge as described in (b) or (c).

#### Theorem 8.51 (Cauchy condition for products)

The infinite product $\prod u_n$ converges if and only if for every $\varepsilon>0$ there exists an $N$ such that $n>N$ implies
$$
|u_{n+1}u_{n+2}\cdots u_{n+k}-1|<\varepsilon,\quad k=1,2,3,\dots
$$

#### Theorem 8.52

Assume that each $a_n>0$. Then the product $\prod(1+a_n)$ converges if and only if the series $\sum a_n$ converges.

#### Definition 8.53

The product $\prod(1+a_n)$ is said to converge absolutely if $\prod(1+|a_n|)$ converges.

#### Theorem 8.54

Absolute convergence of $\prod(1+a_n)$ implies convergence.

#### Theorem 8.55

Assume that each $a_n\ge0$. Then the product $\prod(1-a_n)$ converges if and only if the series $\sum a_n$ converges.