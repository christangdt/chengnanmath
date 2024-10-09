# The Riemann-Stieltjes Integral

## 两种积分的引入与符号

本章详细研究所谓“传统”的积分。积分的起源是Riemann积分，用于计算某一曲线下方的面积，利用极限和逼近的思想，以多个宽度极窄的矩形并列以逼近曲线的面积，与我国古代的“割圆术”思想相通。由此产生的积分形如$\int_a^bf(x)dx$，是最简单形式的积分。

本书入手研究的是一种比Riemann积分更广义的积分，即Riemann-Stieltjes积分，形如$\int_a^bf(x)d\alpha(x)$，其与两个函数$f$和$\alpha$都有关，传统Riemann积分是$\alpha(x)=x$时的特例。且当$\alpha$有连续的导数时，该积分可转化为形如$\int_a^bf(x)\alpha'(x)dx$的Riemann积分。但Stieltjes积分能够处理当$\alpha$不连续的情况，能够处理比Riemann积分更为一般的情形。在物理学、概率论等领域应用时能够统一离散和连续的情况，因此更有用。另一种Riemann积分的一般性推广是Lebesgue积分，将在第10章讨论。

本章的讨论会限制在闭区间$[a,b]$上（如这个限制打开，则称为广义积分或者瑕积分）；一般地，所有标为$f,g,\alpha,\beta$等的函数都在闭区间$[a,b]$上定义且有界。$[a,b]$的一个分割被定义为$P=\{x_0,x_1,\dots,x_n\}$且$a=x_0<x_1<\cdots<x_{n-1}<x_n=b$。如果两个分割$P,P'$有关系$P\subseteq P'$，就称$P'$比$P$ "finer"。定义$\Delta\alpha_k=\alpha(x_k)-\alpha(x_{k-1})$，我们有$\sum_{k=1}^n\Delta\alpha_k=\alpha(b)-\alpha(a)$。所有$[a,b]$上可能的分割记为$\mathscr{P}[a,b]$。一个分割$P$的norm指$P$中长度最大的子区间，记为$\|P\|$，因此$P\subseteq P'\implies\|P'\|\le\|P\|$。

## Riemann-Stieltjes积分

### 定义和性质

首先给出Riemann-Stieltjes积分的定义：

#### Definition 7.1

*Let $P=\{x_0,x_1,\dots,x_n\}$ be a partition of $[a,b]$ and let $t_k$ be a point in the subinterval $[x_{k-1},x_k]$. A sum of the form*
$$
S(P,f,\alpha)=\sum_{k=1}^nf(t_k)\Delta\alpha_k
$$
*is called a Riemann-Stieltjes sum of $f$ with respect to $\alpha$. We say $f$ is Riemann-integrable with respect to $\alpha$ on $[a,b]$, and we write "$f\in R(\alpha)$ on $[a,b]$" if there exists a number $A$ having the following property: For every $\varepsilon>0$, there exists a partition $P_{\varepsilon}$ of $[a,b]$ such that for every partition $P$ finer than $P_{\varepsilon}$ and for every choice of the points $t_k$ in $[x_{k-1},x_k]$, we have $|S(P,f,\alpha)-A|<\varepsilon$.*

定义7.1中的数值$A$存在时是唯一的，记为$\int_a^bfd\alpha$或者$\int_a^bf(x)d\alpha(x)$。在$\alpha(x)=x$的特殊情况下，需将$S(P,f,\alpha)$替换为$S(P,f)$，将$f\in R(\alpha)$替换为$f\in R$，此时的积分称为Riemann积分，记为$\int_a^bfdx$或者$\int_a^bf(x)dx$。这个定义是多个Riemann-Stieltjes积分定义中的一个，习题7.3给出了另一个定义。

Riemann-Stieltjes积分对于$f$和$\alpha$都具有线性可加的性质，详见如下两个定理：

#### Theorem 7.2

*If $f\in R(\alpha)$ and if $g\in R(\alpha)$ on $[a,b]$, then $c_1f+c_2g\in R(\alpha)$ on $[a,b]$ and we have*
$$
\int_a^b(c_1f+c_2g)d\alpha=c_1\int_a^bfd\alpha+c_2\int_a^bgd\alpha
$$

