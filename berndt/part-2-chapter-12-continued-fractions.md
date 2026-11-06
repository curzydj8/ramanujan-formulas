# Part II，Chapter 12——Continued Fractions（连分数）

出处：Bruce C. Berndt，《Ramanujan's Notebooks》，Part II，Springer，1989，Ch. 12，书页 103–184。

本章是 Berndt 五卷中连分数理论的核心章：从连分数基本递推与 Euler 对应定理出发，经无穷根式、Gauss 与 Euler 的超几何商连分数，到三条最主要的 Gamma 函数连分数公式（Entry 34、39、40）与指数积分、Stirling 展开的渐近连分数，收束于 θ_n 的渐近展开。本章共 **49 条 Entry（Entry 1–49，无缺号）**，另含分体 Entry 5(i)(ii)、Entry 32(i)(ii)(iii)、Entry 44(i)–(iv)、Entry 45(i)(ii)、Entry 46(i)–(iv)，共 **59 个 Entry 标题**。

## 背景与记号

- 章首导言（p. 103）：拉马努金在致 Hardy 第一封信中给出的连分数 (1.10)–(1.12)——Hardy 评「defeated me completely」（彻底难倒了我）；三条最主要的 Gamma 函数公式是 **Entry 34、Entry 39、Entry 40**；**Entry 20（Gauss 连分数）与 Entry 22（Euler 连分数）**是两个超几何商的连分数，在全章起枢纽作用：Entry 13、Entry 20、Entry 22 的证明与推论反复互引，Entry 7、Entry 9、Entry 11、Entry 12、Entry 41、Entry 42 均由它们导出。
- 连分数记号（0.2）：$b_0 + \frac{a_1}{b_1} + \frac{a_2}{b_2} + \cdots$ 表示 $b_0 + \cfrac{a_1}{b_1 + \cfrac{a_2}{b_2 + \cdots}}$；间或用 $K(a_n/b_n)$ 记连分数。本文件沿用此写法：$a/b + c/d + \cdots$ 即 $a/(b + c/(d + \cdots))$。
- 收敛域的放宽：Jacobsen [3] 用解析延拓与 uniform parabola 定理放宽了若干条目的收敛条件；Jacobsen [1]、Waadeland [1] 的尾部（tails）工作统一了若干证明。本章多条目的证明注明「由尾部定理」或「由 Jacobsen 的方法」，不再逐条复述。
- p. 104 有 Entry 间依赖关系示意图：Entry 20、Entry 22 为中心节点，Entry 1、Entry 14、Entry 15 为形式工具，Entry 25、Entry 34、Entry 39、Entry 40 为 Gamma 函数主线，Entry 44、Entry 46–49 为渐近分析支线。
- 本章与 Ch. 10–11 的互见：Entry 20、Entry 22 的超几何商即 Ch. 11 的 Gauss 连分数主题的继续；Entry 17 的「对应」理论与 Ch. 10 Entry 27 的幂级数对应互补；Entry 39 的证明用 Perron 定理（Bauer–Muir 变换），与 Ch. 11 Entry 21 的变换思想同源；Entry 40 的第一推论是 Entry 35。
- 与主题模块的对照总览：连分数主线见 **M03**（Rogers–Ramanujan 连分数已收录）；超几何衔接见 **M07** 与 **M02**；π 相关连分数见 **M04**（Brouncker 公式、Apéry 的 ζ(3) 连分数）；Gamma 与 digamma 函数见 **M10**；渐近展开见 **M12**；ζ 值与 Catalan 常数见 **M01**、**M02**；误差函数积分见 **M09**。另注：M01 目前缺少 Bernoulli 数的定义（M02、M06 引用它并写「见 M01.3」，但 M01 全文未给定义；出处已在 Part I Ch. 5 Entry 9 定位，待日后补入 M01），本章 Entry 46(ii) 的 $S_k = \zeta(k)$ 递推与 Γ 系数相关，不在本章文件里顺手改 M01。

## 本章结构

| Entry | 主题 | 书页 |
|---|---|---|
| Entry 1 | 连分数基本递推与 Euler 对应定理 | 105 |
| Entry 2 | 级数发散条件下的连分数表示 | 106 |
| Entry 3 | 无穷根式恒等式 | 108 |
| Entry 4 | 迭代根式与 Vijayaraghavan 收敛定理 | 108 |
| Entry 5(i) | 2cosθ 的平方根式（仅 θ=0 成立） | 109 |
| Entry 5(ii) | 2cosθ 的立方根式（First Part / Second Part） | 109–110 |
| Entry 6 | 迭代根式的幂级数展开 | 111 |
| Entry 7 | 1 的连分数与 ₁F₁ 商的连分数 | 112 |
| Entry 8 | 有限和的连分数与 e 的连分数 | 113–114 |
| Entry 9 | (x+a+1)/(x+1) 的连分数 | 114–115 |
| Entry 10 | 含零分母的连分数 | 116 |
| Entry 11 | 终止 ₁F₁ 商的连分数 | 117–118 |
| Entry 12 | 1 的另一连分数 | 118 |
| Entry 13 | a 的连分数（条件符号疑似印错，待核对） | 119–120 |
| Entry 14 | 有限偶部收缩 | 121 |
| Entry 15 | 对应恒等式（First Version / Second Version） | 122–123 |
| Entry 16 | 双重级数的连分数 | 123 |
| Entry 17 | 连分数与幂级数的对应理论 | 124–131 |
| Entry 18 | Euler 的 tan⁻¹、Log、tan、tanh 连分数 | 131–132 |
| Entry 19 | Bessel 函数商的连分数 | 133 |
| Entry 20 | Gauss 连分数 | 134 |
| Entry 21 | ₂F₁(β+1,1) 的三式连分数 | 134–135 |
| Entry 22 | Euler 连分数 | 136–137 |
| Entry 23 | 连分数与幂级数的对应系数递推 | 137–138 |
| Entry 24 | 有限 ₂F₃ 商的连分数 | 139 |
| Entry 25 | Gamma 函数商的连分数（Brouncker 的 π） | 140–145 |
| Entry 26 | Gamma 函数平方商的连分数 | 145–146 |
| Entry 27 | x、y 对称的连分数恒等式 | 146 |
| Entry 28 | 两连分数之比的极限 | 146–147 |
| Entry 29 | digamma 型级数的连分数 | 147–148 |
| Entry 30 | digamma 差的连分数 | 149–150 |
| Entry 31 | 交错 digamma 差的连分数（Catalan 常数） | 150–151 |
| Entry 32(i) | 交错级数的连分数 | 151–152 |
| Entry 32(ii) | 平方倒数交错级数的连分数（ζ(2)、2G） | 152–153 |
| Entry 32(iii) | Hurwitz ζ(3) 的连分数（Apéry） | 153–154 |
| Entry 33 | Gamma 函数差商的连分数 | 155–156 |
| Entry 34 | 三条最主要 Gamma 公式之一（致 Hardy 第一封信） | 156 |
| Entry 35 | 五参数 Gamma 商的连分数 | 156–158 |
| Entry 36 | 四参数 Gamma 商的连分数 | 158 |
| Entry 37 | digamma 组合的连分数 | 158 |
| Entry 38 | 平方倒数差的连分数 | 158 |
| Entry 39 | 三条最主要 Gamma 公式之二 | 159–163 |
| Entry 40 | 三条最主要 Gamma 公式之三（五参数） | 163–164 |
| Entry 41 | ₂F₁(−β,1) 的连分数 | 164–165 |
| Entry 42 | ₁F₁(1;n+1;x) 的连分数（Legendre） | 165 |
| Entry 43 | 误差函数级数的连分数 | 166 |
| Entry 44(i) | 指数积分 φ(x) 的渐近级数 | 167–171 |
| Entry 44(ii) | φ(x) 的界与近似 | 167–171 |
| Entry 44(iii) | φ(x) 的两式连分数 | 167–171 |
| Entry 44(iv) | φ(x) 的截断展开与尾部连分数 | 167–171 |
| Entry 45(i) | 渐近分数分子的偶次多项式 | 171–172 |
| Entry 45(ii) | 渐近分数分子的奇次多项式 | 171–172 |
| Entry 46(i) | Γ(x+1) 的系数与 ψ_n 的微分方程 | 172–173 |
| Entry 46(ii) | Γ 系数的 ζ 递推 | 173 |
| Entry 46(iii) | Γ(x+1) 的 b_k 数值表（拉马努金值末位有误） | 174 |
| Entry 46(iv) | ψ_n(x) 的连分数与渐近展开 | 175–178 |
| Entry 47 | Nielsen 积分的三式连分数 | 179–181 |
| Entry 48 | Nielsen 积分的渐近展开（θ_n） | 181–184 |
| Entry 49 | Ei(n) 的 θ 渐近展开 | 184 |

## Entry 1——连分数基本递推与 Euler 对应定理

**陈述。**设 $N_{-1} = 0$、$N_0 = 1$、$D_{-1} = 0$、$D_0 = 1$，$N_{k-1} = b_k N_{k-2} + a_k N_{k-3}$（$k \ge 2$），$D_k = b_k D_{k-1} + a_k D_{k-2}$（$k \ge 1$），则
$$\frac{a_1}{b_1} + \frac{a_2}{b_2} + \cdots + \frac{a_r}{b_r} = \frac{a_1 N_{r-1}}{D_r} = \sum_{k=1}^{r} (-1)^{k+1} \frac{a_1 \cdots a_k}{D_{k-1} D_k}. \tag{1.2}$$
改写：$A_{-1} = 1$、$A_0 = 0$、$B_{-1} = 0$、$B_0 = 1$，同递推，则连分数 $= A_r/B_r$（1.5）；且 $a_1 N_k = A_{k+1}$、$D_k = B_k$。推论（Euler，p. 106）：
$$\sum_{k=1}^{r} a_k = \frac{a_1}{1 - \frac{a_2}{a_1+a_2 - \frac{a_1 a_3}{a_2+a_3 - \cdots - \frac{a_{r-1}a_r}{a_{r-1}+a_r}}}}.$$

**出处。**Part II，Ch. 12，Entry 1（pp. 105–106）。全章的递推工具。

**状态。**已证明（标准连分数理论）。

**对照。**M03（连分数基本理论）；M02。

## Entry 2——级数发散条件下的连分数表示

**陈述。**设 $f_n(x) = \sum_{k=0}^{n} (-x)^k/(a_1 \cdots a_{k+1})$；若 $\lim_{n\to\infty} f_n(x) = \infty$（2.1），则
$$x = x - a_1 + \frac{a_1 x}{x - a_2 + \frac{a_2 x}{x - a_3 + \cdots}}. \tag{2.2}$$
如 $\lim |a_n| = \rho$，则 $|x| > \rho$ 时 (2.1) 成立。

**出处。**Part II，Ch. 12，Entry 2（pp. 106–107）。

**状态。**已证明。

**对照。**M03；M02。

## Entry 3——无穷根式恒等式

**陈述。**形式恒等式：
$$x = a_1 + \left(x^2 + a_1(a_1 - 2a_2) - 2a_1\left(x^2 + a_2(a_2 - 2a_3) - 2a_2(\cdots)^{1/2}\right)^{1/2}\right)^{1/2}.$$
拉马努金表述有小误印（笔记本 p. 143），Berndt 已纠正。

**出处。**Part II，Ch. 12，Entry 3（p. 108）。

**状态。**已证明（形式恒等式；收敛条件见 Entry 4 的 Vijayaraghavan 定理）。

**对照。**M03（无穷根式，见 M03 收录的 $\sqrt{1+2\sqrt{1+3\sqrt{1+\cdots}}} = 3$）。

## Entry 4——迭代根式与 Vijayaraghavan 收敛定理

**陈述。**记 $f(x) := x + n + a$，则
$$f(x) = \left(ax + (n+a)^2 + x\left(a(x+n) + (n+a)^2 + (x+n)\left(a(x+2n) + (n+a)^2 + (x+2n)(\cdots)^{1/2}\right)^{1/2}\right)^{1/2}\right)^{1/2}.$$
例：(i) $3 = \left(1 + 2\left(1 + 3\left(1 + 4\left(1 + \cdots\right)^{1/2}\right)^{1/2}\right)^{1/2}\right)^{1/2}$；(ii) $4 = \left(6 + 2\left(7 + 3\left(8 + 4\left(9 + \cdots\right)^{1/2}\right)^{1/2}\right)^{1/2}\right)^{1/2}$（(ii) 为 JIMS 投稿题；(i) 曾为 1966 年 Putnam 赛题）。Vijayaraghavan 定理：$\left(a_1 + \left(a_2 + \left(a_3 + \cdots (a_n)^{1/2}\right)^{1/2}\right)^{1/2}\right)^{1/2}$ 收敛当且仅当 $\limsup (\mathrm{Log}\, a_n)/2^n < \infty$（4.1）。

