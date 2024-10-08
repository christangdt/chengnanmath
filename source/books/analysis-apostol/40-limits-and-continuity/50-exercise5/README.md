# Exercise 36-49 (Connectedness)

### 4.36

Prove that a metric space $S$ is disconnected if, and only if, there is a nonempty subset $A$ of $S$, $A\neq S$, which is both open and closed in $S$.

#### Proof

If $S$ is disconnected, then there exist nonempty open sets $A$ and $B$ such that $S=A\cup B$ and $A\cap B=\empty$, we claim $A$ is also closed, let $p\notin A$, then $p\in B$, since $B$ is open, there is some $r>0$ such that $B(p;r)\subseteq B$, as $A\cap B=\empty$, this means $p$ is not an accumulation point of $A$. Thus all accumulation point of $A$ lies in $A$.

Conversely, if there is $A$ not empty, $A\neq S$ such that $A$ is both closed and open, let $B=S-A$, then $S=A\cup B$ and $A\cap B=\empty$, from $A$ being closed we know $B$ is open, and we conclude $S$ is disconnected.

### 4.37

Prove that a metric space $S$ is connected if, and only if, the only subsets of $S $ which
are both open and closed in $S$ are the empty set and $S$ itself.

#### Proof

If $S$ is connected, and assume there exist $A\subseteq S$ which is both open and closed in $S$, but neither empty nor $S$ itself, then $A$ satisfy the condition in Exercise 4.36, we can say $S$ is disconnected and get a contradiction. Conversely, if the only subsets of $S $ which are both open and closed in $S$ are the empty set and $S$ itself, then $S$ must be connected, otherwise we can find some nonempty subset $A$ of $S$, $A\neq S$, which is both open and closed in $S$.

### 4.38

Prove that the only connected subsets of $\mathbf{R}$ are (a) the empty set, (b) sets consisting of a single point, and (c) intervals (open, closed, half-open, or infinite). 

#### Proof

It is easy to verify (a),(b) and (c) are connected subsets. To see these are the only subsets of $\mathbf{R}$, we only need to prove if $S$ is connected and $a,b\in S,a\neq b$, then all points between $a$ and $b$ belong to $S$. Suppose $a<b$ and $c\in (a,b)$ with $c\notin S$, then let $A=(-\infty,c)\cap S$ and $B=(c,+\infty)\cap S$, we have $A\cup B=S$, since $a\in A$ and $b\in B$, both $A$ and $B$ are nonempty, obviously $A\cap B=\empty$ and both are open in $S$, this means $S$ is disconnected, a contradiction.

### 4.39

Let $X$ be a connected subset of a metric space $S$. Let $Y$ be a subset of $S$ such that $X\subseteq Y\subseteq\overline{X}$, where $\overline{X}$ is the closure of $X$. Prove that $Y$ is also connected. In particular, this shows that $\overline{X}$ is connected.

#### Proof

 Let $f$ be a two-value function on $Y$, then $f$ is constant on $X$ since $X$ is connected. Suppose $f(x)=c,x\in X$, for $y\in Y,y\notin X$, we see that $y$ is an accumulation point of $X$, if $f(y)\neq c$, then $f$ cannot be continuous at $y$, a contradiction. Thus $f(x)=c$ for $x\in Y$, this means $Y$ is connected.

### 4.40

If $x$ is a point in a metric space $S$, let $U(x)$ be the component of $S$ containing $x$.
Prove that $U(x)$ is closed in $S$.  

#### Proof

Let $p$ be an accumulation point of $U(x)$ and let $f$ be a two-value function on $U(x)\cup\{p\}$, we shall prove $f$ is constant and the set $U(x)\cup\{p\}$ is connected, by definition of $U(x)$ it means $p\in U(x)$. Suppose $f(x)=c$ on $U(x)$, as $p$ is an accumulation point of $U(x)$, we can find some $\{x_n\}$ approaches $p$ close enough such that $|f(p)-f(x_n)|<\varepsilon$ for any $\varepsilon >0$, it follows that $f(p)=c$, and the proof is complete.

### 4.41

Let $S$ be an open subset of $\mathbf{R}$. By Theorem 3.11, $S$ is the union of a countable disjoint collection of open intervals in $\mathbf{R}$. Prove that each of these open intervals is a component of the metric subspace $S$. Explain why this does not contradict Exercise 4.40. 

#### Proof

