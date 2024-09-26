# Linear Combinations and Systems of Linear Equations

### Content Notes

#### Definition (linear combination)

Let $\mathsf{V}$ be a vector space and $S$ a nonempty subset of $\mathsf{V}$. A vector $v\in\mathsf{V}$ is called a **linear combination** of vectors of $S$ if there exist a finite number of vectors $u_1, u_2, . . . , u_n$ in $S$ and scalars $a_1, a_2, . . . , a_n$ in $F$ such that $v = a_1u_1 + a_2u_2 + \cdots + a_nu_n$. In this case we also say that $v$ is a linear combination of $u_1, u_2, . . . , u_n$ and call $a_1, a_2, . . . , a_n$ the **coefficients** of the linear combination.
Observe that in any vector space $\mathsf{V}$, $0v = 0$ for each $v \in\mathsf{V}$. Thus the zero vector is a linear combination of any nonempty subset of $\mathsf{V}$.

#### Definition (span)

Let $S$ be a nonempty subset of a vector space $\mathsf{V}$. The **span** of $S$, denoted span($S$), is the set consisting of all linear combinations of the vectors in $S$. For convenience, we define span$(\emptyset) = \{0\}$.

#### Theorem 1.5

The span of any subset $S$ of a vector space $\mathsf{V}$ is a subspace of $\mathsf{V}$. Moreover, any subspace of $\mathsf{V}$ that contains $S$ must also contain the span of $S$.

#### Definition (generate)

A subset $S$ of a vector space $\mathsf{V}$ **generates** (or **spans**) $\mathsf{V}$ if span$(S)=\mathsf{V}$ . In this case, we also say that the vectors of $S$ generate (or span) $\mathsf{V}$.

### Selected Exercises

#### 12

If $\mathsf{W}$ is a subspace of $\mathsf{V}$, then since $\text{span}(\mathsf{W})$ is the smallest subspace containing $\mathsf{W}$,  we have $\text{span}(\mathsf{W})\subset\mathsf{W}$, and we obviously have $\mathsf{W}\subset\text{span}(\mathsf{W})$, done.

Conversely, obvious since $\text{span}(\mathsf{W})$ is a subspace.

#### 13

For any $v\in\text{span}(S_1)$, we can find some vectors, say $u_1,\dots,u_n$ in $S_1$, such that $v=a_1u_1+\cdots+a_nu_n$ for scalars $a_1,\dots,a_n\in F$, that $S_1\subseteq S_2$ means $u_1,\dots,u_n$ are in $S_2$, so $v\in\text{span}(S_2)$.

#### 14

Let $A=\text{span}(S_1\cup S_2)$, and $B=\text{span}(S_1),C=\text{span}(S_2)$. We have

$\forall v\in A$, we can write $v=a_1u_1+\cdots+a_nu_n$, each $u_i$ belongs to either $S_1$ or $S_2$, so it is easy to write $v=v_1+v_2$ where $v_1\in B,v_2\in C$, thus $v\in B+C$.

Conversely, $\forall w\in B+C$, we can write $w=w_1+w_2$ where $w_1\in B$, thus a linear combination of vectors in $S_1$, and $w_2\in C$, thus a linear combination of vectors in $S_2$, this means $w_1$ and $w_2$ are both linear combinations of vectors in $S_1\cup S_2$, so $w\in A$.

#### 15

Let $A=\text{span}(S_1\cap S_2)$, and $B=\text{span}(S_1),C=\text{span}(S_2)$. We have

$\forall v\in A$, we can write $v=a_1u_1+\cdots+a_nu_n$, each $u_i$ belongs to both $S_1$ and $S_2$, thus $v\in B$ and $v\in C$, so $v\in B\cap C$.

One example of $A=B\cap C$ is
$$
S_1\cap S_2=\{(1,0,0)\},S_1=\{(1,0,0),(0,1,0)\},S_2=\{(1,0,0),(0,0,1)\}
$$
One example of $A\neq B\cap C$ is
$$
S_1=\{(0,1),(1,0)\},S_2=\{(1,1)\},S_1\cap S_2=\empty
$$

#### 16

Assume there is $u\in\text{span}(S)$ which can not be uniquely written, then we have
$$
u=a_1u_1+\cdots+a_nu_n=b_1v_1+\cdots+b_mv_m
$$
with $u_1,\dots,u_n,v_1,\dots,v_m$ all vectors in $S$. If we further add the condition $u\ne0$, then we can get a contradiction since
$$
a_1u_1+\cdots+a_nu_n=b_1v_1+\cdots+b_mv_m
\\
\implies a_1u_1+\cdots+a_nu_n-b_1v_1-\cdots-b_mv_m=0
\\
\implies a_1=\cdots=a_n=b_1=\cdots=b_m=0\implies u=0
$$

#### 17

$\mathsf{W}$ has finite dimension.

### Summary

这一节介绍线性组合，衍生于同一空间内的向量进行加法和数乘两种运算后的结果。线性组合与张成空间（span somewhat space）的概念有密切的联系。一组向量张成了某一空间，可以理解为这组向量足以“代表”该空间，但其中可能有冗余代表。