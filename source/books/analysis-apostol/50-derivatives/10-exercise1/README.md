# Exercise 1-9 (Real-valued functions)

In the following exercises assume, where necessary, a knowledge of the formulas for differentiating the elementary trigonometric, exponential, and logarithmic functions. 

### 5.1

A function $f$ is said to satisfy a Lipschitz condition of order $\alpha$ at $c$ if there exists a positive number $M$ (which may depend on $c$) and a 1-ball $B(c)$ such that
$$
|f(x)-f(c)|<M|x-c|^{\alpha},\quad x\in B(c),x\neq c
$$
(a) Show that a function which satisfies a Lipschitz condition of order $\alpha$ is continuous at $c$ if $\alpha>0$, and has a derivative at $c$ if $\alpha>1$.

(b) Give an example of a function satisfying a Lipschitz condition of order $1$ at $c$ for which $f'(c)$ does not exist. 

#### Solution

(a) If $\alpha>0$, then for $\forall\varepsilon>0$, let $0<\delta<(\varepsilon)^{1/\alpha}/M$ such that $(c-\delta,c+\delta)\subseteq B(c)$, then whenever $|x-c|<\delta$, we have
$$
|f(x)-f(c)|<M|x-c|^{\alpha}<M\delta^{\alpha}<\varepsilon,\quad{x\neq c}
$$
and when $x=c$, we have $0=|f(x)-f(c)|<\varepsilon$. Thus $f$ is continuous at $c$.

If $\alpha>1$, then as $x\to c,x\neq c$, we have
$$
\left|\dfrac{f(x)-f(c)}{x-c}\right|<M|x-c|^{\alpha-1}\to 0
$$
thus $f$ has a derivative at $c$ and $f'(c)=0$.

(b) Let $f(x)=|x|$ and $c=0$, then $|f(x)-f(0)|=|f(x)|=|x|<2|x-0|$ for any 1-ball $B(0)$, but $f$ is not differentiable at $0$ since $\lim_{x\to0}f(x)/x$ does not exist.

### 5.2

In each of the following cases, determine the intervals in which the function $f$ is increasing or decreasing and find the maxima and minima (if any) in the set where each $f$ is defined.  

(a) $f(x)=x^3+ax+b,x\in\mathbf{R}$.

(b) $f(x)=\log(x^2-9),|x|>3$.

(c) $f(x)=x^{2/3}(x-1)^4,0\le{x}\le1$.

(d) $f(x)=(\sin{x})/x$ if $x\neq 0$, $f(0)=1,0\le{x}\le\pi/2$.

#### Solution

(a) We have $f'(x)=3x^2+a$. If $a\ge0$, then $f$ is increasing on $\mathbf{R}$. If $a<0$, then we have $f$ increasing on $(-\infty,-\sqrt{-a/3})$ and $(\sqrt{-a/3},+\infty)$, decreasing on $[-\sqrt{-a/3},\sqrt{-a/3}]$. $f$ has a local maxima at $-\sqrt{-a/3}$, has a local minima at $\sqrt{-a/3}$.

(b) We have $f'(x)=2x/(x^2-9)$, so $f'(x)>0$ when $x>3$ and $f'(x)<0$ when $x<-3$, thus $f$ is increasing on $(3,+\infty)$ and decreasing on $(-\infty,3)$, $f$ has no local maxima or minima.

(c) We have
$$
f'(x)=\dfrac{2}{3}(x-1)^3(7x^{2/3}-x^{-1/3})
$$
let $f'(x)=0$ we have $x=0,x=1/7$, so $f$ is increasing on $[0,1/7)$, decreasing on $(1/7,1]$, $f$ has a local maxima at $1/7$, and has local minima at $0$ and $1$.

(d) We have
$$
f'(x)=\dfrac{x\cos{x}-\sin{x}}{x^2},x\neq0
$$
and
$$
f'(0)=\lim_{x\to0}\dfrac{\dfrac{\sin{x}}{x}-1}{x}=\lim_{x\to0}\dfrac{\sin{x}-x}{x^2}=\lim_{x\to0}\dfrac{\cos{x}-1}{2x}\lim_{x\to0}\dfrac{-\sin{x}}{2}=0
$$
In the interval $(0,\pi/2]$ we have $\sin{x}<x<\tan{x}$, thus $x\cos{x}-\sin{x}<0$, so $f$ is decreasing on $[0,\pi/2]$ and $f$ has a local maxima at $0$, a local minima at $\pi/2$.

### 5.3

