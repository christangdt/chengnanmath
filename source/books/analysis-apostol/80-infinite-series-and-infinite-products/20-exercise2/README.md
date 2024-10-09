# Exercise 15-27 (Series)

### 8.15

Test for convergence ($p$ and $q$ denote fixed real numbers).
$$
\begin{aligned}
&a)\sum_{n=1}^{\infty}n^3e^{-n},\qquad&&b)\sum_{n=2}^{\infty}(\log{n})^p,\\&c)\sum_{n=1}^{\infty}p^nn^p\quad(p>0)
&&d)\sum_{n=2}^{\infty}\dfrac{1}{n^p-n^q}\quad(0<q<p),\\&e)\sum_{n=1}^{\infty}n^{-1-1/n},&&f)\sum_{n=1}^{\infty}\dfrac{1}{p^n-q^n}\quad(0<q<p)
\\&g)\sum_{n=1}^{\infty}\dfrac{1}{n\log(1+1/n)},&&h)\sum_{n=2}^{\infty}\dfrac{1}{(\log{n})^{\log{n}}},
\\&i) \sum_{n=3}^{\infty}\dfrac{1}{n\log{n}(\log{\log{n}})^p},&&j)\sum_{n=3}^{\infty}\left(\dfrac{1}{\log\log{n}}\right)^{\log\log{n}},
\\&k)\sum_{n=1}^{\infty}(\sqrt{1+n^2}-n),&&l)\sum_{n=2}^{\infty}n^p\left(\dfrac{1}{\sqrt{n-1}}-\dfrac{1}{\sqrt{n}}\right),
\\&m)\sum_{n=1}^{\infty}(\sqrt[n]{n}-1)^n,&&n)\sum_{n=1}^{\infty}n^p(\sqrt{n+1}-2\sqrt{n}+\sqrt{n-1}).
\end{aligned}
$$

#### Solution

(a) Use root test, we have $\lim_{n\to\infty}\sqrt[n]{n^3e^{-n}}=1/e<1$, thus the series converges.

(b) We have $\lim_{n\to\infty}(\log{n})^p\ne0$ if $p\ge0$, thus the series diverges if $p\ge0$. When $p<0$, we let $f(x)=(\log{x})^p$, then $\lim_{x\to+\infty}f(x)=0$ , since
$$
t_n=\int_2^nf(x)dx=\int_2^n\frac{1}{(\log{x})^{|p|}}dx=\int_{\log2}^{\log{n}}\frac{1}{t^{|p|}}de^t=\int_{\log2}^{\log{n}}\frac{e^t}{t^{|p|}}dt
$$
use the Taylor formula, we choose some integer $k$ such that $k>[|p|]+1$, so $k-|p|>0$, and $e^t>t^k/k!$, thus
$$
t_n=\int_{\log2}^{\log{n}}\frac{e^t}{t^{|p|}}dt>=\int_{\log2}^{\log{n}}\dfrac{t^{k-|p|}}{k!}dt\implies \lim_{n\to\infty}t_n=+\infty
$$
so the sequence $\{t_n\}$ diverges, thus the series diverges by the Integral test.

(c) Use root test, we have $\lim_{n\to\infty}\sqrt[n]{p^nn^p}=p$, thus the series converges if $p<1$, diverges if $p>1$, when $p=1$, the series obviously diverges.

(d) We have
$$
\lim_{n\to\infty}\dfrac{\dfrac{1}{n^p}}{\dfrac{1}{n^p-n^q}}=\lim_{n\to\infty}\dfrac{n^p-n^q}{n^p}=\lim_{n\to\infty}\dfrac{1-n^{q-p}}{1}=1
$$
thus the series converges if $p>1$, and diverges if $p\le1$.

(e) We have
$$
n^{-1-1/n}=\dfrac{1}{n^{1+1/n}}=\dfrac{1}{n\cdot n^{1/n}}\implies\lim_{n\to\infty}\dfrac{\dfrac{1}{n}}{\dfrac{1}{n\cdot n^{1/n}}}=\lim_{n\to\infty}n^{1/n}=1
$$

