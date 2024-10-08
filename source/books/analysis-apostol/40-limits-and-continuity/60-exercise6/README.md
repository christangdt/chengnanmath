# Exercise 50-59 (Uniform continuity and discontinuities)

### 4.50

Prove that a function which is uniformly continuous on $S$ is also continuous on $S$. 

#### Proof

Let $f$ be uniformly continuous on $S$ to $T$, then $\forall\varepsilon>0$, there exist $\delta>0$ such that $d_S(x,y)<\delta$ means $d_T(f(x),f(y))<\varepsilon$. Let $x_0\in S$, then whenever $d_S(x,x_0)<\delta$, we have $d_T(f(x),f(x_0))<\varepsilon$, this means $f$ is continuous at $x_0$.

### 4.51

If $f(x)=x^2$ for $x\in\mathbf{R}$, prove that $f$ is not uniformly continuous on $\mathbf{R}$.

#### Proof

Given $\varepsilon_0=1/2$, and the pair of points $(\sqrt{n},\sqrt{n+1})$, for any $\delta>0$, if $n$ is large enough, then $\sqrt{n+1}-\sqrt{n}=\frac{1}{\sqrt{n+1}+\sqrt{n}}<\delta$, but $|f(\sqrt{n+1})-f(\sqrt{n})|=1>\varepsilon_0$.

### 4.52

Assume that $f$ is uniformly continuous on a bounded set $S$ in $\mathbf{R}^n$. Prove that $f$ must be bounded on $S$.

#### Proof

Let $g$ be a function defined on $\overline{S}$ with $g(x)=f(x),x\in S$ and for $x\in S'$, define $g(x)=\lim_{z\to x}f(z)$. The definition is valid, since if $x\in S'$, then $\lim_{z\to x}f(z)=\lim_{n\to\infty}f(x_n)$ for any sequence $x_n\in S$ such that $x_n\to x$. For $\varepsilon >0$, from the uniformly continuity of $f$ we have $\|f(a)-f(b)\|<\varepsilon$ whenever $\|a-b\|<\delta$ for some $\delta$, thus as long as $m,n$ is large enough such that $x_m,x_n\in B(x;\delta/2)$, we have $\|f(x_n)-f(x_m)\|<\varepsilon$, so the sequence $\{f(x_n)\}$ is a Cauchy sequence, thus must converge. By definition, $g$ is continuous on $\overline{S}$, from $S$ is bounded we can see $\overline{S}$ is bounded, thus $\overline{S}$ is compact in $\mathbf{R}^n$. Then $g(\overline{S})$ is compact, thus is bounded, and $g(S)\subseteq g(\overline{S})$, this means $g(S)$ is bounded.

### 4.53

Let $f$ be a function defined on a set $S$ in $\mathbf{R}^n$ and assume that $f(S)\subseteq\mathbf{R}^n$. Let $g$ be defined on $f(S)$ with value in $\mathbf{R}^k$, and let $h$ denote the composite function defined by $h(x) = g[f(x)]$ if $x\in S$. If $f$ is uniformly continuous on $S$ and if $g$ is uniformly continuous on $f(S)$, show that $h$ is uniformly continuous on $S$.

#### Proof

For $\forall\varepsilon>0$, since $g$ is uniformly continuous on $f(S)$, we can find a $\delta_1>0$ such that $\|g(a)-g(b)\|<\varepsilon$ whenever $a,b\in f(S), \|a-b\|<\delta_1$,  since $f$ is uniformly continuous on $S$, we can find $\delta>0$ such that $\|f(x)-f(y)\|<\delta_1$ whenever $x,y\in S,\|x-y\|<\delta$, this means
$$
x,y\in S,\|x-y\|<\delta\implies\|g(f(x))-g(f(y))\|<\varepsilon
$$
So $h$ is uniformly continuous on $S$.

### 4.54

Assume $f : S \to T$ is uniformly continuous on $S$, where $S$ and $T$ are metric spaces. If $\{x_n\}$ is any Cauchy sequence in $S$, prove that $\{f(x_n)\}$ is a Cauchy sequence in $T$.

