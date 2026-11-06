# Part I · 第 5 章 Eulerian Polynomials and Numbers, Bernoulli Numbers, and the Riemann Zeta-Function（Eulerian 多项式与数、Bernoulli 数与 Riemann zeta 函数）

出处：Bruce C. Berndt, *Ramanujan's Notebooks*, Part I, Springer, 1985, 第 5 章，pp. 109–132（第 4 章 pp. 85–108；第 6 章起自 p. 133）。对应拉马努金**第二本笔记第 5 章**。

## 背景与记号

- 本章是全书数论含量最高的一章。Berndt 在章首写道：本章 94 条公式或定理陈述中，绝大多数关于 Bernoulli 数、Euler 数、Eulerian 多项式与数以及 Riemann zeta 函数。拉马努金的第一篇论文 [4]（Bernoulli 数）与第四篇论文 [7]（与 Riemann zeta 函数有关的和）的起源都在本章。Bernoulli 数的大多数结果见于标准教科书（Bromwich [1]、Nielsen [5]、Nörlund [2]、Uspensky–Heaslet [1]）；Eulerian 多项式与数的结果则大多不为人熟知，其中拉马努金的一些定理看来是新的，证明又很短，Berndt 因此给出大多数证明。
- **Eulerian 多项式** $\psi_n(p)$（$0 \le n < \infty$，$p \ne -1$）按拉马努金的记号由下式定义：
$$\frac{1}{e^x + p} = \sum_{n=0}^{\infty} \frac{(-1)^n \psi_n(p) x^n}{n! (p+1)^{n+1}}, \qquad |x| < |\mathrm{Log}(-p)|. \qquad (0.1)$$
下文将证明 $\psi_n(p)$ 确为 $p$ 的 $n-1$ 次多项式。Carlitz 的记号中 $R_n[-p] = \psi_n(p)$。**Eulerian 数** $A_{nk}$（$1 \le k \le n$）一般由 $\psi_n(p) = \sum_{k=1}^n A_{nk}(-p)^{k-1}$ 定义；$A_{nk}$ 等于 $\{1, 2, \dots, n\}$ 的恰有 $k$ 个上升（含左端约定的一个）的排列数。拉马努金的记号是 $A_{nk} = F_k(n)$，见 (6.1)。Eulerian 多项式与数由 Euler [1] 于 1755 年首先引入。
- **Bernoulli 数** $B_n$ 用当代定义（见下文 Entry 9 与导言 (I1)）：$B_1 = -1/2$，$B_{2k+1} = 0$（$k \ge 1$）。**Euler 数** $E_n$ 用当代定义（导言 (I2)）：$\sec x = \sum_{n=0}^{\infty} (-1)^n E_{2n} x^{2n}/(2n)!$，$|x| < \pi/2$，$E_{2n+1} = 0$；即 $E_0 = 1$、$E_2 = -1$、$E_4 = 5$、$E_6 = -61$、$E_8 = 1385$、$E_{10} = -50521$、$E_{12} = 2702765$、$E_{14} = -199360981$。两种记号都与拉马努金本人的约定不同，Berndt 在导言中已说明。
- 记号：$\zeta(s) = \sum_{n=1}^{\infty} n^{-s}$（$\mathrm{Re}\, s > 1$），拉马努金记作 $S_k = \zeta(k)$；$\lambda(s) = \sum_{k=0}^{\infty} (2k+1)^{-s}$（$\mathrm{Re}\, s > 1$）；$\eta(s) = \sum_{k=1}^{\infty} (-1)^{k+1} k^{-s}$（$\mathrm{Re}\, s > 0$）；$L(s) = \sum_{k=0}^{\infty} (-1)^k (2k+1)^{-s}$（Dirichlet beta 函数）。$B_s^*$、$E_s^*$ 为拉马努金推广到任意实指标的 Bernoulli 数与 Euler 数，见 Entry 25 之后。$\gamma$ 为 Euler 常数（拉马努金记作 $c$）。
- 本章在原文中明确出现编号的 Entry 共 **30 条**：Entry 1–30（Entry 1、2、6、19 各分 (i)(ii)(iii)，Entry 23、24 各分 (i)–(iv)）。Berndt 章首计数：本章共 **94 条公式或定理陈述**。IMSC 整理表计本章的结果数本次未能读取（imsc.res.in 当日不可达），待补。
- **本章的拉马努金原文疏失**（Berndt 已指出，详见各条与末尾小结）：Entry 6(ii) 在笔记中的表述有误（见该条）；Entry 7 的 (7.2)「取整部分」说法含糊（$\psi_n(x-1)$ 一般不是整数）；第 12 节后例 1 右端 $-1/2$ 应为 $1/2$；Entry 19(ii) 加强断言（商为素数）不成立（$B_{22}$ 的分子 $854513 = 11 \cdot 131 \cdot 593$）；Entry 20 后例 1 用 $B_{22}$ 的推理有误（同上）；Entry 29 被拉马努金本人划去（$c_{21} = 30 \ne 31 = d_{21}$）；Entry 30 后推论 3 被拉马努金本人划去（$p_n/n = \mathrm{Log}\, n + \mathrm{Log\, Log}\, n + O(1)$）；$\zeta(n)$ 表（p. 127）有五处末位数字错误（见 Entry 26 后）。

## 本章结构

| Entry | 页 | 内容 |
|---|---|---|
| Entry 1(i)(ii) | 110 | 差分方程 $f(x+h) \mp f(x) = h\varphi'(x)$ 的展开系数 $a_n = B_n/n!$、$(1-2^n)B_n/n!$ |
| Entry 2(i)(ii) | 111–112 | $f(x+1) \mp f(x-1) = 2\varphi'(x)$、$2\varphi(x)$ 的多项式解（$F_{2n+1}$，(2.1)–(2.3)） |
| Entry 3 | 113 | $f(x+h) + pf(x) = \varphi(x)$ 的系数 $a_n = (-1)^n\psi_n(p)/(n!(p+1)^{n+1})$ |
| Entry 4 | 113 | $(p+1)^{-n-1}\psi_n(p) = \sum_{k=0}^{\infty} (k+1)^n(-p)^k$ (4.1) |
| Entry 5 | 113–114 | $\psi_0(p) = 1$；递推 (5.1)(5.2)；$\psi_n(p)$ 为 $n-1$ 次多项式 |
| Entry 6(i)(ii)(iii) | 114–115 | Eulerian 数 $F_r(n)$ 的对称性与求和恒等式 |
| Entry 7 | 115 | $\psi_n(x-1)$ 的对数展开 (7.1)；拉马努金版 (7.2) |
| Entry 8 | 116–119 | $\psi_n(-1) = n!$、$\psi_n(1)$ 公式；$\psi_0,\dots,\psi_7$；递推 (8.1)；推论 1–6 |
| Entry 9 | 119 | Bernoulli 数的定义 (I1) |
| Entry 10 | 119 | $h/(e^h+1)$ 的展开（(1.3) 右端） |
| Entry 11 | 119–120 | $\mathrm{Log}(x/(e^x-1))$ 的 Bernoulli 级数 |
| Entry 12 | 120 | $\mathrm{Log}(2/(e^x+1))$ 的 Bernoulli 级数 |
| §12 例 1–3 | 120–121 | 三个近似式（$P, Q, R, S, T$ 的倒数和） |
| Entry 13 | 121 | $x\cot x$ 的 Bernoulli 级数 |
| Entry 14 | 121 | $x\csc x$ 的 Bernoulli 级数 |
| Entry 15 | 121 | $x\tan x$ 的 Bernoulli 级数 |
| Entry 16 | 122 | $\mathrm{Log}(x/\sin x)$ 的 Bernoulli 级数 |
| Entry 17 | 122 | $\mathrm{Log}(\sec x)$ 的 Bernoulli 级数 |
| Entry 18 | 122 | Euler 递推 $-(2n+1)B_{2n} = \sum \binom{2n}{2k} B_{2k}B_{2n-2k}$ |
| Entry 19(i)(ii)(iii) | 122–123 | $2(2^{2n}-1)B_{2n}$ 为整数；Adams 定理；von Staudt–Clausen 定理 |
| Entry 20 | 123 | von Staudt–Clausen 的另一形式；$I_{2n}$ 表 |
| §20 例 1–2 | 123 | $B_{22}$ 的计算（推理有误）；$B_{200}$ 的分数部分 |
| Entry 21 | 123–124 | 两张素数表（至 211、至 4969） |
| Entry 22 | 124 | $2^{2n}(2^{2n}-1)B_{2n}$ 与 Euler 数的恒等式；$E_{2n}$（$0 \le n \le 7$） |
| Entry 23(i)–(iv) | 124 | $\cot(\pi x)$、$\tan(\pi x/2)$、$\csc(\pi x)$、$\sec(\pi x/2)$ 的部分分式分解 |
| Entry 24(i)–(iv) | 124 | $\coth(\pi x)$、$\tanh(\pi x/2)$、$\mathrm{csch}(\pi x)$、$\mathrm{sech}(\pi x/2)$ 的部分分式分解 |
| §24 注记 | 124 | $E_{4n} \equiv 5 \pmod{60}$ 等同余式；$E_{2n+2h}/E_{2n}$ 渐近 |
| Entry 25(i)–(iv) | 125–126 | $\zeta(2n)$、$\lambda(2n)$、$\eta(2n)$、$L(2n-1)$ 的 Euler 公式；$B_s^*$、$E_s^*$ |
| Entry 26 | 126–128 | $f(a) = \sum (a+bk)^{-n}$ 的渐近 (26.1)；$\zeta(n)$ 例与数值表；推论 1–2 |
| Entry 27 | 128 | 素数上的一般乘积 $\prod_p (1-a_p)^{-1}$ |
| Entry 28 | 128–129 | $\zeta(s)$ 的 Euler 乘积；推论 1–5；例 1–3 |
| Entry 29 | 130 | $\prod (1-x^{p_k})^{-1}$ 的恒等式（被划去，不成立）；Ramanujan 对 |
| Entry 30 | 131–132 | 素数上的一般乘积 $\prod_p (1+a_p)$；推论 1–3（素数倒数和发散等） |

## Entry 1(i)——差分方程的展开系数（Bernoulli 数）

**陈述。**在 Entry 1(i)、1(ii) 与 Entry 3 中假设：$|h|$ 充分小时，$f$ 可展成
$$f(x) = \sum_{n=0}^{\infty} a_n h^n \varphi^{(n)}(x), \qquad (1.1)$$
其中 $a_n$（$0 \le n < \infty$）与 $\varphi$ 无关。**Entry 1(i)：**设 $f(x+h) - f(x) = h\varphi'(x)$，则按 (1.1) 的记号，$a_n = B_n/n!$（$0 \le n < \infty$），其中 $B_n$ 为第 $n$ 个 Bernoulli 数。

**出处。**Berndt Part I, Ch. 5, Entry 1(i), pp. 109–110。

