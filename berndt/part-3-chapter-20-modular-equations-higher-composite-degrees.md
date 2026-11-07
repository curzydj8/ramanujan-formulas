# Part III，Chapter 20——Modular Equations of Higher and Composite Degrees（高次与合数次模方程）

出处：Bruce C. Berndt，《Ramanujan's Notebooks》，Part III，Springer，1991，Ch. 20，书页 325–453。

本章是 Part III 的第五章、Berndt 五卷的第 20 章：拉马努金在此给出 11、13、17、19、23、31、47、71 次等高次模方程，以及 15、21、27、33、35、39、55、63、87、95、119、135、143、175、207、231、247、255 次等合数次（“混合”）模方程——Berndt 在章末写道：“This concludes a truly fascinating chapter!”本章共 **24 条编号 Entry（Entry 1–24，无缺号）**，另含引言定理 0.9、(7.1)、Evans 定理 8.1 等附带公式，共 129 个分体标题（见“本章结构”表后的计数说明）。

## 背景与记号

- 全章默认 $|q| < 1$。拉马努金常把级数的前几项显式写出而不写紧凑的求和记号；下文照录其显式前几项，并在说明中给出一般项的规律。
- theta 函数（Ch. 16 Entry 22）：$\varphi(q) := f(q,q) = \sum_{n=-\infty}^{\infty}q^{n^2}$，$\psi(q) := f(q,q^3) = \sum_{n=0}^{\infty}q^{n(n+1)/2}$，$f(a,b) := \sum_{n=-\infty}^{\infty}a^{n(n+1)/2}b^{n(n-1)/2}$，$f(-q) := f(-q,-q^2) = (q;q)_{\infty}$，$\chi(q) := (-q;q^2)_{\infty}$。另有一单变量记号 $f(q)$：书中 $f(q)$ 指 $f(q,-q^2)$，即 $f(q) = (-q;q^2)_{\infty}(q^2;q^2)_{\infty} = \prod_{n\ge 1}(1-(-q)^n)$；本章 Entry 17(iii)(iv) 与 Entry 19(i) 的 $f(q^3)$、$f(q^9)$、$f(q^{15})$、$f(q^{21})$、$f(q^{45})$ 皆按此义理解（本轮数值复核确认：Entry 19(i) 按此读法在 $q = 0.5$、$0.3$ 处差 $\le 5.9\times 10^{-31}$；按 $(q^3;q^3)_{\infty}$ 或 $f(q^3,q^{21})$ 读法皆不成立，见 Entry 19 说明）。
- 模与乘子（Ch. 17 第 6 节、Ch. 18 Entry 24、Ch. 19 Entry 5）：$z_1 = {}_2F_1(\frac12,\frac12;1;\alpha)$，$z_n = {}_2F_1(\frac12,\frac12;1;\beta)$；$\varphi(q) = \varphi(e^{-y}) = z_1^{1/2}$，$\varphi(q^n) = z_n^{1/2}$；乘子 $m$ 由 $z_1 = m\cdot z_n$ 定义。$\alpha$、$\beta$ 为两模，$\beta$ 称为 $\alpha$ 的 $n$ 次模。本章多用四个模 $\alpha$、$\beta$、$\gamma$、$\delta$（次数依次为 $1$、$n_1$、$n_2$、$n_3 = n_1n_2$），$m$ 为 $\alpha$–$\beta$ 间的乘子，$m'$（或 $m''$）为另一对模间的乘子，各条开头均有说明。
- “正函数”（positive function）：指对充分小的正 $q$ 取正值的函数；其分数次方根皆取正实根。
- 本章与已填章节的互见：Ch. 16 的 theta 函数（Entry 22 的 $\varphi$、$\psi$、$f$、$\chi$ 定义，Entry 24 的 $f^3(-q^{1/3})$ 级数表示，Entry 19 的 Jacobi 三重积，Entry 18(iv)、Entry 30、31、33）是全章的工具；Ch. 17 的椭圆函数（第 6 节的 $z$、Entry 7 的加法定理、Entry 10–12 的 $L$、$M$、$N$）是 Entry 3、5、11 的证明工具；Ch. 18 的模方程定义（Entry 24）与 2、4 次模方程、Ch. 19 的 3、5、7 次模方程与定理 12.1 是本章的先行——本章 Entry 6(iii)、Entry 8(i)、Entry 12(i) 即定理 12.1 在 $n = 11$、$13$、$17$ 的情形；Ch. 19 Entry 12 的 (12.32) 亦在本章多处引用。
- 与主题模块的对照总览：模方程与模形式主线见 **M06**（全章；Entry 3、5、7、11、13–16、18–24 的高次与合数次模方程与乘子公式，引言的模形式理论与赋值公式）；q 级数与 theta 函数见 **M07**（Entry 1、2、4、6、8–10、12、17 的 theta 恒等式）；无穷级数见 **M02**（Entry 1(v)、Entry 10(v)(vi) 的 Lambert 级数与系数周期）；连分数见 **M03**（Entry 1(i) 与 (1.3) 的连分数）；椭圆函数见 **M11**（Entry 3、5、11 的椭圆函数翻译与参数化）；超几何函数见 **M10**（$z_n = {}_2F_1(\frac12,\frac12;1;\cdot)$）；代数方程见 **M14**（Entry 3、5 的 $q$、$u$ 参数化，Entry 7、15、16、23 的多项式关系）；Eisenstein 级数见 **M01**（引言的 $\eta$ 函数与模形式；下一章 Ch. 21 的主题）。

## 引言（第 0 节，书页 325–344）

本章开篇先给出“混合”模方程的定义：设 $\alpha$、$\beta$、$\gamma$、$\delta$ 的次数依次为 $1$、$n_1$、$n_2$、$n_3 = n_1n_2$，$K'/K$ 的比值相应为 $n_1$、$n_2$、$n_3$（式 (0.1)）；$m = z_1/z_{n_1}$，$m' = z_{n_1}/z_{n_3}$。拉马努金在第二本笔记中共记录了二十组次数三元组 $\{n_1,n_2,n_3\}$ 的混合模方程：$\{3,5,15\}$、$\{3,7,21\}$、$\{3,9,27\}$、$\{3,11,33\}$、$\{3,13,39\}$、$\{3,21,63\}$、$\{3,29,87\}$、$\{5,7,35\}$、$\{5,11,55\}$、$\{5,19,95\}$、$\{5,27,135\}$、$\{7,9,63\}$、$\{7,17,119\}$、$\{7,25,175\}$、$\{9,15,135\}$、$\{9,23,207\}$、$\{11,13,143\}$、$\{11,21,231\}$、$\{13,19,247\}$、$\{15,17,255\}$。其中 $\{3,5,15\}$ 的两条方程曾由 Hardy（文献 [1]，p. 220）无证明地记录；除此之外，在 Berndt–Biagioli–Purtilo 的三篇论文 [1]–[3] 之前，混合模方程未见于任何已发表文献。

引言随后系统介绍证明本章结果所需的模形式理论（式 (0.1)–(0.87)）：上半平面、stroke 算子、$\Gamma(1)$ 及其子群 $\Gamma(2)$、$\Gamma_0(n)$、$\Gamma'$、$\Gamma''$、赋值公式 (0.5)、乘子系统、Dedekind $\eta$ 函数、函数 $g_j$、$h_j$、$f_j$、尖点阶表（表 1）、引理 0.1–0.3、$G(m;z)$（式 (0.50)）、定理 0.4、推论 0.5–0.7，以及定理 0.8（即 Ch. 19 的 (18.2)，$p = 7$ 的情形）。其中最重要的是 **定理 0.9**（Evans 对 Ch. 19 定理 12.1 的推广）：对奇数 $p > 1$，

$$\sum_{m\bmod p}G(m;z) = 2\left(\frac{3}{p}\right)\eta(z/p^2)/\eta(z),$$

其中 $\left(\frac{3}{p}\right)$ 为 Legendre 符号。本章各 Entry 的证明大都归结为：把模方程翻译成 theta 恒等式或模形式恒等式，再用赋值公式与计算机代数系统 MACSYMA 验证有限个 $q$ 展开系数（各条说明中注明验证到的 $q$ 幂次）。

## 本章结构

| Entry | 主题 | 书页 |
|---|---|---|
| Entry 1 | $\psi/\varphi$ 与 $v$ 的 3 次连分数公式 (i)–(v)；(1.3) | 344–348 |
| Entry 2 | 9 次 theta 恒等式 (i)–(ix) | 348–351 |
| Entry 3 | 3、9 次模方程 (i)–(xvi) | 352–358 |
| Entry 4 | 9、27 次 theta 恒等式 (i)–(iv) | 358–360 |
| Entry 5 | 3、9、27 次模方程 (i)–(iv) | 360–362 |
| Entry 6 | 11 次 theta 恒等式 (i)–(iii) | 362–363 |
| Entry 7 | 11 次模方程 (i)–(vii)；(7.1) | 363–371 |
| Entry 8 | 13 次 theta 恒等式与模方程 (i)–(iv)；(8.1)–(8.5) | 371–376 |
| Entry 9 | 15 次 theta 恒等式 (i)–(vii) | 376–378 |
| Entry 10 | 15 次 theta 恒等式 (i)–(vi)；系数周期 30、60 | 378–382 |
| Entry 11 | 3、5、15 次模方程 (i)–(xv) | 382–396 |
| Entry 12 | 17 次 theta 恒等式与模方程 (i)–(iv)；(12.1)–(12.3) | 396–400 |
| Entry 13 | 3、7、21 次模方程 (i)–(vi) | 400–408 |
| Entry 14 | 3、11、33 次模方程 (i)(ii) | 408–410 |
| Entry 15 | 23 次模方程 (i)–(iii)；(iii) 为 Berndt 的订正 | 410–416 |
| Entry 16 | 19 次模方程 (i)(ii) | 416–417 |
| Entry 17 | 35、135 次 theta 恒等式 (i)–(iv) | 416–422 |
| Entry 18 | 5、7、35 次模方程 (i)–(vii) | 422–426 |
| Entry 19 | 63 次 theta 恒等式 (i)(ii)；3、13、39 等模方程 (iii)(iv) | 426–430 |
| Entry 20 | 63、95、119、135、143 次模方程 (i)(ii) | 430–434 |
| Entry 21 | 7、15 次与 39、55、63 次模方程 (i)(ii) | 434–438 |
| Entry 22 | 31 次模方程 (i)–(iii)；$\Omega$ 函数 | 438–444 |
| Entry 23 | 47、71 次模方程 (i)(ii)；本章两模方程的高潮 | 444–448 |
| Entry 24 | 87、135、143、175、207、231、247、255 次模方程 (i)(ii) | 448–453 |

计数说明：编号 Entry 1–24 共 24 条，无缺号。分体标题 129 个：Entry 1(i)–(v) 5、Entry 2(i)–(ix) 9、Entry 3(i)–(xvi) 16、Entry 4(i)–(iv) 4、Entry 5(i)–(iv) 4、Entry 6(i)–(iii) 3、Entry 7(i)–(vii) 7、Entry 8(i) 的 (8.1)–(8.5) 5 与 (ii)(iii)(iv) 3 共 8、Entry 9(i)–(vii) 7、Entry 10(i)–(vi) 6、Entry 11(i)–(xv) 15、Entry 12(i) 的 (12.1)–(12.3) 3 与 (ii)(iii)(iv) 3 共 6、Entry 13(i)–(vi) 6、Entry 14(i)(ii) 2、Entry 15(i)–(iii) 3、Entry 16(i)(ii) 2、Entry 17(i)–(iv) 4、Entry 18(i)–(vii) 7、Entry 19(i)–(iv) 4、Entry 20(i)(ii) 2、Entry 21(i)(ii) 2、Entry 22(i)–(iii) 3、Entry 23(i)(ii) 2、Entry 24(i)(ii) 2。另有引言的定理 0.9、(7.1)、Evans 定理 8.1 与各节编号公式，均已按其所属 Entry 收录。Entry 7 的 (viii)(ix) 在笔记中已被拉马努金本人划去，不计入陈述。

## Entry 1

**陈述。** $\varphi$、$\psi$、$\chi$、$f$ 如 Ch. 16 Entry 22。置

$$v := q^{1/3}\chi(-q)/\chi^3(-q^3).$$

则

**(i)**

$$v = q^{1/3}/(1 + (q+q^2)/(1 + (q^2+q^4)/(1 + \cdots))),$$

$$1 + 1/v = \psi(q^{1/3})/(q^{1/3}\psi(q^3)),$$

$$1 + 1/v^3 = \psi^4(q)/(q\psi^4(q^3)).$$

**(ii)**

$$1 + \psi(-q^{1/3})/(q^{1/3}\psi(-q^3)) = (1 + \psi^4(-q)/(q\psi^4(-q^3)))^{1/3},$$

$$2v = 1 - \varphi(-q^{1/3})/\varphi(-q^3),$$

$$1 + 3q\psi(-q^9)/\psi(-q) = (1 + 9q\psi^4(-q^3)/\psi^4(-q))^{1/3}.$$

**(iii)**

$$\varphi(q^{1/3})/\varphi(q^3) = 1 + (\varphi^4(q)/\varphi^4(q^3) - 1)^{1/3},$$

$$3\varphi(q^9)/\varphi(q) = 1 + (9\varphi^4(q^3)/\varphi^4(q) - 1)^{1/3},$$

$$\cos 40^{\circ} + \cos 80^{\circ} = \cos 20^{\circ},$$

$$1/\cos 40^{\circ} + 1/\cos 80^{\circ} = 1/\cos 20^{\circ} + 6.$$

**(iv)**

$$3 + f^3(-q^{1/3})/(q^{1/3}f^3(-q^3)) = (27 + f^{12}(-q)/(qf^{12}(-q^3)))^{1/3} = 1/v + 4v^2,$$

$$1 + 9qf^3(-q^9)/f^3(-q) = (1 + 27qf^{12}(-q^3)/f^{12}(-q))^{1/3}.$$

**(v)**

