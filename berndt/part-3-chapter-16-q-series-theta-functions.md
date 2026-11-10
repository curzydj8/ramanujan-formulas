# Part III，Chapter 16——q-Series and Theta-Functions（q 级数与 theta 函数）

出处：Bruce C. Berndt，《Ramanujan's Notebooks》，Part III，Springer，1991，Ch. 16，书页 11–86。

本章是 Part III 的第一章、Berndt 五卷的第 16 章：前 17 节讲 q 级数，后 22 节讲 theta 函数。Berndt 在章首导言（pp. 11–12）中说，本章收有拉马努金最著名的若干定理；全卷六章（Ch. 16–21）由 theta 函数贯穿，见 Part III 导言（pp. 1–10）。本章共 **39 条编号 Entry（Entry 1–39，无缺号）**，另含分体与推论 70 个子标题（见“本章结构”表后的计数说明）；此外还有若干以 Lemma、Theorem、Corollary、Example 之名出现的结果（第 8 节引理 (8.1)、第 36 节 Schröter 公式 (36.1)(36.2) 与 Blecksmith–Brillhart–Gerst 定理 (36.15)、第 38 节五重积定理 (38.2)），书中明确标为引理或定理而非 Entry。

## 背景与记号

- 章首导言（pp. 11–12）：本章前 17 节主要讲 q 级数，后 22 节构成 theta 函数理论的系统发展。拉马努金重新发现了 Heine 的若干著名定理（含 Gauss 定理的 q 类比，Entry 4）；新结果以第 10–13 节的连分数最著（Entry 10 不是 q 连分数，更宜归入第 12 章；Entry 13 后来由拉马努金在“失落笔记”中推广；Entry 16 是 Rogers–Ramanujan 连分数的“有限”形式，Hirschhorn 1972 年首次在印刷品中证明，当时不知道结果已在笔记中）。theta 函数方面，拉马努金重新发现了 Jacobi《Fundamenta Nova》中的若干定理；Entry 27 给出模变换 $\tau \mapsto -1/\tau$ 的变换公式，未发现更一般的变换公式；Entry 19 为 Jacobi 三重积恒等式；若干证明用到 Watson 五重积恒等式，而五重积恒等式可在拉马努金“失落笔记”中找到，可见拉马努金应已发现它；本章末尾表明拉马努金已发现 Schröter 公式（虽未给出最一般形式）。新而深刻的定理见第 33–35 节、Entry 38(iv) 与第 31 节的推论。
- 章首点名的四项拉马努金原创名 theorem：Entry 14（beta 函数的 q 类比，积分求值最早见于拉马努金论文 [4]，[10, p. 57]，今有至少四种不同验证）；Entry 17（拉马努金的 ${}_1\psi_1$ 求和）；Entry 38(i)(ii)（Rogers–Ramanujan 恒等式）；Entry 38(iii)（Rogers–Ramanujan 连分数，拉马努金发表的论文中证明的唯一连分数）。另：Entry 7 蕴含 Rogers–Ramanujan 恒等式为极限情形，拉马努金显然没有注意到这一点。
- 本章的较早版本：C. Adiga、B. C. Berndt、S. Bhargava 与 G. N. Watson 合著《Chapter 16 of Ramanujan's second notebook: theta-functions and q-series》，Memoirs of the American Mathematical Society，第 53 卷第 315 号，1985 年 1 月；本书的修订版经美国数学会许可刊出（版权页说明）。
- 记号（pp. 12–13）：全章假定 $|q| < 1$。对任意复数 $a$，$(a)_k := (a;q)_k := (1-a)(1-aq)\cdots(1-aq^{k-1})$，$(a)_\infty := (a;q)_\infty := \prod_{k=0}^{\infty}(1-aq^k)$；拉马努金记 $(a)_\infty$ 为 $\eta(-a,x)$（其中 $x = q$）。基本超几何级数 ${}_{s+1}\phi_s$ 按 (0.1) 定义（$|x| < 1$，分母因子 $(b_j)_k \ne 0$）；$s$ 较小时写 ${}_{s+1}\phi_s(a_1,\dots,a_{s+1};b_1,\dots,b_s;x)$。为标明底 $q$，可写 ${}_{s+1}\phi_s(a_1,\dots,a_{s+1};b_1,\dots,b_s;q;x)$。底不是 $q$ 时写明，如 $(a;q^2)_k$、$(a;q^4)_\infty$。
- theta 函数记号（第 18 节，(18.1)）：拉马努金的一般 theta 函数

$$f(a,b) = 1 + \sum_{k=1}^{\infty}(ab)^{k(k-1)/2}(a^k+b^k) = \sum_{k=-\infty}^{\infty}a^{k(k+1)/2}b^{k(k-1)/2}, \qquad |ab| < 1.$$

置 $a = qe^{2iz}$、$b = qe^{-2iz}$、$q = e^{\pi i\tau}$（$z$ 复数，$\mathrm{Im}\,\tau > 0$），则 $f(a,b) = \vartheta_3(z,\tau)$（Whittaker–Watson 记号）。全章保留拉马努金的 $f(a,b)$ 记号。
- 单变量记号（第 22 节）：$\varphi(q) := f(q,q) = 1 + 2\sum_{k=1}^{\infty}q^{k^2}$，$\psi(q) := f(q,q^3) = \sum_{k=0}^{\infty}q^{k(k+1)/2}$，$f(-q) := f(-q,-q^2) = (q;q)_\infty$，$\chi(q) := (-q;q^2)_\infty$。另有一单变量记号 $f(q)$（见 Entry 24 下的注记）：本文件经数值核对确认，书中 $f(q)$ 指 $f(q,-q^2)$，即 $f(q) = (-q;q^2)_\infty(q^2;q^2)_\infty$。
- 第 35 节记号：$L = 1 - 24\sum_{k=1}^{\infty}kq^k/(1-q^k)$，$M = 1 + 240\sum_{k=1}^{\infty}k^3q^k/(1-q^k)$，$N = 1 - 504\sum_{k=1}^{\infty}k^5q^k/(1-q^k)$（与 Part II Ch. 15 第 9 节的 $L$、$M$、$N$ 相同；拉马努金名篇 [11] 中分别记为 $P$、$Q$、$R$）。第 35 节的 Bernoulli 数 $B_n$（$0 \le n < \infty$）与 Euler 数 $E_{2n}$ 按 Gradshteyn–Ryzhik 的定义（(35.1)：$x/(e^x-1) = \sum_{n=0}^{\infty}B_nx^n/n!$，$|x| < 2\pi$；$\sec x = \sum_{n=0}^{\infty}(-1)^nE_{2n}x^{2n}/(2n)!$，$|x| < \pi/2$），与拉马努金所用的约定不同。
- 本章与已填章节的互见：Part II Ch. 11 的超几何与 theta（Entry 22 的“amazing”公式、Entry 34 的 $\Gamma(1/4)$ 常数）与本章 Entry 2–9 的基本超几何同源，Ch. 11 Entry 24 的形式恒等式与本章 Entry 17 的 ${}_1\psi_1$ 求和同属一脉；Part II Ch. 12 的连分数（Entry 40 的五参数 Gamma 商连分数、Entry 34/39/40 三条最主要 Gamma 公式）与本章 Entry 10–16、Entry 38(iii)、Entry 39 的 q 连分数衔接，Entry 10 的证明直接引用 Ch. 12 Entry 40；Part II Ch. 14 的 theta 函数变换（Entry 7）与 Eisenstein 级数（Entry 13 的 Bernoulli 数级数、Entry 21 的 $\zeta(2n+1)$ 公式）与本章 Entry 20、Entry 27 的变换公式、Entry 35 的 $P_n$、$Q_n$ 直接衔接，Entry 20 在 Ch. 14 中亦有记录（[9, Vol. 2, p. 169, Entry 7]）；Part II Ch. 15 的 theta 反演 (8.3) 与模形式（Entry 12 的 $\Delta(\tau)$、Entry 12(ix) 已注明为 Part III Ch. 16 Entry 35(i) 的特例、Entry 13 的 $\Phi_v(q)$、Entry 14 的 Eisenstein 递推、Entry 15–16 的模方程先声）与本章 Entry 19、Entry 27、Entry 35(i)、§§36–39 的 Schröter 公式与模方程直接衔接，Ch. 15 Entry 10(ii) 的级数“度”定义（笔记 pp. 186–187）是本章 Entry 26 的依据。
- 与主题模块的对照总览：q 级数主线见 **M07**（全章前半 §§1–17：Entry 1–17，q-Pochhammer、q-二项式定理、Heine 变换、${}_1\psi_1$ 求和；后半 §§18–39：Jacobi 三重积 Entry 19、Rogers–Ramanujan 恒等式 Entry 38(i)(ii)、五重积定理 (38.2)）；theta 函数与模形式见 **M06**（§§18–39：$f(a,b)$、$\varphi$、$\psi$、$\chi$、Entry 20 与 Entry 27 的变换公式、§35 的 $L$、$M$、$N$ 与 $P_n$、$Q_n$、§§36–39 的 Schröter 公式与模方程）；连分数见 **M03**（Entry 10、11、12、13、15、16、38(iii)、39）；分拆见 **M05**（Entry 22(iii) 的 Euler 五边形数定理、Entry 38(i)(ii) 的分拆解释、Entry 38(iii) 的喷泉组合解释、Entry 31 例 (iii) 的最近整数）；无穷级数见 **M02**（Entry 1–9 的基本超几何级数、Entry 21 与 Entry 23 的对数级数）；椭圆函数见 **M11**（Entry 33(iii) 的 $\mathrm{dn}\,u$ Fourier 级数、Entry 27 的 $\vartheta_3$ 与 $\eta$ 变换、§36 的 Schröter 公式）；Gamma 函数见 **M10**（Entry 1 的 q-Gamma 函数 $\Gamma_q$、Entry 10 的 Gamma 商连分数、Entry 14 的 q-beta 积分）；数论见 **M01**（Entry 35 的 Bernoulli 数与 Euler 数、§35 的 $L$、$M$、$N$、Entry 23 的 $\chi(q)$ 与 $\varphi(q)$ 对数级数）；渐近展开见 **M12**（Entry 26 的级数“度”与 Euler–Maclaurin 求和公式）；组合见 **M13**（Entry 38(iii) 的 $(n,k)$ 喷泉计数）；$\pi$ 与特殊常数见 **M04**（Entry 27 的 $\alpha\beta = \pi$、$\alpha\beta = \pi^2$ 变换、Entry 39 的黄金比 $(\sqrt{5}\pm 1)/2$）。

## 本章结构

| Entry | 主题 | 书页 |
|---|---|---|
| Entry 1 | q-Gamma 函数的极限：(i)–(iv) | 13 |
| Entry 2 | q-二项式定理（Rothe–Cauchy） | 14 |
| Entry 3 | $\sum a^kq^{k^2}/((q)_k(aq)_k) = 1/(aq)_\infty$（Cauchy–Jacobi） | 14 |
| Entry 4 | Heine 求和公式（Gauss 求和的 q 类比） | 14 |
| Entry 5 | Rogers 求和公式（Jackson–Dougall 的极限情形） | 14–15 |
| Entry 6 | Heine 变换公式 ${}_2\phi_1$ | 15 |
| Entry 7 | Watson 变换导出的 ${}_3\phi_2$ 恒等式（Rogers–Ramanujan 恒等式的母公式） | 16 |
| 第 8 节引理 (8.1) | ${}_3\phi_2$–${}_3\phi_2$ 变换 | 17 |
| Entry 8 | Pfaff 变换的 q 推广 | 17 |
| Entry 9 | ${}_2\phi_1$ 极限恒等式与推论 (i)(ii) | 18 |
| Entry 10 | Gamma 商的连分数（Watson–Ch. 12 Entry 40 的应用） | 19 |
| Entry 11 | 含 $a = bq^m$ 情形的连分数恒等式 | 21 |
| Entry 12 | Rogers–Ramanujan 型连分数（Göllnitz–Gordon 连分数的推广） | 24 |
| Entry 13 | Eisenstein 连分数 $\sum (-a)^kq^{k(k+1)/2}$ | 27 |
| Entry 14 | q-beta 积分（Ramanujan 的 q 类比 beta 函数） | 29 |
| Entry 15 | $f(b,a)/f(bq,a)$ 的连分数与推论 | 30 |
| Entry 16 | Entry 15 的有限形式（Rogers–Ramanujan 连分数的有限版） | 31 |
| Entry 17 | Ramanujan 的 ${}_1\psi_1$ 求和与推论 | 32 |
| Entry 18 | $f(a,b)$ 的基本性质 (i)–(iv) | 34 |
| Entry 19 | Jacobi 三重积恒等式 | 35 |
| Entry 20 | theta 函数的经典变换公式（Ch. 14 Entry 7 亦有记录） | 36 |
| Entry 21 | $\mathrm{Log}(-a;q)_\infty$ 与 $\mathrm{Log}\,f(a,b)$ 的级数 (21.1)(21.2) | 36 |
| Entry 22 | $\varphi(q)$、$\psi(q)$、$f(-q)$、$\chi(q)$ 的乘积表示 (i)–(iv) | 36–37 |
| Entry 23 | $\mathrm{Log}\,\varphi$、$\mathrm{Log}\,\psi$、$\mathrm{Log}\,f(-q)$、$\mathrm{Log}\,\chi$ 的级数 (i)–(v) | 38 |
| Entry 24 | $\varphi$、$\psi$、$\chi$、$f$ 的比值恒等式 (i)–(iv) | 39 |
| Entry 25 | $\varphi$、$\psi$ 的七条恒等式 (i)–(vii) | 40 |
| Entry 26 | $G(q)$ 为 $\frac12$ 度的完全纯双重级数与推论 (i)(ii) | 42 |
| Entry 27 | $\vartheta_3$ 与 $\eta$ 的模变换公式 (i)–(v) | 43 |
| Entry 28 | $f$ 的乘积恒等式与推论 (28.1) | 44 |
| Entry 29 | $f$ 的加法公式 (i)(ii) | 45 |
| Entry 30 | $f$ 的六条恒等式 (i)–(vi) | 46 |
| Entry 31 | $f(U_1,V_1)$ 的 $n$ 项展开与推论 (i)(ii)、例 (i)–(v) | 48 |
| Entry 32 | $\varphi'/\varphi$、$\psi'/\psi$ 的对数导数恒等式 (i)–(iv) | 51–52 |
| Entry 33 | 三角级数的对数恒等式 (i)(ii)(iii) 与推论、(33.5) | 52–54 |
| Entry 34 | Entry 34(i)：$\varphi^2(q)$ 的对数恒等式 (34.1) | 54 |
| Entry 35 | $P_n$、$Q_n$ 的递推 (i)(ii) 与例 (i)–(iii)（$L$、$M$、$N$ 多项式） | 61–65 |
| Entry 36 | $S$、$D$ 的求和公式 (i)(ii)；Schröter 公式 (36.1)(36.2)；Blecksmith 定理 (36.15) | 65–73 |
| Entry 37 | $\varphi$、$\psi$ 乘积的三条恒等式 (i)(ii)(iii) | 73 |
| Entry 38 | Rogers–Ramanujan 恒等式 (i)(ii)、Rogers–Ramanujan 连分数 (iii)、五重积恒等式 (iv) | 77–80 |
| Entry 39 | 黄金比连分数恒等式 (i)(ii) 与推论 (i)(ii) | 83–86 |

