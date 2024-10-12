# Exercise 36-43

## Cesàro summability

### 8.36

Show that each of the following series has (C,1) sum $0$:

a) $1-1-1+1+1-1-1+1+1--++\cdots$.

b) $\frac{1}{2}-1+\frac{1}{2}+\frac{1}{2}-1+\frac{1}{2}+\frac{1}{2}-1++-\cdots$

c) $\cos{x}+\cos{3x}+\cos{5x}+\cdots$ ($x$ real, $x\ne m\pi$).

#### Solution

(a) $s_{4n+1}=1,s_{4n+2}=0,s_{4n+3}=-1,s_{4n}=0$, thus we can conclude $s_1+\cdots+s_n\in[-1,1]$, thus $\sigma_n\in[-1/n,1/n]$ and $S=\lim_{n\to\infty}\sigma_n=0$.

(b) We can conclude $s_1+\cdots+s_n\in[-1/2,1/2]$, thus $\sigma_n\in[-1/2n,1/2n]$ and $S=\lim_{n\to\infty}\sigma_n=0$.

(c) Let $s_n=\cos{x}+\cos{3x}+\cdots+\cos(2n-1)x$, then as $x\ne m\pi$, we have $\sin{x}\ne0$, use the equality
$$
\cos{x}+i\sin{x}=e^{ix}
$$
we have
$$
s_n=\Re(e^{ix}+e^{3ix}+\cdots+e^{(2n-1)ix})=\Re\left(\dfrac{e^{ix}-e^{(2n+1)ix}}{1-e^{2ix}}\right)
$$
then use DeMoivre's theorem (Exercise 1.44 in Chapter 1) we have
$$
\begin{aligned}
\dfrac{e^{ix}-e^{(2n+1)ix}}{1-e^{2ix}}&=\dfrac{(e^{ix}-e^{(2n+1)ix})(1-e^{-2ix})}{(1-e^{2ix})(1-e^{-2ix})}
\\&=\dfrac{e^{ix}-e^{-ix}-e^{(2n+1)ix}+e^{(2n-1)ix}}{2-e^{2ix}-e^{-2ix}}
\\&=\dfrac{-2i\sin{x}+\cos(2n-1)x+i\sin(2n-1)x-\cos(2n+1)x-i\sin(2n+1)x}{2-2\cos{2x}}
\end{aligned}
$$
thus
$$
s_n=\dfrac{\cos(2n-1)x-\cos(2n+1)x}{2-2\cos{2x}}=\dfrac{2\sin(2nx)\sin{x}}{4\sin^2{x}}=\dfrac{\sin(2nx)}{2\sin{x}}
$$
so
$$
\sigma_n=\dfrac{\sum_{k=1}^ns_k}{n}=\dfrac{\sum_{k=1}^n\sin(2kx)}{2n\sin{x}}=\dfrac{\Im(e^{2ix}+e^{4ix}+\cdots+e^{2nix})}{2n\sin{x}}
$$
use DeMoivre's theorem again we have
$$
\begin{aligned}
e^{2ix}+e^{4ix}+\cdots+e^{2nix}&=\dfrac{e^{2ix}-e^{(2n+2)ix}}{1-e^{2ix}}
\\&=\dfrac{(e^{2ix}-e^{(2n+2)ix})(1-e^{-2ix})}{(1-e^{2ix})(1-e^{-2ix})}
\\&=\dfrac{e^{2ix}-1-e^{(2n+2)ix}+e^{2nix}}{4\sin^2{x}}
\\
\implies\Im(e^{2ix}+e^{4ix}+\cdots+e^{2nix})&=\dfrac{\sin{2x}-\sin(2n+2)x+\sin(2nx)}{4\sin^2{x}}
\end{aligned}
$$
then we have
$$
\sigma_n=\dfrac{\sin{2x}-\sin(2n+2)x+\sin(2nx)}{8n\sin^3{x}}\implies|\sigma_n|\le\dfrac{3}{|8\sin^3{x}|n}
$$
and $S=\lim_{n\to\infty}\sigma_n=0$.

