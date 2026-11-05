# M01 · 数论（Number Theory）

素数、整数、除数函数。拉马努金是 20 世纪最伟大的数论学家之一，笔记中数论条目贯穿始终。

## 核心定义

除数函数（$n$ 的正约数）：

$$\sigma_k(n) = \sum_{d \mid n} d^k, \qquad d(n) = \sigma_0(n), \qquad \sigma(n) = \sigma_1(n)$$

## 代表公式

### Ramanujan tau 函数

$$\Delta(q) = q \prod_{n=1}^{\infty} (1-q^n)^{24} = \sum_{n=1}^{\infty} \tau(n)\, q^n$$

$\tau(n)$ 即 Ramanujan tau 函数，$\Delta$ 是权为 12 的尖点模形式（见 M06）。

### Ramanujan 同余式（1916）

$$\tau(n) \equiv \sigma_{11}(n) \pmod{691}$$

### Ramanujan 猜想（1916，Deligne 1974 年证明）

$$|\tau(p)| \le 2p^{11/2} \qquad (p \text{ 为素数})$$

这是 Weil 猜想的一部分，Deligne 凭此相关工作获 Fields 奖。

### Ramanujan 素数

第 $n$ 个 Ramanujan 素数 $R_n$ 是满足「对一切 $x \ge R_n$ 都有 $\pi(x) - \pi(x/2) \ge n$」的最小素数，其中 $\pi(x)$ 为素数计数函数。这是拉马努金对 Bertrand 假设的推广。

## 来源与延伸

- 出处：三本笔记中的数论条目；与哈代合作的论文。
- 关联模块：M05（分拆函数的同余方法）、M06（tau 函数即模形式）、M13（组合数论）。

## 待补充

- 逐条收录笔记中的数论公式（素数分布、除数函数恒等式、Bernoulli 数相关结果），每条注明出处与证明指引。
