# Nested Radicals · AIMER 站公式提取

分类页：https://ramanujan.aimersociety.com/discoveries/category/nested-radicals

3 条中 **1 条有公式，2 条无单一公式**。提取自本站 Next.js 数据 chunk（/_next/static/ 下 JS chunk 内含全部 177 条的 KaTeX 原始源码）；chunk 中有公式字段的条目对应站内公式面板、无公式字段的条目对应站内 contribution-family 声明，此对应关系已在前几轮（Partition Theory、Mock Theta Functions、Formulas for pi）经实况浏览器逐条验证一致。本分类未做实况浏览器抽查复核——但已用条目页静态 HTML 逐页核对：有公式的条目页 HTML 中含与 chunk 相同的公式源码且含「Formula permalink」与「Copy LaTeX」按钮、无 contribution-family 字样；无公式的条目页 HTML 中含完整 contribution-family 声明。本站只收公式，解说不抄；站内条目多为 needs-review，公式须与 Berndt 五卷核对后才标「已核对」。

## 1. General Nested-Radical Identities

来源：https://ramanujan.aimersociety.com/discoveries/general-nested-radical-identities

无单一公式。站内类型为 contribution-family，chunk 数据中无公式字段；条目页 HTML 含完整 contribution-family 声明：「This is a contribution-family entry; no single canonical formula is asserted here.」

## 2. Infinite Nested Radical

来源：https://ramanujan.aimersociety.com/discoveries/infinite-nested-radical

$$\sqrt{1+2\sqrt{1+3\sqrt{1+\cdots}}}=3$$

状态：已提取待核对；站内类型 formula，难度 Advanced，年份未注明，needs-review，Original Source 为编辑目录条目。**M01–M14 未收的新增形式**：M01–M14 全文未收嵌套根式（nested radical）相关内容，本式是拉马努金最著名的无穷根式恒等式。数值复核通过：有限截断 $\sqrt{1+2\sqrt{1+3\sqrt{1+\cdots}}}$（深度 20）约为 2.99998788，收敛到 3；其一般形式为 $x+1=\sqrt{1+x\sqrt{1+(x+1)\sqrt{1+(x+2)\sqrt{1+\cdots}}}}$（取 $x=2$ 即得本式；我数值复核 $x=1,2,3,5$ 均收敛到 $x+1$）。站内未注明收敛条件与出处，待核对。

## 3. Nested Radical Continued Forms

来源：https://ramanujan.aimersociety.com/discoveries/nested-radical-continued-forms

无单一公式。注意：站内类型标为 formula，但 chunk 数据中无公式字段，条目页 HTML 含完整 contribution-family 声明：「This is a contribution-family entry; no single canonical formula is asserted here.」以条目页实际显示为准（与前几轮 Eta-Transformation Formulas、Definite Integrals、Frullani-Type 等同类陷阱）。