**状态。**已证明（取 $\varphi(x) = e^x$，由 (1.1) 得 $\sum a_n h^n = h/(e^h-1)$，与 (I1) 比较即得）。注：若 $f$ 是 Entry 1(i) 或 1(ii) 的差分方程的解，则 (1.1) 右端的级数一般发散；Nörlund [2, pp. 58–60] 证明在适当条件下它在 $h \to 0$ 时渐近地表示该函数。

**对照。**Bernoulli 数的生成函数见 M01（**本条即 M01 缺失的 Bernoulli 数定义所由来的条目**，见文末「与 M 模块对照」）；差分方程与 Euler–Maclaurin 公式见 M12。

## Entry 1(ii)——差分方程的展开系数（$1-2^n$ 因子）

**陈述。**设 $f(x+h) + f(x) = h\varphi'(x)$，则 $a_n = (1-2^n)B_n/n!$（$0 \le n < \infty$）。

**出处。**Berndt Part I, Ch. 5, Entry 1(ii), p. 110。

**状态。**已证明（取 $\varphi(x) = e^x$，得 $\sum a_n h^n = h/(e^h+1) = h/(e^h-1) - 2h/(e^{2h}-1)$，展开即得 (1.3)）。数值复核（精确分数）：$n = 2$ 时 $a_2 = (1-4)(1/6)/2 = -1/4$；$n = 4$ 时 $a_4 = (1-16)(-1/30)/24 = 1/48$。

**对照。**见 Entry 1(i)；$h/(e^h+1)$ 的展开即 Entry 10。

## Entry 2(i)——$f(x+1) - f(x-1) = 2\varphi'(x)$ 的多项式解

**陈述。**设 $\varphi$ 为定义在 $(-\infty, \infty)$ 上的任意函数，$n$ 为非负整数，定义
$$F_{2n+1}(x) = \varphi(x) + \sum_{k=1}^n (-1)^k \frac{(n!)^2}{(n+k)!(n-k)!}\{\varphi(x+k) + \varphi(x-k)\}. \qquad (2.1)$$
**Entry 2(i)：**设 $f(x+1) - f(x-1) = 2\varphi'(x)$，其中 $\varphi$ 为多项式，则存在如下形式的多项式解 $f$：
$$f(x) = \sum_{n=0}^{\infty} \frac{F_{2n+1}(x)}{2n+1}. \qquad (2.2)$$

**出处。**Berndt Part I, Ch. 5, Entry 2(i), p. 111。

**状态。**已证明（Doron Zeilberger 建议的算子演算证明：记 $D$ 为微分算子、$Ef(x) = f(x+1) = e^D f(x)$，由 (2.1) 得 $F_{2n+1}(x) = \frac{(-1)^n(n!)^2}{(2n)!}(2\sinh(D/2))^{2n}\varphi$，再验证 (2.5)–(2.7)）。注：(2.2) 右端的级数实际上是有限和（$\varphi$ 为多项式时 $F_{2n+1}$ 在 $n$ 超过多项式次数后为零）；一般情形下级数不收敛。拉马努金实际考虑的是更一般的方程 $f(x+h) - f(x-h) = 2h\varphi'(x)$，取 $h = 1$ 不失一般性（置 $y = xh$ 换元）。

**对照。**差分方程与算子演算见 M02、M12；$F_{2n+1}$ 的组合结构见 M13。

## Entry 2(ii)——$f(x+1) + f(x-1) = 2\varphi(x)$ 的多项式解

**陈述。**设 $f(x+1) + f(x-1) = 2\varphi(x)$，其中 $\varphi$ 为多项式，则存在如下形式的多项式解 $f$：
$$f(x) = \sum_{n=0}^{\infty} 2^{-n}\binom{2n}{n} F_{2n+1}(x), \qquad (2.3)$$
其中 $F_{2n+1}$ 由 (2.1) 定义。

**出处。**Berndt Part I, Ch. 5, Entry 2(ii), p. 111。

**状态。**已证明（同 Entry 2(i) 的算子演算：(2.3) 左端化为 $\sum_{n=0}^{\infty} (-2\sinh^2(D/2))^n \varphi = \varphi/\cosh D$，而所给方程的算子形式为 $(E+E^{-1})f = 2\varphi$，即 $f = \varphi/\cosh D$）。注：同 Entry 2(i)，(2.3) 右端在 $\varphi$ 为多项式时为有限和；一般情形下级数不收敛。

**对照。**见 Entry 2(i)。

**数值复核（精确分数，取 $\varphi(x) = x^2$）：**$F_1(x) = x^2$、$F_3(x) = -1$、$F_5(x) = F_7(x) = 0$，故 (2.2) 给出 $f(x) = x^2 - 1/3$，(2.3) 给出 $f(x) = x^2 - 1$；两者均满足所给差分方程（相差常数）。

## Entry 3——$f(x+h) + pf(x) = \varphi(x)$ 的展开系数（Eulerian 多项式）

**陈述。**设 $f(x+h) + pf(x) = \varphi(x)$，其中 $p \ne -1$，则按 (1.1) 的记号，
$$a_n = \frac{(-1)^n \psi_n(p)}{n!(p+1)^{n+1}}, \qquad 0 \le n < \infty,$$
其中 $\psi_n(p)$ 由 (0.1) 定义。

**出处。**Berndt Part I, Ch. 5, Entry 3, p. 113。

**状态。**已证明（取 $\varphi(x) = e^x$，由 (1.1) 得 $\sum a_n h^n = 1/(e^h+p)$，与 (0.1) 比较即得 (3.1)）。注：Appell、Brodén、Picard 研究过 $f(x+h) + pf(x) = \varphi(x)$ 的周期解；Nörlund 的综述有更多类型差分方程的讨论。

**对照。**Eulerian 多项式 $\psi_n(p)$ 见 M13（Eulerian 数）；$p = 0$ 时 $a_n = (-1)^n/n!$（因 $\psi_n(0) = 1$），与 $e^{-h}$ 的展开一致。

## Entry 4——Eulerian 多项式的级数表示

**陈述。**设 $|p| < 1$，$n \ge 0$，则
$$(p+1)^{-n-1}\psi_n(p) = \sum_{k=0}^{\infty} (k+1)^n (-p)^k. \qquad (4.1)$$

**出处。**Berndt Part I, Ch. 5, Entry 4, p. 113。

**状态。**已证明（$|e^{-x}p| < 1$ 时 $1/(e^x+p) = \sum_{k=0}^{\infty} e^{-(k+1)x}(-p)^k$，展开 $e^{-(k+1)x}$ 并与 (0.1) 比较 $x^n$ 的系数；两级数在复 $x$ 平面上有公共收敛域，论证见书中 p. 113）。数值复核：$p = 0.1$、$0.3$、$0.5$，$n = 0,\dots,4$ 时两边一致至 $10^{-12}$。

**对照。**幂和 $\sum (k+1)^n(-p)^k$ 见 M02（幂级数）、M13（Eulerian 数）；(4.1) 是下文 Entry 6、Entry 8 与第 8 节例题的出发点。

## Entry 5——$\psi_n(p)$ 的递推

**陈述。**$\psi_0(p) = 1$；$n \ge 1$ 时
$$(-1)^{n+1}p(p+1)^{-n}\psi_n(p) = \sum_{k=0}^n (-1)^k \binom{n}{k}(p+1)^{-k}\psi_k(p). \qquad (5.1)$$

**出处。**Berndt Part I, Ch. 5, Entry 5, pp. 113–114。

**状态。**已证明（由 (0.1)，$1 = \{p + \sum_{n=0}^{\infty} x^n/n!\}\sum_{n=0}^{\infty} (-1)^n\psi_n(p)x^n/(n!(p+1)^{n+1})$，比较系数即得）。$n \ge 1$ 时 (5.1) 可改写为递推
$$\psi_n(p) = \sum_{j=0}^{n-1} (-1)^j \binom{n}{j+1}(p+1)^j \psi_{n-j-1}(p), \qquad (5.2)$$
其中已置 $j = n-k-1$。由 $\psi_1(p) = 1$ 出发对 $n$ 归纳，可见 $\psi_n(p)$ 为 $p$ 的 $n-1$ 次多项式。数值复核（精确分数）：(5.1) 在 $n = 1,\dots,5$、$p = 1/5$、$2/5$ 时逐项成立。

**对照。**递推与多项式次数见 M13；由 (5.2) 得 $\psi_n(p) = \sum_{k=0}^{n-1} F_{k+1}(n)(-p)^k$（(6.1)，$F_{k+1}(n)$ 为 Eulerian 数）。

## Entry 6(i)(ii)(iii)——Eulerian 数的恒等式

**陈述。**设 $1 \le r \le n$，则
$$\text{(i)} \qquad F_r(n) = F_{n-r+1}(n),$$
$$\text{(ii)} \qquad \sum_{k=0}^{r-1} \binom{n+k}{k} F_{r-k}(n) = r^n,$$
$$\text{(iii)} \qquad F_r(n) = \sum_{k=0}^{r-1} (-1)^k \binom{n+1}{k}(r-k)^n.$$

**出处。**Berndt Part I, Ch. 5, Entry 6, pp. 114–115。

**状态。**已证明（(i) 由 (0.1) 与 (6.2) $(-1)^{n-1}\psi_n(p) = p^{n-1}\psi_n(1/p)$ 得；(ii)(iii) 由 (4.1) 与 (6.1) 比较 $p^{r-1}$ 的系数得）。**拉马努金原文疏失**：笔记（TIFR 第二卷 p. 48）中 (ii) 的表述有误；Berndt 指出须把左端的 $n$ 换成 $n+1$（即书中印出的 (ii) 为订正后的形式）。(ii) 是 Worpitzky 的结果，(iii) 是 Euler 的结果。数值复核（精确分数）：(i)(ii)(iii) 在 $n = 1,\dots,7$、$1 \le r \le n$ 时逐项成立。

**对照。**Eulerian 数的对称性与求和见 M13；(iii) 是 Eulerian 数的显式公式（容斥形式）。

## Entry 7——$\psi_n(x-1)$ 的对数展开

**陈述。**设 $n \ge 0$，$0 < x < 1 - e^{-2\pi}$，则
$$\psi_n(x-1) = \frac{x^{n+1}}{1-x}\left\{\frac{n!}{\left(\mathrm{Log}\frac{1}{1-x}\right)^{n+1}} + (-1)^n \sum_{k=n+1}^{\infty} \frac{B_k}{k(k-n-1)!}\left(\mathrm{Log}\frac{1}{1-x}\right)^{k-n-1}\right\}, \qquad (7.1)$$
其中 $B_k$ 为第 $k$ 个 Bernoulli 数。

**出处。**Berndt Part I, Ch. 5, Entry 7, p. 115。

**状态。**已证明（由 (I1) 得 (7.3) $\sum_{k=1}^{\infty} e^{-kx} = \sum_{k=0}^{\infty} B_k x^{k-1}/k!$，对 $x$ 求导 $n$ 次得 (7.4)，再置 $x = -\mathrm{Log}(1-x)$，由 Entry 4 知 (7.4) 左端为 $(1-x)x^{-n-1}\psi_n(x-1)$）。数值复核（mpmath，30 位）：$n = 1,2,3$，$x = 0.1$、$0.3$ 时两边一致至 $10^{-9}$。

