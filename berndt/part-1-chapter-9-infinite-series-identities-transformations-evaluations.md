# Part I · 第 9 章 Infinite Series Identities, Transformations, and Evaluations（无穷级数恒等式、变换与求值）

出处：Bruce C. Berndt, *Ramanujan's Notebooks*, Part I, Springer, 1985, 第 9 章，pp. 232–294（第 8 章 pp. 181–231；本书 Part I 的最后一章，其后为 Quarterly Reports，起自 p. 295）。对应拉马努金**第二本笔记第 9 章**。

## 背景与记号

- 本章主题：无穷级数的恒等式、变换与求值。Berndt 在章首导言（pp. 232–233）说明：本章共 **35 节、139 条公式**，多为优美精致的结果；拉马努金给出若干幂级数变换，由此得到许多引人注目的级数关系与求值；他最初在这方面的努力多与多对数（dilogarithm）及相关函数有关，这些结果多非新，可追溯到 Euler、Landen、Abel 等人；但其余关于幂级数变换的结果多数似乎是新的。Hardy 在拉马努金文集导言中的判语见导言引用：「正是他对代数公式、无穷级数变换等的洞察力最令人惊叹。」
- 章首最著名的公式是 Apéry 证明 $\zeta(3)$ 无理数所用的公式
  $$\zeta(3) = \frac52\sum_{k=1}^{\infty}(-1)^{k+1}\frac{(k!)^2}{(2k)!\,k^3}, \tag{0.1}$$
  拉马努金显然错过了这一公式，但本章含有若干同类型的公式，其中一些涉及 $\zeta(3)$ 与 Catalan 常数 $G$（见 Entry 16、Entry 17、Entry 32）。
- **与第 8 章的衔接（澄清 Ch. 8 待核对清单第 8 项）**：第 8 章研究 $\mathrm{Log}\,\Gamma(x+1)$ 的若干类比；本章第 27–30 节回到这一主题（p. 273 原文：「第 27–30 节与本章其余部分主题完全不同」）。这里的推广是 $\varphi_r(x) = \sum_{k=1}^{x} k^r\mathrm{Log}\,k$（(27.1)，$r > -1$），第 8 章研究的是 $r \le -1$ 与 $r = -1/2$ 的情形（第 8 章第 21、24 节）；(28.3) 给出 $\varphi_r(x) = \zeta'(-r, x+1) - \zeta'(-r)$ 的解析延拓，与 Bendersky、Büsing 的 $\Gamma$ 推广相关。见 Entry 27(a)–Entry 30。
- 本章多数公式只对实数 $x$ 陈述（Berndt 注：拉马努金显然只打算让结果对实 $x$ 成立；许多公式可经解析延拓推广到复 $x$，仅在不如此就会得到空洞定理的少数情形作了例外）。
- **记号**（$\mathrm{Log}$ 为自然对数；$\gamma = 0.577215664901533\ldots$ 为 Euler 常数）：
  - 多对数 $\mathrm{Li}_n(z) = \sum_{k=1}^{\infty} z^k/k^n$（(6.1)）；$2\chi_n(z) = \mathrm{Li}_n(z) - \mathrm{Li}_n(-z)$（(6.2)），故 $\chi_n(1) = \sum_{k\ \mathrm{odd}} 1/k^n$，$\chi_2(1) = G$（Catalan 常数）、$\chi_3(1) = \frac78\zeta(3)$；
  - 调和数 $H_n = \sum_{k=1}^{n} 1/k$；$h_n = \sum_{k=1}^{n} 1/(2k-1)$（(8.2)）；
  - $g(z) = \sum_{k=1}^{\infty} H_k z^{k+1}/(k+1)^2$（(9.1)）；$h(z) = \sum_{k=1}^{\infty} H_k z^{k+1}/(k+1)^3$；
  - Clausen 函数 $\mathrm{Cl}_{2n}(x)$、$\mathrm{Cl}_{2n+1}(x)$（(13.1)(13.2)），$\mathrm{Cl}_1(x) = -\mathrm{Log}|2\sin(x/2)|$（(13.3)）；$D_{2n}(x)$、$D_{2n+1}(x)$（(14.1)(14.2)），$D_1(x) = -\frac12\mathrm{Log}|\tan(x/2)|$（(14.3)）；
  - $f_n(x) = \int x^n\cot x\,dx$（第 15 节）；Catalan 常数 $G = 0.915965594177219\ldots$（(16.3)）；
  - $\varphi_r(x) = \sum_{k=1}^{x} k^r\mathrm{Log}\,k$（(27.1)）；常数 $C_r = -\zeta'(-r)$（(27.7)），$C_0 = \frac12\mathrm{Log}(2\pi)$、$C_2 = \zeta(3)/(4\pi^2)$、$C_4 = -3\zeta(5)/(4\pi^4)$、$C_6 = 45\zeta(7)/(8\pi^6)$；
  - $\psi(x) = \sum_{k=0}^{\infty} \binom{2k}{k}\sin^{2k+1}(\pi x)/(2^{2k}(2k+1)^2)$（(31.1)）；
  - $K_r = \sum_{k=1}^{\infty} 1/(k^r(k+1)^r)$（第 35 节）；$A_n = (1+\cos\pi n)\zeta(n)$（第 35 节前定义，$A_1 = 0$、$A_0 = -1$）；
  - $B_n$ 为 Bernoulli 数（当代定义，见 Ch. 5 Entry 9 与导言 (I1)；M01 伯努利数定义缺口仍待补，见文末）；$B_n(x)$ 为 Bernoulli 多项式；$\zeta(s,x)$ 为 Hurwitz zeta 函数。
- 本章在原文中明确出现编号的 Entry 共 **35 条**：Entry 1–35，**无缺号**；另有分体 Entry 27(a)/27(b)、Entry 28(a)/28(b)、Entry 31(a)/31(b)，共 38 个 Entry 标题。Berndt 章首计数本章共 139 条公式或定理陈述；IMSC 整理表计本章的结果数本次未能读取（imsc.res.in 当日不可达），待补。
- **本章的拉马努金原文疏失**（Berndt 已指出，详见各条与末尾小结）：Entry 3 不成立（n 充分大时）；公式 (11.3) 不成立；Entry 31(b)(iv) 拉马努金版错误；Entry 10(i)(ii) 笔记本右端须乘 $(-1)$；Entry 8 例 (ii)(iii) 笔记本有误；Entry 7 例 (ii) 笔记本漏系数 $4/5$；Entry 9(iii) 笔记本误印 $\mathrm{Log}(1-z)$ 应为 $\mathrm{Log}(z-1)$；Entry 14 (14.4) 右端笔记本写 $\mathrm{Li}_{n+1}(1)$ 应为 $\chi_{n+1}(1)$；Entry 20 (20.1) 笔记本漏 $-\zeta(3)/4$ 一项；Entry 21 (21.2) 笔记本右端错乘 $1/4$；Entry 27 例 (i) 拉马努金所给不正确；Entry 31(b) 例 (ii) 拉马努金版读 $2\psi(1/4)$ 应为 $\psi(1/4)$；Entry 32 推论 (i) 拉马努金版左端第三项有小误印。
- **本轮发现的原书印文问题**（数值证实，详见末尾小结）：Entry 12 例 (ii) 的 $H_k$ 应为 $H_{2k-1}$（印文版与右端差 0.103，证明版差 $7.2\times 10^{-7}$）；Entry 28(b) 的公式 (28.8) 两行互不一致且均与 (28.3) 的 $\varphi_r(x)$ 不符（订正形式已在 $r = 1$–$4$ 七点 40 位复核通过），(28.13) 的 Bernoulli 和上限 $(r+1)/2$ 应为 $r/2$。

## 本章结构

