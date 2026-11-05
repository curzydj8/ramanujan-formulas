# M02 · 无穷级数（Infinite Series）

收敛、发散、级数变换。本模块已从拉马努金专章扩展为**通用无穷级数公式库**：判别法、求值、幂级数、Fourier 级数、发散级数的求和法、级数变换，欧拉、高斯、黎曼、傅里叶、阿贝尔、狄利克雷、拉马努金等人的工作一并收录。拉马努金本人的级数工作集中在 M02.7。

## M02.1 收敛与发散的判别法

### 几何级数

$$\sum_{n=0}^{\infty} r^n = \frac{1}{1-r} \qquad (|r| < 1)$$

$|r| \ge 1$ 时发散（$r = 1$ 时部分和为 $n+1$）。

### p-级数

$$\sum_{n=1}^{\infty} \frac{1}{n^p} \text{ 收敛} \iff p > 1$$

### 比较判别法

$0 \le a_n \le b_n$ 时：$\sum b_n$ 收敛则 $\sum a_n$ 收敛；$\sum a_n$ 发散则 $\sum b_n$ 发散。

### 比值判别法（d'Alembert，1768）

$$L = \lim_{n \to \infty} \left|\frac{a_{n+1}}{a_n}\right|$$

$L < 1$ 时绝对收敛，$L > 1$ 时发散，$L = 1$ 时不定。

### 根值判别法（Cauchy，1821）

$$L = \limsup_{n \to \infty} \sqrt[n]{|a_n|}$$

$L < 1$ 时绝对收敛，$L > 1$ 时发散，$L = 1$ 时不定。

### 积分判别法（Cauchy）

$a_n = f(n)$，$f$ 正值递减连续时，$\sum a_n$ 与 $\int_1^{\infty} f(x)\,dx$ 同敛散。

### Raabe 判别法

$$\lim_{n \to \infty} n\left(\frac{a_n}{a_{n+1}} - 1\right) = R$$

$R > 1$ 时收敛，$R < 1$ 时发散。比值判别法失效（$L = 1$）时常用。

### Leibniz 判别法（交错级数）

$a_n$ 单调递减趋于 0 时，$\sum (-1)^n a_n$ 收敛，且余项不超过首个略去项的绝对值：

$$\left|R_N\right| \le a_{N+1}$$

### 绝对收敛与条件收敛

- 绝对收敛：$\sum |a_n|$ 收敛，则 $\sum a_n$ 收敛，且任意重排后和不变。
- 条件收敛：$\sum a_n$ 收敛但 $\sum |a_n|$ 发散。
- **Riemann 重排定理**：条件收敛级数经适当重排，可收敛到任意指定实数，也可发散。

### Dirichlet 判别法与 Abel 判别法

- Dirichlet：$a_n$ 的部分和有界、$b_n$ 单调趋于 0，则 $\sum a_n b_n$ 收敛。
- Abel：$\sum a_n$ 收敛、$b_n$ 单调有界，则 $\sum a_n b_n$ 收敛。

## M02.2 著名级数求值

### 调和级数（发散）

$$\sum_{n=1}^{\infty} \frac{1}{n} = \infty, \qquad \sum_{n=1}^{N} \frac{1}{n} = \log N + \gamma + o(1)$$

$\gamma \approx 0.57721$ 为 Euler–Mascheroni 常数。

### Basel 问题（Euler，1734）

$$\sum_{n=1}^{\infty} \frac{1}{n^2} = \frac{\pi^2}{6}, \qquad \sum_{n=1}^{\infty} \frac{1}{n^4} = \frac{\pi^4}{90}$$

### zeta 偶数值通式（Euler）

$$\zeta(2n) = (-1)^{n+1} \frac{B_{2n} (2\pi)^{2n}}{2(2n)!}$$

其中 $B_{2n}$ 为 Bernoulli 数（$B_2 = 1/6$，$B_4 = -1/30$）。

### 奇倒数平方和

$$\sum_{n=0}^{\infty} \frac{1}{(2n+1)^2} = \frac{\pi^2}{8}$$

### 交错调和级数

$$\sum_{n=1}^{\infty} \frac{(-1)^{n+1}}{n} = \log 2$$

### Leibniz–Gregory 级数

$$\sum_{n=0}^{\infty} \frac{(-1)^n}{2n+1} = \frac{\pi}{4}$$

### 望远镜级数

$$\sum_{n=1}^{\infty} \frac{1}{n(n+1)} = 1$$

### Wallis 乘积（Wallis，1655）

$$\frac{\pi}{2} = \prod_{n=1}^{\infty} \frac{2n \cdot 2n}{(2n-1)(2n+1)} = \frac{2}{1} \cdot \frac{2}{3} \cdot \frac{4}{3} \cdot \frac{4}{5} \cdots$$

### 含 2 的幂的级数

$$\sum_{n=1}^{\infty} \frac{n}{2^n} = 2, \qquad \sum_{n=1}^{\infty} \frac{n^2}{2^n} = 6$$

## M02.3 幂级数与 Taylor 展开

### Cauchy–Hadamard 公式

幂级数 $\sum a_n (x - x_0)^n$ 的收敛半径：

$$\frac{1}{R} = \limsup_{n \to \infty} \sqrt[n]{|a_n|}$$

$|x - x_0| < R$ 时绝对收敛，$|x - x_0| > R$ 时发散。

### 指数函数

$$e^x = \sum_{n=0}^{\infty} \frac{x^n}{n!} \qquad (x \in \mathbb{R})$$

取 $x = 1$ 得 $e = \sum 1/n!$；取 $x = i\theta$ 得 Euler 公式 $e^{i\theta} = \cos\theta + i\sin\theta$。

### 三角函数