Let $S=\bigcup_{n=1}^{\infty}I_n$. By Exercise 4.38, each of these open interval $I_n$ is connected, and $I_n\cap I_m=\empty$ if $n\neq m$. Assume some $I_n$ is not a component of $S$, then we can find some component $U$ of $S$ such that $I_n\subsetneq U$, since $I_n$ itself is connected. Let $x\in U-I_n$, consider $U(x)$ which is the component of $S$ containing $x$, as $x\in U$, we have $U(x)\subseteq U$, as $x\in S,x\notin I_n$, we can find some $m\neq n$ such that $x\in I_m$, then $I_m$ and $U$ are two connected sets both contain $x$, so $U\cup I_m\subseteq U(x)\subseteq U$, we can get $I_m\subseteq U$. This means $I_n\cup I_m\subseteq U$, we can further deduce $I_n\cup I_m\subseteq\text{int }U$, since $U\subseteq S$, $U$ contains at least two distinct open intervals, $U$ is an interval in $\mathbf{R}$, thus $\text{int }U$ is an open interval belonging to $S$, and $I_n\subsetneq \text{int }U$, it contradicts the definition of component interval ($I_n$ is a component interval means no open interval $J\neq I_n$ can have $I_n\subseteq J\subseteq S$, but $\text{int }U$ does).

This does not contradict Exercise 4.40 since each $I_n$ is open in $\mathbf{R}$ but not open relative to $S$.

### 4.42

Given a compact set $S$ in $\mathbf{R}^n$ with the following property: For every pair of points $\mathbf{a}$ and $\mathbf{b}$ in $S$ and for every $\varepsilon>0$ there exists a finite set of points $\{\mathbf{x}_0,\mathbf{x}_1,\dots,\mathbf{x}_n\}$ in $S$ with $\mathbf{x}_0=\mathbf{a}$ and $\mathbf{x}_n=\mathbf{b}$ such that
$$
\|\mathbf{x}_k-\mathbf{x}_{k-1}\|<\varepsilon,\quad k=1,2,\dots,n
$$
Prove or disprove: $S$ is connected.

#### Proof

Assume $S$ is not connected, then there exist nonempty disjoint open sets $A$ and $B$ such that $S=A\cap B$. Choose $\mathbf{a}\in A$ and $\mathbf{b}\in B$, we form two sequences $\{\mathbf{y}_n\}$ in $A$  and $\{\mathbf{z}_n\}$ in $B$ like this: for $n\in\mathbf{N}$, we can find a finite set of points $\{\mathbf{x}_0=\mathbf{a},\mathbf{x}_1,\dots,\mathbf{x}_m=\mathbf{b}\}$ in $S$ such that $\|\mathbf{x}_k-\mathbf{x}_{k-1}\|<1/n$, since $A\cap B=\empty$, we select some $k$ such that $\mathbf{x}_k\in A$ and $\mathbf{x}_{k+1}\in B$, it is always possible to find such a $k$ since $\mathbf{x}_0\in A$ and $\mathbf{x}_{m}\in B$. We let $\mathbf{y}_n=\mathbf{x}_k$ and $\mathbf{z}_n=\mathbf{x}_{k+1}$, then $\|\mathbf{y}_n-\mathbf{z}_{n}\|<1/n$ for all $n$. As $S$ is compact, both  $\{\mathbf{y}_n\}$ and  $\{\mathbf{z}_n\}$ has convergent subsequence which converges in $S$, let $\mathbf{y}_{n_k}\to y$ and $\mathbf{z}_{n_k}\to z$, since both $A$ and $B$ are closed in $S$ (by Exercise 4.36), we have $y\in A$ and $z\in B$, thus $y\neq z$. Consider $y\in A$, we can find a ball $B(y;r)\subseteq A$ as $A$ is open, thus there are no points of $B$ in this ball, but if we choose $N$ enough such that $1/N<r/2$, there exist $K$ such that $n_K>N$ and $\|\mathbf{y}_{n_K}-y\|<r/2$, this means
$$
\|\mathbf{z}_{n_K}-y\|\le\|\mathbf{z}_{n_K}-\mathbf{y}_{n_K}\|+\|\mathbf{y}_{n_K}-y\|<\dfrac{1}{n_K}+\dfrac{r}{2}<r
$$
thus $\mathbf{z}_{n_K}\in B(y;r)\subseteq A$, a contradiction to $A\cap B=\empty$.

