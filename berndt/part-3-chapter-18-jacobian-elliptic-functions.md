# Part III，Chapter 18——The Jacobian Elliptic Functions（Jacobi 椭圆函数）

出处：Bruce C. Berndt，《Ramanujan's Notebooks》，Part III，Springer，1991，Ch. 18，书页 143–219。

本章是 Part III 的第三章、Berndt 五卷的第 18 章：拉马努金在此展开 Jacobian 椭圆函数的理论——椭圆周长的超几何表示与近似、$\sinh$、$\cosh$ 级数的求值、$\mathrm{sn}$、$\mathrm{cn}$、$\mathrm{dn}$ 的连分数、椭圆积分的反演、化圆为方与立方和参数解、$\omega = e^{2\pi i/3}$ 的部分分式，以及 2 次、4 次模方程（附 8 次、16 次的未成立断言）。Berndt 在章首导言（p. 143）中说，本章“最有趣”的恒等式是 Entry 11(i) 的 $\mathrm{dn}$ 恒等式（化为 $2\Gamma^4(3/4)/\pi$）；又说 Entry 8 的四个 $\theta$ 级数求值“ apparently not previously in the literature”。本章共 **24 条编号 Entry（Entry 1–24，无缺号）**，另含定理、推论与例题 59 个分体标题（见“本章结构”表后的计数说明）。

## 背景与记号

- 记号（沿用 Ch. 17 第 6 节，(6.2)–(6.4)）：$z = {}_2F_1(\frac12,\frac12;1;x)$，$y = \pi\,{}_2F_1(\frac12,\frac12;1;1-x)/{}_2F_1(\frac12,\frac12;1;x)$，$q = e^{-y}$；则 $\varphi(e^{-y}) = \sqrt{z}$，$K = \frac12\pi z$。余模记号：$x' = 1-x$，$y' = \pi z/z'$，$z' = {}_2F_1(\frac12,\frac12;1;1-x)$，其中 $z'$ 为余模的 $z$。下文大量使用 $x$、$y$、$z$ 这一组记号；$x$ 与 $1-x$ 的对称性（模与余模互换）贯穿全章。
- Eisenstein 级数 $L$（Ch. 17 (9.2)）：$L(e^{-2y}) = 1 - 24\sum_{n=1}^{\infty}n/(e^{2ny}-1)$；Entry 1、Entry 2、Entry 17 均用 $L(e^{-2y})$。$E = \int_0^{\pi/2}\sqrt{1-x\sin^2\varphi}\,d\varphi$ 为第二类完全椭圆积分（Entry 17）；(17.4)：$L(e^{-2y}) = 6zE/\pi - 2z^2 + xz^2$。
- 第 14 节的三个级数（(14.1)）：$S(\theta) = \sum_{j=0}^{\infty}\sin(2j+1)\theta/\sinh\{\frac12(2j+1)y\}$，$C(\theta) = \sum_{j=0}^{\infty}\cos(2j+1)\theta/\cosh\{\frac12(2j+1)y\}$，$C_1(\theta) = \frac12 + \sum_{j=1}^{\infty}\cos(2j\theta)/\cosh(jy)$；则 $S = \frac12z\sqrt{x}\,\mathrm{sn}(z\theta)$，$C = \frac12z\sqrt{x}\,\mathrm{cn}(z\theta)$，$C_1 = \frac12z\,\mathrm{dn}(z\theta)$。$\varphi$ 由 (14.8) 定义：$C = \frac12z\sqrt{x}\cos\varphi$，$S = \frac12z\sqrt{x}\sin\varphi$（$0\le\varphi<2\pi$）；(14.11)：$\theta = (1/z)\int_0^{\varphi}d\varphi/\sqrt{1-x\sin^2\varphi}$，即第一类椭圆积分的反演（拉马努金的形式）。
- 第 18 节的一般方程 (18.1)：$\Omega(x,e^{-y},z,\theta,\varphi) = 0$，即由 (14.8) 与 (14.11) 联立所得的 $\theta$、$\varphi$ 间关系；Entry 18 的 (i)–(iv) 为该方程在四种参数变换（dimidiation、change of sign、虚变换）下的形式。三种变换的定义见 Ch. 17 第 13 节：duplication（倍乘）、dimidiation（折半）、change of sign（变号，Jacobi 的方法）。
- $\omega = \exp(2\pi i/3)$（Entry 8–10）：$1$ 的三次单位根，$1+\omega+\omega^2 = 0$；Entry 8–10 的部分分式以 $\omega$ 的六次单位根为极点。
- Catalan 常数（Entry 7）：$C = \sum_{n=0}^{\infty}(-1)^n/(2n+1)^2$。
- $\varphi(q) = \sum_{n=-\infty}^{\infty}q^{n^2}$（Ch. 16 Entry 22）；Entry 23 的反演公式与 Ch. 14 Entry 7 的推论、Ch. 16 Entry 27(i)、Ch. 17 第 6 节推论的 $\sqrt{\alpha}\{1/2+\sum e^{-\alpha n^2}\} = \sqrt{\beta}\{1/2+\sum e^{-\beta n^2}\}$（$\alpha\beta = \pi$）为同一公式。
- 模方程的定义（Entry 24，(24.13)）：设 $K$、$K'$、$L$、$L'$ 为模 $k$、$k'$、$\ell$、$\ell'$ 的第一类完全椭圆积分；若 $L'/L = nK'/K$，则 $k$ 与 $\ell$ 间由此诱导的关系称为 $n$ 次模方程。置 $\alpha = k^2$、$\beta = \ell^2$，则 (24.13)：$n\,{}_2F_1(\frac12,\frac12;1;1-\alpha)/{}_2F_1(\frac12,\frac12;1;\alpha) = {}_2F_1(\frac12,\frac12;1;1-\beta)/{}_2F_1(\frac12,\frac12;1;\beta)$。乘子 $m$ 由 (24.14) 定义：$m = {}_2F_1(\frac12,\frac12;1;\alpha)/{}_2F_1(\frac12,\frac12;1;\beta)$。
- 本章与已填章节的互见：Ch. 17 的椭圆函数基本性质是本章的前提——Entry 7 的加法定理、Entry 16–17 的 $\mathrm{dn}$ 级数、Entry 18 的 Cauchy 级数（Ch. 17 文件已注明 Ch. 18 第 10 节会回到这些和式，即本章 Entry 10）；Ch. 16 的 theta 函数（Entry 27 的变换、Entry 33(iii) 的 $\mathrm{dn}$ Fourier 级数）是 Entry 11、Entry 14、Entry 23 的工具；Part I Ch. 11 的 M11 椭圆函数（Entry 25 的推论、Entry 30、Entry 32–35）是 Entry 1、Entry 2、Entry 6、Entry 17 的证明工具；Ch. 15 的 $L$、$M$、$N$ 是 Entry 17 的工具；Ch. 14 Entry 7 的 theta 反演公式即 Entry 23 的 (23.1)。
- 与主题模块的对照总览：椭圆函数主线见 **M11**（全章；Entry 1–2 的超几何与椭圆积分、Entry 6–7 的 $\cosh$ 级数与 Catalan 常数、Entry 11 的 $\mathrm{dn}$ 恒等式、Entry 14–18 的 $\mathrm{sn}$、$\mathrm{cn}$、$\mathrm{dn}$ Fourier 级数与参数变换、Entry 19 的椭圆弧与双曲弧、Entry 24 的模方程）；无穷级数见 **M02**（Entry 4–10 的 $\sinh$、$\cosh$、$e^{ky}\pm 1$ 级数与 $\omega$ 部分分式、Entry 15–17 的 $\theta$、$\varphi$ 级数、Entry 21 的部分分式、Entry 23 的 theta 反演）；连分数见 **M03**（Entry 12–13 的 $\mathrm{dn}$、$\mathrm{cn}$、$\mathrm{cd}$、$\mathrm{sd}$、$\mathrm{sn}$ 连分数、Entry 22 的积分连分数、第 3 节 (3.5)(3.6) 的椭圆周长连分数）；$\pi$ 与特殊常数见 **M04**（第 3 节例题与推论的 $\pi$ 近似、Entry 11(i) 的 $\Gamma(3/4)$、Entry 20 的化圆为方、第 13 节推论的 $\mu = \sqrt{\pi}/\Gamma^2(3/4)$）；模形式与模方程见 **M06**（Entry 12 的推论、Entry 17 的 $L(e^{-2y})$、Entry 23 的 theta 反演、Entry 24 的 2 次、4 次模方程）；q 级数与 theta 函数见 **M07**（Entry 11、Entry 23、第 24 节 (vii) 的 $\vartheta$、$\varphi$ 函数）；积分见 **M09**（Entry 1–2 的 $\int_0^x z\,dx$、Entry 14 的 (14.11)、Entry 19 的椭圆弧与双曲弧积分、Entry 22 的 Laplace 型积分）；Gamma 函数见 **M10**（Entry 11(i) 的 $\Gamma(3/4)$、第 13 节推论的 $\mu$）；数论见 **M01**（Entry 8–10 的 $\omega$ 部分分式、Entry 20(ii)(iii) 的立方和丢番图方程）；代数方程见 **M14**（Entry 20(ii)(iii) 的参数解）。

## 本章结构

| Entry | 主题 | 书页 |
|---|---|---|
| Entry 1 | ${}_2F_1(-\frac12,-\frac12;1;x)$ 用 $z$ 与 $L(e^{-2y})$ 表出 | 144–145 |
| Entry 2 | ${}_2F_1(-\frac12,\frac12;1;x)$ 用 $z$ 与 $L(e^{-2y})$ 表出 | 145 |
| Entry 3 | 椭圆周长：精确式 (3.1)(3.2) 与拉马努金近似 (3.3) nearly、(3.4) very nearly；定理 1、定理 2；例题（$\pi$ 等小数）；推论（$\pi$ 近似） | 145–152 |
| Entry 4 | $(\sqrt{x}/2)\cdot$ 级数 $=$ 对数比级数 | 152 |
| Entry 5 | $\mathrm{Log}(16/x) -$ 级数 $= y - 4\cdot$ 对数级数 | 152–153 |
| Entry 6 | $\cosh$ 级数 $= (\sqrt{x}/2z)\cdot{}_3F_2(1,1,1;3/2,3/2;x)$ | 153–154 |
| Entry 7 | Catalan 常数 $C$；$e^{(2n+1)y}+1$ 级数与 ${}_3F_2(\cdots;1-x)$；第 7 节例题（$\sinh$ 级数 $= \frac14\mathrm{Log}((1+\sqrt{x})/(1-\sqrt{x}))$） | 155–157 |
| Entry 8 | 四个 $\theta$ 级数求值 (i)–(iv)，$\omega = \exp(2\pi i/3)$ 部分分式 | 157–159 |
| Entry 9 | 部分分式级数 $= \pi/(12\cos(\frac12\pi z)(\cos(\frac12\pi z)+\cosh(\frac12\pi\sqrt{3}z)))$；第 9 节例题 (i)(ii) 乘积公式 | 159–160 |
| Entry 10 | 同型级数（分母 $\cosh\{\frac12(2n+1)\pi/\sqrt{3}\}$）；第 10 节例 1（$\tan$ 乘积 (10.2)）、例 2（$\pi^7/23040$） | 160–162 |
| Entry 11 | (i) $\mathrm{dn}$ 恒等式 $= 2\Gamma^4(3/4)/\pi$；(ii) 余模乘积 $= \frac14zz'\sqrt{xx'}$ | 162–163 |
| Entry 12 | (i)(ii) $\mathrm{dn}$、$\mathrm{cn}$ 连分数（Stieltjes–Rogers）；推论 $F((\alpha+\beta)/2,\sqrt{\alpha\beta}) = \frac12\{F(\alpha,\beta)+F(\beta,\alpha)\}$ | 163–165 |
| Entry 13 | (i)(ii)(iii) $\mathrm{cd}$、$\mathrm{sd}$、$\mathrm{sn}$ 连分数；第 13 节推论（$\mu = \sqrt{\pi}/\Gamma^2(3/4)$ 的连分数） | 165–168 |
| Entry 14 | $S$、$C$、$C_1$（$\mathrm{sn}$、$\mathrm{cn}$、$\mathrm{dn}$ 的 Fourier 级数）：(14.2)–(14.11) | 168–172 |
| Entry 15 | $\theta$、$\varphi$ 的六条级数 (i)–(vi) | 172–173 |
| Entry 16 | 第一部分（$\theta\to\frac12\pi-\theta$ 换表）与第二部分 (i)–(v) | 173–175 |
| Entry 17 | (i)–(iv)，$L(e^{-2y})$ 与第二类椭圆积分 $E$ | 175–177 |
| Entry 18 | (i)–(iv) 参数变换（dimidiation、change of sign、虚变换） | 177–180 |
| Entry 19 | (i) 椭圆弧、(ii) 双曲弧、(iii)(iv) 周长角 $\varphi$；推论 (i)(ii) | 180–193 |
| Entry 20 | (i) 化圆为方（$355/113$）；推论 (i)(ii)；(ii) $A^3+B^3 = C^2$ 参数解；(iii) $A^3+B^3+C^3 = D^3$ 参数解与例题（含 1729） | 193–200 |
| Entry 21 | (i)–(iv) 部分分式；例题（拉马努金两处数值错误）；(21.9) 的 $\psi$ 和注记 | 200–206 |
| Entry 22 | (i)(ii)(iii) $\mathrm{dn}$、$\mathrm{cn}$、$\mathrm{coam}$ 连分数 | 206–208 |
| Entry 23 | (i)(ii) theta 反演公式；推论；例题 (23.4)(23.5) | 208–210 |
| Entry 24 | (i) 几何作图，命题 1–3；(ii) 2 次模方程；(iii) 4 次模方程；(iv) 8 次、16 次断言（不成立）；(v) 倒易；(vi) $d\alpha/d\beta$；第 24 节 (vii) $\vartheta$、$\varphi$ 函数陈述 | 211–219 |

