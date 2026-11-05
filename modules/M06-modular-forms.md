# M06 · 模形式（Modular Forms）

模方程与模函数。本模块已从拉马努金专章扩展为**通用模形式库**：从 Eisenstein 级数到 Hecke 理论与模性定理，定义、基本例子、Δ 与 τ(n)、j 不变量、模方程、L 函数一并收录。模形式是拉马努金全部工作的组织骨架：tau 函数、theta 函数、模方程都在这套语言里。

## M06.1 定义与基本概念

### 上半平面与模群

$$\mathbb{H} = \{\tau \in \mathbb{C} : \mathrm{Im}\,\tau > 0\}$$

模群 $\mathrm{SL}(2, \mathbb{Z})$ 由分式线性变换作用于 $\mathbb{H}$：

$$\gamma \tau = \frac{a\tau + b}{c\tau + d}, \qquad \gamma = \begin{pmatrix} a & b \\ c & d \end{pmatrix} \in \mathrm{SL}(2, \mathbb{Z})$$

### 权 $k$ 模形式

权 $k$ 模形式 $f$ 是 $\mathbb{H}$ 上的全纯函数，满足对一切 $\gamma \in \mathrm{SL}(2, \mathbb{Z})$：

$$f(\gamma \tau) = (c\tau + d)^k f(\tau)$$

且在无穷远处全纯。其 Fourier 展开（$q = e^{2\pi i \tau}$）：

$$f(\tau) = \sum_{n=0}^{\infty} a_n q^n$$

若 $a_0 = 0$，称 $f$ 为**尖点形式**（cusp form）。

### 维数公式

$\mathrm{SL}(2, \mathbb{Z})$ 上权 $k$（$k$ 为偶数）模形式空间 $M_k$ 的维数：

$$\dim M_k = \begin{cases}
\lfloor k/12 \rfloor + 1, & k \not\equiv 2 \pmod{12} \\
\lfloor k/12 \rfloor, & k \equiv 2 \pmod{12}
\end{cases}$$

## M06.2 Eisenstein 级数

### 定义

$$G_k(\tau) = \sum_{(m,n) \ne (0,0)} \frac{1}{(m\tau + n)^k} \qquad (k \ge 4 \text{ 偶数})$$

归一化 Eisenstein 级数 $E_k = G_k / (2\zeta(k))$。

### Fourier 展开

$$E_k(\tau) = 1 - \frac{2k}{B_k} \sum_{n=1}^{\infty} \sigma_{k-1}(n)\, q^n$$

其中 $B_k$ 为 Bernoulli 数（M01.3），$\sigma_{k-1}(n)$ 为除数函数。

### $E_4$ 与 $E_6$

$$E_4(\tau) = 1 + 240 \sum_{n=1}^{\infty} \sigma_3(n)\, q^n$$

$$E_6(\tau) = 1 - 504 \sum_{n=1}^{\infty} \sigma_5(n)\, q^n$$

$E_4$ 与 $E_6$ 生成全部模形式环：每个权 $k$ 模形式都是 $E_4$ 与 $E_6$ 的多项式。

## M06.3 Δ 函数与 τ(n)

### 判别式 Δ

$$\Delta(\tau) = \frac{E_4(\tau)^3 - E_6(\tau)^2}{1728} = q \prod_{n=1}^{\infty} (1-q^n)^{24} = \sum_{n=1}^{\infty} \tau(n)\, q^n$$

$\Delta$ 是权 12 的尖点形式，$S_{12}$ 的基。

### Ramanujan tau 函数

$$\tau(1), \tau(2), \tau(3), \dots = 1, -24, 252, -1472, 4830, -6048, -16744, 84480, -113643, -115920, \dots$$

### τ(n) 的性质

**乘性**（Hecke）：$(m, n) = 1$ 时 $\tau(mn) = \tau(m)\tau(n)$，且

$$\tau(p^{n+1}) = \tau(p)\tau(p^n) - p^{11}\tau(p^{n-1})$$

**同余式**（Ramanujan，1916）：

$$\tau(n) \equiv \sigma_{11}(n) \pmod{691}$$

