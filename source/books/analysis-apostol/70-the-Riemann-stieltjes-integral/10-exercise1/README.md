# Exercise 1-17 (Riemann-Stieltjes integrals)

### 7.1

Prove that $\int_a^bd\alpha(x)=\alpha(b)-\alpha(a)$ directly from Definition 7.1.

#### Proof

This is a special case of integrals for the constant function $f=1$, thus for a partition $P=\{x_0,x_1,\dots,x_n\}$ of $[a,b]$, we consider the Riemann-Stieltjes sum
$$
S(P,1,\alpha)=\sum_{k=1}^n\Delta\alpha_k=\alpha(b)-\alpha(a)
$$
which shows that $S(P,1,\alpha)$ equals $\alpha(b)-\alpha(a)$ regardless of which partition to choose.

### 7.2

If $f\in R$ on $[a,b]$ and if $\int_a^bfd\alpha=0$ for every $f$ which is monotonic on $[a,b]$, prove that $\alpha$ must be constant on $[a,b]$.

#### Proof

Let $f=1$ on $[a,b]$, we get $\alpha(b)-\alpha(a)=0$ from Exercise 7.1. Assume $\alpha$ is not constant on $[a,b]$, then there exist $c\in(a,b)$ such that $\alpha(c)\ne\alpha(b)$. Let $f$ be defined as
$$
f(x)=\begin{cases}0,\quad& x\in[a,c)\\1,\quad& x\in[c,b]\end{cases}
$$
then $f$ is monotonic on $[a,b]$, and
$$
0=\int_a^bfd\alpha=\int_a^cfd\alpha+\int_c^bfd\alpha=\int_c^bd\alpha=\alpha(b)-\alpha(c)\ne0
$$
which is a contradiction.

### 7.3

The following definition of a Riemann-Stieltjes integral is often used in the literature:

We say $f$ is integrable with respect to $\alpha$ if there exists a real number $A$ having the property that for every $\varepsilon>0$ there exists a $\delta>0$ such that for every partition $P$ of $[a,b]$ with norm $\|P\|<\delta$ and for every choice of $t_k$ in $[x_{k-1},x_k]$, we have $|S(P,f,\alpha)-A|<\varepsilon$.

a) Show that if $\int_a^bfd\alpha$ exists according to this definition, then it also exists according to Definition 7.1 and the two integrals are equal.

b) Let $f(x)=\alpha(x)=0$ for $a\le x<c$, $f(x)=\alpha(x)=1$ for $c<x\le b$, $f(c)=0,\alpha(c)=1$. Show that $\int_a^bfd\alpha$ exists according to Definition 7.1 but does not exist by this second definition.

#### Solution

(a) For $\forall\varepsilon>0$, we can get a $\delta>0$ which satisfy the condition in this definition. Choose a partition $P_{\varepsilon}$ of $[a,b]$ with norm $\|P_{\varepsilon}\|<\delta$. If $P$ is any partition finer than $P_{\varepsilon}$, we have $\|P\|\le\|P_{\varepsilon}\|<\delta$, thus for every choice of  $t_k$ in $[x_{k-1},x_k]$, we have $|S(P,f,\alpha)-A|<\varepsilon$. This shows $\int_a^bfd\alpha$ exists according to Definition 7.1. Both integrals equal to $A$.

(b)  For $\forall\varepsilon>0$, , let $P_{\varepsilon}=\{a,c,b\}$, then choose any $t_1\in[a,c]$ and $t_2\in[c,b]$, we have
$$
S(P_{\varepsilon},f,\alpha)=f(t_1)(\alpha(c)-\alpha(a))+f(t_2)(\alpha(b)-\alpha(c))=0(1)+f(t_2)0=0
$$
If $P$ is any partition of $[a,b]$ finer than $P_{\varepsilon}$, then $P=\{a=x_0,x_1,\dots,x_n=b\}$ and there exist some integer $m\in[1,n-1]$ such that $x_m=c$, thus $f(t_k)=0$ when $k\le m$ and $\Delta\alpha_k=0$ when $k>m$, which means
$$
S(P,f,\alpha)=\sum_{k=1}^nf(t_k)\Delta\alpha_k=\sum_{k=1}^mf(t_k)\Delta\alpha_k+\sum_{k=m+1}^nf(t_k)\Delta\alpha_k=0
$$
According to Definition 7.1, we get $\int_a^bfd\alpha=0$.

