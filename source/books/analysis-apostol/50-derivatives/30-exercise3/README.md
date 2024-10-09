# Exercise 30-34 (Vector-valued functions, Partial derivatives)

## Vector-valued functions

### 5.30

If a vector-valued function $\mathbf{f}$ is differentiable at $c$, prove that
$$
\mathbf{f}'(c)=\lim_{h\to 0}\dfrac{1}{h}[\mathbf{f}(c+h)-\mathbf{f}(c)].
$$
Conversely, if this limit exists, prove that $\mathbf{f}$ is differentiable at $c$.

#### Proof

We write $\mathbf{f}=(f_1,\dots,f_n)$, use addition and multiplication for vectors, we can have
$$
\begin{aligned}
\mathbf{f}'(c)&=(f_1'(c),\dots,f_n'(c))
\\&=\left(\lim_{h\to0}\dfrac{f_1(c+h)-f_1(c)}{h},\cdots,\lim_{h\to0}\dfrac{f_n(c+h)-f_n(c)}{h}
\right)
\\&=\lim_{h\to0}\dfrac{1}{h}\left(f_1(c+h),\dots,f_n(c+h)\right)-\lim_{h\to0}\dfrac{1}{h}\left(f_1(c),\dots,f_n(c)\right)
\\&=\lim_{h\to0}\dfrac{1}{h}[\mathbf{f}(c+h)-\mathbf{f}(c)]
\end{aligned}
$$
Conversely, if the limit exists and has value $A$, then $A$ is a vector which can be written as $A=(A_1,\dots,A_n)$, this means for $h$ sufficiently close to $0$, we have
$$
\left|\dfrac{\mathbf{f}(c+h)-\mathbf{f}(c)}{h}-A\right|<\varepsilon
$$
and for each $k=1,\dots,n$ we have
$$
\left|\dfrac{f_k(c+h)-f_k(c)}{h}-A_k\right|\le\left|\dfrac{\mathbf{f}(c+h)-\mathbf{f}(c)}{h}-A\right|
$$
this shows that $f'_k(c)$ exists for each $k$, thus $\mathbf{f}$ is differentiable at $c$.

### 5.31

A vector-valued function $\mathbf{f}$ is differentiable at each point of $(a, b)$ and has constant
norm $\|\mathbf{f}\|$. Prove that $\mathbf{f}(t)\cdot\mathbf{f}'(t)=0$ on $(a,b)$.

#### Proof

Write $\mathbf{f}=(f_1,\dots,f_n)$, then $\mathbf{f}$ is differentiable on $(a,b)$ means each $f_k$ is continuous and differentiable on $(a,b)$. Thus for $t\in(a,b)$, use differentiable at $t$ we have
$$
\begin{aligned}\mathbf{f}(t)\cdot\mathbf{f}'(t)&=\sum_{k=1}^nf_k(t)f'_k(t)=\sum_{k=1}^n\left(f_k(t)\lim_{x\to t}\dfrac{f_k(x)-f_k(t)}{x-t}\right)\\&=\lim_{x\to t}\sum_{k=1}^n\left(\dfrac{f_k(x)-f_k(t)}{x-t}f_k(t)\right)
\end{aligned}
$$
further use continuous at $t$ we have
$$
\begin{aligned}\mathbf{f}(t)\cdot\mathbf{f}'(t)&=\lim_{x\to t}\sum_{k=1}^n\left(\dfrac{f_k(x)-f_k(t)}{x-t}f_k(x)\right)
\end{aligned}
$$
so we can have
$$
\begin{aligned}\mathbf{f}(t)\cdot\mathbf{f}'(t)&=\dfrac{1}{2}\mathbf{f}(t)\cdot\mathbf{f}'(t)+\dfrac{1}{2}\mathbf{f}(t)\cdot\mathbf{f}'(t)
\\&=\dfrac{1}{2}\lim_{x\to t}\sum_{k=1}^n\left(\dfrac{f_k(x)-f_k(t)}{x-t}f_k(t)\right)+\dfrac{1}{2}\lim_{x\to t}\sum_{k=1}^n\left(\dfrac{f_k(x)-f_k(t)}{x-t}f_k(x)\right)
\\&=\dfrac{1}{2}\lim_{x\to t}\sum_{k=1}^n\left(\dfrac{(f_k(x)-f_k(t))(f_k(x)+f_k(t))}{x-t}\right)
\\&=\dfrac{1}{2}\lim_{x\to t}\sum_{k=1}^n\left(\dfrac{f_k^2(x)-f_k^2(t)}{x-t}\right)=\dfrac{1}{2}\lim_{x\to t}\dfrac{\sum_{k=1}^n[f_k^2(x)-f_k^2(t)]}{x-t}
\end{aligned}
$$
the function has constant norm $\|\mathbf{f}\|$ means $\|\mathbf{f}(t)\|=\|\mathbf{f}(x)\|$, or $\sum_{k=1}^n[f_k^2(x)-f_k^2(t)]=0$, and the conclusion follows.

### 5.32

A vector-valued function $\mathbf{f}$ is never zero and has a derivative $\mathbf{f}'$ which exists and is continuous on $\mathbf{R}$. If there is a real function $\lambda$ such that $\mathbf{f}'(t)=\lambda(t)\mathbf{f}(t)$ for all $t$, prove
that there is a positive real function $u$ and a constant vector $\mathbf{c}$ such that $\mathbf{f}(t)=u(t)\mathbf{c}$ for all $t$.  

