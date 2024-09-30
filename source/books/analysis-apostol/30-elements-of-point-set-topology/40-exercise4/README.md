# Exercise 26-37 (Metric spaces)

### 3.26

In any metric space $(M,d)$, prove that the empty set $\emptyset$ and the whole space $M$ are both open and closed.

#### Proof

The empty set is open. For the assersion that all points in $\empty$ are interior points, we have no $x\in M$ such that $x\in\empty$, thus this assersion is true. Thus the whole space $M$ is closed.
The whole space $M$ is open, since for all $x\in M$ and any ball $B(x)$, we shall have $B(x)\subseteq M$, thus $x$ is an interior point of $M$. This means $\empty$ is closed.

### 3.27

Consider the following two metrics in $\mathbf{R}^n$:
$$
d_1(\mathbf{x},\mathbf{y})=\max_{1\leq i\leq n}|x_i-y_i|,\qquad d_2(\mathbf{x},\mathbf{y})=\sum_{i=1}^n|x_i-y_i|,
$$
In each of the following metric spaces prove that the ball $B(\mathbf{a};r)$ has the geometric appearance indicated:

a) In $(\mathbf{R}^2,d_1)$, a square with sides parallel to the coordinate axes.

b) In $(\mathbf{R}^2,d_2)$, a square with diagonals parallel to the axes.

c) A cube in $(\mathbf{R}^3,d_1)$.

d) An octahedron in $(\mathbf{R}^3,d_2)$.

#### Proof

All are easy to imagine. Ommitted.

### 3.28

Let $d_1$ and $d_2$ be the metrics of Exercise 3.27 and let $\|\mathbf{x}-\mathbf{y}\|$ denote the usual Euclidean metric. Prove the following inequalities for all $\mathbf{x}$ and $\mathbf{y}$ in $\mathbf{R}^n$:
$$
d_1(\mathbf{x},\mathbf{y})\leq\|\mathbf{x}-\mathbf{y}\|\leq d_2(\mathbf{x},\mathbf{y})\qquad d_2(\mathbf{x},\mathbf{y})\leq\sqrt{n}\|\mathbf{x}-\mathbf{y}\|\leq nd_1(\mathbf{x},\mathbf{y})
$$

#### Proof

Let $\mathbf{x}=(x_1,\dots,x_n),\mathbf{y}=(y_1,\dots,y_n)$, let the index $k$ be that satisfies $|x_k-y_k|=\max_{1\leq i\leq n}|x_i-y_i|$, then we have
$$
d_1(\mathbf{x},\mathbf{y})=|x_k-y_k|\leq\sqrt{\sum_{i=1}^n|x_i-y_i|^2}=\|\mathbf{x}-\mathbf{y}\|
$$
also we have
$$
\begin{aligned}
\|\mathbf{x}-\mathbf{y}\|&=\sqrt{\sum_{i=1}^n|x_i-y_i|^2}\leq\sqrt{\sum_{i=1}^n|x_i-y_i|^2+2\sum_{i\neq j}|x_i-y_i||x_j-y_j|}\\&=\sum_{i=1}^n|x_i-y_i|=d_2(\mathbf{x},\mathbf{y})
\end{aligned}
$$
For the second inequality, let $c_i=|x_i-y_i|$, then $d_2(\mathbf{x},\mathbf{y})=\sum_ic_i$ and $\|\mathbf{x}-\mathbf{y}\|=\sqrt{\sum_ic_i^2}$. We first prove $(\sum_ic_i)^2\leq n\sum_ic_i^2$ with induction on $n$.
For $n=1$, we have $c_1^2\leq c_1^2$.
Suppose the inequality holds for $n-1$, we have
$$
\begin{aligned}
    \left(\sum_{i=1}^nc_i\right)^2&=\left(\sum_{i=1}^{n-1}c_i\right)^2+c_n^2+2\sum_{i=1}^{n-1}c_ic_n
    \\&\leq(n-1)\sum_{i=1}^{n-1}c_i^2+c_n^2+\sum_{i=1}^{n-1}(c_i^2+c_n^2)=n\sum_{i=1}^nc_i^2
