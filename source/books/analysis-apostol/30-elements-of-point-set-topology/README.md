# Elements of Point Set Topology

本章聚焦数的集合，介绍实数线上的集合、平面上的集合以及高维空间的集合，并研究开集、闭集、紧集的概念。

## n维空间的开集

Definition 3.1, 3.2 阐述了n维点的定义和计算，包括内积、模都是以最常见的方式定义的。Theorem 3.3 给出关于模的一些常见性质，包括n维空间的Cauchy-Schwarz不等式和三角不等式。Definition 3.4 给出单位向量的定义，单位向量也叫基向量。
有了模的定义后就可以定义n维向量的开球，而后是内点的定义（Definition 3.5）和开集的定义（Definition 3.6）。后续两个定理涉及开集代数，Theorem 3.7 说明任意开集的并集都是开集，Theorem 3.8 说明有限个开集的交集是开集。

3.9-3.11这一部分整体上为证明一个重要结论：1维空间上的任意一个非空开集都是可数个互不相交开集的并.
3.12开始介绍闭集，闭集是补集为开集的集合，Theorem 3.13 说明闭集代数与开集代数正好相反，有限个闭集的并是闭集，任意闭集的交集是闭集。

3.15开始介绍 adherent point 和 accumulation point，这两个概念的中文翻译比较多样，直接用英文名称比较好。某一集合的 adherent point 是任何一个邻域都有集合中至少一个点的point，某一集合的 accumulation point 是任何一个邻域都有集合中至少一个不同于本点的point，也就是说 x 是 S 的 accumulation point 当且仅当 x 是 S-{x} 的 adherent point，如果 x 是 S 的 accumulation point 但却不属于 S ，称 x 是 S 的 isolated point。可以总结为如下等式

adherent point = accumulation point + isolated point

Theorem 3.17 说明一个 accumulation point的邻域一定包含该集合的无限个点。这个定理说明如果一个集合是有限的，那它一定没有 accumulation point，但一个无限的集合也有可能没有 accumulation point，只有限定在某一个n维球中的无限集合才总是有一个 accumulation point，这就是Bolzano-Weierstrass定理。

引入 adherent point 之后，闭集可以有新的刻画方式，即 Theorem 3.18，闭集的充要条件是包含了所有自己的 adherent point。一个集合加上自己所有的 adherent points 称为集合的闭包 closure。Theorem 3.20 说明闭集的另一个充要条件为集合等于自己的closure。Definition 3.21 定义了 derived set 为所有的 accumulation point的集合，因此闭集的另一个充要条件是集合包含了所有自己的 accumulation point。

## n维空间的覆盖定理

下一步是经典的几个实数定理。首先是3.24 Bolzano-Weierstrass定理，如果一个有界集内有无穷多个点，那么这个集合一定存在一个accumulation point。证明就是不断的用二分法。最终收缩到一个点，此点就是所求。

Theorem 3.25是Cantor intersection Theorem，如果有一系列不断嵌套的非空闭集，第一个集合是有界的，那么这些闭集的共同交集是非空闭集。

Theorem 3.28 Lindelof covering theorem，首先介绍covering的概念，Theorem3.27 更像一个引理，若S是一个开集，包含x，则能找到一个有理坐标为中心、有理数半径的球，使得x在球中，球在S中。借助3.27，可以证明Lindelof covering theorem: 若F是A的一个开覆盖，则存在一个F的可数子集也覆盖A。

Theorem 3.29 是另一个覆盖定理即Heine-Borel，在Lindelof的基础上又加强了，若F是有界闭集A的一个开覆盖，那么存在一个F的有限子集也覆盖A。

此后引入compact的概念，任意一个开覆盖都有有限子覆盖的集合是compact。Theorem 3.31是一个经典的等价关系(Heine-Borel)：在n维实空间中，compact等价于closed&bounded，等价于每个无限子集有一个accumulation point。

## 度量空间

3.32定义度量空间，注意度量空间是从集合的笛卡尔积到实数集的函数，满足所要求的条件即可。一个度量空间有时被标为$(M,d)$，因为集合M和度量d都会影响空间。

如果将点集拓扑拓展到任意度量空间，则需要用度量定义球、开集和闭集。有如下重要定理：

Theorem 3.33，X在子空间S上是开集的充要条件是X是原空间上某一个开集A和S的交集。

Theorem 3.34，Y在子空间S上是闭集的充要条件是Y是原空间上某一个开集B和S的交集。

定理3.35-3.37在欧式空间上已经得证，并且可不修改证明思路地拓展到度量空间。

## 度量空间上的紧集

定理3.38说明在度量空间上，compact可以推出closed and bounded，以及每个无限集都含有至少一个聚点。与3.31的区别是这里只证明了一个方向。定理3.39是紧空间的闭子集也是紧的

## 内部和边界

定义3.40是边界的定义。有一些习题辅助理解此定义。