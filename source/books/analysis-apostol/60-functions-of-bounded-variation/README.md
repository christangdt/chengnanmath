# Functions of Bounded Variation and Rectifiable Curves

本章的内容在其他数学分析书中很少见，常见于实变函数论等本科高阶课程，有界变差函数是与单调函数联系紧密的一类函数，也与有限弧长的曲线（可求长曲线rectifiable curves）联系紧密。

## 有界变差函数

### 单调函数的性质

定理6.1说明在$[a,b]$上单调的函数，若在其中选择若干个点，则$f$在每个点的跳跃累加起来，不会超过$f$在$[a,b]$上的跨度。因此有定理6.2：单调函数在$[a,b]$上的不连续点是可数的，证明用了一个分析中非常常见的技巧，即将不连续点变成$\bigcup_1^{\infty}S_n$，每个$S_n$是jump大于1/n的点。

### 有界变差函数

定义6.3提前引入了分割partition的概念，一般在黎曼积分的时候才会引入。定义6.4是有界变差函数的定义，对任一分割$P=\{x_0,x_1,\dots,x_n\}$定义$\Delta f_k=f(x_k)-f(x_{k-1})$， 如果$\sum_{k=1}^n|\Delta f_k|$是有上界的，那么$f$就是有界变差函数。后续两个定理是有界变差函数的实例。定理6.5说明单调函数是有界变差，定理6.6说明导函数有界的函数是有界变差。定理6.7是有界变差函数的性质，有界变差函数一定是有界函数，且能够被边界点函数值和变差的上限框住，即如果有$\sum|\Delta f_k|\le M$，那么对$x\in[a,b]$成立$|f(x)|\le|f(a)|+M$。

一个不是有界变差的函数例子是$f(x)=x\cos(\frac{\pi}{2x}),x\in[0,1]$，通过取
$$
P=\left\{0,\dfrac{1}{2n},\dfrac{1}{2n-1},\dots,\dfrac{1}{3},\dfrac{1}{2},1\right\}
$$
可以使得$\sum_{k=1}^{2n}|\Delta f_k|=1+\frac{1}{2}+\cdots+\frac{1}{n}$，因此不是有界的，但是$f$在任何$[a,1],0<a<1$上是有界变差的。

另一个比较类似的例子是$f(x)=x^2\cos(1/x),x\neq 0,f(0)=0$。这个函数是有界变差的，因为$f'$是有界的。但$f'$有界是充分非必要条件，例如$f(x)=x^{1/3}$的导函数在$x\to0$时是无穷的，但是该函数是单调的，因此在任何有限区间上都是有界变差。

### 全变差

根据定义6.8，全变差$V_f(a,b)$是有界变差函数$f$的变分和$\sum_{k=1}^n|\Delta f_k|$在选遍所有分割$P$后可能达到的最大值。$V_f(a,b)$是介于$[0,+\infty)$的一个数，且$V_f(a,b)=0$等价于$f$是常数函数。

定理6.9说明如果$f,g$都是有界变差函数，那么$f+g,f-g,fg$都是有界变差函数，且全变差有关系$V_{f\pm g}\le V_f+V_g$和$V_{f\cdot g}\le AV_f+BV_g$， 其中$A=\sup|g(x)|,B=\sup|f(x)|$。

定理6.9并没有包括两个有界变差函数的商，因为一个有界变差函数的倒数可能不是有界变差的，例如趋于0的函数。但是可以讨论bounded away from 0的函数，即在$x\in[a,b]$时有$0<m\le|f(x)|$的函数，定理6.10说明对这样的有界变差函数$f$，其倒数函数$g=1/f$还是有界变差的，且有$V_g\le V_f/m^2$。

### 全变差的可加性

之前的讨论中，自变量的取值区间$[a,b]$都是固定的，而把全变差$V_f(a,b)$视作关于$f$的函数。如果反之，将$f$固定，研究自变量区间的变化，则会有定理6.11：对$[a,b]$上有界变差的函数$f$, 取$c\in(a,b)$，则$f$在$[a,c]$上和$[c,b]$上都是有界变差函数，并且$V_f(a,b)=V_f(a,c)+V_f(c,b)$。

### 在$[a,x]$上的全变差视作$x$的函数

继续将全变差作为区间的变化函数，此时固定左端点，将右端点作为自变量，则形成一种新的函数$V(x)=V_f(a,x),x\in(a,b],V(a)=0$。定理6.12证明，这个新函数在$[a,b]$上是单调增函数，同时$V-f$也在$[a,b]$上是单调增函数。

