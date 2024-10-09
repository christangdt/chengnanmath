# Exercise 36-37

## Existence theorems for integral and differential equations

The following exercises illustrate how the fixed-point theorem for contractions (Theorem 4.48) is used to prove existence theorems for solutions of certain integral and differential equations. We denote by $C[a,b]$ the metric space of all real continuous functions on $[a,b]$ with the metric
$$
d(f,g)=\|f-g\|=\max_{a\le x\le b}|f(x)-g(x)|
$$
and recall that $C[a,b]$ is a complete metric space. (Exercise 4.67).

### 7.36

Given a function $g\in C[a,b]$, and a function $K$ continuous on the rectangle $Q=[a,b]\times[a,b]$, consider the function $T$ defined on $C[a,b]$ by the equation
$$
T(\varphi)(x)=g(x)+\lambda\int_a^bK(x,t)\varphi(t)dt,\quad\lambda\in\mathbf{R}
$$
a) Prove that $T$ maps $C[a,b]$ into itself.

b) If $|K(x,y)|\le M$ on $Q$, where $M>0$, and if $|\lambda|<M^{-1}(b-a)^{-1}$, prove that $T$ is a contraction of $C[a,b]$ and hence has a fixed point $\varphi$ which is a solution of the integral equation $\varphi(x)=g(x)+\lambda\int_a^bK(x,t)\varphi(t)dt$.

#### Proof

(a) Let $\varphi\in C[a,b]$, then to prove $T(\varphi)\in C[a,b]$ we only need to show $\int_a^bK(x,t)\varphi(t)dt$ is continuous on $[a,b]$. That $\varphi\in C[a,b]$ means $\varphi$ is bounded and we can find $G>0$ such that $|\varphi|\le G$ on $[a,b]$. That $K$ continuous on $Q$ means for $\forall\varepsilon>0$ there exists $\delta>0$ such that $|(x_1,y_1)-(x_2,y_2)|<\delta$ means $|K(x_1,y_1)-K(x_2,y_2)|<\varepsilon/(Gb-Ga)$, so when $|x-x'|<\delta$ we have
$$
\left|\int_a^bK(x,t)\varphi(t)dt-\int_a^bK(x',t)\varphi(t)dt\right|=\left|\int_a^b[K(x,t)-K(x',t)]\varphi(t)dt\right|\le\int_a^b\dfrac{\varepsilon}{G(b-a)}Gdt=\varepsilon
$$
this means $\int_a^bK(x,t)\varphi(t)dt$ is continuous on $[a,b]$.

(b) Let $\varphi,\phi\in C[a,b]$, then
$$
\begin{aligned}
\|T(\varphi)-T(\phi)\|&=\left\|\lambda\int_a^bK(x,t)[\varphi(t)-\phi(t)]dt\right\|=\max_{a\le x\le b}|\lambda|M\left|\int_a^b[\varphi(t)-\phi(t)]dt\right|
\\&\le|\lambda|M\int_a^b\|\varphi-\phi\|dt=|\lambda|M(b-a)\|\varphi-\phi\|<\|\varphi-\phi\|
\end{aligned}
$$
this means $T$ is a contraction of $C[a,b]$.

### 7.37

Assume $f$ is continuous on a rectangle $Q=[a-h,a+h]\times[b-k,b+k]$, where $h>0,k>0$.

a) Let $\varphi$ be a function, continuous on $[a-h,a+h]$, such that $(x,\varphi(x))\in Q$ for all $x\in[a-h,a+h]$. If $0<c\le h$, prove that $\varphi$ satisfies the differential equation $y'=f(x,y)$ on $(a-c,a+c)$ and the initial condition $\varphi(a)=b$ if and only if $\varphi$ satisfies the integral equation
$$
\varphi(x)=b+\int_a^xf(t,\varphi(t))dt\quad\text{on }(a-c,a+c)
$$
b) Assume that $|f(x,y)|\le M$ on $Q$ where $M>0$, and let $c=\min\{h,k/M\}$. Let $S$ denote the metric subspace of $C[a-c,a+c]$ consisting of all $\varphi$ such that $|\varphi(x)-b|\le Mc$ on $[a-c,a+c]$. Prove that $S$ is a closed subspace of $C[a-c,a+c]$ and hence that $S$ is itself a complete metric space.

c) Prove that the function $T$ defined on $S$ by the equation
$$
T(\varphi)(x)=b+\int_a^xf(t,\varphi(t))dt
$$
maps $S$ into itself.

d) Now assume that $f$ satisfies a Lipschitz condition of the form
$$
|f(x,y)-f(x,z)|\le A|y-z|
$$
for every pair of points $(x,y)$ and $(x,z)$ in $Q$, where $A>0$. Prove that $T$ is a contraction of $S$ if $h<1/A$. Deduce that for $h<1/A$ the differential equation $y'=f(x,y)$ has exactly one solution $y=\varphi(x)$ on $(a-c,a+c)$ such that $\varphi(a)=b$.

#### Proof

(a) If $\varphi$ satisfy $\varphi'=f(x,\varphi(x))$ and the initial condition $\varphi(a)=b$, then we have
$$
\int_a^x\varphi'(t)dt=\int_a^xf(t,\varphi(t))dt=\varphi(x)-\varphi(a)\implies\varphi(x)=b+\int_a^xf(t,\varphi(t))dt
$$
Conversely, if $\varphi(x)=b+\int_a^xf(t,\varphi(t))dt$ on $(a-c,a+c)$, then $\varphi(a)=b+\int_a^af(t,\varphi(t))dt=b$ and $\varphi'(x)=f(x,\varphi(x))$, thus it satisfy the given differential equation and the initial condition.

(b) Let $\phi\in S'$, then for $\varepsilon>0$ there is $\varphi\in S$ such that $\|\varphi-\phi\|<\varepsilon$, thus
$$
|\phi(x)-b|\le|\phi(x)-\varphi(x)|+|\varphi(x)-b|<\|\phi-\varphi\|+|\varphi(x)-b|<Mc+\varepsilon
$$
thus we get $|\phi(x)-b|\le Mc$ and $\phi\in S$.

(c) If $\varphi\in S$, then
$$
|T(\varphi)(x)-b|=\left|\int_a^xf(t,\varphi(t))dt\right|\le M\left|\int_a^xdt\right|=M|x-a|\le Mc,\quad x\in [c-a,c+a]
$$
thus we have $T(\varphi)\in S$.

(d) If $h<1/A$, then
$$
\begin{aligned}
\|T(\varphi)-T(\phi)\|&=\max_{x\in[a-h,a+h]}\left|\int_a^x[f(t,\varphi(t))-f(t,\phi(t))]dt\right|\le\max_{x\in[a-h,a+h]}\int_a^x|f(t,\varphi(t))-f(t,\phi(t))|dt
\\&\le\max_{x\in[a-h,a+h]}\int_a^xA|\varphi(t)-\phi(t)|dt\le Ah\|\varphi-\phi\|<\|\varphi-\phi\|
\end{aligned}
$$
so $T$ is a contraction of $S$, thus there is a unique $\varphi\in S$ such that $\varphi(x)=b+\int_a^xf(t,\varphi(t))dt$, the result follows from (a).