#### Theorem 7.3

*If $f\in R(\alpha)$ and $f\in R(\beta)$ on $[a,b]$, then $f\in R(c_1\alpha+c_2\beta)$ on $[a,b]$ and we have*
$$
\int_a^bfd(c_1\alpha+c_2\beta)=c_1\int_a^bfd\alpha+c_2\int_a^bfd\beta.
$$
更进一步地，积分对于所积分的区间也是可加的（线性的）

#### Theorem 7.4

*Assume that $c\in(a,b)$. If two of the three integrals in (1) exist, then the third also exists and we have*
$$
\int_a^cfd\alpha+\int_c^bfd\alpha=\int_a^bfd\alpha\tag{1}
$$
基于定理7.4的结论，可以定义颠倒积分区间的积分

#### Definition 7.5

*If $a<b$, we define $\int_a^bfd\alpha=-\int_a^bfd\alpha$ whenever $\int_a^bfd\alpha$ exists. We also define $\int_a^bfd\alpha=0$.*

### 分部积分和换元积分

分部积分的定理说明了被积函数和积分元之间有非常密切的联系。

#### Theorem 7.6

*If $f\in R(\alpha)$ on $[a,b]$, then $\alpha\in R(f)$ on $[a,b]$ and we have*
$$
\int_a^bf(x)d\alpha(x)+\int_a^b\alpha(x)df(x)=f(b)\alpha(b)-f(a)\alpha(a).
$$

#### Theorem 7.7

*Let $f\in R(\alpha)$ on $[a,b]$ and let $g$ be a strictly monotonic continuous function defined on an interval $S$ having endpoints $c$ and $d$. Assume $a=g(c),b=g(d)$. Let $h$ and $\beta$ be the composite functions defined as follows:*
$$
h(x)=f[g(x)],\quad\beta(x)=\alpha[g(x)],\quad\text{if }x\in S.
$$
*Then $h\in R(\beta)$ on $S$ and we have $\int_a^bfd\alpha=\int_c^dhd\beta$. That is,*
$$
\int_{g(c)}^{g(d)}f(t)d\alpha(t)=\int_c^df[g(x)]d\{\alpha[g(x)]\}.
$$

### 退化成Riemann积分的情形

如果$\alpha$具有连续的导函数$\alpha'$，那么Riemann-Stieltjes积分能够使用Riemann积分的方式表示。

#### Theorem 7.8

*Assume $f\in R(\alpha)$ on $[a,b]$ and assume that $\alpha$ has a continuous derivative $\alpha'$ on $[a,b]$. then the Riemann integral $\int_a^bf(x)\alpha'(x)dx$ exists and we have*
$$
\int_a^bf(x)d\alpha(x)=\int_a^bf(x)\alpha'(x)dx
$$
在后面的定理中还可以进一步放松$\alpha$的条件。

### 阶梯函数积分元

阶梯函数作为积分元，本质是$\alpha$存在跳跃间断点的情况，此时积分$\int_a^bfd\alpha$不一定存在，如果存在，其值也与$\alpha$的跳跃幅度有关。

#### Theorem 7.9

*Given $a<c<b$. Define $\alpha$ on $[a,b]$ as follows: The values $\alpha(a),\alpha(b),\alpha(c)$ are arbitrary; $\alpha(x)=\alpha(a)$ if $a\le x<c$, and $\alpha(x)=\alpha(b)$ if $c<x\le b$. Let $f$ be defined on $[a,b]$ in such a way that at least one of the functions $f$ or $\alpha$ is continuous from the left at $c$ and at least one of the functions $f$ or $\alpha$ is continuous from the right at $c$. Then $f\in R(\alpha)$ on $[a,b]$ and we have*
$$
\int_a^bfd\alpha=f(c)[\alpha(c+)-\alpha(c-)]
$$
这个定理说明，函数$f$在某一点的值变化就可影响Riemann-Stieltjes积分的值，事实上，函数$f$在某一点的值变化可以影响Riemann-Stieltjes积分是否存在。

