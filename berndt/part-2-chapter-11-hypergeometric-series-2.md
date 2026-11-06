# Part II · 第 11 章 Hypergeometric Series, II（超几何级数（二））

出处：Bruce C. Berndt, *Ramanujan's Notebooks*, Part II, Springer, 1989, 第 11 章，pp. 48–102（Part II 的第二章；本书 Part II 覆盖第二本笔记第 10–15 章）。对应拉马努金**第一本笔记第 13、15 章**的大部分内容，个别公式散见于第一本笔记的「working pages」。

## 背景与记号

- 本章主题：超几何级数的**二次变换**与**超几何级数乘积定理**。Berndt 在章首导言（pp. 48–49）说明：二次变换多可追溯至 Kummer；乘积定理 19 世纪已有部分，多数为拉马努金原创，Bailey 1930 年代的乘积工作受拉马努金启发。亮点有二：Entry 34(iii) 把乘积公式与二次变换结合；Entry 22（递归定义的 $A_k$ 序列，引出二项系数恒等式 (22.22)(22.23)）与 Entry 31(ii)（只用二阶非齐次线性微分方程理论与 15 个幂级数系数比较才证出）是两条「amazing」公式，Berndt 称不知拉马努金如何发现。第 24 节推论 2 是零平衡 ${}_3F_2$ 的渐近公式（此前文献只有零平衡 ${}_2F_1$ 的同类公式，该式被忽视约 60 年；Evans–Stanton 给出优雅证明，但依赖事先知道公式）。第 30、31 节是 Ch. 10–11 中仅有的与微分方程有联系的公式（超几何微分方程以伪装形式出现在 Entry 31(i)）。
- **记号**（沿用 Ch. 10 引言；$\mathrm{Log}$ 为自然对数；$\gamma = 0.577215664901533\ldots$ 为 Euler 常数；$\psi$ 为 digamma 函数；$B_n$ 为 Bernoulli 数）：
  - 上升阶乘（Pochhammer 记号）$(a)_k = \Gamma(a+k)/\Gamma(a)$；
  - 广义超几何级数 ${}_pF_q$ 的定义见 Ch. 10 (0.1)；收敛性：$p < q+1$ 时 ${}_pF_q$ 对一切有限 $x$ 收敛，$p > q+1$ 时除非级数终止否则只在 $x = 0$ 收敛；多数定理不写明有效区域；
  - 本章常引 Erdélyi 的《Higher Transcendental Functions》与 Bailey 的《Generalized Hypergeometric Series》。
- 本章在原文中明确出现编号的 Entry 共 **36 条**：Entry 1–36，**无缺号**；另有分体 Entry 29(i)/29(ii)、Entry 31(i)/31(ii)、Entry 32(i)–32(v)、Entry 33(i)–33(v)、Entry 34(i)/34(ii)/34(iii)、Entry 35(i)/35(ii)/35(iii)、Entry 36(i)/36(ii)/36(iii)/36(iv)，另 Entry 34 有数值表与例 (i)(ii)，共 **56 个 Entry 标题**。Berndt 章首计数（本章共几条陈述）未在章首导言中找到，待核对原书章首；IMSC 整理表本章的结果数本次未能读取（imsc.res.in 当日不可达），待补。
- **本章的拉马努金原文疏失**（Berndt 已指出，详见各条与末尾小结）：Entry 9 拉马努金未必限定 $n$ 为整数；Entry 18 右端 $x^4$ 系数分母多一个 $(\gamma+4)$ 因子（笔记本 p. 133）；Entry 22 的 (22.2) 表述不严谨（$p^j$ 的系数无通式）；Entry 24 与推论 1 均 enigmatic，很可能不存在使恒等式成立的 $\varphi$；Entry 24 推论 2 的来源 Berndt 不知；Entry 27 例 1–4 的意图 Berndt 不知；Entry 31(ii) 拉马努金的表述「somewhat imprecisely stated」；Entry 34(ii) 拉马努金（笔记本 p. 141）第二项误写 $(1+x^2)^{1/2}$ 而非 $(1+x^2)^{3/2}$；Entry 34 例 (i) 拉马努金（笔记本 p. 142）误写 $(1-x^2)^{-5/4}$ 而非 $(1-x^2)^{-3/4}$；Entry 34 例 (ii) 拉马努金（笔记本 p. 142）误写 $2$ 而非 $1+x^2$。
- **本轮发现的原书印文问题**（数值证实，详见末尾小结）：Entry 29(i) 第二系数的 $\Gamma(\alpha+\beta-\gamma)$ 应为 $\Gamma(\alpha+\beta-\delta)$；Entry 34(ii) 的 (34.3) 印文两处有误（右端两个 ${}_2F_1$ 的第二参数应为 $\frac12$ 而非 $\frac14$、$\frac34$，第二项系数应为 $2\eta x(1+x^2)^{1/2}$ 而非 $\eta x(1+x^2)^{3/2}$）；Entry 34 数值 (c)(d)(e) 的末位错（Berndt 已在书中注明）。

## 本章结构

| Entry | 页 | 内容 |
|---|---|---|
| Entry 1 | 49 | $\varphi$ 任意时 $1/\varphi^r(x)\cdot\sum$ 为偶函数；Kummer 二次变换 |
| Entry 2 | 49 | Kummer 著名二次变换 ${}_2F_1(r,m;2m;2x/(1+x))$ |
| Entry 3 | 50 | Gauss 首证的二次变换；Entry 2、3 为全章工作母机 |
| Entry 4 | 50 | Entry 2 换元 + Entry 3 复合 |
| Entry 5 | 50 | $m = \frac12$ 特例；${}_2F_1(r,\frac12;1;\cdot)$ |
| Entry 6 | 50 | $m = \frac12$ 特例；${}_2F_1(\frac12r,\frac12(r+1);1;\cdot)$ |
| Entry 7 | 50 | ${}_1F_1(m;2m;2x) = e^x{}_0F_1(m+\frac12;x^2/4)$；Kummer 首证 |
| Entry 8 | 51 | $\varphi$ 的 Taylor 系数恒等式；由 (7.1) 系数比较 |
| Entry 9 | 51–52 | ${}_0F_1(n+\frac12;(\frac12x)^2)$ 与 Bessel $I_{n-1/2}$；推论：$I_0(x)$ 渐近 |
| Entry 10 | 52–54 | ${}_0F_1(n+\frac12;-(\frac12x)^2)$ 的三角展开；推论：大根渐近 (10.1) |
| Entry 11 | 54–56 | 正弦积分与对数积分的极坐标渐近 (11.3)(11.4)(11.5)；例 1–3 |
| Entry 12 | 56–58 | Gauss 二次变换（$x+y+z = \frac12$）；推论；例 1、2 |
| Entry 13 | 58 | Clausen 乘积 ${}_2F_1^2 = {}_3F_2$；推论 1、2（$J_0^2$） |
| Entry 14 | 59 | ${}_2F_1$ 乘积 $= {}_4F_3$；Bailey 1935 年首证 |
| Entry 15 | 59 | ${}_0F_1$ 乘积 $= {}_2F_3$；Schläfli 首证 |
| Entry 16 | 59–60 | ${}_0F_2$ 乘积 $= {}_3F_8$；Hardy 首证 |
| Entry 17 | 60–61 | ${}_0F_2$ 乘积（$\alpha_k$ 系数）；Dixon 定理 |
| Entry 18 | 61 | ${}_1F_1$ 乘积 $= {}_2F_3$；Hardy 首证；极限 (18.1) |
| Entry 19 | 61 | ${}_2F_0$ 乘积（终止级数）；Dixon 定理 |
| Entry 20 | 61–64 | ${}_1F_1$ 乘积（$\alpha_k$ 系数）；例 1–10 |
| Entry 21 | 64 | Kummer 公式（${}_2F_1$ 在 $\frac12(1+x)$ 处分解）；Entry 34 的源头 |
| Entry 22 | 64–69 | 「amazing」公式之一：$A_k$ 递归序列与 Legendre 多项式；二项恒等式 (22.22)(22.23) |
| Entry 23 | 69 | 表面无意义：$\varphi(x) = c_1+\sqrt1 = c_2+\sqrt2 = \cdots$ |
| Entry 24 | 69–77 | 形式恒等式 (24.1) 与推论 1（enigmatic）；推论 2：零平衡 ${}_3F_2$ 渐近；定理 1、2 |
| Entry 25 | 77 | ${}_2F_1$ 解析延拓基本公式；推论 1、2（整数 $n$ 的对数项） |
| Entry 26 | 78–80 | $n = 0$ 的对数恒等式；推论（$\pi\,{}_2F_1$ 的对数奇性）；例 (26.2) 双重积分 |
| Entry 27 | 80–83 | (27.1)：调和型求和 $= -\frac14{}_2F_1\mathrm{Log}(1-x)$；例 1–4（指数比） |
| Entry 28 | 83–86 | 多项式 $\varphi$ 的推广恒等式；推论（对 $n$ 求导） |
| Entry 29(i) | 86 | ${}_3F_2$ 联络公式（致 Hardy 第二封信）；**第二系数分子印文有误** |
| Entry 29(ii) | 86 | ${}_3F_2 = {}_4F_3$ (29.1)；Askey–Wilson 正交多项式 |
| Entry 30 | 87–88 | 比值 $y$ 的导数公式；超几何微分方程与 Wronskian；推论 |
| Entry 31(i) | 88 | 积分恒等式；求导化归微分方程 |
| Entry 31(ii) | 88–92 | 「amazing」公式之二：双重积分 $= {}_3F_2$ (31.1)；推论 |
| Entry 32(i) | 92 | Entry 1 取 $r = m = \frac12$：偶函数 |
| Entry 32(ii) | 92 | ${}_2F_1(\frac12,\frac12;1;1-1/x) = \sqrt{x}\,{}_2F_1(\frac12,\frac12;1;1-x)$；Pfaff 变换 (32.1) |
| Entry 32(iii) | 93 | Entry 32(ii) 换元 + Entry 5 |
| Entry 32(iv) | 93 | Kummer 公式；四次变换 |
| Entry 32(v) | 93–94 | 复参数求值；Erdélyi 公式 (8)(9) |
| Entry 33(i) | 94 | Entry 2 取 $r = m = \frac12$ |
| Entry 33(ii) | 94 | Entry 12 取 $x = y = -\frac14$ |
| Entry 33(iii) | 95 | Entry 13 取 $\alpha = \beta = -\frac14$：${}_3F_2 = {}_2F_1^2$ |
| Entry 33(iv) | 95 | Entry 4 取 $r = m = \frac12$ |
| Entry 33(v) | 95 | Erdélyi 公式；例 (i)(ii)(iii) |
| Entry 34 | 96 | 数值表 (a)–(e)；$\mu$、$\eta$ 的定义 (34.1) |
| Entry 34(i) | 96 | Kummer 分解 (34.2)；${}_2F_1(\frac12,\frac12;1;\frac12(1+x))$ |
| Entry 34(ii) | 97 | (34.3)；**印文两处有误，Rakha 订正 (1.13) 正确** |
| Entry 34(iii) | 97–98 | $\frac\pi4({}_2F_1^2(\frac12(1+x)) - {}_2F_1^2(\frac12(1-x)))$ 的级数 |
| Entry 34 例 (i) | 98 | Entry 34(i) 加 (32.1)；拉马努金误写 $(1-x^2)^{-5/4}$ |
| Entry 34 例 (ii) | 99 | Entry 34(ii) 加 (32.1)；**拉马努金原版 $2\eta x$ 正确，Berndt 版有误** |
| Entry 35(i) | 99 | $\cos(2n\sin^{-1}x) = {}_2F_1(n,-n;\frac12;x^2)$ |
| Entry 35(ii) | 99 | $\sin(2n\sin^{-1}x) = 2nx\,{}_2F_1(\frac12+n,\frac12-n;\frac32;x^2)$ |
| Entry 35(iii) | 99 | $(1-x^2)^{-1/2}\cos(2n\sin^{-1}x) = {}_2F_1(\frac12+n,\frac12-n;\frac12;x^2)$ |
| Entry 36(i)(ii) | 100 | $(x+1)^{\pm n/2}$ 的 $b_k(n)$ 展开 (36.1)(36.2) |
| Entry 36(iii)(iv) | 100–102 | Lagrange 反演展开 (36.6)(36.7) |

## Entry 1——任意函数的偶性

**陈述。**设 $\varphi$ 为任意函数，$r$、$m$ 为任意参数，则
$$\frac{1}{\varphi^r(x)}\sum_{k=0}^{\infty}\frac{(r)_k(m)_k}{(2m)_k k!}\left\{1-\frac{\varphi(-x)}{\varphi(x)}\right\}^k$$
是 $x$ 的偶函数（级数收敛时）。

**出处。**Part II，Ch. 11，Entry 1（p. 49）。证明：用 Erdélyi 书 p. 112 公式 (26) 的 Kummer 二次变换
$${}_2F_1(r,m;2m;z) = (1-z)^{-r/2}{}_2F_1\left(\tfrac12r,m-\tfrac12r;m+\tfrac12;\frac{z^2}{4(z-1)}\right).$$

**状态。**已证明（Kummer 二次变换的推论）。

**对照。**M02（超几何级数）；M07（Kummer 变换亦见 Ch. 10 Entry 21）。