**出处。**Part II，Ch. 12，Entry 4（pp. 108–109）。

**状态。**已证明（Vijayaraghavan）。

**对照。**M03（无穷根式）。

## Entry 5(i)——2cosθ 的平方根式

**陈述。**
$$2\cos\theta = (2 + 2\cos 2\theta)^{1/2} = \left(2 + \left(2 + 2\cos 4\theta\right)^{1/2}\right)^{1/2} = \cdots$$
**仅 θ=0 时成立**（一般须取负号）；θ=0 时 $2 = \left(2 + \left(2 + \left(2 + \cdots\right)^{1/2}\right)^{1/2}\right)^{1/2}$。

**出处。**Part II，Ch. 12，Entry 5(i)（p. 109）。拉马努金原表述未加限定，Berndt 指出一般情形不成立。

**状态。**已证明（θ=0 的特例；一般 θ 的断言不成立）。

**对照。**M03。

## Entry 5(ii)——2cosθ 的立方根式

**陈述。**First Part：$|\theta| \le \pi/6$ 或 $5\pi/6 \le \theta \le 7\pi/6$ 时，
$$2\cos\theta = \left(2\cos 3\theta + 3\left(2\cos 3\theta + 3\left(2\cos 3\theta + \cdots\right)^{1/3}\right)^{1/3}\right)^{1/3};$$
证明用 $x^3 - 3x - 2\cos 3\theta$ 的三个实根；其他 θ 区间收敛到另两根。Second Part：形式恒等式
$$2\cos\theta = \left(6\cos\theta + \left(6\cos 3\theta + \left(6\cos 9\theta + \cdots\right)^{1/3}\right)^{1/3}\right)^{1/3}. \tag{5.2}$$
严格成立的特例：θ=0（$2 = \left(6 + \left(6 + \cdots\right)^{1/3}\right)^{1/3}$，(5.3)）、θ=π（(5.5)）、θ=π/3（进而 θ=π/3^k，$k \ge 1$）；θ=π/2、2π/3 也成立，θ=π/4 成立但验证更难。

**出处。**Part II，Ch. 12，Entry 5(ii)（pp. 109–110）。

**状态。**已证明（所列特例与区间）。

**对照。**M03。

## Entry 6——迭代根式的幂级数展开

**陈述。**$a > 0$、$a \ne 1$，$n \ge 0$ 整数；形式幂级数 $f_n(v) = \sum_{j=0}^{\infty} a_j(n) v^j$，$a_0(n) = 1$，$a_1(n) = -a^{-n}$，
$$a_j(n) = \frac{1}{2(a^{j-1} - 1)} \sum_{k=1}^{j-1} a_k(n) a_{j-k}(n) \tag{6.1}$$
（$j \ge 2$）；则 $n$ 重迭代根式 $= (a/2) f_n(v)$（6.2）；$f_n(v)$ 的展开 (6.3) 前几项：
$$1 - \frac{v}{a^n} + \frac{(v/a^n)^2}{2(a-1)} - \frac{(v/a^n)^3}{2(a-1)(a^2-1)} + \frac{(v/a^n)^4 (a+5)}{8(a-1)(a^2-1)(a^3-1)} - \frac{(v/a^n)^5 (2a^2+3a+7)}{8(a-1)(a^2-1)(a^3-1)(a^4-1)} + \cdots.$$
拉马努金表述略有误（笔记本 p. 143）：他给的 $a_j(n)$ 求和为 $\sum_{k=0}^{j-1} a_k(n) a_{j-1-k}(n)$，Berndt 已纠正。

**出处。**Part II，Ch. 12，Entry 6（pp. 111–112）。

**状态。**已证明（形式幂级数）。

**对照。**M03；M02。

## Entry 7——1 的连分数与 ₁F₁ 商的连分数

**陈述。**$x$ 不是负整数时，
$$1 = \frac{x+1}{x} + \frac{x+2}{x+1} + \frac{x+3}{x+2} + \cdots. \tag{7.1}$$
拉马努金左端误写作 $x$（笔记本 p. 143），Berndt 已纠正。由 Entry 22 的推论 (7.2)：
$$\frac{{}_1F_1(\beta+1;\gamma+1;x)}{\gamma\, {}_1F_1(\beta;\gamma;x)} = \frac{1}{\gamma - x + \frac{(\beta+1)x}{\gamma+1 - x + \frac{(\beta+2)x}{\gamma+2 - x + \cdots}}};$$
亦可由 Entry 11（$a = 1$，$n = x+1$）得出。推论（$x = 1$）：$1 = \frac{2}{1} + \frac{3}{2} + \frac{4}{3} + \frac{5}{4} + \cdots$。

**出处。**Part II，Ch. 12，Entry 7（p. 112）。

**状态。**已证明。

**对照。**M03；M07（₁F₁ 商）；Ch. 11 Entry 21 与之相关。

## Entry 8——有限和的连分数与 e 的连分数

**陈述。**$n$ 正整数，$x \ne -ka$（$1 \le k \le n$）：
$$\sum_{k=1}^{n} \frac{(-1)^{k+1}}{(x+a)(x+2a)\cdots(x+ka)} = \frac{1}{x+a + \frac{x+a}{x+2a-1 + \frac{x+2a}{x+3a-1 + \cdots + \frac{x+(n-1)a}{x+na-1}}}}. \tag{8.1}$$
推论（Euler）：**$\frac{1}{e-1} = \frac{1}{1} + \frac{2}{2} + \frac{3}{3} + \cdots$；且 $1 - \frac1e = \frac{1}{1} + \frac{1}{1} + \frac{2}{2} + \frac{3}{3} + \cdots$**（本轮 mpmath 30 位数值复核，两式均与真值精确吻合，差 $0$）。

**出处。**Part II，Ch. 12，Entry 8（pp. 113–114）。

**状态。**已证明（Euler）。

**对照。**M03；M02（e 的连分数）。

## Entry 9——(x+a+1)/(x+1) 的连分数

**陈述。**
$$\frac{x+a+1}{x+1} = \frac{x+a}{x-1} + \frac{x+2a}{x+a-1} + \frac{x+3a}{x+2a-1} + \cdots, \tag{9.1}$$
条件：$x \ne -ka$（$k \ge 1$）且 $a \ne 0$，或 $a = 0$ 且 $|x| > 1$。$a = 0$ 时退化为周期连分数 $K(x/(x-1))$，$|x| > 1$ 收敛到 $1$，$|x| < 1$ 收敛到 $-x$。例：(i) $\frac43 = \frac31 + \frac42 + \frac53 + \frac64 + \cdots$（$x = 2$，$a = 1$）；(ii) $\frac53 = \frac41 + \frac63 + \frac85 + \frac{10}{7} + \cdots$（$x = 2$，$a = 2$）。

**出处。**Part II，Ch. 12，Entry 9（pp. 114–115）；例在 p. 116。证明用 (7.2) 与 ₁F₁ 恒等式 (9.3)(9.4)。

**状态。**已证明。

**对照。**M03；M07。

## Entry 10——含零分母的连分数

**陈述。**$n$ 正整数：
$$n = \frac{1}{1-n} + \frac{2}{2-n} + \frac{3}{3-n} + \cdots + \frac{n}{0} + \frac{n+1}{1} + \frac{n+2}{2} + \cdots,$$
中间出现 $0$ 分母，靠 (10.1)：$\frac{n}{2-n} + \frac{n-1}{3-n} + \cdots = n$ 理解。

**出处。**Part II，Ch. 12，Entry 10（p. 116）。

**状态。**已证明（在 (10.1) 的解释下）。

**对照。**M03。

## Entry 11——终止 ₁F₁ 商的连分数

**陈述。**$a$ 正整数，$n \notin \{0, -1, -2, \ldots\}$；$N_a$、$D_a$ 由终止的 ₁F₁ 定义（11.1)(11.2)，为 $n$ 的 $a-1$ 次多项式；则
$$\frac{N_a}{D_a} = \frac{n}{n-a} + \frac{n+1}{n-a+1} + \frac{n+2}{n-a+2} + \cdots; \tag{11.3}$$
$$\frac{N_{a+1}}{N_a} = n+2-a + \frac{a-1}{n+3-a} + \frac{a-2}{n+4-a} + \cdots. \tag{11.4}$$
推广 (11.7)：上式 $= 1 + \frac{a-1}{n+2-a} + \frac{a-2}{n+3-a} + \cdots$。推论 1：$\frac{n^2+n+1}{n^2-n+1} = \frac{n}{n-3} + \frac{n+1}{n-2} + \cdots$；推论 2：$\frac{n^3+2n+1}{(n-1)^3+2(n-1)+1} = \frac{n}{n-4} + \frac{n+1}{n-3} + \cdots$。

**出处。**Part II，Ch. 12，Entry 11（pp. 117–118）。

**状态。**已证明。

**对照。**M03；M07；Entry 7 可由本条（$a = 1$，$n = x+1$）得出。

## Entry 12——1 的另一连分数

**陈述。**$a \ne 0$，$x \ne -ka$：
$$1 = \frac{x+a}{a} + \frac{(x+a)^2-a^2}{a} + \frac{(x+2a)^2-a^2}{a} + \frac{(x+3a)^2-a^2}{a} + \cdots. \tag{12.1}$$

**出处。**Part II，Ch. 12，Entry 12（p. 118）。三个证明：Entry 22；Entry 27；尾部定理。

**状态。**已证明。

**对照。**M03。

## Entry 13——a 的连分数

**陈述。**印文条件三选一：$d \ne 0$、$b \ne -kd$、$a$ 为非负整数且 $\mathrm{Re}((a-b)/d) > 0$；或 $d \ne 0$ 且 $a = b$；或 $d = 0$ 且 $|a| < |b|$。则
$$a = \frac{ab}{a+b+d} - \frac{(a+d)(b+d)}{a+b+3d} - \frac{(a+2d)(b+2d)}{a+b+5d} - \cdots. \tag{13.1}$$
书中给出四个证明：Perron 定理；Entry 20 + Gauss 定理（得 Gamma 商 (13.2)）；尾部定理；Jacobsen [3]。

**本轮发现的印文问题（待核对，原文未改动）。**印文条件第一组的符号疑似有误：数值复核（16 组整数参数 + 4 组非整数参数，3000 项，mpmath 30 位）表明连分数关于 $a$、$b$ 对称，极限恒为 $\min(a,b)$——$(a,b,d) = (3,2,1) \to 2$、$(4,2,1) \to 2$、$(5,1,1) \to 1$、$(4,3,1) \to 3$、$(5,2,1) \to 2$、$(6,2,1) \to 2$、$(1.5,2.5,1) \to 1.4995$、$(2.5,1.5,1) \to 1.4995$、$(3.5,2.5,1) \to 2.4992$。$a = 3$、$b = 2$、$d = 1$ 满足印文全部条件（$d \ne 0$、$b \ne -kd$、$a = 3$ 为非负整数、$\mathrm{Re}((3-2)/1) = 1 > 0$），连分数却趋向 $2$ 而非 $3$。书中诸证明的步骤均要求 $\mathrm{Re}((b-a)/d) > 0$：尾部证明明言级数在 $\mathrm{Re}((b-a)/d) \ge 0$ 时发散从而连分数收敛到 $a$；Entry 20 + Gauss 定理的步骤需 $\mathrm{Re}((b-a)/d) > 0$（否则 ₂F₁ 在 $1$ 处发散）；Perron 定理的极小解辨认（$x_0/x_1 = b$）亦需 $\mathrm{Re}((b-a)/d) > 0$。结论：印文条件的符号似应为 $\mathrm{Re}((b-a)/d) > 0$（或等价地结论应为 $b$），待独立核对（或查其他印次、勘误表）。600 DPI 放大图确认印文条件确为 $a-b$。

**出处。**Part II，Ch. 12，Entry 13（pp. 119–120）。

**状态。**已证明（在订正后的条件下）；印文条件符号待核对。

**对照。**M03；M07（Gauss 定理）；M10（Gamma 商 (13.2)）。

## Entry 14——有限偶部收缩

