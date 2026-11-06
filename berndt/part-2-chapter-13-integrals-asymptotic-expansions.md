# Part II，Chapter 13——Integrals and Asymptotic Expansions（积分与渐近展开）

出处：Bruce C. Berndt，《Ramanujan's Notebooks》，Part II，Springer，1989，Ch. 13，书页 185–239。

本章是 Berndt 五卷中积分与渐近展开的核心章：从发散积分的定义与分部积分出发，经 Hardy's 插值定理与 Mellin 变换的 Entry 5、JIMS 名题的推广 Entry 6、本章最难证的 Entry 7（双参数渐近）与 Entry 8，到 Entry 10 的级数渐近（Berndt 称「truly a remarkable theorem」，文献中无同类结果），收束于 Poisson 求和与 Euler–Maclaurin 的 Entry 31–32、36。本章共 **35 条 Entry（Entry 1–11、13–36；无 Entry 12——第 12 节只有例题，见下）**，另含分体 Entry 11(i)(ii)(iii)、18(i)(ii)、24(i)(ii)(iii)、25(i)(ii)、26(i)(ii)、29(i)(ii)、30(i)(ii)、31(i)(ii)、32(i)(ii)、33(i)(ii)、34(i)(ii)，共 **45 个 Entry 标题**。

## 背景与记号

- 章首导言（pp. 185–186）：Hardy 评拉马努金的积分公式「on the whole … seemed the least impressive」（总体上最不起眼），后又补「are still interesting and will repay a careful analysis」（仍有意思、值得细究）；Berndt 指出：若与级数、连分数的钻石光芒相比，积分只是红宝石稍逊——其中仍有许多优美而重要的积分以拉马努金命名（例如 Entry 22）。本章许多积分出自拉马努金论文 [8]（Collected Papers [16]，pp. 53–58）；更重要的是若干「absolutely remarkable results not heretofore observed」（此前未被注意到的绝对非凡的结果）。
- 章首点名的亮点：**Entry 6**（某积分的渐近展开，推广了拉马努金向 Journal of the Indian Mathematical Society 提交的名题 [4]，[16]，pp. 323，324；该题及相关展开见 Ch. 12 末尾 Entry 48）；**Entry 7**（本章 highlight，双参数趋向无穷时某积分的渐近展开，理论与计算两方面都极难证；其副产品是超几何函数 ${}_2F_1(1,m;m-n;(m-n)/m)$ 的渐近展开，文献中此前未见）；**Entry 8**（优美的积分渐近，与合流超几何函数 $\Phi(a,c;z)$、$\Psi(a,c;z)$ 相关；推广见第 10 节 (10.22)）；**Entry 5**（非常特殊的积分公式，根在拉马努金最喜爱的插值定理，即 Ch. 4 Entry 11；特例给出 $K$-Bessel 与合流超几何函数公式）；**Entry 10**（级数渐近，Berndt 称 extraordinarily beautiful，文献中无同类结果；推论 (i) 的特例与 Entry 8 相关）。
- 拉马努金的积分求值与渐近展开均不附带成立条件；尤其 Entry 5、7、10 的条件确定殊非易事。Evans 的论文 [1] 讨论了其中若干渐近展开并给出推广。许多求值是经典结果，原始发现者难以考证，书中通常只指明其在 Gradshteyn 与 Ryzhik 表 [1] 中的出处。
- 渐近记号约定（p. 186）：$f(x) \sim g(x)h\left(a_0 + \frac{a_1}{x} + \frac{a_2}{x^2} + \cdots\right)$ 意指 $f(x) = g(x)h(F(x))$，其中 $F(x)$ 有渐近展开 $F(x) \sim a_0 + \frac{a_1}{x} + \frac{a_2}{x^2} + \cdots$（$x \to \infty$）。
- 求和号上的撇号（p. 233，Entry 31 前）：$\sum_{a \le k \le b}' f(k)$ 表示若 $a$ 或 $b$ 为整数，则端点项只计 $\frac{1}{2}f(a)$ 或 $\frac{1}{2}f(b)$。
- 本章与已填章节的互见：Entry 5 的根是 **Part I Ch. 4 Entry 11**（拉马努金主定理，Hardy 称其为拉马努金最喜爱的公式之一）；Entry 11(i)(ii) 与第 12 节例题的证明用 **Part I Ch. 3 Entry 10** 的一般渐近公式 (11.1)；Entry 6 的 $h = 0$ 情形与 Entry 10 推论 (i) 的 $n = 1$ 情形见 **Part II Ch. 12 Entry 48**；Entry 7 的证明用 **Part II Ch. 11 (36.8)** 的 Lagrange 反演公式；Entry 25 例 (i) 用 **Part I Ch. 8 Entry 15** 的 $\psi(x+1) - \mathrm{Log}\,a = 0$ 的根的渐近；Entry 24(iii) 的同类实例见 **Part II Ch. 14 Entry 5(i)(ii)、Entry 16(i)(ii)**；Euler–Maclaurin 公式是 **Part I Ch. 6–8** 与本章第 10 节、第 32 节的焦点，Ch. 15 将继续。
- 与主题模块的对照总览：积分主线见 **M09**（拉马努金主定理、Gamma 积分、Fourier 积分）；渐近展开见 **M12**（Stirling 展开、Watson 引理、Euler–Maclaurin）；Gamma 函数见 **M10**（Entry 1 推论、Entry 14、15、22、23、25、35）；级数见 **M02**（Entry 2、11、17、18、24、27、28、31、32、36）；Bernoulli 数与 Euler 数见 **M01**（Entry 10 的 Euler–Maclaurin、Entry 16(iv)、Entry 36）——另注：M01 目前缺少 Bernoulli 数的定义（M02、M06 引用它并写「见 M01.3」，但 M01 全文未给定义；出处已在 Part I Ch. 5 Entry 9 定位，待日后补入 M01），本章 Entry 16(iv) 与 Entry 36 均用 Bernoulli 数 $B_k$ 与 Euler 数 $E_k$，不在本章文件里顺手改 M01；合流超几何与 Bessel 函数见 **M07**（Entry 6、7、8、Entry 10 推论 (ii) 的 $I_0$）；Poisson 求和与模形式氛围见 **M06**（Entry 21 例、Entry 35 的 $\alpha\beta = \pi$）。

## 本章结构

| Entry | 主题 | 书页 |
|---|---|---|
| Entry 1 | 发散积分的定义（Ramanujan 定义）与例 (1.1)、推论 | 186–187 |
| Entry 2 | 分部积分三式 (i)(ii)(iii) | 188 |
| Entry 3 | $\int_x^\infty e^{-t^2}\cos(2nt)\,dt$ 的渐近展开 | 188–189 |
| Entry 4 | 高斯核的平移恒等式与级数 | 189–190 |
| Entry 5 | Hardy 插值定理的积分形式（Mellin 变换） | 190–192 |
| Entry 6 | $\int_0^\infty e^{-x}(1+x/n)^{n-h}\,dx$ 的渐近展开（JIMS 名题推广） | 193–195 |
| Entry 7 | 双参数积分 $I(m,n)$ 的渐近展开（本章 highlight） | 195–202 |
| Entry 8 | $\int_0^\infty \{n^x\Gamma(n+1)/\Gamma(n+x+1) + e^{-x}(1+x/n)^n\}\,dx$ 的渐近 | 202–205 |
| Entry 9 | $\varphi(m) = \int_0^\infty e^{-m^2x^2}/(1+x^2)\,dx$ 的余弦积分 | 205–207 |
| Entry 10 | 级数的渐近展开（超几何型级数）与推论 (i)(ii) | 207–214 |
| Entry 11(i) | $\sum (ex/k)^k$ 的渐近展开 | 215–216 |
| Entry 11(ii) | $I_n = \int_0^\infty x^{n-1}/\sum (x/k)^k\,dx$ 的渐近展开 | 216–217 |
| Entry 11(iii) | $S = 1$（对数级数恒等式，JIMS 投稿题） | 217 |
| 第 12 节（无 Entry 12） | 例题：$\sum \mathrm{Log}(k+1)x^k/k!$ 的渐近展开 | 217–218 |
| Entry 13 | 四因子有理积分 (13.1) 与推论 (13.2) | 219 |
| Entry 14 | $\sum (-1)^k(2a)_k(a+k)/(k!\{(a+k)^2+x^2\})$ 的求值 | 219–220 |
| Entry 15 | $\int_0^\infty \|\Gamma(a+ix)\|^2\cos(2nx)\,dx$ | 220 |
| Entry 16 | 四组经典积分 (i)–(iv)（Bernoulli 数、Euler 数） | 220 |
| Entry 17 | Abel–Plana 求和公式与 $\mathrm{Log}\,n!$ 推论 | 220–221 |
| Entry 18(i) | Abel–Plana 的差分形式 | 221 |
| Entry 18(ii) | 偶数情形的 Abel–Plana 型引理与公式 | 222 |
| Entry 19 | Fourier 积分定理 (i)(ii) 与 $\mathrm{sech}^{2a}$ 推论 | 223 |
| Entry 20 | $\int_0^\infty \sinh(ax)/\sinh(\pi x) \cdot dx/(1+n^2x^2)$ | 224 |
| Entry 21 | 积分次序交换恒等式与余弦变换的 Parseval 定理 | 224–225 |
| Entry 22 | 最著名的 Gamma 乘积积分 (i)(ii) | 225–226 |
| Entry 23 | $\int_0^\infty x^{-m}\Gamma(x+a)/\Gamma(x+a+n+1)\,dx$ | 226 |
| Entry 24(i) | 平凡恒等式 $\sum_{k=0}^n A_k = \sum_{k=0}^\infty A_{n-k} - \sum_{k=1}^\infty A_{-k}$ | 226 |
| Entry 24(ii) | 极限等式（意图不明）与已否定的推论 | 226 |
| Entry 24(iii) | $\int_{-\infty}^\infty \varphi(x)/\Gamma(x+1)\,dx = \sum \varphi(n)/\Gamma(n+1)$（一般不成立） | 226–227 |
| Entry 25(i) | Entry 25(ii) 的 $b = 0$ 特例 | 227 |
| Entry 25(ii) | $A_n$、$B_n$ 的形式公式（积分发散）与例 (i)(ii) | 227–228 |
| Entry 26(i) | $\int_0^\infty \cos(2nx)/(1+x^2)^{m+1}\,dx$ 的闭式 | 229 |
| Entry 26(ii) | $I(m,n) = \int_0^\infty x^{2m}\cos(px)/(1+x^2)^{n+1}\,dx$ | 229–230 |
| Entry 27 | 无穷乘积 $\prod_{k=1}^\infty \{1+(x/k)^n\}^2$（$n$ 偶）与推论 (i)(ii) | 230–231 |
| Entry 28 | $mn\sum x^{nk}/(nk)!$ 的三角和表示 | 231 |
| Entry 29(i)(ii) | $\int_0^\infty (-x^2)^l/(1+x^{2n})\cos(px)\,dx$（$n$ 奇/偶） | 231–232 |
| Entry 30(i) | $\int_0^\infty \sin^{2n+1}x/x\,dx = \int_0^\infty \sin^{2n+2}x/x^2\,dx$ | 232 |
| Entry 30(ii) | $\varphi(n,p) = \int_0^\infty \sin^n x/x^p\,dx$ 的递推与推论 (i)(ii) | 232–233 |
| Entry 31(i) | Poisson 求和 (31.1) | 233–234 |
| Entry 31(ii) | $\int_0^h \sin(nx)/\sin x \cdot \varphi(x)\,dx$ (31.3) | 234 |
| Entry 32(i) | Poisson 求和的正弦版本 | 235 |
| Entry 32(ii) | Euler–Maclaurin 求和公式的另一版本（仅一句话） | 235–236 |
| Entry 33(i)(ii) | $\int_0^\infty \{(-x^2)^l/(1-x^{2n}) + (-1)^l/(n(x^2-1))\}\cos(px)\,dx$ | 236–237 |
| Entry 34(i)(ii) | $\pi\cos(\theta x)/(x\sin\pi x)$ 与 $\pi\sin(\theta x)/(4x\cos\frac{1}{2}\pi x)$ 的部分分式 | 237–238 |
| Entry 35 | $\sqrt{\alpha}\{1 + 2\sum 1/(1+\alpha^2k^2)^{n+1}\}$ 的 Poisson 型恒等式 | 238 |
| Entry 36 | $m\sum' 1/(m^2+(n+k)^2)$ 的渐近展开（Bernoulli 数）与推论 | 238–239 |

