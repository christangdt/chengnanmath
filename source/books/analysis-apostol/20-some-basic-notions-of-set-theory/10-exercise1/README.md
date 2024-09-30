# Exercise 1-9

### 2.1

Prove Theorem 2.2.

#### Proof

Theorem 2.2: $(a,b)=(c,d)$ if and only if $a=c$ and $b=d$.
To prove it, one direction is obvious. Now suppose $(a,b)=(c,d)$, by Definition 2.1, we have
$$
\{\{a\},\{a,b\}\}=\{\{c\},\{c,d\}\}
$$
from the definition of set equality, this means $\{a\}\in\{\{c\},\{c,d\}\}$, which gives $\{a\}=\{c\}$, which means $a=c$, similarly we can have $\{a,b\}=\{c,d\}$, or $\{a,b\}=\{a,d\}$, which means $b\in\{a,d\}$, thus $b=d$.

### 2.2

Let $S$ be a relation and let $\mathscr{D}(S)$ be its domain. The relation $S$ is said to be

- i) *reflexive* if $a\in\mathscr{D}(S)$ implies $(a,a)\in S$,
- ii) *symmetric* if $(a,b)\in S$ implies $(b,a)\in S$,
- iii) *transitive* if $(a,b)\in S$ and $(b,c)\in S$ implies $(a,c)\in S$.

A relation which is symmetric, reflexive and transitive is called an *equivalence relation*. Determine which of these properties is possessed by $S$, if $S$ is the set of all pairs of real numbers $(x,y)$ such that

a) $x\leq y$,

b) $x<y$,

c) $x<|y|$,

d) $x^2+y^2=1$,

e) $x^2+y^2<0$,

f) $x^2+x=y^2+y$.

#### Solution

a) reflexive is true since $x\leq x$ for any $x$, symmetric is false since $(x,x+1)\in S$ but $(x+1,x)$ is not, transitive is true.

b) reflexive is false, symmetric is false, transitive is true.

c) reflexive is false, symmetric is false, transitive is false since $(1,-2)\in S$ and $(-2,0)\in S$ but $(1,0)$ is not.

d) reflexive is false since $(0,0)\notin S$, symmetric is true, transitive is false.

e) since $\mathscr{D}(S)=S=\empty$, reflexive, symmetric and transitive are all true.

f) reflexive is true, symmetric is true, transitive is true.

### 2.3

The following functions $F$ and $G$ are defined for all real $x$ by the equations given. In each case where the composite function $G\circ F$ can be formed, give the domain of $G\circ F$ and a formula (or fomulas) for $(G\circ F)(x)$.

a) $F(x)=1-x,\quad G(x)=x^2+2x$,

b) $F(x)=x+5,\quad G(x)=|x|/x,\text{if }x\neq 0, G(0)=1$.

c) $F(x)=\begin{cases}2x,\quad\text{if }0\leq x\leq1,\\1,\qquad\text{otherwise}\end{cases},\quad G(x)=\begin{cases}x^2,\quad\text{if }0\leq x\leq1,\\1,\qquad\text{otherwise}\end{cases}$


Find $F(x)$ if $G(x)$ and $G[F(x)]$ are given as follows:

d) $G(x)=x^3,\quad G[F(x)]=x^3-3x^2+3x-1$.

e) $G(x)=3+x+x^2,\quad G[F(x)]=x^2-3x+5$.

#### Solution

a) $\mathscr{D}(G\circ F)=\mathbf{R},(G\circ F)(x)=G(1-x)=x^2-4x+3$.

b) $\mathscr{D}(G\circ F)=\mathbf{R},(G\circ F)(x)=|x+5|/(x+5)\text{if }x\neq -5,G(-5)=0$.

c) $\mathscr{D}(G\circ F)=\mathbf{R}$ and
$$
(G\circ F)(x)=\begin{cases}4x^2,\quad\text{if }0\leq x\leq1/2,\\1,\qquad\text{otherwise}\end{cases}
$$

d) $G[F(x)]=(x-1)^3$, thus $F(x)=x-1$.

e) $G[F(x)]=3+(1-x)+(1-x)^2$, thus $F(x)=1-x$.

### 2.4

Given three functions $F,G,H$, what restrictions must be placed on their domains so that the following four composite functions can be defined?
$$
G\circ F,\qquad H\circ G,\qquad H\circ(G\circ F),\qquad(H\circ G)\circ F.
$$
Assuming that $H\circ(G\circ F)$ and $(H\circ G)\circ F$ can be defined, prove the associative law:
$$
H\circ(G\circ F)=(H\circ G)\circ F
$$

