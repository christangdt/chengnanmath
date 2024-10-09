# Exercise 18-35 (Riemann Integrals)

### 7.18

Assume $f\in R$ on $[a.b]$. Use Exercise 7.4 to prove that the limit
$$
\lim_{n\to\infty}\dfrac{b-a}{n}\sum_{k=1}^nf\left(a+k\dfrac{b-a}{n}\right)
$$
exist and has the value $\int_a^bf(x)dx$. Deduce that
$$
\lim_{n\to\infty}\sum_{k=1}^n\dfrac{n}{k^2+n^2}=\dfrac{\pi}{4},\quad\lim_{n\to\infty}\sum_{k=1}^n(n^2+k^2)^{-1/2}=\log(1+\sqrt{2}).
$$

#### Proof

If $f\in R$, use Exercise 7.4 we know that for $\forall\varepsilon>0$, there exists $\delta>0$ such that for any partition $P$ with $\|P\|<\delta$, we have $|S(P,f)-\int_a^bf(x)dx|<\varepsilon$. Let $N$ be an integer such that $N>(b-a)/\delta$, then if $n>N$, the partition
$$
P_n=\{a,a+\frac{b-a}{n},\dots,a+\frac{n-1}{n}(b-a),b\}
$$
has norm $\|P_n\|<\delta$, choose $t_k=x_{x+1}$ we have
$$
\left|\dfrac{b-a}{n}\sum_{k=1}^nf\left(a+k\dfrac{b-a}{n}\right)-\int_a^bf(x)dx\right|=\left|S(P_n,f)-\int_a^bf(x)dx\right|<\varepsilon
$$
and the conclusion follows.

Next, we have
$$
\lim_{n\to\infty}\sum_{k=1}^n\dfrac{n}{k^2+n^2}=\lim_{n\to\infty}\dfrac{1}{n}\sum_{k=1}^n\dfrac{1}{1+\frac{k^2}{n^2}}=\int_0^1\dfrac{1}{1+x^2}dx=\arctan{x}|_0^1=\dfrac{\pi}{4},
\\
\begin{aligned}\lim_{n\to\infty}\sum_{k=1}^n(n^2+k^2)^{-1/2}&=\lim_{n\to\infty}\dfrac{1}{n}\sum_{k=1}^n\dfrac{1}{\sqrt{1+\dfrac{k^2}{n^2}}}=\int_0^1\dfrac{1}{\sqrt{1+x^2}}dx\\&=\log|x+\sqrt{1+x^2}|\bigg|_0^1=\log(1+\sqrt{2})
\end{aligned}
$$

### 7.19

Define
$$
f(x)=\left(\int_0^xe^{-t^2}dt\right)^2,\quad g(x)=\int_0^1\frac{e^{-x^2(t^2+1)}}{t^2+1}dt.
$$
a) Show that $g'(x)+f'(x)=0$ for all $x$ and deduce that $g(x)+f(x)=\pi/4$.

b) Use (a) to prove that
$$
\lim_{x\to\infty}\int_0^xe^{-t^2}dt=\dfrac{1}{2}\sqrt{\pi}.
$$

#### Proof

(a) We have
$$
f'(x)=2e^{-x^2}\left(\int_0^xe^{-t^2}dt\right),\quad\forall x\in R
$$
if $x=0$, we have $f(0)=f'(0)=0$ and $g(0)=\arctan1=\pi/4$. Let
$$
h(t,x)=\frac{e^{-x^2(t^2+1)}}{t^2+1}
$$
then $D_2h=-2xe^{-x^2(t^2+1)}$ is continuous on $[0,1]\times[0,a]$ for any $a>0$, use Theorem 7.40, the derivative $g'(x)$ exists for each $x\in[0,a]$ and
$$
g'(x)=\int_0^1-2xe^{-x^2(t^2+1)}dt=-2e^{-x^2}\int_0^1e^{-x^2t^2}d(xt)=-2e^{-x^2}\int_0^xe^{-y^2}dy
$$
thus $g'(x)+f'(x)=0$ for all $x$, which means $g(x)+f(x)$ is constant for all $x$, and we have $g(0)+f(0)=\pi/4$.

(b) When $t\in[0,1]$, we have
$$
0<h(t,x)<e^{-x^2(t^2+1)}<e^{-x^2}\implies 0<g(x)=\int_0^1h(t,x)dt<e^{-x^2}
$$
if $x\to\infty$, we have $e^{-x^2}\to0$, thus $\lim_{x\to\infty}g(x)=0$, which means $\lim_{x\to\infty}f(x)=\pi/4$, and the conclusion follows.

### 7.20

Assume $g\in R$ on $[a,b]$ and define $f(x)=\int_a^xg(t)dt$ if $x\in[a,b]$. Prove that the integral $\int_a^x|g(t)|dt$ gives the total variation of $f$ on $[a,x]$.

#### Proof

Let $\varepsilon>0$, from $g\in R$ on $[a,b]$ we know $|g|\in R$ on $[a,b]$ by Theorem 7.21. So there exists a partition $P_1=\{a=x_0,x_1,\dots,x_n=x\}$ such that $L(P_1,|g|)>\int_a^x|g(t)|dt-\varepsilon$. For this $P_1$, use Mean Value Theorem we have
$$
\sum_{k=1}^n|f(x_k)-f(x_{k-1})|=\sum_{k=1}^n\left|\int_{x_{k-1}}^{x_k}g(t)dt\right|=\sum_{k=1}^n|c_k(x_k-x_{k-1})|,\quad |c_k|\ge\inf_{x\in[x_{k-1},x_k]}|g(x)|
$$
so we have
$$
\sum_{k=1}^n|f(x_k)-f(x_{k-1})|=\sum_{k=1}^n|c_k||(x_k-x_{k-1})|\ge L(P_1,|g|)>\int_a^x|g(t)|dt-\varepsilon
$$
thus $V_f(a,x)\ge\int_a^x|g(t)|dt$.

