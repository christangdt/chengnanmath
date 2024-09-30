# Exercise 18-22 (Upper bounds)

### 1.18

Show that the sup and inf of a set are uniquely determined whenever they exist.

#### Solution

Suppose a set $S$ has two sups $\alpha=\sup{S}$ and $\alpha'=\sup{S}$, then by definition of sup, we have $\alpha\leq\alpha'$ and $\alpha'\leq\alpha$, thus $\alpha=\alpha'$.
The case of inf can be similarly proved. 

### 1.19

Find the sup and inf of each of the following sets of real numbers:
a) All numbers of the form $2^{-p}+3^{-q}+5^{-r}$, where $p,q,r$ take on all positive integer values.
b) $S=\{x:3x^2-10x+3<0\}$.
c) $S=\{x:(x-a)(x-b)(x-c)(x-d)<0\}$, where $a<b<c<d$.

#### Solution

a) the sup is $3$ and the inf is $0$.
b) $3x^2-10x+3=(3x-1)(x-3)$, thus the sup is $3$ and the inf is $1/3$.
c) the sup is $d$ and the inf is $a$.

### 1.20

Prove the comparison property for suprema (Theorem 1.16).

#### Proof

Let $\alpha=\sup{T}$, then $\alpha\geq t,\forall t\in T$, which means $\alpha$ is an upper bound of $S$, by the completeness Axiom, $S$ has a supremum $\sup{S}$.
Assume $\alpha<\sup{S}$, then by Theorem 1.14 $\exists s\in S$, such that $\alpha<s\leq\sup{S}$, since $T$ is nonempty, there is $t\in T$, then we have $t\leq\alpha<s$, a contradiction to $s\leq t$. Thus we must have $\sup{S}\leq\alpha=\sup{T}$.

### 1.21

Let $A$ and $B$ be two sets of positive numbers bounded above, and let $a=\sup{A},b=\sup{B}$. Let $C$ be the set of all products of the form $xy$, where $x\in A$ and $y\in B$. Prove that $ab=\sup{C}$.

#### Proof

Obviously $a>0,b>0$, for $\forall c\in C$, there is $x\in A,y\in B$ s.t. $c=xy\leq ab$, thus $ab$ is an upper bound of $C$.
Next for $\forall\varepsilon>0$, let $\delta=\min\{\varepsilon,1/(a+b),a+b\}$, then by definition of $a$ and $b$, we can find $x'\in A,y'\in B$ such that
$$
a-\delta^2<x',\quad b-\delta^2<y'
$$
let $c'=x'y'$, then
$$
c'>(a-\delta^2)(b-\delta^2)=ab-[(a+b-\delta^2)\delta]\delta\geq ab-[(a+b)\delta]\delta\geq ab-\varepsilon
$$
which shows $ab$ is the least upper bound.

### 1.22

Given $x>0$ and an integer $k\geq 2$. Let $a_0$ denote the largest integer $\leq x$ and, assuming that $a_0,a_1,\dots,a_{n-1}$ have been defined, let $a_n$ denote the largest integer such that
$$
a_0+\dfrac{a_1}{k}+\dfrac{a_2}{k^2}+\dots+\dfrac{a_n}{k^n}\leq x
$$
a) Prove that $0\leq a_i\leq k-1$ for each $i=1,2,\dots$
b) Let $r_n=a_0+a_1k^{-1}+a_2k^{-2}+\cdots+a_nk^{-n}$ and show that $x$ is the sup of the set of rational numbers $r_1,r_2,\dots$

#### Solution

a) If $a_i>k-1$, then write $a_i=k+\delta$, we have $\delta\geq 0$ and
$$
a_0+\dfrac{a_1}{k}+\cdots+\dfrac{a_{i-1}+1}{k^{i-1}}\leq a_0+\dfrac{a_1}{k}+\cdots+\dfrac{a_{i-1}+1}{k^{i-1}}+\dfrac{\delta}{k^i}=a_0+\dfrac{a_1}{k}+\cdots+\dfrac{a_i}{k^i}\leq x
$$
gives a contradiction to the finding of $a_{i-1}$.
If $a_i<0$, we suppose $0\leq a_j\leq k-1$ for each $j=1,\dots,i-1$, as $a_i$ is the largest integer to make
$$
a_0+\dfrac{a_1}{k}+\dfrac{a_2}{k^2}+\dots+\dfrac{a_i}{k^i}\leq x
$$
we know that
$$
a_0+\dfrac{a_1}{k}+\dfrac{a_2}{k^2}+\dots+\dfrac{a_{i-1}}{k^{i-1}}=a_0+\dfrac{a_1}{k}+\dfrac{a_2}{k^2}+\dots+\dfrac{0}{k^i}>x
$$
this contradicts the search of $a_{i-1}$.
b) It is easy to see $x\geq r_n$ for all $r_n$, thus $x$ is an upper bound of the set $\{r_1,r_2,\dots\}$, we also have $x-r_n<1/k^n$ for each $n$, thus for any $x'<x$, we choose integer $m$ such that $1/k^m<x-x'$, then $x'<x-1/k^m<r_m\leq x$, which means $x'$ is not an upper bound of $\{r_1,r_2,\dots\}$