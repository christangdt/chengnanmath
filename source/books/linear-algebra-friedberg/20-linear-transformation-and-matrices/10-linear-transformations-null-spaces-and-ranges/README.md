# Linear Transformations, Null spaces and Ranges

### Content Notes

#### Definition (linear transformation)

Let $\mathsf{V}$ and $\mathsf{W}$ be vector spaces (over $F$). We call a function $\mathsf{T}:\mathsf{V}\to\mathsf{W}$ a **linear transformation from $\mathsf{V}$ to $\mathsf{W}$** if, for all $x,y\in\mathsf{V}$ and $c\in F$, we have

(a) $\mathsf{T}(x+y)=\mathsf{T}(x)+\mathsf{T}(y)$ and

(b) $\mathsf{T}(cx)=c\mathsf{T}(x)$.

#### Definition (null space and range)

Let $\mathsf{V}$ and $\mathsf{W}$ be vector spaces, and let $\mathsf{T}:\mathsf{V}\to\mathsf{W}$ be linear. We define the **null space** (or **kernel**) $\mathsf{N(T)}$ of $\mathsf{T}$ to be the set of all vectors $x\in \mathsf{V}$ such that $\mathsf{T}(x)=0$; that is, $\mathsf{N(T)}=\{x\in\mathsf{V}:\mathsf{T}(x)=0\}$.

We define the **range** (or **image**) $\mathsf{R(T)}$ of $\mathsf{T}$ to be the subset of $\mathsf{W}$ consisting of all images (under $\mathsf{T}$) of vectors in $\mathsf{V}$; that is, $\mathsf{R(T)}=\{\mathsf{T}(x):x\in\mathsf{V}\}$.

#### Theorem 2.1

Let $\mathsf{V}$ and $\mathsf{W}$ be vector spaces, and let $\mathsf{T}:\mathsf{V}\to\mathsf{W}$ be linear. Then $\mathsf{N(T)}$ and $\mathsf{R(T)}$ are subspaces of  $\mathsf{V}$ and $\mathsf{W}$ respectively.

#### Theorem 2.2

Let $\mathsf{V}$ and $\mathsf{W}$ be vector spaces, and let $\mathsf{T}:\mathsf{V}\to\mathsf{W}$ be linear. If $\beta=\{v_1,v_2,\dots,v_n\}$ is a basis for $\mathsf{V}$, then
$$
\mathsf{R(T)}=\text{span}(\mathsf{T}(\beta))=\text{span}(\{\mathsf{T}(v_1),\mathsf{T}(v_2),\dots,\mathsf{T}(v_n)\})
$$

#### Definitions (nullity and rank)

Let $\mathsf{V}$ and $\mathsf{W}$ be vector spaces, and let $\mathsf{T}:\mathsf{V}\to\mathsf{W}$ be linear. If $\mathsf{N(T)}$ and $\mathsf{R(T)}$ are finite-dimensional, then we define the **nullity** of $\mathsf{T}$, denote nullity($\mathsf{T}$), and the **rank** of $\mathsf{T}$, denoted rank$(\mathsf{T})$, to be the dimensions of $\mathsf{N(T)}$ and $\mathsf{R(T)}$ respectively.

#### Theorem 2.3 (Dimension Theorem)

Let $\mathsf{V}$ and $\mathsf{W}$ be vector spaces, and let $\mathsf{T}:\mathsf{V}\to\mathsf{W}$ be linear. If $\mathsf{V}$ is finite-dimensional, then
$$
\text{nullity}(\mathsf{T})+\text{rank}(\mathsf{T})=\dim(\mathsf{V})
$$

#### Theorem 2.4

Let $\mathsf{V}$ and $\mathsf{W}$ be vector spaces, and let $\mathsf{T}:\mathsf{V}\to\mathsf{W}$ be linear. Then $\mathsf{T}$ is one-to-one if and only if $\mathsf{N(T)}=\{0\}$.

#### Theorem 2.5

Let $\mathsf{V}$ and $\mathsf{W}$ be vector spaces of equal (finite) dimension, and let $\mathsf{T}:\mathsf{V}\to\mathsf{W}$ be linear. Then the following are equivalent.

(a) $\mathsf{T}$ is one-to-one.

(b) $\mathsf{T}$ is onto.

