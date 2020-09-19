# 1.2 数学分析中的基础定义及定理

这边一些涉及数学分析的基础定义跟定理，这里的证明会略去，应该都很容易查到。

**Definition 1.1** 称集合 X 是一个度量空间 (metric space)，若存在一个映射 d: X \times X \mapsto \mathbb R (称为度量函数，metric)，满足以下条件：<br>
(1) $d(x,y)=d(y,x), \forall x,y \in X$ <br>
(2) $d(x,y) \ge0, \forall x, y \in X; d(x,y)=0 \iff x = y $ <br> 
(3) $d(x,z) \le d(x,y) + d(y,z), \forall x, y, z \in X $ <br>
**Definition 1.2** 半径为 r 中心为 x 的开球 (open ball) 定义：(X,d) 为一度量空间 <br>
$ B(x,r)=\\{y \in X: d(x,y) < r\\} $ <br>

**Definition 1.3** 令 A $\subset X$，定义 $A$ 的内点 (interior point)， 记作 $A^o$ 是由这样的点 $x$ 构成：$\exists r_x > 0, s.t. B(x, r_x) \subset A$ ，即点 $x$ 处能找到一个完全包含在 $A$ 内的开球 <br>
**Definition 1.4** $A$ 的闭集 (closure)，记作 $\overline A$ 是由所有满足一下条件的点 $x$ 构成： <br>
每一个以点 $x$ 为中心的开球都至少包含一个点在集合 $A$ 里面 <br>
**Definition 1.5** 定义集合 $A$ 为开集 (open)，如果 $A=A^o$；集合 $A$ 为闭集 (closed)， 如果 $A=\overline A$  <br>
**Definition 1.6** 令 $f:X \mapsto \mathbb R$ ，$f$ 的支撑 (support) 被定义为 $\overline {\{x: f(x) \ne 0\}}$ <br>
**Definition 1.7** 称 $f: \mathbb R \mapsto \mathbb R$ 在 $x$ 处连续 (continuous)，若 $\forall \epsilon > 0, \exists \delta >0; s.t. \forall d(x,y) < \delta, |f(x) - f(y)| < \epsilon$  <br>
称 $f$ 是连续函数，如果 $f$ 在其定义域内每一点连续 <br>
一个关于连续的性质：开集的 $f$ 逆也是一个开集 <br>
注：我们后面会看到这一性质把连续映射的定义推广到了更一般的拓扑空间 <br>
**Definition 1.8** 称 $f:\mathbb R \mapsto \mathbb R$ 在点 $x$ 处上半连续 (upper semicontinuous), 当且仅当 $f(x) \ge \limsup_{y \to x}f(y)$; 称其在点 $x$ 处下半连续 (lower semicontinuous), 当且仅当 $f(x) \le \liminf_{y \to x}f(y)$；称其是上半/下半连续的，当且仅当其在定义域中每一点都是上半/下半连续的；称其是半连续的 (semicontinuous), 当且仅当在定义域内几乎处处连续，且在不连续点处为上半连续或下半连续的 <br>
注：半连续是比连续更弱的一个概念。直觉上理解，半连续是指函数在点 $x$ 附近的值没有比 $f(x)$ 高出太多或低出太多；上/下半连续要么是连续的，要么是往上/下跳跃 <br>
注：一个函数是连续的，当且仅当它既是上半连续又是下半连续的。
注：函数 $f$ 上半连续，当且仅当任取 $y \in \mathbb R$ ，集合 $\\{x \in X:f(x) > y\\}$ 是开集；函数 $f$ 下半连续，当且仅当任取 $y \in \mathbb R$，集合 $\\{x \in X:f(x) \le y\\}$ 是集 <br>
注：这个概念可以跟右连续 ( $f(x)=f(x^+)$ ) 跟 左连续 ( $f(x)=f(x^-)$ )对比着看，是不同角度的考量：定义域 vs. 值域。 <br>
**Definition 1.9** 称一个序列 $\\{x_n\\} \subset X$ 收敛 (converge) 到一个点 $x \in X$，当且仅当 $\forall \epsilon > 0, \exists N \in \mathbb N; s.t. \forall n \ge N, d(x_n,x) < \epsilon$ <br>
**Definition 1.10** 称一个序列被称为柯西序列 (Cauchy Sequence)，当且仅当 $\forall \epsilon > 0, \exists N \in \mathbb N; s.t. \forall m, n \ge N, d(x_m, x_n) < \epsilon $ <br>
注：从上面的定义看，柯西序列比收敛序列弱一点；即柯西序列不一定收敛（可能会收敛到 $X$ 的外面去），但收敛序列一定是柯西序列 <br>
**Definition 1.11** 若空间 $X$ 中的每一条柯西序列都收敛到 $X$ 中的一点，那么称 $X$ 为完备的 (complete) <br>
**Definition 1.12** 令 $K \subset X$, 定义 $K$ 的开覆盖 (open cover) 为一个非空集合 (collection of sets) $\{G_{\alpha}\}_{\alpha \in I} \, s.t. \,K \subset \cup_{\alpha \in I}G_{\alpha}$ ，所有的 $G_{\alpha}$ 均为开集 <br>
**Definition 1.13** 称集合 $K$ 为紧致的/紧集 (compact)，若它的每一个开覆盖都存在一个有限子覆盖，即 $\forall \{G_\alpha\}_{\alpha \in I}, \exists \, G_1, \ldots, G_n \in \{G_\alpha\}_{\alpha \in I}, s.t. K \subset \cup_{i=1}^nG_i$ 。注意，这边需要对任意一个开覆盖都成立才行。 <br>
下面给出两个关于紧集的结论：<br>

