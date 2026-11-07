# Part III，Chapter 21——Eisenstein Series（Eisenstein 级数）

出处：Bruce C. Berndt，《Ramanujan's Notebooks》，Part III，Springer，1991，Ch. 21，书页 454–488。

本章是 Part III 的第六章、最后一章，也是 Berndt 五卷的第 21 章：拉马努金在此把 Eisenstein 级数的线性组合与 theta 函数、椭圆模联系起来。本章共 **11 条编号 Entry（Entry 1–11，无缺号）**，另含书末未编号的 Final Entry（(11.15)(11.16)，与 Eisenstein 级数主题无关，见文末），共 34 个分体标题（见“本章结构”表后的计数说明）。

## 背景与记号

- 本章收束第二本笔记的有组织部分：Berndt 在章首说明，Ch. 21 之后第二本笔记还有 100 页未组织内容；Ch. 21 在笔记中只有四页，是第二本笔记中最短的一章（此前各章多为十二页）。
- 全章默认 $|q| < 1$，$q = e^{-y}$（$y > 0$）。$x$、$y$、$z$ 沿用 Ch. 17 第 6 节的记号：$x = k^2$（$k$ 为椭圆模），$y = \pi K'/K$，$z = 2K/\pi$，$\varphi(e^{-y}) = \sqrt{z}$；$K$、$K'$ 为第一类完全椭圆积分，$E$、$E'$ 为第二类完全椭圆积分。$z_n = {}_2F_1(\frac12,\frac12;1;\alpha_n)$，$\varphi(q^n) = z_n^{1/2}$；$\alpha$、$\beta$ 为两模，$\beta$ 为 $\alpha$ 的 $n$ 次模时乘子 $m$ 由 $z_1 = m\cdot z_n$ 定义。
- theta 函数（Ch. 16 Entry 22）：$\varphi(q) := f(q,q) = \sum_{n=-\infty}^{\infty}q^{n^2}$，$\psi(q) := f(q,q^3) = \sum_{n=0}^{\infty}q^{n(n+1)/2}$，$f(a,b) := \sum_{n=-\infty}^{\infty}a^{n(n+1)/2}b^{n(n-1)/2}$，$f(-q) := f(-q,-q^2) = (q;q)_{\infty}$，$\chi(q) := (-q;q^2)_{\infty}$。单变量记号 $f(q)$：书中 $f(q)$ 指 $f(q,-q^2)$，即 $f(q) = \prod_{n\ge 1}(1-(-q)^n)$（见 Ch. 20 章首记号说明）；本章 Entry 8(i) 的 $f^2(q)$、$f^2(q^{11})$ 按此义理解（本轮数值复核确认：按此读法在 $q = 0.5$、$0.2$ 处差 $0$；按 $(q;q)_{\infty}$ 计差 $13.8$、$3.07$，按 $(-q;q)_{\infty}$ 计差 $42.2$、$0.98$，皆不成立，见 Entry 8 说明）。
- Eisenstein 级数 $L$、$M$、$N$：拉马努金在 Ch. 15 第 9 节引入，$L = 1 - 3/y - 24\sum_{n=1}^{\infty}n/(e^{2ny}-1)$（即下文 (1.1)），$M = 1 + 240\sum_{n=1}^{\infty}n^3/(e^{2ny}-1)$（即 (1.2)），$N = 1 - 504\sum_{n=1}^{\infty}n^5/(e^{2ny}-1)$（即 (1.3)）；在拉马努金名篇 [6]（Collected Papers，pp. 136–162）中，$L$、$M$、$N$ 记为 $P$、$Q$、$R$。第 11 节的 $E_2(\tau) := 1 - 24\sum_{k=1}^{\infty}kq^{2k}/(1-q^{2k})$（$q = e^{\pi i\tau}$）即 $L$ 的 $q$ 形式（差一个 $3/y$ 项，见第 11 节）。
- 本章与已填章节的互见：Ch. 15 的 $L$、$M$、$N$（第 9 节）与“complete”级数的定义（第 10 节）是 Entry 1 的出发点；Ch. 16 的 theta 函数（Entry 22 的 $\varphi$、$\psi$、$f$、$\chi$ 定义，Entry 23 的对数展开，Entry 24、25、27 的恒等式）是 Entry 2 与第 11 节 theta 翻译的工具；Ch. 17 的椭圆函数（Entry 11–13 的 $L$、$M$、$N$ 求值与“change of sign”方法、Entry 10、12 的 $\varphi$、$\psi$ 恒等式）是 Entry 1、3–7 的证明工具；Ch. 18 的 (3.7) 与 Entry 2 是 (1.4) 的证明工具；Ch. 19 的 3、5、7 次模方程（Entry 5、11、13、14、17）与 Ch. 20 的 9 次模方程（第 3 节）与模形式理论（(0.4)、(0.6)、(0.13)、(0.14)、(0.16)、(0.18)–(0.23)、(0.24)、(0.27)、(0.30)）是 Entry 3–11 的证明工具。
- 与主题模块的对照总览：Eisenstein 级数见 **M06**（全章；M06.2 的 $E_k$ 定义与 Fourier 展开，Entry 1 的 $L$、$M$、$N$ 即 $E_2$、$E_4$、$E_6$ 的 $y$ 形式；第 11 节的 $F_n(\tau) = E_2(\tau) - nE_2(n\tau)$ 为 $\Gamma_0(n)$ 上权 2 模形式）；椭圆函数与椭圆积分见 **M11**（Entry 1 的 (1.4) 与 $K$、$E$，各条的 $\alpha$、$\beta$、$m$、$z_n$）；theta 函数与 q 级数见 **M07**（Entry 2 的对数导数、Entry 3–7 的 $\varphi$、$\psi$、$f$ 表达式、第 11 节的 theta 翻译 (11.2)–(11.7)）；无穷级数见 **M02**（Entry 3(i)、Entry 5(i) 的 Lambert 级数与系数周期）；模方程见 **M06**（Entry 3(iii)、4(iii)、5(iii)、6、8(ii)(iii)、9、10、11 的次数条件与 $\alpha$、$\beta$ 公式）；Bernoulli 数见 **M01**（$E_k$ 的 Fourier 系数含 $B_k$，见 M06.2）。

## 本章结构

| Entry | 主题 | 书页 |
|---|---|---|
| Entry 1 | Eisenstein 级数 $L$、$M$、$N$（(1.1)–(1.3)）与 (ii)–(iv) 的 $z$、$x$ 闭式；(1.4) | 454–456 |
| Entry 2 | $\varphi$、$\psi$、$f$、$\chi$ 的对数导数 (i)–(iv)；含义不明的 (v)；关键公式 (2.3)、(2.5) | 456–460 |
| Entry 3 | 3 次 Eisenstein–theta 恒等式 (i)–(iii) | 460–463 |
| Entry 4 | 5 次 Eisenstein–theta 恒等式 (i)–(iii) | 463–467 |
| Entry 5 | 7 次 Eisenstein–theta 恒等式 (i)–(iii)；关键公式 (5.3) | 467–473 |
| Entry 6 | $-q$ 版 3、5、7 次恒等式 (i)–(iii) | 473–475 |
| Entry 7 | 9 次与 25 次恒等式 (i)–(iii) | 475–480 |
| Entry 8 | 11 次与 19 次恒等式 (i)–(iii)；(i)(iii) 的证明推迟到第 11 节 | 480–481 |
| Entry 9 | 23、15、31 次恒等式 (i)–(iii)；证明全部推迟到第 11 节 | 481 |
| Entry 10 | 5、9、17 次恒等式 (i)–(iii)；(iii) 的证明推迟到第 11 节 | 482–484 |
| Entry 11 | 35 次恒等式（单条；笔记中列为 11(i)，p. 256）；证明在第 11 节 | 484 |
| 第 11 节 | 定理（$F_n$ 为 $\Gamma_0(n)$ 上权 2 模形式）与七条推迟公式的模形式证明 (11.2)–(11.14) | 484–488 |
| Final Entry | 未编号：$\varphi$ 的两条恒等式 (11.15)(11.16)（笔记最后一页，p. 256） | 488 |

计数说明：编号 Entry 1–11 共 11 条，无缺号。分体标题 34 个：Entry 1(i)–(iv) 4、Entry 2(i)–(v) 5、Entry 3(i)–(iii) 3、Entry 4(i)–(iii) 3、Entry 5(i)–(iii) 3、Entry 6(i)–(iii) 3、Entry 7(i)–(iii) 3、Entry 8(i)–(iii) 3、Entry 9(i)–(iii) 3、Entry 10(i)–(iii) 3、Entry 11 1。另有未编号的 Final Entry（(11.15)(11.16) 两式）与第 11 节的定理及编号公式 (11.2)–(11.14)，均已按其所属位置收录。Entry 11 在笔记中列为 11(i)，但该节无进一步结果，故本章编号只有一条 Entry 11。

## Entry 1

**陈述。** $x$、$y$、$z$ 如章首（$q = e^{-y}$）。拉马努金（笔记 p. 253）原文照录：

**(i)** 级数

$$(1.1)\quad 1 - \frac{3}{y} - 24\sum_{n=1}^{\infty}\frac{n}{e^{2ny}-1}$$

is a complete series which when divided by $z^2$ can be expressed by radicals precisely in the same manner as the series

$$(1.2)\quad 1 + 240\sum_{n=1}^{\infty}\frac{n^3}{e^{2ny}-1}$$

and the series

$$(1.3)\quad 1 - 504\sum_{n=1}^{\infty}\frac{n^5}{e^{2ny}-1}$$

when divided by $z^4$ and $z^6$, respectively.

**(ii)**

$$1 - 24\sum_{n=0}^{\infty}\frac{2n+1}{e^{(2n+1)y}+1} = z^2(1-2x).$$

**(iii)**

$$1 - 240\sum_{n=1}^{\infty}\frac{(-1)^{n+1}n^3}{e^{ny}-(-1)^n} = z^4\{1-16x(1-x)\}.$$

**(iv)**

$$1 + 504\sum_{n=1}^{\infty}\frac{(-1)^{n+1}n^5}{e^{ny}-(-1)^n} = z^6(1-2x)\{1+32x(1-x)\}.$$

另有 Berndt 的注记 (1.4)：置 $S := (1/z^2)(1 - 3/y - 24\sum_{n=1}^{\infty}n/(e^{2ny}-1))$，则