## Entry 1——发散积分的定义

设 $n \ge 0$，置 $N = [n+1]$（取整部分）。则

$$\int_0^\infty x^{-n-1} \sum_{k=0}^\infty A_k(-x)^k\,dx = (-1)^N \int_0^\infty x^{-n+N-1} \sum_{k=0}^\infty A_{N+k}(-x)^k\,dx,$$

只要右端有意义。

**状态：定义，非定理。**拉马努金并不把 Entry 1 当作定理，而是用右端表达式来**定义**左端的积分。Berndt 用 Cauchy–Saalschütz 公式

$$\Gamma(z) = \int_0^\infty t^{z-1}\left(e^{-t} - \sum_{k=0}^n \frac{(-t)^k}{k!}\right)dt \tag{1.2}$$

（其中整数 $n$ 使 $-n-1 < \mathrm{Re}(z) < -n$）论证该定义的合理性。例：

$$\int_0^\infty \frac{e^{-x^2}}{x^4}\,dx = \frac{2}{3}\sqrt{\pi},$$

理解为 $\int_0^\infty (e^{-x^2}-1+x^2)/x^4\,dx = \frac{2}{3}\sqrt{\pi}$（(1.1)，数值复核：直接求和在 $x=0$ 处用 Taylor 展开 $1/2 - x^2/6 + \cdots$ 去奇点后得 $1.1816359006$，与 $\frac{2}{3}\sqrt{\pi}$ 一致到 15 位）。

**推论。**若 $a, n > 0$，$b$ 为实数，则

$$\int_0^\infty e^{-ax}x^{n-1}\begin{matrix}\cos(bx) \\ \sin(bx)\end{matrix}dx = \frac{\Gamma(n)}{(a^2+b^2)^{n/2}}\begin{matrix}\cos(n\tan^{-1}(b/a)) \\ \sin(n\tan^{-1}(b/a))\end{matrix}.$$

这两式是熟知的（Gradshteyn 与 Ryzhik [1]，p. 490）。拉马努金还注：上述积分「对 $n$ 的负值也是知道的」——Entry 1 的定义恰为负 $n$（非负整数除外）赋予这些积分以意义，且同公式仍成立。

**对照：** M09（Gamma 积分）、M10（Gamma 函数）、M12（发散级数的 Ramanujan 求和，见 Part I Ch. 6 Entry 1 的常数 $c$）。

## Entry 2——分部积分三式

设 $\varphi$ 有 $m+1$ 阶连续导数。则

(i) $\displaystyle \int \varphi(x)e^{-nx}\,dx = -e^{-nx}\sum_{k=0}^m \frac{\varphi^{(k)}(x)}{n^{k+1}} + \frac{1}{n^{m+1}}\int \varphi^{(m+1)}(x)e^{-nx}\,dx$；

(ii) $\displaystyle \int \varphi(x)\cos(nx)\,dx$：$m$ 为偶数时 $= \sin(nx)\sum_{k=0}^{m/2} \frac{(-1)^k\varphi^{(2k)}(x)}{n^{2k+1}} + \cos(nx)\sum_{k=0}^{m/2-1} \frac{(-1)^k\varphi^{(2k+1)}(x)}{n^{2k+2}} + \frac{(-1)^{m/2+1}}{n^{m+1}}\int \varphi^{(m+1)}(x)\sin(nx)\,dx$；$m$ 为奇数时 $= \sin(nx)\sum_{k=0}^{(m-1)/2} \frac{(-1)^k\varphi^{(2k)}(x)}{n^{2k+1}} + \cos(nx)\sum_{k=0}^{(m-1)/2} \frac{(-1)^k\varphi^{(2k+1)}(x)}{n^{2k+2}} + \frac{(-1)^{(m+1)/2}}{n^{m+1}}\int \varphi^{(m+1)}(x)\cos(nx)\,dx$；

(iii) $\displaystyle \int \varphi(x)\sin(nx)\,dx$：$m$ 为偶数时 $= \sin(nx)\sum_{k=0}^{m/2-1} \frac{(-1)^k\varphi^{(2k+1)}(x)}{n^{2k+2}} - \cos(nx)\sum_{k=0}^{m/2} \frac{(-1)^k\varphi^{(2k)}(x)}{n^{2k+1}} + \frac{(-1)^{m/2}}{n^{m+1}}\int \varphi^{(m+1)}(x)\cos(nx)\,dx$；$m$ 为奇数时 $= \sin(nx)\sum_{k=0}^{(m-1)/2} \frac{(-1)^k\varphi^{(2k+1)}(x)}{n^{2k+2}} - \cos(nx)\sum_{k=0}^{(m-1)/2} \frac{(-1)^k\varphi^{(2k)}(x)}{n^{2k+1}} + \frac{(-1)^{(m+1)/2}}{n^{m+1}}\int \varphi^{(m+1)}(x)\sin(nx)\,dx$。

**状态：已证明。**以上各式均可由逐次分部积分得到（书中未印积分上下限，按分部积分的不定积分形式理解；定积分版本见待核对清单）。

**对照：** M09（分部积分）、M02（渐近展开的工具，Entry 3 即其应用）。

## Entry 3——$\int_x^\infty e^{-t^2}\cos(2nt)\,dt$ 的渐近展开

设 $n, x > 0$，$\theta = \tan^{-1}(n/x)$，$r = (n^2+x^2)^{1/2}$。设 $m$ 为任意正整数。则当 $x \to \infty$ 时，

$$\int_x^\infty e^{-t^2}\cos(2nt)\,dt = \frac{e^{-x^2}}{2}\sum_{k=0}^{m-1} \frac{(-1)^k(\frac{1}{2})_k\cos(2nx+(2k+1)\theta)}{r^{2k+1}} + O(r^{-2m-1}).$$

**状态：已证明**（逐次分部积分）。数值复核：$n=1$、$x=2$、$m=3$ 时左端与右端差 $3.3\times 10^{-5}$，在余项 $O(r^{-7})$ 量级内。

**对照：** M12（渐近展开）、M09（误差函数型积分）。

## Entry 4——高斯核的平移恒等式

设 $\varphi$ 为整函数，$n$ 为实数，且以下积分与级数均收敛。则

$$\int_0^\infty e^{-x^2}\{e^{2nx}\varphi(x) + e^{-2nx}\varphi(-x)\}\,dx = \int_0^\infty e^{n^2-x^2}\{\varphi(n+x) + \varphi(n-x)\}\,dx = \sqrt{\pi}e^{n^2}\sum_{k=0}^\infty \frac{\varphi^{(2k)}(n)}{2^{2k}k!}.$$

例：取 $\varphi(x) = e^x$，得

$$\int_0^\infty e^{-x^2}\cosh((2n+1)x)\,dx = \int_0^\infty e^{n^2+n-x^2}\cosh x\,dx = \frac{\sqrt{\pi}e^{n^2+n+1/4}}{2}$$

（数值复核：$n=1$ 时两端差 $0$，30 位精度）。

**状态：已证明**（配方法换元 + Taylor 展开逐项积分，引用 Titchmarsh 书中的求和积分交换定理）。

**对照：** M09（高斯积分）、M10（Gamma 函数的矩）。

## Entry 5——Hardy 插值定理的积分形式

先述 Hardy 定理（Hardy [9]，p. 186，公式 (A)；亦见 Part I [9]，p. 299）：设 $s = \sigma + it$，$H(\delta) = \{s: \sigma \ge -\delta\}$（$0 < \delta < 1$），$\psi(s)$ 在 $H(\delta)$ 上解析，且存在常数 $C$、$P$、$A$（$A < \pi$）使 $|\psi(s)| \le Ce^{P\sigma + A|t|}$（(5.1)）。对 $x > 0$、$0 < c < \delta$，定义

$$\Psi(x) = \frac{1}{2\pi i}\int_{c-i\infty}^{c+i\infty} \frac{\pi}{\sin(\pi s)}\psi(-s)x^{-s}\,ds. \tag{5.2}$$

则当 $0 < x < e^{-P}$ 时 $\Psi(x) = \sum_{k=0}^\infty \psi(k)(-x)^k$；当 $0 < \sigma < \delta$ 时 $\int_0^\infty \Psi(x)x^{s-1}\,dx = \frac{\pi}{\sin(\pi s)}\psi(-s)$（(5.3)）。

**Entry 5。**设 $\psi(s)$ 对某个 $\delta > \frac{1}{2}$ 满足 Hardy 定理的假设。置 $\psi(s) = A_{2s+1}/\Gamma(s+1)$，于是按上述记号 $\Psi(x) = \sum_{k=0}^\infty A_{2k+1}(-x)^k/k!$（$0 < x < e^{-P}$）。设对 $a = 2\delta > 1$，$x^{a-1/2}\Psi(x^2) \in L^2(0,\infty)$。则

$$\int_0^\infty e^{-1/x^2}\Psi(x^2)\,dx = \frac{\sqrt{\pi}}{2}\sum_{k=0}^\infty \frac{(-2)^k A_k}{k!}.$$

拉马努金（p. 156）把 Entry 5 写成

$$\int_0^\infty e^{-1/x^2}\sum_{k=0}^\infty \frac{(-1)^k A_{2k+1}x^{2k}}{k!}\,dx = \frac{\sqrt{\pi}}{2}\sum_{k=0}^\infty \frac{(-2)^k A_k}{k!}.$$

**状态：已证明**（Mellin 变换的 Parseval 定理 + 留数定理；(5.4)–(5.9)）。注：Berndt 还给出另一形式论证：把 $\exp(-1/x^2)$ 展成幂级数、交换求和积分次序并套用拉马努金最喜爱的定理（Ch. 4 Entry 11），会得到「错误」的答案——奇数下标项不出现；拉马努金在许多类似场合用过同类论证，凭直觉判断何时得出正确公式、何时出错。

例 1（Gradshteyn 与 Ryzhik [1]，p. 307）：$\int_0^\infty e^{-x^2-1/x^2}\,dx = \frac{\sqrt{\pi}}{2}e^{-2}$（数值复核：差 $0$）。例 2：取 $\Psi(x) = (1+x)^{-\mu}$（$\mu > \frac{1}{2}$），则 $A_s = \Gamma(\mu+\frac{1}{2}s-\frac{1}{2})/\Gamma(\mu)$，应用 Entry 5 得 $\int_0^\infty e^{-1/x^2}(1+x^2)^{-\mu}\,dx = \frac{\Gamma(\mu-\frac{1}{2})}{2}\Psi(\mu-\frac{1}{2},\frac{1}{2};1)$，其中 $\Psi(a,c;z)$ 为合流超几何函数。

**对照：** M09（Mellin 变换、积分变换）、M07（合流超几何函数）、M10（Gamma 函数）；与 Part I Ch. 4 Entry 11（拉马努金主定理）互见。

## Entry 6——$\int_0^\infty e^{-x}(1+x/n)^{n-h}\,dx$ 的渐近展开

设 $n > 0$，$m$ 为正整数。则

$$\int_0^\infty e^{-x}\left(1+\frac{x}{n}\right)^{n-h}dx = \sum_{k=0}^{m-1} \frac{(-1)^k(-n+h)_k}{n^k} + \frac{(-1)^m(-n+h)_m}{n^m}\int_0^\infty e^{-x}\left(1+\frac{x}{n}\right)^{n-h-m}dx$$

$$= \frac{e^n\Gamma(n-h+1)}{2n^{n-h}} + A_0 - \frac{A_1}{n} + \frac{A_2}{n^2} + \cdots,$$

当 $n \to \infty$ 时，其中

$$A_0 = \frac{2}{3}-h, \quad A_1 = \frac{4}{135} - \frac{h^2(1-h)}{3}, \quad A_2 = \frac{8}{2835} + \frac{2h(1-h)}{135} - \frac{h(1-h^2)(2-3h^2)}{45}.$$