## Entry 2——Kummer 二次变换

**陈述。**
$${}_2F_1\left(r,m;2m;\frac{2x}{1+x}\right) = (1+x)^r{}_2F_1\left(\tfrac12r,\tfrac12(r+1);\tfrac12(2m+1);x^2\right).$$

**出处。**Part II，Ch. 11，Entry 2（p. 49）。Kummer 的著名二次变换（Erdélyi 书 p. 111 公式 (4)）。

**状态。**已证明（Kummer）。

**对照。**M02；M07。

## Entry 3——Gauss 首证的二次变换

**陈述。**
$${}_2F_1\left(r,m;2m;\frac{4x}{(1+x)^2}\right) = (1+x)^{2r}{}_2F_1\left(r,r-m+\tfrac12;m+\tfrac12;x^2\right).$$

**出处。**Part II，Ch. 11，Entry 3（p. 50）。Erdélyi 书公式 (5)，Gauss 首证，Hardy 提及。本章的工作母机之一：Entry 34(ii) 的证明两次用它（见 Entry 34(ii)）。

**状态。**已证明（Gauss）。

**对照。**M02；M07。

## Entry 4——Entry 2 与 Entry 3 的复合

**陈述。**
$${}_2F_1\left(\tfrac12r,\tfrac12(r+1);\tfrac12(2m+1);\frac{4x}{(1+x)^2}\right) = (1+x)^r{}_2F_1\left(r,r-m+\tfrac12;m+\tfrac12;x\right).$$

**出处。**Part II，Ch. 11，Entry 4（p. 50）。证明：Entry 2 中 $x$ 换 $2\sqrt{x}/(1+x)$，再用 Entry 3。

**状态。**已证明。

**对照。**M02。

## Entry 5——$m = \frac12$ 特例

**陈述。**
$${}_2F_1\left(r,\tfrac12;1;\frac{4x}{(1+x)^2}\right) = (1+x)^{2r}{}_2F_1(r,r;1;x^2).$$

**出处。**Part II，Ch. 11，Entry 5（p. 50）。证明：Entry 3 取 $m = \frac12$。

**状态。**已证明。

**对照。**M02；Entry 32(iii) 的证明用它。

## Entry 6——$m = \frac12$ 特例

**陈述。**
$${}_2F_1\left(\tfrac12r,\tfrac12(r+1);1;\frac{4x}{(1+x)^2}\right) = (1+x)^r{}_2F_1(r,r;1;x).$$

**出处。**Part II，Ch. 11，Entry 6（p. 50）。证明：Entry 4 取 $m = \frac12$。

**状态。**已证明。

**对照。**M02。

## Entry 7——${}_1F_1$ 与 ${}_0F_1$ 的关系

**陈述。**
$${}_1F_1(m;2m;2x) = e^x{}_0F_1\left(m+\tfrac12;\frac{x^2}{4}\right). \tag{7.1}$$

推论：${}_1F_1(\frac12;1;x) = e^{x/2}{}_0F_1(1;(x/4)^2)$。

**出处。**Part II，Ch. 11，Entry 7（p. 50）。Kummer 首证，Hardy 记录；由 Entry 2 令 $x \to x/r$ 再 $r \to \infty$ 得。

**状态。**已证明（Kummer）。

**对照。**M02；M09（合流超几何函数与 Bessel 函数）；M10（Gamma 函数）。

## Entry 8——Taylor 系数的恒等式

**陈述。**设 $\varphi$ 在 $|x-1| < R$（$R > 1$）解析，且求和次序可交换，则
$$\sum_{k=0}^{\infty}\frac{\varphi^{(k)}(0)2^k(m)_k}{(2m)_k k!} = \sum_{k=0}^{\infty}\frac{\varphi^{(2k)}(1)}{2^{2k}(m+\frac12)_k k!}.$$

**出处。**Part II，Ch. 11，Entry 8（p. 51）。证明：用 (7.1) 的系数比较得 (8.2)，再代入 $\varphi$ 的 Taylor 展开。

**状态。**已证明（在所述解析性与可交换求和假设下）。

**对照。**M02；M12（渐近与级数技巧）。

## Entry 9——${}_0F_1$ 与 Bessel 函数 $I_{n-1/2}$

**陈述。**$n$ 为整数时，
$${}_0F_1\left(n+\tfrac12;\left(\tfrac12x\right)^2\right) = \frac{2^{n-1}\Gamma(n+\frac12)}{\sqrt{\pi}\,x^n}\left\{e^x{}_2F_0\left(n,1-n;\frac{1}{2x}\right) + \cos(n\pi)e^{-x}{}_2F_0\left(n,1-n;-\frac{1}{2x}\right)\right\}.$$
即 (9.1)：
$${}_0F_1\left(n+\tfrac12;\left(\tfrac12x\right)^2\right) = \Gamma\left(n+\tfrac12\right)\left(\frac{2}{x}\right)^{n-1/2}I_{n-1/2}(x),$$
其中 $I_{\nu}$ 为第一类修正 Bessel 函数。

推论（p. 52）：$x \to \infty$ 时
$${}_0F_1\left(1;\left(\tfrac12x\right)^2\right) \sim \frac{e^x}{\sqrt{2\pi x}}\left(1+\frac{1^2}{2^2(2x)}+\frac{1^2\cdot 3^2}{2^4 2!(2x)^2}+\frac{1^2\cdot 3^2\cdot 5^2}{2^6 3!(2x)^3}+\cdots\right),$$
即 $I_0(x)$ 的渐近展开（Watson 书 p. 203）。

**出处。**Part II，Ch. 11，Entry 9（pp. 51–52）。(9.1) 见 Watson 的 Bessel 函数专著 p. 77、p. 80 公式 (10)(11)，为熟知结果。注：拉马努金未必限定 $n$ 为整数；此时右端是 $|x| \to \infty$、$|\arg x| < 3\pi/2$ 时的渐近展开，$\cos(n\pi)$ 改 $\exp(in\pi)$。

**状态。**已证明（Watson）。

**对照。**M02；M09（Bessel 函数）；M12（渐近展开）。

## Entry 10——${}_0F_1$ 的三角展开与大根渐近

**陈述。**$n$ 为整数时，
$${}_0F_1\left(n+\tfrac12;-\left(\tfrac12x\right)^2\right) = \frac{2^n\Gamma(n+\frac12)}{\sqrt{\pi}\,x^n}\left\{\cos\left(\tfrac12n\pi-x\right)\sum_{k=0}^{\infty}\frac{(-1)^k(n)_{2k}(1-n)_{2k}}{(2k)!(2x)^{2k}} - \sin\left(\tfrac12n\pi-x\right)\sum_{k=0}^{\infty}\frac{(-1)^k(n)_{2k+1}(1-n)_{2k+1}}{(2k+1)!(2x)^{2k+1}}\right\}.$$

推论：${}_0F_1(n+\frac12;-(\frac12x)^2) = 0$ 的大根 $x_0$ 满足
$$x_0 \approx \frac{\pi(\mu+n)}{2} + \frac{n(1-n)}{\pi(\mu+n)} + \frac{n(1-n)\{7n(1-n)-6\}}{3\pi^3(\mu+n)^3} + \cdots, \tag{10.1}$$
其中 $\mu$ 为奇整数，使 $|x_0 - \frac12\pi(\mu+n)|$ 最小。

**出处。**Part II，Ch. 11，Entry 10（pp. 52–54）。证明：Entry 9 中 $x$ 换 $ix$ 取实部；(10.1) 用逐次逼近 (10.2)–(10.4)。

**状态。**已证明；(10.1) 为渐近展开。

**对照。**M02；M09（Bessel 函数零点）；M12（渐近展开）。

## Entry 11——正弦积分与对数积分的渐近

**陈述。**设
$$\int_0^x \frac{\sin u}{u}\,du = \frac{\pi}{2} - r\cos(x-\theta), \tag{11.1}$$
$$\int_0^x \frac{1-\cos u}{u}\,du = \gamma + \mathrm{Log}\,x - r\sin(x-\theta), \tag{11.2}$$
则 $x \to \infty$ 时
$$r\cos\theta \sim \sum_{k=0}^{\infty}\frac{(-1)^k(2k)!}{x^{2k+1}}, \tag{11.3}$$
$$r\sin\theta \sim \sum_{k=0}^{\infty}\frac{(-1)^{k+1}(2k-1)!}{x^{2k}}, \tag{11.4}$$
$$r^2 \sim \sum_{k=0}^{\infty}\frac{(-1)^{k+1}(2k-1)!}{k\,x^{2k}}. \tag{11.5}$$

例 1：$\int_0^{\pi/2}\cos(\pi\sin^2\theta)\,d\theta = 0$；例 2：$\int_0^{\pi/2}\cos(2\pi\sin^2\theta)\,d\theta = -\int_0^{\pi/2}\cos(\pi\sin\theta)\,d\theta$；例 3：$\int_0^{\pi/2}\cos(\frac{2\pi}{3}\sin^2\theta)\,d\theta = \frac12\int_0^{\pi/2}\cos(\frac\pi3\sin\theta)\,d\theta$。

**出处。**Part II，Ch. 11，Entry 11（pp. 54–56）。证明关键恒等式 (11.11)：$\sum_{k=0}^{2n}(-1)^k k!(2n-k)! = (2n+1)!/(n+1)$（$n \ge 0$），用 Ch. 10 (32.2) 与 Gauss 定理（Ch. 10 Entry 8）证。

**状态。**已证明；(11.3)–(11.5) 为渐近展开。

**对照。**M02；M09（正弦积分 $\mathrm{Si}$ 与余弦积分 $\mathrm{Ci}$）；M12（渐近展开）。

## Entry 12——Gauss 二次变换

**陈述。**$x+y+z = \frac12$ 时，
$${}_2F_1(-x,-y;z;p) = {}_2F_1\left(-2x,-2y;z;\tfrac12(1-\sqrt{1-p})\right).$$

推论：$1+\frac{1^2+n}{4^2}x+\frac{(1^2+n)(5^2+n)}{4^2\cdot 8^2}x^2+\cdots = 1+\frac{1^2+n}{2^2}\cdot\frac{1-\sqrt{1-x}}{2}+\frac{(1^2+n)(3^2+n)}{2^2\cdot 4^2}\cdot\left(\frac{1-\sqrt{1-x}}{2}\right)^2+\cdots$（证明：Entry 12 取 $x = (-1+i\sqrt{n})/4$、$y = (-1-i\sqrt{n})/4$、$z = 1$、$p = x$）。

例 1（$n = 3$）：$1+\frac{x}{2^2}+\sum_{k\ge 2}\frac{(1)_k}{(\frac12)_k}(1-\frac{1}{2^3})(1-\frac{1}{4^3})\cdots(1-\frac{1}{(2k-2)^3})\cdot\frac{x^k}{(2k)^2} = 1+\sum_{k\ge 1}\frac{1}{k+1}(1+\frac{1}{1^3})(1+\frac{1}{2^3})\cdots(1+\frac{1}{k^3})\cdot\left(\frac{1-\sqrt{1-x}}{2}\right)^k$（用 (12.1)(12.2)，其中用到 $4((2n)^2+2n+1) = (4n+1)^2+3$ 与 $4(n^2-n+1) = (2n-1)^2+3$）。

例 2：$\alpha+\beta = 1$ 时，$\left(\frac{1+\sqrt{1-x}}{2}\right)^{\gamma}{}_2F_1(\frac12(\alpha+\gamma),\frac12(\beta+\gamma);\gamma+1;x) = {}_2F_1(\alpha,\beta;\gamma+1;\frac12(1-\sqrt{1-x}))$（Erdélyi 书 p. 112 公式 (22) 的熟知结果）。

**出处。**Part II，Ch. 11，Entry 12（pp. 56–58）。Gauss 首证，Erdélyi 书 p. 111 公式 (10)，Hardy 有等价式。

**状态。**已证明（Gauss）。

**对照。**M02；M07。

## Entry 13——Clausen 乘积

**陈述。**$\alpha+\beta+\gamma = 0$ 时，
$${}_2F_1^2(-\alpha,-\beta;\gamma+\tfrac12;x) = {}_3F_2(-2\alpha,-2\beta,\gamma;\gamma+\tfrac12,2\gamma;x).$$

推论 1：$\left\{1+\frac{1^2+n}{4^2}x+\frac{(1^2+n)(5^2+n)}{4^2\cdot 8^2}x^2+\cdots\right\}^2 = 1+\frac12\cdot\frac{1^2+n}{2^2}x+\frac{1\cdot 3}{2\cdot 4}\cdot\frac{(1^2+n)(3^2+n)}{2^2\cdot 4^2}x^2+\cdots$（证明：Entry 13 取 $\alpha = (-1+i\sqrt{n})/4$、$\beta = (-1-i\sqrt{n})/4$、$\gamma = \frac12$）。

推论 2：$J_0^2(i\sqrt{x}) = {}_1F_2(\frac12;1,1;x)$，其中 $J_0$ 为 0 阶常义 Bessel 函数（Watson 书 p. 147 公式 (6)，原属 Schläfli）。

**出处。**Part II，Ch. 11，Entry 13（p. 58）。Clausen 的著名结果，Hardy 提及；Bailey 专著第 10 章有其他乘积结果。

**状态。**已证明（Clausen）。

