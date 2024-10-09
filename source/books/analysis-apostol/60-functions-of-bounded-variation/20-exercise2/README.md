# Exercise 8-10 (Curves)

### 6.8

Let $f$ and $g$ be complex-valued functions defined as follows:
$$
f(t)=e^{2\pi it}\quad\text{if }t\in[0,1],\quad g(t)=e^{2\pi it}\quad\text{if }t\in[0,2]
$$
a) Prove that $f$ and $g$ have the same graph but are not equivalent according to the definition in Section 6.12.

b) Prove that the length of $g$ is twice that of $f$.

#### Proof

(a) Let $S_f$ be the graph of $f$ and $S_g$ be the graph of $g$, since $f(t)=g(t)$ for $t\in[0,1]$, we see $S_f\subseteq S_g$, also $g(t-1)=f(t)$ for $t\in[1,2]$, thus $S_g\subseteq S_f$ and so $S_g=S_f$. To see they are not equivalent, assume $u:[0,2]\to[0,1]$ is continuous and strictly monotonic and $g=f\circ u$ on $[0,2]$, then $g(t)=f(u(t))$ means $e^{2\pi it}=e^{2\pi iu(t)}$ for any $t\in[0,2]$, so
$$
e^{2\pi iu(0)}=e^{2\pi iu(1)}=e^{2\pi iu(2)}=1
$$
with $u(0),u(1),u(2)\in[0,1]$ and either $u(0)<u(1)<u(2)$ or $u(0)>u(1)>u(2)$, but if $t\in[0,1]$, the only possible values to make $e^{2\pi it}=1$ are $t=0$ or $t=1$, so we get a contradiction. Thus no such $u$ can exist.



(b) Let $P=\{t_0,t_1,\dots,t_m\}\in\mathscr{P}[0,1]$, let $t_{m+i}=1+t_i$ for $i=1,\dots,m$, then the partition $P':=\{t_0,t_1,\dots,t_{2m}\}\in\mathscr{P}[0,2]$, and it is easy to see
$$
\begin{aligned}2\Lambda_f(P)&=2\sum_{k=1}^n|f(t_k)-f(t_{k-1})|\\&=\sum_{k=1}^n|g(t_k)-g(t_{k-1})|+\sum_{k=1}^n|g(t_{m+k})-g(t_{m+k-1})|
\\&=\sum_{k=1}^{2n}|g(t_k)-g(t_{k-1})|=\Lambda_g(P')
\end{aligned}
$$
Thus we have $2\Lambda_f(P)\le\Lambda_g(0,2)$ for all $P$ and $2\Lambda_f(0,1)\le\Lambda_g(0,2)$. Conversely, let $P=\{t_0,t_1,\dots,t_m\}\in\mathscr{P}[0,2]$, add $1$ if the point $1$ is not in $P$, then $P\cup\{1\}$ can be split into two partitions $P_1\in\mathscr{P}[0,1]$ and $P_2\in\mathscr{P}[1,2]$, let $P_2'=\{x-1:x\in P_2\}$, then $P_2'\in\mathscr{P}[0,1]$, and
$$
\Lambda_g(P)\le\Lambda_g(P\cup\{1\})=\Lambda_g(P_1)+\Lambda_g(P_2)=\Lambda_f(P_1)+\Lambda_f(P_2')\le2\Lambda_f(0,1)
$$
so we have $\Lambda_g(0,2)\le2\Lambda_f(0,1)$. In conclusion we get $\Lambda_g(0,2)=2\Lambda_f(0,1)$.

### 6.9

Let $f$ be a rectifiable path of length $L$ defined on $[a,b]$, and assume that $f$ is not constant on any subinterval of $[a,b]$. Let $s$ denote the arc-length function given by $s(x)=\Lambda_{\mathbf{f}}(a,x)$ if $a<x\le b$, $s(a)=0$.

a) Prove that $s^{-1}$ exists and is continuous on $[0,L]$.

b) Define $\mathbf{g}(t)=\mathbf{f}[s^{-1}(t)]$ if $t\in[0,L]$ and show that $g$ is equivalent to $\mathbf{f}$. Since $\mathbf{f}(t)=\mathbf{g}[s(t)]$, the function $\mathbf{g}$ is said to provide a representation of the graph of $\mathbf{f}$ with arc length as parameter.

#### Solution