### 8.37

Given a series $\sum a_n$, let
$$
s_n=\sum_{k=1}^na_k,\quad t_n=\sum_{k=1}^nka_k,\quad \sigma_n=\frac{1}{n}\sum_{k=1}^ns_k.
$$
Prove that

a) $t_n=(n+1)s_n-n\sigma_n$.

b) If $\sum a_n$ is (C,1) summable, then $\sum a_n$ converges if and only if $t_n=o(n)$ as $n\to\infty$.

c) $\sum a_n$ is (C,1) summable if and only if $\sum_{n=1}^{\infty}t_n/n(n+1)$ converges.

#### Proof

(a) We have
$$
t_1=a_1=2a_1-a_1=(1+1)s_1-\sigma_1
$$
suppose $t_n=(n+1)s_n-n\sigma_n$, then
$$
\begin{aligned}
t_{n+1}&=\sum_{k=1}^{n+1}ka_k=t_n+(n+1)a_{n+1}=(n+1)s_n-n\sigma_n+(n+1)a_{n+1}
\\&=(n+1)\sum_{k=1}^na_k-\sum_{k=1}^ns_k+(n+1)a_{n+1}
\\&=(n+1)s_{n+1}-\sum_{k=1}^ns_k=(n+2)s_{n+1}-\sum_{k=1}^{n+1}s_k
\\&=(n+2)s_{n+1}-(n+1)\sigma_{n+1}
\end{aligned}
$$
(b) Suppose $\lim_{n\to\infty}\sigma_n=S$, use (a) we have
$$
\sigma_n=\dfrac{n+1}{n}s_n-\dfrac{t_n}{n}
$$
If $\sum a_n$ converges, then Theorem 8.48 tells that $\lim_{n\to\infty} s_n=S$, thus
$$
\lim_{n\to\infty}\dfrac{t_n}{n}=\lim_{n\to\infty}\left(\dfrac{n+1}{n}s_n-\sigma_n\right)=\lim_{n\to\infty}\dfrac{n+1}{n}\lim_{n\to\infty}s_n-\lim_{n\to\infty}\sigma_n=S-S=0
$$
which gives $t_n=o(n)$. Conversely if $t_n=o(n)$, then
$$
\lim_{n\to\infty}s_n=\lim_{n\to\infty}\dfrac{n}{n+1}\left(\sigma_n+\dfrac{t_n}{n}\right)=S
$$
and this means $\sum a_n$ converges.

(c) If $\sum_{n=1}^{\infty}t_n/n(n+1)$ converges, then $\dfrac{t_n}{n(n+1)}\to0$ as $n\to\infty$, thus $t_n=o(n)$, use the result of (b) and Theorem 8.48, we know that $\sum a_n$ converges and so is (C,1) summable. On the other hand, suppose $\sum a_n$ is (C,1) summable, we let  $\lim_{n\to\infty}\sigma_n=S$, use (a) we have
$$
\dfrac{t_n}{n(n+1)}=\dfrac{s_n}{n}-\dfrac{\sigma_n}{n+1}=\dfrac{n\sigma_n-(n-1)\sigma_{n-1}}{n}-\dfrac{\sigma_n}{n+1}=\dfrac{n}{n+1}\sigma_n-\dfrac{n-1}{n}\sigma_{n-1}
$$
let $b_n=\frac{n}{n+1}\sigma_n$, we have
$$
\sum_{n=1}^m\dfrac{t_n}{n(n+1)}=\sum_{n=1}^m(b_n-b_{n-1})=b_m-0=b_m\implies\sum_{n=1}^{\infty}\dfrac{t_n}{n(n+1)}=\lim_{m\to\infty}b_m=S
$$
thus  $\sum_{n=1}^{\infty}t_n/n(n+1)$ converges.