$$(1.4)\quad S = \frac{3}{2}\left(\frac{E}{K}-\frac{E'}{K'}\right) + k^2 - \frac{1}{2},$$

其中 $k^2 = x$。而 (1.2)、(1.3) 除以 $z^4$、$z^6$ 的值（Ch. 17 Entry 13(i)(ii)）为

$$\frac{1}{z^4}\left(1 + 240\sum_{n=1}^{\infty}\frac{n^3}{e^{2ny}-1}\right) = 1-x+x^2,\quad \frac{1}{z^6}\left(1 - 504\sum_{n=1}^{\infty}\frac{n^5}{e^{2ny}-1}\right) = (1+x)(1-\frac{1}{2}x)(1-2x).$$

**说明。**(i) 的“complete”定义见 Ch. 15 第 10 节（Part II，p. 320），Berndt 注明拉马努金的定义相当含糊（rather vaguely）。(i) 的表述并不完全准确：须补加条件 $y^2/\pi^2$ 为有理数；补上该条件后，(i) 由拉马努金在论文 [2]（pp. 32、33）中建立；读者可参阅 [2] 与 Borwein 的书 [2，Chap. 5]，了解拉马努金如何用此类结果导出 $\pi$ 的优良逼近。(1.4) 的证明用 Ch. 18 Entry 2 与 (3.7)（${}_2F_1(-\frac12,\frac12;1;k^2) = 2E/\pi$）及 Legendre 关系（Whittaker and Watson [1，p. 520]；Almkvist and Berndt [1] 给出一个较简单的 Legendre 关系证明）。(ii) 的证明用 Ch. 17 Entry 13(viii)(ix)。(iii)(iv) 的证明用 Ch. 17 第 13 节的“change of sign”方法：(iii) 在 Ch. 17 Entry 13(iii) 中以 $-x/(1-x)$ 代 $x$（$e^{-y}$ 换为 $-e^{-y}$，$z$ 换为 $z\sqrt{1-x}$）；(iv) 同法用于 Entry 13(iv)。

**状态：** 已证明（书中给出证明；(i) 须补加 $y^2/\pi^2$ 为有理数的条件，见说明）。**对照：** M06（Eisenstein 级数 $L$、$M$、$N$）、M11（椭圆积分 (1.4)）、M01（$E_k$ 与 Bernoulli 数，见 M06.2）。

**我自验：** 取 $q = 0.5$、$0.3$（$y = -\log q$，$x = \alpha(q)$，$z = \varphi^2(q)$；mpmath 30 位，直接求和）：(ii) 差 $\le 7.9\times 10^{-30}$；(iii) 差 $\le 1.4\times 10^{-27}$；(iv) 差 $\le 2.6\times 10^{-26}$；(1.2)/$z^4$ 与 (1.3)/$z^6$ 差 $\le 1.3\times 10^{-30}$；(1.4)（$K$、$E$ 用 mpmath 椭圆积分）差 $\le 2.1\times 10^{-28}$。(i) 为定性断言（“可以表为根式”），不作数值复核。

## Entry 2

**陈述。** $\varphi$、$\psi$、$f$、$\chi$ 如 Ch. 16 Entry 22。则

**(i)**

$$12q\frac{\varphi'(q)}{\varphi(q)} = 1 - 24\sum_{n=1}^{\infty}\frac{nq^{2n}}{1-q^{2n}} - \left(1 - 24\sum_{n=0}^{\infty}\frac{(2n+1)q^{2n+1}}{1+q^{2n+1}}\right).$$

**(ii)**

$$24q\frac{\frac{d}{dq}\{q^{1/8}\psi(q)\}}{q^{1/8}\psi(q)} = 4\left(1 - 24\sum_{n=1}^{\infty}\frac{nq^{4n}}{1-q^{4n}}\right) - \left(1 - 24\sum_{n=0}^{\infty}\frac{(2n+1)q^{2n+1}}{1+q^{2n+1}}\right).$$

**(iii)**

$$24q\frac{\frac{d}{dq}\{q^{1/24}f(-q)\}}{q^{1/24}f(-q)} = 1 - 24\sum_{n=1}^{\infty}\frac{nq^n}{1-q^n}.$$

**(iv)**

$$24q\frac{\frac{d}{dq}\{q^{1/24}/\chi(q)\}}{q^{1/24}/\chi(q)} = 1 - 24\sum_{n=0}^{\infty}\frac{(2n+1)q^{2n+1}}{1+q^{2n+1}}.$$

**(v)** By differentiating the equation for $m$ once or the equation for $\alpha$, $\beta$ twice we can calculate the value of the first series.（拉马努金原话，笔记 p. 253 照录。）

本章其余部分所依据的关键公式（Berndt 的整理，拉马努金未明言）：设 $n$ 为正整数，$\beta$ 为 $\alpha$ 的 $n$ 次模，$m$ 为相应乘子，则

$$(2.3)\quad 1 - 24\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - n\left(1 - 24\sum_{k=1}^{\infty}\frac{kq^{2nk}}{1-q^{2nk}}\right) = -\alpha(1-\alpha)z_1^2\frac{d}{d\alpha}\mathrm{Log}\left(\frac{\beta(1-\beta)}{m^6\alpha(1-\alpha)}\right).$$

第二种可能解释用 Ch. 16 Entry 27(iii)：设 $y$、$y' > 0$，$yy' = \pi^2$，$q = e^{-y}$、$q' = e^{-y'}$，则

