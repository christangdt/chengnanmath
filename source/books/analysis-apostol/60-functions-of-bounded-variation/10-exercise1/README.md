# Exercise 1-7 (Functions of bounded variation)

### 6.1

Determine which of the following functions are of bounded variation on $[0,1]$.

a) $f(x)=x^2\sin(1/x)$ if $x\neq0$, $f(0)=0$.

b) $f(x)=\sqrt{x}\sin(1/x)$ if $x\neq0$, $f(0)=0$.

#### Solution

a) When $x\ne0$, we can have $f'(x)=2x\sin(1/x)-\cos(1/x)$, so $|f'(x)|\le3$ for $x\in(0,1]$. It is easy to see that $\lim_{x\to0}f(x)=0=f(0)$, thus $f$ is continuous on $[0,1]$, apply Theorem 6.6, we have $f$ is of bounded variation on $[0,1]$.

b) Choose a particular partition
$$
P=\left\{0,\dfrac{2}{(2n+1)\pi},\dfrac{2}{2n\pi},\dots,\dfrac{2}{\pi},1\right\}
$$
we have
$$
\begin{aligned}
\sum_{k=1}^{2n}|\Delta f_k|&=\sqrt{\dfrac{2}{\pi}}\left(\dfrac{2}{\sqrt{2n+1}}+\cdots+\dfrac{2}{\sqrt{3}}\right)+\sqrt{\dfrac{2}{\pi}}+\sin1-\sqrt{\dfrac{2}{\pi}}
\\&\ge\sqrt{\dfrac{8}{\pi}}\left(\dfrac{1}{\sqrt{2n+1}}+\cdots+\dfrac{1}{\sqrt{3}}\right)\ge\sum_{k=1}^n\dfrac{1}{\sqrt{2n+1}}\ge\sum_{k=1}^n\dfrac{1}{2n+1}
\end{aligned}
$$
Since $\sum_{k=1}^n\frac{1}{2n+1}$ diverges, we can find $N$ such that $\sum_{k=1}^N\frac{1}{2n+1}>M$ for any $M$, thus $f$ is not of bounded variation on $[0,1]$.

### 6.2

A function $f$ defined on $[a,b]$ is said to satisfy a uniform Lipschitz condition of order $\alpha>0$ on $[a,b]$ if there exists a constant $M>0$ such that $|f(x)-f(y)|<M|x-y|^{\alpha}$ for all $x,y\in[a,b]$.

a) If $f$ is such a function, show that $\alpha>1$ implies $f$ is constant on $[a,b]$, whereas
$\alpha=1$ implies $f$ is of bounded variation $[a,b]$.

b) Give an example of a function $f$ satisfying a uniform Lipschitz condition of order
$\alpha<1$ on $[a,b]$ such that $f$ is not of bounded variation on $[a,b]$.

c) Give an example of a function $f$ which is of bounded variation on $[a, b]$ but
which satisfies no uniform Lipschitz condition on $[a,b]$. 

#### Solution

a) It is easy to see that if $\alpha\ge1$, then $f$ is continuous on $[a,b]$. For $\forall x\in(a,b)$ and sufficiently small $h>0$ we have
$$
\left|\dfrac{f(x+h)-f(x)}{h}\right|<Mh^{\alpha-1}
$$
thus if $\alpha>1$, then $f'(x)=0$, and $f$ is constant on $[a,b]$. If $\alpha=1$, then we have $|f'(x)|<M$ on $[a,b]$, thus $f'$ is bounded, which means $f$ is of bounded variation $[a,b]$.

b) One example can be
$$
f(x)=\sum_{k=1}^{\infty}\dfrac{\cos(3^kx)}{3^{k\alpha}}
$$

c) Define
$$
f(x)=\begin{cases}x,\quad&x\in[a,b)\\b+1,\quad&x=b\end{cases}
$$
then $f$ is increasing on $[a,b]$, thus is of bounded variation on $[a,b]$, assume $f$ satisfy some uniform Lipschitz condition, and let $\alpha>0$ and $M>0$ be the parameters of uniform Lipschitz condition, we select
$$
c=b-\dfrac{1}{M^{1/\alpha}}\implies M|b-c|^{\alpha}=M\dfrac{1}{M}=1
$$
but 
$$
|f(b)-f(c)|=b+1-b+\dfrac{1}{M^{1/\alpha}}=1+\dfrac{1}{M^{1/\alpha}}>1
$$
thus we have $|f(b)-f(c)|>M|b-c|^{\alpha}$, a contradiction.

### 6.3