### 退化成有限和的情形

定理7.9中的$\alpha$是一种称为阶梯函数的函数类别，其能够将Riemann-Stieltjes积分与有限级数和联系起来。

#### Definition 7.10 (Step function)

*A function a defined on $[a,b]$ is called a step function if there is a partition $a=x_1<x_2\cdots<x_n=b$ such that $\alpha$ is constant on each open subinterval $(x_{k-1},x_k)$. The number $\alpha(x_k+)-\alpha(x_k-)$ is called the jump at $x_k$ if $1<k<n$. The jump at $x_1$ is $\alpha(x_1+)-\alpha(x_1)$ and the jump at $x_n$ is $\alpha(x_n)-\alpha(x_n-)$.*

#### Theorem 7.11 (Reduction of a Riemann-Stieltjes integral to a finite sum)

*Let $\alpha$ be a step function defined on $[a,b]$ with jump $\alpha_k$ at $x_k$, where $x_1,\dots,x_n$ are described in Definition 7.10. Let $f$ be defined on $[a,b]$ in such a way that not both $f$ and $\alpha$ are discontinuous from the right or from the left at each $x_k$. Then $\int_a^bfd\alpha$ exists and we have*
$$
\int_a^bf(x)d\alpha(x)=\sum_{k=1}^nf(x_k)\alpha_k.
$$

#### Theorem 7.12

*Every finite sum can be written as a Riemann-Stieltjes integral. In fact, given a sum $\sum_{k=1}^na_k$, define $f$ on $[0,n]$ as follows:*
$$
f(x)=a_k\quad\text{if }k-1<{x}\le k\quad(k=1,2,\dots,n),\quad f(0)=0.
$$
*Then*
$$
\sum_{k=1}^na_k=\sum_{k=1}^nf(k)=\int_0^nf(x)d[x].
$$
*where $[x]$ is the greatest integer $\le x$.*

### 欧拉求和公式

#### Theorem 7.13 (Euler's summation formula)

*If $f$ has a continuous derivative $f'$ on $[a,b]$, then we have*
$$
\sum_{a<n\le b}f(n)=\int_a^bf(x)dx+\int_a^bf'(x)\big((x)\big)dx+f(a)\big((a)\big)-f(b)\big((b)\big)
$$
*where $\big((x)\big)=x-[x]$. When $a$ and $b$ are integers, this becomes*
$$
\sum_{n=a}^bf(n)=\int_a^bf(x)dx+\int_a^bf'(x)\left(x-[x]-\dfrac{1}{2}\right)dx+\dfrac{f(a)+f(b)}{2}.
$$
NOTE: $\sum_{a<n\le b}$ means the sum from $n=[a]+1$ to $n=[b]$.

## 积分元单调上升的Riemann-Stieltjes积分

从此处开始，后续讨论的都是积分元$\alpha$为单调上升（记号为$\alpha\nearrow$ on $[a,b]$）的Riemann-Stieltjes积分，引入上积分和下积分的概念，并将可积性与上下积分联系起来。相对于之前的定义，这样的处理更好理解也更常见。

### 上积分与下积分

#### Definition 7.14

*Let $P$ be a partition of $[a,b]$ and let*
$$
M_k(f)=\sup\{f(x):x\in[x_{k-1},x_k]\},
\\
m_k(f)=\inf\{f(x):x\in[x_{k-1},x_k]\}.
$$
*The numbers*
$$
U(P,f,\alpha)=\sum_{k=1}^nM_k(f)\Delta\alpha_k\quad\text{and}\quad L(P,f,\alpha)=\sum_{k=1}^nm_k(f)\Delta\alpha_k
$$
*are called, respectively, the upper and lower Stieltjes sums of $f$ with respect to $\alpha$ for*
*the partition $P$.*  

#### Theorem 7.15

*Assume that $\alpha\nearrow$ on $[a,b]$. Then:*

*i) If $P'$ is finer than $P$, we have $U(P',f,\alpha)\le U(P,f,\alpha)$ and $L(P',f,\alpha)\ge L(P,f,\alpha)$.*

*ii) For any two partitions $P_1$ and $P_2$ we have $L(P_1,f,\alpha)\le U(P_2,f,\alpha)$.*