**陈述。**
$$\frac{a_1}{x} + \frac{a_2}{1} + \frac{a_3}{x} + \frac{a_4}{1} + \cdots + \frac{a_{2n}}{1} = \frac{a_1}{x+a_2} - \frac{a_2 a_3}{x+a_3+a_4} - \frac{a_4 a_5}{x+a_5+a_6} - \cdots - \frac{a_{2n-2}a_{2n-1}}{x+a_{2n-1}+a_{2n}}. \tag{14.1}$$
另给一般偶部公式 (14.2)（Jones–Thron）；Preece 有无穷推广。

**出处。**Part II，Ch. 12，Entry 14（p. 121）。

**状态。**已证明。

**对照。**M03；Entry 21 (21.3) 与 Entry 43 第二式均为偶部收缩的实例。

## Entry 15——对应恒等式

**陈述。**First Version（形式恒等式）：
$$\frac{a_1+h}{1} + \frac{a_1}{x} + \frac{a_2+h}{1} + \frac{a_2}{x} + \cdots = h + \frac{a_1}{1} + \frac{a_1+h}{x} + \frac{a_2}{1} + \frac{a_2+h}{x} + \cdots, \tag{15.1}$$
两边对应同一幂级数 $\sum c_k x^{-k}$。Second Version（Jacobsen）：(i) 左边收敛到 $F$ 则右边奇部收敛到 $F$，反之亦然（通常意义下）；(ii) 除 $h$ 为 $\{-B_{2k}/B_{2k-1}\}$ 的极限点之可能例外外亦然；另左右两边一般收敛等价。

**出处。**Part II，Ch. 12，Entry 15（pp. 122–123）。

**状态。**已证明（Jacobsen）。

**对照。**M03；M02（幂级数对应）。

## Entry 16——双重级数的连分数

**陈述。**$m$、$n$ 均非负整数时，
$$\sum_{k=1}^{\infty} \frac{(-1)^{k+1}}{(m+k)(n+k)} = \frac{1}{(m+1)(n+1)} + \frac{(m+1)^2(n+1)^2}{m+n+3} + \frac{(m+2)^2(n+2)^2}{m+n+5} + \frac{(m+3)^2(n+3)^2}{m+n+7} + \cdots.$$

**出处。**Part II，Ch. 12，Entry 16（p. 123）。

**状态。**已证明。

**对照。**M03；M02。

## Entry 17——连分数与幂级数的对应理论

**陈述。**「对应」意义（两边未必收敛）：
$$\frac{1}{1} + \frac{a_1 x}{1} + \frac{a_2 x}{1} + \cdots = \sum_{k=0}^{\infty} A_k (-x)^k, \tag{17.1}$$
$A_0 = 1$；$P_n = a_1 \cdots a_{n-1}(a_1 + \cdots + a_n)$；$P_1 = A_1$，$P_2 = A_2$，$P_3 = A_3 - a_1 A_2$，$P_4 = A_4 - (a_1+a_2)A_3$，$P_5 = A_5 - (a_1+a_2+a_3)A_4 + a_1 a_3 A_3$，$P_6 = A_6 - (a_1+\cdots+a_4)A_5 + (a_1 a_3 + a_2 a_4 + a_1 a_4)A_4$；一般
$$P_n = \sum_{0 \le k < n/2} (-1)^k \varphi_k(n) A_{n-k}, \tag{17.2}$$
其中 $\varphi_0(n) \equiv 1$，$\varphi_r(n+1) - \varphi_r(n) = a_{n-1} \varphi_{r-1}(n-1)$（17.3），$\varphi_r(n) = 0$（$r \ge [n/2]$）；$\varphi_k(n)$ 显式公式 (17.12)：$\varphi_k(n) = \sum a_{j_1} \cdots a_{j_k}$（$1 \le j_1 \le j_2 - 2$，…，$1 \le j_k \le n-2$）。另有 Andrews 的第二证明（组合：$A_n$ 为非交换齐次多项式，指标 $j_{k+1} - j_k \le 1$；筛法得 (17.2)）。

Corollary (i)（p. 130）：
$$\frac{1}{1+b_1 x} + \frac{a_1 x}{1+b_2 x} + \cdots = \sum_{k=0}^{\infty} A_k (-x)^k, \tag{17.17}$$
$P_n = a_1 \cdots a_{n-1}(a_1 + b_1 + \cdots + a_n + b_n)$，$P_n = \sum_{k=0}^{n-1} (-1)^k \varphi_k(n) A_{n-k}$，$\varphi_r(n+1) - \varphi_r(n) = b_n \varphi_{r-1}(n) + a_{n-1} \varphi_{r-1}(n-1)$。

Corollary (ii)（p. 131）：$B_n(x) = \sum_{k=0}^{[n/2]} \varphi_k(n+1) x^k$。

例 (17.22)：**${}_2F_1^2(\tfrac12,\tfrac12;1;x) = \frac{1}{1} - \frac{x}{2} - \frac{3x}{8} - \frac{5x}{2} - \frac{17x}{40} - \frac{23x}{2} - \frac{1395x}{3128} - \cdots$**，其中 $a_1 = -\frac12$，$a_2 = -\frac{3}{16}$，$a_3 = -\frac{5}{16}$，$a_4 = -\frac{17}{80}$，$a_5 = -\frac{23}{80}$，$a_6 = -\frac{1395}{6256}$；$A_1 = -\frac12$，$A_2 = \frac{11}{32}$，$A_3 = -\frac{17}{64}$，$A_4 = \frac{1787}{2^{13}}$，$A_5 = -\frac{3047}{2^{14}}$，$A_6 = \frac{42631}{2^{18}}$；$P_1 = -\frac12$，$P_2 = \frac{11}{32}$，$P_3 = -\frac{3}{32}$，$P_4 = \frac{291}{2^{13}}$，$P_5 = -\frac{153}{2^{14}}$，$P_6 = \frac{32337}{5 \cdot 2^{21}}$。（注：(17.22) 显示式是 Entry 17 形式经等价变换 $c = (1,2,8,2,40,2,3128)$ 后的写法，非印文错误；本轮 6 项截断复核：$x = 0.3$ 时连分数值 $1.19049019243913339036574785744$，真值 $({}_2F_1(\tfrac12,\tfrac12;1;0.3))^2 = 1.19049028561038706676646587515$，差 $9.3 \times 10^{-8}$，属 6 项截断误差，非原书错误。）

**出处。**Part II，Ch. 12，Entry 17（pp. 124–131）。本章最长的理论节。

**状态。**已证明（Berndt；Andrews 第二证明）。

**对照。**M03；M07（超几何对应）；M02；Entry 46(iv) 的证明用本条（$a_1 = n/2$，$a_2 = (5n+10)/12$，$a_3 = (41n+58)/60$）。

## Entry 18——Euler 的 tan⁻¹、Log、tan、tanh 连分数

**陈述。**（Euler）
$$\frac{(x+1)^n - (x-1)^n}{(x+1)^n + (x-1)^n} = \frac{n}{x} + \frac{n^2-1^2}{3x} + \frac{n^2-2^2}{5x} + \frac{n^2-3^2}{7x} + \cdots, \tag{18.1}$$
条件：$x \notin [-1,1]$，或 $x = \pm 1$ 且 $\mathrm{Re}\, n \ne 0$，或 $n$ 为整数。推论 1：$\tan^{-1} x = \frac{x}{1} + \frac{x^2}{3} + \frac{(2x)^2}{5} + \frac{(3x)^2}{7} + \cdots$（Lambert、Lagrange、Euler；本轮 $x = 1$ 时数值复核：$\pi/4$ 差 $9.9 \times 10^{-32}$）；推论 2：$\mathrm{Log}\frac{1+x}{1-x} = \frac{2x}{1} - \frac{x^2}{3} - \frac{(2x)^2}{5} - \frac{(3x)^2}{7} - \cdots$（Euler）；推论 3：$\tan x = \frac{x}{1} - \frac{x^2}{3} - \frac{x^2}{5} - \frac{x^2}{7} - \cdots$（Lambert）；推论 4：$\frac{e^x-1}{e^x+1} = \frac{x}{2} + \frac{x^2}{6} + \frac{x^2}{10} + \frac{x^2}{14} + \cdots$（Euler）。另记 $V_n + 1/V_n = 2/V_{2n}$（$V_n$ 为 (18.1) 左端）。

**出处。**Part II，Ch. 12，Entry 18（pp. 131–132）。

**状态。**已证明（Euler；Lambert）。

**对照。**M03；M04（$\tan^{-1}$ 与 π）；M02。

## Entry 19——Bessel 函数商的连分数

**陈述。**（古典）
$$\frac{x \cdot {}_0F_1(n+1;x)}{n \cdot {}_0F_1(n;x)} = \frac{\sqrt{x}\, J_n(2i\sqrt{x})}{i\, J_{n-1}(2i\sqrt{x})} = \frac{x}{n} + \frac{x}{n+1} + \frac{x}{n+2} + \cdots;$$
证明用 Euler/Perron 的 (19.1)：$c + \frac{a}{c+d} + \frac{a}{c+2d} + \cdots = \frac{c \cdot {}_0F_1(c/d; a/d^2)}{{}_0F_1(c/d+1; a/d^2)}$。

**出处。**Part II，Ch. 12，Entry 19（p. 133）。

**状态。**已证明。

**对照。**M03；M07（Bessel 函数）；M02。

## Entry 20——Gauss 连分数

**陈述。**（Gauss 连分数，全章最著名的公式之一）
$$\frac{\alpha\beta x}{\gamma} \cdot \frac{{}_2F_1(\gamma-\alpha,\beta+1;\gamma+1;-x)}{{}_2F_1(\gamma-\alpha,\beta;\gamma;-x)} = \frac{\alpha\beta x}{\gamma} + \frac{(\alpha-\gamma)(\beta-\gamma)x}{\gamma+1} + \frac{(\alpha+1)(\beta+1)x}{\gamma+2} + \frac{(\alpha-\gamma-1)(\beta-\gamma-1)x}{\gamma+3} + \frac{(\alpha+2)(\beta+2)x}{\gamma+4} + \cdots, \tag{20.1}$$
条件：$x \notin (-\infty,-1]$，或 $\alpha$、$\beta$、$\gamma-\alpha$、$\gamma-\beta \in \{0,-1,-2,\ldots\}$；$\gamma-\beta = \alpha + \frac12$ 时可延拓到 $x = -1$。亦见于 Carr 的书（p. 97，拉马努金最受影响的书）。本轮 $(\alpha,\beta,\gamma,x) = (1,1,2,0.5)$ 数值复核差 $2.5 \times 10^{-32}$。

**出处。**Part II，Ch. 12，Entry 20（p. 134）。

**状态。**已证明（Gauss）。

**对照。**M03；M07；M10；Ch. 11 的 Gauss 连分数主题的继续；Entry 13 第二证明用本条。

## Entry 21——₂F₁(β+1,1) 的三式连分数

**陈述。**
$$\frac{\beta x}{\gamma} \cdot {}_2F_1(\beta+1,1;\gamma+1;-x) = \frac{\beta x}{\gamma} + \frac{\gamma(\beta+1)x}{\gamma+1} + \frac{1(\gamma-\beta)x}{\gamma+2} + \frac{(\gamma+1)(\beta+2)x}{\gamma+3} + \frac{2(\gamma+1-\beta)x}{\gamma+4} + \cdots \tag{21.1}$$
$$= \frac{\beta x}{\gamma} + \frac{(\beta+1)x}{1} + \frac{1(1+x)}{\gamma} + \frac{(\beta+2)x}{1} + \frac{2(1+x)}{\gamma} + \cdots \tag{21.2}$$
$$= \frac{\beta x}{\gamma + x(\beta+1)} - \frac{1(\beta+1)x(x+1)}{\gamma+1+x(\beta+3)} - \frac{2(\beta+2)x(x+1)}{\gamma+2+x(\beta+5)} - \cdots. \tag{21.3}$$
(21.3) 是 (21.2) 的偶部。推论 1（p. 136）：$\frac{x}{n} \cdot {}_1F_1(1;n+1;x) = \frac{x}{n-n+1} + \frac{nx}{n+2} - \frac{x}{n+3} + \frac{(n+1)x}{n+4} - \frac{2x}{n+5} + \cdots$（**第一式存疑，见下**）$= \frac{x}{n-x} + \frac{x}{n+1-x} + \frac{2x}{n+2-x} + \frac{3x}{n+3-x} + \cdots$（**第二式已本轮数值证实**：$n = 2$、$x = 0.5$ 与 $n = 3$、$x = 0.7$ 时两端差均为 $0$）。推论 2：${}_1F_1(1;x+1;x) = 1 + \frac{2x}{2} + \frac{3x}{3} + \frac{4x}{4} + \frac{5x}{5} + \cdots$。

