# Exercise 1-14 (Sequences)

### 8.1

a) Given a real-valued sequence $\{a_n\}$ bounded above, let $u_n=\sup\{a_k:k\ge n\}$. Then $u_n\searrow$ and hence $U=\lim_{n\to\infty}u_n$ is either finite or $-\infty$. Prove that
$$
U=\limsup_{n\to\infty}a_n=\lim_{n\to\infty}(\sup\{a_k:k\ge n\}).
$$
b) Similarly, if $\{a_n\}$ is bounded below, prove that
$$
V=\liminf_{n\to\infty}a_n=\lim_{n\to\infty}(\inf\{a_k:k\ge n\}).
$$
If $U$ and $V$ are finite, show that:

c) There exists a subsequence of $\{a_n\}$ which converges to $U$ and a subsequence of $\{a_n\}$ which converges to $V$.

d) If $U=V$, every subsequence of $\{a_n\}$ converges to $U$.

#### Proof

(a) First suppose $U$ is finite, then for every $\varepsilon>0$, there exists $N$ such that $n>N$ implies $|u_n-U|<\varepsilon$, thus $U-\varepsilon<u_n<U+\varepsilon$, by definition, we have $a_n\le u_n$ for all $n>N$, thus $a_n<U+\varepsilon$ for all $n>N$, also, if given $\varepsilon>0$ and given $m>0$, we first find an integer $N$ such that $n>N$ implies $U-\varepsilon/2<u_n$, let $n'>\max(N,m)$, then $U-\varepsilon/2<u_{n'}$, then there exists some $a_n$ with $n\ge n'$ which satisfies $u_n'-a_n<\varepsilon/2$, combined we get $U-\varepsilon/2<a_n+\varepsilon/2$, or $U-\varepsilon<a_n$. This means $U=\limsup_{n\to\infty}a_n$.

Next suppose $U=-\infty$, then for any $G>0$, we can find $u_n$ such that $u_n<-G$, thus $a_n<-G$, so $\{a_n\}$ is not bounded below. To see that $\{a_n\}$ has no finite limit superior, let $U'$ be a finite number, then $U'-\varepsilon$ is a finite number for any given $\varepsilon>0$, then we can find $m$ such that $u_m<U'-\varepsilon$, but this means $a_n<U'-\varepsilon$ for any $n>m$, thus $U'$ does not satisfy condition (ii) in Definition 8.2, thus cannot be a limit superior of $\{a_n\}$. This means $\limsup_{n\to\infty}a_n=-\infty$.

(b) Let $b_n=-a_n$, then $\{b_n\}$ is bounded above, let $u_n=\sup\{b_k:k\ge n\}$, then $u_n\ge b_k$ for all $k\ge n$, thus $-u_n\le a_k$ for all $k\ge n$, which means $-u_n=\inf\{b_k:k\ge n\}$. Let $V=\lim_{n\to\infty}(-u_n)$, then
$$
V=-\lim_{n\to\infty}u_n=-\limsup_{n\to\infty}b_n=\liminf_{n\to\infty}a_n
$$
(c) For $k=1,2,\dots$, there exist an integer $N$ such that $a_n<U+1$ for any $n>N$, given this $N$, we can find some integer $n_1>N$ such that $a_{n_1}>U-1$, suppose we have chosen $a_{n_k}$, we choose $a_{n_{k+1}}$ as follows: first there exist an integer $N\ge{n_k}$ such that $a_n<U+\frac{1}{k+1}$ for any $n>N$, given this $N$, we can find some integer $n_{k+1}>N$ such that $a_{n_{k+1}}>U-\frac{1}{k+1}$, this means $|a_{n_k}-U|<\frac{1}{k}$ for all $k$. The subsequence $\{a_{n_k}\}$ converges to $U$. The proof of the existence of a subsequence of $\{a_n\}$ which converges to $V$ is similar and is omitted.

(d) We only need to prove $\{a_n\}$ converges to $U$. For every $\varepsilon>0$, by definition of $U$ and $V$, we can find $N$ such that $n>N$ implies $a_n<U+\varepsilon$, and we can find $N'$ such that $n>N'$ implies $a_n>V-\varepsilon$. Hence $n>\max(N,N')$ implies $U-\varepsilon<a_n<U+\varepsilon$.

### 8.2

Given two real-valued sequences $\{a_n\}$ and $\{b_n\}$ bounded below. Prove that

a) $\limsup_{n\to\infty}(a_n+b_n)\le\limsup_{n\to\infty}a_n+\limsup_{n\to\infty}b_n$.