\end{aligned}
$$
thus the first half is proved. The second half, we let $c=\max_{1\leq i\leq n}c_i$, then 
$$
\begin{aligned}
\sum_{i=1}^nc_i^2\leq nc^2&\implies\|\mathbf{x}-\mathbf{y}\|=\sqrt{\sum_{i=1}^nc_i^2}\leq\sqrt{n}c=\sqrt{n}d_1(\mathbf{x},\mathbf{y})\\&\implies\sqrt{n}\|\mathbf{x}-\mathbf{y}\|\leq nd_1(\mathbf{x},\mathbf{y})
\end{aligned}
$$

### 3.29

If $(M,d)$ is a metric space, define
$$
d'(x,y)=\dfrac{d(x,y)}{1+d(x,y)}.
$$
Prove that $d'$ is also a metric for $M$. Note that $0\leq d'(x,y)<1$ for all $x,y$ in $M$.

#### Proof

First $d'(x,x)=0$, and $d'(x,y)>0$ since $d(x,y)>0$ if $x\neq y$. Second,
$$
d'(x,y)=\dfrac{d(x,y)}{1+d(x,y)}=\dfrac{d(y,x)}{1+d(y,x)}=d'(y,x)
$$
Let $d(x,y)=a,d(x,z)=b,d(y,z)=c$, then $a\leq b+c$, let $m=b+c+bc\geq a$, we have
$$
\begin{aligned}
&\qquad a\leq m+bc+abc
\\&\implies (1+m)a\leq (1+a)(m+bc)
\\&\implies \dfrac{a}{1+a}\leq\dfrac{m+bc}{1+m}=\dfrac{b+c+2bc}{1+b+c+bc}=\dfrac{b(1+c)+c(1+b)}{(1+b)(1+c)}
\\&\implies \dfrac{a}{1+a}\leq \dfrac{b}{1+b}+\dfrac{c}{1+c}
\end{aligned}
$$

### 3.30

Prove that every finite subset of a metric space is closed.

#### Proof

Let $S$ be a finite set in $(M,d)$, let $x\notin S$, we prove $x$ is not an adherent point of $S$. Since $S$ is finite, we can denote $S=\{x_1,\dots,x_n\}$, let
$$
r=\dfrac{\min_{1\leq i\leq n}d(x,x_i)}{2}>0
$$
then $B(x,r)\cap S=\empty$.

### 3.31

In a metric space $(M,d)$ the *closed ball* of radius $r>0$ about a point $a$ in $M$ is the set $\overline{B}(a;r)=\{x:d(x,a)\leq r\}$.

a) Prove that $\overline{B}(a;r)$ is a closed set.

b) Give an example of a metric space in which $\overline{B}(a;r)$ is not the closure of the open ball ${B}(a;r)$.

#### Proof

a) If $x$ is an adherent point of $\overline{B}(a;r)$, assume $d(a,x)>r$, then let $r':=(d(a,x)-r)/2$ and the ball $B(x,r')\cap \overline{B}(a;r)=\empty$, a contradiction to $x$ being an adherent point of $\overline{B}(a;r)$, thus $d(a,x)\leq r$, or $x\in\overline{B}(a;r)$. It follows that $\overline{B}(a;r)$ contains all its adherent points.

b) In any discrete metric space with more than two points including $a$, the open ball $B(a,1)$ contains only $a$, since no point $x\neq a$ can be an accumulation point of $B(a,1)$, the closure of $B(a,1)$ is $B(a,1)$ itself, but $\overline{B}(a,1)$ contains all points of the metric space.

### 3.32

In a metric space $M$, if subsets satisfy $A\subset S\subset \overline{A}$, where $\overline{A}$ is the closure of $A$, then $A$ is said to be *dense* in $S$. For example, the set $\mathbf{Q}$ of rational numbers is dense in $\mathbf{R}$. If $A$ is dense in $S$ and if $S$ is dense in $T$, prove that $A$ is dense in $T$.

#### Proof

