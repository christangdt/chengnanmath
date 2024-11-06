# Density and Mass Functions

## Content Notes

#### Definition 1.6.1

The *probability mass function (pmf)* of a discrete random variable $X$ is given by
$$
f_X(x)=P(X=x)\quad\text{for all }x.
$$

#### Definition 1.6.3

The *probability density function* or *pdf*, $f_X(x)$, of a continuous random variable $X$ is the function that satisfies
$$
F_X(x)=\int_{-\infty}^xf_X(t)dt\quad\text{for all }x.
$$

#### A note on notation

"$X$ has a distribution given by $F_X(x)$" is abbreviated symbolically by "$X\sim F_X(x)$".

#### Example 1.6.4 (Logistic probabilities)

The logistic distribution has
$$
F_X(x)=\dfrac{1}{1+e^{-x}},\quad f_X(x)=\dfrac{d}{dx}F_X(x)=\dfrac{e^{-x}}{(1+e^{-x})^2}
$$
which gives
$$
P(a<X<b)=F_X(b)-F_X(a)=\int_a^bf_X(x)dx
$$

#### Theorem 1.6.5

A function $f_X(x)$ is a pdf (or pmf) of a random variable $X$ if and only if

- a. $f_X(x)\ge0$ for all $x$.
- b. $\sum_x f_X(x)=1$ (pmf) or $\int_{-\infty}^{\infty}f_X(x)dx=1$ (pdf).

## Exercises

#### 1.51

We have
$$
f_X(i)=P(X=i)=\dfrac{\binom{5}{i}\binom{25}{4-i}}{\binom{30}{4}},\quad i=0,1,2,3,4
$$
the cdf is a step-up jump function, with jumps at $x=0,1,2,3,4$.

#### 1.52

If $F(x_0)<1$, then $g(x)>0$ for all $x$, and
$$
\int_{-\infty}^{\infty}g(x)dx=\int_{x_0}^{\infty}\dfrac{f(x)}{1-F(x_0)}dx=\lim_{x\to\infty}\dfrac{F(x)-F(x_0)}{1-F(x_0)}=1
$$
since $F(x)$ is a cdf and $\lim_{x\to\infty} F(x)=1$. By Theorem 1.6.5, $g$ is a pdf.

#### 1.53

(a) $F_Y(y)$ is continuous and $0\le F_Y(y)\le 1$, we can easily verify $\lim_{y\to-\infty}F_Y(y)=0$ and $\lim_{y\to\infty}F_Y(y)=1$. Since $\frac{d}{dy}F_Y(y)=2/y^3>0$ for $1\le y<\infty$, $F$ is nondecreasing of $y$. Also $F_Y(y)$ is continuous on its domain. By Theorem 1.5.3, $F_Y(y)$ is a cdf.

(b) We have
$$
f_Y(y)=\begin{cases}
0,&y<1
\\
\dfrac{2}{y^3},&y\ge1
\end{cases}
$$
(c) By definition, $F_Z(z)=P(Z\le z)$, thus
$$
F_Z(z)=P(10Y-10\le z)=P(Y\le1+z/10)=1-\dfrac{1}{(1+z/10)^2},\quad 0\le z<\infty
$$

#### 1.54

(a) Since
$$
1=\int_0^{\pi/2}c\sin{x}dx=c
$$
(b) We have
$$
\begin{aligned}
1=\int_{-\infty}^{\infty}f(x)dx&=\int_{-\infty}^0ce^{-|x|}dx+\int_0^{\infty}ce^{-|x|}dx=\int_{-\infty}^0ce^{x}dx+\int_0^{\infty}ce^{-x}dx
\\&=ce^0+ce^0=2c\implies c=\dfrac{1}{2}
\end{aligned}
$$

#### 1.55

$V$ cannot be less than 5, and
$$
P(V=5)=P(0<T\le3)=\int_0^3f_T(t)dt=\int_0^3\dfrac{e^{-t/1.5}}{1.5}dt=1-1/e^2
$$
If $T>3$, then $V=2T>6$, and when $v>6$, we have
$$
P(V\le v)=P(T\le v/2)=\int_0^{v/2}f_T(t)dt=1-\dfrac{1}{e^{v/3}}
$$
so
$$
F_V(v)=\begin{cases}
0,&v<5
\\
1-e^{-2},&5\le v<6
\\
1-e^{-v/3},&6\le v<\infty
\end{cases}
$$
