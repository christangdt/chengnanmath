# Exercise 44-50 (Complex numbers III)

### 1.44

i) If $\theta$ and $a$ are real numbers, $-\pi<\theta\leq+\pi$, prove that
$$
(\cos\theta+i\sin\theta)^a=\cos(a\theta)+i\sin(a\theta).
$$
ii) Show that, in general, the restriction $-\pi<\theta\leq+\pi$ is necessary in (i) by taking $\theta=-\pi,a=1/2$.

iii) If $a$ is an integer, show that the formula in (i) holds without any restriction on $\theta$. In this case it is known as DeMoivre's theorem.

#### Solution

i) $\cos\theta+i\sin\theta=e^{i\theta}$, thus
$$
(\cos\theta+i\sin\theta)^a=(e^{i\theta})^a=e^{ia\theta}=\cos(a\theta)+i\sin(a\theta)
$$
ii) when $\theta=-\pi,a=1/2$, we have $(\cos\theta+i\sin\theta)^a=(-1)^{1/2}$, and $\cos(a\theta)+i\sin(a\theta)=-i$.

iii) Let $\theta'=\theta+2k\pi$, with $k$ being the appropriate integer such that $-\pi<\theta'\leq\pi$, then by (i) we have
$$
(\cos\theta+i\sin\theta)^a=(\cos\theta'+i\sin\theta')^a=\cos(a\theta')+i\sin(a\theta')
$$
notice $a\theta'=a(\theta+2k\pi)=a\theta+2ka\pi$, thus
$$
\cos(a\theta')=\cos(a\theta),\quad\sin(a\theta')=\sin(a\theta)
$$

### 1.45

Use DeMoivre's theorem to derive the trigonometric identities
$$
\sin3\theta=3\cos^2\theta\sin\theta-\sin^3\theta
\\
\cos3\theta=\cos^3\theta-3\cos\theta\sin^2\theta
$$
valid for real $\theta$. Are these valid when $\theta$ is complex?

#### Solution

DeMoivre's theorem tells $(\cos\theta+i\sin\theta)^3=\cos(3\theta)+i\sin(3\theta)$, which gives
$$
\cos^3\theta+3i\cos^2\theta\sin\theta-3\cos\theta\sin^2\theta-i\sin^3\theta=\cos(3\theta)+i\sin(3\theta)
$$
Since $\theta$ is real, both $\sin\theta$ and $\cos\theta$ is real, thus the equation equals to
$$
(\cos^3\theta-3\cos\theta\sin^2\theta,3\cos^2\theta\sin\theta-\sin^3\theta)=(\cos(3\theta),\sin(3\theta))
$$
and the conclusion holds.
When $\theta$ is complex, we use Definition 1.58 to get
$$
\cos(3\theta)=\dfrac{e^{3i\theta}+e^{-3i\theta}}{2},\quad\sin(3\theta)=\dfrac{e^{3i\theta}-e^{-3i\theta}}{2i}
$$
and
$$
\begin{aligned}
\cos^3\theta-3\cos\theta\sin^2\theta
&=\left(\dfrac{e^{i\theta}+e^{-i\theta}}{2}\right)^3-3\dfrac{(e^{i\theta}+e^{-i\theta})(e^{i\theta}-e^{-i\theta})^2}{8i^2}
\\&=\dfrac{e^{i\theta}+e^{-i\theta}}{8}\left((e^{i\theta}+e^{-i\theta})^2+3(e^{i\theta}-e^{-i\theta})^2\right)
\\&=\dfrac{e^{i\theta}+e^{-i\theta}}{8}\left(4e^{2i\theta}+4e^{-2i\theta}-4\right)
\\&=\dfrac{(e^{i\theta}+e^{-i\theta})(e^{2i\theta}+e^{-2i\theta}-1)}{2}=\dfrac{e^{3i\theta}+e^{-3i\theta}}{2}=\cos(3\theta)
\end{aligned}
$$
also we have (write $z=i\theta$)
$$
\begin{aligned}
3\cos^2\theta\sin\theta-\sin^3\theta&=3\dfrac{(e^z+e^{-z})^2}{4}\dfrac{e^z-e^{-z}}{2i}-\dfrac{(e^z-e^{-z})^3}{8i^3}
\\&=\dfrac{e^z-e^{-z}}{8i}\left(3(e^z+e^{-z})^2+(e^z-e^{-z})^2\right)
\\&=\dfrac{e^z-e^{-z}}{8i}\left(4e^z+4e^{-z}+4\right)=\dfrac{e^{3z}-e^{-3z}}{2i}=\sin(3\theta)
\end{aligned}
$$

### 1.46

