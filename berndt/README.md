# Berndt 整理本 · 学术整理与证明

本目录按 **Bruce C. Berndt 的五卷整理本**组织，把三本早期笔记的全部公式逐条整理到这里。

## 两层来源，先分清

| 层 | 出版物 | 性质 |
|---|---|---|
| 原文层 | Srinivasa Ramanujan, *Notebooks*（2 卷），Tata Institute of Fundamental Research（TIFR），孟买，1957 年；2011 年 TIFR 再版两卷 Collector's Edition | **手稿影印版**，无整理、无注释、无证明：就是拉马努金本人手写的影印件 |
| 整理层 | Bruce C. Berndt, *Ramanujan's Notebooks*, Parts I–V，Springer，1985–1998 | **学术整理本**：逐条编号、注释，并为全部条目给出证明或引出文献证明 |

也就是说：TIFR 出的是原文影印，Berndt 出的是整理与证明。本目录按 Berndt 五卷的结构逐条填，公式出处同时标 TIFR 影印版的笔记位置与 Berndt 卷的章、Entry 号。

## 三本笔记的物理结构

- **第一本笔记**：351 页，16 个有组织的章节 + 未组织的散页（其中 198 页未组织内容见 Part V）。
- **第二本笔记**：256 页，21 章 + 约 100 页未组织内容；是第一本的修订扩充版。
- **第三本笔记**：33 页未组织内容。
- Berndt 自 1977 年起整理，历时 20 余年，**共数出 3,254 条结果**（Berndt 2019 年自述）。

## 五卷结构总表

| 卷 | 年份 | 覆盖范围 | 章节 | 状态 |
|---|---|---|---|---|
| Part I | 1985 | 第二本笔记第 1–9 章 + Quarterly Reports | Ch. 1 Magic Squares（幻方）；Ch. 2 Sums Related to the Harmonic Series or the Inverse Tangent Function；Ch. 3 Combinatorial Analysis and Series Inversions；Ch. 4 Iterates of the Exponential Function and an Ingenious Formal Technique；Ch. 5 Eulerian Polynomials and Numbers, Bernoulli Numbers, and the Riemann Zeta-Function；Ch. 6 Ramanujan's Theory of Divergent Series；Ch. 7 Sums of Powers, Bernoulli Numbers, and the Gamma Function；Ch. 8 Analogues of the Gamma Function；Ch. 9 Infinite Series Identities, Transformations, and Evaluations | Ch. 1 已填（见 part-1-chapter-1-magic-squares.md：Entry 6 (i)(ii) 已核对 + 第 1–8 节构造与例题；Entry 1–5 编号待核对），Ch. 2 已填（见 part-1-chapter-2-harmonic-series-arctan.md：Entry 1–12，φ(2)/φ(3)/φ(4)/φ(6) 四推论与 Entry 6、Entry 7 已核对；(3.1)–(3.3)、(4.1)(4.2)、(5.1)、(11.1) 等确切形式待核对），Ch. 3 已填（见 part-1-chapter-3-combinatorial-analysis-series-inversions.md：Entry 1–17 全收；Entry 10 通用渐近展开、Entry 13 Lagrange 反演中心、Entry 15 例 1 的范围订正已核对；待核对八项详见该文件末尾），Ch. 4 已填（见 part-1-chapter-4-iterates-exponential-formal-technique.md：Entry 1–8、Entry 10–15 全收，无 Entry 9；Entry 11 主定理推广形式为本章中心；第 9 节推论 2 在 $n > 2$ 时已否定；待核对九项详见该文件末尾），Ch. 5 已填（见 part-1-chapter-5-eulerian-bernoulli-zeta.md：Entry 1–30 全收；Bernoulli 数定义 (I1) 即 M01 缺失的定义出处；Entry 19(ii) 加强断言与 Entry 29、Entry 30 后推论 3 已否定；待核对九项详见该文件末尾），Ch. 6 已填（见 part-1-chapter-6-divergent-series.md：Entry 1–4、Entry 6–12、Entry 14–17 全收，无 Entry 5、Entry 13；Entry 1 的常数 $c$ 与 $1+2+3+\cdots = -1/12$ 为本章中心；第 5 节例 3 的 (5.8) 不成立、Entry 12 的界断言已否定；待核对九项详见该文件末尾），Ch. 7–9 待填 |
| Part II | 1989 | 第二本笔记第 10–15 章 | Ch. 10 Hypergeometric Series, I；Ch. 11 Hypergeometric Series, II；Ch. 12 Continued Fractions；Ch. 13 Integrals and Asymptotic Expansions；Ch. 14 Infinite Series；Ch. 15 Asymptotic Expansions and Modular Forms | 待填 |
| Part III | 1991 | 第二本笔记第 16–21 章 | Ch. 16 q-Series and Theta-Functions；Ch. 17 Fundamental Properties of Elliptic Functions；Ch. 18 The Jacobian Elliptic Functions；Ch. 19 Modular Equations of Degrees 3, 5, and 7 and Associated Theta-Function Identities；Ch. 20 Modular Equations of Higher and Composite Degrees；Ch. 21 Eisenstein Series | 待填 |
| Part IV | 1994 | 第二本笔记 100 页未组织内容 + 第三本笔记 33 页未组织内容 + 第一本笔记 16 章 | Ch. 22 Elementary Results；Ch. 23 Number Theory；Ch. 24 Ramanujan's Theory of Prime Numbers；Ch. 25 Theta-Functions and Modular Equations；Ch. 26 Inversion Formulas for the Lemniscate and Allied Functions；Ch. 27 q-Series；Ch. 28 Integrals；Ch. 29 Special Functions；Ch. 30 Partial Fraction Expansions；Ch. 31 Elementary and Miscellaneous Analysis | 待填 |
| Part V | 1998 | 第二、三本笔记剩余 133 页未组织内容 + 第一本笔记 198 页未组织内容 | Ch. 32 Continued Fractions；Ch. 33 Ramanujan's Theories of Elliptic Functions to Alternative Bases；Ch. 34 Class Invariants and Singular Moduli；Ch. 35 Values of Theta-Functions；Ch. 36 Modular Equations and Theta-Function Identities in Notebook 1；Ch. 37 Approximations and Asymptotic Expansions；Ch. 38 Miscellaneous Results in the First Notebook | 待填 |