定理7.15说明如果分割$P$更细了，那么下和会增加，上和会减少，但任一下和始终不超过任一上和。

#### Definition 7.16

*Assume that $\alpha\nearrow$ on $[a,b]$. The upper Stieltjes integral of $f$ with respect to $\alpha$ is defined as follows and denoted $\bar{I}(f,\alpha)$:*
$$
\bar{\int}_a^bfd\alpha=\inf\{U(P,f,\alpha):P\in\mathscr{P}[a,b]\}.
$$
*The lower Stieltjes integral is similarly defined and denoted $\underline{I}(f,\alpha)$:*
$$
\underline{\int}_a^bfd\alpha=\sup\{L(P,f,\alpha):P\in\mathscr{P}[a,b]\}.
$$

#### Theorem 7.17

*Assume that $\alpha\nearrow$ on $[a,b]$. Then $\underline{I}(f,\alpha)\le\bar{I}(f,\alpha)$.*

### 黎曼条件

#### Definition 7.18

*We say that $f$ satisfies Riemann's condition with respect to $\alpha$ on $[a,b]$ if, for every $\varepsilon>0$, there exists a partition $P_{\varepsilon}$ such that $P$ finer than $P_{\varepsilon}$ implies $0\le U(P,f,\alpha)-L(P,f,\alpha)<\varepsilon$.*

#### Theorem 7.19

*Assume that $\alpha\nearrow$ on $[a,b]$. Then the following three statements are equivalent:*

*i) $f\in R(\alpha)$ on $[a,b]$.*

*ii) $f$ satisfies Riemann's condition with respect to $\alpha$ on $[a,b]$.*

*iii)  $\underline{I}(f,\alpha)=\bar{I}(f,\alpha)$.*

### 比较定理和衍生可积函数

#### Theorem 7.20

*Assume that $\alpha\nearrow$ on $[a,b]$. If $f\in R(\alpha)$ and $g\in R(\alpha)$ on $[a,b]$ and if $f(x)\le g(x)$ for all $x$ in $[a,b]$, then we have*
$$
\int_a^bf(x)d\alpha(x)\le\int_a^bg(x)d\alpha(x).
$$

#### Theorem 7.21

*Assume that $\alpha\nearrow$ on $[a,b]$. If $f\in R(\alpha)$ on $[a,b]$, then $|f|\in R(\alpha)$ on $[a,b]$ and we have the inequality*
$$
\left|\int_a^bf(x)d\alpha(x)\right|\le\int_a^b|f(x)|d\alpha(x).
$$

#### Theorem 7.22

*Assume that $\alpha\nearrow$ on $[a,b]$. If $f\in R(\alpha)$ on $[a,b]$, then $f^2\in R(\alpha)$ on $[a,b]$.*

#### Theorem 7.23

*Assume that $\alpha\nearrow$ on $[a,b]$. If $f\in R(\alpha)$ and $g\in R(\alpha)$ on $[a,b]$, then the product $f\cdot g\in R(\alpha)$ on $[a,b]$.* 

### 有界变差积分元

有界变差函数$\alpha$总能够表示为两个单增函数的差，即$\alpha=\alpha_1-\alpha_2$。如果$f\in R(\alpha_1)$以及$f\in R(\alpha_2)$，那么根据定理7.3积分的线性性质，$f\in R(\alpha)$。但反之是不一定成立的，可以证明的是对于有界变差函数$\alpha$的一种特定的分解，能够有反之的成立。

#### Theorem 7.24

*Assume that $\alpha$ is of bounded variation on $[a,b]$. Let $V(x)$ denote the total variation of $\alpha$ on $[a,x]$ if $a<x\le b$, and let $V(a)=0$. Let $f$ be defined and bounded on $[a,b]$. If $f\in R(\alpha)$ on $[a,b]$, then $f\in R(V)$ on $[a,b]$.*

