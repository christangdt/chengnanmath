# Subspaces

### Content Notes

#### Definition (Subspace)

A subset $\mathsf{W}$ of a vector space $\mathsf{V}$ over a field $F$ is called a subspace of $\mathsf{V}$ if $\mathsf{W}$ is a vector space over $F$ with the operations of addition and scalar multiplication defined on $\mathsf{V}$.

#### Theorem 1.3

Let $\mathsf{V}$ be a vector space and $\mathsf{W}$ a subset of $\mathsf{V}$. Then $\mathsf{W}$ is a subspace of $\mathsf{V}$ if and only if the following three conditions hold for the operations defined in $\mathsf{V}$.
(a) $0 \in\mathsf{W}$.
(b) $x + y \in\mathsf{W}$ whenever $x \in\mathsf{W}$ and $y \in\mathsf{W}$.
(c) $cx \in\mathsf{W}$ whenever $c \in F$ and $x \in\mathsf{W}$.

#### Examples

$\mathsf{P}_n(F)$ is a subspace of $\mathsf{P}(F)$.

$\mathsf{C}(R)$, the set of all continuous real-valued functions defined on $R$, is a subspace of $\mathcal{F}(R,R)$.

The set of diagonal matrices is a subspace of  $\mathsf{M}_{n\times n}(F)$.

The set of $n\times n$ matrices having trace equal to zero is a subspace of $\mathsf{M}_{n\times n}(F)$.

#### Theorem 1.4

Any intersection of subspaces of a vector space $\mathsf{V}$ is a subspace of $\mathsf{V}$. 

### Selected Exercises

#### 17

One direction obvious.

Conversely, $0\in F,x\in\mathsf{W}\implies0\in\mathsf{W}$. The other two conditions are obvious.

#### 18

One direction obvious.

Conversely, $a\in F$ and $x,0\in\mathsf{W}$ means $ax+0=ax\in\mathsf{W}$.

$1\in F$ and $x,y\in\mathsf{W}$ means $1x+y=x+y\in\mathsf{W}$.

#### 19

One direction obvious.

Conversely, suppose $\mathsf{W}=\mathsf{W_1}\cup\mathsf{W_2}$ is a subspace, assume we find $x\in\mathsf{W_1}\backslash\mathsf{W_2}$ and $y\in\mathsf{W_2}\backslash \mathsf{W_1}$, then $x,y\in W$ and so $x+y\in\mathsf{W}$, so we either have $x+y\in\mathsf{W_1}$ or $x+y\in\mathsf{W_2}$.

i) If $x+y\in\mathsf{W_1}$, then $y=(x+y)-x\in\mathsf{W_1}$, contradiction.

ii) If $x+y \in\mathsf{W_2}$, then $x=(x+y)-y\in\mathsf{W_2}$, contradiction.

#### 20

Induction on $n$. When $n=1$, $w_1\in\mathsf{W}\implies a_1w_1\in\mathsf{W}$ for any scalars $a_1$ since $\mathsf{W}$ is a subspace.

Suppose the conclusion is true for $n=k$, then for $n=k+1$, if $w_1,w_2,\dots,w_{k+1}$ are in $W$, then
$$
a_1w_1+\cdots+a_{k+1}w_{k+1}=\underbrace{(a_1w_1+\cdots+a_{k}w_{k})}_{\in W\text{ by induction hypothesis}}+a_{k+1}w_{k+1}\in\mathsf{W}
$$
So the induction is valid.

#### 21

$\mathsf{V}$ is the set of sequences of real numbers. Let $\mathsf{W}$ be the set of convergent sequences of real numbers. We have

$\{0\}=\{0,0,\dots\}\in\mathsf{W}$.

If $\{a_n\},\{b_n\}\in\mathsf{W}$, and $a_n\to a\in R,b_n\to b\in R$, then $a_n+b_n\to a+b$, so $\{a_n\}+\{b_n\}\in\mathsf{W}$. Similarly, for any $c\in R$, we have $ca_n\to ca$ so $c\{a_n\}\in\mathsf{W}$.

#### 22

Let $O$ be the set of all odd functions in $\mathcal{F}(F_1,F_2)$ and $E$ be the set of all even functions in $\mathcal{F}(F_1,F_2)$.

Consider the zero function $z(x)=0\in F_2$ for all $x\in F_1$, then $z$ is both even and odd. So $z\in E,z\in O$.

Let $f,g\in E$, then $(f+g)(-t)=f(-t)+g(-t)=f(t)+g(t)=(f+g)(t)$, thus $f+g\in E$. Similarly, $(af)(-t)=af(-t)=af(t)=(af)(t)$ for $a\in F_2$, thus $af\in E$. We proved $E$ is a subspace of $\mathcal{F}(F_1,F_2)$.

