# Exercise 1-6 (Integers)

### 1.1

Prove that there is no largest prime.

#### Solution

Assume there is the largest prime $k$, then there are finite primes $p_1,\dots,p_n$ with $p_n=k$. Consider
$$
N=p_1p_2\cdots p_n+1
$$
this $N$ is a composite, by our assumption, thus can be written in the form
$$
N=q_1\cdots q_m
$$
with all $q_i$ being primes, in particular, this means there exists a prime $p=q_i$ for some $i$ such that $p|N$. Now $p$ must be one of $p_j$ for some positive interger $j\leq n$. And thus $p_j|N$, but $p_j|p_1p_2\cdots p_n$, we get $p_j|1$, a contradiction.

### 1.2

If $n$ is a positive integer, prove the algebraic identity
$$
a^n-b^n=(a-b)\sum_{k=0}^{n-1}a^kb^{n-1-k}.
$$

#### Solution

Use induction, the identity is true when $n=1$. Suppose it is true for $n=m$, consider the case $m+1$:
$$
\begin{aligned}
    a^{m+1}-b^{m+1}&=a^{m+1}-ab^m+ab^m-b^{m+1}
    \\&=a(a^m-b^m)+b^m(a-b)
    \\&=a(a-b)\sum_{k=0}^{m-1}a^kb^{m-1-k}+(a-b)b^m
    \\&=(a-b)\left(\sum_{k=0}^{m-1}a^{k+1}b^{m-1-k}+b^m\right)
    \\&=(a-b)\sum_{k=0}^{m}a^kb^{m-k}
\end{aligned}
$$
which shows the induction hypothesis is true.

### 1.3

If $2^n-1$ is a prime, prove that $n$ is a prime. A prime of the form $2^p-1$, where $p$ is prime, is called a *Mersenne prime*.

#### Solution

Assume $n$ is not a prime, then $n=1$ or $n$ is a composite. If $n=1$ then $2^n-1=1$, a contradiction. If $n$ is a composite, then $\exists p,q>1$ s.t. $n=pq$, use Exercise 1.2 we have
$$
2^n-1=2^{pq}-1=(2^q-1)\sum_{k=0}^{p-1}(2^q)^{p-k-1}
$$
this means $(2^q-1)|(2^n-1)$, but $2^q-1>1$, this contradicts the fact that $2^n-1$ is a prime.

### 1.4

If $2^n+1$ is prime, prove that $n$ is a power of $2$. A prime of the form $2^{2^m}+1$ is called a *Fermat prime*.

#### Solution

Apparently $2^n+1\geq 3$ if $n>0$. If $2^n+1=3$, then $n=1=2^0$, now assume $n>1$ and is not a power of $2$, by Unique factorization theorem, $n$ can be represented as a product of prime factors, not a power of $2$ means at least one prime factor shall be odd, let it be $q$ and write $n=pq$, we have $p\geq 1,q>1$, then
$$
\begin{aligned}
    2^n+1&=2^{pq}+1=(2^p+1-1)^q+1
    \\&=1+\sum_{i=0}^{q}\begin{pmatrix}i\\q\end{pmatrix}(2^p+1)^i(-1)^{q-i}
    \\&=1+(-1)^q+\sum_{i=1}^{q}\begin{pmatrix}i\\q\end{pmatrix}(2^p+1)^i(-1)^{q-i}
    \\&=\sum_{i=1}^{q}\begin{pmatrix}i\\q\end{pmatrix}(2^p+1)^i(-1)^{q-i}
\end{aligned}
$$
this shows that $(2^p+1)|(2^n+1)$, and from $2^p+1>1$ we see $2^n+1$ is not a prime, a contradiction.

### 1.5

The *Fibonacci numbers* $1,1,2,3,5,8,13,\dots$ are defined by the recursion formula $x_{n+1}=x_n+x_{n-1}$, with $x_1=x_2=1$. Prove that $(x_n,x_{n+1})=1$ and that $x_n=(a^n-b^n)/(a-b)$, where $a$ and $b$ are the roots of the quadratic equation $x^2-x-1=0$.

#### Solution

I prove by induction. For $n=1$, there is $(x_1,x_2)=(1,1)=1$, and $(a-b)/(a-b)=1=x_1$, for $n=2$, there is $(x_2,x_3)=(1,2)=1$ and $(a^2-b^2)/(a-b)=(a+1-b-1)/(a-b)=1=x_2$.
Now suppose the conclusion holds for $n=k-1>2$, consider the case $n=k$.
To prove $(x_k,x_{k+1})=1$, assume $(x_k,x_{k+1})=d>1$, then $d|x_k$ and $d|(x_k+x_{k-1})$, which means $d|(x_k+x_{k-1}-x_k)$, or $d|x_{k-1}$, but this means $(x_k,x_{k-1})\geq d>1$, a contradiction to $(x_k,x_{k-1})=1$.
To prove $x_k=(a^k-b^k)/(a-b)$, there is
$$
\begin{aligned}
x_k&=x_{k-1}+x_{k-2}=\dfrac{a^{k-1}-b^{k-1}+a^{k-2}-b^{k-2}}{a-b}
\\&=\dfrac{a^{k-2}(a+1)-b^{k-2}(b+1)}{a-b}
\\&=\dfrac{a^{k-2}a^2-b^{k-2}b^2}{a-b}=\dfrac{a^k-b^k}{a-b}
\end{aligned}
$$

### 1.6

Prove that every nonempty set of positive integers contains a smallest member. This is called the *well-ordering principle*.

#### Solution

Let $S$ be a nonempty set of positive integers, then we can choose a positive integer $n\in S$. Since $n>0$, consider the finite set $\{1,2,\dots,n\}$, each element of this set either belongs to $S$ or not. We start from the number $1$ and goes forward, the first element that belongs to $S$ is the smallest member of $S$.

