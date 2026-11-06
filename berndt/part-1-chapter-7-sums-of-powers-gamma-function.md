# Part I · 第 7 章 Sums of Powers, Bernoulli Numbers, and the Gamma Function（幂和、Bernoulli 数与 Gamma 函数）

出处：Bruce C. Berndt, *Ramanujan's Notebooks*, Part I, Springer, 1985, 第 7 章，pp. 150–181（第 6 章 pp. 133–149；第 8 章起自 p. 182）。对应拉马努金**第二本笔记第 7 章**。

## 背景与记号

- 本章主题：幂和、Bernoulli 数的推广定义、Riemann zeta 函数 $\zeta(s)$ 及其相关函数、拉马努金的发散级数理论、Gamma 函数。Berndt 在章首说明：本章是第 5、6 章内容的继续；就数值计算的数量而言，本章在第二本笔记中首屈一指——拉马努金显然没有任何机械或电子计算工具的帮助，其计算量之大令人惊叹。
- 本章多次对复变量陈述并证明结果（拉马努金本人显然只考虑实变量；为给出严格证明，Berndt 常需解析延拓，故定理比原意更一般）。复变量记作 $s$（$\sigma = \mathrm{Re}\, s$）、$r$（$u = \mathrm{Re}\, r$）与 $z$。
- 本章的核心记号是幂和
$$\varphi_r(x) = \sum_{k=1}^{x} k^r, \qquad (1.1)$$
$r$ 为任意复数。$r$ 为非负整数时，$\varphi_r(x)$ 是 $x$ 的多项式（见 Entry 1 的 (1.6)）。$u < 0$ 时 $\varphi_r(x)$ 由 (2.3) 推广到复 $x$（见 Entry 2）。
- $B_r^*$ 为第 5 章 Entry 25 定义的任意指标 Bernoulli 数（导言后 (1.7)：$\zeta(r) = (2\pi)^r B_r^* / (2\Gamma(r+1))$；$r = 2n$ 为正偶数时 $B_{2n}^* = (-1)^{n-1} B_{2n}$，化为 Euler 的 $\zeta(2n)$ 公式）。$E_r^*$ 为第 6 章第 25 节定义的推广 Euler 数（见 Entry 17 前的 (17.1)）。$\eta(s)$ 为交错 zeta 函数（(2.1)），$L(s)$ 为 Dirichlet beta 函数（(17.2)）。$c_k$、$A_k$ 为 Stieltjes 常数（Entry 13）。$\gamma$ 为 Euler 常数（拉马努金记作 $c$）。$B_n$ 为 Bernoulli 数（当代定义，见 Ch. 5 Entry 9 与导言 (I1)；M01 伯努利数定义缺口仍待补，见文末）。
- 本章最著名的结果是 Entry 4：拉马努金以发散级数「常数」理论的脆弱推理，重新发现了 $\zeta(s)$ 的函数方程（以伪装形式出现）。Berndt 写道：像 Euler 一样，拉马努金并没有真正的证明；他如何得到这一结果，令人着迷。
- 本章在原文中明确出现编号的 Entry 共 **27 条**：Entry 1–27（Entry 6、19、27 各有 (i)(ii)(iii) 三部分；Entry 9 与 Entry 24 只是前面结果的重述，见各条）。Berndt 未在章首给出本章公式或定理陈述的总数（Ch. 5 章首有「94 条」的计数，本章无对应计数）；IMSC 整理表计本章的结果数本次未能读取（imsc.res.in 当日不可达），待补。
- **本章的拉马努金原文疏失**（Berndt 已指出，详见各条与末尾小结）：Entry 4 推论 6–8 的 (4.4)(4.6)(4.8) 与正确渐近式不相容；Entry 5 笔记误印 $b^r$ 应为 $(2b)^r$；Entry 11 的求导次数与 cot 表末项分母 2385 应为 2835；Entry 11 例 (vi)(vii) 右端错误；Entry 12 的 (12.2)(12.3) 右端符号错误；Entry 13 例 1 的 $+0.0001n^4$ 应为 $-0.0001n^4$ 与多处数值末位错误；Entry 14 的 $a_3$ 值（见该条，本轮发现书内自相矛盾）；Entry 14 推论 2 的 $s^3$、$s^4$ 系数小误差；Entry 19(ii) 拉马努金版不正确；Entry 25 推论 4 的无穷级数符号错误；Entry 26 的 (26.1) 第 10 项起替换与 $\mathrm{Log}\,\Gamma(2/3)$ 的 0.5341990853；Entry 27(i)(ii) 的 $e^{\pi x} - e^{-\pi x}\theta$（已划去）。

## 本章结构

| Entry | 页 | 内容 |
|---|---|---|
| Entry 1 | 150–152 | $\varphi_r(x)$ 的渐近展开 (1.2)；常数 $\zeta(-r)$；(1.6) 与 $B_r^*$ 定义 (1.7)(1.8) |
| Entry 2 | 152–153 | $\eta(-r)$ 公式；$\varphi_r(x)$ 向复 $x$ 的推广 (2.3)–(2.5)；推论 $\varphi_r(-1/2)$ |
| Entry 3 | 153 | 等差数列的幂和 |
| Entry 4 | 153–157 | $\zeta(r)$ 的函数方程（伪装形式）(4.1)(4.2)；推论 1–8 |
| Entry 5 | 157 | 交错等差幂和 (5.1)；笔记误印 $b^r$ 应为 $(2b)^r$ |
| Entry 6(i)(ii) | 157–158 | $(x^2+x)^n$ 的 $\varphi$ 展开；推论 1（$\varphi_1,\dots,\varphi_{11}$ 显式）与推论 2 |
| Entry 7 | 159 | $\varphi_r(x-1) + (-1)^r\varphi_r(-x) = 0$；推论（整除性） |
| Entry 8 | 159–160 | $\varphi_r(x)$ 的 Bernoulli 展开 (8.1)；后一等式原书印文有误（见该条） |
| Entry 9 | 160 | 只是 (2.3) 的重述 |
| Entry 10 | 160 | $\varphi_r$ 的乘法公式 (10.1)；推论 |
| Entry 11 | 161–163 | $\varphi_{-r}$ 与 $\pi\cot\pi x$ 的导数 (11.1)；cot 导数表；推论 (i)–(v) 与例 (i)–(vii) |
| Entry 12 | 163–164 | $2^r$ 恒等式 (12.1)；例 1–4（$\sum 1/(ak+1)^3$） |
| Entry 13 | 164–166 | Stieltjes 常数 $c_k$ 与 $\zeta(s)$ 的 Laurent 展开 (13.2)；例 1–7（数值） |
| Entry 14 | 166–169 | $\sum 1/(k(k^n-1))$ 的渐近 (14.1)；$a_0$、$a_1$、$a_{k+1}$；推论 1–2 |
| Entry 15 | 169 | Hurwitz 公式推论（正弦级数） |
| Entry 16 | 169–170 | Hurwitz 公式推论（余弦级数）；推论 16(i)(ii) |
| Entry 17 | 170–171 | $\varphi_r(-1/4) - \varphi_r(-3/4)$ 与 $E_r^*$；推论（Dirichlet beta） |
| Entry 18 | 171–172 | $L(r)$ 的函数方程 (18.1)；推论 |
| Entry 19(i)(ii) | 172–173 | Cor 16(i)(ii) 的奇 $q$ 版本；推论 1–2 |
| Entry 20 | 173 | $q = 3$ 的特例 |
| Entry 21 | 173–174 | $\varphi_\infty$ 与二项期望 (21.1)–(21.3)；递推 $\varphi_r$ 含义不明 |
| Entry 22 | 174–175 | $\sum 1/(k^n(k+1)^n)$（与 Ch. 9 Entry 35 相同）；例 $n = 3$ |
| Entry 23 | 175 | Stirling 展开；推论（$e^x\Gamma(x+1)/x^x$ 近似） |
| Entry 24 | 175 | 第 4 节推论 3、推论 2 的重述 |
| Entry 25 | 175–176 | Gauss 乘法定理；推论 1–4（$\Gamma(2/3)$、Legendre 倍元公式、$\mathrm{Log}\,\Gamma(z+1/2)$） |
| Entry 26 | 176–177 | $\mathrm{Log}\,\Gamma(z+1)$ 的 Maclaurin 级数；推论 (26.1)；例 1–3 |
| Entry 27(i)(ii)(iii) | 177–180 | 无穷乘积 $\prod (1+z^2/(n+k)^2)$ 的三个公式 |

## Entry 1——幂和的渐近展开

**陈述。**设 $\varphi_r(x)$ 如 (1.1)，$r$ 为任意复数。则若 $r \ne -1$，当 $x \to \infty$ 时，
$$\varphi_r(x) \sim \zeta(-r) + \frac{x^{r+1}}{r+1} + \frac{x^r}{2} + \sum_{k=1}^{\infty} \frac{B_{2k}\Gamma(r+1)x^{r-2k+1}}{(2k)!\Gamma(r-2k+2)}. \qquad (1.2)$$
$r = -1$ 的类似结果属于 Euler，见 Ch. 8 Entry 2。证明：对 $f(t) = t^r$ 用 Euler–Maclaurin 公式 (I3)，常数 $c$ 经 (1.5) 与解析延拓化为 $\zeta(-r)$（(1.4)）。

若 $r$ 为非负整数，(1.2) 中的级数有限，可把渐近号换成等号；(1.2) 化为熟知的公式
$$\varphi_r(x) = \frac{B_{r+1}(x+1) - B_{r+1}(1)}{r+1}, \qquad (1.6)$$
其中 $B_n(x)$ 为第 $n$ 个 Bernoulli 多项式。

在 Ch. 5 第 25 节，拉马努金把 Bernoulli 数 $B_r^*$ 推广到任意指标：
$$\zeta(r) = \frac{(2\pi)^r}{2\Gamma(r+1)} B_r^*. \qquad (1.7)$$
特别 $r = 2n$ 为正偶数时 $B_{2n}^* = (-1)^{n-1}B_{2n}$，(1.7) 化为 Euler 著名的 $\zeta(2n)$ 公式。用 $\zeta(s)$ 的函数方程（见 Entry 4）得
$$\zeta(-r) = \frac{B_{r+1}^*\cos\{\pi(r+1)/2\}}{r+1}. \qquad (1.8)$$
在拉马努金的 (1.2) 版本中，$\zeta(-r)$ 由 (1.8) 的右端代替。Entry 1 之后，拉马努金对级数的「常数」作了一些说明（见 Ch. 6）；Entry 1 中的「常数」就是渐近展开 (1.2) 中的常数项 $\zeta(-r)$。

**出处。**Berndt Part I, Ch. 7, Entry 1, pp. 150–152。

**状态。**已证明。数值复核：$r = 2$、$x = 10$ 时 (1.2) 右端有限和恰为 $\varphi_2(10) = 385$（精确）；$r = 1/2$、$x = 100$ 时左端 $\sum_{k=1}^{100} \sqrt{k} = 671.462947103$，(1.2) 前三项给出 $671.462947108$（差 $5.2\times 10^{-9}$）；(1.6) 在 $r = 3$、$x = 2$ 时得 $9 = 1 + 8$（精确）。

**对照。**幂和与 Euler–Maclaurin 公式见 M12；Bernoulli 数与 $\zeta(2n)$ 见 M01；$\varphi_r(x)$ 的多项式形式见 M13（Ch. 5 Entry 2 的 $F_{2n+1}$）。

## Entry 2——$\eta(-r)$ 与 $\varphi_r(x)$ 向复 $x$ 的推广

**陈述。**对 $\sigma > 0$，定义
$$\eta(s) = \sum_{k=1}^{\infty} (-1)^{k+1} k^{-s}. \qquad (2.1)$$
则 $\eta(s) = (1 - 2^{1-s})\zeta(s)$（(2.2)，由解析延拓对一切复 $s$ 成立）。

**Entry 2。**对每个复数 $r$，
$$\eta(-r) = \frac{(2^{r+1}-1)B_{r+1}^*\sin(\pi r/2)}{r+1}.$$
证明：在 (2.2) 中置 $s = -r$，用 (1.8)。

