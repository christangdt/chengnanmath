# Exercise 43-52 (Miscellaneous properties of the interior and the boundary)

If $A$ and $B$ denote arbitrary subsets of a metric space $M$, prove that:

### 3.43

$\text{int }A=M-\overline{M-A}$.

#### Proof

Let $x\in\text{int }A$, then there is a ball $B(x;r)\subseteq A$, which means the ball $B(x;r)\cap(M-A)$ is empty, so $x$ is not an adherent point of $M-A$, this means $\text{int }A\subseteq M-\overline{M-A}$. Conversely, let $y\notin\overline{M-A}$, then there is a ball $B(y;r')$ which contains no point of $M-A$, this means $B(y;r')\subseteq A$ and $y$ is an interior point of $A$. 

### 3.44

$\text{int }(M-A)=M-\overline{A}$.

#### Proof

$$
\begin{aligned}
x\in\text{int }(M-A)&\iff\exists B(x;r)\subseteq M-A
\\&\iff\exists B(x;r),B(x;r)\cap A=\empty
\\&\iff x\notin\overline{A}
\\&\iff x\in M-\overline{A}
\end{aligned}
$$

### 3.45

$\text{int }(\text{int }A)=\text{int }A$.

#### Proof

Let $S=\text{int }A$, then $\text{int }S\subseteq S$. We only need to prove $S\subseteq\text{int }S$. Let $x\in S$, then exists a ball $B(x;r)\subseteq A$, let $r'=r/2$, consider the ball $B(x;r')$, for each point $y$ of this ball, we see the smaller ball $B(y,r/4)$ is contained in $B(x;r)$, since
$$
d(z,x)\leq d(z,y)+d(y,x)\leq\dfrac{r}{2}+\dfrac{r}{4}<r,\quad\forall q\in B(y;r/4)
$$
this shows that each $y$ in $B(x;r')$ is an interior point of $A$, or $y\in S$, thus $x\in\text{int }S$, and the proof is complete.

### 3.46

a) $\text{int }(\bigcap_{i=1}^n A_i)=\bigcap_{i=1}^n(\text{int }A_i)$, where each $A_i\subseteq M$.

b) $\text{int }(\bigcap_{A\in F}A)\subseteq\bigcap_{A\in F}(\text{int }A)$, if $F$ is an infinite collection of subsets of $M$.

c) Give an example where equality does not hold in (b).

#### Proof

a) First let $x\in\text{int }(\bigcap_{i=1}^n A_i)$, then exists a ball $B(x;r)\subseteq\bigcap_{i=1}^nA_i$, thus $B(x;r)\subseteq A_i$ for each $i=1,\dots,n$, which means $x\in\text{int }A_i$ for each $i=1,\dots,n$, which means $x\in\bigcap_{i=1}^n(\text{int }A_i)$, thus $\text{int }(\bigcap_{i=1}^n A_i)\subseteq\bigcap_{i=1}^n(\text{int }A_i)$. Conversely, let $x\in\bigcap_{i=1}^n(\text{int }A_i)$, then $x\in\text{int }A_i$ for $i=1,\dots,n$, thus there exist balls $B(x;r_1),\dots,B(x;r_n)$ such that $B(x;r_i)\subseteq A_i$ for each $i$. Choose $r'=\min(r_1,\dots,r_n)$, we see that $B(x;r')\subseteq A_i$ for each $i$, thus $B(x;r')\subseteq\bigcap_{i=1}^nA_i$, which means $x\in\text{int }(\bigcap_{i=1}^n A_i)$, thus $\text{int }(\bigcap_{i=1}^n A_i)\supseteq\bigcap_{i=1}^n(\text{int }A_i)$.

b) Let $x\in\text{int }(\bigcap_{A\in F}A)$, then there exists a ball $B(x;r)\subseteq\bigcap_{A\in F}A$, thus $B(x;r)\subseteq A$ for each $A\in F$, which means $x\in\text{int }A$ for each $A\in F$, thus $x\in\bigcap_{A\in F}(\text{int }A)$ and the proof is complete.

c) Let $A_n=[-1/n,1/n]\subseteq\mathbf{R}$, then $\bigcap_{n=1}^{\infty} A_n=\{0\}$, which is a closed interval, thus $\text{int }(\bigcap_{n=1}^{\infty} A_n)=\empty$, but $\text{int }A_n=(-1/n,1/n)$ for each $n$, thus $\bigcap_{i=1}^{\infty}(\text{int }A_n)=\{0\}$.

### 3.47

a) $\bigcup_{A\in F}(\text{int }A)\subseteq\text{int }(\bigcup_{A\in F}A)$.

b) Give an example of a finite collection $F$ in which equality does not hold in (a)

#### Proof

a) Let $x\in\bigcup_{A\in F}(\text{int }A)$, then $x\in\text{int }A$ for at least one $A\in F$, we can find a ball $B(x,r)\subseteq A\subseteq\bigcup_{A\in F}A$, this shows that $x\in\text{int }\bigcup_{A\in F}A$.

b) Let $A=[0,1]$ and $B=[1,2]$, then $\text{int }A\cup\text{int }B=(0,1)\cup(1,2)$, while $\text{int }(A\cup B)=(0,2)$.

### 3.48

a) $\text{int }(\partial A)=\empty$ if $A$ is open or if $A$ is closed in $M$.

b) Give an example in which $\text{int }(\partial A)=M$.

#### Proof