| Entry | 页 | 内容 |
|---|---|---|
| Entry 1 | 233–235 | $c_r(x)$ 的定义；$r$ 奇/偶两种情形的闭式 (i)(ii) |
| Entry 2 | 235–236 | $r \ge 2$ 时 $c_r(x)$、$s_r(x)$ 的闭式 (i)(ii)；笔记本提示不完整 |
| Entry 3 | 236 | $S_n$、$C_n$、$\varphi_n$ 的定义；(3.2) 已否定 |
| Entry 4 | 236–242 | $F_n$、$G_n$ 的恒等式 (4.1)(4.2)；Proposition 4 (i)–(x) |
| Entry 5 | 246 | 二项正弦/余弦和 |
| Entry 6 | 247–249 | $\mathrm{Li}_2$ 的函数方程；例 (i)–(viii) |
| Entry 7 | 249 | $\mathrm{Li}_3$ 的例 (i)(ii) |
| Entry 8 | 249–250 | $f(x) = \sum h_k x^{2k-1}/(2k-1)$；例 (i)–(iii) |
| Entry 9 | 251–253 | $g(z)$、$h(z)$；(9.4) $\sum H_k/(k+1)^2 = \zeta(3)$ |
| Entry 10 | 253–255 | $h(z)$ 的函数方程 (i)(ii)；笔记本右端须乘 $(-1)$ |
| Entry 11 | 255–257 | $F(x)$、$G(x)$；(11.3) 不成立 |
| Entry 12 | 257–260 | $H(x)$；例 (i)–(iii)；例 (ii) 印文有误 |
| Entry 13 | 260–261 | $\int (u^n/2)\cot(u/2)\,du$；Clausen 函数 |
| Entry 14 | 261–262 | $\int (u^n/2)(1/\sin u)\,du$；$D_n$ 函数 |
| Entry 15 | 262–264 | $f_n(x) = \int x^n\cot x\,dx$；Proposition 15 (i)–(iv) |
| Entry 16 | 264–265 | 中心二项系数级数与 Catalan 常数 $G$；(16.1) |
| Entry 17 | 265–267 | (17.1)；$\int_0^{1/\sqrt3}(\tan^{-1}t)/t\,dt$ 的求值 |
| Entry 18 | 267–268 | 中心二项系数级数（$\cos$ 与 $\sin$ 之差） |
| Entry 19 | 268–269 | 中心二项系数级数（$\cos$ 与 $\sin$ 之和） |
| Entry 20 | 269–270 | (20.1)；例 (i)(ii) |
| Entry 21 | 270–271 | (21.2)；Nielsen 先证 |
| Entry 22 | 270–271 | 中心二项系数级数（Entry 20 换 $x \to \pi/2 - x$） |
| Entry 23 | 271–272 | 中心二项系数级数与 $\tan$ |
| Entry 24 | 272–273 | $\mathrm{Li}_2$ 的两变量函数方程 (i)(ii) |
| Entry 25 | 272–273 | $\mathrm{Li}_2$ 的另一两变量函数方程 (i) |
| Entry 26 | 273 | $\chi_2$ 的两变量函数方程 (i) |
| Entry 27(a) | 273–275 | $\varphi_r(x)$ 的渐近展开；常数 $C_r$ |
| Entry 27(b) | 275–278 | $C_r$ 的推论；例 (i) 拉马努金所给不正确 |
| Entry 28(a) | 278–279 | $f(r,x)$ 的递推 |
| Entry 28(b) | 279–281 | $\varphi_r(x)$ 的展开式 (28.8)；印文有误 |
| Entry 29 | 284–285 | $\varphi_r$ 的倍元公式；推论 1、2 |
| Entry 30 | 284–285 | $\varphi_r(x-1) \pm \varphi_r(-x)$ 的 Fourier 级数 |
| Entry 31(a) | 285–286 | $\psi(x)$ 与 $\varphi_1$ 的关系 |
| Entry 31(b) | 286–288 | $\psi(x)$ 的函数方程；例 (i)–(iv) |
| Entry 32 | 288–290 | 超几何 ${}_3F_2$ 恒等式 (32.1)；例 (i)(v)(vi)(vii) |
| Entry 33 | 290–293 | $\int_0^{\pi/2} x\cos^n x\sin(nx)\,dx$ 等积分 |
| Entry 34 | 293 | 二项和恒等式 |
| Entry 35 | 294 | $K_r = \sum 1/(k^r(k+1)^r)$ 的递推 (35.1)；例 (i)–(iv) |

## Entry 1——$c_r(x)$ 的闭式

**陈述。**对每个正整数 $r$，定义
$$c_r(x) = \sum_{k=0}^{\infty}\left\{\frac{\cos(2k+1-a)x}{(2k+1-a)^r} - \frac{\cos(2k+1+a)x}{(2k+1+a)^r}\right\},$$
其中 $a$ 为实数但不是奇整数，$|x| < \pi$。则 (i) $r$ 为奇正整数时，$c_r(x)$ 等于一个与 $x$ 有关的闭式；(ii) $r$ 为偶正整数时，$c_r(x)$ 由 (i) 积分得到。特别 $r = 1$ 时
$$c_1(x) = \sum_{k=0}^{\infty}\left\{\frac{1}{2k+1-a} - \frac{1}{2k+1+a}\right\},$$
与 $x$ 无关（已数值复核：$a = 1/2$、$x = 1$ 时两端精确相等）。

**出处。**Part I，Ch. 9，Entry 1（pp. 233–235）。证明用 Bromwich 书中的公式 (1.2)，再对 $x$ 积分作归纳。

**状态。**已证明（Berndt 给出完整证明）。

**对照。**M02（无穷级数：三角级数求和）、M12（渐近分析：积分归纳法）。

## Entry 2——$c_r(x)$、$s_r(x)$ 的闭式（$r \ge 2$）

**陈述。**对整数 $r \ge 2$，定义 $c_r(x)$ 如 Entry 1，另定义
$$s_r(x) = \sum_{k=0}^{\infty}\left\{\frac{\sin(2k+1-a)x}{(2k+1-a)^r} + \frac{\sin(2k+1+a)x}{(2k+1+a)^r}\right\},$$
$0 < x < \pi$。则 (i) $r$ 为偶正整数时 $c_r(x)$ 等于 $x$ 的一个多项式加 $(-1)^{r/2}\pi x^{r-1}/(r-1)!$ 型的项；(ii) $r$ 为奇正整数时 $s_r(x)$ 等于 $x$ 的幂级数加 $(-1)^{(r-1)/2}\pi x^{r-1}/(r-1)!$ 型的项。特别 $r = 1$ 时 $s_1(x) = \pi/2$（$0 < x < \pi$，已数值复核：$a = 1/2$、$x = 1$），$r = 2$ 时 (i) 由 (ii) 积分得到。

**出处。**Part I，Ch. 9，Entry 2（pp. 235–236）。拉马努金在第二本笔记 p. 104 只给出不完整的提示（「把 1 与 2 两式展成 $x$ 的升幂再用」），(i)(ii) 右端的末项在笔记本中缺失。

**状态。**已证明（Berndt 给出证明；拉马努金原提示不完整）。

**对照。**M02（三角级数）、M12。

## Entry 3——$S_n$、$C_n$、$\varphi_n$；(3.2) 已否定

**陈述。**定义
$$S_n(x) = \sum_{k=0}^{\infty}(-1)^k\frac{\sin(2k+1)x}{(2k+1)^n},\quad C_n(x) = \sum_{k=0}^{\infty}(-1)^k\frac{\cos(2k+1)x}{(2k+1)^n},\quad \varphi_n(x) = \sum_{k=0}^{\infty}(-1)^k H_{k+1}\frac{\cos(2k+1)x}{(2k+1)^n},$$
$n$ 为自然数，$x$ 为实数。拉马努金声称：若 $n$ 为不小于 3 的奇整数，则
$$\varphi_{n-2}(x) - \varphi_n(x) = xS_{n-2}(x) - xS_n(x) + nC_{n-1}(x) - nC_{n+1}(x). \tag{3.2}$$

**出处。**Part I，Ch. 9，Entry 3（p. 236）。

**状态。已否定。**Berndt 证明：$x$ 为 $\pi/2$ 的奇数倍时 (3.2) 对一切 $n$ 皆错；$x$ 不是 $\pi/2$ 的奇数倍时，(3.2) 两端当 $n \to \infty$ 的渐近 (3.3) 与 (3.4) 不相容，故 $n$ 充分大时不成立；Berndt 称无法给出修正版（若有修正版，其形状将显著不同）。数值复核：$n = 5$、$x = 1$ 时左端 $0.0467380777$、右端 $0.0417613504$，确实不等。

**对照。**M02（调和数级数）、M07（$q$-级数与三角级数）。

## Entry 4——$F_n$、$G_n$ 的恒等式；Proposition 4