### 8.38

Given a monotonic sequence $\{a_n\}$ of positive terms, such that $\lim_{n\to\infty}a_n=0$. Let
$$
s_n=\sum_{k=1}^na_k,\quad u_n=\sum_{k=1}^n(-1)^ka_k,\quad v_n=\sum_{k=1}^n(-1)^ks_k.
$$
Prove that

a) $v_n=\frac{1}{2}u_n+(-1)^ns_n/2$.

b) $\sum_{n=1}^{\infty}(-1)^ns_n$ is (C,1) summable and has Cesàro sum $\frac{1}{2}\sum_{n=1}^{\infty}(-1)^na_n$.

c) $\sum_{n=1}^{\infty}(-1)^n(1+\frac{1}{2}+\cdots+1/n)=-\log\sqrt{2}\quad(C,1)$.

#### Proof

(a) First $v_1=-s_1=-a_1$ and $\frac{1}{2}u_1-s_1/2=-a_1$. Suppose the conclusion holds for $n$, then
$$
\begin{aligned}
v_{n+1}&=\sum_{k=1}^{n+1}(-1)^ks_k=v_n+(-1)^{n+1}s_{n+1}=\dfrac{1}{2}u_n+(-1)^n\dfrac{s_n}{2}+(-1)^{n+1}s_{n+1}
\\&=\dfrac{1}{2}\sum_{k=1}^n(-1)^ka_k+\dfrac{(-1)^n}{2}\sum_{k=1}^na_k+(-1)^{n+1}\sum_{k=1}^{n}a_k+(-1)^{n+1}a_{n+1}
\\&=\dfrac{1}{2}\sum_{k=1}^{n+1}(-1)^ka_k+\dfrac{1}{2}(-1)^{n+1}a_{n+1}+\dfrac{(-1)^{n+1}}{2}\sum_{k=1}^na_k
\\&=\dfrac{1}{2}u_{n+1}+\dfrac{(-1)^{n+1}}{2}s_{n+1}
\end{aligned}
$$
(b) $u_n$ is an alternating series, thus converges, by Theorem 8.48, it is (C,1) summable with the same convergent value. Notice that $\lim_{n\to\infty}a_n=0$ means $\lim_{n\to\infty}s_n/n=0$, thus
$$
\dfrac{v_n}{n}=\dfrac{u_n}{2n}+(-1)^n\dfrac{s_n}{2n}\implies\lim_{n\to\infty}\dfrac{v_n}{n}=0
$$
we write the partial Cesàro sum of the series $\sum_{n=1}^{\infty}(-1)^ns_n$ in the form as
$$
\dfrac{\sum_{k=1}^nv_k}{n}=\dfrac{\sum_{k=1}^nu_n}{2n}+\dfrac{\sum_{k=1}^n(-1)^ks_k}{2n}=\dfrac{1}{2}\dfrac{\sum_{k=1}^nu_n}{n}+\dfrac{v_n}{2n}
$$
let $n\to\infty$, the first part in the right of the equation is $1/2$ times the Cesàro sum of $u_n$, which is equal to $\frac{1}{2}\sum_{n=1}^{\infty}(-1)^na_n$, the second item becomes 0.

(c) Let $a_n=1/n$, use (b) and the result that $\sum_{n=1}^{\infty}(-1)^n(1/n)=-\log2$. This result can be shown use the Taylor expansion of $\log(1+x)$ at the point $x=0$, which is
$$
\log(1+x)=\sum_{n=1}^{\infty}(-1)^{n+1}\dfrac{x^n}{n}=-\sum_{n=1}^{\infty}(-1)^{n}\dfrac{x^n}{n}
$$
then let $x=1$.

## Infinite products

### 8.39

