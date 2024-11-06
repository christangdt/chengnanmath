# Basics of Probability Theory

## Content Notes

Probability can be thought as the "frequency of occurence" of an outcome in a sample space. However, this book defines probability in axiomatic approach, which is concerned only that the probabilities are defined by a function satisfying the axioms.

### 1.2.1 Axiomatic Foundations

For each event $A$ in the sample space $S$, we associate with $A$ a number $P(A)\in[0,1]$ that will be called the probability of $A$.

#### Definition 1.2.1

A collection of subsets of $S$ is called a *sigma algebra* or *Borel field*, denoted by $\mathcal{B}$, if it satisfies the following three properties:

-  $\empty\in\mathcal{B}$ (the empty set is an element of $\mathcal{B}$).
-  If $A\in\mathcal{B}$, then $A^c\in\mathcal{B}$ ($\mathcal{B}$ is closed under complementation).
-  If $A_1,A_2,\dots\in\mathcal{B}$, then $\cup_{i=1}^{\infty}A_i\in\mathcal{B}$ ($\mathcal{B}$ is closed under countable unions).

The empty set $\empty$ is a subset of any set, thus satisfy property 1, thus $\empty\in\mathcal{B}$. Since $S=\empty^c$, property 1,2 shows $S\in\mathcal{B}$. By DeMorgan's Law, 
$$
\bigcap_{i=1}^{\infty}A_i=\left(\bigcup_{i=1}^{\infty}A_i^c\right)^c\in\mathcal{B}
$$
Given a sample space $S$, $\{\empty,S\}$ is a sigma algebra, we concern the smallest sigma algebra that contains all open sets in $S$.

#### Example 1.2.2 (Sigma algebra I)

If a sample space $S$ is finite or countable, define
$$
\mathcal{B}=\{\text{all subsets of }S\}
$$
If $S$ has $n$ elements, then there are $2^n$ sets in $\mathcal{B}$.

#### Example 1.2.3 (Sigma algebra II)

Let $S=(-\infty,\infty)=\R$, then $\mathcal{B}$ is chosen to contain all sets of the form 
$$
[a,b],(a,b),(a,b],[a,b),\quad a,b\in\R
$$
Also $\mathcal{B}$ contains all sets that can be formed by taking unions and intersections of sets in the form above.

####  Definition 1.2.4

Given a sample space $S$ and an associated sigma algebra $\mathcal{B}$, a *probability function* is a function $P$ with domain $\mathcal{B}$ that satisfies:

1. $P(A)\ge0,\forall A\in\mathcal{B}$.
2. $P(S)=1$.
3. If $A_1,A_2,\dots\in\mathcal{B}$ are pairwise disjoint, then $P(\cup_{i=1}^{\infty}A_i)=\sum_{i=1}^{\infty}P(A_i)$.

The three properties are called the Axioms of Probability (the **Kolmogorov Axioms**). There can be many different probability functions defined for the same sample space.

#### Example 1.2.5 (Defining probabilities I)

Experiment: tossing a fair coin. $S=\{H,T\}$. "Fair" means $P(\{H\})=P(\{T\})$. By Axiom 2 we have $P(\{H\}\cup\{T\})=1$, by Axiom 3 we have $P(\{H\})+P(\{T\})=1$, then we can solve $P(\{H\})=P(\{T\})=\frac{1}{2}$.

The condition $P(\{H\})=P(\{T\})$ is not based on the axioms, we might also let $P(\{H\})=\frac{1}{9},P(\{T\})=\frac{8}{9}$ and $P$ is still a probability function.

#### Theorem 1.2.6

Let $S=\{s_1,\dots,s_n\}$ be a finite set. Let $\mathcal{B}$ be any sigma algebra of subsets of $S$. Let $p_1,\dots,p_n$ be nonnegative numbers that sum to $1$. For any $A\in\mathcal{B}$, define
$$
P(A):=\sum_{\{i,s_i\in A\}}p_i
$$
 while the sum over an empty set is define to be $0$. Then $P$ is a probability function on $\mathcal{B}$. This remains true if $S=\{s_1,\dots,s_n\}$ is a countable set.

#### Example 1.2.7 (Defining probabilities II)

