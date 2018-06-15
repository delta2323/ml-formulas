# ステートメント

$X_1, \ldots, X_N$を独立な確率変数であり，$\mathbb{E}X_i^2 < \infty$かつ，ある$b > 0$が存在して$X_i < b$ a.s. であると仮定する．$S := \sum_{i=1}^{N} X_i$とすると，任意の$\lambda > 0$に対して，

$$
\psi_S(\lambda) \leq \frac{v}{b^2} \phi (b\lambda) 
$$

が成立する．ここで，$\psi_S$は確率変数の生成母関数の対数，すなわち$\psi_S(\lambda) := \mathrm{\log} \mathbb{E}\left[ e^{\lambda S} \right]$，$v := \sum_{i=1}^N \mathbb{E}\[X_i^2\]$，$\phi(u)$は$Z$をパラメータ$1$のポアソン分布とした時，$Z-1$の生成母関数の対数，すなわち$\phi(u) := e^u-u-1$である．

さらに，任意の$t>0$に対して，

$$
\mathbb{P}\left(S \geq t\right) \leq \exp\left( -\frac{v}{b} h\left( \frac{bt}{v}\right) \right)
$$

が成立する．ここで，$h(u) := (1+u)\log (1+u) - u (u>0)$である．

# コメント

* [Hoeffdingの不等式](hoeffding_inequality.md)を使うには，確率変数$X_i$達の値域が両側が抑えられている必要があるが，Bennettの不等式は片側だけ抑えられていれば使える．そのかわり各確率変数の分散が有限でないといけない．
* 2つ目の不等式は1つ目の不等式と[Chernoff bound](chernoff_bound.md)から導かれる．

# 出典
Boucheron et al. Concentration inequalities: A Nonasymptotic Theory of Independence (2013)