计数说明：编号 Entry 1–24 共 24 条，无缺号。分体、推论与例子标题 59 个：Entry 3 的定理 1、定理 2、例题、推论 4，Entry 7 的第 7 节例题 1，Entry 8(i)–(iv) 3（除 Entry 本身计 1），Entry 9 的第 9 节例题 (i)(ii) 2，Entry 10 的第 10 节例 1、例 2 共 2，Entry 11(ii) 1，Entry 12(ii) 与推论 2，Entry 13(ii)(iii) 与第 13 节推论 3，Entry 15(ii)–(vi) 5，Entry 16 的第二部分 (i)–(v) 5（第一部分换表计入 Entry 本身），Entry 17(ii)–(iv) 3，Entry 18(ii)–(iv) 3，Entry 19(ii)–(iv) 与推论 (i)(ii) 5，Entry 20(ii)(iii) 与推论 (i)(ii) 4，Entry 21(ii)–(iv) 与例题 4，Entry 22(ii)(iii) 2，Entry 23(ii) 与推论、例题 (23.4)(23.5) 4，Entry 24(ii)–(vi) 与第 24 节 (vii) 6。按“无分体的 Entry 计 1、有分体的 Entry 计其分体数”的口径，Entry 标题共 83 个。另有第 14 节 (14.2)–(14.11)、第 19 节 (19.19)–(19.23)、(19.34)、(19.36)(19.37)、第 21 节 (21.8)–(21.10)、第 24 节 (24.1)–(24.31) 等编号公式，均已按其所属 Entry 收录。

## Entry 1

**陈述。** 对 $0 < x < 1$，

$${}_2F_1(-\tfrac12,-\tfrac12;1;x) = z(1-x) + \int_0^x z\,dx = \frac{z}{3}(1+x) + \frac{2}{3z}L(e^{-2y}),$$

其中 $z = {}_2F_1(\frac12,\frac12;1;x)$，$L(e^{-2y}) = 1 - 24\sum_{n=1}^{\infty}n/(e^{2ny}-1)$（Ch. 17 (9.2)）。

**说明。** 证明用 Ch. 11 Entry 35(iii) 的超几何积分与 Ch. 17 Entry 9(iv) 的 $L(e^{-2y})$ 公式；第一等式为积分表示，第二等式把积分化为 $z$ 与 $L$ 的闭式。本条与 Entry 3 的椭圆周长 (3.2) 直接相关（${}_2F_1(-\frac12,-\frac12;1;t)$ 即周长核）。

**状态：** 已证明（书中给出证明）。**对照：** M11（椭圆积分与超几何）、M02（超几何级数）、M09（积分）。

**我自验：** 取 $x = 0.5$（$z = 1.18034059902$、$y = \pi$）：第一式左端 $1.21105646917$、右端 $1.21105646917$，差 $2.0\times 10^{-31}$；第二式差 $0$（mpmath 30 位，直接求和）。

## Entry 2

**陈述。** 对 $0 < x < 1$，

$${}_2F_1(-\tfrac12,\tfrac12;1;x) = z(1-x) + \frac12\int_0^x z\,dx = \frac{z}{3}(2-x) + \frac{1}{3z}L(e^{-2y}).$$

**说明。** 与 Entry 1 同法证明；两条的差别仅在 $\int_0^x z\,dx$ 的系数（$1$ 与 $\frac12$）与 $L$ 项的系数（$2/(3z)$ 与 $1/(3z)$）。Entry 1、Entry 2 合为椭圆周长精确式 (3.1)(3.2) 的超几何准备。

**状态：** 已证明（书中给出证明）。**对照：** M11、M02、M09。

**我自验：** 取 $x = 0.5$：两式差均为 $9.9\times 10^{-32}$（mpmath 30 位）。

## Entry 3

**陈述。** 设椭圆 $x^2/a^2 + y^2/b^2 = 1$（$a > b > 0$），离心率 $e = (1/a)\sqrt{a^2-b^2}$，$t = ((a-b)/(a+b))^2$。记周长为 $L$。则

$$(3.1)\quad L = 2\pi a\,{}_2F_1(\tfrac12,-\tfrac12;1;e^2);$$

$$(3.2)\quad L = \pi(a+b)\,{}_2F_1(-\tfrac12,-\tfrac12;1;t);$$

$$(3.3)\quad L = \pi\{3(a+b)-\sqrt{(a+3b)(3a+b)}\}\quad\text{nearly};$$

$$(3.4)\quad L = \pi(a+b)\left\{1+\frac{3t}{10+\sqrt{4-3t}}\right\}\quad\text{very nearly}.$$

其中 (3.3) 的“nearly”与 (3.4) 的“very nearly”为拉马努金原话（第二本笔记 p. 217）：(3.3) 为近似式，(3.4) 为更精确的近似式。

**说明。**(3.1) 为 Maclaurin 1742 年的结果；(3.2) 为 Ivory 1796 年经 Landen 变换所得；(3.3) 为拉马努金所发现，Fergestad 1951 年重新发现；(3.4) 的解释见 Jacobsen–Waadeland：由 (3.5) ${}_2F_1(-\frac12,-\frac12;1;t) = 1 + t/(4(1+w))$ 与连分数 (3.6)，$w \approx (1/12)(-2+\sqrt{4-3t})$，(3.4) 即取 $w$ 的近似。系数的比较：(3.8) ${}_2F_1(-\frac12,-\frac12;1;t) = 1 + t/4 + t^2/4^3 + t^3/4^4 + 25t^4/4^7 + 49t^5/4^8 + \cdots = \sum\alpha_nt^n$；(3.9) $3(a+b)-\sqrt{(a+3b)(3a+b)} = (a+b)(3-\sqrt{4-t}) = (a+b)\sum\beta_nt^n$，$\alpha_n = \beta_n$（$n\le 2$），$\alpha_3 = 2\beta_3$，$\alpha_4 = 5\beta_4$，故 (3.3) 的误差约为 $t^3/2^9$；(3.10) $1+3t/(10+\sqrt{4-3t}) = \sum\gamma_nt^n$，$\alpha_n = \gamma_n$（$n\le 4$），$\gamma_5 = 95/98\cdot\alpha_5$，故 (3.4) 的误差约为 $3t^5/2^{17}$。

**定理 1。** $\beta_n \le \alpha_n/2^{n-2}$（$n\ge 3$）。

**定理 2。** $\gamma_n < \alpha_n$（$n\ge 5$）。

Villarino 对 (3.4) 的界（$a\ne b$）：$-(0.000512272\cdots)t^5 = -(4/\pi-14/11)t^5 < A(t)-L/(\pi(a+b)) < -3t^5/2^{17} = -(0.000022888\cdots)t^5$，其中 $A(t) = 1+3t/(10+\sqrt{4-3t})$。

**第 3 节例题。** $\pi = 3.14159\,26535\,89793\,23846\,26434$；$\mathrm{Log}\,10 = 2.30258\,50929\,94045\,68401\,8$；$e^{-\pi} = 0.04321\,39182\,63772\,25$；$e^{\pi/2} = 4.81047\,73809\,65351\,65547\,3$。

**第 3 节推论。** $\pi = (355/113)(1-0.0003/3533)$，very nearly（$= 3.14159\,26535\,89794\,32$，比 $\pi$ 大约 $10^{-15}$）；$\pi = (97\frac12-1/11)^{1/4}$，nearly（$= 3.14159\,26526\,2$，比 $\pi$ 小约 $10^{-9}$）。$\pi^4$ 的连分数为 $97+1/(2+1/(2+1/(3+1/(1+1/(16,539+1/(1+\cdots))))))$；截断到第四个部分商得 $\pi^4 \approx 97\frac{9}{22}$。

**状态：** 已证明（书中给出证明；(3.3)(3.4) 为近似式，非等式）。**对照：** M11（椭圆周长）、M02（超几何级数）、M03（连分数 (3.5)(3.6)）、M04（$\pi$ 近似）。

**我自验：** 取 $a = 2$、$b = 1$（$t = 1/9$）：(3.1) 与 (3.2) 的左端与右端差分别为 $7.9\times 10^{-31}$、$0$；(3.3) 的相对误差 $2.2792\times 10^{-11}$，与 $t^3/2^9 = 2.2773\times 10^{-11}$ 一致；(3.4) 的相对误差 $1.3766\times 10^{-18}$，与 $3t^5/2^{17} = 1.3722\times 10^{-18}$ 一致。例题四小数与推论两 $\pi$ 近似值逐项核对无误：$(355/113)(1-0.0003/3533) - \pi = 1.09\times 10^{-15}$，$(97\frac12-1/11)^{1/4} - \pi = -1.01\times 10^{-9}$，$\pi^4$ 截断值 $97\frac{9}{22} = 97.4090909091$，$\pi^4 = 97.409091034$（mpmath 30 位）。

## Entry 4

**陈述。** 对 $0 < x < 1$，

$$\frac{\sqrt{x}}{2}\sum_{n=0}^{\infty}\frac{(\frac12)_n^2}{(n!)^2}\frac{x^n}{2n+1} = \sum_{n=0}^{\infty}(-1)^n(2n+1)\,\mathrm{Log}\frac{1+e^{-(2n+1)y/2}}{1-e^{-(2n+1)y/2}}.$$

**说明。** 左端为超几何级数的逐项积分形式（$(\frac12)_n$ 为 Pochhammer 符号）；右端为对数比级数。证明用 Ch. 11 的超几何结果与 $y$ 的定义。

**状态：** 已证明（书中给出证明）。**对照：** M02（无穷级数）、M11（椭圆函数参数）。

**我自验：** 取 $x = 0.5$：左端与右端差 $7.4\times 10^{-30}$（mpmath 30 位，直接求和）。

## Entry 5

**陈述。** 对 $0 < x < 1$，

$$\mathrm{Log}\frac{16}{x} - \sum_{n=1}^{\infty}\frac{(\frac12)_n^2}{(n!)^2}\frac{x^n}{n} = y - 4\sum_{n=0}^{\infty}(-1)^n(2n+1)\,\mathrm{Log}(1-e^{-(2n+1)y}).$$

**说明。** 左端为 $\mathrm{Log}(16/x)$ 减一超几何级数；右端为 $y$ 减一对数级数。与 Entry 4 同源，证明用 $z$ 的对数导数。

**状态：** 已证明（书中给出证明）。**对照：** M02、M11。

**我自验：** 取 $x = 0.5$：差 $1.2\times 10^{-30}$（mpmath 30 位）。

## Entry 6

**陈述。** 对 $0 < x < 1$，

$$\sum_{n=0}^{\infty}\frac{1}{(2n+1)^2\cosh\{\frac12(2n+1)y\}} = \frac{\sqrt{x}}{2z}\,{}_3F_2(1,1,1;3/2,3/2;x).$$

**说明。** 左端为 $\cosh$ 倒数级数；右端为广义超几何函数 ${}_3F_2$。证明用 Entry 4 的级数逐项积分（对 $y$ 积分两次）。

**状态：** 已证明（书中给出证明）。**对照：** M02、M11。

**我自验：** 取 $x = 0.5$：差 $4.9\times 10^{-32}$（mpmath 30 位）。

## Entry 7

**陈述。** 设 Catalan 常数 $C = \sum_{n=0}^{\infty}(-1)^n/(2n+1)^2$。则对 $0 < x < 1$，

$$\sum_{n=0}^{\infty}\frac{(-1)^n}{(2n+1)^2(e^{(2n+1)y}+1)} = \frac12C - \frac{\pi y}{16} + \frac{\sqrt{1-x}}{4z}\,{}_3F_2(1,1,1;3/2,3/2;1-x).$$

**第 7 节例题。**

$$\sum_{n=0}^{\infty}\frac{1}{(2n+1)\sinh\{\frac12(2n+1)y\}} = \frac14\,\mathrm{Log}\frac{1+\sqrt{x}}{1-\sqrt{x}}.$$

**说明。** 本条把 $e^{(2n+1)y}+1$ 级数化为 Catalan 常数、$\pi y$ 与余模 $1-x$ 的 ${}_3F_2$；例题为 $\sinh$ 级数的闭式。证明用 Entry 6 的余模形式与部分分式。

**状态：** 已证明（书中给出证明）。**对照：** M02、M11、M04（Catalan 常数）。

**我自验：** 取 $x = 0.5$：Entry 7 差 $4.3\times 10^{-32}$；第 7 节例题差 $9.9\times 10^{-32}$（mpmath 30 位）。

## Entry 8

**陈述。** 设 $\theta$ 为实数，$\omega = \exp(2\pi i/3)$。则

**(i)** $|{\theta}| < \pi$ 时，

$$\sum_{n=0}^{\infty}(-1)^n\frac{\cos(2n+1)\theta + 2\cos\{\frac12(2n+1)\theta\}\cosh\{\frac12(2n+1)\sqrt{3}\,\theta\}}{(2n+1)\cosh\{\frac12(2n+1)\pi\sqrt{3}\}} = \frac{\pi}{8};$$

**(ii)** $|\theta| < \pi/2$ 时，