Show that a polynomial $f$ is of bounded variation on every compact interval $[a,b]$.
Describe a method for finding the total variation of $f$ on $[a,b]$ if the zeros of the derivative $f'$ are known.

#### Solution

A polynomial $f$ is continuous on $[a,b]$, and $f'$ is also a polynomial, thus bounded on $[a,b]$, which means $f$ is of bounded variation.

If the zeros of $f'$ are known, namely $\{x_1,\dots,x_n\}$, let $x_0=a$ and $x_{n+1}=b$, we may have $x_1=a$ or $x_n=b$, but has no effect. By the additivity of total variation we have $V_f(a,b)=\sum_{i=1}^nV_f(x_i,x_{i+1})$. At each interval $[x_i,x_{i+1}]$ we can have $f$ being monotonic, since $f'$ does not change sign, thus $V_f(x_i,x_{i+1})=|f(x_{i+1})-f(x_i)|$, it follows that
$$
V_f(a,b)=\sum_{i=1}^n|f(x_{i+1})-f(x_i)|
$$

### 6.4

A nonempty set S of real-valued functions defined on an interval $[a,b]$ is called a
*linear space of functions* if it has the following two properties: 

a) If $f\in S$, then $cf\in S$ for every real number $c$.

b) If $f\in S$ and $g\in S$, then $f+g\in S$.

Theorem 6.9 shows that the set $V$ of all functions of bounded variation on $[a, b]$ is a linear space. If $S$ is any linear space which contains all monotonic functions on $[a,b]$, prove that $V\subseteq S$. This can be described by saying that the functions of bounded variation form the smallest linear space containing all monotonic functions. 

#### Proof

Let $f\in V$, then $f$ is of bounded variation on $[a,b]$, thus can be expressed as $f=f_1-f_2$, where $f_1,f_2$ are monotonic functions on $[a,b]$, thus $f_1,f_2\in S$, since $S$ is a linear space, we have $f_1+(-1)f_2=f\in S$, this means $V\subseteq S$.

### 6.5

Let $f$ be a real-valued function defined on $[0,1]$ such that $f(0)>0,f(x)\ne x$ for all $x$, and $f(x)\le f(y)$ whenever $x\le y$. Let $A=\{x:f(x)>x\}$. Prove that $\sup{A}\in A$ and $f(1)>1$.

#### Proof

That $f(0)>0$ means $0\in A$, so $A$ is nonempty and has a supreme, let $a=\sup{A}$ and assume $a\notin A$, then we must have $f(a)<a$, thus for $\varepsilon_0=a-f(a)>0$ we can find $b\in A$ such that $b\in(a-\varepsilon_0,a)$, so $f(b)>b>a-\varepsilon_0=f(a)$, on the other hand, from $b<a$ we have $f(b)\le f(a)$, so we have $f(b)>f(a)\ge f(b)$, a contradiction.

To prove $f(1)>1$, we only need to prove $1\in A$. Assume $a=\sup{A}<1$, then we can have $f(x)<x$ whenever $x\in(a,1]$. As we have both $f(a)>a$ and $1>a$, it is possible to choose some $b\in(a,f(a))\cap(a,1]$, for this $b$ we have $f(b)<b$ and $b<f(a)$, so we get $f(b)<f(a)$ and $b>a$ at the same time, a contradiction to $f$ being monotonic increasing. Thus $\sup{A}=1$, and the conclusion follows since we already proved $\sup{A}\in A$.

### 6.6

If $f$ is defined everywhere in $\mathbf{R}^1$, then $f$ is said to be of bounded variation on $(-\infty,+\infty)$ if $f$ is of bounded variation on every finite interval and if there exists a positive number $M$ such that $V_f(a,b)<M$ for all compact intervals $[a,b]$. The total variation of $f$ on $(-\infty,+\infty)$ is then defined to be the sup of all numbers $V_f(a,b),-\infty<a<b<+\infty$, and is denoted by $V_f(-\infty,+\infty)$. Similar definitions apply to half-open infinite intervals $[a,+\infty)$ and $(-\infty,b]$.

a) State and prove theorems for the infinite interval $(-\infty,+\infty)$ analogous to Theorem 6.7, 6.9, 6.10, 6.11 and 6.12.

b) Show that Theorem 6.5 is true for $(-\infty,+\infty)$ if "monotonic" is replaced by "bounded and monotonic". State and prove a similar modification of Theorem 6.13.

#### Solution

(a) Mark the theorem analogous to Theorem 6.x as Theorem 6.x', and prove:

**Theorem 6.7'**: If $f$ is of bounded variation on $(-\infty,+\infty)$, then $f$ is bounded on $(-\infty,+\infty)$.