计数说明：编号 Entry 1–39 共 39 条，无缺号。分体与推论子标题 70 个：Entry 1(i)–(iv) 4、Entry 9 推论 (i)(ii) 2、Entry 15 推论 1、Entry 17 推论 1、Entry 22(i)–(iv) 4、Entry 23(i)–(v) 5、Entry 24(i)–(iv) 4、Entry 25(i)–(vii) 7、Entry 26 推论 (i)(ii) 2、Entry 27(i)–(v) 5、Entry 28 推论 1、Entry 29(i)(ii) 2、Entry 30(i)–(vi) 6、Entry 31 推论 (i)(ii) 2、Entry 32(i)–(iv) 4、Entry 33(i)(ii)(iii) 3 与推论 1、Entry 34(i) 1、Entry 35(i)(ii) 2、Entry 36(i)(ii) 2、Entry 37(i)(ii)(iii) 3、Entry 38(i)–(iv) 4、Entry 39(i)(ii) 2 与推论 (i)(ii) 2。按“无分体的 Entry 计 1、有分体的 Entry 计其分体数”的口径，Entry 标题共 $17 + 70 = 87$ 个（17 条无分体的 Entry：Entry 2、3、4、5、6、7、8、10、11、12、13、14、16、18、19、20、21）。另有第 31 节例 (i)–(v) 5 个、第 35 节例 (i)–(iii) 3 个、第 23 节例 1 个，共 9 个例题标题未计入 87 个之内。

## Entry 1

**陈述。** 设 $q$ 为实数，$|q| < 1$；$a$ 与 $x$ 为任意复数；取 $(1-a)^x$ 与 $(1-q)^x$ 的主支。则

$$\begin{aligned}
\text{(i)}\quad \lim_{q\to 1-}\frac{(a)_\infty}{(aq^x)_\infty} &= (1-a)^x, \\
\text{(ii)}\quad \lim_{q\to 1-}\frac{(q)_\infty}{(1-q)^x(q^{x+1})_\infty} &= \Gamma(x+1), \\
\text{(iii)}\quad (a)_\infty &= \prod_{k=0}^{n-1}(aq^k;q^n)_\infty, \\
\text{(iv)}\quad (a)_\infty &= \frac{(a;\sqrt{q})_\infty}{(a\sqrt{q};\sqrt{q})_\infty}.
\end{aligned}$$

**说明。** (i) 的证明：先设 $|a| < 1$，在下述 Entry 2 的 (2.1) 中以 $aq^x$ 代 $a$、以 $q^{-x}$ 代 $t$，由二项式定理得极限；一般情形由解析延拓。(ii) 的证明属 R. W. Gosper（见 Andrews 专著 [18, p. 109]）。q-Gamma 函数 $\Gamma_q(x)$ 定义为

$$\Gamma_q(x) = \frac{(q)_\infty}{(q^x)_\infty}(1-q)^{1-x}. \tag{1.1}$$

于是 Entry 1(ii) 可改写为 $\lim_{q\to 1-}\Gamma_q(x+1) = \Gamma(x+1)$。Berndt 注：Entry 1(i)(ii) 的证明不完全严格，因在求和号与乘积号下取极限未加论证；T. H. Koornwinder [1] 已论证了这些形式步骤并给出严格证明。

**状态：** 已证明（Koornwinder 严格化之前的形式证明见书中；(iii)(iv) 为初等恒等式）。**对照：** M07（q-Pochhammer 与 q-Gamma 函数）、M10（$\Gamma$ 函数）。

## Entry 2

**陈述。** 若 $|q|, |a| < 1$，则

$$\frac{(-b)_\infty}{(a)_\infty} = \sum_{k=0}^{\infty}\frac{(-b/a)_k}{(q)_k}a^k.$$

置 $-b = at$，上式可写为

$$\frac{(at)_\infty}{(a)_\infty} = \sum_{k=0}^{\infty}\frac{(t)_k}{(q)_k}a^k. \tag{2.1}$$

**说明。** 此即 q-二项式定理。最早的已知出处为 Rothe [1]；亦为 Cauchy [1]、[2, pp. 42–50] 所发现，并曾归于 Euler、Gauss 与 Heine 名下。拉马努金对 Entry 2 的证明见其论文 [4]（[10, pp. 57–58]）。

**状态：** 已证明（经典结果）。**对照：** M07（q-二项式定理，M07.2）、M13。

**我自验：** 取 $q = 0.5$、$a = 0.3$、$b = 0.2$：左端 $2.85515071519$、右端 $2.85515071519$，差 $1.2\times 10^{-30}$。

## Entry 3

**陈述。** 若 $a$ 任意、$|q| < 1$，则

$$\frac{1}{(aq)_\infty} = \sum_{k=0}^{\infty}\frac{a^kq^{k^2}}{(q)_k(aq)_k}. \tag{3.1}$$

**说明。** (3.1) 通常归于 Cauchy [1]、[2, pp. 42–50]；但它见于 Jacobi《Fundamenta Nova》[1]、[2, p. 232]，早 14 年。证明推迟至第 9 节，在那里证明一个推广（Entry 9）。

**状态：** 已证明（由 Entry 9 推出；见 Entry 9 的注）。**对照：** M07、M02。

**我自验：** 取 $q = 0.5$、$a = 0.4$：左端 $1.53759589061$、右端 $1.53759589061$，差 $5.9\times 10^{-31}$。

## Entry 4

**陈述。** 若 $|abc| < 1$，则

$$\frac{(ab)_\infty(ac)_\infty}{(a)_\infty(abc)_\infty} = \sum_{k=0}^{\infty}\frac{(1/b)_k(1/c)_k}{(q)_k(a)_k}(abc)^k.$$

**说明。** 此为 Heine [1] 的著名结果，即普通超几何级数 Gauss 求和公式的 q 类比。证明见 Andrews 的书 [9, p. 20]。在 Entry 4 中以 $1/t$ 代 $b$、以 $1/c$ 代 $c$、再以 $atc$ 代 $a$、最后置 $c = 0$，得 (2.1)；令 $b, c \to 0$ 并以 $aq$ 代 $a$，得 Entry 3。Askey [8, p. 69] 指出，拉马努金表述基本超几何级数的发现时，强调和的值的对称性，Entry 4 与 Entry 5 即为明证。

**状态：** 已证明（Heine 的经典结果；证明见 Andrews [9, p. 20]）。**对照：** M07、M02。

## Entry 5

**陈述。** 若 $|q|, |abcd| < 1$，则

$$\sum_{k=0}^{\infty}\frac{(a/q)_k(1/b)_k(1/c)_k(1/d)_k(1-aq^{2k-1})(abcd)^k}{(ab)_k(ac)_k(ad)_k(q)_k(1-a/q)} = \frac{(a)_\infty(abc)_\infty(abd)_\infty(acd)_\infty}{(ab)_\infty(ac)_\infty(ad)_\infty(abcd)_\infty}.$$

**说明。** Entry 5 最早由 L. J. Rogers [2, p. 29] 发现（其中一因子中的 $v - \sqrt{q}$ 应改为 $1 - v\sqrt{q}$）；它是 F. H. Jackson [1] 发现的更一般恒等式的极限情形；Jackson 定理的另一证明见 Andrews–Askey [1]。书中证明：Jackson 恒等式即 Dougall 定理的 q 类比（Bailey [4, p. 67]），为

$${}_8\phi_7\left[\begin{matrix}a, q\sqrt{a}, -q\sqrt{a}, b, c, d, e, q^{-N} \\ \sqrt{a}, -\sqrt{a}, aq/b, aq/c, aq/d, aq/e, aq^{N+1}\end{matrix}; q\right] = \frac{(aq)_N(aq/cd)_N(aq/bd)_N(aq/bc)_N}{(aq/b)_N(aq/c)_N(aq/d)_N(aq/bcd)_N}, \tag{5.1}$$

其中 $N$ 为正整数，$a^2q^{N+1} = bcde$；并用

$$\frac{(q\sqrt{a})_k(-q\sqrt{a})_k}{(\sqrt{a})_k(-\sqrt{a})_k} = \frac{1-aq^{2k}}{1-a}. \tag{5.2}$$

令 $N \to \infty$、$e \to 0$，再以 $a/q$ 代 $a$、以 $1/b$、$1/c$、$1/d$ 分别代 $b$、$c$、$d$，即得 Entry 5。

**状态：** 已证明（由 Jackson–Dougall 恒等式推出）。**对照：** M07、M02。

## Entry 6

**陈述。** 若 $|a|, |c|, |q| < 1$，则

$${}_2\phi_1(b/a, c; d; a) = \frac{(b)_\infty(c)_\infty}{(a)_\infty(d)_\infty}{}_2\phi_1(d/c, a; b; c).$$

**说明。** 此优美定理属 Heine [1]；基于 Entry 2 的简单证明见 Andrews 的书 [9, p. 19]。反方向，在 Entry 6 中置 $c = d$ 得 Entry 2。把 Entry 6 用三次得

$$\sum_{k=0}^{\infty}\frac{(a)_k(b)_k}{(c)_k(q)_k}t^k = \frac{(b)_\infty(at)_\infty}{(c)_\infty(t)_\infty}\sum_{k=0}^{\infty}\frac{(c/b)_k(t)_k}{(at)_k(q)_k}b^k = \cdots = \frac{(abt/c)_\infty}{(t)_\infty}\sum_{k=0}^{\infty}\frac{(c/a)_k(c/b)_k}{(c)_k(q)_k}\left(\frac{abt}{c}\right)^k, \tag{6.1}$$

下文要用。

**状态：** 已证明（Heine 的经典结果）。**对照：** M07（Heine 变换）、M02。

## Entry 7

**陈述。** 若 $|a|, |q| < 1$，则

$$\sum_{k=0}^{\infty}\frac{(a)_k(d/b)_k(d/c)_k(d/q)_k(1-dq^{2k-1})(bc/a)^kq^{k(k-1)}}{(b)_k(c)_k(d/a)_k(q)_k(1-d/q)} = \frac{(a)_\infty(d)_\infty}{(b)_\infty(c)_\infty}\sum_{k=0}^{\infty}\frac{(b/a)_k(c/a)_k}{(d/a)_k(q)_k}a^k.$$

**说明。** Watson [1] 的定理：若 $a^2q^{N+1} = bcde$，则

$${}_8\phi_7\left[\begin{matrix}a, q\sqrt{a}, -q\sqrt{a}, b, c, d, e, q^{-N} \\ \sqrt{a}, -\sqrt{a}, aq/b, aq/c, aq/d, aq/e, aq^{N+1}\end{matrix}; q\right] = \frac{(aq)_N(aq/de)_N}{(aq/d)_N(aq/e)_N}{}_4\phi_3\left[\begin{matrix}aq/bc, d, e, q^{-N} \\ aq/b, aq/c, de/a\end{matrix}; q\right]. \tag{7.1}$$

令 $N \to \infty$、$e \to 0$ 得 (7.2)，再令 $d \to \infty$ 并化简即得 Entry 7；书中给出证明。Berndt 注：Rogers–Ramanujan 恒等式是 Entry 7 的极限情形（见 Entry 38 的证明），但拉马努金似乎没有注意到这一点。

**状态：** 已证明（由 Watson 定理推出）。**对照：** M07（Watson 定理、Rogers–Ramanujan 恒等式的母公式）、M02。

**我自验：** 取 $q = 0.5$、$a = 0.3$、$b = 0.2$、$c = 0.4$、$d = 0.15$：左端 $1.23946561463$、右端 $1.23946561463$，差 $2.0\times 10^{-31}$（以 30 位直接求和 + 解析尾项计）。

## 第 8 节引理 (8.1)

**陈述。** 若 $|de/abc| < 1$，则

$${}_3\phi_2\left[\begin{matrix}a, b, c \\ d, e\end{matrix}; \frac{de}{abc}\right] = \frac{(e/a)_\infty(de/bc)_\infty}{(e)_\infty(de/abc)_\infty}{}_3\phi_2\left[\begin{matrix}a, d/b, d/c \\ d, de/bc\end{matrix}; \frac{e}{a}\right]. \tag{8.1}$$

**说明。** 此为 Sears [1] 发现的优美恒等式。证明见 Bailey 的书 [4, p. 75] 或 Slater 的书 [2, p. 111]。本节引理只记其一，另一与之相关的恒等式见 [2, p. 111]。

