# Conditional Probability and Independence

## Content Notes

If we update the sample space based on new information, we need to calculate conditional probabilities.

#### Example 1.3.1 (Four aces)

Four cards are dealt from the top of a well-shuffled deck, the probability that they are the four aces can be calculated in two ways:

Way 1: the number of distinct four cards are $\dbinom{52}{4}=270725$ and the event is the only 1, so the probability is $\dfrac{1}{270725}$.

Way 2: The first card is ace has $p=4/52$, given that, the second card is an ace has $p=3/51$, given that, the third card is ace has $p=2/52$, .... The probability is
$$
\dfrac{4}{52}\times\dfrac{3}{51}\times\dfrac{2}{50}\times\dfrac{1}{49}=\dfrac{1}{270725}
$$
The key difference in way 2 is that we **update the sample space** after each draw of a card.

#### Definition 1.3.2

If $A$ and $B$ are events in $S$ and $P(B)>0$, then the *conditional probability of $A$ given $B$* is
$$
P(A|B):=\dfrac{P(A\cap B)}{P(B)}
$$

#### Example 1.3.2 (Continuation of Example 1.3.1)

For $i=1,2,3$ we calculate
$$
P(\text{$4$ aces in $4$ cards | $i$ aces in $i$ cards})\\=\dfrac{P(\{\text{$4$ aces in $4$ cards}\})\cap P(\{\text{$i$ aces in $i$ cards}\})}{P(\text{$i$ aces in $i$ cards})}=\dfrac{P(\text{$4$ aces in $4$ cards})}{P(\text{$i$ aces in $i$ cards})}
$$
Since
$$
P(\text{$i$ aces in $i$ cards})=\dfrac{\binom{4}{i}}{\binom{52}{i}}
$$
we have
$$
P(\text{$4$ aces in $4$ cards | $i$ aces in $i$ cards})=\dfrac{\binom{52}{i}}{\binom{4}{i}\binom{52}{4}}
$$

#### Example 1.3.4 (Three prisoners)

Three prisoners $A,B,C$ are on death row. One of the three is pardoned and chooses at random. The warden knows whom and tell $A$ that $B$ is to be executed. Then the warden and $A$ have different reasonings.

**Warden's reasoning**: Each prisoner has $\frac{1}{3}$ chance of being pardoned, thus eigher $B$ or $C$ must be executed, so I have given $A$ no new information.

**$A$'s reasoning**: Given that $B$ will be executed, either $A$ or $C$ will be pardoned, my chance of alive has risen to $\frac{1}{2}$.

The warden is correct. To see why, let $A,B,C$ denote the events that $A,B,C$ is pardoned, then $P(A)=P(B)=P(C)=\frac{1}{3}$. If $\mathcal{W}$ denote the event that the warden says $B$ is executed, then
$$
P(A|\mathcal{W})=\dfrac{P(A\cap\mathcal{W})}{P(\mathcal{W})}
$$
The key to calculate this probability correctly is to list the event throughly.

| Prisoner pardoned | Warden tells A | Probability |
| :---------------: | :------------: | :---------: |
|         A         |     B dies     |     1/6     |
|         A         |     C dies     |     1/6     |
|         B         |     C dies     |     1/3     |
|         C         |     B dies     |     1/3     |

We can see $P(\mathcal{W})=1/6+1/3=1/2$, and $P(A\cap\mathcal{W})=1/6$, thus $P(A|\mathcal{W})=1/3=P(A)$. That A's reasoning is wrong is due to $A$ interprets the event $\mathcal{W}$ to be the event $B^c$.

#### Theorem 1.3.5 (Bayes' Rule)

Let $A_1,A_2,\dots$ be a partition of the sample space, and let $B$ be any set. Then for each $i=1,2,\dots$,
$$
P(A_i|B)=\dfrac{P(B|A_i)P(A_i)}{\sum_{j=1}^{\infty}P(B|A_j)P(A_j)}
$$

#### Definition 1.3.7

Two events $A$ and $B$ are *statistically independent* if $P(A\cap B)=P(A)P(B)$.

#### Theorem 1.3.9

If $A$ and $B$ are independent events, then the following pairs are also independent.

- $A$ and $B^c$,
- $A^c$ and $B$,
- $A^c$ and $B^c$.

#### Definition 1.3.12

A collection of events $A_1,\dots,A_n$ are *mutually independent* if for any subcollection $A_{i_1},\dots,A_{i_k}$, we have
$$
P\left(\bigcap_{j=1}^kA_{i_j}\right)=\prod_{j=1}^kP(A_{i_j}).
$$