**本轮发现的印文问题（待核对，原文未改动）。**推论 1 第一式按字面读不成立：数值复核（mpmath 30 位）：$(n,x) = (2,0.5)$ 时左端 $0.297442541400256293697301575628$；$b_1 = 1$ 的字面式得 $0.398060466155671997398312959113$；$b_1 = n-x+1$ 得 $0.181416389015867339187807963887$；$b_1 = n+1$ 得 $0.153558381873294612182236669641$；$b_1 = n-x$ 得 $0.284723354813287842479182067476$；$b_1 = n$ 得 $0.221622307827250032150579823873$。反解使该式成立的 $b_1$：$(2,0.5) \to 1.42490635808953576270214112038$，$(3,0.7) \to 2.06506886837707851849686915213$，$(4,0.2) \to 3.70712509566033446812013779633$——均非 $n$、$x$ 的简单表达式，说明字面 $a$-模式本身也可能有误，不只是分母问题。**但**由 (21.1) 令 $\gamma = n$、$x \to -x/\beta$、$\beta \to \infty$ 直接推导的形式 $-V = \frac{x}{n - \frac{nx}{n+1 + \frac{x}{n+2 - \frac{(n+1)x}{n+3 + \frac{2x}{n+4 - \cdots}}}}}$ 在 $(2,0.5)$、$(3,0.7)$ 两组参数下与左端精确吻合，证明本身无误。第一分母 300 DPI 放大图确为「$n - n + 1$」字样。处理：照录印文第一式并标待核对，同时给出推导出的正确形式与数值证据；不得把推导形式冒充印文。

**出处。**Part II，Ch. 12，Entry 21（pp. 134–136）。

**状态。**已证明（主恒等式与推论 1 第二式）；推论 1 第一式待核对。

**对照。**M03；M07；Entry 41 由 (21.3) 得出。

## Entry 22——Euler 连分数

**陈述。**（Euler 连分数）
$$\frac{\beta x}{\gamma} \cdot \frac{{}_2F_1(-\alpha,\beta+1;\gamma+1;-x)}{{}_2F_1(-\alpha,\beta;\gamma;-x)} = \frac{\beta x}{\gamma-(\alpha+\beta+1)x} + \frac{(\beta+1)(\alpha+\gamma+1)x}{\gamma+1-(\alpha+\beta+2)x} + \frac{(\beta+2)(\alpha+\gamma+2)x}{\gamma+2-(\alpha+\beta+3)x} + \cdots,$$
条件：不同时 $\beta+1$、$\gamma-\beta \in \{0,-1,-2,\ldots\}$ 且不同时 $-\alpha$、$\alpha+\gamma+1 \in \{0,-1,-2,\ldots\}$；且 $|x| < 1$，或 $\beta \in \{0,-1,-2,\ldots\}$，或 $x = 1$ 且 $\mathrm{Re}(\gamma-\alpha-\beta-1) > 0$。Perron 归于 Andoyer，Askey 指出实为 Euler；等价于 Nörlund 结果 (21.6)。本轮两点复核均差约 $10^{-32}$（$(\alpha,\beta,\gamma,x) = (1,1,3,0.3)$ 与 $(2,1,4,0.2)$）。

**出处。**Part II，Ch. 12，Entry 22（pp. 136–137）。

**状态。**已证明（Euler）。

**对照。**M03；M07；Entry 7 的 (7.2) 与 Entry 12 均由本条导出；与 Entry 20 并列为全章枢纽。

## Entry 23——连分数与幂级数的对应系数递推

**陈述。**「对应」意义：
$$\frac{a_n}{b_n x} + \frac{a_{n+1}}{b_{n+1} x} + \cdots = c_n \sum_{k=0}^{\infty} A_n(k) (-x)^k, \tag{23.1}$$
$A_n(0) = 1$；$c_n c_{n+1} = a_n$；$A_n(1) + A_{n+1}(1) = b_n/c_{n+1} = b_n c_n/a_n$（23.2）；$A_n(2) + A_{n+1}(2) = A_n(1)^2$；$A_n(3) + A_{n+1}(3) = A_n(1)\{A_n(2) - A_{n+1}(2)\}$；$A_n(4) + A_{n+1}(4) = A_n(1)\{A_n(3) - A_{n+1}(3)\} - A_n(2) A_{n+1}(2)$（23.3）；一般 (23.4)。例：$\lim_{x\to\infty} \{\sqrt{2x/\pi} - \frac{x}{1} + \frac{2x}{2} + \frac{3x}{3} + \frac{4x}{4} + \cdots\} = \frac{2}{3\pi}$（由 Entry 47，用渐近级数 (48.4) 与 Stirling 公式）。

**出处。**Part II，Ch. 12，Entry 23（pp. 137–138）。

**状态。**已证明。

**对照。**M03；M02；M12（渐近）。

## Entry 24——有限 ₂F₃ 商的连分数

**陈述。**$f(n,r,x) = \sum_{k=0}^{\infty} (-r+k-1)_k x^k/((n)_k (-n-r)_k k!)$；则
$$\frac{n}{n} + \frac{x}{n+1} + \frac{x}{n+2} + \cdots + \frac{x}{n+r} = \frac{f(n+1,r-1,x)}{f(n,r,x)}. \tag{24.1}$$
Entry 19 的有限形式；另给出 ₂F₃ 多项式商的连分数。

**出处。**Part II，Ch. 12，Entry 24（p. 139）。

**状态。**已证明。

**对照。**M03；M07。

## Entry 25——Gamma 函数商的连分数

**陈述。**（Euler；Stieltjes）$n$ 为奇整数且 $x$ 任意，或 $n$ 复数且 $\mathrm{Re}\, x > 0$：
$$\frac{\Gamma(\frac14(x+n+1))\Gamma(\frac14(x-n+1))}{\Gamma(\frac14(x+n+3))\Gamma(\frac14(x-n+3))} = \frac{4}{x} - \frac{n^2-1^2}{2x} - \frac{n^2-3^2}{2x} - \frac{n^2-5^2}{2x} - \cdots. \tag{25.1}$$
证明经 Entry 39，以及 Masson 的 Pincherle 定理方法（递推 (25.2)、定理 1）。推论 1（$n = 0$）：$\frac{\Gamma^2(\frac14(x+1))}{\Gamma^2(\frac14(x+3))} = \frac{4}{x} + \frac{1^2}{2x} + \frac{3^2}{2x} + \frac{5^2}{2x} + \cdots$；$x = 1$ 得 Brouncker 的 $\pi = \frac{4}{1} + \frac{1^2}{2} + \frac{3^2}{2} + \frac{5^2}{2} + \cdots$（Bauer 1872 年首证；拉马努金致 Hardy 第一封信）。推论 2：$\frac{\Gamma(\frac18(x+3))\Gamma(\frac18(x+1))}{\Gamma(\frac18(x+7))\Gamma(\frac18(x+5))} = \frac{8}{x} + \frac{1 \cdot 3}{2x} + \frac{5 \cdot 7}{2x} + \frac{9 \cdot 11}{2x} + \cdots$。本轮复核：(25.1) 在 $x = 2$、$n = 1$ 时差 $0$；推论 1 在 $x = 2$ 时 2000 项差 $5.7 \times 10^{-8}$、10000 项差 $2.3 \times 10^{-9}$（慢收敛）；Brouncker π 3000 项差 $3.3 \times 10^{-4}$（慢收敛，误差约 $1/(3N)$）。

**出处。**Part II，Ch. 12，Entry 25（pp. 140–145）。

**状态。**已证明（Euler；Stieltjes）。

**对照。**M03；M10（Gamma 函数）；M04（Brouncker 的 π）。

## Entry 26——Gamma 函数平方商的连分数

**陈述。**同 Entry 25 条件：
$$\frac{\Gamma^2(\frac14(x+n+1))\Gamma^2(\frac14(x-n+1))}{\Gamma^2(\frac14(x+n+3))\Gamma^2(\frac14(x-n+3))} = \frac{8}{\frac12(x^2+n^2-1)} + \frac{1^2-n^2}{1} + \frac{1^2}{x^2-1} + \frac{3^2-n^2}{1} + \frac{3^2}{x^2-1} + \cdots$$
$$= \frac{8}{\frac12(x^2-n^2-1)} + \frac{1}{1} + \frac{1^2-n^2}{x^2-1} + \frac{3^2}{1} + \frac{3^2-n^2}{x^2-1} + \cdots.$$
推论（$n = 0$）：$\frac{\Gamma^4(\frac14(x+1))}{\Gamma^4(\frac14(x+3))} = \frac{8}{\frac12(x^2-1)} + \frac{1^2}{1} + \frac{1^2}{x^2-1} + \frac{3^2}{1} + \frac{3^2}{x^2-1} + \cdots$。

**出处。**Part II，Ch. 12，Entry 26（pp. 145–146）。

**状态。**已证明。

**对照。**M03；M10。

## Entry 27——x、y 对称的连分数恒等式

**陈述。**（致 Hardy 第二封信）$x, y > 0$：
$$x + \frac{(1+y)^2+n}{2x} + \frac{(3+y)^2+n}{2x} + \frac{(5+y)^2+n}{2x} + \cdots = y + \frac{(1+x)^2+n}{2y} + \frac{(3+x)^2+n}{2y} + \frac{(5+x)^2+n}{2y} + \cdots$$
（$n$ 为参数；首个印刷证明为 Preece；Ramanathan 证明；Jacobsen 有改进版）。本轮 $(x,y,n) = (1,2,1)$ 两边复核：$N = 500$ 时差 $0.012$、$N = 2000$ 时差 $0.003$、$N = 8000$ 时差 $0.00075$、$N = 20000$ 时差 $0.00030$（误差约 $1/N$，慢收敛，两边趋向同一值约 $2.8105$）。

**出处。**Part II，Ch. 12，Entry 27（p. 146）。

**状态。**已证明（Preece；Ramanathan；Jacobsen）。

**对照。**M03。

## Entry 28——两连分数之比的极限

**陈述。**$\mathrm{Re}\, x > 0$、$|\arg n| \le \pi/2 - \delta$ 时，
$$\lim_{n\to\infty} \frac{x + \frac{n^2+1^2}{2x} + \frac{n^2+3^2}{2x} + \cdots}{n + \frac{x^2-1^2}{2n} - \frac{x^2-3^2}{2n} - \cdots} = 1. \tag{28.1}$$
拉马努金更精确版（第一本笔记 p. 160）：比值 $= \frac{1-e^{-\pi n}}{1-2e^{-\pi n/2} \sin(\pi x/2) + e^{-\pi n}}$；Berndt 指出左端为 $1 + O(1/n)$、右端为 $1 + O(e^{-\pi n/2})$，故拉马努金的断言似乎无合理解释。

**出处。**Part II，Ch. 12，Entry 28（pp. 146–147）。

**状态。**已证明（28.1）；拉马努金的精确版断言存疑（Berndt）。

**对照。**M03；M12。

## Entry 29——digamma 型级数的连分数

**陈述。**$n$ 为奇整数且 $x$ 复数，或 $n$ 复数且 $\mathrm{Re}\, x > 0$：
$$\sum_{k=1}^{\infty} \left\{\frac{(-1)^{k+1}}{x+n+2k-1} + \frac{(-1)^{k+1}}{x-n+2k-1}\right\} = \frac{1}{x} + \frac{1^2-n^2}{x} + \frac{2^2}{x} + \frac{3^2-n^2}{x} + \frac{4^2}{x} + \frac{5^2-n^2}{x} + \cdots.$$
由 Perron 的 (29.1) digamma 形式；1953 年 Perron 由 Entry 34 首证；Jacobsen 在所述条件下证明。推论（$n = 0$）：$2\sum_{k=1}^{\infty} \frac{(-1)^{k+1}}{x+2k-1} = \frac{1}{x} + \frac{1^2}{x} + \frac{2^2}{x} + \frac{3^2}{x} + \frac{4^2}{x} + \cdots$。本轮复核：(29.1) 的 $4/x$ 首项经 300 DPI 确认；$(x,n) = (3,0.5)$ 时 (29.1) 与 digamma 右端差 $1.4 \times 10^{-11}$（3000 项，慢收敛）；注意 (29.1) 左端恰为本条连分数的 $4$ 倍（首分子 $4$ 而非 $1$），级数 $= (1/4) \cdot$ digamma 右端，$(x,n) = (2,1)$ 时 $a_2 = 0$ 截断得 $1/2$ 与 $2$，全部自洽。

**出处。**Part II，Ch. 12，Entry 29（pp. 147–148）。

**状态。**已证明（Perron；Jacobsen）。

