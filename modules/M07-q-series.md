# M07 · q-级数（q-Series）

q-级数恒等式。本模块已从拉马努金专章扩展为**通用 q-级数库**：从 q-Pochhammer 记号到 Jacobi 三重积、Rogers–Ramanujan 恒等式、q-超几何求和与 Ramanujan 的 _1ψ_1 求和一并收录。q-级数是拉马努金笔记与失落笔记中占比最大的主题，也是 mock theta 函数（M08）与分拆理论（M05、M13）的基础。

## M07.1 q-Pochhammer 符号与基本记号

### 定义（$|q| < 1$）

$$(a;q)_n = \prod_{k=0}^{n-1} (1 - a q^k), \qquad (a;q)_0 = 1$$

$$(a;q)_\infty = \prod_{k=0}^{\infty} (1 - a q^k)$$

多重记号 $(a_1, a_2, \dots, a_r; q)_n = (a_1;q)_n (a_2;q)_n \cdots (a_r;q)_n$。

### 常用特例

$$(q;q)_n = (1-q)(1-q^2)\cdots(1-q^n), \qquad (q;q)_\infty = \prod_{n=1}^{\infty} (1-q^n)$$

分拆生成函数即 $1/(q;q)_\infty$（见 M05.1）；$\Delta(\tau) = q\,(q;q)_\infty^{24}$（见 M06.3）。

## M07.2 q-二项式定理

### q-二项式定理（Rothe，1811；Cauchy）

$$\sum_{n=0}^{\infty} \frac{(a;q)_n}{(q;q)_n}\, z^n = \frac{(az;q)_\infty}{(z;q)_\infty} \qquad (|z| < 1,\ |q| < 1)$$

### 极限情形

令 $a \to 0$ 得 Euler 恒等式：

$$\sum_{n=0}^{\infty} \frac{z^n}{(q;q)_n} = \frac{1}{(z;q)_\infty}$$

令 $a \to \infty$（配 $z \to z/a$）得另一 Euler 恒等式：

$$\sum_{n=0}^{\infty} \frac{q^{n(n-1)/2} z^n}{(q;q)_n} = (-z;q)_\infty$$

### q-二项式系数

$$\binom{n}{k}_q = \frac{(q;q)_n}{(q;q)_k\,(q;q)_{n-k}}$$

它是「至多 $k$ 部分、最大部分至多 $n-k$ 的分拆」的生成函数；$q \to 1$ 时退化为普通二项式系数（见 M05.5）。

## M07.3 Jacobi 三重积

### Jacobi 三重积公式（Jacobi，1829）

$$\sum_{n=-\infty}^{\infty} z^n q^{n^2} = \prod_{m=1}^{\infty} (1-q^{2m})(1+z q^{2m-1})(1+z^{-1} q^{2m-1})$$

### 特殊情形

取 $z = 1$ 得 theta 函数 $\theta_3$：

$$\sum_{n=-\infty}^{\infty} q^{n^2} = \prod_{m=1}^{\infty} (1-q^{2m})(1+q^{2m-1})^2$$

取 $z = -1$ 得：

$$\sum_{n=-\infty}^{\infty} (-1)^n q^{n^2} = \prod_{m=1}^{\infty} (1-q^{2m})(1-q^{2m-1})^2$$

### 导出 Euler 五边形数定理

三重积中取 $Q = q^{3/2}$、$z = -q^{1/2}$，即得：

$$\prod_{n=1}^{\infty} (1-q^n) = \sum_{k=-\infty}^{\infty} (-1)^k q^{k(3k-1)/2}$$

见 M05.2。

## M07.4 Rogers–Ramanujan 恒等式

### 两条恒等式（Rogers，1894；Ramanujan，1913）

$$\sum_{n=0}^{\infty} \frac{q^{n^2}}{(q;q)_n} = \frac{1}{(q;q^5)_\infty (q^4;q^5)_\infty}$$

$$\sum_{n=0}^{\infty} \frac{q^{n^2+n}}{(q;q)_n} = \frac{1}{(q^2;q^5)_\infty (q^3;q^5)_\infty}$$