**对照。**M02；M09（Bessel 函数）；M07（Clausen 恒等式亦见 Ch. 10）。

## Entry 14——${}_2F_1$ 乘积 $= {}_4F_3$

**陈述。**$\alpha+\beta+1 = \gamma+\delta$ 时，
$${}_2F_1\left(\alpha,\beta;\gamma;\tfrac12(1-\sqrt{1-x})\right){}_2F_1\left(\alpha,\beta;\delta;\tfrac12(1-\sqrt{1-x})\right) = {}_4F_3\left[\alpha,\beta,\tfrac12(\alpha+\beta),\tfrac12(\gamma+\delta);\gamma,\delta,\alpha+\beta;x\right].$$

**出处。**Part II，Ch. 11，Entry 14（p. 59）。Bailey 专著 p. 88 公式 (3)（其中 $x = 4z(1-z)$）；首个发表证明为 Bailey 1935 年。

**状态。**已证明（Bailey 1935）。

**对照。**M02。

## Entry 15——${}_0F_1$ 乘积 $= {}_2F_3$

**陈述。**
$${}_0F_1(\gamma;x)\,{}_0F_1(\delta;x) = \sum_{k=0}^{\infty}\frac{(\gamma+\delta+k-1)_k x^k}{(\gamma)_k(\delta)_k k!},$$
即 $= {}_2F_3(\frac12(\gamma+\delta),\frac12(\gamma+\delta-1);\gamma,\delta,\gamma+\delta-1;4x)$。

**出处。**Part II，Ch. 11，Entry 15（p. 59）。实为 $J_{\gamma-1}(2i\sqrt{x})J_{\delta-1}(2i\sqrt{x})$ 的公式，Schläfli 首证，是 Entry 13 推论 2 的推广；Watson 书 p. 147 公式 (5)、Hardy、Erdélyi 书 p. 185 公式 (2) 均有，Bailey 亦证。

**状态。**已证明（Schläfli）。

**对照。**M02；M09（Bessel 函数乘积）。

## Entry 16——${}_0F_2$ 乘积 $= {}_3F_8$

**陈述。**
$${}_0F_2(m+1,n+1;x)\,{}_0F_2(m+1,n+1;-x) = \sum_{k=0}^{\infty}\frac{(-1)^k(m+n+2k+1)_k x^{2k}}{(m+1)_k(n+1)_k(m+1)_{2k}(n+1)_{2k}k!}, \tag{16.1}$$
亦可写为 ${}_3F_8[\frac13(m+n+1),\frac13(m+n+2),\frac13(m+n+3);\frac12(m+n+1),\frac12(m+n+2),m+1,n+1,\frac12(m+1),\frac12(m+2),\frac12(n+1),\frac12(n+2);-27x^2/64]$。

**出处。**Part II，Ch. 11，Entry 16（pp. 59–60）。首个发表证明似为 Hardy（书 p. 503、p. 516，以后一形式陈述），Erdélyi 书 p. 186 公式 (7)。

**状态。**已证明（Hardy）。

**对照。**M02。

## Entry 17——${}_0F_2$ 乘积（$\alpha_k$ 系数）

**陈述。**
$${}_0F_2(m+n+1,n+1;x)\,{}_0F_2(m+1,1-n;-x) = 1+\sum_{k\ge 1}\alpha_k\frac{(\frac12(2m+n+k+2))_k(2x)^k}{(m+n+1)_k(m+1)_k k!}, \tag{17.1}$$
其中 $\alpha_k$ 由 (17.2) 定义：$k$ 奇时 $\alpha_k = n/((n^2-1^2)(n^2-3^2)\cdots(n^2-k^2))$，$k$ 偶时 $\alpha_k = 1/((n^2-2^2)(n^2-4^2)\cdots(n^2-k^2))$。

**出处。**Part II，Ch. 11，Entry 17（pp. 60–61）。证明用 (17.3)：$(a)_{r-k} = (-1)^k(a)_r/(-a-r+1)_k$ 与 Dixon 定理（Ch. 10 Entry 7），关键步骤 (17.4)(17.5)。

**状态。**已证明。

**对照。**M02；M07（Dixon 定理见 Ch. 10 Entry 7）。

## Entry 18——${}_1F_1$ 乘积 $= {}_2F_3$

**陈述。**
$${}_1F_1(-\beta;\gamma;-x)\,{}_1F_1(-\beta;\gamma;x) = {}_2F_3\left(-\beta,\beta+\gamma;\gamma,\tfrac12\gamma,\tfrac12(\gamma+1);\frac{x^2}{4}\right).$$

**出处。**Part II，Ch. 11，Entry 18（p. 61）。首个发表证明为 Hardy（书 p. 503、p. 516；Hardy 的表述有误印：读 $x^2/4$ 而非 $-x^2/4$），Erdélyi 书 p. 186 公式 (5)。注：拉马努金（笔记本 p. 133）在右端 $x^4$ 系数分母多写了一个 $(\gamma+4)$ 因子。

$x \to -x/\beta$、$\beta \to \infty$ 得 (18.1)：
$${}_0F_1(\gamma;-x)\,{}_0F_1(\gamma;x) = {}_0F_3\left(\gamma,\tfrac12\gamma,\tfrac12(\gamma+1);-\frac{x^2}{4}\right).$$

**状态。**已证明（Hardy）。

**对照。**M02；M09。Entry 16 与 18 的推广与 $q$-类比见 Srivastava 的文章。

## Entry 19——${}_2F_0$ 乘积（终止级数）

**陈述。**$\alpha$ 或 $\beta$ 为非负整数时，
$${}_2F_0(-\alpha,-\beta;x)\,{}_2F_0(-\alpha,-\beta;-x) = \sum_{k=0}^{\infty}\frac{(-\alpha)_k(-\beta)_k(-\alpha-\beta+k)_k x^{2k}}{k!} = {}_4F_1\left(-\alpha,-\beta,-\tfrac12(\alpha+\beta),-\tfrac12(\alpha+\beta-1);-\alpha-\beta;4x^2\right).$$

**出处。**Part II，Ch. 11，Entry 19（p. 61）。证明：逐项相乘 + Dixon 定理；Erdélyi 书 p. 186 公式 (4)。

**状态。**已证明。

**对照。**M02。

## Entry 20——${}_1F_1$ 乘积（$\alpha_k$ 系数）与例 1–10

**陈述。**$\alpha_k$ 由 (17.2) 定义时，
$${}_1F_1(-m;n+1;-x)\,{}_1F_1(-m-n;1-n;x) = 1+\sum_{k\ge 1}\alpha_k\frac{(\frac12(-2m-n-k))_k(-2x)^k}{k!}. \tag{20.1}$$

**出处。**Part II，Ch. 11，Entry 20（pp. 61–62）。证明用 (17.3) 与 Dixon 定理 (17.4)。

其后例 1–10（pp. 62–64，属 Entry 16/18 的例）：

- 例 1：$\sum_{k\ge 0}\frac{x^{3k}}{(3k)!}\cdot\sum_{k\ge 0}\frac{(-x)^{3k}}{(3k)!} = \frac13+\frac23\sum_{k\ge 0}\frac{(-3x^2)^{3k}}{(6k)!}$（Entry 16 取 $m = -\frac13$、$n = -\frac23$、$x \to (x/3)^3$）；
- 例 2：$\sum_{k\ge 0}\frac{x^k}{(k!)^3}\cdot\sum_{k\ge 0}\frac{(-x)^k}{(k!)^3} = \sum_{k\ge 0}\frac{(3k)!(-x^2)^k}{(k!)^3((2k)!)^3}$（Entry 16 取 $m = n = 0$；Hardy 书 p. 7 提及，见于拉马努金致 Hardy 的信）；
- 例 3：$\sum_{k\ge 0}\frac{x^{3k+1}}{(3k+1)!}\cdot\sum_{k\ge 0}\frac{(-1)^k x^{3k+1}}{(3k+1)!} = \frac23\sum_{k\ge 0}\frac{(-1)^k(3x^2)^{3k+1}}{(6k+2)!}$（Entry 16 取 $m = \frac13$、$n = -\frac13$）；
- 例 4：$\cos x\cosh x = \sum_{k\ge 0}\frac{(-1)^k(2x^2)^{2k}}{(4k)!}$（(18.1) 取 $\gamma = \frac12$、$x \to x^2/4$）；
- 例 5：$\sin x\sinh x = \sum_{k\ge 0}\frac{(-1)^k(2x^2)^{2k+1}}{(4k+2)!}$（(18.1) 取 $\gamma = \frac32$）；
- 例 6：$\sum_{k\ge 0}\frac{x^k}{(k!)^2}\cdot\sum_{k\ge 0}\frac{(-x)^k}{(k!)^2} = \sum_{k\ge 0}\frac{(-x^2)^k}{(k!)^2(2k)!}$（(18.1) 取 $\gamma = 1$）；
- 例 7：${}_1F_1(\frac12;1;x)\,{}_1F_1(\frac12;1;-x) = {}_1F_2(\frac12;1,1;x^2/4)$（Entry 18 取 $\beta = -\frac12$、$\gamma = 1$）；
- 例 8：${}_1F_1(1;\frac32;x/2)\,{}_1F_1(1;\frac32;-x/2) = \sum_{k\ge 0}\frac{(2k)!(2x)^{2k}}{(2k+1)(4k+1)!} = {}_2F_3(1,\frac12;\frac32,\frac34,\frac54;x^2/16)$（Entry 18 取 $\beta = -1$、$\gamma = \frac32$、$x \to x/2$）；
- 例 9：${}_1F_1(1;n+1;x)\,{}_1F_1(1;n+1;-x) = \sum_{k\ge 0}\frac{nx^{2k}}{(n+k)(n+1)_{2k}} = {}_2F_3\left(1,n;n+1,\frac12(n+1),\frac12(n+2);\frac{x^2}{4}\right)$（Entry 18 取 $\beta = -1$、$\gamma = n+1$）；
- 例 10：$n$ 为非负整数时，${}_2F_0(-n,1;x)\,{}_2F_0(-n,1;-x) = \sum_{k\ge 0}(-n)_k(-n+1+k)_k x^{2k}$（Entry 19 取 $\alpha = n$、$\beta = -1$）。

**状态。**已证明。

**对照。**M02；M09（例 4–6 的三角–双曲乘积）；M07。

## Entry 21——Kummer 公式

**陈述。**
$${}_2F_1\left(m,n;\tfrac12(m+n+1);\tfrac12(1+x)\right) = \frac{\sqrt{\pi}\,\Gamma(\frac12(m+n+1))}{\Gamma(\frac12(m+1))\Gamma(\frac12(n+1))}\,{}_2F_1\left(\tfrac12m,\tfrac12n;\tfrac12;x^2\right) + \frac{2\sqrt{\pi}\,\Gamma(\frac12(m+n+1))x}{\Gamma(\frac12m)\Gamma(\frac12n)}\,{}_2F_1\left(\tfrac12(m+1),\tfrac12(n+1);\tfrac32;x^2\right).$$

**出处。**Part II，Ch. 11，Entry 21（p. 64）。Kummer 首创，Erdélyi 书 p. 111 公式 (3)。本章的关键枢纽：$m = n = \frac12$ 时即 Entry 34(i)，再经 Entry 3 得 Entry 34(ii)。

**状态。**已证明（Kummer）。

**对照。**M02；M07；M10。

## Entry 22——「amazing」公式：$A_k$ 递归序列

**陈述。**$m$ 为非正整数，$p = \frac12m(m-1)$（22.1）；$A_k$ 由 (22.2) 定义（$A_k = p^k - \frac{k(k-1)}{3!}p^{k-1} + \frac{k(k-1)(k-2)(3k-1)}{5!}p^{k-2} + \cdots + \frac{2(k-1)!(2^{2k}-1)B_{2k}}{1\cdot 3\cdots(2k-1)}p$，$B_j$ 为 Bernoulli 数），则 $|x| < \pi$ 时
$$e^{-mx}\sum_{k=0}^{-m}\frac{(m)_k(\frac12)_k}{(k!)^2}(1-e^{-2x})^k = 1+\sum_{k=1}^{\infty}\frac{A_k x^{2k}}{2^k(k!)^2}. \tag{22.3}$$

注：(22.2) 的表述不严谨（$p^j$、$1 \le j \le k$ 的系数无通式），但 $A_k$ 由递推 (22.13) 良定义：$A_r + \sum_{k=1}^{r-1}\frac{2^{3k-1}\{(r-1)!\}^2 B_{2k}A_{r-k}}{(r-k)!(r-k-1)!(2k)!} - pA_{r-1} = 0$（$r \ge 1$，$A_0 = 1$）。前几项：$A_1 = p$（22.14）、$A_2 = p^2-\frac13p$（22.15）、$A_3 = p^3-p^2+\frac25p$（22.16）。

推论：$p = 1$ 时 $A_k = A_k(1) = 2^k(k!)^2/(2k)!$（22.20）；$p = 3$ 时 $A_k = A_k(3) = 3\cdot 2^{2k-2}A_k(1)$（22.21）。

