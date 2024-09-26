# vector Spaces

### Content Notes

#### Definitions of Vector Space

A vector space (or linear space) $\mathsf{V}$ over a field $F$ consists of a set on which two operations (called addition and scalar multiplication, respectively) are defined so that for each pair of elements $x, y$, in $\mathsf{V}$ there is a unique element $x + y$ in $\mathsf{V}$, and for each element $a$ in $F$ and each element $x$ in $\mathsf{V}$ there is a unique element $ax$ in $\mathsf{V}$, such that the following conditions hold. 

- (VS 1) For all $x, y$ in $\mathsf{V}$, $x + y = y + x$ (commutativity of addition).
- (VS 2) For all $x, y, z$ in $\mathsf{V}$, $(x + y) + z = x + (y + z)$ (associativity of addition).
- (VS 3) There exists an element in $\mathsf{V}$ denoted by $0$ such that $x+ 0 = x$ for each $x$ in $\mathsf{V}$.
- (VS 4) For each element $x$ in $\mathsf{V}$ there exists an element $y$ in $\mathsf{V}$ such that $x + y = 0$.
- (VS 5) For each element $x$ in $\mathsf{V}$, $1x = x$.
- (VS 6) For each pair of elements $a, b$ in $F$ and each element $x$ in $\mathsf{V}$, $(ab)x = a(bx)$.
- (VS 7) For each element $a$ in F and each pair of elements $x, y$ in $\mathsf{V}$, $a(x + y) = ax + ay$.
- (VS 8) For each pair of elements $a, b$ in $F$ and each element $x$ in $\mathsf{V}$, $(a + b)x = ax + bx$.

The elements $x + y$ and $ax$ are called the **sum** of $x$ and $y$ and the **product** of $a$ and $x$, respectively.

#### Examples

The set of all $n$-tuples with entries from a field $F$ is denoted by $\mathsf{F}^n$. This set is a vector space over $F$ with the operations of coordinatewise addition and scalar multiplication.

The set of all $m\times n$ matrices with entries from a field $F$ is a vector space, which we denote by $\mathsf{M}_{m\times n}(F)$.

The set $\mathcal{F}(S,F)$ which is the set of all functions from $S$ to $F$, is a vector space with functional addition and multiplication.

the set of all polynomials with coefficients from $F$ is a vector space, which we denote by $\mathsf{P}(F)$.

all sequences $\{a_n\}$ in $F$ that have only a finite number of nonzero terms $a_n$ is a vector space.

#### Theorem 1.1 (Cancellation Law for Vector Addition)

If $x, y$, and $z$ are vectors in a vector space $\mathsf{V}$ such that $x + z = y + z$, then $x = y$.

##### Corollary 1

The vector $0$ described in (VS 3) is unique.

##### Corollary 2

The vector $y$ described in (VS 4) is unique.

#### Theorem 1.2

In any vector space $\mathsf{V}$, the following statements are true:
(a) $0x = 0$ for each $x\in\mathsf{V}$ .
(b) $(-a)x = -(ax) = a(-x)$ for each $a \in F$ and each $x \in\mathsf{V}$ .
(c) $a0 = 0$ for each $a \in F$.

### Selected Exercises

#### 2

The zero vector of $\mathsf{M}_{3\times4}(F)$ is $\begin{pmatrix}0&0&0\\0&0&0\\0&0&0\\0&0&0\end{pmatrix}$

#### 4

(b) $\begin{pmatrix}1&-1\\3&-5\\3&8\end{pmatrix}$.	(d) $\begin{pmatrix}30&-20\\-15&10\\-5&-40\end{pmatrix}$.	(f) $-x^3+7x^2+4$. 	(h) $3x^5-6x^3+12x+6$.

#### 6

