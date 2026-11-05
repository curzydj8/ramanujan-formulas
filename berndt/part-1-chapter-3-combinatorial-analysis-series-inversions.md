# Part I · 第 3 章 Combinatorial Analysis and Series Inversions（组合分析与级数反演）

出处：Bruce C. Berndt, *Ramanujan's Notebooks*, Part I, Springer, 1985, 第 3 章，pp. 44–84（第 2 章 pp. 25–43；第 4 章起自 p. 85）。对应拉马努金**第二本笔记第 3 章**。

## 背景与记号

- 章首导言说：本章虽未提及任何组合问题，但大部分内容属于组合分析的范畴；另一主题是各种级数展开。**Entry 10 是本章最深、最有趣的结果**，它把两个主题分开，但与前者也有联系；它给出一大类幂级数的通用渐近展开。拉马努金对部分结果只给了极简略的证明提纲，包括 Entry 10。
- 本章部分结果可追溯到 Lambert、Lagrange、Euler、Rothe、Abel 等人；另一方面，拉马努金的许多工作曾被他人在不知情的情况下重新发现：单变量 Bell 多项式直到 1933 年 Touchard 与 1934 年 E. T. Bell 才在印刷品中被系统研究，而拉马努金在本章已发现其众多性质；H. W. Gould 在 1950 年代末至 1960 年代初重新发现并大幅推广了若干结果。
- **前 9 节共 45 个公式**（导言原话），多数涉及 Bell 数与单变量 Bell 多项式，不难证明。
- Entry 10：拉马努金提出渐近展开并给出形式论证的提纲，但论证不严谨；他给出**三个**应用，但三个应用都不满足其形式论证所隐含的假设。Berndt 在远弱的假设下重证该公式。注意：导言称「三个应用」，而书中 Entry 10 之下列出例 1–4（例 4 是否拉马努金原有，见末尾待核对清单）。
- 第 11–17 节的主题是把 $x$ 的幂表成级数，其中 $x$ 是某个方程的根；源头是 Lambert、Lagrange、Euler 的工作，可由 Lagrange 反演定理导出（该定理见 Carr 的书；拉马努金的 quarterly reports 表明他熟知 Lagrange 定理，但他另有一种巧妙的新方法）。**Entry 13 是中心**；Entry 15 的例 1 极有趣；Entry 16、Entry 17 在文献中未见展开，似可成为进一步研究的基础。
- 本章在原文中明确出现编号的 Entry 共 **17 条**（Entry 1–17），另有推论（Corollary）、例题（Example）与若干未编号的定理（§13 的一般定理）。IMSC 的整理表计本章 **86 条结果**（含 Entry、推论与例题；第 1 章为 43 条，第 2 章为 68 条）——该数为 IMSC 表的计数，Berndt 原书未逐章公布条目数。
- **本章首个拉马努金原文错误**见第 8 节例 4（Berndt 已纠正）；另有 Entry 9 例 (iii)(iv) 两处、Entry 15 例 1 的断言范围、Entry 17 (17.5) 的末项，详见各条与末尾小结。

## 本章结构

| Entry | 页 | 内容 |
|---|---|---|
| Entry 1 | 45 | 对角求和恒等式；推论 1（$(1+xz)^n$）、推论 2 |
| Entry 2 | 46–47 | $\varphi(z)$ 的逆阶乘级数 (2.1)；推论 1、推论 2；(2.3) |
| Entry 3 | 47 | $\psi(z)$ 的第二渐近展开 (3.4)；证明推迟到第 8 节例 1 |
| Entry 4 | 47 | $e^{x(e^a-1)}$ 的展开 (4.1) |
| Entry 5 | 48 | $f_n(x)$ 的递推 (5.1) 与生成函数 (5.2) |
| Entry 6 | 49 | $\sum \varphi_k(n)/(r-k)! = r^n/(r-1)!$ |
| Entry 7 | 49 | $r!\varphi_{r+1}(n)$ 的容斥公式 |
| Entry 8 | 49–50 | $\varphi_r(n)$ 的 Stirling 递推；推论：$f_0,\dots,f_6$ 显式多项式 |
| §8 例 1–6 | 50–53 | $\psi(z)$ 的一般渐近展开；Bell 数 $A_n$、$C_n$；Bernoulli 数记号 |
| Entry 9 | 53–57 | $F_n(a,b;x)$ 的推广 (i)–(vii)；例 (i)–(iv) |
| Entry 10 | 57–66 | 通用渐近展开 (10.3)；4 引理；例 1–4 |
| Entry 11 | 66 | $p_n$ 的递推 (11.2)；推论：Newton 恒等式 |
| (12.1) | 66 | $F_r(n)$ 的定义与收敛条件 |
| Entry 12 | 67 | $F_{r+1}(n)$ 的递推 |
| §13 定理与推论 | 67–69 | Abel 型卷积 (13.1)；Gould 多项式 |
| Entry 13 | 69–70 | $x = a\log x$ 的根与 $x^n = f(n)$；推论 (13.8) |
| Entry 14 | 70–72 | $aqx^p - x^q + 1 = 0$ 的根与 $\varphi(n) = x^n$；推论 1、推论 2 |
| Entry 15 | 73–76 | $u - \log u = 1 + x^2/2$；例 1（$2^m$ 的级数，$0 < n \le 2$）、例 2 |
| Entry 16 | 78–81 | $\varphi_r(n)$ 的递推 (16.2) 与 $\psi_k(r,n)$；推论 1、推论 2 |
| Entry 17 | 81–83 | $A_r$ 的递推 (17.5)；$A_1,\dots,A_7$；例 1、例 2 |

## Entry 1——对角求和恒等式

**陈述。**设 $f(z)$ 在 $|z| < R_1$（$R_1 > 1$）解析，$g(z) = \sum Q_k z^k$ 在 $|z| < R_2$（$R_2 > 0$）解析，且 $\sum P_k z^k = e^z g(z)$。若 $\sum_j Q_j \sum_k f^{(j+k)}(0)/k!$ 收敛且可按对角线 $j+k=n$ 求和，则
$$\sum_{n=0}^{\infty} P_n f^{(n)}(0) = \sum_{n=0}^{\infty} Q_n f^{(n)}(1)$$

**推论 1。**取 $f(z) = (1+xz)^n$（$|x| < 1$，$n$ 任意），$f^{(k)}(0) = \Gamma(n+1)x^k/\Gamma(n-k+1)$，$f^{(k)}(1) = \Gamma(n+1)x^k(1+x)^{n-k}/\Gamma(n-k+1)$，得
$$\sum_{k=0}^{\infty} \frac{P_k x^k}{\Gamma(n-k+1)} = \sum_{k=0}^{\infty} \frac{Q_k x^k (1+x)^{n-k}}{\Gamma(n-k+1)}$$

**推论 2。**只是 Entry 1 的另一表述，书中未展开。

**出处。**Berndt Part I, Ch. 3, Entry 1, p. 45。

**状态。**已证明（Berndt 给出证明；对角求和的收敛条件已在陈述中明示）。

**对照。**对角求和与级数重排的思想见 M02（无穷级数）；$e^z g(z)$ 的系数关系见 M13（组合恒等式）。

## Entry 2——$\varphi(z)$ 的逆阶乘级数

**陈述。**定义
$$\varphi(z) = \sum_{k=1}^{\infty} \frac{x^k}{(z+k-1)(k-1)!}$$
则 (2.1)
$$\varphi(z) = e^x \sum_{k=1}^{\infty} \frac{(-1)^{k-1}x^k}{z(z+1)\cdots(z+k-1)}$$

证明思路（书中给出两种）：其一，$\varphi(z) = x^{1-z}\sum_{k=0}^{\infty} x^{z+k}/((z+k)k!) = x^{1-z}\int_0^x t^{z-1}e^t\,dt$，分部积分无穷次得 (2.1)；其二，递推 $z\varphi(z) + x\varphi(z+1) = xe^x$，且 (2.2)
$$\varphi(z) - e^x\sum_{k=1}^{n} \frac{(-1)^{k-1}x^k}{z(z+1)\cdots(z+k-1)} = \frac{(-1)^n x^n \varphi(z+n)}{z(z+1)\cdots(z+n-1)}$$
右端当 $n \to \infty$ 时趋于 0。

**推论 1。**
$$\sum_{k=0}^{\infty} \frac{f^{(k)}(0)}{(z+k)k!} = \sum_{k=0}^{\infty} \frac{(-1)^k f^{(k)}(1)}{z(z+1)\cdots(z+k)}$$

**推论 2。**
$$\sum_{k=1}^{\infty} \frac{(1+1/2+\cdots+1/k)x^k}{k!} = e^x \sum_{k=1}^{\infty} \frac{(-1)^{k-1}x^k}{k!\cdot k}$$

另 (2.3)（p. 47）：
$$\sum_{k=1}^{\infty} \frac{x^k}{(z+1)\cdots(z+k)} = e^x \sum_{k=1}^{\infty} \frac{(-1)^{k-1}x^k}{(z+k)(k-1)!}$$

**出处。**Berndt Part I, Ch. 3, Entry 2, pp. 46–47。

**状态。**已证明。数值复核（mpmath，30 位）：(2.1) 在 $x=1$、$z=10$ 时两边均为 $0.24903$；递推 $z\varphi(z)+x\varphi(z+1)=xe^x$ 两边均为 $e$；推论 2 在 $x=1$ 时两边约 $2.1654$。

**对照。**逆阶乘级数与调和数见 M02；积分表示见 M09；$\varphi(z)$ 的渐近行为是 Entry 3 的主题。

## Entry 3——$\psi(z)$ 的第二渐近展开

**陈述。**(3.1)
$$\psi(z) = \sum_{k=1}^{\infty} \frac{(-1)^{k-1}x^k}{(z+1)(z+2)\cdots(z+k)}, \qquad x \ne 0$$
$\psi(z)$ 在 $z = -k$（$1 \le k < \infty$）有单极点，在 $\infty$ 处有本性奇点；这是一个逆阶乘级数，收敛横坐标为 $-\infty$，在区域 $R_\varepsilon$ 内亦表渐近展开。(3.2)
$$R_\varepsilon = \{z: -\pi+\varepsilon \le \arg z \le \pi-\varepsilon\}, \qquad \varepsilon > 0$$
(3.3) 定义 $f_{-1}(x) \equiv 1$，且
$$e^x f_n(x) = \sum_{k=1}^{\infty} \frac{k^n x^k}{(k-1)!}, \qquad n \ge 0$$
则 (3.4)：当 $z \to \infty$（在 $R_\varepsilon$ 内）时
$$\psi(z) \sim \sum_{k=1}^{\infty} \frac{(-1)^{k-1}f_{k-1}(x)}{z^k}$$
该级数对一切 $x \ne 0$、$z$ 均发散。