a) Assume there exists $x\in M$ such that $x\in\text{int }(\partial A)$, then there is a ball $B(x;r)$ such that $B(x;r)\subseteq\partial A$. From this we get $x\in\partial A$, by definition, $B(x;r)$ contains at least one point $p\in A$ and one point $q\in M-A$.  Now if $A$ is open, $p$ shall be an interior point of $A$, we can find a ball $B(p;r')$ which contained in $B(x;r)$ such that  $B(p;r')\subseteq A$. But from $B(x;r)\subseteq\partial A$ we know that $p\in\partial A$, thus $B(p;r')$ shall contain a point of $M-A$, this is a contradiction. If $A$ is closed, then $M-A$ is open, with the same logic applied to $q$ we get another contradiction.

b) Consider the case $M=\mathbf{R}$ and $A=\mathbf{Q}$ with the Euclidean metric.

### 3.49

If $\text{int }A=\text{int }B=\empty$ and if $A$ is closed in $M$, then $\text{int }(A\cup B)=\empty$.

#### Proof

If either $A$ or $B$ is empty the proof is trivial. Suppose both $A$ and $B$ are not empty, and assume there is $x\in\text{int }(A\cup B)$, then we can find a ball $B(x;r)\subseteq A\cup B$,  if $A$ is closed, then $M-A$ is open, thus $S=B(x;r)\cap(M-A)$ is an open set and $S\subseteq B$. If $S$ is empty, then $B(x;r)\subseteq A$ and $x\in\text{int }A$, a contradiction to $\text{int }A=\empty$. If $S$ is a nonempty open set in $B$, choose $p\in S$, there is a ball $B(p;r')\subseteq S\subseteq B$, then $p\in\text{int }B$, a contradiction to $\text{int }B=\empty$. We see both case lead to a contradiction, and the proof is complete.

### 3.50

Give an example in which $\text{int }A=\text{int }B=\empty$ but $\text{int }(A\cup B)=M$.

#### Solution

Consider the case $A=\mathbf{R}-\mathbf{Q}$ and $B=\mathbf{Q}$ with the Euclidean metric.

### 3.51

$\partial A=\overline{A}\cap\overline{M-A}$ and $\partial A=\partial(M-A)$.

#### Proof

By definition, $x\in\partial A$ means that every ball $B(x;r)$ contains at least one point of $A$ and at least one point of $M-A$, this means $x\in\overline{A}$ and $x\in\overline{M-A}$. Conversely, if $x\in\overline{A}\cap\overline{M-A}$, then every ball $B(x;r)$ contains at least one point of $A$ and at least one point of $M-A$, and then $x\in\partial A$.

To prove the second statement, notice that
$$
\partial(M-A)=\overline{M-A}\cap\overline{M-(M-A)}=\overline{M-A}\cap\overline{A}=\partial A
$$

### 3.52

If $\overline{A}\cap\overline{B}=\empty$, then $\partial(A\cup B)=\partial A\cup\partial B$.

#### Proof

By Exercise 3.12 we have $(A\cup B)'=A'\cup B'$ and $\overline{A}$ is the smallest closed set containing $A$. We first show that $A\subseteq\overline{M-B}$, for any $a\in A$, assume $a\notin\overline{M-B}$, then there exists a ball $B(a;r)$ which has no points of $M-B$, then $B(a;r)\subseteq B$, in particular, $a\in B$, this means $a\in A\cap B\subseteq\overline{A}\cap\overline{B}$, a contradiction to $\overline{A}\cap\overline{B}=\empty$. Thus $A\subseteq\overline{M-B}$, and we further get $\overline{A}\subseteq\overline{M-B}$, as $\overline{M-B}$ is closed. By symmetry we can get $\overline{B}\subseteq\overline{M-A}$.

Next, we show $\overline{M-(A\cup B)}=\overline{M-A}\cap\overline{M-B}$. Suppose $x\in\overline{M-(A\cup B)}$, then every ball $B(x;r)$ contains at least one point of $M-(A\cup B)$. Assume $x\notin\overline{M-A}$, then there exists some ball $B(x;r_0)$ which has no point of $M-A$, or $B(x;r_0)\subseteq A\subseteq A\cup B$, a contradiction, thus we must have $x\in\overline{M-A}$, similarly we could get $x\in\overline{M-B}$ and so $\overline{M-(A\cup B)}\subseteq\overline{M-A}\cap\overline{M-B}$. Conversely, let $x\in\overline{M-A}\cap\overline{M-B}$, and assume $x\notin\overline{M-(A\cup B)}$, then there exists a ball $B(x;r_1)\subseteq A\cup B$, we claim that for some $r'<r_1$, either $B(x;r')\subseteq A$ or $B(x;r')\subseteq B$, if not, then any ball $B(x;r)$ with $r<r_1$ will contains at least one point of $A$ and at least one point of $B$, this means $x\in\overline{A}\cap\overline{B}$, which contradicts the condition $\overline{A}\cap\overline{B}=\empty$. But $B(x;r')\subseteq A$ means $x\notin\overline{M-A}$ and $B(x;r')\subseteq B$ means $x\notin\overline{M-B}$, both leads to a contradiction. So we get $\overline{M-A}\cap\overline{M-B}\subseteq\overline{M-(A\cup B)}$.

Finally, we have
$$
\begin{aligned}
\partial(A\cup B)&=\overline{A\cup B}\cap\overline{M-(A\cup B)}
\\&=\left((A\cup B)\cup(A\cup B)'\right)\cap\overline{M-A}\cap\overline{M-B}
\\&=(\overline{A}\cup\overline{B})\cap\overline{M-A}\cap\overline{M-B}
\\&=(\overline{A}\cap\overline{M-A})\cup(\overline{B}\cap\overline{M-B})
\\&=\partial A\cup\partial B
\end{aligned}
$$