**陈述。**对非负整数 $n$ 定义 $F_n(x)$、$G_n(x)$ 为二项系数正弦/余弦和（形如 $\sum (-1)^k\binom{n}{k}\sin((2k+1)x)/2^{2k}(2k+1)$ 等），并记 $S_n = (1-2^{1-n})\zeta(n)$。Entry 4(i)(ii) 给出 $F_n(x)$、$G_n(x)$ 的恒等式 (4.1)(4.2)：左端为 $S_{2j}$ 与 $\varphi$ 的组合求和，右端按 $n$ 的奇偶分别为 $\sin(\pi n/2)F_n(x)$、$\cos(\pi n/2)F_n(x)$ 型的式子（$|x| < \pi/2$；(4.1)(4.2) 的确切形式见原文，OCR 损坏严重，待核对）。证明的关键是一个奇妙定理 (4.8)（R. J. Evans 提供证明）。Proposition 4 (i)–(x) 给出十个基本正弦/余弦级数求值（$|x| < \pi/2$），例如 (i) $\sum_{k=0}^{\infty}(-1)^k\binom{2k}{k}\sin((2k+1)x)/4^k = \sin(x/2)/\sqrt{2\cos x}$（已数值复核：$x = 1$ 时精确成立）。拉马努金另定义的 $A_n$（只对 $x$ 为 $\pi$ 的正整数倍有定义）与 (4.1)(4.2) 中的连续变量 $x$ 无法调和，Berndt 不再讨论。

**出处。**Part I，Ch. 9，Entry 4（pp. 236–242）；Proposition 4 在 p. 242。拉马努金关于 $q(n)$ 的递推亦见其第二篇发表论文与本书第 10 章第 13 节。

**状态。**已证明（Berndt 用归纳法证明 (4.1)(4.2)；Proposition 4 已证明）。

**对照。**M02（三角级数）、M07（中心二项系数）、M12。

## Entry 5——二项正弦/余弦和

**陈述。**对非负整数 $n$ 与实数 $a$、$\theta$，
$$\sum_{k=0}^{n}\binom{n}{k}\sin((a+2k)\theta) = 2^n\cos^n\theta\sin((n+a)\theta),\quad \sum_{k=0}^{n}\binom{n}{k}\cos((a+2k)\theta) = 2^n\cos^n\theta\cos((n+a)\theta).$$
例 (i) $n = 2$、$a = 1$、$\theta = \pi/6$ 时左端 $= 4\cos^2\theta\sin 3\theta$（已数值复核，精确成立）。

**出处。**Part I，Ch. 9，Entry 5（p. 246）。

**状态。**已证明（初等恒等式）。

**对照。**M02、M13（组合数学：二项系数）。

## Entry 6——$\mathrm{Li}_2$ 的函数方程

**陈述。**记 $\mathrm{Li}_n(z)$、$\chi_n(z)$ 如 (6.1)(6.2)。Entry 6 给出 $\mathrm{Li}_2$ 的若干函数方程与展开，其中 (vii)(viii) 为
$$\mathrm{Li}_2(e^{-z}) = \frac{\pi^2}{6} + z\mathrm{Log}\,z - z + \sum_{n=1}^{\infty}\frac{B_n z^{n+1}}{(n+1)!\,n},\quad \mathrm{Li}_2(1-e^{-z}) = \sum_{n=0}^{\infty}\frac{B_n z^{n+1}}{(n+1)!}$$
（$z = 1$ 时已数值复核，误差 $< 10^{-6}$）。例 (i)–(vi) 为特殊值：
$$\mathrm{Li}_2(1/2) = \frac{\pi^2}{12} - \frac{(\mathrm{Log}\,2)^2}{2},\quad \mathrm{Li}_2\!\left(\frac{\sqrt5-1}{2}\right) = \frac{\pi^2}{10} - \mathrm{Log}^2\!\left(\frac{\sqrt5-1}{2}\right),\quad \mathrm{Li}_2\!\left(\frac{3-\sqrt5}{2}\right) = \frac{\pi^2}{15} - \mathrm{Log}^2\!\left(\frac{\sqrt5-1}{2}\right),$$
$$\chi_2(\sqrt2-1) = \frac{\pi^2}{16} - \frac{\mathrm{Log}^2(\sqrt2-1)}{4},\quad \chi_2\!\left(\frac{\sqrt5-1}{2}\right) = \frac{\pi^2}{12} - \frac34\mathrm{Log}^2\!\left(\frac{\sqrt5-1}{2}\right),\quad \chi_2(\sqrt5-2) = \frac{\pi^2}{24} - \frac34\mathrm{Log}^2\!\left(\frac{\sqrt5-1}{2}\right)$$
（以上六式均已数值复核，30 位精度通过）。

**出处。**Part I，Ch. 9，Entry 6（pp. 247–249）。

**状态。**已证明（多为 Euler、Landen、Abel 的经典结果；Berndt 在导言中指出本章前段结果多非新）。

**对照。**M02（多对数）、M07、M10（Gamma 函数：Bernoulli 数展开）。

## Entry 7——$\mathrm{Li}_3$ 的例 (i)(ii)

**陈述。**例 (i)：$\mathrm{Li}_3(1/2) = \frac16\mathrm{Log}^3 2 - \frac{\pi^2}{12}\mathrm{Log}\,2 + \chi_3(1)$，其中 $\chi_3(1) = \frac78\zeta(3)$；例 (ii)：$\mathrm{Li}_3\!\left(\frac{3-\sqrt5}{2}\right) = \frac23\mathrm{Log}^3\!\left(\frac{\sqrt5+1}{2}\right) - \frac{2\pi^2}{15}\mathrm{Log}\!\left(\frac{\sqrt5+1}{2}\right) + \frac45\zeta(3)$（两式均已数值复核，30 位精度通过）。

**出处。**Part I，Ch. 9，Entry 7（p. 249）。笔记本 p. 107：例 (ii) 漏系数 $4/5$。

**状态。**已证明。

**对照。**M02（多对数）、M07。

## Entry 8——$f(x) = \sum h_k x^{2k-1}/(2k-1)$

**陈述。**记 $h_k = \sum_{j=1}^{k} 1/(2j-1)$（(8.2)），定义 $f(x) = \sum_{k=1}^{\infty} h_k x^{2k-1}/(2k-1)$。例 (i) $f(1/3) = \pi^2/24 - (\mathrm{Log}\,2)^2/8$；例 (ii) $f(1/\sqrt5) = \pi^2/20$；例 (iii) $f(\sqrt5-2) = \pi^2/30 - \frac38\mathrm{Log}^2\!\left(\frac{\sqrt5-1}{2}\right)$（三式均已数值复核，30 位精度通过）。

**出处。**Part I，Ch. 9，Entry 8（pp. 249–250）。笔记本 p. 107：例 (ii) 多 $-\frac38\mathrm{Log}^2\{(\sqrt5-1)/2\}$ 一项，例 (iii) 系数 $3/4$ 应为 $3/8$。

**状态。**已证明。

**对照。**M02（调和数级数）、M07。

## Entry 9——$g(z)$、$h(z)$；(9.4)

**陈述。**记 $g(z) = \sum_{k=1}^{\infty} H_k z^{k+1}/(k+1)^2$（(9.1)）、$h(z) = \sum_{k=1}^{\infty} H_k z^{k+1}/(k+1)^3$。Entry 9 给出 $g(z)$、$h(z)$ 的函数方程，其中 (9.4) 为
$$\sum_{k=1}^{\infty}\frac{H_k}{(k+1)^2} = \zeta(3),$$
即 Euler 1775 年的结果（已数值复核：直接求和 200000 项加解析尾项，差 $2.9\times 10^{-6}$）。

**出处。**Part I，Ch. 9，Entry 9（pp. 251–253）。笔记本 p. 107：(iii) 的 $\mathrm{Log}(1-z)$ 应为 $\mathrm{Log}(z-1)$。

**状态。**已证明。

**对照。**M02（调和数级数、$\zeta(3)$）、M07。

## Entry 10——$h(z)$ 的函数方程

**陈述。**$h(z) = \sum_{k=1}^{\infty} H_k z^{k+1}/(k+1)^3$（$|z| < 1$）可解析延拓到整个复平面。Entry 10(i)(ii) 给出 $h(z)$ 的两个函数方程，右端含 $\mathrm{Li}_3$、$\mathrm{Li}_4$ 与 $\mathrm{Log}$ 的多项式（确切形式见原文，OCR 损坏严重，待核对）。

**出处。**Part I，Ch. 9，Entry 10（pp. 253–255）。笔记本 pp. 107–108：(i)(ii) 的右端须乘 $(-1)$。