(a) Theorem 6.19 shows that $s$ is strictly monotonic and continuous on $[a,b]$, which is a compact interval, use Theorem 4.29 we see $s^{-1}$ exists and is continuous.



(b) From $\mathbf{g}(t)=\mathbf{f}[s^{-1}(t)]$ we see that
$$
\mathbf{g}(s(t))=\mathbf{f}[s^{-1}(s(t))]=\mathbf{f}(t),\quad t\in[0,L]
$$
so $s:[a,b]\to[0,L]$ is a continuous and strictly monotonic function which makes $\mathbf{f}=\mathbf{g}\circ s$, and the equivalence relation holds.

### 6.10

Let $f$ and $g$ be two real-valued continuous functions of bounded variation defined on $[a,b]$, with $0<f(x)<g(x)$ for each $x\in(a,b)$, $f(a)=g(a),f(b)=g(b)$. Let $h$ be the complex-valued function defined on the interval $[a,2b-a]$ as follows:
$$
\begin{aligned}
&h(t)=t+if(t),\quad&&\text{if }a\le t\le b,
\\
&h(t)=2b-t+ig(2b-t),\quad&&\text{if }b\le t\le 2b-a.
\end{aligned}
$$
a) Show that $h$ describes a rectifiable curve $\Gamma$.

b) Explain, by means of a sketch, the geometric relationship between $f$, $g$, and $h$.

c) Show that the set of points
$$
S=\{(x,y):a\le x\le b,\quad f(x)\le y\le g(x)\}
$$
is a region in $\mathbf{R}^2$ whose boundary is the curve $\Gamma$.

d) Let $H$ be the complex-valued function defined on $[a,2b-a]$ as follows:
$$
\begin{aligned}
&H(t)=t-\frac{1}{2}i[g(t)-f(t)],\quad&&\text{if }a\le t\le b,
\\
&H(t)=t+\frac{1}{2}i[g(2b-t)-f(2b-t)],\quad&&\text{if }b\le t\le 2b-a.
\end{aligned}
$$
Show that $H$ describes a rectifiable curve $\Gamma_0$ which is the boundary of the region
$$
S_0=\{(x,y):a\le x\le b,\quad f(x)-g(x)\le 2y\le g(x)-f(x)\}
$$
e) Show that $S_0$ has the $x$-axis as a line of symmetry. (The region $S_0$ is called the *symmetrization* of $S$ with respect to the $x$ -axis.)

f) Show that the length of $\Gamma_0$ does not exceed the length of $\Gamma$. 

#### Solution

(a) Let $P\in\mathscr{P}[a,2b-a]$, then $P\cup\{b\}=P_1\cup P_2$ where $P_1\in\mathscr{P}[a,b]$ and $P_2\in\mathscr{P}[b,2b-a]$, denote $P_1=\{t_0,t_1,\dots,t_m\}$ and $P_2=\{s_0,s_1,\dots,s_n\}$, then
$$
\Lambda_h(P)\le\Lambda_h(P_1)+\Lambda_h(P_2)=\sum_{k=1}^m\|h(t_k)-h(t_{k-1})\|+\sum_{j=1}^n\|h(s_j)-h(s_{j-1})\|
$$
and we have
$$
\sum_{k=1}^m\|h(t_k)-h(t_{k-1})\|\le\sum_{k=1}^m(|t_k-t_{k-1}|+|f(t_k)-f(t_{k-1})|)\le(b-a)+V_f(a,b)
\\
\begin{aligned}\sum_{j=1}^n\|h(s_j)-h(s_{j-1})\|&\le\sum_{j=1}^n(|t_k-t_{k-1}|+|g(2b-t_k)-g(2b-t_{k-1})|)\\&\le(b-a)+V_g(a,b)
\end{aligned}
$$
so $\Lambda_h(P)\le2(b-a)+V_f(a,b)+V_g(a,b)$, since $f$ and $g$ are of bounded variation, we see that $\Lambda_h(P)$ is bounded above for any $P\in\mathscr{P}[a,2b-a]$.

(b) Geometrically, if we draw the graph of $f$ and $g$ in $\mathbf{R}^2$, since $f(a)=g(a)$ and $f(b)=g(b)$, their graphs form a closed region, which coincide with the graph of $h$ in the complex plane.

(c) From (b) we can see this is true.

(d)-(f) The definition of $H(t)$ seems to be wrong, since the graph of $H$ cannot form a closed region.