(c)  $\text{rank}(\mathsf{T})=\dim(\mathsf{V})$.

#### Theorem 2.6

Let $\mathsf{V}$ and $\mathsf{W}$ be vector spaces over $F$, and suppose that $\{v_1,v_2,\dots,v_n\}$ is a basis for $\mathsf{V}$. For $w_1,w_2,\dots,w_n$ in $\mathsf{W}$, there exists exactly one linear transformation $\mathsf{T:V\to W}$ such that $\mathsf{T}(v_i)=w_i$ for $i=1,2,\dots,n$.

##### Corollary

Let $\mathsf{V}$ and $\mathsf{W}$ be vector spaces, and suppose that $\mathsf{V}$ has a finite basis $\{v_1,v_2,\dots,v_n\}$. If $\mathsf{U,T:V\to W}$ are linear and $\mathsf{U}(v_i)=\mathsf{T}(v_i)$ for $i=1,2,\dots,n$, then $\mathsf{U}=\mathsf{T}$.

### Selected Exercises 

#### 3

The nullity is 0, the rank is 2. $\mathsf{T}$ is one-to-one but not onto.

#### 6

The nullity is $n-1$, the rank is 1. $\mathsf{T}$ is not one-to-one but onto.  

#### 10

$\mathsf{T}(0,1)=\mathsf{T}(1,1)-\mathsf{T}(1,0)=(1,1)$, thus
$$
\mathsf{T}(2,3)=2\mathsf{T}(1,0)+3\mathsf{T}(0,1)=2(1,4)+3(1,1)=(5,11)
$$
$\mathsf{T}$ is one-to-one since it is onto.

#### 11

Use Theorem 2.6, there exists one such $\mathsf{T}$, and
$$
\mathsf{T}(8,11)=5\mathsf{T}(1,1)+3\mathsf{T}(2,3)=5(1,0,2)+3(1,-1,4)=(8,-3,22)
$$

#### 13

Let $a_1,\dots,a_k$ be such that $a_1v_1+\cdots+a_kv_k=0$, then
$$
0=\mathsf{T}(a_1v_1+\cdots+a_kw_k)=a_1w_1+\cdots+a_kw_k
$$
thus $a_1=\cdots=a_k=0$.

#### 14

(a) Suppose $\mathsf{T}$ is one-to-one, let $\{v_1,\dots,v_n \}$ be linearly independent subsets of $\mathsf{V}$, then
$$
\begin{aligned}a_1\mathsf{T}(v_1)+\cdots+a_n\mathsf{T}(v_n)=0&\implies\mathsf{T}(a_1v_1+\cdots+a_nv_n)=0
\\&\implies a_1v_1+\cdots+a_nv_n=0
\\&\implies a_1=\cdots=a_n=0
\end{aligned}
$$
Conversely, let $\mathsf{T}(x)=0$ and assume $x\ne 0$, then $\{x\}$ is linearly independent in $\mathsf{V}$ but $\{0\}$ is not linearly independent in $\mathsf{W}$, a contradiction, so we must have $x=0$.

(b) Choose any $v_1,\dots,v_n\in S$, and let $a_1v_1+\cdots+a_nv_n=0$, since $\mathsf{T}(S)$ is linearly independent, we have
$$
a_1\mathsf{T}(v_1)+\cdots+a_n\mathsf{T}(v_n)=0\implies a_1=\cdots=a_n=0
$$
this means $v_1,\dots,v_n$ is linearly independent, and so is $S$.

Conversely, let $S$ be linearly independent, use (a) we can see $\mathsf{T}(S)$ is linearly independent.

(c) Use (b) we can have $\mathsf{T}(\beta)$ linearly independent. To show $\mathsf{T}(\beta)$ spans $\mathsf{W}$, we choose any $w\in\mathsf{W}$, since $\mathsf{T}$ is onto, there is $v\in\mathsf{V}$ such that $\mathsf{T}(v)=w$, $\beta$ is a basis of $\mathsf{V}$ means $v=a_1v_1+\cdots+a_nv_n$, so
$$
w=\mathsf{T}(a_1v_1+\cdots+a_nv_n)=a_1\mathsf{T}(v_1)+\cdots+a_n\mathsf{T}(v_n)
$$

#### 15