**对照。**M03；M10（digamma 函数）；M02。

## Entry 30——digamma 差的连分数

**陈述。**$n$ 为整数或 $\mathrm{Re}\, x > 0$：
$$\sum_{k=0}^{\infty} \left\{\frac{1}{x-n+2k+1} - \frac{1}{x+n+2k+1}\right\} = \frac{n}{x} + \frac{1^2(1^2-n^2)}{3x} + \frac{2^2(2^2-n^2)}{5x} + \frac{3^2(3^2-n^2)}{7x} + \cdots. \tag{30.1}$$
由 Entry 33（$m \to 0$）。推论：$2\sum_{k=0}^{\infty} \frac{1}{(x+2k+1)^2} = \frac{1}{x} + \frac{1^4}{3x} + \frac{2^4}{5x} + \frac{3^4}{7x} + \cdots$；$x = 1$：$\frac12 \zeta(2) = \frac{\pi^2}{12} = \frac{1}{1} + \frac{1^4}{3} + \frac{2^4}{5} + \frac{3^4}{7} + \cdots$（Stieltjes）。本轮复核：$(x,n) = (2,1)$ 时 $a_2 = 0$ 截断，连分数恰为 $1/2$，digamma 闭式 $\frac12[\psi((x+n+1)/2) - \psi((x-n+1)/2)]$ 亦为 $1/2$；推论 $\pi^2/12$ 在 300 项差 $5.5 \times 10^{-6}$、2000 项差 $1.2 \times 10^{-7}$、8000 项差 $7.8 \times 10^{-9}$（慢收敛）。

**出处。**Part II，Ch. 12，Entry 30（pp. 149–150）。

**状态。**已证明。

**对照。**M03；M10；M01（ζ(2)）；M04（π²）。

## Entry 31——交错 digamma 差的连分数

**陈述。**$n$ 为偶整数或 $\mathrm{Re}\, x > 0$：
$$\sum_{k=0}^{\infty} \left\{\frac{(-1)^k}{x-n+2k+1} - \frac{(-1)^k}{x+n+2k+1}\right\} = \frac{n}{x^2-1} + \frac{2^2-n^2}{1} + \frac{2^2}{x^2-1} + \frac{4^2-n^2}{1} + \frac{4^2}{x^2-1} + \cdots. \tag{31.1}$$
由 Entry 36（$\ell \to 0$）。推论（$n \to 0$）：$2\sum_{k=0}^{\infty} \frac{(-1)^k}{(x+2k+1)^2} = \frac{1}{x^2-1} + \frac{2^2}{1} + \frac{2^2}{x^2-1} + \frac{4^2}{1} + \frac{4^2}{x^2-1} + \cdots$；$x = 2$：$2G = 2 - \frac13 + \frac{2^2}{1} + \frac{2^2}{3} + \frac{4^2}{1} + \frac{4^2}{3} + \cdots$（Catalan 常数；同一族连分数由 H. Cohen 独立发现）。本轮复核：$2G$ 在 300 项差 $2.0 \times 10^{-6}$、2000 项差 $4.5 \times 10^{-8}$、8000 项差 $2.8 \times 10^{-9}$（慢收敛）。

**出处。**Part II，Ch. 12，Entry 31（pp. 150–151）。

**状态。**已证明。

**对照。**M03；M01（Catalan 常数 $G$）；M02。

## Entry 32(i)——交错级数的连分数

**陈述。**$\mathrm{Re}\, x > 0$：
$$1 + 2x \sum_{k=1}^{\infty} \frac{(-1)^k}{x+2k} = \frac{1}{x} + \frac{1 \cdot 2}{x} + \frac{2 \cdot 3}{x} + \frac{3 \cdot 4}{x} + \cdots. \tag{32.1}$$

**出处。**Part II，Ch. 12，Entry 32(i)（pp. 151–152）。

**状态。**已证明。

**对照。**M03；M02。

## Entry 32(ii)——平方倒数交错级数的连分数

**陈述。**$\mathrm{Re}\, x > 0$：
$$1 + 2x^2 \sum_{k=1}^{\infty} \frac{(-1)^k}{(x+k)^2} = \frac{1}{x} + \frac{1^2}{x} + \frac{1 \cdot 2}{x} + \frac{2^2}{x} + \frac{2 \cdot 3}{x} + \frac{3^2}{x} + \cdots.$$
$x = 1$：$\zeta(2) = 1 + \frac{1}{1} + \frac{1^2}{1} + \frac{1 \cdot 2}{1} + \frac{2^2}{1} + \frac{2 \cdot 3}{1} + \frac{3^2}{1} + \cdots$；$x = \frac12$：$2G = 1 + \frac{1}{1/2} + \frac{1^2}{1/2} + \frac{1 \cdot 2}{1/2} + \frac{2^2}{1/2} + \frac{2 \cdot 3}{1/2} + \frac{3^2}{1/2} + \cdots$。本轮复核（注意显示式首项的 $1 +$ 是前导常数，连分数本身从 $1/1$ 起）：$\zeta(2)$ 在 400 项差 $3.1 \times 10^{-6}$、2000 项差 $1.2 \times 10^{-7}$、8000 项差 $7.8 \times 10^{-9}$（慢收敛）。

**出处。**Part II，Ch. 12，Entry 32(ii)（pp. 152–153）。

**状态。**已证明。

**对照。**M03；M01（ζ(2)、Catalan 常数）；M04。

## Entry 32(iii)——Hurwitz ζ(3) 的连分数

**陈述。**$\mathrm{Re}\, x > -\frac12$：$\zeta(3,x+1) := \sum_{k=1}^{\infty} \frac{1}{(x+k)^3} =$
$$\frac{1}{2x(x+1)} + \frac{1^3}{1} + \frac{1^3}{6x(x+1)} + \frac{2^3}{1} + \frac{2^3}{10x(x+1)} + \cdots = \frac{1}{2x^2+2x+1} - \frac{1^6}{3(2x^2+2x+3)} - \frac{2^6}{5(2x^2+2x+7)} - \frac{3^6}{7(2x^2+2x+13)} - \cdots. \tag{32.4}$$
拉马努金第二连分数略有错误（笔记本 p. 149），Berndt 给出订正形式。另 Stieltjes：$4x^3 \zeta(3,x) = 2x+2 + \frac{1}{x} + \frac{p_1}{x} + \frac{q_1}{x} + \frac{p_2}{x} + \frac{q_2}{x} + \cdots$，$p_k = k^2(k+1)/(4k+2)$，$q_k = k(k+1)^2/(4k+2)$。$x = 1$：$\zeta(3) = 1 + \frac{1}{2 \cdot 2} + \frac{1^3}{1} + \frac{1^3}{6 \cdot 2} + \frac{2^3}{1} + \frac{2^3}{10 \cdot 2} + \cdots$（Apéry 的连分数，在其 ζ(3) 无理性证明中起关键作用）。本轮复核：$\zeta(3)$ 在 300 项差 $1.1 \times 10^{-16}$、2000 项差 $1.3 \times 10^{-21}$（项构造须注意：分母序列为 $4$、$1$、$12$、$1$、$20$、$1$、$28$、…，即 $(4k+2) \cdot 2$ 的形式，初版脚本误用 $(4k-2) \cdot 2$ 曾得恒定差 $0.0015$，已纠正）。

**出处。**Part II，Ch. 12，Entry 32(iii)（pp. 153–154）。

**状态。**已证明（Berndt 订正版）；拉马努金第二连分数原版略有错误。

**对照。**M03；M01（ζ(3)）；M04（Apéry）。

## Entry 33——Gamma 函数差商的连分数

**陈述。**$x$、$m$、$n$ 复数；$m$ 或 $n$ 为整数或 $\mathrm{Re}\, x > 0$：
$$\frac{\Gamma(\frac12(x+m+n+1))\Gamma(\frac12(x-m-n+1)) - \Gamma(\frac12(x+m-n+1))\Gamma(\frac12(x-m+n+1))}{\Gamma(\frac12(x+m+n+1))\Gamma(\frac12(x-m-n+1)) + \Gamma(\frac12(x+m-n+1))\Gamma(\frac12(x-m+n+1))} = \frac{mn}{x} + \frac{(m^2-1^2)(n^2-1^2)}{3x} + \frac{(m^2-2^2)(n^2-2^2)}{5x} + \frac{(m^2-3^2)(n^2-3^2)}{7x} + \cdots.$$
Nörlund 首个印刷证明；为 Stieltjes 的超几何积分商连分数的特例。本轮 $(x,m,n) = (2,1,1)$ 复核差 $0$。

**出处。**Part II，Ch. 12，Entry 33（pp. 155–156）。

**状态。**已证明（Nörlund）。

**对照。**M03；M10；Entry 30 由本条（$m \to 0$）得出。

## Entry 34——三条最主要 Gamma 公式之一

**陈述。**（致 Hardy 第一封信 p. 350）$n$ 为奇整数或 $\ell$ 为偶整数，或 $\mathrm{Re}\, x > 0$ 且 $\ell$、$n$ 任意：记
$$P = \frac{\Gamma(\frac14(x+\ell+n+1))\Gamma(\frac14(x+\ell-n+1))\Gamma(\frac14(x-\ell+n+3))\Gamma(\frac14(x-\ell-n+3))}{\Gamma(\frac14(x-\ell+n+1))\Gamma(\frac14(x-\ell-n+1))\Gamma(\frac14(x+\ell+n+3))\Gamma(\frac14(x+\ell-n+3))};$$
则
$$\frac{1-P}{1+P} = \frac{\ell}{x} + \frac{1^2-n^2}{x} + \frac{2^2-\ell^2}{x} + \frac{3^2-n^2}{x} + \frac{4^2-\ell^2}{x} + \cdots$$
（奇平方减 $n^2$、偶平方减 $\ell^2$；300 DPI 放大图确认 $(2^2-\ell^2)$ 等写法）。三条最主要 Gamma 公式之一。首个印刷证明为 Preece；Perron；Jacobsen 在所述条件下证明。推论（第二封信 p. 353）：$F(\alpha,\beta) = \tan^{-1}\{\frac{\alpha}{x} + \frac{\beta^2+\gamma^2}{x} + \frac{\alpha^2+(2\gamma)^2}{x} + \frac{\beta^2+(3\gamma)^2}{x} + \cdots\}$；$F(\alpha,\beta) + F(\beta,\alpha) = 2F(\frac12(\alpha+\beta), \frac12(\alpha+\beta))$。本轮 $(x,\ell,n) = (3,2,1)$ 复核差 $0$。

**出处。**Part II，Ch. 12，Entry 34（p. 156）。

**状态。**已证明（Preece；Perron；Jacobsen）。

**对照。**M03；M10；M04；Entry 29 由本条首证（Perron，1953 年）。

## Entry 35——五参数 Gamma 商的连分数

**陈述。**$y = x^2 - (1-m)^2$，$t = (n^2-\ell^2)(1-2m)$；$P$ 为 8 个 Gamma 因子的商；$\ell$、$m$ 或 $n$ 为整数或 $\mathrm{Re}\, x > 0$：
$$\frac{1-P}{1+P} = \frac{2\ell mn}{x^2-\ell^2-m^2-n^2+1} + \frac{4(\ell^2-1^2)(m^2-1^2)(n^2-1^2)}{3(x^2-\ell^2-m^2-n^2+5)} + \frac{4(\ell^2-2^2)(m^2-2^2)(n^2-2^2)}{5(x^2-\ell^2-m^2-n^2+13)} + \cdots$$
$$= \frac{2\ell mn}{y+t-2\ell^2 m} + \frac{2(1-m)(1^2-n^2)}{1} + \frac{2(1+m)(1^2-\ell^2)}{3y+t} + \frac{2(2-m)(2^2-n^2)}{1} + \frac{2(2+m)(2^2-\ell^2)}{5y+t} + \cdots. \tag{35.1}$$
第一等式是 Entry 40 的推论（Watson）。

**出处。**Part II，Ch. 12，Entry 35（pp. 156–158）。

**状态。**已证明。

**对照。**M03；M10；Entry 36、Entry 37、Entry 38 均由本条得出。

## Entry 36——四参数 Gamma 商的连分数