thus the series diverges by limit comparison test.

(f) We have
$$
\lim_{n\to\infty}\dfrac{\dfrac{1}{p^n}}{\dfrac{1}{p^n-q^n}}=\lim_{n\to\infty}\dfrac{p^n-q^n}{p^n}=\lim_{n\to\infty}1-\left(\dfrac{q}{p}\right)^n=1
$$
thus the series converges if $p>1$, and diverges if $p\le1$.

(g) Since
$$
\lim_{x\to0+}\dfrac{x}{\log(1+x)}=\lim_{x\to0+}\dfrac{1}{\dfrac{1}{1+x}}=1\implies\lim_{n\to\infty}\dfrac{1}{n\log(1+1/n)}=1
$$
the series diverges.

(h) We have
$$
\log(\log{n})=e^{\log(\log{n})^{log n}}=e^{\log n\log{\log n}}=n^{\log\log n}\ge n^2
$$
if $n$ is big enough, thus $\dfrac{1}{(\log{n})^{\log{n}}}\le\dfrac{1}{n^2}$, so this series converges.

(i) If $p\le0$, then $\dfrac{1}{n\log{n}(\log{\log{n}})^p}\ge\dfrac{1}{n\log n}$ for $n\ge a$ with $a$ some positive integer, use Integral test, we have $t_n=\int_a^n\dfrac{1}{x\log x}dx=\log\log n-\log\log a$, thus $\{t_n\}$ diverges and so the series diverges. 

If $p>0$, let $f(x)=\dfrac{1}{x\log{x}(\log\log x)^p}$, we can again use Integral test to get
$$
t_n=\int_3^n\dfrac{dx}{x\log{x}(\log\log x)^p}=\int_{\log\log3}^{\log\log n}\dfrac{dy}{y^p}
$$
if $p\le1$, then $t_n$ diverges and the series diverges, if $p>1$, then $t_n$ converges and so is the series.

(j) Omitted. 

(k) $\sqrt{1+n^2}-n=\dfrac{1}{\sqrt{1+n^2}+n}$, since
$$
\lim_{n\to\infty}\dfrac{n}{\sqrt{1+n^2}+n}=\frac{1}{2}
$$
the series diverges.

(l) We have
$$
n^p\left(\dfrac{1}{\sqrt{n-1}}-\dfrac{1}{\sqrt{n}}\right)=n^p\dfrac{\sqrt{n}-\sqrt{n-1}}{\sqrt{n(n-1)}}=\dfrac{n^{p-3/2}}{\sqrt{\dfrac{n(n-1)}{n^2}}\dfrac{(\sqrt{n}+\sqrt{n-1})}{\sqrt{n}}}
$$
so if $p<1/2$, the series converges, and if $p\ge1/2$, the series diverges.

(m) Use root test we see the series converges.

(n) We have
$$
\begin{aligned}(\sqrt{n+1}-2\sqrt{n}+\sqrt{n-1})&=\dfrac{1}{\sqrt{n+1}+\sqrt{n}}-\dfrac{1}{\sqrt{n}+\sqrt{n-1}}
\\&=\dfrac{\sqrt{n-1}-\sqrt{n+1}}{(\sqrt{n+1}+\sqrt{n})(\sqrt{n}+\sqrt{n-1})}
\\&=\dfrac{-2}{(\sqrt{n+1}+\sqrt{n})(\sqrt{n}+\sqrt{n-1})(\sqrt{n-1}+\sqrt{n+1})}

\end{aligned}
$$
thus
$$
n^p(\sqrt{n+1}-2\sqrt{n}+\sqrt{n-1})=\dfrac{1}{n^{2/3-p}}\dfrac{-2n^{3/2}}{(\sqrt{n+1}+\sqrt{n})(\sqrt{n}+\sqrt{n-1})(\sqrt{n-1}+\sqrt{n+1})}
$$
so if $p<1/2$, the series converges, and if $p\ge1/2$, the series diverges.

### 8.16