However, for any $\delta>0$, choose integer $N$ such that $1/N<\delta$, then there exist an integer $n$ such that
$$
a+\dfrac{n}{N}<b\le a+\dfrac{n+1}{N}
$$
we can form a partition $P$ of $[a,b]$ to be
$$
P=\left\{a,a+\dfrac{1}{N},\dots,a+\dfrac{n}{N},b\right\}
$$
if there happens to have some integer $m$ which makes $c=a+\frac{m}{N}$, we substitute the point $a+\frac{m}{N}$ in $P$ with two point $a+\frac{m-1/2}{N}$ and $a+\frac{m+1/2}{N}$. Thus we can form a partition $P$ with $\|P\|<\delta$ and $c\notin P$. Let the points adjacent to $c$ be marked with $p,q$, we have either $p=a+\dfrac{k-1}{N}<c<q=a+\dfrac{k}{N}$ or $p=a+\dfrac{k-1/2}{N}<c<q=a+\dfrac{k+1/2}{N}$, and
$$
S(P,f,\alpha)=f(t)(\alpha(q)-\alpha(p))=f(t),\quad t\in[p,q]
$$
if we choose $t\in[p,c)$, then $S(P,f,\alpha)=0$, if choose $t\in[c,q]$, then $S(P,f,\alpha)=1$. 

### 7.4

If $f\in R$ according to Definition 7.1, prove that $\int_a^bf(x)dx$ also exists according to the definition of Exercise 7.3.

#### Proof

*Remark*: The key point that Definition 7.1 and definition in Exercise 7.3 are equal, as we proved in this exercise, is that we are talking about Riemann integrals instead of Riemann-Stieltjes integral.

Let $I=\int_a^bf(x)dx$ and $M=\sup\{|f(x)|:x\in[a,b]\}$. Given $\varepsilon>0$, choose $P_{\varepsilon}$ such that $U(P_{\varepsilon},f)<I+\varepsilon/2$. Let $N$ be the number of subdivision points in $P_{\varepsilon}$ and let $\delta=\varepsilon/(2MN)$. If $\|P\|<\delta$, write
$$
U(P,f)=\sum_kM_k(f)\Delta x_k=S_1+S_2
$$
where $S_1$ is the sum of terms arising from those subintervals of $P$ containing no points of $P_{\varepsilon}$ and $S_2$ the sum of the remaining terms. Then
$$
S_1\le U(P_{\varepsilon},f)<I+\varepsilon/2,\quad S_2\le NM\|P\|<NM\delta=\varepsilon/2
$$
and hence $U(P,f)<I+\varepsilon$. Similarly we can find some $\delta'$ such that $\|P\|<\delta'$ means $L(P,f)>I-\varepsilon$. Hence $|S(P,f)-I|<\varepsilon$ if $\|P\|<\min(\delta,\delta')$.

### 7.5

Let $\{a_n\}$ be a sequence of real numbers. For $x\ge0$, define
$$
A(x)=\sum_{n\le x}a_n=\sum_{n=1}^{[x]}a_n,
$$
where $[x]$ is the greatest integer in $x$ and empty sums are interpreted as zero. Let $f$ have a continuous derivative in the interval $1\le x\le a$. Use Stieltjes integrals to derive the following formula:
$$
\sum_{n\le a}a_nf(n)=-\int_1^aA(x)f'(x)dx+A(a)f(a).
$$

#### Solution

$f$ is continuous on $[1,a]$ and $A(x)$ is a step function on $[1,a]$, thus $f\in R(A)$ by Theorem 7.11 and
$$
\int_1^afdA=\sum_{n=2}^{[x]}f(n)[A(n+)-A(n-)]=\sum_{n=2}^{[x]}f(n)a_n
$$
On the other hand, we have
$$
\int_1^afdA+\int_1^aAdf=A(a)f(a)-A(1)f(1)
$$
since $f$ has continuous derivative, we have
$$
\int_1^aAdf=\int_1^aA(x)f'(x)dx=A(a)f(a)-A(1)f(1)-\int_1^af(x)dA(x)
$$
use $A(1)=a_1$, we have
$$
A(1)f(1)+\int_1^af(x)dA(x)=\sum_{n=1}^{[x]}f(n)a_n=\sum_{n\le a}a_nf(n)\\=-\int_1^aA(x)f'(x)dx+A(a)f(a).
$$

### 7.6

Use Euler's summation formula, or integration by parts in a Stieltjes integral, to derive the following identities:
$$
\begin{aligned}&\text{a)}\quad\sum_{k=1}^n\dfrac{1}{k^s}=\dfrac{1}{n^{s-1}}+s\int_1^n\dfrac{[x]}{x^{s+1}}dx\quad\text{if }s\ne1.
\\
&\text{b)}\quad \sum_{k=1}^n\dfrac{1}{k}=\log{n}-\int_1^n\dfrac{x-[x]}{x^2}dx+1
\end{aligned}
$$

#### Solution

