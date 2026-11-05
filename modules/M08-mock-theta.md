# M08 · Mock Theta Functions（模拟 theta 函数）

模拟 theta 函数。本模块已从拉马努金专章扩展为**通用 mock theta 库**：从 1920 年最后一封信的 17 个例子，到 Watson 与 Hickerson 的证明，再到 Zwegers 2002 年的现代定义与分拆 rank 的联系一并收录。拉马努金临终前的发现，写在他 1920 年 1 月给哈代的最后一封信里。

> 订正：本文件旧版写「第三阶 7 个、第五阶 10 个」有误；信中 17 个的正确分组为三阶 4 个、五阶 6 个、七阶 3 个、六阶 4 个（见 M08.2）。八阶与十阶的例子出自失落笔记，不在信中。

## M08.1 历史与定义

### 最后一封信（Ramanujan，1920 年 1 月）

拉马努金在给哈代的最后一封信中说他发现了一些「非常有趣的函数」，称之为 mock theta 函数，给出了 17 个例子与一些性质描述，但**没有给出严格定义**。他于同年 4 月去世，享年 32 岁。

### 「mock」的含义

mock theta 函数在单位根处的行为像 theta 函数（有类似的渐近展开），但本身不是模形式：把它补上一个非全纯的修正项后，才具有模变换性。这个定义等了 80 年才出现。

### 现代定义（Zwegers，2002）

mock theta 函数是**调和 Maass 形式**（harmonic Maass form）的全纯部分。权 1/2 的调和 Maass 形式可分解为全纯部分（mock 模形式）与非全纯部分；全纯部分配上其「影子」（shadow，一个权 3/2 的一元 theta 级数）的非全纯 Eichler 积分后，整体具有模变换性。

## M08.2 17 个例子一览

拉马努金信中 17 个例子按「阶」（order）分组：

| 阶 | 个数 | 函数 |
|---|---|---|
| 3 阶 | 4 | $f(q)$、$\phi(q)$、$\psi(q)$、$\chi(q)$ |
| 5 阶 | 6 | $f_0(q)$、$f_1(q)$、$F_0(q)$、$F_1(q)$、$\Phi(q)$、$\Psi(q)$ |
| 7 阶 | 3 | $F_0(q)$、$F_1(q)$、$F_2(q)$ |
| 6 阶 | 4 | $\phi(q)$、$\psi(q)$、$\rho(q)$、$\sigma(q)$ |

失落笔记中还有更多例子：六阶的 $\lambda(q)$、$\mu(q)$，以及八阶（$S_0, S_1, T_0, T_1, U_0, U_1, V_0, V_1$）与十阶（$\phi, \psi, X, \chi$）的例子。

## M08.3 第三阶 mock theta 函数

### 四个三阶例子

$$f(q) = \sum_{n=0}^{\infty} \frac{q^{n^2}}{(-q;q)_n^2}$$

$$\phi(q) = \sum_{n=0}^{\infty} \frac{q^{n^2}}{(-q^2;q^2)_n}$$

$$\psi(q) = \sum_{n=0}^{\infty} \frac{q^{n^2}}{(q;q^2)_n}$$

$$\chi(q) = \sum_{n=0}^{\infty} \frac{q^{n^2}}{(q;q)_n^2}$$

其中 $(a;q)_n$ 为 q-Pochhammer 符号（见 M07）。

### mock theta 猜想（Ramanujan，1920）

拉马努金在信中给出 10 条关于三阶 mock theta 的恒等式，把 mock theta 函数与 theta 函数联系起来。Watson 于 1936 年证明了其中大部分，Hickerson 于 1987 年补全其余部分，全部证明完成。

## M08.4 第五阶 mock theta 函数

### 四个五阶例子（级数形式）

$$f_0(q) = \sum_{n=0}^{\infty} \frac{q^{n^2}}{(-q;q)_n}$$

$$f_1(q) = \sum_{n=0}^{\infty} \frac{q^{n^2+n}}{(-q;q)_n}$$

$$F_0(q) = \sum_{n=0}^{\infty} \frac{q^{2n^2}}{(q;q^2)_n}$$

$$F_1(q) = \sum_{n=0}^{\infty} \frac{q^{2n^2+2n}}{(q;q^2)_n}$$

### 其余两个五阶例子

$\Phi(q)$ 与 $\Psi(q)$ 是另外两个五阶例子；五阶 mock theta 猜想由 Hickerson（1988）与 Andrews–Hickerson（1991）证明。

## M08.5 Zwegers 的现代定义（续）

权 1/2 的调和 Maass 形式 $F$ 可写成全纯部分 $f$（mock 模形式）与非全纯部分之和；$f$ 的「影子」（shadow）是一个权 3/2 的一元 theta 级数。把 $f$ 加上影子的非全纯 Eichler 积分（称为 $f$ 的「完备化」）后，整体按权 1/2 模变换。例如 $f(q)$ 的影子是一个权 3/2 的一元 theta 级数。

## M08.6 mock theta 与分拆

### rank 生成函数（Dyson，1944）

$$R(z;q) = \sum_{n=0}^{\infty} \frac{q^{n^2}}{(zq;q)_n\,(z^{-1}q;q)_n}$$

其中 $z$ 标记 rank（见 M05.7）。取 $z = -1$ 得：

$$R(-1;q) = f(q)$$

即三阶 mock theta 函数 $f(q)$ 就是 rank 生成函数在 $z = -1$ 处的值。

### crank 生成函数（Andrews–Garvan，1988）

$$C(z;q) = \frac{(q;q)_\infty}{(zq;q)_\infty\,(z^{-1}q;q)_\infty}$$

crank 生成函数本质上是模形式（而非 mock），这正是 crank 能解释模 11 同余式的原因（见 M05.7）。

### Bringmann–Ono（2006）

Bringmann 与 Ono 证明 rank 生成函数是 mock 模形式，并用 Maass 形式理论给出分拆同余式的新证明，把 mock theta 与分拆同余式（M05.3）连成一体。

## M08.7 拉马努金的 mock theta 工作

- **1920 年最后一封信**：17 个例子，无定义，只有例子与性质描述。
- **失落笔记**：更多 mock theta 例子（六阶 $\lambda, \mu$、八阶、十阶）与恒等式，见 Andrews–Berndt《Lost Notebook》多卷。
- **证明史**：Watson 1936 年证明三阶 mock theta 猜想的大部分；Hickerson 1987 年补全三阶、1988 年证明五阶；Zwegers 2002 年给出调和 Maass 形式的现代定义。

## M08.8 待补充

- 17 个例子逐个收录（六阶 $\phi, \psi, \rho, \sigma$ 与七阶 $F_0, F_1, F_2$ 的级数表达式），每条注明失落笔记出处与现代文献中的证明指引。
- 八阶与十阶例子的级数表达式。
- mock theta 猜想（五阶）的完整陈述与证明文献指引。