$$(2.5)\quad 1 - 24\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} = \frac{6}{y} - \frac{y'}{y}\left(1 - 24\sum_{k=1}^{\infty}\frac{kq'^{2k}}{1-q'^{2k}}\right).$$

取 $y = \pi/\sqrt{n}$（故 $y' = \pi\sqrt{n}$），联立 (2.3) 与 (2.5) 可得 $n(1 - 24\sum_{k=1}^{\infty}k/(e^{2\pi k/\sqrt{n}}-1)) - 3\sqrt{n}/\pi$ 的 $\alpha$、$z_1$ 表达式（书页 460）。

**说明。**(i)–(iv) 很容易证明：(iii) 由 Ch. 16 Entry 23(iii)（$\mathrm{Log}\{q^{1/24}f(-q)\} = \frac{1}{24}\mathrm{Log}\,q - \sum_{k=1}^{\infty}q^k/(k(1-q^k))$）对 $q$ 求导、展开求和并交换求和次序得到；(iv) 由 Ch. 16 Entry 23(iv) 同法得到；(i) 由 Ch. 16 Entry 22(i) 与 (22.2)（$\varphi(q) = f(-q^2)\chi^2(q)$）结合 (iii)(iv) 得到；(ii) 由 Ch. 16 Entry 23(ii) 求导同法得到。(v) 的含义相当含糊（rather opaque），Berndt 称：拉马努金或许是指 Entry 1(i) 的一个更精确版本，或是指 (2.3)；(2.3) 未由拉马努金明言，Berndt 猜测 (v) 所指即此式。不幸的是，(2.3) 或相关公式 (5.3) 并非总能奏效；本章七条结果（Entry 8(i)(iii)、9(i)–(iii)、10(iii)、11）不得不借助 Ch. 20 发展的模形式理论来证明（见第 11 节）。

**状态：** (i)–(iv) 已证明（书中给出证明）；(v) 含义未定（拉马努金原话照录，Berndt 给出两种可能解释并证明了相应公式 (2.3)、(2.5)，但原意未确证）。**对照：** M06（Eisenstein 级数）、M07（$\varphi$、$\psi$、$f$、$\chi$ 的对数导数）。

**我自验：** 取 $q = 0.5$、$0.3$（mpmath 30 位，直接求和；对数导数由级数逐项求导直接计算）：(i) 差 $\le 3.2\times 10^{-30}$；(ii) 差 $\le 3.2\times 10^{-30}$；(iii) 差 $\le 9.5\times 10^{-30}$；(iv) 差 $\le 2.4\times 10^{-30}$。(2.5) 取 $n = 3$、$5$（$y = \pi/\sqrt{n}$、$y' = \pi\sqrt{n}$），差 $\le 4.0\times 10^{-31}$。(v) 为文字陈述，不作数值复核。

## Entry 3

**陈述。** $\varphi$、$\psi$、$f$ 如 Ch. 16 Entry 22。则

**(i)**

$$1 + 12\sum_{k=1}^{\infty}\frac{kq^k}{1-q^k} - 36\sum_{k=1}^{\infty}\frac{kq^{3k}}{1-q^{3k}}$$
$$= \left\{1 + 6\left(\frac{q}{1-q} - \frac{q^2}{1-q^2} + \frac{q^4}{1-q^4} - \frac{q^5}{1-q^5} + \cdots\right)\right\}^2$$
$$= \left\{1 + 24\sum_{k=1}^{\infty}\frac{k^3q^k}{1-q^k} + 216\sum_{k=1}^{\infty}\frac{k^3q^{3k}}{1-q^{3k}}\right\}^{1/2}$$
$$= \left\{\frac{\psi^4(q) + 3q\psi^4(q^3)}{\psi(q)\psi(q^3)}\right\}^2$$
$$= \left\{\frac{f^{12}(-q) + 27qf^{12}(-q^3)}{f^3(-q)f^3(-q^3)}\right\}^{2/3}.$$

**(ii)**

$$1 + 12\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 36\sum_{k=1}^{\infty}\frac{kq^{6k}}{1-q^{6k}}$$
$$= \left\{\frac{\varphi^4(q) + 3\varphi^4(q^3)}{4\varphi(q)\varphi(q^3)}\right\}^2$$
$$= \varphi^2(q)\varphi^2(q^3) - 4q\psi^2(-q)\psi^2(-q^3).$$

**(iii)** Let $\beta$ have degree $3$ with respect to $\alpha$. Then

$$1 + 12\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 36\sum_{k=1}^{\infty}\frac{kq^{6k}}{1-q^{6k}} = \frac{1}{2}\varphi^2(q)\varphi^2(q^3)\{1 + \sqrt{\alpha\beta} + \sqrt{(1-\alpha)(1-\beta)}\}.$$

**说明。**拉马努金用变量 $y$（$q = e^{-y}$）表述 (iii)。证明顺序为先 (ii)(iii) 后 (i)：在 (2.3) 中取 $n = 3$ 得 $S := 1 + 12\sum kq^{2k}/(1-q^{2k}) - 36\sum kq^{6k}/(1-q^{6k}) = \frac{1}{2}\alpha(1-\alpha)z_1^2\frac{d}{d\alpha}\mathrm{Log}(\beta(1-\beta)/(m^6\alpha(1-\alpha)))$（式 (3.1)）；用 Ch. 19 的 (5.2)、(5.5) 化为 $S = \varphi^6(q^3)/(16\varphi^2(q))\cdot(\varphi^4(q)/\varphi^4(q^3) + 3)^2$（式 (3.3)），由此得 (ii) 的第一等式与 (iii)；(ii) 的第二等式用 (3.3) 与 (3.2) 及 Ch. 17 Entry 11(ii)。(i) 的第一与第四表达式之等：由 (3.3) 与 Ch. 19 的 (5.1)，经 $q^2$ 换 $q$ 得 (3.4)；第二与第四表达式之等：由 Ch. 17 Entry 11(i)、Ch. 19 的 (5.2)(5.3) 与 Ch. 17 Entry 11(iii)，得 $\varphi(q)\varphi(q^3) + 4q\psi(q^2)\psi(q^6) = 1 + 6(q/(1-q) - q^2/(1-q^2) + q^4/(1-q^4) - q^5/(1-q^5) + \cdots)$（式 (3.5)(3.6)，用 Ch. 19 Entry 3(i)(ii) 处理偶指标求和项）；第三与第四表达式之等：由 Ch. 17 Entry 13(i) 与 (3.2)，化为 $\{\psi^3(q^2)/\psi(q^6) + 3q^2\psi^3(q^6)/\psi(q^2)\}^4$ 的形式（书页 463）。(i) 的第五表达式由 Ch. 16 Entry 24(i)(iii)、Ch. 20 Entry 1(i)(iv) 与 $v$ 的定义（Ch. 20 Entry 1）及 (3.7)（$f(-q) = f(q)\chi(-q)/\chi(q) = f(-q^2)\chi(-q) = \psi(q)\chi^2(-q)$）得到。

**状态：** 已证明（书中给出证明）。**对照：** M06（Eisenstein 级数与 3 次模）、M07（theta 函数）、M02（(i) 第二表达式的 Lambert 级数：按 (3.6)，通项为 $q^{3m+1}/(1-q^{3m+1}) - q^{3m+2}/(1-q^{3m+2})$）。

**我自验：** 取 $q = 0.5$、$0.3$（mpmath 30 位，直接求和；Lambert 级数按 (3.6) 的 $3m+1$、$3m+2$ 模式求和）：(i) 五个表达式两两之差 $\le 3.0\times 10^{-29}$；(ii) 两式差 $\le 1.6\times 10^{-30}$；(iii) 差 $\le 2.8\times 10^{-29}$（$\alpha$、$\beta$ 用 theta 路线，见 Ch. 20 章首）。

## Entry 4

**陈述。** $\varphi$、$\psi$、$f$、$\chi$ 如 Ch. 16 Entry 22。则

**(i)**

$$1 + 6\sum_{k=1}^{\infty}\frac{kq^k}{1-q^k} - 30\sum_{k=1}^{\infty}\frac{kq^{5k}}{1-q^{5k}}$$
$$= \frac{\{f^{12}(-q) + 22qf^6(-q)f^6(-q^5) + 125q^2f^{12}(-q^5)\}^{1/2}}{f(-q)f(-q^5)}$$
$$= \frac{\psi^4(q) + 2q\psi^2(q)\psi^2(q^5) + 5q^2\psi^4(q^5)}{\psi(q)\psi(q^5)}\times\{\psi^4(q) - 2q\psi^2(q)\psi^2(q^5) + 5q^2\psi^4(q^5)\}^{1/2}.$$

**(ii)**

$$1 + 6\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 30\sum_{k=1}^{\infty}\frac{kq^{10k}}{1-q^{10k}}$$
$$= \{\varphi^2(q)\varphi^2(q^5) - 2qf^2(-q^2)f^2(-q^{10})\}\left(1 - \frac{4q}{\chi^4(q)\chi^4(q^5)}\right)^{1/2}.$$

**(iii)** Let $\beta$ have degree $5$ over $\alpha$. Then

$$1 + 6\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 30\sum_{k=1}^{\infty}\frac{kq^{10k}}{1-q^{10k}}$$
$$= \frac{1}{4}\varphi^2(q)\varphi^2(q^5)\{3 + \sqrt{\alpha\beta} + \sqrt{(1-\alpha)(1-\beta)}\}\times\left(\frac{1}{2}\{1 + \sqrt{\alpha\beta} + \sqrt{(1-\alpha)(1-\beta)}\}\right)^{1/2}$$
$$= \varphi^2(q)\varphi^2(q^5)\left(\frac{1}{2}\{1 + \alpha\beta + (1-\alpha)(1-\beta)\} - \frac{3}{4}\{16\alpha\beta(1-\alpha)(1-\beta)\}^{1/3}\right)^{1/2}.$$

**说明。**拉马努金用变量 $y$（$q = e^{-y}$）表述 (iii)。(i) 的证明：在 (2.3) 中取 $n = 5$ 得 $S = \frac{1}{4}\alpha(1-\alpha)z_1^2\frac{d}{d\alpha}\mathrm{Log}(\beta(1-\beta)/(m^6\alpha(1-\alpha)))$（式 (4.1)）；用 Ch. 19 的 (14.2) 对 $m$ 求导、(14.2)(14.4) 与 Ch. 19 Entry 14(ii)（代换 $p = (m-1)/2$）及 $\rho$ 的定义（Ch. 19 (13.3)），得 $S = \rho(m^2+2m+5)z_1^2/(16m^3)$（式 (4.3)）；再用 Ch. 17 Entry 12(iii) 与 Ch. 19 Entry 13(iv) 化为 (4.4)，换 $q^2$ 为 $q$ 得 (i) 的第一等式；(i) 的第二等式由 (4.3)、$m = \varphi^2(q)/\varphi^2(q^5)$ 与 (4.4) 的 $q$ 变号不变性，经 (4.5)(4.6)（化为模方程）与 Ch. 17 Entry 11(iii) 得到。(ii) 的证明：由 Ch. 17 Entry 12(iii) 与 Ch. 19 的 (13.8)，$1 - 2qf^2(-q)f^2(-q^{10})/(\varphi^2(q)\varphi^2(q^5)) = (m^2+2m+5)/(8m)$（式 (4.7)）；由 Ch. 17 Entry 12(v) 与 (13.8)，$1 - 4q/(\chi^4(q)\chi^4(q^5)) = \rho^2/(4m^2)$（式 (4.8)）；两式相乘并用 (4.3) 即得。(iii) 的证明：由 Ch. 19 的 (13.7)，$\{\frac{1}{2}(1 + \sqrt{\alpha\beta} + \sqrt{(1-\alpha)(1-\beta)})\}^{1/2} = \rho/(2m)$（式 (4.9)），结合 (4.10) 得第一等式；第二等式由 (13.7)(13.8) 与 (13.3) 经冗长代数得到（Berndt 注明“我们略去了大量繁琐代数”）。

**状态：** 已证明（书中给出证明）。**对照：** M06（Eisenstein 级数与 5 次模）、M07（theta 函数）、M11。

**我自验：** 取 $q = 0.5$、$0.3$（mpmath 30 位，直接求和；(iii) 用 theta 路线）：(i) 两式差 $\le 7.9\times 10^{-30}$；(ii) 差 $\le 1.6\times 10^{-30}$；(iii) 两式差 $\le 3.7\times 10^{-28}$。

## Entry 5

**陈述。** $\varphi$、$\psi$、$f$ 如 Ch. 16 Entry 22。则

**(i)**

$$1 + 4\sum_{k=1}^{\infty}\frac{kq^k}{1-q^k} - 28\sum_{k=1}^{\infty}\frac{kq^{7k}}{1-q^{7k}}$$
$$= \left\{1 + 2\left(\frac{q}{1-q} + \frac{q^2}{1-q^2} - \frac{q^3}{1-q^3} + \frac{q^4}{1-q^4} - \frac{q^5}{1-q^5} - \frac{q^6}{1-q^6} + \frac{q^8}{1-q^8} + \cdots\right)\right\}^2$$
$$= \left\{\frac{f^8(-q) + 13qf^4(-q)f^4(-q^7) + 49q^2f^8(-q^7)}{f(-q)f(-q^7)}\right\}^{2/3}.$$

中间表达式的系数循环长度为 7。

**(ii)**

$$1 + 4\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 28\sum_{k=1}^{\infty}\frac{kq^{14k}}{1-q^{14k}} = \{\varphi(q)\varphi(q^7) - 2q\psi(-q)\psi(-q^7)\}^2.$$

**(iii)** Let $\beta$ have degree $7$ over $\alpha$. Then

$$1 + 4\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 28\sum_{k=1}^{\infty}\frac{kq^{14k}}{1-q^{14k}} = \frac{1}{2}\varphi^2(q)\varphi^2(q^7)\{1 + \sqrt{\alpha\beta} + \sqrt{(1-\alpha)(1-\beta)}\}.$$

本条证明所用的 (2.3) 的 $-q$ 类比（式 (5.3)）：设 $\beta$ 为 $\alpha$ 的 $n$ 次模，则

$$(5.3)\quad 1 - 24\sum_{k=1}^{\infty}\frac{k(-q)^k}{1-(-q)^k} - n\left(1 - 24\sum_{k=1}^{\infty}\frac{k(-q^n)^k}{1-(-q^n)^k}\right) = -\alpha(1-\alpha)z_1^2\frac{d}{d\alpha}\mathrm{Log}\left(\frac{\beta(1-\beta)}{m^{12}\alpha(1-\alpha)}\right).$$

**说明。**(i) 的证明：先在 (i) 左端以 $-q$ 代 $q$，用 (5.3) 的推导（式 (5.1)(5.2)，其中 $q^2$ 换为 $-q$）得 $S := 1 + 4\sum k(-q)^k/(1-(-q)^k) - 28\sum k(-q^7)^k/(1-(-q^7)^k) = \frac{1}{6}\alpha(1-\alpha)z_1^2\frac{d}{d\alpha}\mathrm{Log}(\beta(1-\beta)/(m^{12}\alpha(1-\alpha)))$；用 Ch. 19 的 (19.17)（$t$ 的定义见 (19.2)）与 (5.5)(5.6) 化为 (5.4)(5.7)；用 (19.23)、(19.20)(19.22)（$m - 7/m = -6 + 16t - 12t^2 + 8t^3$，$m + 7/m = 4R$，$R$ 由 (19.6) 定义）与 $(dt/d\alpha)(dt/d\beta)$ 的计算（式 (5.11)，$\alpha > t$、$\beta < t$）得 $S = z_1z_7(1-2t+2t^2)^2 = z_1z_7\{(1-t)^2+t^2\}^2$（式 (5.13)，代数由计算机代数包完成）；再用 (19.2)(19.3) 与 Ch. 17 Entry 10(ii)、11(iii) 得 $S = \{\varphi(-q)\varphi(-q^7) + 4q^2\psi(q^2)\psi(q^{14})\}^2$（式 (5.14)）；用 Ch. 19 Entry 17(i)(ii) 得 (5.15)（系数循环长度为 7）；变 $q$ 的符号并结合 (5.14)(5.15) 得 (i) 的第一等式。(i) 的第二等式：由 Ch. 17 Entry 12(i)、(19.2)(19.3) 得 $\{2q/(t(1-t))\}^{2/3}f^2(q)f^2(q^7) = z_1z_7$，结合 (5.16)(5.17)（$f^4(q)/(qf^4(q^7)) + 49qf^4(q^7)/f^4(q)$ 的 $t$ 表达式）得 $z_1z_7(1-2t+2t^2)^2 = ([f^8(q) + 49q^2f^8(q^7) - 13qf^4(q)f^4(q^7)]/(f(q)f(q^7)))^{2/3}$；变 $q$ 的符号（$-13q$ 变 $+13q$）即得。(ii)(iii) 的证明：在 (5.14) 中以 $-q^2$ 代 $q$ 得 (5.18)，用 Ch. 17 Entry 10(iv)、11(iv)、Ch. 20 的 (20.6)、Ch. 19 的 (19.2)(19.3) 得 (5.19)，代入 (5.18) 得 (ii)，再代入 (5.19) 的第二表达式得 (iii)。

**状态：** 已证明（书中给出证明）。**对照：** M06（Eisenstein 级数与 7 次模）、M07（theta 函数）、M02（(i) 中间表达式的 Lambert 级数：系数以 7 为周期，$n \bmod 7 = 1,2,3,4,5,6,0$ 的系数依次为 $+1,+1,-1,+1,-1,-1,0$）、M14（$t$、$R$ 参数化，见证明）。

**我自验：** 取 $q = 0.5$、$0.3$（mpmath 30 位，直接求和；(i) 中间 Lambert 级数按 7 周期系数求和到 $n = 499$）：(i) 两式差 $\le 4.8\times 10^{-30}$；(ii) 差 $\le 7.9\times 10^{-31}$；(iii) 差 $\le 5.0\times 10^{-29}$（theta 路线）。注意 (i) 第三表达式（$f$ 形式）的系数为 $+13q$，而证明中的 (5.17) 式对应 $+q$ 版本为 $-13q$，变号后一致，已核对。

## Entry 6

**陈述。** $\varphi$、$\psi$、$f$ 如 Ch. 16 Entry 22。则

**(i)** If $\beta$ has degree $3$, then

$$1 + 12\sum_{k=1}^{\infty}\frac{k(-q)^k}{1-(-q)^k} - 36\sum_{k=1}^{\infty}\frac{k(-q)^{3k}}{1-(-q)^{3k}} = \varphi^2(q)\varphi^2(q^3)\{(\alpha\beta)^{1/4} - \{(1-\alpha)(1-\beta)\}^{1/4}\}^2.$$

**(ii)** If $\beta$ has degree $5$, then

$$1 + 6\sum_{k=1}^{\infty}\frac{k(-q)^k}{1-(-q)^k} - 30\sum_{k=1}^{\infty}\frac{k(-q)^{5k}}{1-(-q)^{5k}}$$
$$= \varphi^2(q)\varphi^2(q^5)(\sqrt{\alpha\beta} + \sqrt{(1-\alpha)(1-\beta)})\times\left(\frac{1}{2}\{1 + \sqrt{\alpha\beta} + \sqrt{(1-\alpha)(1-\beta)}\}\right)^{1/2}.$$

**(iii)** If $\beta$ has degree $7$, then

$$1 + 4\sum_{k=1}^{\infty}\frac{k(-q)^k}{1-(-q)^k} - 28\sum_{k=1}^{\infty}\frac{k(-q)^{7k}}{1-(-q)^{7k}} = \varphi^2(q)\varphi^2(q^7)\{(\alpha\beta)^{1/4} + \{(1-\alpha)(1-\beta)\}^{1/4}\}^2.$$

**说明。**(i) 的证明：由 Entry 3(i)，左端级数等于 $\Psi := \{(\psi^4(-q) - 3q\psi^4(-q^3))/(\psi(-q)\psi(-q^3))\}^2$；用 Ch. 17 Entry 11(ii) 与 Ch. 19 的 (5.2)(5.5) 化为 $z_1z_3\{(1-\alpha)(1-\beta)\}^{1/4} - (\alpha\beta)^{1/4}\}^2$（式 (6.1)）。(ii) 的证明：由 Entry 4(i)，左端等于 $\Psi := [\psi^4(-q) - 2q\psi^2(-q)\psi^2(-q^5) + 5q^2\psi^4(-q^5)]/[\psi(-q)\psi(-q^5)]\times\{\psi^4(-q) + 2q\psi^2(-q)\psi^2(-q^5) + 5q^2\psi^4(-q^5)\}^{1/2}$；用 Ch. 17 Entry 11(ii) 与 Ch. 19 的 (14.2)(14.4)，化为 $\Psi = z_1z_5(\sqrt{\alpha\beta} + \sqrt{(1-\alpha)(1-\beta)})(\frac{1}{2}\{1 + \sqrt{\alpha\beta} + \sqrt{(1-\alpha)(1-\beta)}\})^{1/2}$（式 (6.2) 及后续计算，用 Ch. 17 Entry 11(ii) 与 Ch. 19 的 (13.3)–(13.5)、(13.6)(13.7)）。(iii) 的证明：(5.14) 式正是 Entry 6(iii)，故证明已在 Entry 5 中完成。