**拉马努金原文表述问题：**拉马努金的版本与此不同。他断言 $\psi_n(x-1)$ 是下式的「取整部分」（integral part）：
$$\frac{x^{n+1}}{1-x}\left\{\frac{n!}{\left(\mathrm{Log}\frac{1}{1-x}\right)^{n+1}} + (-1)^n \frac{B_{n+1}}{n+1}\right\}. \qquad (7.2)$$
但 $\psi_n(x-1)$ 一般不是整数，Berndt 表示不清楚拉马努金意指什么；或许他是指 (7.1) 的主要贡献是 (7.2)，尤其当 $x$ 很小时。

**对照。**对数展开与 Bernoulli 级数见 M01、M02；Eulerian 多项式在 $x-1$ 处的值见 Entry 8（$\psi_n(-1) = n!$）。

## Entry 8——$\psi_n(-1)$、$\psi_n(1)$ 与前七个 Eulerian 多项式

**陈述。**设 $n \ge 1$，则 $\psi_n(-1) = n!$，且 $\psi_n(1) = 2^{n+1}(2^{n+1}-1)B_{n+1}/(n+1)$。此外
$$\psi_0(p) = \psi_1(p) = 1,$$
$$\psi_2(p) = 1-p,$$
$$\psi_3(p) = 1-4p+p^2,$$
$$\psi_4(p) = 1-11p+11p^2-p^3,$$
$$\psi_5(p) = 1-26p+66p^2-26p^3+p^4,$$
$$\psi_6(p) = 1-57p+302p^2-302p^3+57p^4-p^5,$$
$$\psi_7(p) = 1-120p+1191p^2-2416p^3+1191p^4-120p^5+p^6.$$

**出处。**Berndt Part I, Ch. 5, Entry 8, p. 116。

**状态。**已证明（$\psi_n(-1)$ 由 (5.2) 与归纳得；$\psi_n(1)$ 由 (I1) 得 $\sum_{k=0}^{\infty} (1-2^k)B_k x^{k-1}/k! = 1/(e^x+1) = \sum_{n=0}^{\infty} (-1)^n\psi_n(1)x^n/(2^{n+1}n!)$，比较系数即得；其余多项式用 Entry 6(i) 与递推 (8.1) $F_k(n) = kF_k(n-1) + (n-k+1)F_{k-1}(n-1)$（$2 \le k \le n$；拉马努金未明写 (8.1)，但显示他掌握了这样的公式）算出）。数值复核（精确分数）：$\psi_n(-1) = n!$（$n = 1,\dots,7$）、$\psi_n(1)$ 公式（$n = 1,\dots,7$，如 $\psi_5(1) = 16$）、$\psi_0,\dots,\psi_7$ 的全部系数均与 (5.2) 的递推一致；另 $\psi_5(-2) = 541$、$\psi_5(-3) = 1456$。

**对照。**Eulerian 多项式表见 M13；$\psi_n(1)$ 公式中的 Bernoulli 数见 M01。

### 推论 1——Entry 3 的解的另一表示

**陈述。**设 $f(x)$ 为 Entry 3 中找到的解，则 $f(x)$ 是下式中与 $n$ 无关的项：
$$\frac{\sum_{k=0}^{\infty} \varphi^{(k)}(x)/n^k}{e^{nh}+p}, \qquad (8.2)$$
其中约定分子中的级数确实收敛。

**出处。**Berndt Part I, Ch. 5, §8 推论 1，p. 117。**状态。**已证明（按 (0.1) 展开 $1/(e^{nh}+p)$，乘开两级数即得）。**对照。**见 Entry 3、M02。

### 推论 2

Berndt 注：推论 2 是完全平凡的，不值得在此记录。——本文件从略。

### 推论 3——偶数阶 Eulerian 多项式含因子 $1-p$

**陈述。**设 $n$ 为偶数且为正数，则 $\psi_n(p)$ 可被 $1-p$ 整除。

**出处。**Berndt Part I, Ch. 5, §8 推论 3，p. 117。**状态。**已证明（由 (6.1) 与 Entry 6(i) 即得）。**对照。**见 M13；如 $\psi_2(p) = 1-p$、$\psi_4(p) = (1-p)(1-10p+p^2)$。

### 推论 4、5——$\cos x$、$\sin x$ 的 Eulerian 展开

**陈述。**设 $|x| < |\mathrm{Log}(-p)|$，则
$$\frac{\cos x + p}{p^2 + 2p\cos x + 1} = \sum_{n=0}^{\infty} \frac{(-1)^n \psi_{2n}(p) x^{2n}}{(2n)!(p+1)^{2n+1}},$$
$$\frac{\sin x}{p^2 + 2p\cos x + 1} = \sum_{n=0}^{\infty} \frac{(-1)^n \psi_{2n+1}(p) x^{2n+1}}{(2n+1)!(p+1)^{2n+2}}.$$

**出处。**Berndt Part I, Ch. 5, §8 推论 4、5，p. 117。**状态。**已证明（在 (0.1) 中置 $x = ix$，取实部与虚部即得）。**对照。**三角函数的幂级数见 M02；Eulerian 多项式的奇偶部分见 M13。

### 推论 6——数列 $\{A_n\}$ 与 zeta 值

**陈述。**设 $\psi_n(p-1) = \sum_{k=0}^{n-1} A_{n-k}(-p)^k$（(8.3)；Berndt 注：拉马努金如此定义的 $A_n$ 并不唯一确定，他改取 (8.3) 的 (iv) 为定义再推其余各式；注意 $A_k$ 依赖于 $n$）。设 $1 \le r \le n$，则
$$\text{(i)} \qquad \sum_{k=1}^r \binom{r}{k} A_k = r^n,$$
$$\text{(ii)} \qquad A_r = \sum_{k=0}^{r-1} (-1)^k \binom{r}{k}(r-k)^n,$$
$$\text{(iii)} \qquad A_r/n! \text{ 是 } (e^x-1)^r \text{ 中 } x^n \text{ 的系数},$$
$$\text{(iv)} \qquad \sum_{k=1}^{\infty} (-1)^{k+1} k^n(\zeta(k+1)-1) = (-1)^n + (-1)^n 2^{-n-1}\psi_n(1) + \sum_{k=1}^n (-1)^{k+1} A_k\zeta(k+1),$$
其中 $\psi_n(1)$ 由 Entry 8 确定。

**出处。**Berndt Part I, Ch. 5, §8 推论 6，pp. 117–119。

**状态。**已证明（(i) 由 (6.1) 与 (8.4) $\psi_n(p-1) = \sum_{k=0}^{n-1} F_{k+1}(n)(1-p)^k$ 比较 $p^{n-j}$ 的系数，再用 Vandermonde 定理与 Entry 6(i)(ii) 得；(ii) 由 (i) 反演得；(iii) 是第二类 Stirling 数的熟知性质（证明从略）；(iv) 依次用 Entry 4、(6.2) 与 (8.3) 得）。附注：由 (ii) 可见 $A_r = A_r(n) = r!\, S(n,r)$，其中 $S(n,r)$ 为第二类 Stirling 数（见 Abramowitz–Stegun pp. 824–825 与本书第 3 章第 6–8 节）。数值复核（mpmath，30 位）：(iv) 在 $n = 1,2$ 时两边一致至 $10^{-20}$（$n = 1$ 时两边约为 $0.394934$）。

**对照。**第二类 Stirling 数见 M13；(iv) 中的 zeta 值见 M01、M02。

### 第 8 节例 1、2——$\sum k^5/2^k$ 与 $\sum k^5/3^k$

**陈述。**$\sum_{k=1}^{\infty} k^5/2^k = 1082$，$\sum_{k=1}^{\infty} k^5/3^k = 273/4$。

**出处。**Berndt Part I, Ch. 5, §8 例 1、2，p. 119。**状态。**已证明（由 Entry 4 与 (6.2) 得 (8.5) $\sum_{k=1}^{\infty} k^n/p^k = \psi_n(-1/p)/(p(1-1/p)^{n+1}) = p\psi_n(-p)/(p-1)^{n+1}$；由 Entry 8，$\psi_5(-2) = 541$、$\psi_5(-3) = 1456$，代入即得）。数值复核：两和的前 300 项部分和分别为 $1082.0$ 与 $68.25$（误差 $< 10^{-25}$）。**对照。**幂和的求值见 M02、M13。

## Entry 9——Bernoulli 数的定义

**陈述。**Bernoulli 数 $B_n$（$0 \le n < \infty$）由导言的 (I1) 定义：
$$\frac{x}{e^x-1} = \sum_{n=0}^{\infty} \frac{B_n x^n}{n!}, \qquad |x| < 2\pi. \qquad \text{(I1)}$$

**出处。**Berndt Part I, Ch. 5, Entry 9, p. 119；定义见导言 (I1)，pp. 12–13（当代定义，见 Abramowitz–Stegun [1, p. 804]；与拉马努金本人的约定不同）。

**状态。**定义。由此 $B_0 = 1$、$B_1 = -1/2$、$B_2 = 1/6$、$B_4 = -1/30$、$B_6 = 1/42$、$B_8 = -1/30$、$B_{10} = 5/66$、$B_{12} = -691/2730$，奇数项 $B_{2k+1} = 0$（$k \ge 1$）。数值复核（精确分数）：$B_n$（$n \le 38$）与 Abramowitz–Stegun 表一致。

**对照。**这就是 **M01 缺失的 Bernoulli 数定义**（M02/M06 引用它并写「见 M01.3」，但 M01 全文未给定义；见文末「与 M 模块对照」）。Euler 数的对应定义见导言 (I2)：$\sec x = \sum_{n=0}^{\infty} (-1)^n E_{2n} x^{2n}/(2n)!$。

## Entry 10——$h/(e^h+1)$ 的展开

**陈述。**Entry 10 即 (1.3) 右端给出的展开：
$$\frac{h}{e^h+1} = \sum_{n=0}^{\infty} \frac{(1-2^n)B_n h^n}{n!}.$$

**出处。**Berndt Part I, Ch. 5, Entry 10, p. 119。**状态。**已证明（见 Entry 1(ii) 的证明）。**对照。**见 Entry 1(ii)、M01。

## Entry 11——$\mathrm{Log}(x/(e^x-1))$ 的级数

**陈述。**设 $|x| < 2\pi$，则
$$\mathrm{Log}\left(\frac{x}{e^x-1}\right) = \sum_{n=1}^{\infty} \frac{(-1)^{n-1}B_n x^n}{n\, n!}.$$

**出处。**Berndt Part I, Ch. 5, Entry 11, pp. 119–120。

**状态。**已证明（由 (I1)，$\mathrm{Log}(x/(e^x-1)) = \int_0^x (1/t - e^t/(e^t-1))\,dt$，逐项积分即得）。数值复核（mpmath，30 位）：$x = 0.5$ 时两边均为 $-0.26039505099275674$。

**对照。**对数级数与 Bernoulli 数见 M01、M02。

