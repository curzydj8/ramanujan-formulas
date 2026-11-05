# Eisenstein and Modular Series · AIMER 站公式提取

分类页：https://ramanujan.aimersociety.com/discoveries/category/eisenstein-modular-series

7 条中 **5 条有公式，2 条无单一公式**。提取自本站 Next.js 数据 chunk（/_next/static/ 下 JS chunk 内含全部 177 条的 KaTeX 原始源码）；chunk 中有公式字段的条目对应站内公式面板、无公式字段的条目对应站内 contribution-family 声明，此对应关系已在前几轮（Partition Theory、Mock Theta Functions、Formulas for pi）经实况浏览器逐条验证一致。本分类未做实况浏览器抽查复核——但已用条目页静态 HTML 逐页核对：有公式的条目页 HTML 中含与 chunk 相同的公式源码且含「Formula permalink」与「Copy LaTeX」按钮、无 contribution-family 字样；无公式的条目页 HTML 中含完整 contribution-family 声明。本站只收公式，解说不抄；站内条目多为 needs-review，公式须与 Berndt 五卷核对后才标「已核对」。

## 1. Ramanujan Differential Equations

来源：https://ramanujan.aimersociety.com/discoveries/ramanujan-differential-equations

$$q\frac{dE_2}{dq}=\frac{E_2^2-E_4}{12}$$

状态：已提取待核对；站内类型 formula，难度 Advanced，年份未注明，needs-review，Original Source 为编辑目录条目。**M01–M14 未收的新增形式**：拉马努金微分方程组在 M01–M14 及仓库其他文件中均无收录（M06.2 只收 Eisenstein 级数的定义与 Fourier 展开，未收微分方程组）。注意：本站本条只给三元方程组中的第一式；第二式见本分类第 7 条；第三式（$E_6$ 的方程）本站未给出。站内未注明 $q$ 的定义与收敛条件，待核对。

## 2. Eisenstein Series E2

来源：https://ramanujan.aimersociety.com/discoveries/eisenstein-series-e2

$$E_2(q)=1-24\sum_{n=1}^{\infty}\sigma_1(n)q^n$$

状态：已提取待核对；站内类型 series，难度 Advanced，年份未注明，needs-review，Original Source 为编辑目录条目。**与 M06.2 的一般展开式一致**：M06.2 已收 $E_k(\tau) = 1 - \frac{2k}{B_k} \sum_{n=1}^{\infty} \sigma_{k-1}(n)\, q^n$，取 $k=2$、$B_2=1/6$ 即得系数 $24$ 与本式；但 M06 未以 $E_2$ 形式单独列出，且 $E_2$ 是拟模形式（quasimodular）而非模形式，M06 未收 $E_2$ 本身。站内未注明 $q$ 的定义与收敛条件，待核对。

## 3. Eisenstein Series E4

来源：https://ramanujan.aimersociety.com/discoveries/eisenstein-series-e4

$$E_4(q)=1+240\sum_{n=1}^{\infty}\sigma_3(n)q^n$$

状态：已提取待核对；站内类型 series，难度 Advanced，年份未注明，needs-review，Original Source 为编辑目录条目。**与 M06.2 一致**：M06.2 已收 $E_4(\tau) = 1 + 240 \sum_{n=1}^{\infty} \sigma_3(n)\, q^n$，与本站公式逐字一致（仅变量写法 $E_4(\tau)$ 与 $E_4(q)$ 之别，同为 $q$ 展开式）。站内未注明 $q$ 的定义与收敛条件，待核对。

## 4. Eisenstein Series E6

来源：https://ramanujan.aimersociety.com/discoveries/eisenstein-series-e6

$$E_6(q)=1-504\sum_{n=1}^{\infty}\sigma_5(n)q^n$$

状态：已提取待核对；站内类型 series，难度 Advanced，年份未注明，needs-review，Original Source 为编辑目录条目。**与 M06.2 一致**：M06.2 已收 $E_6(\tau) = 1 - 504 \sum_{n=1}^{\infty} \sigma_5(n)\, q^n$，与本站公式逐字一致（仅变量写法 $E_6(\tau)$ 与 $E_6(q)$ 之别，同为 $q$ 展开式）。站内未注明 $q$ 的定义与收敛条件，待核对。

## 5. Eisenstein-Series Congruences

来源：https://ramanujan.aimersociety.com/discoveries/eisenstein-series-congruences

无单一公式。站内类型为 identity，chunk 数据中无公式字段；条目页 HTML 含完整 contribution-family 声明：「This is a contribution-family entry; no single canonical formula is asserted here.」

## 6. Quasimodular Transformations of E2

来源：https://ramanujan.aimersociety.com/discoveries/quasimodular-e2-transformations

无单一公式。站内类型为 concept，chunk 数据中无公式字段；条目页 HTML 含完整 contribution-family 声明：「This is a contribution-family entry; no single canonical formula is asserted here.」

## 7. Ramanujan's Modular Differential System

来源：https://ramanujan.aimersociety.com/discoveries/modular-differential-system

$$q\frac{dE_4}{dq}=\frac{E_2E_4-E_6}{3}$$

状态：已提取待核对；站内类型 formula，难度 Advanced，年份未注明，needs-review，Original Source 为编辑目录条目。**M01–M14 未收的新增形式**（同第 1 条）。注意：本站本条只给三元方程组中的第二式；第一式见本分类第 1 条。两条合起来给出方程组的前两式；第三式本站未给出，按标准拉马努金微分方程组为 $q\frac{dE_6}{dq}=\frac{E_2E_6-E_4^2}{2}$——此式非本站内容，仅作对照注记。站内未注明 $q$ 的定义与收敛条件，待核对。
