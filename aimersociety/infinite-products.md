# Infinite Products · AIMER 站公式提取

分类页：https://ramanujan.aimersociety.com/discoveries/category/infinite-products

5 条中 **2 条有公式，3 条无单一公式**。提取自本站 Next.js 数据 chunk（/_next/static/ 下 JS chunk 内含全部 177 条的 KaTeX 原始源码）；chunk 中有公式字段的条目对应站内公式面板、无公式字段的条目对应站内 contribution-family 声明，此对应关系已在前几轮（Partition Theory、Mock Theta Functions、Formulas for pi）经实况浏览器逐条验证一致。本分类未做实况浏览器抽查复核——但已用条目页静态 HTML 逐页核对：有公式的条目页 HTML 中含与 chunk 相同的公式源码且含「Formula permalink」与「Copy LaTeX」按钮、无 contribution-family 字样；无公式的条目页 HTML 中含完整 contribution-family 声明（见各条状态）。本站只收公式，解说不抄；站内条目多为 needs-review，公式须与 Berndt 五卷核对后才标「已核对」。

## 1. Eta Quotients

来源：https://ramanujan.aimersociety.com/discoveries/eta-quotients

$$\eta(\tau)=q^{1/24}\prod_{n=1}^{\infty}(1-q^n)$$

状态：已提取待核对；与 M06.7 的 Dedekind η 函数定义逐字一致（M06.7 另给出 $\Delta(\tau)=\eta(\tau)^{24}$）。站内未注明 $q$ 的定义与收敛条件（M06 为 $q=e^{2\pi i\tau}$，$|q|<1$ 即 $\mathrm{Im}\,\tau>0$），待核对。

## 2. Eta-Product Identities

来源：https://ramanujan.aimersociety.com/discoveries/eta-product-identities

无单一公式。站内明确标注为 contribution-family：「This is a contribution-family entry; no single canonical formula is asserted here.」（条目页 HTML 已核对，含该声明。）

## 3. Eta-Transformation Formulas

来源：https://ramanujan.aimersociety.com/discoveries/eta-transformation-formulas

无单一公式。站内明确标注为 contribution-family：「This is a contribution-family entry; no single canonical formula is asserted here.」（条目页 HTML 已核对，含该声明。）注意：chunk 中本站将此条类型标为 formula，但条目页仍显示 contribution-family 声明、无公式面板，以条目页实际显示为准。

## 4. Infinite Products

来源：https://ramanujan.aimersociety.com/discoveries/infinite-products

无单一公式。站内明确标注为 contribution-family：「This is a contribution-family entry; no single canonical formula is asserted here.」（条目页 HTML 已核对，含该声明。）站内论文记录另关联拉马努金 1920 年论文「Algebraic Relations Between Certain Infinite Products」（Proc. London Math. Soc. (2) 18，1919 年 3 月 13 日会议记录），但该条目本身未给出单一公式。

## 5. Infinite-Product Transformations

来源：https://ramanujan.aimersociety.com/discoveries/infinite-product-transformations

$$(a;q)_\infty=\prod_{k=0}^{\infty}(1-aq^k)$$

状态：已提取待核对；与 M07.1 的 q-Pochhammer 符号无穷情形逐字一致（M07.1 另给出有限情形 $(a;q)_n=\prod_{k=0}^{n-1}(1-aq^k)$ 与约定 $(a;q)_0=1$）。站内未注明收敛条件（M07.1 为 $|q|<1$），待核对。