**状态。**已证明（Berndt 给出证明；笔记本版有符号错误）。

**对照。**M02（多对数）、M12（解析延拓）。

## Entry 11——$F(x)$、$G(x)$；(11.3) 不成立

**陈述。**对 $-1 \le x \le 1$ 定义 $F(x)$、$G(x)$ 为 $h_k$ 的偶幂级数（分母 $(2k)^3$ 型；确切定义见原文，待核对）。Entry 11(i)(ii) 给出 $F$、$G$ 的函数方程（(11.1) 为 $xF'(x)$ 的积分表示；(i)(ii) 的确切形式待核对）。其中 (11.3) 声称
$$G(1) = \frac{\pi}{4}\sum_{k=0}^{\infty}\frac{(-1)^k}{(4k+1)^3} - \frac{\pi}{3\sqrt3}\sum_{k=0}^{\infty}\frac{1}{(2k+1)^3}.$$

**出处。**Part I，Ch. 9，Entry 11（pp. 255–257）。

**状态。**(11.3) **已否定**：Berndt 给出 $G(1) > 0.1529320988\ldots$ 而右端 $< 0.1442780636\ldots$，故不可能相等；数值复核：$G(1) = \sum h_k/(2k)^3 \approx 0.16227$（200000 项部分和），右端 $\approx 0.14402$。其余部分已证明。

**对照。**M02、M07。

## Entry 12——$H(x)$；例 (i)–(iii)

**陈述。**Entry 12 给出 $H(x)$（调和数生成函数）的函数方程与三个求值例：例 (i) $\sum_{k=1}^{\infty} H_k/(k^2 2^k) = \zeta(3) - \frac{\pi^2}{12}\mathrm{Log}\,2$；例 (ii) 印文为 $\sum_{k=1}^{\infty} H_k/(2k-1)^2 = \frac32\chi_3(1)$；例 (iii) $\sum_{k=1}^{\infty} h_k/k^2 = 2\chi_3(1)$（例 (i)(iii) 已数值复核通过；$\chi_3(1) = \frac78\zeta(3)$）。

**出处。**Part I，Ch. 9，Entry 12（pp. 257–260）。

**状态。**例 (i)(iii) 已证明。例 (ii) **印文有误（本轮发现，标待核对）**：印文版左端 $\approx 1.47443348$，右端 $\frac32\chi_3(1) = 21\zeta(3)/16 \approx 1.57769969$，差 0.103；书中证明实际算的是 $\{t(1)-t(-1)\}/2 = \sum_{k\ \mathrm{odd}} H_k/k^2 = \sum_{k=1}^{\infty} H_{2k-1}/(2k-1)^2$，该式数值 $\approx 1.57769896$，与右端差 $7.2\times 10^{-7}$，成立。故例 (ii) 左端的 $H_k$ 应为 $H_{2k-1}$。300 DPI 放大图已确认印文确为 $H_k$（非 $H_{2k-1}$），不是转录误读。

**对照。**M02（调和数级数）、M07。

## Entry 13——$\int (u^n/2)\cot(u/2)\,du$；Clausen 函数

**陈述。**定义 Clausen 函数 $\mathrm{Cl}_{2n}(x) = \sum_{k=1}^{\infty} \sin(kx)/k^{2n}$、$\mathrm{Cl}_{2n+1}(x) = \sum_{k=1}^{\infty} \cos(kx)/k^{2n+1}$（(13.1)(13.2)），$\mathrm{Cl}_1(x) = -\mathrm{Log}|2\sin(x/2)|$（(13.3)）。则
$$\int_0^x \frac{u^n}{2}\cot\frac{u}{2}\,du = \cos\frac{n\pi}{2}\cdot n!\,\zeta(n+1) - \sum_{j=0}^{n}(-1)^{j(j+1)/2}\frac{\Gamma(n+1)}{\Gamma(n+1-j)}x^{n-j}\mathrm{Cl}_{j+1}(x)$$
（$n = 1$、$x = 1$ 时已数值复核，精确成立）。

**出处。**Part I，Ch. 9，Entry 13（pp. 260–261）。

**状态。**已证明。

**对照。**M02（Clausen 函数）、M09（积分）、M10。

## Entry 14——$\int (u^n/2)(1/\sin u)\,du$；$D_n$ 函数

**陈述。**定义 $D_{2n}(x)$、$D_{2n+1}(x)$（(14.1)(14.2)，奇数分母的正弦/余弦级数），$D_1(x) = -\frac12\mathrm{Log}|\tan(x/2)|$（(14.3)）。则
$$\int_0^x \frac{u^n}{2}\frac{du}{\sin u} = \cos\frac{n\pi}{2}\cdot n!\,\chi_{n+1}(1) - \sum_{j=0}^{n}(-1)^{j(j+1)/2}\frac{\Gamma(n+1)}{\Gamma(n+1-j)}x^{n-j}D_{j+1}(x)$$
（$n = 1$、$x = 1$ 时已数值复核，精确成立）。

**出处。**Part I，Ch. 9，Entry 14（pp. 261–262）。笔记本 p. 109：(14.4) 右端写 $\mathrm{Li}_{n+1}(1)$，应为 $\chi_{n+1}(1)$。

**状态。**已证明。

**对照。**M02、M09、M10。

## Entry 15——$f_n(x) = \int x^n\cot x\,dx$；Proposition 15

**陈述。**记 $f_n(x) = \int x^n\cot x\,dx$。Proposition 15 (i)–(iv) 给出 $(\tan^{-1}x)^2$、$(\sin^{-1}x)^2$、$(\sin^{-1}x)^3$、$(\sin^{-1}x)^4$ 的 Maclaurin 级数，其中 (i) $\sum_{k=1}^{\infty}(-1)^{k-1}h_k/(2k) = (\tan^{-1}1)^2/2 = \pi^2/32$（已数值复核），(ii) $\sum_{k=0}^{\infty} 2^{2k}(k!)^2/(2k+2)! = (\sin^{-1}1)^2/2 = \pi^2/8$（已数值复核）。

**出处。**Part I，Ch. 9，Entry 15（pp. 262–264）；Proposition 15 在 p. 262。

**状态。**已证明。

**对照。**M02、M09（积分）、M12（幂级数）。

## Entry 16——中心二项系数级数与 Catalan 常数

**陈述。**记 Catalan 常数 $G = 0.915965594177219\ldots$（(16.3)）。Entry 16 (16.1) 给出中心二项系数级数的求值，例 (i) $\sum_{k=0}^{\infty} \binom{2k}{k}/(4^k(2k+1)^2) = \frac{\pi}{2}\mathrm{Log}\,2$；例 (ii) $\sum_{k=0}^{\infty} \binom{2k}{k}/(8^k(2k+1)^2) = \frac{\pi}{4\sqrt2}\mathrm{Log}\,2 + \frac{G}{\sqrt2}$（两式均已数值复核，30 位精度通过）。

**出处。**Part I，Ch. 9，Entry 16（pp. 264–265）。

**状态。**已证明。

**对照。**M02（中心二项系数级数）、M07、M04（$\pi$ 相关常数）。

## Entry 17——(17.1)；$\int_0^{1/\sqrt3}(\tan^{-1}t)/t\,dt$

**陈述。**Entry 17 (17.1) 给出一个含 $\tan^{-1}$ 的积分求值，例 (i)：
$$\int_0^{1/\sqrt3}\frac{\tan^{-1}t}{t}\,dt = -\frac{\pi}{12}\mathrm{Log}\,3 - \frac{5\pi^2}{18\sqrt3} + \frac{5\sqrt3}{4}\sum_{k=0}^{\infty}\frac{1}{(3k+1)^2}$$
（已数值复核，30 位精度通过）。

**出处。**Part I，Ch. 9，Entry 17（pp. 265–267）。Entry 32 应与本条对照。

**状态。**已证明。

**对照。**M02、M09（积分）、M04。

## Entry 18——中心二项系数级数（$\cos$ 与 $\sin$ 之差）

**陈述。**$x = \pi/6$ 时
$$\sum_{k=0}^{\infty}\binom{2k}{k}\frac{\cos^{2k+1}x - \sin^{2k+1}x}{2^{2k}(2k+1)^2} = \frac{\pi}{2}\mathrm{Log}(2\cos x) - \frac12\sum_{k=0}^{\infty}\binom{2k}{k}\frac{\sin^{2k+1}(2x)}{2^{2k}(2k+1)^2}$$
（已数值复核，30 位精度通过）。