**状态：** 已证明（书中给出证明）。**对照：** M06（Eisenstein 级数与 3、5、7 次模）、M07（theta 函数）、M11。

**我自验：** 取 $q = 0.5$、$0.3$（mpmath 30 位，直接求和；交错级数 $\sum k(-q)^{nk}/(1-(-q)^{nk})$ 直接求和）：(i) 差 $\le 1.6\times 10^{-27}$；(ii) 差 $\le 9.8\times 10^{-29}$；(iii) 差 $\le 1.2\times 10^{-27}$（theta 路线）。

## Entry 7

**陈述。** $\varphi$、$\psi$、$f$ 如 Ch. 16 Entry 22。则

**(i)**

$$1 + 3\sum_{k=1}^{\infty}\frac{kq^k}{1-q^k} - 27\sum_{k=1}^{\infty}\frac{kq^{9k}}{1-q^{9k}}$$
$$= \frac{f^6(-q^3)}{f^2(-q)f^2(-q^9)}\{f^6(-q) + 9qf^3(-q)f^3(-q^9) + 27q^2f^6(-q^9)\}^{1/3}$$
$$= \left\{\frac{\psi^4(q^3) + 3q\psi^2(q)\psi^2(q^9)}{\psi(q)\psi(q^9)}\right\}^2\cdot\frac{\psi^2(q^3)}{\psi(q)\psi(q^9)}.$$

**(ii)**

$$1 + 3\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 27\sum_{k=1}^{\infty}\frac{kq^{18k}}{1-q^{18k}} = \left\{\frac{\varphi^4(q^3) + 3\varphi^2(q)\varphi^2(q^9)}{4}\right\}^2\cdot\frac{\varphi^2(q^3)}{\varphi^3(q)\varphi^3(q^9)}.$$

**(iii)**

$$1 + \sum_{k=1}^{\infty}\frac{kq^k}{1-q^k} - 25\sum_{k=1}^{\infty}\frac{kq^{25k}}{1-q^{25k}} = \frac{f^5(-q^5)}{f(-q)f(-q^{25})}\{f^2(-q) + 2qf(-q)f(-q^{25}) + 5q^2f^2(-q^{25})\}^{1/2}.$$