b) $\limsup_{n\to\infty}(a_nb_n)\le(\limsup_{n\to\infty}a_n)(\limsup_{n\to\infty}b_n)$ if $a_n>0,b_n>0$ for all $n$, and if both $\limsup_{n\to\infty}a_n$ and $\limsup_{n\to\infty}b_n$ are finite or both are infinite.

#### Proof

(a) If one of $\limsup_{n\to\infty}a_n$ and $\limsup_{n\to\infty}b_n$ is $+\infty$, then the inequality obviously holds since the right side is $+\infty$. Now suppose $U=\limsup_{n\to\infty}a_n$ and $V=\limsup_{n\to\infty}b_n$ are both finite, and assume $\limsup_{n\to\infty}(a_n+b_n)>U+V$, let
$$
\varepsilon=\dfrac{\limsup_{n\to\infty}(a_n+b_n)-U-V}{2}>0
$$
then we can find $N_1$ such that $n>N_1$ implies $a_n<U+\varepsilon/2$, and we can find $N_2$ such that $n>N_2$ implies $b_n<V+\varepsilon/2$, so that $n>N=\max(N_1,N_2)$ implies $a_n+b_n<U+V+\varepsilon$, and given this $N$, we can find an integer $k>N$ such that $a_k+b_k>\limsup_{n\to\infty}(a_n+b_n)-\varepsilon$, this means
$$
\limsup_{n\to\infty}(a_n+b_n)-\varepsilon<a_k+b_k<U+V+\varepsilon\implies\varepsilon=\dfrac{\limsup_{n\to\infty}(a_n+b_n)-U-V}{2}<\varepsilon
$$
which is a contradiction. Hence we must have $\limsup_{n\to\infty}(a_n+b_n)\le U+V$.

(b) If both $\limsup_{n\to\infty}a_n$ and $\limsup_{n\to\infty}b_n$ are infinite, then we shall have $\limsup_{n\to\infty}a_n=\limsup_{n\to\infty}b_n=+\infty$, thus the inequality obviously holds since the right side is $+\infty$. Now suppose $U=\limsup_{n\to\infty}a_n$ and $V=\limsup_{n\to\infty}b_n$ are both finite, we have $U\ge 0$ and $V\ge 0$, which means both $\{a_n\}$ and $\{b_n\}$ are bounded above, so we can find $M>1$ such that $a_n\le M$ and $b_n\le M$ for all $n$. Thus $U\le M$ and $V\le M$. Assume $\limsup_{n\to\infty}(a_nb_n)>UV$. Let
$$
\varepsilon=\min\left(\limsup_{n\to\infty}(a_nb_n)-UV,1\right)>0
$$
then we can find $N_1$ such that $n>N_1$ implies $a_n<U+\varepsilon/(3M)$, and we can find $N_2$ such that $n>N_2$ implies $b_n<V+\varepsilon/(3M)$, so that $n>N=\max(N_1,N_2)$ implies
$$
a_nb_n<\left(U+\dfrac{\varepsilon}{3M}\right)\left(V+\dfrac{\varepsilon}{3M}\right)=UV+\dfrac{(U+V)\varepsilon}{3M}+\dfrac{\varepsilon^2}{9M^2}\le UV+\dfrac{2M\varepsilon}{3M}+\dfrac{\varepsilon}{9}=UV+\dfrac{7\varepsilon}{9}
$$
given this $N$, we can find an integer $k>N$ such that $a_kb_k>\limsup_{n\to\infty}(a_nb_n)-\frac{1}{9}\varepsilon$, this means
$$
\limsup_{n\to\infty}(a_nb_n)-\dfrac{1}{9}\varepsilon<a_kb_k<UV+\dfrac{7\varepsilon}{9}\implies\varepsilon\le\limsup_{n\to\infty}(a_nb_n)-UV<\dfrac{8}{9}\varepsilon<\varepsilon
$$
which is a contradiction. Hence we must have $\limsup_{n\to\infty}(a_nb_n)\le UV$.

### 8.3

Prove Theorems 8.3 and 8.4.

#### Proof

**Proof of Theorem 8.3:**

(a) If either $\liminf_{n\to\infty}a_n$ or $\limsup_{n\to\infty}a_n$ is not finite, then the inequality obviously holds. Suppose $\liminf_{n\to\infty}a_n=u$ and $\limsup_{n\to\infty}a_n=U$, both are finite, then for every $\varepsilon>0$ we can find $N$ such that $n>N$ implies $a_n<U+\varepsilon/2$ and $a_n>u-\varepsilon/2$, which means $u<U+\varepsilon$, thus $u\le U$.

