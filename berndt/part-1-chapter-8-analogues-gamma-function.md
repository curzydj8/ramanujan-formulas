# Part I · 第 8 章 Analogues of the Gamma Function（Gamma 函数的类比）

出处：Bruce C. Berndt, *Ramanujan's Notebooks*, Part I, Springer, 1985, 第 8 章，pp. 181–231（第 7 章 pp. 150–181；第 9 章起自 p. 232）。对应拉马努金**第二本笔记第 8 章**。

## 背景与记号

- 本章主题：$\mathrm{Log}\,\Gamma(x+1)$ 的若干类比。Berndt 在章首导言（pp. 181–182）说明：前 14 节只占「12 页中的 $4\frac{1}{2}$ 页」（原文如此；结合上下文应指拉马努金笔记本原稿本章的页数——本书本章实为 pp. 181–231，共 51 页），第 17–24 节是本章重点，基本全是新结果；拉马努金研究 $\mathrm{Log}\,\Gamma(x+1)$ 的若干类比，含 Stirling 公式、Gauss 乘法定理、Kummer 公式 $\mathrm{Log}\,\Gamma(x)$ 的类比；第 9 章第 27–30 节继续此主题；与 Bendersky、Büsing 的 $\Gamma$ 推广相关；Post 的另一类推广与此无关。
- 本章的中心思想：$\Gamma(x+1)$ 的对数有 $\mathrm{Log}\,\Gamma(x+1) = \sum_{k=1}^{x} \mathrm{Log}\,k + \cdots$（Stirling 展开）；把求和式 $\sum_{k=1}^{x} \mathrm{Log}\,k$ 中的 $\mathrm{Log}\,k$ 换成 $1/k$、$\mathrm{Log}^2 k$、$\mathrm{Log}^n k$、$(\mathrm{Log}\,k)/k^r$、$(\mathrm{Log}^r k)/k$、$n^r k^{n-1}$ 等，就得到一族「$\mathrm{Log}\,\Gamma$ 的类比」：每种求和都有自己的渐近展开（Euler–Maclaurin 型）、乘法公式（Gauss 乘法定理的类比）、解析延拓（Hurwitz zeta 函数的导数）与 Fourier 展开（Kummer 公式的类比）。第 17–19 节是这条主线最系统的展开，第 20–24 节是它的变体与特例。
- **记号警告（本章最大的阅读陷阱）**：$\varphi$ 在几乎每节都被重新定义，含义随节而变，切勿跨节混用：
  - 第 3–16 节：$\varphi(x) = \psi(x+1) + \gamma = \Gamma'(x+1)/\Gamma(x+1) + \gamma$，即拉马努金视之为 $\sum_{k \le x} 1/k$ 的 digamma 类比（见 Entry 3 前的定义）；
  - 第 17 节：$\varphi(x) = \sum_{k=1}^{x} (\mathrm{Log}\,k)/k$（(17.1)，$\mathrm{Log}\,\Gamma$ 的直接类比）；
  - 第 18 节：$\varphi(x) = \sum_{k=1}^{x} \mathrm{Log}^2 k$（(18.1)）；
  - 第 19 节：$\varphi_n(x) = \sum_{k=1}^{x} \mathrm{Log}^n k$，$\psi_n(x) = \varphi_n(x) - c_n$（(19.2)）；
  - 第 20 节：$F_k(x) = k^x\varphi(x) = \sum_{n=1}^{x} n^r k^{n-1}$（(20.1)），$\varphi$ 另有含义；
  - 第 21 节：$\varphi_r(x) = \sum_{k=1}^{x} (\mathrm{Log}\,k)/k^r$（(21.1)）；
  - 第 22 节：$\varphi_r(x) = \sum_{k=1}^{x} (\mathrm{Log}^r k)/k$（(22.1)）；
  - 第 24 节：$\varphi(x) = \sum_{k=1}^{x} (\mathrm{Log}\,k)/\sqrt{k}$（(24.1)，即第 21 节 $r = 1/2$ 的情形），$\psi(x) = \sum_{k=1}^{\infty} \{1/\sqrt{k} - 1/\sqrt{k+x}\}$（(24.7)）。
  本文件每条都按该条所在的节注明 $\varphi$ 的含义。
- **常数记号同样有三套，不可混淆**：
  - 第 17 节的 $c_1$（(17.2)）：$c_1 = \lim_{n\to\infty}\{\varphi(n) - \frac12\mathrm{Log}^2 n\} = -0.072815845483677\ldots$，即第一 Stieltjes 常数 $\gamma_1$（见 Ch. 7 Entry 13）；
  - 第 19 节的 $c_n$（(19.1)）：$c_n = \lim_{x\to\infty}\{\sum_{k=1}^{x} \mathrm{Log}^n k - \int_1^{x} \mathrm{Log}^n t\,dt - \frac12\mathrm{Log}^n x + (-1)^{n+1}n!\}$，其中 $c_0 = -1/2$、$c_1 = \frac12\mathrm{Log}(2\pi)$、$c_2 = C$（第 18 节的常数），且 $c_n = (-1)^n\zeta^{(n)}(0)$（(19.18)）；
  - 第 22 节的 $c_r$（第 22 节）：$c_r = \lim_{x\to\infty}\{\varphi_r(x) - \mathrm{Log}^{r+1}x/(r+1)\}$，Stieltjes 型常数，$c_0 = \gamma$、$c_1 = \gamma_1$、$c_2 = \gamma_2$（符号约定 $c_r = (-1)^r\gamma_r$）。
  此外 $C_r(k)$ 在第 20 节 (i) 与 (iii) 中是**两个不同定义**（见 Entry 20(i) 与 Entry 20(iii)）。
- $\mathrm{Log}$ 为自然对数（拉马努金与 Berndt 的记法）；$\psi(x) = \Gamma'(x)/\Gamma(x)$ 为 digamma 函数；$\gamma = 0.577215664901533\ldots$ 为 Euler 常数（拉马努金记作 $c$）；$B_n$ 为 Bernoulli 数（当代定义，见 Ch. 5 Entry 9 与导言 (I1)；M01 伯努利数定义缺口仍待补，见文末）；$B_r^*$ 为第 5 章 Entry 25 定义的任意指标 Bernoulli 数；$\zeta(s,x)$ 为 Hurwitz zeta 函数；$\mathcal{L}f(x)$ 表示 $f(x)$ 的「对数部分」（第 19 节定义，见 Entry 19(i) 前）；$H_n(r) = \sum_{k=0}^{n} 1/(k+r)$（(21.2)），$H_n = H_n(1)$ 为调和数。
- 本章在原文中明确出现编号的 Entry 共 **23 条**：Entry 2–24。**没有 Entry 1**——章首（pp. 182–183）为未编号的开场白（$B_r^*$ 的极限与 $\gamma$、$e^{-\gamma}$ 的数值），随后直接是 Entry 2（与 Ch. 4 无 Entry 9、Ch. 6 无 Entry 5 与 Entry 13 的情形类似）。Berndt 未在章首给出本章公式或定理陈述的总数；IMSC 整理表计本章的结果数本次未能读取（imsc.res.in 当日不可达），待补。
- **本章的拉马努金原文疏失**（Berndt 已指出，详见各条与末尾小结）：开场白 $e^{-\gamma}$ 末位应为 7；Entry 5 右端被拉马努金错乘 $-1$；Entry 10 笔记本把 $1-u$ 错写成平方；例 13(vi)(b) 漏写一个求和号；Entry 14 (v) 分母与 $A_{10}$ 的 arctan 项与笔记本不符；例 14.1(iii) 漏写分母中的 $\sqrt{2}$；例 14.2(viii) 漏一项；Entry 16「the last term」应为「the first term」；Entry 17(i) $c_1$ 末两位应为 77；Entry 17(v) 原文表述无意义（级数发散）；Entry 18(ii) 例 2 拉马努金只问未给值（值见第一本笔记）；推论 19(iii) 1 拉马努金版右端多一个 $-c_n$；Entry 20(i) 原文不完整（多处缺失）；Entry 20(ii) 右端下标漏写；Entry 23 例 2 拉马努金值 0.9382 有小误差。
- **本轮发现的原书印文问题**（数值证实，详见末尾小结）：Entry 18(ii) 后例 1 的 $1/(24\pi^2)$ 应为 $\pi^2/24$；Entry 23 例 1、3、4 的 $M_n$ 值恰好 10 倍于真值（0.009940/0.014859/0.008541 应为 0.000994/0.001486/0.000854），书中「改进值」96.009940、24.014859、7680.008541 均错，拉马努金原值 96.001 反而精确到 $6\times 10^{-6}$。

## 本章结构

