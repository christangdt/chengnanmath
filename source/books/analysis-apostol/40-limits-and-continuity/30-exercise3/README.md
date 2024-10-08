# Exercise 13-28 (Continuity of real-valued functions)

NOTE. In Exercises 4.10 through 4.28, all functions are real-valued. 

### 4.13

Let $f$ be continuous on $[a, b]$ and let $f(x) = 0$ when $x$ is rational. Prove that
$f(x) = 0$ for every $x$ in $[a, b]$.

#### Proof

Assume there is $p\in[a,b]$ such that $f(p)\neq 0$, let $\varepsilon=|f(p)|/2>0$, then given any $\delta>0$,   we can find some rational $q\in(p-\delta,p+\delta)\cap[a,b]$, and $|f(p)-f(q)|>\varepsilon$, this contradicts $f$ being continuous.

### 4.14

Let $f$ be continuous at the point $\mathbf{a} = (a_1, a_2, \dots, a_n)$ in $\mathbf{R}^n$. Keep $a_2, a_3, \dots, a_n$ fixed and define a new function $g$ of one real variable by the equation
$$
g(x)=f(x,a_2,\dots,a_n)
$$
Prove that $g$ is continuous at the point $x = a_1$.  

#### Proof

For $\forall\varepsilon>0$, since $f$ is continuous at $\mathbf{a}$, there is $\delta>0$ such that $|f(\mathbf{z})-f(\mathbf{a})|<\varepsilon$ whenever $|\mathbf{z}-\mathbf{a}|<\delta$, consider $g(x)$ and let $|x-a_1|<\delta$, then $\mathbf{z}=(x,a_2,\dots,a_n$) satisfy $|\mathbf{z}-\mathbf{a}|<\delta$, thus $|g(x)-g(a_1)|=|f(\mathbf{z})-f(\mathbf{a})|<\varepsilon$, this means $g$ is continuous at the point $x = a_1$. 

### 4.15

Show by an example that the converse of the statement in Exercise 4.14 is not true in general.

#### Solution

Let $f:\mathbf{R}^2\to\mathbf{R}$ be defined as follows: 
$$
f(x,y)=\begin{cases}
\dfrac{xy}{x^2+y^2},&\quad (x,y)\neq(0,0)
\\
0,&\quad (x,y)=(0,0)
\end{cases}
$$
Consider the point $\mathbf{a}=(0,0)$, function $g_1(x)=f(x,0)=0$  is continuous at the point $x=0$, function $g_2(y)=f(0,y)=0$ is continuous at the point $y=0$, but $f$ is not continuous at $\mathbf{a}=(0,0)$, since $f(1/n,1/n)=1/2$ as $n\to\infty$.

### 4.16

Let $f, g$, and $h$ be defined on $[0, 1]$ as follows:  
$$
f(x)=g(x)=h(x)=0,\quad x\in\mathbf{R}-\mathbf{Q}
\\
f(x)=1,g(x)=x,h(x)=1/n,\quad x\in\mathbf{Q}-\{0\},x=m/n
\\
f(0)=1,g(0)=0,h(0)=1
$$
Prove that $f$ is not continuous anywhere in $[0, 1]$, that $g$ is continuous only at $x = 0$, and that $h$ is continuous only at the irrational points in $[0, 1]$.

#### Proof

Let $\varepsilon=1/2$, then given any $x\in[0,1]$ and any $\delta>0$, the open ball $(x-\delta,x+\delta)\cap[0,1]$ will contain infinitely many rational points and irrational points, thus if $x$ is rational, we can find a irrational point $x'$, if $x$ is irrational, we can find a rational point $x'$, in both cases lead to $|f(x)-f(x')|=1>\varepsilon$.

Consider $g$ at $x=0$, for any $\varepsilon>0$, we can choose $\delta=\varepsilon$, if $x-0<\delta$, then $|g(x)-g(0)|=g(x)=x<\delta=\varepsilon$, thus $g$ is continuous at $0$. If $a\in(0,1]$, let $\varepsilon_0=a/2>0$, since in any ball $B(a;\delta)\cap[0,1]$ with $\delta>0$ there exists a irrational $x'$, such that $|g(x')-g(a)|=a>\varepsilon_0$, this means $g$ is not continuous at $a$.

