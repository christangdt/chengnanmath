# Exercise 35-43 (Complex numbers II)

### 1.35

Recall the definition of the inverse tangent: given a real number $t$, $\tan^{-1}(t)$ is the unique real number $\theta$ which satisfies the two conditions
$$
-\dfrac{\pi}{2}<\theta<+\dfrac{\pi}{2},\quad\tan\theta=t.
$$
If $z=x+iy$, show that
a) $\arg(z)=\tan^{-1}\left(\frac{y}{x}\right),\quad\text{if }x>0$
b) $\arg(z)=\tan^{-1}\left(\frac{y}{x}\right)+\pi,\quad\text{if }x<0,y\geq 0$
c) $\arg(z)=\tan^{-1}\left(\frac{y}{x}\right)-\pi,\quad\text{if }x<0,y<0$
d) $\arg(z)=\dfrac{\pi}{2}\text{ if }x=0,y>0;\arg(z)=-\dfrac{\pi}{2}\text{ if }x=0,y<0$.

#### Solution

By the definition of $\arg(z)$ we know that $\tan(\arg(z))=y/x$, but since $\arg(z)\in(-\pi,\pi]$ and $\tan^{-1}(y/x)\in(-\pi/2,\pi/2]$, we need to modify due to the conditions of $x,y$.
a) if $x>0$, then $\arg(z)\in(-\pi/2,\pi/2)$ since $\cos\arg(z)>0$
b) if $x<0,y\geq 0$, then $\cos\arg(z)<0$ and $\sin\arg(z)\geq 0$, this means $\arg(z)\in(\pi/2,\pi)$
c) Similarly we get $\arg(z)\in(-\pi/2,0)$
d) by direct calculation of $\arg(z)$. 

### 1.36

Define the following "pseudo-ordering" of the complex numbers: we say $z_1<z_2$ if we have either
i)$|z_1|<|z_2|$
or
ii) $|z_1|=|z_2|$ and $\arg(z_1)<\arg(z_2)$.
Which of Axioms $6,7,8,9$ are satisfied by this relation?

#### Solution

Axiom 6 is satisfied. For any two complex numbers, both their norms and principal arguments are real, thus can be compared.
Axiom 7 is not satisfied, consider $x=1-i,y=1+i$, since $|x|=|y|$ and $\arg(x)=-\pi/4<\arg(y)=\pi/4$, we have $x<y$, but $x-i=1-2i$ and $y-i=1$, we have $|x-i|>|y-i|$ thus $x-i>y-i$.
Axiom 8 is satisfied, since under this ordering we have $z>0$ for all $z$.
Axiom 9 is satisfied, $x>y$ and $y>z$ means $|x|\geq |z|$, if $|x|>|z|$ then $x>z$, if $|x|=|z|$ then it means $|x|=|y|=|z|$, thus $\arg(x)>\arg(y)$ and $\arg(y)>\arg(z)$, which gives $\arg(x)>\arg(z)$ and $x>z$.

### 1.37

Which of Axioms $6,7,8,9$ are satisfied if the pseudo-ordering is defined as follows? We say $(x_1,y_1)<(x_2,y_2)$ if we have either
i) $x_1<x_2$
or
ii) $x_1=x_2$ and $y_1<y_2$.

#### Solution

Axiom 6 is satisfied.
Axiom 7 is satisfied.
Axiom 8 is not satisfied since for $x=(1,1),y=(1,2)$, we have $xy=(-1,3)$, then $x>0,y>0$ but $xy<0$.
Axiom 9 is satisfied.

### 1.38

State and prove a theorem analogous to Theorem 1.48, expressing $\arg(z_1/z_2)$ in terms of $\arg(z_1)$ and $\arg(z_2)$.

#### Solution

Theorem: If $z_1/z_2\neq 0$, then $\arg(z_1/z_2)=\arg(z_1)-\arg(z_2)+2\pi n(z_1,z_2)$, where
$$
n(z_1,z_2)=\begin{cases}
\text{ \ \ }0,\quad\text{if }-\pi<\arg(z_1)-\arg(z_2)\leq+\pi,
\\+1,\quad\text{if }-2\pi<\arg(z_1)-\arg(z_2)\leq-\pi,
\\-1,\quad\text{if }\pi<\arg(z_1)-\arg(z_2)< 2\pi.
\end{cases}
$$

*Proof*. Write $z_1=|z_1|e^{i\theta_1},z_2=|z_2|e^{i\theta_2}$, where $\theta_1=\arg(z_1)$ and $\theta_2=\arg(z_2)$. Since $-\pi<\theta_1\leq+\pi$ and $-\pi<\theta_2\leq+\pi$, we have $-2\pi<\theta_1-\theta_2<2\pi$. Hence there is an integer $n$ such that $-\pi<\theta_1-\theta_2+2n\pi\leq\pi$. this $n$ is the same as the integer $n(z_1,z_2)$ given in the theorem, and for this $n$ we have $\arg(z_1/z_2)=\theta_1-\theta_2+2\pi n$.

### 1.39

State and prove a theorem analogous to Theorem 1.54, expressing $\text{Log }(z_1/z_2)$ in terms of $\text{Log }(z_1)$ and $\text{Log }(z_2)$.

#### Solution

