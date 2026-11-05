# Rogers-Ramanujan Continued Fraction · AIMER 站公式提取

分类页：https://ramanujan.aimersociety.com/discoveries/category/rogers-ramanujan-continued-fraction

4 条中 **3 条有公式，1 条无单一公式**。提取自本站 Next.js 数据 chunk（/_next/static/ 下 JS chunk 内含全部 177 条的 KaTeX 原始源码）；chunk 中有公式字段的条目对应站内公式面板、无公式字段的条目对应站内 contribution-family 声明，此对应关系已在前几轮（Partition Theory、Mock Theta Functions、Formulas for pi）经实况浏览器逐条验证一致。本分类尚未做实况浏览器抽查复核——但三条公式已与 M03.4 已收录内容逐字核对一致，其中两条另经数值验证（见各条状态）。本站只收公式，解说不抄；站内条目多为 needs-review，公式须与 Berndt 五卷核对后才标「已核对」。

## 1. Rogers-Ramanujan Continued Fraction

来源：https://ramanujan.aimersociety.com/discoveries/rogers-ramanujan-continued-fraction

$$R(q)=q^{1/5}\cfrac{1}{1+\cfrac{q}{1+\cfrac{q^2}{1+\cdots}}}$$

状态：已提取待核对；与 M03.4 Rogers–Ramanujan 连分数完全一致（M03.4 用 $\frac$ 嵌套写法并展开到 $q^3$，本站用 $\cfrac$ 且截断于 $q^2$ 后接 $\cdots$，同一公式两种排版；M07 亦收录此式）。站内未注明收敛条件（$|q|<1$），待核对。

## 2. Exact Values and Modular Equations

来源：https://ramanujan.aimersociety.com/discoveries/exact-values-modular-equations

无单一公式。站内类型标为 formula，但条目数据中无公式字段，条目页未断言单一标准公式（以条目页实际显示为准；此前分类亦有类型标注与实际显示不符的先例，如 Alpha-Beta Modular Relations）。

## 3. Golden-Ratio Connections

来源：https://ramanujan.aimersociety.com/discoveries/golden-ratio-connections

$$R(e^{-2\pi})=\sqrt{\frac{5+\sqrt5}{2}}-\frac{1+\sqrt5}{2}$$

状态：已提取待核对；拉马努金关于 $R(q)$ 在 $q=e^{-2\pi}$ 处的著名求值。数值验证：按连分数定义在 $q=e^{-2\pi}$ 处算得 $0.2840790438404123$，与上式右端 $0.28407904384041216$ 吻合至机器精度。M03 未收录此具体求值，是新增形式（M03.4 只收了 $R(q)$ 的连分数定义与乘积式）。

## 4. Product Form of the Continued Fraction

来源：https://ramanujan.aimersociety.com/discoveries/product-form-continued-fraction

$$R(q)=q^{1/5}\frac{(q;q^5)_\infty(q^4;q^5)_\infty}{(q^2;q^5)_\infty(q^3;q^5)_\infty}$$

状态：已提取待核对；与 M03.4 乘积式完全一致（M03.4 多 $\,$ 间隔符）。数值验证：$q=0.5$ 时连分数定义算得 $0.6180183781955219$，乘积式算得 $0.6180183781955221$，吻合。