### 将有界变差函数表示成单增函数的差分

基于定理6.12，能够得到定理6.13，即$f$是有界变差函数的充要条件是$f$能够被表示为两个单调递增函数之差。这里单调递增可以被替换为严格单调递增。

### 连续有界变差函数

定理6.14：有界变差函数$f$的连续点和$V=V_f(a,x)$的连续点相同。定理6.14和定理6.13共同推出定理6.15：在$[a,b]$上连续的函数$f$是有界变差的充要条件是$f$能够被表示为两个连续单调递增函数之差。这里单调递增可以被替换为严格单调递增。

## 可求长曲线

### 曲线和路径

对于一个连续的向量值函数$\mathbf{f}:[a,b]\to\mathbf{R}^n$，当$t$从$a$变到$b$时，函数值$\mathbf{f}(t)$划出的点集被称为$\mathbf{f}$的graph或者curve，函数$\mathbf{f}$自身被称为path

### 可求长曲线与弧长

求曲线长度的思想是用多边形来逼近弧长，并将多边形的总长度的最小上界作为弧长的长度。但实际上，存在有多边形总长度但是这个总长度没有上界的弧，因此曲线需要分为能够利用上述方式求弧长的曲线和不能利用上述方式求弧长的曲线，前者称为可求长曲线rectifiable。

正式地，对$\mathbf{R}^n$中的一个path: $\mathbf{f}:[a,b]\to\mathbf{R}^n$, 给定$[a,b]$中的一个分割$P=\{t_0,t_1,\dots,t_m\}$，我们得到多边形的一系列端点$\mathbf{f}(t_0),\mathbf{f}(t_1),\dots,\mathbf{f}(t_m)$， 这个多边形的周长记为$\Lambda_{\mathbf{f}}(P)$， 计算方式是$\Lambda_{\mathbf{f}}(P)=\sum_{k=1}^n\|\mathbf{f}(t_k)-\mathbf{f}(t_{k-1})\|$。

定义6.16为，如果$\Lambda_{\mathbf{f}}(P)$对于所有$[a,b]$的分割$P$都是有上界的，那么path $\mathbf{f}$被称为可求长的rectifiable，且其弧长arc length定义为$\Lambda_{\mathbf{f}}(a,b)=\sup\{\Lambda_{\mathbf{f}}(P):P\in\mathscr{P}[a,b]\}$。如果$\Lambda_{\mathbf{f}}(P)$不是有界的，那么$\mathbf{f}$记为不可求长的nonrectifiable。

定理6.17将rectifiable与有界变差联系起来。path $\mathbf{f}=(f_1,\dots,f_n)$可求长的充要条件是每个分量函数$f_k$均是有界变差的。且对于可求长的$\mathbf{f}$我们有
$$
V_k(a,b)\le\Lambda_{\mathbf{f}}(a,b)\le V_1(a,b)+\cdots+V_n(a,b),\quad(k=1,\dots,n)
$$
其中$V_k(a,b)$是$f_k$在$[a,b]$上的全变差。

### 弧长的可加性和连续性

与有界变差的研究类似，固定一个path $\mathbf{f}$， 研究其作为区间$[x,y]\subseteq[a,b]$的函数。

定理6.18：如果$c\in(a,b)$，那么$\Lambda_{\mathbf{f}}(a,b)=\Lambda_{\mathbf{f}}(a,c)+\Lambda_{\mathbf{f}}(c,b)$。

定理6.19：对于一个可求长的path $\mathbf{f}$以及$x\in(a,b]$， 定义$s(x)=\Lambda_{\mathbf{f}}(a,x)$和$s(a)=0$，则$s$是一个连续单调增函数；进一步地，如果$\mathbf{f}$在任何子区间上都不是constant的，那么$s$是严格单增函数。

### 路径的等价性和换元

不同的路径可以有相同的曲线，特别是对于一个$\mathbf{f}:[a,b]\to\mathbf{R}^n$，如果有连续严格单调函数$u:[c.d]\to[a.b]$，那么新的path $\mathbf{g}=\mathbf{f}\circ u$与原来的path有相同的graph，可以把它们称为等价的equivalent。函数$u$定义了一个换元change of parameter。定理6.20说明两个path是等价的当且仅当他们有相同的graph。

## 绝对连续函数

本章最后一部分习题是绝对连续函数的定义和一些性质，这一类函数在Lebesgue积分和微分中有所应用。