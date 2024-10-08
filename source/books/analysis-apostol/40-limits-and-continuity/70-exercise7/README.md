# Exercise 60-65 (Monotonic functions)

### 4.60

Let $f$ be defined in the open interval $(a, b)$ and assume that for each interior point $x$ of $(a, b)$ there exists a $1$-ball $B(x)$ in which $f$ is increasing. Prove that $f$ is an increasing function throughout $(a, b)$.  

#### Proof

Let $a<m<n<b$, then $[m,n]$ is compact, and for each $x\in[m,n]$ there is a $1$-ball $B(x)$ in which $f$ is increasing, thus we have $[m,n]\subseteq\{B(x):x\in[m,n]\}$, and thus a finite set of the balls can cover $[m,n]$, suppose we have $k$ balls $B(x_1),\dots,B(x_k)$ covering $[m,n]$, $B(x_i)$ has radius $r_i>0$, we can rearrange so that $x_1<\cdots<x_k$ and we can further suppose $B(x_i)\nsubseteq{B(x_j)}$ for any $i,j$, otherwise we can drop some balls from $B(x_1),\dots,B(x_k)$ and obtain a new set of balls still cover $[m,n]$.

Now if $m,n$ are covered in one ball $B(x_i)$, then $f(m)\le{f(n)}$ since $f$ is increasing in this ball. If $m,n$ are not covered in one ball, then we claim $m\in B(x_1)$ and $n\in B(x_k)$, assume $m\in B(x_i),i\neq 1$ but $m\notin B(x_1)$, then $m\le{x_1-r_1}$ and $x_i-r_i<m$, which means
$$
\begin{aligned}
x_i-r_i<m\le x_1-r_1<x_1+r_1&\le x_1+x_1-m
\\&<2x_i+r_i-x_i=x_i+r_i
\end{aligned}
$$
and then $B(x_1)\subseteq B(x_i)$, a contradiction. The proof of $n\in B(x_k)$ is similar.

Next we prove $B(x_i)\cap{B(x_{i+1})}\ne\empty$ for $i=1,\dots,k-1$. Assume $B(x_i)\cap{B(x_{i+1})}=\empty$ for some $i$, then there is a point $c\in(x_i,x_{i+1})$ not covered by $B(x_i)$ or $B(x_{i+1})$, thus must be covered by other balls. Suppose it is covered by $B(x_j)$ with $x_j<x_i$, we have the following inequalities:
$$
x_i+r_i\le{c}\le{x_{i+1}-r_{i+1}}\tag{*}
$$

$$
x_j-r_j<c<x_j+r_j\tag{**}
$$

combined we have
$$
\begin{aligned}
x_j-r_j&<x_j+x_j-c\quad(\text{by **})
\\&<2x_i-c
\\&\le 2x_i-x_i-r_i\quad(\text{by *})
\\&=x_i-r_i
\end{aligned}
$$
thus $x_j-r_j<x_i-r_i<x_i+r_i\le{c}<x_j+r_j$, which means $B(x_i)\subseteq B(x_j)$, a contradiction. Suppose $c$ is covered by $B(x_j)$ with $x_j>x_{i+1}$, then similarly we can prove $B(x_{i+1})\subseteq B(x_j)$ and obtain a contradiction.

Next we prove that given $B(x_i)$ and $B(x_{i+1})$, if $x\in B(x_i)-B(x_{i+1})$ and $y\in B(x_i)\cap{B(x_{i+1})}$ and $z\in B(x_{i+1})-B(x_{i})$, then $f(x)\le f(y)\le f(z)$. It suffices to show $x<y<z$. Consider $x$ and $y$, $x\notin B(x_{i+1})$ means either $x\le x_{i+1}-r_{i+1}$ or $x\ge x_{i+1}+r_{i+1}$, if the latter is true, then we have
$$
x_{i+1}+r_{i+1}\le{x}<x_i+r_i
\\
x_i-r_i<2x_i-x<2x_{i+1}-x\le x_{i+1}-r_{i+1}
$$
which means $B(x_{i+1})\subseteq B(x_i)$, a contradiction. Thus $x\le x_{i+1}-r_{i+1}<y$, similarly we have $y<z$.

