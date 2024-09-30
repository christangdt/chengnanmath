# Exercise 27-34 (Complex numbers I)

### 1.27

Express the following complex numbers in the form $a+bi$.

a) $(1+i)^3$

b) $(2+3i)/(3-4i)$

c) $i^5+i^{16}$

d) $\frac{1}{2}(1+i)(1+i^{-8})$.

#### Solution

a) $(1+i)^3=2i(1+i)=-2+2i$

b) $(2+3i)/(3-4i)=(2+3i)(3+4i)/25=(-6+17i)25=-6/25+(17/25)i$

c) $i^5+i^{16}=i+(i^4)^4=1+i$

d) since $i^2=-1$, we have $i^4=1$ and $i^8=1$, thus $\frac{1}{2}(1+i)(1+i^{-8})=1+i$.

### 1.28

In each case, determine all real $x$ and $y$ which satisfy the given relation.

a) $x+iy=|x-iy|$

b) $x+iy=(x-iy)^2$

c) $\sum_{k=0}^{100}i^k=x+iy$.

#### Solution

a) $(x,0),x\in\mathbf{R}$

b) $x=0,y=0$ or $x=1,y=0$ or $x=-1/2,y=\pm\sqrt{3}/2$

c) we have $i+i^2+i^3+i^4=0$, thus $\sum_{k=0}^{100}i^k=i^0=1$, which means $x=1,y=0$.

### 1.29

If $z=x+iy$, $x$ and $y$ real, the complex conjugate of $z$ is the complex number $\bar{z}=x-iy$. Prove that:

a) $\overline{z_1+z_2}=\bar{z}_1+\bar{z}_2$

b) $\overline{z_1z_2}=\bar{z}_1\bar{z}_2$

c) $z\bar{z}=|z|^2$

d) $z+\bar{z}=$ twice the real part of $z$

e) $(z-\bar{z})/i=$ twice the inaginary part of $z$

#### Proof

a) Let $z_1=a+bi,z_2=c+di$, then 
$$\overline{z_1+z_2}=\overline{a+c+(b+d)i}=a+c-(b+d)i=a-bi+c-di=\bar{z}_1+\bar{z}_2$$

b) $\overline{z_1z_2}=\overline{ac-bd+(ad+bc)i}=ac-bd-(ad+bc)i$ and $\bar{z}_1\bar{z}_2=(a-bi)(c-di)=ac-bd-(ad+bc)i$

c) Let $z=a+bi$ then $z\bar{z}=(a+bi)(a-bi)=a^2+b^2=|z|^2$

d) Let $z=a+bi$ then $z+\bar{z}=2a$

e) Let $z=a+bi$ then $z-\bar{z}=2bi$

### 1.30

Describe geometrically the set of complex numbers $z$ which satisfies each of the following conditions:

a) $|z|=1$

b) $|z|<1$

c) $|z|\leq 1$

d) $z+\bar{z}=1$

e) $z-\bar{z}=i$

f) $\bar{z}+z=|z|^2$

#### Solution

On the complex plane

a) is points on the unit circle.

b) is points inside the unit circle

c) is points not outside the unit circle

d) the verticle line which cross the point $(1/2,0)$

e) the horizontal line which cross the point $(0,1/2)$

f) Let $z=a+bi$, then $z+\bar{z}=2a$ and $|z|^2=a^2+b^2$, and $2a=a^2+b^2$ means $(a-1)^2+b^2=1$, thus this represents points on the circle which has center at $(1,0)$ and radius $1$.

### 1.31

Given three complex numbers $z_1,z_2,z_3$ such that $|z_1|=|z_2|=|z_3|=1$ and $z_1+z_2+z_3=0$. Show that these numbers are vertices of an equilateral triangle inscribed in the unit circle with center at the origin.

#### Solution