这个定理的有用之处在于其能将有界变差函数作为积分元的积分转为积分元单调上升的积分情况，因此可以应用黎曼条件。例如下面的两个应用：

#### Theorem 7.25

*Let $\alpha$ be of bounded variation on $[a,b]$ and assume that $f\in R(\alpha)$ on $[a,b]$. Then $f\in R(\alpha)$ on every subinterval $[c,d]$ of $[a,b]$.*

#### Theorem 7.26

*Assume $f\in R(\alpha)$ and $g\in R(\alpha)$ on $[a,b]$, where $\alpha\nearrow$ on $[a,b]$. Define*
$$
F(x)=\int_a^xf(t)d\alpha(t)
$$
*and*
$$
G(x)=\int_a^xg(t)d\alpha(t)\quad\text{ if }x\in[a,b].
$$
*Then $f\in R(G),g\in R(F)$, and the product $f\cdot g\in R(\alpha)$ on $[a,b]$, and we have*
$$
\int_a^bf(x)g(x)d\alpha(x)=\int_a^bf(x)dG(x)=\int_a^bg(x)dF(x).
$$

## Riemann-Stieltjes积分存在的充要条件

### 充分条件

之前的多数定理都假设特定积分存在，再研究它们的性质。但积分存在是否有充分条件？有两个定理可以判断积分的存在性：

#### Theorem 7.27

*If $f$ is continuous on $[a,b]$ and if $\alpha$ is of bounded variation on $[a,b]$, then $f\in R(\alpha)$ on $[a,b]$.*

#### Theorem 7.28

*Each of the following conditions is sufficient for the existence of the Riemann integral $\int_a^bf(x)dx$:*

*(a) $f$ is continuous on $[a,b]$.*

*(b) $f$ is of bounded variation on $[a,b]$.*

### 必要条件

若要使得积分存在，对于$f$连续的条件可以进一步放松，只要保证在特定的点连续，其他点可以不连续。

#### Theorem 7.29

*Assume that $\alpha\nearrow$ on $[a,b]$ and let $a<c<b$. Assume further that both $\alpha$ and $f$ are discontinuous from the right at $x=c$; that is, assume that there exists an $\varepsilon>0$ such that for every $\delta>0$ there are values of $x,y$ in the interval $(c,c+\delta)$ for which*
$$
|f(x)-f(c)|\ge\varepsilon\quad\text{and}\quad|\alpha(y)-\alpha(c)|\ge\varepsilon
$$
*Then the integral $\int_a^bf(x)d\alpha(x)$ cannot exist. The integral also fails to exist if $\alpha$ and $f$ are discontinuous from the left at $c$.*

## 积分中值定理

能够显式计算出积分精确值的情况并不多，也很难。大部分时候对积分有一个相对精确的估计就很好，此时积分中值定理就能派上用场。

### 基本形态：第一和第二中值定理

#### Theorem 7.30 (First Mean-Value Theorem for Riemann-Stieltjes integrals)

*Assume that $\alpha\nearrow$ on $[a,b]$ and let $f\in R(\alpha)$ on $[a,b]$. Let $M$ and $m$ denote, respectively, the $\sup$ and $\inf$ of the set $\{f(x):x\in[a,b]\}$. Then there exists a real number $c$ satisfying $m\le c\le M$ such that*
$$
\int_a^bf(x)d\alpha(x)=c\int_a^bd\alpha(x)=c[\alpha(b)-\alpha(a)].
$$
*In particular, if $f$ is continuous on $[a,b]$, then $c=f(x_0)$ for some $x_0\in[a,b]$.*

#### Theorem 7.31 (Second Mean-Value Theorem for Riemann-Stieltjes integrals)

*Assume that $\alpha$ is continuous and that $f\nearrow$ on $[a,b]$. Then there exists a point $x_0\in[a,b]$ such that*
$$
\int_a^bf(x)d\alpha(x)=f(a)\int_a^{x_0}d\alpha(x)+f(b)\int_{x_0}^bd\alpha(x).
$$

### 将积分视作区间的函数

当积分元是有界变差函数时，定理7.25保证了$\int_a^xfd\alpha$在$x\in[a,b]$时均存在，因此可视作$x$的函数。据此能得到一些性质：

