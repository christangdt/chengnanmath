# Exercise 35-37 (Complex-valued functions)

### 5.35

Let $S$ be an open set in $\mathbf{C}$ and let $S^*$ be the set of complex conjugates $\overline{z}$ where $z\in S$. If $f$ is defined on $S$, define $g$ on $S^*$ as follows: $g(\overline{z})=\overline{f(z)}$. If $f$ is differentiable at $c$ prove that $g$ is differentiable at $\overline{c}$ and that $g'(\overline{c})=\overline{f'(c)}$.

#### Proof

If $z\to\overline{c}$, then $\overline{z}\to\overline{\overline{c}}=c$, vise versa, thus
$$
\lim_{z\to\overline{c}}\dfrac{g(z)-g(\overline{c})}{z-\overline{c}}=\lim_{z\to\overline{c}}\dfrac{\overline{f(\overline{z})}-\overline{f(c)}}{z-\overline{c}}=\lim_{z\to\overline{c}}\dfrac{\overline{f(\overline{z})-f(c)}}{\overline{\overline{z}-c}}=\overline{\lim_{\overline{z}\to c}\dfrac{f(\overline{z})-f(c)}{\overline{z}-c}}
=\overline{f'(c)}
$$
and the conclusion follows.

### 5.36

i) In each of the following examples write $f=u+iv$ and find explicit formulas for $u(x,y)$ and $v(x,y)$: (Functions below are to be defined as indicated in Chapter 1).

a) $f(z)=\sin{z}$,

b) $f(z)=\cos{z}$,

c) $f(z)=|z|$, 

d) $f(z)=\overline{z}$,

e) $f(z)=\arg{z}\quad(z\neq0)$,

f) $f(z)=\text{Log }z\quad(z\neq0)$,

g) $f(z)=e^{z^2}$,

h) $f(z)=z^{\alpha}\quad(\alpha\text{ complex, }z\neq0)$.

ii) Show that $u$ and $v$ satisfy the Cauchy-Riemann equations for the following values of $z$: All $z$ in (a),(b),(g); no $z$ in (c),(d),(e); all $z$ except real $z\le0$ in (f),(h).

iii) Compute the derivative $f'(z)$ in (a),(b),(f),(g),(h), assuming it exists.

#### Solution

Refer to Chapter 1 for the definition and theorem of functions, let $z=x+iy$, The Cauchy-Riemann equations states that $D_1u=D_2v$ and $D_1v=-D_2u$. For (a)-(h) we do (i)-(iii) together. 

(a) $\sin{z}=\sin{x}\cosh{y}+i\cos{x}\sinh{y}$, thus $u(x,y)=\sin{x}\cosh{y}$, $v(x,y)=\cos{x}\sinh{y}$.  Thus $D_1u=\cos{x}\cosh{y}$, $D_1v=-\sin{x}\sinh{y}$, $D_2u=\sin{x}\sinh{y}$, $D_2v=\cos{x}\cosh{y}$, and Cauchy-Riemann equations are satisfied for all $z$. We have 
$$
f'(z)=f'(x+iy)=\cos{x}\cosh{y}-i\sin{x}\sinh{y}
$$


(b) $\cos{z}=\cos{x}\cosh{y}-i\sin{x}\sinh{y}$, thus $u(x,y)=\cos{x}\cosh{y}$, $v(x,y)=-\sin{x}\sinh{y}$. And $D_1u=-\sin{x}\cosh{y}$, $D_1v=-\cos{x}\sinh{y}$, $D_2u=\cos{x}\sinh{y}$, $D_2v=-\sin{x}\cosh{y}$. It is easy to see the Cauchy-Riemann equations are satisfied for all $z$. We have
$$
f'(z)=f'(x+iy)=-\sin{x}\cosh{y}-i\cos{x}\sinh{y}
$$


(c) $|z|=\sqrt{x^2+y^2}$, thus $u(x,y)=\sqrt{x^2+y^2}$ and $v(x,y)=0$. So $D_2u=D_2v=0$ and
$$
D_1u=\begin{cases}\dfrac{2x}{\sqrt{x^2+y^2}},\quad&(x,y)\neq(0,0)\\\text{not exist}&(x,y)=(0,0)\end{cases}
\quad
D_1v=\begin{cases}\dfrac{2y}{\sqrt{x^2+y^2}},\quad&(x,y)\neq(0,0)\\\text{not exist}&(x,y)=(0,0)\end{cases}
$$
thus for all $z=x+iy$ we have $D_1u\neq D_2v$ and $D_1v\neq-D_2u$.



