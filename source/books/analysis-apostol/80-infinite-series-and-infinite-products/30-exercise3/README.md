# Exercise 28-35 (Double sequences and double series)

### 8.28

Investigate the existence of the two iterated limits and the double limit of the double sequence $f$ defined by
$$
\begin{aligned}
&a) f(p,q)=\dfrac{1}{p+q},\qquad&&b)f(p,q)=\dfrac{p}{p+q},
\\
&c)f(p,q)=\dfrac{(-1)^pp}{p+q},\qquad&&d)f(p,q)=(-1)^{p+q}\left(\frac{1}{p}+\frac{1}{q}\right),
\\
&e)f(p,q)=\dfrac{(-1)^p}{q},\qquad&&f)f(p,q)=(-1)^{p+q},
\\
&g)f(p,q)=\dfrac{\cos p}{q},\qquad&&h)f(p,q)=\frac{p}{q^2}\sum_{n=1}^q\sin\frac{n}{p}.
\end{aligned}
$$

#### Solution

Double limit exists in (a), (d), (e), (g). Both iterated limits exist in (a), (b), (h). Only one iterated limit exists in (c), (e). Neither iterated limit exists in (d), (f).  

### 8.29

Prove the following statements:

a) A double series of positive terms converges if, and only if, the set of partial sums is bounded. 

b) A double series converges if it converges absolutely.

c) $\sum_{m,n}e^{-(m^2+n^2)}$ converges.

#### Proof

(a) Let $f$ be a double sequence and let $s$ be its partial sums, then $f(m,n)>0$ for all $m,n$. Suppose $f$ converges to $a$, then $\lim_{p,q\to\infty}s(p,q)=a$, thus there is an integer $N$ such that $|s(p,q)-a|<1$ for all $p>N$ and $q>N$, which means
$$
s(p,q)<a+1,\quad\forall p>N,q>N
$$
let
$$
M=\max\left(\max_{1\le a,b\le N}s(a,b),a+1\right)\implies s(p,q)\le M,\forall p,q\in\mathbf{Z}^+
$$
thus $\{s(p,q)\}$ is bounded. 

Conversely, if we can find an $M$ such that $s(p,q)\le M$ for all $p,q\in\mathbf{Z}^+$, then the set $\{s(p,q)\}$ has an upper bound $a$, thus for any $\varepsilon>0$ there exists some $a,b$ such that $a-\varepsilon<s(a,b)\le a$, let $N=\max(a,b)$, since $f$ is positive, we have $s(N,N)\ge s(a,b)$, and $s(N,N)$ belongs to the set or partial sums, thus we have $a-\varepsilon<s(N,N)\le a$. Now for any $p>N,q>N$ we deduce that $s(p,q)>s(N,N)$ by the positivity of $f$, and $s(p,q)\le a$ by the definition of $a$. So we conclude
$$
a-\varepsilon<s(p,q)\le a\implies|s(p,q)-a|<\varepsilon,\forall p>N,q>N
$$
this means $f$ converges to $a$, by Definition 8.38.

(b) Let $(f,s)$ be a double series which converges absolutely, then $\sum|f(m,n)|$ converges, so the set of partial sums of $|f|$ is bounded. Let $(f_+,s_+)$ be the double series which consists of only positive items of $f$, and $(f_-,s_-)$ be the double series which consists of only the inverse of negative items of $f$, i.e.
$$
f_+(m,n)=\begin{cases}f(m,n),\quad&\text{if }f(m,n)>0\\0,\quad&\text{if }f(m,n)\le 0\end{cases}\qquad s_+(p,q)=\sum_{m=1}^p\sum_{n=1}^qf_+(m,n)
\\
f_-(m,n)=\begin{cases}-f(m,n),\quad&\text{if }f(m,n)<0\\0,\quad&\text{if }f(m,n)\ge 0\end{cases}\qquad s_-(p,q)=\sum_{m=1}^p\sum_{n=1}^qf_-(m,n)
$$
then $(f_+,s_+)$ and $(f_-,s_-)$ are double series of positive terms, we have $|s(p,q)|=s_+(p,q)+s_-(p,q)$ and $s(p,q)=s_+(p,q)-s_-(p,q)$ for all $p,q\in\mathbf{Z}^+$. 