#### Theorem 7.32

*Let $\alpha$ be of bounded variation on $[a,b]$ and assume that $f\in R(\alpha)$ on $[a,b]$. Define $F$ by the equation*
$$
F(x)=\int_a^xfd\alpha,\quad\text{if }x\in[a,b].
$$
*Then we have*

*i) $F$ is of bounded variation on $[a,b]$.*

*ii) Every point of continuity of $\alpha$ is also a point of continuity of $F$.*

*iii) If $\alpha\nearrow$ on $[a,b]$, the derivative $F'(x)$ exists at each point $x$ in $(a,b)$ where $\alpha'(x)$ exists and where $f$ is continuous. For such $x$, we have $F'(x)=f(x)\alpha'(x)$.*

NOTE: When $\alpha(x)=x$, part (iii) of Theorem 7.32 is sometimes called the *first fundamental theorem of integral calculus*. It states that $F'(x)=f(x)$ at each point of continuity of $f$.

#### Theorem 7.33

*If $f\in R$ and $g\in R$ on $[a,b]$, let*
$$
F(x)=\int_a^xf(t)dt,\quad G(x)=\int_a^xg(t)dt\quad\text{if }x\in[a,b].
$$
*Then $F$ and $G$ are continuous functions of bounded variation on $[a,b]$. Also, $f\in R(G)$ and $g\in R(F)$ on $[a,b]$ and we have*
$$
\int_a^bf(x)g(x)dx=\int_a^bf(x)dG(x)=\int_a^bg(x)dF(x).
$$

#### Theorem 7.34 (Second fundamental theorem of integral calculus)

*Assume that $f\in R$ on $[a,b]$. Let $g$ be the function defined on $[a,b]$ such that the derivative $g'$ exists in $(a,b)$ and has the value $g'(x)=f(x)$ for every $x\in(a,b)$. At the endpoints assume that $g(a+)$ and $g(b-)$ exist and satisfy $g(a)-g(a+)=g(b)-g(b-)$. Then we have*
$$
\int_a^bf(x)dx=\int_a^bg'(x)dx=g(b)-g(a).
$$
将定理7.34和定理7.33结合，能够得到下列定理7.8的强化形式：

#### Theorem 7.35

*Assume that $f\in R$ on $[a,b]$. Let $\alpha$ be a function which is continuous on $[a,b]$ and whose derivative $\alpha'$ is Riemann integrable on $[a,b]$. Then the following integrals exist and are equal:*
$$
\int_a^bf(x)d\alpha(x)=\int_a^bf(x)\alpha'(x)dx.
$$

### Riemann积分的换元法

定理7.7是Riemann-Stieltjes积分的换元，可以同样适用于Riemann积分，如果其中$f$是连续的，那么就不需要$g$单调的条件。

#### Theorem 7.36 (Change of variable in Riemann integral)

*Assume that $g$ has a continuous derivative $g'$ on an interval $[c,d]$. Let $f$ be continuous on $g([c,d])$ and define $F$ by the equation*
$$
F(x)=\int_{g(c)}^xf(t)dt\qquad\text{if }x\in g([c,d]).
$$
 *Then for each $x\in[c,d]$, the integral $\int_c^xf[g(t)]g'(t)dt$ exists and has the value $F[g(x)]$. In particular, we have*
$$
\int_{g(c)}^{g(d)}f(x)dx=\int_c^df[g(t)]g'(t)dt.
$$

#### Theorem 7.37 (Second Mean-Value Theorem for Riemann integrals)

*Let $g$ be continuous and assume that $f\nearrow$ on $[a,b]$. Let $A$ and $B$ be two real numbers satisfying the inequalities $A\le f(a+)$ and $B\ge f(b-)$. Then there exists a point $x_0\in[a,b]$ such that*
$$
\int_a^bf(x)g(x)dx=A\int_a^{x_0}g(x)dx+B\int_{x_0}^bg(x)dx.\tag{i}
$$
*In particular, if $f(x)\ge0$ for all $x\in[a,b]$, we have*
$$
\int_a^bf(x)g(x)dx=B\int_{x_0}^bg(x)dx,\quad x_0\in[a,b]\tag{ii}
$$
NOTE. Part (ii) is known as *Bonnet's theorem*.

