# Part II，Chapter 14——Infinite Series（无穷级数）

出处：Bruce C. Berndt，《Ramanujan's Notebooks》，Part II，Springer，1989，Ch. 14，书页 240–299。

本章是 Berndt 五卷中无穷级数恒等式最集中、最著名的一章：从解析 Eisenstein 级数的一般变换公式与部分分式分解出发，经 Poisson 求和与留数定理，收束于 $\zeta(2n+1)$ 的 Ramanujan 公式（Entry 21(i)，本章最著名的结果）与一系列双曲函数级数求值。本章共 **25 条 Entry（Entry 1–25，无缺号）**，另含分体 Entry 5(i)/5(ii)、8(i)/8(ii)/8(iii)、9(i)/9(ii)、16(i)/16(ii)、17(i)/17(ii)、19(i)–19(v)、20(i)–20(iv)、21(i)/21(ii)/21(iii)、22(i)/22(ii)/22(iii)、24(i)/24(ii)、25(i)–25(xii)，共 **57 个 Entry 标题**。

## 背景与记号

- 章首导言（pp. 240–241）：自拉马努金 1920 年去世以来，确立本章结果的已发表论文比其余 20 章中任何一章都多；在许多情形下，作者并不知道自己的发现已见于拉马努金笔记。Berndt 在 [6]、[7] 中证明：本章若干结果以及许多其他结果，源于解析 Eisenstein 级数的一条一般变换公式；但本章也含有许多其他类型的结果。Hardy 在《Collected Papers》[16, p. xxv] 的评语（Berndt 称没有比这更贴切的关于本章的评论）：“There is always more in one of Ramanujan's formulae than meets the eye, as anyone who sets to work to verify those which look the easiest will soon discover. In some the interest lies very deep, in others comparatively near the surface; but there is not one which is not curious and entertaining.”（拉马努金的公式总比一眼看去蕴含得更多，任何动手验证那些看似最容易的公式的人都会很快发现这一点；有些趣味藏得很深，有些则比较浅近，但没有一条是不奇妙而有趣的。）本章有些公式相当容易证明，有些则需要相当大的努力；许多公式的源头在椭圆模函数，大量公式源于部分分式分解，若干为 Poisson 求和的实例，六条属于超几何级数，另有少量积分求值。
- 记号（p. 241）：$R(f, z_0) = R(z_0)$ 表示 $f$ 在极点 $z_0$ 处的留数；$\chi(n)$ 恒表示模 4 的本原特征，即

$$\chi(n) = \begin{cases} 0, & n \equiv 0 \pmod 2, \\ 1, & n \equiv 1 \pmod 4, \\ -1, & n \equiv 3 \pmod 4. \end{cases} \tag{0.1}$$

- 本章与已填章节的互见：Part I Ch. 2 的调和级数与反正切和（Entry 5(i)(ii) 的正弦幂级数、Entry 16 的正弦幂积分与之呼应）；Part I Ch. 3 的组合级数反演与 Lagrange 反演（Entry 17 的 Gamma 分母结构、Entry 2–3 的 Gamma 级数与之同源）；Part I Ch. 6 的发散级数（Entry 23 的形式推导与之同属“纯形式”一路，见该条）；Part I Ch. 9 的无穷级数恒等式（Entry 4 的推论、Entry 18 的部分分式主线、Entry 32 的 $2G$ 级数与本章 Entry 21(ii)、Entry 25(vii) 的 $L(2) = G$ 互见）；Part II Ch. 10–11 的超几何级数（Entry 2 的推论 1 可用 Dougall 定理证，Entry 3 即 Dougall 定理的推论，Entry 21(i) 的 $n < -1$ 情形化归 Entry 13 的超几何型恒等式；六条超几何级数见章首导言）；Part II Ch. 13 的级数渐近（Entry 10–11、第 12 节例题）与本章 Entry 23 的渐近误差 $h$、Entry 11(iii) 的 $S = 1$ 互见；Ch. 13 Entry 31(i)、32(ii) 的 Poisson 求和是本章 Entry 9(i)(ii) 的类比。Ch. 15（Asymptotic Expansions and Modular Forms）将继续模形式一线。
- 与主题模块的对照总览：级数主线见 **M02**（几乎全章；Entry 5、16 的正弦幂级数与积分、Entry 13、21 的 Bernoulli 数级数、Entry 25 的 coth/tanh/csch/sech 求值均属 M02 核心）；数论衔接见 **M01**（Bernoulli 数 $B_{2n}$ 与 Euler 数 $E_{2n}$：Entry 13、20、21、25；Dirichlet $L$ 函数：Entry 21(ii)(iii)；除数函数 $\sigma_v$：Entry 13 推论 (iv) 后的 (13.2)）；分拆与 $q$ 级数见 **M05、M07**（Entry 8 推论 (ii) 的无穷乘积、Entry 13 (13.2) 的 $\sigma_v$ 生成级数、Entry 2–3 的 Gamma 级数）；模形式与 theta 函数见 **M06**（Entry 7 的 theta 函数方程、Entry 8 的 Dedekind eta 函数背景、Entry 13 的 Eisenstein 级数源头、Entry 21 的模变换）；Gamma 函数见 **M10**（Entry 2、3、6、17 的 Gamma 商与乘积）；渐近分析见 **M12**（Entry 16、17 的积分渐近、Entry 23 的形式渐近与误差 $h$、Entry 11(iii) 的 $S = 1$）；积分见 **M09**（Entry 16 的正弦幂积分、Entry 22(ii) 的双曲积分）；$\pi$ 与特殊常数见 **M04**（Entry 8 例 (8.4)、Entry 15 的 $\pi/16$、Entry 25 的 $\pi^3$、$\pi^5$、$\pi^7$、$\pi^9$ 求值与 Catalan 常数 $G$）；椭圆函数见 **M11**（Entry 22(iii) (22.11) 的证明用椭圆函数、Entry 13 的 Glaisher 证明）。

## 本章结构

| Entry | 主题 | 书页 |
|---|---|---|
| Entry 1 | 无穷乘积与交错级数 (1.1) 及其推论 (1.3)、常数 $C$ | 241 |
| Entry 2 | 两个 Gamma 级数之和 (2.1) 与推论 1、2 | 245 |
| Entry 3 | 四 Gamma 分母级数 (3.1)（Dougall 定理） | 248 |
| Entry 4 | $\sum 1/(n^2+z^2+z^4/n^2)$ (4.1) 与推论 | 248 |
| Entry 5(i) | $\sum \sin^{2n+1}(kx)/k$ | 249 |
| Entry 5(ii) | $\sum \sin^{2n+2}(kx)/k^2$ | 250 |
| Entry 6 | $\mathrm{sech}^{2n}$ 与 $\varphi$ 的 Poisson 变换 | 252 |
| Entry 7 | theta 函数变换（Poisson 求和）与推论 | 252–253 |
| Entry 8(i) | $\sinh$–$\sin$ 双曲三角级数（Schlömilch 首证） | 253 |
| Entry 8(ii) | $\cos$–$\cosh$ 对数级数 | 253 |
| Entry 8(iii) | 一般整函数 $\varphi$ 的围道公式 (8.1) | 253–254 |
| Entry 9(i) | $\chi$ 加权的正弦有限和（余弦变换） | 257 |
| Entry 9(ii) | $\chi$ 加权的余弦有限和（正弦变换） | 257 |
| Entry 10 | $\chi$ 加权的 theta 型变换（与 Entry 7 对照） | 257 |
| Entry 11 | $\sec$–$\cosh$ 变换 (11.1) | 258 |
| Entry 12 | $\chi$ 加权的 $\sin$–$\sinh$ 变换 (12.1) 与推论 (12.3) | 260 |
| Entry 13 | Bernoulli 数级数（$\alpha^n$–$(-\beta)^n$ 型）与推论 (i)–(iv) | 261 |
| Entry 14 | $\chi$ 加权的 $\cosh$ 级数 (14.1) 与推论 (14.2) | 262 |
| Entry 15 | $\tan^{-1}$ 与 $\mathrm{sech}$ 的双重求值 (15.1) 与推论 | 262 |
| Entry 16(i) | $\sin^{2n+1}x/x$ 与 $\sin^{2n+2}x/x^2$ 的 $\cos^{2m}x$ 积分 | 263 |
| Entry 16(ii) | 上述积分的 $\cos(2px)$ 推广 | 264 |
| Entry 17(i) | $\cos^n$ 有限和的 Gamma 展开 (17.1) | 264 |
| Entry 17(ii) | $\chi$ 加权的 $\cos^n\sin$ 有限和 (17.4) | 265 |
| Entry 18 | 部分分式主恒等式 (18.1) 与推论 1、2、3 | 267 |
| Entry 19(i) | $\pi^2xy\cot(\pi x)\coth(\pi y)$ (19.1)（级数一般不收敛） | 271 |
| Entry 19(ii) | $\pi^2xy\csc(\pi x)\mathrm{csch}(\pi y)$ | 272 |
| Entry 19(iii) | $\tan$–$\tanh$ 部分分式 | 272 |
| Entry 19(iv) | $\sec$–$\mathrm{sech}$ 部分分式 | 273 |
| Entry 19(v) | $\cot$–$\mathrm{sech}$ 部分分式 | 273 |
| Entry 20(i) | $\pi^2z^2\cot(\pi z)\coth(\pi z)$（$x = y$ 特例）与推论 | 274 |
| Entry 20(ii) | $\pi^2z^2\csc(\pi z)\mathrm{csch}(\pi z)$ 与推论 | 275 |
| Entry 20(iii) | $\tan$–$\tanh$ 的 $z$ 特例与推论 | 275 |
| Entry 20(iv) | $\sec$–$\mathrm{sech}$ 的 $z$ 特例与推论 | 275 |
| Entry 21(i) | $\zeta(2n+1)$ 的 Ramanujan 公式（本章最著名结果） | 275–276 |
| Entry 21(ii) | Dirichlet $L$ 函数的 Euler 数公式 | 276 |
| Entry 21(iii) | $L(2n)$ 的混合公式 | 277 |
| Entry 22(i) | 双曲余弦商的恒等式 (22.1)（笔记版有误） | 277 |
| Entry 22(ii) | 双曲积分 (22.6) 与推论 (22.8) | 278 |
| Entry 22(iii) | $\cos\sqrt{\alpha n}$ 级数 (22.10) 与 (22.11) | 280 |
| Entry 23(i) | 形式双重级数 (23.1) 与误差 $h$（拉马努金可能有误） | 283 |
| Entry 23(ii) | $\chi$ 加权的形式双重级数 (23.8) 与误差 $h$ | 285 |
| Entry 24 | $\pi e^{-2\pi z}$ 的部分分式 (24.1) 型恒等式 | 291 |
| Entry 24(i) | $\sum 1/(z^2+n^2)$ 的闭式（(1.9) 的改写） | 292 |
| Entry 24(ii) | $1/[z(e^{\pi z}+1)]$ 的部分分式 | 292 |
| Entry 25 | $\pi e^{-\pi z}$ 的部分分式（与 Entry 24 互补） | 292 |
| Entry 25(i)(ii) | $\sum \coth(\pi k)/k^3$、$\sum \coth(\pi k)/k^7$ 与通式 (25.3) | 293 |
| Entry 25(iii)(iv) | $\sum \tanh((2k+1)\pi/2)/(2k+1)^3$、$(2k+1)^7$ 与通式 (25.4) | 293 |
| Entry 25(v)(vi) | $\sum (-1)^{k+1}\mathrm{csch}(\pi k)/k^3$、$/k^7$ 与通式 (25.5) | 294 |
| Entry 25(vii)(viii)(ix) | $\sum \chi(k)\mathrm{sech}(\pi k/2)/k$、$/k^5$、$/k^9$ 与通式 (25.6) | 295 |
| Entry 25(x) | $\sum \chi(k)/[k^2(e^{\pi k}-1)]$ 与 Catalan 常数 (25.7) | 295 |
| Entry 25(xi) | $\sum 1/[\{k^2+(k+1)^2\}(\cosh((2k+1)\pi)-\cosh\pi)]$ (25.10) | 296 |
| Entry 25(xii) | $\sum (2k+1)/[\{25+(2k+1)^4/100\}(e^{(2k+1)\pi}+1)]$ (25.11) | 298 |

## Entry 1

**陈述。** 设 $z$ 为复数，则

$$\frac{1}{z^2}\prod_{n=1}^{\infty}\left(1+\frac{2z^2}{n(n+1)}\right)^{-1} = \sum_{n=0}^{\infty}\frac{(-1)^n(2n+1)}{z^2+n(n+1)/2}. \tag{1.1}$$

**推论。** 设 $\mathrm{Re}\,z > 0$，则

$$\sum_{n=1}^{\infty}\frac{(-1)^{n+1}(2n+1)}{\sqrt{n(n+1)}\left(e^{2\pi z\sqrt{n(n+1)}}-1\right)} + \frac{1}{z}\sum_{n=1}^{\infty}\mathrm{sech}\left(\frac{\pi}{z}\sqrt{n^2-z^2/4}\right) = \frac{1}{2\pi z}+\frac{\pi z}{6}-C, \tag{1.3}$$

