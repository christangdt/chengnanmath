# Inner Products and Norms

### Content Notes

#### Definition (inner product)

Let $\mathsf{V}$ be a vector space over $F$. An **inner product** on $\mathsf{V}$ is a function that assigns, to every ordered pair of vectors $x$ and $y$ in $\mathsf{V}$, a scalar in $F$, denoted $\lang{x,y}\rang$, such that for all $x,y,z$ in $\mathsf{V}$ and all $c$ in $F$, the following hold:

(a) $\lang{x+z,y}\rang=\lang{x,y}\rang+\lang{z,y}\rang$.

(b) $\lang{cx,y}\rang=c\lang{x,y}\rang$.

(c) $\overline{\lang{x,y}\rang}=\lang{y,x}\rang$, where the bar denotes complex conjugation.

(d) $\lang{x,x}\rang>0$ if $x\ne0$​.

Note: conditions (a) and (b) require the inner product to be linear in the first component.

#### Example 1 (standard inner product)

For $x=(a_1,a_2,\dots,a_n)$ and $y=(b_1,b_2,\dots,b_n)$ in $\mathsf{F}^n$, define
$$
\lang{x,y}\rang=\sum_{i=1}^na_i\overline{b_i}.
$$

#### Definition (conjugate transpose/adjoint of matrix)

Let $A\in\mathsf{M}_{m\times n}(F)$. We define the **conjugate transpose** or **adjoint** of $A$ to be the $n\times m$ matrix $A^*$ such that $(A^*)_{ij}=\overline{A_{ji}}$ for all $i,j$​.

Using this definition, if $x$ and $y$ are viewed as column vectors in $\mathsf{F}^n$, then $\lang{x,y}\rang=y^*x$​.

#### Example 5 (Frobenius inner product)

Let $\mathsf{V}=\mathsf{M}_{n\times n}(F)$, define $\lang{A,B}\rang=\text{tr}(B^*A)$ for $A,B\in\mathsf{V}$.

#### Definition (Inner product space)

A vector space $\mathsf{V}$ over $F$ endowed with a specific inner product is called an **inner product space**. If $F=C$, we call $\mathsf{V}$ a **complex inner product space**, whereas if $F=R$, we call $\mathsf{V}$ a **real inner product space**.

#### Theorem 6.1

Let $\mathsf{V}$ be an inner product space. Then for $x,y,z\in\mathsf{V}$ and $c\in F$, the following statements are true.

(a) $\lang{x,y+z}\rang=\lang{x,y}\rang+\lang{x,z}\rang$.

(b) $\lang{x,cy}\rang=\overline{c}\lang{x,y}\rang$.

(c) $\lang{x,0}\rang=\lang{0,x}\rang=0$.

(d) $\lang{x,x}\rang=0$ if and only if $x=0$.

(e) If $\lang{x,y}\rang=\lang{x,z}\rang$ for all $x\in\mathsf{V}$, then $y=z$.

Note: (a) and (b) of Theorem 6.1 show the inner product is **conjugate linear** in the second component.

#### Definition (norm/length)

Let $\mathsf{V}$ be an inner product space. For $x\in\mathsf{V}$, we define the **norm** or **length** of $x$ by $\|x\|=\sqrt{\lang{x,x}\rang}$.

#### Theorem 6.2

Let $\mathsf{V}$ be an inner product space over $F$. Then for all $x,y\in\mathsf{V}$ and $c\in F$, the following statements are true.

(a) $\|cx\|=|c|\cdot\|x\|$.

(b) $\|x\|=0$ if and only if $x=0$. In any case, $\|x\|\ge0$.

(c) (Cauchy-Schwarz Inequality) $|\lang{x,y}\rang|\le\|x\|\cdot\|y\|$.

(d) (Triangle Inequality) $\|x+y\|\le\|x\|+\|y\|$.

#### Definition (orthogonal, unit vector, orthonormal)