Since $\{s(p,q)\}$ is bounded, both $\{s_+(p,q)\}$ and $\{s_-(p,q)\}$ are bounded, thus by (a),  $(f_+,s_+)$ and $(f_-,s_-)$ both converges, which means $\lim_{p,q\to\infty}s_+(p,q)$ and $\lim_{p,q\to\infty}s_-(p,q)$ exists, thus $\lim_{p,q\to\infty}s(p,q)$ exists, hence $(f,s)$ converges.

(c) This is a double series of positive terms, let $s(p,q)$ be its partial sums, then
$$
\begin{aligned}
s(p,q)&=\sum_{m=1}^p\sum_{n=1}^qe^{-(m^2+n^2)}=\sum_{m=1}^p\frac{1}{e^{m^2}}\sum_{n=1}^q\frac{1}{e^{n^2}}\le\sum_{m=1}^p\frac{1}{e^{m^2}}\sum_{n=1}^q\frac{1}{e^n}=\sum_{m=1}^p\frac{1}{e^{m^2}}\frac{1-e^q}{e-1}
\\&\le\sum_{m=1}^p\frac{1}{e^{m^2}}\frac{1}{e-1}\le\frac{1}{e-1}\sum_{m=1}^p\frac{1}{e^m}=\frac{1}{e-1}\frac{1-e^p}{e-1}\le\frac{1}{(e-1)^2}
\end{aligned}
$$
so $s(p,q)$ is bounded above, so the series converges by (a).

### 8.30

Assume that the double series $\sum_{m,n}a(n)x^{mn}$ converges absolutely for $|x|<1$. Call its sum $S(x)$. Show that each of the following series also converges absolutely for $|x|<1$ and has sum $S(x)$:
$$
\sum_{n=1}^{\infty}a(n)\frac{x^n}{1-x^n},\quad\sum_{n=1}^{\infty}A(n)x^n,\quad\text{where }A(n)=\sum_{d|n}a(d)
$$

#### Proof

Given $n$ fixed and $|x|<1$, we have $\sum_{m=1}^{\infty}x^{mn}=\dfrac{x^n}{1-x^n}$, thus by Theorem 8.39 we have $\sum_{n=1}^{\infty}a(n)\dfrac{x^n}{1-x^n}=\sum_{m,n}a(n)x^{mn}=S(x)$. To verify the second series, we rewrite it to be a double series
$$
\sum_{n=1}^{\infty}A(n)x^n=\sum_{n=1}^{\infty}\sum_{d|n}a(d)x^n=\sum_{n=1}^{\infty}\sum_{d\le n,d|n}a(d)x^n=:\sum_{n=1}^{\infty}\sum_{d\le n,d|n}g(d,n)
$$
for any positive integer $m,n$, the item $f(m,n):=a(n)x^{mn}$ is equal to $g(n,mn)$, also if given $g(d,n)$, we have $d|n$ and so $\exists m\in\mathbf{N}^+$ such that $n=md$, so $g(d,n)=a(d)x^{md}=f(m,d)$, thus we can establish a one-to-one correspondence between the items of the two series $\sum_{m,n}a(n)x^{mn}$ and $\sum_{n=1}^{\infty}\sum_{d\le n,d|n}a(d)x^n$, which means they are equal.

### 8.31

If $\alpha$ is real, show that the double series $\sum_{m,n}(m+in)^{-\alpha}$ converges absolutely if and only if $\alpha>2$.

#### Proof

