# Exercise 1-9 (Limits of sequences)

### 4.1

Prove each of the following statements about sequences in $\mathbf{C}$.

a) $z^n\to 0$ if $|z|<1$; $\{z^n\}$ diverges if $|z|>1$.

b) If $z_n\to 0$ and if $\{c_n\}$ is bounded, then $c_nz_n\to 0$.

c) $z^n/n!\to 0$ for every complex $z$.

d) If $a_n=\sqrt{n^2+2}-n$, then $a_n\to 0$.

#### Solution

We let $z=a+bi$ for $a,b\in\mathbf{R}$ in (a),(b) and (c).

a) If $|z|<1$, then $|z^n-0|=|z^n|=|z|^n\to 0$. Thus $z^n\to 0$. If $|z|>1$, then $|z^n|=|z|^n\to\infty$, thus $z^n$ diverges.

b) We can find $M\in\mathbf{R}^+$ such that $|c_n|\leq M$, then $|c_nz_n|\leq M|z_n|\to 0$.

c) Since $|z^n/n!|\leq|z|^n/n!$ and $a^n/n!\to 0$ for any real number $a\geq 0$.

d) Since $0<a_n=\dfrac{2}{\sqrt{n^2+2}+n}<\dfrac{2}{n}\to 0$.

### 4.2

If $a_{n+2}=(a_{n+1}+a_n)/2$ for all $n\geq 1$, show that $a_n\to(a_1+2a_2)/3$.

#### Solution

We have
$$
a_{n+2}-a_{n+1}=\dfrac{a_{n+1}+a_n}{2}-a_{n+1}=\dfrac{a_n-a_{n+1}}{2}
$$
let $b_n=a_{n+1}-a_n$, then $b_{n+1}=-b_n/2$, thus $b_n\to 0$ and
$$
b_n=\left(-\dfrac{1}{2}\right)^{n-1}b_1=\left(-\dfrac{1}{2}\right)^{n-1}(a_2-a_1)
$$
as $a_{n+1}=\sum_1^nb_i+a_1$, we have
$$
\begin{aligned}
a_{n}&=\sum_{i=1}^{n-1}b_i+a_1=a_1+(a_2-a_1)\sum_{i=0}^{n-2}\left(-\dfrac{1}{2}\right)^i
\\&=a_1+(a_2-a_1)\dfrac{1-(-1/2)^{n-2}}{3/2}
\end{aligned}
$$
thus $a_n\to a_1+2(a_2-a_1)/3=(a_1+2a_2)/3$.

### 4.3

If $0<x_1<1$ and if $x_{n+1}=1-\sqrt{1-x_n}$ for all $n\geq 1$, prove that $\{x_n\}$ is a decreasing sequence with limit $0$. Prove also that $x_{n+1}/x_n\to\frac{1}{2}$.

#### Solution

If $0<x_n<1$, then $0<x_{n+1}<1$, we can conclude that $0<x_n<1$ for all $n$, let $y_n=1-x_n$, then $0<y_n<1$ and $\sqrt{y_n}=y_{n+1}$, it is easy to see $y_n<y_{n+1}$, or $y_n$ is an increasing sequence, thus $x_n$ is a decreasing sequence, thus both $x_n$ and $y_n$ converges, as $y_n\to 1$, we have $x_n\to 0$. Also, we have
$$
\dfrac{x_{n+1}}{x_n}=\dfrac{1-\sqrt{1-x_n}}{x_n}=\dfrac{1-(1-x_n)}{x_n(1+\sqrt{1-x_n})}=\dfrac{1}{1+\sqrt{1-x_n}}
$$
since $x_n\to 0$, we see $x_{n+1}/x_n\to\frac{1}{2}$.

### 4.4

Two sequences of positive integers $\{a_n\}$ and $\{b_n\}$ are defined recursively by taking $a_1=b_1=1$ and equating rational and irrational parts in the equation
$$
a_n+b_n\sqrt{2}=(a_{n-1}+b_{n-1}\sqrt{2})^2,\quad n\geq 2
$$
Prove that $a_n^2-2b_n^2=1$ for $n\geq 2$. Deduce that $a_n/b_n\to \sqrt{2}$ through values $>\sqrt{2}$, and that $2b_n/a_n\to\sqrt{2}$ through values $<\sqrt{2}$.

#### Solution

Use the equation we get $a_n=a_{n-1}^2+2b_{n-1}^2$ and $b_n=2a_{n-1}b_{n-1}$ for $n\geq 2$, since $a_1=b_1=1$, we know that $a_2=3,b_2=2$ and $a_2^2-2b_2^2=1$. Suppose that $a_k^2-2b_k^2=1$ for $2\leq k\leq n-1$, then
$$
a_n^2-2b_n^2=(a_{n-1}^2+2b_{n-1}^2)^2-2(4a_{n-1}^2b_{n-1}^2)=(a_{n-1}^2-2b_{n-1}^2)^2=1
$$
By induction, $a_n^2-2b_n^2=1$ for $n\geq 2$. 

From the expression of $a_n$ we see that $a_2=3>2$, and if $a_k>k>1$, then $a_{k+1}>a_k^2\geq(k+1)^2>k+1$, thus $a_n\geq n>1$ for all $n\geq 2$, this further means $a_n>a_{n-1}$,  so $\{a_n\}$ is increasing and tends to infinity, so is $\{b_n\}$. We now have
$$
\dfrac{a_n^2}{b_n^2}=2+\dfrac{1}{b_n^2}\implies\dfrac{a_n}{b_n}>\sqrt{2},\dfrac{a_n}{b_n}\to\sqrt{2}
\\
\dfrac{4b_n^2}{a_n^2}=\dfrac{4b_n^2}{1+2b_n^2}=2-\dfrac{2}{1+2b_n^2}\implies\dfrac{2b_n}{a_n}<\sqrt{2},\dfrac{2b_n}{a_n}\to\sqrt{2}
$$