## Entry 12——$\mathrm{Log}(2/(e^x+1))$ 的级数

**陈述。**设 $|x| < \pi$，则
$$\mathrm{Log}\left(\frac{2}{e^x+1}\right) = \sum_{n=1}^{\infty} \frac{(-1)^{n-1}(2^n-1)B_n x^n}{n\, n!}.$$

**出处。**Berndt Part I, Ch. 5, Entry 12, p. 120。

**状态。**已证明（$\mathrm{Log}(2/(e^x+1)) = \mathrm{Log}(2x/(e^{2x}-1)) - \mathrm{Log}(x/(e^x-1))$，用 Entry 11 即得）。数值复核（mpmath，30 位）：$x = 0.5$ 时两边均为 $-0.28092980362016137$。

**对照。**见 Entry 11、M01、M02。

### 第 12 节后例 1–3——三个近似式

**背景。**以下例 1–3 的结论在笔记中写成等式，但拉马努金显然知道它们是近似。置 $e^P = 1+p$、$e^Q = 1+q$、$e^R = 1+r$、$e^S = 1+s$、$e^T = 1+t$，其中 $p, q, r, s, t$ 视为小量。

**例 1。**若 $e^P + e^Q + e^R = 2 + e^{P+Q+R}$，则
$$\frac{1}{P} + \frac{1}{Q} + \frac{1}{R} + \frac{1}{12}(P+Q+R) \approx \frac{1}{2}.$$

**例 2。**若 $e^{P+Q+R+S} = \frac{e^P+e^Q+e^R+e^S-2}{e^{-P}+e^{-Q}+e^{-R}+e^{-S}-2}$，则
$$\frac{1}{P} + \frac{1}{Q} + \frac{1}{R} + \frac{1}{S} + \frac{1}{12}(P+Q+R+S) \approx 0.$$

**例 3。**若 $2e^{P+Q+R+S+T} = \frac{(e^P+e^Q+e^R+e^S+e^T-2)^2 - (e^{2P}+e^{2Q}+e^{2R}+e^{2S}+e^{2T}-2)}{e^{-P}+e^{-Q}+e^{-R}+e^{-S}+e^{-T}-2}$，则
$$\frac{1}{P} + \frac{1}{Q} + \frac{1}{R} + \frac{1}{S} + \frac{1}{T} + \frac{1}{12}(P+Q+R+S+T) \approx \frac{1}{2}.$$

**出处。**Berndt Part I, Ch. 5, §12 例 1–3，pp. 120–121。**状态。**已证明（近似式；证明用 (I1) 展开 $1/(e^P-1)$ 等并略去 $P, Q, R$ 的二次以上项）。**拉马努金原文疏失**：例 1 中拉马努金在右端误写 $-1/2$，应为 $1/2$。**对照。**近似计算见 M12（渐近展开）。

## Entry 13——$x\cot x$ 的级数

**陈述。**设 $|x| < \pi$，则
$$x\cot x = \sum_{n=0}^{\infty} \frac{(-1)^n B_{2n}(2x)^{2n}}{(2n)!}.$$

**出处。**Berndt Part I, Ch. 5, Entry 13, p. 121。**状态。**已证明（熟知公式，Berndt 从略）。数值复核（mpmath，30 位）：$x = 0.5$ 时两边一致至 $10^{-25}$。**对照。**三角函数的 Bernoulli 展开见 M01、M02。

## Entry 14——$x\csc x$ 的级数

**陈述。**设 $|x| < \pi$，则
$$x\csc x = \sum_{n=0}^{\infty} \frac{(-1)^n(2-2^{2n})B_{2n}x^{2n}}{(2n)!}.$$

**出处。**Berndt Part I, Ch. 5, Entry 14, p. 121。**状态。**已证明（熟知公式，Berndt 从略）。数值复核（mpmath，30 位）：$x = 0.5$ 时两边一致至 $10^{-25}$。**对照。**见 Entry 13。

## Entry 15——$x\tan x$ 的级数

**陈述。**设 $|x| < \pi/2$，则
$$x\tan x = \sum_{n=1}^{\infty} \frac{(-1)^n 2^{2n}(1-2^{2n})B_{2n}x^{2n}}{(2n)!}.$$

**出处。**Berndt Part I, Ch. 5, Entry 15, p. 121。**状态。**已证明（熟知公式，Berndt 从略；由 (12) 与 Entry 14 可得，见 Entry 22 的证明）。数值复核（mpmath，30 位）：$x = 0.5$ 时两边一致至 $10^{-25}$（首项 $n = 1$ 给出 $x^2$）。**对照。**见 Entry 13。

## Entry 16——$\mathrm{Log}(x/\sin x)$ 的级数

**陈述。**设 $|x| < \pi$，则
$$\mathrm{Log}\left(\frac{x}{\sin x}\right) = \sum_{n=1}^{\infty} \frac{(-1)^{n+1}B_{2n}(2x)^{2n}}{(2n)(2n)!}.$$

**出处。**Berndt Part I, Ch. 5, Entry 16, p. 122。**状态。**已证明（$\mathrm{Log}(x/\sin x) = \int_0^x (1/t - t\cot t)\,dt/t$，用 Entry 13 即得）。数值复核（mpmath，30 位）：$x = 0.5$ 时两边一致至 $10^{-31}$。**对照。**见 Entry 13、M02。

## Entry 17——$\mathrm{Log}(\sec x)$ 的级数

**陈述。**设 $|x| < \pi/2$，则
$$\mathrm{Log}(\sec x) = \sum_{n=1}^{\infty} \frac{(-1)^n 2^{2n}(1-2^{2n})B_{2n}x^{2n}}{(2n)(2n)!}.$$

**出处。**Berndt Part I, Ch. 5, Entry 17, p. 122。**状态。**已证明（$\mathrm{Log}(\sec x) = \int_0^x \tan t\,dt$，用 Entry 15 即得）。数值复核（mpmath，30 位）：$x = 0.5$ 时两边一致至 $10^{-31}$。**对照。**见 Entry 15、M02。

**注记（Entry 17 之后）。**拉马努金接着作三个注记，第一个平凡，第二个是第三个的特例：
$$\frac{B_{2n}}{B_{2n-2h}} \sim \frac{(-1)^h(2n)!}{(2\pi)^{2h}(2n-2h)!}, \qquad n \to \infty, \quad 0 \le h \le n-1,$$
这是 $\zeta(2n)$ 的 Euler 公式（Entry 25(i)）的简单推论。

## Entry 18——Euler 的 Bernoulli 数递推

**陈述。**设 $n$ 为大于 1 的整数，则
$$-(2n+1)B_{2n} = \sum_{k=1}^{n-1} \binom{2n}{2k} B_{2k}B_{2n-2k}.$$

**出处。**Berndt Part I, Ch. 5, Entry 18, p. 122。

**状态。**已证明（Euler 的递推；拉马努金第一篇论文 [4]（[15, pp. 1–14]，Bernoulli 数）的第 2 节含有本条的证明）。拉马努金在本条之后列出全部指标 $\le 38$ 的 Bernoulli 数，值全部正确，与 Abramowitz–Stegun 表（[1, p. 810]）一致。下一结果见该论文 [4] 的 (16)。数值复核（精确分数）：$n = 2,\dots,7$ 时逐项成立。

**对照。**Bernoulli 数的递推见 M01；本条是拉马努金第一篇论文的核心结果之一。

## Entry 19(i)——$2(2^{2n}-1)B_{2n}$ 为整数

**陈述。**对每个正整数 $n$，$2(2^{2n}-1)B_{2n}$ 是整数。

**出处。**Berndt Part I, Ch. 5, Entry 19(i), p. 122。**状态。**已证明（Berndt 给出比 [4] 中更简易的证明：由 von Staudt–Clausen 定理，$B_{2n}$ 的分母是全部满足 $(p-1)|2n$ 的素数 $p$ 的乘积；设 $p$ 为这样的奇素数，则由 Fermat 定理 $p | (2^{p-1}-1)$，又 $(p-1)|2n$，故 $p | (2^{2n}-1)$）。数值复核（精确分数）：$n = 1,\dots,12$ 时均为整数。**对照。**见 M01（von Staudt–Clausen 定理）。

## Entry 19(ii)——$B_{2n}$ 分子的整除性（Adams 定理）

**陈述。**$B_{2n}$ 的分子可被 $2n$ 的最大因子整除，该因子与 $B_{2n}$ 的分母互素。

**出处。**Berndt Part I, Ch. 5, Entry 19(ii), p. 123。**状态。**已证明（见 [4] 的 (18)，原为 J. C. Adams 的结果，见 Uspensky–Heaslet [1, p. 261]）。**拉马努金原文疏失**：在 Entry 19(ii) 与 [4] 的 (18) 中，拉马努金都断言了更强的结果，即所指的商是素数；这是**错的**，例如 $B_{22}$ 的分子是 $854513 = 11 \cdot 131 \cdot 593$（见 Wagstaff 的表 [1, p. 589]）。数值复核（精确分数）：$n = 1,\dots,12$ 时分子整除性成立。**对照。**见 M01。

## Entry 19(iii)——von Staudt–Clausen 定理

**陈述。**Entry 19(iii) 即 von Staudt–Clausen 定理的陈述（见 [4] 的 (19)）。

**出处。**Berndt Part I, Ch. 5, Entry 19(iii), p. 123。**状态。**已证明（经典定理：$B_{2n} + \sum_{(p-1)|2n} 1/p$ 为整数，其中求和取遍全部满足 $(p-1)|2n$ 的素数 $p$）。**对照。**von Staudt–Clausen 定理见 M01；其另一形式见 Entry 20。

## Entry 20——von Staudt–Clausen 定理的另一形式

**陈述。**设 $n$ 为非负整数，$F_{2n}$ 为全部满足 $(p-1)|2n$ 的素数 $p$ 的倒数之和，则 $(-1)^{n-1}B_{2n} + (-1)^n(1-F_{2n})$ 是整数 $I_{2n}$。

**出处。**Berndt Part I, Ch. 5, Entry 20, p. 123。**状态。**已证明（von Staudt–Clausen 定理的另一版本）。拉马努金接着列出 $I_{2n}$ 的值：$I_{2n} = 0$（$0 \le n \le 6$）、$I_{14} = 1$、$I_{16} = 7$、$I_{18} = 55$、$I_{20} = 529$、$I_{22} = 6192$、$I_{24} = 86580$、$I_{26} = 1425517$，全部正确。数值复核（精确分数）：$n = 1,\dots,13$ 时 $I_{2n}$ 的值与表中一致（$n = 0$ 时 $F_0$ 无定义——每个素数都整除 0——$I_0 = 0$ 是约定）。

**对照。**见 Entry 19(iii)、M01。

### 第 20 节例 1——$B_{22}$ 的计算（推理有误）

**陈述。**例 1 中拉马努金部分借助 von Staudt–Clausen 定理计算 $B_{22}$。