(b) If $\limsup_{n\to\infty}a_n$ and $\liminf_{n\to\infty}a_n$ are both finite and equal, then $\{a_n\}$ converges due to Exercise 8.1(d). Conversely, if the sequence converges to $L$, then for every $\varepsilon>0$, we can find $N$ such that $n>N$ means $L-\varepsilon<a_n<L+\varepsilon$, thus the two conditions in Definition 8.2 are both satisfied, which means $\limsup_{n\to\infty}a_n=L$, similarly $\liminf_{n\to\infty}a_n=L$.

(c) If $\{a_n\}$ diverges to $+\infty$, then for any $G>0$ we can find $N>0$ such that $a_n>G$ for all $n>N$, this means $\liminf_{n\to\infty}a_n\ge G$, thus $\liminf_{n\to\infty}a_n=+\infty$, and use (a) we have $\limsup_{n\to\infty}a_n=+\infty$.

(d) Similar to the proof of (c).

**Proof of Theorem 8.4:**

We first prove $\limsup_{n\to\infty}a_n\le\limsup_{n\to\infty}b_n$. 

If $\limsup_{n\to\infty}b_n=+\infty$ there is nothing to prove. 

If $\limsup_{n\to\infty}b_n=U$ which is finite, assume $\limsup_{n\to\infty}a_n>U$, then let $\varepsilon=\limsup_{n\to\infty}a_n-U>0$, then there is $N$ such that $n>N$ implies $b_n<U+\varepsilon/2$, and for this $N$ there is $k>N$ such that $a_k>\limsup_{n\to\infty}a_n-\varepsilon/2$, thus
$$
\limsup_{n\to\infty}a_n-\dfrac{\varepsilon}{2}<a_k\le b_k<U+\dfrac{\varepsilon}{2}\implies{\varepsilon}=\limsup_{n\to\infty}a_n-U<\varepsilon
$$
which is a contradiction, so we have $\limsup_{n\to\infty}a_n\le U$. 

If $\limsup_{n\to\infty}b_n=-\infty$, then $\{b_n\}$ is bounded above but not bounded below, and has no finite limit superior, from $a_n\le b_n$ we see $\{a_n\}$ is bounded above but not bounded below. Assume $\limsup_{n\to\infty}a_n=U'$ which is finite, then there exist $N$ such that $b_n<U'-1$ for all $n>N$, and we can find $k>N$ such that $a_k>U'-1$, this is a contradiction. Thus $\{a_n\}$ has no finite limit superior, which means $\limsup_{n\to\infty}a_n=-\infty$. This completes the proof.

Next we prove $\liminf_{n\to\infty}a_n\le\liminf_{n\to\infty}b_n$. Since $-b_n\le-a_n$, use the conclusion just proven we have $\limsup_{n\to\infty}(-b_n)\le\limsup_{n\to\infty}(-a_n)$, thus
$$
\liminf_{n\to\infty}a_n=-\limsup_{n\to\infty}(-a_n)\le-\limsup_{n\to\infty}(-b_n)=\liminf_{n\to\infty}b_n
$$

### 8.4

If each $a_n>0$, prove that
$$
\liminf_{n\to\infty}\dfrac{a_{n+1}}{a_n}\le\liminf_{n\to\infty}\sqrt[n]{a_n}\le\limsup_{n\to\infty}\sqrt[n]{a_n}\le\limsup_{n\to\infty}\dfrac{a_{n+1}}{a_n}.
$$

#### Proof

We first prove the inequality at the right side. If $\limsup_{n\to\infty}\dfrac{a_{n+1}}{a_n}=+\infty$, there is nothing to prove. Suppose $\limsup_{n\to\infty}\dfrac{a_{n+1}}{a_n}=U$, assume $\limsup_{n\to\infty}\sqrt[n]{a_n}>U$, let $\varepsilon=(\limsup_{n\to\infty}\sqrt[n]{a_n}-U)/4>0$, then there exist $N$ such that $n>N$ implies $\dfrac{a_{n+1}}{a_n}<U+\varepsilon$, for this $N$ we define $A_N:=a_{N+1}/(U+\varepsilon)^{N+1}>0$, since $A_N$ is a fixed number, we have $\lim_{n\to\infty}\sqrt[n]{A_n}=1$, so there exists $N'>N$ such that
$$
\sqrt[n]{A_N}<\dfrac{U+2\varepsilon}{U+\varepsilon},\qquad\forall n>N'
$$
given this $N'$, we can find $k>N'+2$ such that $\sqrt[k]{a_k}>\limsup_{n\to\infty}\sqrt[n]{a_n}-\varepsilon$, we also have
$$
a_k=\dfrac{a_k}{a_{k-1}}\dfrac{a_{k-1}}{a_{k-2}}\cdots\dfrac{a_{N+2}}{a_{N+1}}a_{N+1}\le a_{N+1}(U+\varepsilon)^{k-N-1}=\dfrac{a_{N+1}}{(U+\varepsilon)^{N+1}}(U+\varepsilon)^k=A_N(U+\varepsilon)^k
$$
thus
$$
\limsup_{n\to\infty}\sqrt[n]{a_n}-\varepsilon<\sqrt[k]{a_k}\le\sqrt[k]{A_N}(U+\varepsilon)<U+2\varepsilon\implies\limsup_{n\to\infty}\sqrt[n]{a_n}-U<3\varepsilon
$$
which means $\varepsilon<\frac{3}{4}\varepsilon$, a contradiction since $\varepsilon>0$. Thus $\limsup_{n\to\infty}\sqrt[n]{a_n}\le U$.