Define $\tan{z}=(\sin{z})/(\cos{z})$ and show that for $z=x+iy$, we have
$$
\tan{z}=\dfrac{\sin2x+i\sinh2y}{\cos2x+\cosh2y}
$$

#### Solution

This can be showed by Theorem 1.59 and direct calculation. I ommit the details here.

### 1.47

Let $w$ be a given complex number. If $w\neq\pm 1$, show that there exist two values of $z=x+iy$ satisfying the conditions $\cos{z}=w$ and $-\pi<x\leq+\pi$. find these values when $w=i$ and when $w=2$.

#### Solution

Write $e^{iz}=a=e^{-y}(\cos{x}+i\sin{x})$, then $\cos{z}=w$ means $a+a^{-1}=2w$, or equivalently
$$
(a-w)^2=w^2-1
$$
Since $w\neq\pm 1$, $w^2-1$ has two different square roots in the complex field, thus $a$ has two values, so is $z$.
When $w=i$, solve $(a-i)^2=-2$ we see that $a=(1+\sqrt{2})i$ or $a=(1-\sqrt{2})i$, thus $(x,y)=(\pi/2,\log(\sqrt{2}-1))$ or $(x,y)=(-\pi/2,\log(\sqrt{2}+1))$.
When $w=2$, solve $(a-2)^2=3$ we see that $a=2+\sqrt{3}$ or $a=2-\sqrt{3}$, thus $(x,y)=(0,\log(2-\sqrt{3})$ or $(x,y)=(0,\log(2+\sqrt{3})$.

### 1.48

Prove Lagrange's identity for complex numbers:
$$
\left|\sum_{k=1}^na_kb_k\right|^2=\sum_{k=1}^n|a_k|^2\sum_{k=1}^n|b_k|^2-\sum_{1\leq k<j\leq n}|a_k\bar{b}_j-a_j\bar{b}_k|^2
$$

#### Proof

Use induction, with a similar process of Exercise 1.23.

### 1.49

a) By equating imaginary parts in DeMoivre's formula prove that
$$
\sin{n\theta}=\sin^n\theta\left\{\begin{pmatrix}n\\1\end{pmatrix} \cot^{n-1}\theta-\begin{pmatrix}n\\3\end{pmatrix}\cot^{n-3}\theta+\begin{pmatrix}n\\5\end{pmatrix}\cot^{n-5}\theta-\cdots\right\}
$$
b) If $0<\theta<\pi/2$, prove that
$$
\sin(2m+1)\theta=\sin^{2m+1}\theta{P_m}(\cot^2\theta)
$$
where $P_m$ is the polynomial of degree $m$ given by
$$
P_m(x)=\begin{pmatrix}2m+1\\1\end{pmatrix}x^m-\begin{pmatrix}2m+1\\3\end{pmatrix}x^{m-1}+\begin{pmatrix}2m+1\\5\end{pmatrix}x^{m-2}-\cdots
$$
Use this to show that $P_m$ has zeros at the $m$ distinct points $x_k=\cot^2\{\pi k/(2m+1)\}$ for $k=1,2,\dots,m$

c) Show that the sum of the zeros of $P_m$ is given by
$$
\sum_{k=1}^m\cot^2\dfrac{\pi k}{2m+1}=\dfrac{m(2m-1)}{3},
$$
and that the sum of their squares is given by
$$
\sum_{k=1}^m\cot^4\dfrac{\pi k}{2m+1}=\dfrac{m(2m-1)(4m^2+10m-9)}{45}.
$$

#### Solution