**Proposition 1.14** 若集合 $K$ 紧致, $F \subset K$ 为闭集，那么 $F$ 也是紧致
证：略。

**Proposition 1.15** 若集合 $K$ 紧致，且 $f$ 在 $K$ 上连续，那么 $\exists x_1, x_2 \in K, \, s.t. \, f(x_1)=\inf_{x \in K}f(x);f(x_2)=\sup_{x \in }f(x)$ <br>
证： 略。注：换言之, $f$ 能在 $K$ 上取到最大、最小值。另外一个理解/联想是：若 $f$ 在紧集上连续，那么 $f$ 也是一致连续的 (uniformly continuous)。注意到上文中连续的定义，每一个 $\delta>0$ 的都是对每一个点 $x$ 而言的，即 $\delta_x$ ；而一致收敛的区别就是 $\delta$ 是对定义域内所有点而言的。

紧致是分析学中一个很重要的概念。纵观整个分析学，大部分都在跟“无限”较劲 —— 所有的“有限”都很好处理，“无限”却很令人头疼。而“紧致”则是仅次于“有限”的性质，所以非常的好。

**Remark 1.16** 注意到对于一个度量空间而言，若 $x \ne y$ ，我们就可以令 $r=d(x,y) > 0$ ，那么开球 $d(x,r/2)$ 跟开球 $d(y,r/2)$ 是不相交的。于是我们找到两个不相交的开集，分别包含点 $x$ 跟点 $y$ - 这一可分割的性质叫做 Hausdorff 性质。度量空间也是一个 Hausdorff 空间。

**Definition 1.17** 令 $F$ 为 $\mathbb R$ 或 $\mathbb C$。称 $X$ 为向量空间 (vector space) 或线性空间 (linear space)，如果在空间上存在两个运算：加法 (+) 和 标量乘法 (scalar multiplication)，满足：
(1) $x+y = y+x, \forall x, y \in X$ <br>
(2) $(x+y)+z=x+(y+z), \,\forall x, y, z \in X$ <br>
(3) $\exists \, 0 \in X; s.t. \, \forall x\in X, 0+x=x$ <br>
(4) $\forall x \in X, \, \exists -x \in X, s.t. x+(-x)=0$ <br>
(5) $c(x+y)=cx+cy, \forall x,y \in X, c \in F$ <br>
(6) $(c+d)x=cx+dx, \forall x\in X; \forall c, d \in F$ <br>
(7) $c(dx)=(cd)x, \forall x \in X; \forall c,d \in F$ <br>
(8) $1x=x, \forall x \in X$ <br>

**Definition 1.18** 称线性空间 X 为范数空间 (normed linear space)， 若存在一个映射 x \mapsto||x|| ，满足：
(1) $||x|| \ge 0, \forall x \in X, 且 ||x|| = 0 \iff x=0 $ <br>
(2) $||cx||=|c|\cdot ||x||, \forall c \in F, x \in X $ <br>
(3) $||x+y|| \le ||x|| + ||y||, \forall x,y \in X $ <br>
我们可以很简单的就把一个范数空间变成一个度量空间：只需定义 $d(x,y)=||x-y|| $

