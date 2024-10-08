# AI的强项与限制——浅度使用AI随感

时至今日（2024年），AI已经不是一个陌生的东西。自前一年OpenAI的ChatGPT开启AI之门后，很多国内外大模型迅猛创新，呈现一个百花齐放的生态。但从原理上说，AI提供回答文本的本质是一种大量数据、大量参数支撑的数据回归行为，与其说是其推理出了结果，不如说是其用超强的体力、搜索力和不知疲倦的输出能力以极快速度寻找出“最像结果”的文字。近两日，我因解一道数学题，浅度使用了AI，发现结果并不如预想的那样美好，但也不是一无是处。

这道需要AI来解答的数学题是这样的：

Let $F=\{F_1,F_2,\dots\}$ be a countable collection of connected compact sets in $\mathbf{R}^n$ such that $F_{k+1}\subseteq F_k$ for each $k\ge1$. Prove that the intersection $\bigcap_{k=1}^{\infty}F_k$ is connected.

由于苦寻思路无果，我希望用AI来提供一些启发。首先使用的是国内的某义某问，我将问题转换为一个描述性的文字问题喂给了它，返回的解答如下

## 第一轮问答

我的问题：why is the intersection of a set of nested compact connected sets still connected?

AI的回答：

To understand why the intersection of a set of nested compact connected sets is still connected, let's break down the reasoning step by step.

### Definitions and Assumptions

1. **Compact Set**: A set is compact if every open cover has a finite subcover.
2. **Connected Set**: A set is connected if it cannot be divided into two disjoint non-empty open subsets.
3. **Nested Sets**: A sequence of sets $\{A_n\}$ is nested if $A_{n+1} \subseteq A_n$ for all $n$.

### Theorem

**Theorem**: Let $\{A_n\}$ be a sequence of nested compact connected subsets of a topological space $X$. Then the intersection $A = \bigcap_{n=1}^\infty A_n$ is connected.

### Proof

1. **Assume for contradiction**: Suppose $A$ is not connected. Then there exist two non-empty, disjoint, open sets $U$ and $V$ in $A$ such that $A = U \cup V $.

2. **Extend $U$ and $V$ to $X$**: Since $U$ and $V$ are open in $A$, there exist open sets $U'$ and $V'$ in $X$ such that $U = U' \cap A$ and $V = V' \cap A$.

3. **Consider the complements in $A_n$**: For each $n$, define $U_n = U' \cap A_n$ and $V_n = V' \cap A_n$. Note that $U_n$ and $V_n$ are open in $A_n$.

4. **Disjoint and covering $ A_n $**: Since $A \subseteq A_n$ for all $n$, we have $A = U \cup V \subseteq U_n \cup V_n$. Therefore, $A_n = (U_n \cup V_n) \cup (A_n \setminus A)$.

5. **Non-emptiness of $U_n$ and $V_n$**: Since $U$ and $V$ are non-empty and $U \subseteq U_n$ and $V \subseteq V_n$, $U_n$ and $V_n$ are non-empty for all $n$.

6. **Compactness of $A_n$**: Each $A_n$ is compact. By the definition of compactness, there must be a finite subcover for any open cover of $A_n$. Consider the open cover $\{U_n, V_n\}$ of $A_n$. Since $A_n$ is connected, $A_n$ cannot be written as the union of two non-empty, disjoint, open sets. Therefore, either $U_n$ or $V_n$ must be empty, which contradicts the non-emptiness established in step 5.

7. **Conclusion**: The assumption that $A$ is not connected leads to a contradiction. Therefore, $A$ must be connected.

### Intuitive Explanation

Intuitively, if the intersection $A$ were not connected, it could be split into two non-empty, disjoint, open sets $U$ and $V$. However, since each $A_n$ is connected and compact, any attempt to split $A$ into $U$ and $V$ would have to split at least one of the $A_n$ into two non-empty, disjoint, open sets, which is impossible because $A_n$ is connected. The compactness ensures that this splitting cannot happen without violating the connectedness of some $A_n$.

