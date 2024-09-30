# Exercise 17-25 (Covering theorems in Rn)

### 3.17

If $S\subseteq\mathbf{R}^n$, prove that the collection of isolated points of $S$ is countable.

#### Proof

Let $\mathbf{x}$ be an isolated point of $S$, then we can find a ball $B(\mathbf{x},r)$ such that $B(\mathbf{x},r)\cap S=\mathbf{x}$. For any two isolated points $\mathbf{x}_1$ and $\mathbf{x}_2$, we can modify two balls to make them not joint. Thus each isolated points of $S$ corresponds to a ball, we can choose a rational $q$ for each ball, it follows that the set of isolated points of $S$ is equivalent to a subset of $\mathbf{Q}$, thus countable.

### 3.18

Prove that the set of open disks in the $xy$-plane with center at $(x,x)$ and radius $x>0$, $x$ rational, is a countable covering of the set $\{(x,y):x>0,y>0\}$.

#### Proof

It is easy to see the set of open disks is countable. To prove it is a covering of $\{(x,y):x>0,y>0\}$, consider $(x,y)$ with $x>0,y>0$, we further suppose $x\leq y$, let $q$ be a rational such that
$$
y<q<\dfrac{\sqrt{2}y-(y-x)}{\sqrt{2}-1}\implies \sqrt{2}q-q<\sqrt{2}y-(y-x)
$$
then the point $(q,q)$ lies above the point $(y,y)$ in the $xy$-plane, and
$$
\|(q,q)-(x,y)\|\leq\|(q,q)-(y,y)\|+\|(y,y)-(x,y)\|=\sqrt{2}(q-y)+(y-x)<q
$$
thus the point $(x,y)$ lies in the open disk with center at $(q,q)$ and radius $q$. 
The case when $x>y$ can be similarly proved.

### 3.19

The collection $F$ of open intervals of the form $(1/n,2/n)$, where $n=2,3,\dots,$ is an open covering of the open interval $(0,1)$. Prove (without using Theorem 3.31) that no finite subcollection of $F$ covers $(0,1)$.

#### Proof

For any finite subcollection of $F$, we can find a largest $N$ in all $n$ which constitute such intervals $(1/n,2/n)$, then the point $1/(N+1)$ is not covered by the finite subcollection.

### 3.20

Give an example of a set $S$ which is closed but not bounded and exhibit a countable open covering $F$ such that no finite subset of $F$ covers $S$.

#### Solution

Let $S=\{n:n\in\mathbf{Z}\}$, then $S$ is closed since $S=\mathbf{R}-\cup_{k\in\mathbf{Z}}(k,k+1)$ is the complement of an open set. $S$ is obviously not bounded. The covering $F=\{(n-1/2,n+1/2):n\in\mathbf{Z}\}$ covers $S$, it is countable since $F$ is equivalent to $\mathbf{Z}$, but no finite subset of $F$ covers $S$.

### 3.21

Given a set $S$ in $\mathbf{R}^n$ with the property that for every $\mathbf{x}$ in $S$ there is an $n$-ball $B(\mathbf{x})$ such that $B(\mathbf{x})\cap S$ is countable. Prove that $S$ is countable.

#### Proof

By the Lindelof covering theorem, for each $\mathbf{x}\in S$ we choose a ball $B(\mathbf{x})$ such that $B(\mathbf{x})\cap S$ is countable, the collection $F=\{B(\mathbf{x})\cap S:\mathbf{x}\in S\}$ is a covering of $S$, and we can choose a countable subcollection $F'$ that covers $S$. It follows that $S\subseteq\bigcup_{B\in F'}B$, since each $B$ is countable and $F'$ is countable, we have $\bigcup_{B\in F'}B$ being countable and so is $S$.

### 3.22

Prove that a collection of disjoint open sets in $\mathbf{R}^n$ is necessarily countable. Given an example of a collection of disjoint closed sets which is not countable.

#### Proof