Consider $h$, if $x$ is a irrational point in $[0,1]$, then for any $\varepsilon>0$, there is an integer $N$ such that $1/N<\varepsilon$, since $x$ is irrational, for every integer $1\leq n\leq N$ we can find integer $k_n$ such that
$$
\dfrac{k_n}{n}<x<\dfrac{k_n+1}{n},\quad\forall 1\leq n\leq N
$$
 thus we get $2N$ points, each has the form $k_n/n$ or $(k_n+1)/n$ for integer $n$ between $1$ and $N$, let $p$ be the point which is nearest to $x$ and let $\delta=|x-p|$, then in the ball $B(x;\delta)$ there is no rational points of the form $a/b$ with $b\leq N$, thus we can declare $|h(x)-h(y)|<1/N<\varepsilon, \forall y\in B(x;\delta)$, this means $h$ is continuous at $x$. Now if $x$ is rational, then $h(x)=1/n$ for some integer $n\geq 1$, given $\varepsilon_0=1/2n$, in any ball $B(x;\delta)$ there are irrational points $q$ which makes $|h(x)-h(q)|=1/n>\varepsilon_0$, thus $h$ is not continuous at $x$.

### 4.17

For each $x$ in $[0,1]$, let $f(x) = x$ if $x$ is rational, and let $f(x) = 1 - x$ if $x$ is
irrational. Prove that:  

(a) $f(f(x))=x$ for all $x$ in $[0,1]$.

(b) $f(x)+f(1-x)=1$ for all $x$ in $[0,1]$.

(c) $f$ is continuous only at the point $x=1/2$.

(d) $f$ assumes every value between $0$ and $1$.

(e) $f(x+y)-f(x)-f(y)$ is rational for all $x$ and $y$ in $[0,1]$.

#### Proof

Notice that if $x\in[0,1]$ is rational, then $1-x$ is rational. If $x$ is irrational, then so is $1-x$.

(a) If $x\in\mathbf{Q}\cap[0,1]$, then $f(f(x))=f(x)=x$, if $x$ is not rational, then $f(f(x))=f(1-x)=1-(1-x)=x$.

(b) If $x$ is rational, then $f(x)+f(1-x)=x+1-x=1$. If $x$ is irrational, then $f(x)+f(1-x)=1-x+1-(1-x)=1$.

(c) For $\varepsilon>0$, choose $\delta=\varepsilon$, if $|x-1/2|<\delta$, then $|f(x)-1/2|=|x-1/2|<\varepsilon$ regardless of whether $x$ is rational or not, so $f$ is continuous at $1/2$. For points $p\neq 1/2$, let $\varepsilon_0=|2p-1|/2>0$, then given any $\delta>0$, we can choose $q$ in $B(p;\delta)$, which satisfy the two conditions below: (1) $q$ is rational if $p$ is irrational, $q$ is irrational if $p$ is rational;(2) $|p+q-1|>\varepsilon_0$ since $|p+q-1|\to|2p-1|$ as $q\to p$. Now $|f(p)-f(q)|=|p+q-1|$, and we conclude $f$ is not continuous at $p$.

(d) Given any value $y\in[0,1]$, if $y$ is rational, then $f(y)=y$; if $y$ is irrational, then $1-y$ is irrational and $f(1-y)=y$.

(e) If both $x$ and $y$ are rational, then the conclusion is obvious. If $x$ is rational but $y$ is not, then $x+y$ is irrational and then
$$
f(x+y)-f(x)-f(y)=1-(x+y)-x-(1-y)=-2x\in\mathbf{Q}
$$
If $y$ is rational but $x$ is not, the proof is similar. If both $x$ and $y$ are irrational, then $x+y$ may be rational or irrational, thus
$$
f(x+y)-f(x)-f(y)=\begin{cases}
2(x+y)-2,&\quad x+y\in\mathbf{Q}
\\
-1, &\quad x+y\notin\mathbf{Q}
\end{cases}
$$
and the result is rational.