(a) Use the integer part of Euler’s summation formula, we have
$$
\sum_{k=1}^n\dfrac{1}{k^s}=\int_1^n\dfrac{1}{x^s}dx+\int_1^n\left(\dfrac{1}{x^s}\right)'\left(x-[x]-\dfrac{1}{2}\right)dx+\dfrac{1}{2}\left(1+\dfrac{1}{n^s}\right)
$$
if $s\ne1$, then
$$
\begin{aligned}
\int_1^n\left(\dfrac{1}{x^s}\right)'\left(x-[x]-\dfrac{1}{2}\right)dx&=-s\int_1^n\dfrac{1}{x^{s+1}}\left(x-[x]-\dfrac{1}{2}\right)dx
\\&=-s\int_1^n\dfrac{1}{x^s}dx+s\int_1^n\dfrac{[x]}{x^{s+1}}dx-\dfrac{1}{2}\left(\dfrac{1}{n^s}-1\right)
\end{aligned}
$$
combined with the first equation, we have
$$
\begin{aligned}
\sum_{k=1}^n\dfrac{1}{k^s}&=(1-s)\int_1^n\dfrac{1}{x^s}dx+s\int_1^n\dfrac{[x]}{x^{s+1}}dx-\dfrac{1}{2}\left(\dfrac{1}{n^s}-1\right)+\dfrac{1}{2}\left(\dfrac{1}{n^s}+1\right)
\\&=\dfrac{1}{n^{s-1}}-1+1+s\int_1^n\dfrac{[x]}{x^{s+1}}dx
\\&=\dfrac{1}{n^{s-1}}+s\int_1^n\dfrac{[x]}{x^{s+1}}dx
\end{aligned}
$$
(b) We have
$$
\sum_{k=1}^n\dfrac{1}{k}=\int_1^n\dfrac{1}{x}dx-\int_1^n\dfrac{1}{x^2}\left(x-[x]-\dfrac{1}{2}\right)dx+\dfrac{1}{2}\left(1+\dfrac{1}{n}\right)
$$
Since
$$
\dfrac{1}{2}\int_1^n\dfrac{1}{x^2}+\dfrac{1}{2}\left(1+\dfrac{1}{n}\right)=-\dfrac{1}{2}\left(\dfrac{1}{n}-1\right)+\dfrac{1}{2}\left(1+\dfrac{1}{n}\right)=1
$$
we have
$$
\sum_{k=1}^n\dfrac{1}{k}=\int_1^n\dfrac{1}{x}dx-\int_1^n\dfrac{1}{x^2}(x-[x])dx+1=\log{n}-\int_1^n\dfrac{x-[x]}{x^2}dx+1
$$

### 7.7

Assume $f'$ is continuous on $[1,2n]$ and use Euler's summation formula or integration by parts to prove that
$$
\sum_{k=1}^{2n}(-1)^kf(k)=\int_1^{2n}f'(x)([x]-2[x/2])dx.
$$

#### Proof

Use formula in Exercise 7.5 we let $a_n=(-1)^n$, then for $1\le x\le 2n$, we have $A(x)=\sum_{n=1}^{[x]}a_n$, thus $A(x)=0$ if $x\in[2k,2k+1)$ and $A(x)=-1$ if $x\in[2k+1,2k+2)$, specially, $A(2n)=0$ and we can write $A(x)=2[x/2]-[x]$. So we have
$$
\sum_{k=1}^{2n}(-1)^kf(k)=-\int_1^{2n}A(x)f'(x)dx+A(2n)f(2n)
$$
and the conclusion follows.

### 7.8

Let $\varphi_1(x)=x-[x]-\frac{1}{2}$ if $x$ is not an integer, and let $\varphi_1(x)=0$ if $x$ is an integer. Also, let $\varphi_2(x)=\int_0^x\varphi_1(t)dt$. If $f''$ is continuous on $[1,n]$ prove that Euler's summation formula implies that
$$
\sum_{k=1}^nf(k)=\int_1^nf(x)dx-\int_1^n\varphi_2(x)f''(x)dx+\dfrac{f(1)+f(n)}{2}.
$$

#### Proof

Using Euler’s summation formula we have
$$
\sum_{k=1}^nf(k)=\int_1^nf(x)dx+\int_1^nf'(x)\left(x-[x]-\dfrac{1}{2}\right)dx+\dfrac{f(1)+f(n)}{2}
$$
so we only have to prove that
$$
\int_1^nf'(x)\left(x-[x]-\dfrac{1}{2}\right)dx=-\int_1^n\varphi_2(x)f''(x)dx
$$
Notice that when $x$ shifts from $k$ to $k+1$, $\varphi_1(x)$ shifts from $-1/2$ to $1/2$, so $\int_k^{k+1}\varphi_1(t)dt=0$, which means $\varphi_2(n)=0$ whenever $n$ is a positive integer. Also, $f'\in R$ since $f'$ is continuous. Use Theorem 7.26 and integration by parts we get
$$
\begin{aligned}-\int_1^n\varphi_2(x)f''(x)dx&=-\int_1^n\varphi_2(x)df'(x)\\&=f'(1)\varphi_2(1)-f'(n)\varphi_2(n)+\int_1^nf'(x)d\varphi_2(x)
\\&=\int_1^nf'(x)d\varphi_2(x)=\int_1^nf'(x)\varphi_1(x)dx
\end{aligned}
$$
thus we only have to prove
$$
\int_1^nf'(x)\left(x-[x]-\dfrac{1}{2}-\varphi_1(x)\right)dx=0
$$
Let $g(x)=x-[x]-\frac{1}{2}-\varphi_1(x)$, then $g(x)=0$ if $x$ is not an integer, and $g(x)=-\frac{1}{2}$ if $x$ is an integer. Since $f'$ is continuous on $[1,n]$, it is bounded and we choose $M>1$ such that $|f'(x)|\le M$ for $x\in[1,n]$. For any $0<\varepsilon<1$, let $\delta=\varepsilon/(Mn)$ and we have 
$$
\int_1^nf'(x)g(x)dx=\int_1^{1+\delta}f'(x)g(x)dx+\sum_{j=2}^{n-1}\int_{j-\delta}^{j+\delta}f'(x)g(x)dx+\int_{n-\delta}^nf'(x)g(x)dx
$$
which shall give
$$
\left|\int_1^nf'(x)g(x)dx\right|\le\dfrac{M\delta}{2}+(n-2)M\delta+\dfrac{M\delta}{2}<nM\delta<\varepsilon
$$