其中

$$C = \frac{1}{2}+\frac{1}{2}\sum_{n=1}^{\infty *}\frac{(-1)^{n+1}(2n+1)}{\sqrt{n(n+1)}} = 0.54661949\ldots,$$

求和号上的星号表示逐对相加（即把 $n$ 为奇数与 $n+1$ 两项先合并再求和）。

**出处。** Berndt Part II，Ch. 14，Entry 1（书页 241）。证明用留数定理，见书中 (1.4)–(1.16)；推论的证明属 R. J. Evans，归结为 (1.16)：$\alpha, \beta > 0$、$\alpha\beta = \pi^2$ 时 $\alpha\sum \mathrm{csch}^2(\alpha n)+\beta\sum \mathrm{csch}^2(\beta n) = -1+(\alpha+\beta)/6$。

**状态。** 已证明。另有两处拉马努金原文错误已按 Berndt 注明：拉马努金自称的常数值 $C' = 0.61144169\ldots$ 是错的（J. Hill 计算证实；拉马努金在 (1.5) 左端分母漏了因子 $2\sqrt{n(n+1)}$）；正确的 (1.3) 由 R. Lamphere 猜想并经数值验证。

**对照。** M02（无穷乘积与交错级数）；M01（常数 $C$ 的逐对求和是条件收敛级数的标准处理）；M06（推论的证明归结为 Eisenstein 级数型恒等式 (1.16)，与模形式一线相通）。

**数值复核。** (1.1) 在 $z = 1$ 时两端均为 $0.196880615315$（mpmath 30 位，差 0）；$C$ 的逐对求和得 $0.5466194979$，与书中 $0.54661949$ 一致；$C'$ 的级数求和（nsum）得 $0.6114416901$，与拉马努金自称值一致，确为错误值；(1.3) 在 $z = 1$ 与 $z = 0.5$ 时两端差 $1.1\times 10^{-10}$（差值来自 $C$ 只取 8 位小数）。

## Entry 2

**陈述。** 设 $m, n, x, y$ 为复数，$\Gamma(1+xz)$ 与 $\Gamma(1+yz)$ 无重合极点，$z = 1$ 不是二者的极点，且 $\mathrm{Re}(m+n) > 0$，则

$$\sum_{k=1}^{\infty}\frac{(-1)^{k+1}\Gamma(1-ky/x)}{\Gamma(m-k+1)\Gamma(n+1-ky/x)\Gamma(k)(x+k)} + \sum_{k=1}^{\infty}\frac{(-1)^{k+1}\Gamma(1-kx/y)}{\Gamma(n-k+1)\Gamma(m+1-kx/y)\Gamma(k)(y+k)} = \frac{\Gamma(x+1)\Gamma(y+1)}{\Gamma(x+m+1)\Gamma(y+n+1)}. \tag{2.1}$$

**推论 1。** 设 $x$ 不是整数，$\mathrm{Re}(m+n) > -1$，则

$$\sum_{k=-\infty}^{\infty}\frac{(-1)^k}{(x+k)\Gamma(m+1-k)\Gamma(n+1+k)} = \frac{\pi}{\sin(\pi x)\Gamma(m+x+1)\Gamma(n-x+1)}. \tag{2.3}$$

推论 1 可用 Dougall 定理证明，Entry 2 本身不可。

**推论 2。** 设 $\mathrm{Re}(\alpha+\beta) > 0$，则

$$\sum_{k=0}^{\infty}\frac{(-1)^k}{(2k+1)\Gamma(\alpha-k)\Gamma(\beta+k+1)} + \sum_{k=0}^{\infty}\frac{(-1)^k}{(2k+1)\Gamma(\beta-k)\Gamma(\alpha+k+1)} = \frac{\pi}{2\Gamma(\alpha+\frac12)\Gamma(\beta+\frac12)}. \tag{2.4}$$

**出处。** Berndt Part II，Ch. 14，Entry 2（书页 245）。证明用留数定理。

**状态。** 已证明。

**对照。** M10（Gamma 函数商与乘积）；M07（超几何级数：推论 1 的 Dougall 定理背景见 Ch. 10 Entry 1）；M02（双边级数 (2.3)）。

**数值复核。** (2.1) 取 $m = 1.5$、$n = 0.7$、$x = 2$、$y = \sqrt{3}$（无理比值，避免 $\Gamma(1+xz)$ 与 $\Gamma(1+yz)$ 的重合极点），直接求和至 $k = 6000$ 得差 $3.6\times 10^{-10}$；(2.3) 取 $m = 1.3$、$n = 0.6$、$x = 0.5$，nsum 双边求和差 $5.1\times 10^{-13}$；(2.4) 取 $\alpha = 1.3$、$\beta = 0.7$，nsum 差 0。

## Entry 3

**陈述。** 设 $\mathrm{Re}(\alpha+\beta+\gamma+\delta) > -1$，则

$$\sum_{k=0}^{\infty}\frac{1}{\Gamma(\alpha-k+1)\Gamma(\beta-k+1)\Gamma(\gamma+k+1)\Gamma(\delta+k+1)} + \sum_{k=1}^{\infty}\frac{1}{\Gamma(\alpha+k+1)\Gamma(\beta+k+1)\Gamma(\gamma-k+1)\Gamma(\delta-k+1)} = \frac{\Gamma(\alpha+\beta+\gamma+\delta+1)}{\Gamma(\alpha+\gamma+1)\Gamma(\beta+\gamma+1)\Gamma(\alpha+\delta+1)\Gamma(\beta+\delta+1)}. \tag{3.1}$$

**出处。** Berndt Part II，Ch. 14，Entry 3（书页 248）。由 Dougall 定理证明。

**状态。** 已证明。

**对照。** M10（Gamma 函数）；M07（Dougall 定理，见 Ch. 10 Entry 1）；M02。

**数值复核。** 取 $\alpha = \beta = \gamma = \delta = 0.5$，nsum 得两端均为 $2.0$，差 0。

## Entry 4

**陈述。** 设 $z \ne me^{\pm\pi i/3}$（$m$ 为整数），则

$$\sum_{n=1}^{\infty}\frac{1}{n^2+z^2+z^4/n^2} = \frac{\pi}{2z\sqrt{3}}\cdot\frac{\sinh(\pi z\sqrt{3})-\sqrt{3}\sin\pi z}{\cosh(\pi z\sqrt{3})-\cos\pi z}. \tag{4.1}$$

**推论。** 对正整数 $n$，

$$\sum_{k=1}^{\infty}\frac{1}{k^2+(2n)^2+(2n)^4/k^2} = \frac{1}{12n^2}+\frac{1}{2}\sum_{k=1}^{\infty}\frac{1}{k^2+3n^2}.$$

**出处。** Berndt Part II，Ch. 14，Entry 4（书页 248）。证明用部分分式分解与 (1.9) 型恒等式。

**状态。** 已证明。

**对照。** M02（有理函数级数）；M09（Ch. 9 的部分分式主线与之同源）；M01（推论右端 $\sum 1/(k^2+3n^2)$ 为 $\zeta$ 型求和）。

**数值复核。** (4.1) 在 $z = 1$ 与 $z = 0.5$ 时 nsum 差均为 0；推论在 $n = 1$ 时 nsum 差 0。

## Entry 5(i)

**陈述。** 设 $n$ 为非负整数，$0 < x < \pi/(n+\frac12)$，则

$$\sum_{k=1}^{\infty}\frac{\sin^{2n+1}(kx)}{k} = \frac{\sqrt{\pi}}{2}\frac{\Gamma(n+\frac12)}{\Gamma(n+1)}.$$

**出处。** Berndt Part II，Ch. 14，Entry 5(i)（书页 249）。

**状态。** 已证明。

**对照。** M02（正弦幂级数）；M12（右端与 $x$ 无关的常数是本条的要点）；与 Entry 16(i)(ii) 的积分形式对照（$p = 0$ 的情形）。

**数值复核。** $n = 1$、$x = 1$ 时左端 $= \pi/4$：直接求和至 $2\times 10^6$ 项差 $3.3\times 10^{-7}$（$1/N$ 型尾项），另经 Gradshteyn–Ryzhik (5.2)（$\sum \sin(ax)/k = (\pi-a)/2$）化为三角恒等式逐项验证，精确成立。

## Entry 5(ii)

**陈述。** 设 $n$ 为非负整数，$0 \le x \le \pi/(n+1)$，则

$$\sum_{k=1}^{\infty}\frac{\sin^{2n+2}(kx)}{k^2} = \frac{\sqrt{\pi}}{2}\frac{\Gamma(n+\frac12)}{\Gamma(n+1)}\cdot x.$$

**出处。** Berndt Part II，Ch. 14，Entry 5(ii)（书页 250）。

**状态。** 已证明。

**对照。** M02；与 Entry 16(i)(ii) 对照。

**数值复核。** $n = 1$、$x = 1$ 时左端 $= \pi/4$：直接求和至 $2\times 10^6$ 项差 $1.9\times 10^{-7}$，另经 $\sum \cos(ak)/k^2 = \pi^2/6-\pi a/2+a^2/4$ 化为三角恒等式逐项验证，精确成立。

## Entry 6

**陈述。** 设 $n > 0$，$\varphi(\beta) = \prod_{k=0}^{\infty}\{1+(\beta/(n+k))^2\}^{-1}$。设 $\alpha, \beta > 0$ 且 $\alpha\beta = \pi$，则

$$\sqrt{\alpha}\left\{\frac{1}{2}+\sum_{k=1}^{\infty}\mathrm{sech}^{2n}(\alpha k)\right\} = \frac{\Gamma(n)}{\Gamma(n+\frac12)}\sqrt{\beta}\left\{\frac{1}{2}+\sum_{k=1}^{\infty}\varphi(\beta k)\right\}.$$

其中 $\varphi(x) = \Gamma(n+ix)\Gamma(n-ix)/\Gamma^2(n)$（拉马努金 [8]，[16] pp. 53–58，p. 54）。

**出处。** Berndt Part II，Ch. 14，Entry 6（书页 252）。证明用 Poisson 求和（Ch. 13 Entry 15）。

**状态。** 已证明。

**对照。** M10（Gamma 乘积 $\varphi$）；M02（$\mathrm{sech}$ 级数）；M09（Poisson 求和，见 Ch. 13 Entry 31(i)）。

**数值复核。** $n = 1$、$\alpha = \beta = \sqrt{\pi}$ 时两端均为 $0.81547296044$，差 0（$\varphi(\beta k) = |\Gamma(1+i\beta k)|^2 = \pi\beta k/\sinh(\pi\beta k)$）。

## Entry 7

**陈述。** 设 $\alpha, \beta > 0$ 且 $\alpha\beta = \pi$，$z$ 为任意复数，则

$$e^{z^2/4}\sqrt{\alpha}\left\{\frac{1}{2}+\sum_{k=1}^{\infty}e^{-\alpha^2k^2}\cos(\alpha zk)\right\} = \sqrt{\beta}\left\{\frac{1}{2}+\sum_{k=1}^{\infty}e^{-\beta^2k^2}\cosh(\beta zk)\right\}.$$

**推论。** 取 $z = 0$，得

$$\sqrt{\alpha}\left\{\frac{1}{2}+\sum_{k=1}^{\infty}e^{-\alpha^2k^2}\right\} = \sqrt{\beta}\left\{\frac{1}{2}+\sum_{k=1}^{\infty}e^{-\beta^2k^2}\right\},$$

即经典 theta 函数的函数方程。

**出处。** Berndt Part II，Ch. 14，Entry 7（书页 252–253）。证明用 Poisson 公式 (6.1) 与 Gradshteyn–Ryzhik [1, p. 480] 的积分 (7.1)：$\int_0^{\infty}e^{-cx^2}\cos(rx)\,dx = \frac12\sqrt{\pi/c}\,e^{-r^2/(4c)}$（$\mathrm{Re}\,c > 0$）。

**状态。** 已证明。

**对照。** M06（theta 函数与模变换，本章 theta 一线的起点）；M02；M09（Poisson 求和）。

**数值复核。** $\alpha = 2$、$\beta = \pi/2$、$z = 1$ 时两端差 $2.0\times 10^{-31}$；推论（$z = 0$）差 $9.9\times 10^{-32}$。

## Entry 8(i)

**陈述。** 设 $\alpha, \beta, n > 0$ 且 $\alpha\beta = \pi$、$0 < \beta n < \pi$，则

$$\alpha\sum_{k=1}^{\infty}\frac{\sinh(2\alpha nk)}{e^{2\alpha^2k}-1} + \beta\sum_{k=1}^{\infty}\frac{\sin(2\beta nk)}{e^{2\beta^2k}-1} = \frac{1}{4}\alpha\coth(\alpha n)-\frac{1}{4}\beta\cot(\beta n)-\frac{1}{2}n.$$

