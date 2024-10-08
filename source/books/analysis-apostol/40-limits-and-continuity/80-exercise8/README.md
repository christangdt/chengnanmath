# Exercise 66-72 (Metric spaces and fixed points)

### 4.66

Let $B(S)$ denote the set of all real-valued functions which are defined and bounded on a nonempty set $S$. If $f\in B(S)$, let
$$
\|f\|=\sup_{x\in S}|f(x)|
$$
The number $\|f\|$ is called the "sup norm" of $f$.

(a) Prove that the formula $d(f,g)=\|f-g\|$ defines a metric $d$ on $B(S)$.

(b) Prove that the metric space $(B(s),d)$ is complete.

#### Proof

(a) By definition, $d(f,g)\ge0$, since $|f(x)-g(x)|=|g(x)-f(x)|$ for all $x\in S$, we can have $\sup_{x\in S}|f(x)-g(x)|=\sup_{x\in S}|g(x)-f(x)|$ and $d(f,g)=d(g,f)$. Use triangle inequality we have
$$
\begin{aligned}
|f(x)-g(x)|&\le|f(x)-h(x)|+|h(x)-g(x)|
\\&\le\|f-h\|+\|h-g\|
\end{aligned}
$$
which gives $\|f-g\|\le\|f-h\|+\|h-g\|$, or $d(f,h)\le d(f,g)+d(g,h)$.

(b) Let $\{f_n\}$ be a Cauchy sequence in $(B(S),d)$, then $\forall\varepsilon>0$, there exist $N>0$ such that $m,n>N$ means $d(f_n,f_m)<\varepsilon$, this means $|f_n(x)-f_m(x)|<\varepsilon$ for all $x\in S$, thus for a fixed $x\in S$, the sequence $\{f_n(x)\}$ is a Cauchy sequence in $\mathbf{R}$, thus converge to a point $f_x$, define $f(x)=f_x,x\in S$, then $f\in B(S)$. Let $m\to\infty$ we have $|f_n(x)-f_x|\le\varepsilon,\forall{x\in S}$ whenever $n>N$, this means $\|f_n-f\|\le\varepsilon$, or $d(f_n,f)\le\varepsilon$ for $n>N$, so $\{f_n\}$ converges to $f$ in $(B(S),d)$.

### 4.67

Refer to Exercise 4.66 and let $C(S)$ denote the subset of $B(S)$ consisting of all functions continuous and bounded on $S$, where now $S$ is a metric space. 

(a) Prove that $C(S)$ is a closed subset of $B(S)$.

(b) Prove that the metric subspace $C(S)$ is complete.

#### Proof

(a) Let $f$ be an accumulation point of $C(S)$, then $\forall\varepsilon>0$, there exist $g\in C(S)$ such that $d(f,g)=\|f-g\|<\varepsilon/3$, Choose $\varepsilon<1$ we can see $f$ is bounded on $S$, since $|f(x)|<|g(x)|+1,x\in S$ and $g$ is bounded. To see $f$ is continuous on $S$, let $a\in S$, since $g$ is continuous at $a$, we can find $\delta>0$ such that
$$
d_S(x,a)<\delta\implies|g(x)-g(a)|<\varepsilon/3
$$
this means for $x$ which satisfy $d_S(x,a)<\delta$, we have
$$
|f(x)-f(a)|\le|f(x)-g(x)|+|g(x)-g(a)|+|g(a)-f(a)|<\varepsilon
$$
thus $f$ is continuous at $a$, and continuous on $S$, so $f\in C(S)$ and $C(S)$ is closed.

(b) Let $\{f_n\}$ be a Cauchy sequence in $C(S)\subseteq B(S)$, then $f_n\to{f}\in B(S)$ by Exercise 4.66(b), and use (a) we also get $f\in C(S)$, so $C(S)$ is complete.

### 4.68

Refer to the proof of the fixed-point theorem (Theorem 4.48) for notation. 

(a) Prove that $d(p,p_n)\le d(x,f(x)){\alpha}^n/(1-\alpha)$.

(b) Take $f(x)=\dfrac{1}{2}(x+2/x), S=[1,+\infty)$. Prove that $f$ is a contraction of $S$ with contraction constant $\alpha=\dfrac{1}{2}$ and fixed point $p=\sqrt{2}$. Form the sequence $\{p_n\}$ starting with $x=p_0=1$ and show that $|p_n-\sqrt{2}|\le2^{-n}$.

#### Proof

