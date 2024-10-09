# Exercise 10-29 (Mean-Value Theorem)

### 5.10

Given a function $f$ defined and having a finite derivative in $(a, b)$ and such that $\lim_{x\to b-}f(x)=+\infty$. Prove that $\lim_{x\to b-}f'(x)$ either fails to exist or is infinite.

#### Proof

Assume $\lim_{x\to b-}f'(x)=A$ with $|A|<\infty$, then $\exists\delta>0$ such that whenever $b-\delta<x<b$, we have $|f'(x)-A|<1$, or $A-1<f'(x)<A+1$. Since $\lim_{x\to b-}f(x)=+\infty$, we can find a point $y\in(b-\delta,b)$ such that $f(y)\ge f(b-\delta)+(A+1)\delta$, By Mean-Value theorem, there exists a $\xi\in(b-\delta,y)$ such that
$$
f'(\xi)=\dfrac{f(y)-f(b-\delta)}{y-(b-\delta)}>\dfrac{f(y)-f(b-\delta)}{\delta}=A+1
$$
this is a contradiction.

### 5.11

Show that the formula in the Mean-Value Theorem can be written as follows: 
$$
\dfrac{f(x+h)-f(x)}{h}=f'(x+\theta h),
$$
where $0<\theta<1$. Determine $\theta$ as a function of $x$ and $h$ when

(a) $f(x)=x^2$

(b) $f(x)=x^3$

(c) $f(x)=e^x$

(d) $f(x)=\log{x},\quad{x>0}$.

Keep $x\neq 0$ fixed, and find $\lim_{h\to 0}\theta$ in each case.

#### Solution

In the Mean-Value Theorem, let $a=x,b=x+h$, then
$$
f(b)-f(a)=f'(c)(b-a),\quad c\in(a,b)
$$
can be written as
$$
f(x+h)-f(x)=f'(c)h,\quad c\in(x,x+h)
$$
write $c=x+\theta h$ with $0<\theta<1$, we have
$$
\dfrac{f(x+h)-f(x)}{h}=f'(x+\theta h),\quad 0<\theta<1
$$
(a) We have $f'(x)=2x$, thus
$$
\dfrac{f(x+h)-f(x)}{h}=2x+h,\quad f'(x+\theta h)=2x+2\theta h
$$
so $\theta=1/2$, and $\lim_{h\to 0}\theta=1/2$.

(b) We have $f'(x)=3x^2$, thus
$$
\dfrac{f(x+h)-f(x)}{h}=3x^2+3xh+h^2, \quad f'(x+\theta h)=3(x+\theta h)^2
$$
write $x/h=y$, the equation becomes $y+\theta=\pm\sqrt{y^2+y+1/3}$.  Notice that $h$ should be close to $0$, thus $y$ tends to be large, so when $x>0$, $\theta=\sqrt{y^2+y+1/3}-y$ and when $x<0$, $\theta=-\sqrt{y^2+y+1/3}-y$, when $x=0$, we have $\theta=\sqrt{1/3}$ and $\lim_{h\to 0}\theta=\sqrt{1/3}$. And we have when $x>0$:
$$
\lim_{h\to0}\theta=\lim_{y\to+\infty}\left(\sqrt{y^2+y+1/3}-y\right)=\lim_{y\to+\infty}\dfrac{y+1/3}{\sqrt{y^2+y+1/3}+y}=\dfrac{1}{2}
$$
and when $x<0$:
$$
\lim_{h\to0}\theta=\lim_{y\to-\infty}\left(-\sqrt{y^2+y+1/3}-y\right)=\lim_{y\to-\infty}\dfrac{y+1/3}{y-\sqrt{y^2+y+1/3}}=\dfrac{1}{2}
$$
thus $\lim_{h\to 0}\theta=1/2$ when $x\neq 0$.