二项系数恒等式 (22.22)：$\sum_{k=1}^n \binom{2n+2k}{n+k}\binom{2n-2k}{n-k}k^{2j} = 2^{4n-3j-1}\binom{2j}{j}A_j(p)$（$n,j \ge 1$，$p = n(2n+1)$）；(22.23)：$\sum_{k=0}^n \binom{2n+2k+2}{n+k+1}\binom{2n-2k}{n-k}(2k+1)^{2j} = 2^{4n-j+1}\binom{2j}{j}A_j(p)$（$n \ge 0$，$j \ge 1$，$p = (n+1)(2n+1)$）；据称是新的，Gould 与 Hansen 的表里没有。

**出处。**Part II，Ch. 11，Entry 22（pp. 64–69）。证明：$f_n(x) = P_n(\cos x)$（Legendre 多项式，R. J. Evans 指出），(22.7)：$P_n(\cos x) = 1+\sum_{k\ge 1}(-1)^k A_k x^{2k}/(2^k(k!)^2)$；用 Legendre 微分方程 $y''+(\cot x)y'+n(n+1)y = 0$（22.8）与 $\cot x$ 展开 (22.11) 归纳证得。

**状态。**已证明（Evans 指认 Legendre 多项式后由 Berndt 给出证明）；(22.22)(22.23) 为新恒等式。

**对照。**M02（Legendre 多项式）；M01（Bernoulli 数 $B_{2k}$——注：M01 目前缺少 Bernoulli 数定义，见 Part I Ch. 5 Entry 9）；M13（组合恒等式）；M12。

## Entry 23——表面无意义的断言

**陈述。**拉马努金称：若 $\varphi(x) = c_1+\sqrt1 = c_2+\sqrt2 = \cdots = c_n+\sqrt n$ 且「$c_1,c_2,c_3,\ldots,c_n$ 看似相似」，则它们全等于 $c$，于是 $\varphi(x) = c+\sqrt1+\sqrt2+\cdots+\sqrt n$。

**出处。**Part II，Ch. 11，Entry 23（p. 69）。Berndt：意图或将永远是谜。

**状态。**未解决（意图不明；无从数值验证）。

**对照。**无。

## Entry 24——形式恒等式与零平衡 ${}_3F_2$ 渐近

**陈述。**设 $\varphi(r) = \frac{1}{\Gamma(n+1)}\sum_{k=0}^{\infty}\binom{n}{k}P_k r^{n-k}$，$Q_r = \sum_{k=0}^{\infty}\frac{(r+1)_k}{k!}\varphi(r+k)$，则
$$\sum_{k=0}^{\infty}\varphi(k)(1-x)^k = \sum_{k=0}^{\infty}Q_k(-x)^k + \frac{1}{(\mathrm{Log}\frac{1}{1-x})^{n+1}}\sum_{k=0}^{\infty}P_k\left(\mathrm{Log}\frac{1}{1-x}\right)^k. \tag{24.1}$$

推论 1：$Q'_r = \frac{\Gamma(m+1)}{\Gamma(m+1-r)\Gamma(r+1)}\sum_{k=0}^{\infty}\frac{(m+1)_k}{(m+1-r)_k}\varphi(m+k)$，则 $\sum_{k=0}^{\infty}\varphi(m+k)(1-x)^{m+k} = \sum_{k=0}^{\infty}Q'_k(-x)^k + \frac{1}{(\mathrm{Log}\frac{1}{1-x})^{n+1}}\sum_{k=0}^{\infty}P_k(\mathrm{Log}\frac{1}{1-x})^k$。

推论 2：$\alpha+\beta+\gamma+1 = \delta+\varepsilon$、$\gamma > -1$ 时，$x \to 0^+$ 有
$$\frac{\Gamma(\alpha+1)\Gamma(\beta+1)\Gamma(\gamma+1)}{\Gamma(\delta+1)\Gamma(\varepsilon+1)}\,{}_3F_2[\alpha+1,\beta+1,\gamma+1;\delta+1,\varepsilon+1;1-x] \sim -\mathrm{Log}\,x - \psi(\alpha+1) - \psi(\beta+1) - 2C + \sum_{k=1}^{\infty}\frac{(\delta-\gamma)_k(\varepsilon-\gamma)_k}{(\alpha+1)_k(\beta+1)_k k},$$
其中 $\psi = \Gamma'/\Gamma$，$C$ 为 Euler 常数。

定理 1：$a+b+c = d+e$、$\mathrm{Re}\,c > 0$ 时，
$$\sum_{k=0}^{\infty}\left\{\frac{\Gamma(a+k)\Gamma(b+k)\Gamma(c+k)}{\Gamma(d+k)\Gamma(e+k)\Gamma(1+k)} - \frac{1}{k+1}\right\} = L, \tag{24.2}$$
其中 $L = -2\gamma - \psi(a) - \psi(b) + \sum_{k=1}^{\infty}\frac{(d-c)_k(e-c)_k}{(a)_k(b)_k k}$（24.3）；且 $m \to \infty$ 时 $\sum_{k=0}^{m-1}\frac{(a)_k(b)_k(c)_k}{(d)_k(e)_k k!} = \frac{\Gamma(d)\Gamma(e)}{\Gamma(a)\Gamma(b)\Gamma(c)}\{\mathrm{Log}\,m + L + \gamma\} + O(1/m)$（24.4）。

定理 2（比推论 2 稍精确）：$a+b+c = d+e$、$\mathrm{Re}\,c > 0$ 时，$x \to 1^-$（$0 < x < 1$）有
$$\frac{\Gamma(a)\Gamma(b)\Gamma(c)}{\Gamma(d)\Gamma(e)}\,{}_3F_2[a,b,c;d,e;x] = -\mathrm{Log}(1-x) + L + O((1-x)\mathrm{Log}(1-x)), \tag{24.6}$$
$L$ 由 (24.3) 定义。

**出处。**Part II，Ch. 11，Entry 24（pp. 69–77）。Berndt：Entry 24 与推论 1 均 enigmatic，很可能不存在使恒等式成立的 $\varphi$；对多数 $\varphi$，$Q_r$ 与 $Q'_r$ 的级数发散；形式推导得 $\sum Q_j(-x)^j = \sum \varphi(n)(1-x)^n$，对数级数不出现。推论 2 的来源 Berndt 不知；它是除 Entry 26 可得的 ${}_2F_1$ 公式外唯一的零平衡级数渐近公式；Evans–Stanton 给出优雅证明（及 $q$-类比），并有稍强版本；本书用 Evans–Stanton 的方法展开。定理 1 的证明用引理 1–4 与 Carlson 定理；定理 2 由定理 1 推出。引理 1：${}_3F_2[A,B,C;D,E] = \frac{\Gamma(D)\Gamma(E)\Gamma(S)}{\Gamma(C)\Gamma(A+S)\Gamma(B+S)}\,{}_3F_2[D-C,E-C,S;A+S,B+S]$（$S = D+E-A-B-C$，$\mathrm{Re}\,C > 0$，$\mathrm{Re}\,S > 0$），即 Ch. 10 Entry 27 的重述。引理 2：$\Gamma(a+z)/\Gamma(d+z) = z^{a-d}(1+O(1/z))$（Stirling 推论，见 Ch. 7 Entry 23）。引理 3：$(1+z/k)^E-1 = O(z^N/k)$。引理 4：$(D-z)_k/(D)_k = O(e^{2\pi|z|/3})$。Bühring 最近用 ${}_3F_2$ 的微分方程给出定理 2 的推广（优点是不需事先知道渐近形式；拉马努金对微分方程兴趣不大，很可能另有证明）。$c = e$ 时定理 2 退化为零平衡 ${}_2F_1$ 部分和渐近 (24.5)（Luke 书 p. 109 公式 (34)；稍弱版本见 Ch. 10 Entry 15）。

**状态。**推论 2 与定理 1、2 已证明（Evans–Stanton；Bühring 推广）；主恒等式 (24.1) 与推论 1 的适用函数问题未解决。

**对照。**M02；M12（渐近分析，本章核心）；M07（$q$-类比）；M10（Gamma 函数）。

## Entry 25——${}_2F_1$ 解析延拓基本公式

**陈述。**$n$ 不是整数时，
$${}_2F_1[a+n+1,b+n+1;a+b+n+2;1-x] = \frac{\Gamma(a+b+n+2)\Gamma(-n)}{\Gamma(a+1)\Gamma(b+1)}\,{}_2F_1[a+n+1,b+n+1;n+1;x] + \frac{\Gamma(a+b+n+2)\Gamma(n)x^{-n}}{\Gamma(a+n+1)\Gamma(b+n+1)}\,{}_2F_1[a+1,b+1;-n+1;x].$$

推论 1：$n$ 为非负整数时，
$${}_2F_1[a+n+1,b+n+1;a+b+n+2;1-x] = \frac{\Gamma(a+b+n+2)\Gamma(n)x^{-n}}{\Gamma(a+n+1)\Gamma(b+n+1)}\sum_{k=0}^{n-1}\frac{(a+1)_k(b+1)_k x^k}{(-n+1)_k k!} - \frac{(-1)^n\Gamma(a+b+n+2)}{\Gamma(a+1)\Gamma(b+1)\Gamma(n+1)}\sum_{k=0}^{\infty}\frac{(a+n+1)_k(b+n+1)_k}{(n+1)_k k!}\{\psi(a+n+k+1)+\psi(b+n+k+1)-\psi(n+k+1)-\psi(k+1)+\mathrm{Log}\,x\}x^k$$
（$n = 0$ 时右端第一项理解为 0；Erdélyi 书 p. 110 公式 (14)）。

推论 2：$n$ 为非正整数时，
$${}_2F_1[a+n+1,b+n+1;a+b+n+2;1-x] = \frac{\Gamma(a+b+n+2)\Gamma(-n)}{\Gamma(a+1)\Gamma(b+1)}\sum_{k=0}^{-n-1}\frac{(a+n+1)_k(b+n+1)_k x^k}{(n+1)_k k!} - \frac{\Gamma(a+b+n+2)(-x)^{-n}}{\Gamma(a+n+1)\Gamma(b+n+1)\Gamma(1-n)}\sum_{k=0}^{\infty}\frac{(a+1)_k(b+1)_k}{(1-n)_k k!}\{\psi(a+k+1)+\psi(b+k+1)-\psi(k-n+1)-\psi(k+1)+\mathrm{Log}\,x\}x^k$$
（$n = 0$ 同推论 1 的约定；Erdélyi 书 p. 110 公式 (12) 的重述）。

**出处。**Part II，Ch. 11，Entry 25（p. 77）。超几何级数解析延拓的基本公式（Bailey 书 p. 4、Erdélyi 书 p. 108 公式 (1)）。

**状态。**已证明。

**对照。**M02；M07；M12。

## Entry 26——$n = 0$ 的对数恒等式

**陈述。**
$$\frac{\Gamma(a+1)\Gamma(b+1)}{\Gamma(a+b+2)}\,{}_2F_1(a+1,b+1;a+b+2;1-x) + \mathrm{Log}\,x\cdot{}_2F_1(a+1,b+1;1;x) + \sum_{k=0}^{\infty}\frac{(a+1)_k(b+1)_k}{(k!)^2}\{\psi(a+k+1)+\psi(b+k+1)-2\psi(k+1)\}x^k = 0.$$

推论：
$$\pi\,{}_2F_1\left(\tfrac12,\tfrac12;1;1-x\right) = \mathrm{Log}\left(\frac{16}{x}\right){}_2F_1\left(\tfrac12,\tfrac12;1;x\right) - 4\sum_{k=1}^{\infty}\frac{(\frac12)_k^2}{(k!)^2}\sum_{j=1}^k\frac{1}{(2j-1)(2j)}x^k$$
（证明：Entry 26 取 $a = b = -\frac12$，用 Gradshteyn–Ryzhik 书 p. 945 的 $\psi(k+1)$、$\psi(k+\frac12)$ 公式）。

例（pp. 79–80）：$0 < x < 1$ 时，
$$\int_0^{\pi/2}\!\!\int_0^{\pi/2}\frac{\tan(\varphi/2)\,d\theta\,d\varphi}{\sqrt{1-x\cos^2\theta\cos^2\varphi}} = \frac\pi4\int_0^{\pi/2}\frac{d\varphi}{\sqrt{1-(1-x)\sin^2\varphi}} + \frac14\mathrm{Log}\,x\int_0^{\pi/2}\frac{d\varphi}{\sqrt{1-x\sin^2\varphi}}, \tag{26.2}$$
其中 (26.3)：$\int_0^{\pi/2}\frac{d\varphi}{\sqrt{1-x\sin^2\varphi}} = \frac\pi2\,{}_2F_1(\frac12,\frac12;1;x)$ 为第一类完全椭圆积分；(26.4)：$\int_0^{\pi}\frac{d\varphi}{\sqrt{1-(1-x)\sin^2\varphi}} = \frac\pi2\,{}_2F_1(\frac12,\frac12;1;1-x)$。

**出处。**Part II，Ch. 11，Entry 26（pp. 78–80）。即推论 1 或推论 2 取 $n = 0$ 的情形；拉马努金在 Ch. 10 第 15 节给了较不精确的版本。注：$c = e$ 时定理 2 的特例即零平衡 ${}_2F_1$ 在 $x \to 1^-$ 的渐近，亦为 Entry 26 的易得推论，等价于 (24.5)。

**状态。**已证明。

**对照。**M02；M11（完全椭圆积分）；M09（双重积分）；M12。

## Entry 27——调和型求和与指数比