**出处。**Part I，Ch. 9，Entry 18（pp. 267–268）。

**状态。**已证明。

**对照。**M02、M07。

## Entry 19——中心二项系数级数（$\cos$ 与 $\sin$ 之和）

**陈述。**$x = \pi/6$ 时
$$\sum_{k=0}^{\infty}\binom{2k}{k}\frac{\cos^{2k+1}x + \sin^{2k+1}x}{2^{2k}(2k+1)^2} = \frac{\pi}{2}\mathrm{Log}(2\cos x) + \sum_{k=0}^{\infty}(-1)^k\frac{\tan^{2k+1}x}{(2k+1)^2}$$
（已数值复核，30 位精度通过）。

**出处。**Part I，Ch. 9，Entry 19（pp. 268–269）。

**状态。**已证明。

**对照。**M02、M07。

## Entry 20——(20.1)；例 (i)(ii)

**陈述。**Entry 20 (20.1) 给出含 $2^{2k}(k!)^2/(2k+1)!$ 的级数求值，例 (i) $\sum_{k=0}^{\infty} 2^{2k}(k!)^2/((2k+1)!(2k+2)^2) = \frac{\pi^2}{8}\mathrm{Log}\,2 - \frac12\chi_3(1)$；例 (ii) $\sum_{k=0}^{\infty} 2^{k-1}(k!)^2/((2k+1)!(2k+2)^2) = \frac{\pi^2}{64}\mathrm{Log}\,2 + \frac{\pi}{8}G - \frac{5}{16}\chi_3(1)$（两式均已数值复核，30 位精度通过）。

**出处。**Part I，Ch. 9，Entry 20（pp. 269–270）。笔记本 p. 111：(20.1) 漏 $-\zeta(3)/4$ 一项。

**状态。**已证明。

**对照。**M02、M07。

## Entry 21——(21.2)；Nielsen 先证

**陈述。**(21.2)：$\sum_{k=1}^{\infty}(-1)^{k-1}h_k/k^2 = \pi G - 2\chi_3(1)$（已数值复核，30 位精度通过；$\chi_3(1) = \frac78\zeta(3)$）。Berndt 注：Nielsen 显然先建立了 (21.2)。

**出处。**Part I，Ch. 9，Entry 21（pp. 270–271）。笔记本 p. 112：(21.2) 右端错乘 $1/4$。

**状态。**已证明。

**对照。**M02、M07。

## Entry 22——中心二项系数级数（Entry 20 换元）

**陈述。**$0 < x \le \pi/2$ 时，$\sum_{k=0}^{\infty} 2^{2k}(k!)^2\{\cos^{2k+2}x + \sin^{2k+2}x\}/((2k+1)!(2k+2)^2)$ 等于含 $\frac{\pi}{2}\mathrm{Log}(2\cos x)$、$\sin(2x)$ 的同型级数与 $\chi_3(1)$ 的组合（确切系数见原文，待核对）。证明：将 Entry 20 中的 $x$ 换成 $\pi/2 - x$。

**出处。**Part I，Ch. 9，Entry 22（pp. 270–271）。

**状态。**已证明（由 Entry 20 推出）。

**对照。**M02、M07。

## Entry 23——中心二项系数级数与 $\tan$

**陈述。**$|x| \le \pi/4$ 时，$\sum_{k=0}^{\infty} 2^{2k}(k!)^2\sin^{2k+2}x\tan^{2k}x/((2k+1)!(2k+2)^2)$ 等于一个含 $h_k$ 的交错级数（(23.1)；确切右端见原文，待核对）。证明：由 Entry 20 得右端等于含 $\mathrm{Log}|2\sin 2x|$、$\cos(4kx)/k^3$、$\sin(4kx)/k^2$ 等的式子，再由 Entry 21 得 (23.1)。

**出处。**Part I，Ch. 9，Entry 23（pp. 271–272）。

**状态。**已证明（由 Entry 20、Entry 21 推出）。

**对照。**M02、M07。

## Entry 24——$\mathrm{Li}_2$ 的两变量函数方程

**陈述。**设 $x$、$y$、$\theta$、$\varphi$ 为实数，$xe^{i\theta} + ye^{i\varphi} = 1$，$0 \le x, y \le 1$，$-\pi < \theta, \varphi \le \pi$。则 (i) $\sum_{k=1}^{\infty} x^k\cos(k\theta)/k^2 + \sum_{k=1}^{\infty} y^k\cos(k\varphi)/k^2 = \frac{\pi^2}{6} - \mathrm{Log}\,x\,\mathrm{Log}\,y + \theta\varphi$；(ii) $\sum_{k=1}^{\infty} x^k\sin(k\theta)/k^2 + \sum_{k=1}^{\infty} y^k\sin(k\varphi)/k^2 = -\varphi\,\mathrm{Log}\,x - \theta\,\mathrm{Log}\,y$。两者合起来即 $\mathrm{Li}_2(xe^{i\theta}) + \mathrm{Li}_2(ye^{i\varphi}) = \frac{\pi^2}{6} - (\mathrm{Log}\,x + i\theta)(\mathrm{Log}\,y + i\varphi)$（Abel 恒等式）。例 (i) $x = 0.3$、$y = 0.7$、$\theta = \varphi = 0$ 时：$\mathrm{Li}_2(0.3) + \mathrm{Li}_2(0.7) = \frac{\pi^2}{6} - \mathrm{Log}(0.3)\mathrm{Log}(0.7)$（已数值复核，精确成立）。

**出处。**Part I，Ch. 9，Entry 24（pp. 272–273）。证明用 Entry 6(iii)（书中互见如此；Entry 6 的 (iii) 具体编号待核对）。

**状态。**已证明。

**对照。**M02（多对数函数方程）、M07。

## Entry 25——$\mathrm{Li}_2$ 的另一两变量函数方程

**陈述。**设 $x$、$y$、$\theta$、$\varphi$ 为实数，$xe^{i\theta} + ye^{i\varphi} = xye^{i(\theta+\varphi)}$，$0 < x, y \le 1$，$-\pi < \theta, \varphi \le \pi$。则 (i) 给出 $\mathrm{Li}_2$ 的另一两变量函数方程（确切形式见原文，待核对）。例：$x = y = 1$、$\theta = \pi/3$、$\varphi = -\pi/3$ 时，$2\sum_{k=1}^{\infty}\cos(k\pi/3)/k^2 = \pi^2/18$（已数值复核，误差 $< 10^{-5}$）。

**出处。**Part I，Ch. 9，Entry 25（pp. 272–273）。

**状态。**已证明。

**对照。**M02、M07。

## Entry 26——$\chi_2$ 的两变量函数方程

**陈述。**(i) $\chi_2(1/2) + \chi_2(1/3) = \frac{\pi^2}{8} - \frac12\mathrm{Log}(1/2)\mathrm{Log}(1/3)$（已数值复核，精确成立）。一般形式为 $\chi_2$ 的两变量函数方程（确切形式见原文，待核对）。

**出处。**Part I，Ch. 9，Entry 26（p. 273）。

**状态。**已证明。

**对照。**M02、M07。

## Entry 27(a)——$\varphi_r(x)$ 的渐近展开；常数 $C_r$

**陈述。**记 $\varphi_r(x) = \sum_{k=1}^{x} k^r\mathrm{Log}\,k$（(27.1)），$r > -1$。则当 $x \to \infty$ 时 $\varphi_r(x)$ 有 Euler–Maclaurin 型渐近展开，主项为 $\frac{x^{r+1}}{r+1}\mathrm{Log}\,x - \frac{x^{r+1}}{(r+1)^2} + \frac12 x^r\mathrm{Log}\,x + \cdots$，另含与 $x$ 无关的常数 $C_r$ 与 Bernoulli 数级数（确切展开式见原文，待核对），其中 $C_r = -\zeta'(-r)$（(27.7)）。推论：$C_0 = \frac12\mathrm{Log}(2\pi)$、$C_2 = \zeta(3)/(4\pi^2)$、$C_4 = -3\zeta(5)/(4\pi^4)$、$C_6 = 45\zeta(7)/(8\pi^6)$（四式均已数值复核，30 位精度通过）。

**出处。**Part I，Ch. 9，Entry 27(a)（pp. 273–275）。证明用 Euler–Maclaurin 求和法。应用见 MacLeod 的论文。

