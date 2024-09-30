# Exercise 17-23

### 2.17

Let $\mathbf{R}$ denote the set of real numbers and let $S$ denote the set of all real-valued functions whose domain is $\mathbf{R}$. Show that $S$ and $\mathbf{R}$ are not equinumerous.

#### Solution

Assume $S\thicksim\mathbf{R}$ and let $f$ be a one-to-one function such that $f(\mathbf{R})=S$, If $a\in\mathbf{R}$, let $g_a=f(a)$ be the real-valued function in $S$, define $h$ by $h(x)=1+g_x(x)$, since $h$ is real-valued and has domain $\mathbf{R}$, we shall have $h\in S$, but this means we can find $b\in\mathbf{R}$ s.t. $h=f(b)$, thus
$$
h=f(b)=g_b\implies g_b(x)=1+g_x(x)\implies g_b(b)=1+g_b(b)
$$
this is a contradiction.

### 2.18

Let $S$ be the collection of all sequences whose terms are the integers $0$ and $1$. Show that $S$ is uncountable.

#### Solution

Assume $S$ is countable, then we can write $S=\{s_1,s_2,\dots\}$, where each $s_i$ is a sequence whose terms are $0$ and $1$, we use $s_{ij}$ to denote the $j$th term in $s_i$. Now we construct a sequence as follows: the $j$th term of this sequence is $1$ if $s_{jj}=0$, or $0$ if $s_{jj}=1$, then this sequence is different from any $s_i$, thus it does not belong to $S$, but this sequence has terms only $0$ and $1$, thus it belongs to $S$, a contradiction.

### 2.19

Show that the following sets are countable:

a) the set of circles in the complex plane having rational radii and centers with rational coordinates,

b) any collection of disjoint intervals of positive length.

#### Solution

a) Let $S_q$ be the set of all circles with radius $q>0$ and centers with rational coordinates, then since the set of all points with rational coordinates is a subset of $\mathbf{Q}\times\mathbf{Q}$, which is countable, we see that $S_q$ is countable for each $q$, thus $\cup_{q\in\mathbf{Q},q>0}S_q$ is countable.

b) For any interval with positive length, we can find a rational number inside the interval, since for $a<b$ we can find $q\in\mathbf{Q}$ such that $a<q<b$. If there is a collection of disjoint intervals of positive length, then each interval can be assigned with a rational number, thus the total collection is at most countable.

### 2.20

Let $f$ be a real-valued function defined for every $x$ in the interval $0\leq x\leq 1$. Suppose there is a positive number $M$ having the following property: for every choice of a finite number of points $x_1,x_2,\dots,x_n$ in the interval $0\leq x\leq 1$, the sum
$$
|f(x_1)+\cdots+f(x_n)|\leq M.
$$
Let $S$ be the set of those $x$ in $0\leq x\leq 1$ for which $f(x)\neq 0$. Prove that $S$ is countable.

#### Proof

Let $S_n$ be the set $S_n=\{x\in[0,1]:f(x)>M/n\}$, then the elements in $S_n$ can be no more than $n$, otherwise we have a choice of $n+1$ points $x_1,\dots,x_{n+1}$ with $f(x_i)> M/n$, or
$$
|f(x_1)+\cdots+f(x_{n+1})|>(n+1)\dfrac{M}{n}>M
$$
thus each $S_n$ is finite, or at most countable, and thus $\cup_{n=1}^{\infty}S_n$ is countable.
Similarly, Define $T_n=\{x\in[0,1]:f(x)<-M/n\}$, we see that $\cup_{n=1}^{\infty}T_n$ is countable. Since
$$
S=\left(\bigcup_{n=1}^{\infty}S_n\right)\cup\left(\bigcup_{n=1}^{\infty}T_n\right)
$$
we see $S$ is countable.

### 2.21

Find the fallacy in the following "proof" that the set of all intervals of positive length is countable.

Let $\{x_1,x_2,\dots\}$ denote the countable set of rational numbers and let $I$ be any interval of positive length. Then $I$ contains infinitely many rational points $x_n$, but among these there will be one with *smallest index* $n$. Define a function $F$ by means of the equation $F(I)=n$, if $x_n$ is the rational number with smallest index in the interval $I$. This function establishes a one-to-one correspondence between the set of all intervals and a subset of the positive integers. Hence the set of all intervals is countable.

#### Solution

$F$ is not one-to-one, consider an interval $I$ which contains $x_1$, suppose $I$ has endpoints $a$ and $b$ with $a<b$, then the interval $I'$ with endpoints $a-1$ and $b+1$ also contains $x_1$, thus $F(I')=1$.

### 2.22

Let $S$ denote the collection of all subsets of a given set $T$. Let $f:S\to\mathbf{R}$ be a real-valued function defined on $S$. The function $f$ is called *additive* if $f(A\cup B)=f(A)+f(B)$ whenever $A$ and $B$ are disjoint subsets of $T$. If $f$ is additive, prove that for any two subsets $A$ and $B$ we have
$$f(A\cup B)=f(A)+f(B-A)\quad f(A\cup B)=f(A)+f(B)-f(A\cap B)$$

#### Proof

The first equation is easy since $A$ and $B-A$ are disjoint. To prove the second equation, notice that $(B-A)\cap(A\cap B)=\empty$ and $(B-A)\cup(A\cap B)=B$, thus $f(B)=f(B-A)+f(A\cap B)$.

### 2.23

Refer to Exercise 2.22. Assume $f$ is additive and assume also that the following relations hold for two particular subsets $A$ and $B$ of $T$:
$$
f(A\cup B)=f(A')+f(B')-f(A')f(B')
\\
f(A\cap B)=f(A)f(B),\quad f(A)+f(B)\neq f(T),
$$
where $A'=T-A,B'=T-B$. Prove that these relations determine $f(T)$, and compute the value of $f(T)$.

#### Solution

We let $a=f(A),b=f(B)$, notice that $f(A)+f(A')=f(T)$ we have $f(A')=f(T)-a$, similarly $f(B')=f(T)-b$. Use Exercise 2.22 we have
$$
f(A')+f(B')-f(A')f(B')=f(A)+f(B)-f(A)f(B)
$$
or, if we let $f(T)=M$, with $a+b\neq M$
$$
2M-a-b-(M-a)(M-b)=a+b-ab
$$
which gives $[M-(a+b)][M-2]=0$, thus $M=f(T)=2$.