### 4.43

Prove that a metric space $S$ is connected if, and only if, every nonempty proper
subset of $S$ has a nonempty boundary.  

#### Proof

If $S$ is connected, assume there is $A\subsetneq S$ which is nonempty but has empty boundary, let $B=S-A$, since $\partial{A}=\overline{A}\cap\overline{B}=\empty$, we have $A\cap\overline{B}=\empty$, thus if $a\in A$, then $a$ is not an accumulation point of $B$, meaning there is a ball $B(a;r)$ which has no points of $B$, thus $a$ is an interior point of $A$, it means $A$ is open, similarly we can prove $B$ is open. Now from $A\cup B=S$ and $A\cap B=\empty$ we deduce $S$ being disconnected, a contradiction. 

Conversely, if every nonempty proper subset of $S$ has a nonempty boundary. Assume $S$ is disconnected and $A,B$ be nonempty open sets in $S$ which satisfy $A\cap B=\empty$ and $A\cup B=S$, then $A$ is a proper subset of $S$ since $B$ is nonempty, and $\partial{A}$ must be empty, since any point belongs to $\partial{A}$ must belong to either $A$ or $B$ since $A\cup B=S$, but belonging to $A$ means it cannot belong to $\overline{B}$ as $A$ is open, and vice versa. We obtain a nonempty proper subset of $S$ which has empty boundary, a contradiction.

### 4.44

Prove that every convex subset of $\mathbf{R}^n$ is connected. 

#### Proof

A convex subset of $\mathbf{R}^n$ is arcwise connected, thus connected.

### 4.45

Given a function $\mathbf{f}:\mathbf{R}^n\to\mathbf{R}^m$ which is one-to-one and continuous on $\mathbf{R}^n$. If $A$ is open and disconnected in $\mathbf{R}^n$, prove that $\mathbf{f}(A)$ is open and disconnected in $\mathbf{f}(\mathbf{R}^n)$.

#### Proof

$\mathbf{f}(A)$ is open by the continuity of $\mathbf{f}$. Since $A$ is disconnected, we have $A=B\cup S$ for open set $B$ and $S$ with $B\cap S=\empty$. Both $\mathbf{f}(B)$ and $\mathbf{f}(S)$ are open, and $\mathbf{f}(B)\cap \mathbf{f}(S)=\empty$ since $\mathbf{f}$ is one-to-one, obviously $\mathbf{f}(B)\cup\mathbf{f}(S)=\mathbf{f}(A)$. Thus $\mathbf{f}(A)$ is disconnected.

### 4.46

Let $A=\{(x,y):0<x\le1,y=\sin{1/x}\}, B=\{(x,y):y=0,-1\le x\le0\}$, and let $S=A\cup B$. Prove that $S$ is connected but not arcwise connected.

#### Proof

To see $S$ is connected, let $f$ be a two-value function on $S$, then $f$ is constant on $A$ and constant on $B$, since two points both in $A$ can be arbitrarily close, so is two points in $B$. Also notice that $(0,0)\in B$ is an accumulation point of $A$, thus we can select $a\in A$ which is close enough to $(0,0)$, thus $f(a)=f(0,0)$. It follows that $S$ is a connected set.

To see $S$ is not arcwise connected, assume there is a continuous function $\mathbf{f}:[0,1]\to S$ such that $\mathbf{f}(0)=(0,0)$ and $\mathbf{f}(1)=(1,\sin1)$, then for $\varepsilon=1/2$, there is a $\delta>0$ such that $\|\mathbf{f}(x)-(0,0)\|<\varepsilon$ whenever $0<x<\delta$, choose $N$ large enough so that $1/(2N\pi)<\delta$, let
$$
p=\dfrac{1}{2N\pi},\quad q=\dfrac{1}{(2N+1)\pi},\quad r=\dfrac{1}{(2N+\frac{1}{2})\pi}
$$
define $S'=\mathbf{f}([q,p])$, then $S'$ is connected since the interval $[q,p]$ is connected in $[0,1]$ and $\mathbf{f}$ is continuous. we define
$$
U=\{(x,y):x<r\}\cap S',\quad V=\{(x,y):x>r\}\cap S'
$$
then $U,V$ are open in $S$ since $\{(x,y):x<r\}$ and $\{(x,y):x>r\}$ are open in $\mathbf{R}^2$, and $U\cap V=\empty$, to see $U\cup V=S'$, notice when $x=r$, the only point possibly in $S$ is the point $(r,1)\in S$, but $(r,1)\notin S'$ since $\|\mathbf{f}(x)\|<1/2$ whenever $x\in[q,p]$, since the point $(p,0)\in U$ and $(q,0)\in V$, both $U$ and $V$ are nonempty, we conclude the set $S'$ is disconnected, a contradiction.