#### Proof

That $f$ is uniformly continuous on $S$ means for $\varepsilon>0$, there exists $\delta>0$ such that $d_S(x,y)<\delta\implies d_T(f(x),f(y))<\varepsilon$. For this $\delta$, we can find $N$ such that if $m,n>N$, we can have $d_S(x_m,x_n)<\delta$, thus if $m,n>N$, we can have $d_T(f(x),f(y))<\varepsilon$, thus $\{f(x_n)\}$ is a Cauchy sequence in $T$.

### 4.55

Let $f : S\to T$ be a function from a metric space $S$ to another metric space $T$.
Assume $f$ is uniformly continuous on a subset $A$ of $S$ and that $T$ is complete. Prove that there is a unique extension of $f$ to $\overline{A}$ which is uniformly continuous on $\overline{A}$.

#### Proof

Let $g$ be the extension of $f$ to $\overline{A}$ by define $g(x)=\lim_{y\to x}f(y)$ for $x\in A'-A$, with the proof of Exercise 4.52 we know that $g(x)\in T$. Given $\varepsilon >0$, we have $d_T(f(x),f(y))<\varepsilon$ whenever $x,y\in S,d_S(x,y)<\delta$, Now let $a,b\in\overline{A}$, to prove $g$ is uniformly continuous we break into cases:

**Case I**: $a,b\in A$, then as long as $d_S(a,b)<\delta$ we have $d_T(f(a),f(b))<\varepsilon$. 

**Case II**: one point in $A$ and one point in $A'-A$, suppose $a\in A$ and $b\in A'-A$, then first there exist $\delta'>0$ such that $d_T(g(x),g(b))<\varepsilon$ if $d_S(x,b)<\delta'$, now let $d_S(a,b)<\delta/2$, then choose some $x\in S$ which lies in $B(b;\delta/2)$ such that $d_S(x,b)<\delta'$, we can have
$$
d_S(a,x)\le d_S(a,b)+d_S(x,b)<\delta/2+\delta/2=\delta
$$
which implies $d_T(g(a),g(x))<\varepsilon$, thus $d_T(g(a),g(b))<2\varepsilon$.

**Case III** : $a,b\in A'-A$, then there exists $\delta_1>0,\delta_2>0$ such that
$$
d_S(x,a)<\delta_1\implies d_T(g(x),g(a))<\varepsilon
\\
d_S(x,b)<\delta_2\implies d_T(g(x),g(b))<\varepsilon
$$
now let $d_S(a,b)<\delta/3$, choose some $x_1\in A$ which lies in $B(a;\delta/3)$ such that $d_S(x_1,a)<\delta_1$, choose some $x_2\in A$ which lies in $B(b;\delta/3)$ such that $d_S(x_2,b)<\delta_2$, notice that $d_S(x_1,x_2)<\delta$, then we have
$$
\begin{aligned}
d_T(g(a),g(b))&\le d_T(g(a),g(x_1))+d_T(g(x_1),g(x_2))+d_T(g(x_2),g(b))
\\
&\le\varepsilon+\varepsilon+\varepsilon=3\varepsilon
\end{aligned}
$$
In conclusion, for any $\varepsilon>0$, we select the $\delta$ according to the uniformly continuity of $f$, then for $g$, we only need to limit $d_S(a,b)<\delta/3$ to guarantee $d_T(g(a),g(b))<3\varepsilon$ for any $a,b\in\overline{A}$, this shows $g$ is uniformly continuous on $\overline{A}$.

To prove $g$ is unique, any extension of $f$ which is different from $g$ must have different value on at least one accumulation point $p$ of $S$. Then suppose $h$ is an extension of $f$ on $\overline{A}$, and $h(p)\neq g(p)$, let $\varepsilon_0=d_T(h(p),g(p))/2$, then there is a ball $B(p;r)$ such that $d(g(p),h(x))<\varepsilon_0$ whenever $x\in B(p;r)\cap A$ by the definition of $g(p)$ and $h(x)=f(x)$ on $A$. This means $d_T(h(x),h(p))>\varepsilon_0$  whenever $x\in B(p;r)\cap A$, this means $h$ is not continuous at $p$, thus not uniformly continuous on $\overline{A}$.