**陈述。**$|x| < 1$ 时，
$$\sum_{k=1}^{\infty}\frac{(\frac12)_k^2}{(k!)^2}\sum_{j=1}^k\frac{1}{2j-1}x^k = -\frac14\,{}_2F_1\left(\tfrac12,\tfrac12;1;x\right)\mathrm{Log}(1-x). \tag{27.1}$$

例 1：$\exp\left(-\pi\,{}_2F_1(\frac12,\frac12;1;1-x)/{}_2F_1(\frac12,\frac12;1;x)\right) = \frac{x}{16}\left(1+\frac12x+\frac{21}{64}x^2+\cdots\right)$；例 2：$\exp\left(-\frac{2\pi}{\sqrt3}\,{}_2F_1(\frac13,\frac23;1;1-x)/{}_2F_1(\frac13,\frac23;1;x)\right) = \frac{x}{27}\left(1+\frac59x+\cdots\right)$（证明：Entry 26 取 $a = -\frac13$、$b = -\frac23$；用到 $\psi(\frac23)+\psi(\frac13)-2\psi(1) = -3\mathrm{Log}\,3$ 与 $\psi(k+\frac23)+\psi(k+\frac13) = 3\psi(3k)-\psi(k)-3\mathrm{Log}\,3$）；例 3：$\exp\left(-\sqrt2\pi\,{}_2F_1(\frac14,\frac34;1;1-x)/{}_2F_1(\frac14,\frac34;1;x)\right) = \frac{x}{64}\left(1+\frac58x+\cdots\right)$（Entry 26 取 $a = -\frac14$、$b = -\frac34$；用到 $\psi(\frac14)+\psi(\frac34)-2\psi(1) = -6\mathrm{Log}\,2$ 与 $\psi(k+\frac14)+\psi(k+\frac34) = 4\psi(4k)-\psi(k)-\psi(k+\frac12)-8\mathrm{Log}\,2$）；例 4：$\exp\left(-2\pi\,{}_2F_1(\frac16,\frac56;1;1-x)/{}_2F_1(\frac16,\frac56;1;x)\right) = \frac{x}{432}\left(1+\frac{13}{18}x+\cdots\right)$（Entry 26 取 $a = -\frac16$、$b = -\frac56$；用到 $\psi(\frac16)+\psi(\frac56)-2\psi(1) = -4\mathrm{Log}\,2-3\mathrm{Log}\,3$）。

**出处。**Part II，Ch. 11，Entry 27（pp. 80–83）。证明关键 (27.2)：$\sum_{k=1}^n\frac{(-n)_k^2}{(\frac12-n)_k^2 k} = 4\sum_{j=1}^n\frac{1}{2j-1}$（$n \ge 1$），用 Ch. 10 (6.3) 的平衡 ${}_4F_3$ 变换证。左端表达式是椭圆函数理论的基本量（见 Part III Ch. 17 第 6 节）。Berndt：不知拉马努金给出例 1–4 的意图。

**状态。**已证明；例 1–4 的意图未明（Berndt 明言不知）。

**对照。**M02；M11（椭圆函数理论；例 1–4 的指数比即椭圆模量的 $q$-展开）；M06（模形式）。

## Entry 28——多项式 $\varphi$ 的推广恒等式

**陈述。**$\varphi$ 为 $m$ 次多项式，$n$ 不是整数，$\mathrm{Re}(a+b+m+n+1) < 0$ 时，
$$\Gamma(a+1)\Gamma(b+1)\Gamma(n)\sum_{k=0}^{\infty}\frac{(a+1)_k(b+1)_k\varphi(k)}{(1-n)_k k!} + \Gamma(a+n+1)\Gamma(b+n+1)\Gamma(-n)\sum_{k=0}^{\infty}\frac{(a+n+1)_k(b+n+1)_k\varphi(n+k)}{(n+1)_k k!} = \frac{\Gamma(a+n+1)\Gamma(b+n+1)\Gamma(a+1)\Gamma(b+1)}{\Gamma(a+b+n+2)}\sum_{k=0}^{\infty}\frac{(a+1)_k(b+1)_k\Delta^k\varphi(0)}{(a+b+n+2)_k k!}.$$