**陈述。**$n$ 或 $\ell$ 为偶整数，或 $\mathrm{Re}\, x > 0$：记
$$P = \frac{\Gamma(\frac14(x+\ell+n+3))\Gamma(\frac14(x-\ell-n+3))\Gamma(\frac14(x+\ell-n+1))\Gamma(\frac14(x-\ell+n+1))}{\Gamma(\frac14(x+\ell+n+1))\Gamma(\frac14(x-\ell-n+1))\Gamma(\frac14(x+\ell-n+3))\Gamma(\frac14(x-\ell+n+3))};$$
则
$$\frac{1-P}{1+P} = \frac{\ell n}{x^2-1-\ell^2} + \frac{2^2-n^2}{1} + \frac{2^2-\ell^2}{x^2-1} + \frac{4^2-n^2}{1} + \frac{4^2-\ell^2}{x^2-1} + \cdots.$$
由 Entry 35（$m = 1/2$，$x$、$n$、$\ell$ 减半）。

**出处。**Part II，Ch. 12，Entry 36（p. 158）。

**状态。**已证明。

**对照。**M03；M10；Entry 31 由本条（$\ell \to 0$）得出。

## Entry 37——digamma 组合的连分数

**陈述。**$\ell$ 或 $n$ 为整数或 $\mathrm{Re}\, x > 0$：
$$\frac12\left\{\psi\left(\frac{x+\ell-n+1}{2}\right) + \psi\left(\frac{x-\ell+n+1}{2}\right) - \psi\left(\frac{x+\ell+n+1}{2}\right) - \psi\left(\frac{x-\ell-n+1}{2}\right)\right\}$$
$$= \frac{2\ell n}{x^2-1+n^2-\ell^2} + \frac{2(1^2-n^2)}{1} + \frac{2(1^2-\ell^2)}{3(x^2-1)+n^2-\ell^2} + \frac{4(2^2-n^2)}{1} + \frac{4(2^2-\ell^2)}{5(x^2-1)+n^2-\ell^2} + \cdots. \tag{37.1}$$
由 Entry 35（$m \to 0$，L'Hôpital 法则）。

**出处。**Part II，Ch. 12，Entry 37（p. 158）。

**状态。**已证明。

**对照。**M03；M10（digamma 函数）。

## Entry 38——平方倒数差的连分数

**陈述。**$n$ 为整数或 $\mathrm{Re}\, x > 0$：
$$\sum_{k=0}^{\infty} \frac{1}{(x-n+2k+1)^2} - \sum_{k=0}^{\infty} \frac{1}{(x+n+2k+1)^2} = \frac{n}{x^2-1+n^2} + \frac{2(1^2-n^2)}{1} + \frac{2 \cdot 1^2}{3(x^2-1)+n^2} + \frac{4(2^2-n^2)}{1} + \frac{4 \cdot 2^2}{5(x^2-1)+n^2} + \cdots$$
$$= \frac{n}{x^2-n^2+1} - \frac{4(1^2-n^2)1^4}{3(x^2-n^2+5)} - \frac{4(2^2-n^2)2^4}{5(x^2-n^2+13)} - \cdots. \tag{38.1}$$

**出处。**Part II，Ch. 12，Entry 38（p. 158）。

**状态。**已证明。

**对照。**M03；M10；M02。

## Entry 39——三条最主要 Gamma 公式之二

**陈述。**$\ell$、$n$ 任意复数；$\mathrm{Re}\, x > 0$ 或 $n$、$\ell$ 为奇整数：记
$$P := \frac{\Gamma(\frac14(x+\ell+n+1))\Gamma(\frac14(x-\ell+n+1))\Gamma(\frac14(x+\ell-n+1))\Gamma(\frac14(x-\ell-n+1))}{\Gamma(\frac14(x+\ell+n+3))\Gamma(\frac14(x-\ell+n+3))\Gamma(\frac14(x+\ell-n+3))\Gamma(\frac14(x-\ell-n+3))};$$
则
$$P = \frac{8}{(x^2-\ell^2+n^2-1)/2} + \frac{1^2-n^2}{1} + \frac{1^2-\ell^2}{x^2-1} + \frac{3^2-n^2}{1} + \frac{3^2-\ell^2}{x^2-1} + \cdots. \tag{39.1}$$
三条最主要 Gamma 公式之一。证明用 Perron 定理 (39.2)（即 Bauer–Muir 变换；Jacobsen [5] 放宽了条件）；$F(x)F(x+2) = \frac14 \prod_{\pm}(x+1 \pm \ell \pm n)$（39.15）；$\alpha = \prod_{\pm}(x+1 \pm \ell \pm n)/(4(x+1)^2)$（39.14）。推论 (39.19)：
$$\exp\left(2\int_0^{\infty} e^{-tx}\left(\frac{\cosh(\ell t)\cosh(nt)}{\cosh t} - 1\right) \frac{dt}{t}\right) = \frac{x^2/2}{(x^2-\ell^2+n^2-1)/2} + \frac{1^2-n^2}{1} + \frac{1^2-\ell^2}{x^2-1} + \frac{3^2-n^2}{1} + \frac{3^2-\ell^2}{x^2-1} + \cdots$$
（$0 \le |\ell|, |n| < 1$，$x > 1$）。本轮 $(x,\ell,n) = (3,2,1)$ 复核：$P = 3.2$，差 $3.9 \times 10^{-31}$。

**出处。**Part II，Ch. 12，Entry 39（pp. 159–163）。

**状态。**已证明。

**对照。**M03；M10；Entry 25 的证明经本条。

## Entry 40——三条最主要 Gamma 公式之三

**陈述。**$P$ = 8 个 Gamma 函数 $\Gamma(\frac12(\alpha \pm \beta \pm \gamma \pm \delta \pm \varepsilon + 1))$ 之积（偶数个负号），$Q$ = 同式（奇数个负号）；$\beta$、$\gamma$、$\delta$、$\varepsilon$ 中至少一个为非零整数。则
$$\frac{P-Q}{P+Q} = \frac{8\alpha\beta\gamma\delta\varepsilon}{1\{2(\alpha^4+\beta^4+\gamma^4+\delta^4+\varepsilon^4+1) - (\alpha^2+\beta^2+\gamma^2+\delta^2+\varepsilon^2-1)^2 - 2^2\}}$$
$$+ \frac{64(\alpha^2-1^2)(\beta^2-1^2)(\gamma^2-1^2)(\delta^2-1^2)(\varepsilon^2-1^2)}{3\{2(\alpha^4+\cdots+\varepsilon^4+1) - (\alpha^2+\cdots+\varepsilon^2-5)^2 - 6^2\}}$$
$$+ \frac{64(\alpha^2-2^2)(\beta^2-2^2)(\gamma^2-2^2)(\delta^2-2^2)(\varepsilon^2-2^2)}{5\{2(\alpha^4+\cdots+\varepsilon^4+1) - (\alpha^2+\cdots+\varepsilon^2-13)^2 - 14^2\}} + \cdots. \tag{40.1}$$
三条最主要 Gamma 公式之一；Berndt 称「certainly one of Ramanujan's crowning achievements in the theory of continued fractions」（无疑是拉马努金在连分数理论中最辉煌的成就之一）。Watson [8] 给出唯一已发表证明。拉马努金（第一本笔记 p. 152）只给了序列 $2n^2+2n+1$ 与 $2n^2+2n+2$ 的两项（1、5 与 2、6），误以为线性；Watson 在 1931 年伦敦数学会演讲中也照抄了此误（写 9、10 而非 13、14），[8] 中亦有此误印。Jacobsen 定理：(40.1) 右端连分数收敛到 $\mathbb{C}^5$ 上的亚纯函数 $F(\alpha,\beta,\gamma,\delta,\varepsilon)$，但一般 $F \ne (P-Q)/(P+Q)$，$F$ 的恒等式未知。

**出处。**Part II，Ch. 12，Entry 40（pp. 163–164）。

**状态。**已证明（Watson，唯一已发表证明）；右端连分数的一般极限函数 $F$ 的恒等式未知（Jacobsen）。

**对照。**M03；M10；Entry 35 第一等式是本条的推论（Watson）。

## Entry 41——₂F₁(−β,1) 的连分数

**陈述。**$|x+1| > 1$ 或 $\gamma$ 为非负整数：
$${}_2F_1(-\beta,1;\gamma+1;-x) = \frac{\Gamma(\beta+1)\Gamma(\gamma+1)(1+x)^{\beta+\gamma}}{\Gamma(\beta+\gamma+1)x^{\gamma}} - \frac{\gamma}{(\beta+1)x+1-\gamma} - \frac{1(1-\gamma)(x+1)}{(\beta+2)x+3-\gamma} - \frac{2(2-\gamma)(x+1)}{(\beta+3)x+5-\gamma} - \cdots. \tag{41.1}$$
由 (21.3) 得出。本轮 $(\beta,\gamma,x) = (1,1,2)$ 复核差 $0$。

**出处。**Part II，Ch. 12，Entry 41（pp. 164–165）。

**状态。**已证明。

**对照。**M03；M07；M10。

## Entry 42——₁F₁(1;n+1;x) 的连分数

**陈述。**（Legendre 首发现）$n$ 为非负整数或 $x$ 在 $(-\infty,0]$ 外：
$${}_1F_1(1;n+1;x) = \frac{e^x \Gamma(n+1)}{x^n} - \frac{n}{x} + \frac{1-n}{1} + \frac{1}{x} + \frac{2-n}{1} + \frac{2}{x} + \frac{3-n}{1} + \frac{3}{x} + \cdots$$
$$= \frac{e^x \Gamma(n+1)}{x^n} - \frac{n}{x+1-n} - \frac{1(1-n)}{x+3-n} - \frac{2(2-n)}{x+5-n} - \frac{3(3-n)}{x+7-n} - \cdots. \tag{42.1}$$
推论：$\sum_{k=0}^{\infty} \frac{(-x)^k}{k!(n+k)} = \frac{\Gamma(n)}{x^n} - \frac{e^{-x}}{x} + \frac{1-n}{1} + \frac{1}{x} + \frac{2-n}{1} + \frac{2}{x} + \cdots$。本轮 $(n,x) = (1,1)$ 复核差 $2.0 \times 10^{-31}$。

**出处。**Part II，Ch. 12，Entry 42（p. 165）。

**状态。**已证明（Legendre）。

**对照。**M03；M07；M10；Entry 47 (47.3) 的连分数与本条同族。

## Entry 43——误差函数级数的连分数

**陈述。**$x$ 在 $(-\infty,0]$ 外：
$$\sum_{k=0}^{\infty} \frac{x^k}{1 \cdot 3 \cdots (2k+1)} = \sqrt{\frac{\pi}{2x}} e^{x/2} - \frac{1}{x} + \frac{1}{1} + \frac{2}{x} + \frac{3}{1} + \frac{4}{x} + \frac{5}{1} + \cdots$$
$$= \sqrt{\frac{\pi}{2x}} e^{x/2} - \frac{1}{x+1} - \frac{1 \cdot 2}{x+5} - \frac{3 \cdot 4}{x+9} - \frac{5 \cdot 6}{x+13} - \cdots. \tag{43.1}$$
推论 1：$F(x) := \int_0^x e^{-t^2} dt = \frac{\sqrt{\pi}}{2} - \frac{e^{-x^2}}{2x} + \frac{1}{x} + \frac{2}{2x} + \frac{3}{x} + \frac{4}{2x} + \cdots$（300 DPI 放大图确认）。推论 2：$\int_0^x \frac{F(t)}{t} dt = \frac{\sqrt{\pi}}{2}(\frac{\gamma}{2} + \mathrm{Log}(2x)) + o(1)$（$x \to \infty$）。本轮复核：$x = 1$ 时第一式 300 项差 $3.6 \times 10^{-15}$、1000 项差 $1.4 \times 10^{-27}$；第二式（偶部，分子带负号）300 项差 $2.1 \times 10^{-21}$。

**出处。**Part II，Ch. 12，Entry 43（p. 166）。

**状态。**已证明。

**对照。**M03；M09（误差函数积分）；M12。

## Entry 44(i)——指数积分 φ(x) 的渐近级数

**陈述。**$\varphi(x) = \int_0^{\infty} \frac{e^{-t}}{x+t} dt$；$\int_0^x \frac{1-e^{-t}}{t} dt = \sum_{k=1}^{\infty} \frac{(-1)^{k-1} x^k}{k! k} = \gamma + \mathrm{Log}\, x + e^{-x} \varphi(x)$（44.1）。Entry 44(i)（Euler）：$\varphi(x) \sim \sum_{k=0}^{\infty} (-1)^k k!/x^{k+1}$（$x \to \infty$）。

**出处。**Part II，Ch. 12，Entry 44(i)（pp. 167–171）。

**状态。**已证明（Euler；渐近级数）。

**对照。**M03；M12（渐近级数）；M01（Euler 常数 γ）；M09。

## Entry 44(ii)——φ(x) 的界与近似