On the other hand, there exists a partition $P_2\in\mathscr{P}[a,x]$ such that $U(P_2,g)<\int_a^x|g(t)|dt+\varepsilon$, and there exists a partition $P_3=\{a=y_0,y_1,\dots,y_m=x\}$ such that
$$
V_f(a,x)-\varepsilon<\sum_{k=1}^m|f(y_k)-f(y_{k-1})|
$$
If we let $P=P_2\cup P_3$, with the notation $P=\{a=t_0,t_1,\dots,t_p=x\}$, then $U(P,g)\le U(P_2,g)$ and
$$
\sum_{k=1}^m|f(y_k)-f(y_{k-1})|\le\sum_{k=1}^p|f(t_k)-f(t_{k-1})|=\sum_{k=1}^p\left|\int_{t_{k-1}}^{t_k}g(t)dt\right|=\sum_{k=1}^n|c_k(t_k-t_{k-1})|
$$
with $|c_k|\le\sup_{x\in[x_{k-1},x_k]}|g(x)|$, thus we can have
$$
V_f(a,x)-\varepsilon<\sum_{k=1}^n|c_k(t_k-t_{k-1})|\le U(P,|g|)\le U(P_2,g)<\int_a^x|g(t)|dt+\varepsilon
$$
thus $V_f(a,x)\le\int_a^x|g(t)|dt$.

### 7.21

Let $\mathbf{f}=(f_1,\dots,f_n)$ be a vector-valued function with a continuous derivative $\mathbf{f}'$ on $[a,b]$. Prove that the curve described by $\mathbf{f}$ has length
$$
\Lambda_{\mathbf{f}}(a,b)=\int_a^b\|\mathbf{f}'(t)\|dt.
$$

#### Proof

 Let $\varepsilon>0$. Each $f_i$ is continuous differentiable on $[a,b]$, so $f_i\in R[a,b]$ for $i=1,\dots,n$, so we have
$$
\|\mathbf{f}'(t)\|=\sqrt{\sum_{i=1}^n[f_i'(t)]^2}
$$
is continuous on $[a,b]$, thus uniformly continuous, then $\|\mathbf{f}'(t)\|\in R[a,b]$ and we can find $\delta>0$ such that whenever $x,y\in [a,b],|x-y|<\delta$, we have $|\|\mathbf{f}'(x)\|-\|\mathbf{f}'(y)\||<\varepsilon/(b-a)$. From $\|\mathbf{f}'(t)\|\in R[a,b]$ we can find a partition $P_{\varepsilon}$ of $[a,b]$ such that if $P_1=\{x_0,x_1,\dots,x_m\}$ is a partition finer than $P_{\varepsilon}$, then
$$
\left|\sum_{k=1}^m\|\mathbf{f}'(t_k)\|(x_k-x_{k-1})-\int_a^b\|\mathbf{f}'(t)\|dt\right|<\varepsilon,\quad t_k\in[x_{k-1},x_k]
$$
By definition of $\Lambda_{\mathbf{f}}(a,b)$, there exists a partition $P_2$ such that $\Lambda_{\mathbf{f}}(a,b)-\varepsilon<\Lambda_{\mathbf{f}}(P_2)\le\Lambda_{\mathbf{f}}(a,b)$. Let $P=\{s_0,s_1,\dots,s_p\}$ be a partition finer than $P_1\cup P_2$ with $\|P\|<\delta$, then  $\Lambda_{\mathbf{f}}(a,b)-\varepsilon<\Lambda_{\mathbf{f}}(P)\le\Lambda_{\mathbf{f}}(a,b)$ still holds and
$$
\begin{aligned}
\Lambda_{\mathbf{f}}(P)&=\sum_{k=1}^p\|\mathbf{f}(s_k)-\mathbf{f}(s_{k-1})\|=\sum_{k=1}^p\sqrt{\sum_{i=1}^n[f_i(s_k)-f_i(s_{k-1})]^2}
\\&=\sum_{k=1}^p\sqrt{\sum_{i=1}^n[f'_i(\xi_k)]^2(s_k-s_{k-1})^2}=\sum_{k=1}^p\left(\sqrt{\sum_{i=1}^n[f'_i(\xi_k)]^2}\right)(s_k-s_{k-1})
\\&=\sum_{k=1}^p\|\mathbf{f}'(\xi_k)\|(s_k-s_{k-1}),\quad \xi_k\in[s_{k-1},s_k]
\end{aligned}
$$

while the last equality comes from the Mean Value Theorem. We also have
$$
\left|\sum_{k=1}^p\|\mathbf{f}'(t_k)\|(s_k-s_{k-1})-\int_a^b\|\mathbf{f}'(t)\|dt\right|<\varepsilon,\quad t_k\in[s_{k-1},s_k]
$$
thus
$$
\begin{aligned}
\left|\Lambda_{\mathbf{f}}(a,b)-\int_a^b\|\mathbf{f}'(t)\|dt\right|&\le|\Lambda_{\mathbf{f}}(a,b)-\Lambda_{\mathbf{f}}(P)|+\left|\Lambda_{\mathbf{f}}(P)-\int_a^b\|\mathbf{f}'(t)\|dt\right|
\\&\le\varepsilon+\left|\Lambda_{\mathbf{f}}(P)-\sum_{k=1}^p\|\mathbf{f}'(t_k)\|(s_k-s_{k-1})\right|+\left|\sum_{k=1}^p\|\mathbf{f}'(t_k)\|(s_k-s_{k-1})-\int_a^b\|\mathbf{f}'(t)\|dt\right|
\\&=2\varepsilon+\left|\sum_{k=1}^p\|\mathbf{f}'(\xi_k)\|(s_k-s_{k-1})-\sum_{k=1}^p\|\mathbf{f}'(t_k)\|(s_k-s_{k-1})\right|
\\&=2\varepsilon+\sum_{k=1}^p\left|\|\mathbf{f}'(\xi_k)\|-\|\mathbf{f}'(t_k)\|\right|(s_k-s_{k-1})
\\&<2\varepsilon+\dfrac{\varepsilon}{b-a}\sum_{k=1}^p(s_k-s_{k-1})=3\varepsilon
\end{aligned}
$$
the conclusion follows since $\varepsilon$ is arbitrarily chosen.