## Exercises

#### 1.33

Let $M,F$ be the event that a person is male or female, thus $P(M)=P(F)=\frac{1}{2}$. Let $C$ be the event that a person is color blind, then $P(C|M)=0.05$ and $P(C|F)=0.0025$. We have
$$
P(M|C)=\dfrac{P(C|M)P(M)}{P(C|M)P(M)+P(C|F)P(F)}=\dfrac{0.5\times0.05}{0.5\times0.05+0.5\times0.0025}=0.95238
$$

#### 1.34

We write the outcomes as events and list their probabilities:
$$
P(\text{brown}|\text{litter1})=\dfrac{2}{3},P(\text{gray}|\text{litter1})=\dfrac{1}{3},

P(\text{brown}|\text{litter2})=\dfrac{3}{5},P(\text{gray}|\text{litter2})=\dfrac{2}{5}
$$
(a) We need to calculate $P(\text{brown})$, notice that $P(\text{litter1})=P(\text{litter2})=\frac{1}{2}$, then
$$
\begin{aligned}
P(\text{brown})&=P(\text{brown}|\text{litter1})P(\text{litter1})+P(\text{brown}|\text{litter2})P(\text{litter2})
\\&=\dfrac{2}{3}\times\dfrac{1}{2}+\dfrac{3}{5}\times\dfrac{1}{2}=\dfrac{19}{30}
\end{aligned}
$$
(b) Use Bayes' Rule we have
$$
\begin{aligned}
P(\text{litter1}|\text{brown})=\dfrac{P(\text{brown}|\text{litter1})P(\text{litter1})}{P(\text{brown})}=\dfrac{1/3}{19/30}=\dfrac{10}{19}
\end{aligned}
$$

#### 1.35

Axiom 1: For $\forall A\in\mathcal{B}$, we have $A\cap B\in\mathcal{B}$ and thus $P(A\cap B)\ge0$, so $P(A|B)=P(A\cap B)/P(B)\ge0$.

Axiom 2: we have
$$
P(S|B)=\dfrac{P(S\cap B)}{P(B)}=\dfrac{P(B)}{P(B)}=1
$$
Axiom 3: If $A_1,A_2,\dots\in\mathcal{B}$ are pairwise disjoint, then
$$
\begin{aligned}
P(\cup_{i=1}^{\infty}A_i|B)&=\dfrac{P\big((\cup_{i=1}^{\infty}A_i)\cap B\big)}{P(B)}=\dfrac{P\big(\cup_{i=1}^{\infty}(A_i\cap B)\big)}{P(B)}=\dfrac{\sum_{i=1}^{\infty}P(A_i\cap B)}{P(B)}
\\&=\sum_{i=1}^{\infty}\dfrac{P(A_i\cap B)}{P(B)}=\sum_{i=1}^{\infty}P(A_i|B)
\end{aligned}
$$

#### 1.36

Let $H_i$ be the event of the target hitting $i$ times in ten shots. Then
$$
P(H_0)=(4/5)^{10},\quad P(H_1)=\binom{10}{1}\frac{1}{5}\left(\dfrac{4}{5}\right)^9=\dfrac{2\times4^9}{5^9}
$$
The probability of the target being hit at least twice is
$$
P(H_i:i\ge2)=P(S\setminus\{H_0\cup H_1\})=1-\dfrac{4^{10}}{5^{10}}-\dfrac{2\times4^9}{5^9}=\dfrac{5^{10}-14\times4^{9}}{5^{10}}
$$
Similarly we can have
$$
P(H_i:i\ge1)=P(S\setminus H_0)=1-\dfrac{4^{10}}{5^{10}}
$$
The conditional probability that the target is hit at least twice, given that it is hit at least once, is
$$
P(H_i:i\ge2 |H_i:i\ge1)=\dfrac{P(\{H_i:i\ge1\}\cap\{H_i:i\ge2\})}{P(H_i:i\ge1)}\\=\dfrac{{P(H_i:i\ge2)}}{{P(H_i:i\ge1)}}=\dfrac{5^{10}-14\times4^9}{5^{10}-4^{10}}
$$

#### 1.37