注：第一个积分等于 $n\Psi(1,n+2-h;n)$（Lebedev [1]，p. 268，公式 (9.11.6)），其中 $\Psi(a,c;z)$ 为合流超几何函数。$h = 0$ 的情形本质上就是拉马努金 [4]（[16]，pp. 323，324）向 Journal of the Indian Mathematical Society 提交的名题；亦见 Ch. 12 Entry 48 的 $h = 0$ 情形。Watson [3] 对该渐近展开有更细致的研究，Berndt 的证明用了他的部分分析。

**状态：已证明。**数值复核：$n=10$ 时，$h=0$ 与 $h=1$ 两情形左端积分与右端前三项之差均为 $1.8\times 10^{-6}$（在 $O(n^{-3})$ 量级内）；$A_2$ 的展开式与证明中 (6.1) 的系数逐项一致（已手工核对）。

**对照：** M12（渐近展开、Watson 引理）、M07（合流超几何函数 $\Psi$）；与 Part II Ch. 12 Entry 48 互见。

## Entry 7——双参数积分 $I(m,n)$ 的渐近展开

设 $m > n+1$。若 $m$ 与 $n$ 趋向 $\infty$ 而 $m-n$ 保持有界，则

$$I := I(m,n) := (m-n-1)\int_0^\infty \frac{(1+x/n)^n}{(1+x/m)^m}\,dx = n\sum_{k=0}^\infty \frac{(m-n)^k}{(m-n)_k} + O(1). \tag{7.1}$$

置 $R = n(m-n)/(2m)$（(7.2)）。若 $m$、$n$ 与 $m-n$ 均趋向 $\infty$（从而 $R \to \infty$），则有渐近展开

$$I = \frac{m^{m+1}\Gamma(n+1)\Gamma(m-n+1)}{2n^n\Gamma(m+1)(m-n)^{m-n}} + A_1 + A_2 + A_3 + A_4 + \cdots, \tag{7.3}$$

其中 $A_k$（$1 \le k < \infty$）为 $m$、$n$ 的有理函数，且 $A_k = O(mR^{1-k})$（(7.4)）。进而

$$A_1 = \frac{2(m+n)}{3}, \tag{7.5}$$
$$A_2 = -\frac{4(m+n)(m-2n)(m-\frac{1}{2}n)}{135mn(m-n)}, \tag{7.6}$$
$$A_3 = \frac{8(m^3+n^3)(m-2n)(m-\frac{1}{2}n)}{2835m^2n^2(m-n)^2}, \tag{7.7}$$
$$A_4 = \frac{16(m^3+n^3)(m-2n)(m-\frac{1}{2}n)(m^2-mn+n^2)}{8505m^3n^3(m-n)^3}. \tag{7.8}$$

另有 $I = n\,{}_2F_1(1,m;m-n;(m-n)/m)$（(7.10)）。结合 (7.3) 与 Stirling 公式，可得 ${}_2F_1(1,m;m-n;(m-n)/m)$（$m$、$n$、$m-n \to \infty$）的渐近展开；Evans [1] 的定理 15–17 讨论了该 ${}_2F_1$ 在一般 $m > n > 0$、$m \to \infty$ 时的渐近行为，但本展开在文献中似未曾出现。

**状态：已证明**（Berndt 的证明；拉马努金通常不给假设，且只给出展开 (7.3)，(7.1) 不见于笔记；$A_3$、$A_4$ 的计算极繁，Berndt 注拉马努金必有更自然的证法使系数 $A_k$ 更自然地出现）。数值复核：(7.1) 的 $O(1)$ 项在 $m-n=2$ 固定时随 $m$、$n$ 增大保持有界（$m=12$、$52$、$102$ 时差分别为 $3.128$、$3.180$、$3.187$）；(7.3) 在 $m=300$、$n=100$ 时 $I - S = 266.6173392$，$A_1+A_2+A_3+A_4 = 266.6173392$，差 $1.6\times 10^{-9}$（$A_5$ 量级 $mR^{-4} \approx 2.4\times 10^{-4}$ 的界内）；$A_1$、$A_2$ 另由 (7.39) 与 $a_2$、$a_4$ 的值手工复核一致。

**对照：** M12（双参数渐近展开）、M07（超几何函数 ${}_2F_1$）；证明用 Ch. 11 (36.8) 的 Lagrange 反演公式。

## Entry 8——$\int_0^\infty \{n^x\Gamma(n+1)/\Gamma(n+x+1) + e^{-x}(1+x/n)^n\}\,dx$ 的渐近

当 $n \to \infty$ 时，

$$\int_0^\infty \left\{\frac{n^x\Gamma(n+1)}{\Gamma(n+x+1)} + e^{-x}\left(1+\frac{x}{n}\right)^n\right\}dx = \frac{e^n\Gamma(n+1)}{n^n} + \frac{6n}{12n+1} + O(n^{-3/2}).$$

改写为 (8.1)：$\int_0^\infty n^x\Gamma(n+1)/\Gamma(n+x+1)\,dx - \sum_{k=0}^\infty n^k\Gamma(n+1)/\Gamma(n+k+1) = -\frac{6n+1}{12n+1} + O(n^{-3/2})$。联系：$n\Psi(1,n+2;n) = \int_0^\infty e^{-x}(1+x/n)^n\,dx$，且 $n\Psi(1,n+2;n) = -\sum_{k=0}^\infty n^k\Gamma(n+1)/\Gamma(n+k+1) + e^n\Gamma(n+1)/n^n + 1$（Lebedev [1]，p. 263，Eq. (9.10.3) 与 $\Phi$ 的定义）。推广见第 10 节 (10.22)。

**状态：已证明**（Stirling 公式 + Watson 引理）。数值复核：$n=10$ 时左端与右端差 $2.6\times 10^{-6}$（在 $O(n^{-3/2}) \approx 0.03$ 的界内，实际余项更小）。

**对照：** M12（渐近展开）、M07（合流超几何函数 $\Phi$、$\Psi$）、M10（Gamma 函数）。

## Entry 9——$\varphi(m)$ 的余弦积分

设 $\varphi(m) = \int_0^\infty e^{-m^2x^2}/(1+x^2)\,dx$。若 $|m| \ge |n|$（$m$、$n$ 为实数），则

$$\int_0^\infty \frac{e^{-m^2x^2}}{1+x^2}\cos(2mnx)\,dx = \frac{e^{-n^2}}{2}\{\varphi(m+n) + \varphi(m-n)\}. \tag{9.1}$$

若 $|n| > |m|$，则有类似式

$$\int_0^\infty \frac{e^{-m^2x^2}}{1+x^2}\cos(2mnx)\,dx = \frac{1}{2}e^{-n^2}\{\varphi(m+n) - \varphi(m-n)\} + \frac{1}{2}\pi e^{m^2-2mn}. \tag{9.6}$$

**状态：已证明**（围道积分；(9.1) 在 $n=0$ 时平凡；另一证明可用 Binet 的结果（Burkhardt [1]，p. 1154）与 Nielsen 书 [2]，pp. 18，19，Eqs. (5)，(13)，或 Parseval 定理）。数值复核：$m=2$、$n=1$ 时 (9.1) 两端差 $2.5\times 10^{-32}$。

**对照：** M09（Fourier 余弦积分）、M10（误差函数型积分 $\varphi$）。

## Entry 10——级数的渐近展开

设 $\alpha$、$\beta$、$\gamma$、$\delta$ 为固定实数，$\gamma > \delta \ge 0$。设对某个固定 $d > 0$，$\varphi(x)$ 在圆盘 $|x| \le d$ 内解析且非零；$\varphi(x)$ 与 $\varphi'(x)$ 在 $x \ge -d$ 时为正；存在常数 $M > 0$ 使 $x\varphi'(x) \ge M\varphi(x)$（(10.1)）对所有 $x \ge d$ 成立。设 $h > 0$。则当 $h \to 0$ 时，

$$S = S(h) := \sum_{k=0}^\infty \prod_{j=1}^k \frac{\varphi(h\alpha+hj\delta)}{\varphi(h\beta+hj\gamma)}$$

$$= \sqrt{\frac{\pi\varphi(0)}{2h(\gamma-\delta)\varphi'(0)}} + \frac{1}{3}\frac{\gamma+\delta}{\gamma-\delta}\left\{1 - \frac{\varphi(0)\varphi''(0)}{\varphi'(0)^2}\right\} + \frac{\alpha-\beta}{\gamma-\delta} + O(\sqrt{h}). \tag{10.2}$$

满足 Entry 10 的两个函数是 $e^x$ 与 $(1+x)^n$（$n > 0$，见下推论 (i)）。若 $\varphi$ 满足 Entry 10，则 $e^\varphi$ 与 $\varphi^c$（$c > 0$）亦然；$\varphi_1$、$\varphi_2$ 满足时 $\varphi_1\varphi_2$ 亦然。Berndt 称 Entry 10 是真正非凡的定理，文献中似无同类结果；其形式令人想起驻相法与积分的其他渐近估计中出现的渐近公式。

**推论 (i)。**设 $n > 0$。则当 $x \to \infty$ 时，

$$\sum_{k=0}^\infty \left\{\frac{x^k\Gamma(x+1)}{\Gamma(x+k+1)}\right\}^n = \sqrt{\frac{\pi x}{2n}} + \frac{1}{3n} + O(x^{-1/2}).$$

$n=1$ 时有更精确版（结合 (8.1) 与 (8.10)）：$\sum_{k=0}^\infty x^k\Gamma(x+1)/\Gamma(x+k+1) = \sqrt{\pi x/2} + 1/3 + \frac{1}{24}\sqrt{2\pi/x} + 4/(135x) + O(x^{-3/2})$。另有无穷渐近展开 (10.21)：$\sum_{k=0}^\infty f(k) - \int_0^\infty f(u)\,du \sim \frac{1}{2} - \sum_{k=1}^\infty \frac{B_{2k}}{(2k)!}f^{(2k-1)}(0)$（其中 $f(u) = (x^u\Gamma(x+1)/\Gamma(x+u+1))^n$）。作为 (10.21) 的应用，(10.22)：$\sum_{k=0}^\infty \{x^k\Gamma(x+1)/\Gamma(x+k+1)\}^n - \int_0^\infty \{x^t\Gamma(x+1)/\Gamma(x+t+1)\}^n dt = \frac{1}{2} + \frac{n}{24x} + O(x^{-2})$（$n > 0$，$x \to \infty$）；(10.22) 推广了 Entry 8（$n=1$ 时即 (8.1)）。

**推论 (ii)。**若 $n$ 为正整数，则当 $x \to \infty$ 时，

$$\sum_{k=0}^\infty \left(\frac{x^k}{k!}\right)^n \sim \frac{\exp\left\{nx + \frac{n^2-1}{24}\left(\frac{1}{nx} + \frac{1}{2n^2x^2} + \cdots\right)\right\}}{\sqrt{n(2\pi x)^{(n-1)/2}}}. \tag{10.23}$$

注：指数中的和看似 $-\mathrm{Log}(1-1/(nx))$，但那样会得到精确公式而非渐近公式，对 $n > 1$ 显然不可能。$n=1$ 时 (10.23) 平凡；$n=2$ 时左端为 $I_0(2x)$（零阶虚宗量 Bessel 函数），前三项 $e^{2x}/(2\sqrt{\pi x})(1 + 1/(16x) + 9/(512x^2) + \cdots)$ 与 Watson 专著 [9]，p. 203，Eq. (2) 的 $I_0(2x)$ 渐近一致；$n=5$ 的情形由拉马努金在致 Hardy 第一封信中传达（[16]，p. xxvi），Watson [2] 证明。证明：Barnes [1]，p. 115 的一般结果给出 $\sum (x^k/k!)^n \sim e^{nx}/\sqrt{n(2\pi x)^{(n-1)/2}} \cdot (1 + (n^2-1)/(24nx) + (n^2-1)(n^2+23)/(1152n^2x^2) + \cdots)$，与 (10.23) 前三项一致。

**状态：已证明。**推论 (i) 有两证：其一用 Entry 10（取 $\varphi(t) = (1+t)^n$、$\alpha = \beta = \delta = 0$、$\gamma = 1$、$x = 1/h$）；其二为 ab initio，第二证实质上属于 F. W. J. Olver（私人通信），他证明了 $m=1$ 时的 (10.20)，Berndt 等推广到一切 $m$ 以得 (10.21)。数值复核：推论 (i) 在 $n=1$、$x=20$ 时左端与精确版右端差 $3.9\times 10^{-5}$（在 $O(x^{-3/2}) \approx 0.011$ 界内）。