**状态：** 已证明（Sears 发现；证明见 Bailey [4]、Slater [2]）。**对照：** M07（Sears 变换）、M02。

## Entry 8

**陈述。** 若 $|a| < 1$、$|ac| < 1$，则

$$\frac{(a)_\infty}{(b)_\infty}\sum_{k=0}^{\infty}\frac{(c)_k(b/a)_k}{(d)_k(q)_k}a^k = \sum_{k=0}^{\infty}\frac{(-1)^k(b/a)_k(d/c)_k}{(b)_k(d)_k(q)_k}(ac)^kq^{k(k-1)/2}.$$

**说明。** 此为 Pfaff 变换公式（[1]、[2, p. 76]）的 q 推广。证明由引理 (8.1) 直接推出。

**状态：** 已证明（由 Sears 变换推出）。**对照：** M07（Pfaff 变换的 q 推广）、M02。

## Entry 9

**陈述。** 若 $a \ne 0$，则

$$(aq)_\infty\sum_{k=0}^{\infty}\frac{b^kq^{k^2}}{(q)_k(aq)_k} = \sum_{k=0}^{\infty}\frac{(-1)^k(b/a)_k}{(q)_k}a^kq^{k(k+1)/2}.$$

**说明。** 证明思路（自写）：用 Entry 2 的 (2.1) 展开 $(aq)_\infty$ 的倒数并逐项相乘，合并后由 Entry 2 再次求和即得。书中给出两种证明：其一用 Entry 2；其二用 (6.1) 与 Entry 2。令 $b = a$ 得 Entry 3。Entry 3 与 Entry 9 在 Heine 1886 年的《Theorie der Kugelfunctionen》中可找到（第 92 页），但不含 Entry 9 的推论。

**推论 (i)。** 取 $a = 1$、$b = q$，得

$$(q)_\infty\sum_{k=0}^{\infty}\frac{q^{k(k+1)}}{(q)_k^2} = \sum_{k=0}^{\infty}(-1)^kq^{k(k+1)/2}.$$

**推论 (ii)。** 取 $a = q$、$b = -q$，得

$$(q;q^2)_\infty\sum_{k=0}^{\infty}\frac{q^{k(2k+1)}}{(q)_{2k}} = \sum_{k=0}^{\infty}(-1)^kq^{k^2}.$$

**状态：** 已证明（两种证明见书中）。**对照：** M07、M02。

**我自验：** 取 $q = 0.5$、$a = 0.4$、$b = 0.3$：左端 $0.907955664488$、右端 $0.907955664488$，差 $3.0\times 10^{-31}$。推论 (i)(ii) 未逐项数值复核（见待核对清单）。

## Entry 10

**陈述。** 设 $\ell$、$m$、$n$ 与 $x$ 为复数；$P$ 为

$$P = \frac{\Gamma(\frac12(x+\ell+m+n+1))\Gamma(\frac12(x-\ell+m-n+1))\Gamma(\frac12(x+\ell-m-n+1))\Gamma(\frac12(x-\ell-m+n+1))}{\Gamma(\frac12(x+\ell+m-n+1))\Gamma(\frac12(x-\ell+m+n+1))\Gamma(\frac12(x+\ell-m+n+1))\Gamma(\frac12(x-\ell-m-n+1))},$$

其中分母的 $\Gamma$ 值都非零、非无穷；且 $\ell$、$m$、$n$ 中至少一个为整数或 $\mathrm{Re}\,x > 0$。则

$$\begin{aligned}
\frac{1-P}{1+P} &= \frac{2\ell mx}{x^2+\ell^2+m^2-n^2-1} \\
&\quad + \frac{4(x^2-1^2)(\ell^2-1^2)(m^2-1^2)}{3(x^2+\ell^2+m^2-n^2-5)} \\
&\quad + \frac{4(x^2-2^2)(\ell^2-2^2)(m^2-2^2)}{5(x^2+\ell^2+m^2-n^2-13)} + \cdots \\
&\quad + \frac{4(x^2-(k-1)^2)(\ell^2-(k-1)^2)(m^2-(k-1)^2)}{(2k-1)(x^2+\ell^2+m^2-n^2-2k^2+2k-1)} + \cdots.
\end{aligned}$$

**说明。** 此连分数不是 q 连分数（与本章主题不同）；Berndt 注：它更宜归入 Part II Ch. 12，与 Ch. 12 Entry 40 同源。证明思路（自写）：由 Ch. 12 Entry 40（Watson 的连分数恒等式）直接推出，见 Berndt 的注记。拉马努金在笔记 p. 195 中亦给出其推导；其证明（Berndt 的证明，见书中）以 Ch. 12 Entry 40 为起点，代入 $\ell$、$m$、$n$、$x$ 的特定值并化简。

**状态：** 已证明（由 Ch. 12 Entry 40 推出；书中给出证明）。**对照：** M10（Gamma 函数）、M03（连分数）、M07。

## Entry 11

**陈述。** 若 $q$ 为实数、$|q| < 1$，$a$、$b$ 为复数且 $|ab| < 1$，则

$$\frac{(-a)_\infty(b)_\infty - (a)_\infty(-b)_\infty}{(-a)_\infty(b)_\infty + (a)_\infty(-b)_\infty} = \frac{a-b}{1-q} + \frac{(a-bq)(aq-b)}{1-q^3} + \frac{q(a-bq^2)(aq^2-b)}{1-q^5} + \cdots.$$

**说明。** 此为 Heine [1] 的连分数公式（邻近 ${}_2\phi_1$ 的比值连分数，书中 (11.1)(11.2)）。证明思路（自写）：由 (11.1) 的 Heine 连分数恒等式与 (11.2) 的恒等式推出；书中给出证明。Berndt 的注记：若 $a = bq^m$（$m$ 为整数），则连分数终止（见 Entry 12 的注）。

**状态：** 已证明（Heine 的经典结果）。**对照：** M03（Heine 连分数）、M07、M02。

## Entry 12

**陈述。** 设 $q$ 为实数、$|q| < 1$，$a$、$b$ 为复数且 $|ab| < 1$。则

$$\frac{(a^2q^3;q^4)_\infty(b^2q^3;q^4)_\infty}{(a^2q;q^4)_\infty(b^2q;q^4)_\infty} = \frac{1}{1-ab + \frac{(a-bq)(b-aq)}{(1-ab)(q^2+1) + \frac{(a-bq^3)(b-aq^3)}{(1-ab)(q^4+1) + \cdots}}}.$$

**读法注记（本文件所做之澄清）。** 原书 (12.1) 的排版把首项印作 $1/(1-ab)$ 后接连分数；按字面把首项读作 $1/(1-ab)$ 再加连分数则数值不符（取 $a = 0.3$、$b = 0.4$、$q = 0.5$，左端 $1.10979422566$，字面读法得 $1.1574315793$，差 $0.0476$；在 $(0.4,0.4,0.5)$、$(0.2,0.6,0.7)$、$(0.15,0.8,0.3)$ 三组参数下差亦为 $0.05$–$0.19$）。按上式读作“1 除以整个连分数”（即分母为 $(1-ab) + (a-bq)(b-aq)/((1-ab)(q^2+1) + \cdots)$），四组参数下左端与右端差皆 $\le 4\times 10^{-31}$（见“我自验”）。终止情形 $a = bq^3$（$m = 1$）下，左端 $1.07057024252$，1 除以整个连分数读法亦得 $1.07057024252$（差 0），字面读法得 $0.974489795918$。本文件按数值验证的读法写出上式，并将此排版歧义记入待核对清单（与他本的对照）。Göllnitz–Gordon 连分数为本条的特例（见 (12.6) 与 Entry 15 的注）。

**假设注记（疑似印文问题，待核对）。** 原书 (12.1) 的条件印作“$|ab| < 1$，或 $a = b^{2m+1}$（$m$ 为整数）”；300 DPI 放大图确认条件行确为 $a = b^{2m+1}$（$b$ 与上标 $2m+1$ 之间无 $q$）。但书中证明（pp. 24–25）三次写为 $a = bq^{2m+1}$：(12.1) 在 $a = bq^{2m+1}$ 时成立（(12.3) 由 $a^2q^3 = b^2q^{4m+5}$ 得来，需 $a = bq^{2m+1}$）；“当 $a = bq^{2m+1}$ 时，(12.1) 右端为终止连分数”；“已证 (12.1) 对集合 $\{a = bq^{2m+1}: 0 \le m < \infty\}$ 成立”。且 $a = bq^{2m+1}$ 时第 $m+1$ 项因子 $a - bq^{2m+1} = 0$，连分数终止；$a = b^{2m+1}$ 时无此终止性。综合判断：条件中的 $b^{2m+1}$ 很可能漏印了 $q$，应为 $a = bq^{2m+1}$；但因条件行经 300 DPI 确认为无 $q$ 的印文，本文件在此如实记下两种写法，列为待核对（疑似印文问题）。

**说明。** 引理 12.1：对任意 $a$ 与任意非负整数 $n$，$(a)_n = \sum_{k=0}^{n}(-1)^k(q^{n+1-k})_k/(q)_k \cdot q^{(k^2-k)/2}a^k$（(12.2)）。证明思路（自写）：由 (12.2) 与 (12.3) 得 (12.1) 在 $a = bq^{2m+1}$（$m \ge 0$）时成立；再用 Vitali 定理（Jacobsen 的证明，见书中）推广至 $|ab| < 1$ 的一般情形；$a = 0$ 时 (12.1) 化为 (12.6)，由 Entry 15（取 $a = -1$、$q \to q^2$、$b \to -b^2/q$）得证。$|ab| > 1$ 时 (12.1) 的右端连分数仍收敛，其值由 (12.1) 在 $|ab| < 1$ 时的值经解析延拓给出，见书末的注记（(12.7)）。

**状态：** 已证明（Jacobsen 的证明；见书中）。**对照：** M03（连分数）、M07、M02。

**我自验：** 按“1 除以整个连分数”读法：$(a,b,q) = (0.3,0.4,0.5)$ 时左端 $1.10979422566$、右端 $1.10979422566$，差 $5.9\times 10^{-31}$；$(0.4,0.4,0.5)$、$(0.2,0.6,0.7)$、$(0.15,0.8,0.3)$ 三组参数下差皆 $\le 4\times 10^{-31}$。终止情形 $a = bq^3$、$b = 0.4$、$q = 0.5$：左端 $1.07057024252$、右端 $1.07057024252$，差 0。

## Entry 13

**陈述。** 若 $a$ 为复数、$q$ 为实数、$|q| < 1$，则

$$\sum_{k=0}^{\infty}(-a)^kq^{k(k+1)/2} = \frac{1}{1 + \frac{aq}{1 + \frac{a(q^2-q)}{1 + \frac{aq^3}{1 + \frac{a(q^4-q^2)}{1 + \cdots}}}}} \tag{13.1}$$

（连分数第 $j$ 项的分子：$j$ 为奇数时为 $aq^j$，$j$ 为偶数时为 $a(q^j - q^{j/2})$；即 $j = 2$ 时为 $a(q^2-q)$，$j = 4$ 时为 $a(q^4-q^2)$，余类推）。

**读法注记。** 原书 (13.1) 的偶数项分子印作 $a(q^{2n} - q^n)$（$n = 1, 2, \dots$）；本文件按 300 DPI 放大图核对后写为上式（$j = 2n$ 时分子 $a(q^{2n} - q^n)$，与 $a(q^j - q^{j/2})$ 同一式子）。初版误把偶数项读作 $a(q^{2n} - q^{2n-1})$，数值不符；按上式重验后差 0（见“我自验”）。

**说明。** 此连分数属 Eisenstein [1]；拉马努金在笔记 p. 197 中亦有记录。证明思路（自写）：置 $f(b,a) = (aq)_\infty\sum_{k=0}^{\infty}b^kq^{k^2}/((aq)_k(q)_k)$（(13.2)）；由 (13.2) 得递推 (13.3)(13.4)：$f(b,a) = f(bq,a) + bq f(bq^2,aq)$ 与 $f(b,a) = f(b,a/q) - bq f(bq^2,aq)$；两式相减得 (13.5)，再由 (13.5) 与 (13.2) 推出 (13.1) 的分母 $D_{2n}$、$D_{2n+1}$ 的显式公式 (13.6)(13.7)，其中 $D_{2n} = (aq^{2n})_\infty \sum_{k=0}^{\infty}(-a)^kq^{k^2+2nk}/((q)_k(aq^{2n})_k)$，$D_{2n+1} = (aq^{2n+1})_\infty\sum_{k=0}^{\infty}(-a)^kq^{k^2+2nk+k}/((q)_k(aq^{2n+1})_k)$。

**状态：** 已证明（Eisenstein 的经典结果；书中给出证明）。**对照：** M03（Eisenstein 连分数）、M07、M02。

**我自验：** 取 $a = 0.7$、$q = 0.5$：左端 $0.70612002436$、右端 $0.70612002436$，差 0；取 $a = 0.4$、$q = 0.6$：差 $9.9\times 10^{-32}$。

## Entry 14

**陈述。** 设 $n < 1$、$0 < a < q^{1-n}$，$q$ 为实数、$0 < q < 1$。则

$$\int_0^\infty \frac{(-at)_\infty}{t^n(-t)_\infty}\,dt = \frac{\pi}{\sin \pi n}\cdot\frac{(a)_\infty(q^n)_\infty}{(q)_\infty(aq^{n-1})_\infty}. \tag{14.1}$$

**说明。** 此为 beta 函数的 q 类比（拉马努金原创名 theorem 之一）。以 q-Gamma 函数 (1.1) 改写，(14.1) 可写为