### 7.9

Take $f(x)=\log{x}$ in Exercise 7.8 and prove that
$$
\log{n!}=(n+\frac{1}{2})\log{n}-n+1+\int_1^n\frac{\varphi_2(t)}{t^2}dt
$$

#### Proof

If $f(x)=\log{x}$ then $f'(x)=1/x$ and $f''(x)=-1/x^2$ when $x>0$. Thus
$$
\sum_{k=1}^nf(k)=\log{n!}=\int_1^n\log{x}dx+\frac{1}{2}(\log{n}-\log{1})+\int_1^n\frac{\varphi_2(t)}{t^2}dt
$$
to finish the proof, we see that $\log{1}=0$ and
$$
\int_1^n\log{x}dx=n\log{n}-\log{1}-\int_1^nxd\log{x}=n\log{n}-n+1
$$

### 7.10

If $x\ge1$, let $\pi(x)$ denote the number of primes $\le x$, that is $\pi(x)=\sum_{p\le x}1$, where the sum is extended over all primes $p\le x$. The *prime number theorem* states that
$$
\lim_{x\to\infty}\pi(x)\frac{\log{x}}{x}=1
$$
This is usually proved by studying a related function $\thetasym$ given by $\thetasym(x)=\sum_{p\le x}\log{p}$, where the sum is extended over all primes $p\le x$. Both functions $\pi$ and $\thetasym$ are step functions with jumps at the primes. This exercise show how the Riemann-Stieltjes integral can be used to relate these two functions.

a) If $x\ge2$, prove that $\pi(x)$ and $\thetasym(x)$ can be expressed as the following Riemann-Stieltjes integrals:
$$
\thetasym(x)=\int_{3/2}^x\log{t}d\pi(t),\qquad\pi(x)=\int_{3/2}^x\frac{1}{\log{t}}d\thetasym(t).
$$
b) If $x\ge2$, use integration by parts to show that
$$
\thetasym(x)=\pi(x)\log{x}-\int_2^x\frac{\pi(t)}{t}dt,\quad\pi(x)=\frac{\thetasym(x)}{\log{x}}+\int_2^x\frac{\thetasym(t)}{t\log^2{t}}dt.
$$
These equations can be used to prove that the prime number theorem is equivalent to the relation $\lim_{x\to\infty}\thetasym(x)/x=1$.

#### Solution

(a) It is easy to see $\pi(x)$ is discontinuous but right continuous at each prime $\le{x}$, and the jump at each discontinuous is 1. Hence
$$
\int_{3/2}^x\log{t}d\pi(t)=\sum_{p\ge3/2}^{p\le x}\log{p}(\pi(p+)-\pi(p-))=\sum_{p\le x}\log{p}=\thetasym(x)
$$
Similarly, $\thetasym(x)$ is discontinuous but right continuous at each prime $\le{x}$, and the jump at $p$ is $\log{p}$, hence
$$
\int_{3/2}^x\frac{1}{\log{t}}d\thetasym(t)=\sum_{p\ge3/2}^{p\le x}\frac{1}{\log p}(\thetasym(p+)-\thetasym(p-))=\sum_{p\le x}\frac{\log{p}}{\log p}=\pi(x)
$$
(b) Notice that $\pi(t)=0$ if $t<2$, use (a) we have
$$
\begin{aligned}
\thetasym(x)&=\pi(x)\log{x}-\pi(3/2)\log(3/2)-\int_{3/2}^x\pi(t)d(\log{t})
\\&=\pi(x)\log{x}-\int_{3/2}^2\pi(t)d(\log{t})-\int_2^x\frac{\pi(t)}{t}dt
\end{aligned}
$$
since
$$
\int_{3/2}^2\pi(t)d(\log{t})=\pi(2)[\log2-\log(2-)]=0
$$
the first equality holds. Also, notice that $\thetasym(t)=0$ if $t<2$, and from (a) we have
$$
\begin{aligned}
\pi(x)&=\int_{3/2}^x\frac{1}{\log t}d\thetasym(t)=\frac{\thetasym(x)}{\log x}-\frac{\thetasym(3/2)}{\log(3/2)}-\int_{3/2}^x\thetasym(t)d\left(\frac{1}{\log t}\right)
\\&=\frac{\thetasym(x)}{\log x}-\int_{3/2}^2\thetasym(t)d\left(\frac{1}{\log t}\right)+\int_2^x\frac{\thetasym(t)}{t\log^2{t}}dt
\end{aligned}
$$
since
$$
\int_{3/2}^2\thetasym(t)d\left(\frac{1}{\log t}\right)=\thetasym(2)\left(\frac{1}{\log2}-\frac{1}{\log(2-)}\right)=0
$$
the second equality holds.