### 组合解释

第一条：相邻部分差至少为 2 的分拆数 = 各部分模 5 余 1 或 4 的分拆数。

第二条：相邻部分差至少为 2、且最小部分至少为 2 的分拆数 = 各部分模 5 余 2 或 3 的分拆数。

### Rogers–Ramanujan 连分数

$$R(q) = \frac{q^{1/5}}{1 + \dfrac{q}{1 + \dfrac{q^2}{1 + \dfrac{q^3}{1 + \cdots}}}}$$

与恒等式的关系见 M03.4。

## M07.5 q-超几何级数

### 基本超几何级数

$${}_r\phi_s\left[\begin{matrix} a_1, \dots, a_r \\ b_1, \dots, b_s \end{matrix}; q, z\right] = \sum_{n=0}^{\infty} \frac{(a_1, \dots, a_r;q)_n}{(b_1, \dots, b_s;q)_n\,(q;q)_n} \left[(-1)^n q^{n(n-1)/2}\right]^{1+s-r} z^n$$

$q \to 1$ 时退化为普通超几何级数 ${}_rF_s$（见 M09）。

### q-Gauss 求和（Heine）

$${}_2\phi_1(a, b; c; q, c/ab) = \frac{(c/a;q)_\infty\,(c/b;q)_\infty}{(c;q)_\infty\,(c/ab;q)_\infty}$$

### Heine 变换

$${}_2\phi_1(a, b; c; q, z) = \frac{(b;q)_\infty\,(az;q)_\infty}{(c;q)_\infty\,(z;q)_\infty}\; {}_2\phi_1(c/b, z; az; q, b)$$

## M07.6 Ramanujan 的 _1ψ_1 求和

### 双边基本超几何级数

$${}_1\psi_1(a; b; q, z) = \sum_{n=-\infty}^{\infty} \frac{(a;q)_n}{(b;q)_n}\, z^n$$

其中负指标 $(a;q)_n = (a;q)_\infty / (aq^n;q)_\infty$（$n < 0$）。

### Ramanujan _1ψ_1 求和公式

$$\sum_{n=-\infty}^{\infty} \frac{(a;q)_n}{(b;q)_n}\, z^n = \frac{(q;q)_\infty\,(b/a;q)_\infty\,(az;q)_\infty\,(q/az;q)_\infty}{(b;q)_\infty\,(q/a;q)_\infty\,(z;q)_\infty\,(b/az;q)_\infty}$$

成立条件：$|b/a| < |z| < 1$。这是拉马努金最著名的 q-级数求和，q-二项式定理与 Jacobi 三重积都是它的特例。

## M07.7 q-级数与分拆

q-级数大多是分拆生成函数：$\prod_{n\ge1} 1/(1-q^n)$ 计全部整数分拆（M05.1）；$\prod_{n\ge1} (1+q^n)$ 计不同部分的分拆（M05.5）；Rogers–Ramanujan 恒等式把受限分拆与模 5 剩余类联系起来（M07.4）。反之，分拆的组合证明常给出 q-级数恒等式的初等证明。

## M07.8 拉马努金的 q-级数工作

- **_1ψ_1 求和**：见 M07.6，拉马努金在笔记中给出、无证明，后由他人证明。
- **Rogers–Ramanujan 恒等式**：拉马努金 1913 年独立重新发现，比 Rogers 的 1894 年工作晚 19 年；Schur 于 1917 年给出证明。
- **失落笔记**：Andrews–Berndt《Lost Notebook》Part I（2005）前 442 条以连分数与 q-级数为重点；全五卷中 q-级数条目数以百计。
- **mock theta**：失落笔记中的 mock theta 函数是 q-级数的特殊一支（见 M08）。

## M07.9 待补充

- 按 Berndt 五卷与失落笔记五卷的条目号，逐条收录 q-级数恒等式（含 Watson 变换、Bailey 引理相关条目），每条注明出处与证明指引。
- 更多求和公式：q-Saalschütz、q-Dixon、Bailey 对与 WP-Bailey 链。