**出处。**Berndt Part I, Ch. 5, §20 例 1，p. 123。**状态。**推理有误：拉马努金以为 $B_{22}$ 的分子除以 11 是素数，这是不对的（见 Entry 19(ii)：$854513 = 11 \cdot 131 \cdot 593$）。**对照。**见 Entry 19(ii)。

### 第 20 节例 2——$B_{200}$ 的分数部分

**陈述。**$B_{200}$ 的分数部分是 $216641/1366530$。

**出处。**Berndt Part I, Ch. 5, §20 例 2，p. 123。**状态。**已证明（von Staudt–Clausen 定理的直接推论：$(p-1)|200$ 的素数为 $2, 3, 5, 11, 41, 101$，其倒数和为 $1 + 216641/1366530$，故 $B_{200} = \text{整数} - 216641/1366530$）。**写法说明**：此处「分数部分」按 $B_{200} = \text{整数} - f$（$0 < f < 1$）的写法，即 $f = \lceil B_{200}\rceil - B_{200}$；按现代记号 $\{x\} = x - \lfloor x\rfloor$，则 $\{B_{200}\} = 1149889/1366530$。数值复核（精确分数）：$B_{200} + \sum 1/p$ 为整数（约 $-3.6 \times 10^{182}$），$B_{200}$ 的上述两种分数表示均已验证。**对照。**见 Entry 19(iii)、M01。

## Entry 21——两张素数表

**陈述。**Entry 21 由两张表组成。第一张是至 211 的素数表：造表时拉马努金利用了下述事实——除 2、3、5 外的任何素数都形如 $p + 30n$（$n \ge 0$，$p$ 为 7、11、13、17、19、23、29、31 之一）。第二张表列出全部至 4969 的素数：先填入至 211 的素数，再利用除 2、3、5、7 外的任何素数都形如 $q + 210n$（$n \ge 0$，$q$ 为 11、13、17、…、199、211 之一）的事实，每次加 210 的倍数，直至素数 $2 \cdot 3 \cdot 5 \cdot 7 \cdot 11 + 1 = 2311$；再以类似方式用等差数列 $r + 2310n$（$r$ 为 13、17、19、…、2309、2311 之一）继续。

**出处。**Berndt Part I, Ch. 5, Entry 21, pp. 123–124。**状态。**已核对（第一张表的规则：$\le 211$ 的素数除 2、3、5 外模 30 的余数确为 7、11、13、17、19、23、29、1（$31 \equiv 1$），共 47 个素数；第二张表至 4969 共 665 个素数。注：第二张表基数表述中的省略号须理解为 11 至 211 间全部与 210 互素的数（含合数余数 121、143、169、187、209，例如素数 $331 = 121 + 210$）；若只取素数余数则会漏掉 $331$ 等素数）。**对照。**素数表与素数定理见 M01。

## Entry 22——$B_{2n}$ 与 Euler 数的恒等式

**陈述。**设 $n$ 为自然数，则
$$2^{2n}(2^{2n}-1)B_{2n} = 2n\sum_{k=0}^{n-1} \binom{2n-2}{2k} E_{2k}E_{2n-2k-2},$$
其中 $E_j$ 为第 $j$ 个 Euler 数。

**出处。**Berndt Part I, Ch. 5, Entry 22, p. 124。**状态。**已证明（由 (I2) 与 Entry 15：$\{\sum_{k=0}^{\infty} (-1)^k E_{2k}x^{2k}/(2k)!\}^2 = \sec^2 x = \frac{d}{dx}\tan x = \sum_{n=1}^{\infty} (-1)^n 2^{2n}(1-2^{2n})B_{2n}x^{2n-2}/((2n)(2n-2)!)$，比较 $x^{2n-2}$ 的系数即得）。拉马努金接着记录 Euler 数 $E_{2n}$（$0 \le n \le 7$），值全部正确（$1, -1, 5, -61, 1385, -50521, 2702765, -199360981$）。数值复核（精确分数）：$n = 1,\dots,6$ 时逐项成立。**对照。**Bernoulli 数与 Euler 数的关系见 M01。

## Entry 23(i)–(iv)——三角函数的部分分式分解

**陈述。**Entry 23(i)–(iv) 给出 $\cot(\pi x)$、$\tan(\pi x/2)$、$\csc(\pi x)$、$\sec(\pi x/2)$ 的熟知部分分式分解。拉马努金在第 2 章 Entry 10 的推论 1–3 中也推导过这些展开。书中未印出确切形式（见 Bromwich [1, pp. 217、225]），标准形式为：
$$\text{(i)} \qquad \pi\cot\pi x = \frac{1}{x} + \sum_{k\ne 0}\left(\frac{1}{x-k}+\frac{1}{k}\right),$$
$$\text{(ii)} \qquad \pi\tan\frac{\pi x}{2} = 4x\sum_{k=0}^{\infty} \frac{1}{(2k+1)^2-x^2},$$
$$\text{(iii)} \qquad \pi\csc\pi x = \frac{1}{x} + \sum_{k=1}^{\infty} \frac{(-1)^k 2x}{x^2-k^2},$$
$$\text{(iv)} \qquad \pi\sec\frac{\pi x}{2} = 4\sum_{k=0}^{\infty} \frac{(-1)^k(2k+1)}{(2k+1)^2-x^2}.$$

**出处。**Berndt Part I, Ch. 5, Entry 23, p. 124。**状态。**已证明（经典结果；上述标准形式在 $x = 0.3$ 处数值复核通过，误差 $< 10^{-30}$）。**对照。**部分分式分解见 M02、M09；与第 2 章 Entry 10 的推论 1–3 相同。

## Entry 24(i)–(iv)——双曲函数的部分分式分解

**陈述。**Entry 24(i)–(iv) 给出 $\coth(\pi x)$、$\tanh(\pi x/2)$、$\mathrm{csch}(\pi x)$、$\mathrm{sech}(\pi x/2)$ 的熟知部分分式展开。标准形式为：
$$\text{(i)} \qquad \pi\coth\pi x = \frac{1}{x} + \sum_{k=1}^{\infty} \frac{2x}{x^2+k^2},$$
$$\text{(ii)} \qquad \pi\tanh\frac{\pi x}{2} = 4x\sum_{k=0}^{\infty} \frac{1}{(2k+1)^2+x^2},$$
$$\text{(iii)} \qquad \pi\,\mathrm{csch}\,\pi x = \frac{1}{x} + \sum_{k=1}^{\infty} \frac{(-1)^k 2x}{x^2+k^2},$$
$$\text{(iv)} \qquad \pi\,\mathrm{sech}\,\frac{\pi x}{2} = 4\sum_{k=0}^{\infty} \frac{(-1)^k(2k+1)}{(2k+1)^2+x^2}.$$

**出处。**Berndt Part I, Ch. 5, Entry 24, p. 124。**状态。**已证明（经典结果；上述标准形式在 $x = 0.3$ 处数值复核通过，误差 $< 10^{-30}$）。**对照。**见 Entry 23、M02、M09。

### 第 24 节后注记——Euler 数的同余式与渐近

**陈述。**Entry 24 之后拉马努金作三个注记。第一：$E_{4n}$ 的末位数字是 5，且 $E_{4n-2}+1$ 可被 4 整除（$n \ge 1$；后者是 Sylvester 的结果）。两者分别是以下同余式的特例（通常归于 Stern，见 Nielsen [5, p. 261]）：
$$E_{4n} \equiv 5 \pmod{60}, \qquad E_{4n-2} \equiv -1 \pmod{60}.$$
第二：是第三个的特例。第三：
$$\frac{E_{2n+2h}}{E_{2n}} \sim \frac{(-1)^h 2^{2h}(2n+2h)!}{\pi^{2h}(2n)!}, \qquad n \to \infty,$$
其中 $h$ 为非负整数；这是 Entry 25(iv) 的简单推论。

**出处。**Berndt Part I, Ch. 5, §24 注记，p. 124。**状态。**已证明（同余式：数值复核 $n = 1,\dots,4$ 时成立；渐近式：$n = 10$、$h = 1$ 时两边分别为 $-187.24154738695103$ 与 $-187.2415473710402$，相对误差 $8 \times 10^{-11}$）。**对照。**Euler 数的同余性质见 M01；渐近式见 M12。

## Entry 25(i)–(iv)——$\zeta(2n)$、$\lambda(2n)$、$\eta(2n)$、$L(2n-1)$ 的 Euler 公式

**陈述。**设 $\mathrm{Re}\, s > 1$ 时 $\lambda(s) = \sum_{k=0}^{\infty} (2k+1)^{-s}$；$\mathrm{Re}\, s > 0$ 时 $\eta(s) = \sum_{k=1}^{\infty} (-1)^{k+1}k^{-s}$，$L(s) = \sum_{k=0}^{\infty} (-1)^k(2k+1)^{-s}$。设 $n$ 为正整数，则
$$\text{(i)} \qquad \zeta(2n) = \frac{(-1)^{n-1}(2\pi)^{2n}}{2(2n)!}B_{2n},$$
$$\text{(ii)} \qquad \lambda(2n) = \frac{(-1)^{n-1}(1-2^{-2n})(2\pi)^{2n}}{2(2n)!}B_{2n},$$
$$\text{(iii)} \qquad \eta(2n) = \frac{(-1)^{n-1}(1-2^{1-2n})(2\pi)^{2n}}{2(2n)!}B_{2n},$$
$$\text{(iv)} \qquad L(2n-1) = \frac{(-1)^{n-1}(\pi/2)^{2n-1}}{2(2n-2)!}E_{2n-2}.$$

**出处。**Berndt Part I, Ch. 5, Entry 25, p. 125。

**状态。**已证明（(i) 为 Euler 的著名公式；$\lambda(s) = (1-2^{-s})\zeta(s)$、$\eta(s) = (1-2^{1-s})\zeta(s)$，故 (ii)(iii) 由 (i) 得；(iv) 是熟知公式——奇特征的 Dirichlet $L$ 函数在奇正整数处可显式求值，见 Berndt–Schoenfeld [1]）。数值复核（mpmath，30 位）：$n = 1,2,3$ 时四式一致至 $10^{-25}$（如 $L(1) = \pi/4$、$L(3) = \pi^3/32$、$L(5) = 5\pi^5/1536$；$\lambda(4) = \pi^4/96$）。

**拉马努金对 Bernoulli 数与 Euler 数的推广。**拉马努金接着用 (i) 与 (iii) 把 Bernoulli 数定义到任意指标：对任何实数 $s$，
$$B_s^* = \frac{2\Gamma(s+1)}{(2\pi)^s}\zeta(s). \qquad (25.1)$$
（采用拉马努金对普通 Bernoulli 数的约定。）注意 $B_{2n+1}^* \ne 0$（$n \ge 1$），与 (I1) 冲突；Euler [1]、[7, p. 350] 也曾用 (25.1) 定义任意指标的 Bernoulli 数，但未作重要应用。类似地，用 (iv) 插值定义任意实指标的 Euler 数：
$$E_s^* = \frac{2\Gamma(s)}{(\pi/2)^s}L(s),$$
则 $E_{2n+1}^* = (-1)^n E_{2n}$。拉马努金未给 $B_s$、$E_s$ 加星号，星号是 Berndt 为区分而加的。