The proof of $O$ being a subspace of $\mathcal{F}(F_1,F_2)$ is similar.

#### 23

(a) $0\in\mathsf{W_1}$ means $\mathsf{W_1}+\mathsf{W_2}$ contains $\mathsf{W_2}$, and $0\in\mathsf{W_2}$ means $\mathsf{W_1}+\mathsf{W_2}$ contains $\mathsf{W_1}$. To show $\mathsf{W_1}+\mathsf{W_2}$ is a subspace, we have

- (i) $0\in\mathsf{W_1},0\in\mathsf{W_2}\implies 0=0+0\in\mathsf{W_1}+\mathsf{W_2}$.

- (ii) $x,y\in\mathsf{W_1}+\mathsf{W_2}$ means $x=x_1+x_2$ for $x_1\in\mathsf{W_1},x_2\in\mathsf{W_2}$ and $y=y_1+y_2$ for $y_1\in W_1,y_2\in W_2$. Thus $x+y=x_1+x_2+y_1+y_2=(x_1+x_2)+(y_1+y_2)\in\mathsf{W_1}+\mathsf{W_2}$.

- (iii) $a\in F$ and $x\in\mathsf{W_1}+\mathsf{W_2}$, means  $x=x_1+x_2$ for $x_1\in\mathsf{W_1},x_2\in\mathsf{W_2}$, since $\mathsf{W_1,W_2}$ are subspaces, we have $ax_1\in\mathsf{W_1},ax_2\in\mathsf{W_2}$, thus $ax=ax_1+ax_2\in\mathsf{W_1}+\mathsf{W_2}$.

(b) Let $\mathsf{W}$ be a subspace of $\mathsf{V}$ that contains $\mathsf{W_1}$ and $\mathsf{W_2}$, let $w$ be arbitrary element in $\mathsf{W_1}+\mathsf{W_2}$, by definition, we can find $x\in\mathsf{W_1},y\in\mathsf{W_2}$ such that $w=x+y$. Since $\mathsf{W}$ contains both $\mathsf{W_1}$ and $\mathsf{W_2}$, we have $x\in\mathsf{W},y\in\mathsf{W}$, which means $w=x+y\in\mathsf{W}$ since $\mathsf{W}$ is a subspace. We proved $\mathsf{W_1}+\mathsf{W_2}\subseteq\mathsf{W}$.

#### 24

First choose any $(x_1,\dots,x_n)\in\mathsf{F}^n$, we have
$$
(x_1,\dots,x_n)=\underbrace{(x_1,\dots,x_{n-1},0)}_{\in W_1}+\underbrace{(0,\dots,0,x_n)}_{\in W_2}
$$
thus $\mathsf{F}^n=\mathsf{W_1}+\mathsf{W_2}$.

Next let $x=(x_1,\dots,x_n)\in\mathsf{W_1}\cap\mathsf{W_2}$, then $x\in\mathsf{W_1}$ means $x_n=0$ and $x\in\mathsf{W_2}$ means $x_1=\cdots=x_{n-1}=0$. Thus $x=0$.

#### 28

skew-symmetric: 反对称矩阵 $M^t=-M$.

Prove $\mathsf{W_1}$ is a subspace of $\mathsf{M}_{n\times n}(F)$:

the zero matrix is skew-symmetric.

If $M_1$ and $M_2$ are skew-symmetric and $a\in F$, then
$$
(M_1+M_2)^t=M_1^t+M_2^t=-M_1-M_2=-(M_1+M_2)\\
(aM_1)^t=a^tM_1^t=a(-M_1)=-(aM_1)
$$
If $F$ is not of characteristic 2, we prove $\mathsf{M}_{n\times n}(F)=\mathsf{W_1}\oplus\mathsf{W_2}$, first $\mathsf{W_1}\cap\mathsf{W_2}=\{0\}$ is easy to see. We only need to prove $\mathsf{M}_{n\times n}(F)=\mathsf{W_1}+\mathsf{W_2}$. Let
$$
A=\begin{pmatrix}a_{11}&\cdots&a_{1n}\\&\cdots&\\a_{n1}&\cdots&a_{nn}\end{pmatrix}\in\mathsf{M}_{n\times n}(F)
$$
Let $B=(b_{ij})\in\mathsf{W_2}$ and $C=(c_{ij})\in\mathsf{W_1}$, which means
$$
B=\begin{pmatrix}b_{11}&\cdots&b_{1n}\\&\cdots&\\b_{1n}&\cdots&b_{nn}\end{pmatrix},\quad C=\begin{pmatrix}0&\cdots&c_{1n}\\&\cdots&\\-c_{1n}&\cdots&0\end{pmatrix}
$$
also for any $i,j\in\{1,\dots,n\}$, each $b_{ij}$ and $c_{ij}$ satisfy
$$
b_{ij}=\dfrac{a_{ij}+a_{ji}}{2},\quad c_{ij}=\dfrac{a_{ij}-a_{ji}}{2},\quad \forall i<j\\b_{ii}=a_{ii},\quad i=1,\dots,n
$$