## 初涉二维积分

### 含一个变元的Riemann-Stieltjes积分

#### Theorem 7.38

*Let $f$ be continuous at each point $(x,y)$ of a rectangle $Q=\{(x,y):a\le{x}\le b,c\le y\le d\}$. Assume that $\alpha$ is of bounded variation on $[a,b]$ and let $F$ be the function defined on $[c,d]$ by the equation*
$$
F(y)=\int_a^bf(x,y)d\alpha(x).
$$
*Then $F$ is continuous on $[c,d]$. In other words, if $y_0\in[c,d]$, we have*
$$
\lim_{y\to y_0}\int_a^bf(x,y)d\alpha(x)=\int_a^b\lim_{y\to y_0}f(x,y)d\alpha(x)=\int_a^bf(x,y_0)d\alpha(x).
$$

#### Theorem 7.39

*If $f$ is continuous on the rectangle $[a,b]\times[c,d]$, and if $g\in R$ on $[a,b]$, then the function $F$ defined by the equation*
$$
F(y)=\int_a^bg(x)f(x,y)dx
$$
*is continuous on $[c,d]$. That is, if $y_0\in[c,d]$, we have*
$$
\lim_{y\to y_0}\int_a^bg(x)f(x,y)dx=\int_a^bg(x)f(x,y_0)dx.
$$

### 对积分求导

#### Theorem 7.40

*Let $Q=\{(x,y):a\le{x}\le b,c\le y\le d\}$. Assume that $\alpha$ is of bounded variation on $[a,b]$ and, for each fixed $y\in[c,d]$, assume that the integral*
$$
F(y)=\int_a^bf(x,y)d\alpha(x)
$$
*exists. If the partial derivative $D_2f$ is continuous on $Q$, the derivative $F'(y)$ exists for each $y\in[c,d]$ and is given by*
$$
F'(y)=\int_a^bD_2f(x,y)d\alpha(x).
$$

### 积分换序

#### Theorem 7.41

*Let $Q=\{(x,y):a\le{x}\le b,c\le y\le d\}$. Assume that $\alpha$ is of bounded variation on $[a,b]$, $\beta$ is of bounded variation on $[c,d]$, and $f$ is continuous on $Q$. If $(x,y)\in Q$, define*
$$
F(y)=\int_a^bf(x,y)d\alpha(x),\quad G(x)=\int_c^df(x,y)d\beta(y).
$$
*Then $F\in R(\beta)$ on $[c,d]$, $G\in R(\alpha)$ on $[a,b]$, and we have*
$$
\int_c^dF(y)d\beta(y)=\int_a^bG(x)d\alpha(x)
$$
*In other words, we may interchange the order of in as follows:*
$$
\int_a^b\left[\int_c^df(x,y)d\beta(y)\right]d\alpha(x)=\int_c^d\left[\int_a^bf(x,y)d\alpha(x)\right]d\beta(y)
$$

#### Theorem 7.42

*Let $f$ be continuous on the rectangle $[a,b]\times[c,d]$. If $g\in R$ on $[a,b]$ and if $h\in R$ on $[c,d]$, then we have*
$$
\int_a^b\left[\int_c^dg(x)h(y)f(x,y)dy\right]dx=\int_c^d\left[\int_a^bg(x)h(y)f(x,y)dx\right]dy.
$$

## Riemann积分存在的Lebesgue条件

Lebesgue条件是对Riemann积分的进一步松绑，Riemann和的上和与下和之差的典型形式是$\sum_{k=1}^n[M_k(f)-m_k(f)]\Delta x_k$，Riemann可积意味着这个和趋于0。这个和可以分为两部分：一部分是连续所导致的$M_k(f)-m_k(f)$很小，另一部分是可以不连续（$M_k(f)-m_k(f)$无法任意小）但是不连续区间的总长度是很小的，从而仍然可积。这些是Lebesgue定理的核心思想。