(c) We have $f'(x)=e^x$, thus
$$
\dfrac{f(x+h)-f(x)}{h}=\dfrac{e^{x+h}-e^x}{h}=e^x\left(\dfrac{e^h-1}{h}\right)=e^{x+\theta h}\\
\implies\theta=\dfrac{1}{h}\log{\dfrac{e^h-1}{h}}
$$
and
$$
\lim_{h\to0}\theta=\lim_{h\to0}\dfrac{e^hh-e^h+1}{h(e^h-1)}=\lim_{h\to0}\dfrac{e^hh}{e^h-1+he^h}=\lim_{h\to0}\dfrac{e^hh+e^h}{2e^h+he^h}=\dfrac{1}{2}
$$
(d) We have $f(x)=\log{x}$ and $f'(x)=1/x$, thus
$$
\dfrac{f(x+h)-f(x)}{h}=\dfrac{1}{h}\log\left(1+\dfrac{h}{x}\right)=\dfrac{1}{x+\theta h}\\\implies\theta=\dfrac{1}{\log(1+h/x)}-\dfrac{x}{h}
\\
\begin{aligned}\lim_{h\to0}\theta&=\lim_{y\to0}\dfrac{1}{\log(1+y)}-\dfrac{1}{y}=\lim_{y\to0}\dfrac{y-\log(1+y)}{y\log(1+y)}\\&=\lim_{y\to0}\dfrac{1-\dfrac{1}{1+y}}{\log(1+y)+\dfrac{y}{1+y}}
\\&=\lim_{y\to0}\dfrac{y}{(1+y)\log(1+y)+y}=\lim_{y\to0}\dfrac{1}{1+\log(1+y)+1}=\dfrac{1}{2}
\end{aligned}
$$

### 5.12

Take $f(x)=3x^4-2x^3-x^2+1$ and $g(x)=4x^3-3x^2-2x$ in Theorem 5.20. Show that $f'(x)/g'(x)$ is never equal to the quotient $[f(1)-f(0)]/[g(1)-g(0)]$ if $0<x\le 1$. How do you reconcile this with the equation
$$
\dfrac{f(b)-f(a)}{g(b)-g(a)}=\dfrac{f'(x_1)}{g'(x_1)},\quad{a<x_1<b},
$$
obtainable from Theorem 5.20 when $n =1$?  

#### Solution

First $[f(1)-f(0)]/[g(1)-g(0)]=0$. Since $f'(x)=12x^3-6x^2-2x$ and $g'(x)=12x^2-6x-2$, so if $0<x\le1$, we have
$$
\dfrac{f'(x)}{g'(x)}=\dfrac{12x^3-6x^2-2x}{12x^2-6x-2}=x>0=\dfrac{f(1)-f(0)}{g(1)-g(0)}
$$
Theorem 5.20 when $n=1$ gives
$$
[f(x)-f(c)]g'(x_1)=[g(x)-g(c)]f'(x_1),\quad x_1\in(c,x)
$$
let $x=1,c=0$, then we have $[f(1)-f(0)]g'(x_1)=[g(1)-g(0)]f'(x_1)$, and only when $g'(x_1)\neq 0$ can we have
$$
\dfrac{f(1)-f(0)}{g(1)-g(0)}=\dfrac{f'(x_1)}{g'(x_1)}
$$
In fact, choose $\xi\in(0,1)$ such that $g'(\xi)=0$, then $f'(\xi)=\xi g'(\xi)=0$, which satisfies Theorem 5.20. That $\xi$ must exists can be seen from $g'(0)=-2<0,g'(1)=4>0$ and $g'$ is continuous on $[0,1]$.

### 5.13

In each of the following special cases of Theorem 5.20, take $n=1,c=a,x=b$ and show that $x_1=(a+b)/2$.

(a) $f(x)=\sin{x},\quad g(x)=\cos{x}$;

(b) $f(x)=e^x,\quad g(x)=e^{-x}$.

Can you find a general class of such pairs of functions $f$ and $g$ for which $x_1$ will always be $(a + b)/2$ and such that both examples (a) and (b) are in this class?  

#### Solution

(a) We suppose $a<b$, and $(\sin{b}-\sin{a})(-\sin{x_1})=(\cos{b}-\cos{a})\cos{x_1}$ with $x_1\in(a,b)$ means
$$
\tan{x_1}=-\dfrac{\cos{b}-\cos{a}}{\sin{b}-\sin{a}}=-\dfrac{2\sin{\frac{a-b}{2}}\sin{\frac{a+b}{2}}}{-2\cos{\frac{a+b}{2}}\sin{\frac{a-b}{2}}}=\tan\dfrac{a+b}{2}
$$
(b) We suppose $a<b$, and we have
$$
(e^b-e^a)(-e^{-x_1})=(e^{-b}-e^{-a})e^{x_1},\quad x_1\in(a,b)
$$
this means
$$
e^{2x_1}=-\dfrac{e^b-e^a}{e^{-b}-e^{-a}}=-e^{a+b}\dfrac{e^b-e^a}{e^a-e^b}=e^{a+b}\implies x_1=\dfrac{a+b}{2}
$$