**出处。** Berndt Part II，Ch. 14，Entry 8(i)（书页 253）。源于与 Dedekind eta 函数对数相近的函数的变换公式；首个证明先于拉马努金，由 Schlömilch [1] 给出；后有 Rao–Ayyar [1]、J. Lagrange [1] 与 Berndt [6, Eq. (3.31)]、[2, Eq. (11.21)] 的证明。

**状态。** 已证明（首证 Schlömilch）。

**对照。** M06（Dedekind eta 函数）；M02（双曲–三角混合级数）；M04（$\coth$、$\cot$ 的 $\pi$ 系数）。

**数值复核。** $\alpha = 2$、$\beta = \pi/2$、$n = 1$ 时两端差 0。

## Entry 8(ii)

**陈述。** 设 $\alpha, \beta, n > 0$ 且 $\alpha\beta = \pi$、$0 < \alpha n < \pi$，则

$$2\sum_{k=1}^{\infty}\frac{\cos(2\alpha nk)}{k(e^{2\alpha^2k}-1)} - 2\sum_{k=1}^{\infty}\frac{\cosh(2\beta nk)}{k(e^{2\beta^2k}-1)} = n^2-\frac{1}{6}(\alpha^2-\beta^2)+\mathrm{Log}\left\{\frac{\sin(\alpha n)}{\sinh(\beta n)}\right\}.$$

**出处。** Berndt Part II，Ch. 14，Entry 8(ii)（书页 253）。源于推广 Dedekind eta 函数对数的函数的变换公式；证明见 J. Lagrange [1] 与 Berndt [6, Proposition 3.4]。

**状态。** 已证明。

**对照。** M06；M02；M01（右端 $\mathrm{Log}$ 项与 $\zeta$ 的联系见 Entry 21）。

**数值复核。** $\alpha = 2$、$\beta = \pi/2$、$n = 1$ 时两端差 0。

## Entry 8(iii)

**陈述。** 设 $\alpha, \beta, n, r, t > 0$ 且 $\alpha\beta = \pi$、$r = n\beta$、$t = \pi/\beta^2$。设 $C$ 为顶点 $\pm i$ 与 $\pm t$ 的正向平行四边形，$\varphi(z)$ 为整函数，$m$ 为正整数，$M = m+\frac12$，定义 $f_m(z) = \varphi(rMz)/[z(e^{2\pi Mz}-1)(e^{2\pi iMz/t}-1)]$，并设 $f_m(z)$ 在 $C' = C-\{\pm i, \pm t\}$ 上有界趋于 0（$m\to\infty$）。则

$$\sum_{k=1}^{\infty}\frac{\varphi(\alpha nk)+\varphi(-\alpha nk)}{k(e^{2\alpha^2k}-1)} + \sum_{k=1}^{\infty}\frac{\varphi(\alpha nk)}{k} - \sum_{k=1}^{\infty}\frac{\varphi(\beta nki)+\varphi(-\beta nki)}{k(e^{2\beta^2k}-1)} - \sum_{k=1}^{\infty}\frac{\varphi(\beta nki)}{k} = \frac{\pi i\varphi(0)}{2}-\frac{\alpha^2\varphi(0)}{6}+\frac{\beta^2\varphi(0)}{6}-\frac{\alpha n\varphi'(0)}{2}+\frac{\beta ni\varphi'(0)}{2}-\frac{n^2\varphi''(0)}{4}, \tag{8.1}$$

只要上述级数均收敛。Berndt 注：关于 $\varphi$ 的假设显然非常严格，是技术性的；可以表述得更具体，但定理的陈述会更长。

**出处。** Berndt Part II，Ch. 14，Entry 8(iii)（书页 253–254）。证明：对 $f_m(z)$ 在 $C$ 上积分，$f_m$ 在 $C$ 内有单极点 $z = \pm ik/M$ 与 $z = \pm kt/M$（$1\le k\le m$），另有 $z = 0$ 处的三重极点。

**状态。** 已证明（在所述技术性假设下）。Entry 8(ii) 形式上为其特例（取 $\varphi(z) = e^{2iz}$）。

**对照。** M02（一般整函数的变换公式）；M06（围道与模变换）；M12（假设的严格性属渐近分析的技术细节）。

**数值复核。** 未直接数值复核（$\varphi$ 为任意整函数）；其特例 Entry 8(ii) 已复核通过（见上条）。

**推论 (i)。** 设 $\alpha\beta = \pi^2$，则

$$\alpha\sum_{k=1}^{\infty}\frac{k}{e^{2\alpha k}-1}+\beta\sum_{k=1}^{\infty}\frac{k}{e^{2\beta k}-1} = \frac{\alpha+\beta}{24}-\frac{1}{4}. \tag{8.3}$$

首证 Schlömilch。

**推论 (ii)。** 设 $\alpha\beta = \pi^2$，则

$$e^{(\alpha-\beta)/12} = \left(\frac{\alpha}{\beta}\right)^{1/4}\prod_{k=1}^{\infty}\frac{1-e^{-2\alpha k}}{1-e^{-2\beta k}}.$$

**例 (8.4)。** $\sum_{k=1}^{\infty}k/(e^{2\pi k}-1) = 1/24-1/(8\pi)$。拉马努金向 JIMS 投稿的题目 [3]，[16] p. 326。

**数值复核。** 例 (8.4) 两端差 $5.0\times 10^{-33}$；推论 (ii) 取 $\alpha = 2$、$\beta = \pi^2/2$ 时两端差 0。

## Entry 9(i)

**陈述。** 设 $\alpha, \beta > 0$ 且 $\alpha\beta = \pi/2$。设 $h > 0$ 使 $h/\alpha > 1$ 且 $h/\alpha$ 不是奇整数，$m$ 为小于 $h/\alpha$ 的最大奇整数，$n$ 为任意实数，$\varphi(x)$ 在 $[0, h]$ 上连续且有界变差，定义

$$\psi(t) = \int_0^h\varphi(x)\cos(tx)\,dx. \tag{9.1}$$

则

$$\alpha\sum_{k=1}^{m}\chi(k)\sin(\alpha nk)\varphi(\alpha k) = \frac{1}{2}\sum_{k=1}^{\infty}\chi(k)\{\psi(\beta k-n)-\psi(\beta k+n)\}.$$

**出处。** Berndt Part II，Ch. 14，Entry 9(i)（书页 257）。证明用正弦变换的 Poisson 公式（Titchmarsh [2, p. 66] 的 (9.2)）。

**状态。** 已证明。拉马努金原陈述附加条件 $|n| < \beta$，Berndt 注该假设似乎无必要；本条与 Ch. 13 Entry 31(i) 类比。

**对照。** M02（$\chi$ 加权有限和）；M09（Poisson 求和，Ch. 13 Entry 31(i)）；M06（$\chi$ 为模 4 特征）。

## Entry 9(ii)

**陈述。** 设 $\alpha, \beta, h, m, n, \varphi$ 满足与 Entry 9(i) 相同的假设，定义 $\psi(t) = \int_0^h\varphi(x)\sin(tx)\,dx$，则

$$\alpha\sum_{k=1}^{m}\chi(k)\cos(\alpha nk)\varphi(\alpha k) = \frac{1}{2}\sum_{k=1}^{\infty}\chi(k)\{\psi(\beta k-n)+\psi(\beta k+n)\}.$$

**出处。** Berndt Part II，Ch. 14，Entry 9(ii)（书页 257）。证明与 Entry 9(i) 完全类似。

**状态。** 已证明；与 Ch. 13 Entry 32(ii) 类比。

**对照。** M02；M09。

## Entry 10

**陈述。** 设 $\alpha, \beta > 0$ 且 $\alpha\beta = \pi/4$，$z$ 为任意复数，则

$$e^{z^2/4}\sqrt{\alpha}\sum_{k=1}^{\infty}\chi(k)e^{-\alpha^2k^2}\sin(\alpha zk) = \sqrt{\beta}\sum_{k=1}^{\infty}\chi(k)e^{-\beta^2k^2}\sinh(\beta zk).$$

**出处。** Berndt Part II，Ch. 14，Entry 10（书页 257）。

**状态。** 已证明。

**对照。** M06（theta 型变换，与 Entry 7 对照：Entry 7 用 $\cos$/$\cosh$，本条用 $\chi$ 加权的 $\sin$/$\sinh$）；M02。

**数值复核。** $\alpha = \beta = \sqrt{\pi}/2$、$z = 1$ 时两端差 $9.9\times 10^{-32}$。

## Entry 11

**陈述。** 设 $\alpha, \beta > 0$ 且 $\alpha\beta = \pi$，$|n| < \beta/2$，则

$$\alpha\left\{\frac{1}{4}\sec(\alpha n)+\sum_{k=1}^{\infty}\chi(k)\frac{\cos(\alpha nk)}{e^{\alpha^2k}-1}\right\} = \beta\left\{\frac{1}{4}+\frac{1}{2}\sum_{k=1}^{\infty}\frac{\cosh(2\beta nk)}{\cosh(\beta^2k)}\right\}. \tag{11.1}$$

**出处。** Berndt Part II，Ch. 14，Entry 11（书页 258）。证明用 Berndt [4] 的变换定理 3(i) 与 Lerch zeta 函数；(11.1) 对 $n$ 的两端均为偶函数，故在 $0 < |n| < \beta/2$ 成立后由连续性得 $|n| < \beta/2$ 成立。

**状态。** 已证明。

**对照。** M06（Lerch zeta 与模变换）；M02；M01（$\chi$ 加权与 Dirichlet $L$ 函数一线，见 Entry 21）。

**数值复核。** $\alpha = 2$、$\beta = \pi/2$、$n = 0.5$ 时两端差 $3.0\times 10^{-31}$。

## Entry 12

**陈述。** 设 $\alpha, \beta > 0$ 且 $\alpha\beta = \pi/2$，$0 < n < \pi/(2\alpha)$，则

$$\alpha\sum_{k=1}^{\infty}\chi(k)\frac{\sin(\alpha nk)}{\cosh(\alpha^2k)} = \beta\sum_{k=1}^{\infty}\chi(k)\frac{\sinh(\beta nk)}{\cosh(\beta^2k)}. \tag{12.1}$$

**出处。** Berndt Part II，Ch. 14，Entry 12（书页 260）。证明：Berndt [6, Eq. (4.23)] 证得 $0 < r < 1$、$\alpha\beta = \pi^2/16$ 时 $\sqrt{\alpha}\sum\chi(k)\sin(\pi rk/2)/\cosh(2\alpha k) = \sqrt{\beta}\sum\chi(k)\sinh(2\beta rk)/\cosh(2\beta k)$ (12.2)；代 $\alpha\to\alpha^2/2$、$\beta\to\beta^2/2$、$r = 2\alpha n/\pi$ 即得 (12.1)。

**状态。** 已证明。

**对照。** M02；M06。

**数值复核。** $\alpha = 2$、$\beta = \pi/4$、$n = 0.5$ 时两端差 $2.5\times 10^{-30}$。

**推论 (12.3)。** 设 $\alpha, \beta, t > 0$ 且 $\alpha\beta = \pi/2$、$t = \alpha/\beta$，$C$ 为顶点 $\pm i$ 与 $\pm t$ 的正向平行四边形，$\varphi(z)$ 为整函数，对每个正整数 $N$ 定义 $f_N(z) = \varphi(4\beta Nz)/[\cosh(2\pi Nz)\cosh(2\pi iNz/t)]$，并设 $Nf_N(z)$ 在 $C$ 上有界趋于 0（$N\to\infty$），则

$$\alpha\sum_{k=1}^{\infty}\chi(k)\frac{\{\varphi(\alpha k)-\varphi(-\alpha k)\}}{\cosh(\alpha^2k)} + i\beta\sum_{k=1}^{\infty}\chi(k)\frac{\{\varphi(i\beta k)-\varphi(-i\beta k)\}}{\cosh(\beta^2k)} = 0. \tag{12.3}$$

Berndt 明言：**上述条目不是 Entry 12 的推论；事实上反过来才对**——取 $\varphi(z) = e^{inz}$（$n > 0$），(12.3) 即化为 (12.1)；$Nf_N(z)$ 在 $C$ 下半平面上有界趋于 0 当且仅当 $n < \pi/(2\alpha)$，恰为 Entry 12 的假设。文件此处按 Berndt 的说明记录，不称之为 Entry 12 的推论。

## Entry 13

**陈述。** 设 $\alpha, \beta > 0$ 且 $\alpha\beta = \pi^2$，$n$ 为大于 1 的整数，则

$$\alpha^n\sum_{k=1}^{\infty}\frac{k^{2n-1}}{e^{2\alpha k}-1} - (-\beta)^n\sum_{k=1}^{\infty}\frac{k^{2n-1}}{e^{2\beta k}-1} = \{\alpha^n-(-\beta)^n\}\frac{B_{2n}}{4n}.$$

**出处。** Berndt Part II，Ch. 14，Entry 13（书页 261）。拉马努金无证明陈述 [13, p. 269]、[16, p. 190]；首个已发表证明属 Rao–Ayyar [1]；Malurkar [1] 与 Hardy [3]、[7, pp. 537–539] 随后给出证明；后有 Nanjundiah [1]、J. Lagrange [1]、Grosswald [2]、Sitaramachandrarao [2] 与 Berndt [2, Eq. (11.10)]、[6, Proposition 2.6] 的证明。