为把 $\varphi_r(x)$ 的定义推广到复 $x$，先对 $u < 0$ 重新定义
$$\varphi_r(x) = \sum_{k=1}^{\infty} \{k^r - (k+x)^r\}. \qquad (2.3)$$
若 $u < -1$，则
$$\varphi_r(x) = \zeta(-r) - \psi(-r, x+1), \qquad (2.4)$$
其中 $\psi(s, x) = \sum_{k=1}^{\infty} (k+x)^{-s}$，与 Hurwitz zeta 函数 $\zeta(s, x)$ 密切相关（通常只对 $0 < x \le 1$ 定义）。由解析延拓，(2.4) 定义一切复 $x$、$r$ 的 $\varphi_r(x)$。若 $u < 0$ 且 $x$ 为正整数，(2.3) 给出 $\varphi_r(x) = \sum_{k=1}^{x} k^r$（(2.5)），与旧定义一致；若 $r$ 为非负整数且 $-1 < x \le 0$，则 (2.4) 与 $\psi(-r, x+1) = -B_{r+1}(x+1)/(r+1)$ 给出 (1.6)，故 (2.4) 与 (1.6) 一致。

**推论。**若 $r$ 为复数且 $r \ne -1$，则
$$\varphi_r(-\tfrac12) = \frac{(2-2^{-r})B_{r+1}^*\cos\{\pi(r+1)/2\}}{r+1}.$$
证明：由 (2.3)，$u < 0$ 时 $\varphi_r(-1/2) = -2^{-r}\eta(-r)$（(2.6)）；解析延拓后对一切 $r \ne -1$ 成立，再用 Entry 2。若 $r$ 为正整数，推论等价于熟知的 $B_{r+1}(1/2) = -(1-2^{-r})B_{r+1}$。

**出处。**Berndt Part I, Ch. 7, Entry 2, pp. 152–153。

**状态。**已证明。数值复核：推论在 $r = 1$ 时两边均为 $-1/8$（精确分数）；$r = 2$ 时两边均为 $0$（$\cos(3\pi/2) = 0$）。

**对照。**交错 zeta 函数 $\eta(s)$ 见 M01、M02；Hurwitz zeta 函数见 M01、M10；Bernoulli 多项式在 $1/2$ 处的值见 M01。

## Entry 3——等差数列的幂和

**陈述。**设 $\varphi_r(x)$ 由 (2.4) 定义，$a$、$b$ 为复数，$b \ne 0$。则
$$\sum_{k=1}^{x} (a+kb)^r = b^r\left\{\varphi_r\left(x + \frac{a}{b}\right) - \varphi_r\left(\frac{a}{b}\right)\right\}.$$
证明：$r < 0$ 时由 (2.3) 直接得到；一般 $r$ 由解析延拓得到。

**出处。**Berndt Part I, Ch. 7, Entry 3, p. 153。

**状态。**已证明。

**对照。**等差数列幂和见 M01、M13；$\varphi_r$ 的平移公式见 M02。

## Entry 4——$\zeta(r)$ 的函数方程（伪装形式）

**陈述。**对任意复数 $r$，
$$\frac{\sin(\pi r/2)B_{1-r}^*}{1-r} = \zeta(r) = \frac{(2\pi)^r}{2\Gamma(r+1)} B_r^*. \qquad (4.1)$$
证明（Berndt 明言：这是拉马努金饶有趣味的论证，**并不严格**）。把 (1.6) 改写成拉马努金的记号：$r$ 为自然数时
$$\varphi_r(x) = \frac{B_{r+1}(x+1) - \sin(\pi r/2)B_{r+1}^*}{r+1},$$
现假设此式对一切 $r$ 成立，则 $\varphi_{-r}(x)$ 的「常数」是 $\sin(\pi r/2)B_{1-r}^*/(1-r)$；另一方面，由 (1.4) 与 (1.7)，「常数」也等于 $\zeta(r) = (2\pi)^r B_r^*/(2\Gamma(r+1))$。两常数必相等，故 (4.1) 成立。

(4.1) 推出
$$\zeta(r) = 2(2\pi)^{r-1}\Gamma(1-r)\zeta(1-r)\sin\left(\frac{\pi r}{2}\right). \qquad (4.2)$$
即 $\zeta(r)$ 的函数方程（Titchmarsh）。Berndt 感叹：拉马努金竟以如此非正统的方式导出了 $\zeta(r)$ 的函数方程！

**推论 1。**$B_{-2}^* = 2\zeta(3)$，$B_{-4}^* = -4\zeta(5)$，$B_{-6}^* = 6\zeta(7)$，$B_{-8}^* = -8\zeta(9)$（(4.1) 第一式的特例）。

**推论 2。**$\Gamma(1/2) = \sqrt{\pi}$。

**推论 3。**对每个复数 $z$，$\Gamma(z)\Gamma(1-z) = \pi/\sin\pi z$（Euler 反射公式；拉马努金的证明：(4.1) 中分别取 $r = -z$ 与 $r = z+1$，两式相乘，用 $\Gamma(z+2) = (z+1)z\Gamma(z)$ 化简）。

**推论 4。**
$$\pi\sum_{k=0}^{\infty} \frac{(-1)^k}{\sqrt{2k}+\sqrt{2k+2}} = \sum_{k=0}^{\infty} \frac{1}{(2k+1)^{3/2}}.$$
拉马努金的证明本质上有误（由 (2.1)（$s = -1/2$）、(2.2) 与 (4.2) 的推导中，对发散级数的重排不合法）。事实上推论 4 是恒等式
$$\pi^{p+1}\sum_{k=0}^{\infty} (-1)^k\{(k+1)^p - k^p\} = 4\sin\left(\frac{\pi p}{2}\right)\Gamma(p+1)\sum_{k=0}^{\infty} \frac{1}{(2k+1)^{p+1}}$$
在 $p = 1/2$ 的特例（Titchmarsh，$0 < p < 1$）。拉马努金另有与推论 4 类似的结果（Kesava Menon 给出更简单的证明并证明了更多同类结果）。

**推论 5。**设 $\eta(s)$ 由 (2.1) 定义，则
$$(2\pi)^{2/3}\eta(\tfrac13) = (1+2^{1/3})\Gamma(\tfrac23)\eta(\tfrac23).$$
证明：把 (4.2) 用 $\eta$ 改写，取 $r = 1/3$ 化简。

**推论 6。**当 $x \to \infty$ 时，
$$\sum_{k=1}^{x} \frac{1}{\sqrt{k}} \sim 2\sqrt{x} + \zeta(\tfrac12) + \frac{1}{2\sqrt{x}} - \sum_{k=1}^{\infty} \frac{B_{2k}}{(2k)!}\frac{1\cdot 3\cdots(4k-3)}{2^{2k-1}}x^{-2k+1/2}. \qquad (4.3)$$
这是 (1.2) 的特例。但拉马努金（p. 79）断言
$$\sum_{k=1}^{x} \frac{1}{\sqrt{k}} \sim \sqrt{2+4x} + \zeta(\tfrac12). \qquad (4.4)$$
(4.3) 与 (4.4) 不相容：$\sqrt{2+4x} = 2\sqrt{x} + 1/(2\sqrt{x}) - 1/(16x^{3/2}) + \cdots$，前两项与 (4.3) 一致，但第三项与 (4.3) 的 $-x^{-3/2}/24$ 不同。拉马努金未说明如何得到 $\sqrt{2+4x}$ 这一近似。

**推论 7。**当 $x \to \infty$ 时，
$$\sum_{k=1}^{x} \sqrt{k} \sim \tfrac23 x^{3/2} + \tfrac12 x^{1/2} - \frac{1}{4\pi}\zeta(\tfrac32) + \tfrac{1}{24}x^{-1/2} + \sum_{k=2}^{\infty} \frac{B_{2k}}{(2k)!}\frac{1\cdot 3\cdots(4k-5)}{2^{2k-1}}x^{-2k+3/2}. \qquad (4.5)$$
这是 Entry 1 与函数方程 (4.2) 的特例。但拉马努金提出的是
$$\sum_{k=1}^{x} \sqrt{k} \sim \tfrac23\sqrt{(x+\tfrac14)(x+\tfrac12)(x+\tfrac34)} - \frac{1}{4\pi}\zeta(\tfrac32), \qquad (4.6)$$
(4.5) 与 (4.6) 决不相容：(4.5) 中的无穷级数发散，而 (4.6) 右端在 $x \to \infty$ 附近收敛；不过 (4.6) 的右端确实是左端的一个好的近似。Gates 得到了 $\varphi_{1/2}(x)$ 的类似近似。

**推论 8。**当 $x \to \infty$ 时，
$$\sum_{k=1}^{x} k^{3/2} \sim \tfrac25 x^{5/2} + \tfrac12 x^{3/2} + \tfrac18 x^{1/2} - \frac{3}{16\pi^2}\zeta(\tfrac52) - 3\sum_{k=2}^{\infty} \frac{B_{2k}}{(2k)!}\frac{1\cdot 3\cdots(4k-7)}{2^{2k-1}}x^{-2k+5/2}. \qquad (4.7)$$
拉马努金则断言
$$\sum_{k=1}^{x} k^{3/2} \sim \tfrac25\left(x(x+\tfrac14)(x+\tfrac12)(x+\tfrac34)(x+1) + \tfrac{5}{768}(x+\tfrac12)\right)^{1/2} - \frac{3}{16\pi^2}\zeta(\tfrac52), \qquad (4.8)$$
(4.7) 与 (4.8) 同样不相容（理由同推论 7），但 (4.8) 的右端仍是左端的好近似。

**出处。**Berndt Part I, Ch. 7, Entry 4, pp. 153–157。

**状态。**(4.1)(4.2) 已证明（Berndt 的证明严格；拉马努金本人的论证不严格）。推论 1–3、5–8 已证明；推论 4 的等式本身成立，但拉马努金的证明有误。数值复核：推论 1（$B_{-2}^* = 2\zeta(3)$，由 (4.1) 直接得）；推论 4 两边均为 $1.68876118666\cdots$（即 $(1-2^{-3/2})\zeta(3/2)$，30 位）；推论 5 两边差 $9.9\times 10^{-31}$；推论 6 在 $x = 100$ 时左端 $18.5896038248$，(4.3) 前三项 $18.5896038245$（差 $2.6\times 10^{-10}$）；推论 7 在 $x = 100$ 时左端 $671.462947103$，(4.5) 前四项 $671.462947108$（差 $5.2\times 10^{-9}$）；推论 8 在 $x = 100$ 时左端 $40501.2245153$，(4.7) 前四项 $40501.2245148$（差 $5.2\times 10^{-7}$）。

**对照。**$\zeta$ 函数方程与反射公式见 M01、M10；$\Gamma(1/2) = \sqrt{\pi}$ 见 M10；$\varphi_{1/2}$、$\varphi_{3/2}$ 的渐近见 M12；Dirichlet eta 函数见 M01、M02。

## Entry 5——交错等差幂和

**陈述。**设 $a$、$b$ 为复数，$b \ne 0$，$a/b$ 不是负整数。若 $u < -1$，则
$$\sum_{k=1}^{\infty} (-1)^{k+1}(a+kb)^r = (2b)^r\left\{\varphi_r\left(\frac{a}{2b}\right) - \varphi_r\left(\frac{a-b}{2b}\right)\right\}. \qquad (5.1)$$
证明：$\sum_{k=1}^{\infty} (-1)^{k+1}(a+kb)^r = \sum_{k=1}^{\infty} (a+(2k-1)b)^r - \sum_{k=1}^{\infty} (a+2kb)^r$，由 (2.3) 的定义即得。

笔记中有误印（p. 79）：拉马努金在 (5.1) 右端写的是 $b^r$ 而非 $(2b)^r$。

**出处。**Berndt Part I, Ch. 7, Entry 5, p. 157。

**状态。**已证明。数值复核：$a = 1$、$b = 1$、$r = -2$ 时左端 $1 - \eta(2) = 1 - \pi^2/12 = 0.177532966576\cdots$，右端 $(1/4)\varphi_{-2}(1/2) = 0.177532966576\cdots$（差 $4.9\times 10^{-32}$）。

**对照。**交错级数与 $\eta$ 函数见 M02；$\varphi_r$ 的平移公式见 Entry 3。

## Entry 6(i)(ii)——$(x^2+x)^n$ 的 $\varphi$ 展开

**陈述。**设 $x$ 为正整数，$n > 0$。则

**Entry 6(i)。**
$$(x^2+x)^n = 2\sum_{k=0}^{\infty} \binom{n}{2k+1}\varphi_{2n-2k-1}(x).$$
证明思路：对 $|z| \ge 1$，$(z^2+z)^n - (z^2-z)^n = 2z^{2n}\sum_{k=0}^{\infty} \binom{n}{2k+1}z^{-2k-1}$（(6.1)，二项式定理）；置 $z = j$ 并对 $j = 1,\dots,x$ 求和，交换求和次序，用 (1.1) 即得。

