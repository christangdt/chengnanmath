# Exercise 1-7 Open and closed sets in R^1 and R^2

### 3.1

Prove that an open interval in $\mathbf{R}^1$ is an open set and that a closed interval is a closed set.

#### Proof

Let $(a,b)$ be an open interval, we allow $a=-\infty$ or $b=+\infty$, for any point $x\in (a,b)$, we set $r=\min(1,x-a,b-x)$, then the 1-ball $B(x;r)\subseteq(a,b)$, thus $x$ is an interior point of $(a,b)$.
Let $[a,b]$ be a closed interval, then $\mathbf{R}-[a,b]=(-\infty,a)\cup(b,\infty)$, which is open.

### 3.2

Determine all the accumulation points of the following sets in $\mathbf{R}^1$ and decide whether the sets are open or closed (or neither).

- a) All integers.
- b) The interval $(a,b]$.
- c) All numbers of the form $1/n,n=1,2,3,\dots$
- d) All rational numbers.
- e) All numbers of the form $2^{-n}+5^{-m},m,n=1,2,3,\dots$
- f) All numbers of the form $(-1)^n+(1/m),m,n=1,2,3,\dots$
- g) All numbers of the form $(1/n)+(1/m),m,n=1,2,3,\dots$
- h) All numbers of the form $(-1)^n[1+(1/n)],n=1,2,3,\dots$

#### Solution

a) No accumulation points, the set is closed.

b) The accumulation points are all points in $[a,b]$, the set is neither open nor closed.

c) Only one accumulation point $0$, the set is neither open nor closed.

d) All real numbers are accumulation points, the set is neither open nor closed.

e) Only one accumulation point $0$, the set is neither open nor closed.

f) Two accumulation points $1$ and $-1$, the set is neither open nor closed.

g) The accumulation points are the points $1/n,n=1,2,\dots$ and $0$, the set is neither open nor closed.

h) Two accumulation points $1$ and $-1$, the set is neither open nor closed.

### 3.3

The same as Exercise 3.2 for the following sets in $\mathbf{R}^2$:

- a) All complex $z$ such that $|z|>1$.
- b) All complex $z$ such that $|z|\geq 1$.
- c) All complex numbers of the form $(1/n)+(i/m),(m,n=1,2,\dots)$
- d) All points $(x,y)$ such that $x^2-y^2<1$.
- e) All points $(x,y)$ such that $x>0$.
- f) All points $(x,y)$ such that $x\geq 0$.

#### Solution

a) The accumulation points are all complex $z$ such that $|z|\geq 1$. The set is open.

b) The accumulation points are all complex $z$ such that $|z|\geq 1$. The set is closed.

c) One accumulation point $(0,0)$. The set is neither open nor closed.

d) The accumulation points are the points $(x,y)$ such that $x^2-y^2\leq 1$. The set is open.

e) The accumulation points are all points $(x,y)$ such that $x\geq 0$. The set is open.

f) The accumulation points are all points $(x,y)$ such that $x\geq 0$. The set is closed.

### 3.4

Prove that every nonempty open set $S$ in $\mathbf{R}^1$ contains both rational and irrational numbers.

#### Proof

$S$ is nonempty means we can find $x\in S$, thus there exists a 1-ball $B(x,r)\subseteq S$, between the point $x-r$ and $x+r$ we can find rational number and irrational numbers.

### 3.5

Prove that the only sets in $\mathbf{R}^1$ which are both open and closed are the empty set and $\mathbf{R}^1$ itself. Is a similar statement true for $\mathbf{R}^2$?

#### Proof

The empty set is obviously both open and closed. And for $\mathbf{R}^1$, each point $x$ is an interior point since $(x-1,x+1)\in\mathbf{R}^1$, and the adherent point of $\mathbf{R}^1$ is $\mathbf{R}^1$ which contains in $\mathbf{R}^1$.