(a) From proof of Theorem 4.48 we have
$$
d(p_m,p_n)\le c\dfrac{\alpha^n-\alpha^m}{1-\alpha}=d(x,f(x))\dfrac{\alpha^n-\alpha^m}{1-\alpha}
$$
Let $m\to\infty$, then $p_m\to p$ and $\alpha^m\to0$, the conclusion follows.

(b) We have
$$
x,y\in S\implies\dfrac{1}{xy}\in(0,1]\implies\left|\dfrac{1}{2}-\dfrac{1}{xy}\right|\in[0,1/2]
$$
thus
$$
\begin{aligned}
d(f(x),f(y))&=\left|\dfrac{1}{2}\left(x+\dfrac{2}{x}\right)-\dfrac{1}{2}\left(y+\dfrac{2}{y}\right)\right|
\\&=\dfrac{1}{2}\left|(x-y)+\dfrac{2}{xy}(y-x)\right|
\\&=|x-y|\left|\dfrac{1}{2}-\dfrac{1}{xy}\right|\le\dfrac{1}{2}d(x,y)
\end{aligned}
$$
This means $f$ is a contraction of $S$, the contraction constant is $\alpha=1/2$. To get the fixed point $p$, we know $p=f(p)$, as $f(x)\ge1$ for $x\in{S}$, we have $p\ge1$, so
$$
p=\dfrac{1}{2}\left(p+\dfrac{2}{p}\right)\implies\dfrac{p}{2}=\dfrac{1}{p}\implies p^2=2\implies p=\sqrt{2}
$$
For the sequence $\{p_n\}$ starting from $x=1$, we have $d(x,f(x))=1/2$, thus use (a) we have
$$
|p_n-\sqrt{2}|=d(p_n,p)\le\dfrac{1}{2}\dfrac{\left(\dfrac{1}{2}\right)^n}{1-\dfrac{1}{2}}=2^{-n}
$$

### 4.69

Show by counterexamples that the fixed-point theorem for contractions need not hold if either (a) the underlying metric space is not complete, or (b) the contraction constant $\alpha\ge1$.

#### Solution

(a) Let $S=(0,1/4]$, and $f(x)=x^2,x\in{S}$, then
$$
|f(x)-f(y)|=|x^2-y^2|=(x+y)|x-y|\le\dfrac{1}{2}|x-y|
$$
but $S$ is not complete, so $f$ has no fixed points in $S$.

(b) Let $S=[0,+\infty)$ and $f(x)=x+1$, then $S$ is complete but $|f(x)-f(y)|=|x-y|$, so $f$ has no fixed point in $S$.

### 4.70

Let $f:S\to{S}$ be a function from a complete metric space $(S,d)$ into itself. Assume there is a real sequence $\{\alpha_n\}$ which converges to $0$ such that $d(f^n(x),f^n(y))\le\alpha_n d(x,y)$ for all $n\ge1$ and all $x,y\in S$, where $f^n$ is the $n$th iterate of $f$. Prove that $f$ has a unique fixed point.

#### Proof

We can find a $m\in\mathbf{N}$ such that $\alpha_n\le1/2$ whenever $n\ge{m}$, thus $f^m$ satisfies
$$
d(f^m(x),f^m(y))\le\alpha_md(x,y)\le\dfrac{1}{2}d(x,y),\quad\forall x,y\in S
$$
so $f^m$ is a contraction on $S$, thus has a unique fixed point $p\in S$, and $f^m(p)=p$. Then we have
$$
f^m(f(p))=f^{m+1}(p)=f(f^m(p))=f(p)
$$
thus $f(p)$ is a fixed point of $f^m$, which means $f(p)=p$, thus $p$ is a fixed point of $f$. If there is any $q\in S$ satisfies $f(q)=q$, then by iteration we have
$$
f^m(q)=f^{m-1}(f(q))=f^{m-1}(q)=\cdots=f(q)=q
$$
thus $q=p$ and the fixed point is unique.

### 4.71

Let $f:S\to{S}$ be a function from a metric space $(S,d)$ into itself such that
$$
d(f(x),f(y))<d(x,y)
$$
whenever $x\neq y$.

(a) Prove that $f$ has at most one fixed point, and give an example of such an $f$ with no fixed point. 

(b) If $S$ is compact, prove that $f$ has exactly one fixed point. 

(c) Give an example with $S$ compact in which $f$ is not a contraction.

#### Solution

