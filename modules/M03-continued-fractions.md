# M03 · 连分数（Continued Fractions）

拉马努金连分数。连分数是拉马努金最拿手的工具之一，Rogers–Ramanujan 连分数是其中最著名的一个。

## 核心定义

一般连分数记法：

$$b_0 + \frac{a_1}{b_1 + \frac{a_2}{b_2 + \frac{a_3}{b_3 + \cdots}}}$$

## 代表公式

### Rogers–Ramanujan 连分数

$$R(q) = \frac{q^{1/5}}{1 + \frac{q}{1 + \frac{q^2}{1 + \frac{q^3}{1 + \cdots}}}}$$

它满足恒等式（$|q| < 1$）：

$$R(q) = q^{1/5}\,\frac{(q;q^5)_\infty\,(q^4;q^5)_\infty}{(q^2;q^5)_\infty\,(q^3;q^5)_\infty}$$

其中 $(a;q)_\infty$ 为 q-Pochhammer 符号（见 M07）。该连分数与 Rogers–Ramanujan 恒等式（M07）本质上是同一组事实的两种面孔。

## 来源与延伸

- 出处：三本笔记与失落笔记中的连分数条目；Andrews–Berndt《Lost Notebook》Part I（2005）以连分数与 q-级数为重点，共讨论 442 条。
- 关联模块：M07（q-级数恒等式）、M06（模函数常用连分数表示）。

## 待补充

- 逐条收录笔记中的连分数公式（Rogers–Ramanujan 型、e 与 π 相关连分数、收敛性结果），每条注明出处与证明指引。