Thus, the intersection of a set of nested compact connected sets remains connected.

回答到此结束。为保持原样，我直接复制文本，数学符号在AI对话框中正常显示。这一轮AI的回答亮点是：第一，准确的理解了问题，并且将问题相关的数学概念Compact set， Connected set和Nested set都定义出来；第二，分节合理，答案中给出了定义和假设、定理、证明、直觉解释四个小节，将我提出的问题转化为一个定理并尝试证明。AI回答的不足在于，证明这一节中的逻辑在我看来仍有断节，因此我开启了第二轮追问。

## 第二轮问答

我的问题：in the explanation above, why $A_n$ has an open cover $U_n,V_n$?

AI的回答：

Let's clarify why $A_n$ has an open cover $\{U_n, V_n\}$ in the context of the proof.

### Detailed Explanation

1. **Assume for contradiction**: Suppose $A$ is not connected. Then there exist two non-empty, disjoint, open sets $U$ and $V$ in $A$ such that $A = U \cup V$.

2. **Extend $U$ and $V$ to $X$**: Since $U$ and $V$ are open in $A$, there exist open sets $U'$ and $V'$ in $X$ such that $U = U' \cap A$ and $V = V' \cap A$.

3. **Define $U_n$ and $V_n$**: For each $n$, define $U_n = U' \cap A_n$ and $V_n = V' \cap A_n$. Note that $U_n$ and $V_n$ are open in $A_n$ because they are intersections of open sets in $X$ with $A_n$.

4. **Disjoint and covering $A_n$**: Since $A \subseteq A_n$ for all $n$, and $A = U \cup V$, we have:
   $$
   A_n = (A_n \cap A) \cup (A_n \setminus A)
   $$
   Because $A = U \cup V$, we can write:
   $$
   A_n = (A_n \cap (U \cup V)) \cup (A_n \setminus A)
   $$
   Since $U$ and $V$ are disjoint, $A_n \cap U$ and $A_n \cap V$ are also disjoint. Therefore:
   $$
   A_n = (U_n \cup V_n) \cup (A_n \setminus A)
   $$
   However, $A_n \setminus A$ is a subset of $A_n$ that does not intersect $A$, so it does not affect the disjointness of $U_n$ and $V_n$.

5. **Non-emptiness of $U_n$ and $V_n$**: Since $U$ and $V$ are non-empty and $U \subseteq U_n$ and $V \subseteq V_n$, $U_n$ and $V_n$ are non-empty for all $n$.

6. **Compactness of $A_n$**: Each $A_n$ is compact. By the definition of compactness, any open cover of $A_n$ has a finite subcover. Consider the open cover $\{U_n, V_n\}$ of $A_n$. Since $A_n$ is connected, $A_n$ cannot be written as the union of two non-empty, disjoint, open sets. Therefore, either $U_n$ or $V_n$ must be empty, which contradicts the non-emptiness established in step 5.

### Why $\{U_n, V_n\}$ is an Open Cover of $A_n$

- **Openness**: $U_n$ and $V_n$ are open in $A_n$ because they are intersections of open sets in $X$ with $A_n$.
- **Covering**: $U_n \cup V_n$ covers $A_n$ because $A_n \cap A = (U_n \cup V_n)$ and $A_n \setminus A$ does not affect the covering property.

### Conclusion

The sets $U_n$ and $V_n$ form an open cover of $A_n$ because they are open in $A_n$ and their union covers $A_n$. The contradiction arises because $A_n$ being connected implies that it cannot be covered by two non-empty, disjoint, open sets, leading to the conclusion that $A$ must be connected.

回答到此结束。这里AI的回答看起来很完整，但是似乎仍不太对，特别是对我的提问，AI给出了一个看似正确的解答，于是我进一步追问。

## 第三轮问答

我的问题：why $A_n \setminus A$ does not affect the covering property? without $A_n \setminus A$, the union $U_n$ and $V_n$ can not cover $A_n$

AI的回答：

You are correct in noting that $A_n \setminus A$ is a part of $A_n$ and needs to be considered in the covering. Let's refine the argument to address this point more clearly.

