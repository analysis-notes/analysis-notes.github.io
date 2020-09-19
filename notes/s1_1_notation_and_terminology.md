# 1.1 一些数学的符号跟定义
## 分析常用的几个符号

$\forall$ 表示：“任取”，“对所有”

$\exists$ 表示：“存在(至少一个)“

$s.t. (\text{such that})$ 表示：“导致，以至于，满足，使得”

$\iff$ 表示：“定义，等价，一回事儿”


## 一些集合论的基本符号跟定义

$A^C=\{x \in X: x\notin A\}$

$A-B=A \cap B^C$

$A\Delta B=(A-B) \cup (B-A)$，也叫对称差 (symmetric difference)

## 罗列一些定义

令 $I$ 为非空指数集 (index set)， 集合系 $\\{A_{\alpha}\\}\_{\alpha \in I}$ 称为不相交 (disjoint)，如果 $A_{\alpha} \cap A_{\beta} = \emptyset, \forall \alpha \ne \beta$ 

把 $A_1 \subset A_2 \subset A_3 \ldots$  记作 $A_i \uparrow$ ；如果 $A_1 \subset A_2 \subset A_3 \ldots$，且 $A=\cup_{i=1}^\infty A_i$ ，则记为 $A_i \uparrow A$

把 $A_1 \supset A_2 \supset \ldots$ 记为 $A_i \downarrow$；若 $A_1 \supset A_2 \supset \ldots$，且 $A = \cap_{i=1}^\infty A_i$，则记为 $A_i \downarrow A$ 

$\mathbb N$ 为整数集，$\mathbb Q$ 为有理数集， $\mathbb R$ 为实数集，$\mathbb C$ 为复数集

$\Re$ 表示取复数的实部，$\Im$ 表示取复数的虚部

$x \vee y = \max(x,y) , x\wedge y = \min(x,y) $

对于 $x \in \mathbb R, x^+=x \vee 0, x^- =(-x) \vee 0, x=x^+-x^- $

对于 $z \in \mathbb C, \overline {z}$ 为 $z$ 的共轭 (conjugate)：令 $z=a+ib$ ，其中 $a,b \in \mathbb R$ , 则 $\overline{z}=a-ib$

映射的复合：$f \circ g(x) = f(g(x))$ 

若 $f$ 的定义域为实数，或者实数的某个子集，那么 $f(x^+)=\lim_{y \rightarrow x^+} f(y),~ f(x^-)=\lim_{y\rightarrow x^-}f(y)$ 分别称为 $f$ 在 $x$ 处的右极限 (right limit)跟左极限 (left limit)

增函数 (increasing): $f: \mathbb R \rightarrow \mathbb R$，若 $x <y$ ， 那么 $f(x) \le f(y) $

严格增函数 (strict increasing): $f: \mathbb R \rightarrow \mathbb R$ ，若 $x < y$ ，那么 $f(x) < f(y) $

类似可定义减函数 (decreasing), 严格减函数 (strict decreasing)

增函数跟减函数统称为单调函数

给定一个实数序列 $\{a_n\}$ :

 $\limsup_{n\rightarrow \infty} a_n=\inf_n \sup _{m\ge n} a_m$,
 
 $\liminf_{n\rightarrow \infty} a_n=\sup_n \inf _{m\ge n} a_m$
 
举个例子：若

$a_n= \begin{cases} 1,  n 偶数 \\\\ -1/n, n 奇数 \end{cases} $

那么 $\limsup_{n\rightarrow \infty}a_n=1, \liminf_{n\rightarrow \infty}a_n=0. $ 

注意：这两个都是序列的极限行为，一个是上限，一个是下限；这个上下限都跟序列任何前有限项无关，而必须是是往后无限次都会出现才行

序列 $\{a_n\}$ 的极限 (limit)存在，当且仅当 $\limsup_{n\rightarrow \infty}a_n=\liminf_{n\rightarrow \infty}a_n$ ,且它们都不为无穷大

我们可以拓展类似的定义到连续的情况：

$\limsup_{y\rightarrow x}f(y) = \inf_{\delta > 0} \sup_{|y-x| < \delta}f(y) $

上一节: 第一章、预备知识

下一节: 1.2 数学分析中的基础定义及定理