$$\sum_{n=0}^{\infty}(-1)^n\frac{\cos(2n+1)\theta\,(\cos(2n+1)\theta + \cosh\{(2n+1)\sqrt{3}\,\theta\})}{(2n+1)\cosh\{\frac12(2n+1)\pi\sqrt{3}\}} = \frac{\pi}{12};$$

**(iii)**

$$\sum_{n=0}^{\infty}(-1)^n\frac{\sin(2n+1)\theta\,(\cos(2n+1)\theta - \cosh\{(2n+1)\sqrt{3}\,\theta\})}{(2n+1)^4\cosh\{\frac12(2n+1)\pi\sqrt{3}\}} = -\frac{\pi\theta^3}{12};$$

**(iv)**

$$\sum_{n=0}^{\infty}(-1)^n\frac{\cos(2n+1)\theta\,(\cos(2n+1)\theta + \cosh\{(2n+1)\sqrt{3}\,\theta\})}{(2n+1)^7\cosh\{\frac12(2n+1)\pi\sqrt{3}\}} = \frac{\pi^7}{11520} - \frac{\pi\theta^6}{180}.$$

**说明。** 四式为 $\omega$ 的部分分式（$\cosh\{\frac12(2n+1)\pi\sqrt{3}\}$ 为 $\omega$ 的极点留数分母）；Berndt 注明这些求值“apparently not previously in the literature”。证明用 Ch. 17 Entry 18 的 Cauchy 级数方法（以 $\omega$ 为极点作部分分式）。

**状态：** 已证明（书中给出证明）。**对照：** M02（无穷级数）、M01（$\omega$ 部分分式）、M04（$\pi^7$ 常数）。

**我自验：** 取 $\theta = 0.7$：(i) 差 $4.9\times 10^{-32}$，(ii) 差 $9.9\times 10^{-32}$，(iii) 差 $0$，(iv) 差 $1.5\times 10^{-31}$（mpmath 30 位，直接求和）。

## Entry 9

**陈述。** 设 $z\ne\pm\omega^j(2n+1)$（$0\le j\le 2$，$n\ge 0$，$\omega = \exp(2\pi i/3)$）。则

$$\sum_{n=0}^{\infty}(-1)^n\frac{(2n+1)^5}{\cosh\{\frac12(2n+1)\pi\sqrt{3}\}\,((2n+1)^6-z^6)} = \frac{\pi}{12}\cdot\frac{1}{\cos(\frac12\pi z)(\cos(\frac12\pi z)+\cosh(\frac12\pi\sqrt{3}\,z))}.$$

**第 9 节例题。**

**(i)** $\frac12\cos(\frac12z)(\cos(\frac12z)+\cosh(\frac12\sqrt{3}\,z)) = 1 + \frac34\sum_{n=1}^{\infty}(-1)^n z^{6n}/(6n)! = \prod_{n=0}^{\infty}(1-z^6/((2n+1)^6\pi^6))$；

**(ii)** $\frac12\sin(\frac12z)(\cos(\frac12z)-\cosh(\frac12\sqrt{3}\,z)) = -\frac34\sum_{n=0}^{\infty}(-1)^n z^{6n+3}/(6n+3)! = -(z^3/8)\prod_{n=1}^{\infty}(1-z^6/(2n\pi)^6)$。

**说明。** 左端为 $(2n+1)^6-z^6$ 的部分分式；右端为 $\cos$ 与 $\cosh$ 的乘积之倒数。例题 (i)(ii) 为相应的无穷乘积公式（由 (i) 的幂级数与零点分布得）。

**状态：** 已证明（书中给出证明）。**对照：** M02、M01（$\omega$ 部分分式）。

**我自验：** 取 $z = 0.5$：Entry 9 差 $4.9\times 10^{-32}$；例题 (i) 级数差 $0$、乘积差 $5.1\times 10^{-23}$（乘积取 1000 项，截断尾项），例题 (ii) 级数差 $4.6\times 10^{-33}$、乘积差 $8.0\times 10^{-25}$（乘积取 1000 项，截断尾项）（mpmath 30 位）。

## Entry 10

**陈述。** 设 $z\ne\pm\omega^j(2n+1)$（$0\le j\le 2$，$n\ge 0$）。则

$$\sum_{n=0}^{\infty}(-1)^n\frac{(2n+1)^5}{\cosh\{\frac12(2n+1)\pi/\sqrt{3}\}\,((2n+1)^6-z^6)} = \frac{\pi}{12}\cdot\frac{4\cosh(\pi z/(2\sqrt{3}))(\cos(\frac12\pi z)+\cosh(\pi z/(2\sqrt{3})))-3}{\cos(\frac12\pi z)(\cos(\frac12\pi z)+\cosh(\frac12\pi\sqrt{3}\,z))}.$$

**第 10 节例 1。**

$$z^3\sum_{n=0}^{\infty}\frac{(2n+1)^2}{(2n+1)^6-z^6} = \frac{\pi}{12}\cdot\frac{\cosh(\frac12\pi\sqrt{3}\,z)-\cos(\frac12\pi z)}{\cosh(\frac12\pi\sqrt{3}\,z)+\cos(\frac12\pi z)}\tan(\frac12\pi z);$$

其对称形式 (10.2)：

$$\frac{\pi\tan(\frac12\pi z)\tan(\frac12\pi\omega z)\tan(\frac12\pi\omega^2 z)}{12z^3} = \sum_{n=0}^{\infty}\frac{(2n+1)^2}{(2n+1)^6-z^6}.$$

**第 10 节例 2。**

$$\sum_{n=0}^{\infty}\frac{(-1)^n}{(2n+1)^7\cosh\{\frac12(2n+1)\pi\sqrt{3}\}} = \frac{\pi^7}{23040}.$$

**说明。** 本条为 Entry 9 的同型级数（分母 $\cosh\{\frac12(2n+1)\pi/\sqrt{3}\}$）；Ch. 17 文件已注明 Ch. 18 第 10 节会回到 Ch. 17 Entry 18 的 Cauchy 级数，即此处。例 2 载于拉马努金致 Hardy 的第一封信，Watson 首见于印刷品证明。

**状态：** 已证明（书中给出证明）。**对照：** M02、M01、M04（$\pi^7$）。

**我自验：** 取 $z = 0.5$：Entry 10 差 $3.0\times 10^{-31}$；例 1 差 $2.6\times 10^{-15}$、(10.2) 差 $2.1\times 10^{-14}$（级数取 10000 项并补 $\zeta(4)$ 解析尾项，余项量级与之相符）；例 2 差 $4.9\times 10^{-32}$（mpmath 30 位）。

## Entry 11

**陈述。**

**(i)** $|\mathrm{Im}\,\theta| < \pi$ 时，

$$\left\{1+2\sum_{n=1}^{\infty}\frac{\cos(n\theta)}{\cosh(n\pi)}\right\}^{-2} + \left\{1+2\sum_{n=1}^{\infty}\frac{\cosh(n\theta)}{\cosh(n\pi)}\right\}^{-2} = \frac{2\Gamma^4(3/4)}{\pi}.$$

**(ii)** 设 $x'$、$y'$、$z'$ 为余模 $1-x$ 的相应参数，则