For any open set in this disjoint open sets, we can find a point with all coordinates rational, thus the collection is equivalent to a subset of rational points in $\mathbf{R}^n$, thus countable.
The collection of sets $\{(a,0,\dots,0)\}$ with $0\leq a\leq 1$ is a collection which is not countable, but each set consists only one point $(a,0,\dots,0)$, thus is closed and disjoint.

### 3.23

Assume that $S\subseteq\mathbf{R}^n$. A point $\mathbf{x}$ in $\mathbf{R}^n$ is said to be a *condensation point* of $S$ if every $n$-ball $B(\mathbf{x})$ has the property that $B(\mathbf{x})\cap S$ is not countable. Prove that if $S$ is not countable, then there exists a point $\mathbf{x}$ in $S$ such that $\mathbf{x}$ is a condensation point of $S$.

#### Proof

Assume each point in $S$ is not a condensation point of $S$, then for each $\mathbf{x}\in S$ we can find at least one ball $B(\mathbf{x})$ such that $B(\mathbf{x})\cap S$ is countable, then $S$ is countable by Exercise 3.21, a contradiction.

### 3.24

Assume that $S\subseteq\mathbf{R}^n$ and assume that $S$ is not countable. Let $T$ denote the set of condensation points of $S$. Prove that:

a) $S-T$ is countable,

b) $S\cap T$ is not countable,

c) $T$ is a closed set,

d) $T$ contains no isolated points.

#### Proof

a) $S-T$ consists of points that are not condensation points of $S$, which satisfies the requirements of Exercise 3.21, thus is countable.

b) Assume $S\cap T$ is countable, then $S=(S-T)\cup(S\cap T)$ is countable, a contradiction.

c) Let $\mathbf{x}\notin T$, then we can find a ball $B(\mathbf{x})$ such that $B(\mathbf{x})\cap S$ is countable. Let the radius of $B(\mathbf{x})$ to be $r$, then for any point $\mathbf{y}\in B(\mathbf{x},r/2)$, the ball $B(\mathbf{y},r/2)\subset B(\mathbf{x},r)$, thus we have $B(\mathbf{y},r/2)\cap S$ is countable, which means $\mathbf{y}\notin T$, it follows that $\mathbf{R}^n-T$ is open.

d) Assume $\mathbf{p}$ is an isolated point of $T$, then by definition, $\mathbf{p}\in T$ and $\mathbf{p}$ is not an accumulation point of $T$, thus we can find a ball $B(\mathbf{p})$ which contains no point of $T$ other than $\mathbf{p}$. Since $\mathbf{p}\in T$, we have $B(\mathbf{p})\cap S$ not countable, but for any point $\mathbf{x}\in B(\mathbf{p}),\mathbf{x}\neq\mathbf{p}$, the point $\mathbf{x}$ is not a condensation point of $S$, which means $\exists B(\mathbf{x})$ such that $B(\mathbf{x})\cap S$ is countable. The collection of all such $B(\mathbf{x})$ covers $B(\mathbf{p})-\{\mathbf{p}\}$, by the Lindelof covering theorem, there is a countable subcollection $F$ that covers this set, thus $B(\mathbf{p})-\{\mathbf{p}\}\subset\bigcup_{B\in F}B$, or $B(\mathbf{p})\cap S\subset\left(\bigcup_{B\in F}B\cap S\right)\cup\{\mathbf{p}\}$. Notice that $F$ is countable and $B\cap S$ is countable for each $B\in F$, we conclude $B(\mathbf{p})\cap S$ is countable, this is a contradiction.

### 3.25

A set in $\mathbf{R}^n$ is called *perfect* if $S=S'$, that is, if $S$ is a closed set which contains no isolated points. Prove that every uncountable closed set $F$ in $\mathbf{R}^n$ can be expressed in the form $F=A\cup B$, where $A$ is perfect and $B$ is countable. (*Cantor-Bendixon theorem*)

#### Proof

Let $A$ be the set of condensation points of $F$, let $B=F-A$, then $A$ is perfect and $B$ is countable by Exercise 3.24.