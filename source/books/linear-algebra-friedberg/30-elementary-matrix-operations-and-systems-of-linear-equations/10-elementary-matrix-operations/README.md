# Elementary Matrix Operations and Elementary Matrices

### Content Notes

#### Definitions

Let $A$ be an $m\times n$ matrix. Any one of the following three operations on the rows [columns] of $A$ is called an **elementary row [column] operation**:

- (1) interchanging any two rows [columns] of $A$;
- (2) multiplying any row [column] of $A$ by a nonzero scalar;
- (3) adding any scalar multiple of a row [column] of $A$ to another row [column].

They are all called **elementary operation** of **type 1,type 2** or **type 3**.

#### Definition

An $n\times n$ **elementary matrix** is a matrix obtained by performing an elementary operation on $I_n$. The elementary matrix is said to be of **type 1, 2** or **3** according to whether the elementary operation performed on $I_n$​ is a type 1, 2, or 3 operation, respectively.

#### Theorem 3.1

Let $A\in\mathsf{M}_{m\times n}(F)$, and suppose $B$ is obtained from $A$ by performing an elementary row [column] operation. Then there exists an $m\times m\text{ }[n\times n]$ elementary matrix $E$ such that $B=EA\text{ }[B=AE]$. In fact, $E$ is obtained from $I_m[I_n]$ by performing the same elementary row [column] operation as that which was performed on $A$ to obtain $B$. Conversely, if $E$ is an elementary $m\times m\text{ }[n\times n]$ matrix, then $EA[AE]$ is the matrix obtained from $A$ by performing the same elementary row [column] operation as that which produces $E$ from $I_m[I_n]$.

#### Theorem 3.2

Elementary matrices are invertible, and the inverse of an elementary matrix is an elementary matrix of the same type.

### Selected Exercise

#### 9

Suppose we want to perform type 1 operation to interchange row $i$ and row $j$ of $A$, then
$$
A=\begin{pmatrix}\\{\text{row }i}\\{\vdots}\\{\text{row }j}\\{}\end{pmatrix}\xrightarrow{\text{add }1\times i\text{ to }j}\begin{pmatrix}\\{\text{row }i}\\{\vdots}\\{\text{row }i+j}\\{}\end{pmatrix}\xrightarrow{\text{add }-1\times(i+j)\text{ to }i}
\begin{pmatrix}\\{\text{row }-j}\\{\vdots}\\{\text{row }i+j}\\{}\end{pmatrix}\\
\xrightarrow{\text{add }-1\times j\text{ to }i+j}
\begin{pmatrix}\\{\text{row }-j}\\{\vdots}\\{\text{row }i}\\{}\end{pmatrix}\xrightarrow{\text{multiply row }j\text{ by }-1}
\begin{pmatrix}\\{\text{row }j}\\{\vdots}\\{\text{row }i}\\{}\end{pmatrix}
$$

#### 10

Multiplying any row [column] of $A$ by a nonzero scalar $c$ is equivalent to dividing this row by $1/c$.

#### 11

Adding any scalar multiple $c$ of a row [column] of $A$ to another row [column] is equivalent to subtracting $-c$ multiple of this row [column] of $A$ to another row [column].

### Summary

初等变换，包括对行（列）交换、数乘、数乘加到另一个三类，对应有三种初等矩阵。定理3.1说明初等变换和初等矩阵的关系：对一个矩阵进行一次初等行（列）变换，等价于使用对应类型初等行（列）变换的初等矩阵左乘（右乘）该矩阵。定理3.2描述初等矩阵的性质：初等矩阵都是可逆的，且逆矩阵是同类型的初等矩阵。