(d) $\overline{z}=x-iy$, thus $u(x,y)=x$ and $v(x,y)=-y$. So $D_1u=1,D_1v=0,D_2u=0$, and $D_2v=-1$, for all $z=x+iy$ we have $D_1u\neq D_2v$ and $D_1v\neq-D_2u$.



(e) We have $x=|z|\cos({\arg{z}})$ and $y=|z|\sin(\arg{z})$, thus when $x\neq0$, there is $\tan(\arg{z})=y/x$ and $f(z)=\arctan{y/x}$, and it is easy to see $f(z)=\pi/2$ when $x=0,y>0$ and $f(z)=-\pi/2$ when $x=0,y<0$, so
$$
f(z)=f(x+iy)=\begin{cases}
\arctan{\dfrac{y}{x}},\quad&x\neq0
\\
\dfrac{\pi}{2},\quad&x=0,y>0
\\
-\dfrac{\pi}{2},\quad&x=0,y<0
\end{cases}
$$
and we immediately get
$$
v(x,y)=0,\quad u(x,y)=\begin{cases}
\arctan{\dfrac{y}{x}},\quad&x\neq0
\\
\dfrac{\pi}{2},\quad&x=0,y>0
\\
-\dfrac{\pi}{2},\quad&x=0,y<0
\end{cases}
$$
So $D_1v=D_2v=0$, and 
$$
D_1u(x,y)=\begin{cases}\dfrac{-y}{x^2+y^2},\quad&x\neq0\\\text{not exist}\quad&x=0\end{cases},\quad
D_2u(x,y)=\begin{cases}\dfrac{x}{x^2+y^2},\quad&x\neq0\\\text{not exist}\quad&x=0\end{cases}
$$
for all $z=x+iy$ we have $D_1v\neq-D_2u$.



(f) Since $f(z)=\log|z|+i\arg(z)$, we see that $u(x,y)=\log\sqrt{x^2+y^2}$ and $v(x,y)$ is defined the same as the $u(x,y)$ in (e). We have
$$
D_1u=\dfrac{1}{\sqrt{x^2+y^2}}\dfrac{2x}{2\sqrt{x^2+y^2}}=\dfrac{x}{x^2+y^2},\quad D_2u=\dfrac{y}{x^2+y^2}
$$
I omit the part (ii) and (iii).



(g) We have $z^2=zz=(x+iy)^2=x^2-y^2+i2xy$ which is a complex number, so
$$
f(z)=e^{x^2-y^2+i2xy}=e^{x^2-y^2}(\cos{2xy}+i\sin{2xy})
$$
thus $u(x,y)=e^{x^2-y^2}\cos{2xy}$ and $v(x,y)=e^{x^2-y^2}\sin{2xy}$.

We have 
$$
D_1u=e^{x^2-y^2}(2x\cos{2xy}-2y\sin{2xy}),D_2u=e^{x^2-y^2}(-2y\cos{2xy}-2x\sin{2xy})
\\
D_1v=e^{x^2-y^2}(2x\sin{2xy}+2y\cos{2xy}),D_2v=e^{x^2-y^2}(-2y\sin{2xy}+2x\cos{2xy})
$$
It is easy to see the Cauchy-Riemann equations are satisfied for all $z$. We have
$$
\begin{aligned}f'(z)&=e^{x^2-y^2}(2x\cos{2xy}-2y\sin{2xy})+ie^{x^2-y^2}(2x\sin{2xy}+2y\cos{2xy})
\\&=e^{x^2-y^2}2x(\cos{2xy}+i\sin{2xy})+ie^{x^2-y^2}2y(\cos{2xy}+i\sin{2xy})
\\&=e^{z^2}2(x+iy)=2ze^{z^2}
\end{aligned}
$$