$$\int_0^\infty t^{\alpha-1}\frac{(-tq^{\alpha+\beta})_\infty}{(-t)_\infty}\,dt = \frac{\Gamma(\alpha)\Gamma(1-\alpha)\Gamma_q(\beta)}{\Gamma_q(1-\alpha)\Gamma_q(\alpha+\beta)}. \tag{14.2}$$

Berndt 注：拉马努金在论文 [4]（[10, p. 57]）中给出 (14.1) 的表述，但未给出严格证明（Hardy 在 [3, p. 227] 中指出其证明不严格）；Askey [1] 给出一个简单证明，见书中；另有至少四种不同验证（见书中注记）。积分 (14.1) 的左端在 $n < 1$ 时收敛；右端的 $(q^n)_\infty$ 在 $n < 1$ 时有意义。

**状态：** 已证明（Askey 的简单证明；拉马努金的原证明不严格，见 Hardy [3] 的注记）。**对照：** M10（q-beta 积分、q-Gamma 函数）、M07。

**我自验：** 取 $n = 1/2$、$a = 0.3$、$q = 0.5$：左端（数值积分）$1.98045687184$、右端 $1.98045687184$，差 $1.4\times 10^{-17}$（此差为 mpmath `quad` 数值积分的容差，非公式误差；见待核对清单注）。

## Entry 15

**陈述。** 若 $a \ne 0$、$|q| < 1$，则

$$\frac{\sum_{k=0}^{\infty}b^kq^{k^2}/((aq)_k(q)_k)}{\sum_{k=0}^{\infty}b^kq^{k(k+1)}/((aq)_k(q)_k)} = 1 + \frac{bq}{1-aq} + \frac{bq^2}{1-aq^2} + \frac{bq^3}{1-aq^3} + \cdots.$$

**说明。** 证明思路（自写）：由 Entry 13 的 (13.2)–(13.5) 推出；书中给出证明。拉马努金在致 Hardy 的第二封信中提及本条（见 Hardy [3, p. 226]）。

**推论。** 取 $a = 0$，得

$$\frac{\sum_{k=0}^{\infty}a^kq^{k(k+1)}/(q)_k}{\sum_{k=0}^{\infty}a^kq^{k^2}/(q)_k} = \frac{1}{1 + \frac{aq}{1 + \frac{aq^2}{1 + \frac{aq^3}{1 + \cdots}}}}.$$

$a = 1$ 时即 Entry 38(iii) 的 Rogers–Ramanujan 连分数。

**状态：** 已证明（书中给出证明）。**对照：** M03（连分数）、M07、M02。

**我自验：** 取 $q = 0.5$、$a = 0.4$、$b = 0.3$：左端 $1.17047432158$、右端 $1.17047432158$，差 $3.9\times 10^{-31}$。推论（$a = 0$ 的情形）未逐项数值复核（见待核对清单）。

## Entry 16

**陈述。** 设 $n$ 为正整数，$a$ 为复数，$q$ 为实数、$|q| < 1$。置

$$\mu = \mu_n(a,q) = \sum_{k=0}^{[(n+1)/2]}\frac{a^kq^{k^2}(q)_{n-k+1}}{(q)_k(q)_{n-2k+1}}, \qquad \nu = \nu_n(a,q) = \sum_{k=0}^{[n/2]}\frac{a^kq^{k(k+1)}(q)_{n-k}}{(q)_k(q)_{n-2k}}.$$

则

$$\frac{\mu}{\nu} = 1 + \frac{aq}{1 + \frac{aq^2}{1 + \cdots + \frac{aq^n}{1}}}.$$

**说明。** 此为 Entry 15 推论的有限形式（Rogers–Ramanujan 连分数的有限版）。证明思路（自写）：由 Entry 15 的证明中 (13.6)(13.7) 的有限和版本推出；书中给出证明。Berndt 注：Hirschhorn [1] 于 1972 年首次在印刷品中证明本条，当时不知道结果已在拉马努金的笔记中。

**状态：** 已证明（书中给出证明；Hirschhorn 1972 年首次在印刷品中证明）。**对照：** M03（有限连分数）、M07、M02。

**我自验：** 取 $n = 3$、$a = 0.4$、$q = 0.5$：左端 $1.18260869565$、右端 $1.18260869565$，差 $2.0\times 10^{-31}$。

## Entry 17

**陈述。** 设 $\alpha$、$\beta$、$z$ 为复数，$q$ 为实数、$0 < q < 1$，且 $|\beta q| < |z| < 1/|\alpha q|$。则

$$\begin{aligned}
&1 + \sum_{k=1}^{\infty}\frac{(1/\alpha;q^2)_k}{( \beta q^2;q^2)_k}(-\alpha q)^kz^k + \sum_{k=1}^{\infty}\frac{(1/\beta;q^2)_k}{(\alpha q^2;q^2)_k}(-\beta q)^kz^{-k} \\
&\qquad = \frac{(-qz;q^2)_\infty(-q/z;q^2)_\infty}{(-\alpha qz;q^2)_\infty(-\beta q/z;q^2)_\infty}\cdot\frac{(q^2;q^2)_\infty(\alpha\beta q^2;q^2)_\infty}{(\alpha q^2;q^2)_\infty(\beta q^2;q^2)_\infty}. \tag{17.1}
\end{aligned}$$

**说明。** 此为拉马努金的 ${}_1\psi_1$ 求和（拉马努金原创名 theorem 之一）。Berndt 注：(17.1) 的第一个发表证明由 Hahn [1]（1949 年）与 Jackson [1]（1950 年）给出；拉马努金在笔记中给出本条的证明（书中给出）。本条是普通超几何级数 ${}_1F_0$ 求和公式的双边 q 类比。

**推论。** 取 $\alpha = \beta = n$（$n$ 为正整数），得 (17.1) 的特例（书中 (17.2)–(17.5)）。

**改写 (17.6)。** (17.1) 可改写为标准的 ${}_1\psi_1$ 形式：若 $|b/a| < |z| < 1$，则

$$\sum_{k=-\infty}^{\infty}\frac{(a)_k}{(b)_k}z^k = \frac{(az)_\infty(q/az)_\infty(q)_\infty(b/a)_\infty}{(z)_\infty(b/az)_\infty(b)_\infty(q/a)_\infty}. \tag{17.6}$$

**状态：** 已证明（Hahn 1949 年、Jackson 1950 年首次在印刷品中证明；拉马努金的证明见书中）。**对照：** M07（${}_1\psi_1$ 求和）、M02。

**我自验：** (17.1) 取 $\alpha = 0.3$、$\beta = 0.2$、$z = 0.7$、$q = 0.5$：左端 $1.89195418266$、右端 $1.89195418266$，差 $2.0\times 10^{-31}$。(17.6) 取 $a = 0.3$、$b = 0.2$、$z = 0.7$、$q = 0.5$：双边和在负向需取 $k \ge -1500$（负向项以比值 $b/(az) = 0.952$ 缓慢衰减，截断于 $k = -60$ 时差达 $1.8$，属自验方法错误），补足负向项与解析尾项后左端 $-29.2068867642$、右端 $-29.2068867633$，差 $9.3\times 10^{-10}$（余差为正向截断于 $k = 60$ 的尾项 $\sim 0.7^{60} \approx 5\times 10^{-10}$，非公式误差）。

## Entry 18

**陈述。** 设 $f(a,b)$ 如 (18.1) 所定义，$|ab| < 1$，$n$ 为整数。则

$$\begin{aligned}
\text{(i)}\quad f(a,b) &= f(b,a), \\
\text{(ii)}\quad f(1,a) &= 2f(a,a^3), \\
\text{(iii)}\quad f(-1,a) &= 0, \\
\text{(iv)}\quad f(a,b) &= a^{n(n+1)/2}b^{n(n-1)/2}f(a(ab)^n, b(ab)^{-n}).
\end{aligned}$$

**说明。** (i) 由定义直接得；(ii) 由 (i) 与 $f(1,a) = f(a,1)$ 的级数展开得；(iii) 由 (i) 与 $f(-1,a) = -f(-1,a)$ 得；(iv) 由 (18.1) 的双边级数平移指标 $k \mapsto k+n$ 得。Berndt 注：拉马努金在笔记 p. 197 中说 (iv) 对非整数 $n$“近似成立”；Berndt 未能把这一说法表述精确（见书中注记）。

**状态：** 已证明（(i)–(iv) 对整数 $n$；(iv) 对非整数 $n$ 的表述未精确化，见待核对清单）。**对照：** M07（theta 函数）、M06。

## Entry 19

**陈述。** 若 $|ab| < 1$，则

$$f(a,b) = (-a;ab)_\infty(-b;ab)_\infty(ab;ab)_\infty.$$

**说明。** 此为 Jacobi 三重积恒等式。证明思路（自写）：由 Entry 17（取 $\alpha = \beta = 0$）推出；书中给出证明。Berndt 注：拉马努金在笔记 p. 197 中写道：“$f(a,b) = (-a;ab)_\infty(-b;ab)_\infty(ab;ab)_\infty$。此恒等式是 Jacobi 的。”拉马努金在笔记中给出本条的证明（见书中）。

**状态：** 已证明（由 Entry 17 推出；拉马努金的证明见书中）。**对照：** M07（Jacobi 三重积）、M06。

**我自验：** 取 $q = 0.5$、$a = 0.3$、$b = 0.2$：左端 $1.50780756045$、右端 $1.50780756045$，差 $2.0\times 10^{-31}$。

## Entry 20

**陈述。** 设 $\alpha$、$\beta$ 为正实数，$\alpha\beta = \pi$，$\mathrm{Re}\,\alpha^2 > 0$；$n$ 为任意复数。则

$$\sqrt{\alpha}\,f(e^{-\alpha^2+n\alpha}, e^{-\alpha^2-n\alpha}) = e^{n^2/4}\sqrt{\beta}\,f(e^{-\beta^2+in\beta}, e^{-\beta^2-in\beta}).$$

**说明。** 此为 theta 函数的经典变换公式（Jacobi 变换公式的特例）。Berndt 注：本条在 Ch. 14 中亦有记录（Part II，Vol. 2，p. 169，Entry 7）；证明见书中（由 Entry 19 的三重积与 Poisson 求和公式推出）。

**状态：** 已证明（书中给出证明）。**对照：** M06（theta 变换）、M07、M11。

**我自验：** 取 $\alpha = \beta = \sqrt{\pi}$、$n = 1$：左端 $1.6798649776$、右端 $1.6798649776 - 1.5\times 10^{-33}i$，差 $1.5\times 10^{-33}$（复数直接求和，30 位）。

## Entry 21

**陈述。** 若 $|a| < 1$、$|ab| < 1$，则

$$\mathrm{Log}(-a;q)_\infty = \sum_{k=1}^{\infty}\frac{(-1)^{k-1}a^k}{k(1-q^k)}, \tag{21.1}$$

$$\mathrm{Log}\,f(a,b) = \mathrm{Log}(ab;ab)_\infty + \sum_{k=1}^{\infty}\frac{(-1)^{k-1}(a^k+b^k)}{k(1-a^kb^k)}. \tag{21.2}$$

**说明。** (21.1) 由 $\mathrm{Log}(1-x) = -\sum_{k=1}^{\infty}x^k/k$（$|x| < 1$）逐项展开并交换求和次序得；(21.2) 由 (21.1) 与 Entry 19 的三重积得。$\mathrm{Log}$ 均取主支。

**状态：** 已证明（初等展开）。**对照：** M07、M02。

## Entry 22

**陈述。** 若 $|q| < 1$，则

$$\begin{aligned}
\text{(i)}\quad \varphi(q) = f(q,q) &= 1 + 2\sum_{k=1}^{\infty}q^{k^2} = \frac{(-q;q^2)_\infty(q^2;q^2)_\infty}{(q;q^2)_\infty(-q^2;q^2)_\infty}, \\
\text{(ii)}\quad \psi(q) = f(q,q^3) &= \sum_{k=0}^{\infty}q^{k(k+1)/2} = \frac{(q^2;q^2)_\infty}{(q;q^2)_\infty}, \\
\text{(iii)}\quad f(-q) = f(-q,-q^2) &= \sum_{k=0}^{\infty}(-1)^kq^{k(3k-1)/2} + \sum_{k=1}^{\infty}(-1)^kq^{k(3k+1)/2} = (q;q)_\infty, \\
\text{(iv)}\quad \chi(q) &:= (-q;q^2)_\infty \quad\text{（定义）}.
\end{aligned}$$

**说明。** (i) 由 Entry 19（取 $a = b = q$）与 (22.2) 的 Euler 恒等式 $(-q;q^2)_\infty(q^2;q^2)_\infty = (q;q^2)_\infty(-q^2;q^2)_\infty \cdot \varphi(q)$ 得；(ii) 由 Entry 19（取 $a = q$、$b = q^3$）与 (22.3) 的恒等式 $(-q;q)_\infty = 1/(q;q^2)_\infty$ 得；(iii) 由 Entry 19（取 $a = -q$、$b = -q^2$）得 Euler 五边形数定理；(iv) 为 $\chi(q)$ 的定义（拉马努金记 $\chi(q)$ 为 $\eta(q)$ 的某种形式）。另有 (22.4)：$\varphi(-q) = (q;q)_\infty(q;q^2)_\infty/(-q;q)_\infty$。

**状态：** 已证明（由 Entry 19 推出）。**对照：** M06（$\varphi$、$\psi$、$\chi$）、M07、M05（(iii) 的 Euler 五边形数定理）。

**我自验：** 取 $q = 0.5$：(i) 左端 $2.12893682721$、右端 $2.12893682721$，差 $3.9\times 10^{-31}$；(ii) 左端 $1.64163256066$、右端 $1.64163256066$，差 $3.9\times 10^{-31}$；(iii) 左端 $0.288788095087$、右端 $0.288788095087$，差 $4.9\times 10^{-32}$；(iv) 为定义，无需复核。

## Entry 23

**陈述。** 若 $|q| < 1$，则