(a) We have 
$$
P(\text{warden says B dies and A pardoned})=P(A\cap\mathcal{W})=\dfrac{1}{3}\gamma
\\
P(\text{warden says C dies and A pardoned})=\dfrac{1}{3}(1-\gamma)
$$
thus $P(\mathcal{W})=(1+\gamma)/3$, and
$$
\begin{aligned}
P(A|\mathcal{W})=\dfrac{P(A\cap\mathcal{W})}{P(\mathcal{W})}=\dfrac{\gamma/3}{(\gamma+1)/3}=\dfrac{\gamma}{1+\gamma}
\end{aligned}
$$
this probability is monotonic increasing with respect to $\gamma$, if $0\ge\gamma<1/2$, then $P(A\cap\mathcal{W})<1/3$, if $\gamma=1/2$ then $P(A\cap\mathcal{W})<=1/3$, if $1/2<\gamma\le1$ then $P(A\cap\mathcal{W})>1/3$.

(b) If $A$ swap with $C$, then the probability that $A$ survives is the original probability $P(C|\mathcal{W})$, and
$$
P(C|\mathcal{W})=\dfrac{P(\text{warden says B dies and C pardoned})}{P(\mathcal{W})}=\dfrac{1/3}{1/2}=\dfrac{2}{3}
$$

#### 1.38

(a) $P(B)=1$ means that $P(A\cap B)=P(A)$, otherwise we will have
$$
P(A)-P(A\cap B)=P(A\cap B^c)>0\implies P(A\cap B^c)+P(B)>1
$$
but $(A\cap B^c)$ and $B$ are two djsoint events, thus $P((A\cap B^c)\cup B)>1$, a contradiction. Thus
$$
P(A|B)=\dfrac{P(A\cap B)}{P(B)}=\dfrac{P(A)}{1}=P(A)
$$
(b) That $A\subset B$ means $P(A\cap B)=P(A)$, thus $P(B|A)=P(A\cap B)/P(A)=1$, and
$$
P(A|B)=\dfrac{P(A\cap B)}{P(B)}=\dfrac{P(A)}{P(B)}
$$
(c) Mutually exclusive means $A\cap B=\empty$, thus use Theorem 1.2.9(b) we have
$$
P(A|A\cup B)=\dfrac{P(A\cap(A\cup B))}{P(A\cup B)}=\dfrac{P\big((A\cap A)\cup(A\cap B)\big)}{P(A)+P(B)-P(A\cap B)}=\dfrac{P(A)}{P(A)+P(B)}
$$
(d) Let $D=B\cap C$, then
$$
\begin{aligned}
P(A\cap B\cap C)&=P(A\cap D)=P(A|D)P(D)
\\&=P(A|D)P(B\cap C)=P(A|D)P(B|C)P(C)
\\&=P(A|B\cap C)P(B|C)P(C)
\end{aligned}
$$

#### 1.39

(a) Mutually exclusive means $P(A\cap B)=0$, thus we cannot have $P(A\cap B)=P(A)P(B)$.

(b) $A$ and $B$ are independent means $P(A\cap B)>0$, thus by $P(A\cup B)=P(A)+P(B)-P(A\cap B)$ we have $P(A\cup B)<P(A)+P(B)$.

#### 1.40

To prove Theorem 1.3.9(b), use the symmetry of $A$ and $B$. To prove (c), use (b) we have $A^c$ and $B$ are independent, then use (a) on $A^c$ and $B$ we have $A^c$ and $B^c$ are independent.

#### 1.41

We write the events in probabilities, which are
$$
P(\text{dash sent})=\dfrac{4}{7},\quad P(\text{dot sent})=\dfrac{3}{7}
\\
P(\text{dash received }| \text{ dash sent})=\dfrac{2}{3},P(\text{dash received }| \text{ dot sent})=\dfrac{1}{4}
\\
P(\text{dot received }| \text{ dot sent})=\dfrac{3}{4},P(\text{dot received }| \text{ dash sent})=\dfrac{1}{3}
$$
(a) We need to calculate $P(\text{dash sent }|\text{ dash received})$, which is
$$
\begin{aligned}
P(\text{dash sent }|\text{ dash received})&=\dfrac{P(\text{dash sent}\cap\text{dash received})}{P(\text{dash received})}
\\&=\dfrac{\dfrac{2}{3}\times\dfrac{4}{7}}{\dfrac{2}{3}\times\dfrac{4}{7}+\dfrac{1}{4}\times\dfrac{3}{7}}=\dfrac{8}{11}
\end{aligned}
$$
(b) With similar techniques in (a) we calculate
$$
P(\text{dot sent }|\text{ dot received})=\dfrac{\dfrac{3}{4}\times\dfrac{3}{7}}{\dfrac{3}{4}\times\dfrac{3}{7}+\dfrac{1}{3}\times\dfrac{4}{7}}=\dfrac{27}{43}
\\
P(\text{dash sent }|\text{ dot received})=\dfrac{\dfrac{1}{3}\times\dfrac{4}{7}}{\dfrac{3}{4}\times\dfrac{3}{7}+\dfrac{1}{3}\times\dfrac{4}{7}}=\dfrac{16}{43}
$$
thus $P(\text{dot-dot})=(\frac{27}{43})^2$, $P(\text{dot-dash})=P(\text{dash-dot})=\frac{27\times16}{43^2}$ and $P(\text{dash-dash})=(\frac{16}{43})^2$.