Find a polynomial $f$ of lowest possible degree such that
$$
f(x_1)=a_1\quad f(x_2)=a_2,\quad f'(x_1)=b_1,\quad f'(x_2)=b_2,
$$
where $x_1\neq x_2$ and $a_1,a_2,b_1,b_2$ are given real numbers.

#### Solution

If $b_1=b_2$ and $a_2-a_1=b_1(x_2-x_1)$, then $f(x)=b_1x+a_1-b_1x_1$ satisfy the condition. Other cases where the lowest possible degree of $f$ is $2$ or $3$ can be similarly deduced.

### 5.4

Define $f$ as follows: $f(x)=e^{-1/x^2}$ if $x\neq 0,f(0)=0$. Show that

(a) $f$ is continuous for all $x$.

(b) $f^{(n)}$ is continuous for all $x$ and $f^{(n)}(0)=0,(n=1,2\dots)$.

#### Proof

(a) It is obvious that $f$ is continuous when $x\neq 0$, and 
$$
\lim_{x\to0}f(x)=\lim_{x\to0}e^{-1/x^2}=0=f(0)
$$
(b) We have $f'(x)=2x^{-3}e^{-1/x^2}$ when $x\neq 0$, thus
$$
\lim_{x\to0}f'(x)=\lim_{x\to0}2x^{-3}e^{-1/x^2}=\lim_{y\to\infty}\dfrac{2(\sqrt{y})^3}{e^y}=0
$$
and
$$
f'(0)=\lim_{x\to0}\dfrac{e^{-1/x^2}-f(0)}{x-0}=\lim_{x\to0}\dfrac{e^{-1/x^2}}{x}=\lim_{y\to\infty}\dfrac{\sqrt{y}}{e^y}=0
$$
so $f'(x)$ is continuous for all $x$ and $f'(0)=0$. Notice that $f^{(n)}(x)=P(1/x)f(x)$ for polynomial $P$ with no constant term, and $\lim_{x\to0}P(1/x)f(x)=0$ for all $P$ with finite degrees, thus $f^{(n)}$ is continuous for all $x$ and $f^{(n)}(0)=0$.

### 5.5

Define $f,g,h$ as follows: $f(0)=g(0)=h(0)=0$ and if $x\neq 0$, $f(x)=\sin(1/x)$, $g(x)=x\sin(1/x)$, $h(x)=x^2\sin(1/x)$. Show that

(a) $f'(x)=-1/x^2\cos(1/x)$ if $x\neq 0$; $f'(0)$ does not exist.

(b) $g'(x)=\sin(1/x)-1/x\cos(1/x)$ if $x\neq 0$; $g'(0)$ does not exist.

(c) $h'(x)=2x\sin(1/x)-\cos(1/x)$ if $x\neq 0$; $h'(0)=0$; $\lim_{x\to0}h'(x)$ does not exist.

#### Solution

(a) That $f'(0)$ does not exist can be seen by
$$
f'(0)=\lim_{x\to0}\dfrac{\sin{\frac{1}{x}}-0}{x-0}=\lim_{x\to0}\dfrac{\sin{\frac{1}{x}}}{x}=\lim_{y\to\infty}y\sin{y}
$$
(b) That $g'(0)$ does not exist can be seen by
$$
g'(0)=\lim_{x\to0}\dfrac{x\sin{\frac{1}{x}}-0}{x-0}=\lim_{x\to0}\sin{\dfrac{1}{x}}
$$
(c) We have
$$
h'(0)=\lim_{x\to0}\dfrac{x^2\sin{\frac{1}{x}}-0}{x-0}=\lim_{x\to0}x\sin{\dfrac{1}{x}}
$$
however,
$$
\lim_{x\to0}h'(x)=\lim_{x\to0}(2x\sin{1/x}-\cos{1/x})
$$
the first item tends to $0$ as $x\to 0$, but the second item has no limit. 

### 5.6

Derive Leibnitz's formula for the $n$th derivative of the product $h$ of two functions $f$ and $g$:
$$
h^{(n)}(x)=\sum_{k=0}^n\begin{pmatrix}n\\k\end{pmatrix}f^{(k)}(x)g^{(n-k)}(x),\quad\text{where }\begin{pmatrix}n\\k\end{pmatrix}=\dfrac{n!}{k!(n-k)!}.
$$

#### Proof

