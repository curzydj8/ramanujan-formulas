# Ramanujan's Master Theorem · AIMER 站公式提取

分类页：https://ramanujan.aimersociety.com/discoveries/category/ramanujan-master-theorem

2 条中 **1 条有公式，1 条无单一公式**。提取自本站 Next.js 数据 chunk（/_next/static/ 下 JS chunk 内含全部 177 条的 KaTeX 原始源码）；chunk 中有公式字段的条目对应站内公式面板、无公式字段的条目对应站内 contribution-family 声明，此对应关系已在前几轮（Partition Theory、Mock Theta Functions、Formulas for pi）经实况浏览器逐条验证一致。本分类未做实况浏览器抽查复核——但已用条目页静态 HTML 逐页核对：有公式的条目页 HTML 中含与 chunk 相同的公式源码且无 contribution-family 字样；无公式的条目页 HTML 中含完整 contribution-family 声明。本站只收公式，解说不抄；站内条目多为 needs-review，公式须与 Berndt 五卷核对后才标「已核对」。

## 1. Ramanujan's Master Theorem

来源：https://ramanujan.aimersociety.com/discoveries/ramanujan-master-theorem

$$\int_0^\infty x^{s-1}\{\lambda(0)-x\lambda(1)+\cdots\}\,dx=\frac{\pi}{\sin\pi s}\lambda(-s)$$

状态：已提取待核对；与 M09.4 拉马努金主定理一致。M09.4 用 $\varphi(n)/n!$ 系数约定给出 $\int_0^\infty x^{s-1}F(x)\,dx=\Gamma(s)\varphi(-s)$；本站用无阶乘系数约定（级数 $\lambda(0)-x\lambda(1)+\cdots$），右端为 $\frac{\pi}{\sin\pi s}\lambda(-s)$，两者为同一主定理的不同写法（$\Gamma(s)\Gamma(1-s)=\frac{\pi}{\sin\pi s}$，见 M09.4 应用与 M10 反射公式）。站内标注 Advanced、1918 年。站内未注明收敛条件（$s$ 的范围、对 $\lambda$ 的增长条件），待核对；站内级数只写到 $+\cdots$，未展开 $x^2\lambda(2)$ 项与交错符号，按本站公式原文照录。

## 2. Mellin-Transform Context of the Master Theorem

来源：https://ramanujan.aimersociety.com/discoveries/master-theorem-mellin-context

无单一公式。站内类型标为 method，chunk 数据中无公式字段；条目页 HTML 含完整 contribution-family 声明：「This is a contribution-family entry; no single canonical formula is asserted here.」
