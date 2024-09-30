# Exercise 8-16 (Open and closed sets in Rn)

### 3.8

Prove that open $n$-balls and $n$-dimensional open invervals are open sets in $\mathbf{R}^n$.

#### Proof

Let $B(\mathbf{x};r)$ be an open $n$-ball, choose any $\mathbf{y}\in B(\mathbf{x};r)$, we have $d:=\|\mathbf{x}-\mathbf{y}\|<r$, let $r'=\min(d,r-d)$, then $B(\mathbf{y};r')\subseteq B(\mathbf{x};r)$, thus $\mathbf{y}$ is an interior point of $B(\mathbf{x};r)$, and $B(\mathbf{x};r)$ is open.

For any $n$-dimensional open interval $(x_1,y_1)\times\cdots\times(x_n,y_n)$, given any point $\mathbf{p}=(p_1,\dots,p_n)$ we have $x_i<p_i<y_i$ for $i=1,\dots,n$. Define
$$
d_i=\min(p_i-x_i,y_i-p_i),i=1,\dots,n\qquad
r=\dfrac{\min_{1\leq i\leq n}d_i}{\sqrt{n}}
$$
then the ball $B(\mathbf{p};r)$ lies in the open interval $(x_1,y_1)\times\cdots\times(x_n,y_n)$, thus the open interval is open in $\mathbf{R}^n$.

### 3.9

Prove that the interior of a set in $\mathbf{R}^n$ is open in $\mathbf{R}^n$.

#### Proof

Let $S$ be a set in $\mathbf{R}^n$, and let $S_0$ be the interior of $S$. For any $\mathbf{x}\in S_0$, $\mathbf{x}$ is an interior point of $S$, thus there is $B(\mathbf{x},r)\subseteq S$, this means any point $\mathbf{y}\in B(\mathbf{x},r/2)$, the ball $B(\mathbf{y},r/2)$ lies in $S$, thus $\mathbf{y}\in S_0$ and so $\mathbf{x}$ is an interior point of $S_0$, which means $S_0$ is open.

### 3.10

If $S\subseteq\mathbf{R}^n$, prove that int $S$ is the union of all open subsets of $\mathbf{R}^n$ which are contained in $S$. This is described by saying that int $S$ is the largest open subset of $S$.

#### Proof

Apparently int $S$ is an open subset contained in $S$. To prove the converse, for any point which belongs to the union of all open subsets of $\mathbf{R}^n$ containted in $S$, it must belong to at least one open subset of $S$, thus it is an interior point of $S$, and belongs to int $S$.

### 3.11

If $S$ and $T$ are subsets of $\mathbf{R}^n$, prove that
$$
(\text{int }S)\cap(\text{int }T)=\text{int }(S\cap T)\quad\text{and}\quad(\text{int }S)\cup(\text{int }T)\subseteq\text{int }(S\cup T)
$$

#### Proof

To prove the first conclusion, if $\mathbf{x}\in(\text{int }S)\cap(\text{int }T)$, then $\mathbf{x}$ is an interior point of $S$ and $T$, thus we can find $B(\mathbf{x},r)\subseteq S$ and $B(\mathbf{x},r')\subseteq T$, let $R=\min\{r,r'\}$, we have $B(\mathbf{x},R)\subseteq S\cap T$. Conversely, if $\mathbf{x}\subseteq S\cap T$, we find $B(\mathbf{x},r)\subseteq S\cap T$, this means $\mathbf{x}$ is both an interior point of $S$ and an interior point of $T$.

To prove the second conclusion, let $\mathbf{x}\in(\text{int }S)\cup(\text{int }T)$, then $\mathbf{x}$ is either an interior point of $S$, or an interior point of $T$, we can find some ball centered in $\mathbf{x}$, and is either totally in $S$, or totally in $T$, thus always totally in $S\cup T$, and the conclusion follows.

### 3.12

Let $S'$ denote the derived set and $\overline{S}$ the closure of a set $S$ in $\mathbf{R}^n$. Prove that:

