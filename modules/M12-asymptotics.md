# M12 · 渐近分析（Asymptotics）

近似公式与渐近展开。本模块已从拉马努金专章扩展为**通用渐近分析库**：从渐近记号到 Stirling 公式、分拆与素数渐近、调和数、Euler–Maclaurin 公式一并收录。拉马努金与哈代 1917–1918 年开创的圆法（circle method）是解析数论的里程碑。

## M12.1 渐近记号

### 记号定义（$x \to \infty$）

$$f(x) \sim g(x) \iff \frac{f(x)}{g(x)} \to 1$$

$$f(x) = O(g(x)) \iff |f(x)| \le C\,|g(x)| \quad (x \text{ 充分大})$$

$$f(x) = o(g(x)) \iff \frac{f(x)}{g(x)} \to 0$$

$$f(x) = \Theta(g(x)) \iff f(x) = O(g(x)) \text{ 且 } g(x) = O(f(x))$$

## M12.2 Stirling 公式

### 阶乘渐近

$$n! \sim \sqrt{2\pi n}\left(\frac{n}{e}\right)^n \qquad (n \to \infty)$$

### 对数形式

$$\ln n! = n\ln n - n + \frac12\ln(2\pi n) + \frac{1}{12n} - \frac{1}{360n^3} + \frac{1}{1260n^5} - \cdots$$

系数由 Bernoulli 数给出；Gamma 函数的版本见 M10.6。

### 二项式系数渐近

$$\binom{2n}{n} \sim \frac{4^n}{\sqrt{\pi n}} \qquad (n \to \infty)$$

## M12.3 分拆渐近

### Hardy–Ramanujan 分拆渐近公式（1917–1918）

记 $p(n)$ 为 $n$ 的分拆数，则当 $n \to \infty$ 时

$$p(n) \sim \frac{e^{\pi\sqrt{2n/3}}}{4n\sqrt{3}}$$

这是圆法的第一个重大成果；Rademacher 后来把它改进为收敛的精确级数（见 M05.4）。

## M12.4 素数渐近

### 素数定理（Hadamard、de la Vallée Poussin，1896）

$$\pi(x) \sim \frac{x}{\ln x}, \qquad \pi(x) = \mathrm{Li}(x) + O\left(x\,e^{-c\sqrt{\ln x}}\right)$$

其中 $\mathrm{Li}(x) = \int_{2}^{x} dt/\ln t$，$c > 0$ 为常数。

### 第 $n$ 个素数

$$p_n \sim n\ln n \qquad (n \to \infty)$$

### Chebyshev 函数

$$\theta(x) = \sum_{p \le x} \ln p \sim x, \qquad \psi(x) = \sum_{n \le x} \Lambda(n) \sim x$$

$\theta(x) \sim x$ 与素数定理等价。

### 除数求和（Dirichlet，1849）

$$\sum_{n \le x} d(n) = x\ln x + (2\gamma-1)x + O(\sqrt{x})$$

其中 $d(n)$ 为除数个数，$\gamma$ 为 Euler 常数；误差项的最优阶仍是未解决问题（猜想为 $O(x^{1/4+\varepsilon})$）。

## M12.5 调和数

### 调和数的渐近展开

$$H_n = \sum_{k=1}^{n} \frac{1}{k} = \ln n + \gamma + \frac{1}{2n} - \frac{1}{12n^2} + \frac{1}{120n^4} - \cdots$$

其中 $\gamma \approx 0.5772156649$ 为 Euler–Mascheroni 常数（见 M10.5）。

## M12.6 Euler–Maclaurin 公式与渐近级数

### Euler–Maclaurin 求和公式

$$\sum_{k=a}^{b} f(k) = \int_{a}^{b} f(x)\,dx + \frac{f(a)+f(b)}{2} + \sum_{k=1}^{m} \frac{B_{2k}}{(2k)!}\left(f^{(2k-1)}(b) - f^{(2k-1)}(a)\right) + R_m$$

其中 $B_{2k}$ 为 Bernoulli 数（见 M01.3）；它是调和数展开（M12.5）与 Stirling 公式（M12.2）的统一来源。

### 渐近级数（Poincaré）

渐近级数一般是发散的：固定 $x$ 时项数加多不收敛，固定项数时 $x \to \infty$ 才逼近。Stirling 级数即为发散的渐近级数；最优截断（在最小项处截断）给出最佳近似。

## M12.7 拉马努金的渐近工作

- **圆法**：与哈代 1917–1918 年开创圆法，得出分拆渐近公式（M12.3），是解析数论的里程碑。
- **笔记中的渐近条目**：三本笔记与失落笔记中有大量渐近公式（含调和数、阶乘、素数相关量与分拆函数的近似）；失落笔记其余部分包括渐近分析。
- **Ramanujan 求和**：发散级数的求值方法（见 M02.5），与渐近展开密切相关。

## M12.8 待补充

- 逐条收录笔记中的渐近公式，每条注明出处、适用范围与误差项；区分「渐近等价」与「带误差项的精确估计」。
- 鞍点法（saddle-point method）与 Laplace 方法的公式表。
