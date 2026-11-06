# Part I · 第 4 章 Iterates of the Exponential Function and an Ingenious Formal Technique（指数函数的迭代与一种巧妙的形式技巧）

出处：Bruce C. Berndt, *Ramanujan's Notebooks*, Part I, Springer, 1985, 第 4 章，pp. 85–108（第 3 章 pp. 44–84；第 5 章起自 p. 109）。对应拉马努金**第二本笔记第 4 章**。

## 背景与记号

- 本章由两个主题组成。**前八节**是指数函数的迭代，是第 3 章 Bell 数理论的续篇：记 $F_0(x) = x$，$F_{r+1}(x) = \exp\{F_r(x)\} - 1$，则 $F_1(x) = e^x - 1$ 的幂级数系数是 Bell 数（$e^{e^x-1} = \sum_{n=0}^{\infty} B(n)x^n/n!$）；进一步的迭代在文献中极少有人研究，最系统的研究是 Bell [2]（1938），Becker–Riordan 与 Carlitz 建立了这些广义 Bell 数的算术性质，Ginsburg 亦有简短讨论；组合解释见 Stanley [1, Theorem 6.1]。Berndt 强调：除拉马努金外，似乎无人研究过系数 $\varphi_k(r)$ 与 $f_k(x)$，该理论值得继续发展。
- **第 9–13 节**是另一个主题，展示拉马努金最喜爱的一种形式技巧：若两个关于 $x$ 的函数相等，则把 $x^n$ 换成 $\varphi(n)$ 可得一般定理。Berndt 明言：拉马努金的方法是**严格形式化**的，所得结果只在很强的限制下成立；书中对每个结果都给出严格陈述与证明。本章最著名的公式是第 11 节的 (0.1)：
$$\int_0^{\infty} x^{n-1} \sum_{k=0}^{\infty} \varphi(k)(-x)^k\,dx = \frac{\pi\varphi(-n)}{\sin(\pi n)}, \qquad n > 0$$
Hardy 在其著作 [20, p. 15] 中称这是拉马努金「特别喜爱」的公式之一，并在第 11 章中对 Entry 11 及其推论 1、3 作了详尽讨论。
- **季报背景**：拉马努金赴英前约一年获马德拉斯大学奖学金，按规定于 1913 年 8 月 5 日、1913 年 11 月 7 日、1914 年 3 月 9 日向数学评议会提交了三份季报；前两份季报几乎全是 (0.1) 一类公式及其应用，拉马努金还对 Entry 11 的相关公式给出详细证明并列出他认为成立的假设。后来（可能经 Hardy 指出）他发现假设不够强；在 [13]、[15, pp. 53–58] 中他写道：「我对上述结果的证明用了一个一般公式，其真理性依赖于我尚未完全研究清楚的条件。」第 11–13 节的全部公式都已在季报中建立，另有更多公式。
- **第一本笔记的对应**：第一本笔记第 5 章与第二本笔记第 4 章的前八节大体重合（第二本是第一本的修订扩充版）；第 9–15 节的公式在第一本笔记第 5 章中找不到。但 Entry 11 见于第一本笔记 p. 182（第 12 章某页的背面）；第一本笔记 pp. 180、182、184 载有 Entry 11 的 13 个应用，其中只有一个（Entry 13(ii)）出现在第二本笔记第 4 章中。
- 本章在原文中明确出现编号的 Entry 共 **14 条**：Entry 1–8、Entry 10–15。**没有 Entry 9**：第 9 节只含例题 1–4 与推论 1–2，未编号为 Entry。IMSC 整理表计本章的结果数本次未能读取（imsc.res.in 当日不可达），待补。
- **本章的拉马努金原文疏失**（Berndt 已指出，详见各条与末尾小结）：第 6 节末拉马努金无意中暗示 $f_1(x)$ 是 7 次多项式；第 9 节推论 2 在 $n > 2$ 时不成立；Entry 11 的推导是纯形式的，Hardy 指出拉马努金并未真正证明这些公式；Entry 10 的推论与例 1 的条件极少满足，(10.1) 常为发散的渐近级数。

## 记号说明

- $\varphi_k(r)$：迭代系数，见 (1.2)；$\varphi(z)$：第 9–11 节的任意整函数；两者同名异义，见各条上下文。$\psi_k(n)$：(4.3) 的系数；$\psi(n)$：Entry 12 的余弦变换；$\psi(k) = \sum_{n \le k} 1/n$：第 10 节例 2 第三版与例 4 的调和数——三者亦同名异义。
- $B_n$：Bernoulli 数（$B_1 = -1/2$，$B_2 = 1/6$，$B_4 = -1/30$，$B_6 = 1/42$；奇数项 $B_{2k+1} = 0$，$k \ge 1$）。$H_n = \sum_{k=1}^{n} 1/k$：调和数。$\gamma$：Euler 常数（拉马努金记作 $c$）。

## 本章结构

| Entry | 页 | 内容 |
|---|---|---|
| Entry 1 | 86–87 | 迭代函数 $F_r(x)$ 的定义；(1.2) 两类系数 $\varphi_k(r)$、$f_k(x)$ |
| Entry 2 | 87 | $F_r'(x) = \{1+F_r(x)\}F_{r-1}'(x)$ (2.1)；推论 1、推论 2 (2.2) |
| Entry 3 | 87–88 | $f_1'(x) = x + \sum B_n f_n(x)$；辅助函数 $\psi(x)$ (3.4)–(3.6) |
| Entry 4 | 89–90 | $nf_n(x) = f_1(x)f_{n-1}'(x)$ (4.1)；(4.3) 的 $\psi_k(n)$；推论 1、推论 2 |
| Entry 5 | 90 | $f_1(x) = (1+x)f_1\{\mathrm{Log}(1+x)\}$ |
| Entry 6(i) | 90–91 | $1/n!$ 与 $1/n$ 的 $\psi_k$ 求和 (6.1)(6.2) |
| Entry 6(ii) | 91–92 | $\psi_1,\psi_2,\psi_3$ 的闭式 (6.3)–(6.5)；$\varphi_1(2r),\dots,\varphi_7(2r)$；$f_1(x)$ 前七项 |
| Entry 7 | 92–94 | $F_{2r}(x)$ 的展开 (7.1)(7.2)；例 1：$f_1'f_1''$ 的恒等式；例 2 未收录 |
| Entry 8 | 94–95 | 调和数幂和 (i)(ii)(iii) |
| §9 例 1–4 | 95–98 | 形式技巧的四个严格化例题；推论 1（渐近）、推论 2（$n>2$ 时不成立） |
| Entry 10 | 100–101 | 二项系数对称和；推论 (10.1) 与 $f(0) = \varphi(r)$；例 1 |
| §10 例 | 101–105 | $\tan^{-1}$ 例；例 2 三版（Euler 积分、连分数、指数积分）；例 3、例 4 |
| Entry 11 | 105–107 | $\int_0^{\infty} x^{n-1}\sum \varphi(k)(-x)^k/k!\,dx = \Gamma(n)\varphi(-n)$；推论 1–5 |
| Entry 12 | 107 | Fourier 余弦变换的反演公式 (i)(ii) |
| Entry 13(i)(ii) | 107 | $\int_0^{\pi/2} \sin^m x\cos^n x\,dx$ 与 $\int_0^{\pi/2} \cos^m x\cos nx\,dx$ |
| Entry 14 | 107–108 | $\prod_{n=1}^{\infty}(1+x^6/n^6)$ 的闭式 |
| Entry 15 | 108 | $G_k$（奇数倒数和）与 (15.1)；系数恒等式 $\sum \binom{n}{k}(-2)^{k-1}/k = G_n$ |

## Entry 1——迭代函数 $F_r(x)$ 的定义

**陈述。**令 $F_0(x) = x$，定义
$$F_{r+1}(x) = \exp\{F_r(x)\} - 1, \qquad (1.1)$$
其中 $r$ 为任意整数。于是 $F_1(x) = e^x - 1$，$F_2(x) = e^{e^x-1} - 1$，$F_{-1}(x) = \mathrm{Log}(1+x)$，$F_{-2}(x) = \mathrm{Log}\{1+\mathrm{Log}(1+x)\}$。$r \ge 0$ 时 $F_r(x)$ 为整函数；$r < 0$ 时在原点某邻域内解析；$F_r(0) = 0$。拉马努金默认 $F_r(x)$ 可对一切实数 $r$ 定义（未说明如何定义；Comtet [1, pp. 144–148] 论述了形式幂级数的任意实数阶迭代，本情形见该书 p. 147）。拉马努金写
$$F_r(x) = \sum_{k=1}^{\infty} \varphi_k(r)x^k = \sum_{k=0}^{\infty} f_k(x)r^k, \qquad (1.2)$$
两边均视为形式幂级数。Comtet 证明 $\varphi_k(r)$ 是 $r$ 的 $k-1$ 次多项式；代入前一級數并比较 $r$ 的同次幂系数，可得 $f_k(x)$ 在原点有 $k+1$ 重零点。

