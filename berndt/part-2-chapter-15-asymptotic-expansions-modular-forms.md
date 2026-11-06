# Part II，Chapter 15——Asymptotic Expansions and Modular Forms（渐近展开与模形式）

出处：Bruce C. Berndt，《Ramanujan's Notebooks》，Part II，Springer，1989，Ch. 15，书页 300–338。

本章是 Berndt 五卷中话题最杂的一章，也是 Part II 的最后一章：前七节是级数渐近展开（Euler–Maclaurin 与 Mellin 变换的系统应用），后半是模形式（以 Eisenstein 级数 $L$、$M$、$N$ 为主线），末两节是 Ch. 19–21 模方程工作的先声。本章共 **15 条编号 Entry（Entry 1–8、10–16，无 Entry 9）**，另含分体 Entry 10(i) 两部分、Entry 10(ii)、Entry 12(i)–(x)、Entry 13(i)–(x)、Entry 15(ii)、Entry 15(iii)，共 **36 个 Entry 标题**；此外还有 Berndt 的六条推广定理（Theorem 3.1、3.2、6.1、6.2、6.3、7.1），书中明确标为 Theorem 而非 Entry。

## 背景与记号

- 章首导言（pp. 300–301）：章名并不完全反映内容；第二本笔记 21 章之中，本章话题比其余各章都更零散，拉马努金似乎在此收集了若干“零碎”（odds and ends）；大部分材料引人入胜，少数部分没什么实质。前七节主要讲级数的渐近展开，例如当 $x \to 0+$ 时 $\sum_{k=1}^{\infty} e^{-xk^p}k^{m-1}$、$\sum_{k=1}^{\infty} e^{-kx}\mathrm{Log}\,k$ 与 $\sum_{k=1}^{\infty} k^{m-1}/(1+xk^p)^d$。Berndt 对这类级数的定理常比拉马努金所指的更一般，未由拉马努金明确陈述的推广在书中标为 Theorem，以别于拉马努金的 Entry；这使得第 2–7 节的叙述对拉马努金的材料作了若干重排。第 1 节中拉马努金的论述似乎表明他用 Euler–Maclaurin 求和公式建立渐近展开，但他的评语过于隐晦含糊，无法找到恰当解释；无论如何，他对 Euler–Maclaurin 公式的运用是形式的、非严格的；尽管方法如此，他的结论除少数小错外都是正确的。Berndt 原先的证明同样基于 Euler–Maclaurin，相当冗长；P. Flajolet 建议改用 Mellin 变换可得短得多的证明。
- 后半（p. 301）：模形式、特别是 Eisenstein 级数居于中心舞台。本章最有趣的定理之一在 (8.3)：一个修正 theta 函数的反演公式，一个全新的结果；如此精确的公式存在，令人惊讶。Entry 11 是一条优美而新的互反公式，令人想起第 14 章的若干公式。第 12 节的若干结果见于拉马努金名篇 [11]（[16], pp. 136–162），特别提到 Entry 12(x) 等价于一条非常有趣的恒等式（见该条）。第 13 节的全部结果亦见 [11]。Entry 14 给出 Eisenstein 级数的一条新递推公式，与拉马努金在 [11]（[16], p. 140）中发现的最著名的 Eisenstein 级数递推公式截然不同。第 10 节中拉马努金定义了无穷级数理论中的若干术语，定义相当含糊，似乎不重要。末两节材料的动机不明；但一旦意识到它是 Ch. 19–21 模方程深刻工作的先声，其中部分工作就有了意义（见 Part III）。
- 第 2–7 节的大部分结果用 Bernoulli 数 $B_n$ 表述。记（Titchmarsh [3, p. 19]）：对每个正整数 $n$，

$$\zeta(1-n) = (-1)^{n+1}B_n/n. \tag{0.1}$$

由于 $\zeta(1-n)$ 的值而非 Bernoulli 数本身自然出现在证明中，且前一记号更经济，书中一般用 $\zeta(s)$ 表述拉马努金的结果。
- 记号（p. 306）：$\mathbf{Z}^{-}$ 表示非正整数集，$\sigma = \mathrm{Re}\,s$；$\sum_k^*$ 表示略去使被加项无定义的 $k$ 值；亚纯函数 $f$ 在极点 $z_0$ 处的留数记为 $R(z_0)$。
- 本章与已填章节的互见：Part I Ch. 4 的拉马努金主定理（Entry 11）与本章 Entry 1 的 Euler–Maclaurin 形式同源；Part I Ch. 6 的发散级数理论（Entry 1 的 (1.1) 与常数 $c$）与本章第 1 节的 $F(h)$ 是同一主题的两面；Part I Ch. 7 的幂和与 $\zeta$ 函数方程（Entry 4）与本章 (0.1)、Theorem 3.1 的 $\zeta$ 值呼应；Part II Ch. 13 的渐近展开（Entry 3、6–11、36 与 Abel–Plana 公式 Entry 17）与本章前七节同属 Mellin/Euler–Maclaurin 一路，本章 (1.1) 所引的 Euler–Maclaurin 公式即 Ch. 13 (10.5)；Part II Ch. 14 的 theta 函数与 Eisenstein 级数（Entry 7 的 theta 变换、Entry 13 的 Bernoulli 数级数、Entry 21 的 $\zeta(2n+1)$ 公式）与本章 Entry 8 的 theta 反演、Entry 11 的互反公式、Entry 14 的 Eisenstein 递推直接衔接，Entry 8 的证明更直接引用 Ch. 14 Entry 7 的推论与 (6.1) Poisson 求和、(5.2)。
- 与主题模块的对照总览：渐近展开主线见 **M12**（全章前半 §§1–8：Entry 1–8 与 Theorem 3.1–7.1，Euler–Maclaurin、Mellin 变换、除数问题、素数加权级数）；模形式主线见 **M06**（后半 §§9–14：$L$、$M$、$N$ 与 Eisenstein 级数、Entry 10–14、模方程 §§15–16）；无穷级数见 **M02**（Entry 1–8 的级数渐近、Entry 11 的互反级数、Entry 12–13 的 Lambert 级数 $\Phi_v(q)$）；数论见 **M01**（Bernoulli 数 (0.1)、除数函数 $\sigma_v$、Entry 12(x) 的 $\sigma$ 恒等式、Entry 13 的 $\Phi_v$、§2 例 (ii) 的除数问题与例 (iii) 的素数级数）；Gamma 函数见 **M10**（Theorem 3.1 等处处出现的 $\Gamma$、Entry 14 的 $\wp$ 函数与 $b(n)$）；椭圆函数见 **M11**（§14 的 Weierstrass $\wp$ 函数、Entry 12(x) 的椭圆函数证明、§§15–16 的模方程）；$q$ 级数见 **M07**（$\Phi_v(q)$、$L$、$M$、$N$ 的 $q$ 展开、Entry 12–13）；分拆见 **M05**（§2 例 (iv) 的 $p(n)$ 渐近与 Rademacher 精确公式、$I(n)$ 的 Zuckerman 精确公式）；积分见 **M09**（Mellin 变换证明方法、(8.2) 的积分求值、Entry 11 的留数积分）；$\pi$ 与特殊常数见 **M04**（Entry 8 的 theta 反演、Entry 11 的 $\pi^2$ 互反、§§15–16 的模方程与 $F(x) = (1-x)^{-1/2}$）。

## 本章结构

| Entry | 主题 | 书页 |
|---|---|---|
| Entry 1 | Euler–Maclaurin 形式的 $F(h)$ 与推论（$h\varphi(h)$ 展开） | 301–302 |
| 第 1 节例 1、例 2 | $\varphi = 1/(1+h^2)$ 与 $\varphi = e^{-h^2}$ 的 $F(h)$（拉马努金两处有误） | 303 |
| 第 2 节例 (i)–(iv) | $\sum e^{-kx}\mathrm{Log}\,k$、除数问题、素数级数、$I(n)$ 量级 | 303–305 |
| Entry 2 | Entry 3 的 $p = 1$ 特例（书中未单独印出公式） | 303 |
| Entry 3 | $\sum e^{-k^px}k^{m-1}$ 渐近展开与推论 $\sum e^{-k^px}/k$ | 305–306 |
| Theorem 3.1 | Entry 3 的 Mellin 推广（$m/p \notin \mathbf{Z}^{-}$ 与 $m/p = -r$ 双重极点情形） | 306–308 |
| Theorem 3.2 | $\sum e^{-xk^p}k^{m-1}\mathrm{Log}\,k$ 的 $\zeta'$ 版 | 308–309 |
| 第 3 节例 (i)–(v) | Entry 3/推论的特例（$p = 2$、$p = 4$、$m = 2$、$p = 3$、$m = 2$；$\sum e^{-k^2x}/k^2$；$m = 3$、$p = 6$） | 309 |
| Entry 4 | $\sum k^{m-1}/(1+xk^p)^d$ 渐近展开（$(d)_k$ 版） | 309–310 |
| Entry 5 | Theorem 6.1 的 $n = q = 1$、$m \ne p$ 情形（书中未单独印出公式） | 310 |
| Entry 6 | Theorem 6.1 的 $m/p \ne n/q$ 情形；“N.B.”结果为 $m/p = n/q$ 情形 | 310 |
| Theorem 6.1 | 双重和 $f_{m,n}(x)$ 的双 $\Gamma$ 项 + 双 $\zeta$ 级数（$pn \ne qm$ 与 $pn = qm$ 双重极点情形） | 310–311 |
| Theorem 6.2 | $m = 0$ 情形（含常数 $A_n$） | 311–312 |
| Theorem 6.3 | $m = n = 0$ 情形（含常数 $A_0$、$c_1$） | 312 |
| Entry 7 | $\sum s^{m-1}\sigma_{n-m}(s)/(e^{sx}-1)$ 渐近展开（订正版；拉马努金误写 $\sigma_{n-1}$） | 313 |
| Theorem 7.1 | 三重和 $f_{m,n,l}$ 的推广 | 313–314 |
| 第 7 节例 | (7.1) 的 $m = 3$、$n = 5$ 情形（拉马努金又误写 $\sigma_{n-1}$ 且漏项 $-1/(1440x)$） | 314 |
| 第 8 节 (8.1)(8.2) | $\sum 1/(e^{k^2x}-1)$ 的渐近与 $\int_0^{\infty}\sum e^{-k^2x}\cos(ax)\,dx$ 的闭式 | 314 |
| Entry 8 | $\sum 1/(e^{k^2x}-1)$ 的精确反演公式 (8.3)（章首点名最有趣的定理之一） | 314–317 |
| 第 9 节 | $F_{m,n}(x)$、$L$、$M$、$N$、$\Phi_v(q)$、Eisenstein 级数 $E_n(\tau)$ 的 Fourier 展开 (9.3)(9.4) | 318–319 |
| Entry 10(i) 第一部分 | $n \ge 2$ 时 $-(B_{2n}/4n)E_{2n}(\tau)$ 可表为 $M$、$N$ 的多项式 | 319 |
| Entry 10(i) 第二部分 | $f_n(x)$ 可表为 $M$、$N$ 的多项式（$\delta_1 = 1/2$，$n \ge 2$ 时 $\delta_n = 1$） | 319–320 |
| Entry 10(ii) | 级数的“度”、纯/混合、完全/不完全、完备/不完备、绝对完备等定义（引自笔记 pp. 186–187） | 320–321 |
| 第 10 节例 1–7 | 上述术语的七个例子（$f_1$、$f_2$、$F_{m,n}$、$g_{m,n}$、$h_{m,n}$、theta 函数、$L$、$M$、$N$） | 321–323 |
| Entry 11 | $\alpha\beta = \pi^2$ 时的互反公式（章首点名的优美新互反公式） | 323–326 |
| Entry 12(i)–(x) | 判别式 $\Delta(\tau)$、$E_8$、$E_{10}$、$E_{14}$ 与 $\sum k^{2j}q^k/(1-q^k)^2$ 四式、(ix)(x) | 326–329 |
| Entry 13(i)–(x) | $\Phi_{11}$–$\Phi_{31}$ 的十条 $M$、$N$ 多项式恒等式；注记（$q\,dL/dq$ 等）与 $\Phi_{r,s}$ 三例 | 330 |
| Entry 14 | Eisenstein 级数的新递推公式（$S_{n+2}$ 的递推） | 331–333 |
| 第 15 节 (i) | 2 次模方程与乘子 $M_2(\alpha)$、一般 $n$ 次模方程 (15.4) 与乘子 $M_n(\alpha)$、推论 | 333–335 |
| Entry 15(ii) | 函数复合的“$p$ 次、$q$ 次、$r$ 次”陈述与推论 | 335 |
| 第 15 节 (ii) 推论 (i)(ii) | 函数迭代的两个闭式（$x^2+4x$ 型与 $x^2-2$ 型） | 335–336 |
| Entry 15(iii) | $\varphi$、$\chi$ 与“自重复级数”的谜样陈述 (15.6)(15.7) | 336–337 |
| 第 15 节例 | $I = x$、$II = x^2+2nx$ 时的 $III$ 近似 (15.10) 与 $P_r(x)$ 展开 (15.11)(15.12) | 337–338 |
| Entry 16 | $n-1$ 次模方程推出 $(n-1)^2$ 次模方程 | 338 |