**说明。**(i)(ii) 的证明用 Ch. 20 第 3 节的记号（$\alpha$、$\beta$、$\gamma$ 的次数依次为 1、3、9；$m$、$m'$ 为相应乘子；$t$ 由 Ch. 20 (3.10)(3.11) 定义）。(i)：先变号，由 (6.1) 得 $S := 1 + 3\sum k(-q)^k/(1-(-q)^k) - 27\sum k(-q)^{9k}/(1-(-q)^{9k}) = \frac{1}{4}z_1z_3((3-m^2)/(2m))^2 + \frac{3}{4}z_3z_9((3-m'^2)/(2m'))^2$（式 (7.1)）；用 Ch. 20 的 (3.10)(3.11) 与 (7.1) 化为 $S = z_3z_9(1+t+t^2)(1-2t+4t^2)^2/(1+2t)$（式 (7.2)）；用 Ch. 17 Entry 12(i) 与 Ch. 20 的 (3.7)–(3.11) 化为 (7.3)，再证 (7.4)（$f^3(q)/(qf^3(q^9)) = (1+2t)^2(1-t)/t$）并变 $q$ 的符号，得 (i) 的第一等式；(i) 的第二等式由 (7.2)、(7.5)（$S = q^2\psi^2(-q^3)\psi(-q)\psi(-q^9)((1-2t+4t^2)/(t(1-t)))^2$）与 (7.6)（$\psi^4(-q^3)/(q\psi^2(-q)\psi^2(-q^9)) = (1+t+t^2)/(t(1-t))$）得到。(ii) 的证明：由 (i)，左端级数等于 $T := q^{2/3}f^6(-q^6)/(f(-q^2)f(-q^{18}))\cdot(f^3(-q^2)/(q^2f^3(-q^{18})) + 9 + 27q^2f^3(-q^{18})/f^3(-q^2))$；用 Ch. 17 Entry 12(iii) 与 Ch. 20 的 (3.7)–(3.11) 化为 (7.7)，即得。(iii) 的证明：置 $w = f(-q)/(qf(-q^{25}))$（式 (7.8)，为 Ch. 19 (11.7) 的变体）；由 Entry 4(i) 与 Ch. 19 的 (11.8)，把 $1 + 6\sum kq^k/(1-q^k) - 30\sum kq^{5k}/(1-q^{5k})$ 与 $1 + 6\sum kq^{5k}/(1-q^{5k}) - 30\sum kq^{25k}/(1-q^{25k})$ 表为 $w$ 的多项式（式 (7.9)(7.10)）；前者乘 $1/6$、后者乘 $5/6$ 相加，再用 Ch. 19 的 (11.8) 与 (7.8)，即得 (iii)。

**状态：** 已证明（书中给出证明）。**对照：** M06（Eisenstein 级数与 9、25 次模）、M07（theta 函数）、M11。

**我自验：** 取 $q = 0.5$、$0.3$（mpmath 30 位，直接求和）：(i) 两式差 $\le 9.1\times 10^{-30}$；(ii) 差 $\le 1.2\times 10^{-30}$（分母确为 $\varphi^3(q)\varphi^3(q^9)$：按 $\varphi^2(q)\varphi^2(q^9)$ 计差 $2.97$、$0.83$，不成立）；(iii) 差 $\le 7.9\times 10^{-31}$。

## Entry 8

**陈述。** $\varphi$、$\psi$、$f$、$\chi$ 如 Ch. 16 Entry 22（$f(q)$ 为单变量记号，见章首）。则

**(i)**

$$5 + 12\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 132\sum_{k=1}^{\infty}\frac{kq^{22k}}{1-q^{22k}}$$
$$= 5\varphi^2(q)\varphi^2(q^{11}) - 20qf^2(q)f^2(q^{11}) + 32q^2f^2(-q^2)f^2(-q^{22}) - 20q^3\psi^2(-q)\psi^2(-q^{11}).$$

**(ii)** Let $\beta$ have degree $11$ over $\alpha$. Then

$$5 + 12\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 132\sum_{k=1}^{\infty}\frac{kq^{22k}}{1-q^{22k}}$$
$$= \varphi^2(q)\varphi^2(q^{11})(2 + 2(\alpha\beta)^{1/2} + 2\{(1-\alpha)(1-\beta)\}^{1/2} + (\alpha\beta)^{1/4} + \{(1-\alpha)(1-\beta)\}^{1/4} - \{\alpha\beta(1-\alpha)(1-\beta)\}^{1/4}).$$

**(iii)** If $\beta$ has degree $19$, then

$$3 + 4\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 76\sum_{k=1}^{\infty}\frac{kq^{38k}}{1-q^{38k}}$$
$$= \varphi^2(q)\varphi^2(q^{19})(1 + (\alpha\beta)^{1/2} + \{(1-\alpha)(1-\beta)\}^{1/2} + (\alpha\beta)^{1/4} + \{(1-\alpha)(1-\beta)\}^{1/4} - \{\alpha\beta(1-\alpha)(1-\beta)\}^{1/4}).$$

**说明。**Berndt 注明：用 (2.3) 或 (5.3) 既证不出 (i) 也证不出 (iii)；故 (i)(iii) 的证明推迟到第 11 节，用模形式理论建立（见第 11 节的 (11.8)、(11.9) 与 (11.2)）。(ii) 由 (i) 推出，是本节给出的唯一证明：由 Ch. 17 Entry 11(ii)、12(i)(iii) 与 Ch. 20 Entry 7(i)，(i) 的右端化为 $z_1z_{11}(5 - 20\cdot 2^{-2/3}\{\alpha(1-\alpha)\beta(1-\beta)\}^{1/12} + 32\cdot 2^{-4/3}\{\alpha(1-\alpha)\beta(1-\beta)\}^{1/6} - 5\{\alpha(1-\alpha)\beta(1-\beta)\}^{1/4}) = z_1z_{11}(2 + 2(\alpha\beta)^{1/2} + 2\{(1-\alpha)(1-\beta)\}^{1/2} + (\alpha\beta)^{1/4} + \{(1-\alpha)(1-\beta)\}^{1/4} - \{\alpha\beta(1-\alpha)(1-\beta)\}^{1/4})$，即 (ii)。

**状态：** 已证明（(ii) 在本节证明；(i)(iii) 在第 11 节用模形式理论证明）。**对照：** M06（Eisenstein 级数与 11、19 次模；第 11 节的模形式证明）、M07（theta 函数）。

**我自验：** 取 $q = 0.5$、$0.2$（mpmath 30 位，直接求和；(ii)(iii) 用 theta 路线）：(i) 按单变量 $f(q) = \prod_{n\ge 1}(1-(-q)^n)$ 计差 $\le 4.8\times 10^{-30}$；(ii) 差 $\le 8.4\times 10^{-28}$；(iii) 差 $\le 9.4\times 10^{-28}$。第 11 节的 theta 翻译 (11.2)（即 (iii) 的 theta 形式）亦复核通过，差 $\le 7.9\times 10^{-31}$。

## Entry 9

**陈述。** $\varphi$、$\psi$、$f$ 如 Ch. 16 Entry 22。则

**(i)**

$$11 + 12\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 276\sum_{k=1}^{\infty}\frac{kq^{46k}}{1-q^{46k}}$$
$$= \varphi^2(q)\varphi^2(q^{23})\left\{\frac{11}{2}(1 + \sqrt{\alpha\beta} + \sqrt{(1-\alpha)(1-\beta)}) - 10\{16\alpha\beta(1-\alpha)(1-\beta)\}^{1/6}\right.$$
$$\left. - 8\{16\alpha\beta(1-\alpha)(1-\beta)\}^{1/12}(1 + (\alpha\beta)^{1/4} + \{(1-\alpha)(1-\beta)\}^{1/4})\right\},$$

其中 $\beta$ 为 $\alpha$ 的 23 次模（书中 (i) 未明言次数，由 $\varphi^2(q^{23})$ 与 $q^{46k}$ 知次数为 23，见待核对清单）。

**(ii)** If $\beta$ is of degree $15$, then

$$7 + 12\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 180\sum_{k=1}^{\infty}\frac{kq^{30k}}{1-q^{30k}}$$
$$= \frac{1}{2}\varphi^2(q)\varphi^2(q^{15})\left\{\{1 + (\alpha\beta)^{1/8} + \{(1-\alpha)(1-\beta)\}^{1/8}\}^4 - 1 - \sqrt{\alpha\beta} - \sqrt{(1-\alpha)(1-\beta)}\right\}.$$

**(iii)** If $\beta$ is of degree $31$, then

$$5 + 4\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 124\sum_{k=1}^{\infty}\frac{kq^{62k}}{1-q^{62k}}$$
$$= \varphi^2(q)\varphi^2(q^{31})\left\{\frac{1}{2}\{1 + \sqrt{\alpha\beta} + \sqrt{(1-\alpha)(1-\beta)}\} + \{1 + (\alpha\beta)^{1/4} + \{(1-\alpha)(1-\beta)\}^{1/4}\}^2\right.$$
$$\left. - 2\{\alpha\beta(1-\alpha)(1-\beta)\}^{1/8}\{1 + (\alpha\beta)^{1/8} + \{(1-\alpha)(1-\beta)\}^{1/8}\}\right\}.$$

**说明。**本条证明全部推迟到第 11 节，用模形式理论建立（见第 11 节的 (11.3)–(11.5) 与 (11.10)–(11.12)）。

**状态：** 已证明（第 11 节用模形式理论证明）。**对照：** M06（Eisenstein 级数与 23、15、31 次模；第 11 节的模形式证明）、M07、M11。

**我自验：** 取 $q = 0.5$、$0.2$（mpmath 30 位，直接求和；右端用 theta 路线）：(i) 差 $\le 1.1\times 10^{-26}$；(ii) 差 $\le 1.7\times 10^{-26}$；(iii) 差 $\le 1.5\times 10^{-27}$。第 11 节的 theta 翻译 (11.3)、(11.4)、(11.5) 亦复核通过，差 $\le 1.6\times 10^{-30}$。

## Entry 10

**陈述。** $\varphi$、$\psi$、$f$ 如 Ch. 16 Entry 22。则

**(i)** Let $\beta$ have degree $5$ with respect to $\alpha$. Then

$$1 + 6\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 30\sum_{k=1}^{\infty}\frac{kq^{10k}}{1-q^{10k}}$$
$$= \varphi^2(q)\varphi^2(q^5)\left(\frac{1}{2}\{1 + \alpha\beta + (1-\alpha)(1-\beta)\} - \frac{3}{16}\{1 - \sqrt{\alpha\beta} - \sqrt{(1-\alpha)(1-\beta)}\}^2\right)^{1/2}.$$

**(ii)** If $\beta$ has degree $9$, then

$$1 + 3\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 27\sum_{k=1}^{\infty}\frac{kq^{18k}}{1-q^{18k}}$$
$$= \varphi^2(q)\varphi^2(q^9)\left(\frac{1}{2}\{1 + \alpha\beta + (1-\alpha)(1-\beta)\} - \frac{9}{32}\{1 - \sqrt{\alpha\beta} - \sqrt{(1-\alpha)(1-\beta)}\}^2\right.$$
$$\left. + \frac{3}{2}\cdot\frac{\{\alpha\beta(1-\alpha)(1-\beta)\}^{1/2}}{1 - (\alpha\beta)^{1/2} - \{(1-\alpha)(1-\beta)\}^{1/2}}\right)^{1/2}.$$

**(iii)** If $\beta$ is of degree $17$, then

$$2 + 3\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 51\sum_{k=1}^{\infty}\frac{kq^{34k}}{1-q^{34k}}$$
$$= \varphi^2(q)\varphi^2(q^{17})\left(2\{1 + \alpha\beta + (1-\alpha)(1-\beta)\} - \frac{21}{16}\{1 - \sqrt{\alpha\beta} - \sqrt{(1-\alpha)(1-\beta)}\}^2\right.$$
$$\left. - \frac{51}{32}\{1 - \sqrt{\alpha\beta} - \sqrt{(1-\alpha)(1-\beta)}\}\{16\alpha\beta(1-\alpha)(1-\beta)\}^{1/6} - 3\{16\alpha\beta(1-\alpha)(1-\beta)\}^{1/3}\right)^{1/2}.$$

**说明。**(i) 的证明：与 Entry 4(iii) 比较，只需证 $\{1 - \sqrt{\alpha\beta} - \sqrt{(1-\alpha)(1-\beta)}\}^2 = 4\{16\alpha\beta(1-\alpha)(1-\beta)\}^{1/3}$，此式由 Ch. 19 Entry 13(i) 立得。(ii) 的证明：用第 7 节的记号、(7.7) 与 Ch. 20 的 (3.10)(3.11)，左端等于 $z_1z_9(m'/m)^{1/2}((1+t+t^2)/(1+2t))^2 = z_1z_9(1+8t^3)^{1/2}/(1+2t)\cdot((1+t+t^2)/(1+2t))^2 = z_1z_9(1-2t+4t^2)^{1/2}(1+t+t^2)^2/(1+2t)^{5/2}$（式 (10.1)）；再用 Ch. 20 的 (3.17)、(3.7)、(3.9) 得 (10.2)(10.3)，经冗长计算得 (10.4)，结合 (10.2)–(10.4) 即得 (ii)。(iii) 的证明推迟到第 11 节（见 (11.6) 与 (11.13)，左端取平方后化为权 4 模形式）。

**状态：** 已证明（(i)(ii) 在本节证明；(iii) 在第 11 节用模形式理论证明）。**对照：** M06（Eisenstein 级数与 5、9、17 次模）、M07、M11。

**我自验：** 取 $q = 0.5$、$0.2$（mpmath 30 位，直接求和；右端用 theta 路线）：(i) 差 $\le 7.9\times 10^{-30}$；(ii) 差 $\le 7.0\times 10^{-29}$；(iii) 差 $\le 4.9\times 10^{-28}$。第 11 节的 theta 翻译 (11.6)（(iii) 左端平方的 theta 形式）亦复核通过，差 $\le 7.9\times 10^{-30}$。

## Entry 11

**陈述。** If $\beta$ has degree $35$ over $\alpha$, then

$$17 + 12\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 420\sum_{k=1}^{\infty}\frac{kq^{70k}}{1-q^{70k}}$$
$$= \varphi^2(q)\varphi^2(q^{35})\left(\frac{(1 - (\alpha\beta)^{1/4} - \{(1-\alpha)(1-\beta)\}^{1/4})^3}{2\{16\alpha\beta(1-\alpha)(1-\beta)\}^{1/12}} + (\alpha\beta)^{1/4} + \{(1-\alpha)(1-\beta)\}^{1/4} - \{\alpha\beta(1-\alpha)(1-\beta)\}^{1/4}\right).$$

**说明。**事实上，Entry 11 在第二本笔记（p. 256）中列为 11(i)，但该节没有进一步的结果。证明在第 11 节：先把左端与右端翻译成 theta 恒等式 (11.7)，再改写为模形式恒等式 (11.14)，用赋值公式与 MACSYMA 验证 $q$ 展开系数到 $q^{72}$（见第 11 节的表）。

**状态：** 已证明（第 11 节用模形式理论证明）。**对照：** M06（Eisenstein 级数与 35 次模；第 11 节的模形式证明）、M07、M11。

**我自验：** 取 $q = 0.5$、$0.2$（mpmath 30 位，直接求和；右端用 theta 路线）：差 $\le 4.1\times 10^{-26}$（$q = 0.5$ 处，为 $\alpha\approx 1$ 的相对精度极限；$q = 0.2$ 时差 $4.7\times 10^{-29}$）。第 11 节的 theta 翻译 (11.7) 亦复核通过，差 $\le 2.3\times 10^{-29}$。**转录注意（分母指数）：** 150 DPI 原图上分母指数易误读为 $1/2$，300 DPI 放大图（PDF 页 498）确认确为 $1/12$；按 $1/2$ 计，$q = 0.5$ 时差约 $6.7\times 10^6$、$q = 0.2$ 时差约 $1.1\times 10^{11}$，不成立。

## 第 11 节——七条推迟公式的模形式证明

**定理。** 设

$$E_2(\tau) = 1 - 24\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}},$$