*Proof*: We first have $V_f(0,0)=|f(0)|<M$, for any $x\in(-\infty,+\infty)$, $f$ is of bounded variation on $[x,0]$ or $[0,x]$, thus $V_f(0,x)<M$ or $V_f(x,0)<M$, in either case we have
$$
|f(x)|<|f(0)|+M<2M
$$
thus $f$ is bounded.



**Theorem 6.9'**: Assume $f$ and $g$ are each of bounded variation on $(-\infty,+\infty)$, then so are their sum, difference and product. Also we have
$$
V_{f\pm g}(-\infty,+\infty)\le V_f(-\infty,+\infty)+V_g(-\infty,+\infty)\\ V_{f\cdot g}(-\infty,+\infty)\le AV_f(-\infty,+\infty)+BV_g(-\infty,+\infty)
$$
where
$$
A=\sup\{|g(x)|:x\in(-\infty,+\infty)\},\quad B=\sup\{|f(x)|:x\in(-\infty,+\infty)\}
$$
*Proof*: Suppose $M_1$ is the positive number such that $V_f(a,b)<M_1$ for all compact intervals $[a,b]$ and  $M_2$ is the positive number such that $V_g(a,b)<M_2$ for all compact intervals $[a,b]$. From
$$
|f(x_k)-g(x_k)\pm(f(x_{k-1})-g(x_{k-1}))|\le|f(x_k)-f(x_{k-1})|+|g(x_k)-g(x_{k-1})|
$$
we can see that $|\Delta (f_k\pm g_k)|\le|\Delta f_k|+|\Delta g_k|$, thus on every finite interval $[a,b]$ we have $V_{f\pm g}(a,b)\le V_f(a,b)+V_g(a,b)$, this means $f\pm g$ is of bounded variation on every finite interval. Further, we can have $V_{f\pm g}(a,b)\le M_1+M_2$ for all compact intervals $[a,b]$, so $f\pm g$ is of bounded variation on $(-\infty,+\infty)$. To prove the inequality, for any $-\infty<a<b<+\infty$, we have
$$
V_{f\pm g}(a,b)\le V_f(a,b)+V_g(a,b)\le V_f(-\infty,+\infty)+V_g(-\infty,+\infty)
$$
thus $V_f(-\infty,+\infty)+V_g(-\infty,+\infty)$ is an upper bound of $V_{f\pm g}(a,b)$, and the inequality follows.

Similarly, let $h=f\cdot g$ and we can have $V_h(a,b)\le AV_f(a,b)+BV_g(a,b)$ on every finite interval $[a,b]$, thus $h$ is of bounded variation on every finite interval. Further, we can have $V_h(a,b)\le AM_1+BM_2$ for all compact intervals $[a,b]$, so $h$ is of bounded variation on $(-\infty,+\infty)$. To prove the inequality,  for any $-\infty<a<b<+\infty$, we can see the number $AV_f(-\infty,+\infty)+BV_g(-\infty,+\infty)$ is an upper bound of $V_h(a,b)$, and the inequality follows.



**Theorem 6.10'**: If $f$ is of bounded variation on $(-\infty,+\infty)$, and $|f(x)|\ge m>0$ for all $x$, then $g=1/f$ is of bounded variation on $(-\infty,+\infty)$ and $V_g(-\infty,+\infty)\le V_f(-\infty,+\infty)/m^2$.

*Proof*: From $|\Delta g_k|\le|\Delta f_k|/m^2$, we see that $V_g(a,b)\le V_f(a,b)/m^2$, thus suppose $M_1$ is the positive number such that $V_f(a,b)<M_1$ for all compact intervals $[a,b]$, we can have $V_g(a,b)\le M_1/m^2$ for all compact intervals $[a,b]$, this shows that $g$ is of bounded variation on $(-\infty,+\infty)$. From $V_g(a,b)\le V_f(a,b)/m^2$ we see that $V_f(-\infty,+\infty)/m^2$ is an upper bound of $V_g(a,b)$ for any $-\infty<a<b<+\infty$, and the inequality follows.



**Theorem 6.11'**: If $f$ is of bounded variation on $(-\infty,+\infty)$ and $c\in\mathbf{R}$, then $f$ is of bounded variation on $(-\infty,c]$ and on $[c,+\infty)$, and we have $V_f(-\infty,+\infty)=V_f(-\infty,c)+V_f(c,+\infty)$.