## Entry 1

**陈述。**（逐字引自拉马努金，书 p. 301）

$$``h\sum_{k=1}^{\infty}\varphi(kh) = \int_{0}^{\infty}\varphi(x)\,dx + F(h),$$

其中 $F(h)$ 可由展开左边并以常数代替级数求得，且 $F(0) = 0$。”

**说明。** 若对 $f(x) = \varphi(hx)$ 在 $[0, \infty)$ 上形式地应用 Euler–Maclaurin 公式（Ch. 13 (10.5)），则

$$F(h) = h\sum_{k=1}^{\infty}\varphi(kh) - \int_{0}^{\infty}\varphi(x)\,dx = \sum_{k=1}^{m}\frac{(-1)^{k+1}B_k}{k!}\varphi^{(k-1)}(0)h^k + hR_m, \tag{1.1}$$

其中

$$R_m = \frac{(-1)^{m-1}}{m!}\int_{0}^{\infty}B_m(t-[t])f^{(m)}(t)\,dt,$$

并假定 $\varphi^{(k-1)}(\infty) = 0$（$1 \le k \le m$）。若 (1.1) 对 $\varphi$ 成立且 $hR_m \to 0$（$h \to 0$），则如 Entry 1 所言 $F(0) = 0$。

**推论。**（逐字引自拉马努金）“若

$$h\varphi(h) = ah^p + bh^q + ch^r + dh^s + \cdots,$$

则

$$h\sum_{k=1}^{\infty}\varphi(kh) = \int_{0}^{\infty}\varphi(x)\,dx - \frac{aB_p h^p}{p} - \frac{bB_q h^q}{q} - \cdots.''$$

Berndt 注：拉马努金显然假定 $p, q, \dots$ 为整数且 $2 \le p < q < \cdots$。若 (1.1) 对 $\varphi$ 成立且 $R_m = O(h^m)$（每个 $m \ge 1$），则此推论在 $h \to 0$ 时给出有效的渐近公式。拉马努金接着指出：“若 $\varphi(h)$ 的展开是无穷级数，则 $F(h)$ 的展开也是无穷级数；但若数 $p, q, r, s$ 等多为奇整数，则 $F(h)$ 似乎终止。此时 $F(h)$ 的隐藏部分不能按 $h$ 的升幂展开，且当 $h$ 缓慢减小时它衰减得非常快，因而 $h$ 很小时在实用上可以忽略。”前半句指系数 $B_p, B_q, \dots$ 在 $p, q, \dots$ 为大于 1 的奇整数时为零；后半句的“隐藏部分”指下述例 1（$\varphi(h) = (1+h^2)^{-1}$）与例 2（$\varphi(h) = \exp(-h^2)$）的情形，其中 (1.1) 取 $F(h) = -h/2 + hR_m$ 的形式。拉马努金断言 $F(h) + h/2 = hR_m$ 在 $h \to 0$ 时迅速趋于 0；订正后的例 1、例 2 中可见 $F(h) + h/2 \sim \exp(-2\pi/h)$ 与 $F(h) + h/2 \sim \exp(-\pi^2/h^2)$。对其他偶亚纯函数类求 $F(h)$ 在 $h \to 0$ 时的渐近估计是有趣的（见第 3 节例 (iv) 与 (8.3)）。

**状态：** 已证明（Berndt 的形式 Euler–Maclaurin 论证 + Mellin 变换严格化，见 Theorem 3.1 等）。**对照：** M12（本章渐近主线的起点）、M02、M01（Bernoulli 数）。

**第 1 节例 1。** 若 $\varphi(h) = 1/(1+h^2)$，则

$$F(h) = \frac{\pi}{e^{2\pi/h}-1} - \frac{h}{2}, \qquad F\left(\frac{1}{10}\right) = \pi/(e^{20\pi}-1) - \frac{1}{20}.$$

证明：由 Entry 1，$F(h) = h\sum_{k=1}^{\infty} 1/(1+h^2k^2) - \int_0^{\infty} dx/(1+x^2) = (\pi/2)\coth(\pi/h) - h/2 - \pi/2$。拉马努金（笔记 p. 181）断言 $F(h) = 2\pi/(e^{2\pi/h}-1)$，故他的 $F(1/10)$ 也有误。**我自验：** 直接求和 $F(1/10) = -0.0505000124585$，与 $-1/20$ 之差 $5.0\times 10^{-4}$ 恰为截断尾项（$k > 20000$ 的尾和约 $0.1\cdot 100/20000 = 5\times 10^{-4}$），补尾项后与公式一致。

**第 1 节例 2。** 若 $\varphi(h) = \exp(-h^2)$，则

$$F\left(\frac{1}{10}\right) \approx -\frac{1}{20} + \sqrt{\pi}e^{-100\pi^2}.$$

证明：由 Entry 1 与经典 theta 函数 $\theta(z)$ 的变换公式（Ch. 14 Entry 7 的推论），$F(h) = h\sum_{k=1}^{\infty} e^{-h^2k^2} - \int_0^{\infty} e^{-x^2}\,dx = -h/2 + \sqrt{\pi}\sum_{k=1}^{\infty} e^{-\pi^2k^2/h^2}$（(1.2)）。拉马努金断言“$F(1/10)$ 非常接近 $10\sqrt{\pi}e^{-100\pi^2}$”，系数 10 有误。

## 第 2 节例 (i)–(iv)

本节无编号 Entry，只有四个例子；Entry 2 亦在本节末以一句话交代（见下）。

**例 (i)。** 当 $x \to 0+$ 时，

$$\sum_{k=1}^{\infty} e^{-kx}\mathrm{Log}\,k \sim \frac{-\gamma-\mathrm{Log}\,x}{x} + \frac{1}{2}\mathrm{Log}(2\pi),$$

其中 $\gamma$ 为 Euler 常数。证明：由 Theorem 3.2 的 $p = m = 1$ 情形，因 $\zeta'(0) = -\frac{1}{2}\mathrm{Log}(2\pi)$（Titchmarsh [3, p. 20]）。

**例 (ii)。** 设 $d(n)$ 为正整数 $n$ 的正因数个数，则当 $x \to \infty$ 时，

$$\sum_{n \le x} d(n) \sim x\,\mathrm{Log}\,x + (2\gamma-1)x. \tag{2.1}$$

这是初等数论中著名的结果。记 $\Delta(x)$ 为 (2.1) 两端之差；初等方法得 $\Delta(x) = O(\sqrt{x})$（Hardy–Wright [1, p. 264]）；当时最好的 $O$ 估计为 $\Delta(x) = O(x^{7/22+\varepsilon})$（每个 $\varepsilon > 0$，Iwaniec–Mozzochi [1]）；Hafner [1] 证明对某个常数 $c > 0$，$\Delta(x) = \Omega_{+}((x\,\mathrm{Log}\,x)^{1/4}(\mathrm{Log}\,\mathrm{Log}\,x)^{(3+2\,\mathrm{Log}\,2)/4}\exp(-c(\mathrm{Log}\,\mathrm{Log}\,\mathrm{Log}\,x)^{1/2}))$，为当时最好的 $\Omega$ 定理。确定 $\Delta(x)$ 的量级的问题称为“除数问题”，是解析数论中最困难、最著名的难题之一；猜想为每个 $\varepsilon > 0$ 都有 $\Delta(x) = O(x^{1/4+\varepsilon})$。 fuller 讨论见 Ivić [1, Chapter 10] 与 Graham–Kolesnik [1]。**对照：** M01（除数函数与除数问题）、M12。

**例 (iii)。** 若 $p_k$ 为第 $k$ 个素数，则当 $x \to 0+$ 时，

$$\sum_{k=1}^{\infty} e^{-kx}p_k \sim -\frac{\mathrm{Log}\,x}{x^2}.$$

证明：由 Landau [1, p. 215]，$p_k = k\,\mathrm{Log}\,k + O(k\,\mathrm{Log}\,\mathrm{Log}\,k)$（$k \to \infty$）；故 $F(t) := \sum_{k \le t} p_k = \frac{1}{2}t^2\,\mathrm{Log}\,t + O(t^2\,\mathrm{Log}\,\mathrm{Log}\,t)$；分部求和即得。**对照：** M01（素数）。

**例 (iv)。** 记

$$\left(\sum_{k=-\infty}^{\infty}(-x)^{k^2}\right)^{-1} = \sum_{n=0}^{\infty} I(n)x^n, \qquad |x| < 1.$$

则“$I(n)$ 的量级为

$$\frac{1}{4n}\left\{\cosh\pi\sqrt{n} - \frac{\sinh\pi\sqrt{n}}{\pi\sqrt{n}}\right\}.”$$

此断言实质上见于拉马努金致 Hardy 的头两封信（[16, pp. xxvii, 352]），但表述不正确（Watson [2] 指出）。订正版见 Hardy–Ramanujan 名篇 [1]（Hardy [6, p. 334]，Ramanujan [16, p. 304]），其中建立了分拆函数 $p(n)$ 的渐近公式。例 (iv) 是该定理的类比：$p(n)$ 的生成函数 Dedekind eta 函数在此基本被经典 theta 函数 $\theta(\tau)$ 代替，其中 $x = -e^{-\pi i\tau}$。Littlewood [1]（另见 Andrews [2, pp. 68–69]）写道，在与 Hardy 合作 $p(n)$ 的过程中，拉马努金坚持认为存在高度精确的 $p(n)$ 公式；这种坚持尤其推动 Hardy 发现了他们惊人精确的渐近公式；例 (iv) 表明拉马努金信心的根源早在印度时期就已奠定。1937 年 Rademacher [1] 发现了 $p(n)$ 的精确公式（当然推出 Hardy–Ramanujan 渐近公式为推论；证明见 Ayoub [1, Chap. 3]）；Zuckerman [1] 不久后也为本例的 $I(n)$ 以及其他模形式的倒数的 Fourier 系数找到了精确公式；Goldberg [1] 给出了经典 theta 函数倒数的 Fourier 系数的更简单公式与更简单证明。**对照：** M05（分拆 $p(n)$）、M06（theta 函数与模形式）。

**Entry 2。** 书中只记一句话：“Entry 2 是下述 Entry 3 的 $p = 1$ 特例。”即 Entry 2 为

$$\sum_{k=1}^{\infty} e^{-kx}k^{m-1} \sim \frac{\Gamma(m)}{x^m} - \sum_{k=0}^{\infty}(-1)^{m+k}\frac{B_{m+k}}{m+k}\cdot\frac{(-x)^k}{k!}, \qquad x \to 0+,$$

（Entry 3 取 $p = 1$ 所得），但书中未单独印出此公式。**状态：** 已证明（由 Theorem 3.1 推出）；**确切表述待核对**（见末尾待核对清单）。

Riesel [1] 曾考察 Entry 3–5 并断言它们不正确，因为他把它们当作精确公式来理解；作为渐近公式，Entry 3–5 确实正确。

## Entry 3

**陈述。** 设 $m$ 与 $p$ 为正整数，则当 $x \to 0+$ 时，

$$\sum_{k=1}^{\infty} e^{-k^px}k^{m-1} \sim \frac{\Gamma(m/p)}{px^{m/p}} - \sum_{k=0}^{\infty}(-1)^{m+pk}\frac{B_{m+pk}}{m+pk}\cdot\frac{(-x)^k}{k!}.$$

**推论。** 设 $p$ 为正整数，则当 $x \to 0+$ 时，

$$\sum_{k=1}^{\infty}\frac{e^{-k^px}}{k} \sim \frac{-\mathrm{Log}\,x}{p} + \gamma\left(1-1/p\right) - \sum_{k=1}^{\infty}(-1)^{pk}\frac{B_{pk}}{pk}\cdot\frac{(-x)^k}{k!}.$$

由 (0.1)，Entry 3 及其推论由下述 Theorem 3.1 推出。

**状态：** 已证明（Berndt 的 Mellin 变换证明）。**对照：** M12、M02、M01（Bernoulli 数）、M10（$\Gamma$）。

**我自验：** Entry 3 取 $m = 2$、$p = 1$、$x = 0.05$：左端 $\sum e^{-kx}k = 399.916677082$，右端 $1/x^2 - 1/12 + x^2/240 = 399.916677083$，差 $1.0\times 10^{-9}$；推论取 $p = 2$、$x = 0.1$：左端 $\sum e^{-k^2x}/k = 1.44827605835$，右端 $-\mathrm{Log}\,x/2 + \gamma/2 - \sum_{k=1}^{4} B_{2k}(-x)^k/(2k\cdot k!) = 1.44827605768$，差 $6.6\times 10^{-10}$。