其中 $q = e^{\pi i\tau}$，$\tau\in\mathfrak{H}$。定义

$$F_n(\tau) = E_2(\tau) - nE_2(n\tau).$$

则 $F_n$ 为 $\Gamma_0(n)$ 上权 2、平凡乘子系的模形式。

证明思路（自写提要）：置 $E_2^*(\tau) = E_2(\tau) + 3/(\pi y)$（$y = \mathrm{Im}(\tau)$），则 $E_2^*$ 满足变换公式 $E_2^*(V\tau) = (c\tau+d)^2E_2^*(\tau) - (6ic/\pi)(c\tau+d)$（式 (11.1)，见 Rankin [2，pp. 194–195] 或 Schoeneberg [1，p. 68]）；而 $F_n(\tau) = E_2^*(\tau) - nE_2^*(n\tau)$，结合 (11.1) 与 Ch. 20 的 (0.4)，当 $V\in\Gamma_0(n)$ 时非全纯修正项相消，得 $F_n(V\tau) = (c\tau+d)^2F_n(\tau)$。

**七条推迟公式的证明。** 节标题为“Proofs of Entries 8(i), (iii), 9(i)–(iii), 10(iii), 11”（七条）。先用 Ch. 17 Entry 10(i)–(iii)、11(i)–(iii)、12(iii) 把其中六条（Entry 8(iii)、9(i)–(iii)、10(iii)、11）写成 theta 恒等式 (11.2)–(11.7)；Entry 8(i) 则由 Ch. 20 的 (0.13) 直接改写为模形式恒等式 (11.8)（故正文“those six entries”指 (11.2)–(11.7) 的六条，8(i) 为第七条，另行处理）：

$$(11.2)\quad 3 + 4\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 76\sum_{k=1}^{\infty}\frac{kq^{38k}}{1-q^{38k}} = \varphi^2(q)\varphi^2(q^{19}) + 16q^{10}\psi^2(q^2)\psi^2(q^{38}) + \varphi^2(-q)\varphi^2(-q^{19})$$
$$+ 4q^5\psi(q^2)\psi(q^{38})\varphi(q)\varphi(q^{19}) + \varphi(q)\varphi(q^{19})\varphi(-q)\varphi(-q^{19}) - 4q^5\psi(q^2)\psi(q^{38})\varphi(-q)\varphi(-q^{19}).$$

$$(11.3)\quad 11 + 12\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 276\sum_{k=1}^{\infty}\frac{kq^{46k}}{1-q^{46k}} = \frac{11}{2}(\varphi^2(q)\varphi^2(q^{23}) + 16q^{12}\psi^2(q^2)\psi^2(q^{46}) + \varphi^2(-q)\varphi^2(-q^{23}))$$
$$- 16q^2f(-q^2)f(-q^{46})(\varphi(q)\varphi(q^{23}) + 4q^6\psi(q^2)\psi(q^{46}) + \varphi(-q)\varphi(-q^{23})) - 40q^4f^2(-q^2)f^2(-q^{46}).$$

$$(11.4)\quad 7 + 12\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 180\sum_{k=1}^{\infty}\frac{kq^{30k}}{1-q^{30k}} = \frac{1}{2\varphi^2(q)\varphi^2(q^{15})}(\varphi(q)\varphi(q^{15}) + 2q^2\psi(q)\psi(q^{15}) + \varphi(-q^2)\varphi(-q^{30}))^4$$
$$- \frac{1}{2}(\varphi^2(q)\varphi^2(q^{15}) + 16q^8\psi^2(q^2)\psi^2(q^{30}) + \varphi^2(-q)\varphi^2(-q^{15})).$$

$$(11.5)\quad 5 + 4\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 124\sum_{k=1}^{\infty}\frac{kq^{62k}}{1-q^{62k}} = \frac{1}{2}(\varphi^2(q)\varphi^2(q^{31}) + 16q^{16}\psi^2(q^2)\psi^2(q^{62}) + \varphi^2(-q)\varphi^2(-q^{31}))$$
$$+ (\varphi(q)\varphi(q^{31}) + 4q^8\psi(q^2)\psi(q^{62}) + \varphi(-q)\varphi(-q^{31}))^2$$
$$- 4q^4\psi(-q)\psi(-q^{31})(\varphi(q)\varphi(q^{31}) + 2q^4\psi(q)\psi(q^{31}) + \varphi(-q^2)\varphi(-q^{62})).$$

$$(11.6)\quad \left(2 + 3\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 51\sum_{k=1}^{\infty}\frac{kq^{34k}}{1-q^{34k}}\right)^2 = 2(\varphi^4(q)\varphi^4(q^{17}) + 256q^{18}\psi^4(q^2)\psi^4(q^{34}) + \varphi^4(-q)\varphi^4(-q^{17}))$$
$$- \frac{21}{16}(\varphi^2(q)\varphi^2(q^{17}) - 16q^9\psi^2(q^2)\psi^2(q^{34}) - \varphi^2(-q)\varphi^2(-q^{17}))^2$$
$$- \frac{51}{8}q^3f^2(-q^2)f^2(-q^{34})(\varphi^2(q)\varphi^2(q^{17}) - 16q^9\psi^2(q^2)\psi^2(q^{34}) - \varphi^2(-q)\varphi^2(-q^{17})) - 48q^6f^4(-q^2)f^4(-q^{34}).$$

$$(11.7)\quad 17 + 12\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 420\sum_{k=1}^{\infty}\frac{kq^{70k}}{1-q^{70k}} = \frac{1}{4q^3f(-q^2)f(-q^{70})}(\varphi(q)\varphi(q^{35}) - 4q^9\psi(q^2)\psi(q^{70}) - \varphi(-q)\varphi(-q^{35}))^3$$
$$+ 4q^9\psi(q^2)\psi(q^{70})\varphi(q)\varphi(q^{35}) + \varphi(q)\varphi(q^{35})\varphi(-q)\varphi(-q^{35}) - 4q^9\psi^2(-q)\psi^2(-q^{35}).$$

再由 Ch. 20 的 (0.13) 把 Entry 8(i) 与 (11.2)–(11.7) 改写为模形式恒等式 (11.8)–(11.14)（$g_j$、$h_j$、$f_j$、$\eta$ 的定义见 Ch. 20 (0.13)；$\eta$ 为 Dedekind $\eta$ 函数）：

$$(11.8)\quad 5 + 12\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 132\sum_{k=1}^{\infty}\frac{kq^{22k}}{1-q^{22k}} = 5g_1^2(\tau)g_1^2(11\tau) - 20f_1^2(\tau)f_1^2(11\tau) + 32\eta^2(\tau)\eta^2(11\tau) - 20h_1^2(\tau)h_1^2(11\tau).$$