### 7.11

If $\alpha\nearrow$ on $[a,b]$, prove that we have

a) $\bar{\int}_a^bfd\alpha=\bar{\int}_a^cfd\alpha+\bar{\int}_c^bfd\alpha,\quad(a<c<b)$.

b) $\bar{\int}_a^b(f+g)d\alpha\le\bar{\int}_a^bfd\alpha+\bar{\int}_a^bgd\alpha$.

c) $\underline{\int}_a^b(f+g)d\alpha\ge\underline{\int}_a^bfd\alpha+\underline{\int}_a^bgd\alpha$.

#### Proof

(a) Let $\forall\varepsilon>0$, there exist a partition $P\in\mathscr{P}[a,b]$ such that $U(P,f,\alpha)<\bar{\int}_a^bfd\alpha+\varepsilon$. If $c$ is not in $P$, we add $c$ to get a refined partition $P'$, split $P'$ to $P'=P_1\cup P_2$ with $P_1\in\mathscr{P}[a,c]$ and $P_2\in\mathscr{P}[c,b]$. So
$$
\bar{\int}_a^cfd\alpha+\bar{\int}_c^bfd\alpha\le U(P_1,f,\alpha)+U(P_2,f,\alpha)=U(P',f,\alpha)\le U(P,f,\alpha)
$$
which means
$$
\bar{\int}_a^cfd\alpha+\bar{\int}_c^bfd\alpha<\bar{\int}_a^bfd\alpha+\varepsilon\tag{1}
$$
On the other hand, we can choose $P_1'\in\mathscr{P}[a,c]$ and $P_2'\in\mathscr{P}[c,b]$ such that
$$
U(P_1',f,\alpha)<\bar{\int}_a^cfd\alpha+\dfrac{\varepsilon}{2},\quad U(P_2',f,\alpha)<\bar{\int}_c^bfd\alpha+\dfrac{\varepsilon}{2}
$$
Let $P_0=P_1'\cup P_2'$, we have
$$
\bar{\int}_a^bfd\alpha\le U(P_0,f,\alpha)=U(P_1',f,\alpha)+U(P_2',f,\alpha)<\bar{\int}_a^cfd\alpha+\bar{\int}_c^bfd\alpha+\varepsilon
$$
combined with (1) we get
$$
\bar{\int}_a^bfd\alpha-\varepsilon<\bar{\int}_a^cfd\alpha+\bar{\int}_c^bfd\alpha<\bar{\int}_a^bfd\alpha+\varepsilon
$$
since $\varepsilon$ is arbitrary, the proof is complete.

(b) Let $P\in\mathscr{P}[a,b]$, on every segment $I$ of $P$ we have
$$
\max_{x\in I}(f+g)\le\max_{x\in I}f+\max_{x\in I}g\implies U(P,f+g,\alpha)\le U(P,f,\alpha)+U(P,g,\alpha)
$$
which gives
$$
\bar{\int}_a^b(f+g)d\alpha\le U(P,f,\alpha)+U(P,g,\alpha)
$$
For any $\varepsilon>0$, choose $P_1,P_2\in\mathscr{P}[a,b]$ such that
$$
U(P_1,f,\alpha)<\bar{\int}_a^bfd\alpha+\dfrac{\varepsilon}{2},\quad U(P_2,g,\alpha)<\bar{\int}_a^bgd\alpha+\dfrac{\varepsilon}{2}
$$
thus
$$
\begin{aligned}
\bar{\int}_a^b(f+g)d\alpha&\le U(P_1\cup P_2,f+g,\alpha)
\\&\le U(P_1\cup P_2,f,\alpha)+U(P_1\cup P_2,g,\alpha)
\\&\le U(P_1,f,\alpha)+U(P_2,g,\alpha)
\\&<\bar{\int}_a^bfd\alpha+\bar{\int}_a^bgd\alpha+\varepsilon
\end{aligned}
$$
since $\varepsilon$ is arbitrary, the proof is complete.

(c) The proof is similar to (b), ommitted.

### 7.12

Give an example of a bounded function $f$ and an increasing function $\alpha$ defined on $[a,b]$ such that $|f|\in R(\alpha)$ but for which $\int_a^bfd\alpha$ does not exist.

#### Solution

Let $f$ be defined on $[a,b]$ by
$$
f(x)=\begin{cases}1,&x\in[a,b]\cap\mathbf{Q}\\-1,&x\in[a,b]-\mathbf{Q}\end{cases}
$$
and $\alpha(x)=x$ on $[a,b]$. Then $|f|=1$ on $[a,b]$, so $|f|\in R$, but $\bar{I}(f,\alpha)=b-a$ and $\underline{I}(f,\alpha)=a-b$, thus as long as $a<b$ we will have $\bar{I}(f,\alpha)\ne\underline{I}(f,\alpha)$, thus $\int_a^bfd\alpha$ does not exist.

### 7.13

Let $\alpha$ be a continuous function of bounded variation on $[a,b]$. Assume $g\in R(\alpha)$ on $[a,b]$ and define $\beta(x)=\int_a^xg(t)d\alpha(t)$ if $x\in[a,b]$. Show that:

a) If $f\nearrow$ on $[a,b]$, there exists a point $x_0\in[a,b]$ such that
$$
\int_a^bfd\beta=f(a)\int_a^{x_0}gd\alpha+f(b)\int_{x_0}^bgd\alpha.
$$
b) If, in addition, $f$ is continuous on $[a,b]$, we also have
$$
\int_a^bf(x)g(x)d\alpha(x)=f(a)\int_a^{x_0}gd\alpha+f(b)\int_{x_0}^bgd\alpha.
$$