| Entry | 页 | 内容 |
|---|---|---|
| 开场白（未编号） | 182–183 | $B_r^*$ 的极限 $c_0 = \gamma$；$\gamma$、$e^{-\gamma}$ 的数值 |
| Entry 2 | 182 | $\sum_{k\le x} 1/k$ 的 Euler 渐近展开 |
| Entry 3 | 183 | $\sum_{k\le x} 1/k$ 的级数表示 (3.1)；$\varphi(x)$ 延拓到一切实数 $x$ |
| Entry 4 | 183 | $|x|<1$ 时的幂级数 (4.1)；digamma 公式 (4.2) |
| Entry 5 | 183 | $\pi\cot(\pi x)$ 的部分分式展开 (5.1)；拉马努金符号错误 |
| Entry 6 | 184–185 | Gauss 乘法定理的 digamma 形式；推论 1–4（$\psi$ 的特殊值） |
| Entry 7 | 185 | $\psi(a/b+x+1) - \psi(a/b+1)$ 的有限和 |
| Entry 8 | 185 | $\psi$ 的交错级数表示 |
| Entry 9 | 185 | $\psi(1/(2x)+1)$ 的积分表示 (9.1) |
| Entry 10 | 186 | $\psi(1-1/x)$ 的积分表示；Re $x<0$ |
| Entry 11 | 186 | $\psi(1/x) + \psi(1-1/x) = -2\gamma - x\phi(x)$；$\phi$ 的定义 (11.1) |
| Entry 12 | 186 | $\phi(x)-1$ 的积分表示 |
| Entry 13 | 187–189 | $\phi(2x)$ 的函数方程 (13.1)；例 13(i)–(vi)（有理函数初等积分） |
| Entry 14 | 189–193 | $A_n = \int_0^x du/(1+u^n)$，$n = 1,2,3,4,5,6,8,10$；例 14.1、14.2 |
| Entry 15 | 194–195 | $\Gamma(x+1)$ 的渐近与最小值点；拉马努金插值 6/13 |
| Entry 16 | 196 | $\gamma$ 的一个级数表示 (16.1)；曾作 JIMS 投稿题 |
| Entry 17(i) | 196–197 | $\varphi(x) = \sum (\mathrm{Log}\,k)/k$ 的渐近；常数 $c_1 = \gamma_1$ |
| Entry 17(ii) | 197–198 | $\varphi(x)$ 的级数延拓 (17.7)；推论（交错对数和） |
| Entry 17(iii) | 198–199 | $\varphi$ 的乘法公式；推论 (17.8)；例 1–5 |
| Entry 17(iv) | 199 | Kummer 公式的类比（正弦级数） |
| Entry 17(v) | 200–201 | (17.11)（形式推导，原文表述无意义）；例 1–3 |
| Entry 18(i) | 202–204 | $\varphi(x) = \sum \mathrm{Log}^2 k$ 的渐近；常数 $C$；$\zeta''(0)$ |
| Entry 18(ii) | 204–208 | $\varphi$（$\mathrm{Log}^2$ 版）的乘法公式 (18.16)；例 1、2 |
| Entry 18(iii) | 208–209 | $\varphi(x-1)+\varphi(-x)$ 的余弦级数 (18.19) |
| Entry 19(i) | 210 | 「对数部分」$\mathcal{L}\psi_n(x)$ 的递推 (19.3) |
| Entry 19(ii) | 210–214 | $\psi_n$ 的渐近展开 (19.7)；Faà di Bruno 行列式；解析延拓 (19.16)(19.17) |
| Entry 19(iii) | 215–216 | $\psi_n$ 的乘法公式 (19.19)；推论 1、2 |
| Entry 20(i) | 216–217 | $F_k(x) = \sum n^r k^{n-1}$ 的渐近 (20.2)；原文不完整 |
| Entry 20(ii) | 217 | $C_r(k)$ 与 $\psi_r$ 的关系；延拓 (20.8) |
| Entry 20(iii) | 218 | $F_k$ 的乘法公式 (20.9)；推论 |
| Entry 21(i) | 218–220 | $\varphi_r(x) = \sum (\mathrm{Log}\,k)/k^r$ 的渐近 (21.3)；延拓 (21.10) |
| Entry 21(ii) | 220 | $\varphi_r(x)$ 的幂级数展开 |
| Entry 21(iii) | 221 | $\varphi_r$ 的乘法公式；推论 |
| Entry 22(i) | 221 | $\varphi_r(x) = \sum (\mathrm{Log}^r k)/k$；常数 $c_r$（Stieltjes 型） |
| Entry 22(ii) | 222 | $\varphi_r$ 的乘法公式 (22.3) |
| Entry 23 | 223–226 | $\zeta^{(r)}(s+1)$ 的 Taylor 展开 (23.1)；例 1–5（数值） |
| Entry 24(i) | 226 | $\varphi(x) = \sum (\mathrm{Log}\,k)/\sqrt{k}$ 的级数延拓 (24.2) |
| Entry 24(ii) | 226–227 | $\varphi$（$r=1/2$ 版）的渐近；常数 $c = 3.92265$；$\zeta'(1/2) = -c$ |
| Entry 24(iii) | 228 | $\varphi$（$r=1/2$ 版）的乘法公式；$\psi(x)$ 的定义 (24.7) |
| Entry 24(iv) | 228 | $\varphi(x-1)+\varphi(-x)$ 的余弦级数 |
| Entry 24(v) | 229 | $\varphi(x-1)-\varphi(-x)$ 的正弦级数 |
| 例 1、2 | 229–231 | $\varphi(-1/2)$ 等值的讨论；$c$ 的半收敛级数 (24.13) |

## 开场白——$B_r^*$ 的极限与 $\gamma$（未编号）

**陈述。**设 $B_r^*$ 为第 5 章 Entry 25 定义的任意指标 Bernoulli 数。则
$$\lim_{r\to 0}\left\{\frac{B_r^*\cos(\frac12\pi r)}{r} + \frac{1}{r}\right\} = c_0 = \gamma,$$
其中 $\gamma = 0.577215664901533\ldots$ 为 Euler 常数。拉马努金并给出 $e^{-\gamma} = 0.56145948356$，**末位应为 7**（Berndt 注）：真值 $e^{-\gamma} = 0.5614594835668857\ldots$。

**出处。**Berndt Part I, Ch. 8, pp. 182–183（开场白，未编号）。

**状态。**已证明（由 Ch. 7 Entry 1 的 (1.7)(1.8) 与 $\zeta(s)$ 在 $s = 1$ 的 Laurent 展开）。数值复核：$e^{-\gamma} = 0.5614594835668857$（mpmath 30 位）。

**对照。**$B_r^*$ 的定义见 M01（Ch. 5 Entry 25）；$\gamma$ 的定义与数值见 M01、M12；$e^{-\gamma}$ 的常数见 M12。

## Entry 2——调和和的 Euler 渐近展开

**陈述。**当 $x \to \infty$ 时，
$$\sum_{k\le x} \frac{1}{k} \sim \mathrm{Log}\,x + \gamma - \sum_{k=1}^{\infty} \frac{B_k}{k x^k},$$
其中 $B_k$ 为 Bernoulli 数。这是 Euler 的经典渐近展开（Ch. 7 Entry 1 的 $r = -1$ 情形，见该章注）。

**出处。**Berndt Part I, Ch. 8, Entry 2, p. 182。

**状态。**已证明（Euler–Maclaurin 公式）。

**对照。**调和数的渐近展开见 M12（Euler–Maclaurin 公式）；Bernoulli 数见 M01（定义出处 Ch. 5 Entry 9，M01 定义缺口仍待补）。

## Entry 3——$\sum_{k\le x} 1/k$ 的级数表示

**陈述。**
$$\sum_{k\le x} \frac{1}{k} = \sum_{k=1}^{\infty} \left\{\frac{1}{k} - \frac{1}{k+x}\right\} = x\sum_{k=1}^{\infty} \frac{1}{k(k+x)}. \qquad (3.1)$$
以此把 $\varphi(x) = \psi(x+1) + \gamma$ 定义到一切实数 $x$（$x$ 为负整数时除外），即本章第 3–16 节的 $\varphi$。

**出处。**Berndt Part I, Ch. 8, Entry 3, p. 183。

**状态。**已证明（(3.1) 右端级数在 $x$ 不为负整数时收敛；$x$ 为正整数时化为调和数）。

**对照。**digamma 函数 $\psi$ 与调和数见 M10、M12；本章 $\varphi$ 的记号约定见「背景与记号」。

## Entry 4——$|x|<1$ 时的幂级数