$$f^3(-q^{1/3}) + 3q^{1/3}f^3(-q^3) = f(-q)\left\{1 + 6\sum_{n\ge 0}\left(q^{3n+1}/(1-q^{3n+1}) - q^{3n+2}/(1-q^{3n+2})\right)\right\}.$$

另有连分数

$$(1.3)\quad f(-q,-q^5)/f(-q^3,-q^3) = 1/(1 + (q+q^2)/(1 + (q^2+q^4)/(1 + \cdots))).$$

**说明。**(i) 的第一式由拉马努金在致 Hardy 的第二封信中给出（文献 [10]，p. xxviii）；(1.3) 亦见于第三本笔记（文献 [9]，p. 373）。(i) 的连分数在书中排成平铺写法，按连分数读法记录（见 Ch. 19 Entry 1 的转录注意，为同一排版惯例）。Watson [4] 证明了该连分数等于 $q^{1/3}\psi(q^3)/f(q,q^2)$。(ii) 与 (iii) 的第一等式分别是 Ch. 18 的 (24.28) 与 (24.29)；(iii) 的两条三角恒等式在书中未与本条其余公式建立联系。Biagioli [2] 与 J. M. Borwein、P. B. Borwein [2，pp. 142–144] 证明了 (i)–(v)。

**状态：** 已证明（书中给出证明；(i) 的第一式为拉马努金致 Hardy 第二封信的内容）。**对照：** M07（theta 函数）、M03（连分数）、M02。

**我自验：** 取 $q = 0.5$、$0.3$（mpmath 30 位，直接求和）：(i) 连分数读法差 $\le 4.9\times 10^{-32}$，$1+1/v$ 与 $1+1/v^3$ 差 $\le 3.2\times 10^{-30}$；(ii) 三式差 $0$；(iii) 两式差 $\le 3.9\times 10^{-31}$，两三角恒等式精确成立；(iv) 两式差 $\le 1.7\times 10^{-15}$（$q = 0.5$，$q$-Pochhammer 在 $q^{1/3}$ 处的截断尾项量级；$q = 0.3$ 时差 $6.0\times 10^{-19}$）；(v) 差 $\le 8.3\times 10^{-16}$（同上原因；$q = 0.3$ 时差 $3.7\times 10^{-19}$）；(1.3) 差 $0$。

## Entry 2

**陈述。** $\varphi$、$\psi$、$f$、$\chi$ 如 Ch. 16 Entry 22。则

**(i)** $\varphi(q)\varphi(q^9) - \varphi^2(q^3) = 2q\varphi(-q^2)\psi(q^9)\chi(q^3).$

**(ii)** $\psi(q) - 3q\psi(q^9) = \varphi(-q)/\chi(-q^3).$

**(iii)** $\varphi(q)\varphi(q^9) + \varphi^2(q^3) = 2\psi(q)\varphi(-q^{18})\chi(q^3).$

**(iv)** $\psi(q^{1/9}) - q^{1/9}\psi(q) = f(q^4,q^5) + q^{1/3}f(q^2,q^7) + q^{2/3}f(q,q^8).$

**(v)** $f(-q^{1/3}) = f(-q^4,-q^5) - q^{1/3}f(-q^2,-q^7) - q^{2/3}f(-q,-q^8).$

**(vi)** $f(-q,-q^8)f(-q^2,-q^7)f(-q^4,-q^5) = f(-q)f^3(-q^9)/f(-q^3).$

**(vii)** $f(-q^4,-q^5)/f(-q^2,-q^7) + qf(-q,-q^8)/f(-q^4,-q^5) = f(-q^2,-q^7)/f(-q,-q^8).$

**(viii)** $f(-q^4,-q^5)/f(-q,-q^8) + qf(-q^2,-q^7)/f(-q^4,-q^5) = qf(-q,-q^8)/f(-q^2,-q^7) + f^4(-q^3)/(f(-q)f^3(-q^9)).$

**(ix)** $\varphi(q^{1/9}) - \varphi(q) = 2q^{1/9}f(q^7,q^{11}) + 2q^{4/9}f(q^5,q^{13}) + 2q^{16/9}f(q,q^{17}).$

**说明。** (i)–(iii) 的证明用 Ch. 16 Entry 30 与第 31 节的恒等式；(iv)(ix) 由 Ch. 19 定理 12.1 的方法得到；(v) 由 Ch. 16 Entry 24(ii) 的 $f^3(-q^{1/3})$ 级数按模 3 余数分组得到，(vi) 由 (v) 与 Ch. 16 Entry 22(iii) 的乘积表示得到，(vii)(viii) 由 (v) 立方后比较 $q^{1/3}$、$q^{2/3}$ 的系数并利用 (vi) 得到。Entry 2 与 Entry 3 之间另有一条 Evans [1，定理 7.2] 的恒等式：

$$G_1(z)G_2^2(z) + G_2(z)G_4^2(z) + G_4(z)G_1^2(z) = 6 - \eta(z/3)\{3\eta^3(z/3) + \eta^3(z/27)\}/(\eta(z/9)\eta^3(z)),$$

其中 $G_j$ 为引言的函数 $G(m;z)$ 在特定参数处的值。

**状态：** 已证明（书中给出证明）。**对照：** M07（theta 函数）、M02。

**我自验：** 取 $q = 0.5$、$0.3$（mpmath 30 位，直接求和）：(i)–(vii)、(ix) 差 $\le 2.7\times 10^{-28}$（(v) 在 $q = 0.5$ 处差 $1.5\times 10^{-11}$，为 $f(-q^{1/3})$ 的 $q$-Pochhammer 截断尾项量级；$q = 0.3$ 时差 $2.8\times 10^{-17}$）；(viii) 差 $0$。

**转录注意（Entry 2(viii) 第一项分母）。** (viii) 第一项的分母在 150 DPI 原图上易误读为 $f(-q^2,-q^8)$，300 DPI 放大图（PDF 页 363）确认确为 $f(-q,-q^8)$；按 $f(-q^2,-q^8)$ 计，$q = 0.5$ 时差 $0.61$、$q = 0.3$ 时差 $0.33$，不成立。证明中由 (v) 立方所得的等式 $A^2B + B^2Cq - AC^2q = f^3(-q^3)$（其中 $A = f(-q^4,-q^5)$、$B = f(-q^2,-q^7)$、$C = f(-q,-q^8)$）除以 $ABC$ 并利用 (vi) 亦得 $f(-q,-q^8)$ 的分母，与放大图一致。

## Entry 3

**陈述。** 设 $\alpha$、$\beta$、$\gamma$ 的次数依次为 $1$、$3$、$9$，$m = z_1/z_3$，$m' = z_3/z_9$。则