Finally, we prove $f(m)\le{f(n)}$, let $c_i\in B(x_i)\cap{B(x_{i+1})}$ for $i=1,\dots,k-1$, let
$$
M=\sup\{l\in\mathbf{N}:m\in{B(x_l)}\},\quad N=\inf\{l\in\mathbf{N}:n\in{B(x_l)}\}
$$
apparently $M<N$, then $f(m)\le{f(c_M)}\le\cdots\le{f(c_N)}\le{f(n)}$.

### 4.61

Let $f$ be continuous on a compact interval $[a, b]$ and assume that $f$ does not have a local maximum or a local minimum at any interior point. (See the NOTE following
Exercise 4.25.) Prove that $f$ must be monotonic on $[a, b]$.  

#### Proof

First consider the case $f(a)\le{f(b)}$, we claim $f$ must be monotonic increasing. Assume not, then $\exist a<m'<n'<b$ such that $f(m')>f(n')$, let $m\in[a,n']$ be the point where $f(m)=\max\{f(x):x\in[a,n']\}$, and $n\in[m',b]$ be the point such that $f(n)=\min\{f(x):x\in[m',b]\}$. Thus $f(m)\ge f(m')>f(n')\ge f(n)$. If $m=a$ and $n=b$, then we get $f(a)>f(b)$ and contradicts our case hypothesis, thus either $m\in(a,n')$ or $n\in(m',b)$. If $m\in(a,n')$ we let $r=\min(m-a,n'-m)$, then for any $x\in B(m,r)$, we have $f(x)\le f(m)$, thus $m$ is a local maximum. If $n\in(m',b)$, we let $r=\min(n-m',b-n)$, then for any $x\in B(n,r)$ we have $f(x)\ge f(n)$, thus $n$ is a local minimum. In either case, we get a contradiction. Thus $f$ must be monotonic increasing. For the case $f(a)\ge f(b)$ we can similarly prove $f$ must be monotonic decreasing.

### 4.62

If $f$ is one-to-one and continuous on $[a, b]$, prove that $f$ must be strictly monotonic on $[a, b]$. That is, prove that every topological mapping of $[a,b]$ onto an interval $[c, d]$ must be strictly monotonic. 

#### Proof

Assume there exist a local maximum $x\in(a,b)$, then there is a ball $B(x)$ such that $f(y)\le{f(x)}$ for all $y\in B(x)\cap [a,b]$, shrink the radius of the ball to $r>0$ so that $B(x;r)\subseteq(a,b)$, this is possible since $x$ is an interior point of $(a,b)$. Let $x_1=x-r/2$ and $x_2=x+r/2$, then $f(x_1)<f(x)$ and $f(x_2)<f(x)$ as $r>0$ and $f$ is one-to-one. We also have $f(x_1)\neq f(x_2)$. If $f(x_1)<f(x_2)$ then by Bolzano's Theorem we can find $z\in(x_1,x)$ such that $f(z)=f(x_2)$, a contradiction to $f$ being one-to-one. If $f(x_1)>f(x_2)$ we can find $z\in(x,x_2)$ such that $f(z)=f(x_1)$, also a contradiction to $f$ being one-to-one. We conclude $f$ cannot have any local maximum on $(a,b)$, similarly cannot have any local minimum on $(a,b)$. By Exercise 4.61, $f$ is monotonic on $[a, b]$, thus strictly monotonic since $f$ is one-to-one.

### 4.63

Let $f$ be an increasing function defined on $[a, b]$ and let $x_1,\dots,x_n$ be $n$ points in the interior such that $a<x_1<x_2<\cdots<x_n<b$.

(a) Show that $\sum_{k=1}^n[f(x_k+)-f(x_k-)]\le f(b-)-f(a+)$.

(b) Deduce from part (a) that the set of discontinuities of $f$ is countable. 

(c) Prove that $f$ has points of continuity in every open subinterval of $[a, b]$. 

#### Proof