### 7.22

If $f^{(n+1)}$ is continuous on $[a,x]$, define
$$
I_n(x)=\dfrac{1}{n!}\int_a^x(x-t)^nf^{(n+1)}(t)dt.
$$
a) Show that
$$
I_{k-1}(x)-I_k(x)=\dfrac{f^{(k)}(a)(x-a)^k}{k!},\quad k=1,2,\dots,n.
$$
b) Use (a) to express the remainder in Taylor's formula (Theorem 5.19) as an integral.

#### Proof

(a) For $k\ge1$ we have
$$
\begin{aligned}
I_k(x)&=\dfrac{1}{k!}\int_a^x(x-t)^kf^{(k+1)}(t)dt=\dfrac{1}{k!}\int_a^x(x-t)^kd[f^{(k)}(t)]
\\&=-\dfrac{1}{k!}(x-a)^kf^{(k)}(a)-\dfrac{1}{k!}\int_a^xf^{(k)}(t)d(x-t)^k
\\&=\dfrac{1}{(k-1)!}\int_a^x(x-t)^{k-1}f^{(k)}(t)dt-\dfrac{f^{(k)}(a)(x-a)^k}{k!}
\end{aligned}
$$
thus the equality holds.

(b) Theorem 5.19 says for $x\in[a,b],x\ne c$ there exists $x_1$ between $x$ and $c$ such that
$$
f(x)=f(c)+\sum_{k=1}^{n-1}\dfrac{f^{(k)}(c)}{k!}(x-c)^k+\dfrac{f^{(n)}(x_1)}{n!}(x-c)^n
$$
thus the remainder can be expressed as
$$
\begin{aligned}
\dfrac{f^{(n)}(x_1)}{n!}(x-c)^n&=f(x)-f(c)-\sum_{k=1}^{n-1}\dfrac{f^{(k)}(c)}{k!}(x-c)^k\\&=f(x)-f(c)-\sum_{k=1}^{n-1}[I_{k-1}(x)-I_k(x)]
\\&=f(x)-f(c)-I_0+I_{n-1}\\&=f(x)-f(c)-\int_c^xf'(t)dt+I_{n-1}
\\&=I_{n-1}=\dfrac{1}{(n-1)!}\int_c^x(x-t)^{n-1}f^{(n)}(t)dt
\end{aligned}
$$

### 7.23

Let $f$ be continuous on $[0,a]$. If $x\in[0,a]$, define $f_0(x)=f(x)$ and let
$$
f_{n+1}(x)=\dfrac{1}{n!}\int_0^x(x-t)^nf(t)dt,\quad n=0,1,2\dots
$$
Show that the $n$th derivative of $f_n$ exists and equals $f$.

#### Proof

The conclusion obviously holds when $n=0$. And $f_1(x)=\int_0^xf(t)dt$ means $(f_1)'=f(x)$. For $n\ge2$ we have
$$
(n-1)!f_n(x)=\int_0^x(x-t)^{n-1}f(t)dt=\sum_{k=0}^{n-1}\dfrac{(-1)^k(n-1)!}{k!(n-1-k)!}x^{n-1-k}\int_0^xt^kf(t)dt
$$
which means
$$
\begin{aligned}
f_n'(x)&=\left(\sum_{k=0}^{n-1}\left[\dfrac{(-1)^kx^{n-1-k}}{k!(n-1-k)!}\int_0^xt^kf(t)dt\right]\right)'=\sum_{k=0}^{n-1}\left[\dfrac{(-1)^kx^{n-1-k}}{k!(n-1-k)!}\int_0^xt^kf(t)dt\right]'
\\&=\sum_{k=0}^{n-2}\dfrac{(-1)^kx^{n-2-k}}{k!(n-2-k)!}\int_0^xt^kf(t)dt+\sum_{k=0}^{n-1}\dfrac{(-1)^kx^{n-1-k}}{k!(n-1-k)!}x^kf(x)
\\&=\dfrac{1}{(n-2)!}\int_0^x(x-t)^{n-2}f(t)dt+\sum_{k=0}^{n-1}\dfrac{(-1)^kx^{n-1}}{k!(n-1-k)!}f(x)
\\&=f_{n-1}(x)+\dfrac{x^{n-1}f(x)}{(n-1)!}\sum_{k=0}^{n-1}\dfrac{(n-1)!}{k!(n-1-k)!}(-1)^k1^{n-1-k}
\\&=f_{n-1}(x)+\dfrac{x^{n-1}f(x)}{(n-1)!}(-1+1)^{n-1}=f_{n-1}(x)
\end{aligned}
$$
thus $(f_n)^{(n)}=(f_{n-1})^{(n-1)}=\cdots=(f_1)'=f$.

### 7.24

Let $f$ be a positive continuous function in $[a,b]$. Let $M$ denote the maximum value of $f$ on $[a,b]$. Show that
$$
\lim_{n\to\infty}\left(\int_a^bf(x)^ndx\right)^{1/n}=M.
$$

#### Proof