If $\alpha>2$, we have
$$
\sum_{m,n}\left|\frac{1}{(m+in)^{\alpha}}\right|\le\sum_{m,n}\frac{1}{|m+in|^2}\le\sum_m\frac{1}{m^2}
$$
thus the double series converges absolutely. Conversely, suppose the double series converges absolutely, let
$$
s(p,q)=\sum_{m=1}^p\sum_{n=1}^q|m+in|^{-\alpha}
$$
then $\lim_{p,q\to\infty}s(p,q)$ exists. Notice that the set
$$
m+in:m=1,2,\dots,p,n=1,2,\dots,p
$$
consists of $p^2$ complex numbers with the following properties:
$$
m=1,n=1:|1+i|=\sqrt{2}
\\
(m,n)\in\{(1,2),(2,1),(2,2)\}:|m+in|\le2\sqrt{2}
\\
(m,n)\in\{(1,3),(2,3),(3,1),(3,2),(3,3)\}:|m+in|\le3\sqrt{2}
\\{\vdots}
$$
thus
$$
s(p,p)=\sum_{m=1}^p\sum_{n=1}^p\dfrac{1}{|m+in|^{\alpha}}\ge\sum_{n=1}^p\dfrac{2n-1}{(n\sqrt{2})^{\alpha}}=2^{-\alpha/2}\sum_{n=1}^p\dfrac{2n-1}{n^{\alpha}}
$$
this means the series $\sum_{n=1}^{\infty}(2n-1)/n^{\alpha}$ converges, then $\lim_{n\to\infty}(2n-1)/n^{\alpha}=0$, thus $\alpha>1$, this means the series $\sum_{n=1}^{\infty}1/n^{\alpha}$ converges, thus the series
$$
\sum_{n=1}^{\infty}\dfrac{2}{n^{\alpha-1}}=\sum_{n=1}^{\infty}\dfrac{2n-1}{n^{\alpha}}+\sum_{n=1}^{\infty}\dfrac{1}{n^{\alpha}}
$$
converges, then $\alpha-1>1$ and $\alpha>2$.

### 8.32

a) Show that the Cauchy product of $\sum_{n=0}^{\infty}(-1)^{n+1}/\sqrt{n+1}$ with itself is a divergent series.

b) Show that the Cauchy product of $\sum_{n=0}^{\infty}(-1)^{n+1}/(n+1)$ with itself is the series
$$
2\sum_{n=1}^{\infty}\frac{(-1)^{n+1}}{n+1}\left(1+\frac{1}{2}+\cdots+\frac{1}{n}\right).
$$
Does this converge? Why?

#### Solution

(a) The Cauchy product is $\sum_{n=0}^{\infty}c_n$ with 
$$
c_n=\sum_{k=0}^n\dfrac{(-1)^{k+1}}{\sqrt{k+1}}\dfrac{(-1)^{n-k+1}}{\sqrt{n-k+1}}=\sum_{k=0}^n\dfrac{(-1)^{n+2}}{\sqrt{(k+1)(n-k+1)}}
$$
thus
$$
|c_n|=\sum_{k=0}^n\dfrac{1}{\sqrt{k+1}\sqrt{n-k+1}}\ge\sum_{k=0}^n\dfrac{2}{k+1+n-k+1}=\dfrac{2(n+1)}{n+2}
$$
so $\lim_{n\to\infty}c_n\ne0$, thus $\sum_{n=0}^{\infty}c_n$ diverges.