Let $\mathsf{V}$ be an inner product space. Vectors $x$ and $y$ in $\mathsf{V}$ are **orthogonal (perpendicular)** if $\lang{x,y}\rang=0$. A subset $S$ of $\mathsf{V}$ is **orthogonal** if any two distinct vectors in $S$ are orthogonal. A vector $x$ in $\mathsf{V}$ is a **unit vector** if $\|x\|=1$. Finally, a subset $S$ of $\mathsf{V}$ is **orthonormal** if $S$ is orthogonal and consists entirely of unit vectors.

### Selected Exercises

#### 4

(a) We need to verify (b) and (c) of the definition of inner product. We have
$$
\lang{cA,B}\rang=\text{tr}(B^*(cA))=\text{tr}(cB^*A)=c\text{tr}(B^*A)=c\lang{A,B}\rang
$$
and
$$
\begin{aligned}
\overline{\lang{A,B}\rang}&=\overline{\text{tr}(B^*A)}=\sum_{i=1}^n\overline{(B^*A)_{ii}}=\sum_{i=1}^n\sum_{k=1}^n\overline{(B^*)_{ik}A_{ki}}\\&=\sum_{i=1}^n\sum_{k=1}^n\overline{A_{ki}}B_{ki}
=\sum_{i=1}^n\sum_{k=1}^n(A^*)_{ik}B_{ki}=\sum_{i=1}^n(A^*B)_{ii}\\&=\text{tr}(A^*B)=\lang{B,A}\rang
\end{aligned}
$$

#### 6

Proof of the rest of Theorem 6.1: 

(b) We have
$$
\lang{x,cy}\rang=\overline{\lang{cy,x}\rang}=\overline{c}\overline{\lang{y,x}\rang}=\overline{c}\lang{x,y}\rang.
$$
(c) We have, using (a), that
$$
\lang{x,y}\rang=\lang{x,y+0}\rang=\lang{x,y}\rang+\lang{x,0}\rang\implies\lang{x,0}\rang=0
$$
and $\lang{0,x}\rang=\overline{\lang{x,0}\rang}=\overline{0}=0$.

(d) If $x=0$, use (c) we get $\lang{x,x}\rang=0$, the other direction is from condition (d) of the definition of inner product.

(e) Let $x=y-z$, we have
$$
\lang{x,y}\rang=\lang{x,z}\rang\implies\lang{x,y}\rang-\lang{x,z}\rang=\lang{y-z,y-z\rang}=0\implies y-z=0
$$

#### 7

Proof of the rest of Theorem 6.2: 

(a) We have
$$
\|cx\|^2=\lang{cx,cx}\rang=c\overline{c}\lang{x,x}\rang=|c|^2\|x\|^2
$$
(b) $\|x\|=0$ if and only if $\lang{x,x}\rang=0$, then use Theorem 6.1(d). If $x\ne0$, then $\lang{x,x}\rang>0$ by condition (d) of the definition of inner product.

#### 9

(a) Suppose $\beta=\{z_1,\dots,z_n\}$ and write $x=\sum_ia_iz_i$, then
$$
\lang{x,x}\rang=\sum_{i=1}^na_i\lang{z_i,x\rang}=\sum_{i=1}^na_i\overline{\lang{x,z_i}\rang}=\sum_{i=1}^na_i\overline{0}=0
$$
thus $x=0$.

(b) We have
$$
0=\lang{x,z}\rang-\lang{y,z}\rang=\lang{x-y,z}\rang,\quad\forall z\in\beta
$$
use (a) we see $x-y=0$, thus $x=y$.

#### 10

$x$ and $y$ are orthogonal means $\lang{x,y}\rang=0$, thus
$$
\begin{aligned}
\|x+y\|^2&=\lang{x+y,x+y}\rang
\\&=\lang{x,x+y}\rang+\lang{y,x+y}\rang
\\&=\lang{x,x}\rang+\lang{x,y}\rang+\lang{y,x}\rang+\lang{y,y}\rang
\\&=\|x\|^2+\lang{x,y}\rang+\overline{\lang{x,y}\rang}+\|y\|^2
\\&=\|x\|^2+\|y\|^2
\end{aligned}
$$

#### 11

