# M10 · Gamma 函数（Gamma Function）

阶乘推广与特殊函数。本模块已从拉马努金专章扩展为**通用 Gamma 函数库**：从积分定义到反射与倍元公式、Weierstrass 乘积、Stirling 公式、Beta 函数与特殊值一并收录。Gamma 函数是拉马努金公式中最常用的特殊函数之一。

## M10.1 定义

### 积分定义（Euler）

$$\Gamma(z) = \int_{0}^{\infty} t^{z-1} e^{-t}\,dt \qquad (\mathrm{Re}\,z > 0)$$

解析延拓后 $\Gamma$ 在全复平面上除 $z = 0, -1, -2, \dots$ 处的单极点外全纯。

### 与阶乘的关系

$$\Gamma(n+1) = n! \qquad (n = 0, 1, 2, \dots)$$

$$\Gamma(1) = 1, \qquad \Gamma\left(\frac12\right) = \sqrt{\pi}$$

## M10.2 基本性质

### 递推公式

$$\Gamma(z+1) = z\,\Gamma(z)$$

### 半整数值

$$\Gamma\left(n+\frac12\right) = \frac{(2n)!}{4^n\, n!}\,\sqrt{\pi} \qquad (n = 0, 1, 2, \dots)$$

例如 $\Gamma(3/2) = \sqrt{\pi}/2$，$\Gamma(5/2) = 3\sqrt{\pi}/4$。

### 对数导数（digamma 函数）

$$\psi(z) = \frac{\Gamma'(z)}{\Gamma(z)}, \qquad \psi(1) = -\gamma$$

其中 $\gamma$ 为 Euler–Mascheroni 常数（见 M10.5）。

## M10.3 反射公式

### 反射公式（Euler）

$$\Gamma(z)\,\Gamma(1-z) = \frac{\pi}{\sin(\pi z)}$$

### 推论

$$\Gamma\left(\frac12\right)^2 = \pi, \qquad \Gamma\left(\frac14\right)\Gamma\left(\frac34\right) = \pi\sqrt{2}$$

$$\Gamma\left(\frac13\right)\Gamma\left(\frac23\right) = \frac{2\pi}{\sqrt{3}}, \qquad \Gamma\left(\frac16\right)\Gamma\left(\frac56\right) = 2\pi$$

注：反射公式与倍元公式是 Euler 与 Legendre 的经典结果，列在这里是因为它们是本模块一切公式的工具底座，不是拉马努金的发现；模块内收录时须区分「工具恒等式」与「拉马努金原结果」。

## M10.4 倍元与乘法公式

### 倍元公式（Legendre）

$$\Gamma(z)\,\Gamma\left(z+\frac12\right) = 2^{1-2z}\sqrt{\pi}\,\Gamma(2z)$$

### Gauss 乘法公式

$$\prod_{k=0}^{n-1} \Gamma\left(z+\frac{k}{n}\right) = (2\pi)^{(n-1)/2}\, n^{1/2-nz}\, \Gamma(nz)$$

$n = 2$ 时退化为倍元公式。

## M10.5 Weierstrass 乘积与 Euler 常数

### Weierstrass 乘积

$$\frac{1}{\Gamma(z)} = z\, e^{\gamma z} \prod_{n=1}^{\infty} \left(1+\frac{z}{n}\right) e^{-z/n}$$

### Euler–Mascheroni 常数

$$\gamma = \lim_{n\to\infty}\left(\sum_{k=1}^{n} \frac{1}{k} - \ln n\right) \approx 0.5772156649$$

$\gamma$ 是否为无理数仍未解决（见 M02.2 的注记）。

## M10.6 Stirling 公式

### 渐近展开

$$\Gamma(z) \sim \sqrt{2\pi}\, z^{z-1/2} e^{-z} \left(1 + \frac{1}{12z} + \frac{1}{288z^2} - \frac{139}{51840z^3} - \cdots\right)$$

### 对数形式

$$\ln\Gamma(z) = \left(z-\frac12\right)\ln z - z + \frac12\ln(2\pi) + \frac{1}{12z} - \frac{1}{360z^3} + \frac{1}{1260z^5} - \cdots$$

系数由 Bernoulli 数给出（见 M01.3）；详见 M12。

## M10.7 Beta 函数

### 定义与 Gamma 的关系

$$B(p, q) = \int_{0}^{1} t^{p-1}(1-t)^{q-1}\,dt = \frac{\Gamma(p)\,\Gamma(q)}{\Gamma(p+q)}$$

### 三角形式

$$B(p, q) = 2\int_{0}^{\pi/2} \sin^{2p-1}\theta\, \cos^{2q-1}\theta\,d\theta$$

## M10.8 特殊值

$$\Gamma\left(\frac14\right) \approx 3.6256099082, \qquad \Gamma\left(\frac13\right) \approx 2.6789385347$$

### 双纽线常数

$$\varpi = \frac{\Gamma(1/4)^2}{2\sqrt{2\pi}} \approx 2.6220575543$$

$\varpi$ 为双纽线常数（Gauss），即双纽线 $r^2 = \cos 2\theta$ 一半弧长；椭圆积分常表为 Gamma 值之比（见 M11）。

## M10.9 拉马努金的 Gamma 工作

- **主定理**：Ramanujan 主定理（M09.4）以 $\Gamma$ 为核心工具，拉马努金凭它求出大量定积分。
- **特殊值**：三本笔记中大量涉及 Gamma 函数与相关特殊函数的条目；奇异模常表为 Gamma 值之比（见 M11）。
- **与模形式的联系**：$\Delta(\tau) = q\,(q;q)_\infty^{24}$ 与 Gamma 值通过 Chowla–Selberg 公式相连（见 M06、M11）。

## M10.10 待补充

- 逐条收录拉马努金关于 Gamma 函数的公式（特殊值、乘积公式、与 Beta 函数及超几何函数的关系），每条注明出处与证明指引。
- digamma 函数 $\psi(z)$ 与 polygamma 函数的公式表；q-Gamma 函数。