**推论 1。**$B_1^* = \infty$，$B_{3/2}^* = 3\zeta(3/2)/(4\pi\sqrt 2)$，$B_3^* = 3\zeta(3)/(2\pi^3)$。

**推论 2。**$B_0^* = -1$，$B_{1/2}^* = -(1+1/\sqrt 2)\eta(1/2)$，$E_0^* = \infty$，$E_{1/2}^* = 2\sqrt 2\, L(1/2)$，$E_2^* = 8L(2)/\pi^2$。

**出处。**Berndt Part I, Ch. 5, §25 推论 1、2，pp. 125–126。**状态。**已证明（$B_0^*$ 由 (25.1) 与 $\zeta(0) = -1/2$ 得；$E_0^*$ 由 $\Gamma(s)$ 在 $s = 0$ 处有单极点得；其余值易验证）。数值复核（mpmath，30 位）：推论 1、2 的全部等式均成立（$B_0^* = -1$ 由 $\zeta(0) = -1/2$ 直接得）。**对照。**$\zeta(2n)$ 的 Euler 公式见 M01；$B_s^*$、$E_s^*$ 的解析延拓思想见 M12。

## Entry 26——$f(a) = \sum (a+bk)^{-n}$ 的渐近展开

**陈述。**设 $f(a) = \sum_{k=1}^{\infty} (a+bk)^{-n}$，其中 $a, b > 0$，$n > 1$。则当 $b/a \to 0$ 时
$$a^n f(a) \sim \frac{a}{b(n-1)} - \frac{1}{2} + \sum_{k=1}^{\infty} \frac{B_{2k}}{n-1}\binom{n+2k-2}{2k}\left(\frac{b}{a}\right)^{2k-1}. \qquad (26.1)$$
注：$f(a) = b^{-n}\zeta(n, a/b) - a^{-n}$，其中 $\zeta(s, \alpha)$ 为 Hurwitz zeta 函数。

**出处。**Berndt Part I, Ch. 5, Entry 26, p. 126。

**状态。**已证明（渐近式；直接计算得 $f(a-b) - f(a) = a^{-n}$；按 Entry 1(i) 的记号，$h = -b$、$\varphi(a) = 1/\{a^{n-1}b(n-1)\}$，若 Entry 1(i) 适用则 (26.1) 中的 $\sim$ 可换成等号，但右端级数不收敛；用 Nörlund [2, pp. 58–60] 的定理（Entry 1(ii) 证明后提及）可得右端在 $b/a \to 0$ 时渐近地表示左端）。数值复核（mpmath，30 位）：$a = 10$、$b = 1$、$n = 2$ 时左端 $a^n f(a) \approx 9.5166$，右端前三项和 $\approx 9.516633$（渐近级数，误差 $3 \times 10^{-9}$ 量级为下一项）。

**例。**设 $n > 1$，则当正整数 $r \to \infty$ 时
$$\zeta(n) \sim \sum_{k=1}^{r-1} k^{-n} + \frac{1}{(n-1)r^{n-1}} + \frac{1}{2r^n} + \sum_{k=1}^{\infty} \frac{B_{2k}}{n-1}\binom{n+2k-2}{2k}r^{-n-2k+1}. \qquad (26.2)$$
证明：Entry 26 取 $a = r$、$b = 1$，两边加 $\sum_{k=1}^{r-1} k^{-n}$ 即得。拉马努金用 (26.2) 计算 $\zeta(n)$（$2 \le n \le 10$ 的正整数）到小数点后第十位，见下表；Euler 用同样方法算 $\zeta(n)$（$2 \le n \le 16$）到 18 位小数（Bromwich [1, p. 326]）。

**$\zeta(n)$ 数值表（p. 127）。**拉马努金算得（Berndt 订正五处，见下）：

| $n$ | $\zeta(n)$ | $1/B_n^*$ |
|---|---|---|
| 2 | 1.6449340668 | 6 |
| 3 | 1.2020569031 | 17.19624 |
| 4 | 1.0823232337 | 30 |
| 5 | 1.0369277551 | 39.34953 |
| 6 | 1.0173430620 | 42 |
| 7 | 1.0083492774 | 38.03538 |
| 8 | 1.0040773562 | 30 |
| 9 | 1.0020083928 | 20.98719 |
| 10 | 1.0009945781 | 13.2 |

**Berndt 的订正（已数值核实）：**$\zeta(3)$ 的第十位小数应为 2（真值 1.2020569031595942，表中 1.2020569031 是截断）；$\zeta(10)$ 的第九位小数应为 5（真值 1.000994575127818，表中 1.0009945781）；$1/B_3^*$ 的末位数字应为 3（真值 17.196233444412456）；$1/B_7^*$ 的末位数字应为 6（真值 38.03536208813498）；$1/B_9^*$ 的末两位数字应为 20（真值 20.987196437683803）。其余表值与真值在所给位数内一致；偶数 $n$ 的 $1/B_n^*$ 由 Bernoulli 数表得，奇数 $n$ 的由 (25.1) 与 $\zeta(n)$ 的表值得。

**对照。**Hurwitz zeta 函数与 Euler–Maclaurin 求和见 M12；$\zeta(n)$ 的数值见 M01。

### 推论 1（Entry 26）——$\zeta(s)$ 在 $s = 1$ 处的极点与 Euler 常数

**陈述。**Riemann zeta 函数在 $s = 1$ 处有单极点，留数为 1；$\zeta(s)$ 在 $s = 1$ 附近的 Laurent 展开的常数项是 Euler 常数 $\gamma$。

**出处。**Berndt Part I, Ch. 5, §26 推论 1，p. 127。**状态。**已证明（熟知结果，见 Landau [1, p. 164]、Titchmarsh [3, p. 16]）。拉马努金特有的表述是：「$nS_{n+1} = 1$（若 $n = 0$），$S_{n+1} - 1/n = 0.577$ 近似。」其后的草图中拉马努金给出渐近级数的前三项：
$$\gamma \sim \frac{1}{2} + \sum_{n=1}^{\infty} \frac{B_{2n}}{2n}. \qquad (26.3)$$
其中 $\sim$ 的意思是右端前 $n$ 项逼近左端，误差小于第 $n+1$ 项的量级。事实上 (26.3) 的 $\gamma$ 渐近级数最早由 Euler 发现并用于计算 $\gamma$（Bromwich [1, pp. 324–325]）。数值复核：前四项部分和 $\approx 0.57897$（Bromwich 指出这是 (26.3) 能给出的最好逼近 $0.5790$）；取前三项的两个逼近取平均得 $0.5770$，与拉马努金的 $0.577$ 相符。**对照。**Euler 常数见 M01、M12。

### 推论 2（Entry 26）

推论 2 只是推论 1 后半部分用拉马努金的推广 (25.1) 的改写。——本文件从略。

## Entry 27——素数上的一般乘积

**陈述。**设对每个素数 $p$ 与某个常数 $c > 1$，有 $|a_p| \le p^{-c}$，则
$$\prod_p (1-a_p)^{-1} = 1 + \sum_{\substack{n=2 \\ n=p_1\cdots p_k}}^{\infty} a_{p_1}\cdots a_{p_k},$$
其中左端乘积取遍全部素数 $p$，右端求和的下标 $p_1, \dots, p_k$ 是 $n$ 的标准分解中的素数（不必互不相同）。

**出处。**Berndt Part I, Ch. 5, Entry 27, p. 128。**状态。**已证明（展开左端乘积，用唯一分解定理即得）。数值复核：取 $a_p = p^{-2}$，则左端 $= \zeta(2) = \pi^2/6$（见 Entry 28 的特例；素数 $\le 5000$ 的部分乘积相对误差 $3 \times 10^{-5}$）。**对照。**Euler 乘积见 M01；唯一分解定理见 M01。

## Entry 28——$\zeta(s)$ 的 Euler 乘积

**陈述。**设 $\mathrm{Re}\, s > 1$，则
$$\zeta(s) = \prod_p (1-p^{-s})^{-1}.$$

**出处。**Berndt Part I, Ch. 5, Entry 28, p. 128。**状态。**已证明（熟知的 Euler 乘积；实为 Entry 27 取 $a_p = p^{-s}$ 的特例）。**对照。**Euler 乘积见 M01。

### 推论 1——$\prod_p (1+p^{-s}) = \zeta(s)/\zeta(2s)$

**陈述。**设 $\mathrm{Re}\, s > 1$，则 $\prod_p (1+p^{-s}) = \zeta(s)/\zeta(2s)$。

**出处。**Berndt Part I, Ch. 5, §28 推论 1，p. 128。**状态。**已证明（Entry 28 的简单推论）。数值复核：$s = 2$ 时两边均为 $15/\pi^2 \approx 1.51986$（素数 $\le 5000$ 的部分乘积误差 $3 \times 10^{-5}$）。**对照。**见 Entry 28、M01。

### 推论 2——$\prod_p \frac{1+p^{-s}}{1-p^{-s}} = \zeta^2(s)/\zeta(2s)$

**陈述。**设 $\mathrm{Re}\, s > 1$，则 $\prod_p \left(\frac{1+p^{-s}}{1-p^{-s}}\right) = \zeta^2(s)/\zeta(2s)$。

**出处。**Berndt Part I, Ch. 5, §28 推论 2，p. 128。**状态。**已证明（Entry 28 的简单推论）。数值复核：$s = 2$ 时两边均为 $5/2$。**对照。**见 Entry 28、M01。

### 推论 3——$T(s) = (\zeta^2(s)-\zeta(2s))/(2\zeta(s))$

**陈述。**设 $\mathrm{Re}\, s > 1$，则 $T(s) \equiv \sum_n n^{-s} = \frac{\zeta^2(s)-\zeta(2s)}{2\zeta(s)}$，其中左端求和取遍全部标准分解中素因子个数为奇数的正整数 $n$。

**出处。**Berndt Part I, Ch. 5, §28 推论 3，p. 128。**状态。**已证明（由 Entry 28 与推论 1：$\zeta(s) - \zeta(2s)/\zeta(s) = \prod_p (1-p^{-s})^{-1} - \prod_p (1+p^{-s})^{-1}$，即得）。数值复核：$T(2) = \pi^2/20$、$T(4) = \pi^4/1260$（见下文例 3；$n < 3000$ 的部分和误差 $< 2 \times 10^{-4}$）。**对照。**见 Entry 28、M01。

### 第 28 节例 1——$\zeta(2)$、$L(3)$、$\lambda(4)$

**陈述。**例 1(i)(ii)(iii) 记录熟知结果 $\zeta(2) = \pi^2/6$、$L(3) = \pi^3/32$、$\lambda(4) = \pi^4/96$，均可由 Entry 25 推出。

**出处。**Berndt Part I, Ch. 5, §28 例 1，p. 129。**状态。**已证明（Entry 25(i)(iv)(ii) 的特例）。**对照。**见 Entry 25、M01。

### 第 28 节例 2——两个素数乘积