### 5.14

Given a function $f$ defined and having a finite derivative $f'$ in the half-open interval $0 < x < 1$ and such that  $|f'(x)| < 1$. Define $a_n = f(1/n)$ for $n = 1, 2, 3, \dots$ , and show that $\lim_{n\to\infty}a_n$ exists. 

#### Proof

Let $\forall\varepsilon>0$, there exists $N>0$ such that $\varepsilon>1/N$, for $m>n>N$, we have
$$
|a_n-a_m|=\left|f(\dfrac{1}{n})-f(\dfrac{1}{m})\right|=\left|f'(x)\left(\dfrac{1}{n}-\dfrac{1}{m}\right)\right|<\left|\dfrac{1}{n}-\dfrac{1}{m}\right|<\dfrac{1}{n}<\varepsilon
$$
thus $\{a_n\}$ is a Cauchy sequence.

### 5.15

Assume that $f$ has a finite derivative at each point of the open interval $(a, b)$. Assume also that $\lim_{x\to c} f'(x)$ exists and is finite for some interior point $c$. Prove that the value of this limit must be $f'(c)$. 

#### Proof

We have
$$
f'(c)=\lim_{x\to c}\dfrac{f(x)-f(c)}{x-c}=\lim_{x\to c}\dfrac{f'(y)(x-c)}{x-c}=\lim_{x\to c}f'(y)
$$
for some $y$ between $x$ and $c$, when $x\to c$, we have $y\to c$, and the conclusion follows.

### 5.16

Let $f$ be continuous on $(a, b)$ with a finite derivative $f'$ everywhere in $(a, b)$, except
possibly at $c$. If $\lim_{x\to c} f'(x)$ exists and has the value $A$, show that $f'(c)$ must also exist and have the value $A$.

#### Proof

We have
$$
\lim_{x\to c}\dfrac{f(x)-f(c)}{x-c}=\lim_{x\to c}\dfrac{f'(y)(x-c)}{x-c}=\lim_{x\to c}f'(y)
$$
for some $y$ between $x$ and $c$, when $x\to c$, we have $y\to c$, and $\lim_{x\to c}f'(y)=A$, thus
$$
\lim_{x\to c}\dfrac{f(x)-f(c)}{x-c}=A
$$
which implies $f'(c)$ exists and $f'(c)=A$.

### 5.17

Let $f$ be continuous on $[0, 1]$, $f(0) = 0$, $f'(x)$ finite for each $x$ in $(0, 1)$. Prove that if $f'$ is an increasing function on $(0, 1)$, then so too is the function $g$ defined by the equation $g(x) = f(x)/x$.

#### Proof

for any $x\in (0,1)$ we can find some $c\in(0,x)$ such that
$$
f(x)=f(x)-f(0)=f'(c)(x-0)=xf'(c)
$$
so for this $x$, we have
$$
g'(x)=\dfrac{xf'(x)-f(x)}{x^2}=\dfrac{xf'(x)-xf'(c)}{x^2}=\dfrac{1}{x}\left(f'(x)-f'(c)\right)\ge0
$$
since $x>c>0$ and $f'$ is increasing. Thus $g$ is increasing.

### 5.18

Assume $f$ has a finite derivative in $(a, b)$ and is continuous on $[a, b]$ with $f(a)=f(b) =0$. Prove that for every real $\lambda$ there is some $c$ in $(a, b)$ such that $f'(c) = \lambda f(c)$.

#### Proof

Let $g(x)=e^{-\lambda x}$ and define $F(x)=g(x)f(x)$, which is continuous on $[a,b]$ and $F(a)=F(b)=0$, by Roll's theorem, there exist $c\in(a,b)$ such that $F'(c)=0$, which means
$$
-\lambda e^{-\lambda c}f(c)+e^{-\lambda c}f'(c)=0\implies f'(c)=\lambda f(c)
$$