Determine whether or not the following infinite products converge. Find the value of each convergent product.
$$
\begin{aligned}
&\text{a)}\prod_{n=2}^{\infty}\left(1-\frac{2}{n(n+1)}\right),\quad&&\text{b)}\prod_{n=2}^{\infty}(1-n^{-2})
\\
&\text{c)}\prod_{n=2}^{\infty}\dfrac{n^3-1}{n^3+1},\quad&&\text{d)}\prod_{n=0}^{\infty}(1+z^{2^n})\quad\text{if }|z|<1.
\end{aligned}
$$

#### Solution

(a) Converge. We have
$$
1-\frac{2}{n(n+1)}=\frac{n^2+n-2}{n(n+1)}=\frac{(n+2)(n-1)}{n(n+1)}
$$
which means
$$
\prod_{n=2}^{m}\left(1-\frac{2}{n(n+1)}\right)=\dfrac{(m-1)!(m+2)!}{3\times m!(m+1)!}=\dfrac{m+2}{3m}\implies\prod_{n=2}^{\infty}\left(1-\frac{2}{n(n+1)}\right)=\dfrac{1}{3}
$$
(b) Converge.
$$
\prod_{n=2}^m(1-n^{-2})=\prod_{n=2}^m\dfrac{(n+1)(n-1)}{n^2}=\dfrac{(m-1)!(m+1)!}{2\times m!m!}=\dfrac{m+1}{2m}
\\
\implies\prod_{n=2}^{\infty}(1-n^{-2})=\dfrac{1}{2}
$$
(c) Converge.
$$
\begin{aligned}
\prod_{n=2}^{m}\dfrac{n^3-1}{n^3+1}&=\prod_{n=2}^{m}\dfrac{(n-1)(n^2+n+1)}{(n+1)(n^2-n+1)}=\prod_{n=2}^{m}\dfrac{(n-1)(n^2+n+1)}{(n+1)(n^2-2n+1+n-1+1)}
\\&=\prod_{n=2}^{m}\dfrac{(n-1)(n^2+n+1)}{(n+1)[(n-1)^2+(n-1)+1]}=\dfrac{2(m^2+m+1)}{(1^2+1+1)m(m+1)}
\end{aligned}
$$
thus
$$
\prod_{n=2}^{\infty}\dfrac{n^3-1}{n^3+1}=\lim_{m\to\infty}\dfrac{2(m^2+m+1)}{(1^2+1+1)m(m+1)}=\dfrac{2}{3}
$$
(d) Converge. We have
$$
(1+z^{2^n})=\dfrac{1-z^{2^{n+1}}}{1-z^{2^n}}\implies\prod_{n=0}^{m}(1+z^{2^n})=\dfrac{1-z^{2^{m+1}}}{1-z}\implies\prod_{n=0}^{\infty}(1+z^{2^n})=\dfrac{1}{1-z}
$$

### 8.40

If each partial sum $s_n$ of the convergent series $\sum a_n$ is not zero and if the sum itself is not zero, show that the infinite product $a_1\prod_{n=2}^{\infty}(1+a_n/s_{n-1})$ converges and has the value $\sum_{n=1}^{\infty}a_n$.

#### Proof

Let $\sum_{n=1}^{\infty}a_n=\lim_{n\to\infty}s_n=S$, notice that
$$
1+\dfrac{a_n}{s_{n-1}}=\dfrac{s_{n-1}+a_n}{s_{n-1}}=\dfrac{s_n}{s_{n-1}}
$$
we see that
$$
\prod_{n=2}^{m}(1+a_n/s_{n-1})=\dfrac{s_m}{s_1}=\dfrac{s_m}{a_1}\implies a_1\prod_{n=2}^{\infty}(1+a_n/s_{n-1})=\lim_{m\to\infty} s_m=S
$$

### 8.41

Find the values of the following products by establishing the following identities and summing the series:
$$
\text{a)}\prod_{n=2}^{\infty}\left(1+\frac{1}{2^n-2}\right)=2\sum_{n=1}^{\infty}2^{-n}.\qquad\text{b)}\prod_{n=2}^{\infty}\left(1+\dfrac{1}{n^2-1}\right)=2\sum_{n=1}^{\infty}\dfrac{1}{n(n+1)}.
$$