### 4.47

Let $F=\{F_1,F_2,\dots\}$ be a countable collection of connected compact sets in $\mathbf{R}^n$ such that $F_{k+1}\subseteq F_k$ for each $k\ge1$. Prove that the intersection $\bigcap_{k=1}^{\infty}F_k$ is connected and closed.

#### Proof

If some $F_i$ is empty, then $\bigcap_{k=1}^{\infty}F_k$ is empty and there is nothing to prove. Suppose $F_n\neq\empty$ for all $n$, since compact sets in $\mathbf{R}^n$ are closed and bounded, use the Cantor intersection theorem we can see $\bigcap_{k=1}^{\infty}F_k$ is closed and nonempty, thus compact. 

To prove $\bigcap_{k=1}^{\infty}F_k:=F$ is connected, assume it is not, then there exists nonempty open sets $U$ and $V$ in $F$ such that $F=U\cup V$ and $U\cap V=\empty$. Since $U$ and $V$ are open in $F$, for each $\mathbf{u}\in U$ there exists a ball $B(\mathbf{u};r_{\mathbf{u}})\cap F\subseteq U$, and for each $\mathbf{v}\in V$ there exists a ball $B(\mathbf{v};r_{\mathbf{v}})\cap F\subseteq V$. Consider the balls $B(\mathbf{u};r_{\mathbf{u}}/2)$ and $B(\mathbf{v};r_{\mathbf{v}}/2)$ where $\mathbf{u}\in U$ and $\mathbf{v}\in V$, then
$$
\mathbf{w}\in B(\mathbf{u};r_{\mathbf{u}}/2)\cap B(\mathbf{v};r_{\mathbf{v}}/2)\implies\|\mathbf{u}-\mathbf{v}\|<\dfrac{r_{\mathbf{u}}+r_{\mathbf{v}}}{2}\le\max(r_{\mathbf{u}},r_{\mathbf{v}})
$$
but $B(\mathbf{u};r_{\mathbf{u}})\cap V=\empty$ and $B(\mathbf{v};r_{\mathbf{v}})\cap U=\empty$, so $\|\mathbf{u}-\mathbf{v}\|\ge r_{\mathbf{u}}$ and $\|\mathbf{u}-\mathbf{v}\|\ge r_{\mathbf{v}}$, this is a contradiction, so no such $\mathbf{w}$ exists, thus we can prove that 
$$
B(\mathbf{u};r_{\mathbf{u}}/2)\cap B(\mathbf{v};r_{\mathbf{v}}/2)=\empty, \quad\forall\mathbf{u}\in U, \forall\mathbf{v}\in V
$$
Define 
$$
U'=\bigcup_{\mathbf{u}\in U}B(\mathbf{u};r_{\mathbf{u}}/2),\quad V'=\bigcup_{\mathbf{v}\in V}B(\mathbf{v};r_{\mathbf{v}}/2)
$$
then both $U'$ and $V'$ are nonempty, open in $\mathbf{R}^n$, and $U'\cap V'=\empty$, and $A:=U'\cup V'$ is an open cover of $F$. 

Assume now that $F_n\nsubseteq A$ for all $n$, then for each $n$ there exists a $\mathbf{x}_n\in F_n\backslash A$, the sequence $\{\mathbf{x}_n\}$ is in $F_1$ which is compact, thus $\{\mathbf{x}_n\}$ has a convergent subsequence $\{\mathbf{x}_{n_k}\}$, define $\mathbf{x}:=\lim_{k\to\infty}\mathbf{x}_{n_k}$, it is easy to see that for any fixed integer $N$, $\mathbf{x}$ is a limit point of $F_N$, since every neighborhood of $\mathbf{x}$ contains infinitely many points of $\{\mathbf{x}_{n_k}\}$, for $k$ large enough we can have $n_k>N$ and $\mathbf{x}_{n_k}\in F_{n_k}\subseteq F_N$, given $F_N$ being compact (thus closed), we deduce $\mathbf{x}\in F_N$, then we can conclude $\mathbf{x}\in\bigcap_{k=1}^{\infty}F_k\subseteq A$. As $A$ is open, there exists some ball $B(\mathbf{x};r)\subseteq A$, but in this ball we can always find a point $\mathbf{x}_n$ chosen from the sequence $\{\mathbf{x}_{n_k}\}$, and this point has the property $\mathbf{x}_n\in A$, this is a contradiction. Thus we can find at least one integer $M$ such that $F_M\subseteq A$.