We have $A\subset S\subset \overline{A}$ and $S\subset T\subset \overline{S}$, thus $A\subset T$, from Exercise 3.12 (f) we know that $S\subset \overline{A}$ and $\overline{A}$ is closed means $\overline{S}\subset\overline{A}$, thus $T\subset\overline{A}$.

### 3.33

Refer to Exercise 3.32. A metric space $M$ is said to be *separable* if there is a *countable* subset $A$ which is dense in $M$. Prove that every Euclidean space $\mathbf{R}^k$ is separable.

#### Proof

Let $\mathbf{Q}^k$ be the set of all points $(q_1,\dots,q_k)$ where each $q_i\in\mathbf{Q}$, then $\mathbf{Q}^k$ is countable and dense in $\mathbf{R}^k$.

### 3.34

Refer to Exercise 3.32. Prove that the Lindelof covering theorem is valid in any separable metric space.

#### Proof

Let $(M,d)$ be a separable metric space, then there is a countable subset $A$ which is dense in $M$. Let $G=\{B(a,r):a\in A,r\in\mathbf{Q}\}$, then $G$ is a countable set.

Suppose there is an open covering $F$ of $M$, then for each $x\in M$, there is an open set $S\in F$ such that $x\in S$, which means $\exists B(x,r)\subset S$, since $A$ is dense in $M$, $x\in\overline{A}$, thus the ball $B(x,r/2)$ contains some point $a\in A$, choose a rational $q$ such that $d(x,a)<q<r/2$, then $x\in B(a,q)\subset B(x,r)\subset S$, and $B(a,q)\in G$. Since $G$ is countable, we can choose one $S\in F$ for each $B(a,q)\in G$, the collection $S$ selected is countable and covers $M$. 

### 3.35

Refer to Exercise 3.32. If $A$ is dense in $S$ and if $B$ is open in $S$, prove that $B\subseteq\overline{A\cap S}$.

#### Proof

Let $b\in B$, then there is a ball $B(b;r_0)\subseteq S$, thus $b\in S\subseteq\overline{A}=\overline{A\cap S}$. 

### 3.36

Refer to Exercise 3.32. If each of $A$ and $B$ is dense in $S$ and if $B$ is open in $S$, prove that $A\cap B$ is dense in $S$.

#### Proof

We have $A\subset S\subset\overline{A}$ and $B\subset S\subset\overline{B}$, thus $A\cap B\subset S$. To prove $S\subset\overline{A\cap B}$, 

### 3.37

Given two metric spaces $(S_1,d_1)$ and $(S_2,d_2)$, a metric $\rho$ for the Cartesian product $S_1\times S_2$ can be constructed from $d_1$ and $d_2$ in many ways. For example, if $x=(x_1,x_2)$ and $y=(y_1,y_2)$ are in $S_1\times S_2$, let $\rho(x,y)=d_1(x_1,y_1)+d_2(x_2,y_2)$. Prove that $\rho$ is a metric for $S_1\times S_2$ and construct further examples.

#### Proof

First, obviously $\rho(x,y)\ge0$ and $\rho(x,x)=d_1(x_1,x_1)+d_2(x_2,x_2)=0+0=0$. If $x\ne y$, then either $x_1\ne y_1$ or $x_2\ne y_2$ or both, thus we have either $d_1(x_1,y_1)>0$ or $d_2(x_2,y_2)>0$ or both, which gives $\rho(x,y)>0$.

Second, from $d_1(x_1,y_1)=d_1(y_1,x_1)$ and $d_2(x_2,y_2)=d_2(y_2,x_2)$ we have $\rho(x,y)=\rho(y,x)$.

Third, let $z=(z_1,z_2)$, we have
$$
\begin{aligned}
\rho(x,y)&=d_1(x_1,y_1)+d_2(x_2,y_2)
\\&\le d_1(x_1,z_1)+d_1(z_1,y_1)+d_2(x_2,z_2)+d_2(z_2,y_2)
\\&=\rho(x,z)+\rho(z,y)
\end{aligned}
$$
This shows $\rho$ is a metric for $S_1\times S_2$.