Suppose $S$ is a nonempty set of $\mathbf{R}^1$ which is not equal to $\mathbf{R}^1$, and assume $S$ is both open and closed, $S$ is open means that $S=\bigcup_{n=1}^{\infty}I_n$ where each $I_n$ is a component interval and $I_n\cap I_m=\empty$ for $n\neq m$. Since $S$ is nonempty, at least one $I_n$ is nonempty, write this $I_n$ to be $(a,b)$, then $a\notin S$, otherwise $a\in I_m$ for some $m$, and as $I_m$ is open we can find $(a-r,a+r)\subseteq I_m$, then $a+r/2\in I_n\cap I_m$. If $a\notin S$, then $a\in\mathbf{R}^1-S$, since $S$ is closed, $\mathbf{R}^1-S$ is open, which means we can find $(a-r',a+r')\notin S$, but for any $r$, we have $I_n\cap(a-r,a+r)\neq\empty$, thus a contradiction.

A similar statement is true for $\mathbf{R}^2$.

### 3.6

Prove that every closed set in $\mathbf{R}^1$ is the intersection of a countable collection of open sets.

#### Proof

Let $S$ be a closed set, then $\mathbf{R}^1-S$ is open. If $\mathbf{R}^1-S$ is nonempty, then by Theorem 3.11, we can write $\mathbf{R}^1-S=\bigcup_{i=1}^{\infty}I_i$, all of $I_i$ are component intervals, thus $S=\mathbf{R}^1-\bigcup_{i=1}^{\infty}I_i=\bigcap_{i=1}^{\infty}(\mathbf{R}^1-I_i)$

Now consider each set $\mathbf{R}^1-I_i$, write $I_i=(a_i,b_i)$, then $\mathbf{R}^1-I_i=(-\infty,a_i]\cup[b_i,+\infty)$, this set can be written as a countable intersection of open sets, i.e.
$$
(-\infty,a_i]\cup[b_i,+\infty)=\bigcap_{n=1}^{\infty}\left(\left(-\infty,a_i+\dfrac{1}{n}\right)\cup\left(b_i-\dfrac{1}{n},+\infty\right)\right)
$$
since the intersection of a countable intersections is still countable intersection, we finished the proof.

### 3.7

Prove that a nonempty, bounded closed set $S$ in $\mathbf{R}^1$ is either a closed interval, or that $S$ can be obtained from a closed interval by removing a countable disjoint collection of open intervals whose endpoints belong to $S$.

#### Proof

Since $S$ is nonempty and bounded, we let $a=\min{S}$ and $b=\max{S}$, then $a\leq b$. Clearly $S\subseteq[a,b]$.

Consider the closed interval $[a,b]$, if $[a,b]\subseteq S$, this means $S$ is a closed interval, if not, as $S$ is closed, we have $\mathbf{R}^1-S$ open, we also have $a-1\in\mathbf{R}^1-S$ and thus $\mathbf{R}^1-S$ is nonempty, thus we can write $\mathbf{R}^1-S$ as a union of a countable collection of disjoint component intervals of $\mathbf{R}^1-S$.

We first prove that $(-\infty,a)$ and $(b,\infty)$ must lie in this collection as a component interval. Consider the component interval in this collection that starts with $-\infty$, i.e. the interval $(-\infty,k)$, we must have $k\geq a$ because $(-\infty,a)\subseteq\mathbf{R}^1-S$, but if $k>a$, it means $a\in\mathbf{R}^1-S$, or $a\notin S$, a contradiction. Thus $(-\infty,a)$ must lie in this collection, the same with $(b,\infty)$.

Delete $(-\infty,a)$ and $(b,\infty)$ from the collection, we see that all the other component intervals lies in $[a,b]$, and subtract all these intervals gives $S$. It only remains to show that the endpoints of any of these intervals belongs to $S$. 

Let $I=(c,d)$ be any component interval of $\mathbf{R}^1-S$ which lies in $[a,b]$, then $a\leq c<d\leq b$. Consider $c$ first, if $c=a$ we have $c\in S$, if $c>a$, assume $c\notin S$, then $c\in\mathbf{R}^1-S$ which is open, thus we can find $r>0$ such that $(c-r,c+r)\in\mathbf{R}^1-S$, this means $(c-r,d)\in\mathbf{R}^1-S$, a contradiction since $(c,d)$ is a component interval, thus $c$ must belong to $S$, similarly we can show $d$ must belong to $S$.