$$\sum_{n=0}^{\infty}\frac{\cos(2n+1)\theta}{\cosh\{\frac12(2n+1)y\}}\cdot\sum_{n=0}^{\infty}\frac{\cosh(2n+1)\theta}{\cosh\{\frac12(2n+1)y'\}} = \frac14zz'\sqrt{xx'}.$$

**说明。**(i) 为章首导言点名的本章“最有趣”的恒等式；证明用 $\mathrm{dn}$ 的 Fourier 级数 (11.1)，在 $x = \frac12$ 处 $K = \frac12\pi^{3/2}/\Gamma^2(3/4)$，化为 $\mathrm{dn}^{-2}(K\theta/\pi) + \mathrm{dn}^{-2}(Ki\theta/\pi) = 2$。(ii) 为余模乘积公式；证明用 (i) 的 Fourier 级数与 Ch. 16 Entry 27 的变换。

**状态：** 已证明（书中给出证明）。**对照：** M11（$\mathrm{dn}$ 恒等式）、M10（$\Gamma(3/4)$）、M07（theta 函数）。

**我自验：** 取 $x = 0.5$、$\theta = 0.3$：(i) 差 $3.9\times 10^{-31}$，(ii) 差 $0$（mpmath 30 位）。

## Entry 12

**陈述。** 设 $n > 0$。则

**(i)**

$$\frac12 + \sum_{j=1}^{\infty}\frac{\mathrm{sech}(jy)}{1+(jn)^2} = \frac{z}{2}\cdot\frac{1}{1+\cfrac{(nz)^2x}{1+\cfrac{(2nz)^2}{1+\cfrac{(3nz)^2x}{1+\cfrac{(4nz)^2}{1+\cdots}}}}};$$

**(ii)**

$$2\sum_{j=0}^{\infty}\frac{\mathrm{sech}\{\frac12(2j+1)y\}}{1+(2j+1)^2n^2} = \frac{z\sqrt{x}}{1+\cfrac{(nz)^2}{1+\cfrac{(2nz)^2x}{1+\cfrac{(3nz)^2}{1+\cfrac{(4nz)^2x}{1+\cdots}}}}}.$$

**第 12 节推论。** 设 $F(\alpha,\beta) = \alpha/(n+\beta^2/(n+(2\alpha)^2/(n+(3\beta)^2/(n+(4\alpha)^2/(n+\cdots)))))$，$\mathrm{Re}\,\alpha$、$\mathrm{Re}\,\beta > 0$。则

$$F((\alpha+\beta)/2,\sqrt{\alpha\beta}) = \frac12\{F(\alpha,\beta)+F(\beta,\alpha)\}. \tag{12.3}$$

**说明。**(i)(ii) 为 $\mathrm{dn}$、$\mathrm{cn}$ 的 Laplace 变换连分数（Stieltjes–Rogers 方法）；(ii) 载于拉马努金致 Hardy 的第一封信，Preece 首见于印刷品证明。推论 (12.3) 载于拉马努金致 Hardy 的第二封信，Preece 证明；为算术–几何平均型恒等式。

**状态：** 已证明（书中给出证明）。**对照：** M03（连分数）、M11、M06（模形式）。

**我自验：** 取 $x = 0.5$、$n = 1$：(i) 差 $4.9\times 10^{-31}$，(ii) 差 $4.9\times 10^{-32}$（连分数取 300 项后向递推）；推论取 $\alpha = 1.2$、$\beta = 0.8$：差 $0$（连分数取 1000 项）（mpmath 30 位）。

## Entry 13

**陈述。** 设 $n > 0$。则

**(i)**

$$2\sum_{j=0}^{\infty}(-1)^j\frac{\mathrm{csch}\{\frac12(2j+1)y\}}{1+(2j+1)^2n^2} = \frac{z\sqrt{x}}{1+\cfrac{(1-x)(nz)^2}{1-\cfrac{x(2nz)^2}{1+\cfrac{(1-x)(3nz)^2}{1-\cdots}}}};$$

**(ii)**

$$2\sum_{j=0}^{\infty}(-1)^j\frac{(2j+1)\,\mathrm{sech}\{\frac12(2j+1)y\}}{1+(2j+1)^2n^2} = \frac{z^2\sqrt{x(1-x)}}{1+(nz)^2(1-2x)+\cfrac{2^2(2^2-1)x(1-x)(nz)^4}{1+(3nz)^2(1-2x)+\cfrac{4^2(4^2-1)x(1-x)(nz)^4}{1+(5nz)^2(1-2x)+\cdots}}};$$

**(iii)**

$$2\sum_{j=0}^{\infty}\frac{(2j+1)\,\mathrm{csch}\{\frac12(2j+1)y\}}{1+(2j+1)^2n^2} = \frac{z^2\sqrt{x}}{1+(nz)^2(1+x)-\cfrac{2^2(2^2-1)x(nz)^4}{1+(3nz)^2(1+x)-\cfrac{4^2(4^2-1)x(nz)^4}{1+(5nz)^2(1+x)-\cdots}}}.$$

书中称 (i)(ii) 要求 $0 < x < 1/\sqrt{2}$（见下文“适用范围订正”）。

**第 13 节推论。** 设 $n > 0$，$\mu = \sqrt{\pi}/\Gamma^2(3/4)$。则

$$\sum_{j=0}^{\infty}(-1)^j\frac{(2j+1)\,\mathrm{sech}\{\frac12(2j+1)\pi\}}{1+(2j+1)^2n^2} = \frac14\left(\frac{\mu^2}{1+\cfrac{1\cdot 3(n\mu)^4}{1+\cfrac{6\cdot 10(n\mu)^4}{1+\cfrac{15\cdot 21(n\mu)^4}{1+\cdots}}}}\right).$$

证明：在 Entry 13(ii) 中取 $y = \pi$，则 $x = \frac12$，由 Ch. 17 (6.15) 得 $z = \mu$。

**说明。**(i)(ii)(iii) 分别为 $\mathrm{cd}$、$\mathrm{sd}$、$\mathrm{sn}$ 的 Laplace 变换连分数（Stieltjes–Rogers 方法；积分表示见 (13.1)、(13.4)、(13.7)）。证明中收敛条件为 Perron Satz 2.16 的 $k/k' < 1$，即 $x < 1/2$。

**适用范围订正（数值复核发现）。** 书中 (i)(ii) 的适用范围“$0 < x < 1/\sqrt{2}$”过宽，证明自身的 Perron 条件 $k/k' < 1$ 等价于 $x < 1/2$；书中收敛句“$k/k' < 1$ 或 $x < 1/\sqrt{2}$”前后亦不一致（$k/k' < 1$ 当且仅当 $x < 1/2$）。数值结果：(ii) 在 $0 < x < 1/2$ 内成立（$x = 0.25$ 时 Lentz 算法差 $4.0\times 10^{-32}$；$x = 0.4$、$0.45$、$0.49$、$0.499$ 均与左端一致；积分 (13.4) 在 $x = 0.25$、$0.4$、$0.5$ 处与左端一致）；但在端点 $x = 1/2$ 处，连分数收敛到约 $0.63754$，而左端为 $0.388047266716$（正向渐近分数：深度 10 得 $0.64543$，100 得 $0.63842$，1000 得 $0.63763$，尾和仅约 $9\times 10^{-5}$，极限确为约 $0.63754$，不可能到达 $0.38805$；后向递推 $N = 20000$ 与 Lentz 算法一致）；在 $x > 1/2$ 处亦不成立（$x = 0.6$ 时连分数 $-4.09$，左端 $0.436$；$x = 0.7$ 时连分数 $-1.83$，左端 $0.485$）。(i) 在 $0 < x \le 1/2$ 内成立（积分 (13.1) 精确成立；$x = 1/2$ 处连分数以 $1/N$ 速率缓慢收敛，$N = 5000$ 时得 $0.43097$，左端 $0.431002017567$），但在 $x > 1/2$ 处不成立（$x = 0.6$ 时连分数 $1.133$，左端 $0.501$；$x = 0.7$ 时连分数 $1.233$，左端 $0.583$）。故 (i)(ii) 的正确适用范围为 $0 < x < 1/2$（(i) 含端点 $x = 1/2$），而非书中所称 $0 < x < 1/\sqrt{2}$。**第 13 节推论因此按原样不成立**（它在 (ii) 中取 $x = 1/2$）：$n = 1$ 时左端 $0.194023633358$，连分数值约 $0.3188$。以上均列入待核对清单，待查 Berndt 勘误与文献。

**状态：**(i)(iii) 已证明（书中给出证明；(i) 的适用范围以 $0 < x \le 1/2$ 为限）；(ii) 已证明（书中给出证明；适用范围以 $0 < x < 1/2$ 为限，端点 $x = 1/2$ 除外）；第 13 节推论按原样不成立（见上文）。**对照：** M03（连分数）、M11、M10（$\mu$）、M04。

**我自验：** 取 $x = 0.5$、$n = 1$：(i) 积分 (13.1) 差 $9.8\times 10^{-15}$（数值积分容差；直接求和左端 $0.431002017567$）；(ii) 积分 (13.4) 差 $1.3\times 10^{-15}$（数值积分容差）；(iii) 差 $4.9\times 10^{-32}$。$x = 0.25$ 时 (ii) 的 Lentz 算法差 $9.9\times 10^{-32}$。第 13 节推论 $n = 1$ 时左端 $0.194023633358$、连分数 $0.318778626464$，差 $0.1248$（mpmath 30 位）。

## Entry 14

**陈述。** 设 $S$、$C$、$C_1$ 如第 14 节 (14.1) 所定义，$\varphi$ 由 (14.8) 定义。则

$$(14.2)\quad C^2+S^2 = \tfrac14xz^2;$$

$$(14.3)\quad C_1^2+S^2 = \tfrac14z^2;$$

$$(14.4)\quad CS = \sum_{j=1}^{\infty}\frac{j\sin(2j\theta)}{\cosh(jy)};$$

$$(14.5)\quad 2CS+\frac{dC_1}{d\theta} = 0;$$

$$(14.6)\quad 2C_1S+\frac{dC}{d\theta} = 0;$$

$$(14.7)\quad 2CC_1 = \frac{dS}{d\theta};$$

$$(14.9)\quad C_1 = \tfrac12z\sqrt{1-x\sin^2\varphi};$$

$$(14.10)\quad z\cos\varphi\sqrt{1-x\sin^2\varphi} = \frac{d\sin\varphi}{d\theta} = \cos\varphi\,\frac{d\varphi}{d\theta};$$

$$(14.11)\quad \theta = \frac1z\int_0^{\varphi}\frac{d\varphi}{\sqrt{1-x\sin^2\varphi}}.$$

此外 (14.15)：$\sum_{n=-\infty}^{\infty}\mathrm{csch}^2\{\frac12(2n+1)y\} = 4\sum_{n=1}^{\infty}n/\sinh(ny)$；Berndt 命题 2.25：$\alpha$、$\beta > 0$，$\alpha\beta = \pi^2$，则 $\alpha\sum_{n=1}^{\infty}\mathrm{csch}^2(\alpha n) + \beta\sum_{n=1}^{\infty}\mathrm{csch}^2(\beta n) = (\alpha+\beta)/6 - 1$。

**说明。**(14.2)–(14.7) 为 $S$、$C$、$C_1$ 的代数与微分关系（即 $\mathrm{sn}$、$\mathrm{cn}$、$\mathrm{dn}$ 的恒等式）；(14.11) 为拉马努金形式的椭圆积分反演。证明用 $S$、$C$、$C_1$ 的 Fourier 级数定义与 (14.1)。

**状态：** 已证明（书中给出证明）。**对照：** M11（$\mathrm{sn}$、$\mathrm{cn}$、$\mathrm{dn}$）、M02、M09（(14.11) 的积分反演）。

**我自验：** 取 $x = 0.5$、$\theta = 0.5$：(14.2) 差 $2.5\times 10^{-32}$，(14.3) 差 $9.9\times 10^{-32}$，(14.4) 差 $4.9\times 10^{-32}$，(14.5)(14.6) 差 $0$，(14.7) 差 $9.9\times 10^{-32}$；$\varphi(0.5) = 0.574295226452$，$\sin^2\varphi+\cos^2\varphi-1 = -3.0\times 10^{-31}$；(14.9) 差 $9.9\times 10^{-32}$，(14.11) 差 $0$；(14.15) 差 $9.9\times 10^{-32}$；Berndt 命题 2.25 取 $\alpha = 2$、$\beta = \pi^2/2$：差 $2.0\times 10^{-31}$（mpmath 30 位）。

## Entry 15

**陈述。** 设 $\varphi$ 由 (14.8) 定义。则

**(i)** $1+2\sum_{n=1}^{\infty}\cos(2n\theta)/\cosh(ny) = z\sqrt{1-x\sin^2\varphi}$；

**(ii)** $\sum_{n=0}^{\infty}\cos(2n+1)\theta/\cosh\{\frac12(2n+1)y\} = \frac12z\sqrt{x}\cos\varphi$；

**(iii)** $\sum_{n=0}^{\infty}\sin(2n+1)\theta/\sinh\{\frac12(2n+1)y\} = \frac12z\sqrt{x}\sin\varphi$；

**(iv)** $\theta + \sum_{n=1}^{\infty}\sin(2n\theta)/(n\cosh(ny)) = \varphi$；

**(v)** $\sum_{n=0}^{\infty}\sin(2n+1)\theta/((2n+1)\cosh\{\frac12(2n+1)y\}) = \frac12\sin^{-1}(\sqrt{x}\sin\varphi)$；

**(vi)** $\sum_{n=0}^{\infty}\cos(2n+1)\theta/((2n+1)\sinh\{\frac12(2n+1)y\}) = -\frac12\,\mathrm{Log}\frac{\sqrt{1-x\sin^2\varphi}-\sqrt{x}\cos\varphi}{\sqrt{1-x}}$。

**说明。**(i)–(iii) 为 (14.1) 的重述；(iv) 归于 Jacobi；(v)(vi) 为 $\varphi$ 的反正弦与对数表示。**拉马努金笔误**：笔记 p. 222 的 (vi) 右端漏写负号（Berndt 注明）。

**状态：** 已证明（书中给出证明）。**对照：** M11、M02。

**我自验：** 取 $x = 0.5$、$\theta = 0.5$：(i) 差 $2.0\times 10^{-31}$，(ii) 差 $0$，(iii) 差 $2.5\times 10^{-32}$，(iv) 差 $0$，(v) 差 $2.5\times 10^{-32}$，(vi) 差 $2.5\times 10^{-31}$（mpmath 30 位；(vi) 按书中带负号的式子验证通过）。

## Entry 16

**陈述。**

**第一部分。** $\theta\to\frac12\pi-\theta$ 时，$\varphi$ 的函数按下表变换：$\cot\varphi\to\sqrt{1-x}\tan\varphi$；$\sin\varphi\to\cos\varphi/\sqrt{1-x\sin^2\varphi}$；$\cos\varphi\to\sqrt{1-x}\sin\varphi/\sqrt{1-x\sin^2\varphi}$；$\sqrt{1-x\sin^2\varphi}\to\sqrt{1-x}/\sqrt{1-x\sin^2\varphi}$。

**第二部分。**

**(i)** $\sum_{n=0}^{\infty}(-1)^n\cos(2n+1)\theta/\sinh\{\frac12(2n+1)y\} = \frac12z\sqrt{x}\cos\varphi/\sqrt{1-x\sin^2\varphi}$；

**(ii)** $\sum_{n=0}^{\infty}(-1)^n\sin(2n+1)\theta/\cosh\{\frac12(2n+1)y\} = \frac12z\sqrt{x(1-x)}\sin\varphi/\sqrt{1-x\sin^2\varphi}$；

**(iii)** $\csc\theta + 4\sum_{n=0}^{\infty}\sin(2n+1)\theta/(e^{(2n+1)y}-1) = z\csc\varphi$；

**(iv)** $\sec\theta + 4\sum_{n=0}^{\infty}(-1)^n\cos(2n+1)\theta/(e^{(2n+1)y}-1) = z\sec\varphi\sqrt{1-x\sin^2\varphi}$；

**(v)** $\mathrm{Log}\tan(\pi/4+\theta/2) + 4\sum_{n=0}^{\infty}(-1)^n\sin(2n+1)\theta/((2n+1)(e^{(2n+1)y}-1)) = \mathrm{Log}\tan(\pi/4+\varphi/2)$。

**说明。** 第一部分为 $\theta\to\frac12\pi-\theta$ 的换表（由 (14.8) 与 (14.11) 直接得）；第二部分 (i)(ii) 为 (i)(ii) 的 $(-1)^n$ 形式，(iii)–(v) 涉及 $\mathrm{dc}\,u$、$\mathrm{ns}\,u$ 的 Fourier 级数，Berndt 注明“somewhat mysterious”，因拉马努金此前并未记录证明所需的 $\mathrm{dc}\,u$、$\mathrm{ns}\,u$ Fourier 级数。

**状态：** 已证明（书中给出证明；(iii)–(v) 的证明工具在拉马努金笔记中未出现，见上文）。**对照：** M11、M02。

**我自验：** 取 $x = 0.5$、$\theta = 0.5$：(i) 差 $9.9\times 10^{-32}$，(ii) 差 $2.5\times 10^{-32}$，(iii) 差 $0$，(iv) 差 $2.0\times 10^{-31}$，(v) 差 $9.9\times 10^{-32}$（mpmath 30 位）。

## Entry 17

**陈述。** 设 $L(e^{-2y}) = 1 - 24\sum_{n=1}^{\infty}n/(e^{2ny}-1)$。则

**(i)** $\cos\theta/\sin^3\theta - 8\sum_{n=1}^{\infty}n^2\sin(2n\theta)/(e^{2ny}-1) = z^3\cos\varphi/\sin^3\varphi\cdot\sqrt{1-x\sin^2\varphi}$；

**(ii)** $1/\sin^2\theta - 8\sum_{n=1}^{\infty}n\cos(2n\theta)/(e^{2ny}-1) = z^2/\sin^2\varphi - \frac13z^2(1+x) + \frac13L(e^{-2y})$；

**(iii)** $\cot\theta + 4\sum_{n=1}^{\infty}\sin(2n\theta)/(e^{2ny}-1) = z\cot\varphi\sqrt{1-x\sin^2\varphi} + z\int_0^{\varphi}\sqrt{1-x\sin^2\varphi}\,d\varphi - \frac{2\theta z}{\pi}\int_0^{\pi/2}\sqrt{1-x\sin^2\varphi}\,d\varphi$；

**(iv)** $\sum_{n=1}^{\infty}\sin(2n\theta)/\sinh(ny) = \frac12z\int_0^{\varphi}\sqrt{1-x\sin^2\varphi}\,d\varphi - \frac{\theta z}{\pi}\int_0^{\pi/2}\sqrt{1-x\sin^2\varphi}\,d\varphi$。

其中 $E = \int_0^{\pi/2}\sqrt{1-x\sin^2\varphi}\,d\varphi$ 为第二类完全椭圆积分；(17.4)：$L(e^{-2y}) = 6zE/\pi - 2z^2 + xz^2$。

**说明。**(ii) 与 (iv) 归于 Jacobi（Whittaker–Watson [1, p. 520]）；(iii)(iv) 的右端含第二类椭圆积分（不完全与完全）。证明用 $\mathrm{sn}$、$\mathrm{cn}$、$\mathrm{dn}$ 的 Fourier 级数逐项微分与积分。

**状态：** 已证明（书中给出证明）。**对照：** M11、M02、M06（$L(e^{-2y})$）、M09（椭圆积分 $E$）。

**我自验：** 取 $x = 0.5$、$\theta = 0.5$：(i) 差 $7.9\times 10^{-31}$，(ii) 差 $7.9\times 10^{-31}$，(iii) 差 $2.0\times 10^{-31}$，(iv) 差 $1.2\times 10^{-32}$（mpmath 30 位）。

## Entry 18

**陈述。** 设 $\Omega(x,e^{-y},z,\theta,\varphi) = 0$ 为第 18 节的一般方程 (18.1)。则

**(i)** $\theta\to\frac12\theta$、$y\to\frac12y$ 时（dimidiation）：$\Omega(4\sqrt{x}/(1+\sqrt{x})^2, e^{-y/2}, (1+\sqrt{x})z, \frac12\theta, \frac12(\varphi+\sin^{-1}(\sqrt{x}\sin\varphi))) = 0$；

**(ii)** $\theta\to\frac12\pi-\theta$、$e^{-y}\to -e^{-y}$ 时（change of sign）：$\Omega(x/(x-1), -e^{-y}, z\sqrt{1-x}, \frac12\pi-\theta, \frac12\pi-\varphi) = 0$；

**(iii)** $e^{-y}\to -e^{-y}$ 时：$\Omega(x/(x-1), -e^{-y}, z\sqrt{1-x}, \theta, \cot^{-1}(\cot\varphi/\sqrt{1-x})) = 0$；拉马努金（笔记 p. 223）曾错误断言 $\cot\varphi$ 变为 $\sqrt{1-x}\cot\varphi$（Berndt 注明）；

**(iv)** 虚变换：置 $z' = {}_2F_1(\frac12,\frac12;1;1-x)$、$y' = \pi z/z'$；$\theta\to i\theta z/z'$、$y\to y'$ 时：$\Omega(1-x, e^{-y'}, z', i\theta z/z', i\,\mathrm{Log}\tan(\pi/4+\varphi/2)) = 0$；此时 $\sin\varphi\to i\tan\varphi$，$\cos\varphi\to\sec\varphi$。

证明中用 (18.4)：$\frac1z(\cot\theta - 4\sum_{n=1}^{\infty}e^{-2ny}\sin(2n\theta)/(1+e^{-2ny})) = \mathrm{cs}(z\theta) = \mathrm{cn}(z\theta)/\mathrm{sn}(z\theta) = \cot\varphi$（见下文“新发现的印文问题”）。

**新发现的印文问题（18.4)。** 书中 (18.4) 印为 $\frac12(\cot\theta - 4\sum_{n=1}^{\infty}e^{-2ny}\sin(2n\theta)/(1+e^{-2ny})) = \mathrm{cs}(z\theta)$，即首因子为 $1/2$；数值复核表明首因子应为 $1/z$：取 $x = 0.5$、$\theta = 0.5$，按 $1/2$ 计左端 $0.9121005773$，而 $\mathrm{cs}(z\theta) = 1.5454870875$；按 $1/z$ 计差 $2.0\times 10^{-31}$；另在 $(x,\theta) = (0.25,0.3)$、$(0.5,1.0)$、$(0.75,0.7)$ 三点差分别为 $3.9\times 10^{-31}$、$9.9\times 10^{-32}$、$0$。佐证有二：其一，书中下一句的变换后左端 $1/(z\sqrt{1-x})$ 仅当 (18.4) 取 $1/z$ 时成立；其二，Fourier 分析：$\mathrm{cs}(z\theta)-\cot\theta$ 的系数趋于 $2(1/z-1)$（$x = 0.5$ 时为 $-0.30557$；前三系数 $-0.31189$、$-0.30559$、$-0.30557$）；mpmath 的 $\mathrm{ellipfun}$ 独立确认 $\mathrm{sn}(z\theta) = \sin\varphi$、$\mathrm{cn}(z\theta) = \cos\varphi$、$\mathrm{cs}(z\theta) = \cot\varphi$。300 DPI 放大图确认印文确为 $1/2$。本条列入待核对清单，待查 Berndt 勘误。