We have
$$
\|x+y\|^2=\|x\|^2+\lang{x,y}\rang+\overline{\lang{x,y}\rang}+\|y\|^2
\\
\|x-y\|^2=\|x\|^2-\lang{x,y}\rang-\overline{\lang{x,y}\rang}+\|y\|^2
$$
and the conclusion follows.

#### 12

That $\{v_1,\dots,v_k\}$ is an orthogonal set means $\lang{v_i,v_j}\rang=0$ for $i\ne j$. Thus
$$
\begin{aligned}
\left\|\sum_{i=1}^ka_iv_i\right\|^2&=\lang{\sum_{i=1}^ka_iv_i,\sum_{i=1}^ka_iv_i}\rang\\&=\sum_{i=1}^ka_i\lang{v_i,\sum_{j=1}^ka_jv_j}\rang=\sum_{i=1}^ka_i\overline{a_i}\lang{v_i,v_i}\rang
\end{aligned}
$$

#### 13

Verify the four conditions of the definition of inner product. Let $x,y,z\in\mathsf{V}$, then

(a) We have
$$
\begin{aligned}
\lang{x+z,y}\rang&=\lang{x+z,y}\rang_1+\lang{x+z,y}\rang_2
\\&=\lang{x,y}\rang_1+\lang{z,y}\rang_1+\lang{x,y}\rang_2+\lang{z,y}\rang_2
\\&=\lang{x,y}\rang_1+\lang{x,y}\rang_2+\lang{z,y}\rang_1+\lang{z,y}\rang_2
\\&=\lang{x,y}\rang+\lang{z,y}\rang
\end{aligned}
$$
(b) We have
$$
\begin{aligned}
\lang{cx,y}\rang&=\lang{cx,y}\rang_1+\lang{cx,y}\rang_2
=c\lang{x,y}\rang_1+c\lang{x,y}\rang_2
\\&=c(\lang{x,y}\rang_1+\lang{x,y}\rang_2)=c\lang{x,y}\rang
\end{aligned}
$$
(c) We have
$$
\begin{aligned}
\overline{\lang{x,y}\rang}&=\overline{\lang{x,y}\rang_1+\lang{x,y}\rang_2}
=\overline{\lang{x,y}\rang_1}+\overline{\lang{x,y}\rang_2}
\\&=\lang{y,x}\rang_1+\lang{y,x}\rang_2=\lang{y,x}\rang
\end{aligned}
$$
(d) If $x\ne0$, then
$$
\lang{x,x}\rang=\lang{x,x}\rang_1+\lang{x,x}\rang_2>0
$$

#### 14

For $1\le i,j\le n$ we have
$$
\begin{aligned}
(A+cB)^*_{ij}&=\overline{(A+cB)_{ji}}=\overline{A_{ji}+cB_{ji}}=\overline{A_{ji}}+\overline{c}\overline{B_{ji}}
\\&=(A^*)_{ij}+\overline{c}(B^*)_{ij}=(A^*+\overline{c}B^*)_{ij}
\end{aligned}
$$

#### 15

(a) First suppose $x=ay$ or $y=ax$ for some $a\in F$, then in the case $x=ay$ we have
$$
|\lang{x,y}\rang|^2=|a\lang{y,y}\rang|^2=a\overline{a}\lang{y,y}\rang\|y\|^2=\lang{ay,ay}\rang\|y\|^2=\|x\|^2\|y\|^2
$$
thus $|\lang{x,y}\rang|=\|x\|\cdot\|y\|$, the case $y=ax$ can be similarly proved. Conversely, suppose $|\lang{x,y}\rang|=\|x\|\cdot\|y\|$ holds, if $y=0$ then there is nothing to prove (just let $y=0x$), if $y\ne0$, let $a=|\lang{x,y}\rang|/\|y\|^2$ and let $z=x-ay$, then we have
$$
\lang{z,y}\rang=\lang{x-ay,y}\rang=\lang{x,y}\rang-a\lang{y,y}\rang=\lang{x,y}\rang-\lang{x,y}\rang=0
$$
thus $y$ and $z$ are orthogonal. Also we have
$$
|a|=\left|\frac{\lang{x,y}\rang}{\|y\|^2}\right|=\frac{|\lang{x,y}\rang|}{\|y\|^2}=\frac{\|x\|}{\|y\|}
$$
Use Exercise 10, we have
$$
\|x\|^2=\|ay+z\|^2=\|ay\|^2+\|z\|^2=|a|^2\|y\|^2+\|z\|^2=\|x\|^2+\|z\|^2
$$
this means $\|z\|=0$, thus $z=0$ and $x=ay$.

