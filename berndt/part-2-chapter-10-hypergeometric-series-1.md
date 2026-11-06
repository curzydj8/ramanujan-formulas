# Part II · 第 10 章 Hypergeometric Series, I（超几何级数（一））

出处：Bruce C. Berndt, *Ramanujan's Notebooks*, Part II, Springer, 1989, 第 10 章，pp. 7–47（Part II 的第一章；本书 Part II 覆盖第二本笔记第 10–15 章）。对应拉马努金**第二本笔记第 10 章**（亦与第一本笔记第 12 章内容相应，见下）。

## 背景与记号

- 本章主题：超几何级数的经典定理与求值。Berndt 在章首导言（pp. 7–8）说明：Hardy 1923 年的综述只覆盖了第一本笔记第 12 章的一部分；本章对应第二本笔记第 10 章，含有 Hardy 未提及的大量结果，第二本笔记中亦有第一本所无的材料。拉马努金独立重新发现了超几何级数理论中的许多主要经典定理，特别是 Gauss、Kummer、Dougall、Dixon、Saalschütz、Thomae 的定理，以及 Whipple 变换的特例。拉马努金几乎没有留下他如何发现这些结果的线索：第一本笔记中有少量简短的证明草图，第二本笔记中唯一的证明草图在 Entry 8（Gauss 定理）之后，本章将给出拉马努金的这一论证。
- 本章的许多结果是超几何函数在自变量 $+1$ 或 $-1$ 处的优美求值；许多二项系数和可用 Gauss、Dixon、Saalschütz、Kummer 等定理求值（见 R. Roy 的文章）。
- **记号**（$\mathrm{Log}$ 为自然对数；$\gamma = 0.577215664901533\ldots$ 为 Euler 常数；$\psi$ 为 digamma 函数）：
  - 上升阶乘（Pochhammer 记号）$(a)_k = \Gamma(a+k)/\Gamma(a)$，$k$ 为任意复数；
  - 广义超几何级数
    $${}_pF_q\left[\begin{matrix}a_1, \ldots, a_{p} \\ b_1, \ldots, b_q\end{matrix}; z\right] = \sum_{k=0}^{\infty} \frac{(a_1)_k \cdots (a_p)_k}{(b_1)_k \cdots (b_q)_k} \frac{z^k}{k!}, \tag{0.1}$$
    本章只涉及 $p = q+1$ 的情形；$|z| < 1$ 时收敛，$z = 1$ 时收敛条件为 $\mathrm{Re}(a_1+\cdots+a_{p}) < \mathrm{Re}(b_1+\cdots+b_q)$，$z = -1$ 时为 $\mathrm{Re}(a_1+\cdots+a_{p}) < \mathrm{Re}(b_1+\cdots+b_q)+1$；$z = 1$ 时常省略自变量。拉马努金本人没有超几何记号，所有公式都写出级数的前几项；Berndt 为简洁多用紧凑记号，个别特别优美的例子沿用拉马努金的做法；
  - digamma 函数的级数表示
    $$\psi(z+1) = -\gamma + \sum_{k=1}^{\infty}\left(\frac{1}{k} - \frac{1}{k+z}\right), \tag{0.2}$$
  - 微分公式
    $$\left.\frac{d}{du}(\pm u)_k\right|_{u=0} = \pm(k-1)!, \qquad k \ge 1. \tag{0.3}$$
- 本章在原文中明确出现编号的 Entry 共 **35 条**：Entry 1–35，**无缺号**；另有分体 Entry 12(a)/12(b)、Entry 18(i)/18(ii)/18(iii)、Entry 29(a)/29(b)/29(c)/29(d)、Entry 35(i)/35(ii)/35(iii)/35(iv)，共 **44 个 Entry 标题**。Berndt 章首计数（本章共几条陈述）未在章首导言中找到，待核对原书章首；IMSC 整理表本章的结果数本次未能读取（imsc.res.in 当日不可达），待补。
- **本章的拉马努金原文疏失**（Berndt 已指出，详见各条与末尾小结）：Entry 1 未说明 $-x-y-z-u-2n-1$ 为正整数的情形亦成立；Entry 2 Hardy 的表述有误；Entry 4 例 (iv) 笔记本（p. 118）把 $\Gamma(3x+1)$ 误放分子；Entry 7 推论 6 (7.3) 笔记本（p. 119）写 $k!$ 应为 $(k-1)!$；Entry 7 推论 21 笔记本（p. 120）漏记 $-1/k$ 求和项；Entry 13 推论 1 拉马努金在笔记本（p. 124）为推论 1 重定义 $S_r$；Entry 14 拉马努金表述（笔记本 p. 124）「somewhat imprecise」；Entry 18(ii) 拉马努金断言为假；Entry 32 拉马努金未提 $x+y+z = 0$ 的前提（见本轮发现）；Entry 35(i) 拉马努金的 $\varphi(n)$ 定义不严谨，应按 (29.1) 定义，且第一本笔记（p. 239）中 35(iv) 列在 (35.10)(35.11) 之前。
- **本轮发现的原书印文问题**（数值证实，详见末尾小结）：Entry 15 推论的 $\mathrm{Log}\,x + 4\mathrm{Log}\,2$ 应为 $-\mathrm{Log}\,x + 4\mathrm{Log}\,2$（符号错）；Entry 32 后的注释称 (32.1) 在 $x+y+z \ne 0$ 时一般为假并举例 $x = 2$、$y = z = -1/2$，但 (32.1) 在该例对一切 $n$ 均成立，且有初等证明表明 (32.1) 对一般参数恒成立（待独立核对）。

## 本章结构

| Entry | 页 | 内容 |
|---|---|---|
| Entry 1 | 9 | Dougall 定理 ${}_7F_6$ (1.1)，1907 年 |
| Entry 2 | 9 | Saalschütz 定理 ${}_3F_2$；Pfaff 1797 年首证 |
| Entry 3 | 9–10 | ${}_6F_5$ 闭式（Entry 1 取 $u = -1$） |
| Entry 4 | 10–11 | 对 (1.1) 取对数微分得 $\psi$ 和；例 (i)–(v) |
| Entry 5 | 11–12 | Dougall ${}_5F_4$ (5.1)；部分和记号 |
| Entry 6 | 12–14 | ${}_5F_4$ 部分和渐近；Second Version（Evans 简化证明，Whipple 变换 (6.1)）；推论（$\pi^2/4\,{}_5F_4$ 的对数奇性） |
| Entry 7 | 15–19 | Dixon 定理 ${}_3F_2$；推论 1–24 |
| Entry 7 例 1–20 | 20–25 | 二项系数级数求值；例 14 $= 2/\pi$（Bauer 1859 年首证）；例 20 Morley 1902 年 |
| Entry 8 | 25 | Gauss 定理 ${}_2F_1$ (8.1)；拉马努金证明草图 (8.2)(8.3) |
| Entry 9 | 25 | $\sum (\beta)_k/(k(\alpha)_k) = \psi(\alpha)-\psi(\alpha-\beta)$ (9.1) |
| Entry 10 | 25–27 | (10.1)；例 1–7 |
| Entry 11 | 27–28 | 望远镜和；推论 1、2 |
| Entry 12(a) | 28 | 指数公式递推 $nP_n = \sum A_kP_{n-k}$ (12.1) |
| Entry 12(b) | 28–29 | Newton 恒等式 (12.2) |
| Entry 13 | 30–32 | (13.5)；$\varphi(r)$ 递推 (13.2)、引理 (13.3)；推论 1 (13.6)、推论 2；例 1、2 |
| Entry 14 | 32–33 | 双重和恒等式；$S_m(x)$、$C_{m,n}(x)$ |
| Entry 15 | 33–34 | 部分和渐近；推论（$\pi\,{}_2F_1$ 的对数奇性，印文符号有误） |
| Entry 16 | 34 | 二项反演公式 |
| Entry 17 | 34–35 | 移位公式 (17.1)(17.2) |
| Entry 18(i) | 35 | (18.2)：$e^x$ 乘幂级数 |
| Entry 18(ii) | 35–36 | 拉马努金断言为假（Berndt 反例） |
| Entry 18(iii) | 36 | Bernoulli 数递推 (18.6) |
| Entry 19 | 36 | Pfaff 变换；Vandermonde 定理 (19.1) 为其特例 |
| Entry 20 | 36–37 | (20.2) |
| Entry 21 | 37 | Kummer 第一变换 |
| Entry 22 | 38 | Pfaff 型 ${}_2F_1$ 变换 |
| Entry 23 | 38 | Kummer 第二变换变体；推论 1、2（完全椭圆积分） |
| Entry 24 | 38 | ${}_2F_1$ 的积分变换 |
| Entry 25 | 38–39 | ${}_2F_1$ 的积分变换 |
| Entry 26 | 39 | Euler 变换 |
| Entry 27 | 39 | Thomae 定理 |
| Entry 28 | 39 | Entry 27 取 $q = -1$ |
| Entry 29(a)–(d) | 39–40 | ${}_3F_2$ 恒等式；(b) (29.1) 见于致 Hardy 第一封信，Watson 1929 年首证；推论 1 (29.3)：$\pi/4\,{}_3F_2 = G$；推论 2 |
| Entry 30 | 41 | ${}_3F_2$ 对称恒等式 |
| Entry 31 | 41 | Whipple 变换特例；(31.1)：$1-5(1/2)^5+\cdots = 2/\Gamma^4(3/4)$ |
| Entry 32 | 41–42 | (32.1)；缺失前提 $x+y+z = 0$；(32.2) Bailey 推广 |
| Entry 33 | 42 | (32.2) 的推论（拉马努金给了 $x+y+z = 0$ 前提） |
| Entry 34 | 42 | Gauss ${}_2F_1$ 在 $1/2$ 的求值；推论 |
| Entry 35(i) | 42–45 | $\varphi(n)$ 定义 (35.1) 与渐近展开 |
| Entry 35(ii) | 45 | (35.10) |
| Entry 35(iii) | 45 | (35.11) |
| Entry 35(iv) | 45–47 | $\varphi(1/2) = 8G/\pi^2$，$\varphi(1/4) = 1/2$ |

## Entry 1——Dougall 定理