Linear: 
$$
\mathsf{T}(cf+g)=\int_0^x(cf+g)(t)dt=c\int_0^xf(t)dt+\int_0^xg(t)dt=c\mathsf{T}(f)+\mathsf{T}(g)
$$
one-to-one:
$$
f(x)\in\mathsf{P(R)}\implies f(x)=a_0+a_1x+\cdots+a_nx^n\\
\begin{aligned}\mathsf{T}(f(x))=\int_0^xf(t)dt=0&\implies a_0x+\frac{a_1}{2}x^2+\cdots+\frac{a_n}{n+1}x^{n+1}=0\\&\implies a_0=a_1=\cdots=a_n=0\\&\implies f(x)=0
\end{aligned}
$$
Not onto: No $f(x)\in\mathsf{P(R)}$ can make $\mathsf{T}(f)=1$.

#### 16

Onto: any $g(x)=a_0+a_1x+\cdots+a_nx^n$, we let
$$
f(x)=a_0x+\frac{a_1}{2}x^2+\cdots+\frac{a_n}{n+1}x^{n+1}
$$
then $\mathsf{T}(f(x))=g(x)$.

Not one-to-one: $\mathsf{T}(1)=0$.

#### 17

Use the Dimension Theorem $\text{nullity}(\mathsf{T})+\text{rank}(\mathsf{T})=\dim(\mathsf{V})$. (a) means $\text{rank}(\mathsf{T})<\dim(\mathsf{W})$. (b) means $\text{nullity}(\mathsf{T})>0$.

#### 18

$\mathsf{T}(a,b)=(b,0)$.

#### 19

$\mathsf{T}(a,b)=(b,0)$. $\mathsf{U}(a,b)=(2b,0)$.

#### 20

Let $w_1,w_2\in\mathsf{T(V_1)}$, then we have $v_1,v_2\in\mathsf{V_1}$ such that $\mathsf{T}(v_1)=w_1,\mathsf{T}(v_2)=w_2$. Then $cw_1+w_2=c\mathsf{T}(v_1)+\mathsf{T}(v_2)=\mathsf{T}(cv_1+v_2)\in\mathsf{T(V_1)}$.

Let $v_1,v_2\in\{x\in\mathsf{V}:\mathsf{T}(x)\in\mathsf{W_1}\}$, then $\mathsf{T}(v_1),\mathsf{T}(v_2)\in\mathsf{W}_1$, thus for $cv_1+v_2$ we have $\mathsf{T}(cv_1+v_2)=c\mathsf{T}(v_1)+\mathsf{T}(v_2)\in\mathsf{W_1}$, so $cv_1+v_2\in\{x\in\mathsf{V}:\mathsf{T}(x)\in\mathsf{W_1}\}$.

#### 22

Let $\mathsf{T}(1,0,0)=a,\mathsf{T}(0,1,0)=b,\mathsf{T}(0,0,1)=c$. Then
$$
\mathsf{T}(x,y,z)=x\mathsf{T}(1,0,0)+y\mathsf{T}(0,1,0)+z\mathsf{T}(0,0,1)=ax+by+cz
$$
An analogous result for $\mathsf{T:F^n\to F^m}$: there exists vectors $u_1,\dots,u_n\in\mathsf{F}^m$ such that $\mathsf{T}(x_1,\dots,x_n)=x_1u_1+\cdots+x_nu_n$.

#### 23

The null space of $\mathsf{T}$ may be the whole space $\mathsf{R}^3$, the $xy-$plane, $yz-$plane, $xz-$plane, a line crossing the origin, or $\{(0,0,0)\}$.

#### 24

(a) $\mathsf{T}(a,b)=(0,b)$. 

(b) $\mathsf{T}(a,b)=(0,b-a)$. 

#### 25

(b)  $\mathsf{T}(a,b,c)=(0,0,c)$. 

(c) For $(a,b,c)\in\mathsf{R}^3$ we have $(a,b,c)=(c,0,c)+(a-c,b,0)$.

#### 26

(a) Let $x,y\in\mathsf{V}$, then $x=x_1+x_2,y=y_1+y_2$ with $x_1,y_1\in\mathsf{W_1}$ and $x_2,y_2\in\mathsf{W}_2$, so $\mathsf{T}(x)=x_1$ and $\mathsf{T}(y)=y_1$, we have $cx+y=(cx_1+y_1)+(cx_2+y_2)$, since $\mathsf{W_1} ,\mathsf{W_2}$ are subspaces, we conclude $\mathsf{T}(cx+y)=cx_1+y_1=c\mathsf{T}(x)+\mathsf{T}(y)$. 