Let $S=\{n_1,n_2,\dots\}$ denote the collection of those positive integers that do not involve the digit 0 in their decimal representation. Show that $\sum_{k=1}^{\infty}1/n_k$ converges and has a sum less than 90.

#### Solution

Let $S_i$ be the subset of $S$ which contains only numbers with $i$ digits, which means $S_1=\{1,2,3,4,5,6,7,8,9\}$, and $S_2$ contains $11,\dots,19$ and $21,\dots,29$ till $91,\dots,99$, etc. For each $S_i$, every digit has 9 choices (from 1 to 9), thus each $S_i$ has $9^i$ elements, if $n_k\in S_i$, then $n_k\ge10^{i-1}$, for example, all elements in $S_1$ is no less than 1, all elements in $S_2$ is no less than 10. Thus we have
$$
\sum_{n_k\in S_i}\dfrac{1}{n_k}\le\dfrac{9^i}{10^{i-1}}\implies\sum_{k=1}^{\infty}\dfrac{1}{n_k}=\sum_{i=1}^{\infty}\sum_{n_k\in S_i}\dfrac{1}{n_k}\le\sum_{i=1}^{\infty}\dfrac{9^i}{10^{i-1}}=90
$$
Obviously equality cannot hold, and the conclusion is proved.

### 8.17

Given integers $a_1,a_2,\dots$ such that $1\le a_n\le n-1,n=2,3,\dots$. Show that the sum of the series $\sum_{n=1}^{\infty}a_n/n!$ is rational if and only if there exists an integer $N$ such that $a_n=n-1$ for all $n\ge N$.

#### Proof

$(\Rightarrow)$: Let $N$ be the integer such that $a_n=n-1$ for all $n\ge N$. Then $\sum_{n=1}^{\infty}a_n/n!=\sum_{n=1}^{N-1}a_n/n!+\sum_{n=N}^{\infty}(n-1)/n!$, since each $a_n/n!$ is rational for $1\le n<N$, the number $\sum_{n=1}^{N-1}a_n/n!$ is rational, and we have
$$
\sum_{n=N}^{\infty}\frac{n-1}{n!}=\sum_{n=N}^{\infty}\left[\frac{1}{(n-1)!}-\frac{1}{n!}\right]=\frac{1}{(N-1)!}
$$
which is also rational, thus the original series is rational.

$(\Leftarrow)$: Suppose $\sum_{n=1}^{\infty}a_n/n!=q/p$ for integers $p,q$ with $p>0$, then $p!\sum_{n=1}^{\infty}a_n/n!$ is a positive integer, which means $p!\sum_{n=p+1}^{\infty}a_n/n!$ is a positive integer, we have
$$
1\le p!\sum_{n=p+1}^{\infty}\frac{a_n}{n!}\le p!\sum_{n=p+1}^{\infty}\frac{n-1}{n!}=\frac{p!}{p!}=1
$$
thus $a_n=n-1$ for $n\ge p+1$.

### 8.18

Let $p$ and $q$ be fixed integers, $p\ge q\ge 1$, and let
$$
x_n=\sum_{k=qn+1}^{pn}\dfrac{1}{k},\quad s_n=\sum_{k=1}^n\dfrac{(-1)^{k+1}}{k}.
$$
a) Use formula (8) to prove that $\lim_{n\to\infty}x_n=\log(p/q)$.

b) When $q=1,p=2$, show that $s_{2n}=x_n$ and deduce that
$$
\sum_{n=1}^{\infty}\dfrac{(-1)^{n+1}}{n}=\log2
$$
c) Rearrange the series in (b), writing alternately $p$ positive terms followed by $q$ negative terms and use (a) to show that this rearrangement has sum $\log2+\frac{1}{2}\log(p/q)$.

d) Find the sum of $\sum_{n=1}^{\infty}(-1)^{n+1}(1/(3n-2)-1/(3n-1))$.

#### Solution