**对照：** M12（渐近展开、Euler–Maclaurin）、M02（超几何型级数）、M07（Bessel 函数 $I_0$、合流超几何函数）；与 Part II Ch. 12 Entry 48（推论 (i) 的 $n=1$ 情形）互见。

## Entry 11(i)——$\sum (ex/k)^k$ 的渐近展开

当 $x \to \infty$ 时，

$$\sum_{k=0}^\infty \left(\frac{ex}{k}\right)^k \sim \sqrt{2\pi x}\exp\left(x - \frac{1}{24x} - \frac{1}{48x^2} - \left(\frac{1}{36} + \frac{1}{5760}\right)\frac{1}{x^3} + \cdots\right).$$

（$k=0$ 项按 $1$ 理解。）证明用一般渐近公式

$$e^{-x}\sum_{k=0}^\infty \frac{\varphi(k)x^k}{k!} \sim \varphi(x) + \frac{x}{2}\varphi''(x) + \frac{x}{6}\varphi'''(x) + \frac{x^2}{8}\varphi^{(4)}(x) + \frac{x}{24}\varphi^{(4)}(x) + \frac{x^2}{12}\varphi^{(5)}(x) + \frac{x^3}{48}\varphi^{(6)}(x) + \cdots, \tag{11.1}$$

即 Part I Ch. 3 Entry 10（第二本笔记），取 $\varphi(x) = e^x\Gamma(x+1)/x^x$，结合 Stirling 公式。Berndt 注：拉马努金的渐近公式 (11.1) 非常有用且强大；Evans [1] 的论文有若干应用，其推论 14 解决了 Appledorn [1] 的一个此前未解问题。

**状态：已证明。**数值复核：$x=20$ 时左端 $5{,}427{,}070{,}254.31$，右端 $5{,}427{,}072{,}870.79$，相对差 $4.8\times 10^{-7}$（在略去的 $O(x^{-4})$ 项量级内）。

**对照：** M12（渐近展开）、M02（阶乘级数）；与 Part I Ch. 3 Entry 10 互见。

## Entry 11(ii)——$I_n$ 的渐近展开

当 $n \to \infty$ 时，

$$I_n := \int_0^\infty \frac{x^{n-1}\,dx}{\sum_{k=0}^\infty (x/k)^k} \sim n^n\left(\frac{1}{n} + \frac{1}{2n^2} + \frac{1}{3n^3} + \frac{3}{8n^4} + \cdots\right).$$

证明用 (11.2)（Entry 11(i) 证明中的展开）与 $\Gamma(n+\frac{1}{2}) \sim \sqrt{2\pi}n^ne^{-n}(1 - 1/(24n) + 1/(2^7\cdot 3^2n^2) + 1003/(2^{10}\cdot 3^4\cdot 5n^3) + \cdots)$（Olver [1]，p. 295）。

**状态：已证明。**

**对照：** M12（渐近展开）、M09（积分比值）。

## Entry 11(iii)——$S = 1$（对数级数恒等式）

$$S := \mathrm{Log}\,2\sum_{k=2}^\infty \frac{(-1)^k}{k\,\mathrm{Log}\,k} + \mathrm{Log}^2 2\sum_{k=2}^\infty \frac{1}{k\,\mathrm{Log}\,k\,\mathrm{Log}(2k)} = 1.$$

Entry 11(iii) 事实上是拉马努金向 Journal of the Indian Mathematical Society 提交的投稿题 [12]（[16]，p. 333）。证明：对 $n \ge 0$ 归纳证

$$S = \sum_{k=1}^n \frac{1}{k(k+1)} + \sum_{k=2}^\infty \frac{\mathrm{Log}^2 2}{k\,\mathrm{Log}(2^n k)\,\mathrm{Log}(2^{n+1}k)} + \sum_{k=2}^\infty \frac{(-1)^k\mathrm{Log}\,2}{k\,\mathrm{Log}(2^n k)}; \tag{11.3}$$

令 $n \to \infty$，得 $S = \sum_{k=1}^\infty 1/(k(k+1)) = 1$。

**状态：已证明。**数值复核：按 (11.3) 取 $n=20$、$n=50$（尾项直接求和至 $k=3000$ 加解析尾估计）得 $S = 1.000000163$、$1.000000044$，趋向 $1$（直接对原定义求和因两级数收敛极慢而失真，改用 (11.3) 复核）。

**对照：** M02（对数级数）、M12（渐近/望远镜求和）。

## 第 12 节（无 Entry 12）——例题：$\sum \mathrm{Log}(k+1)x^k/k!$ 的渐近展开

**本节无 Entry 12。**拉马努金在第 12 节开头简述 Part I Ch. 3 Entry 10，结尾给出一个例题（为 Ch. 3 第 10 节例 2 的展开）：当 $x \to \infty$ 时，

$$\sum_{k=1}^\infty \frac{\mathrm{Log}(k+1)x^k}{k!} \sim e^x\left(\mathrm{Log}\,x + \frac{1}{2x} + \frac{1}{12x^2} + \frac{1}{12x^3} + \frac{19}{120x^4} + \frac{9}{20x^5} + \cdots\right).$$

证明如 Entry 11(i)，用 Ch. 3 Entry 10，但除 (11.1) 所示七项外还需九项。Pollak 与 Shepp [1] 提出过一个等价的渐近展开，但项数较少。

**状态：已证明。**数值复核：$x=20$ 时左端 $1{,}465{,}660{,}859.52$，右端 $1{,}465{,}660{,}842.0$，相对差 $1.2\times 10^{-8}$（在略去的 $O(x^{-6})$ 项量级内）。

**对照：** M12（渐近展开）、M02（对数级数）。

## Entry 13——四因子有理积分

设 $\alpha$、$\beta$、$\gamma$、$\delta$ 为任意复数。则

$$\int_0^\infty \frac{dx}{(x^2+\alpha^2)(x^2+\beta^2)(x^2+\gamma^2)(x^2+\delta^2)} = \frac{\pi}{6}\cdot\frac{(\alpha+\beta+\gamma+\delta)^3 - (\alpha^3+\beta^3+\gamma^3+\delta^3)}{\alpha\beta\gamma\delta(\alpha+\beta)(\beta+\gamma)(\gamma+\alpha)(\alpha+\delta)(\beta+\delta)(\gamma+\delta)}. \tag{13.1}$$

**推论。**若 $\alpha$、$\beta$、$\gamma$、$\delta$ 为多项式 $x^4 - px^3 + qx^2 - rx + s$ 的根，则

$$\int_0^\infty \frac{dx}{(x^2+\alpha^2)(x^2+\beta^2)(x^2+\gamma^2)(x^2+\delta^2)} = \frac{\pi}{2s}\cdot\frac{1}{r - \frac{ps}{q - r/p}}. \tag{13.2}$$

(13.2) 与 Gradshteyn 与 Ryzhik 表 [1]，p. 218，公式 (5) 的求值相同；因 $p = \alpha+\beta+\gamma+\delta$、$q = \alpha\beta+\alpha\gamma+\alpha\delta+\beta\gamma+\beta\delta+\gamma\delta$、$r = \alpha\beta\gamma+\alpha\beta\delta+\alpha\gamma\delta+\beta\gamma\delta$、$s = \alpha\beta\gamma\delta$，经繁琐计算 (13.2) 可改写为 (13.1) 的形式。

**状态：已证明。**数值复核：$\alpha=1$、$\beta=2$、$\gamma=3$、$\delta=4$ 时两端差 $1.9\times 10^{-34}$；推论 (13.2) 的对称多项式代入亦手工核对得 $\pi/2016$，与 (13.1) 一致。

**对照：** M09（有理函数积分）、M10（Gamma 函数的留数法背景）。

## Entry 14——$\sum (-1)^k(2a)_k(a+k)/(k!\{(a+k)^2+x^2\})$ 的求值

若 $x$ 任意且 $a \ne 0, -1, -2, \dots$，则

$$\sum_{k=0}^\infty \frac{(-1)^k(2a)_k(a+k)}{k!\{(a+k)^2+x^2\}} = \frac{\Gamma^2(a)}{2\Gamma(2a)\prod_{k=0}^\infty\left\{1+\left(\frac{x}{a+k}\right)^2\right\}}.$$

拉马努金 [8]（[16]，p. 53）发表过 Entry 14 的证明。R. Askey 指出如下观察：取 $b = ix$、$c = -ix$，用 Wilson 论文 [1]，Eq. (2.4) 的 ${}_5F_4$ 求值，可得该和等于 $\frac{a}{a^2+x^2}\,{}_4F_3\left[\begin{matrix}2a, a+1, a+ix, a-ix \\ a, a+1+ix, a+1-ix\end{matrix}; -1\right]$，再取极限即得 Entry 14。

例：$n, a > 0$ 时，$\int_0^\infty \cos(nx)/(a^2+x^2)\,dx = \frac{\pi}{2a}e^{-na}$（熟知公式，拉马努金在季报中用 Fourier 余弦反演公式证明，Part I [9]，p. 322）。

**状态：已证明**（拉马努金 [8]）。数值复核：$a=2$、$x=1$ 时左端级数与右端 $\lvert\Gamma(2+i)\rvert^2/(2\Gamma(4))$ 之差 $6.2\times 10^{-33}$。

**对照：** M09（Fourier 余弦积分）、M07（超几何级数 ${}_5F_4$）、M10（Gamma 函数）。

## Entry 15——$\int_0^\infty \lvert\Gamma(a+ix)\rvert^2\cos(2nx)\,dx$

设 $a > 0$，$n$ 为实数，则

$$\int_0^\infty \lvert\Gamma(a+ix)\rvert^2\cos(2nx)\,dx = \frac{1}{2}\sqrt{\pi}\,\Gamma(a)\Gamma(a+\tfrac{1}{2})\,\mathrm{sech}^{2a}n.$$

拉马努金 [8]（[16]，pp. 53，54）证明了 Entry 15。推广：若 $a > 0$ 且 $\lvert\mathrm{Re}\,y\rvert < \frac{1}{2}$，则 $\int_{-\infty}^\infty \lvert\Gamma(a+ix)\rvert^2 e^{2yx}\,dx = \sqrt{\pi}\,\Gamma(a)\Gamma(a+\frac{1}{2})\sec^{2a}y$（见 Wilson 的论文 [1] 及其众多推论）。

**状态：已证明**（拉马努金 [8]）。数值复核：$a=1$、$n=1$ 时两端差 $4.9\times 10^{-32}$（用 $\lvert\Gamma(1+ix)\rvert^2 = \pi x/\sinh\pi x$ 计算）。

**对照：** M09（Fourier 余弦积分）、M10（Gamma 函数）；与 Entry 19 推论（$\mathrm{sech}^{2a}$ 积分）互见。

## Entry 16——四组经典积分

设 $a$ 与 $n$ 均为实数，(iv) 中 $n$ 为整数，则

(i) $\displaystyle \int_0^\infty \frac{\sinh(ax)}{\sinh(\pi x)}\cos(nx)\,dx = \frac{1}{2}\cdot\frac{\sin a}{\cosh n + \cos a}, \quad \lvert a\rvert < \pi$；

(ii) $\displaystyle \int_0^\infty \frac{\cosh(ax)}{\sinh(\pi x)}\sin(nx)\,dx = \frac{1}{2}\cdot\frac{\sinh n}{\cosh n + \cos a}, \quad \lvert a\rvert < \pi$；

(iii) $\displaystyle \int_0^\infty \frac{\sin(nx)}{e^{2\pi x}-1}\,dx = \frac{1}{2}\left(\frac{1}{e^n-1} + \frac{1}{2} - \frac{1}{n}\right), \quad n > 0$；

(iv) $\displaystyle \int_0^\infty \frac{x^{2n-1}}{e^{2\pi x}-1}\,dx = \frac{(-1)^{n-1}B_{2n}}{4n}, \quad n > 0$；$\displaystyle \int_0^\infty \frac{x^{2n}}{\cosh(\pi x/2)}\,dx = (-1)^n E_{2n}, \quad n \ge 0$，

其中 $B_k$、$E_k$（$0 \le k < \infty$）分别为第 $k$ 个 Bernoulli 数与 Euler 数。

(i)(ii) 见 Gradshteyn 与 Ryzhik [1]，p. 504；(iii) 由拉马努金 [8]（[16]，p. 56）陈述，未给证明，但易由 [1]，p. 481，公式 3.911，No. 2 导出；(iv) 两积分均为经典（[1]，pp. 1076，349）。

**状态：已证明**（经典结果）。数值复核：(i) 在 $a=1$、$n=2$ 时差 $1.2\times 10^{-32}$；(iv) 在 $n=1$、$2$ 时分别得 $B_2/4 = 1/24$、$-B_4/8 = 1/240$（差 $0$、$3.1\times 10^{-33}$），Euler 部分 $n=1$、$2$ 时积分值分别为 $1$、$5$，即 $(-1)^1E_2 = 1$、$(+1)E_4 = 5$（标准 Euler 数 $E_2 = -1$、$E_4 = 5$；注：mpmath 的 `euler(n)` 并非 Euler 数，不可直接用它复核）。

**对照：** M09（双曲函数积分）、M01（Bernoulli 数 $B_k$、Euler 数 $E_k$——其定义缺口见 Part I Ch. 5 Entry 9，待补入 M01）、M10（Gamma 函数的矩）。

## Entry 17——Abel–Plana 求和公式

设 $\varphi(z)$ 在 $a \le \mathrm{Re}(z) \le n$ 上解析，其中 $a$ 为非负整数。设 $\lim_{y\to\infty} \lvert\varphi(x\pm iy)\rvert e^{-2\pi y} = 0$（对 $a \le x \le n$ 一致）。则

$$\sum_{k=a}^n \varphi(k) = \int_a^n \varphi(u)\,du + \tfrac{1}{2}\{\varphi(a) + \varphi(n)\} - i\int_0^\infty \frac{\varphi(n+iu) - \varphi(n-iu) - \varphi(a+iu) + \varphi(a-iu)}{e^{2\pi u}-1}\,du. \tag{17.1}$$

Entry 17 即著名的 Abel–Plana 求和公式（Henrici [1]，p. 274；Whittaker 与 Watson [1]，p. 145；历史与应用见 Lindelöf 书 [1]，第 3 章）。拉马努金的表述不如上式精确，因为所有与 $n$ 无关的项都未明确写出。

**推论。**对每个正整数 $n$，$\mathrm{Log}\,n! = n\,\mathrm{Log}\,n - n + \frac{1}{2}\mathrm{Log}(2\pi n) + 2\int_0^\infty \tan^{-1}(x/n)/(e^{2\pi x}-1)\,dx$（取 $\varphi(x) = \mathrm{Log}\,x$ 即得；细节见 Lindelöf [1]，pp. 69，70；Whittaker 与 Watson [1]，pp. 250，251 给出另一证明并归于 Binet 1839 年）。

**状态：已证明**（经典公式）。数值复核：推论在 $n=3$ 时两端差 $2.0\times 10^{-31}$。

**对照：** M02（求和公式）、M12（Euler–Maclaurin 的复变版本）、M10（Stirling 公式、$\mathrm{Log}\,\Gamma$）。

## Entry 18(i)——Abel–Plana 的差分形式

设 $t > 0$，固定正整数 $n$。置 $x = tn$，$\varphi(z) = f(t+tz) - f(tz)$（$f$ 为给定函数）。设 $\varphi(z)$ 满足 Entry 17 的假设（$a = 0$）。则

$$f(x) + \tfrac{1}{2}\varphi(n) = \tfrac{1}{2}\{f(0) + f(t)\} + \int_0^n \varphi(u)\,du - i\int_0^\infty \frac{\varphi(n+iu) - \varphi(n-iu) - \varphi(iu) + \varphi(-iu)}{e^{2\pi u}-1}\,du.$$

**状态：已证明**（对 $\varphi(z)$ 用 Entry 17（$a=0$），注意 (17.1) 左端 $= \varphi(n) + f(x) - f(0)$）。Berndt 注：本书的表述与拉马努金（p. 159）的颇有不同，因为他未记录那些与 $x$ 无关的项；且他的陈述中有两处误印（具体内容见待核对清单）。

**对照：** M02（求和公式）、M12（差分方程）。

## Entry 18(ii)——偶数情形的 Abel–Plana 型公式

设 $t > 0$，固定偶正整数 $n = 2m$。置 $x = tn$，$\varphi(z) = f(tz+t) + f(tz-t)$（$f$ 为给定函数）。设 $\varphi(z)$ 满足下述引理的假设。则

$$2f(x) = 2(-1)^m f(0) + \int_0^\infty \frac{\varphi(n+iu) + \varphi(n-iu)}{e^{\pi u/2} + e^{-\pi u/2}}\,du - (-1)^m\int_0^\infty \frac{\varphi(iu) + \varphi(-iu)}{e^{\pi u/2} + e^{-\pi u/2}}\,du,$$

只要上述积分存在。

所用引理：设 $n = 2m$ 为偶正整数，$\varphi(z)$ 在 $0 \le \mathrm{Re}(z) \le n$ 上解析，且 $\lim_{y\to\infty} \lvert\varphi(x\pm iy)\rvert e^{-\pi y/2} = 0$（对 $0 \le x \le n$ 一致）。则只要以下积分存在，$2\sum_{k=1}^m (-1)^k\varphi(2k-1) = (-1)^m\int_0^\infty \{\varphi(n+iu)+\varphi(n-iu)\}/(e^{\pi u/2}+e^{-\pi u/2})\,du - \int_0^\infty \{\varphi(iu)+\varphi(-iu)\}/(e^{\pi u/2}+e^{-\pi u/2})\,du$。

**状态：已证明**（留数定理；Entry 18(ii) 同样不是拉马努金所正确表述的，Berndt 为证它先建立了上述引理）。

**对照：** M02（交错求和）、M09（Fourier 积分）。

## Entry 19——Fourier 积分定理

设 $n > 0$。若 $\psi(n) = \int_0^h \varphi(x)\cos(nx)\,dx$，则

(i) $\displaystyle \int_0^\infty \psi(x)\cos(mx)\,dx = \begin{cases} \frac{\pi}{2}\varphi(m), & m < h, \\ \frac{\pi}{4}\varphi(m), & m = h, \\ 0, & m > h; \end{cases}$

若 $\psi(n) = \int_0^h \varphi(x)\sin(nx)\,dx$，则

(ii) $\displaystyle \int_0^\infty \psi(x)\sin(mx)\,dx = \begin{cases} \frac{\pi}{2}\varphi(m), & m < h, \\ \frac{\pi}{4}\varphi(m), & m = h, \\ 0, & m > h. \end{cases}$

Entry 19 易由 Fourier 积分定理得到（Titchmarsh [1]，pp. 432–435；[2]，pp. 16，17），在 $\varphi$ 于 $[0,h]$ 上连续且有界变差时成立；亦见于拉马努金的季报（Part I [9]，p. 333）。

**推论。**若 $a > 0$，$n$ 为实数，则 $\int_0^\infty \mathrm{sech}^{2a}x\cos(2nx)\,dx = \sqrt{\pi}\,\lvert\Gamma(a+in)\rvert^2/(2\Gamma(a)\Gamma(a+\frac{1}{2}))$（拉马努金 [8]（[16]，p. 54）用 Fourier 反演公式与 Entry 15 证明）。推广：若 $a > \lvert\mathrm{Re}\,y\rvert$，则 $\int_{-\infty}^\infty \mathrm{sech}^{2a}x\,e^{2yx}\,dx = 2^{2a-1}\Gamma(a+y)\Gamma(a-y)/\Gamma(2a)$（Beta 积分）。

**状态：已证明**（Fourier 积分定理）。

**对照：** M09（Fourier 积分定理、余弦/正弦变换）、M10（Gamma 函数）。

## Entry 20——$\int_0^\infty \sinh(ax)/\sinh(\pi x) \cdot dx/(1+n^2x^2)$

若 $n > 0$ 且 $0 \le a < \pi$，则

$$\int_0^\infty \frac{\sinh(ax)}{\sinh(\pi x)}\cdot\frac{dx}{1+n^2x^2} = \sum_{k=1}^\infty \frac{(-1)^{k+1}\sin(ka)}{1+nk}.$$

**状态：已证明**（经典结果，Gradshteyn 与 Ryzhik [1]，p. 352；围道积分易得）。数值复核：$n=1$、$a=1$ 时两端差 $0$（30 位精度）。

**对照：** M09（双曲函数积分）、M02（交错级数）。

## Entry 21——积分次序交换恒等式

设 $p$、$q$、$n$ 为实数。设 $\varphi_j(p,x)$ 与 $F(nx)$ 在 $\alpha_j \le x \le \beta_j$（$j = 1, 2$）上连续。定义 $\psi_1(p,n)$、$\psi_2(p,n)$ 为 $\int_{\alpha_1}^{\beta_1} \varphi_1(p,x)F(nx)\,dx = \psi_1(p,n)$ 与 $\int_{\alpha_2}^{\beta_2} \varphi_2(p,x)F(nx)\,dx = \psi_2(p,n)$。则

$$\int_{\alpha_1}^{\beta_1} \varphi_1(p,x)\psi_2(q,nx)\,dx = \int_{\alpha_2}^{\beta_2} \varphi_2(q,x)\psi_1(p,nx)\,dx.$$

**状态：已证明**（交换积分次序即得）。下述推论形式上是 Entry 21 的特例，即余弦变换的 Parseval 定理，但因积分区间无限，需另取假设（取自 Titchmarsh 书 [2]，p. 54）。Entry 21 与推论均由拉马努金 [8]（[16]，pp. 55，56）形式地证明。

**推论。**设 $p$、$q$、$l$、$n$ 为实数。设 $\varphi(p,x) \in L(0,\infty)$（关于变量 $x$）且 $\lim_{x\to 0+} \varphi(p,x)$ 存在。定义 $\psi(p,n) = \int_0^\infty \varphi(p,x)\cos(nx)\,dx$（设其在 $0 \le n < \infty$ 的任一有限区间上可积），并设 $\psi(p,n) \to 0$（$n \to \infty$）。则 $\frac{\pi}{2}\int_0^\infty \varphi(p,x)\varphi(q,lx)\,dx = \int_0^\infty \psi(q,x)\psi(p,lx)\,dx$。

例：若 $\alpha\beta = \pi/4$，则 $\sqrt{\alpha}\int_0^\infty e^{-x^2}/\cosh(\alpha x)\,dx = \sqrt{\beta}\int_0^\infty e^{-x^2}/\cosh(\beta x)\,dx$（该例与推论均见于拉马努金致 Hardy 第一封信 [16]，p. 350；此前拉马努金 [6] 已将其作为问题投稿于 Journal of the Indian Mathematical Society；亦见 [8]，[16]，p. 55）。拉马努金接下来说该例可由公式 $\sqrt{\alpha}\sum_{k=0}^\infty (-1)^k E_{2k+1}\alpha^{2k}/k! = \sqrt{\beta}\sum_{k=0}^\infty (-1)^k E_{2k+1}\beta^{2k}/k!$（(21.1)）导出，而 (21.1) 又「由定理」$\sum_{k=1}^\infty (-1)^{k+1}\varphi(k) = \sum_{k=0}^\infty (-1)^k\varphi(-k)$（(21.2)，即 Part I Ch. 4 第 9 节例 2）得到。(21.1) 实际上只是 Poisson 求和公式（见第 31 节推论 (i)）在函数为特殊自反 Fourier 变换时的特例；(21.2) 只在严厉限制下成立（Part I，p. 97）。

**对照：** M09（Parseval 定理、余弦变换）、M06（自反变换、模形式氛围）、M01（Euler 数 $E_{2k+1}$）。

## Entry 22——最著名的 Gamma 乘积积分

设 $a, b > 0$，则

(i) $\displaystyle \int_0^\infty \lvert\Gamma(a+ix)\Gamma(b+ix)\rvert^2\,dx = \frac{\sqrt{\pi}\,\Gamma(a)\Gamma(a+\frac{1}{2})\Gamma(b)\Gamma(b+\frac{1}{2})\Gamma(a+b)}{2\Gamma(a+b+\frac{1}{2})}$；

若 $0 < a < b + \frac{1}{2}$，则

(ii) $\displaystyle \int_0^\infty \left\lvert\frac{\Gamma(a+ix)}{\Gamma(b+1+ix)}\right\rvert^2 dx = \frac{\sqrt{\pi}\,\Gamma(a)\Gamma(a+\frac{1}{2})\Gamma(b-a+\frac{1}{2})}{2\Gamma(b+1)\Gamma(b+\frac{1}{2})\Gamma(b-a+1)}.$$

这两条优美的公式由拉马努金 [8]（[16]，pp. 57，54）导出，或许是他最著名的积分求值。Barnes [2]，pp. 154，155 在大约同一时间建立了 (i) 的推广；R. Roy [1] 用 Mellin 变换证明了 (ii)。推广（用 Parseval 定理（Titchmarsh [2]，p. 5）、第 19 节推论与 Legendre 倍元公式）：$2\int_0^\infty \lvert\Gamma(a+ix)\Gamma(b+ix)\rvert^2\cos(xy)\,dx = \frac{\pi}{4^{a+b-1}}\Gamma(2a)\Gamma(2b)\int_{-\infty}^\infty \mathrm{sech}^{2a}\frac{u}{2}\,\mathrm{sech}^{2b}\frac{u+y}{2}\,du$（$y \ge 0$；Glaister [1] 说明如何求右端这类积分）。

**状态：已证明**（拉马努金 [8]）。数值复核：(i) 在 $a=b=1$ 时两端差 $9.9\times 10^{-32}$（用 $\lvert\Gamma(1+ix)\rvert^2 = \pi x/\sinh\pi x$ 计算）。

**对照：** M09（Gamma 乘积积分）、M10（Gamma 函数）、M06（Barnes 推广）；章首导言点名「许多优美而重要的积分以拉马努金命名（例如 Entry 22）」。

## Entry 23——$\int_0^\infty x^{-m}\Gamma(x+a)/\Gamma(x+a+n+1)\,dx$

设 $a > 0$，$m < 1$，$m+n > 0$。则

$$\int_0^\infty \frac{x^{-m}\Gamma(x+a)}{\Gamma(x+a+n+1)}\,dx = \frac{\pi\csc(\pi m)}{\Gamma(n+1)}\sum_{k=0}^\infty \frac{(-n)_k}{k!(a+k)^m}.$$

Berndt 注：本书作者未能在文献中找到该结果；拉马努金在季报中亦得到此积分公式，完整证明见 Part I，pp. 303，304。

**状态：已证明**（季报证明）。

**对照：** M09（Gamma 比值积分）、M10（Gamma 函数）、M02（Pochhammer 级数）。

## Entry 24(i)——平凡恒等式

$$\sum_{k=0}^n A_k = \sum_{k=0}^\infty A_{n-k} - \sum_{k=1}^\infty A_{-k},$$

其后有一推论，其中 $A_k$ 换成 $A_k/\Gamma(k+1)$。

**状态：已证明**（平凡）。

**对照：** M02（级数重排）。

## Entry 24(ii)——极限等式（意图不明）

Entry 24(ii) 的意图是 $\lim_{N\to\infty}\sum_{k=-N}^N \varphi(x+k) = \lim_{N\to\infty}\sum_{k=-N}^N \varphi(y+k)$，但 Berndt 明言其意图「indeed unclear」（确实不明）。

拉马努金在一推论中断言：$\frac{x^h}{h!} + \sum_{k=1}^\infty\left(\frac{x^{h+kn}}{\Gamma(h+kn+1)} + \frac{x^{h-kn}}{\Gamma(h-kn+1)}\right) = 1 + \sum_{k=1}^\infty\left(\frac{x^{kn}}{\Gamma(kn+1)} + \frac{x^{-kn}}{\Gamma(-kn+1)}\right) = \frac{e^x}{n}$，其中 $n \le 1$，$x$、$h$ 任意。**该断言一般不成立**：虽然 $h=0$、$n=1$ 时等式成立，但一般情形下最左端是 $h$ 的非常值函数而其余表达式不是；且若 $n$ 不是整数，级数发散。

**状态：已否定**（按字面表述；Berndt 在书中已指出不成立）。

**对照：** M02（级数）、M10（Gamma 函数）。

## Entry 24(iii)——$\int_{-\infty}^\infty \varphi(x)/\Gamma(x+1)\,dx = \sum \varphi(n)/\Gamma(n+1)$

拉马努金给出等式

$$\int_{-\infty}^\infty \frac{\varphi(x)}{\Gamma(x+1)}\,dx = \sum_{n=0}^\infty \frac{\varphi(n)}{\Gamma(n+1)}. \tag{24.1}$$

积分等于相应和的实例是罕见的（见 Boas 与 Pollard [1]、Krishnan [1]、Forrester [1] 的论文；亦见 Part II Ch. 14 Entry 5(i)(ii) 与 Entry 16(i)(ii)）。

推论 (i)：拉马努金断言 $\int_{-\infty}^\infty a^x/\Gamma(x+1)\,dx = e^a$（形式上由 (24.1) 取 $\varphi(x) = a^x$ 得到）。但 $a=0$ 时断言显然为假；$a$ 为实数且非零时积分发散。

推论 (ii)：拉马努金断言 $\int_{-\infty}^\infty a^x\Gamma(n+1)/(\Gamma(x+1)\Gamma(n-x+1))\,dx = (1+a)^n$（(24.2)，形式上由 (24.1) 取 $\varphi(x) = a^x\Gamma(n+1)/\Gamma(n-x+1)$ 得到）。同样，$a=0$ 时 (24.2) 为假；$a$ 为实数且 $\ne 0, \pm 1$ 时积分发散。若 $a = e^{i\alpha}$（$\lvert\alpha\rvert < \pi$，$\alpha$ 为实数），则 (24.2) 成立，事实上由拉马努金在其论文 [14]（[16]，pp. 216–229，Eq. (1.2)）中证明。

**状态：已否定**（(24.1) 作为一般陈述不成立；推论 (i) 不成立；推论 (ii) 仅在 $a = e^{i\alpha}$ 时成立）。

**对照：** M02（积分与求和的互换）、M10（Gamma 函数）；与 Part II Ch. 14 Entry 5、Entry 16 互见。

## Entry 25(i)——Entry 25(ii) 的 $b = 0$ 特例

Entry 25(i) 是 $b = 0$ 时 Entry 25(ii) 的特例（见下）。

**对照：** M10（Gamma 函数）。

## Entry 25(ii)——$A_n$、$B_n$ 的形式公式

拉马努金写道

$$A_n := \int_0^\infty \left(\frac{a^{b+x}}{\Gamma(b+x+1)} + \frac{a^{b-x}}{\Gamma(b-x+1)}\right)\cos(nx)\,dx = e^{a\cos n}\cos(a\sin n - nb)$$

与

$$B_n := \int_0^\infty \left(\frac{a^{b+x}}{\Gamma(b+x+1)} - \frac{a^{b-x}}{\Gamma(b-x+1)}\right)\sin(nx)\,dx = e^{a\cos n}\sin(a\sin n - nb),$$

其中大概 $a$ 为实数。由 Stirling 公式易见，若 $a \ne 0$，这两个积分都发散。但拉马努金的推理可由简单换元与 (24.1) 辨认：$A_n + iB_n = \int_{-\infty}^\infty a^{b+x}/\Gamma(b+x+1)\cdot e^{inx}\,dx = \sum_{k=0}^\infty a^k e^{in(k-b)}/k! = \exp(ae^{in} - inb)$；取实部与虚部即得其形式推导。Entry 23–25 的内容或许是拉马努金名篇 [14]（关于含 Gamma 函数的积分）的种子。

例 (i)：$a^x/\Gamma(x+1)$ 的最大值在 $a$ 大时等于 $\frac{a^{a-1/2}}{\Gamma(a+\frac{1}{2})}\left\{1 + \frac{1}{1152a^3} + O\left(\frac{1}{a^4}\right)\right\}$。证明：$a^x/\Gamma(x+1)$ 在 $\psi(x+1) - \mathrm{Log}\,a = 0$（(25.1)，$\psi(x) = \Gamma'(x)/\Gamma(x)$）处取最大值；用 Part I Ch. 8 Entry 15（Part I，p. 194）中拉马努金给出的该根的渐近 $x + \frac{1}{2} = a - 1/(24a) + 3/(640a^3) + \cdots$，结合 Ch. 11 第 24 节引理 2 的 $\Gamma(a+\frac{1}{2}+\varepsilon)/\Gamma(a+\frac{1}{2})$ 展开即得。Berndt 的版本与拉马努金的不同：拉马努金写最大值「very nearly」为 $\frac{a^{a-1/2}}{\Gamma(a+\frac{1}{2})}\exp\left(\frac{1}{1152a^3+323.2a}\right)$，除 $323.2a$ 一项外与本书陈述一致，而 $323.2a$ 显然不正确。

例 (ii)：拉马努金陈述了 Euler–Maclaurin 求和公式 (10.5) 的一个版本，并注它「在求定积分时非常有用」。

**状态：** Entry 25(ii) 的两积分在 $a \ne 0$ 时发散，**按字面已否定**（仅为形式公式）；例 (i) 已证明（Berndt 的版本；拉马努金版的 $323.2a$ 有误）。

**对照：** M10（Gamma 函数、$\psi$ 函数）、M12（Euler–Maclaurin）；与 Part I Ch. 8 Entry 15、Part II Ch. 11 第 24 节引理 2 互见。

## Entry 26(i)——$\int_0^\infty \cos(2nx)/(1+x^2)^{m+1}\,dx$ 的闭式

设 $n > 0$，$m$ 为非负整数。则

$$\int_0^\infty \frac{\cos(2nx)}{(1+x^2)^{m+1}}\,dx = \frac{\pi n^m e^{-2n}}{2m!}\sum_{k=0}^m \frac{(m+k)!}{(4n)^k(m-k)!k!}.$$

**状态：已证明**（经典结果，Gradshteyn 与 Ryzhik [1]，p. 413；围道积分可得）。数值复核：$m=1$、$n=1$ 时左端积分（scipy 求积 $0.31887624949$）与右端 $3\pi e^{-2}/4 = 0.31887624869$ 之差 $8\times 10^{-10}$（在求积误差估计内；mpmath 的 quad 在此振荡积分上有约 $10^{-7}$ 的误差，已用 scipy 交叉核对）。

**对照：** M09（余弦积分）。

## Entry 26(ii)——$I(m,n)$ 的闭式

设 $p > 0$，$m$、$n$ 为非负整数且 $m \le n$。则

$$I(m,n) := \int_0^\infty \frac{x^{2m}\cos(px)}{(1+x^2)^{n+1}}\,dx = \frac{(-1)^m\pi e^{-p}}{2^{n+1}n!}\sum_{r=0}^n A_r p^{n-r}, \tag{26.1}$$

其中（$r \ge 0$）$A_r = \frac{(n+r)!}{2^r r!(n-r)!}\sum_{k=0}^{\min(r,m)} \frac{4^k(-r)_k(-m)_k(-n)_k}{(-n-r)_{2k}k!}$。

**状态：已证明**（对 $m$ 归纳；$m=0$ 时由 Entry 26(i) 得；用递推 $I(m+1,n) = I(m,n-1) - I(m,n)$（(26.2)））。数值复核：$m=0$、$n=1$、$p=1$ 时左端与右端 $\pi/(2e)$ 之差约 $4\times 10^{-10}$（scipy 求积；mpmath 的 quad 在此振荡积分上有约 $10^{-8}$ 的误差）。

**对照：** M09（余弦积分）、M07（Pochhammer 级数）。

## Entry 27——无穷乘积 $\prod_{k=1}^\infty \{1+(x/k)^n\}^2$

若 $n$ 为偶正整数，则

$$\prod_{k=1}^\infty \left\{1+\left(\frac{x}{k}\right)^n\right\}^2 = \prod_{k=1}^{n/2} \frac{\cosh(2\pi x\sin((2k-1)\pi/n)) - \cos(2\pi x\cos((2k-1)\pi/n))}{2\pi^2x^2}. \tag{27.1}$$

证明：右端化为 $\prod_{k=1}^\infty\prod_{j=1}^{n/2}(1 - x^2e^{-2\pi i(2j-1)/n}/k^2)(1 - x^2e^{2\pi i(2j-1)/n}/k^2)$（(27.2)），比较两端 $2n$ 个根即得。

推论 (i)：$n$ 任意时，$\prod_{k=1}^\infty \{1+(2n/(n+k))^3\} = \Gamma^3(n+1)\sinh(\pi n\sqrt{3})/(\Gamma(3n+1)\pi n\sqrt{3})$。推论 (ii)：$n$ 任意时，$\prod_{k=1}^\infty \{1+((2n+1)/(n+k))^3\} = \Gamma^3(n+1)\cosh\{\pi(n+\frac{1}{2})\sqrt{3}\}/(\Gamma(3n+2)\pi)$。后两式由拉马努金 [9]（[16]，p. 51）证明。

**状态：已证明。**数值复核：$n=4$、$x=0.5$ 时左端乘积（截断至 $k=200$）与右端差 $6.0\times 10^{-9}$（截断尾量级）。

**对照：** M02（无穷乘积）、M10（Gamma 函数）。

## Entry 28——$mn\sum x^{nk}/(nk)!$ 的三角和表示

若 $m$、$n$ 为正整数，$x$ 任意，则

$$mn\sum_{k=0}^\infty \frac{x^{nk}}{(nk)!} = \sum_{k=0}^{mn-1} e^{x\cos(2\pi k/n)}\cos(x\sin(2\pi k/n)).$$

**状态：已证明**（令 $k = jn+r$ 分组求和；内层和除非 $n \mid j$ 否则为 $0$）。数值复核：$m=2$、$n=3$、$x=1$ 时两端差 $7.9\times 10^{-31}$。

**对照：** M02（指数级数的根式滤子）、M09（三角和）。

## Entry 29(i)(ii)——$\int_0^\infty (-x^2)^l/(1+x^{2n})\cos(px)\,dx$

设 $p \ge 0$，$l$ 为非负整数，$n$ 为大于 $1$ 的正整数。则

$$\int_0^\infty \frac{(-x^2)^l}{1+x^{2n}}\cos(px)\,dx = \begin{cases} \frac{\pi}{2n}e^{-p} + \frac{\pi}{n}\sum_{k=1}^{(n-1)/2} e^{-p\cos(\pi k/n)}\cos\left(\frac{(2l+1)\pi k}{n} - p\sin\frac{\pi k}{n}\right), & n \text{ 为奇数}, \\ \frac{\pi}{n}\sum_{k=1}^{n/2} e^{-p\cos((2k-1)\pi/(2n))}\cos\left(\frac{(2l+1)(2k-1)\pi}{2n} - p\sin\frac{(2k-1)\pi}{2n}\right), & n \text{ 为偶数}. \end{cases}$$

**状态：已证明**（留数计算；与 Gradshteyn 与 Ryzhik 表 [1]，p. 414，公式 3.738，No. 2 的表述不同，且该处一个括号放错了位置；与 Entry 33(i)(ii) 的证明做类似计算，细节略）。数值复核：奇情形 $n=3$、$l=0$、$p=1$ 时差 $3.3\times 10^{-12}$；偶情形 $n=4$、$l=1$、$p=0.7$ 时差 $3.2\times 10^{-14}$（均为振荡积分求积误差量级）。

**对照：** M09（有理三角积分）。

## Entry 30(i)——$\int_0^\infty \sin^{2n+1}x/x\,dx = \int_0^\infty \sin^{2n+2}x/x^2\,dx$

若 $n$ 为非负整数，则

$$\int_0^\infty \frac{\sin^{2n+1}x}{x}\,dx = \int_0^\infty \frac{\sin^{2n+2}x}{x^2}\,dx = \frac{\sqrt{\pi}\,\Gamma(n+\frac{1}{2})}{2n!}.$$

**状态：已证明**（Fichtenholz 书 [1]，p. 656；这两积分实际是 Part II Ch. 14 Entry 16(i)(ii) 的特例；更多文献见 Wang [1] 的问题）。数值复核：$n=1$ 时 $\int_0^\infty \sin^3x/x\,dx = \pi/4$（用 $\sin^3x = (3\sin x - \sin 3x)/4$ 与 $\int_0^\infty \sin(ax)/x\,dx = \pi/2$ 验证，精确成立）；$n=2$ 时 $\sin^5x$ 恒等式亦精确成立。

**对照：** M09（正弦幂积分）、M10（Gamma 函数）。

## Entry 30(ii)——$\varphi(n,p)$ 的递推

若 $p > 2$ 且 $n-p+1 > 0$，则

$$(p-1)(p-2)\varphi(n,p) = n(n-1)\varphi(n-2,p-2) - n^2\varphi(n,p-2),$$

其中 $\varphi(n,p) = \int_0^\infty \sin^n x/x^p\,dx$（(30.1)）。

**推论 (i)。**若 $n$ 为非负整数，则 $\varphi(2n+3,3) = \sqrt{\pi}(n+\frac{3}{2})\Gamma(n+\frac{1}{2})/(4(n+1)!)$。**推论 (ii)。**若 $n$ 为非负整数，则 $\varphi(2n+4,4) = \sqrt{\pi}(n+2)\Gamma(n+\frac{1}{2})/(6(n+1)!)$。

例 (i)：若 $0 < p < n+1$，$\varphi(n,p) = \frac{1}{\Gamma(p)}\int_0^\infty \sin^n x\int_0^\infty e^{-tx}t^{p-1}\,dt\,dx$。例 (ii)(iii)：若 $a > 0$，$n$ 为非负整数，则 $\int_0^\infty e^{-ax}\sin^{2n+1}x\,dx = (2n+1)!/((a^2+1^2)(a^2+3^2)\cdots(a^2+(2n+1)^2))$ 与 $\int_0^\infty e^{-ax}\sin^{2n}x\,dx = (2n)!/(a(a^2+2^2)(a^2+4^2)\cdots(a^2+(2n)^2))$（经典，Gradshteyn 与 Ryzhik [1]，p. 478；归纳易得）。

**状态：已证明**（两次分部积分）。

**对照：** M09（正弦幂积分）、M10（Gamma 函数）。

## Entry 31(i)——Poisson 求和

设 $h$、$\alpha$、$\beta > 0$，$\alpha\beta = 2\pi$。设 $\varphi$ 在 $[0,h]$ 上连续且有界变差。定义 $\psi(r) = \int_0^h \varphi(x)\cos(rx)\,dx$。则若 $n$ 为实数，

$$\alpha\sum_{0\le k\le h/\alpha}' \varphi(\alpha k)\cos(\alpha nk) = \psi(n) + \sum_{k=1}^\infty \{\psi(\beta k+n) + \psi(\beta k-n)\}. \tag{31.1}$$

证明用 Poisson 求和公式 $\sum_{a\le k\le b}' f(k) = \int_a^b f(x)\,dx + 2\sum_{k=1}^\infty \int_a^b f(x)\cos(2\pi kx)\,dx$（(31.2)）。

**状态：已证明。**

**对照：** M02（Poisson 求和）、M09（余弦变换）。

## Entry 31(ii)——$\int_0^h \sin(nx)/\sin x \cdot \varphi(x)\,dx$

设 $\varphi$、$\psi$ 如 Entry 31(i) 所定义。设 $h > 0$，$n$ 为整数。则

$$\int_0^h \frac{\sin(nx)}{\sin x}\varphi(x)\,dx = \pi\sum_{0\le k\le h/\pi}' (-1)^k\varphi(k\pi)\cos(kn\pi) - 2\sum_{k=0}^\infty \psi(n+2k+1). \tag{31.3}$$

**推论 (i)。**设 $\alpha$、$\beta > 0$，$\alpha\beta = 2\pi$。设 $\varphi$ 在 $(0,\infty)$ 上连续且有界变差，在 $(0,\infty)$ 上可积。置 $\psi(r) = \int_0^\infty \varphi(x)\cos(rx)\,dx$。则 $\alpha\sum_{k=0}^\infty{}' \varphi(\alpha k) = \psi(0) + 2\sum_{k=1}^\infty \psi(\beta k)$（在 (31.1) 中取 $n=0$、$h \to \infty$）。

**推论 (ii)。**在 Entry 31(ii) 的假设下，$\lim_{n\to\infty}\left(\int_0^h \frac{\sin(nx)}{\sin x}\varphi(x)\,dx - \pi\sum_{0\le k\le h/\pi}' (-1)^k\varphi(k\pi)\cos(kn\pi)\right) = 0$（因 $\sum_{k=1}^\infty \psi(k)$ 收敛）。

**状态：已证明**（对 $n$ 归纳；(31.3) 在 $n=0$、$1$ 时由 (31.1) 取 $\alpha = \pi$、$\beta = 2$ 得到）。

**对照：** M02（Poisson 求和）、M09（Fourier 积分）。

## Entry 32(i)——Poisson 求和的正弦版本

设 $h$、$\alpha$、$\beta > 0$，$\alpha\beta = 2\pi$。设 $\varphi$ 在 $[0,h]$ 上连续且有界变差。定义 $\psi(r) = \int_0^h \varphi(x)\sin(rx)\,dx$。则若 $n$ 为实数，

$$\alpha\sum_{0\le k\le h/\alpha}' \varphi(\alpha k)\sin(\alpha nk) = \psi(n) + \sum_{k=1}^\infty \{\psi(\beta k+n) - \psi(\beta k-n)\}.$$

**状态：已证明**（在 Poisson 求和公式 (31.2) 中取 $a = 0$、$b = h/\alpha$、$f(x) = \varphi(\alpha x)\sin(\alpha nx)$）。

**对照：** M02（Poisson 求和）、M09（正弦变换）。

## Entry 32(ii)——Euler–Maclaurin 求和公式的另一版本

Entry 32(ii) 是 Euler–Maclaurin 求和公式 (10.5) 的另一版本（书中仅此一句话，未印公式；确切形式见待核对清单）。

**推论。**设 $\alpha$、$\beta > 0$，$\alpha\beta = \pi/2$。设 $\varphi(x)$ 在 $(0,\infty)$ 上连续，在 $(0,\delta)$ 上可积，在 $(\delta,\infty)$ 上有界变差，且当 $x \to \infty$ 时趋向 $0$（$0 < \delta < \pi/2$）。定义 $\psi(r) = \int_0^\infty \varphi(x)\sin(rx)\,dx$。则 $\alpha\sum_{k=0}^\infty (-1)^k\varphi((2k+1)\alpha) = \sum_{k=0}^\infty (-1)^k\psi((2k+1)\beta)$。该推论给出 Fourier 正弦变换的 Poisson 求和公式（Titchmarsh [2]，p. 66）。

拉马努金在第 32 节结尾注：$\int_0^h \cos(nx)/\cos x \cdot \varphi(x)\,dx$、$\int_0^h \sin(nx)/\cos x \cdot \varphi(x)\,dx$ 与 $\int_0^h \cos(nx)/\sin x \cdot \varphi(x)\,dx$ 这类积分都可求出——他显然在指 Entry 31(ii) 的类似物存在。

**状态：** Entry 32(ii) 仅为一句话的指引（未印公式）；推论已证明。

**对照：** M02（Poisson 求和、Euler–Maclaurin）、M01（Bernoulli 数，(10.5) 的系数）。

## Entry 33(i)(ii)——$\int_0^\infty \{(-x^2)^l/(1-x^{2n}) + (-1)^l/(n(x^2-1))\}\cos(px)\,dx$

设 $n$、$l$ 为非负整数且 $n > 1$，$p > 0$。则

$$I := \int_0^\infty \left\{\frac{(-x^2)^l}{1-x^{2n}} + \frac{(-1)^l}{n(x^2-1)}\right\}\cos(px)\,dx$$

$$= \begin{cases} \frac{\pi}{2n}e^{-p} + \frac{\pi}{n}\sum_{k=1}^{n/2-1} e^{-p\cos(\pi k/n)}\cos\left(\frac{\pi(2l+1)k}{n} - p\sin\frac{\pi k}{n}\right), & n \text{ 为偶数}, \\ \frac{\pi}{n}\sum_{k=1}^{(n-1)/2} e^{-p\cos((2k-1)\pi/(2n))}\cos\left(\frac{\pi(2l+1)(2k-1)}{2n} - p\sin\frac{(2k-1)\pi}{2n}\right), & n \text{ 为奇数}. \end{cases}$$

**状态：已证明**（留数计算；$f(z) = (nz^{2l} - z^{2n-2} - \cdots - z^2 - 1)/(n(1-z^{2n}))\cdot e^{ipz}$ 在上半平面有单极点 $z = \exp(\pi ik/n)$（$1 \le k \le n-1$））。数值复核：奇情形 $n=3$、$l=0$、$p=1$：被积函数在 $x=1$ 处的可去奇点化简为 $(x^2+2)/(3(x^4+x^2+1))$，其积分的留数计算值 $0.440349616972202$ 与右端公式值逐位一致；偶情形 $n=2$、$l=0$、$p=1$：被积函数化简为 $1/(2(x^2+1))$，积分 $= \pi/(4e)$，与右端 $\frac{\pi}{4}e^{-1}$ 恒等（直接求积的振荡误差约 $10^{-4}$，已用留数与恒等式交叉核对）。

**对照：** M09（留数积分）、M02（三角和）。

## Entry 34(i)(ii)——$\pi\cos(\theta x)/(x\sin\pi x)$ 与 $\pi\sin(\theta x)/(4x\cos\frac{1}{2}\pi x)$ 的部分分式

设 $x$ 任意，则

(i) $\displaystyle \frac{\pi\cos(\theta x)}{x\sin(\pi x)} = \frac{1}{x^2} + 2\sum_{k=1}^\infty \frac{(-1)^{k+1}\cos(k\theta)}{k^2-x^2}, \quad \lvert\theta\rvert \le \pi$；

(ii) $\displaystyle \frac{\pi\sin(\theta x)}{4x\cos(\frac{1}{2}\pi x)} = \sum_{k=0}^\infty \frac{(-1)^k\sin((2k+1)\theta)}{(2k+1)^2-x^2}, \quad \lvert\theta\rvert \le \pi/2$。

**推论。**设 $x$ 任意，则 (i) $\frac{\pi\cosh(\theta x)}{x\sinh(\pi x)} = \frac{1}{x^2} + 2\sum_{k=1}^\infty \frac{(-1)^k\cos(k\theta)}{k^2+x^2}$（$\lvert\theta\rvert \le \pi$）；(ii) $\frac{\pi\sinh(\theta x)}{4x\cosh(\frac{1}{2}\pi x)} = \sum_{k=0}^\infty \frac{(-1)^k\sin((2k+1)\theta)}{(2k+1)^2+x^2}$（$\lvert\theta\rvert \le \pi/2$）。

**状态：已证明**（推论 (i) 见 Bromwich 书 [1]，p. 368，Eq. (4.1)；Entry 34(i) 由推论 (i) 将 $x$ 换成 $ix$ 即得；Entry 34(ii) 由 $\sin\{(2k+1)\theta\}$ 在 $[-\pi/2,\pi/2]$ 上的完备正交集作 Fourier 展开，再解析延拓；推论 (ii) 由 Entry 34(ii) 将 $x$ 换成 $ix$ 即得）。数值复核：$x=0.5$、$\theta=1$ 时 (i)(ii) 两端差均为 $7.9\times 10^{-31}$。

**对照：** M02（部分分式、Fourier 级数）、M09（三角积分）。

## Entry 35——$\sqrt{\alpha}\{1 + 2\sum 1/(1+\alpha^2k^2)^{n+1}\}$ 的 Poisson 型恒等式

设 $n$ 为非负整数，$\alpha, \beta > 0$，$\alpha\beta = \pi$。则

$$\sqrt{\alpha}\left\{1 + 2\sum_{k=1}^\infty \frac{1}{(1+\alpha^2k^2)^{n+1}}\right\} = \sqrt{\beta}\,\frac{\Gamma(n+\frac{1}{2})}{\Gamma(n+1)}\left\{1 + 2\sum_{k=1}^\infty e^{-2\beta k}\varphi(4\beta k)\right\},$$

其中 $\varphi(t) = \frac{n!}{(2n)!}\sum_{k=0}^n \frac{(n+k)!t^{n-k}}{(n-k)!k!}$。

**状态：已证明**（在 Poisson 求和公式 (31.2) 中取 $a = 0$、$b = \infty$、$f(x) = 2(1+\alpha^2x^2)^{-n-1}$，结合 Entry 26(i)）。数值复核：$n=0$、$\alpha=1$、$\beta=\pi$ 时两端差 $0$；$n=1$、$\alpha=2$、$\beta=\pi/2$ 时差 $2.0\times 10^{-31}$。

**对照：** M02（Poisson 求和）、M06（$\alpha\beta = \pi$ 的模形式氛围）、M10（Gamma 函数）。

## Entry 36——$m\sum' 1/(m^2+(n+k)^2)$ 的渐近展开

设 $N$ 为任意正整数。当 $m^2+n^2 \to \infty$ 时，

$$m\sum_{k=0}^\infty{}' \frac{1}{m^2+(n+k)^2} = \tan^{-1}(m/n) + \sum_{k=1}^N \frac{B_{2k}\sin(2k\tan^{-1}(m/n))}{2k(m^2+n^2)^k} + O((m^2+n^2)^{-N-1}),$$

其中 $B_j$（$0 \le j < \infty$）为第 $j$ 个 Bernoulli 数。

**推论。**当 $n \to \infty$ 时，$n\sum_{k=0}^\infty{}' 1/(n^2+(n+k)^2) \sim \frac{\pi}{4} + \sum_{k=0}^\infty \frac{(-1)^k B_{4k+2}}{(2k+1)2^{2k+2}n^{4k+2}}$（取 $m=n$）。

**状态：已证明**（在 Euler–Maclaurin 公式 (10.5) 中取 $a=0$、$b=\infty$、$f(x) = \{m^2+(n+x)^2\}^{-1}$）。数值复核：$m=n=5$、$N=2$ 时左端与右端差 $3.2\times 10^{-8}$（在余项 $O((m^2+n^2)^{-3}) \approx 8\times 10^{-6}$ 界内）。

**对照：** M02（Euler–Maclaurin 求和）、M01（Bernoulli 数）、M12（渐近展开）。

## 小结

本章共 **35 条 Entry（Entry 1–11、13–36；无 Entry 12）**，另含第 12 节的一道例题、Entry 1、13、17、19、21、30、31、32、34、36 的推论与 Entry 10 的推论 (i)(ii)、Entry 25 的例 (i)(ii)、Entry 27 的推论 (i)(ii)。按主题分三组：**积分求值**（Entry 1、4、5、9、13–16、19–23、26、29、30、33、34，约占一半，多为经典结果或拉马努金 [8] 的发表结果）；**渐近展开**（Entry 3、6、7、8、10、11、第 12 节例题、Entry 25 例 (i)、Entry 36，其中 Entry 7 与 Entry 10 为本章最难、最新的结果）；**求和公式**（Entry 2、17、18、24、27、28、31、32、35，以 Abel–Plana、Poisson 求和与 Euler–Maclaurin 为主线）。

与前几章不同，本轮数值复核（约 37 项，mpmath 30–50 位；初轮 23 项直接通过，其余 14 项经第二、三轮复核全部澄清）**未发现新的原书印文问题**：初轮的 14 项「失败」均为数值方法所致——振荡积分的求积误差（Entry 26、Entry 29、Entry 33 的直接求积）、可去奇点处的灾难性抵消（Entry 1 的 (1.1)，$x \to 0$ 时分子分母同趋于 $0$；Entry 33 在 $x=1$ 处）、慢收敛级数（Entry 11(iii) 的两对数级数，改用 (11.3) 复核后得 $1.000000044$）、渐近余项的量级（Entry 3 的 $O(r^{-7})$、Entry 7 (7.1) 的 $O(1)$ 项在 $m-n=2$ 时稳定在 $3.13$–$3.19$、Entry 11(i) 与第 12 节例题在 $x=20$ 时的相对差 $4.8\times 10^{-7}$ 与 $1.2\times 10^{-8}$），以及 mpmath 的 `euler(n)` 并非 Euler 数（Entry 16(iv) 的积分值 $1$、$5$ 与标准 Euler 数 $E_2=-1$、$E_4=5$ 一致）。其中 Entry 7 的 (7.3) 在 $m=300$、$n=100$ 时 $A_1+A_2+A_3+A_4$ 与 $I-S$ 之差仅 $1.6\times 10^{-9}$，Entry 33 奇情形的留数计算与右端公式逐位一致。

本章由 Berndt 本人指出的不成立或形式性断言有：Entry 24(ii) 的意图不明、其推论的等式一般不成立；Entry 24(iii) 的 (24.1) 一般不成立，推论 (i) 不成立，推论 (ii) (24.2) 仅在 $a = e^{i\alpha}$ 时成立；Entry 25(ii) 的两积分在 $a \ne 0$ 时发散（仅为形式公式），例 (i) 中拉马努金版的 $323.2a$ 有误；Entry 5 的另一形式论证会给出「错误」答案（奇数下标项缺失）；Entry 18(i) 拉马努金原文有两处误印；Entry 29 所引 Gradshteyn 与 Ryzhik 表 3.738 No. 2 的一个括号放错了位置。以上均已按 Berndt 的说明如实记录，未擅自改动原文。

## 待核对清单

1. IMSC 本章结果数（当日不可达，见前几章同项）。
2. Berndt 章首计数（本章导言未给出明确的公式或定理陈述总数，待核对原书目录）。
3. TIFR 影印版页码（除书中明引的拉马努金原文 p. 156（Entry 5）与 p. 159（Entry 18）外，其余条目的笔记位置待核对）。
4. Entry 32(ii) 的确切形式（书中仅一句话指为 Euler–Maclaurin (10.5) 的另一版本，未印公式）。
5. Entry 24(ii) 的意图（Berndt 明言 unclear；其推论等式已否定，见正文）。
6. Entry 24(iii) (24.1) 的有效实例范围（Boas–Pollard、Krishnan、Forrester 文献的具体结论）。
7. Entry 5 的 Hardy 定理条件细节（$\delta > \frac{1}{2}$ 的取法与 $A_{2s+1}$ 的增长性假设）。
8. Entry 18(i) 拉马努金原文（p. 159）的两处误印具体内容（Berndt 未逐字列出）。
9. Entry 25 例 (ii) 的 Euler–Maclaurin 版本确切表述（书中仅一句话提及）。
10. Entry 7 (7.1) 的 $O(1)$ 项的显式界（本书只给 $O(1)$；本轮数值显示 $m-n=2$ 时约为 $3.13$–$3.19$）。
11. Entry 21 例 (21.1)(21.2) 的 Poisson 求和推导细节（$\alpha\beta = \pi/4$ 情形的自反函数）。
12. Entry 2 (i)(ii)(iii) 的积分上下限（书中未印，按分部积分的不定积分形式理解；定积分版本待核对）。
13. Entry 13 推论 (13.2) 的分母 $r - ps/(q - r/p)$ 在 $q = r/p$ 时的退化情形（书中未讨论）。

## 来源说明

- 整理本：Bruce C. Berndt，《Ramanujan's Notebooks》，Part II，Springer，1989，Ch. 13，书页 185–239。
- 电子版：archive.org 标识符 `ramanujan_notebooks_ii`（《Ramanujan's Notebooks, Part 2》，Springer 1989，XII + 360 页，DOI 10.1007/978-1-4612-4530-8；PDF 14,538,056 字节、371 叶）；**PDF 页 = 书页 + 12**（与 Part I 的 +10 不同）。本章公式按 PDF 原图（150 DPI，书页 185–239，即 PDF 页 197–251）逐字转录；关键公式另用留数计算与数值复核交叉确认。OCR 公式损坏严重，凡与原图或数值不符者一律以原图为准。
- 原文层：Srinivasa Ramanujan，《Notebooks》（2 卷），Tata Institute of Fundamental Research，孟买，1957 年；2011 年 TIFR 再版两卷 Collector's Edition。拉马努金论文 [8]（Collected Papers [16]，pp. 53–58 的积分）与 [14]（含 Gamma 函数的积分）为本章多条目的原始出处；季报证明见 Part I，pp. 298–304、322、333。
- 数值复核：mpmath 30–50 位，约 37 项（另有 scipy 交叉核对 Entry 26(i)(ii) 的振荡积分）；慢收敛级数改用直接求和加解析尾项或 (11.3) 式复核；振荡积分的求积误差已在正文中注明。