### Detailed Explanation

1. **Assume for contradiction**: Suppose $A$ is not connected. Then there exist two non-empty, disjoint, open sets $U$ and $V$ in $A$ such that $A = U \cup V$.

2. **Extend $U$ and $V$ to $X$**: Since $U$ and $V$ are open in $A$, there exist open sets $U'$ and $V'$ in $X$ such that $U = U' \cap A$ and $V = V' \cap A$.

3. **Define $U_n$ and $V_n$**: For each $n$, define $U_n = U' \cap A_n$ and $V_n = V' \cap A_n$. Note that $U_n$ and $V_n$ are open in $A_n$ because they are intersections of open sets in $X$ with $A_n$.

4. **Disjoint and covering $A_n$**: Since $A \subseteq A_n$ for all $n$, and $A = U \cup V$, we have:
   $$
   A_n = (A_n \cap A) \cup (A_n \setminus A)
   $$
   Because $A = U \cup V$, we can write:
   $$
   A_n = (A_n \cap (U \cup V)) \cup (A_n \setminus A)
   $$
   Since $U$ and $V$ are disjoint, $A_n \cap U$ and $A_n \cap V$ are also disjoint. Therefore:
   $$
   A_n = (U_n \cup V_n) \cup (A_n \setminus A)
   $$

5. **Non-emptiness of $U_n$ and $V_n$**: Since $U$ and $V$ are non-empty and $U \subseteq U_n$ and $V \subseteq V_n$, $U_n$ and $V_n$ are non-empty for all $n$.

6. **Compactness of $A_n$**: Each $A_n$ is compact. By the definition of compactness, any open cover of $A_n$ has a finite subcover. Consider the open cover $\{U_n, V_n, A_n \setminus A\}$ of $A_n$. Since $A_n \setminus A$ is open in $A_n$ (as $A_n$ is closed in $X$ and $A$ is closed in $A_n$), $\{U_n, V_n, A_n \setminus A\}$ is an open cover of $A_n$.

7. **Connectedness of $A_n$**: Since $A_n$ is connected, it cannot be written as the union of two non-empty, disjoint, open sets. If $U_n$ and $V_n$ were both non-empty, then $A_n$ would be the union of $U_n$ and $V_n$, which are disjoint and open in $A_n$. This would contradict the connectedness of $A_n$.

8. **Conclusion**: The assumption that $A$ is not connected leads to a contradiction. Therefore, $A$ must be connected.

### Addressing the Concern

- **Covering Property**: The set $A_n \setminus A$ is open in $A_n$ because $A$ is closed in $A_n$. Therefore, $\{U_n, V_n, A_n \setminus A\}$ is an open cover of $A_n$.
- **Disjointness**: If $U_n$ and $V_n$ were both non-empty, then $A_n$ would be the union of $U_n$ and $V_n$, which are disjoint and open in $A_n$. This contradicts the connectedness of $A_n$.

Thus, the intersection $A = \bigcap_{n=1}^\infty A_n$ must be connected.

这一次，AI直接“肯定”了我的疑问，然后声称它会修正自己的证明，然而……于是我继续追问。

## 第四轮问答

我的提问：As long as the set $A_n \setminus A$ is non-empty, this proof is wrong since $A_n$ may not be covered by $U_n$ and $V_n$

AI的回答：

You are correct in pointing out that the set $A_n \setminus A$ being non-empty could potentially affect the argument. Let's refine the proof to address this concern more rigorously.

### Refined Proof

1. **Assume for contradiction**: Suppose $A$ is not connected. Then there exist two non-empty, disjoint, open sets $U$ and $V$ in $A$ such that $A = U \cup V$.

2. **Extend $U$ and $V$ to $X$**: Since $U$ and $V$ are open in $A$, there exist open sets $U'$ and $V'$ in $X$ such that $U = U' \cap A$ and $V = V' \cap A$.

