# Part III，Chapter 17——Fundamental Properties of Elliptic Functions（椭圆函数的基本性质）

出处：Bruce C. Berndt，《Ramanujan's Notebooks》，Part III，Springer，1991，Ch. 17，书页 87–142。

本章是 Part III 的第二章、Berndt 五卷的第 17 章：拉马努金在此引入 Jacobian 椭圆函数与椭圆积分，并把大量无穷级数求值归结为椭圆函数论中的参数。Berndt 在章首导言（p. 87）中说，本章几乎全部 devoted 于椭圆函数论，基础已在 Ch. 16 的 theta 函数诸节中打好；拉马努金不使用椭圆函数与椭圆积分的经典记号与术语，第 6 节把他的函数与参数与熟知的记号对上。本章共 **18 条编号 Entry（Entry 1–18，无缺号）**，另含推论、例题与引理 149 个子标题（见“本章结构”表后的计数说明）；此外还有若干以 Lemma、Corollary、Example 之名出现的结果（第 3 节引理、第 4 节引理、第 6 节推论与例 (i)–(iv)、第 9 节例题），书中明确标为引理、推论或例题而非 Entry。

## 背景与记号

- 章首导言（p. 87）：本章大部分内容是各种无穷级数求值，求值结果用椭圆函数与椭圆积分中频繁出现的参数表出；拉马努金的许多恒等式可由 Jacobi《Fundamenta Nova》中的定理推出，特别是 Jacobian 椭圆函数的 Fourier 级数，但 Berndt 与拉马努金一样 prefer 用 theta 函数。本章有多少结果是拉马努金原创难以评估：多数公式在印刷品中找不到，但多数可由已发表结果不太费力地推出。
- 记号（pp. 87–88）：$(a)_k := \Gamma(a+k)/\Gamma(a)$（(0.1)，Pochhammer 符号）；广义超几何级数 ${}_pF_q$ 按 (0.2) 定义，本章 $p = q+1$，故 ${}_{q+1}F_q$ 在 $|x| < 1$ 时恒收敛；q 级数记号 $(a)_n := (a;q)_n := \prod_{k=0}^{n-1}(1-aq^k)$、$(a)_\infty := (a;q)_\infty := \prod_{k=0}^{\infty}(1-aq^k)$（(0.3)，$|q| < 1$）；(0.1) 与 (0.3) 的记号冲突，上下文可分辨。$\psi(z) = \Gamma'(z)/\Gamma(z) = -\gamma + \sum_{k=0}^{\infty}(1/(k+1) - 1/(k+z))$（(0.4)，$\gamma$ 为 Euler 常数），下文频繁使用。
- 第 2 节的函数 $F(x)$（(2.1)）：对 $0 < x < 1$，$F(x) = \exp\left(-\pi\,{}_2F_1(\frac12,\frac12;1;1-x)/{}_2F_1(\frac12,\frac12;1;x)\right)$，$\lim_{x\to 0+}F(x) = 0$、$\lim_{x\to 1-}F(x) = 1$（(2.2)(2.3)）。$F(x)$ 在 Ch. 11 第 27 节中已简略讨论过。
- 第 3 节的 theta 函数 $\varphi(q) = \sum_{k=-\infty}^{\infty}q^{k^2}$（(3.1)，$|q| < 1$）；第 5 节的 $\psi(q) = \sum_{k=0}^{\infty}q^{k(k+1)/2}$（(5.1)）。$\varphi$、$\psi$、$f(-q)$、$\chi(q)$ 的定义与乘积表示见 Ch. 16 Entry 22（本文件沿用 Ch. 16 的记号：$\varphi(q) = f(q,q)$、$\psi(q) = f(q,q^3)$、$f(-q) = f(-q,-q^2) = (q;q)_\infty$、$\chi(q) = (-q;q^2)_\infty$；$f(a,b)$ 为 Ch. 16 (18.1) 的一般 theta 函数）。
- 第 6 节的记号（(6.2)–(6.4)）：$z = {}_2F_1(\frac12,\frac12;1;x)$，$y = \pi\,{}_2F_1(\frac12,\frac12;1;1-x)/{}_2F_1(\frac12,\frac12;1;x)$，则 $\varphi(e^{-y}) = \sqrt{z}$；且 $F(x) = e^{-y}$。下文大量使用 $x$、$y$、$z$ 这一组记号。
- 第 6 节的椭圆积分对接（(6.9)–(6.12)）：完全椭圆积分 $K := K(k) := \int_0^{\pi/2}d\varphi/\sqrt{1-k^2\sin^2\varphi} = \frac12{}_2F_1(\frac12,\frac12;1;k^2) = \frac12\pi\varphi^2(q)$，$k$（$0 < k < 1$）为模；拉马努金不用 $k$ 而置 $x = k^2$（后文推导模方程时置 $\alpha = k^2$）；余模 $k' = \sqrt{1-k^2}$，$\sqrt{1-x} = k' = \varphi^2(-q)/\varphi^2(q)$（(6.10)）；$z = 2K/\pi$（(6.11)）；$q = e^{-y} = e^{-\pi K'/K}$（(6.12)）。
- 第 9 节的 Eisenstein 级数 $L$（(9.2)）：$L(e^{-2y}) = 1 - 24\sum_{k=1}^{\infty}k/(e^{2ky}-1)$；第 13 节的 $M(q) = 1 + 240\sum_{k=1}^{\infty}k^3q^k/(1-q^k)$、$N(q) = 1 - 504\sum_{k=1}^{\infty}k^5q^k/(1-q^k)$（与 Ch. 15 第 9 节、Ch. 16 第 35 节的 $L$、$M$、$N$ 相同；拉马努金名篇 [11] 中分别记为 $P$、$Q$、$R$）。
- 第 13 节的三种生成新公式的方法：duplication（倍乘：由 $\Omega(x,e^{-y},z) = 0$ 得 $\Omega(((1-\sqrt{1-x})/(1+\sqrt{1-x}))^2,e^{-2y},\frac12z(1+\sqrt{1-x})) = 0$）、dimidiation（折半：反向变换，$\Omega(4\sqrt{x}/(1+\sqrt{x})^2,e^{-y/2},(1+\sqrt{x})z) = 0$）、change of sign（变号，Jacobi 的方法：由 $\Omega(x,e^{-y},z) = 0$ 得 $\Omega(x/(x-1),-e^{-y},z\sqrt{1-x}) = 0$）。前两种等价于 Landen 变换。
- 第 8 节的双重级数求和术语（MacMahon [1, pp. 26–32]）：按行求和、按列求和、row–column 方法、column–row 方法、对称阵的 Clausen 变换。
- 本章与已填章节的互见：Ch. 11 的超几何（Entry 25 的推论、Entry 30、Entry 32(ii)(iii)、Entry 33(iv)、Entry 34、Entry 35(iii)）是 Entry 1、Entry 2、Entry 6 的证明工具，Entry 2(i) 在 Ch. 11 第 26 节已作为推论陈述并证明，$F(x)$ 在 Ch. 11 第 27 节已简略讨论；Ch. 14 第 7 节的 theta 函数反演公式（Entry 7）与第 6 节推论的 $\sqrt{\alpha}\varphi(e^{-\alpha^2}) = \sqrt{\beta}\varphi(e^{-\beta^2})$（$\alpha\beta = \pi$）为同一公式的两种形式（见 Ch. 16 Entry 27(i)）；Ch. 15 的 $L$、$M$、$N$ 与 Eisenstein 级数（Entry 12、Entry 13、Entry 14）是 Entry 9(iv)、Entry 13、Entry 14、Entry 15 的直接前驱，Entry 9 的 (9.3) 即 Ch. 15 的 $L(e^{-2y})$ 公式，Entry 13 的证明用 Ch. 15 第 13 节的 $t\,dL/dt = (L^2-M)/12$ 与 $t\,dM/dt = (LM-N)/3$；Ch. 16 的 theta 函数（Entry 17 的 ${}_1\psi_1$ 求和、Entry 19 的三重积、Entry 22 的 $\varphi$、$\psi$、$f(-q)$、$\chi$ 乘积表示、Entry 24 的比值恒等式、Entry 25 的 $\varphi$、$\psi$ 恒等式、Entry 27 的模变换、Entry 32–35 的对数恒等式与 $P_n$、$Q_n$）是 Entry 3、Entry 8、Entry 10–12、Entry 15–17 的证明工具；Ch. 16 Entry 33(iii) 的 $\mathrm{dn}\,u$ Fourier 级数即本章 Entry 16–17 所用的 $\mathrm{sn}\,u$、$\mathrm{dn}\,u$ Fourier 级数之同源；Part I Ch. 3 第 14 节的推论 1（(2.13)）是 Entry 2(vi) 证明的工具。
- 与主题模块的对照总览：椭圆函数主线见 **M11**（全章：Entry 1 的 Legendre 函数与椭圆积分、Entry 3–6 的 $\varphi(q)$ 与 $F(x)$、Entry 7 的椭圆积分加法定理与 Gauss、Landen 变换、Entry 8 的 Jacobi 恒等式、Entry 9–12 的 $\varphi$、$\psi$、$f$、$\chi$ 求值、Entry 13–17 的 Eisenstein 级数与 $\sinh$、$\cosh$ 级数求值、Entry 18 的 Cauchy 级数）；无穷级数见 **M02**（Entry 2 的 $F(x)$ 幂级数算法、Entry 8、Entry 13–18 的 $\sinh$、$\cosh$、$e^{ky}\pm 1$ 级数求值）；模形式见 **M06**（Entry 5 的反演公式、Entry 6 的 $\varphi(e^{-y}) = \sqrt{z}$ 与推论的模变换、Entry 9–13 的 $L$、$M$、$N$ Eisenstein 级数、Entry 13–14 的 duplication/dimidiation 与模方程前驱）；q 级数与 theta 函数见 **M07**（Entry 3–6、Entry 8、Entry 10–12 的 $\varphi$、$\psi$、$\chi$、Entry 17 例 (i)–(vi) 的 $\varphi^8$、$\psi^8$ 求值）；超几何函数见 **M02**（Entry 1、Entry 6、Entry 9 的 ${}_2F_1$、${}_3F_2$、${}_4F_3$）；Gamma 函数见 **M10**（Entry 1 推论 (i) 的 Gauss 定理、Entry 6 例 (i)–(iii) 的 $\Gamma(1/4)$、$\Gamma(3/4)$、$\Gamma(5/8)$、$\Gamma(9/8)$ 特殊值）；积分见 **M09**（Entry 1、Entry 7 的椭圆积分）；数论见 **M01**（Entry 2(vii) 的 Bernoulli 数、Entry 8(iv) 的 Legendre 符号、Entry 18 的 Cauchy–Rao–Ayyar–Riesel–Zucker–Ling 级数）；$\pi$ 与特殊常数见 **M04**（Entry 2 例 1 的 $e^{-\pi}$、$e^{-\pi\sqrt{2}}$、$e^{-2\pi}$、Entry 6 例 (i)–(iii) 的 $\varphi(e^{-\pi})$ 等、Entry 18 的 $\pi/24$、$5\pi/24$）。

## 本章结构

| Entry | 主题 | 书页 |
|---|---|---|
| Entry 1 | 椭圆积分与 Legendre 函数 $P_{-n}$（推论 (i)(ii)） | 88–91 |
| Entry 2 | $F(x)$ 的七条性质 (i)–(vii) 与例 1、例 2 | 91–97 |
| Entry 3 | $\varphi^2(q) = {}_2F_1(\frac12,\frac12;1;1-\varphi^4(-q)/\varphi^4(q))$（第 3 节引理） | 98–99 |
| Entry 4 | $F$ 的倍乘公式 (i)(ii)（第 4 节引理） | 99–100 |
| Entry 5 | 反演公式 $F(1-\varphi^4(-q)/\varphi^4(q)) = q$ | 100–101 |
| Entry 6 | $\varphi^2(F(x)) = {}_2F_1(\frac12,\frac12;1;x)$、$\varphi(e^{-y}) = \sqrt{z}$（推论与例 (i)–(iv)） | 101–104 |
| Entry 7 | 椭圆积分的十三条结果 (i)–(xiii)（加法定理、Gauss 与 Landen 变换） | 104–113 |
| Entry 8 | $\varphi$、$\psi$、$f$ 的十二条级数恒等式 (i)–(xii) 与例题 | 114–120 |
| Entry 9 | $y$、$z$ 的微分关系 (i)–(iv) 与例题 | 120–122 |
| Entry 10 | $\varphi(e^{-y})$ 等九条求值 (i)–(ix) | 122–123 |
| Entry 11 | $\psi(e^{-y})$ 等九条求值 (i)–(ix) | 123–124 |
| Entry 12 | $f$、$\chi$ 的七条求值 (i)–(vii) | 124–125 |
| Entry 13 | $L$、$M$、$N$ 的十三条公式 (i)–(xiii) | 126–129 |
| Entry 14 | $e^{ky}\pm 1$ 级数的十二条求值 (i)–(xii) | 129–132 |
| Entry 15 | $\sinh$ 级数的十六条求值 (i)–(xvi) | 132–134 |
| Entry 16 | $\cosh$ 级数的十三条求值 (i)–(xiii) | 134–138 |
| Entry 17 | $\cosh$ 级数与 $e^{(2k+1)y}-1$ 级数的九条求值 (i)–(ix) 与例 (i)–(vi) | 138–140 |
| Entry 18 | Cauchy 级数三条 (i)–(iii) 与例 (i)–(iii) | 140–142 |

计数说明：编号 Entry 1–18 共 18 条，无缺号。分体、推论与例子标题 149 个：Entry 1 推论 (i)(ii) 2、Entry 2(i)–(vii) 7 与例 1、例 2 共 2、Entry 4(i)(ii) 2、Entry 6 推论 1 与例 (i)–(iv) 4、Entry 7(i)–(xiii) 13、Entry 8(i)–(xii) 12 与例题 1、Entry 9(i)–(iv) 4 与例题 1、Entry 10(i)–(ix) 9、Entry 11(i)–(ix) 9、Entry 12(i)–(vii) 7、Entry 13(i)–(xiii) 13、Entry 14(i)–(xii) 12、Entry 15(i)–(xvi) 16、Entry 16(i)–(xiii) 13、Entry 17(i)–(ix) 9 与例 (i)–(vi) 6、Entry 18(i)–(iii) 3 与例 (i)–(iii) 3。按“无分体的 Entry 计 1、有分体的 Entry 计其分体数”的口径，Entry 标题共 153 个（另有 Entry 1、Entry 3、Entry 5、Entry 6 的主陈述 4 个计入 153 之内；Entry 3 与 Entry 5 无分体，各计 1）。另有第 3 节引理、第 4 节引理 2 个非 Entry 标题的结果。

## Entry 1

**陈述。** 设 $n$ 与 $x$ 为实数，$0 \le x < 1$。则

$$\int_0^{\pi/2}\frac{\cos\{(1-2n)\sin^{-1}(\sqrt{x}\sin\varphi)\}}{\sqrt{1-x\sin^2\varphi}}\,d\varphi = \frac{\pi}{2}\,{}_2F_1(1-n,n;1;x).$$

**说明。** 证明用 Ch. 11 Entry 35(iii) 的 $(1-x^2)^{-1/2}\cos(2n\sin^{-1}x) = {}_2F_1(\frac12+n,\frac12-n;\frac12;x^2)$，以 $1-2n$ 代 $2n$、以 $\sqrt{x}\sin\varphi$ 代 $x$，再对 $\varphi$ 在 $[0,\pi/2]$ 上积分。改写 (1.1)：置 $\sin\theta = \sqrt{x}\sin\varphi$，则

$$\int_0^{\sin^{-1}\sqrt{x}}\frac{\cos(2n-1)\theta}{\sqrt{x-\sin^2\theta}}\,d\theta = \frac{\pi}{2}\,{}_2F_1(1-n,n;1;x). \tag{1.1}$$

由 Murphy 的结果（Whittaker–Watson [1, p. 312]），${}_2F_1(1-n,n;1;x) = P_{-n}(1-2x)$（$P_n$ 为 Legendre 函数），故 (1.1) 可写为

$$\int_0^{\sin^{-1}\sqrt{x}}\frac{\cos(2n-1)\theta}{\sqrt{x-\sin^2\theta}}\,d\theta = \frac{\pi}{2}P_{-n}(1-2x). \tag{1.2}$$

取 $n = \frac12$，得 $P_{-1/2}$ 用第一类椭圆积分的表示（Kleiber [1, p. 10]）。再以 $\cos\alpha$ 代 $1-2x$、以 $-n$ 代 $n$、以 $\varphi/2$ 代 $\theta$，得 Mehler–Dirichlet 积分

$$\frac{\sqrt{2}}{\pi}\int_0^{\alpha}\frac{\cos(n+\frac12)\varphi}{\sqrt{\cos\varphi-\cos\alpha}}\,d\varphi = P_n(\cos\alpha).$$

**推论 (i)。** 对任意实数 $n$，

$$\int_0^{\pi/2}\frac{\cos\left\{(1-2n)\sin^{-1}\left(\frac{\sin\varphi}{\sqrt{2}}\right)\right\}}{\sqrt{1-\frac12\sin^2\varphi}}\,d\varphi = \frac{\pi^{3/2}}{2\Gamma(1-\frac12n)\Gamma(\frac12+\frac12n)}. \tag{1.3}$$

证明：在 Entry 1 中取 $x = \frac12$，再用 Gauss 定理 (1.4)：${}_2F_1(a,b;\frac12(a+b+1);\frac12) = \Gamma(\frac12)\Gamma(\frac12(a+b+1))/(\Gamma(\frac12+\frac12a)\Gamma(\frac12+\frac12b))$（Bailey [4, p. 11]；拉马努金在 Ch. 10 Entry 34 中亦重新发现）。

**推论 (ii)。** 对 $0 \le x < 1$，置 $u_x = \int_0^{\pi/2}\cos\{(1-2n)\sin^{-1}(\sqrt{x}\sin\varphi)\}/\sqrt{1-x\sin^2\varphi}\,d\varphi$。则对 $0 < x < 1$ 与非整数 $n$，

$$\exp\left(-\frac{\pi}{\sin(\pi n)}\frac{u_{1-x}}{u_x}\right) = x\exp(\psi(n)+\psi(1-n)+2\gamma)\times\{1+(2n^2-2n+1)x+(1-\frac72(n-n^2)+\frac{13}{4}(n-n^2)^2)x^2+\cdots\}.$$

证明用 Ch. 11 Entry 25 的推论 1（取 $n = 0$，再以 $n-1$、$-n$ 代 $a$、$b$）与 Entry 1；其中 $\psi(x) = \Gamma'(x)/\Gamma(x)$，$\gamma$ 为 Euler 常数。

**状态：** 已证明（书中给出证明）。**对照：** M11（椭圆积分与 Legendre 函数）、M09（积分）、M10（Gamma 函数）。

**我自验：** 取 $n = 0.3$、$x = 0.4$：Entry 1 左端 $1.74361172018$、右端 $1.74361172018$，差 0（mpmath 数值积分，30 位）。推论 (i) 取 $n = 0.3$：左端 $1.80723914012$、右端 $1.80723914012$，差 $5.9\times 10^{-31}$。推论 (ii) 未逐项数值复核（见待核对清单）。

## Entry 2

**陈述。** 对 $0 < x < 1$，$F(x)$ 如 (2.1) 所定义。

**(i)** 若 $0 < x < 1$，则

$$F(x) = \frac{x}{16}\exp\left(\frac{4\sum_{k=1}^{\infty}\frac{(\frac12)_k^2}{(k!)^2}\sum_{j=1}^k\frac{1}{2j(2j-1)}x^k}{{}_2F_1(\frac12,\frac12;1;x)}\right).$$

Entry 2(i) 在 Ch. 11 第 26 节中已作为推论陈述并证明（Part II [9, pp. 78–79]）。

**(ii)**（拉马努金原话，$x \ge 0$）

$$F(1-e^{-x}) = \frac{x}{10+\sqrt{36+x^2}}\quad\text{very nearly.} \tag{2.4}$$

即近似式而非等式。(2.4) 右端的 Maclaurin 级数为 $x/16 - x^3/3072 + 280x^5/(2^{19}\cdot 3^3\cdot 5) + \cdots$（(2.5)，$|x| < 8$）；而由 Entry 2(vii)（$x$ 换为 $x/8$）得 $F(1-e^{-x}) = x/16 - x^3/3072 + 279x^5/(2^{19}\cdot 3^3\cdot 5) + \cdots$（(2.6)），$x^5$ 系数仅差 $1/(2^{19}\cdot 3^3\cdot 5)$。Waadeland 的解释：把 (2.6) 的连分数中 $53/(2^9\cdot 3\cdot 5) = 1/144.905660\cdots$ 的分母换为高度合成数 144，并把后续分子一律换为 $t/144$，即得 (2.4)。

**(iii)** 对 $0 < x < 1$，

$$\mathrm{Log}\,F(x)\,\mathrm{Log}\,F(1-x) = \pi^2.$$

由 $F$ 的定义 (2.1) 直接得。

**(iv)** $F(1-x) + F(1-1/x) = 0$。

证明用 Ch. 11 Entry 30 与 Entry 32(ii)；由 Entry 2(i) 得 $\lim_{x\to 1}F(1-x)/F(1-1/x) = -1$，故比值为常数 $-1$。

**(v)** $F(x^2) = F\left(\frac{4x}{(1+x)^2}\right)^2$。

证明用 Ch. 11 Entry 32(iii) 的 (2.7)：${}_2F_1(\frac12,\frac12;1;4x/(1+x)^2) = (1+x)\,{}_2F_1(\frac12,\frac12;1;x^2)$，与 (2.8)。

**(vi)** 若 $|x| < \frac13$，则

$$F\left(\frac{2x}{1+x}\right) = \frac{1}{2^3}x + \frac{5}{2^7}x^3 + \frac{369}{2^{14}}x^5 + \frac{4097}{2^{18}}x^7 + \frac{1594895}{2^{27}}x^9 + \cdots.$$

证明：拉马努金关于计算 $F(2x/(1+x))$ 幂级数展开的精巧算法——由 Entry 2(iv) 知 $F(2x/(1+x))$ 为 $x$ 的奇函数，设 $F(2x/(1+x)) = \sum_{k=1}^n a_kx^{2k-1} + O(x^{2n+1})$（(2.9)，$|x| < \frac13$）；置 $y^2 = 2x/(1+x)$，用 Entry 2(v) 得 $F(4y/(1+y)^2)$ 的展开 (2.10)；再置 $x = 2y/(1+y^2)$ 得 (2.11)，比较系数知 $a_{2m-1}$、$a_{2m}$ 可由 $a_1,\dots,a_m$ 定出。由 Entry 2(i) 知 $a_1 = \frac18$。计算中用 Ch. 3（Part I [5, p. 71]）第 14 节推论 1 的 (2.13)：$(2/(1+\sqrt{1-4a}))^n = 1 + na + n\sum_{k=2}^{\infty}\Gamma(n+2k)a^k/(\Gamma(n+k+1)k!)$（$|a| < \frac14$），及 (2.14)–(2.17)。

**(vii)** 对 $x \ge 0$，

$$F(1-e^{-8x}) = \frac12x - \frac16x^3 + \frac{31}{240}x^5 - \frac{661}{5040}x^7 + \frac{219677}{1451520}x^9 + \cdots.$$

证明：在 Entry 2(vi) 中以 $\tanh(4x)$ 代 $x$（因 $2\tanh(4x)/(1+\tanh(4x)) = 1-e^{-8x}$），再用 $\tanh(4x) = \sum_{k=1}^{\infty}2^{2k}(2^{2k}-1)B_{2k}(4x)^{2k-1}/(2k)!$（(2.19)，$|x| < \pi/2$，$B_n$ 为 Bernoulli 数）。

**例 1。** $F(0) = 0$，$F(\frac12) = e^{-\pi}$，$F(1) = 1$，$F((\sqrt{2}-1)^2) = e^{-\pi\sqrt{2}}$，$F((\sqrt{2}-1)^4) = e^{-2\pi}$。

**例 2。** 若 $0 \le x < 1$，则

$$F\left(1-\exp\left(\frac{-8x}{1-x^2}\right)\right) = \frac12x + \frac13x^3 + \frac{31}{240}x^5 + \frac{37}{2520}x^7 + \frac{5981}{1451520}x^9 + \cdots.$$

证明：在 Entry 2(vii) 中以 $x/(1-x^2)$ 代 $x$，展开 $(1-x^2)^{-2n-1}$（$0 \le n \le 4$）并合并同次项。

**状态：** 已证明（书中给出证明；(ii) 为近似式，见注记）。**对照：** M11（$F(x)$ 与椭圆模）、M02（幂级数与算法）、M01（(vii) 的 Bernoulli 数）、M04（例 1 的 $e^{-\pi}$ 等）。

**我自验：** Entry 2(i) 取 $x = 0.5$：左端 $0.0432139182638$、右端 $0.0432139182638$，差 $6.6\times 10^{-28}$（级数截断于 $k = 80$）。Entry 2(ii) 取 $x = 0.5$：左端 $0.0312094325924$、右端 $0.0312094330243$，差 $4.3\times 10^{-10}$（相对差 $1.4\times 10^{-8}$，确为近似）。Entry 2(iii) 取 $x = 0.3$：差 0。Entry 2(iv) 取 $x = 0.5$：$F(1-x) + F(1-1/x)$ 差 $8.1\times 10^{-28}$（复数解析延拓）。Entry 2(v) 取 $x = 0.4$：差 $9.2\times 10^{-33}$。Entry 2(vi) 取 $x = 0.2$：截断至 $x^9$ 的级数与左端差 $2.0\times 10^{-10}$（为 $x^{11}$ 余项量级）。Entry 2(vii) 取 $x = 0.1$：截断差 $1.9\times 10^{-12}$。例 1 三式差皆 $\le 1.4\times 10^{-32}$。例 2 取 $x = 0.2$：截断差 $4.8\times 10^{-10}$。

## 第 3 节引理

**陈述。** 若 $|q| < 1$，则

$${}_2F_1\left(\frac12,\frac12;1;1-\frac{\varphi^4(-q)}{\varphi^4(q)}\right) = \frac{\varphi^2(q)}{\varphi^2(q^2)}\,{}_2F_1\left(\frac12,\frac12;1;1-\frac{\varphi^4(-q^2)}{\varphi^4(q^2)}\right).$$

**说明。** 证明用 Ch. 11 Entry 32(iii) 的 (3.2)：${}_2F_1(\frac12,\frac12;1;1-((1-x)/(1+x))^2) = (1+x)\,{}_2F_1(\frac12,\frac12;1;x^2)$，取 $(1-x)/(1+x) = \varphi^2(-q)/\varphi^2(q)$（(3.3)），并用 Ch. 16 第 25 节推论与 Entry 25(iii) 的 $\varphi(q)\varphi(-q) = \varphi^2(-q^2)$（(3.5)）。

**状态：** 已证明（书中给出证明）。**对照：** M11、M07。

## Entry 3

**陈述。** 若 $|q| < 1$，则

$$\varphi^2(q) = {}_2F_1\left(\frac12,\frac12;1;1-\frac{\varphi^4(-q)}{\varphi^4(q)}\right).$$

**说明。** 证明：将第 3 节引理迭代 $m$ 次；若 $n = 2^m$，得 (3.7)：${}_2F_1(\frac12,\frac12;1;1-\varphi^4(-q)/\varphi^4(q)) = \varphi^2(q)/\varphi^2(q^n)\cdot{}_2F_1(\frac12,\frac12;1;1-\varphi^4(-q^n)/\varphi^4(q^n))$；令 $n\to\infty$，$\varphi(-q^n)$、$\varphi(q^n)\to 1$，即得本条。Berndt 注：引理与 Entry 3 的证明在拉马努金笔记（p. 206）中只有极简略的草图；第二本笔记后半的证明本来就极罕见。拉马努金在草图中似乎声称

$${}_2F_1\left(\frac12,\frac12;1;\left(\frac{1-x}{1+x}\right)^2\right) = \frac12(1+x)\,{}_2F_1\left(\frac12,\frac12;1;x^2\right),$$

但此式为假（右端在 $x = 0$ 解析而左端不解析）；没有证据表明拉马努金实际用过这一断言。

**状态：** 已证明（书中给出证明；拉马努金草图中的上述断言已否定）。**对照：** M11（$\varphi(q)$ 的超几何表示）、M07。

**我自验：** 取 $q = 0.5$：左端 $4.53237201426$、右端 $4.53237201426$，差 $1.5\times 10^{-27}$。

## 第 4 节引理

**陈述。** 若 $|q| < 1$，则

$${}_2F_1\left(\frac12,\frac12;1;\frac{\varphi^4(-q)}{\varphi^4(q)}\right) = \frac{\varphi^2(q)}{2\varphi^2(q^2)}\,{}_2F_1\left(\frac12,\frac12;1;\frac{\varphi^4(-q^2)}{\varphi^4(q^2)}\right).$$

**说明。** 证明用 (2.7)（取 $x = \varphi^2(-q)/\varphi^2(q)$）与 Ch. 16 Entry 25(vi) 的 $\varphi^2(q)+\varphi^2(-q) = 2\varphi^2(q^2)$（(4.1)），得 $4x/(1+x)^2 = \varphi^4(-q^2)/\varphi^4(q^2)$（(4.2)）与 $1+x = 2\varphi^2(q^2)/\varphi^2(q)$（(4.3)）。

**状态：** 已证明（书中给出证明）。**对照：** M11、M07。

## Entry 4

**陈述。** 若 $m$ 为非负整数，$n = 2^m$，则

$$\text{(i)}\quad F\left(\frac{\varphi^4(-q)}{\varphi^4(q)}\right) = F\left(\frac{\varphi^4(-q^n)}{\varphi^4(q^n)}\right)^n,$$

$$\text{(ii)}\quad F\left(1-\frac{\varphi^4(-q)}{\varphi^4(q)}\right)^n = F\left(1-\frac{\varphi^4(-q^n)}{\varphi^4(q^n)}\right).$$

**说明。** (i) 的证明：将第 4 节引理迭代 $m$ 次，得 ${}_2F_1(\frac12,\frac12;1;\varphi^4(-q)/\varphi^4(q)) = \varphi^2(q)/(n\varphi^2(q^n))\cdot{}_2F_1(\frac12,\frac12;1;\varphi^4(-q^n)/\varphi^4(q^n))$；与 (3.7) 结合得 (4.4)，乘以 $-\pi$ 再取指数即得。(ii) 由 (4.4) 直接得。Berndt 注：第 4 节诸结果的证明在拉马努金笔记中亦有草图；无疑是下面第 5 节反演公式的重要性促使拉马努金把第 3、4 节的证明草图记入笔记。

**状态：** 已证明（书中给出证明）。**对照：** M11（$F$ 的倍乘公式）、M07。

**我自验：** 取 $q = 0.5$、$n = 4$：(i) 两端皆 $6.54869848924\times 10^{-7}$，差 $3.0\times 10^{-33}$；(ii) 两端皆 $0.0625$，差 $5.6\times 10^{-29}$。

## Entry 5（反演公式）

**陈述。** 若 $|q| < 1$，则

$$F\left(1-\frac{\varphi^4(-q)}{\varphi^4(q)}\right) = q.$$

**说明。** 证明：在 Entry 4(ii) 中令 $n\to\infty$。当 $x\to 0$ 时，由 Entry 2(i) 知 $F(x)\sim x/16$；置 $\xi_n = \varphi^4(-q^n)/\varphi^4(q^n)$，则 $\lim_{n\to\infty}\sqrt[n]{F(1-\xi_n)} = \lim_{n\to\infty}\sqrt[n]{1-\xi_n}$；由 Ch. 16 Entry 25(vii)，$\lim_{n\to\infty}\frac1n\mathrm{Log}(1-\xi_n) = \mathrm{Log}\,q$（其中用 $\psi(q)$ 的 (5.1) 与 $16q^n\psi^4(q^{2n})/\varphi^4(q^n)$ 的极限），故极限为 $q$。

**状态：** 已证明（书中给出证明）。**对照：** M11（$\varphi$ 的反演公式）、M06。

**我自验：** 取 $q = 0.5$：左端 $0.5$、右端 $0.5$，差 $1.1\times 10^{-28}$。

## Entry 6

**陈述。** 在记号 (2.1) 与 (3.1) 下，

$$\varphi^2(F(x)) = {}_2F_1\left(\frac12,\frac12;1;x\right). \tag{6.1}$$

若进一步置 $z = {}_2F_1(\frac12,\frac12;1;x)$（(6.2)）与 $y = \pi\,{}_2F_1(\frac12,\frac12;1;1-x)/{}_2F_1(\frac12,\frac12;1;x)$（(6.3)），则

$$\varphi(e^{-y}) = \sqrt{z}. \tag{6.4}$$

**说明。** 证明：由 Entry 3 与 Entry 5，$\varphi^2(F(x)) = {}_2F_1(\frac12,\frac12;1;1-u)$（(6.5)）与 $F(1-u) = F(x)$，其中 $u = \varphi^4(-F(x))/\varphi^4(F(x))$；故 ${}_2F_1(\frac12,\frac12;1;u)/{}_2F_1(\frac12,\frac12;1;1-u) = {}_2F_1(\frac12,\frac12;1;1-x)/{}_2F_1(\frac12,\frac12;1;x)$（(6.6)）；由 ${}_2F_1(\frac12,\frac12;1;x)$ 在 $(0,1)$ 上单调，推出 (6.7)：${}_2F_1(\frac12,\frac12;1;1-u) = {}_2F_1(\frac12,\frac12;1;x)$，即 (6.1)。由 (2.1) 与 (6.3)，$F(x) = e^{-y}$，故 (6.1) 与 (6.4) 等价。记号 (6.2)–(6.4) 下文大量使用。

**推论。** 设 $\alpha$、$\beta > 0$，$\alpha\beta = \pi$。则 $\sqrt{\alpha}\,\varphi(e^{-\alpha^2}) = \sqrt{\beta}\,\varphi(e^{-\beta^2})$。

证明：置 $y = \alpha^2$，则 $F(x) = e^{-y}$，$F(1-x) = e^{-\pi^2/y} = e^{-\beta^2}$（(6.13)）；由 (6.1) 与 (6.3)，$\varphi^2(F(1-x))/\varphi^2(F(x)) = y/\pi = \alpha/\beta$（(6.14)）。Berndt 注：此即 $\varphi$ 的著名反演公式，亦见 Ch. 14 第 7 节（p. 169）与 Ch. 16 Entry 27(i)（p. 199）；下面的证明大概是拉马努金在此处找到的新而新颖的证明，与他先前的两个证明都不同。

**例 (i)。** $\varphi(e^{-\pi}) = \pi^{1/4}/\Gamma(\frac34)$。

证明：由例 1（第 2 节），$F(\frac12) = e^{-\pi}$；由 Entry 6，$\varphi^2(e^{-\pi}) = {}_2F_1(\frac12,\frac12;1;\frac12)$；由 (1.4)，${}_2F_1(\frac12,\frac12;1;\frac12) = \sqrt{\pi}/\Gamma^2(\frac34)$（(6.15)）。

**例 (ii)。** $\varphi(e^{-\pi\sqrt{2}}) = \frac{\Gamma(\frac98)}{\Gamma(\frac54)}\sqrt{\frac{\Gamma(\frac14)}{2^{1/4}\pi}}$。

证明：由例 1，$F((\sqrt{2}-1)^2) = e^{-\pi\sqrt{2}}$；由 Entry 6，$\varphi^2(e^{-\pi\sqrt{2}}) = {}_2F_1(\frac12,\frac12;1;(\sqrt{2}-1)^2)$（(6.16)）；用 Ch. 11 Entry 33(iv) 的 ${}_2F_1(\frac14,\frac34;1;4x/(1+x)^2) = \sqrt{1+x}\,{}_2F_1(\frac12,\frac12;1;x)$，取 $x = (\sqrt{2}-1)^2$，再用 (1.4)、倍元公式与反射公式，得 $\sqrt{4-2\sqrt{2}}\,{}_2F_1(\frac12,\frac12;1;(\sqrt{2}-1)^2) = \Gamma^2(\frac98)\sqrt{4-2\sqrt{2}}\,\Gamma(\frac14)/(\Gamma^2(\frac54)2^{1/4}\pi)$，两端除以 $\sqrt{4-2\sqrt{2}}$ 即 $\varphi^2(e^{-\pi\sqrt{2}}) = \Gamma^2(\frac98)\Gamma(\frac14)/(\Gamma^2(\frac54)2^{1/4}\pi)$。Berndt 注：拉马努金（p. 207）在表述中无意漏掉了因子 $\sqrt{\Gamma(\frac14)}/2^{1/4}$。

**例 (iii)。** $\varphi(e^{-2\pi}) = \frac{\sqrt{2+\sqrt{2}}}{2}\cdot\frac{\pi^{1/4}}{\Gamma(\frac34)}$。

证明：由例 1，$F((\sqrt{2}-1)^4) = e^{-2\pi}$；由 Entry 6，$\varphi^2(e^{-2\pi}) = {}_2F_1(\frac12,\frac12;1;(\sqrt{2}-1)^4)$（(6.17)）；用 (3.2)（取 $x = (\sqrt{2}-1)^2$）与 (1.4)，得 ${}_2F_1(\frac12,\frac12;1;(\sqrt{2}-1)^4) = (2+\sqrt{2})\sqrt{\pi}/(4\Gamma^2(\frac34))$。

**例 (iv)。** $\sum_{k=1}^{\infty}(k^2\pi-\frac14)e^{-\pi k^2} = \frac18$。

证明：在上述推论中对 $\alpha$ 求导，再取 $\alpha = \beta = \sqrt{\pi}$ 化简。

**状态：** 已证明（书中给出证明）。**对照：** M11（$\varphi(e^{-y}) = \sqrt{z}$ 与椭圆模对接）、M06（模变换）、M10（例 (i)–(iii) 的 Gamma 特殊值）、M04（$\varphi(e^{-\pi})$ 等）。

**我自验：** 取 $x = 0.4$：(6.1) 两端皆 $1.13160397766$，差 $3.9\times 10^{-31}$；(6.4) 两端皆 $1.06376876137$，差 $2.0\times 10^{-31}$。推论取 $\alpha = \beta = \sqrt{\pi}$：两端皆 $1.44640908463$，差 0。例 (i) 差 $2.0\times 10^{-31}$；例 (ii) 差 0（按 $\sqrt{\Gamma(1/4)/(2^{1/4}\pi)}$ 的读法；初版误把根号只罩 $\Gamma(1/4)$ 已纠正，见待核对清单）；例 (iii) 差 0（按 $\sqrt{2+\sqrt{2}}/2$ 的读法；初版误读作 $(\sqrt{2}+\sqrt{2})/2$ 已纠正）；例 (iv) 差 $2.5\times 10^{-32}$。

## Entry 7

**陈述。** 第 7 节收集椭圆积分的大量结果；有的很初等，有的较不初等但已知，或许有两三条是新的。以下默认参数 $x$ 的选取使积分存在，且积分上限不超过 $\pi/2$，使变量替换合法。Thiruvenkatachar 与 Venkatacahaliengar [1] 亦证明了第 7 节的部分结果。

**(i)** 若 $\sin\alpha = \sqrt{x}\sin\beta$，则

$$\int_0^{\alpha}\frac{d\varphi}{\sqrt{x-\sin^2\varphi}} = \int_0^{\beta}\frac{d\varphi}{\sqrt{1-x\sin^2\varphi}}.$$

证明：左端置 $\sin\varphi = \sqrt{x}\sin\theta$。

**(ii)** 若 $\tan\alpha = \sqrt{1-x}\tan\beta$，则

$$\int_0^{\alpha}\frac{d\varphi}{\sqrt{1-x\cos^2\varphi}} = \int_0^{\beta}\frac{d\varphi}{\sqrt{1-x\sin^2\varphi}}.$$

证明：左端置 $\tan\varphi = \sqrt{1-x}\tan\theta$。

**(iii)** 若 $\tan\alpha = \sqrt{1-b}\tan\beta$，则

$$\int_0^{\alpha}\frac{d\varphi}{\sqrt{1-\frac{a-b}{1-b}\sin^2\varphi}} = \sqrt{1-b}\int_0^{\beta}\frac{d\varphi}{\sqrt{(1-a\sin^2\varphi)(1-b\sin^2\varphi)}}.$$

证明：左端置 $\tan\varphi = \sqrt{1-b}\tan\theta$。

**(iv)** 若 $\tan\alpha = \sqrt{1+x}\tan\beta$，则

$$\int_0^{\alpha}\frac{d\varphi}{\sqrt{1+x\cos 2\varphi}} = \int_0^{\beta}\frac{d\varphi}{\sqrt{1-x^2\sin^4\varphi}}.$$

证明：左端置 $\tan\varphi = \sqrt{1+x}\tan\theta$。

**(v)** 若 $\cot\alpha\cot\beta = \sqrt{1-x}$，则

$$\int_0^{\alpha}\frac{d\varphi}{\sqrt{1-x\sin^2\varphi}} + \int_0^{\beta}\frac{d\varphi}{\sqrt{1-x\sin^2\varphi}} = \frac{\pi}{2}\,{}_2F_1\left(\frac12,\frac12;1;x\right).$$

证明：由 (6.11)，上式可写为 $\int_0^{\alpha} = \int_{\beta}^{\pi/2}$；左端置 $\cot\varphi = \sqrt{1-x}\tan\theta$。Berndt 注：下一条是加法定理的退化形式。

**(vi)** 若 $\cot\alpha\tan(\beta/2) = \sqrt{1-x\sin^2\alpha}$，则

$$2\int_0^{\alpha}\frac{d\varphi}{\sqrt{1-x\sin^2\varphi}} = \int_0^{\beta}\frac{d\varphi}{\sqrt{1-x\sin^2\varphi}}.$$

证明：Entry 7(vi) 是下面 Entry 7(viii)(a) 的逆定理的特例（(a)–(d) 既必要又充分）；取 $\beta$、$\gamma$ 分别代 $\alpha$、$\beta$ 即得。实即经典的倍乘公式（duplication formula）。

**(vii)** 若 $\alpha = \mathrm{Log}(\tan(\pi/4+\beta/2))$，则

$$\int_0^{\alpha i}\frac{d\varphi}{\sqrt{1-x\sin^2\varphi}} = i\int_0^{\beta}\frac{d\varphi}{\sqrt{1-(1-x)\sin^2\varphi}}.$$

此即 Jacobi 虚变换（Cayley [1, p. 68]）。证明：左端置 $\sin\varphi = i\tan\theta$；余下须证所给假设等价于 $\alpha = \mathrm{Log}(\cos\beta/(1-\sin\beta))$，为初等三角恒等式练习。

**(viii)** 设 $u = \int_0^{\alpha}d\varphi/\sqrt{1-x\sin^2\varphi}$，$v = \int_0^{\beta}d\varphi/\sqrt{1-x\sin^2\varphi}$，$w = \int_0^{\gamma}d\varphi/\sqrt{1-x\sin^2\varphi}$。加法定理称 $u+v = w$（(7.1)）。若 (7.1) 成立，则

$$\text{(a)}\quad \tan\frac12\gamma = \frac{\sin\alpha\sqrt{1-x\sin^2\beta}+\sin\beta\sqrt{1-x\sin^2\alpha}}{\cos\alpha+\cos\beta},$$

$$\text{(b)}\quad \gamma = \tan^{-1}(\tan\alpha\sqrt{1-x\sin^2\beta}) + \tan^{-1}(\tan\beta\sqrt{1-x\sin^2\alpha}),$$

$$\text{(c)}\quad \cot\alpha\cot\beta = \frac{\cos\gamma}{\sin\alpha\sin\beta} + \sqrt{1-x\sin^2\gamma},$$

$$\text{(d)}\quad \frac{\sqrt{\sin s\sin(s-\alpha)\sin(s-\beta)\sin(s-\gamma)}}{\sin\alpha\sin\beta\sin\gamma} = \frac{\sqrt{x}}{2},$$

其中 $2s = \alpha+\beta+\gamma$。Berndt 注：证明中的步骤可逆，故 (a)–(d) 各自都蕴含 (7.1)；(c) 为 Legendre 的加法定理标准形式。证明用 Jacobian 椭圆函数 $\mathrm{sn}$、$\mathrm{cn}$、$\mathrm{dn}$ 的理论（Whittaker–Watson [1, Chap. 22]、Cayley [1, Chap. 4]）与加法公式。

**(ix)** 若 $|x| < 1$，则

$$\frac{\pi}{2}\int_0^{\pi/2}\frac{d\varphi}{\sqrt{1+x\sin\varphi}} = \int_0^{\pi/2}\frac{\cos^{-1}(x\sin^2\varphi)}{\sqrt{1-x^2\sin^4\varphi}}\,d\varphi.$$

Berndt 注：以下给出两个证明，两个都不完全令人满意，因其本质上是验证。第一证明：展开 $(1+x\sin\varphi)^{-1/2}$ 为二项级数得 (7.2)；置 $y = \cos^{-1}u/\sqrt{1-u^2}$，$y$ 满足初值问题 $(1-u^2)y'-uy+1 = 0$、$y(0) = \pi/2$，幂级数解为 (7.3)：$\cos^{-1}u/\sqrt{1-u^2} = \frac{\pi}{2}\sum_{k=0}^{\infty}(2k)!u^{2k}/(2^{2k}(k!)^2) - \sum_{k=0}^{\infty}2^{2k}(k!)^2u^{2k+1}/(2k+1)!$，积分得 (7.4)，与 (7.2) 比较，归结为倍元公式的两个推论。第二证明：展开 $(1+x\sin\theta\sin^2\varphi)^{-1}$ 为几何级数，再与 (7.2) 比较，归结为 (7.5)：$\int_0^{\pi/2}d\theta/(1+u\sin\theta) = \cos^{-1}u/\sqrt{1-u^2}$（$|u| < 1$）。Glasser [1] 由其椭圆积分表（表 1，公式 (10)）亦可推出 Entry 7(ix)。

**(x)** 若 $|x| < 1$，则

$$\int_0^{\pi/2}\int_0^{\pi/2}\frac{d\theta\,d\varphi}{\sqrt{(1-x\sin^2\theta)(1-x\sin^2\theta\sin^2\varphi)}} = \left(\int_0^{\pi/2}\frac{d\varphi}{\sqrt{1-x\sin^4\varphi}}\right)^2.$$

证明：被积函数展开为二项级数逐项积分得 (7.6)–(7.8)；比较系数归结为恒等式 (7.9)，再用 (7.10) 的 $(a)_{n-k} = (-1)^k(a)_n/(-a-n+1)_k$ 与 $(a)_{2k} = 2^{2k}(\frac12a)_k(\frac12a+\frac12)_k$，结合 Ch. 11 的结果与 Bailey 的 ${}_4F_3$ 恒等式 (7.12)–(7.14)，证得 (7.11)：${}_4F_3[\frac14,\frac34,-n,-n;\frac14-n,\frac34-n,1] = (\frac12)_n(1)_{2n}/((\frac12)_{2n}(1)_n)\cdot{}_3F_2[\frac12,\frac12,-n;1,\frac12-n]$。

**(xi)** 若 $|x| < 1$，则

$$\int_0^{\pi/2}\int_0^{\pi/2}\frac{x\sin\varphi\,d\theta\,d\varphi}{\sqrt{(1-x^2\sin^2\varphi)(1-x^2\sin^2\theta\sin^2\varphi)}} = \int_0^{\pi/2}\int_0^{\sin^{-1}x}\frac{d\theta\,d\varphi}{\sqrt{1-x^2\sin^2\varphi-\sin^2\theta\cos^2\varphi}}$$

$$= \frac12\left(\int_0^{\pi/2}\frac{d\varphi}{\sqrt{1-\frac12(1+x)\sin^2\varphi}}\right)^2 - \frac12\left(\int_0^{\pi/2}\frac{d\varphi}{\sqrt{1-\frac12(1-x)\sin^2\varphi}}\right)^2.$$

证明：第一等式为初等变量替换（右端置 $\sin\theta = x\cos\psi/\sqrt{1-x^2\sin^2\psi}$）；第二等式用 (7.6) 展开再用二项级数，得 $I = \frac{\pi}{2}\sum_{n=0}^{\infty}(\frac12)_n/(\frac32)_n\cdot{}_3F_2[\frac12,\frac12,-n;1,1]x^{2n+1} = \frac{\pi^2}{8}\{{}_2F_1^2(\frac12,\frac12;1;\frac12(1+x)) - {}_2F_1^2(\frac12,\frac12;1;\frac12(1-x))\}$，再用 (6.11)。Berndt 注：Entry 7(x) 与 7(xi) 的证明无疑不是拉马努金本人的证明，但都依赖 Ch. 11 的结果，故拉马努金可能正是从超几何级数的这些定理出发而得到椭圆积分。

**(xii)** 若 $(1+x\sin^2\alpha)\sin\beta = (1+x)\sin\alpha$，则

$$(1+x)\int_0^{\alpha}\frac{d\varphi}{\sqrt{1-x^2\sin^2\varphi}} = \int_0^{\beta}\frac{d\varphi}{\sqrt{1-\frac{4x}{(1+x)^2}\sin^2\varphi}}.$$

此即 Gauss 变换。证明：右端被积函数置 $\sin\varphi = (1+x)\sin\theta/(1+x\sin^2\theta)$。

**(xiii)** 若 $x\sin\alpha = \sin(2\beta-\alpha)$，则

$$(1+x)\int_0^{\alpha}\frac{d\varphi}{\sqrt{1-x^2\sin^2\varphi}} = 2\int_0^{\beta}\frac{d\varphi}{\sqrt{1-\frac{4x}{(1+x)^2}\sin^2\varphi}}.$$

此即 Landen 变换（[1]、[2]），与 (xii) 外形极相似。证明：后一积分置 $x\sin\theta = \sin(2\varphi-\theta)$，即 $\varphi = \frac12(\sin^{-1}(x\sin\theta)+\theta)$。

**说明。** 拉马努金在“失落笔记”[11] 中记录了许多关于椭圆积分的深刻结果，Raghavan 与 Rangachari [1] 的论文证明了其中若干优美定理。关于椭圆积分的文献很多，最完整的表见 Byrd 与 Friedman [1]，另见 Gradshteyn–Ryzhik [1] 与 Glasser [1] 的表。

**状态：** 已证明（书中给出证明；(ix) 的两个证明 Berndt 自承皆为验证性质；(x)(xi) 的证明依赖 Ch. 11 的超几何结果，或非拉马努金原证）。**对照：** M11（椭圆积分、加法定理、Gauss 与 Landen 变换）、M09（积分）、M02（(ix)–(xi) 的超几何级数）。

**我自验：** 取 $x = 0.25$：(i)（$\beta = 0.5$）差 0；(ii)（$\beta = 0.5$）差 0；(iii)（$a = 0.3$、$b = 0.1$、$\beta = 0.5$）差 0；(iv)（$\beta = 0.5$）差 $9.9\times 10^{-32}$；(v)（$\alpha = 0.7$，$\beta$ 由 $\cot\alpha\cot\beta = \sqrt{1-x}$ 定）差 $2.0\times 10^{-31}$；(vi)（$\alpha = 0.6$，$\beta$ 由条件定）差 $2.0\times 10^{-31}$；(vii)（$\beta = 0.5$，虚轴积分）差 $9.9\times 10^{-32}$；(viii) 取 $\alpha = 0.6$、$\beta = 0.5$，由积分反解 $\gamma = 1.06901066045$，(a) 差 0、(b) 差 $1.4\times 10^{-26}$、(c) 差 $3.9\times 10^{-26}$、(d) 差 $8.1\times 10^{-26}$（25 位数值积分与反解容差）。取 $x = 0.3$：(ix) 差 0；(x) 差 $3.9\times 10^{-31}$；(xii)（$\alpha = 0.6$）差 0；(xiii)（$\alpha = 0.6$）差 0。(xi) 未逐项数值复核（见待核对清单）。

## Entry 8

**陈述。** 设 $|q| < 1$，$f(a,b)$ 如 Ch. 16 (18.1) 所定义，$\varphi(q) = f(q,q)$、$\psi(q) = f(q,q^3)$、$f(-q) = f(-q,-q^2)$（(8.1)）。则

$$\begin{aligned}
\text{(i)}\quad \varphi^2(q) &= 1 + 4\sum_{k=0}^{\infty}\frac{(-1)^kq^{2k+1}}{1-q^{2k+1}}, \\
\text{(ii)}\quad \varphi^4(q) &= 1 + 8\sum_{k=1}^{\infty}\frac{kq^k}{1+(-q)^k}, \\
\text{(iii)}\quad \varphi(q)\varphi(q^2) &= 1 - 2\sum_{k=1}^{\infty}\frac{(-1)^{k(k+1)/2}q^{2k-1}}{1-q^{2k-1}}, \\
\text{(iv)}\quad \varphi(q)\varphi(q^3) &= 1 + 2\sum_{k=1}^{\infty}\left(\frac{k}{3}\right)\frac{q^k}{1+(-q)^k},
\end{aligned}$$

其中 $(k/3)$ 为 Legendre 符号，

$$\begin{aligned}
\text{(v)}\quad \varphi^2(-q) &= 1 + 4\sum_{k=1}^{\infty}\frac{(-1)^kq^{k(k+1)/2}}{1+q^k}, \\
\text{(vi)}\quad \psi(q)\varphi(q^2) &= \sum_{k=0}^{\infty}(-1)^kq^{k(k+1)/2}\frac{1+q^{2k+1}}{1-q^{2k+1}}, \\
\text{(vii)}\quad \psi^2(q) &= \sum_{k=0}^{\infty}(-1)^kq^{k(k+1)}\frac{1+q^{2k+1}}{1-q^{2k+1}}, \\
\text{(viii)}\quad \sum_{k=1}^{\infty}\frac{kq^k}{1-q^k} &= \sum_{k=1}^{\infty}(-1)^{k+1}q^{k(k+1)/2}\frac{1+q^k}{(1-q^k)^2}, \\
\text{(ix)}\quad \varphi^2(-q)f(-q) &= \sum_{k=-\infty}^{\infty}(6k+1)q^{(3k^2+k)/2}, \\
\text{(x)}\quad \psi(q^2)f^2(-q) &= \sum_{k=-\infty}^{\infty}(3k+1)q^{3k^2+2k}, \\
\text{(xi)}\quad f(-q)f(-q^2) &= \varphi(-q)\psi(q), \\
\text{(xii)}\quad \frac{f(-q)}{f(-q^4)} &= \frac{\varphi(-q^2)}{\psi(q)}.
\end{aligned}$$

**说明。** (i) 的证明：在 Ch. 16 Entry 33(iii) 中取 $n = \pi/2$ 并以 $-q$ 代 $q^2$，得 (8.2)：$\varphi^2(q) = 1 + 4\sum_{k=1}^{\infty}q^k/(1+q^{2k})$；展开为几何级数得双重级数，按列求和即得 (i)（Jacobi [1]、[2]）。(ii) 的证明：在 Ch. 16 (33.5) 中以 $-q$ 代 $q^2$，再按列求和（Jacobi）。(iii) 的证明：用 Ch. 16 第 33 节推论（取 $a = q$、$b = q^3$）得 (8.3)，再用 Ch. 16 Entry 25(iii) 与 Entry 24(i) 得 (8.4)，按列求和。(iv) 的证明：用 Ch. 16 第 33 节推论（取 $a = q$、$b = q^2$），再用 (8.1) 与 Ch. 16 Entry 30(iv)、Entry 24(iii)，按列求和得 $\sum_{k=1}^{\infty}(q^k+(-q^2)^k)/(1+(-q)^{3k}) = \sum_{k=1}^{\infty}(k/3)q^k/(1+(-q)^k)$。(v) 的证明：由 (8.2)（$q$ 换为 $-q$），按 column–row 方法求和（Jacobi [1]、[2, p. 187] 最先发现）。(vi)(vii) 的证明：由 Ch. 16 第 33 节推论得 $\varphi^2(ab)f(-a,b)/f(a,-b) = 1 + 2\sum_{k=1}^{\infty}((-a)^k+b^k)/(1+(-ab)^k)$；交换 $a$、$b$ 相减得 $\varphi^2(ab)\{f(a,-b)/f(-a,b) - f(-a,b)/f(a,-b)\} = 4\sum_{k=1}^{\infty}(a^{2k-1}-b^{2k-1})/(1-(ab)^{2k-1})$；用 Ch. 16 Entry 30(iv)(vi) 得 (8.5)；取 $b = a^3$ 并用 Ch. 16 Entry 25(iv) 得 (8.6)：$\psi^2(a^4) = \varphi(a^4)\psi(a^8) = \sum_{k=0}^{\infty}a^{4k}/(1-a^{8k+2}) - \sum_{k=0}^{\infty}a^{4k+2}/(1-a^{8k+6})$；以 $ia$ 代 $a$ 得另一式，相加并以 $q$ 代 $a^4$ 得 (8.7)；对 (8.7) 右端两级数用 Clausen 变换即得 (vii)；再以 $\pm\sqrt{q}$ 代 $q$ 相加，用 Ch. 16 Entry 25(i)，经 Clausen 变换得 (vi)。(viii) 的证明：考虑 $\sum_{k=1}^{\infty}\{2q^{2k-1}/(1-q^{2k-1})^2 - (2k-1)q^{2k-1}/(1-q^{2k-1})\}$，按 row–column 方法变换得右端；按列求和得 $\sum_{k=1}^{\infty}q^{2k-1}/(1-q^{2k-1})^2 = \sum_{k=1}^{\infty}kq^k/(1-q^{2k})$，合并即得。(ix) 的证明：由 Ch. 16 第 34 节推论 (ii) 第一版的证明，$(q;q)_\infty(qz;q)_\infty(q/z;q)_\infty(qz^2;q^2)_\infty(q/z^2;q^2)_\infty = \sum_{k=-\infty}^{\infty}q^{(3k^2+k)/2}\sin\{(6k+1)n\}/\sin n$（$z = e^{2in}$）；令 $n\to 0$，由 Ch. 16 Entry 22(iii) 与 (22.4) 得 $\sum_{k=-\infty}^{\infty}(6k+1)q^{(3k^2+k)/2} = (q;q)_\infty^3(q;q^2)_\infty^2 = \varphi^2(-q)f(-q)$。(x) 的证明：由 Ch. 16 第 34 节推论 (i) 第一版的证明，令 $n\to 0$ 得 $\sum_{k=-\infty}^{\infty}(3k+1)q^{3k^2+2k} = (q^2;q^2)_\infty(q;q^2)_\infty^2(q^4;q^4)_\infty^2 = \psi(q^2)f^2(-q)$（Ch. 16 Entry 22(ii)(iii)）。(xi) 含于 Ch. 16 Entry 24(iii)。(xii) 的证明：先用 (xi) 与 Ch. 16 Entry 25(iii)(iv)。

**例。** $\psi(q^2)f^2(-q) + 2q\psi(q^8)f^2(-q^4) = \varphi^2(-q^8)f(-q^8)$。

证明有二：其一由 Entry 8(x) 的级数表示直接合并（大概是拉马努金本人的较短证明）；其二由 (3.1) 与 (5.1) 得 $\varphi(-q)+2q\psi(q^8) = \varphi(q^4)$，乘以 $f^2(-q^4)$ 得 (8.8)，再用 Ch. 16 Entry 22 的乘积公式化简。

**状态：** 已证明（书中给出证明；(i)(ii)(v) 属 Jacobi）。**对照：** M07（theta 函数的级数恒等式）、M06、M11。

**我自验：** 取 $q = 0.5$：(i) 左端 $4.53237201426$、右端 $4.53237201426$，差 $7.9\times 10^{-31}$（$k = 0$ 项 $(-1)^0q/(1-q) = 1$ 不可漏）；(ii) 差 0；(iii) 差 0；(iv) 差 0（Legendre 符号 $(k/3)$：$k\equiv 1\pmod 3$ 时为 $1$，$k\equiv 2\pmod 3$ 时为 $-1$，$3\mid k$ 时为 $0$）；(v) 差 $1.2\times 10^{-32}$；(vi) 差 0；(vii) 差 0；(viii) 差 $7.9\times 10^{-31}$；(ix) 差 $7.7\times 10^{-34}$；(x) 差 $3.7\times 10^{-32}$；(xi) 差 $2.5\times 10^{-32}$；(xii) 差 0；例题差 $2.0\times 10^{-31}$。

## Entry 9

**陈述。** 设 $x$、$y$、$z$ 由 (2.1) 与 (6.2)–(6.4) 联系。则

$$\text{(i)}\quad \frac{dy}{dx} = -\frac{1}{x(1-x)z^2},$$

$$\text{(ii)}\quad \frac{dz}{dx} = \frac{\int_0^x z\,dx}{4x(1-x)},$$

$$\text{(iii)}\quad z\int_0^x\left\{\int_0^u t^{n-1}z(t)\,dt\right\}\frac{du}{u(1-u)z^2(u)} = \frac{x^n}{n^2}\,{}_3F_2\left[\begin{matrix}n+\frac12, n+\frac12, 1 \\ n+1, n+1\end{matrix}; x\right],$$

其中 $n > 0$，以及

$$\text{(iv)}\quad 1 - 24\sum_{k=1}^{\infty}\frac{k}{e^{2ky}-1} = (1-2x)z^2 + 6x(1-x)z\frac{dz}{dx}.$$

**说明。** (i) 为 Ch. 11 第 30 节推论（$n = \frac12$ 的特例）。(ii) 的证明：由 L'Hôpital 法则，$\lim_{x\to 0}\int_0^x z\,dx/(4x(1-x)) = \frac14$，又 $z'(0) = \frac14$；故只需证两端导数相等，两端乘 $4x(1-x)$ 再求导得 (9.1)：$4(1-x)z' - 4xz' + 4x(1-x)z'' = z$，即 $z = {}_2F_1(\frac12,\frac12;1;x)$ 满足的超几何微分方程（Bailey [4, p. 1]；Ch. 11 Entry 31(i) 中拉马努金陈述了等价形式）。(iii) 为 Ch. 11 Entry 31(ii) 的特例（取 $\alpha = \beta = \frac12$、$\gamma = \delta = 1$，$n$ 换为 $n+1$）。(iv) 的证明：用 Ch. 16 的 Entry 22(iii)（$f(-q) = (q;q)_\infty$）、Entry 24(iv)、Entry 25(iv) 与 Entry 25(vii)，及 (6.10)、(6.4)，经对数求导的链式计算（末步用 Entry 9(i)）得 $1 - 24\sum_{k=1}^{\infty}k/(e^{2ky}-1) = -xz^2 + (1-x)z^2 + 6x(1-x)z\,dz/dx$。

**例。** 对 $y > 0$，

$$16^{11}e^{-11y} = x^{11}\left(1 + \frac{11}{2}x + \frac{1111}{64}x^2 + \frac{111111}{2688}x^3 + \cdots\right).$$

证明：在 Entry 2(vi) 中以 $x/(2-x)$ 代 $x$，得 $F(x) = x/(8(2-x)) + 5(x/(2-x))^3/128 + O(x^5)$，即 $16F(x) = x + \frac12x^2 + \frac{21}{64}x^3 + \frac{31}{128}x^4 + O(x^5)$；用 (2.1) 并取 11 次方，适量计算即得。Berndt 注：此例更宜放在第 2 节；不清楚拉马努金为何要考察 $\exp(-11y)$。

**状态：** 已证明（书中给出证明）。**对照：** M11（$y$、$z$ 的微分方程）、M06（$L(e^{-2y})$ 的公式 (9.3)）、M02（(iii) 的 ${}_3F_2$）。

**我自验：** 取 $x = 0.5$：(i) $dy/dx = -2.8710800442$，差 $3.9\times 10^{-31}$（数值微分，30 位）；(ii) $dz/dx = 0.53935260119$，差 0；(iii) 取 $n = 1$：左端 $0.72136239606$、右端 $0.72136239606$，差 0（双重数值积分，30 位）；(iv) 左端 $0.95492965855$、右端 $0.95492965855$，差 $2.0\times 10^{-31}$。例题：$x^3$ 系数经幂级数验算确为 $111111/2688$（$16F(x)$ 的系数 $1$、$1/2$、$21/64$、$31/128$ 的 11 次方展开：$11\cdot\frac{31}{128} + 55\cdot 2\cdot\frac12\cdot\frac{21}{64} + 165\cdot\frac18 = 111111/2688$；150 DPI 初版误读作 $1111111/2688$，300 DPI 放大图确认为六个 1，见待核对清单）；取 $x = 0.2$，截断至 $x^3$ 的级数与左端差 $4.1\times 10^{-9}$（为 $x^4$ 余项量级）。

## Entry 10

**陈述。** 设 $x$、$y$、$z$ 由 (2.1) 与 (6.2)–(6.4) 联系。则

$$\begin{aligned}
\text{(i)}\quad \varphi(e^{-y}) &= \sqrt{z}, \\
\text{(ii)}\quad \varphi(-e^{-y}) &= \sqrt{z}\,(1-x)^{1/4}, \\
\text{(iii)}\quad \varphi(-e^{-2y}) &= \sqrt{z}\,(1-x)^{1/8}, \\
\text{(iv)}\quad \varphi(e^{-2y}) &= \sqrt{z}\left\{\frac12(1+\sqrt{1-x})\right\}^{1/2}, \\
\text{(v)}\quad \varphi(e^{-4y}) &= \frac12\sqrt{z}\left(1+(1-x)^{1/4}\right), \\
\text{(vi)}\quad \varphi(e^{-y/2}) &= \sqrt{z}\,(1+\sqrt{x})^{1/2}, \\
\text{(vii)}\quad \varphi(-e^{-y/2}) &= \sqrt{z}\,(1-\sqrt{x})^{1/2}, \\
\text{(viii)}\quad \varphi(e^{-y/4}) &= \sqrt{z}\,(1+x^{1/4}), \\
\text{(ix)}\quad \varphi(-e^{-y/4}) &= \sqrt{z}\,(1-x^{1/4}).
\end{aligned}$$

**说明。** (i) 即 (6.4)。(ii) 的证明：由 Ch. 16 Entry 25(iii) 的 $\varphi(q)\varphi(-q) = \varphi^2(-q^2)$（(10.1)）与 (6.10)、(i)，得 $\varphi^2(-e^{-y}) = z\sqrt{1-x}$。(iii) 的证明：由 (i)（$y$ 换为 $2y$）与 (ii)，用 Entry 4(ii)（$n = 2$）得 $1-x = \varphi^4(-e^{-y})/\varphi^4(e^{-y})$，再取 8 次方根。(iv) 的证明：由 (10.2)：$\varphi^2(q)+\varphi^2(-q) = 2\varphi^2(q^2)$（Ch. 16 Entry 25(vi)），取 $q = e^{-y}$，用 (i)(ii) 与 $1-x$ 的关系。(v) 的证明：由 (iv)（$y$ 换为 $2y$）与 (iii)，用 (10.2)（$q = e^{-2y}$）。(vi)(vii) 的证明：由 (10.3)：$\varphi(\pm q) = \frac{1}{\sqrt{2}}\left(\{\varphi^2(q^2)+\varphi^2(-q^2)\}^{1/2}\pm\{\varphi^2(q^2)-\varphi^2(-q^2)\}^{1/2}\right)$（由 (10.2) 与 (10.1) 推出），取 $q = e^{-y/2}$，用 (i)(ii) 与 (6.10)。(viii)(ix) 的证明：由 (10.3) 取 $q = e^{-y/4}$，用 (iv)(iii) 与 (10.1)。

**状态：** 已证明（书中给出证明）。**对照：** M11（$\varphi(e^{-y})$ 的二分、折半求值）、M07。

**我自验：** 取 $x = 0.5$：(i) 差 $2.0\times 10^{-31}$；(ii) 差 $1.6\times 10^{-31}$；(iii) 差 $2.5\times 10^{-32}$；(iv) 差 $2.5\times 10^{-31}$；(v) 差 $1.6\times 10^{-31}$；(vi) 差 $2.4\times 10^{-32}$；(vii) 差 $2.5\times 10^{-32}$；(viii) 差 $2.2\times 10^{-31}$；(ix) 差 $7.9\times 10^{-31}$。

## Entry 11

**陈述。** 设 $\psi(q)$ 如 (5.1) 所定义，$x$、$y$、$z$ 如 (2.1) 与 (6.2)–(6.4)。则

$$\begin{aligned}
\text{(i)}\quad \psi(e^{-y}) &= \sqrt{\frac12z}\,(xe^y)^{1/8}, \\
\text{(ii)}\quad \psi(-e^{-y}) &= \sqrt{\frac12z}\,\{x(1-x)e^y\}^{1/8}, \\
\text{(iii)}\quad \psi(e^{-2y}) &= \frac12\sqrt{z}\,(xe^y)^{1/4}, \\
\text{(iv)}\quad \psi(e^{-4y}) &= \frac12\sqrt{\frac12z}\,\{(1-\sqrt{1-x})e^y\}^{1/2}, \\
\text{(v)}\quad \psi(e^{-8y}) &= \frac14\sqrt{z}\,\{1-(1-x)^{1/4}\}e^y, \\
\text{(vi)}\quad \psi(e^{-y/2}) &= \sqrt{z}\left\{\frac12(1+\sqrt{x})\right\}^{1/4}(xe^y)^{1/16}, \\
\text{(vii)}\quad \psi(-e^{-y/2}) &= \sqrt{z}\left\{\frac12(1-\sqrt{x})\right\}^{1/4}(xe^y)^{1/16}, \\
\text{(viii)}\quad \psi(e^{-y/4}) &= \sqrt{z}\,(1+x^{1/4})^{1/2}\left\{\frac12(1+\sqrt{x})\right\}^{1/8}(xe^y)^{1/32}, \\
\text{(ix)}\quad \psi(-e^{-y/4}) &= \sqrt{z}\,(1-x^{1/4})^{1/2}\left\{\frac12(1+\sqrt{x})\right\}^{1/8}(xe^y)^{1/32}.
\end{aligned}$$

**说明。** 证明用 (11.1)：$\psi(q^2) = \frac12q^{-1/4}(\varphi^4(q)-\varphi^4(-q))^{1/4}$（Ch. 16 Entry 24(iv) 与 Entry 25(iii)）；(11.2)：$\psi(q^8) = \frac{1}{4q}(\varphi(q)-\varphi(-q))$（Ch. 16 Entry 24(iv)(ii) 与 Entry 25(iv)）；(11.3)：$\psi(q) = \sqrt{\varphi(q)\psi(q^2)}$（Ch. 16 Entry 25(vii)）。(i) 的证明：由 (11.1)（$q = e^{-y}$）与 Entry 10(i)(ii)。(ii) 的证明：由 (11.1)（$q = -e^{-y}$）与 (10.1)。(iii) 的证明：由 (11.1)（$q = e^{-2y}$）与 (11.3)、(6.4)。(iv) 的证明：由 (11.1)（$q = e^{-4y}$）与 Entry 10(iv)(v)。(v) 的证明：由 (11.2)（$q = e^{-y}$）与 Entry 10(i)(ii)。(vi)(vii) 的证明：由 (11.3)（$q = e^{-y/2}$）与 Entry 10(vi)(vii)、Entry 11(iii)。(viii)(ix) 的证明：由 (11.3)（$q = e^{-y/4}$）与 Entry 10(viii)(ix)、Entry 11(vi)。

**状态：** 已证明（书中给出证明）。**对照：** M11、M07。

**我自验：** 取 $x = 0.5$：(i) 差 $1.2\times 10^{-31}$；(ii) 差 $2.2\times 10^{-31}$；(iii) 差 0；(iv) 差 $2.0\times 10^{-31}$；(v) 差 $3.1\times 10^{-31}$；(vi) 差 $6.3\times 10^{-31}$；(vii) 差 $1.2\times 10^{-31}$；(viii) 差 $3.9\times 10^{-31}$；(ix) 差 $7.3\times 10^{-31}$。

## Entry 12

**陈述。** 设 $f$ 如 Ch. 16 (18.1) 所定义，$\chi(q) = (-q;q^2)_\infty$（(12.1)），$x$、$y$、$z$ 如 (2.1) 与 (6.2)–(6.4)。则

$$\begin{aligned}
\text{(i)}\quad f(e^{-y}) &= \sqrt{z}\,2^{-1/6}\{x(1-x)e^y\}^{1/24}, \\
\text{(ii)}\quad f(-e^{-y}) &= \sqrt{z}\,2^{-1/6}(1-x)^{1/6}(xe^y)^{1/24}, \\
\text{(iii)}\quad f(-e^{-2y}) &= \sqrt{z}\,2^{-1/3}\{x(1-x)e^y\}^{1/12}, \\
\text{(iv)}\quad f(-e^{-4y}) &= \sqrt{z}\,4^{-1/3}(1-x)^{1/24}(xe^y)^{1/6}, \\
\text{(v)}\quad \chi(e^{-y}) &= 2^{1/6}\{x(1-x)e^y\}^{-1/24}, \\
\text{(vi)}\quad \chi(-e^{-y}) &= 2^{1/6}(1-x)^{1/12}(xe^y)^{-1/24}, \\
\text{(vii)}\quad \chi(-e^{-2y}) &= 2^{1/3}(1-x)^{1/24}(xe^y)^{-1/12}.
\end{aligned}$$

**说明。** 证明用 (12.2)：$f^3(-q) = \varphi^2(-q)\psi(q)$（Ch. 16 Entry 24(ii)），(12.3)：$f^3(-q^2) = \varphi(-q)\psi^2(q)$（Ch. 16 Entry 24(iv)），(12.4)：$\chi(q) = \varphi(q)/f(q)$（Ch. 16 Entry 24(ii)(iv)(iii)）。(i) 的证明：由 (12.2)（$q = -e^{-y}$）与 Entry 10(ii)、Entry 11(ii)。(ii) 的证明：由 (12.2)（$q = e^{-y}$）与 Entry 10(i)、Entry 11(i)。(iii) 的证明：由 (12.3)（$q = e^{-y}$）与 Entry 10(ii)、Entry 11(i)。(iv) 的证明：由 (12.3)（$q = e^{-2y}$）与 Entry 10(iii)、Entry 11(iii)。(v)–(vii) 的证明：由 (12.4) 与 Entry 10、Entry 12(i)–(iii)。

**状态：** 已证明（书中给出证明）。**对照：** M11、M07（$f$、$\chi$ 的求值）。

**我自验：** 取 $x = 0.5$：(i) 差 $1.2\times 10^{-31}$；(ii) 差 $7.9\times 10^{-31}$；(iii) 差 $3.9\times 10^{-31}$；(iv) 差 $2.5\times 10^{-31}$；(v) 差 $1.6\times 10^{-31}$；(vi) 差 $7.9\times 10^{-31}$；(vii) 差 $2.5\times 10^{-31}$。

## Entry 13

**陈述。** 设 $L$、$M$、$N$ 如 Ch. 15 第 9 节与本章第 13 节所定义（$L(q) = 1 - 24\sum_{k=1}^{\infty}kq^k/(1-q^k)$、$M(q) = 1 + 240\sum_{k=1}^{\infty}k^3q^k/(1-q^k)$、$N(q) = 1 - 504\sum_{k=1}^{\infty}k^5q^k/(1-q^k)$），$x$、$y$、$z$ 如 (2.1) 与 (6.2)–(6.4)。则

$$\begin{aligned}
\text{(i)}\quad M(e^{-2y}) &= z^4(1-x+x^2), \\
\text{(ii)}\quad N(e^{-2y}) &= z^6(1+x)(1-\tfrac12x)(1-2x), \\
\text{(iii)}\quad M(e^{-y}) &= z^4(1+14x+x^2), \\
\text{(iv)}\quad N(e^{-y}) &= z^6(1+x)(1-34x+x^2), \\
\text{(v)}\quad M(e^{-4y}) &= z^4(1-x+\tfrac{1}{16}x^2), \\
\text{(vi)}\quad N(e^{-4y}) &= z^6(1-\tfrac12x)(1-x-\tfrac{1}{32}x^2),
\end{aligned}$$

$$\text{(vii)}\quad \text{若 } x \text{ 变为 } \left(\frac{1-\sqrt{1-x}}{1+\sqrt{1-x}}\right)^2 \text{，则 } y \text{ 变为 } 2y，$$

$$\begin{aligned}
\text{(viii)}\quad 2L(e^{-2y})-L(e^{-y}) &= 1 + 24\sum_{k=1}^{\infty}\frac{k}{e^{ky}+1} = z^2(1+x), \\
\text{(ix)}\quad 2L(e^{-4y})-L(e^{-2y}) &= 1 + 24\sum_{k=1}^{\infty}\frac{k}{e^{2ky}+1} = z^2(1-\tfrac12x), \\
\text{(x)}\quad 2M(e^{-2y})-M(e^{-y}) &= 1 - 240\sum_{k=1}^{\infty}\frac{k^3}{e^{ky}+1} = z^4(1-16x+x^2), \\
\text{(xi)}\quad 2N(e^{-2y})-N(e^{-y}) &= 1 + 504\sum_{k=1}^{\infty}\frac{k^5}{e^{ky}+1} = z^6(1+x)(1+29x+x^2), \\
\text{(xii)}\quad 2M(e^{-4y})-M(e^{-2y}) &= 1 - 240\sum_{k=1}^{\infty}\frac{k^3}{e^{2ky}+1} = z^4(1-x-\tfrac78x^2), \\
\text{(xiii)}\quad 2N(e^{-4y})-N(e^{-2y}) &= 1 + 504\sum_{k=1}^{\infty}\frac{k^5}{e^{2ky}+1} = z^6(1-\tfrac12x)(1-x+\tfrac{31}{16}x^2).
\end{aligned}$$

**说明。** (i) 的证明：由 Ch. 15 第 13 节的 $t\,dL/dt = (L^2-M)/12$（$t = e^{-2y}$），经链式法则与 Entry 9(i) 得 (13.3)：$-x(1-x)z^2\,dL(e^{-2y})/dx = (M(e^{-2y})-L^2(e^{-2y}))/6$；由 (9.3) 与超几何微分方程 (9.1) 直接计算得 (13.4)：$dL(e^{-2y})/dx$ 的表达式；代入 (13.3) 并用 (9.1) 化简即得 (i)。(ii) 的证明类似：由 Ch. 15 第 13 节的 $t\,dM/dt = (LM-N)/3$，经链式法则与 Entry 9(i) 得 $-3x(1-x)z^2\,dM(e^{-2y})/dx = 2N(e^{-2y})-2L(e^{-2y})M(e^{-2y})$；解出 $N(e^{-2y})$，用 (9.3) 与 Entry 13(i) 即得 (ii)。(iii)(iv) 的证明：对 (i)(ii) 用 dimidiation。(v)(vi) 的证明：对 (i)(ii) 用 duplication。(vii) 为 duplication 变换的文字表述。(viii) 的证明：初等计算得 $2L(e^{-2y})-L(e^{-y}) = 1 + 24\sum_{k=1}^{\infty}k/(e^{ky}+1)$；$L(e^{-y})$ 的值由 Ch. 16 Entry 24(ii)、25(iv)、25(vii) 与 (6.4)、(6.10)（或 Entry 10(i)(ii)）经对数求导算出（(13.5)），与 (9.3) 联立即得。(ix) 的证明：对 (viii) 用 duplication。(x) 的证明：初等计算得 (13.6)：$1 - 240\sum_{k=1}^{\infty}k^3/(e^{ky}+1) = 2M(e^{-2y})-M(e^{-y})$；用 (i)(iii) 完成。(xi) 的证明：初等计算得 (13.7)：$1 + 504\sum_{k=1}^{\infty}k^5/(e^{ky}+1) = 2N(e^{-2y})-N(e^{-y})$；用 (ii)(iv) 完成。(xii) 的证明：(13.6) 中 $y$ 换为 $2y$，用 (i)(v)。(xiii) 的证明：(13.7) 中 $y$ 换为 $2y$，用 (ii)(vi)。

**状态：** 已证明（书中给出证明；(vii) 为 duplication 变换的文字表述，无公式可验）。**对照：** M06（$L$、$M$、$N$ Eisenstein 级数与 duplication）、M11、M02。

**我自验：** 取 $x = 0.5$：(i) 差 $6.3\times 10^{-32}$；(iii) 差 $1.6\times 10^{-31}$；(iv) 差 $2.0\times 10^{-31}$；(v) 差 $6.3\times 10^{-31}$；(vi) 差 $3.1\times 10^{-31}$；(viii) 差 $7.9\times 10^{-32}$；(ix) 差 $7.9\times 10^{-31}$；(x) 差 $1.2\times 10^{-30}$；(xi) 差 $2.4\times 10^{-31}$；(xii) 差 $2.5\times 10^{-31}$；(xiii) 差 $1.6\times 10^{-31}$。(ii) 在 $x = 0.5$ 时两端同为 $0$（因子 $1-2x = 0$），改取 $x = 0.3$：差 $2.5\times 10^{-31}$。

## Entry 14

**陈述。** 设 $x$、$y$、$z$ 如 (2.1) 与 (6.2)–(6.4)。则

$$\begin{aligned}
\text{(i)}\quad 1 - 8\sum_{k=1}^{\infty}(-1)^{k-1}\frac{k}{e^{ky}+1} &= z^2(1-x), \\
\text{(ii)}\quad 1 + 16\sum_{k=1}^{\infty}(-1)^{k-1}\frac{k^3}{e^{ky}+1} &= z^4(1-x^2), \\
\text{(iii)}\quad 1 - 8\sum_{k=1}^{\infty}(-1)^{k-1}\frac{k^5}{e^{ky}+1} &= z^6(1-x)(1-x+x^2), \\
\text{(iv)}\quad 17 + 32\sum_{k=1}^{\infty}(-1)^{k-1}\frac{k^7}{e^{ky}+1} &= z^8(1-x^2)(17-32x+17x^2), \\
\text{(v)}\quad 1 - 16\sum_{k=1}^{\infty}(-1)^{k-1}\frac{k^3}{e^{ky}-1} &= z^4(1-x)^2, \\
\text{(vi)}\quad 1 + 8\sum_{k=1}^{\infty}(-1)^{k-1}\frac{k^5}{e^{ky}-1} &= z^6(1-x)(1-x^2), \\
\text{(vii)}\quad 17 - 32\sum_{k=1}^{\infty}(-1)^{k-1}\frac{k^7}{e^{ky}-1} &= z^8(1-x)^2(17-2x+17x^2), \\
\text{(viii)}\quad 31 + 8\sum_{k=1}^{\infty}(-1)^{k-1}\frac{k^9}{e^{ky}-1} &= z^{10}(1-x)(1-x^2)(31-46x+31x^2), \\
\text{(ix)}\quad 1 - 16\sum_{k=1}^{\infty}(-1)^{k-1}\frac{k^3}{e^{2ky}-1} &= z^4(1-x), \\
\text{(x)}\quad 1 + 8\sum_{k=1}^{\infty}(-1)^{k-1}\frac{k^5}{e^{2ky}-1} &= z^6(1-x)(1-\tfrac12x), \\
\text{(xi)}\quad 17 - 32\sum_{k=1}^{\infty}(-1)^{k-1}\frac{k^7}{e^{2ky}-1} &= z^8(1-x)(17-17x+2x^2),
\end{aligned}$$

$$\text{(xii)}\quad \text{若 } x \text{ 变为 } -x/(1-x) \text{，则 } e^{-y} \text{ 变为 } -e^{-y}。$$

**说明。** (i) 的证明：初等计算得 $3\left(1 - 8\sum_{k=1}^{\infty}(-1)^{k-1}k/(e^{ky}+1)\right) = 4\left(1 + 24\sum_{k=1}^{\infty}k/(e^{2ky}+1)\right) - \left(1 + 24\sum_{k=1}^{\infty}k/(e^{ky}+1)\right)$；用 Entry 13(viii)(ix) 完成。(ii) 的证明：初等计算得 $15\left(1 + 16\sum_{k=1}^{\infty}(-1)^{k-1}k^3/(e^{ky}+1)\right) = 16\left(1 - 240\sum_{k=1}^{\infty}k^3/(e^{2ky}+1)\right) - \left(1 - 240\sum_{k=1}^{\infty}k^3/(e^{ky}+1)\right)$；用 Entry 13(x)(xii) 完成。(iii) 的证明：初等计算得 $63\left(1 - 8\sum_{k=1}^{\infty}(-1)^{k-1}k^5/(e^{ky}+1)\right) = 64\left(1 + 504\sum_{k=1}^{\infty}k^5/(e^{2ky}+1)\right) - \left(1 + 504\sum_{k=1}^{\infty}k^5/(e^{ky}+1)\right)$；用 Entry 13(xi)(xiii) 完成。(iv) 的证明：由 Ch. 15 Entry 12(ii) 的 (14.1)：$M^2(e^{-2y}) = 1 + 480\sum_{k=1}^{\infty}k^7/(e^{2ky}-1)$；初等计算得 $256\{2M^2(e^{-4y})-M^2(e^{-2y})\} - \{2M^2(e^{-2y})-M^2(e^{-y})\} = 15\left(17 + 32\sum_{k=1}^{\infty}(-1)^{k-1}k^7/(e^{ky}+1)\right)$（已数值核对）；用 Entry 13(i)(iii)(v) 完成。Berndt 注：拉马努金（p. 212）在 (iv) 中无意把 $17-32x+17x^2$ 写成了 $17-32x+x^2$。(v) 的证明：初等计算得 $16M(e^{-2y})-M(e^{-y}) = 15\left(1 - 16\sum_{k=1}^{\infty}(-1)^{k-1}k^3/(e^{ky}-1)\right)$；用 Entry 13(i)(iii) 完成。(vi) 的证明：初等计算得 $64N(e^{-2y})-N(e^{-y}) = 63\left(1 + 8\sum_{k=1}^{\infty}(-1)^{k-1}k^5/(e^{ky}-1)\right)$；用 Entry 13(ii)(iv) 完成。(vii) 的证明：由 (14.1)，$256M^2(e^{-2y})-M^2(e^{-y}) = 15\left(17 - 32\sum_{k=1}^{\infty}(-1)^{k-1}k^7/(e^{ky}-1)\right)$；用 Entry 13(i)(iii) 完成。(viii) 的证明：由 Ch. 15 Entry 12(iii) 的 $MN$ 恒等式 $M(e^{-2y})N(e^{-2y}) = 1 - 264\sum_{k=1}^{\infty}k^9/(e^{2ky}-1)$，得 $1024M(e^{-2y})N(e^{-2y})-M(e^{-y})N(e^{-y}) = 33\left(31 + 8\sum_{k=1}^{\infty}(-1)^{k-1}k^9/(e^{ky}-1)\right)$（已数值核对）；用 Entry 13(i)–(iv) 完成。(ix)–(xi) 的证明：对 (v)(vi)(vii) 用 duplication 变换。(xii) 为 change of sign 变换的文字表述。

**状态：** 已证明（书中给出证明；(xii) 为 change of sign 变换的文字表述）。**对照：** M06（$L$、$M$、$N$ 的 $e^{ky}\pm 1$ 级数）、M11、M02。

**我自验：** 取 $x = 0.5$：(i) 差 $2.0\times 10^{-31}$；(ii) 差 $3.1\times 10^{-31}$；(iii) 差 $3.9\times 10^{-31}$；(iv) 差 $3.1\times 10^{-31}$；(v) 差 $6.3\times 10^{-31}$（按 $(1-x)^2$ 的读法；150 DPI 初版误读作 $(1-x^2)$，300 DPI 放大图确认为 $(1-x)^2$，见待核对清单）；(vi) 差 $6.3\times 10^{-31}$；(vii) 差 $7.9\times 10^{-31}$；(viii) 差 $3.1\times 10^{-31}$；(ix) 差 $2.5\times 10^{-31}$；(x) 差 $2.5\times 10^{-31}$；(xi) 差 $3.1\times 10^{-31}$。

## Entry 15

**陈述。** 设 $x$、$y$、$z$ 如 (2.1) 与 (6.2)–(6.4)。则

$$\begin{aligned}
\text{(i)}\quad \sum_{k=1}^{\infty}\frac{k^3}{\sinh(ky)} &= \frac18z^4x, \\
\text{(ii)}\quad \sum_{k=1}^{\infty}\frac{k^5}{\sinh(ky)} &= \frac18z^6x(1+x), \\
\text{(iii)}\quad \sum_{k=1}^{\infty}\frac{k^7}{\sinh(ky)} &= \frac18z^8x\left(1+\frac{13}{2}x+x^2\right), \\
\text{(iv)}\quad \sum_{k=1}^{\infty}\frac{k^9}{\sinh(ky)} &= \frac18z^{10}x(1+x)(1+29x+x^2), \\
\text{(v)}\quad \sum_{k=1}^{\infty}\frac{k^3}{\sinh(2ky)} &= \frac{1}{128}z^4x^2, \\
\text{(vi)}\quad \sum_{k=1}^{\infty}\frac{k^5}{\sinh(2ky)} &= \frac{1}{128}z^6x^2\left(1-\frac12x\right), \\
\text{(vii)}\quad \sum_{k=1}^{\infty}\frac{k^7}{\sinh(2ky)} &= \frac{1}{128}z^8x^2\left(1-x+\frac{17}{32}x^2\right), \\
\text{(viii)}\quad \sum_{k=1}^{\infty}\frac{k^9}{\sinh(2ky)} &= \frac{1}{128}z^{10}x^2\left(1-\frac12x\right)\left(1-x+\frac{31}{16}x^2\right), \\
\text{(ix)}\quad \sum_{k=0}^{\infty}\frac{2k+1}{\sinh((2k+1)y)} &= \frac18z^2x, \\
\text{(x)}\quad \sum_{k=0}^{\infty}\frac{(2k+1)^3}{\sinh((2k+1)y)} &= \frac18z^4x\left(1-\frac12x\right), \\
\text{(xi)}\quad \sum_{k=0}^{\infty}\frac{(2k+1)^5}{\sinh((2k+1)y)} &= \frac18z^6x(1-x+x^2), \\
\text{(xii)}\quad \sum_{k=0}^{\infty}\frac{(2k+1)^7}{\sinh((2k+1)y)} &= \frac18z^8x\left(1-\frac12x\right)\left(1-x+\frac{17}{2}x^2\right), \\
\text{(xiii)}\quad \sum_{k=0}^{\infty}\frac{2k+1}{\sinh(\frac12(2k+1)y)} &= \frac12z^2\sqrt{x}, \\
\text{(xiv)}\quad \sum_{k=0}^{\infty}\frac{(2k+1)^3}{\sinh(\frac12(2k+1)y)} &= \frac12z^4(1+x)\sqrt{x}, \\
\text{(xv)}\quad \sum_{k=0}^{\infty}\frac{(2k+1)^5}{\sinh(\frac12(2k+1)y)} &= \frac12z^6(1+14x+x^2)\sqrt{x}, \\
\text{(xvi)}\quad \sum_{k=0}^{\infty}\frac{(2k+1)^7}{\sinh(\frac12(2k+1)y)} &= \frac12z^8(1+x)(1+134x+x^2)\sqrt{x}.
\end{aligned}$$

**说明。** (i) 的证明：$\sum_{k=1}^{\infty}k^3/\sinh(ky) = \frac{1}{120}\{M(e^{-y})-M(e^{-2y})\}$；用 Entry 13(i)(iii) 完成（系数 $1/120$ 已数值核对）。(ii) 的证明：$\sum_{k=1}^{\infty}k^5/\sinh(ky) = -\frac{1}{252}\{N(e^{-y})-N(e^{-2y})\}$；用 Entry 13(ii)(iv) 完成（系数 $-1/252$ 已数值核对）。(iii) 的证明：$\sum_{k=1}^{\infty}k^7/\sinh(ky) = \frac{1}{240}\{M^2(e^{-y})-M^2(e^{-2y})\}$；用 Entry 13(i)(iii) 完成（系数 $1/240$ 已数值核对）。(iv) 的证明：$\sum_{k=1}^{\infty}k^9/\sinh(ky) = -\frac{1}{132}\{M(e^{-y})N(e^{-y})-M(e^{-2y})N(e^{-2y})\}$；用 Entry 13(i)–(iv) 完成（系数 $-1/132$ 已数值核对）。(v)–(viii) 的证明：对 (i)–(iv) 用 duplication。(ix) 的证明：直接计算得 $\sum_{k=0}^{\infty}(2k+1)/\sinh((2k+1)y) = \frac{1}{12}\{L(e^{-2y})-L(e^{-y})\} - \frac16\{L(e^{-4y})-L(e^{-2y})\} = \frac{1}{12}\{2L(e^{-2y})-L(e^{-y})\} - \frac{1}{12}\{2L(e^{-4y})-L(e^{-2y})\}$（系数已数值核对）；用 Entry 13(viii)(ix) 完成。(x)–(xii) 的证明：由 $\sum_{k=0}^{\infty}(2k+1)^{2n+1}/\sinh((2k+1)y) = \sum_{k=1}^{\infty}k^{2n+1}/\sinh(ky) - \sum_{k=1}^{\infty}(2k)^{2n+1}/\sinh(2ky)$（奇数项 = 全体减偶数项），用 (ii)(vi) 等完成。(xiii)–(xvi) 的证明：对 (ix)–(xii) 用 dimidiation。

**状态：** 已证明（书中给出证明）。**对照：** M02（$\sinh$ 级数求值）、M06（$M$、$N$ 的应用）、M11。

**我自验：** 取 $x = 0.5$：(i) 差 $6.3\times 10^{-32}$；(ii) 差 $2.5\times 10^{-31}$；(iii) 差 $1.6\times 10^{-31}$；(iv) 差 $7.9\times 10^{-31}$；(v) 差 $2.5\times 10^{-32}$；(vi) 差 $6.3\times 10^{-32}$；(vii) 差 $6.3\times 10^{-32}$；(viii) 差 $2.5\times 10^{-31}$；(ix) 差 $6.3\times 10^{-32}$；(x) 差 $3.1\times 10^{-31}$；(xi) 差 $1.2\times 10^{-31}$；(xii) 差 $6.3\times 10^{-31}$；(xiii) 差 $2.5\times 10^{-31}$；(xiv) 差 $6.3\times 10^{-31}$；(xv) 差 $2.5\times 10^{-31}$；(xvi) 差 $1.2\times 10^{-30}$。

## Entry 16

**陈述。** 设 $x$、$y$、$z$ 如 (2.1) 与 (6.2)–(6.4)。则

$$\begin{aligned}
\text{(i)}\quad \sum_{k=0}^{\infty}\frac{(-1)^k(2k+1)}{\cosh(\frac12(2k+1)y)} &= \frac12z^2\sqrt{x(1-x)}, \\
\text{(ii)}\quad \sum_{k=0}^{\infty}\frac{(-1)^k(2k+1)^3}{\cosh(\frac12(2k+1)y)} &= \frac12z^4(1-2x)\sqrt{x(1-x)}, \\
\text{(iii)}\quad \sum_{k=0}^{\infty}\frac{(-1)^k(2k+1)^5}{\cosh(\frac12(2k+1)y)} &= \frac12z^6\{1-16x(1-x)\}\sqrt{x(1-x)}, \\
\text{(iv)}\quad \sum_{k=0}^{\infty}\frac{(-1)^k(2k+1)^7}{\cosh(\frac12(2k+1)y)} &= \frac12z^8(1-2x)\{1-136x(1-x)\}\sqrt{x(1-x)}, \\
\text{(v)}\quad \sum_{k=0}^{\infty}\frac{(-1)^k(2k+1)^9}{\cosh(\frac12(2k+1)y)} &= \frac12z^{10}\{1-1232x(1-x)+7936x^2(1-x)^2\}\sqrt{x(1-x)}, \\
\text{(vi)}\quad \sum_{k=0}^{\infty}\frac{(-1)^k(2k+1)^{11}}{\cosh(\frac12(2k+1)y)} &= \frac12z^{12}(1-2x)\{1-11072x(1-x)+176896x^2(1-x)^2\}\sqrt{x(1-x)},
\end{aligned}$$

$$\text{(vii)}\quad \sum_{k=0}^{\infty}(-1)^k\tan^{-1}e^{-(2k+1)y/2} = \frac14\sin^{-1}\sqrt{x},$$

$$\text{(viii)}\quad \sum_{k=0}^{\infty}(-1)^k\tan^{-1}e^{-(2k+1)y/4} = \frac12\tan^{-1}x^{1/4},$$

$$\begin{aligned}
\text{(ix)}\quad \sum_{k=0}^{\infty}\frac{1}{\cosh(\frac12(2k+1)y)} &= \frac12z\sqrt{x}, \\
\text{(x)}\quad \sum_{k=0}^{\infty}\frac{(2k+1)^2}{\cosh(\frac12(2k+1)y)} &= \frac12z^3\sqrt{x}, \\
\text{(xi)}\quad \sum_{k=0}^{\infty}\frac{(2k+1)^4}{\cosh(\frac12(2k+1)y)} &= \frac12z^5(1+4x)\sqrt{x}, \\
\text{(xii)}\quad \sum_{k=0}^{\infty}\frac{(2k+1)^6}{\cosh(\frac12(2k+1)y)} &= \frac12z^7\{1+11(4x)+(4x)^2\}\sqrt{x}, \\
\text{(xiii)}\quad \sum_{k=0}^{\infty}\frac{(2k+1)^8}{\cosh(\frac12(2k+1)y)} &= \frac12z^9\{1+102(4x)+57(4x)^2+(4x)^3\}\sqrt{x}.
\end{aligned}$$

**说明。** (i)–(iv) 的证明：对 Entry 15(xiii)–(xvi) 用 change of sign，由 (16.1)（$\sum_{k=0}^{\infty}(-1)^k(2k+1)^n/\cosh(\frac12(2k+1)y)$ 与 $\sinh$ 级数的关系，$n = 1,3,5,7$）即得。(v)(vi) 的证明：用 Hermite 的 $\mathrm{sn}\,u$ 展开 (16.2)（Cayley [1, p. 56]）与 Jacobi 的 $\mathrm{sn}\,u$ Fourier 级数 (16.3)（Whittaker–Watson [1, p. 510]）；比较 $u^9$、$u^{11}$ 的系数得 (16.4)、(16.5)，再用 change of sign。Berndt 注：(v)(vi) 的出现颇为神秘——证明所需的中间结果（含十一次幂的级数）拉马努金在本章此前并未给出；Berndt 改用 $\mathrm{sn}$ 的 Fourier 级数证明，并指出第 13–17 节的大多数结果都可用相应椭圆函数的 Fourier 级数同样建立。(vii) 的证明：对 Entry 16(i) 在 $[0,y]$ 上积分（(16.6)、(16.7)，后者用 Entry 9(i) 与两次变量替换）；Jacobi [1]、[2, p. 164] 最先发现，Jacobi 称此式为“在最优美的公式中应占一席之地者”。(viii) 的证明：对 (vii) 用 dimidiation，须证 $\frac12\sin^{-1}(2x^{1/4}/(1+\sqrt{x})) = \tan^{-1}x^{1/4}$（留作练习）。(ix)–(xiii) 的证明：对 Entry 17(i)–(v) 分别用 duplication，再与 Entry 17(i)–(v) 相减得 $\cosh((2k+1)y)$ 的级数，最后用 dimidiation。

**状态：** 已证明（书中给出证明；(vii) 属 Jacobi）。**对照：** M02（$\cosh$ 级数求值）、M11（$\mathrm{sn}$、$\mathrm{dn}$ 的 Fourier 级数）。

**我自验：** 取 $x = 0.5$：(i) 差 $6.3\times 10^{-32}$；(iii) 差 $3.1\times 10^{-31}$；(v) 差 $2.5\times 10^{-31}$；(vii) 差 $3.1\times 10^{-31}$；(viii) 差 $6.3\times 10^{-31}$；(ix) 差 $2.5\times 10^{-31}$；(x) 差 $1.6\times 10^{-31}$；(xi) 差 $3.1\times 10^{-31}$；(xii) 差 $1.6\times 10^{-31}$；(xiii) 差 $3.1\times 10^{-31}$。(ii)(iv)(vi) 在 $x = 0.5$ 时两端同为 $0$（因子 $1-2x = 0$），改取 $x = 0.3$：(ii) 差 $2.5\times 10^{-31}$，(iv) 差 $6.3\times 10^{-31}$，(vi) 差 $7.1\times 10^{-30}$。

## Entry 17

**陈述。** 设 $x$、$y$、$z$ 如 (2.1) 与 (6.2)–(6.4)。则

$$\begin{aligned}
\text{(i)}\quad 1 + 2\sum_{k=1}^{\infty}\frac{1}{\cosh(ky)} &= z, \\
\text{(ii)}\quad \sum_{k=1}^{\infty}\frac{k^2}{\cosh(ky)} &= \frac18z^3x, \\
\text{(iii)}\quad \sum_{k=1}^{\infty}\frac{k^4}{\cosh(ky)} &= \frac12z^5\left(\frac{x}{4}+\left(\frac{x}{4}\right)^2\right), \\
\text{(iv)}\quad \sum_{k=1}^{\infty}\frac{k^6}{\cosh(ky)} &= \frac12z^7\left(\frac{x}{4}+11\left(\frac{x}{4}\right)^2+\left(\frac{x}{4}\right)^3\right), \\
\text{(v)}\quad \sum_{k=1}^{\infty}\frac{k^8}{\cosh(ky)} &= \frac12z^9\left(\frac{x}{4}+57\left(\frac{x}{4}\right)^2+102\left(\frac{x}{4}\right)^3+\left(\frac{x}{4}\right)^4\right),
\end{aligned}$$

$$\begin{aligned}
\text{(vi)}\quad 1 + 4\sum_{k=0}^{\infty}\frac{(-1)^k}{e^{(2k+1)y}-1} &= z, \\
\text{(vii)}\quad 1 - 4\sum_{k=0}^{\infty}\frac{(-1)^k(2k+1)^2}{e^{(2k+1)y}-1} &= z^3(1-x), \\
\text{(viii)}\quad 5 + 4\sum_{k=0}^{\infty}\frac{(-1)^k(2k+1)^4}{e^{(2k+1)y}-1} &= z^5(5-x)(1-x), \\
\text{(ix)}\quad 61 - 4\sum_{k=0}^{\infty}\frac{(-1)^k(2k+1)^6}{e^{(2k+1)y}-1} &= z^7(1-x)(61-46x+x^2).
\end{aligned}$$

**说明。** (i)–(v) 的证明：由 Cayley [1, p. 57] 的 $\mathrm{dn}\,u$ 展开 (17.1)（Berndt 纠正了 Cayley 的一处小印误：右端第一项应为 $1$ 而非 $u$）与 Whittaker–Watson [1, p. 511] 的 $\mathrm{dn}\,u$ Fourier 级数 (17.2)（实即拉马努金在 Ch. 16 Entry 33(iii) 中所推导者），比较 $u^{2n}$（$0 \le n \le 4$）的系数即得。(vi) 与 Entry 8(i) 相同（因 $z = \varphi^2(e^{-y})$）。(vii)–(ix) 的证明：由 Ch. 16 Entry 35(ii) 取 $n = 1,2,3$；其中 $P_2$、$P_4$、$P_6$ 分别为 Entry 14(i)–(iii) 中级数的常数倍。

**例 (i)。** $\varphi^8(q) = 1 + 16\sum_{k=1}^{\infty}k^3q^k/(1-(-q)^k)$。

证明：由 Entry 10(ii) 与 Entry 14(v)（$q$ 换为 $-q$）。

**例 (ii)。** $q\psi^8(q) = \sum_{k=1}^{\infty}k^3q^k/(1-q^{2k})$。

证明：由 Entry 11(i) 与 Entry 15(i)。

**例 (iii)。** $q\psi^4(q^2) = \sum_{k=0}^{\infty}(2k+1)q^{2k+1}/(1-q^{4k+2})$。

证明：由 Entry 11(iii) 与 Entry 15(ix)。

**例 (iv)。** $\psi^2(q^2) = \sum_{k=0}^{\infty}q^k/(1+q^{2k+1})$。

证明：由例 (iii) 的等式与 Entry 16(ix)。

**例 (v)。** $\varphi^2(q)\psi^4(q) = \sum_{k=0}^{\infty}(2k+1)^2q^k/(1+q^{2k+1})$。

证明：由 Entry 16(x)、(6.4)、(6.10)、(11.1)、(11.3)。

**例 (vi)。** $\sum_{k=1}^{\infty}k^9q^k/(1-q^{2k}) = q\psi^8(q)\left(1 + 504\sum_{k=1}^{\infty}k^5q^k/(1+q^k)\right)$。

证明：由 Entry 13(xi)、Entry 15(iv) 与 (17.3)。

**状态：** 已证明（书中给出证明）。**对照：** M02（$\cosh$ 级数求值）、M11（$\mathrm{dn}\,u$ 的 Fourier 级数）、M07（例 (i)–(vi) 的 $\varphi^8$、$\psi^8$ 求值）。

**我自验：** 取 $x = 0.5$：(i) 差 $6.3\times 10^{-32}$；(ii) 差 $2.5\times 10^{-31}$；(iii) 差 $3.1\times 10^{-31}$；(iv) 差 $6.3\times 10^{-31}$；(v) 差 $1.2\times 10^{-30}$；(vi) 差 $6.3\times 10^{-32}$；(vii) 差 $2.5\times 10^{-31}$；(viii) 差 $3.1\times 10^{-31}$；(ix) 差 $6.3\times 10^{-31}$。取 $q = 0.5$：例 (i) 差 $2.5\times 10^{-31}$；例 (ii) 差 $3.1\times 10^{-31}$；例 (iii) 差 $6.3\times 10^{-31}$（初版脚本误用 $\psi(q)$ 代 $\psi(q^2)$ 已纠正）；例 (iv) 差 $2.5\times 10^{-31}$；例 (v) 差 $6.3\times 10^{-31}$；例 (vi) 差 $1.2\times 10^{-30}$。

## Entry 18

**陈述。** 设 $n$ 为正整数。则

$$\begin{aligned}
\text{(i)}\quad \sum_{k=0}^{\infty}\frac{(-1)^k}{(2k+1)\cosh\{\frac12(2k+1)\pi\sqrt{3}\}} &= \frac{\pi}{24}, \\
\text{(ii)}\quad \sum_{k=0}^{\infty}\frac{(-1)^k}{(2k+1)\cosh\{\frac12(2k+1)\pi/\sqrt{3}\}} &= \frac{5\pi}{24}, \\
\text{(iii)}\quad \sum_{k=0}^{\infty}\frac{(-1)^k(2k+1)^{6n-1}}{\cosh\{\frac12(2k+1)\pi\sqrt{3}\}} &= 0 = \sum_{k=0}^{\infty}\frac{(-1)^k(2k+1)^{6n-1}}{\cosh\{\frac12(2k+1)\pi/\sqrt{3}\}}.
\end{aligned}$$

**说明。** (i) 与 (iii) 的前半部分最早由 Cauchy [3, p. 317] 建立；Rao 与 Ayyar [1]、Riesel [1] 各自重新发现了 (iii) 的前半部分；(i) 与 (iii) 前半部分的证明亦见 Berndt [4, 推论 7.2、7.6]；Zucker [2] 推导了 (i)(ii)，Ling [3] 证明了 (iii) 的两半，Zucker [1] 建立了 $n = 1$ 时 (iii) 的前半部分。拉马努金大概用部分分式法建立 Entry 18：若 $\omega$ 为本原三次单位根，则对每个非负整数 $n$，有 (18.1)：$\cos u\cos(\omega u)\cos(\omega^2 u)$ 的部分分式展开；令 $u\to 0$，得 $n = 0$ 时的 (i) 与 $n > 0$ 时 (iii) 的前半部分。Berndt 注：Entry 18 放在本章此处似乎有些突兀，但拉马努金大概是因其与 Entry 16(iii) 的明显联系而把它放在这里；他在 Ch. 18 第 10 节中还会回到这些和式。在 Ch. 14 中，拉马努金建立了若干同类结果；更多此类结果与文献见 Berndt [3]、[4] 与书 [9]。

**例 (i)。** 若 $\sum_{k=0}^{\infty}(-1)^k(2k+1)^7q^k/(1+q^{2k+1}) = 0$，则 $\chi(q) = 2^{1/4}q^{1/24}$ 或 $2^{1/4}(34q)^{1/24}$。

证明：考虑 Entry 16(iv)：左端为 $0$ 时，因 $0 < x < 1$，必有 $x = \frac12$ 或 $x(1-x) = \frac{1}{136}$；再用 Entry 12(v) 即得。

**例 (ii)。** 若 $\sum_{k=0}^{\infty}(-1)^k(2k+1)^9q^k/(1+q^{2k+1}) = 0$，则 $\chi(q) = 2^{1/4}\{(154\pm 6\sqrt{645})q\}^{1/24}$。

证明：考虑 Entry 16(v)：左端为 $0$ 时 $\{x(1-x)\}^{-1} = 616\pm 24\sqrt{645}$；再用 Entry 12(v) 即得。

**例 (iii)。** 若 $\sum_{k=0}^{\infty}(-1)^k(2k+1)^{11}q^k/(1+q^{2k+1}) = 0$，则 $\chi(q) = 2^{1/4}q^{1/24}$ 或 $2^{1/4}(4q)^{1/24}$ 或 $2^{1/4}(2764q)^{1/24}$。

证明：Entry 16(vi) 的左端为 $0$ 当且仅当 $x = \frac12$ 或 $\{x(1-x)\}^{-1} = 16$ 或 $11056$；再用 Entry 12(v) 即得。

Berndt 注：我们不知道拉马努金导出上述例子的动机。

**状态：** 已证明（书中给出证明思路与文献指引；(i) 与 (iii) 前半部分属 Cauchy）。**对照：** M02（Cauchy 级数求值）、M04（$\pi/24$、$5\pi/24$）、M01（三次单位根与部分分式）。

**我自验：** (i) 左端 $0.130899693899$、右端 $\pi/24 = 0.130899693899$，差 $6.3\times 10^{-32}$；(ii) 左端 $0.654498469497$、右端 $5\pi/24 = 0.654498469497$，差 $2.5\times 10^{-31}$；(iii) 取 $n = 1$：两级数皆 $0$，差 $6.3\times 10^{-32}$；取 $n = 2$：两级数皆 $0$，差 $1.2\times 10^{-30}$。

## 小结

本章共 18 条编号 Entry（Entry 1–18，无缺号），分体、推论与例子标题 149 个，Entry 标题共 153 个，另有第 3 节引理与第 4 节引理 2 个非 Entry 标题的结果；书页 87–142（56 页）。要点如下：

- Entry 1 以 Legendre 函数 $P_{-n}$ 表出椭圆积分，并得 Gauss 定理的推论 (i) 与含 $\psi$ 的展开式推论 (ii)。
- Entry 2 引入 $F(x)$，给出七条性质：(i) 的指数表示、(ii) 拉马努金著名的“very nearly”近似（$x^5$ 系数仅差 $1/(2^{19}\cdot 3^3\cdot 5)$）、(iii) 的对数乘积 $\pi^2$、(iv) 的 $F(1-x)+F(1-1/x) = 0$、(v) 的倍乘、(vi) 的幂级数算法与 (vii) 的 $\tanh$ 展开；例 1 给出 $e^{-\pi}$、$e^{-\pi\sqrt{2}}$、$e^{-2\pi}$ 等奇异值。
- Entry 3–5 建立 $\varphi^2(q) = {}_2F_1(\frac12,\frac12;1;1-\varphi^4(-q)/\varphi^4(q))$ 与反演公式 $F(1-\varphi^4(-q)/\varphi^4(q)) = q$；第 3 节引理的证明中拉马努金草图的错误断言已被 Berndt 否定。
- Entry 6 把拉马努金的记号与经典椭圆积分对接：$\varphi(e^{-y}) = \sqrt{z}$、$K = \frac12\pi\varphi^2(q)$、$q = e^{-\pi K'/K}$；推论为 $\varphi$ 的反演公式；例 (i)–(iii) 给出 $\varphi(e^{-\pi})$、$\varphi(e^{-\pi\sqrt{2}})$、$\varphi(e^{-2\pi})$ 的 Gamma 值（例 (ii) 中拉马努金漏写因子 $\sqrt{\Gamma(1/4)}/2^{1/4}$）。
- Entry 7 是椭圆积分的十三条结果：变量替换 (i)–(iv)、加法定理的退化形式 (v)、倍乘公式 (vi)、Jacobi 虚变换 (vii)、加法定理 (viii)(a)–(d)、双重积分 (ix)–(xi)、Gauss 变换 (xii) 与 Landen 变换 (xiii)。
- Entry 8 是 $\varphi$、$\psi$、$f$ 的十二条 Jacobi 型级数恒等式，证明用双重级数的行列求和与 Clausen 变换。
- Entry 9 给出 $y$、$z$ 的微分关系与 $L(e^{-2y})$ 的公式（(9.3)）。
- Entry 10–12 分别给出 $\varphi$、$\psi$、$f$、$\chi$ 在 $e^{-y}$、$e^{-2y}$、$e^{-4y}$、$e^{-y/2}$、$e^{-y/4}$ 等处的求值。
- Entry 13–14 给出 Eisenstein 级数 $L$、$M$、$N$ 的值与 $e^{ky}\pm 1$ 级数的求值，工具为 duplication、dimidiation 与 change of sign 三种变换（Entry 14(iv) 中拉马努金把 $17-32x+17x^2$ 误写为 $17-32x+x^2$）。
- Entry 15–17 给出 $\sinh$、$\cosh$ 级数的大量求值，工具为 $L$、$M$、$N$ 的值、$\mathrm{sn}\,u$ 与 $\mathrm{dn}\,u$ 的 Fourier 级数，以及三种变换。
- Entry 18 是 Cauchy 的级数 (i)–(iii)（$\pi/24$、$5\pi/24$ 与 $6n-1$ 次幂的消失），并以 Entry 16(iv)–(vi) 导出 $\chi(q)$ 的三个例子。

数值复核：约 155 项数值检查全部通过（mpmath 30 位，直接求和；截断级数余项量级与预期一致）。本章未发现新的原书印误；初版误读的五处均为我方转录或脚本错误，均已纠正并重新验证：Entry 6 例 (ii) 根号范围、Entry 6 例 (iii) $\sqrt{2+\sqrt{2}}/2$、Entry 8(i) 脚本漏 $k = 0$ 项、Entry 14(v) $(1-x)^2$、Entry 17 例 (iii) 脚本误用 $\psi(q)$ 代 $\psi(q^2)$，以及第 9 节例题系数 $111111/2688$（六个 1）。Berndt 本人记录的拉马努金笔误三处：§3 草图中的错误断言（已否定）、例 (ii) 漏因子（笔记 p. 207）、Entry 14(iv) $17-32x+x^2$（笔记 p. 212）。

## 待核对清单

- IMSC 本章结果数：imsc.res.in 2026-11-08 再次不可达（curl 返回 000），未能补录。
- Berndt 章首计数：本章导言（p. 87）未给出本章公式或定理陈述的总数。
- Entry 1 推论 (ii) 的长展开式未逐项数值复核（仅证明思路已记录）；Entry 7(xi) 未逐项数值复核（双重积分，证明思路已记录）；Entry 13(vii) 为 duplication 的文字表述，无公式可验；Entry 14(xii) 为 change of sign 的文字表述，无公式可验。
- Entry 7(ix) 的两个证明 Berndt 自承“都不完全令人满意，因其本质上是验证”；Entry 7(x)(xi) 的证明依赖 Ch. 11 的超几何结果，Berndt 注明“无疑不是拉马努金本人的证明”。
- Entry 2(ii) 为近似式（“very nearly”），非等式；数值差 $4.3\times 10^{-10}$（$x = 0.5$）与书中说明一致。
- Entry 6 例 (ii)：根号覆盖范围为 $\Gamma(1/4)/(2^{1/4}\pi)$（即 $\sqrt{\Gamma(1/4)/(2^{1/4}\pi)}$），已由 300 DPI 放大图与数值验证确认；Entry 6 例 (iii)：$\sqrt{2+\sqrt{2}}/2$，已由数值验证确认；Entry 14(v)：右端为 $(1-x)^2$ 而非 $(1-x^2)$，已由 300 DPI 放大图与数值验证确认；第 9 节例题 $x^3$ 系数为 $111111/2688$（六个 1），已由 300 DPI 放大图与幂级数展开确认。
- Entry 13 证明中 (13.4) 的具体形式与 Entry 15(ix) 的系数 $1/12$、$1/6$、Entry 14(viii) 的 $MN$ 恒等式均已数值核对；Entry 13(viii) 证明中 $L(e^{-y})$ 的链式计算（(13.5)）未逐式转录。
- TIFR 1957 年影印版的笔记页码：Berndt 在本章引用的笔记页码为 p. 206（§3 草图）、p. 207（例 (ii) 漏因子）、p. 212（Entry 14(iv) 笔误）；其余 Entry 的 TIFR 页码未逐条核对。
- 本章条目总数未见于其他目录核对；以书中编号 Entry 1–18 为准。

## 来源说明

- 整理层：Bruce C. Berndt，《Ramanujan's Notebooks》，Part III，Springer，1991，Ch. 17，书页 87–142（正文）；参考文献自书页 489 起，索引自书页 505 起。
- 电子版：archive.org 标识符 `ramanujan_notebooks_iii`（《Ramanujan's Notebooks, Part 3》，Springer 1991，XIII + 510 页，DOI **10.1007/978-1-4612-0965-2**；PDF 21,002,730 字节、524 叶，md5 `de9211b0bde03dd9255145d3f09bb78f`），**PDF 页 = 书页 + 14**（与 Part II 的 +12 不同）。本章为 PDF 页 101–156（书页 87–142）；PDF 页 157 起为 Ch. 18（书页 143）。DOI 核对：任务简报所给 DOI 10.1007/978-1-4612-0963-8 经 Springer 官网（link.springer.com/book/10.1007/978-1-4612-0965-2）与多家书目核对为误，正确 DOI 为 10.1007/978-1-4612-0965-2（eBook ISBN 978-1-4612-0965-2，精装 ISBN 978-0-387-97503-0，1991 年初版，1997 年修订第二版）。
- 转录方法：全部公式按 PDF 原图（150 DPI，书页 87–142）逐字转录；关键公式 Entry 6 例 (ii) 与例 (iii)、Entry 14(v)、第 9 节例题系数另用 300 DPI 放大图确认；OCR（DjVu 文本层）只作检索索引，公式凡与原图或数值不符者一律纠正。
- 数值复核：mpmath 30 位，直接求和 + 解析尾项；约 155 项检查全部通过（详见各 Entry 的“我自验”）。
- 章名与目录：以原书目录为准，Ch. 17 为 "Fundamental Properties of Elliptic Functions"；下一章 Ch. 18 为 "The Jacobian Elliptic Functions"（书页 143 起）。
- 参考文献（书中引用，本章出现者）：Bailey [4]、Byrd–Friedman [1]、Cayley [1]、Glasser [1]、Gradshteyn–Ryzhik [1]、Jacobi [1]、[2]、Kleiber [1]、Ling [1]–[3]、MacMahon [1]、Raghavan–Rangachari [1]、Rao–Ayyar [1]、Riesel [1]、Thiruvenkatachar–Venkatachaliengar [1]、Whittaker–Watson [1]、Zucker [1]、[2]、Schoissengeier [1]、Berndt [3]、[4]、[9]、Adiga [1]（学位论文）、Bhargava 与 Adiga 的独立证明。