*Proof*: Since $f$ is of bounded variation on $(-\infty,+\infty)$, we can find $M$ such that $V_f(a,b)<M$ for all compact intervals $[a,b]$, thus $V_f(a,c)<M$ for all $a<c$ and $V_f(c,b)<M$ for all $b>c$, it follows that $f$ is of bounded variation on $(-\infty,c]$ and on $[c,+\infty)$. Notice that
$$
V_f(-\infty,c)=\sup\{V_f(a,c):-\infty<a<c\}
\\
V_f(c,+\infty)=\sup\{V_f(c,b):c<b<+\infty\}
$$
and we have $V_f(a,b)=V_f(a,c)+V_f(c,b)$, thus $V_f(a,c)+V_f(c,b)\le V_f(-\infty,+\infty)$ for all $a,b$ such that $-\infty<a<c<b<+\infty$, it follows that
$$
V_f(-\infty,c)+V_f(c,+\infty)\le V_f(-\infty,+\infty)
$$
From $V_f(a,b)=V_f(a,c)+V_f(c,b)$ we can also get $V_f(a,b)\le V_f(-\infty,c)+V_f(c,+\infty)$ for all $a,b$ such that $-\infty<a<b<+\infty$, it follows that
$$
V_f(-\infty,+\infty)\le V_f(-\infty,c)+V_f(c,+\infty)
$$
and this completes the proof.



**Theorem 6.12'**: Let $f$ be of bounded variation on $(-\infty,+\infty)$. Let $V$ be defined on $(-\infty,+\infty)$ as follows: $V(x)=V_f(-\infty,x)$ if $-\infty<x<+\infty$, $V(-\infty)=0$. Then both $V$ and $V-f$ are increasing functions on $(-\infty,+\infty)$.

*Proof*: For $x<y$ we have $V_f(a,y)=V_f(a,x)+V_f(x,y)$ for all $a<x$, thus we can have
$$
V_f(a,y)\le V_f(-\infty,x)+V_f(x,y)\implies V_f(-\infty,y)\le V_f(-\infty,x)+V_f(x,y)
\\
V_f(a,x)\le V_f(-\infty,y)-V_f(x,y)\implies V_f(-\infty,x)\le V_f(-\infty,y)-V_f(x,y)
$$
this means $V_f(-\infty,y)=V_f(-\infty,x)+V_f(x,y)$, so $V(y)-V(x)=V_f(x,y)\ge0$ and $V(y)\ge V(x)$, which means $V$ is increasing.

Let $D(x)=V(x)-f(x)$ for $x\in(-\infty,+\infty)$. Then if $x<y$, we have
$$
D(y)-D(x)=V_f(x,y)-[f(y)-f(x)]\ge0
$$
the last inequality follows from the definition of $V_f(x,y)$. This means $D$ is increasing.

### 6.7

Assume that $f$ is of bounded variation on $[a,b]$ and let $P=\{x_0,x_1,\dots,x_n\}\in\mathscr{P}[a,b]$. As usual, write $\Delta f_k=f(x_k)-f(x_{k-1}), k=1,2,\dots,n$. Define
$$
A(P)=\{k:\Delta f_k>0\},\qquad B(P)=\{k:\Delta f_k<0\}
$$
The numbers
$$
p_f(a,b)=\sup\left\{\sum_{k\in A(P)}\Delta f_k:P\in\mathscr{P}[a,b]\right\}
$$
and
$$
n_f(a,b)=\sup\left\{\sum_{k\in B(P)}|\Delta f_k|:P\in\mathscr{P}[a,b]\right\}
$$
are called, respectively, the positive and negative variations of $f$ on $[a,b]$. For each $x$ in $(a,b]$, let $V(x)=V_f(a,x),p(x)=p_f(a,x),n(x)=n_f(a,x)$ and let $V(a)=p(a)=n(a)=0$. Show that we have

a) $V(x)=p(x)+n(x)$.

b) $0\le p(X)\le V(x)$ and $0\le n(x)\le V(x)$.

c) $p$ and $n$ are increasing on $[a,b]$.

d) $f(x)=f(a)+p(x)-n(x)$.

e) $2p(x)=V(x)+f(x)-f(a),\quad 2n(x)=V(x)-f(x)+f(a)$.

f) Every point of continuity of $f$ is also a point of continuity of $p$ and of $n$.

#### Solution