(a) Assume $f$ has fixed points $p,q$, then $d(f(p),f(q))=d(p,q)$, but $d(f(p),f(q))<d(p,q)$ whenever $p\neq q$, thus we must have $p=q$, so $f$ cannot have more than one fixed point. One example of such an $f$ with no fixed point is
$$
f(x)=\sqrt{x},x\in(1,+\infty)
$$
(b) Let $g(x)=d(x,f(x))$ for $x\in{S}$, then $g\ge0$, and
$$
\begin{aligned}
|g(x)-g(y)|&=\left|d(x,f(x))-d(y,f(y))\right|
\\&=|d(x,f(x))-d(y,f(x))+d(y,f(x))-d(y,f(y))|
\\&\le|d(x,f(x))-d(y,f(x))|+|d(y,f(x))-d(y,f(y))|
\\&\le d(x,y)+d(f(x),f(y))<2d(x,y)
\end{aligned}
$$
so $g$ is continuous on $S$, since $S$ is compact, $g$ attains its minimum on $S$. Let $g(p)=\min_{x\in S}g(S)$, we shall prove $g(p)=0$, assume not, then $g(p)>0$, thus $p\neq f(p)$, let $q=f(p)\in{S}$, then
$$
g(q)=d(q,f(q))=d(f(p),f(q))<d(p,q)=d(p,f(p))=g(p)
$$
a contradiction to $g(p)=\min_{x\in S}g(S)$, thus $g(p)=0$ and $p=f(p)$, so $p$ is a fixed point of $f$, the uniqueness follows from (a).

(c) Let $f(x)=2\sqrt{x}$ for $x\in[1,2]$, we have $[1,2]$ being compact, and for $\forall x,y\in[1,2]$ with $x\neq y$, we have
$$
|f(x)-f(y)|=2|\sqrt{x}-\sqrt{y}|=2\dfrac{|x-y|}{\sqrt{x}+\sqrt{y}}<|x-y|
$$
But $f$ is not a contraction, given any $\alpha<1$, choose
$$
x=\left(\dfrac{3-\alpha}{\alpha+1}\right)^2>1,\quad y=1
$$
we have
$$
|f(x)-f(y)|=\dfrac{2}{\dfrac{3-\alpha}{\alpha+1}+1}|x-y|=\dfrac{\alpha+1}{2}|x-y|>\alpha|x-y|
$$

### 4.72

Assume that $f$ satisfies the condition in Exercise 4.71. If $x\in{S}$, let $p_0=x$, $p_{n+1}=f(p_n)$ and $c_n=d(p_n,p_{n+1})$ for $n\ge0$.

(a) Prove that $\{c_n\}$ is a decreasing sequence, and let $c=\lim{c_n}$.

(b) Assume there is a subsequence $\{p_{k(n)}\}$ which converges to a point $q$ in $S$. Prove that
$$
c=d(q,f(q))=d(f(q),f[f(q)]).
$$
Deduce that $q$ is a fixed point of $f$ and that $p_n\to{q}$.

#### Proof

(a) If $n\ge1$, we have
$$
c_n=d(p_n,p_{n+1})=d(f(p_{n-1}),f(p_n))<d(p_{n-1},p_n)=c_{n-1}
$$
So $\{c_n\}$ is a decreasing sequence, since obviously $c_n\ge0$ for all $n$, it converges to some $c$.

(b) The condition given shows $f$ is uniformly continuous on $S$, thus
$$
c=\lim_{n\to\infty}c_n=\lim_{n\to\infty}c_{k(n)}=\lim_{n\to\infty}d(p_{k(n)},f(p_{k(n)}))=d(q,f(q))
$$
we can also have
$$
\begin{aligned}
c&=\lim_{n\to\infty}c_{k(n)+1}=\lim_{n\to\infty}d(p_{k(n)+1},f(p_{k(n)+1}))\\&=\lim_{n\to\infty}d(f(p_{k(n)}),f[f(p_{k(n)})])=d(f(q),f[f(q)])
\end{aligned}
$$
If $c>0$, then $q\neq f(q)$, which means $d(f(q),f[f(q)])<d(q,f(q))$, but both should equal to $c$, a contradiction. Thus $c=0$ and $q$ is a fixed point of $f$.

Notice that $c=\lim_{n\to\infty}d(p_n,p_{n+1})$ and $\lim_{n\to\infty}p_{k(n)}=q$, for any $\varepsilon>0$, we can find an integer $N$ such that $d(p_{k(n)},q)<\varepsilon$ whenever $n\ge{N}$, if we set $m>k(N)$, then
$$
d(p_m,q)=d(f(p_{m-1}),f(q))<d(p_{m-1},q)<\cdots<d(p_{k(n)},q)<\varepsilon
$$
this means $p_m\to q$ as $m\to\infty$.