(b) If $\mathsf{V}$ is an inner product space, then $\|x+y\|=\|x\|+\|y\|$ if and only if one of the vectors $x$ or $y$ is a multiple of the other.

#### 16

(a) To verify that $\mathsf{H}$ is an inner product space, we verify the conditions of the definitions of inner product. Let $f,g,h\in\mathsf{H}$, then:

For condition (a), we have
$$
\begin{aligned}
\lang{f+g,h}\rang&=\frac{1}{2\pi}\int_0^{2\pi}[f(t)+g(t)]\overline{h(t)}dt
\\&=\frac{1}{2\pi}\int_0^{2\pi}f(t)\overline{h(t)}dt+\frac{1}{2\pi}\int_0^{2\pi}g(t)\overline{h(t)}dt
\\&=\lang{f,h}\rang+\lang{g,h}\rang
\end{aligned}
$$
For condition (b) we have
$$
\begin{aligned}
\lang{cf,h}\rang&=\frac{1}{2\pi}\int_0^{2\pi}[cf(t)]\overline{h(t)}dt
\\&=c\frac{1}{2\pi}\int_0^{2\pi}f(t)\overline{h(t)}dt
=c\lang{f,h}\rang
\end{aligned}
$$
For condition (c) we have
$$
\begin{aligned}
\overline{\lang{f,g}\rang}&=\overline{\frac{1}{2\pi}\int_0^{2\pi}f(t)\overline{g(t)}dt}=\frac{1}{2\pi}\int_0^{2\pi}\overline{f(t)\overline{g(t)}}dt
\\&=\frac{1}{2\pi}\int_0^{2\pi}\overline{f(t)}g(t)dt=\lang{g,f}\rang
\end{aligned}
$$
For condition (d) we have if $f\ne0$, then $|f|^2$ is bounded away from zero on some subinterval of $[0,2\pi]$, and hence
$$
\lang{f,f}\rang=\frac{1}{2\pi}\int_0^{2\pi}|f(t)|^2dt>0
$$
(b) It is not an inner product on $\mathsf{V}$, consider the function $f\in\mathsf{C}([0,1])$ defined by
$$
f(x)=\begin{cases}
0,&0\le x\le\frac{1}{2}\\
x-\frac{1}{2}&\frac{1}{2}<x\le1
\end{cases}
$$
we see $f\ne0$, but
$$
\lang{f,f}\rang=\int_0^{1/2}f(t)f(t)dt=\int_0^{1/2}0dt=0
$$
thus condition (d) of the definition of inner product is not satisfied.

#### 17

Let $x\in\mathsf{V}$ such that $\mathsf{T}(x)=0_{\mathsf{V}}$, then $0=\|0_{\mathsf{V}}\|=\|\mathsf{T}(x)\|=\|x\|$, so we have $\lang{x,x}\rang=0$, use Theorem 6.1(d) we have $x=0_{\mathsf{V}}$, which means $\mathsf{T}$ is one-to-one.

#### 18

First suppose $\lang{x,y}\rang'$ is an inner product on $\mathsf{V}$. Let $x\in\mathsf{V}$ such that $\mathsf{T}(x)=0_{\mathsf{W}}$, then $\lang{x,x}\rang'=0$, thus $x=0_{\mathsf{V}}$, so $\mathsf{T}$ is one-to-one. Conversely, it is easy to verify that $\lang{x,y}\rang'$ satisfy all conditions of the definition of inner product.

#### 19