$$\begin{aligned}
\text{(i)}\quad \mathrm{Log}\,\varphi(q) &= 2\sum_{k=1}^{\infty}\frac{q^{2k-1}}{(2k-1)(1+q^{2k-1})}, \\
\text{(ii)}\quad \mathrm{Log}\,\psi(q) &= \sum_{k=1}^{\infty}\frac{q^k}{k(1+q^k)}, \\
\text{(iii)}\quad \mathrm{Log}\,f(-q) &= -\sum_{k=1}^{\infty}\frac{q^k}{k(1-q^k)}, \\
\text{(iv)}\quad \mathrm{Log}\,\chi(q) &= \sum_{k=1}^{\infty}\frac{(-1)^{k-1}q^k}{k(1-q^{2k})}, \\
\text{(v)}\quad \frac{\psi(q)}{\varphi(q)} &= \frac{(-q^2;q^2)_\infty}{(-q;q^2)_\infty}.
\end{aligned}$$

**说明。** (i)–(iv) 由 Entry 21 的 (21.1)(21.2) 与 Entry 22 的 (i)–(iv) 推出；(v) 由 Entry 22(i)(ii) 的乘积表示相除得。

**例。** 取 $q = 1/10$，由 Entry 22(ii) 得

$$\frac{11}{10}\cdot\frac{1111}{1110}\cdot\frac{111111}{111110}\cdots = 1.1010010000100001\cdots,$$

即 $\psi(1/10)$ 的十进制展开中 1 的位置恰为三角数 $k(k+1)/2$（$k = 0, 1, 2, \dots$）。

**状态：** 已证明（由 Entry 21 与 Entry 22 推出）。**对照：** M06、M07、M01。

## Entry 24

**陈述。** 若 $|q| < 1$，则

$$\begin{aligned}
\text{(i)}\quad \frac{f(q)}{f(-q)} = \frac{\psi(q)}{\psi(-q)} = \frac{\chi(q)}{\chi(-q)} &= \sqrt{\frac{\varphi(q)}{\varphi(-q)}}, \\
\text{(ii)}\quad f^3(-q) &= \varphi^2(-q)\psi(q) = \sum_{k=0}^{\infty}(-1)^k(2k+1)q^{k(k+1)/2}, \\
\text{(iii)}\quad \chi(q) = \frac{f(q)}{f(-q^2)} = \sqrt[3]{\frac{\varphi(q)}{\psi(-q)}} = \frac{\varphi(q)}{f(q)} &= \frac{f(-q^2)}{\psi(-q)}, \\
\text{(iv)}\quad f^3(-q^2) = \varphi(-q)\psi^2(q) \quad\text{与}\quad \chi(q)\chi(-q) &= \chi(-q^2).
\end{aligned}$$

**注记（本文件所做之澄清）：$f(q)$ 的含义。** 书中在 Entry 24(i)(iii) 与 Entry 38、Entry 39 中使用单变量记号 $f(q)$，但未在本章定义它。经数值核对（mpmath 30 位，$q = 0.5$），$f(q)$ 应指 $f(q,-q^2)$，即

$$f(q) = f(q,-q^2) = (-q;q^2)_\infty(q^2;q^2)_\infty = \sum_{k=-\infty}^{\infty}(-1)^{k(k-1)/2}q^{k(3k-1)/2} = 1.21072413030105918013617285611.$$

证据：(a) $f(q,-q^2) = 1.21072413030105918013617285611$ 与 $\varphi(q)/\chi(q)$ 精确相等；(b) Entry 24(i) 的 $f(q)/f(-q) = 4.19243088929266462344639696087$ 等于 $(-q;q^2)_\infty/(q;q^2)_\infty$（即 $\psi(q)/\psi(-q)$ 与 $\chi(q)/\chi(-q)$ 的值）；(c) Entry 24(iii) 的 $f(q)/f(-q^2) = \chi(q)$ 精确成立（差 0）；(d) 另一候选 $f(q,q^2) = 1.78933741155287907159762028642$ 与上述三式皆不符。另经核对，$f(-q^5) = f(-q^5,-q^{10}) = (q^5;q^5)_\infty = 0.967773467331426217284657995845$（$q = 0.5$），与 Entry 38(i) 的用法一致。本文件以下凡写 $f(q)$ 皆指 $f(q,-q^2)$。

**说明。** (i) 由 Entry 22(i)–(iv) 的乘积表示直接推出；(ii) 由 Entry 22(i)(ii) 与 (i) 推出，右端级数即 $\sum_{k=0}^{\infty}(-1)^k(2k+1)q^{k(k+1)/2}$（Jacobi 的恒等式）；(iii) 由 (i)(ii) 推出；(iv) 由 (i)–(iii) 推出。

**状态：** 已证明（由 Entry 22 推出）。**对照：** M06（$\varphi$、$\psi$、$\chi$ 的比值）、M07。

**我自验：** 取 $q = 0.5$：(i) 四个比值皆为 $4.19243088929266462344639696087$，差 $\le 7.9\times 10^{-31}$；(ii) 左端 $0.0240845123912$、右端 $0.0240845123912$，差 $1.2\times 10^{-32}$；(iii) $f(q)/f(-q^2) = \chi(q)$，差 0；(iv) 未逐项数值复核（见待核对清单）。

## Entry 25

**陈述。** 若 $|q| < 1$，则

$$\begin{aligned}
\text{(i)}\quad \varphi(q) + \varphi(-q) &= 2\varphi(q^4), \\
\text{(ii)}\quad \varphi(q) - \varphi(-q) &= 4q\psi(q^8), \\
\text{(iii)}\quad \varphi(q)\varphi(-q) = \varphi^2(-q^2), \qquad \psi(q)\psi(-q) &= \psi(q^2)\varphi(-q^2), \\
\text{(iv)}\quad \varphi(q)\psi(q^2) &= \psi^2(q), \\
\text{(v)}\quad \varphi^2(q) - \varphi^2(-q) &= 8q\psi^2(q^4), \\
\text{(vi)}\quad \varphi^2(q) + \varphi^2(-q) &= 2\varphi^2(q^2), \\
\text{(vii)}\quad \varphi^4(q) - \varphi^4(-q) &= 16q\psi^4(q^2).
\end{aligned}$$

**说明。** (i)(ii) 由 $\varphi(q) = 1 + 2\sum_{k=1}^{\infty}q^{k^2}$ 的级数定义直接得；(iii) 由 Entry 22(i)(ii) 的乘积表示得；(iv) 由 (iii) 与 Entry 24(ii) 得；(v)–(vii) 由 (i)–(iv) 推出。

**状态：** 已证明（初等恒等式）。**对照：** M06（$\varphi$、$\psi$ 的恒等式）、M07。

**我自验：** 取 $q = 0.5$：(i) 左端 $2.25006103521$、右端 $2.25006103521$，差 0；(ii) 左端 $2.00781261921$、右端 $2.00781261921$，差 0；(v) 左端 $4.51770094049$、右端 $4.51770094049$，差 0；(iii)(iv)(vi)(vii) 未逐项数值复核（见待核对清单）。

## Entry 26

**陈述。** 设 $m$、$n$ 为正实数，$q$ 为实数、$|q| < 1$。置

$$G(q) = q^{(m-n)^2/8(m+n)}f(q^m,q^n).$$

则 $G(q)$ 为“$\frac12$ 度的完全纯双重级数”（a perfect, complete, pure, double series of $\frac12$ a degree）。

**推论 (i)。** $\varphi(q)$、$\sqrt[8]{q}\,\psi(q)$、$\sqrt[24]{q}\,f(q)$ 皆为 $\frac12$ 度的完全级数。

**推论 (ii)。** $\chi(q)/\sqrt[24]{q}$ 为 0 度的完全级数。

**说明。** “度”、“完全”、“纯”、“双重级数”的定义见 Part II Ch. 15 第 10 节（Part II，Vol. 2，pp. 320–321；拉马努金在笔记 pp. 186–187 中定义“度”）。Berndt 注：拉马努金在笔记 [9, Vol. 2, p. 198] 中写道：“$G(q)$ 为 $\frac12$ 度的完全纯双重级数。”本条的证明见书中（由 Entry 18(iv) 与 Entry 19 推出）。Ismail [1] 指出，“度”的定义与级数的奇点阶有关；Entry 26 的“度”与 Ch. 15 Entry 10(ii) 的“度”定义之间的关系见书中注记（Ch. 15 待核对清单第 14 项亦有记录）。

**状态：** 已证明（书中给出证明；“度”的定义见 Ch. 15 第 10 节，Ismail 的奇点阶解释见书中注记）。**对照：** M06（级数的度）、M12（Euler–Maclaurin 求和公式）、M01。

## Entry 27

**陈述。** 设 $\alpha$、$\beta$ 为正实数。

$$\begin{aligned}
\text{(i)}\quad \text{若 }\alpha\beta = \pi\text{，则}\quad \sqrt{\alpha}\,\varphi(e^{-\alpha^2}) &= \sqrt{\beta}\,\varphi(e^{-\beta^2}), \\
\text{(ii)}\quad \text{若 }\alpha\beta = \pi\text{，则}\quad 2\sqrt{\alpha}\,\psi(e^{-2\alpha^2}) &= \sqrt{\beta}\,e^{\alpha^2/4}\varphi(-e^{-\beta^2}), \\
\text{(iii)}\quad \text{若 }\alpha\beta = \pi^2\text{，则}\quad e^{-\alpha/12}\sqrt[4]{\alpha}\,f(-e^{-2\alpha}) &= e^{-\beta/12}\sqrt[4]{\beta}\,f(-e^{-2\beta}), \\
\text{(iv)}\quad \text{若 }\alpha\beta = \pi^2\text{，则}\quad e^{-\alpha/24}\sqrt[4]{\alpha}\,f(e^{-\alpha}) &= e^{-\beta/24}\sqrt[4]{\beta}\,f(e^{-\beta}), \\
\text{(v)}\quad \text{若 }\alpha\beta = \pi^2\text{，则}\quad e^{\alpha/24}\chi(e^{-\alpha}) &= e^{\beta/24}\chi(e^{-\beta}).
\end{aligned}$$

**说明。** (i) 为 $\vartheta_3(0,\tau)$ 的模变换公式；(ii) 由 (i) 与 Entry 25(ii) 推出；(iii) 为 Dedekind $\eta$ 函数的模变换公式（因 $f(-q) = (q;q)_\infty$，(iii) 即 $\eta(\tau)$ 的变换）；(iv) 由 (iii) 与 Entry 24(ii) 推出；(v) 由 (iii)(iv) 推出。Berndt 注：本条只给出模变换 $\tau \mapsto -1/\tau$ 的公式，拉马努金未发现更一般的变换公式。

**状态：** 已证明（书中给出证明）。**对照：** M06（模变换）、M11（$\vartheta_3$ 与 $\eta$ 函数）、M04。

**我自验：** (i) 取 $\alpha = \beta = \sqrt{\pi}$：左端 $1.44640908463$、右端 $1.44640908463$，差 0；(ii)–(v) 未逐项数值复核（见待核对清单）。

## Entry 28

**陈述。** 设 $a$、$b$ 为复数，$|ab| < 1$；$p = ab$；$n$ 为自然数。则

$$\prod_{k=1}^{n}f(ap^{k-1}, bp^{n-k}) = f(a,b)\frac{f^n(-p^n)}{f(-p)}.$$

**推论。** 取 $a = -q$、$b = -q^{2n}$（$n$ 为自然数），得

$$\prod_{k=1}^{n}f(-q^k, -q^{2n+1-k}) = f(-q)f^{n-1}(-q^{2n+1}). \tag{28.1}$$

特别地，$f(-q^2,-q^3)f(-q,-q^4) = f(-q)f(-q^5)$；$f(-q,-q^6)f(-q^2,-q^5)f(-q^3,-q^4) = f(-q)f^2(-q^7)$。

**说明。** 证明思路（自写）：由 Entry 19 的三重积与 Entry 18(iv) 推出；书中给出证明。Berndt 注：拉马努金在笔记 [9, Vol. 2, p. 199] 中写道：“and so on.”（依此类推）。

**状态：** 已证明（书中给出证明）。**对照：** M07（theta 函数的乘积恒等式）、M06。

## Entry 29

**陈述。** 若 $ab = cd$，$|ab| < 1$，则

$$\begin{aligned}
\text{(i)}\quad f(a,b)f(c,d) + f(-a,-b)f(-c,-d) &= 2f(ac,bd)f(ad,bc), \\
\text{(ii)}\quad f(a,b)f(c,d) - f(-a,-b)f(-c,-d) &= 2af(b/c, c/b\cdot abcd)f(b/d, d/b\cdot abcd).
\end{aligned}$$

**说明。** (i) 由 Entry 19 的三重积与 (29.1) 的恒等式推出；(ii) 由 (i) 与 Entry 18(iv) 推出。Berndt 注：(ii) 为 Hardy [3, p. 223] 讨论过的恒等式。

**状态：** 已证明（书中给出证明）。**对照：** M07（theta 函数的加法公式）、M06。

**我自验：** (i) 取 $q = 0.5$、$a = 0.3$、$b = 0.2$、$c = 0.4$、$d = 0.15$（$ab = cd = 0.06$）：左端 $2.58769369259$、右端 $2.58769369259$，差 $1.2\times 10^{-30}$；(ii) 未逐项数值复核（见待核对清单）。

## Entry 30

**陈述。** 若 $|ab| < 1$，则