**出处。**Berndt Part I, Ch. 4, Entry 1, pp. 86–87。

**状态。**定义（已证明的性质：$\varphi_k(r)$ 为 $k-1$ 次多项式见 Comtet；$f_0(x) = x$）。

**对照。**$F_1(x) = e^x - 1$ 的系数是 Bell 数，见 M13（Bell 数、Dobiński 公式）；$F_2(x) = e^{e^x-1}-1$ 是无穷幂塔 $e^{e^x}$ 的截断形式，见 M12（无穷幂塔）；形式幂级数的迭代见 M02。

## Entry 2——导数关系

**陈述。**对每个整数 $r$，
$$F_r'(x) = \{1+F_r(x)\}F_{r-1}'(x). \qquad (2.1)$$

**推论 1。**$r$ 为正整数时
$$F_r'(x) = \prod_{k=1}^{r} \{1+F_k(x)\}.$$

**推论 2。**$r$ 为任意整数，$n$ 为正整数时
$$n\{\varphi_n(r) - \varphi_n(r-1)\} = \sum_{k=1}^{n-1} (n-k)\varphi_k(r)\varphi_{n-k}(r-1). \qquad (2.2)$$
由此可归纳证明 $\varphi_n(r)$ 是 $r$ 的 $n-1$ 次多项式。

**出处。**Berndt Part I, Ch. 4, Entry 2, p. 87。

**状态。**已证明。数值复核（精确分数）：(2.2) 在 $n=3$、$r=2$ 时两边均为 $2$；在 $n=4$、$r=2$ 时两边均为 $7/3$（用 $\varphi_k(1) = 1/k!$ 与 $\varphi_k(2) = B(k)/k!$，$B(k)$ 为 Bell 数）。

**对照。**递推与卷积见 M13；$\varphi_n(r)$ 的多项式性质见 M02（形式幂级数）。

## Entry 3——$f_1'(x)$ 的 Bernoulli 展开

**陈述。**对每个实数 $x$，
$$f_1'(x) = x + \sum_{n=1}^{\infty} B_n f_n(x).$$
证明用 Euler–Maclaurin 公式 (3.1)：
$$\sum_{n=0}^{r-1} f(n) = \int_0^r f(x)\,dx + \sum_{n=1}^{\infty} \frac{B_n}{n!}\{f^{(n-1)}(r) - f^{(n-1)}(0)\}, \qquad (3.1)$$
其中 $B_n$ 为第 $n$ 个 Bernoulli 数。关键步骤：(3.2) $\mathrm{Log}\,F_r'(x) = \sum_{k=0}^{r-1} F_k(x)$；(3.4)
$$\mathrm{Log}\,F_r'(x) = \psi(x) + \int_0^r F_u(x)\,du + \sum_{n=1}^{\infty} \frac{B_n}{n!}\left.\frac{d^{n-1}}{du^{n-1}}F_u(x)\right|_{u=r},$$
其中 $\psi(x)$ 只依赖 $x$；比较 $r$ 的系数即得本条。