(a) We have
$$
\begin{aligned}\|x+y\|^2&=\lang{x+y,x+y}\rang=\|x\|^2+\lang{x,y}\rang+\lang{y,x}\rang+\|y\|^2\\&=\|x\|^2+\lang{x,y}\rang+\overline{\lang{x,y}\rang}+\|y\|^2
\end{aligned}
$$

$$
\begin{aligned}\|x-y\|^2&=\lang{x-y,x-y}\rang=\|x\|^2-\lang{x,y}\rang-\lang{y,x}\rang+\|y\|^2\\&=\|x\|^2-\lang{x,y}\rang-\overline{\lang{x,y}\rang}+\|y\|^2
\end{aligned}
$$

(b) Use (a) and Cauchy-Schwarz inequality we have
$$
\begin{aligned}
\|x-y\|^2&=\|x\|^2+\|y\|^2-2\Re\lang{x,y}\rang\ge\|x\|^2+\|y\|^2-2|\lang{x,y}\rang|
\\&\ge\|x\|^2+\|y\|^2-2\|x\|\cdot\|y\|=(\|x\|-\|y\|)^2
\end{aligned}
$$

#### 20

(a) Use Exercise 19(a) and the fact that $\Re\lang{x,y}\rang=\lang{x,y}\rang$ when $F=R$.

(b) We can easily prove that
$$
\|x+iy\|^2=\|x\|^2+\|y\|^2-i\lang{x,y}\rang+i\lang{y,x}\rang=\|x\|^2+\|y\|^2+2\Im\lang{x,y}\rang
\\
\|x-iy\|^2=\|x\|^2+\|y\|^2-2\Im\lang{x,y}\rang
$$
thus
$$
\begin{aligned}
\sum_{k=1}^4i^k\|x+i^ky\|^2&=i\|x+iy\|^2-\|x-y\|^2-i\|x-iy\|^2+\|x+y\|^2
\\&=i(\|x+iy\|^2-\|x-iy\|^2)+(\|x+y\|^2-\|x-y\|^2)
\\&=4i\Im\lang{x,y}\rang+4\Re\lang{x,y}\rang=4\lang{x,y}\rang
\end{aligned}
$$

#### 21

(a) Use definition of matrix adjoint, we have, for $j,k=1,\dots,n$, that
$$
(A_1^*)_{jk}=\frac{1}{2}(\overline{A}_{kj}+\overline{A^*_{kj}})=\frac{1}{2}(A^*_{jk}+A_{jk})=(A_1)_{jk}
\\
(A_2^*)_{jk}=\overline{\frac{1}{2i}}(\overline{A}_{kj}-\overline{A^*_{kj}})=\frac{i}{2}(A^*_{jk}-A_{jk})=\frac{1}{2i}(A_{jk}-A^*_{jk})=(A_2)_{jk}
$$
and then we have
$$
A_i+iA_2=\frac{1}{2}(A+A^*)+\frac{1}{2}(A-A^*)=A
$$
(b) If $A=B_1+iB_2$, then
$$
\begin{aligned}(A^*)_{jk}&=(\overline{B_1+iB_2})_{kj}=(\overline{B_1})_{kj}-i(\overline{B_2})_{kj}\\&=(B_1)_{jk}-i(B_2)_{jk}=(B_1-iB_2)_{jk}
\end{aligned}
$$
which implies $A^*=B_1-iB_2$, and then it is easy to solve $B_1,B_2$ in terms of $A$ and $A^*$, the expression is the same as $A_1,A_2$ in (a)

#### 22