**状态。** 已证明（后人补证；拉马努金本人无证明）。

**对照。** M01（Bernoulli 数 $B_{2n}$，见 M01 的 Bernoulli 数一节）；M02（$\sum k^{2n-1}/(e^{2\alpha k}-1)$ 型级数）；M06（Eisenstein 级数源头）。

**数值复核。** $\alpha = 2$、$\beta = \pi^2/2$、$n = 2$ 时两端差 0。

**推论 (i)。** $\sum_{k=1}^{\infty}k^5/(e^{2\pi k}-1) = 1/504$。

**推论 (ii)。** $\sum_{k=1}^{\infty}k^9/(e^{2\pi k}-1) = 1/264$。

**推论 (iii)。** $\sum_{k=1}^{\infty}k^{13}/(e^{2\pi k}-1) = 1/24$。见于致 Hardy 的信 [16, p. xxvi]。

**推论 (iv)。**

$$\sum_{k=1}^{\infty}\frac{k^{4n+1}}{e^{2\pi k}-1} = \frac{B_{4n+2}}{8n+4}. \tag{13.1}$$

首证 Glaisher 1889。另有 (13.2)：$\sum_{k=1}^{\infty}\sigma_v(k)e^{-ky} = \sum_{d=1}^{\infty}d^v/(e^{dy}-1)$，此形式见于 Hurwitz 1881 年论文。

**数值复核。** 推论 (i)(ii)(iii) nsum 差均为 0；推论 (iv) 在 $n = 3$ 时（即 $\sum k^{13}/(e^{2\pi k}-1) = B_{14}/28 = 1/24$）差 0。

## Entry 14

**陈述。** 设 $\alpha, \beta > 0$ 且 $\alpha\beta = \pi^2$，$n$ 为任意正整数，则

$$\alpha^n\sum_{k=1}^{\infty}\chi(k)\frac{k^{2n-1}}{\cosh(\alpha k/2)} + (-\beta)^n\sum_{k=1}^{\infty}\chi(k)\frac{k^{2n-1}}{\cosh(\beta k/2)} = 0. \tag{14.1}$$

**出处。** Berndt Part II，Ch. 14，Entry 14（书页 262）。证明见 Malurkar [1]、Nanjundiah [1]、Berndt [6, Proposition 4.7]。

**状态。** 已证明（后人补证）。

**对照。** M01（$\chi$ 与 Dirichlet $L$ 函数）；M02；与 Entry 21(ii) 的 $n < 0$ 情形互见（见该条）。

**数值复核。** $\alpha = 2$、$\beta = \pi^2/2$、$n = 1$ 时左端 $= 2.0\times 10^{-31}$（即 0）。

**推论 (14.2)。** 对正整数 $n$，

$$\sum_{k=0}^{\infty}\frac{(-1)^k(2k+1)^{4n-1}}{\cosh\{(2k+1)\pi/2\}} = 0.$$

首证 Cauchy [1, pp. 313, 362]；拉马努金投稿题 [2]。

**数值复核。** $n = 1$ 时 nsum 得 $-1.1\times 10^{-36}$（即 0）。

## Entry 15

**陈述。** 设 $\alpha, \beta > 0$ 且 $\alpha\beta = \pi^2/4$，则

$$2\sum_{n=1}^{\infty}\chi(n)\tan^{-1}(e^{-\alpha n}) + 2\sum_{n=1}^{\infty}\chi(n)\tan^{-1}(e^{-\beta n}) = \sum_{n=1}^{\infty}\chi(n)\frac{\mathrm{sech}(\alpha n)}{n} + \sum_{n=1}^{\infty}\chi(n)\frac{\mathrm{sech}(\beta n)}{n} = \frac{\pi}{4}. \tag{15.1}$$

**推论。** $\sum_{n=1}^{\infty}\chi(n)\tan^{-1}(e^{-\pi n/2}) = \pi/16$。

**出处。** Berndt Part II，Ch. 14，Entry 15（书页 262）。

**状态。** 已证明。另注：(15.1) 的后一等式是 Entry 21(ii) 在 $n = 0$ 时的特例（见该条）。

**对照。** M02；M04（$\pi/16$、$\pi/4$）；M01（$\chi$ 加权）。

**数值复核。** $\alpha = \beta = \pi/2$ 时三端均为 $\pi/4$，差 $9.9\times 10^{-32}$；推论差 $2.5\times 10^{-32}$。

## Entry 16(i)

**陈述。** 设 $m, n$ 为非负整数，则

$$\int_0^{\infty}\frac{\sin^{2n+1}x}{x}\cos^{2m}x\,dx = \frac{\Gamma(m+\frac12)\Gamma(n+\frac12)}{2\Gamma(m+n+1)} = \int_0^{\infty}\frac{\sin^{2n+2}x}{x^2}\cos^{2m}x\,dx.$$

**出处。** Berndt Part II，Ch. 14，Entry 16(i)（书页 263）。

**状态。** 已证明。

**对照。** M09（正弦幂积分）；M02（与 Entry 5(i)(ii) 对照：$m = 0$ 时两式即 Entry 5 的积分形式）；M10（Gamma 商）。

**数值复核。** $m = 1$、$n = 1$ 时积分 $= \pi/16$：被积函数经三角展开化为 Dirichlet 积分 $\int_0^{\infty}\sin(ax)/x\,dx = \pi/2$ 逐项验证，精确成立；有限上限求积亦收敛至该值（$T = 200$ 时差 $1.9\times 10^{-3}$，为 $1/T$ 型振荡尾项）。

## Entry 16(ii)

**陈述。** 设 $n, p$ 为非负整数，则

$$\int_0^{\infty}\frac{\sin^{2n+1}x}{x}\cos(2px)\,dx = (-1)^p\frac{\sqrt{\pi}}{2}\cdot\frac{\Gamma(n+1)\Gamma(n+\frac12)}{\Gamma(n-p+1)\Gamma(n+p+1)} = \int_0^{\infty}\frac{\sin^{2n+2}x}{x^2}\cos(2px)\,dx.$$

$p = 0$ 的情形与 Entry 5(i)(ii) 对照。

**出处。** Berndt Part II，Ch. 14，Entry 16(ii)（书页 264）。证明：$p = 0$ 时由 Entry 16(i) 得；$p > 0$ 时对 $n$ 归纳，用 $2\sin^2x = 1-\cos(2x)$ 与 $2\cos(2x)\cos(2px) = \cos\{2(p+1)x\}+\cos\{2(p-1)x\}$ 及 $\Gamma$ 的函数方程。

**状态。** 已证明。

**对照。** M09；M02；M10。

**数值复核。** $n = 1$、$p = 1$ 时积分 $= -\pi/8$，$n = 2$、$p = 0$ 时 $= 3\pi/16$：均经三角展开化为 Dirichlet 积分逐项验证，精确成立。

## Entry 17(i)

**陈述。** 设 $\alpha, \beta, n > 0$ 且 $\alpha\beta = 2\pi$，$\pi/(2\alpha)$ 不是整数，$m = [\pi/(2\alpha)]$（取整），$p$ 为实数，则

$$\alpha\left\{\frac{1}{2}+\sum_{k=1}^{m}\cos^n(\alpha k)\cos(\alpha pk)\right\} = \frac{\pi n!}{2^{n+1}}\left\{\frac{1}{\Gamma\{\frac12(n+p)+1\}\Gamma\{\frac12(n-p)+1\}} + \sum_{k=1}^{\infty}\left(\frac{1}{\Gamma\{\frac12(n-p+\beta k)+1\}\Gamma\{\frac12(n+p-\beta k)+1\}} + \frac{1}{\Gamma\{\frac12(n+p+\beta k)+1\}\Gamma\{\frac12(n-p-\beta k)+1\}}\right)\right\}. \tag{17.1}$$

(17.1) 右端按 Stirling 公式对 $n > 0$ 绝对收敛。证明用 Poisson 公式 (6.1) 与 Gradshteyn–Ryzhik [1, p. 372] 的积分 (17.3)：$\int_0^{\pi/2}\cos^{v-1}x\cos(ax)\,dx = \pi\Gamma(v+1)/[2^vv\Gamma\{\frac12(v+a+1)\}\Gamma\{\frac12(v-a+1)\}]$（$v > 0$）。

**出处。** Berndt Part II，Ch. 14，Entry 17(i)（书页 264）。

**状态。** 已证明。

**对照。** M10（Gamma 分母展开）；M02（$\cos^n$ 有限和）；M09（Poisson 求和）。

**数值复核。** $\alpha = \beta = \sqrt{2\pi}$、$n = 1$、$p = 0$ 时两端差 $2.0\times 10^{-31}$。

**推论 1 (17.6)。** 设 $\alpha = \pi/(n+j)$，$n, j$ 为奇偶性不同的正整数，则

$$\frac{1}{2}+\sum_{k=1}^{m}\cos^{2n}(\alpha k) = \frac{\sqrt{\pi}\,\Gamma(n+\frac12)}{2\alpha n!}.$$

**推论 2 (17.7)。** 设 $\alpha = \pi/(n-j)$，$0\le j\le (n-1)/2$，则

$$\alpha\left\{\frac{1}{2}+\sum_{k=1}^{m}\cos^{2n}(\alpha k)\right\} = \frac{\sqrt{\pi}\,\Gamma(n+\frac12)}{2n!}\left\{1+\frac{2(n!)^2}{\Gamma(n+1+\pi/\alpha)\Gamma(n+1-\pi/\alpha)}\right\}.$$

**拉马努金原文错误（Berndt 注明）。** 拉马努金称 (17.6) 对 $0\le\alpha\le\pi/(n+1)$ 成立、(17.7) 对 $\pi/n\le\alpha\le 2\pi/(n+1)$ 成立，均不成立。反例：$n = 1$、$\alpha = 2\pi/5$ 时 (17.6) 左端减右端 $= (1/10)(1-\sec(\pi/5))\ne 0$；$n = 3$、$\alpha = 2\pi/5$ 时 (17.7) 的差 $= (1/10)\{(4-\sqrt5)/45-4^4/(2079\pi)\}\ne 0$。本文件按 Berndt 的说明记录，推论 1、2 只在所述 $\alpha$ 取值下成立。

**数值复核。** 推论 1 在 $n = 1$、$j = 2$ 与 $n = 2$、$j = 1$ 时差均为 0；推论 2 在 $n = 2$、$j = 0$ 时差 0。

## Entry 17(ii)

**陈述。** 设 $\alpha, \beta, n > 0$ 且 $\alpha\beta = \pi/2$，$\pi/(2\alpha)$ 不是奇整数，$m = [\pi/(2\alpha)]$，$p$ 为实数，则

$$\alpha\sum_{k=1}^{m}\chi(k)\cos^n(\alpha k)\sin(\alpha pk) = \frac{\pi n!}{2^{2n+2}}\sum_{k=1}^{\infty}\chi(k)\left\{\frac{1}{\Gamma\{\frac12(n-p+\beta k)+1\}\Gamma\{\frac12(n+p-\beta k)+1\}} - \frac{1}{\Gamma\{\frac12(n+p+\beta k)+1\}\Gamma\{\frac12(n-p-\beta k)+1\}}\right\}. \tag{17.4}$$

**本轮发现的原书印文问题（待核对）。** 上式按印文（系数 $\pi n!/2^{2n+2}$）数值不成立：$\alpha = 1$、$\beta = \pi/2$、$n = 1$、$p = 1$ 时左端 $0.4546487134$、印文右端 $0.2273257002$，左端恰为右端的 2 倍；$n = 2$ 时比值恰为 4；$n = 3$ 时比值恰为 8；另三组参数（$n = 1$、$p = 2$；$n = 1$、$p = 0.5$、$\alpha = 0.7$；$n = 2$、$p = 0.3$、$\alpha = 0.9$）比值亦恰为 $2^n$。**订正系数应为 $\pi n!/2^{n+2}$**：七组参数下订正版差 $5\times 10^{-13}$–$3\times 10^{-9}$（余差为 $k^{-n-2}$ 型级数尾项）。300 DPI 放大图确认印文确为 $2^{2n+2}$。是否见于其他印次或勘误表，待核对。

**出处。** Berndt Part II，Ch. 14，Entry 17(ii)（书页 265）。

**状态。** 印文存疑（见上）；订正版已证明（数值复核通过，待独立核对）。

**对照。** M10；M02；M06（$\chi$ 加权）。

## Entry 18

**陈述。** 设 $\varphi(x) = \sum_n P_n/(p_n-a_nx)$、$\psi(y) = \sum_n Q_n/(q_n-b_ny)$，则

$$\varphi(x)\psi(y) = \sum_n\frac{P_n}{p_n-a_nx}\cdot\psi\left(\frac{p_ny}{a_nx}\right) + \sum_n\frac{Q_n}{q_n-b_ny}\cdot\varphi\left(\frac{q_nx}{b_ny}\right), \tag{18.1}$$

只要至少一侧的双重级数绝对收敛。

