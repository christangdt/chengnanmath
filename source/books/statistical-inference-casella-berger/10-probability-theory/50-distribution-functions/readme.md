# Distribution Functions

## Content Notes

#### Definition 1.5.1

The *cumulative distribution function* or *cdf* of a random variable $X$, denoted by $F_X(x)$ is defined by
$$
F_X(x)=P_X(X\le x),\quad\forall x
$$

#### Theorem 1.5.3

The function $F(x)$ is a cdf if and only if the following three conditions hold:

- a. $\lim_{x\to-\infty}F(x)=0$ and $\lim_{x\to\infty}F(x)=1$.
- b. $F(x)$ is a nondecreasing function of $x$.
- c. $F(x)$ is right-continuous; that is $\lim_{x\downarrow x_0}F(x)=F(x_0)$ for all $x_0$.

#### Example 1.5.4 (Tossing for a head)

Toss a coin until a head appears. Let $p=$ probability of a head on any given toss, define $X=$ number of tosses required to get a head. Then
$$
P(X=x)=(1-p)^{x-1}p,\quad x=1,2,\dots
$$
which means for any positive integer $x$,
$$
P(X\le x)=\sum_{i=1}^xP(X=i)=\sum_{i=1}^x(1-p)^{i-1}p
$$
The partial sum of the geometric series is
$$
\sum_{k=1}^nt^{k-1}=\dfrac{1-t^n}{1-t},\quad t\ne1
$$
thus
$$
F_X(x)=P(X\le x)=\dfrac{1-(1-p)^x}{1-(1-p)}p=1-(1-p)^x,\quad x=1,2,\dots
$$
$F_X(x)$ is the cdf of the *geometric distribution*.

#### Example 1.5.5 (Continuous cdf)

The cdf of the *logistic distribution* is given by
$$
F_X(x)=\dfrac{1}{1+e^{-x}}
$$

#### Example 1.5.6 (Cdf with jumps)

Modify $F_X(x)$ of (1.5.5) to be: for $0<\epsilon<1$,
$$
F_Y(y)=\begin{cases}
\dfrac{1-\epsilon}{1+e^{-y}},& y<0
\\
\epsilon+\dfrac{1-\epsilon}{1+e^{-y}},& y\ge0
\end{cases}
$$
Then $F_Y$ has a jump of height $\epsilon$ at $y=0$ and otherwise is continuous.

#### Definition 1.5.7

A random variable $X$ is *continuous* if $F_X(x)$ is a continuous function of $x$. A random variable $X$ is *discrete* if $F_X(x)$ is a step function of $x$.

#### Definition 1.5.8

The random variables $X$ and $Y$ are *identically distributed* if for every set $A\in\mathcal{B}^1$, $P(X\in A)=P(Y\in A)$, in which $\mathcal{B}^1$ is the smallest sigma algebra containing all the intervals of real numbers of the form $(a,b),(a,b],[a,b)$ and $[a,b]$.

#### Theorem 1.5.10

The random variables $X$ and $Y$ are identically distributed if and only if $F_X(x)=F_Y(x)$ for every $x$.

## Exercises

#### 1.47

From (a) to (e), just verify the three conditions of Theorem 1.5.3. We prove (e) as an example.

For condition a, notice as $y\to-\infty$ and $y\to\infty$, the function $F_Y(y)$ has different expressions.
$$
\lim_{y\to-\infty}F_Y(y)=\lim_{y\to-\infty}\frac{1-\epsilon}{1+e^{-y}}=0
\\
\lim_{y\to\infty}F_Y(y)=\epsilon+\lim_{y\to\infty}\dfrac{1-\epsilon}{1+e^{-y}}=\epsilon+1-\epsilon=1
$$
For condition b, we have
$$
[F_Y(y)]'=
\dfrac{e^{-y}(1-\epsilon)}{1+e^{-y}}>0,\quad\forall y\in(-\infty,\infty)
$$
For condition c, $F_Y$ is continuous on $(-\infty,0)$ and $[0,\infty)$ separately, thus it is right-continuous.

#### 1.48

Let $\mathcal{X}$ be the range of $X$, as $x\to-\infty$, it will eventually fall out of the minima of $\mathcal{X}$, so
$$
P_X(X\le x)=P(\{s\in S:X(s)\in(-\infty,x]\})=P(\empty)=0,\quad x\to-\infty
$$
similarly, we have
$$
P_X(X\le x)=P(\{s\in S:X(s)\in(-\infty,x]\})=P(S)=0,\quad x\to\infty
$$
this proves condition a. For $x_1\le x_2$, we have
$$
\{s\in S:X(s)\in(-\infty,x_1]\}\subset\{s\in S:X(s)\in(-\infty,x_2]\}
$$
so we have
$$
\begin{aligned}
F_X(x_1)&=P_X(X\le x_1)=P(\{s\in S:X(s)\in(-\infty,x_1]\})
\\&\le P(\{s\in S:X(s)\in(-\infty,x_2]\})=P_X(X\le x_2)=F_X(x_2)

\end{aligned}
$$
which proves condition b. For c, notice that for $x>x_0$, we can write
$$
\{s\in S:X(s)\in(-\infty,x]\}=\{s\in S:X(s)\in(-\infty,x_0]\}\cup\{s\in S:X(s)\in(x_0,x]\}
$$
and the two sets on the right are disjoint, thus we get
$$
F_X(x)=F_X(x_0)+P(\{s\in S:X(s)\in(x_0,x]\})
$$
as $x\downarrow x_0$, the set $\{s\in S:X(s)\in(x_0,x]\}$ tends to become $\empty$, and the conclusion follows.

#### 1.49

Since we have $P(X\le t)\le P(Y\le t)$ for all $t$, we have
$$
1-P(X\le t)\ge 1-P(Y\le t)\quad\forall t\implies P(X>t)\ge P(Y>t),\quad\forall t
$$
similarly we can prove $P(X>t)> P(Y>t)$ for some $t$.

#### 1.50

Prove by induction. When $n=1$, we have $\sum_{k=1}^nt^{k-1}=t^0=1=\dfrac{1-t^1}{1-t}$. Suppose the expression is valid for $n$, then
$$
\sum_{k=1}^{n+1}t^{k-1}=t^n+\sum_{k=1}^nt^{k-1}=t^n+\dfrac{1-t^n}{1-t}=\dfrac{1-t^{n+1}}{1-t}
$$