推论：同假设下，
$$\frac{\Gamma(a+1)\Gamma(b+1)}{\Gamma(a+b+2)}\sum_{k=0}^{\infty}\frac{(a+1)_k(b+1)_k\Delta^k\varphi(0)}{(a+b+2)_k k!} + \sum_{k=0}^{\infty}\frac{(a+1)_k(b+1)_k\varphi'(k)}{(k!)^2} + \sum_{k=0}^{\infty}\frac{(a+1)_k(b+1)_k\varphi(k)}{(k!)^2}\{\psi(a+1+k)+\psi(b+1+k)-2\psi(k+1)\} = 0$$
（证明：把 Entry 28 改写后对 $n$ 求导再令 $n = 0$）。

**出处。**Part II，Ch. 11，Entry 28（pp. 83–86）。证明：只需对基 $\varphi_m(x) = x(x-1)\cdots(x-m+1)$ 证；$m = 0$ 时即 Entry 25 在 $x = 1$ 的情形；对 $m$ 归纳 (28.1)–(28.4)。注：书中 $\Delta^k\varphi(0) = \sum_{j=0}^k(-1)^j\binom{k}{j}\varphi(j)$，即带 $(-1)^k$ 因子的前向差分；$\varphi(x) = x$ 时 $\Delta^1\varphi(0) = -1$。

**状态。**已证明；推论的逐项数值复核未做（见待核对清单）。

**对照。**M02；M13（差分与多项式基）；M12。

## Entry 29(i)——${}_3F_2$ 联络公式

**陈述。**$\mathrm{Re}(\alpha+\beta+\gamma-\delta-\varepsilon) < 0$、$\mathrm{Re}(\delta-\gamma-1) < 0$ 时，
$${}_3F_2[\alpha,\beta,\gamma;\delta,\varepsilon] = \frac{\Gamma(\delta)\Gamma(\delta-\alpha-\beta)}{\Gamma(\delta-\alpha)\Gamma(\delta-\beta)}\,{}_3F_2[\alpha,\beta,\varepsilon-\gamma;\alpha+\beta-\delta+1,\varepsilon] + \frac{\Gamma(\delta)\Gamma(\varepsilon)\Gamma(\alpha+\beta-\gamma)\Gamma(\delta+\varepsilon-\alpha-\beta-\gamma)}{\Gamma(\alpha)\Gamma(\beta)\Gamma(\varepsilon-\gamma)\Gamma(\delta+\varepsilon-\alpha-\beta)}\,{}_3F_2[\delta-\alpha,\delta-\beta,\delta+\varepsilon-\alpha-\beta-\gamma;\delta-\alpha-\beta+1,\delta+\varepsilon-\alpha-\beta].$$

**出处。**Part II，Ch. 11，Entry 29(i)（p. 86）。拉马努金在致 Hardy 第二封信中给出（Hardy 文集，p. xxviii）；证明见 Hardy 的文章（pp. 498–499、pp. 511–512）与 Bailey 专著 p. 21。

**状态。**已证明；但**印文有误**：数值复核表明第二系数的分子 $\Gamma(\alpha+\beta-\gamma)$ 应为 $\Gamma(\alpha+\beta-\delta)$（详见小结）。正文仍按原书印文转述，不擅自改动。

**对照。**M02；M07。

## Entry 29(ii)——${}_3F_2 = {}_4F_3$ 与正交多项式

**陈述。**$\alpha$、$\beta$ 或 $\gamma$ 为非负整数时，
$${}_3F_2[-2\alpha,-2\beta,-\gamma;-\alpha-\beta+\tfrac12,\delta] = {}_4F_3\left[-\alpha,-\beta,-\gamma,\gamma+\delta;-\alpha-\beta+\tfrac12,\tfrac12\delta,\tfrac12(\delta+1)\right]. \tag{29.1}$$

由此定义 $P_{2n}(x) = P_{2n}(x;\alpha,\gamma) = (-1)^n{}_4F_3[-n,n+\alpha+\gamma-\frac12,\gamma+ix,\gamma-ix;\alpha+\gamma,\gamma,\gamma+\frac12]$，则 $\{P_{2n}(x)\}$ 在 $(-\infty,\infty)$ 上关于权 $|\Gamma(\alpha+ix)\Gamma(\gamma+ix)|^2$ 正交；另有奇次多项式 $P_{2n+1}(x)$ 使 $\{P_n(x)\}$ 构成完全正交系（Askey–Wilson）；权函数在 $(-\infty,\infty)$ 上的积分最早由拉马努金算出（Ch. 10 已述）。

**出处。**Part II，Ch. 11，Entry 29(ii)（p. 86）。Askey–Wilson 近期给出简短证明（$\alpha$ 或 $\beta$ 为非负整数时）；$\gamma$ 为非负整数时，两端同乘 $(-\alpha-\beta+\frac12)_{\gamma}$ 后均为 $\alpha$ 的 $\gamma$ 次多项式，对一切非负整数 $\alpha$ 相等故恒等。

**状态。**已证明（Askey–Wilson）。

**对照。**M02；M13（正交多项式）；M09（权函数积分）。

## Entry 30——比值 $y$ 的导数公式

**陈述。**$\alpha+\beta+1 = \gamma+\delta$，$c = \Gamma(\alpha)\Gamma(\beta)/(\Gamma(\gamma)\Gamma(\delta))$，$y = c\cdot{}_2F_1(\alpha,\beta;\delta;1-x)/{}_2F_1(\alpha,\beta;\gamma;x)$，则
$$y' = -\frac{x^{-\gamma}(1-x)^{-\delta}}{{}_2F_1^2(\alpha,\beta;\gamma;x)}.$$

推论：$y = \frac{\pi}{\sin(\pi n)}\cdot{}_2F_1(n,1-n;1;1-x)/{}_2F_1(n,1-n;1;x)$ 时，$y' = -\frac{1}{x(1-x)\,{}_2F_1^2(n,1-n;1;x)}$（Entry 30 取 $\alpha = n$、$\beta = 1-n$、$\gamma = \delta = 1$）。

**出处。**Part II，Ch. 11，Entry 30（pp. 87–88）。证明：用 Entry 25、Wronskian 与 Abel 公式（$W(x) = -(\gamma-1)x^{-\gamma}(1-x)^{-\delta}$，(30.3)）及超几何微分方程 $x(1-x)y''+\{\gamma-(\alpha+\beta+1)x\}y'-\alpha\beta y = 0$（30.2，Bailey 书 p. 1）。

**状态。**已证明。

**对照。**M02；M11（椭圆积分的比值；推论即模量的导数）；M12（微分方程）。

## Entry 31(i)——积分恒等式

**陈述。**$y = {}_2F_1(\alpha,\beta;\gamma;x)$ 时，
$$(\alpha-1)(\beta-1)\int_0^x y\,dx - x(1-x)y' = (\gamma-1)(y-1) - (\alpha+\beta-1)xy.$$

**出处。**Part II，Ch. 11，Entry 31(i)（p. 88）。证明：求导后化归为超几何微分方程 (30.2)。

**状态。**已证明。

**对照。**M02；M12。

## Entry 31(ii)——「amazing」公式：双重积分 $= {}_3F_2$

**陈述。**$\alpha+\beta+1 = \gamma+\delta$，$n > 1$，$n > \mathrm{Re}\,\gamma$，$y = y(x) = {}_2F_1(\alpha,\beta;\gamma;x)$ 时，
$$y(x)\int_0^x\left\{\int_0^u t^{n-2}y(t)\,dt\right\}\cdot\frac{du}{u^{\gamma}(1-u)^{\delta}y^2(u)} = \frac{x^{n-\gamma}(1-x)^{1-\delta}}{(n-\gamma)(n-1)}\,{}_3F_2[n-\alpha,n-\beta,1;n,n-\gamma+1;x]. \tag{31.1}$$

推论：$n$ 任意、$y = {}_2F_1(n,1-n;1;x)$ 时，$x(x-1)y' = n(n-1)\int_0^x y\,dx$（Entry 31(i) 取 $\alpha = n$、$\beta = 1-n$、$\gamma = 1$）。

**出处。**Part II，Ch. 11，Entry 31(ii)（pp. 88–92）。注：$n$ 的条件仅为左端积分收敛所需；拉马努金的表述「somewhat imprecisely stated」。证明方法：先证左端满足非齐次超几何微分方程 $x(1-x)z''+\{\gamma-(\alpha+\beta+1)x\}z'-\alpha\beta z = x^{n-\gamma-1}(1-x)^{1-\delta}$，再证右端亦然（15 个幂级数的系数比较，(31.5)–(31.7)：消去 $(1-x)^{-\delta}$ 后系数化为关于 $u = n+k-1$ 的五次多项式，在 $u = 0$、$-1$、$\gamma-1$、$\alpha$、$\beta$ 五点为零且 $u^5$ 系数为零）；两解之差满足齐次方程 (30.2)，由幂级数展开比较知差不含 $y_1 = {}_2F_1(\alpha,\beta;\gamma;x)$ 与 $y_2 = x^{1-\gamma}{}_2F_1(\delta-\alpha,\delta-\beta;2-\gamma;x)$，故恒为零。

**状态。**已证明（Berndt）；表述不精确之处见待核对清单。

**对照。**M02；M12（微分方程证明法，本章仅见于 Entry 30、31）；M09（积分）。

## Entry 32(i)——偶函数（Entry 1 的特例）

**陈述。**$\varphi$ 为任意函数时，$\frac{1}{\sqrt{\varphi(x)}}\sum_{k=0}^{\infty}\frac{(\frac12)_k^2}{(k!)^2}\left\{1-\frac{\varphi(-x)}{\varphi(x)}\right\}^k$ 恒为 $x$ 的偶函数（级数收敛时）。

**出处。**Part II，Ch. 11，Entry 32(i)（p. 92）。证明：Entry 1 取 $r = m = \frac12$。

**状态。**已证明。

**对照。**M02。

## Entry 32(ii)——${}_2F_1(\frac12,\frac12;1)$ 的变换

**陈述。**$\frac12 < x < 2$ 时，
$${}_2F_1\left(\tfrac12,\tfrac12;1;1-\frac1x\right) = \sqrt{x}\,{}_2F_1\left(\tfrac12,\tfrac12;1;1-x\right).$$

**出处。**Part II，Ch. 11，Entry 32(ii)（p. 92）。特例：Pfaff 变换 (32.1)：${}_2F_1(a,b;c;z) = (1-z)^{-a}{}_2F_1(a,c-b;c;z/(z-1))$，一般归于 Gauss 或 Kummer，实为 Pfaff 首证；亦见 Ch. 10 Entry 19，证明见 Ch. 10 或 Bailey 书 p. 10 公式 (1)。

**状态。**已证明（Pfaff）。

**对照。**M02；M07；M11（完全椭圆积分的 Landen 变换）。

## Entry 32(iii)——四次变换

**陈述。**
$${}_2F_1\left(\tfrac12,\tfrac12;1;1-\left(\frac{1-x}{1+x}\right)^2\right) = (1+x)\,{}_2F_1\left(\tfrac12,\tfrac12;1;x^2\right).$$

**出处。**Part II，Ch. 11，Entry 32(iii)（p. 93）。证明：Entry 32(ii) 中 $x$ 换 $((1-x)/(1+x))^2$，再用 Entry 5（$r = \frac12$，$x$ 换 $-x$）。

**状态。**已证明。

**对照。**M02；M11。

## Entry 32(iv)——四次变换之二

**陈述。**
$${}_2F_1\left(\tfrac12,\tfrac12;1;1-\left(\frac{1-x}{1+x}\right)^4\right) = (1+x)^2{}_2F_1\left(\tfrac12,\tfrac12;1;x^4\right).$$

**出处。**Part II，Ch. 11，Entry 32(iv)（p. 93）。证明：Kummer 的公式 ${}_2F_1(\frac12,\frac12;1;c^2) = (2/(1+\sqrt{b}))^2{}_2F_1(\frac12,\frac12;1;((1-\sqrt{b})/(1+\sqrt{b}))^4)$，$c^2 = 1-b^2$，取 $b = ((1-x)/(1+x))^2$。

**状态。**已证明（Kummer）。

**对照。**M02；M11。

## Entry 32(v)——复参数求值

**陈述。**
$$(1+n^2)^{1/4}{}_2F_1\left(\tfrac12,\tfrac12;1;\tfrac12(1+in)\right) = \tfrac12(1+i)\,{}_2F_1\left(\tfrac12,\tfrac12;1;\tfrac12\left(1+\frac{n}{\sqrt{1+n^2}}\right)\right) + \tfrac12(1-i)\,{}_2F_1\left(\tfrac12,\tfrac12;1;\tfrac12\left(1-\frac{n}{\sqrt{1+n^2}}\right)\right).$$

**出处。**Part II，Ch. 11，Entry 32(v)（pp. 93–94）。证明：Erdélyi 书 p. 111 公式 (8) 取 $a = b = \frac14$、$z = n^2$ 得 (32.2)，公式 (9) 取 $a = b = \frac34$、$z = n^2/(1+n^2)$ 得 (32.3)，再用 (32.1) 与 Entry 21（$m = n = \frac12$，$x$ 换 $in$）。

**状态。**已证明。

**对照。**M02；M11。

## Entry 33(i)——Entry 2 的特例

**陈述。**
$${}_2F_1\left(\tfrac12,\tfrac12;1;\frac{2x}{1+x}\right) = \sqrt{1+x}\,{}_2F_1\left(\tfrac14,\tfrac34;1;x^2\right).$$

**出处。**Part II，Ch. 11，Entry 33(i)（p. 94）。证明：Entry 2 取 $r = m = \frac12$。

**状态。**已证明。

**对照。**M02；M11。

## Entry 33(ii)——Entry 12 的特例

**陈述。**
$${}_2F_1\left(\tfrac12,\tfrac12;1;\tfrac12(1-\sqrt{1-x})\right) = {}_2F_1\left(\tfrac14,\tfrac14;1;x\right).$$

**出处。**Part II，Ch. 11，Entry 33(ii)（p. 94）。证明：Entry 12 取 $x = y = -\frac14$、$z = 1$、$p$ 换 $x$。

**状态。**已证明。

**对照。**M02；M11。

## Entry 33(iii)——${}_3F_2 = {}_2F_1^2$

**陈述。**
$${}_3F_2\left(\tfrac12,\tfrac12,\tfrac12;1,1;x\right) = {}_2F_1^2\left(\tfrac14,\tfrac14;1;x\right).$$

**出处。**Part II，Ch. 11，Entry 33(iii)（p. 95）。证明：Entry 13 取 $\alpha = \beta = -\frac14$、$\gamma = \frac12$。

**状态。**已证明。

**对照。**M02。

## Entry 33(iv)——Entry 4 的特例

**陈述。**
$${}_2F_1\left(\tfrac14,\tfrac34;1;\frac{4x}{(1+x)^2}\right) = \sqrt{1+x}\,{}_2F_1\left(\tfrac12,\tfrac12;1;x\right).$$

**出处。**Part II，Ch. 11，Entry 33(iv)（p. 95）。证明：Entry 4 取 $r = m = \frac12$。

**状态。**已证明。

**对照。**M02；M11。

## Entry 33(v)——Erdélyi 公式特例

**陈述。**
$${}_2F_1\left(\tfrac14,\tfrac14;1;x\right) = \sqrt{1-x}\,{}_2F_1\left(\tfrac34,\tfrac34;1;x\right).$$

例 (i)：${}_2F_1(\frac14,\frac34;1;-\frac{4x}{(1-x)^2}) = \sqrt{\frac{1-x}{1+x}}\,{}_2F_1(\frac12,\frac12;1;\frac{x}{1+x})$（Entry 33(iv) 中 $x$ 换 $-x$ 再用 (32.1)）；例 (ii)：${}_2F_1(\frac14,\frac14;1;-\frac{4x}{(1-x)^2}) = \sqrt{1-x}\,{}_2F_1(\frac12,\frac12;1;x)$（用 Entry 33(iv)、例 (i) 与 Entry 33(ii)，其中 $\frac12(1-\sqrt{1-x})$ 换 $x/(x-1)$）；例 (iii)：${}_2F_1(\frac34,\frac34;1;-\frac{4x}{(1-x)^2}) = \frac{(1-x)^{3/2}}{1+x}\,{}_2F_1(\frac12,\frac12;1;x)$（Entry 33(v) 中 $x$ 换 $-\frac{4x}{(1-x)^2}$ 再用例 (ii)）。

**出处。**Part II，Ch. 11，Entry 33(v)（p. 95）。证明：Erdélyi 书 p. 105 公式 (1) 取 $a = b = \frac14$、$c = 1$。

**状态。**已证明。

**对照。**M02；M11。

## Entry 34——数值表与 $\mu$、$\eta$

**陈述。**（a）$\pi^{1/4}/\Gamma(\frac34) = 1.08643481121330801457531612$；（b）$\Gamma^2(\frac14)/(4\sqrt{2\pi}) = 1.311028777146060$；（c）$\sqrt{\pi}/\Gamma^2(\frac34) = 1.180340599016092$；（d）$\Gamma^2(\frac34)/\pi^{3/2} = 0.269676300594191$；（e）$\pi^{3/2}/\Gamma^2(\frac34) = 3.708149354602731$。

Berndt 注：(a)(b) 正确；(c)(d) 的末位应分别为 6 和 0，(e) 的末两位应为 44。$\Gamma(\frac34)$ 的数值取自 Fransén–Wrigge 的表；$\pi$ 的幂见 Fletcher 等人的表第 5 章。

为简便，设（34.1）
$$\mu = \frac{\sqrt{\pi}}{\Gamma^2(\frac34)}, \qquad \eta = \frac{\Gamma^2(\frac34)}{\pi^{3/2}}.$$
注：$\mu\eta = 1/\pi$。

**出处。**Part II，Ch. 11，Entry 34（p. 96）。

**状态。**数值表：(a)(b) 已核对正确（40 位复核：(a) 真值 $1.0864348112133080145753161215\ldots$，印文 30 位全对；(b) 真值 $1.3110287771460599\ldots$，印文为其 15 位四舍五入）；(c)(d)(e) 的末位错已由 Berndt 在书中注明并经本轮 30 位复核确认：(c) 真值 $1.1803405990160962\ldots$（15 位应为 $1.180340599016096$，末位 6）；(d) 真值 $0.2696763005941897\ldots$（15 位应为 $0.269676300594190$，末位 0）；(e) 真值 $3.7081493546027438\ldots$（15 位应为 $3.708149354602744$，末两位 44）。

**对照。**M10（Gamma 函数特殊值）；M04（$\Gamma(\frac14)$、$\Gamma(\frac34)$ 与 $\pi$ 的常数）。

## Entry 34(i)——Kummer 分解

**陈述。**$|x| < 1$ 时，
$${}_2F_1\left(\tfrac12,\tfrac12;1;\tfrac12(1+x)\right) = \mu\,{}_2F_1\left(\tfrac14,\tfrac14;\tfrac12;x^2\right) + \eta x\,{}_2F_1\left(\tfrac34,\tfrac34;\tfrac32;x^2\right).$$

**出处。**Part II，Ch. 11，Entry 34(i)（p. 96）。证明：用 Bailey 书 p. 11 公式 (2) 的 Kummer 公式求 ${}_2F_1(j+\frac12,j+\frac12;j+1;\frac12)$（34.2）。

**状态。**已证明。

**对照。**M02；M10；M11（完全椭圆积分 $K$ 的分解）。

## Entry 34(ii)——(34.3) 与三方争议

**陈述。**（原书印文）
$${}_2F_1\left(\tfrac12,\tfrac12;1;\tfrac12+\frac{x}{1+x^2}\right) = \mu\sqrt{1+x^2}\,{}_2F_1\left(\tfrac14,\tfrac14;\tfrac34;x^4\right) + \eta x(1+x^2)^{3/2}{}_2F_1\left(\tfrac34,\tfrac34;\tfrac54;x^4\right). \tag{34.3}$$

**出处。**Part II，Ch. 11，Entry 34(ii)（p. 97）。证明：先用 Entry 21（$m = n = \frac12$，$x$ 换 $2x/(1+x^2)$），再两次用 Entry 3（$x$ 换 $x^2$，$r = m = \frac14$ 与 $r = m = \frac34$）。注：拉马努金（笔记本 p. 141）在右端第二项误写 $(1+x^2)^{1/2}$ 而非 $(1+x^2)^{3/2}$。

**状态。**已证明（但**印文有误**，见下）。本轮数值裁决（mpmath 30 位，$x = 0.3$、$0.5$、$-0.2$ 三点）：

- Berndt 印文版 (34.3)：与左端差 $0.05$–$0.12$，**不成立**。错在两处：右端两个 ${}_2F_1$ 的第二参数应为 $\frac12$ 而非 $\frac14$、$\frac34$（Entry 3 取 $r = m$ 时第二参数为 $r-m+\frac12 = \frac12$）；第二项系数应为 $2\eta x(1+x^2)^{1/2}$ 而非 $\eta x(1+x^2)^{3/2}$。
- 拉马努金原版（第二项 $\eta x(1+x^2)^{1/2}$）：与左端差 $0.05$–$0.16$，**亦不成立**（缺因子 2，且第二参数亦错）。
- Rakha–Ibrahim–Rathie 的订正 (1.13)：
  $${}_2F_1\left(\tfrac12,\tfrac12;1;\tfrac12+\frac{x}{1+x^2}\right) = \mu\sqrt{1+x^2}\,{}_2F_1\left(\tfrac14,\tfrac12;\tfrac34;x^4\right) + 2\eta x\sqrt{1+x^2}\,{}_2F_1\left(\tfrac34,\tfrac12;\tfrac54;x^4\right),$$
  与左端差 $0$（三点均吻合到 $10^{-30}$），**正确**。其 (1.9)(1.10) 两式亦逐项数值证实无误。

正文仍按原书印文转述 (34.3)，不擅自改动；正确形式见上，详见小结。

**对照。**M02；M11。Ch. 10 待核对清单第 7 项（Rakha 短文页码问题）至此澄清：该短文确指本章 Entry 34(ii) 与 Entry 34 例 (ii)，不是 Ch. 10。

## Entry 34(iii)——乘积与二次变换的结合

**陈述。**
$$\frac\pi4\,{}_2F_1^2\left(\tfrac12,\tfrac12;1;\tfrac12(1+x)\right) - \frac\pi4\,{}_2F_1^2\left(\tfrac12,\tfrac12;1;\tfrac12(1-x)\right) = x\sum_{n=0}^{\infty}\frac{n!x^{2n}}{(\frac32)_n}\,{}_3F_2\left[\tfrac12,\tfrac12,-n;1,1\right] = x+\frac{x^3}{2}+\frac{41x^5}{120}+\frac{21x^7}{80}+\cdots = \frac{x}{1-x^2}-\frac{x^3}{2(1-x^2)^2}+\frac{41x^5}{120(1-x^2)^3}+\cdots. \tag{34.4}$$

**出处。**Part II，Ch. 11，Entry 34(iii)（pp. 97–98）。证明：后两个等式是左端前四个系数的数值计算（拉马努金显然没有 $x^{2k-1}/(1-x^2)^k$（$k \ge 1$）的系数的通用公式）；第一个等式用 Entry 21 与 (34.1) 得 (34.5)，再用 Erdélyi 书 p. 187 公式 (14) 与 p. 85 公式 (2)，最后归约为 Entry 29(i) 的特例。

**状态。**已证明（首等式）；后两等式只算到 $x^7$ 项。

**对照。**M02；M12。

## Entry 34 例 (i)——Entry 34(i) 加 Pfaff 变换

**陈述。**
$${}_2F_1\left(\tfrac12,\tfrac12;1;\tfrac12(1+x)\right) = \mu(1-x^2)^{-1/4}{}_2F_1\left(\tfrac14,\tfrac14;\tfrac12;\frac{x^2}{x^2-1}\right) + \eta x(1-x^2)^{-3/4}{}_2F_1\left(\tfrac34,\tfrac34;\tfrac32;\frac{x^2}{x^2-1}\right).$$

**出处。**Part II，Ch. 11，Entry 34 例 (i)（p. 98）。证明：用 Entry 34(i) 再用 (32.1)；拉马努金（笔记本 p. 142）误写 $(1-x^2)^{-5/4}$ 而非 $(1-x^2)^{-3/4}$。

**状态。**已证明。

**对照。**M02；M07。

## Entry 34 例 (ii)——拉马努金原版正确

**陈述。**（原书印文）
$$\sqrt{1-x^2}\,{}_2F_1\left(\tfrac12,\tfrac12;1;\tfrac12+\frac{x}{1+x^2}\right) = \mu\,{}_2F_1\left(\tfrac12,\tfrac12;\tfrac34;\frac{x^4}{x^4-1}\right) + \eta x(1+x^2)\,{}_2F_1\left(\tfrac12,\tfrac12;\tfrac54;\frac{x^4}{x^4-1}\right).$$

**出处。**Part II，Ch. 11，Entry 34 例 (ii)（p. 99）。证明：对 Entry 34(ii) 右端两函数各用 (32.1)；拉马努金（笔记本 p. 142）误写 $2$ 而非 $1+x^2$。

**状态。**已证明（但**印文有误**，见下）。本轮数值裁决（mpmath 30 位，$x = 0.3$、$0.5$、$-0.2$ 三点）：拉马努金原版（第二项系数 $2\eta x$）与左端差 $0$，**正确**；Berndt 印文版（第二项系数 $\eta x(1+x^2)$）与左端差 $0.05$–$0.10$，**不成立**。Rakha 短文称拉马努金原版正确、Berndt 版有误，数值复核支持 Rakha 的这一判断。

**对照。**M02；M07。

## Entry 35(i)——余弦的超几何表示

**陈述。**$n$ 任意时，
$$\cos(2n\sin^{-1}x) = {}_2F_1\left(n,-n;\tfrac12;x^2\right).$$

**出处。**Part II，Ch. 11，Entry 35(i)（p. 99）。证明：Erdélyi 书 p. 101 公式 (11)，取 $a = 2n$、$z = \sin^{-1}x$。

**状态。**已证明。

**对照。**M02；M13（Chebyshev 多项式：$n$ 为整数时右端即 $T_{2n}$ 的表示）；M14。

## Entry 35(ii)——正弦的超几何表示

**陈述。**$n$ 任意时，
$$\sin(2n\sin^{-1}x) = 2nx\,{}_2F_1\left(\tfrac12+n,\tfrac12-n;\tfrac32;x^2\right).$$

**出处。**Part II，Ch. 11，Entry 35(ii)（p. 99）。证明：Erdélyi 书 p. 101 公式 (12)。

**状态。**已证明。

**对照。**M02；M13（Chebyshev 多项式）。

## Entry 35(iii)——余弦的第二表示

**陈述。**$n$ 任意时，
$$(1-x^2)^{-1/2}\cos(2n\sin^{-1}x) = {}_2F_1\left(\tfrac12+n,\tfrac12-n;\tfrac12;x^2\right).$$

**出处。**Part II，Ch. 11，Entry 35(iii)（p. 99）。证明：用 Entry 35(i) 与 (17.3)，系数比较用 Saalschütz 定理（Ch. 10 Entry 2）。注：Entry 35(i)(ii) 与 Tschebyscheff 多项式密切相关。

**状态。**已证明。

**对照。**M02；M13（Chebyshev 多项式）；M07（Saalschütz 定理）。

## Entry 36(i)(ii)——$(x+1)^{\pm n/2}$ 的 $b_k(n)$ 展开

**陈述。**$n$ 为实数，$k \ge 2$，$b_k(n) = n^2(n^2-2^2)(n^2-4^2)\cdots(n^2-(k-2)^2)$（$k$ 偶）或 $n(n^2-1^2)(n^2-3^2)\cdots(n^2-(k-2)^2)$（$k$ 奇）；$2-2\sqrt2 \le x \le 2+2\sqrt2$ 时，
$$(x+1)^{n/2} - (x+1)^{-n/2} = \frac{nx}{\sqrt{1+x}} + 2\sum_{k=1}^{\infty}\frac{b_{2k+1}(n)}{(2k+1)!}\left(\frac{x}{2\sqrt{1+x}}\right)^{2k+1}, \tag{36.1}$$
$$(x+1)^{n/2} + (x+1)^{-n/2} = 2 + 2\sum_{k=1}^{\infty}\frac{b_{2k}(n)}{(2k)!}\left(\frac{x}{2\sqrt{1+x}}\right)^{2k}. \tag{36.2}$$

**出处。**Part II，Ch. 11，Entry 36(i)(ii)（p. 100）。Berndt 注：表述与拉马努金略有不同。证明：用 Ch. 3 第 14 节推论 2（$(a+\sqrt{1+a^2})^n = 1+na+\sum_{k\ge 1}b_k(n)a^k/k!$，$|a| \le 1$），取 $a = x/(2\sqrt{1+x})$。

**状态。**已证明。

**对照。**M02；M13（Ch. 3 第 14 节的 $b_k(n)$）；M12。

## Entry 36(iii)(iv)——Lagrange 反演展开

**陈述。**$n$ 为实数，$|x/(1+x)^{3/2}| \le 2/3^{3/2}$（36.5）时，
$$\left(\frac{1+\sqrt{1+4x}}{2}\right)^n = 1+nx(1+x)^{(n-3)/2} + \frac{n(n-5)(n-7)}{4\cdot 3!}x^3(1+x)^{(n-9)/2} + \frac{n(n-7)(n-9)(n-11)(n-13)}{4^2\cdot 5!}x^5(1+x)^{(n-15)/2} + \cdots, \tag{36.6}$$
且
$$\tfrac12+\tfrac12\left(\frac{1+\sqrt{1+4x}}{2}\right)^n = (1+x)^{n/2} + \frac{n(n-4)}{4\cdot 2!}x^2(1+x)^{(n-6)/2} + \frac{n(n-6)(n-8)(n-10)}{4^2\cdot 4!}x^4(1+x)^{(n-12)/2} + \cdots. \tag{36.7}$$

**出处。**Part II，Ch. 11，Entry 36(iii)(iv)（pp. 100–102）。Berndt 注：按拉马努金原样呈现；$(x/(1+x)^{3/2})^k$（$k \ge 0$）的系数通式可用 Gamma 函数给出。证明：Lagrange 反演公式（Whittaker–Watson 书 p. 133）：取 $\varphi(x) = 1/\sqrt{1+x}$、$f(x) = (1+x)^{n/2}$，$y = x+x\varphi(y)$，解得 $y = \frac12(2x-1+\sqrt{1+4x})$，得 (36.9)：$((1+\sqrt{1+4x})/2)^n = (1+x)^{n/2}\sum_{k=0}^{\infty}(-1)^{k+1}\frac{\Gamma(\frac12(-n+3k))}{\Gamma(\frac12(-n+3k)-k+1)k!}(x/(1+x)^{3/2})^k$；Stirling 公式知级数在 (36.5) 的 $x$ 收敛；第二次应用 Lagrange 反演（$\varphi(x) = -1/\sqrt{1+x}$）得 (36.10)，(36.9) 减 (36.10) 得 (36.6)，相加得 (36.7）。

章末注：拉马努金偏爱 Lagrange 反演公式（大概从 Carr 的《Synopsis》学到；亦见 Edwards、Williamson 的微积分书）；他在第二本笔记 Ch. 3 与季报中多处应用；他得出这些展开式的主要方法是一种积分变换中的插值公式（Hardy 书第 11 章与 Berndt 的季报论述有详述）；$q$-Lagrange 反演公式的综述见 Stanton。

**状态。**已证明。

**对照。**M02；M13（Lagrange 反演，见 Ch. 3）；M12。

## 小结

- 本章是超几何级数的下半篇：Entry 1–8 为 Kummer、Gauss 的二次变换及其直接推论（Entry 2、3 为全章工作母机，Entry 7 由 Entry 2 取极限得）；Entry 9–12 为 Bessel 型 ${}_0F_1$ 与 Gauss 二次变换（Entry 12 的推论与例 1 的 $(1^2+n)(5^2+n)\cdots$ 级数是拉马努金式恒等式的典型）；Entry 13–20 为乘积定理（Clausen、Bailey、Schläfli、Hardy），例 1–10 给出一批初等三角–双曲与阶乘级数恒等式；Entry 21 为 Kummer 分解公式，是 Entry 34 的源头；Entry 22 为「amazing」公式之一（Legendre 多项式与 $A_k$ 递归序列）；Entry 23 表面无意义；Entry 24–28 为解析延拓与渐近理论（推论 2 的零平衡 ${}_3F_2$ 渐近是本章理论高点，定理 1、2 为其严格化）；Entry 29–31 为联络公式与微分方程（Entry 31(ii) 为「amazing」公式之二）；Entry 32–33 为 $\frac12$、$\frac14$ 参数的变换群（多为前述条目的特例）；Entry 34 为 $\Gamma(\frac14)$、$\Gamma(\frac34)$ 常数与 Kummer 分解的数值–解析交汇点；Entry 35–36 为三角函数的超几何表示与 Lagrange 反演展开，收束全章。
- 与 Ch. 10 的互见：Entry 3、21 的 Kummer 公式与 Ch. 10 Entry 21 同源；Entry 12 的证明用 Ch. 10 (32.2) 与 Gauss 定理；Entry 13 的 Clausen 恒等式与 Ch. 10 Entry 31 相关；Entry 17、19、20 的证明用 Dixon 定理（Ch. 10 Entry 7）；Entry 24 引理 1 即 Ch. 10 Entry 27 的重述；Entry 25 的解析延拓与 Ch. 10 Entry 15 的渐近互补；Entry 27 (27.2) 的证明用 Ch. 10 (6.3)；Entry 29(i) 的证明见 Hardy 文章与 Bailey 专著；Entry 32(ii) 的 Pfaff 变换见 Ch. 10 Entry 19；Entry 35(iii) 的证明用 Saalschütz 定理（Ch. 10 Entry 2）；Entry 36 的 $b_k(n)$ 见 Ch. 3 第 14 节。
- 数值复核（mpmath 30 位；脚本在工作目录，未入仓库）：verify1（Entries 1–22）75 项与 verify2（Entries 24–36）71 项，合计约 146 项检查全部通过。复核内容：Entry 2、3、4、5、6、7 及推论、Entry 1（$\varphi = e^x$ 的偶性）、Entry 8（$m = 0.8$、$1.3$）、Entry 9（$n = 2$、$3$）与推论 $I_0$ 渐近（$x = 10$，相对误差 $1.4\times 10^{-5}$，合截断量级）、Entry 10（$n = 2$、$3$）与推论 (10.1) 大根（$n = 2$ 时真根 $4.4934095$、公式近似 $4.5161091$，误差 $0.0227$，合三项渐近量级）、Entry 11 (11.11)（$n = 0$–$6$ 精确成立）与 (11.3)(11.4)（$x = 10$，差 $1.7\times 10^{-5}$、$1.9\times 10^{-5}$，合五项截断量级）、Entry 12（两组）与推论（$n = 1.5$、$x = 0.2$，差 $6.9\times 10^{-21}$）、Entry 13 Clausen（两组）与推论 2（$x = 0.5$、$1.2$）、Entry 14（两组）、Entry 15（两组）、Entry 16（两组）、Entry 17（两组）、Entry 18 及 (18.1)（两组）、Entry 19（$\alpha = 2$、$3$）、Entry 20（两组）与例 4、例 6、Entry 21（两组）、Entry 22（$A_1$、$A_2$、$A_3$（$p = 1$、$3$、$10$）、(22.2) 末项系数、(22.22)（$n = 2$、$j = 1$；$n = 3$、$j = 1$；$n = 2$、$j = 2$，精确成立）、(22.23)（$n = 1$、$j = 1$；$n = 2$、$j = 1$，精确成立）、(22.3)（$m = -1$、$x = 0.5$））、Entry 24 推论 2（$x = 0.001$，差 $0.009$，合 $O(x\mathrm{Log}\,x)$ 量级）、Entry 25（两组）、Entry 26（两组）与推论（$x = 0.3$、$0.1$）及例 (26.2) 双重积分（$x = 0.3$，差 $2\times 10^{-31}$）、Entry 27（$x = 0.3$、$-0.2$）、(27.2)（$n = 1$–$6$，精确分数成立）与例 1（$x = 0.1$，差 $1.6\times 10^{-6}$，合截断量级）、Entry 28（$\varphi(x) = x$，差 $6.5\times 10^{-12}$）、Entry 29(i)（订正版，差 $3.9\times 10^{-31}$；印文版差 $0.0037$–$3.65$）、Entry 29(ii)（精确成立）、Entry 30（数值导数，差 $1.6\times 10^{-30}$）、Entry 31(i)（差 $1.2\times 10^{-32}$）、Entry 31(ii) (31.1)（差 $0$）、Entry 32(ii)(iii)(iv)(v)、Entry 33(i)–(v) 与例 (i)(ii)(iii)、Entry 34(i)（两组）、Entry 34(ii) 三版本对决、Entry 34 例 (ii) 两版本对决、Entry 34(iii) 级数系数（$x = 0.1$、$0.2$）、Entry 34 数值 (a)–(e)（30–40 位）、Entry 35(i)(ii)(iii)（两组）、Entry 36(i)(ii)（两组）与 (36.6)(36.7) 前三项（$x = 0.1$、$0.05$）。复核中的插曲（均已解决，非书错）：mpmath 无 `hyp0f2`，改用 `mp.hyper([], [..], z)`；Entry 9 推论与 Entry 11 (11.3)(11.4) 的绝对容差须按渐近截断量级放宽；Entry 12 推论左端乘积因子初版误写为 $(2j-1)^2+n$（应为 $(4j-3)^2+n$）且分母误写 $(2j)^2$（应为 $(4j)^2$）；Entry 13 Clausen 第一组参数 $\gamma = -0.5$ 使 ${}_3F_2$ 分母参数 $2\gamma = -1$ 触极点，改 $\gamma = -0.4$；Entry 22 (22.2) 末项系数提取的 Richardson 组合误写且多乘因子 $p$，修正后通过（$k = 3$、$4$ 余差 $2$–$4\times 10^{-6}$ 为外推截断误差，容差放宽至 $10^{-5}$ 后通过）；Bernoulli 数改用 `mp.bernoulli`（原手写字典只到 $B_{10}$，$A_{12}$ 需 $B_{22}$ 曾报 KeyError）；Entry 26 推论、Entry 27 的 30 位容差须放宽至 $10^{-15}$（级数截断）；Entry 27 (27.2) 的 mpmath `rf` 在负整数参数处经 Gamma 比值会丢精度，改精确分数复核后 $n = 1$–$6$ 精确成立；Entry 28 的 RHS 求和初版漏 $\Delta^1\varphi(0) = -1$（Berndt 的 $\Delta$ 定义带 $(-1)^k$ 因子）与 $(a+1)(b+1)/(a+b+n+2)$ 因子，修正后通过；Entry 29(i) 的印文问题见下；Entry 34(ii) 与例 (ii) 的三方争议见下；Entry 36(i)(ii) 的 $n = 2.2$、$x = 1.0$ 组余差 $1.9\times 10^{-16}$ 为交错级数抵消噪声，容差放宽至 $10^{-12}$ 后通过。
- **本轮发现的原书印文问题**（数值证实，原文未改动，标待核对）：
  1. **Entry 29(i) 第二系数分子印文有误**：原文印 $\Gamma(\alpha+\beta-\gamma)$，应为 $\Gamma(\alpha+\beta-\delta)$。证据三重：(a) 由 ${}_2F_1$ 联络公式（Abramowitz–Stegun 15.3.6）与 ${}_3F_2$ 的积分表示直接推导，第二系数应为 $\Gamma(\delta)\Gamma(\varepsilon)\Gamma(\alpha+\beta-\delta)\Gamma(\delta+\varepsilon-\alpha-\beta-\gamma)/(\Gamma(\alpha)\Gamma(\beta)\Gamma(\varepsilon-\gamma)\Gamma(\delta+\varepsilon-\alpha-\beta))$；(b) 三组随机参数直接求和（50 位，20000 项）复核：订正版差 $1.6\times 10^{-8}$、$1.3\times 10^{-4}$、$2.5\times 10^{-7}$（均为直接求和截断量级），印文版差 $0.0037$、$0.705$、$3.65$；(c) 终止情形 $\gamma = 0$ 的精确检验：订正版得 $0.99995 \approx 1 = $ 左端，印文版得 $1.5698$。300 DPI 放大图确认印文确为 $\Gamma(\alpha+\beta-\gamma)$。
  2. **Entry 34(ii) 的 (34.3) 印文两处有误**：(a) 右端两个 ${}_2F_1$ 的第二参数应为 $\frac12$ 而非 $\frac14$、$\frac34$——Entry 3 取 $r = m$ 时第二参数为 $r-m+\frac12 = \frac12$，两处 Entry 3 特例逐项数值证实（差 $0$，而印文参数差 $7\times 10^{-4}$–$1.4\times 10^{-2}$）；(b) 第二项系数应为 $2\eta x(1+x^2)^{1/2}$ 而非 $\eta x(1+x^2)^{3/2}$。正确形式即 Rakha–Ibrahim–Rathie 短文的 (1.13)，三点数值复核差 $0$；Berndt 印文版差 $0.05$–$0.12$；拉马努金原版（$\eta x(1+x^2)^{1/2}$，缺因子 2）差 $0.05$–$0.16$。三方中只有 Rakha 的 (1.13) 成立。
  3. **Entry 34 例 (ii) 印文有误，拉马努金原版正确**：Berndt 印文版第二项系数 $\eta x(1+x^2)$ 与左端差 $0.05$–$0.10$；拉马努金原版（笔记本 p. 142）第二项系数 $2\eta x$ 与左端差 $0$（三点均吻合到 $10^{-30}$）。Rakha 短文称拉马努金原版正确、Berndt 版有误，数值复核支持 Rakha 的这一判断。附带：本轮 300 DPI 放大图确认例 (ii) 印文第二项的 ${}_2F_1$ 参数确为 $(\frac12,\frac12;\frac54)$，150 DPI 曾误读为 $(\frac14,\frac14;\frac54)$。
  4. **Entry 34 数值 (c)(d)(e) 末位错**：Berndt 已在书中注明（(c) 末位应为 6、(d) 末位应为 0、(e) 末两位应为 44），本轮 30 位复核确认（见 Entry 34 节）；(a)(b) 正确（(a) 40 位复核全对）。
- **Rakha–Ibrahim–Rathie 短文已澄清**：Medhat A. Rakha、Adel K. Ibrahim、Arjun K. Rathie，〈Remark on two results due to Ramanujan on hypergeometric series〉，arXiv:1302.4902v1，2013-02-20。短文的 (1.1) = 拉马努金笔记本 p. 141 的结果 = 本章 **Entry 34(ii)**；短文的 (1.2) = 拉马努金笔记本 p. 142 的结果 = 本章 **Entry 34 例 (ii)**。Ch. 10 待核对清单第 7 项「疑指 Ch. 11」至此落实。短文的两个判断均经本轮数值复核证实：其一，Entry 34(ii) 的拉马努金原版与 Berndt 版均有误，正确形式是短文的 (1.13)（三点复核差 $0$）；其二，Entry 34 例 (ii) 的拉马努金原版正确、Berndt 版有误（三点复核差 $0$ 对 $0.05$–$0.10$）。
- 拉马努金原文疏失（Berndt 已指出）：见章首背景列表；其中 Entry 34(ii) 与例 (ii) 的「拉马努金误写」断言经本轮复核须修正：Entry 34(ii) 拉马努金版确实有误（但 Berndt 的修正版亦有误，正确的是 Rakha (1.13)）；Entry 34 例 (ii) 拉马努金版实为正确，Berndt「误写 $2$ 而非 $1+x^2$」的断言不成立。

## 待核对清单

1. IMSC 整理表本章的结果数（2026-11-06 实测 imsc.res.in 当日不可达，未能补录；此前 Ch. 1–10 亦多次不可达）。
2. **Entry 29(i) 的本轮发现**：第二系数分子 $\Gamma(\alpha+\beta-\gamma)$ 应为 $\Gamma(\alpha+\beta-\delta)$（推导 + 三组随机参数 50 位复核 + $\gamma = 0$ 终止情形精确检验），与印文相左，须独立核对（或查其他印次、勘误表）。
3. **Entry 34(ii) 与例 (ii) 的本轮发现**：(34.3) 印文两处有误（第二参数 $\frac12$、系数 $2\eta x(1+x^2)^{1/2}$），正确形式为 Rakha (1.13)；例 (ii) 拉马努金原版 $2\eta x$ 正确、Berndt 版有误；均经三点 30 位数值复核，须独立核对（或查其他印次、勘误表）。
4. Entry 34 数值 (c)(d)(e) 的末位错是否见于其他印次或勘误表（Berndt 已在书中注明）。
5. Berndt 章首计数（本章共几条陈述）：章首导言未见计数句，待核对原书章首。
6. TIFR 影印版页码：Berndt 文中明确引用的有 Entry 18（笔记本 p. 133）、Entry 34(ii)（笔记本 p. 141）、Entry 34 例 (i)(ii)（笔记本 p. 142）；其余各条的 TIFR 页码待核对。
7. Entry 23 的意图（Berndt：或将永远是谜）；Entry 27 例 1–4 的意图（Berndt 明言不知）。
8. Entry 24 主恒等式 (24.1) 与推论 1 的适用函数问题（Berndt：很可能不存在使恒等式成立的 $\varphi$）；推论 2 的来源（Berndt 不知如何从 Entry 24 得出）。
9. Entry 28 推论的逐项数值复核（主恒等式已复核 $\varphi(x) = x$ 一点；推论为对 $n$ 求导所得，未逐项复核）。
10. Entry 31(ii) 表述不精确之处的细节（Berndt：拉马努金表述「somewhat imprecisely stated」；$n$ 的条件仅为积分收敛所需）。
11. Entry 11 例 1–3、Entry 12 例 1、Entry 20 例 1–10、Entry 27 例 1–4 的确切形式（本文件只给主题与已核对的几条；例 1–10 的级数已按原文转录，个别长式未逐项数值复核）。
12. Entry 22 (22.2) 的 $p^j$ 系数通式（原文表述不严谨；$A_k$ 由递推 (22.13) 良定义，已数值复核）。

## 来源说明

- 整理本：Bruce C. Berndt, *Ramanujan's Notebooks*, Part II, Springer, 1989, Ch. 11, pp. 48–102。电子版：archive.org 标识符 `ramanujan_notebooks_ii`（《Ramanujan's Notebooks, Part 2》），PDF 14,538,056 字节、371 叶，DjVu OCR 文本 560,610 字节。**PDF 页与书页对应关系：PDF 页 = 书页 + 12**（与 Part I 的 +10 不同；实测 Ch. 10 章首 PDF 页 19、Ch. 11 章首 PDF 页 60、Ch. 11 末页书页 47 在 PDF 页 59、Ch. 12 章首书页 103）。本章范围：书页 48–102，PDF 页 60–114，共 55 页。全部公式按 PDF 原图（150 DPI）逐字转录，关键公式另用 300 DPI 放大图确认（Entry 29(i) 的 $\Gamma(\alpha+\beta-\gamma)$、Entry 34 (34.1) 的 $\eta = \Gamma^2(\frac34)/\pi^{3/2}$、Entry 34 例 (ii) 的 $(\frac12,\frac12;\frac54)$ 参数、Entry 34(ii) 的 (34.3)）。
- 目录核对：Part II 目录（PDF 页 12）确认 Ch. 10 Hypergeometric Series, I 起书页 7；Ch. 11 Hypergeometric Series, II 起书页 48；Ch. 12 Continued Fractions 起书页 103；Ch. 13 Integrals and Asymptotic Expansions 起书页 185；Ch. 14 Infinite Series 起书页 240；Ch. 15 Asymptotic Expansions and Modular Forms 起书页 300。
- 书目：Part II，Springer，1989，XII + 360 页，DOI 10.1007/978-1-4612-4530-8，ISBN 0-387-96794-X。
- 另引：Medhat A. Rakha、Adel K. Ibrahim、Arjun K. Rathie，〈Remark on two results due to Ramanujan on hypergeometric series〉，arXiv:1302.4902v1 [math.CV]，2013-02-20（全文已读；其 (1.1)/(1.2) 分别对应本章 Entry 34(ii) 与 Entry 34 例 (ii)）。
- 数值复核：mpmath 30 位（个别 40–50 位）；复核脚本在工作目录（未入仓库）。下一章：Part II Ch. 12 Continued Fractions。