### 5.19

Assume $f$ is continuous on $[a, b]$ and has a finite second derivative $f''$ in the open interval $(a, b)$. Assume that the line segment joining the points $A=(a, f(a))$ and $B = (b, f(b))$ intersects the graph of $f$ in a third point $P$ different from $A$ and $B$. Prove that $f''(c) = 0$ for some $c$ in $(a, b)$.

#### Proof

The line joining $A$ and $B$ can be written as
$$
y-f(a)=\dfrac{f(b)-f(a)}{b-a}(x-a)
$$
Write $P=(p,f(p))$, then $p\in(a,b)$ satisfy the equation above. Define
$$
F(x)=f(x)-f(a)-\dfrac{f(b)-f(a)}{b-a}(x-a),\quad x\in[a,b]
$$
It is easy to see that $F(a)=F(b)=0$, and further $F(p)=0$, by Roll's theorem, we can find $x_1\in(a,p)$ and $x_2\in(p,b)$ such that $F'(x_1)=F'(x_2)=0$, so we can find $c\in(x_1,x_2)$ such that $F''(c)=0$, we have
$$
F'(x)=f'(x)-\dfrac{f(b)-f(a)}{b-a},\quad F''(x)=f''(x)
$$
thus $f''(c)=F''(c)=0$.

### 5.20

If $f$ has a finite third derivative $f'''$ in $[a, b]$ and if
$$
f(a)=f'(a)=f(b)=f'(b)=0,
$$
prove that $f'''(c)=0$ for some $c\in(a,b)$.

#### Proof