First we have $0<f(x)\le M$ on $[a,b]$, thus
$$
\begin{aligned}
0<f(x)^n\le M^n&\implies\int_a^bf(x)^ndx\le\int_a^bM^ndx=M^n(b-a)\\&\implies\left(\int_a^bf(x)^ndx\right)^{1/n}\le M(b-a)^{1/n}
\end{aligned}
$$
Next for $\forall\varepsilon>0$, since $f$ is continuous on $[a,b]$, $f$ attains $M$ at some point in $[a,b]$, thus there exists $[c,d]\subset[a,b]$ with $d>c$ such that
$$
f(x)\ge M-\varepsilon,\quad x\in[c,d]
$$
choose $\varepsilon$ small enough such that $M-\varepsilon>0$, we can have
$$
\int_a^bf(x)^ndx\ge\int_c^df(x)^ndx\ge\int_c^d(M-\varepsilon)^ndx=(M-\varepsilon)^n(d-c)\\\implies\left(\int_a^bf(x)^ndx\right)^{1/n}\ge(M-\varepsilon)(d-c)^{1/n}
$$
thus
$$
M-\varepsilon=\lim_{n\to\infty}(M-\varepsilon)(d-c)^{1/n}\le\lim_{n\to\infty}\left(\int_a^bf(x)^ndx\right)^{1/n}\le\lim_{n\to\infty}M(b-a)^{1/n}=M
$$
and the conclusion follows.

### 7.25

A function $f$ of two real variables is defined for each point $(x,y)$ in the unit square $0\le x\le1,0\le y\le1$ as follows:
$$
f(x,y)=\begin{cases}1,\quad&x\in\mathbf{Q}\\2y,\quad&x\notin\mathbf{Q}\end{cases}
$$
a) Compute $\bar{\int}_0^1f(x,y)dx$ and $\underline{\int}_0^1f(x,y)dx$ in terms of $y$.

b) Show that $\int_0^1f(x,y)dy$ exists for each fixed $x$ and compute $\int_0^tf(x,y)dy$ in terms of $x$ and $t$ for $0\le x\le1,0\le t\le1$.

c) Let $F(x)=\int_0^1f(x,y)dy$. Show that $\int_0^1F(x)dx$ exists and find its value.

#### Proof

(a) Given a partition $P=\{0=x_0,x_1,\dots,x_n=1\}$, we have
$$
\min_{x\in[x_{k-1},x_k]}f(x,y)=\begin{cases}
2y,\quad&0\le y<1/2
\\
1,\quad& y\ge1/2
\end{cases},\qquad\max_{x\in[x_{k-1},x_k]}f(x,y)=\begin{cases}
1,\quad&0\le y<1/2
\\
2y,\quad& y\ge1/2
\end{cases}
$$
thus
$$
\bar{\int}_0^1f(x,y)dx=\begin{cases}
1,\quad&0\le y<1/2
\\
2y,\quad& y\ge1/2
\end{cases},\qquad\underline{\int}_0^1f(x,y)dx=\begin{cases}
2y,\quad&0\le y<1/2
\\
1,\quad& y\ge1/2
\end{cases}
$$
(b) If $x$ is fixed, then either $x\in\mathbf{Q}$ or not, thus
$$
\int_0^1f(x,y)dy=\begin{cases}
\int_0^11dy=1,\quad&x\in\mathbf{Q}
\\
\int_0^12ydy=1,\quad&x\notin\mathbf{Q}
\end{cases}
$$
which means $\int_0^1f(x,y)dy=1$. For $0\le x\le1,0\le t\le1$, we have
$$
\int_0^tf(x,y)dy=\int_0^tdy=t,\quad x\in\mathbf{Q}
\\
\int_0^tf(x,y)dy=\int_0^t2ydy=t^2,\quad x\notin\mathbf{Q}
$$
(c) Since $F(x)=\int_0^1f(x,y)dy=1$ for $x\in[0,1]$, we have
$$
\int_0^1F(x)dx=\int_0^11dx=1
$$

### 7.26

Let $f$ be defined on $[0,1]$ as follows: $f(0)=0$; if $2^{-n-1}<x\le2^{-n}$, then $f(x)=2^{-n}$ for $n=0,1,2,\dots$

a) Give two reasons why $\int_0^1f(x)dx$ exists.

b) Let $F(x)=\int_0^xf(t)dt$. Show that for $0<x\le1$ we have $F(x)=xA(x)-\frac{1}{3}A(x)^2$, where $A(x)=2^{-[-\log{x}/\log2]}$ and where $[y]$ is the greatest integer in $y$.

#### Proof

(a) Reason 1: $f$ is of bounded variation, since $f$ is monotonic increasing and $f(x)\in[0,1]$ for $x\in[0,1]$. By Theorem 7.28, $\int_0^1f(x)dx$ exists.

Reason 2: The set of discontinuities of $f$ on $[0,1]$ is the set $D=\{1/2,1/2^2,\dots\}$, which is countable, for $\forall\varepsilon>0$, we can cover each point $1/2^k$ with the interval $(1/2^k-\varepsilon,1/2^k+\varepsilon)$, so $1/2^k$ has measure zero, and $D$ has measure zero by Theorem 7.44, and $\int_0^1f(x)dx$ exists by Theorem 7.48.

