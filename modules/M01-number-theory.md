# M01 · 数论（Number Theory）

素数、整数、除数函数。本模块已从拉马努金专章扩展为**通用数论公式库**：不只拉马努金，欧几里得、欧拉、高斯、黎曼、狄利克雷、哈代、陈景润等数学家的数论公式一并收录。拉马努金本人的数论工作集中在 M01.7。

每条公式标注状态：**已证明**（附证明者与年份）或**未解决**（猜想）。未解决的只陈述、不冒充已证。

## M01.1 算术函数

### 除数函数

$$\sigma_k(n) = \sum_{d \mid n} d^k, \qquad d(n) = \sigma_0(n), \qquad \sigma(n) = \sigma_1(n)$$

若 $n = \prod p_i^{a_i}$，则约数个数：

$$d(n) = \prod_i (a_i + 1)$$

$\sigma_k$ 是积性函数：$\gcd(m, n) = 1$ 时 $\sigma_k(mn) = \sigma_k(m)\sigma_k(n)$。

### Euler 函数

$$\varphi(n) = n \prod_{p \mid n}\left(1 - \frac{1}{p}\right), \qquad \sum_{d \mid n} \varphi(d) = n$$

### Möbius 函数与反演公式

$$\mu(n) = \begin{cases} 0 & n \text{ 不是无平方因子数} \\ (-1)^k & n = p_1 p_2 \cdots p_k \text{（} k \text{ 个不同素数）} \end{cases}$$

$$\sum_{d \mid n} \mu(d) = \begin{cases} 1 & n = 1 \\ 0 & n > 1 \end{cases}$$

**Möbius 反演**（Möbius, 1832）：

$$f(n) = \sum_{d \mid n} g(d) \iff g(n) = \sum_{d \mid n} \mu(d)\, f\left(\frac{n}{d}\right)$$

### Dirichlet 卷积

$$(f * g)(n) = \sum_{d \mid n} f(d)\, g\left(\frac{n}{d}\right)$$

积性函数的 Dirichlet 卷积仍为积性函数；$\mu * 1 = \epsilon$（$\epsilon(1) = 1$，其余为 0）。

### von Mangoldt 函数

$$\Lambda(n) = \begin{cases} \log p & n = p^k \text{（} p \text{ 为素数）} \\ 0 & \text{其他} \end{cases}, \qquad \sum_{d \mid n} \Lambda(d) = \log n$$

Chebyshev 函数：$\psi(x) = \sum_{n \le x} \Lambda(n)$，素数定理等价于 $\psi(x) \sim x$。

### Liouville 函数

$$\lambda(n) = (-1)^{\Omega(n)}, \qquad \sum_{d \mid n} \lambda(d) = \begin{cases} 1 & n \text{ 为完全平方数} \\ 0 & \text{其他} \end{cases}$$

其中 $\Omega(n)$ 为 $n$ 的素因子个数（计重数）。

### Jacobi 四平方定理

$n$ 表为四个平方和的方式数（计顺序与符号）$r_4(n)$ 满足：

$$r_4(n) = 8\sigma(n) - 32\sigma\left(\frac{n}{4}\right)$$

其中 $4 \nmid n$ 时 $\sigma(n/4) = 0$。

## M01.2 素数分布

### Euclid 定理

素数有无穷多个（Euclid，《几何原本》第九卷命题 20）。

### 素数定理（Hadamard、de la Vallée Poussin，1896）

$$\pi(x) \sim \frac{x}{\log x} \sim \mathrm{Li}(x) = \int_2^x \frac{dt}{\log t}$$

其中 $\pi(x)$ 为不超过 $x$ 的素数个数。

### Chebyshev 界（Chebyshev，1850）

$$0.92129\,\frac{x}{\log x} < \pi(x) < 1.1056\,\frac{x}{\log x} \qquad (x \text{ 充分大})$$

### Bertrand 假设（Bertrand 猜想，Chebyshev 1850 年证明）

对一切 $n > 1$，存在素数 $p$ 满足 $n < p < 2n$。

### Dirichlet 定理（Dirichlet，1837）