#### Solution

(a) For $\varepsilon>0$, since $g$ is bounded on $[a,b]$, we have $|g|\le M$ for some $M>0$, since $\alpha$ is continuous, there exists $\delta>0$ such that for $x_1,x_2\in[a,b]$, if $|x_1-x_2|<\delta$, then $|\alpha(x_1)-\alpha(x_2)|<\varepsilon/M$, this means
$$
|x_1-x_2|<\delta\implies|\beta(x_1)-\beta(x_2)|=\left|\int_{x_1}^{x_2}gd\alpha\right|\le M\left|\int_{x_1}^{x_2}d\alpha\right|<\varepsilon
$$
hence $\beta$ is continuous. Use the second Mean-Value Theorem for Riemann-Stieltjes integrals, there exists a point $x_0\in[a,b]$ such that
$$
\int_a^bf(x)d\beta(x)=f(a)\int_a^{x_0}d\beta(x)+f(b)\int_{x_0}^bd\beta(x)
$$
Theorem 7.26 gives $\int_a^{x_0}d\beta(x)=\int_a^{x_0}g(x)d\alpha(x)$ and $\int_{x_0}^{b}d\beta(x)=\int_{x_0}^bg(x)d\alpha(x)$.

(b) Theorem 7.27 shows $f\in R(\alpha)$, thus $fg\in R(\alpha)$, Theorem 7.26 gives $\int_a^bf(x)g(x)d\alpha(x)=\int_a^bf(x)d\beta(x)$ and then use (a).

### 7.14

Assume $f\in R(\alpha)$ on $[a,b]$, where $\alpha$ is of bounded variation on $[a,b]$. Let $V(x)$ denote the total variation of $\alpha$ on $[a,x]$ for each $x\in[a,b]$, and let $V(a)=0$. Show that
$$
\left|\int_a^bfd\alpha\right|\le\int_a^b|f|dV\le MV(b),
$$
where $M$ is an upper bound for $|f|$ on $[a,b]$. In particular, when $\alpha(x)=x$, the inequality becomes
$$
\left|\int_a^bf(x)dx\right|\le M(b-a).
$$

#### Solution

That $f\in R(\alpha)$ means $f\in R(V)$ and $|f|\in R(V)$, and we have
$$
\left|\int_a^bfd\alpha\right|\le\int_a^b|f|d\alpha,\quad\int_a^b|f|dV\le M\int_a^bdV=MV(b).
$$
To finish the proof, notice that for any two points $x,y\in[a,b]$ with $x<y$, we have
$$
\alpha(x)-\alpha(y)\le|\alpha(x)-\alpha(y)|\le V(y)-V(x)
$$
thus
$$
S(P,|f|,\alpha)=\sum_k|f(t_k)|\Delta\alpha_k\le\sum_k|f(t_k)|\Delta V_k=S(P,|f|,V)
$$
which means $\int_a^b|f|d\alpha\le\int_a^b|f|dV$. When $\alpha(x)=x$, we have $V(x)=x-a$ and $MV(b)=M(b-a)$.

### 7.15

