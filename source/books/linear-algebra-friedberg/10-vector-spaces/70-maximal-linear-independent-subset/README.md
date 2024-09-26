# Maximal Linearly Independent Subsets

### Content Notes

#### Definition (Maximal)

Let $\mathcal{F}$ be a family of sets. A member $M$ of $\mathcal{F}$ is called **maximal** (with respect to set inclusion) if $M$ is contained in no member of $\mathcal{F}$ other than $M$ itself.

#### Definition (chain)

A collection of sets $\mathcal{C}$ is called a **chain** (or **nest** or **tower**) if for each pair of sets $A$ and $B$ in $\mathcal{C}$, either $A\subseteq B$ or $B\subseteq A$.

#### Maximal Principle

Let $\mathcal{F}$ be a family of sets. If, for each chain $\mathcal{C}\subseteq\mathcal{F}$, there exists a member of $\mathcal{F}$ that contains each member of $\mathcal{C}$, then $\mathcal{F}$ contains a maximal member.

#### Definition (maximal linearly independent subset)

Let $S$ be a subset of a vector space $\mathsf{V}$. A **maximal linearly independent subset** of $S$ is a subset $B$ of $S$ satisfying both of the following conditions.

(a) $B$ is linearly independent.

(b) The only linearly independent subset of $S$ that contains $B$ is $B$ itself.

#### Theorem 1.12

Let $\mathsf{V}$ be a vector space and $S$ a subset that generates $\mathsf{V}$. If $\beta$ is a maximal linearly independent subset of $S$, then $\beta$ is a basis for $\mathsf{V}$.

#### Theorem 1.13

Let $S$ be a linearly independent subset of a vector space $\mathsf{V}$. There exists a maximal linearly independent subset of $\mathsf{V}$ that contains $S$.  

##### Corollary

Every vector space has a basis.

### Selected Exercises

#### 2

Let $A_i$ be the sequence that starts to be 1 at the $i$th position, i.e.
$$
A_1=1,1,1,\dots\\A_2=0,1,1,\dots\\A_3=0,0,1,\dots
$$
Since $A_i\to 1$ for all $i\in N$, each $A_i$ is a convergent sequence, and it is easy to see that $\{A_1,A_2,\dots\}$ are linearly independent.

#### 3

That $\pi$ is transcendental shows the subset $\{1,\pi,\pi^2,\dots\}$ is a linearly independent subset of $\mathsf{V}$.

#### 4

Let $S$ be a basis for $\mathsf{W}$, then it is a linearly independent subset of $\mathsf{V}$, use Theorem 1.13, there exists a maximal linearly independent subset of $\mathsf{V}$ that contains $S$. This maximal linearly independent subset is a basis for $\mathsf{V}$.

#### 5

If $\beta$ is a basis for $\mathsf{V}$, we can finish with the proof of Theorem 1.8 unchanged. Conversely, the condition guarantees $\beta$ can generate $\mathsf{V}$. Assume that $\beta$ is not linearly independent, then one vector $u\in\beta$ can be expressed as
$$
u=a_1u_1+\cdots+a_nu_n
$$
with scalars $a_i$ and $u_i\in\beta$. Also we have $u=u\in\beta$, a contradiction. Thus $\beta$ must be linearly independent.

#### 6

Let $\mathcal{F}$ be the family of all linearly independent subsets of $S_2$ that contains $S_1$, follow the proof of Theorem 1.13, there exists a maximal linearly independent subset $\beta$ of $S_2$ that contains $S_1$. Since $S_2$ generates $\mathsf{V}$, we have $\beta$ generates $\mathsf{V}$, thus is a basis for $\mathsf{V}$.

#### 7

Define $\mathcal{F}$ to be the family of linearly independent sets in the form $\{S\cup B:B\subseteq\beta\}$, then $S\in\mathcal{F}$, for each chain $\mathcal{C}$ in $\mathcal{F}$, take $U$ as the union of all sets in $\mathcal{C}$ makes it a a member of $\mathcal{F}$ that contains each member of $\mathcal{C}$, thus $\mathcal{F}$ has a maximal element, which is in the form $S\cup S_1$ for some set $S_1\subseteq\beta$, this set is linearly independent by the definition of $\mathcal{F}$. We only need to show it generates $\mathsf{V}$.

Assume this set cannot generate $\mathsf{V}$, then there exists $v\in\mathsf{V}$ not in the span of $S\cup S_1$. That $\beta$ is a basis for V means we can find $u_1,\dots,u_n\in\beta$ such that $v=a_1u_1+\cdots+a_nu_n$, this means at least one $u_i$ is not in the span of $S\cup S_1$, thus $S\cup S_1\cup\{u_i\}$ is linearly independent. Since $u_i\in\beta$, we have $S_1\cup\{u_i\}\subseteq\beta$, this contradicts $S\cup S_1$ being the maximal element in $\mathcal{F}$.

### Summary

本节是一个可选章节，初等线性代数一般并不讨论无限维空间的情况，本节试图作了一些拓展，目的是证明所有无限维空间都存在一组基，这个证明不是构造性的，因此无法根据定理显式写出一组基，但存在性的结论也很重要。