**状态。**已证明。

**对照。**M02、M10（Gamma 函数的类比：第 8 章主线的继续，见章首背景）、M12（渐近展开）、M01（$\zeta$ 函数）。

## Entry 27(b)——$C_r$ 的推论

**陈述。**设 $C_r$ 如 Entry 27(a)。则 $r > 0$ 时 $\varphi_r(x)$ 满足一个递推/积分关系（确切形式见原文，待核对），其推论给出 $C_r$ 的若干显式值。例 (i) 拉马努金所给不正确（笔记本 p. 113）。

**出处。**Part I，Ch. 9，Entry 27(b)（pp. 275–278）。推导见第一本笔记 p. 163。

**状态。**已证明（例 (i) 除外：拉马努金所给值不正确）。

**对照。**M02、M10、M12。

## Entry 28(a)——$f(r,x)$ 的递推

**陈述。**记 $f(r,x) = \frac{H_r}{r+1}B_{r+1}(x+1) - \sum_{1\le k\le (r+1)/2} \frac{r!B_{2k}H_{2k-1}x^{r+1-2k}}{(2k)!(r+1-2k)!}$（(28.1) 的定义形式；确切定义见原文）。Entry 28(a) 给出 $f(r,x)$ 的递推：$r = 2$ 时 $f_2(x) = \frac{B_3(x+1)-B_3}{6} + 2\int_0^x f_1(t)\,dt$（已数值复核：$x = 0.7$ 时精确成立；一般 $r$ 的递推形式待核对）。

**出处。**Part I，Ch. 9，Entry 28(a)（pp. 278–279）。

**状态。**已证明。

**对照。**M02、M10、M12。

## Entry 28(b)——$\varphi_r(x)$ 的展开式 (28.8)；印文有误

**陈述。**记 $\varphi_r(x) = \zeta'(-r, x+1) - \zeta'(-r)$（(28.3)，解析延拓定义）。Entry 28(b) 声称：$|x| < 1$、$r$ 为任意正整数时
$$\varphi_r(x) = \frac{H_r}{r+1}\{B_{r+1}(x+1) - B_{r+1}\} = \frac{\gamma x^{r+1}}{r+1} - \sum_{1\le k\le (r+1)/2}\frac{r!B_{2k}H_{2k-1}x^{r+1-2k}}{(2k)!(r+1-2k)!} - \sum_{k=0}^{r-1}\binom{r}{k}C_k x^{r-k} + \sum_{k=2}^{\infty}\frac{(-1)^k r!(k-1)!\zeta(k)x^{r+k}}{(r+k)!}, \tag{28.8}$$
其中 $H_n$ 由 (3.1) 定义，$C_k = -\zeta'(-k)$（$k \ge 0$）。

**出处。**Part I，Ch. 9，Entry 28(b)（pp. 279–281）。证明分解 $\zeta'(s, x+1)$ 为 $S_1$–$S_6$ 六部分（(28.9)），在 $s = -r$ 处取值：$S_1(-r)$ 见 (28.10)、$S_3(-r) = 0$ 见 (28.11)、$S_4(-r)$ 见 (28.13)、$S_6(-r)$ 见 (28.15)、$\lim(S_2 + S_5)$ 见 (28.22)。

**状态。印文有误（本轮发现，标待核对）**：(28.8) 的两行互不一致，且均与 (28.3) 的 $\varphi_r(x)$ 不符。数值证据（mpmath 50 位；$\zeta'$ 的值经有限差分与差分关系 $\varphi_1(x)-\varphi_1(x-1) = x\mathrm{Log}\,x$、$\varphi_1(2) = 2\mathrm{Log}\,2$ 双重确认）：$r = 1$、$x = 0.5$ 时第一行 $= 0.375$，第二行 $= -0.4413524244$，而 $\varphi_1(0.5) = \zeta'(-1, 3/2) - \zeta'(-1) = -0.1273230073$。订正形式（经 $r = 1$–$4$、$x = 0.2$–$0.7$ 七点 40 位复核，误差 $< 10^{-41}$）：
$$\varphi_r(x) = \frac{H_r}{r+1}\{B_{r+1}(x+1) - B_{r+1}\} - \frac{\gamma x^{r+1}}{r+1} - \sum_{1\le k\le r/2}\frac{r!B_{2k}H_{2k-1}x^{r+1-2k}}{(2k)!(r+1-2k)!} - \sum_{k=0}^{r-1}\binom{r}{k}C_k x^{r-k} + \sum_{k=2}^{\infty}\frac{(-1)^k r!(k-1)!\zeta(k)x^{r+k}}{(r+k)!}.$$
印文错误有二：①第二行漏了 $\frac{H_r}{r+1}\{B_{r+1}(x+1)-B_{r+1}\}$ 一项且 $\gamma$ 项符号反了（应为 $-\gamma x^{r+1}/(r+1)$）；②Bernoulli 和的上限 $(r+1)/2$ 应为 $r/2$（$r$ 为奇数时多出一项；根源在 (28.13) 的最后一步：中途和 $\sum_{k=1}^{r}$ 只到 $k = r$，而终式把 $2k = r+1$ 的项也收入了；逐项核对：$S_4(-r)$ 的直接值与 (28.13) 终式在 $r = 1$ 时差 $1/12$、$r = 3$ 时差 $11/720$，$r = 2$ 时一致；而 $S_1$–$S_6$ 的分解本身在 $r = 1,2,3$ 时精确成立，故错误只在最后的闭式化简）。另注：按书中所述，Bendersky 的定义即 (28.8) 去掉 Bernoulli 和（$r = 1$、$x = 0.5$ 时得 $-0.35802$），亦不等于 (28.3) 的 $\varphi_1(0.5)$，其 $\varphi$ 可能取了不同规范化，待核对。

**对照。**M02、M10（$\mathrm{Log}\,\Gamma$ 的类比）、M12、M01。

## Entry 29——$\varphi_r$ 的倍元公式；推论 1、2

**陈述。**记 $\varphi_r(x)$ 由 (28.3) 定义，$C_r$ 由 (27.7) 定义，$-1 < x \le 0$，$n$、$r$ 为自然数，则 $\varphi_r$ 满足一个倍元公式（左端含 $\varphi_r(x)$ 与 $\varphi_r$ 在 $x$ 的 $n$ 等分点处的值，右端为 $-\frac{B_{r+1}(x+1)}{r+1}\mathrm{Log}\,n + (1-n^{r+1})C_r$ 型的式子；确切形式见原文，待核对）。推论 1（$x = 0$）：$n$、$r$ 为任意正整数时的倍元关系。推论 2（$n = 2$）：$\varphi_r(-1/2) = -\frac{B_{r+1}}{(r+1)2^r}\mathrm{Log}\,2 + (2-2^{-r})C_r$（$r = 1$ 时已数值复核，精确成立）。

**出处。**Part I，Ch. 9，Entry 29（pp. 284–285）。

**状态。**已证明。

**对照。**M02、M10、M12。

## Entry 30——$\varphi_r(x-1) \pm \varphi_r(-x)$ 的 Fourier 级数

**陈述。**$0 < x < 1$。若 $r$ 为正偶数，则 (i) $\varphi_r(x-1) + \varphi_r(-x) = 2C_r +$ 一个 $\sum_{k=1}^{\infty}\cos(2\pi kx)/k^{r+1}$ 型的余弦级数项；若 $r$ 为正奇数，则 (ii) $\varphi_r(x-1) - \varphi_r(-x)$ 等于相应的正弦级数（(i)(ii) 的确切系数见原文，待核对）。$r = 2$、$x = 1/2$ 时 (i) 已数值复核：$\varphi_2(-1/2) + \varphi_2(-1/2) = 2C_2 + \frac{2}{(2\pi)^2}\cos\pi\sum_{k=1}^{\infty}\frac{\cos(\pi k)}{k^3}$，精确成立（与 Entry 29 推论 2 的 $\varphi_2(-1/2) = \frac74 C_2$ 一致）。证明用第 8 章 (17.15) 的 Hurwitz 公式求导得 (30.1)。拉马努金注：「更一般的定理对一切 $r$ 成立……」（笔记本 p. 114）；(28.3) 可定义一切实数 $r \ne -1$ 的 $\varphi_r(x)$，(30.1) 可给出 (i)(ii) 在 $r > -1$ 时的推广。

**出处。**Part I，Ch. 9，Entry 30（pp. 284–285）。