**出处。**Berndt Part I, Ch. 3, Entry 3, p. 47。证明推迟到第 8 节例 1（Entry 3 是该例的特例）。

**状态。**已证明（见第 8 节例 1）。数值复核：$x=1$、$z=10$ 时级数部分和 $0.08386$，$\psi(10) = 0.083876$。

**对照。**渐近展开与发散级数见 M12；逆阶乘级数见 M02；$f_n(x)$ 是单变量 Bell 多项式，见 M13。

**记号说明。**OCR 底本把 (3.1) 的 $\psi$ 误读为 $\varphi$；已按 PDF 原图纠正——本章 $\varphi(z)$（Entry 2）与 $\psi(z)$（Entry 3）是两个不同的函数。

## Entry 4——$e^{x(e^a-1)}$ 的展开

**陈述。**(4.1)
$$e^{x(e^a-1)} = \sum_{n=0}^{\infty} \frac{a^n}{n!}\, f_{n-1}(x), \qquad a, x \text{ 任意复数}$$
其中 $f_{-1}(x) \equiv 1$（见 (3.3)）。

**出处。**Berndt Part I, Ch. 3, Entry 4, p. 47。

**状态。**已证明。代数验算通过：左端 $= e^{-x}e^{xe^a} = e^{-x}\sum_{n=0}^{\infty} (xe^a)^n/n!$，与右端逐项对照一致（注意 $n=0$ 项 $f_{-1} \equiv 1$ 抵消 $e^{-x}$ 的余项）。

**对照。**指数生成函数见 M13；$e^{x(e^a-1)}$ 是 Bell 多项式的双变量生成函数，见 Entry 5 的 (5.2)。

## Entry 5——$f_n(x)$ 的递推

**陈述。**(5.1)
$$f_n(x) = x\sum_{k=0}^{n} \binom{n}{k} f_{k-1}(x), \qquad n \ge 0$$
(5.2)
$$\sum_{n=0}^{\infty} \frac{a^n}{n!} f_n(x) = xe^a e^{x(e^a-1)}$$
由此 $f_n(x)$ 是 $n+1$ 次整系数多项式；$n \ge 0$ 时 $f_n(0) = 0$。

**出处。**Berndt Part I, Ch. 3, Entry 5, p. 48。

**状态。**已证明。数值复核：(5.1) 在 $n=2$ 时，右端 $x[f_{-1} + 2f_0 + f_1] = x[1 + 2x + (x+x^2)] = x+3x^2+x^3 = f_2(x)$。

**对照。**Bell 多项式的递推与生成函数见 M13；二项卷积见 M02。

## 第 6 节——单变量 Bell 多项式与 Stirling 数

**陈述。**(6.1)
$$f_n(x) = \sum_{k=1}^{n+1} \varphi_k(n)x^k$$
定义整数 $\varphi_1(n), \dots, \varphi_{n+1}(n)$。$f_n(x)$ 即今称**单变量 Bell 多项式**，常用记号 $\varphi_n(x) = f_{n-1}(x)$（$n \ge 0$）；系数 $\varphi_k(n)$ 是**第二类 Stirling 数**，今记号 $\varphi_k(n) = S(n+1,k)$。Touchard 1933 年、Bell 1934 年才系统研究；早期见 Bromwich 的书 p. 195。

## Entry 6

**陈述。**(6.2) $e^x \sum_{k=1}^{n+1} \varphi_k(n)x^k = \sum_{k=1}^{\infty} k^n x^k/(k-1)!$；比较 $x^r$ 的系数得
$$\sum_{k=1}^{r} \frac{\varphi_k(n)}{(r-k)!} = \frac{r^n}{(r-1)!}, \qquad n \ge 0,\ 1 \le r \le n+1$$

**出处。**Berndt Part I, Ch. 3, Entry 6, p. 49。

**状态。**已证明。数值复核：$r=2$、$n=3$ 时左端 $1 + 7 = 8 = 2^3$。

**对照。**第二类 Stirling 数的求和恒等式见 M13。

## Entry 7

**陈述。**
$$r!\,\varphi_{r+1}(n) = \sum_{k=0}^{r} (-1)^k \binom{r}{k}(r+1-k)^n, \qquad r, n \ge 0,\ r \le n$$

**出处。**Berndt Part I, Ch. 3, Entry 7, p. 49。

**状态。**已证明。数值复核：$r=1$、$n=3$ 时右端 $8-1 = 7 = \varphi_2(3)$。

**对照。**Stirling 数的容斥公式见 M13（与 $S(n,k) = (1/k!)\sum (-1)^j \binom{k}{j}(k-j)^n$ 同型）。

## Entry 8——Stirling 递推

**陈述。**
$$\varphi_r(n+1) = r\varphi_r(n) + \varphi_{r-1}(n), \qquad 1 \le r \le n+1,\ \varphi_0(n) = 0$$

**出处。**Berndt Part I, Ch. 3, Entry 8, p. 49。

**状态。**已证明（即第二类 Stirling 数的标准递推 $S(n+2,r) = rS(n+1,r) + S(n+1,r-1)$）。

**对照。**见 M13（Stirling 数）。

**推论（p. 50，$f_n(x)$ 的前 7 个，逐字核对）。**
$$f_0(x) = x;\quad f_1(x) = x+x^2;\quad f_2(x) = x+3x^2+x^3;\quad f_3(x) = x+7x^2+6x^3+x^4$$
$$f_4(x) = x+15x^2+25x^3+10x^4+x^5;\quad f_5(x) = x+31x^2+90x^3+65x^4+15x^5+x^6$$
$$f_6(x) = x+63x^2+301x^3+350x^4+140x^5+21x^6+x^7$$

## 第 8 节 例 1——$\psi(z)$ 的一般渐近展开

**陈述。**设 $\psi(z) = \sum_{k=1}^{\infty} (-1)^{k-1}a_k/((z+1)\cdots(z+k))$，收敛横坐标 $\lambda < \infty$；记 $F(j) = \sum_{k=1}^{j+1} a_k\varphi_k(j)$。$\lambda = -\infty$ 时 $R_\varepsilon$ 如 (3.2)，$\lambda$ 有限时 $R_\varepsilon = \{z: -\pi/2+\varepsilon \le \arg(z-\lambda) \le \pi/2-\varepsilon\}$；则当 $z \to \infty$（在 $R_\varepsilon$ 内）时
$$\psi(z) \sim \sum_{k=0}^{\infty} \frac{(-1)^k F(k)}{z^{k+1}}$$
证明用 Abramowitz–Stegun 24.1.4B 的 Stirling 数生成函数。Entry 3 是本例的特例（取 $a_k = x^k$）。

**出处。**Berndt Part I, Ch. 3, §8 例 1, p. 50。

**状态。**已证明。

**对照。**渐近展开见 M12；逆阶乘级数见 M02。

## 第 8 节 例 2——$e^x(e^x-1)^r$ 的系数

**陈述。**$0 \le r \le n$ 时，$r!\,\varphi_{r+1}(n)$ 是 $e^x(e^x-1)^r$ 的 Maclaurin 级数中 $x^n/n!$ 的系数。

**出处。**Berndt Part I, Ch. 3, §8 例 2, p. 51。

**状态。**已证明（熟知结果；与 Entry 7 的容斥公式等价）。

**对照。**指数生成函数见 M13。

## 第 8 节 例 3——$f_{n-1}$ 的导数

**陈述。**$n$ 为正整数时
$$f'_{n-1}(x) = \sum_{k=0}^{n-1} \binom{n}{k} f_{k-1}(x)$$

**出处。**Berndt Part I, Ch. 3, §8 例 3, p. 51。

**状态。**已证明（熟知结果）。数值复核：$n=2$ 时左端 $f'_1(x) = 1+2x$，右端 $\binom{2}{0}f_{-1} + \binom{2}{1}f_0 = 1+2x$。

**对照。**见 M13。

## Bernoulli 数记号（p. 51，重要）

拉马努金用 (8.2)
$$\frac{x}{e^x-1} = 1 - \frac{1}{2}x + \sum_{n=1}^{\infty} \frac{(-1)^{n-1}B_{2n}}{(2n)!}x^{2n}, \qquad |x| < 2\pi$$
定义 Bernoulli 数；当今通用定义为导言 (I1) 式 $x/(e^x-1) = \sum B_n x^n/n!$。**Berndt 全书采用今通用定义**，以下各条的 $B_n$ 均指今通用定义。注意：M01 的伯努利数定义缺口（M02/M06 引用伯努利数并写「见 M01.3」，但 M01 全文未给定义）仍待补，见本仓库 M01 缺口备忘。

## 第 8 节 例 4——$f_n$ 的积分

**陈述。**$n \ge -1$ 时
$$\int_0^x f_n(t)\,dt = \sum_{k=0}^{n+1} \binom{n+1}{k} \frac{B_{n+1-k}f_k(x)}{k+1}$$
其中 $B$ 为今通用 Bernoulli 数。

**拉马努金原文表述有误**：右端须把 $n$ 换成 $n+1$（下标后缀除外），Berndt 已纠正。这是本章首个拉马努金原文错误。

**出处。**Berndt Part I, Ch. 3, §8 例 4, pp. 51–52。

**状态。**已证明（纠正后的形式）。数值复核：$n=0$ 时左端 $x^2/2$，右端 $B_1 f_0(x) + B_0 f_1(x)/2 = -x/2 + (x+x^2)/2 = x^2/2$；$n=1$ 时左端 $x^2/2 + x^3/3$，右端 $x/6 - (x+x^2)/2 + (x+3x^2+x^3)/3$ 亦同。

**对照。**Bernoulli 数与 Euler–Maclaurin 公式见 M01/M12；$f_n$ 的积分见 M09。

## 第 8 节 例 5(i)——Bell 数 $A_n$