$2M-A$ is the amount of furniture sold in June sale. We have
$$
2M-A=\begin{pmatrix}8&4&2&6\\10&2&2&8\\6&2&4&12\end{pmatrix}-\begin{pmatrix}5&3&1&2\\6&2&1&5\\1&0&3&3\end{pmatrix}=\begin{pmatrix}3&1&1&4\\4&0&1&3\\5&2&1&9\end{pmatrix}
$$
In total, 34 suites were sold during the June sale.

#### 7

We have $f=g$ since
$$
f(0)=2\cdot0+1=1,\quad g(0)=1\\f(1)=2+1=3,\quad g(1)=1+4-2=3
$$
We have $f+g=h$ since
$$
(f+g)(t)=f(t)+g(t)=2+6t-2t^2
\\(f+g)(0)=2=5^0+1=h(0),\quad (f+g)(1)=6=5^1+1=h(1)
$$

#### 8

We have
$$
\begin{aligned}
(a+b)(x+y)&=a(x+y)+b(x+y)\quad(VS7)
\\&=(ax+ay)+(bx+by)\quad(VS8)
\\&=ax+ay+bx+by
\end{aligned}
$$

#### 9

Proof of Corollary 1:
Let $0$ and $0'$ be both zeros in (VS 3), then
$$
0=0+0=0+(0+0')=(0+0)+0'=0+0'=0'
$$
Proof of Corollary 2:

Let $y$ and $y'$ be both negatives in (VS 4), then
$$
y=0+y=(x+y')+y=x+(y'+y)\\=x+(y+y')=(x+y)+y'=0+y'=y'
$$
Proof of Theorem 1.2(c):
$$
a0=a(0+0)=a0+a0\implies a0=0
$$

#### 10

We only need to verify if $f,g$ is differentiable, then $f+g$ and $af$ is differentiable, this is obvious. Also, the additive unit $0(x)=0, \forall x\in R$ is differentiable. Then VS 1- VS 8 are satisfied since the vector space $\mathsf{V}$ we denote is a subspace of $\mathcal{F}(R,R)$.

#### 11

VS 1 and VS 2 are ovbious, since only one element in $\mathsf{V}$. 

$0$ is the additive unit and the additive inverse, thus VS3 and VS 4 holds.

That $10=0$ means VS 5 holds.

For VS 6 to VS 8, we have
$$
(ab)0=0=b0=a(b0)\\a(0+0)=a0=0=a0+a0\\(a+b)0=0=a0+b0
$$

#### 12

Let $f,g$ be even functions, then
$$
(f+g)(-t)=f(-t)+g(-t)=f(t)+g(t)=(f+g)(t)\\(cf)(-t)=cf(-t)=cf(t)=(cf)(t)
$$
the function $0(t)=0$ is even since $0(-t)=0(t)$ for all $t\in R$.

#### 16

Yes. The set of rational numbers is a field.

#### 18

No. For $(0,1)$ and $(1,0)$, both belongs to $\mathsf{V}$, we have
$$
(0,1)+(1,0)=(0+2\times 1,1+3\times 0)=(2,1)
\\
(1,0)+(0,1)=(1+2\times 0,0+3\times 1)=(1,3)
$$
thus VS 1 fails.

#### 19

No. For $a,b\in R$ and $(x,y)\in\mathsf{V}$, we have
$$
(a+b)(x,y)=\left((a+b)x,\frac{y}{a+b}\right),\\ a(x,y)+b(x,y)=\left(ax,\frac{y}{a}\right)+\left(bx,\frac{y}{b}\right)=\left((a+b)x,\frac{(a+b)y}{ab}\right)
$$
thus VS 8 fails.

#### 21

For VS1, we have
$$
(v_1,w_1)+(v_2,w_2)=(v_1+v_2,w_1+w_2)\\=(v_2+v_1,w_2+w_1)=(v_2,w_2)+(v_1,w_1)
$$
the first equality comes from definition, the second use the fact that $\mathsf{V}$ and $\mathsf{W}$ are vector spaces, the third equality comes from definition again. The rest can be similarly proved.

### Summary

这一节主要介绍向量空间，以及空间中的一些常见性质。