Game of darts. Assume the probability of the dart hitting a particular region is propotional to the area of the region. Thus a bigger region has a higher probability of being hit, namely
$$
P(\text{scoring $i$ points})=\dfrac{\text{Area of region $i$}}{\text{Area of dart board}}
$$
We have
$$
P(\text{scoring $1$ points})=\dfrac{\pi r^2-\pi(4r/5)^2}{\pi r^2}=1-\dfrac{16}{25}=\dfrac{9}{25}
$$
It is easy to derive the general formula, which is
$$
P(\text{scoring $i$ points})=\dfrac{(6-i)^2-(5-i)^2}{5^2},\quad i=1,\dots,5
$$
it is independent of $\pi$ and $r$, we can prove this $P$ is a probability function.

#### Remark

The *Axiom of countable additivity* (Axiom 3 of Kolmogorov) is rejected by a school of statisticians led by deFinetti (1972), who choose to replace it with the *Axiom of finite additivity*, which is
$$
A,B\in\mathcal{B}:A\cap B=\empty\implies P(A\cup B)=P(A)+P(B)
$$
this axiom may not be entirely self-evident, but it is simpler than the Axiom of countable additivity.

Assuming only finite additivity can lead to unexpected complications in statistical theory. this book proceeds under the assumption of the Axiom of countable additivity.

### 1.2.2 The Calculus of Probabilities

From the Axioms of Probability we can build up many properties of the probability function that are helpful in the calculation of more complicated probabilities.

#### Theorem 1.2.8

If $P$ is a probability function and $A$ is any set in $\mathcal{B}$, then

a. $P(\empty)=0$.

b. $P(A)\le1$.

c. $P(A^c)=1-P(A)$.

#### Theorem 1.2.9

If $P$ is a probability function and $A$ and $B$ are any sets in $\mathcal{B}$, then

a. $P(B\cap A^c)=P(B)-P(A\cap B)$.

b. $P(A\cup B)=P(A)+P(B)-P(A\cap B)$.

c. If $A\subset B$, then $P(A)\le P(B)$.

#### Example 1.2.10 (Bonferroni's Inequality)

Bonferroni's Inequality allows to bound the probability of a simultaneous event in terms of the probabilities of the individual events. Use Theorem 1.2.9(b), we have
$$
P(A)+P(B)-P(A\cap B)=P(A\cup B)\le1\implies P(A\cap B)\ge P(A)+P(B)-1
$$
Suppose $A$ and $B$ are two events, each has probability .95, then
$$
P(A\cap B)\ge.95+.95-1=.90
$$

#### Theorem 1.2.11

If $P$ is a probability function, then

a. $P(A)=\sum_{i=1}^{\infty}P(A\cap C_i)$ for any partition $C_1,C_2,\dots$ ;