**陈述。**$|x| < 1$ 时，
$$\sum_{k\le x} \frac{1}{k} = \sum_{k=1}^{\infty} (-1)^{k+1}\zeta(k+1)x^k. \qquad (4.1)$$
配 digamma 公式
$$\frac{\Gamma'(x+1)}{\Gamma(x+1)} + \gamma = \sum_{k=1}^{\infty} \left\{\frac{1}{k} - \frac{1}{k+x}\right\}. \qquad (4.2)$$
(4.2) 与 Ch. 6 第 6 节例 2 相同。

**出处。**Berndt Part I, Ch. 8, Entry 4, p. 183。

**状态。**已证明（(4.1) 由 $\zeta(k+1)$ 的级数定义逐项求和；(4.2) 是 digamma 函数的标准级数表示）。

**对照。**digamma 函数的级数表示见 M10；$\zeta(k+1)$ 的值见 M01。

## Entry 5——$\pi\cot(\pi x)$ 的部分分式展开

**陈述。**
$$\sum_{k=1}^{\infty} \left\{\frac{1}{k-1+x} - \frac{1}{k-x}\right\} = \pi\cot(\pi x). \qquad (5.1)$$
**拉马努金把右端错乘了 $-1$**（Berndt 注）。配公式
$$\frac{\Gamma'(x)}{\Gamma(x)} - \frac{\Gamma'(1-x)}{\Gamma(1-x)} = -\pi\cot(\pi x). \qquad (5.2)$$

**出处。**Berndt Part I, Ch. 8, Entry 5, p. 183。

**状态。**已证明（订正后；(5.1) 是 $\pi\cot\pi x$ 的经典部分分式展开）。数值复核：$x = 1/4$ 时 (5.1) 左端部分和（$10^6$ 项）$= \pi$，误差 0（在双精度舍入内）。

**对照。**$\pi\cot\pi x$ 的部分分式展开见 M02、M10（Ch. 7 Entry 11 的 (11.1) 为其导数形式）。

## Entry 6——Gauss 乘法定理的 digamma 形式

**陈述。**设 $n$ 为正整数，则
$$n\psi(x+1) - \sum_{k=0}^{n-1}\psi\left(\frac{x+k+1}{n}\right) = n\,\mathrm{Log}\,n.$$
这是 Gauss 乘法定理 $\Gamma(x+1)\Gamma(x+2/n)\cdots$ 的对数微分形式。

**推论 1。**当 $x \to \infty$ 时，
$$\psi\left(x+\frac12\right) \sim \mathrm{Log}\,x + \sum_{k=1}^{\infty} \frac{B_{2k}(1-2^{1-2k})}{2k x^{2k}}, \qquad |\arg x| < \pi.$$

**推论 2。**设 $n$ 为正整数，则
$$\sum_{k=1}^{n-1}\psi\left(\frac{k}{n}\right) = -(n-1)\gamma - n\,\mathrm{Log}\,n. \qquad (6.1)$$

**推论 3。**$\psi$ 在 $1/2, 1/3, 1/4, 1/6$ 的值：
$$\psi\left(\frac12\right) = -\gamma - 2\mathrm{Log}\,2, \qquad \psi\left(\frac13\right) = -\gamma - \frac32\mathrm{Log}\,3 - \frac{\pi}{2\sqrt{3}},$$
$$\psi\left(\frac14\right) = -\gamma - 3\mathrm{Log}\,2 - \frac{\pi}{2}, \qquad \psi\left(\frac16\right) = -\gamma - 2\mathrm{Log}\,2 - \frac32\mathrm{Log}\,3 - \frac{\pi\sqrt{3}}{2},$$
$$3\psi\left(\frac12\right) - 2\psi\left(\frac14\right) = -\gamma + \pi.$$

**推论 4。**设 $n$ 为正整数，则
$$\sum_{k=1}^{n}\psi\left(\frac{2k-1}{2n}\right) = -n\gamma - n\,\mathrm{Log}(4n).$$

**出处。**Berndt Part I, Ch. 8, Entry 6, pp. 184–185。

**状态。**已证明。数值复核：推论 3 五式用 mpmath 30 位复核，误差 $\le 10^{-30}$。

**对照。**Gauss 乘法定理见 M10（Ch. 7 Entry 25 为 $\Gamma$ 形式）；$\psi(1/2)$ 等特殊值见 M10；Bernoulli 数见 M01。

## Entry 7——$\psi$ 的有限和

**陈述。**设 $a, b$ 为正实数，$x$ 为正整数，则
$$\psi\left(\frac{a}{b} + x + 1\right) - \psi\left(\frac{a}{b} + 1\right) = b\sum_{k=1}^{x} \frac{1}{a+bk}.$$

**出处。**Berndt Part I, Ch. 8, Entry 7, p. 185。

**状态。**已证明（由 $\psi(z+1) - \psi(z) = 1/z$ 递推）。

**对照。**digamma 函数的递推见 M10；等差数列倒数和见 M02。

## Entry 8——$\psi$ 的交错级数表示

**陈述。**设 $a, b$ 为正实数，则
$$\psi\left(\frac{a+2b}{2b}\right) - \psi\left(\frac{a+b}{2b}\right) = 2b\sum_{k=1}^{\infty} \frac{(-1)^{k+1}}{a+bk}.$$

**出处。**Berndt Part I, Ch. 8, Entry 8, p. 185。

**状态。**已证明（由 Entry 7 令 $x \to \infty$ 并用交错级数求和）。

**对照。**交错级数与 digamma 函数见 M02、M10。

## Entry 9——$\psi(1/(2x)+1)$ 的积分表示

**陈述。**Re $x > 0$ 时，
$$\psi\left(\frac{1}{2x}+1\right) = \psi\left(\frac{1}{x}+1\right) - \mathrm{Log}\,2 + x\int_0^1 \frac{u^x}{1+u^x}\,du. \qquad (9.1)$$

**出处。**Berndt Part I, Ch. 8, Entry 9, p. 185。

**状态。**已证明。

**对照。**$\psi$ 的积分表示见 M09、M10。

## Entry 10——$\psi(1-1/x)$ 的积分表示

**陈述。**Re $x < 0$ 时，
$$\psi\left(1-\frac{1}{x}\right) + \gamma = -x\int_0^1 \frac{1-u}{u(u^x-1)}\,du.$$
该积分在 Re $x > 0$ 时发散。**拉马努金在笔记本 p. 92 把被积函数中的 $1-u$ 错写成平方**（Berndt 注）。

**出处。**Berndt Part I, Ch. 8, Entry 10, p. 186；笔记本出处：第二本笔记 p. 92。

**状态。**已证明（订正后）。

**对照。**$\psi$ 的积分表示见 M09、M10。

## Entry 11——$\psi(1/x) + \psi(1-1/x)$ 与 $\phi(x)$

**陈述。**记
$$\phi(x) = 1 + \sum_{k=1}^{\infty} \frac{2}{(kx)^3-kx}. \qquad (11.1)$$
则
$$\psi\left(\frac{1}{x}\right) + \psi\left(1-\frac{1}{x}\right) = -2\gamma - x\phi(x).$$
注意此处的 $\phi(x)$（(11.1)）与本章各节的 $\varphi(x)$ 是不同的函数；$\phi$ 的有理值见 Entry 14 的例 14.2。

**出处。**Berndt Part I, Ch. 8, Entry 11, p. 186。

**状态。**已证明。数值复核：$x = 2$ 时，用 $\phi(2) = 2\mathrm{Log}\,2$（例 14.2(i)）代入，左右两端在 30 位精度下一致。

**对照。**$\phi(x)$ 的有理值见本章 Entry 14 例 14.2；digamma 函数的反射公式见 M10。

## Entry 12——$\phi(x)-1$ 的积分表示

**陈述。**Re $x > 1$ 时，
$$\int_0^1 \frac{u^{x-2}(1-u)^2}{1-u^x}\,du = \phi(x)-1,$$
其中 $\phi(x)$ 如 (11.1)。

**出处。**Berndt Part I, Ch. 8, Entry 12, p. 186。

**状态。**已证明。

**对照。**$\phi$ 函数见 Entry 11；积分表示见 M09。

## Entry 13——$\phi(2x)$ 的函数方程与有理函数积分

**陈述。**Re $x > 0$ 时，
$$\phi(2x) - \frac12\phi(x) - \frac{1}{x}\mathrm{Log}\,2 = 1 - \frac{\pi}{2x}\csc\left(\frac{\pi}{x}\right) - \int_0^1 \frac{u^x}{1+u^x}\,du. \qquad (13.1)$$
**拉马努金在笔记本 p. 92 右端写的是「$\sum_{k=0}^{\infty} (-1)^k/(kx+1)$ 的对数部分」**（Berndt 注，即 (13.1) 右端末项的另一种表述）。

**例 13(i)。**$|x| < 1$、Re $n > 0$ 时，
$$\int_0^x \frac{du}{1+u^n} = \sum_{k=0}^{\infty} \frac{(-1)^k x^{nk+1}}{nk+1}.$$

**例 13(ii)。**$|x| < 1$、Re $n > 0$ 时，
$$\int_0^x \frac{du}{1-u^n} = \sum_{k=0}^{\infty} \frac{x^{nk+1}}{nk+1}.$$

**例 13(iii)。**$n$ 为奇数时，$\int_0^x du/(1-u^n) = \int_0^x du/(1+(-u)^n)$。

**例 13(iv)。**$n$ 为偶数时，
$$\int_0^x \frac{du}{1-u^n} = \frac12\int_0^x \frac{du}{1+u^{n/2}} + \frac12\int_0^x \frac{du}{1-u^{n/2}}.$$

**例 13(v)。**设 $n$ 为偶数，$1 \le l \le n$，则
$$\int \frac{x^{l-1}dx}{x^n-1} = \frac1n\mathrm{Log}(x-1) + \frac{(-1)^l}{n}\mathrm{Log}(x+1) + \frac1n\sum_{r=1}^{\frac12n-1}\cos\left(\frac{2rl\pi}{n}\right)\mathrm{Log}\left(x^2-2x\cos\frac{2r\pi}{n}+1\right) - \frac2n\sum_{r=1}^{\frac12n-1}\sin\left(\frac{2rl\pi}{n}\right)\tan^{-1}\left(\frac{x-\cos(2r\pi/n)}{\sin(2r\pi/n)}\right).$$
设 $n$ 为奇数，$1 \le l \le n$，则
$$\int \frac{x^{l-1}dx}{x^n+1} = \frac{(-1)^{l-1}}{n}\mathrm{Log}(x+1) - \frac1n\sum_{r=1}^{\frac12(n-1)}\cos\left(\frac{(2r-1)l\pi}{n}\right)\mathrm{Log}\left(x^2-2x\cos\frac{(2r-1)\pi}{n}+1\right) + \frac2n\sum_{r=1}^{\frac12(n-1)}\sin\left(\frac{(2r-1)l\pi}{n}\right)\tan^{-1}\left(\frac{x-\cos((2r-1)\pi/n)}{\sin((2r-1)\pi/n)}\right).$$

**例 13(vi)。**设 $n$ 为奇数，$1 \le l \le n$，则
$$\int \frac{x^{l-1}dx}{x^n-1} = \frac1n\mathrm{Log}(x-1) + \frac1n\sum_{r=1}^{\frac12(n-1)}\cos\left(\frac{2rl\pi}{n}\right)\mathrm{Log}\left(x^2-2x\cos\frac{2r\pi}{n}+1\right) - \frac2n\sum_{r=1}^{\frac12(n-1)}\sin\left(\frac{2rl\pi}{n}\right)\tan^{-1}\left(\frac{x-\cos(2r\pi/n)}{\sin(2r\pi/n)}\right).$$
设 $n$ 为偶数，$1 \le l \le n$，则
$$\int \frac{x^{l-1}dx}{x^n+1} = -\frac1n\sum_{r=1}^{\frac12n}\cos\left(\frac{(2r-1)l\pi}{n}\right)\mathrm{Log}\left(x^2-2x\cos\frac{(2r-1)\pi}{n}+1\right) + \frac2n\sum_{r=1}^{\frac12n}\sin\left(\frac{(2r-1)l\pi}{n}\right)\tan^{-1}\left(\frac{x-\cos((2r-1)\pi/n)}{\sin((2r-1)\pi/n)}\right).$$
**拉马努金在例 13(vi)(b)（即上式）漏写了后一个求和号**（Berndt 注）。

**出处。**Berndt Part I, Ch. 8, Entry 13, pp. 187–189；笔记本出处：第二本笔记 p. 92（(13.1) 右端的表述）。

**状态。**已证明（订正后）。数值复核：(13.1) 在 $x = 2$ 时两边均为 0（左端 $\phi(4) - \frac12\phi(2) - \frac12\mathrm{Log}\,2 = \frac32\mathrm{Log}\,2 - \mathrm{Log}\,2 - \frac12\mathrm{Log}\,2 = 0$；右端 $1 - \frac{\pi}{4}\csc(\pi/2) - \int_0^1 u^2/(1+u^2)\,du = 1 - \pi/4 - (1 - \pi/4) = 0$），误差 0。

**对照。**有理函数的初等积分见 M09；$\phi$ 的有理值见 Entry 14 例 14.2；部分分式与 $\tan^{-1}$、$\mathrm{Log}$ 的组合见 M09、M13。

## Entry 14——$A_n = \int_0^x du/(1+u^n)$ 的显式公式

**陈述。**设 $A_n = \int_0^x du/(1+u^n)$，$n \ge 1$。则

(i) $A_1 = \mathrm{Log}(1+x)$；

(ii) $A_2 = \tan^{-1}x$；

(iii) $A_3 = \frac16\mathrm{Log}\left(\frac{(1+x)^3}{1+x^3}\right) + \frac{1}{\sqrt{3}}\tan^{-1}\left(\frac{x\sqrt{3}}{2-x}\right)$；

(iv) $A_4 = \frac{1}{4\sqrt{2}}\mathrm{Log}\left(\frac{1+x\sqrt{2}+x^2}{1-x\sqrt{2}+x^2}\right) + \frac{1}{2\sqrt{2}}\tan^{-1}\left(\frac{x\sqrt{2}}{1-x^2}\right)$；

(v) $A_5 = \frac{1}{20}\mathrm{Log}\left(\frac{(1+x)^5}{1+x^5}\right) + \frac{1}{4\sqrt{5}}\mathrm{Log}\left(\frac{1+\frac12x(\sqrt{5}-1)+x^2}{1-\frac12x(\sqrt{5}+1)+x^2}\right) + \frac{1}{10}\sqrt{10+2\sqrt{5}}\tan^{-1}\left(\frac{x\sqrt{10+2\sqrt{5}}}{4+x(\sqrt{5}-1)}\right) + \frac{1}{10}\sqrt{10-2\sqrt{5}}\tan^{-1}\left(\frac{x\sqrt{10-2\sqrt{5}}}{4-x(\sqrt{5}+1)}\right)$；

(vi) $A_6 = \frac12\tan^{-1}x + \frac16\tan^{-1}x^3 + \frac{1}{4\sqrt{3}}\mathrm{Log}\left(\frac{1+x\sqrt{3}+x^2}{1-x\sqrt{3}+x^2}\right)$；

(vii) $A_8 = \frac{\sqrt{2+\sqrt{2}}}{16}\left\{\mathrm{Log}\left(\frac{1+x\sqrt{2+\sqrt{2}}+x^2}{1-x\sqrt{2+\sqrt{2}}+x^2}\right) + 2\tan^{-1}\left(\frac{x\sqrt{2+\sqrt{2}}}{1-x^2}\right)\right\} + \frac{\sqrt{2-\sqrt{2}}}{16}\left\{\mathrm{Log}\left(\frac{1+x\sqrt{2-\sqrt{2}}+x^2}{1-x\sqrt{2-\sqrt{2}}+x^2}\right) + 2\tan^{-1}\left(\frac{x\sqrt{2-\sqrt{2}}}{1-x^2}\right)\right\}$；

(viii) $A_{10} = \frac15\tan^{-1}x + \frac{\sqrt{6+2\sqrt{5}}}{20}\tan^{-1}\left(\frac{x\sqrt{6+2\sqrt{5}}}{2(1-x^2)}\right) + \frac{\sqrt{6-2\sqrt{5}}}{20}\tan^{-1}\left(\frac{x\sqrt{6-2\sqrt{5}}}{2(1-x^2)}\right) + \frac{\sqrt{10+2\sqrt{5}}}{40}\mathrm{Log}\left(\frac{1+\frac12x\sqrt{10+2\sqrt{5}}+x^2}{1-\frac12x\sqrt{10+2\sqrt{5}}+x^2}\right) + \frac{\sqrt{10-2\sqrt{5}}}{40}\mathrm{Log}\left(\frac{1+\frac12x\sqrt{10-2\sqrt{5}}+x^2}{1-\frac12x\sqrt{10-2\sqrt{5}}+x^2}\right)$。

（无 $A_7$、$A_9$。）与拉马努金本（第二本笔记 p. 94）两处不符（Berndt 注）：(v) 第二式分母拉马努金写 $\frac12(\sqrt{5}-1)$，应为 $\frac12(\sqrt{5}+1)$；$A_{10}$ 拉马努金把三个 arctan 项换成 $\frac14\tan^{-1}x - \frac{1}{20}\tan^{-1}x^5 + \frac{1}{4\sqrt{5}}\tan^{-1}\left(\frac{(x-x^3)\sqrt{5}}{1-3x^2+x^4}\right)$。

**例 14.1。**(i) $\sum_{k=0}^{\infty} \frac{(-1)^k}{(3k+1)2^{3k+1}} = \frac{\pi}{6\sqrt{3}} + \frac16\mathrm{Log}\,3$；(ii) $\sum_{k=0}^{\infty} \frac{(-1)^k(\sqrt{3}-1)^{3k+1}}{3k+1} = \frac{\pi}{4\sqrt{3}} + \frac13\mathrm{Log}\left(\frac{1+\sqrt{3}}{\sqrt{2}}\right)$；(iii) $\sum_{k=0}^{\infty} \frac{(-1)^k(2-\sqrt{3})^{2k+1}}{4k+1} = \frac{(\sqrt{3}-1)\pi}{16} - \frac{\sqrt{3}-1}{4}\mathrm{Log}\left(\frac{\sqrt{3}-1}{\sqrt{2}}\right)$。**拉马努金在 (iii) 右端漏写了分母中的 $\sqrt{2}$**（Berndt 注）。

**例 14.2。**$\phi$（(11.1)）的有理值：(i) $\phi(2) = 2\mathrm{Log}\,2$；(ii) $\phi(3) = \mathrm{Log}\,3$；(iii) $\phi(4) = \frac32\mathrm{Log}\,2$；(iv) $\phi(6) = \frac12\mathrm{Log}\,3 + \frac13\mathrm{Log}\,4$；(v) $\phi(5) = \frac12\mathrm{Log}\,5 + \frac{1}{\sqrt{5}}\mathrm{Log}\left(\frac{\sqrt{5}+1}{2}\right)$；(vi) $\phi(8) = \mathrm{Log}\,2 + \frac{\sqrt{2}}{4}\mathrm{Log}(\sqrt{2}+1)$；(vii) $\phi(10)$；(viii) $\phi(12)$；(ix) $\phi(16)$；(x) $\phi(20)$。**拉马努金在 (viii) 的表述中漏了 $(\sqrt{3}/6)\mathrm{Log}\,2$ 一项**（Berndt 注，笔记本 p. 95）。

**出处。**Berndt Part I, Ch. 8, Entry 14, pp. 189–193；笔记本出处：第二本笔记 p. 94（$A_n$ 公式）、p. 95（例 14.2）。

**状态。**已证明（订正后）。数值复核：$A_3$–$A_{10}$ 六式在 $x = 0.7$ 时与数值积分对照，误差 $\le 10^{-18}$；例 14.1 三式与例 14.2 前八值（$\phi(2)$、$\phi(3)$、$\phi(4)$、$\phi(6)$、$\phi(5)$、$\phi(8)$、$\phi(10)$、$\phi(12)$）用 mpmath 30 位复核全部通过。

**对照。**$\int du/(1+u^n)$ 的初等积分见 M09；$\phi$ 的定义见 Entry 11；$\mathrm{Log}$ 与 $\tan^{-1}$ 的组合见 M09、M02。

## Entry 15——$\Gamma(x+1)$ 的渐近与最小值点

**陈述。**设 $\mathrm{Log}\,a = \psi(x+1)$（(15.1)，即 $a = e^{\psi(x+1)}$），则
$$\left(\frac{x+\frac12}{a}\right)^{4n} \sim 1 - \frac{n}{6a^2} + \frac{10n^2+11n}{720a^4} - \frac{70n^3+231n^2+891n}{90720a^6} + \cdots. \qquad (15.2)$$

**推论。**「$\Gamma(x+1)$ 在 $x = 6/13$ 附近取最小值。」$\Gamma(x+1)$ 的真最小值点为 $x_0 = 0.4616321\ldots$（$x_0$ 是 $\psi(x+1) = 0$ 的根）；拉马努金的插值 $6/13 = 0.4615384$ 优于 $11/24 = 0.4583333$ 与 $889/1920 = 0.4630208$ 两个近似（Berndt 注）。

**出处。**Berndt Part I, Ch. 8, Entry 15, pp. 194–195；笔记本出处：第二本笔记 p. 95。

**状态。**已证明。数值复核：(15.2) 在 $n = 1$、$x = 10$ 时三项近似误差 $1.5\times 10^{-9}$；最小值点用 findroot 得 $x_0 = 0.461632144968$。

**对照。**$\Gamma$ 函数的最小值与 Stirling 公式见 M10、M12；$\psi(x+1) = 0$ 的根见 M10。

## Entry 16——$\gamma$ 的一个级数表示

**陈述。**设 $A_k = \frac12(3^k-1)$，则
$$\gamma = \mathrm{Log}\,2 - 2\sum_{k=1}^{\infty} k\sum_{j=A_{k-1}+1}^{A_k} \frac{1}{(3j)^3-3j}. \qquad (16.1)$$
**拉马努金「the last term …」应为「the first term …」**（Berndt 注）。(16.1) 曾作为向 *Journal of the Indian Mathematical Society* 提交的问题，从未发表解答（Berndt 注）。

**出处。**Berndt Part I, Ch. 8, Entry 16, p. 196；笔记本出处：第二本笔记 p. 95。

**状态。**已证明（Berndt 在此给出证明；该级数收敛很慢）。数值复核：$k \le 8$ 的部分和与 $\gamma$ 之差 $3.1\times 10^{-8}$（$k \le 6$ 时差 $2\times 10^{-6}$）。

**对照。**Euler 常数 $\gamma$ 的级数表示见 M01、M12；JIMS 投稿问题见 notebooks.md。

## Entry 17(i)——$\varphi(x) = \sum (\mathrm{Log}\,k)/k$ 的渐近

**陈述。**本节的 $\varphi(x) = \sum_{k=1}^{x} (\mathrm{Log}\,k)/k$（(17.1)，即 $\mathrm{Log}\,\Gamma$ 的直接类比：把 $\sum \mathrm{Log}\,k$ 中的 $\mathrm{Log}\,k$ 换成 $(\mathrm{Log}\,k)/k$）。设
$$c_1 = \lim_{n\to\infty}\left\{\varphi(n) - \frac12\mathrm{Log}^2 n\right\}, \qquad (17.2)$$
$$H_n = \sum_{k=1}^{n} \frac{1}{k}. \qquad (17.3)$$
则当 $x \to \infty$ 时，
$$\varphi(x) - \psi(x+1)\mathrm{Log}\,x \sim -\frac12\mathrm{Log}^2 x + c_1 + \sum_{k=1}^{\infty} \frac{B_{2k}H_{2k-1}}{2k x^{2k}}.$$
**拉马努金给 $c_1 = -0.072815845483680$，与 Liang–Todd 的计算相比末两位应为 77 而非 80**（Berndt 注）：$c_1 = -0.072815845483676724\ldots$，即第一 Stieltjes 常数 $\gamma_1$（见 Ch. 7 Entry 13）。

**推论。**
$$\lim_{x\to\infty}\left\{\varphi(x) - \frac12\psi^2(x+1)\right\} = c_1.$$

**出处。**Berndt Part I, Ch. 8, Entry 17(i), pp. 196–197。

**状态。**已证明。数值复核：渐近式在 $x = 2000$ 时成立（mpmath 30 位）；$c_1$ 用 Stieltjes 常数 $\gamma_1$ 复核通过。

**对照。**Stieltjes 常数 $\gamma_1$ 见 M01（Ch. 7 Entry 13）；Euler–Maclaurin 渐近见 M12；$\mathrm{Log}\,\Gamma$ 的类比主线见 M10。

## Entry 17(ii)——$\varphi(x)$ 的级数延拓

**陈述。**本节的 $\varphi(x) = \sum_{k=1}^{x} (\mathrm{Log}\,k)/k$ 有延拓
$$\varphi(x) = \sum_{k=1}^{\infty} \left\{\frac{\mathrm{Log}\,k}{k} - \frac{\mathrm{Log}(k+x)}{k+x}\right\}. \qquad (17.7)$$

**推论。**
$$\sum_{k=0}^{\infty} (-1)^k\frac{\mathrm{Log}(2k+1)}{2k+1} = \frac14\left\{\varphi\left(-\frac14\right) - \varphi\left(-\frac34\right)\right\} + \frac12\pi\,\mathrm{Log}\,2.$$

**出处。**Berndt Part I, Ch. 8, Entry 17(ii), pp. 197–198。

**状态。**已证明。数值复核：推论左端交错级数（$2\times 10^5$ 项）$= -0.192917440822$，右端（由 (17.7) 直接求和）$= -0.192901316797$，差 $1.6\times 10^{-5}$（交错级数尾项量级，见「数值复核小结」）。

**对照。**Hurwitz zeta 函数的延拓见 M01、M10；交错对数级数见 M02。

## Entry 17(iii)——$\varphi$ 的乘法公式

**陈述。**本节的 $\varphi(x) = \sum_{k=1}^{x} (\mathrm{Log}\,k)/k$ 满足乘法公式（Gauss 乘法定理的类比）
$$n\varphi(x) - \sum_{k=0}^{n-1}\varphi\left(\frac{x-k}{n}\right) = n\,\mathrm{Log}\,n\,\psi(x+1) - \frac12 n\,\mathrm{Log}^2 n.$$

**推论。**
$$\sum_{k=1}^{n-1}\varphi\left(-\frac{k}{n}\right) = \gamma n\,\mathrm{Log}\,n + \frac12 n\,\mathrm{Log}^2 n. \qquad (17.8)$$

**例 1。**$\prod_{k=1}^{\infty} \frac{(2k-1)^{1/(2k-1)}}{(2k)^{1/(2k)}} = 2^{\frac12\mathrm{Log}\,2 - \gamma}$。

**例 2。**$\varphi\left(-\frac12\right) = 2\gamma\,\mathrm{Log}\,2 + \mathrm{Log}^2 2$。

**例 3。**$\varphi\left(-\frac13\right) + \varphi\left(-\frac23\right) = 3\gamma\,\mathrm{Log}\,3 + \frac32\mathrm{Log}^2 3$。

**例 4。**$\varphi\left(-\frac14\right) + \varphi\left(-\frac34\right) = 6\gamma\,\mathrm{Log}\,2 + 7\mathrm{Log}^2 2$。

**例 5。**$\varphi\left(-\frac16\right) + \varphi\left(-\frac56\right) = 3\gamma\,\mathrm{Log}\,3 + 4\gamma\,\mathrm{Log}\,2 + \frac32\mathrm{Log}^2(12) - \mathrm{Log}^2 4$。

**出处。**Berndt Part I, Ch. 8, Entry 17(iii), pp. 198–199。

**状态。**已证明。数值复核：推论 (17.8) 在 $n = 2, 3, 4, 6$ 时由 (17.7) 直接求和（$2\times 10^6$ 项 + 尾项 $x\mathrm{Log}\,N/N$ 修正）复核，误差 $\le 2\times 10^{-12}$；例 2–5 同法复核，误差 $\le 10^{-12}$。

**对照。**Gauss 乘法定理的类比见 M10；$\varphi(-1/2)$ 等值见 Entry 17(ii) 推论；无穷乘积见 M02。

## Entry 17(iv)——Kummer 公式的类比（正弦级数）

**陈述。**$0 < x < 1$ 时，
$$\frac{1}{2\pi}\left\{\mathrm{Log}\left(\frac{\Gamma(x)}{\Gamma(1-x)}\right) + (\gamma+\mathrm{Log}(2\pi))(2x-1)\right\} = \sum_{k=1}^{\infty} \frac{\mathrm{Log}\,k}{k}\sin(2\pi kx).$$
这是 Kummer 公式 $\mathrm{Log}\,\Gamma(x)$ 的类比（Kummer 公式本身见 Ch. 7 Entry 15）。

**出处。**Berndt Part I, Ch. 8, Entry 17(iv), p. 199。

**状态。**已证明（由 Hurwitz 公式）。

**对照。**Kummer 公式见 M10（Ch. 7 Entry 15）；Fourier 级数见 M02、M12。

## Entry 17(v)——(17.11)（形式推导）

**陈述。**
$$\varphi(x-1) - \varphi(-x) = (\gamma+\mathrm{Log}(2\pi))\pi\cot(\pi x) + 2\pi\sum_{k=1}^{\infty} \sin(2\pi kx)\,\mathrm{Log}\,k. \qquad (17.11)$$
**原文如此即无意义**（Berndt 注）：右端级数在 $0 < x < 1$ 时发散；意为 Entry 17(iv) 的类比。拉马努金在 $\cot(\pi x)$ 后插入括号注「for the same limits」，Berndt 称含义不明。另 (17.12) $\sum_{k=1}^{\infty} \sin(2\pi kx) = \frac12\cot(\pi x)$ 同样无意义（形式推导）；Berndt 用 Hurwitz 公式作形式推导。

**附注。**拉马努金在例 1 中问「求 $\varphi(-\frac12)$、$\varphi(-\frac23)$、$\varphi(-\frac34)$、$\varphi(-\frac56)$」，但除 $\varphi(-\frac12)$（见 Entry 17(iii) 例 2）外未记录其余三值（Berndt 注）。

**例 2。**$\sum_{k=0}^{\infty} (-1)^k\frac{\mathrm{Log}(2k+1)}{2k+1} = \frac14\pi\,\mathrm{Log}\,\pi - \pi\,\mathrm{Log}\,\Gamma\left(\frac34\right) - \frac14\pi\gamma$。

**例 3。**两个无穷乘积之比 $= (\sqrt{2}/\pi)\Gamma^4\left(\frac34\right)$（具体乘积见原书 p. 201）。

**出处。**Berndt Part I, Ch. 8, Entry 17(v), pp. 200–201。

**状态。**形式推导；原文表述在通常意义下无意义（级数发散），严格解释待核对。例 2、例 3 为已证明的推论（由 Entry 17(iv) 与 (17.11) 的形式推导所得，Berndt 给出严格化）。

**对照。**发散级数的形式推导见 M02、M12（Ch. 6 发散级数理论）；$\Gamma(3/4)$ 的值见 M10。

## Entry 18(i)——$\varphi(x) = \sum \mathrm{Log}^2 k$ 的渐近

**陈述。**本节的 $\varphi(x) = \sum_{k=1}^{x} \mathrm{Log}^2 k$（(18.1)）。设
$$C = \frac12\gamma^2 + c_1 - \frac{1}{24}\pi^2 - \frac12\mathrm{Log}^2(2\pi), \qquad (18.2)$$
其中 $c_1$ 为 Entry 17(i) 的常数（第一 Stieltjes 常数 $\gamma_1$）。则当 $x \to \infty$ 时，
$$\varphi(x) - 2\mathrm{Log}\,x\,\mathrm{Log}\left(\frac{\Gamma(x+1)}{\sqrt{2\pi}}\right) \sim -(x+\frac12)\mathrm{Log}^2 x + 2x + C - 2\sum_{k=2}^{\infty} \frac{B_{2k}H_{2k-2}}{(2k-1)2k\,x^{2k-1}}.$$
证明要点：常数 $c = \zeta''(0) = C$，其中 $\frac12\zeta''(0) = -\pi^2/48 + c_1/2 + \gamma^2/4 - \mathrm{Log}^2(2\pi)/4$。

**延拓。**$\varphi(x)$ 可按 Nörlund Hauptlösung 延拓（差分方程 $\varphi(x)-\varphi(x-1) = \mathrm{Log}^2 x$（(18.9)），极限式 (18.10)），也可按 Hurwitz zeta 定义 $\varphi(x) = -\zeta''(0,x+1) + \zeta''(0)$（(18.13)，Lerch 公式 $\mathrm{Log}\,\Gamma(x) = \zeta'(0,x) - \zeta'(0)$（(18.12)））；两定义相容。

**出处。**Berndt Part I, Ch. 8, Entry 18(i), pp. 202–206。

**状态。**已证明。数值复核：$C = -1.097069\ldots$（由 (18.2) 与 $\zeta''(0) = 2C$ 两种算法一致）；$\zeta''(0)$ 的值与 mpmath 一致。

**对照。**$\zeta''(0)$ 与 Lerch 公式见 M01、M10；Stirling 公式见 M12；Nörlund Hauptlösung 见 M12。

## Entry 18(ii)——$\varphi$（$\mathrm{Log}^2$ 版）的乘法公式

**陈述。**本节的 $\varphi(x) = \sum_{k=1}^{x} \mathrm{Log}^2 k$ 满足
$$\varphi(x) - \sum_{j=0}^{n-1}\varphi\left(\frac{x-j}{n}\right) = 2\mathrm{Log}\,n\,\mathrm{Log}\left(\frac{\Gamma(x+1)}{\sqrt{2\pi}}\right) - (x+\frac12)\mathrm{Log}^2 n - C(n-1). \qquad (18.16)$$

**推论。**
$$\sum_{k=1}^{n-1}\varphi\left(-\frac{k}{n}\right) = \mathrm{Log}(2\pi)\,\mathrm{Log}\,n + \frac12\mathrm{Log}^2 n + C(n-1).$$

**例 1。**$\lim_{x\to\infty} x^{x\mathrm{Log}\,x-2x}e^{2x}\prod_{k=1}^{x} k^{1/k}/k^{\mathrm{Log}\,k} = (2\pi)^{\frac12\mathrm{Log}(2\pi)}e^{-\frac12\gamma^2+\frac{1}{24}\pi^2}$。**原书印文为 $e^{-\frac12\gamma^2+1/(24\pi^2)}$，应为 $e^{-\frac12\gamma^2+\pi^2/24}$**（本轮发现，见末尾小结；书中证明 (17.5)(18.3) 联立亦得 $\pi^2/24$，与印文自相矛盾）。

**例 2。**$\varphi(-\frac12) = \mathrm{Log}(2\pi)\mathrm{Log}\,2 + \frac12\mathrm{Log}^2 2 + C$，及 $n = 3, 4, 6$ 的三式（见原书 p. 208）。第二本笔记 p. 98 拉马努金只问未给值，第一本笔记 p. 135 记录了值（Berndt 注）。

**出处。**Berndt Part I, Ch. 8, Entry 18(ii), pp. 207–208；笔记本出处：第二本笔记 p. 98、第一本笔记 p. 135（例 2 的值）。

**状态。**已证明（例 1 按订正后的指数）。数值复核：例 2 四式用 Hurwitz zeta 二阶导数（$\varphi(x) = -\zeta''(0,x+1) + \zeta''(0)$）复核，误差 $\le 10^{-12}$；例 1 的对数极限在 $N = 2000$ 时 $= 1.93480729$，订正版 $\frac12\mathrm{Log}^2(2\pi) - \frac12\gamma^2 + \pi^2/24 + (\mathrm{Log}\,N)/(3N) = 1.93480743$（差 $1.4\times 10^{-7}$），印文版 $1/(24\pi^2)$ 得 $1.52653$（差 $0.41$）。

**对照。**Gauss 乘法定理的类比见 M10；$\zeta''(0)$ 见 M01；无穷乘积的极限见 M02、M12。

## Entry 18(iii)——$\varphi(x-1)+\varphi(-x)$ 的余弦级数

**陈述。**$0 < x < 1$ 时，
$$\frac12\{\varphi(x-1)+\varphi(-x)\} = c_1 - \frac{1}{24}\pi^2 + \frac12(\gamma+\mathrm{Log}(2\pi))\left(\gamma - \mathrm{Log}\left\{\frac12\pi\csc^2(\pi x)\right\}\right) - \sum_{k=1}^{\infty} \frac{\mathrm{Log}\,k\cos(2\pi kx)}{k}. \qquad (18.19)$$
其中 $\varphi$ 为本节（$\mathrm{Log}^2$ 版）的 $\varphi$，$c_1$ 为 Entry 17(i) 的常数。

**出处。**Berndt Part I, Ch. 8, Entry 18(iii), pp. 208–209。

**状态。**已证明（由 Hurwitz 公式）。

**对照。**Kummer 公式的余弦类比见 M10；Fourier 级数见 M02、M12。

## Entry 19(i)——「对数部分」$\mathcal{L}\psi_n(x)$ 的递推

**陈述。**设 $\varphi_n(x) = \sum_{k=1}^{x} \mathrm{Log}^n k$，$\psi_n(x) = \varphi_n(x) - c_n$（(19.2)），其中 $c_n$ 为第 19 节的常数（(19.1)，见「背景与记号」；$c_0 = -1/2$、$c_1 = \frac12\mathrm{Log}(2\pi)$、$c_2 = C$）。记 $\mathcal{L}f(x)$ 为 $f(x)$ 的「对数部分」（即渐近展开中 $\mathrm{Log}\,x$ 的多项式部分，见原书 p. 209 定义）。则
$$\mathcal{L}\psi_n(x) = \mathcal{L}\sum_{k=1}^{n} (-1)^{k+1}\binom{n}{k}\mathrm{Log}^k x\,\psi_{\,n-k}(x). \qquad (19.3)$$

**出处。**Berndt Part I, Ch. 8, Entry 19(i), p. 210。

**状态。**已证明。

**对照。**$\varphi_n$ 的渐近展开见 M12；$\mathrm{Log}\,\Gamma$ 的类比主线见 M10。

## Entry 19(ii)——$\psi_n$ 的渐近展开

**陈述。**
$$\sum_{k=0}^{n} (-1)^{n+k}\binom{n}{k}\mathrm{Log}^k x\,\psi_{\,n-k}(x) \sim n!\,x - \frac{B_{n+1}}{(n+1)x^n} - \frac{nB_{n+2}}{2(n+2)x^{n+1}} - \frac{n(n+\frac32)B_{n+3}}{2^2 2!(n+3)x^{n+2}} - \frac{n(n+2)(n+3)B_{n+4}}{2^3 3!(n+4)x^{n+3}} - \frac{n\{(n+2)(n+4)^2 + \frac13(n+2) + \frac45\}B_{n+5}}{2^4 4!(n+5)x^{n+4}} - \frac{n(n+4)(n+5)\{(n+3)(n+4) + \frac23(n+1)\}B_{n+6}}{2^5 5!(n+6)x^{n+5}} - \cdots. \qquad (19.7)$$
证明用 Faà di Bruno 行列式 (19.12) 与 $A_k(n)$（pp. 211–214）。

**解析延拓。**$\varphi_n(x) = (-1)^{n+1}\{\zeta^{(n)}(0,x+1) - \zeta^{(n)}(0)\}$（(19.16)），$\psi_n(x) = (-1)^{n+1}\zeta^{(n)}(0,x+1)$（(19.17)）；$c_n = (-1)^n\zeta^{(n)}(0)$（(19.18)）。

**出处。**Berndt Part I, Ch. 8, Entry 19(ii), pp. 210–214。

**状态。**已证明。

**对照。**Faà di Bruno 公式见 M13；Hurwitz zeta 的导数见 M01；渐近展开见 M12。

## Entry 19(iii)——$\psi_n$ 的乘法公式

**陈述。**
$$\psi_n(x) - \sum_{j=0}^{r-1}\psi_n\left(\frac{x-j}{r}\right) = \sum_{j=1}^{n} \binom{n}{j}(-1)^{j+1}\mathrm{Log}^j r\,\psi_{\,n-j}(x). \qquad (19.19)$$
特例 $n = 1$ 为 Gauss 乘法定理的另一形式，$n = 2$ 等价于 Entry 18(ii)。

**推论 1。**
$$\sum_{j=1}^{r-1}\psi_n\left(-\frac{j}{r}\right) = \sum_{j=1}^{n} \binom{n}{j}(-1)^{j+1}c_{n-j}\,\mathrm{Log}^j r.$$
**拉马努金版右端多了一个 $-c_n$ 加项**（Berndt 注，第二本笔记 p. 99）。

**推论 2。**$\mathcal{L}\sum_{j=0}^{x-1}\psi_n\left(\frac{x-j}{x}\right) = 0$。

**出处。**Berndt Part I, Ch. 8, Entry 19(iii), pp. 215–216；笔记本出处：第二本笔记 p. 99（推论 1）。

**状态。**已证明（订正后）。

**对照。**Gauss 乘法定理的类比见 M10；$c_n$ 常数见「背景与记号」（第 19 节的 $c_n$ 与第 17、22 节的 $c$ 不同）。

## Entry 20(i)——$F_k(x) = \sum n^r k^{n-1}$ 的渐近

**陈述。**设 $r, x$ 为正整数，$k > 0$，$F_k(x) = k^x\varphi(x) = \sum_{n=1}^{x} n^r k^{n-1}$（(20.1)；此处的 $\varphi$ 与本章其他节的 $\varphi$ 含义不同）。$k \ne 1$ 时，
$$\varphi(x) = \sum_{j=0}^{r} \binom{r}{j}(-1)^j\frac{\psi_j(-k)x^{r-j}}{(k-1)^{j+1}} + \frac{C_r(k)}{k^x} + \frac{x^r}{2k} + \frac{R}{k^{x+1}}, \qquad (20.2)$$
其中
$$\psi_j(-k) = \frac{j!(k-1)^{j+1}}{k\,\mathrm{Log}^{j+1}k}, \qquad (20.3)$$
$$C_r(k) = \frac{(-1)^{r+1}r!}{k\,\mathrm{Log}^{r+1}k}, \qquad (20.4)$$
$$R = \int_0^x P_1(t)k^t(rt^{r-1}+t^r\mathrm{Log}\,k)\,dt, \qquad (20.5)$$
$P_1(t)$ 为第一 Bernoulli 周期函数（(20.6)）。**Berndt 注：拉马努金本（第二本笔记 p. 99）未给 (20.2) 的最后两项、未给 $C_r(k)$ 的定义、把 $C_r(k)/k^x$ 写成 $C_r(k)$、「where $\psi$ is the same $\psi$ in」一句未写完，故 (20.3) 未给出。**

**出处。**Berndt Part I, Ch. 8, Entry 20(i), pp. 216–217；笔记本出处：第二本笔记 p. 99。

**状态。**陈述经 Berndt 补全（原文不完整），已证明。

**对照。**幂和与指数权的渐近见 M12、M13；Bernoulli 周期函数见 M12。

## Entry 20(ii)——$C_r(k)$ 与 $\psi_r$ 的关系

**陈述。**
$$C_r(k) = \frac{\psi_r(-k)}{(1-k)^{r+1}}, \qquad k\psi_j(-k) = k^j\psi_j\left(-\frac1k\right), \quad 0 \le j \le r.$$
**后一等式拉马努金只对 $j = r$ 陈述，且右端下标漏写**（Berndt 注）。

**延拓。**$0 < k < 1$ 时，
$$F_k(x) = \sum_{n=1}^{\infty} \{n^r k^{n-1} - (n+x)^r k^{n+x-1}\}. \qquad (20.8)$$

**出处。**Berndt Part I, Ch. 8, Entry 20(ii), p. 217。

**状态。**已证明（订正后）。

**对照。**$\psi_j$ 的函数关系见 M10、M12。

## Entry 20(iii)——$F_k$ 的乘法公式

**陈述。****此处 $C_r(k)$ 改义**：$C_r(k) = \sum_{m=1}^{\infty} m^r k^{m-1}$（与 Entry 20(i) 的 $C_r(k)$ 不同，见「背景与记号」）。则
$$\sum_{j=0}^{n-1} F_k\left(\frac{x-j}{n}\right) = nC_r(k) + n^{-r}k^{(1-n)/n}\{F_{k^{1/n}}(x) - C_r(k^{1/n})\}. \qquad (20.9)$$

**推论。**
$$\sum_{j=1}^{n-1} F_k\left(-\frac{j}{n}\right) = nC_r(k) - n^{-r}k^{(1-n)/n}C_r(k^{1/n}).$$

**出处。**Berndt Part I, Ch. 8, Entry 20(iii), p. 218。

**状态。**已证明。数值复核：推论在 $r = 1$、$n = 2$、$k = 1/2$ 时直接求和复核，误差 $1.6\times 10^{-30}$。

**对照。**乘法公式见 M10；$C_r(k)$ 的两义见「背景与记号」。

## Entry 21(i)——$\varphi_r(x) = \sum (\mathrm{Log}\,k)/k^r$ 的渐近

**陈述。**设 $r > 1$（$r = 1$ 见第 17 节，$r < 0$ 见第 9 章），$\varphi_r(x) = \sum_{k=1}^{x} (\mathrm{Log}\,k)/k^r$（(21.1)），$H_n(r) = \sum_{k=0}^{n} 1/(k+r)$（(21.2)）。则当 $x \to \infty$ 时，
$$\varphi_r(x) + \mathrm{Log}\,x\,\zeta(r,x+1) \sim -\zeta'(r) - \frac{1}{(r-1)^2 x^{r-1}} + \sum_{k=1}^{\infty} \frac{B_{2k}(r)_{2k-1}H_{2k-2}(r)}{(2k)!\,x^{r+2k-1}}. \qquad (21.3)$$
其中 $(r)_{2k-1} = r(r+1)\cdots(r+2k-2)$ 为上升阶乘。

**延拓。**
$$\varphi_r(x) = \sum_{k=1}^{\infty} \left\{\frac{\mathrm{Log}\,k}{k^r} - \frac{\mathrm{Log}(k+x)}{(k+x)^r}\right\}. \qquad (21.10)$$

**出处。**Berndt Part I, Ch. 8, Entry 21(i), pp. 218–220。

**状态。**已证明。

**对照。**Hurwitz zeta 函数 $\zeta(r,x+1)$ 见 M01、M10；渐近展开见 M12。

## Entry 21(ii)——$\varphi_r(x)$ 的幂级数展开

**陈述。**$r > 0$、$|x| < 1$ 时，
$$\varphi_r(x) = \sum_{j=1}^{\infty} \binom{-r}{j}\{\zeta(r+j)H_{j-1}(r) - \zeta'(r+j)\}x^j.$$

**出处。**Berndt Part I, Ch. 8, Entry 21(ii), p. 220。

**状态。**已证明。

**对照。**$\zeta$ 与 $\zeta'$ 的级数见 M01；幂级数展开见 M02。

## Entry 21(iii)——$\varphi_r$ 的乘法公式

**陈述。**$r > 1$ 时，
$$n^r\varphi_r(x) - \sum_{j=0}^{n-1}\varphi_r\left(\frac{x-j}{n}\right) = (n-n^r)\zeta'(r) - n^r\mathrm{Log}\,n\,\zeta(r,x+1).$$

**推论。**
$$\sum_{j=1}^{n-1}\varphi_r\left(-\frac{j}{n}\right) = n^r\mathrm{Log}\,n\,\zeta(r) + (n^r-n)\zeta'(r).$$

**出处。**Berndt Part I, Ch. 8, Entry 21(iii), p. 221。

**状态。**已证明。数值复核：推论在 $r = 2$、$n = 2$ 时直接求和复核，$\varphi_2(-1/2) = 2.68562913409$，右端 $4\mathrm{Log}\,2\,\zeta(2) + 2\zeta'(2) = 2.68562913394$，差 $1.5\times 10^{-10}$。

**对照。**乘法公式见 M10；Hurwitz zeta 函数见 M01。

## Entry 22(i)——$\varphi_r(x) = \sum (\mathrm{Log}^r k)/k$ 与常数 $c_r$

**陈述。**设 $r \ge 0$，$\varphi_r(x) = \sum_{k=1}^{x} (\mathrm{Log}^r k)/k$（(22.1)），
$$c_r = \lim_{x\to\infty}\left\{\varphi_r(x) - \frac{\mathrm{Log}^{r+1}x}{r+1}\right\}.$$
此处 $c_r$ 是 Stieltjes 型常数：$c_0 = \gamma$、$c_1 = \gamma_1$、$c_2 = \gamma_2$（符号约定 $c_r = (-1)^r\gamma_r$），与第 19 节的 $c_n$ 不同（见「背景与记号」）。

**延拓。**
$$\varphi_r(x) = \sum_{k=1}^{\infty} \left\{\frac{\mathrm{Log}^r k}{k} - \frac{\mathrm{Log}^r(k+x)}{k+x}\right\}. \qquad (22.2)$$

**出处。**Berndt Part I, Ch. 8, Entry 22(i), p. 221。

**状态。**已证明。

**对照。**Stieltjes 常数见 M01（Ch. 7 Entry 13）；$\mathrm{Log}\,\Gamma$ 的类比主线见 M10。

## Entry 22(ii)——$\varphi_r$ 的乘法公式

**陈述。**$r$ 为非负整数时，
$$n\varphi_r(x) - \sum_{j=0}^{n-1}\varphi_r\left(\frac{x-j}{n}\right) = \frac{(-1)^r n}{r+1}\,\mathrm{Log}^{r+1} n + n\sum_{j=1}^{r} \binom{r}{j}(-1)^{j+1}\mathrm{Log}^j n\,\{\varphi_{r-j}(x) - c_{r-j}\}.$$

**出处。**Berndt Part I, Ch. 8, Entry 22(ii), p. 222。

**状态。**已证明。数值复核：$r = 1$、$n = 2$、$x = 1/2$ 时，由 (22.2) 直接求和（$10^6$ 项 + 尾项修正）复核，左右两端 $= -0.429867168745$ 与 $-0.429867168754$，差 $8.3\times 10^{-12}$（注意此处 $c_0 = \gamma$，不是第 19 节的 $c_0 = -1/2$）。

**对照。**乘法公式见 M10；Stieltjes 常数见 M01。

## Entry 23——$\zeta^{(r)}(s+1)$ 的 Taylor 展开

**陈述。**$r \ge 0$，$\sigma > 0$ 时，
$$\sum_{k=1}^{\infty} \frac{\mathrm{Log}^r k}{k^{s+1}} = \frac{\Gamma(r+1)}{s^{r+1}} + \sum_{k=0}^{\infty} (-1)^k\frac{c_{r+k}s^k}{k!}, \qquad (23.1)$$
即 $\zeta^{(r)}(s+1)$ 在 $s = 0$ 的 Taylor 展开（$c_{r+k}$ 为 Stieltjes 常数，见 Entry 22(i)）。证明由 (23.2) $\zeta(s+1) = 1/s + \sum_{k=0}^{\infty} (-1)^k c_k s^k/k!$ 逐项求导。另有界 $|c_k/k!| \le 4/(k\pi^k)$，$k \ge 1$（(23.10)）。

**例 1。**$-\zeta'''(3/2) = 96.001$（拉马努金近似）。**书中「改进值」96.009940 是错的**（本轮发现，见末尾小结）：真值 $-\zeta'''(3/2) = 96.000994$，拉马努金原值 96.001 的误差仅 $6\times 10^{-6}$；书中「96.01 会是比 96.001 更好的近似」的说法亦错。

**例 2。**$-\zeta'(2) = 0.9382$（拉马努金近似）。真值 $-\zeta'(2) = 0.93754825431584375$（Rosser–Schoenfeld；拉马努金值有小误差，Berndt 注）。

**例 3。**$\zeta^{(iv)}(2) = 24$（拉马努金近似）。**书中「改进值」24.014859 是错的**（本轮发现）：真值 $\zeta^{(iv)}(2) = 24.001486$。

**例 4。**$-\zeta^{(v)}(3/2) = 7680$（拉马努金近似）。**书中「改进值」7680.008541 是错的**（本轮发现）：真值 $-\zeta^{(v)}(3/2) = 7680.000854$。

**例 5。**$\sum_{k=1}^{\infty} \mathrm{Log}^{11/2}k/k^2 = 288$（拉马努金近似）。$\Gamma(13/2) = 287.88528$，故 288 合理；真值 $= 287.88575$。

**出处。**Berndt Part I, Ch. 8, Entry 23, pp. 223–226。

**状态。**已证明（例 1、3、4 按订正后的数值）。数值复核：$-\zeta'''(3/2) = 96.0009940067$（mpmath 50 位 zeta 导数）、$= 96 + M_6(3,1/2)$（$M_6 = 0.000994008$，Stieltjes 常数求和）、直接求和（$2\times 10^5$ 项 + 不完全 Gamma 尾项）$= 96.001014$（差 $2\times 10^{-5}$，尾项修正量级），三法一致；$\zeta^{(iv)}(2) = 24.0014863937$（三法一致，$M_5(4,1) = 0.001485871$）；$-\zeta^{(v)}(3/2) = 7680.000854$（$M_4(5,1/2) = 0.000854133$）；$-\zeta'(2) = 0.93754825431584375$（精确）；例 5 直接求和（$10^5$ 项 + 不完全 Gamma 尾项）$= 287.88575$。

**对照。**$\zeta$ 的导数与 Stieltjes 常数见 M01；Taylor 展开见 M02、M12；$\Gamma(13/2)$ 见 M10。

## Entry 24(i)——$\varphi(x) = \sum (\mathrm{Log}\,k)/\sqrt{k}$ 的级数延拓

**陈述。**第 24 节的 $\varphi(x) = \sum_{k=1}^{x} (\mathrm{Log}\,k)/\sqrt{k}$（(24.1)，即 Entry 21(i) 的 $r = 1/2$ 情形）。$x > -1$ 时，
$$\varphi(x) = \sum_{k=1}^{\infty} \left\{\frac{\mathrm{Log}\,k}{\sqrt{k}} - \frac{\mathrm{Log}(k+x)}{\sqrt{k+x}}\right\}. \qquad (24.2)$$

**出处。**Berndt Part I, Ch. 8, Entry 24(i), p. 226。

**状态。**已证明。

**对照。**$r = 1/2$ 的 $\varphi_r$ 见 Entry 21；Hurwitz zeta 的延拓见 M01、M10。

## Entry 24(ii)——$\varphi$（$r=1/2$ 版）的渐近与常数 $c$

**陈述。**设 $\varphi(x)$ 如 (24.1)。则当 $x \to \infty$ 时，
$$\varphi(x) - \left\{\sum_{k=1}^{x} \frac{1}{\sqrt{k}} - \zeta\left(\frac12\right)\right\}\mathrm{Log}\,x \sim -4\sqrt{x} - \zeta\left(\frac12\right)\left\{\frac12\gamma + \frac14\pi + \frac12\mathrm{Log}(8\pi)\right\} + \sum_{k=1}^{\infty} \frac{B_{2k}(\frac12)_{2k-1}H_{2k-2}(\frac12)}{(2k)!\,x^{2k-1/2}},$$
其中 $H_n(1/2)$ 由 (21.2) 定义。常数
$$c = -\zeta\left(\frac12\right)\left\{\frac12\gamma + \frac14\pi + \frac12\mathrm{Log}(8\pi)\right\}, \qquad (24.4)$$
$$c = \lim_{x\to\infty}\left\{\varphi(x) - 2\sqrt{x}\,\mathrm{Log}\,x + 4\sqrt{x}\right\}, \qquad (24.5)$$
并证
$$\zeta'\left(\frac12\right) = -c. \qquad (24.6)$$

**出处。**Berndt Part I, Ch. 8, Entry 24(ii), pp. 226–227。

**状态。**已证明。数值复核：(24.4) 得 $c = 3.92264613921$（$\zeta(1/2) = -1.4603545088$，$\{\cdots\} = 2.68609$）；(24.5) 由直接求和（$10^6$ 项 + Euler–Maclaurin 修正 $(\mathrm{Log}\,N)/(2\sqrt{N})$）得 $c = 3.92264613801$；$\zeta'(1/2) = -3.9226461392$（mpmath 50 位），与 (24.6) 一致。**注意：(24.4)、Entry 24(ii) 渐近式、Entry 24(iii) 末项与 $\varphi(-1/2)$ 公式中的 $\zeta(1/2)$ 均无撇号**——150 DPI 读图时 $\zeta$ 字形的顶部弯钩易被误读为撇号，已用 300 DPI 放大 4 倍逐字确认无撇号，见末尾小结。

**对照。**$\zeta(1/2)$、$\zeta'(1/2)$ 的值见 M01；渐近展开见 M12；$\mathrm{Log}\,\Gamma$ 的类比主线见 M10。

## Entry 24(iii)——$\varphi$（$r=1/2$ 版）的乘法公式

**陈述。**设 $\psi(x) = \sum_{k=1}^{\infty} \{1/\sqrt{k} - 1/\sqrt{k+x}\}$（(24.7)，$x > -1$），$\varphi(x)$ 如 (24.1)，$c$ 如 (24.4)。则
$$\varphi(x) - \frac{1}{\sqrt{n}}\sum_{j=0}^{n-1}\varphi\left(\frac{x-j}{n}\right) = \psi(x)\,\mathrm{Log}\,n - (\sqrt{n}-1)c - \zeta\left(\frac12\right)\mathrm{Log}\,n.$$
证明由 (24.8)（$s = 1/2$ 的一般恒等式，见原书 p. 228）得来。

**出处。**Berndt Part I, Ch. 8, Entry 24(iii), p. 228。

**状态。**已证明。数值复核：由此式与 Entry 24(iv) 联立得 $\varphi(-1/2) = 0.866308507608$（直接求和 $10^6$ 项 + 尾项修正），公式值 $0.866308508347$（差 $7.4\times 10^{-10}$），见例 2(a)。

**对照。**乘法公式见 M10；$\psi(x)$（(24.7)）为 $\sum 1/\sqrt{k}$ 的类比，见 M01、M10。

## Entry 24(iv)——$\varphi(x-1)+\varphi(-x)$ 的余弦级数

**陈述。**$0 < x < 1$ 时，
$$\varphi(x-1)+\varphi(-x) - 2c + \left(\gamma + \frac12\pi + \mathrm{Log}(8\pi)\right)\left\{\psi(x-1)+\psi(-x) - 2\zeta\left(\frac12\right)\right\} = 2\sum_{k=1}^{\infty} \frac{\mathrm{Log}\,k\cos(2\pi kx)}{\sqrt{k}}.$$
其中 $\varphi$、$\psi$、$c$ 如 Entry 24(i)–(iii)。

**出处。**Berndt Part I, Ch. 8, Entry 24(iv), p. 228。

**状态。**已证明（由 Hurwitz 公式）。

**对照。**Kummer 公式的余弦类比见 M10；Fourier 级数见 M02、M12。

## Entry 24(v)——$\varphi(x-1)-\varphi(-x)$ 的正弦级数

**陈述。**$0 < x < 1$ 时，
$$\varphi(x-1) - \varphi(-x) + \left(\gamma - \frac12\pi + \mathrm{Log}(8\pi)\right)\left\{\psi(x-1) - \psi(-x)\right\} = 2\sum_{k=1}^{\infty} \frac{\mathrm{Log}\,k\sin(2\pi kx)}{\sqrt{k}}.$$

**出处。**Berndt Part I, Ch. 8, Entry 24(v), p. 229。

**状态。**已证明（由 Hurwitz 公式）。

**对照。**Kummer 公式的正弦类比见 M10（Entry 17(iv) 为 $(\mathrm{Log}\,k)/k$ 版，本条为 $(\mathrm{Log}\,k)/\sqrt{k}$ 版）。

## 例 1、例 2——$\varphi(-1/2)$ 与常数 $c$（第 24 节末）

**例 1。**拉马努金问 $\varphi(-1/2)$、$\varphi(-2/3)$、$\varphi(-3/4)$ 的值（与 Entry 17(v) 的提问呼应）。

**例 2(a)。**$c = 3.92265$（用 Dwight 表值 $\zeta(\frac12) = -1.4603545088$ 可验证）。由 Entry 24(iii)（取 $n = 2$）与 Entry 24(iv)（取 $x = 1/2$）联立得
$$\varphi\left(-\frac12\right) = (\sqrt{2}-2)\left\{\frac12\gamma + \frac14\pi + \frac12\mathrm{Log}(8\pi)\right\}\zeta\left(\frac12\right) + \sqrt{2}\,\mathrm{Log}\,2\,\zeta\left(\frac12\right).$$
数值复核：右端 $= 0.866308508347$，由 (24.2) 直接求和得 $\varphi(-1/2) = 0.866308507608$（差 $7.4\times 10^{-10}$）。（同法由 $n = 3$、$x = 1/3$ 得 $\varphi(-1/3)$ 的公式，见原书 pp. 230–231。）

**例 2(b)。**$c$ 的半收敛级数（Bromwich 意义）：
$$c \sim 4 - \sum_{k=1}^{\infty} \frac{B_{2k}(\frac12)_{2k-1}H_{2k-2}(\frac12)}{(2k)!}. \qquad (24.13)$$

**出处。**Berndt Part I, Ch. 8, pp. 229–231。

**状态。**已证明。数值复核见 Entry 24(ii) 与 Entry 24(iii)。

**对照。**$\varphi(-1/2)$ 的值见 Entry 17(iii) 例 2（$(\mathrm{Log}\,k)/k$ 版）；半收敛级数见 M12。

## 小结

### 本章的地位

本章是 Part I 中最长的一章（pp. 181–231，共 51 页；第 7 章为 32 页），也是 $\mathrm{Log}\,\Gamma$ 类比理论最系统的展开。第 17–19 节构成主线：$\sum (\mathrm{Log}\,k)/k$、$\sum \mathrm{Log}^2 k$、$\sum \mathrm{Log}^n k$ 三层类比，各有渐近展开、乘法公式与 Hurwitz zeta 延拓；第 20–24 节为变体（指数权、$(\mathrm{Log}\,k)/k^r$、$(\mathrm{Log}^r k)/k$、$\zeta^{(r)}$、$r = 1/2$ 特例）。第 9 章第 27–30 节继续此主题（$r < 0$ 的情形见第 9 章）。

### 拉马努金原文疏失（Berndt 已指出）

开场白 $e^{-\gamma}$ 末位应为 7；Entry 5 右端错乘 $-1$；Entry 10 笔记本把 $1-u$ 错写成平方；例 13(vi)(b) 漏写一个求和号；Entry 14 (v) 分母 $\frac12(\sqrt{5}-1)$ 应为 $\frac12(\sqrt{5}+1)$、$A_{10}$ 的 arctan 项与笔记本不符；例 14.1(iii) 漏写分母中的 $\sqrt{2}$；例 14.2(viii) 漏 $(\sqrt{3}/6)\mathrm{Log}\,2$ 一项；Entry 16「the last term」应为「the first term」；Entry 17(i) $c_1$ 末两位应为 77；Entry 17(v) 原文表述无意义（级数发散）、$\cot(\pi x)$ 后的「for the same limits」含义不明；Entry 17(v) 附注拉马努金问了 $\varphi(-1/2)$ 等四值却只记录其一；Entry 18(ii) 例 2 拉马努金只问未给值（值见第一本笔记 p. 135）；推论 19(iii) 1 拉马努金版右端多一个 $-c_n$；Entry 20(i) 原文不完整（(20.2) 最后两项、$C_r(k)$ 定义、(20.3) 均未给出）；Entry 20(ii) 右端下标漏写；Entry 23 例 2 拉马努金值 0.9382 有小误差。

### 本轮发现的原书印文问题（数值证实，未擅自改动原文）

1. **Entry 18(ii) 后例 1（p. 208）：指数中的 $1/(24\pi^2)$ 应为 $\pi^2/24$。** 印文：$\lim = (2\pi)^{\frac12\mathrm{Log}(2\pi)}e^{-\frac12\gamma^2+1/(24\pi^2)}$。证据：(a) 书中证明 (17.5)(18.3) 联立得 $\mathrm{Log}\,P_x \sim \cdots - \frac12\gamma^2 + \frac{1}{24}\pi^2 + \frac12\mathrm{Log}^2(2\pi)$，与印文自相矛盾；(b) 数值：对数极限在 $N = 2000$ 时 $= 1.93480729$，订正版 $\frac12\mathrm{Log}^2(2\pi) - \frac12\gamma^2 + \pi^2/24 = 1.93354061$（加渐近修正 $(\mathrm{Log}\,N)/(3N) = 0.00499$ 后差 $1.4\times 10^{-7}$），印文版 $1/(24\pi^2)$ 得 $1.52653$（差 $0.41$）。本文件按订正值记录，印文如实注明。
2. **Entry 23 例 1、3、4（pp. 225–226）：书中 $M_n$ 值恰好 10 倍于真值。** 书称 $M_6(3,1/2) = 0.009940$、$M_5(4,1) = 0.014859$、$M_4(5,1/2) = 0.008541$，故「改进值」为 96.009940、24.014859、7680.008541。证据：用 Stieltjes 常数（mpmath 50 位）直接求和得 $M_6 = 0.000994008$、$M_5 = 0.001485871$、$M_4 = 0.000854133$；mpmath 50 位 zeta 导数得 $-\zeta'''(3/2) = 96.0009940067$、$\zeta^{(iv)}(2) = 24.0014863937$、$-\zeta^{(v)}(3/2) = 7680.000854$；直接求和 + 不完全 Gamma 尾项三法一致。真值应为 96.000994、24.001486、7680.000854。附带结论：拉马努金原值 96.001 的误差仅 $6\times 10^{-6}$，书中「96.01 会是比 96.001 更好的近似」的说法是错的；书称的误差界（0.000195、0.008670、0.045880）亦不适用于其所刊数值。$M_2(3,1/2) = 0.000891$（书称拉马努金可能用的截断）经复核正确，故错误出在 $M_6$、$M_5$、$M_4$ 的较长部分和计算上，不在 $c_k$ 值本身。本文件按订正值记录，书值如实注明。

### 300 DPI 澄清：第 24 节无错印

本轮初读 150 DPI 图时，曾把第 24 节四处 $\zeta(1/2)$ 误读为 $\zeta'(1/2)$（(24.4)、Entry 24(ii) 渐近式常数项、Entry 24(iii) 末项、$\varphi(-1/2)$ 公式首项），并据此推断「系统性错印」。**300 DPI 放大 4 倍逐字复核后确认：四处印文均为无撇号的 $\zeta(1/2)$，与推导完全自洽**（$c = -\zeta(1/2)\{\cdots\} = 3.92265$；$\zeta'(1/2) = -c$ 仅出现在 (24.6)）。教训：$\zeta$ 字形的顶部弯钩在低分辨率下酷似撇号，撇号的有无必须以高分辨率放大图为准，不可凭低分辨率读图断言。本文件第 24 节各公式均按 300 DPI 确认的印文记录。

### 数值复核小结

本轮数值复核共约 60 项，全部通过（除上述两处原书印文问题外）：开场白 $e^{-\gamma}$；Entry 5（$x = 1/4$）；Entry 6 推论 3 五式；Entry 11（$x = 2$）；Entry 13 (13.1)（$x = 2$）；Entry 14 $A_3$–$A_{10}$ 六式（$x = 0.7$ 对积分）；例 14.1 三式；例 14.2 前八值；Entry 15 (15.2)（$n = 1$、$x = 10$）与 $\Gamma(x+1)$ 最小值点 $0.461632144968$；Entry 16（$k \le 8$）；Entry 17(i) 渐近（$x = 2000$）与 $c_1 = \gamma_1$；Entry 17(ii) 推论（交错级数）；Entry 17(iii) 推论 (17.8)（$n = 2, 3, 4, 6$）与例 2–5；Entry 18(ii) 例 1（订正后）、例 2 四式；Entry 20(iii) 推论（$r = 1$、$n = 2$、$k = 1/2$）；Entry 21(iii) 推论（$r = 2$、$n = 2$）；Entry 22(ii)（$r = 1$、$n = 2$、$x = 1/2$）；Entry 23 例 1–5；Entry 24(ii) $c$（(24.4)(24.5)(24.6) 三法）与 Entry 24(iii) $\varphi(-1/2)$。

方法教训：mpmath `nsum` 对尾项含 $(\mathrm{Log}\,N)/N$ 的慢收敛级数（如 (17.7)、(22.2)）外推会产生约 $+2.6\times 10^{-4}$/项的系统性偏差，对 $(\mathrm{Log}\,x)^{11/2}$ 这类在下限非光滑的被求和函数（例 23-5）会错 26 之多；`mp.diff` 的高阶 zeta 导数亦有约 $0.01$ 量级误差。**慢收敛/非光滑级数一律改用双精度直接求和 + 解析尾项（不完全 Gamma / 显式原函数 / Euler–Maclaurin 修正）复核，不可只信 nsum/diff。** 本轮复核脚本存于工作目录（未入仓库）：`verify1.py`、`verify2.py`、`verify3.py`、`verify4.py`。

## 待核对清单

1. IMSC 整理表计本章的结果数（imsc.res.in 当日不可达，待补）。
2. TIFR 影印版（1957 年版）中本章各条的页码（本文件所标笔记本页码 p. 92、94、95、98、99 与第一本笔记 p. 135 均据 Berndt 文中引用，TIFR 版页码待按影印版核对）。
3. Entry 17(v) (17.11) 的严格解释（原文表述在通常意义下无意义，Berndt 只作形式推导）。
4. Entry 19(ii) (19.7) 的 $A_k(n)$ 系数表（pp. 211–214，证明细节未逐项复核）。
5. 例 14.2 (vii)–(x)（$\phi(10)$、$\phi(12)$、$\phi(16)$、$\phi(20)$）的显式公式——本文件只记录了前六值的显式形式，(vii)–(x) 的显式公式见原书 pp. 192–193，未全文抄录。
6. Entry 23 例 1、3、4 的 $M_n$ 10 倍误差：是否见于本书其他印次或勘误表，待查（本书为 1985 年第一版；后续印次或 Berndt 勘误表可能已更正）。
7. 章首导言「前 14 节只占 12 页中的 $4\frac12$ 页」一句的所指（本文件按笔记本原稿页数理解，待按第二本笔记原稿页码核对）。
8. 本章与第 9 章第 27–30 节的衔接（$r < 0$ 的 $\varphi_r$，见第 9 章）。

## 来源说明

- 主来源：Bruce C. Berndt, *Ramanujan's Notebooks*, Part I, Springer, 1985, Ch. 8, pp. 181–231（archive.org 全文，`ramanujan_notebooks_i`：DjVu OCR + PDF，PDF 页 = 书页 + 10；本章 PDF pp. 192–241）。
- 核对方法：全章 50 页均以 150 DPI 读图核对；关键公式（第 24 节 $\zeta(1/2)$ 撇号问题、例 1 的指数）以 300 DPI 放大 4 倍逐字复核；数值复核用 mpmath（30–50 位）与双精度直接求和 + 解析尾项（不完全 Gamma / Euler–Maclaurin 修正）交叉验证。
- 引用文献（据 Berndt 文中引用）：Liang–Todd（Stieltjes 常数数值，见 Entry 17(i) 与 Entry 23）；Rosser–Schoenfeld（$-\zeta'(2)$ 的值，见 Entry 23 例 2）；Dwight（$\zeta(1/2)$ 表值，见 Entry 24 例 2(a)）；Bromwich（半收敛级数，见 Entry 24 例 2(b)）；Bendersky、Büsing（$\Gamma$ 推广，见章首导言）；Nörlund（Hauptlösung，见 Entry 18(i)）；Lerch（$\mathrm{Log}\,\Gamma$ 公式，见 Entry 18(i)）；Faà di Bruno（行列式，见 Entry 19(ii)）。
- 版权说明：本文件只收录公式陈述与自写导读/证明思路，不照抄 Berndt 正文与证明；数值复核为独立计算。