(b) The Cauchy product is $\sum_{n=0}^{\infty}c_n$ with
$$
\begin{aligned}
c_n&=\sum_{k=0}^n\dfrac{(-1)^{k+1}}{k+1}\dfrac{(-1)^{n-k+1}}{n-k+1}=\sum_{k=0}^n\dfrac{(-1)^{n+2}}{(k+1)(n-k+1)}\\&=\dfrac{(-1)^n}{n+2}\sum_{k=0}^n\left(\dfrac{1}{k+1}+\dfrac{1}{n-k+1}\right)
\\&=\dfrac{2(-1)^n}{n+2}\left(1+\dfrac{1}{2}+\cdots+\dfrac{1}{n+1}\right)
\end{aligned}
$$
thus
$$
\sum_{n=0}^{\infty}c_n=\sum_{n=0}^{\infty}\dfrac{2(-1)^n}{n+2}\left(1+\dfrac{1}{2}+\cdots+\dfrac{1}{n+1}\right)=\sum_{n=1}^{\infty}\dfrac{2(-1)^{n+1}}{n+1}\left(1+\dfrac{1}{2}+\cdots+\dfrac{1}{n}\right)
$$
This is an alternating series. Write $\sum_{n=0}^{\infty}c_n=\sum_{n=0}^{\infty}2(-1)^na_n$, then
$$
\begin{aligned}
a_{n+1}-a_n&=\dfrac{1}{n+2}\left(1+\dfrac{1}{2}+\cdots+\dfrac{1}{n+1}\right)-\dfrac{1}{n+1}\left(1+\dfrac{1}{2}+\cdots+\dfrac{1}{n}\right)
\\&=\dfrac{1}{(n+1)(n+2)}-\left(\dfrac{1}{n+1}-\dfrac{1}{n+2}\right)\left(1+\dfrac{1}{2}+\cdots+\dfrac{1}{n}\right)
\\&=\dfrac{1}{(n+1)(n+2)}-\dfrac{1}{(n+1)(n+2)}\left(1+\dfrac{1}{2}+\cdots+\dfrac{1}{n}\right)
\\&=-\dfrac{1}{(n+1)(n+2)}\left(\dfrac{1}{2}+\cdots+\dfrac{1}{n}\right)<0
\end{aligned}
$$
thus $0<a_{n+1}<a_n$, for any $n\in\mathbf{N}$, there is an integer $k$ such that $n+1\le2^k<2n$, then
$$
\begin{aligned}
0<a_n&=\dfrac{1}{n+1}\left(1+\dfrac{1}{2}+\cdots+\dfrac{1}{n}\right)\le\dfrac{1}{n+1}\left(1+\dfrac{1}{2}+\dfrac{1}{3}\cdots+\dfrac{1}{2^k-1}\right)
\\&<\dfrac{1}{n+1}\left(1+\underbrace{\dfrac{1}{2}+\dfrac{1}{2}}_{2^1}+\cdots+\underbrace{\dfrac{1}{2^{k-1}}+\cdots+\dfrac{1}{2^{k-1}}}_{2^{k-1}}\right)=\dfrac{k}{n+1}<\dfrac{\log_2(2n)}{n+1}
\end{aligned}
$$
use the L'Hospital rule we can easily see that
$$
\lim_{n\to\infty}\dfrac{\log_2(2n)}{n+1}=\lim_{n\to\infty}\dfrac{2}{2n\ln2}=0
$$
thus $a_n\to0$, use Theorem 8.16, this series is convergent.

### 8.33

Given two absolutely convergent power series, say $\sum_{n=0}^{\infty}a_nx^n$ and $\sum_{n=0}^{\infty}b_nx^n$, having sums $A(x)$ and $B(x)$, respectively, show that $\sum_{n=0}^{\infty}c_nx^n=A(x)B(x)$ where $c_n=\sum_{k=0}^na_kb_{n-k}$.

#### Proof

It is easy to see that $\sum_{n=0}^{\infty}c_nx^n$ is the Cauchy product of $\sum_{n=0}^{\infty}a_nx^n$ and $\sum_{n=0}^{\infty}b_nx^n$, then use Theorem 8.46 (Mertens).

### 8.34

A series of the form $\sum_{n=1}^{\infty}a_n/n^s$ is called a *Dirichlet series*. Given two absolutely convergent Dirichlet series, say $\sum_{n=1}^{\infty}a_n/n^s$ and $\sum_{n=1}^{\infty}b_n/n^s$, having sums $A(s)$ and $B(s)$, respectively, show that $\sum_{n=1}^{\infty}c_n/n^s=A(s)B(s)$ where $c_n=\sum_{d|n}a_db_{n/d}$.

#### Proof

It is easy to see that
$$
\dfrac{c_n}{n^s}=\sum_{d|n}\dfrac{a_d}{d^s}\dfrac{b_{n/d}}{(n/d)^s}\implies\left(\sum_{n=1}^{\infty}\dfrac{a_n}{n^s}\right)\left(\sum_{n=1}^{\infty}\dfrac{b_n}{n^s}\right)=\sum_{n=1}^{\infty}\dfrac{c_n}{n^s}
$$
Then use Theorem 8.44.

### 8.35

If $\zeta(s)=\sum_{n=1}^{\infty}1/n^s,s>1$, show that $\zeta^2(s)=\sum_{n=1}^{\infty}d(n)/n^s$, where $d(n)$ is the number of positive divisors of $n$ (including $1$ and $n$).

#### Proof

Use Exercise 8.34, let $a_n=b_n=1$ for all $n$, we have $d(n)=\sum_{d|n}1$, which is the number of positive divisors of $n$ (including $1$ and $n$).