**Entry 6(ii)。**在同样假设下，
$$(x+\tfrac12)(x^2+x)^n = \sum_{k=0}^{\infty} \left\{2\binom{n}{2k+1} + \binom{n}{2k}\right\}\varphi_{2n-2k}(x).$$
证明与 (i) 类似，用 $(z+\tfrac12)(z^2+z)^n - (z-\tfrac12)(z^2-z)^n$ 的展开 (6.2)。

若 $n$ 为正整数，Entry 6(i)(ii) 对一切 $x$ 成立（多项式恒等式）。

**推论 1。**设 $y = x^2+x$，$a = x+\tfrac12$。则
$$\begin{aligned}
\varphi_1(x) &= \tfrac12 y, & \varphi_2(x) &= \tfrac13 ay, & \varphi_3(x) &= \tfrac14 y^2,\\
\varphi_4(x) &= \tfrac15 ay(y-\tfrac13), & \varphi_5(x) &= \tfrac16 y^2(y-\tfrac12),\\
\varphi_6(x) &= \tfrac17 ay(y^2-y+\tfrac13), & \varphi_7(x) &= \tfrac18 y^2(y^2-\tfrac43 y+\tfrac23),\\
\varphi_8(x) &= \tfrac19 ay(y^3-2y^2+\tfrac95 y-\tfrac35),\\
\varphi_9(x) &= \tfrac{1}{10}y^2(y-1)(y^2-\tfrac32 y+\tfrac32),\\
\varphi_{10}(x) &= \tfrac{1}{11}ay(y-1)(y^3-\tfrac73 y^2+\tfrac{19}{3}y-\tfrac53),\\
\varphi_{11}(x) &= \tfrac{1}{12}y^2(y^4-4y^3+\tfrac{17}{2}y^2-10y+5).
\end{aligned}$$
奇指标公式由 Entry 6(i) 依次取 $n = 1,\dots,6$ 得到；偶指标公式由 Entry 6(ii) 依次取 $n = 1,\dots,5$ 得到。这些公式早已为人所知（是 (1.6) 的特例），但拉马努金用 Entry 6(i)(ii) 求它们的方法特别简短优雅。$r$、$x$ 为正整数时求 $\varphi_r(x)$ 的其他公式与方法，见 Snow 的综述文章。

**推论 2。**对每个正整数 $n$，有
$$\begin{aligned}
\text{(i)}\quad \sum_{k=1}^{n} \left(\frac{2k-1+\sqrt{5}}{2}\right)^9 &= \varphi_9\left(\frac{2n-1+\sqrt{5}}{2}\right),\\
\text{(ii)}\quad \sum_{k=1}^{n} \left(\frac{2k-1+\sqrt{5}}{2}\right)^{10} &= \varphi_{10}\left(\frac{2n-1+\sqrt{5}}{2}\right).
\end{aligned}$$
若 $p$、$n$ 为正整数且 $n$ 为偶数，则
$$\text{(iii)}\quad \sum_{k=1}^{p} (2k-1)^n = 2^n\varphi_n(p-\tfrac12).$$
证明：(i) 用 Entry 3（$r = 9$、$x = n$、$a = (\sqrt{5}-1)/2$、$b = 1$），并用推论 1 知 $(\sqrt{5}-1)/2$ 是 $\varphi_9(x)$ 的根；(ii) 同理（$\varphi_{10}((\sqrt{5}-1)/2) = 0$）；(iii) 用 Entry 3（$r = n$、$x = p$、$a = -1$、$b = 2$）与 Entry 2 的推论 $\varphi_n(-1/2) = 0$（$n$ 偶数时）。

**注记（本轮核对发现，原书误印）。**原书推论 2(i) 左端的分母印作 $9$，即 $\sum_{k=1}^{n} ((2k-1+\sqrt{5})/9)^9$。数值复核表明分母应为 $2$：$n = 1$ 时分母取 2 的左端与右端差 $8.8\times 10^{-29}$，分母取 9 的差为 $76.0$；$n = 2$ 时分母取 2 的差为 $0$（精确），分母取 9 的差为 $5.85\times 10^{3}$。且证明过程（Entry 3，$a = (\sqrt{5}-1)/2$、$b = 1$）给出分母 $2$。原书的 $9$ 疑为指数 $9$ 误入分母。

**出处。**Berndt Part I, Ch. 7, Entry 6, pp. 157–158。

**状态。**已证明（推论 2(i) 的分母按数值与证明过程订正为 $2$，见注记）。数值复核：Entry 6(i) 在 $x = 2$、$n = 2$ 时两边均为 $36$（精确分数）；推论 1 的 $\varphi_5(2) = 33 = (1/6)\cdot 36\cdot(11/2)$（精确）；推论 2(iii) 在 $n = 2$、$p = 3$ 时两边均为 $35$（精确）。

**对照。**幂和的显式多项式见 M01、M13；二项式系数恒等式见 M13；$\varphi_9$、$\varphi_{10}$ 在 $(\sqrt{5}-1)/2$ 处为零见 M14（黄金比例）。

## Entry 7——$\varphi_r$ 的反射恒等式

**陈述。**若 $r$ 为正整数，则
$$\varphi_r(x-1) + (-1)^r\varphi_r(-x) = 0.$$
证明：由 (1.6)，左端 $= \{B_{r+1}(x) + (-1)^r B_{r+1}(1-x)\}/(r+1)$；由 Bernoulli 多项式的熟知性质（Abramowitz–Stegun），右端为 $0$。

**推论。**若 $r$ 为大于 $1$ 的正整数，则 $\varphi_r(x)$ 可被 $x^2(x+1)^2$（$r$ 为奇数）或 $x(x+\tfrac12)(x+1)$（$r$ 为偶数）整除。证明：由 Entry 6(i)(ii) 对 $r$ 归纳即得。

**出处。**Berndt Part I, Ch. 7, Entry 7, p. 159。

**状态。**已证明。数值复核：$r = 2$、$x = 3$ 时 $\varphi_2(2) + \varphi_2(-3) = 5 + (-5) = 0$（精确分数）；推论在 $r = 3$ 时 $\varphi_3(0) = \varphi_3(-1) = 0$。

**对照。**Bernoulli 多项式的反射性质见 M01；$\varphi_r(x)$ 的因式分解见 M13、M14。

## Entry 8——$\varphi_r(x)$ 的 Bernoulli 展开

**陈述。**若 $r$ 为正整数，则
$$\varphi_r(x) = \frac{1}{r+1}\sum_{k=0}^{r} \binom{r+1}{k}B_k x^{r+1-k} + x^r = \frac{x^{r+1}}{r+1} + \frac{x^r}{2} - 2\sum_{k=1}^{[r/2]} \binom{r+1}{2k}k\zeta(1-2k)x^{r+1-2k}. \qquad (8.1)$$
证明：用 Bernoulli 多项式公式 $B_r(x) = \sum_{k=0}^{r} \binom{r}{k}B_k x^{r-k}$（Abramowitz–Stegun）于 (1.6)，并由 $\varphi_r(x) = \varphi_r(x-1) + x^r$ 得第一等式；后一等式据称由 (4.1) 得到。

**注记（本轮核对发现，原书印文有误）。**原书 (8.1) 的后一等式按印文不成立。数值复核（$x = 1.7$）：$r = 2$ 时左端 $\varphi_2(1.7) = 3.366\cdots$，第一等式给出 $3.366\cdots$（差 $3.9\times 10^{-31}$），后一等式按印文给出 $3.932666667$（差 $0.567$）；$r = 3$ 时后一等式按印文差 $2.17$。正确的后一等式应为
$$\varphi_r(x) = \frac{x^{r+1}}{r+1} + \frac{x^r}{2} - \frac{2}{r+1}\sum_{k=1}^{[r/2]} \binom{r+1}{2k}k\zeta(1-2k)x^{r+1-2k},$$
即系数 $-2$ 应为 $-2/(r+1)$（因 $\zeta(1-2k) = -B_{2k}/(2k)$，第一等式的 $k = 2m$ 项为 $\binom{r+1}{2m}B_{2m}x^{r+1-2m}/(r+1)$）。$r = 2$ 时误差恰为 $x(1/2-1/6) = 0.5667$，即 $(r+1)$ 倍之差的直接证据。此式按订正后的系数复核通过。原书印文缺因子 $1/(r+1)$，疑为误印，待核对。

**出处。**Berndt Part I, Ch. 7, Entry 8, pp. 159–160。

**状态。**第一等式已证明；后一等式原书印文经数值复核不成立（见注记），订正形式已数值复核通过。

**对照。**Bernoulli 数与 $\zeta$ 在负整数处的值见 M01；$\varphi_r(x)$ 的显式公式见 M13。

## Entry 9——(2.3) 的重述

**陈述。**Entry 9 只是 (2.3) 的重述。

**出处。**Berndt Part I, Ch. 7, Entry 9, p. 160。

**状态。**定义（见 Entry 2 的 (2.3)）。

**对照。**见 Entry 2。

## Entry 10——$\varphi_r$ 的乘法公式

**陈述。**对每个复数 $r$ 与每个正整数 $n$，
$$\varphi_r(x) - n^r\sum_{k=0}^{n-1} \varphi_r\left(\frac{x-k}{n}\right) = (1-n^{r+1})\zeta(-r) = (n^{r+1}-1)\frac{\sin(\pi r/2)B_{r+1}^*}{r+1}. \qquad (10.1)$$
证明：$u < -1$ 时由 (2.3) 直接计算得 (10.2)；解析延拓后对一切 $r$ 成立；第二等式由 (4.1) 得到。

**推论。**在 Entry 10 的假设下，
$$\sum_{k=1}^{n-1} \varphi_r(-k/n) = (n-n^{-r})\zeta(-r).$$
证明：在 Entry 10 中置 $x = 0$，用 $\varphi_r(0) = 0$。

**出处。**Berndt Part I, Ch. 7, Entry 10, p. 160。

**状态。**已证明。数值复核：$r = 2$、$n = 3$、$x = 2$ 时左端 $= 4.1\times 10^{-15}$（Hurwitz zeta 数值计算的舍入量级内为 $0$，与右端 $(1-27)\zeta(-2) = 0$ 一致）。

**对照。**乘法公式（分布关系）见 M01、M10（Gauss 乘法定理见 Entry 25）；$\zeta$ 在负整数处的值见 M01。

## Entry 11——$\varphi_{-r}$ 与 $\pi\cot\pi x$ 的导数

**陈述。**若 $r$ 为正整数，则
$$\varphi_{-r}(x-1) + (-1)^r\varphi_{-r}(-x) = \{1+(-1)^r\}\zeta(r) + \frac{(-1)^r}{(r-1)!}\frac{d^{r-1}}{dx^{r-1}}(\pi\cot\pi x), \qquad (11.1)$$
其中 $r = 1$ 时右端第一项理解为 $0$。证明：由 (2.3) 得左端 $= \{1+(-1)^r\}\zeta(r) - \sum_{k=0}^{\infty} \{1/(k+x)^r + 1/(x-k-1)^r\}$；用 $\pi\cot\pi x = \sum_{k=0}^{\infty} \{1/(k+x) + 1/(x-k-1)\}$ 求导即得。

拉马努金在笔记（p. 81）中给出的是 (11.1) 中 $r$ 换成 $-r$ 的形式，并称它是对 $\varphi_{-1}(x-1) - \varphi_{-1}(-x) = -\pi\cot(\pi x)$ 求导 $r$ 次得到的；正确的求导次数是 $-r-1$。拉马努金还指出 (11.1) 对负 $r$ 与正 $r$ 同样成立，从而可推出 Entry 7——若把 $(-1)^r/(r-1)! \cdot d^{r-1}/dx^{r-1}\cot(\pi x)$ 在 $r < 0$ 时理解为恒等于 $0$，则确实得到 Entry 7（但这并不证明 Entry 7）。

拉马努金接着给出计算 $\cot(\pi x)$ 各阶导数的方法（Berndt 不确定其方法是什么；下表的方法是 Berndt 给出的简单方法，由 $y = \cot(\pi x)$、$\tan^{-1}(1/y) = \pi x$ 求导得 $dy/dx = -\pi(y^2+1)$（(11.2)），逐次求导即得）。下表列出 $(-1)^k/(\pi^k k!) \cdot d^k y/dx^k$（$y = \cot\pi x$），$k = 0,\dots,9$：

