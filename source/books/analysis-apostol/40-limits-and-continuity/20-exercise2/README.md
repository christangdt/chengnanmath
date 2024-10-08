# Exercise 10-12 (Limits of functions)

NOTE. In Exercises 4.10 through 4.28, all functions are real-valued.

### 4.10

Let $f$ be defined on an open interval $(a,b)$ and assume $x\in(a,b)$.  Consider the two statements:
$$
(a)\lim_{h\to 0}|f(x+h)-f(x)|=0;\quad(b)\lim_{h\to 0}|f(x+h)-f(x-h)|=0
$$
Prove that (a) always implies (b), and give an example in which (b) holds but (a) does not.

#### Proof

For $\forall\varepsilon>0$, there exists $\delta>0$ such that $|f(x+h)-f(x)|<\varepsilon/2$ for $|h|<\delta$, thus
$$
|f(x+h)-f(x-h)|\leq|f(x+h)-f(x)|+|f(x-h)-f(x)|<{\varepsilon}
$$
for every $h$ which satisfies $|h|<\delta$.

Let $f(x)=0$ if $x\neq 0$ and $f(0)=1$, then $\lim_{h\to 0}|f(h)-f(-h)|=0$ but
$$
\lim_{h\to 0}|f(0+h)-f(0)|=1
$$

### 4.11

Let $f$ be defined on $\mathbf{R}^2$. If
$$
\lim_{(x,y)\to(a,b)}f(x,y)=L
$$
and if the one-dimensional limits $\lim_{x\to a}f(x,y)$ and $\lim_{y\to b}f(x,y)$ both exists, prove that
$$
\lim_{x\to a}[\lim_{y\to b}f(x,y)]=\lim_{y\to b}[\lim_{x\to a}f(x,y)]=L
$$

#### Proof

Let $\lim_{x\to a}f(x,y)=A(y)$ and $\lim_{y\to b}f(x,y)=B(x)$, for $\forall\varepsilon>0$, first there is a $\delta_1>0$ such that
$$
|f(x,y)-L|<\dfrac{\varepsilon}{2}\quad\text{whenever }|(x,y)-(a,b)|<\delta_1
$$
and there is a $0<\delta_2<\delta_1$ such that
$$
|f(x,y)-A(y)|<\dfrac{\varepsilon}{2},\forall{y}\quad\text{whenever }|x-a|<\delta_2
$$
let $\delta=\delta_1-\delta_2$, then if $|y-b|<\delta$, we can have
$$
|(x,y)-(a,b)|\leq |x-a|+|y-b|<\delta_2+\delta=\delta_1
$$
thus as long as $x$ is close enough to $a$, we have
$$
|A(y)-L|\leq|f(x,y)-A(y)|+|f(x,y)-L|<\varepsilon,\quad\text{whenever }|y-b|<\delta
$$
this means $\lim_{y\to b}A(y)=L$, similarly we can prove $\lim_{x\to a}B(x)=L$.

### 4.12

If $x\in[0,1]$ prove the following limit exists,
$$
\lim_{m\to\infty}[\lim_{n\to\infty}\cos^{2n}(m!\pi x)],
$$
and that its value is $0$ or $1$, according to whether $x$ is rational or irrational.

#### Proof

If $x$ is irrational, then $m!x$ cannot be an integer, thus $|\cos(m!\pi x)|<1$ for any possible choices of $m$, thus $\lim_{n\to\infty}\cos^{2n}(m!\pi x)=0$ and the limit we seek is $0$.

If $x$ is rational, say $x=p/q$ with $p,q>0$ and $p,q$ have no common factors, then
$$
|\cos(m!\pi x)|\begin{cases}
=1,\quad m\geq q
\\
<1,\quad m<q
\end{cases}
$$
thus when $m\geq q$, the limit has value $1$, when $m<q$, the limit has value $0$.