**状态：** 已证明（书中给出证明；(18.4) 的首因子按上文订正为 $1/z$）。**对照：** M11（参数变换）、M06（模变换）。

**我自验：** 取 $x = 0.5$、$\theta = 0.5$：(i) 的 $\varphi$ 变换经 Entry 15(iv) 验证，差 $4.9\times 10^{-32}$；(18.4) 按 $1/z$ 计差 $0$（mpmath 30 位）。

## Entry 19

**陈述。**

**(i)** 椭圆弧（Legendre）：$L(AP) = a\int_0^{\varphi}\sqrt{1-e^2\cos^2\varphi}\,d\varphi$；

**(ii)** 双曲弧（Legendre；Landen 1775 年）：$L(AP) = a\tan\varphi\sqrt{e^2-\cos^2\varphi} - a\int_0^{\varphi}\sqrt{e^2-\cos^2\varphi}\,d\varphi + (b^2/a)\int_0^{\varphi}d\varphi/\sqrt{e^2-\cos^2\varphi}$；

**(iii)** $L = \pi(a+b)(1+4\sin^2(\frac12\theta))$，$0\le\theta\le\pi$，$\sin\theta = \sqrt{x}\sin\varphi$，$x = ((a-b)/(a+b))^2$；$e = 1$ 时 $\varphi = 30^\circ18'6''$，$e\to 0$ 时 $\varphi\to 30^\circ$ 单调；

**(iv)** $L = \pi(a+b)(1+\sin^2\theta/(2+\cos^2(\frac12\theta)))$；$e = 1$ 时 $\varphi = 60^\circ4'55''$，$e = 0$ 时 $\varphi = 60^\circ$；$\varphi$ 关于 $e$ 的单调性仅为猜想，未证明。

**推论 (i)。** $L = \pi(a+b)\tan\theta/\theta$，$0\le\theta<\pi/2$，$\tan\theta = \sqrt{x}\cos\varphi$；$e$ 由 $0$ 变到 $1$ 时，$\varphi$ 由 $\pi/6$ 递减到 $0$；$\varphi$ 近似于 $(2\sqrt{ab}/(a+b))\{30^\circ + 6^\circ18'49''(\sqrt{a}-\sqrt{b})^2/(a+b) - 1^\circ10'55''(a-b)^2/(a+b)^2\}$。(19.19)：$\varphi\approx\sqrt{1-x}(A+B\{1-\sqrt{1-x}\}+Cx)$；(19.20)：$\varphi = \pi/6 - (21\sqrt{3}/160)x + O(x^2)$；(19.21)–(19.23) 为 $x\to 1$ 附近的展开。

**推论 (ii)。** 在 $L(AJ)/L(AK) = L(AB)/AN$（(19.28)）的条件下，$\varphi\approx 30^\circ - x(1-x)(11'22'' + 32'42''x)$（(19.29)），$x = ((a-b)/(a+b))^2$；拉马努金的版本 (19.30) $30^\circ + x(1-x)(5^\circ19.4' - 6^\circ3.5'x)$ 是错误的（Berndt 注明为计算错误）。(19.29) 在 $x = 0.6213949$（$e = 0.9929672$）处有局部极小值 $29^\circ52'33''$。(19.34)：$\tan(\frac32\tan^{-1}(\sqrt{x}\tan\varphi))/(\frac32\tan^{-1}(\sqrt{x}\tan\varphi)) = {}_2F_1(-\frac12,-\frac12;1;x)$；(19.36)：$\varphi = \pi/6 - (11\sqrt{3}/5760)x + O(x^2)$；(19.37) 为 $x\to 1$ 附近的展开。Villarino 以 $e$ 的幂级数加强了 (iii)(iv)。

**状态：**(i)(ii) 已证明（Legendre、Landen 的经典结果，书中给出证明）；(iii) 已证明（书中给出证明）；(iv) 的公式已证明，$\varphi$ 单调性为猜想（未证明）；推论 (i)(ii) 为近似式（“approximately”），其中 (19.30) 为拉马努金的错误版本。**对照：** M11（椭圆弧）、M09（积分）、M04（角度数值）。

**我自验：** 取 $a = 2$、$b = 1$：(i)(ii) 的积分与右端差均为 $0$（mpmath 30 位，数值积分）；(iii) 由 (19.34) 解得 $\varphi(e=1) = 30.30174008^\circ = 30^\circ18'6.3''$，与书中 $30^\circ18'6''$ 一致；(iv) $\varphi(e=1) = 60.08205501^\circ = 60^\circ4'55.4''$，与书中 $60^\circ4'55''$ 一致。推论 (i)：$\varphi = 28.502801^\circ$，近似式 $28.500886^\circ$，差 $6.8''$。推论 (ii)：由 (19.34) 解得真 $\varphi$：$x = 0.5$ 时 $29.926912^\circ$，(19.29) 近似 $29.884514^\circ$（差 $2.544'$）；$x = 0.6213949$ 时真 $\varphi = 29.921523^\circ$，(19.29) 近似 $29.875756^\circ$（差 $2.746'$）；$x = 0.3$ 时差 $1.394'$，$x = 0.8$ 时差 $1.927'$——故 (19.29) 为中段误差数角分的粗近似。(19.36)：$\varphi(0.01) = 0.5235657728$，$\pi/6 - (11\sqrt{3}/5760)\cdot 0.01 = 0.5235656982$，差 $7.5\times 10^{-8}$（$O(x^2)$ 量级）。

## Entry 20

**陈述。**

**(i)** 化圆为方：$RD^2 = \frac14PR^2\cdot 355/113$；$\pi\approx 355/113 = 3.14159292$，与 $\pi$ 相差约 $0.00000027$；拉马努金注：对面积为 14 平方英里的圆，$RD$ 比真长多 $1/100$ 英寸（$RD-\frac12d\sqrt{\pi} = 0.0100653026$，$d$ 为直径）。

**推论 (i)。** $(31)^{1/3} = 3.1413807$ 为 $\pi$ 近似（相差约 $0.00021$）；$m/(\frac12d\sqrt{\pi}) = (31)^{1/6}/\sqrt{\pi}\approx 1-1/29630$。

**推论 (ii)。** $\pi\approx(97\frac12-1/11)^{1/4}$；对面积为一百万平方英里的圆，误差约 $1/100$ 英寸（$0.0101561291$）。

**(ii)** $A^3+B^3 = C^2$ 的参数解（Euler；Hoppe 重新发现）：$A = 3n^3+6n^2-n$，$B = -3n^3+6n^2+n$，$C = 6n^2(3n^2+1)$（$n$ 任意）。

**(iii)** $A^3+B^3+C^3 = D^3$ 的参数解：$A = m^7-3(p+1)m^4+(3p^2+6p+2)m$，$B = 2m^6-3(2p+1)m^3+(3p^2+3p+1)$，$C = m^6-(3p^2+3p+1)$，$D = m^7-3pm^4+(3p^2-1)m$（$m$、$p$ 任意）。

例题（书页 199，300 DPI 核对）：$(11\frac12)^3+(\frac12)^3 = 39^2$（$n = 2$）；$(3-1/105)^3+(1/105)^3 = (5\frac{6}{35})^2$（$n = 15/7$）；$(3\frac17)^3-(1/7)^3 = (5\frac47)^2$（$n = 1/7$）；$(3\frac{1}{104})^3-(1/104)^3 = (5\frac{23}{104})^2$（$n = 13/6$）；$11^3+37^3 = 228^2$（$n = 1/4$）；$71^3-23^3 = 588^2$（$n = 4$）；$3^3+4^3+5^3 = 6^3$（$m = p = 2$）；$1^3+12^3 = 9^3+10^3$（$m = 2$、$p = 3$；即 1729，Frenicle 1657 年已先发现）；$1^3+75^3 = (70\frac12)^3+(41\frac12)^3$（$m = 3$、$p = 11$）；$3^3+509^3+34^6 = 1188^3$（$m = 4$、$p = 53/2$；$34^6 = 1156^3$）；$18^3+19^3+21^3 = 28^3$（$m = 2$、$p = 1$）；$7^3+14^3+17^3 = 20^3$（$m = 2$、$p = -1$）；$19^3+60^3+69^3 = 82^3$（$m = 2$、$p = -2$）；$15^3+82^3+89^3 = 108^3$（$m = 2$、$p = -3$）；$3^3+36^3+37^3 = 46^3$（$m = 2$、$p = -4$）；$1^3+135^3+138^3 = 172^3$（$m = 2$、$p = -5$）；$23^3+134^3 = 95^3+116^3$（$m = 2$、$p = -10$）；$133^3+174^3 = 45^3+196^3$（$m = 2$、$p = -13$）；$1^3+6^3+8^3 = 9^3$（在 Entry 20(iii) 的参数解范围之外——拉马努金知最一般解）。另：$133^4+134^4 = 158^4+59^4 = 635,318,657$（Euler）。$1^3+12^3 = 9^3+10^3$ 亦见于拉马努金“lost notebook”残页（p. 341）。

**状态：**(i) 与推论 (i)(ii) 为近似作图（“very nearly”/“nearly”量级，书中给出误差）；(ii)(iii) 为参数恒等式，已证明（Euler 的参数解；书中给出证明）。**对照：** M04（$\pi$ 近似与化圆为方）、M01（丢番图方程）、M14（参数解）。

**我自验：** $355/113-\pi = 2.668\times 10^{-7}$；(i) $RD-\frac12d\sqrt{\pi} = 0.01006530264$（书 $0.0100653026$）；推论 (i) $(31)^{1/6}/\sqrt{\pi} = 0.999966258392$，$1-1/29630 = 0.999966250422$；推论 (ii) 误差 $0.01015612909$（书 $0.0101561291$）。(ii) 参数恒等式对 $n = 2$、$15/7$、$1/7$、$13/6$、$1/4$、$4$ 六值精确成立，六个所列例子精确成立。(iii) 参数恒等式对六组 $(m,p)$ 精确成立，11 个所列数值例子精确成立（其中 $(1,75)$ 例正确读作 $(70\frac12)^3+(41\frac12)^3$：$1+75^3 = (141/2)^3+(83/2)^3 = 421876$）；$3^3+509^3+34^6 = 1188^3 = 1676676672$；$1^3+6^3+8^3 = 729 = 9^3$（有理数精确运算）。