### 4.18

Let $f$ be defined on $\mathbf{R}$ and assume that there exists at least one point $x_0$ in $\mathbf{R}$ at where $f$ is continuous. Suppose also that, for every $x$ and $y$ in $\mathbf{R}$, $f$ satisfies the equation $f(x+y)=f(x)+f(y)$. Prove that there exists a constant $a$ such that $f(x) = ax$ for all $x$. 

#### Proof

From $f(x+y)=f(x)+f(y)$ we have $f(0)=0$ and $f(-x)=-f(x)$ for $x\in\mathbf{R}$. Also we have $f(x)=f(x-r)+f(r)=f(x+x_0-r)-f(x_0)+f(r)$ for any $r\in\mathbf{R}$, when $x\to r$, or $x+x_0-r\to x_0$, we have $f(x+x_0-r)\to f(x_0)$ since $f$ is continuous at $x_0$, and so $f(x)\to f(r)$, this shows $f$ is continuous on $\mathbf{R}$.

Use $f(x+y)=f(x)+f(y)$ we get $f(m)=mf(1)$ for any $m\in\mathbf{N}$, and $f(-m)=-f(m)=-mf(1)$, thus $f(m)=mf(1)$ for any integer $m$. If $n\in\mathbf{N}^+$, we have $f(1)=nf(1/n)$, thus given any $q\in\mathbf{Q}$, write $q=m/n$ with $n>0$, then
$$
f(q)=f\left(\dfrac{m}{n}\right)=mf\left(\dfrac{1}{n}\right)=\dfrac{m}{n}f(1)=qf(1)
$$
Let $a=f(1)$, we see that $f(x)=ax$ if $x\in\mathbf{Q}$, the conclusion follows since $f$ is continuous on $\mathbf{R}$.

### 4.19

Let $f$ be continuous on $[a,b]$ and define $g$ as follows: $g(a) = f(a)$ and, for $a<x\leq b$, let $g(x)$ be the maximum value of $f$ in the subinterval $[a,x]$. Show that $g$ is continuous on $[a,b]$.

#### Proof

$g$ is monotonic increasing, choose some $y\in[a,b]$, for any $\varepsilon>0$, as $f$ is continuous at $y$, we can find some $\delta$ such that $|f(x)-f(y)|<\varepsilon$ whenever $x\in B(y;\delta)\cap [a,b]$, we conclude $f(y)-\varepsilon<f(x)<f(y)+\varepsilon$ if $x\in B(y;\delta)\cap [a,b]$. Now consider the behavior of $g(x)$ when $x\in B(y;\delta)\cap [a,b]$.

For any $y-\delta<x<y$ such that $g(x)<g(y)$ , we can have $f(y)>f(z)$ for $z\in[a,x]$, or $f(y)>g(x)$, as $g(x)\geq f(x)>f(y)-\varepsilon$, and on the interval $[x,y]$ $f$ is restricted by $f(y)+\varepsilon$, thus $g(y)\leq f(y)+\varepsilon$, or $f(y)\ge g(y)-\varepsilon$, so we get
$$
g(y)-2\varepsilon\le f(y)-\varepsilon<g(x)<g(y)
$$
Similarly, for any $y<x<y+\delta$ such that $g(y)<g(x)$, we can get
$$
g(y)<g(x)<g(y)+2\varepsilon
$$
So whenever $x\in B(y;\delta)\cap [a,b]$, we have $|g(x)-g(y)|<2\varepsilon$, so $g$ is continuous.

### 4.20

Let $f_1, \dots,f_m$ be $m$ real-valued functions defined on a set $S$ in $\mathbf{R}^n$. Assume that each $f_k$ is continuous at the point $\mathbf{a}$ of $S$. Define a new function $f$ as follows: For each $\mathbf{x}$ in $S$, $f(x)$ is the largest of the $m$ numbers $f_1(\mathbf{x}),\dots, f_m(\mathbf{x})$. Discuss the continuity of $f$ at $\mathbf{a}$. 