Let $\{\alpha_n\}$ be a sequence of functions of bounded variation on $[a,b]$. Suppose there exists a function $\alpha$ defined on $[a,b]$ such that the total variation of $\alpha-\alpha_n$ on $[a,b]$ tends to $0$ as $n\to\infty$. Assume also that $\alpha(a)=\alpha_n(a)=0$ for each $n=1,2,\dots$. If $f$ is continuous on $[a,b]$, prove that
$$
\lim_{n\to\infty}\int_a^bf(x)d\alpha_n(x)=\int_a^bf(x)d\alpha(x).
$$

#### Solution

Since $V(\alpha-\alpha_n)\to0$ as $n\to\infty$, there exist an integer $N$ such that $V(\alpha-\alpha_n)<1$ if $n\ge N$, since the function $\alpha_N$ is of bounded variation on $[a,b]$, we can choose $M>0$ such that $\sum|\Delta\alpha_N|\le M$, given any points $x,y\in[a,b]$ with $x<y$ we have
$$
|\alpha(y)-\alpha(x)|=|\Delta\alpha|\le|\Delta(\alpha-\alpha_N)|+|\Delta\alpha_N|
$$
thus
$$
\sum|\Delta\alpha|\le\sum|\Delta(\alpha-\alpha_N)|+\sum|\Delta\alpha_N|\le V(\alpha-\alpha_N)+M<1+M
$$
this means $\alpha$ is of bounded variation on $[a,b]$, thus $f\in R(\alpha)$.

If $f$ is continuous on $[a,b]$, then there exists $M'>0$ such that $|f|\le M'$ on $[a,b]$. For $\forall\varepsilon>0$, there exists an integer $N'$ such that $V(\alpha-\alpha_n)<\varepsilon/M'$ if $n>N'$. Since $f\in R(\alpha-\alpha_n)$ by Theorem 7.27 and Theorem 7.3, we have
$$
\left|\int_a^bfd(\alpha-\alpha_n)\right|\le M|[\alpha(b)-\alpha_n(b)-\alpha(a)+\alpha_n(a)]|\le M'V(\alpha-\alpha_n)<\varepsilon
$$
thus we have
$$
n>N'\implies\left|\int_a^bfd\alpha-\int_a^bfd\alpha_n\right|=\left|\int_a^bfd(\alpha-\alpha_n)\right|<\varepsilon
$$
and the conclusion follows.

### 7.16

If $f,f^2,g,g^2\in R(\alpha)$ on $[a,b]$, prove that
$$
\dfrac{1}{2}\int_a^b\left[\int_a^b\begin{vmatrix}f(x)&g(x)\\f(y)&g(y)\end{vmatrix}^2d\alpha(y)\right]d\alpha(x)\\=\left(\int_a^bf^2(x)d\alpha(x)\right)\left(\int_a^bg^2(x)d\alpha(x)\right)-\left(\int_a^bf(x)g(x)d\alpha(x)\right)^2.
$$
When $\alpha\nearrow$ on $[a,b]$, deduce the Cauchy-Schwarz inequality
$$
\left(\int_a^bf(x)g(x)d\alpha(x)\right)^2\le\left(\int_a^bf^2(x)d\alpha(x)\right)\left(\int_a^bg^2(x)d\alpha(x)\right)
$$

#### Proof

We have
$$
\begin{aligned}
&\dfrac{1}{2}\int_a^b\left[\int_a^b\begin{vmatrix}f(x)&g(x)\\f(y)&g(y)\end{vmatrix}^2d\alpha(y)\right]d\alpha(x)
\\=&\dfrac{1}{2}\int_a^b\left[\int_a^b\big(f(x)g(y)-f(y)g(x)\big)^2d\alpha(y)\right]d\alpha(x)
\\=&\dfrac{1}{2}\int_a^b\left[\int_a^b\big(f^2(x)g^2(y)+f^2(y)g^2(x)-2f(x)g(x)f(y)g(y)\big)d\alpha(y)\right]d\alpha(x)
\\=&\dfrac{1}{2}\int_a^b\left[f^2(x)\int_a^bg^2(y)d\alpha(y)+g^2(x)\int_a^bf^2(y)d\alpha(y)\right]d\alpha(x)
\\&\quad-\int_a^b\left[f(x)g(x)\int_a^bf(y)g(y)d\alpha(y)\right]d\alpha(x)
\\=&\dfrac{1}{2}\left(\int_a^bg^2(y)d\alpha(y)\right)\left(\int_a^bf^2(x)d\alpha(x)\right)+\left(\int_a^bf^2(y)d\alpha(y)\right)\left(\int_a^bg^2(x)d\alpha(x)\right)
\\&\quad-\left(\int_a^bf(y)g(y)d\alpha(y)\right)\left(\int_a^bf(x)g(x)d\alpha(x)\right)
\\=&\dfrac{1}{2}\left(\int_a^bg^2(x)d\alpha(x)\right)\left(\int_a^bf^2(x)d\alpha(x)\right)+\left(\int_a^bf^2(x)d\alpha(x)\right)\left(\int_a^bg^2(x)d\alpha(x)\right)
\\&\quad-\left(\int_a^bf(x)g(x)d\alpha(x)\right)\left(\int_a^bf(x)g(x)d\alpha(x)\right)
\\=&\left(\int_a^bf^2(x)d\alpha(x)\right)\left(\int_a^bg^2(x)d\alpha(x)\right)-\left(\int_a^bf(x)g(x)d\alpha(x)\right)^2
\end{aligned}
$$
and when $\alpha\nearrow$ on $[a,b]$, use Theorem 7.20 we have
$$
\int_a^b\begin{vmatrix}f(x)&g(x)\\f(y)&g(y)\end{vmatrix}^2d\alpha(y)\ge\int_a^b0d\alpha(y)=0
$$
and
$$
\int_a^b\left[\int_a^b\begin{vmatrix}f(x)&g(x)\\f(y)&g(y)\end{vmatrix}^2d\alpha(y)\right]d\alpha(x)\ge\int_a^b0d\alpha(x)=0
$$
which shows
$$
\left(\int_a^bf^2(x)d\alpha(x)\right)\left(\int_a^bg^2(x)d\alpha(x)\right)-\left(\int_a^bf(x)g(x)d\alpha(x)\right)^2\ge0
$$
and the Cauchy-Schwarz inequality follows.