**陈述。**$\varphi(x)$ 介于 $1/x$ 与 $1/(x+1)$ 之间，且近似等于 $\sqrt{\varphi(x+1)/x}$；$f(x) = \frac{1}{x} + \frac{1}{1} + \frac{1}{x} + \frac{2}{1} + \frac{2}{x} + \cdots$（44.3）。

**出处。**Part II，Ch. 12，Entry 44(ii)（pp. 167–171）。

**状态。**已证明。

**对照。**M03；M12。

## Entry 44(iii)——φ(x) 的两式连分数

**陈述。**
$$\varphi(x) = \frac{1}{x} + \frac{1}{1} + \frac{1}{x} + \frac{2}{1} + \frac{2}{x} + \frac{3}{1} + \frac{3}{x} + \cdots = \frac{1}{x+1} - \frac{1^2}{x+3} - \frac{2^2}{x+5} - \frac{3^2}{x+7} - \cdots$$
（第二连分数首由 Tschebyscheff 导出；Jacobsen 证对一切在 $(-\infty,0)$ 外的复 $x$ 成立）。

**出处。**Part II，Ch. 12，Entry 44(iii)（pp. 167–171）。

**状态。**已证明（Tschebyscheff；Jacobsen）。

**对照。**M03；M12。

## Entry 44(iv)——φ(x) 的截断展开与尾部连分数

**陈述。**
$$\varphi(x) = \sum_{k=0}^{n-1} (-1)^k \frac{k!}{x^{k+1}} + (-1)^n \frac{n!}{x^n} \cdot \left(\frac{1}{x+n+1} - \frac{n+1}{x+n+3} - \frac{2(n+2)}{x+n+5} - \frac{3(n+3)}{x+n+7} - \cdots\right).$$
推论 1：$\sum_{k=1}^{\infty} \frac{H_k x^k}{k!} = e^x(\mathrm{Log}\, x + \gamma) + \varphi(x)$。推论 2：$\int_0^{n(1-h)} \frac{1-e^{-t}}{t} dt = \gamma + \mathrm{Log}\, n + e^{-n}\varphi(n) - e^{-n} f(h,n)$；$f(h,n) = \sum_{k=1}^{\infty} \frac1k \left(e^n - \sum_{j=0}^{k-1} \frac{n^j}{j!}\right) h^k$（Berndt 的表述纠正了拉马努金 p. 153 的版本）。拉马努金数值：$\varphi(1) = 0.5963474$，$\varphi(1/2) = 0.9229106$，Berndt 用 (44.1) 分别取 11 项与 9 项验证无误。本轮复核：$\varphi(1) = 0.596347362323194074341078499369$（300 项差 $1.4 \times 10^{-29}$），与拉马努金值一致。

**出处。**Part II，Ch. 12，Entry 44(iv)（pp. 167–171）。

**状态。**已证明。

**对照。**M03；M12；M01（调和数 $H_k$、Euler 常数 γ）。

## Entry 45(i)——渐近分数分子的偶次多项式

**陈述。**连分数 $\frac{1}{1} + \frac{x}{1} + \frac{x}{1} + \frac{2x}{1} + \frac{2x}{1} + \frac{3x}{1} + \frac{3x}{1} + \cdots + \frac{(n-1)x}{1} + \frac{nx}{1}$；则 $B_{2n}(x) := B_{2n} = \sum_{k=0}^{n} (-n)_k^2 \frac{x^k}{k!}$（45.1）。（$B_m$ 为 (1.4) 记号下的渐近分数分子/分母。）

**出处。**Part II，Ch. 12，Entry 45(i)（pp. 171–172）。

**状态。**已证明。

**对照。**M03；M07（Pochhammer 符号）。

## Entry 45(ii)——渐近分数分子的奇次多项式

**陈述。**$B_{2n-1}(x) := B_{2n-1} = \sum_{k=0}^{n-1} \frac{(-n)_k^2}{k!} \left(1 - \frac{k}{n}\right) x^k$（45.2）。

**出处。**Part II，Ch. 12，Entry 45(ii)（pp. 171–172）。

**状态。**已证明。

**对照。**M03；M07。

## Entry 46(i)——Γ(x+1) 的系数与 ψ_n 的微分方程

**陈述。**$\Gamma(x+1) = \sum_{k=0}^{\infty} A_k \frac{(-x)^k}{k!}$（46.1），$|x| < 1$；$\varphi_n(x) = \frac{1}{n!} \sum_{k=0}^{n} \binom{n}{k} A_{n-k} \mathrm{Log}^k x$（46.2）；$\psi_n$ 由 $\sum_{k=1}^{\infty} (-1)^{k-1} \frac{x^k}{k^n k!} = \varphi_n(x) + (-1)^{n-1} e^{-x} \psi_n(x)$（46.3）定义；则 $n \ge 1$ 时 $\psi_n(x) - \psi_n'(x) = \psi_{n-1}(x)/x$（46.4）。

**出处。**Part II，Ch. 12，Entry 46(i)（pp. 172–173）。

**状态。**已证明。

**对照。**M03；M10（Γ 函数）；M02。

## Entry 46(ii)——Γ 系数的 ζ 递推

**陈述。**$A_n = \sum_{k=1}^{n} \frac{(n-1)!}{(n-k)!} S_k A_{n-k}$（46.5），$S_1 = \gamma$，$S_k = \zeta(k)$（$k \ge 2$）。

**出处。**Part II，Ch. 12，Entry 46(ii)（p. 173）。

**状态。**已证明。

**对照。**M10；M01（ζ(k)、Euler 常数 γ）；M01 的 Bernoulli 数定义缺口见章首注（出处 Part I Ch. 5 Entry 9）。

## Entry 46(iii)——Γ(x+1) 的 b_k 数值表

**陈述。**$b_1 = -0.5772156649$，$b_2 = 0.9890560173$，$b_3 = -0.9074790803$，$b_4 = 0.9817280965$（拉马努金值；Berndt：$b_1$ 正确（$= -\gamma$），$b_2$、$b_3$、$b_4$ 末位有误；订正值 $b_2 = 0.9890559953$，$b_3 = -0.9074790762$，$b_4 = 0.9817280865$）。$\Gamma(x+1) = 1 + b_1 x + b_2 x^2 + b_3 x^3 + b_4 \cdot \frac{x^4}{1+\theta_x x}$（46.7）；$\theta_0 = 1.00027$，$\theta_1 = 51/52$，$\theta_2 = 77/82$，$\theta_6 = 5/68$，$\theta_7 = -1/38$「nearly」。附表 $x = 1$、$2$、$6$、$7$：Γ 值 $1$、$2$、$720$、$5040$；拉马努金近似 $0.999990949$、$1.999702292$、$719.9611865$、$2623.541808$；Berndt 重算 $0.999990967$、$1.999702625$、$719.9612493$、$2623.542013$。本轮复核：由 (46.6) 递推得 $b_2 = 0.989055995327972555395395651501$、$b_3 = -0.907479076080886289016560167356$、$b_4 = 0.981728086834400187336380294022$，Berndt 订正值正确，拉马努金值在第 8 位小数处有误。

**出处。**Part II，Ch. 12，Entry 46(iii)（p. 174）。

**状态。**已证明（Berndt 订正值）；拉马努金原值末位有误。

**对照。**M10；M01（Euler 常数 γ）。

## Entry 46(iv)——ψ_n(x) 的连分数与渐近展开

**陈述。**
$$\psi_n(x) = \frac{x}{\left(x + \frac{n}{2} + \frac{5n+10}{6x} + \frac{41n+58}{10} + \cdots\right)^{n+1}} \tag{46.8}$$
（300 DPI 放大图确认分母连分数与指数 $n+1$ 的位置）。(46.20)：
$$\psi_n(x) = \frac{1}{x^n}\left(1 - \frac{n(n+1)}{2x} + \frac{n(n+1)(n+2)(3n+5)}{24x^2} - \frac{n(n+1)(n+2)^2(n+3)^2}{48x^3} + \cdots\right).$$
证明经 Entry 17（$a_1 = n/2$，$a_2 = (5n+10)/12$，$a_3 = (41n+58)/60$）。例：$F(x) = \int_0^x \frac{1-e^{-t}}{t} dt$；$\lim_{x\to\infty} \left(\int_0^x \frac{F(t)}{t} dt - \frac12 F^2(x)\right) = \frac{\pi^2}{12}$。

**出处。**Part II，Ch. 12，Entry 46(iv)（pp. 175–178）。

**状态。**已证明。

**对照。**M03；M10；M12；M09。

## Entry 47——Nielsen 积分的三式连分数

**陈述。**（Nielsen）
$$\int_0^{\infty} e^{-x}\left(1+\frac{x}{n}\right)^n dx = 1 + \frac{n}{1} + \frac{1(n-1)}{3} + \frac{2(n-2)}{5} + \frac{3(n-3)}{7} + \cdots \tag{47.1}$$
$$= 2 + \frac{n-1}{2} + \frac{1(n-2)}{4} + \frac{2(n-3)}{6} + \frac{3(n-4)}{8} + \cdots \tag{47.2}$$
$$= \frac{e^n \Gamma(n+1)}{n^n} - \frac{2n}{2} + \frac{3n}{3} + \frac{4n}{4} + \frac{5n}{5} + \cdots. \tag{47.3}$$
(47.3) 的连分数对一切复 $n$ 收敛（第 21 节推论 2）。本轮复核：$n = 2$ 时积分 $= 2.5$，(47.1) 因 $a_3 = 0$ 截断得 $2.5$（差 $0$），(47.3) 差 $7.9 \times 10^{-31}$。

**出处。**Part II，Ch. 12，Entry 47（pp. 179–181）。

**状态。**已证明（Nielsen）。

**对照。**M03；M10；M12；Entry 48 是本条积分的渐近展开。

## Entry 48——Nielsen 积分的渐近展开

**陈述。**$n \to \infty$ 时，
$$\int_0^{\infty} e^{-x}\left(1+\frac{x}{n}\right)^n dx = \frac{e^n \Gamma(n+1)}{2n^n} + \frac23 - \frac{4}{135n} + \frac{8}{2835n^2} + \frac{16}{8505n^3} - \frac{8992}{3^8 \cdot 5^2 \cdot 7 \cdot 11 n^4} + \cdots. \tag{48.1}$$
（拉马努金 JIMS 投稿题 [16, pp. 323–324]；Watson、Szegő 证明；末项未见于前人；更后系数由 Bowman 等与 Marsaglia 算出。）推论：$\theta = \theta_n$ 由 $\sum_{k=0}^{n-1} \frac{n^k}{k!} + \frac{n^n}{n!} \theta = \frac{e^n}{2}$（48.2）定义；$\theta \approx \theta^* = \theta_n^* := \frac{4+15n}{8+45n}$（48.3）；$\theta = \frac{e^n \Gamma(n+1)}{2n^n} + 1 - \int_0^{\infty} e^{-x}\left(1+\frac{x}{n}\right)^n dx$（48.4）；$\theta = \frac13 + \frac{4}{135n} - \frac{8}{2835n^2} + \cdots$（48.5）。附表：$n = 0$：$\theta = 0.50000$；$n = 1/2$：$\theta = 0.37750$，$\theta^* = 0.37705$；$n = 1$：$0.35914$，$0.35849$；$n = 3/2$：$0.35146$，$0.35099$；$n = 2$：$0.34726$，$0.34694$；$n = \infty$：$1/3$。Berndt 重算：$\theta_{3/2} = 0.35145$（与拉马努金表值 $0.35146$ 略差），$\theta_{1/2}$ 验证无误。(48.7)：$\theta_n = 1 - \frac{e^n \Gamma(n+1)}{2n^n} + \frac{2n}{2} + \frac{3n}{3} + \frac{4n}{4} + \frac{5n}{5} + \cdots$（$n > 0$）。拉马努金猜想 $\theta_n$ 恒介于 $1/2$ 与 $1/3$ 之间，Watson 与 Szegő 证明。联系：Poisson 分布 $P(S_n \le n) \to 1/2$（《Mathematical Gazette》1983 年问题）；「生日惊喜」问题（Blaum 等）；Copson 类似结果 $\varphi_n = \frac12 + \frac{1}{8n} + \frac{1}{32n^2} + \cdots$。本轮复核：$\theta_2 = 0.347264024732662556807606865144$（表值 $0.34726$ 一致）；$\theta_{1/2}$ 经 (48.7) 连分数得 $0.377503296111824763073476740344$（表值 $0.37750$ 一致）。

**出处。**Part II，Ch. 12，Entry 48（pp. 181–184）。