**陈述。**(8.4)(8.5)
$$eA_n = ef_n(1) = \sum_{k=1}^{\infty} \frac{k^n}{(k-1)!};\qquad \Delta^n A_0 = A_{n-1}\ (n \ge 1)$$
$$A_0 = 1,\ A_1 = 2,\ A_2 = 5,\ A_3 = 15,\ A_4 = 52,\ A_5 = 203,\ A_6 = 877,\ A_7 = 4140,\ A_8 = 21147$$
$A_n$ 即 Bell 数，第 $n$ 个 Bell 数 $B(n) = A_{n-1}$（$n \ge 1$），组合意义是 $n$ 元集的分拆数；$A_n$ 为偶数当且仅当 $n \equiv 1 \pmod 3$，余为奇数。

历史：Dobiński 1877 年用 (8.4) 算出 $B(1),\dots,B(8)$；Cesàro 1885 年发现 (8.5)；最早明确出现是 Kramp 1796 年的论文，Tate 1845 年的专著亦有；最早的应用是 17 世纪《源氏物语》版本中的线香排列数；Browne 指出它是 $n$ 行诗节的押韵方式数；(8.4) 曾作 1868 年《Matematicheskii Sbornik》的习题；Hardy 的书 p. 424、Bromwich 的书 p. 197 亦有；Levine–Dalton 算出前 74 个 Bell 数；Epstein 得出渐近公式。

**出处。**Berndt Part I, Ch. 3, §8 例 5(i), p. 52。

**状态。**已证明。数值复核：(8.5) 在 $n=1,2,3$ 时成立（$\Delta A_0 = 1$、$\Delta^2 A_0 = 2$、$\Delta^3 A_0 = 5$）；$A_n$ 的奇偶规律在 $n \le 8$ 逐项成立。

**对照。**Bell 数、Dobiński 公式见 M13；(8.4) 的级数形式见 M02。

## 第 8 节 例 5(ii)——$C_n = f_n(-1)$

**陈述。**
$$\frac{C_n}{e} = \sum_{k=1}^{\infty} \frac{(-1)^k k^n}{(k-1)!};\qquad C_0 = -1,\ C_1 = 0,\ C_2 = C_3 = 1,\ C_4 = -2,\ C_5 = C_6 = -9,\ C_7 = 50,\ C_8 = 267$$
$C_n = f_n(-1)$；$\Delta^n C_0 = -C_{n-1}$（$n \ge 1$）。

**出处。**Berndt Part I, Ch. 3, §8 例 5(ii), p. 53。

**状态。**已证明。数值复核：$\Delta^n C_0 = -C_{n-1}$ 在 $n=1,\dots,4$ 时成立（$1, 0, -1, -1$）。

**对照。**见 M13。

**记号说明。**OCR 底本把 $\Delta^n C_0$ 的下标 $0$ 误读为 $n$；已按 PDF 原图与数值复核纠正。

## 第 8 节 例 6——$f_n(\pm 1)$ 的恒等式

**陈述。**(i) $f_3(1) = 3f_2(1) = 15$；(ii) $f_5(1) + f_2(1) = 4f_4(1) = 208$；(iii) $f_3(-1) = f_2(-1) = 1$；(iv) $f_6(-1) = f_5(-1) = -9$；(v) $f_8(-1) + f_6(-1) + f_5(-1) + f_3(-1) = 5f_7(-1) = 250$。由例 5(i)(ii) 易验。

**出处。**Berndt Part I, Ch. 3, §8 例 6, p. 53。

**状态。**已证明。

**对照。**见 M13。

## Entry 9——$F_n(a,b;x)$ 的推广

**陈述。**(9.1)(9.2)
$$e^x F_n(a,b;x) = \sum_{k=1}^{\infty} \frac{(a+bk)^n x^k}{(k-1)!};\qquad e^x F_n(a,b;x) = e^x\sum_{j=0}^{n} \binom{n}{j} a^{n-j}b^j f_j(x)$$
$f_n(x)$ 是 $a=0$、$b=1$ 的特例。

**(i)** 当 $z \to \infty$（在 $R_\varepsilon$ 内）时
$$\sum_{k=0}^{n} \frac{(-1)^k F_k(x)}{z^{k+1}} = \sum_{k=1}^{n+1} \frac{(-b)^{k-1}x^k}{(z+a+b)(z+a+2b)\cdots(z+a+kb)} + O(z^{-n-2})$$
即 Entry 3 的推广；证明用 Taylor 定理引理 (9.3)。

**(ii)** (9.4)
$$\sum_{n=0}^{\infty} \frac{y^n}{n!} F_n(x) = x e^{(a+b)y} e^{x(e^{by}-1)}, \qquad a, b, x, y \text{ 任意复数}$$
即 Entry 4 的推广。代数验算通过（经 (9.2) 与 (5.2)，把 $a$ 换成 $by$）。

**(iii)** $F_{n+1}(x) - (a+b)F_n(x) = bx\sum_{k=0}^{n} \binom{n}{k} b^k F_{n-k}(x)$，即 Entry 5 的类比。差分表述：$\psi_n(x) = F_{n+1}(x) - (a+b)F_n(x) = bx(b+F)^n$（umbral 记号，$F^k$ 表 $F_k(x)$）；算子 $\delta g(n) = g(n) - bg(n-1)$；$\delta^k \psi_n = bx(b+F)^{n-k}F^k$（$0 \le k \le n$）；$\delta^n \psi_n = bxF_n(x)$。$F_0(x) = x$；$F_n(x)$ 是 $n+1$ 次多项式，$F_n(0) = 0$。

(9.5)
$$F_n(x) = \sum_{k=1}^{n+1} \theta_k(n)x^k$$
**注意：此处 $\theta_k(n)$ 是依赖 $a$、$b$ 的推广系数，与 §6 的 $\varphi_k(n) = S(n+1,k)$ 同名异义**——本书在 (9.5) 处沿用 $\varphi_k(n)$ 的记号，本文件改用 $\theta_k(n)$ 区分，并以此为准。

**(iv)** $\sum_{k=0}^{r-1} \theta_{r-k}(n)/k! = (a+br)^n/(r-1)!$，$0 < r \le n+1$（Entry 6 的推广；$a=0$、$b=1$ 时还原）。

**(v)** $(r-1)!\,\theta_r(n) = \sum_{k=0}^{r-1} (-1)^k \binom{r-1}{k}\{a+(r-k)b\}^n$（Entry 7 的推广）。

**(vi)** $\theta_r(n+1) = (a+br)\theta_r(n) + b\theta_{r-1}(n)$，$1 \le r \le n+1$，$\theta_0(n) = 0$（Entry 8 的推广）。

(9.6)
$$F_0(x) = x;\quad F_1(x) = (a+b)x + bx^2;\quad F_2(x) = (a+b)^2x + b(2a+3b)x^2 + b^2x^3$$
$$F_3(x) = (a+b)^3x + b\{3(a+b)(a+2b)+b^2\}x^2 + 3b^2(a+2b)x^3 + b^3x^4$$
$$F_4(x) = (a+b)^4x + b(2a+3b)\{2(a+b)(a+2b)+b^2\}x^2 + b^2\{6(a+2b)^2+b^2\}x^3 + 2b^3(2a+5b)x^4 + b^4x^5$$
数值复核：$a=-1$、$b=2$ 时 $F_2 = x+8x^2+4x^3$、$F_3 = x+26x^2+36x^3+8x^4$、$F_4 = x+80x^2+232x^3+128x^4+16x^5$。

**(vii)** $0 \le r \le n$ 时 $r!\,\theta_{r+1}(n)$ 是 $e^{(a+b)x}(e^{bx}-1)^r$ 的 Maclaurin 级数中 $x^n/n!$ 的系数（第 8 节例 2 的推广；$a=0$、$b=1$ 时还原）。

**Entry 9 后的例 (i)–(iv)**（pp. 56–57）：(i) $\sum_{k=0}^{\infty} (-1)^k[(2k+1)^3+(2k+1)^2]/k! = 0$（经 (9.7)，$F_2(-1,2;-1) = 3 = -F_3(-1,2;-1)$）；(ii) $\sum_{k=1}^{\infty} k^4/(k-1)! = 4\sum_{k=0}^{\infty} (2k+1)^2/k!$（两边 $= 52e$；左用第 8 节例 5(i)，右 $= 4eF_2(-1,2;1) = 4e\cdot 13$）；(iii) $\sum_{k=1}^{\infty} (-1)^{k-1}(k^7+k^6)/(k-1)! = \sum_{k=1}^{\infty} (-1)^k(2k-1)^4/(k-1)!$（两边 $= -41/e$；左用第 8 节例 5(ii)：$-50/e + 9/e$；右 $= F_4(-1,2;-1)/e = -41/e$）；(iv) $\sum_{k=1}^{\infty} (-1)^k(2k+1)^4/(k!\cdot k) = \sum_{k=1}^{\infty} (-1)^k/(k!\cdot k) - 8$（(9.8)：花括号内 $8F_0 + 24F_1 + 32F_2 + 16F_3$ 在 $a=-1$、$b=1$、$x=-1$ 时 $= -8+24+0-16 = 0$）。

**两处拉马努金原文错误**（p. 57）：例 (iii) 须把等式任一边乘 $-1$；例 (iv) 须把右端 $-4$ 改为 $-8$。$F_n(a-1,1;x)$ 的性质见 Manikarnikamma 的工作。

**出处。**Berndt Part I, Ch. 3, Entry 9, pp. 53–57。

**状态。**已证明（(i)–(vii) 与例 (i)–(iv) 的纠正后形式）。数值复核：(i) 在 $z=100$、$a=1$、$b=2$、$x=1$、$n=2$ 时左端 $0.009529$、右端 $0.0095273$，差 $1.7\times 10^{-6}$，与 $O(z^{-4})$ 的量级一致；(iii) 在 $n=1$ 时代数验算通过（两边 $= b(a+2b)x^2 + b^2x^3$）。

**对照。**推广的 Bell 多项式与 Stirling 数见 M13；渐近展开 (i) 见 M12；生成函数 (ii) 见 M02。

## Entry 10——通用渐近展开