#### Solution

(a) Since
$$
1+\frac{1}{2^n-2}=\dfrac{2^n-1}{2^n-2}=\dfrac{2^n-1}{2(2^{n-1}-1)}
$$
which means
$$
\prod_{n=2}^{m}\left(1+\frac{1}{2^n-2}\right)=\dfrac{2^2-1}{2(2^{1}-1)}\dfrac{2^3-1}{2(2^{2}-1)}\cdots\dfrac{2^m-1}{2(2^{m-1}-1)}=\dfrac{2^m-1}{2^{m-1}}=2-\dfrac{1}{2^{m-1}}
$$
thus we can see the value of the product is $2$. To establish the identity, just expand $2^m-1$.

(b) We have
$$
1+\dfrac{1}{n^2-1}=\dfrac{n^2}{n^2-1}=\dfrac{nn}{(n-1)(n+1)}
\\
\implies\prod_{n=2}^{m}\left(1+\dfrac{1}{n^2-1}\right)=\dfrac{2m!m!}{(m-1)!(m+1)!}=\dfrac{2m}{m+1}
$$
thus we can see the value of the product is $2$. To establish the identity, notice that
$$
\dfrac{2n}{n+1}=2\left(1-\dfrac{1}{n+1}\right)=2\sum_{k=1}^n\dfrac{1}{k(k+1)}
$$

### 8.42

Determine all real $x$ for which the product $\prod_{n=1}^{\infty}\cos(x/2^n)$ converges and find the value of the product when it does converge.

#### Solution

Notice that if $x\ne k\pi$ for all integers $k$, we have
$$
\cos(x/2)\cos(x/2^2)\cdots\cos(x/2^n)=\dfrac{\sin{x}}{2^n\sin(x/2^n)}
$$
thus
$$
\prod_{n=1}^{\infty}\cos(x/2^n)=\lim_{n\to\infty}\dfrac{\sin{x}}{2^n\sin(x/2^n)}=\dfrac{\sin{x}}{x}\lim_{n\to\infty}\dfrac{x/2^n}{\sin(x/2^n)}=\dfrac{\sin{x}}{x}
$$
and the product converges.

If $x=0$, then the product converges to 1.

If $x=k\pi$ for some integer $k\ne0$, then the product shall converge, choose $N$ such that $x/2^N<\pi/2$, then for $n\ge N$, we have $\sin(x/2^n)\ne0$ and $\cos(x/2^n)\ne0$, we have
$$
\prod_{n=N}^{m}\cos(x/2^n)=\dfrac{\sin(x/2^{N-1})}{2^{m-N+1}\sin(x/2^{m})}\implies\prod_{n=N}^{\infty}\cos(x/2^n)=\dfrac{\sin(x/2^{N-1})}{2^{1-N}x}
$$
and so
$$
\prod_{n=1}^{\infty}\cos(x/2^n)=\cos(x/2)\cos(x/2^2)\cdots\cos(x/2^{N-1})\dfrac{\sin(x/2^{N-1})}{2^{1-N}x}=\dfrac{\sin{x}}{x}
$$

### 8.43

a) Let $a_n=(-1)^n/\sqrt{n}$ for $n=1,2,\dots$ Show that $\prod(1+a_n)$ diverges but that $\sum a_n$ converges.

b) Let $a_{2n-1}=-1/\sqrt{n}$ and $a_{2n}=1/\sqrt{n}+1/n$ for $n=1,2,\dots$ Show that $\prod(1+a_n)$ converges but that $\sum a_n$ diverges.

#### Proof