$\gcd(a, d) = 1$ 时，等差数列 $a, a+d, a+2d, \dots$ 中有无穷多个素数。

### Mertens 第二定理（Mertens，1874）

$$\sum_{p \le x} \frac{1}{p} = \log\log x + M + o(1), \qquad M \approx 0.261497$$

$M$ 为 Meissel–Mertens 常数。

### 孪生素数猜想（未解决）

有无穷多对素数 $(p, p+2)$。Brun 定理（Brun，1919）只证明了孪生素数倒数和收敛：

$$\sum_{p,\, p+2 \text{ 均为素数}} \left(\frac{1}{p} + \frac{1}{p+2}\right) < \infty$$

### Sophie Germain 素数

$p$ 与 $2p+1$ 同时为素数时，称 $p$ 为 Sophie Germain 素数。是否有无穷多个，未解决。

### Mersenne 素数

$2^p - 1$ 为素数时，$p$ 本身必为素数；反之不成立。完全数与 Mersenne 素数一一对应（见 M01.5）。

### AKS 素性测试（Agrawal–Kayal–Saxena，2002）

存在确定性多项式时间算法判定一个数是否为素数。

## M01.3 zeta 函数与 L 函数

### Riemann zeta 函数

$$\zeta(s) = \sum_{n=1}^{\infty} \frac{1}{n^s} = \prod_{p} \frac{1}{1 - p^{-s}} \qquad (\operatorname{Re} s > 1)$$

右端为 Euler 乘积，$p$ 取遍全部素数。

### 特殊值（Euler，1734）

$$\zeta(2) = \frac{\pi^2}{6}, \qquad \zeta(4) = \frac{\pi^4}{90}$$

$\zeta(3)$ 为无理数（Apéry，1978），$\zeta(3)$ 是否为超越数未解决。

### 函数方程（Riemann，1859）

$$\zeta(s) = 2^s \pi^{s-1} \sin\left(\frac{\pi s}{2}\right) \Gamma(1-s)\, \zeta(1-s)$$

### 显式公式（Riemann–von Mangoldt）

$$\psi(x) = x - \sum_{\rho} \frac{x^{\rho}}{\rho} - \log 2\pi - \frac{1}{2}\log\left(1 - x^{-2}\right)$$

其中 $\rho$ 取遍 $\zeta$ 的全部非平凡零点（$x$ 不取素数幂时成立）。素数的分布就藏在零点 $\rho$ 的位置里。

### Riemann 猜想（未解决，千禧难题）

$\zeta$ 的全部非平凡零点都满足 $\operatorname{Re} s = 1/2$。

### Dirichlet L 函数

$$L(s, \chi) = \sum_{n=1}^{\infty} \frac{\chi(n)}{n^s}$$

其中 $\chi$ 为 Dirichlet 特征。Dirichlet 用 $L(1, \chi) \ne 0$ 证明了等差数列中的素数定理（M01.2）。广义 Riemann 猜想（GRH）断言全部 Dirichlet L 函数的非平凡零点也在临界线上，未解决。

## M01.4 同余与二次互反律

### Fermat 小定理（Fermat，1640）

$p$ 为素数、$p \nmid a$ 时：

$$a^{p-1} \equiv 1 \pmod p$$

### Euler 定理（Euler，1736）

$\gcd(a, n) = 1$ 时：

$$a^{\varphi(n)} \equiv 1 \pmod n$$

### Wilson 定理（Wilson，1770；Lagrange 证明）

$p$ 为素数时：

$$(p-1)! \equiv -1 \pmod p$$

### 中国剩余定理（孙子定理）

$m_1, \dots, m_k$ 两两互素时，同余方程组

$$x \equiv a_i \pmod{m_i} \quad (i = 1, \dots, k)$$

在模 $m_1 m_2 \cdots m_k$ 意义下有唯一解。

### 二次互反律（Euler、Legendre；Gauss 1796 年首个完整证明）

$p, q$ 为不同奇素数时：

$$\left(\frac{p}{q}\right)\left(\frac{q}{p}\right) = (-1)^{\frac{p-1}{2}\cdot\frac{q-1}{2}}$$