Finally, as $F_M$ is covered by $A$, form open sets $U'\cap F_M$ and $V'\cap F_M$ in $F_M$, since $U'$ and $V'$ contains points in $F$ (which is a subset of $F_M$), both $U'\cap F_M$ and $V'\cap F_M$ is nonempty, also
$$
(U'\cap F_M)\cap(V'\cap F_M)=(U'\cap V')\cap F_M=\empty
\\
(U'\cap F_M)\cup(V'\cap F_M)=(U'\cup V')\cap F_M=F_M
$$
this means $F_M$ is not connected, a contradiction.

### 4.48

Let $S$ be an open connected set in $\mathbf{R}^n$. Let $T$ be a component of $\mathbf{R}^n-S$. Prove that $\mathbf{R}^n-T$ is connected.

#### Proof

If $S=\empty$, then $\mathbf{R}^n-T=\empty$ and there is nothing to prove. The same if $S=\mathbf{R}^n$. Now suppose $S$ and $\mathbf{R}^n-S$ are both nonempty, write $\mathbf{R}^n-S=\bigcup_{x\in\mathbf{R}^n-S}C(x)$, where $C(x)$ is a component of $\mathbf{R}^n-S$ that contains $x$. Let $p\in\mathbf{R}^n-S$ such that $T=C(p)$, then
$$
\mathbf{R}^n-T=S\cup\left(\bigcup_{x\in\mathbf{R}^n-S-T}C(x)\right)
$$
We first show that for any $x\in\mathbf{R}^n-S-T$, the component $C(x)$ contains at least a limit point of $S$. Assume not, then $C(x)\subseteq\mathbf{R}^n-\bar{S}$, which is an open set, as $C(x)$ is itself a connected set, there exists a component $V$ of $\mathbf{R}^n-\bar{S}$ which is open and contains $C(x)$, this means $V$ is a connected set in $\mathbf{R}^n-\bar{S}\subseteq\mathbf{R}^n-{S}$, thus $V\subseteq C(x)$ and so $V=C(x)$, which means $C(x)$ is open. The definition of component guarantees that $\overline{C(x)}=C(x)$, which means $C(x)$ is closed. This is impossible since $C(x)$ is nonempty and $C(x)\ne\mathbf{R}^n$.

Given a two-valued function $f$ on $\mathbf{R}^n-T$, we can prove $f$ is constant, since for $\forall a,b\in\mathbf{R}^n-T$, if $a,b\in S$, then $f(a)=f(b)$. If $a\in S$ and $b$ is in some $C(x)$, then choose a limit point $s$ of $S$ in $C(x)$, we have $f(b)=f(s)$ by $C(x)$ being connected, and $f(s)=f(a)$ by choosing some $s_n\to s$ and $f(a)=f(s_n)$ and the continuity of $f$. If $a,b$ are in different $C(x)$, choose some $s\in S$ and we shall have $f(a)=f(s)=f(b)$. Thus $f$ is constant on $\mathbf{R}^n-T$, then use Theorem 4.36.

### 4.49

Let $(S,d)$ be a connected metric space which is not bounded. Prove that for every $a$ in $S$ and every $r>0$, the set $\{x:d(x,a)=r\}$ is nonempty.

#### Proof

Assume there exist $a\in S,r>0$ such that the set $\{x:d(x,a)=r\}$ is empty. Then we define
$$
A=\{x\in S:d(x,a)<r\},\quad B=\{x\in S:d(x,a)>r\}
$$
Since $d(a,a)=0<r$, we have $a\in A$, if $B=\empty$, then $S=A$, which means $S$ is bounded, but the condition says $S$ is not bounded, thus $B$ is nonempty. Obviously both $A$ and $B$ are open, and $A\cup B=S$ and $A\cap B=\empty$, then $S$ is disconnected, a contradiction.