**Definition 1.19** 接下来我们来定义集合 X 上的一个等价关系 (equivalence relationship)，记为 "$\sim$" :
(1) $x \sim x, \forall x \in X $ <br>
(2) 若 $x \sim y$ ，那么 $y \sim x$ <br> 
(3) 若 $x \sim y, y \sim z$ ，那么 $x \sim z $ <br>

给定一个等价关系, $X$ 可以被写成等价类的无交并, $x,y$ 属于同一个等价类当且仅当 $x \sim y$ 。

**Example 1.20** 令 $X=\mathbb R$ ,定义等价关系 $x\sim y$ 若 $x-y$ 是有理数 （易证这是一个等价关系）

**Definition 1.21** 集合 X 上有一个偏序关系 (partial order), 记作 "$\le$" ，如果满足：
(1) $x \le x, \forall x \in X $ <br>
(2) 若 $x \le y, y \le x $，那么$ x=y $ <br>
注：对于偏序集上任意的 x,y ; x \le y 跟 y \le x 可以同时不成立。例：令 Y 是一个集合， X 是由 Y 的所有子集构成的集合；定义 A \le B \iff A, B \in X; A \subset B。有兴趣还可以了解一下: 全序 (total oder)跟良序 (well order)。 <br>

接下来罗列三个关于实数的结论 <br>

**Proposition 1.22** 任取闭集 $K \subset \mathbb R$, $K$ 是某个有限区间的子集，那么 $K$ 是紧致的 <br>
注：我们后面会讲到，对一般的拓扑空间，紧集的闭子集都是紧致的。反过来：若 $K \in \mathbb R$ 是紧致的，那么 $K$ 是一个闭集。注：这个结论对于 Hausdorff 拓扑空间也成立。 <br>
证：略。

**Proposition 1.23** 任取开集 $G \subset \mathbb R$, 那么 $G$ 可以被写成可数个 (countable) 开区间的无交并 <br>
证：略。注：这个是 Lindelof 引理在 $\mathbb R$ 上的应用。有兴趣的同学可以去查一下：Lindeof 性质指的是集合 A 的任意一个开覆盖都有一个可数子覆盖 (countable subcover)；这个跟紧致集的定义很类似。度量空间 X 拥有Lindelof 性质，当且仅当 $X$ 是可分的 (separable)

**Proposition 1.24** 令 $f: \mathbb R \mapsto \mathbb R$ 是增函数，那么 $\lim_{y\rightarrow x^+}f(y),\lim_{y \rightarrow x^-}f(y)$ 在每一点 $x$ 处都存在；并且 $f$ 不连续出的点集是可数的 <br>
证： 见 14.5 节 Lemma 14.32 (1) 的证明。

最后，写一个Stone-Weierstrass定理应用于度量空间的结论。这个略有提前，Stone-Weierstrass定理会在拓扑章节详细证明，但是在此之前就会用到它（讲傅立叶变换的时候），所以这边先写一下，也暂时不证了。
**Theorem 1.25** 令 $X$ 是一个紧致的度量空间, $\mathcal A$ 是一个由 $X$ 上连续复值函数组成的集合，并且有以下性质： <br>
(1) 若 $f,g \in \mathcal A$，且 $c \in \mathbb C$，那么 $f+g, fg, cf \in \mathcal A$ <br>
(2) 若 $f \in \mathcal A$，那么 $\bar f \in \mathcal A$  <br>
(3) $\forall x \in X, \,\exists f \in \mathcal A, \, st f(x) \ne 0$ 注：我们也称 $\mathcal A$ 在所有 $X$ 的点上都不消失 (vanish at no point of $X$ ) <br>
(4) $\forall x\ne y \in X, \, \exists \, f\in \mathcal A, s.t. f(x) \ne f(y)$ 注：我们也称 $\mathcal A$ 可把点分开 (separate points) <br>
那么， $\mathcal A$ 对映于上确界范数 (supremum norm, 即：$||f||:=\sup_{x \in X}|f(x)|$)的闭 (closure) $\overline {\mathcal A}$ 是 X 上所有连续复值函数组成的集合。用数学语言描述这个结论，就是：对于所有 $X$ 上的连续复值函数 $f$ , 以下结论都成立：<br>
$\forall \varepsilon >0, ~\exists ~g \in \mathcal A ,\, s.t. \, \sup_{x \in X}|f(x)-g(x)| < \varepsilon $ <br>

证：略, 后面讲到拓扑的时候会详细证明一个更一般的结论
上一节: 1.1 一些数学的符号跟定义
下一节: 1.3 集合论的公理