### 4.56

In a metric space $(S, d)$, let $A$ be a nonempty subset of $S$. Define a function $f_A:S\to\mathbf{R}$ by the equation
$$
f_A=\inf\{d(x,y):y\in A\},x\in S
$$
  The number $f_A(x)$ is called the distance from $x$ to $A$.

(a) Prove $f_A$ is uniformly continuous on $S$.

(b) Prove that $\overline{A}=\{x:x\in S\text{ and }f_A(x)=0\}$.

#### Proof

(a) For $\varepsilon>0$, let $\delta=\varepsilon/2$, if $a,b\in S$ and $d(a,b)<\delta$, then we first can find $a'\in A$ such that $d(a,a')<f_A(a)+\varepsilon/2$, then
$$
f_A(b)\le d(b,a')\le d(a,b)+d(a,a')<f_A(a)+\varepsilon
$$
similarly we can have $f_A(a)<f_A(b)+\varepsilon$, thus $|f_A(a)-f_A(b)|<\varepsilon$ whenever $d(a,b)<\delta$, which means $f_A$ is uniformly continuous on $S$.

(b) If $p\in\overline{A}$, then $f_A(p)=0$, otherwise in the ball $B(p;f_A(p)/2)$ there will be no point in $A$, a contradiction to $p$ being an accumulation point of $A$. Conversely if $f_A(p)=0$ for some $p\in S$, then for any $r>0$, there exist $a\in A$ such that $d(a,p)<r$, thus $p\in\overline{A}$.

### 4.57

In a metric space $(S, d)$, let $A$ and $B$ be disjoint closed subsets of $S$. Prove that there exist disjoint open subsets $U$ and $V$ of $S$ such that $A\subseteq U$ and $B\subseteq V$.  

#### Proof

Let $g(x)=f_A(x)-f_B(x)$, by Exercise 4.56, $g$ is uniformly continuous on $S$, and we have
$$
A=\{x\in S,f_A(x)=0\},\quad B=\{x\in S,f_B(x)=0\}.
$$
Also since $A\cap B=\empty$, if $x\in A$ then $x\notin B$, thus $x\notin B'$, which means $f_B(x)>0$, similarly $f_A(y)>0,y\in A$, thus if we let $U=g^{-1}(-\infty,0), V=g^{-1}(0,+\infty)$, then $A\subseteq U$ and $B\subseteq V$, and both $U$ and $V$ are open by the continuity of $g$. To see $U\cap V=\empty$, assume $s\in U\cap V$, then $s\in U$ means $g(s)<0$, $s\in V$ means $g(s)>0$, which is a contradiction.

### 4.58

Locate and classify the discontinuities of the functions $f$ defined on $\mathbf{R}$ by the following equations: 
$$
\begin{aligned}
&a)\quad f(x)=(\sin{x})/x\quad&&\text{if }x\neq0,f(0)=0.
\\
&b)\quad f(x)=e^{1/x}\quad&&\text{if }x\neq0,f(0)=0.
\\
&c)\quad f(x)=e^{1/x}+\sin(1/x)\quad&&\text{if }x\neq0,f(0)=0.
\\
&d)\quad f(x)=1/(1-e^{1/x})\quad&&\text{if }x\neq0,f(0)=0.
\end{aligned}
$$

#### Solution

(a) Discontinuity at $x=0$, which is a removable discontinuity since $f(0+)=f(0-)=1$.

(b) Discontinuity at $x=0$, which is a irremovable discontinuity since $f(0+)$ does not exist and $f(0-)=0$.

(c) Discontinuity at $x=0$, which is a irremovable discontinuity since $f(0+)$ and $f(0-)$ does not exist.

(d) Discontinuity at $x=0$, which is a irremovable jump discontinuity since $f(0+)=0$ and $f(0-)=1$.

### 4.59

Locate the points in $\mathbf{R}$ at which each of the functions in Exercise 4.11 is not continuous. 

#### Solution

Omitted. 