**状态。**已证明。

**对照。**M02、M10（Kummer 公式的类比：第 8 章第 17(iv) 节的平行结果）、M12。

## Entry 31(a)——$\psi(x)$ 与 $\varphi_1$ 的关系

**陈述。**记 $\psi(x)$ 由 (31.1) 定义，$C_r(x)$ 由 (28.3) 定义。则 $0 < x < 1$ 时
$$\psi(x) = \pi\{\varphi_1(x-1) - \varphi_1(-x)\} + \pi x\,\mathrm{Log}(2\sin\pi x)$$
（定义域端点待核对：原文作 $0 < x \le 1/3$ 或 $0 < x < 1$，OCR 未能确读）。证明用 Entry 30(ii) 与 Entry 16。

**出处。**Part I，Ch. 9，Entry 31(a)（pp. 285–286）。

**状态。**已证明。

**对照。**M02、M07、M10。

## Entry 31(b)——$\psi(x)$ 的函数方程；例 (i)–(iv)

**陈述。**记 $\psi(x)$ 由 (31.1) 定义，$h_k$ 由 (8.2) 定义。则 (i) $\psi(x) + \psi(1/2-x) = -\frac{\pi}{2}\mathrm{Log}(2\cos\pi x)$；(ii) $\psi(x)$ 与 $\sum_{k=0}^{\infty}(-1)^k\tan^{2k+1}(\pi x)/(2k+1)^2$ 的关系式；(iii) $\psi(x)$、$\psi(1-x)$、$\psi(2x)$ 的关系式（(i)–(iii) 的确切形式见原文，待核对）；(iv) 拉马努金版声称 $\psi(1/2-x) + \psi(1/2+x) = \pi\,\mathrm{Log}(2\cos\pi x)$，**错误**，正确版右端多一项无穷级数 $\sum_{k=1}^{\infty}(-1)^{k+1}\sin(2\pi kx)/k^2 = 2\pi\int_0^x \mathrm{Log}|2\cos\pi t|\,dt$。例 (iii) $\psi(1/3) = \frac{\sqrt3}{2}\sum_{k=0}^{\infty} 1/(3k+1)^2 - \frac{\pi^2}{9\sqrt3} + \frac{\pi}{6}\mathrm{Log}\,3$（已数值复核，精确成立）。

**出处。**Part I，Ch. 9，Entry 31(b)（pp. 286–288）。笔记本 p. 115：例 (ii) 拉马努金版读 $2\psi(1/4)$，应为 $\psi(1/4)$。

**状态。**已证明（(iv) 的拉马努金版除外，已纠正）。

**对照。**M02、M07、M10。

## Entry 32——超几何 ${}_3F_2$ 恒等式；例 (i)(v)(vi)(vii)

**陈述。**$|x| \le \pi/4$ 时
$$\sum_{k=0}^{\infty}\frac{2^{2k}(k!)^2}{(2k)!}\frac{\sin^{2k+1}(2x)}{(2k+1)^2} = 2\sum_{k=0}^{\infty}(-1)^k\frac{\tan^{2k+1}x}{(2k+1)^2}. \tag{32.1}$$
证明用 Proposition 15(ii) 再作代换。例 (i) $\sum_{k=0}^{\infty} 2^{2k}(k!)^2/((2k)!(2k+1)^2) = 2G$（Nielsen 先发现；比 Apéry 的 $\zeta(3)$ 公式 (0.1) 早约半世纪）；例 (v) $\sum_{k=0}^{\infty} 2^{2k}(k!)^2/((2k)!(2k+1)^2)\cdot(1-3/4^{k+1}) = \frac{\pi}{4}\mathrm{Log}(2+\sqrt3)$；例 (vi) $\sum_{k=0}^{\infty}(-4)^k(k!)^2/((2k)!(2k+1)^2) = \frac{\pi^2}{8} - \frac12\mathrm{Log}^2(1+\sqrt2)$；例 (vii) $\sum_{k=0}^{\infty}(-1)^k(k!)^2/((2k)!(2k+1)^2) = \frac{\pi^2}{6} - 3\mathrm{Log}^2\!\left(\frac{\sqrt5+1}{2}\right)$（四式均已数值复核，30 位精度通过；例 (i)(v) 的慢收敛尾项用直接求和加解析尾项 $\sqrt\pi/(2\sqrt N)$ 复核）。

**出处。**Part I，Ch. 9，Entry 32（pp. 288–290）。笔记本 p. 115：推论 (i) 拉马努金版左端第三项有小误印。本条应与 Entry 17 对照。

**状态。**已证明。

**对照。**M02（中心二项系数级数）、M07（超几何级数）、M04。

## Entry 33——$\int_0^{\pi/2} x\cos^n x\sin(nx)\,dx$ 等积分

**陈述。**(i) $\int_0^{\pi/2} x\cos^n x\sin(nx)\,dx = \frac{\pi}{2^{n+2}}H_n$；(ii) $\int_0^{\pi/2} \cos^n x\sin(nx)\,dx = \frac{1}{2^{n+1}}\sum_{k=1}^{n} 2^k/k$（$n = 1, 2$ 时两式均已数值复核，精确成立）。

**出处。**Part I，Ch. 9，Entry 33（pp. 290–293）。笔记本 p. 116。

**状态。**已证明。

**对照。**M02、M09（积分）、M13。

## Entry 34——二项和恒等式

**陈述。**$\sum_{k=0}^{\infty} \frac{1}{(2k+1)^2}\left(\frac{x}{1+x}\right)^{k+1} = \sum_{k=0}^{\infty}(-1)^k\frac{2^{2k}(k!)^2}{(2k+1)!}h_{k+1}x^{k+1}$（$x = 0.5$ 时已数值复核，精确成立）。

**出处。**Part I，Ch. 9，Entry 34（p. 293）。

**状态。**已证明。

**对照。**M02、M07、M13。

## Entry 35——$K_r$ 的递推；例 (i)–(iv)

**陈述。**记 $K_r = \sum_{k=1}^{\infty} 1/(k^r(k+1)^r)$，$A_n = (1+\cos\pi n)\zeta(n)$（$A_1 = 0$、$A_0 = -1$）。则 $K_r$ 满足递推 (35.1)（用 $A_n$ 表出；确切形式见原文，待核对）。例 (i) $K_2 = \pi^2/3 - 3$；例 (ii) $K_3 = 10 - \pi^2$；例 (iii) $K_4 = \pi^4/45 + 10\pi^2/3 - 35$；例 (iv) $K_5 = 126 - 35\pi^2/3 - \pi^4/9$（四式均已数值复核，30 位精度通过）。

**出处。**Part I，Ch. 9，Entry 35（p. 294）。

**状态。**已证明。

**对照。**M02（与 Ch. 7 Entry 22 的 $\sum 1/(k^n(k+1)^n)$ 为同一求和，跨章重复，互见，不去重）、M01（$\zeta$ 函数）。

## 小结