We only need to prove $|z_1-z_2|=|z_2-z_3|=|z_1-z_3|$, by symmetry we only need to prove one equality.
Define $z_k=a_k+b_ki,k=1,2,3$, then $a_k^2+b_k^2=1$ for $k=1,2,3$, thus
$$
|z_1-z_2|^2=(a_1-a_2)^2+(b_1-b_2)^2=2-2(a_1a_2+b_1b_2)
\\
|z_1-z_2|^2=|2z_1+z_3|^2=(2a_1+a_3)^2+(2b_1+b_3)^2=5+4(a_1a_3+b_1b_3)
$$
which gives 
$$2(a_1a_2+b_1b_2)+4(a_1a_3+b_1b_3)+3=0\tag{1}$$
Similarly, we have
$$
|z_1-z_3|^2=2-2(a_1a_3+b_1b_3)
\\
|z_1-z_3|^2=|2z_1+z_2|^2=5+4(a_1a_2+b_1b_2)
$$
which gives $$2(a_1a_3+b_1b_3)+4(a_1a_2+b_1b_2)+3=0\tag{2}$$
From $(1)(2)$ we have $(a_1a_2+b_1b_2)=(a_1a_3+b_1b_3)=-1/2$ and
$$
|z_1-z_2|^2=|z_1-z_3|^2=3
$$

### 1.32

If $a$ and $b$ are complex numbers, prove that:

a) $|a-b|^2\leq(1+|a|^2)(1+|b|^2)$

b) If $a\neq 0$, then $|a+b|=|a|+|b|$ if and only if $b/a$ is real and nonnegative.

#### Proof

a) We have
$$
\begin{aligned}
(1+|a|^2)(1+|b|^2)-|a-b|^2&=(1+a\bar{a})(1+b\bar{b})-(a-b)(\bar{a}-\bar{b})
\\&=1+a\bar{a}+b\bar{b}+ab\bar{a}\bar{b}-a\bar{a}-b\bar{b}+a\bar{b}+b\bar{a}
\\&=1+a\bar{b}+b\bar{a}+ab\bar{a}\bar{b}
\\&=(1+a\bar{b})(1+\bar{a}b)=(1+a\bar{b})^2\geq 0
\end{aligned}
$$
b) $a\neq 0$ means $|a|\neq 0$, thus
$$
\dfrac{|a+b|}{|a|}=\left|\dfrac{a+b}{a}\right|=\left|1+\dfrac{b}{a}\right|,\quad\dfrac{|a|+|b|}{|a|}=1+\dfrac{|b|}{|a|}=1+\left|\dfrac{b}{a}\right|
$$
Now one direction is obvious. For another direction, if $|a+b|=|a|+|b|$, as $b/a$ is a complex number, we let $b/a=x+iy$, then $|1+x+iy|=1+|x+iy|$, or
$$
\sqrt{(1+x)^2+y^2}=1+\sqrt{x^2+y^2}
$$
which gives
$$
(1+x)^2+y^2=1+x^2+y^2+2\sqrt{x^2+y^2}\Rightarrow 2x=2\sqrt{x^2+y^2}
$$
thus $x$ is nonnegative, also $2x=2\sqrt{x^2+y^2}$ means $4x^2=4x^2+4y^2$, thus $y=0$ and the proof is complete.

### 1.33

If $a$ and $b$ are complex numbers, prove that
$$
|a-b|=|1-\bar{a}b|
$$
if and only if $|a|=1$ or $|b|=1$. For which $a$ and $b$ is the inequality $|a-b|<|1-\bar{a}b|$ valid?

#### Solution

Use $z\bar{z}=|z|^2$ we have
$$
\begin{aligned}
|a-b|^2-|1-a\bar{b}|^2&=(a-b)(\bar{a}-\bar{b})-(1-a\bar{b})(1-\bar{a}b)
\\&=|a|^2+|b|^2-|a|^2|b|^2-1
\\&=(|a|^2-1)(|b|^2-1)
\end{aligned}
$$
so $|a-b|=|1-\bar{a}b|$ if and only if $|a|=1$ or $|b|=1$.
If $|a-b|<|1-\bar{a}b|$, then $(|a|^2-1)(|b|^2-1)<0$, thus $|a|<1,|b|>1$ or $|a|>1,|b|<1$.

### 1.34

If $a$ and $c$ are real constants, $b$ complex, show that the equation
$$
az\bar{z}+b\bar{z}+\bar{b}z+c=0\quad(a\neq0,z=x+iy)
$$
represents a circle in the $xy$-plane.

#### Solution

First $az\bar{z}=a(x^2+y^2)$, next $b\bar{z}+\bar{b}z=$ twice the real part of $\bar{b}z$, if $b=b_1+b_2i$, then the real part of $\bar{b}z$ is $b_1x+b_2y$, thus the equation becomes
$$
a(x^2+y^2)+2b_1x+2b_2y+c=0
$$
or