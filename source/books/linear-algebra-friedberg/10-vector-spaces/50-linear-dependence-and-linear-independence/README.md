# Linear Dependence and Linear Independence

### Content Notes

#### Definition (linearly dependent)

A subset $S$ of a vector space $\mathsf{V}$ is called **linearly dependent** if there exist a finite number of distinct vectors $u_1, u_2, . . . , u_n$ in $S$ and scalars $a_1, a_2, . . . , a_n$, not all zero, such that
$$
a_1u_1 + a_2u_2 + \cdots+ a_nu_n = 0.
$$

In this case we also say that the vectors of $S$ are linearly dependent.  

#### Definition (linearly independent)

A subset $S$ of a vector space that is not linearly dependent is called **linearly independent**. As before, we also say that the vectors of S are linearly independent.

#### Theorem 1.6

Let $\mathsf{V}$ be a vector space, and let $S_1\subseteq S_2\subseteq\mathsf{V}$. If $S_1$ is linearly dependent, then $S_2$ is linearly dependent.

##### Corollary

Let $\mathsf{V}$ be a vector space, and let $S_1\subseteq S_2\subseteq\mathsf{V}$. If $S_2$ is linearly independent, then $S_1$ is linearly independent.

#### Theorem 1.7

Let $S$ be a linearly independent subset of a vector space $\mathsf{V}$, and let $v$ be a vector in $\mathsf{V}$ that is not in $S$. Then $S\cup \{v\}$ is linearly dependent if and only if $v\in\text{span}(S)$.

### Selected Exercises

#### 8

(a) Solve $a_1(1,1,0)+a_2(1,0,1)+a_3(0,1,1)=0$, we have $a_1=a_2=a_3=0$.

(b) That $F$ has characteristic 2 means $1+1=0$, then $(1,1,0)+(1,0,1)=(0,1,1)$.

#### 9

If $u$ and $v$ are linearly dependent, then there exists $a,b$ not all zero such that $au+bv=0$, if $a\ne 0$, then we have $u=(-b/a)v$, if $a=0,b\ne 0$, then we have $v=(-a/b)u$, thus $u$ or $v$ is a multiple of the other. The other direction is easy.

#### 12

$S_1$ is linearly dependent, then there exist a finite number of distinct vectors $u_1, u_2, . . . , u_n$ in $S_1$ and scalars $a_1, a_2, . . . , a_n$, not all zero, such that $a_1u_1+\cdots+a_nu_n=0$. That $S_1\subseteq S_2$ means $u_1, u_2, . . . , u_n$ are in $S_2$, so $S_2$ is linearly dependent by definition.

To prove corollary, assume $S_1$ is linearly dependent, then $S_2$ is linearly dependent by Theorem 1.6, a contradiction, thus $S_1$ must be linearly independent.

#### 13

(a) If $\{u,v\}$ is linearly independent, then $au+bv=0\implies a=b=0$, let $c,d\in F$ such that
$$
c(u+v)+d(u-v)=0\implies(c+d)u+(c-d)v=0
$$
thus $c+d=c-d=0$, which gives $c=d=0$ and so $\{u+v,u-v\}$ is linearly independent. The other direction is similarly proved.

(b) If $\{u,v,w\}$ is linearly independent, then $au+bv+cw=0\implies a=b=c=0$, let $d,e,f\in F$ such that
$$
d(u+v)+e(v+w)+f(u+w)=0\\\implies (d+f)u+(d+e)v+(e+f)w=0\\\implies d+f=d+e=e+f=0\\\implies d+e+f=0
$$
The other direction is similarly proved.

#### 14

One direction is obvious. Suppose $S$ is linearly dependent, then $S=\{0\}$, or there exist a finite number of distinct vectors $u_1, u_2, . . . , u_{n+1}$ in S and scalars $a_1, a_2, . . . , a_{n+1}$, not all zero, such that $a_1u_1+\cdots+a_{n+1}u_{n+1}=0$. Suppose $a_{n+1}$ is not zero, then we can let $v=u_{n+1}$ and get the conclusion.

#### 15

One direction is obvious. Suppose $S$ is linearly dependent, then we check $u_1$ first, if $u_1=0$, then we are done. If not, then we can find scalars $a_1, a_2, . . . , a_n$, not all zero, such that $a_1u_1 + a_2u_2 + \cdots+ a_nu_n = 0$. Let $m$ be the largest integer such that $a_m$ is nonzero, and let $k=m-1$, then we have
$$
a_1u_1 + a_2u_2 + \cdots+ a_mu_m = 0\implies u_m=-\frac{1}{a_m}(a_1u_1+\cdots+a_ku_k)
$$
this means $u_m=u_{k+1}\in\text{span}(\{u_1,\dots,u_k\})$.

#### 16

Let $S$ be a set of vectors linearly independent, then any finite subset $S'$ of $S$ is linearly independent by corollary of Theorem 1.6. Conversely, assume $S$ is a set of vector linearly dependent, then by definition, there exist a finite number of distinct vectors $u_1, u_2,\dots, u_n$ in $S$ and scalars $a_1, a_2, \dots, a_n$, not all zero, such that $a_1u_1 + a_2u_2 + \cdots+ a_nu_n = 0$. This means the finite subset $\{u_1, u_2,\dots, u_n\}$ of $S$ is linearly dependent, a contradiction.

#### 19

Let $a_1, a_2, \dots, a_k$ be scalars such that
$$
a_1A_1^t+a_2A_2^t+\cdots+a_kA_k^t=0
$$
then this means
$$
(a_1A_1+\cdots+a_kA_k)^t=0\implies a_1A_1+\cdots+a_kA_k=0
$$
thus $a_1=\cdots=a_k=0$.

#### 20

Let $a,b\in R$ such that
$$
af(t)+bg(t)=0\implies ae^{rt}+be^{st}=0(t)
$$
this is true for all $t\in R$, let $t=0$ ,we have $a+b=0$ or $b=-a$, thus we get
$$
ae^{rt}+be^{st}=0\implies a(e^{rt}-e^{st})=0 \quad\forall t\in R
$$
since $r\ne s$, we have $e^{rt}-e^{st}\ne 0$, thus $a=0$, which means $b=0$.

### Summary

这一节内容介绍线性无关和线性相关的概念，线性无关可以理解为向量互相之间独立，无法被其他向量“代表”。