$$(11.9)\quad 3 + 4\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 76\sum_{k=1}^{\infty}\frac{kq^{38k}}{1-q^{38k}} = g_1^2(\tau)g_1^2(19\tau) + 16g_2^2(\tau)g_2^2(19\tau) + g_0^2(\tau)g_0^2(19\tau)$$
$$+ 4g_2(\tau)g_2(19\tau)g_1(\tau)g_1(19\tau) + g_1(\tau)g_1(19\tau)g_0(\tau)g_0(19\tau) - 4g_2(\tau)g_2(19\tau)g_0(\tau)g_0(19\tau).$$

$$(11.10)\quad 11 + 12\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 276\sum_{k=1}^{\infty}\frac{kq^{46k}}{1-q^{46k}} = \frac{11}{2}(g_1^2(\tau)g_1^2(23\tau) + 16g_2^2(\tau)g_2^2(23\tau) + g_0^2(\tau)g_0^2(23\tau))$$
$$- 16\eta(\tau)\eta(23\tau)(g_1(\tau)g_1(23\tau) + 4g_2(\tau)g_2(23\tau) + g_0(\tau)g_0(23\tau)) - 40\eta^2(\tau)\eta^2(23\tau).$$

$$(11.11)\quad 7 + 12\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 180\sum_{k=1}^{\infty}\frac{kq^{30k}}{1-q^{30k}} = \frac{1}{2g_1^2(\tau)g_1^2(15\tau)}(g_1(\tau)g_1(15\tau) + 2h_0(\tau)h_0(15\tau) + h_2(\tau)h_2(15\tau))^4$$
$$- \frac{1}{2}(g_1^2(\tau)g_1^2(15\tau) + 16g_2^2(\tau)g_2^2(15\tau) + g_0^2(\tau)g_0^2(15\tau)).$$

$$(11.12)\quad 5 + 4\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 124\sum_{k=1}^{\infty}\frac{kq^{62k}}{1-q^{62k}} = \frac{1}{2}(g_1^2(\tau)g_1^2(31\tau) + 16g_2^2(\tau)g_2^2(31\tau) + g_0^2(\tau)g_0^2(31\tau))$$
$$+ (g_1(\tau)g_1(31\tau) + 4g_2(\tau)g_2(31\tau) + g_0(\tau)g_0(31\tau))^2 - 4h_1(\tau)h_1(31\tau)(g_1(\tau)g_1(31\tau) + 2h_0(\tau)h_0(31\tau) + h_2(\tau)h_2(31\tau)).$$

$$(11.13)\quad \left(2 + 3\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 51\sum_{k=1}^{\infty}\frac{kq^{34k}}{1-q^{34k}}\right)^2 = 2(g_1^4(\tau)g_1^4(17\tau) + 256g_2^4(\tau)g_2^4(17\tau) + g_0^4(\tau)g_0^4(17\tau))$$
$$- \frac{21}{16}(g_1^2(\tau)g_1^2(17\tau) - 16g_2^2(\tau)g_2^2(17\tau) - g_0^2(\tau)g_0^2(17\tau))^2$$
$$- \frac{51}{8}\eta^2(\tau)\eta^2(17\tau)(g_1^2(\tau)g_1^2(17\tau) - 16g_2^2(\tau)g_2^2(17\tau) - g_0^2(\tau)g_0^2(17\tau)) - 48\eta^4(\tau)\eta^4(17\tau).$$

$$(11.14)\quad 17 + 12\sum_{k=1}^{\infty}\frac{kq^{2k}}{1-q^{2k}} - 420\sum_{k=1}^{\infty}\frac{kq^{70k}}{1-q^{70k}} = \frac{1}{4\eta(\tau)\eta(35\tau)}(g_1(\tau)g_1(35\tau) - 4g_2(\tau)g_2(35\tau) - g_0(\tau)g_0(35\tau))^3$$
$$+ 4g_2(\tau)g_2(35\tau)g_1(\tau)g_1(35\tau) + g_1(\tau)g_1(35\tau)g_0(\tau)g_0(35\tau) - 4h_1^2(\tau)h_1^2(35\tau).$$

各恒等式两侧每一项在 $\Gamma = \Gamma(2)\cap\Gamma_0(n)$（$n = 11$、$19$、$23$、$15$、$31$、$17$、$35$，依次对应 (11.8)–(11.14)）上的乘子系皆为平凡（用 Ch. 20 的 (0.14)、(0.16)、(0.18)–(0.23) 验证；(11.11) 另用 Ch. 20 (13.8) 后的注记，因 $3\mid n$）。清除 (11.11) 与 (11.14) 的分母后，每条恒等式写成 $F := F_1 + F_2 + \cdots + F_m = 0$；下表给出每条的权 $r$、由 Ch. 20 (0.6)(0.24) 算得的 $\rho_{\Gamma}$ 与由 (0.30) 定出的 $\mu$：

| 恒等式 | $r$ | $\rho_{\Gamma}$ | $\mu$ |
|---|---|---|---|
| (11.8) | 2 | 6 | 12 |
| (11.9) | 2 | 10 | 20 |
| (11.10) | 2 | 12 | 24 |
| (11.11) | 4 | 12 | 48 |
| (11.12) | 2 | 16 | 32 |
| (11.13) | 4 | 9 | 36 |
| (11.14) | 3 | 24 | 72 |

由 Ch. 20 (0.30) 的理论，只需验证 $F$ 的 $q^0$、$q^1$、$\dots$、$q^{\mu}$ 系数皆为 0，即得 $F\equiv 0$；Berndt 用计算机代数系统 MACSYMA 验证了所需系数皆为 0，(11.8)–(11.14) 由此得证，七条推迟公式的证明完成。

**我自验：** (11.2)–(11.7) 的 theta 形式已在各 Entry 的数值复核中逐条验证（见 Entry 8(iii)、9(i)–(iii)、10(iii)、11 的“我自验”）：取 $q = 0.5$、$0.2$，差 $\le 2.3\times 10^{-29}$（(11.3) 在 $q = 0.5$ 处差 $0$）。(11.8)–(11.14) 的模形式版本未另作数值复核（与 (11.2)–(11.7) 等价，见各 Entry）。

## Final Entry

**陈述。** 在 Entry 11 的陈述之后，拉马努金画了一条短横线，并在其下给出三条关于 $\varphi$ 在特定变元处的等式；虽然与 Ch. 21 的主题无关，但因其出现在 Ch. 21 的最后一页（笔记 p. 256），Berndt 在此给出证明。If the principal branch of each root is taken, then

$$(11.15)\quad \frac{\varphi(q) - \varphi(-q)}{\varphi(q) + \varphi(-q)} = \left(\frac{\varphi^2(q^2) - \varphi^2(-q^2)}{\varphi^2(q^2) + \varphi^2(-q^2)}\right)^{1/2} = \left(\frac{\varphi^4(q^4) - \varphi^4(-q^4)}{\varphi^4(q^4)}\right)^{1/4}$$

and

$$(11.16)\quad \{\varphi(q) + i\varphi(-q)\}^{1/2} = \left(\frac{\varphi(q) + \varphi(q^2)\sqrt{2}}{2}\right)^{1/2} + \left(\frac{\varphi(q) - \varphi(q^2)\sqrt{2}}{2}\right)^{1/2}.$$

**说明。**(11.15) 的第一个等式：平方并用 Ch. 17 Entry 10(i)–(iv)，等价于 $((1-(1-x)^{1/4})/(1+(1-x)^{1/4}))^2 = (\frac{1}{2}(1+\sqrt{1-x})-(1-x)^{1/4})/(\frac{1}{2}(1+\sqrt{1-x})+(1-x)^{1/4})$，显然成立。(11.15) 的第二个等式：取四次方，用 Ch. 17 Entry 10(i)(ii)(v) 与 (11.17)（$\varphi^4(-q^4) = \varphi^2(q^2)\varphi^2(-q^2) = \frac{1}{2}z^2(1+\sqrt{1-x})(1-x)^{1/4}$，由 (10.1) 与 Ch. 17 Entry 10(iii)(iv) 得到），化为 $((1-(1-x)^{1/4})/(1+(1-x)^{1/4}))^4 = (\frac{1}{16}(1+(1-x)^{1/4})^4 - \frac{1}{2}(1+\sqrt{1-x})(1-x)^{1/4})/(\frac{1}{16}(1+(1-x)^{1/4})^4)$，直接计算验证。(11.16)：两边平方，等价于 $\varphi(q) + i\varphi(-q) = \varphi(q) + \{\varphi^2(q) - 2\varphi^2(q^2)\}^{1/2}$；由 Ch. 17 Entry 10(i)(ii)(iv)，等价于 $1 + i(1-x)^{1/4} = 1 + \{1-(1+\sqrt{1-x})\}^{1/2}$，显然成立。Berndt 在章末注明：本章一些结果由 S. Ghosh 在其博士论文 [1] 中独立导出。

**状态：** 已证明（书中给出证明；未编号，笔记最后一页）。**对照：** M07（$\varphi$ 恒等式）。

**我自验：** 取 $q = 0.5$、$0.3$（mpmath 30 位，直接求和；主支根）：(11.15) 两等式差 $\le 2.0\times 10^{-31}$；(11.16) 差 $\le 4.0\times 10^{-31}$。

## 小结

本章共 11 条编号 Entry（Entry 1–11，无缺号），分体标题 34 个，另有未编号的 Final Entry（(11.15)(11.16)）；书页 454–488（35 页）。要点如下：