(b) For any fixed $0<x\le1$, we can find a unique $n\ge0$ such that $2^{-n-1}<x\le2^{-n}$, which means
$$
(-n-1)\log2<\log{x}\le-n\log2\implies n\le-\dfrac{\log{x}}{\log2}<n+1\implies n=[-\log{x}/\log2]
$$
Thus $A(x)=2^{-n}$. If $k>n$, then $f(t)=2^{-k}$ for $2^{-k-1}<x\le2^{-k}$, thus we have
$$
\begin{aligned}
F(x)&=\int_0^xf(t)dt=\int_0^{2^{-n-1}}f(t)dt+\int_{2^{-n-1}}^xf(t)dt=\sum_{k=n+1}^{+\infty}\int_{2^{-k-1}}^{2^{-k}}2^{-k}dt+\int_{2^{-n-1}}^x2^{-n}dt
\\&=\sum_{k=n+1}^{+\infty}2^{-k}\left(\dfrac{1}{2^k}-\dfrac{1}{2^{k+1}}\right)+\dfrac{1}{2^n}(x-2^{-n-1})
\\&=\sum_{k=n+1}^{+\infty}\dfrac{1}{2^{2k+1}}+\dfrac{x}{2^n}-\dfrac{1}{2^{2n+1}}=xA(x)+\dfrac{1}{2^{2n+3}}\sum_{m=0}^{\infty}\dfrac{1}{4^m}-\dfrac{1}{2^{2n+1}}
\\&=xA(x)+\dfrac{1}{2^{2n+3}}\dfrac{4}{3}-\dfrac{1}{2^{2n+1}}=xA(x)-\dfrac{1}{2^{2n}}\left(\dfrac{1}{2}-\dfrac{1}{6}\right)=xA(x)-\dfrac{1}{3}A(x)^2
\end{aligned}
$$

### 7.27

Assume $f$ has a derivative which is *continuous* and monotonic decreasing and satisfies $f'(x)\ge m>0$ for all $x\in[a,b]$. Prove that
$$
\left|\int_a^b\cos{f(x)dx}\right|\le\dfrac{2}{m}.
$$

#### Proof

Let $g(x)=f'(x)\cos f(x)$, since the function $1/f'(x)$ is increasing and positive on $[a,b]$, we let $B=1/f'(b)$ and use Theorem 7.37(ii) to have
$$
\int_a^b\cos{f(x)}dx=\int_a^bg(x)\dfrac{1}{f'(x)}dx=\dfrac{1}{f'(b)}\int_{x_0}^bg(x)dx=\dfrac{1}{f'(b)}\int_{x_0}^bd\sin{f(x)}=\dfrac{\sin{f(b)}-\sin{f(x_0)}}{f'(b)},\quad x_0\in[a,b]
$$
since $f'(b)\ge m$, we have
$$
\left|\int_a^b\cos{f(x)}dx\right|\le\dfrac{|\sin{f(b)}-\sin{f(x_0)}|}{m}\le\dfrac{2}{m}
$$

### 7.28

Given a decreasing sequence of real numbers $\{G(n)\}$ such that $G(n)\to0$ as $n\to\infty$. Define a function $f$ on $[0,1]$ in terms of $\{G(n)\}$ as follows: $f(0)=1$; if $x$ is irrational then $f(x)=0$; if $x$ is the rational $m/n$ (in lowest terms), then $f(m/n)=G(n)$. Compute the oscillation $\omega_f(x)$ at each $x$ in $[0,1]$ and show that $f\in R$ on $[0,1]$.

#### Solution

If $x$ is irrational in $[0,1]$, for any $\varepsilon>0$ we can find $N$ such that $G(n)<\varepsilon$ whenever $n>N$, for each integer $k=1,\dots,N$ we can find $m_k$ such that
$$
\dfrac{m_k}{k}<x<\dfrac{m_k+1}{k},\quad k=1,\dots,N
$$
define
$$
h_k=\min\left(x-\dfrac{m_k}{k},\dfrac{m_k+1}{k}-x\right),\quad k=1,\dots,N\quad, h_0=\min(h_1,\dots,h_N)>0
$$
then if $h<h_0$, we can conclude that for any $y\in(x-h,x+h)$, either $y$ is irrational, or $y$ is a rational in the form $m/n$ with $n>N$, thus we have $0\le f(y)\le G(N+1)<\varepsilon$, which means $\Omega_f(B(x;h)\cap[0,1])<\varepsilon$ whenever $h<h_0$, thus $w_f(x)=0$.

If $x$ is rational in $[0,1]$, then we can write $x=M/N$ for some $N$, thus $f(x)=G(N)$, similar to the procedure above, we can find some $h>0$ such that for any $y\in(x-h,x+h)$, either $y$ is irrational, or $y$ is a rational in the form $m/n$ with $n>N$, which means $0\le f(y)\le G(N)$, so $\Omega_f(B(x;h)\cap[0,1])=G(N)$, and as $h\to 0+$, this value remains constant. So $\omega_f(x)=G(N)\ge0$.

Let $D$ be the set of discontinuities of $f$ on $[0,1]$, then $D\subseteq\mathbf{Q}\cap[0,1]$, thus $D$ is countable and has measure zero, by Theorem 7.48 we have $f\in R$.

### 7.29

Let $f$ be defined as in Exercise 7.28 with $G(n)=1/n$. Let $g(x)=1$ if $0<x\le1$, $g(0)=0$. Show that the composite function $h$ defined by $h(x)=g[f(x)]$ is not Riemann-integrable on $[0,1]$, although both $f\in R$ and $g\in R$ on $[0,1]$.

#### Proof

We have $0<f(x)\le1$ if $x\in\mathbf{Q}$, and $f(x)=0$ if $x\notin\mathbf{Q}$, thus $h(x)=1$ if $x\in\mathbf{Q}$ and $h(x)=0$ if $x\notin\mathbf{Q}$, for any partition $P=\{x_0,\dots,x_n\}$ of $[0,1]$, we have
$$
U(P,h)=\sum_{k=1}^nM_k(h)(x_k-x_{k-1})=\sum_{k=1}^n1(x_k-x_{k-1})=x_n-x_0=1,\\L(P,h)=\sum_{k=1}^nm_k(h)(x_k-x_{k-1})=\sum_{k=1}^n0(x_k-x_{k-1})=0
$$
thus $h$ does not satisfy Riemann's condition on $[0,1]$.

### 7.30

Use Lebesgue's theorem to prove Theorem 7.49.