a) $S'$ is closed in $\mathbf{R}^n$; that is, $(S')'\subseteq S'$.

b) If $S\subseteq T$, then $S'\subseteq T'$.

c) $(S\cup T)'=S'\cup T'$.

d) $(\overline{S})'=S'$

e) $\overline{S}$ is closed in $\mathbf{R}^n$.

f) $\overline{S}$ is the intersection of all closed subsets of $\mathbf{R}^n$ containing $S$. That is, $\overline{S}$ is the smallest closed set containing $S$.

#### Proof

a) Let $\mathbf{x}\in (S')'$, then any $n$-ball $B(\mathbf{x},r)$ contains one point $\mathbf{y}\neq\mathbf{x},\mathbf{y}\in S'$, let $R=\min(|\mathbf{y}-\mathbf{x}|,r-|\mathbf{y}-\mathbf{x}|)$, then $B(\mathbf{y},R)\subseteq B(\mathbf{x},r)$ and $\mathbf{x}\notin B(\mathbf{y},R)$, and there exists one point of $S$ distinct from $\mathbf{y}$ which is contained in $B(\mathbf{y},R)$, thus in $B(\mathbf{x},r)$, since this $B(\mathbf{x},r)$ is arbitrary, we conclude $\mathbf{x}$ is an accumulation point of $S$.

b) If $\mathbf{x}\in S'$, then for any $n$-ball $B(\mathbf{x})$, it contains at least one point of $S$ distinct from $\mathbf{x}$, thus one point of $T$ distinct from $\mathbf{x}$, thus $\mathbf{x}\in T'$.

c) Let $\mathbf{x}$ be an accumulation point of $S\cup T$, then for each $n$-ball of $\mathbf{x}$ there is a point of $S\cup T$ distinct from $\mathbf{x}$. Now if $\mathbf{x}\notin S'$, then there is a $n$-ball $B$ such that no point in $S$ is in, this means $\mathbf{x}\in T'$, since for each $n$-ball contained in $B$ shall contain a point of $T$.

d) We use $\overline{S}=S\cup S'$, by (c) $(\overline{S})'=S'\cup(S')'$, by (a) $(S')\subseteq S'$, thus $S'\cup(S')'=S'$.

e) by (d) we know $\overline{S}$ contains all its accumulation points, and use Theorem 3.22.

f) Use the fact that $\mathbf{R}^n-\overline{S}$ is open, any closed subset $C$ of $\mathbf{R}^n$ containing $S$ has the property that $\mathbf{R}^n-C$ is an open subset contained in $\mathbf{R}^n-\overline{S}$, and Exercise 3.10.


### 3.13

Let $S$ and $T$ be subsets of $\mathbf{R}^n$. Prove that $\overline{S\cap T}\subseteq\overline{S}\cap\overline{T}$ and that $S\cap\overline{T}\subseteq\overline{S\cap T}$ if $S$ is open.

#### Proof

Let $\mathbf{x}\in S\cap T$, then for each $n$-ball of $\mathbf{x}$ there is a point of $S\cap T$ distinct from $\mathbf{x}$, since this point belongs to both $S$ and $T$, we have $\mathbf{x}\in\overline{S}$ and $\mathbf{x}\in\overline{T}$.

If $S$ is open, let $\mathbf{x}\in S\cap\overline{T}$, we first can find a $n$-ball $B$ of $\mathbf{x}$ such that $B\subset S$, for each $n$-ball of $\mathbf{x}$ contained in $B$, as $\mathbf{x}\in T'$, will have a point of $T$ distinct from $\mathbf{x}$, this point must belongs to $S$ since it belongs to $B$. thus $\mathbf{x}\in\overline{S\cap T}$.

### 3.14