The proof of $\liminf_{n\to\infty}\dfrac{a_{n+1}}{a_n}\le\liminf_{n\to\infty}\sqrt[n]{a_n}$ can be similarly done.

The inequality in the middle is obvious from Theorem 8.3(a).

### 8.5

Let $a_n=n^n/n!$. Show that $\lim_{n\to\infty}a_{n+1}/a_n=e$ and use Exercise 8.4 to deduce that
$$
\lim_{n\to\infty}\dfrac{n}{(n!)^{1/n}}=e.
$$

#### Proof

We have
$$
\dfrac{a_{n+1}}{a_n}=\dfrac{(n+1)^{n+1}n!}{n^n(n+1)!}=\dfrac{(n+1)^n}{n^n}=\left(1+\dfrac{1}{n}\right)^n\implies\lim_{n\to\infty}\dfrac{a_{n+1}}{a_n}=e
$$
Since the sequence $\{a_{n+1}/a_n\}$ is convergent, by Theorem 8.3(b) we have $e=\liminf_{n\to\infty}\dfrac{a_{n+1}}{a_n}=\limsup_{n\to\infty}\dfrac{a_{n+1}}{a_n}$, this means $e=\liminf_{n\to\infty}\dfrac{n}{(n!)^{1/n}}=\limsup_{n\to\infty}\dfrac{n}{(n!)^{1/n}}$ since $\sqrt[n]{a_n}=\dfrac{n}{(n!)^{1/n}}$, the conclusion follows again from Theorem 8.3(b).

### 8.6

Let $\{a_n\}$ be a real-valued sequence and let $\sigma_n=(a_1+\cdots+a_n)/n$. Show that
$$
\liminf_{n\to\infty}{a_n}\le\liminf_{n\to\infty}\sigma_n\le\limsup_{n\to\infty}\sigma_n\le\limsup_{n\to\infty}{a_n}.
$$

#### Proof

We first prove the inequality at the right side. If $\limsup_{n\to\infty}{a_n}=+\infty$ there is nothing to prove. 

If $\limsup_{n\to\infty}{a_n}=-\infty$, then $\{a_n\}$ is bounded above and not bounded below and has no finite limit superior. Choose $M>0$ such that $a_n\le M$ for all $n$, then $\sigma_n=(a_1+\cdots+a_n)/n\le nM/n=M$ for all $n$, so $\{\sigma_n\}$ is bounded above. By Exercise 8.1, we know that $\lim_{n\to\infty}(\sup\{a_k:k\ge n\})=-\infty$, let $G>0$ be any finite number, then there exists an integer $N$ such that $n>N$ implies $a_n<-2G-2$, choose $k>2N$ such that $k>a_1+\cdots+a_N$, then
$$
\sigma_k=\dfrac{a_1+\cdots+a_k}{k}=\dfrac{a_1+\cdots+a_N}{k}+\dfrac{a_{N+1}+\cdots+a_k}{k}<1+\dfrac{k-N}{k}(-2G-2)<1+\dfrac{1}{2}(-2G-2)=-G
$$
this shows $-G$ is not a lower bound of $\{\sigma_n\}$ and $\{\sigma_n\}$ is not bounded below. In the proof above notice that any $k>\max(2N,\sum_{i=1}^Na_i)$ can satisfy $\sigma_k<-G$, thus $\{\sigma_n\}$ cannot have any finite limit superior. We conclude $\limsup_{n\to\infty}\sigma_n=-\infty$.