**出处。** Berndt Part II，Ch. 14，Entry 18（书页 267）。证明用留数定理（书中 (18.4)、(18.5) 的推导）。

**状态。** 已证明（在绝对收敛假设下）。本条是本章部分分式主线的主恒等式，Entry 19、20 均由其导出。

**对照。** M02（部分分式主线）；M09（Ch. 9 的部分分式与之同源）；M01（推论中的 $\chi$ 加权与 Dirichlet 特征）。

**推论 1。** 设 $|\theta|, |\varphi| < \pi$，$x/y$ 不是纯虚数，则

$$\frac{\pi^2n^2xy\cos(\theta nx)\cosh(\varphi ny)}{\sin(\pi nx)\sinh(\pi ny)} = 1+2\pi n^2xy\sum_{k=1}^{\infty}\frac{(-1)^k k\cos(k\varphi)\cosh(k\theta x/y)}{(k^2+n^2y^2)\sinh(\pi kx/y)} - 2\pi n^2xy\sum_{k=1}^{\infty}\frac{(-1)^k k\cos(k\theta)\cosh(k\varphi y/x)}{(k^2-n^2x^2)\sinh(\pi ky/x)}.$$

**推论 2。** 设 $|\theta|, |\varphi|\le\pi/2$，则

$$\frac{\pi\sin(\theta nx)\sinh(\varphi ny)}{4n^2\cos(\pi nx/2)\cosh(\pi ny/2)} = y^2\sum_{k=1}^{\infty}\chi(k)\frac{\sin(k\varphi)\sinh(k\theta x/y)}{k(k^2+n^2y^2)\cosh(\pi kx/(2y))} + x^2\sum_{k=1}^{\infty}\chi(k)\frac{\sin(k\theta)\sinh(k\varphi y/x)}{k(k^2-n^2x^2)\cosh(\pi ky/(2x))}. \tag{18.2}$$

**推论 3。**

$$\frac{\pi\cos(\theta nx)\sinh(\varphi ny)}{4\sin(\pi nx/2)\cosh(\pi ny/2)} = \frac{\varphi y}{2x} + n^2y^2\sum_{k=0}^{\infty}\frac{(-1)^{k+1}\sin\{(2k+1)\varphi\}\cosh\{(2k+1)\theta x/y\}}{(2k+1)\{(2k+1)^2+n^2y^2\}\sinh\{(2k+1)\pi x/(2y)\}} + n^2x^2\sum_{k=1}^{\infty}\frac{(-1)^{k+1}\cos(2k\theta)\sinh(2k\varphi y/x)}{2k\{(2k)^2-n^2x^2\}\cosh(\pi ky/x)}. \tag{18.3}$$

**数值复核。** 推论 1、2、3 取 $\theta = \varphi = 0.5$、$n = 1$、$x = 0.5$、$y = 2$ 时差分别为 $5.4\times 10^{-31}$、$9.2\times 10^{-33}$、$3.0\times 10^{-31}$。

## Entry 19(i)

**陈述。**

$$\pi^2xy\cot(\pi x)\coth(\pi y) = 1+2\pi xy\sum_{n=1}^{\infty}\frac{n\coth(\pi nx/y)}{n^2+y^2} - 2\pi xy\sum_{n=1}^{\infty}\frac{n\coth(\pi ny/x)}{n^2-x^2}. \tag{19.1}$$

**拉马努金原文的问题（Berndt 注明）。** Berndt 明言：(19.1) 未附任何假设地陈述，但一般情形下右端两级数不收敛。拉马努金显然用 Entry 18 导出 (19.1)，Berndt 亦形式地如此推导（用 (1.9) 的 $\pi x\cot(\pi x) = 1+x^2\sum_{n\ne 0}1/(nx-n^2)$ 与 $\pi y\coth(\pi y) = 1+y^2\sum_{n\ne 0}1/(n^2-iny)$，对 $\varphi(x) = \pi x\cot(\pi x)-1$、$\psi(y) = \pi y\coth(\pi y)-1$ 用 Entry 18，忽略所得双重级数发散的事实）。

**Sitaramachandrarao 的修正版 (19.3)。**

$$\pi^2xy\cot(\pi x)\coth(\pi y) = 1+\frac{\pi^2}{3}(y^2-x^2) - 2\pi xy^3\sum_{n=1}^{\infty}\frac{\coth(\pi nx/y)}{n(n^2+y^2)} - 2\pi x^3y\sum_{n=1}^{\infty}\frac{\coth(\pi ny/x)}{n(n^2-x^2)}. \tag{19.3}$$

**出处。** Berndt Part II，Ch. 14，Entry 19(i)（书页 271）。修正版见 Sitaramachandrarao [1]、[2]。

**状态。** (19.1) 按字面一般不成立（级数发散）；修正版 (19.3) 已证明。

**对照。** M02（部分分式）；M09（Ch. 9 的 $\cot$ 部分分式 (1.9)）。

**数值复核。** 修正版 (19.3) 取 $x = 0.3$、$y = 0.7$ 时 nsum 差 $3.9\times 10^{-31}$。

## Entry 19(ii)

**陈述。** 设 $x/y$ 不是纯虚数，则

$$\pi^2xy\csc(\pi x)\mathrm{csch}(\pi y) = 1+2\pi xy\sum_{n=1}^{\infty}\frac{(-1)^n n\,\mathrm{csch}(\pi nx/y)}{n^2+y^2} - 2\pi xy\sum_{n=1}^{\infty}\frac{(-1)^n n\,\mathrm{csch}(\pi ny/x)}{n^2-x^2}.$$

**出处。** Berndt Part II，Ch. 14，Entry 19(ii)（书页 272）。

**状态。** 已证明。

**对照。** M02。

**数值复核。** $x = 0.3$、$y = 0.7$ 时两端差 $9.9\times 10^{-32}$。

## Entry 19(iii)

**陈述。** 设 $y/x$ 不是纯虚数，则

$$\frac{\pi}{4}\tan\left(\frac{\pi x}{2}\right)\tanh\left(\frac{\pi y}{2}\right) = y^2\sum_{n=0}^{\infty}\frac{\tanh\{(2n+1)\pi x/(2y)\}}{(2n+1)\{(2n+1)^2+y^2\}} + x^2\sum_{n=0}^{\infty}\frac{\tanh\{(2n+1)\pi y/(2x)\}}{(2n+1)\{(2n+1)^2-x^2\}}.$$

**出处。** Berndt Part II，Ch. 14，Entry 19(iii)（书页 272）。

**状态。** 已证明。

**对照。** M02。

**数值复核。** $x = 0.3$、$y = 0.7$ 时 nsum 差 0。

## Entry 19(iv)

**陈述。**

$$\frac{\pi}{4}\sec\left(\frac{\pi x}{2}\right)\mathrm{sech}\left(\frac{\pi y}{2}\right) = \sum_{n=1}^{\infty}\chi(n)\frac{n\,\mathrm{sech}\{\pi nx/(2y)\}}{n^2+y^2} + \sum_{n=1}^{\infty}\chi(n)\frac{n\,\mathrm{sech}\{\pi ny/(2x)\}}{n^2-x^2}.$$

**出处。** Berndt Part II，Ch. 14，Entry 19(iv)（书页 273）。

**状态。** 已证明。

**对照。** M02；M01（$\chi$ 加权）。

**数值复核。** $x = 0.3$、$y = 0.7$ 时两端差 $9.9\times 10^{-32}$。

## Entry 19(v)

**陈述。**

$$\frac{\pi}{4}\cot\left(\frac{\pi x}{2}\right)\mathrm{sech}\left(\frac{\pi y}{2}\right) = \frac{1}{2x} - y\sum_{n=1}^{\infty}\chi(n)\frac{\coth\{\pi nx/(2y)\}}{n^2+y^2} - x\sum_{n=1}^{\infty}\frac{\mathrm{sech}(\pi ny/x)}{(2n)^2-x^2}.$$

拉马努金另注 $\tan(\pi x/2)\coth(\pi y/2)$、$\sec(\pi x/2)\coth(\pi y/2)$ 有类似公式。

**出处。** Berndt Part II，Ch. 14，Entry 19(v)（书页 273）。

**状态。** 已证明。

**对照。** M02；M01。

**数值复核。** $x = 0.3$、$y = 0.7$ 时直接求和至 $N = 5000$ 差 $1.4\times 10^{-8}$（$\chi$ 分块交错级数的 $1/N^2$ 型尾项；nsum 对此类级数会误外推，见小结）。

## Entry 20(i)

**陈述。**

$$\pi^2z^2\cot(\pi z)\coth(\pi z) = 1-4\pi z^4\sum_{n=1}^{\infty}\frac{n\coth(\pi n)}{n^4-z^4}.$$

正确证明取自修正版 (19.3) 而非 (19.1)（后者在 $x = y$ 时不收敛）。

**推论。**

$$\pi^2z^2\frac{\cosh(\pi z\sqrt2)+\cos(\pi z\sqrt2)}{\cosh(\pi z\sqrt2)-\cos(\pi z\sqrt2)} = 1+4\pi z^4\sum_{n=1}^{\infty}\frac{n\coth(\pi n)}{n^4+z^4}.$$

**出处。** Berndt Part II，Ch. 14，Entry 20(i)（书页 274）。

**状态。** 已证明。

**对照。** M02；M09（$x = y$ 的对角特例）。

**数值复核。** $z = 0.3$ 时主式与推论 nsum 差均为 $2.0\times 10^{-31}$。

## Entry 20(ii)

**陈述。**

$$\pi^2z^2\csc(\pi z)\mathrm{csch}(\pi z) = 1-4\pi z^4\sum_{n=1}^{\infty}\frac{(-1)^n n\,\mathrm{csch}(\pi n)}{n^4-z^4}.$$

**推论。**

$$\frac{2\pi^2z^2}{\cosh(\pi z\sqrt2)-\cos(\pi z\sqrt2)} = 1+4\pi z^4\sum_{n=1}^{\infty}\frac{(-1)^n n\,\mathrm{csch}(\pi n)}{n^4+z^4}.$$

**出处。** Berndt Part II，Ch. 14，Entry 20(ii)（书页 275）。

**状态。** 已证明。

**对照。** M02。

**数值复核。** $z = 0.3$ 时主式差 $2.0\times 10^{-31}$，推论差 0。

## Entry 20(iii)

**陈述。**

$$\frac{\pi}{8z^2}\tan\left(\frac{\pi z}{2}\right)\tanh\left(\frac{\pi z}{2}\right) = \sum_{n=0}^{\infty}\frac{(2n+1)\tanh\{(2n+1)\pi/2\}}{(2n+1)^4-z^4}.$$

**推论。**

$$\frac{\pi}{8z^2}\cdot\frac{\cosh(\pi z/\sqrt2)-\cos(\pi z/\sqrt2)}{\cosh(\pi z/\sqrt2)+\cos(\pi z/\sqrt2)} = \sum_{n=0}^{\infty}\frac{(2n+1)\tanh\{(2n+1)\pi/2\}}{(2n+1)^4+z^4}.$$

**出处。** Berndt Part II，Ch. 14，Entry 20(iii)（书页 275）。

**状态。** 已证明。

**对照。** M02。

**数值复核。** $z = 0.3$ 时主式与推论 nsum 差均为 $9.9\times 10^{-32}$。

## Entry 20(iv)

**陈述。**

$$\frac{\pi}{8}\sec\left(\frac{\pi z}{2}\right)\mathrm{sech}\left(\frac{\pi z}{2}\right) = \sum_{n=1}^{\infty}\chi(n)\frac{n^3\mathrm{sech}(\pi n/2)}{n^4-z^4}.$$

**推论。**

$$\frac{\pi/4}{\cosh(\pi z/\sqrt2)+\cos(\pi z/\sqrt2)} = \sum_{n=1}^{\infty}\chi(n)\frac{n^3\mathrm{sech}(\pi n/2)}{n^4+z^4}.$$

**出处。** Berndt Part II，Ch. 14，Entry 20(iv)（书页 275）。

**状态。** 已证明。

**对照。** M02；M01。

**数值复核。** $z = 0.3$ 时主式差 0，推论差 $9.9\times 10^{-32}$。

## Entry 21(i)

**陈述。** 设 $\alpha, \beta > 0$ 且 $\alpha\beta = \pi^2$，$n$ 为任意非零整数，则

$$\alpha^{-n}\left\{\frac{1}{2}\zeta(2n+1)+\sum_{k=1}^{\infty}\frac{k^{-2n-1}}{e^{2\alpha k}-1}\right\} = (-\beta)^{-n}\left\{\frac{1}{2}\zeta(2n+1)+\sum_{k=1}^{\infty}\frac{k^{-2n-1}}{e^{2\beta k}-1}\right\} - 2^{2n}\sum_{k=0}^{n+1}(-1)^k\frac{B_{2k}}{(2k)!}\cdot\frac{B_{2n+2-2k}}{(2n+2-2k)!}\alpha^{n+1-k}\beta^k,$$

其中 $B_j$ 为 Bernoulli 数。