#### Proof

Let $v(t)=\int_0^t\lambda(x)dx$, then $v'(t)=\lambda(t)$, write $\mathbf{f}=(f_1,\dots,f_n)$, then from $\mathbf{f}'(t)=\lambda(t)\mathbf{f}(t)$ we get $f'_k(t)=\lambda(t)f_k(t)$ for $k=1,\dots,n$, thus
$$
\left(e^{-v(t)}f_k(t)\right)'=\left(e^{-v(t)}\right)'f_k(t)+e^{-v(t)}f'_k(t)=e^{-v(t)}\left(-\lambda(t)f_k(t)+f'_k(t)\right)=0
$$
which means $e^{-v(t)}f_k(t)=c_k$ for some constant $c_k\in\mathbf{R}$. Let $u(t)=e^{v(t)}>0$ and $\mathbf{c}=(c_1,\dots,c_n)$, we have
$$
u(t)\mathbf{c}=e^{v(t)}(e^{-v(t)}f_1(t),\dots,e^{-v(t)}f_n(t))=(f_1(t),\dots,f_n(t))=\mathbf{f}(t)
$$

## Partial derivatives

### 5.33

Consider the function $f$ defined on $\mathbf{R}^2$ by the following formulas:
$$
f(x,y)=\dfrac{xy}{x^2+y^2},\quad\text{if }(x,y)\neq(0,0)\quad f(0,0)=0.
$$
Prove that the partial derivatives $D_1f(x,y)$ and $D_2f(x,y)$ exist for every $(x,y)$ in $\mathbf{R}^2$ and evaluate these derivatives explicitly in terms of $x$ and $y$. Also, show that $f$ is not continuous at $(0,0)$.

#### Proof

When $(x,y)\neq(0,0)$, we have
$$
\begin{aligned}
D_1f(x,y)&=\lim_{t\to x}\dfrac{f(t,y)-f(x,y)}{t-x}=\lim_{t\to x}\dfrac{\dfrac{ty}{t^2+y^2}-\dfrac{xy}{t^2+y^2}}{t-x}
\\&=\lim_{t\to x}\dfrac{ty(x^2+y^2)-xy(t^2+y^2)}{(t-x)(t^2+y^2)(x^2+y^2)}=\lim_{t\to x}\dfrac{txy(x-t)+y^3(t-x)}{(t-x)(t^2+y^2)(x^2+y^2)}
\\&=\lim_{t\to x}\dfrac{y^3-txy}{(t^2+y^2)(x^2+y^2)}=\dfrac{y^3-x^2y}{(x^2+y^2)^2}
\end{aligned}
$$
Similarly, we can have $D_2f(x,y)=\dfrac{x^3-xy^2}{(x^2+y^2)^2}$. For the case $(x,y)=(0,0)$, we have
$$
D_1f(0,0)=\lim_{t\to0}\dfrac{f(t,0)-f(0,0)}{t-0}=0,\quad D_2f(0,0)=0
$$
thus $D_1f(x,y)$ and $D_2f(x,y)$ exists in $\mathbf{R}^2$.

To see $f$ is not continuous at $(0,0)$, notice that for any $\delta>0$, let $(x,y)=(\frac{\delta}{2},\frac{\delta}{2})$, then
$$
\|(x,y)-(0,0)\|=\sqrt{\delta}/{2},\quad|f(x,y)-f(0,0)|=1/2
$$

### 5.34

Let $f$ be defined on $\mathbf{R}^2$ as follows:
$$
f(x,y)=y\dfrac{x^2-y^2}{x^2+y^2},\quad\text{if }(x,y)\neq(0,0)\quad f(0,0)=0.
$$
Compute the first- and second-order partial derivatives of $f$ at the origin, when they exist.

#### Solution

For the first-order partial derivative we have
$$
D_1f(0,0)=\lim_{t\to0}\dfrac{f(t,0)-f(0,0)}{t-0}=\lim_{t\to0}\dfrac{0}{t}=0
\\
D_2f(0,0)=\lim_{t\to0}\dfrac{f(0,t)-f(0,0)}{t-0}=\lim_{t\to0}\dfrac{-t}{t}=-1
$$
For the second-order partial derivative, we first compute $D_1f(x,y)$ and $D_2f(x,y)$ when $(x,y)\neq (0,0)$, which are
$$
D_1f(x,y)=\dfrac{4xy^3}{(x^2+y^2)^2},\quad D_2f(x,y)=\dfrac{x^4-4x^2y^2-y^4}{(x^2+y^2)^2}
$$
thus
$$
D_{1,1}f(0,0)=\lim_{t\to0}\dfrac{D_1f(t,0)-D_1f(0,0)}{t-0}=\lim_{t\to0}\dfrac{0-0}{t}=0
\\
D_{1,2}f(0,0)=\lim_{t\to0}\dfrac{D_2f(t,0)-D_2f(0,0)}{t-0}=\lim_{t\to0}\dfrac{1-(-1)}{t}=\infty
\\D_{2,1}f(0,0)=\lim_{t\to0}\dfrac{D_1f(0,t)-D_1f(0,0)}{t-0}=\lim_{t\to0}\dfrac{0-0}{t}=0
\\
D_{2,2}f(0,0)=\lim_{t\to0}\dfrac{D_2f(0,t)-D_2f(0,0)}{t-0}=\lim_{t\to0}\dfrac{-1-(-1)}{t}=0
$$