#### Solution

For $G\circ F$, we must restrict $\mathscr{R}(F)\subset\mathscr{D}(G)$.
For $H\circ G$, we must restrict $\mathscr{R}(G)\subset\mathscr{D}(H)$.
For $H\circ(G\circ F)$ and $(H\circ G)\circ F$, we must restrict both $\mathscr{R}(F)\subset\mathscr{D}(G)$ and $\mathscr{R}(G)\subset\mathscr{D}(H)$.
Assume $H\circ(G\circ F)$ and $(H\circ G)\circ F$ can be defined, then
$$
\mathscr{D}(H\circ(G\circ F))=\mathscr{D}((H\circ G)\circ F)=\mathscr{D}(F)
$$
For any $x\in\mathscr{D}(F)$, we have
$$
(H\circ(G\circ F))(x)=((H\circ G)\circ F)(x)=H(G(F(x)))
$$
by Theorem 2.6, the two functions $H\circ(G\circ F)$ and $(H\circ G)\circ F$ are equal.

### 2.5

Prove the following set-theoretic identities for union and intersection:

a) $A\cup(B\cup C)=(A\cup B)\cup C,\quad A\cap(B\cap C)=(A\cap B)\cap C$.

b) $A\cap(B\cup C)=(A\cap B)\cup(A\cap C)$.

c) $(A\cup B)\cap(A\cup C)=A\cup(B\cap C)$.

d) $(A\cup B)\cap(B\cup C)\cap(C\cup A)=(A\cap B)\cup(A\cap C)\cup(B\cap C)$.

e) $A\cap(B-C)=(A\cap B)-(A\cap C)$.

f) $(A-C)\cap (B-C)=(A\cap B)-C$.

g) $(A-B)\cup B=A$ if and only if $B\subseteq A$.

#### Proof

a) It is easy to see that
$$
A\cup(B\cup C)=(A\cup B)\cup C=A\cup B\cup C
\\
A\cap(B\cap C)=(A\cap B)\cap C=A\cap B\cap C
$$

b) If $x\in A\cap(B\cup C)$, then $x\in A$, and either $x\in B$ or $x\in C$, thus either $x\in A\cap B$ or $x\in A\cap C$, which means $x\in(A\cap B)\cup(A\cap C)$, the converse is also true.

c) If $x\in (A\cup B)\cap(A\cup C)$, then both $x\in A\cup B$ and $x\in A\cup C$, if $x\in A$, then $x\in A\cup(B\cap C)$, if $x\notin A$, then from $x\in A\cup B$ we have $x\in B$, from $x\in A\cup C$ we have $x\in C$, thus $x\in B\cap C$, and $x\in A\cup(B\cap C)$.

On the other hand, if $x\in A\cup(B\cap C)$, then either $x\in A$, which means $x\in(A\cup B)\cap(A\cup C)$, or $x\in B\cap C$, thus $x\in A\cup B$ and $x\in A\cup C$, which means $x\in(A\cup B)\cap(A\cup C)$.

d) It is easy to see that $x$ must lies in at least two of the three sets $A,B,C$.

e) We have
$$
\begin{aligned}
x\in A\cap(B-C)&\Leftrightarrow(x\in A)\wedge(x\in B)\wedge(x\notin C)
\\&\Leftrightarrow(x\in A\cap B)\wedge(x\notin A\cap C)
\\&\Leftrightarrow x\in (A\cap B)-(A\cap C)
\end{aligned}
$$
f) We have
$$
\begin{aligned}
x\in (A-C)\cap(B-C)&\Leftrightarrow(x\in A)\wedge(x\in B)\wedge(x\notin C)
\\&\Leftrightarrow(x\in A\cap B)\wedge(x\notin C)
\\&\Leftrightarrow x\in (A\cap B)-C
\end{aligned}
$$

g) If $(A-B)\cup B=A$, then $\forall x\in B$, we have $x\in (A-B)\cup B$, thus $x\in A$, which means $B\subseteq A$. Conversely, if $B\subseteq A$, then $(A-B)\cup B\subseteq A$, and $\forall a\in A$, we have either $a\in B$, or $a\notin B$, the latter means $a\in A-B$, thus $a\in(A-B)\cup B$, this shows $(A-B)\cup B=A$.

### 2.6

Let $f:S\to T$ be a function. If $A$ and $B$ are arbitrary subsets of $S$, prove that
$$
f(A\cup B)=f(A)\cup f(B),\quad f(A\cap B)\subseteq f(A)\cap f(B)
$$
Generalize to arbitrary unions and intersections.