**Ramanujan 猜想**（Deligne，1974 年证明）：

$$|\tau(p)| \le 2p^{11/2}$$

**Lehmer 猜想**（未解决）：$\tau(n) \ne 0$ 对一切 $n$ 成立。

## M06.4 j 不变量

### 定义

$$j(\tau) = 1728\,\frac{E_4(\tau)^3}{E_4(\tau)^3 - E_6(\tau)^2} = 1728\,\frac{E_4(\tau)^3}{\Delta(\tau)}$$

$j$ 是权 0 的模函数，在 $\mathbb{H}/\mathrm{SL}(2,\mathbb{Z})$ 上给出双射。

### Fourier 展开

$$j(\tau) = q^{-1} + 744 + 196884\,q + 21493760\,q^2 + 864299970\,q^3 + \cdots$$

### 特殊值

$$j(i) = 1728, \qquad j\left(e^{2\pi i/3}\right) = 0$$

### 月光猜想（Monstrous Moonshine）

$196884 = 196883 + 1$：$196883$ 是 Monster 群最小非平凡表示的维数。Borcherds（1992）证明了月光猜想，获 Fields 奖。

## M06.5 模方程与奇异模

### 模方程

$n$ 次模方程是联系 $j(\tau)$ 与 $j(n\tau)$ 的代数关系 $\Phi_n(X, Y) = 0$，其中 $\Phi_n$ 为整系数多项式。拉马努金给出 3 次、5 次、7 次等多个次数的模方程，这是他 1914 年 1/π 级数（见 M04）的推导来源。

### 奇异模

当 $\tau$ 为虚二次域中的点时，$j(\tau)$ 为代数整数，称为**奇异模**；椭圆模 $k$ 的值多表为根式与 Gamma 值之比（见 M11）。失落笔记约三分之一关于模方程与奇异模。

## M06.6 Hecke 算子与 L 函数

### Hecke 算子

Hecke 算子 $T_n$ 作用于权 $k$ 模形式；Hecke 特征形式满足 $T_n f = a_n f$，其 Fourier 系数 $a_n$ 即特征值。

### Hecke L 函数

$$L(s, f) = \sum_{n=1}^{\infty} \frac{a_n}{n^s} = \prod_{p} \frac{1}{1 - a_p p^{-s} + p^{k-1-2s}}$$

### 模性定理（Taniyama–Shimura–Weil；Wiles，1994–1995）

每条有理椭圆曲线都是模的：其 L 函数等于某个权 2 新形式的 L 函数。由此推出 Fermat 大定理（见 M01.5）。

## M06.7 theta 函数与 η 函数

### Dedekind η 函数

$$\eta(\tau) = q^{1/24} \prod_{n=1}^{\infty} (1-q^n), \qquad \Delta(\tau) = \eta(\tau)^{24}$$

### Jacobi theta 恒等式

$$\eta(\tau)^3 = \frac{1}{2}\,\theta_2(\tau)\,\theta_3(\tau)\,\theta_4(\tau)$$

由此 $\Delta(\tau) = \left(\frac{\theta_2\theta_3\theta_4}{2}\right)^8$。

### 权 1/2 的 theta 级数

$$\theta(\tau) = \sum_{n=-\infty}^{\infty} q^{n^2} = 1 + 2q + 2q^4 + 2q^9 + \cdots$$

theta 级数是半整权模形式，是平方和问题（M01.1 的四平方定理）的生成函数。

## M06.8 拉马努金的模形式工作

- **τ(n) 的同余式与猜想**（1916）：见 M06.3，$\tau(n) \equiv \sigma_{11}(n) \pmod{691}$ 与 $|\tau(p)| \le 2p^{11/2}$ 的猜想。
- **模方程**：三本笔记中的模方程条目（按次数），是 1/π 级数的推导来源。
- **mock theta**：失落笔记中的 mock theta 函数与模形式的现代联系（见 M08）。

## M06.9 待补充

- 逐条收录笔记中的模方程（按次数）与模函数恒等式，每条注明出处与证明指引。
- Eisenstein 级数与 theta 函数的关系表。
- Atkin–Lehner 理论与新形式（newform）的完整表述。