- 本章 35 节、139 条公式（章首计数），Entry 1–35 无缺号，另有分体 27(a)/27(b)、28(a)/28(b)、31(a)/31(b)。主线有四条：§§1–5 三角/二项级数变换（Entry 1–5）；§§6–12 多对数 $\mathrm{Li}_2$、$\mathrm{Li}_3$ 与 $\chi_n$、调和数级数（Entry 6–12；$g(z)$、$h(z)$）；§§13–15 Clausen 函数 $\mathrm{Cl}_n$、$D_n$ 与 $\int x^n\cot x\,dx$（Entry 13–15）；§§16–23 中心二项系数级数与 Catalan 常数 $G$（Entry 16–23）；§§24–26 $\mathrm{Li}_2$ 的复变函数方程（两变量和；Entry 24–26）；§§27–30 $\mathrm{Log}\,\Gamma$ 类比的继续（Entry 27–30）；§31 $\psi(x)$（Entry 31）；§32 超几何 ${}_3F_2$ 恒等式（Entry 32）；§33 积分（Entry 33）；§34 二项和恒等式（Entry 34）；§35 $K_r$ 递推（Entry 35）。
- 数值复核：verify1.py（mpmath 30 位，约 40 项）与 verify2.py（直接求和加解析尾项，约 30 项）合计约 70 项检查；除下述两处印文问题与 Berndt 已指出的两处错误外全部通过。注意：mpmath 的 `nsum` 对慢收敛级数（如 $\sum H_k/(k+1)^2$、$\sum 1/(c_k(2k+1)^2)$）会因尾项处理不佳而误报，复核时改用双精度直接求和加解析尾项（$\sum_{k>N} H_k/(k+1)^2$ 尾项 $\approx (\mathrm{Log}\,N+1)/N$；中心二项级数尾项 $\approx \sqrt\pi/(2\sqrt N)$）。
- Berndt 已指出的错误（写进各条，未擅自改动原文）：Entry 3 不成立（$n$ 充分大时，(3.3) 与 (3.4) 渐近不相容；$x$ 为 $\pi/2$ 奇数倍时对一切 $n$ 皆错）；公式 (11.3) 不成立（$G(1) > 0.1529320988\ldots$，右端 $< 0.1442780636\ldots$；数值 $G(1) \approx 0.16227$、右端 $\approx 0.14402$）；Entry 31(b)(iv) 拉马努金版错误（正确版多一项无穷级数）；其余笔记本疏失见章首列表。
- **本轮发现的原书印文问题**（均已数值证实，标待核对，未擅自改动原文）：
  1. Entry 12 例 (ii)：左端 $H_k$ 应为 $H_{2k-1}$。印文版 $\sum H_k/(2k-1)^2 \approx 1.47443348$，右端 $\frac32\chi_3(1) = 21\zeta(3)/16 \approx 1.57769969$，差 0.103；书中证明实际算的是 $\sum H_{2k-1}/(2k-1)^2 \approx 1.57769896$，差 $7.2\times 10^{-7}$。300 DPI 放大图确认印文确为 $H_k$。
  2. Entry 28(b) 公式 (28.8)：两行互不一致且均与 (28.3) 的 $\varphi_r(x)$ 不符。$r = 1$、$x = 0.5$ 时第一行 $= 0.375$，第二行 $= -0.4413524244$，$\varphi_1(0.5) = -0.1273230073$。订正形式见 Entry 28(b)（$r = 1$–$4$、$x = 0.2$–$0.7$ 七点 40 位复核，误差 $< 10^{-41}$）。印文错误：①第二行漏了 $\frac{H_r}{r+1}\{B_{r+1}(x+1)-B_{r+1}\}$ 一项且 $\gamma$ 项符号反了；②Bernoulli 和上限 $(r+1)/2$ 应为 $r/2$（根源在 (28.13) 的最后一步；$S_4(-r)$ 的直接值与 (28.13) 终式在 $r = 1$ 时差 $1/12$、$r = 3$ 时差 $11/720$，$r = 2$ 时一致）。
- 与 M 模块的对照：本章主线在 M02（无穷级数：多对数、调和数级数、中心二项系数级数、Clausen 函数）、M07（$q$-级数与超几何级数：Entry 32 的 ${}_3F_2$、中心二项系数）、M12（渐近分析：Entry 27(a) 的 Euler–Maclaurin 展开、Entry 28(b) 的级数展开）、M10（Gamma 函数的类比：§§27–30 接续第 8 章）、M09（积分：Entry 13–15、Entry 17、Entry 33）、M01（$\zeta$ 函数：$\chi_n(1)$、$C_r = -\zeta'(-r)$、$K_r$ 递推中的 $A_n$）、M04（$\pi$ 与 Catalan 常数 $G$）、M13（组合数学：Entry 5、Entry 34 的二项和）。
- M01 伯努利数定义缺口（见 Ch. 5 Entry 9）：本章多处用到 $B_n$、$B_n(x)$（Entry 6(vii)(viii)、Entry 27(a)、Entry 28(a)(b)、Entry 29 推论 2），均按当代定义（导言 (I1)）使用；M01 本身的定义缺口仍待日后补，不在本章文件里改动。

## 待核对清单

1. IMSC 整理表计本章的结果数（2026-11-06 多次 curl 得 000，不可达，待补）。
2. TIFR 影印版页码：本章各条在第二本笔记中的页码目前只核对了 Entry 2（p. 104）、Entry 7 例 (ii)/Entry 8 例/Entry 9(iii)/Entry 10（p. 107–108）、Entry 14（p. 109）、Entry 20（p. 111）、Entry 21（p. 112）、Entry 27 例（p. 113）、Entry 30 评注（p. 114）、Entry 31(b)(iv)/Entry 32（p. 115）、Entry 33（p. 116）、Entry 27(b) 推导（第一本笔记 p. 163），其余条目待按 TIFR 影印版逐条核对。
3. Entry 12 例 (ii) 的 $H_k$ 应为 $H_{2k-1}$：是否见于其他印次或勘误表，待查他版。
4. Entry 28(b) 公式 (28.8) 与 (28.13) 的印文问题：订正形式已数值证实，待查他版或勘误表确认；Bendersky 定义（(28.8) 去掉 Bernoulli 和）与 (28.3) 的 $\varphi_r$ 亦不一致，其规范化差异待核对。
5. Entry 2(i)(ii) 的确切闭式（$x$ 的多项式部分系数与 $\pi x^{r-1}$ 项的符号）：OCR 未能确读，待对原图逐字转录。
6. Entry 4 (4.1)(4.2) 的确切形式（$F_n$、$G_n$ 的定义式与求和上下限）：OCR 损坏严重，待对原图逐字转录。
7. Entry 10(i)(ii)、Entry 11(i)(ii) 与 $F(x)$、$G(x)$ 的确切定义：OCR 损坏严重，待对原图逐字转录。
8. Entry 22、Entry 23 的确切右端系数：待对原图逐字转录。
9. Entry 24 证明中引用的「Entry 6(iii)」的具体编号：待核对。
10. Entry 25(i)、Entry 26 一般形式的确切表述：待对原图逐字转录。
11. Entry 27(b) 的递推/积分关系确切形式：待对原图逐字转录。
12. Entry 28(a) 一般 $r$ 的递推形式：待对原图逐字转录。
13. Entry 29 倍元公式与推论 1 的确切形式：待对原图逐字转录。
14. Entry 30(i)(ii) 的确切系数：待对原图逐字转录（$r = 2$、$x = 1/2$ 的情形已数值复核）。
15. Entry 31(a) 的定义域端点（$0 < x \le 1/3$ 或 $0 < x < 1$）：OCR 未能确读，待对原图确认。
16. Entry 31(b)(i)–(iii) 的确切形式：待对原图逐字转录。
17. Entry 35 (35.1) 递推的确切形式：待对原图逐字转录。
18. Entry 1(i)(ii)、Entry 6(i)–(vi)、Entry 9（除 (9.4) 外）、Entry 12（除例 (i)–(iii) 外）的主方程确切形式：本文件只写了定义与已复核的特例/例题，主方程的逐字转录待补。
19. Entry 27(a) 渐近展开的确切形式（Bernoulli 级数项是否含 $\mathrm{Log}\,x$ 因子）：OCR 未能确读，待对原图逐字转录。

## 来源说明

- 底本：Bruce C. Berndt, *Ramanujan's Notebooks*, Part I, Springer, 1985, Ch. 9, pp. 232–294。电子版：archive.org `ramanujan_notebooks_i` 全文（DjVu OCR + PDF，PDF 页 = 书页 + 10，共 368 页）；本章 64 页（PDF pp. 242–304）均渲染 150 DPI 图片逐字读过，关键公式（Entry 12 例 (ii)、Entry 28(b) 的 (28.8)）另用 300 DPI 放大图确认；OCR 公式凡与图片或数值不符者一律纠正并注明。
- 数值复核：`~/workspace/.berndt-ch9-work/verify1.py`（mpmath 30 位，约 40 项）与 `verify2.py`（双精度直接求和加解析尾项，约 30 项）；两处印文问题（Entry 12 例 (ii)、Entry 28(b)）另用 50 位/40 位高精度复核（$\zeta'$ 的值经有限差分与差分关系双重确认）。
- 笔记本页码引用（第二本笔记，除注明外）：Entry 2 提示 p. 104；Entry 7 例 (ii)、Entry 8 例、Entry 9(iii)、Entry 10 均 p. 107（Entry 10 另 p. 108）；Entry 14 p. 109；Entry 20 p. 111；Entry 21 p. 112；Entry 27 例 p. 113；Entry 30 评注 p. 114；Entry 31(b)(iv)、Entry 32 p. 115；Entry 33 p. 116；Entry 27(b) 推导见第一本笔记 p. 163。
- 本文件只收公式陈述与自写导读/证明思路，未照抄 Berndt 的正文与证明。