**出处。** Berndt Part II，Ch. 14，Entry 21(i)（书页 275–276）。Berndt 称其为“perhaps the most well-known result in Chapter 14”（本章最著名的结果）。$\alpha = \beta = \pi$、$n$ 为奇正数时首证 Lerch [1]；一般情形首证 Malurkar [1]；另有 Grosswald [1]、[2]、Smart [1]、Katayama [1]、[4]、Riesel [1]、S. N. Rao [1]、N. Zhang [1]、Sitaramachandrarao [2]、Berndt [5]、[6] 等的证明；Guinand [1]、[2]、Apostol [1]、Mikolás [1]、Iseki [1]、Chandrasekharan–Narasimhan [1]、Glaeske [1]、[2]、Bodendiek [1]、Bodendiek–Halbritter [1] 实质上亦已证明。$n < -1$ 时本条化归 Entry 13（$n$ 换为 $-n$）。

**状态。** 已证明。

**对照。** M01（$\zeta(2n+1)$ 与 Bernoulli 数的核心公式）；M02；M06（模变换）；M12（渐近一线亦用此式）。

**数值复核。** 特例 $\alpha = \beta = \pi$、$n = 1$：$\sum k^{-3}/(e^{2\pi k}-1) = 7\pi^3/360-\zeta(3)/2$，差 $1.3\times 10^{-26}$；一般情形 $\alpha = 2$、$\beta = \pi^2/2$、$n = 1$ 时差 $6.3\times 10^{-24}$。

## Entry 21(ii)

**陈述。** 设 $\alpha, \beta > 0$ 且 $\alpha\beta = \pi^2/4$，$n$ 为任意整数，则

$$\alpha^{-n}\sum_{k=1}^{\infty}\chi(k)\frac{\mathrm{sech}(\alpha k)}{k^{2n+1}} + (-\beta)^{-n}\sum_{k=1}^{\infty}\chi(k)\frac{\mathrm{sech}(\beta k)}{k^{2n+1}} = \frac{\pi}{4}\sum_{k=0}^{n}(-1)^k\frac{E_{2k}}{(2k)!}\cdot\frac{E_{2n-2k}}{(2n-2k)!}\alpha^{n-k}\beta^k,$$

其中 $E_j$ 为 Euler 数（$E_0 = 1$、$E_2 = -1$、$E_4 = 5$、$E_6 = -61$）。

**出处。** Berndt Part II，Ch. 14，Entry 21(ii)（书页 276）。首个证明属 Malurkar [1]，后有 Nanjundiah [1] 与 Berndt [6, Proposition 4.5]。另注：Entry 15 的后一等式是本条 $n = 0$ 的情形；$n < 0$ 时本条化归 Entry 14（参数 $n, \alpha, \beta$ 换为 $-n, \alpha/2, \beta/2$）。

**状态。** 已证明。

**对照。** M01（Euler 数与 Dirichlet $L$ 函数）；M02；M04（$n = 0$ 时右端 $\pi/4$，见 Entry 15）。

**数值复核。** $n = 0$、$\alpha = \beta = \pi/2$ 时两端 $= \pi/4$，差 $9.9\times 10^{-32}$；$n = 1$、$\alpha = 2$、$\beta = \pi^2/8$ 时两端 $= -0.300925090268$，差 $1.5\times 10^{-31}$。注：mpmath 的 `euler(n)` 并非此处 Euler 数（其 `euler(0)` 得 Euler–Mascheroni 常数 $\gamma$），复核用 $E_{2k} = 2^{2k}E_{2k}(1/2)$（Euler 多项式在 $1/2$ 处的值）计算。

## Entry 21(iii)

**陈述。** 设 $\alpha, \beta > 0$ 且 $\alpha\beta = \pi^2$，$n$ 为任意整数，则

$$\alpha^{-n+1/2}\left\{\frac{1}{2}L(2n)+\sum_{k=1}^{\infty}\frac{\chi(k)}{k^{2n}(e^{\alpha k}-1)}\right\} = \frac{(-1)^n\beta^{-n+1/2}}{2^{2n+1}}\sum_{k=1}^{\infty}\frac{1}{k^{2n}\cosh(\beta k)} + \frac{1}{4}\sum_{k=0}^{n}\frac{(-1)^k}{2^{2k}}\cdot\frac{E_{2k}}{(2k)!}\cdot\frac{E_{2n-2k}}{(2n-2k)!}\alpha^{n-k}\beta^{k+1/2},$$

其中 $L(s) = \sum_{n=1}^{\infty}\chi(n)n^{-s}$ (21.1) 为与本原特征 $\chi$ 相伴的 Dirichlet $L$ 函数，可解析延拓为整函数。

**出处。** Berndt Part II，Ch. 14，Entry 21(iii)（书页 277）。首个已发表证明属 Chowla [1, Eq. (1.2)]；Berndt [6, Eq. (3.20)] 亦有证明，但该式有误：末尾的 $(\beta/8)^k$ 应改为 $\beta^{k+1/2}2^{-4k}$；另见 Katayama [2]、[3]。

**状态。** 已证明。

**对照。** M01（Dirichlet $L$ 函数与 Euler 数）；M02。

**数值复核。** $n = 0$、$\alpha = \beta = \pi$ 时两端 $= 0.523024810027$，差 0（其中 $L(0) = 1/2$ 取解析延拓值；直接部分和 $\sum_{k\le N}\chi(k)$ 得 0，不可代入）。

## Entry 22(i)

**陈述。** 设 $x, y$ 为复数，$y/x$ 不是纯虚数，则

$$\pi^2xy\frac{\cosh\{\pi(x+y)\sqrt2\}+\cos\{\pi(x-y)\sqrt2\}-\cosh\{\pi(x-y)\sqrt2\}-\cos\{\pi(x+y)\sqrt2\}}{\{\cosh(\pi x\sqrt2)-\cos(\pi x\sqrt2)\}\{\cosh(\pi y\sqrt2)-\cos(\pi y\sqrt2)\}} = 2+4\pi xy^3\sum_{n=1}^{\infty}\frac{n\coth(\pi nx/y)}{n^4+y^4} + 4\pi x^3y\sum_{n=1}^{\infty}\frac{n\coth(\pi ny/x)}{n^4+x^4}. \tag{22.1}$$

**拉马努金原文错误（Berndt 注明）。** 笔记版略有错误：拉马努金把左端分子写成乘积 $\cosh\{\pi(x+y)\sqrt2\}\cos\{\pi(x-y)\sqrt2\} - \cosh\{\pi(x-y)\sqrt2\}\cos\{\pi(x+y)\sqrt2\}$（两项之积的差，而非四项之和差）。(22.2) 形式上可由 Entry 19(i) 导出。

**出处。** Berndt Part II，Ch. 14，Entry 22(i)（书页 277）。证明：对 $zf(z) = \pi^2\cot(\pi zx)\coth(\pi zy)$ 与 $zg(z) = \pi^2\cot(\pi zy)\coth(\pi zx)$ 作部分分式展开。

**状态。** 已证明（笔记版已订正）。

**对照。** M02；M09（部分分式）。

**数值复核。** $x = 0.3$、$y = 0.7$ 时 nsum 差 $7.9\times 10^{-31}$。

## Entry 22(ii)

**陈述。** 设 $n\ge 0$ 为整数，则

$$\int_0^{\infty}\frac{\cos(2nx)}{\cosh(\pi\sqrt{x})+\cos(\pi\sqrt{x})}\,dx = \sum_{k=1}^{\infty}\chi(k)\frac{k}{\cosh(\pi k/2)}e^{-nk^2}. \tag{22.6}$$

**出处。** Berndt Part II，Ch. 14，Entry 22(ii)（书页 278）。证明用留数定理与 $\int_0^{\infty}\cos(2nx)/(x^2+b^2)\,dx = \pi/(2b)e^{-2nb}$（$a\ge 0$、$b > 0$）。

**状态。** 已证明。

**对照。** M09（双曲积分）；M02（右端 $\chi$ 加权级数）；M06。

**数值复核。** $n = 0$ 时两端 $= 0.348300982421$，差 $4.9\times 10^{-32}$；$n = 1$ 时差 $5.4\times 10^{-10}$（积分换元 $x = t^2$ 后求积；直接对原式求积会因 $\sqrt{x}$ 振荡而失真）。

**推论 (22.8)。** 设 $\alpha, \beta > 0$ 且 $\alpha\beta = \pi^3/4$，则

$$\sum_{n=1}^{\infty}\frac{\chi(n)}{n\{\cosh\sqrt{\alpha n}+\cos\sqrt{\alpha n}\}} + \sum_{n=1}^{\infty}\frac{\chi(n)}{n\cosh(\pi n/2)\cosh^2(\beta n^2)} = \frac{\pi}{8}. \tag{22.8}$$

拉马努金称其为 Entry 22(ii) 的推论，Berndt 无法证实，另从头证明。

**本轮发现的原书印文问题（待核对）。** 上式按印文（第二求和含 $\cosh^2(\beta n^2)$）数值不成立：$\alpha = \beta = \pi^{3/2}/2$ 时左端 $= 0.349680991911$，右端 $\pi/8 = 0.392699081699$，差 $0.043$。**订正为 $\cosh(\beta n^2)$（去掉平方）后左端 $= 0.392699081699$，差 $5.9\times 10^{-31}$**；书中本条证明（书页 280）的留数公式 $R((2n+1)(\pm 1+i)/(2N)) = (-1)^{n+1}/[\pi(2n+1)\cosh\{(2n+1)\pi/2\}\cosh\{(2n+1)^2\beta\}]$ 亦为单 $\cosh$，与订正版一致。300 DPI 放大图确认印文确为 $\cosh^2(\beta n^2)$。是否见于其他印次或勘误表，待核对。

## Entry 22(iii)

**陈述。** 设 $\alpha, \beta > 0$ 且 $\alpha\beta = 4\pi^3$，$\gamma$ 为 Euler 常数，则

$$\frac{7\alpha}{720}+\frac{1}{2}\sum_{n=1}^{\infty}\frac{\cos\sqrt{\alpha n}}{n(\cosh\sqrt{\alpha n}-\cos\sqrt{\alpha n})} = \frac{\gamma+\mathrm{Log}(2\pi/\beta)}{4}+\frac{\beta}{48\pi}+\sum_{n=1}^{\infty}\frac{1}{n(e^{2\pi n}-1)}+\sum_{n=1}^{\infty}\frac{\coth(\pi n)}{n(e^{\beta n^2}-1)}. \tag{22.10}$$

另有 (22.11)：

$$\sum_{n=1}^{\infty}\frac{1}{n(e^{2\pi n}-1)} = \frac{1}{4}\mathrm{Log}\left(\frac{4}{\pi}\right)-\frac{\pi}{12}+\mathrm{Log}\,\Gamma\left(\frac{3}{4}\right).$$

(22.11) 的证明用 Whittaker–Watson [1, p. 488, problem 10] 的乘积 $\prod_{n=1}^{\infty}(1-q^{2n})^6 = 2kk'K^3/(\pi^3q^{1/2})$（$q = e^{-\pi}$，$k = k' = 1/\sqrt2$，$K = \pi^{3/2}/(2\Gamma^2(3/4))$）。

**拉马努金原文错误（Berndt 注明）。** 笔记版 (22.11) 有误印：$\mathrm{Log}\,\Gamma(3/4)$ 被写成 $\frac14\mathrm{Log}\,\Gamma(3/4)$。

**出处。** Berndt Part II，Ch. 14，Entry 22(iii)（书页 280）。

**状态。** 已证明（笔记版已订正）。

**对照。** M11（(22.11) 的证明用椭圆函数）；M01（Euler 常数 $\gamma$）；M02；M12（左端 $\cos\sqrt{\alpha n}$ 级数的 $e^{-\sqrt{\alpha n}}$ 型收敛）。

**数值复核。** (22.10) 取 $\alpha = \beta = 2\pi^{3/2}$ 时两端差 $2.5\times 10^{-32}$；(22.11) 两端差 $3.9\times 10^{-32}$。

## Entry 23(i)

**陈述。**

$$\frac{\varphi(0)}{4\pi}+\sum_{k=1}^{\infty}\sum_{n=0}^{\infty}k\coth(\pi k)(-1)^n(kx)^{4n}\varphi(4n) = \frac{\pi}{2x^2}\left\{\frac{1}{3}\varphi(-2)+h\right\}, \tag{23.1}$$

其中误差 $h$ 近似等于

$$\varphi(-2)+\sum_{n=0}^{\infty}\frac{(2\pi)^{2n+1}\cos\{3(2n+1)\pi/4\}\varphi(-2n-3)}{x^{2n+1}(2n+1)!}, \tag{23.2}$$

当 $x$ 很小时成立。（(23.1) 右端读作 $\varphi(2)$ 还是 $\varphi(-2)$，尚不清楚。）