注：Part V 年份部分书目著录为 1997 年 12 月；各卷条目数待逐卷核对原书目录后补（总计 3,254 条已核实）。

## 填写进度

- **Part I Ch. 1 Magic Squares**（2026-11-05，已填）：part-1-chapter-1-magic-squares.md，178 行。内容：8 节全收；正式编号的 Entry 只有 Entry 6 (i)(ii)（pp. 20–21，已核对）；第 1–5 节的一般构造暂记 Entry 1–5，编号待核对（p. 17 原文未能直接读取）；第 7–8 节为应用与例题，无新 Entry。待核对五项：Entry 1–5 编号、p. 17 全文、Entry 6(i) 恒等式的确切表述、Entry 5 条件式中的 $3D$、生日幻方在本章的位置。下一章：Part I Ch. 2。
- **Part I Ch. 2 Sums Related to the Harmonic Series or the Inverse Tangent Function**（2026-11-06，已填）：part-1-chapter-2-harmonic-series-arctan.md，270 行。内容：Entry 1–12 全收（编号均在原文明确出现）；φ(2)=2log2、φ(3)=log3、φ(4)=(3/2)log2、φ(6)=(1/2)log3+(1/3)log4 四推论与 Entry 6（H_{A_r}−H_n 双重和、H_{1000} 估计）、Entry 7（拉马努金反正切和、Σ arctan(1/(2k²))=π/4）已核对并数值复核通过（mpmath 30 位）；Entry 12 的六个根与渐近分数已数值复核通过；两个错误断言（Entry 6 等差数列倒数和近似、Entry 12 mediant 逼近）已按 Berndt 的反例标已否定。待核对十项：(3.1)–(3.3)、(4.1)(4.2)、(5.1)、(11.1) 等的确切形式，Entry 5 例 4/8/9/10、Entry 7 例 2/3/5–8、Entry 8 表述、Entry 9 推论 3/4 与例 1/2、Entry 10 四式、Entry 6 的 A_k 定义式原文与 (6.2) 数值、Entry 12 例 2 的方程原表述（详见该文件末尾「待核对清单」）。
- **Part I Ch. 3 Combinatorial Analysis and Series Inversions**（2026-11-06，已填）：part-1-chapter-3-combinatorial-analysis-series-inversions.md，619 行。内容：Entry 1–17 全收（编号均在原文明确出现）；前半 Bell 多项式理论（Entry 1–9、第 8 节例 1–6：$f_n(x)$、Stirling 数、Bell 数 $A_n$/$C_n$、$F_n(a,b;x)$）与后半级数反演（Entry 10 通用渐近展开、Entry 11 Newton 恒等式、Entry 12–14 Lagrange 反演、Entry 15、Entry 16、Entry 17）已核对并数值复核通过（mpmath 30 位，本轮 34 项 + 前期 20 余项）；四处拉马努金原文错误已按 Berndt 纠正（第 8 节例 4、Entry 9 例 (iii)(iv)、Entry 15 例 1 的 $0<n\le 2$ 范围、Entry 17 (17.5) 末项）；OCR 误读纠正 8 处（(3.1) 的 $\psi$、(12.1) 底数 $(n+k)$、$\Delta^n C_0$ 下标、Entry 9(vii) 的 $e^{(a+b)x}$、(9.6) 的 $F_3$ 系数、(10.6)(10.7) 下标、$A_r$ 指数、Entry 13 的 $f'(n)$ 指数待核对）。待核对八项：Entry 10「三个应用」与例 1–4 的对应、Entry 13 的 $f'(n)$ 第一求和指数、Entry 15 例 2 的 $y$ 定义印文、例 4(iv) 的 $x+u$、Entry 16 推论 1 (16.7) 的文献细节、Entry 17 例 2 的 $A_k$ 参数、TIFR 影印版页码、(10.9)–(10.11) 逐项数值复核（详见该文件末尾「待核对清单」）。
- **Part I Ch. 4 Iterates of the Exponential Function and an Ingenious Formal Technique**（2026-11-06，已填）：part-1-chapter-4-iterates-exponential-formal-technique.md，403 行。内容：Entry 1–8、Entry 10–15 全收（编号均在原文明确出现；**第 9 节无 Entry 9**，只有例题 1–4 与推论 1–2）；前半指数函数迭代（Entry 1–2 的 $F_r(x)$ 与 $\varphi_k(r)$、Entry 3 的 Bernoulli 展开、Entry 4 与 Entry 6 的 $\psi_k(n)$ 递推与显式公式、Entry 5 的函数方程、Entry 7 的 $F_{2r}$ 展开、Entry 8 的调和数幂和）与后半形式技巧（第 9 节留数定理重证的例 1–3 与例 4、Entry 10 二项对称和与指数积分三版、Entry 11 主定理推广形式与推论 1–5、Entry 12 Fourier 余弦反演、Entry 13 Beta 型积分、Entry 14 无穷乘积、Entry 15 奇数倒数和）已核对并数值复核通过（mpmath 30 位 + 精确分数，约 70 项）；拉马努金原文疏失四处已按 Berndt 注明（$f_1(x)$ 被暗示为 7 次多项式、第 9 节推论 2 在 $n > 2$ 时不成立、Entry 11 的推导纯形式未真正证明、Entry 10 推论的条件极少满足）；OCR 公式损坏严重，全部公式按 PDF 原图（150 DPI，书 pp. 85–108）逐字转录并纠正。待核对九项：IMSC 本章结果数（当日不可达）、推论 2 在 $n = 2$ 时是否成立、Entry 11 推论 4 与 Entry 12 的季报证明、Entry 12(i) 的振荡积分数值方法、Entry 7 余项、$\psi_7(1) = -11/120960$（导出值）、TIFR 影印版页码、(10.9)–(10.11) 逐项数值复核（详见该文件末尾「待核对清单」）。下一章：Part I Ch. 5。
- **Part I Ch. 5 Eulerian Polynomials and Numbers, Bernoulli Numbers, and the Riemann Zeta-Function**（2026-11-06，已填）：part-1-chapter-5-eulerian-bernoulli-zeta.md。内容：Entry 1–30 全收（编号均在原文明确出现；Berndt 章首计数本章共 94 条公式或定理陈述）；前半 Eulerian 多项式与数理论（Entry 1–8：差分方程系数、(0.1) 定义、递推 (5.1)(5.2)、Entry 6 三恒等式、Entry 7 对数展开、Entry 8 的 $\psi_n(-1)$、$\psi_n(1)$ 与 $\psi_0,\dots,\psi_7$ 及推论 1–6）与中段 Bernoulli 数经典理论（Entry 9 定义 (I1)、Entry 11–17 的对数与三角级数、Entry 18 Euler 递推、Entry 19–20 的 von Staudt–Clausen 定理、Entry 21 两张素数表、Entry 22 的 $B$–$E$ 恒等式、Entry 23–24 的部分分式分解）与后半 zeta 函数与 Euler 乘积（Entry 25 的 $\zeta(2n)$ 等 Euler 公式与 $B_s^*$、$E_s^*$ 推广、Entry 26 的渐近与 $\zeta(n)$ 数值表、Entry 27–28 的 Euler 乘积、Entry 29、Entry 30）已核对并数值复核通过（mpmath 30 位 + 精确分数，37 项检查全部通过）；拉马努金原文疏失八处已按 Berndt 注明（Entry 6(ii) 笔记表述有误、Entry 7 (7.2) 取整说法含糊、例 1 右端 $-1/2$ 应为 $1/2$、Entry 19(ii) 加强断言不成立、Entry 20 例 1 推理有误、Entry 29 被划去、Entry 30 后推论 3 被划去、$\zeta(n)$ 表五处末位错）；OCR 公式损坏严重，全部公式按 PDF 原图（150 DPI，书 pp. 109–132）逐字转录并纠正。待核对九项：IMSC 本章结果数（当日不可达）、Entry 23/24 确切表述（Berndt 未印公式，只引 Bromwich）、Entry 21 第二张表排版、Entry 7 (7.2) 的含义、$I_0 = 0$ 的约定、$B_{200}$ 分数部分的两种写法、推论 2 极限值的补充注记、TIFR 影印版页码、Entry 29 Ramanujan 对的 1985 年后进展（详见该文件末尾「待核对清单」）。下一章：Part I Ch. 6。
- **Part I Ch. 6 Ramanujan's Theory of Divergent Series**（2026-11-06，已填）：part-1-chapter-6-divergent-series.md，477 行。内容：Entry 1–4、Entry 6–12、Entry 14–17 全收（编号均在原文明确出现；**无 Entry 5**——第 5 节只有例题 1–6；**无 Entry 13**——第 13 节只有例题 (a)、(b1)、(b2)、(c) 与例题 1–3）；前半发散级数理论基础（Entry 1 的 Euler–Maclaurin 特例 (1.1) 与级数的常数 $c$、例 2 的 $1+2+3+\cdots = -1/12$、Entry 3 的 $\varphi(x)$ 定义、Entry 4 的分数项数和与公式 (4.1)）与中段展开与警示（第 5 节的「修正」级数与 $S_n(x)$、Entry 6 的 $\varphi(x)$ 幂级数展开、Entry 7 的尺度变换与推论 2、Entry 10 的「正则」级数警示、Entry 11 的 Euler 级数变换、Entry 12 的界断言被否定与 Diamond 修正定理）与后半应用与恒等式（第 13 节的加速收敛、Entry 14 的带余项界有限展开与四个数值应用、Entry 15 的 Clausen 恒等式、Entry 16–17 的分式级数恒等式与除数函数推论）已核对并数值复核通过（mpmath 30 位 + 精确分数，约 39 项检查全部通过）；拉马努金原文疏失五处已按 Berndt 注明（第 5 节例 3 的 (5.8) 在 (5.6) 定义下连渐近都不成立、例 6 误印 4 应为 $2\sqrt{2}$、推论 2(v) 误印 $c_4'$ 应为 $c_6'$、Entry 12 界断言不成立、Entry 14 例 1 自称的 $-0.4909100$ 精度无法从 (14.5) 得到）；OCR 公式损坏严重，全部公式按 PDF 原图（150 DPI，书 pp. 133–149）逐字转录并纠正，(4.1) 的上限 $n$ 另用 300 DPI 放大图确认。待核对九项：IMSC 本章结果数（当日不可达）、Entry 2/Entry 8 确切表述（Berndt 未印公式）、Entry 9 的记号、Entry 10(ii) 第三式的推导、第 5 节例 3 (5.8) 在 (5.11) 定义下的完整验证、Entry 12 第三例与 Diamond 定理的引文、第 13 节例 2 的 $\cot(\pi x)$ 分解确切形式、TIFR 影印版页码、Entry 14 例 1 (14.5) 的独立重算（详见该文件末尾「待核对清单」）。下一章：Part I Ch. 7。