## Entry 21

**陈述。** 设 $x$ 为任意复数，除左端函数的极点外。则

**(i)**

$$\frac{\pi}{3\sqrt{3}x^2}\cdot\frac{\cosh(\pi\sqrt{3}x)+2\cos(\pi x)}{\cosh(\pi\sqrt{3}x)-\cos(\pi x)} = \frac{1}{2\sqrt{3}\pi x^4} + \sum_{n=1}^{\infty}\frac{n}{x^4+n^2x^2+n^4} + 2\sum_{n=1}^{\infty}\frac{(-1)^nn}{(x^4+n^2x^2+n^4)(e^{n\pi\sqrt{3}}-(-1)^n)};$$

**(ii)**

$$\frac{\pi}{3\sqrt{3}x^2}\cdot\frac{\cosh(\pi\sqrt{3}x)+2\cos(\pi x)+6\cosh(\pi x/\sqrt{3})}{\cosh(\pi\sqrt{3}x)-\cos(\pi x)} = \frac{\sqrt{3}}{2\pi x^4} + \sum_{n=1}^{\infty}\frac{n}{x^4+n^2x^2+n^4} + 2\sum_{n=1}^{\infty}\frac{(-1)^nn}{(x^4+n^2x^2+n^4)(e^{n\pi\sqrt{3}}-(-1)^n)} + 2\sum_{n=1}^{\infty}\frac{(-1)^nn\rho(n)}{x^4+n^2x^2+n^4},$$

其中 $\rho(n) = \cosh(\frac12\pi n/\sqrt{3})/\sinh(\frac12\pi n\sqrt{3})$（$n$ 为偶数），$\rho(n) = \sinh(\frac12\pi n/\sqrt{3})/\cosh(\frac12\pi n\sqrt{3})$（$n$ 为奇数）。

注意 $\rho(n)$ 的分子用 $\frac12\pi n/\sqrt{3}$、分母用 $\frac12\pi n\sqrt{3}$（混合式；300 DPI 确认，与证明 (21.5)(21.6) 一致）；150 DPI 下易误读为分子分母皆 $/\sqrt{3}$，彼读法数值不成立。

**(iii)**

$$\frac{2\pi}{\sqrt{3}x^2}\cdot\frac{1}{e^{2\pi\sqrt{3}x}-2e^{\pi\sqrt{3}x}\cos(\pi x)+1} = \frac{1}{2\sqrt{3}\pi x^4} - \frac{1}{2x^3} + \frac{2\pi}{3\sqrt{3}x^2} + 2\sum_{n=1}^{\infty}\frac{(-1)^nn}{(x^4+n^2x^2+n^4)(e^{n\pi\sqrt{3}}-(-1)^n)} - \frac1x\sum_{n=1}^{\infty}\frac{1}{x^2+nx+n^2};$$

**(iv)**

$$\frac{2\pi}{\sqrt{3}x^2}\cdot\frac{1}{e^{2\pi\sqrt{3}x}-2e^{\pi\sqrt{3}x}\cos(3\pi x)+1} = \frac{1}{6\sqrt{3}\pi x^4} - \frac{1}{6x^3} + \frac{\pi}{3\sqrt{3}x^2} + 6\sum_{n=1}^{\infty}\frac{(-1)^nn}{(9x^4-3n^2x^2+n^4)(e^{n\pi\sqrt{3}}-(-1)^n)} - \frac1x\sum_{n=1}^{\infty}\frac{1}{3x^2+3nx+n^2}.$$

**第 21 节例题。**

$$\sum_{n=1}^{\infty}\frac{(-1)^{n-1}n}{81+9n^2+n^4} = \frac{1}{324\sqrt{3}\pi} + \frac{11}{756} + \frac{\pi}{27\sqrt{3}} + \frac{\pi}{18\sqrt{3}(1+\cosh(3\sqrt{3}\pi))}.$$

书中称此版本与拉马努金（笔记 p. 226）的版本有两处不同：拉马努金作 $25/756$（而非 $11/756$）与 $-\pi/(54\sqrt{3})$（而非 $\pi/(27\sqrt{3})$）；又称若 (21.8) 中出现 $1/108$ 而非 $-1/108$，则得 $25/756$；对拉马努金的另一数值错误“无解释”。

**说明。**(i)–(iv) 为 $f(x) = \pi(\cosh(\pi\sqrt{3}x)+2\cos(\pi x))/(3\sqrt{3}x^2(\cosh(\pi\sqrt{3}x)-\cos(\pi x)))$（(21.1)）及其变形的部分分式展开；极点在 $x = n\exp(\pm\pi i/3)$。拉马努金笔记中 (ii) 的表述“does not appear to be correct”（Berndt 注明，笔记 p. 226）。证明用留数定理：(i) 的留数含 $\coth(\frac12\pi n\sqrt{3})$、$\tanh(\frac12\pi n\sqrt{3})$（(21.2)(21.3)）；(ii) 的证明置 $h(x) = f(x)+g(x)$，$g$ 的留数给出 (21.5)(21.6) 的 $\rho(n)$ 项（见下文“证明中的印文问题”）。(21.9)：$\sum_{n=0}^{\infty}1/((nx+y)^2-z^2) = (1/(2xz))\{\psi((y+z)/x)-\psi((y-z)/x)\}$；$\psi(\frac12+z)-\psi(\frac12-z) = \pi\tan(\pi z)$（(21.10)）。书末注记：$\sum_{n=1}^{\infty}1/(n^2+nx+y)$ 在 $x$ 为整数时可用 $\psi$ 函数精确求值。

**证明中的印文问题（$g(x)$ 的系数）。** (ii) 的证明定义 $g(x) := 2\pi\cosh(\pi x/\sqrt{3})/(3\sqrt{3}x^2(\cosh(\pi\sqrt{3}x)-\cos(\pi x)))$，并置 $h = f+g$，称 $h$ 的展开即 Entry 21(ii)。但 (ii) 左端 $= f + 3g$（$6\cosh$ 项）；且 (21.7) 称 $g(x) = 1/(\pi\sqrt{3}x^4)+O(1)$，而按 $2\pi$ 的定义 $g(x) = 1/(3\sqrt{3}\pi x^4)+O(1)$；(ii) 右端首项 $\sqrt{3}/(2\pi x^4) = 1/(2\sqrt{3}\pi x^4) + 1/(\pi\sqrt{3}x^4)$ 亦要求 $g$ 的主部为 $1/(\pi\sqrt{3}x^4)$。三处一致表明 $g(x)$ 定义式的系数应为 $6\pi$ 而非 $2\pi$（留数 (21.5)(21.6) 与 (ii) 的 $\rho$ 和式一致，说明计算按 $6\pi$ 进行）。列入待核对清单，待查 Berndt 勘误。

**第 21 节例题不成立（数值复核发现）。** 例题按原样数值不成立：左端直接求和 $= 0.00323859$（400 项，交错尾项 $< 10^{-8}$；另由 $C = B(3)-B(3/2)/4$ 验算，$B(x) = \sum n/(x^4+n^2x^2+n^4)$，得 $0.00323859$，一致），右端 $= 0.08229525$，差 $0.0790567$。拉马努金的版本右端 $= 0.00004713$，亦不成立（差 $0.00319$）。证明中的错误至少有一处已定位：p. 206 用 (21.9)（$n$ 从 $0$ 求和）计算 $\sum_{n=1}^{\infty}1/(n^2+3n+9)$ 时漏减 $n = 0$ 项 $1/9$，故书中 $S = -1/7 + \pi/(3\sqrt{3})\tanh(\frac12(3\sqrt{3})\pi) = 0.46174255$ 比真值 $0.35062043$ 大 $1/9$（差 $0.11112211$，余为尾项近似误差）；仅此一项已使 (21.8) 的代入值偏离 $1/54 = 0.0185185$，而例题总偏差 $0.0790567$ 尚余约 $0.0605$ 未解释，表明从 (21.8) 化简为例题的步骤另有错误。例题的正确闭式需重新推导（见待核对清单）。(21.8) 本身经数值验证成立（差 $7.8\times 10^{-17}$）。

**状态：**(i)–(iv) 已证明（书中给出证明；(ii) 的 $\rho(n)$ 按混合式理解，$g(x)$ 系数按 $6\pi$ 理解）；第 21 节例题按原样不成立（见上文）。**对照：** M02（部分分式）、M01（$\omega$ 极点）、M10（$\psi$ 函数）。

**我自验：** 取 $x = 1$、$3$、$0.5$：(i) 差 $\le 1.1\times 10^{-22}$，(ii) 差 $\le 1.1\times 10^{-22}$（$\sum n/(x^4+n^2x^2+n^4)$ 取 300 项并补 $\zeta(3)$、$\zeta(5)$、$\zeta(9)$ 解析尾项；$\rho$ 和式取 300 项）；$x = 1$、$3$ 时 (iii) 差 $\le 1.6\times 10^{-16}$，(iv) 差 $\le 4.2\times 10^{-15}$（$\psi$ 和取 300 项并补 $\zeta$ 尾项）；(21.8) 差 $7.8\times 10^{-17}$（mpmath 30 位）。

## Entry 22

**陈述。** 设 $0 < x < 1$，$n > 0$。则

**(i)**

$$\int_0^{\infty}\exp\left(-n\int_0^{\varphi}\frac{d\theta}{\sqrt{1-x\sin^2\theta}}\right)d\varphi = \frac{1}{n+\cfrac{x}{n+\cfrac{4}{n+\cfrac{9x}{n+\cfrac{16}{n+\cdots}}}}};$$

**(ii)**

$$\int_0^{\infty}\exp\left(-n\int_0^{\varphi}\frac{d\theta}{\sqrt{1-x\sin^2\theta}}\right)\frac{\cos\varphi}{\sqrt{1-x\sin^2\varphi}}\,d\varphi = \frac{1}{n+\cfrac{1}{n+\cfrac{4x}{n+\cfrac{9}{n+\cfrac{16x}{n+\cdots}}}}};$$

**(iii)**

$$\int_0^{\infty}\exp\left(-n\int_0^{\varphi}\frac{d\theta}{\sqrt{1-x\sin^2\theta}}\right)\frac{\cos\varphi}{1-x\sin^2\varphi}\,d\varphi = \frac{1}{n+\cfrac{1-x}{n-\cfrac{4x}{n+\cfrac{9(1-x)}{n-\cfrac{16x}{n+\cdots}}}}}.$$

**说明。** 左端为 $\mathrm{dn}$、$\mathrm{cn}$、$\mathrm{coam}$ 的 Laplace 变换（置 $u = \int_0^{\varphi}d\theta/\sqrt{1-x\sin^2\theta}$，则 (i) $= \int_0^{\infty}e^{-nu}\mathrm{dn}\,u\,du$，(ii) $= \int_0^{\infty}e^{-nu}\mathrm{cn}\,u\,du$，(iii) $= \int_0^{\infty}e^{-nu}\mathrm{cn}\,u/\mathrm{dn}\,u\,du$）；右端为相应的 Stieltjes–Rogers 连分数（(i) 用 (22.2) $\int_0^{\infty}e^{-nu}\mathrm{cn}\,u\,du$，(iii) 用 $\sin\mathrm{coam}\,u = \mathrm{cn}(k'u,ik/k')$）；收敛性用 Perron Satz 2.16。

**适用范围订正（数值复核发现）。**(i)(ii) 在书中所称 $0 < x < 1$ 全程成立（$x = 0.25$、$0.5$、$0.6$、$0.7$、$0.9$，$n = 1$、$2$，积分与连分数差 $\le 6\times 10^{-15}$）。但 (iii) 只在 $0 < x < 1/2$ 内成立（$x = 0.25$、$0.4$、$0.45$、$0.49$ 均成立；$x = 0.49$ 处连分数收敛缓慢，$N = 100$ 时得 $1.21$，$N = 5000$ 时得 $0.59775714$，与积分一致）；在 $x = 1/2$ 处，连分数收敛到约 $1.3078$，而积分值 $0.600501553$（$u$ 换元积分与 $\varphi$ 原式积分一致，$n = 1$；$n = 2$ 时积分 $0.433358861265$，连分数 $0.224900786314$）；在 $x = 0.6$、$0.7$、$0.9$ 处亦不成立（连分数 $1.2089$、$1.1366$、$1.0365$，积分 $0.63077$、$0.66784$、$0.78635$）。原因与 Entry 13(ii) 相同：(iii) 的证明用 $\sin\mathrm{coam}\,u = \mathrm{cn}(k'u,ik/k')$，其连分数收敛要求 $k/k' < 1$，即 $x < 1/2$。故 (iii) 的正确适用范围为 $0 < x < 1/2$，而非书中所称 $0 < x < 1$。列入待核对清单。

**状态：**(i)(ii) 已证明（书中给出证明）；(iii) 已证明（书中给出证明；适用范围以 $0 < x < 1/2$ 为限）。**对照：** M03（连分数）、M11、M09（Laplace 型积分）。