(a) Formula (8) is $\sum_{k=1}^n(1/k)=\log{n}+C+O(1/n)$, thus
$$
x_n=\sum_{k=qn+1}^{pn}\dfrac{1}{k}=\sum_{k=1}^{pn}\dfrac{1}{k}-\sum_{k=1}^{qn}\dfrac{1}{k}=\log{pn}+C+O(1/n)-(\log{qn}+C+O(1/n))=\log({p/q})+O(1/n)
$$
thus $\lim_{n\to\infty}x_n=\log(p/q)$.

(b) Use induction. $s_2=1-1/2=1/2=x_1$, suppose we already have $s_{2n}=x_n$, then
$$
\begin{aligned}s_{2n+2}&=s_{2n}+\frac{1}{2n+1}-\frac{1}{2n+2}=x_n+\frac{1}{2n+1}-\frac{1}{2n+2}\\&=\frac{1}{n+1}+\sum_{k=n+2}^{2n}\frac{1}{k}+\frac{1}{2n+1}-\frac{1}{2n+2}=\sum_{k=n+2}^{2n}\frac{1}{k}+\frac{1}{2n+1}+\frac{1}{2n+2}
\\&=\sum_{k=n+2}^{2n+2}\frac{1}{k}=x_{n+1}
\end{aligned}
$$
thus we proved $s_{2n}=x_n$ for all $n$. And so
$$
\sum_{n=1}^{\infty}\dfrac{(-1)^{n+1}}{n}=\lim_{n\to\infty}s_{n}=\lim_{n\to\infty}x_{n}=\log2
$$
(c) The positive series in (b) has the form $\dfrac{1}{2k+1}$ and the negative series in (b) has the form $\dfrac{-1}{2k}$, if we regard each $p$ positive terms followed by $q$ negative terms as a unit, namely $a_k$, then
$$
a_1=\frac{1}{1}+\frac{1}{3}+\cdots+\frac{1}{2p-1}-\frac{1}{2}-\cdots-\frac{1}{2q}
\\
a_2=\frac{1}{2p+1}+\cdots+\frac{1}{2(2p)-1}-\frac{1}{2q+2}-\cdots-\frac{1}{2(2q)}
$$
we can conclude
$$
a_n=\frac{1}{2(n-1)p+1}+\cdots+\frac{1}{2np-1}-\frac{1}{2(n-1)q+2}-\cdots-\frac{1}{2nq}
$$
thus by Theorem 8.13, the rearranged series converges to $\sum_{n=1}^{\infty}a_n$, and we have
$$
\begin{aligned}\sum_{k=1}^na_k&=\sum_{k=1}^{2np}\frac{1}{k}-\sum_{k=1}^{np}\frac{1}{2k}-\sum_{k=1}^{nq}\frac{1}{2k}
\\&=\log{(2np)}+C+O(1/n)-\frac{1}{2}\log(np)-\frac{C}{2}-O(1/n)-\frac{1}{2}\log(nq)-\frac{C}{2}-O(1/n)
\\&=\log\frac{2p}{\sqrt{pq}}+O(1/n)
\end{aligned}
$$
so $\sum_{n=1}^{\infty}a_n=\log2+\frac{1}{2}\log(p/q)$.

(d) We have
$$
\sum_{n=1}^{\infty}(-1)^{n+1}\left(\frac{1}{3n-2}-\frac{1}{3n-1}\right)=\sum_{n=1}^{\infty}\frac{(-1)^{n+1}}{n}-\sum_{n=1}^{\infty}\frac{(-1)^{n+1}}{3n}=\frac{2}{3}\log{2}
$$

### 8.19

Let $c_n=a_n+ib_n$, where $a_n=(-1)^n/\sqrt{n},b_n=1/n^2$. Show that $\sum c_n$ is conditionally convergent.

#### Proof

Since $\sum a_n$ is convergent by Theorem 8.16 and $\sum b_n$ is convergent, we see that $\sum c_n$ is convergent. On the other hand, we have
$$
\sum |c_n|=\sum\sqrt{\frac{1}{n}+\frac{1}{n^4}}=\sum\frac{1}{\sqrt{n}}\sqrt{1+\frac{1}{n^3}}\ge\sum\frac{1}{\sqrt{n}}\ge\sum\frac{1}{n}
$$
thus $\sum|c_n|$ diverges.