**陈述。**设 $x$、$y$、$z$、$u$、$-x-y-z-u-2n-1$ 中至少一个为正整数，则
$${}_7F_6\left[\begin{matrix}n, \frac12n+1, -x, -y, -z, -u, x+y+z+u+2n+1 \\ \frac12n, x+n+1, y+n+1, z+n+1, u+n+1, -x-y-z-u-n\end{matrix}\right]$$
$$= \frac{\Gamma(x+n+1)\Gamma(y+n+1)\Gamma(z+n+1)\Gamma(u+n+1)\Gamma(x+y+z+n+1)}{\Gamma(n+1)\Gamma(x+y+n+1)\Gamma(y+z+n+1)\Gamma(x+u+n+1)\Gamma(z+u+n+1)}$$
$$\times \frac{\Gamma(y+z+u+n+1)\Gamma(x+u+z+n+1)\Gamma(x+y+u+n+1)}{\Gamma(x+z+n+1)\Gamma(y+u+n+1)\Gamma(x+y+z+u+n+1)}. \tag{1.1}$$

**出处。**Part II，Ch. 10，Entry 1（p. 9）。Dougall 1907 年首证（拉马努金发现此定理约在其后不到三年）；Hardy 综述 Eq. (2.1) 详论，Bailey 书 p. 34 亦给 Dougall 证明。拉马努金未说明 $-x-y-z-u-2n-1$ 为正整数时 (1.1) 亦成立。

**状态。**已证明（Dougall 1907 年；见 Bailey）。

**对照。**M02（超几何级数主线：Dougall 定理）。

## Entry 2——Saalschütz 定理

**陈述。**若 $x$、$y$、$z$ 中至少一个为正整数，则
$${}_3F_2\left[\begin{matrix}-x, -y, -z \\ n+1, -x-y-z-n\end{matrix}\right] = \frac{\Gamma(n+1)\Gamma(x+y+n+1)\Gamma(y+z+n+1)\Gamma(z+x+n+1)}{\Gamma(x+n+1)\Gamma(y+n+1)\Gamma(z+n+1)\Gamma(x+y+z+n+1)}.$$

**出处。**Part II，Ch. 10，Entry 2（p. 9）。Saalschütz 定理；据 Jacobi 与 Askey 的考证，实为 Pfaff 1797 年首证。Hardy 综述 Eq. (5.1) 的表述有误。证明见 Bailey 书 p. 9。

**状态。**已证明（Pfaff 1797 年）。

**对照。**M02（Saalschütz 定理）。

## Entry 3——${}_6F_5$ 闭式

**陈述。**若 $x$、$y$、$z$、$-x-y-z-2n$ 中至少一个为正整数，则
$${}_6F_5\left[\begin{matrix}\frac12n+1, 1, -x, -y, -z, x+y+z+2n \\ \frac12n, x+n+1, y+n+1, z+n+1, -x-y-z-n+1\end{matrix}\right] = \frac{(x+n)(y+n)(z+n)(x+y+z+n)}{n(x+y+n)(y+z+n)(x+z+n)}.$$

**出处。**Part II，Ch. 10，Entry 3（pp. 9–10）。在 Entry 1 中取 $u = -1$ 即得。

**状态。**已证明（Entry 1 的特例）。

**对照。**M02。

## Entry 4——(1.1) 的对数微分

**陈述。**若 $x$、$y$、$z$、$-x-y-z-2n-1$ 中至少一个为正整数，则
$$\sum_{k=1}^{\infty} \frac{(n+2k)(-x)_k(-y)_k(-z)_k(x+y+z+2n+1)_k}{k(n+k)(x+n+1)_k(y+n+1)_k(z+n+1)_k(-x-y-z-n)_k}$$
$$= \psi(x+n+1)+\psi(y+n+1)+\psi(z+n+1)+\psi(x+y+z+n+1)$$
$$- \psi(n+1)-\psi(x+y+n+1)-\psi(y+z+n+1)-\psi(z+x+n+1).$$

**出处。**Part II，Ch. 10，Entry 4（pp. 10–11）。对 (1.1) 两端关于 $u$ 取对数微分再令 $u = 0$，用 (0.3)。例 (i)–(v)（pp. 10–11）：例 (i) 在 Entry 1 取 $n = 1$、$x \to x-1$、$y = z = u = x-1$；例 (ii) 在 Entry 4 取 $n = 0$、$x \to i(x-1)$、$y = z = 4(x-1)$；例 (iii) 在 Entry 3 取 $n = 1$、$x \to x-1$、$y = z = x-1$；例 (iv) 在 Entry 2 取 $n = 0$、$x = y = z$（笔记本 p. 118 把 $\Gamma(3x+1)$ 误放分子）；例 (v) 的确切形式待核对。

**状态。**已证明（Entry 1 的对数微分）。

**对照。**M02、M07（digamma 函数）。

## Entry 5——Dougall ${}_5F_4$

**陈述。**若 $\mathrm{Re}(x+y+z+n+1) > 0$，则
$${}_5F_4\left[\begin{matrix}\frac12n+1, n, -x, -y, -z \\ \frac12n, x+n+1, y+n+1, z+n+1\end{matrix}\right] = \frac{\Gamma(x+n+1)\Gamma(y+n+1)\Gamma(z+n+1)\Gamma(x+y+z+n+1)}{\Gamma(n+1)\Gamma(x+y+n+1)\Gamma(y+z+n+1)\Gamma(x+z+n+1)}. \tag{5.1}$$

**出处。**Part II，Ch. 10，Entry 5（pp. 11–12）。又 due to Dougall；Hardy 综述 (3.1)。另有连续类比（积分形式），$c = 0$、$d = 3$ 的特例见原文。

**状态。**已证明（Dougall）。

**对照。**M02。本章后续 Entry 7（Dixon）及诸推论多由此导出；部分和记号 ${}_{p+1}F_p[\cdots|m]$（上标 $m$ 表截断求和）见原文。

## Entry 6——${}_5F_4$ 部分和的渐近

**陈述。**若 $\alpha+\beta+\gamma+1 = n$，则当 $m \to \infty$ 时
$$\frac{\Gamma(n+2)\Gamma(\alpha+1)\Gamma(\beta+1)\Gamma(\gamma+1)}{\Gamma(n-\alpha+1)\Gamma(n-\beta+1)\Gamma(n-\gamma+1)}$$
$$\times {}_5F_4\left[\begin{matrix}\frac12(n+3), n+1, \alpha+1, \beta+1, \gamma+1 \\ \frac12(n+1), n-\alpha+1, n-\beta+1, n-\gamma+1\end{matrix} \middle| m\right]$$
$$\sim 2\mathrm{Log}\,m - \psi(\alpha+1) - \psi(\beta+1) - \psi(\gamma+1) - C,$$
其中 $C$ 为 Euler 常数。

**Second Version。**若 $a$、$b$、$c$、$a+b+c$ 均非非正整数，则当 $m \to \infty$ 时
$$\frac{\Gamma(a+b+c)\Gamma(a)\Gamma(b)\Gamma(c)}{\Gamma(b+c)\Gamma(a+c)\Gamma(a+b)} \cdot {}_5F_4\left[\begin{matrix}\frac12(a+b+c+1), a+b+c-1, a, b, c \\ \frac12(a+b+c-1), b+c, a+c, a+b\end{matrix} \middle| m\right]$$
$$= 2\mathrm{Log}\,m - \gamma - \psi(a) - \psi(b) - \psi(c) + O\left(\frac{\mathrm{Log}\,m}{m}\right).$$

**出处。**Part II，Ch. 10，Entry 6（pp. 12–14）。原证明由 J. L. Fields 供稿；R. J. Evans 后给出更简证明（即 Second Version），用 Whipple 变换
$${}_7F_6\left[\begin{matrix}a, 1+\frac12a, b, c, d, e, -m \\ \frac12a, 1+a-b, 1+a-c, 1+a-d, 1+a-e, 1+a+m\end{matrix}\right]$$
$$= \frac{(1+a)_m(1+a-d-e)_m}{(1+a-d)_m(1+a-e)_m} \cdot {}_4F_3\left[\begin{matrix}1+a-b-c, d, e, -m \\ 1+a-b, 1+a-c, d+e-a-m\end{matrix}\right], \tag{6.1}$$
$m$ 为非负整数（Bailey 书 p. 25）。

**推论。**$0 < x < 1$，当 $x \to 0$ 时
$$\frac{\pi^2}{4}{}_5F_4\left[\begin{matrix}\frac54, \frac12, \frac12, \frac12, \frac12 \\ \frac14, 1, 1, 1\end{matrix}; 1-x\right] \sim -\mathrm{Log}\,x + 3\mathrm{Log}\,2.$$
（取 $n = \alpha = \beta = \gamma = -1/2$，用 $\psi(1/2) = -2\mathrm{Log}\,2 - \gamma$。本推论已数值核对：$x = 0.01$ 时两端 $6.6984$ 与 $6.6846$，差随 $x \to 0$ 缩小。）

**状态。**已证明（Fields；Evans 简化证明）。

**对照。**M02、M12（渐近展开；Whipple 变换见 Entry 31）。

## Entry 7——Dixon 定理

**陈述。**若 $\mathrm{Re}(x+y+n+1) > 0$，则
$${}_3F_2\left[\begin{matrix}n, -x, -y \\ x+n+1, y+n+1\end{matrix}\right] = \frac{\Gamma(x+n+1)\Gamma(y+n+1)\Gamma(\frac12n+1)\Gamma(x+y+\frac12n+1)}{\Gamma(n+1)\Gamma(x+y+n+1)\Gamma(x+\frac12n+1)\Gamma(y+\frac12n+1)}.$$

**出处。**Part II，Ch. 10，Entry 7（pp. 15–19）。Dixon 定理；在 Entry 5 中取 $z = -3n$ 即得。Hardy 综述 (3.2)。终止情形可用于二维 Selberg 积分的求值（Andrews）；Dyson–Gunson–Wilson 恒等式的 $n = 3$ 情形亦可由此建立。Gessel 与 Stanton 给出 Saalschütz 定理与 Dixon 定理的新短证明。

**状态。**已证明（Dixon）。

**对照。**M02（Dixon 定理）。

**推论 1。**若 $\mathrm{Re}(x+y+n+1) > 0$，则
$$\sum_{k=1}^{\infty}\left(\frac{1}{k}+\frac{1}{n+k}\right)\frac{(-x)_k(-y)_k}{(x+n+1)_k(y+n+1)_k} = \psi(x+n+1)+\psi(y+n+1)-\psi(n+1)-\psi(x+y+n+1). \tag{7.1}$$
（对 (5.1) 关于 $z$ 取对数微分再令 $z = 0$。）

**推论 2。**若 $\mathrm{Re}(x+y+1) > 0$，则 ${}_5F_4[\frac12n+1, n, n, -x, -y; \frac12n, x+n+1, y+n+1, 1] = \Gamma(x+n+1)\Gamma(y+n+1)\Gamma(x+y+1)/(\Gamma(n+1)\Gamma(x+y+n+1)\Gamma(x+1)\Gamma(y+1))$。（在 Entry 5 中取 $z = -n$。确切形式待核对。）