b. $P(\cup_{i=1}^{\infty}A_i)\le\sum_{i=1}^{\infty}P(A_i)$ for any sets $A_1,A_2,\dots$ . (Boole's Inequality)

#### Remark (Similarity between Boole's Inequality and bonferroni's Inequality)

Apply Boole's Inequality to $A^c$, we have $P(\cup_{i=1}^nA_i^c)\le\sum_{i=1}^nP(A_i^c)$, since $\cup A_i^c=(\cap A_i)^c$ and $P(A_i^c)=1-P(A_i)$, we obtain
$$
1-P\left(\bigcap_{i=1}^nA_i\right)\le n-\sum_{i=1}^nP(A_i)\implies P\left(\bigcap_{i=1}^nA_i\right)\ge\sum_{i=1}^nP(A_i)-(n-1)
$$
this is a more general version of the Bonferroni Inequality.

### 1.2.3 Counting

Counting is not easy in the hands of a statistician. The way to solve is to break down into a series of simple tasks that are easy to count, and employ known rules of combining tasks.

#### Example 1.2.12 (Lottery I)

Pick 6 numbers from the numbers $1,2,\dots,44$. To calculate the probability of wining, we must count how many different groups of six numbers can be chosen from 44.

#### Example 1.2.13 (Tournament)

In a single-elimination tournament, players advance only if they win. If we have 16 entrants, we might be interested in the number of paths a particular player can take to win, where a path is taken to mean a sequence of opponents.

#### Theorem 1.2.14 (Fundamental Theorem of Counting)

If a job consists of $k$ separate tasks, the $i$th of which can be done in $n_i$ ways, $i=1,\dots,k$, then the entire job can be done in $n_1\times n_2\times \cdots\times n_k$ ways.

#### Example 1.2.15 (Lottery II)

Refer to Example 1.2.12, the first number can be chosen in $44$ ways, the second in $43$ ways, thus the first two numbers can be chosen in $44\times43=1892$ ways. However, if the same number can be chosen repeatedly, then the first two numbers can be chosen in $44\times44=1936$ ways.

#### Definition 1.2.16

For a positive integer $n$, we define
$$
n!:=n\times(n-1)\times(n-2)\times\cdots\times3\times2\times1
$$
we further define $0!=1$.

#### Definition 1.2.17

For nonnegative integers $n$ and $r$ where $n\ge r$, we define $\binom{n}{r}$ read $n$ *choose* $r$, as
$$
\dbinom{n}{r}:=\dfrac{n!}{r!(n-r)!}
$$

#### Remark (Possible methods of counting)

Table 1.2.1 Number of possible arrangements of size $r$ from $n$ objects

|           | Without replacement  |  With replacement   |
| :-------: | :------------------: | :-----------------: |
|  Ordered  | $\dfrac{n!}{(n-r)!}$ |        $n^r$        |
| Unordered |   $\dbinom{n}{r}$    | $\dbinom{n+r-1}{r}$ |

Use the Lottery Example for discussion

1. Ordered, without replacement. The first number in 44 ways, the second in 43 ways, etc, thus there are $44!/38!$ possible tickets.
2. Ordered, with replacement. Each number can be selected in 44 ways, thus there are $44^6$ tickets.
3. Unordered, without replacement. Start from 1 and divide out the redundant orderings, six numbers can be arranged in $6!$ ways, thus there are $\dfrac{44!}{6!38!}=\dbinom{44}{6}$ possible tickets.
4. Unordered, with replacement. This is the most difficult! It is equivalent to placing 6 markers on the 44 numbers, it is further reduced to the problem of arranging 43 walls and 6 markers, which is 49 objects in total, and eliminating the redundant orderings we get there are $\dfrac{49!}{6!43!}=\dbinom{49}{6}$ tickets.

### 1.2.4 Enumerating Outcomes

To conclude 1.2.3, suppose $S=\{s_1,\dots,s_N\}$ is a finite sample space and all the outcomes are equally likely, which means $P(\{s_i\})=1/N$ for all $s_i$, then we have
$$
P(A)=\sum_{s_i\in A}P(\{s_i\})=\sum_{s_i\in A}\dfrac{1}{N}=\dfrac{\#\text{ of elements in }A}{\#\text{ of elements in }S}
$$
For large sample spaces, the counting techniques might be used to calculate both the numerator and denominator of this expression.

#### Example 1.2.18 (Poker)

Choosing a five-card poker hand from a standard deck of 52 playing cards. The sample space consists of all the five-card hangs chosen from the 52-card deck. There are $\binom{52}{5}=2598960$ possible hands. Some probabilities are
$$
P(\text{four aces})=\dfrac{48}{2598960}
\\
P(\text{four of a kind})=\dfrac{(13)(48)}{2598960}
\\
P(\text{exactly one pair})=\dfrac{13\dbinom{4}{2}\dbinom{12}{3}4^3}{2598960}
$$

#### Example 1.2.19 (Sampling with replacement)

Consider sampling $r=2$ from $n=3$ items with replacement. The outcomes in the ordered and unordered sample spaces are

|             |       |       |       |             |             |             |
| ----------- | :---: | :---: | :---: | :---------: | :---------: | :---------: |
| Unordered   | {1,1} | {2,2} | {3,3} |    {1,2}    |    {1,3}    |    {2,3}    |
| Ordered     | (1,1) | (2,2) | (3,3) | (1,2),(2,1) | (1,3),(3,1) | (2,3),(3,2) |
| Probability |  1/9  |  1/9  |  1/9  |     2/9     |     2/9     |     2/9     |

#### Example 1.2.20 (Calculating an average)

Suppose we are going to calculate all possible averages of four numbers selected from 2, 4, 9, 12, where we draw the numbers with replacement. Notice from Example 1.2.19 that in order to get the correct probability of the unordered case, we shall consider and count the ordered case. 

If we want to cosider the event of average 4.75, which can only occur when the sample is 2,4,4,9 in the unordered case. The total number of ordered sample is $n^n=4^4=256$, and the number of ordered samples that would result in $\{2,4,4,9\}$ is equivalent to enumerating the possible ordered of the four numbers, this comes in $4!=24$ ways, but the two 4s are the same, so we need to divide the $2!$ ways to arrange the two 4s and resulting in $4!/2!=12$ ways, thus the probability of drawing the unordered sample $\{2,4,4,9\}$ is $12/256$.

## Exercices

#### 1.4

(a) $P(A)+P(B)-P(A\cap B)$.

(b) $P(A)+P(B)-2P(A\cap B)$.

(c) The same as (a).

(d) $1-P(A\cap B)$.

#### 1.5

(a) $A\cap B\cap C=$ {a U.S. birth results in identical female twins}.

(b) 1 in 90 is a twin birth, and in which 1/3 are identical, in which 1/2 are female, thus
$$
P(A\cap B\cap C)=\dfrac{1}{90}\times\dfrac{1}{3}\times\dfrac{1}{2}=\dfrac{1}{540}
$$

#### 1.6

Call the first penny $P_1$, we have $P_1(head)=u,P_1(tail)=1-u$, the second penny $P_2$, we have $P_2(head)=w,P_2(tail)=1-w$, thus
$$
\begin{aligned}
p_0&=P_1(tail)P_2(tail)=(1-u)(1-w)
\\
p_1&=P_1(head)P_2(tail)+P_1(tail)P_2(head)=u(1-w)+w(1-u)
\\
p_2&=P_1(head)P_2(head)=uw
\end{aligned}
$$
If indeed $p_0=p_1=p_2$, we have
$$
p_0=p_2\implies(1-u)(1-w)=uw\implies u+w=1
\\
p_1=p_2\implies u+w-2uw=1-2uw=uw\implies uw=1/3
$$
the second equality means $u\ne0$ and $w\ne0$, let $u=1/3w$, the first equality gives
$$
\dfrac{1}{3w}+w=1\implies3w^2-3w+1=0
$$
this equation has no solution, since
$$
3w^2-3w+1\ge3\times\dfrac{1}{4}-\dfrac{3}{2}+1=\dfrac{1}{4}>0
$$

#### 1.7

(a) If the wall has area $A$, then since the area of the dart is region is $\pi 5^2=25\pi$, we can have
$$
\begin{aligned}
P(\text{scoring $0$ points})&=\dfrac{A-25\pi}{A}
\\
P(\text{scoring $1$ points})&=\dfrac{5^2\pi-4^2\pi}{A}=\dfrac{25\pi-16\pi}{A}=\dfrac{9\pi}{A}
\\
P(\text{scoring $2$ points})&=\dfrac{16\pi-9\pi}{A}=\dfrac{7\pi}{A}
\\
P(\text{scoring $3$ points})&=\dfrac{9\pi-4\pi}{A}=\dfrac{5\pi}{A}
\\
P(\text{scoring $4$ points})&=\dfrac{4\pi-\pi}{A}=\dfrac{3\pi}{A}
\\
P(\text{scoring $5$ points})&=\dfrac{\pi}{A}
\end{aligned}
$$
(b) 

#### 1.8

(a) The Area of region $i$ is the area of the outside circle minus the area of the inner side circle, the outside circle has radius $\frac{5-i+1}{5}r$ and the inner side has radius $\frac{5-i}{5}r$, thus for $i=1,\dots,5$ we have
$$
P(\text{scoring $i$ points})=\dfrac{(5-i+1)^2r^2\pi-(5-i)^2r^2\pi}{5^2\pi r^2}=\dfrac{(6-i)^2-(5-i)^2}{5^2}
$$
(b) We have
$$
P(\text{scoring $i$ points})=\dfrac{11-2i}{25}=-\dfrac{2}{25}i+\dfrac{11}{25}
$$
this is a decreasing function of $i$.

(c) We write $P(i)=P(\text{scoring $i$ points})$ for convenience, we can directly calculate
$$
P(1)=\dfrac{9}{25},P(2)=\dfrac{7}{25},P(3)=\dfrac{5}{25},P(4)=\dfrac{3}{25},P(5)=\dfrac{1}{25}
$$
then $P(i)\ge0$ for $i=1,\dots,5$, $P(S)=\sum_{i=1}^5P(i)=1$, and since scoring $i$ points and scoring $j$ points are pariwise disjoint if $i\ne j$, the third axiom is satisfied.

#### 1.9

(a) If $x\in(\cup_{\alpha}A_{\alpha})^c$, then $x\notin A_{\alpha}$ for all $\alpha\in\Gamma$, thus $x\in A_{\alpha}^c$ for all $\alpha\in\Gamma$, thus $x\in\cap_{\alpha}A_{\alpha}$. Vice versa.

(b) We have
$$
\begin{aligned}
x\in(\cap_{\alpha}A_{\alpha})^c&\iff x\notin\cap_{\alpha}A_{\alpha}\iff\exists\beta\in\Gamma,x\notin A_{\beta}
\\&\iff\exists\beta\in\Gamma,x\in A_{\beta}^c\iff x\in\cup_{\alpha}A_{\alpha}^c
\end{aligned}
$$

#### 1.10

Let $A_1,\dots,A_n$ be a collection of sets, then $(\cup_{i=1}^nA_i)^c=\cap_{i=1}^nA_i^c$ and $(\cap_{i=1}^nA_i)^c=\cup_{i=1}^nA_i^c$. The prove process can follow Exercise 1.9.

#### 1.11

(a) First $\empty\in\mathcal{B}$, second $\empty^c=S$ and $S^c=\empty$, third $\empty\cup S=S\in\mathcal{B}$.

(b) First $\empty\in\mathcal{B}$, second if $A\subseteq S$, then $A^c=S\setminus A\subseteq S$, third for any $A_1,A_2,\dots\subseteq S$, we have $\cup_{i=1}^{\infty}A_i\subseteq S$.

(c) Let $\mathcal{B}_1,\mathcal{B}_2$ be two sigma algebras and let $\mathcal{B}=\mathcal{B}_1\cap\mathcal{B}_2$. Since $\empty\in\mathcal{B}_1$ and $\empty\in\mathcal{B}_2$, we see $\empty\in\mathcal{B}$ and property 1 is satisfied. If $A\in\mathcal{B}$, then $A\in\mathcal{B}_1$ and $A\in\mathcal{B}_2$, thus $A^c\in\mathcal{B}_1$ and $A^c\in\mathcal{B}_2$ and so $A^c\in\mathcal{B}$, so property 2 is satisfied. If $A_1,A_2,\dots\in\mathcal{B}$, then $A_i\in\mathcal{B}_1$ and $A_i\in\mathcal{B}_2$ for all $i$, thus $\cup_{i=1}^{\infty}A_i\in\mathcal{B}_1$ and $\cup_{i=1}^{\infty}A_i\in\mathcal{B}_2$, which gives $\cup_{i=1}^{\infty}A_i\in\mathcal{B}$.

#### 1.12

(a) For $A,B\in\mathcal{B}:A\cap B=\empty$, we see that $A$ and $B$ are pairwise disjoint, thus $P(A\cup B)=P(A)+P(B)$ holds.

(b) Let $A_1,A_2,\dots\in\mathcal{B}$ be a sequence of sets that are pairwise disjoint, define $B_n=\cup_{i=n}^{\infty}A_i$, then $B_1\supset B_2\supset\cdots\supset B_n\supset\cdots$, moreover, we have $B_n=(\cup_{i=1}^{\infty}A_i)\cap(\cup_{i=1}^{n-1}A_i)^c$, as $n\to\infty$, we have $\cup_{i=1}^{n-1}A_i\to\cup_{i=1}^{\infty}A_i$ and thus $B_n\downarrow\empty$. From the Axiom of Finite Additivity we have $P(\cup_{i=1}^{n-1}A_i)=\sum_{i=1}^{n-1}P(A_i)$. Now use Theorem 1.2.9(a) we have
$$
\begin{aligned}
P(B_n)&=P\Big((\cup_{i=1}^{\infty}A_i)\cap(\cup_{i=1}^{n-1}A_i)^c\Big)=P(\cup_{i=1}^{\infty}A_i)-P\Big((\cup_{i=1}^{\infty}A_i)\cap(\cup_{i=1}^{n-1}A_i)\Big)
\\&=P(\cup_{i=1}^{\infty}A_i)-P(\cup_{i=1}^{n-1}A_i)
=P(\cup_{i=1}^{\infty}A_i)-\sum_{i=1}^{n-1}P(A_i)
\\&\implies P(\cup_{i=1}^{\infty}A_i)=P(B_n)+\sum_{i=1}^{n-1}P(A_i)
\end{aligned}
$$
Use Axiom of Continuity we have $P(B_n)\to 0$ as $n\to\infty$, this gives $P(\cup_{i=1}^{\infty}A_i)=\sum_{i=1}^{\infty}P(A_i)$, so the Axiom of Countable Additivity holds.

#### 1.13

Assume that $A$ and $B$ are disjoint, then $P(A\cup B)=P(A)+P(B)$, use Axiom 2 we have $P(B)=P(S)-P(B^c)=1-\frac{1}{4}=\frac{3}{4}$, thus we have
$$
P(A\cup B)=\dfrac{1}{3}+\dfrac{3}{4}>1=P(S)
$$
this is a contradiction to Theorem 1.2.8(b). Thus $A$ and $B$ cannot be disjoint.

#### 1.14

For each element $x\in S$, $x$ may or maynot occur in a subset of $S$. Thus there are $2^n$ choices when formatting a subset of $S$, resulting in $2^n$ subsets of $S$ in total.

#### 1.15

The case $k=2$ is already proved, suppose the statement is true for any jobs that consist of $k=m$ tasks, where $m\ge2$, if there is a job consisting of $k=m+1$ tasks, the $i$th of which can be done in $n_i$ ways, then consider the last task as task $m+1$, and the first $m$ tasks as a new job as a whole, which we suppose can be done in $p$ ways, then we can do the entire job in $p\times n_{m+1}$ ways, as in the case when $k=2$. Now the new job consists of $m$ tasks, the $i$th of which can be done in $n_i$ ways, by the induction hypothesis, we thus have
$$
p=n_1\times n_2\times\cdots\times n_m
$$
thus the whole task can be done in $n_1\times n_2\times\cdots\times n_m\times n_{m+1}$ ways and the induction is valid.

#### 1.16

(a) One surname and two given names can have 26 choices of initials each, thus there are $26^3$ sets.

(b) One surname and one given name has $26^2$ sets, combining (a), the answer is $26^2+26^3$.

(c) Similar to (b), the answer is $26^4+26^3+26^2$.

#### 1.17

There are two kinds of pieces: one kind with the same number repeated twice, we have $n$ choices and $n$ pieces; the other kind with different numbers, we have $n$ choices for the first and $(n-1)$ for the second, dividing the order effect $2!$, this kind has $\dfrac{n(n-1)}{2!}$ different pieces. In total, the answer is
$$
n+\dfrac{n(n-1)}{2!}=\dfrac{n^2-n+2n}{2}=\dfrac{n(n+1)}{2}
$$

#### 1.18

In the sample space, each ball has $n$ choices, thus there are $n^n$ elements in total. The event "exactly one cell remains empty" means there is one cell empty, one cell has two balls, the other $n-2$ cells has one ball. We shall first choose 2 cells out of $n$ to be the empty and the two-ball cell, since they are different, there are $n(n-1)$ ways to choose. Having chosen the empty and the two-ball cell, we can select which two balls go into the two-ball cell, this has $\binom{n}{2}$ ways, and the remaining $n-2$ balls are put into the remaining $n-2$ cells with 1 ball picking 1 cell, this results in $(n-2)\times(n-1)\times\cdots\times2\times1$ ways, or $(n-2)!$ ways, use Theorem 1.2.14, the answer is
$$
\dfrac{n(n-1)\times\dbinom{n}{2}\times(n-2)!}{n^n}=\dfrac{\dbinom{n}{2}n!}{n^n}
$$

#### 1.19

(a) This is equivalent to the problem of placing 4 markers ($\partial$) on the 3 variables ($x,y,z$), this can be further reduced to the unordered with replacement situation, thus a function of $n$ variables has $\binom{3+4-1}{3}=\binom{6}{3}$ fourth partial derivatives.

(b) This is equivalent to the problem of placing $r$ markers ($\partial$) on the $n$ variables, this can be further reduced to the unordered with replacement situation, and the conclusion is obvious, since possible unordered with replacement arrangements of size $r$ from $n$ objects has number $\dbinom{n+r-1}{r}$.

#### 1.20

The sample space is equivalent to putting 6 walls in between 12 calls. From left to right, wall $i$ separates calls from day $i$ to day $i+1$. For the sample space there are 13 places to put the 6 same walls, there are $\binom{13+6-1}{6}=\binom{18}{6}$ ways. For the event of at least one call each day, there are 11 places to put the 6 walls without replacement, which is $\binom{11}{6}$ ways. The probability is
$$
\dfrac{\dbinom{11}{6}}{\dbinom{18}{6}}=\dfrac{11!/5!}{18!/12!}=\dfrac{462}{18564}
$$
【Remark】书中给的参考答案是.2285，其是将12个call视为有序重复排列 ordered with replacement，但题面中并未明确这12个call到底是否是不同的（有序的），本人更倾向于理解这12次call是同类的，因此更符合 unordered with replacement的情况

#### 1.21

The sample space is choosing $2r$ shoes from $2n$ shoes, which is $\binom{2n}{2r}$. The event can be break down into: select $2r$ pairs from the $n$ pairs, which is $\binom{n}{2r}$, and then for each of the $r$ pair choose one shoe, which has $2^{2r}$ choices, thus the probability is $\binom{n}{2r}2^{2r}/\binom{2n}{2r}$.

#### 1.22

(a) The sample space is drawing 180 days from the 366 days, which has $\binom{366}{180}$ choices, the event is to select 15 days in each month, thus the probability is
$$
\dfrac{\binom{31}{15}\binom{29}{15}\binom{31}{15}\binom{30}{15}\binom{31}{15}\binom{30}{15}\binom{31}{15}\binom{31}{15}\binom{30}{15}\binom{31}{15}\binom{30}{15}\binom{31}{15}}{\binom{366}{180}}=\dfrac{\binom{31}{15}^7\binom{30}{15}^4\binom{29}{15}}{\binom{366}{180}}
$$
(b) The sample space is drawing 30 days from 366days, which has $\binom{366}{30}$ choices. The event is select 30 days from 336 days (excluding September), which is $\binom{336}{30}$, thus the probability is $\binom{336}{30}/\binom{366}{30}$.

#### 1.23

The probability that one person tosses a fair coin $n$ times with $k$ heads ($0\le k\le n$) is the same as the probability with $k$ tails. Thus the event is equivalent to arrange $2n$ coins in a row and select $n$ position to make then heads, since if the first person tosses $k$ heads (which is represented by $k$ heads in the first $n$ positions), then the second person has $n-k$ heads, which has the same probability of having $k$ heads, thus as long as there are $n$ heads in total, it is an element of the event. The probability of "select $n$ in $2n$ and make them heads" is $\binom{2n}{n}(\frac{1}{2})^n(\frac{1}{2})^n$, the first $(\frac{1}{2})^n$ is the probability of the $n$ positions in heads, and the second $(\frac{1}{2})^n$ is the probability of the $n$ positions in tails.

#### 1.24

We let $E_i=\{\text{head first appears on the $i$th toss}\}$, and suppose $P(head)=p$ for each toss. Then the event [$A$ wins] can be expressed as $E_1\cup E_3\cup E_5\cup\cdots$, or $\cup_{i=1}^{\infty}E_{2i-1}$. We have $E_i\cap E_j=\empty$, and $P(E_i)=(1-p)^{i-1}p$ for all $i$, thus
$$
P(A \text{ wins})=\sum_{i=1}^{\infty}P(E_{2i-1})=\sum_{i=1}^{\infty}(1-p)^{2i-2}p=p\sum_{i=0}^{\infty}[(1-p)^2]^i=\dfrac{p}{1-(1-p)^2}
$$
(a) The coin is fair means $p=1/2$, thus $P(A \text{ wins})=\frac{1/2}{1-1/4}=2/3$.

(b) Obvious.

(c) We have
$$
\dfrac{p}{1-(1-p)^2}=\dfrac{p}{2p-p^2}=\dfrac{1}{2-p}>\dfrac{1}{2}
$$

#### 1.25

The sample space is $\{BG,BB,GB\}$, and the event is $BB$, thus the probability is $1/3$. Or, we can treat it as a contitional probability, the probability of "at least one of two children is a boy" is $3/4$, and the probability of "both children are boys" is $1/4$, thus the probability of "both children are boys given at least one of two children is a boy" is $1/3$.

#### 1.26

Let $E_i=\{\text{6 first appears on the $i$th cast}\}$, then $P(E_i)=(\frac{5}{6})^{i-1}(\frac{1}{6})$. We have
$$
P(E_1)=\dfrac{1}{6},P(E_2)=\dfrac{5}{36},P(E_3)=\dfrac{25}{6^3},P(E_4)=\dfrac{5^3}{6^4},P(E_5)=\dfrac{5^4}{6^5}
$$
The probability that it must be cast more than 5 times is
$$
P=1-\sum_{i=1}^5P(E_i)=\dfrac{6^5-6^4-5\times6^3-5^2\times6^2-5^3\times6-5^4}{6^5}=\dfrac{5^5}{6^5}
$$
Another method is to treat the event "it must be cast more than 5 times" as "no 6 in the $i$th cast" for $i=1,\dots,5$, each has the probability $5/6$, thus the event has probability $(5/6)^5$.

#### 1.27

(a) When $n\ge2$, we have
$$
(1+x)^n=1+\dbinom{n}{1}x+\cdots+\dbinom{n}{n-1}x^{n-1}+\dbinom{n}{n}x^n=\sum_{k=0}^n\dbinom{n}{k}x^k
$$
thus let $x=-1$ we get $\sum_{k=0}^n(-1)^k\binom{n}{k}=(1-1)^n=0$.

(b) Use (a) and differentiate with respect to $x$ on both sides of the equation, we get
$$
n(1+x)^{n-1}=\dbinom{n}{1}+\cdots+(n-1)\dbinom{n}{n-1}x^{n-2}+n\dbinom{n}{n}x^{n-1}=\sum_{k=1}^nk\dbinom{n}{k}x^{k-1}
$$
thus let $x=1$ we get $\sum_{k=1}^nk\binom{n}{k}=n2^{n-1}$.

(c) Use (b), let $x=-1$, we have $\sum_{k=1}^n(-1)^{k-1}k\binom{n}{k}=\sum_{k=1}^n(-1)^{k+1}k\binom{n}{k}=n0^{n-1}=0$.

#### 1.28

One can refer to the book "An Introduction to Probability Theory and its Applications" (Feller 1968) and find a rigorous proof of the Stirling's Formula. This exercise cannot be done with the hint it refers, one can apply the Euler-Maclarin formular to $f(x)=\log{x}$ and then get the proof.

【Remark】这一题与概率基本无关，主要是提供一个可以近似计算$n!$的公式，在$n$非常大的时候，这个公式是有用的，因为常用的计算机语言多数会遇到计算结果溢出整数范围的情况。除了Feller书中严格的证明外，也可以利用无穷级数的知识予以证明。

#### 1.29

(a) For the case {4,4,12,12} the ordered samples include {4,4,12,12},{4,12,4,12},{4,12,12,4},{12,12,4,4},{12,4,12,4},{12,4,4,12}. For the case {2,9,9,12}, the ordered samples include the first six {2,9,9,12},{2,12,9,9},{12,9,9,2},{9,9,2,12},{9,9,12,2},{12,2,9,9}, which make the 9's together, and six {12,9,2,9},{9,2,9,12},{2,9,12,9},{9,12,9,2},{9,12,2,9},{9,2,12,9}, which seperates the 9's apart.

(b) is the same as (a).

(c) The sample space counts for $6^6$, and for the particular unordered sample we have $\frac{6!}{2!2!}=180$ results, thus the probability is $180/6^6=.003858$.

(d) For an unordered sample of size $k$, to count the ordered components we have $k!$ arrangements, in which each number from $1$ to $m$ is repeatedly counted $k_m!$ times, thus the total number of ordered components is $\dfrac{k!}{k_1!k_2!\cdots k_m!}$.

(e) The number of distinct bootstrap examples is equivalent to selecting $k$ from $m$ numbers with replacement, and the order does not matter (since we consider distinct examples), which has number $\dbinom{m+k-1}{k}$ according to table 1.2.1.

#### 1.31

(a) If the outcome has average $(x_1+\cdots+x_n)/n$, by Exercise 1.29(d), we know that each $k_1=\cdots=k_n=1$, and it corresponds to $n!/(1!1!\cdots1!)=n!$ ordered components, thus the out come has probabiliy $n!/n^n$. Suppose there are some $k_i>1$, then $k_1!k_2!\cdots k_m!>1$ and the number of ordered components is $\dfrac{n!}{k_1!k_2!\cdots k_m!}<n!$, thus the probability is smaller.

(b) From $n!\approx\sqrt{2\pi}n^{n+(1/2)}e^{-n}$ we have $n!/n^n\approx\sqrt{2\pi}n^{(1/2)}e^{-n}$.

(c) We need to select $n$ times to get the outcome, the event that each time we miss a particular $x_i$ has the probability $\frac{n-1}{n}$, thus the probability of the outcome is $(\frac{n-1}{n})^n=(1-\frac{1}{n})^n$, as $n\to\infty$, this probability tends to $e^{-1}$ is obvious.