**陈述。**(10.1) 定义非负整数列 $b_{k,n}$：$b_{k,k} = 1$；$b_{k,n} = 0$（$n < k$ 或 $n > 2k-2$）；
$$b_{k+1,n+1} = n\cdot b_{k,n-1} + (n-k+1)\cdot b_{k,n}, \qquad k \le n \le 2k-1$$
$b_{k,n}$ 表（$k$ 行 2–7，$n$ 列 2–12，全部用递推复核通过）：$k=2$：$1$；$k=3$：$1, 3$；$k=4$：$1, 10, 15$；$k=5$：$1, 25, 105, 105$；$k=6$：$1, 56, 490, 1260, 945$；$k=7$：$1, 119, 1918, 9450, 17325, 10395$。实为 $b_{k,n} = S_2(n, n+1-k)$，$S_2$ 为 2-结合第二类 Stirling 数（Comtet pp. 221–222；Riordan pp. 74–78）。

(10.2)(10.3)：设 $\varphi(x)$（实变元）至多多项式增长；存在常数 $A \ge 1$ 与至多多项式增长的 $G(x)$，使每非负整数 $m$ 与充分大 $x$ 有 $|\varphi^{(m)}(x)/m!| \le G(x)(A/x)^m$；置 $\varphi_\infty(x) = e^{-x}\sum'_{k=0}^{\infty} x^k\varphi(k)/k!$（撇号表示略去 $\varphi(k)$ 无定义的有限项）。则任固定正整数 $M$ 有
$$\varphi_\infty(x) = \varphi(x) + \sum_{k=2}^{M} \sum_{n=k}^{2k-2} b_{k,n} x^{n-k+1} \frac{\varphi^{(n)}(x)}{n!} + O(G(x)x^{-M}), \qquad x \to \infty$$
等价形式见 Yu 2009 年 arXiv:0904.1226（指标交换：$\sum_{n=2}^{2M-2}\sum_{k=\lfloor(n+1)/2\rfloor+1}^{n} b_{k,n} x^{n-k+1}\varphi^{(n)}(x)/n!$）。注：若 $\varphi$ 在 $[0,\infty)$ 有界连续，Feller 的书 pp. 219、227 给出 $e^{-x}\sum x^k\varphi(k)/k! \sim \varphi(x)$；左端即 $E[\varphi(U)]$，$U$ 为均值 $x$ 的 Poisson 随机变量（现代解释：去 Poisson 化）。