**陈述。**(i) $\prod_p \frac{1+p^{-2}}{1-p^{-2}} = \frac{5}{2}$；(ii) $\prod_p (1+p^{-4}) = \frac{105}{\pi^4}$。

**出处。**Berndt Part I, Ch. 5, §28 例 2，p. 129。**状态。**已证明（(i) 由推论 2 得（$s = 2$）；(ii) 由推论 1 得（$s = 4$）：$\zeta(4)/\zeta(8) = 105/\pi^4$）。数值复核：(ii) 的素数 $\le 5000$ 部分乘积误差 $3 \times 10^{-13}$。**对照。**见 Entry 28、M01。

### 第 28 节例 3——$T(2)$、$T(4)$

**陈述。**$T(2) = \pi^2/20$，$T(4) = \pi^4/1260$，其中 $T(s)$ 如推论 3 所给。

**出处。**Berndt Part I, Ch. 5, §28 例 3，p. 129。**状态。**已证明（由推论 3 与 Entry 25(i) 得）。**对照。**见 Entry 25、Entry 28 推论 3。

### 推论 4——$L(s)$ 的 Euler 乘积

**陈述。**设 $\mathrm{Re}\, s > 1$，则 $L(s) = \prod_p \left(1 - \sin\frac{\pi p}{2}\, p^{-s}\right)^{-1}$。

**出处。**Berndt Part I, Ch. 5, §28 推论 4，p. 129。**状态。**已证明（即 $L(s)$ 的 Euler 乘积，是 Entry 27 的特例）。**对照。**见 Entry 27、M01。

### 推论 5——$\sum k^{-s}\mathrm{Log}\, k$ 的 Euler 乘积对数导数

**陈述。**设 $\mathrm{Re}\, s > 1$，则 $\sum_{k=1}^{\infty} k^{-s}\mathrm{Log}\, k = \zeta(s)\sum_p \frac{\mathrm{Log}\, p}{p^s-1}$。

**出处。**Berndt Part I, Ch. 5, §28 推论 5，p. 129。**状态。**已证明（Entry 28 的 Euler 乘积取对数导数的熟知结果）。数值复核：$s = 2$ 时两边一致（素数 $\le 5000$ 的右端和误差 $2 \times 10^{-4}$）。**对照。**见 Entry 28、M01。

### 第 28 节末例——$\sum_p \sin(\pi p/2)/p$ 收敛

**陈述。**级数 $\sum_p \sin(\pi p/2)/p$ 收敛。

**出处。**Berndt Part I, Ch. 5, §28 末例，p. 129。**状态。**已证明（但证明比本节其余结果深得多，是 $L$ 函数理论中熟知定理的特例，见 Landau [1, pp. 446–449]；拉马努金未给任何他如何得出此结果的提示）。**对照。**Dirichlet $L$ 函数见 M01、M06。

## Entry 29——$\prod (1-x^{p_k})^{-1}$ 的恒等式（被划去，不成立）

**陈述。**设 $|x| < 1$，则
$$\prod_{k=1}^{\infty} (1-x^{p_k})^{-1} = 1 + \sum_{k=1}^{\infty} \frac{x^{p_1+p_2+\cdots+p_k}}{(1-x)(1-x^2)\cdots(1-x^k)}, \qquad (29.1)$$
其中 $p_1, p_2, \dots$ 为按升序排列的素数。

**出处。**Berndt Part I, Ch. 5, Entry 29, p. 130。

**状态。**不成立（拉马努金本人已划去）。设 $c_n$、$d_n$（$2 \le n < \infty$）分别为 (29.1) 左右两端 $x^n$ 的系数，则 $c_n = d_n$（$2 \le n \le 20$），但 $c_{21} = 30$、$d_{21} = 31$，故 (29.1) 为假。数值复核（精确整数级数展开）：$c_n = d_n$（$2 \le n \le 20$）、$c_{21} = 30$、$d_{21} = 31$ 均已验证（左端系数为 $n$ 分拆成素数部分的分拆数；右端系数为 $\sum_k p_{\le k}(n - S_k)$，其中 $S_k$ 为前 $k$ 个素数之和）。

**后续。**G. E. Andrews [3] 讨论了 Entry 29 并提出以下问题：把满足 $\prod_{k=1}^{\infty} (1-x^{a_k})^{-1} = 1 + \sum_{k=1}^{\infty} x^{b_1+\cdots+b_k}/((1-x)\cdots(1-x^k))$ 的一对无穷递增序列 $\{a_k\}$、$\{b_k\}$ 称为「Ramanujan 对」（(29.2)）。若拉马努金是对的，则 $\{a_k\} = \{b_k\} = \{p_k\}$ 将是一对 Ramanujan 对。已知的 Ramanujan 对有四组：(1) $a_k = m+k-1$、$b_k = m$（Euler 定理）；(2) $a_k = m+k-1$（$1 \le k \le m$）、$a_k = 2k-1$（$k > m$）、$b_k = m+k-1$（Euler 的另一恒等式）；(3) $\{a_k\} = \{m > 0 : m \equiv \pm 1 \pmod 5\}$、$b_k = 2k-1$（Rogers–Ramanujan 恒等式）；(4) $\{a_k\} = \{m > 0 : m \equiv \pm 2 \pmod 5\}$、$b_k = 2k$（Rogers–Ramanujan 恒等式）。Andrews 猜想这四组穷尽一切可能；但 Hirschhorn [1] 又找到两组，Blecksmith、Brillhart、Gerst [1] 又发现四组；Blecksmith [1] 的计算机辅助结果强烈表明不存在更多的 Ramanujan 对。Acreman–Loxton [1] 从另一角度研究了 Andrews 的问题（渐近公式与 dilogarithm，见第 9 章 (6.1)）。

**对照。**Rogers–Ramanujan 恒等式见 M07、M03；分拆生成函数见 M05。

## Entry 30——素数上的一般乘积 $\prod_p (1+a_p)$

**陈述。**设对每个素数 $p$ 与某个常数 $c > 1$，有 $|a_p| \le p^{-c}$，则
$$\prod_p (1+a_p) = 1 + \sum_{\substack{n \\ n=p_1\cdots p_k}} a_{p_1}\cdots a_{p_k},$$
其中右端求和取遍全部无平方因子整数 $n = p_1\cdots p_k$（$p_1, \dots, p_k$ 为互不相同的素数）。

**出处。**Berndt Part I, Ch. 5, Entry 30, p. 131。**状态。**已证明（展开左端乘积即得）。**对照。**见 Entry 27、M01。

### 推论 1——无平方因子整数的倒数和

**陈述。**设 $\mathrm{Re}\, s > 1$，则 $\sum_{n=1, n \text{ squarefree}}^{\infty} n^{-s} = \zeta(s)/\zeta(2s)$。

**出处。**Berndt Part I, Ch. 5, §30 推论 1，p. 131。**状态。**已证明（Entry 30 取 $a_p = p^{-s}$，用 Entry 28 推论 1 即得）。数值复核：$s = 2$ 时两边均为 $15/\pi^2$（$n < 3000$ 的部分和误差 $2 \times 10^{-4}$）。**对照。**见 Entry 28、M01。

### 推论 2——奇数个素因子的无平方因子整数

**陈述。**设 $\mathrm{Re}\, s > 1$，则 $\sum_n n^{-s} = \frac{\zeta^2(s)-\zeta(2s)}{2\zeta(s)\zeta(2s)}$，其中求和取遍全部含奇数个素因子的无平方因子整数 $n$。

**出处。**Berndt Part I, Ch. 5, §30 推论 2，p. 131。**状态。**已证明（由 Entry 28 与 Entry 28 推论 1：$\zeta(s)/\zeta(2s) - 1/\zeta(s) = \prod_p (1+p^{-s}) - \prod_p (1-p^{-s})$，即得）。数值复核：$s = 2$ 时两边均为 $5/(2\pi^2) \approx 0.2533$（$n < 3000$ 的部分和误差 $1 \times 10^{-4}$）。**对照。**见 Entry 28、M01。

### 推论 3——非无平方因子整数的倒数和

**陈述。**设 $\mathrm{Re}\, s > 1$，则 $\sum_{n=1, n \text{ not squarefree}}^{\infty} n^{-s} = \frac{\zeta(s)(\zeta(2s)-1)}{\zeta(2s)}$。

**出处。**Berndt Part I, Ch. 5, §30 推论 3，p. 131。**状态。**已证明（由推论 1，左端 $= \zeta(s) - \zeta(s)/\zeta(2s)$）。数值复核：$s = 2$ 时两边一致（$n < 3000$ 的部分和误差 $1.3 \times 10^{-4}$）。**对照。**见 Entry 28、M01。

**注。**Entry 27、Entry 28 的推论 1、3 与第 28 节例 2(ii)、例 3，以及 Entry 30 及其前三个推论，都见于拉马努金的第四篇论文 [7]（[15, pp. 20–21]）。

### 推论 1（Entry 30 后）——素数倒数和发散

**陈述。**素数倒数之和 $\sum_p 1/p$ 发散。

**出处。**Berndt Part I, Ch. 5, §30 推论 1，p. 131。**状态。**已证明（Euler 的熟知结果；拉马努金的证明与 Euler 的证明相似，见 Ayoub [1, p. 6]）。**对照。**素数倒数和发散见 M01。

### 推论 2（Entry 30 后）——$\lim_{s\to 1^+} \{\mathrm{Log}(s-1) + \sum_p p^{-s}\}$ 存在

**陈述。**$\lim_{s\to 1^+} \{\mathrm{Log}(s-1) + \sum_p p^{-s}\}$ 存在。

**出处。**Berndt Part I, Ch. 5, §30 推论 2，p. 132。**状态。**已证明（由 Entry 28，$s > 1$ 时 $\mathrm{Log}\,\zeta(s) = \sum_p 1/p^s + \sum_p \sum_{k=2}^{\infty} 1/(kp^{ks})$；由 Entry 26 推论 1，$\mathrm{Log}\,\zeta(s) \sim -\mathrm{Log}(s-1)$（$s \to 1^+$），即得）。数值复核：该极限的值为 $\sum_p [\mathrm{Log}(1-1/p) + 1/p] \approx -0.315708$（素数 $\le 10^6$ 的部分和；另 Meissel–Mertens 常数 $M = \gamma - \sum_p \sum_{k=2}^{\infty} 1/(kp^k) \approx 0.2614972$，两者相差 $\gamma$）。**对照。**Mertens 定理与 Meissel–Mertens 常数见 M01。

### 推论 3（Entry 30 后）——$p_n/n - \mathrm{Log}\, n$ 的极限（被划去）

**陈述。**设 $p_n$ 为第 $n$ 个素数，则 $p_n/n - \mathrm{Log}\, n$ 在 $n \to \infty$ 时趋于一极限。

**出处。**Berndt Part I, Ch. 5, §30 推论 3，p. 132。**状态。**不成立（拉马努金本人已正确地划去：见 Landau [1, p. 215]，$p_n/n = \mathrm{Log}\, n + \mathrm{Log\, Log}\, n + O(1)$（$n \to \infty$），故 $p_n/n - \mathrm{Log}\, n \sim \mathrm{Log\, Log}\, n$ 发散）。**对照。**素数定理见 M01。