If $\limsup_{n\to\infty}{a_n}=U$ which is finite, assume $\limsup_{n\to\infty}\sigma_n>U$, let $\varepsilon=(\limsup_{n\to\infty}\sigma_n-U)/3>0$, then there exists an integer $N$ such that $a_n<U+\varepsilon$ for any $n>N$, and there exists $N'>N$ such that $(a_1+\cdots+a_N)/N'<\varepsilon$, for this $N'$, we can find $k>N'$ such that $\sigma_k>\limsup_{n\to\infty}\sigma_n-\varepsilon$, which means
$$
\limsup_{n\to\infty}\sigma_n-\varepsilon<\sigma_k=\dfrac{\sum_{i=1}^Na_i}{k}+\dfrac{\sum_{i=N+1}^ka_i}{k}<\varepsilon+\left(1-\dfrac{N}{k}\right)(U+\varepsilon)<U+2\varepsilon
$$
which means $\limsup_{n\to\infty}\sigma_n-U<3\varepsilon$ or $\varepsilon<\varepsilon$, a contradiction. Thus $\limsup_{n\to\infty}\sigma_n\le U$ and the inequality at the right side is proved.

The inequality at the left side can be proved similarly. The inequality in the middle is obvious from Theorem 8.3(a).

### 8.7

Find $\limsup_{n\to\infty}a_n$ and $\liminf_{n\to\infty}a_n$ if $a_n$ is given by

a) $\cos{n}$,

b) $\left(1+\dfrac{1}{n}\right)\cos{n\pi}$,

c) $n\sin\dfrac{n\pi}{3}$,

d) $\sin\dfrac{n\pi}{2}\cos\dfrac{n\pi}{2}$,

e) $(-1)^nn/(1+n)^n$,

f) $\dfrac{n}{3}-\left[\dfrac{n}{3}\right]$.

#### Solution

(a) $\limsup_{n\to\infty}a_n=1$ and $\liminf_{n\to\infty}a_n=-1$.

(b) $\limsup_{n\to\infty}a_n=1$ and $\liminf_{n\to\infty}a_n=-1$.

(c) This sequence is not bounded above, not bounded below, thus $\limsup_{n\to\infty}a_n=+\infty$ and $\liminf_{n\to\infty}a_n=-\infty$.

(d) $a_n=\frac{1}{2}\sin{n\pi}$, thus $\limsup_{n\to\infty}a_n=\frac{1}{2}$ and $\liminf_{n\to\infty}a_n=-\frac{1}{2}$.

(e) $\limsup_{n\to\infty}a_n=0$ and $\liminf_{n\to\infty}a_n=0$.

(f)  $\limsup_{n\to\infty}a_n=\frac{2}{3}$ and $\liminf_{n\to\infty}a_n=0$.

### 8.8

Let $a_n=2\sqrt{n}-\sum_{k=1}^n1/\sqrt{k}$. Prove that the sequence $\{a_n\}$ converges to a limit $p$ in the interval $1<p<2$.

#### Proof

We have $a_1=2-1=1$ and
$$
\begin{aligned}a_{n+1}-a_n&=2\sqrt{n+1}-2\sqrt{n}-\dfrac{1}{\sqrt{n+1}}=\left(\dfrac{2}{\sqrt{n+1}+\sqrt{n}}\right)-\dfrac{1}{\sqrt{n+1}}
\\&=\dfrac{2\sqrt{n+1}-\sqrt{n+1}-\sqrt{n}}{(\sqrt{n+1}+\sqrt{n})\sqrt{n+1}}=\dfrac{\sqrt{n+1}-\sqrt{n}}{(\sqrt{n+1}+\sqrt{n})\sqrt{n+1}}
\\&=\dfrac{1}{(\sqrt{n+1}+\sqrt{n})^2\sqrt{n+1}}>0,\quad n\ge1
\end{aligned}
$$
thus $\{a_n\}$ is a monotonic increasing sequence. Also we have
$$
a_{n+1}-a_n=\dfrac{1}{(2n+1+2\sqrt{n(n+1)})\sqrt{n+1}}=\dfrac{1}{(2n+1)\sqrt{n+1}+(2n+2)\sqrt{n}}<\dfrac{1}{4n^{3/2}}
$$
so we can have $a_n<1+\sum_{k=1}^{n-1}\dfrac{1}{4k^{3/2}}$ for $n\ge2$, which means $a_n<1+\sum_{k=1}^{\infty}\dfrac{1}{4k^{3/2}}$ for all $n$. We also have
$$
\sum_{k=1}^{\infty}\dfrac{1}{4k^{3/2}}=\sum_{k=1}^{\infty}\dfrac{1}{4\sqrt{k}}\dfrac{1}{k}=\int_0^1\dfrac{1}{4\sqrt{x}}dx=\dfrac{1}{2}
$$
thus $a_n<3/2$ for all $n$, this means  $\{a_n\}$ converges to a limit $p$ by Theorem 8.6, and we shall have $p\le3/2$, also $p\ge a_2=a_1+\dfrac{1}{(\sqrt{2}-1)^2\sqrt{2}}>a_1=1$, which means $1<p<2$.