(a) That $\sum a_n$ converges can be seen by $a_n$ being an alternating series and $1/\sqrt{n}\to0$ as $n\to\infty$.  Since
$$
\left(1-\dfrac{1}{\sqrt{2n-1}}\right)\left(1+\dfrac{1}{\sqrt{2n}}\right)\le\left(1-\dfrac{1}{\sqrt{2n}}\right)\left(1+\dfrac{1}{\sqrt{2n}}\right)=1-\dfrac{1}{2n}
\\
\left(1-\dfrac{1}{\sqrt{2n-1}}\right)\left(1+\dfrac{1}{\sqrt{2n}}\right)\ge\left(1-\dfrac{1}{\sqrt{2n-1}}\right)\left(1+\dfrac{1}{\sqrt{2n-1}}\right)=1-\dfrac{1}{2n-1}
$$
we have
$$
\begin{aligned}
\prod_{k=2}^{2n}(1+a_k)&=\prod_{k=2}^{2n}\left(1+\dfrac{(-1)^k}{\sqrt{k}}\right)
\\&=\left(1+\dfrac{1}{\sqrt{2}}\right)\left(1-\dfrac{1}{\sqrt{3}}\right)\left(1+\dfrac{1}{\sqrt{4}}\right)\cdots\left(1-\dfrac{1}{\sqrt{2n-1}}\right)\left(1+\dfrac{1}{\sqrt{2n}}\right)
\\&\le\left(1+\dfrac{1}{\sqrt{2}}\right)\left(1-\dfrac{1}{4}\right)\cdots\left(1-\dfrac{1}{2n}\right)
\end{aligned}
$$
and similarly
$$
\prod_{k=2}^{2n-1}(1+a_k)\ge\left(1+\dfrac{1}{\sqrt{2}}\right)\left(1-\dfrac{1}{3}\right)\cdots\left(1-\dfrac{1}{2n-1}\right)
$$
by the divergence of the series $\sum\frac{1}{2k}$, we see that the product $\prod(1-\frac{1}{2n})$ and $\prod(1-\frac{1}{2n-1})$ diverges, in particular, as $n\to\infty$, the products are positive and monotonic decreasing, thus they must diverge to zero, this means $\prod(1+a_n)=0$ and diverges.

(b) We have
$$
\sum a_n =\sum_n(-1)^n/\sqrt{n}+\sum_n\dfrac{1}{n}
$$
the first series converges and the second diverges, thus $\sum a_n$ diverges. Since
$$
(1+a_{2n-1})(1+a_{2n})=\left(1-\dfrac{1}{\sqrt{n}}\right)\left(1+\dfrac{1}{\sqrt{n}}+\dfrac{1}{n}\right)=1-\dfrac{1}{n}+\dfrac{1}{n}-\dfrac{1}{n\sqrt{n}}
$$
we have
$$
\prod_{k=2}^{2n}(1+a_k)=(1+a_2)\left(1-\dfrac{1}{2\sqrt{2}}\right)\cdots\left(1-\dfrac{1}{n\sqrt{n}}\right)
\\
\prod_{k=2}^{2n+1}(1+a_k)=(1+a_2)\left(1-\dfrac{1}{2\sqrt{2}}\right)\cdots\left(1-\dfrac{1}{n\sqrt{n}}\right)\left(1-\dfrac{1}{\sqrt{n+1}}\right)
$$
Since the series $\sum\frac{1}{n\sqrt{n}}$ converges, the product $\prod(1-\frac{1}{n\sqrt{n}})$ converges, thus $\lim_{n\to\infty}\prod_{k=2}^{2n}(1+a_k)$ exists, since
$$
\lim_{n\to\infty}\prod_{k=2}^{2n+1}(1+a_k)=\left(\lim_{n\to\infty}\prod_{k=2}^{2n}(1+a_k)\right)\lim_{n\to\infty}\left(1-\dfrac{1}{\sqrt{n+1}}\right)=\lim_{n\to\infty}\prod_{k=2}^{2n}(1+a_k)
$$
we see the series $\prod(1+a_n)$ converges.