**推论 3。**若 $\mathrm{Re}(x+y+n) > 0$，则 ${}_4F_3[\frac12n+1, -x, -y, 1; \frac12n, x+n+1, y+n+1] = (x+n)(y+n)/(n(x+y+n))$。（在 Entry 5 中取 $z = -1$。）

**推论 4。**若 $\mathrm{Re}(x+y+\frac12(n+1)) > 0$，则
$${}_4F_3\left[\begin{matrix}\frac12n+1, n, -x, -y \\ \frac12n, x+n+1, y+n+1\end{matrix}\right] = \frac{\Gamma(x+n+1)\Gamma(y+n+1)\Gamma(\frac12(n+1))\Gamma(x+y+\frac12(n+1))}{\Gamma(n+1)\Gamma(x+y+n+1)\Gamma(x+\frac12(n+1))\Gamma(y+\frac12(n+1))}.$$
（在 Entry 5 中取 $z = -\frac12(n+1)$。）

**推论 5。**若 $\mathrm{Re}(2x+2y+n+2) > 0$，则
$${}_4F_3\left[\begin{matrix}\frac12n+1, n, -x, -y \\ \frac12n, x+n+1, y+n+1\end{matrix}; -1\right] = \frac{\Gamma(x+n+1)\Gamma(y+n+1)}{\Gamma(n+1)\Gamma(x+y+n+1)}. \tag{7.2}$$
（在 Entry 5 中令 $z \to \infty$；Bailey 书 p. 28 另有基于 Whipple 变换 (6.1) 的证明。）

**推论 6。**若 $\mathrm{Re}(x+n+1) > 0$，则
$$\sum_{k=1}^{\infty}\left(\frac{1}{k}+\frac{1}{n+k}\right)\frac{(-x)_k(k-1)!}{(x+n+1)_k(n+1)_k} = \sum_{k=1}^{\infty}\frac{1}{(k+x+n)^2} - \sum_{k=1}^{\infty}\frac{1}{(k+n)^2}. \tag{7.3}$$
（对 (7.1) 关于 $y$ 求导再令 $y = 0$，用 (0.2)(0.3)。拉马努金在笔记本 p. 119 左端写 $k!$ 应为 $(k-1)!$。）

**推论 7。**若 $\mathrm{Re}(x-n+1) > 0$，则
$${}_5F_4\left[\begin{matrix}\frac12n+1, n, n, n, -x \\ \frac12n, x+n+1, 1, 1\end{matrix}\right] = \frac{\sin(\pi n)\Gamma(x+n+1)\Gamma(x-n+1)}{\pi n\Gamma^2(x+1)}. \tag{7.4}$$
（在 Entry 5 中取 $y = z = -n$。）

**推论 8–11。**（确切形式待核对。）推论 8 在 Entry 7 取 $y = -n$；推论 9、10、11 由推论 4、5、7 派生。

**推论 12。**Gauss 定理的特例（由 Entry 7 取 $y = -n$ 并化简；实为 Entry 8 的特例）。

**推论 13。**Kummer 定理：${}_2F_1$ 在 $-1$ 处的求值（在 Entry 7 中令 $y \to \infty$）。

**推论 14。**若 $\mathrm{Re}\,x > -\frac12$，则
$${}_3F_2\left[\begin{matrix}\frac12n+1, n, -x \\ \frac12n, x+n+1\end{matrix}; -1\right] = \frac{\Gamma(x+n+1)\Gamma(\frac12n+\frac12)}{\Gamma(n+1)\Gamma(x+\frac12n+\frac12)}.$$
（在推论 5 中取 $y = -\frac12(n+1)$。）

**推论 15。**若 $\mathrm{Re}\,n < \frac12$，则
$${}_5F_4\left[\begin{matrix}\frac12n+1, n, n, n, n \\ \frac12n, 1, 1, 1\end{matrix}\right] = \frac{\Gamma^2(n)\sin(\pi n)\tan(\pi n)}{\pi^2\Gamma(2n+1)}.$$
（在 Entry 5 取 $x = y = z = -n$，用反射公式化简。Hardy 综述 Eq. (3.33)。）

**推论 16。**若 $\mathrm{Re}\,n < \frac13$，则
$${}_4F_3\left[\begin{matrix}\frac12n+1, n, n, n \\ \frac12n, 1, 1\end{matrix}\right] = \frac{\sin(\pi n)\Gamma(\frac12n+\frac12)\Gamma(\frac12-\frac32n)}{\pi n\Gamma^2(\frac12-\frac12n)}.$$
（在推论 4 取 $x = y = -n$。Hardy 综述 (3.31)；Bailey 书 p. 96。）

**推论 17。**若 $\mathrm{Re}\,n < \frac23$，则
$${}_4F_3\left[\begin{matrix}\frac12n+1, n, n, n \\ \frac12n, 1, 1\end{matrix}; -1\right] = \frac{\sin(\pi n)}{\pi n}.$$
（在推论 5 取 $x = y = -n$。Hardy 综述 Eq. (3.32)；Bailey 书 p. 96。）

**推论 18。**若 $\mathrm{Re}\,n < 1$，则
$${}_3F_2\left[\begin{matrix}\frac12n, n, n \\ \frac12n+1, 1\end{matrix}\right] = \frac{2\tan(\frac12\pi n)\Gamma^4(\frac12n+1)}{\pi n\Gamma^2(n+1)}.$$
（在推论 11 取 $x = -n$，用反射公式化简。）

**推论 19。**若 $\mathrm{Re}\,n < 2$，则
$${}_3F_2\left[\begin{matrix}\frac12n, \frac12n, n \\ \frac12n+1, \frac12n+1\end{matrix}\right] = \frac{\pi n\Gamma^2(\frac12n+1)}{2\sin(\frac12\pi n)\Gamma(n+1)}.$$
（在推论 11 取 $x = -\frac12n$。）

**推论 20。**若 $\mathrm{Re}(2x+n+2) > 0$，则为对 (7.2) 关于 $x$（或 $y$）取对数微分所得的 $\psi$ 和。（确切形式待核对。）

**推论 21。**若 $\mathrm{Re}\,x > -1$，则为一 $\psi$ 和，其中含 $\sum 1/(k+x+n)$ 型求和；拉马努金在笔记本 p. 120 漏记 $-1/k$ 求和项。（确切形式待核对。）

**推论 22。**若 $\mathrm{Re}\,n > 0$，则为一 ${}_3F_2$ 求值。（确切形式待核对。）

**推论 23。**若 $\mathrm{Re}\,n > -2$，则在推论 6 取 $x = -\frac12n$ 化简所得。（确切形式待核对。）

**推论 24。**若 $\mathrm{Re}\,n < 1$，则对 (7.4) 关于 $x$ 求导所得。（确切形式待核对。）

**例 1–20**（pp. 20–25）：多为在 Dixon 定理及诸推论中取 $n = 1$、$x \to x-1$、$y = x-1$ 等特例所得的二项系数级数求值。已核对的几例如下；其余例的确切形式待核对。
- **例 14。**$1 - 5(\frac12)^3 + 9(\frac{1\cdot3}{2\cdot4})^3 - \cdots = 2/\pi$，即
  $$\sum_{k=0}^{\infty}(-1)^k(4k+1)\left(\frac{(\frac12)_k}{k!}\right)^3 = \frac{2}{\pi}.$$
  证明：在推论 5 取 $n = -x = -y = 1/2$，得 ${}_4F_3[\frac54, \frac12, \frac12, \frac12; \frac14, 1, 1; -1] = 1/(\Gamma(\frac32)\Gamma(\frac12)) = 2/\pi$。此例见于拉马努金致 Hardy 第一封信（p. xxvi）；Bauer 1859 年首证；Hardy 与 Bailey 均载。**注意**：本例级数的系数是 $4k+1$（不是 $2k+1$）；150 DPI 初读曾误读证明中的 $\Gamma(\frac32)$ 为 $\Gamma(\frac34)$，300 DPI 放大图确认无误。
- **例 15。**见于致 Hardy 第一封信（p. xxv）。（确切形式待核对。）
- **例 16–19。**含 $\Gamma(\frac34)$ 的求值；例 18 为 $1 + (\frac12)^3 + (\frac{1\cdot3}{2\cdot4})^3 + \cdots = \pi/\Gamma^4(\frac34)$（Entry 31 (31.1) 的证明所引）。
- **例 20。**若 $\mathrm{Re}\,n < \frac23$，则
  $$1 + \left(\frac{n}{1!}\right)^3 + \left(\frac{n(n+1)}{2!}\right)^3 + \cdots = \frac{6\sin(\frac12\pi n)\sin(\pi n)\Gamma^3(\frac12n+1)}{\pi^2n^2(1+2\cos(\pi n))\Gamma(\frac32n+1)}.$$
  Morley 1902 年首证；Bailey 书 p. 13。

## Entry 8——Gauss 定理

**陈述。**若 $\mathrm{Re}(x+y+n+1) > 0$，则
$${}_2F_1(-x, -y; n+1) = \frac{\Gamma(n+1)\Gamma(x+y+n+1)}{\Gamma(x+n+1)\Gamma(y+n+1)}. \tag{8.1}$$

**出处。**Part II，Ch. 10，Entry 8（p. 25）。Gauss 定理。拉马努金在 Entry 8 之后用一句话指出他的推导：设 $n$、$x$ 为整数，$n \ge 0$、$n+x \ge 0$，将 $(1+u)^{y+n}$ 与 $(1+1/u)^x$ 展成形式二项级数相乘，取 $u^n$ 的系数 $a_n$，得
$$a_n = \sum_{k=0}^{\infty}\binom{y+n}{k+n}\binom{x}{k} = \frac{\Gamma(y+n+1)}{\Gamma(n+1)\Gamma(y+1)}\sum_{k=0}^{\infty}\frac{(-x)_k(-y)_k}{(n+1)_k k!}, \tag{8.2}$$
另一方面将 $(1+u)^{x+y+n}$ 展开并除以 $u^x$，得
$$a_n = \binom{x+y+n}{x+n} = \frac{\Gamma(x+y+n+1)}{\Gamma(x+n+1)\Gamma(y+1)}. \tag{8.3}$$
比较 (8.2)(8.3) 即得 (8.1)。这是第二本笔记中唯一的证明草图。

**状态。**已证明（Gauss；拉马努金草图如上）。