| $k$ | $(-1)^k/(\pi^k k!) \cdot d^k y/dx^k$ |
|---|---|
| 0 | $y$ |
| 1 | $y^2+1$ |
| 2 | $y^3+y$ |
| 3 | $y^4+\frac43 y^2+\frac13$ |
| 4 | $y^5+\frac53 y^3+\frac23 y$ |
| 5 | $y^6+2y^4+\frac{17}{15}y^2+\frac{2}{15}$ |
| 6 | $y^7+\frac73 y^5+\frac{77}{45}y^3+\frac{17}{45}y$ |
| 7 | $y^8+\frac83 y^6+\frac{12}{5}y^4+\frac{248}{315}y^2+\frac{17}{315}$ |
| 8 | $y^9+3y^7+\frac{16}{5}y^5+\frac{88}{63}y^3+\frac{62}{315}y$ |
| 9 | $y^{10}+\frac{10}{3}y^8+\frac{37}{9}y^6+\frac{424}{189}y^4+\frac{1382}{2835}y^2+\frac{62}{2835}$ |

表中公式拉马努金全都给对了，只有一处例外：最后一项的最后一个分母，他写的是 2385，应为 2835。

**推论。**若 $r$ 为任意复数，则
$$\begin{aligned}
\text{(i)}\quad \varphi_r(x) - 2^r\left\{\varphi_r\left(\frac{x}{2}\right) + \varphi_r\left(\frac{x-1}{2}\right)\right\} &= (1-2^{r+1})\zeta(-r),\\
\text{(ii)}\quad \varphi_r(-\tfrac12) &= (2-2^{-r})\zeta(-r),\\
\text{(iii)}\quad \varphi_r(-\tfrac13) + \varphi_r(-\tfrac23) &= (3-3^{-r})\zeta(-r),\\
\text{(iv)}\quad \varphi_r(-\tfrac14) + \varphi_r(-\tfrac34) &= (2+2^{-r}-4^{-r})\zeta(-r),\\
\text{(v)}\quad \varphi_r(-\tfrac16) + \varphi_r(-\tfrac56) &= (1+2^{-r}+3^{-r}-6^{-r})\zeta(-r).
\end{aligned}$$
证明：(i) 是 Entry 10 在 $n = 2$ 的情形；(ii)–(v) 由 Entry 10 的推论依次取 $n = 2, 3, 4, 6$ 得到。

**例。**若 $r$ 为正奇整数，则
$$\begin{aligned}
\text{(i)}\quad \varphi_r(-\tfrac13) &= (3-3^{-r})\zeta(-r)/2,\\
\text{(ii)}\quad \varphi_r(-\tfrac14) &= (1+2^{-r-1}-2^{-2r-1})\zeta(-r),\\
\text{(iii)}\quad \varphi_r(-\tfrac16) &= (1+2^{-r}+3^{-r}-6^{-r})\zeta(-r)/2,\\
\text{(iv)}\quad \varphi_r(-\tfrac15) + \varphi_r(-\tfrac25) &= (5-5^{-r})\zeta(-r)/2,\\
\text{(v)}\quad \varphi_r(-\tfrac18) + \varphi_r(-\tfrac38) &= (2+2^{-2r-1}-2^{-3r-1})\zeta(-r),\\
\text{(vi)}\quad \varphi_r(-\tfrac{1}{10}) + \varphi_r(-\tfrac{3}{10}) &= (3+2^{-r}+5^{-r}-10^{-r})\zeta(-r)/2,\\
\text{(vii)}\quad \varphi_r(-\tfrac{1}{12}) + \varphi_r(-\tfrac{5}{12}) &= (4-2^{-r}+4^{-r}+6^{-r}-12^{-r})\zeta(-r)/2.
\end{aligned}$$
证明：用 Entry 10 的推论与 Entry 7。**拉马努金把 (vi) 与 (vii) 的右端给错了**（p. 83）。这些例子更常表为 Bernoulli 多项式的值（Abramowitz–Stegun，pp. 805–806）。

**出处。**Berndt Part I, Ch. 7, Entry 11, pp. 161–163。

**状态。**已证明（拉马努金版的求导次数、(vi)(vii) 右端与 cot 表末项分母均已按 Berndt 纠正）。数值复核：(11.1) 在 $r = 2$、$x = 1/4$ 时两边均为 $-5\pi^2/3$（差 $0$，30 位）；cot 表 $k = 1$、$k = 2$ 两式在 $x = 0.3$ 时逐项成立（差 $\sim 2\times 10^{-31}$）。

**对照。**$\cot$ 的部分分式分解见 M01、M02（Ch. 5 Entry 23）；$\varphi_r$ 在分点处的值见 M01（Bernoulli 多项式）；$\zeta$ 在负整数处的值见 M01。

## Entry 12——$2^r$ 恒等式

**陈述。**对每个复数 $r$，
$$2^r\{\varphi_r(-\tfrac16) - \varphi_r(-\tfrac56)\} = (2^r+1)\{\varphi_r(-\tfrac13) - \varphi_r(-\tfrac23)\}. \qquad (12.1)$$
证明：在 Entry 10 中取 $n = 2$、$x = -1/3$ 与 $x = -2/3$，得 (12.2)(12.3)，两式相减并整理即得 (12.1)。上述证明是拉马努金在笔记中给出的，但他不慎把 (12.2) 与 (12.3) 的右端都乘了 $-1$。

**例 1。**$\sum_{k=0}^{\infty} 1/(2k+1)^3 = \frac78\zeta(3)$。

**例 2。**$\sum_{k=0}^{\infty} 1/(3k+1)^3 = \frac{2\pi^3}{81\sqrt{3}} + \frac{13}{27}\zeta(3)$。

**例 3。**$\sum_{k=0}^{\infty} 1/(4k+1)^3 = \frac{\pi^3}{64} + \frac{7}{16}\zeta(3)$。

**例 4。**$\sum_{k=0}^{\infty} 1/(6k+1)^3 = \frac{\pi^3}{36\sqrt{3}} + \frac{91}{216}\zeta(3)$。

例 1 是平凡的；例 2–4 由 $\varphi_{-2n-1}(-2/3)$、$\varphi_{-2n-1}(-3/4)$、$\varphi_{-2n-1}(-5/6)$ 的一般公式得到（Hansen 表，公式 (6.3.10)、(6.3.18)、(6.3.23)）。

**出处。**Berndt Part I, Ch. 7, Entry 12, pp. 163–164。

**状态。**已证明（拉马努金证明中 (12.2)(12.3) 右端的符号错误已按 Berndt 纠正）。数值复核：例 1–4 四式全部通过（30 位，差 $0$ 至 $2\times 10^{-31}$）。

**对照。**$\zeta(3)$ 与奇数倒数立方和见 M01、M02；$\varphi_{-r}$ 在分点处的值见 M01。

## Entry 13——Stieltjes 常数与 $\zeta(s)$ 的 Laurent 展开

**陈述。**对每个非负整数 $k$，定义
$$c_k = \lim_{m\to\infty} \left(\sum_{j=1}^{m} \frac{\mathrm{Log}^k j}{j} - \frac{\mathrm{Log}^{k+1} m}{k+1}\right). \qquad (13.1)$$
则对一切 $s$，
$$\zeta(s) = \frac{1}{s-1} + \sum_{k=0}^{\infty} \frac{(-1)^k c_k}{k!}(s-1)^k. \qquad (13.2)$$
特别若 $A_k = (-1)^k c_k/k!$（$0 \le k < \infty$），则
$$A_0 = \gamma = 0.5772156649, \qquad A_1 = 0.0728158455, \qquad A_2 = -0.00485, \qquad A_3 = -0.00034, \qquad (13.3)$$
其中 $\gamma$ 为 Euler 常数。

拉马努金没有用 (13.1) 明确定义 $c_k$；他说 $c_k$ 是 $\sum_{j=1}^{\infty} (\mathrm{Log}^k j)/j$ 的常数，这与 (13.1) 等价。(13.3) 中 $A_k$（$0 \le k \le 3$）的值在所给的十进位数内正确。

Laurent 级数 (13.2) 在文献中被多次独立发现：Stieltjes 于 1885 年首先建立（并与 Hermite 在书信中详细讨论）；Jensen 于 1887 年重新发现；Hardy 与拉马努金本人各自无证明地陈述过 (13.2)；Briggs–Chowla 于 1955 年再次重新发现；Verma 与 Ferguson（1963）、Lammel（1966）给出证明。常数 $A_k$ 今称 Stieltjes 常数。$c_k$ 的数值计算最早由 Jensen（前 9 个系数，9 位小数）与 Gram（1895 年，前 16 个系数，16 位小数）完成；最 extensive 的计算是 Liang–Todd（前 20 个系数，15 位小数）。$c_k$ 的符号定理见 Briggs 与 Mitrović；$|c_k|$ 的一致界见 Briggs，后由 Berndt、Israilov、Balakrishnan 改进。Hurwitz zeta 函数的 Laurent 系数见 Wilton、Berndt、Lavrik；其他 Dirichlet 级数的推广见 Briggs–Buschman、Knopfmacher、Balakrishnan。

**例 1。**$|n|$ 充分小时，
$$\zeta(1+n) + \zeta(1-n) = \frac{2\gamma}{1 + 0.00839n^2 - 0.0001n^4 + \cdots}.$$
证明：由 Entry 13，$\zeta(1+n) + \zeta(1-n) = 2\gamma + 2A_2 n^2 + 2A_4 n^4 + \cdots = 2\gamma/(1 - (A_2/\gamma)n^2 + (A_2^2/\gamma^2 - A_4/\gamma)n^4 + \cdots)$；用 Liang–Todd 的 $A_0(\gamma)$、$A_2$、$A_4$ 值与计算器即得。**例 1 中拉马努金实际写的是 $+0.0001n^4$ 而非 $-0.0001n^4$**；以下若干例也需要纠正。

**例 2。**$\zeta(\frac{11}{10}) = 10.58444842$。

**例 3。**$\zeta(\frac32) = 2.6123752$。

**例 4。**$\zeta(\frac52) = 1.341490$。

**例 5。**$B_{3/2}^* = 0.4409932$；$B_{1/2}^* = -1.032627$。

**例 6。**$B_{1/3}^* = -0.9420745$；$B_{-1/3}^* = -1.3841347$。

**例 7。**$B_{-1/2}^* = -1.847228$。

按 Gram 的 $\zeta(s)$ 值表（Dwight 的表转载）：$\zeta(11/10)$ 的最后一位应为 6 而非 2；$\zeta(3/2)$ 的最后一位应为 3 而非 2；$\zeta(5/2)$ 的最后两位应为 87 而非 90。Glaisher 的早期表中 $\zeta(11/10)$ 与 $\zeta(3/2)$ 的值到六位小数。拉马努金的五个 $B_r^*$ 值可用 (4.1) 与 $\zeta$ 值表求得：用 $\zeta(3/2)$ 的值，$B_{3/2}^*$ 的最后一位应为 3 而非 2；$B_{1/2}^*$ 与 $B_{-1/2}^*$ 的值正确；计算 $B_{1/3}^*$ 与 $B_{-1/3}^*$ 需用 $\zeta(2/3)$ 与 $\zeta(4/3)$（表中未收，由 Hansen–Patrick 算出），$B_{1/3}^*$ 的最后一位应为 3 而非 5；拉马努金的 $B_{-1/3}^*$ 与其他计算相比颇为不准，正确值为 $-1.3860016$。

**出处。**Berndt Part I, Ch. 7, Entry 13, pp. 164–166。

**状态。**已证明（(13.2) 的历史归属见上文；$A_k$ 数值与例 2–7 的末位按 Berndt 的纠正为准）。数值复核（mpmath 的 Stieltjes 常数，30 位）：$A_0 = 0.5772156649$、$A_1 = 0.072815845484$、$A_2 = -0.0048451816$、$A_3 = -0.0003423057$（与书中四舍五入值一致）；$\zeta(11/10) = 10.584448465\cdots$（末位 6，证实 Berndt 的纠正）；$\zeta(3/2) = 2.6123753487\cdots$（末位 3）；$\zeta(5/2) = 1.3414872573\cdots$（末两位 87）；$B_{3/2}^* = 0.4409932782\cdots$（末位 3）；$B_{1/3}^* = -0.9420742646\cdots$（末位 3）；$B_{-1/3}^* = -1.386001586\cdots$（拉马努金的 $-1.3841347$ 偏差 $0.00187$）；$B_{-1/2}^* = -1.847228324\cdots$（与书中一致）。

**对照。**Stieltjes 常数与 $\zeta(s)$ 在 $s = 1$ 附近的展开见 M01；Euler 常数 $\gamma$ 见 M01、M12；$B_r^*$ 的分数指标值见 M01、M10。

## Entry 14——$\sum 1/(k(k^n-1))$ 的渐近展开