拉马努金的形式论证假定 $\varphi$ 整函数（用 (3.3) 展开；笔记中有误印，$f_{n-1}$ 写成 $f_n$），三个应用均不满足其隐含假设。拉马努金用 (10.4)–(10.11) 逐项算到 $k=4$：(10.4) $\varphi_\infty(x) = \varphi(0) + \sum_{n\ge 1} \varphi^{(n)}(0)/n!\sum_{j=1}^n \varphi_j(n-1)x^j$；(10.5) 用 (10.6) $\varphi_n(n-1) = 1$（$n \ge 1$）得 $\varphi(0) + \sum \varphi^{(n)}(0)x^n/n! = \varphi(x)$；(10.7) 用 $\varphi_n(n) = n(n+1)/2$（$n \ge 1$，即 $S(n+1,n) = \binom{n+1}{2}$）得 $(x/2)\varphi''(x)$；(10.8)–(10.11) 为 $k=3,4,5,6$ 的逐项计算（用引理 3 的特例），例如 (10.8) $\sum_{n\ge 3} \varphi^{(n)}(0)/n!\cdot\varphi_{n-2}(n-1)x^{n-2} = (x/6)\varphi'''(x) + (x^2/8)\varphi^{(4)}(x)$。推论：$\varphi_\infty(x) = \varphi(x) + (x/2)\varphi''(x)$「非常近似」，无误差讨论。

4 引理：引理 1（Breusch：$0 < t < 1$ 时 $e^{-x}\sum_{0\le k<tx} x^k/k!$ 与 $e^{-x}\sum_{k>x/t} x^k/k!$ 指数趋 0）；引理 2（$2 \le k \le n$ 时 $b_{k,n} \le (n-1)!$）；引理 3（$2 \le k \le n$ 时 $\varphi_{n+1-k}(n-1) = \sum_{j=k}^{2k-2} b_{k,j}\binom{n}{j}$，其中 $\varphi_k(n)$ 由 (6.1) 定义）；引理 4（$p(x)$ 为 $n$ 次多项式时 $p_\infty(x) := e^{-x}\sum_{k=0}^{\infty} x^k p(k)/k! = p(x) + \sum_{j=2}^{n}\sum_{k=2}^{j} b_{k,j} x^{j-k+1} p^{(j)}(x)/j!$）。

**例 1**（p. 64）：$e^{-x}\sum_{k=0}^{\infty} \sqrt{k}\,x^k/k! = \sqrt{x}(1 - 1/(8x) - 7/(128x^2) + O(x^{-3}))$（$\varphi(x) = \sqrt{x}$，$M=3$；Yu 论文 (4) 式同）。Hardy 特例：$\varphi(x) = (x+a)^{-s}$ 时 (10.3) 给出更复杂形式的展开（Hardy 的书 pp. 410–411；[18] pp. 71–72），系数由 (10.3) 导出：$(x+a)^{-s} + s(s+1)x/[2(x+a)^{s+2}] - s(s+1)(s+2)x/[6(x+a)^{s+3}] + s(s+1)(s+2)(s+3)(x^2/8+x/24)/(x+a)^{s+4} + \cdots$。

**例 2**（p. 65）：$e^{-x}\sum_{k=1}^{\infty} x^k\log(k+1)/k! = \log x + 1/(2x) + 1/(12x^2) + O(1/x^3)$。证明：$\varphi(x) = \log(x+1)$，$M=4$：$= \log(x+1) - x/[2(x+1)^2] + x/[3(x+1)^3] - 3x^2/[4(x+1)^4] + O(1/x^3)$，展开后化简得上式。拉马努金在第 13 章第 12 节重算更多项；Pollak–Shepp 有等价展开。

**例 3**（p. 65）：$\log(\sum_{k=0}^{\infty} 100^k\varphi(k)/k!) = 100 + \log((\varphi(110)+\varphi(90))/2)$「nearly」。拉马努金原话引用：用 $\varphi_\infty(x) \sim \varphi(x)$，$x=100$，$\varphi(100)$ 换成 $\{\varphi(110)+\varphi(90)\}/2$。

**例 4**（p. 65，(10.25)(10.26)）：$\psi(x) = \sum_{k\le x} 1/k$，则 $x \to \infty$ 时 $\sum_{k=1}^{\infty} x^k\psi(k)/k! = e^x(\log x + \gamma + O(1/x))$，$\gamma$ 为 Euler 常数。(10.26)：$\psi(x) = \log x + \gamma + O(1/x)$（Ayoub 的书 p. 43）。证明：代入 (10.25) 后对 $\varphi(x) = \log x$ 用 (10.3) 取 $M=1$。另证可用 Entry 2 推论 2。拉马努金称 $\gamma$（他记 $c$）为级数 $\sum_{k=1}^{\infty} 1/k$ 的「常数」，预示第 6 章发散级数工作。

**出处。**Berndt Part I, Ch. 3, Entry 10, pp. 57–66。

**状态。**已证明（Berndt 在弱假设下重证；拉马努金的形式论证不严谨，三个应用不满足其隐含假设——见导言）。数值复核（mpmath，30 位）：例 1 在 $x=100$ 时左端 $9.98744456$、右端 $9.98744531$，差 $7.5\times 10^{-7}$，与 $O(x^{-3})$ 的量级一致；Hardy 特例 $s=1$、$a=1$、$x=100$ 时左端 $0.01$、右端 $0.00999995$，差 $4.8\times 10^{-8}$；引理 3 在 $(n,k) = (3,2)$、$(4,3)$ 时两边分别为 $3$、$7$；(10.8) 在 $\varphi(x) = x^4$ 时两边均为 $7x^2$。

**对照。**渐近展开与 Poisson 去 Poisson 化见 M12；Bell 多项式与 Stirling 数见 M13；调和数与 Euler 常数见 M01；对数渐近见 M02。

**记号说明。**本条的 $\varphi(x)$、$\varphi_\infty(x)$ 与 Entry 2 的 $\varphi(z)$、Entry 3 的 $\psi(z)$ 是不同的函数，勿混淆；$\psi(x) = \sum_{k\le x} 1/k$（例 4）又与 Entry 3 的 $\psi(z)$ 不同，是调和数函数。

## Entry 11——$p_n$ 的递推与 Newton 恒等式

**陈述。**(11.1)(11.2) 设 $f(x) = \sum_{n=1}^{\infty} A_n x^n/n$ 在 $|x| < R$ 解析；定义 $p_n$（$n \ge 0$）使 $\sum_{n=0}^{\infty} p_n x^n = \exp\{f(x)\}$；则
$$n p_n = \sum_{k=1}^{n} A_k p_{n-k}, \qquad n \ge 1$$

**推论（Newton 恒等式）。**$\{a_k\}$ 满足 $\sum|a_k| < \infty$；$S_n = \sum_k a_k^n$；$p_n$ 为从 $\{a_k\}$ 取 $n$ 个不同项之积的和，$p_0 = 1$；则
$$n p_n = \sum_{k=1}^{n} (-1)^{k-1} S_k p_{n-k}, \qquad n \ge 1$$
证明：$\sum p_n x^n = \prod(1+a_k x)$，取对数得 $A_n = (-1)^{n-1}S_n$。拉马努金假定 $\{a_k\}$ 有限，实无必要。

**出处。**Berndt Part I, Ch. 3, Entry 11, p. 66。

**状态。**已证明。

**对照。**Newton 恒等式与初等对称和见 M01（数论）与 M13（组合）；指数生成函数见 M02。

## (12.1)——$F_r(n)$ 的定义

**陈述。**
$$F_r(n) = \sum_{k=0}^{\infty} \frac{(n+k)^{r+k}}{a^k k!}, \qquad r \text{ 为整数，} n \text{ 为复数}$$
Stirling 公式得第 $k+1$ 项渐近于 $(1/\sqrt{2\pi})k^{r-1/2}(e/a)^k$，故 $|a| > e$ 时收敛，$|a| = e$ 时 $r < -1/2$ 亦收敛。

**出处。**Berndt Part I, Ch. 3, (12.1), p. 66。

**状态。**已证明（收敛性由 Stirling 公式）。

**对照。**Stirling 公式见 M12；级数收敛判别见 M02。

**记号说明。**本条底数是 $(n+k)$，不是 $(n+kr)$——初读误读为 $(n+kr)$，已按三方证据纠正：渐近式 $(1/\sqrt{2\pi})k^{r-1/2}(e/a)^k$ 与收敛条件 $|a| > e$（而非 $|a| > re$）只与底数 $(n+k)$ 相容；且 Entry 13 的 $f(n) = nF_{-1}(n)$ 与其推论 (13.8) 均须 $F_{-1}(n) = \sum (n+k)^{k-1}/(a^k k!)$，已数值验证（见 Entry 13）。

## Entry 12——$F_r(n)$ 的递推

**陈述。**$r$、$n$、$a$ 如 (12.1) 之前所定，
$$F_{r+1}(n) = nF_r(n) + \frac{1}{a}F_{r+1}(n+1)$$

**出处。**Berndt Part I, Ch. 3, Entry 12, p. 67。

**状态。**已证明。数值复核：$r=1$、$n=2$、$a=3$ 时两边均为 $1453.68914474$（差 $1.7\times 10^{-13}$）。证明思路：$(n+k)^{r+1+k} = n(n+k)^{r+k} + k(n+k)^{r+k}$，逐项求和即得。

**对照。**见 M02（级数恒等式）与 M12（Stirling 公式应用）。

## §13 定理与推论——Abel 型卷积与 Gould 多项式

**陈述。**Entry 13 与 Entry 14 涉及形如 $\varphi(x) = \sum_{n=0}^{\infty} f_n(x)a^n$ 的函数，其中系数是 $x$ 的多项式，满足 (13.1)
$$f_n(x+y) = \sum_{k=0}^{n} f_k(x)f_{n-k}(y), \qquad 0 \le n < \infty$$
$x$、$y$ 为任意实数。于是 $\varphi$ 满足 (13.2) $\varphi(x+y) = \varphi(x)\varphi(y)$。

**定理。**设 $p$、$q$ 为常数，$q \ne 0$；多项式列 $f_n(x)$（$0 \le n < \infty$）满足差分方程 (13.3)
$$f_n(x+q) - f_n(x) = qf_{n-1}(x+p), \qquad n \ge 1$$
及初值 (13.4) $f_0(x) \equiv 1$ 与 (13.5) $f_n(0) = 0$（$n \ge 1$），则 $f_n(x)$ 满足 (13.1)。注：(13.3) 右端的因子 $q$ 换成任意常数 $r \ne 0$ 亦成立（解乘 $(r/q)^n$）。

**推论（Gould 多项式）。**$f_0(x) = 1$、$f_1(x) = x$、
$$f_n(x) = \frac{x}{n!}\prod_{k=1}^{n-1} (x+np-kq), \qquad n \ge 2$$
满足 (13.1)。定理与推论非拉马努金原文明言，证明由 U. S. Haslam-Jones 提供给 Wilson；今属 Rota–Mullin 一般理论；多项式由 Jensen 1902 年首引、Gould 续研，即今 Gould 多项式。

**出处。**Berndt Part I, Ch. 3, §13, pp. 67–69。

**状态。**已证明。数值复核：推论在 $p=1$、$q=0$、$n=2$、$x=1$、$y=2$ 时，$f_2(3) = 3\cdot 5/2 = 7.5$，右端 $f_0(1)f_2(2) + f_1(1)f_1(2) + f_2(1)f_0(2) = 4 + 2 + 1.5 = 7.5$；$n=3$ 时两边均为 $18$。

**对照。**Abel 二项定理与 Gould 多项式见 M13；卷积恒等式见 M02；多项式列的差分方程见 M14。

## Entry 13——$x = a\log x$ 的根与 $x^n = f(n)$

**陈述。**设 $f(n) = nF_{-1}(n)$，$F_{-1}$ 由 (12.1) 定义；$a$ 为实数，$|a| \ge e$；则存在正实数 $x$ 满足 $x = a\log x$，使对任意实数 $n$ 有 $x^n = f(n)$。即
$$f(n) = 1 + \sum_{k=1}^{\infty} \frac{n(n+k)^{k-1}}{a^k k!} = x^n$$
证明：推论取 $p=1$、$q=0$，由 (13.2) 得 $f(m)f(n) = f(m+n)$；正整数 $n$ 得 $f(n) = x^n$（$x = f(1)$）；延拓到负整数（$f(n)f(-n) = f(0) = 1$）、有理数（$\{f(r/s)\}^s = f(r) = x^r$）、全体实数（$|a| \ge e$ 时一致收敛故连续）。又 $f'(n) = x^n\log x$，$f'(0) = \log x = \sum_{k=1}^{\infty} k^{k-2}/(a^k(k-1)!) = f(1)/a = x/a$。

分支讨论（p. 70）：$a > e$ 时 $x(a)$ 有两实分支 $x_1$（$a: e \to \infty$ 时 $e \to 1$）与 $x_2$（$e \to \infty$）；$a = e$ 为分支点；$f(1)$ 在 $a \to \infty$ 时趋于 1，故取 1 与 $e$ 之间的分支；Entry 13 表明 $f(n) = x_1^n$。

**推论。**(13.8) $z$ 为任意复数，$w$ 为任意复数且 $e^{w-1} \ge |w|$，则
$$e^z = \sum_{k=0}^{\infty} \frac{z(z+kw)^{k-1}e^{-kw}}{k!}$$
证明：Entry 13 取 $x = e^w$、$a = e^w/w$，令 $z = nw$；再对 $w$、$z$ 作解析延拓。

**出处。**Berndt Part I, Ch. 3, Entry 13, pp. 69–70。

**状态。**已证明。数值复核（mpmath，30 位）：$a=3$ 时 $x \approx 1.857184$（$x = 3\log x$ 在 $(1,e)$ 内的根），$f(1) \approx 1.857$、$f(2) \approx 3.449 = x^2$；$f'(0) = \sum k^{k-2}/(a^k(k-1)!) \approx 0.619 = x/a$；推论 (13.8) 在 $z=1$、$w=0.5$ 时左端 $e \approx 2.71828$、右端部分和（$k \le 10$）$2.66219$、余项约 $0.056$，收敛到 $e$。

**对照。**Lambert W 函数与树函数型展开见 M13/M12；$x = a\log x$ 的分支见 M14（超越方程）；推论 (13.8) 的 Abel 型级数见 M02。

## Entry 14——$aqx^p - x^q + 1 = 0$ 的根与 $\varphi(n) = x^n$

**陈述。**(14.1) $c_0(n) = 1$、$c_1(n) = n$，
$$c_k(n) = n\prod_{j=1}^{k-1} (n+kp-jq), \qquad k \ge 2$$
(14.2) 对复数 $a$，
$$\varphi(n) = \sum_{k=0}^{\infty} \frac{c_k(n)a^k}{k!}$$
特殊情形：$p = q = 0$ 时 $\varphi(n) = e^{an}$；$p \ne 0$、$q = 0$ 时 $\varphi(n) = f(n/p)$（$f$ 为 Entry 13 的函数，$a$ 换成 $1/(ap)$）；$p = 0$、$q \ne 0$ 时 $\varphi(n) = (1+aq)^{n/q}$；$p = q \ne 0$ 时 $\varphi(n) = (1-ap)^{-n/p}$。对称性：$\varphi(n) = \varphi(n; p, q, a) = \varphi(-n; -p, -q, -a) = \varphi(n; p-q, -q, a) = \varphi(-n; q-p, q, -a)$。收敛条件 (14.3)：$|a| \le p^{-p/q}|p-q|^{(p-q)/q}$。

**Entry 14。**(14.4) 若 $x$ 是方程
$$aqx^p - x^q + 1 = 0$$
的某根，则 $\varphi(n) = x^n$ 对一切实数 $n$ 成立。证明要点：直接计算得 $(1/k!)c_k(q) - (q/(k-1)!)c_{k-1}(p) = 0$，故 $\varphi(q) = aq\varphi(p) + 1$，即 $x^q = aqx^p + 1$；由 (14.5) $\varphi(n) = x^n$（$\varphi(1) = x$）得证。注：由 (14.2)，$x = x(a)$ 在 $a \to 0$ 时趋于 1。

**推论 1。**$n$ 为实数，$|a| \le 1/4$ 时
$$\left(\frac{2}{1+\sqrt{1-4a}}\right)^n = 1 + na + n\sum_{k=2}^{\infty} \frac{\Gamma(n+2k)a^k}{\Gamma(n+k+1)k!}$$
证明：Entry 14 取 $p = 2q$，趋于 1 的根 $x^q = (1-\sqrt{1-4aq})/(2aq) = 2/(1+\sqrt{1-4aq})$，再令 $q = 1$。

**推论 2。**$n$ 为实数，$|a| \le 1$ 时
$$(a+\sqrt{1+a^2})^n = 1 + na + \sum_{k=2}^{\infty} \frac{b_k(n)a^k}{k!}$$
其中 $k \ge 2$ 时，$k$ 偶：$b_k(n) = n^2(n^2-2^2)(n^2-4^2)\cdots(n^2-(k-2)^2)$；$k$ 奇：$b_k(n) = n(n^2-1^2)(n^2-3^2)\cdots(n^2-(k-2)^2)$。证明：Entry 14 取 $q = 2p$，根 $x^p = ap + \sqrt{a^2p^2+1}$，令 $p = 1$、$q = 2$。

历史（p. 72）：Entry 14 首见 Lambert 1758 年的论文；Lagrange 1770 年发表 Lagrange 反演公式并由此导出 Entry 14；Euler 1779 年（受 Lambert 启发）证明 Entry 13 与 Entry 14，Entry 13 实已见 Euler 1778 年的论文（无证明）；Rothe 1793 年学位论文重发现 Entry 14 的 $q=1$ 特例；亦可由 Abel 二项定理推广得出，有时归于 Abel；Entry 13 于 1844 年由 Eisenstein 重发现；Wittstein 1845、Woepcke 1851、Seidel 1873、Jensen 1902 另有证明；Gould 有类似更一般的定理；Entry 14 的推广见 Birkeland；Hardy [20] p. 194 提到拉马努金关于 (14.4) 的工作；拉马努金在 quarterly reports 中亦讨论 (14.4)；Entry 13 推论基本即 Bromwich 的书 p. 160 的习题（亦见 p. 195），Chaundy 的书 p. 409 与 Carmichael 的论文用 Lagrange 反演导出；Rogers 给出应用；Jackson 得出 q-模拟；Gould [7] 编有相关文献目录；Knoebel 有综述。

**出处。**Berndt Part I, Ch. 3, Entry 14, pp. 70–72。

**状态。**已证明。数值复核：推论 1 在 $n=1$、$a=0.1$ 时左端 $2/(1+\sqrt{0.6}) \approx 1.12702$、右端 $1 + 0.1 + 0.02 + 0.005 + 0.0014 + \cdots \approx 1.127$；推论 2 在 $a=0.3$、$n=2$ 时两边均为 $1.80641839053$（差 $7\times 10^{-17}$）；关键恒等式 $(1/k!)c_k(q) - (q/(k-1)!)c_{k-1}(p) = 0$ 在 $p=2$、$q=1$、$j=2,3,4$ 时逐项成立（$4$、$30$、$336$）。

**对照。**Lagrange 反演与 Abel 二项定理见 M13；代数方程 (14.4) 的根见 M14；Gamma 函数见 M10；推论 1 的 $\Gamma$ 级数见 M02。

## Entry 15——$u - \log u = 1 + x^2/2$

**陈述。**(15.1) $0 < u < 1$ 由
$$u - \log u = 1 + \frac{x^2}{2}, \qquad x \text{ 实数}$$
定义，则 (15.2)
$$\sum_{k=0}^{\infty} \frac{(k+1)^{k-1}}{k!} e^{-k(1+x^2/2)} = ue^{1+x^2/2}$$
又充分小正 $x$ 时 $u = \sum_{k=0}^{\infty} b_k x^k$，其中 $b_0 = 1$、$b_1 = -1$、$b_2 = 1/3$、$b_3 = -1/36$、$b_4 = -1/270$，余系数由代入恒等式 $(1/2)x^2 = \sum_{j=2}^{\infty} (1-u)^j/j$ 逐次求得。证明：Entry 13 取 $x = e^u$、$a = e^u/u$，则 $a = \exp(1+x^2/2)$；$F(u) = 2(u-1-\log u) = x^2$，$F$ 在 $u=1$ 附近解析，$F'(1) = 0$、$F''(1) \ne 0$，故 $u$ 可表为 $x$ 的解析函数。

**例 1**（pp. 73–75）：$m$ 为实数、$0 < n \le 2$ 时
$$2^m = \sum_{k=0}^{\infty} \frac{m\Gamma(m+kn)}{\Gamma(m+kn-k+1)2^{kn}k!}$$
**拉马努金断言 $0 < n < \infty$ 皆真，实为 $0 < n \le 2$ 真、$n > 2$ 假**（级数在 $0 < n < \infty$ 均收敛，但 $n > 2$ 时收敛到另一值）。证明：Entry 14 取 $n \to m$、$a = 2^{-n}$、$p \to n$、$q = 1$，方程 (15.3) $f(x) = 2^{-n}x^n - x + 1 = 0$ 有根 $x = 2$；收敛条件 (15.5) $2^{-n} \le n^{-n}|n-1|^{n-1}$（$n \ne 1$；$n=1$ 时作 $2^{-1} \le 1$ 解），$g(x) = (x/2)^x(1-x)^{1-x} \le 1$（$x \ge 0$）保证成立；$f'(x) = n2^{-n}x^{n-1} - 1$ 有唯一正零点 $\xi$；$0 < n \le 1$ 时 $x=2$ 为唯一正根；$n > 1$ 时另有一正根 $\alpha > 1$，$\alpha = 2$ 当且仅当 $n=2$，$f'(2)$ 的符号同 $n-2$，故 $1 < n < 2$ 时 $\alpha > 2$，$n > 2$ 时 $\alpha < 2$；$m = -1/2$ 时在 $1 \le n \le 2$ 一致收敛故 $x=2$；$n > 2$ 时取 $m=1$、$n=3$ 证级数和 $< 2$（$\alpha = \sqrt{5}-1 \approx 1.236$ 的情形，$a_k$ 比值估计），故等式在 $n > 2$ 时不成立。关键一步 (15.6)：$\sum_{k=0}^{\infty} \Gamma(3k+1)/(\Gamma(2k+2)8^k k!) = \sqrt{5}-1$，比值 $a_{k+1}/a_k = 3(3k+1)(3k+2)/(16(k+1)(2k+3)) < 27/32$，故和 $< 1 + 1/8 + 3/10 < 2$。

**例 2**（p. 75）：$a > 0$，$m$、$n$、$p$ 为实数非零，$x > 0$ 由 $(\log x)^m = ax^n$ 定义，则对 $a \le |m/(en)|^m$ 有
$$x^p = p\sum_{k=0}^{\infty} \frac{(mp+nk)^{k-1}a^{k/m}}{m^{k-1}k!}$$
证明：定义 $y > 0$ 使 $y^m = x^n$（即 $y = x^{n/m}$），则 $(\log y)/y = (n/m)a^{1/m}$；Entry 13 取 $x \to y$、$a \to (m/n)a^{-1/m}$，得 $x^p = y^{mp/n} = \sum_{k=0}^{\infty} (mp/n)(mp/n+k)^{k-1}/((ma^{-1/m}/n)^k k!)$，化简即得。

**出处。**Berndt Part I, Ch. 3, Entry 15, pp. 73–76。

**状态。**已证明（例 1 的范围经 Berndt 订正为 $0 < n \le 2$）。数值复核：(15.2) 在 $x=1$ 时两边均为 $1.3521684495$（差 $2\times 10^{-16}$）；例 1 在 $(m,n) = (1,1)$、$(1,2)$、$(2,1)$ 时两边分别为 $2$、$2$、$4$（其中 $(1,2)$ 的通项即 Catalan 数$/4^k \sim k^{-3/2}$）；例 2 在 $m=2$、$n=1$、$p=1$、$a=0.1$ 时右端 $\approx 1.467$，与 $(\log x)^2 = 0.1x$ 的根 $x \approx 1.47$ 一致。

**对照。**Catalan 数见 M13；Gamma 函数见 M10；Lagrange 反演见 M13；$u$ 的幂级数（$b_k$）见 M02。

**记号说明。**例 2 证明中 $y$ 的定义，原文印文疑有误（见末尾待核对清单第 6 项）；按证明推导应为 $y^m = x^n$，已数值验证公式本身成立。

## 例 3(i)–(viii) 与例 4(i)–(iv)——Entry 13 的换元族

以下各例均由 Entry 13 换元得出（pp. 76–77）。书中注记：在以下全部例子的证明中，方程 $X = A\log X$（$A \ge e$）的相关根 $X$ 取 1 与 $e$ 之间的那支；若 $X = -A\log X$（$A \ge e$），则 0 与 1 之间的根唯一，无歧义。

**例 3(i)。**与 Entry 13 基本相同，唯 $x$ 改由 $x = \pm a\log x$ 两种方式定义。

**例 3(ii)。**Entry 13 中 $a$ 换成 $\pm a/\log a$。

**例 3(iii)。**$a$ 为实数，$a \le e$，$x$ 由 $x = ae^{\pm x}$ 两种等式之一定义，则
$$e^x = \sum_{k=0}^{\infty} \frac{(k+1)^{k-1}a^k}{k!} \quad\text{与}\quad e^{-x} = \sum_{k=0}^{\infty} \frac{(k+1)^{k-1}(-a)^k}{k!}$$
分别成立。证明：令 $x = \log y$，则 $y/\log y = 1/a$ 与 $y^{-1}/\log(y^{-1}) = 1/a$，Entry 13 取 $a \to 1/a$ 与 $-1/a$。$x=1$ 时第一等式是 Newman 提出的问题（亦可由 Entry 13 的推论得出）。

**例 3(iv)。**Entry 13 中 $a$ 换成 $\pm 1/\log a$。

**例 3(v)。**$a > 0$、$|\log a| \le e$，$x > 0$ 由 $x^{\pm x} = a$ 两种关系之一定义，则
$$\frac{1}{x} = \sum_{k=0}^{\infty} \frac{(k+1)^{k-1}(\mp\log a)^k}{k!}$$
证明：令 $x = 1/y$，则 $\mp(\log y)/y = \log a$，Entry 13 取 $x \to y$、$a \to \mp 1/\log a$。

**例 3(vi)。**与例 3(iii) 相同，唯第二本笔记中关系换成 $x = ae^{\mp x}$ 的另一形式。

**例 3(vii)。**$a$ 为实数，$x$ 由 $e^x \pm x = a$ 两种关系之一定义，则分别地，若 $a \le -1$，
$$e^{-e^x} = \sum_{k=0}^{\infty} \frac{(k+1)^{k-1}(-1)^k e^{ak}}{k!}$$
若 $a \ge 1$，
$$e^{e^x} = \sum_{k=0}^{\infty} \frac{(k+1)^{k-1}e^{-ak}}{k!}$$
证明：令 $x = \log\log y$，则 $e^a = y(\log y)^{\pm 1}$；前者 $\log(1/y)/(1/y) = e^{-a}$，后者 $y/\log y = e^a$，Entry 13 取 $x \to 1/y$、$a \to -e^{-a}$ 与 $x \to y$、$a \to e^a$。

**例 3(viii)。**与例 3(vii) 相同，唯 $x$ 换成 $\log x$。

**例 4(i)。**$x > 0$，$v$ 由 $v = x^{x^{x^{\cdots}}}$（无穷幂塔）定义，则当 $\log x \le 1/e$ 时
$$v = \sum_{k=0}^{\infty} \frac{(k+1)^{k-1}(\log x)^k}{k!}$$
证明：Entry 13 取 $a \to 1/\log x$，$x$ 换成 $v$。拉马努金把 $v$ 写作 $x^{x^{x^{\cdots}}}$ 之类记号，Eisenstein 亦用此记号。若把 $x^{x^{x^{\cdots}}}$ 解释为序列 $x$、$x^x$、$x^{x^x}$、$\cdots$ 的极限，则在 $e^{-e} \le x \le e^{1/e}$ 时收敛（Apostol 习题 12-7 p. 383、Bromwich 习题 11 p. 23、Knopp 习题 23 p. 108、Bender–Orszag 习题 4.2 p. 196、Francis–Littlewood pp. 10、38、39；Lense、Ogilvy 曾作期刊问题；Andrews–Lacher 详研；更一般问题见 Barrow、Creutz–Sternheimer、Shell；Knoebel 综述）。

**例 4(ii)。**与例 3(vii) 相同，唯 $x$、$a$ 换成 $v$、$\pm x$。

**例 4(iii)。**Entry 13 的改述，$x$ 换成 $e^x$、$a$ 换成 $x$。

**例 4(iv)。**例 4(ii) 的另一版本，$x$ 换成 $-x$、$v$ 换成 $-v$；即 $x$、$v$ 满足 $v = \pm\log(x+v)$ 之类关系（原文此处印作 $x + u$，见末尾待核对清单第 7 项）。

**出处。**Berndt Part I, Ch. 3, 例 3(i)–(viii) 与例 4(i)–(iv), pp. 76–77。

**状态。**已证明（均由 Entry 13 换元得出）。

**对照。**无穷幂塔与 $e^{-e} \le x \le e^{1/e}$ 的收敛区间见 M12；Lambert W 函数与树函数见 M13；例 3(iii) 的 Newman 问题见 M02。

## Entry 16——$\varphi_r(n)$ 的推广

**陈述。**(16.1) 拉马努金接下来尝试推广 Entry 13，考虑由
$$x^n\varphi_r(n) = F_r(n)$$
定义的函数 $\varphi_r(n)$，其中 $x = a\log x$，$F_r(n)$ 由 (12.1) 定义，$a$ 如 Entry 12 之前所定。故 $\varphi_{-1}(n) = 1/n$。

**Entry 16(a)。**(16.2) $r$ 为整数、$n$ 为任意复数时
$$n\varphi_r(n) = \varphi_{r+1}(n) - (\log x)\varphi_{r+1}(n+1)$$
证明用 (16.1) 与 Entry 12 及 $x/a = \log x$。

$r = -2$ 得 $\varphi_{-2}(n) = 1/n^2 - (\log x)/(n(n+1)) = (1-\log x)/(n(n+1)) + 1/(n^2(n+1))$；$r = -3$ 得
$$\varphi_{-3}(n) = \frac{1-\log x}{n^2(n+1)} + \frac{1}{n^3(n+1)} - \frac{\log x}{n}\left\{\frac{1-\log x}{(n+1)(n+2)} + \frac{1}{(n+1)^2(n+2)}\right\}$$
$$= \frac{(1-\log x)^2}{n(n+1)(n+2)} + \frac{(3n+2)(1-\log x)}{n^2(n+1)^2(n+2)} + \frac{3n+2}{n^3(n+1)^2(n+2)}$$
两式均为拉马努金所给；由 (16.2) 知 $r \ge 1$ 时 $\varphi_{-r}(n)$ 是 $\log x$ 的 $r-1$ 次多项式，系数为 $n$ 的有理函数。

$r \ge 0$ 的计算：令 $x = e^u$、$a = e^u/u$，$\varphi_r(n) = g_r(n,u) = g_r(u)$；由 (16.1) 得 $g_r(u) = \sum_{k=0}^{\infty} (n+k)^{r+k}e^{-u(n+k)}u^k/k! = \sum_{k=0}^{\infty}\sum_{j=0}^{\infty} (n+k)^{r+k+j}(-1)^j u^{k+j}/(k!j!)$。$g_0^{(m)}(0) = S(m,m)$，其中 $S(m,m) = \sum_{k=0}^{m} (-1)^{k+m}\binom{m}{k}(n+k)^m$；众所周知（Hansen 的表 p. 134）$S(m,m) = m!$，故 (16.3) $g_0(u) = \sum_{m=0}^{\infty} u^m = 1/(1-u)$。归纳得 (16.4)
$$g_r(u) = \sum_{k=1}^{r+1} \frac{\psi_k(r,n)}{(1-u)^{r+k}}, \qquad r \ge 0$$
其中 $\psi_k(r,n)$（$1 \le k \le r+1$）与 $u$ 无关；递推 (16.5)
$$\psi_k(r,n) = (n-r-k+1)\psi_k(r-1,n) + (r+k-2)\psi_{k-1}(r-1,n), \qquad 1 \le k \le r+1$$
约定 $\psi_0(r-1,n) = 0 = \psi_{r+1}(r-1,n)$。

**Entry 16(b)。**$r$、$t$ 为整数，$1 \le t \le r+2$ 时
$$\psi_t(r+1,n) = (n-1)\psi_t(r,n-1) + \psi_{t-1}(r+1,n) - \psi_{t-1}(r+1,n-1)$$
其中 $\psi_t(r,n) = 0$ 若 $t \notin \{k: 1 \le k \le r+1\}$。证明：把 (16.4) 代入 (16.2)，比较 $(1-\log x)$ 的幂系数，$n$ 换成 $n-1$ 得。

用 (16.5) 或 16(b) 与 $\psi_1(0,n) = 1$ 可逐次算出 $\varphi_1(n)$、$\varphi_2(n)$、$\varphi_3(n)$……原文给出（均为拉马努金所给）：
$$\varphi_1(n) = \frac{n-1}{(1-\log x)^2} + \frac{1}{(1-\log x)^3}$$
$$\varphi_2(n) = \frac{(n-1)(n-2)}{(1-\log x)^3} + \frac{(n-1)(n-2)\{1/(n-2) + 2/(n-1)\}}{(1-\log x)^4} + \frac{3}{(1-\log x)^5}$$
$$\varphi_3(n) = \frac{(n-1)(n-2)(n-3)}{(1-\log x)^4} + \frac{(n-1)(n-2)(n-3)\{1/(n-3) + 2/(n-2) + 3/(n-1)\}}{(1-\log x)^5} + \frac{15n-35}{(1-\log x)^6} + \frac{15}{(1-\log x)^7}$$

**推论 1。**$x$ 为复数。若 $-\rho < n < 1$，其中 $\rho$ 是 $ye^{y+1} = 1$ 的唯一实根（Newton 法得 $\rho = 0.27846454\cdots$），则 (16.6)
$$\frac{e^x}{1-n} = \sum_{k=0}^{\infty} \frac{(x+kn)^k}{k!\,e^{kn}}$$
若 $n > 1$，则 (16.7)
$$\frac{e^{mx/n}}{1-m} = \sum_{k=0}^{\infty} \frac{(x+kn)^k}{k!\,e^{kn}}$$
其中 $0 < m < 1$、$e^m/m = e^n/n$。证明：(16.8) $F_0(y) = \sum_{k=0}^{\infty} (y+k)^k/(a^k k!) = t^y/(1-\log t)$，其中 $t = a\log t$；$n=0$ 时 (16.6) 化为 $e^x$ 的 Maclaurin 级数；取 $a = e^n/n$（$-\rho < n < 1$，$n \ne 0$），$|a| > e$，根 $t = e^n$，令 $y = x/n$ 得 (16.6)；$n=1$ 时级数发散，$n > 1$ 时收敛，取 $a = e^m/m$ 证 (16.7)。(16.6) 显然首见 Jensen [2]，Duparc–Lekkerkerker–Peremans 与 Gould [3] 另有证明；Carlitz [2] 用此推论证某多项式集的正交性。注：推论 1 的第二部分（(16.7)）非拉马努金所给；拉马努金对 (16.6) 未加 $n$ 的条件。

**推论 2。**每非负整数 $r$ 有
$$n^r = \lim_{a\to\infty} \varphi_r(n) = \sum_{k=1}^{r+1} \psi_k(r,n)$$
第一等式由 (12.1)(16.1) 直接得，第二等式由 (16.4) 的 $\psi_k(r,n)$ 定义得。

**出处。**Berndt Part I, Ch. 3, Entry 16, pp. 78–81。

**状态。**已证明。数值复核（mpmath，30 位）：16(a) 在 $a=3$（$x \approx 1.857184$）、$r=0$、$n=2.5$ 时两边均为 $6.56273545573$；$\varphi_1$、$\varphi_2$、$\varphi_{-2}$、$\varphi_{-3}$ 的闭式在同组参数下与级数定义逐项一致（差 $< 4\times 10^{-13}$）；推论 1 的 (16.6) 在 $n=0.5$、$x=1$ 时左端 $e/0.5 = 5.43656$、右端部分和（$k \le 10$）$4.9805$、余项约 $0.456$，收敛到左端；推论 2 在 $r=0,\dots,5$、$n=2$、$3.5$ 时逐项成立。

**对照。**$\varphi_r(n)$ 的递推与 $\psi_k(r,n)$ 的组合数见 M13；(16.6) 作为 $e^x$ 的 Maclaurin 级数的推广见 M02；$\rho = 0.27846454$ 的数值见 M12。

**记号说明。**本条的 $\psi_k(r,n)$ 与 Entry 3 的 $\psi(z)$、例 4 的 $\psi(x)$ 均不同，是三个同名异义的记号；$\varphi_r(n)$ 亦与 Entry 2 的 $\varphi(z)$ 不同。

## Entry 17——$A_r$ 的递推

**陈述。**固定 $a > 1/e$，实数 $h$ 定义 $x > 0$ 使 (17.1)
$$x^x = a^a e^h$$
则 $x\log x = a\log a + h$ 且 $(1+\log x)dx/dh = 1$，即 (17.2) $(x + a\log a + h)dx/dh = x$。$h=0$ 时 $x=a$，(17.3) $dx/dh|_{h=0} = 1/(1+\log a) \equiv n$。$h(x)$ 在 $a$ 附近一一解析，有解析逆 $x = x(h)$，故有展开 (17.4)
$$\frac{x-a}{a} = \sum_{k=1}^{\infty} (-1)^{k-1}\frac{A_k}{k!}\left(\frac{h}{a}\right)^k$$
$|h|$ 充分小。

**Entry 17。**(17.5) $r > 2$ 时
$$A_r = n(r-2)A_{r-1} + n\sum_{k=1}^{r-1} \binom{r-1}{k} A_k A_{r-k}$$
证明：(17.4) 代入 (17.2)，比较 $(h/a)^{r-1}$ 系数（$r > 2$）。拉马努金版 (17.5) 把 $k$ 与 $r-k$（$1 \le j < r/2$）的项合并，但最后一项写错；p. 36 第 4 行：$A_{(r-1)/2}$ 乘以 $A_{(r+1)/2}$ 并平方 $A_{r/2}$（Berndt 注）。

(17.6) $A_1 = dx/dh|_{h=0} = N|_{x=a} = n$，其中 $N = dx/dh = 1/(1+\log x)$；(17.7) 一般地 $A_r = (-a)^{r-1}d^r x/dh^r|_{h=0}$（$r \ge 1$）；(17.8) $\sum_{k=0}^{r-2} a(r,k)N^{2r-k-1} = (-x)^{r-1}d^r x/dh^r$（$r \ge 2$）；(17.9) $a(r+1,k) = (r-1)a(r,k-1) + (2r-k-1)a(r,k)$（$r \ge 2$，$0 \le k \le r-1$；$k < 0$ 或 $k > r-2$ 时 $a(r,k) = 0$）；(17.10) $A_r = \sum_{k=0}^{r-2} a(r,k)n^{2r-k-1}$（$r \ge 2$）。

拉马努金算出 $A_r$（$1 \le r \le 7$）：
$$A_1 = n;\quad A_2 = n^3;\quad A_3 = 3n^5+n^4;\quad A_4 = 15n^7+10n^6+2n^5$$
$$A_5 = 105n^9+105n^8+40n^7+6n^6;\quad A_6 = 945n^{11}+1260n^{10}+700n^9+196n^8+24n^7$$
$$A_7 = 10395n^{13}+17325n^{12}+12600n^{11}+5068n^{10}+1148n^9+120n^8$$
首系数 $(2r-3)!!$，末系数 $(r-2)!$；$n=1$ 时 $A_r = (r-1)^{r-1}$。

**例 1。**$n=1$、$r \ge 2$ 时 $\sum_{k=0}^{r-2} a(r,k) = A_r = (r-1)^{r-1}$。证明：(17.6) 取 $n=1$；(17.1) 取 $a=1$、$x=1/y$ 得 $y/\log y = -1/h$，Entry 13 取 $n=-1$、$x \to y$、$a \to -1/h$，比较两级数。

**例 2。**固定 $a$（$0 < a < e$），实数 $h$ 定义 $x > 0$ 使 $x^{1/x} = a^{1/a}e^h$，则 $|h|$ 充分小时
$$\frac{a}{x} = 1 - \sum_{k=1}^{\infty} \frac{A_k(ah)^k}{k!}$$
证明：$x = 1/y$，$y^y = (1/a)^{1/a}e^{-h}$，(17.4) 取 $a \to 1/a$、$h \to -h$、$x \to y$。

另 p. 84 注记：Howard [1] 证 $a(r,k)$ 可用第一类 Stirling 数与结合第二类 Stirling 数表出；Berndt 感谢 R. A. Askey、H. W. Gould、D. Zeilberger 提供的若干文献。

**出处。**Berndt Part I, Ch. 3, Entry 17, pp. 81–83；注记 p. 84。

**状态。**已证明。数值复核：(17.5) 在 $n=1.7$ 时 $A_2,\dots,A_7$ 与书中闭式逐项一致（差 $< 4\times 10^{-9}$）；$n=1$ 时 $A_r = (r-1)^{r-1}$ 在 $r=2,\dots,7$ 时逐项成立（$1$、$4$、$27$、$256$、$3125$、$46656$）；$A_2 = n^3$ 与微分方程直接求导一致（$d^2x/dh^2|_0 = -n^3/a$）。

**对照。**$x^x = a^ae^h$ 的反演与树函数型展开见 M13/M12；$a(r,k)$ 的 Stirling 数表出见 M13；$A_r(1) = (r-1)^{r-1}$ 的计数意义（Cayley 树数）见 M13。

**记号说明。**本条的 $n$ 是 (17.3) 定义的参数 $n = 1/(1+\log a)$，不是求和指标；$A_r$ 的指数规律是 $n^{2r-1}$ 至 $n^{r+1}$（OCR 底本把指数整体读低两档，已按 PDF 原图纠正）。

## 小结

- 本章 17 条 Entry 全部收录完毕（编号均在原文明确出现）。前半（Entry 1–9 与第 8 节例题）是 Bell 数与单变量 Bell 多项式的系统理论：$f_n(x)$ 的定义、递推、生成函数、Stirling 数表出、Bell 数 $A_n$ 与 $C_n$、推广 $F_n(a,b;x)$。后半（Entry 10–17）是级数反演与渐近展开：Entry 10 的通用渐近展开是本章最深的结果；Entry 11 的 Newton 恒等式；Entry 12–14 的 Lagrange 反演主题（Entry 13 为中心）；Entry 15 的 $2^m$ 级数；Entry 16 的 $\varphi_r(n)$；Entry 17 的 $A_r$ 递推。
- 本章发现并纠正的拉马努金原文错误（均已在各条注明）：第 8 节例 4 的积分公式（$n$ 换成 $n+1$）；Entry 9 例 (iii)（等式任一边乘 $-1$）、例 (iv)（右端 $-4$ 改为 $-8$）；Entry 15 例 1 的断言范围（$0 < n < \infty$ 改为 $0 < n \le 2$）；Entry 17 (17.5) 拉马努金版的末项写错。另：Entry 10 的形式论证不严谨、三个应用不满足隐含假设（Berndt 在弱假设下重证）。
- 本轮 OCR 误读纠正（均经 PDF 原图或数值复核证实）：(3.1) 的 $\psi$ 误读为 $\varphi$；(12.1) 的底数误读为 $(n+kr)$，实为 $(n+k)$（渐近式、收敛条件 $|a| > e$ 与 Entry 13 三方印证）；$\Delta^n C_0$ 的下标 $0$ 误读为 $n$；Entry 9(vii) 的 $e^{(a+b)x}$ 读丢；(9.6) 的 $F_3$ 系数读错；(10.6)(10.7) 的 $\varphi_n(n-1)$、$\varphi_n(n)$ 下标误读；$A_r$ 的指数整体读低两档（$A_2 = n^3$ 不是 $n^2$，余类推）；Entry 13 证明中 $f'(n)$ 的第一求和指数（见待核对第 5 项）。
- 与 M 模块的对照：组合分析主线见 M13（Bell 数、Bell 多项式、第二类 Stirling 数、Dobiński 公式、Abel 二项定理、Gould 多项式、Lagrange 反演、无穷幂塔、Cayley 树数）；级数反演与渐近展开见 M02（逆阶乘级数、发散级数、Bernoulli 数——注意 M01 伯努利数定义缺口仍待补）、M07（q-级数背景下的反演思想，Entry 13 推论有 Jackson q-模拟）、M09（积分表示 (2.1) 的积分、Entry 10 的 Poisson 期望）、M12（渐近分析：Entry 3、Entry 9(i)、Entry 10 的通用渐近展开、Stirling 公式应用）、M01（Bernoulli 数、调和数 $\psi(x)$ 与 Euler 常数 $\gamma$、Entry 11 的 Newton 恒等式与初等对称和）；Entry 13–14 的 Lambert–Lagrange–Euler–Abel 历史线与 M14（代数方程 (14.4)、(15.3) 的根）互链；Entry 15 例 1 的 Catalan 数联系 M13；Entry 17 的树函数型展开联系 M13/M12。

## 待核对清单

1. Entry 10 导言称拉马努金给出「三个应用」，而书中 Entry 10 之下列出例 1–4：例 4 是否拉马努金原有、抑或 Berndt 补充，待核对原书导言与例 4 的出处说明。
2. Entry 13 证明中 $f'(n)$ 的第一求和：图示为 $\sum (n+k)^k/(a^k k!)$，但与 $f'(0) = \sum k^{k-2}/(a^k(k-1)!)$ 及推论 (13.8) 一致的应为 $\sum (n+k)^{k-1}/(a^k k!)$（由 $f(n) = 1 + \sum n(n+k)^{k-1}/(a^k k!)$ 求导即得）；图上指数疑为 $k-1$ 印得模糊，待放大核对。
3. Entry 15 例 2 证明中 $y$ 的定义：原文印文疑有误；按证明推导应为 $y^m = x^n$（即 $y = x^{n/m}$），已数值验证公式本身成立，印文待核对。
4. 例 4(iv) 的关系式：原文印作 $v = \pm\log(x+u)$，其中 $u$ 未定义，疑为 $v$ 之误，待核对。
5. Entry 16 推论 1 的 (16.7)：第二部分非拉马努金所给（已注明）；(16.6) 首见 Jensen [2] 的说法已按原文记录，文献细节待核对。
6. Entry 17 例 2 的 $A_k$：证明中 (17.4) 取 $a \to 1/a$，$A_k$ 应按新参数 $n' = 1/(1-\log a)$ 取值，原文未明言，待核对。
7. 本章 TIFR 影印版（第二本笔记第 3 章）的具体页码未标：Berndt 原书未逐条给出 TIFR 页码，待查 TIFR 1957 年版目录后补。
8. Entry 10 的 (10.9)–(10.11) 逐项系数已按 PDF 原图 (p. 59) 记录，未逐项数值复核（(10.8) 已验）；引理 2–4 的证明细节未展开，只记陈述。

## 来源说明

- 底本：Bruce C. Berndt, *Ramanujan's Notebooks*, Part I, Springer, 1985, Ch. 3, pp. 44–84。archive.org 全文（`ramanujan_notebooks_i`）：DjVu OCR 文本（563,342 字节）与 PDF（13,201,802 字节，368 叶；**PDF 页 = 书页 + 10**，如书 p. 44 = PDF p. 54）。
- 核对方法：关键页均渲染成 150 DPI 图片逐字读过（书 pp. 45–50、53–67、69–84）；OCR 公式凡与图片或数值不符者一律纠正并注明；数值复核用 Python + mpmath（30 位），本章共复核 40 余项，见各条「数值复核」。
- IMSC 整理表计本章 86 条结果（第 1 章 43 条、第 2 章 68 条），该数为 IMSC 表的计数，Berndt 原书未逐章公布条目数。
- 本文件只收公式陈述与自写导读/证明思路，不照抄 Berndt 的正文与证明。