**对照。**M02（Gauss 定理；本章的基石，后续多条由此导出）。

## Entry 9——$\psi$ 差

**陈述。**若 $\mathrm{Re}(\alpha-\beta) > 0$，则
$$\sum_{k=1}^{\infty}\frac{(\beta)_k}{k(\alpha)_k} = \psi(\alpha) - \psi(\alpha-\beta). \tag{9.1}$$

**出处。**Part II，Ch. 10，Entry 9（p. 25）。在 Gauss 定理 Entry 8 取 $\beta = -x$、$\alpha = n+1$，对 (8.1) 关于 $y$ 取对数微分再令 $y = 0$，用 (0.3)。

**状态。**已证明（Entry 8 的对数微分）。

**对照。**M02、M07。

## Entry 10——(10.1)

**陈述。**若 $\mathrm{Re}\,x > -1$，则
$$\sum_{k=0}^{\infty}\frac{(-x)_k}{(n+k)k!} = \frac{\Gamma(n)\Gamma(x+1)}{\Gamma(n+x+1)}. \tag{10.1}$$

**出处。**Part II，Ch. 10，Entry 10（pp. 25–27）。在 Gauss 定理 Entry 8 令 $y = -n$ 即得。例 1–7（pp. 26–27）：例 1 由 (9.1) 关于 $\beta$ 求导、$\beta = 0$、$\alpha = n+1$；例 2 在 Entry 10 取 $x = -n$；例 3 $n$ 任意；例 4–7 的确切形式待核对。

**状态。**已证明（Entry 8 的特例）。

**对照。**M02、M07。

## Entry 11——望远镜和

**陈述。**设 $n > 0$，$\mathrm{Re}(\alpha-\beta-1) > 0$，则
$$\sum_{k=0}^{\infty}\{(\alpha+k)^n - (\beta+1+k)^n\}\left\{\frac{(\beta+1)_k}{(\alpha+1)_k}\right\}^n = \alpha^n.$$

**出处。**Part II，Ch. 10，Entry 11（pp. 27–28）。证明：部分和望远镜化为 $\alpha^n - \{(\beta+1)_{m+1}/(\alpha+1)_m\}^n$，由 Stirling 公式余项趋于 0。

**推论 1。**若 $\mathrm{Re}(\alpha-\beta-1) > 0$，则 $\sum_{k=1}^{\infty}(\beta)_k/(\alpha)_k = \beta/(\alpha-\beta-1)$。（取 $n = 1$；亦可由 Entry 8 取 $n+1 = \alpha$、$x = -1$、$y = -\beta$ 得。）

**推论 2。**若 $\mathrm{Re}(\alpha-\beta-1) > 0$，则 $\sum_{k=1}^{\infty}(\alpha+\beta+2k-1)(\beta)_k^2/(\alpha)_k^2 = \beta^2/(\alpha-\beta-1)$。（取 $n = 2$；$(\alpha+k)^2-(\beta+1+k)^2 = (\alpha-\beta-1)(\alpha+\beta+2k+1)$。）

**状态。**已证明。

**对照。**M02、M12。

## Entry 12(a)——指数公式递推

**陈述。**设 $f(x) = \sum_{k=1}^{\infty}(A_kx^k/k)$ 在原点某邻域内成立。定义 $P_k$（$0 \le k < \infty$）为
$$e^{f(x)} = \sum_{k=0}^{\infty}P_kx^k. \tag{12.1}$$
则 $P_0 = 1$，且 $n \ge 1$ 时
$$nP_n = \sum_{k=1}^{n}A_kP_{n-k}.$$

**出处。**Part II，Ch. 10，Entry 12(a)（p. 28）。对 (12.1) 求导并比较 $x^{n-1}$ 的系数即得。

**状态。**已证明。

**对照。**M02（形式幂级数；与 Ch. 3 的 Bell 多项式理论互见）。

## Entry 12(b)——Newton 恒等式

**陈述。**设 $n$、$r$ 为正整数，定义幂和 $S_r = S_r(n) = \sum_{k=1}^{n}a_k^r$ 与初等对称和 $\mathcal{P}_r = \mathcal{P}_r(n) = \sum_{1 \le k_1 < \cdots < k_r \le n}a_{k_1}\cdots a_{k_r}$（$r \le n$），其中 $a_1, \ldots, a_n$ 为任意非零复数。则 $r \ge 1$ 时
$$r\mathcal{P}_r = \sum_{k=1}^{r}(-1)^{k+1}S_k\mathcal{P}_{r-k}, \tag{12.2}$$
其中 $\mathcal{P}_0 = 1$。

**出处。**Part II，Ch. 10，Entry 12(b)（pp. 28–29）。由 Entry 12(a) 取 $A_j = (-1)^{j+1}S_j$ 推出（此时 $P_r = \mathcal{P}_r$）。据 MacMahon 的说法，此恒等式出自 Newton；Berndt 注 Entry 12(b) 是容斥原理的一个实例。

**状态。**已证明（Newton；经 Entry 12(a)）。

**对照。**M02（与 Ch. 3 Entry 11 的 Newton 恒等式互见）。

## Entry 13——(13.5)

**准备。**对正整数 $r$ 定义
$$S_r = S_r(n, x) = \sum_{k=0}^{\infty}\left(\frac{1}{(k+n)^r} - \frac{1}{(k+n+x+1)^r}\right). \tag{13.1}$$
令 $\varphi(0) = 1$，$\varphi(n, x, r) = \varphi(r)$（$r \ge 1$）由下式递推定义：
$$r\varphi(r) = \sum_{k=1}^{r}S_k\varphi(r-k). \tag{13.2}$$
**引理。**$r$ 为正整数时，$\frac{d}{dn}\varphi(r) = -\sum_{k=1}^{r}S_{k+1}\varphi(r-k)$。(13.3)

**陈述。**若 $\mathrm{Re}\,x > -1$，$r$ 为任意正整数，则
$$\sum_{k=0}^{\infty}\frac{(-x)_k}{(n+k)^{r+1}k!} = \frac{\Gamma(n)\Gamma(x+1)}{\Gamma(n+x+1)}\varphi(r). \tag{13.5}$$

**出处。**Part II，Ch. 10，Entry 13（pp. 30–32）。$r = 1$ 时由第 10 节例 5；归纳步对 (13.5) 关于 $n$ 求导并用引理 (13.3)。

**推论 1。**设 $S_r(n, x)$、$\varphi(n, x, r)$ 如 (13.1)(13.2) 所定义。若 $n = \frac12$、$x = -\frac12$，则 $S_1 = 2\mathrm{Log}\,2$，$S_r = (2^r-2)\zeta(r)$（$r \ge 2$），且
$$1 + \frac{1}{3^{r+1}}\left(\frac12\right) + \frac{1}{5^{r+1}}\left(\frac{1\cdot3}{2\cdot4}\right) + \cdots = \frac{\pi}{2^{r+1}}\varphi(r), \qquad r \ge 1. \tag{13.6}$$
（拉马努金在笔记本 p. 124 为推论 1 重定义 $S_r$。）

**推论 2。**（p. 31；确切形式待核对。）

**例 1。**$1 + \frac{1}{3^3}(\frac12) + \frac{1}{5^3}(\frac{1\cdot3}{2\cdot4}) + \cdots = \frac{\pi}{4}\mathrm{Log}^2 2 + \frac{\pi^3}{48}$，即 $\sum_{k=0}^{\infty}((\frac12)_k/k!)/(2k+1)^3 = \frac{\pi}{4}\mathrm{Log}^2 2 + \frac{\pi^3}{48}$。（(13.6) 取 $r = 2$；$\varphi(2) = 2\mathrm{Log}^2 2 + \pi^2/6$。**注意**：本例级数的因子 $((\frac12)_k/k!)$ 是一次方，不是平方；初版数值复核曾误写平方，纠正后通过。）

**例 2。**$\int_0^{\pi/2}\theta\cot\theta\,\mathrm{Log}(\sin\theta)\,d\theta = -\frac{\pi}{4}\mathrm{Log}^2 2 - \frac{\pi^3}{48}$。（用 $\frac12\int_0^1 u^k\mathrm{Log}^2 u\,du = 1/(k+1)^3$ 与 $(1-u^2)^{-1/2}$ 的展开逐项积分。）

**状态。**已证明（归纳法）。

**对照。**M02、M07（$\varphi(r)$ 与 $\zeta(r)$；$r = 2$ 的例 1 与 Ch. 9 的多对数主题互见）。

## Entry 14——双重和恒等式

**准备。**定义 $C_{m,n}(x) = \sum_{k=0}^{\infty}\frac{1}{(k+x)^m}\sum_{j=0}^{k-1}\frac{1}{(j+x)^n}$ 与 $S_m(x) = \sum_{k=0}^{\infty}1/(k+x)^m$，其中 $m$、$n$ 为正整数，$m \ge 2$。

**陈述。**设 $n$ 为整数，$n \ge 2$，则
$$2\sum_{k=1}^{\infty}\frac{1}{(k+x)^n}\sum_{j=1}^{k}\frac{1}{j} = nS_{n+1}(x) - \sum_{r=1}^{n-2}S_{r+1}(x)S_{n-r}(x)$$
$$- 2\sum_{k=1}^{\infty}\frac{1}{(k+x)^n}\sum_{j=0}^{k}\frac{1}{j+x} + 2\sum_{k=1}^{\infty}\sum_{j=0}^{k-1}\frac{1}{(j+x)^n}\left(\frac{1}{k-j} - \frac{1}{k+x}\right).$$
另有等价形式 (14.1)：$\sum_{k=1}^{\infty}\frac{1}{(k+x)^n}\sum_{j=1}^{k}\frac{1}{j} = -\sum_{r=1}^{n-2}C_{n-r,r+1} - C_{n,1}(x) + \sum_{k=1}^{\infty}\sum_{j=0}^{k-1}\frac{1}{(j+x)^n}(\frac{1}{k-j}-\frac{1}{k+x})$；且 $S_m(x)S_n(x) = S_{m+n}(x) + C_{m,n}(x) + C_{n,m}(x)$（$m, n \ge 2$）。

**出处。**Part II，Ch. 10，Entry 14（pp. 32–33）。证明用 Nielsen 书 p. 48 的分解 $1/((k+x)^n(k-j)) = -\sum_{r=0}^{n-1}1/((k+x)^{n-r}(j+x)^{r+1}) + 1/((j+x)^n(k-j))$。Berndt 注：拉马努金在笔记本 p. 124 的表述「somewhat imprecise」。同类结果见 Ch. 9 与 Part I 的有关引文。