Theorem: If $z_1/z_2\neq 0$, then
$$
\text{Log }(z_1/z_2)=\text{Log }z_1-\text{Log }z_2+2\pi in(z_1,z_2)
$$
where $n(z_1,z_2)$ is the integer defined in theorem in Exercise 1.38.


*Proof.*
$$
\begin{aligned}
\text{Log }(z_1/z_2)&=\log|z_1/z_2|+i\arg(z_1/z_2)
\\&=\log|z_1|-\log|z_2|+i[\arg(z_1)-\arg(z_2)+2\pi n(z_1,z_2)]
\end{aligned}
$$

### 1.40

Prove that the $n$th roots of $1$ (also called the $n$th roots of unity) are given by $\alpha,\alpha^2,\dots,\alpha^n$, where $\alpha=e^{2\pi i/n}$, and show that the roots $\neq 1$ satisfy the equation
$$
1+x+x^2+\cdots+x^{n-1}=0.
$$

#### Proof

Use Theorem 1.51, the $n$th roots of $1$ can be written as $z_k=Re^{i\phi_k},k=0,1,\dots,n-1$, where $R=|1|^{1/n}=1$ and
$$
\phi_k=\dfrac{\arg(1)}{n}+\dfrac{2\pi k}{n}=\dfrac{2\pi k}{n},\quad(k=0,1,\dots,n-1)
$$
thus $z_k=(e^{2\pi i/n})^k=\alpha^k$ with $k=0,1,\dots,n-1$. Notice that $\alpha^0=1$ and $\alpha^n=e^{2\pi i}=\cos2\pi+i\sin2\pi=1$, thus $z_0=\alpha^n$.
Since
$$
1+x+x^2+\cdots+x^{n-1}=\dfrac{1-x^n}{1-x},\quad x\neq 1
$$
the roots of $1$ which $\neq 1$ obviously satisfy the equation.

### 1.41

a) Prove that $|z^i|<e^{\pi}$ for all complex $z\neq 0$.
b) Prove that there is no constant $M>0$ such that $|\cos{z}|<M$ for all complex $z$.

#### Solution

a) $z^i=e^{i\text{Log }z}=e^{-\arg(z)+i\log|z|}=e^{-\arg(z)}e^{i\log|z|}$, since $\log|z|$ is real, we have
$$
|z^i|=\left|e^{-\arg(z)}\right|\left|e^{i\log|z|}\right|=\left|e^{-\arg(z)}\right|<e^{\pi}
$$
b) Since $\cos{z}=(e^{iz}+e^{-iz})/2$, if we write $z=x+iy$, then
$$
2\cos{z}=\cos{x}(e^{y}+e^{-y})-i\sin{x}(e^y-e^{-y})
$$
which gives
$$
|\cos{z}|=\dfrac{\sqrt{\cos^2x(e^y+e^{-y})^2+\sin^2x(e^y-e^{-y})^2}}{4}=\dfrac{\sqrt{e^{2y}+e^{-2y}+2e^ye^{-y}(\cos^2x-\sin^2x)}}{4}
$$
thus for any $M>0$, we can let $z=\pi/4+\log{4M}$, then
$$
|\cos{z}|=\dfrac{\sqrt{e^{2y}+e^{-2y}}}{4}>\dfrac{e^y}{4}=\dfrac{4M}{4}=M
$$

### 1.42

If $w=u+iv$ ($u,v$ real), show that
$$
z^w=e^{u\log|z|-v\arg(z)}e^{i[v\log|z|+u\arg(z)]}.
$$

#### Solution

We write $e^z=\exp(z)$ and
$$
\begin{aligned}
z^w&=z^{u+iv}=\exp((u+iv)\text{Log }z)
\\&=\exp((u+iv)(\log|z|+i\arg(z)))
\\&=\exp(u\log|z|+iv\log|z|+iu\arg(z)-v\arg(z))
\\&=\exp(u\log|z|-v\arg(z))\exp(i[v\log|z|+u\arg(z)])
\end{aligned}
$$

### 1.43

a) Prove that $\text{Log }(z^w)=w\text{Log }z+2\pi in$, where $n$ is an integer.
b) Prove that $(z^w)^{\alpha}=z^{w\alpha}e^{2\pi in\alpha}$, where $n$ is an integer.

#### Proof

a) By the definition of $\text{Log }(z^w)$ we need to prove $\exp(w\text{Log }z+2\pi in)=z^w$ for integer $n$, or $\exp(w\text{Log }z)=z^w$ since $\exp(2\pi in)=1$. Use Exercise 1.42 we know that if write $w=u+iv$, then
$$
\begin{aligned}
z^w&=\exp(u\log|z|-v\arg(z))\exp(i[v\log|z|+u\arg(z)])
\\&=\exp(u\log|z|-v\arg(z)+i[v\log|z|+u\arg(z)])
\\&=\exp((u+iv)(\log|z|+i\arg(z)))=\exp(w\text{Log }z)
\end{aligned}
$$
b) We have
$$
(z^w)^{\alpha}=e^{\alpha\text{Log }z^w}=e^{w\alpha\text{Log }z+2\pi in\alpha}=\left(e^{\text{Log }(z)}\right)^{w\alpha}e^{2\pi in\alpha}=z^{w\alpha}e^{2\pi in\alpha}
$$