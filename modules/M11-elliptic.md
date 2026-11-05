# M11 · 椭圆函数（Elliptic Functions）

椭圆积分与椭圆模数。本模块已从拉马努金专章扩展为**通用椭圆函数库**：从椭圆积分到 Jacobi 与 Weierstrass 椭圆函数、奇异模、theta 函数与模形式的联系一并收录。拉马努金的模方程理论是他最具独创性的工作之一，1914 年的 1/π 级数就源于这套理论。

## M11.1 椭圆积分

### 第一类与第二类完全椭圆积分

$$K(k) = \int_{0}^{\pi/2} \frac{d\theta}{\sqrt{1-k^2\sin^2\theta}}, \qquad E(k) = \int_{0}^{\pi/2} \sqrt{1-k^2\sin^2\theta}\,d\theta$$

其中 $k$ 为模数，$k' = \sqrt{1-k^2}$ 为余模数，$K' = K(k')$、$E' = E(k')$。

### 不完全椭圆积分

$$F(\varphi;k) = \int_{0}^{\varphi} \frac{d\theta}{\sqrt{1-k^2\sin^2\theta}}, \qquad E(\varphi;k) = \int_{0}^{\varphi} \sqrt{1-k^2\sin^2\theta}\,d\theta$$

### 第三类完全椭圆积分

$$\Pi(n;k) = \int_{0}^{\pi/2} \frac{d\theta}{(1-n\sin^2\theta)\sqrt{1-k^2\sin^2\theta}}$$

### Legendre 关系

$$K E' + K' E - K K' = \frac{\pi}{2}$$

### 周期比与 nome

$$\tau = i\,\frac{K'}{K}, \qquad q = e^{i\pi\tau} = e^{-\pi K'/K}$$

nome $q$ 把椭圆积分与 theta 函数、模形式连在一起（见 M06、M07）。

## M11.2 Jacobi 椭圆函数

### 定义

$\mathrm{sn}(u;k)$、$\mathrm{cn}(u;k)$、$\mathrm{dn}(u;k)$ 由第一类不完全椭圆积分的反函数定义：若 $u = F(\varphi;k)$，则 $\mathrm{sn}\,u = \sin\varphi$、$\mathrm{cn}\,u = \cos\varphi$、$\mathrm{dn}\,u = \sqrt{1-k^2\sin^2\varphi}$。

### 基本恒等式

$$\mathrm{sn}^2 u + \mathrm{cn}^2 u = 1, \qquad \mathrm{dn}^2 u + k^2\mathrm{sn}^2 u = 1$$

### 导数

$$\frac{d}{du}\mathrm{sn}\,u = \mathrm{cn}\,u\,\mathrm{dn}\,u, \qquad \frac{d}{du}\mathrm{cn}\,u = -\mathrm{sn}\,u\,\mathrm{dn}\,u, \qquad \frac{d}{du}\mathrm{dn}\,u = -k^2\mathrm{sn}\,u\,\mathrm{cn}\,u$$

### 退化情形

$k = 0$ 时 $\mathrm{sn}\,u = \sin u$、$\mathrm{cn}\,u = \cos u$、$\mathrm{dn}\,u = 1$；$k \to 1$ 时 $\mathrm{sn}\,u \to \tanh u$、$\mathrm{cn}\,u \to \mathrm{sech}\,u$。

## M11.3 Weierstrass ℘ 函数

### 定义

$$\wp(z) = \frac{1}{z^2} + \sum_{\omega \in \Lambda \setminus \{0\}} \left(\frac{1}{(z-\omega)^2} - \frac{1}{\omega^2}\right)$$

其中 $\Lambda$ 为复平面上的格。

### 微分方程

$$(\wp')^2 = 4\wp^3 - g_2\wp - g_3$$

其中不变量 $g_2 = 60\sum_{\omega \ne 0} \omega^{-4}$，$g_3 = 140\sum_{\omega \ne 0} \omega^{-6}$。

### 与 Eisenstein 级数的关系（格 $\Lambda = \mathbb{Z} + \mathbb{Z}\tau$）

$$g_2(\tau) = \frac{4\pi^4}{3}\,E_4(\tau), \qquad g_3(\tau) = \frac{8\pi^6}{27}\,E_6(\tau)$$

$$j(\tau) = 1728\,\frac{g_2^3}{g_2^3 - 27g_3^2}$$

见 M06.2 与 M06.4。

## M11.4 奇异模

### 定义

当 $\tau$ 为虚二次域中的点（即周期比 $K'/K = \sqrt{n}$，$n$ 为正整数）时，椭圆模 $k$ 的值称为**奇异模**，多表为根式与 Gamma 值之比；此时 $j(\tau)$ 为代数整数。

### 奇异模表

| $n = (K'/K)^2$ | $k$ |
|---|---|
| $1$ | $1/\sqrt{2}$ |
| $2$ | $\sqrt{2}-1$ |
| $3$ | $(\sqrt{6}-\sqrt{2})/4$ |

其中 $n = 3$ 的值即 $\sin(\pi/12)$。

### 一个著名求值

$$K\left(\frac{1}{\sqrt{2}}\right) = \frac{\Gamma(1/4)^2}{4\sqrt{\pi}} \approx 1.85407$$

见 M10.8 的双纽线常数。

## M11.5 theta 函数与模形式

### Jacobi theta 函数

$$\theta_3(z|\tau) = \sum_{n=-\infty}^{\infty} q^{n^2} e^{2\pi i n z}, \qquad q = e^{i\pi\tau}$$

$z = 0$ 时即 M06.7 的 $\theta(\tau)$。Jacobi 椭圆函数可表为 theta 函数之比；$\Delta(\tau) = \eta(\tau)^{24}$ 与 theta 函数的关系见 M06.7。

### 模方程与 1/π

$n$ 次模方程联系 $j(\tau)$ 与 $j(n\tau)$（见 M06.5）；拉马努金用模方程与奇异模推出 1/π 级数（见 M11.6）。

## M11.6 拉马努金的 1/π 级数（1914）

$$\frac{1}{\pi} = \frac{2\sqrt{2}}{9801} \sum_{n=0}^{\infty} \frac{(4n)!\,(1103 + 26390n)}{(n!)^4\, 396^{4n}}$$

该级数每项约给出 8 位十进制精度，源于模方程与奇异模的理论。完整推导与更多 1/π 级数见《数学全景图》拉马努金卷 r4；Chudnovsky 算法是其推广（见 M04.3）。

## M11.7 拉马努金的椭圆函数工作

- **模方程**：三本笔记中的模方程条目；拉马努金给出 3 次、5 次、7 次等多个次数的模方程。
- **奇异模**：失落笔记约三分之一关于模方程与奇异模；奇异模表见 M11.4。
- **1/π 级数**：见 M11.6，1914 年论文的代表作。

## M11.8 待补充

- 逐条收录模方程（按次数）与奇异模表，每条注明出处与证明指引。
- 椭圆积分求值公式与 theta 函数恒等式；Landen 变换表。