**我自验：** 取 $x = 0.5$、$n = 1$：(i) 积分 $0.885490610688$、连分数 $0.885490610688$，差 $4.5\times 10^{-16}$；(ii) $0.561828095622$，差 $1.9\times 10^{-15}$；(iii) 积分 $0.600501553012$、连分数（$N = 2000$ 后向递推）$1.30693320732$（mpmath 30 位；积分经 $u$ 换元与 $\varphi$ 原式双重验证一致）。

## Entry 23

**陈述。** 设 $\mathrm{Re}(x\pm iy) > 0$。则

**(i)**

$$\sqrt{2}\left\{\frac12+\sum_{n=1}^{\infty}\exp\left(-\frac{n^2\pi x}{x^2+y^2}\right)\cos\left(\frac{n^2\pi y}{x^2+y^2}\right)\right\} = (\sqrt{x^2+y^2}+x)^{1/2}\left\{\frac12+\sum_{n=1}^{\infty}e^{-n^2\pi x}\cos(n^2\pi y)\right\} + (\sqrt{x^2+y^2}-x)^{1/2}\sum_{n=1}^{\infty}e^{-n^2\pi x}\sin(n^2\pi y);$$

**(ii)**

$$\sqrt{2}\sum_{n=1}^{\infty}\exp\left(-\frac{n^2\pi x}{x^2+y^2}\right)\sin\left(\frac{n^2\pi y}{x^2+y^2}\right) = (\sqrt{x^2+y^2}-x)^{1/2}\left\{\frac12+\sum_{n=1}^{\infty}e^{-n^2\pi x}\cos(n^2\pi y)\right\} - (\sqrt{x^2+y^2}+x)^{1/2}\sum_{n=1}^{\infty}e^{-n^2\pi x}\sin(n^2\pi y).$$

**推论。** $\mathrm{Re}(x) > 0$ 时，

$$\frac12+\sum_{n=1}^{\infty}e^{-n^2\pi x}\cos(n^2\pi\sqrt{1-x^2}) = \frac{\sqrt{2}+\sqrt{1+x}}{\sqrt{1-x}}\sum_{n=1}^{\infty}e^{-n^2\pi x}\sin(n^2\pi\sqrt{1-x^2}).$$

证明：在 Entry 23(ii) 中取 $y = \sqrt{1-x^2}$ 化简即得。

**例题。** 记 $\varphi(q) = \sum_{n=-\infty}^{\infty}q^{n^2}$（Ch. 16 Entry 22）。则

$$(23.4)\quad \varphi(e^{-\pi}) = \sqrt{5\sqrt{5}-10}\,\varphi(e^{-5\pi});$$

$$(23.5)\quad (\sqrt{5}+\sqrt{3})\varphi(e^{-\pi\sqrt{5}/3}) = (3+\sqrt{3})\varphi(e^{-3\pi\sqrt{5}}).$$

**说明。** (i)(ii) 由反演公式 (23.1) $\sqrt{\alpha}\{\frac12+\sum e^{-\alpha n^2}\} = \sqrt{\beta}\{\frac12+\sum e^{-\beta n^2}\}$（$\alpha\beta = \pi$，$\mathrm{Re}\,\alpha$、$\mathrm{Re}\,\beta > 0$；亦见 Ch. 14 Entry 7 的推论、Ch. 16 Entry 27(i)、Ch. 17 第 6 节推论）经 $\alpha^2 = \pi(x\pm iy)$ 的代入与加减得。推论由 (ii) 取 $y = \sqrt{1-x^2}$ 得。(23.4) 的证明取 $\alpha^2 = 5\pi$、$\beta^2 = \pi/5$ 得 (23.6) $\sqrt{5}\varphi(e^{-5\pi}) = \varphi(e^{-\pi/5})$，再取 $x = 1$、$y = 2$ 用 Entry 23(i)。(23.5) 的证明取推论中 $x = \sqrt{5}/3$，得 $\cos(2\pi n^2/3)$、$\sin(2\pi n^2/3)$ 的和式，再化简。

**转录注意（(23.5) 的根号范围）。**(23.5) 的指数为 $e^{-\pi\sqrt{5}/3}$（根号只盖 $5$），而非 $e^{-\pi\sqrt{5/3}}$（根号盖 $5/3$）：按 $\sqrt{5}/3$ 计，左端与右端均为 $4.73205081423026$，差 $0$；按 $\sqrt{5/3}$ 计，左端 $4.10559090134$、右端 $4.73205081423$，差 $0.62646$。证明的每一步亦只对 $\sqrt{5}/3$ 成立：取 $x = \sqrt{5}/3$ 时 $\sqrt{1-x^2} = 2/3$，故出现 $\cos(2\pi n^2/3)$；系数恒等式 $(\sqrt{2}+\sqrt{1+\sqrt{5}/3})/\sqrt{1-\sqrt{5}/3} = (2\sqrt{3}+\sqrt{5}+1)/(\sqrt{5}-1) = 5.42055106563804$ 亦只对 $\sqrt{5}/3$ 成立（取 $\sqrt{5/3}$ 时左端为纯虚数）。600 DPI 像素测量确认印文根号横线止于“5”之后、“3”之前（横线 $x = 218$–$256$，“3”位于 $x = 270$–$291$），故印文本身为 $\sqrt{5}/3$，此处为转录时易误读之处，并非书中印误。倒数第二等式亦已数值验证（左端与右端均为 $0.903741287272173$，差 $4.9\times 10^{-31}$）。

**状态：** 已证明（书中给出证明）。**对照：** M07（theta 函数）、M06（模变换）、M02。

**我自验：** 取 $x = 1$、$y = 2$：(i) 差 $9.9\times 10^{-32}$，(ii) 差 $0$；推论取 $x = 0.5$：差 $9.9\times 10^{-32}$；(23.4) 差 $0$；(23.5) 按 $\sqrt{5}/3$ 计差 $0$（mpmath 30 位）。

## Entry 24

**陈述。**

**(i)** 几何作图：$\gamma = \angle TMM'$，$0 < \gamma < \pi$；$MM'$ 为一半圆的直径；$RP\perp MM'$；$MP$ 为另一半圆的直径；$Q$ 满足 $PQ = PM'$；$\delta = \angle QMP$；$S$ 为 $MM'$ 的中点。

**命题 1**（黄金分割）：若 $MP/PM' = (\sqrt{5}+1)/2$（(24.1)），则 $MQ$ 与 $MR$ 重合；证明用 (24.2) $MQ/MP = MP/MR$、(24.3) $MR/MM' = MP/MR$、(24.4) $MP^2-MP\cdot PM'-PM'^2 = 0$。

**命题 2**（摆）：若 $t_1$、$t_2$ 为摆通过角 $4\gamma$、$4\delta$ 的时间，则 $t_1 = (MM'/MP)t_2 =: mt_2$（(24.5)）；$t_1 = \pi\sqrt{MM'/g}\,{}_2F_1(\frac12,\frac12;1;\alpha)$，$\alpha = \sin^2\gamma$；$t_2 = \pi\sqrt{MM'/g}\,{}_2F_1(\frac12,\frac12;1;\beta)$，$\beta = \sin^2\delta$；(24.6) $t_1/t_2 = {}_2F_1(\frac12,\frac12;1;\alpha)/{}_2F_1(\frac12,\frac12;1;\beta)$；(24.7) $\beta = \sin^2\delta = (m-1)^2$；(24.8) $\alpha = \sin^2\gamma = 4(1/m-1/m^2)$；(24.9) $t_1/t_2 = {}_2F_1(\frac12,\frac12;1;4(m-1)/m^2)/{}_2F_1(\frac12,\frac12;1;(m-1)^2)$；Landen (24.10) ${}_2F_1(\frac12,\frac12;1;4z/(1+z)^2) = (1+z)\,{}_2F_1(\frac12,\frac12;1;z^2)$，取 $z = m-1$ 即得 $t_1/t_2 = m$。$m > 1$，且 $m < 2$。

**命题 3**：$\cos\gamma = 2PS/(m\cdot MP)$；拉马努金（笔记 p. 228）无意中漏写因子 $MP$（Berndt 注明）。

第 24 节 (i) 末注记：$\beta$ 为 $\alpha$ 的 2 次函数：(24.11) $m = (2-2\sqrt{1-\alpha})/\alpha$；(24.12) $\beta = ((2-2\sqrt{1-\alpha}-\alpha)/\alpha)^2 = (1-\sqrt{1-\alpha})^4/\alpha^2 = \alpha^2/(1+\sqrt{1-\alpha})^4$。故 (24.12) 为 2 次模方程。

**(ii)** 乘子 $m = {}_2F_1(\frac12,\frac12;1;\alpha)/{}_2F_1(\frac12,\frac12;1;\beta)$（(24.14)）；2 次模方程：(24.15) $m\sqrt{1-\alpha}+\sqrt{\beta} = 1$；(24.16) $m^2\sqrt{1-\alpha}+\beta = 1$；(24.17) $\frac12m^2 = (1+\sqrt{\beta})/(1+\sqrt{1-\alpha}) = (1+\beta)/(1+(1-\alpha))$。

**(iii)** 4 次模方程：(24.18) $\sqrt{m}(1-\alpha)^{1/4}+\beta^{1/4} = 1$；(24.19) $m(1-\alpha)^{1/4}+\sqrt{\beta} = 1$；(24.20) $\frac12m = (1+\beta^{1/4})/(1+(1-\alpha)^{1/4}) = (1+\sqrt{\beta})/(1+\sqrt{1-\alpha})$；(24.21) $\beta = ((1-\sqrt{1-\alpha})/(1+\sqrt{1-\alpha}))^2$（2 次关系重写）；(24.22) $\sqrt{\beta} = ((1-(1-\alpha)^{1/4})/(1+(1-\alpha)^{1/4}))^2$（由 (24.21) 迭代得：$\beta$ 换为 $\sqrt{\beta}$，$1-\alpha$ 换为 $\sqrt{1-\alpha}$）；(24.23) $m = 4/\{1+(1-\alpha)^{1/4}\}^2$。

**(iv)** 拉马努金断言 (24.24) $\sqrt{m}(1-\alpha)^{1/8}+\beta^{1/4} = 1$ 为 8 次模方程，且 $\frac12\sqrt{m} = (1+\beta^{1/4})/(1+(1-\alpha)^{1/4})$ 为 16 次模方程；Berndt 注明：计算表明 8 次与 16 次方程“不如所断言的那样简洁”，不予深究。

**(v)** 倒易（Fricke 对合）：$\alpha$ 换为 $1-\beta$，$\beta$ 换为 $1-\alpha$，$m$ 换为 $n/m$（$n$ 为次数），得同次数的模方程。例：(24.25) $(2/m)\sqrt{\beta}+\sqrt{1-\alpha} = 1$；$(1-\sqrt{1-\alpha})(1-\sqrt{\beta}) = 2\sqrt{\beta(1-\alpha)}$；4 次倒易 $(2/\sqrt{m})\beta^{1/4}+(1-\alpha)^{1/4} = 1$；$(1-(1-\alpha)^{1/4})(1-\beta^{1/4}) = 2(\beta(1-\alpha))^{1/4}$；若 (24.24) 成立，则 8 次倒易为 (24.26) $(2\sqrt{2}/\sqrt{m})\beta^{1/8}+(1-\alpha)^{1/4} = 1$。

**(vi)** (24.27) $n\,d\alpha/d\beta = \alpha(1-\alpha)/(\beta(1-\beta))\cdot m^2$（Jacobi）。

**第 24 节 (vii)。** “$\psi$ 函数的方程可化为 $\varphi$ 函数的方程，反之亦然，而 $f$ 与 $\chi$ 函数的方程保持不变”；例 (24.28) $\psi(q^{1/3})/(q^{1/3}\psi(q^3)) = 1+(\psi^4(q)/(q\psi^4(q^3))-1)^{1/3}$ 化为 (24.29) $\varphi(q^{1/3})/\varphi(q^3) = 1+(\varphi^4(q)/\varphi^4(q^3)-1)^{1/3}$；(24.30)(24.31) 用 $\vartheta_2/\vartheta_3$ 变换公式（Rademacher）；拉马努金在 Ch. 20 第 1 节重述 (24.28)(24.29)，证明留待该处；Berndt 不确定拉马努金的意图。

**状态：**(i) 命题 1–3 已证明（书中给出证明；命题 3 的 $MP$ 因子为 Berndt 补正）；(ii)(iii) 已证明（书中给出证明）；(iv) 的 8 次、16 次断言按原样不成立（Berndt 注明）；(v)(vi) 已证明（书中给出证明）；第 24 节 (vii) 为陈述，证明留待 Ch. 20 第 1 节。**对照：** M11（椭圆积分与模方程）、M06（模方程）、M07（$\vartheta$、$\varphi$ 函数）、M09（摆的椭圆积分）。

**我自验：** 取 $\alpha = 8/9$、$\beta = 1/4$（2 次）、$m = 3/2$：(24.14) 的 $m = 1.5$；(24.15) 左端 $1.0$，(24.16) 左端 $1.0$，(24.17) 三式均为 $1.125$。取 $\alpha = 8/9$（4 次）：$\beta = 0.00515477614287$，$m = 1.60769515459$；(24.18) 左端 $1.0$，(24.19) 左端 $1.0$，(24.20) 三式均为 $0.803847577293$；(24.14) 的 $m = 1.60769515459$，与 (24.23) 一致。(24.24) 左端 $1.23138223643 \ne 1$，与 Berndt 的否定一致。(24.27) 取 $\alpha = 0.5$、$\beta$ 由 (24.12) 得：差 $4.7\times 10^{-30}$（$d\alpha/d\beta$ 用数值微分）。(24.28) 差 $0$，(24.29) 差 $3.9\times 10^{-31}$（$q = 0.5$）（mpmath 30 位）。

## 小结

本章共 24 条编号 Entry（Entry 1–24，无缺号），分体、推论与例子标题 59 个，Entry 标题共 83 个；书页 143–219（77 页）。要点如下：

- Entry 1–2 以 $z$ 与 $L(e^{-2y})$ 表出 ${}_2F_1(-\frac12,-\frac12;1;x)$ 与 ${}_2F_1(-\frac12,\frac12;1;x)$，为椭圆周长的超几何准备。
- Entry 3 为椭圆周长：精确式 (3.1)(3.2)（Maclaurin、Ivory）与拉马努金近似 (3.3) nearly、(3.4) very nearly（误差分别约 $t^3/2^9$、$3t^5/2^{17}$；定理 1、定理 2；Villarino 的界）；例题给出 $\pi$、$\mathrm{Log}\,10$、$e^{-\pi}$、$e^{\pi/2}$ 的小数，推论给出 $355/113$ 与 $(97\frac12-1/11)^{1/4}$ 两 $\pi$ 近似及 $\pi^4$ 连分数。
- Entry 4–7 为 $\sinh$、$\cosh$ 级数求值：Entry 4 的对数比级数、Entry 5 的 $\mathrm{Log}(16/x)$、Entry 6 的 ${}_3F_2$、Entry 7 的 Catalan 常数与余模 ${}_3F_2$，第 7 节例题的 $\sinh$ 级数闭式。
- Entry 8–10 为 $\omega = e^{2\pi i/3}$ 的部分分式：Entry 8 的四个 $\theta$ 级数（Berndt 称前所未见于文献）、Entry 9–10 的 $(2n+1)^6-z^6$ 部分分式与乘积公式、第 10 节例 2 的 $\pi^7/23040$（致 Hardy 第一封信，Watson 首证）。
- Entry 11 为章首点名的最有趣恒等式：(i) 的 $\mathrm{dn}$ 恒等式 $= 2\Gamma^4(3/4)/\pi$；(ii) 为余模乘积。
- Entry 12–13 为 $\mathrm{dn}$、$\mathrm{cn}$、$\mathrm{cd}$、$\mathrm{sd}$、$\mathrm{sn}$ 的连分数（Stieltjes–Rogers）；第 12 节推论为算术–几何平均型恒等式 (12.3)（致 Hardy 第二封信，Preece 证明）；第 13 节推论的 $\mu$ 连分数按原样不成立（见下）。
- Entry 14–18 为 $\mathrm{sn}$、$\mathrm{cn}$、$\mathrm{dn}$ 的 Fourier 级数与参数变换：Entry 14 的 $S$、$C$、$C_1$ 关系与 (14.11) 的椭圆积分反演；Entry 15 的六条 $\theta$、$\varphi$ 级数（(vi) 的负号为拉马努金所漏，笔记 p. 222）；Entry 16 的换表与 (i)–(v)（(iii)–(v) 的证明工具在笔记中未出现）；Entry 17 的 $L(e^{-2y})$ 与第二类椭圆积分 $E$；Entry 18 的四种参数变换（(iii) 的 $\cot\varphi$ 错误，笔记 p. 223；（18.4) 的首因子 $1/2$ 应为 $1/z$，为本轮新发现的印文问题）。
- Entry 19 为椭圆弧与双曲弧（Legendre、Landen）及周长角 $\varphi$ 的 (iii)(iv)（(iv) 单调性为猜想）；推论 (ii) 的 (19.30) 为拉马努金的错误版本（计算错误），(19.29) 为中段误差数角分的粗近似。
- Entry 20 为化圆为方（$355/113$；推论 (i)(ii) 的 $(31)^{1/3}$ 与 $(97\frac12-1/11)^{1/4}$）与立方和参数解（(ii) $A^3+B^3 = C^2$，(iii) $A^3+B^3+C^3 = D^3$，含 1729；$1^3+6^3+8^3 = 9^3$ 在参数解范围之外）。
- Entry 21 为 $\omega$ 极点的部分分式 (i)–(iv)（(ii) 的 $\rho(n)$ 为分子 $/\sqrt{3}$、分母 $\sqrt{3}$ 的混合式；证明中 $g(x)$ 的系数 $2\pi$ 应为 $6\pi$）；第 21 节例题按原样不成立（左端 $0.00323859$，右端 $0.08229525$；证明中 $\psi$ 和 $S$ 漏减 $n = 0$ 项 $1/9$）；(21.8) 本身成立，(21.9) 的 $\psi$ 和注记收尾。
- Entry 22 为 $\mathrm{dn}$、$\mathrm{cn}$、$\mathrm{coam}$ 的 Laplace 变换连分数；(i)(ii) 在 $0 < x < 1$ 全程成立，(iii) 只在 $0 < x < 1/2$ 内成立（$x\ge 1/2$ 时连分数收敛到错误值）。
- Entry 23 为 theta 反演公式 (i)(ii) 及其推论；例题 (23.4)(23.5)（(23.5) 的指数为 $e^{-\pi\sqrt{5}/3}$，根号只盖 $5$）。
- Entry 24 为几何作图与模方程：命题 1（黄金分割）、命题 2（摆）、命题 3（$\cos\gamma$，$MP$ 因子为 Berndt 补正）；2 次模方程 (24.15)–(24.17)；4 次模方程 (24.18)–(24.23)（迭代法：$\beta$ 换为 $\sqrt{\beta}$，$1-\alpha$ 换为 $\sqrt{1-\alpha}$）；8 次、16 次断言不成立；倒易 (v) 与 (24.27)；第 24 节 (vii) 的 $\vartheta$、$\varphi$ 陈述留待 Ch. 20 第 1 节。