#### 1.42

(a) For any points in $\cup_{i=1}^nA_i$, it must belongs to one $E_k$ for $k=1,\dots,n$, since it is contained in at least one of the events $A_1,A_2,\dots,A_n$, and it can be contained at most in each one of the events $A_1,A_2,\dots,A_n$. Conversely we ovbiously have $E_k\subseteq\cup_{i=1}^nA_i$ for $k=1,\dots,n$. Thus we have $\cup_{i=1}^nA_i=\cup_{i=1}^nE_i$ and then use the fact that $E_k$ are pairwise disjoint, we get
$$
P(\cup_{i=1}^nA_i)=P(\cup_{i=1}^nE_i)=\sum_{i=1}^nP(E_i)
$$
 (b) If $E_k$ is contained in $A_1,A_2,\dots,A_k$, then the sum $P_1,\dots,P_k$ is able to be written in the form of sums of $P(E_i)$ for $i=1,\dots,k$. In this manner, notice that whenever we choose $j$ sets from $A_1,\dots,A_k$ and form an intersection set, it will contain $E_k$, thus the times $P(E_k)$ appears in $P_j$ is the number of summing items in $P_j$, which is $\binom{k}{j}$.

(c) By Exercise 1.27(a) we have $\sum_{i=0}^k(-1)^i\binom{k}{i}=0$, which gives
$$
\binom{k}{0}-\binom{k}{1}+\binom{k}{2}-\cdots+(-1)^k\binom{k}{k}=0
$$
thus
$$
\binom{k}{1}-\binom{k}{2}+\binom{k}{3}-\cdots\pm\binom{k}{k}=\binom{k}{0}=1
$$
(d) In the expression $P_1-P_2+P_3-\cdots\pm P_n$, the item $P(E_k)$ appears exactly
$$
\binom{k}{1}-\binom{k}{2}+\binom{k}{3}-\cdots\pm\binom{k}{k}
$$
times, thus the coefficient of $P(E_k)$ is $1$, thus we get $P_1-P_2+P_3-\cdots\pm P_n=\sum_{i=1}^nP(E_i)$.

【Remark：这道题书中正文有(a)-(e)五个小题，但书后的Errata载明，删去(b)，并将原来的(c)-(e)题号改为(b)-(d)】

#### 1.43

(a) The inclusion-exclusion identity shows that $P_1=\sum_{i=1}^nP(A_i)\ge P(\cup_{i=1}^nA_i)$, let $n\to\infty$ we get the Boole's inequality. Apply the expression to $A_i^c$ we can have
$$
\begin{aligned}
P\left(\bigcup_{i=1}^nA_i^c\right)\le\sum_{i=1}^nP(A_i^c)&\implies1-P\left(\bigcap_{i=1}^nA_i\right)\le n-\sum_{i=1}^nP(A_i)
\\
&\implies P\left(\bigcap_{i=1}^nA_i\right)\ge\sum_{i=1}^nP(A_i)-(n-1)
\end{aligned}
$$
which is the gerenal version of the Bonferroni Inequality.

【Remark：习题(b)和(c)疑似存在错误，习题(b)的题面要求证明$P_i\ge P_j$ if $i\ge j$，在书后Errata中改为证明$P_i\ge P_j$ if $i\le j$，但这个结论似乎也无法证明，利用(c)提供的极端例子，即当$A_1=\cdots=A_n=A$时，可计算得到$P_1=nP(A),P_2=\binom{n}{2}P(A)$, 此时无法保证$P_1\ge P_2$, 例如当$n=4$时就有$P_1=4P(A)<P_2=6P(A)$】

#### 1.44

If the student is guessing, the probability that he is correct in 1 question is $\frac{1}{4}$. Then the probability that he has $k$ questions correct is $P(k)=\binom{20}{k}(\frac{1}{4})^k(\frac{3}{4})^{20-k}$, and the probability that he gets at least 10 questions correct is $P(k\ge10)=\sum_{k=10}^{20}P(k)$.