$$\sin x = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{(2n+1)!}, \qquad \cos x = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n}}{(2n)!}$$

### 对数与反三角

$$\log(1+x) = \sum_{n=1}^{\infty} (-1)^{n+1} \frac{x^n}{n} \qquad (-1 < x \le 1)$$

$$\arctan x = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n+1}}{2n+1} \qquad (|x| \le 1)$$

### 二项式级数（Newton）

$$(1+x)^{\alpha} = \sum_{n=0}^{\infty} \binom{\alpha}{n} x^n \qquad (|x| < 1)$$

其中 $\binom{\alpha}{n} = \alpha(\alpha-1)\cdots(\alpha-n+1)/n!$。

### 几何级数的微分与积分

$$\frac{1}{1-x} = \sum_{n=0}^{\infty} x^n, \qquad \frac{1}{(1-x)^2} = \sum_{n=1}^{\infty} n x^{n-1} \qquad (|x| < 1)$$

## M02.4 Fourier 级数

### Fourier 展开（Fourier，1822）

周期 $2\pi$ 的函数 $f$（分段光滑时）：

$$f(x) \sim \frac{a_0}{2} + \sum_{n=1}^{\infty} \left(a_n \cos nx + b_n \sin nx\right)$$

$$a_n = \frac{1}{\pi}\int_{-\pi}^{\pi} f(x)\cos nx\,dx, \qquad b_n = \frac{1}{\pi}\int_{-\pi}^{\pi} f(x)\sin nx\,dx$$

### 锯齿波

$$x = 2\sum_{n=1}^{\infty} (-1)^{n+1} \frac{\sin nx}{n} \qquad (-\pi < x < \pi)$$

### Parseval 恒等式

$$\frac{1}{\pi}\int_{-\pi}^{\pi} f(x)^2\,dx = \frac{a_0^2}{2} + \sum_{n=1}^{\infty} \left(a_n^2 + b_n^2\right)$$

取 $f(x) = x$ 可另证 $\sum 1/n^2 = \pi^2/6$。

### Dirichlet 条件

$f$ 在一周期内分段单调、有有限个间断点时，Fourier 级数在连续点收敛到 $f(x)$，在间断点收敛到左右极限的平均值。

## M02.5 发散级数的求和法

通常收敛意义下发散的级数，可用求和方法赋予一个和；不同的求和方法可能给出不同的值，须注明用的是哪一种。

### Abel 求和

$$\sum_{n=0}^{\infty} a_n = \lim_{x \to 1^-} \sum_{n=0}^{\infty} a_n x^n \qquad (\text{Abel 和})$$

### Cesàro 求和

部分和的算术平均收敛到的值。Grandi 级数：

$$1 - 1 + 1 - 1 + \cdots = \frac{1}{2} \qquad (\text{Cesàro 和、Abel 和})$$

### Ramanujan 求和（Ramanujan，1913）

$$1 + 2 + 3 + \cdots = -\frac{1}{12}, \qquad 1 + 1 + 1 + \cdots = -\frac{1}{2} \qquad (\text{Ramanujan 求和})$$

严格表述是 $\zeta(-1) = -1/12$、$\zeta(0) = -1/2$，即 Riemann zeta 函数在负整数点的解析延拓值。按通常的收敛意义，这两个级数都发散。

## M02.6 级数变换

### Abel 分部求和

记 $A_n = a_1 + \cdots + a_n$（$A_0 = 0$），则

$$\sum_{n=1}^{N} a_n b_n = A_N b_{N+1} - \sum_{n=1}^{N} A_n \left(b_{n+1} - b_n\right)$$

这是 Dirichlet 判别法与 Abel 判别法（M02.1）的证明工具。

### Euler 变换

$$\sum_{n=0}^{\infty} (-1)^n a_n = \sum_{n=0}^{\infty} \frac{\Delta^n a_0}{2^{n+1}}$$

其中 $\Delta a_n = a_{n+1} - a_n$ 为前向差分。Euler 变换可把收敛慢的交错级数变成收敛快的级数。

### 二项式反演

$$a_n = \sum_{k=0}^{n} \binom{n}{k} b_k \iff b_n = \sum_{k=0}^{n} (-1)^{n-k} \binom{n}{k} a_k$$

### Dirichlet 级数

$$F(s) = \sum_{n=1}^{\infty} \frac{a_n}{n^s}$$

Euler 乘积与 zeta 函数见 M01.3；Dirichlet 级数的收敛横坐标由 $\sum a_n$ 的性态决定。

## M02.7 拉马努金的级数

- **1913 年第一封信**：拉马努金写给哈代的第一封信包含约 120 条定理，其中大量是无穷级数——哈代正是看到这些级数才认定他是天才。
- **Ramanujan 求和**：$1 + 2 + 3 + \cdots = -1/12$（见 M02.5），即 $\zeta(-1)$ 的解析延拓值。
- **1/π 级数**：1914 年的快速收敛级数见 M04；其推导源于模方程（M11）。
- **Ramanujan 主定理**：级数与积分的桥梁，见 M09。
- **q-级数**：拉马努金级数工作的另一大分支，见 M07。

## M02.8 待补充

- 渐近级数：Stirling 公式 $n! \sim \sqrt{2\pi n}\,(n/e)^n$、Euler–Maclaurin 公式（与 M12 互链）。
- 超几何级数：Gauss 求和公式、广义超几何函数 ${}_pF_q$。
- Dirichlet 级数与 L 函数的深入内容（与 M01.3 互链）。
- 多重 zeta 值：Euler 和 $\zeta(a, b)$ 等。
- 拉马努金笔记中的级数条目：按 Berndt 五卷条目号逐条收录（与 M02.1–M02.6 的通用公式互链，不重复抄录）。