**Berndt 的说明。** 不清楚应如何解释 Entry 23(i)；$x$ 的幂级数在 $x = 0$ 附近由 $1/x$ 的幂级数逼近，令人惊讶；(23.2) 许是 $h$ 的渐近级数；拉马努金几乎肯定以纯形式方式导出 (23.1)。Berndt 证明：拉马努金可能有误——形式论证似乎给出略有不同的公式。以下讨论多承 D. Zagier 协助。设 $\varphi(n) = \psi(n+2)$，$F(x) = \sum_{n=0}^{\infty}(-1)^n\psi(4n+2)x^{4n}$ (23.3)（拉马努金似乎默认 $F$ 为整函数），则 (23.1) 可改写为 $\psi(2)/(4\pi)+\sum k\coth(\pi k)F(kx) = \pi/(2x^2)\{(1/3)\psi(0)+h\}$ (23.4)。Zagier 的检验（取 $\psi(s) = \lambda^{-s}$）表明：误差 $h$ 实为拉马努金所称的两倍，且 (23.6) 多出一项幂级数 $2\sum_{n=1}^{\infty}(-1)^n(2u)^{4n}/(4n)!$；$h \approx G(2\pi/x\cdot e^{-\pi i/4})+G(2\pi/x\cdot e^{\pi i/4})$，其中 $G(t) = e^{-\lambda t}$ 为 $\Gamma(s)\lambda^{-s}$ 的逆 Mellin 变换。

**出处。** Berndt Part II，Ch. 14，Entry 23(i)（书页 283）。

**状态。** 形式公式，解释不明；Berndt 与 Zagier 的分析表明拉马努金所称的 $h$ 有误（实为两倍），(23.1) 的严格含义待核对。

**对照。** M12（形式渐近与误差分析）；M02；M06（Mellin 变换）。

## Entry 23(ii)

**陈述。**

$$\sum_{k=1}^{\infty}\sum_{n=0}^{\infty}k^{-1}\chi(k)\mathrm{sech}(\pi k/2)(-1)^n(kx)^{4n}\varphi(4n) = \frac{\pi}{8}\varphi(0)-\frac{\pi}{2}h, \tag{23.8}$$

其中 $h$ 近似等于 $\sum_{n=0}^{\infty}(-1)^n(\pi/\sqrt2)^n\varphi(-n)/(x^nn!)$。若双重级数绝对收敛，则 (23.8) 以 $h\equiv 0$ 成立（用 Entry 14 推论与 Entry 15 证明）。

**Zagier 的分析。** 设 $\varphi(s) = (1/\Gamma(s))\int_0^{\infty}G(t)t^{s-1}\,dt$，则 (23.8) 可改写为 $\sum_{k=1}^{\infty}\chi(k)F(kx)/(k\cosh(\pi k/2)) = \pi/8\cdot\varphi(0)-\pi/2\cdot h$ (23.9)，其中 $h\approx G(\pi/(x\sqrt2))$ (23.10)。情形 1（$G$ 紧支集）→ $h\equiv 0$，与上段一致；情形 2（$\varphi(s) = \lambda^{-s}$）→ $h = 2/[\cosh(u/\sqrt2)+\cos(u/\sqrt2)] = G(\pi/(x\sqrt2))+O(e^{-u\sqrt2})$ (23.11)，$u = \pi\lambda/x$。一般式 (23.12)：$h = \sum_{j=1}^{\infty}(-1)^{j-1}\sum_{|k|\le j-1,\,k\equiv j-1\bmod 2}G((j+ik)\pi/(x\sqrt2))$。例：$G(z) = ze^{-cz^2}$ → $\varphi(s) = c^{-(s+1)/2}\sqrt{\pi}/[2^s\Gamma(s/2)]$，$H(u) = \sqrt{\pi}u/(4c^{3/2})e^{-u^2/(4c)}$，终得 $(x^3/c^{3/2})\sum_{k=1}^{\infty}\chi(k)k\sin(k^2x^2/(4c))/\cosh(\pi k/2) = (2\pi^3)^{1/2}\sum_{j=1}^{\infty}(-1)^{j-1}\sum_{|k|\le j-1}(j+ik)\exp(-c(j+ik)^2\pi^2/(2x^2))$。

**出处。** Berndt Part II，Ch. 14，Entry 23(ii)（书页 285）。

**状态。** 形式公式；绝对收敛时 $h\equiv 0$ 的版本已证明，一般情形的 $h$ 解释见 Zagier 分析，待核对。

**对照。** M12；M02；M01（$\chi$ 加权）。

## Entry 24

**陈述。**

$$\frac{\pi e^{-2\pi z}}{2z\{\cosh(2\pi z)-\cos(2\pi z)\}} = \frac{1}{8\pi z^3}-\frac{1}{4z^2}+\frac{\pi}{4z}-\sum_{n=1}^{\infty}\frac{1}{z^2+(z+n)^2}+4z\sum_{n=1}^{\infty}\frac{n}{(e^{2\pi n}-1)(4z^4+n^4)}.$$

**出处。** Berndt Part II，Ch. 14，Entry 24（书页 291）。

**状态。** 已证明。

**对照。** M02（部分分式）；与 Entry 25 互补（见该条）。

**数值复核。** $z = 0.3$ 时 nsum 差 $5.9\times 10^{-31}$。

## Entry 24(i)

**陈述。**

$$\frac{1}{2z^2}+\sum_{n=1}^{\infty}\frac{1}{z^2+n^2} = \frac{\pi}{2z}+\frac{\pi}{z(e^{2\pi z}-1)}.$$

即 (1.9) 的改写。

**出处。** Berndt Part II，Ch. 14，Entry 24(i)（书页 292）。

**状态。** 已证明。

**对照。** M02；M09（Ch. 9 的 (1.9)）。

**数值复核。** $z = 0.5$ 时 nsum 差 $3.9\times 10^{-31}$。

## Entry 24(ii)

**陈述。**

$$\frac{1}{z(e^{\pi z}+1)} = \frac{1}{2z}-\frac{2}{\pi}\sum_{n=0}^{\infty}\frac{1}{z^2+(2n+1)^2}.$$

**出处。** Berndt Part II，Ch. 14，Entry 24(ii)（书页 292）。

**状态。** 已证明。

**对照。** M02。

**数值复核。** $z = 0.5$ 时 nsum 差 0。

## Entry 25

**陈述。**

$$\frac{\pi e^{-\pi z}}{4z\{\cosh(\pi z)+\cos(\pi z)\}} = \frac{\pi}{8z}-\sum_{n=0}^{\infty}\frac{1}{z^2+(z+2n+1)^2}-4z\sum_{n=0}^{\infty}\frac{2n+1}{(e^{(2n+1)\pi}+1)(4z^4+(2n+1)^4)}.$$

与 Entry 24 互补；Entry 25(xii) 是其推论（见该条）。

**出处。** Berndt Part II，Ch. 14，Entry 25（书页 292）。

**状态。** 已证明。

**对照。** M02。

**数值复核。** $z = 0.3$ 时 nsum 差 $4.9\times 10^{-32}$。

## Entry 25(i)

**陈述。**

$$\sum_{k=1}^{\infty}\frac{\coth(\pi k)}{k^3} = \frac{7\pi^3}{180}. \tag{25.1}$$

首证 Cauchy。

**出处。** Berndt Part II，Ch. 14，Entry 25(i)（书页 293）。

**状态。** 已证明。

**对照。** M02；M04（$\pi^3$ 求值）。

**数值复核。** nsum 差 $2.0\times 10^{-31}$。

## Entry 25(ii)

**陈述。**

$$\sum_{k=1}^{\infty}\frac{\coth(\pi k)}{k^7} = \frac{19\pi^7}{56700}. \tag{25.2}$$

见于致 Hardy 的信 [16, p. xxvi]。

**通式 (25.3)。** 对奇正整数 $n$，

$$\sum_{k=1}^{\infty}\frac{\coth(\pi k)}{k^{2n+1}} = 2^{2n}\pi^{2n+1}\sum_{k=0}^{n+1}(-1)^{k+1}\frac{B_{2k}}{(2k)!}\cdot\frac{B_{2n+2-2k}}{(2n+2-2k)!}.$$

首述 Lerch。

**出处。** Berndt Part II，Ch. 14，Entry 25(ii)（书页 293）。

**状态。** 已证明。

**对照。** M01（Bernoulli 数通式）；M02；M04。

**数值复核。** (25.2) nsum 差 $3.9\times 10^{-31}$；(25.3) 在 $n = 1$、$n = 3$ 时差均为 $3.9\times 10^{-31}$。

## Entry 25(iii)

**陈述。**

$$\sum_{k=0}^{\infty}\frac{\tanh\{(2k+1)\pi/2\}}{(2k+1)^3} = \frac{\pi^3}{32}.$$

**出处。** Berndt Part II，Ch. 14，Entry 25(iii)（书页 293）。

**状态。** 已证明。

**对照。** M02；M04。

**数值复核。** nsum 差 $9.9\times 10^{-32}$。

## Entry 25(iv)

**陈述。**

$$\sum_{k=0}^{\infty}\frac{\tanh\{(2k+1)\pi/2\}}{(2k+1)^7} = \frac{7\pi^7}{23040}.$$

**通式 (25.4)。**

$$\sum_{k=0}^{\infty}\frac{\tanh\{(2k+1)\pi/2\}}{(2k+1)^{4n+3}} = \frac{\pi^{4n+3}}{8}\sum_{k=0}^{2n}(-1)^k\frac{E_{2k+1}(0)}{(2k+1)!}\cdot\frac{E_{4n+1-2k}(0)}{(4n+1-2k)!},$$

其中 $E_j(x)$ 为 Euler 多项式。(25.4) 不在笔记中，首证 Phillips；更一般的 $\alpha\beta = \pi^2$ 公式见书中；$n = 1$ 情形属 Grosjean，$n = 2$ 情形属 de Saint-Venant 1856（矩形截面梁的扭转刚度）。

**出处。** Berndt Part II，Ch. 14，Entry 25(iv)（书页 293）。

**状态。** 已证明（(25.4) 为后人补证）。

**对照。** M01（Euler 多项式在 0 处的值）；M02。

**数值复核。** (25.4) 在 $n = 0$、$n = 1$ 时差均为 $9.9\times 10^{-32}$；(25.4) 的求和实为有限和（$k = 0,\dots,2n$，超出后 Euler 多项式下标为负）。

## Entry 25(v)

**陈述。**

$$\sum_{k=1}^{\infty}\frac{(-1)^{k+1}\mathrm{csch}(\pi k)}{k^3} = \frac{\pi^3}{360}.$$

**出处。** Berndt Part II，Ch. 14，Entry 25(v)（书页 294）。

**状态。** 已证明。

**对照。** M02；M04。

**数值复核。** nsum 差 $1.2\times 10^{-32}$。

## Entry 25(vi)

**陈述。**

$$\sum_{k=1}^{\infty}\frac{(-1)^{k+1}\mathrm{csch}(\pi k)}{k^7} = \frac{13\pi^7}{453600}.$$

**通式 (25.5)。**

$$\sum_{k=1}^{\infty}\frac{(-1)^{k+1}\mathrm{csch}(\pi k)}{k^{4n+3}} = \frac{1}{2}(2\pi)^{4n+3}\sum_{k=0}^{2n+2}(-1)^k\frac{B_{2k}(\frac12)}{(2k)!}\cdot\frac{B_{4n+4-2k}(\frac12)}{(4n+4-2k)!},$$

其中 $B_j(x)$ 为 Bernoulli 多项式。实质源于 Cauchy；首证 Mellin；另有一般 $\alpha\beta = \pi^2$ 公式。

**出处。** Berndt Part II，Ch. 14，Entry 25(vi)（书页 294）。

**状态。** 已证明。

**对照。** M01（Bernoulli 多项式在 $1/2$ 处的值）；M02。

**数值复核。** (25.5) 在 $n = 0$、$n = 1$ 时差分别为 $2.5\times 10^{-32}$、$3.7\times 10^{-32}$。

## Entry 25(vii)

**陈述。**

$$\sum_{k=1}^{\infty}\chi(k)\frac{\mathrm{sech}(\pi k/2)}{k} = \frac{\pi}{8}.$$

为 Entry 15 的简单推论；Preece 证、Zucker 亦证；曾投《Mathematical Gazette》为问题。

**出处。** Berndt Part II，Ch. 14，Entry 25(vii)（书页 295）。

**状态。** 已证明。

**对照。** M02；M01；M04（$\pi/8$）。

**数值复核。** 直接求和差 $4.9\times 10^{-32}$（nsum 对 $\chi$ 分块交错级数误外推得差 $5.5\times 10^{-9}$，不可信，见小结）。

## Entry 25(viii)

**陈述。**

$$\sum_{k=1}^{\infty}\chi(k)\frac{\mathrm{sech}(\pi k/2)}{k^5} = \frac{\pi^5}{768}.$$

见于致 Hardy 的信。

**出处。** Berndt Part II，Ch. 14，Entry 25(viii)（书页 295）。

**状态。** 已证明。

**对照。** M02；M01。

**数值复核。** nsum 差 $3.8\times 10^{-13}$。

## Entry 25(ix)

**陈述。**

$$\sum_{k=1}^{\infty}\chi(k)\frac{\mathrm{sech}(\pi k/2)}{k^9} = \frac{23\pi^9}{1720320}.$$