If $x\in\mathsf{W}_1$, then obviously $\mathsf{T}(x)=x$. Conversely, if $x\in\mathsf{V}$ such that $\mathsf{T}(x)=x$, separate $x=x_1+x_2$ with $x_1\in\mathsf{W_1}$ and $x_2\in\mathsf{W}_2$, we see that $x_1=x$ and thus $x_2=0$, this means $x\in\mathsf{W}_1$.

(b) The definition of $\mathsf{T}$ shows $\mathsf{R(T)}\subseteq\mathsf{W_1}$, conversely, for any $x\in\mathsf{W_1}$, the equation $\mathsf{T}(x)=x$ shows $x\in\mathsf{R(T)}$. The definition of $\mathsf{T}$ shows $\mathsf{W_2}\subseteq\mathsf{N(T)}$, conversely, if $x\in\mathsf{N(T)}$, write $x=x_1+x_2$ with $x_1\in\mathsf{W_1}$ and $x_2\in\mathsf{W}_2$, we see that $\mathsf{T}(x)=x_1=0$, which means $x=x_2\in\mathsf{W_2}$.

(c) $\mathsf{T}$ is the identity transformation.

(d) $\mathsf{T}$ is the zero transformation.

#### 27

(a) Let $\dim(\mathsf{V})=n$ and $\dim(\mathsf{W})=k\le n$, choose $v_1,\dots,v_k$ to be a basis for $\mathsf{W}$, extending it to a basis $v_1,\dots,v_n$ of $\mathsf{V}$. Let $\mathsf{W'}$ be the space generated by $\{v_{k+1},\dots,v_n\}$, Define $\mathsf{T:V\to V}$ as
$$
\mathsf{T}(a_1v_1+\cdots+a_nv_n)=a_1v_1+\cdots+a_kv_k
$$
(b) See Exercise 24 with $\mathsf{W}$ being the $y$-axis.

####  28

$\mathsf{T}(0)=0$, $\mathsf{T(V)}\subseteq\mathsf{V}$, $\mathsf{T(R(T))}\subseteq\mathsf{T(V)}\subseteq\mathsf{R(T)}$, and $\mathsf{T(N(T))}=0\subseteq\mathsf{N(T)}$.

#### 29

$\mathsf{T_W}(cx+y)=\mathsf{T}(cx+y)=c\mathsf{T_W}(x)+\mathsf{T_W}(y)$ for $x,y\in\mathsf{W}$.

#### 30

Since $\mathsf{T}(w)=w$ for all $w\in\mathsf{W}$, we see $\mathsf{W}$ is $\mathsf{T}$-invariant, and $\mathsf{T_W}(w)=w$ shows $\mathsf{T_W}=\mathsf{I_W}$.

#### 31

(a) Let $w\in\mathsf{W}$, if $\mathsf{T}(w)=v\ne 0$, then $v\in\mathsf{R(T)}$ and thus $v\notin\mathsf{W}$, a contradiction to $\mathsf{W}$ being $\mathsf{T}$-invariant.

(b) Dimension Theorem shows $\dim(\mathsf{W})=\dim(\mathsf{N(T)})$, then use (a).

(c) In $\mathsf{R}^{\infty}$ let $\mathsf{T}(x_1,x_2,x_3,\dots)=(x_2,x_3,\dots)$, then $\mathsf{R(T)}=\mathsf{R}^{\infty}$ and $\mathsf{W}=\{0\}$, but $\mathsf{N(T)}=\{(a,0,0,\dots):a\in\mathsf{R}\}$.

#### 32

First obviously $\mathsf{N(T)}\cap\mathsf{W}\subseteq\mathsf{N(T_W)}$. Let $v\in\mathsf{N(T_W)}$, we have $v\in\mathsf{W}$ and $0=\mathsf{T_W}(v)=\mathsf{T}(v)$, thus $v\in\mathsf{N(T)}$.

That $\mathsf{R(T_W)}=\{\mathsf{T_W}(x):x\in\mathsf{W}\}=\{\mathsf{T}(x):x\in\mathsf{W}\}\subseteq\mathsf{T(W)}$ is easy to see. Conversely, for $v\in\mathsf{T(W)}$, there is $w\in\mathsf{W}$ such that $\mathsf{T}(w)=v$, but this means $\mathsf{T_W}(w)=v$, so $v\in\mathsf{R(T_W)}$.

#### 33

We have $\mathsf{T}(v)\in\mathsf{R(T)}$ for all $v\in\beta$, thus $\text{span}\{\mathsf{T}(v):v\in\beta\}\subseteq\mathsf{R(T)}$. Conversely, for any $w\in\mathsf{R(T)}$, we have $w=\mathsf{T}(v)$ for some $v\in\mathsf{V}$, then there are $v_1,\dots,v_n\in\beta$ with $v=a_1v_1+\cdots+a_nv_n$, which gives
$$
w=a_1\mathsf{T}(v_1)+\cdots+a_n\mathsf{T}(v_n)\in\text{span}\{\mathsf{T}(v):v\in\beta\}
$$

#### 34

For $v\in\mathsf{V}$, as there are $v_1,\dots,v_n\in\beta$ with $v=a_1v_1+\cdots+a_nv_n$, we define $\mathsf{T:V\to W}$ with
$$
\mathsf{T}(v)=\mathsf{T}(a_1v_1+\cdots+a_nv_n)=a_1f(v_1)+\cdots+a_nf(v_n)
$$
To prove $\mathsf{T}$ is linear, let $x,y\in\mathsf{V}$, then there exists $v_1,\dots,v_n$ and $u_1,\dots,u_m$ in $\beta$, such that $x=a_1v_1+\cdots+a_nv_n$ and $y=b_1u_1+\cdots+b_mu_m$. We have
$$
\begin{aligned}
\mathsf{T}(cx+y)&=\mathsf{T}\left(\sum_{i=1}^nca_iv_i+\sum_{j=1}^mb_ju_j\right)=\sum_{i=1}^nca_if(v_i)+\sum_{j=1}^mb_jf(u_j)
\\&=c\mathsf{T}(x)+\mathsf{T}(y)
\end{aligned}
$$
That $\mathsf{T}(x)=f(x)$ for all $x\in\beta$ is clear from definition.

Suppose $\mathsf{S}$ is a linear transformation such that $\mathsf{S}(x)=f(x)$ for all $x\in\beta$, then for any $v\in V$, we express $v=a_1v_1+\cdots+a_nv_n$, then
$$
\begin{aligned}
\mathsf{T}(v)&=\mathsf{T}(a_1v_1+\cdots+a_nv_n)=a_1f(v_1)+\cdots+a_nf(v_n)
\\&=a_1\mathsf{S}(v_1)+\cdots+a_n\mathsf{S}(v_n)=\mathsf{S}(a_1v_1+\cdots+a_nv_n)
\\&=\mathsf{S}(v)
\end{aligned}
$$
Since $v$ is arbitrary, we have $\mathsf{T}=\mathsf{S}$, so it is unique.

#### 35

(a) We have $\dim(\mathsf{V})=\dim(\mathsf{R(T)})+\dim(\mathsf{N(T)})$, let $\dim(\mathsf{V})=n$ and $\dim(\mathsf{R(T)})=k$. Assume $v\in\mathsf{R(T)}\cap\mathsf{N(T)}$ and $v\ne 0$, then we can extend $v$ to a basis for $\mathsf{R(T)}$ to be $\{v,v_2,\dots,v_k\}$ and a basis for $\mathsf{N(T)}$ to be $\{v,u_2,\dots,u_{n-k}\}$, then we can say the set $\{v,v_2,\dots,v_k,u_2,\dots,u_{n-k}\}$ of $n-1$ vectors generates $\mathsf{V}=\mathsf{R(T)}+\mathsf{N(T)}$, this means $n=\dim(\mathsf{V})\le n-1$, a contradiction. Thus $\mathsf{R(T)}\cap\mathsf{N(T)}=\{0\}$.

(b) We have $\dim(\mathsf{V})=\dim(\mathsf{R(T)})+\dim(\mathsf{N(T)})$, let $\dim(\mathsf{V})=n$ and $\dim(\mathsf{R(T)})=k$. Choose a basis for $\mathsf{R(T)}$ to be $\{v_1,v_2,\dots,v_k\}$ and a basis for $\mathsf{N(T)}$ to be $\{u_1,u_2,\dots,u_{n-k}\}$, use the condition $\mathsf{R(T)}\cap\mathsf{N(T)}=\{0\}$ we can say the set $\{v_1,v_2,\dots,v_k,u_1,u_2,\dots,u_{n-k}\}$ is linearly independent in $\mathsf{V}$,  thus a basis for $\mathsf{V}$. This further means $\mathsf{V}=\mathsf{R(T)}+\mathsf{N(T)}$.

#### 36

(a) For $\mathsf{T}$ is the left shift, we have $\mathsf{V}=\mathsf{R(T)}=\mathsf{R(T)}+\mathsf{N(T)}$, but $\mathsf{R(T)}\cap\mathsf{N(T)}=\{(a,0,\dots,0):a\in\mathsf{R}\}$.

(b) Let $\mathsf{T}_1=\mathsf{U}$ in Exercise 21, i.e. the right shift.

#### 37

Let $x,y=0$, then $\mathsf{T}(0)=\mathsf{T}(0)+\mathsf{T}(0)$ shows $\mathsf{T}(0)=0$. Let $y=-x$, then $\mathsf{T}(0)=\mathsf{T}(x)+\mathsf{T}(-x)$ shows $-\mathsf{T}(x)=\mathsf{T}(-x)$. Use induction we can have $\mathsf{T}(nx)=n\mathsf{T}(x)$ for positive integers $n$, and
$$
\mathsf{T}(nx)=\mathsf{T}(-(-n)x)=-\mathsf{T}(-nx)=-(-n)\mathsf{T}(x)=n\mathsf{T}(x)
$$
for negative integers $n$. Thus $\mathsf{T}(nx)=n\mathsf{T}(x)$ for all integers $n$. Now for any $q\in\mathsf{Q}$, express $q=m/n$, with $m$ integer and $n$ positive integer. Then for $x\in\mathsf{V}$ we have
$$
n\mathsf{T}(qx)=\mathsf{T}(nqx)=\mathsf{T}(mx)=m\mathsf{T}(x)\implies\mathsf{T}(qx)=q\mathsf{T}(x)
$$

#### 38

Let $z_1=a+bi,z_2=c+di$, then
$$
\begin{aligned}\mathsf{T}(z_1+z_2)&=\overline{z_1+z_2}=a+c-(b+d)i=a-bi+c-di\\&=\overline{z_1}+\overline{z_2}=\mathsf{T}(z_1)+\mathsf{T}(z_2)
\end{aligned}
$$
That $\mathsf{T}$ is not linear can be showed by $\mathsf{T}(ii)=-1$ but $i\mathsf{T}(i)=i(-i)=1$.

**<u>Remark: Exercise 37-39 shows condition (b) in the definition of linear transformation is NECESSARY.</u>**

#### 40

(a) That $\eta$ is linear and onto is easy. And 
$$
v\in\mathsf{N}(\eta)\Leftrightarrow\eta(v)=0\Leftrightarrow v+\mathsf{W}=\mathsf{W}\Leftrightarrow v\in\mathsf{W}
$$
(b) $\dim\mathsf{V}=\dim(\mathsf{N(\eta)})+\dim(\mathsf{R(\eta)})=\dim\mathsf{W}+\dim\mathsf{V/W}$.

### Summary

本节介绍线性变换，线性变换是一个连接两个向量空间之间的关系，且满足一个线性的性质：即变换对加法和数乘运算保持不变。由于涉及到两个向量空间，那么就有一些特别需要注意的情况：一是源空间中的一些向量经过线性变换后会消失（vanish，变成0），这部分向量的集合可以证明是一个子空间，称为null space，有的书会称其为kernel；二是目标空间中有一些向量能够被线性变换覆盖到，另外一部分覆盖不到，那些能够被覆盖到的向量的集合可以证明是一个子空间，称为range。由于null space和range都是子空间，就会有维数，并且两个维数相加应等于源空间的维数。在基础的理论建构完毕后，能够证明一些很有意思的结论：例如，从源空间的一组基（含n个向量）一定能够发出一个线性变换指向目标空间的任意n个向量，如果两个线性变换在一组基上相等，那这两个线性变换就相同。本节习题量较多，习题里还有一些有意思的结论。