then we have $A=B+C$.

#### 30

$\Rightarrow$: Let $v\in\mathsf{V}$, suppose we have $v=x_1+x_2$, where $x_1\in\mathsf{W_1}$ and $x_2\in\mathsf{W_2}$, also we have $v=y_1+y_2$, where $y_1\in\mathsf{W_1}$ and $y_2\in\mathsf{W_2}$, this means
$$
x_1+x_2=y_1+y_2\implies w:=x_1-y_1=y_2-x_2\in\mathsf{W_1}\cap\mathsf{W_2}
\\{\implies}x_1-y_1=y_2-x_2=0\implies x_1=y_1,x_2=y_2
$$
$\Leftarrow$: the condition guarantees $\mathsf{V}=\mathsf{W_1}+\mathsf{W_2}$. Let $w\in\mathsf{W_1}\cap\mathsf{W_2}$, then we can write $w=x_1+x_2$ where $x_1\in\mathsf{W_1}$ and $x_2\in\mathsf{W_2}$, we also can write $w = w+0$, where $w\in\mathsf{W_1}$ and $0\in\mathsf{W_2}$, use the uniquely condition, we have $x_2=0$, similarly, write $w=0+w$ gives $x_1=0$, so $w=0$ and $\mathsf{V}=\mathsf{W_1}\oplus\mathsf{W_2}$.

#### 31

**(a)** That $v\in\mathsf{W}$ means $v+\mathsf{W}=\mathsf{W}$, thus is a subspace of $\mathsf{V}$. Conversely, $v+\mathsf{W}$ is a subspace of $\mathsf{V}$ means $0\in v+\mathsf{W}$, so $\exists w\in\mathsf{W}$ such that $0=v+w$, so $v=-w\in\mathsf{W}$.

(b) Suppose $v_1-v_2\in\mathsf{W}$, then $\forall v_1+w\in v_1+\mathsf{W}$, we have $v_1+w=v_2+(v_1-v_2)+w$, which gives $v_1+w\in v_2 +\mathsf{W}$, or $v_1+\mathsf{W}\subset v_2 +\mathsf{W}$, vice versa. So $v_1+\mathsf{W}=v_2+\mathsf{W}$. Conversely, if $v_1+\mathsf{W}=v_2+\mathsf{W}$, then choose any $v_1+w\in v_1+\mathsf{W}$, we can find $w'\in\mathsf{W}$ such that $v_1+w=v_2+w'$, thus $v_1-v_2=w'-w\in\mathsf{W}$.

**(c)** Prove $(v_1+\mathsf{W})+(v_2+\mathsf{W})=(v_1'+\mathsf{W})+(v_2'+\mathsf{W})$ is equivalent to prove $(v_1+v_2)+\mathsf{W}=(v_1'+v_2')+\mathsf{W}$, use (b), this is equivalent to prove $v_1+v_2-(v_1'+v_2')\in\mathsf{W}$. We have
$$
v_1+\mathsf{W}=v_1'+\mathsf{W}\implies v_1-v_1'\in\mathsf{W}\\v_2+\mathsf{W}=v_2'+\mathsf{W}\implies v_2-v_2'\in\mathsf{W}
$$
the two conclusion above gives $(v_1-v_1')+(v_2-v_2')=(v_1+v_2)-(v_1'-v_2')\in\mathsf{W}$. The case of $a(v_1+\mathsf{W})$ is similar.

**(d)** Check conditions VS1-VS8:

VS1, VS2 is guaranteed by $\mathsf{V}$ being a subspace. 

The subspace $\mathsf{W}=0+\mathsf{W}$ act as the additive zero in VS3. 

For any $v+\mathsf{W}\in S$, the element $-v+\mathsf{W}\in S$ is the additive inverse, so VS4 is true.

For any $v+\mathsf{W}\in S$, we have $1(v+\mathsf{W})=1v+\mathsf{W}=v+\mathsf{W}$, so VS5 holds.

For any $v+\mathsf{W}\in S$, we have $(ab)(v+\mathsf{W})=(ab)v+\mathsf{W}=a(bv)+\mathsf{W}=a(bv+\mathsf{W})=a(b(v+\mathsf{W}))$, so VS6 holds.

The check of VS7, VS8 is similar with VS 6 by using definition and properties with $\mathsf{V}$ being a vector space.

### Summary

这一节介绍子空间，子空间的特征是对加法和数乘运算封闭。