# Ramanujan's Tau Function · AIMER 站公式提取

分类页：https://ramanujan.aimersociety.com/discoveries/category/ramanujan-tau-function

8 条中 **7 条有公式，1 条无单一公式**。提取自本站 Next.js 数据 chunk（/_next/static/ 下 JS chunk 内含全部 177 条的 KaTeX 原始源码）；chunk 中有公式字段的条目对应站内公式面板、无公式字段的条目对应站内 contribution-family 声明，此对应关系已在前几轮（Partition Theory、Mock Theta Functions、Formulas for pi）经实况浏览器逐条验证一致。本分类未做实况浏览器抽查复核——但已用条目页静态 HTML 逐页核对：7 条有公式的条目页 HTML 中均含与 chunk 相同的公式源码且无 contribution-family 字样；其余 1 条条目页 HTML 中含完整 contribution-family 声明（见各条状态）。本站只收公式，解说不抄；站内条目多为 needs-review，公式须与 Berndt 五卷核对后才标「已核对」。

## 1. Ramanujan's Tau Function

来源：https://ramanujan.aimersociety.com/discoveries/ramanujan-tau-function

$$\Delta(q)=q\prod_{n=1}^{\infty}(1-q^n)^{24}=\sum_{n=1}^{\infty}\tau(n)q^n$$

状态：已提取待核对；与 M06.3 的 Δ 函数定义逐字一致（M01 亦收录同一等式）。$\tau(n)$ 即 Ramanujan tau 函数，$\Delta$ 是权为 12 的尖点模形式。注意：第 3 条为同一乘积式的单独条目（不含 Fourier 级数部分）。

## 2. Further Tau Congruences

来源：https://ramanujan.aimersociety.com/discoveries/tau-ramanujan-congruences

无单一公式。站内明确标注为 contribution-family：「This is a contribution-family entry; no single canonical formula is asserted here.」（条目页 HTML 已核对，含该声明。）注：主题为 τ 函数的进一步同余式，具体同余式见第 5、8 条（模 691）。

## 3. Generating Function for tau(n)

来源：https://ramanujan.aimersociety.com/discoveries/tau-generating-function

$$\Delta(q)=q\prod_{n=1}^{\infty}(1-q^n)^{24}$$

状态：已提取待核对；与 M06.3 的 Δ 函数定义一致，是第 1 条公式的乘积式部分（不含 Fourier 级数 $\sum \tau(n)q^n$）。

## 4. Ramanujan-Petersson Conjecture

来源：https://ramanujan.aimersociety.com/discoveries/ramanujan-petersson-conjecture

$$|\tau(p)|\le 2p^{11/2}$$

状态：已提取待核对；与 M06.3、M01 的 Ramanujan 猜想逐字一致（M01 注明 $p$ 为素数）。拉马努金于 1916 年猜想，Deligne 于 1974 年证明（Weil 猜想的一部分）。站内将本条类型标为 conjecture，未注明证明者与年份，已在此注明。

## 5. Tau Congruence Modulo 691

来源：https://ramanujan.aimersociety.com/discoveries/tau-mod-691-congruence

$$\tau(n)\equiv\sigma_{11}(n)\pmod{691}$$

状态：已提取待核对；与 M01 的同余式逐字一致（M06.3 亦有收录）。注意：与第 8 条公式完全相同，站内两条目为重复收录的同一同余式。

## 6. Tau Multiplicativity

来源：https://ramanujan.aimersociety.com/discoveries/tau-multiplicativity

$$\tau(mn)=\tau(m)\tau(n)\quad((m,n)=1)$$

状态：已提取待核对；与 M06.3 的 τ(n) 乘性逐字一致（M06.3 注明为 Hecke 乘性）。Mordell 于 1917 年证明。站内将本条类型标为 conjecture，未注明证明者与年份，已在此注明。

## 7. Tau Prime-Power Recurrence

来源：https://ramanujan.aimersociety.com/discoveries/tau-prime-power-recurrence

$$\tau(p^{r+1})=\tau(p)\tau(p^r)-p^{11}\tau(p^{r-1})$$

状态：已提取待核对；与 M06.3 的素数幂递推一致（M06.3 用 $n$ 作指数，站内用 $r$，同一公式）。Mordell 于 1917 年证明。站内未注明 $p$ 为素数、$r \ge 1$ 等适用条件，待核对。

## 8. Tau-Function Congruences

来源：https://ramanujan.aimersociety.com/discoveries/tau-function-congruences

$$\tau(n)\equiv\sigma_{11}(n)\pmod{691}$$

状态：已提取待核对；与 M01 的同余式逐字一致（M06.3 亦有收录）。注意：与第 5 条公式完全相同，站内两条目为重复收录的同一同余式。