(a) If $x,y\in[a,b]$ with $x<y$, then there is $\delta>0$ such that $x+\delta<y-\delta$, which means $z<z'$ for all $z<x+\delta$ and all $z'>y-\delta$, so $f(z)\le f(z')$, which means $f(x+)\le f(y-)$. So we can conclude:
$$
\begin{aligned}\sum_{k=1}^n[f(x_k+)-f(x_k-)]&=f(x_n+)-\sum_{k=2}^n[f(x_k-)-f(x_{k-1}+)]-f(x_1-)
\\&\le f(x_n+)-f(x_1-)\le f(b-)-f(a+)
\end{aligned}
$$
(b) $f$ is bounded by $f(a)$ and $f(b)$, if $x$ is a discontinuity of $f$, then  the only possible case is $f(x-)<f(x+)$. Let $D$ be the set of discontinuities of $f$, let
$$
D_n=\{x\in[a,b]:f(x+)-f(x-)\ge{1/n}\}
$$
then we have $D=\bigcup_{n=1}^{\infty}D_n$. Let $K_n$ be the number of points in $D_n$, then we have
$$
K_n\leq n[f(b-)-f(a+)]
$$
 which is finite. Thus each $D_n$ is finite, so $D$ is countable.

(c) There are uncountable many points in every open subinterval of $[a,b]$, thus $f$ must have points of continuity in it.

### 4.64

Give an example of a function $f$, defined and strictly increasing on a set $S$ in $\mathbf{R}$, such that $f^{-1}$ is not continuous on $f(S)$.

#### Solution

Define
$$
f=\begin{cases}
x,\quad&x\in[0,1]
\\
x-1,\quad&x\in(2,3]
\end{cases}
$$
then $f$ is strictly increasing on $S=[0,1]\cup(2,3]$, and $f(S)=[0,2]$, we can see
$$
f^{-1}(y)=\begin{cases}
y,\quad&y\in[0,1]
\\
y+1\quad&y\in(1,2]
\end{cases}
$$
this means $f^{-1}$ is not continuous at $y=1$.

### 4.65

Let $f$ be strictly increasing on a subset $S$ of $\mathbf{R}$. Assume that the image $f(S)$ has one of the following properties: (a) $f(S)$ is open; (b) $f(S)$ is connected; (c) $f(S)$ is closed. Prove that $f$ must be continuous on $S$.  

#### Proof

Let $f$ be a strictly increasing function on $S$ which is not continuous, assume $f$ is not continuous at $x\in S$, then $f(x-)<f(x+)$ and $f(x)\in[f(x-),f(x+)]$, which lead to the following results:

First, at least one of $f(x-),f(x+)$ is not in $f(S)$, suppose $f(x-)\in f(S)$, then there is $y\in S$ such that $f(y)=f(x-)$, for any $\varepsilon>0$, we have $f(x+\varepsilon)\ge f(x+)>f(y)$ and $f(x-\varepsilon)<f(x-)=f(y)$, thus $x-\varepsilon<y<x+\varepsilon$, which means $y=x$, similarly $f(x+)\in f(S)$ means the only possible point $y$ which can make $f(y)=f(x+)$ is $y=x$, this is impossible since $f(x-)\neq f(x+)$. As both $f(x-),f(x+)$ are accumulation point of $f(S)$, we conclude $f(S)$ is not closed.

Next, $f(x)$ is not an interior point of $f(S)$, since we either have $f(x-)<f(x)$ or $f(x)<f(x+)$, if $f(x-)<f(x)$, then for any ball $B(f(x);r)$, let
$$
z=f(x)-\dfrac{\min(r,f(x)-f(x-))}{2}
$$
then $z\in B(f(x);r)$, but if there exist $y\in S$ such that $f(y)=z$, we would have $y<x$ since $z<f(x)$, then $y=x-\delta$ for some $\delta>0$, this lead to 
$$
z=f(y)=f(x-\delta)<f(x-\delta/2)\le f(x-)
$$
a contradiction to $z>f(x-)$. So $z\notin f(S)$, we conclude $f(x)$ is not an interior point of $f(S)$, and $f(S)$ is not open.

Finally, when $f(x)<f(x+)$, we let $A=f(S\cap(-\infty, x])$ and $B=f(S\cap(x,+\infty))$, then $A\cap B=\empty, A\cup B=f(S)$, and both $A$ and $B$ are open in $f(S)$, so $f(S)$ is disconnected. When $f(x)=f(x+)$ we let $A=f(S\cap(-\infty, x)$ and $B=f(S\cap[x,+\infty))$, still can have $f(S)$ being disconnected.

So if any one of (a) to (c) is true, $f$ must be continuous.