#### Solution

For $\forall\varepsilon>0$, suppose $f(\mathbf{a})=f_k(\mathbf{a})$ for some integer $k$ between $1,\dots,m$, first suppose $k$ is the only integer which makes $f(\mathbf{a})=f_k(\mathbf{a})$, and without loss of generality we set $k=1$, let
$$
\varepsilon_0=\min\{\varepsilon, f(\mathbf{a})-f_2(\mathbf{a}),\dots,f(\mathbf{a})-f_m(\mathbf{a})\}/2
$$
since each $f_i$ is continuous at $\mathbf{a}$, we can find a $\delta$ such that whenever $|\mathbf{x}-\mathbf{a}|<\delta$, we can have $|f_i(\mathbf{x})-f_i(\mathbf{a})|<\varepsilon_0$, this means $f(\mathbf{x})=f_1(\mathbf{x})$ on $B(\mathbf{a};\delta)$, so $f$ is continuous at $\mathbf{a}$. 

If there is more than one integer $k$ that makes $f(\mathbf{a})=f_k(\mathbf{a})$, we prove $f$ is still continuous at $\mathbf{a}$ for the case of two integers, and cases for more than two integers up to $m$ integers can be proved similarly. Suppose we have  $f_l(\mathbf{a})=f_k(\mathbf{a})$ for $k\neq l$, then choose $\varepsilon_0$ in the way below:
$$
\varepsilon_0=\dfrac{\min(\varepsilon, \min_{i\neq k,l}\{f(\mathbf{a})-f_i(\mathbf{a})\})}{2}
$$
find a $\delta$ such that whenever $|\mathbf{x}-\mathbf{a}|<\delta$, we have $|f_i(\mathbf{x})-f_i(\mathbf{a})|<\varepsilon_0$, then the value of $f$ is only determined by $f_k,f_l$ on $B(\mathbf{a};\delta)$, since
$$
f_l(\mathbf{a})-\varepsilon_0<f_l(\mathbf{x})<f_l(\mathbf{a})+\varepsilon_0
\\
f_k(\mathbf{a})-\varepsilon_0<f_k(\mathbf{x})<f_k(\mathbf{a})+\varepsilon_0
$$
we have $f(\mathbf{a})-\varepsilon_0<f(\mathbf{x})<f(\mathbf{a})+\varepsilon_0$ when $\mathbf{x}\in B(\mathbf{a};\delta)$, thus $|f(\mathbf{x})-f(\mathbf{a})|<\varepsilon_0<\varepsilon$, and $f$ is continuous at $\mathbf{a}$.

### 4.21

Let $f:S\to\mathbf{R}$ be continuous on an open set $S$ in $\mathbf{R}^n$, assume that $p\in S$, and assume that $f(\mathbf{p})>0$. Prove that there is an $n$-ball $B(\mathbf{p};r)$ such that $f(\mathbf{x})>0$ for every $\mathbf{x}$ in the ball.  

#### Proof

Let $\varepsilon=f(\mathbf{p})/2>0$, then there is $r>0$ such that $|f(\mathbf{x})-f(\mathbf{p})|<\varepsilon$ whenever $|\mathbf{x}-\mathbf{p}|<r$, or $f(\mathbf{x})>f(\mathbf{p})-\varepsilon=f(\mathbf{p})/2>0$ whenever $\mathbf{x}\in B(\mathbf{p};r)$.

### 4.22

Let $f$ be defined and continuous on a closed set $S$ in $\mathbf{R}$. Let
$$
A=\{x:x\in S \text{ and }f(x)=0\}.
$$
Prove that $A$ is a closed subset of $\mathbf{R}$.

#### Proof

Let $p$ be an accumulation point of $A$, assume $p\notin A$, then $f(p)\neq 0$, since $f$ is continuous on $S$, $f$ is continuous at $p$ and thus there exists a ball $B(p;r)$ such that $f(x)\neq 0$ for every $x$ in the ball, thus $B(p;r)\cap A=\empty$, a contradiction. Thus $p\in A$ and $A$ is closed.