数值复核：约 120 项数值检查中，除下述五处已定位的问题外全部通过（mpmath 30 位，直接求和 + 解析尾项；截断级数余项量级与预期一致）。本轮发现的原书印文与范围问题共五处：(1) (18.4) 首因子 $1/2$ 应为 $1/z$（四点 30 位验证 + 书中下一句代数佐证）；(2) Entry 13(ii) 适用范围应为 $0 < x < 1/2$ 而非 $0 < x < 1/\sqrt{2}$，第 13 节推论按原样不成立（$n = 1$ 时连分数 $0.3188$，左端 $0.19402$）；(3) Entry 22(iii) 适用范围应为 $0 < x < 1/2$ 而非 $0 < x < 1$（$x = 1/2$ 时连分数约 $1.3078$，积分 $0.60050$）；(4) Entry 21(ii) 证明中 $g(x)$ 的系数 $2\pi$ 应为 $6\pi$（(21.7) 主部、(ii) 左端 $6\cosh$ 项与右端首项三处一致）；(5) 第 21 节例题按原样不成立（左端 $0.00323859$，右端 $0.08229525$；证明中 $\psi$ 和 $S$ 漏减 $n = 0$ 项 $1/9$ 为已定位的错误之一，余约 $0.0605$ 未解释）。另有转录注意一处：(23.5) 的指数为 $e^{-\pi\sqrt{5}/3}$（600 DPI 像素测量确认根号只盖 $5$），误读为 $e^{-\pi\sqrt{5/3}}$ 时差 $0.62646$。拉马努金原文疏失五处已按 Berndt 注明：Entry 15(vi) 漏负号（笔记 p. 222）、Entry 18(iii) 的 $\cot\varphi$ 错误（笔记 p. 223）、推论 (ii) 的 (19.30) 计算错误、第 21 节例题的两处数值错误（$25/756$、$-\pi/(54\sqrt{3})$，笔记 p. 226）、命题 3 漏因子 $MP$（笔记 p. 228）；Entry 21(ii) 的笔记表述不正确（笔记 p. 226）、Entry 24(iv) 的 8 次、16 次断言不正确（Berndt 注明）、Entry 19(iv) 的单调性为猜想。

## 待核对清单

- IMSC 本章结果数：imsc.res.in 2026-11-08 再次不可达（curl 返回 000），未能补录。
- Berndt 章首计数：本章导言（p. 143）未给出本章公式或定理陈述的总数。
- (18.4) 的首因子：书中印为 $1/2$，数值复核（四点 30 位）与书中下一句代数均表明应为 $1/z$；待查 Berndt 勘误。
- Entry 13(ii) 的适用范围：书中称 $0 < x < 1/\sqrt{2}$，证明的 Perron 条件 $k/k' < 1$ 与数值复核均表明应为 $0 < x < 1/2$；第 13 节推论（取 $x = 1/2$）按原样不成立，待查 Berndt 勘误与文献。
- Entry 22(iii) 的适用范围：书中称 $0 < x < 1$，数值复核表明应为 $0 < x < 1/2$（$x\ge 1/2$ 时连分数收敛到错误值）；待查 Berndt 勘误与文献。
- Entry 21(ii) 证明中 $g(x)$ 的系数：书中印为 $2\pi$，(21.7) 主部、(ii) 左端 $6\cosh$ 项与右端首项三处一致表明应为 $6\pi$；待查 Berndt 勘误。
- 第 21 节例题：按原样不成立（左端 $0.00323859$，右端 $0.08229525$）；证明中 $\psi$ 和 $S$ 漏减 $n = 0$ 项 $1/9$ 为已定位的错误之一，余约 $0.0605$ 未解释；例题的正确闭式需重新推导（经 $B(3)-B(3/2)/4$ 的验算，左端值 $0.00323859$ 无误）。
- Entry 24(iv) 的 8 次、16 次模方程断言：Berndt 注明计算表明不如所断言的那样简洁，不予深究；(24.24) 左端在 $\alpha = 8/9$ 处为 $1.23138223643 \ne 1$，与 Berndt 的否定一致。
- Entry 19(iv) 的 $\varphi$ 单调性：书中明言仅为猜想，未证明。
- 第 24 节 (vii)：Berndt 不确定拉马努金的意图，证明留待 Ch. 20 第 1 节；本章未展开。
- Entry 13(ii) 在 $x\to 1/2^-$ 时连分数收敛极慢（$x = 0.499$ 处 Lentz 算法与左端一致，$x = 0.4999$ 处后向递推 $N = 2000$ 尚未收敛）；端点 $x = 1/2$ 的连分数极限约 $0.63754$（正向渐近分数与 Lentz 算法一致），其闭式未求。
- Entry 22(iii) 在 $x = 1/2$ 处连分数极限约 $1.3078$（$n = 1$），其闭式未求。
- TIFR 1957 年影印版的笔记页码：Berndt 在本章引用的笔记页码为 p. 217（Entry 3 的 nearly/very nearly）、p. 222（Entry 15(vi) 漏负号）、p. 223（Entry 18(iii) 错误）、p. 225（第 20 节推论 (ii)）、p. 226（Entry 21(ii) 表述不正确、例题两处数值错误）、p. 228（命题 3 漏因子）；其余 Entry 的 TIFR 页码未逐条核对。
- 本章条目总数未见于其他目录核对；以书中编号 Entry 1–24 为准。

## 来源说明

- 整理层：Bruce C. Berndt，《Ramanujan's Notebooks》，Part III，Springer，1991，Ch. 18，书页 143–219（正文）；参考文献自书页 489 起，索引自书页 505 起。
- 电子版：archive.org 标识符 `ramanujan_notebooks_iii`（《Ramanujan's Notebooks, Part 3》，Springer 1991，XIII + 510 页，DOI **10.1007/978-1-4612-0965-2**；PDF 21,002,730 字节、524 叶，md5 `de9211b0bde03dd9255145d3f09bb78f`），**PDF 页 = 书页 + 14**（与 Part II 的 +12 不同）。本章为 PDF 页 157–233（书页 143–219）；PDF 页 234 起为 Ch. 19（书页 220）。
- 转录方法：全部公式按 PDF 原图（150 DPI，书页 143–219）逐字转录；关键公式另用 300 DPI 放大图确认：p. 199 例题表（PDF 页 213）、(18.4)（PDF 页 193）、第 13 节收敛句（PDF 页 180）、$\rho(n)$ 定义（PDF 页 214）、第 21 节例题（PDF 页 219）；(23.5) 的根号范围另用 600 DPI 像素测量确认；OCR（DjVu 文本层）只作检索索引，公式凡与原图或数值不符者一律纠正。
- 数值复核：mpmath 30 位，直接求和 + 解析尾项（$\zeta$ 尾项、Lentz 连分数算法、后向递推）；约 120 项检查中除待核对清单所列五处问题外全部通过（详见各 Entry 的“我自验”）；慢收敛连分数（Entry 13(i)(ii)、Entry 22(iii) 在边界附近）另用正向渐近分数、Lentz 算法与积分表示三重验证。
- 章名与目录：以原书目录为准，Ch. 18 为 "The Jacobian Elliptic Functions"；下一章 Ch. 19 为 "Modular Equations of Degrees 3, 5, and 7 and Associated Theta-Function Identities"（书页 220 起）。
- 参考文献（书中引用，本章出现者）：Bailey [4]、Byrd–Friedman [1]、Cayley [1]、Dickson [1]、Erdélyi [1]、Fergestad [1]、Frenicle [1]、Gradshteyn–Ryzhik [1]、Hancock [1]、Hansen [1]、Hoppe [1]、Ivory [1]、Jacobsen–Waadeland [1]、Landen [1]、Legendre [1]、Maclaurin [1]、Moreau [1]、Preece [1]、Rademacher [1]、Villarino [1]、Wallis [1]、Watson [1]、Whittaker–Watson [1]、Berndt [3]、[9]、[11]。