## Theorem 3.1

**陈述。** 设 $p > 0$，$m$ 为复数，定义 $f(x) = \sum_{k=1}^{\infty} e^{-xk^p}k^{m-1}$。则当 $x \to 0+$ 时，

$$f(x) \sim \frac{\Gamma(m/p)}{px^{m/p}} + \sum_{k=0}^{\infty}\zeta(1-m-pk)\frac{(-x)^k}{k!}, \tag{3.1}$$

若 $m/p \notin \mathbf{Z}^{-}$；而若 $m/p = -r \in \mathbf{Z}^{-}$，则

$$f(x) \sim \left\{\frac{1}{p}(H_r-\gamma) + \gamma - \frac{1}{p}\mathrm{Log}\,x\right\}\frac{(-x)^r}{r!} + \sum_{k=0}^{\infty*}\zeta(1-m-pk)\frac{(-x)^k}{k!}, \tag{3.2}$$

其中 $\gamma$ 为 Euler 常数，$H_r = \sum_{k=1}^{r} 1/k$。

**证明思路（自写）。** Mellin 变换：$\int_0^{\infty} f(x)x^{s-1}\,dx = \Gamma(s)\zeta(1-m+ps)$（$\sigma > \sup\{0, m/p\}$）；Mellin 反演得 (3.3)；对矩形围道 $C_{M,T}$ 用留数定理：被积函数在 $s = m/p$ 与 $s = 0, -1, \dots, -N$ 处有单极点（$m/p = -r \in \mathbf{Z}^{-}$ 时在 $s = -r$ 处为双重极点），双重极点的留数 $R(-r)$ 由 (3.6)–(3.8) 算出；余项估计 (3.9)(3.10) 由 Stirling 公式 (3.11) 与 $\zeta(s) = O(|t|^k)$ (3.12) 得到。

## Theorem 3.2

**陈述。** 设 $p > 0$，定义 $g(x) = \sum_{k=1}^{\infty} e^{-xk^p}k^{m-1}\mathrm{Log}\,k$。则若 $m/p \notin \mathbf{Z}^{-}$，当 $x \to 0+$ 时，