**In each of Exercises 8.9 through 8.14, show that the real-valued sequence $\{a_n\}$ is convergent. The given conditions are assumed to hold for all $n\ge1$. In Exercises 8.10 through 8.14, show that $\{a_n\}$ has the limit $L$ indicated.**

### 8.9

$|a_n|\le2$, $|a_{n+2}-a_{n+1}|\le\frac{1}{8}|a_{n+1}^2-a_n^2|$.

#### Solution

We have
$$
|a_{n+2}-a_{n+1}|\le\frac{1}{8}|a_{n+1}^2-a_n^2|=\frac{1}{8}|a_{n+1}-a_n||a_{n+1}+a_n|\le\frac{1}{2}|a_{n+1}-a_n|
$$
so
$$
|a_{n+1}-a_n|\le\frac{1}{2}|a_{n}-a_{n-1}|\le\cdots\le\frac{1}{2^{n-1}}|a_2-a_1|\le\frac{1}{2^{n-1}}(|a_2|+|a_1|)\le\frac{1}{2^{n-3}}
$$
thus for every $\varepsilon>0$ we can choose $N$ such that $|a_{n+1}-a_n|<\varepsilon/2$ whenever $n>N$, and for any $m\ge n$ we have
$$
|a_m-a_n|\le|a_m-a_{m-1}|+\cdots+|a_{n+1}-a_n|\le\left(1+\frac{1}{2}+\cdots+\frac{1}{2^{m-n-1}}\right)|a_{n+1}-a_n|\le2|a_{n+1}-a_n|<\varepsilon
$$
thus the sequence $\{a_n\}$ satisfies the Cauchy condition, thus is convergent.

### 8.10

$a_1\ge0,a_2\ge0,a_{n+2}=(a_na_{n+1})^{1/2},L=(a_1a_2^2)^{1/3}$.

#### Solution

We have
$$
a_n^2a_{n-1}=a_{n-1}a_{n-2}a_{n-1}=a_{n-1}^2a_{n-2}=\cdots=a_2^2a_1
$$
Also the relationship between $a_{n+2}$ and $a_{n+1},a_n$ can be described as:
$$
a_{n+1}=a_n\implies a_{n+2}=a_{n+1}=a_n
\\
a_{n+1}>a_n\implies a_n<a_{n+2}<a_{n+1}\implies a_n<a_{n+2}<a_{n+3}<a_{n+1}
\\
a_{n+1}<a_n\implies a_{n+1}<a_{n+2}<a_{n}\implies a_{n+1}<a_{n+3}<a_{n+2}<a_{n}
$$
Thus if $a_1=a_2$, then $\{a_n\}$ is constant, and $L=a_1=a_2=(a_1a_2^2)^{1/3}$. If $a_1>a_2$, then $a_1>a_3>a_2$, we shall have the subsequence $\{a_{2k}\}$ monotonic increasing and the subsequence $\{a_{2k+1}\}$ monotonic decreasing. If $a_1<a_2$, the subsequence $\{a_{2k}\}$ is monotonic decreasing and the subsequence $\{a_{2k+1}\}$ monotonic increasing. Either case means the subsequence $\{a_{2k}\}$ and $\{a_{2k+1}\}$ are convergent, since they are bounded between $a_1$ and $a_2$. Let $L_1=\lim_{k\to\infty}a_{2k}$ and $L_2=\lim_{k\to\infty}a_{2k+1}$, we have
$$
a_{2n+2}^2=a_{2n}a_{2n+1}\implies L_1^2=L_1L_2,\quad a_{2n+1}^2=a_{2n}a_{2n-1}\implies L_2^2=L_1L_2
$$
which means $L_1=L_2$ since they are both $\ge0$. This shows the sequence is convergent and $L=L_1=L_2$. Thus $a_2^2a_1=\lim_{n\to\infty}a_n^2a_{n-1}=L^3$.

### 8.11

$a_1=2,a_2=8,a_{2n+1}=\frac{1}{2}(a_{2n}+a_{2n-1}),a_{2n+2}=\dfrac{a_{2n}a_{2n-1}}{a_{2n+1}},L=4$.

#### Solution