3. **Define $U_n$ and $V_n$**: For each $n$, define $U_n = U' \cap A_n$ and $V_n = V' \cap A_n$. Note that $U_n$ and $V_n$ are open in $A_n$ because they are intersections of open sets in $X$ with $A_n$.

4. **Disjoint and covering $A \cap A_n$**: Since $A \subseteq A_n$ for all $n$, and $A = U \cup V$, we have:
   $$
   A \cap A_n = (U \cup V) \cap A_n = (U_n \cup V_n)
   $$
   Therefore, $A_n \cap A = U_n \cup V_n$.

5. **Non-emptiness of $U_n$ and $V_n$**: Since $U$ and $V$ are non-empty and $U \subseteq U_n$ and $V \subseteq V_n$, $U_n$ and $V_n$ are non-empty for all $n$.

6. **Compactness of $A_n$**: Each $A_n$ is compact. By the definition of compactness, any open cover of $A_n$ has a finite subcover. Consider the open cover $\{U_n, V_n, A_n \setminus A\}$ of $A_n$. Since $A_n \setminus A$ is open in $A_n$ (as $A$ is closed in $A_n$), $\{U_n, V_n, A_n \setminus A\}$ is an open cover of $A_n$.

7. **Connectedness of $A_n$**: Since $A_n$ is connected, it cannot be written as the union of two non-empty, disjoint, open sets. If $U_n$ and $V_n$ were both non-empty, then $A_n$ would be the union of $U_n$ and $V_n$, which are disjoint and open in $A_n$. This would contradict the connectedness of $A_n$.

8. **Refinement**: To address the concern about $A_n \setminus A$, note that if $A_n \setminus A$ is non-empty, it does not affect the connectedness of $A_n$ because $A_n$ is connected by assumption. The key point is that $U_n$ and $V_n$ must cover $A_n \cap A$, and if $A_n$ is connected, it cannot be split into two non-empty, disjoint, open sets $U_n$ and $V_n$.

9. **Conclusion**: The assumption that $A$ is not connected leads to a contradiction. Therefore, $A$ must be connected.

### Addressing the Concern

- **Covering Property**: The set $A_n \setminus A$ being non-empty does not affect the connectedness of $A_n$. The connectedness of $A_n$ ensures that $A_n$ cannot be split into two non-empty, disjoint, open sets $U_n$ and $V_n$.
- **Disjointness**: If $U_n$ and $V_n$ were both non-empty, then $A_n$ would be the union of $U_n$ and $V_n$, which are disjoint and open in $A_n$. This contradicts the connectedness of $A_n$.

Thus, the intersection $A = \bigcap_{n=1}^\infty A_n$ must be connected.

AI继续肯定我的疑问，然后给出一个……仍然在数学上会被判定为错误的解答。

后续还有若干次问答，最终我并没有在这里得到满意的答案。

## 总结

如果读者有时间细看这道题，并且熟悉相关概念，则应该能与我一样看出AI表现究竟好在哪里和差在哪里。结合前期使用其他AI的一些体验，对目前阶段AI的能与不能体会如下：

### AI的擅长

第一，指向明确的工作，如果给AI的问题不会产生歧义且不需要复杂的推理或推导，则基本上会得到可用的答案。

第二，逻辑简单或高度确定，但重复次数太多导致难度很大的工作。典型例子如围棋，是确定逻辑的多次重复形成的博弈，这也是我最看好AI的一部分，类似于流水线上的机器人可以取代很多初级工人的工作，AI可以取代办公室、实验室、检测、控制等场合的重复性脑力劳动工作，既往这些工作的难度在于大量重复之下人的稳定性下降，能够持续稳定的人（现在所说的能卷、能熬）往往胜人一筹，但怎会有人卷的过24小时待机输出速度快还能调教的AI呢。。。

第三，能够跨时空迁移不受质量影响的工作。典型例子如软件，世界上任何一个人做出来，就能被其他地区有同样需求的人使用。以往软件还需要一些代码知识等门槛，并且通常需要软件开发者提供一个框架供二次开发或者拷贝使用，学习框架也是一个耗时的过程啊！但AI的出现让这个传播的颗粒度从框架下降到了功能点，基本上只要提问者能准确描述一个功能点，AI则大致能提供可用的代码。