$$g(x) \sim \frac{\Gamma'(m/p)-\Gamma(m/p)\,\mathrm{Log}\,x}{p^2x^{m/p}} - \sum_{k=0}^{\infty}\zeta'(1-m-pk)\frac{(-x)^k}{k!}.$$

$m = p = 1$ 的情形给出第 2 节例 (i)。Theorem 3.2 形式上由 Theorem 3.1 对 $m$ 求导得到（非严格步骤；拉马努金可能正是用此法推出第 2 节例 (i)）。证明与 Theorem 3.1 类似，只需把 $\zeta'(s)$ 的估计（由 Euler–Maclaurin 公式求导得到）代替 $\zeta(s)$ 的估计。

## 第 3 节例 (i)–(v)

拉马努金记录了若干例子说明上述结果。例 (i) 为 Entry 3 的推论取 $p = 2$ 的情形；例 (ii) 为 Entry 3 取 $p = 4$、$m = 2$ 的情形；例 (iii) 为 Entry 3 取 $p = 3$、$m = 2$ 的情形；例 (v) 为 Entry 3 取 $m = 3$、$p = 6$ 的情形。书中只记特例参数，未逐项印出展开式（待核对清单第 8 项）。例如例 (ii) 即 $\sum_{k=1}^{\infty} e^{-k^4x}k \sim \sqrt{\pi}/(4\sqrt{x}) - \sum_{k=0}^{\infty} B_{4k+2}(-x)^k/((4k+2)k!)$，例 (iii) 即 $\sum_{k=1}^{\infty} e^{-k^3x}k \sim \Gamma(2/3)/(3x^{2/3}) - \sum_{k=0}^{\infty}(-1)^{2+3k}B_{3k+2}(-x)^k/((3k+2)k!)$（均由 Entry 3 直接代入）。

**例 (iv)。** 当 $x \to 0+$ 时，

$$\sum_{k=1}^{\infty}\frac{e^{-k^2x}}{k^2} = \frac{\pi^2}{6} + \frac{x}{2} - \sqrt{\pi x} + O(\sqrt{x}e^{-\pi^2/x}).$$

证明：由 (1.2)，当 $t \to 0+$ 时 $\sum_{k=1}^{\infty} e^{-k^2t} = -\frac{1}{2} + \frac{1}{2}\sqrt{\pi/t} + O(e^{-\pi^2/t}/\sqrt{t})$；在 $[0, x]$ 上积分得 $\sum_{k=1}^{\infty}(1-e^{-k^2x})/k^2 = -x/2 + \sqrt{\pi x} + O(\sqrt{x}e^{-\pi^2/x})$；因 $\zeta(2) = \pi^2/6$ 即得。**我自验：** $x = 0.01$ 时左端 $1.47268868176$，右端 $\pi^2/6 + x/2 - \sqrt{\pi x} = 1.47268868176$，差 $0$（余项 $O(\sqrt{x}e^{-\pi^2/x})$ 在此量级下为零）。

## Entry 4

**陈述。** 设 $p > 0$，$m$、$d$ 为复数且 $\mathrm{Re}(pd-m) > 0$。定义

$$h(x) = \sum_{k=1}^{\infty}\frac{k^{m-1}}{(1+xk^p)^d}.$$

则若 $m/p \notin \mathbf{Z}^{-}$，当 $x \to 0+$ 时，

$$h(x) \sim \frac{\Gamma(m/p)\Gamma(d-m/p)}{p\Gamma(d)x^{m/p}} + \sum_{k=0}^{\infty}(d)_k\zeta(1-m-pk)\frac{(-x)^k}{k!},$$

其中如常 $(d)_k = \Gamma(d+k)/\Gamma(d)$。

**证明思路（自写）。** Mellin 变换：$\int_0^{\infty} h(x)x^{s-1}\,dx = \zeta(1-m+ps)\Gamma(s)\Gamma(d-s)/\Gamma(d)$（$m/p < \sigma < d$，$\sigma > 0$）；Mellin 反演后对同一矩形围道用留数定理，其余与 Theorem 3.1 平行。

**状态：** 已证明。**对照：** M12、M10（$\Gamma$ 商）、M02。

拉马努金以一个例子结束第 4 节：Entry 4 取 $p = 8$、$m = 2$、$d = 1/2$ 的情形（书中未印出展开式）。

## Entry 5 与 Entry 6

书中未把 Entry 5、Entry 6 作为独立公式印出，而是在第 4 节末以特例关系交代：

- **Entry 5** 是第 6 节 Theorem 6.1 取 $n = q = 1$、$m \ne p$ 的情形；**Entry 5 的推论**是 Theorem 6.1 取 $n = q = 1$、$m = p$ 的情形（即 $pn = qm$ 的双重极点情形）。
- 在 $m/p \ne n/q$ 的情形，Theorem 6.1 是 **Entry 6** 的稍广版本；在 $m/p = n/q$ 的情形，Theorem 6.1 推广了紧跟 Entry 6 之后标有“N.B.”的一项结果。

即 Entry 5 的陈述为 $f_{m,1}(x) = \sum_{j,k\ge 1} e^{-xk^pj}k^{m-1} \sim \Gamma(m/p)/(px^{m/p})\cdot\zeta(1-1+m/p) + \Gamma(1)/x\cdot\zeta(1-m+p) + \sum_{k=0}^{\infty}\zeta(1-m-pk)\zeta(-k)(-x)^k/k!$（$m \ne p$ 时），其推论为 $m = p$ 时的双重极点形式（见 Theorem 6.1）；Entry 6 的陈述即 Theorem 6.1 的一般 $m$、$n$、$p$、$q$ 形式。**状态：** 已证明（由 Theorem 6.1 推出）；**确切表述待核对**（书中未单独印出 Entry 5、Entry 6 的公式，见末尾待核对清单）。**对照：** M12、M02、M01。

另注：书中第 4 节末直接接 Theorem 6.1，未见独立的“第 5 节”节首；第 5 节的节编号存疑（见末尾待核对清单）。

## Theorem 6.1

**陈述。** 设 $p, q > 0$，$m$、$n$ 为复数。定义

$$f_{m,n}(x) = \sum_{j,k=1}^{\infty} e^{-xk^pj^q}k^{m-1}j^{n-1}.$$

则若 $m/p, n/q \notin \mathbf{Z}^{-}$，当 $x \to 0+$ 时，

$$f_{m,n}(x) \sim \frac{\Gamma(m/p)}{px^{m/p}}\zeta(1-n+qm/p) + \frac{\Gamma(n/q)}{qx^{n/q}}\zeta(1-m+pn/q) + \sum_{k=0}^{\infty}\zeta(1-m-pk)\zeta(1-n-qk)\frac{(-x)^k}{k!}, \quad \text{若 } pn \ne qm,$$

而

$$f_{m,n}(x) \sim \frac{\Gamma(m/p)}{pqx^{m/p}}\left\{(p+q)\gamma + \frac{\Gamma'(m/p)}{\Gamma(m/p)} - \mathrm{Log}\,x\right\} + \sum_{k=0}^{\infty}\zeta(1-m-pk)\zeta(1-n-qk)\frac{(-x)^k}{k!}, \quad \text{若 } pn = qm.$$

$p = q = 1$ 时，$f_{1,1}(x) = \sum_{r=1}^{\infty} e^{-rx}d(r)$，其中 $d(r)$ 为 $r$ 的正因数个数；Titchmarsh [3, p. 140] 在得到 $\zeta(s)$ 的均值定理时用了 $f_{1,1}(x)$ 的渐近展开，该展开由 Wigert [1] 首证，是 Theorem 6.1 的特例。

**证明思路（自写）。** Mellin 变换：$\int_0^{\infty} f_{m,n}(x)x^{s-1}\,dx = \Gamma(s)\zeta(1-m+ps)\zeta(1-n+qs)$（$\sigma > \sup\{0, m/p, n/q\}$）；留数定理：$pn \ne qm$ 时 $\delta_{m,n} = 1$，$pn = qm$ 时 $\delta_{m,n} = 1/2$（被积函数在 $m/p = n/q$ 处由两个单极点合并为双重极点），双重极点的留数由 (3.6)、(3.7) 及 $\Gamma(s)$ 在 $s = m/p$ 处的 Taylor 展开算出；其余与 Theorem 3.1 几乎相同。

## Theorem 6.2

**陈述。** 设 $p, q > 0$，$n$ 为复数，则若 $n/q \notin \mathbf{Z}^{-}$，当 $x \to 0+$ 时，

$$f_{0,n}(x) \sim \frac{\Gamma(n/q)\zeta(1+pn/q)}{qx^{n/q}} - \frac{\zeta(1-n)\,\mathrm{Log}\,x}{p} + A_n + \sum_{k=1}^{\infty}\zeta(1-pk)\zeta(1-n-qk)\frac{(-x)^k}{k!},$$

其中

$$A_n = \frac{\zeta'(1-n)q}{p} + \gamma\left(1-\frac{1}{p}\right)\zeta(1-n).$$

**证明思路（自写）。** 与 Theorem 6.1 的证明相同，只有一处不同：被积函数原先在 $s = 0$ 与 $s = m/p$ 处的单极点现合并为 $s = 0$ 处的双重极点；初等计算得 $R(0) = A_n - \zeta(1-n)\,\mathrm{Log}\,x/p$。

## Theorem 6.3

**陈述。** 设 $p, q > 0$。记

$$A_0 = \frac{\pi^2}{12pq} + \gamma^2\left(1 + \frac{1}{2pq} - \frac{1}{p} - \frac{1}{q}\right) - c_1\left(\frac{p}{q} + \frac{q}{p}\right), \qquad c_1 = \lim_{n\to\infty}\left(\sum_{r=1}^{n}\frac{\mathrm{Log}\,r}{r} - \frac{\mathrm{Log}^2 n}{2}\right).$$

则当 $x \to 0+$ 时，

$$f_{0,0}(x) \sim \frac{\mathrm{Log}^2 x}{2pq} - \frac{(p+q-1)\gamma\,\mathrm{Log}\,x}{pq} + A_0 + \sum_{k=1}^{\infty}\zeta(1-pk)\zeta(1-qk)\frac{(-x)^k}{k!}.$$

**证明思路（自写）。** 与 Theorem 6.1 的证明相同，只是原先在 $s = 0$、$m/p$、$n/q$ 处的单极点现合并为 $s = 0$ 处的三重极点；计算 $R(0)$ 需 $\Gamma(s)$、$\zeta(1+ps)$、$\zeta(1+qs)$ 在 $s = 0$ 附近的 Laurent 展开（$\Gamma(s) = 1/s - \gamma + (\gamma^2/2 + \pi^2/12)s + \cdots$；$\zeta(1+ps) = 1/(ps) + \gamma - c_1ps + \cdots$；$\zeta(s)$ 在 $s = 1$ 附近的 Laurent 展开见 Part I Ch. 7 Entry 13），得 $R(0) = \mathrm{Log}^2 x/(2pq) - (p+q-1)\gamma\,\mathrm{Log}\,x/(pq) + A_0$。

**注。** $A_n$ 在 $n \to 0$ 时不趋向 $A_0$。

Theorem 6.2 与 6.3 补充 Theorem 6.1，给出 $m$ 或 $n$ 或两者皆为 0 时的渐近展开。第 6 节末有两个例子：例 (i) 为 Theorem 6.2 取 $p = 2$、$n = q = 1$ 的情形；例 (ii) 为 Theorem 6.1 取 $m = 3$、$p = q = n = 1$ 的情形（书中只记特例参数，未逐项印出展开式；例 (ii) 的主项为 $2\zeta(3)/x^3 - 1/(12x) + \cdots$，由 Theorem 6.1 直接代入）。

## Entry 7

**陈述。**（Berndt 的订正版；拉马努金误写 $\sigma_{n-1}(s)$，应为 $\sigma_{n-m}(s)$。）当 $x \to 0+$ 时，

$$\sum_{s=1}^{\infty}\frac{s^{m-1}\sigma_{n-m}(s)}{e^{sx}-1} \sim \frac{\Gamma(m)}{x^m}\zeta(m)\zeta(1+m-n) + \frac{\Gamma(n)}{x^n}\zeta(n)\zeta(1+n-m) + \frac{\zeta(2-m)\zeta(2-n)}{x} + \sum_{k=0}^{\infty}\zeta(1-m-k)\zeta(1-n-k)\zeta(-k)\frac{(-x)^k}{k!}, \tag{7.1}$$

条件为 $m \ne n$、$m \ne 1$、$n \ne 1$，且 $m, n \notin \mathbf{Z}^{-}$。其中 $\sigma_r(s) = \sum_{d|s} d^r$。

**说明。** 置 $s = jk$，则 (7.1) 的左端 $= \sum_{s=1}^{\infty} s^{m-1}\sigma_{n-m}(s)\sum_{i=1}^{\infty} e^{-isx} = \sum_{i,j,k=1}^{\infty} e^{-ijkx}(jk)^{m-1}j^{n-m}$，即对 $p = q = r = l = 1$ 的特殊选取，左端等于下述三重和

$$f_{m,n,l}(x) := \sum_{i,j,k=1}^{\infty} e^{-xk^pj^qi^r}k^{m-1}j^{n-1}i^{l-1}. \tag{7.2}$$

Ramanujan 的公式 (7.1) 由 Theorem 7.1 取 $p = q = r = l = 1$ 得到。

**状态：** 已证明（Berndt 订正后证明）。**对照：** M12、M01（除数函数 $\sigma$）、M02。

**我自验：** (7.1) 取 $m = 2$、$n = 3$、$x = 0.5$：左端 $\sum_{s\ge 1} s\sigma_1(s)/(e^{0.5s}-1) = 28.4303348044$，右端 $\Gamma(2)\zeta(2)\zeta(0)/x^2 + \Gamma(3)\zeta(3)\zeta(2)/x^3 + \zeta(0)\zeta(-1)/x = 28.4303348044$（级数项全为零：每项含 $\zeta(-\text{偶数}) = 0$ 因子），差 $2.6\times 10^{-12}$。

## Theorem 7.1

**陈述。** 设 $p, q, r > 0$，$m$、$n$、$l$ 为复数，$f_{m,n,l}(x)$ 由 (7.2) 定义。设 $m/p, n/q, l/r \notin \mathbf{Z}^{-}$，$qm \ne np$、$rm \ne pl$、$rn \ne ql$，则当 $x \to 0+$ 时，

$$\begin{aligned}
f_{m,n,l}(x) \sim{}& \frac{\Gamma(m/p)}{px^{m/p}}\zeta(1-n+qm/p)\zeta(1-l+rm/p) \\
&+ \frac{\Gamma(n/q)}{qx^{n/q}}\zeta(1-m+pn/q)\zeta(1-l+rn/q) \\
&+ \frac{\Gamma(l/r)}{rx^{l/r}}\zeta(1-m+pl/r)\zeta(1-n+ql/r) \\
&+ \sum_{k=0}^{\infty}\zeta(1-m-pk)\zeta(1-n-qk)\zeta(1-l-rk)\frac{(-x)^k}{k!}.
\end{aligned}$$

**证明思路（自写）。** 与 Theorem 3.1、Theorem 6.1 的证明完全平行（Mellin 变换 + 矩形围道留数定理）。

**第 7 节例。** 拉马努金以 (7.1) 取 $m = 3$、$n = 5$ 的情形结束第 7 节；他又一次误写 $\sigma_{n-1}(s)$ 代替 $\sigma_{n-m}(s)$，且在渐近展开中无意漏掉了 $-1/(1440x)$ 一项（书中未印出完整展开式）。注：Berndt 指出上述定理还可以进一步推广与放宽参数限制，只是留数的计算会更困难。

## 第 8 节与 Entry 8

第 8 节开头，拉马努金说：“若 $F(h)$（第 15 章第 1 节者）终止，我们不知道结果在多远的范围内成立；但由下述及类似方法，我们可以计算这种情形下的误差。”为说明这些隐晦的话，他指出一个计算渐近展开中误差的方法：

$$\sum_{k=1}^{\infty}\frac{1}{e^{k^2x}-1} = \frac{\pi^2}{6x} + \frac{1}{2}\sqrt{\frac{\pi}{x}}\zeta\left(\frac{1}{2}\right) + \frac{1}{4} + o(1), \tag{8.1}$$

当 $x \to 0+$ 时；这是 Theorem 6.1 取 $p = 2$、$q = m = n = 1$ 的情形。事实上他指出等式

$$\int_{0}^{\infty}\sum_{k=1}^{\infty} e^{-k^2x}\cos(ax)\,dx = \sum_{k=1}^{\infty}\frac{k^2}{a^2+k^4} = \frac{\pi}{2\sqrt{2a}}\cdot\frac{\sinh(\pi\sqrt{2a})-\sin(\pi\sqrt{2a})}{\cosh(\pi\sqrt{2a})-\cos(\pi\sqrt{2a})} \tag{8.2}$$

可用来推出下述推广 (8.1) 的精确公式。

**Entry 8。** 若 $x > 0$，则

$$\begin{aligned}
\sum_{k=1}^{\infty}\frac{1}{e^{k^2x}-1} ={}& \frac{\pi^2}{6x} + \frac{1}{2}\sqrt{\frac{\pi}{x}}\zeta\left(\frac{1}{2}\right) + \frac{1}{4} \\
&+ \sqrt{\frac{\pi}{2x}}\sum_{k=1}^{\infty}\frac{1}{\sqrt{k}}\left\{\frac{\cos\left(\frac{\pi}{4}+2\pi\sqrt{\frac{\pi k}{x}}\right) - e^{-2\pi\sqrt{\pi k/x}}\cos\left(\frac{\pi}{4}\right)}{\cosh\left(2\pi\sqrt{\frac{\pi k}{x}}\right) - \cos\left(2\pi\sqrt{\frac{\pi k}{x}}\right)}\right\}.
\end{aligned} \tag{8.3}$$

Berndt 称：“这确实是一条非凡的公式。左端可看作 theta 函数 $\theta(x) = 1 + 2\sum_{k=1}^{\infty} 1/e^{k^2x}$ 的一种修正；因此 Entry 8 是 $\theta(x)$ 的反演公式的类比。”证明 Entry 8 之前先建立 (8.2)。

**证明思路（自写）。** (8.2) 的第一等式由交换求和与积分次序并用 Gradshteyn–Ryzhik [1, p. 477] 的积分求值即得；第二等式由部分分式展开：$\cosh(\pi\sqrt{2a})-\cos(\pi\sqrt{2a})$ 的非零零点在 $a = \pm k^2i$（$1 \le k < \infty$），皆为单零点，留数 $R(\pm k^2i) = \mp i/2$；故右端 $= \sum_{k=1}^{\infty} k^2/(a^2+k^4) + g(a)$（$g$ 整函数），令 $a \to \infty$ 得 $g(a) \to 0$，由 Liouville 定理 $g \equiv 0$。(8.2) 的第二等式的另一证明见 Glaisher [1]。Entry 8 的证明：置 $x = \pi y$，把 (8.3) 改写为 (8.4)；用 (8.2) 与 (8.5) 把余项 $R$ 化为 (8.6)；再用 Ch. 14 (6.1) 的 Poisson 求和公式（(8.9)–(8.11)）、Ch. 14 Entry 7 的推论 $\psi(uy) = -\frac{1}{2} + 1/(2\sqrt{uy}) + \psi(1/(uy))/\sqrt{uy}$（其中 $\psi(u) = \sum_{k=1}^{\infty} e^{-\pi k^2u}$）、Ch. 14 (5.2)（(8.13) 的 $-1/4$）与 Gradshteyn–Ryzhik [1, p. 395] 的积分（(8.15)–(8.16)），最后归结为 $\zeta(1/2) = \frac{1}{2}\int_0^{\infty}([u]-u)/u^{3/2}\,du$（Titchmarsh [3, p. 14, Eq. (2.1.5)]）。

**状态：** 已证明（Berndt 的证明；章首称“毫无疑问是新的结果”）。**对照：** M06（theta 函数反演）、M12、M04、M09（Poisson 求和）、M10（$\zeta(1/2)$）。

**我自验：** (8.3) 在 $x = 1$ 时左端 $0.600757604818$、右端 $0.600757604818$，差 $3.6\times 10^{-18}$；在 $x = 0.5$ 时左端 $1.70958483511$、右端 $1.70958483511$，差 $8.3\times 10^{-25}$。公式 (8.3) 的 $\sqrt{\pi k/x}$ 诸项已用 300 DPI 放大图逐字确认（150 DPI 初读无误）。

## 第 9 节：$F_{m,n}(x)$、$L$、$M$、$N$ 与 Eisenstein 级数

本节无编号 Entry 9（第 9 节只有定义与 $L$、$M$、$N$ 的引入，Entry 10(i) 紧接其后）。

**定义。** 置

$$F_{m,n}(x) = \sum_{j,k=1}^{\infty} j^m k^n e^{-jkx}, \tag{9.1}$$

其中 $x > 0$，$m$、$n$ 为非负整数；不失一般性设 $m \ge n$。Theorem 6.1 给出 $F_{m,n}(x)$ 在 $x \to 0+$ 时的渐近展开。拉马努金以 Theorem 6.1 取 $p = q = 1$、$m \ne n$ 的特例开始第 9 节；然后对 $|q| < 1$ 定义

$$L = 1 - 24\sum_{k=1}^{\infty}\frac{kq^k}{1-q^k}, \qquad M = 1 + 240\sum_{k=1}^{\infty}\frac{k^3q^k}{1-q^k}, \qquad N = 1 - 504\sum_{k=1}^{\infty}\frac{k^5q^k}{1-q^k}.$$

函数 $L$、$M$、$N$ 在拉马努金名篇 [11]（[16, pp. 136–162]）中得到透彻研究，那里分别记为 $P$、$Q$、$R$。$L$、$M$、$N$ 本质上是全模群 $\Gamma(1)$ 上权分别为 2、4、6 的 Eisenstein 级数：置 $q = \exp(2\pi i\tau)$，$\tau$ 在上半平面 $\mathfrak{H}$ 中，记

$$\Phi_v(q) := \sum_{k=1}^{\infty}\frac{k^v q^k}{1-q^k} = \sum_{k=1}^{\infty} k^v\sum_{j=1}^{\infty} e^{2\pi ijk\tau} = \sum_{r=1}^{\infty}\sigma_v(r)e^{2\pi ir\tau}, \tag{9.2}$$

其中 $\sigma_v(r) = \sum_{k|r} k^v$。Eisenstein 级数 $E_n(\tau)$（$n$ 为偶正整数）的 Fourier 展开为（Rankin [2, p. 194]）

$$E_2(\tau) = 1 - 24\sum_{k=1}^{\infty}\sigma_1(k)e^{2\pi ik\tau} - \frac{3}{\pi y} = 1 - 24\Phi_1(q) - \frac{3}{\pi y} \tag{9.3}$$

与

$$E_n(\tau) = 1 - \frac{2n}{B_n}\sum_{k=1}^{\infty}\sigma_{n-1}(k)e^{2\pi ik\tau} = 1 - \frac{2n}{B_n}\Phi_{n-1}(q), \qquad n > 2, \tag{9.4}$$

其中 $y = \mathrm{Im}\,\tau > 0$，$B_n$ 为第 $n$ 个 Bernoulli 数。于是 $L = E_2(\tau) + 3/(\pi y)$，$M = E_4(\tau)$，$N = E_6(\tau)$。

拉马努金接着断言：若 $m+n$ 为奇正整数，则 (9.1) 的 $F_{m,n}(x)$ 可用 $L$、$M$、$N$ 精确表出。事实上，置 $jk = r$ 得 $F_{m,n}(x) = \sum_{r=1}^{\infty} r^n\sigma_{m-n}(r)e^{-rx}$；取 $x = -2\pi i\tau$，若 $m-n$ 为奇数，则 $F_{m,n}(x)$ 本质上是偶权 Eisenstein 级数的 $n$ 重导数。若 $m-n = 1$ 且 $n \ge 1$，$F_{m,n}(x)$ 显然是 $L$ 的 $n$ 重导数的倍数；若 $m-n$ 为大于 1 的奇数，由 Rankin [2, p. 199] 的定理，每个偶正权模形式都可表为 $E_4(\tau)$ 与 $E_6(\tau)$ 的多项式，故 $\sum_{r=1}^{\infty}\sigma_{m-n}(r)e^{-rx}$ 可如此表出，而 $F_{m,n}(x)$ 至多差一个 $\pm 1$ 因子是其 $n$ 重导数，因而 $F_{m,n}(x)$ 可表为 $M$、$N$ 及其导数的多项式。进一步的评述见 Venkatachaliengar [1, pp. 30, 31]。

**对照：** M06（Eisenstein 级数主线）、M07（$q$ 展开）、M01（$\sigma_v$、Bernoulli 数）。

## Entry 10(i)

**第一部分。** 对每个正整数 $n \ge 2$，

$$-\frac{B_{2n}}{4n}E_{2n}(\tau) = -\frac{B_{2n}}{4n} + \sum_{k=1}^{\infty}\sigma_{2n-1}(k)e^{2\pi ik\tau}$$

可表为 $M$ 与 $N$ 的多项式。此断言已在第 9 节用 Rankin [2, p. 199] 验证；另见 (14.2) 与下述 Entry 14。

**第二部分。** 对每个正整数 $n$，

$$f_n(x) := \sum_{k=1}^{\infty}\frac{k^{2n}q^k}{(1-q^k)^2} - \delta_n\frac{nL}{6}\left\{-\frac{B_{2n}}{4n} + \sum_{k=1}^{\infty}\frac{k^{2n-1}q^k}{1-q^k}\right\}$$

可表为 $M$ 与 $N$ 的多项式；其中 $\delta_1 = 1/2$，$n \ge 2$ 时 $\delta_n = 1$。

**证明思路（自写）。** 由 (9.3)(9.4)，$\sum_{k=1}^{\infty} k^{2n}q^k/(1-q^k)^2 = (1/(2\pi i))\,d/d\tau(-(B_{2n}/4n)E^*_{2n}(\tau))$，其中 $E^*_{2n}(\tau) = E_2(\tau) + 3/(\pi y) = L$（$n = 1$ 时），$E_{2n}(\tau)$（$n > 1$ 时）。于是 $f_n(x) = F_n(\tau) := (1/(2\pi i))\,d/d\tau(-(B_{2n}/4n)E^*_{2n}(\tau)) + (\delta_n n E^*_2(\tau)/6)(B_{2n}/(4n))E^*_{2n}(\tau)$；由 Rankin [2, p. 199]，只需证 $F_n(\tau)$ 是 $\Gamma(1)$ 上权 $2n+2$ 的模形式，即 $F_n(-1/\tau) = \tau^{2n+2}F_n(\tau)$（(10.1)，Serre [1, Eq. (5), p. 80]），这由 (10.2)（$E^*_{2n}$ 在 $V\tau = (a\tau+b)/(c\tau+d) \in \Gamma(1)$ 下的变换）推出；$n > 1$ 时 (10.1) 也可由 Ogg [1, pp. 16, 17] 的定理推出（若 $f(\tau)$ 为权 $k$ 模形式，则 $f'(\tau) - (2\pi ik/12)E^*_2(\tau)f(\tau)$ 为权 $k+2$ 模形式）。**拉马努金未考虑 $n = 1$ 的情形**（Berndt 用 $\delta_1 = 1/2$ 补入）。

**状态：** 已证明。**对照：** M06（模形式主线）、M01（Bernoulli 数）。

## Entry 10(ii)

**陈述。**（逐字引自笔记，pp. 186–187）“级数的度是各项的最高幂之和，若级数含有 $x$ 的所有幂或 $x$ 的幂成等差数列（A.P.），则再加 1。若每项的系数是齐次的，则级数称为纯的，其他情形称为混合的。指标理论在级数的度方面成立。若第 15 章第 1 节中的 $F(h)$ 终止，则级数称为完全的；若不终止，则称为不完全的。若 $F(h) = 0$，则级数称为完备的，其他情形称为不完备的。级数称为绝对完备的，当它在变换或拆分后仍保持完备时。线性级数只能由线性级数表出，双重级数只能由双重级数表出，三重级数只能由三重级数表出，纯级数只能由纯级数表出，完全级数只能由完全级数表出，不完全级数只能由不完全级数表出，绝对完备级数只能由绝对完备级数表出，在所有情形下都遵守指标法则；但混合级数可以拆分为若干不同度的纯级数。”

Berndt 注：M. E. H. Ismail 建议，级数的度更恰当地定义为收敛边界上奇点的阶；若边界上有不止一个奇点，此定义可能含糊；但对拉马努金的部分例子，Ismail 的定义更可行。“指标理论”是什么意思，我们不知道；$F(h)$ 的定义见 Entry 1。

**第 10 节例 1。** 设 $f_1(x) = \sum_{k=1}^{\infty} k^n x^k$（$|x| < 1$），$n$ 为非负整数。$f_1$ 的度为 $n+1$（$k^n$ 的度为 $n$，$x^k$ 贡献 1）；因 $f_1$ 在 $x = 1$ 处有 $n+1$ 阶极点，按 Ismail 的定义度亦为 $n+1$。$k^n$ 是齐次的（$g(jk) = (jk)^n = j^n g(k)$），故 $f_1$ 是纯的。$\varphi(t) = t^n x^t$，因 $\varphi^{(2k-1)}(0)$ 对充分大的 $k$ 未必为 0，$F(h)$ 不终止，故 $f_1$ 不完全；$f_1$ 不完备；若“线性”指级数不是多重级数，则 $f_1$ 是线性的。

**第 10 节例 2。** 设 $f_2(x) = \sum_{k=1}^{\infty} \sin(kx)/k$（$x$ 实）。$\sin(kx)$ 的度大概为 1，$1/k$ 的度为 $-1$，故 $f_2$ 的度为 0；$x = 2n\pi$ 处的奇点是“跳跃”间断点，阶为 0，按此解释 $f_2$ 的度亦为 0。系数皆为 $1/k$，故 $f_2$ 是纯的、线性的。$F(h) \not\equiv 0$，但 $\varphi(t) = \sin(tx)/t$ 是 $t$ 的偶函数，故 $\varphi^{(2k-1)}(0) = 0$（$k \ge 1$），于是 $f_2$ 完全且不完备。

**第 10 节例 3。** $F_{m,n}(x)$（由 (9.1) 定义）是纯的双重级数；$j^m$、$k^n$、$e^{-x}$ 的度分别为 $m$、$n$、1，故 $F_{m,n}(x)$ 的度为 $m+n+1$。但它在 $x = 0$ 处的奇点阶并不等于 $m+n+1$；由 Theorem 6.1，$F_{m,n}$ 不完备。Theorem 6.1 右端的级数之项为 $\zeta(-m-k)\zeta(-n-k)(-x)^k/k! = B_{m+k+1}B_{n+k+1}(-x)^k/((m+k+1)(n+k+1)k!)$（由 (0.1)，$k \ge 1$ 时）；若 $m+n$ 为偶数，当 $m$ 与 $k$ 奇偶相反时此项不为 0，故 $m+n$ 为偶数时 $F_{m,n}$ 不完全；若 $m+n$ 为奇数，则 $B_{m+k+1}$ 或 $B_{n+k+1}$ 为 0，故 $m+n$ 为奇数时 $F_{m,n}$ 完全。

**第 10 节例 4。** 设 $m$、$n$ 为正整数，$m \ne n$，$g_{m,n}(x) = \sum_{i,j,k=1}^{\infty} e^{-ijkx}j^m k^n$；按第 7 节记号 $g_{m,n}(x) = f_{m+1,n+1,1}$。拉马努金断言 $g_{m,n}$ 是度为 $m+n+1$ 的三重纯级数，显然成立；但由 Theorem 7.1，度的另一定义在此失效；由 Theorem 7.1，$g_{m,n}$ 不完备。$g_{m,n}(x)$ 的渐近展开中典型项（由 Theorem 7.1 与 (0.1)）为 $(-1)^{m+n}B_{m+k+1}B_{n+k+1}B_{k+1}x^k/((m+k+1)(n+k+1)(k+1)k!)$；若 $m$、$n$ 皆为偶数，展开不终止，故 $g_{m,n}$ 不完全；若 $m$ 或 $n$ 为奇数，展开终止，故 $g_{m,n}$ 在这些情形下完全。

**第 10 节例 5。** 设 $m$、$n$、$x$ 为实数，$n > 0$，$h_{m,n}(x) = \sum_{k=1}^{\infty} k^m/(e^{kx}+e^{-kx})^n$。拉马努金断言 $h_{m,n}(x)$ 是双重级数，显然他把 $h_{m,n}(x)$ 写成 $h_{m,n}(x) = \sum_{k=1}^{\infty}\sum_{j=0}^{\infty}(-1)^j(n)_j/j!\cdot k^m e^{-kx(n+2j)}$（$x > 0$）。系数不是齐次的，故级数是混合的。拉马努金断言 $h_{m,n}$ 的度为 $m+n$，但 Berndt 认为度应为 $m+n+1$（$k^m$、$e^{-kxn}$、$e^{-2jkx}$ 的度分别为 $m$、$n$、1）；$h_{m,n}$ 在 $x = 0$ 处有本性奇点；$h_{m,n}$ 不完备。

**第 10 节例 6。** theta 函数 $f(x) = \frac{1}{2} + \sum_{k=1}^{\infty} x^{k^2} = \frac{1}{2}\sum_{k=-\infty}^{\infty} x^{k^2}$（$|x| < 1$）。$f$ 显然是纯的；因 $x^{t^2}$ 是 $t$ 的偶函数，$F(h)$ 终止，故 $f$ 完全。拉马努金还断言 $f$ 是纯双重级数，这令人费解——若把 $x^{k^2}$ 按 $k$ 的幂级数展开，$f$ 不再是纯的；但若他用“双重”指“双边”，则断言正确。最后他断言 $f$ 的度为 $1/2$，Berndt 无法用拉马努金的度定义证成；$f$ 在 $x = 0$ 处解析，但若置 $x = e^{\pi i\tau}$（$\tau \in \mathfrak{H}$），由 theta 变换公式 (1.2)，可含糊地把 $f(e^{\pi i\tau})$ 说成在 $\tau = 0$ 处有“$1/2$ 阶奇点”；当然这并不真正成立，因为实轴是 $f(e^{\pi i\tau})$ 的自然边界；于是 Ismail 定义的含糊解释有几分可行性。

**第 10 节例 7。** 拉马努金说 $L$、$M$、$N$ 是度分别为 2、4、6 的完全纯双重级数。把 $(1-q^k)^{-1}$ 按几何级数展开即见 $L$、$M$、$N$ 是度分别为 2、4、6 的纯双重级数（$q^{jk}$（$1 \le j, k < \infty$）的度为 1）。再对 Theorem 6.1 取 $m = p = q = 1$、$e^{-x} = q$，$n = 2, 4, 6$；因 $B_{1+k}B_{n+k} = 0$（$k \ge 1$），$L$、$M$、$N$ 完全。拉马努金断言 $M$、$N$ 完备而 $L$ 不完备；但 Berndt 认为三者皆不完备，因为在 Theorem 6.1 中 $\zeta(2-n)/x + \Gamma(n)\zeta(n)/x^n \ne 0$。

**状态：** Entry 10(ii) 的定义为拉马努金原文引述，Berndt 认为多处含糊、不重要；七个例子中多处断言经 Berndt 订正（例 3 的奇点阶、例 5 的度、例 6 的“双重”与度 $1/2$、例 7 的完备性）。**对照：** M06、M12。

## Entry 11

**陈述。** 若 $\alpha, \beta > 0$ 且 $\alpha\beta = \pi^2$，则

$$\frac{1}{4}\sum_{k=1}^{\infty}\frac{1}{k^2\sinh^2(\alpha k)} + \frac{1}{4}\sum_{k=1}^{\infty}\frac{1}{k^2\sinh^2(\beta k)} - 2\alpha\sum_{k=1}^{\infty}k^2\mathrm{Log}(1-e^{-2\alpha k}) - 2\beta\sum_{k=1}^{\infty}k^2\mathrm{Log}(1-e^{-2\beta k}) = \frac{\alpha^2+\beta^2}{120} - \frac{\alpha\beta}{72}.$$

**证明思路（自写）。** 初等计算得 $\sum_{k=1}^{\infty} k^2\mathrm{Log}(1-e^{-2\alpha k}) = -\frac{1}{4}\sum_{j=1}^{\infty}\cosh(\alpha j)/(j\sinh^3(\alpha j))$（(11.1)）；以此为启发，定义 $f(z) = \pi\cot(\pi z)(1/(z^2\sinh^2(\alpha z)) + 2\alpha\cosh(\alpha z)/(z\sinh^3(\alpha z)))$，对矩形 $C_N$ 用留数定理：$f$ 在非零整数 $k$ 处有单极点，留数和为 (11.2)；第一部分 $f_1(z) = \pi\cot(\pi z)/(z^2\sinh^2(\alpha z))$ 在 $z = ik\pi/\alpha$ 处有双重极点（Churchill [1, p. 160] 的双重极点留数公式 (11.3)），留数和为 (11.4)；第二部分 $f_2(z) = 2\pi\alpha\cot(\pi z)\cosh(\alpha z)/(z\sinh^3(\alpha z))$ 在 $z = i\pi k/\alpha$ 处有三重极点（三重极点留数公式 (11.5)），留数和为 (11.6)；$f$ 在原点有 5 阶极点，留数 $R(0) = \alpha\beta/9 - (\alpha^2+\beta^2)/15$（(11.7)）；围道积分 $I_N = o(1)$（(11.8)）。令 $N \to \infty$，留数和为 0 即得 Entry 11。Entry 11 的另一证明可由 Berndt 的论文 [6, Theorems 2.2, 2.16] 结合 (11.1) 构造。

**状态：** 已证明（Berndt 的留数证明；章首称“优美而新的互反公式”）。**对照：** M02（互反级数）、M04（$\pi^2$）、M09（留数积分）、M14（Ch. 14 的互反公式）。

**我自验：** 取 $\alpha = \beta = \pi$：左端 $0.0274155677808$，右端 $\pi^2/360 = 0.0274155677808$，差 $4.7\times 10^{-29}$。

## Entry 12

**陈述。** 设 $L$、$M$、$N$ 如第 9 节所定义，$E_n(\tau)$（$n > 2$）与 $\Phi_n(q)$ 分别由 (9.4) 与 (9.2) 定义。定义判别式函数

$$\Delta(\tau) = q\prod_{k=1}^{\infty}(1-q^k)^{24}, \qquad q = e^{2\pi i\tau},\ \tau \in \mathfrak{H}.$$

则对 $|q| < 1$，

$$\begin{aligned}
\text{(i)}\quad M^3 - N^2 &= 1728\Delta(\tau), \\
\text{(ii)}\quad E_8(\tau) &= M^2, \\
\text{(iii)}\quad E_{10}(\tau) &= MN, \\
\text{(iv)}\quad E_{14}(\tau) &= M^2N, \\
\text{(v)}\quad \sum_{k=1}^{\infty}\frac{k^2q^k}{(1-q^k)^2} &= \frac{M-L^2}{288}, \\
\text{(vi)}\quad \sum_{k=1}^{\infty}\frac{k^4q^k}{(1-q^k)^2} &= \frac{LM-N}{720}, \\
\text{(vii)}\quad \sum_{k=1}^{\infty}\frac{k^6q^k}{(1-q^k)^2} &= \frac{M^2-LN}{1008}, \\
\text{(viii)}\quad \sum_{k=1}^{\infty}\frac{k^8q^k}{(1-q^k)^2} &= \frac{LM^2-MN}{720}, \\
\text{(ix)}\quad L\sum_{k=0}^{\infty}(-1)^k(2k+1)q^{k(k+1)/2} &= \sum_{k=0}^{\infty}(-1)^k(2k+1)^3q^{k(k+1)/2}, \\
\text{(x)}\quad M\sum_{k=1}^{\infty}\frac{(2k-1)q^k}{1-q^{2k-1}} &= \sum_{k=1}^{\infty}\frac{(2k-1)^5q^k}{1-q^{2k-1}}.
\end{aligned}$$

**证明思路（自写）。** (i)–(iv) 是 Rankin [2, p. 199] 的一般定理的特例（该定理在第 9 节已用），亦见 Rankin [2, pp. 195, 197, Eqs. (6.1.8), (6.1.9), (6.1.14)]；这些公式也由拉马努金在 [11]（[16, p. 141]）中导出。(v)–(viii) 最初属于拉马努金，证明见 [11]（[16, pp. 141, 142]）。(ix) 的第一证明：它是拉马努金在第 16 章建立的一般公式的特例（Part III，Ch. 16，Entry 35(i)）；第二证明：把 (ix) 重排后比较 $q^n$ 的系数，得 Glaisher [2]（1884 年）的算术恒等式：若 $n$ 不是三角数，则 $\sigma(n) - 3\sigma(n-1) + 5\sigma(n-3) - 7\sigma(n-6) + \cdots = 0$（(12.1)）；若 $n = r(r+1)/2$ 为三角数，则上式 $= \frac{1}{6}(-1)^{r-1}r(r+1)(2r+1) = (-1)^{r-1}\sum_{k=1}^{r} k^2$（(12.2)）；这些恒等式实为 Halphen [1] 七年前证明的公式的推论。(x) 的证明：把 (x) 改写为 $N_1 - N_0 = 21M(L_1 - L_0)$（(12.3)），用 $\Gamma(2)$ 上的权 2、权 6 模形式空间 $M_2$、$M_6$ 的基（$X_0$、$X_{\infty}$ 及其幂）与 $q$ 展开比较系数；此证明由 D. W. Masser 提供；A. O. L. Atkin 用 $\Gamma_0(2)$ 上的模形式理论给出了 (x) 的另一证明；Ramamani 在其学位论文 [1, p. 59] 中用椭圆函数理论给出了 (x) 的证明。

**注。** Entry 12(x) 等价于优美的恒等式

$$\sum_{k=0}^{n}\sigma_1(2k+1)\sigma_3(n-k) = \frac{1}{240}\sigma_5(2n+1), \qquad n \ge 0,$$

其中 $\sigma_3(0) = 1/240$。拉马努金在 [11]（[16, p. 146]）中无证明地陈述此恒等式，并表示他有两个证明，一个是初等的，另一个用椭圆函数，但他对任一证明都未给提示；Berndt 表示在文献中找不到初等证明，自己也未能给出。另：拉马努金在 [11]（[16, pp. 136–162]）中研究 $\sum_{r,s}(n) = \sum_{k=0}^{n}\sigma_r(k)\sigma_s(n-k)$（$r$、$s$ 为奇正整数，$\sigma_m(0) = \frac{1}{2}\zeta(-m)$），建立了它在 $n \to \infty$ 时带误差项的渐近公式，并猜想了更好的误差项（[11]，[16, p. 136, Eq. (3)]）；此猜想直到 1978 年才由 Levitt [1] 在其学位论文中证明；Levitt 建立了误差项恒为 0 的充要条件，从而表明拉马努金找到的此类情形是穷尽的；Grosjean [1]、[2] 也发现了类似定理，并对与 $\sum_{r,s}(n)$ 相连的递推公式作了系统研究；Lehmer [1] 写过一篇关于 $\sigma_k(n)$ 的卷积的有益综述；其他文献见 [1, Sect. A30]（LeVeque 编）。

**状态：** 已证明（(i)–(viii) 见 Rankin 与拉马努金 [11]；(ix) 见 Part III Ch. 16 Entry 35(i) 与 Glaisher–Halphen；(x) 见 Masser、Atkin、Ramamani 的证明）。**对照：** M06（Eisenstein 级数与 $\Delta$，M06 的 $\Delta$ 与 $\tau(n)$ 主线）、M01（$\sigma$ 恒等式）、M07（$q$ 展开）、M11（椭圆函数证明）。

**我自验：** 取 $q = 0.1$：(i) $M^3-N^2 = 1728\Delta(\tau) = 10.544407496$，差 $2.4\times 10^{-27}$；(v) 差 $2.5\times 10^{-32}$；(vi) 差 $4.9\times 10^{-32}$；(vii) 差 $3.9\times 10^{-31}$；(viii) 差 $0$。(x) 的等价恒等式在 $n = 0$–$6$ 时用精确整数运算复核成立（须用约定 $\sigma_3(0) = 1/240$；例如 $n = 2$ 时左端 $13.025$、右端 $13.025$）。

## Entry 13

**陈述。** 设 $\Phi_n(q)$ 如 Entry 12 所定义，则对 $|q| < 1$，

$$\begin{aligned}
\text{(i)}\quad 691 + 65,520\Phi_{11}(q) &= 441M^3 + 250N^2, \\
\text{(ii)}\quad 3,617 + 16,320\Phi_{15}(q) &= 1,617M^4 + 2,000MN^2, \\
\text{(iii)}\quad 43,867 - 28,728\Phi_{17}(q) &= 38,367M^3N + 5,500N^3, \\
\text{(iv)}\quad 174,611 + 13,200\Phi_{19}(q) &= 53,361M^5 + 121,250M^2N^2, \\
\text{(v)}\quad 77,683 - 552\Phi_{21}(q) &= 57,183M^4N + 20,500MN^3, \\
\text{(vi)}\quad 236,364,091 + 131,040\Phi_{23}(q) &= 49,679,091M^6 + 176,400,000M^3N^2 + 10,285,000N^4, \\
\text{(vii)}\quad 657,931 - 24\Phi_{25}(q) &= 392,931M^5N + 265,000M^2N^3, \\
\text{(viii)}\quad 3,392,780,147 + 6,960\Phi_{27}(q) &= 489,693,897M^7 + 2,507,636,250M^4N^2 + 395,450,000MN^4, \\
\text{(ix)}\quad 1,723,168,255,201 - 171,864\Phi_{29}(q) &= 815,806,500,201M^6N + 881,340,705,000M^3N^3 + 26,021,050,000N^5, \\
\text{(x)}\quad 7,709,321,041,217 + 32,640\Phi_{31}(q) &= 764,412,173,217M^8 + 5,323,905,468,000M^5N^2 + 1,621,003,400,000M^2N^4.
\end{aligned}$$

**注记。**

$$q\frac{dL}{dq} = \frac{L^2-M}{12}, \qquad q\frac{dM}{dq} = \frac{LM-N}{3}, \qquad q\frac{dN}{dq} = \frac{LN-M^2}{2}.$$

**例。** 对 $|q| < 1$ 定义 $\Phi_{r,s}(q) = \sum_{j,k=1}^{\infty} j^r k^s q^{jk}$（于是 $\Phi_{0,s}(q) = \Phi_s(q)$），则

$$\begin{aligned}
\text{(i)}\quad 20,736\Phi_{4,5}(q) &= 15LM^2 + 10L^3M - 20L^2N - 4MN - L^5, \\
\text{(ii)}\quad 1,728\Phi_{2,7}(q) &= 2LM^2 - MN - L^2N, \\
\text{(iii)}\quad 3,456\Phi_{3,6}(q) &= L^3M - 3L^2N + 3LM^2 - MN.
\end{aligned}$$

上述全部结果见于拉马努金论文 [11]（[16, pp. 141, 142]），其中指出了证明方法。

**状态：** 已证明（拉马努金 [11]）。**对照：** M06（Eisenstein 级数）、M01（$\sigma$ 与 $\Phi_v$）、M07（$q$ 级数）。

**我自验：** 取 $q = 0.1$：(i) 左端 $117,774,068.418$、右端 $117,774,068.418$，差 $1.3\times 10^{-23}$；例 (i) 左端 $23,616.082784$、右端 $23,616.082784$，差 $1.3\times 10^{-26}$。例 (ii)(iii) 未逐项数值复核（见待核对清单）。

## Entry 14

**陈述。** 若 $n$ 为大于 4 的偶整数，则

$$-\frac{(n+2)(n+3)}{2n(n-1)}S_{n+2} = -20\binom{n-2}{2}S_4S_{n-2} + \sum_{k=1}^{[(n-2)/4]}{}'\binom{n-2}{2k}\{(n+3-5k)(n-8-5k) - 5(k-2)(k+3)\}S_{2k+2}S_{n-2k},$$

其中求和号上的撇表示：若 $(n-2)/4$ 为整数，则和的最后一项乘以 $1/2$。

**记号。** 若 $n$ 为偶正整数，拉马努金定义

$$S_n = \frac{(-1)^{n/2-1}B_n}{2n} + (-1)^{n/2}\sum_{k=1}^{\infty}\frac{k^{n-1}q^k}{1-q^k},$$

其中 $|q| < 1$，$B_n$ 为第 $n$ 个 Bernoulli 数。若 $n > 1$ 且 $q = \exp(2\pi i\tau)$（$\tau \in \mathfrak{H}$），则由 (9.4)，$S_{2n} = (-1)^{n-1}B_{2n}/(4n)\cdot E_{2n}(\tau)$。又由 (14.1)，$S_{2n+2} = (2n)!/(2(2\pi)^{2n+2})\cdot b(n)$（$n \ge 1$）（(14.10)），其中

$$b(n) = 2(2n+1)\zeta(2n+2)E_{2n+2}(\tau). \tag{14.1}$$

**证明思路（自写）。** 先建立 Weierstrass $\wp$ 函数的事实（Apostol [3, pp. 12, 13]）：$\wp(z) = 1/z^2 + \sum_{\omega\ne 0}(1/(z-\omega)^2 - 1/\omega^2)$（$\omega = m\omega_1 + n\omega_2$）；对 $n \ge 3$，$(2n+3)(n-2)b(n) = 3\sum_{k=1}^{n-2} b(k)b(n-1-k)$（(14.2)，此即 Entry 10(i) 第一部分的更明确版本）；$\omega_1 = 1$、$\omega_2 = \tau$ 时 $\wp(z) = 1/z^2 + \sum_{k=1}^{\infty} b(k)z^{2k}$（(14.3)）；$\wp$ 满足两个微分方程 $\{\wp'(z)\}^2 = 4\wp^3(z) - 20b(1)\wp(z) - 28b(2)$（(14.4)）与 $\wp''(z) = 6\wp^2(z) - 10b(1)$（(14.5)）；(14.2) 由 (14.5) 立得。引理：$\wp^{(4)}(z) = 30\{\wp'(z)\}^2 + 240b(1)\wp(z) + 504b(2)$（由 (14.5) 求导两次并用 (14.4)）。把 Entry 14 用 (14.10) 改写为关于 $b$ 的恒等式 (14.11)，再用 (14.2) 的改写形式 (14.12) 化归为 (14.13)，减 $2(m+1)b(m+1)$ 得 (14.14)；(14.14) 的三部分恰为 $2b(1)\wp(z)$、$\wp'(z)^2/4$ 与 $\wp^{(4)}(z)/120$ 的 $z^{2m-2}$ 系数，故由引理得证。

Berndt 注：在 Entry 14 中，拉马努金给出 $S_{2n+2}$ 的递推公式，与 (14.2) 不同；他在论文 [11]（[16, p. 140, Eq. (22)]）中用不同的 $S_n$ 定义给出了 (14.2) 的一个非常巧妙的证明；Rankin [1] 也给出了 (14.2) 的初等证明以及 $S_{2n}$ 的其他递推公式与文献指引。但 Entry 14 的递推公式（拉马努金在笔记 p. 191 中表述不完全）在文献中似乎未曾出现。

**状态：** 已证明（Berndt 的证明；拉马努金原表述不完全）。**对照：** M06（Eisenstein 级数递推）、M11（$\wp$ 函数）、M01（Bernoulli 数）。

**我自验：** 取 $n = 6$：Entry 14 化为 $S_8 = 120S_4^2$（$q \to 0$ 时 $S_4 \to 1/240$、$S_8 \to 1/480$，精确成立）；取 $q = 0.1$ 数值复核，$S_8 = 6.40441790794 = 120S_4^2$，差 $7.9\times 10^{-31}$。

## 第 15 节：模方程的先声

Berndt 注：乍看之下，接下来两节的材料似乎没什么意思；但它是拉马努金在 Ch. 18–21 关于模方程的工作的先驱性介绍。下述“模方程”的定义是拉马努金个人的定义，不同于他后来使用的标准定义（例如见 Hardy 的书 [9, p. 214]）；关于这两种定义的类比，见 Berndt 的论文 [10]。

### 第 15 节 (i)：2 次模方程与乘子

设 $F(x) = (1-x)^{-1/2}$，拉马努金以平凡恒等式开始第 15 节 (i)：

$$F\left(\frac{2t}{1+t}\right) = (1+t)F(t^2), \tag{15.1}$$

用二项级数写出。若置 $\alpha = 2t/(1+t)$、$\beta = \alpha^2/(2-\alpha)^2$，则 (15.1) 可写为

$$F(\alpha) = M_2(\alpha)F(\beta), \tag{15.2}$$

其中 $M_2(\alpha) = 2/(2-\alpha)$。拉马努金说 $\beta = \alpha^2/(2-\alpha)^2$ 是 2 次模方程，(15.2) 中的因子 $M_2(\alpha)$ 是“乘子”。他还记录了 $M_2(\alpha)$ 的如下表示：

$$M_2(\alpha) = 1 + \sqrt{\beta} = \sqrt{\frac{1-\beta}{1-\alpha}} = \sqrt{(1-\alpha)(1-\beta)} + 2\sqrt{\beta},$$

每式都容易验证。再考虑更一般的方程

$$F(\alpha) = M_n(\alpha)F(\beta), \tag{15.3}$$

其中 $\beta = R_n(\alpha)$ 是“$n$ 次”的函数，$F(x)$ 未必等于 $(1-x)^{-1/2}$；因子 $M_n(\alpha)$ 是“$n$ 次乘子”。“度”的含义不清楚；下文将由迭代得到 $2^m$ 次的模方程与乘子；标准定义中“度”的含义是精确的。

迭代 (15.2) 得 4 次模方程：$\beta = \alpha^4/(\alpha^2-8\alpha+8)^2$。此法只在 $n$ 为 2 的正幂时给出模方程；但拉马努金断言，对任何正整数 $n$，$n$ 次模方程为

$$\beta = \frac{4\alpha^n}{\{(1+\sqrt{1-\alpha})^n + (1-\sqrt{1-\alpha})^n\}^2}. \tag{15.4}$$

拉马努金可能先对 $n = 2^m$ 用归纳法建立 (15.4)，再“插值”得到一般正整数 $n$ 的公式；$m = 0, 1, 2$ 时 (15.4) 与前面的计算一致；$n = 2^m$ 时 (15.4) 的归纳证明是直接的，只是繁琐，故略去。

(15.4) 对应的乘子 $M_n(\alpha)$ 如下：置 $P_n = (1+\sqrt{1-\alpha})^n + (1-\sqrt{1-\alpha})^n$ 与 $Q_n = \{(1+\sqrt{1-\alpha})^n - (1-\sqrt{1-\alpha})^n\}/\sqrt{1-\alpha}$（$n \ge 1$），则由 (15.3)(15.4) 经直接计算得

$$M_n(\alpha) = \frac{F(\alpha)}{F(\beta)} = \frac{(P_n^2-4\alpha^n)^{1/2}}{P_n(1-\alpha)^{1/2}} = \frac{Q_n}{P_n},$$

可见 $M_n(\alpha)$ 是 $\alpha$ 的有理函数。特别地，$n = 3$ 时 $M_3(\alpha) = (4-\alpha)/(4-3\alpha)$；拉马努金断言 $M_3(\alpha) = 1 + 2\sqrt{\beta/\alpha} = \sqrt{(1-\beta)/(1-\alpha)}$，两式都容易验证。

**推论。** 拉马努金断言：“若 2 次为 $\alpha^2 + 2\alpha = \beta$，则 $n$ 次为 $\beta = (\alpha+1)^n - 1$。”Berndt 注：我们看不出此断言与原函数 $F$ 有何联系；拉马努金似乎在断言 $2^m$ 次的“模方程”可由 2 次“模方程”经迭代得到；因 $\{(x+1)^k-1\}^2 + 2\{(x+1)^k-1\} = (x+1)^{2k}-1$（每个正整数 $k$），当 $n = 2^m$（$m \ge 0$）时他的断言容易建立；如前，拉马努金显然用了“插值”论证以对一般的 $n$ 建立推论；他在季报中用同类插值论证定义了函数的 $n$ 次迭代（$n$ 为任意实数），见 Part I [9, pp. 324–326, 328–329]。

### Entry 15(ii)

**陈述。**（逐字引自拉马努金）“若 $p$ 次与 $q$ 次为 $\varphi(x)$ 与 $\psi(x)$，$r$ 次为 $f(x)$，则若 $p$ 次与 $q$ 次为 $\varphi F(x)$ 与 $\psi F(x)$，则 $r$ 次为 $fF(x)$；又若 $p$ 次与 $q$ 次为 $F\varphi(x)$ 与 $F\psi(x)$，则 $r$ 次为 $Ff(x)$。”

**推论。**（逐字引自拉马努金）“于是我们可以在每个函数中或对每个函数给 $x$ 加减任意常数、乘除任意常数。”

Berndt 注：对此能说什么呢？拉马努金似乎只是在对函数的复合做一些初等评述。

对 $n = 2^m$（$m$ 为任意非负整数），定义 $F^{(n)}(x) = FF\cdots F(x)$（(15.5)，右端 $F$ 出现 $m$ 次）；特别地 $F^{(1)}(x) = x$。

**推论 (i)。** 若 $f^{(1)}(x) = x$ 且 $f^{(2)}(x) = x^2+4x$，则

$$f^{(n)}(x) = \left\{\left(\frac{\sqrt{x+4}+\sqrt{x}}{2}\right)^n - \left(\frac{\sqrt{x+4}-\sqrt{x}}{2}\right)^n\right\}^2.$$

**推论 (ii)。** 若 $f^{(1)}(x) = x$ 且 $f^{(2)}(x) = x^2-2$，则

$$f^{(n)}(x) = \left(\frac{x+\sqrt{x^2-4}}{2}\right)^n + \left(\frac{x-\sqrt{x^2-4}}{2}\right)^n.$$

如前，这两个推论是关于 $n = 2^m$ 时函数迭代的陈述；拉马努金大概假定他的公式由插值对所有正整数 $n$ 成立；两个推论的归纳证明都完全直接。

**我自验：** 推论 (i) 取 $n = 4$、$x = 3$：迭代 $f(f(3)) = 525$，公式右端 $525$，差 $2.0\times 10^{-28}$。

### Entry 15(iii)

**陈述。**（逐字引自拉马努金，p. 192）“若 $f(x)$ 与 $F(x)$ 为 $p$ 次与 $q$ 次，求 $\varphi(x)$ 使得

$$\sqrt[p]{\varphi f(x)} = \sqrt[q]{\varphi F(x)} = \chi(x), \tag{15.6}$$

假定如此，则 $r$ 次的函数 $= \varphi^{-1}\{\chi(x)\}^r$，自重复级数为 $\sqrt[n]{\varphi(x)/(\psi(x)\varphi'(x))}$，其中 $n$ 为任意量，$\psi(x)$ 为任意合适的函数。设级数为 $S(x)$，则有

$$\frac{SF(x)}{Sf(x)} = \sqrt[n]{\frac{p}{q}\cdot\frac{\psi f(x)}{\psi F(x)}\cdot\frac{F'(x)}{f'(x)}}. \tag{15.7}$$

Berndt 注：我们引述了拉马努金（p. 192）的 Entry 15(iii)，它确实非常费解；不能保证函数 $\varphi$ 存在；也不清楚什么是自重复级数。Berndt 在若干假定下给出证明：假定存在 $\varphi$ 使 (15.6) 成立；不失一般性设 $p = 1$，即 $f(x) = x$；再假定 $q$、$r$ 为 2 的非负幂且 $2 \le q \le 2r$；因 $F$ 为“$q$ 次”，置 $F(x) = G^{(q)}(x)$（$G^{(q)}$ 由 (15.5) 定义）。此时 (15.6) 取 $\varphi^q(x) = \varphi(F(x))$（(15.8)）的形式，需证 $G^{(r)}(x) = \varphi^{-1}(\varphi(x)^r)$（(15.9)）；对 $r$ 归纳（$r \to 2r$），用 (15.8)、归纳假设与 (15.5) 即得 (15.9)，此即 Entry 15(iii) 的第一断言。(15.7) 的证明则无需对 $p$、$q$ 作限制（除 $pq \ne 0$），只需 $f$、$F$、$\varphi$ 可微；用链式法则与 (15.6) 直接算出。

**状态：** Entry 15(ii) 的两个推论已证明（归纳法，$n = 2^m$ 情形；一般 $n$ 靠插值）；Entry 15(iii) 只有在 Berndt 的假定下才有证明，原文表述费解，$\varphi$ 的存在性与“自重复级数”的含义均不清楚。**对照：** M06（模方程先声）、M12、M02。

### 第 15 节例

**例。**（逐字引自拉马努金，p. 192）“若 $I = x$ 且 $II = x^2+2nx$，则若 $x$ 很大，

$$III = x^3 + 3nx^2 + \frac{3n(n+1)}{2}x - \frac{n(n-1)(n-2)x}{2x+3(n+1)/2}\ \text{近似}.” \tag{15.10}$$

Berndt 的解释：如上例，这应理解为函数迭代的例子；其一，第 15 节 (i) 的推论中第三个函数等于 $x^3+3x^2+3x$，与 (15.10) 取 $n = 1$ 时一致；其二，第 15 节 (ii) 的推论 (i) 给出 $f^{(3)}(x) = x^3+6x^2+9x$，与 (15.10) 取 $n = 2$ 时一致。按早先的评述，拉马努金大概先对 $r = 2^m$ 导出 $r$ 次迭代的表示，再把 $r$ 换成任意正整数；然后他显然对第三个函数导出了某种渐近公式并截断级数得到给出的近似。事实上，对 $r = 2^m$（$m \ge 0$），定义多项式序列 $P_1(x) = x$、$P_{2r}(x) = P_r^2(x) + 2nP_r(x)$；归纳可证对 $r = 2^m > 2$，

$$P_r(x) = x^r + rnx^{r-1} + \frac{1}{2}rn(1+(r-2)n)x^{r-2} + \frac{1}{2}r(r-2)n^2(1+n(r-4)/3)x^{r-3} + \cdots. \tag{15.11}$$

在 (15.11) 中插值取 $r = 3$ 得

$$P_3(x) = x^3 + 3nx^2 + \frac{3}{2}n(n+1)x + \frac{3}{2}n^2(1-n/3) + \cdots. \tag{15.12}$$

(15.12) 右端前三项与 (15.10) 一致；但 (15.10) 的最后一项在 $x \to \infty$ 时趋于 $-n(n-1)(n-2)/2$，与 (15.12) 的 $\frac{3}{2}n^2(1-n/3)$ 不同。Berndt 注：我们不知道如何求 (15.11) 中 $x^k$ 系数的一般闭式。

## Entry 16

**陈述。** 若 $n-1$ 次模方程为

$$\sqrt[n]{\alpha\beta} + \sqrt[n]{(1-\alpha)(1-\beta)} = 1,$$

则 $(n-1)^2$ 次模方程为

$$\{\sqrt[n]{\alpha(1-\beta)} - \sqrt[n]{\beta(1-\alpha)}\}^n = \{\sqrt[n]{\alpha} - \sqrt[n]{\beta}\}^n + \{\sqrt[n]{1-\beta} - \sqrt[n]{1-\alpha}\}^n.$$

**证明思路（自写）。** 为简便置 $A = \sqrt[n]{\alpha}$、$B = \sqrt[n]{\beta}$、$C = \sqrt[n]{\gamma}$、$a = \sqrt[n]{1-\alpha}$、$b = \sqrt[n]{1-\beta}$、$c = \sqrt[n]{1-\gamma}$。$\gamma$ 关于 $\alpha$ 的 $n-1$ 次模方程为 $AC + ac = 1$（(16.1)），$\beta$ 关于 $\gamma$ 的 $n-1$ 次模方程为 $BC + bc = 1$（(16.2)）；于是 $\beta$ 关于 $\alpha$ 为 $(n-1)^2$ 次；从 (16.1)(16.2) 消去 $\gamma$：(16.1) 减 (16.2) 得 $(A-B)/(b-a) = (1/\gamma-1)^{1/n}$，即 $\gamma = 1/(((A-B)/(b-a))^n+1)$；代入 (16.1)，两端乘 $\{(A-B)^n+(b-a)^n\}^{1/n}$ 并化简得 $Ab - aB = \{(A-B)^n+(b-a)^n\}^{1/n}$，即所求恒等式。

**状态：** 已证明。**对照：** M06（模方程）、M04。

**我自验与注记：** Entry 16 的假设是复合关系（$\gamma$ 对 $\alpha$ 为 $n-1$ 次、$\beta$ 对 $\gamma$ 为 $n-1$ 次），不是 $\alpha$、$\beta$ 直接满足 $n-1$ 次模方程；我初版误按后者检验，在 $n = 3$、$\alpha = 0.3$ 时得差 $0.0126$，属自验方法错误。按正确含义检验：$\alpha = 0.3$ 时由 $n-1$ 次方程解出 $\gamma = 0.00487925604888$，再由 $\gamma$ 解出 $\beta = 8.86548417972\times 10^{-7}$，结论两端 $0.288677730734$，差 $3.5\times 10^{-31}$；$\alpha = 0.6$ 时 $\gamma = 0.0333460673$、$\beta = 4.275937531\times 10^{-5}$，两端 $0.546652435714$，差 $9.9\times 10^{-32}$。

## 小结

- 本章 39 页正文（书页 300–338），是 Part II 的收官之章，也是五卷中话题最杂的一章：前七节为级数渐近展开（Entry 1–8 + Theorem 3.1、3.2、6.1、6.2、6.3、7.1），后半为模形式（Entry 10–14），末两节为 Ch. 19–21 模方程的先声（Entry 15、16）。
- 编号 Entry 15 条（Entry 1–8、10–16，**无 Entry 9**——第 9 节只有 $F_{m,n}$、$L$、$M$、$N$ 的定义与 Eisenstein 级数引入），Entry 标题 36 个；Berndt 的推广定理 6 条，明确标为 Theorem 而非 Entry。Entry 2、Entry 5、Entry 6 在书中只以特例关系记述，未单独印出公式；Entry 15 只编号 (ii)(iii)，第 15 节 (i) 的模方程材料未冠 Entry 之名。
- 亮点：Entry 8 的 (8.3)（修正 theta 函数的精确反演公式，章首点名最有趣的定理之一；两点数值复核差 $\le 3.6\times 10^{-18}$）；Entry 11 的互反公式（$\alpha = \beta = \pi$ 时差 $4.7\times 10^{-29}$）；Entry 12(x) 等价的 $\sigma$ 恒等式（$n = 0$–$6$ 精确整数复核成立）与 $\sum_{r,s}(n)$ 的 Levitt 1978 年定理；Entry 14 的 Eisenstein 级数新递推公式（$n = 6$ 时差 $7.9\times 10^{-31}$）；Entry 16 的模方程复合（两组参数差 $\le 3.5\times 10^{-31}$）。
- 拉马努金原文疏失（均按 Berndt 注明）：例 1 的 $F(h) = 2\pi/(e^{2\pi/h}-1)$ 有误、例 2 的 $10\sqrt{\pi}e^{-100\pi^2}$ 有误；§2 例 (iv) 致 Hardy 信中的 $I(n)$ 表述有误（Watson 指出）；Entry 7 的 $\sigma_{n-1}$ 应为 $\sigma_{n-m}$、第 7 节例又误写 $\sigma_{n-1}$ 且漏项 $-1/(1440x)$；Entry 10(ii) 的定义多处含糊（度、指标理论、例 3 的奇点阶、例 5 的度、例 6 的“双重”与度 $1/2$、例 7 的完备性均经 Berndt 订正或存疑）；Entry 14 在笔记 p. 191 中表述不完全；Riesel 把 Entry 3–5 当作精确公式而断言其不正确，实为误解（作为渐近公式正确）。
- 本轮数值复核约 25 项（直接求和，mpmath 30 位；慢收敛级数不用 `nsum`，见 Ch. 8–14 的教训）：Entry 1 例 1、Entry 3 及其推论、§3 例 (iv)、Entry 8 (8.3) 两点、Entry 11、Entry 12(i)(v)–(viii) 与 (x) 的 $n = 0$–$6$、Entry 13(i) 与例 (i)、Entry 14（$n = 6$）、Entry 7 (7.1)、Entry 15(ii) 推论 (i)、Entry 16 两组参数，全部通过；**本轮未发现新的原书印文问题**。另有两处自验方法错误的纠正记录：Entry 1 例 1 初算差 $5\times 10^{-4}$ 系截断尾项（$k > 20000$，约 $5\times 10^{-4}$），补尾项后一致；Entry 16 初版误按直接关系检验（见该条注记），按复合关系重验后通过。
- Part II 六章收官：Ch. 10：35 条、Ch. 11：36 条、Ch. 12：49 条、Ch. 13：35 条（Entry 1–11、13–36）、Ch. 14：25 条、Ch. 15：15 条（Entry 1–8、10–16），**编号 Entry 加总 195 条**；Entry 标题按各章文件所记加总 $44+56+59+45+57+36 = 297$ 个（Ch. 11 的标题数按 README 所记 56 计，该文件另注本地数得 54 个标题的计法差异）。

## 待核对清单

1. IMSC 本章结果数：imsc.res.in 2026-11-06 再次不可达（curl 返回 000），未能补录。
2. Berndt 章首计数：本章导言（pp. 300–301）未给出本章公式或定理陈述的总数。
3. TIFR 影印版页码：除笔记 p. 181（例 1 的 $F(h)$ 断言）、pp. 186–187（Entry 10(ii) 定义引文）、p. 191（Entry 14）、p. 192（Entry 15(iii) 与第 15 节例）外，各条在 TIFR 影印版中的对应页未逐条核对。
4. Entry 2 的确切表述：书中只记“Entry 2 是 Entry 3 的 $p = 1$ 特例”，未单独印出公式；本文件所写为由 Entry 3 代入 $p = 1$ 所得。
5. Entry 5、Entry 6 的确切表述：书中只记 Entry 5 为 Theorem 6.1 的 $n = q = 1$、$m \ne p$ 情形、其推论为 $m = p$ 情形，Entry 6 为 $m/p \ne n/q$ 情形、“N.B.”结果为 $m/p = n/q$ 情形，未单独印出公式；本文件所写为由 Theorem 6.1 代入所得。
6. 第 5 节的节编号：第 4 节末直接接 Theorem 6.1，书中未见独立的“第 5 节”节首；Entry 5、Entry 6 所在的第 5 节是否存在独立节首，待核对原文。
7. Entry 15(i) 的定位：第 15 节 (i) 为模方程材料（(15.1)–(15.4) 与推论），未冠“Entry 15(i)”之名；Entry 15 只编号 (ii)(iii)，此定位以原文为准。
8. §3 例 (i)(ii)(iii)(v) 的展开式：书中只记特例参数（推论取 $p = 2$；Entry 3 取 $p = 4$、$m = 2$；$p = 3$、$m = 2$；$m = 3$、$p = 6$），未逐项印出展开式；本文件所写的例 (ii)(iii) 展开式为由 Entry 3 直接代入。
9. §6 例 (i)(ii) 的展开式：书中只记特例参数（Theorem 6.2 取 $p = 2$、$n = q = 1$；Theorem 6.1 取 $m = 3$、$p = q = n = 1$），未逐项印出展开式；本文件所写的例 (ii) 主项 $2\zeta(3)/x^3 - 1/(12x)$ 为由 Theorem 6.1 直接代入。
10. §7 例（$m = 3$、$n = 5$）的完整展开式：书中未印出，只记拉马努金误写 $\sigma_{n-1}$ 且漏项 $-1/(1440x)$。
11. Entry 12(ii)(iii)(iv) 的 $E_8$、$E_{10}$、$E_{14}$ 未逐项数值复核（本轮只复核了 (i)(v)–(viii) 与 (x)）。
12. Entry 13 例 (ii)(iii)（$\Phi_{2,7}$、$\Phi_{3,6}$）未逐项数值复核（本轮只复核了 (i) 与例 (i)）。
13. Entry 12(x) 的初等证明仍未找到（Berndt 明言在文献中找不到、自己也未能给出）；$\sum_{r,s}(n)$ 的 Levitt 1978 年定理与 Grosjean 的系统研究只记结论，未展开。
14. “指标理论”的含义未知（Berndt 明言）；Entry 10(ii) 的“度”定义与 Ismail 的建议定义之间的关系未完全澄清。
15. Entry 10(i) 第二部分 $n = 1$ 的情形：拉马努金未考虑，Berndt 用 $\delta_1 = 1/2$ 补入；$n = 1$ 时 (10.1) 的证明细节（书中称“类似论证”）未展开。

## 来源说明

- 整理层：Bruce C. Berndt，《Ramanujan's Notebooks》，Part II，Springer，1989，Ch. 15，书页 300–338（正文）；参考文献自书页 339 起，索引在后。
- 电子版：archive.org 标识符 `ramanujan_notebooks_ii`（《Ramanujan's Notebooks, Part 2》，Springer 1989，XII + 360 页，DOI 10.1007/978-1-4612-4530-8；PDF 14,538,056 字节、372 叶），**PDF 页 = 书页 + 12**（与 Part I 的 +10 不同）。本章为 PDF 页 312–350（书页 300–338），PDF 页 351 起为参考文献与索引。
- 转录方法：全部公式按 PDF 原图（150 DPI，书页 300–338）逐字转录；关键公式 (8.3) 另用 300 DPI 放大图确认；OCR（DjVu 文本层）只作检索索引，公式凡与原图或数值不符者一律纠正。
- 文献指引：[11] 指拉马努金名篇“On certain arithmetical functions”（[16] 即 Hardy 等编《Collected Papers of Srinivasa Ramanujan》，pp. 136–162）；[16] 的页码均按 Berndt 书中所引；Rankin [2] 指《Modular Forms and Functions》；Titchmarsh [3] 指《The Theory of the Riemann Zeta-Function》；Apostol [3] 指《Modular Functions and Dirichlet Series in Number Theory》。
- 版权说明：本文件只收公式陈述与自写导读、证明思路与文献指引，未复制 Berndt 原文的正文与证明。