(h) $z^{\alpha}=e^{\alpha\text{Log }z}$, let $a=\Re(\alpha)$ and $b=\Im(\alpha)$, then $\alpha=a+ib$, use (f) we know $\text{Log }z=\log|z|+i\arg(z)$, thus
$$
\alpha\text{Log }z=a\log|z|-b\arg(z)+i(a\arg(z)+b\log|z|)
$$
so we have
$$
f(z)=e^{a\log|z|-b\arg(z)}[\cos(a\arg(z)+b\log|z|)+i\sin(a\arg(z)+b\log|z|)]
$$
thus
$$
u(x,y)=\begin{cases}
e^{a\log\sqrt{x^2+y^2}-b\arctan{\frac{y}{x}}}\cos\left(a\arctan{\dfrac{y}{x}}+b\log\sqrt{x^2+y^2}\right),&x\neq0
\\
e^{a\log{y}-\frac{b\pi}{2}}\cos\left(\dfrac{a\pi}{2}+b\log{y}\right),\quad&x=0,y>0
\\
e^{a\log(-y)+\frac{b\pi}{2}}\cos\left(-\dfrac{a\pi}{2}+b\log({-y})\right),\quad&x=0,y<0
\end{cases}
$$
and
$$
v(x,y)=\begin{cases}
e^{a\log\sqrt{x^2+y^2}-b\arctan{\frac{y}{x}}}\sin\left(a\arctan{\dfrac{y}{x}}+b\log\sqrt{x^2+y^2}\right),&x\neq0
\\
e^{a\log{y}-\frac{b\pi}{2}}\sin\left(\dfrac{a\pi}{2}+b\log{y}\right),\quad&x=0,y>0
\\
e^{a\log(-y)+\frac{b\pi}{2}}\sin\left(-\dfrac{a\pi}{2}+b\log({-y})\right),\quad&x=0,y<0
\end{cases}
$$
I omit the part (ii) and (iii).

### 5.37

Write $f=u+iv$ and assume that $f$ has a derivative at each point of an open dist $D$ centered at $(0,0)$. If $au^2+bv^2$ is constant on $D$ for some real $a$ and $b$ not both $0$, prove that $f$ is constant on $D$.

#### Proof

If $a=0,b\neq 0$, then $v^2$ is constant on $D$, thus $vD_1v=vD_2v=0$. If $v\neq0$, then $v^2\neq 0$, but $v^2D_1v=v(vD_1v)=v0=0$ and $v^2D_2v=0$, this means $D_1v=D_2v=0$. If $v=0$ then we immediately get $D_1v=D_2v=0$. Thus $f'=0$ by Cauchy-Riemann equation and $f$ is constant by Theorem 5.23. The case when $a\neq0,b=0$ is similar.

Suppose $a\neq0,b\neq0$. Since $f$ is differentiable on $D$, we use Cauchy-Riemann equation to have $D_1u=D_2v$ and $D_1v=-D_2u$ on $D$, since $au^2+bv^2$ is constant on $D$, we have
$$
D_1(au^2+bv^2)=2auD_1u+2bvD_1v=0\implies auD_1u+bvD_1v=0
\\
D_2(au^2+bv^2)=2auD_2u+2bvD_2v=0\implies auD_2u+bvD_2v=0
$$
the second equality means $bvD_1u-auD_1v=0$, thus we have
$$
auD_1^2u+bvD_1vD_1u=0,bvD_1uD_1v-auD_1^2v=0\implies au(D_1^2u+D_1^2v)=0
$$
similarly $bv(D_1^2u+D_1^2v)=0$, combined to get $(au^2+bv^2)(D_1^2u+D_1^2v)=0$. If $au^2+bv^2$ is a nonzero constant on $D$, then we have $D_1u=D_1v=0$ on $D$ and the conclusion follows. If $au^2+bv^2=0$ on $D$, then $u^2=(-b/a)v^2$, one case is $u=0$ on $D$, thus $v=0$ on $D$ and $f$ is constant, the other case is that $u\neq 0$ for some $(x,y)$, then we can deduce $-b/a>0$, thus $a$ and $b$ must have different sign. From the two equation above we can also have
$$
a^2u^2D_1u+abuvD_1v=0,b^2v^2D_1u-abuvD_1v=0\implies (a^2u^2+b^2v^2)D_1u=0
$$
thus $(a^2-ab)u^2D_1u=0$, since $ab<0$, we have $a^2-ab=a(a-b)\neq 0$, so $u^2D_1u=0$, we can similarly get $v^2D_1v=0$. But from $u^2D_1u=0$ we have $3u^2D_1u=0$ or $D_1[u^3]=0$, thus $u^3(x,y)$ is constant when $x$ moves for any $y$ such that $(x,y)\in D$, which means $u(x,y)$ is constant when $x$ changes, or $D_1u=0$, similarly we can have $D_1v=0$, so $f'=0$ and the proof is finished.
