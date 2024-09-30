# Exercise 38-42 (Compact subsets of a metric space)

Prove each of the following statements concerning an arbitrary metric space $(M,d)$ and subsets $S,T$ of $M$.

### 3.38

Assume $S\subseteq T\subseteq M$. Then $S$ is compact in $(M,d)$ if and only if $S$ is compact in the metric subspace $(T,d)$.

#### Proof

Suppose $S$ is compact in $(M,d)$, let $F$ be an open covering of $S$, say $S\subseteq \bigcup_{A\in F}A$, where each $A\in F$ is open in $T$. To find a finite covering of $S$ in $T$, notice that by Theorem 3.33 we can find some $A'$ open in $M$ for each set $A\in F$ such that $A=A'\cap T$. Call the collection of all sets $A'$ as $F'$, we have
$$
S\subseteq \bigcup_{A\in F}A=\bigcup_{A'\in F'}(A'\cap T)\subseteq\bigcup_{A'\in F'}A'
$$
We can then find a finite number of the sets $A'$ to cover $S$, use the fact that $S\subseteq T$ we get 
$$
S=(S\cap T)\subseteq (A'_1\cup\cdots\cup A'_p)\cap T=A_1\cup\cdots\cup A_p
$$
This shows that $S$ is compact in $(T,d)$.

Conversely, suppose $S$ is compact in $(T,d)$, let $F'$ be an open covering of $S$, say $S\subseteq \bigcup_{A'\in F}A'$, where each $A'\in F$ is open in $M$. Then let $A=A'\cap T$, use Theorem 3.33 we know $A$ is open in $T$, and
$$
S=(S\cap T)\subseteq \left(\bigcup_{A'\in F}A'\right)\cap T=\bigcup_{A'\in F}A'\cap T=\bigcup_{A'\in F}A
$$
Thus we can find a finite number of the sets $A$ cover $S$, as each $A\subseteq A'$, the corresponding finite number of sets $A'$ cover $S$. This completes the proof.

### 3.39

If $S$ is closed and $T$ is compact, then $S\cap T$ is compact.

#### Proof

By Theorem 3.38, $T$ is closed, thus $S\cap T$ is closed in $(T,d)$, as $T$ is compact, we see $S\cap T$ is compact in $(T,d)$, use Exercise 3.38 we see $S\cap T$ is compact in $(M,d)$.

### 3.40

The intersection of an arbitrary collection of compact subsets of $M$ is compact.

#### Proof

Let $F$ be a collection of compact subsets of $M$, for each $A\in F$, $A$ is closed by Theorem 3.38, thus $\bigcap_{A\in F}A$ is closed in $M$, by Theorem 3.39, $\bigcap_{A\in F}A$ is compact.

### 3.41

The union of a finite number of compact subsets of $M$ is compact.

#### Proof

Let $F$ be a finite collection of compact subsets of $M$, for each $A\in F$, $A$ is closed by Theorem 3.38, thus $\bigcup_{A\in F}A$ is closed in $M$, by Theorem 3.39, $\bigcup_{A\in F}A$ is compact.

### 3.42

Consider the metric space $\mathbf{Q}$ of rational numbers with the Euclidean metric. Let $S$ consist of all rational numbers in the open interval $(a,b)$, where $a$ and $b$ are irrational. Then $S$ is a closed and bounded subset of $\mathbf{Q}$ which is not compact.

#### Proof

$S$ is obviously bounded. If $q$ is an accumulation point of $S$, then we must have $q\in (a,b)$, since assume $q\leq a$, as $a$ is irrational we get $q<a$, then the ball $B(q,a-q)$ contains no point of $S$, a contradiction, and the same case when we assume $q\geq b$. To see $S$ is not compact, choose an integer $N$ such that $1/N<b-a$, let $A_n=(a+1/n,b)\cap\mathbf{Q}$ which is an open interval in $\mathbf{Q}$, then the collection $\bigcup_{n=N}^{\infty}A_n$ covers $(a,b)\cap\mathbf{Q}$, thus covers $S$. Now assume a finite number of the sets $A_n$ cover $S$, notice $A_m\subseteq A_n$ if $m\leq n$, we can define $M$ to be the maximum integer such that $A_M=(a+1/M,b)$ is in the finite subcover we assume, then $S\subseteq A_M$. Choose $q\in\mathbf{Q}$ such that $a<q<a+1/M$, then $q\in S$ but $q\notin A_M$, a contradiction.