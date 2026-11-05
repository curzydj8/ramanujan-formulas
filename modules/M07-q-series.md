# M07 · q-级数（q-Series）

q-级数恒等式。q-级数是拉马努金笔记与失落笔记中占比最大的主题，也是 mock theta 函数（M08）与分拆理论（M13）的基础。

## 核心定义

q-Pochhammer 符号（$|q| < 1$）：

$$(a;q)_n = \prod_{k=0}^{n-1} (1 - a q^k), \qquad (a;q)_\infty = \prod_{k=0}^{\infty} (1 - a q^k)$$

## 代表公式

### Jacobi 三重积

$$\sum_{n \in \mathbb{Z}} q^{n^2} z^n = \prod_{m=1}^{\infty} (1 - q^{2m})(1 + z q^{2m-1})(1 + z^{-1} q^{2m-1})$$

### Rogers–Ramanujan 恒等式

$$\sum_{n=0}^{\infty} \frac{q^{n^2}}{(q;q)_n} = \frac{1}{(q;q^5)_\infty (q^4;q^5)_\infty}$$

$$\sum_{n=0}^{\infty} \frac{q^{n^2+n}}{(q;q)_n} = \frac{1}{(q^2;q^5)_\infty (q^3;q^5)_\infty}$$

## 来源与延伸

- 出处：三本笔记与失落笔记均有大量 q-级数条目；Andrews–Berndt《Lost Notebook》Part I（2005）前 442 条以连分数与 q-级数为重点。
- 关联模块：M08（mock theta 函数是 q-级数的特殊一支）、M13（分拆生成函数）、M11（模形式与 theta 函数）。

## 待补充

- 按 Berndt 五卷与失落笔记五卷的条目号，逐条收录 q-级数恒等式（含 Rogers–Ramanujan 型、Watson 变换、Bailey 引理相关条目），每条注明出处与证明指引。
