# Exercise 29-35 (Continuity in metric spaces)

In Exercises 4.29 through 4.33, we assume that $f: S\to T$ is a function from one metric space $(S, d_S)$ to another $(T, d_T)$.

### 4.29

Prove that $f$ is continuous on $S$ if, and only if $f^{-1}(\text{int }B)\subseteq\text{int }f^{-1}(B)$ for every subset $B$ of $T$.

#### Proof

Let $f$ be continuous on $S$, let $p\in f^{-1}(\text{int }B)$, then $\exists r>0$ such that $B(f(p);r)\subseteq B$, which means there is $\delta>0$ such that $x\in B(p;\delta)$ implies $f(x)\in B(f(p),r)\subseteq B$, so we have $B(p;\delta)\subseteq f^{-1}(B)$ and $p\in \text{int }f^{-1}(B)$. Conversely, if $f^{-1}(\text{int }B)\subseteq\text{int }f^{-1}(B)$ for every subset $B$ of $T$, consider any open set $B\subseteq T$, we have $\text{int }B=B$, thus $f^{-1}(B)\subseteq\text{int }f^{-1}(B)$, which means $f^{-1}(B)$ is open, by Theorem 4.23, $f$ is continuous on $S$.

### 4.30

Prove that $f$ is continuous on $S$ if, and only if $f(\overline{A})\subseteq\overline{f(A)}$ for every subset $A$ of $S$.

#### Proof

Let $f$ be continuous on $S$, let $p\in f(\overline{A})$, then $\exist a\in\overline{A}$ such that $f(a)=p$, if $a\in A$ then $p\in f(A)$ and there is nothing to prove. Suppose $a$ is an accumulation point of $A$, then given any ball $B(p;r)$ in $T$ with $r>0$, by the continuity of $f$ at $a$, there is some $\delta >0$ such that $x\in B(a;\delta)$ implies $f(x)\in B(p;r)$, in the ball $B(a;\delta)$ there is at least one point $y\in A$, thus $f(y)\in B(p;r)$, but $f(y)\in f(A)$, this shows that $p$ is an accumulation point of $f(A)$, or $p\in\overline{f(A)}$.

Conversely, if $f(\overline{A})\subseteq\overline{f(A)}$ for every subset $A$ of $S$, let $C\subseteq T$ be a closed set, and define $A=f^{-1}(C)$, then $f(\overline{A})\subseteq\overline{f(A)}=\overline{f(f^{-1}(C))}\subseteq\overline{C}=C$, which means $\overline{A}\subseteq f^{-1}[f(\overline{A})]\subseteq f^{-1}(C)=A$, thus $A$ is closed. By Theorem 4.24, $f$ is continuous.

### 4.31

Prove that $f$ is continuous on $S$ if, and only if, $f$ is continuous on every compact
subset of $S$.

#### Proof

One direction is obvious. To prove the other direction, consider $s\in S$, if $s$ is an isolated point of $S$, the proof is trivial, if $s$ is an accumulation point of $S$, then there exists a sequence $\{x_n\}\subseteq S$ such that $x_n\to s$. The set $\{s,x_1,x_2,\dots\}$ is a compact subset of $S$ and so $f$ is continuous on it, thus continuous at $s$.

### 4.32

A function $f:S\to T$ is called a *closed mapping* on $S$ if the image $f(A)$ is closed in $T$ for every closed subset $A$ of $S$. Prove that $f$ is continuous and closed on $S$ if, and only if $f(\overline{A})=\overline{f(A)}$ for every subset $A$ of $S$.

#### Proof

If $f(\overline{A})=\overline{f(A)}$ for every subset $A$ of $S$, then by Exercise 4.30, $f$ is continuous, and if $A$ is closed in $S$, then $f(A)=f(\overline{A})=\overline{f(A)}$, which is closed in $T$, thus $f$ is a closed mapping. Conversely, suppose $f$ is continuous and closed on $S$, then by Exercise 4.30 we have $f(\overline{A})\subseteq\overline{f(A)}$, and if $A\subseteq S$, then $\overline{A}$ is closed, thus the image $f(\overline{A})$ is closed in $T$. Since $f(A)\subseteq f(\overline{A})$, we can have $\overline{f(A)}\subseteq f(\overline{A})$, as $\overline{f(A)}$ is the smallest closed set containing $f(A)$. Combined we get $\overline{f(A)}=f(\overline{A})$.

### 4.33

Give an example of a continuous $f$ and a Cauchy sequence $\{x_n\}$ in some metric space $S$ for which $\{f(x_n)\}$ is not a Cauchy sequence in $T$.

#### Solution

Let $f(x)=1/x$ and $x_n=1/n$ in $S=(0,1]$.

### 4.34

Prove that the interval $(-1,1)$ in $\mathbf{R}^1$ is homeomorphic to $\mathbf{R}^1$. This shows that neither boundedness nor completeness is a topological property.

#### Proof

Let $f(x)=\tan{\pi x/2}$ on $(-1,1)$, then $f$ is continuous on $S=(-1,1)$ and $f(S)=\mathbf{R}^1$.

### 4.35

Section 9.7 contains an example of a function $f$, continuous on $[0, 1]$, with $f([0, 1]) = [0, 1 ]\times[0, 1]$. Prove that no such $f$ can be one-to-one on $[0, 1]$.  

#### Proof

Assume there exist one such $f$ which is one-to-one on $[0,1]$, then $f$ has an inverse $g=f^{-1}$ and $g$ is continuous on $S=[0, 1 ]\times[0, 1]$, also $g(S)=[0,1]$. Choose $a\in(0,1)$, then there exist point $\mathbf{x}\in S$ such that $g(\mathbf{x})=a$.  $S-\{\mathbf{x}\}$ is connected since it is arcwise connected and $[0,a)\cup(a,1]$ is obviously disconnected. If we define $h:S-\{\mathbf{x}\}\to[0,a)\cup(a,1]$ by $h(x)=g(x)$, then $h$ is continuous on its connected domain but its image set is disconnected. This is a contradiction.