**通式 (25.6)。**

$$\sum_{k=1}^{\infty}\chi(k)\frac{\mathrm{sech}(\pi k/2)}{k^{4n+1}} = \frac{1}{4}\left(\frac{\pi}{2}\right)^{4n+1}\sum_{k=0}^{2n}(-1)^k\frac{E_{2k}}{(2k)!}\cdot\frac{E_{4n-2k}}{(4n-2k)!},$$

可由 Entry 21(ii) 推出。

**出处。** Berndt Part II，Ch. 14，Entry 25(ix)（书页 295）。

**状态。** 已证明。

**对照。** M01（Euler 数通式）；M02。

**数值复核。** (25.6) 在 $n = 0$、$1$、$2$ 时差分别为 $5.5\times 10^{-9}$（nsum 误外推，见 25(vii) 注）、$3.8\times 10^{-13}$、$2.6\times 10^{-17}$；(25.6) $n = 0$ 的情形直接求和差 $4.9\times 10^{-32}$。

## Entry 25(x)

**陈述。**

$$\sum_{k=1}^{\infty}\frac{\chi(k)}{k^2(e^{\pi k}-1)} + \frac{1}{8}\sum_{k=1}^{\infty}\frac{1}{k^2\cosh(\pi k)} = \frac{5\pi^2}{96}-\frac{1}{2}\int_0^1\frac{\tan^{-1}x}{x}\,dx. \tag{25.7}$$

书页底有手写旁注（300 DPI 确认）：$= 5\pi^2/96-\frac12G$，其中 $G$ 为 Catalan 常数；(25.9) $\int_0^1(\tan^{-1}x)/x\,dx = L(2)$，而 $L(2) = G$。

**出处。** Berndt Part II，Ch. 14，Entry 25(x)（书页 295）。证明用 $f(z) = 1/[z^2(e^{2\pi z}-1)\cos(\pi z)]$，$R(0) = 5\pi/12$，得 (25.8)：$0 = -(8/\pi)\sum\chi(k)/[k^2(e^{\pi k}-1)]-(4/\pi)L(2)-(1/\pi)\sum 1/[k^2\cosh(\pi k)]+5\pi/12$，结合 (25.9) 即得 (25.7)。

**状态。** 已证明。

**对照。** M02；M01（$L(2) = G$）；M04（Catalan 常数 $G$，见 Ch. 9 Entry 16、32）。

**数值复核。** (25.7) 两端 $= 0.0560590988015$，差 $4.9\times 10^{-32}$；(25.9) 的积分求积得 $0.915965594177$，与 $G$ 差 0。

## Entry 25(xi)

**陈述。**

$$\sum_{k=1}^{\infty}\frac{1}{\{k^2+(k+1)^2\}(\cosh\{(2k+1)\pi\}-\cosh\pi)} = \frac{1}{2\sinh\pi}\left\{\frac{1}{\pi}+\coth\pi-\frac{\pi}{2}\tanh^2\left(\frac{\pi}{2}\right)\right\}. \tag{25.10}$$

**拉马努金原文错误（Berndt 注明）。** 笔记版有误：拉马努金写的是 $\sinh\{(2k+1)\pi\}-\sinh\pi$（书页 297 明言）；他致 Hardy 的信 [16, p. 349] 中亦带同一错误传出。Watson [1] 用围道积分证明 (25.10)（其证明有几处错误）；Sitaramachandrarao [1] 另有基于 Entry 20(i) 的优雅证明（可能即拉马努金原证）；书中给出两证。

**出处。** Berndt Part II，Ch. 14，Entry 25(xi)（书页 296）。

**状态。** 已证明（笔记版已订正）。

**对照。** M02。

**数值复核。** nsum 差 $1.0\times 10^{-32}$。

## Entry 25(xii)

**陈述。**

$$\sum_{k=0}^{\infty}\frac{2k+1}{\{25+(2k+1)^4/100\}(e^{(2k+1)\pi}+1)} = \frac{4689}{11890}-\frac{\pi}{8}\coth^2\left(\frac{5\pi}{2}\right). \tag{25.11}$$

**拉马努金原文错误（Berndt 注明）。** 本条亦见于拉马努金致 Hardy 的信 [16, p. 349]；(25.11) 右端两项的符号均错（笔记版亦然）；左端在笔记中只写了级数的前三项，且第二项另有一处误印。Berndt 注：前三项之和 $1/[25.01(e^{\pi}+1)]+3/[25.81(e^{3\pi}+1)]+5/[31.25(e^{5\pi}+1)] = 0.001665694154\ldots$，右端 $= 0.001665694195\ldots$，颇堪玩味。

**出处。** Berndt Part II，Ch. 14，Entry 25(xii)（书页 298）。Watson [1] 用围道积分证明 (25.11)；Berndt 证明其为 Entry 25（取 $z = 5i$）的推论，得 (25.12)、(25.13)，归结为 (25.14)：$50\sum_{k=0}^{\infty}(2k+1)/[(2k+1)^4+2500] = 4689/11890$，由部分分式裂项得证。

**状态。** 已证明（笔记版已订正）。

**对照。** M02；与 Entry 25 主式互见。

**数值复核。** (25.11) nsum 差 $1.2\times 10^{-31}$；前三项和 $= 0.00166569415488$、右端 $= 0.00166569419513$，与书中 $0.001665694154$、$0.001665694195$ 逐位一致。

## 小结

- 本章 25 条 Entry（Entry 1–25，无缺号）、57 个 Entry 标题全部收录；书页 240–299（PDF 页 252–311）逐页读完并转录。
- 主线有三：**变换公式线**（Entry 6、7、8、10、11、12、17 的 Poisson 求和与 theta/eta 变换；Entry 13、14、21 的 $\alpha$–$\beta$ 对偶恒等式）；**部分分式线**（Entry 18 的主恒等式 (18.1)，Entry 19、20、22、24、25 由其导出或与之互补）；**求值线**（Entry 15、25 的 $\pi$ 幂与 Catalan 常数求值，Entry 21(i) 的 $\zeta(2n+1)$ 公式为本章顶峰）。
- 数值复核约 91 项（mpmath 30 位，直接求和为主，nsum 只用于收敛行为良好的级数），全部通过。本轮复核的方法教训有三：(1) nsum 对慢收敛级数与 $\chi$ 分块交错级数会系统性误外推（Entry 2、19(v)、25(vii) 均初报不符，改直接求和加解析尾项后通过；Entry 25(vii) nsum 误报 $5.5\times 10^{-9}$，直接求和差 $4.9\times 10^{-32}$）；(2) mpmath 的 `euler(n)` 并非 Bernoulli–Euler 意义下的 Euler 数（其 `euler(0)` 得 Euler–Mascheroni 常数 $\gamma$），复核用 $E_{2k} = 2^{2k}E_{2k}(1/2)$ 计算；(3) 振荡积分须先换元或三角展开再求积（Entry 16 的 $\sin^{2n+1}x/x$ 积分、Entry 22(ii) 的 $\sqrt{x}$ 积分直接求积均失真）。
- **本轮发现的原书印文问题两处（均已标待核对）**：(1) Entry 17(ii) (17.4) 的系数 $\pi n!/2^{2n+2}$ 应为 $\pi n!/2^{n+2}$（七组参数下左端/印文右端之比恰为 $2^n$；300 DPI 确认印文）；(2) Entry 22 推论 (22.8) 第二求和的 $\cosh^2(\beta n^2)$ 应为 $\cosh(\beta n^2)$（印文版差 $0.043$，订正版差 $5.9\times 10^{-31}$；书中本条证明的留数公式亦为单 $\cosh$）。
- 拉马努金原文错误（Berndt 已注明，本文件如实记录）：Entry 1 的 $C'$ 值、Entry 17 推论 1、2 的适用范围、Entry 19(i) (19.1) 的发散级数、Entry 22(i) 分子的乘积写法、Entry 22(iii) (22.11) 的 $\frac14\mathrm{Log}\,\Gamma(3/4)$、Entry 25(xi) 的 $\sinh$ 写法、Entry 25(xii) 右端两项的符号与左端只写前三项。
- 章末收束（书页 299）：涉及双曲函数的无穷级数吸引了众多作者的注意；Berndt [6]、[7] 含有许多此类结果与大量参考文献；读者还可参阅 Cauchy [1]、Zucker [1]、[2]、Ling [1]、[2]、[3]、Forrester [1]、Bruckman [1] 的论文；Berndt [8] 与 Klusch [1] 给出其他类型的双曲级数。

## 待核对清单

1. IMSC 本章结果数（当日不可达，https://imsc.res.in/~rao/ramanujan/newnow/Bpart2.htm 连接失败）。
2. Berndt 章首计数：章首导言未给出本章公式或定理陈述的总数，待核对原书目录。
3. TIFR 影印版页码：本章各条在 TIFR 1957 年版第二本笔记中的位置未核对。
4. Entry 17(ii) (17.4) 的本轮发现：系数 $\pi n!/2^{2n+2}$ 与 $\pi n!/2^{n+2}$ 之辨（七组参数数值复核 + 300 DPI 确认印文），待独立核对、待查其他印次或勘误表。
5. Entry 22 推论 (22.8) 的本轮发现：$\cosh^2(\beta n^2)$ 与 $\cosh(\beta n^2)$ 之辨（数值复核 + 书中证明的留数公式交叉确认 + 300 DPI 确认印文），待独立核对、待查其他印次或勘误表。
6. Entry 23(i) (23.1) 右端读作 $\varphi(2)$ 还是 $\varphi(-2)$，Berndt 明言不清楚；(23.1) 的严格解释与 $h$ 的确切含义（Zagier 分析），待核对。
7. Entry 23(ii) (23.8)–(23.12) 与例子的确切形式（Zagier 的 $G$ 函数分析），待逐字核对原书 pp. 285–290。
8. Entry 1 推论 (1.3) 的 (1.5) 与 (1.16) 的确切形式、Entry 2 的证明细节（留数计算），待逐字核对。
9. Entry 8(iii) (8.1) 的第二、第四求和（$\sum\varphi(\alpha nk)/k$、$\sum\varphi(\beta nki)/k$）的确切形式，待逐字核对原书 p. 254。
10. Entry 9(i)(ii) 的 $\psi$ 定义与 (9.2)(9.3) 的细节，待逐字核对。
11. Entry 12 推论 (12.3) 的 $f_N(z)$ 假设细节，待逐字核对。
12. Entry 18 推论 1、2、3 的确切形式（(18.2)(18.3) 的分母与 $\chi$ 因子），待逐字核对。
13. Entry 21(iii) 的 $L(s)$ 定义域与 Chowla 证明的引文细节，待核对。
14. Entry 22(ii) 推论 (22.8) 的证明中 $N$ 的限制条件（$N$ 为偶数、$N^2$ 与某值保持有界距离），待逐字核对原书 pp. 279–280。
15. Entry 25(x) 的 (25.8) 与手写旁注的含义（$= 5\pi^2/96-\frac12G$），待核对旁注是否为 Berndt 本人所加。
16. Entry 25(xii) 的 (25.12)–(25.14) 推导细节，待逐字核对。

## 来源说明

- 整理本：Bruce C. Berndt，《Ramanujan's Notebooks》，Part II，Springer，1989，Ch. 14，书页 240–299。
- 电子版：archive.org 标识符 `ramanujan_notebooks_ii`（《Ramanujan's Notebooks, Part 2》，Springer 1989，XII + 360 页，DOI 10.1007/978-1-4612-4530-8）；PDF 14,538,056 字节、371 叶；**PDF 页 = 书页 + 12**（与 Part I 的 +10 不同）。本章书页 240–299 对应 PDF 页 252–311，全部 60 页均渲染 150 DPI 图片逐字读完并转录；关键公式另用 300 DPI 放大图确认（Entry 17(ii) (17.4) 的系数、Entry 22 推论 (22.8) 的 $\cosh^2$、Entry 25(x) 页底手写旁注、Entry 25(xi) 的 $\cosh$ 写法）；OCR 公式凡与原图或数值不符者一律纠正并注明。
- 数值复核：mpmath 30 位，直接求和为主；nsum 只用于收敛行为良好的级数（慢收敛与 $\chi$ 分块交错级数改用直接求和加解析尾项，见小结）；振荡积分先换元或三角展开再求积；Euler 数用 $E_{2k} = 2^{2k}E_{2k}(1/2)$ 计算。复核脚本见工作底稿（未收入本仓库）。
- 引用文献（Berndt 书中编号）：[1] Cauchy；[2]（多篇，见各条）；[6]、[7] Berndt 的 Eisenstein 级数论文；[13] 拉马努金论文；[16] 拉马努金《Collected Papers》；另见各条所引 Schlömilch、Rao–Ayyar、Malurkar、Nanjundiah、Lerch、Chowla、Watson、Sitaramachandrarao、Zagier 等。文献全称与卷期以原书参考文献表为准，本文件不另编。
- 下一章：Part II Ch. 15 Asymptotic Expansions and Modular Forms（书页 300 起）。