A set $S$ in $\mathbf{R}^n$ is called *convex* if, for every pair of points $\mathbf{x}$ and $\mathbf{y}$ in $S$ and every real $\theta$ satisfying $0<\theta<1$, we have $\theta\mathbf{x}+(1-\theta)\mathbf{y}\in S$. Interpret this statement geometrically (in $\mathbf{R}^2$ and $\mathbf{R}^3$) and prove that:

a) Every $n$-ball in $\mathbf{R}^n$ is convex.

b) Every $n$-dimensional open interval is convex.

c) The interior of a convex set is convex.

d) The closure of a convex set is convex.

#### Proof

a) Let $B(\mathbf{z},r)$ be a $n$-ball, let $\mathbf{x},\mathbf{y}\in B(\mathbf{z},r)$ and $0<\theta<1$, consider
$$
\begin{aligned}
\|\theta\mathbf{x}+(1-\theta)\mathbf{y}-z\|&=\|\theta(\mathbf{x}-\mathbf{z})+(1-\theta)(\mathbf{y}-\mathbf{z})\|
\\&\leq\|\theta(\mathbf{x}-\mathbf{z})\|+\|(1-\theta)(\mathbf{y}-\mathbf{z})\|
\\&\leq\theta r+(1-\theta)r=r
\end{aligned}
$$
thus $\theta\mathbf{x}+(1-\theta)\mathbf{y}\in B(\mathbf{z},r)$.

b) Let $I=(a_1,b_1)\times\cdots\times(a_n,b_n)$ be an $n$-dimensional open interval. If $\mathbf{x}=(x_1,\dots,x_n)$ and $\mathbf{y}=(y_1,\dots,y_n)$ belongs to $I$, then we have $x_i\in(a_i,b_i)$ and $y_i\in(a_i,b_i)$ for $i=1,\dots,n$, then as long as $0<\theta<1$, we have $x_i+(1-\theta)y_i\in(a_i,b_i)$, thus $\theta\mathbf{x}+(1-\theta)\mathbf{y}\in I$.

c) Let $S$ be a convex set, and $\mathbf{x},\mathbf{y}\in\text{int }S$, let $\mathbf{z}=\theta\mathbf{x}+(1-\theta)\mathbf{y}$ for $0<\theta<1$, then $\mathbf{z}\in S$. Since $\mathbf{x},\mathbf{y}\in\text{int }S$, we can find $B(\mathbf{x},r)\subset S$ and $B(\mathbf{y},r)\subset S$. Consider the set $B(\mathbf{z},r)$, for any $\mathbf{p}\in B(\mathbf{z},r)$, we let $\mathbf{x}'=\mathbf{p}+(\mathbf{x}-\mathbf{z}),\mathbf{y}'=\mathbf{p}+(\mathbf{y}-\mathbf{z})$, then
$$
\theta\mathbf{x}'+(1-\theta)\mathbf{y}'=\mathbf{p}+\mathbf{z}-\mathbf{z}=\mathbf{p}
$$
and
$$
\|\mathbf{x}'-\mathbf{x}\|=\|\mathbf{y}'-\mathbf{y}\|=\|\mathbf{p}-\mathbf{z}\|<r
$$
thus $\mathbf{x}'\in B(\mathbf{x},r),\mathbf{y}'\in B(\mathbf{y},r)$, we conclude that $\mathbf{x}'\in S,\mathbf{y}'\in S$, and $\mathbf{p}\in S$ since $S$ is convex. It follows that $B(\mathbf{z},r)\subseteq S$ and $\mathbf{z}\in\text{int }S$.