## 小结

- 本章 30 条 Entry 全部收录完毕（Entry 1–30，编号均在原文明确出现；Berndt 章首计数本章共 94 条公式或定理陈述）。前半（Entry 1–8）是 Eulerian 多项式与数的系统理论：差分方程的展开系数（Entry 1、3）、多项式解（Entry 2）、级数表示与递推（Entry 4、5）、Eulerian 数的恒等式（Entry 6）、对数展开（Entry 7）、$\psi_n(-1)$、$\psi_n(1)$ 与前七个多项式及推论 1–6（Entry 8）。中段（Entry 9–24）是 Bernoulli 数与 Euler 数的经典理论：定义（Entry 9、10）、对数与三角级数（Entry 11–17）、Euler 递推（Entry 18）、整除性与 von Staudt–Clausen 定理（Entry 19、20）、素数表（Entry 21）、$B_{2n}$ 与 Euler 数的恒等式（Entry 22）、部分分式分解（Entry 23、24）。后半（Entry 25–30）是 Riemann zeta 函数与 Euler 乘积：$\zeta(2n)$ 等 Euler 公式与 $B_s^*$、$E_s^*$ 的推广（Entry 25）、Hurwitz zeta 的渐近与 $\zeta(n)$ 数值表（Entry 26）、素数上的一般乘积（Entry 27、30）与 Euler 乘积及其推论（Entry 28）、被划去的 Entry 29。
- 本章发现的拉马努金原文疏失（均已在各条注明）：Entry 6(ii) 笔记表述有误（Berndt 印出订正后的形式）；Entry 7 的 (7.2)「取整部分」说法含糊（$\psi_n(x-1)$ 一般不是整数）；第 12 节后例 1 右端 $-1/2$ 应为 $1/2$；Entry 19(ii) 加强断言（商为素数）不成立（$B_{22}$ 的分子 $854513 = 11 \cdot 131 \cdot 593$）；Entry 20 后例 1 用 $B_{22}$ 的推理有误（同上）；Entry 29 被拉马努金本人划去（$c_{21} = 30 \ne 31 = d_{21}$）；Entry 30 后推论 3 被拉马努金本人划去（$p_n/n - \mathrm{Log}\, n$ 发散）；$\zeta(n)$ 表（p. 127）五处末位数字错误（$\zeta(3)$、$\zeta(10)$、$1/B_3^*$、$1/B_7^*$、$1/B_9^*$）。
- 本轮 OCR 误读纠正（均经 PDF 原图或数值复核证实）：本章 DjVu OCR 的公式部分损坏严重，全部公式均按 PDF 原图（150 DPI，书 pp. 109–132）逐字转录；其中较关键的纠正有：(0.1) 的 $\psi_n(p)$ 定义与 $|\mathrm{Log}(-p)|$；Entry 2 的 (2.1)–(2.3)；Entry 4 的 $(p+1)^{-n-1}$；Entry 6 的 (i)(ii)(iii)；Entry 7 的 (7.1)(7.2)；Entry 8 的 $\psi_5(p)$、$\psi_6(p)$、$\psi_7(p)$ 系数与 $\psi_n(1)$ 公式；Entry 11、12 的 $(-1)^{n-1}$；Entry 13–17 的 $B_{2n}$ 系数；Entry 18 的递推；Entry 20 的 $I_{2n}$ 表值；Entry 22 的 $2^{2n}(2^{2n}-1)$；Entry 25 的 (i)–(iv)；Entry 26 的 (26.1)(26.2)；Entry 29 的 (29.1)。另：第 2 章 Entry 10 与本章 Entry 23/24 均未印出部分分式分解的确切形式，本文件给出的是 Bromwich 的标准形式（已数值复核），并已注明。
- 数值复核小计：本轮共复核 37 项检查（mpmath 30 位 + 精确分数），全部通过：Bernoulli 数表（$n \le 38$）与 $B_{22}$ 分子分解；Euler 数表（$n \le 14$）；$\psi_0,\dots,\psi_7$ 多项式与 $\psi_n(-1)$、$\psi_n(1)$ 公式、$\psi_5(-2) = 541$、$\psi_5(-3) = 1456$；Entry 2(i)(ii)（$\varphi(x) = x^2$，精确分数）；Entry 4、5、6、7；第 8 节例 1、2（$k^5$ 和）；推论 6(iv)（$n = 1,2$）；Entry 11–17（$x = 0.5$）；Entry 18（$n = 2,\dots,7$）；Entry 19(i)(ii)（$n = 1,\dots,12$）；Entry 20 的 $I_{2n}$ 表（$n = 1,\dots,13$）；$B_{200}$ 的分数部分（两种写法）；素数表计数（$\pi(211) = 47$、$\pi(4969) = 665）$；Entry 22（$n = 1,\dots,6$）；Entry 23/24 的八个标准形式（$x = 0.3$，误差 $< 10^{-30}$）；第 24 节后同余式与渐近式；Entry 25(i)–(iv)（$n = 1,2,3$）与 $B^*$、$E^*$ 推论；$\zeta(n)$ 表与五处订正；Entry 26 的 (26.1)(26.2)；$\gamma$ 的 (26.3) 部分和；Entry 27/28 的推论与例题；Entry 29 的 $c_{21} = 30$、$d_{21} = 31$；Entry 30 的推论 1–3（$s = 2$）；推论 2 的极限值 $-0.315708$ 与 Meissel–Mertens 常数 $0.2614972$。
- 与 M 模块的对照：Bernoulli 数与 Euler 数主线见 M01（定义 (I1)(I2)、von Staudt–Clausen 定理、Euler 递推、$\zeta(2n)$ 公式、素数表、素数倒数和发散、Mertens 定理）；Eulerian 多项式与数、第二类 Stirling 数、幂和见 M13；幂级数、对数与三角级数、部分分式分解见 M02；渐近展开（Entry 26、(26.3)、$E_{2n+2h}/E_{2n}$）与 Hurwitz zeta 见 M12；Euler 乘积与 Dirichlet $L$ 函数见 M01、M06；Rogers–Ramanujan 恒等式（Entry 29 的 Ramanujan 对）见 M07、M03；分拆生成函数（Entry 29 的级数展开）见 M05。

## 与 M 模块对照 / 待补

- **M01 伯努利数定义缺口（本章已定位定义出处，待日后补入 M01）：**M02/M06 引用 Bernoulli 数并写「见 M01.3」，但 M01 全文未给 Bernoulli 数定义。本章 Entry 9 即该定义的出处：Berndt 导言 (I1)，$x/(e^x-1) = \sum_{n=0}^{\infty} B_n x^n/n!$（$|x| < 2\pi$），见 Abramowitz–Stegun [1, p. 804]。补入 M01 时应同时补 Euler 数的定义 (I2)（$\sec x = \sum_{n=0}^{\infty} (-1)^n E_{2n} x^{2n}/(2n)!$）与 von Staudt–Clausen 定理（Entry 19(iii)、Entry 20）。**本章文件只记录出处，不顺手改 M01。**
- 其余对照见各条「对照」与小结；$B_s^*$、$E_s^*$ 的推广（Entry 25）与 $\zeta(n)$ 数值表（Entry 26）是 M01–M14 未收的新内容，可供日后扩充 M01 时参考。

## 待核对清单

1. IMSC 整理表计本章的结果数本次未能读取（imsc.res.in 当日不可达），待该表可达后补；Berndt 章首计数本章共 94 条公式或定理陈述（已核实）。
2. Entry 23(i)–(iv) 与 Entry 24(i)–(iv) 的确切表述：Berndt 在本章与第 2 章 Entry 10 中均未印出部分分式分解的公式，只引 Bromwich [1, pp. 217、225]；本文件给出的是 Bromwich 的标准形式（已数值复核），拉马努金在笔记中的原始写法待查 TIFR 影印版后补。
3. Entry 21 第二张素数表的完整造表过程：书中所述三阶段（30n、210n、2310n）已按文字记录；第二张表基数表述中的省略号已按「11 至 211 间全部与 210 互素的数」理解并数值验证（含合数余数 121、143、169、187、209），但拉马努金原始表中的具体排版（竖线分隔、百位数标注）未逐项核对。
4. Entry 7 的 (7.2)：Berndt 亦不清楚拉马努金「取整部分」意指什么，本文件只记录两种表述与 Berndt 的按语，未作推测。
5. Entry 20 的 $I_0 = 0$：$F_0$ 无定义（每个素数都整除 0），$I_0 = 0$ 是约定；$n \ge 1$ 时的 $I_{2n}$ 值已逐项数值核实。
6. 第 20 节例 2「$B_{200}$ 的分数部分」：书中写法是 $B_{200} = \text{整数} - 216641/1366530$；按现代 $\{x\} = x - \lfloor x\rfloor$ 则为 $1149889/1366530$，两种写法均已数值验证，见该条例 2 的「写法说明」。
7. Entry 30 后推论 2 的极限值：本书只断言极限存在，未给值；本文件附记的极限值 $-0.315708$（$\sum_p [\mathrm{Log}(1-1/p) + 1/p]$）与 Meissel–Mertens 常数 $0.2614972$（$\gamma - C$）均已数值验证（素数 $\le 10^6$），但未在 Berndt 原书中出现，属补充注记。
8. 本章 TIFR 影印版（第二本笔记第 5 章）的具体页码未标：Berndt 原书未逐条给出 TIFR 页码，待查 TIFR 1957 年版目录后补；目前只知一条线索——Entry 6(ii) 的笔记原文见 TIFR 第二卷 p. 48。
9. Entry 29 的 Ramanujan 对：Andrews 的猜想与 Hirschhorn、Blecksmith 等人的后续发现均按 Berndt 原书（1985）记录，1985 年之后的进展未追踪。

## 来源说明

- 底本：Bruce C. Berndt, *Ramanujan's Notebooks*, Part I, Springer, 1985, Ch. 5, pp. 109–132。archive.org 全文（`ramanujan_notebooks_i`）：DjVu OCR 文本（563,342 字节）与 PDF（13,201,802 字节，368 叶；**PDF 页 = 书页 + 10**，如书 p. 109 = PDF p. 119）。
- 核对方法：本章 24 页（书 pp. 109–132）均渲染成 150 DPI 图片逐字读过；DjVu OCR 的公式部分损坏严重，全部公式均按 PDF 原图转录，OCR 凡与图片或数值不符者一律纠正并注明；数值复核用 Python + mpmath（30 位）与精确分数（Fraction），本章共复核 37 项检查，见各条「数值复核」与小结。
- IMSC 整理表计本章的结果数本次未能读取（imsc.res.in 当日不可达），待补；该数为 IMSC 表的计数，Berndt 原书未逐章公布条目数，章首的 94 条是 Berndt 本人的计数。
- 本文件只收公式陈述与自写导读/证明思路，不照抄 Berndt 的正文与证明。