If $n=1$, then
$$
h'(x)=f'(x)g(x)+f(x)g'(x)=\begin{pmatrix}1\\0\end{pmatrix}f(x)g^{(1)}(x)+\begin{pmatrix}1\\1\end{pmatrix}f^{(1)}(x)g(x)
$$
and the Leibnitz's formula is true. Now suppose the Leibnitz's formula holds for $h^{(n)}$, we consider the Leibnitz's formula for $h^{(n+1)}$, first we have
$$
\begin{aligned}
\begin{pmatrix}n\\k\end{pmatrix}+\begin{pmatrix}n\\k+1\end{pmatrix}&=\dfrac{n!}{k!(n-k)!}+\dfrac{n!}{(k+1)!(n-k-1)!}
\\&=\dfrac{n!}{k!(n-k-1)!}\left(\dfrac{1}{n-k}+\dfrac{1}{k+1}\right)
\\&=\dfrac{n!}{k!(n-k-1)!}\dfrac{n+1}{(n-k)(k+1)}
\\&=\dfrac{(n+1)!}{(k+1)!(n-k)!}=\begin{pmatrix}n+1\\k+1\end{pmatrix}
\end{aligned}
$$
and we obviously have
$$
\begin{pmatrix}n\\0\end{pmatrix}=\begin{pmatrix}n+1\\0\end{pmatrix}=\begin{pmatrix}n\\n\end{pmatrix}=\begin{pmatrix}n+1\\n+1\end{pmatrix}=1
$$
Thus
$$
\begin{aligned}
h^{(n+1)}(x)&=\left(h^{(n)}(x)\right)'=\left(\sum_{k=0}^n\begin{pmatrix}n\\k\end{pmatrix}f^{(k)}(x)g^{(n-k)}(x)\right)'
\\&=\sum_{k=0}^n\left(\begin{pmatrix}n\\k\end{pmatrix}f^{(k)}(x)g^{(n-k)}(x)\right)'
\\&=\underbrace{\sum_{k=0}^n\begin{pmatrix}n\\k\end{pmatrix}f^{(k+1)}(x)g^{(n-k)}(x)}_A+\underbrace{\sum_{k=0}^n\begin{pmatrix}n\\k\end{pmatrix}f^{(k)}(x)g^{(n-k+1)}(x)}_B
\end{aligned}
$$
Notice that
$$
A=\sum_{k=1}^{n}\begin{pmatrix}n\\k-1\end{pmatrix}f^{(k)}(x)g^{(n-k+1)}(x)+f^{(n+1)}(x)g(x)
\\
B=f(x)g^{(n+1)}(x)+\sum_{k=1}^n\begin{pmatrix}n\\k\end{pmatrix}f^{(k)}(x)g^{(n-k+1)}(x)
$$
we have
$$
\begin{aligned}
&\quad h^{(n+1)}(x)\\&=f(x)g^{(n+1)}(x)+\sum_{k=1}^n\begin{pmatrix}n+1\\k\end{pmatrix}f^{(k)}(x)g^{(n-k+1)}(x)+f^{(n+1)}(x)g(x)
\\&=\sum_{k=0}^{n+1}\begin{pmatrix}n+1\\k\end{pmatrix}f^{(k)}(x)g^{(n-k+1)}(x)
\end{aligned}
$$
So by mathematical induction, the Leibnitz's formula holds.

### 5.7

Let $f$ and $g$ be two functions defined and having finite third-order derivatives $f'''(x)$ and $g'''(x)$ for all $x\in\mathbf{R}$. If $f(x)g(x)=1$ for all $x$, show that the relations in (a), (b), (c) and (d) hold at those points where the denominators are not zero:

(a) $f'(x)/f(x)+g'(x)/g(x)=0$.

(b) $f''(x)/f'(x)-2f'(x)/f(x)-g''(x)/g'(x)=0$.

(c) $\dfrac{f'''(x)}{f'(x)}-3\dfrac{f'(x)g''(x)}{f(x)g'(x)}-3\dfrac{f''(x)}{f(x)}-\dfrac{g'''(x)}{g'(x)}=0$.

(d) $\dfrac{f'''(x)}{f'(x)}-\dfrac{3}{2}\left(\dfrac{f''(x)}{f'(x)}\right)^2=\dfrac{g'''(x)}{g'(x)}-\dfrac{3}{2}\left(\dfrac{g''(x)}{g'(x)}\right)^2$.

NOTE. The expression which appears on the left side of (d) is called the *Schwarzian* derivative of $f$ at $x$. 

(e) Show that $f$ and $g$ have the same Schwarzian derivative if
$$
g(x)=[af(x)+b]/[cf(x)+d],\quad\text{where }ad-bc\neq 0.
$$

