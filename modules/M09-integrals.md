# M09 · 积分（Integrals）

定积分与特殊积分。本模块已从拉马努金专章扩展为**通用积分公式库**：从基本不定积分到 Ramanujan 主定理、著名定积分与椭圆积分一并收录。拉马努金留下了大量定积分求值公式，许多是他凭直觉写下、后人补证明的。

## M09.1 基本不定积分

$$\int x^n\,dx = \frac{x^{n+1}}{n+1} + C \quad (n \ne -1)$$

$$\int e^x\,dx = e^x + C, \qquad \int \frac{dx}{x} = \ln|x| + C$$

$$\int \sin x\,dx = -\cos x + C, \qquad \int \cos x\,dx = \sin x + C$$

$$\int \frac{dx}{1+x^2} = \arctan x + C, \qquad \int \frac{dx}{\sqrt{1-x^2}} = \arcsin x + C$$

$$\int \ln x\,dx = x\ln x - x + C$$

## M09.2 定积分技巧

### 分部积分

$$\int u\,dv = uv - \int v\,du$$

### 对称性

$f$ 为偶函数时 $\int_{-a}^{a} f(x)\,dx = 2\int_{0}^{a} f(x)\,dx$；$f$ 为奇函数时 $\int_{-a}^{a} f(x)\,dx = 0$。

### Wallis 积分

$$W_n = \int_{0}^{\pi/2} \sin^n x\,dx = \frac{n-1}{n}\, W_{n-2}, \qquad W_0 = \frac{\pi}{2},\ W_1 = 1$$

由此得 Wallis 乘积（M04.2）。

### 参数求导（Feynman 技巧）

$$\frac{d}{da} \int f(x, a)\,dx = \int \frac{\partial f}{\partial a}\,dx$$

在积分号下求导，常把难积分化为易积分。

## M09.3 Gamma 与 Beta 积分

### Gamma 函数的积分定义（见 M10）

$$\Gamma(s) = \int_{0}^{\infty} x^{s-1} e^{-x}\,dx \qquad (\mathrm{Re}\,s > 0)$$

特别地 $\int_{0}^{\infty} x^n e^{-x}\,dx = n!$（$n$ 为非负整数）。

### Beta 函数

$$B(p, q) = \int_{0}^{1} t^{p-1}(1-t)^{q-1}\,dt = \frac{\Gamma(p)\,\Gamma(q)}{\Gamma(p+q)}$$

### 高斯积分

$$\int_{-\infty}^{\infty} e^{-x^2}\,dx = \sqrt{\pi}, \qquad \int_{0}^{\infty} e^{-ax^2}\,dx = \frac{1}{2}\sqrt{\frac{\pi}{a}} \quad (a > 0)$$

## M09.4 Ramanujan 主定理

### 定理（Ramanujan's Master Theorem）

若 $F(x) = \sum_{n=0}^{\infty} \varphi(n)\,\frac{(-x)^n}{n!}$（$\varphi$ 有解析延拓且增长适当），则

$$\int_{0}^{\infty} x^{s-1} F(x)\,dx = \Gamma(s)\,\varphi(-s)$$

其中 $\Gamma$ 为 Gamma 函数（见 M10）。这是拉马努金最常用的积分工具：把级数系数解析延拓后直接读出积分值。

### 应用：$\pi / \sin \pi s$

取 $F(x) = 1/(1+x) = \sum_{n=0}^{\infty} (-x)^n$，此时 $\varphi(n) = n!$，得：

$$\int_{0}^{\infty} \frac{x^{s-1}}{1+x}\,dx = \Gamma(s)\,\Gamma(1-s) = \frac{\pi}{\sin \pi s} \qquad (0 < s < 1)$$

其中 $\Gamma(s)\Gamma(1-s) = \pi/\sin \pi s$ 为 Euler 反射公式（见 M10）。

## M09.5 著名定积分

### Dirichlet 积分

$$\int_{0}^{\infty} \frac{\sin x}{x}\,dx = \frac{\pi}{2}$$

### 对数积分

$$\int_{0}^{1} \ln x\,dx = -1, \qquad \int_{0}^{\pi/2} \ln(\sin x)\,dx = -\frac{\pi}{2}\ln 2$$

### 有理函数

$$\int_{0}^{\infty} \frac{dx}{1+x^2} = \frac{\pi}{2}, \qquad \int_{0}^{\infty} \frac{\cos bx}{1+x^2}\,dx = \frac{\pi}{2}\, e^{-|b|}$$

### Fresnel 积分

$$\int_{0}^{\infty} \sin(x^2)\,dx = \int_{0}^{\infty} \cos(x^2)\,dx = \sqrt{\frac{\pi}{8}}$$

### 高斯型

$$\int_{0}^{\infty} e^{-x^2}\cos bx\,dx = \frac{\sqrt{\pi}}{2}\, e^{-b^2/4}$$

## M09.6 椭圆积分

### 第一类与第二类完全椭圆积分（见 M11）

$$K(k) = \int_{0}^{\pi/2} \frac{d\theta}{\sqrt{1-k^2\sin^2\theta}}, \qquad E(k) = \int_{0}^{\pi/2} \sqrt{1-k^2\sin^2\theta}\,d\theta$$

其中 $k$ 为椭圆模。$K(k)$ 与 $K'(k) = K(\sqrt{1-k^2})$ 之比给出椭圆函数的周期比（见 M11）。

## M09.7 拉马努金的积分工作

- **主定理**：见 M09.4，拉马努金凭直觉写下、Hardy 补上严格条件；现代证明见 Berndt 整理本。
- **定积分求值**：三本笔记与失落笔记中有大量定积分条目（含三角函数、有理函数与指数型被积函数），失落笔记其余部分包括积分与 Dirichlet 级数。
- **与主定理的联系**：许多条目可用主定理统一求值；逐条收录时区分「拉马努金原结果」与「后人补证」。

## M09.8 待补充

- 逐条收录笔记中的定积分求值，每条注明出处、条件与证明指引。
- Frullani 积分、Laplace 变换表、椭圆积分的数值表。
