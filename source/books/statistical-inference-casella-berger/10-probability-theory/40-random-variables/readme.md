# Random Variables

## Content Notes

#### Definition 1.4.1

A *random variable* $X:S\to\R$ is a function from a sample space $S$ into the real numbers.

#### Example 1.4.2 (Random variables)

| Experiment                                           | Random variable                   |
| ---------------------------------------------------- | --------------------------------- |
| Toss two dice                                        | $X=$ sum of the numbers           |
| Toss a coin 25 times                                 | $X=$ number of heads in 25 tosses |
| Apply different amounts of fertilizer to corn plants | $X=$ yield/acre                   |

#### Remark (Probability function of random variable)

The original probability function is defined on the original sample space, we need to TRANSFER it to define on random variable. Suppose the sample space is $S=\{s_1,\dots,s_n\}$ with a probability function $P$, the random variable $X$ is defined with range $\mathcal{X}=\{x_1,\dots,x_m\}$. Then we can define
$$
P_X(X=x_i):=P(\{s_j\in S:X(s_j)=x_i\})
$$
Note that $P_X$ is an *induced* probability function on $\mathcal{X}$ defined in terms of the function $P$. We simply write $P(X=x_i)$ rather than $P_X(X=x_i)$.

Random variables is denoted with uppercase letters and the realized values of the variable is denoted by the corresponding lowercase letters. e.g, the random variable $X$ can take the value $x$.

#### Example 1.4.4 (Distribution of a random variable)

The distribution of a random variable is obtained by computing all possibilities $P_X(X=x)$ for all  $x\in\mathcal{X}$. If $\mathcal{X}$ is uncountable, we can modify the probability function to be
$$
P_X(X\in A)=P(\{s\in S:X(s)\in A\}),\quad\forall A\subset\mathcal{X}
$$

## Exercises

#### 1.45

Obviously $P_X(X=x_i)\ge0$ for all $x_i$. Consider $P_X(\mathcal{X})$, we have
$$
P_X(\mathcal{X})=P(\{s_j\in S:X(s_j)\in\mathcal{X}\})=P(S)=1
$$
Let $X_1,X_2,\dots,X_k\in\mathcal{X}$ be pairwise disjoint, then it is easy to see that $X^{-1}(X_1),\dots,X^{-1}(X_k)$ are pairwise disjoint sets in $S$, thus
$$
P_X(\cup_{i=1}^kX_i)=P\big(\cup_{i=1}^nX^{-1}(X_i)\big)=\sum_{i=1}^k P(X^{-1}(X_i))=\sum_{i=1}^kP_X(X_i)
$$

#### 1.46

The possible values of $x$ for the random variable $X_3$ is $0,1,2$. The event $X_3=0$ is the event "no cells contain exactly 3 balls". The event $X_3=1$ is the event "just one cell contain exactly 3 balls". The event $X_3=2$ is the event "two cells contain exactly 3 balls". And
$$
P(X_3=2)=\dfrac{\binom{7}{2}\binom{7}{3}\binom{4}{3}\binom{5}{1}}{7^7}
$$
The sample space contains $7^7$ points. The event: choose 2 places in 7 to put 3 balls, then choose 3 balls out of 7, choose 3 balls out of the remaining 4, then choose 1 places in 5 to put the last ball.

For $X_3=1$, the probability depends on how the ball is organized, there are four types of organization that satisfy the event (4-3),(3-2-2),(3-2-1-1),(3-1-1-1-1), the corresponding numbers in the event space can be similarly computed.
$$
\begin{aligned}
4-3&:\binom{7}{1}\binom{7}{4}\binom{6}{1}
\\
3-2-2&:\binom{7}{1}\binom{7}{3}\binom{6}{2}\binom{4}{2}
\\
3-2-1-1&:\binom{7}{1}\binom{7}{3}\binom{6}{1}\binom{4}{2}\binom{5}{2}\binom{2}{1}
\\
3-1-1-1-1&:\binom{7}{1}\binom{7}{3}\binom{6}{4}4!
\end{aligned}
$$
Thus
$$
P(X_3=1)=\dfrac{
\binom{7}{1}\binom{7}{4}\binom{6}{1}
+\binom{7}{1}\binom{7}{3}\binom{6}{2}\binom{4}{2}
+\binom{7}{1}\binom{7}{3}\binom{6}{1}\binom{4}{2}\binom{5}{2}\binom{2}{1}
+\binom{7}{1}\binom{7}{3}\binom{6}{4}4!
}{7^7}
$$

 