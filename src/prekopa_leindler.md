# Precopa--Leindlerの不等式

## ステートメント

$\lambda \in (0, 1)$ とする．$f, g, h: \mathbb{R}^n \to [0, \infty)$ は可測関数で，任意の $x, y \in \mathbb{R}^n$ に対して
$$
h((1 - \lambda) x + \lambda y) \geq f(x)^{1 - \lambda} g(y)^{\lambda}
$$
を満たすものとする．このとき，
$$
\int_{\mathbb{R}^n} h(x) d x \geq
\left( \int_{\mathbb{R}^n} f(x) d x \right)^{1 - \lambda}
\left( \int_{\mathbb{R}^n} g(x) d x \right)^{\lambda}
$$
が成り立つ．


## コメント

$\mathbb{R}^n$ 上の絶対連続な確率測度で，密度関数 $\phi$ の対数が凹関数であるもの，すなわち
$$
\phi((1 - \lambda)x + \lambda y) \geq \phi(x)^{1 - \lambda}\phi(y)^{\lambda}
$$
を満たすものを対数凹分布という．Prekopa--Leindlerの不等式から，対数凹分布のいろいろな性質が示せる．

まず，対数凹性は周辺化によって保存する．$\mathbb{R}^{n_1 \times n_2}$ 上の対数凹分布で，密度関数 $\phi(x, y)$ をもつものを考える．$y$ について周辺化した $\mathbb{R}^{n_1}$ 上の確率密度を
$$
\phi_{x}(x) = \int_{\mathbb{R}^{n_2}} \phi(x, y) d y
$$
とする．ここで，$x_1, x_2 \in \mathbb{R}^{n_1}$ を固定し，$h(y) = \phi((1 - \eta)x_1 + \eta x_2)$, $f(y) = \phi(x_1, y)$, $g(y) = \phi(x_2, y)$ に対してPrekopa--Leindlerの不等式を適用すると，
$$
\phi_x((1 - \eta)x_1 + \eta x_2) \geq \phi_x(x_1)^{1 - \eta} \phi_x(x_2)^\eta
$$
が成り立つ．

また，$\mu$ が密度 $\phi$ をもつ対数凹分布であるとき，
$$
\mu((1 - \lambda) A + \lambda B) \geq \mu(A)^{1 - \lambda} \mu(B)^{\lambda}
$$
が成り立つ．これを確認するには，$h(x) = \phi(x) 1_{(1 - \lambda) A + \lambda B}(x)$, $f(x) = \phi(x) 1_{A}$, $g(x) = \phi(x) 1_{B}$ にPrekopa--Leindlerの不等式を適用すればよい．特に，$\mu$ が $\mathbb{R}^n$ の一様測度のときにも成立し，ここから多次元の[Brunn--Minkowskiの不等式](brunn_minkowski.md)が示せる (Boucheron, Lugosi and Massart (2013), Section 4.14)．また，低次元の線形部分空間に縮退したGauss測度でも同様のことが示せる (Gine and Nickl (2015), Theorem 2.4.3).

## 出典

- Boucheron, Lugosi and Massart. Concentration inequalities: A Nonasymptotic Theory of Independence (2013).
- Gine and Nickl. Mathematical Foundations of Infinite-Dimensional Statistical Models (2015).