$$\begin{aligned}
\text{(i)}\quad f(a,ab^2)f(b,a^2b) &= f(a,b)\psi(ab), \\
\text{(ii)}\quad f(a,b) + f(-a,-b) &= 2f(a^3b, ab^3), \\
\text{(iii)}\quad f(a,b) - f(-a,-b) &= 2af(b/a, a/b\cdot a^4b^4), \\
\text{(iv)}\quad f(a,b)f(-a,-b) &= f(-a^2,-b^2)\varphi(-ab), \\
\text{(v)}\quad f^2(a,b) + f^2(-a,-b) &= 2f(a^2,b^2)\varphi(ab), \\
\text{(vi)}\quad f^2(a,b) - f^2(-a,-b) &= 4af(b/a, a/b\cdot a^2b^2)\psi(a^2b^2).
\end{aligned}$$

**说明。** (i) 由 Entry 19 的三重积与 Entry 22(ii) 推出；(ii)(iii) 由 Entry 18(iv)（取 $n = 1$）推出；(iv) 由 Entry 19 与 Entry 22(i) 推出；(v)(vi) 由 (ii)(iii) 平方相加减推出。

**状态：** 已证明（书中给出证明）。**对照：** M07、M06。

**我自验：** (i) 取 $q = 0.5$、$a = 0.3$、$b = 0.2$：左端 $1.59860177086$、右端 $1.59860177086$，差 $2.0\times 10^{-31}$；(ii)–(vi) 未逐项数值复核（见待核对清单）。

## Entry 31

**陈述。** 设 $a$、$b$ 为复数，$|ab| < 1$；$n$ 为正整数。置 $U_n = a^{n(n+1)/2}b^{n(n-1)/2}$、$V_n = a^{n(n-1)/2}b^{n(n+1)/2}$。则

$$f(U_1,V_1) = \sum_{r=0}^{n-1}U_r\,f(U_{n+r}/U_r, V_{n-r}/U_r). \tag{31.1}$$

拉马努金的形式为

$$f(U_1,V_1) = f(U_n,V_n) + U_1f\left(\frac{V_{n-1}}{U_1}, \frac{U_{n+1}}{U_1}\right) + V_1f\left(\frac{U_{n-1}}{V_1}, \frac{V_{n+1}}{V_1}\right) + U_2f\left(\frac{V_{n-2}}{U_2}, \frac{U_{n+2}}{U_2}\right) + V_2f\left(\frac{U_{n-2}}{V_2}, \frac{V_{n+2}}{V_2}\right) + \cdots, \tag{31.2}$$

其中右端之和显然含 $n$ 项。由 Entry 18(iv)，对 $r \ge 1$，

$$V_rf\left(\frac{U_{n-r}}{V_r}, \frac{V_{n+r}}{V_r}\right) = U_{n-r}f\left(\frac{U_{n-r}^2V_{n+r}}{V_r^3}, \frac{V_r}{U_{n-r}}\right) = U_{n-r}f\left(\frac{U_{2n-r}}{U_{n-r}}, \frac{V_r}{U_{n-r}}\right). \tag{31.3}$$

(31.3) 表明 (31.1) 与 (31.2) 的右端之和相等。

**推论 (i)。** 取 $a = b = q$，得

$$\varphi(q) = \varphi(q^9) + 2qf(q^3,q^{15}) = \varphi(q^{25}) + 2qf(q^{15},q^{35}) + 2q^4f(q^5,q^{45}).$$

**推论 (ii)。** 取 $a = q$、$b = q^3$，得

$$\begin{aligned}
\psi(q) &= f(q^3,q^6) + q\psi(q^9) = f(q^6,q^{10}) + qf(q^2,q^{14}) \\
&= f(q^{10},q^{15}) + qf(q^5,q^{20}) + q^3\psi(q^{25}) = f(q^{15},q^{21}) + q\psi(q^9) + q^3f(q^3,q^{33}).
\end{aligned}$$

一般公式：

$$\varphi(q) = \varphi(q^{n^2}) + \sum_{r=1}^{n-1}q^{r^2}f(q^{n(n-2r)}, q^{n(n+2r)}),$$

$$\psi(q) = \frac12\sum_{r=0}^{n-1}q^{r(r-1)/2}f(q^{n(n-2r+1)/2}, q^{n(n+2r-1)/2}) = \sum_{r=0}^{n-1}q^{r(2r-1)}f(q^{n(2n-4r+1)}, q^{n(2n+4r-1)}).$$

**例 (i)。** 设 $q$、$r$、$s$ 为复数，$|q|, |r|, |s| < 1$，则

$$\frac{\varphi^2(q)}{\varphi^2(-q)} + \frac{\varphi^2(r)}{\varphi^2(-r)} + \frac{\varphi^2(s)}{\varphi^2(-s)} + \frac{\varphi^2(q)\varphi^2(r)\varphi^2(s)}{\varphi^2(-q)\varphi^2(-r)\varphi^2(-s)} = 4\frac{\varphi^2(q^2)\varphi^2(r^2)\varphi^2(s^2)}{\varphi^2(-q)\varphi^2(-r)\varphi^2(-s)} + 256qrs\frac{\psi^2(q^4)\psi^2(r^4)\psi^2(s^4)}{\varphi^2(-q)\varphi^2(-r)\varphi^2(-s)}. \tag{31.4}$$

**例 (ii)。**

$$\frac{1}{\varphi(q^4)} = \frac{1}{\varphi(q) \pm \varphi(q^2)} + \frac{1}{\varphi(-q) \pm \varphi(q^2)}, \tag{31.5}$$

$$\frac{1}{\varphi(-q^2)} = \frac{1}{\varphi(-q^2) \pm \varphi(q)} + \frac{1}{\varphi(-q^2) \pm \varphi(-q)}. \tag{31.6}$$

**例 (iii)。** 对每个自然数 $n$，$[q/(1-q)]\psi(q^2)$ 的展开式中 $q^n$ 的系数为最接近 $\sqrt{n}$ 的整数。

**例 (iv)。**

$$\varphi(-q) + \varphi(q^2) = \frac{2f^2(q^3,q^5)}{\psi(q)}, \qquad \varphi(-q) - \varphi(q^2) = -\frac{2qf^2(q,q^7)}{\psi(q)}.$$

**例 (v)。** $f(q,q^5) = \psi(-q^3)\chi(q)$。

**说明。** (31.1) 的证明见书中（由 Entry 18(iv) 与 (18.1) 的双边级数重排推出）；推论 (i)(ii) 由 (31.1) 取 $a = b = q$ 与 $a = q$、$b = q^3$ 推出；例 (i) 由 Entry 25(vi)(v) 推出；例 (ii) 由 (31.7)–(31.9) 的初等恒等式与 Entry 25(i)(iii)(vi) 推出；例 (iii) 由 $\psi(q^2) = \sum_{k=0}^{\infty}q^{k(k+1)}$ 与 $[q/(1-q)]$ 的展开推出；例 (iv)(v) 由 (31.1) 的特例推出。

**状态：** 已证明（书中给出证明）。**对照：** M07（theta 函数的 $n$ 项展开）、M06、M05（例 (iii) 的最近整数）。

**我自验：** 取 $q = 0.5$、$a = 0.3$、$b = 0.2$、$n = 3$：(31.1) 左端 $1.50780756045$、右端 $1.50780756045$，差 $1.97\times 10^{-31}$；(31.2)（3 项）差 $1.97\times 10^{-31}$；(31.3)（$r = 1$）左端 $0.205400000075$、右端 $0.205400000075$，差 $2.5\times 10^{-32}$。推论 (i)(ii) 与例 (i)–(v) 未逐项数值复核（见待核对清单）。

## Entry 32

**陈述。** 若 $|q| < 1$，则