d) Let $S$ be a convex set, and $\mathbf{x},\mathbf{y}\in\overline{S}$, let $\mathbf{z}=\theta\mathbf{x}+(1-\theta)\mathbf{y}$ for $0<\theta<1$, we need to prove $\mathbf{z}\in\overline{S}$, or $\mathbf{z}$ is adherent to $S$. Choose a $n$-ball of $z$, namely $B(\mathbf{z},r)$, for this $r$ we can find $\mathbf{p},\mathbf{q}\in S$ such that $\mathbf{p}\in B(\mathbf{x},r)$ and $\mathbf{q}\in B(\mathbf{y},r)$, define
$$
\mathbf{z}'=\theta\mathbf{p}+(1-\theta)\mathbf{q}
$$
then
$$
\|\mathbf{z}-\mathbf{z}'\|=\|\theta(\mathbf{x}-\mathbf{p})+(1-\theta)(\mathbf{y}-\mathbf{p})\|\leq\theta\|\mathbf{x}-\mathbf{p}\|+(1-\theta)\|\mathbf{y}-\mathbf{p}\|<r
$$
which means $\mathbf{z}'\in B(\mathbf{z},r)$, also $\mathbf{z}'\in S$ since $S$ is convex. This shows $\mathbf{z}$ is adherent to $S$.

### 3.15

Let $F$ be a collection of sets in $\mathbf{R}^n$, and let $S=\bigcup_{A\in F}A$ and $T=\bigcap_{A\in F}A$. For each of the following statements, either give a proof or exhibit a counterexample.

a) If $\mathbf{x}$ is an accumulation point of $T$, then $\mathbf{x}$ is an accumulation point of each set $A$ in $F$.

b) If $\mathbf{x}$ is an accumulation point of $S$, then $\mathbf{x}$ is an accumulation point of at least one set $A$ in $F$.

#### Proof

a) $\mathbf{x}$ is an accumulation point of $T$ means that for each $n$-ball $B(\mathbf{x},r)$ there is a point of $T$ distinct from $\mathbf{x}$, since this point belongs to each set $A$ in $F$, we conclude that for each $n$-ball $B(\mathbf{x},r)$ there is a point of $A\in F$ distinct from $\mathbf{x}$, thus $\mathbf{x}$ is an accumulation point of $A$ for each $A$ in $F$.

b) A counterexample is as follows: let $A_n=(1/n,1]$ and $F=\{A_n,n=1,2,\dots\}$, $F$ is a collection of sets in $\mathbf{R}$, we have $\bigcup_{A_n\in F}A_n=(0,1]$, and $0$ is an accumulation point of $(0,1]$, but each $A_n$ does not have $0$ as its accumulation point, since the ball $(-1/2n,1/2n)\cap A_n=\emptyset$.  

### 3.16

Prove that the set $S$ of rational numbers in the interval $(0,1)$ cannot be expressed as the intersection of a countable collection of open sets.

#### Proof

Write $S=\{x_1,x_2,\dots\}$, assume $S=\bigcap_{k=1}^{\infty}S_k$, where each $S_k$ is open, we construct a sequence $\{Q_n\}$ of closed intervals as follows:

Since $x_1\in S_1$, $S_1$ shall contain an open inverval $I_1$ which contains $x_1$, choose a closed interval inside $I_1$ which has length $>0$ that does not include $x_1$, name it $Q_1$. Since $Q_1$ contains infinitelly many rational number, we can choose one in int $Q_1$ and name it $x_2$ by rearranging $\{x_2,x_3,\dots\}$. Since $x_2\in S_2$, $S_2$ shall contain an open inverval $I_2$ which contains $x_2$, choose a closed interval inside $I_2\cap Q_1$ that does not include $x_2$, name it $Q_2$.

The process continues as each $Q_i$ with positive length will have infinitely many rational numbers in it. We have $Q_{n+1}\subseteq Q_n\subseteq S_n$ and $x_n\notin Q_n$ for each $n$. Now by Cantor intersection theorem, $\bigcap_{n=1}^{\infty}Q_n$ is not empty, i.e. we have some $x\in \bigcap_{n=1}^{\infty}Q_n$. Since $\bigcap_{n=1}^{\infty}Q_n\subseteq\bigcap_{n=1}^{\infty}S_n=S$, we have $x\in S$, or $x=x_n$ for some $n$, but this means $x\notin Q_n$, thus $x\notin\bigcap_{n=1}^{\infty}Q_n$, this is a contradiction.