By Roll's theorem, there is $d\in(a,b)$ such that $f'(d)=0$, thus we can find $x_1\in(a,d)$ and $x_2\in(d,b)$ such that $f''(x_1)=f''(x_2)=0$, which means we can further find $c\in(x_1,x_2)$ such that $f'''(c)=0$.

### 5.21

Assume $f$ is nonnegative and has a finite third derivative $f'''$ in the open interval $(0, 1)$. If $f(x)=0$ for at least two values of $x$ in $(0, 1)$, prove that $f'''(c) = 0$ for some $c$ in $(0, 1)$.

#### Proof

Suppose $f(a)=f(b)=0$ for $a,b\in(0,1)$, since $f$ is nonnegative in $(0,1)$, the point $a$ and $b$ are local minima of $f$, thus $f'(a)=f'(b)=0$, the conclusion follows from Exercise 5.20.

### 5.22

Assume $f$ has a finite derivative in some interval $(a, +\infty)$.

(a) If $f(x)\to1$ and $f'(x)\to{c}$ as $x\to+\infty$, prove that $c=0$.

(b) If $f'(x)\to1$ as $x\to+\infty$, prove that $f(x)/x\to1$ as $x\to+\infty$.

(c) If $f'(x)\to0$ as $x\to+\infty$, prove that $f(x)/x\to0$ as $x\to+\infty$.

#### Proof

(a) Assume $c\neq 0$, then $\exists G>1$ such that $x>G\implies |f'(x)|>c/2>0$, and $\exist N>G$ such that
$$
|f(n)-1|<1/2,\forall n>N\implies|f(2n)-f(n)|<1,n>N
$$
if we choose $n>N$ such that $n>2/c$, we have $|f(2n)-f(n)|=|f'(\xi)|n$ for some $\xi\in(n,2n)$, so we can have
$$
1=\dfrac{c}{2}\dfrac{2}{c}<|f'(\xi)|n=|f(2n)-f(n)|<1
$$
which is a contradiction.

(b) For $\forall\varepsilon>0$, there exist $G>0$ such that $|f'(x)-1|<\varepsilon$ whenever $x\ge G$. for any $x>G$, we can find some $c\in(G,x)$ such that
$$
f(x)=f(G)+f'(c)(x-G)
$$
which means
$$
\begin{aligned}\left|\dfrac{f(x)}{x}-1\right|&=\left|\dfrac{f(G)}{x}+f'(c)-1-\dfrac{f'(c)G}{x}\right|
\\&\le\left|\dfrac{f(G)-f'(c)G}{x}\right|+|f'(c)-1|
\\&<\dfrac{|f(G)|+(1+\varepsilon)G}{x}+\varepsilon
\end{aligned}
$$
let $x\to+\infty$, we can have
$$
\dfrac{|f(G)|+(1+\varepsilon)G}{x}<\varepsilon\implies\left|\dfrac{f(x)}{x}-1\right|<2\varepsilon
$$
(c) Let $g(x)=f(x)+x$, then $g'(x)=f'(x)+1$, so $g'(x)\to 1$ as $x\to+\infty$, use (b) we can have $g(x)/x\to 1$ as $x\to+\infty$, but $g(x)/x=f(x)/x+1$ for $\forall x\in(a,+\infty)$, and the conclusion follows.

### 5.23

Let $h$ be a fixed positive number. Show that there is no function $f$ satisfying the
following three conditions: $f(x)$ exists for $x\ge0$, $f'(0)=0$, $f'(x)\ge{h}$ for $x>0$.

#### Proof

That $f'(0)=0$ means $f'_+(0)=0$, thus $\exist\delta>0$ such that whenever $x\in(0,\delta)$, we have
$$
\dfrac{f(x)-f(0)}{x-0}<h
$$
choose some $x<\delta$, then there is $c\in(0,x)$ such that $f(x)-f(0)=f'(c)(x-0)$, then we have $f'(c)<h$, which is a contradiction.

### 5.24

If $h>0$ and if $f(x)$ exists (and is finite) for every $x$ in $(a - h, a + h)$, and if $f$ is
continuous on $[a - h, a + h]$, show that we have:

(a) $\dfrac{f(a+h)-f(a-h)}{h}=f'(a+\theta h)+f'(a-\theta h),\quad 0<\theta<1$;

(b) $\dfrac{f(a+h)-2f(a)+f(a-h)}{h}=f'(a+\lambda h)-f'(a-\lambda h),\quad 0<\lambda<1$.

(c) If $f''(a)$ exists, show that $f''(a)=\lim_{h\to0}\dfrac{f(a+h)-2f(a)+f(a-h)}{h^2}$.

(d) Give an example where the limit of the quotient in (c) exists but where $f''(a)$ does not exist. 

#### Solution

(a) Let $F(x)=f(a+x)-f(a-x)$, then $F$ is continuous on $[0,h]$ and $F'(x)$ exists in $[0,h)$. Thus we can find $c\in(0,h)$ such that
$$
F(h)-F(0)=f(a+h)-f(a-h)=F'(c)h=[f'(a+c)+f'(a-c)]h
$$
write $c=\theta h$, then $\theta\in (0,1)$.

(b) With a similar proof of (a) by replacing $F$ with
$$
F(x)=f(a+x)+f(a-x)-2f(a)
$$
(c) Let $F$ be defined like (b) and $G(x)=x^2$, by generalized Mean-Value Theorem, we can find $\lambda\in(0,1)$ such that
$$
[F(x)-F(0)]G'(\lambda x)=F'(\lambda x)[G(x)-G(0)]
$$
which means
$$
[f(a+x)+f(a-x)-2f(a)]2\lambda x=x^2[f'(a+\lambda x)-f'(a-\lambda x)]
$$
or
$$
\dfrac{f'(a+\lambda x)-f'(a-\lambda x)}{2\lambda x}=\dfrac{f(a+x)+f(a-x)-2f(a)}{x^2}
$$
the conclusion follows since we can write $f''(a)$ as
$$
f''(a)=\lim_{h\to0}\dfrac{f'(a+\lambda h)-f'(a-\lambda h)}{2\lambda h}
$$
(d) Let $f(x)=x^2/2$ when $x\ge 0$ and $-x^2/2$ when $x<0$, then for $a=0$, we see that $f(x)$ exists and is continuous on $[-h,h]$ if $h>0$, and
$$
\lim_{h\to0}\dfrac{f(h)-2f(0)+f(-h)}{h^2}=\lim_{h\to 0}\dfrac{0}{h^2}=0
$$
but
$$
f'(x)=\begin{cases}x,\quad &x\ge0\\-x,\quad &x<0\end{cases}
$$
so $f''_+(0)=1$ and $f''_-(0)=-1$, thus $f''(0)$ does not exist.

### 5.25

Let $f$ have a finite derivative in $(a, b)$ and assume that $c\in(a, b)$. Consider the following condition: For every $\varepsilon>0$ there exists a 1-ball $B(c; \delta)$, whose radius $\delta$ depends only on $\varepsilon$ and not on $c$, such that if $x\in B(c;\delta)$, and $x\neq c$, then
$$
\left|\dfrac{f(x)-f(c)}{x-c}-f'(c)\right|<\varepsilon
$$
Show that $f'$ is continuous on $(a,b)$ if this condition holds throughout $(a,b)$.

#### Solution

Assume $f'(x)$ is not continuous at some point $c\in(a,b)$, since $f'$ is finite in $(a,b)$, the discontinuity should be a jump or removable, in either case, we can find an interval $(m,c)$ or $(c,m)$ such that $|f'(x)-f'(c)|>\varepsilon_0$ for some given $\varepsilon_0$ whenever $x$ is in the interval. For this $\varepsilon_0$, we select the corresponding $\delta$ for the condition to hold, let $\delta'=\min(\delta,|c-m|)$, then if $x$ is in the interval $(c-\delta',c)$ or $(c,c+\delta')$ we have
$$
|f'(x)-f'(c)|>\varepsilon_0,\quad\left|\dfrac{f(x)-f(c)}{x-c}-f'(c)\right|<\varepsilon_0
$$
Choose $d$ between $x$ and $c$ such that
$$
\dfrac{f(x)-f(c)}{x-c}=f'(d)
$$
we have $|f'(d)-f'(c)|>\varepsilon_0$ and $|f'(x)-f'(c)|<\varepsilon_0$, which is a contradiction.

### 5.26

Assume $f$ has a finite derivative in $(a, b)$ and is continuous on $[a,b]$, with $a\le f(x)\le b$ for all $x\in[a,b]$ and $|f'(x)|\le\alpha<1$ for all $x\in(a,b)$. Prove that $f$ has a unique fixed point in $[a,b]$.

#### Proof

Let $F(x)=f(x)-x$, then $F(a)\ge 0$ and $F(b)\le 0$, thus there exists $c\in[a,b]$ such that $F(c)=0$ or $f(c)=c$. Now assume $f$ has more than one fixed point, then $\exist c_1,c_2\in[a,b]$ and $F(c_1)=F(c_2)=0$, by Roll's theorem, we can find $d\in(c_1,c_2)\subseteq(a.b)$ such that $F'(d)=f'(d)-1=0$, which means $f'(d)=1$, but we shall have $|f'(d)|<1$, so we get a contradiction.

### 5.27

Give an example of a pair of functions $f$ and $g$ having finite derivatives in $(0, 1)$, such that
$$
\lim_{x\to0}\dfrac{f(x)}{g(x)}=0,
$$
but such that $\lim_{x\to0}f'(x)/g'(x)$ does not exist, choosing $g$ so that $g'(x)$ is never zero.

#### Solution

Let $f(x)=x$ and $g(x)=x^2+1$, then $g'(x)=2x\ne0$ if $x\in(0,1)$, but
$$
\lim_{x\to0}\dfrac{f(x)}{g(x)}=\lim_{x\to0}\dfrac{x}{x^2+1}=0,\quad\lim_{x\to0}\dfrac{f'(x)}{g'(x)}=\lim_{x\to0}\dfrac{1}{2x}
$$
which does not exist.

### 5.28

Prove the following theorem:

Let $f$ and $g$ be two functions having finite $n$th derivatives in $(a,b)$. For some interior point $c$ in $(a,b)$, assume that $f(c)=f'(c)=\cdots=f^{(n-1)}(c)=0$, and that $g(c)=g'(c)=\cdots=g^{(n-1)}(c)=0$, but $g^{(n)}(x)$ is never zero in $(a,b)$. Show that
$$
\lim_{x\to c}\dfrac{f(x)}{g(x)}=\dfrac{f^{(n)}(c)}{g^{(n)}(c)}.
$$
NOTE: $f^{(n)}$ and $g^{(n)}$ are not assumed to be continuous at $c$. 

#### Proof

For any $x\in(a,b)$ with $x\neq c$ such that $g(x)\neq 0$, apply Theorem 5.20 to $f$ and $g$, we can find $x_1$ between $x$ and $c$ such that
$$
\left[f(x)-\sum_{k=0}^{n-2}\dfrac{f^{(k)}(c)}{k!}(x-c)^k\right]g^{(n-1)}(x_1)=f^{(n-1)}(x_1)\left[g(x)-\sum_{k=0}^{n-2}\dfrac{g^{(k)}(c)}{k!}(x-c)^k\right]
$$

which gives $f(x)g^{(n-1)}(x_1)=f^{(n-1)}(x_1)g(x)$, use the condition $f^{(n-1)}(c)=g^{(n-1)}(c)=0$, we can further get
$$
f(x)\left[g^{(n-1)}(x_1)-g^{(n-1)}(c)\right]=g(x)\left[f^{(n-1)}(x_1)-f^{(n-1)}(c)\right]
$$
notice that $g^{(n-1)}(x_1)=g^{(n-1)}(c)$ implies we can find some $x'$ between $x_1$ and $c$ such that $g^{(n)}(x')=0$, but $g^{(n)}(x)$ is never zero in $(a,b)$ means we must have $g^{(n-1)}(x_1)\neq g^{(n-1)}(c)$, thus the equation above can be written as
$$
\dfrac{f(x)}{g(x)}=\dfrac{f^{(n-1)}(x_1)-f^{(n-1)}(c)}{g^{(n-1)}(x_1)-g^{(n-1)}(c)}
$$
Now let $x\to c$, then $x_1\to c$ at the same time, thus
$$
\lim_{x\to c}\dfrac{f(x)}{g(x)}=\lim_{x_1\to c}\dfrac{f^{(n-1)}(x_1)-f^{(n-1)}(c)}{g^{(n-1)}(x_1)-g^{(n-1)}(c)}=\lim_{x_1\to c}\dfrac{\dfrac{f^{(n-1)}(x_1)-f^{(n-1)}(c)}{x_1-c}}{\dfrac{g^{(n-1)}(x_1)-g^{(n-1)}(c)}{x_1-c}}=\dfrac{f^{(n)}(c)}{g^{(n)}(c)}
$$

### 5.29

Show that the formula in Taylor's theorem can also be written as follows:
$$
f(x)=\sum_{k=0}^{n-1}\dfrac{f^{(k)}(c)}{k!}(x-c)^k+\dfrac{(x-c)(x-x_1)^{n-1}}{(n-1)!}f^{(n)}(x_1),
$$
where $x_1$ is interior to the interval joining $x$ and $c$. Let $1-\theta=(x-x_1)/(x-c)$. Show that $0<\theta<1$ and deduce the following form of the remainder term (due to Cauchy):
$$
\dfrac{(1-\theta)^{n-1}(x-c)^n}{(n-1)!}f^{(n)}[\theta x+(1-\theta)c].
$$

#### Proof

Keep $x$ fixed and define
$$
F(t)=f(t)+\sum_{k=1}^{n-1}\dfrac{f^{(k)}(t)}{k!}(x-t)^k,\quad G(t)=g(t)=t
$$
Apply Theorem 5.12 to get $x_1$ between $x$ and $c$ such that
$$
F'(x_1)[G(x)-G(c)]=G'(x_1)[F(x)-F(c)]
$$
which means
$$
\dfrac{(x-x_1)^{n-1}}{(n-1)!}f^{(n)}(x_1)(x-c)=f(x)-f(c)-\sum_{k=1}^{n-1}\dfrac{f^{(k)}(c)}{k!}(x-c)^k
$$
since $f(c)=\frac{f(c)}{0!}(x-c)^0$, we get $f(x)$ as the desired form.

As
$$
1-\theta=\dfrac{x-x_1}{x-c}\implies x_1=x-(1-\theta)(x-c)=\theta x+(1-\theta)c
$$
we can have
$$
\begin{aligned}
\dfrac{(x-c)(x-x_1)^{n-1}}{(n-1)!}f^{(n)}(x_1)&=\dfrac{(x-c)^n\dfrac{(x-x_1)^{n-1}}{(x-c)^{n-1}}}{(n-1)!}f^{(n)}(x_1)\\&=\dfrac{(x-c)(1-\theta)^{n-1}}{(n-1)!}f^{(n)}[\theta x+(1-\theta)c]
\end{aligned}
$$