**陈述。**设 $n > 0$。则当 $n \to 0$ 时，
$$\sum_{k=2}^{\infty} \frac{1}{k(k^n-1)} \sim \frac{a_0 - \mathrm{Log}\, n}{n} + a_1 + \sum_{k=1}^{\infty} a_{k+1}n^{2k-1}, \qquad (14.1)$$
其中
$$a_0 = \lim_{m\to\infty} \left(\sum_{k=2}^{m} \frac{1}{k\,\mathrm{Log}\, k} - \mathrm{Log}\,\mathrm{Log}\, m\right) = 0.7946786, \qquad (14.2)$$
$$a_1 = \tfrac12(1-\gamma) = 0.2113922,$$
$$a_{k+1} = -\frac{B_{2k}A_{2k-1}}{2k}, \qquad k \ge 1,$$
$B_j$ 为第 $j$ 个 Bernoulli 数，$A_j$ 由 Entry 13 定义。特别 $a_2 = -0.0060680$，$a_3 = -0.000000475$。

$a_0 + \mathrm{Log}\,\mathrm{Log}\, 2$ 的数值见 Boas 的文章；$a_1$、$a_2$、$a_3$ 的数值可由 (13.3) 确定，或更准确地由 Liang–Todd 的表确定。拉马努金正确给出了 $a_1$ 与 $a_2$，但他给出的 $a_3$ 值 $-0.0000028$ 是不正确的（Berndt 语）。

证明思路：设 $t \ge 1$、$x \ge 0$、$0 < n < A$（$A$ 固定），定义 $f(t) = 1/(t(t^n-1))$、$h(t) = f(t) - 1/(nt\,\mathrm{Log}\, t)$、$g(x) = 1/(e^x-1) - 1/x$；则 $h(t) = g(n\,\mathrm{Log}\, t)/t$，$h'(t) = t^{-2}\{ng'(n\,\mathrm{Log}\, t) - g(n\,\mathrm{Log}\, t)\}$（(14.3)）。对 $g$、$g'$ 用 Taylor 定理（(14.4)），并用 (I1) 得 $g^{(j)}(0)/j! = B_{j+1}/(j+1)!$（(14.5)），得 (14.6)；再对 $h$ 用 Euler–Maclaurin 公式 (I3)（(14.7)(14.8)），算出积分 (14.9)(14.10)，令 $m \to \infty$ 即得 (14.1)。

**注记（本轮核对发现：书内自相矛盾，待核对）。**Berndt 印出的 $a_3 = -0.000000475$ 与他自己印出的系数公式不一致。按公式 $a_{k+1} = -B_{2k}A_{2k-1}/(2k)$ 与 $A_3 = -0.0003423057$（Stieltjes 常数，mpmath 核实），$a_3 = -B_4 A_3/4 = -(-1/30)(-0.0003423057)/4 = -2.8525\times 10^{-6}$；按书中证明的推导（(14.8) 中 $n^j$ 的系数为 $B_{j+1}c_j/(j+1)!$，$c_{2k-1} = -(2k-1)!A_{2k-1}$），同样得到 $a_3 = -2.8525\times 10^{-6}$。直接数值渐近检验（用 $1/(k^n-1) = \sum_{j\ge1} k^{-jn}$ 得 $\sum_{k\ge2} 1/(k(k^n-1)) = \sum_{j\ge1}(\zeta(jn+1)-1)$，$a_0 = 0.7946786456$ 由 $m = 10^7$ 直接求和加尾项修正核实）：$(S(n) - (a_0-\mathrm{Log}\, n)/n - a_1 - a_2 n)/n^3$ 在 $n = 0.3$、$0.2$、$0.15$ 时分别为 $-2.87\times 10^{-6}$、$-2.94\times 10^{-6}$、$-3.14\times 10^{-6}$，趋向公式值 $-2.85\times 10^{-6}$，与书中印值 $-4.75\times 10^{-7}$ 相差约 6 倍。**拉马努金的原值 $-0.0000028$ 与公式值及直接渐近一致（误差约 2%），Berndt 称其「不正确」的判断值得怀疑。**书中印值 $-0.000000475$ 恰等于 $-B_4 A_3/24$，即系数公式的分母若为 $(2k)!$ 而非 $(2k)$ 才会得到的值；究竟是系数公式漏印阶乘，还是 $a_3$ 印值有误，待查他版或勘误表后定。本文件如实记录原书印值与上述矛盾，不擅自改动公式或数值。

**推论 1。**即 (14.2) 的重述。

**推论 2。**对 $s > 0$，
$$\sum_{k=2}^{\infty} \frac{1}{k^{s+1}\,\mathrm{Log}\, k} = -\mathrm{Log}\, s + C + (1-\gamma)s - \sum_{k=2}^{\infty} \frac{A_{k-1}s^k}{k}, \qquad (14.11)$$
其中
$$C = \sum_{k=2}^{\infty} \frac{1}{k^2\,\mathrm{Log}\, k} - 1 + \gamma + \sum_{k=2}^{\infty} \frac{A_{k-1}}{k}, \qquad (14.12)$$
$A_k$（$1 \le k < \infty$）由 Entry 13 定义。又 $C = 0.2174630$，$1-\gamma = 0.4227843$，$-\frac12 A_1 = -0.0364079$，$-\frac13 A_2 = 0.001615$，$-\frac14 A_3 = 0.000086$，$-\frac15 A_4 = -0.00002$。证明：在 (13.2) 中把 $s$ 换成 $x+1$，在 $[1, s]$ 上积分即得。$s^k$（$1 \le k \le 5$）的数值系数现用 Liang–Todd 的表求得；$\sum_{k=2}^{\infty} 1/(k^2\,\mathrm{Log}\, k) = 0.605521788883$ 由 J. R. Hill 在 PDP11/34 计算机上算出；用此值、Liang–Todd 的表与 Berndt 的界 $|A_k| \le 4/(k\pi^k)$ 得到 $C$ 的值。拉马努金的推论 2 版本有些小出入：他的 $s^3$ 与 $s^4$ 系数是 $0.001617$ 与 $0.000085$（正确值为 $0.001615$ 与 $0.000086$）。

**出处。**Berndt Part I, Ch. 7, Entry 14, pp. 166–169。

**状态。**(14.1) 与推论 2 已证明；$a_0$、$a_1$、$a_2$ 已数值核实；$a_3$ 的印值与系数公式矛盾（见注记，待核对）。数值复核：$a_0 = 0.7946786486\cdots$（$m = 10^7$ 直接求和，尾项修正后 $0.7946786456$；书中 $0.7946786$）；$a_1 = (1-\gamma)/2 = 0.2113922\cdots$（差 $3.3\times 10^{-8}$，为书中四舍五入）；$a_2 = -0.0060679871\cdots$（书中 $-0.0060680$）；$\sum_{k=2}^{\infty} 1/(k^2\,\mathrm{Log}\, k) = 0.6055217910\cdots$（直接求和至 $2\times 10^6$ 加尾项积分；书中 $0.605521788883$，差 $2.1\times 10^{-9}$）；$C = 0.21746298\cdots$（书中 $0.2174630$）。

**对照。**Stieltjes 常数见 M01；Euler 常数见 M01、M12；渐近展开与 Euler–Maclaurin 公式见 M12；$\sum 1/(k^2\,\mathrm{Log}\, k)$ 一类常数见 M01。

## Entry 15——Hurwitz 公式推论（正弦级数）

**陈述。**设 $u > -1$，$0 < x < 1$。则
$$\frac{\varphi_r(x-1) - \varphi_r(-x)}{4\Gamma(r+1)} = -\cos\left(\frac{\pi r}{2}\right)\sum_{k=1}^{\infty} \frac{\sin(2\pi kx)}{(2\pi k)^{r+1}}.$$
证明：回顾 Titchmarsh 的 Hurwitz 公式（$\sigma < 1$，$0 < a \le 1$）
$$\zeta(s, a) = 2\Gamma(1-s)\left\{\sin\left(\frac{\pi s}{2}\right)\sum_{k=1}^{\infty} \frac{\cos(2\pi ka)}{(2\pi k)^{1-s}} + \cos\left(\frac{\pi s}{2}\right)\sum_{k=1}^{\infty} \frac{\sin(2\pi ka)}{(2\pi k)^{1-s}}\right\}, \qquad (15.1)$$
由 (2.4) 与 (15.1) 即得。

**出处。**Berndt Part I, Ch. 7, Entry 15, p. 169。

**状态。**已证明。数值复核：$r = -1/2$、$x = 1/4$ 时两边均为 $-0.188352282585\cdots$（差 $2.5\times 10^{-32}$；右端级数按 Dirichlet beta 函数 $\beta(1/2)$ 的闭式求值，直接截断求和因收敛极慢会误报）。

**对照。**Hurwitz zeta 函数见 M01、M10；Fourier 级数与正弦级数见 M02、M12。

## Entry 16——Hurwitz 公式推论（余弦级数）

**陈述。**设 $u > -1$，$0 < x < 1$。则
$$\frac{\varphi_r(x-1) + \varphi_r(-x) - 2\zeta(-r)}{4\Gamma(r+1)} = \sin\left(\frac{\pi r}{2}\right)\sum_{k=1}^{\infty} \frac{\cos(2\pi kx)}{(2\pi k)^{r+1}}.$$
证明与 Entry 15 完全类似。

**推论 16(i)。**设 $p$、$q$ 为整数，$0 < p < q$。则对任意复数 $r$，
$$\frac{(2\pi q)^r}{4\Gamma(r)}\left\{\varphi_{r-1}\left(\frac{p}{q}-1\right) - \varphi_{r-1}\left(-\frac{p}{q}\right)\right\} = -\sin\left(\frac{\pi r}{2}\right)\sum_{j=1}^{q-1} \sin\left(\frac{2\pi jp}{q}\right)\left\{\zeta(r) - \varphi_{-r}\left(\frac{j}{q}-1\right)\right\}. \qquad (16.1)$$

**推论 16(ii)。**在同样假设下，
$$\frac{(2\pi q)^r}{4\Gamma(r)}\left\{\varphi_{r-1}\left(\frac{p}{q}-1\right) + \varphi_{r-1}\left(-\frac{p}{q}\right) - 2(1-q^{-r})\zeta(1-r)\right\} = -\cos\left(\frac{\pi r}{2}\right)\sum_{j=1}^{q-1} \cos\left(\frac{2\pi jp}{q}\right)\left\{\zeta(r) - \varphi_{-r}\left(\frac{j}{q}-1\right)\right\}. \qquad (16.2)$$
证明与 (i) 类似，另用函数方程 (4.2)。

**出处。**Berndt Part I, Ch. 7, Entry 16, pp. 169–170。

**状态。**已证明。数值复核：Entry 16 在 $r = -1/2$、$x = 1/4$ 时两边均为 $0.120659822109\cdots$（差 $0$；右端级数按 $\eta(1/2)$ 的闭式求值）；推论 16(i) 在 $p = 1$、$q = 3$、$r = 3/2$ 时两边差 $2.4\times 10^{-30}$。

**对照。**Hurwitz zeta 函数与 Fourier 级数见 M01、M10、M02；分点处的 $\varphi_r$ 值见 M01。

## Entry 17——$\varphi_r(-1/4) - \varphi_r(-3/4)$ 与 $E_r^*$

**陈述。**以下若干结果需用 Ch. 6 第 25 节拉马努金推广的 Euler 数概念。定义
$$E_r^* = \frac{2\Gamma(r)}{(\pi/2)^r}L(r), \qquad (17.1)$$
$r$ 为任意复数，其中
$$L(s) = \sum_{k=0}^{\infty} (-1)^k(2k+1)^{-s}, \qquad \sigma > 0. \qquad (17.2)$$
$L(s)$（Dirichlet beta 函数）可解析延拓为整函数（Davenport）。

**Entry 17。**对每个复数 $r$，
$$\varphi_r(-\tfrac14) - \varphi_r(-\tfrac34) = \frac{2\cos(\pi r/2)E_{r+1}^*}{4^{r+1}}.$$
证明：在 Entry 15 中取 $x = 1/4$，用 (17.2) 与 (17.1) 即得（解析延拓后对一切 $r$ 成立）。

**推论。**若 $u < 0$，则
$$\sum_{k=0}^{\infty} (-1)^k(2k+1)^r = \tfrac12\cos\left(\frac{\pi r}{2}\right)E_{r+1}^*.$$
证明：由 Entry 17 与 (2.3)，$u < 0$ 时 $2\cos(\pi r/2)E_{r+1}^*/4^{r+1} = \varphi_r(-1/4) - \varphi_r(-3/4) = \sum_{k=1}^{\infty} \{(k-\tfrac34)^r - (k-\tfrac14)^r\} = 4^{-r}\sum_{k=0}^{\infty} (-1)^k(2k+1)^r$。

**出处。**Berndt Part I, Ch. 7, Entry 17, pp. 170–171。