其中 $\left(\frac{a}{p}\right)$ 为 Legendre 符号：$a$ 为模 $p$ 二次剩余时取 $1$，非剩余时取 $-1$，$p \mid a$ 时取 $0$。

补充律：

$$\left(\frac{2}{p}\right) = (-1)^{\frac{p^2-1}{8}}, \qquad \left(\frac{-1}{p}\right) = (-1)^{\frac{p-1}{2}}$$

### Euler 判别法

$$a^{\frac{p-1}{2}} \equiv \left(\frac{a}{p}\right) \pmod p$$

## M01.5 丢番图方程与经典定理

### 勾股数组（Euclid 公式）

本原勾股数组（$\gcd(a, b, c) = 1$）可表为：

$$a = m^2 - n^2, \qquad b = 2mn, \qquad c = m^2 + n^2$$

其中 $m > n$，$\gcd(m, n) = 1$，$m, n$ 一奇一偶。

### 两平方和定理（Fermat，1640；Euler 证明）

素数 $p$ 可表为两平方和当且仅当 $p = 2$ 或 $p \equiv 1 \pmod 4$：

$$p = x^2 + y^2 \iff p = 2 \text{ 或 } p \equiv 1 \pmod 4$$

### 四平方和定理（Lagrange，1770）

每个自然数都是四个整数平方之和。个数公式见 M01.1 的 Jacobi 四平方定理。

### Waring 问题

$g(k)$ 为使每个自然数都可表为 $g(k)$ 个 $k$ 次幂之和的最小个数：

$$g(2) = 4, \qquad g(3) = 9, \qquad g(4) = 19$$

$g(2) = 4$ 即 Lagrange 四平方定理。

### Fermat 大定理（Fermat 猜想 1637；Wiles 1994 年证明、1995 年发表）

$n > 2$ 时，$x^n + y^n = z^n$ 没有正整数解。

### Catalan 猜想（Mihăilescu 定理，2002）

大于 1 的连续幂只有一组：

$$3^2 - 2^3 = 1$$

### 完全数（Euclid–Euler 定理）

偶完全数与 Mersenne 素数一一对应：

$$n = 2^{p-1}(2^p - 1) \text{ 为完全数} \iff 2^p - 1 \text{ 为素数}$$

奇完全数是否存在，未解决。

### Ramanujan–Nagell 方程（详见 M14）

$$x^2 + 7 = 2^n$$

整数解只有 $n = 3, 4, 5, 7, 15$（Nagell 1948 年证明这就是全部）。

## M01.6 加性数论与猜想

### Goldbach 猜想（未解决）

每个大于 2 的偶数都是两个素数之和。弱 Goldbach 猜想（每个大于 5 的奇数是三个素数之和）已由 Helfgott 于 2013 年证明。

### Chen 定理（陈景润，1973）

每个充分大的偶数都可表为一个素数与一个素数或两个素数之积之和。

### 三立方和问题

$x^3 + y^3 + z^3 = 33$ 与 $= 42$ 的整数解分别于 2019 年由 Booker（33）与 Booker–Sutherland（42）找到；此前 33 与 42 是 100 以内仅剩的两个未知数。

### abc 猜想（未解决）

对互素正整数 $a + b = c$，$c$ 的大小受 $a, b, c$ 的不同素因子乘积控制（精确表述用根基 radical）。望月新一 2012 年的证明未获学界公认。

## M01.7 拉马努金的数论

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

## M01.8 待补充

- 代数数论：Dedekind zeta 函数、类数公式、单位定理。
- 解析数论进阶：Bombieri–Vinogradov 定理、零点密度估计、筛法（Selberg 筛、Brun 筛）。
- 椭圆曲线：Mordell 定理、BSD 猜想（与 M11 互链）。
- 计算数论：Miller–Rabin 素性测试、Pollard rho 分解、数域筛法。
- 拉马努金笔记中的数论条目：按 Berndt 五卷条目号逐条收录（与 M01.1–M01.6 的通用公式互链，不重复抄录）。
