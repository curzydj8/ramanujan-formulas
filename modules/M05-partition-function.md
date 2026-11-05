# M05 · 分拆函数（Partition Function）

整数分拆与同余关系。本模块已从拉马努金专章扩展为**通用分拆函数库**：从 Euler 的五边形数定理到 Rademacher 精确公式，生成函数、递推、同余式、渐近、rank 与 crank 一并收录。分拆理论是拉马努金与哈代合作的中心课题。

## M05.1 定义与生成函数

### 定义

$n$ 的分拆数 $p(n)$ 是把 $n$ 写成正整数之和的方法数（不计顺序），约定 $p(0) = 1$。

$$p(0), p(1), p(2), \dots = 1, 1, 2, 3, 5, 7, 11, 15, 22, 30, 42, \dots$$

例如 $4$ 的分拆：$4$、$3+1$、$2+2$、$2+1+1$、$1+1+1+1$，共 $p(4) = 5$ 种。

### 生成函数（Euler）

$$\sum_{n=0}^{\infty} p(n)\, q^n = \prod_{n=1}^{\infty} \frac{1}{1-q^n} = \frac{1}{(q;q)_\infty}$$

其中 $(q;q)_\infty$ 为 q-Pochhammer 符号（见 M07）。

### 受限分拆的生成函数

$$\sum_{n=0}^{\infty} p_{\le k}(n)\, q^n = \frac{1}{(q;q)_k} = \frac{1}{(1-q)(1-q^2)\cdots(1-q^k)}$$

其中 $p_{\le k}(n)$ 为最大部分不超过 $k$ 的分拆数；由共轭分拆（M05.6）可知它也等于恰好 $k$ 部分以下的分拆数。

## M05.2 Euler 五边形数定理与递推

### 五边形数定理（Euler，1750）

$$\prod_{n=1}^{\infty} (1-q^n) = \sum_{k=-\infty}^{\infty} (-1)^k q^{k(3k-1)/2}$$

广义五边形数 $k(3k-1)/2$（$k = \pm 1, \pm 2, \dots$）依次为 $1, 2, 5, 7, 12, 15, 22, 26, \dots$。

### $p(n)$ 的递推公式

$$p(n) = p(n-1) + p(n-2) - p(n-5) - p(n-7) + p(n-12) + p(n-15) - \cdots$$

即对广义五边形数 $g_k$ 求和，符号按 $+, +, -, -, +, +, \dots$ 交替（约定 $p(0) = 1$，$p(m) = 0$ 当 $m < 0$）。这是实际计算 $p(n)$ 的经典方法。

## M05.3 拉马努金分拆同余式

### 三大同余式（Ramanujan，1919）

$$\begin{aligned}
p(5n+4) &\equiv 0 \pmod{5} \\
p(7n+5) &\equiv 0 \pmod{7} \\
p(11n+6) &\equiv 0 \pmod{11}
\end{aligned}$$

拉马努金从分拆数表里直接观察到这三条规律并给出证明；其中模 11 的一条证明最为艰深。

### 后续推广（Ono，2000）

对每个素数 $m \ge 5$，都存在无穷多个 $n$ 使得 $p(n) \equiv 0 \pmod{m}$。

## M05.4 渐近与精确公式

### Hardy–Ramanujan 渐近公式（1917–1918）

$$p(n) \sim \frac{e^{\pi\sqrt{2n/3}}}{4n\sqrt{3}} \qquad (n \to \infty)$$

哈代与拉马努金的圆法（circle method）由此诞生，是解析数论的里程碑；详见 M12。

### Rademacher 精确公式（Rademacher，1937）

$$p(n) = \frac{1}{\pi\sqrt{2}} \sum_{k=1}^{\infty} A_k(n)\, \sqrt{k}\, \frac{d}{dn}\left[\frac{\sinh\left(\frac{\pi}{k}\sqrt{\frac{2}{3}\left(n-\frac{1}{24}\right)}\right)}{\sqrt{n-\frac{1}{24}}}\right]$$

其中 $A_k(n)$ 为 Kloosterman 型和。这是收敛的精确级数：取前几项就能算出 $p(n)$ 的整数值。

### 一个著名数值

$$p(200) = 3972999029388$$

哈代与拉马努金用递推与渐近公式算出此值，验证了渐近公式的精度。

## M05.5 分拆类型

### 不同部分的分拆 = 奇部分的分拆（Euler）

$$\prod_{k=1}^{\infty} (1+q^k) = \prod_{k=1}^{\infty} \frac{1}{1-q^{2k-1}}$$

左端是分拆成互不相同部分的生成函数，右端是分拆成奇数的生成函数；两者相等。

### Rogers–Ramanujan 恒等式

$$\sum_{n=0}^{\infty} \frac{q^{n^2}}{(q;q)_n} = \frac{1}{(q;q^5)_\infty (q^4;q^5)_\infty}$$

$$\sum_{n=0}^{\infty} \frac{q^{n^2+n}}{(q;q)_n} = \frac{1}{(q^2;q^5)_\infty (q^3;q^5)_\infty}$$

左端是带受限条件的分拆生成函数，右端是模 5 余数类的乘积；详见 M07。

### q-二项式系数（Gaussian 二项式）

$$\binom{n}{k}_q = \frac{(q;q)_n}{(q;q)_k\,(q;q)_{n-k}}$$

它是「至多 $k$ 部分、最大部分至多 $n-k$ 的分拆」的生成函数；$q \to 1$ 时退化为普通二项式系数。

## M05.6 Ferrers 图与共轭分拆

分拆 $\lambda = (\lambda_1 \ge \lambda_2 \ge \cdots)$ 的 Ferrers 图是 $\lambda_i$ 个点排成的左对齐行；沿主对角线翻转得到**共轭分拆** $\lambda'$。共轭是一一对应，由此得到：

- $n$ 分拆成恰好 $k$ 部分的数目 = $n$ 分拆成最大部分为 $k$ 的数目；
- $n$ 分拆成至多 $k$ 部分的数目 = $n$ 分拆成部分不超过 $k$ 的数目。

自共轭分拆（$\lambda = \lambda'$）的数目等于 $n$ 分拆成互不相同的奇数的数目。

## M05.7 rank 与 crank

### Dyson 的 rank（Dyson，1944）

$$\mathrm{rank}(\lambda) = \lambda_1 - \ell(\lambda)$$

即最大部分减去部分个数。Dyson 猜想 rank 能组合地解释模 5 与模 7 的同余式（Atkin–Swinnerton-Dyer，1954 年证明）。

### crank（Andrews–Garvan，1988）

crank 是为解释模 11 同余式而引入的统计量：若分拆含 1，则 crank 为大于 1 的部分个数减去 1 的个数；否则 crank 为最大部分。Andrews 与 Garvan 证明 crank 在模 11 的剩余类上均匀分布，从而组合地解释了 $p(11n+6) \equiv 0 \pmod{11}$。

## M05.8 拉马努金的分拆工作

- **1919 年同余式**：见 M05.3，从分拆数表直接观察、再用模形式证明。
- **1917–1918 年渐近公式**：与哈代合作，圆法的起点（M05.4）。
- **分拆数表**：拉马努金手算大量 $p(n)$ 值，$p(200) = 3972999029388$ 是其中最著名的一个。
- **mock theta 与分拆**：失落笔记中的 mock theta 函数与分拆生成函数密切相关（见 M08）。

## M05.9 待补充

- Ramanujan 同余式的模形式证明思路（与 M06 互链）。
- 更多受限分拆：平面分拆（MacMahon 公式）、分拆成平方数。
- 分拆与表示论、统计力学的联系。