**状态。**已证明（Nielsen 分解）。

**对照。**M02、M07（多重 zeta 型和）。

## Entry 15——部分和渐近

**陈述。**若 $\alpha$、$\beta$ 为任意复数，则当 $n \to \infty$ 时
$$\sum_{k=0}^{n-1}\frac{\Gamma(\alpha+k+1)\Gamma(\beta+k+1)}{\Gamma(\alpha+\beta+k+2)k!} \sim \mathrm{Log}\,n - \psi(\alpha+1) - \psi(\beta+1) - \gamma.$$

**出处。**Part II，Ch. 10，Entry 15（pp. 33–34）。由 Luke 书 p. 110 Eq. (35)：$\Gamma(a)\Gamma(b)/\Gamma(a+b)\cdot\sum_{k=0}^{n-1}(a)_k(b)_k/((a+b)_k k!) \sim \mathrm{Log}\,n - \psi(a) - \psi(b) - \gamma$，取 $a = \alpha+1$、$b = \beta+1$。弱化形式 $\sum \sim \mathrm{Log}\,n$ 归于 Hill；Gauss 曾证 $\lim_{x\to1^-} {}_2F_1(a,b;a+b;x)/\mathrm{Log}\{1/(1-x)\} = \Gamma(a+b)/(\Gamma(a)\Gamma(b))$。

**推论。**$0 < x < 1$，当 $x \to 0$ 时
$$\pi\,{}_2F_1\left(\frac12, \frac12; 1; 1-x\right) \sim -\mathrm{Log}\,x + 4\mathrm{Log}\,2.$$
（原文印为 $\mathrm{Log}\,x + 4\mathrm{Log}\,2$，符号有误，见末尾小结。）证明用 Luke 书 p. 87 Eq. (11)：
$${}_2F_1(a, b; a+b; 1-x) \sim -\frac{\Gamma(a+b)}{\Gamma(a)\Gamma(b)}(\mathrm{Log}\,x + \psi(a) + \psi(b) + 2\gamma), \tag{15.1}$$
取 $a = b = \frac12$，用 $\psi(\frac12) = -\gamma - 2\mathrm{Log}\,2$。

**状态。**已证明（Luke）。

**对照。**M02、M12（渐近展开；与 Entry 6 推论的对数奇性同类）。

## Entry 16——二项反演

**陈述。**若 $A_0, A_1, \ldots, A_r$ 为任意复数，且
$$P_r = \sum_{k=0}^{r}A_k(-1)^k\binom{r}{k}, \qquad r \ge 0,$$
则
$$A_r = \sum_{k=0}^{r}P_k(-1)^k\binom{r}{k}, \qquad r \ge 0.$$

**出处。**Part II，Ch. 10，Entry 16（p. 34）。熟知的反演公式；证明见 Riordan 书 pp. 43–44。

**状态。**已证明。

**对照。**M02（与 Ch. 3 的反演理论互见）。

## Entry 17——移位公式

**陈述。**设
$$f(x) = f(r, x) = \sum_{k=0}^{\infty}\frac{(r)_kA_k}{k!x^{r+k}} \tag{17.1}$$
在 $|x| > R$ 解析。对 $|x| > \sup(R, |h|)$，写
$$f(x) = \sum_{k=0}^{\infty}\frac{(r)_kB_k}{k!(x+h)^{r+k}}. \tag{17.2}$$
则
$$B_k = \sum_{j=0}^{k}A_jh^{k-j}\binom{k}{j}, \qquad k \ge 0.$$

**出处。**Part II，Ch. 10，Entry 17（pp. 34–35）。将 (17.2) 在 $|x| > R, |h|$ 展开并比较 $x^{-r-n}$ 的系数即得（用 (17.3)）。

**状态。**已证明。

**对照。**M02（Entry 18–20 的工具）。

## Entry 18(i)——$e^x$ 乘幂级数

**陈述。**设 (17.1) 成立，又设
$$f(x) = \sum_{k=0}^{\infty}\frac{(-1)^k(r)_kA_k}{k!(x-1)^{r+k}} \tag{18.1}$$
在 $|x| > \sup(R, 1)$ 成立。再设 $\sum_{k=0}^{\infty}(A_kx^k/k!)$ 在 $|x| < R^*$ 解析，则对 $|x| < R^*$，
$$e^x\sum_{k=0}^{\infty}\frac{A_k(-x)^k}{k!} = \sum_{k=0}^{\infty}\frac{A_kx^k}{k!}. \tag{18.2}$$

**出处。**Part II，Ch. 10，Entry 18(i)（p. 35）。在 Entry 17 取 $h = -1$，比较 (17.2) 与 (18.1) 得 $A_k = \sum_{j=0}^{k}A_j(-1)^j\binom{k}{j}$ (18.3)；另一方面 Cauchy 乘积给出 $e^x\sum A_j(-x)^j/j! = \sum C_kx^k/k!$，其中 $C_k = \sum_{j=0}^{k}(-1)^jA_j\binom{k}{j}$ (18.5)，故 $A_k = C_k$。

**状态。**已证明。

**对照。**M02。

## Entry 18(ii)——拉马努金断言为假

**陈述。**拉马努金断言：若 (17.1) 与 (18.1) 成立，则
$$\frac{1}{\varphi^r(x)}\sum_{k=0}^{\infty}\frac{(r)_kA_k}{k!}\left\{\frac{\varphi(x)-\varphi(-x)}{\varphi(x)}\right\}^k$$
恒为 $x$ 的偶函数。此断言**为假**。

**出处。**Part II，Ch. 10，Entry 18(ii)（pp. 35–36）。Berndt 的反例：取 $\varphi(x) := x$、$r = 1$，则表达式形式上化为 $(1/x)\sum A_k2^k$，是 $x$ 的奇函数，不可能恒为偶函数。收敛性细节原文未展开，此处如实转述 Berndt 的说法，不作完整数值验证。

**状态。**已否定（Berndt 反例）。

**对照。**M02。

## Entry 18(iii)——Bernoulli 数递推

**陈述。**设 (17.1) 与 (18.1) 成立，则 $n$ 为偶整数、$n \ge 2$ 时
$$\frac12nA_{n-1} = \sum_{k=1}^{n/2}\binom{n}{2k}(2^{2k}-1)B_{2k}A_{n-2k}, \tag{18.6}$$
其中 $B_j$ 为第 $j$ 个 Bernoulli 数。

**出处。**Part II，Ch. 10，Entry 18(iii)（p. 36）。由生成函数 $x/(e^x-1) = \sum B_nx^n/n!$（$|x| < 2\pi$）得 $x/(e^x+1) = \sum B_k(1-2^k)x^k/k!$ (18.7)，再用 (18.2) 表示 $e^x$ 并比较 $x^n$（$n$ 偶）的系数。

**状态。**已证明。

**对照。**M01（Bernoulli 数；注意 M01 目前缺少 Bernoulli 数的定义，见 Ch. 5 Entry 9 导言 (I1)，不在本章顺手改）、M02。

## Entry 19——Pfaff 变换

**陈述。**设 $|x|$、$|x-1| > 1$，则
$$x^{-r}{}_2F_1(r, m; n; 1/x) = (x-1)^{-r}{}_2F_1(r, n-m; n; -1/(x-1)).$$

**出处。**Part II，Ch. 10，Entry 19（p. 36）。此变换广为人知（Bailey 书 p. 10），一般归于 Gauss 或 Kummer；据 Askey 的考证，实为 Pfaff 首创。证明：在 Entry 17 取 $A_k = (m)_k/(n)_k$、$h = 1$，归结为 Vandermonde 定理
$$\frac{(n-m)_k}{(n)_k} = \sum_{j=0}^{k}(-1)^j\frac{(m)_j}{(n)_j}\binom{k}{j}, \qquad k \ge 0, \tag{19.1}$$
而 (19.1) 是 Gauss 定理 Entry 8 的特例。

**状态。**已证明（Pfaff；经 Entry 17 与 Vandermonde 定理）。

**对照。**M02（Pfaff 变换）。

## Entry 20——(20.2)

**陈述。**设 $\varphi(x) = \sum_{r=0}^{\infty}\varphi^{(r)}(1)/r!\cdot(x-1)^r$ (20.1) 在 $|x-1| < R$（$R > 1$）解析，$m$、$n$ 为复参数使下述双重求和可交换次序，则
$$\sum_{k=0}^{\infty}\frac{(m)_k\varphi^{(k)}(0)}{(n)_k k!} = \sum_{k=0}^{\infty}\frac{(-1)^k(n-m)_k\varphi^{(k)}(1)}{(n)_k k!}. \tag{20.2}$$

**出处。**Part II，Ch. 10，Entry 20（pp. 36–37）。用 (20.1) 计算 $\varphi^{(k)}(0)$ 并交换求和次序，再用 Vandermonde 定理 (19.1)。注：若 $\varphi(x) = (x-1)^r$（$r$ 为非负整数），则 (20.2) 化为 $\sum_{k=0}^{r}(m)_k(-r)_k/((n)_k k!) = (n-m)_r/(n)_r$，即 Vandermonde 定理。

**状态。**已证明（经 Entry 19 与 Vandermonde 定理）。

**对照。**M02。

## Entry 21——Kummer 第一变换

**陈述。**对任意复数 $m$、$n$、$x$，
$$e^x\sum_{k=0}^{\infty}\frac{(-1)^k(n-m)_kx^k}{(n)_kk!} = \sum_{r=0}^{\infty}\frac{(m)_rx^r}{(n)_rr!},$$
即 $e^x\cdot{}_2F_1(n-m, 1; n; -x) = {}_2F_1(m, 1; n; x)$。

**出处。**Part II，Ch. 10，Entry 21（p. 37）。Kummer 首证；亦可由 Entry 19 取 $x \to r/x$ 再令 $r \to \infty$ 得。证明：将 $e^x$ 展开并比较 $x^r$ 的系数，用 Vandermonde 定理 (19.1)。

**状态。**已证明（Kummer）。

**对照。**M02（Kummer 变换）。

## Entry 22——Pfaff 型 ${}_2F_1$ 变换

**陈述。**设 $|x|$、$|x+1| > 1$，则
$$(x+1)^{-r}{}_2F_1(r, m; 2m; 1/(x+1)) = x^{-r}{}_2F_1(r, m; 2m; -1/x).$$

**出处。**Part II，Ch. 10，Entry 22（p. 38）。在 Entry 19 取 $n = 2m$、$x \to x+1$ 即得。

**状态。**已证明（Entry 19 的特例）。

**对照。**M02。

## Entry 23——Kummer 第二变换变体