If $a_{2n}>0$ and $a_{2n-1}>0$ we can easily deduce that $a_{2n+1}>0$ and $a_{2n+2}>0$, thus $a_n>0$ for all $n$. From $a_{2n+1}=\frac{1}{2}(a_{2n}+a_{2n-1})$ we know $a_{2n+1}\ge\min(a_{2n},a_{2n-1})$, and
$$
\begin{aligned}
a_{2n+2}=\dfrac{a_{2n}a_{2n-1}}{a_{2n+1}}&\implies\frac{1}{a_{2n+2}}=\frac{a_{2n+1}}{a_{2n}a_{2n-1}}=\frac{a_{2n}+a_{2n-1}}{2a_{2n}a_{2n-1}}=\frac{1}{2}\left(\frac{1}{a_{2n}}+\frac{1}{a_{2n-1}}\right)
\\&\implies\frac{1}{a_{2n+2}}\le\max\left(\frac{1}{a_{2n}},\frac{1}{a_{2n-1}}\right)
\\&\implies a_{2n+2}\ge\min(a_{2n},a_{2n-1})
\end{aligned}
$$
so use induction we can conclude $a_n\ge\min(a_2,a_1)=2$ for all $n$.

Next, we have
$$
a_{2n+1}-a_{2n}=-\frac{1}{2}(a_{2n}-a_{2n-1})
\\
\begin{aligned}a_{2n+2}-a_{2n+1}&=\dfrac{a_{2n}a_{2n-1}}{a_{2n+1}}-a_{2n+1}=\dfrac{a_{2n}a_{2n-1}-a_{2n+1}^2}{a_{2n+1}}=\dfrac{4a_{2n}a_{2n-1}-(a_{2n}+a_{2n-1})^2}{4a_{2n+1}}\\&=-\frac{(a_{2n}-a_{2n-1})^2}{4a_{2n+1}}=-\dfrac{a_{2n}-a_{2n-1}}{2}\frac{a_{2n}-a_{2n-1}}{2a_{2n+1}}=(a_{2n+1}-a_{2n})\frac{a_{2n}-a_{2n-1}}{a_{2n}+a_{2n-1}}
\end{aligned}
$$
thus $|a_{2n+1}-a_{2n}|=\frac{1}{2}|a_{2n}-a_{2n-1}|$ and $|a_{2n+2}-a_{2n+1}|<|a_{2n+1}-a_{2n}|$, use induction we get
$$
|a_{2n}-a_{2n-1}|<|a_{2n-1}-a_{2n-2}|=\frac{1}{2}|a_{2n-2}-a_{2n-3}|<\cdots<\frac{1}{2^{n-1}}|a_2-a_1|=\frac{6}{2^{n-1}}
$$
so for every $\varepsilon>0$ there exists $N$ such that $|a_{2n}-a_{2n-1}|<|a_{2n-1}-a_{2n-2}|<\min(\varepsilon/2,1)$ for all $n>N$, and if $n>N$, we also have
$$
|a_{2n+2}-a_{2n+1}|=|a_{2n+1}-a_{2n}|\left|\frac{a_{2n}-a_{2n-1}}{a_{2n}+a_{2n-1}}\right|<\frac{1}{4}|a_{2n+1}-a_{2n}|
$$
thus we conclude $|a_{n+2}-a_{n+1}|\le\frac{1}{2}|a_{n+1}-a_{n}|$ for all $n>2N$, so if $m>n>2N$, we have
$$
|a_m-a_n|\le\sum_{k=n}^{m-1}|a_{k+1}-a_k|\le\left(\sum_{i=0}^{m-n}\dfrac{1}{2^i}\right)|a_{n+1}-a_n|\le\left(\sum_{i=0}^{\infty}\dfrac{1}{2^i}\right)\frac{\varepsilon}{2}=\varepsilon
$$
and the sequence is convergent. Thus we have $a_{2n+2}a_{2n+1}=a_{2n}a_{2n-1}=\cdots=a_2a_1=16$, so $L^2=16$ and $L=4$.

### 8.12

$a_1=-\frac{3}{2},3a_{n+1}=2+a_n^3,L=1$. Modify $a_1$ to make $L=-2$.

#### Solution

If $a_n<1$, then $a_{n+1}=(2+a_n^3)/3<1$, also if $a_n>-2$, then $a_{n+1}>-6/3=-2$, since $-2<a_1<1$, we can conclude $-2<a_n<1$ for all $n$. We further have
$$
3a_{n+1}-3a_n=a_n^3-3a_n+2=a_n^3-1-3(a_n-1)=(a_n-1)(a_n^2+a_n-2)=(a_n-1)^2(a_n+2)>0
$$
thus $\{a_n\}$ is monotonic increasing, which means convergent. From $3L=2+L^3$ we have $(L-1)^2(L+2)=0$, since $L\ge-3/2$, we have $L=1$. To make $L=-2$, we can let $a_1=-3$.