We can also use Theorem 4.24, and the fact that $A=f^{-1}(\{0\})$, and $\{0\}$ is a closed set in $\mathbf{R}$ to get $A$ being closed.

### 4.23

Given a function $f:\mathbf{R}\to\mathbf{R}$, define two sets $A$ and $B$ in $\mathbf{R}^2$ as follows: 
$$
A=\{(x,y):y<f(x)\},\quad B=\{(x,y):y>f(x)\}.
$$
Prove that $f$ is continuous on $\mathbf{R}$ if, and only if, both $A$ and $B$ are open subsets of $\mathbf{R}^2$.  

#### Proof

First suppose $f$ is continuous on $\mathbf{R}$, let $\mathbf{p}=(a,b)\in A$, then $b<f(a)$, let $\varepsilon=(f(a)-b)/2>0$, there is $\delta>0$ such that $|f(x)-f(a)|<\varepsilon$ whenever $x\in(a-\delta,a+\delta)$,  we can make $\delta<\varepsilon$,  consider the ball $B(\mathbf{p};\delta)$, for  $\forall(x,y)\in B(\mathbf{p};\delta)$, we have $|x-a|<\delta$ and $|y-b|<\delta$, thus
$$
y<b+\delta<b+\varepsilon=\dfrac{f(a)+b}{2}=f(a)-\varepsilon<f(x)
$$
which means $(x,y)\in A$, thus the ball $B(\mathbf{p};\delta)\subseteq A$ and $A$ is open. Similarly we can prove $B$ is open.