**陈述。**设 $m$、$x$ 为任意复数，则
$$e^x\sum_{k=0}^{\infty}\frac{(-1)^k(m)_kx^k}{(2m)_kk!} = \sum_{r=0}^{\infty}\frac{(m)_rx^r}{(2m)_rr!},$$
即 $e^x\cdot{}_2F_1(m, 1; 2m; -x) = {}_2F_1(m, 1; 2m; x)$。

**出处。**Part II，Ch. 10，Entry 23（p. 38）。在 Entry 21 取 $n = 2m$ 即得。

**推论 1。**$x$ 为任意复数时，$e^x(1 - (\frac12)\frac{x}{1!} + (\frac{1\cdot3}{2\cdot4})\frac{x^2}{2!} - \cdots) = 1 + (\frac12)\frac{x}{1!} + (\frac{1\cdot3}{2\cdot4})\frac{x^2}{2!} + \cdots$。（取 $m = \frac12$。）

**推论 2。**若 $|x| < 1$、$\mathrm{Re}\,x < \frac12$，则 ${}_2F_1(\frac12, \frac12; 1; \frac{-x}{1-x}) = \sqrt{1-x}\,{}_2F_1(\frac12, \frac12; 1; x)$。（在 Entry 22 取 $r = m = \frac12$、$x \to -1/x$。）函数 ${}_2F_1(\frac12, \frac12; 1; x)$ 是第一类完全椭圆积分的常数倍，是椭圆函数理论的核心；见 Part III。

**状态。**已证明（Entry 21 的特例）。

**对照。**M02、M07（椭圆积分；与 Part III 第 17–18 章互见）。

## Entry 24——${}_2F_1$ 的积分变换

**陈述。**设 $|x|$、$|x-1| > 1$，$m$ 任意，$\mathrm{Re}\,n > 0$，则
$$\sum_{k=0}^{\infty}\frac{(m)_k}{(n+k)k!x^{n+k}} = \sum_{k=0}^{\infty}\frac{(-1)^k(n+1-m)_k}{(n+k)k!(x-1)^{n+k}}.$$

**出处。**Part II，Ch. 10，Entry 24（p. 38）。在 Entry 19 取 $n \to n+1$、$r = n+1$，再在 $[x, \infty)$ 上积分即得。

**状态。**已证明（Entry 19 的积分形式）。

**对照。**M02。

## Entry 25——${}_2F_1$ 的积分变换

**陈述。**设 $|x|$、$|x-1| > 1$，$n$ 任意，则
$$\sum_{k=0}^{\infty}\frac{k!}{(n)_{k+1}x^{k+1}} = \sum_{k=0}^{\infty}\frac{(-1)^k}{(n+k)(x-1)^{k+1}}.$$

**出处。**Part II，Ch. 10，Entry 25（p. 38）。在 Entry 19 取 $r = m = 1$、$n \to n+1$，两端乘 $1/n$ 即得。

**状态。**已证明（Entry 19 的特例）。

**对照。**M02。

## Entry 26——Euler 变换

**陈述。**若 $|x| < 1$，$\alpha$、$\beta$、$\gamma$ 任意，则
$$(1-x)^{\alpha+\beta}{}_2F_1(\alpha, \beta; \gamma; x) = (1-x)^{\gamma}{}_2F_1(\gamma-\alpha, \gamma-\beta; \gamma; x).$$

**出处。**Part II，Ch. 10，Entry 26（p. 39）。初等且熟知；见 Bailey 书 p. 2。

**状态。**已证明（Euler）。

**对照。**M02（Euler 变换；Entry 27 Thomae 定理可由此导出）。

## Entry 27——Thomae 定理

**陈述。**若 $\mathrm{Re}(n+1) > -\mathrm{Re}(x+y)$、$-\mathrm{Re}(p+q)$，则
$$\frac{\Gamma(x+y+n+1)}{\Gamma(x+n+1)\Gamma(y+n+1)}{}_3F_2\left[\begin{matrix}-p, -q, x+y+n+1 \\ x+n+1, y+n+1\end{matrix}\right]$$
$$= \frac{\Gamma(p+q+n+1)}{\Gamma(p+n+1)\Gamma(q+n+1)}{}_3F_2\left[\begin{matrix}-x, -y, p+q+n+1 \\ p+n+1, q+n+1\end{matrix}\right].$$

**出处。**Part II，Ch. 10，Entry 27（p. 39）。Thomae 定理；可由 Entry 26 导出。Hardy 综述 p. 499 与文集 p. 512 有详论；Bailey 书 p. 14 的公式 (1) 与之等价。

**状态。**已证明（Thomae）。

**对照。**M02（Thomae 定理）。

## Entry 28——Entry 27 取 $q = -1$

**陈述。**若 $\mathrm{Re}(n+1) > -\mathrm{Re}(x+y)$、$-\mathrm{Re}(p-1)$，则
$${}_3F_2\left[\begin{matrix}-x, -y, p+n \\ n, p+n+1\end{matrix}\right] = \frac{(p+n)\Gamma(n)\Gamma(x+y+n+1)}{\Gamma(x+n+1)\Gamma(y+n+1)} \cdot {}_3F_2\left[\begin{matrix}-p, 1, x+y+n+1 \\ x+n+1, y+n+1\end{matrix}\right].$$

**出处。**Part II，Ch. 10，Entry 28（p. 39）。在 Entry 27 取 $q = -1$ 即得。

**状态。**已证明（Entry 27 的特例）。

**对照。**M02。

## Entry 29(a)——${}_3F_2$ 恒等式

**陈述。**若 $\mathrm{Re}\,n > -1$，则
$${}_3F_2\left[\begin{matrix}\frac12, \frac12, n+1 \\ 1, n+2\end{matrix}\right] = \frac{4(n+1)}{\pi}{}_3F_2\left[\begin{matrix}-n, 1, 1 \\ \frac32, \frac32\end{matrix}\right].$$

**出处。**Part II，Ch. 10，Entry 29(a)（p. 39）。在 Entry 28 取 $x = y = -\frac12$、$n = 1$、$p = n$ 即得。

**状态。**已证明（Entry 28 的特例）。

**对照。**M02。

## Entry 29(b)——(29.1)

**陈述。**若 $n$ 为非负整数，则
$$\frac{1}{n+1}{}_3F_2\left[\begin{matrix}\frac12, \frac12, n+1 \\ 1, n+2\end{matrix}\right] = \frac{\Gamma^2(n+1)}{\Gamma^2(n+\frac32)}\sum_{k=0}^{n}\frac{(\frac12)_k^2}{(k!)^2}. \tag{29.1}$$

**出处。**Part II，Ch. 10，Entry 29(b)（pp. 39–40）。拉马努金在致 Hardy 第一封信（p. 351）中给出；Watson 1929 年首次在印刷品中证明；1929–1931 年间有多篇论文讨论此式及其推广（见 Bailey 书 pp. 92–95）；Dutka 给出更新的证明；Lamm 与 Szabó 在 Coulomb 逼近工作中建立了超几何级数部分和的更多恒等式。(29.1) 右端的有限和出现于单复变函数论，称 Landau 常数；其与 Watson 论文的联系见原文。

**状态。**已证明（Watson 1929 年）。

**对照。**M02、M12（Landau 常数；与 Entry 32、Entry 35 相关）。

## Entry 29(c)——${}_3F_2$ 恒等式

**陈述。**若 $n$ 为任意复数，则
$${}_3F_2\left[\begin{matrix}\frac12, \frac12, n+1 \\ 1, n+2\end{matrix}\right] = \frac{2}{\pi}{}_3F_2\left[\begin{matrix}\frac12, 1, n+\frac32 \\ \frac32, n+2\end{matrix}\right].$$

**出处。**Part II，Ch. 10，Entry 29(c)（p. 40）。在 Entry 27 取 $p = -n-1$、$q = -\frac12$、$x = -n-\frac32$、$y = -\frac12$，并以 $n+\frac32$ 代 $n$ 即得。

**状态。**已证明（Entry 27 的特例）。

**对照。**M02。

## Entry 29(d)——${}_3F_2$ 恒等式

**陈述。**若 $\mathrm{Re}\,n > -\frac32$，则
$${}_3F_2\left[\begin{matrix}\frac12, 1, n+\frac32 \\ \frac32, n+2\end{matrix}\right] = \frac{\sqrt{\pi}\,\Gamma(n+2)}{\Gamma(n+\frac32)}{}_3F_2\left[\begin{matrix}\frac12, \frac12, -n \\ 1, \frac32\end{matrix}\right].$$

**出处。**Part II，Ch. 10，Entry 29(d)（p. 40）。在 Entry 27 取 $p = -\frac12$、$q = -1$、$x = n$、$y = -\frac12$、$n = 1$ 即得。

**状态。**已证明（Entry 27 的特例）。

**对照。**M02。

**推论 1。**设 $G$ 为 Catalan 常数，即 $G = \sum_{k=0}^{\infty}(-1)^k/(2k+1)^2$ (29.2)，则
$$\frac{\pi}{4}{}_3F_2\left(\frac12, \frac12, \frac12; 1, \frac32\right) = G. \tag{29.3}$$
（在 Entry 29(a) 取 $n = -\frac12$，得 $\frac{\pi}{2}{}_3F_2(\frac12, \frac12, \frac12; 1, \frac32) = {}_3F_2(\frac12, 1, 1; \frac32, \frac32)$；而 Ch. 9 第 32 节例 (i) 给出 ${}_3F_2(\frac12, 1, 1; \frac32, \frac32) = 2G$（Ch. 9 Entry 32 例 (i)：$\sum 2^{2k}(k!)^2/((2k)!(2k+1)^2) = 2G$），故得 (29.3)。**与 Ch. 9 Entry 32 的互见**，不去重。）

**推论 2。**当 $n \to \infty$ 时，$\pi\,{}_3F_2(\frac12, \frac12, n; 1, n+1) \sim \mathrm{Log}\,n + 4\mathrm{Log}\,2 + \gamma$。（由 Entry 29(b)、Watson 的渐近公式与 Stirling 公式；R. J. Evans 推广了推论 2；Entry 35(i) 给出更完整的渐近展开。）

## Entry 30——${}_3F_2$ 对称恒等式

**陈述。**若 $\mathrm{Re}\,n > -\mathrm{Re}\,x$、$-\mathrm{Re}\,y$，则
$${}_3F_2\left[\begin{matrix}-x, 1, y+n \\ n, y+n+1\end{matrix}\right] = \frac{y+n}{x+n}{}_3F_2\left[\begin{matrix}-y, 1, x+n \\ n, x+n+1\end{matrix}\right].$$

