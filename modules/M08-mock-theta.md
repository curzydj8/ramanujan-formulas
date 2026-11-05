# M08 · Mock Theta Functions（模拟 theta 函数）

模拟 theta 函数。拉马努金临终前的发现，写在他 1920 年 1 月给哈代的最后一封信里。

## 背景

- 拉马努金在最后一封信中说他发现了一些「非常有趣的函数」，称之为 mock theta 函数，给出了 17 个例子，但**没有给出严格定义**，只给了例子与一些性质描述。
- 其中第三阶与第五阶最著名：第五阶共 10 个，分成两组。
- **mock theta 猜想**（拉马努金临终猜想）：1987 年由 Hickerson 证明。
- **现代定义**（Zwegers, 2002）：mock theta 函数是调和 Maass 形式的全纯部分。这个定义等了 80 年才出现。

## 代表公式

第三阶 mock theta 函数 $f(q)$：

$$f(q) = \sum_{n=0}^{\infty} \frac{q^{n^2}}{(-q;q)_n^2}$$

其中 $(a;q)_n$ 为 q-Pochhammer 符号（见 M07）。

## 来源与延伸

- 出处：失落笔记的核心内容；Andrews–Berndt《Lost Notebook》多卷涉及。
- 关联模块：M07（q-级数）、M11（模形式、theta 函数）、M12（渐近展开）。

## 待补充

- 17 个 mock theta 例子逐个收录（第三阶 7 个、第五阶 10 个的分组与级数表达式），每条注明失落笔记出处与现代文献中的证明指引；mock theta 猜想的陈述与 Hickerson 证明的文献指引。