### AI的问题

第一，目前似乎在严格且链条长的逻辑推理上仍会不足，因为AI自己是“不懂”这些问题的，只是寻找最“像”正确答案的回答。

第二，有时会自说自话，或者如有些AI使用者评论所说：一本正经的胡说八道，感官上，AI像一个懂一点但又不是真懂，并且死活不承认自己错了（当然它会承认提问者对了）的小年轻。

第三，AI有时会是信息错误的，这种信息错误不同于本文前半部分所述的逻辑错误，信息错误可能是输入语料或者训练用的信息不对，使得AI会将一个错误的东西认为是正确的，举例子而言，与connected set相关，我使用另一个国内的AI大模型提问“what is thedefinition of a connected set”，其给出的答案是

In topology, a connected set is a set that cannot be represented as the union of two or more disjoint non-empty open sets. More formally:

**Definition**: Let $X$ be a topological space. A subset $A \subseteq X$ is said to be connected if it cannot be expressed as the union of two disjoint non-empty open subsets of $X$. In other words, $A$ is connected if the only subsets of $A$ that are both open and closed in $A$ (with respect to the subspace topology) are the empty set $\emptyset$ and $A$ itself.

Here are some key points related to this definition:

1. **Disjoint Sets**: The open sets whose union is supposed to represent $A$ must be disjoint, meaning their intersection is empty.

2. **Non-Empty Sets**: Both of the open sets must be non-empty. If one of them were empty, it would not contribute to the representation of $A$.

3. **Open in the Topological Space**: <u>The open sets must be open in the topology of $X$, not just open in the subspace topology induced on $A$.</u>

4. **Closed Complements**: The complements of these open sets in $A$ must also be non-empty. If one of the complements were empty, it would mean that the corresponding open set contains $A$, which would make $A$ disconnected.

5. **Equivalent Definitions**: There are several equivalent ways to define connectedness:
   - A set is connected if and only if it is path-connected, meaning that for any two points in the set, there is a continuous function (a path) connecting them within the set.
   - A set is connected if and only if its only connected subsets are itself and the empty set.

6. **Examples**:
   - In the real line $\mathbb{R}$ with the standard topology, intervals (both open, closed, and half-open) are connected sets.
   - The union of two or more disjoint intervals is not connected.
   - The singleton set $\{a\}$ consisting of a single point is connected if considered in isolation, but it is not maximally connected because it can be part of a larger connected set (e.g., an interval containing $a$).

Connectedness is a fundamental concept in topology and has many important implications and applications in various areas of mathematics.

注意其中下划线的部分，在任何规范的拓扑学教材中，都没有对connected set的定义作如此严格的要求，并且实际上这个要求可能是错误的，例如$\R$上的区间$[0,1)\cup(1,2)$是不连通的，其可以表示为两个区间的union，但其中一个区间$[0,1)$在$\R$中不是开集。所以这个关于connected set的定义就是错误的。

第四，语言似乎会有影响。我在使用过程中也尝试过用中文提问，有些AI会智能进行翻译并且理解相对准确，但另外一些AI就

## 如何使用AI

使用AI首先要对AI的原理有个基本了解，如果数学功底好建议读一读机器学习和神经网络的入门类书籍，对AI的底层方法有起码的认识。其次应对AI有一个恰当的定位和预期，AI不是全知全能，当作从0到1的认识工具也有一定的风险（上文所说的逻辑问题和信息问题），但AI是个很好的增强工具，是个优秀的实施者，对于既往善于提出思路但不善于落实的人而言，AI是其最好的配合者。最后，对AI的使用要抱有开放的心态，AI会出现很多错误，但也能提供很多有用的信息，不妨多问一些问题，多引导AI，或多尝试不同的大模型；目前AI的使用成本还是很低，如果利用AI的成本低于自己实施或者领导他人带来的精力与心力损耗，那么学习使用AI依然是值得的。