# Systems of Linear equations--Theoretical Aspects

### Content Notes

The system of equations
$$
a_{11}x_1+a_{12}x_2+\cdots+a_{1n}x_n=b_1
\\
a_{21}x_1+a_{22}x_2+\cdots+a_{2n}x_n=b_2
\\
{\vdots}
\\
a_{m1}x_1+a_{m2}x_2+\cdots+a_{mn}x_n=b_m\tag{S}
$$
where $a_{ij}$ and $b_i$ ($1\le i\le m$ and $1\le j\le n$) are scalars in a field $F$ and $x_1,x_2,\dots,x_n$ are $n$ variables taking values in $F$, is called a **system of** $m
$ **linear equations in** $n$ **unknowns over the field** $F$.

The $m\times n$ matrix
$$
A=\begin{pmatrix}a_{11}&a_{12}&\cdots&a_{1n}\\a_{21}&a_{22}&\cdots&a_{2n}\\{\vdots}&\vdots&&\vdots\\a_{m1}&a_{m2}&\cdots&a_{mn}\end{pmatrix}
$$
is called the **coefficient matrix** of the system $(S)$. The system may be written as $Ax=b$.

A **solution** to the system $(S)$ is an $n$-tuple
$$
s=\begin{pmatrix}s_1\\s_2\\{\vdots}\\s_n\end{pmatrix}\in\mathsf{F}^n
$$
such that $As=b$. The set of all solutions to the system $(S)$ is called the **solution set** of the system. System $(S)$ is called **consistent** if its solution set is nonempty; otherwise it is called **inconsistent**.

#### Definition

A system $Ax=b$ of $m$ linear equations in $n$ unknowns is said to be **homogeneous** if $b=0$. Otherwise the system is said to be **nonhomogeneous**.

#### Theorem 3.8

Let $Ax=0$ be a homogeneous system of $m$ linear equations in $n$ unknowns over a field $F$. Let $\mathsf{K}$ denote the set of all solutions to $Ax=0$. Then $\mathsf{K}=\mathsf{N}(\mathsf{L}_A)$; hence $\mathsf{K}$ is a subspace of $\mathsf{F}^n$ of dimension $n-\text{rank}(\mathsf{L}_A)=n-\text{rank}(A)$.

##### Corollary

If $m<n$, the system $Ax=0$​ has a nonzero solution.

#### Theorem 3.9

Let $\mathsf{K}$ be the solution set of a system of linear equations $Ax=b$, and let $\mathsf{K_H}$ be the solution set of the corresponding homogeneous system $Ax=0$. Then for any solution $s$ to $Ax=b$, 
$$
K=\{s\}+\mathsf{K_H}=\{s+k:k\in\mathsf{K_H}\}.
$$

#### Theorem 3.10

Let $Ax=b$ be a homogeneous system of $n$ linear equations in $n$ unknowns. If $A$ is invertible, then the system has exactly one solution, namely $A^{-1}b$. Conversely, if the system has exactly one solution, then $A$ is invertible.

#### Theorem 3.11

Let $Ax=b$ be a system of linear equations. Then the system is consistent if and only if $\text{rank}(A)=\text{rank}(A|b)$.

### Selected Exercises

#### 9

If $Ax=b$ has a solution, then there is $s\in\mathsf{F}^n$ such that $As=b$, this means $\mathsf{L}_A(s)=b$, thus $b\in\mathsf{R}(\mathsf{L}_A)$. Conversely, if $b\in\mathsf{R}(\mathsf{L}_A)$, then there is $s\in\mathsf{F}^n$ such that $As=b$, this $s$ is a solution.

#### 10

Let $Ax=b$ be a homogeneous system of $m$ linear equations in $n$ unknowns. If $A$ has rank $m$, then $\text{rank}(A|b)=m$, thus by Theorem 3.11, the system has a solution.

### Summary

本节和下一节专门研究线性方程组系统，本节使用第二章的结果把线性方程组的解集合描述为一个线性空间的子集（齐次方程组的解集合是一个子空间）。首先研究齐次方程组，定理3.8说明齐次方程组的解集合是一个子空间，定理3.9说明非齐次方程组的解集合可以表示成一个coset，定理3.10说明线性方程组有唯一解的等价条件是系数矩阵$A$是可逆的，定理3.11说明线性方程组有解的等价条件是系数矩阵和增广矩阵等秩。本节的最后给了一个关于Leontief的应用。