**(i)** $1 + 4^{1/3}(\alpha^3(1-\alpha)^3/(\beta(1-\beta)))^{1/24} = 3/\sqrt{mm'}.$

**(ii)** $1 + 4^{1/3}(\gamma^3(1-\gamma)^3/(\beta(1-\beta)))^{1/24} = \sqrt{mm'}.$

**(iii)** $1 - 2^{4/3}(\alpha^3\gamma^3(1-\alpha)^3(1-\gamma)^3/(\beta^2(1-\beta)^2))^{1/24} = m'/m.$

**(iv)** $1 - 4^{1/3}(\gamma^3(1-\alpha)^3/(\beta(1-\beta)))^{1/24} = \sqrt{m'/m} = 4^{1/3}(\alpha^3(1-\gamma)^3/(\beta(1-\beta)))^{1/24} - 1.$

**(v)** $(\alpha\gamma)^{1/2} + \{(1-\alpha)(1-\gamma)\}^{1/2} + 2\{4\beta(1-\beta)\}^{1/3} = 1 + 8\{\beta(1-\beta)\}^{1/4}\{\alpha\gamma(1-\alpha)(1-\gamma)\}^{1/8}.$

**(vi)** $\{\alpha(1-\gamma)\}^{1/8} + \{\gamma(1-\alpha)\}^{1/8} = 2^{1/3}\{\beta(1-\beta)\}^{1/24}.$

**(vii)** $[((1-\beta)^3/(1-\alpha))^{1/4} - 1]/[1 - \{(1-\alpha)(1-\beta)\}^{1/4}] = m = [1 - (\beta^3/\alpha)^{1/4}]/[1 - (\alpha\beta)^{1/4}].$

**(viii)** $1 + (\beta^3(1-\beta)^3/(\alpha(1-\alpha)))^{1/8} = m(\frac12\{1 + (\alpha\beta)^{1/2} + \{(1-\alpha)(1-\beta)\}^{1/2}\})^{1/2}.$

**(ix)** $1 + (\alpha^3(1-\alpha)^3/(\beta(1-\beta)))^{1/8} = (3/m)(\frac12\{1 + (\alpha\beta)^{1/2} + \{(1-\alpha)(1-\beta)\}^{1/2}\})^{1/2}.$

**(x)** $(\gamma/\alpha)^{1/8} + ((1-\gamma)/(1-\alpha))^{1/8} - (\gamma(1-\gamma)/(\alpha(1-\alpha)))^{1/8} = \sqrt{mm'}.$

**(xi)** $(\alpha/\gamma)^{1/8} + ((1-\alpha)/(1-\gamma))^{1/8} - (\alpha(1-\alpha)/(\gamma(1-\gamma)))^{1/8} = 3/\sqrt{mm'}.$

**(xii)** $(\beta^2/(\alpha\gamma))^{1/4} + ((1-\beta)^2/((1-\alpha)(1-\gamma)))^{1/4} - (\beta^2(1-\beta)^2/(\alpha(1-\alpha)(1-\gamma)))^{1/4} = -3m/m'.$

**(xiii)** $(\alpha\gamma/\beta^2)^{1/4} + ((1-\alpha)(1-\gamma)/(1-\beta)^2)^{1/4} - (\alpha\gamma(1-\alpha)(1-\gamma)/(\beta^2(1-\beta)^2))^{1/4} = m'/m.$

**(xiv)** $2^{1/3}\{\beta(1-\beta)\}^{1/24}/[\{\alpha(1-\gamma)\}^{1/8} - \{\gamma(1-\alpha)\}^{1/8}] = \sqrt{m/m'}.$

**(xv)** $(\alpha^{1/4} - \gamma^{1/4})^4 + \{(1-\gamma)^{1/4} - (1-\alpha)^{1/4}\}^4 = (\{\alpha(1-\gamma)\}^{1/4} - \{\gamma(1-\alpha)\}^{1/4})^4.$

**(xvi)** $1 = (\alpha\gamma)^{1/2} + \{(1-\alpha)(1-\gamma)\}^{1/2} + 2\{4\beta(1-\beta)\}^{1/3}m'/m.$

**说明。**(vii)–(ix) 本身是 3 次模方程，Berndt 注明其在本节中的位置未必自然。证明用参数化：(3.1) $m = \sqrt{1+4q}$，(3.2) $\alpha(1-\alpha) = q((2-q)/(1+4q))^3$，$\beta(1-\beta) = q^3(2-q)/(1+4q)$，以及 (3.3)–(3.5)；关键一步是关于 $q$ 的三次方程。

**状态：** 已证明（书中给出证明）。**对照：** M06（模方程）、M11、M14（$q$ 参数化）。

**我自验：** 取 $q = 0.5$、$0.2$，$\alpha$、$\beta$、$\gamma$ 由 $\alpha(q) = (\theta_2/\theta_3)^4$（$\theta_2 = 2q^{1/4}\psi(q^2)$、$\theta_3 = \varphi(q)$）、$\beta = \alpha(q^3)$、$\gamma = \alpha(q^9)$ 取，$m = \varphi^2(q)/\varphi^2(q^3)$、$m' = \varphi^2(q^3)/\varphi^2(q^9)$（mpmath 30 位，直接求和；下文各模方程条目皆用同一 theta 路线复核，不再重复说明）：(i)–(xvi) 全部通过，差 $\le 2.8\times 10^{-26}$。

## Entry 4

**陈述。** $\varphi$、$\psi$、$f$ 如 Ch. 16 Entry 22。则

**(i)** $\varphi(-q^{18})/\varphi(-q^2) + q(\psi(q^9)/\psi(q) - \psi(-q^9)/\psi(-q)) = 1.$

**(ii)** $\varphi(-q^2)/\varphi(-q^{18}) + (1/q)(\psi(q)/\psi(q^9) - \psi(-q)/\psi(-q^9)) = 3.$

**(iii)** $\varphi(-q^2)\varphi(-q^{54})/(\varphi(-q^6)\varphi(-q^{18})) + q^2(\psi(q)\psi(q^{27})/(\psi(q^3)\psi(q^9)) + \psi(-q)\psi(-q^{27})/(\psi(-q^3)\psi(-q^9))) = 1.$

**(iv)** $\varphi(q)\varphi(q^{27}) - \varphi(-q)\varphi(-q^{27}) = 4qf(-q^6)f(-q^{18}) + 4q^7\psi(q^2)\psi(q^{54}).$

**说明。**(i)(ii) 是 Entry 3(x)、(xi) 的转录（把 (x)、(xi) 的模翻译成 $\varphi$、$\psi$ 即得）；(iv) 的证明用 (4.1)（Ch. 16 Entry 18(iv) 的应用）与 Ch. 17 Entry 10(iii)、11(i)(ii)、12(iii)。

**状态：** 已证明（书中给出证明；(i)(ii) 为 Entry 3(x)(xi) 的转录）。**对照：** M07（theta 函数）、M06。

**我自验：** 取 $q = 0.5$、$0.3$（mpmath 30 位，直接求和）：(i)–(iv) 差 $\le 2.0\times 10^{-31}$。

## Entry 5

**陈述。** 设 $\alpha$、$\beta$、$\gamma$、$\delta$ 的次数依次为 $1$、$3$、$9$、$27$，$m$ 为 $\alpha$–$\beta$ 间的乘子，$m''$ 为 $\gamma$–$\delta$ 间的乘子。则

**(i)** $(\alpha\delta/(\beta\gamma))^{1/8} + ((1-\alpha)(1-\delta)/((1-\beta)(1-\gamma)))^{1/8} + (\alpha\delta(1-\alpha)(1-\delta)/(\beta\gamma(1-\beta)(1-\gamma)))^{1/8} = \sqrt{m''/m}.$

**(ii)** $(\beta\gamma/(\alpha\delta))^{1/4} + ((1-\beta)(1-\gamma)/((1-\alpha)(1-\delta)))^{1/4} + (\beta\gamma(1-\beta)(1-\gamma)/(\alpha\delta(1-\alpha)(1-\delta)))^{1/4} - 2(\beta\gamma(1-\beta)(1-\gamma)/(\alpha\delta(1-\alpha)(1-\delta)))^{1/8}\{1 + (\beta\gamma/(\alpha\delta))^{1/8} + ((1-\beta)(1-\gamma)/((1-\alpha)(1-\delta)))^{1/8}\} = -3m/m''.$

**(iii)** $[1 - (\alpha\delta)^{1/4} - \{(1-\alpha)(1-\delta)\}^{1/4}]/[2\{16\beta\gamma(1-\beta)(1-\gamma)\}^{1/12}] = \sqrt{m''/m}.$

**(iv)** $[\{16\beta\gamma(1-\beta)(1-\gamma)\}^{1/24} + \{16\alpha\delta(1-\alpha)(1-\delta)\}^{1/8}]/[\{16\beta\gamma(1-\beta)(1-\gamma)\}^{1/24} + \{16\beta\gamma(1-\beta)(1-\gamma)\}^{1/8}] = \sqrt{m''/m}.$

**说明。** 证明用参数化：(5.1) $m'' = 1 + 8u^3$；(5.2) $\beta(1-\beta) = 16u((1-u)/(1+2u))^8(1-u^3)/(1+8u^3)$；(5.3) $\gamma(1-\gamma) = 16u^3((1-u^3)/(1+8u^3))^3$；(5.4) $\delta(1-\delta) = 16u^9(1-u^3)/(1+8u^3)$；(5.5) $1 + 8t^3 = m'^2 = (1+2u)^4/(1+8u^3)$；(5.6) $t^3(1-2u+4u^2) = u(1+u+u^2)$。其中 $m'$ 为第 3 节的 $\alpha$–$\beta$ 间乘子的平方根关系中的量（见 (5.5)）。

**状态：** 已证明（书中给出证明；(iv) 的印文见下“转录注意”）。**对照：** M06（模方程）、M11、M14（$u$ 参数化）。

**我自验：** 取 $q = 0.5$、$0.2$（mpmath 30 位，theta 路线）：(i)–(iii) 差 $\le 1.9\times 10^{-25}$（(ii) 在 $q = 0.5$ 处差 $1.9\times 10^{-25}$，为 $\alpha\approx 0.99999$ 时 $1-\alpha\approx 10^{-5}$ 的相对精度极限；$q = 0.2$ 时差 $\le 2.0\times 10^{-28}$）；(iv) 按上文订正形式差 $\le 1.0\times 10^{-30}$。

**转录注意（Entry 5(iv) 原书印文问题）。** 书中 (iv) 的印文（书页 360）为 $[\{16\beta\gamma(1-\beta)(1-\gamma)\}^{1/24} + \{\alpha\delta(1-\alpha)(1-\delta)\}^{1/8}]/[\{16\beta\gamma(1-\beta)(1-\gamma)\}^{1/24} + \{\beta\gamma(1-\beta)(1-\gamma)\}^{1/8}]$，即两处 $1/8$ 次项内无因子 $16$；但书中 (iv) 的证明（书页 362）所用的却是 $[\{16\beta\gamma(1-\beta)(1-\gamma)\}^{1/24} + \{16\alpha\delta(1-\alpha)(1-\delta)\}^{1/8}]/[\{16\beta\gamma(1-\beta)(1-\gamma)\}^{1/24} + \{16\beta\gamma(1-\beta)(1-\gamma)\}^{1/8}]$，并由此推出 $(256\alpha^3(1-\alpha)^3\delta^3(1-\delta)^3/(\beta(1-\beta)\gamma(1-\gamma)))^{1/24}$ 等式——证明的代数与带 $16$ 的版本一致，与印文版差一个 $\sqrt{2}$ 因子。数值复核：按印文版，$q = 0.5$ 时差 $0.077321$、$q = 0.2$ 时差 $0.063222$；按证明版（上文陈述），两点差 $\le 1.0\times 10^{-30}$。故印文 (iv) 为印误，两个 $1/8$ 次项内应各补因子 $16$；上文陈述已按订正记录。待查 Berndt 勘误。

## Entry 6

**陈述。** $\varphi$、$\psi$、$f$ 如 Ch. 16 Entry 22。则

**(i)** $\psi(q^{1/11}) - q^{15/11}\psi(q^{11}) = f(q^5,q^6) + q^{1/11}f(q^4,q^7) + q^{3/11}f(q^3,q^8) + q^{6/11}f(q^2,q^9) + q^{10/11}f(q,q^{10}).$

**(ii)** $\varphi(q^{1/11}) - \varphi(q^{11}) = 2q^{1/11}f(q^9,q^{13}) + 2q^{4/11}f(q^7,q^{15}) + 2q^{9/11}f(q^5,q^{17}) + 2q^{16/11}f(q^3,q^{19}) + 2q^{25/11}f(q,q^{21}).$

**(iii)** $f(-q^{1/11})/f(-q^{11}) = f(-q^4,-q^7)/f(-q^2,-q^9) - q^{1/11}f(-q^2,-q^9)/f(-q,-q^{10}) - q^{2/11}f(-q^5,-q^6)/f(-q^3,-q^8) + q^{5/11} + q^{7/11}f(-q^3,-q^8)/f(-q^4,-q^7) - q^{15/11}f(-q,-q^{10})/f(-q^5,-q^6).$

**说明。**(iii) 是 Ch. 19 定理 12.1 的 (12.26) 在 $n = 11$ 的情形（已逐项对照定理原文）；(i)(ii) 由 (iii) 与 Ch. 16 的恒等式得到。

**状态：** 已证明（书中给出证明）。**对照：** M07（theta 函数）、M02。

**我自验：** 取 $q = 0.5$、$0.3$（mpmath 30 位，直接求和）：(i)(ii) 差 $\le 7.9\times 10^{-31}$；(iii) 差 $\le 2.5\times 10^{-12}$（$q = 0.5$，$f(-q^{1/11})$ 的 $q$-Pochhammer 截断尾项量级；$q = 0.3$ 时差 $1.0\times 10^{-9}$，同上原因）。

## Entry 7

**陈述。** 设 $\beta$ 为 $\alpha$ 的 11 次模，$m = z_1/z_{11}$。则

**(i)** $(\alpha\beta)^{1/4} + \{(1-\alpha)(1-\beta)\}^{1/4} + 2\{16\alpha\beta(1-\alpha)(1-\beta)\}^{1/12} = 1.$

**(ii)** $m - 11/m = 2((\alpha\beta)^{1/4} - \{(1-\alpha)(1-\beta)\}^{1/4})(4 + (\alpha\beta)^{1/4} + \{(1-\alpha)(1-\beta)\}^{1/4}).$

**(iii)** $m + 11/m = 2\sqrt{2}(2 + (\alpha\beta)^{1/4} + \{(1-\alpha)(1-\beta)\}^{1/4})(1 + (\alpha\beta)^{1/2} + \{(1-\alpha)(1-\beta)\}^{1/2})^{1/2}.$

**(iv)** $((1-\beta)^3/(1-\alpha))^{1/8} - (\beta^3/\alpha)^{1/8} - (\beta^3(1-\beta)^3/(\alpha(1-\alpha)))^{1/8} = (m/\sqrt{2})(1 + (\alpha\beta)^{1/2} + \{(1-\alpha)(1-\beta)\}^{1/2})^{1/2}.$

**(v)** $(\alpha^3/\beta)^{1/8} - ((1-\alpha)^3/(1-\beta))^{1/8} - (\alpha^3(1-\alpha)^3/(\beta(1-\beta)))^{1/8} = (11/(m\sqrt{2}))(1 + (\alpha\beta)^{1/2} + \{(1-\alpha)(1-\beta)\}^{1/2})^{1/2}.$

**(vi)** $(1/m)\{1 + 2^{10/3}(\beta^{11}(1-\beta)^{11}/(\alpha(1-\alpha)))^{1/24}\} - (m/11)\{1 + 2^{10/3}(\alpha^{11}(1-\alpha)^{11}/(\beta(1-\beta)))^{1/24}\} = 2((\alpha\beta)^{1/2} - \{(1-\alpha)(1-\beta)\}^{1/2}).$

**(vii)** $(1/m)\{1 + 2^{10/3}(\beta^{11}(1-\beta)^{11}/(\alpha(1-\alpha)))^{1/24}\} + (m/11)\{1 + 2^{10/3}(\alpha^{11}(1-\alpha)^{11}/(\beta(1-\beta)))^{1/24}\} = 2\sqrt{2}((\alpha\beta)^{1/4} + \{(1-\alpha)(1-\beta)\}^{1/4})(1 + (\alpha\beta)^{1/2} + \{(1-\alpha)(1-\beta)\}^{1/2})^{1/2}.$

另有恒等式

$$(7.1)\quad f(a,b) = f(a^3b,ab^3) + a\cdot f(b/a,a^5b^3).$$

**说明。** 拉马努金在笔记中还标了 (viii)、(ix) 两条，但已被他本人划去，故不收录。文献中第一个 11 次模方程见 Sohncke [1]、[2]；(i) 本身则出自 Schröter 1858 年的论文 [3]、[4]（无证明）；其余六条归于拉马努金；更复杂的 11 次方程见 Schläfli、Fiedler、Fricke、Russell。(i) 的证明用 theta 恒等式 (7.2)–(7.5)；(ii)–(vii) 翻译成模形式后（式 (7.6)–(7.15)），由赋值公式与 MACSYMA 验证 $q$ 展开系数：(7.11)–(7.13) 验到 $q^{12}$，(7.14)(7.15) 验到 $q^{16}$；引理 7.1–7.5 处理尖点 $\zeta_1$ 至 $\zeta_6$ 处的阶。

**状态：** 已证明（书中给出证明；(i) 为 Schröter 1858 年的结果，其余六条为拉马努金的结果）。**对照：** M06（模方程）、M11、M07（(7.1) 的 theta 恒等式）。

**我自验：** 取 $q = 0.5$、$0.2$（mpmath 30 位，theta 路线）：(i)–(vii) 全部通过，差 $\le 6.2\times 10^{-27}$；(7.1) 取 $a = 0.3$、$b = 0.5$ 与 $a = 0.2$、$b = 0.7$ 两组，差 $0$。

**转录注意（(7.1) 第二个 $f$ 的第二变元）。** 书中 (7.1) 的第二个 $f$ 的第二变元印为 $(a/b)a^4b^4$，即 $a^5b^3$；300 DPI 放大图（PDF 页 365）确认此读法。数值复核：按 $a^5b^3$ 计，两组参数差均为 $0$；若按字面 $a^4b^4$ 计，差分别为 $3.4\times 10^{-4}$、$2.4\times 10^{-3}$，不成立。

## Entry 8

**陈述。** $\varphi$、$\psi$、$f$ 如 Ch. 16 Entry 22。置

$$\mu_1 = f(-q^4,-q^9)/(q^{7/13}f(-q^2,-q^{11})),\quad \mu_2 = f(-q^6,-q^7)/(q^{6/13}f(-q^3,-q^{10})),\quad \mu_3 = f(-q^2,-q^{11})/(q^{5/13}f(-q,-q^{12})),$$

$$\mu_4 = f(-q^5,-q^8)/(q^{2/13}f(-q^4,-q^9)),\quad \mu_5 = q^{5/13}f(-q^3,-q^{10})/f(-q^5,-q^8),\quad \mu_6 = q^{15/13}f(-q,-q^{12})/f(-q^6,-q^7).$$

则

**(i)**

$$(8.1)\quad f(-q^{1/13})/(q^{7/13}f(-q^{13})) = \mu_1 - \mu_2 - \mu_3 + \mu_4 + 1 - \mu_5 + \mu_6,$$

$$(8.2)\quad 1 + f^2(-q)/(qf^2(-q^{13})) = \mu_1\mu_2 - \mu_3\mu_5 - \mu_4\mu_6,$$

$$(8.3)\quad -4 - f^2(-q)/(qf^2(-q^{13})) = 1/(\mu_1\mu_2) - 1/(\mu_3\mu_5) - 1/(\mu_4\mu_6),$$

$$(8.4)\quad 3 + f^2(-q)/(qf^2(-q^{13})) = \mu_2\mu_3\mu_4 - \mu_1\mu_5\mu_6,$$

$$(8.5)\quad 1 = \mu_1\mu_2\mu_3\mu_4\mu_5\mu_6.$$

**(ii)** $f(-q,-q^{12})f(-q^2,-q^{11})f(-q^3,-q^{10})f(-q^4,-q^9)f(-q^5,-q^8)f(-q^6,-q^7) = f(-q)f^5(-q^{13}).$

**(iii)** 设 $\beta$ 为 $\alpha$ 的 13 次模，$m = z_1/z_{13}$，则

$$m = (\beta/\alpha)^{1/4} + ((1-\beta)/(1-\alpha))^{1/4} - (\beta(1-\beta)/(\alpha(1-\alpha)))^{1/4} - 4(\beta(1-\beta)/(\alpha(1-\alpha)))^{1/6}.$$

**(iv)** $13/m = (\alpha/\beta)^{1/4} + ((1-\alpha)/(1-\beta))^{1/4} - (\alpha(1-\alpha)/(\beta(1-\beta)))^{1/4} - 4(\alpha(1-\alpha)/(\beta(1-\beta)))^{1/6}.$

**说明。**(8.1) 即 Ch. 19 定理 12.1 的 (12.25) 在 $n = 13$ 的情形（已逐项对照定理原文，首项 $q^{7/13}$ 一致）。(8.2) 的证明用 Evans 定理 8.1（即 Evans [1，定理 6.2]，其中 $a_{13} = -2$，用 Hecke 算子与 $\{\Gamma(12),1,1\}_0$ 的维数为 1）；(8.3)(8.4) 翻译成 (8.14)(8.15) 后由尖点阶证明。另有 Evans [1，定理 7.1] 的恒等式（书页 376）：置 $t = q^{1/13}$，则

$$1/((t^2)_{\infty}(t^3)_{\infty}(t^{10})_{\infty}(t^{11})_{\infty}) + t/((t^4)_{\infty}(t^6)_{\infty}(t^7)_{\infty}(t^9)_{\infty}) = 1/((t)_{\infty}(t^5)_{\infty}(t^8)_{\infty}(t^{12})_{\infty}),$$

等价于 $G_1^{-1}G_5^{-1} + G_4G_6 = 1$。(iii)(iv) 的证明用 theta 恒等式 (8.25)/(8.27) 与 $\Gamma(2)\cap\Gamma_0(13)$ 上的权 $9/2$ 模形式，$\rho = 9$，MACSYMA 验证 $q$ 展开系数到 $q^{13}$（由互反关系得 $\mu = 15$）。此前文献中的 13 次模方程见 Sohncke、Schläfli、Klein、Russell，皆比 (iii)(iv) 复杂。

**状态：** 已证明（书中给出证明；(8.1) 为 Ch. 19 定理 12.1 的 $n = 13$ 情形）。**对照：** M06（模方程）、M07（theta 函数）、M02。

**我自验：** 取 $q = 0.5$、$0.3$（mpmath 30 位，直接求和）：(8.1)–(8.5) 与 (ii) 差 $\le 2.7\times 10^{-26}$；取 $q = 0.5$、$0.2$（theta 路线）：(iii)(iv) 差 $\le 2.7\times 10^{-26}$。

## Entry 9

**陈述。** $\varphi$、$\psi$、$f$、$\chi$ 如 Ch. 16 Entry 22。则

**(i)** $\psi(q^3)\psi(q^5) - \psi(-q^3)\psi(-q^5) = 2q^3\psi(q^2)\psi(q^{30}).$

**(ii)** $\varphi(-q^6)\varphi(-q^{10}) + 2q\psi(q^3)\psi(q^5) = \varphi(q)\varphi(q^{15}).$

**(iii)** $\varphi(-q^2)\varphi(-q^{30}) + 2q^2\psi(q)\psi(q^{15}) = \varphi(q^3)\varphi(q^5).$

**(iv)** $\psi(q)\psi(q^{15}) + \psi(-q)\psi(-q^{15}) = 2\psi(q^6)\psi(q^{10}).$

**(v)** $\varphi(q)\varphi(q^{15}) - \varphi(q^3)\varphi(q^5) = 2qf(-q^2)f(-q^{30})\chi(q^3)\chi(q^5).$

**(vi)** $\varphi(q)\varphi(q^{15}) + \varphi(q^3)\varphi(q^5) = 2f(-q^6)f(-q^{10})\chi(q)\chi(q^{15}).$

**(vii)** $\{\psi(q^3)\psi(q^5) - q\psi(q)\psi(q^{15})\}\varphi(-q^3)\varphi(-q^5) = \{\psi(q^3)\psi(q^5) + q\psi(q)\psi(q^{15})\}\varphi(-q)\varphi(-q^{15}) = f(-q)f(-q^3)f(-q^5)f(-q^{15}).$

**说明。**(v)–(vii) 的证明推迟到第 11 节（书页 394–396，式 (11.40)(11.41)）；(i)–(iv) 由 Ch. 16 Entry 18(iv) 与第 31 节的恒等式得到。

**状态：** 已证明（书中给出证明；(v)–(vii) 的证明在第 11 节）。**对照：** M07（theta 函数）、M02。

**我自验：** 取 $q = 0.5$、$0.3$（mpmath 30 位，直接求和）：(i)–(vii) 差 $\le 1.9\times 10^{-28}$。

## Entry 10

**陈述。** $\varphi$、$\psi$、$f$ 如 Ch. 16 Entry 22。则

**(i)** $f(-q^7,-q^8) + qf(-q^2,-q^{13}) = f(-q^2,-q^3)/f(-q,-q^4)\cdot f(-q^5).$

**(ii)** $f(-q^4,-q^{11}) - qf(-q,-q^{14}) = f(-q,-q^4)/f(-q^2,-q^3)\cdot f(-q^5).$

**(iii)** $f(-q^7,-q^8) - qf(-q^2,-q^{13}) = f(-q^{2/3},-q) + q^{2/3}f(-q^3,-q^{12}).$

**(iv)** $\{f(-q^4,-q^{11}) + qf(-q,-q^{14})\}q^{1/3} = f(-q^6,-q^9) - f(-q^{1/3},-q^{4/3}).$

**(v)** $q\psi(q^3)\psi(q^5) + q^2\psi(q)\psi(q^{15}) = q/(1-q) - q^7/(1-q^7) - q^{11}/(1-q^{11}) - q^{13}/(1-q^{13}) + q^{17}/(1-q^{17}) + q^{19}/(1-q^{19}) + q^{23}/(1-q^{23}) - q^{29}/(1-q^{29}) + \cdots,$

其中右端系数以 30 为周期：一般项为 $\sum_{n\ge 1}(q^n - q^{7n} - q^{11n} - q^{13n} + q^{17n} + q^{19n} + q^{23n} - q^{29n})/(1-q^{30n})$。

**(vi)** $\varphi(q^3)\varphi(q^5) + \varphi(q)\varphi(q^{15}) = 2(1 + q/(1-q) - q^2/(1-q^2) + q^4/(1-q^4) - q^7/(1-q^7) + q^8/(1-q^8) - q^{11}/(1-q^{11}) - q^{13}/(1-q^{13}) + q^{14}/(1-q^{14}) + q^{16}/(1-q^{16}) + q^{17}/(1-q^{17}) + q^{19}/(1-q^{19}) + q^{22}/(1-q^{22}) + q^{23}/(1-q^{23}) + q^{26}/(1-q^{26}) - q^{28}/(1-q^{28}) - q^{29}/(1-q^{29}) + q^{31}/(1-q^{31}) + q^{32}/(1-q^{32}) - q^{34}/(1-q^{34}) - q^{37}/(1-q^{37}) - q^{38}/(1-q^{38}) - q^{41}/(1-q^{41}) - q^{43}/(1-q^{43}) - q^{44}/(1-q^{44}) - q^{46}/(1-q^{46}) + q^{47}/(1-q^{47}) + q^{49}/(1-q^{49}) - q^{52}/(1-q^{52}) + q^{53}/(1-q^{53}) - q^{56}/(1-q^{56}) + q^{58}/(1-q^{58}) - q^{59}/(1-q^{59}) + \cdots),$

其中右端系数以 60 为周期（上文印出的项覆盖一个完整周期 $1$ 至 $59$，未出现的剩余类系数为 $0$）。

**说明。** 拉马努金在笔记（p. 245）中 (v) 只写了前六项、(vi) 只写了前四项，未明言周期规律；书中先由 15 周期的中间形式（书页 383：$\varphi(-q^3)\varphi(-q^5) + \varphi(-q)\varphi(-q^{15}) - 2 = -2(q/(1+q) + q^2/(1+q^2) + q^4/(1+q^4) - q^7/(1+q^7) + q^8/(1+q^8) - q^{11}/(1+q^{11}) - q^{13}/(1+q^{13}) - q^{14}/(1+q^{14}) + \cdots)$）变号，再用 $q^n/(1+q^n) = q^n/(1-q^n) - 2q^{2n}/(1-q^{2n})$（$n$ 偶）化到 30 周期、60 周期，得到 (v)(vi)。

**状态：** 已证明（书中给出证明；(v)(vi) 的周期规律为 Berndt 的整理，拉马努金原文只写了前几项）。**对照：** M07（theta 函数）、M02（Lambert 级数与系数周期）。

**我自验：** 取 $q = 0.5$、$0.3$（mpmath 30 位，直接求和）：(i)–(iv) 差 $0$；(v) 按上文 $\sum_{n\ge 1}(\cdots)/(1-q^{30n})$ 的形式（求和到 $n = 199$）差 $0$；(vi) 按上文 60 周期系数（求和到 $n = 399$）差 $\le 3.9\times 10^{-31}$。

## Entry 11

**陈述。** 设 $\alpha$、$\beta$、$\gamma$、$\delta$ 的次数依次为 $1$、$3$、$5$、$15$，$m$ 为 $\alpha$–$\beta$ 间的乘子，$m'$ 为 $\gamma$–$\delta$ 间的乘子。则

**(i)** $(\alpha\delta)^{1/8} + \{(1-\alpha)(1-\delta)\}^{1/8} = \sqrt{m'/m}.$

**(ii)** $(\beta\gamma)^{1/8} + \{(1-\beta)(1-\gamma)\}^{1/8} = \sqrt{m/m'} = [(\beta\gamma)^{1/8} - \{\beta\gamma(1-\beta)(1-\gamma)\}^{1/8}]/(\alpha\delta)^{1/4} = [\{(1-\beta)(1-\gamma)\}^{1/8} - \{\beta\gamma(1-\beta)(1-\gamma)\}^{1/8}]/[(1-\alpha)(1-\delta)]^{1/4}.$

**(iii)** $(\alpha\delta)^{1/8} - \{(1-\alpha)(1-\delta)\}^{1/8} = (\beta\gamma)^{1/8} - \{(1-\beta)(1-\gamma)\}^{1/8}.$

**(iv)** $1 + (\beta\gamma)^{1/8} + \{(1-\beta)(1-\gamma)\}^{1/8} = 4^{1/3}(\beta^2\gamma^2(1-\beta)^2(1-\gamma)^2/(\alpha\delta(1-\alpha)(1-\delta)))^{1/24}.$

**(v)** $1 - (\alpha\delta)^{1/8} - \{(1-\alpha)(1-\delta)\}^{1/8} = 4^{1/3}(\alpha^2\delta^2(1-\alpha)^2(1-\delta)^2/(\beta\gamma(1-\beta)(1-\gamma)))^{1/24}.$

**(vi)** $(\alpha\delta)^{1/16}(\{(1+\sqrt{\alpha})(1+\sqrt{\delta})\}^{1/4} + \{(1-\sqrt{\alpha})(1-\sqrt{\delta})\}^{1/4}) + \{(1-\alpha)(1-\delta)\}^{1/16}(\{(1+\sqrt{1-\alpha})(1+\sqrt{1-\delta})\}^{1/4} + \{(1-\sqrt{1-\alpha})(1-\sqrt{1-\delta})\}^{1/4}) = \sqrt{2}.$

**(vii)** $(\beta\gamma)^{1/16}(\{(1+\sqrt{\beta})(1+\sqrt{\gamma})\}^{1/4} - \{(1-\sqrt{\beta})(1-\sqrt{\gamma})\}^{1/4}) + \{(1-\beta)(1-\gamma)\}^{1/16}(\{(1+\sqrt{1-\beta})(1+\sqrt{1-\gamma})\}^{1/4} - \{(1-\sqrt{1-\beta})(1-\sqrt{1-\gamma})\}^{1/4}) = \sqrt{2}.$

**(viii)** $(\alpha\delta/(\beta\gamma))^{1/8} + ((1-\alpha)(1-\delta)/((1-\beta)(1-\gamma)))^{1/8} - (\alpha\delta(1-\alpha)(1-\delta)/(\beta\gamma(1-\beta)(1-\gamma)))^{1/8} = \sqrt{m'/m}.$

**(ix)** $(\beta\gamma/(\alpha\delta))^{1/8} + ((1-\beta)(1-\gamma)/((1-\alpha)(1-\delta)))^{1/8} - (\beta\gamma(1-\beta)(1-\gamma)/(\alpha\delta(1-\alpha)(1-\delta)))^{1/8} = -\sqrt{m/m'}.$

**(x)** $(\beta\delta/(\alpha\gamma))^{1/4} + ((1-\beta)(1-\delta)/((1-\alpha)(1-\gamma)))^{1/4} - (\beta\delta(1-\beta)(1-\delta)/(\alpha\gamma(1-\alpha)(1-\gamma)))^{1/4} - 4(\beta\delta(1-\beta)(1-\delta)/(\alpha\gamma(1-\alpha)(1-\gamma)))^{1/6} = mm'.$

**(xi)** $(\alpha\gamma/(\beta\delta))^{1/4} + ((1-\alpha)(1-\gamma)/((1-\beta)(1-\delta)))^{1/4} - (\alpha\gamma(1-\alpha)(1-\gamma)/(\beta\delta(1-\beta)(1-\delta)))^{1/4} - 4(\alpha\gamma(1-\alpha)(1-\gamma)/(\beta\delta(1-\beta)(1-\delta)))^{1/6} = 9/(mm').$

**(xii)** $(\gamma\delta/(\alpha\beta))^{1/4} + ((1-\gamma)(1-\delta)/((1-\alpha)(1-\beta)))^{1/4} + (\gamma\delta(1-\gamma)(1-\delta)/(\alpha\beta(1-\alpha)(1-\beta)))^{1/4} - 2(\gamma\delta(1-\gamma)(1-\delta)/(\alpha\beta(1-\alpha)(1-\beta)))^{1/8}\{1 + (\gamma\delta/(\alpha\beta))^{1/8} + ((1-\gamma)(1-\delta)/((1-\alpha)(1-\beta)))^{1/8}\} = z_1z_3/(z_5z_{15}).$

**(xiii)** $(\alpha\beta/(\gamma\delta))^{1/4} + ((1-\alpha)(1-\beta)/((1-\gamma)(1-\delta)))^{1/4} + (\alpha\beta(1-\alpha)(1-\beta)/(\gamma\delta(1-\gamma)(1-\delta)))^{1/4} - 2(\alpha\beta(1-\alpha)(1-\beta)/(\gamma\delta(1-\gamma)(1-\delta)))^{1/8}\{1 + (\alpha\beta/(\gamma\delta))^{1/8} + ((1-\alpha)(1-\beta)/((1-\gamma)(1-\delta)))^{1/8}\} = 25z_5z_{15}/(z_1z_3).$

**(xiv)** $(\alpha\beta\gamma\delta)^{1/8} + \{(1-\alpha)(1-\beta)(1-\gamma)(1-\delta)\}^{1/8} + 2^{1/3}\{\alpha\beta\gamma\delta(1-\alpha)(1-\beta)(1-\gamma)(1-\delta)\}^{1/24} = 1.$

**(xv)** 若 $P = \{256\alpha\beta\gamma\delta(1-\alpha)(1-\beta)(1-\gamma)(1-\delta)\}^{1/48}$，$Q = (\alpha\delta(1-\alpha)(1-\delta)/(\beta\gamma(1-\beta)(1-\gamma)))^{1/16}$，则 $Q + 1/Q = \sqrt{2}(P + 1/P).$

**说明。**(i) 与 (ii) 的第一等式之积由拉马努金在致 Hardy 的第二封信中给出（文献 [10]，p. xxix）；(xiv) 亦见该信；(iii) 与 (vi) 由 Hardy [3，p. 220] 记录（Hardy 在 (vi) 中有两个符号错误，书中已订正）；(viii) 与 (ix) 相乘得 Weber [1] 的方程；Weber 亦建立了 (xiv)。证明用 (11.1)–(11.6)、(11.13)–(11.15)，其中 $\rho^2 = (1+M-M^2)/M$（式 (11.4)），$M = (z_1z_{15}/(z_3z_5))^{1/2} = (m/m')^{1/2}$。

**状态：** 已证明（书中给出证明；(vi) 为 Hardy 记录的公式经 Berndt 订正符号后的版本）。**对照：** M06（模方程）、M11、M14。

**我自验：** 取 $q = 0.5$、$0.2$（mpmath 30 位，theta 路线）：(i)–(xv) 全部通过，差 $\le 5.1\times 10^{-26}$。

## Entry 12

**陈述。** $\varphi$、$\psi$、$f$ 如 Ch. 16 Entry 22。置

$$\mu_1 = f(-q^6,-q^{11})/(q^{12/17}f(-q^3,-q^{14})),\quad \mu_2 = f(-q^4,-q^{13})/(q^{11/17}f(-q^2,-q^{15})),\quad \mu_3 = f(-q^8,-q^9)/(q^{10/17}f(-q^4,-q^{13})),$$

$$\mu_4 = f(-q^2,-q^{15})/(q^{7/17}f(-q,-q^{16})),\quad \mu_5 = f(-q^7,-q^{10})/(q^{5/17}f(-q^5,-q^{12})),\quad \mu_6 = q^{3/17}f(-q^5,-q^{12})/f(-q^6,-q^{11}),$$

$$\mu_7 = q^{14/17}f(-q^3,-q^{14})/f(-q^7,-q^{10}),\quad \mu_8 = q^{28/17}f(-q,-q^{16})/f(-q^8,-q^9).$$

则

**(i)**

$$(12.1)\quad f(-q^{1/17})/(q^{12/17}f(-q^{17})) = \mu_1 - \mu_2 - \mu_3 + \mu_4 + \mu_5 - 1 - \mu_6 + \mu_7 - \mu_8,$$

$$(12.2)\quad \mu_1\mu_5\mu_6\mu_7 = \mu_2\mu_8\mu_3\mu_4 = 1,$$

$$(12.3)\quad \mu_1\mu_5 + \mu_2\mu_8 - \mu_3\mu_4 - \mu_6\mu_7 = -1.$$

**(ii)** $f(-q)f^7(-q^{17}) = \prod_{k=1}^{8}f(-q^k,-q^{17-k}).$

**(iii)** 设 $\beta$ 为 $\alpha$ 的 17 次模，$m = z_1/z_{17}$，则

$$m = (\beta/\alpha)^{1/4} + ((1-\beta)/(1-\alpha))^{1/4} + (\beta(1-\beta)/(\alpha(1-\alpha)))^{1/4} - 2(\beta(1-\beta)/(\alpha(1-\alpha)))^{1/8}\{1 + (\beta/\alpha)^{1/8} + ((1-\beta)/(1-\alpha))^{1/8}\}.$$

**(iv)** $17/m = (\alpha/\beta)^{1/4} + ((1-\alpha)/(1-\beta))^{1/4} + (\alpha(1-\alpha)/(\beta(1-\beta)))^{1/4} - 2(\alpha(1-\alpha)/(\beta(1-\beta)))^{1/8}\{1 + (\alpha/\beta)^{1/8} + ((1-\alpha)/(1-\beta))^{1/8}\}.$

**说明。**(12.1) 即 Ch. 19 定理 12.1 的 (12.26) 在 $n = 17$ 的情形（已逐项对照定理原文，首项 $q^{12/17}$ 一致）。(12.3) 的证明用 (12.4)：$f^2(-q) = \sum_{m,n;\,n\ge 2|m|}(-1)^{m+n}q^{n(n+1)/2-m(3m-1)/2}$（Rogers [1] 1894 年、Hecke 1925 年、Andrews、Bressoud、Kac–Peterson 的工作）。(iii)(iv) 的证明用 (12.10)(12.11) 的权 3 模形式，$\rho_{\Gamma} = 9$，MACSYMA 验证 $q$ 展开系数到 $q^{13}$。此前文献中的 17 次模方程见 Sohncke、Schläfli、Russell、Greenhill，皆不如 (iii)(iv) 简洁。拉马努金在本节末尾有一段注记（N.B.，书页 400）：$\varphi(x^{1/n})$、$\psi(x^{1/n})$、$f(-x^{1/n})$ 可表为 $\frac12(n-1)$ 个 $n$ 次根之和；二次情形只在 5、17、257 次出现，三次在 7、13、19、37、73、97、109、163、193 次出现，五次在 11、41、101 次出现；$f^3(-x^{1/n})$ 亦有类似表述——Berndt 注明：“We are unable to provide a proper interpretation for most of this statement.”（该注记的大部分表述尚无合理解释。）

**状态：** 已证明（书中给出证明；(12.1) 为 Ch. 19 定理 12.1 的 $n = 17$ 情形；末尾 N.B. 注记的大部分表述未解决）。**对照：** M06（模方程）、M07（theta 函数）、M02。

**我自验：** 取 $q = 0.5$、$0.3$（mpmath 30 位，直接求和）：(12.1)–(12.3) 与 (ii) 差 $\le 2.2\times 10^{-26}$；取 $q = 0.5$、$0.2$（theta 路线）：(iii)(iv) 差 $\le 2.2\times 10^{-26}$。

## Entry 13

**陈述。** 设 $\alpha$、$\beta$、$\gamma$、$\delta$ 的次数依次为 $1$、$3$、$7$、$21$，$m = z_1/z_3$，$m' = z_7/z_{21}$。则

**(i)** $(\beta\gamma/(\alpha\delta))^{1/4} + ((1-\beta)(1-\gamma)/((1-\alpha)(1-\delta)))^{1/4} - (\beta\gamma(1-\beta)(1-\gamma)/(\alpha\delta(1-\alpha)(1-\delta)))^{1/4} + 4(\beta\gamma(1-\beta)(1-\gamma)/(\alpha\delta(1-\alpha)(1-\delta)))^{1/6} = m/m'.$

**(ii)** $(\alpha\delta/(\beta\gamma))^{1/4} + ((1-\alpha)(1-\delta)/((1-\beta)(1-\gamma)))^{1/4} - (\alpha\delta(1-\alpha)(1-\delta)/(\beta\gamma(1-\beta)(1-\gamma)))^{1/4} + 4(\alpha\delta(1-\alpha)(1-\delta)/(\beta\gamma(1-\beta)(1-\gamma)))^{1/6} = m'/m.$

**(iii)** $(\gamma\delta/(\alpha\beta))^{1/8} + ((1-\gamma)(1-\delta)/((1-\alpha)(1-\beta)))^{1/8} - (\gamma\delta(1-\gamma)(1-\delta)/(\alpha\beta(1-\alpha)(1-\beta)))^{1/8} - 2(\gamma\delta(1-\gamma)(1-\delta)/(\alpha\beta(1-\alpha)(1-\beta)))^{1/12} = (z_1z_3/(z_7z_{21}))^{1/2}.$

**(iv)** $(\alpha\beta/(\gamma\delta))^{1/8} + ((1-\alpha)(1-\beta)/((1-\gamma)(1-\delta)))^{1/8} - (\alpha\beta(1-\alpha)(1-\beta)/(\gamma\delta(1-\gamma)(1-\delta)))^{1/8} - 2(\alpha\beta(1-\alpha)(1-\beta)/(\gamma\delta(1-\gamma)(1-\delta)))^{1/12} = 7(z_7z_{21}/(z_1z_3))^{1/2}.$

**(v)** $(\beta\delta/(\alpha\gamma))^{1/4} + ((1-\beta)(1-\delta)/((1-\alpha)(1-\gamma)))^{1/4} + (\beta\delta(1-\beta)(1-\delta)/(\alpha\gamma(1-\alpha)(1-\gamma)))^{1/4} - 2(\beta\delta(1-\beta)(1-\delta)/(\alpha\gamma(1-\alpha)(1-\gamma)))^{1/8}\{1 + (\beta\delta/(\alpha\gamma))^{1/8} + ((1-\beta)(1-\delta)/((1-\alpha)(1-\gamma)))^{1/8}\} = mm'.$

**(vi)** $(\alpha\gamma/(\beta\delta))^{1/4} + ((1-\alpha)(1-\gamma)/((1-\beta)(1-\delta)))^{1/4} + (\alpha\gamma(1-\alpha)(1-\gamma)/(\beta\delta(1-\beta)(1-\delta)))^{1/4} - 2(\alpha\gamma(1-\alpha)(1-\gamma)/(\beta\delta(1-\beta)(1-\delta)))^{1/8}\{1 + (\alpha\gamma/(\beta\delta))^{1/8} + ((1-\alpha)(1-\gamma)/((1-\beta)(1-\delta)))^{1/8}\} = 9/(mm').$

**说明。**(ii)、(iv)、(vi) 分别是 (i)、(iii)、(v) 的互反形式（把 $\alpha$、$\beta$、$\gamma$、$\delta$ 换成其补 $1-\delta$、$1-\gamma$、$1-\beta$、$1-\alpha$ 得到）。证明用模形式与 theta 恒等式 (13.1)–(13.6)；$\mu$ 表：(13.4) $\nu = 10$、$\mu = 20$，(13.5) $\nu = 8$、$\mu = 16$，(13.6) $\nu = 12$、$\mu = 24$，MACSYMA 验证 $F$、$F^*$ 的系数到 $q^{\mu}$；(13.19) 的不等式 $\mu+1 > \nu(p+1)(q+1)/16$ 在 $p = 3$、$q = 7$ 时给出 $2$。

**状态：** 已证明（书中给出证明）。**对照：** M06（模方程）、M11。

**我自验：** 取 $q = 0.5$、$0.2$（mpmath 30 位，theta 路线）：(i)–(vi) 全部通过，差 $\le 1.4\times 10^{-25}$（(i) 在 $q = 0.5$ 处差 $1.4\times 10^{-25}$，为 $\alpha\approx 0.99999$ 时 $1-\alpha\approx 10^{-5}$ 的相对精度极限；$q = 0.2$ 时差 $\le 2.0\times 10^{-28}$）。

## Entry 14

**陈述。** 设 $\alpha$、$\beta$、$\gamma$、$\delta$ 的次数依次为 $1$、$3$、$11$、$33$，$m$ 为 $\alpha$–$\beta$ 间的乘子，$m'$ 为 $\gamma$–$\delta$ 间的乘子。则

**(i)** $(\beta\delta/(\alpha\gamma))^{1/8} + ((1-\beta)(1-\delta)/((1-\alpha)(1-\gamma)))^{1/8} - (\beta\delta(1-\beta)(1-\delta)/(\alpha\gamma(1-\alpha)(1-\gamma)))^{1/8} - 2(\beta\delta(1-\beta)(1-\delta)/(\alpha\gamma(1-\alpha)(1-\gamma)))^{1/12} = \sqrt{mm'}.$

**(ii)** $(\alpha\gamma/(\beta\delta))^{1/8} + ((1-\alpha)(1-\gamma)/((1-\beta)(1-\delta)))^{1/8} - (\alpha\gamma(1-\alpha)(1-\gamma)/(\beta\delta(1-\beta)(1-\delta)))^{1/8} - 2(\alpha\gamma(1-\alpha)(1-\gamma)/(\beta\delta(1-\beta)(1-\delta)))^{1/12} = 3/\sqrt{mm'}.$

**说明。**(ii) 是 (i) 的互反形式。证明用 theta 恒等式 (14.1)–(14.9) 与 Ch. 19 Entry 7(i)。

**状态：** 已证明（书中给出证明）。**对照：** M06（模方程）、M11。

**我自验：** 取 $q = 0.5$、$0.2$（mpmath 30 位，theta 路线）：(i)(ii) 差 $\le 7.0\times 10^{-27}$。

## Entry 15

**陈述。** 设 $\beta$ 为 $\alpha$ 的 23 次模，$m = z_1/z_{23}$。则

**(i)** $(\alpha\beta)^{1/8} + \{(1-\alpha)(1-\beta)\}^{1/8} + 2^{2/3}\{\alpha\beta(1-\alpha)(1-\beta)\}^{1/24} = 1.$

**(ii)** $1 + (\alpha\beta)^{1/4} + \{(1-\alpha)(1-\beta)\}^{1/4} + 2^{4/3}\{\alpha\beta(1-\alpha)(1-\beta)\}^{1/12} = \{2(1 + (\alpha\beta)^{1/2} + \{(1-\alpha)(1-\beta)\}^{1/2})\}^{1/2}.$

**(iii)** $m - 23/m = 2((\alpha\beta)^{1/8} - \{(1-\alpha)(1-\beta)\}^{1/8})(11 - 13\cdot 4^{1/3}\{\alpha\beta(1-\alpha)(1-\beta)\}^{1/24} + 18\cdot 2^{1/3}\{\alpha\beta(1-\alpha)(1-\beta)\}^{1/12} - 14\{\alpha\beta(1-\alpha)(1-\beta)\}^{1/8} + 2^{5/3}\{\alpha\beta(1-\alpha)(1-\beta)\}^{1/6}).$

**说明。**(i) 本身出自 Schröter [3]、[4]（无证明）；更复杂的 23 次方程见其学位论文 [1] 与论文 [2]。(i) 的证明“decidedly nontrivial”（书中原话），此前未见于印刷品；Berndt 用 (15.1)–(15.11) 给出证明，MACSYMA 验证 $q$ 展开系数到 $q^{18}$。(ii) 由 (i) 经初等代数得到：置 $t = 1 - (\alpha\beta)^{1/8} - \{(1-\alpha)(1-\beta)\}^{1/8}$、$u = \{\alpha\beta(1-\alpha)(1-\beta)\}^{1/8}$，则 $t^3 = 4u$。拉马努金在笔记（p. 249）中给出的 (iii) 的表述似乎有误，上文为 **Berndt 的订正版**。

**状态：** 已证明（书中给出证明；(iii) 为 Berndt 订正的拉马努金笔记表述）。**对照：** M06（模方程）、M11、M14。

**我自验：** 取 $q = 0.5$、$0.2$（mpmath 30 位，theta 路线）：(i)–(iii) 全部通过，差 $\le 4.8\times 10^{-27}$（其中 (iii) 按 Berndt 的订正版验证通过）。

## Entry 16

**陈述。** 设 $\beta$ 为 $\alpha$ 的 19 次模，$m = z_1/z_{19}$。则

**(i)** $((1-\beta)^3/(1-\alpha))^{1/8} - (\beta^3/\alpha)^{1/8} + (\beta^3(1-\beta)^3/(\alpha(1-\alpha)))^{1/8} - 2(\beta^3(1-\beta)^3/(\alpha(1-\alpha)))^{1/16}\{((1-\beta)^3/(1-\alpha))^{1/8} - 1 - (\beta^3/\alpha)^{1/8}\}^{1/2} = m\{\frac12(1 + \sqrt{\alpha\beta} + \sqrt{(1-\alpha)(1-\beta)})\}^{1/2}.$

**(ii)** $(\alpha^3/\beta)^{1/8} - ((1-\alpha)^3/(1-\beta))^{1/8} + (\alpha^3(1-\alpha)^3/(\beta(1-\beta)))^{1/8} - 2(\alpha^3(1-\alpha)^3/(\beta(1-\beta)))^{1/16}\{(\alpha^3/\beta)^{1/8} - 1 - ((1-\alpha)^3/(1-\beta))^{1/8}\}^{1/2} = (19/m)\{\frac12(1 + \sqrt{\alpha\beta} + \sqrt{(1-\alpha)(1-\beta)})\}^{1/2}.$

**说明。**(ii) 是 (i) 的互反形式；两式同时用模形式 (16.1) 证明，MACSYMA 验证 $q$ 展开系数到 $q^{27}$，权 $11/2$，$\rho_{\Gamma} = 10$。此前文献中的 19 次模方程见 Sohncke、Schläfli、Fiedler、Weber、Russell、Fricke，皆不如 (i)(ii) 简洁。

**状态：** 已证明（书中给出证明）。**对照：** M06（模方程）、M11。

**我自验：** 取 $q = 0.5$、$0.2$（mpmath 30 位，theta 路线）：(i)(ii) 差 $\le 5.5\times 10^{-27}$。

## Entry 17

**陈述。** $\varphi$、$\psi$、$f$ 如 Ch. 16 Entry 22（$f(q)$ 为单变量记号，见章首）。则

**(i)** $\varphi(q)\varphi(q^{35}) = \varphi(-q)\varphi(-q^{35}) + 4qf(-q^{10})f(-q^{14}) + 4q^9\psi(q^2)\psi(q^{70}).$

**(ii)** $\varphi(q^5)\varphi(q^7) = \varphi(-q^5)\varphi(-q^7) + 4q^3\psi(q^{10})\psi(q^{14}) - 4q^3f(-q^2)f(-q^{70}).$

**(iii)** $\varphi(q)\varphi(q^{135}) = \varphi(-q^{10})\varphi(-q^{54}) + 2qf(q^9)f(q^{15}) + 2q^4\psi(q^5)\psi(q^{27}).$

**(iv)** $\varphi(q^5)\varphi(q^{27}) = \varphi(-q^2)\varphi(-q^{270}) + 2q^{17}\psi(q)\psi(q^{135}) + 2q^2f(q^3)f(q^{45}).$

**说明。** 证明用 Ch. 16 的 (36.1)(36.2)(36.3)(36.10)、Entry 18(iv)、(7.1) 与式 (17.3)–(17.5)；(iii) 与 (17.1) 等价，(i) 与 Entry 11(i)–(iii)、Entry 12(iv) 有关。

**状态：** 已证明（书中给出证明）。**对照：** M07（theta 函数）、M02。

**我自验：** 取 $q = 0.5$、$0.3$（mpmath 30 位，直接求和；$f(q^9)$ 等按单变量 $f$ 的定义 $\prod_{n\ge 1}(1-(-q)^n)$ 计算）：(i)–(iv) 差 $\le 3.9\times 10^{-31}$。

## Entry 18

**陈述。** 设 $\alpha$、$\beta$、$\gamma$、$\delta$ 的次数依次为 $1$、$5$、$7$、$35$，$m$ 为 $\alpha$–$\beta$ 间的乘子，$m'$ 为 $\gamma$–$\delta$ 间的乘子。则

**(i)** $(\alpha\delta)^{1/4} + \{(1-\alpha)(1-\delta)\}^{1/4} + 2^{4/3}\{\alpha\delta(1-\alpha)(1-\delta)\}^{1/12} + (\beta\gamma)^{1/4} + \{(1-\beta)(1-\gamma)\}^{1/4} + 2^{4/3}\{\beta\gamma(1-\beta)(1-\gamma)\}^{1/12} = 1 + \{1 + 2^{4/3}\{\alpha\beta\gamma\delta(1-\alpha)(1-\beta)(1-\gamma)(1-\delta)\}^{1/24}\}^2.$

**(ii)** $\{(\alpha\delta)^{1/4} + \{(1-\alpha)(1-\delta)\}^{1/4} + 2^{4/3}\{\alpha\delta(1-\alpha)(1-\delta)\}^{1/12}\}\times\{(\beta\gamma)^{1/4} + \{(1-\beta)(1-\gamma)\}^{1/4} + 2^{4/3}\{\beta\gamma(1-\beta)(1-\gamma)\}^{1/12}\} = 1 - 2^{7/3}\{\alpha\beta\gamma\delta(1-\alpha)(1-\beta)(1-\gamma)(1-\delta)\}^{1/24}\times((\alpha\beta\gamma\delta)^{1/8} + \{(1-\alpha)(1-\beta)(1-\gamma)(1-\delta)\}^{1/8}).$

**(iii)** $(\alpha\delta)^{1/4} + \{(1-\alpha)(1-\delta)\}^{1/4} + 2^{4/3}\{\beta\gamma(1-\beta)(1-\gamma)\}^{1/12}(m'/m)^{1/2} = 1.$

**(iv)** $(\beta\gamma)^{1/4} + \{(1-\beta)(1-\gamma)\}^{1/4} - 2^{4/3}\{\alpha\delta(1-\alpha)(1-\delta)\}^{1/12}(m/m')^{1/2} = 1.$

**(v)** $[\{16\beta\gamma(1-\beta)(1-\gamma)\}^{1/24} - \{16\alpha\delta(1-\alpha)(1-\delta)\}^{1/8}]/[\{16\beta\gamma(1-\beta)(1-\gamma)\}^{1/24} + \{16\beta\gamma(1-\beta)(1-\gamma)\}^{1/8}] = (m'/m)^{1/2} = [\{16\alpha\delta(1-\alpha)(1-\delta)\}^{1/8} + \{16\alpha\delta(1-\alpha)(1-\delta)\}^{1/24}]/[\{16\beta\gamma(1-\beta)(1-\gamma)\}^{1/8} - \{16\alpha\delta(1-\alpha)(1-\delta)\}^{1/24}].$

**(vi)** $(\alpha\delta/(\beta\gamma))^{1/8} + ((1-\alpha)(1-\delta)/((1-\beta)(1-\gamma)))^{1/8} - (\alpha\delta(1-\alpha)(1-\delta)/(\beta\gamma(1-\beta)(1-\gamma)))^{1/8} + 2(\alpha\delta(1-\alpha)(1-\delta)/(\beta\gamma(1-\beta)(1-\gamma)))^{1/12} = (m'/m)^{1/2}.$

**(vii)** $(\beta\gamma/(\alpha\delta))^{1/8} + ((1-\beta)(1-\gamma)/((1-\alpha)(1-\delta)))^{1/8} - (\beta\gamma(1-\beta)(1-\gamma)/(\alpha\delta(1-\alpha)(1-\delta)))^{1/8} + 2(\beta\gamma(1-\beta)(1-\gamma)/(\alpha\delta(1-\alpha)(1-\delta)))^{1/12} = -(m/m')^{1/2}.$

**说明。**(iii)(iv) 由 Entry 17(i)(ii) 的转录得到；(i)(ii) 与 (v)–(vii) 由模形式与 theta 恒等式 (18.1)–(18.6) 证明。(vi)(vii) 相乘得 Weber [1] 的方程。

**状态：** 已证明（书中给出证明）。**对照：** M06（模方程）、M11。

**我自验：** 取 $q = 0.5$、$0.2$（mpmath 30 位，theta 路线）：(i)–(vii) 全部通过，差 $\le 3.5\times 10^{-26}$。

## Entry 19

**陈述。** $\varphi$、$\psi$、$f$ 如 Ch. 16 Entry 22（$f(q)$ 为单变量记号，见章首）。则

**(i)** $\varphi(q)\varphi(q^{63}) - \varphi(q^7)\varphi(q^9) = 2qf(q^3)f(q^{21}).$

**(ii)** $\psi(q^7)\psi(q^9) - q^6\psi(q)\psi(q^{63}) = f(-q^6)f(-q^{42}).$

**(iii)** 设 $\beta$、$\gamma$、$\delta$ 的次数依次为 $3$、$13$、$39$；或 $5$、$11$、$55$；或 $7$、$9$、$63$，则

$$\frac{1 + \{(1-\alpha)(1-\delta)\}^{1/4} + (\alpha\delta)^{1/4}}{1 + \{(1-\beta)(1-\gamma)\}^{1/4} + (\beta\gamma)^{1/4}} = \frac{\{(1-\alpha)(1-\delta)\}^{1/8} - (\alpha\delta)^{1/8}}{\{(1-\beta)(1-\gamma)\}^{1/8} - (\beta\gamma)^{1/8}} = \frac{(\alpha\delta)^{1/8} \pm \{\alpha\delta(1-\alpha)(1-\delta)\}^{1/8}}{(\beta\gamma)^{1/8} - \{\beta\gamma(1-\beta)(1-\gamma)\}^{1/8}} = \sqrt{m'/m},$$

其中第三个表达式取 $+$ 号于前两种情形，取 $-$ 号于第三种情形；$m$ 为 $\alpha$–$\beta$ 间的乘子，$m'$ 为 $\gamma$–$\delta$ 间的乘子。

**(iv)** 设 $\beta$、$\gamma$、$\delta$ 的次数依次为 $3$、$13$、$39$；或 $5$、$7$、$35$，则

$$(\alpha\delta/(\beta\gamma))^{1/8} + ((1-\alpha)(1-\delta)/((1-\beta)(1-\gamma)))^{1/8} - (\alpha\delta(1-\alpha)(1-\delta)/(\beta\gamma(1-\beta)(1-\gamma)))^{1/8} + 2(\alpha\delta(1-\alpha)(1-\delta)/(\beta\gamma(1-\beta)(1-\gamma)))^{1/12} = \sqrt{m'/m},$$

且互反一侧的公式等于 $\pm\sqrt{m/m'}$，$+$ 号于第一种情形，$-$ 号于第二种情形。次数为 $5$、$7$、$35$ 时，(iv) 的两式与 Entry 18(vi)、(vii) 相同。

**说明。**(iii) 的第一与第三等式见于拉马努金致 Hardy 的第二封信（文献 [10]，pp. xxix、353）。(i) 的证明：先由 Ch. 17 Entry 11(i)、12(iii) 得 $\varphi(-q^{14})\varphi(-q^{18}) - \varphi(-q^2)\varphi(-q^{126}) = 2q^2f(-q^6)f(-q^{42})$，再以 $-q$ 代 $q^2$ 即得 (i)（代换后 $f(-q^6)$ 变为单变量 $f(q^3)$，见章首记号说明）。(iv) 的证明用模形式，$p = 3$、$q = 13$，$(p+1)(q+1)/16 = 7/2$，$\nu = 8$、$\mu = 28$，MACSYMA 验证 $q$ 展开系数到 $q^{28}$。(iv) 的两式相乘（次数 $3$、$13$、$39$）得 Weber [1] 的方程。

**状态：** 已证明（书中给出证明）。**对照：** M07（theta 函数）、M06（模方程）。

**我自验：** 取 $q = 0.5$、$0.3$（mpmath 30 位，直接求和）：(i) 差 $\le 5.9\times 10^{-31}$（$f(q^3)$、$f(q^{21})$ 按单变量 $f$ 的定义计算；按 $(q^3;q^3)_{\infty}$ 计差约 $0.25$，按 $f(q^3,q^{21})$ 计差 $0.0157$，皆不成立）；(ii) 差 $0$。取 $q = 0.5$、$0.2$（theta 路线）：(iii) 三种情形的三个等式与 (iv) 两种情形的两式全部通过，差 $\le 5.9\times 10^{-31}$。

## Entry 20

**陈述。** 设 $\alpha$、$\beta$、$\gamma$、$\delta$ 的次数依次为 $1$、$n_1$、$n_2$、$n_3 = n_1n_2$，$m$ 为 $\alpha$–$\beta$ 间的乘子，$m'$ 为 $\gamma$–$\delta$ 间的乘子。则

**(i)** $\beta$、$\gamma$、$\delta$ 的次数为 $3$、$21$、$63$；或 $5$、$19$、$95$；或 $11$、$13$、$143$；或 $7$、$17$、$119$；或 $9$、$15$、$135$ 时，

$$\{\frac12(1 + (\alpha\delta)^{1/2} + \{(1-\alpha)(1-\delta)\}^{1/2})\}^{1/2} = (\alpha\delta)^{1/8} + \{(1-\alpha)(1-\delta)\}^{1/8} \pm \{\alpha\delta(1-\alpha)(1-\delta)\}^{1/8} + 2^{4/3}\{\beta\gamma(1-\beta)(1-\gamma)\}^{1/12}\sqrt{m'/m},$$

其中 $\pm$ 号取 $+$ 于前三种情形，取 $-$ 于后两种情形。

**(ii)** $\beta$、$\gamma$、$\delta$ 的次数为 $5$、$19$、$95$；或 $7$、$17$、$119$；或 $11$、$13$、$143$ 时，

$$\{\frac12(1 + (\beta\gamma)^{1/2} + \{(1-\beta)(1-\gamma)\}^{1/2})\}^{1/2} = (\beta\gamma)^{1/8} + \{(1-\beta)(1-\gamma)\}^{1/8} - \{\beta\gamma(1-\beta)(1-\gamma)\}^{1/8} \pm 2^{4/3}\{\alpha\delta(1-\alpha)(1-\delta)\}^{1/12}\sqrt{m/m'},$$

其中 $\pm$ 号取 $-$ 于前两种情形，取 $+$ 于最后一种情形。

**说明。** 证明顺序与陈述相反：先证 (ii)，用 (20.1)–(20.3) 与 Ch. 16 的 (36.8)(36.2)(36.10)，$\mu = 12$，$Q = q^{144-v^2}$，$v = 7$、$5$、$1$；再由此得 (i) 的第二、第四、第三式；(i) 的第一与第五式（次数 $3$、$21$ 与 $9$、$15$，共有一个因子）需另用论证。

**状态：** 已证明（书中给出证明）。**对照：** M06（模方程）、M11。

**我自验：** 取 $q = 0.5$、$0.2$（mpmath 30 位，theta 路线）：(i) 五种情形与 (ii) 三种情形全部通过，差 $\le 4.1\times 10^{-28}$。

## Entry 21

**陈述。** 设 $\alpha$、$\beta$、$\gamma$、$\delta$ 的次数依次为 $1$、$n_1$、$n_2$、$n_3 = n_1n_2$，$m$ 为 $\alpha$–$\beta$ 间的乘子，$m'$ 为 $\gamma$–$\delta$ 间的乘子。则

**(i)** $\alpha$、$\beta$ 的次数为 $1$、$7$；或 $3$、$5$；或 $1$、$15$ 时，

$$(\alpha\beta)^{1/8} + \{(1-\alpha)(1-\beta)\}^{1/8} \pm \{\alpha\beta(1-\alpha)(1-\beta)\}^{1/8} = \{\frac12(1 + \sqrt{\alpha\beta} + \sqrt{(1-\alpha)(1-\beta)})\}^{1/2},$$

其中 $\pm$ 号取 $-$ 于前两种情形，取 $+$ 于最后一种情形。

**(ii)** $\beta$、$\gamma$、$\delta$ 的次数为 $3$、$13$、$39$；或 $5$、$11$、$55$；或 $7$、$9$、$63$ 时，

$$\{(1-\alpha)(1-\delta)\}^{1/8} + ((\beta\gamma)^{1/8} + \{\beta\gamma(1-\beta)(1-\gamma)\}^{1/8})\sqrt{m'/m} = \{\frac12(1 + \sqrt{\alpha\delta} + \sqrt{(1-\alpha)(1-\delta)})\}^{1/2},$$

$$\{(1-\beta)(1-\gamma)\}^{1/8} + ((\alpha\delta)^{1/8} \pm \{\alpha\delta(1-\alpha)(1-\delta)\}^{1/8})\sqrt{m/m'} = \{\frac12(1 + \sqrt{\beta\gamma} + \sqrt{(1-\beta)(1-\gamma)})\}^{1/2},$$

其中第二式的 $\pm$ 号取 $-$ 于前两种情形，取 $+$ 于最后一种情形。

**说明。** Russell [2，p. 388] 曾导出一条类似但更复杂的 15 次模方程。证明用 Ch. 16 的 (36.12)(36.13)，$\mu = 8$，$\omega = 3$ 或 $1$，以及 (7.1)、Entry 18(iv) 与 Ch. 16 Entry 25(i)(ii)。

**状态：** 已证明（书中给出证明）。**对照：** M06（模方程）、M11。

**我自验：** 取 $q = 0.5$、$0.2$（mpmath 30 位，theta 路线）：(i) 三种情形与 (ii) 三种情形的两式全部通过，差 \le 5.8\times 10^{-28}。

## Entry 22

**陈述。** 设 $\beta$ 为 $\alpha$ 的 31 次模。置

$$\Omega(\alpha,\beta) = (\alpha\beta)^{1/32}(\{(1+\sqrt{\alpha})(1+\sqrt{\beta})\}^{1/8}\{1 + (\alpha\beta)^{1/4} + \{(1-\sqrt{\alpha})(1-\sqrt{\beta})\}^{1/2}\}^{1/2} + \{(1-\sqrt{\alpha})(1-\sqrt{\beta})\}^{1/8}\{1 + (\alpha\beta)^{1/4} + \{(1+\sqrt{\alpha})(1+\sqrt{\beta})\}^{1/2}\}^{1/2}).$$

则

**(i)** $\Omega(\alpha,\beta) + \Omega(1-\beta,1-\alpha) = 8^{1/4}.$

**(ii)** $1 + (\alpha\beta)^{1/4} + \{(1-\alpha)(1-\beta)\}^{1/4} - 2((\alpha\beta)^{1/8} + \{(1-\alpha)(1-\beta)\}^{1/8} + \{\alpha\beta(1-\alpha)(1-\beta)\}^{1/8}) = 2\{\alpha\beta(1-\alpha)(1-\beta)\}^{1/16}(1 + (\alpha\beta)^{1/8} + \{(1-\alpha)(1-\beta)\}^{1/8})^{1/2}.$

**(iii)** $1 + (\alpha\beta)^{1/4} + \{(1-\alpha)(1-\beta)\}^{1/4} - (\{\frac12(1 + \sqrt{\alpha\beta} + \sqrt{(1-\alpha)(1-\beta)})\})^{1/2} = (\alpha\beta)^{1/8} + \{(1-\alpha)(1-\beta)\}^{1/8} + \{\alpha\beta(1-\alpha)(1-\beta)\}^{1/8}.$

**说明。**(i) 在第二本笔记（p. 252）中的表述颇为含糊；(i) 与 (iii) 为新结果，(ii) 出自 Russell [1]（见 Greenhill [1，p. 327]）；Schröter 的同类 31 次方程引于正文，Weber、Berry、Hanna 的更复杂。证明按相反顺序进行，先证 (iii)，用 Ch. 16 的 (36.14)，$\mu = 16$，$\omega = 1$，$Q = q^{31}$。

**状态：** 已证明（书中给出证明；(i)(iii) 为新结果，(ii) 为 Russell 的结果）。**对照：** M06（模方程）、M11。

**我自验：** 取 $q = 0.5$、$0.3$（mpmath 30 位，theta 路线；$q = 0.9$ 时 $\alpha\approx 1 - 4\times 10^{-40}$，超出 30 位精度，故改取 $q = 0.5$、$0.3$）：(i)–(iii) 全部通过，差 $\le 6.1\times 10^{-21}$（(i) 在 $q = 0.3$ 处差 $6.1\times 10^{-21}$，为 $\beta\approx 10^{-15}$ 时 $(1-\sqrt{1-\beta})^{1/8}$ 的相对精度极限；$q = 0.5$ 时差 $\le 1.0\times 10^{-27}$）。

## Entry 23

**陈述。** 设 $\beta$ 为 $\alpha$ 的 47 次或 71 次模。则

**(i)** $\beta$ 为 47 次模时，

$$2\{\frac12(1 + \sqrt{\alpha\beta} + \sqrt{(1-\alpha)(1-\beta)})\}^{1/2} = 1 + (\alpha\beta)^{1/4} + \{(1-\alpha)(1-\beta)\}^{1/4} + 4^{1/3}\{\alpha\beta(1-\alpha)(1-\beta)\}^{1/24}(1 + (\alpha\beta)^{1/8} + \{(1-\alpha)(1-\beta)\}^{1/8}).$$

**(ii)** $\beta$ 为 71 次模时，

$$1 + (\alpha\beta)^{1/4} + \{(1-\alpha)(1-\beta)\}^{1/4} - (\{\frac12(1 + \sqrt{\alpha\beta} + \sqrt{(1-\alpha)(1-\beta)})\})^{1/2} = (\alpha\beta)^{1/8} + \{(1-\alpha)(1-\beta)\}^{1/8} - \{\alpha\beta(1-\alpha)(1-\beta)\}^{1/8} + 4^{1/3}\{\alpha\beta(1-\alpha)(1-\beta)\}^{1/24}(1 - (\alpha\beta)^{1/8} - \{(1-\alpha)(1-\beta)\}^{1/8}).$$

**说明。** Berndt 称本条为“拉马努金的只含两个模的模方程的高潮”（the climax of Ramanujan's modular equations involving two moduli only）。47 次方程最早由 Hurwitz 在 Klein [2] 的一篇论文中无证明地给出，带两个符号错误；Russell [1] 订正并证明了它；更复杂的 47 次方程见 Fiedler [1]、Hanna [1]；Fiedler 亦有 71 次方程；较简形式见 Weber [1]、Russell [2]。Russell 的方程 (23.1)（47 次：$(P-2)^2 - P(4R)^{1/3} - 2(4R)^{2/3} - 4R = 0$，其中 $P = 1 + (\alpha\beta)^{1/8} + \{(1-\alpha)(1-\beta)\}^{1/8}$，$R = \{\alpha\beta(1-\alpha)(1-\beta)\}^{1/8}$）与 (23.2)（71 次）由拉马努金的方程平方得到。(i) 的证明用 $47 = 3\cdot 2^4 - 1^2 = 3\cdot 2^5 - 7^2$ 与 Ch. 16 的 (36.14)，$\mu = 48$，$\omega = 7$，$Q = q^{47}$。

**状态：** 已证明（书中给出证明；47 次方程为 Russell 订正并证明的 Hurwitz 方程的拉马努金形式）。**对照：** M06（模方程）、M11。

**我自验：** 取 $q = 0.5$、$0.3$（mpmath 30 位，theta 路线；$q = 0.9$ 时 $\alpha$ 过于接近 1，超出 30 位精度，故改取 $q = 0.5$、$0.3$）：(i)(ii) 差 \le 5.2\times 10^{-28}。

## Entry 24

**陈述。** 设 $\alpha$、$\beta$、$\gamma$、$\delta$ 的次数依次为 $1$、$n_1$、$n_2$、$n_3 = n_1n_2$，其中 $\{n_1,n_2,n_3\}$ 为 $3$、$29$、$87$；$5$、$27$、$135$；$11$、$21$、$231$；$13$、$19$、$247$；$7$、$25$、$175$；$9$、$23$、$207$；$15$、$17$、$255$ 七组之一；$m$ 为 $\alpha$–$\beta$ 间的乘子，$m'$ 为 $\gamma$–$\delta$ 间的乘子。则

**(i)** $\{\frac12(1 + \sqrt{\beta\gamma} + \sqrt{(1-\beta)(1-\gamma)})\}^{1/2} + (\beta\gamma)^{1/8} + \{(1-\beta)(1-\gamma)\}^{1/8} + \{\beta\gamma(1-\beta)(1-\gamma)\}^{1/8} = (1 + (\alpha\delta)^{1/4} + \{(1-\alpha)(1-\delta)\}^{1/4})\sqrt{m/m'}.$

**(ii)** $\{\frac12(1 + \sqrt{\alpha\delta} + \sqrt{(1-\alpha)(1-\delta)})\}^{1/2} + (\alpha\delta)^{1/8} + \{(1-\alpha)(1-\delta)\}^{1/8} \pm \{\alpha\delta(1-\alpha)(1-\delta)\}^{1/8} = (1 + (\beta\gamma)^{1/4} + \{(1-\beta)(1-\gamma)\}^{1/4})\sqrt{m'/m},$

其中 $\pm$ 号取 $-$ 于前四种情形，取 $+$ 于后三种情形。笔记（p. 252）中关于适用符号的说明缺失，符号规则为 Berndt 的整理。

**说明。** (i) 见于拉马努金致 Hardy 的第二封信（文献 [10]，p. 353）。证明用 Ch. 16 的 (36.6)，$\mu = 16$，$v = 13$、$11$、$5$、$3$、$9$、$7$、$1$，$Q = q^{256-v^2}$，以及式 (24.3)；(ii) 的第六种情形的证明引用 Ch. 16 Entry 25(i)(ii)（本章多处证明引用的“Entries 25(i),(ii)”皆指 Ch. 16 Entry 25(i)(ii)，见 Entry 19 说明）。

**状态：** 已证明（书中给出证明；(ii) 的符号规则为 Berndt 的整理，笔记原文缺失该说明）。**对照：** M06（模方程）、M11。

**我自验：** 取 $q = 0.5$、$0.2$（mpmath 30 位，theta 路线）：(i)(ii) 七种情形全部通过，差 \le 4.3\times 10^{-28}。

## 小结

本章共 24 条编号 Entry（Entry 1–24，无缺号），分体标题 129 个；书页 325–453（129 页）。要点如下：

- 引言（第 0 节）为全章的理论准备：混合模方程的定义、二十组次数三元组、模形式理论（赋值公式、乘子系统、Dedekind $\eta$ 函数、$G(m;z)$）与定理 0.9（Evans 对 Ch. 19 定理 12.1 的推广）。
- Entry 1–2 为 3、9 次 theta 恒等式：Entry 1 的 $v$ 连分数与 $\psi/\varphi$ 公式（(i) 的第一式见于致 Hardy 的第二封信；(1.3) 的连分数亦见第三本笔记）；Entry 2 的九条 9 次恒等式（(v) 的 $f(-q^{1/3})$ 三分组、(vi) 的乘积恒等式、(vii)(viii) 的比值恒等式；(viii) 第一项分母经 300 DPI 确认为 $f(-q,-q^8)$）。
- Entry 3–5 为 3、9、27 次模方程：Entry 3 的十六条（(vii)–(ix) 本身是 3 次方程；参数化 (3.1)–(3.5)）；Entry 4 的四条 theta 恒等式（(i)(ii) 为 Entry 3(x)(xi) 的转录）；Entry 5 的四条 27 次方程（(iv) 的印文缺两个因子 $16$，见待核对清单）。
- Entry 6–8 为 11、13 次：Entry 6 的三条 11 次 theta 恒等式（(iii) 为 Ch. 19 定理 12.1 的 $n = 11$ 情形）；Entry 7 的七条 11 次模方程（(i) 为 Schröter 1858 年的结果；(7.1) 的第二变元为 $a^5b^3$；(viii)(ix) 已被拉马努金本人划去）；Entry 8 的 13 次恒等式与模方程（(8.1) 为定理 12.1 的 $n = 13$ 情形；(8.2) 用 Evans 定理 8.1；(iii)(iv) 的 $m$ 与 $13/m$ 公式）。
- Entry 9–11 为 15 次：Entry 9 的七条 theta 恒等式；Entry 10 的六条（(v)(vi) 的 Lambert 级数系数周期 30、60，拉马努金原文只写了前几项）；Entry 11 的十五条 3、5、15 次模方程（(i) 与 (ii) 之积及 (xiv) 见于致 Hardy 的第二封信；(vi) 为 Hardy 记录的公式经 Berndt 订正符号后的版本；(viii) 与 (ix) 相乘得 Weber 的方程）。
- Entry 12 为 17 次：(12.1) 为定理 12.1 的 $n = 17$ 情形；(12.3) 用 Rogers–Hecke–Andrews–Bressoud–Kac–Peterson 的 (12.4)；(iii)(iv) 的 $m$ 与 $17/m$ 公式；末尾 N.B. 注记的大部分表述尚无合理解释。
- Entry 13–16 为 21、33、23、19 次：Entry 13 的六条 3、7、21 次方程（(ii)(iv)(vi) 为互反形式）；Entry 14 的两条 3、11、33 次方程；Entry 15 的三条 23 次方程（(i) 为 Schröter 的结果，证明此前未见于印刷品；(iii) 为 Berndt 订正的拉马努金笔记表述）；Entry 16 的两条 19 次方程（带平方根因子的 $m$ 与 $19/m$ 公式）。
- Entry 17–19 为 35、63 次：Entry 17 的四条 35、135 次 theta 恒等式；Entry 18 的七条 5、7、35 次方程（(iii)(iv) 由 Entry 17(i)(ii) 转录；(vi)(vii) 相乘得 Weber 的方程）；Entry 19 的四条（(i)(ii) 的 63 次 theta 恒等式，$f(q^3)$ 为单变量 $f$；(iii)(iv) 的 39、55、63、35 次方程；(iii) 的第一与第三等式见于致 Hardy 的第二封信）。
- Entry 20–24 为高次与合数次的收束：Entry 20 的 63、95、119、135、143 次方程（(i) 五种情形、(ii) 三种情形）；Entry 21 的 7、15 次与 39、55、63 次方程；Entry 22 的 31 次方程（$\Omega$ 函数；(ii) 为 Russell 的结果）；Entry 23 的 47、71 次方程（Berndt 称之为“拉马努金的只含两个模的模方程的高潮”）；Entry 24 的七组高次合数次方程（87、135、143、175、207、231、247、255；(i) 见于致 Hardy 的第二封信；(ii) 的符号规则为 Berndt 的整理）。

数值复核：368 项数值检查中 361 项差 $< 1\times 10^{-25}$（mpmath 30 位，直接求和 + 解析尾项；模方程用 $\alpha(q) = (\theta_2/\theta_3)^4$ 的 theta 路线，$\theta_2 = 2q^{1/4}\psi(q^2)$、$\theta_3 = \varphi(q)$，$m = \varphi^2(q)/\varphi^2(q^n)$），3 项为已解释的精度伪影（Entry 5(ii) 在 $q = 0.5$ 处差 $1.9\times 10^{-25}$、Entry 13(i) 在 $q = 0.5$ 处差 $1.4\times 10^{-25}$，皆为 $\alpha\approx 0.99999$ 时 $1-\alpha\approx 10^{-5}$ 的相对精度极限，$q = 0.2$ 时差 $\le 2.0\times 10^{-28}$；Entry 22(i) 在 $q = 0.3$ 处差 $6.1\times 10^{-21}$，为 $\beta\approx 10^{-15}$ 时 $(1-\sqrt{1-\beta})^{1/8}$ 的相对精度极限，$q = 0.5$ 时差 $\le 1.0\times 10^{-27}$），2 项为 Entry 5(iv) 印文版的不成立（见下），另有 2 项为 (7.1) 的反面验证（按 $a^4b^4$ 读法差 $3.4\times 10^{-4}$、$2.4\times 10^{-3}$，反证正确读法为 $a^5b^3$）。本轮新发现的原书印文问题一处：Entry 5(iv) 的两个 $1/8$ 次项内各缺因子 $16$（按印文版，$q = 0.5$ 时差 $0.077321$、$q = 0.2$ 时差 $0.063222$；按证明版差 $\le 1.0\times 10^{-30}$；书中证明（书页 362）所用的亦为带 $16$ 的版本）。另有转录注意三处：Entry 2(viii) 第一项分母为 $f(-q,-q^8)$（300 DPI 确认）、(7.1) 的第二变元为 $a^5b^3$（300 DPI 确认）、Entry 17(iii)(iv) 与 Entry 19(i) 的 $f(q^3)$ 等为单变量 $f$（按 $(q^3;q^3)_{\infty}$ 或 $f(q^3,q^{21})$ 读法皆不成立）。拉马努金原文疏失已按 Berndt 注明：Entry 7 的 (viii)(ix) 已被拉马努金本人划去、Entry 15(iii) 的笔记表述有误（Berndt 已订正）、Entry 24(ii) 的符号说明在笔记中缺失（Berndt 已整理）、Hardy 在 Entry 11(vi) 中有两个符号错误（Berndt 已订正）、Hurwitz 的 47 次方程带两个符号错误（Russell 已订正）。

## 待核对清单

- Berndt 章首计数：本章导言（p. 325）未给出本章公式或定理陈述的总数。
- Entry 5(iv) 的印文问题：书中印为 $[\{16\beta\gamma(1-\beta)(1-\gamma)\}^{1/24} + \{\alpha\delta(1-\alpha)(1-\delta)\}^{1/8}]/[\{16\beta\gamma(1-\beta)(1-\gamma)\}^{1/24} + \{\beta\gamma(1-\beta)(1-\gamma)\}^{1/8}]$，两个 $1/8$ 次项内无因子 $16$；书中证明（书页 362）所用的却是带 $16$ 的版本，并由此推出 $(256\alpha^3(1-\alpha)^3\delta^3(1-\delta)^3/(\beta(1-\beta)\gamma(1-\gamma)))^{1/24}$ 的等式；数值复核：按印文版，$q = 0.5$ 时差 $0.077321$、$q = 0.2$ 时差 $0.063222$，按证明版差 $\le 1.0\times 10^{-30}$；待查 Berndt 勘误。
- Entry 2(viii) 第一项分母：150 DPI 原图上易误读为 $f(-q^2,-q^8)$，300 DPI 放大图（PDF 页 363）确认确为 $f(-q,-q^8)$；按 $f(-q^2,-q^8)$ 计，$q = 0.5$ 时差 $0.61$、$q = 0.3$ 时差 $0.33$；证明的代数亦支持 $f(-q,-q^8)$；此处仅记录转录细节。
- (7.1) 的第二变元：书中印为 $(a/b)a^4b^4$（即 $a^5b^3$），300 DPI 放大图（PDF 页 365）确认；按字面 $a^4b^4$ 计，$a = 0.3$、$b = 0.5$ 时差 $3.4\times 10^{-4}$，$a = 0.2$、$b = 0.7$ 时差 $2.4\times 10^{-3}$；此处仅记录转录细节。
- Entry 17(iii)(iv) 与 Entry 19(i) 的单变量 $f$：$f(q^3)$、$f(q^9)$、$f(q^{15})$、$f(q^{21})$、$f(q^{45})$ 按 Ch. 19 文件已确认的单变量 $f$ 定义 $f(q) = f(q,-q^2) = \prod_{n\ge 1}(1-(-q)^n)$ 理解时，Entry 17(iii)(iv) 差 $\le 3.9\times 10^{-31}$、Entry 19(i) 差 $\le 5.9\times 10^{-31}$；按 $(q^3;q^3)_{\infty}$ 计 Entry 19(i) 差约 $0.25$，按 $f(q^3,q^{21})$ 计差 $0.0157$；Entry 19(i) 的证明（以 $-q$ 代 $q^2$ 的代换）亦支持单变量 $f$ 的读法；此处仅记录转录细节。
- Entry 12 末尾 N.B. 注记：拉马努金关于 $\varphi(x^{1/n})$、$\psi(x^{1/n})$、$f(-x^{1/n})$ 与 $f^3(-x^{1/n})$ 的 $n$ 次根表述（二次只在 5、17、257 次，三次在 7、13、19、37、73、97、109、163、193 次，五次在 11、41、101 次），Berndt 注明大部分表述尚无合理解释；待查后续文献。
- Entry 15(iii) 的拉马努金笔记表述：Berndt 注明笔记（p. 249）的表述似乎有误，上文为 Berndt 的订正版；笔记原文的误印细节未逐字核对。
- Entry 24(ii) 的符号规则：笔记（p. 252）中关于适用符号的说明缺失，符号规则（前四种情形取 $-$、后三种取 $+$）为 Berndt 的整理；数值复核在七种情形下全部通过。
- Entry 22(i) 在 $q = 0.3$ 处的差 $6.1\times 10^{-21}$：已定位为 $\beta\approx 10^{-15}$ 时 $(1-\sqrt{1-\beta})^{1/8}$ 的相对精度极限（$q = 0.5$ 时差 $\le 1.0\times 10^{-27}$）；公式本身无误，此处仅记录数值复核的精度细节。
- Entry 5(ii) 与 Entry 13(i) 在 $q = 0.5$ 处的差 $1.9\times 10^{-25}$、$1.4\times 10^{-25}$：已定位为 $\alpha\approx 0.99999$ 时 $1-\alpha\approx 10^{-5}$ 的相对精度极限（$q = 0.2$ 时差 $\le 2.0\times 10^{-28}$）；公式本身无误，此处仅记录数值复核的精度细节。
- TIFR 1957 年影印版的笔记页码：本章各 Entry 的 TIFR 页码未逐条核对（Berndt 在本章引用的笔记页码见书中各节注记，如 Entry 7 的 (viii)(ix) 划去见笔记 p. 244、Entry 10(v)(vi) 见笔记 p. 245、Entry 15(iii) 见笔记 p. 249、Entry 22(i) 与 Entry 24 见笔记 p. 252）。
- 本章条目总数未见于其他目录核对；以书中编号 Entry 1–24 为准。

## 来源说明

- 整理层：Bruce C. Berndt，《Ramanujan's Notebooks》，Part III，Springer，1991，Ch. 20，书页 325–453（正文）；参考文献自书页 489 起，索引自书页 505 起。
- 电子版：archive.org 标识符 `ramanujan_notebooks_iii`（《Ramanujan's Notebooks, Part 3》，Springer 1991，XIII + 510 页，DOI **10.1007/978-1-4612-0965-2**；PDF 21,002,730 字节、524 叶，md5 `de9211b0bde03dd9255145d3f09bb78f`），**PDF 页 = 书页 + 14**（与 Part II 的 +12 不同）。本章为 PDF 页 339–467（书页 325–453）；PDF 页 468 起为 Ch. 21（书页 454）。
- 转录方法：全部公式按 PDF 原图（150 DPI，书页 325–453）逐字转录；关键公式另用 300 DPI 放大图确认：(7.1)（PDF 页 365）、Entry 2(viii)（PDF 页 363）、Entry 5(iv) 的陈述（PDF 页 374）与证明（PDF 页 376）、Entry 19(i)–(iii)（PDF 页 440）；OCR（DjVu 文本层）只作检索索引，公式凡与原图或数值不符者一律纠正。
- 数值复核：mpmath 30 位，直接求和 + 解析尾项（$q$-Pochhammer 乘积截断到 1500 项、theta 双边和截断到 $\pm 120$ 项；模方程用 $\alpha(q) = (\theta_2/\theta_3)^4$ 的 theta 路线，$\theta_2 = 2q^{1/4}\psi(q^2)$、$\theta_3 = \varphi(q)$，$m = \varphi^2(q)/\varphi^2(q^n)$；$q = 0.9$ 时 $\alpha\approx 1 - 4\times 10^{-40}$ 超出 30 位精度，故 Entry 22、23 改取 $q = 0.5$、$0.3$）；368 项检查中 361 项差 $< 1\times 10^{-25}$，另有三处已解释的精度伪影与一处已确认的印文问题（见小结）；慢收敛级数一律不用 `nsum`。
- 章名与目录：以原书目录为准，Ch. 20 为 "Modular Equations of Higher and Composite Degrees"；上一章 Ch. 19 为 "Modular Equations of Degrees 3, 5, and 7 and Associated Theta-Function Identities"（书页 220–324）；下一章 Ch. 21 为 "Eisenstein Series"（书页 454 起）。
- 参考文献（书中引用，本章出现者）：Andrews [1]、Berndt–Biagioli–Purtilo [1][2][3]、Berry [1]、Biagioli [2]、Borwein, J. M. 与 P. B. [2]、Bressoud [1]、Evans [1]、Fiedler [1][2]、Fricke [1]、Greenhill [1]、Hanna [1]、Hardy [1][3][10]、Hecke [1]、Hurwitz（见 Klein [2]）、Kac–Peterson [1]、Klein [1][2]、Ramanathan [1]、Rogers [1]、Russell [1][2]、Schläfli [1]、Schröter [1][2][3][4]、Sohncke [1][2]、Watson [4]、Weber [1]、Berndt [3][9]。
