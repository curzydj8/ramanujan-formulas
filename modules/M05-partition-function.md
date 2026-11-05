# M05 · 分拆函数（Partition Function）

整数分拆与同余关系。分拆理论是拉马努金与哈代合作的中心课题。

## 代表公式

### 分拆生成函数

$$\sum_{n=0}^{\infty} p(n)\, q^n = \prod_{n=1}^{\infty} \frac{1}{1-q^n} = \frac{1}{(q;q)_\infty}$$

其中 $p(n)$ 为 $n$ 的分拆数（$p(0) = 1$），$(q;q)_\infty$ 为 q-Pochhammer 符号（见 M07）。

### 拉马努金分拆同余式

$$\begin{aligned}
p(5n+4) &\equiv 0 \pmod{5} \\
p(7n+5) &\equiv 0 \pmod{7} \\
p(11n+6) &\equiv 0 \pmod{11}
\end{aligned}$$

### Hardy–Ramanujan 渐近公式（1917）

$$p(n) \sim \frac{e^{\pi\sqrt{2n/3}}}{4n\sqrt{3}} \qquad (n \to \infty)$$

Rademacher 后来把它改进为收敛的精确级数。

## 来源与延伸

- 出处：与哈代合作的论文（1917 年 Comptes Rendus 论文为起点）及笔记中的分拆条目。
- 关联模块：M13（分拆恒等式的组合视角）、M12（渐近公式的详细讨论）、M07（生成函数即 q-级数）。

## 待补充

- 逐条收录笔记中的分拆公式（递推关系、Ramanujan 同余式的推广、mock theta 与分拆的联系），每条注明出处与证明指引。