#### Proof

First let $y\in f(A\cup B)$, then $\exists x\in A\cup B$ such that $f(x)=y$. Since $x\in A$ or $x\in B$, we have $f(x)\in f(A)\cup f(B)$, so $f(A\cup B)\subseteq f(A)\cup f(B)$. On the other hand, for any $y\in f(A)\cup f(B)$, we have $y\in f(A)$ or $y\in f(B)$, then $y=f(a)$ for some $a\in A$ or $y=f(b)$ for some $b\in B$, in either case, there is $x\in A\cup B$ such that $y=f(x)$, so $y\in A\cup B$ and $f(A)\cup f(B)\subseteq f(A\cup B)$.
Next, let $y\in f(A\cap B)$, then $\exists x\in A\cap B$ such that $f(x)=y$, this means $y\in f(A)$ and $y\in f(B)$. Conversely let $A=\{1,2\},B=\{1,3\}$ and $f$ is defined with $f(1)=1,f(2)=f(3)=0$, then $f(A\cap B)=\{1\}$, but $f(A)\cap f(B)=\{0,1\}$.
Generalize to arbitrary unions and intersections, we have
$$
f(\cup_i A_i)=\bigcup_i f(A_i),\quad f(\cap_i A_i)=\bigcap_i f(A_i)
$$
the proof is similar with the proof when $i=2$ and is ommited.

### 2.7

Let $f:S\to T$ be a function. If $Y\subseteq T$, we denote by $f^{-1}(Y)$ the largest subset of $S$ which $f$ maps into $Y$. That is
$$
f^{-1}(Y)=\{x:x\in S,f(x)\in Y\}.
$$
The set $f^{-1}(Y)$ is called the *inverse image* of $Y$ under $f$. Prove the following for arbitrary subsets $X$ of $S$ and $Y$ of $T$.

a) $X\subseteq f^{-1}[f(X)]$,

b) $f[f^{-1}(Y)]\subseteq Y$,

c) $f^{-1}[Y_1\cup Y_2]=f^{-1}(Y_1)\cup f^{-1}(Y_2)$,

d) $f^{-1}(Y_1\cap Y_2)=f^{-1}(Y_1)\cap f^{-1}(Y_2)$,

e) $f^{-1}(T-Y)=S-f^{-1}(Y)$.

f) Generalize (c) and (d) to arbitrary unions and intersections.

#### Proof

a) Let $x\in X\subseteq S$, then $f(x)\in f(X)$, by definition, $x\in f^{-1}[f(X)]$.

b) For $\forall y\in f[f^{-1}(Y)],\exists x\in f^{-1}(Y)$, s.t. $y=f(x)$, but if $x\in f^{-1}(Y)$, then $f(x)\in Y$ by definition, thus $y\in Y$.

c) We have
$$
\begin{aligned}
x\in f^{-1}(Y_1\cup Y_2)&\Leftrightarrow f(x)\in (Y_1\cup Y_2)\Leftrightarrow (f(x)\in Y_1)\vee(f(x)\in Y_2)
\\&\Leftrightarrow(x\in f^{-1}(Y_1))\vee(x\in f^{-1}(Y_2))\Leftrightarrow x\in f^{-1}(Y_1)\cup f^{-1}(Y_2)
\end{aligned}
$$
d) We have
$$
\begin{aligned}
x\in f^{-1}(Y_1\cap Y_2)&\Leftrightarrow f(x)\in (Y_1\cap Y_2)\Leftrightarrow (f(x)\in Y_1)\wedge(f(x)\in Y_2)
\\&\Leftrightarrow(x\in f^{-1}(Y_1))\wedge(x\in f^{-1}(Y_2))\Leftrightarrow x\in f^{-1}(Y_1)\cap f^{-1}(Y_2)
\end{aligned}
$$
e) We have
$$
\begin{aligned}
x\in f^{-1}(T-Y)&\Leftrightarrow (x\in S)\wedge(f(x)\in T-Y)\Leftrightarrow (x\in S)\wedge(f(x)\notin Y)
\\&\Leftrightarrow(x\in S)\wedge(x\notin f^{-1}(Y))\Leftrightarrow x\in S-f^{-1}(Y)
\end{aligned}
$$

f) We can have $f^{-1}(\cup_i Y_i)=\bigcup_if^{-1}(Y_i)$ and $f^{-1}(\cap_i Y_i)=\bigcap_if^{-1}(Y_i)$.