### 零测度

#### Definition 7.43

*A set $S$ of real numbers is said to have measure zero if, for every $\varepsilon>0$, there is a countable covering of $S$ by open intervals, the sum of whose lengths is less than $\varepsilon$.*

#### Theorem 7.44

*Let $F$ be a countable collection of sets in $\mathbf{R}$, say $F=\{F_1,F_2,\dots\}$, each of which has measure zero. Then their union $S=\bigcup_{k=1}^{\infty}F_k$ also has a measure zero.*

### 震荡

#### Definition 7.45

*Let $f$ be defined and bounded on an interval $S$. If $T\subseteq S$, the number*
$$
\Omega_f(T)=\sup\{f(x)-f(y):x\in T,y\in T\},
$$
*is called the oscillation of $f$ on $T$. The oscillation of $f$ at $x$ is defined to be the number*
$$
\omega_f(x)=\lim_{h\to 0+}\Omega_f(B(x;h)\cap S).
$$

#### Theorem 7.46

*Let $f$ be defined and bounded on $[a,b]$ and let $\varepsilon>0$ be given. Assume that $\omega_f(x)<\varepsilon$ for every $x\in[a,b]$. Then there exists a $\delta>0$ such that for every closed subinterval $T\subseteq[a,b]$, we have $\Omega_f(T)<\varepsilon$ whenever the length of $T$ is less than $\delta$.*

#### Theorem 7.47

*Let $f$ be defined and bounded on $[a,b]$. For each $\varepsilon>0$ define the set $J_{\varepsilon}$ as follows:*
$$
J_{\varepsilon}=\{x:x\in[a,b],\quad\omega_f(x)\ge\varepsilon\}.
$$
*Then $J_{\varepsilon}$ is a closed set.*

### Lebesgue条件

#### Theorem 7.48 (Lebesgue's criterion for Riemann-integrability)

*Let $f$ be defined and bounded on $[a,b]$ and let $D$ denote the set of discontinuities of $f$ in $[a,b]$. Then $f\in R$ on $[a,b]$ if and only if $D$ has measure zero.*

#### Theorem 7.49

a) *If $f$ is of bounded variation on $[a,b]$, then $f\in R$ on $[a,b]$.*

b) *If $f\in R$ on $[a,b]$, then $f\in R$ on $[c,d]$ for every subinterval $[c,d]\subset[a,b]$.*

c) *If $f\in R$ and $g\in R$ on $[a,b]$, then $f/g\in R$ on $[a,b]$ whenever $g$ is bounded away from $0$.*

d) *If $f$ and $g$ are bounded functions having the same discontinuities on $[a,b]$, then $f\in R$ on $[a,b]$ if and only if $g\in R$ on $[a,b]$.*

e) *Let $g\in R$ on $[a,b]$ and assume that $m\le g(x)\le M$ for all $x\in[a,b]$. If $f$ is continuous on $[m,M]$, the composite function $h$ defined by $h(x)=f[g(x)]$ is Riemann-integrable on $[a,b]$.*

## 复值函数的Riemann-Stieltjes积分

如果将$f$和$\alpha$都从实值函数放宽到复值函数，则成为复值函数的Riemann-Stieltjes积分，定义7.1仍然可用，定理7.2, 7.3, 7.4, 7.6和7.7都可以原样照搬。此外，通过如下的定理，复值函数的Riemann-Stieltjes积分能够呗轻易地转为实值函数的Riemann-Stieltjes积分。

#### Theorem 7.50

*Let $f=f_1+if_2$ and $\alpha=\alpha_1+i\alpha_2$ be complex-valued functions defined on an interval $[a,b]$. Then we have*
$$
\int_a^bfd\alpha=\left(\int_a^bf_1d\alpha_1-\int_a^bf_2d\alpha_2\right)+i\left(\int_a^bf_2d\alpha_1+\int_a^bf_1d\alpha_2\right)
$$
*whenever all four integrals on the right exist.*

利用这个定理，可以在复值函数情形使用很多实值函数积分的性质。例如定理7.32和定理7.34仍然会成立。