#### Solution

(a) From $f(x)g(x)=1$ we get $\left(f(x)g(x)\right)'=f'(x)g(x)+f(x)g'(x)=0$, so
$$
\dfrac{f'(x)}{f(x)}+\dfrac{g'(x)}{g(x)}=\dfrac{f'(x)g(x)+f(x)g'(x)}{f(x)g(x)}=\dfrac{0}{1}=0
$$
(b) We abbreviate $f(x)$ to be $f$ and $g(x)$ to be $g$, thus from (a) we get
$$
\begin{aligned}
\dfrac{f'}{f}+\dfrac{g'}{g}=0&\implies\left(\dfrac{f'}{f}+\dfrac{g'}{g}\right)'=0
\\&\implies\dfrac{f''f-(f')^2}{f^2}+\dfrac{g''g-(g')^2}{g^2}=0
\\&\implies\dfrac{f''f-(f')^2}{f^2\dfrac{f'}{f}}=\dfrac{g''g-(g')^2}{g^2\dfrac{g'}{g}}
\\&\implies\dfrac{f''f-(f')^2}{ff'}=\dfrac{g''g-(g')^2}{gg'}
\\&\implies\dfrac{f''}{f'}-\dfrac{f'}{f}=\dfrac{g''}{g'}-\dfrac{g'}{g}
\\&\implies\dfrac{f''}{f'}-2\dfrac{f'}{f}-\dfrac{g''}{g'}=0
\end{aligned}
$$

during the process we use $f'/f=-g'/g$ several times.

(c) From the proof of (b) we have
$$
\begin{aligned}
&\quad\dfrac{f''}{f'}-\dfrac{f'}{f}=\dfrac{g''}{g'}-\dfrac{g'}{g}
\\&\implies\dfrac{f'''f'-(f'')^2}{(f')^2}-\dfrac{f''f-(f')^2}{f^2}=\dfrac{g'''g'-(g'')^2}{(g')^2}-\dfrac{g''g-(g')^2}{g^2}
\\&\implies\dfrac{f'''}{f'}-\left(\dfrac{f''}{f'}\right)^2-\dfrac{f''}{f}+\left(\dfrac{f'}{f}\right)^2=\dfrac{g'''}{g'}-\left(\dfrac{g''}{g'}\right)^2-\dfrac{g''}{g}+\left(\dfrac{g'}{g}\right)^2
\\&\implies\dfrac{f'''}{f'}-\dfrac{g'''}{g'}+\left(\dfrac{g''}{g'}\right)^2-\left(\dfrac{f''}{f'}\right)^2+\dfrac{g''}{g}-\dfrac{f''}{f}=0
\end{aligned}
$$
the last step comes from (a) since we have $(f'/f)^2=(g'/g)^2$, and
$$
-\dfrac{g''}{g'}=-\dfrac{g'}{g}\dfrac{g''}{g'}=\dfrac{f'}{f}\dfrac{g''}{g'}=\dfrac{f'g''}{fg'}
$$
from (b) we have
$$
\left(\dfrac{g''}{g'}\right)^2-\left(\dfrac{f''}{f'}\right)^2=\left(\dfrac{g''}{g'}+\dfrac{f''}{f'}\right)\left(\dfrac{g''}{g'}-\dfrac{f''}{f'}\right)=-2\dfrac{f'}{f}\left(\dfrac{g''}{g'}+\dfrac{f''}{f'}\right)
$$
So we get
$$
\dfrac{f'''}{f'}-\dfrac{g'''}{g'}-2\dfrac{f'}{f}\left(\dfrac{g''}{g'}+\dfrac{f''}{f'}\right)-\dfrac{f'g''}{fg'}-\dfrac{f''}{f}=0
$$
which gives
$$
\dfrac{f'''}{f'}-3\dfrac{f'g''}{fg'}-3\dfrac{f''}{f}-\dfrac{g'''}{g'}=0
$$
(d) From (c) we have
$$
\dfrac{f'''}{f'}-\dfrac{g'''}{g'}=3\dfrac{f'g''}{fg'}+3\dfrac{f''}{f}
$$
thus to prove (d) we only need to prove
$$
\dfrac{(f'')^2}{2(f')^2}-\dfrac{(g'')^2}{2(g')^2}=\dfrac{f'g''}{fg'}+\dfrac{f''}{f}\tag{*}
$$
Use the result of (b) we have
$$
\begin{aligned}\left(\dfrac{g''}{g'}\right)^2+2\dfrac{f'g''}{fg'}+2\dfrac{f''}{f}&=\left(\dfrac{f''}{f'}-2\dfrac{f'}{f}\right)^2+2\dfrac{f'g''}{fg'}+2\dfrac{f''}{f}
\\&=\left(\dfrac{f''}{f'}\right)^2-4\dfrac{f''}{f}+4\dfrac{(f')^2}{f^2}+2\dfrac{f'g''}{fg'}+2\dfrac{f''}{f}
\\&=\left(\dfrac{f''}{f'}\right)^2-2\dfrac{f''}{f}+4\dfrac{(f')^2}{f^2}+2\dfrac{f'g''}{fg'}
\end{aligned}
$$
since
$$
4\dfrac{(f')^2}{f^2}+2\dfrac{f'g''}{fg'}-2\dfrac{f''}{f'}=2\dfrac{f'}{f}\left(\dfrac{f''}{f'}-\dfrac{g''}{g'}\right)+2\dfrac{f'g''}{fg'}-2\dfrac{f''}{f'}=0
$$
we have
$$
\left(\dfrac{g''}{g'}\right)^2+2\dfrac{f'g''}{fg'}+2\dfrac{f''}{f}=\left(\dfrac{f''}{f'}\right)^2\tag{**}
$$
Now it is easy to see $(*)$ and $(**)$ are the same.

(e) If $c=0$, then $g(x)=[af(x)+b]/d$, then $g'=kf'$ with $k=a/d$ and $g''=kf''$, $g'''=kf'''$, it is easy to see $g$ and $f$ have the same Schwarzian derivative. Suppose $c\neq 0$, then we can write
$$
g(x)=\dfrac{a}{c}+\dfrac{bc-ad}{c(cf(x)+d)}\implies\left(g-\dfrac{a}{c}\right)\left(f+\dfrac{d}{c}\right)=\dfrac{bc-ad}{c^2}\neq 0
$$
Let $k=c^2/(bc-ad)$, and $G(x)=g(x)-a/c$, $F(x)=kf(x)+kd/c$, we have $F(x)G(x)=1$, also we see that
$$
F^{(n)}(x)=kf^{(n)}(x),G^{(n)}(x)=g^{(n)}(x),n=1,2,3
$$
which means the Schwarzian derivative of $F$ is equal to the Schwarzian derivative of $f$, and the Schwarzian derivative of $G$ is equal to the Schwarzian derivative of $g$. Finally $F(x)G(x)=1$ means the Schwarzian derivative of $F$ and $G$ are equal from the conclusion of (d).


### 5.8

Let $f_1,f_2,g_1,g_2$ be four functions having derivatives in $(a,b)$. Define $F$ by means of the determinant
$$
F(x)=\left|\begin{matrix}f_1(x)&f_2(x)\\g_1(x)&g_2(x)\end{matrix}\right|,\quad\text{if }x\in(a,b).
$$
(a) Show that $F'(x)$ exists for each $x$ in $(a,b)$ and that
$$
F'(x)=\left|\begin{matrix}f_1'(x)&f_2'(x)\\g_1(x)&g_2(x)\end{matrix}\right|+\left|\begin{matrix}f_1(x)&f_2(x)\\g'_1(x)&g'_2(x)\end{matrix}\right|
$$
(b) State and prove a more general result for $n$th order determinants.  

#### Solution

(a) As $F(x)=f_1(x)g_2(x)-f_2(x)g_1(x),x\in(a,b)$, thus for $x\in(a,b)$ we have
$$
\begin{aligned}
F'(x)&=f_1'(x)g_2(x)+f_1(x)g_2'(x)-f_2'(x)g_1(x)-f_2(x)g_1'(x)
\\&=\begin{vmatrix}f_1'(x)&f_2'(x)\\g_1(x)&g_2(x)\end{vmatrix}+\begin{vmatrix}f_1(x)&f_2(x)\\g_1'(x)&g_2'(x)\end{vmatrix}
\end{aligned}
$$
(b) If $\{f_{ij}\}$ with $i,j=1,\dots,n$ be functions having derivatives in $(a,b)$. Define $F$ by means of the determinant
$$
F(x)=\begin{vmatrix}f_{11}&\cdots&f_{1n}\\{\vdots}&&{\vdots}\\f_{n1}&\cdots&f_{nn}\end{vmatrix},\quad x\in(a,b)
$$
then $F'(x)$ exists for each $x$ in $(a,b)$ and
$$
F'(x)=\sum_{i=1}^n\begin{vmatrix}f_{11}&\cdots&f_{1n}\\{\vdots}&&{\vdots}\\f'_{i1}&\cdots&f'_{in}\\{\vdots}&&{\vdots}\\f_{n1}&\cdots&f_{nn}\end{vmatrix},\quad x\in(a,b)
$$
This result can be proved by induction on $n$. 

### 5.9

Given $n$ functions $f_1,\dots,f_n$, each having $n$th order derivatives in $(a,b)$. A function $W$, called the *Wronskian* of $f_1,\dots,f_n$, is defined as follows: For each $x$ in $(a,b)$, $W(x)$ is the value of the determinant of order $n$ whose element in the $k$th row and $m$th column is $f_m^{(k-1)}(x)$, where $k=1,2,\dots,n$ and $m=1,2,\dots,n$. [The expression $f_m^{(0)}(x)$ is written for $f_m(x)$.]

(a) Show that $W'(x)$ can be obtained by replacing the last row of determinant defining $W(x)$ by the $n$th derivatives $f_1^{(n)}(x),\dots,f_n^{(n)}(x)$.

(b) Assuming the existence of $n$ constants $c_1,\dots,c_n$, not all zero, such that $c_1f_1(x)+\cdots+c_nf_n(x)=0$ for every $x$ in $(a,b)$, show that $W(x)=0$ for each $x$ in $(a,b)$.

NOTE. A set of functions satisfying such a relation is said to be a *linearly dependent* set on $(a, b)$.  

(c) The vanishing of the Wronskian throughout $(a, b)$ is necessary, but not sufficient, for linear dependence of $f_1,\cdots, f_n$. Show that in the case of two functions, if the Wronskian vanishes throughout $(a, b)$ and if one of the functions does not vanish in $(a, b)$, then they form a linearly dependent set in $(a, b)$.  

#### Solution

(a) We write
$$
W(x)=\begin{vmatrix}f_1&\cdots&f_n\\{\vdots}&&{\vdots}\\f_1^{(n-1)}&\cdots&f_n^{(n-1)}\end{vmatrix}=\begin{vmatrix}F_1\\{\vdots}\\F_n\end{vmatrix}
$$
Use Exercise 5.8(b) we can get $W'(x)$ by
$$
W'(x)=\begin{vmatrix}F_1'\\{\vdots}\\F_n\end{vmatrix}+\cdots+\begin{vmatrix}F_1\\{\vdots}\\F_i'\\{\vdots}\\F_n\end{vmatrix}+\cdots+\begin{vmatrix}F_1\\{\vdots}\\F_n'\end{vmatrix}
$$
Notice that $F_j'=F_{j+1}$ for $j=1,\dots,n-1$, and if two rows in a determinant equals, the value of the determinant is zero. Thus we have
$$
W'(x)=\begin{vmatrix}F_1\\{\vdots}\\F_n'\end{vmatrix}=\begin{vmatrix}f_1&\cdots&f_n\\{\vdots}&&{\vdots}\\f_1^{(n-2)}&\cdots&f_n^{(n-2)}\\f_1^{(n)}&\cdots&f_n^{(n)}\end{vmatrix}
$$
(b) Without loss of generality, we suppose $c_1\neq 0$, then
$$
f_1(x)=-\dfrac{1}{c_1}(c_2f_2(x)+\cdots+c_nf_n(x))
$$
this gives
$$
f_1^{(k)}(x)=-\dfrac{1}{c_1}\left(c_2f_2^{(k)}(x)+\cdots+c_nf_n^{(k)}(x)\right),\quad k=1,2,\dots,n-1
$$
thus if we write $W(x)=|C_1,\dots,C_n|$ where $C_i=\begin{bmatrix}f_1\\{\vdots}\\f_1^{(n-1)}\end{bmatrix}$,  we can have
$$
C_1=-\dfrac{1}{c_1}(c_2C_2+\cdots+c_nC_n)
$$
which means $W(x)=0$.

(c) If there exist $f(x),g(x)$ and $f(x)\neq 0,\forall{x\in(a,b)}$, then suppose we further have $W(x)=f(x)g'(x)-g(x)f'(x)=0$ whenever $x\in(a,b)$, then
$$
\left(\dfrac{g(x)}{f(x)}\right)'=\dfrac{f(x)g'(x)-g(x)f'(x)}{f^2(x)}=0
$$
this means $g(x)/f(x)=c$ where $c$ is a constant, thus $g(x)=cf(x)$.