#### Proof

Let $D$ denote the set of discontinuities of $f$ in $[a,b]$ and $D_g$ denote the set of discontinuities of $g$ in $[a,b]$.

(a) If $f$ is of bounded variation on $[a,b]$, then $f=f_1-f_2$ where $f_1,f_2$ are both monotonic increasing, by Theorem 6.2, $D$ is countable, thus has measure zero.

(b) Let $D'$ denote the set of discontinuities of $f$ in $[c,d]\subseteq[a,b]$, then $D'\subset D$, that $f\in R$ on $[a,b]$ means $D$ has measure zero, so $D'$ has measure zero, so $f\in R$ on $[c,d]$.

(c) We have $D$ and $D_g$ both have measure zero, if $D''$ is the discontinuities of $f/g$ on $[a,b]$ if $g$ is bounded away from zero, then $D''\subset D\cup D_g$, which shows $D''$ has measure zero.

(d) In this case we have $D=D_g$, thus $D$ has measure zero if and only if $D_g$ has measure zero.

(e) If $g$ is continuous at $x\in[a,b]$, then $h$ is continuous at $x$, thus the set of discontinuities of $h$ is a subset of $D_g$, which has measure zero.

### 7.31

Use Lebesgue's theorem to prove that if $f\in R$ and $g\in R$ on $[a,b]$ and if $f(x)\ge m>0$ for all $x\in[a,b]$, then the function $h$ defined by $h(x)=f(x)^{g(x)}$ is Riemann-integrable on $[a,b]$.

#### Proof

Let $D_f$ denote the set of discontinuities of $f$ in $[a,b]$, and $D_g,D_h$ similarly defined. From $h(x)=f(x)^{g(x)}$ we have $\log{h(x)}=g(x)\log{f(x)}$, thus $D_{\log{h}}\subseteq D_g\cup D_{\log{f}}$. Let $y(x)=\log{h(x)}$, then if $h$ is continuous at $x$, then $y$ is continuous at $x$, since $y=\log{h}$ means $h(x)=e^{y(x)}$, we see if $y$ is continuous at $x$, then $h$ is continuous at $x$, we can conclude $D_h=D_{\log{h}}$, similarly $D_f=D\log{f}$. Now $f\in R$ and $g\in R$ means $D_f$ and $D_g$ has measure zero, so $D_{\log{f}}$ has measure zero, so $D_h=D_{\log{h}}$ has measure zero, which means $h\in R$ on $[a,b]$.

### 7.32

Let $I=[0,1]$ and let $A_1=I-(\frac{1}{3},\frac{2}{3})$ be that subset of $I$ obtained by removing those points which lie in the middle third of $I$; that is, $A_1=[0,\frac{1}{3}]\cup[\frac{2}{3},1]$. Let $A_2$ be that subset of $A_1$ obtained by removing the open middle third of $[0,\frac{1}{3}]$ and of $[\frac{2}{3},1]$. Continue this process and define $A_3,A_4,\dots$ The set $C=\cap_{n=1}^{\infty}A_n$ is called the *Cantor set*. Prove that:

a) $C$ is a compact set having measure zero.

b) $x\in C$ if and only if $x=\sum_{n=1}^{\infty}a_n3^{-n}$, where each $a_n$ is either $0$ or $2$.

c) $C$ is uncountable.

d) Let $f(x)=1$ if $x\in C$, $f(x)=0$ if $x\notin C$. Prove that $f\in R$ on $[0,1]$.

#### Proof

(a) $C$ is bounded since $C\subseteq[0,1]$, and $C=R-A$ where $A=(-\infty,0)\cup(1,+\infty)\cup(\frac{1}{3},\frac{2}{3})\cup\cdots$, notice $A$ is a countable union of open sets, thus is open, so $C$ is closed. Hence $C$ is compact. Let $\forall\varepsilon>0$, since we need $\varepsilon$ to be small, we can suppose $\varepsilon<1/6$,let $B_i=A_i-A_{i+1}$, thus $B_1=(\frac{1}{3},\frac{2}{3})$, $B_2=(\frac{1}{9},\frac{2}{9})\cup(\frac{7}{9},\frac{8}{9})$, and $B_3,B_4$ can be found similarly. Each $B_i$ has length $\|B_i\|=2^{i-1}/3^i$ and has $2^i$ end points. Let $S_i$ be obtained from $B_i$ by subtract $\varepsilon/2^{2i}$ at each end point, which means
$$
S_1=\left(\dfrac{1}{3}+\dfrac{\varepsilon}{4},\dfrac{2}{3}-\dfrac{\varepsilon}{4}\right),S_2=\left(\frac{1}{9}+\dfrac{\varepsilon}{16},\frac{2}{9}-\dfrac{\varepsilon}{16}\right)\cup\left(\frac{7}{9}+\dfrac{\varepsilon}{16},\frac{8}{9}-\dfrac{\varepsilon}{16}\right),\dots
$$
each $S_i$ has length $2^{i-1}/3^i-\varepsilon/2^i$, and $S_i\cap S_j=\empty$ for any $i\ne j$, let $S=[0,1]-\bigcup_{i=1}^{\infty}S_i$, then we have $C\subseteq S$ since $S_i\subseteq B_i$ for all $i$, the length of $S$ is
$$
\|S\|=1-\sum_{i=1}^{\infty}\left(\dfrac{2^{i-1}}{3^i}-\dfrac{\varepsilon}{2^i}\right)=1-\dfrac{1}{3}\sum_{i=0}^{\infty}\left(\dfrac{2}{3}\right)^i+\sum_{i=1}^{\infty}\dfrac{\varepsilon}{2^i}=\varepsilon
$$
thus $C$ has measure zero.

