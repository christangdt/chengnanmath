# Introduction

### Content Notes

#### Definition for vector

A vector is represented by an arrow whose **length** denotes the magnitude of the vector and whose **direction** represents the direction of the vector.

#### Parallelogram Law for Vector Addition

The sum of two vectors $x$ and $y$ that act at the same point $P$ is the vector beginning at $P$ that is represented by the diagonal of parallelogram having $x$ and $y$ as adjacent sides.

#### Geometric View for Vector Addition and Multiplication

Two nonzero vectors $x$ and $y$ are called parallel if $y = tx$ for some nonzero real number $t$.  

#### Algebraic Properties of Vector Calculation

1. For all vectors $x$ and $y$, $x + y = y + x$.
2. For all vectors $x, y$, and $z$, $(x + y) + z = x + (y + z)$.
3. There exists a vector denoted $0$ such that $x + 0 = x$ for each vector $x$.
4. For each vector $x$, there is a vector $y$ such that $x + y = 0$.
5. For each vector $x$, $1x = x$.
6. For each pair of real numbers $a$ and $b$ and each vector $x$, $(ab)x = a(bx)$.
7. For each real number $a$ and each pair of vectors $x$ and $y$, $a(x + y) =ax + ay$.
8. For each pair of real numbers $a$ and $b$ and each vector $x$, $(a + b)x =ax + bx$.

#### Line and Plane Equations

Line equation: $x=u+t(v-u)$

Plane equation: $x=A+su+tv$

### Selected Exercises

#### 2

(b) $x=(2,4,0)+t(-5,-10,0)$.

(d) $x=(-2,-1,5)+t(5,10,2)$.

#### 3

(b) $u=(-5,6,-11),v=(2,-3,-9).x=(3,-6,7)+s(-5,6,-11)+t(2,-3,-9)$.

(d) $u=(4,4,4),v=(-7,3,1).x=(1,1,1)+s(4,4,4)+t(-7,3,1)$.

#### 4

In the Euclidean plane $\mathbf{R}^n$, the vector $0=(0,\dots,0)$.

Justify: $\forall x=(x_1,\dots,x_n)\in\mathbf{R}^n$, we have
$$
x+0=(x_1,\dots,x_n)+(0,\dots,0)=(x_1+0,\dots,x_n+0)\\=(x_1,\dots,x_n)=x
$$

#### 5

$x=(a_1,a_2)\implies tx=t(a_1,a_2)=(ta_1,ta_2)$.

#### 6

Let $A=(a,b),B=(c,d)$, the vector emanates from $A$ and terminates at $B$ is $u=(c-a,b-d)$. Let $C=(x,y)$ be the midpoint, then the vector emanates from $A$ and terminates at $C$ shall be $\frac{1}{2}u$, which means
$$
(x,y)-(a,b)=\frac{1}{2}(c-a,b-d)\implies(x,y)=\frac{1}{2}(c+a,b+d)
$$

#### 7

Let the endpoints of a parallelogram be $A=(a,a'),B=(b,b'),C=(c,c'),D=(d,d')$. The diagonals are line segment $AC$ and $BD$, let the midpoints be $M$ and $M'$, then
$$
M=\frac{1}{2}(a+c,a'+c'),\quad M'=\frac{1}{2}(b+d,b'+d')
$$
parallelogram means the vectors $u=(b,b')-(a,a')$ is the same as $v=(c,c')-(d,d')$, which means
$$
(b-a,b'-a')=(c-d,c'-d')\\\implies\begin{cases}b-a=c-d\\b'-a'=c'-d'\end{cases}\implies\begin{cases}b+d=a+c\\b'+d'=a'+c'\end{cases}
$$
thus $M=M'$.

### Summary

本节主要内容是向量的定义，向量加法的平行四边形法则，向量运算的代数性质，以及上述内容的解析几何应用：如何利用已知向量和向量的运算性质来给出直线和平面方程表达式。总体内容不多，习题也比较容易处理。这一节中向量运算的代数性质和下一节向量空间的定义有一些交叉，可以看作提前引入做一个预备。