## 收录规则（与全仓库一致）

- 每条按 **Berndt 的 Entry 编号**收录：公式陈述 + 出处（卷、章、Entry 号）+ 状态（已证明 / 后人补证 / 未解决）。
- **不照抄 Berndt 的正文与证明**（Springer 整理本受版权保护）：证明只写自写思路或文献指引。
- 每条注明与主题模块 M01–M14 的对应关系，互链、不去重。
- 填法：一章一批，说「继续」就填下一章；每章填完浏览器抽查渲染。

## 失落笔记（另线，不在此表）

失落笔记的影印版是 Narosa 出版社 1987/1988 年出的，不属 TIFR；学术整理是 Andrews 与 Berndt 的《Ramanujan's Lost Notebook》五卷（Springer，2005、2009、2012、2013、2018），约 650 条，其中 Part I 考证 442 条。是否也按此方式逐条填，等 Zhang 定。

## 参考文献

- Bruce C. Berndt, *Ramanujan's Notebooks*, Parts I–V, Springer, 1985–1998.
- Bruce C. Berndt, "Living with Ramanujan for 40 years", *Phil. Trans. R. Soc. A* 378 (2019) 20180437（3,254 条的计数出处）。
- Srinivasa Ramanujan, *Notebooks* (2 vols.), Tata Institute of Fundamental Research, Bombay, 1957；Collector's Edition, TIFR, 2011.
- George E. Andrews & Bruce C. Berndt, *Ramanujan's Lost Notebook*, Parts I–V, Springer, 2005–2018.