Conversely, if $A$ and $B$ are open, choose $x_0\in\mathbf{R}$, for any $\varepsilon>0$, consider the point $\mathbf{p}=(x_0, f(x_0)-\varepsilon/2)\in A$, as $A$ is open, there is a $r''>0$ which makes the ball $B(\mathbf{p};r)\subseteq A$, this means if $x\in(x_0-r'',x_0+r'')$, then $f(x)\ge f(x_0)-\varepsilon/2$, similarly, from $B$ being open we can find a $r'>0$ and $x\in(x_0-r',x_0+r')$ means $f(x)\le f(x_0)
+\varepsilon/2$. Let $r=\min(r',r'')$ we get
$$
f(x_0)-\dfrac{\varepsilon}{2}\le f(x)\le f(x_0)+\dfrac{\varepsilon}{2},\quad\forall x\in (x_0-r,x_0+r)
$$
this means $|f(x)-f(x_0)|<\varepsilon$ for all $x$ in $(x_0-r,x_0+r)$, thus $f$ is continuous at $x_0$. The conclusion follows as $x_0$ is arbitrarily chosen.

### 4.24

Let $f$ be defined and bounded on a compact interval $S$ in $\mathbf{R}$. If $T\subseteq S$, the num
$$
\Omega_f(T)=\sup\{f(x)-f(y):x\in T,y\in T\}
$$
is called the *oscillation* (or *span*) of $f$ on $T$. If $x\in S$, the oscillation of $f$ at $x$ is defined to be the number
$$
\omega_f(x)=\lim_{h\to 0+}\Omega_f(B(x;h)\cap S).
$$
Prove that this limit always exists and that $\omega_f(x) = 0$ if, and only if, $f$ is continuous at $x$.

#### Proof

Since $f$ is bounded, $\Omega_f(T)$ exists for any $T\subseteq S$, if we define $a_n=\Omega_f(B(x;1/n)\cap S)$ , then $\{a_n\}$ is a monotonic decreasing sequence bounded below by $0$, thus $\lim_{n\to\infty}a_n$ exists, and it is easy to see that $\omega_f(x)=\lim_{n\to\infty}a_n$.

If $f$ is continuous at $x$, then given $\forall\varepsilon>0$, there is $\delta>0$ such that $|f(y)-f(x)|<\varepsilon/2$ whenever $|y-x|<\delta$, this means
$$
\Omega_f(B(x;\delta)\cap S)<|f(x)+\varepsilon/2-(f(x)-\varepsilon/2)|=\varepsilon
$$
thus $\omega_f(x)=0$. Conversely, $\omega_f(x)=0$ means that given $\forall\varepsilon>0$, there is $\delta>0$ such that $\Omega_f(B(x;\delta)\cap S)<\varepsilon$, if $y\in B(x;\delta)\cap S$, we have
$$
|f(y)-f(x)|\leq\Omega_f(B(x;\delta)\cap S)<\varepsilon
$$
thus $f$ is continuous at $x$.

### 4.25

Let $f$ be continuous on a compact interval $[a, b]$. Suppose that $f$ has a local maximum at $x_1$ and a local maximum at $x_2$. Show that there must be a third point between $x_1$ and $x_2$ where $f$ has a local minimum.  NOTE: To say that $f$ has a local maximum at $x_1$ means that there is a $1$-ball $B(x_1)$ such that $f(x)\leq f(x_1)$ for all $x$ in $B(x_1)\cap [a, b]$. Local minimum is similarly defined.

#### Proof

Without loss of generality, we assume $x_1<x_2$ and find two $1$-balls $B(x_1;r_1)$ and $B(x_2;r_2)$ with $0<r_1,r_2<(x_2-x_1)/2$ and satisfy
$$
f(x)\leq f(x_1),x\in B(x_1;r_1)\cap[a,b]
\\
f(x)\leq f(x_2),x\in B(x_2;r_2)\cap[a,b]
$$
the interval $[x_1,x_2]$ is compact and $f$ is continuous on $[x_1,x_2]$, thus by Theorem 4.28 there exists a point $x_3\in[x_1,x_2]$ such that $f(x_3)=\inf f([x_1,x_2])$. If $x_3=x_1$, this means $f(x)$ is constant in $B(x_1)\cap[x_1,x_2]$, since $f(x)\leq f(x_1)$ and $f(x_1)\leq f(x)$ for all $x\in B(x_1)\cap[x_1,x_2]$, then we can let $x_3=x_1+r_1/2$ and still satisfy $f(x_3)=\inf f([x_1,x_2])$. Similarly we can move $x_3$ smaller than $x_2$ if originally $x_3=x_2$. Thus we conclude there exists a point $x_3\in(x_1,x_2)$ such that $f(x_3)=\inf f([x_1,x_2])$. Now let $r=\min(x_3-x_1,x_2-x_3)$, the ball $B(x_3;r)\subseteq[x_1,x_2]$ and $f(x_3)\leq f(x)$ for all $x\in B(x_3;r)$, which means f has a local minimum at $x_3$.

### 4.26

Let $f$ be a real-valued function, continuous on $[0, 1]$, with the following property:
For every real $y$, either there is no $x$ in $[0, 1]$ for which $f(x) = y$ or there is exactly one such $x$. Prove that $f$ is strictly monotonic on $[0, 1]$.  

#### Proof

We have $f(0)\neq f(1)$, suppose $f(0)<f(1)$, and we assume $f$ is not strictly monotonic increasing on $[0,1]$, then there exist $x,y\in[0,1]$ such that $x<y$ and $f(x)\ge f(y)$, we further get $f(x)>f(y)$ since $x$ is the only value for $f$ to get $f(x)$. We also have $x<1$ and $y>0$, and either $f(0)>f(y)$ or $f(0)<f(y)$.

If $f(0)>f(y)$, then $f(1)>f(y)$ and $f(x)>f(y)$ and $x<y<1$. We can choose $\varepsilon>0$ such that $f(y)+\varepsilon<f(x)$ and $f(y)+\varepsilon<f(1)$, then there shall be $a\in(x,y)$ and $b\in(y,1)$ such that $f(a)=f(b)=f(y)+\varepsilon$, this is a contradiction to $f$ being one-to-one. If $f(0)<f(y)$, then $f(0)<f(x)$ and $f(y)<f(x)$ and $0<x<y$. We can choose $\varepsilon>0$ such that $f(0)<f(x)-\varepsilon$ and $f(y)<f(x)-\varepsilon$, then there shall be $a\in(0,x)$ and $b\in(x,y)$ such that $f(a)=f(b)=f(x)-\varepsilon$, this is a contradiction to $f$ being one-to-one.

In conclusion, suppose $f(0)<f(1)$, then $f$ must be strictly monotonic increasing on $[0,1]$. Similarly, suppose  $f(0)>f(1)$, then $f$ must be strictly monotonic decreasing on $[0,1]$. 

### 4.27

Let $f$ be a function defined on $[0,1]$ with the following property: For every
number $y$, either there is no $x$ in $[0, 1]$ for which $f(x)=y$ or there are exactly two values of $x$ in $[0, 1]$ for which $f(x) = y$.

(a) Prove that $f$ cannot be continuous on $[0,1]$

(b) Construct a function $f$ which has the above property. 

(c) Prove that any function with this property has infinitely many discontinuities on $[0,1]$.

#### Proof

(a) Assume $f$ is continuous on $[0,1]$, let $M=\sup f([0,1])$ and $m=\inf f([0,1])$, then exists $a,b\in[0,1]$ such that $f(a)=M,f(b)=m$, then there exists $a',b'\in[0,1]$ such that $f(a)=f(a')=M$ and $f(b)=f(b')=m$. Obviously $M>m$, otherwise there are four points which has equal function value, thus $a,a',b,b'$ are four distinct points, since $f$ has a local maximum both at $a$ and at $a'$, by Exercise 4.25 $f$ has a local minimum at some $c$ between $a$ and $a'$, and $m\leq f(c)<M$. 

If one of $b,b'$ lies outside the interval between $a$ and $a'$, for example, $a<a'<b$, then there are three points which has function value $(M+f(c))/2$, one between $a$ and $c$, one between $a'$ and $c$, and one between $a'$ and $b$. Other cases when $b<a<a'$, or the interchange of $a'$ and $a$, the interchange of $b'$ and $b$, can be proved similarly.

If $a<b,b'<a'$ or $a'<b,b'<a$, then $f$ has a local maximum at some point $d$ between $b$ and $b'$, and $M\ge f(d)>m$, consider the value $(m+f(d))/2$, we can still find at least three distinct points which has function value of it.

We derived a contradiction as long as we assume $f$ is continuous.

(b) Let $\mathbf{Q}\cap[0,1]=\{q_1,q_2,\dots\}$ and define $f$ on $[0,1]$ as follows:
$$
f(x)=\begin{cases}
n,\quad &x=q_{2n}\text{ or }x=q_{2n+1}
\\
x,\quad &x\in[0,1/2]-\mathbf{Q}
\\
1-x,\quad &x\in[1/2,1]-\mathbf{Q}
\end{cases}
$$
(c) LEFT TO BE DONE.

### 4.28

In each case, give an example of a function $f$, continuous on $S$ and such that $f(S) = T$, or else explain why there can be no such $f$.
$$
\begin{aligned}&a)\quad S=(0,1),&&T=(0,1].
\\
&b)\quad S=(0,1),&&T=(0,1)\cup(1,2).
\\
&c)\quad S=\mathbf{R}^1,&&T=\text{the set of rational numbers}.
\\
&d)\quad S=[0,1]\cup[2,3],&&T=\{0,1\}.
\\
&e)\quad S=[0,1]\times[0,1],&&T=\mathbf{R}^2.
\\
&f)\quad S=[0,1]\times[0,1],&&T=(0,1)\times(0,1).
\\
&g)\quad S=(0,1)\times(0,1),&&T=\mathbf{R}^2.
\end{aligned}
$$

#### Solution

(a) $f(x)=\sin(\pi x)$.

(b) No, since $S$ is connected and $T$ is not.

(c) No, since $S$ is connected and $T$ is not.

(d) $f(x)=0,x\in[0,1]$ and $f(x)=1,x\in[2,3]$.

(e) No, since $S$ is compact and $T$ is not.

(f) No, since $S$ is compact and $T$ is not.

(g) $f(x,y)=(\cot\pi x,\cot\pi y)$.