$$\begin{aligned}
\text{(i)}\quad \frac{\varphi'(q)}{\varphi(q)} - \frac{\psi'(q)}{\psi(q)} &= \frac{1-\varphi^4(-q)}{8q}, \\
\text{(ii)}\quad \frac{\psi'(q)}{\psi(q)} - \frac{2q\psi'(q^2)}{\psi(q^2)} &= \frac{1-\varphi^4(-q)}{8q}, \\
\text{(iii)}\quad \frac{\varphi'(q)}{\varphi(q)} + \frac{\varphi'(-q)}{\varphi(-q)} &= \frac{\varphi^4(q)-\varphi^4(-q)}{4q}, \\
\text{(iv)}\quad \frac{\varphi'(q)}{\varphi(q)} - \frac{\varphi'(-q)}{\varphi(-q)} &= -4q\frac{\varphi'(-q^2)}{\varphi(-q^2)}.
\end{aligned}$$

**说明。** 证明思路（自写）：由 Entry 33 的 (33.5)（Jacobi 的恒等式 $\varphi^4(-q^2) = 1 + 8\sum_{k=1}^{\infty}(-1)^kq^{2k}/(1+q^{2k})^2$）与 Entry 22 的乘积表示对数求导推出；书中给出证明。

**状态：** 已证明（书中给出证明）。**对照：** M06（$\varphi$、$\psi$ 的对数导数）、M07、M11。

**我自验：** (i) 取 $q = 0.5$（mpmath 数值微分，30 位）：左端 $0.249946189899$、右端 $0.249946189899$，差 $7.4\times 10^{-32}$；(ii)–(iv) 未逐项数值复核（见待核对清单）。

## Entry 33

**陈述。** 设 $|q| < 1$，$\theta$、$n$ 为实数。则

$$\text{(i)}\quad \mathrm{Log}\left[\frac{1 + 2\sum_{k=1}^{\infty}q^{k^2}\cos k\theta}{f(-q^2)}\right] = 2\sum_{k=1}^{\infty}\frac{(-1)^{k-1}q^k\cos k\theta}{k(1-q^{2k})}.$$

$$\text{(ii)}\quad \frac14\mathrm{Log}\left[\frac{\sum_{k=1}^{\infty}(-1)^{k-1}q^{k(k-1)/2}\sin(2k-1)n/\sin n}{\sum_{k=1}^{\infty}(-1)^{k-1}(2k-1)q^{k(k-1)/2}}\right] = \sum_{k=1}^{\infty}\frac{q^k\sin^2 kn}{k(1-q^k)}. \tag{33.1}$$

$$\text{(iii)}\quad 1 + 4\sum_{k=1}^{\infty}\frac{q^k\cos kn}{1+q^{2k}} = \varphi^2(-q^2)\cdot\frac{1 + 2\sum_{k=1}^{\infty}q^{k^2}\cos kn}{1 + 2\sum_{k=1}^{\infty}(-1)^kq^{k^2}\cos kn}. \tag{33.3}$$

**说明。** (i) 由 Entry 21 的 (21.2) 与 Entry 19 推出；(ii) 由 (i) 与 Entry 22(iii) 推出；(iii) 由 (i)(ii) 与 Entry 25(iii) 推出。(iii) 的右端分子 $1 + 2\sum_{k=1}^{\infty}q^{k^2}\cos kn$ 为 Jacobi 的 $\vartheta_3$ 函数，分母为 $\vartheta_4$ 函数；(iii) 即 $\mathrm{dn}\,u$ 的 Fourier 级数（见书中注记）。另有 Jacobi 的恒等式

$$\varphi^4(-q^2) = 1 + 8\sum_{k=1}^{\infty}\frac{(-1)^kq^{2k}}{(1+q^{2k})^2}. \tag{33.5}$$

**推论。** 设 $|ab| < 1$，则

$$\varphi^2(-ab)\cdot\frac{f(a,b)}{f(-a,-b)} = 1 + 2\sum_{k=1}^{\infty}\frac{a^k+b^k}{1+a^kb^k}.$$

**状态：** 已证明（书中给出证明）。**对照：** M06（三角级数与 theta 函数）、M11（$\mathrm{dn}\,u$ 的 Fourier 级数）、M07。

**我自验：** (iii) 取 $q = 0.5$、$n = 1$：左端 $0.930134837838$、右端 $0.930134837838$，差 $3.9\times 10^{-31}$（慢收敛级数直接求和至 $k = 200$ + 解析尾项计）；(i)(ii) 与推论未逐项数值复核（见待核对清单）。

## Entry 34

**陈述。** Entry 34 只有 (i)：设 $|q| < 1$，$n$ 为实数，则

$$\mathrm{Log}\left[\frac{\varphi^2(q)}{1 + 4\cos n\cdot\sum_{k=1}^{\infty}(-1)^{k-1}q^{2k-1}\cos(2k-1)n/(1-q^{2k-1})}\right] = 4\sum_{k=1}^{\infty}\frac{(-1)^{k-1}q^k\sin^2 kn}{k(1+q^k)}. \tag{34.1}$$

**说明。** (34.1) 由 Entry 33 的 (33.1) 与 Entry 25(iii) 推出；(33.5) 由 (34.1) 推出（见书中）。另有 (35.9)：$\varphi^2(q) = 1 + 4\sum_{k=1}^{\infty}(-1)^{k-1}q^{2k-1}/(1-q^{2k-1})$。

**状态：** 已证明（书中给出证明）。**对照：** M06、M07、M11。

**我自验：** (i) 取 $q = 0.5$、$n = 1$：左端 $0.60430645152$、右端 $0.60430645152$，差 $9.9\times 10^{-32}$（直接求和至 $k = 200$ + 解析尾项计）。

## Entry 35

**陈述。** 设 $|q| < 1$。置

$$P_n = -\frac{B_n}{2n} + \sum_{k=1}^{\infty}\frac{k^{n-1}q^k}{1-q^k}, \qquad Q_n = \frac{1}{n+1}\cdot\frac{\sum_{k=1}^{\infty}(-1)^{k+1}(2k-1)^{n+1}q^{k(k-1)/2}}{\sum_{k=1}^{\infty}(-1)^{k+1}(2k-1)q^{k(k-1)/2}}.$$

则

$$\text{(i)}\quad \frac12Q_{2n} = -\sum_{k=1}^{n}\binom{2n-1}{2k-1}2^{2k}P_{2k}Q_{2n-2k}. \tag{35.2}$$

置

$$P_n = \frac{(1-2^n)B_n}{2n} + \sum_{k=1}^{\infty}(-1)^{k+1}\frac{k^{n-1}q^k}{1+q^k}, \qquad Q_{2n} = \frac{\frac14E_{2n} + \sum_{k=1}^{\infty}(-1)^{k-1}(2k-1)^{2n}q^{2k-1}/(1-q^{2k-1})}{\frac14 + \sum_{k=1}^{\infty}(-1)^{k-1}q^{2k-1}/(1-q^{2k-1})}.$$

则

$$\text{(ii)}\quad \text{同 (35.2) 的递推成立（书中 (35.6)）。} \tag{35.6}$$

**说明。** (i) 的证明见书中（由 Entry 33 的 (33.1) 与 Entry 34 的 (34.1) 推出）；(ii) 的证明见书中（由 (i) 与 (35.9) 推出）。Berndt 注：(i) 的 $P_n$、$Q_n$ 定义中 $B_n$ 为 Bernoulli 数（Gradshteyn–Ryzhik 约定，见“背景与记号”）；(ii) 的 $E_{2n}$ 为 Euler 数（同约定）。Ch. 15 Entry 12(ix) 已注明为 Entry 35(i) 的特例（Part II，Vol. 2，p. 320）。

**例 (i)。** $3Q_2 = L$。

**例 (ii)。** $5Q_4 = (5L^2-2M)/3$。

**例 (iii)。** $7Q_6 = (35L^3-42ML+16N)/9$。

其中 $L$、$M$、$N$ 为 Eisenstein 级数（见“背景与记号”）。

**状态：** 已证明（书中给出证明）。**对照：** M06（Eisenstein 级数）、M01（Bernoulli 数与 Euler 数）、M07。

**我自验：** (i) 取 $n = 1$、$q = 0.5$：左端 $-10.8094688884$、右端 $-10.8094688884$，差 $1.6\times 10^{-30}$；例 (i) $3Q_2 = L$ 取 $q = 0.5$：左端 $-64.8568133302$、右端 $-64.8568133302$，差 0；(ii) 与例 (ii)(iii) 未逐项数值复核（见待核对清单）。

## Entry 36

**陈述。** 设 $a$、$b$、$c$、$d$ 为复数，$|ab|, |cd| < 1$；置 $p = ab/cd$。则

$$\begin{aligned}
\text{(i)}\quad S := \frac12\{f(a,b)f(c,d) + f(-a,-b)f(-c,-d)\} &= \sum_{k=-\infty}^{\infty}(ad)^{k(k+1)/2}(bc)^{k(k-1)/2}f(acp^k, bd/p^k), \\
\text{(ii)}\quad D := \frac12\{f(a,b)f(c,d) - f(-a,-b)f(-c,-d)\} &= \sum_{k=-\infty}^{\infty}a^{2k+1}(ad)^{k(k-1)/2}(bc)^{k(k+1)/2}f(c/(ap^k), ap^k/c\cdot abcd).
\end{aligned}$$

**Schröter 公式。** (36.1) 与 (36.2) 为 Schröter [1] 的公式：设 $a$、$b$ 为复数，$|ab| < 1$；$n$ 为正整数，则

$$\frac12\{f(a,b)f(a^n,b^n) + f(-a,-b)f(-a^n,-b^n)\} = \sum_{k=0}^{n-1}a^{k(k+1)/2}b^{k(k-1)/2}f(a^{n+2k}b^{n-2k}, a^{n-2k}b^{n+2k}), \tag{36.1}$$

$$\frac12\{f(a,b)f(a^n,b^n) - f(-a,-b)f(-a^n,-b^n)\} = \sum_{k=0}^{n-1}a^{(k+1)(k+2)/2}b^{k(k+1)/2}f(a^{n+2k+2}b^{n-2k-2}, a^{n-2k-2}b^{n+2k+2}). \tag{36.2}$$

(36.1)(36.2) 由 Entry 36(i)(ii) 取 $c = a^n$、$d = b^n$（$p = 1$）推出；此时 Entry 36(i)(ii) 化为 Entry 29(i)(ii)。另有特例 (36.3)–(36.6)（取 $n = 2, 3$ 与 $a = b = q$ 的情形），见书中。

**Blecksmith–Brillhart–Gerst 定理 (36.15)。** 置 $f_0(a,b) = f(a,b)$、$f_1(a,b) = f(-a,-b)$。设 $a$、$b$、$c$、$d$ 为复数，$|ab|, |cd| < 1$；设存在正整数 $\alpha$、$\beta$、$m$ 使 $(ab)^\beta = (cd)^{\alpha(m-\alpha\beta)}$；$\varepsilon_1, \varepsilon_2 \in \{0, 1\}$。则

$$f_{\varepsilon_1}(a,b)f_{\varepsilon_2}(c,d) = \sum_{r\in R}(-1)^{\varepsilon_2r}c^{r(r+1)/2}d^{r(r-1)/2}f_{\delta_1}\left(\frac{a(cd)^{\alpha(1-2r)/2}}{c^\alpha}, \frac{b(cd)^{\alpha(1+2r)/2}}{d^\alpha}\right) \times f_{\delta_2}\left(\frac{(a/b)^{\beta/2}(cd)^{(m-\alpha\beta)(m+1-2r)/2}}{d^{m-\alpha\beta}}, \frac{(b/a)^{\beta/2}(cd)^{(m-\alpha\beta)(m+1-2r)/2}}{c^{m-\alpha\beta}}\right), \tag{36.15}$$

其中 $R$ 为模 $m$ 的完全剩余系，$\delta_1 = 0$（若 $\varepsilon_1 + \alpha\varepsilon_2$ 为偶数）、$1$（若为奇数），$\delta_2 = 0$（若 $\varepsilon_1\beta + \varepsilon_2(m-\alpha\beta)$ 为偶数）、$1$（若为奇数）。取 $\alpha = \beta = 1$、$m = 2$，(36.15) 给出一个恒等式，亦可由 Entry 29(i)(ii) 相加得到。

**说明。** (i)(ii) 的证明见书中（由 Entry 19 的三重积与 (18.1) 的双边级数重排推出）。Berndt 注：Schröter 公式 (36.1)(36.2) 在拉马努金的笔记中已有记录（拉马努金未给出最一般形式）；Blecksmith、Brillhart 与 Gerst [1] 的定理 (36.15) 为 (36.1) 的推广，见书中注记。

**状态：** 已证明（书中给出证明；(36.15) 为 Blecksmith–Brillhart–Gerst 的定理）。**对照：** M06（Schröter 公式）、M07、M11。

**我自验：** (i) 取 $q = 0.5$、$a = 0.3$、$b = 0.2$、$c = 0.4$、$d = 0.15$（$p = ab/cd = 1$）：左端 $1.2938468463$、右端 $1.2938468463$，差 $7.9\times 10^{-31}$；(ii) 与 (36.1)(36.2)(36.15) 未逐项数值复核（见待核对清单）。

## Entry 37

**陈述。** 设 $a$、$b$ 为复数，$|ab| < 1$。则

$$\begin{aligned}
\text{(i)}\quad \frac12\{\varphi(a)\varphi(b) + \varphi(-a)\varphi(-b)\} &= \varphi(ab) + 2\sum_{k=1}^{\infty}(ab)^{k^2}f(ab\cdot a^{2k}/b^{2k}, ab\cdot b^{2k}/a^{2k}), \\
\text{(ii)}\quad \frac12\{\varphi(a)\varphi(b) - \varphi(-a)\varphi(-b)\} &= 2\sum_{k=1}^{\infty}a^{k^2}b^{(k-1)^2}f(a^2b^2\cdot a^{2k-1}/b^{2k-1}, b^{2k-1}/a^{2k-1}), \\
\text{(iii)}\quad \psi(a)\psi(b) &= \psi(ab) + \sum_{k=1}^{\infty}a^{k(k+1)/2}b^{k(k-1)/2}f(ab\cdot a^k/b^k, b^k/a^k).
\end{aligned}$$

**说明。** (i)(ii) 由 Entry 36(i)(ii) 取 $c = a$、$d = b$（$p = 1$）与 Entry 22(i) 推出；(iii) 由 Entry 36(i) 取 $c = a^3$、$d = b^3$ 与 Entry 22(ii) 推出。书中 (i)(ii)(iii) 的公式经 300 DPI 放大图逐字核对无误（$f$ 的自变量中 $a^{2k}/b^{2k}$、$a^{2k-1}/b^{2k-1}$、$a^k/b^k$ 的指数皆与原图一致）。

**状态：** 已证明（由 Entry 36 推出）。**对照：** M06（$\varphi$、$\psi$ 的乘积公式）、M07。

**我自验：** 取 $q = 0.5$、$a = 0.3$、$b = 0.2$：(i) 左端 $1.25946820949$、右端 $1.25946820949$，差 0；(ii) 左端 $1.00844053601$、右端 $1.00844053601$，差 $2.0\times 10^{-31}$；(iii) 左端 $1.6039888935$、右端 $1.6039888935$，差 $3.9\times 10^{-31}$。

## Entry 38

**陈述。** 设 $|q| < 1$。则

$$\begin{aligned}
\text{(i)}\quad \frac{f(-q^5)}{f(-q,-q^4)} &= \sum_{k=0}^{\infty}\frac{q^{k^2}}{(q)_k}, \\
\text{(ii)}\quad \frac{f(-q^5)}{f(-q^2,-q^3)} &= \sum_{k=0}^{\infty}\frac{q^{k(k+1)}}{(q)_k}, \\
\text{(iii)}\quad \frac{f(-q,-q^4)}{f(-q^2,-q^3)} &= \frac{1}{1 + \frac{q}{1 + \frac{q^2}{1 + \frac{q^3}{1 + \cdots}}}}, \\
\text{(iv)}\quad f^2(-q^2,-q^3) - q^{2/5}f^2(-q,-q^4) &= f(-q)\{f(-q^{1/5}) + q^{1/5}f(-q^5)\}. \tag{38.1}
\end{aligned}$$

**说明。** (i)(ii) 为 Rogers–Ramanujan 恒等式（拉马努金原创名 theorem 之一）。Berndt 注：拉马努金在笔记中记录 (i)(ii) 时未给出证明；他多年后发现 Rogers [1]（1916 年）已证明 (i)(ii)，并在论文 [4] 中给出自己的证明。书中证明：由 Entry 7（取 $d = q$、$c = 1$、$b = q^2$、$a = q^3$ 的极限情形）推出 (i)；由 Entry 7 的另一极限情形推出 (ii)。(i)(ii) 的分拆解释：(i) 的右端 $\sum_{k=0}^{\infty}q^{k^2}/(q)_k$ 为分拆数生成函数（部分之差至少为 2 的分拆数等于部分 $\equiv \pm 1 \pmod 5$ 的分拆数）；(ii) 的右端 $\sum_{k=0}^{\infty}q^{k(k+1)}/(q)_k$ 为部分之差至少为 2 且最小部分至少为 2 的分拆数生成函数（等于部分 $\equiv \pm 2 \pmod 5$ 的分拆数）。(iii) 为 Rogers–Ramanujan 连分数（拉马努金发表的论文中证明的唯一连分数）；由 (i)(ii) 相除与 Entry 15 的推论（$a = 1$）推出。Berndt 注：(iii) 的分母 $1 + q/(1 + q^2/(1 + \cdots))$ 的收敛性见书中注记；Odlyzko 与 Wilf [1] 给出 (iii) 的组合解释：$f(n)$（$n$ 个 $(n,k)$ 喷泉的个数）满足 $f(n) = f(n-1) + f(n-2)$（$n \ge 2$），$f(0) = f(1) = 1$，故 $f(n)$ 为 Fibonacci 数；(iii) 的连分数展开系数即 $f(n)$。(iv) 的证明见书中（由五重积定理 (38.2) 推出）。

**五重积定理 (38.2)。** 设 $B$、$q$ 为复数，$|q| < 1$，$B \ne 0$。则

$$f(B^3q, q^5/B^3) - B^2f(q/B^3, B^3q^5) = f(-q^2)\cdot\frac{f(-B^2, -q^2/B^2)}{f(Bq, q/B)}. \tag{38.2}$$

Berndt 注：(38.2) 的历史见书中注记（Weierstrass 与 Schwarz 1893 年、Fricke 1916 年、Watson 1929 年、Bailey 1951 年、Sears 1952 年、Atkin 与 Swinnerton-Dyer 1954 年、Gordon 1961 年、Mordell、Subbarao 与 Vidyasagar 1970 年、Carlitz 1972 年、Andrews 1975 年、Hirschhorn 1988 年、Blecksmith 等 1989 年、Evens 1990 年）。

**状态：** 已证明（(i)(ii) 由 Entry 7 推出；(iii) 由 (i)(ii) 与 Entry 15 推出；(iv) 由五重积定理推出）。**对照：** M07（Rogers–Ramanujan 恒等式与连分数）、M06、M05（分拆与喷泉）、M03。

**我自验：** 取 $q = 0.5$：(i) 左端 $2.17266875085$、右端 $2.17266875085$，差 $3.9\times 10^{-31}$；(ii) 左端 $1.54241381761$、右端 $1.54241381761$，差 $3.9\times 10^{-31}$；(iii) 左端 $0.709916694391$、右端 $0.709916694391$，差 $2.0\times 10^{-31}$；(iv) 左端 $0.243316480916$、右端 $0.243316480916$，差 $4.9\times 10^{-32}$。

## Entry 39

**陈述。** 设 $\alpha$、$\beta$ 为正实数，$\alpha\beta = \pi^2$。则

$$\begin{aligned}
\text{(i)}\quad \left\{\frac{\sqrt{5}+1}{2} + \frac{e^{-2\alpha/5}}{1 + \frac{e^{-2\alpha}}{1 + \frac{e^{-4\alpha}}{1 + \cdots}}}\right\} \times \left\{\frac{\sqrt{5}+1}{2} + \frac{e^{-2\beta/5}}{1 + \frac{e^{-2\beta}}{1 + \frac{e^{-4\beta}}{1 + \cdots}}}\right\} &= \frac{5+\sqrt{5}}{2}, \\
\text{(ii)}\quad \left\{\frac{\sqrt{5}-1}{2} + \frac{e^{-\alpha/5}}{1 - \frac{e^{-\alpha}}{1 + \frac{e^{-2\alpha}}{1 - \cdots}}}\right\} \times \left\{\frac{\sqrt{5}-1}{2} + \frac{e^{-\beta/5}}{1 - \frac{e^{-\beta}}{1 + \frac{e^{-2\beta}}{1 - \cdots}}}\right\} &= \frac{5-\sqrt{5}}{2}.
\end{aligned}$$

**推论 (i)。** 取 $\alpha = \beta = \pi$，得

$$\frac{e^{-\pi/5}}{1 - \frac{e^{-\pi}}{1 + \frac{e^{-2\pi}}{1 - \cdots}}} = \sqrt{\frac{5-\sqrt{5}}{2}} - \frac{\sqrt{5}-1}{2}.$$

**推论 (ii)。** 取 $\alpha = \beta = \pi$，得

$$\frac{e^{-2\pi/5}}{1 + \frac{e^{-2\pi}}{1 + \frac{e^{-4\pi}}{1 + \cdots}}} = \sqrt{\frac{5+\sqrt{5}}{2}} - \frac{\sqrt{5}+1}{2}.$$

**说明。** (i) 在拉马努金致 Hardy 的第一封信中已有记录；Watson [1] 首次在印刷品中证明 (i)。(ii) 的证明见书中（由 (39.1) 的 Watson 恒等式与 Entry 38(iii) 推出）。Berndt 注：Jacobsen [1] 证明 (i)(ii) 对复数 $\alpha$、$\beta$（$\alpha\beta = \pi^2$，$\mathrm{Re}\,\alpha, \mathrm{Re}\,\beta > 0$）亦成立。推论 (i)(ii) 由 (i)(ii) 取 $\alpha = \beta = \pi$ 推出（此时两因子相等，故每因子为右端的平方根）。

**状态：** 已证明（Watson 首次在印刷品中证明 (i)；(ii) 的证明见书中；Jacobsen 推广至复数 $\alpha$、$\beta$）。**对照：** M06（模变换与黄金比）、M03（连分数）、M04。

**我自验：** (i) 取 $\alpha = \beta = \pi$：每因子 $1.90211303259$，乘积 $3.61803398875 = (5+\sqrt{5})/2$，差 0；(ii) 每因子 $1.17557050458$，乘积 $1.38196601125 = (5-\sqrt{5})/2$，差 0；推论 (i) 左端 $0.557536515835$、右端 $0.557536515835$，差 $9.9\times 10^{-32}$；推论 (ii) 左端 $0.28407904384$、右端 $0.28407904384$，差 $4.9\times 10^{-32}$。

## 小结

- 本章 76 页正文（书页 11–86），是 Part III 的第一章、五卷的第 16 章：前 17 节为 q 级数（Entry 1–17），后 22 节为 theta 函数（Entry 18–39）。编号 Entry 39 条（Entry 1–39，无缺号），Entry 标题 87 个（见“本章结构”表后的计数说明）；另有第 8 节引理 (8.1)、第 36 节 Schröter 公式 (36.1)(36.2) 与 Blecksmith–Brillhart–Gerst 定理 (36.15)、第 38 节五重积定理 (38.2)，书中明确标为引理或定理而非 Entry。
- 亮点：Entry 14 的 q-beta 积分（拉马努金原创，Askey 的简单证明）；Entry 17 的 ${}_1\psi_1$ 求和（拉马努金原创，Hahn 1949 年、Jackson 1950 年首次在印刷品中证明）；Entry 19 的 Jacobi 三重积（由 Entry 17 推出）；Entry 38(i)(ii) 的 Rogers–Ramanujan 恒等式（由 Entry 7 推出）与 (iii) 的 Rogers–Ramanujan 连分数（拉马努金发表的论文中证明的唯一连分数）及 (iv) 的五重积恒等式；Entry 39 的黄金比连分数（(i) 在拉马努金致 Hardy 的第一封信中已有记录，Watson 首次在印刷品中证明）。
- 本轮发现的两处原书印文问题（均经 300 DPI 放大图与数值复核确认，见各条注记）：(1) Entry 12 的条件 $a = b^{2m+1}$ 很可能漏印了 $q$，应为 $a = bq^{2m+1}$（书中证明三次写为 $a = bq^{2m+1}$；$a = bq^{2m+1}$ 时第 $m+1$ 项因子为 0，连分数终止）；(2) Entry 12 的 (12.1) 连分数排版有歧义：按字面把首项读作 $1/(1-ab)$ 再加连分数则数值不符（四组参数下差 $0.05$–$0.19$），读作“1 除以整个连分数”则四组参数下差皆 $\le 4\times 10^{-31}$，终止情形 $a = bq^3$ 下差 0。本文件按数值验证的读法写出 (12.1)。
- 本轮的另一发现：书中未定义的单变量记号 $f(q)$ 经数值核对确为 $f(q,-q^2)$（$q = 0.5$ 时 $f(q,-q^2) = 1.21072413030105918013617285611$，等于 $\varphi(q)/\chi(q)$；Entry 24(i) 的 $f(q)/f(-q) = 4.19243088929266462344639696087$ 等于 $(-q;q^2)_\infty/(q;q^2)_\infty$；Entry 24(iii) 的 $f(q)/f(-q^2) = \chi(q)$ 精确成立；另一候选 $f(q,q^2) = 1.78933741155287907159762028642$ 与三式皆不符）。
- 本轮数值复核约 36 项（直接求和 + 解析尾项，mpmath 30 位；慢收敛级数不用 `nsum`，见 Ch. 8–14 的教训）：Entry 2、Entry 3、Entry 7、Entry 9、Entry 12（四组参数 + 终止情形）、Entry 13（两组参数）、Entry 14（数值积分容差 $1.4\times 10^{-17}$）、Entry 15、Entry 16（$n = 3$）、Entry 17（(17.1) 差 $2.0\times 10^{-31}$；(17.6) 差 $9.3\times 10^{-10}$，为正向截断尾项）、Entry 19、Entry 20（$n = 1$，复数，差 $1.5\times 10^{-33}$）、Entry 22(i)–(iii)、Entry 24(i)(ii)(iii)、Entry 25(i)(ii)(v)、Entry 27(i)、Entry 29(i)、Entry 30(i)、Entry 31（(31.1)(31.2)(31.3)，$n = 3$）、Entry 32(i)、Entry 33(iii)（差 $3.9\times 10^{-31}$）、Entry 34(i)（差 $9.9\times 10^{-32}$）、Entry 35(i)（差 $1.6\times 10^{-30}$）与例 (i)（差 0）、Entry 36(i)、Entry 37(i)(ii)(iii)、Entry 38(i)–(iv)、Entry 39(i)(ii) 与推论 (i)(ii)，全部通过。另有三处自验方法错误的纠正记录：Entry 12 初版按字面读法检验（差 $0.0476$），按“1 除以整个连分数”读法重验后通过；Entry 13 初版误把偶数项读作 $a(q^{2n} - q^{2n-1})$，按 $a(q^{2n} - q^n)$ 重验后差 0；Entry 17(17.6) 初版把双边和负向截断于 $k = -60$（差 $1.8$），补足负向项至 $k = -1500$ 与解析尾项后差 $9.3\times 10^{-10}$（余差为正向截断尾项）。
- Part III 第一章收官：Ch. 16：39 条（Entry 1–39）。Part I + Part II + Part III Ch. 16 = $174 + 195 + 39 = 408$ 条已填上线。

## 待核对清单

1. IMSC 本章结果数：imsc.res.in 2026-11-08 再次不可达（curl 返回 000），未能补录。
2. Berndt 章首计数：本章导言（pp. 11–12）未给出本章公式或定理陈述的总数。
3. TIFR 影印版页码：除笔记 [9, Vol. 2, p. 197]（Entry 19 的三重积恒等式）、p. 198（Entry 26 的 $G(q)$ 断言）、p. 199（Entry 28 的推论“and so on”）外，各条在 TIFR 影印版中的对应页未逐条核对。
4. Entry 12 的条件：原书 (12.1) 的条件印作 $a = b^{2m+1}$（300 DPI 放大图确认无 $q$），但书中证明三次写为 $a = bq^{2m+1}$，且 $a = bq^{2m+1}$ 时连分数终止；疑似漏印 $q$，应为 $a = bq^{2m+1}$，待与其他印本或 Adiga–Berndt–Bhargava–Watson 的 Memoir（1985）对照。
5. Entry 12 的 (12.1) 连分数读法：原书排版把首项印作 $1/(1-ab)$ 后接连分数；按字面读法数值不符，按“1 除以整个连分数”读法四组参数下差皆 $\le 4\times 10^{-31}$，终止情形下差 0。本文件按数值验证的读法写出，待与其他印本或 Memoir 对照排版。
6. Entry 13 的 (13.1) 偶数项分子：原书印作 $a(q^{2n} - q^n)$（$n = 1, 2, \dots$）；本文件按 300 DPI 放大图核对后写为 $j$ 为偶数时 $a(q^j - q^{j/2})$（同一式子），数值复核差 0。初版误读作 $a(q^{2n} - q^{2n-1})$ 的纠正记录见 Entry 13 注记。
7. Entry 18(iv) 的非整数 $n$ 情形：拉马努金说 (iv) 对非整数 $n$“近似成立”；Berndt 未能把这一说法表述精确（见书中注记）。
8. Entry 26 的“度”定义：与 Ch. 15 Entry 10(ii) 的“度”定义之间的关系未完全澄清（Ismail 的奇点阶解释见书中注记；Ch. 15 待核对清单第 14 项亦有记录）。
9. Entry 14 的数值复核：差 $1.4\times 10^{-17}$ 为 mpmath `quad` 数值积分的容差（$n = 1/2$、$a = 0.3$、$q = 0.5$，值 $1.98045687184$），非公式误差；可改用更高精度积分或解析尾项重验。
10. Entry 17(17.6) 的数值复核：差 $9.3\times 10^{-10}$ 为正向截断于 $k = 60$ 的尾项（$\sim 0.7^{60} \approx 5\times 10^{-10}$），非公式误差；可延长正向求和至 $k = 100$ 重验。
11. 未逐项数值复核的条目：Entry 9 推论 (i)(ii)、Entry 15 推论、Entry 24(iv)、Entry 25(iii)(iv)(vi)(vii)、Entry 27(ii)–(v)、Entry 29(ii)、Entry 30(ii)–(vi)、Entry 31 推论 (i)(ii) 与例 (i)–(v)、Entry 32(ii)–(iv)、Entry 33(i)(ii) 与推论、Entry 35(ii) 与例 (ii)(iii)、Entry 36(ii) 与 (36.1)(36.2)(36.15)。Entry 1(i)–(iv)、Entry 4、Entry 5、Entry 6、Entry 8、Entry 10、Entry 11、Entry 18、Entry 21、Entry 23、Entry 26、Entry 28 未做数值复核（或为定义、或为已证明的经典结果、或为证明思路已见书中）。
12. 第 35 节的 $B_n$、$E_{2n}$ 约定：Gradshteyn–Ryzhik 的定义与拉马努金所用的约定不同（见“背景与记号”）；$P_n$、$Q_n$ 的定义中 $B_n$、$E_{2n}$ 的取值（$B_1 = -1/2$ 等）待逐项核对。
13. Entry 10 的证明细节：书中以 Ch. 12 Entry 40 为起点，代入 $\ell$、$m$、$n$、$x$ 的特定值并化简；代入的细节未展开。

## 来源说明

- 整理层：Bruce C. Berndt，《Ramanujan's Notebooks》，Part III，Springer，1991，Ch. 16，书页 11–86（正文）；参考文献自书页 489 起，索引自书页 505 起。
- 电子版：archive.org 标识符 `ramanujan_notebooks_iii`（《Ramanujan's Notebooks, Part 3》，Springer 1991，XIII + 510 页，DOI **10.1007/978-1-4612-0965-2**；PDF 21,002,730 字节、524 叶，md5 `de9211b0bde03dd9255145d3f09bb78f`），**PDF 页 = 书页 + 14**（与 Part II 的 +12 不同）。本章为 PDF 页 25–100（书页 11–86）；PDF 页 101 起为 Ch. 17（书页 87）。DOI 核对：任务简报所给 DOI 10.1007/978-1-4612-0963-8 经 Springer 官网（link.springer.com/book/10.1007/978-1-4612-0965-2）与多家书目核对为误，正确 DOI 为 10.1007/978-1-4612-0965-2（eBook ISBN 978-1-4612-0965-2，精装 ISBN 978-0-387-97503-0，1991 年初版，1997 年修订第二版）。
- 转录方法：全部公式按 PDF 原图（150 DPI，书页 11–86）逐字转录；关键公式 Entry 12（条件行与 (12.1)）、Entry 13（(13.1) 偶数项）、Entry 37(i)(ii)(iii) 另用 300 DPI 放大图确认；OCR（DjVu 文本层）只作检索索引，公式凡与原图或数值不符者一律纠正。
- 文献指引：[9] 指拉马努金《Notebooks》TIFR 影印版（Vol. 2）；[10] 指 Hardy 等编《Collected Papers of Srinivasa Ramanujan》；[11] 指拉马努金名篇“On certain arithmetical functions”；[3] 指 Hardy《Ramanujan: Twelve Lectures on Subjects Suggested by His Life and Work》；[4] 指拉马努金论文“On certain infinite series”；[18] 指 Andrews《The Theory of Partitions》；[1]、[2] 等文献编号均按 Berndt 书中所引。
- 版权说明：本文件只收公式陈述与自写导读、证明思路与文献指引，未复制 Berndt 原文的正文与证明。
