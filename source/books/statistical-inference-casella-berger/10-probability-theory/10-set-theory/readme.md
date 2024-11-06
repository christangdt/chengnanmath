# Set Theory

## Content Notes

#### Definition 1.1.1

The set $S$, of all possible outcomes of a particular experiment is called the *sample space* for the experiment.

#### Definition 1.1.2

An *event* is any collection of possible outcomes of an experiment, that is any subset of $S$ (including $S$ itself).

#### Theorem 1.1.4

For any three events $A$, $B$ and $C$, defined on a sample space $S$, 

a. Commutativity: $A\cup B=B\cup A$, $A\cap B=B\cap A$;

b. Associativity: $A\cup(B\cup C)=(A\cup B)\cup C$, $A\cap(B\cap C)=(A\cap B)\cap C$;

c. Distributive Laws: $A\cap(B\cup C)=(A\cap B)\cup(A\cap C)$, $A\cup(B\cap C)=(A\cup B)\cap(A\cup C)$;

d. DeMogan's Laws: $(A\cup B)^c=A^c\cap B^c$, $(A\cap B)^c=A^c\cup B^c$.

#### Remark

The operations of union and intersection can be extended to infinite collections of sets, countable or uncountable. A countable example can be
$$
\bigcup_{i=1}^{\infty}(1/i,1]=(0,1]
$$
An uncountable example can be
$$
\bigcup_{\alpha\in\R^+}(0,\alpha]=(0,+\infty)
$$

#### Definition 1.1.5

Two events $A$ and $B$ are *disjoint* (or *mutually exclusive*) if $A\cap B=\empty$. The events $A_1,A_2,\dots$ are *pairwise disjoint* (or *mutually exclusive*) if $A_i\cap A_j=\empty$ for all $i\ne j$. To conclude: disjoint sets are sets with no points in common.

#### Definition 1.1.6

If $A_1,A_2,\dots$ are pairwise disjoint and $\cup_{i=1}^{\infty}A_i=S$, then the collection $A_1,A_2,\dots$ forms a *partition* of $S$.

## Exercises 1.1-1.3

#### 1.1

(a) $S=\{HHHH,HHHT,HHTT,HTTT,TTTT\}$.

(b) All non-negative integer numbers, $S=[0,\infty)$.

(c) All positive integer numbers. $S=(0,\infty)$.

(d) All positive numbers. $S=(0,\infty)$.

(e) $S=[0,1]$.

#### 1.2

(a) We have
$$
\begin{aligned}
x\in A\setminus B&\iff (x\in A)\wedge(x\notin B)\iff (x\in A)\wedge(x\notin A\cap B)
\\&\iff (x\in A)\wedge(x\in B^c)\iff x\in A\cap B^c
\end{aligned}
$$
(b) If $x\in B$, then either $x\in A$ or $x\notin A$, thus either $x\in B\cap A$ or $x\in B\cap A^c$, this gives $B\subseteq(B\cap A)\cup(B\cap A^c)$. Conversely, if $x\in(B\cap A)\cup(B\cap A^c)$, then either $x\in B\cap A$ or $x\in B\cap A^c$, in both cases we have $x\in B$.

(c) We have
$$
x\in B\setminus A\iff(x\in B)\wedge(x\notin A)\iff(x\in B)\wedge(x\in A^c)\iff x\in B\cap A^c
$$
(d) Obviously $A\cup(B\cap A^c)\subseteq A\cup B$, if $x\in A\cup B$, then either $x\in A\subseteq A\cup(B\cap A^c)$, or $x\notin A$, then $x$ must belongs to $B$, so $x\in B\cap A^c\subseteq A\cup(B\cap A^c)$.

#### 1.3

(a) Obvious.

(b) First if $x\in A\cup(B\cup C)$, then at least one of $x\in A,x\in B,x\in C$ must hold. Thus $x\in(A\cup B)\cup C$, vise versa. Next we have
$$
\begin{aligned}
x\in A\cap(B\cap C)&\iff(x\in A)\wedge(x\in B\cap C)\iff(x\in A)\wedge(x\in B)\wedge(x\in C)
\\&\iff(x\in A\cap B)\wedge(x\in C)\iff x\in (A\cap B)\cap C
\end{aligned}
$$
(c) We have
$$
\begin{aligned}
x\in(A\cup B)^c&\iff x\notin A\cup B\iff(x\notin A)\wedge(x\notin B)\\&\iff(x\in A^c)\wedge(x\in B^c)\iff x\in A^c\cap B^c
\\
x\in(A\cap B)^c&\iff x\notin (A\cap B)\iff(x\notin A)\vee(x\notin B)\\&\iff(x\in A^c)\vee(x\in B^c)\iff x\in A^c\cup B^c
\end{aligned}
$$

