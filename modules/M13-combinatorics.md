# M13 · 组合数学（Combinatorics）

组合恒等式，以分拆理论为核心。本模块已从拉马努金专章扩展为**通用组合数学库**：从计数基本原理到二项式恒等式、容斥原理、生成函数、Catalan 数、Stirling 数与分拆恒等式一并收录。

## M13.1 计数基本原理

### 排列与组合

$$P(n, k) = \frac{n!}{(n-k)!}, \qquad C(n, k) = \binom{n}{k} = \frac{n!}{k!\,(n-k)!}$$

### 可重组合（stars and bars）

从 $n$ 类物品中取 $k$ 个（可重复）的种数：

$$\binom{n+k-1}{k}$$

### 多项式系数

$$\binom{n}{k_1, k_2, \dots, k_r} = \frac{n!}{k_1!\,k_2!\cdots k_r!} \qquad (k_1 + \cdots + k_r = n)$$

## M13.2 二项式恒等式

### 二项式定理（Newton）

$$(x+y)^n = \sum_{k=0}^{n} \binom{n}{k} x^k y^{n-k}$$

### 基本求和

$$\sum_{k=0}^{n} \binom{n}{k} = 2^n, \qquad \sum_{k=0}^{n} (-1)^k \binom{n}{k} = 0$$

### Pascal 恒等式

$$\binom{n}{k} = \binom{n-1}{k-1} + \binom{n-1}{k}$$

### Vandermonde 恒等式

$$\sum_{k=0}^{n} \binom{r}{k}\binom{s}{n-k} = \binom{r+s}{n}$$

特别地 $\sum_{k=0}^{n} \binom{n}{k}^2 = \binom{2n}{n}$。

## M13.3 容斥原理与错排

### 容斥原理

$$\left|\bigcup_{i=1}^{n} A_i\right| = \sum_{i} |A_i| - \sum_{i<j} |A_i \cap A_j| + \sum_{i<j<k} |A_i \cap A_j \cap A_k| - \cdots$$

### 错排数

$$D_n = n!\sum_{k=0}^{n} \frac{(-1)^k}{k!}, \qquad D_n \approx \frac{n!}{e}$$

$D_0, D_1, D_2, \dots = 1, 0, 1, 2, 9, 44, 265, \dots$；递推 $D_n = (n-1)(D_{n-1} + D_{n-2})$。

## M13.4 生成函数与 Catalan 数

### 普通生成函数

数列 $\{a_n\}$ 的普通生成函数 $A(x) = \sum_{n\ge0} a_n x^n$；指数生成函数 $\hat{A}(x) = \sum_{n\ge0} a_n x^n/n!$。

### Catalan 数

$$C_n = \frac{1}{n+1}\binom{2n}{n}, \qquad C_0, C_1, C_2, \dots = 1, 1, 2, 5, 14, 42, \dots$$

$$C(x) = \sum_{n=0}^{\infty} C_n x^n = \frac{1-\sqrt{1-4x}}{2x}$$

$$C_{n+1} = \sum_{i=0}^{n} C_i\, C_{n-i}$$

Catalan 数计数：$n+1$ 个因子的加括号方式、$n$ 步 Dyck 路径、$n+2$ 边形的三角剖分。

## M13.5 Stirling 数与 Bell 数

### 第二类 Stirling 数 $S(n, k)$

把 $n$ 元集划分为 $k$ 个非空子集的种数：

$$x^n = \sum_{k=0}^{n} S(n, k)\, x^{\underline{k}}, \qquad S(n, k) = k\,S(n-1, k) + S(n-1, k-1)$$

其中 $x^{\underline{k}} = x(x-1)\cdots(x-k+1)$ 为下降阶乘。

### 第一类 Stirling 数 $s(n, k)$

$$x^{\underline{n}} = \sum_{k=0}^{n} s(n, k)\, x^k, \qquad s(n, k) = s(n-1, k-1) - (n-1)\,s(n-1, k)$$

### Bell 数

$$B_n = \sum_{k=0}^{n} S(n, k), \qquad B_{n+1} = \sum_{k=0}^{n} \binom{n}{k} B_k$$

$B_0, B_1, B_2, \dots = 1, 1, 2, 5, 15, 52, \dots$；指数生成函数 $\sum_{n\ge0} B_n x^n/n! = e^{e^x - 1}$。

## M13.6 分拆恒等式

### 分拆生成函数（见 M05.1）

$$\sum_{n=0}^{\infty} p(n)\, q^n = \prod_{n=1}^{\infty} \frac{1}{1-q^n} = \frac{1}{(q;q)_\infty}$$

### 拉马努金分拆同余式（见 M05.3）

$$\begin{aligned}
p(5n+4) &\equiv 0 \pmod{5} \\
p(7n+5) &\equiv 0 \pmod{7} \\
p(11n+6) &\equiv 0 \pmod{11}
\end{aligned}$$

### Rogers–Ramanujan 恒等式的组合解释（见 M07.4）

相邻部分差至少为 2 的分拆数 = 各部分模 5 余 1 或 4 的分拆数。

### Ferrers 图与共轭（见 M05.6）

分拆成恰好 $k$ 部分的数目 = 分拆成最大部分为 $k$ 的数目。

## M13.7 拉马努金的组合工作

- **分拆同余式**：见 M05.3 与 M13.6，从分拆数表直接观察、再用模形式证明。
- **Rogers–Ramanujan 恒等式**：组合解释见 M07.4；rank 与 crank 的组合证明见 M05.7。
- **q-级数**：生成函数即 q-级数（见 M07）；分拆的组合证明常给出 q-级数恒等式的初等证明。
- **与哈代合作**：分拆渐近工作（见 M12.3）。

## M13.8 待补充

- 逐条收录组合恒等式（含分拆恒等式、Rogers–Ramanujan 型恒等式的组合解释、q-二项式定理相关条目），每条注明出处与证明指引。
- Rook 理论与 Pólya 计数定理的公式表。