### 7.17

Assume that $f\in R(\alpha),g\in R(\alpha)$ and $f\cdot g\in R(\alpha)$ on $[a,b]$. Show that
$$
\dfrac{1}{2}\int_a^b\left[\int_a^b\big(f(y)-f(x)\big)\big(g(y)-g(x)\big)d\alpha(y)\right]d\alpha(x)
\\=\big(\alpha(b)-\alpha(a)\big)\int_a^bf(x)g(x)d\alpha(x)-\left(\int_a^bf(x)d\alpha(x)\right)\left(\int_a^bg(x)d\alpha(x)\right)
$$
If $\alpha\nearrow$ on $[a,b]$, deduce the inequality
$$
\left(\int_a^bf(x)d\alpha(x)\right)\left(\int_a^bg(x)d\alpha(x)\right)\le\big(\alpha(b)-\alpha(a)\big)\int_a^bf(x)g(x)d\alpha(x)
$$
when both $f$ and $g$ are increasing (or both are decreasing) on $[a,b]$. Show that the reverse inequality holds if $f$ increases and $g$ decreases on $[a,b]$.

#### Proof

For convenience we denote
$$
A=\int_a^bf(x)d\alpha(x),\quad B=\int_a^bg(x)d\alpha(x),\quad C=\int_a^bf(x)g(x)d\alpha(x)
$$
then we have
$$
\begin{aligned}&\int_a^b\big(f(y)-f(x)\big)\big(g(y)-g(x)\big)d\alpha(y)
\\=&\int_a^b\big(f(y)g(y)+f(x)g(x)-f(x)g(y)-f(y)g(x)\big)d\alpha(y)
\\=&\int_a^bf(y)g(y)d\alpha(y)+f(x)g(x)\int_a^bd\alpha(y)-f(x)\int_a^bg(y)d\alpha(y)\\&-g(x)\int_a^bf(y)d\alpha(y)
\\=&C+f(x)g(x)[\alpha(b)-\alpha(a)]-Bf(x)-Ag(x)
\end{aligned}
$$
hence
$$
\begin{aligned}
&\int_a^b\left[\int_a^b\big(f(y)-f(x)\big)\big(g(y)-g(x)\big)d\alpha(y)\right]d\alpha(x)
\\=&\int_a^b\bigg(C+f(x)g(x)[\alpha(b)-\alpha(a)]-Bf(x)-Ag(x)\bigg)d\alpha(x)
\\=&[\alpha(b)-\alpha(a)]\left[C+\int_a^bf(x)g(x)d\alpha(x)\right]-B\int_a^bf(x)d\alpha(x)-A\int_a^bg(x)d\alpha(x)
\\=&2[\alpha(b)-\alpha(a)]C-BA-AB=2[\alpha(b)-\alpha(a)]C-2AB
\end{aligned}
$$
thus we have
$$
\dfrac{1}{2}\int_a^b\left[\int_a^b\big(f(y)-f(x)\big)\big(g(y)-g(x)\big)d\alpha(y)\right]d\alpha(x)=[\alpha(b)-\alpha(a)]C-AB
$$
when $\alpha\nearrow$ on $[a,b]$, we see that if both $f$ and $g$ are increasing (or both are decreasing) on $[a,b]$, then $\big(f(y)-f(x)\big)\big(g(y)-g(x)\big)\ge0$ for any $x,y\in[a,b]$, thus use Theorem 7.20 we see the original integral $\ge0$. If $f$ increases and $g$ decreases on $[a,b]$, then  for any $x,y\in[a,b]$ we have $\big(f(y)-f(x)\big)\big(g(y)-g(x)\big)\le0$, so the original integral $\le0$ and the reverse inequality holds.