a) the DeMoivre's formula tells
$$
(\cos\theta+i\sin\theta)^n=\cos(n\theta)+i\sin(n\theta)
$$
for the left side, the imaginary part is
$$
i\begin{pmatrix}n\\1\end{pmatrix}\cos\theta\sin^{n-1}\theta+i^3\begin{pmatrix}n\\3\end{pmatrix}\cos^{3}\theta\sin^{n-3}\theta+i^5\begin{pmatrix}n\\5\end{pmatrix}\cos^{5}\theta\sin^{n-5}\theta+\cdots
$$
which equals to
$$
i\begin{pmatrix}n\\1\end{pmatrix}\dfrac{\cos\theta}{\sin\theta}\sin^{n}\theta-i\begin{pmatrix}n\\3\end{pmatrix}\dfrac{\cos^{3}\theta}{\sin^3\theta}\sin^{n}\theta+i\begin{pmatrix}n\\5\end{pmatrix}\dfrac{\cos^{5}\theta}{\sin^5\theta}\sin^{n}\theta+\cdots
$$
which proves the result.
b) let $n=2m+1$ in (a), we get
$$
\begin{aligned}
&\quad\sin(2m+1)\theta
\\&=\sin^{2m+1}\theta\left\{\begin{pmatrix}2m+1\\1\end{pmatrix} \cot^{2m+1-1}\theta-\begin{pmatrix}2m+1\\3\end{pmatrix}\cot^{2m+1-3}\theta+\begin{pmatrix}2m+1\\5\end{pmatrix}\cot^{2m+1-5}\theta-\cdots\right\}
\\&=\sin^{2m+1}\theta\left\{\begin{pmatrix}2m+1\\1\end{pmatrix} \cot^{2m}\theta-\begin{pmatrix}2m+1\\3\end{pmatrix}\cot^{2(m-1)}\theta+\begin{pmatrix}2m+1\\5\end{pmatrix}\cot^{2(m-2)}\theta-\cdots\right\}
\\&=\sin^{2m+1}\theta{P_m}(\cot^2\theta)
\end{aligned}
$$
and when $\alpha_k=\pi k/(2m+1)$ for $k=1,2,\dots,m$, we have $0<\alpha_k<\pi/2$ and $\sin\alpha_k>0$ for all $k=1,2,\dots,n$ , so
$$
\sin^{2m+1}\alpha_k P_m(\cot^2\alpha_k)=\sin(\pi k)=0\Rightarrow P_m(\cot^2\alpha_k)=0
$$
c) Denote the zero points of $P_m(x)$ with $x_1,\dots,x_m$, then
$$
P_m(x)=a(x-x_1)\cdots(x-x_m),\quad a=\begin{pmatrix}2m+1\\1\end{pmatrix}
$$
by comparing the coefficient of $x^{m-1}$, we have
$$
-a\sum_{k=1}^mx_k=-\begin{pmatrix}2m+1\\3\end{pmatrix}\Rightarrow\sum_{k=1}^mx_k=\dfrac{\begin{pmatrix}2m+1\\3\end{pmatrix}}{\begin{pmatrix}2m+1\\1\end{pmatrix}}=\dfrac{(2m)!}{3!(2m-2)!}=\dfrac{m(2m-1)}{3}
$$
To calculate $\sum_{k=1}^nx_k^2$, use the equality
$$
\sum_{k=1}^nx_k^2=\left(\sum_{k=1}^nx_k\right)^2-2\sum_{1\leq i<j\leq n}x_ix_j
$$
and the fact that the coefficient of $x^{m-2}$ in $P_m(x)/a$ is $\sum_{1\leq i<j\leq n}x_ix_j$, we have
$$
\begin{aligned}
\sum_{k=1}^nx_k^2&=\left(\dfrac{m(2m-1)}{3}\right)^2-2\dfrac{\begin{pmatrix}2m+1\\5\end{pmatrix}}{a}=\dfrac{m^2(2m-1)^2}{9}-2\dfrac{(2m)!}{5!(2m-4)!}
\\&=\dfrac{m^2(2m-1)^2}{9}-\dfrac{(m)(2m-1)(m-1)(2m-3)}{15}
\\&=\dfrac{m(2m-1)}{45}(5m(2m-1)-3(m-1)(2m-3))
\\&=\dfrac{m(2m-1)}{45}(10m^2-5m-(6m^2-15m+9))
\\&=\dfrac{m(2m-1)}{45}(4m^2+10m-9)
\end{aligned}
$$


### 1.50

Prove that $z^n-1=\prod_{k=1}^n(z-e^{2\pi ik/n})$ for all complex $z$. Use this to derive the formula
$$
\prod_{k=1}^{n-1}\sin\dfrac{k\pi}{n}=\dfrac{n}{2^{n-1}}\quad\text{for }n\geq 2.
$$

#### Proof

By Theorem 1.51 we know there are exactly $n$ distinct complex numbers $z_0,z_1,\dots,z_{n-1}$ such that $z_k^n=1$, thus
$$
z^n-1=\prod_{k=0}^{n-1}(z-z_k),\quad z_k=\exp\left(i\dfrac{\arg(1)}{n}+\dfrac{2\pi ik}{n}\right)
$$
Since $\arg(1)=0$ and $e^{2\pi i}=\cos(2\pi)+i\sin(2\pi)=1=e^0$, we have
$$
z^n-1=\prod_{k=0}^{n-1}(z-e^{2\pi ik/n})=\prod_{k=1}^{n}(z-e^{2\pi ik/n})
$$
From this equality we can get
$$
z^{n-1}+\cdots+1=\prod_{k=1}^{n-1}(z-e^{2\pi ik/n})
$$
let $z=1$ we can get the formula.