**状态。**已证明。数值复核：Entry 17 在 $r = 1/2$ 时两边差 $2.5\times 10^{-32}$；推论在 $r = -1/2$ 时两边差 $9.9\times 10^{-32}$（$L(s)$ 按 Hurwitz zeta 的闭式 $4^{-s}(\zeta(s,1/4)-\zeta(s,3/4))$ 求值）。

**对照。**Dirichlet beta 函数与 Euler 数见 M01；$\varphi_r$ 在四分点处的值见 M01。

## Entry 18——$L(r)$ 的函数方程

**陈述。**对每个复数 $r$，
$$\cos\left(\frac{\pi r}{2}\right)E_{1-r}^* = 2L(r) = \left(\frac{\pi}{2}\right)^r \frac{E_r^*}{\Gamma(r)}. \qquad (18.1)$$
(18.1) 给出 $L(r)$ 的函数方程
$$L(r) = \cos\left(\frac{\pi r}{2}\right)\left(\frac{\pi}{2}\right)^{r-1}\Gamma(1-r)L(1-r)$$
（见 Davenport，p. 69）。

证明（拉马努金的论证）：由 (17.1)，$L(r)$ 的「常数」是 $(\pi/2)^r E_r^*/(2\Gamma(r))$；而由上一条推论，$L(r)$ 的「常数」也等于 $\frac12\cos(\pi r/2)E_{1-r}^*$；两常数必相等，故 (18.1) 成立。

**推论。**
$$\pi\left(\tfrac12 + \sum_{k=1}^{\infty} \frac{(-1)^k}{\sqrt{2k-1}+\sqrt{2k+1}}\right) = L(\tfrac32).$$
证明与第 4 节推论 4 的证明非常类似（用 Titchmarsh 的相应恒等式，取 $p = 1/2$）。

**出处。**Berndt Part I, Ch. 7, Entry 18, pp. 171–172。

**状态。**已证明。数值复核：(18.1) 在 $r = 1/2$ 时两边差 $0$；推论两边均为 $L(3/2) = 0.864379\cdots$（差 $9.9\times 10^{-32}$）。

**对照。**Dirichlet beta 函数的函数方程见 M01；Euler 数的推广见 M01；交错根式级数见 M02。

## Entry 19(i)(ii)——推论 16(i)(ii) 的奇 $q$ 版本

**陈述。**

**Entry 19(i)。**假设推论 16(i) 的假设成立，并另设 $q$ 为奇数。则
$$\frac{(2\pi q)^r}{4\Gamma(r)}\left\{\varphi_{r-1}\left(\frac{p}{q}-1\right) - \varphi_{r-1}\left(-\frac{p}{q}\right)\right\} = \sin\left(\frac{\pi r}{2}\right)\sum_{j=1}^{(q-1)/2} \sin\left(\frac{2\pi jp}{q}\right)\left\{\varphi_{-r}\left(\frac{j}{q}-1\right) - \varphi_{-r}\left(-\frac{j}{q}\right)\right\}.$$
证明：在 (16.1) 的右端，对 $(q+1)/2 \le j \le q-1$ 的部分把 $j$ 换成 $q-j$。

**Entry 19(ii)。**假设推论 16(ii) 的全部假设成立，并另设 $q$ 为奇数。则
$$\frac{(2\pi q)^r}{4\Gamma(r)}\left\{\varphi_{r-1}\left(\frac{p}{q}-1\right) + \varphi_{r-1}\left(-\frac{p}{q}\right) - 2\zeta(1-r)\right\} = \cos\left(\frac{\pi r}{2}\right)\sum_{j=1}^{(q-1)/2} \cos\left(\frac{2\pi jp}{q}\right)\left\{\varphi_{-r}\left(\frac{j}{q}-1\right) + \varphi_{-r}\left(-\frac{j}{q}\right)\right\}.$$
证明：用 (16.2)，与上一证明同样处理，并用函数方程 (4.2)。

拉马努金的 Entry 19(ii) 版本是不正确的（pp. 86、87）。

**注记（本轮核对发现，原书误印）。**原书 Entry 19(ii) 右端大括号内第一项印作 $\varphi_{-r}(j/p - 1)$。数值复核（$p = 1$、$q = 3$、$r = 3/2$）：左端 $= -2.02839747959\cdots$；按印文（$j/p$）右端 $= -0.36756261665\cdots$（差 $1.66$）；把 $j/p$ 改为 $j/q$ 后右端 $= -2.02839747959\cdots$（差 $3.9\times 10^{-31}$）。且证明所用的 (16.2) 中对应项为 $\varphi_{-r}(j/q-1)$。故原书的 $j/p$ 疑为误印，应为 $j/q$，待核对。本文件按订正后的 $j/q$ 记录公式，并保留此注记。

**推论 1。**设 $u > 0$，$0 \le x < 1$。则
$$\frac{2^{r-1}\pi^{r+1}}{\Gamma(r+1)}\varphi_r(-x) = \sum_{k=1}^{\infty} \frac{\sin(\pi kx)\cos(\pi kx + \pi r/2)}{k^{r+1}}.$$
证明：由 (2.4)、(4.2) 与 (15.1)，并用恒等式 $-\sin A + \sin(A+2B) = 2\sin B\cos(A+B)$。

**推论 2。**若 $0 < x < 1$，则
$$\sum_{k=0}^{\infty} \left(\frac{1}{\sqrt{k+x}} - \frac{1}{\sqrt{k+1-x}}\right) = 2\sum_{k=1}^{\infty} \frac{\sin(2\pi kx)}{\sqrt{k}}.$$
证明：在 Entry 15 中取 $r = -1/2$，用 (2.3)。

**出处。**Berndt Part I, Ch. 7, Entry 19, pp. 172–173。

**状态。**已证明（Entry 19(ii) 右端第一项按数值与证明过程订正为 $j/q$，见注记）。数值复核：Entry 19(i) 在 $p = 1$、$q = 3$、$r = 3/2$ 时两边差 $1.6\times 10^{-30}$。

**对照。**分点处的 $\varphi_r$ 值见 M01；Fourier 正弦级数见 M02；Hurwitz 公式见 M10。

## Entry 20——$q = 3$ 的特例

**陈述。**若 $r$ 为任意复数，则
$$\frac{(6\pi)^r}{2\sqrt{3}\,\Gamma(r)}\left\{\varphi_{r-1}(-\tfrac13) - \varphi_{r-1}(-\tfrac23)\right\} = \sin\left(\frac{\pi r}{2}\right)\left\{\varphi_{-r}(-\tfrac13) - \varphi_{-r}(-\tfrac23)\right\}.$$
证明：在 Entry 19(i) 中取 $p = 1$、$q = 3$ 即得。

**出处。**Berndt Part I, Ch. 7, Entry 20, p. 173。

**状态。**已证明。数值复核：$r = 3/2$ 时两边差 $3.9\times 10^{-31}$。

**对照。**见 Entry 19(i)；三分点处的 $\varphi_r$ 值见 M01。

## Entry 21——$\varphi_\infty$ 与二项期望

