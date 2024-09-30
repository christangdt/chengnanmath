# Exercise 7-17 (Rational and irrational numbers)

### 1.7

Find the rational number whose decimal expansion is $0.3344444...$

#### Solution

Write $0.3344444...=0.33333...+0.00111....$, then we have
$$
0.3344444...=\dfrac{1}{3}+\dfrac{1}{900}=\dfrac{301}{900}
$$

### 1.8

Prove that the decimal expansion of $x$ will end in zeros (or in nines) if, and only if, $x$ is a rational number whose denominator is of the form $2^n5^m$, where $m$ and $n$ are non-negative integers.

#### Solution

One direction is obvious, to prove the other direction, notice that the unique factorization of the decimal base $10$ is $2\cdot 5$, thus other factor in the denominator would yield a nonzero end, since if $x$ ends in zero, then we shall find a integer $n$ such that $10^nx$ is an integer, but factors other than $2$ and $5$ will make it impossible.

### 1.9

Prove that $\sqrt{2}+\sqrt{3}$ is irrational.

#### Solution

Assume $\sqrt{2}+\sqrt{3}=m/n$, then $\sqrt{3}=m/n-\sqrt{2}$ and thus
$$
3=m^2/n^2-2m/n\sqrt{2}+2\Rightarrow\sqrt{2}=\dfrac{n}{2m}(m^2/n^2-1)\in\mathbf{Q}
$$
but $\sqrt{2}$ is irrational, we can prove this by:
assume $\sqrt{2}=p/q, (p,q)=1$, then $p^2=2q^2$, which means $p$ is even, thus $p=2k$ and $4k^2=2q^2$, which shows $2k^2=q^2$ and $q$ is even, which contradicts $(p,q)=1$.

### 1.10

If $a,b,c,d$ are rational and if $x$ is irrational, prove that $(ax+b)/(cx+d)$ is usually irrational. When do expcetions occur?

#### Solution

If $(ax+b)/(cx+d)$ is rational, we can assume
$$
\dfrac{ax+b}{cx+d}=\dfrac{m}{n},\quad n\neq 0
$$
which means $nax+nb=mcx+md$, or $(mc-na)x=nb-md$, thus $x$ is rational when $mc\neq na$ and $nb\neq md$, this is a contradiction.
Exceptions occur when $mc=na,nb=md$, that is when $a=c=0,d\neq 0$, or when $b=d=0,c\neq 0$, or when $a/c=b/d,c\neq 0,d\neq 0$.

### 1.11

Given any real $x>0$, prove that there is an irrational number between $0$ and $x$.

#### Solution

If $x$ is rational, then choose $x/\sqrt{2}$, if $x$ is irrational, choose $x/2$.

### 1.12

If $a/b<c/d$ with $b>0,d>0$, prove that $(a+c)/(b+d)$ lies between $a/b$ and $c/d$.

#### Solution

It is easy to get
$$
\dfrac{a+c}{b+d}-\dfrac{a}{b}=\dfrac{bc-ad}{(b+d)b}
\\
\dfrac{a+c}{b+d}-\dfrac{c}{d}=\dfrac{ad-bc}{(b+d)b}
$$
the sign of $bc-ad$ and $ad-bc$ are different (except $bc=ad$), thus $(a+c)/(b+d)$ lies between $a/b$ and $c/d$. If $bc=ad$, then we have $(a+c)/(b+d)=a/b=c/d$, the conclusion still holds.

### 1.13

Let $a$ and $b$ be positive integers. Prove that $\sqrt{2}$ always lies between the two fractions $a/b$ and $(a+2b)/(a+b)$. Which fraction is closer to $\sqrt{2}$?

#### Solution

First we have
$$
\sqrt{2}-\dfrac{a}{b}=\dfrac{\sqrt{2}b-a}{b}=\dfrac{(\sqrt{2}b-a)(a+b)}{b(a+b)}
$$
and then
$$
\sqrt{2}-\dfrac{a+2b}{a+b}=\dfrac{(a-\sqrt{2}b)(\sqrt{2}-1)}{a+b}=\dfrac{(a-\sqrt{2}b)(\sqrt{2}-1)b}{(a+b)b}
$$
if $\sqrt{2}\geq a/b$, then $a\leq\sqrt{2}b$, the second expression is no greater than zero, and vise versa, thus the lie between part is true.
We further denote
$$
d_1=\left|\sqrt{2}-\dfrac{a}{b}\right|,d_2=\left|\sqrt{2}-\dfrac{a+2b}{a+b}\right|
$$
then if $a<\sqrt{2}b$, there is
$$
d_1=\dfrac{(\sqrt{2}b-a)(a+b)}{b(a+b)},d_2=\dfrac{(\sqrt{2}b-a)(\sqrt{2}-1)b}{(a+b)b}
$$
since $a+b>b>(\sqrt{2}-1)b$, we have $d_1>d_2$, the second expression is closer.
If $a>\sqrt{2}b$, the second expression is closer, with a similar proof.
If $a=\sqrt{2}b$, we have $d_1=d_2$.
In conclusion, the second expression is closer to $\sqrt{2}$.

### 1.14

Prove that $\sqrt{n-1}+\sqrt{n+1}$ is irrational for every integer $n\geq 1$.

#### Solution

Assume $\sqrt{n-1}+\sqrt{n+1}\in\mathbf{Q}$, then since
$$
\sqrt{n-1}+\sqrt{n+1}=\dfrac{2}{\sqrt{n+1}-\sqrt{n-1}}\in\mathbf{Q}
$$
we have $\sqrt{n+1}-\sqrt{n-1}\in\mathbf{Q}$, further we can have both $\sqrt{n+1}\in\mathbf{Q}$ and $\sqrt{n-1}\in\mathbf{Q}$, but if $n$ is a positive integer, then $n+1$ and $n-1$ cannot be perfect squares at the same time, use Theorem 1.10, at least one of $n+1$ and $n-1$ is irrational, a contradiction.