(a) It is easy to prove $\lang{\cdot,\cdot}\rang$ is an inner product on $\mathsf{V}$. For any $v,v'\in\beta$, we have $v=1v+0v'$ and $v'=0v+1v'$, thus
$$
\lang{v,v'}\rang=1\overline{0}+0\overline{1}=0,\quad \lang{v,v}\rang=1\overline{1}=1
$$
so $\beta$ is an orthonormal basis for $\mathsf{V}$.

#### 23

(a) Let $x=(x_1,\dots,x_n)^t$ and $y=(y_1,\dots,y_n)^t$, write $A=(A_{ij})$, then
$$
\lang{x,Ay}\rang=\sum_{i=1}^nx_i\overline{\sum_{j=1}^nA_{ij}y_j}=\sum_{i=1}^nx_i\sum_{j=1}^n\overline{A_{ij}}\overline{y_j}=\sum_{i=1}^n\sum_{j=1}^nx_i(A^*)_{ji}\overline{y_j}\\=\sum_{j=1}^n\left(\sum_{i=1}^n(A^*)_{ji}x_i\right)\overline{y_j}=\lang{A^*x,y}\rang
$$
(b) Since $\lang{x,Ay}\rang=\lang{A^*x,y}\rang=\lang{Bx,y}\rang$, we have $\lang{A^*x,y}\rang-\lang{Bx,y}\rang=0$ or $\lang{(A^*-B)x,y}\rang=0$ for all $x,y\in\mathsf{V}$, let $y=(A^*-B)x$ we have $\|(A^*-B)x\|=0$ and then $(A^*-B)x=0$ for all $x$, thus $A^*-B=0$ and $B=A^*$.

(c) Write $\beta=\{\beta_1,\dots,\beta_n\}$, where each $\beta_i$ is a column vector, then $Q=(\beta_1,\dots,\beta_n)$, by definition, we have
$$
Q^*=\begin{pmatrix}\overline{\beta_1^t}\\{\vdots}\\{\overline{\beta_n^t}}\end{pmatrix}\\\implies
Q^*Q=\begin{pmatrix}\overline{\beta_1^t}\\{\vdots}\\{\overline{\beta_n^t}}\end{pmatrix}
\begin{pmatrix}\beta_1&\dots&\beta_n\end{pmatrix}=
\begin{pmatrix}\overline{\beta_1^t}\beta_1&\cdots&\overline{\beta_1^t}\beta_n
\\{\vdots}&&\vdots
\\
\overline{\beta_n^t}\beta_1&\cdots&\overline{\beta_n^t}\beta_n
\end{pmatrix}=I_n
$$
then we have $Q^{-1}=Q^*$​ by Exercise 10 of Section 2.4.

(d) We first prove for two $n\times n$ matrices $A$ and $B$, we have $(AB)^*=B^*A^*$, this is true since
$$
(AB)^*_{ij}=\overline{AB_{ji}}=\sum_{k=1}^n\overline{A_{jk}B_{ki}}=\sum_{k=1}^n(B^*)_{ik}(A^*)_{kj}=(B^*A^*)_{ij}
$$
use this relation we further get, for any invertible matrix $A$, that
$$
(AA^{-1})^*=(A^{-1})^*A^*=I\implies(A^*)^{-1}=(A^{-1})^*
$$
then use the matrix representation and notations in (c), we have
$$
[\mathsf{U}]_{\beta}=Q^{-1}[\mathsf{U}]_{\alpha}Q=Q^{-1}A^*Q,\quad [\mathsf{T}]_{\beta}=Q^{-1}[\mathsf{T}]_{\alpha}Q=Q^{-1}AQ
$$
this means
$$
\begin{aligned}
\quad[\mathsf{T}]_{\beta}^*&=(Q^{-1}AQ)^*=Q^*A^*(Q^{-1})^*=Q^{-1}A^*(Q^*)^{-1}\\&=Q^{-1}A^*(Q^{-1})^{-1}=Q^{-1}A^*Q=[\mathsf{U}]_{\beta}
\end{aligned}
$$

#### 28

To show $[\cdot,\cdot]$ is an inner product for $\mathsf{V}$ over $R$, we have for $x,y,z\in\mathsf{V}$ and $c\in R$, that
$$
\begin{aligned}
\quad[x+z,y]&=\Re\lang{x+z,y}\rang =\Re(\lang{x,y}\rang+\lang{z,y}\rang)\\&=\Re\lang{x,y}\rang+\Re\lang{z,y}\rang=[x,y]+[z,y]
\end{aligned}
$$

$$
[cx,y]=\Re\lang{cx,y}\rang=\Re c\lang{x,y}\rang=c\Re\lang{x,y}\rang=c[x,y]
\\
[y,x]=\Re\lang{y,x}\rang=\Re\overline{\lang{x,y}\rang}=\Re\lang{x,y}\rang=[x,y]
$$

notice that $\lang{x,x}\rang\in R$ since $\overline{\lang{x,x}\rang}=\lang{x,x}\rang$, and if $x\ne0$, we have $\lang{x,x}\rang>0$, so $[x,x]=\Re\lang{x,x}\rang=\lang{x,x}\rang>0$, then we finished the proof that $[x,x]$​ is an inner product.

For any $x\in\mathsf{V}$, we have $[x,ix]=\Re\lang{x,ix}\rang=\Re(-i\lang{x,x}\rang)=0$ since $\lang{x,x}\rang\in R$.

#### 29

To show $\lang{\cdot,\cdot}\rang$ is a complex inner product on $\mathsf{V}$, we have, for $x,y,z\in\mathsf{V}$ and $c=a+bi\in C$​, that

Condition (a):
$$
\begin{aligned}
\lang{x+z,y}\rang&=[x+z,y]+i[x+z,iy]\\&=[x,y]+[z,y]+i[x,iy]+i[z,iy]=\lang{x,y}\rang+\lang{z,y}\rang
\end{aligned}
$$
Condition (b): notice that
$$
0=[x+iy,i(x+iy)]=[x+iy,ix-y]=[x,ix]-[x,y]+[iy,ix]-[iy,y]
$$
use the condition again we have $[x,ix]=0$ and $[iy,y]=0$, so $[x,y]=[ix,iy]$, thus
$$
\begin{aligned}
\lang{cx,y}\rang&=[cx,y]+i[cx,iy]=[ax,y]+[ibx,y]+i[ax,iy]+i[ibx,iy]
\\&=a([x,y]+i[x,iy])+b([ix,y]+i[ix,iy])
\\&=a\lang{x,y}\rang+b(i[x,y]+i^2[x,iy])
\\&=a\lang{x,y}\rang+bi\lang{x,y}\rang=(a+bi)\lang{x,y}\rang=c\lang{x,y}\rang
\end{aligned}
$$
Condition (c): 
$$
\lang{y,x}\rang=[y,x]+i[y,ix]=[x,y]+i[iy,-x]=[x,y]-i[x,iy]=\overline{\lang{x,y}\rang}
$$
Condition (d): If $x\ne0$, then
$$
\lang{x,x}\rang=[x,x]+i[x,ix]=[x,x]+0>0
$$

#### 30

Use Exercise 27, we can define an inner product $[\cdot,\cdot]$ on $\mathsf{V}$ over $R$ by
$$
[x,y]=\frac{1}{4}[\|x+y\|^2-\|x-y\|^2]
$$
it is easy to verify that $x-ix=(-i)(x+ix)$, thus
$$
[x,ix]=\frac{1}{4}[\|x+ix\|^2-\|x-ix\|^2]=\frac{1}{4}[\|x+ix\|^2-|-i|\|x+ix\|^2]=0
$$
then use Exercise 29.

### Summary

本章开始介绍内积，是线性代数中非常重要的一个概念。内积是一个从V中向量对到F的函数，满足以下条件：针对自变量对中第一个组成部分的线性性质、调换自变量对顺序的共轭性质、自变量对是同一向量时的正性。另一个重要概念是矩阵的adjoint伴随矩阵，即原矩阵的共轭转置。文中5个例子表明内积的种类并不唯一，装配了某一种内积的向量空间称为内积空间。根据内积指向值域F的不同，又可分为复内积空间和实内积空间。定理6.1是内积函数的性质，其中可以证明内积函数针对自变量对中的第二个组成部分是共轭线性的。模/长度需要通过内积来定义，是向量自内积的平方根。定理6.2是模的一些性质，包括著名的Cauchy-Schwarz不等式和三角不等式。本节最后定义了垂直（内积为0的特殊情况）、单位向量和正交归一向量组。