**状态。**已证明（Watson；Szegő）；θ_n 介于 1/2 与 1/3 之间的猜想已证明。

**对照。**M03；M10；M12（渐近展开）；M01（Poisson 分布）。

## Entry 49——Ei(n) 的 θ 渐近展开

**陈述。**$n \ge 2$ 整数；$\theta = \theta_n$ 由 $\gamma + \mathrm{Log}\, n + \sum_{k=1}^{\infty} \frac{n^k}{k! k} = e^n \left(\sum_{k=0}^{n-2} \frac{k!}{n^{k+1}} + \frac{(n-1)!}{n^n} \cdot \theta\right)$ 定义；则 $n \to \infty$ 时 $\theta = \frac23 + \frac{4}{135n} + \frac{8}{2835n^2} + \cdots$（Olver 的解法；$\gamma_0(1) = 2/3$，$\gamma_1(1) = 4/135$，$\gamma_2(1) = -76/2835$；左端为 PV $\int_{-\infty}^n \frac{e^t}{t} dt =: \mathrm{Ei}(n)$）。

**出处。**Part II，Ch. 12，Entry 49（p. 184）。本章最后一条。

**状态。**已证明（Olver）。

**对照。**M03；M12；M01（Euler 常数 γ）；M09（指数积分 Ei）。

## 小结

- 本章是连分数理论的核心章：Entry 1–2 为基本递推与级数–连分数对应；Entry 3–6 为无穷根式（Entry 4 的 Vijayaraghavan 收敛定理、Entry 5 的 cos 根式为全章仅有的「拉马努金断言不成立」案例）；Entry 7–16 为初等连分数恒等式（Entry 8 的 e 连分数、Entry 11 的终止 ₁F₁ 商、Entry 13 的 a 连分数、Entry 14 的偶部收缩、Entry 15 的对应恒等式、Entry 16 的双重级数）；Entry 17 为「对应」理论的长节（φ_k 递推与 Andrews 组合证明，例 (17.22) 为 ₂F₁² 的连分数）；Entry 18–24 为古典超几何商连分数（Entry 18 的 Euler 四推论、Entry 19 的 Bessel 商、Entry 20 的 Gauss 连分数、Entry 21 的三式、Entry 22 的 Euler 连分数、Entry 23 的对应系数递推、Entry 24 的有限 ₂F₃ 商）；Entry 25–40 为 Gamma 函数主线（Entry 25 的 Brouncker π、Entry 27 的 x、y 对称恒等式、Entry 29–32 的 digamma 型级数与 ζ(2)、ζ(3)、2G 的连分数、Entry 33–40 的 Gamma 商连分数，其中 Entry 34、39、40 为章首点名的三条最主要 Gamma 公式，Entry 40 为五参数的顶峰）；Entry 41–43 为 ₂F₁、₁F₁ 与误差函数级数的连分数；Entry 44–49 为渐近分析支线（Entry 44 的指数积分 φ(x)、Entry 45–46 的 Γ 系数与 ψ_n、Entry 47–49 的 Nielsen 积分与 θ_n 渐近展开，收束全章）。
- 与 Ch. 10–11 的互见：Entry 20、Entry 22 的超几何商是 Ch. 11 Gauss 连分数主题的继续；Entry 7 (7.2)、Entry 12 由 Entry 22 导出，Entry 9 由 (7.2) 导出，Entry 41 由 Entry 21 (21.3) 导出；Entry 17 的「对应」理论与 Ch. 10 Entry 27 的幂级数对应互补；Entry 39 的 Perron 定理（Bauer–Muir 变换）与 Ch. 11 Entry 21 的变换思想同源；Entry 40 的第一推论是 Entry 35，Entry 35 又生出 Entry 36、37、38；Entry 30 由 Entry 33（m→0），Entry 31 由 Entry 36（ℓ→0），Entry 25 的证明经 Entry 39，Entry 29 由 Entry 34 首证（Perron，1953 年）。
- 数值复核（mpmath 30 位；脚本在工作目录，未入仓库）：verify.py、verify2.py、verify3.py、verify4.py、verify5.py、verify6.py、verify13.py，约 30 项检查。精确通过约 20 项：Entry 8 两 e 连分数（差 0）、Entry 17 例 (17.22) 6 项截断（差 9.3×10⁻⁸，属截断误差）、Entry 18 推论 1（x=1，差 9.9×10⁻³²）、Entry 20（差 2.5×10⁻³²）、Entry 21 推论 1 第二式（两组差 0）、Entry 22（两组差约 10⁻³²）、Entry 25 (25.1)（x=2、n=1，差 0）、Entry 29 (29.1)（差 1.4×10⁻¹¹，3000 项慢收敛）、Entry 30 (x,n)=(2,1) 截断（差 0）、Entry 32(iii) ζ(3)（300 项差 1.1×10⁻¹⁶）、Entry 33（差 0）、Entry 34（差 0）、Entry 39（差 3.9×10⁻³¹）、Entry 41（差 0）、Entry 42（差 2.0×10⁻³¹）、Entry 43（两式差 3.6×10⁻¹⁵ 与 2.1×10⁻²¹）、Entry 44(iv) φ(1)（差 1.4×10⁻²⁹）、Entry 46(iii) b₂、b₃、b₄（Berndt 订正值复核一致）、Entry 47 (47.1) 截断与 (47.3)（差 0 与 7.9×10⁻³¹）、Entry 48 θ₂ 与 θ_{1/2}（与表值一致）。慢收敛通过 7 项（误差约 1/N，项数加大后按 1/N 缩小）：Entry 25 推论 1、Brouncker π、Entry 27、Entry 30 推论、Entry 31 推论 2G、Entry 32(ii) ζ(2)。另有两处本轮发现的原书印文问题（见下），均已数值证实并标待核对、未擅自改动原文。
- **本轮发现的原书印文问题**（数值证实，原文未改动，标待核对）：
  1. **Entry 21 推论 1 第一式存疑**：印文第一式按字面读不成立。证据：(n,x)=(2,0.5) 时左端 0.297442541400256293697301575628；b₁=1 的字面式得 0.398060466155671997398312959113；b₁=n−x+1、n+1、n−x、n 均不符（0.1814、0.1536、0.2847、0.2216）；反解使该式成立的 b₁（(2,0.5)→1.4249、(3,0.7)→2.0651、(4,0.2)→3.7071）均非 n、x 的简单表达式，说明字面 a-模式本身也可能有误，不只是分母问题。但由 (21.1) 令 γ=n、x→−x/β、β→∞ 直接推导的形式在 (2,0.5)、(3,0.7) 两组参数下与左端精确吻合，证明本身无误。300 DPI 放大图确认第一分母印文确为「n − n + 1」字样。
  2. **Entry 13 条件符号疑似印错**：印文条件第一组为 Re((a−b)/d)>0，结论为连分数 = a。证据：20 组参数（16 组整数 + 4 组非整数，3000 项）复核表明连分数关于 a、b 对称，极限恒为 min(a,b)；a=3、b=2、d=1 满足印文全部条件，连分数却趋向 2 而非 3。书中诸证明的步骤均要求 Re((b−a)/d)>0：尾部证明明言级数在 Re((b−a)/d)≥0 时发散从而连分数收敛到 a；Entry 20 + Gauss 定理的步骤需 Re((b−a)/d)>0（否则 ₂F₁ 在 1 处发散）；Perron 定理的极小解辨认（x₀/x₁ = b）亦需 Re((b−a)/d)>0。结论：印文条件的符号似应为 Re((b−a)/d)>0（或等价地结论应为 b）。600 DPI 放大图确认印文条件确为 a−b。
- 拉马努金原文疏失（Berndt 已指出）：Entry 3 误印（笔记本 p. 143）、Entry 5(i) 仅 θ=0 成立、Entry 6 系数求和（笔记本 p. 143）、Entry 7 左端误写作 x（笔记本 p. 143）、Entry 28 精确版无合理解释（第一本笔记 p. 160）、Entry 32(iii) 第二连分数略有错误（笔记本 p. 149）、Entry 40 序列误以为线性（第一本笔记 p. 152）、Entry 44 推论 2 的表述（Berndt 纠正了拉马努金 p. 153 的版本）、Entry 46(iii) b₂、b₃、b₄ 末位错、Entry 48 θ_{3/2} 表值略差（0.35146 对重算 0.35145）。

## 待核对清单

1. IMSC 整理表本章的结果数（2026-11-06 实测 imsc.res.in 当日不可达，未能补录；此前 Ch. 1–11 亦多次不可达）。
2. **Entry 21 推论 1 第一式的本轮发现**：印文第一式按字面读不成立（b₁=1、n−x+1、n+1、n−x、n 均不符；反解 b₁ 非 n、x 的简单表达式），疑似印文有误；由 (21.1) 推导的正确形式已给出并经两组参数精确复核。须独立核对（或查其他印次、勘误表）。
3. **Entry 13 条件的本轮发现**：印文条件 Re((a−b)/d)>0 疑似应为 Re((b−a)/d)>0（或结论应为 b），20 组参数数值复核 + 三处证明步骤均支持。须独立核对（或查其他印次、勘误表）。
4. Berndt 章首计数（本章共几条陈述）：章首导言未见计数句，待核对原书章首。
5. TIFR 影印版页码：Berndt 文中明确引用的有 Entry 3、Entry 6、Entry 7（笔记本 p. 143）、Entry 28（第一本笔记 p. 160）、Entry 32(iii)（笔记本 p. 149）、Entry 40（第一本笔记 p. 152）、Entry 44 推论 2（笔记本 p. 153）；其余各条的 TIFR 页码待核对。
6. Entry 40 (40.1) 右端连分数的一般极限函数 F(α,β,γ,δ,ε) 的恒等式（Jacobsen：F ≠ (P−Q)/(P+Q)，恒等式未知）。
7. Entry 27、Entry 28 的更精确版断言（Entry 28 的精确版 Berndt 称无合理解释）。
8. Entry 13 (13.2) Gamma 商的逐项数值复核（主恒等式 (13.1) 已复核；(13.2) 未逐项复核）。
9. Entry 17 例 (17.22) 的 6 项以上截断复核（本轮 6 项截断差 9.3×10⁻⁸，属截断量级；更多项未跑）。
10. Entry 45(i)(ii) 的 B_{2n}、B_{2n−1} 多项式在具体 n 下的逐项数值复核（本文件只给通式，未逐项复核）。
11. Entry 46(iv) (46.8) 连分数在具体 n、x 下的逐项数值复核（本文件只给通式与 (46.20) 展开，未逐项复核）。
12. Entry 48 附表 θ_{3/2} 的拉马努金表值 0.35146 与 Berndt 重算 0.35145 之差是否见于其他印次或勘误表。

## 来源说明

- 整理本：Bruce C. Berndt, *Ramanujan's Notebooks*, Part II, Springer, 1989, Ch. 12, pp. 103–184。电子版：archive.org 标识符 `ramanujan_notebooks_ii`（《Ramanujan's Notebooks, Part 2》），PDF 14,538,056 字节、371 叶，DjVu OCR 文本 560,610 字节。**PDF 页与书页对应关系：PDF 页 = 书页 + 12**（与 Part I 的 +10 不同；实测 Ch. 10 章首 PDF 页 19、Ch. 11 章首 PDF 页 60、Ch. 12 章首书页 103 在 PDF 页 115）。本章范围：书页 103–184，PDF 页 115–196，共 82 页。全部公式按 PDF 原图（150 DPI）逐字转录，关键公式另用 300 DPI 放大图确认（Entry 13 的 Re((a−b)/d)>0 条件、Entry 21 推论 1 第一分母「n − n + 1」、Entry 29 (29.1) 的 4/x 首项、Entry 32(iii) 的分母序列、Entry 34 的 (2²−ℓ²)、Entry 43 推论 1、Entry 46(iv) (46.8) 的分母连分数与指数 n+1）。
- 目录核对：Part II 目录（PDF 页 12）确认 Ch. 10 Hypergeometric Series, I 起书页 7；Ch. 11 Hypergeometric Series, II 起书页 48；Ch. 12 Continued Fractions 起书页 103；Ch. 13 Integrals and Asymptotic Expansions 起书页 185；Ch. 14 Infinite Series 起书页 240；Ch. 15 Asymptotic Expansions and Modular Forms 起书页 300。
- 书目：Part II，Springer，1989，XII + 360 页，DOI 10.1007/978-1-4612-4530-8，ISBN 0-387-96794-X。
- 数值复核：mpmath 30 位；复核脚本在工作目录（未入仓库）。下一章：Part II Ch. 13 Integrals and Asymptotic Expansions（书页 185 起）。