### 4.5

A real sequence ${x_n}$ satisfies $7x_{n+1}=x_n^3+6$ for $n\geq 1$, if $x_1=1/2$, prove that the sequence increases and find its limit. What happens if $x_1=3/2$ or if $x_1=5/2$?

#### Solution

If $x_n<1$, then $x_n^3<1$, which gives $x_{n+1}<1$, thus we can conclude $x_n<1$ for all $n$ if $x_1=1/2$, and from $7x_{n+1}=x_n^3+6$ we get
$$
x_{n+1}-x_n=\dfrac{(x_n-1)(x_n^2-6)}{7}>0
$$
thus the sequence is increasing, since it is bounded, it must converge, let $x_n\to a$, we see that $7a=a^3+6$, thus $a=1$ since $0<x_n<1$ limits the possible value of $a$.

If $x_1=3/2$, then it is easy to see that $x_{n+1}<x_n$ and $1<x_n<3/2$ for all $n\geq 2$, thus the sequence decreases, and its limit is also $1$.

If $x_1=5/2$, then $x_n$ increases, and the sequence has no limit.

### 4.6

If $|a_n|<2$ and $|a_{n+2}-a_{n+1}|\leq\frac{1}{8}|a_{n+1}^2-a_n^2|$ for all $n\geq 1$, prove that $\{a_n\}$ converges.

#### Solution

Let $b_n=|a_{n+1}-a_n|$, then we have
$$
b_{n+2}\leq\dfrac{1}{8}b_{n+1}|a_{n+1}+a_n|\leq\dfrac{1}{8}b_{n+1}(|a_{n+1}|+|a_n|)\leq\dfrac{1}{2}b_{n+1}
$$
thus $b_n\to 0$, if $m>n$ we have
$$
|a_m-a_n|\leq\sum_{k=n}^mb_k\leq 2b_n
$$
This implies $\{a_n\}$ is a Cauchy sequence, so $\{a_n\}$ converges.

### 4.7

In a metric space $(S,d)$, assume that $x_n\to x$ and $y_n\to y$. Prove that $d(x_n,y_n)\to d(x,y)$.

#### Solution

For $\forall\varepsilon>0$, we can find $N>0$ such that $d(x_n,x)<\varepsilon/2,d(y_n,y)<\varepsilon/2$ if $n>N$, we also have
$$
d(x_n,y_n)\leq d(x_n,x)+d(x,y)+d(y,y_n)<d(x,y)+\varepsilon
\\
d(x,y)\leq d(x,x_n)+d(x_n,y_n)+d(y_n,y)<d(x_n,y_n)+\varepsilon
$$
which shows $|d(x,y)-d(x_n,y_n)|<\varepsilon$ when $n>N$.

### 4.8

Prove that in a compact metric space $(S, d)$, every sequence in $S$ has a subsequence which converges in $S$. This property also implies that $S$ is compact but you are not required to prove this.  

#### Proof

Let $\{x_n\}$ be a sequence in $S$ and let $A=\{x_1,x_2,\dots\}$ denote the range of $\{x_n\}$. If $A$ is finite,  then for each $N$, at least one element $a^*\in A$ will be reached with some $x_n,n>N$, assume not, then for every element $a\in A$, we can find a number $N_a$ such that $x_n\neq a, n>N_a$, since $A$ is finite, we can find a number $K=\max_{a\in A}{N_a}$, which guarantees $x_{K+1}\notin A$, this contradicts the definition of $A$. Now we select a subsequence of $\{x_n\}$ with $x_n=a^*$, this subsequence converges.

If $A$ is infinite, Theorem 3.38 tells us that $A$ has an accumulation point $p$ in $S$,  we first prove that in any ball $B(p;r)$ there are infinitely many points of $A$, assume not, then there exists some ball $B(p;r^*)$ with only finite many points $a_1,\dots,a_m$ of $A$, let
$$
r'=\dfrac{1}{2}\min\{d(p,a_1),\dots,d(p,a_m)\}
$$
then $A\cap B(p;r')=\empty$, a contradiction. Now choose some $x_i$ such that $d(x_i,p)<1$, and let $i=n_1$, let
$$
n_k=\min\left\{n>n_{k-1}:d(x_{n_k},p)<\dfrac{1}{k}\right\}
$$
then the subsequence $\{x_{n_k}\}$ converges to $p$.

### 4.9

Let $A$ be a subset of a metric space $S$. If $A$ is complete, prove that $A$ is closed. Prove that the converse also holds if $S$ is complete.  

#### Solution

Let $p$ be an accumulation point of $A$, then there is a sequence $\{a_n\}$ in $A$ which converges to $p$ by choosing $a_n\in A$ inside the ball $B(p;1/n)$, since $A$ is complete, we see that $p\in A$, and thus $A$ contains all its accumulation points, so $A$ is closed.

If $A$ is closed and $S$ is complete, let $\{a_n\}$ be a Cauchy sequence in $A$, then it converges in $S$ to some point $p$, by definition, $p$ is  an accumulation point of $A$, thus $p\in A$, this means $A$ is complete.