### 1.15

Given a real $x$ and an integer $N>1$, prove that there exists integers $h$ and $k$ with $0<k\leq N$ such that $|kx-h|<1/N$.

#### Solution

The $N+1$ numbers $tx-[tx],t=0,1,\dots,N$ all lies in $[0,1)$, thus at least two has distance less than $1/N$, let us say that integers $i,j$ with $i>j$ makes
$$
|ix-[ix]-(jx-[jx])|=|(i-j)x+[jx]-[ix]|<1/N
$$
Let $k=i-j$ and $h=[ix]-[jx]$. That $0<k\leq N$ follows from $i>j$ and $i\leq N$.

### 1.16

If $x$ is irrational prove that there are infinitely many rational numbers $h/k$ with $k>0$ such that $|x-h/k|<1/k^2$.

#### Solution

Use Exercises 1.15 we have, for an integer $N>1$, there exists integers $h$ and $k$ with $0<k\leq N$ such that $|kx-h|<1/N$, which means
$$
\left|x-\dfrac{h}{k}\right|<\dfrac{1}{kN}\leq\dfrac{1}{k^2}
$$
This is true for all $N>1$, thus we can find infinitely many $h/k$.

### 1.17

Let $x$ be a positive rational number of the form
$$
x=\sum_{k=1}^n\dfrac{a_k}{k!},
$$
where each $a_k$ is a nonnegative integer with $a_k\leq k-1$ for $k\geq 2$ and $a_n>0$. Let $[x]$ denote the greatest integer in $x$. Prove that $a_1=[x]$, that $a_k=[k!x]-k[(k-1)!x]$ for $k=2,\dots,n$, and that $n$ is the smallest integer such that $n!x$ is an integer. Conversely, show that every positive rational number $x$ can be expressed in this form in one and only one way.

#### Solution

Write
$$
x=a_1+\sum_{k=2}^n\dfrac{a_k}{k!}
$$
to prove $a_1=[x]$, notice that
$$
\sum_{k=2}^n\dfrac{a_k}{k!}\leq \sum_{k=2}^n\dfrac{k-1}{k!}=\sum_{k=2}^n\left(\dfrac{1}{(k-1)!}-\dfrac{1}{k!}\right)=1-\dfrac{1}{n!}<1
$$
we get $[x]=a_1$. To calculate $a_k$, we have
$$
k!x=k!\sum_{j=1}^n\dfrac{a_j}{j!}=\left(\sum_{j=1}^k\dfrac{k!}{j!}a_j\right)+\left(\sum_{j=k+1}^n\dfrac{k!}{j!}a_j\right)
$$
and
$$
(k-1)!x=(k-1)!\sum_{j=1}^n\dfrac{a_j}{j!}=\left(\sum_{j=1}^{k-1}\dfrac{(k-1)!}{j!}a_j\right)+\left(\sum_{j=k}^n\dfrac{(k-1)!}{j!}a_j\right)
$$
Now since
$$
\sum_{j=k+1}^n\dfrac{k!}{j!}a_j=k!\sum_{j=k+1}^n\dfrac{a_j}{j!}\leq k!\sum_{j=k+1}^n\left(\dfrac{1}{(j-1)!}+\dfrac{1}{j!}\right)=k!\left(\dfrac{1}{k!}-\dfrac{1}{n!}\right)<1
$$
we see that 
$$[k!x]=\sum_{j=1}^k\dfrac{k!}{j!}a_j$$
similarly 
$$[(k-1)!x]=\sum_{j=1}^{k-1}\dfrac{(k-1)!}{j!}a_j$$
thus
$$
[k!x]-k[(k-1)!x]=\sum_{j=1}^k\dfrac{k!}{j!}a_j-\sum_{j=1}^{k-1}\dfrac{(k)!}{j!}a_j=\dfrac{k!}{k!}a_k=a_k
$$
To prove $n$ is the smallest integer such that $n!x$ is an integer, we see that for any integer $k\leq n$:
$$
k!x=k!\sum_{j=1}^n\dfrac{a_j}{j!}=\left(\sum_{j=1}^k\dfrac{k!}{j!}a_j\right)+\left(\sum_{j=k+1}^n\dfrac{k!}{j!}a_j\right)
$$
the first bracket is an integer, the second bracket is between $0$ and $1$, the second bracket vanishes only when $k=n$.
Conversely, if given a positive $x\in\mathbf{Q}$, choose $n$ being the smallest integer such that $n!x$ is an integer, we let $a_1=[x]$ and $a_k=[k!x]-k[(k-1)!x]$ for $k=2,\dots,n$, then $a_1,\dots,a_n$ is decided uniquely. We only need to show $x=\sum_{k=1}^n{a_k}/{k!}$. This is clear since
$$
\begin{aligned}
\sum_{k=1}^n\dfrac{a_k}{k!}&=[x]+\sum_{k=2}^n\dfrac{[k!x]-k[(k-1)!x]}{k!}\\&=[x]+\sum_{k=2}^n\left(\dfrac{[k!x]}{k!}-\dfrac{[(k-1)!x]}{(k-1)!}\right)
\\&=[x]+\dfrac{[n!x]}{n!}-[x]=\dfrac{[n!x]}{n!}=\dfrac{n!x}{n!}
\\&=x
\end{aligned}
$$
and the proof is complete.