(a) If $x=a$, there is nothing to prove. Suppose $x\in(a,b]$, for any partition $P\in\mathscr{P}[a,x]$, we let $\sum(P)$ denote the sum $\sum|\Delta f_k|$ corresponding to the partition $P$, then
$$
\sum(P)=\sum(A(P))+\sum(B(P))\le p_f(a,x)+n_f(a,x)=p(x)+n(x)
$$
thus we can have $V(x)\le p(x)+n(x)$. Conversely, given $A(P_1)$ and $B(P_2)$ with $P_1,P_2\in\mathscr{P}[a,x]$, we see that add a point to $P_1$ will enlarge $A(P_1)$, suppose $P_1=\{a=x_0,x_1,\dots,x_n=x\}$, and a new point $c$ is added between $x_k$ and $x_{k+1}$, then $A(P_1)$ and $A(P_1\cup\{c\})$ differs on $\Delta f_{k+1}=f(x_{k+1})-f(x_k)$ and $f(x_{k+1})-f(c), f(c)-f(x_k)$, let $\Delta_1=f(_{k+1})-f(c)$ and $\Delta_2=f(c)-f(x_k)$, we have $\Delta f_{k+1}=\Delta_1+\Delta_2$. Split in cases:

If all three deltas are positive, they are equal and $A(P_1)=A(P_1\cup\{c\})$. 

If $\Delta f_{k+1}<0$, then it does not contribute to $A(P_1)$, but $\Delta_1$ or $\Delta_2$ may be positive, thus $A(P_1)\le A(P_1\cup\{c\})$.

If $\Delta f_{k+1}>0$ but one of $\Delta_1$ and $\Delta_2$ is negative, suppose $\Delta_1<0$ and $\Delta_2>0$, then $\Delta_2$ contributes to $A(P_1\cup\{c\})$ more than $\Delta f_{k+1}$ contributes to $A(P_1)$, so $A(P_1)< A(P_1\cup\{c\})$.

In conclusion we have $A(P_1)\le A(P_1\cup\{c\})$ thus $A(P_1)\le A(P_1\cup P_2)$. Similarly we can have $B(P_1)\le B(P_1\cup P_2)$. Thus
$$
\begin{aligned}
\sum(A(P_1))+\sum(B(P_2))&\le\sum(A(P_1\cup P_2))+\sum(B(P_1\cup P_2))
\\&=\sum(P_1\cup P_2)\le V_f(a,x)=V(x)
\end{aligned}
$$
so we have $p(x)+n(x)\le V(x)$.



(b) By definition, $p(x)\ge0$ and $n(x)\ge0$, use (a) we get the result.



(c) If $a\le x<y\le b$, then for any $P\in\mathscr{P}[a,x]$, the partition $P'=P\cup\{y\}\in\mathscr{P}[a,y]$, thus $\sum(A(P))\le\sum(A(P'))\le p(y)$, so $p(x)\le p(y)$ and $p$ is increasing. Similarly for $n$.



(d) We have $f(x)-f(a)=\sum(A(p))-\sum(B(P))$ for any $P\in\mathscr{P}[a,x]$, thus
$$
\begin{aligned}
&\qquad f(x)-f(a)+\sum(B(P))=\sum(A(P))\le p(x)\\&\implies\sum(B(P))\le p(x)-(f(x)-f(a))
\\&\implies n(x)\le p(x)-(f(x)-f(a))\implies f(x)\le f(a)+p(x)-n(x)
\end{aligned}
$$
and
$$
\begin{aligned}
&\qquad\sum(A(P))-(f(x)-f(a))=\sum(B(P))\le n(x)
\\&\implies\sum(A(P))\le n(x)+f(x)-f(a)
\\&\implies p(x)\le n(x)+f(x)-f(a)\implies f(x)\ge f(a)+p(x)-n(x)
\end{aligned}
$$


(e) Use (a) and (d) we have
$$
2p(x)=p(x)+V(x)-n(x)=V(x)+[p(x)-n(x)]=V(x)+f(x)-f(a)
\\
2n(x)=n(x)+V(x)-p(x)=V(x)-[p(x)-n(x)]=V(x)-f(x)+f(a)
$$


(f) Theorem 6.14 means if $c\in[a,b]$ is a point of continuity of $f$, then it is also a point of continuity of $V$. Thus for $\forall\varepsilon>0$, there exists $\delta>0$ such that whenever $|x-c|<\delta$, we have
$$
|f(x)-f(c)|<\varepsilon,\quad |V(x)-V(c)|<\varepsilon
$$
thus use (e) we have whenever $|x-c|<\delta$:
$$
\begin{aligned}
|p(x)-p(z)|&=\dfrac{1}{2}|V(x)+f(x)-V(c)-f(c)|\\&\le\dfrac{1}{2}(|V(x)-V(c)|+|f(x)-f(c)|)<\dfrac{1}{2}(2\varepsilon)=\varepsilon
\end{aligned}
$$
thus $c$ is a point of continuity of $p$, similarly we can prove $c$ is a point of continuity of $n$.