(b) First suppose $x\in C$, then $x\in A_n$ for $n=1,2,\dots$. we have
$$
x\in A_1\implies x=\dfrac{0}{3}+x_1\text{ or }x=\dfrac{2}{3}+x_1,x_1\in\left[0,\dfrac{1}{3}\right]
\\
x\in A_2\implies x_1=\dfrac{0}{3^2}+x_2\text{ or }x_1=\dfrac{2}{3^2}+x_2,x_2\in\left[0,\dfrac{1}{3^2}\right]
\\
\cdots
\\
x\in A_n\implies x_{n-1}=\dfrac{0}{3^n}+x_n\text{ or }x_{n-1}=\dfrac{2}{3^n}+x_n,\quad x_n\in\left[0,\dfrac{1}{3^n}\right]
\\
\cdots
$$
thus $x=\sum_{n=1}^{\infty}a_n3^{-n}$, where each $a_n$ is either $0$ or $2$. Conversely, if $x$ has the form given , let $x_k=\sum_{n=k+1}^{\infty}a_n3^{-n}$, we have
$$
0=\sum_{n=k+1}^{\infty}0(3^{-n})\le x_k\le\sum_{n=k+1}^{\infty}2(3^{-n})=\dfrac{1}{3^k}
$$
from $x_1\in[0,1/3]$ we have $x\in A_1$, from $x_2\in[0,1/3^2]$ we have $x\in A_2$, similarly we have $x\in A_k$ for all $k$, thus $x\in C$.

(c) Assume $C$ is countable, then $C=\{c_1,c_2,\dots\}$ where each $c_i=\sum_{n=1}^{\infty}a_{i,n}3^{-n}$, where each $a_{i,n}$ is either $0$ or $2$. Form a number $c$ as follows: define
$$
b_n=\begin{cases}1,\quad&a_{n,n}=0\\0,\quad&a_{n,n}=1\end{cases}
$$
and let $c=\sum_{n=1}^{\infty}b_n3^{-n}$, since $b_n$ is either $0$ or $2$ for each $n$, use (b) we have $c\in C$, but we have $b\ne c_i$ for all $i=1,2,\dots$.

(d) The set of discontinuities of $f$ is $C$, which has measure zero.

### 7.33

This exercise outlines a proof (due to Ivan Niven) that $\pi^2$ is irrational. Let $f(x)=x^n(1-x)^n/n!$. Prove that

a) $0<f(x)<1/n!$ if $0<x<1$.

b) Each $k$th derivative $f^{(k)}(0)$ and $f^{(k)}(1)$ is an integer.

Now assume that $\pi^2=a/b$, where $a$ and $b$ are positive integers, and let
$$
F(x)=b^n\sum_{k=0}^n(-1)^kf^{(2k)}(x)\pi^{2n-2k}
$$
Prove that:

c) $F(0)$ and $F(1)$ are integers.

d) $\pi^2a^nf(x)\sin\pi{x}=\dfrac{d}{dx}\{F'(x)\sin\pi{x}-\pi F(x)\cos\pi{x}\}$.

e) $F(1)+F(0)=\pi a^n\int_0^1f(x)\sin\pi{x}dx$.

f) Use (a) in (e) to deduce that $0<F(1)+F(0)<1$ if $n$ is sufficiently large. This contradicts (c) and shows that $\pi^2$ (and hence $\pi$) is irrational.

#### Proof

(a) If $0<x<1$, then $0<1-x<1$, thus $0<x^n(1-x)^n<1$ for all integer $n$, so $0<f(x)<1/n!$.

(b) Let $A_n(x)=x^n(1-x)^n/n!$ and $p(x)=1-2x$, we have $A_n'(x)=A_{n-1}(x)p(x)$ and $p'(x)=c$ which is an integer. Also $A_n(0)=A_n(1)=0$ for positive integers $n$, $p(0)$ and $p(1)$ are integers. Now we have
$$
f^{(1)}=A_{n-1}p
\\
f^{(2)}=A_{n-2}p^2+cA_{n-1}
\\
f^{(3)}=A_{n-3}p^3+2cpA_{n-2}+cA_{n-2}p=A_{n-3}p^3+c_3A_{n-2}p,\quad c_3\in\mathbf{Z}
\\
f^{(4)}=A_{n-4}p^4+3cp^2A_{n-3}+c_3cA_{n-2}+c_3A_{n-3}p^2=A_{n-4}p^4+c_{4,1}A_{n-3}p^2+c_{4,2}A_{n-2}
$$
continue this process, we see $f^{(k)}$ is a linear combination of $A_j$ and $p^i$ for several $j,i$ with coefficients all integers, notice that when $j=0$, we will have $A_j=1$ which vanishes to a constant. and $p''=1$, we can see that $f^{(k)}(0)$ and $f^{(k)}(1)$ are integers for all $k$.

(c) Use (b) we see that $f^{(2k)}(0)$ and $f^{(2k)}(1)$ are integers, and for $k=0,\dots,n$ we have
$$
\pi^{2n-2k}b^n=\dfrac{a^{n-k}}{b^{n-k}}b^n=a^{n-k}b^k\in\mathbf{Z}
$$
this shows $F(0)$ and $F(1)$ are integers.