### 8.20

Use Theorem 8.23 to derive the following formulas:

a) $\displaystyle{\sum_{k=1}^{n}\frac{\log k}{k}=\frac{1}{2}\log^2n+A+O\left(\frac{\log n}{n}\right)}$, ($A$ is constant).

b) $\displaystyle{\sum_{k=2}^{n}\frac{1}{k\log k}=\log\log n+B+O\left(\frac{1}{n\log n}\right)}$, ($B$ is constant).

#### Proof

(a) Let $f(x)=\log{x}/x$, then $f$ is positively decreasing on $[2,+\infty)$ and $\lim_{x\to+\infty}f(x)=0$. So $f$ satisfy the prerequisites of Theorem 8.23, which means
$$
\sum_{k=1}^{n}\frac{\log k}{k}=\sum_{k=2}^{n}\frac{\log k}{k}=\int_2^n\frac{\log{x}}{x}dx+D+O\left(\frac{\log n}{n}\right)=\frac{1}{2}\log^2n-\frac{1}{2}\log^22+D+O\left(\frac{\log n}{n}\right)
$$
Let $A=D-\frac{1}{2}\log^22$, and the conclusion is proved.

(b) Let $f(x)=\dfrac{1}{x\log x}$ on $[2,+\infty)$, since $x$ and $\log x$ are increasing on $[2,+\infty)$, which tends to $+\infty$ as $x\to\infty$, we see that $f$ is positively decreasing on $[2,+\infty)$ and $\lim_{x\to+\infty}f(x)=0$. So $f$ satisfy the prerequisites of Theorem 8.23, which means
$$
\sum_{k=2}^{n}\frac{1}{k\log k}=\int_2^n\frac{1}{x\log x}dx+D+O\left(\frac{1}{n\log n}\right)=\log\log n-\log\log2+D+O\left(\frac{1}{n\log n}\right)
$$
Let $B=D-\log\log2$ we get the result.


### 8.21

If $0<a\le1,s>1$, define $\zeta(s,a)=\sum_{n=0}^{\infty}(n+a)^{-s}$.

a) Show that this series converges absolutely for $s>1$ and prove that
$$
\sum_{h=1}^k\zeta\left(s,\frac{h}{k}\right)=k^s\zeta(s),\quad\text{if }k=1,2,\dots
$$
where $\zeta(s)=\zeta(s,1)$ is the Riemann zeta function.

b) Prove that $\sum_{n=1}^{\infty}(-1)^{n-1}/n^s=(1-2^{1-s})\zeta(s)$ if $s>1$.

#### Proof

(a) If $s>1$, then $\sum_{n=0}^{\infty}(n+a)^{-s}<a^{-s}+\sum_{n=1}^{\infty}n^{-s}$, the latter is a convergent series. 

The next equality to prove seems to be wrong, when trying to prove it, we will finally reach to the statement
$$
\sum_{h=1}^k\dfrac{1}{(kn+h)^s}=\dfrac{1}{(n+1)^s},\quad s>1,n=0,1,2,\dots
$$
and the equality to prove is true if and only if this statement is true. But this statement is false.

(b) Notice that 
$$
\sum_{n=1}^{\infty}(-1)^{n-1}/n^s=\dfrac{1}{1^s}-\dfrac{1}{2^s}+\dfrac{1}{3^s}-\dfrac{1}{4^s}+\cdots
\\
\zeta(s)=\zeta(s,1)=\sum_{n=0}^{\infty}(n+1)^{-s}=\sum_{n=1}^{\infty}\dfrac{1}{n^s}=\dfrac{1}{1^s}+\dfrac{1}{2^s}+\dfrac{1}{3^s}+\dfrac{1}{4^s}+\cdots
$$
thus we have
$$
\zeta(s)-\sum_{n=1}^{\infty}(-1)^{n-1}/n^s=2\left(\dfrac{1}{2^s}+\dfrac{1}{4^s}+\cdots\right)=\dfrac{2}{2^s}\left(\dfrac{1}{1^s}+\dfrac{1}{2^s}+\cdots\right)=2^{1-s}\zeta(s)
$$
and the conclusion follows.