**出处。**Part II，Ch. 10，Entry 30（p. 41）。在 Entry 28 取 $y = -1$、$p = y$ 即得。

**状态。**已证明（Entry 28 的特例）。

**对照。**M02。

## Entry 31——Whipple 变换特例

**陈述。**若 $\mathrm{Re}(x+y+n+1) > 0$、$\mathrm{Re}(2x+2y+2z+2u+3n+4) > 0$，则
$${}_6F_5\left[\begin{matrix}\frac12n+1, n, -x, -y, -z, -u \\ \frac12n, x+n+1, y+n+1, z+n+1, u+n+1\end{matrix}; -1\right]$$
$$= \frac{\Gamma(x+n+1)\Gamma(y+n+1)}{\Gamma(n+1)\Gamma(x+y+n+1)}{}_3F_2\left[\begin{matrix}-x, -y, z+u+n+1 \\ z+n+1, u+n+1\end{matrix}\right].$$

**出处。**Part II，Ch. 10，Entry 31（p. 41）。Whipple 变换 (6.1) 的直接推论；见 Bailey 书 p. 28。值得注意的是，拉马努金并未发现 Whipple 的变换，但他在 Whipple 1926 年证明之前约 20 年就发现了这一重要的特例；Whipple 定理的启发性讨论见 Askey 的文章。

**特例 (31.1)。**取 $-n = x = y = z = u = -\frac12$，得
$$1 - 5\left(\frac12\right)^5 + 9\left(\frac{1\cdot3}{2\cdot4}\right)^5 - 13\left(\frac{1\cdot3\cdot5}{2\cdot4\cdot6}\right)^5 + \cdots$$
$$= \frac{1}{\Gamma(\frac32)\Gamma(\frac12)}{}_3F_2\left[\begin{matrix}\frac12, \frac12, \frac12 \\ 1, 1\end{matrix}\right] = \frac{2}{\Gamma^4(\frac34)}. \tag{31.1}$$
（用第 7 节例 18：$\sum ((\frac12)_k/k!)^3 = \pi/\Gamma^4(\frac34)$。）此结果见于拉马努金致 Hardy 第一封信（p. xxviii）与 Hardy 书 p. 7 Eq. (1.4)；Watson 给出与本书相同的证明，Hardy 另有证明。**注意**：本例级数的系数是 $4k+1$（$1, 5, 9, 13, \ldots$），不是 $2k+1$。

**状态。**已证明（Whipple 变换的特例；拉马努金约 1906 年已得）。

**对照。**M02（Whipple 变换；与 Entry 6 的 (6.1) 互见）。

## Entry 32——(32.1)

**陈述。**若 $x+y+z = 0$ 且 $x$ 为正整数，则
$${}_3F_2\left[\begin{matrix}n, -x, -y \\ n+1, z\end{matrix}\right] = \frac{\Gamma(n+1)\Gamma(x+1)}{\Gamma(n+x+1)}\sum_{k=0}^{x}\frac{(n)_k(y+z)_k}{(z)_kk!}. \tag{32.1}$$

**出处。**Part II，Ch. 10，Entry 32（pp. 41–42）。证明用 Bailey 的恒等式 (32.2)：
$$\sum_{k=0}^{n-1}\frac{(a)_k(b)_k}{(f)_kk!} = \frac{\Gamma(a+n)\Gamma(b+n)}{\Gamma(n)\Gamma(a+b+n)}{}_3F_2\left[\begin{matrix}a, b, f+n-1 \\ f, a+b+n\end{matrix}\right], \tag{32.2}$$
（Bailey 书 p. 93），取 $a = n$、$b = y+z$、$f = z$、$n = x+1$，并用 $x+y+z = 0$。Berndt 注：Entry 29(b) 不是 Entry 32 的特例，但 (32.2) 推广了 Entry 29(b)；$x+y+z = 0$ 的前提拉马努金未提；Entry 33（下）中拉马努金给了这一前提。

**状态。**已证明（在 $x+y+z = 0$ 前提下，经 (32.2)）。

**对照。**M02。**关于前提的注记见末尾小结「本轮发现」第 2 项**：Berndt 称 (32.1) 在 $x+y+z \ne 0$ 时一般为假，但本轮数值与初等证明均表明 (32.1) 对一般参数恒成立（待独立核对）。

## Entry 33——(32.2) 的推论

**陈述。**若 $x+y+z = 0$ 且 $x+y+n$ 为正整数，则
$${}_3F_2\left[\begin{matrix}n, -x, -y \\ n+1, z\end{matrix}\right] = \frac{\Gamma(n+1)\Gamma(x+y+n+1)}{\Gamma(x+n+1)\Gamma(y+n+1)}\sum_{k=0}^{x+y+n}\frac{(-x)_k(-y)_k}{(z)_kk!}.$$

**出处。**Part II，Ch. 10，Entry 33（p. 42）。在 (32.2) 取 $a = -x$、$b = -y$、$f = z$，并以 $x+y+n+1$ 代 $n$ 即得。此处拉马努金给了 $x+y+z = 0$ 的前提。

**状态。**已证明（经 (32.2)）。

**对照。**M02。

## Entry 34——Gauss ${}_2F_1$ 在 $1/2$ 的求值

**陈述。**若 $x$、$y$ 为任意复数，则
$${}_2F_1\left(x, y; \frac12(x+y+1); \frac12\right) = \frac{\sqrt{\pi}\,\Gamma(\frac12x+\frac12y+\frac12)}{\Gamma(\frac12x+\frac12)\Gamma(\frac12y+\frac12)}.$$

**出处。**Part II，Ch. 10，Entry 34（p. 42）。Gauss 首证；Bailey 书 p. 11 Eq. (2)。下述结果归于 Kummer，见 Bailey 书 p. 11 Eq. (3)。

**推论。**若 $x$、$n$ 为任意复数，则
$${}_2F_1\left(\frac12-\frac12x, \frac12+\frac12x; \frac12n+\frac12; \frac12\right) = \frac{\sqrt{\pi}\,2^{(1-n)/2}\Gamma(\frac12n+\frac12)}{\Gamma(\frac14\{n-x+2\})\Gamma(\frac14\{n+x+2\})}.$$
例 1、2 未明写，分别为 $x = 0$、$x = \frac12$ 的特例。

**状态。**已证明（Gauss；推论归于 Kummer）。

**对照。**M02、M07。

## Entry 35(i)——$\varphi(n)$ 的渐近展开

**定义。**拉马努金在第一本笔记 p. 239 定义 $\varphi(n) = \sum_{k=0}^{n-1}(\frac12)_k^2/(k!)^2$（整数 $n$）；Berndt 注：更妥当的做法是按 (29.1) 定义，对一切复数 $n$，
$$\varphi(n) = \frac{\Gamma^2(n+\frac12)}{\Gamma(n)\Gamma(n+1)}{}_3F_2\left[\begin{matrix}\frac12, \frac12, n \\ 1, n+1\end{matrix}\right]. \tag{35.1}$$

**陈述。**设 $\varphi(n)$ 如 (35.1) 所定义，则当 $n \to \infty$ 时
$$\pi\varphi\left(\frac{n+1}{4}\right) - \psi\left(\frac{n+1}{2}\right) \sim 3\mathrm{Log}\,2 + \gamma + \frac{3}{4n^2} - \frac{99}{32n^4} + \frac{999}{32n^6} + \cdots.$$

**出处。**Part II，Ch. 10，Entry 35(i)（pp. 42–45）。Watson 与 Dutka 各自导出 $\varphi(n)$ 的渐近展开，但三者的展开形式各不相同；Berndt 采用 Dutka 的渐近级数 $U_n$ (35.2) 证得拉马努金的公式，中间用 Legendre 倍元公式 $2\psi(\frac{n+1}{2}) = \psi(\frac{n+1}{4}) + \psi(\frac{n+3}{4}) + 2\mathrm{Log}\,2$、Stirling 公式 $\psi(x) \sim \mathrm{Log}\,x - 1/(2x) - \sum B_{2k}x^{-2k}/(2k)$，以及 Tricomi–Erdélyi 的 $\Gamma(x+a)/\Gamma(x+b)$ 渐近公式（(35.4)–(35.9)）。Entry 35(i) 是第 29 节推论 2 的推广。

**状态。**已证明（Dutka 的展开；Berndt 据此证得拉马努金公式）。

**对照。**M02、M12（渐近展开；Landau 常数）。

## Entry 35(ii)——(35.10)

**陈述。**设 $\varphi(n)$ 如 (35.1) 所定义，则对每个非负整数 $n$，
$$\frac{\pi^2}{4}\varphi\left(n+\frac12\right) = \sum_{k=0}^{n-1}\frac{(k!)^2}{(\frac32)_k^2} + 2G, \tag{35.10}$$
其中 $G$ 为 Catalan 常数（(29.2)）。

**出处。**Part II，Ch. 10，Entry 35(ii)（p. 45）。先证 Entry 35(iv)，再归纳。

**状态。**已证明（归纳法）。

**对照。**M02（Catalan 常数；与 Ch. 9 Entry 32 互见）。

## Entry 35(iii)——(35.11)

**陈述。**设 $\varphi(n)$ 如 (35.1) 所定义，则对每个非负整数 $n$，
$$2\varphi\left(n+\frac14\right) = 1 + \frac{16\Gamma^4(\frac34)}{\pi^3}\sum_{k=0}^{n-1}\frac{(\frac34)_k^2}{(\frac54)_k^2}. \tag{35.11}$$

**出处。**Part II，Ch. 10，Entry 35(iii)（p. 45）。先证 Entry 35(iv)，再归纳。

**状态。**已证明（归纳法）。

**对照。**M02（$\Gamma(\frac34)$；与第 7 节例 18、Entry 31 (31.1) 互见）。

## Entry 35(iv)——$\varphi(\frac12)$ 与 $\varphi(\frac14)$

**陈述。**设 $\varphi(n)$ 如 (35.1) 所定义，则
$$\varphi\left(\frac12\right) = \frac{8}{\pi^2}G \quad\text{和}\quad \varphi\left(\frac14\right) = \frac12.$$

**出处。**Part II，Ch. 10，Entry 35(iv)（pp. 45–47）。证明：由 (35.1) 与第 29 节推论 1，$\varphi(\frac12) = \frac{2}{\pi}{}_3F_2(\frac12, \frac12, \frac12; 1, \frac32) = \frac{8}{\pi^2}G$；$\varphi(\frac14) = \frac12$ 的证明见 pp. 45–47。注：第一本笔记 p. 239 中 35(iv) 列在 (35.10)(35.11) 之前，且拉马努金先给递推 (35.12)，似亦用归纳法证明。