**推论。**$x$ 为实数时
$$\psi(x) = \int_0^x \frac{t - f_1'(t)}{f_1(t)}\,dt.$$
其中 (3.5) $\psi(x) = -\sum_{n=1}^{\infty} \frac{B_n}{n}f_{n-1}(x)$，(3.6) $\psi'(x)f_1(x) = -\sum_{n=1}^{\infty} B_n f_n(x) = x - f_1'(x)$（后一等式用 Entry 3，倒数第二步用 Entry 4）。

**出处。**Berndt Part I, Ch. 4, Entry 3, pp. 87–88。

**状态。**已证明（形式幂级数意义）。数值复核（mpmath，30 位）：$x = 0.1$ 时 $f_1'(x) = 0.0975806308664$，$x + \sum_{n=1,2,4,6} B_n f_n(x) = 0.0975806308684$，差 $2\times 10^{-12}$（截断与数值微分误差）。

**对照。**Euler–Maclaurin 公式与 Bernoulli 数见 M01（伯努利数定义缺口仍待补）、M12（渐近展开）；$f_n(x)$ 的级数见 M13。

## Entry 4——$f_n(x)$ 的递推与 $\psi_k(n)$

**陈述。**对每个正整数 $n$，
$$nf_n(x) = f_1(x)f_{n-1}'(x). \qquad (4.1)$$
证明用 Comtet 的一般定理：$F_{k+r}(x) = F_r\{F_k(x)\}$ (4.2)，其中 $k$、$r$ 为任意实数；对 $r$ 展开比较 $r$ 的系数得 $dF_k(x)/dk = f_1\{F_k(x)\}$，再比较 $k^{n-1}$ 的系数即得 (4.1)。

由 (1.2) 后注，$f_n(x)$ 在 $x = 0$ 处有 $n+1$ 重零点，故可写
$$f_n(x) = (\tfrac12 x)^n \sum_{k=1}^{\infty} (-1)^{k-1}\psi_k(n)x^k, \qquad n \ge 0. \qquad (4.3)$$

**推论 1。**$n$、$r$ 为正整数时
$$\text{(i)} \qquad n\psi_r(n) = \sum_{k=1}^{r} (n+k-1)\psi_k(n-1)\psi_{r-k+1}(1)$$
$$\text{(ii)} \qquad \varphi_n(2r) = \sum_{k=1}^{n} (-1)^{k-1}r^{n-k}\psi_k(n-k).$$

**推论 2。**$\psi_1(1) = 1$，且 $n \ge 2$ 时
$$(n+1)\psi_n(1) = \tfrac12\psi_{n-1}(1) + \sum_{k=1}^{N} B_{2k}2^{1-2k}\psi_{n-2k}(2k),$$
其中 $N$ 为 $(n-1)/2$ 或 $(n-2)/2$（视 $n$ 为奇数或偶数）。

**出处。**Berndt Part I, Ch. 4, Entry 4, pp. 89–90。

**状态。**已证明。数值复核（精确分数）：推论 1(ii) 与 Entry 6(ii) 的 $\varphi_n(2r)$ 多项式在 $n = 1,\dots,7$、$r = 1,2,3$ 时逐项一致；推论 2 在 $n = 2,\dots,6$ 时给出的 $\psi_n(1)$ 与 $f_1(x)$ 的系数逐项一致（$\psi_2(1) = 1/6$、$\psi_3(1) = 1/24$、$\psi_4(1) = 1/90$、$\psi_5(1) = 11/4320$、$\psi_6(1) = 1/3360$）；由推论 2 递推另得 $\psi_7(1) = -11/120960$（书中 $f_1(x)$ 只列到 $x^7$，此值不在原文中，系按同一递推导出）。

**对照。**$f_n(x)$ 的递推与 Bell 多项式见 M13；$\psi_k(n)$ 的组合递推见 M13；Bernoulli 数见 M01。

**记号说明。**本条的 $\psi_k(n)$ 与 Entry 3 推论的 $\psi(x)$、第 3 章的 $\psi(z)$ 均不同。

## Entry 5——$f_1(x)$ 的函数方程

**陈述。**对每个数 $x > -1$，
$$f_1(x) = (1+x)f_1\{\mathrm{Log}(1+x)\}.$$
证明：由 (4.2)，$F_{r-1}(x) = F_r\{F_{-1}(x)\} = F_r\{\mathrm{Log}(1+x)\}$；由 (1.2) 与 $f_0(x) = x$ 得 (5.1) $\exp\{F_{r-1}(x)\} = (1+x)\exp\{\sum_{k=1}^{\infty} f_k\{\mathrm{Log}(1+x)\}r^k\}$，另一面由 (1.1)(1.2) 得 (5.2) $\exp\{F_{r-1}(x)\} = 1 + F_r(x) = 1 + \sum_{k=0}^{\infty} f_k(x)r^k$；比较 $r$ 的系数即得。

**出处。**Berndt Part I, Ch. 4, Entry 5, p. 90。

**状态。**已证明。

**对照。**对数换元的函数方程见 M02（形式幂级数）、M09（对数积分背景）。

## Entry 6(i)——$1/n!$ 与 $1/n$ 的求和

**陈述。**对 $n \ge 1$，
$$\frac{1}{n!} = \sum_{k=1}^{n} (-1)^{k-1}2^{k-n}\psi_k(n-k) \qquad (6.1)$$
$$\frac{1}{n} = \sum_{k=1}^{n} 2^{k-n}\psi_k(n-k). \qquad (6.2)$$
证明：由 (1.1)(1.2)，$\sum_{n=1}^{\infty} \varphi_n(1)x^n = F_1(x) = e^x - 1 = \sum_{n=1}^{\infty} x^n/n!$，故 $\varphi_n(1) = 1/n!$；用 Entry 4 推论 1(ii) 得 (6.1)。又 $|x| < 1$ 时 $\sum_{n=1}^{\infty} \varphi_n(-1)x^n = F_{-1}(x) = \mathrm{Log}(1+x) = \sum_{n=1}^{\infty} (-1)^{n-1}x^n/n$，故 $\varphi_n(-1) = (-1)^{n-1}/n$；在推论 1(ii) 中取 $r = -1/2$ 得 (6.2)。

**出处。**Berndt Part I, Ch. 4, Entry 6(i), pp. 90–91。

**状态。**已证明。数值复核（精确分数）：(6.1)(6.2) 在 $n = 1,\dots,6$ 时逐项成立。

**对照。**$e^x - 1$ 与 $\mathrm{Log}(1+x)$ 的级数见 M02；$\psi_k$ 的递推见 Entry 4。

## Entry 6(ii)——$\psi_k(n)$ 的显式公式与 $\varphi_n(2r)$

**陈述。**对 $n \ge 1$，
$$\psi_1(n) = 1, \qquad (6.3)$$
$$\psi_2(n) = \frac{n+1}{6}\sum_{k=2}^{n+1} \frac1k, \qquad (6.4)$$
$$\psi_3(n) = \frac{(n+1)(n+2)}{72}\left\{\left(\sum_{k=2}^{n+2}\frac1k\right)^2 - \sum_{k=2}^{n+2}\frac{1}{k^2} - \frac{1}{n+2} + \frac12\right\}. \qquad (6.5)$$
证明：由 Entry 4 推论 2，$\psi_1(1) = 1$；在推论 1 中取 $r = 1$ 得 $\psi_1(n) = \psi_1(n-1)$，故 (6.3)。由推论 2，$\psi_2(1) = 1/6$；在推论 1 中取 $r = 2$ 并用 (6.3)，递推得 (6.4)。$\psi_3(n)$ 用 $\chi(n)$（定义为 $\psi_3(n) = (n+1)(n+2)\chi(n)$）处理：由推论 2，$\psi_3(1) = 1/24$，故 $\chi(1) = 1/144$；由推论 1 得递推 $\chi(n) = \chi(n-1) + \frac{1}{36(n+2)}\sum_{k=2}^{n} \frac1k + \frac{1}{24(n+1)(n+2)}$，求和即得 (6.5)。

此外，
$$\varphi_1(2r) = 1, \quad \varphi_2(2r) = r, \quad \varphi_3(2r) = r^2 - \tfrac16 r,$$
$$\varphi_4(2r) = r^3 - \tfrac{5}{12}r^2 + \tfrac{1}{24}r, \quad \varphi_5(2r) = r^4 - \tfrac{13}{18}r^3 + \tfrac16 r^2 - \tfrac{1}{90}r,$$
$$\varphi_6(2r) = r^5 - \tfrac{77}{72}r^4 + \tfrac{89}{216}r^3 - \tfrac{91}{1440}r^2 + \tfrac{11}{4320}r,$$
$$\varphi_7(2r) = r^6 - \tfrac{29}{20}r^5 + \tfrac{175}{216}r^4 - \tfrac{149}{720}r^3 + \tfrac{91}{4320}r^2 - \tfrac{1}{3360}r.$$
且
$$f_1(x) = \tfrac12 x^2 - \tfrac{1}{12}x^3 + \tfrac{1}{48}x^4 - \tfrac{1}{180}x^5 + \tfrac{11}{8640}x^6 - \tfrac{1}{6720}x^7 + \cdots$$
$\varphi_n(2r)$ 由 Entry 4 推论 1(ii) 算出（注意 $\psi_k(0) = 0$，$k \ge 2$）；用 (6.5) 算 $\psi_3(n)$ 不方便，宜直接用推论 1(i)；$\psi_k(n)$（$k \ge 4$）亦用推论 1(i)。$f_1(x)$ 的公式由 (4.3) 与 $\psi_k(1)$（$1 \le k \le 6$）的计算得。**拉马努金原文疏失**：在第二本笔记中，拉马努金无意中暗示 $f_1(x)$ 是 7 次多项式（Berndt 注）——实际它是无穷级数。

**出处。**Berndt Part I, Ch. 4, Entry 6(ii), pp. 91–92。

**状态。**已证明。数值复核（精确分数）：(6.4) 在 $n = 1$ 时给出 $\psi_2(1) = 1/6$；(6.5) 在 $n = 1,2,3,4$ 时给出 $\psi_3(1) = 1/24$、$\psi_3(2) = 1/6$、$\psi_3(3) = 89/216$、$\psi_3(4) = 175/216$，与 Entry 4 推论 1(i) 的递推逐项一致；$\varphi_n(2r)$ 七式在 $r = 1,2,3$ 时与推论 1(ii) 的求和逐项一致。

**对照。**调和数求和见 M01；$\varphi_n(2r)$ 的多项式见 M13；$f_1(x)$ 的级数见 M02。

## Entry 7——$F_{2r}(x)$ 的展开

**陈述。**令 $x = y(1-rx)$，$z = 1-rx$，则
$$F_{2r}(x) = y + \tfrac16 y^2\,\mathrm{Log}\,z + \tfrac{1}{72}y^3\{\mathrm{Log}^2 z + (1-\mathrm{Log}\,z)^2 - z\} + \cdots \qquad (7.1)$$
证明：由 (1.2) 与 (4.3)，
$$F_{2r}(x) = \sum_{n=1}^{\infty} (-1)^{n+1}\left\{\sum_{k=0}^{\infty} \psi_n(k)(rx)^k\right\}x^n. \qquad (7.2)$$
由 (6.3)，(7.2) 的第一项为 $x\sum_{k=0}^{\infty} (rx)^k = x/(1-rx) = y$；由 (6.4)，第二项为 (7.3)
$$-\frac{x^2}{6}\sum_{k=1}^{\infty} (k+1)\sum_{j=2}^{k+1} \frac1j (rx)^k,$$
与 $\tfrac16 y^2\,\mathrm{Log}\,z$ 的展开一致；第三项由直接计算得 $\frac{x^3}{72(1-rx)^3}\{3rx + \sum_{n=2}^{\infty} c(n)(rx)^n\}$，其中 $c(n) = \frac{6}{n} + \frac{4}{n}\sum_{j=2}^{n-1} \frac1j$（$n \ge 2$）；由 (6.5) 经很长的计算可证 $c(n)$ 等于 $72(1-rx)^3\sum_{k=0}^{\infty} \psi_3(k)(rx)^k$ 中 $(rx)^n$ 的系数（注意 $\psi_3(1) = 1/24$）。

**例 1。**对每个实数 $x$，
$$f_1'(x)f_1''(x) = f_1(x) - f_2(x) + \sum_{k=1}^{\infty} (2k+1)B_{2k}f_{2k+1}(x).$$
证明：对 Entry 3 求导得 $f_1''(x) = 1 - \tfrac12 f_1'(x) + \sum_{k=1}^{\infty} B_{2k}f_{2k}'(x)$，两边乘 $f_1(x)$ 并用 Entry 4 即得。

**例 2 不收录**：只是 Entry 7 在 $2r = n$、$x = 1/n$ 时的重述。

**出处。**Berndt Part I, Ch. 4, Entry 7, pp. 92–94。

**状态。**已证明（前三项已验证与 (7.2) 一致；「$\cdots$」的余项未展开）。数值复核（mpmath，30 位）：$r = 1$、$x = 0.1$ 时 $F_2(x) = 0.110900467100341$，(7.1) 前三项之和为 $0.110900662761331$，差 $-1.96\times 10^{-7}$（余项量级，与第四项一致）。

**对照。**$F_{2r}(x)$ 的对数展开见 M12（渐近展开）、M02（对数级数）；例 1 的 Bernoulli 卷积见 M01。

## Entry 8——调和数的幂和

**陈述。**令 $H_n = \sum_{k=1}^{n} 1/k$。若 $x$ 为正整数，则
$$\text{(i)} \qquad \sum_{k=1}^{x} H_k = (x+1)H_x - x,$$
$$\text{(ii)} \qquad \sum_{k=1}^{x} H_k^2 = (x+1)H_x^2 - (2x+1)H_x + 2x,$$
$$\text{(iii)} \qquad \sum_{k=1}^{x} H_k^3 = (x+1)H_x^3 - \tfrac32(2x+1)H_x^2 + 3(2x+1)H_x - 6x + \tfrac12\sum_{k=1}^{x} \frac{1}{k^2}.$$
证明：(i) 由交换求和次序得；(ii)(iii) 用分部求和 (8.1) $\sum_{k=1}^{x} a_k b_k = s_x b_x - \sum_{k=1}^{x-1} s_k(b_{k+1}-b_k)$（其中 $s_n = \sum_{k=1}^{n} a_k$），取 $a_k = b_k = H_k$ 得 (ii)，取 $a_k = H_k^2$、$b_k = H_k$ 得 (8.2)；再用 (8.3) $H_x^2 = \sum_{k=1}^{x} 1/k^2 + 2S$（其中 $S = \sum_{k=1}^{x} H_{k-1}/k$）消去 $S$ 得 (iii)。

**出处。**Berndt Part I, Ch. 4, Entry 8, pp. 94–95。

**状态。**已证明。数值复核（精确分数）：(i)(ii)(iii) 在 $x = 5$ 与 $x = 10$ 时逐项成立。

**对照。**调和数与分部求和见 M01、M02；$\sum 1/k^2$ 的出现见 M02（$\zeta(2)$ 背景）。

## 第 9 节——巧妙的形式技巧（无 Entry 9）

**拉马努金的方法。**本节开头拉马努金写道：「若两个关于 $x$ 的函数相等，则把 $x^n$ 换成 $\varphi(n)$ 即可得一般定理。」其「解法」（sol.）：置 $x = 1$ 乘以 $f(0)$，再把 $x$ 换成 $x, x^2, x^3, x^4, \dots$，分别乘以 $f'(0)/1!$、$f''(0)/2!$、$f'''(0)/3!$ 等，相加；于是 $x^n$ 的位置出现 $f(x^n)$（$n$ 取正负值均可）；把 $f(x^n)$ 换成 $\varphi(n)$ 即得结果（拉马努金把 $n!$ 记作 $\lfloor n$）。Berndt 明言：由此得到的公式只在很强的限制下成立；下面只对一个例子详述该方法，其余每个结果都给出严格证明（附极强的假设）。

**方法的演示。**取 $\tan^{-1} x + \tan^{-1}(1/x) = \pi/2$。按上述步骤写下
$$f(0)(\tan^{-1} 1 + \tan^{-1} 1) = \tfrac{\pi}{2}f(0), \quad \frac{f'(0)}{1!}(\tan^{-1} x + \tan^{-1}(1/x)) = \tfrac{\pi}{2}\frac{f'(0)}{1!}, \quad \cdots$$
把 $\tan^{-1} z$（$z$ 为 $x$ 的任意整数幂）换成 Maclaurin 级数，相加并交换求和次序得
$$\sum_{n=0}^{\infty} \frac{(-1)^n\{f(x^{2n+1}) + f(x^{-2n-1})\}}{2n+1} = \tfrac{\pi}{2}f(1),$$
把 $f(x^k)$ 换成 $\varphi(k)$ 得
$$\sum_{n=0}^{\infty} \frac{(-1)^n\{\varphi(2n+1) + \varphi(-2n-1)\}}{2n+1} = \tfrac{\pi}{2}\varphi(0).$$
Berndt 注：这一形式步骤有无数困难。

**例 1。**设 $\varphi(z)$ 为整函数，存在趋于 $\infty$ 的正数列 $r_n$ 使
$$I_n \equiv \frac{1}{2\pi i}\int_{|z|=r_n} \frac{\varphi(z)\,dz}{z\cos(\pi z/2)} = o(1),$$
则
$$\lim_{N\to\infty} \sum_{k=-N}^{N} \frac{(-1)^k\varphi(2k+1)}{2k+1} = \tfrac{\pi}{2}\varphi(0).$$
证明用留数定理：被积函数在 $z = 0$ 处留数为 $\varphi(0)$，在 $z = 2k+1$ 处留数为 $2(-1)^{k+1}\varphi(2k+1)/\{\pi(2k+1)\}$。应用：$\varphi(z) = \exp(iz\theta)$（$-\pi/2 < \theta < \pi/2$）时得熟知展开 $\sum_{n=0}^{\infty} (-1)^n\cos(2n+1)\theta/(2n+1) = \pi/4$（$|\theta| < \pi/2$）。

**例 2。**拉马努金考虑 $x/(1+x) + (1/x)/(1+1/x) = 1$，形式地得 $\sum_{n=1}^{\infty} (-1)^{n-1}\{\varphi(n) + \varphi(-n)\} = \varphi(0)$。严格化：设 $\varphi(z)$ 为整函数，存在 $r_n \to \infty$ 使 $I_n \equiv \frac{1}{2\pi i}\int_{|z|=r_n} \frac{\varphi(z)\,dz}{\sin(\pi z)} = o(1)$，则
$$\lim_{N\to\infty} \sum_{\substack{k=-N \\ k\ne 0}}^{N} (-1)^{k-1}\varphi(k) = \varphi(0).$$

**例 3。**拉马努金考虑 $\mathrm{Log}(1+x) - \mathrm{Log}(1+1/x) = \mathrm{Log}\,x$，并注：「若把 $\varphi(n)$ 代入 $x^n$，则须把 $\varphi'(0)$ 代入 $\log_e x$，$\varphi''(0)$ 代入 $(\log_e x)^2$，等等。」形式地得 $\sum_{n=1}^{\infty} (-1)^{n-1}\{\varphi(n) - \varphi(-n)\}/n = \varphi'(0)$。严格化：设 $\varphi(z)$ 为整函数，存在 $r_n \to \infty$ 使 $\frac{1}{2\pi i}\int_{|z|=r_n} \frac{\varphi(z)\,dz}{z\sin(\pi z)} = o(1)$，则
$$\lim_{N\to\infty} \sum_{\substack{k=-N \\ k\ne 0}}^{N} \frac{(-1)^{k-1}\varphi(k)}{k} = \varphi'(0).$$
应用：例 2 取 $\varphi(z) = \sin(z\theta)/z$（$-\pi < \theta < \pi$），或例 3 取 $\varphi(z) = \exp(iz\theta)$（$-\pi < \theta < \pi$），得熟知展开 $\sum_{n=1}^{\infty} (-1)^{n-1}\sin(n\theta)/n = \theta/2$（$|\theta| < \pi$）。

**例 4。**设 $\varphi(z) = \psi(z)/\Gamma(z+1)$ 满足例 3 的假设，则
$$\sum_{k=1}^{\infty} \frac{(-1)^{k-1}\psi(k)}{k!\cdot k} = \gamma\psi(0) + \psi'(0), \qquad (9.1)$$
其中 $\gamma$ 为 Euler 常数。证明：$\varphi(-k) = 0$（$k$ 为正整数），$\Gamma'(1) = -\gamma$（见 (10.7)），故 $\varphi'(0) = \gamma\psi(0) + \psi'(0)$；代入例 3 即得。拉马努金预示其第 6 章的发散级数理论，称 $\gamma$（他记作 $c$）为 $\sum_{k=1}^{\infty} 1/k$ 的「常数」；他在 (9.1) 中并不断言等式，而写左端「近乎」等于右端——他意识到其方法不总给出等式，或许只是某种近似。

**拉马努金的第二段谜语式注记**（在例 3 之前）：「若无穷多项消失，它可能取 $0\times\infty$ 的形式并有确定值。在 $x$ 的函数的情形，此误差是 $e^{-x}$ 的函数，随 $x$ 增大而迅速减小。」Berndt 注：若 $I_n$ 不趋于 0，该方法仍可给出带余项的有限展开，在某些情形下可得渐近展开。

**推论 1。**当 $x \to \infty$ 时
$$\sum_{k=1}^{\infty} \frac{(-1)^{k-1}x^k}{k!\cdot k} \sim \mathrm{Log}\,x + \gamma.$$
证明：由第 3 章第 2 节推论 2，(9.2) $\sum_{k=1}^{\infty} (-1)^{k-1}x^k/(k!\cdot k) = e^{-x}\sum_{k=1}^{\infty} (\sum_{n=1}^{k} 1/n)x^k/k!$；右端由第 3 章第 10 节例 4 或本章第 10 节例 2 第三版知渐近于 $\mathrm{Log}\,x + \gamma$。拉马努金断言两端之差介于 $e^{-x}/x$ 与 $e^{-x}/(1+x)$ 之间——确实正确，证明推迟到第二本笔记第 12 章第 44 节。

**推论 2。**设 $n$ 为正数，则当 $x \to \infty$ 时
$$\sum_{k=1}^{\infty} \frac{(-1)^{k-1}x^{nk}}{k(k!)^n} \sim n\,\mathrm{Log}\,x + n\gamma.$$
**本推论在 $n > 2$ 时不成立**（拉马努金原文错误，Berndt 已否定）：记 $G_n(x) = \sum_{k=0}^{\infty} (-1)^k x^{nk}/(k!)^n$，则 (9.3) $\sum_{k=1}^{\infty} (-1)^{k-1}x^{nk}/(k(k!)^n) = n\int_0^x (1-G_n(t))/t\,dt$；由 (9.3) 与 (10.8) 得 (9.4)，若推论 2 成立则 (9.4) 右端的积分是 $o(1)$；但由 Olver [1, p. 309]，$n \ge 2$ 时 $G_n(x) = \frac{2\exp(xn\cos(\pi/n))}{\sqrt{n}(2\pi x)^{(n-1)/2}}\{\sin(\frac{\pi}{2n} + xn\sin\frac{\pi}{n}) + O(1/x)\}$，故 $n > 2$、$\alpha > 0$ 时 $\lim_{x\to\infty} \int_{\alpha}^{x} G_n(t)/t\,dt$ 不存在，推论 2 不成立。$n = 1$ 时推论 2 即推论 1；$n = 2$ 的情形 Berndt 未断言（见待核对清单）。Berndt 附注：感谢 Emil Grosswald 指出他们原先发表的推论 1 与推论 2 的证明是错的。拉马努金原话：「若 $x$ 变得越来越大，$\sum_{k=1}^{\infty} (-1)^{k-1}x^{nk}/(k(k!)^n) = n\sum_{k=1}^{\infty} (-1)^{k-1}x^k/(k!\cdot k)$」——精确地说，他是断言两级数当 $x\to\infty$ 时渐近于同一函数。

**出处。**Berndt Part I, Ch. 4, §9, pp. 95–100（本节无 Entry 编号）。

**状态。**例 1–3 已证明（在 $I_n = o(1)$ 的严格假设下，留数定理）；例 4 已证明（在例 3 的假设下）；推论 1 已证明（渐近）；**推论 2 在 $n > 2$ 时已否定**，$n = 1$ 时成立，$n = 2$ 未定。数值复核（mpmath，30 位）：例 1 在 $\theta = 0.3$ 时级数和为 $0.785398163397448 = \pi/4$；例 3 在 $\theta = 0.5$ 时级数和为 $0.25 = \theta/2$；推论 1 在 $x = 10$ 时级数和为 $2.87980491486$，$\mathrm{Log}\,10 + \gamma = 2.87980075790$，差 $4.16\times 10^{-6}$，介于 $e^{-10}/11 = 4.13\times 10^{-6}$ 与 $e^{-10}/10 = 4.54\times 10^{-6}$ 之间，与 Berndt 的断言一致。

**对照。**形式代换与留数定理见 M09；发散级数与渐近展开见 M02、M12；Euler 常数 $\gamma$ 见 M01、M12；$\sum (-1)^{n-1}\sin(n\theta)/n = \theta/2$ 见 M02（Fourier 级数）。

## Entry 10——二项系数对称和

**陈述。**设 $n$ 为复数，$\varphi$ 为整函数，存在趋于 $\infty$ 的正数列 $r_j$ 使
$$I_j \equiv \frac{1}{2\pi i}\int_{|z|=r_j} \frac{\pi\varphi(z)\cot(\pi z)\cot\{\pi(z-n)\}}{\Gamma(z+1)\Gamma(n-z+1)}\,dz = o(1),$$
则
$$\sum_{k=0}^{\infty} \binom{n}{k}\varphi(k) = \sum_{k=0}^{\infty} \binom{n}{k}\varphi(n-k),$$
只要每边级数收敛。拉马努金用第 9 节的技巧「证明」本条，出发点是恒等式 $(1+x)^n = x^n(1+1/x)^n$；$n$ 为非负整数时本条是平凡的。证明用留数定理：被积函数在 $z = k$（$k$ 为非负整数）与 $z = n+r$（$r$ 为非正整数）处有单极点，留数分别为 $R_k = -\varphi(k)\cot(\pi n)/\{\Gamma(k+1)\Gamma(n-k+1)\}$ 与 $R_{n+r} = \varphi(n-k)\cot(\pi n)/\{\Gamma(n-k+1)\Gamma(k+1)\}$（$k = -r \ge 0$）。

**推论。**在 Entry 10 的假设下把 $n$ 换成 $r$、$\varphi(z)$ 换成 $x^{r-z}\varphi(z)$（$x > 0$），设 (10.1) $\sum_{k=0}^{\infty} \binom{r}{k}x^{r-k}\varphi(k)$ 在 $\infty$ 附近表一函数 $f$，则 $f(0) = \varphi(r)$。

**例 1。**在推论的假设下取 $r = -1$、$\varphi(z)$ 换成 $\varphi(z+1)$，则 $f(0) = \varphi(0)$。

Berndt 注：推论与例 1 的条件极少满足；(10.1) 常不收敛，而只是 $f$ 的渐近展开，此时推论与例 1 变得含糊——许多函数有同一发散渐近级数。拉马努金称 $f$ 为级数 (10.1) 的「生成函数」（p. 43）。以下例题的表述常含糊、证明一般不严格；书中对每例都给出精确陈述与严格证明。

**例（未编号）。**级数 $\sum_{k=0}^{\infty} (-1)^k/((2k+1)x^{2k+1})$（$|x| > 1$）(10.2) 在 $x \to 0^+$ 时的值为 $\pi/2$：它是 $\tan^{-1}(1/x)$ 的 Maclaurin 级数，$\lim_{x\to 0^+} \tan^{-1}(1/x) = \pi/2$。拉马努金在例 1 中取 $\varphi(z) = \sin(\pi z/2)/z$ 得出此结果。

**例 2（第一版）。**当 $x > 0$ 趋于 $\infty$ 时
$$f(x) \equiv \int_0^{\infty} \frac{e^{-t}}{x+t}\,dt \sim \sum_{k=0}^{\infty} \frac{(-1)^k k!}{x^{k+1}}, \qquad (10.3)$$
且 $\lim_{x\to 0^+} f(x) = \infty$。渐近级数由逐次分部积分得；此结果实为 Euler 首得，详见 Hardy [15, pp. 26–27]。分部积分（另一方式）得 $f(x) = 1/x + \int_0^{\infty} e^{-t}\,\mathrm{Log}(x+t)\,dt$，由此得后一结论。拉马努金在例 1 中取 $\varphi(z) = \Gamma(z)$ 得出此结果。

**例 2（第二版）。**$f$ 如上，$x > 0$ 时
$$f(x) = \frac{1}{x+1} - \frac{1^2}{x+3} - \frac{2^2}{x+5} - \frac{3^2}{x+7} - \cdots,$$
且 $\lim_{x\to 0^+} f(x) = \infty$。连分数展开见 Wall [1, p. 356]；在 $x = 0$ 处取第 $n$ 个渐近分数，按 Wall [1, pp. 17–18] 的标准算法化为级数得 $\frac{1}{1} - \frac{1^2}{3} - \frac{2^2}{5} - \cdots - \frac{(n-1)^2}{2n-1} = \sum_{k=1}^{n} 1/k$，令 $n \to \infty$ 得 $f(0^+) = \infty$。

**例 2（第三版）。**设 $f(x) = e^x\int_x^{\infty} e^{-t}/t\,dt$（$x > 0$），则
$$\sum_{k=1}^{\infty} \frac{\psi(k)x^k}{k!} - e^x(\gamma + \mathrm{Log}\,x) = f(x) \sim \sum_{k=0}^{\infty} \frac{(-1)^k k!}{x^{k+1}}, \qquad (10.4)$$
当 $x \to \infty$ 时，其中 $\psi(k) = \sum_{n\le k} 1/n$，$\gamma$ 为 Euler 常数；且 $f(0^+) = \infty$。证明用第 3 章 Entry 2 推论 2 的 (10.5) $\sum_{k=1}^{\infty} \psi(k)x^k/k! = e^x\sum_{k=1}^{\infty} (-1)^{k-1}x^k/(k!\cdot k)$（$|x| < \infty$）；(10.6) $\sum_{k=1}^{\infty} (-1)^{k-1}x^k/(k!\cdot k) = \int_0^x (1-e^{-t})/t\,dt$；(10.7) $\gamma = -\Gamma'(1) = -\int_0^{\infty} e^{-t}\,\mathrm{Log}\,t\,dt$（见 Gradshteyn–Ryzhik [1, p. 946]）；分部积分得 (10.8) $\gamma = \int_0^1 (1-e^{-t})/t\,dt - \int_1^{\infty} e^{-t}/t\,dt$；综合 (10.5)(10.6)(10.8) 得 $\sum \psi(k)x^k/k! - e^x(\gamma + \mathrm{Log}\,x) = e^x\int_x^{\infty} e^{-t}/t\,dt$，再逐次分部积分得渐近级数。

**例 3。**$\mathrm{Re}\,n > -1$、$x \ge 0$ 时
$$f(x) \equiv \int_0^{\infty} e^{-t}(x+t)^n\,dt \sim \sum_{k=0}^{\infty} \frac{\Gamma(n+1)x^{n-k}}{\Gamma(n-k+1)},$$
当 $x \to \infty$ 时；且 $f(0) = \Gamma(n+1)$。拉马努金在推论中取 $\varphi(z) = \Gamma(z+1)$、$r = n$ 得出 $f(0)$ 的值。证明用 Taylor 定理带余项估计。

**例 4。**$x \ge 0$ 时设 $f(x) = \int_x^{\infty} \sin(t-x)/t\,dt$，则
$$\tfrac{\pi}{2}\cos x + (\gamma + \mathrm{Log}\,x)\sin x - \sum_{k=0}^{\infty} \frac{(-1)^k\psi(2k+1)x^{2k+1}}{(2k+1)!} = f(x) \sim \sum_{k=0}^{\infty} \frac{(-1)^k(2k)!}{x^{2k+1}},$$
当 $x \to \infty$ 时，其中 $\psi$ 如例 2 第三版；且 $f(0) = \pi/2$。拉马努金在例 1 中取 $\varphi(z) = \Gamma(z)\sin(\pi z/2)$ 得出 $f(0)$ 的值。证明：把 (10.5) 中的 $x$ 换成 $ix$ 取虚部得 (10.9)；(10.10) $\sum_{k=0}^{\infty} (-1)^k x^{2k+1}/((2k+1)!(2k+1)) = \int_0^x \sin t/t\,dt$；(10.11) $\sum_{k=1}^{\infty} (-1)^k x^{2k}/((2k)!(2k)) = \int_0^x (\cos t - 1)/t\,dt$；综合并用余弦积分的熟知公式（Gradshteyn–Ryzhik [1, p. 928]）即得。

例题之后拉马努金指出其方法的「优点」：「这样我们能在 $x = 0$ 处求得精确值，尽管生成函数可能太难求出。」

**出处。**Berndt Part I, Ch. 4, Entry 10 与 §10 例题，pp. 100–105。

**状态。**Entry 10 已证明（在 $I_j = o(1)$ 的假设下）；推论与例 1 已证明（条件极少满足，(10.1) 常为发散渐近级数，见 Berndt 的注）；例（未编号）、例 2 三版、例 3、例 4 均已证明（严格陈述见上）。数值复核（mpmath，30 位）：Entry 10 取 $\varphi(k) = k$、$n = 2.5$ 时两边均为 $7.07106781187 = n2^{n-1}$；(10.4) 的左端恒等式由 (10.5)(10.6)(10.8) 的代数推导得，其渐近部分即第 9 节推论 1，已在该节数值复核（$x = 10$ 时差 $4.16\times 10^{-6}$）。

**对照。**二项系数对称和见 M13（组合恒等式）；$\Gamma$ 函数与指数积分见 M10、M09；连分数见 M03；渐近级数见 M12；$\tan^{-1}(1/x)$ 的级数见 M02。

## Entry 11——拉马努金主定理的推广形式

**陈述。**若 $n > 0$，则
$$\int_0^{\infty} x^{n-1} \sum_{k=0}^{\infty} \frac{\varphi(k)(-x)^k}{k!}\,dx = \Gamma(n)\varphi(-n).$$
**推论 1。**若 $n > 0$，则
$$\int_0^{\infty} x^{n-1} \sum_{k=0}^{\infty} \varphi(k)(-x)^k\,dx = \frac{\pi\varphi(-n)}{\sin(\pi n)}.$$
即章首的 (0.1)。
**推论 2。**若 $n > 0$，则
$$\int_0^{\infty} x^{n-1} \sum_{k=0}^{\infty} \frac{\varphi(2k)(-x^2)^k}{(2k)!}\,dx = \Gamma(n)\varphi(-n)\cos\left(\frac{\pi n}{2}\right).$$
**推论 3。**若 $n$ 为实数，则
$$\int_0^{\infty} \sum_{k=0}^{\infty} \frac{\varphi(k)(-x)^k}{k!}\cos(nx)\,dx = \sum_{k=0}^{\infty} \varphi(-2k-1)(-n^2)^k.$$
**推论 4。**若 $n$ 为实数，则
$$\int_0^{\infty} \sum_{k=0}^{\infty} \varphi(2k)(-x^2)^k\cos(nx)\,dx = \frac{\pi}{2}\sum_{k=0}^{\infty} \frac{\varphi(-k-1)(-n)^k}{k!}.$$
**推论 5。**若 $m, n > -1$，则
$$\int_0^1 x^m(1-x)^n\,dx = \frac{\Gamma(m+1)\Gamma(n+1)}{\Gamma(m+n+2)}.$$
即熟知的 Beta 函数 $B(m+1, n+1)$；此例亦见于拉马努金的第一份季报。

**拉马努金的推导（纯形式）。**他先用逐次分部积分与 Entry 10 的例 3（不是他所声称的 Entry 10 推论）得出 $\Gamma(n+1)$ 的熟知积分表示；为证 Entry 11，他考虑 $\sum_{k=0}^{\infty} \frac{f^{(k)}(0)}{k!}\int_0^{\infty} e^{-r^k x}x^{n-1}\,dx = \sum_{k=0}^{\infty} \frac{\Gamma(n)f^{(k)}(0)}{r^{kn}k!}$（$r, n > 0$），交换求和与积分次序，再把 $\exp(-r^k x)$ 展开为 Maclaurin 级数并交换求和次序，得 $\int_0^{\infty} x^{n-1}\sum_{k=0}^{\infty} \frac{f(r^k)(-x)^k}{k!}\,dx = \Gamma(n)f(r^{-n})$；把 $f(r^j)$ 换成 $\varphi(j)$（$j = -n, k$；$0 \le k < \infty$）即完成推导。推论 1 由 Entry 11 取 $\varphi(x) \to \Gamma(x+1)\varphi(x)$ 得；推论 2 由 Entry 11 取 $\varphi(x) \to \varphi(x)\cos(\pi x/2)$ 得；推论 3 把 $\cos(nx)$ 展开为 Maclaurin 级数并交换积分与求和次序、用 Entry 11 得；推论 4 亦见于拉马努金第二份季报的推论 (vii)，证明较难，推迟到季报的讨论。

**Hardy 的评价。**Hardy 在其著作 [20, p. 15] 的导言中引用推论 1，称这一「特别有趣的公式」是拉马努金最喜爱的公式之一；又在第 11 章中详尽讨论 Entry 11 与推论 1、3，对某些函数类 $\varphi$ 确立其有效性。关于拉马努金可能的证明，Hardy 说：「他并未『真正』证明我所引用的任何公式。这是不可能的，因为『自然』条件涉及的思想是他在 1914 年一无所知的，而且直到去世前他几乎都没有吸收。」这些公式的完整证明亦见 Hardy 的论文 [13]、[21, pp. 280–289]。推论 1 在 Riemann zeta 函数上的应用见 H. M. Edwards [1, pp. 218–225]；Hill、Laird 与 Cerone [1] 给出推论 1 的另一形式应用。

**出处。**Berndt Part I, Ch. 4, Entry 11, pp. 105–107。

**状态。**拉马努金的推导是纯形式的；已证明（Hardy [13] 与 Berndt 的严格化，限于适当的函数类）；推论 5（Beta 函数）是经典公式，已证明；推论 4 的证明见季报讨论（待补）。数值复核（mpmath，30 位）：取 $\varphi \equiv 1$ 时 Entry 11 化为 $\int_0^{\infty} x^{n-1}e^{-x}\,dx = \Gamma(n)$，$n = 1/2$ 时两边均为 $1.77245385090552$，$n = 5/2$ 时两边均为 $1.32934038817914$；推论 1 在 $n = 1/2$ 时两边均为 $\pi = 3.14159265358979$，在 $n = 1/3$ 时两边分别为 $3.62759872845738$ 与 $3.62759872846844$（差 $1\times 10^{-11}$，为数值积分误差）。

**对照。**本条是拉马努金主定理的推广形式，见 M09（主定理、Mellin 变换）；$\Gamma$ 函数见 M10；推论 1 的 $\pi/\sin(\pi n)$ 见 M10（反射公式）；推论 5 的 Beta 函数见 M10、M09；zeta 函数的应用见 M01。

## Entry 12——Fourier 余弦变换的反演

**陈述。**若
$$\psi(n) = \int_0^{\infty} \varphi(x)\cos(nx)\,dx,$$
则
$$\text{(i)} \qquad \int_0^{\infty} \psi(x)\cos(nx)\,dx = \tfrac{\pi}{2}\varphi(n)$$
$$\text{(ii)} \qquad \int_0^{\infty} \psi^2(x)\,dx = \tfrac{\pi}{2}\int_0^{\infty} \varphi^2(x)\,dx.$$
第一部分即 Fourier 余弦变换的反演公式；(i)(ii) 成立的充分条件分别见 Titchmarsh [2] 的第 3 章与第 2 章。拉马努金的「证明」推迟到季报的讨论，季报中有 Entry 12 的若干应用。

**出处。**Berndt Part I, Ch. 4, Entry 12, p. 107。

**状态。**已证明（在 Titchmarsh 的充分条件下）。数值复核：取 $\varphi(x) = e^{-x}$，则 $\psi(n) = 1/(1+n^2)$；(i) 在 $n = 1$ 时 $\int_0^{\infty} \cos x/(1+x^2)\,dx = 0.577868 \approx \pi/(2e) = 0.577864$（差 $4\times 10^{-6}$，在 scipy 积分误差估计内；mpmath 的默认积分对振荡被积函数精度不足，见待核对清单）；(ii) 两边均为 $\pi/4 = 0.7853981633974483$。

**对照。**Fourier 余弦变换见 M09；Plancherel 型恒等式 (ii) 见 M09、M12。

## Entry 13(i)(ii)——三角函数的 Beta 型积分

**陈述。**
**Entry 13(i)。**若 $m, n > -1$，则
$$\int_0^{\pi/2} \sin^m x\cos^n x\,dx = \frac{\Gamma\left(\frac{m+1}{2}\right)\Gamma\left(\frac{n+1}{2}\right)}{2\Gamma\left(\frac{m+n}{2}+1\right)}.$$
此为熟知结果，是 Entry 11 推论 5 的直接推论。
**Entry 13(ii)。**若 $m > -1$ 且 $n$ 为任意复数，则
$$\int_0^{\pi/2} \cos^m x\cos nx\,dx = \frac{\pi\Gamma(m+1)}{2^{m+1}\Gamma\left(\frac{m+n}{2}+1\right)\Gamma\left(\frac{m-n}{2}+1\right)}.$$
亦为熟知公式；最简单的证明之一见 Whittaker–Watson [1, exercise 39, p. 263]。

**出处。**Berndt Part I, Ch. 4, Entry 13, p. 107。Entry 13(ii) 亦见于第一本笔记 p. 182（Entry 11 的 13 个应用之一）。

**状态。**已证明（经典公式）。数值复核（mpmath，30 位）：13(i) 在 $m = 2$、$n = 3$ 时两边均为 $2/15 = 0.133333333333333$；13(ii) 在 $m = 2$、$n = 0$ 与 $m = 1$、$n = 1$ 时两边均为 $\pi/4 = 0.785398163397448$。

**对照。**Beta 函数与 Gamma 函数见 M10；三角积分见 M09。

## Entry 14——$\prod (1 + x^6/n^6)$ 的闭式

**陈述。**若 $x$ 为任意复数，则
$$\prod_{n=1}^{\infty} \left(1 + \frac{x^6}{n^6}\right) = \frac{\sinh(2\pi x) - 2\sinh(\pi x)\cos(\pi x\sqrt{3})}{4\pi^3 x^3}.$$
证明：令 $\omega = \exp(2\pi i/3)$，用 $\sinh x$ 的熟知乘积表示得 $\prod_{n=1}^{\infty} (1 + x^6/n^6) = \sinh(\pi x)\sinh(\pi x\omega)\sinh(\pi x\omega^2)/(\pi^3 x^3)$；展开即得。

**出处。**Berndt Part I, Ch. 4, Entry 14, pp. 107–108。

**状态。**已证明。数值复核（mpmath，30 位）：$x = 1$ 时两边均为 $2.03474083500943$；$x = 0.5$ 时两边均为 $1.01590022627052$。

**对照。**无穷乘积与 $\sinh$ 的乘积表示见 M02、M06（Weierstrass 乘积）；$\omega = e^{2\pi i/3}$ 的单位根技巧见 M14。

## Entry 15——奇数倒数和 $G_k$

**陈述。**对每个正整数 $k$，令 $G_k = \sum_{0\le 2n+1\le k} 1/(2n+1)$（即不超过 $k$ 的奇数的倒数和）。则对一切复数 $x$，
$$e^x \sum_{k=1}^{\infty} \frac{(-2)^{k-1}x^k}{k!\cdot k} = \sum_{k=1}^{\infty} \frac{G_k x^k}{k!}. \qquad (15.1)$$
证明：(15.2) $I \equiv e^x\int_0^1 (1-e^{-2xz})/(2z)\,dz = e^x\sum_{k=1}^{\infty} (-2)^{k-1}x^k/(k!\cdot k)$；(15.3) $I = \int_0^1 (e^x - e^{x(1-2z)})/(2z)\,dz = \sum_{k=1}^{\infty} G_k x^k/k!$（其中 $\int_0^1 (1-(1-2z)^k)/(2z)\,dz = \frac12\sum_{k} \cdots$ 化为 $\sum_{0\le 2j\le k-1} \int_0^1 t^{2j}\,dt$）；综合 (15.2)(15.3) 即得 (15.1)。

比较 (15.1) 两边 $x^n$ 的系数得
$$\sum_{k=1}^{n} \binom{n}{k}\frac{(-2)^{k-1}}{k} = G_n, \qquad n \ge 1.$$

**出处。**Berndt Part I, Ch. 4, Entry 15, p. 108。

**状态。**已证明。数值复核：系数恒等式在 $n = 1,\dots,8$ 时精确成立（$G_1 = 1$、$G_2 = 1$、$G_3 = 4/3$、$G_4 = 4/3$、$G_5 = 23/15$、$G_6 = 23/15$、$G_7 = 176/105$、$G_8 = 176/105$）；(15.1) 在 $x = 0.5$ 时两边均为 $0.656685351796125$（15 位）。

**对照。**奇数倒数和与调和数见 M01；指数生成函数见 M13；二项系数恒等式见 M13。

## 小结

- 本章 14 条 Entry 全部收录完毕（Entry 1–8、Entry 10–15；编号均在原文明确出现；**第 9 节无 Entry 9**，只有例题 1–4 与推论 1–2）。前半（Entry 1–8）是指数函数迭代的系统理论：$F_r(x)$ 的定义与两类系数 $\varphi_k(r)$、$f_k(x)$（Entry 1–2）、Bernoulli 展开（Entry 3）、$\psi_k(n)$ 的递推与显式公式（Entry 4、Entry 6）、$f_1$ 的函数方程（Entry 5）、$F_{2r}$ 的展开（Entry 7）、调和数幂和（Entry 8）。后半（第 9 节与 Entry 10–15）是拉马努金的形式技巧及其严格化：留数定理重证的三个例题（§9）、二项对称和与指数积分（Entry 10）、主定理推广形式（Entry 11 为本章中心）、Fourier 余弦反演（Entry 12）、Beta 型积分（Entry 13）、无穷乘积（Entry 14）、奇数倒数和（Entry 15）。
- 本章发现的拉马努金原文疏失（均已在各条注明）：第 6 节末拉马努金无意中暗示 $f_1(x)$ 是 7 次多项式（实为无穷级数）；第 9 节推论 2 在 $n > 2$ 时不成立（Berndt 用 Olver 的 $G_n(x)$ 渐近否定；并附注他们原先发表的推论 1、2 的证明也是错的）；Entry 11 的推导是纯形式的，Hardy 指出拉马努金并未真正证明（自然条件涉及他 1914 年尚不知道的概念）；Entry 10 的推论与例 1 的条件极少满足，(10.1) 常为发散渐近级数。
- 本轮 OCR 误读纠正（均经 PDF 原图或数值复核证实）：本章 DjVu OCR 的公式部分损坏严重，全部公式均按 PDF 原图（150 DPI）逐字转录；其中较关键的纠正有：(1.2) 的 $\varphi_k(r)$、$f_k(x)$ 记号；Entry 3 的陈述 $f_1'(x) = x + \sum B_n f_n(x)$；(4.3) 的 $(\tfrac12 x)^n$ 因子；Entry 6(ii) 的 $\varphi_3(2r) = r^2 - \tfrac16 r$ 与 $\varphi_6(2r)$、$\varphi_7(2r)$ 的各系数；(7.1) 的三项系数 $1/6$、$1/72$；Entry 8(iii) 的 $\tfrac32$ 系数；第 9 节例 3 的分母 $n$ 与 $\varphi'(0)$；Entry 10 的被积函数与二项系数恒等式；Entry 11 推论 2 的 $\cos(\pi n/2)$；Entry 13(ii) 分母的 $2^{m+1}$；Entry 14 分子的 $\sinh(2\pi x) - 2\sinh(\pi x)\cos(\pi x\sqrt{3})$；Entry 15 的 $G_k$ 定义（奇数倒数和）与 $(-2)^{k-1}$。另：第 9 节证明文字中的 $\psi_1(n)$、$\psi_2(n)$ 在 OCR 中被读成 $w_r(n)$、$v_r(n)$，已按原图纠正。
- 数值复核小计：本轮共复核约 70 项（mpmath 30 位 + 精确分数），见各条「数值复核」：$\psi_k(1)$ 表值与 $\psi_3$ 交叉验证 7 项、(6.1)(6.2)（$n = 1,\dots,6$）12 项、$\varphi_n(2r)$ 七式（$r = 1,2,3$）21 项、(2.2)（$n = 3,4$）2 项、Entry 3（$x = 0.1$）、Entry 7（$r = 1$、$x = 0.1$）、Entry 8（$x = 5,10$）6 项、§9 例 1、例 3、推论 1（$x = 10$）、Entry 10（$\varphi(k) = k$、$n = 2.5$）、Entry 11 与推论 1（$\varphi \equiv 1$）4 项、Entry 12（$\varphi = e^{-x}$）2 项、Entry 13(i)(ii) 3 项、Entry 14（$x = 1, 0.5$）2 项、Entry 15（系数恒等式 $n = 1,\dots,8$ 与 (15.1) 在 $x = 0.5$）9 项。
- 与 M 模块的对照：迭代与 Bell 数主线见 M13（Bell 数、Dobiński 公式、指数生成函数、二项卷积）；形式幂级数与发散级数见 M02（$e^x - 1$、$\mathrm{Log}(1+x)$ 的级数、Fourier 级数、无穷乘积）；Bernoulli 数与调和数见 M01（Entry 3 的 $B_n$、Entry 8 的 $H_n$、Entry 15 的 $G_k$，注意 M01 伯努利数定义缺口仍待补）；渐近展开见 M12（无穷幂塔、Entry 7、Entry 10 的渐近级数、§9 推论 1–2）；积分与变换见 M09（留数定理、Mellin 变换、Fourier 余弦变换、拉马努金主定理）；Gamma/Beta 函数见 M10（Entry 11 的 $\Gamma(n)$、推论 5 的 Beta 函数、Entry 13）；无穷乘积与单位根见 M06、M14（Entry 14）。

## 待核对清单

1. 本章没有 Entry 9：已按原文确认（第 9 节只含例题 1–4 与推论 1–2，无 Entry 编号）；IMSC 整理表计本章的结果数本次未能读取（imsc.res.in 当日不可达），待该表可达后补。
2. 第 9 节推论 2 在 $n = 2$ 时是否成立：Berndt 只否定 $n > 2$ 的情形，$n = 2$ 未断言；按 Olver 的渐近，$n = 2$ 时 $G_2(x)$ 的振幅按 $x^{-1/2}$ 衰减，(9.4) 的积分是否趋于 0 需另行核对。
3. Entry 11 推论 4 的证明：Berndt 推迟到季报的讨论（该推论亦为第二份季报的推论 (vii)），本文件只记陈述与 Hardy 的讨论，未展开证明。
4. Entry 12 拉马努金的「证明」：Berndt 推迟到季报的讨论（季报中有 Entry 12 的若干应用），本文件只记 Titchmarsh 的充分条件，未展开。
5. Entry 12(i) 的数值复核：mpmath 默认积分对 $\int_0^{\infty} \cos x/(1+x^2)\,dx$ 给出 $0.575861$，与真值 $\pi/(2e) = 0.577864$ 差 $0.002$；scipy 积分为 $0.577868$（差 $4\times 10^{-6}$，在误差估计内）。振荡积分的数值复核宜用分段或专用方法，本条已按 scipy 结果记录。
6. Entry 7 的 (7.1)：Berndt 只验证前三项与 (7.2) 一致，「$\cdots$」的余项未展开；第四项起的系数未逐项核对。
7. $\psi_7(1) = -11/120960$：由 Entry 4 推论 2 的递推导出，书中 $f_1(x)$ 的级数只列到 $x^7$，此值不在原文中；推论 2 在 $n = 2,\dots,6$ 时与书中系数逐项一致，递推本身可信，但 $\psi_7(1)$ 仍标为「导出值」，待与 Comtet 或其他文献核对。
8. 本章 TIFR 影印版（第二本笔记第 4 章）的具体页码未标：Berndt 原书未逐条给出 TIFR 页码，待查 TIFR 1957 年版目录后补；目前只知两条线索——拉马努金称 $f$ 为级数 (10.1) 的「生成函数」（p. 43），以及 Entry 11 见于第一本笔记 p. 182、其 13 个应用见第一本笔记 pp. 180、182、184。
9. Entry 10 的 (10.9)–(10.11) 逐项系数已按 PDF 原图 (p. 104) 记录，未逐项数值复核（(10.4) 的恒等部分由 (10.5)(10.6)(10.8) 的代数推导保证）。

## 来源说明

- 底本：Bruce C. Berndt, *Ramanujan's Notebooks*, Part I, Springer, 1985, Ch. 4, pp. 85–108。archive.org 全文（`ramanujan_notebooks_i`）：DjVu OCR 文本（563,342 字节）与 PDF（13,201,802 字节，368 叶；**PDF 页 = 书页 + 10**，如书 p. 85 = PDF p. 95）。
- 核对方法：本章 24 页（书 pp. 85–108）均渲染成 150 DPI 图片逐字读过；DjVu OCR 的公式部分损坏严重，全部公式均按 PDF 原图转录，OCR 凡与图片或数值不符者一律纠正并注明；数值复核用 Python + mpmath（30 位）与精确分数（Fraction），本章共复核约 70 项，见各条「数值复核」。
- IMSC 整理表计本章的结果数本次未能读取（imsc.res.in 当日不可达），待补；该数为 IMSC 表的计数，Berndt 原书未逐章公布条目数。
- 本文件只收公式陈述与自写导读/证明思路，不照抄 Berndt 的正文与证明。
