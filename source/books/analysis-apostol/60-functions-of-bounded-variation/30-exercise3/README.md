# Exercise 11-13 (Absolutely continuous functions)

A real-valued function $f$ defined on $[a,b]$ is said to be *absolutely continuous* on $[a,b]$ if for every $\varepsilon>0$ there is a $\delta>0$ such that
$$
\sum_{k=1}^n|f(b_k)-f(a_k)|<\varepsilon
$$
for every $n$ disjoint open subintervals $(a_k,b_k)$ of $[a,b]$, $n=1,2,\dots$, the sum of whose length $\sum_{k=1}^n(b_k-a_k)$ is less than $\delta$.

Absolutely continuous functions occur in the Lebesgue theory of integration and differentiation. The following exercises give some of their elementary properties.

### 6.11

Prove that every absolutely continuous function on $[a,b]$ is continuous and of bounded variation on $[a,b]$.

#### Proof

Let $f$ be an absolutely continuous function on $[a,b]$. For every $\varepsilon>0$, there is a $\delta>0$ which satisfy the conditions of absolutely continuous, then whenever $x,y\in[a,b]$ with $|x-y|<\delta$, we let $a_1=\min(x,y)$ and $b_1=\max(x,y)$, and will have $\sum_{k=1}^1(b_1-a_1)<\delta$, thus $\sum_{k=1}^1|f(b_1)-f(a_1)|=|f(x)-f(y)|<\varepsilon$, so $f$ is uniformly continuous on $[a,b]$, thus continuous on $[a,b]$.

Let $\delta_1$ be the number which satisfy the conditions of absolutely continuous for $\varepsilon=1$, since $\delta>0$, we can find a number $N$ such that $a+N\delta_1\le b$ and $a+(N+1/2)\delta_1>b$. Let $P_1=\{a,a+\delta_1/2,\dots,a+N\delta_1,b\}$, for any $P\in\mathscr{P}[a,b]$, consider $P\cup P_1$, suppose there are points $x_1,\dots,x_n\in P$ such that $a<x_i<a+\delta_1/2$ for $i=1,\dots,n$, let $a=x_0,a+\delta_1=x_{n+1}$, then the subintervals $(x_i,x_{i+1})$ with $i=0,\dots,n$ satisfy $\sum_{i=0}^n(x_{i+1}-x_i)=\delta_1/2<\delta_1$, so $\sum_{i=0}^n|f(x_{i+1})-f(x_i)|<1$. We can prove a similar result for points of $P\cup P_1$ which lie in the interval $[a+k\delta_1/2,a+(k+1)\delta_1/2]$ for $k=1,\dots,2N$, so we have
$$
\sum(P)\le\sum(P\cup P_1)\le(2N+1)\implies V_f(a,b)\le2N+1
$$
this shows $f$ is of bounded variation.

### 6.12

Prove that $f$ is absolutely continuous if it satisfies a uniform Lipschitz condition of
order $1$ on $[a,b]$.

#### Proof

Let $\varepsilon>0$, for every $n$ disjoint open subintervals $(a_k,b_k)$ of $[a,b]$, $n=1,2,\dots$, we have
$$
|f(b_k)-f(a_k)|<M|b_k-a_k|
$$
for some $M>0$. So let $\delta=\varepsilon/M$, if $\sum_{k=1}^n(b_k-a_k)<\delta$, we have
$$
\sum_{k=1}^n|f(b_k)-f(a_k)|<\sum_{k=1}^nM|b_k-a_k|=M\sum_{k=1}^n(b_k-a_k)<M\delta=\varepsilon
$$

### 6.13

If $f$ and $g$ are absolutely continuous on $[a,b]$, prove that each of the following is also: $|f|$, $cf$ ($c$ constant), $f+g$, $f\cdot g$; also $f/g$ if $g$ is bounded away from zero.

#### Proof

For $|f|$, we can prove from $\big||f(b_k)|-|f(a_k)|\big|\le|f(b_k)-f(a_k)|$.

For $cf$, we choose $\delta$ such that $\sum_{k=1}^n|f(b_k)-f(a_k)|<\varepsilon/|c|$ if $c\ne0$, and the case $c=0$ is obviously true.

For $f+g$, choose $\delta$ such that
$$
\sum_{k=1}^n|f(b_k)-f(a_k)|<\dfrac{\varepsilon}{2},\quad\sum_{k=1}^n|g(b_k)-g(a_k)|<\dfrac{\varepsilon}{2}
$$
For $fg$, since $f$ and $g$ are continuous on $[a,b]$, they are bounded, choose $M$ such that $|f|<M$ and $|g|<M$ on $[a,b]$, and choose $\delta$ such that 
$$
\sum_{k=1}^n|f(b_k)-f(a_k)|<\dfrac{\varepsilon}{2M},\quad\sum_{k=1}^n|g(b_k)-g(a_k)|<\dfrac{\varepsilon}{2M}
$$
For $f/g$, we can find $m$ such that $|g|\ge m>0$ on $[a,b]$, choose $\delta$ such that 
$$
\quad\sum_{k=1}^n|g(b_k)-g(a_k)|<\dfrac{\varepsilon}{M^2}
$$
then $1/g$ is absolutely continuous on $[a,b]$, and then use $f/g=f\cdot (1/g)$.