(d) We have $F'(x)=b^n\sum_{k=0}^n(-1)^kf^{(2k+1)}(x)\pi^{2n-2k}$, thus
$$
\begin{aligned}
&\quad\dfrac{d}{dx}\{F'(x)\sin\pi{x}-\pi F(x)\cos\pi{x}\}\\&=F''(x)\sin\pi{x}+\pi F'(x)\cos\pi{x}-\pi F'(x)\cos\pi{x}+\pi^2F(x)\sin\pi{x}
\\&=[F''(x)+\pi^2F(x)]\sin\pi{x}
\\&=(\sin\pi{x})b^n\left[\sum_{k=0}^n(-1)^kf^{(2k+2)}(x)\pi^{2n-2k}+\sum_{k=0}^n(-1)^kf^{(2k)}(x)\pi^{2n-2k+2}\right]
\\&=(\sin\pi{x})b^n\left(\sum_{k=0}^{n-1}(-1)^kf^{(2k+2)}(x)\pi^{2n-2k}+(-1)^nf^{(2n+2)}(x)+f(x)\pi^2+\sum_{k=1}^n(-1)^kf^{(2k)}(x)\pi^{2n-2k+2}\right)
\\&=(\sin\pi{x})b^n\left((-1)^nf^{(2n+2)}(x)+f(x)\pi^2+\sum_{k=1}^n(-1)^{k-1}f^{(2k)}(x)\pi^{2n-2k+2}+\sum_{k=1}^n(-1)^kf^{(2k)}(x)\pi^{2n-2k+2}\right)
\\&=(\sin\pi{x})b^n\left((-1)^nf^{(2n+2)}(x)+f(x)\pi^2\right)
\end{aligned}
$$
since $f$ is a polynomial of degree $2n$, we have $f^{(2n+2)}(x)=0$.

(e) We have
$$
\pi^2 a^n\int_0^1f(x)\sin\pi{x}dx=F'(x)\sin\pi{x}-\pi F(x)\cos\pi{x}|_0^1=\pi(F(1)+F(0))
$$
(f) Since $\lim_{n\to\infty}a^n/n!=0$ for positive integer $a$, for sufficiently large $n$ we have
$$
0<F(1)+F(0)=\pi a^n\int_0^1f(x)\sin\pi(x)dx\le\pi a^n\int_0^1f(x)dx<\dfrac{\pi a^n}{n!}<1
$$

### 7.34

Given a real-valued function $\alpha$, continuous on the interval $[a,b]$ and having a finite bounded derivative $\alpha'$ on $(a,b)$. Let $f$ be defined and bounded on $[a,b]$ and assume that both integrals
$$
\int_a^bf(x)d\alpha(x),\qquad\int_a^bf(x)\alpha'(x)dx
$$
exist. Prove that these integrals are equal. (It is not assumed that $\alpha'$ is continuous).

#### Proof

Since both integrals exist, for every $\varepsilon>0$, there exists a partition $P_{\varepsilon}$ such that for any partition $P$ finer than $P_{\varepsilon}$ and every choice of $t_k\in[x_{k-1},x_k]$, we have $|S(P,f,\alpha)-\int_a^bf(x)d\alpha(x)|<\varepsilon/2$, there exists a partition $P_{\varepsilon}'$ such that for any partition $P$ finer than $P_{\varepsilon}'$ and every choice of $t_k\in[x_{k-1},x_k]$, we have $|S(P,f\alpha')-\int_a^bf(x)\alpha'(x)dx|<\varepsilon/2$. Let $P=P_{\varepsilon}\cup P_{\varepsilon}'$, write $P=\{x_0=a,x_1,\dots,x_n=b\}$, consider $\alpha(x_k)-\alpha(x_{k-1})$, use Mean Value Theorem we know there exists $\xi_k\in(x_{k-1},x_k)$ such that
$$
\alpha(x_k)-\alpha(x_{k-1})=\alpha'(\xi_k)(x_k-x_{k-1})
$$
since $P$ is finer than $P_{\varepsilon}'$ and $\xi_k\in(x_{k-1},x_k)$, we have
$$
\left|\sum_{k=1}^nf(\xi_k)\alpha'(\xi_k)(x_k-x_{k-1})-\int_0^1f(x)\alpha'(x)dx\right|<\dfrac{\varepsilon}{2}
$$
since $P$ is finer than $P_{\varepsilon}$ and $\xi_k\in(x_{k-1},x_k)$, we have
$$
\left|\sum_{k=1}^nf(\xi_k)[\alpha(x_k)-\alpha(x_{k-1})]-\int_0^1f(x)d\alpha(x)\right|<\dfrac{\varepsilon}{2}
$$
thus we have
$$
\left|\int_0^1f(x)d\alpha(x)-\int_0^1f(x)\alpha'(x)dx\right|<\varepsilon
$$

### 7.35

Prove the following theorem, which implies that a function with a positive integral must itself be positive on some interval. Assume that $f\in R$ on $[a,b]$ and that $0\le f(x)\le M$ on $[a,b]$ where $M>0$. Let $I=\int_a^bf(x)dx$, let $h=\frac{1}{2}I/(M+b-a)$ and assume that $I>0$. Then the set $T=\{x:f(x)\ge h\}$ contains a finite number of intervals, the sum of whose length is at least $h$.

#### Proof

Let $P$ be a partition of $[a,b]$ such that every Riemann sum $S(P,f)=\sum_{k=1}^nf(t_k)\Delta x_k$ which satisfy $S(P,f)>I/2$, Split $S(P,f)$ into two parts, $S(P,f)=\sum_{k\in A}+\sum_{k\in B}$, where $A=\{k:[x_{k-1},x_k]\subseteq T\}$ and $B=\{k:k\notin A\}$. So for every $k\in B$, we can choose some $t_k$ such that $f(t_k)<h$. Assume $\sum_{k\in A}\Delta x_k\le h$, then we have
$$
\begin{aligned}
\dfrac{I}{2}<S(P,f)&=\sum_{k\in A}f(t_k)\Delta x_k+\sum_{k\in B}f(t_k)\Delta x_k\le M\sum_{k\in A}\Delta x_k+h\sum_{k\in B}\Delta x_k
\\&\le Mh+h\sum_{k\in B}\Delta x_k\le Mh+h(b-a)=h(M+b-a)
\end{aligned}
$$
divide the positive number $M+b-a$ on both side of the inequality, we get $h<h$, which is a contradiction. 