### 8.13

$a_1=3,a_{n+1}=\dfrac{3(1+a_n)}{3+a_n},L=\sqrt{3}$.

#### Solution

If $a_n>\sqrt{3}$, then
$$
a_{n+1}=\dfrac{3(1+a_n)}{3+a_n}=1+\dfrac{2a_n}{3+a_n}=1+\dfrac{2}{\dfrac{3}{a_n}+1}>1+\dfrac{2}{\dfrac{3}{\sqrt{3}}+1}=1+\dfrac{2}{\sqrt{3}+1}=\sqrt{3}
$$
thus we have $a_n>\sqrt{3}$ for all $n$. Hence we have
$$
a_{n+1}-a_n=\dfrac{3(1+a_n)}{3+a_n}-a_n=\dfrac{3-a_n^2}{3+a_n}<0
$$
which shows  $\{a_n\}$ is monotonic decreasing, thus convergent. Let $n\to\infty$ we have $L=3(1+L)/(3+L)$, or $L^2=3$, thus $L=\sqrt{3}$ since $L\ge\sqrt{3}$.

### 8.14

$a_n=\dfrac{b_{n+1}}{b_n}$, where $b_1=b_2=1,b_{n+2}=b_n+b_{n+1}$, $L=\dfrac{1+\sqrt{5}}{2}$.

#### Solution

For all $n$ we have
$$
a_{n+1}=\frac{b_{n+2}}{b_{n+1}}=\frac{b_{n+1}+b_n}{b_{n+1}}=1+\frac{b_n}{b_{n+1}}=1+\frac{1}{a_n}\tag{1}
$$
Since $\{b_n\}$ is an monotonic increasing sequence with $b_n\ge1$ for all $n$, if we have $1\le a_n<2$, then we can deduce $1\le a_{n+1}<2$, since $a_1=1$, we have $1\le a_n<2$ for all $n$. So $\{a_n\}$ is bounded. We also have
$$
a_{n+1}-a_n=\frac{b_{n+2}}{b_{n+1}}-\dfrac{b_{n+1}}{b_n}=\frac{b_nb_{n+2}-b_{n+1}^2}{b_{n+1}b_n}
$$
and for $n>2$ we have
$$
\begin{aligned}b_nb_{n+2}-b_{n+1}^2&=b_n(b_n+b_{n+1})-(b_n+b_{n-1})^2
\\&=b_n^2+b_nb_{n+1}-b_n^2-b_{n-1}^2-2b_nb_{n-1}=b_n(b_n+b_{n-1})-b_{n-1}^2-2b_nb_{n-1}
\\&=b_n(b_n-b_{n-1})-b_{n-1}^2=b_{n-2}b_n-b_{n-1}^2
\end{aligned}
$$
since $b_1b_3-b_2^2=2-1=1$ and $b_2b_4-b_3^2=3-4=-1$, we can conclude that
$$
a_{2n}-a_{2n-1}=\frac{1}{b_{2n-1}b_{2n}},\quad a_{2n+1}-a_{2n}=-\frac{1}{b_{2n+1}b_{2n}}
$$
thus 
$$
a_{2n+1}-a_{2n-1}=a_{2n+1}-a_{2n}+a_{2n}-a_{2n-1}=\frac{1}{b_{2n-1}b_{2n}}-\frac{1}{b_{2n+1}b_{2n}}=\frac{b_{2n+1}-b_{2n-1}}{b_{2n-1}b_{2n}b_{2n+1}}>0
\\
a_{2n+2}-a_{2n}=a_{2n+2}-a_{2n+1}+a_{2n+1}-a_{2n}=\frac{1}{b_{2n+1}b_{2n+2}}-\frac{1}{b_{2n+1}b_{2n}}=\frac{b_{2n}-b_{2n+2}}{b_{2n}b_{2n+1}b_{2n+2}}<0
$$
The sequence $\{a_{2n}\}$ and $\{a_{2n+1}\}$ are monotonic, thus convergent, let $x=\lim_{n\to\infty}a_{2n}$ and $y=\lim_{n\to\infty}a_{2n+1}$, from equation (1) we see that $x=1+1/y$ and $y=1+1/x$, which means $xy=y+1=x+1$, thus $x=y=L$. Solve the equation $L=1+1/L$ we get $L=\dfrac{1+\sqrt{5}}{2}$.