**陈述。**第 21 节与本章其他内容似乎没有关系。拉马努金在 Entry 21 中写道
$$\varphi_\infty\left(\frac{nx}{1+x}\right) = (1+x)^{-n}\sum_{k=0}^{\infty} \binom{n}{k}\varphi(k)x^k, \qquad (21.1)$$
其中
$$\varphi_r(x) = \varphi_{r-1}(x) - 1 + \exp\left(\frac{nP_{r-1}\varphi_{r-1}'(x)}{r!}\right),$$
$\varphi_1(x) = \varphi(x)$，且
$$P_r = \sum_{k=1}^{\infty} (-1)^{k+1}k^r x^k.$$
Berndt 明言：无法辨明这一结果的含义，因为递推定义的函数 $\varphi_r(x)$ 与 (21.1) 没有任何联系。(21.1) 被当作 $\varphi_\infty$ 的定义。置 $u = nx/(1+x)$、$p = u/n$，则 (21.1) 变成
$$\varphi_\infty(u) = \sum_{k=0}^{\infty} \binom{n}{k}\varphi(k)p^k(1-p)^{n-k}. \qquad (21.2)$$

**推论。**设 $u$、$n$ 固定，$0 \le u \le n$，$n$ 为整数；设 $\varphi(z)$ 在以 $u$ 为中心、包含线段 $[0, n]$ 的圆盘内解析。若 $\varphi_\infty(u)$ 由 (21.2) 定义，则
$$\varphi_\infty(u) = \sum_{j=0}^{\infty} \frac{\varphi^{(j)}(u)}{j!}\sum_{k=0}^{\infty} \binom{n}{k}(k-u)^j p^k(1-p)^{n-k}. \qquad (21.3)$$
证明：把 $\varphi(z)$ 在 $u$ 处作 Taylor 展开，交换求和次序即得。

注记：$\varphi_\infty(u)$ 是 $\varphi(u)$ 的期望值，其中 $u$ 为二项分布 $b(n, k; p)$ 的随机变量。拉马努金暗指 Ch. 3 的 Entry 10，那里他给出了 $\varphi(u)$ 的期望值用 $\varphi^{(j)}(u)$（$0 \le j < \infty$）表示的公式，其中 $u$ 为 Poisson 随机变量；但后一结果比现在的推论深刻得多。推论即使在 $n$ 为任意正数时也成立，只要 $p < 1/2$ 且 $\varphi$ 为多项式；求 (21.3) 成立的更一般条件会很有趣。

**出处。**Berndt Part I, Ch. 7, Entry 21, pp. 173–174。

**状态。**(21.1)–(21.3) 已证明（作为 $\varphi_\infty$ 的定义与推论）；递推定义的 $\varphi_r(x)$ 与 (21.1) 的联系未明（Berndt 原话，见该条）。本轮未对 (21.1)–(21.3) 作数值复核（涉及任意解析函数 $\varphi$，无具体数值例），列入待核对清单。

**对照。**二项期望与 Poisson 期望见 M13（Ch. 3 Entry 10）；Taylor 展开与矩见 M12、M13。

## Entry 22——$\sum 1/(k^n(k+1)^n)$

**陈述。**设 $A_1 = 0$。对每个非负整数 $r$（$r \ne 1$），设 $A_r = \{1+(-1)^r\}\zeta(r)$。若 $n$ 为自然数，则
$$\sum_{k=1}^{\infty} \frac{1}{k^n(k+1)^n} = \sum_{k=0}^{n} A_{n-k}\binom{-n}{k}.$$
Entry 22 的证明见 Glaisher、Kesava Menon、Djoković。Entry 22 与 Ch. 9 的 Entry 35 完全相同。

**例。**$\sum_{k=1}^{\infty} 1/(k^3(k+1)^3) = 10 - \pi^2$（Entry 22 在 $n = 3$ 的特例）。

**出处。**Berndt Part I, Ch. 7, Entry 22, pp. 174–175。

**状态。**已证明。数值复核：$n = 2$ 时两边均为 $\pi^2/3 - 3$（差 $1.5\times 10^{-31}$）；例 $n = 3$ 时两边均为 $10 - \pi^2$（差 $4.4\times 10^{-31}$）。

**对照。**$\zeta$ 在正整数处的值见 M01；二项式系数 $\binom{-n}{k}$ 见 M13；部分分式与望远镜求和见 M02。

## Entry 23——Stirling 展开

**陈述。**设 $|\arg z| < \pi$。则当 $|z| \to \infty$ 时，
$$\mathrm{Log}\,\Gamma(z+1) \sim (z+\tfrac12)\mathrm{Log}\, z - z + \tfrac12\mathrm{Log}(2\pi) + \sum_{k=1}^{\infty} \frac{B_{2k}}{2k(2k-1)z^{2k-1}}.$$
这是 Stirling 著名的 $\mathrm{Log}\,\Gamma(z+1)$ 渐近展开（Whittaker–Watson，p. 252）。

拉马努金指出 $\frac12\mathrm{Log}(2\pi) = 0.9189385332046723$，这是正确的（Abramowitz–Stegun，p. 3）。

**推论。**当 $x$ 很大时，$e^x\Gamma(x+1)/x^x = \sqrt{2\pi x + \pi/3}$（近似成立）。此推论按笔记（p. 88）原样引用；这一 Gamma 函数近似使人想起第 4 节的推论 6–8。证明：由 $\Gamma(x)$ 的熟知渐近展开 (I6)，当 $x \to \infty$ 时，
$$\frac{e^x\Gamma(x+1)}{x^x} \sim \sqrt{2\pi x}\left(1 + \frac{1}{12x} + \frac{1}{288x^2} + \cdots\right). \qquad (23.1)$$
但另一方面，
$$\sqrt{2\pi x + \frac{\pi}{3}} = \sqrt{2\pi x}\sqrt{1 + \frac{1}{6x}} = \sqrt{2\pi x}\left(1 + \frac{1}{12x} - \frac{1}{288x^2} + \cdots\right). \qquad (23.2)$$
故拉马努金的近似是合理的，但注意 (23.1) 与 (23.2) 中 $x^{-2}$ 的系数符号相反。

**出处。**Berndt Part I, Ch. 7, Entry 23, p. 175。

**状态。**已证明。数值复核：$z = 10$ 时 $\mathrm{Log}\,\Gamma(11) = 15.1044125731\cdots$，Stirling 展开前三项给出 $15.1044125652\cdots$（差 $7.9\times 10^{-9}$）；$\frac12\mathrm{Log}(2\pi) = 0.9189385332046723\cdots$（差 $4.4\times 10^{-16}$）。

**对照。**Stirling 公式见 M10、M12；$\mathrm{Log}(2\pi)$ 的数值见 M10。

## Entry 24——第 4 节推论 3、推论 2 的重述

**陈述。**Entry 24 及其推论分别是第 4 节的推论 3（$\Gamma(z)\Gamma(1-z) = \pi/\sin\pi z$）与推论 2（$\Gamma(1/2) = \sqrt{\pi}$）的重述。

**出处。**Berndt Part I, Ch. 7, Entry 24, p. 175。

**状态。**已证明（见 Entry 4 推论 2、推论 3）。

**对照。**见 Entry 4；反射公式见 M10。

## Entry 25——Gauss 乘法定理

**陈述。**对每个复数 $z$ 与正整数 $n$，
$$\prod_{k=1}^{n} \Gamma\left(\frac{z+k}{n}\right) = (2\pi)^{(n-1)/2}n^{-z-1/2}\Gamma(z+1).$$
这是 Gauss 著名的 Gamma 函数乘法定理的版本（Whittaker–Watson，p. 240）。

**推论 1。**Entry 25 在 $z = 0$ 的特例。

**推论 2。**$\Gamma(\frac23) = \sqrt{\Gamma(\frac56)}\,\sqrt[3]{2}\,\sqrt[4]{\pi/3}$。证明：在 Entry 25 中取 $n = 2$、$z = -1/3$，得 $\Gamma(\frac13)\Gamma(\frac56) = \sqrt{\pi}\,2^{1/3}\Gamma(\frac23)$；由第 4 节推论 3，$\Gamma(\frac23)\Gamma(\frac13) = 2\pi/\sqrt{3}$；联立即得。

**推论 3。**对每个复数 $z$，
$$\Gamma(z+1) = \Gamma\left(\frac{z+1}{2}\right)\Gamma\left(\frac{z}{2}+1\right)2^z\pi^{-1/2}.$$
这是 Legendre 倍元公式，是 Gauss 乘法公式在 $n = 2$ 的特例。

**推论 4。**设 $|\arg z| < \pi$。则当 $|z| \to \infty$ 时，
$$\mathrm{Log}\,\Gamma(z+\tfrac12) \sim z\,\mathrm{Log}\, z - z + \tfrac12\mathrm{Log}(2\pi) + \sum_{k=1}^{\infty} \frac{B_{2k}(2^{1-2k}-1)}{2k(2k-1)z^{2k-1}}.$$
证明：在推论 3 中把 $z$ 换成 $2z$，得 $\Gamma(z+\tfrac12) = \sqrt{\pi}\,\Gamma(2z+1)/(2^{2z}\Gamma(z+1))$；两边取对数并用 Entry 23。拉马努金不慎把上面的无穷级数乘了 $-1$。

**出处。**Berndt Part I, Ch. 7, Entry 25, pp. 175–176。

**状态。**已证明（推论 4 的级数符号已按 Berndt 纠正）。数值复核：Entry 25 在 $n = 2$、$z = 1/2$ 时两边均为 $1.11072073454\cdots$（差 $2.0\times 10^{-31}$）；推论 2 两边均为 $1.35411793943\cdots$（差 $2.0\times 10^{-31}$）；推论 3 在 $z = 1/3$ 时两边差 $0$；推论 4 在 $z = 10$ 时前三项差 $7.6\times 10^{-9}$。

**对照。**Gauss 乘法定理与 Legendre 倍元公式见 M10；$\Gamma(2/3)$、$\Gamma(5/6)$ 的值见 M10；$\mathrm{Log}\,\Gamma(z+1/2)$ 的渐近见 M12。

## Entry 26——$\mathrm{Log}\,\Gamma(z+1)$ 的 Maclaurin 级数

**陈述。**对 $|z| < 1$，
$$\mathrm{Log}\,\Gamma(z+1) = -\gamma z + \sum_{k=2}^{\infty} \frac{\zeta(k)(-z)^k}{k},$$
其中 $\gamma$ 为 Euler 常数。这是熟知的 Maclaurin 级数（Abramowitz–Stegun，p. 256）。

**推论。**对 $|z| < 1$，
$$\begin{aligned}
\mathrm{Log}\{\tfrac12\Gamma(z+3)\} &= 0.9227843351z + 0.1974670334z^2\\
&\quad - 0.0256856344z^3 + 0.0049558084z^4\\
&\quad - 0.0011355510z^5 + 0.0002863437z^6\\
&\quad - 0.0000766825z^7 + 0.0000213883z^8\\
&\quad - 0.0000061409z^9 + 0.0000018013z^{10} + \cdots \qquad (26.1)
\end{aligned}$$
证明：用 Entry 26，$\mathrm{Log}\{\frac12\Gamma(z+3)\} = \mathrm{Log}(\frac12 z+1) + \mathrm{Log}(z+1) + \mathrm{Log}\,\Gamma(z+1)$，展开即得 $z^k$（$1 \le k \le 10$）的数值系数（$\zeta(k)$（$2 \le k \le 10$）的值见 Abramowitz–Stegun，p. 811，或 Dwight，p. 224）。在拉马努金的 (26.1) 表述中，他把第 10 项及以后各项替换为单个表达式 $0.0000054047z^{10}/(3+z)$。

**例 1。**$\mathrm{Log}\,\Gamma(\frac23) = 0.3031502752$。

**例 2。**$\mathrm{Log}\,\Gamma(\frac56) = 0.1211436313$。

**例 3。**$\mathrm{Log}\,\Gamma(\frac{9}{10}) = 0.0663762397$。

上述计算由 Fransén–Wrigge 表中的 $\Gamma(2/3)$、$\Gamma(5/6)$、$\Gamma(9/10)$ 值确定。拉马努金莫名其妙地给出 $\mathrm{Log}\,\Gamma(\frac23) = 0.5341990853$。

**出处。**Berndt Part I, Ch. 7, Entry 26, pp. 176–177。

**状态。**已证明（(26.1) 第 10 项起的替换与例 1 的 0.5341990853 已按 Berndt 指出为误）。数值复核：Entry 26 在 $z = 1/2$ 时两边差 $3.7\times 10^{-32}$；(26.1) 的系数 $c_1 = \psi(3) = 0.9227843351$、$c_2 = \psi'(3)/2 = 0.1974670334$、$c_3 = \psi''(3)/6 = -0.0256856344$（与书中一致，30 位）；例 1–3：$\mathrm{Log}\,\Gamma(2/3) = 0.30315027515\cdots$、$\mathrm{Log}\,\Gamma(5/6) = 0.12114363133\cdots$、$\mathrm{Log}\,\Gamma(9/10) = 0.06637623974\cdots$（与书中一致；拉马努金的 $0.5341990853$ 与真值相差 $0.231$）。

**对照。**$\mathrm{Log}\,\Gamma$ 的级数展开见 M10；Euler 常数与 $\zeta(k)$ 见 M01；digamma 函数 $\psi$ 见 M10。

## Entry 27(i)(ii)(iii)——无穷乘积 $\prod (1+z^2/(n+k)^2)$ 的三个公式

**陈述。**设 $n$ 为自然数，$|z| > n$。

**Entry 27(i)。**
$$2\pi z\prod_{k=1}^{\infty} \left(1 + \frac{z^2}{(n+k)^2}\right) = 2\left(\frac{n!}{z^n}\right)^2\sinh(\pi z)\exp\left(\sum_{k=1}^{\infty} \frac{(-1)^k\varphi_{2k}(n)}{kz^{2k}}\right). \qquad (27.1)$$
证明：用 Euler 的 Gamma 函数定义（Whittaker–Watson，p. 237；亦为 Ch. 6 第 4 节例 2），$\Gamma^2(n+1)/(\Gamma(n+1+iz)\Gamma(n+1-iz)) = \prod_{k=1}^{\infty} (1+z^2/(n+k)^2)$（(27.2)）；另一方面，$2\pi z\Gamma^2(n+1)/(\Gamma(n+1+iz)\Gamma(n+1-iz)) = 2\pi z/(z^{2n}(1+1^2/z^2)\cdots(1+n^2/z^2)\Gamma(1+iz)\Gamma(1-iz))$（(27.3)）；对 $\mathrm{Log}(1+k^2/z^2)$ 用 Maclaurin 级数得 (27.4)；用第 4 节推论 3 得 $2\pi z/(\Gamma(1+iz)\Gamma(1-iz)) = 2\sinh(\pi z)$（(27.5)）；代入即得 (27.1)。

在拉马努金的 Entry 27(i)(ii) 表述（pp. 89、90）中，$2\sinh(\pi x)$ 的位置出现的是 $e^{\pi x} - e^{-\pi x}\theta$，其中 $e^{-\pi x}\theta$ 已被划去。在一个同样被划去的脚注中，拉马努金说「$0 = \cos 2\pi n$ 精确成立或几乎成立，视 $2n$ 是否为整数而定」。Entry 27(i) 的一个两行解法也被划去了。

**Entry 27(ii)。**在与 Entry 27(i) 同样的假设下，
$$2\pi(z^2+n^2)^{n+1/2}\prod_{k=1}^{\infty} \left(1 + \frac{z^2}{(n+k)^2}\right) = 2(n!)^2\sinh(\pi z)\exp\left(2n - 2z\tan^{-1}\left(\frac{n}{z}\right) + \sum_{j=1}^{\infty} \frac{(-1)^j B_{2j}S_{2j}}{jz^{2j-1}}\right), \qquad (27.6)$$
其中
$$S_{2j} = \sum_{k=0}^{\infty} \frac{(-1)^k(2k+2j-1)!}{(2j-1)!(2k+1)!}\left(\frac{n}{z}\right)^{2k+1}, \qquad j \ge 1.$$
证明：用 (27.1) 乘以 $(z^2+n^2)^{n+1/2}/z$，并用 $(z^2+n^2)^{n+1/2}/z = z^{2n}e^{(n+1/2)\mathrm{Log}(1+n^2/z^2)}$（(27.7)）与 Entry 1（$\zeta(-2k) = 0$）展开 (27.9)(27.10)，交换求和次序即得。

**Entry 27(iii)。**设 $n$ 为正整数，$x > 0$。写 $r^2 = n^2+x^2$（$r > 0$），$\beta = \tan^{-1}(x/n)$。则当 $x \to \infty$ 时，
$$\mathrm{Log}\left\{2\pi(x^2+n^2)^{n-1/2}\prod_{k=0}^{\infty} \left(1 + \frac{x^2}{(n+k)^2}\right)\right\} \sim 2\,\mathrm{Log}\,\Gamma(n) + 2n + 2x\beta - \sum_{k=1}^{\infty} \frac{B_{2k}\cos\{(2k-1)\beta\}}{k(2k-1)r^{2k-1}}.$$
证明：用 (27.2) 与 Entry 23（Stirling 展开），$n + ix = re^{i\beta}$，即得。Berndt 感谢 J. W. Wrench, Jr. 提供了若干参考文献。

**出处。**Berndt Part I, Ch. 7, Entry 27, pp. 177–180。

**状态。**已证明（拉马努金原稿中被划去的 $e^{-\pi x}\theta$、脚注与两行解法已按 Berndt 的说明记录）。数值复核：Entry 27(i) 在 $n = 1$、$z = 2$ 时两边差 $2.5\times 10^{-29}$（左端无穷乘积按 Gamma 函数比值求值；指数中的级数 $\sum_{k\ge1} (-1)^k/(k\cdot 2^{2k}) = -\mathrm{Log}(5/4)$）；Entry 27(iii) 在 $n = 1$、$x = 20$ 时左端 $62.83310151\cdots$，右端首项 $62.83330943\cdots$（差 $2.1\times 10^{-4}$，为下一渐近项量级；注意左端乘积从 $k = 0$ 起，含因子 $1 + x^2/n^2$）。

**对照。**无穷乘积与 $\sinh$ 见 M02、M10；Stirling 展开见 M12；$\varphi_{2k}(n)$ 见 M01、M13。

## 小结

- 本章 27 条 Entry 全部收录完毕（Entry 1–27，编号均在原文明确出现；**没有缺号的 Entry**）。前半（Entry 1–4）是幂和理论的基础：$\varphi_r(x)$ 的渐近展开 (1.2) 与常数 $\zeta(-r)$（Entry 1）、$\eta(-r)$ 与 $\varphi_r$ 向复 $x$ 的推广（Entry 2）、等差幂和（Entry 3）、$\zeta$ 函数方程的伪装形式 (4.1)(4.2) 及其推论 1–8（Entry 4，本章中心）。中段（Entry 5–14）是幂和的展开与计算：交错等差幂和（Entry 5）、$(x^2+x)^n$ 的 $\varphi$ 展开与 $\varphi_1,\dots,\varphi_{11}$ 显式公式（Entry 6）、反射恒等式与整除性（Entry 7）、Bernoulli 展开 (8.1)（Entry 8）、(2.3) 的重述（Entry 9）、乘法公式（Entry 10）、$\varphi_{-r}$ 与 $\cot$ 导数及导数表（Entry 11）、$2^r$ 恒等式与四个 $\sum 1/(ak+1)^3$ 例（Entry 12）、Stieltjes 常数与 $\zeta(s)$ 的 Laurent 展开及数值例（Entry 13）、$\sum 1/(k(k^n-1))$ 的渐近与 $a_0$、$a_1$、$a_{k+1}$（Entry 14）。后半（Entry 15–27）是 Hurwitz 公式与 Gamma 函数的应用：正弦/余弦级数（Entry 15、16）、$E_r^*$ 与 Dirichlet beta 函数（Entry 17、18）、奇 $q$ 的分点公式（Entry 19、20）、$\varphi_\infty$ 与二项期望（Entry 21）、$\sum 1/(k^n(k+1)^n)$（Entry 22）、Stirling 展开（Entry 23）、第 4 节推论的重述（Entry 24）、Gauss 乘法定理（Entry 25）、$\mathrm{Log}\,\Gamma$ 的 Maclaurin 级数（Entry 26）、无穷乘积的三个公式（Entry 27）。
- 本章发现的拉马努金原文疏失（均已在各条注明）：Entry 4 推论 6–8 的 (4.4)(4.6)(4.8) 与正确渐近式不相容；Entry 5 笔记误印 $b^r$ 应为 $(2b)^r$；Entry 11 的求导次数（应为 $-r-1$ 而非 $r$）与 cot 表末项分母 2385 应为 2835；Entry 11 例 (vi)(vii) 右端错误；Entry 12 的 (12.2)(12.3) 右端符号错误；Entry 13 例 1 的 $+0.0001n^4$ 应为 $-0.0001n^4$ 与多处数值末位错误（$\zeta(11/10)$、$\zeta(3/2)$、$\zeta(5/2)$、$B_{3/2}^*$、$B_{1/3}^*$、$B_{-1/3}^*$）；Entry 14 推论 2 的 $s^3$、$s^4$ 系数小误差（0.001617/0.000085 应为 0.001615/0.000086）；Entry 19(ii) 拉马努金版不正确；Entry 25 推论 4 的无穷级数符号错误；Entry 26 的 (26.1) 第 10 项起替换与 $\mathrm{Log}\,\Gamma(2/3) = 0.5341990853$（真值 $0.3031502752$）；Entry 27(i)(ii) 的 $e^{\pi x} - e^{-\pi x}\theta$（已划去）与被划去的脚注、两行解法。
- 本轮发现的原书印文问题（均经数值复核证实，详见各条注记）：(a) Entry 6 推论 2(i) 左端分母印作 $9$，应为 $2$（$n = 1$、$2$ 数值复核与证明过程双重确认）；(b) Entry 8 的 (8.1) 后一等式印文不成立，系数 $-2$ 应为 $-2/(r+1)$（$r = 2$、$3$ 数值复核）；(c) Entry 14 的 $a_3$ 印值 $-0.000000475$ 与书中系数公式及证明推导矛盾（公式与直接渐近均给出 $-2.85\times 10^{-6}$；拉马努金的原值 $-0.0000028$ 实为正确，Berndt 称其不正确的判断值得怀疑）；(d) Entry 19(ii) 右端第一项印作 $\varphi_{-r}(j/p-1)$，应为 $\varphi_{-r}(j/q-1)$（$p = 1$、$q = 3$、$r = 3/2$ 数值复核：印文差 $1.66$，订正后差 $3.9\times 10^{-31}$）。
- 本轮 OCR 误读纠正：本章 DjVu OCR 的公式部分损坏严重，全部公式均按 PDF 原图（150 DPI，书 pp. 150–181）逐字转录；其中较关键的纠正有：Entry 1 的 (1.2) 与 (1.8)、Entry 4 的 (4.1)(4.2) 与推论 6–8 的渐近式、Entry 6 推论 1 的 $\varphi_4,\dots,\varphi_{11}$ 系数、Entry 11 的 cot 导数表、Entry 13 的 (13.1)–(13.3)、Entry 14 的 (14.1)(14.2) 与 $a_{k+1}$ 公式、Entry 25 推论 2 的 $\Gamma(2/3)$（150 DPI 图上易误读为 $\Gamma(4/3)$，已用 300 DPI 放大图与证明过程双重确认；按 $\Gamma(4/3)$ 理解则公式不成立，见数值复核）、Entry 26 的 (26.1) 系数、Entry 27 的 (27.1)(27.6) 与推论 2 的 $j/q$。另有两处初判「失败」实为检验设定问题：Entry 4 推论 4 的右端直接截断求和收敛极慢（改用 $(1-2^{-3/2})\zeta(3/2)$ 闭式后通过）；Entry 15、16 的右端级数收敛极慢（改用 Dirichlet beta 函数与 $\eta(1/2)$ 的闭式后通过）；Entry 5、Entry 15–20 的 $\varphi_r$ 在分数 $x$ 处的值须用 Hurwitz zeta 的正确形式 $\varphi_r(x) = \zeta(-r) - \zeta(-r, x+1)$（初版误用 $x+2$，$\varphi_r(0) = 0$ 的检验抓出）。
- 数值复核小计：本轮共复核约 50 项（mpmath 30 位 + 精确分数 + $m = 10^7$ 直接求和），全部通过，见各条「数值复核」：Entry 1 的 (1.2)(1.6)、Entry 2 的推论、Entry 4 的推论 1/4/5/6/7/8、Entry 5 的 (5.1)、Entry 6(i) 与推论 1/2、Entry 7 及其推论、Entry 8 的 (8.1) 第一等式、Entry 10 的 (10.1)、Entry 11 的 (11.1) 与 cot 表、Entry 12 的例 1–4、Entry 13 的 $A_0$–$A_3$ 与例 2–7 的数值、Entry 14 的 $a_0$、$a_1$、$a_2$、(14.1) 的渐近检验与推论 2 的 $C$、Entry 15、Entry 16 及其推论 16(i)、Entry 17 及其推论、Entry 18 及其推论、Entry 19(i)、Entry 20、Entry 22 及其例、Entry 23 的 Stirling 展开与 $\frac12\mathrm{Log}(2\pi)$、Entry 25 及其推论 2/3/4、Entry 26 及其推论系数与例 1–3、Entry 27(i)(iii)。
- 与 M 模块的对照：幂和与 Euler–Maclaurin 公式主线见 M12（Entry 1、Entry 4 推论 6–8、Entry 14、Entry 23、Entry 25 推论 4、Entry 27(iii)）；Bernoulli 数、$\zeta$ 函数、Stieltjes 常数与 Dirichlet beta 函数见 M01（Entry 1、2、4、8、10–14、17、18、22）；Gamma 函数（反射公式、倍元公式、乘法定理、Stirling 展开、$\mathrm{Log}\,\Gamma$ 级数）见 M10（Entry 4 推论 2–3、Entry 23–27）；无穷级数与交错级数见 M02（Entry 2、5、11、15–20）；二项式恒等式与期望见 M13（Entry 6、21、22）；$q$ 级数背景见 M07（Entry 15–17 的 Hurwitz 公式与 $L(s)$）；注意 M01 伯努利数定义缺口仍待补，出处见 Ch. 5 Entry 9。

## 待核对清单

1. 本章 Entry 1–27 齐全，无缺号；Berndt 未在章首给出本章公式或定理陈述的总数（Ch. 5 章首有「94 条」的计数，本章无对应计数）；IMSC 整理表计本章的结果数本次未能读取（imsc.res.in 当日不可达），待该表可达后补。
2. Entry 6 推论 2(i) 左端分母：原书印作 $9$，本轮按数值复核（$n = 1$、$2$）与证明过程（Entry 3，$a = (\sqrt{5}-1)/2$、$b = 1$）订正为 $2$；待查他版或勘误表确认。
3. Entry 8 的 (8.1) 后一等式：原书印文系数 $-2$ 经数值复核不成立，订正为 $-2/(r+1)$；待查他版或勘误表确认。
4. Entry 14 的 $a_3$：原书印值 $-0.000000475$ 与书中系数公式 $a_{k+1} = -B_{2k}A_{2k-1}/(2k)$、证明推导（(14.8) 的系数 $B_{j+1}c_j/(j+1)!$）及直接数值渐近（$D(n) \approx -2.87\times 10^{-6}$）均矛盾；拉马努金原值 $-0.0000028$ 与公式值一致；究竟是系数公式漏印阶乘（分母应为 $(2k)!$），还是 $a_3$ 印值有误，待查他版或勘误表后定。
5. Entry 19(ii) 右端第一项：原书印作 $\varphi_{-r}(j/p-1)$，本轮按数值复核（$p = 1$、$q = 3$、$r = 3/2$）与证明所用的 (16.2) 订正为 $\varphi_{-r}(j/q-1)$；待查他版或勘误表确认。
6. Entry 21 的 (21.1)–(21.3)：本轮未作数值复核（涉及任意解析函数 $\varphi$，无具体数值例）；递推定义的 $\varphi_r(x)$ 与 (21.1) 的联系未明（Berndt 原话）；待补具体特例的数值检验。
7. Entry 25 推论 2 的 $\Gamma(2/3)$：150 DPI 图上易误读为 $\Gamma(4/3)$，已用 300 DPI 放大图与证明过程双重确认为 $\Gamma(2/3)$；按 $\Gamma(4/3)$ 理解则公式不成立。
8. Entry 4 推论 4 的拉马努金证明：Berndt 只说明其「本质上有误」，未逐项指出哪一步重排不合法；本文件只记录等式成立与证明有误，未作推测。
9. Entry 11 的 cot 导数表：$k = 0,\dots,9$ 十行已逐项数值复核 $k = 1$、$2$ 两行（$x = 0.3$），其余八行未逐项数值复核，待补。
10. 本章 TIFR 影印版（第二本笔记第 7 章）的具体页码未标：Berndt 原书未逐条给出 TIFR 页码，待查 TIFR 1957 年版目录后补；第一本笔记的相关内容亦未对照。

## 来源说明

- 底本：Bruce C. Berndt, *Ramanujan's Notebooks*, Part I, Springer, 1985, Ch. 7, pp. 150–181。archive.org 全文（`ramanujan_notebooks_i`）：DjVu OCR 文本（563,342 字节）与 PDF（13,201,802 字节，368 叶；**PDF 页 = 书页 + 10**，如书 p. 150 = PDF p. 160）。
- 核对方法：本章 32 页（书 pp. 150–181）均渲染成 150 DPI 图片逐字读过（Entry 6 推论 2(i) 的分母、Entry 8 的 (8.1)、Entry 14 的 $a_{k+1}$ 公式、Entry 19(ii) 的 $j/p$、Entry 25 推论 2 的 $\Gamma(2/3)$ 另用 300 DPI 放大图确认）；DjVu OCR 的公式部分损坏严重，全部公式均按 PDF 原图转录，OCR 凡与图片或数值不符者一律纠正并注明；数值复核用 Python + mpmath（30 位）与精确分数（Fraction），本章共复核约 50 项，见各条「数值复核」；$a_0$ 另用 numpy 直接求和至 $m = 10^7$ 加尾项修正核实。
- IMSC 整理表计本章的结果数本次未能读取（imsc.res.in 当日不可达），待补；该数为 IMSC 表的计数，Berndt 原书未逐章公布条目数，本章章首亦无计数。
- 本文件只收公式陈述与自写导读/证明思路，不照抄 Berndt 的正文与证明。