**状态。**已证明。

**对照。**M02（Catalan 常数）。

## 小结

- 本章是超几何级数的系统开篇：Entry 1–7 为经典求值定理（Dougall、Saalschütz、Dixon、Gauss）及其推论网；Entry 8 的 Gauss 定理附拉马努金本人的证明草图（第二本笔记中唯一的证明草图）；Entry 9–18 为由 Gauss 定理对数微分、望远镜求和、形式幂级数技巧派生的级数与递推；Entry 19–28 为 ${}_2F_1$、${}_3F_2$ 的变换群（Pfaff、Kummer、Euler、Thomae）；Entry 29–35 为以 (29.1)（Landau 常数）与 $\varphi(n)$ 为中心的求值与渐近展开，收束于 Catalan 常数 $G$ 与 $\Gamma(\frac34)$。
- 与 Ch. 9 的互见：Entry 29 推论 1 的证明引用 Ch. 9 第 32 节例 (i) 的 ${}_3F_2(\frac12, 1, 1; \frac32, \frac32) = 2G$；Entry 31 (31.1) 用第 7 节例 18；Entry 35(ii)(iii) 与 Ch. 9 的 Catalan 常数主题呼应；Entry 14 的同类结果见 Ch. 9。
- 数值复核（mpmath 30 位；脚本在工作目录，未入仓库）：Entry 1（Dougall ${}_7F_6$）、Entry 2、Entry 3、Entry 4（$\psi$ 和）、Entry 5（三点）、Entry 7（Dixon 终止与非终止两点）、Entry 7 推论 1 (7.1)、推论 6 (7.3)（三点）、Entry 8（两点）、Entry 9、Entry 10、Entry 11、Entry 12(a)（$n = 1$–$5$）、Entry 12(b)（$r = 1$–$3$）、Entry 13 例 1 与 (13.5)（$r = 1$）、Entry 14 例 14（$2/\pi$，经 ${}_4F_3$ 闭式）、Entry 15（部分和 $N = 4000$，只核量级）、Entry 19、21、22、23、26、27、28、29(a)、29(b)（$n = 1, 2$）、29 推论 1（$= G$）、30、31 (31.1)（经 ${}_6F_5$ 闭式）、32（反例核查，见下）、33、34、35(iv)（$\varphi(\frac12)$、$\varphi(\frac14)$）、35(ii)（$n = 1$）、35(iii)（$n = 1$）、35(i)（$n = 50$ 渐近，差 $1.5\times 10^{-11}$）、第 7 节例 18、Entry 6 推论与 Entry 15 推论（$x = 0.1/0.01/0.001$ 数值趋势），合计约 55 项检查全部通过。复核中的插曲（均已解决，非书错）：Entry 5 在 $x = y = z = 0$ 处的手算误报（$\Gamma(2) = 1$ 误算为 $\Gamma(3) = 2$）；Entry 13 例 1 初版误把因子平方（应为一次方）；Entry 14 例 14 与 Entry 31 (31.1) 初版误把级数系数写成 $2k+1$（实为 $4k+1$），改用 ${}_4F_3$/${}_6F_5$ 闭式后通过；Entry 26 初版左端多乘 $(1-x)^{\alpha+\beta-\gamma}$，按原文 $(1-x)^{\alpha+\beta}$ 纠正后通过；nsum 对慢收敛级数（Entry 9、10、13 (13.5)）与慢收敛交错级数（Entry 14 例 14、Entry 31 (31.1)）会误报，改用直接求和加解析尾项或超几何闭式复核；150 DPI 曾把 Entry 14 例 14 证明中的 $\Gamma(\frac32)$ 误读为 $\Gamma(\frac34)$，300 DPI 放大图确认印文确为 $\Gamma(\frac32)$，无错印。
- **本轮发现的原书印文问题**（数值证实，原文未改动，标待核对）：
  1. **Entry 15 推论符号错**：原文印 $\pi\,{}_2F_1(\frac12, \frac12; 1; 1-x) \sim \mathrm{Log}\,x + 4\mathrm{Log}\,2$（$x \to 0$），应为 $-\mathrm{Log}\,x + 4\mathrm{Log}\,2$。数值：$x = 0.001$ 时左端 $9.6823$，订正版 $9.6803$（差随 $x \to 0$ 缩小），印文版 $-4.1352$（符号都反了）；且与本书自引的 (15.1) 取 $a = b = \frac12$、$\psi(\frac12) = -\gamma - 2\mathrm{Log}\,2$ 的结果矛盾。
  2. **Entry 32 后的注释有误**：Berndt 称「若 $x+y+z \ne 0$，(32.1) 一般为假」，并举例 $x = 2$、$y = z = -\frac12$。但数值复核表明 (32.1) 在该例对 $n = 1$–$5$ 均成立（两端恒为 $2(2n+1)/((n+1)(n+2))$：$n = 1$ 时 $1$、$n = 2$ 时 $5/6$、$n = 3$ 时 $7/10$）；另在 5 组随机参数（$x+y+z \ne 0$，含非整数 $n$、$y$、$z$）下两端吻合到 $10^{-30}$。初等证明：由 Beta 积分 $1/(n+k) = \int_0^1 t^{n+k-1}dt$ 得左端 $= n\int_0^1 t^{n-1}{}_2F_1(-x, -y; z; t)dt$，再用 Pfaff 变换与换元 $u = t/(1-t)$、逐项 Beta 积分即得右端（$x$ 为正整数时级数终止，积分收敛条件满足）。故 (32.1) 对一般参数恒成立，$x+y+z = 0$ 的前提并非必要；Berndt 的注释与所举反例均不成立。**此结论与标准整理本相左，须独立核对**（已标待核对第 2 项），文件正文仍按原书印文转述 (32.1) 及其前提，不擅自改动原文。
- 拉马努金原文疏失（Berndt 已指出）：见章首背景列表；其中 Entry 18(ii) 的断言经 Berndt 反例已否定，Entry 32 的前提缺失问题见上。

## 待核对清单

1. IMSC 整理表本章的结果数（2026-11-06 实测 imsc.res.in 当日不可达，未能补录；此前 Ch. 1–9 亦多次不可达）。
2. **Entry 32 注释的本轮发现**：(32.1) 在 $x+y+z \ne 0$ 时是否恒成立（数值 5 组随机参数吻合到 $10^{-30}$ + Beta 积分与 Pfaff 变换的初等证明），与 Berndt「一般为假」的说法及所举反例 $x = 2$、$y = z = -1/2$ 相左，须独立核对（或查其他印次、勘误表）。
3. **Entry 15 推论的符号问题**：原文 $\mathrm{Log}\,x + 4\mathrm{Log}\,2$ 与 (15.1) 及数值均矛盾，应为 $-\mathrm{Log}\,x + 4\mathrm{Log}\,2$；须查其他印次或勘误表确认是否为印次错误。
4. Berndt 章首计数（本章共几条陈述）：章首导言未见计数句，待核对原书章首。
5. TIFR 影印版页码：Berndt 文中明确引用的有例 (iv) 笔记本 p. 118、推论 6 (7.3) p. 119、推论 21 p. 120、Entry 13 推论 1（$S_r$ 重定义）p. 124、Entry 14 p. 124、Entry 35(iv) 第一本笔记 p. 239；其余各条的 TIFR 页码待核对。
6. Entry 4 例 (i)–(v) 的确切形式（OCR 损坏严重，只核对了推导来源）；Entry 7 推论 2、8–11、20–24 与例 1–13、15–19 的确切形式（本文件只给主题与已核对的几条）；Entry 10 例 1–7 的确切形式（只核对了例 1–3 的来源）；Entry 13 推论 2 与例 2 的积分细节；Entry 7 例 15 的确切形式。
7. Rakha–Ibrahim–Rathie 短文（arXiv:1302.4902，Remark on two results due to Ramanujan on hypergeometric series）称 Berndt Part II 的 Entry 34(ii)（(34.3)，p. 97）与 Entry 21（p. 64）有误并给出订正；但其页码与本章不符（本章 Entry 21 在 p. 37、Entry 34 在 p. 42），疑似指 Ch. 11 的同名 Entry（Ch. 11 起 p. 48，Entry 21 约 p. 64、Entry 34 约 p. 97 吻合），填 Ch. 11 时再核对，勿当作本章发现。
8. Entry 6 推论的 $\pi^2/4\,{}_5F_4$ 在 $1-x$ 处的渐近只核对了数值趋势（$x = 0.1$、$0.01$），未做严格证明核对；Entry 15 的部分和渐近只核对了 $N = 4000$ 的量级（差约 $3.6\times 10^{-4}$，与 $O(1/N)$ 一致）。

## 来源说明

- 整理本：Bruce C. Berndt, *Ramanujan's Notebooks*, Part II, Springer, 1989, Ch. 10, pp. 7–47。电子版：archive.org 标识符 `ramanujan_notebooks_ii`（《Ramanujan's Notebooks, Part 2》），PDF 14,538,056 字节、371 叶，DjVu OCR 文本 560,610 字节。**PDF 页与书页对应关系：PDF 页 = 书页 + 12**（与 Part I 的 +10 不同；pdftotext 分页实测章首在 PDF 页 19、Ch. 11 章首在 PDF 页 60、Ch. 10 末页书页 47 在 PDF 页 59）。本章范围：书页 7–47，PDF 页 19–59，共 41 页。全部公式按 PDF 原图（150 DPI）逐字转录，关键公式另用 300 DPI 放大图确认（Entry 14 例 14 证明的 $\Gamma(\frac32)$、Entry 15 推论的符号、Entry 32 的 (32.1) 与注释、Entry 34 推论、Entry 35(i) 的 $\varphi(n)$ 定义）。
- 目录核对：Part II 目录（PDF 页 12）确认 Ch. 10 Hypergeometric Series, I 起书页 7；Ch. 11 Hypergeometric Series, II 起书页 48；Ch. 12 Continued Fractions 起书页 103；Ch. 13 Integrals and Asymptotic Expansions 起书页 185；Ch. 14 Infinite Series 起书页 240；Ch. 15 Asymptotic Expansions and Modular Forms 起书页 300。
- 书目：Part II，Springer，1989，XII + 360 页，DOI 10.1007/978-1-4612-4530-8，ISBN 0-387-96794-X。
- 数值复核：mpmath 30 位；复核脚本在工作目录（未入仓库）。下一章：Part II Ch. 11 Hypergeometric Series, II。