### 8.22

Given a convergent series $\sum a_n$, where each $a_n\ge0$. Prove that $\sum\sqrt{a_n}n^{-p}$ converges if $p>\frac{1}{2}$. Give a counterexample for $p=1/2$.

#### Proof

We have
$$
\sqrt{a_n}n^{-p}\le\frac{a_n+n^{-2p}}{2}=\frac{a_n}{2}+\frac{1}{2n^{2p}}\implies\sum\sqrt{a_n}n^{-p}\le\sum\frac{a_n}{2}+\sum\frac{1}{2n^{2p}}
$$
if $p>1/2$, then $\sum\dfrac{1}{2n^{2p}}$ is a convergent series, which means $\sum\sqrt{a_n}n^{-p}$ converges.



### 8.23

Given that $\sum a_n$ diverges. Prove that $\sum na_n$ also diverges.

#### Proof

Assume $\sum na_n$ converges to $S$, then the partial sums of $\sum na_n$ form a bounded sequence, since $\{1/n\}$ is a decreasing sequence which converges to $0$, use Dirichlet's test we have $\sum (na_n)\frac{1}{n}=\sum a_n$ converges, a contradiction.



### 8.24

Given that $\sum a_n$ converges, where each $a_n>0$. Prove that $\sum(a_na_{n+1})^{1/2}$ also converges. Show that the converse is also true if $\{a_n\}$ is monotonic.

#### Proof

We have
$$
(a_na_{n+1})^{1/2}\le\frac{a_n+a_{n+1}}{2}\implies\sum(a_na_{n+1})^{1/2}\le\sum\frac{a_n}{2}+\sum\frac{a_{n+1}}{2}
$$
so the series converges. Conversely, if $\sum(a_na_{n+1})^{1/2}$ converges and if $\{a_n\}$ is monotonic, then if $\{a_n\}$ is monotonic decreasing we have $\sqrt{a_na_{n+1}}\le\sqrt{a_na_n}=a_n\le\sqrt{a_{n-1}a_n}$, and if $\{a_n\}$ is monotonic increasing we have $\sqrt{a_na_{n-1}}\le\sqrt{a_na_n}=a_n\le\sqrt{a_{n+1}a_n}$, which shows $\sum a_n$ converges.

### 8.25

Given that $\sum a_n$ converges absolutely. Show that each of the following series also converges absolutely:

a) $\sum a_n^2$.

b) $\sum\dfrac{a_n}{1+a_n}$ if no $a_n=-1$.

c) $\sum\dfrac{a_n^2}{1+a_n^2}$.

#### Proof

(a) $a_n\to0$ as $n\to\infty$, thus $|a_n|<1$ for some $n\ge N$, so $\sum_{n=N}^{\infty}a_n^2=\sum_{n=N}^{\infty}|a_n||a_n|<\sum_{n=N}^{\infty}|a_n|$, which converges, and so $\sum a_n^2$ converges.

(b) $a_n\to0$ as $n\to\infty$, thus $|a_n|<1/2$ for some $n\ge N$, so
$$
\sum_{n=N}^{\infty}\left|\frac{a_n}{1+a_n}\right|=\sum_{n=N}^{\infty}\frac{|a_n|}{|1+a_n|}\le\sum_{n=N}^{\infty}\frac{|a_n|}{1-|a_n|}<\sum_{n=N}^{\infty}2|a_n|
$$
which converges, so the original series converges absolutely.

(c) From (a) we already have $\sum a_n^2$ converges absolutely, and the result follows from (b).

### 8.26

Determine all real values of $x$ for which the following series converges:
$$
\sum_{n=1}^{\infty}\left(1+\frac{1}{2}+\cdots+\frac{1}{n}\right)\frac{\sin{nx}}{n}.
$$

#### Solution