### 2.8

Refer to Exercise 2.7. Prove that $f[f^{-1}(Y)]=Y$ for every subset $Y$ of $T$ if and only if $T=f(S)$.

#### Proof

We already have $f[f^{-1}(Y)]\subseteq Y$, thus we only have to prove $f[f^{-1}(Y)]\supseteq Y$ if and only if $T=f(S)$.
First suppose $T=F(S)$, for $\forall y\in Y$, we have $y\in T$, thus $y\in f(S)$, which means $\exists x\in S$ such that $f(x)=y$, this shows $x\in f^{-1}(Y)$ by definition of $f^{-1}(Y)$, thus $y\in f[f^{-1}(Y)]$.
Next suppose $f[f^{-1}(Y)]\supseteq Y$ for every subset $Y$ of $T$, then since $T$ is a subset of $T$, we have $T\subseteq f[f^{-1}(T)]\subseteq f(S)$, since it is obvious that $f(S)\subseteq T$, we can finish the proof.

### 2.9

Let $f:S\to T$ be a function. Prove that the following statements are equivalent.

a) $f$ is one-to-one on $S$.

b) $f(A\cap B)=f(A)\cap f(B)$ for all subsets $A,B$ of $S$.

c) $f^{-1}[f(A)]=A$ for every subset $A$ of $S$.

d) For all disjoint subsets $A$ and $B$ of $S$, the images $f(A)$ and $f(B)$ are disjoint.

e) For all subsets $A$ and $B$ of $S$ with $B\subseteq A$, we have
$$
f(A-B)=f(A)-f(B).
$$

#### Proof

(a) implies (b): 
For $y=f(x)\in f(A\cap B)$, we have $x\in A\cap B$ and $(f(x)\in f(A))\wedge(f(x)\in f(B))$, this means $f(A\cap B)\subseteq f(A)\cap f(B)$, now assume there is $y'\in f(A)\cap f(B)$, but $y'\notin f(A\cap B)$, then $\exists x'\in A-B$ and $x''\in B-A$ such that $f(x')=f(x'')=y'$, since $A-B\cap B-A=\empty$, we must have $x'\neq x''$, this contradicts $f$ being one-to-one on $S$.

(b) implies (c):
If $x\in A$, then $f(x)\in f(A)$, thus $x\in f^{-1}[f(A)]$, which means $A\subseteq f^{-1}[f(A)]$. Assume $\exists a\in f^{-1}[f(A)],a\notin A$, then $f(a)\in f(A)$, from (b) we can also get $f(A\cap \{a\})=f(A)\cap f(\{a\})=f(a)$, but $A\cap\{a\}=\empty$, this means $f(\empty)=f(a)$, a contradiction. Thus we get $f^{-1}[f(A)]\subseteq A$.

(c) implies (d):
Suppose $A\cap B=\empty$, and assume $f(A)\cap f(B)\neq\empty$, then $\exists c\in f(A)\cap f(B)$, which means $\exists a\in A,b\in B$ such that $f(a)=f(b)=c$, this means $f^{-1}[f(\{a\})]=f^{-1}(\{c\})=\{a,b\}$. Using (c) we have $f^{-1}[f(\{a\})]=\{a\}$. Since $A\cap B=\empty$, we must have $a\neq b$ and $\{a,b\}\neq\{a\}$, this is a contradiction.

(d) implies (e):
The sets $A-B$ and $B$ are disjoint, thus $f(A-B)\cap f(B)=\empty$ by (d). Also if $y\in f(A-B)$, then $\exists x\in A-B\subseteq A$ such that $y=f(x)$, thus $y\in f(A)$ and $f(A-B)\subseteq f(A)$. Now we proved $f(A-B)\subseteq f(A)-f(B)$. To prove the converse, if $y\in f(A)-f(B)$, then $y\in f(A)$ and $y\notin f(B)$, thus $\exists x\in A$ such that $f(x)=y$, moreover we must have $x\notin B$ otherwise $y\in f(B)$, this means $x\in A-B$ and $y\in f(A-B)$.  

(e) implies (a):
Assume $f$ is not one-to-one on $S$, then $\exists a,b\in S$ with $a\neq b$ and $f(a)=f(b):=c$. Let $A=\{a,b\}$ and $B=\{b\}$, then $A-B=\{a\}$, using (e) we have $f(A-B)=f(\{a\})=\{c\}=f(A)-f(B)$, but $f(A)=f(B)=\{c\}$ and thus $f(A)-f(B)=\empty$, a contradiction.