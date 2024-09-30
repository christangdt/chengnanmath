# Exercise 10-16

### 2.10

Prove that if $A\thicksim B$ and $B\thicksim C$, then $A\thicksim C$.

#### Proof

Since $A\thicksim B$ and $B\thicksim C$, we can find one-to-one functions $F$ and $G$, with $F(A)=B$ and $G(B)=C$, thus $G\circ F$ is a one-to one function from $A$ onto $C$.

### 2.11

If $\{1,2,\dots,n\}\thicksim\{1,2,\dots,m\}$, prove that $m=n$.

#### Proof

Assume $m<n$, then let $F$ be the one-to-one function with $F\{1,2,\dots,n\}=\{1,2,\dots,m\}$, since there are $n$ possible variables to choose and the value can have only $m$ possible outcomes, $F$ cannot be one-to-one, this is a contradiction.
The case $m>n$ can be similarly proved.

### 2.12

If $S$ is an infinite set, prove that $S$ contains a countably infinite subset.

#### Proof

That $S$ is infinite means $S$ is not emtpy, choose $a\in S$, consider the set $S\backslash\{a\}$, assume this set is finite, then we have some integer $n$ such that $S\backslash\{a\}\thicksim\{1,2,\dots,n\}$, let $F$ be the one-to-one function with $F(S\backslash\{a\})=\{1,2,\dots,n\}$. Define $G$ with $G=F$ on $S\backslash\{a\}$ and $G(a)=n+1$, we can see that $G$ is a one-to-one function with $G(S)=\{1,2,\dots,n+1\}$, this means $S$ is finite, a contradiction. Thus $S\backslash\{a\}$ must be infinite. 

We let this $a=a_1$, and by the same argument, we can choose $a_2$ from $S\backslash\{a_1\}$, repeat the step we can choose $a_3,a_4,\dots$ and the set $\{a_1,a_2,\dots\}$ is a countably infinite subset of $S$.

### 2.13 

Prove that every infinite set $S$ contains a proper subset similar to $S$.

#### Proof

$S$ is infinite means $S$ is either countably infinite or uncountable. 

If $S$ is countably infinite, then $S$ is similar to $\{1,2,\dots,\}$, let $F$ be the one-to-one function with $F(\{1,2,\dots,\})=S$, let $G$ be the such that $G(n)=F(n+1)$ for natural numbers $n$, then $F\circ G$ is one-to-one from $\{1,2,\dots,\}$ to $S\backslash\{F(1)\}$, which means $F\circ G\circ F^{-1}$ is one-to-one from $S$ to $S\backslash\{F(1)\}$, thus $S$ is similar to $S\backslash\{F(1)\}$.

If $S$ is uncountable, then $S$ contains a countably infinite subset by Exercise 2.12, let this subset be $A$, choose $a\in A$, use the technique above we can prove that $A$ is similar to $A\backslash\{a\}$. Let $F$ be the one-to-one function such that $F(A)=A\backslash\{a\}$, let $G$ be the function such that $G=F$ on $A$ and $G(s)=s$ if $s\in S-A$, then $G$ is one-to-one with $G(S)=S\backslash\{a\}$, thus $S\backslash\{a\}$ is the proper subset we need.

### 2.14

If $A$ is a countable set and $B$ an uncountable set, prove that $B-A$ is similar to $B$.

#### Proof

The set $B\cap A$ is countable. Thus the set $B-A$ must be infinite, otherwise $B$ is countable. 

By Exercise 2.12, we can choose a countably infinite subset $C$ of $B-A$ and the set $S=C\cup(B\cap A)$ is still countably infinite. Notice that $B=(B-A)\cup(B\cap A)$, we can define a one-to-one function $F$ as follows:

Since $C$ and $C\cup(B\cap A)$ are both countable, they are similar, thus we find a one-to-one function $F'$ such that $F'(C)=C\cup(B\cap A)$, we let $F=F'$ on $C$, and $F(a)=a$ for all $a\in(B-A)-C$, then $F$ is a one-to-one function from $B-A$ to $B$.

### 2.15

A real number is called *algebraic* if it is a root of an algebraic equation $f(x)=0$, where $f(x)=a_0+a_1x+\cdots+a_nx^n$ is a polynomial with integer coefficients. Prove that the set of all polynomials with integer coefficients is countable and deduce that the set of algebraic numbers is also countable.

#### Proof

Let $A_n$ be the set of all polynomials with integer coefficients and with degree $n$, i.e.
$$
A_n=\{a_0+a_1x+\cdots+a_nx^n:n\in\mathbf{N}\}
$$
Since there are countable choicesfor each $a_i$ with $0\leq i\leq n$, the set $A_n$ is countable as it is a finite collection of countable sets, thus $\cup_{n=1}^{\infty}A_n$ is also countable.

For each $f\in A_n$, the total amount of algebraic numbers $x$ which makes $f(x)=0$ is no more than $n$, which means the set of algebraic numbers that belongs to polynomial with integer coefficients with degree $n$ is countable, and the conclusion follows.

### 2.16

Let $S$ be a finite set consisting of $n$ elements and let $T$ be the collection of all subsets of $S$. Show that $T$ is a finite set and find the number of elements in $T$.

#### Solution

There are $2^n$ elements in $T$. Since for each of the $n$ elements in $S$, it may or may not be in any subset of $S$.