If $x=k\pi$ for integer $k$, the series converges to 0. If $x\ne k\pi$, use Theorem 8.30 we have
$$
\sum_{k=1}^n\cos{kx}+i\sum_{k=1}^n\sin{kx}=\sum_{k=1}^ne^{ikx}=\frac{\sin(nx/2)}{\sin(x/2)}e^{i(n+1)x/2}
$$
which implies
$$
\sum_{k=1}^n\sin{kx}=\frac{\sin(nx/2)}{\sin(x/2)}\sin\frac{(n+1)x}{2}\implies\sum_{k=1}^n\sin{kx}\le\frac{1}{|\sin(x/2)|}
$$
so the partial sums of the series $\sum\sin{nx}$ form a bounded sequence. Let
$$
b_n=\left(1+\frac{1}{2}+\cdots+\frac{1}{n}\right)\frac{1}{n}:=\frac{A_n}{n}
$$
then we have $A_n\ge1$ for all $n$ and
$$
b_{n+1}-b_n=\dfrac{A_{n+1}}{n+1}-\dfrac{A_{n}}{n}=\dfrac{nA_{n+1}-(n+1)A_n}{n(n+1)}=\dfrac{\frac{n}{n+1}-A_n}{n(n+1)}<0
$$
so $\{b_n\}$ is a decreasing sequence, we also have
$$
0<b_n=\frac{1}{n}\sum_{k=1}^n\frac{1}{k}\le\frac{1}{n^{1/2}}\sum_{k=1}^n\frac{1}{k\sqrt{n}}\le\frac{1}{n^{1/2}}\sum_{k=1}^n\frac{1}{k\sqrt{k}}\implies0\le\lim_{n\to\infty}b_n\le\lim_{n\to\infty}\frac{1}{n^{1/2}}\sum_{k=1}^{\infty}\frac{1}{k\sqrt{k}}=0
$$
thus the given series converges by Dirichlet's test.

### 8.27

Prove the following statements:

a) $\sum a_nb_n$ converges if $\sum a_n$ converges and if $\sum(b_n-b_{n+1})$ converges absolutely.

b) $\sum a_nb_n$ converges if $\sum a_n$ has bounded partial sums and if $\sum(b_n-b_{n+1})$ converges absolutely, provided that $b_n\to0$ as $n\to\infty$.

#### Proof

(a) Use the *partial summation formula* of Abel, we have $\sum_{k=1}^na_kb_k=A_nb_{n+1}-\sum_{k=1}^nA_k(b_{k+1}-b_k)$ where $A_n=a_1+\cdots+a_n$. Since $\sum a_n$ converges, we have $\lim_{n\to\infty}A_n$ exists and we can find an $M$ such that $|A_n|\le M$ for all $n$. By Theorem 8.10, $\sum(b_n-b_{n+1})$ converges absolutely means $\lim_{n\to\infty} b_n$ exists, thus the sequence $\{A_nb_{n+1}\}$ converges, and
$$
\sum_{k=1}^nA_k(b_{k+1}-b_k)\le M\sum_{k=1}^n|b_{k+1}-b_k|=M\sum_{k=1}^n|b_k-b_{k+1}|
$$
which means the series $\sum A_n(b_{n+1}-b_n)$ converges, use Theorem 8.27, we have $\sum a_nb_n$ converges.

(b) Use the *partial summation formula* of Abel, we have $\sum_{k=1}^na_kb_k=A_nb_{n+1}-\sum_{k=1}^nA_k(b_{k+1}-b_k)$ where $A_n=a_1+\cdots+a_n$. Since $\sum a_n$ has bounded partial sums, we can find an $M$ such that $|A_n|\le M$ for all $n$. So
$$
0\le|A_nb_{n+1}|\le M|b_{n+1}|\implies\lim_{n\to\infty}A_n b_{n+1}=0
$$
and
$$
\sum_{k=1}^nA_k(b_{k+1}-b_k)\le M\sum_{k=1}^n|b_{k+1}-b_k|=M\sum_{k=1}^n|b_k-b_{k+1}|
$$
which means the series $\sum A_n(b_{n+1}-b_n)$ converges, use Theorem 8.27, we have $\sum a_nb_n$ converges.