- Entry 1 为全章的主题陈述：Eisenstein 级数 $L$、$M$、$N$（(1.1)–(1.3)）与 (ii)–(iv) 的 $z$、$x$ 闭式；(i) 须补加 $y^2/\pi^2$ 为有理数的条件；(1.4) 把 $L/z^2$ 表为椭圆积分 $E/K$、$E'/K'$ 的组合。
- Entry 2 为全章的工具箱：$\varphi$、$\psi$、$f$、$\chi$ 的对数导数 (i)–(iv) 皆为 Eisenstein 级数；含义不明的 (v)（拉马努金原话照录）引出关键公式 (2.3) 与第二种解释 (2.5)。
- Entry 3–5 为 3、5、7 次 Eisenstein–theta 恒等式：Entry 3 的五表达式 (i)（Lambert 级数、$k^3$ 级数、$\psi$ 式、$f$ 式）、Entry 4 的 $f$ 式与 $\psi$ 式 (i) 及 $\chi$ 因子 (ii)、Entry 5 的 7 周期 Lambert 级数 (i) 与关键公式 (5.3)（(2.3) 的 $-q$ 类比）。
- Entry 6 为 Entry 3–5 的 $-q$ 版：3、5、7 次恒等式的 $\alpha$、$\beta$ 闭式；(iii) 即 Entry 5 证明中的 (5.14)。
- Entry 7 为 9 次与 25 次恒等式：(i) 的 $f$ 式与 $\psi$ 式、(ii) 的 $\varphi$ 式（分母为 $\varphi^3(q)\varphi^3(q^9)$）、(iii) 的 $w = f(-q)/(qf(-q^{25}))$ 参数化。
- Entry 8–11 为高次恒等式，七条（8(i)(iii)、9(i)–(iii)、10(iii)、11）用 (2.3)/(5.3) 证不出，推迟到第 11 节用模形式理论证明：Entry 8 的 11、19 次（(i) 的 $f(q)$ 为单变量 $f$）、Entry 9 的 23、15、31 次、Entry 10 的 5、9、17 次、Entry 11 的 35 次（笔记中列为 11(i)）。
- 第 11 节为全章的模形式收束：定理（$F_n(\tau) = E_2(\tau) - nE_2(n\tau)$ 为 $\Gamma_0(n)$ 上权 2 模形式）与七条推迟公式的 theta 翻译 (11.2)–(11.7) 及模形式版本 (11.8)–(11.14)（权、$\rho_{\Gamma}$、$\mu$ 见表；MACSYMA 验证 $q$ 展开系数到 $q^{\mu}$）。
- Final Entry（未编号，笔记最后一页 p. 256）为两条 $\varphi$ 恒等式 (11.15)(11.16)，与 Eisenstein 主题无关，Berndt 因其位置附于章末并给出证明；本章一些结果由 S. Ghosh 在其博士论文中独立导出。

数值复核：104 项真实数值检查全部通过，差 $< 1\times 10^{-25}$（mpmath 30 位，直接求和 + 解析尾项；$q$-Pochhammer 乘积截断到 1500 项、theta 双边和截断到 $\pm 150$ 项；模方程与 $\alpha$、$\beta$ 公式用 $\alpha(q) = (\theta_2/\theta_3)^4$ 的 theta 路线，$\theta_2 = 2q^{1/4}\psi(q^2)$、$\theta_3 = \varphi(q)$，$m = \varphi^2(q)/\varphi^2(q^n)$；对数导数由级数逐项求导直接计算；慢收敛级数一律不用 `nsum`）。最大差为 Entry 11 在 $q = 0.5$ 处的 $4.1\times 10^{-26}$（$\alpha\approx 1$ 的相对精度极限；$q = 0.2$ 时差 $4.7\times 10^{-29}$）；其余最大差为 Entry 9(i)(ii) 在 $q = 0.5$ 处的 $1.1\times 10^{-26}$、$1.6\times 10^{-26}$。另有 6 项反面验证（Entry 7(ii) 按 $\varphi^2$ 分母计差 $2.97$、$0.83$；Entry 8(i) 的 $f(q)$ 按 $(q;q)_{\infty}$ 计差 $13.8$、$3.07$，按 $(-q;q)_{\infty}$ 计差 $42.2$、$0.98$；Entry 11 分母按 $1/2$ 次计差约 $6.7\times 10^6$、$1.1\times 10^{11}$），反证了正文采用的读法。本轮未发现新的原书印文问题；三处 150 DPI 易误读均经 300 DPI 放大图纠正（见待核对清单）。

## 待核对清单

- Berndt 章首计数：本章导言（p. 454）未给出本章公式或定理陈述的总数。
- Entry 2(v) 的原话含义：Berndt 称其含义相当含糊（rather opaque）；(2.3) 与 (2.5) 两种可能解释均已证明，但拉马努金原意未确证；(2.3) 未由拉马努金明言，为 Berndt 的猜测。
- Entry 9(i) 的 $\beta$ 次数：书中 (i) 未明言 $\beta$ 的次数，由 $\varphi^2(q^{23})$ 与 $q^{46k}$ 推断为 23 次；待查 Berndt 其他表述或勘误。
- Entry 11 的编号：笔记（p. 256）中列为 11(i)，但该节无进一步结果；本章编号 Entry 11 只有一条，无 (ii)。
- 第 11 节正文“those six entries”与节标题七条之数的文字细节：(11.2)–(11.7) 翻译六条（Entry 8(iii)、9(i)–(iii)、10(iii)、11），Entry 8(i) 另由 Ch. 20 的 (0.13) 直接改写为 (11.8)，合计七条；此处仅记录文字细节，证明结构无误。
- Entry 1(i) 的“complete”定义：拉马努金在 Ch. 15 第 10 节的定义相当含糊（Berndt 原话 rather vaguely）；(i) 须补加 $y^2/\pi^2$ 为有理数的条件（拉马努金论文 [2]）。
- 转录注意三处（皆为本轮 150 DPI 误读、300 DPI 纠正，非原书印文问题）：Entry 11 分母指数为 $1/12$（300 DPI，PDF 页 498；按 $1/2$ 计差约 $6.7\times 10^6$）；(11.3) 首项系数为 $11/2$ 且中项为 $f(-q^2)$（300 DPI，PDF 页 499；按 $1/2$ 与 $f(-q)$ 计差 $19.0$）；Entry 7(ii) 分母为 $\varphi^3(q)\varphi^3(q^9)$（数值反面验证：按 $\varphi^2$ 计差 $2.97$）。
- Entry 8(i) 的 $f(q)$ 读法：按单变量 $f(q) = \prod_{n\ge 1}(1-(-q)^n)$（即 $f(q,-q^2)$）计差 $0$；按 $(q;q)_{\infty}$ 计差 $13.8$、按 $(-q;q)_{\infty}$ 计差 $42.2$；此处仅记录转录细节。
- (11.8)–(11.14) 的模形式版本未另作数值复核：其与 (11.2)–(11.7) 的等价性见书中推导，theta 形式已逐条复核通过。
- Almkvist–Berndt [1] 的完整题名与页码未逐字核对（参考文献页 OCR 截断）。
- TIFR 1957 年影印版的笔记页码：Entry 1 与 Entry 2(v) 见笔记 p. 253，Entry 11 与 Final Entry 见笔记 p. 256；其余各条的 TIFR 页码未逐条核对。
- 本章条目总数未见于其他目录核对；以书中编号 Entry 1–11 为准。

## 来源说明

- 整理层：Bruce C. Berndt，《Ramanujan's Notebooks》，Part III，Springer，1991，Ch. 21，书页 454–488（正文）；参考文献自书页 489 起，索引自书页 505 起。
- 电子版：archive.org 标识符 `ramanujan_notebooks_iii`（《Ramanujan's Notebooks, Part 3》，Springer 1991，XIII + 510 页，DOI **10.1007/978-1-4612-0965-2**；PDF 21,002,730 字节、524 叶，md5 `de9211b0bde03dd9255145d3f09bb78f`），**PDF 页 = 书页 + 14**（与 Part II 的 +12 不同）。本章为 PDF 页 468–502（书页 454–488）；PDF 页 503 起为参考文献（书页 489）。
- 转录方法：全部公式按 PDF 原图（150 DPI，书页 454–488）逐字转录；关键公式另用 300 DPI 放大图确认：Entry 11 的分母指数 $1/12$（PDF 页 498）、(11.3) 的系数 $11/2$ 与 $f(-q^2)$（PDF 页 499）、(11.5)(11.6)（PDF 页 499）；OCR（DjVu 文本层）只作检索索引，公式凡与原图或数值不符者一律纠正。
- 数值复核：mpmath 30 位，直接求和 + 解析尾项（$q$-Pochhammer 乘积截断到 1500 项、theta 双边和截断到 $\pm 150$ 项、Lambert 级数求和到 $k = 250$ 项（7 周期级数到 $n = 499$）；模方程与 $\alpha$、$\beta$ 公式用 $\alpha(q) = (\theta_2/\theta_3)^4$ 的 theta 路线，$\theta_2 = 2q^{1/4}\psi(q^2)$、$\theta_3 = \varphi(q)$，$m = \varphi^2(q)/\varphi^2(q^n)$；$q = 0.5$ 时 $\alpha\approx 1$（$1-\alpha\approx 10^{-5}$），相对精度极限约 $10^{-25}$，故模方程条目另取 $q = 0.2$ 复核）；104 项真实检查全部通过，差 $< 1\times 10^{-25}$，另有 6 项反面验证（见小结）；慢收敛级数一律不用 `nsum`。复核脚本见 `~/workspace/.berndt-ch21-work/verify21.py`、`verify21b.py`、`verify21c.py`。
- 章名与目录：以原书目录为准，Ch. 21 为 "Eisenstein Series"（书页 454）；上一章 Ch. 20 为 "Modular Equations of Higher and Composite Degrees"（书页 325–453）；本章为 Part III 最后一章，其后为参考文献（书页 489）与索引（书页 505）。
- 参考文献（书中引用，本章出现者）：Almkvist and Berndt [1]、Borwein, J. M. and P. B. [2]（《Pi and the AGM》，Wiley，1987）、Ghosh, S. [1]（博士论文《On the Evaluation of $k^2$ and $E$ in the Theory of Elliptic Functions》，University of Bombay，1985）、Ramanujan [2]（《Modular equations and approximations to $\pi$》，Q. J. Math. 45 (1914)，350–372）、Ramanujan [6]（《On certain arithmetical functions》，Trans. Cambridge Philos. Soc. 22 (1916)，159–184）、Ramanujan [9]（Notebooks，TIFR，1957）、Ramanujan [10]（Collected Papers，Chelsea，1962）、Rankin [2]（《Modular Forms and Functions》，Cambridge University Press，1977）、Schoeneberg [1]（《Elliptic Modular Functions》，Springer，1974）、Whittaker and Watson [1]（《A Course of Modern Analysis》，4th ed.，1966）；另有 Ch. 15–20 的章内互引（Ch. 16 Entry 22–27、Ch. 17 Entry 10–13、Ch. 18 Entry 2、Ch. 19 Entry 3、5、11、13、14、17、Ch. 20 Entry 1、7 与第 0 节）。
